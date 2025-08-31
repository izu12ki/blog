---
title: テックブログを始めてみようかな
published: 2025-08-31
description: ''
image: ''
tags: [自己紹介]
category: '雑談'
draft: false
lang: 'ja'
---

こんにちは、Izukiです。Webエンジニアをしています。主にTypeScriptとSvelteをよく触っています。

このブログは [Fuwari](https://github.com/saicaca/fuwari)というAstro製のブログテンプレートを使っています。

早速ですがテックブログらしく、Fuwariの特徴や使い方を自分の備忘録を込めて紹介します。

## コード表示機能

- **シンタックスハイライト**: [Shiki により 100以上の言語に対応している。](https://expressive-code.com/key-features/syntax-highlighting/)

  ```js
  console.log('This code is syntax highlighted!')
  ```

- **ファイル名表示**: コードブロックにファイル名やタイトルを表示

  ```html
  <!-- src/content/index.html -->
  <div>File name comment example</div>
  ```

- **diff表示**

  ```diff lang="js"
  <!-- src/content/index.js -->
    function thisIsJavaScript() {
      // This entire block gets highlighted as JavaScript,
      // and we can still add diff markers to it!
  -   console.log('Old code to be removed')
  +   console.log('New and shiny code!')
    }
  ```

## Markdown拡張機能

- **GitHub リポジトリカード**: リポジトリ情報を動的表示

::github{repo="izu12ki/blog"}

- **注意書きボックス**: 装飾されたメッセージボックス

:::note
Highlights information that users should take into account, even when skimming.
:::

:::tip
Optional information to help a user be more successful.
:::

:::important
Crucial information necessary for users to succeed.
:::

:::warning
Critical content demanding immediate user attention due to potential risks.
:::

:::caution
Negative potential consequences of an action.
:::

## 記事の執筆・管理

### フロントマター（Front-matter）について

各記事の先頭にYAML形式でメタデータを記述します：

```yaml
---
title: My First Blog Post
published: 2023-09-09
description: This is the first post of my new Astro blog.
image: ./cover.jpg
tags: [Foo, Bar]
category: Front-end
draft: false
---
```

各項目の説明：

| 項目 | 説明 |
|------|------|
| `title` | 記事のタイトル |
| `published` | 公開日 |
| `description` | 記事の短い説明（インデックスページに表示） |
| `image` | カバー画像のパス（3つの書式に対応）|
| `tags` | 記事のタグ（配列形式） |
| `category` | 記事のカテゴリ |
| `draft` | ドラフト状態（`true`にすると非公開） |

画像パスの書式：

- `http://`や`https://`で始まる：ウェブ画像
- `/`で始まる：`public`ディレクトリの画像
- どちらでもない：Markdownファイルからの相対パス

### ファイルの配置方法

記事ファイルは `src/content/posts/` ディレクトリに配置します。サブディレクトリを作成して記事と画像をまとめて管理することも可能：

```text
src/content/posts/
├── post-1.md
└── post-2/
    ├── cover.png
    └── index.md
```

## サイト機能

- **タグ・カテゴリ分類**: 記事を整理してアーカイブから検索
- **RSSフィード**: 外部配信対応
- **レスポンシブデザイン**: サイドバー、プロフィール、ダーク/ライト切替
- **多言語対応**: `lang` フィールドで記事ごとの言語設定

更新は肩の力を抜いて、気づいたことを週に一度くらいのペースで投稿していく予定です。読みたいテーマや試してほしいことがあれば教えてください。よろしくお願いします。
