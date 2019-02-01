# 線の書き方
- 直線は下記マクロを発動することで一文字ずつ引いていく
  - ← freetext_add_horiline_to_left.mac
  - → freetext_add_horiline_to_right.mac
  - ↓ freetext_add_vertline_to_down.mac
  - ↑ freetext_add_vertline_to_up.mac
- ただし線を引く方向を切り替えるときは **手動でジョイントを追加する**
  - (1) ジョイント `＋` を手動で入力する
  - (2) カーソルを、次に直線を引きたい方向の始点に持っていく

# ジョイント追加時のカーソル位置例
例: ↓の方向に直線を引いていて、ジョイントを追加した場合。

```
     ｜
     ｜
     ｜
     ＋
```

この時、切り替える方向は ←、↓、→ の三パターンある。

各々について、カーソルをどこに移動させるべきかを `I` で示す。

← 左に切り替える場合:

```
     ｜
     ｜
     ｜
    I＋
```

↓ 下に切り替える場合:

```
     ｜
     ｜
     ｜
     ＋
    I

※フォントによってはたぶん I の位置ずれます。すいません……
```

→ 右に切り替える場合:

```
     ｜
     ｜
     ｜
     ＋I
```

# 練習問題
練習用の .free ファイルを用意していますので、遊んでみてください。

- (1) create_new_freefile.bat を実行します
- (2) YYYYMMDD_HHMMSSMM.free みたいなファイル名(現在日付時刻を並べた名前です)が生成されるので、それを秀丸エディタで開いてください
- (3) START から GOAL まで線を引いてみましょう

ちなみに回答サンプルとして sample.free を用意（試しに筆者が遊んでみたもの）してみたので、併せて見てみてください。

この練習問題をサクサク書けるようになったら、線を引く作業についてはマスターしたと言えるでしょう。