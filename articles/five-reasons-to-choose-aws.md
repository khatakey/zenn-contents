---
title: "オンプレミスよりAWSが優れている利点5つとその理由"
emoji: "📌"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [aws]
published: false
---

# はじめに
5つの点から比べていきたいと思います。
# 1. スケーラビリティ

AWSを使う上での最大の利点の1つはスケーラビリティともいえるでしょう。
スケーラビリティ（Scalability）は日本語で拡張性や拡張可能性と訳され、

アプリケーション、ストレージ、データベース、ネットワークなどのITシステムが、**負荷の増大や用途の拡大や縮小に応じてサイズやボリュームを変更しても正常に機能し続けられる能力**のことを指します。

AWSはオンプレミスと比べてより簡単にスケールを変更できます。
[Amazon EC2](https://aws.amazon.com/jp/ec2/)という仮想サーバーサービスの場合、
CPUやストレージ、メモリなどを用途に合わせて簡単に選択、変更することが可能です。

![](https://storage.googleapis.com/zenn-user-upload/f6dff48b836f-20230603.png)
この画像にあるインスタンスのタイプ以外にメモリに最適化されたインスタンスだったりストレージに最適化されたインスタンスなどがあります。
（ただしEC2のインスタンスタイプを変更する場合は1度そのインスタンスを停止してから変更手順を行うことになるのでそこは注意が必要です。）

オンプレミスのサーバーを拡大するとなれば機材調達が必要なので、かなりの時間とお金がかかります。

**よって早く簡単に拡大縮小できる点でAWSがオンプレミスより優れていると言えます。**

# 2. 費用
AWSは、費用が安く済む場合が多いです。
なぜなら、AWSは使った分だけお金を払う**従量課金制**を採用しているからです。
これには大きくメリットが2つあって、

1つ目は使った分しか課金されないのでAWSのサービスをあまり使用しないときにはその分安くなるということ。
たとえば会社などで新しいアプリケーションをローンチさせたとき、当然始めたばかりで認知度も低いため誰もサービスを使ってくれないということもあるでしょう。
その場合にAWSを採用していると少額しか請求されませんが、オンプレミスを採用している場合は初期費用の段階で今後のアプリケーションのニーズを見越して規模のサーバーを用意する必要があるのでコンピューターリソースが有り余ってしまいその分のコストもかかってしまいます。

2つ目はいつでも止めることができるということ。
もし作ったサービスの業績がうまくいかず頓挫してしまった場合を考えてみましょう。

AWSだと使用しないサービスを簡単に停止できて終了月以降は課金されなくなります。
一方オンプレミスの場合は使わなくなった場合でもサーバーの場所代や撤去代などさまざまなコストがかかってきます。


またそれ以外にも、AWSは、AWS Free TierやAWS Savings Planなど、コスト削減のためのプログラムも数多く提供しています。これらのプログラムは、コストをさらに削減するのに役立ちます。

# 3. セキュリティ

AWSには責任共有モデルというのがあります。
AWSのシステムにおいてAWS側かユーザー側どちらがどのサービス範囲においてセキュリティの責任があるかを明確にさせるというものです。
![](https://storage.googleapis.com/zenn-user-upload/e13846940f91-20230604.jpeg)
> 引用　https://aws.amazon.com/jp/compliance/shared-responsibility-model/


たとえばデータセンターで物理的な障害が発生した場合はAWSが責任を持ちます。
オンプレミスで自前のデータセンターで障害が起こった場合は、当然自社のサーバーであるので自分たちで復旧させる必要があリます。

自分たちがカスタマイズできる部分は自分たちが責任を持ち、逆にできないところは責任を持つ必要がないということです。

**責任範囲が少ないということはサッカーゴールのサイズが小さいということと同じでユーザー（ゴールキーパー）はより守りやすくなります。**


# 4.グローバル展開のしやすさ
AWSには現在31のリージョン、99のアベイラビリティゾーンがあります。（2023年6月時点）
各リージョンは、物理的に異なる地理的な場所に存在し、それぞれのアベイラビリティーゾーンは、冗長性と可用性を高めるために複数のデータセンターで構成されています。
![](https://storage.googleapis.com/zenn-user-upload/a00c19c9fd36-20230604.png)
![](https://storage.googleapis.com/zenn-user-upload/bfde57c34f2a-20230604.png)
> 引用　https://aws.amazon.com/jp/about-aws/global-infrastructure/

AWSはこれらの世界中にまたがる高速なネットワークインフラストラクチャを持っています。
ユーザーは自分の拠点に近いデータセンターを利用できるので通信速度が向上し、レイテンシが低下させることができます。

オンプレミスでグローバル展開をしていくと考えた場合、各国にデータセンターを設置する手間やコンプライアンスについて十分に調べる必要があり多くの時間と手間がかかります。
企業はこういったことよりもプロダクトの内容について時間や労力をかけるべきです。


グローバル展開を目指す企業にとってこの点はAWSを使うとても大きなメリットだといえます。


# 5.幅広いサービス
オンプレミスの場合はネットワーク機器やサーバーについてそれぞれ別の事業者から調達する必要があるのに対して、
AWSを使う場合はシステム運用に必要なサービスを**すべてAWSから借りることができます。**

AWSには現在200を超えるサービスがあり、その数もどんどん増えていっています。

時事的な話題でいうと現在、生成系AIが流行っていますがAWSにも[Amazon Bedrock](https://aws.amazon.com/jp/bedrock/)という簡単に生成系AIを利用できるサービスがあります。
他にもAWSには機械学習や自然言語処理などの技術を活用したサービスが提供されており、すぐに最先端の技術を活用できます。

急激に進化しているIT分野において、幅広いサービスを簡単に利用できるというのはとても大事になってきます。
潮流が変わったときによりピボットしやすいAWSを使うことらライバルよりも優位に立つことができるでしょう。




