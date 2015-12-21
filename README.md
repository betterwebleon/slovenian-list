# slovenian-list
Slovenian cosmetic and tracking filters for uBlock Origin and uBlock.

**Statični kozmetični filtri in filtri sledenja za uBlock Origin in uBlock. Naj bo brskanje udobno tudi pri pohajkovanju po slovenskih straneh.** :)

Slovenian List consists mostly of static cosmetic filters and few tracking filters. Among others, there are **[100 most popular Slovenian websites](http://www.moss-soz.si/si/rezultati_moss/obdobje/)** included in this list.

The list is **intended for simple users** with a set-and-forget approach. Copy the raw URL to your content-filtering software's custom filter list (see point 2.B below for more info). If you have any suggestions or issues to report, please do it [here](https://github.com/betterwebleon/slovenian-list/issues) or write an [e-mail](mailto:betterweb.leon@outlook.com).

###1. Recommended content-filtering software:
**uBlock Origin**

Why? Because it's efficient, lightweight, simple and free.

###2. Recommended complementary filter lists:
**A) following lists can be turned on by *ticking* them in uBlock Origin [in "3rd-party filters" tab]**
- uBlock filters
- uBlock filters – Badware risks
- uBlock filters – Block-then-redirect
- uBlock filters – Privacy
- uBlock filters – Unbreak
- Adblock Warning Removal List
- EasyList
- EasyPrivacy
- Fanboy's Enhanced Tracking List
- Malware domains
- Spam404

**B) various filter lists can be added by copying the following URLs to the "Custom" field in uBlock Origin ["3rd-party filters" tab]**

1. https://easylist-downloads.adblockplus.org/adwarefilters.txt
2. https://raw.githubusercontent.com/metaphoricgiraffe/behind-the-scenes-filters/master/filters.txt
3. https://raw.github.com/r4vi/block-the-eu-cookie-shit-list/master/filterlist.txt
4. https://raw.githubusercontent.com/betterwebleon/international-list/master/filters.txt
5. https://raw.github.com/liamja/Prebake/master/obtrusive.txt
6. https://raw.githubusercontent.com/metaphoricgiraffe/tracking-filters/master/trackingfilters.txt
7. https://raw.githubusercontent.com/betterwebleon/slovenian-list/master/filters.txt

(*Slovenian List is under the number 7, however it is recommended to add all of them.*)

###3. Recommended browser:
**Mozilla Firefox**

Why? Because it can be customized in order to improve browsing speed, privacy, user interface, etc.

How? Type this in your address (URL) bar: *<code>about.config</code>*

Hit enter and confirm scary Firefox warning message. Then select the following preference names (by pasting them to a search bar) and change their values to the following ones:

|   | PREFERENCE NAME                      | VALUE |
|---|:-------------------------------------|:-----:|
|1. | beacon.enabled                       | false |
|2. | browser.safebrowsing.malware.enabled | false |
|3. | geo.enabled                          | false |
|4. | layout.css.visited_links_enabled     | false |
|5. | network.http.sendRefererHeader       |   0   |
|6. | network.http.sendSecureXSiteReferrer | false |
|7. | media.peerconnection.enabled         | false |
|8. | media.peerconnection.turn.disable    |  true |
|9. | privacy.trackingprotection.enabled   |  true |

**The upper settings are privacy-related only. If you want more speed as well, keep on tweaking:**

|    | PREFERENCE NAME                           | VALUE |
|----|:------------------------------------------|:-----:|
| 10.| full-screen-api.approval-required         | false |
| 11.| full-screen-api.transition-duration.enter |       |
| 12.| full-screen-api.transition-duration.leave |       |
| 13.| memory.free_dirty_pages                   |  true |
| 14.| network.http.keep-alive.timeout           |   60  |
| 15.| network.http.pipelining                   |  true |
| 16.| network.http.pipelining.aggressive        |  true |
| 17.| network.http.pipelining.maxrequests       |   8   |
| 18.| network.http.pipelining.ssl               |  true |
| 19.| network.http.proxy.pipelining             |  true |
| 20.| network.http.request.max-start-delay      |   3   |
| 21.| network.websocket.delay-failed-reconnects | false |

\* ***Take advantage of this valuable information at your own risk - if there is any. It is possible to revert the changes anytime. Be fearless, padawan!***

###4. License:
This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org>

HAVE A NICE DAY. (*This wish is not part of a license anymore. You can however treat it as a special annex to the license.*)
