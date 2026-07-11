<p align="center"><img src="https://raw.githubusercontent.com/go-atproto/brand/main/social/go-atproto.png" alt="go-atproto" width="640"></p>

<h1 align="center">go-atproto</h1>
<p align="center">Pure-Go read client for Bluesky and the AT Protocol (XRPC).</p>
<p align="center"><a href="https://go-atproto.github.io/docs/"><img src="https://img.shields.io/badge/docs-mkdocs--material-0A6E96?style=flat-square&logo=materialformkdocs&logoColor=white" alt="docs"></a> <a href="https://pkg.go.dev/github.com/go-atproto/atproto"><img src="https://img.shields.io/badge/pkg.go.dev-reference-0079A8?style=flat-square&logo=go&logoColor=white" alt="pkg.go.dev"></a> <img src="https://img.shields.io/badge/Go-1.26-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go"> <img src="https://img.shields.io/badge/license-BSD--3--Clause-0A6E96?style=flat-square" alt="license"></p>

---

## What is this?

A pure-Go, dependency-free read client for **Bluesky** and the **AT Protocol**, talking to the XRPC HTTP API. It targets the public Bluesky AppView at `https://public.api.bsky.app`, which serves read methods without authentication. An optional `Login` exchanges credentials for an access token to use authenticated methods such as the home timeline.

The client lives in [`go-atproto/atproto`](https://github.com/go-atproto/atproto):

```go
c := atproto.New() // defaults to https://public.api.bsky.app

feed, err := c.AuthorFeed(context.Background(), "bsky.app", 25, "")
if err != nil {
	panic(err)
}
for _, p := range feed.Posts {
	fmt.Printf("@%s (%d likes): %s\n", p.Author.Handle, p.LikeCount, p.Text)
}
```

## Install

```sh
go get github.com/go-atproto/atproto
```

## Links

- 📖 Docs — <https://go-atproto.github.io/docs/>
- 🌐 Site — <https://go-atproto.github.io/>
- 🧩 Client — <https://github.com/go-atproto/atproto>
- 📦 API reference — <https://pkg.go.dev/github.com/go-atproto/atproto>
- 🎨 Brand assets — <https://github.com/go-atproto/brand>

---
<p align="center"><sub>Branding in <a href="https://github.com/go-atproto/brand">go-atproto/brand</a>.</sub></p>
