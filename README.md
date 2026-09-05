# homebrew-svipall

A Homebrew tap for [Svipall](https://github.com/ilien-dev/svipall): local-first web scraping and
captcha MCP server for AI agents.

```sh
brew install ilien-dev/svipall/svipall
```

macOS and Linux, Intel and Apple silicon. It installs the release build for your platform, checked
against the `sha256sums.txt` published with that release.

Then:

```sh
svipall doctor                          # what this installation can do, and how to fix what it cannot
claude mcp add svipall -- svipall-mcp   # wire it into Claude Code
```

Browser tiers need a Chromium-based browser. `svipall browser install` fetches a Chrome for Testing
of its own, about 190 MB; without one, only the plain http tier works.

## How this tap is updated

`Formula/svipall.rb` is generated, not hand-written. It is rendered from the release's own
`sha256sums.txt` by [`scripts/render-packaging.sh`](https://github.com/ilien-dev/svipall/blob/main/scripts/render-packaging.sh)
in the main repository, so no checksum is ever typed twice. The template lives at
`packaging/templates/homebrew.rb` there.

Issues and pull requests belong in [ilien-dev/svipall](https://github.com/ilien-dev/svipall), not
here.

## Licence

Svipall is AGPL-3.0-only. This tap carries only packaging metadata.
