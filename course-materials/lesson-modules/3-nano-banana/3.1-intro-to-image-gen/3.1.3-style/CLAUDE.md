# Module 3.1.3: 一貫性とスタイル

おかえりなさい！画像の生成方法とイテレーションの仕方はもう学びましたね。さあ、レベルアップしましょう。

このモジュールでは一貫性とスタイルがテーマです。終わる頃には、プロのようにプロンプトを書く方法、参照画像を使って特定のルックを再現する方法、そしてバリエーションを生成してさまざまな方向性を探る方法がわかるようになります。

STOP: 始める準備はできましたか？

USER: はい

---

## Part 1: プロンプトのゴールデンルール

Google は Gemini の画像生成のための公式プロンプトガイドを公開しています。「ゴールデンルール」と呼ばれる4つのルールがあります：

**ルール 1: リロールせずに編集する** - 画像が80%正しければ、最初からやり直すのではなく、具体的な変更を指示しましょう。これは 3.1.2 で学びました。

**ルール 2: 自然言語とフルセンテンスを使う** - 人間のアーティストに説明するようにブリーフィングしましょう。「タグスープ」ではなく。オンラインで JSON プロンプトライブラリを見かけることがありますが、Gemini での古いやり方です。今はシンキングモデルなので、厳格な構造化は必要ありません。

**ルール 3: 具体的かつ詳細に記述する** - 被写体、設定、ライティング、ムード、テクスチャ、マテリアルを定義しましょう。深く掘り下げてください。

**ルール 4: コンテキストを提供する** - 「なぜ」「誰のために」を伝えることで、シンキングモデルがよりスマートなクリエイティブ判断を下せるようになります。

STOP: 一つずつ見ていきます。ここまで大丈夫ですか？

USER: はい

---

ルール 1 は前のモジュールで学びました - Gemini がシンキングモデルなので、会話を続けることでより多くのコンテキストが得られ、うまく機能します。

では残りの3つのルールを実際に見てみましょう。それぞれのルールで2つのバージョンを同時に生成して、違いを並べて比較できるようにします。

コンセプトはあなたが選んでください - テクニックは私がお見せします。

STOP: 実際に見てみる準備はできましたか？

USER: はい

---

### ルール 2: 自然言語 vs タグスープ

ルール 2 から始めましょう。

「タグスープ」とは、Midjourney や Stable Diffusion などの初期の画像モデルで普及したプロンプトスタイルで、カンマ区切りのキーワードを詰め込む方法です：

```
cat, orange tabby, sitting, window, sunlight, cozy, warm lighting, 8k, hyperrealistic, bokeh, soft focus
```

自然言語は...普通に書くだけです：

```
An orange tabby cat sitting on a windowsill, bathed in warm afternoon sunlight. The scene feels cozy and intimate, with soft focus on the background.
```

どちらも機能しますが、Gemini は自然言語で学習されています。違いを見てみましょう。

STOP: 何のコンセプトでデモを見たいですか？被写体やシーンを教えてください - 何でも構いません。

USER: [コンセプトを指定]

---

いいですね。タグスープと自然言語の違いをお見せします。

両方のバージョンを今生成して、直接比較できるようにします。

ACTION: Generate two images in parallel:
- Tag soup version: comma-separated keywords, no sentences
- Natural language version: full sentences describing the same scene

ACTION: Save both images with descriptive names

それぞれのプロンプトはこちらです：
- **タグスープ:** [タグスーププロンプトを共有]
- **自然言語:** [自然言語プロンプトを共有]

`outputs/` フォルダで両方の画像を確認してください：
- `[concept]_tag_soup.png`
- `[concept]_natural_language.png`

STOP: 両方を見てみてください - 何か気づいたことはありますか？

USER: [観察を述べる]

---

実はかなり似ていると思ったかもしれません。それがポイントなんです。

どちらのアプローチでも良い結果が出ます。でも自然言語の方が...単純に楽なんです。特別な構文を覚えたり、フォーマットを気にする必要がありません。デザイナーに話すように説明するだけです。そして、プロンプトを書くのは私がいつでもお手伝いできますよ。

STOP: 次のルールに進みましょうか？

USER: はい

---

### ルール 3: 具体的かつ詳細に記述する

これは楽しいですよ。ルール 3 は被写体、設定、ライティング、ムード、テクスチャ、マテリアルなど、すべてを定義することです。

Gemini について知っておいてほしいこと：とても多くの詳細を処理できます。想像以上に多くのことを。そして非常に詳細なプロンプトでも驚くほど一貫した結果を出します。

遠慮せず書いてください。もっと詳細を追加する方法がわからなければ、聞いてください - プロンプトの拡張をお手伝いします。

STOP: このデモでは何を作りたいですか？新しいコンセプトを教えてください。

USER: [コンセプトを指定]

---

いい選択ですね。あいまいなプロンプトと詳細なプロンプトの違いをお見せします。

あいまいなバージョンはシンプルな一文の説明にします。詳細なバージョンでは全力を出します - ライティング、テクスチャ、雰囲気、マテリアル、構図、すべてを盛り込みます。

ACTION: Generate two images in parallel:
- Vague prompt: simple, minimal description
- Detailed prompt: extensive description with lighting, mood, textures, materials, atmosphere, composition

ACTION: Save both images with descriptive names

使ったプロンプトはこちらです：
- **あいまい:** [あいまいなプロンプトを共有]
- **詳細:** [詳細なプロンプトを共有 - どれだけ詳しく書いたか見せる]

ACTION: View the images yourself and note the differences

`outputs/` フォルダを確認してください：
- `[concept]_vague.png`
- `[concept]_detailed.png`

STOP: 比べてみてください - 詳細さの違いがわかりますか？

USER: [回答]

---

詳細なバージョンは Gemini にはるかに多くの情報を与えます。そしてすごいのは - 実際にすべての詳細に従っているところです。指定したライティング？そのまま反映されています。テクスチャ？同様です。

とことん具体的に書くことを恐れないでください。行き詰まったら、プロンプトの拡張をお手伝いしますので聞いてください。

STOP: 最後のルールに進みましょうか？

USER: はい

---

### ルール 4: コンテキストを提供する

これは Gemini に「なぜ」「誰のために」を伝えるルールです。

コンテキストはモデルが目的を理解し、適切なクリエイティブ判断を下すのに役立ちます。「絵本のための」ポートレートと「ラグジュアリーブランドの広告のための」ポートレートでは、まったく異なる仕上がりになります。

STOP: 何を作りたいですか？追加するコンテキストの選択肢を提案しますね。

USER: [コンセプトを指定]

---

いいですね。そのコンセプトに合うコンテキストの選択肢はこちらです：

ACTION: Generate context options dynamically based on what makes sense for the user's concept (e.g., "for a children's book illustration", "for a luxury brand advertisement", "for a tech startup landing page", "for a vintage poster design")

STOP: この中から選ぶか、自分でコンテキストを提案してください。

USER: [コンテキストを選択]

---

コンテキストなしとコンテキストありの2つのバージョンを生成します。

ACTION: Generate two images in parallel:
- No context: just the subject description
- With context: same subject plus the "why" / "for whom"

ACTION: Save both images with descriptive names

ACTION: Review both images and identify specific differences

気づいたこと：[コンテキストが結果にどう影響したか具体的に共有 - 何が変わったかを詳しく説明]

`outputs/` フォルダを確認してください：
- `[concept]_no_context.png`
- `[concept]_with_context.png`

STOP: コンテキストがクリエイティブの方向性をどう変えたか、わかりますか？

USER: [回答]

---

これでゴールデンルールのまとめです：
1. **リロールせずに編集する** - うまくいっているものをイテレーションする
2. **自然言語を使う** - デザイナーに話すように
3. **具体的かつ詳細に記述する** - Gemini は詳細を処理できる
4. **コンテキストを提供する** - 「なぜ」を伝える

すべての画像生成作業でこれらを念頭に置いてください。大きな違いが出ます。

STOP: 参照画像に進みましょうか？

USER: はい

---

## Part 2: 参照画像

ここからが本当にパワフルな機能です。

Gemini にスタイルや被写体のガイドとして参照画像を提供できます。ブランドの一貫性を保つ、特定のルックを再現する、キャラクターの見た目を正確にするなど、非常に重要な機能です。

まずは単一のスタイルリファレンスから始めましょう。

ACTION: Read the `style-reference.jpeg` file to understand its visual style

ACTION: Tell user where to find `style-reference.jpeg` so they can view it

これはダイナミックでエネルギッシュなバスケットボールのランディングページです - 大胆でインパクトのあるデザイン。素晴らしいビジュアルスタイルですね。

STOP: このスタイルで何を作ってほしいですか？まったく違う被写体を教えてください。

USER: [被写体を指定]

---

ACTION: Generate an image using `style-reference.jpeg` as a style reference with the user's subject

ACTION: Save with descriptive name

`outputs/` フォルダでスタイル適用済みの画像を確認してください。

STOP: 見てみてください - あの大胆でダイナミックなビジュアルスタイルがあなたの被写体にどう反映されているかわかりますか？

USER: [回答]

---

これはブランドの一貫性を保つのに非常に便利です。気に入ったスタイルがあれば、参照画像として入力するだけです。

次はもう少し高度なことを試してみましょう - 複数の参照画像です。

Carl の猫 Winter と Piper をフィーチャーした「APEX CAT」というキャットフードのランディングページを作ります。

ACTION: Tell users where they can find the cat images (Winter 1-3, Piper 1-2)

STOP: Winter と Piper の写真は見つかりましたか？

USER: [確認]

---

以下を組み合わせます：
- `style-reference.jpeg` - あの大胆でダイナミックなビジュアルスタイル
- Winter（黒いふわふわの猫）の写真 - 3枚すべて
- Piper（グレー/クリーム色のふわふわの猫）の写真 - 2枚とも

プロのコツ：同じ被写体の参照写真を複数提供すると、はるかに良い結果が得られます。モデルがさまざまな角度やライティング条件から被写体を理解できるため、より正確に表現できるようになります。

ACTION: Generate an "APEX CAT" landing page combining style reference + all 5 cat photos

ACTION: Save with descriptive name like `apex_cat_landing_page.png`

`outputs/` フォルダで結果を確認してください。

STOP: どうですか？2匹の猫の特徴がランディングページスタイルに反映されているのがわかりますか？

USER: [回答]

---

これが参照画像のパワーです：
- **単一の参照画像** - スタイルの適用
- **複数の参照画像** - 被写体の精度向上
- **組み合わせ** - ある画像からスタイル、別の画像から被写体

STOP: Part 3 のグリッドとバリエーションに進みましょうか？

USER: はい

---

## Part 3: グリッドとバリエーション

被写体の複数のビューやバリエーションが必要な場合があります。グリッドはこれに最適です - キャラクターシート、スプライトシート、プロダクトのアングル、何にでも使えます。

Winter を使って 3x3 のビデオゲームキャラクタースプライトシートを作りましょう。

STOP: Winter の写真を使ってキャラクタースプライトシートの生成を頼んでみてください。

USER: Winter の写真を使ってキャラクタースプライトシートを生成して

---

ACTION: Generate a 3x3 grid sprite sheet using Winter reference photos
- 9 different poses/actions of Winter as a video game character
- Consistent style across all 9 cells

ACTION: Save as `winter_sprite_sheet.png`

`outputs/` フォルダでスプライトシートを確認してください。

一貫性の確保に最適です - 同じキャラクターで異なるアングルやポーズ、すべて同じデザイン言語で統一されています。

STOP: 9つのポーズすべてが同じキャラクターデザインを維持しているのがわかりますか？

USER: [回答]

---

もう一つグリッドを試してみましょう - ちょっとメタな内容です。

先ほどプロンプトのゴールデンルールを学びましたね。そのルールについてのティーチングスライドを画像生成で作ったらどうでしょう？

STOP: ゴールデンルールについての8スライドのプレゼンテーションを生成するよう頼んでみてください。

USER: ゴールデンルールについての8スライドのプレゼンテーションを生成して

---

ACTION: Generate a 2x4 grid (8 slides) teaching the Golden Rules of prompting
- Slide 1: Title slide - "Golden Rules of Image Prompting"
- Slide 2: Overview - the 4 rules at a glance
- Slides 3-6: One slide per rule with visual example
- Slide 7: Quick reference cheat sheet
- Slide 8: "Now go create!" closing slide
- Consistent visual style across all slides

ACTION: Save as `golden_rules_slides.png`

`outputs/` フォルダでスライドを確認してください。

何をしたかわかりますか？ツールを使ってツールについてのティーチングコンテンツを作ったんです。グリッドはプレゼンテーション、チュートリアル、またはビジュアルの一貫性が必要なあらゆるコンテンツに非常に便利です。

STOP: かなりメタですよね？バリエーションに進みましょうか？

USER: [回答]

---

ではバリエーションについて話しましょう。

重要なことをお伝えします：LLM には固有のランダム性があり、画像生成では特にそうです。まったく同じプロンプトでも、毎回異なる結果が出ます。

これをバグではなくフィーチャーとして活用しましょう。

1枚の画像を生成して当たることを祈るのではなく、同じプロンプトで2-3個のバリエーションを生成しましょう。そしてお気に入りを選んで、それをイテレーションするのです。

STOP: 先ほどのデモの中から、さらに探ってみたいコンセプトを選んでください。忘れてしまったら `outputs/` フォルダを確認してください。

USER: [コンセプトを選択]

---

ACTION: Generate 3 variants of the user's chosen concept using the SAME prompt each time
- Call new_session() before each generation to ensure fresh results
- Use identical prompts to demonstrate the natural variation

ACTION: Save as `[concept]_variant_1.png`, `[concept]_variant_2.png`, `[concept]_variant_3.png`

`outputs/` フォルダを確認してください - 同じプロンプトから3つの異なるバージョンが見られるはずです。

STOP: どのバリエーションが一番好きですか？

USER: [お気に入りを選択]

---

いい選択ですね。では、その方向性をさらに発展させましょう。

これがワークフローです：バリエーションを生成し、ベストを選び、それを磨いていく。

STOP: 選んだバリエーションの何を変えたい、または強化したいですか？

USER: [フィードバックを提供]

---

ACTION: Continue the session to refine the chosen variant based on user feedback

ACTION: Save the refined version

これが完全なクリエイティブワークフローです：
1. **バリエーションを生成** して方向性を探る
2. **お気に入りを選ぶ**
3. **具体的なフィードバックでイテレーションする**

STOP: このワークフローでクリエイティブの方向性をどうコントロールできるか、わかりますか？

USER: [回答]

---

## まとめ

素晴らしい仕事です！学んだことを振り返りましょう：

**ゴールデンルール：**
- リロールせずに編集する
- 自然言語を使う
- 具体的かつ詳細に記述する
- コンテキストを提供する

**参照画像：**
- 単一の参照画像でスタイルを適用
- 複数の参照画像で被写体の精度を向上
- スタイルと被写体の参照画像を組み合わせる

**グリッドとバリエーション：**
- グリッドでポーズ/アングルの一貫性を確保
- バリエーションで方向性を探り、ベストをイテレーション

STOP: 次に進む前に質問はありますか？

USER: [質問または続ける準備ができた]

---

次のモジュールでは、スタイルデータベースを構築して、お気に入りのスタイルを保存・再利用できるようにします。既存の画像を分解してオリジナルのクリエイティブツールキットを構築する方法を学びます。

STOP: Module 3.1.4 の準備ができたら教えてください

USER: 準備できました

`/start-3-1-4` を実行して続けてください。

---

## Claude への重要な注意事項

このモジュールを実行する際の注意：

1. **わかりやすいファイル名** - 出力を保存する際は常に意味のある名前を使用してください（例：`coffee_shop_warm_light.png`、連番ではなく）

2. **プロンプトを共有する** - 比較画像を生成する際は、テクニックを学べるよう、使用したプロンプトを必ずユーザーに見せてください

3. **自分で画像を確認する** - 違いについてコメントが必要なデモでは、実際に生成された画像を見て具体的な観察を述べてください

4. **動的なコンテキストオプション** - ルール 4 のコンテキストオプションを提案する際は、ユーザーの具体的なコンセプトに合った選択肢を生成してください

5. **猫の写真の場所** - 猫の写真（Winter 1-3、Piper 1-2）と style-reference.jpeg はモジュールフォルダにあります。ユーザーに正確なパスを伝えてください。

6. **バリエーションのワークフロー** - バリエーションを生成する際は、自然なランダム性を実証するために毎回同じプロンプトを使用してください

7. **画像を開く** - ユーザーが画像を見つけるのに困っている場合は、`open [path]`（Mac）または `start [path]`（Windows）を使って画像を開くことを提案してください

## 成功基準

モジュールの完了条件：
- [ ] ユーザーが4つのゴールデンルールすべての説明を受けた
- [ ] ユーザーが3つの比較デモを完了した（タグスープ vs 自然言語、あいまい vs 詳細、コンテキストなし vs コンテキストあり）
- [ ] ユーザーが単一のスタイルリファレンスを使用した
- [ ] ユーザーが複数画像の APEX CAT デモを見た
- [ ] ユーザーがグリッド/スプライトシートを生成した
- [ ] ユーザーがバリエーションを生成し、お気に入りをイテレーションした
- [ ] ユーザーが `/start-3-1-4` に案内された
