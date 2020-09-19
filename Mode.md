## VPN Mode

![VPN Mode](https://i.loli.net/2020/09/14/65JhPEfnBeZvrsK.jpg)

For a deeper understanding of the DNS handling, see: 
[漫谈各种黑科技式 DNS 技术在代理环境中的应用](https://medium.com/@TachyonDevel/%E6%BC%AB%E8%B0%88%E5%90%84%E7%A7%8D%E9%BB%91%E7%A7%91%E6%8A%80%E5%BC%8F-dns-%E6%8A%80%E6%9C%AF%E5%9C%A8%E4%BB%A3%E7%90%86%E7%8E%AF%E5%A2%83%E4%B8%AD%E7%9A%84%E5%BA%94%E7%94%A8-62c50e58cbd0)

## Proxy only Mode

![Proxy only Mode](https://i.loli.net/2020/09/14/BWdXMU8GTrmwSiK.jpg)

### Compare to VPN mode

:heavy_check_mark: One less DNS, might be faster  
:heavy_check_mark: Less processing means less battery usage, less memory usage  
:heavy_check_mark: Other apps can take system VPN  
:red_circle: Need manual configuration

### How to configure Proxy only Mode?

* Socks proxy **127.0.0.1:10808**  
Some apps support socks proxy, for example [Firefox Nightly](https://play.google.com/store/apps/details?id=org.mozilla.fenix).
You can follow this [guide](https://mullvad.net/en/help/socks5-proxy/#get-started) to enable proxy for it.

* HTTP proxy **127.0.0.1:10809**  
A system wide HTTP proxy can be configured in [WIFI settings](https://www.howtogeek.com/295048/how-to-configure-a-proxy-server-on-android/). 
It will work for most apps like Chrome or Youtube. Proxy setting needs be to turned off when v2rayNG is not running.

* More complex usage  
Some other tools can become system VPN and route traffic to v2rayNG, like
[Adguard](https://kb.adguard.com/en/android/solving-problems/adguard-outbound-proxy)

* Where is Tproxy/Transproxy mode?  
On the rooted device some tools can be used to edit iptables, you can try Proxy only mode with custom config like 
[this](https://guide.v2fly.org/app/tproxy.html). Though it is not tested.
