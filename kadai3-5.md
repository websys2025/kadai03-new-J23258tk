## 自動販売機（データ構造と各種処理）のミニレポート
### Q5-1. 自動販売機の商品データついて説明せよ。
* データ構造（各項目とその説明）
  ・id: 商品番号。ユーザーが商品を選ぶときに使用する識別番号。
  ・name: 商品名。例：「コーラ」「お茶」など。
  ・price: 商品の価格。例：120円、150円など。
  ・stock: 商品の在庫数。購入可能かどうかに関わる。
* 連想配列の配列として定義するメリット
  ・各商品の情報（id, name, price, stock）をひとまとまりで扱える。
### Q5-2. showItemListの処理内容について説明せよ。
* 配列の繰り返し処理＝配列（商品リスト）をループで回して、各商品の情報を取り出す。
* 連想配列の参照方法＝各商品の譲歩を取り出すときは、連想配列**キー（項目名）**を使って参照する。
### Q5-3. buyItemの処理内容について説明せよ。
* 商品購入の可否判定
  ユーザーが指定した商品番号に対応する商品を探す。
* 商品在庫を減らす処理
  購入できた場合、その商品のstockを１減らす。
* 商品番号のエラー処理
  ユーザーが入力した商品番号が存在しない場合は、エラーメッセージを表示する。
### Q5-4. プログラムの考察
* データ構造について
  ・商品ごとに連想配列を使い、配列にまとめることで、拡張性・保守性が高くなった。
  ・項目が増えても連想配列を拡張するだけで済み、プログラム全体に大きな影響がない。
* 商品一覧表示と購入処理を関数化したメリット
  ・コードの再利用性が高まった（同じ処理を何度も書く必要がない）。
  ・役割分担が明確になり、バグが起きてもどこを直せばいいのかわかりやすい。
### Q5-5. 感想
* 今回の課題で苦労したこと
 商品番号と配列にズレが起きないようにしたこと。
* 演習を通して理解できたこと
  連想配列と配列の組み合わせでデータを扱う基本パターンを理解できた。
* この自動販売機プログラムの追加機能や課題など
  お金を入れておつりを出す処理を追加したい。
