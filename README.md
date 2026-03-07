# ALICE-LegalTech

Legal document management, contract automation, and compliance platform

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum |

## ALICE Crate Integration

alice-legal, alice-db, alice-auth, alice-analytics

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST` | `/api/v1/compile` | 法律文書コンパイル |
| `POST` | `/api/v1/contracts` | 契約作成・実行 |
| `GET ` | `/api/v1/search` | 法令検索 |
| `GET ` | `/api/v1/compliance` | コンプライアンスチェック |
| `GET ` | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
