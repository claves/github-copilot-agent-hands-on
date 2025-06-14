# レスポンシブデザイン コーディング規約

## 基本原則

1. **モバイルファースト**
    - 小さい画面サイズから設計し、より大きな画面向けに拡張する
    - メディアクエリは`min-width`を基本とする

2. **コンテナの幅指定**
    - 固定幅ではなく相対値（%、rem、vw）を使用する
    - 最大幅（max-width）を設定してデスクトップでの過度な拡大を防止する

## ブレークポイント

以下の標準ブレークポイントを使用する:

```css
/* モバイル: デフォルト (0px以上) */

/* タブレット */
@media (min-width: 768px) { }

/* デスクトップ */
@media (min-width: 1024px) { }

/* ワイドスクリーン */
@media (min-width: 1280px) { }
```

## イメージとメディア

```css
img, video {
  max-width: 100%;
  height: auto;
}
```

## フォントサイズ

- 固定値（px）ではなく相対値（rem）を使用する
- ビューポートに応じた動的フォントサイズにはclamp()を活用する
  ```css
  h1 {
     font-size: clamp(1.5rem, 5vw, 3rem);
  }
  ```

## グリッドとフレックスボックス

- 複雑なレイアウトにはCSS Gridを使用
- 一次元のレイアウトにはFlexboxを使用
- グリッドテンプレートには`fr`単位を活用する
  ```css
  .grid {
     display: grid;
     grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
     gap: 1rem;
  }
  ```

## テスト

- 開発中は常に異なるビューポートサイズでテスト
- Chrome DevToolsのレスポンシブモードを活用
- 実機テストも必ず実施する