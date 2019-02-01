# hidemaru_freetext
![hidemaru_freetext_image](https://user-images.githubusercontent.com/23325839/51909987-4314ee80-2411-11e9-92d1-f04477adb509.jpg)

ホワイトボードのような自由を、テキストエディタで。

## これは何？
「書きたい位置に文章を書く」を実現する秀丸エディタ用プラグイン。

- 中身は強調定義ファイル一つ
  - **フリーカーソルモード** を使用
  - 加えてホワイトボードみたいな見た目を実現するための設定をいくつか

### 開発動機
- アナログは使いやすいけど文字書くのがだるい（遅いし汚い）
- デジタルは書くのは速いけど自由に書きづらい

↓ いいとこどりできないか？

**使い慣れたテキストエディタ上で、自由な位置に文字を書く** というアプローチはどうだろう？

↓ 愛用の秀丸エディタで試す

フリーカーソルモードのおかげで案外いけるかも……というわけで hidemaru_freetext と題して整備していく。

## インストール

### 要件
- Windows 7+
- 秀丸エディタ V8.58+

### インストール手順
本リポジトリのファイル一式を適当に入手した後、

- (1) ファイル別タイプの設定に .free ファイルを追加
- (2) つくったファイル別タイプ設定上で free.hilight を読み込む
  - その際カラー、強調表示、複数行、ツリー、#ifdef **すべてを「オン」にする**
- (3) 反映されていない一部設定を手動で反映する。以下参照
  - 体裁 > 折り返しを「最大」に
  - 体裁 > 詳細 > **フリーカーソルモードを ON に(一番の肝！)**
  - 体裁 > インデント > 自動インデントを ON に
  - デザインのうち、以下を OFF にする
    - 改行文字
    - タブ文字
    - 全角空白
    - 半角空白
    - ルーラー
    - 行番号
    - ……
    - **要するに白紙表示を阻む余分な表示は全部カットする**
- (4) **IMEのスペース入力を「常に半角」にする**
  - hidemaru_freetext では「空白 = 半角スペース」を前提として各種設定が組んであるため

### インストール手順（任意）
以下は、やっておくと便利ですが必須ではありません。

- .free ファイルをダブルクリックで開けるよう、秀丸エディタに関連付けておく
- [macrosフォルダ](macros) 内のマクロを導入する
- ファイルタイプ別の設定 > フォント > ＭＳゴシックなど **等角フォント** を選ぶ
  - 等角でないと全角文字で線を引く場合などに表示がズレます

## 使い方

### 基本的なフロー
.free ファイルを新規作成した後、

- (1) たくさん改行して縦領域を確保する
- (2) カーソルキーなりマウスクリックなりで書きたい位置にアクセス
- (3) テキストを書く

### 強調表示
- `：全角コロン：`
- `；全角セミコロン；`
- `・ポチ・`
- `「かぎかっこ」`
- `＜大なり小なり＞`

### その他覚えておくと捗る操作
- Ctrl + マウスで範囲選択
  - **矩形範囲選択** になる
  - 選択範囲の塊をコピペで動かす、選択範囲の空白を消すなど

## FAQ

### Q. 挙動がよくわかりません or 馴染めません
Ans. 慣れてください

### Q. 表示色が気に食わないのでカスタマイズしたいです
Ans. ファイル別タイプの設定を適当にいじってください

### Q. 線で囲んだり矢印描いたりはできませんか？
Ans. できません

あるいは Ascii Art で頑張ってください。

このあたりは課題なので今後考えていきます（テキストでは限界があるので無理な気がしないでもないですが）。

以下は試しに本件の検討を .free ファイルでやってみたもの。

![use_free_file_example](https://user-images.githubusercontent.com/23325839/51909991-46a87580-2411-11e9-9657-174630526660.jpg)

## License
[MIT License](LICENSE)

## Author
[stakiran](https://github.com/stakiran)
