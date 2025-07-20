# Build OpenWrt images

> [!WARNING]
> This project will only build OpenWrt snapshot.

Currently supported devices:

* **friendly NanoPi R5C**

  included packages:
    ```
    zoneinfo-asia btop curl procps-ng-ps tcpdump vim-fuller openssh-sftp-server luci-i18n-base-zh-cn luci-i18n-firewall-zh-cn dae-geosite dae-geoip dae mihomo luci-i18n-cloudflared-zh-cn luci-i18n-package-manager-zh-cn
    ```

  user scripts:
    ```
    uci -q batch << EOF
    set dhcp.@dnsmasq[0].rebind_protection="0"
    commit dhcp
    EOF
    ```
