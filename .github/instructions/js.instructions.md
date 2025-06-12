---
applyTo: "*/*.js"
---

# JSコーディングルール

## 基本原則

- **可読性**: コードは書くよりも読むことの方が多いため、明確で理解しやすいコードを心がける
- **一貫性**: プロジェクト全体で統一されたスタイルを維持する
- **保守性**: 将来の変更や拡張を考慮したコードを書く

## コーディングスタイル

### 命名規則

- **変数・関数**: camelCase を使用 (`userName`, `calculateTotal`)
- **定数**: SCREAMING_SNAKE_CASE を使用 (`MAX_RETRY_COUNT`, `API_BASE_URL`)
- **クラス**: PascalCase を使用 (`UserManager`, `DataProcessor`)
- **ファイル名**: kebab-case を使用 (`user-service.js`, `data-utils.js`)

### 関数

- **単一責任**: 1つの関数は1つの責任のみを持つ
- **純粋関数**: 可能な限り副作用のない純粋関数を作成
- **適切な関数名**: 動詞で始まり、何をするかが明確に分かる名前を付ける
- **引数は3個以下**: 引数が多い場合はオブジェクトを使用

```javascript
// Good
function calculateUserAge(birthDate) {
  return new Date().getFullYear() - birthDate.getFullYear();
}

// Bad
function calc(d) {
  return new Date().getFullYear() - d.getFullYear();
}
```

### 変数

- **const優先**: 再代入しない場合は`const`を使用
- **let使用**: 再代入が必要な場合のみ`let`を使用
- **var禁止**: `var`の使用は避ける
- **意味のある名前**: 変数の内容が推測できる名前を付ける

### エラーハンドリング

- **try-catch**: 例外が発生する可能性のある処理は適切にハンドリング
- **Promise**: async/awaitを使用し、エラーハンドリングを忘れない
- **ログ出力**: エラー発生時は適切なログを出力

```javascript
// Good
async function fetchUserData(userId) {
  try {
    const response = await fetch(`/api/users/${userId}`);
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    return await response.json();
  } catch (error) {
    console.error('Failed to fetch user data:', error);
    throw error;
  }
}
```
