# webone-webfixes

This repository contains edited CSS, JavaScript and other files need to browse particular Web sites in old browsers through the [WebOne HTTP Proxy Server](https://github.com/atauenis/webone).

**UNDER CONSTRUCTION**

## proSilver
A skin for phpBB 3.x forums, created by SubBlue company. Since phpBB 3.2 doesn't work in IE 5.5/6.0, such forums are needs to use phpBB 3.0 version of the skin:

```
[Edit:(^http://.*/styles/prosilver/theme/)(.*)]
; downgrade stylesheets of phpBB proSilver skin to version 3.0 only on IE 3-6
OnHeader=User-Agent: .*MSIE [3456]
AddRedirect=http://atauenis.github.io/webone-webfixes/prosilver/theme/$2
```

Mozilla, Opera appears to still work with modern proSilver code. In Opera, do not check "Identify as MSIE" option.


# iesetup
Patched versions of Microsoft Internet Explorer 5.x/6.0 download site lists (ie5sites.dat, ie6sites.dat) used by installer. As of 01.2023, original lists are lost, but other setup files are still present at download.windowsupdate.com. So, a simple redirect and a updated site list is enough.

```
[Edit:^(?:http://www\.|http://)microsoft.com/windows/ie/(.*)/download/rtw/x86/ie[0-9]sites.dat]
AddRedirect=http://github.com/atauenis/webone-webfixes/raw/main/iesetup/SITES-$1.dat
```

Use original ~500KB installers of IE. :) To get them, see DAT file, corresponding to version, and append `/ie5setup.exe` to URL for your language.