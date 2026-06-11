---
title: "Software Design 6月号に寄稿しました"
author: sivchari
date: 2026-06-10
tags: ["go", "mutation-testing", "software-design"]
categories: ["writing"]
draft: false
---

[Software Design 2026 年 6 月号](https://gihyo.jp/magazine/SD/archive/2026/202606)の第 2 特集「AI が書いたコード、どうテストする？」に「Mutation Testing で見抜く、AI テストコードの落とし穴」という記事を寄稿しました。

## 寄稿のきっかけ

もともと Mutation Testing と、その Go 実装として自分が開発した [gomu](https://github.com/sivchari/gomu) については、[Go Conference mini in Sendai 2026](/ja/logs/sendai-go-2026/) でも発表していました。発表後に声をかけていただいたことが寄稿のきっかけです。

登壇資料で伝えられることと、雑誌の記事で伝えられることはかなり異なります。スライドは「その場で聞いている人に伝わる」ことが大前提であるのに対し、記事は「文章だけで一人で読んでも理解できる」必要があります。コードの背景や理由を省略せず書き下ろす作業は、登壇準備とはまた違う種類の大変さがありました。

## 自分の文章が雑誌に載るということ

Software Design は学生の頃から手に取ってきた雑誌です。自分が読んでいたページに、今度は自分の名前が載るというのは、少し不思議な気持ちになります。

書いてみて、技術を文章で正確に伝えるのは思ったより難しいと感じました。やってよかったです。

## 記事の内容について

記事では、AI がコードとテストを書く時代において、カバレッジだけではテストの品質を担保できないという問題を出発点に、Mutation Testing という手法と gomu の仕組み、そして CI への組み込み方を解説しています。

詳しい内容は誌面でご確認いただければ幸いです。

## おわりに

Software Design 編集部の皆様、ありがとうございました。読んでいただけたら嬉しいです。
