# Module 3.2.2: 戦略＆アーキテクチャビジュアル

Module 3.2.2: 戦略＆アーキテクチャビジュアルへようこそ！

TaskFlow Mobileのプレゼンは大成功 - リーダーシップは大興奮です。でも今度は、それぞれのステークホルダーがより深い内容を求めています。

CTOは技術アーキテクチャを理解したい。CEOは機能の優先順位付けを見たい。そして取締役会はプロダクトロードマップを見たい。

複雑なアイデアを明確に伝えるビジュアルが必要です。さっそく作りましょう。

STOP: ステークホルダーミーティングの準備はできましたか？

USER: Ready

---

リマインダー：`style-library.html` からスタイルを参照するか、欲しいものをそのまま説明できます。

**Architecture** と **Framework** カテゴリーにはこのモジュールに最適なオプションがあります。

STOP: わかりましたか？

USER: Yes

---

## Part 1: システムアーキテクチャ（CTOミーティング）

最初はCTOミーティングです。

CTOは、TaskFlow Mobileが既存のTaskFlowエコシステムにどう組み込まれるかを理解したいと思っています。以下を示すシステムアーキテクチャダイアグラムを作りましょう：

- **TaskFlow Mobile app** - 新しく構築するもの
- **TaskFlow Backend API** - 既存のバックエンド
- **Database layer** - データ用のPostgreSQL、キャッシュ用のRedis
- **Third-party integrations** - プッシュ通知、アナリティクス
- **Data flow** - コンポーネント間の情報の流れ

これは「すべてがどうつながっているのか？」に答えるダイアグラムです。

STOP: TaskFlow Mobileのシステムアーキテクチャダイアグラムを作成するよう依頼してください。

USER: Create a system architecture diagram / Generate the architecture diagram

ACTION: Generate system architecture diagram
- TaskFlow Mobile connecting to TaskFlow Backend API
- Backend connecting to PostgreSQL database and Redis cache
- Third-party services: push notifications (Firebase), analytics (Mixpanel)
- Show data flow arrows between components
- Clean, technical style suitable for engineering review (style #34 or similar)
- 16:9 aspect ratio
- Save to outputs folder with descriptive name

ACTION: Provide the path to the output image so user can view it.

`outputs/` フォルダでアーキテクチャダイアグラムを確認してください。

STOP: パーツ同士のつながりが明確に示されていますか？

USER: Response

ACTION: If user wants changes, iterate on the diagram. If satisfied, continue.

これでCTOは、TaskFlow Mobileが既存システムにどう統合されるかが一目でわかります。

この同じアプローチは、必要なあらゆるダイアグラムに使えます - システムアーキテクチャ、データフロー、組織図、ネットワークトポロジー、何でも。コンポーネントとその接続方法を説明するだけです。

STOP: CEOミーティングの準備はできましたか？

USER: Yes

---

## Part 2: 戦略フレームワーク（CEOミーティング）

次はCEOミーティングです。

CEOは機能の優先順位付けを見たい - 何を最初に作り、なぜなのか。2x2マトリクスがぴったりです：**Impact vs Effort**。

TaskFlow Mobileの主要機能をマッピングしましょう：

- **Quick Wins**（高Impact、低Effort）：タスク更新のプッシュ通知、オフラインタスク閲覧
- **Major Projects**（高Impact、高Effort）：デバイス間リアルタイム同期、チームチャット統合
- **Fill-ins**（低Impact、低Effort）：カスタムテーマ、ウィジェットサポート
- **Avoid**（低Impact、高Effort）：音声コマンドサポート、ARタスク可視化

STOP: TaskFlow Mobile機能の2x2優先順位付けマトリクスを作成するよう依頼してください。

USER: Create a prioritization matrix / Generate the 2x2 matrix

ACTION: Generate 2x2 prioritization matrix
- X-axis: Effort (Low → High)
- Y-axis: Impact (Low → High)
- Four quadrants labeled: Quick Wins, Major Projects, Fill-ins, Avoid
- Plot the features mentioned above in appropriate quadrants
- Clean corporate style suitable for executive presentation (style #5 or similar)
- 1:1 or 16:9 aspect ratio
- Save to outputs folder with descriptive name

ACTION: Provide the path to the output image so user can view it.

`outputs/` フォルダで優先順位付けマトリクスを確認してください。

STOP: マトリクスが優先順位のロジックをビジュアルに明確にしているのがわかりますか？

USER: Response

ACTION: If user wants changes, iterate on the matrix. If satisfied, continue.

これでCEOは、何を最初に作り、なぜなのかが一目でわかります。

そしてこれは、想像できるあらゆるフレームワークに使えます - 2x2マトリクス、ピラミッド、ベンダイアグラム、キャンバス、ファネルなど何でも。同じプロセスです：構造を説明し、どこに何が入るかをリストし、スタイルを指定する。スタイルライブラリを参照することも、ゼロから説明することもできます。

STOP: 取締役会ミーティングの準備はできましたか？

USER: Yes

---

## Part 3: プロダクトロードマップ（取締役会ミーティング）

最後は取締役会ミーティングです。

取締役会は全体像を見たい - いつ出荷し、フェーズドロールアウトはどうなるのか。

3四半期にわたるTaskFlow Mobileのロードマップを作りましょう：

- **Q1: MVP Launch** - コアタスク管理、プッシュ通知、オフライン閲覧
- **Q2: Team Features** - リアルタイム同期、チームチャット統合、共有タスクリスト
- **Q3: Enterprise** - 管理コントロール、SSO統合、高度なアナリティクス

MVPからエンタープライズ対応までの明確な道筋を示します。

STOP: TaskFlow Mobileのプロダクトロードマップを作成するよう依頼してください。

USER: Create a product roadmap / Generate the roadmap

ACTION: Generate product roadmap visualization
- Timeline showing Q1, Q2, Q3
- Each quarter with key milestones/features
- Q1: MVP (core features)
- Q2: Team features (collaboration)
- Q3: Enterprise (admin/security)
- Clean, modern style suitable for board presentation (style #88 or similar)
- 16:9 aspect ratio
- Save to outputs folder with descriptive name

ACTION: Provide the path to the output image so user can view it.

`outputs/` フォルダでロードマップを確認してください。

STOP: プロダクトがどう進化するか、明確なストーリーになっていますか？

USER: Response

ACTION: If user wants changes, iterate on the roadmap. If satisfied, continue.

これで取締役会は、時間軸に沿った戦略ビジョンを見ることができます。

これは必要なあらゆるタイムラインやシーケンスに使えます - ロードマップ、ガントチャート、リリース計画、移行スケジュール。期間を定義し、各期間に入るものをリストし、スタイルを説明する。毎回同じプロセスです。

STOP: まとめに入る前にもう1つあります。

USER: Yes

---

## スタイルライブラリを育てる

覚えておいてください：いつでもスタイルデータベースに独自のスタイルを追加できます。

オンラインで気に入ったダイアグラムスタイルを見つけた？抽出して保存しましょう。このモジュールでうまくいったものがあった？ライブラリに追加しましょう。

フレームワークやダイアグラムのインスピレーション源として **https://slidemodel.com/** がおすすめです - 気に入ったスタイルを見つけ、スクリーンショットを撮り、スタイル抽出を使って自分の目的にクローンしましょう。

時間とともに、あらゆるシチュエーションに対応するスタイルのコレクションが出来上がります。

スタイルの追加方法を復習したい場合は、Module 3.1.4を再訪してください。

STOP: わかりましたか？

USER: Yes

---

## まとめ

作成したものを振り返りましょう：

1. **CTO向けのシステムアーキテクチャダイアグラム**
2. **CEO向けの2x2優先順位付けマトリクス**
3. **取締役会向けのプロダクトロードマップ**

3人の異なるステークホルダー、3つの異なるビジュアルニーズ - すべて対応完了です。

これらのテクニックは、あらゆる戦略的・技術的コミュニケーションに使えます：
- アーキテクチャレビュー
- 戦略プレゼンテーション
- プランニングセッション
- 取締役会への報告

STOP: 次に進む前に質問はありますか？

USER: Questions or ready to continue

---

次のモジュールでは、マーケティングとアナウンスメントのビジュアル - 広告、フィーチャーグラフィック、ローンチアセットに取り組みます。

`/start-3-2-3` と入力して続けましょう。

---

## Important Notes for Claude

- **File paths:** Always provide absolute paths when telling users where to find files.
- **Image generation:** Use the `image_gen.py` module via Python. Start a new session at the beginning of each major generation to keep sessions clean.
- **Style library:** If user references a style number, look up the prompt in `style-library.html` (in the 3.1.4 module folder).
- **Iteration:** If any image doesn't turn out well, offer to regenerate or refine it. Use the session to iterate.
- **Output naming:** Use descriptive names like `taskflow_system_architecture.png`, `feature_prioritization_matrix.png`, `product_roadmap_q1_q3.png`.
- **Technical accuracy:** For the architecture diagram, ensure the components and connections make logical sense for a mobile app backend.
- **Opening images:** If a user is having trouble finding an image, offer to open it for them using `open [path]` (Mac) or `start [path]` (Windows).

## Success Criteria

このモジュールは、受講者が以下を達成した時点で完了です：
- [ ] TaskFlow Mobileの技術スタックを示すシステムアーキテクチャダイアグラムを生成した
- [ ] Impact/Effortで機能をプロットした2x2優先順位付けマトリクスを生成した
- [ ] 3四半期のフェーズドロールアウトを示すプロダクトロードマップを生成した
- [ ] スタイルライブラリにカスタムスタイルを追加できることを理解した（Module 3.1.4への参照）
- [ ] これらのテクニックがあらゆる戦略的・技術的ビジュアルニーズに応用できることを理解した
