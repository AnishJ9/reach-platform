# REACH Platform

Technology platform for REACH Partnerships Foundation - supporting medical trainees pursuing K-award career development.

## Live Sites

Once deployed to GitHub Pages:

- **REACH Exchange**: `https://[username].github.io/reach-platform/` - Fellow and Sponsor portal
- **REACH Access**: `https://[username].github.io/reach-platform/access.html` - Public wiki
- **Admin**: `https://[username].github.io/reach-platform/admin.html` - Internal management

## Files

```
reach-platform/
├── index.html          # REACH Exchange (Fellows + Sponsors)
├── admin.html          # Admin portal (hidden, not linked)
├── access.html         # REACH Access public wiki
├── data/
│   └── articles.json   # Wiki articles content
└── README.md
```

## Deployment

### GitHub Pages

1. Push this repo to GitHub
2. Go to Settings → Pages
3. Source: Deploy from branch `main` (or `master`)
4. Folder: `/ (root)`
5. Save

Site will be live at `https://[username].github.io/[repo-name]/`

### Custom Domain (Optional)

1. Add a `CNAME` file with your domain:
   ```
   exchange.reachpartnerships.org
   ```
2. Configure DNS:
   - Add CNAME record pointing to `[username].github.io`
   - Or add A records for GitHub Pages IPs

## Data Storage

**Current (Prototype):** localStorage in browser
- Data persists per-browser only
- Export/Import available in admin

**Future (Production):** Backend database
- PostgreSQL for structured data
- Firebase Auth for authentication

## Authentication

**Fellows:** Social login (Google/Microsoft) - UI ready, Firebase integration pending
**Sponsors:** No login required (public application form)
**Admin:** Password protected (separate URL)

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

## Development

These are static HTML files with vanilla JavaScript. No build step required.

To test locally:
```bash
# Python 3
python -m http.server 8000

# Then open http://localhost:8000
```

## Contact

REACH Partnerships Foundation
- Web: https://reachpartnerships.org
- Email: info@reachpartnerships.org
