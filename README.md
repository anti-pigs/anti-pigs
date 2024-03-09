### Censorship: because pigs love to sniff 🐽🐽

**هينزل فيديوهات قريب بتوضح ازاى تعمل كل ده بنفسك**

**methods employed by **"ماسر"** for censoring the internet**

- DPI

---

**implementation**

| implementation | Software-based solutions | Hardware-based solutions |
| ----           | -----                    |------                    |
| Advantages     | <ul><li>easier</li></ul> | <ul><li>enable whole network( smartphone, IoT devices, gaming consoles, smart TVs ) to be tunneled</li></ul> |
| Disadvantages  | <ul><li>most clients can only take over application layer traffic and lack higher system permissions</li><li>some applications(banking, games, windows apps) don't follow proxy rules so won't get bypassed</li></ul> |  <ul><li>Heavy CPU utilization</li><li>network congestion</li><li>underutilization of bandwidth</li><li>requires a dedicated Router</li><li>Costly</li></ul>  |
| usecase | <ul><li>lite users</li><li>single devices</i><li>on occassion</li></ul> | <ul><li>multiple users</li><li>labs</li><li> offices </li><li>special devices like Smart TVs</li></ul> |

---

#### working states as of march 2024

- wireguard: blocked by DPI (can be obfuscated)
- openVPN: blocked by DPI (can be obfuscated)
- haven't tested out any other commercial VPN
##### proxies
- shadowsocks: working
- trojan: working
- xray: working

---
#### what you'll need?
a VPS with minimal capabilities

- [a list of free VPS](https://github.com/cloudcommunity/Cloud-Free-Tier-Comparison)
- domain name (optional)
    - [freenom](https://www.freenom.com/en/freeandpaiddomains.html)
    - [getfreedomain](https://www.getfreedomain.name/)
- server (optional)
- client (optional)
---

#### Clients/Software

- cross paltform desktop
  - [Qv2ray](https://github.com/Qv2ray/Qv2ray)
  - [nekoray](https://github.com/MatsuriDayo/nekoray)
- Windows
  - [v2rayN](https://github.com/2dust/v2rayN)
- MacOS
  - [v2rayXS](https://github.com/tzmax/V2RayXS)
- IOS
  - [Shadowrocket](https://apps.apple.com/us/app/shadowrocket/id932747118) NOT open source
- Android
  - [v2rayNG](https://github.com/2dust/v2rayNG)
- OpenWrt
  - [v2rayA](https://github.com/v2rayA/v2rayA)

#### servers

- with a GUI
  - [3x-ui](https://github.com/MHSanaei/3x-ui)
  - [hiddiy](https://github.com/hiddify/Hiddify-Manager)
  - [Marzban](https://github.com/Gozargah/Marzban)
- without a GUI
  - [sing-box](https://github.com/SagerNet/sing-box)

---

#### VPN

**why we don't use VPNs to circumvent censorship**
- VPNs have a distinct signature therefore it's easier to get identified and blocked
- VPN wasn't developed specifically to bypass censorship and restrictions
- the main advantage to a VPN is end-to-end encryption which pervents interception of communication traffic during transmission and safeguards against the leakage of trade secrets, therefore it is not specifically designed to **circumvent censorship**

**usecase**
- when you have a home network and want to access that private network using an open network like a **public WiFi** while encrypting the traffic, then a VPN is a good option

- want to make a private network for all your employees because that's good practise and/or you live in a fascist state

##### list of VPNs (list is not exhaustive)
traditional VPNs
  - wireguard
  - openVPN


Mesh VPNs (overlay networks)
- tailscale
- nebula
- netmaker
- netbird
- zerotier

opensource VPN service providers
- [lantern (free/limited quota, paid)](https://lantern.io/) working
- [riseup (free)](https://riseup.net/en/vpn) not-working
- [psiphon (free) made by citizen lab](https://psiphon.ca/) can't test it

---

#### proxies

**why is it preferable to use proxies to circumvent censorship**
- better suited for this task
- tend to be harder to identify and hence blocked

##### list of proxies (list is not exhaustive)
- [shadowsocks](https://shadowsocks.org/)
- [xray (v2ray fork)](https://github.com/XTLS)
- [trojan](https://github.com/trojan-gfw/trojan)
- [Hysteria2](https://v2.hysteria.network/)

#### obfuscation tools 
- [cloak](https://github.com/cbeuw/Cloak)
- [wstunnel](https://github.com/erebe/wstunnel)

#### bypassing DPI 
> Caution: this DOES NOT hide the fact that you're accessing a blocked site
- [zapret](https://github.com/bol-van/zapret)
- [ByeDPIAndroid](https://github.com/dovecoteescapee/ByeDPIAndroid)
- [ByeDPI for linux](https://github.com/hufrea/byedpi)
- [Goodbye DPI for windows](https://github.com/ValdikSS/GoodbyeDPI)

---

#### SSH proxy

---

#### jargon

- **Airport:** platforms or websites that provide special encrypted internet access nodes

---

#### FAQ
- ليه ال قائمه ديه موجوده؟
كذا سبب
الاول: كنت عايز قائمه تقولى الى ال VPN الى شغال ف مصر و مكنتش لاقى واحده قديمه او جديده كل الى كنت بلاقيه هو شويه بوستات على ساب ريديت بتاعت مصر

الثانى: فيه شويت مصريين استغلالين ولاد متناكه بيقدموا خدمات "VPN" مقابل فلوس طبعا لناس متقدرش تدفع و الناس متعرفش ان فيه بديل و ان الادوات كلها مجانيه عشان ولاد الاحبه مش بيحطوا لينك المشاريع/برامج على github
انا عارف ان فيه ناس مش عايزه تصدع نفسها بكل الكلام ده هما عايزين حاجه شفاله و خلاص و مستعدين يدفعوا مقابل حد يدير ال infrastructure بالنسبه لهم, بس على الاقل النصابيين مش بيحطوا ال toolchain الى بيستخدموها الى بالمناسبه هما مكتبوهاش ولا هى بتاعتهم

الثالث و الاهم : العالم عمال يحدف على اليمين المتطرف, كل يوم الواحد بيشوف دول ديموقراطيه اليمين فيها بقى مهيمن, الولايات المتحده اكتر دوله بتنادى بال freedom of speech حابسيين julian assange و سنودين هربان ف روسيا
ولأ الواحد عمال يسمع ان تلفونت الصحفيين/الناشطيين السياسين عماله تخترق اجهزتهم و الجيش و امن الدوله معندهمش شغلانه غير انهم يقعدوا يشتروا من اسرائيل  ransomware
, ف من المهم ان أنتَ/أنتِ تعرفوا تعملوا proxy سيرفر بنفسك حتى لو بتفضل الخدمات المدفوعه

- انا جربت اشوف tutorial و لقيته يا اما بالصينى, الروسى او فارسى ليه؟ليه كل حاجه على ال github معظمها بالصينى؟
لان الموضوع كله بمطور صينى كتب shadowsocks عشان يقدر يتجاوز جدار الحمايه الصينى ولان اى حد عايز ف بلد فيها انظمه فاشيه/شموليه بيبقى فيها حجب على الانترنت ف مطورين من البلاد دى ساهمت ف تطوير ال ecosystem كله

- يعنى ايه البروتوكول *سين*؟
[project V](https://www.v2ray.com/en/index.html)

- ليه بتذكر البرامج/بروتوكول المفتوح المصدر فقط؟
عشان الشفافيه ولا الامان ولان فيه حالات بالهبل عن مقدمين خدمات vpn زى nord, express بيسلموا ال logs للحكومه الى بتطلب بيانات المستخدمين, صحيح انت برضوا فيه خطر من ان cloud provider يعمل نفس الحركه بس على الاقل انت الى عارف البنيه التحتيه بتاعتك و تقدر تتكيف مع البيئه مش مجرد مستخدم passive

- لو ال guide دى للمصريين ليه فيه كلام بالانجليزى؟
فيه بعض الكلمات الخاصه بالتكنولوجيا ملهاش مقابل ف العربى ولأ الانجليزى لغه النت بس..
