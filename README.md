```
░        ░░        ░░   ░░░  ░░  ░░░░  ░░░      ░░░       ░░░░      ░░░  ░░░░░░░░        ░
▒▒▒▒  ▒▒▒▒▒▒▒▒  ▒▒▒▒▒    ▒▒  ▒▒▒  ▒▒  ▒▒▒  ▒▒▒▒  ▒▒  ▒▒▒▒  ▒▒  ▒▒▒▒▒▒▒▒  ▒▒▒▒▒▒▒▒▒▒▒  ▒▒▒▒
▓▓▓▓  ▓▓▓▓▓▓▓▓  ▓▓▓▓▓  ▓  ▓  ▓▓▓▓    ▓▓▓▓  ▓▓▓▓▓▓▓▓       ▓▓▓▓      ▓▓▓  ▓▓▓▓▓▓▓▓▓▓▓  ▓▓▓▓
████  ████████  █████  ██    █████  █████  ████  ██  ███  █████████  ██  ███████████  ████
████  █████        ██  ███   █████  ██████      ███  ████  ███      ███        █████  ████
                                                                                          
```

## Tinycrslt - RSS Feed Aggregator

**no javascript. no database. just static html.**

### how

```bash
npm i -g tinycrslt
tinycrslt add https://blog.example.com/feed.xml
tinycrslt build
```

generates `index.html` with all feeds merged

### features

- 50+ feeds supported
- auto-dedup articles
- theme: brutalist (only theme)
- updates via cron

### host anywhere

```bash
tinycrslt build --output ./public
rsync -avz ./public/ server:/var/www/
```

works on github pages, netlify, or apache from 2003

### config

`feeds.txt`:

```
https://news.ycombinator.com/rss
https://lobste.rs/rss
https://reddit.com/r/programming/.rss
```

### why

because google reader died and feedly wants $8/month

powered by **rssfetch** parser ([rssfetch.run](https://rssfetch.run))

MIT • made by someone who misses 2010
