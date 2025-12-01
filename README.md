# sing-box Patched

Auto-synced fork of [fscarmen/sing-box](https://github.com/fscarmen/sing-box) with patches applied via GitHub Actions.

## Patches Applied

1. **Shadowsocks 2022 AEAD Password** - Auto-generates correct base64 passwords for 2022 ciphers
2. **Statistics Disabled** - No data sent to remote servers
3. **Custom Script Source** - `sb` shortcut points to this repo

## Usage

```bash
# Basic install
bash <(wget -qO- https://raw.githubusercontent.com/denniszlei/sb-patched/main/sing-box.sh)

# With Shadowsocks 2022 cipher
export SHADOWSOCKS_METHOD='2022-blake3-aes-128-gcm'
bash <(wget -qO- https://raw.githubusercontent.com/denniszlei/sb-patched/main/sing-box.sh)

# Quick install (all protocols)
bash <(wget -qO- https://raw.githubusercontent.com/denniszlei/sb-patched/main/sing-box.sh) -l
```

## Supported Ciphers

| Cipher | Password Type |
|--------|---------------|
| `2022-blake3-aes-128-gcm` | 16-byte base64 key |
| `2022-blake3-aes-256-gcm` | 32-byte base64 key |
| `aes-128-gcm`, `aes-256-gcm`, etc. | UUID |

## Auto-Sync

This repo syncs with upstream daily via GitHub Actions. Patches are automatically applied to each new version.

## Credits

- Original: [fscarmen/sing-box](https://github.com/fscarmen/sing-box)
