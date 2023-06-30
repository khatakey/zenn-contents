---
title: "リザーブドインスタンスとSavings Plansの違い"
emoji: "☪️"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["aws"]
published: false
---

EC2の購入オプションを見ているとリザーブドインスタンスとSavings Plansは非常に似ていて違いがわかりにくいと感じました。
それぞれの特徴や使い分けについて調べたので紹介します。


# リザーブドインスタンス
まず「リザーブド**インスタンス**」と聞くとEC2インスタンスと同様に、
リザーブドインスタンスが起動したり、停止できるものなのかなと考えてしまいがちですが、
実際には**インスタンスタイプ**と**1年または3年**の決められた期間を**リザーブ**（予約）する代わりに従量課金のオンデマンド料金と比べて**最大72%の割引**されるという請求割引自体のことをリザーブドインスタンス（以下 **RI**）と言います。

RIは特定のインスタンスには紐づけるという形ではなく、RIを購入後、そのRIの適用対象となるオンデマンドインスタンスが稼働していれば**AWSが自動的に割引を適用する**形になっています。

たとえば期間が1年分の、インスタンスタイプがt2.microのRIを購入した場合（実際には他にもテナンシーなどの条件を設定する必要有り）、その期間中はRIの適用対象となるt2.microオンデマンドインスタンスを使用するたびに割引が適用されます。

EC2だけではなく、RDSやRedshift、ElastiCache、OpenSearch、DynamoDBのサービスに対応しています。

RIには3つのタイプがあります。

- **スタンダードRI**
- **コンバーティブルRI**
- **スケジュールされたRI**

（本記事ではスケジュールされたRIについての詳しい説明は省略）
### スタンダードRI
**スタンダードRI**は特定のインスタンスファミリーを選択することによって割引されます。

### コンバーティブルRI
**コンバーティブルRI**はインスタンスタイプなどを変更できます。

![](/images/reserved-instances-or-saving-plans/Capture-2023-06-30-185230.png)
引用　https://aws.amazon.com/jp/ec2/pricing/reserved-instances/
# Savings Plans

Savings PlansとはRIと同じ割引率（最大72%の割引）であるにもかかわらずより**柔軟性**のあるプランになっています。


Savings Plansにも2つのタイプがあります。
- EC2 Instance Savings Plans
- Compute Savings Plans

###　EC2 Instance Savings Plans
EC2 Instance Savings PlansはスタンダードRIと同様に

###　Compute Savings Plans
