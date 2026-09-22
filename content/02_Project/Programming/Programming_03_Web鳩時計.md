---
tags:
  - sprout
draft:
---
## 制作のきっかけ
---
- 時間感覚がなくなるので、1時間ごとに音が鳴るようなWebアプリが欲しい

## 欲しい機能
---
- 必須
	- [x] 一時間ごとに音が鳴る
	- [x] 音のON、OFF
	- [x] 音量調整
- あったら便利？
	- 12時間表示、24時間表示の切り替え
	- 時間帯で変わる背景
	- 音量のユーザー設定の保存

### 見た目を変える

- もっと大きな時計にしたい
- フォントを変えたい
- 秒を目立たせたい
- 背景を時間帯によって変えたい
- 鳩時計っぽい雰囲気にしたい

### 機能を足す

- [x] 00分になったら音を鳴らしたい
- [x] 30分になったら音を鳴らしたい
- 次のキリのいい時間まで何分か表示したい
- 「あと30分で○○」みたいな表示をしたい
- タイマーも同じページに置きたい

### 使いやすくする

- [x] 音のON/OFFを切り替えたい
- [x] 音量を変更したい
- [ ] 12時間表示／24時間表示を切り替えたい
- [ ] スマホでも見やすくしたい




## 制作過程
---
**2026-09-08**
- [CSSとJavaScriptでおしゃれなデジタル時計を実装する方法 \| WebDev Tech](https://web-dev.tech/front-end/javascript/digital-clock/)をコピペして、デジタル時計が完成

- [ ] Googleフォントの導入方法
- 背景色や文字色を変更
- ![[Pasted image 20260908220834.png]]
- [[JavaScript]]を読み込むタイミングに気をつけないと、使いたい要素がHTML内に存在していない場合がある
	- headの中に置きたい場合は、<script src="clock.js" defer></script>とする方法もある
- 通知音を入れるかどうか設定するボタンを追加し、30分ごとに音が鳴るようになった
	- addEventListener()を利用
		- [【JavaScript入門】addEventListener()によるイベント処理の使い方！ \| 侍エンジニアブログ](https://www.sejuku.net/blog/57625)
	- soundEnabledによる状態の管理
		- 反転させてから、if文で分岐させる
- [ ] try catchの使い方を調べる
	- [【JavaScript入門】try...catchの使い方と例外処理のまとめ！ \| 侍エンジニアブログ](https://www.sejuku.net/blog/29293)

**2026-09-12**
- 音のON・OFFを表示する位置を調整
- 音量調整スライダーを設置
	- [CSS と JavaScript で input type=range レンジスライダーをカスタマイズ](https://www.webdesignleaves.com/pr/css/input-range-style.html)
- button：inline-block
	- [HTML/CSS　block,inline,inline-block とは？ #Block - Qiita](https://qiita.com/ryoheitakahashi/items/7e4d6d8065972ac99501)
- ![[Pasted image 20260912111652.png]]
- ChatGPTにコードを添削してもらった
	- `innerHTML`と`textContent`の違い
		- **HTML構造やタグを含めて操作したいとき** ➔ `innerHTML` 
		- **純粋なテキストだけを安全に扱いたいとき** ➔ `textContent` 

**2026-09-22**
- mp3から音の生成に変更
	- 音程の試行錯誤
	- [ドレミの振動数！ピアノ88鍵全音域の周波数一覧表 \| ピアノマップ](https://inalesson.com/frequency_list/2417/)
	- 高音と低音を重ねてみたものの、音が気に入らなかったので却下
- 音量調整UIの挙動がおかしかった部分を修正
- ![[Pasted image 20260922143017.png]]

#### 第1弾完成！！
- GitHubに公開

---
[[JavaScript]]