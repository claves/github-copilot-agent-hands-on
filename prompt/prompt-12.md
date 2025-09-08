#　追加課題
playwright mcpを使用したフォームテスト

## .vscode/mcp.jsonに設定を追加
```
"playwright": {
      "command": "npx",
      "args": [
        "@playwright/mcp@latest"
      ]
 }
```

## サーバー起動
```
npx serve public -l 3000
```

## プロンプト
[Prompt]
- PlaywrightのMCPのNavigate to a URLを使用し、http://localhost:3000 にアクセスしフォーム入力を実施してください
