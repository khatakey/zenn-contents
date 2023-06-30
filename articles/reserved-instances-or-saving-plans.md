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

リザーブドインスタンス（以下**RI**）とは**インスタンスタイプ**と**1年または3年**の決められた期間を**リザーブ**（予約）する代わりにオンデマンド料金と比べて**最大72%の割引**されるというオプションです。
EC2だけではなく、RDSやRedshift、DynamoDBなどさまざまなサービスに対応しています。

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
