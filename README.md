# Custom Domain Setup

## 1. Fork this repository

1. Open this repository on GitHub.
2. Click **Fork**.
3. Create a fork under your own GitHub account.

## 2. Edit `domain.json`

Open `domain.json` in your fork and replace the example values with your own.

```json
{
  "domain": "this-is-a.great-site.net",
  "subdomain": "example",
  "cname1": "example.github.io",
  "cname2": "blank"
}
```

### Configuration options

| Option | Description |
|---|---|
| `domain` | Your domain name |
| `subdomain` | The subdomain you want to use |
| `cname1` | Your first CNAME record |
| `cname2` | Your second CNAME record (optional) |

**CNAME rules:**
- You can have up to **2 CNAME records**.
- You must provide at least 1 CNAME.
- Only CNAME records are supported.
- If you only need one CNAME, leave `cname2` as `"blank"`.
- Do not add A, AAAA, TXT or other DNS record types.

## 3. Save your changes

1. Click **Commit changes**.
2. Your configuration will be saved to your fork.
3. Make sure your domain's DNS settings point to the appropriate CNAME destination.

## Example: One CNAME

```json
{
  "domain": "mywebsite.com",
  "subdomain": "blog",
  "cname1": "example.github.io",
  "cname2": "blank"
}
```

## Example: Two CNAMEs

```json
{
  "domain": "mywebsite.com",
  "subdomain": "blog",
  "cname1": "example.github.io",
  "cname2": "another-example.github.io"
}
```

**Important:** Keep the JSON formatting exactly as shown. All values must be inside double quotes, and each property must be separated by a comma.
