---
title: "Kubernetes Contributor Award 2025 をいただきました"
author: sivchari
date: 2026-06-01
tags: ["kubernetes", "cncf", "oss", "cluster-api"]
categories: ["oss"]
draft: false
---

[KubeCon + CloudNativeCon North America 2025](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/) にて、SIG Cluster Lifecycle から [Kubernetes Contributor Award 2025](https://www.kubernetes.dev/community/awards/2025/) をいただきました。受賞理由には「being always available to help and for the impact he made in the Cluster API project」と書いていただきました。とても嬉しい一方で、自分がこれまで何をしてきたのかを振り返る良い機会だったので、受賞につながった活動と、そこで自分が学んだことを書き残しておきます。

![Maintainer Summit での Kubernetes Contributor Award 2025 授賞の様子。スクリーンに「Takuma Shibuya / SIG Cluster Lifecycle」と受賞理由が映し出されている](/images/logs/kubernetes-contributor-award-2025.jpg)

## 受賞につながった活動

僕が SIG Cluster Lifecycle で取り組んできたことは、大きく分けて 2 つあります。

### Kube API Linter

ひとつは [Kube API Linter (KAL)](https://github.com/kubernetes-sigs/kube-api-linter) です。KAL は Kubernetes の [API 規約](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md) や、規約にないルールも含めて API をチェック・強制する linter です。

僕の最初の関わりは、2025 年の初めに `nomaps` linter を追加した [PR #41](https://github.com/kubernetes-sigs/kube-api-linter/pull/41) でした。そこから `duplicatemarkers`、`ssatags`、`defaults` といった linter を継続的に追加し、やがて reviewer に、そして [approver](https://github.com/kubernetes-sigs/kube-api-linter/pull/190) に加えていただきました。

KAL は単体で使うだけでなく、Cluster API のような大きなプロジェクトに導入して API の一貫性を保つのにも使われます。linter を書く側と、それを実際に導入する側の両方を経験できたのは良かったです。

### CAPD の v1beta2 移行

もうひとつは、[Cluster API](https://github.com/kubernetes-sigs/cluster-api) における CAPD (Cluster API Provider Docker) の v1beta2 移行です。自分にとって特に大きなタスクでした。

API バージョンの移行は、新しい types を定義して終わりではありません。[v1beta2 types の追加](https://github.com/kubernetes-sigs/cluster-api/pull/12226) から始まり、condition の promote、v1beta2 contract の実装、controller での v1beta1 status の段階的な切り離し、E2E テストの移行、他プロバイダとの conversion の整合、さらに Cluster API book のサンプル更新まで、十数本の PR にわたる地道な作業の積み重ねでした。Cluster API 全体の API バージョン移行という貴重な機会に携わることができたことは達成感がありました。

## 憧れと、継続すること

学生の頃、Kubernetes のメンテナーというのは僕にとって何となく憧れであり、同時にとても遠い存在のようにも見えていました。

でも、いざ自分がここまで辿り着いてみて思うのは、それを近づけてくれたのは才能でも大きな一発でもなく、ただ「打席に立ち続けたこと」だったということです。Cluster API に出した最初の PR は、2024 年 3 月の [`ptr` パッケージへのちょっとした置き換え](https://github.com/kubernetes-sigs/cluster-api/pull/10276) のような、本当に小さなものでした。小さくても出し続け、レビューをもらい、また出す。すぐに離れずに、続ける。気づけばそうした PR が積み上がっていて、CAPD の移行のような大きなタスクにも自分から手を挙げて取り組めるようになっていました。

OSS で本当に大事なのは、どれだけ打席に立ち続けて、すぐに離れずに継続できるかなのだと思います。そこに一回ごとの貢献の大きさは関係ありません。継続することそのものに価値がある。「always available to help」という言葉も、結局はその継続の積み重ねを見ていてくれた人がいた、ということなのだと受け止めています。

## 感謝

今回の受賞は、間違いなく一緒に活動してきたメンテナー・レビュアーのみなさんのおかげです。

Cluster API では、Fabrizio Pandini さんと Stefan Büringer さんに、CAPD の移行をはじめ何度もレビューしてもらいました。設計の議論にも付き合ってもらって、多くのことを学びました。

Kube API Linter では、Joel Speed さんに API デザインの考え方をたくさん教えてもらいました。

## これから

賞をいただけて、純粋に嬉しいです。これからも変わらず、続けていきたいと思います。
