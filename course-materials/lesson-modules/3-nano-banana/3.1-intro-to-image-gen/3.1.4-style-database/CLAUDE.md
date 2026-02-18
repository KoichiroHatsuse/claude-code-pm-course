# Module 3.1.4: スタイルデータベースの構築

Module 3.1.4: スタイルデータベースの構築へようこそ。

ここまで画像の生成方法とゴールデンルールの適用を学びました。でも、ここからが本番です - カジュアルユーザーとパワーユーザーを分ける大きなステップがあります。

メタスキルはこれです：時間をかけて成長する、パーソナルなクリエイティブツールキットを構築すること。毎回ゼロから始めるのではなく、再利用できるスタイルのライブラリを作るのです。

考えてみてください - 作成した素晴らしい画像、完璧に機能したプロンプト、発見したスタイル...すべてがあなたのツールキットの一部になります。これが AI をたまに使うだけの人と、AI をクリエイティブのスーパーパワーとして持つ人の違いです。

STOP: ここまで大丈夫ですか？

USER: はい

---

ここで Claude Code があなたの完璧なパートナーになります。スタイルデータベース全体を管理できるんです。「スタイル #3 を使って」や「これをライブラリに追加して」と言うだけで、すべて私が処理します - 完全なコンテキスト付きで、コピペも過去のチャット探しも不要です。

ライブラリを成長させる方法は3つあります：
- **作りながら保存** - 気に入ったものができたとき
- **オンラインから収集** - データベース、SNS、チュートリアルから
- **任意の画像からスタイルを抽出** - これが最強の技

今日は3つすべてを試します。

スターターのスタイルライブラリを用意しました。ブラウザで自動的に開きますね。

ACTION: Open the style library in the user's browser:
- Mac: `open [absolute path to style-library.html]`
- Windows: `start [absolute path to style-library.html]`

ブラウザで開いたはずです。

STOP: スタイルライブラリを見てみてください。一通り見終わったら教えてください。

USER: 開きました

---

## Part 2: スタイルライブラリの紹介

大事な補足です：これは本物のウェブサイトではありません！ローカルの HTML ファイルで、コンピュータから直接スタイルコレクションを見るための仕組みです。

そしてすごいところは：デザインや機能はいつでも変更できるということです。今すぐやる必要はありませんが、将来的には新しいカラムの追加、レイアウトの変更、検索機能の追加など、何でも頼んでください。あなたのツールキットです。自分に合うようにカスタマイズしてください。

STOP: なかなかいいでしょう？

USER: はい

---

構造を説明しますね。各スタイルには以下があります：
- **インデックス番号** - 「スタイル #02 を使って」と言えるように
- **サムネイルプレビュー** - ホバーで拡大
- **名前とタグ** - すばやく見つけるために
- **カテゴリ** - フィルタリング用
- **フルプロンプト** - ホバーで展開、クリックでコピー
- **使用例** - いつ使うかがわかるように

上部のフィルタボタンでカテゴリ別に表示してみてください。

STOP: 少し時間をかけて見てみてください。どのスタイルが気になりますか？

USER: [スタイルを選択]

---

いい選択ですね！試してみましょう。

STOP: そのスタイルで何の被写体を生成したいですか？スタイル番号と被写体を教えてください。

USER: [スタイル番号と被写体]

ACTION: Run `python3 get_style.py [number]` to get the style prompt. Then generate an image using that prompt combined with their subject.

画像ができました！

ACTION: Provide the exact path to the output image file

outputs フォルダを開いて確認してください。

STOP: どうですか？

USER: [回答]

---

## Part 3: ライブラリの成長 - 方法 1: 作りながら保存

これがライブラリの使い方の1つ目 - 既存のスタイルを選ぶこと。次はライブラリを成長させる方法について話しましょう。

方法 1 は一番シンプルです：作りながら保存。気に入ったものができたら、ライブラリに追加するよう私に言うだけです。

試してみましょう。好きな画像を何でも生成してください。

STOP: 何を作りたいですか？被写体、スタイル、何でも構いません - 好きなように説明してください。

USER: [画像を説明]

---

ACTION: Generate the image based on their description using image_gen.py

できました！outputs フォルダで画像を確認してください。

ACTION: Provide the exact path to the output image file

STOP: 見てみてください - このスタイルは気に入りましたか？

USER: [回答]

---

気に入ったなら、このスタイルを将来使えるようにライブラリに保存できます。

STOP: 試してみてください - このスタイルをライブラリに追加するよう言ってみてください。

USER: ライブラリに追加して / このスタイルをライブラリに追加して

ACTION: Update style-library.html with the new style entry:
- Find the next available ID number
- Extract a descriptive name from the prompt
- Choose an appropriate category from: Illustration, Photo - Portrait, Photo - Product, Photo - Environment, Diagram, UI/Mockup, 3D/Isometric, Presentation, Marketing, Artistic
- Add 3-5 relevant tags
- Copy the output image to the thumbnails/ folder with a descriptive filename
- Add the entry to the styles array in the JavaScript section
- Write a brief "exampleUse" description

完了です！ブラウザでスタイルライブラリを更新してください。

STOP: 新しいスタイルが表示されていますか？

USER: はい

---

これが方法 1 - 作りながら保存です。気に入ったものができるたびに、保存するよう言ってください。時間が経つにつれて、ライブラリは実証済みスタイルの宝庫になります。

STOP: 方法 2 に進みましょうか？

USER: はい

---

## Part 4: ライブラリの成長 - 方法 2: オンラインから収集

方法 2：オンラインからプロンプトを収集。SNS、プロンプトデータベース、チュートリアルには素晴らしいプロンプトがたくさんあります。気に入ったものを見つけたら、テストして、ライブラリに追加しましょう。

公式 Nano Banana アカウントからの好例です：https://x.com/NanoBanana/status/1998085942201163905

プロンプトはこちらです："Make a photo that is perfectly isometric. It is not a miniature, it is a captured photo that just happened to be perfectly isometric. It is a photo of [subject]."

STOP: アイソメトリック写真にはどんな被写体を使いましょうか？

USER: [被写体を指定]

---

ACTION: Generate an isometric image with their subject using the prompt: "Make a photo that is perfectly isometric. It is not a miniature, it is a captured photo that just happened to be perfectly isometric. It is a photo of [their subject]."

アイソメトリック写真をご覧ください！

ACTION: Provide the exact path to the output image file

outputs フォルダを開いて確認してください。

STOP: なかなかクールなエフェクトですよね？このスタイルをライブラリに追加しますか？

USER: はい / ライブラリに追加して

ACTION: Update style-library.html with the isometric style:
- Name: "Perfect Isometric Photo"
- Category: "3D/Isometric"
- Tags: ["isometric", "photography", "geometric", "perspective"]
- Prompt: "Make a photo that is perfectly isometric. It is not a miniature, it is a captured photo that just happened to be perfectly isometric. It is a photo of [subject]."
- Copy the output image to thumbnails/
- Add entry to styles array

完了です！ブラウザを更新して確認してください。

STOP: 2つのスタイルが追加されました！最強の技に進みましょうか？

USER: はい

---

## Part 5: ライブラリの成長 - 方法 3: 任意の画像からスタイルを抽出

方法 3 が最強の技です。

Gemini 3 Pro は画像の生成だけでなく、あらゆるモデルの中で最高の画像理解力を持っています。つまり、あらゆる画像からスタイルを抽出して再現できるのです。

Pinterest で気に入った画像を見つけた？Instagram？雑誌？スタイルを抽出して、永久に保存できます。

まさにこれを行うスタイル抽出モジュールを構築しました。

STOP: 実際に動くところを見たいですか？

USER: はい

---

ACTION: Confirm the style_extract.py file exists in the lesson-modules/3-nano-banana/ directory

`style_extract.py` モジュールは任意の画像を分析して、詳細なスタイル情報を抽出します。JSON や構造化データではなく、Gemini が直接使える自然言語として出力されます。

キャプチャされるもの：カラーパレット、ライティング、構図、テクスチャ、ムード、アーティスティックスタイル、タイポグラフィ、特殊エフェクト - 画像の見た目を構成するすべての要素です。

意図的に難しい画像でテストしてみましょう。

ACTION: Get the exact path to recursive-painter.jpg in this module folder

このファイルを開いて見てください：[正確なパスを提示]

STOP: 見えますか？自分自身を描いている自分を描いている男性で、CRT テレビに同じシーンが映っています - 1990年代のデイトスタンプ付きの美学です。

USER: はい、見えます

再帰的で、複雑で、レイヤーが重なっています。このスタイルが抽出できれば、何でも抽出できます。

STOP: 抽出を実行する準備はできましたか？

USER: はい

---

ACTION: Run the style extraction on recursive-painter.jpg by executing:
```python
import sys
sys.path.insert(0, '[course root path]')
from style_extract import extract_style
result = extract_style('[path to recursive-painter.jpg]')
print(result)
```

抽出結果はこちらです：

ACTION: Display the extracted style description to the user

[出力を明示的に表示]

この詳細さを見てください - カラーパレット、ライティングの質、構図のメモ、テクスチャの説明。

さて、本当のテストです：このテキスト記述だけで、まったく同じ画像を再現できるでしょうか？

STOP: 抽出されたスタイルを使って画像を再現するよう言ってみてください。

USER: 画像を再現して / 生成して

---

ACTION: Generate an image using the extracted style description. The prompt should recreate the recursive painter scene - a man in an art studio painting himself painting himself, with a CRT TV showing the same recursive scene, 1990s analog snapshot aesthetic with datestamp.

ACTION: Provide the exact path to the output image file

出力を開いて、オリジナルと並べて比較してください。

STOP: どう思いますか？同じスタイルが再現されているのがわかりますか？

USER: [回答 - 感動するはず]

---

これがすごい瞬間です。

複雑でレイヤーが重なった再帰的な画像からエッセンスをテキストとして抽出し、それをゼロから再現しました。

気に入った画像でこれができると想像してみてください - キャプチャしたいスタイルならどんなものでも。Pinterest のインスピレーション → 抽出 → 保存 → 永久にあなたのもの。

STOP: この抽出されたスタイルをライブラリに追加しますか？

USER: はい / 追加して

ACTION: Update style-library.html with the 90s Analog Snapshot style:
- Name: "90s Analog Snapshot"
- Category: "Photo - Portrait"
- Tags: ["vintage", "film grain", "flash", "nostalgic", "datestamp"]
- Prompt: Use the extracted style description
- Copy the generated output image to thumbnails/
- Add entry to styles array

ブラウザを更新してください - 3つの新しいスタイルが追加されました！

STOP: ライブラリはどんな感じですか？

USER: [回答]

---

## Part 6: まとめ

学んだことを振り返りましょう。

メタスキル：時間をかけて成長する、パーソナルなクリエイティブツールキットを構築すること。ライブラリを成長させる3つの方法：
- **作りながら保存** - 気に入ったものを作ったら → 追加
- **オンラインから収集** - プロンプトを見つけたら → テスト → 保存
- **任意の画像からスタイルを抽出** - 最強の技

気に入った画像 → 抽出 → 保存 → 永久に再利用。そしてすべて私が管理します - 「スタイル #3 を使って」や「これをライブラリに追加して」と言うだけです。

STOP: スタイルデータベースの構築について質問はありますか？

USER: [質問またはなし]

---

これで Nano Banana Pro を使うために必要な知識はすべて揃いました。ゴールデンルール、イテレーションの方法、スタイルツールキットの構築方法を身につけました。

Module 3.2 では、これらの学びをすべて実際の PM ユースケースに適用します - モックアップ、ダイアグラム、プレゼンテーションなど。

STOP: Module 3.2 に進む準備はできましたか？

USER: はい

素晴らしいですね！`/start-3-2-1` を実行して続けてください。

---

## Claude への重要な注意事項

### ファイルパス
- `style-library.html` はこのモジュールフォルダにあります：`lesson-modules/3-nano-banana/3.1-intro-to-image-gen/3.1.4-style-database/`
- `recursive-painter.jpg` もこのモジュールフォルダにあります
- `style_extract.py` と `image_gen.py` は `lesson-modules/3-nano-banana/` にあります
- 出力画像は `lesson-modules/3-nano-banana/outputs/` に保存されます
- サムネイルはこのモジュールフォルダの `thumbnails/` フォルダに保存されます

### スタイルをライブラリに追加する際
1. 現在の style-library.html を読んで styles 配列と CANONICAL_TAGS オブジェクトを確認する
2. 次の ID 番号を決定する
3. わかりやすい名前を作成する
4. CATEGORIES 配列からカテゴリを選ぶ（下記参照）
5. そのカテゴリの CANONICAL_TAGS から2-4個のタグのみを選ぶ
6. 出力画像を thumbnails/ にケバブケースのファイル名でコピーする
7. HTML ファイルの styles 配列に新しいエントリを追加する
8. サムネイルパスを新しいファイルに向ける

### カテゴリとカノニカルタグ
style-library.html には CATEGORIES と CANONICAL_TAGS オブジェクトが含まれています。必ずこれらを正確に使用してください：

**カテゴリ:** Framework, Flow, Architecture, Mockup, Persona, Marketing, Artistic

**カテゴリ別カノニカルタグ：**
- **Framework:** 2x2-matrix, pyramid, venn, canvas, concentric, triangle
- **Flow:** process, journey-map, flowchart, steps, sequence
- **Architecture:** hierarchy, hub-spoke, system-diagram, org-chart, tree
- **Mockup:** wireframe, device-frame, ui-concept, landing-page, mobile, desktop
- **Persona:** portrait, lifestyle, headshot, context, illustrated, scene
- **Marketing:** ad, social, announcement, banner, hero
- **Artistic:** flat-illustration, hand-drawn, watercolor, photography, retro, minimalist, bold-graphic, 3d-render

新しいタグやカテゴリを作らないでください。HTML ファイル内の CANONICAL_TAGS を常に参照してください。

**注意：** ユーザーは異なるカテゴリのスタイルを組み合わせることができます（例：「Artistic のレトロスタイルを Persona のシーンスタイルと組み合わせて」）。

### スタイル抽出の実行
style_extract.py の extract_style() 関数を使用してください。画像パスを受け取り、ビジュアルスタイルの詳細な自然言語の説明を返します。

### ターミナルの制限
- 画像を直接表示できません - 必ずファイルパスを提示して開いてもらいましょう
- 開放的な質問ではなくクローズドな確認質問を使用してください（「見えますか？」）
- **画像を開く：** ユーザーが画像を見つけるのに困っている場合は、`open [path]`（Mac）または `start [path]`（Windows）を使って画像を開くことを提案してください

## 成功基準

モジュールの完了条件：
- [ ] ユーザーがスタイルライブラリ HTML を開いて閲覧した
- [ ] ユーザーがライブラリの既存スタイルを使って画像を生成した
- [ ] ユーザーが方法 1（作りながら保存）で少なくとも1つのカスタムスタイルを追加した
- [ ] ユーザーが方法 2（オンラインから収集）でアイソメトリックスタイルを追加した
- [ ] ユーザーが recursive-painter.jpg でスタイル抽出の動作を確認した
- [ ] ユーザーがオリジナルと比較して再現された画像を確認した
- [ ] ユーザーに抽出されたスタイルをライブラリに追加するか提案された
- [ ] ユーザーが `/start-3-2-1` で Module 3.2 に案内された
