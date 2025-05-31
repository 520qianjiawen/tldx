# tldx

`tldx` is a fast, developer-first CLI tool for **researching available domains** across multiple TLDs with intelligent permutations.

Use it to quickly explore domain name ideas for your next product, startup, or side project — without waiting or guessing.

---

## ⚡ Features

- 🔍 Smart keyword-based domain permutations (prefixes, suffixes, TLDs)
- 🚀 Fast and concurrent WHOIS availability checks
- 📤 Streams results as they're found
- 📏 Optional filtering by domain length
- 🧠 Great for technical founders, indie hackers, and naming brainstorms

---

## 🛠️ Usage

```bash
tldx [keywords] [flags]

Flags:
  -h, --help                    help for tldx
  -m, --max-domain-length int   Maximum length of domain name (default 64)
      --only-available          Show only available domains
  -p, --prefixes strings        Prefixes to add (e.g. get,my,use)
  -s, --suffixes strings        Suffixes to add (e.g. ify,ly)
  -t, --tlds strings            TLDs to check (e.g. com,io,dev)
  -v, --verbose                 Show verbose output
```

## 🔗 Examples

### Checking Domain Availability

#### `tldx google` 
```bash
❌ google.com is not available
```

#### `tldx google youtube reddit`
 
```bash
❌ google.com is not available
```

#### `tldx google youtube reddit`
```bash
  ❌ reddit.com is not available
  ❌ google.com is not available
  ❌ youtube.com is not available
```

### Permutations

#### `tldx google --prefixes get,my --suffixes ly,hub --tlds com,io,ai`

This permutates the keywords with the specified prefixes, suffixes, and TLDs, checking for availability:
```bash
  ✔️  mygooglely.com is available
  ✔️  getgooglely.ai is available
  ✔️  getgooglehub.io is available
  ✔️  mygooglehub.io is available
  ❌ mygoogle.ai is not available
```

### Show Only Available Domains

#### `tldx google reddit facebook -p get,my -s ly,hub -t com,io,ai --only-available`

```bash
  ✔️  getgooglely.ai is available
  ✔️  getgooglehub.ai is available
  ✔️  mygooglely.io is available
  ✔️  getreddithub.com is available
  ✔️  getreddit.ai is available
  ✔️  googlely.ai is available
  ✔️  getredditly.com is available
  ✔️  getreddithub.io is available
  ✔️  getredditly.io is available
  ✔️  getredditly.ai is available
  ✔️  myredditly.io is available
  ✔️  myreddithub.io is available
  ✔️  myreddithub.com is available
  ✔️  getfacebookhub.com is available
  ✔️  myfacebookly.com is available
  ✔️  myfacebookhub.ai is available
  ✔️  getfacebookly.ai is available
  ✔️  facebookly.io is available
```


