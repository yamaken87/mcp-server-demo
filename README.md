# UUID Generator MCP Server

MCPプロトコルに準拠したUUID v4生成サーバー

## セットアップ

### 必要要件
- Node.js (v18以上)
- npm (v8以上)

### インストール手順

1. リポジトリのクローン
```bash
git clone <repository-url>
cd mcp-server-demo
```

2. 依存パッケージのインストール
```bash
npm install
```

3. ビルド
```bash
npm run build
```

## 使用方法

### サーバーの起動
```bash
node dist/index.js
```

### 開発用サーバーの起動
```bash
npm run dev
```

### 利用可能なツール

#### generate_uuid
- 説明: UUID v4を生成します
- 入力: なし
- 出力: ランダムなUUID文字列

## MCPクライアントの設定

### VSCode拡張機能の場合
1. 以下のパスの設定ファイルを開きます：
```bash
~/Library/Application Support/Code/User/globalStorage/saoudrizwan.claude-dev/settings/cline_mcp_settings.json
```

2. `mcpServers`オブジェクトに以下の設定を追加します：
```json
{
  "mcpServers": {
    "uuid-generator": {
      "command": "node",
      "args": ["プロジェクトのパス/dist/index.js"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

### Claude Desktopの場合
1. 以下のパスの設定ファイルを開きます：
```bash
~/Library/Application Support/Claude/claude_desktop_config.json
```

2. `mcpServers`オブジェクトに以下の設定を追加します：
```json
{
  "mcpServers": {
    "uuid-generator": {
      "command": "node",
      "args": ["プロジェクトのパス/dist/index.js"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

## ライセンス
MIT
