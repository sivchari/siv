---
title: "I received the Kubernetes Contributor Award 2025"
author: sivchari
date: 2026-06-01
tags: ["kubernetes", "cncf", "oss", "cluster-api"]
categories: ["oss"]
draft: false
---

At [KubeCon + CloudNativeCon North America 2025](https://events.linuxfoundation.org/kubecon-cloudnativecon-north-america/), I received the [Kubernetes Contributor Award 2025](https://www.kubernetes.dev/community/awards/2025/) from SIG Cluster Lifecycle. The citation read: "being always available to help and for the impact he made in the Cluster API project." I was genuinely happy, but it was also a good moment to look back on what I have actually done. So I want to write down the work that led to this award and what I learned along the way.

![The Kubernetes Contributor Award 2025 being presented at the Maintainer Summit, with "Takuma Shibuya / SIG Cluster Lifecycle" and the citation shown on screen](/images/logs/kubernetes-contributor-award-2025.jpg)

## The Work Behind the Award

What I have worked on in SIG Cluster Lifecycle falls into two main areas.

### Kube API Linter

The first is [Kube API Linter (KAL)](https://github.com/kubernetes-sigs/kube-api-linter). KAL is a linter that checks and enforces Kubernetes API rules -- the [API conventions](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md) and rules beyond them.

My first involvement was [PR #41](https://github.com/kubernetes-sigs/kube-api-linter/pull/41), which added the `nomaps` linter in early 2025. From there I kept adding linters such as `duplicatemarkers`, `ssatags`, and `defaults`, and eventually I was added as a reviewer and then an [approver](https://github.com/kubernetes-sigs/kube-api-linter/pull/190).

KAL is used not only as a standalone tool but also by large projects like Cluster API to keep their APIs consistent. Getting to work both on writing the linter and on rolling it out to a real project was good for me.

### The v1beta2 Migration of CAPD

The second is the v1beta2 migration of CAPD (Cluster API Provider Docker) in [Cluster API](https://github.com/kubernetes-sigs/cluster-api). It was a particularly significant task for me.

Migrating an API version is not finished once you define the new types. It started with [adding the v1beta2 types](https://github.com/kubernetes-sigs/cluster-api/pull/12226), and continued through promoting conditions, implementing the v1beta2 contract, gradually decoupling the v1beta1 status in the controllers, migrating the E2E tests, aligning the conversion with the other providers, and even updating the samples in the Cluster API book -- a steady accumulation of more than a dozen PRs. Being able to take part in such a valuable opportunity -- the API version migration of Cluster API as a whole -- gave me a real sense of accomplishment.

## A Distant Dream, and Continuity

When I was a student, being a Kubernetes maintainer was a vague aspiration for me -- and at the same time it felt like something very far away.

Now that I have actually made it this far, what I realize is that what closed that distance was not talent or some single big hit, but simply "staying in the batter's box." My very first PR to Cluster API, back in March 2024, was something tiny -- [just a small replacement to use the `ptr` package](https://github.com/kubernetes-sigs/cluster-api/pull/10276). Keep shipping, even small things; get reviews; ship again. Don't leave right away -- keep going. Before I knew it, those PRs had stacked up, and I was able to raise my own hand for big tasks like the CAPD migration.

What truly matters in open source, I think, is how long you can keep stepping up to the plate without walking away too soon. The size of any single contribution is not the point. There is value in continuity itself. The words "always available to help" are, in the end, simply someone having watched that accumulation of persistence.

## Gratitude

This award is, without a doubt, thanks to the maintainers and reviewers I have worked alongside.

On Cluster API, Fabrizio Pandini and Stefan Büringer reviewed a ton of my work, starting with the CAPD migration. They talked through design with me again and again, and I learned a lot from them.

On Kube API Linter, Joel Speed taught me a lot about how to think about API design.

## Looking Ahead

I am simply happy to have received this award. I just want to keep contributing as I always have.
