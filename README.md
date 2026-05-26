# ubuntu-i386-kernel-base

Ubuntu i386 kernel base — restores i386 kernel support across Ubuntu Resolute (26.04 LTS), Stonking (26.10), and Devel (rolling).

## Branch Structure

| Branch | Release | Version | Role | Content |
|--------|---------|---------|------|---------|
| `ubuntu/resolute` | Resolute | 26.04 LTS | stable | depth=1 from kernel.ubuntu.com |
| `ubuntu/stonking` | Stonking | 26.10 | development | scaffold (upstream not yet seeded) |
| `ubuntu/devel` | Devel | rolling | unstable | scaffold (Launchpad auth required) |

## Upstream Sources

| Release | URL |
|---------|-----|
| resolute | https://kernel.ubuntu.com/git/ubuntu/ubuntu-resolute.git |
| stonking | https://kernel.ubuntu.com/git/ubuntu/ubuntu-stonking.git |
| devel | https://kernel.ubuntu.com/git/ubuntu/ubuntu-devel.git |

## Deepening History

Branches were initially fetched at `--depth=1`. To deepen a branch for active development:

```bash
git fetch --deepen=100 origin ubuntu/resolute
# or fully unshallow (warning: ~5GB):
git fetch --unshallow origin ubuntu/resolute
```

## See Also

- [debian-i386-kernel-base](https://github.com/Interested-Deving-1896/debian-i386-kernel-base) — Debian kernel base
- [devuan-i386-kernel-base](https://github.com/Interested-Deving-1896/devuan-i386-kernel-base) — Devuan kernel overlay
- [i386-deb-linux-kernel-base](https://github.com/Interested-Deving-1896/i386-deb-linux-kernel-base) — patchset orchestration (XanMod/Liquorix/Liqxanmod)
