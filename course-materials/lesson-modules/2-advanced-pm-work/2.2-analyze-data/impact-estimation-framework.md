# Impact Estimation Framework

**プロダクトマネージャーのためのフィーチャーインパクト見積もりガイド**

---

## 計算式

インパクト見積もりは以下の基本計算式に従います:

```
Impact = Users Affected × Current Action Rate × Expected Lift × Value per Action
```

各コンポーネントを分解しましょう:

---

## 1. Users Affected（影響を受けるユーザー数）

**質問:** このフィーチャーに触れるユーザーは何人ですか？

**例:**
- **All new signups:** 5,000 users/month
- **Existing users who see onboarding:** 70% of signups = 3,500 users/month
- **Enterprise customers only:** 500 users/month

**主な考慮事項:**
- 段階的ロールアウトですか、それとも100%ローンチですか？
- 特定のセグメントをターゲットにしていますか？
- 採用カーブはどうですか？（全員がすぐにフィーチャーを使うわけではありません）

---

## 2. Current Action Rate（現在のアクション率）

**質問:** 現在、望ましいアクションを取っているユーザーの割合は？

**例:**
- **Activation rate:** 45% of signups complete first task
- **Invite rate:** 12% of users invite a teammate
- **Feature adoption:** 23% of users use advanced filters

**見つけ方:**
- アナリティクスツール（Mixpanel、Amplitude）でクエリを実行する
- 使用データをエクスポートしてベースラインを計算する
- 関連する場合はユーザータイプ別にセグメント（小規模チーム vs エンタープライズ）

---

## 3. Expected Lift（期待されるリフト）

**質問:** このフィーチャーはアクション率をどれだけ改善しますか？

**これが最も難しい部分です！** 以下に基づいて根拠ある仮定を立てる必要があります:

**リフト見積もりのソース:**
1. **過去にリリースした類似フィーチャー:** "前回オンボーディングを改善したとき、+8pp のリフトが見られた"
2. **競合ベンチマーク:** "Linear のアクティベーションは65%、私たちは45%、つまり20pp の余地がある"
3. **ユーザーリサーチ:** "調査によると離脱の60%が X が原因なので、X を修正すればその離脱の60%を回復できる可能性がある"
4. **類似フィーチャーの A/B テスト結果:** 自社のヒストリカルデータ
5. **エキスパート判断:** 変更のスコープに基づくエンジニアリング/デザイン/PM の見積もり

**計算例:**
- Current: 45% activation (4,500 out of 10,000 signups complete first task)
- Problem: 60% drop-off between "create task" and "complete task"
- Root cause: Users don't know what to put in tasks (from survey)
- Solution: Guided onboarding with pre-filled example tasks
- Estimate: If 60% drop because of confusion, and we eliminate that confusion, we could recover ~50% of that drop-off (being conservative)
- Math: 60% drop = 6,000 users lost. Recover 50% = +3,000 users. New rate: 7,500/10,000 = 75%... but that seems too optimistic
- Conservative estimate: Recover 30% of drop-off = +1,800 users = 63% activation
- Really conservative: Recover 20% = +1,200 users = 58% activation ← Use this

**プロのヒント:** 見積もりの範囲を限定するために、3つのシナリオ（悲観的、現実的、楽観的）を作成しましょう。

---

## 4. Value per Action（アクションあたりの価値）

**質問:** 各増分アクションはビジネスにとっていくらの価値がありますか？

**アクティベーション改善の場合:**
- Activated user → Paying customer conversion rate: 60%
- Average revenue per user: $12/month
- Average customer lifetime: 24 months
- **Value per activated user:** $12 × 60% × 24 months = $172.80 LTV

**リテンション改善の場合:**
- Each percentage point of retention = X users stay longer
- Extended LTV = retention improvement × ARPU × extended months

**バイラル/招待フィーチャーの場合:**
- Each invite → 40% acceptance rate
- Each accepted invite → 60% activation → 60% conversion
- **Value per invite:** 40% × 60% × 60% × $172.80 LTV = $41.47

---

## すべてを組み合わせる

**例: TaskFlow の Guided Onboarding**

### 現在の状態:
- **Users affected:** 5,000 new signups/month (post-launch, assume 70% see it = 3,500/month)
- **Current action rate:** 45% activation
- **Current activated users:** 2,250/month
- **Value per activation:** $172.80 LTV ($12/mo × 60% conversion × 24 months)

### 予測インパクト（Realistic Scenario）:
- **Expected lift:** 45% → 58% activation (+13 percentage points)
- **New activated users:** 2,030/month (58% of 3,500)
- **Incremental activated users:** +130/month (2,030 - 1,900)
- **Annual value:** 130 × 12 months × $172.80 = $269,856 in LTV
- **Year 1 revenue impact:** 130 × 12 × $12 × 60% = $11,232 MRR = $134,784 ARR

### コスト:
- **Engineering:** 4 engineers × 1 month = $100,000

### ROI:
- **Year 1:** $134,784 revenue / $100,000 cost = 1.35x ROI
- **3-year LTV:** $269,856 / $100,000 = 2.7x ROI

---

## 3つのシナリオアプローチ

不確実性を認めるために、必ず3つのシナリオを作成してください:

### Pessimistic Scenario（悲観的シナリオ、20th percentile）:
- 低い採用率（70%ではなく30%）
- 低いリフト（45% → 58%ではなく45% → 50%）
- 最小限の期待インパクトを計算

### Realistic Scenario（現実的シナリオ、50th percentile）:
- 期待される採用率（70%）
- データに基づく保守的なリフト（45% → 58%）
- 「最も可能性が高い」ケース

### Optimistic Scenario（楽観的シナリオ、80th percentile）:
- 高い採用率（90%）
- 強いリフト + 二次効果（45% → 62% + リテンション改善）
- すべてがうまくいった場合のベストケースシナリオ

**3つすべてをリーダーシップに提示して**、結果の範囲を理解してもらいましょう。

---

## よくある落とし穴

**やってはいけないこと:**
- 100%のユーザーがフィーチャーを使うと仮定する
- 最も楽観的なベンチマークを取る（"Notion は80%のアクティベーション！"）
- 価値計算でコンバージョン率を考慮し忘れる
- あらゆる二次効果を含める（シンプルに保つ）
- 不確実性の範囲なしで単一の数字を提示する

**やるべきこと:**
- 可能な限り自社のヒストリカルデータを使用する
- リフト見積もりは保守的に（約束し過ぎないほうが良い）
- 作業を見せる（前提を明示的にする）
- 複数のシナリオを作成する
- 可能な場合はデータで前提を検証する

---

## インパクト見積もりのテンプレート

```markdown
## Feature: [Name]

### Current State
- Users affected: [number]/month
- Current action rate: [%]
- Current performance: [number] users taking action
- Value per action: $[amount]

### Projected Impact (Realistic Scenario)
- Expected lift: [current%] → [new%] (+[difference]pp)
- New users taking action: [number]/month
- Incremental impact: +[number]/month
- Annual value: [calculation]
- Year 1 revenue: [calculation]

### Investment Required
- Engineering: [cost]
- Design: [cost]
- Other: [cost]
- **Total:** $[total]

### ROI
- Year 1: [revenue] / [cost] = [X]x ROI
- 3-year LTV: [LTV value] / [cost] = [X]x ROI

### Assumptions & Risk
- Assumption 1: [state assumption]
- Assumption 2: [state assumption]
- Risk: [what could go wrong]
- Mitigation: [how to reduce risk]
```

---

**覚えておいてください:** インパクト見積もりは予測ではなく、根拠ある仮説です。目的は完璧に正確であることではなく、より良い意思決定を行うことです。作業を見せ、前提を述べ、学びに応じて見積もりを更新しましょう。
