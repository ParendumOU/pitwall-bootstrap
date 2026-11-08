# Pitwall installer

One command that turns a Windows, Linux or macOS machine into a ready Claude Code workstation with Pitwall: several Claude subscriptions used as one (automatic account choice, failover with the same conversation, live and scheduled switches), a web dashboard, the Pitwall Remote phone app, persistent memory with a local model (Pitwall Mem), optional local compaction (Pitwall Compact) and a baseline of working rules. It can also set up a Pitwall server (for example a Raspberry Pi or an always-on laptop) that keeps the accounts of all your machines, and connect your other machines to it.

## Install

Linux, macOS or WSL:

```bash
curl -fsSL https://github.com/ParendumOU/pitwall-bootstrap/releases/latest/download/install.sh | bash
```

Windows (PowerShell, as your normal user):

```powershell
irm https://github.com/ParendumOU/pitwall-bootstrap/releases/latest/download/install.ps1 | iex
```

In a terminal it opens a full-screen installer that asks what to install and how the machine is used: on its own, as the Pitwall server, or as a client of your server. Run the same command again to update or repair, with `--check` / `-Check` to only check, and with `--uninstall` / `-Uninstall` to remove it. `--help` / `-Help` lists every option; `--version X.Y.Z` / `-Version X.Y.Z` installs that release instead of the latest.

Every download (the installer's own files, Pitwall, Pitwall Mem, Pitwall Compact, the full-screen installer) comes from these GitHub releases and is checked against the `SHA256SUMS` of its release before it is used.

## Releases

Each release has `install.sh` and `install.ps1`, the full-screen installer `pitwall-setup` for Windows, Linux and macOS (amd64 and arm64, Raspberry Pi 64-bit included), the installer's files (`pitwall-bootstrap-<version>.tar.gz`) and `SHA256SUMS`.

## More

Website: https://pitwall.parendum.com

License: MIT (see [LICENSE](LICENSE)). Each release includes its full source.
