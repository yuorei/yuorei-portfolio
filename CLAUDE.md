# CLAUDE.md

このファイルは、リポジトリで作業する Claude Code (claude.ai/code) へのガイダンスを提供します。

## プロジェクト概要

yuorei のポートフォリオサイト。ストリーミング動画・バックエンド・クラウドアーキテクチャを専門とするソフトウェアエンジニアのポートフォリオ。ビルドツールなしの純粋な HTML/CSS 静的サイトで、Cloudflare Workers でデプロイされる。

## デプロイ

```bash
wrangler deploy
```

ビルドステップはない。アセットディレクトリはプロジェクトルート (`.`) なので、そのままデプロイされる。

## アーキテクチャ

サイト全体は2ファイルで構成される：

- **index.html** — シングルページポートフォリオ。セクション構成: Hero / Books (№01) / Skills (№02) / Interests (№03) / Contact (№04)
- **style.css** — 全スタイル。CSS カスタムプロパティと Grid/Flexbox レイアウトを使用

画像は `images/` に配置し、HTML から直接参照する。

## CSS デザインシステム

`:root` で定義された CSS 変数：

| 変数 | 値 | 用途 |
|------|-----|------|
| `--bg` | `#F6F2EA` | ページ背景（ベージュ） |
| `--ink` | `#14110E` | 本文テキスト（ダークブラウン） |
| `--accent` | `#FF5B1F` | アクセントカラー（オレンジ） |
| `--paper` | `#FBF8F1` | カード・パネル背景 |
| `--muted` | `#8A8378` | サブテキスト |
| `--line` | `#1C1916` | ボーダー |
| `--rule` | `#D8CFBE` | 薄い区切り線 |

レスポンシブブレークポイント: 980px / 860px / 820px / 760px / 720px / 640px / 620px。最大幅は 1280px。

Google Fonts から読み込んでいるフォント: Fraunces, Instrument Serif, Inter, JetBrains Mono, Noto Sans JP, Noto Serif JP。

## コンテンツ言語

サイトは日英バイリンガル。セクションラベルや UI 要素は英語、書籍タイトルや一部の説明文は日本語。
