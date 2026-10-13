# Night Shift

Things built after the day job, by [DayJob Development](https://dayjob.dev).
Live at https://nights.dayjob.dev.

The page lists every site in `registry.json`. Each site lives in its own
repository and on its own `*.dayjob.dev` subdomain. The library holds only
the listing and a thumbnail for each.

## Adding a site

The `parody-site` Claude Code skill adds entries as part of building a site.
To add one by hand:

```sh
python3 ~/Code/dotfiles/.claude/skills/parody-site/scripts/register_site.py . \
  --slug my-site --title "My Site" --url https://my-site.dayjob.dev/ \
  --repo https://github.com/mcfredrick/my-site \
  --summary "One sentence on what it is." --tags "tag one,tag two" \
  --screenshot path/to/screenshot.png
```

Then commit and push. Entries are listed newest first.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The listing page |
| `registry.json` | One entry per site: slug, title, url, repo, summary, tags, date added, thumbnail |
| `thumbs/` | 960px JPEG screenshots, one per site |
| `CNAME` | `nights.dayjob.dev` |
