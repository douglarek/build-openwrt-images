# Build immortalwrt

Currently supported devices:

* **friendly NanoPi R5C**

  included packages:
    ```
    zoneinfo-asia autocore btop curl tcpdump vim-fuller openssh-sftp-server luci luci-i18n-cpufreq-zh-cn luci-compat luci-lib-base luci-lib-ipkg luci-theme-argon luci-i18n-base-zh-cn luci-i18n-firewall-zh-cn luci-i18n-opkg-zh-cn luci-i18n-alist-zh-cn dae-geosite dae-geoip luci-i18n-cloudflared-zh-cn mihomo
    ```

  user scripts:
    ```
    uci -q batch << EOF
    set dhcp.@dnsmasq[0].rebind_protection="0"
    commit dhcp
    EOF
    ```
