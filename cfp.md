---
layout: page
title: Call for Presentations
permalink: /cfp/
---

# 発表募集

東京Ruby会議11で発表して下さる方を募集いたします。

**まだしてません。このページの確認中です。**

## 応募要綱

* 発表について
  * Ruby に何か絡んでいる内容でお願いします。詳細は [About](../about/) のページをご覧下さい。
  * プレゼンテーションは、質疑応答込みで 30 分を予定しています。
  * ご発表は日本語か英語で行なって下さい
  * スポンサーと人が集まれば録画・配信を行ないたいと思っています（集まらなければやりません）。あらかじめご了承の上ご応募下さい。
  * 発表資料は、英語、もしくは英語併記を期待します。また、発表後に資料の公開も期待します。
  * ご発表をお願いすることになった場合、発表内容について、事前インタビューをさせて頂く可能性があります（メールや skype、直接など）。ご協力をお願いいたします。インタビューした内容は、何らかの媒体で事前に発表します。
  * ご応募頂く内容は、自分が開発に携わっているものに限定させて下さい。また、「これから作る」といった内容ではなく、すでに行なった面白いハックといった内容を期待します。
* 当落について
  * 応募は 2/29 (月) まで受け付けます。事情により（つまり、うまく集まらなかったとき）、延長される可能性があります。
  * 審査（当落の判定）は「プログラム協力」の方々と実行委員会によって行なわれます。
* 連絡について
  * 3月中には当落のご連絡をお送りします。
  * 連絡はスピーカーメーリングリストを作成し、そこで行ないます。

* スケジュール（予定）
  * 2/1 (月) 発表募集開始
  * 2/29 (月) 発表募集締め切り、審査開始
  * 3/どこか 当落発表、プログラム公開
  * 4/中旬 チケット販売開始
  * 5/28 (土) 東京Ruby会議11

不明な点があれば、<tokyorubykaigi11@atdot.net> までお気軽にお寄せ下さい。

## 応募方法

[申し込みページ](...) からお申し込み下さい。

## 応募方法の解説

発表応募に必要となる内容は下記の通りです。

* 名前
* 肩書き

好きな表記をどうぞ。

* 題目
* 概要

発表のタイトルと紹介になります。よくあるやつですね。
前述のとおり、開発に関わっているソフトウェアについてのご発表となるようにお願いいたします。

* 前提知識

この発表を聞くために必要な前提知識です。聞く人にとって便利かと思うので、概要等とともに公開したいと考えています。

* 連絡先メールアドレス（公開されません）

当落通知の宛先、およびスピーカーメーリングリストに追加するメールアドレスです。

* 内容の解説と技術的面白さ（公開されません）

ご応募頂く内容を、なぜこの場で発表する必要があるのか、という点をお寄せ下さい。
どう技術的に面白いか、という点をアピールして頂ければと思います。

学会のように、新規性、独自性などは問いません。

凄い新機能の提案、魔法のような実装、魂の震えるようなコーディングなどを楽しみにしています。

* るびまに記事を書いてくれますか？（公開されません）

事前・事後に記事を書いてくださる方は、「はい」を選択して下さい。
当落に影響するかもしれません。

事前に記事を公開する、というのも、予習ができて、意外といいものですよ。

## 応募例

	* 名前　　笹田耕一
	* 肩書き　Heroku, Inc.
	* 題目　　新しいインラインメソッドキャッシュの無効化によるメソッド呼び出しの高速化
	* 概要
	  Rubyはメソッド呼び出しの多い言語であるため、メソッド呼び出しの効率化は
	  Rubyインタプリタの高速化に有用だと考えられます。Ruby 2.3 ではメソッド呼
	  び出しのたびにメソッド探索（self の継承ツリーの中から、実際にどのメソッ
	  ドを呼び出すかを調べること）をしないで済むようにするために、メソッド
	  キャッシュを使っています。しかし、何らかの理由、たとえばメソッドが追加さ
	  れた場合には、メソッドキャッシュが無効化されるため、現状ではメソッド呼び
	  出しのたびにメソッドキャッシュの無効判定を行なっています。
	  本発表では、メソッドキャッシュの無効判定をしないで済む新しいアルゴリズムを提案し、
	  この手法によるメソッド呼び出しの性能向上について報告します。
	
	* 前提知識
	  Rubyのメソッド呼び出し規則がわかっていれば、後はなんとなくわかると思います。
	  より詳細に理解したい場合は、現状の CRuby/MRI の実装がわかっていると良いと思います。
	  ざっと抑えるなら、「Rubyのしくみ　Ruby Under a Microscope」がよいと思います。
	  1.8 までのメソッドキャッシュは RHG、1.9 の時代のインラインメソッドキャッシュについては、
	  http://www.atdot.net/yarv/imc.pdf を参考にして下さい。
	
	* 内容の解説と技術的面白さ（公開されません）
	  本発表は、新しいインタプリタ実装技術の提案になります。
	  現在、メソッドキャッシュの無効判定は、おおざっぱにいって、
	  メソッドをキャッシュしたタイミングでの、そのクラスのシリアル番号を覚えておき、
	  再度参照時に、そのシリアル番号と一致しているか、ということで判定します。
	  （再定義などがあると、影響を受ける範囲のクラスのシリアル番号がインクリメントされます）
	  擬似コードで書くと（imc がインラインメソッドキャッシュ）、

	    if (imc->class_serial != (RCLASS_SERIAL(CLASS_OF(self)) 再検索(imc);
	    (*imc->call)(...); /* メソッド呼び出し */

	  こんな感じです。
	  これを、
	
	    (*imc->call)(...); /* メソッド呼び出し */
	
	  だけにする、というのが本発表での提案のキモです。
	  このためには、次の2つのテクニックが必要になります。
	  
	  (1) 再検索が必要な状態では、imc->call に、再検索＋呼び出し、を行なう関数ポインタを設定
	  (2) 無効化するとき、対象となる imc に再検索を設定
	  
	  これを丁寧に行なうことで、いくらかの性能改善を見込んでいます。
	  具体的には、シリアル番号を取得する箇所でキャッシュミスが起こる可能性が不要になります。
	  
	  「キャッシュを使うからにはキャッシュの有効・無効を毎回見なければならない」
	  というところを覆しているのが、本提案の面白いところです。
	  また、メソッド呼び出しという、誰でも知っている機能の実装を紹介する、というのが、
	  おもしろがる人が増えるんじゃないかと思います。
	
	  「別にメソッド呼び出しそんなに遅くないよね？」
	  「メソッド呼び出しのオーバヘッドってそこじゃないよね」
	  という突っ込みには、その通りです、という感じです。
	
	* るびまに記事を書いてくれますか？（公開されません）　はい

笹田の持ちネタで書いているので、Ruby インタプリタ改善の例になっていますが、勿論そんな必要はありません。