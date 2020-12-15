# webone-webfixes

This repository contains edited CSS and JavaScript files need to browse particular Web sites in old browsers throught [WebOne HTTP Proxy Server](https://github.com/atauenis/webone).

**UNDER CONSTRUCTION**

## proSilver
A skin for phpBB 3.x forums, created by SubBlue company. Since phpBB 3.2 don't work in IE6. So such forums are needs such fix:
```
[Edit:(^http://.*/styles/prosilver/theme/)(.*)]
; downgrade stylesheets of phpBB proSilver skin to version 3.0 only on IE 3-6
OnHeader=User-Agent: .*MSIE [3456]
AddRedirect=http://atauenis.github.io/webone-webfixes/prosilver/theme/$2
```
