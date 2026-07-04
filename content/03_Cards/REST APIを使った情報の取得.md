---
tags:
  - seed
draft: false
---
#### REST APIとは？
- Webシステムを外部から利用できる
- URLとしてHTTPS経由で情報を渡すと、jsonやhtml形式で応答が返ってくる

（参考ページ）
[REST API の基本と実装 \| Google Cloud](https://cloud.google.com/discover/what-is-rest-api?hl=ja)
[REST API（RESTful API）とは - IT用語辞典 e-Words](https://e-words.jp/w/REST_API.html)

---
#### REST APIの例
- Google Books APIs：[API の使用  \|  Google Books APIs  \|  Google for Developers](https://developers.google.com/books/docs/v1/using?hl=ja)
	- キーワードや作者、[[ISBN]]から本を検索する
	- ある本の詳細情報を取得する　など。

---
#### Annotプロジェクトへの応用
- 本の[[ISBN]]コードを読み取ると書名と作者を取得できる仕組みづくり
	- Annotプロジェクトで渡すレシートに本の情報を記載できる
- 取得した情報を含む.mdファイルを自動生成
	- 参加者の感想を本ごとにまとめて表示できる