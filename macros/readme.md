# hidemaru_freetext Macros
hidemaru_freetext 上でちょっと楽をするためのマクロたち。

## 共通事項
- キー割り当てで適当なキーを割り当てて使うことを想定しています
- テキトーにつくったのでバグがあるかもしれません

## (作者所感)
正直要らないと思います。

元は自分用につくったのですが、挙動がやや不安定だし、いちいちマクロを呼び出すのも面倒なので、使わなくなってしまいました。

## freetext_pullback.mac
おすすめの割り当て: Ctrl + Delete

ある位置にテキストを書くと、右側にあるテキストがズレてしまいますが、これを直す（ **書いたテキストの分だけ Delete キーを押す**）マクロです。

以下に例を示します。I はカーソル位置です。

```

   I             こんなテキストがあって

   ↓ aiueo を挿入します

   aiueoI              こんなテキストがあって

   ↓ 「こんなテキストがあって」部分が右にズレてうざいです
   ↓ これをなんとかして ← 方向にもとに戻したい
   ↓
   ↓ このマクロを発動させると、以下のようになります。

   aiueoI        こんなテキストがあって
```

内部的には、左側にある aiueo の分だけ Delete キーを押してます。

ちなみに aiueo 部分に全角文字が入っていても正しく動作すると思います。

ただし、**Delete キーを押し切った結果、右側のテキストが削れてしまう場合は何もしません。**

## freetext_add_XXXXline_to_XXXX.mac
おすすめの割り当て: Ctrl + . / \ :

`｜` や `―` といった線文字を連続で引きたい場合に使います。

以下 4 つがあります。

- freetext_add_horiline_to_left.mac
- freetext_add_horiline_to_right.mac
- freetext_add_vertline_to_down.mac
- freetext_add_vertline_to_up.mac

たとえば freetext_add_vertline_to_down.mac を例にすると、下記 I の位置からこのマクロを呼び出すだけで、どんどん下方向に `｜` を書くことができます。

```
         aaaaaaa                  
          I           aaaaaaaaaaaa
                                  
aaaaaaa               aaaaaaa     
                                  
                   aaaaaaaaa      
                                  
          aaaaaaaaa               
```

↓ freetext_add_vertline_to_down.mac を発動させていくと、

```
         aaaaaaa                  
          ｜          aaaaaaaaaaaa
          ｜                      
aaaaaaa   ｜          aaaaaaa     
          ｜                      
          ｜       aaaaaaaaa      
          ｜                      
          aaaaaaaaa               
```

上記のように上から下へと `｜` を入れていきます。
