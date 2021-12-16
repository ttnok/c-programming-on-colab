# c-programming-on-colab
Google Colaboratory を利用して C 言語入門のための環境づくり

## Google Colaboratory 上でプログラミング入門を行う利点

- 👍 実行結果が残せる
- 👍 作業の流れが分かりやすい（はず）
- 👍 環境構築不要
- 👍 BYOD でも第 1 回目の授業からプログラミングが始められる
- 👍 提出用 PDF の作成がブラウザから行える
- 👍 Windows 上でよく起こる文字コードの問題が（おそらく）起こらない
- 👍 インデントの練習もしやすい。 `clang-format` や `astyle` を利用すれば模範例がすぐに確認できる。しかも並置される。
- 👍 Scratch などで作成したアプリを埋め込んで、動作イメージを説明することができる。
- 👍 プレゼンテーションファイルや画像を埋め込めるので、画面切り替えをせずにその場で説明可能
- 👍　自作 Web アプリを埋め込んで説明に使える。
- 👍 クリッカーを埋め込んで、リアルタイムに学生の進行状況を把握できる。（ただし、仕組みは自作する必要あり。）
- iPad などタブレット上で演習をすることも可能ではある（推奨はしない）。

## 欠点と思われる事項

- ローカル環境での作業イメージを持たせるために別に時間をとる必要がある。
    - これは Colab の左ペーンにあるファイラー内のソースファイルをダブルクリックして、Colab 内のエディタタブで編集を行うことにより、ほぼローカルでの手順をイメージさせることができそうである。
- コードセルの冒頭にマジックコマンドが入るので、C のコードの行番号が 1 つずれ、エラーメッセージの行番号と食い違いが起こる。
    - これはノートブック拡張で解決できないのだろうか
    - インストール作業などが必要だと授業利用での困難度が上がってしまうので、このずれに慣れてもらうべく周知させるのが現実的か

## Tips

1. 配布は Google Drive 経由、あるいは GitHub 経由が便利。開いたあとは「ドライブにコピーを保存」させる。
2. clang のエラーメッセージなどがずれることがある。これはブラウザの固定幅フォントを適切に設定すればよい。
    * Myrica M、Cica、Ricty などがプログラミング用としてよさそう。
2. グラフィックス描画は、各種マジックコマンドを利用するとよい。%%html や %%svg など。
3. ローカルで簡易 Web サーバを立ち上げて、websocket や SSE(Server-Sent Events) を利用して、html canvas などに表示させることもできる（はず）。libcurl などを利用する。


## 外部アプリ埋め込みの例

- Scratch
    - https://scratch.mit.edu/
    - アルゴリズムの説明などに利用
    - 課題で作成すべきプログラムの動作イメージの説明に利用 
    - ノートブックの例：https://github.com/ttnok/c-programming-on-colab/blob/main/3%E6%95%B0%E3%81%AE%E6%9C%80%E5%A4%A7%E5%80%A4.ipynb
- micro:bit（MakeCode）
    - https://makecode.microbit.org/ 
- Python Tutor
    - https://pythontutor.com/ 
    - 各種言語を行ごとに実行し、変数内容などを随時表示するサービス 
    - Python だけでなく、Java、C、C++、JavaScript、Ruby も対応
- Desmos
    - https://www.desmos.com/
    - 数学的な内容の説明に利用（例：ニュートン法など） 
- Google Slides などの Web 上のスライドサービス
- Microsoft Stream、YouTube などの動画サービス
