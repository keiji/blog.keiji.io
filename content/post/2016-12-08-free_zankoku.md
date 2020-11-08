---
title: 'TLDR: 「フリーランス残酷物語 Advent Calendar」 8日目'
author: Keiji Ariyama
type: post
date: 2016-12-07T15:00:15+00:00
url: /2016/12/free_zankoku.html
categories:
  - イベント
  - 雑記

---
　この記事は「[フリーランス残酷物語 Advent Calendar 2016][1]」 8日目の記事です。

「フリーランス（以下略）」と言うことで、**法人に所属している筆者は対象ではないよ**と言う向きもあるかと思いますが、どうかご安心ください。
  
　僕の所属している会社「[有限会社シーリス][2]」は今年で設立12年になりますが社員は僕一人だけ。営業、開発、その他事務仕事をすべて一人で担当している状態は、実質フリーランスと言ってもいいでしょう。

　もちろん、厳密に言えば法人格があるから契約の主体とか、有限責任だとかいろいろありますが、ようするに、なんとなくこの話題で記事が書きたくなったので、適当な理由を付けて参加していると思っていただいて大丈夫です。

　さて、8日目の今日は<del datetime="2016-12-07T15:29:19+00:00">（と言っても実質最後の記事だと思いますが）</del>、僕のこれまでの経験を振り返りながら、なんとなくの教訓みたいなものを書いていこうかと思います。

* * *

<!--more-->

## 人日5,000円

　仕事を始めたすぐ後のことです。なにもかもが手探りの中はじめて取った仕事は、とある会社のオフィスのPCのメンテナンスでした。
  
いわゆる「何もしてないのに動かなくなった」と言うやつですね。

　メンテナンスにそれほど時間がかかりませんでした。しかし最後にウイルスチェックをかけたところ、大量のウイルスが検出され、データの退避やら調査で１日を費やしました。

　作業を終えた僕に、お客様が訪ねます。
  
『いくら払えばいいですか』
  
　そこで僕は考え込んでしまいました。1日の作業で幾らもらうのが適切なのか。皆目わからなかったのです。かといってお客様に聞くのもおかしな話です。
  
　僕は、おずおずと切り出しました。
  
「1万円でどうでしょう」
  
『そうですか……それでは、少し負けてもらって、5千円をお支払いすると言うことでどうにかならないでしょうか』
  
　僕は、その提案に同意しました。

### 教訓

　この話の教訓はいろいろあります。今から思えば、幾らもらうかは作業前に伝えて合意を取っておくべき。また、追加の作業が必要ならその場で金額を提示して合意をもらうべきでした。50%オフの提案を受け入れるのも、今から思えばどうかしています。
  
　その程度の常識が、当時24歳だった僕には欠けていました。

　さすがに当時の僕のような失敗をする人がいるとは思いません。
  
　なので教訓として、一番ベーシックなものを挙げるなら、

「フリーランスは、自分の価格を自分で決める」ということです。

「価格って……どんな作業をするかによって変わるでしょう？　作業の難易度によっては1日でできるかもしれませんし、1ヶ月かけてもできないかも……」そう思ったあなた。それでも基準となる価格を決めてください。
  
「いくら払えばいいですか」「あなたに一ヶ月働いてもらうと、いくらかかりますか？」
  
　この質問に答えられるようにしておくのは非常に重要です。

## 現場に入ったらバージョン管理がCVSだった件

　僕は現在「持ち帰りの仕事のみ承る」と言う原則でお仕事をさせてもらっていますが、これは、最初の頃に入った常駐の仕事に非常にあまり良くない思い出があるからです。

　見出しで完全にネタバレしていますが、現場で作業に入った直後、バージョン管理システムがCVSであることを聞かされました。当時はまだGitではなくSubversionが主流でしたが、少なくともCVSという選択肢はありえないんだぜ。と言う風潮だったので、大変ショックを受けたことを覚えています。

　作業自体はPHPで開発された既存システムのデザイン調整と機能追加というものでしたが、既存のシステムにあるクラスからを継承することは禁止されていて、一つのクラスの実装を変えるときは、継承関係にあるすべてのクラスファイルをコピーして、まったく新しいパッケージを作るようにとの指示でした。既存クラスを拡張してシンプルに処理をまとめたものをcommitしておいたら、次の日にrevertされていたということもありましたが、このあたりは掘り下げても特に楽しい話題ではないのでこれくらいにしておきましょう。

### 教訓

　この話の教訓は、仕事を受ける前に価格等の条件面だけでなく、共に働くチームがどんなものか、きちんと自分の目で確認するべきだったということでしょう。

　こうしたミスマッチは往々にして起こり得るものです。
  
　自分とチーム、どちらが上ということではありません。採用しているツール、ライブラリ、フレームワーク、設計手法やコーディングルールがマッチせず、その溝を埋めることもできず、双方に大きなストレスがかかる可能性は常にあります。

　フリーランスというと「選んでもらう立場」と言うイメージがつきまといますが、実際にはフリーランス側にも選ぶ権利があります。

  * コード管理システムはなにを使っているか。 
      * ブランチを切る基準やmasterへマージする条件
  * Issue Trackerはなにを使っているか。
  * CIは導入しているか。
  * どんな開発者がチームに在籍しているか【超重要】

　自分が一緒に仕事できる環境かを事前に確認しておくことは、お金の話と同じくらいに大事なことだと思います。

## 同業者から怒られた話

### 「有山さんのところの価格は安すぎます」

　そんなお叱りを受けたのは、日本でAndroidがようやく普及する兆しを見せ始めた頃のことでした。
  
　大きな会社からぽつぽつとAndroidアプリ関係の案件の引き合いがありました。当時、大きな会社とうち（シーリス）のような小さな会社では直接取引は難しく、他の会社に間に立ってもらっていたのですが、そこの社長さんの一言でした。

「その価格でできると思うのでそう書いたのですが……」
  
　確かに、仕事を取りたいばかりに「少し安いかな」と思う価格をだしているきらいはありましたが、安くて叱られるのは予想外です。
  
　まったく理解できないでいる僕に、その社長さんが続けました。

「有山さんはAndroidアプリをずっとやってきてノウハウもありますし知名度もあります。そのあなたがこの価格を出したとなれば、あなたよりノウハウのない人は、知名度のない人はあなた以上の価格を付けられなくなるではありませんか。なにより、その分野で頑張っている人が真っ当な報酬を得ていないとすれば、誰があとに続こうと思いますか？」

　今から思えば、当時だしていた価格は「それだけの時間がかかる（であろうと思った）という価格」に「遠慮の0.8」を掛けた価格で、手戻りや仕様追加が発生したときのリスクを全く含めていない、とんでもない見積もりでした。

　開発案件が当初の予定内に収まらなくなったとき、大きな会社になると再見積をして追加の費用を交渉するには時間がかかります。
  
　そういった諸々の事情があった上での苦言だったのでしょう。

### 「有山さんのところの価格は高すぎます」

　そんなお叱りを受けたのは2013年のことです。
  
　僕にそう言った社長さんとは、それまで開発以外の小さな仕事を一緒にしたことはありましたが、アプリ開発の仕事は初めてでした。

「うちは人月x0万円でやっています」

　社長さんが告げた価格は、僕の標準価格のだいたい半分程度です。これにはさすがに驚きました。

「そんなことでは、社員にちゃんとした給料が支払えないのでは？」
  
「大丈夫です。ちゃんとx0数万は支払っています」

　その金額は、第一線のエンジニアの給与としては不十分だと僕は思いました。しかし「うちのあたりは物価が安いからこれで十分」と言うことでした。
  
　また、僕に「安すぎる」と言った社長さんのような「市場の価格を気にして本来価格より高くつけること」は、お客さんのためにならないのでしないと言いました。

### まとめ

　二つの話は真っ向から対立しています。

「安すぎる」と言った社長さんは、ともすれば市場を統制しているようにも見えます。
  
　しかし、他の会社に仕事を振るときにも、きちんとした額を渡していて、自社の利益のみを優先しているということはないと感じています。

　一方、「高すぎる」といった社長さんは、安い価格でとてもクオリティの高い開発をします。「安かろう悪かろう」は、その会社には当てはまらないと僕は思います。
  
　だからこそ、それがお客様の「標準」になると、他のプレイヤーが辛くなる（それが実感できた）のですが。

　僕自身、どちらが絶対的に正しいという結論は出ていません。
  
　結論は出ていないのですが、現状は「お金をきちんともらって、いい仕事をできるように頑張る」方針で仕事をするように心がけています。

## 契約を解除するとき

　フリーランスにとって、いや、社会人にとって契約は絶対です。
  
　特に請負契約では滅多なことでは契約解除をすることはできません。「契約＝仕事＝お金」なので、お客様から受け取った契約書は黙って押印するものというイメージを持ってしまう人も居るかもしれませんが、実際にはきちんと確認して、変更を希望するところを伝えることをおすすめします。

　僕がお付き合いさせていただいているお客様で、契約書の条件や文言の変更のお願いしたときに「それなら契約はしません」と返答されたお客様はいません。必ず「それは難しいのですが、こういう文言（条件）ではどうでしょう」という代替案を提示してくれます。

　繰り返しになりますが、契約は絶対です。
  
　特に請負契約は、滅多なことでは契約解除をすることはできません。

　しかし、それでも僕は、その契約を解除したことがあります。

　１つは、前述したチームとマッチしなかった案件です。
  
　作業内容に不明点がありプロジェクトマネージャー（PM）に質問するのですが「○○さんが知っているから聞いて」と言うばかりで、その人が出社していなかったり、聞いても「知らない」と言われたりということが何日か続きました。

　ある日、その日もほとんど作業は進まず、約束していた就業時間が過ぎたので帰ろうとしたところ、PMから呼び止められ「あなたは作業が進んでいないのになぜ帰るのか。残って作業してほしい」と言われたため、その場で「契約を解除する」と告げて帰宅しました。

　かなり乱暴な方法だったと思いますが、自分以外の理由で作業が進まないという理不尽と、それを責められるストレスは相当なものでしたから、個人的にはこの決断は正しかったと思います。

　もちろん、この契約解除で僕は多くの信頼を失ったのでしょう。しかし、それを嘆くより「次は今回よりうまくやろう」と研鑽して、また信頼を積み重ねていく方が前向きだと考えています。

　追い詰められて、命を失っては元も子もありませんから。

　もう１つの事例はもう少し最近、話はもっと単純です。開発するソフトウェアが明白に違法であることが判明したときです。このときは公序良俗に反する内容と言うことで契約を無効にしました。

　厳密に言うと「無効」は「解除」とは違うのですが……そういうことができるのだと頭の片隅にでも置いておいてください。

* * *

# おわりに

『フリーランスには、いつでも好きなところでのたれ死ぬ権利がある』

　会社を作ったすぐ後に、ライターの方から聞いた言葉が、フリーランスという立場を端的に表していると思います。

フリーランスになる。ならない。
  
自分の人月単価をいくらにするか。
  
目の前の仕事を請ける、請けない。

　決めるのは全部自分なのです。

　このエントリには、主に僕がこれまでしてきた失敗が詰まっています。
  
　もちろんこれが全部ではありません。ここに書いていない失敗もたくさんあります。

　僕は、これまでの失敗は、すべて自分が原因で起きたと考えています。

　契約をしてひどい目に遭ったとすれば、その契約をすると決めた自分が原因なのです。
  
　不愉快な目に遭わされたのであれば、悪いのは不愉快な目に遭わせた会社や誰かではなく、そこに飛び込んでしまった自分の判断がまずかったと思うしかないのです。
  
（もし本当の理不尽に遭遇したら、そのときは法律を頼りましょう。あれは少しでも勉強しておくと、いざという時、最強の盾と矛になってくれる可能性があります）

　手痛い失敗をしたとしても、振り返って反省して、次につなげていきましょう。

* * *

「[フリーランス残酷物語Advent Calendar 2016][1]」。明日9日の担当はu_akihiroさんです。
  
　u_akihiroさん。よろしくお願いします。

[Reinforce-Lab.&#8217;s Blog &#8211; フリーランスあれこれ][3]

 [1]: http://qiita.com/advent-calendar/2016/free_zankoku
 [2]: https://www.c-lis.co.jp
 [3]: https://blog.reinforce-lab.com/2016/12/09/freelance-sowhat/index.html