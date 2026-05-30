# Xray for OpenWrt

Just the binary file for various platforms, without cgo or any init scripts.

For geoip.dat & geosite.dat try

* [opkg install xray-geodata](https://github.com/openwrt/packages/tree/master/net/xray-core)
* [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat)
* [yichya/openwrt-xray-geodata-cut](https://github.com/yichya/openwrt-xray-geodata-cut)

For LuCI support try [yichya/luci-app-xray](https://github.com/yichya/luci-app-xray)

## Build APK for Xiaomi AX3000T (mediatek/filogic)

GitHub Actions workflow:

* `.github/workflows/build-openwrt-apk.yml`

How to run:

1. Open **Actions** tab and run `Build Xray APK for OpenWrt (AX3000T)` manually (`workflow_dispatch`).
2. Download built `.apk` from workflow artifacts.
3. To auto-publish `.apk` to a GitHub Release, push a version tag (e.g. `v26.2.6`).
