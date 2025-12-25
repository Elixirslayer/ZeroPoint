# ZeroPoint Overlay

This is my personal Gentoo overlay.  
It contains random stuff I either maintain, patch, or don’t want to wait for in ::gentoo.

---

## Usage

### Add the overlay

```sh
sudo mkdir -p /etc/portage/repos.conf

sudo tee /etc/portage/repos.conf/ZeroPoint.conf <<'EOF'
[ZeroPoint]
location = /var/db/repos/ZeroPoint
masters = gentoo
auto-sync = yes
volatile = false
sync-type = git
sync-uri = https://gitlab.com/Elixirslayer/zeropoint.git
EOF
```

### Sync metadata

```sh
sudo emerge --sync ZeroPoint
```
