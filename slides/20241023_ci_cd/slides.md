---
theme: default
background: layouts/images/sky.jpeg
title: GitHub Actionsについて
author: kanorix
class: text-center
drawings:
  persist: false
transition: fade-out
mdc: true
overviewSnapshots: true
fonts:
  sans: M PLUS Rounded 1c
  serif: BIZ UDPMincho
  mono: M PLUS 1 Code
hideInToc: true
---

# CI/CDについて

2024/10/23

---
hideInToc: true
layout: image-left
image: layouts/images/sky.jpeg
---

# 目次

<Toc />

---

<style>
p {
   opacity: 1 !important
}
h2 {
   --uno: 'text-blue';
}
strong {
   --uno: 'text-red text-2xl';
   line-height: 1.5;
}
blockquote {
   p {
      --uno: 'text-size-2xl';
      line-height: 2rem;
   }
   strong {
      --uno: 'text-red text-3xl';
      line-height: 2;
   }
}
</style>

# 目的

- CI/CDに興味を持ってもらう
   - CI/CDなんとなく理解した！
   - なんかすごそう！
   - ちょっと触ってみようかな？

---
layout: center
hideInToc: true
---

# 自動化で「楽」しようぜ！！

---

# CI/CD ？

## 継続的インテグレーション（CI）

**ソースコードに変更をするたび**に自動でソフトウェアのビルドとテストを行う<br>
**ソフトウェア開発の手法**のこと


```mermaid
stateDiagram
  direction LR
  s1 : コミット
  s2 : ビルド
  s3 : テスト
  [*] --> s1
  s1 --> s2
  s2 --> s3
```

<div class="m-6" />

## 継続デリバリー（CD）

アプリケーションを**いつでもデプロイできる状態にする**こと<br>
（デプロイは通常、手動で行う必要がある）

```mermaid
stateDiagram
  direction LR
  s1 : コミット
  s2 : ビルド
  s3 : テスト
  s4 : リリース可能！
  [*] --> s1
  s1 --> s2
  s2 --> s3
  s3 --> s4
```

---
hideInToc: true
---

## 継続デプロイメント (CD)

ソースコードのビルドからテスト、デプロイメントまでを**すべて自動**で行う

```mermaid
stateDiagram
  direction LR
  s1 : コミット
  s2 : ビルド
  s3 : テスト
  s4 : リリース可能！
  s5 : デプロイ
  [*] --> s1
  s1 --> s2
  s2 --> s3
  s3 --> s4
  s4 --> s5
```

<img src="http://cloudbees.techmatrix.jp/wp-content/uploads/2021/09/cb_jenkins_img7_850.png" width="600px" />
https://cloudbees.techmatrix.jp/devops/cd/

---
hideInToc: true
---

# CIの目的

[AWS | 継続的インテグレーションとは?](https://aws.amazon.com/jp/devops/continuous-integration/)

- バグを早期に発見して対処すること
- ソフトウェアの品質を高めること
- ソフトウェアの更新を検証してリリースするためにかかる時間を短縮すること

<div class="m-8" />

簡単にいうと

> 変更するたびに**自動でビルドとテスト**を行い、<br>
> **品質の高いソフトウェア**を担保する！

<style>
a {
  opacity: 0.5;
}
</style>

---
layout: center
---

じゃあどうやって実現するの？

<style>
p {
  --uno: 'text-3xl';
}
</style>
---
layout: two-cols-header
---

# CI/CDのツール

::left::

- コード管理サービスが提供するサービス
   - GitHub Actions
   - GitLab CI/CD
   - Bitbucket Pipelines

- CI/CDのサービス(ソフトウェア)
   - Circle CI
   - Travis CI
   - Jenkins

::right::

<div class="grid grid-cols-2 h-100 grid-items-center">

<img src="./assets/image-gha.png" width="200px" />
<img src="./assets/image-circleci.png" width="200px" />
<img src="./assets/image-gitlabci.png" width="200px" />
<img src="./assets/image-travisci.png" width="200px" />
<img src="./assets/image-bitbucket.png" width="200px" />
<img src="./assets/image-jenkins.png" width="200px" />

</div>

---
layout: image
image: layouts/images/sky.jpeg
---

# まとめ

- 継続的インテグレーション（CI）
   - **変更のたび**に自動でビルドとテストを行う手法
- 継続デリバリー（CD）
   - アプリケーションを<br>**いつでもデプロイできる**状態にすること
- CI/CDを整備することで、コードが変更するたびに<br>**自動でビルドとテスト**を行い、<br>**品質の高いソフトウェア**を担保する！

---

# 次回(予定)

- GitHub Actionsについて
  - 実際にどうやって定義するのか


<!-- ---
layout: quote

# GitHub Actionsとは

> GitHub Actions は、 <br>
> ビルド、テスト、デプロイのパイプラインを<br>
> 自動化できる<br>
> **継続的インテグレーション** と **継続的デリバリー**  (CI/CD) <br>
> のプラットフォームです。

[GitHub Docs | GitHub Actions を理解する](https://docs.github.com/ja/actions/about-github-actions/understanding-github-actions) -->
