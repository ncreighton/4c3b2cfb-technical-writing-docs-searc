# Technical Writing & Docs Search and Discovery API

> Stop wasting hours digging through scattered documentation — this API gives you instant, semantic search across all your technical writing assets, exactly when you need it.

The Technical Writing & Docs Search and Discovery API is purpose-built for technical documentation, not generic text. It understands document structure — headings, code blocks, tables, and cross-references — delivering relevant results that traditional search misses. With a simple REST interface, you can integrate powerful search into your own tools, portals, or workflows without building from scratch.

## What's Included

- Semantic search that grasps technical context (e.g., 'API authentication methods' returns relevant sections even if exact words differ)
- Structure-aware indexing: prioritizes headings, code snippets, and step-by-step instructions for precise discovery
- Tag and metadata filtering to narrow results by product, version, or audience
- RESTful API with JSON responses — easy integration into any platform or custom dashboard
- Auto-sync with your documentation repository via webhook or scheduled updates

## Who Is This For

- Technical writers who need to embed search into internal documentation portals or wikis
- Documentation managers overseeing large sets of versioned product docs
- API developers building developer hubs or knowledge bases for their SaaS products
- Content strategists who want to analyze which docs are most searched or underused

## How It Works

Sign up and get your unique API key. Point the API to your documentation repository (Markdown, HTML, or plain text). Then send a GET request with a search query — the API returns ranked results with metadata like section titles, page URLs, and relevance scores. Integrate it into your frontend with a few lines of code.

## Frequently Asked Questions

**What documentation formats does the API support?**
It supports Markdown, HTML, and plain text files. For structured formats like DITA or AsciiDoc, we provide a conversion guide.

**Can I limit searches to specific product versions?**
Yes. You can tag documents by version or product name, then filter searches using those tags in the API request.

**Is the search real-time?**
Search queries are processed in real-time against the indexed content. New documents can be indexed on-demand via API or automatically via webhooks.

**How is pricing structured beyond the initial $32.49?**
The $32.49 covers up to 10,000 search requests per month and 500 indexed documents. Higher tiers are available for larger volumes.

**Do I need to expose my documentation publicly to use this API?**
No. The API can search private repositories. You control access via your API key; no public exposure required.

## What You Get

- Instant digital download
- Complete REST API with full documentation
- Free updates for life — pay once, own forever
- Setup guide and usage instructions

**Unlock the full discoverability of your technical writing — buy the API now and start searching smarter.**

## Features

- Full REST API

## Quick Start

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Configure environment
cp .env.example .env
# Edit .env with your settings

# 3. Run locally
uvicorn main:app --reload --port 8000

# 4. View interactive docs
open http://localhost:8000/docs
```

## Docker Deployment

```bash
# Build and run
docker compose up -d

# Check health
curl http://localhost:8000/health
```

## Authentication

Get a token first:
```bash
curl -X POST "http://localhost:8000/auth/token?username=admin&password=admin123"
```

Use the token in subsequent requests:
```bash
curl -H "Authorization: Bearer YOUR_TOKEN" http://localhost:8000/items
```

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/health` | System health |
| POST | `/auth/token` | Get JWT token |
| GET | `/items` | List all items |
| POST | `/items` | Create item |
| GET | `/items/{id}` | Get item |
| PATCH | `/items/{id}` | Update item |
| DELETE | `/items/{id}` | Delete item |
| GET | `/stats` | API statistics |

Full interactive docs: `http://localhost:8000/docs`

## Rate Limits

| Endpoint | Limit |
|----------|-------|
| `/auth/token` | 10/minute |
| `GET /items` | 60/minute |
| `POST /items` | 30/minute |
| `DELETE /items` | 20/minute |

## Running Tests

```bash
pip install pytest httpx
pytest tests/ -v
```

## Production Notes

- Change `SECRET_KEY` in `.env` before deploying
- Replace in-memory `_db` with a real database
- Add proper user management to `auth.py`
- Configure `ALLOWED_ORIGINS` for CORS
- Use Nginx/Traefik as reverse proxy

## License

MIT


---

## Free vs Pro

| Feature | Free | Pro |
|---------|:----:|:---:|
| 100 requests/day | Yes | Yes |
| Standard endpoints | Yes | Yes |
| JSON responses | Yes | Yes |
| Unlimited requests | - | Yes |
| Premium endpoints | - | Yes |
| Batch processing | - | Yes |
| Webhook notifications | - | Yes |
| SLA guarantee | - | Yes |
| Priority support | - | Yes |

### Upgrade to Pro

Get the full version with all premium features, priority support, and lifetime updates.

**[Get Pro Version](https://buy.stripe.com/5kQ5kDdPp7EocVWbzScZg3H)**

- [Buy Now (Stripe)](https://buy.stripe.com/5kQ5kDdPp7EocVWbzScZg3H)

