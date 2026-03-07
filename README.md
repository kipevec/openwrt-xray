# Xray for OpenWrt

Just the binary file for various platforms, without cgo or any init scripts.

For geoip.dat & geosite.dat try

* [opkg install xray-geodata](https://github.com/openwrt/packages/tree/master/net/xray-core)
* [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat)
* [yichya/openwrt-xray-geodata-cut](https://github.com/yichya/openwrt-xray-geodata-cut)

For LuCI support try [yichya/luci-app-xray](https://github.com/yichya/luci-app-xray)

## Build for Xiaomi AX3000T (mediatek/filogic, OpenWrt 25.12.0)

GitHub Actions workflow:

* `.github/workflows/build-openwrt-25.12.0-ax3000t.yml`

How to run on GitHub servers:

1. Open **Actions** tab and run `Build Xray for OpenWrt 25.12.0 (AX3000T)` manually (`workflow_dispatch`).
2. Download built `.apk` from workflow artifacts.
3. To auto-publish `.apk` to a GitHub Release, push a tag like `ax3000t-2026-03-07`.
