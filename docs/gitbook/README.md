---
description: Flagger is an Istio progressive delivery Kubernetes operator
---

# Introduction

[Flagger](https://github.com/stefanprodan/flagger) is a **Kubernetes** operator that automates the promotion of canary deployments using **Istio** routing for traffic shifting and **Prometheus** metrics for canary analysis.

Flagger implements a control loop that gradually shifts traffic to the canary while measuring key performance indicators like HTTP requests success rate, requests average duration and pods health. Based on the **KPIs** analysis a canary is promoted or aborted and the analysis result is published to **Slack**.

![Flagger overview diagram](https://raw.githubusercontent.com/stefanprodan/flagger/master/docs/diagrams/flagger-canary-overview.png)

Flagger can be configured with Kubernetes custom resources \(canaries.flagger.app kind\) and is compatible with any CI/CD solutions made for Kubernetes. Since Flagger is declarative and reacts to Kubernetes events, it can be used in **GitOps** pipelines together with Weave Flux or JenkinsX.

This project is sponsored by [Weaveworks](https://www.weave.works/)

