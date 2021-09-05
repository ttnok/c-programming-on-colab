# c-programming-on-colab
Google Colaboratory を利用して C 言語入門

## Google Colaboratory 上でプログラミング入門を行う利点

- 👍 環境構築不要
- 👍 BYOD でも第 1 回目の授業からプログラミングが始められる
- 👍 提出用 PDF の作成がブラウザから行える
- 👍 実行結果が残せる
- 👍 作業の流れが分かりやすい（はず）
- 👍 文字コードの問題が（おそらく）起こらない
- 👍 インデントの練習もしやすい。 `clang-format` や `astyle` を利用すれば模範例がすぐに確認できる。しかも並置される。

## 欠点と思われる事項

- ローカル環境での作業イメージを持たせるために別に時間をとる必要がある。
- コードセルの冒頭にマジックコマンドが入るので、C のコードの行番号が 1 つずれ、エラーメッセージの行番号と食い違いが起こる。
    - これはノートブック拡張で解決できないのだろうか

## Tips

1. clang のエラーメッセージなどがずれることがある。これはブラウザの固定幅フォントを適切に設定すればよい。
    * Myrica M、Cica、Ricty などがプログラミング用としてよさそう。
2. グラフィックス描画は、各種マジックコマンドを利用するとよい。%%html や %%svg など。
3. ローカルで簡易 Web サーバを立ち上げて、websocket や SSE(Server-Sent Events) を利用して、html canvas などに表示させることもできる（はず）。libcurl などを利用する。
