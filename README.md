# ZENITH-ENGINE — YouTube Archive Node Scanner
> *"Scanning 20,000,000,000+ video nodes..."*
> 
<img width="1912" height="607" alt="image" src="https://github.com/user-attachments/assets/2c6d6714-2ac5-448e-aea6-15549401f01f" />



A browser-based tool for surfacing forgotten, unlisted, and unindexed YouTube videos by generating raw camera filename queries — the kind of titles people never change before uploading.

Built on the observation that countless personal videos were uploaded directly from phones and cameras with default filenames like `DSC_0247`, `IMG_3891`, `GOPR0012`, or `Desktop 2014 03 22` — and are effectively invisible to normal search.

---

## How It Works

Most people who upload home videos, travel clips, and personal recordings don't rename their files. YouTube indexes these anyway. By searching for the exact filename patterns cameras generate, you can find videos with zero SEO optimization — raw, unseen, and often years old.

my tool automates this process by randomly generating filename-pattern queries and firing them at YouTube search across different temporal layers.

---

## Features

### Archive Layers
| Layer | Description | Date Filter |
|---|---|---|
| **Layer I — Recent Fallen** | Videos uploaded in the last few years, already forgotten | `before:2023` |
| **Layer II — Forgotten Era** | Mid-2010s uploads, peak unoptimized uploading era | `before:2016` |
| **Layer III — Pre-Archive** | Early YouTube era, pre-smartphone dominance | `before:2010` |
| **Pseudo Random Node** | No date filter — pure random across all time | none |

### Query Pool
Generates queries based on real camera/device filename conventions:

- `IMG XXXX` / `DSC XXXX` / `DSCF XXXX` — standard camera naming
- `GOPRXXXX` / `CIMGXXXX` — GoPro and Casio formats
- `MVI XXXX` — Canon video format
- `VID YYYYMMDD` / `Desktop YYYY MM DD` — date-stamped exports
- `GH XXXXXX` — GoPro Hero format
- `clip XXXX` / `video XXXX` / `File XXXX` / `export YYYYMMDD`

### Advanced Panel
Fine-grained query control:

- **Prefix Term** — lock to a specific filename prefix from the pool
- **Suffix / Keyword** — append a tag (e.g. `birthday`, `vacation`, `vlog`) to narrow context
- **Token Format** — choose between 4-digit, 6-digit, date (`YYYYMMDD`), spaced date, or none
- **Date Filter** — set `before:`, `after:`, or a `between` range manually
- **Sort Mode** — sort by upload date, view count, rating, or relevance
- **Mutation** — randomly alters characters on each rescan for variation
- **Open ×3 At Once** — fires three unique queries simultaneously
- **Live Query Preview** — see the exact search string before firing

### Other Controls
- **Force Corruption** — visual glitch effect
- **Blackout Layer** — unlocks after 8+ scans, switches to unsorted archive access mode
- **Copy Query** — copies the current advanced query to clipboard

---

## Usage

No installation required. Just open `index.html` or use the github pages link in any modern browser.

```
1. Open terminal.html / github pages site
2. Select an archive layer
3. Click SCAN NODE
4. Browse what surfaces
```

For more targeted digs, open the **[ ADVANCED ]** panel and configure your query before firing.

---

## A Note on Exact Matching

The tool wraps queries in quotation marks to signal exact-match intent. However, **YouTube does not reliably honor quote operators** — its search engine prioritizes engagement signals over textual precision. If you're getting irrelevant results, this is a platform limitation, not a bug.

Workarounds:
- Use **Google video search** (`site:youtube.com "DSC 0247"`) — Google's index of YouTube actually respects quotes
- Add **negative keywords** in the suffix field (e.g. `-tutorial -review`)
- Use the **Upload Date** sort mode to surface recent raw uploads first

---

## Inspiration

Core concept inspired by **KVN AUST** and the broader practice of "lost media" YouTube archaeology — the idea that the platform's index contains millions of videos that exist in a kind of digital limbo, uploaded and immediately forgotten.

---

## License

Do whatever you want with it. No tracking, no backend, no dependencies — just a single HTML file.
Have fun, Explorers! :)
