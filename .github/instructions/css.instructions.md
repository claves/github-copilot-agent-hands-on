---
applyTo: "*/*.css"
---

# CSSコーディングルール

## 基本構造

### ファイル構成

- Reset/Normalize CSS → 基本スタイル → レイアウト → コンポーネント → ユーティリティの順で記述
- 関連するスタイルはセクションごとにコメントで区切る

### セレクタの命名規則

- BEM記法を使用（Block__Element--Modifier）
- クラス名は小文字とハイフンを使用
- IDセレクタの使用は避ける

## コーディング品質ルール

### 記述スタイル

- インデントは2スペース
- プロパティ値の後にセミコロンを必須
- プロパティ名と値の間にスペースを1つ
- 1行に1つのプロパティを記述

### プロパティの順序

1. ポジション関連（position, top, right, bottom, left, z-index）
2. ボックスモデル（display, width, height, margin, padding, border）
3. フォント・テキスト（font, line-height, text-align, color）
4. 背景・装飾（background, box-shadow, border-radius）
5. アニメーション・トランジション（transition, animation）

### パフォーマンス最適化

- 過度にネストしたセレクタを避ける（3レベル以下推奨）
- 汎用的すぎるセレクタ（*、div、spanなど）の単体使用を避ける
- !importantの使用は最小限に

### レスポンシブデザイン

- Mobile-firstアプローチを採用
- ブレークポイントは統一された値を使用
- 相対単位（rem、em、%、vw、vh）を優先

### メンテナンス性

- カラーパレットやフォントサイズは変数で管理
- 使用していないCSSは削除

### 互換性

- ベンダープレフィックスが必要なプロパティには適切に付与
- フォールバック値を設定
