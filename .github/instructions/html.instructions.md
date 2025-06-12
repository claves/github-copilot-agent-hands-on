---
applyTo: "*/*.html"
---

# HTMLコーディングルール

## 基本構造

- HTML5のDoctype宣言を必ず使用する (`<!DOCTYPE html>`)
- `<html>`要素にlang属性を設定する (`<html lang="ja">`)
- `<head>`内に適切なメタタグを設定する (charset, viewport, description等)
- セマンティックなHTML要素を優先使用する (header, nav, main, section, article, aside, footer)

## アクセシビリティ

- すべての画像に適切なalt属性を設定する
- フォーム要素にはlabelを関連付ける
- 見出しタグ(h1-h6)を階層順に使用する
- キーボードナビゲーションに配慮したtabindex設定
- ARIAラベルを適切に使用する

## パフォーマンス

- 画像の最適化とWebP形式の使用を推奨
- 不要なCSSやJavaScriptの読み込みを避ける
- レスポンシブ画像の実装 (srcset, sizes属性)
- 重要でないリソースにはloading="lazy"を設定

## コード品質

- インデントは2スペースで統一
- 属性値は必ずダブルクォートで囲む
- 自己終了タグは適切に記述する
- HTMLバリデーターでの検証を必須とする
- 一貫性のあるクラス命名規則を使用 (BEM記法推奨)

## SEO対策

- title要素は各ページで固有にする
- meta descriptionを設定する
- 構造化データ(JSON-LD)の実装
- Open Graphタグの設定
- 適切なheading構造の維持
