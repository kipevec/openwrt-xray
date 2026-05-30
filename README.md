# Xray for OpenWrt

APK package of Xray-core for Xiaomi AX3000T (mediatek/filogic), without cgo or any init scripts.

For geoip.dat & geosite.dat try

* [opkg install xray-geodata](https://github.com/openwrt/packages/tree/master/net/xray-core)
* [Loyalsoldier/v2ray-rules-dat](https://github.com/Loyalsoldier/v2ray-rules-dat)
* [yichya/openwrt-xray-geodata-cut](https://github.com/yichya/openwrt-xray-geodata-cut)

For LuCI support try [yichya/luci-app-xray](https://github.com/yichya/luci-app-xray)

## Build APK for Xiaomi AX3000T (mediatek/filogic)

GitHub Actions workflow: `.github/workflows/build-openwrt-apk.yml`

### Release a new Xray-core version

1. Get the source tarball hash:

   ```bash
   wget -qO- "https://codeload.github.com/XTLS/Xray-core/tar.gz/v<VERSION>" | sha256sum
   ```

2. Update `PKG_VERSION` and `PKG_HASH` in `Makefile`.
3. Commit and push a tag:

   ```bash
   git add Makefile
   git commit -m "tag v<VERSION>"
   git tag v<VERSION>
   git push origin master v<VERSION>
   ```

The workflow triggers on any tag push, builds the `.apk`, and publishes it to a GitHub Release.

### Manual run

Open **Actions** tab and run `Build Xray APK for OpenWrt (AX3000T)` via `workflow_dispatch`.
