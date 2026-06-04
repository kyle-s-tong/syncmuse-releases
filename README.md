# SyncMuse

Point it at the folder where all your bounces live and it untangles them — sorting years of scattered exports back into songs, and each song's versions in order.

It works from your bounced audio, not your project files, so it doesn't care which program you made the music in — and it still works on old songs whose original sessions are long gone.

- **Stays on your computer.** It reads your files. It doesn't upload anything, anywhere.
- **Doesn't touch your files.** It only looks. It never moves, renames, or changes anything.
- **No account, no signup.** Download it, open it, point it at a folder.
- **Free.** Paid features may come later, but nothing's locked away today.

> Heads up: this is early. It will get some groupings wrong. That's exactly the feedback I need right now — if it muddles something, please tell me.

---

## Download

→ **[Get the latest version](https://github.com/kyle-s-tong/syncmuse-releases/releases/download/v0.1.2/SyncMuse-0.1.7-universal.dmg)**

Download the file, open it, and drag SyncMuse into your Applications folder. That's it.

### What you need

- A Mac running macOS 11 (Big Sur) or newer
- Works on both newer (Apple Silicon) and older (Intel) Macs <!-- Pick ONE: "Works on both newer (Apple Silicon) and older (Intel) Macs" OR "Works on newer Macs (Apple Silicon — M1, M2, M3, M4)" based on `lipo -info bin/` result -->

A Windows version is on the way, but I don't have a date yet.

---

## Is it safe to open?

Totally fair to ask. Here's the short answer and then the proof:

**Short answer:** Yes. It's signed by Apple under my real name, so your Mac will recognise it as legitimate. You won't have to do any "right-click to open" workarounds.

**Your files stay yours.** SyncMuse only reads them — it never uploads, moves, renames, or edits anything on your computer.

For the more cautious — and anyone who wants to verify it themselves — there's a [Technical details](#technical-details) section further down with checksums, virus scan reports, and how to verify the download yourself.

### Why is it on GitHub if it's a product?

SyncMuse is a real product I'm building, so the code isn't public. GitHub is just where the installer lives and where the app checks for updates — same way apps like Obsidian do it. Think of this page as a download page, not an open-source project.

---

## What it actually does

1. **You pick a folder** — wherever all your bounces and exports have piled up over the years.
2. **It sorts them out** — grouping them into songs, and each song's versions into the right order, by looking at the file names and how long the audio is.
3. **You browse the result** — finally able to find that one version from two years ago without digging.

Nothing leaves your computer. Nothing on disk changes.

---

## Does it send any data back to me?

**No, unless you choose to turn it on.** It's off by default.

If you do turn it on, it sends me things like _"someone grouped 40 versions today"_ — counts and rough categories. It never sends your file names, your folder paths, or your audio. Your unreleased song titles stay on your computer either way.

---

## Technical details

For the more technically inclined — everything you'd want to verify before running a signed binary from the internet.

### Code signing

Signed and notarized by Apple under my certificate. Gatekeeper will verify the signature on first launch; no override required.

### How the grouping works

SyncMuse reads audio bounces (not DAW project files), which is why it's DAW-agnostic and works on archived sessions. Grouping uses fuzzy matching across filenames combined with audio duration and other factors to cluster exports into projects → tracks → versions.

### Telemetry, in detail

Disabled by default. When enabled, the app emits aggregated event counts and coarse categorical metadata only. It never transmits file paths, filenames, audio content, or project names.

### System requirements

- macOS 11 (Big Sur) or later
- Apple Silicon and Intel <!-- or "Apple Silicon only" depending on the build -->

### Updates

The app checks this GitHub repository for new releases and prompts you when one is available. This repo is a release host only — the application source is not public.

---

## Changelog

### v`<VERSION>` — `<DATE>`

- v0.1.0 - 2026-06-02: Initial public release.
