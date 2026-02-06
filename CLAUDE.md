# CLAUDE.md — プロジェクトルール

## 🔒 セキュリティ（最優先・違反厳禁）

### 絶対禁止事項
- **APIキーをソースコードにハードコードしない**（`|| 'AIza...'` 等のフォールバック含む）
- **`.env` ファイルをGitにコミットしない**
- シークレット情報はすべて環境変数 (`process.env.*`) 経由で参照すること

### コミット前チェック（必須）
- `.env`, `.env.*` が `.gitignore` に含まれているか確認
- `git diff --cached` でAPIキー・シークレットが含まれていないか確認
- `!.env.example` のみ追跡許可

### .gitignore必須パターン
```
.env
.env.*
!.env.example
.claude/
.DS_Store
node_modules/
__pycache__/
```

## 📐 開発規約

### コード品質
- 関数は単一責任（1関数1目的）
- マジックナンバー禁止（定数化する）
- コメントは「なぜ」を説明（「何」はコードで表現）

### Git運用
- コミットメッセージ: `type: 簡潔な説明`（例: `fix: remove hardcoded API key`）
- type: feat / fix / docs / refactor / test / chore

### 環境変数の扱い
- 本番キーは GCP Secret Manager で管理
- ローカル開発は `.env` + `.env.example`（値なしテンプレート）で運用
- フォールバック値にAPIキーを絶対に書かない

## 📋 参照
- セキュリティ詳細: https://github.com/AXSC-Studio/CLAUDE_MASTER
- OWASP Top 10 準拠
