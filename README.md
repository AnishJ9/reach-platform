# REACH Platform

Technology platform for REACH Partnerships Foundation - supporting medical trainees pursuing K-award career development.

## Live Site

https://reachpartnerships.org

## Pages

| Page | File | URL |
|------|------|-----|
| Homepage | `index.html` | `reachpartnerships.org` |
| Exchange | `exchange.html` | `reachpartnerships.org/exchange.html` |
| Access Wiki | `access.html` | `reachpartnerships.org/access.html` |
| Admin | `admin.html` | `reachpartnerships.org/admin.html` |

## Files

```
reach-platform/
├── index.html          # Marketing homepage
├── exchange.html       # Fellow/Sponsor portal
├── access.html         # REACH Access public wiki
├── admin.html          # Admin portal (hidden)
├── data/
│   └── articles.json   # Wiki articles content
├── CNAME               # Custom domain config
└── README.md
```

## Adding Articles

Edit `data/articles.json`:

```json
{
  "articles": [
    {
      "id": 7,
      "status": "published",
      "category": "prevent",
      "topic": "k-award",
      "stages": ["resident", "fellow"],
      "title": "Your Article Title",
      "description": "Brief description",
      "readTime": "5 min read",
      "updated": "December 2025",
      "content": "<p>HTML content here...</p>"
    }
  ]
}
```

**Categories:** `prevent`, `identify`, `remove`
**Topics:** `k-award`, `research`, `career`, `relocation`, `funding`, `wellness`
**Stages:** `student`, `resident`, `fellow`, `early-faculty`

## Contact

REACH Partnerships Foundation
- Web: https://reachpartnerships.org
- Email: info@reachpartnerships.org
