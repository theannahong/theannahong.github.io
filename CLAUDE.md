# CLAUDE.md — handoff notes

Read this first. It explains what this repo does so a new session can pick up without re-discovering it.

## What this repo is

A GitHub Pages site at **https://theannahong.github.io** that does one job: it **hosts the images used in Anna Hong's personal email signature and Google Workspace branding**. Nothing else. There is no website, no build step and no Jekyll (`.nojekyll` turns Jekyll off, so files are served exactly as committed).

## Files and their live URLs

| File | Live URL | Used for |
|---|---|---|
| `email/theannahong-photo@2x.png` | https://theannahong.github.io/email/theannahong-photo@2x.png | Headshot in the email signature |
| `email/theannahong-mark-email@2x.png` | https://theannahong.github.io/email/theannahong-mark-email@2x.png | Brand mark in the email signature |
| `brand/theannahong-workspace-logo_320x132.png` | https://theannahong.github.io/brand/theannahong-workspace-logo_320x132.png | Google Workspace header logo (320×132) |

`@2x` files are exported at double resolution so they look sharp on retina screens. The signature HTML shows them at half size.

## Rules for changing anything

1. **Never rename or move an existing image.** Signatures in emails that were already sent point at these exact URLs, and moving a file breaks every one of them. To update an image, **overwrite the file in place under the same name**. To add a variant, add a **new** file next to it.
2. **Keep it static.** Only plain image files (PNG, or SVG if needed). No scripts, no tracking.
3. **Keep files small.** Under ~100 KB each so signatures load fast in mail clients.
4. After pushing to `main`, GitHub Pages usually updates within a few minutes. Some mail clients (Gmail especially) cache images, so a replaced image can take a while to show up in old emails.

## Branches

- `main` is what GitHub Pages serves.
- `claude/*` branches are working branches from Claude sessions. Merge them into `main` through a pull request.

## Migration status (Nov 2026)

The migration is complete. All three images are committed on `main`, and the README describes the site's purpose. Nothing is outstanding.
