
# ZAP Scanning Report

Generated on Wed, 28 Jul 2021 06:25:20


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - PHP | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 1 | 
| Cookie without SameSite Attribute | Low | 3 | 
| Cookie Without Secure Flag | Low | 3 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 6 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 3 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 7 | 
| Timestamp Disclosure - Unix | Informational | 1825 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="http://www.cnil.fr/vos-droits/vos-traces/les-cookies/" target="_blank" rel="noopener">http://www.cnil.fr/vos-droits/vos-traces/les-cookies/</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="rf_link" href="https://visio-agents.education.fr" target="_blank" rel="noopener">https://visio-agents.education.fr</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source - nouvelle fenêtre" href="https://github.com/betagouv/visio-bbb/" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=yõñ'OØñ³\x0013öq:áçsá\x0010ÌhÎ
ÇÙv9üüÝL'óo\x000c»ü4\x0008v¹Ì­àÊtf_<N~NØóÓ\x00136º­V\x0017²bÇ§á\x000caUn\x001d³ÞäÂ2)dn5³Eîeë¤ÄÆ\x0011i¨»ª\CWëÅåR\x001aölÃ\x000e\x001fé\x0012«xî-sþb¿öI\x000eÂ9í\x0005Í1Åè)J¸\agìå4Då¹±L\x00149×­\x0012NCÝU-ìèaµ¤äÅ0¨\x000b9KüUdÖà¬#ëÂ¤5JÑÑ}_±\x0016*D
ò\x0005S\x0005'?\x0018\x0001it"®ujdni¨½¦QMZ7\x0017ý\x001e %"¦ «) ±åØ(wÔO/!`¿2@ê°\x001d,hà##qPtã\x0001áeOxëIÝ{É\x001e´D7:¤±þ$Ë ÏÓªZWËsöv~¼©ªÍúýüìÏ\x000fËùëÅåêfQ­67ó7·¿TÄz±ÙTËmë6ëÅ\x001d\x001c
áö]}|\x0006á^(&`\x0016 èì.fÀW\x000c(\x0010*wÀñÙ6ÓÊy\x0015Ã\x0019\x001fa±Ç
F\x0007Vx\x0001ÍÎÊ·à³÷ììéäùÙ0RÔ}%\x0016tËH¬ÀÂA`Mª8Øö¾\x0002¿Í^/¶ÕÌd«rõa¹e³#É³¿ñ£³Û\x001b°3±;ÔÐßB
Å\x0005\x0005j±ý<SQbàâ\x000eyM\x000bã\x0008\x0000å2/,[SØ³¹R5C\x0018N5Þæ¶ØQÎHJ#Ci|Ý0$\x0002¢ai/#\x0005ÍOG%
«µ.r½c`µ6¨¦fh+(Ö¥½j*\x001eE«\x0013#
sÝ0¢¬i¯¤G:*Qe_o¬¾NÚÎ#·Á\x001cµ\x0007¯ãg¡¸\x00118\x0005#Ci«\x001a\x0004Jø\x00146,÷L@¼"FHdªvä¨sÔÿ®\x001arÔBßÇSaþá=?qkWgxºwB»G¤"\x0019Û*vÙÉ9KÙR0*\Ú®7Ö
£vVÇ\x001d}\x001bã7\x0006è\x0019¬kÌ­[Æß9¾ç¬®#;~nß8¾\x0007\x001eÚ\x0018+%©H\x0008\x0015Ñï\x0003¶	\x0019#M;vú=\x001bi¨\x0010±\x000fH*®\x0018¡\x0003¶Å\x0012joÁB¾8¹^!³}¼]þ\x0011ÒÝ
	¤\x001d©ð\x00118\x001f6·ô¤h³ÅÅÅª¼"ráÀ³õâÓGìrKys<å\x0014ßJ\x001b
³íks
\x0016ìbyó\x000fÄ©¶KFz/YE"c¨ºC<·×ÈHM\x0011a_ºBå\x0002\x0011dÒ¨ó$ïñSt>ßn~(Hµ"0ÒøÈIU?Gà\x0005XH[\x0007\x0004g¤\x0008\x000ecP\x0004HX\x001a+ Ý\x0001q#Tl(ë\x0010\x0003ê\x0008mQìÒ¹¦É\x0001@öz0Yå\x0012\x000cgãða*LF9Z×ÎHhªÍAiº\x001bByr'u0á\x0016x46¾\x0008×\x0015ÝÇ\x0018EUÎ
Ýf0\x0014\x001b£h²ÌQÓÆy\k\x0013	OÙn)xØ\x001d3\x001d(}m¬ÍÇ(RÃÚh+%,DÕçaª¾TNÒæüesD?\x001aV4yçç&d\x000eÔ7 MYl\x0014¯h\x001d¥xµÔ9	&\x0011ÐËà:ÉN
³¢\x0001lgÿ»±ëQ¨¨NO¿C±\x0004\x001a\x0004ª[4®@\x0017¶¸)hÈZ\x000bHq(©L¢&\x0014l¸¿`cT,"ÃÂÁ,P\x0016&\x0010É
Jø^¸Å°cÃaÎE\x0001Êw\x0014°\x0007ûJÔ\x0001<Öêr	cÒL¢8§Vd
\x0005]\x0010	¤Jv\x00083Qî
\x0008ã¯	û\x0010\x0001¸JãèfJÜÓ\x0008\x001c\x001a. (jKS°1&ÓTë7FÑ:Ð4Xæá\x0001Ú×¶sÇÑ+ZEdTN\x0018\x000c¡T!!AI#©â¦È½h(X!ª\x0018háC­)\x0007Ôx6\x0011\x000eLö\x0004¥w\x001fêëH\x0013~áiDªH\x001bÂ¬÷©)\x001fTOTàºE\x0007ùÒ6$x:>Ë~±üÂÎ"¾Ì\÷räÁ~½JètºÝXHä(O\x000fJ¦÷bUsÙ¿;o|i£\x0017cê`£7<´ï\x0010KU$9\x0004¥&§ø\x0004Ùa
D"×iôlÝèu¬¼nÑÉ\x0007s\x001a­\x001a&\x001d[¦èÙ¨mÁÆ¢É=Û·ÝÒñYcÓ\x000f»\x000eïaa&B|\x000fz\x000eUõB|u!,Ñm ÔÊQõðµuý§ÅíouU¹ØÆºùÎr^È¨ì«\x0007U\x0011Rc_wÙâÍìb\x0003±d¶^UK(ö\x0007¤
\x001fïf\x000c¤\x000ft+7ôóaí¶Ú/yÀ\x0013\x000fy\x001côð¡Öí«\x0012ì¿!-nªå
´<;\x000fN`3U%\-¾«S\x0011õc#êÑPsy\x000eªMmxiPÊSZ\x001e\x001dª\x000eÿ,ÝÜ=Øï/£&||Ý ÍýMÖ{ð\x000cG\x001a®êö4D]\x001dÞ5îÒÿ\x001e:¬øÔy:;²dLÃ·gg[tx\x001e®Æ'¬ê²í]V¬»kt(\x001f\x001c©yÁõ¬ÿó\x0012ÔÁÑA< ÇíZ\x0004ð\x0010¥\x0010ìa\x0001F7y
endstream
endobj
154 0 obj
<</Type/XObject/Subtype/Image/Width 961/Height 525/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 42787>>
stream
xìk\x001cÕçÛ\x001eGElÄ~\x001cÇÆ:Öcì
olìÃþàYÏ~°\x00070ö\x0018\x00023¬Ãj\x0004\x000cBB\x0002ô@G\x0012\x001e#Ç6\x0016\x0002\x000bÀ $a#@\x0012\x0002!d	½¥ZÝz¢7­÷³[ýÐ£ÔïVËôª£>¾ùÎÊªìÌúøEGÖÍ7oVòþêêdVOOoO@\x001e=9räøÙ³ç\x0006Ý°pöî=´~ýæ\x0017³\x0011¶yùò\x0015:åËWÛ®4ééÊÊQLT»£6	Zp/,\x001eÙl»-ôöþôÕÖîtªÀP\x0005ªvôè)÷jV¬sSAÛqgò¤_\x0011Ô2ýöôoýtÃè\x000f±|ùªE>¸»ò>ÏÝ½úÊë'Nö\x0010ÜYøî{;wîqzIP¨W¥éÌoóûHÊ­ÐAQeQÊ×¬^/å´\x001cºçNí'¡Cüå¿ýÊ\x001fþð²S\x0005þÀDø¹}áù\x0017yaÿþOçÏûó·Þ]¸pÉ%\x001fîÙsÀiÃÓßË

Í/·¹·O\x001aþç<ã¹\B\x000büoÜÏU(ÜÅPv4~Üc¶«¨\úãÌÉ÷¼gØÏûyrÙÑ`ï-m>õý£Q}6¢mmðRÔÑL`ß¾îu¨BTÂ\x0010bï7þÀ\x0003ãIót	ÉÉÂK#ÙK{{8\x00151aÂßüæQ£&èB*\x0017¾G:\x0016:
\x0017ø`CððÃ\x000fèL\þÌDnÑôÁ\x0018;ví*:L9ô¡*|_.ª\Jvºò°B{JõõÍT*\x0007½²E¨ÐÃîe×5Ð{qjÜS¡Éý÷ÍIEÈR´\x0019/CCûÒ\x0016j¼Â¨\x0014Ú³ÛÅSh}\x0008´,_\x0013´6ëò 8µ\x001fù[TJÈÇ>2Ñ¥|`|~ný 
]]][S³ÃÏ&¬Ðî¬[·¾ÃÊ?mú'/ÿliA_\x0001¨\x001aUvj'ÜÅ!O¦¯Ò¶«æÏ_0aüã^GSèÙÕ/\x000fµ-È{\x000b\x000eCQGO±ÊåËW\x001b5½ä¹¸\x0008\x0015º¾¾IÏïi®©Ù\x0019­NKãÖ\x0005Ò¤iÓ~\x001fÉ^¶l©Õ¼téJ*$¶Uhª\Ô³Y A\x0015:vf¢µh²VÛ)èÈñäY´ËÅÇÿ,t+[
M\x0001ÚÖJ¶°Yhúú cñàTh\x0012HíÆK&\x001d
í§\x001b¶_Ã,Ò¶C
í2ÿ¬ß±Á¯Ð<íì>ÕÌ\x0013Ô<)íT'ôÅ0ëãë¶×QhnÏV¿\x0016p"\x001a
\x001d¢zbV\x000fÖ<|³gF«Ð\x000f<@Òõ±w\x001a§h,º\x0018f]à#ÄL¦OÉ¿BSå¢Í\x0002ùéÏÿÕåAâÏL\x0016]Ôÿ\x0019ÑpNû¾øJ5Ú\x0013\x000fDóç/p¿@Q\x0005\x0001Ë\x0016\x001anF>ðí¼1A«<½Ý?õõÍdÎÔ,ý¥ek\x0005?_\x0013²\x0001\x0015ZR\x0002¸P'\x001b\x0018/³ý&)"3ºf¶ÎP«a>ú¥No\x0010¶íQßi\x0002ÖÚm+N\x0007\x0012´Ü\x001d'Uv\x0011rò@ÙD¿!¶èÒ¾>|Ý\x000e-ó.Þ¢\x000f?üËÿö+üÍÐ¡?rÛ:c\x001f(\x000eL\x000bT_ZãéeÛf¥qYEÕ}\x0019\x001f\x0018?Ûlÿü¼Nw±~´B\x001f<Xg{:¶oß][³âì\x000eQè\x0006¡\x000cgRñ	¹@\x0015¨Ó\q¶0®\x001cv¯Ë,´SÂE¡·ÍîOðø¼ÂÄ×ª¯K¯Ô¤\x0012©iÝ<_¹zÙ×¶µÄPÔÑS\x0006q=åeLEÈAê%\x0016Í{g¦¿E:4ë\x0002/GbìÃö¯ÐT¹ð=Ò»gÛ¸@f\x001b®åïÜ|WÝ(°3\x001aúl¬^½Á\x0013²è\x0008?6.ð×\x0002w´|ùj
]ìYqÏçfÚÎÜj¨$À\x0001$ó-´*\x0004jÜøi¿#Å¥¿¶ìBä
-:A!zæ>\x000b­%\x0015%;0+\x0005ÆPhNaÕmjU\x0016	¤\x001dérÛîéú.*ëg\x0016Úz !ÊÝÑ=túFàÒs:XyC¬©ãNïí[Äëy~§·HLmiAmë*\x001b©V95«\x001b
Æ¾¬\x001f\x0018?[ýÖéo=ü
ËE¡W®\#¹Ð«j¤­;öí=ÈË§NËúSèlÞ¢éß ËzZE\x0015\ü9[p.´S¶\x0006ùóìY¯¹o>P¡sª:|ÿd9O\x000e\x000fÈô8úþ²êë\x000e|Ý`«gÉZçÍ?Wôh[K\x0012E\x001d=IÄ$Å\x0019iª\x0010Iæ§ \x0016MzÀù¥ûsBOþò¼yo\x0017¾Ò+tñr¡ï\x0019\x0011 {üÅN_:£¹x1ÛÔtÁ½{\x000fB>}®ð}ùIäX¸pi$3Ãú\x0003I\x000bãÆM¦\x0012ú«\x000bt\x001bÆåâÃS:î\x0017¨Êa÷ºd\x001eÚân­!Ò9<³5Âu¦ÀD\x000e\x0017³²*´1Ìbæ>1ët#¡5AÚ6Ê
\x0015×\x0013¶\x0006~\x0014Úz !ÊàCs\x0003wÙ\¾°"êùÏöÞ"~\x000fé¥þ^ãù óÀ<3ì^\x0017è\x0012GÚ,æ¬g­\x0008B\x001bûÒ\x001f[]MÏÕëMD¡5\x001f¯\»µz;×Ü°Á¼\øTèl>#.8¶²J~®E¡/Ùü\x0005va1 \x0012·Tëy`D10£l6g°ThÎ÷\x000eL½8ºìIÞÊvsëw­%¢dúÿâmÓ/©\x0002Uv¿lÑ,Åðç\x001e/&M"Wâ
LO"Ç	\x0013\x0002Õ/Ò\x001f\x0004Ì9*îÉë±ç\x0007cìØIÜª?Ô&\x001fÑ\x001d]¡ëëiÈpùÏSZE\x0015¢ø
¡ÐÖ{\x0006mSDl¿\x000e\x0014ïvÂ@
­\x001bÑæ8aÍÄÆµïùQhÈÕ¶NGa­àt !Ê³ýy\x0005.o¾>pk\x000bìç,~¼`d»´ïô\x0016e-Y\x001fN
M\x000e,i\x0015Z¡uöS\x001dR_a^ j2l»`(´é¡\x000f¶Ø
M¼,/ðT³f« í_¡³y_µýo/§rÐ\x0017Co]0þñùó\x0017Ð2ßE(ÏíñÚüs\x0011U³¾ì·÷h®+´9ëë,½ÖÍÊÑ¶(:zò\x0018]_ßäTV\x0015);-ºx\x0002æ®Ð´w÷\x0003÷íí\x000b\x0016¼G\x0016m}4Ç ¿0¨B÷\x000c\x0002Ö{òß"écé2\x0011M«¨B$ôFfNÔçÂØ\x0015:ÿ¿Q2OÛ	\x0016*¤UÉÒVJ0\x000bm"bûØ\x0010\x000fµ£Ã¤¡Ó³'\x0011ÎBëf­\x0016­ÿëÜxidD\x0018ÿ_ï9\x000bíB³ÐÆñ:uÏå@XùxÆ]K {û.-snû,4'!ËK[vªÃ\x001a<öTåYÄØi\x0013ÁE¡ãMB|à![Y¥B?	`\\x000c\x0019ºî«ó3@øYvTB{÷aÑ\x000e\x001c¶÷\x0015\x0006^\x0014\x0002\x0014Ú³µDQì\x0001tÚ´ß;Ýõ¯o*,\x001cy¸\u|â®Ð¼¯ÂÝÏx¨\x001d+´`LGGòP»âåBPèX-:rÖGdkÑÀ\x001cÕÁ&B¡³yA0þqcª^RaÐ\x001b	È\x0015ÚóA\x0017øf]²²ypôÌ±dB+´¼Ô¨þv#µÃåFBnPôFç¯:uï·þ\x001eªìG¡­\x0007\x0012¢Ü¶ek!\x001dî¶ûQðñê·Â¸ûÒv\x0013yÃm\x001bób{¢es¨LNë¤Ð¶uXôiÞÊv\x0013æ
.
íòùJ¡W®\#\x001bêçBoØ°Y9P.t6¯¯2AÃßù¸ô*\x0017
¼\x0018ºàÃ¢+r:Ý~,\x000c(ìÏ^¶^ûÍ
é¶µ$Qì\x0001=yÜ¸ÉÆÝXä	T\x0018á3µüÌfG8ãí©Ð³gÏä\x0012ÆD´\x0013QMA\x000f\hM1\x001e¨âI}}c1üY¾ªÐç'8ó'Úÿ7IB\x001f÷\x0018	³\x000cÁ´@/©0¨¯2+t!¸<\x001eD
BéóHT$ÛZ V¬_òq[¾Q5FÌhÙúØ:½­ç,´îç}y.%N\x0007\x0012¢Ü@\x001fQYx>ÌYß\x0012¨Ý©}#\x001dÝX«o»ÓËÒ\x0019½¹<\x001fÃI¡êp¹ís9l7ñ£ÐÖ\x000fÏÏm ^øî\x0012¹p÷®½zw7×ð\x00139\x000e\x001e<
\x000bÍSÍ|ç }eæïÎüa´ª¨¹ÐxY´QKçPâ:Ì|8*ÌUs^ÛÍ­Ò\x001bmk¡Ø\x0003hOÞ¢\x0017.\Jz0räøgNÐ\x0002Ýóæ½\x001dá3iù\x0016B\x0016\x0012[x¯ðä
ÃI\x0014:÷1çE\x0010sæüÙÝ©B	Îc\x0004z"Aäõö¤©é\x0002YtñÚç\x0014òsüs<Ñ>¢YÿàyoùWÀ´Öéw^"ÄÏU§yï®¼oñâ\x000f8µ#Ä|¯à2ñ\x001bî\x001cIÇÝZ­\x0018wü¹Ü\x0000\x0008ä~`ø÷èú ï\x001cä{\x000cù°ço<\x0015~1to\x000fý\x0002B±\x0007Pí\x000côQ$O h!ò\x001ft Å"\x001fpñL÷\x001cÔ\x0010~Âó±Ö\x0005\=B?q\x001eä)ÐÂ\x001dA\x000b
Çó_\x0004­-Á\x0017\x0013ÿ×¢E> ÑÁåá¨>)ås¡\x0013APvº\x0010\x0000?$ú\x0003CrB×\x001fk^\x0019\x0015úy4PT\x0017C\x0014b\x001fèOÚÛ»È§OiøðÑ\x0004-ÐËHòKC\x001fø\x0006) öK\x001cH´Ò\x0000 p1,7b\x001faA\x0000.Ob¿Ä\x0001\x0000@iÀÅ°Ü}\x0005e\x0002\x0014º<ý\x0012\x0007\x0000\x0000¥\x0001\x0017Ãr#ö\x0011\x0016	Pèò$öK\x001c\x0000\x0000\x0006\\x000cËØGXP&@¡ËØ/q\x0000\x0000P\x001ap1,7b\x001faA\x0000.OÚÚ:c¿Ê\x0001\x0000@±¡k\x001d.eç\x0019\x0007 * ÐåIW×ÕØ/t\x0000\x0000PlèZaYáyÆ\x0001
(tÙB×\x0019L¿\x0000\x0000Ò
]ß|Ú\x0014.éÀÿ\x0019\x0007 \x0012 Ð\x0000\x0000\x0000\x0000\x0000\x0000\x0004\x0002

\x0000\x0000\x0000\x0000\x0000@  Ð\x0000\x0000\x0000\x0000\x0000\x0000\x0004\x0002

\x0000\x0000\x0000\x0000\x0000@ H¡w"\x0010\x0008\x0004\x0002@ \x0010\x0008ßA
ÝÖÙ\x0003R@\x001f\x0002HldþËÿ\x0002\x0000\x0000  Ð©!n\x0005@ \x0010á#ö±\x0000\x0000\x0000@ î\x001b6"v÷\x0003\x0010·\x0002 \x0010ð\x0011ûX\x0000\x0000\x0000 \x0010wÞ\x0017»ûH[\x0001\x0010\x0008Dø},\x0000\x0000\x0000\x0010\x0008(tj[\x0001\x0010\x0008Dø},\x0000\x0000\x0000\x0010ûï\x0019\x0019»ûH[\x0001\x0010\x0008Dø},\x0000\x0000\x0000\x0010\x0008ÜN\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002
\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004bÄ¨1±»\x001f¸\x0015\x0000@ØÇ\x0002\x0000\x0000\x0000øÎÍwÅî~ \x0012âV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002
\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002
\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002
\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004â¾\x0007FÇî~ \x0012âV\x0000\x0004¢LãröÊc¿üíÝ\x000f>¾wÿ§¡\x001b},\x0000\x0000\x0000\x0010\x0008<Ô.5D¨\x0004\x0008\x0004ÂÌ]ðÞÍwÜK\x001cÿdèFb\x001f\x000b\x0000\x0000 r¾ô½¡_¼ëî/\x0019W1iJÅSS+¦>û;i
P9­½à¢Ð¯Î÷¶a£ö×\x001dç+ÖVÑK*¤åÿÍ\x001fhYÐõ\x0019Þ7ah«Ñ*z9bÜd½/Ý o«[so\x0010@¡\x0011\x0018ãØÉ3wÞóð­wXôÁÐÄ>\x0016\x0000\x0000@d|õ[óå´ÙIS¨&Õ¿ÏÁñTh[m¹¢ÐR®ÅEþòZ-ºâÌÔ\x00027%rÎ/EÔy[ªfh¶S`(ô\x001bo-ZWµµH\x001c?¥H-S\x001c?y>ZFç§>;SvZÔ½#\x0010}Ph\x0000@ZøÒ÷ÿÙ<\x000f\x0014iÚ*ö\x0007Å]¡ISEnyêØI¡y~X¬X¤Ú:WÌHSNÕ¬
íT\x0013D¨Ð=W¯~oè]O<õ¬K\x001d\x0016N^r9-\x0017I5In©qRôb4Þç¥Ð´_ëZ\x0004"Ú},\x0000\x0000Âùâ]w\x0007g\x0005m\x001b{ÿ\x0003á®ÐäÉä±d­<9¬\x0015Z\x000cKØu^®&j-ÕbÈìÞ¶{]\x00183á«\x0008\x0015úöÊ1ßþþí\x001d].uX8ÙY/Å¢\x0013\x001a³Ð\x0008KàvB\x0000\x0000 ¾X9"´?_·èÊ\x0011±\x001f<g¡Y¤	r]YhmÈÚ«ÛòÓ×¢Á"Ì2k­\x0015k²ZÛ&rX\x001b\x0004\x0011*ôã¿úÝýÿØÜrÑ½Vè¾|\x0003Ï\x000fÓ\x0002ig_¿WëIiZà\x0012Ze\x00188×áyf7´J+®ÔÆi§Ö=º¬\x000eKOx*Ë\x001eûBó\x001e¹Ãzïz­ìß\x0001Ýÿ¤¿@x\x0006n'\x0004\x0000Bæ\x0013:\x0017í©ÐbÅmý9\x0018.
-\x001b\x001a\x0013Ë"ÌÆ}TS'QksvQè6»¼\x0011P \x0006L6üyç\x00035
\x0016o\x0014ÖÂÙ7p:W|ÕPhúË¹\x0002sSüR\x0014Z»´4ËêÛg7,«¸W¢ú¶
Í¬Ü}v
m»w[Ã¡¿ÊN}àvB\x0000@ËÂ¤äE{*´\x0016f\x0017[\x0008y-o¨o!d©ÖÉÌÒÔ÷Thk \x0012÷öÿüß¾åÇû|(4Ï9Kê²Æl«Ðìº2+½z\x0013*\x0014¿íSîª\x0015ÝªÐz²Zºg«Ðâð\hUh½wcþ\ïÂÈ\x0015µ\x0008KD~mÿÆ·oÜ¸e[Ww75Þp¾iì¿M}¸\x0001\x0000¤¯~+ðý^w\x0017Fø\x001dÐeðRö
]\x0015£=p?
­
Öö¡vÛ¬KÚÔÝF\x001diMÏ$ë\x0006Ù±\x0006©ÐÚ`ìÖ:¨(dø^°xÙúÊßoªÞî§²g"Gºå°ÏBs\x0018\x000fìÕûa«ÐÚuû¼\x0014Zf¼=\x0015\x000bThÜ~\x0008\x0014\x000fjõ
gÎ5ülÄx\x001a5æ.xv1zâ¯â\x001fj\x0001\x0000©#÷üºPª<uãFÆº*÷¤»(ú6|ôãr÷öh\x000f\x001c?­\x001a
\x001cÁé£E\x0016½÷@gM§Û	E¡¦sûT"\x0007×\x0014e\x0011N^%/
)uJäðThª!ýdE7\x00129¬ÍúIäÐ	Õ}\x0003¿M R\x001fÈqË÷¿ÿÑªÐD{aeîÛí\x001dÿ,%\x001f}¼þÐác±\x000fµ \x0010M-±÷aP±ô/k57ön\x0000ÐSÐ.
¨{õ
t¥Kâ±£=p(tj(Ü\x0004&Oñåÿñ\x000f²WÜ«\x0019
RÎÞ¨o\x000cÉg¹P§m°RnP§Hû·\x0013º+´nY·`Ø¯Üx¨ï\x001cä]\x001b_\x0019nS·\x0013JoyrÛz;!\:õ\x0011ûíÿtÛÝÚ=û?%gÖ%<\x0015cT\x0003]{\x000fÞT3ô~és\x0012¹iD²_Z[Èq"ñ¥ï

°á¦ÐSð·\x000bo¯\x001cS«\x001f\x0014:5D"\x0003ô1ûßÿøãH\x001a\x000cQ¼\x0007Ó\x0019)(r\x000ey¨Ý®=ûC7\x0012ú\x001a>öß¦]½Úk$i46µ¼øÇ7}Èå\x0018dëêÏ\x0016HL·ZÁüà$è8ä\x0003ï©ÐÿÑ\x001cPèÔ\x0010zìÖÁ?­òôï_¤µØ\x0003
HJ»\x0012[ý8qêì;KëüüAÚË¿Ü76öA\x0007\x0008Æ<3\x0014\x0011$/\x0019W$¦£êäíc"¿0\x0003N\x0011ñ
þ\x0008\x0004¢Ð\x0008qõ¾éö{Ú;:mç*É³WZõ±ô/kN­/Æ \x0002Bc(´¼¤sÊ
)¡Ó'sÔ:\x0016\x0008®,´¹Tµz_¶[éµº\x001d®ÆzOeÙÚî?\x001f\x0002×Ã
/\x000b¼¡Þ¯µo¼ë¾sõüó\x0001Q\x00114\x0011ZÎ§BG\x000eÍ¹Ð×®]ûÉÏ\x001föØ\x000f\x001f\x001e»ûHt<G \x0010%\x0010WïSgÎ­Z·Ùv\x0015©ró'Nýé=\x000fó\x00139®^íôôs±¶@£µÌPÓpÑ³BÓ&zY¶âÊì·\H\x000bÒ¬íV¡²ÒÕ¾~}ÕI&º)ªÃåôWwF\x001f\x001c£´@mÊ1\x001ao\x001c5m%/kõ¿Ðyã p*Z,~jjáÝ+ê\x00139\x000c\x0019\x0012»ûH(ù@ "\x0010Wo§,\x000eæ¦ÛïÙ½÷ UèË?\x0017úÿñBìC-0Ð¹Ðâ
²XºÌBë\G\x0014ÚiÛv+c³ÙôÚv@v¡7´\x001eÑ7kSÆ&Æ]Ü¸îµ\x001b øQhù^¡3ýÏ¦Ë ]\x0015£=ö\x001füà\x0007±»\x001fÒ
ö\x0008\x0004"ê\x0008w\x0001'hïè4Æÿ3ä®×U]Î¶^»vMÚ§TxïC¿}À\x0005¸"-sJÆ\x0002$9\x0014®ÐR!BË\±K\x00072>\x0014ZÏ«\x001b\x0015tS|ì2§mücá\x000eDò/\x0008\x0014D\x000e9M±$r\x0014\x000fäB§HÆq\x0004\x0002\x0011K¾`\im\x0013~fú,2ç¦æ\x000bÏ½<çn»~?û7¾}ãÃOLÝ½÷ íhÍêØÇ\x001dÀ=\x0013j¶Ö}\x0016ÚBËQødiÖ:Ì!¶Ï²3f¡Aø¹P.tqÝNX$ Ð©!Q\x001f@D\x0014\ÆüõówÞû\x0008-üË}cÉ?úx½Óm,Øs\x0017¼\x0017ûÐ\x00032\x0003õR\x0012uò0¿ä¿¢}ê>;wÖùÏÆ²u+]"»öTh¥,ËF\x0006Î6nE4ÞÌÀo\x0013rÔz/Ò
ý¯\x0006:\x001d#~\x001ej'\x0017º@
\x001dáCíôDÊÊÊØÝ\x000fDBé\x0007}\x0004\x0002\x0011UDr=_¹vÓc'ÝG5\x001bª³WZc\x001fvAÆî¡v¢ òÁ°&xøÎ8?Ãºu­ÏYhéTÐ\x001bêÃ1n]´Uh§ú²\x0017½¼KÈ\x0011§V³\x0013Z¡£úiâ=ã¦nÝý@$D3#\x00108"ëùSg=gGOüU_L??\x0007Ò\x0007Ü\x0015d\x001cÒ¡åâ\x0016R¡#J.ê\x00139 Ð©¡$ã<\x0002(JDr=ßwððål«\x001fð\x001b+ \x0012 Ðøü,r¦6£ê^ñÈqÿý÷ÛúXK¶ãtcöØ¹`Ð\x0002F R\x0013±\x000f\x0000\x0000

r|õ[A`ÅIS¨ÍøË\x000bÛÛ	\x001b.´ÆîÀ\x0013(4Â|:®´¶\x001d:| \x0005j>OPìc\x0001\x0000\x0000æKßÿç\x0008\x0015Zýü`UèlGìr\x0008ü\x0000F8EÉ4²lãàá£­­münÓ\x0002½ô¿­í)},\x0000\x0000Bðóh\x000e?Dø bcUhäo$\x0005(4Â\x001aÅF\x0004\x0007O>[ßyÏéh#Íc\x001f\x000b\x0000\x0000 @¾X9¢P®\x001c\x0011ûQøÇªÐ±!ð	\x0014\x001a¡Ã¶ý\x0015QXèÉgkðt´T\x000e$Ò±\x0005\x0000\x0000P8ÌE'hþB'\x0017(4\x0003¶\È^i=TwÔÏé jTÙ©\x001d'},\x0000\x0000HÈåE\x0007½»pÒ¤ä?k ÐÉ\x0005
ð#Ï×\x0010\x0005ÇÁ:·Égkä¦£ëê\x0016<E:ö±\x0000\x0000\x0000"ã«ßÊ=éÎHO{~]\x0012¿a\x0005
\ Ðe\x001e.ò¬å­×!®"|Ä¥K}N>[6¼t9Ëï¶­NC¡\x0001\x0000éæKß\x001búÅ»îþÂq9~jjÎéï¤)TBåQýþ`\\x0014¨ÐN4nÜ~pÉªê?}°X¸¢jmÍ¾\x0003Ç\x001bb×Ër\x0000
]Îá.ÏNªÜ\x0008\x0012\x0007>=\x001chòÙ\x001a´ùOÐ;¯Ï­HÇ>\x0016\x0000\x0000\x0000\x0008DhÞºçÈì·>þÚ»¶¼8ÿý7ï]2Ó
\x0014ºÃÉYÒ>óý8bDN´¶èØÇ\x0002\x0000\x0000\x0000\x0008¡Ðu§ç,\ÁªüÚ;Ë×ÖìÛwô\x001c¯:t¢qËîºùKV?÷úBZ;ëÏK÷\x001d9\x0017»j¦\x0015(tÙÕõä3üy¶h\x0011éØÇ\x0002\x0000\x0000\x0000\x0008ªÐû5ðä3éñ'ªfÿé5Tí¹ïíúôtì¶J Ðå\x0019.þÌÙ\x001aqw\x0010á\x001d|¦´EÇ>\x0016\x0000\x0000\x0000\x0008DP¿d5ñ\x001bW\x001e9Óâéx+6í¤Ê¤Ü~* @¡Ë3l\x0015ý¹§§§»»;î\x000e"¼N\x0013,±h(4\x0000\x0000$@
½qûAXö¯Äo}¸6Y¶n[ìÂ> Ðå\x0019îþÜÕÕ\x0015w\x0007\x0011ÞA§É°èØÇ\x0002\x0000\x0000\x0000È)tGÆÓ®­õ¯yÔ¡MþøÎòØ3}@¡Ë0üý¹³³3î>"¼N\x0013[´dtÄ>\x0016\x0000\x0000\x0000\x0008D YhÎÞ¶ïX Ó{ùOK{}aìÂ> Ðå\x0016î)\x001cìÏíííqw\x0013á\x001dtØ¢e":ö±\x0000\x0000\x0000@ \x0002)ô¬?/%Þ~àD Óã­b\x0017ÎAÅ;G¼ðÚ;\x00056\x0002.·0\x0014ÚHá %ëèèhk+è9ÆÒ\x0004&:YtÊ$#ö±\x0000\x0000\x0000@ \x0002)4?dcÅ¦þ5ïÐF¾£°\x0010WÔ\x001dþËúmb¡D1üv¡w\x0004F\x000cp&%kooomm»\x0008ï ÓD'NLDÇ>\x0016\x0000\x0000\x0000\x0008\x0004)tkG·ÆÅÙÖlÝË³ó¯yïþeSÐôi[.ÜX\x0014¤ëðÉ³5\x001c¬Þu\x0000$-;÷3wì«Ú¾·jÛMµl¬Ù½~ë®u[v¬Ù¼}õ¦Ú\x0012\x0018 ¢ÀX»yÛî\x0003ummm2\x0011\x001dûX\x0000\x0000\x0000 \x0010A\x001fjÇéÐ?ÞâÇñX¹\x0003=ÁÃL¿B\x0013c~ñk|¦\x0005\x0016ÈEùXø%ñß¿s3°lÓK^ ¿´,m\x0012òR61ö(KMj:`Ô\x0017¨Öê½S\x000b2[.æÌSèF·­ÐäÏ'Ï5võ\íé½\x0006H÷Õ^Nbgw\x000fÑÞÙÕÖÑÙÚÞmm»½ráÒåæ\x000b\x0017J`\x0002£±¹eÝ±O\x000e\x001eèØÇ\x0002\x0000\x0000\x0000\x0008ªÐÔ!%&1³pÅþc
NÕÈ¬ª¦jÏ½¾0èíî
M
Ê6+
-Ì¦*	\x001eTÈ¾jUh­ßlÂå¼Gô6Ô]ÏS!À´w*ýtQhÙ$Ü¼zP®ùä ü9Ñ\x0018
ÝÑÕÍ
}¥­ýòÖ³-\x0017/55·À\x0000\x0011\x0005\x0006¦¦\x000bëªwH.Gìc\x0001\x0000\x0000@øï}GÎñ\x001d/¾ù¾uíÎ'Ic1U9o	ÿ4!Y4¹ô+\x000bmÝs¤p6f¡éoFYhÆb¤Vf
ÖöK/uf5ïQ´Yë´Ê>Øv\x0014Z\x00129B'u\x0004Uèê]\x0007b@P\x0008¶
ÝÚÞq¥µ-§Ð¹)èÎ
]¾é®û\x001e\x0019>ú1Í\x001dÃGO}vf¤zð\x000e:Mt²ÖlÞÆæèîî},\x0000\x0000\x0000\x0010\x0008RèöÎ\x001e\x001fyÛ¬\x000cXµå\x0017ç¿ÏË$É¼@Ì³héÚZÉßø¤îxõû«·\x0016¢ÐÚµ¾Ö²Ùf|(´4¥+sÎ\x0006Ûl\x0006

\x0006\x001fâÏ¢ÐF\x0016GSËóMÍN\x001fuU[ÉÂã§EO6½P)D\x0004	:Mt²ÖTA¡\x0001\x0000 ©\x0004úi\x0015Åç-Y5sþ\x0012bÎ¢\x000bWTmÙ]g»\x0015\x0019õ\x001bWÒ&\x001b·\x001f\x000c§Ðl¹,½Ú¥µ*ë\x001c	I·\x0010qD\x000eíÀ´ÖÈ[Î¸&r¸+´tOf¼õÔ·ô7Ôi!²Ë2\x0014ºñPèÈÊ\x001a\x001a>\x0000N
½héÑ\x0013	.eÐi¢µ\x001a

\x0000\x0000%D"\x00071Éjöçþô\x0001§jøäÐFRnÚ<¨B\x000b2iÌúÊÎÌ«Äå^?ã~CG-
ê
Ò~ÆõvBw¶ÞiÈ%ôuýØÀÛ	e
\x001a

\ÐY\x001cVæDèÆæ 
ýüì7îºïÊQÞ6lÔs/¿îþ\x0011&§Íð#%½\x0007ê¨Wq÷"@Ði¢µºª\x001f\x0010ÝÕÕ\x0015ûX\x0000\x0000\x0000 \x0010y¾ªñ\x0014Ú#gZ8gã­\x000f×Û>jã­\x000f×½²à#§Ígýyi Çâ%å\x0019\x001dÅ\x0003
]VØ(tÿ½Ùþ{	s
}¾Ñé\x0003`«Ð\x0012o¼µè\x0017Suùü|ó»C\x0017,^&Ëd­\x001f¹Eò\x0014ú|cN¡7A¡\x0001\x0000 ©ÜÿýAg¡«v~:cÎ¢uµû*ÌY´\x001cÛÖ®y\x0016zÞ{«bwÝ"Bâà¢Ð×\x001fÇ¿°Þ·BoªÞvïCOÈKOÎ\x000cbGMB×C¡\x0001\x0000 áL0¡­£[S¸Ú­«Ù£^g]õÎG\x001biÕ­{cwÝ\x0014\x0000.+"Whã¥§Bß^9®\x0018Æäóäi3øJòÍï\x000eåRY^¦Uø±`ñ2.ä\x0005Æh¡
¶u\x0008jÐhû¦w¡·âÖ2)ÿ\x0004

\x0000\x0000I'§ÐÁs¡=á\x001f%|eÁ²Ú½Çd:úí6púGìò\x000e ÐeU¡Bçh×Ô\<îSvÊ\x0019\x001d¤Ó"¥$±\±(4`s5ÚPJè%\x0015êidi\x0016¸Í¹¯_³Yãy\x0013^\x00163·¶ÌÝ¦\x0006Iä\x0014º©y\x0015\x0014\x001a\x0000\x0000\x0012K\x0014Ø´ó\x0010ÿ¡<¸cæü%´pèDcìò\x000e Ðe\x001f>SèóN\x001f\x0000qæyo¿7ééé«ÖWÑK*0å>
ÍÁ¾*ÓÑr1aËÍX\x0014ºOåNs1áÌÒQ
-fÎ\x0013Î~\x0007¦ríÕ²,\x0006îÔò ÊÜîË)ôùó9®immB\x0003\x0000@\x0012)B3u§÷\x001c>KÌ{o\x0015»ôM;cÏt\x0000.+~Ý;B÷öö>üÄSw\x000c\x001f}Û°QwÞûÐî½\x0007ú(t_¿åÊÜoòÞBó4²L\x000bË¬²\x000e#'DO2-ûQhkË\x0019(4\x0000\x0000¨)¶Bk®­}îõo´!vùL\x0007Pè²"BîS\x0016½}÷^.qWhÑ×/¥Zb3j\x0016Z¼7Ó¯Ð_Á	\x001b}\x0003õ_öå'öÈÛö
Ôf-ð²/Û3Ph\x0000\x0000\x0000QSJ&\x000e\x001co¨;Ý\x001c»|¦\x0003(tYáS¡Ï5øRè¾¼EïØ½O^º+4)¨¾MOn'%Fº2dÔ4i°dÝ\x001aoÈ·\x0004
}*Ãv\x0016Úi_Ö3O¡é4A¡\x0001\x0000 ÑäÈ\x0011ø×	Á`\x0000
]VD®ÐF\x0004Jä<$ÇCî(Lk@¡\x0001\x0000 éx\x0016\x001aD\x0008\x0014º¬(\¡ÛÚ;\x001ezüWdÑNcGê\x0001Â^Î\x000c¾yãh\x0003

\x0000\x0000I'¯ÐÁ~\x0010\x000c\x0012 ÐeEá
=ÈC'r¤Ûû Ð\x0000\x0000|0\x000b\ ÐeEê\x0015º¬\x0002

\x0000\x0000I\x0014ºµ£Gsº1\x001b»\x001c\x0002?Ä¥Ð·þèG\x0015\x0015\x0015±+e\x0008vìÚM=7ÿÍ\x0008ÛüÝÐ
Ò\x0002½äe(t\x0002

\x0000\x0000IÇ:\x000bÝí]\x000e\x001f­Ð_ÿú7*T<öø\x0013ºt4v%\x000eJZ\x0015zsõV}¦J`\x0002\x0003

\x0000\x0000IÇªÐDÃÖØý\x0010xR\x0002&xü9rù,=PhÄ 	(4\x0000\x0000$\x001d[æ¹hdt\x000crJ©ÐZ>
i´NSó²Lbó|5¿Ô[qãÜ2È­m\x000b\x0000k½dÃç°\x001e¬ås\x000bôW6±~SúúðÃ´\x001a//ÛV3:ÉGd[ßI¡u\x001fÞ;ÏV¡ÈB\x0003\x0000@ÒqRh8<GíB\x0014Ú*R\x001d\x0005ÍÐ0g®À^ÊúªeXì+h-7ZpRhÞP¤TÑûÕséT7á
Ü\x0007®`mÖÐu'6Þ.ëb\x001c>/ØÖwRhîd÷ÕÞ¹óæÓ2\x0014:Ñ\x0001\x0006\x0000¤\x0003N
£v¹ÐVÖÉõY/µøÑlhª^
âÕÖ\x0016\x0014Z\x001cÛðpë\x0017\x0001§D\x000eiûcô6¦Ð\x0014ÚVõ®
½·­o«ÐÜ1Iäàh(tr\x0003

\x0000\x0000I\x0007
\x001a<GíBf¡µÎãéÌ\x0004à¤Ð²,Ò«3\x00198B(t%|*´î¿»Bë½\x0018÷Q\x001a
­¿w\x0018®.ù!ú]µÖ·Uhë\x001be«Ð\x001c%0@D\x0001\x0006\x0000¤\x0003N
£v
-*ë4\x000bmmC¡e®µb`fu×\x0014ZÏB»\x001fÓÄ²\x001f¶}Oô»¡ç­³Ð\x0002W£\x001d9Õ÷3\x000bít;!YÙM7ß\\x0002\x0003D\x0014\x0018Ph\x0000\x0000H:PèÔà9j\x0017~;¡1\x000bm­ã®Ð²ªb`ò¾cÎ½
ç¤eñUCéuþ³^66wWhÝ\x0019Ãù/\x0014ZD\x000e}»%Upªï\x000bMË¬ÐÛvì\x000c\x000bÝÔr¡rÔ£ÿ1cðÿþuìÔggFä\x0008_\x0001\x0006\x0000¤\x0003N
£v¹ÐN\x001aiMEpQhÞÖ4Ö{±Þ¾§[Ô\x000b~^\x0002ÍaÌ\x0012÷¨,\x0008«Nóä&D[Ö[gÝy­$¨Èû`(´ÎÄ\x001eÚÖ×
òVìÞ$Ïº\x001bµÛwSèã'Ï\x000c\x001fý.\x00199~Êè¿<mzoooA^ð\x001dPh\x0000\x0000H:PèÔà9jã\x0007¾\x0013Má¿NxäØIçÊQÞ6l\x0014-\x0010\x000f=ñTwOÏ3Ï½üà£¿¼ûÁ¿úl¤p\x000c(4\x0000\x0000$\x001d(tjð\x001cµ¡Ð¦p~ã­E/½ö¦¼<~òÌ\x001dÃGßûÐ\x0013dÑ\BjÝÖÞáò\x0011Z°x\:ö\x001e¨ó-\x00083 Ð\x0000\x0000t Ð©ÁsÔB'b(ôðÑ½ùÎ\x0012±hw<m\x0006]1xüùß\x001dêß\x0018©>mK\x0006ît\x0007\x0014\x001a\x0000\x0000\x000e\x0014:5xÚPèD\x0013¹B÷öö>:å×dÑwÝ÷\x0008ßNè®Ð\x0019Ì<G\x0017Ph\x0000\x0000H:PèÔà9jC¡\x0013Mä
­Ë9\x000bÚE¡\x0017,^æ4íLå|1<m\x0006ð2\x0017Þ^9F
ÅÀMè/Á\x001fãt\x0004\x0014\x001a\x0000\x0000\x000e\x0014:5xÚPèD38\x0015\x000cYÌ*ðrf NsþF¦_¡i\x0013Éè M¨}»¬¦¸¡Ð\x0000\x0000t Ð©ÁsÔB'Á©Ð\x0019¥¾RG\x0017ò\x000c³.4.A´\x0015UÉê2	(4\x0000\x0000$\x001d(tjð\x001cµ¡Ð&^îsÈÎ¨Ô\x000b'f=Î(6\x001aBC¡\x0001\x0000 q@¡Sç¨
N4±+´~"G_>\x0007£Ï9S5øA\x001cbÎÈ!ÂÌ%Ph(4\x0000\x0000$\x000e(tjð\x001cµ¡Ð¦¨
}ç½\x000f
\x001fýØS¿éþ\x0003r`F=¡ÎövBÛBëí¼C¡¡Ð\x0000\x00008 Ð©ÁsÔB'\x0012ÌBG\x00152»70D@¡\x0001\x0000 é@¡Sç¨
N4+tíÎ=#ÆN\x001a7iÁÈñSÖUmÐ\x000f3Ph¯B\x0003\x0000@ÒqQèWç¿{Û°QûëóKZ^±¶J¯b¸Â¿ÿæ\x000fR"åºÔ¤F¤D\x001a\x0004PhàNá
]²È@¡½\x0002

\x0000\x0000IÇS¡É
ÖjÍ>,Í«t\x000b#ÆM6Õæl]\x000bBã9jC¡\x0013M\x0014\x001aá\x0019Ph\x0000\x0000H:î
ÍsËl¼²@ÞK«¤\x001a½\x0014ÍöThmL>\x0017	ÏQ\x001b
h|*týy(t\x0002N\x0013\x0014\x001a\x0000\x0000\x0012»B³-³\x0006[]!\x0016O¶*´älfKÊÌ]Hð\x001cµ¡Ð\x0006
¦B\x0003\x0000@ÒñTè¶~g\x000e§ÐN©\x001aWÂñ\x001cµ¡ÐF+4[4\x0014:¹\x0001\x0006\x0000¤ãG¡Ii(<CcäQ\x0002ñ\x001cµ¡ÐÆB7æ\x0014º±\x0004\x0006(0è45æ\x0014º¶­­

\x0000\x0000IÄB·å=9ªÛ	¦¬AxÚPèDcUè
ÝB
ÝÜ\x0002NDä\x0014º¹e5\x0014\x001a\x0000\x0000\x0012OÖ\x001cmv\x000fµ³µbã¡v´9·i»-B\x0003\x0017 Ði
(4\x0000\x0000$\x001dü´Jjð\x001cµ¡ÐÆE¡³¬Ð\x0017/5@¡\x0010
Ph\x0000\x0000H8PèÔà9jC¡\x0013BwuB·¶wd[Û>WèÆ¦\x0012\x0018 ¢À ÓSè*(4\x0000\x0000$\x0015(tjð\x001cµ¡ÐIÇE¡/e¯\¸x©©å\x0002\x0014:\x0011A§NÖêªmíííÝÝÝ±\x0005\x0000\x0000\x0000\x0002\x0001N
£6\x0014:éx(ô¥Ëdeç{{¯@\x0002\x0011¡N\x0010&:Yk Ð\x0000\x0000X Ð©ÁsàB'\x001dã×UH¡Û;»H¡¯´¶åî(¼t¹9G!éÙÕÞÞ\x0012¨ "DÐ©¡\x0013D§NÖÍPh\x0000\x0000H*PèÔà9vC¡\x0007\x0015\x0015\x0015\x0015A7±Uè\x0001\x000få¸x©)\x000e}®áüsçN>sâÔ©c'N\x001e=vüðÑcuGÖ\x001d>ò)QwøÐuê\x000e}
"ÞÌü»Jo/½ÉôVÓ\x001bNo;½ùt
èDÐé B§&ÅÑÜB'kíæí\x0008ÝÓÓ\x0013ûX\x0000\x0000\x0000 \x0010PèÔ\x00006Ø±k7iêc?\x0011BnoýÑÚ7jöòõ¯#ÐVZ¡·íØI-<:ñ1Rè	N¤åª-Õ\x0017.]\x001e2d\x0008-×o<[ßpúì¹9>},úø	r¹#GÔ\x001d&Ö°ïBPïçá¼9\x001fÉË3½íÇsþ|N\x0004\x000e:)tjÎ757_¸@'kí\x001dPh\x0000\x0000H"PèÔ\x0010¹BàòKrÑ\x0010\x0013§12oþ!dÅ[ä6/NÓ^\x0002\x0019>w\x0015ú¹ó¨?¼õVQèÍ[ª/^Î~ík7ÐòÚõ\x001bÄ¢O9³è§Èå±K\x001f?³;2j\x0010)ü®æÞÞã'è­¦7Þvzóé\x0014hæ)h:Yëò
ÝÝÝ
\x0006\x0000Ä\x0001N
ERh\x0011ÈÄ)tT[ì\x0019é 1î(lïìº®ÐÕ[ù¦Âë\x0019ÑMlÑgÎÕ³Hót\x000eÒé\x0001\x0004\x0005óùûy"¯Í<óÌòL§àº?çeG'N\x0013¬õÕ;y
úêÕ«±\x0005\x0000\x0000\x0000\x0002\x0001N
ÅPhÎ7àhC¡ù%\x0007ðüí¼ùoòK­ßÜ®ÜÓ?K,Ó°Ü onm\x001bÊÔ7=Ql­Ü30êð/WãB½Gi·âó\x0008½	÷Cæçm\x001b7B*[ûl¶=RÝ=.\x001c\x001dý
½ekÍå+­Co¹Ù¢\x001f~d¬l²jõ3çÎÎIÉ£Çà:}_øÃÌ¿û»¯ñ\x0002\x001fÃuxÖ\x0012´°âãU\MÚú^Ë
rãº Æ¥J÷xN=Î\x0018ÍêUz\x0017¶ÝýÞxãÒ,oÅ«Þ\x001cÍ)ÞÌ~Nes¾.Ï¹üçüü³øóÅËY:Yë·îâ)h(4\x0000\x0000$\x000e(tj(B³\x001f\x001a
ÍË¬âxN
­+Ó_©`5a½#£q'±tiÜPèælõ|p¶-\x0014æ]pÚÆue£cÜ¬áí
Ý£f¡í;w±KwtuHÓruMm¶µ\x0015$möìWháåY³Ï76­Y·þÅ^&#\x0015¼éæIêV­Yóê5kÎ«W]¯¡Â1c\x001eâe\x0016WZ j\ßZ9óE*¤¿\¹ñ¦¤\x001dÞÖ¨Æ\x000b²\x0017nY/[{¢Ë¹5Ý
î§µ5½_êlEËRÚ7ÄéÍ18ËÔ7\x0008ôn\x0013õç\x001b\x001b\x001a¯O>7µ\ÐþL'kCÍnöçÞÞÞØÇ\x0002\x0000\x0000\x0000B§")´±y+:)´1Û¬1Úä:¶;¥KãVÖm²µ·ëÎ;)´¶YÏÆõl¶\x000bú\x0000Ã)tgw\x000f+ôÖÚmWÚÚY¡IÒ6Vm¦!C¹ñî^zy\x0016¬]·¾¡±¼ñ¡\x001f!Ç£BòjZ0 r®@°¸Ò\x0002Ù¸Qnl+5m¡
isjÛÑÛäS	ýå´JÚ±í	7¥{+ÛZûI­qeÝ=]GïN:éòæØÒ\x0017æüÛÞsyfyn¹xIû3¬µ»¯æ\x0003

\x0000\x0000\x0003
\x001a¤Ð=\x0003\x0013\x0015z,Oº.\x001cÒ`(¥lb§µq\x0017±toÜ]¡eÙsjºÇò¤\x000eyéÞxÃ7tbF$
]S»­µ½ã\x001fþIÒ.e¯¼òê\x001f¹ý¯}í\x0006R¸GÆ«\x0018\x0018\x000f?2\x0004\x0016n\x001e2\x0016\x000c¤\x0002A-\x0010´°nÃF£ÜØÖ¥5	jJ^5[º'/é/×§F¸Ü©'7ç=¢C¶µösZ¸PwO^êÝIeÃq¡)ïÌLÎ<ÓI\x0011¦µ©ö\x0013öçk×®Å>\x0016\x0000\x0000\x0000\x0008\x0004\x0014:5\x0014O¡E\x0017m%Ós\x0016Ú}ÆÕH\x0017qjÜE,\x001a÷£ÐÒ¬*¶í.ÑSô(tWÏUúSèmÛÛ::Y¡ÉÐ²ùß[!g«Ú¼JÆ\x001bÏF½±j3\x0019
\x000c\x001dj\x0014r9Y7/³¸ÒÂMUF¹±­Ô\x0014f¿òªlÂ\x001aOÈZi«Ñ_.§f¥\x001dÛpSÖn\x001bÍJk\YwO×Ñ»ÓtzsÜ¹wfÌÙ*Ït¦MÛö°?ÿõ¯},\x0000\x0000\x0000\x0010\x0008(tj(ªBËL¯~é®Ì\x0015Ä\x0012%%¸ÂtÁúª\x001fïæÔ¸ôµS\x00129\x001a÷i¹,ðNò¯;à\x000bm4Î3Û¶ß&¬íØ~­0T:ã¤ÐµÛwttv±B¤U×Ôð(9[öJ+\x000c½å\x0016²¸\x001bnøú
7Ü@\x000b$u¤Ölw¼5¤\þjÞ½é%-oÊ\x000bù¸ñã:\x0002­¢
´	W\x0012^ægîÑ2!H\x0007d/Æ²mOoê?\x001cy)kõ2·ÀÝ¤\x0017é¤4+\x001dvzs\ ·W mÎs¿<?·wvÑÉªÚ¾÷Z> Ð\x0000\x00008 Ð©¡¨
Í\x001eXáúD\x000e]¨çuuÆ57E×¹µm\ò"ô¬µKã>\x0015ZÕG*MI÷´Ó\x001a\x001d¶m\?sÃÈ!Ý¶¶=R£3Z¡ùé\x001c\x0014\x001d]Ý?¼õVZéh\x000e2g&hYÊÿøÚëTÂeÓSÐZ®Fk	Ú
7Wo¥çëP¡u[Z+»àµz\x0015ùçï±¾J÷xCn\6rÛ0\x0015*hs)ç¦ä`u'¥5c\x0013k'åÛõÍ1É¿·VXÙeò9çÏ]ÝÄæ¼Bÿ5\x001f±\x0005\x0000\x0000\x0000\x0002\x0001N
+4\x0018ÌÈ/\x0015Êc¢ùIÑü°h~^4ÿü7Ã
gE\x001co°A_\x0001ØüÃQ]SËª_²\x000e;½Ãr
øðÙá3µyÇ>öçÏ>û,ö±\x0000\x0000\x0000@  Ð©\x0001
]Vh¶Z´´¸´aÔ\x001fVèÐo­ÝF
=áÑ1\x001e~çåtÈ	¢µ%¯Ðå#ö±\x0000\x0000\x0000@  Ð©\x0001
]n\x0018\x0016m+ÒÚ¥Mòé¸\x001fÞz+)tèÍk¶m¯èÿéâðnë3"§iËÎýõGìc\x0001\x0000\x0000@Vèl[×ëï.þÚ»N¼8ÿýÆ\x000bÙØÅ²|B!VÖ"mÕi\x0010\x0017ÆIá3\x0005\x0006\x0000ä\x0012Z¡wì;B¼sÿÑsM\x0017­Ì~ëCZ;sÞ{§êcwË2\x0001
]¶ø\x0011i0HÐçH\x0014þyÆ>\x0016\x0000\x0000\x0000\x0008DhÞ¶§$ùØó¶k_]°ì¹I¡gÌYtäTCìzY\x000e@¡Ë\x001c[W\x000f\x0012[¶þIÊ?ÏØÇ\x0002\x0000\x0000\x0000(B\x0013$Ï9~}á¾Ã§b7ÌÔ\x0003\x0006=þD\x001a\x000c\x0006èdA¡\x0001\x0000 ¹\x0004RhRâ\x0017æ.vÉ~oå&®ùÇw>zéÍ÷Ï5]Üuàèóo,&þäÐñØ%3Ý@¡~jt"Ý\x000f\x000br Ð\x0000\x0000\\x0002)ôÛËÖ±\x0018Û¢-z×Ác3æ,ÒvMÛÆ.é&
­©°BýâIÝ¯´\x0014	þ\x0019í®HÄîüäMmåó\x0010n×ü{7t^ÿÆzPa¶\x0002\x0006àÿ³w®ÑRTçº^òó}ÆØ{=Î8çGDwLv¶\x0017¼\x001bMbF#hT\x0014IÔ\x0008\x0002\x001asTî"\x0017\x0005\x0005\x0015/ÜD®\x0011QPA\x0011E\x0005ET6Æ ¢\x0008bPCäÒ\x00054B8ßêõå[sVUW_««Ö;Ç3zTÏ5oUÐOkV5!é¥TôÈ°½âÉ\x0013\x001e~J^^¼ÜÙu÷Cs¨Ðµ&
mÿ:\x0011ÆÏ,V±B\x0008¤ý)ÆÄ»Tg\x0002ç=þØ+=|\x001bÂáåM£ó\x0015â(t.ÿ\x000fB\x0008!3eùo\x000eúð_nXWSª«ÐÏ½²Zð-Z¢B\x000b+Ö¬=ïÒ\x001e5ª<
mI*
]]\x0017/\x0003ûßi$A®|\x001a©Ð\x0010ÒøÔÁ«®ÐÏ.])\x001b¾ES¡Áw:uÓÑ5ª¼ê
m=GÌ\x0001¾\x0001ÿ\x0007"9zãdÚ]zHÝ¶VLu8\x000b9Ð%$Ä«µNa\x0004\x001eÑ´\x001d=Öï¶?"Í´ýAÒ\x0019Ã±ØFòjçM÷úÇ\x0006¶½:EÎÔ©FwX°\x0002i'Yò\x0005ä8®¨M;'Å¿H¢'ÖQèÀ>ÛaúgD÷j\x000fn\x0007N¾V\x001b8¶\x001b¢ëX0À\x000b¯T¨Ð\x0010R\x000bêàÏÕUèÇ\x0016.uî.|ýw°«B\x000f©³ça[6"\x0002¹²·vj>¬X³¶¤C¤c5í[=\x0015Úê\x001fÊØà*|&Ð|\x0002·õ\x000fëZ­´jã(´Ó|¤B;fè\x001f«ÈÖà¬0±¶\x0016fqN\x0014Z,pGàÞÀð)
h¾³íw/B¡dÞ/\x0013­Ð\x0011\x0013k\x0015:pm[òjí\x0014»ì±öEô÷¼Qhg\x0006l\x0019§E;èyÄW*ThB\x0008©\x0005©ShAo-|ûý±®£¹\x001a
ýNgÉçJrB×ZSmJUèZSO¶ù0
\x001bóÂJï*¢VÐ\Q¶²|©-Z¡US\x0003õõÕÈ_HàäèDÅQh_§­»íPh\x001bd\x000eì°v/Z¡\x0003/\x0006g6"\x0014:zbmW\x0003'Ùº±3\x001cíÓíR\x0015Úqã\x0016µÃÑc	\x0015\x0010BjA\x001a\x0015ZÙðÉgUThùpQ7¶
-Û¸)RÖ¾UßvÞj\x0001G³åp©\x0013»T5\x0007±\x00192¯»Ð\x0013)`ßÚcý¾Yÿwº§õhÈ=E
Ýä¥0\x000f	Thû7q¤
mÿ"\x0014_¡\x0003µÃ÷Gä\x001b¦ã¸«oqÖ?íâ\x0001$ëa{ã(´4¬{5Uèèµ]
d;öÀ?g\x0004~#hª@¡µXÞµ\x0018qáôï+O&ÚP7Îµì\x0003¬ÐÍm_UhÙ¶ò©6«z¬b½Os8¶Z«¼ªñªÇ¢\x00154§m+wZ\x0014P=Vs¤0jö»§Ã)ïÃÆBû\x001a\x000e<°)F\x0014ÚJZ©QhÀ\x0011Õ4
í\x0010¶7uQè®F_6vÞ\x0002g»©JQè°i\x000cÀ\x000b¯T¨Ð\x0010R\x000b\x0018v\x0014\x001aò¬
­ÚluZ\x0015\x001a9N(\x0018a^\x0001º«Ý¶58\x001aÜì-äÐ|«ÐplÛ\x0019y\x001bØ=Ä®Ë¥ª+´Úÿ¯Ðí8â\x0017G¡\x001dW±qÚ¢k¡í\x001d^iWS\x0007*tØ±þ¦KsýC\x0016\x001b[ÏÄ³Ôü!çÛ¯\x001föm9po åÚùKv£j#\x001a­Ðvý³Ý\x000e¼H¢'Ö_\x000bíL2î»ô/6í¶=³¾\x001bGL¾£Ðº-%µ\x0015'ô\x001dgb\x0003Ï]\x001c¨Ð\x0010R\x000b¨Ð¾Öj¤ÐµI%V\x0003\x0015ÚÑà\x0008¶
Ù(·]\x0004b»êt8p°
\x0012¶\x000fÍÐ]BÛòÑ
\x000fSè|û¥\x000b¾ôÚ[ÆÛÇìßÓ5\x0012XV\x001d¦ÐÇú3`Gä¬9q*±¾\x0007ykj{\x0014\x000eS×\x0000XÇÓÎY\x0008ÜëO²ÞNhgÏ\x001f£í­¶©BÛX\x000e¼HN¬ÿÂÈ\x000eÙ_È5áÎøÝ\x000e|§6jWeø¡i»ÆÃ¹U6bThB\x0008I
*´¯¸ðØø\x000b95Ïþ\x001a\x000f­\x001fo¥Æ«uéu´B;\x000bK°#PèwD÷ÊEW]¡I¨äaË¥\x0012½þÄ
M\x0008!µ n
½{O\x001e4¾B7\x0017\x0002¼a·\x00136Õ\x0017ðU])gÐ9·\x0001Úúq ¿\x0003·\x0010ú
µ\x0019ÈÑ>èîìíhËÞêhWYk\x0019¨xàÝThR\x0014*t\x001a¡B\x0013BH-`\x0014ºnT²\x0002ÙGo\x0018löÄ»¦P¡;2Tè4B&Z@®\x001bÕUèf\x0013^®zÍ\x0011P¡	I\x0017Th=÷\x001eXýÖ'}-èÖkä¿¾úã\x001d»÷'ÞOmê¨ÐûÛ("i¥*ôÓKþ\x001b¿´òÀÌy-\¸*g\x001b*4!é
M²Ä;÷M{d¥xò·.\x0018:zÑ¤\x0019+æ-|oö\x0013oMýãÊIS^»ëþÅ7
{UïéÝ{Í2\x0013§¿¶£9xIVéÀçÛ¼sÏ0\x0006>õEQheì´Ç?Ü´5qÉÌ6ThBÒ\x0005\x0015dÝù¬~ë\x0013\x0011ã¡c^|úÅõÏ/ûxÁ\x001f>þôÚ?>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/7.Creer_des_r%C3%A9unions_priv%C3%A9es_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/7.Creer_des_r%C3%A9unions_priv%C3%A9es_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=u]w[ç§ÅHhfÒf|±\x0011UÏÄt0üY×ÓÖõ¼öoÇ\x000f@\x001d@Ý¶î'¹¶0í´\x001a_x~\x001dSD6¯ëáâÂ\x001d½ u?Ûð¼×ay~>÷g³Û¿ô1spR§\x001eüé®r>ûqyÎóÂüÑW×äÌblkÿ¸Ö¢\x001e<Ò¿¿ê'¹T|qvR__Ï\x001d>f7¸¶±[:k²{ðî§U;ÚÛ,L;,Ï\x001c?êÕesù?}-V\x001a\x001dêÁSêýÕiV\x000f·\x0013+sn»é»õ¬v³eÂ\x0017¥\x000eÊçWÔ¿Pý\^óéø\x0007óûõ¬w³'°üVÒÃzðW=5kG»\x001bá@=wø8}ñLá«\x000bÏÑó§Q)d[ùîøQËG\x001d>á½£z«\x000bÏÑ××ùñÞfÿøyòøRÏ.µ|ôáSivon_ûâÔ»é6«Euüø&>¾FÔ³Ë=·Ü=ª_ruáy÷ÇOruÎe3\x001aF\x001e\x001f>f7\x0014Kç+
v3^ÒÓë'¼\x000eó£ãG
g«sv)±Sªµ9|ð\x0012uü´k¥ÄÒìñ<Ò\x001fÎk_råFå\x0017Ý^w.Ê¹Íµûñí5:fRwW<[¬¶xváe½Ûn«ZÌ¨Ûë½ilôÏécÑw×73\x0006Òã¹~{=\x001f=}\sáÍýòEá\x0001no:\x0017'ûa¿Ëú0~úÓ'¸ÊW]\x000e\x001f\x000c Þ^ÍJ>µ\x001eôØ\x001fÆÏ¨Áô^OÃ3¦\x000f\x0006êÝ^µÏ\x000e³ñÐ´Ãd\x0018ýc9'|¿~Ú)ééóÚ?\x0010?²þø9ÚùôëÌù~üÜ-çåÏ»Çç\x001dòÁ@==~ö+¿<lgµ-þÕýr£ËrÆ@jü4Ê¹ÇÛùþáõ%wJ>\x0018¢wÛm\x001el­\x0005\x001eçcs\x0007"[<¼0ÚÎ­j>\x0015wÛ÷ù\x00186ÏüzªPåá!úù\x0014ÒëAÝhø#\x001f»'\x0018M\x0017É\x0007Ãè|ÎéèÓ|¦ÑLñ|0DïöZå\x0006§ä³\x0010Óù\\x000f\x0006Rù´U>±gòi\x000f\x0006ÓùÔ\x000e³±\x0005ïã|¼\x000b±ìa|0\x0004ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001ò\x0000ù@| @>\x0010 \x001f\x0008\x000f\x0004È\x0007\x0002ä\x0003\x0001òÀóùL-Ä2EòÁ0\x0003ò9#\x001f\x000c¡ó9+fb\x000bSOò	FU>­+òÁ@*Ê'ú4\x001fO0.VÉ\x0007Côn¯T>éhðq>6Ïüzº@>\x0018FçSÕùx\x001eò\x00195ÚÜÈV¾B>\x0018¢O>\x0015÷Ø\x001eò\x0019·ºæÖ¾\x001c6»äz·Ýf%¿µ\x0016pÛ£\x000fùLúW7såF÷|0Hï¦Û8Ímý.ëø\x001fùY³ËÉ½\x000eù` ÞMçâd/¹òÓrÏ»Ñ1óÄÌ¯vÎ/¯o_û÷áv{}y~ô-±43a\x001e{ÈÇäþðÛ×ßkíkÆ\x000f\x0006èÝ^·k¿ýíÃ´CåÓ¯çÝÁh
FÓ*O/\x000c¤s«ZHGSöû\x001e?Fkîßì}_!m\x0018Íû`1Ò°Lv(\x000cE%Ô \x0011]\x001adb¼\x0015ßÿ+ì}\x000fZ½<Û_\ÇW¸ßyW\x0010¶3ð\x001ehútnÑrþA\x0012³ÇKy½ðv>Ë)ã\x0007ü\x0001Vº«ßÆÓ¶\x001aæÓGÙÎxü¤+-h/à
&ãÜ\x0012ÒÇÓg:~(\x000f*Ð^À\x001bL\x001e\x001dñ&Åy¨çé£´\x0017as\x001e¢öjC{\x0001+u×ÙÓFh¶\x0016ôQÚë\x0017]\x001f`\x0015(|ºM?ö*Ýõ¤Ï´½ÜÁD¾\x000eã\x0019X\x0005\x000e\x001f©^H\x0004ÝKÝ5û½ö|±4Ä\x000f°\x0012\x0014>r³ùö¬îR~/\x001d\x001aÏ¡D\x0001â\x0007XÁ,|\x001cc7ëÿ®ùx¶Òóø\x0001WLÆÊòÉÄüôÒpg\x0019ÇOþw»7\x0002}WLÆ£^»O<Jø,é3=ö/÷\x0003¨/à%¨º\x0006\x001d±ÌGYÚJhTËö(ñ¯ÀÙU\x0015Õ\x0017ø\x0003,£TW«ã·ëUøL/Ã\x001bNæßÉ0%°=r»VHE¼\x000eË·k¦Jk$¾èe±.õFà\x000fð\x000c²gÔnK|Ôï$ZÕk}p}éÍûð4S\x0016¥>ø\x0003<íéßBæ4à¶õ¯«KñGêk	Æ³x\x000fþ\x0000s\x0014{:ÊU<Äì¢êz¹ë°:¼Üy®Ò\x0000\x00193{ª¹DØ»g#þZ]óïËHÒ?Ã	äÔÃÿ\x0017\x0008´éL&ãaÿ¾Q½NFXüÛ×µ8L$ÍF\x00129Adä\x000f\x0004Ð3\x0019#{dI¬äG¬sÛ´bøÌýÑèÍÛN6|~U®ßu\x0007¸À@ ÍekÐmß
W\x0008ë¢ÌzÍ\x001böü÷
Ígä\x000fýgµV\x0007\x0015\x0018\x0008´±`y\x001e½N«VÊÆÃ¬\x0013Û³jø<Ígä\x000fI{C§|¡*¶»}\x0010hCÊÓï¶Åj?
yéíwíùc"\x001dÌa4+×¬\x0008\x000c\x00026\x0007tí±",5kå\*\x0016`öHÓûöÌü1ZwÝþH<¯Ô[X \x00116\x0008+\x0004l\x0002cìÎ\x0008ÉsßªW
éxÄïÞµ}È\x001e¼¶Ô:ÂB9½Áh"sS©7¥N\x000f\x001bôð\x001d\x0002ÖÇÇ\x0007äÎ ×õêM6\x0019
zv\x000b¡SÄ©?Zt¸}\,-\x0008µÆÔûýápx\x0000Ö\x0017|àápÐ;Ò]£V¹É¦N8ÛA
ZõÖ·ØóT`\x0016füÜI2/Ukb\x0013)ÔíÊr\x000fXgdYîv¤vK¬WKùLò$ìghÊjüXq-ø\x0002Èdµc¢ñl¾(üªÝf\x000bq\x0007¬'ø¸Íx[û%\x0014óÙËó\x0018çg;6\x001c=±G)0FGmvÚÃ\x0006"±xÏ^\x0017¥² TõE\x0010Ê¥bá:Ë§â±HõÐH\x001eB£ç3ö(\x0001´¥Öè	³r¸\x0018ö;'/.y>
¬/<y<?\x001dq¾}BòèÑêùTô<\x0007Z«#L\x0016Òîp¹÷Ù@\x000bGu&\x0012áB\x0003Öëq9ì¤Ååù|ô,\x0008¤ÑéA6jÇA»~¸\x0019f\x001fXg\x0018ÆãvÑ\x001dÊfAÁ£Óüoyf\x0002)\x0011¤'æïV\x001b¹MÙ\x0011;ÀzKm6ëw³\x0011¹ç\x001fä\x000b3\x0008)d \x0008£	Xw\x0004a@êàÜùWyf\x0006á\x000cR©Õ\x001a\x0016X4\x001aµZõEî<\x0019S\x0008[\x0004¬9ÊñÁ¿ÈEàÍ\x0001\x0000\x0000ørþ\x00080\x0000rúÊ
endstream
endobj
80 0 obj
<</BitsPerComponent 8/ColorSpace 156 0 R/Filter/FlateDecode/Height 257/Length 168/Name/X/SMask 79 0 R/Subtype/Image/Type/XObject/Width 575>>stream
HìÁ\x0001
\x0000\x0000\x0000Â ÷Om\x000f\x0007\x0014\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000À	0\x0000A]\x0000\x0001
endstream
endobj
81 0 obj
<</BitsPerComponent 8/ColorSpace/DeviceGray/DecodeParms<</BitsPerComponent 8/Colors 1/Columns 528>>/Filter/FlateDecode/Height 232/Length 27471/Name/X/Subtype/Image/Type/XObject/Width 528>>stream
HìWysN\x0012­\x0003\x0004KÜâ\x0016B\x0008¡ËvTú%Ùïÿ¡öõ\x000cH²×É¦\x0012y×©¢ÿé×Ýoúx÷®^zé¥^zé¥^zé¥^zé¥^zé¥^zé¥^zé¥^zé¥^zé¥^zé¥^zy#rCòÿ\x0006ñr2ïo¶óæ$¯®èäïõÔ\x0011n\x001f9òïµ³ÅÞÊk\x0002\x0006áp8ë÷¶²Mkß\x0000öñ?W²ó)­
#á\x001bóJ.\x0006ï£± GÃ«8ª#ò[a\x0004ð}cØ_ú\x0003F¼\x0011l¿*,F(N"7âU¬ UcQeI\x001c\x000f_Ã¹¶á<ðøíÜÂ} Nè0zmB\9C"9¢j:¦©S\x0005Ñ"+®o\x0006Ü%HShR\x0015qüÛ~º9ÕµÛÁp,\x0010o#C\x0000Ðx¢h¡MeYQuCWeq4xMhWÏ\x0014#Y3m×#q\x001dÇ\x0015¯ábº=jÚmªð	±`Ä\x0002è0\x0015Eþ£lsE¹¹\x001da»®mê>s<×Òåß5ô\x00175^9CRdÝ\x000eâ4Ë²4Mâ8{\x0012¯ê\x001aSÓ	\x0002ß1\x0014ñ÷Îg%\x0007¹ÂpH·eWÏÊ¿\x0006n0tg\x001eÇkÍl/#ßR'£×Æ2¤\x0008¹Z\x0018MT;ÌWëz]­Êr¹,\x0016)ÌÐ¤îÎýâ\x001cúâ²'C,K\x000f ^\x0014Í]Î§òóÓºa0dÕMU$4:"2e½ãÓ^ÆÕ}zaÕ\x000b;\x0000ë§S3)(³ ],Ò¹çøQVä±§KãÁzë%`?ØCÞ\x0018ÒT%g\éFÒ²áçëÝa¿k@j½^WËtn\x0010ÔCÜ\¡Ï1^ »\x001cWÏè\x000e±MMÜxî\x0018Fo¹·'Ãù>6³Ýv¾j× T\x0008]ÉEQRt\x000b\x0015\x000eIy4x\x0019ÁS\x0015Ý)«Ø\x0001ÓvóLÛÅqÏÍ¾pÇÅÒ¡¨ÚQQUE\x001cøaº¬Vy`*\x0002ùñ©\x0017».p?ÅõîÉ¦\x0017q\x0011\x001d\x0014}fÛ3M\x0016¯Ràon\x0006bEåöîþn¿Y¯VÕºnÍ*[*%aDÛAtÐ\x0006õì»³#ÙÀÊåTÉÚ1vÈX¶º\x0007Ë8°uÔ#Ö\x0000\x000cÃK\x0005­\x001bH)¶ÑR¾\x000e¥BÖq\x0006ebMdªµ¥£=mOzà¤oC6\x0008v'3\x001f\x000fØ«ñÉÄ5\x001c×ùåÙì\x0001{8!kñ\x000f\x0006£æ¦«M]fá<^Tº\x0008­)1ÿb\x0015\x000bd«bÔ\x0001\x001b°ïüo\x0017ýnÏ\x00053¬\x0011©#:\x0018\x000e\x0012nà\©O¡\x00147uêððplª"Ï\x0017Ëj³Û5UæØ#ò\x0014æ&IbõzÐÞPòÝÅÿ\x0011ó1XE¾ÙCcì±"/ö¨t@?\x0013Vn\x0017V\x0015p³[¥x	M­\x001ev$)ªáY¹Zf¥M\x0015¤
\x0017ùA\x0008pÖÕ¦Înþà\x001a$úF«º\x0007ç\x0011}ïL\x001c<Å5n[×çfwÿùvÂJºUÛ¦Êã0YÖÛ¦mÜ«ÿpãIÄÁ\x0008 t\x000bF­\x001b(\x0015\x0017\x0010@±ð\x0004\x0017\x000eu'Ze\x001e:<_\x000f¢ê¤õñánWåÑ<\x0008Aëf¿!\x000ezJ\x0000¢IÔ M¢¦Ì\x0007\x001cîM\x000cª"·FÈSUcÃêD`á b:>½±\x0003\x001b\x0015Ö¸¦\x001f0\x0013 üK
\x001ftÕ)SÀ<,Ê\x0018J
CÇØ6\x00193o²°Ê0-7ZÔ»Ã®\x0002!tUç|\x0002:ê	\x0002Ö¯4\x00188\x000eß\x0014<¶'3m¬þ`2¤wÜDh\x00130´t¸Ð¨L\x0010¢\x00117%ZÀ\x0002BÙ4¨\x000c?v"ÕÞz·]/â(-7»f\x00057NÆÕ¦\x001a?Mb\x0014È àe¸\x00084¡oAðÚÇ±Mð\x0002ÀiqÁäÉ\x0004@TàþÖ\x000bä¡kL¶\x000fnV\x001fî\x000f8\x0013]±åE\x000bj&ê\x001c	\x0002Nf¨9t¦O©cÍ¿\x0014&ô2"Ë¸µãº\x0008ÑõvH<(ôxë±·8\x000bÉÝ	â\x000cÝVäÍTyBÕ\x001f\x000b°Âó}\x000fÚS±\x000f§Ñ;\x0017\x001b8"CâÏ¢>>~|¨\x0012oFôð<ÇÔ\x0010å³®\x000eÁ`Ìª+×\x0010à8ÛÍØÉ¾ËF(rò¤5\x0011\x0008ÈDb\x0007Ü´\x000bÛ<5*ü^Àlv×±@Ó'lªsdØ­ÊòÔ\x000cÀÝºHbâÃ¶Jpqq[Zü4\x0012o&¤ið1mÁv8¾\x0003¡ñâ×\x0001óÈ3ä-î.n
;ISUÝ/6wGËÇ^1N|@zH=\x0013ä3½¸Ü\x001e\x000fM\x0011ÚtýP\x0014h<wtÂíçÎ_4xÛ2uÍ°¼0Iéæ;æ
\x0008\x0006k\x00160Æ¦QàÂYª>óÂ´(W«"\x0003!4\x0005É²Q7	=KcÁ5Ë#Ð;ßÖI\x001a?	8Ò|Y\x001f?|ùçóûm\x0001þZn0{¶i[H\x0017zÕ\x0016\x0001Æë\x0013iÈ!i\x001ca\x0014ã!c#\x0014ÅY¶&ÒVB; Û~\x0018'Irð¶1E u·m\x000càÌaôP?Ë°<K×(@àCÍøÐì·Uêê¸ûX\x0015Òª\x0004ÞÔè\x0005SÑ\x0002ê0¤Ç,'ü\x00061.Së\x0018^ÀâîºÀåÌLËO«ãÇ/?\x001cÊ\x0008	âª|@©7\x0014Í
æxÄ£gÍ\x001c?Î(«r'\x0003TtÇC8NEÅTD8\x000c\x0010\x0015'@3]¯WÅi0á£WV®ù[×2gH\x000eyYÕu½.\x0017±o Q¼(«VØ^4\x0002(*\x0016\x0016r­E\x001a:¦:Õ¬ ÅI\x0018ÊrUïÞþöýëÇÃ*	\\x000fõ\x0007L²m7$]uu\x0000Ô]¦\x0001m2úd|-E±Ä\x000bP\x0019iCÎ2]")Ó¶HPÈÀ[4(Kz.±­Zæ¡kj\x001ab\x00110["³-?NÞHòeÙ9h6sÂb³¿ägj:éX°U@}ä\x0008©`À\x0008×-:¸Æ3Á4\x0019J:ßÃ\x000bHÆÌÿ:\«e\x001e\x0005\x0017.Ï_¿~º_§6\x0019]\x000fÀA| tAêÒ\x0002È /38\x0006õ:Hó,rÑ\x0000àö\x0001a¾7OWÍáxØVÈÑ)\x001a··Ôj'ÕîTS-âÀu<\x001aÀêM\x0003ÙT\x0005b	²\x0015õn¿ß6\x001bz¡\x0006)iàû	\x0008?m65\x000etgðDºÚ\x001eï\x000e»Íºª6ûÇ/ßÿõíÓ±Jç>1§ \x0004a\x0006]w ä\x00088#CÒ°#\x0005Ûýáx.Øí¦Êç\x0014|\x0016\x0019¦¬¡±\x0000Ù\x0005\x0016æU³Ûm7leC\x0010p3\x0010÷<ö\x000c",½H±Ô¹!§8 ®1Tx®\x0017_ò\x0001]\x000e\x001a\x0013YI°®mÔ¥åÛ\x001dp\x001d\x0000\x0003kÖEìT	\x0002ø6áÃ
\x000et\x001c\x001c]ow´\x000c@÷hZ·ï¿|ûöå¡¾"\x001f¼¬>ÞíY½ñT/À\x0007L0\x0003Ó'¸P\x0011¬U\x001ey¶ã'ÅªÌÙT¦Ö\x001cE8Â¸hîÞ?Þ£%
ùíD¯)\x0019AÑÜ?>`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=yõñ'OØñ³\x0013öq:áçsá\x0010ÌhÎ</p><p>ÇÙv9üüÝL'óo\x000c»ü4\x0008v¹Ì­àÊtf_<N~NØóÓ\x00136º­V\x0017²bÇ§á\x000caUn\x001d³ÞäÂ2)dn5³Eîeë¤ÄÆ\x0011i¨»ª\CWëÅåR\x001aölÃ\x000e\x001fé\x0012«xî-sþb¿öI\x000eÂ9í\x0005Í1Åè)J¸\agìå4Då¹±L\x00149×­\x0012NCÝU-ìèaµ¤äÅ0¨\x000b9KüUdÖà¬#ëÂ¤5JÑÑ}_±\x0016*D</p><p>ò\x0005S\x0005'?\x0018\x0001it"®ujdni¨½¦QMZ7\x0017ý\x001e %"¦ «) ±åØ(wÔO/!`¿2@ê°\x001d,hà##qPtã\x0001áeOxëIÝ{É\x001e´D7:¤±þ$Ë ÏÓªZWËsöv~¼©ªÍúýüìÏ\x000fËùëÅåêfQ­67ó7·¿TÄz±ÙTËmë6ëÅ\x001d\x001c</p><p>áö]}|\x0006á^(&`\x0016 èì.fÀW\x000c(\x0010*wÀñÙ6ÓÊy\x0015Ã\x0019\x001fa±Ç
F\x0007Vx\x0001ÍÎÊ·à³÷ììéäùÙ0RÔ}%\x0016tËH¬ÀÂA`Mª8Øö¾\x0002¿Í^/¶ÕÌd«rõa¹e³#É³¿ñ£³Û\x001b°3±;ÔÐßB
Å\x0005\x0005j±ý<SQbàâ\x000eyM\x000bã\x0008\x0000å2/,[SØ³¹R5C\x0018N5Þæ¶ØQÎHJ#Ci|Ý0$\x0002¢ai/#\x0005ÍOG%</p><p>«µ.r½c`µ6¨¦fh+(Ö¥½j*\x001eE«\x0013#</p><p>sÝ0¢¬i¯¤G:*Qe_o¬¾NÚÎ#·Á\x001cµ\x0007¯ãg¡¸\x00118\x0005#Ci«\x001a\x0004Jø\x00146,÷L@¼"FHdªvä¨sÔÿ®\x001arÔBßÇSaþá=?qkWgxºwB»G¤"\x0019Û*vÙÉ9KÙR0*\Ú®7Ö
£vVÇ\x001d}\x001bã7\x0006è\x0019¬kÌ­[Æß9¾ç¬®#;~nß8¾\x0007\x001eÚ\x0018+%©H\x0008\x0015Ñï\x0003¶	\x0019#M;vú=\x001bi¨\x0010±\x000fH*®\x0018¡\x0003¶Å\x0012joÁB¾8¹^!³}¼]þ\x0011ÒÝ</p><p>	¤\x001d©ð\x00118\x001f6·ô¤h³ÅÅÅª¼"ráÀ³õâÓGìrKys<å\x0014ßJ\x001b
³íks
\x0016ìbyó\x000fÄ©¶KFz/YE"c¨ºC<·×ÈHM\x0011a_ºBå\x0002\x0011dÒ¨ó$ïñSt>ßn~(Hµ"0ÒøÈIU?Gà\x0005XH[\x0007\x0004g¤\x0008\x000ecP\x0004HX\x001a+ Ý\x0001q#Tl(ë\x0010\x0003ê\x0008mQìÒ¹¦É\x0001@öz0Yå\x0012\x000cgãða*LF9Z×ÎHhªÍAiº\x001bByr'u0á\x0016x46¾\x0008×\x0015ÝÇ\x0018EUÎ
Ýf0\x0014\x001b£h²ÌQÓÆy\k\x0013	OÙn)xØ\x001d3\x001d(}m¬ÍÇ(RÃÚh+%,DÕçaª¾TNÒæüesD?\x001aV4yçç&d\x000eÔ7 MYl\x0014¯h\x001d¥xµÔ9	&\x0011ÐËà:ÉN</p><p>³¢\x0001lgÿ»±ëQ¨¨NO¿C±\x0004\x001a\x0004ª[4®@\x0017¶¸)hÈZ\x000bHq(©L¢&\x0014l¸¿`cT,"ÃÂÁ,P\x0016&\x0010É</p><p>Jø^¸Å°cÃaÎE\x0001Êw\x0014°\x0007ûJÔ\x0001<Öêr	cÒL¢8§Vd</p><p>\x0005]\x0010	¤Jv\x00083Qî
\x0008ã¯	û\x0010\x0001¸JãèfJÜÓ\x0008\x001c\x001a. (jKS°1&ÓTë7FÑ:Ð4Xæá\x0001Ú×¶sÇÑ+ZEdTN\x0018\x000c¡T!!AI#©â¦È½h(X!ª\x0018háC­)\x0007Ôx6\x0011\x000eLö\x0004¥w\x001fêëH\x0013~áiDªH\x001bÂ¬÷©)\x001fTOTàºE\x0007ùÒ6$x:>Ë~±üÂÎ"¾Ì\÷räÁ~½JètºÝXHä(O\x000fJ¦÷bUsÙ¿;o|i£\x0017cê`£7<´ï\x0010KU$9\x0004¥&§ø\x0004Ùa</p><p>D"×iôlÝèu¬¼nÑÉ\x0007s\x001a­\x001a&\x001d[¦èÙ¨mÁÆ¢É=Û·ÝÒñYcÓ\x000f»\x000eïaa&B|\x000fz\x000eUõB|u!,Ñm ÔÊQõðµuý§ÅíouU¹ØÆºùÎr^È¨ì«\x0007U\x0011Rc_wÙâÍìb\x0003±d¶^UK(ö\x0007¤
\x001fïf\x000c¤\x000ft+7ôóaí¶Ú/yÀ\x0013\x000fy\x001côð¡Öí«\x0012ì¿!-nªå
´<;\x000fN`3U%\-¾«S\x0011õc#êÑPsy\x000eªMmxiPÊSZ\x001e\x001dª\x000eÿ,ÝÜ=Øï/£&||Ý ÍýMÖ{ð\x000cG\x001a®êö4D]\x001dÞ5îÒÿ\x001e:¬øÔy:;²dLÃ·gg[tx\x001e®Æ'¬ê²í]V¬»kt(\x001f\x001c©yÁõ¬ÿó\x0012ÔÁÑA< ÇíZ\x0004ð\x0010¥\x0010ìa\x0001F7y</p><p>endstream</p><p>endobj</p><p>154 0 obj</p><p><</Type/XObject/Subtype/Image/Width 961/Height 525/ColorSpace/DeviceRGB/BitsPerComponent 8/Interpolate false/Filter/FlateDecode/Length 42787>></p><p>stream</p><p>xìk\x001cÕçÛ\x001eGElÄ~\x001cÇÆ:Öcì
olìÃþàYÏ~°\x00070ö\x0018\x00023¬Ãj\x0004\x000cBB\x0002ô@G\x0012\x001e#Ç6\x0016\x0002\x000bÀ $a#@\x0012\x0002!d	½¥ZÝz¢7­÷³[ýÐ£ÔïVËôª£>¾ùÎÊªìÌúøEGÖÍ7oVòþêêdVOOoO@\x001e=9räøÙ³ç\x0006Ý°pöî=´~ýæ\x0017³\x0011¶yùò\x0015:åËWÛ®4ééÊÊQLT»£6	Zp/,\x001eÙl»-ôöþôÕÖîtªÀP\x0005ªvôè)÷jV¬sSAÛqgò¤_\x0011Ô2ýöôoýtÃè\x000f±|ùªE>¸»ò>ÏÝ½úÊë'Nö\x0010ÜYøî{;wîqzIP¨W¥éÌoóûHÊ­ÐAQeQÊ×¬^/å´\x001cºçNí'¡Cüå¿ýÊ\x001fþð²S\x0005þÀDø¹}áù\x0017yaÿþOçÏûó·Þ]¸pÉ%\x001fîÙsÀiÃÓßË

Í/·¹·O\x001aþç<ã¹\B\x000büoÜÏU(ÜÅPv4~Üc¶«¨\úãÌÉ÷¼gØÏûyrÙÑ`ï-m>õý£Q}6¢mmðRÔÑL`ß¾îu¨BTÂ\x0010bï7þÀ\x0003ãIót	ÉÉÂK#ÙK{{8\x00151aÂßüæQ£&èB*\x0017¾G:\x0016:</p><p>\x0017ø`CððÃ\x000fèL\þÌDnÑôÁ\x0018;ví*:L9ô¡*|_.ª\Jvºò°B{JõõÍT*\x0007½²E¨ÐÃîe×5Ð{qjÜS¡Éý÷ÍIEÈR´\x0019/CCûÒ\x0016j¼Â¨\x0014Ú³ÛÅSh}\x0008´,_\x0013´6ëò 8µ\x001fù[TJÈÇ>2Ñ¥|`|~ný </p><p>]]][S³ÃÏ&¬Ðî¬[·¾ÃÊ?mú'/ÿliA_\x0001¨\x001aUvj'ÜÅ!O¦¯Ò¶«æÏ_0aüã^GSèÙÕ/\x000fµ-È{\x000b\x000eCQGO±ÊåËW\x001b5½ä¹¸\x0008\x0015º¾¾IÏïi®©Ù\x0019­NKãÖ\x0005Ò¤iÓ~\x001fÉ^¶l©Õ¼téJ*$¶Uhª\Ô³Y A\x0015:vf¢µh²VÛ)èÈñäY´ËÅÇÿ,t+[</p><p>M\x0001ÚÖJ¶°Yhúú cñàTh\x0012HíÆK&\x001d</p><p>í§\x001b¶_Ã,Ò¶C</p><p>í2ÿ¬ß±Á¯Ð<íì>ÕÌ\x0013Ô<)íT'ôÅ0ëãë¶×QhnÏV¿\x0016p"\x001a</p><p>\x001d¢zbV\x000fÖ<|³gF«Ð\x000f<@Òõ±w\x001a§h,º\x0018f]à#ÄL¦OÉ¿BSå¢Í\x0002ùéÏÿÕåAâÏL\x0016]Ôÿ\x0019ÑpNû¾øJ5Ú\x0013\x000fDóç/p¿@Q\x0005\x0001Ë\x0016\x001anF>ðí¼1A«<½Ý?õõÍdÎÔ,ý¥ek\x0005?_\x0013²\x0001\x0015ZR\x0002¸P'\x001b\x0018/³ý&)"3ºf¶ÎP«a>ú¥No\x0010¶íQßi\x0002ÖÚm+N\x0007\x0012´Ü\x001d'Uv\x0011rò@ÙD¿!¶èÒ¾>|Ý\x000e-ó.Þ¢\x000f?üËÿö+üÍÐ¡?rÛ:c\x001f(\x000eL\x000bT_ZãéeÛf¥qYEÕ}\x0019\x001f\x0018?Ûlÿü¼Nw±~´B\x001f<Xg{:¶oß][³âì\x000eQè\x0006¡\x000cgRñ	¹@\x0015¨Ó\q¶0®\x001cv¯Ë,´SÂE¡·ÍîOðø¼ÂÄ×ª¯K¯Ô¤\x0012©iÝ<_¹zÙ×¶µÄPÔÑS\x0006q=åeLEÈAê%\x0016Í{g¦¿E:4ë\x0002/GbìÃö¯ÐT¹ð=Ò»gÛ¸@f\x001b®åïÜ|WÝ(°3\x001aúl¬^½Á\x0013²è\x0008?6.ð×\x0002w´|ùj</p><p>]ìYqÏçfÚÎÜj¨$À\x0001$ó-´*\x0004jÜøi¿#Å¥¿¶ìBä</p><p>-:A!zæ>\x000b­%\x0015%;0+\x0005ÆPhNaÕmjU\x0016	¤\x001dérÛîéú.*ëg\x0016Úz !ÊÝÑ=túFàÒs:XyC¬©ãNïí[Äëy~§·HLmiAmë*\x001b©V95«\x001b</p><p>Æ¾¬\x001f\x0018?[ýÖéo=ü
ËE¡W®\#¹Ð«j¤­;öí=ÈË§NËúSèlÞ¢éß ËzZE\x0015\ü9[p.´S¶\x0006ùóìY¯¹o>P¡sª:|ÿd9O\x000e\x000fÈô8úþ²êë\x000e|Ý`«gÉZçÍ?Wôh[K\x0012E\x001d=IÄ$Å\x0019iª\x0010Iæ§ \x0016MzÀù¥ûsBOþò¼yo\x0017¾Ò+tñr¡ï\x0019\x0011 {üÅN_:£¹x1ÛÔtÁ½{\x000fB>}®ð}ùIäX¸pi$3Ãú\x0003I\x000bãÆM¦\x0012ú«\x000bt\x001bÆåâÃS:î\x0017¨Êa÷ºd\x001eÚân­!Ò9<³5Âu¦ÀD\x000e\x0017³²*´1Ìbæ>1ët#¡5AÚ6Ê
\x0015×\x0013¶\x0006~\x0014Úz !ÊàCs\x0003wÙ\¾°"êùÏöÞ"~\x000fé¥þ^ãù óÀ<3ì^\x0017è\x0012GÚ,æ¬g­\x0008B\x001bûÒ\x001f[]MÏÕëMD¡5\x001f¯\»µz;×Ü°Á¼\øTèl>#.8¶²J~®E¡/Ùü\x0005va1 \x0012·Tëy`D10£l6g°ThÎ÷\x000eL½8ºìIÞÊvsëw­%¢dúÿâmÓ/©\x0002Uv¿lÑ,Åðç\x001e/&M"Wâ
LO"Ç	\x0013\x0002Õ/Ò\x001f\x0004Ì9*îÉë±ç\x0007cìØIÜª?Ô&\x001fÑ\x001d]¡ëëiÈpùÏSZE\x0015¢ø
¡ÐÖ{\x0006mSDl¿\x000e\x0014ïvÂ@</p><p>­\x001bÑæ8aÍÄÆµïùQhÈÕ¶NGa­àt !Ê³ýy\x0005.o¾>pk\x000bìç,~¼`d»´ïô\x0016e-Y\x001fN</p><p>M\x000e,i\x0015Z¡uöS\x001dR_a^ j2l»`(´é¡\x000f¶Ø</p><p>M¼,/ðT³f« í_¡³y_µýo/§rÐ\x0017Co]0þñùó\x0017Ð2ßE(ÏíñÚüs\x0011U³¾ì·÷h®+´9ëë,½ÖÍÊÑ¶(:zò\x0018]_ßäTV\x0015);-ºx\x0002æ®Ð´w÷\x0003÷íí\x000b\x0016¼G\x0016m}4Ç ¿0¨B÷\x000c\x0002Ö{òß"écé2\x0011M«¨B$ôFfNÔçÂØ\x0015:ÿ¿Q2OÛ	\x0016*¤UÉÒVJ0\x000bm"bûØ\x0010\x000fµ£Ã¤¡Ó³'\x0011ÎBëf­\x0016­ÿëÜxidD\x0018ÿ_ï9\x000bíB³ÐÆñ:uÏå@XùxÆ]K {û.-snû,4'!ËK[vªÃ\x001a<öTåYÄØi\x0013ÁE¡ãMB|à![Y¥B?	`\\x000c\x0019ºî«ó3@øYvTB{÷aÑ\x000e\x001c¶÷\x0015\x0006^\x0014\x0002\x0014Ú³µDQì\x0001tÚ´ß;Ýõ¯o*,\x001cy¸\u|â®Ð¼¯ÂÝÏx¨\x001d+´`LGGòP»âåBPèX-:rÖGdkÑÀ\x001cÕÁ&B¡³yA0þqcª^RaÐ\x001b	È\x0015ÚóA\x0017øf]²²ypôÌ±dB+´¼Ô¨þv#µÃåFBnPôFç¯:uï·þ\x001eªìG¡­\x0007\x0012¢Ü¶ek!\x001dî¶ûQðñê·Â¸ûÒv\x0013yÃm\x001bób{¢es¨LNë¤Ð¶uXôiÞÊv\x0013æ</p><p>.</p><p>íòùJ¡W®\#\x001bêçBoØ°Y9P.t6¯¯2AÃßù¸ô*\x0017</p><p>¼\x0018ºàÃ¢+r:Ý~,\x000c(ìÏ^¶^ûÍ
é¶µ$Qì\x0001=yÜ¸ÉÆÝXä	T\x0018á3µüÌfG8ãí©Ð³gÏä\x0012ÆD´\x0013QMA\x000f\hM1\x001e¨âI}}c1üY¾ªÐç'8ó'Úÿ7IB\x001f÷\x0018	³\x000cÁ´@/©0¨¯2+t!¸<\x001eD
BéóHT$ÛZ V¬_òq[¾Q5FÌhÙúØ:½­ç,´îç}y.%N\x0007\x0012¢Ü@\x001fQYx>ÌYß\x0012¨Ý©}#\x001dÝX«o»ÓËÒ\x0019½¹<\x001fÃI¡êp¹ís9l7ñ£ÐÖ\x000fÏÏm ^øî\x0012¹p÷®½zw7×ð\x00139\x000e\x001e<
\x000bÍSÍ|ç }eæïÎüa´ª¨¹ÐxY´QKçPâ:Ì|8*ÌUs^ÛÍ­Ò\x001bmk¡Ø\x0003hOÞ¢\x0017.\Jz0räøgNÐ\x0002Ýóæ½\x001dá3iù\x0016B\x0016\x0012[x¯ðä</p><p>ÃI\x0014:÷1çE\x0010sæüÙÝ©B	Îc\x0004z"Aäõö¤©é\x0002YtñÚç\x0014òsüs<Ñ>¢YÿàyoùWÀ´Öéw^"ÄÏU§yï®¼oñâ\x000f8µ#Ä|¯à2ñ\x001bî\x001cIÇÝZ­\x0018wü¹Ü\x0000\x0008ä~`ø÷èú ï\x001cä{\x000cù°ço<\x0015~1to\x000fý\x0002B±\x0007Pí\x000côQ$O h!ò\x001ft Å"\x001fpñL÷\x001cÔ\x0010~Âó±Ö\x0005\=B?q\x001eä)ÐÂ\x001dA\x000b</p><p>Çó_\x0004­-Á\x0017\x0013ÿ×¢E> ÑÁåá¨>)ås¡\x0013APvº\x0010\x0000?$ú\x0003CrB×\x001fk^\x0019\x0015úy4PT\x0017C\x0014b\x001fèOÚÛ»È§OiøðÑ\x0004-ÐËHòKC\x001fø\x0006) öK\x001cH´Ò\x0000 p1,7b\x001faA\x0000.Ob¿Ä\x0001\x0000@iÀÅ°Ü}\x0005e\x0002\x0014º<ý\x0012\x0007\x0000\x0000¥\x0001\x0017Ãr#ö\x0011\x0016	Pèò$öK\x001c\x0000\x0000\x0006\\x000cËØGXP&@¡ËØ/q\x0000\x0000P\x001ap1,7b\x001faA\x0000.OÚÚ:c¿Ê\x0001\x0000@±¡k\x001d.eç\x0019\x0007 * ÐåIW×ÕØ/t\x0000\x0000PlèZaYáyÆ\x0001</p><p>(tÙB×\x0019L¿\x0000\x0000Ò</p><p>]ß|Ú\x0014.éÀÿ\x0019\x0007 \x0012 Ð\x0000\x0000\x0000\x0000\x0000\x0000\x0004\x0002</p><p>
\x0000\x0000\x0000\x0000\x0000@  Ð\x0000\x0000\x0000\x0000\x0000\x0000\x0004\x0002</p><p>
\x0000\x0000\x0000\x0000\x0000@ H¡w"\x0010\x0008\x0004\x0002@ \x0010\x0008ßA</p><p>ÝÖÙ\x0003R@\x001f\x0002HldþËÿ\x0002\x0000\x0000  Ð©!n\x0005@ \x0010á#ö±\x0000\x0000\x0000@ î\x001b6"v÷\x0003\x0010·\x0002 \x0010ð\x0011ûX\x0000\x0000\x0000 \x0010wÞ\x0017»ûH[\x0001\x0010\x0008Dø},\x0000\x0000\x0000\x0010\x0008(tj[\x0001\x0010\x0008Dø},\x0000\x0000\x0000\x0010ûï\x0019\x0019»ûH[\x0001\x0010\x0008Dø},\x0000\x0000\x0000\x0010\x0008ÜN\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002</p><p>\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004bÄ¨1±»\x001f¸\x0015\x0000@ØÇ\x0002\x0000\x0000\x0000øÎÍwÅî~ \x0012âV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002</p><p>\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002</p><p>\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004\x0002</p><p>\x001aâV\x0000\x0004\x0002\x0011>b\x001f\x000b\x0000\x0000\x0000\x0004â¾\x0007FÇî~ \x0012âV\x0000\x0004¢LãröÊc¿üíÝ\x000f>¾wÿ§¡\x001b},\x0000\x0000\x0000\x0010\x0008<Ô.5D¨\x0004\x0008\x0004ÂÌ]ðÞÍwÜK\x001cÿdèFb\x001f\x000b\x0000\x0000 r¾ô½¡_¼ëî/\x0019W1iJÅSS+¦>û;i</p><p>P9­½à¢Ð¯Î÷¶a£ö×\x001dç+ÖVÑK*¤åÿÍ\x001fhYÐõ\x0019Þ7ah«Ñ*z9bÜd½/Ý o«[so\x0010@¡\x0011\x0018ãØÉ3wÞóð­wXôÁÐÄ>\x0016\x0000\x0000@d|õ[óå´ÙIS¨&Õ¿ÏÁñTh[m¹¢ÐR®ÅEþòZ-ºâÌÔ\x00027%rÎ/EÔy[ªfh¶S`(ô\x001bo-ZWµµH\x001c?¥H-S\x001c?y>ZFç§>;SvZÔ½#\x0010}Ph\x0000@ZøÒ÷ÿÙ<\x000f\x0014iÚ*ö\x0007Å]¡ISEnyêØI¡y~X¬X¤Ú:WÌHSNÕ¬</p><p>íT\x0013D¨Ð=W¯~oè]O<õ¬K\x001d\x0016N^r9-\x0017I5In©qRôb4Þç¥Ð´_ëZ\x0004"Ú},\x0000\x0000Âùâ]w\x0007g\x0005m\x001b{ÿ\x0003á®ÐäÉä±d­<9¬\x0015Z\x000cKØu^®&j-ÕbÈìÞ¶{]\x00183á«\x0008\x0015úöÊ1ßþþí\x001d].uX8ÙY/Å¢\x0013\x001a³Ð\x0008KàvB\x0000\x0000 ¾X9"´?_·èÊ\x0011±\x001f<g¡Y¤	r]YhmÈÚ«ÛòÓ×¢Á"Ì2k­\x0015k²ZÛ&rX\x001b\x0004\x0011*ôã¿úÝýÿØÜrÑ½Vè¾|\x0003Ï\x000fÓ\x0002ig_¿WëIiZà\x0012Ze\x00188×áyf7´J+®ÔÆi§Ö=º¬\x000eKOx*Ë\x001eûBó\x001e¹Ãzïz­ìß\x0001Ýÿ¤¿@x\x0006n'\x0004\x0000Bæ\x0013:\x0017í©ÐbÅmý9\x0018.</p><p>-\x001b\x001a\x0013Ë"ÌÆ}TS'QksvQè6»¼\x0011P \x0006L6üyç\x00035
\x0016o\x0014ÖÂÙ7p:W|ÕPhúË¹\x0002sSüR\x0014Z»´4ËêÛg7,«¸W¢ú¶</p><p>Í¬Ü}v</p><p>m»w[Ã¡¿ÊN}àvB\x0000@ËÂ¤äE{*´\x0016f\x0017[\x0008y-o¨o!d©ÖÉÌÒÔ÷Thk \x0012÷öÿüß¾åÇû|(4Ï9Kê²Æl«Ðìº2+½z\x0013*\x0014¿íSîª\x0015ÝªÐz²Zºg«Ðâð\hUh½wcþ\ïÂÈ\x0015µ\x0008KD~mÿÆ·oÜ¸e[Ww75Þp¾iì¿M}¸\x0001\x0000¤¯~+ðý^w\x0017Fø\x001dÐeðRö</p><p>]\x0015£=p?</p><p>­
Öö¡vÛ¬KÚÔÝF\x001diMÏ$ë\x0006Ù±\x0006©ÐÚ`ìÖ:¨(dø^°xÙúÊßoªÞî§²g"Gºå°ÏBs\x0018\x000fìÕûa«ÐÚuû¼\x0014Zf¼=\x0015\x000bThÜ~\x0008\x0014\x000fjõ
gÎ5ülÄx\x001a5æ.xv1zâ¯â\x001fj\x0001\x0000©#÷üºPª<uãFÆº*÷¤»(ú6|ôãr÷öh\x000f\x001c?­\x001a</p><p>\x001cÁé£E\x0016½÷@gM§Û	E¡¦sûT"\x0007×\x0014e\x0011N^%/
)uJäðThª!ýdE7\x00129¬ÍúIäÐ	Õ}\x0003¿M R\x001fÈqË÷¿ÿÑªÐD{aeîÛí\x001dÿ,%\x001f}¼þÐác±\x000fµ \x0010M-±÷aP±ô/k57ön\x0000ÐSÐ.</p><p>¨{õ
t¥Kâ±£=p(tj(Ü\x0004&Oñåÿñ\x000f²WÜ«\x0019</p><p>RÎÞ¨o\x000cÉg¹P§m°RnP§Hû·\x0013º+´nY·`Ø¯Üx¨ï\x001cä]\x001b_\x0019nS·\x0013JoyrÛz;!\:õ\x0011ûíÿtÛÝÚ=û?%gÖ%<\x0015cT\x0003]{\x000fÞT3ô~és\x0012¹iD²_Z[Èq"ñ¥ï

°á¦ÐSð·\x000bo¯\x001cS«\x001f\x0014:5D"\x0003ô1ûßÿøãH\x001a\x000cQ¼\x0007Ó\x0019)(r\x000ey¨Ý®=ûC7\x0012ú\x001a>öß¦]½Úk$i46µ¼øÇ7}Èå\x0018dëêÏ\x0016HL·ZÁüà$è8ä\x0003ï©ÐÿÑ\x001cPèÔ\x0010zìÖÁ?­òôï_¤µØ\x0003</p><p>HJ»\x0012[ý8qêì;KëüüAÚË¿Ü76öA\x0007\x0008Æ<3\x0014\x0011$/\x0019W$¦£êäíc"¿0\x0003N\x0011ñ
þ\x0008\x0004¢Ð\x0008qõ¾éö{Ú;:mç*É³WZõ±ô/kN­/Æ \x0002Bc(´¼¤sÊ</p><p>)¡Ó'sÔ:\x0016\x0008®,´¹Tµz_¶[éµº\x001d®ÆzOeÙÚî?\x001f\x0002×Ã
/\x000b¼¡Þ¯µo¼ë¾sõüó\x0001Q\x00114\x0011ZÎ§BG\x000eÍ¹Ð×®]ûÉÏ\x001föØ\x000f\x001f\x001e»ûHt<G \x0010%\x0010WïSgÎ­Z·Ùv\x0015©ró'Nýé=\x000fó\x00139®^íôôs±¶@£µÌPÓpÑ³BÓ&zY¶âÊì·\H\x000bÒ¬íV¡²ÒÕ¾~}ÕI&º)ªÃåôWwF\x001f\x001c£´@mÊ1\x001ao\x001c5m%/kõ¿Ðyã p*Z,~jjáÝ+ê\x00139\x000c\x0019\x0012»ûH(ù@ "\x0010Wo§,\x000eæ¦ÛïÙ½÷ UèË?\x0017úÿñBìC-0Ð¹Ðâ
²XºÌBë\G\x0014ÚiÛv+c³ÙôÚv@v¡7´\x001eÑ7kSÆ&Æ]Ü¸îµ\x001b øQhù^¡3ýÏ¦Ë ]\x0015£=ö\x001füà\x0007±»\x001fÒ
ö\x0008\x0004"ê\x0008w\x0001'hïè4Æÿ3ä®×U]Î¶^»vMÚ§TxïC¿}À\x0005¸"-sJÆ\x0002$9\x0014®ÐR!BË\±K\x00072>\x0014ZÏ«\x001b\x0015tS|ì2§mücá\x000eDò/\x0008\x0014D\x000e9M±$r\x0014\x000fäB§HÆq\x0004\x0002\x0011K¾`\im\x0013~fú,2ç¦æ\x000bÏ½<çn»~?û7¾}ãÃOLÝ½÷ íhÍêØÇ\x001dÀ=\x0013j¶Ö}\x0016ÚBËQødiÖ:Ì!¶Ï²3f¡Aø¹P.tqÝNX$ Ð©!Q\x001f@D\x0014\ÆüõówÞû\x0008-üË}cÉ?úx½Óm,Øs\x0017¼\x0017ûÐ\x00032\x0003õR\x0012uò0¿ä¿¢}ê>;wÖùÏÆ²u+]"»öTh¥,ËF\x0006Î6nE4ÞÌÀo\x0013rÔz/Ò
ý¯\x0006:\x001d#~\x001ej'\x0017º@</p><p>\x001dáCíôDÊÊÊØÝ\x000fDBé\x0007}\x0004\x0002\x0011UDr=_¹vÓc'ÝG5\x001bª³WZc\x001fvAÆî¡v¢ òÁ°&xøÎ8?Ãºu­ÏYhéTÐ\x001bêÃ1n]´Uh§ú²\x0017½¼KÈ\x0011§V³\x0013Z¡£úiâ=ã¦nÝý@$D3#\x00108"ëùSg=gGOüU_L??\x0007Ò\x0007Ü\x0015d\x001cÒ¡åâ\x0016R¡#J.ê\x00139 Ð©¡$ã<\x0002(JDr=ßwððål«\x001fð\x001b+ \x0012 Ðøü,r¦6£ê^ñÈqÿý÷ÛúXK¶ãtcöØ¹`Ð\x0002F R\x0013±\x000f\x0000\x0000</p><p>
r|õ[A`ÅIS¨ÍøË\x000bÛÛ	\x001b.´ÆîÀ\x0013(4Â|:®´¶\x001d:| \x0005j>OPìc\x0001\x0000\x0000æKßÿç\x0008\x0015Zýü`UèlGìr\x0008ü\x0000F8EÉ4²lãàá£­­münÓ\x0002½ô¿­í)},\x0000\x0000Bðóh\x000e?Dø bcUhäo$\x0005(4Â\x001aÅF\x0004\x0007O>[ßyÏéh#Íc\x001f\x000b\x0000\x0000 @¾X9¢P®\x001c\x0011ûQøÇªÐ±!ð	\x0014\x001a¡Ã¶ý\x0015QXèÉgkðt´T\x000e$Ò±\x0005\x0000\x0000P8ÌE'hþB'\x0017(4\x0003¶\È^i=TwÔÏé jTÙ©\x001d'},\x0000\x0000HÈåE\x0007½»pÒ¤ä?k ÐÉ\x0005</p><p>ð#Ï×\x0010\x0005ÇÁ:·Égkä¦£ëê\x0016<E:ö±\x0000\x0000\x0000"ã«ßÊ=éÎHO{~]\x0012¿a\x0005</p><p>\ Ðe\x001e.ò¬å­×!®"|Ä¥K}N>[6¼t9Ëï¶­NC¡\x0001\x0000éæKß\x001búÅ»îþÂq9~jjÎéï¤)TBåQýþ`\\x0014¨ÐN4nÜ~pÉªê?}°X¸¢jmÍ¾\x0003Ç\x001bb×Ër\x0000</p><p>]Îá.ÏNªÜ\x0008\x0012\x0007>=\x001chòÙ\x001a´ùOÐ;¯Ï­HÇ>\x0016\x0000\x0000\x0000\x0008DhÞºçÈì·>þÚ»¶¼8ÿý7ï]2Ó
\x0014ºÃÉYÒ>óý8bDN´¶èØÇ\x0002\x0000\x0000\x0000\x0008¡Ðu§ç,\ÁªüÚ;Ë×ÖìÛwô\x001c¯:t¢qËîºùKV?÷úBZ;ëÏK÷\x001d9\x0017»j¦\x0015(tÙÕõä3üy¶h\x0011éØÇ\x0002\x0000\x0000\x0000\x0008ªÐû5ðä3éñ'ªfÿé5Tí¹ïíúôtì¶J Ðå\x0019.þÌÙ\x001aqw\x0010á\x001d|¦´EÇ>\x0016\x0000\x0000\x0000\x0008DP¿d5ñ\x001bW\x001e9Óâéx+6í¤Ê¤Ü~* @¡Ë3l\x0015ý¹§§§»»;î\x000e"¼N\x0013,±h(4\x0000\x0000$@</p><p>½qûAXö¯Äo}¸6Y¶n[ìÂ> Ðå\x0019îþÜÕÕ\x0015w\x0007\x0011ÞA§É°èØÇ\x0002\x0000\x0000\x0000È)tGÆÓ®­õ¯yÔ¡MþøÎòØ3}@¡Ë0üý¹³³3î>"¼N\x0013[´dtÄ>\x0016\x0000\x0000\x0000\x0008D YhÎÞ¶ïX Ó{ùOK{}aìÂ> Ðå\x0016î)\x001cìÏíííqw\x0013á\x001dtØ¢e":ö±\x0000\x0000\x0000@ \x0002)ô¬?/%Þ~àD Óã­b\x0017ÎAÅ;G¼ðÚ;\x00056\x0002.·0\x0014ÚHá %ëèèhk+è9ÆÒ\x0004&:YtÊ$#ö±\x0000\x0000\x0000@ \x0002)4?dcÅ¦þ5ïÐF¾£°\x0010WÔ\x001dþËúmb¡D1üv¡w\x0004F\x000cp&%kooomm»\x0008ï ÓD'NLDÇ>\x0016\x0000\x0000\x0000\x0008\x0004)tkG·ÆÅÙÖlÝË³ó¯yïþeSÐôi[.ÜX\x0014¤ëðÉ³5\x001c¬Þu\x0000$-;÷3wì«Ú¾·jÛMµl¬Ù½~ë®u[v¬Ù¼}õ¦Ú\x0012\x0018 ¢ÀX»yÛî\x0003ummm2\x0011\x001dûX\x0000\x0000\x0000 \x0010A\x001fjÇéÐ?ÞâÇñX¹\x0003=ÁÃL¿B\x0013c~ñk|¦\x0005\x0016ÈEùXø%ñß¿s3°lÓK^ ¿´,m\x0012òR61ö(KMj:`Ô\x0017¨Öê½S\x000b2[.æÌSèF·­ÐäÏ'Ï5võ\íé½\x0006H÷Õ^Nbgw\x000fÑÞÙÕÖÑÙÚÞmm»½ráÒåæ\x000b\x0017J`\x0002£±¹eÝ±O\x000e\x001eèØÇ\x0002\x0000\x0000\x0000\x0008ªÐÔ!%&1³pÅþc
NÕÈ¬ª¦jÏ½¾0èíî</p><p>M</p><p>Ê6+</p><p>-Ì¦*	\x001eTÈ¾jUh­ßlÂå¼Gô6Ô]ÏS!À´w*ýtQhÙ$Ü¼zP®ùä ü9Ñ\x0018</p><p>ÝÑÕÍ</p><p>}¥­ýòÖ³-\x0017/55·À\x0000\x0011\x0005\x0006¦¦\x000bëªwH.Gìc\x0001\x0000\x0000@øï}GÎñ\x001d/¾ù¾uíÎ'Ic1U9o	ÿ4!Y4¹ô+\x000bmÝs¤p6f¡éoFYhÆb¤Vf
ÖöK/uf5ïQ´Yë´Ê>Øv\x0014Z\x00129B'u\x0004Uèê]\x0007b@P\x0008¶</p><p>ÝÚÞq¥µ-§Ð¹)èÎ</p><p>]¾é®û\x001e\x0019>ú1Í\x001dÃGO}vf¤zð\x000e:Mt²ÖlÞÆæèîî},\x0000\x0000\x0000\x0010\x0008RèöÎ\x001e\x001fyÛ¬\x000cXµå\x0017ç¿ÏË$É¼@Ì³héÚZÉßø¤îxõû«·\x0016¢ÐÚµ¾Ö²Ùf|(´4¥+sÎ\x0006Ûl\x0006</p><p>
\x0006\x001fâÏ¢ÐF\x0016GSËóMÍN\x001fuU[ÉÂã§EO6½P)D\x0004	:Mt²ÖTA¡\x0001\x0000 ©\x0004úi\x0015Åç-Y5sþ\x0012bÎ¢\x000bWTmÙ]g»\x0015\x0019õ\x001bWÒ&\x001b·\x001f\x000c§Ðl¹,½Ú¥µ*ë\x001c	I·\x0010qD\x000eíÀ´ÖÈ[Î¸&r¸+´tOf¼õÔ·ô7Ôi!²Ë2\x0014ºñPèÈÊ\x001a\x001a>\x0000N</p><p>½héÑ\x0013	.eÐi¢µ\x001a</p><p>
\x0000\x0000%D"\x00071Éjöçþô\x0001§jøäÐFRnÚ<¨B\x000b2iÌúÊÎÌ«Äå^?ã~CG-
ê</p><p>Ò~ÆõvBw¶ÞiÈ%ôuýØÀÛ	e</p><p>\x001a</p><p>
\ÐY\x001cVæDèÆæ </p><p>ýüì7îºïÊQÞ6lÔs/¿îþ\x0011&§Íð#%½\x0007ê¨Wq÷"@Ði¢µºª\x001f\x0010ÝÕÕ\x0015ûX\x0000\x0000\x0000 \x0010y¾ªñ\x0014Ú#gZ8gã­\x000f×Û>jã­\x000f×½²à#§Ígýyi Çâ%å\x0019\x001dÅ\x0003</p><p>]VØ(tÿ½Ùþ{	s</p><p>}¾Ñé\x0003`«Ð\x0012o¼µè\x0017Suùü|ó»C\x0017,^&Ëd­\x001f¹Eò\x0014ú|cN¡7A¡\x0001\x0000 ©ÜÿýAg¡«v~:cÎ¢uµû*ÌY´\x001cÛÖ®y\x0016zÞ{«bwÝ"Bâà¢Ð×\x001fÇ¿°Þ·BoªÞvïCOÈKOÎ\x000cbGMB×C¡\x0001\x0000 áL0¡­£[S¸Ú­«Ù£^g]õÎG\x001biÕ­{cwÝ\x0014\x0000.+"Whã¥§Bß^9®\x0018Æäóäi3øJòÍï\x000eåRY^¦Uø±`ñ2.ä\x0005Æh¡</p><p>¶u\x0008jÐhû¦w¡·âÖ2)ÿ\x0004</p><p>
\x0000\x0000I'§ÐÁs¡=á\x001f%|eÁ²Ú½Çd:úí6púGìò\x000e ÐeU¡Bçh×Ô\<îSvÊ\x0019\x001d¤Ó"¥$±\±(4`s5ÚPJè%\x0015êidi\x0016¸Í¹¯_³Yãy\x0013^\x00163·¶ÌÝ¦\x0006Iä\x0014º©y\x0015\x0014\x001a\x0000\x0000\x0012K\x0014Ø´ó\x0010ÿ¡<¸cæü%´pèDcìò\x000e Ðe\x001f>SèóN\x001f\x0000qæyo¿7ééé«ÖWÑK*0å></p><p>ÍÁ¾*ÓÑr1aËÍX\x0014ºOåNs1áÌÒQ</p><p>-fÎ\x0013Î~\x0007¦ríÕ²,\x0006îÔò ÊÜîË)ôùó9®immB\x0003\x0000@\x0012)B3u§÷\x001c>KÌ{o\x0015»ôM;cÏt\x0000.+~Ý;B÷öö>üÄSw\x000c\x001f}Û°QwÞûÐî½\x0007ú(t_¿åÊÜoòÞBó4²L\x000bË¬²\x000e#'DO2-ûQhkË\x0019(4\x0000\x0000¨)¶Bk®­}îõo´!vùL\x0007Pè²"BîS\x0016½}÷^.qWhÑ×/¥Zb3j\x0016Z¼7Ó¯Ð_Á	\x001b}\x0003õ_öå'öÈÛö
Ôf-ð²/Û3Ph\x0000\x0000\x0000QSJ&\x000e\x001co¨;Ý\x001c»|¦\x0003(tYáS¡Ï5øRè¾¼EïØ½O^º+4)¨¾MOn'%Fº2dÔ4i°dÝ\x001aoÈ·\x0004</p><p>}*Ãv\x0016Úi_Ö3O¡é4A¡\x0001\x0000 ÑäÈ\x0011ø×	Á`\x0000</p><p>]VD®ÐF\x0004Jä<$ÇCî(Lk@¡\x0001\x0000 éx\x0016\x001aD\x0008\x0014º¬(\¡ÛÚ;\x001ezüWdÑNcGê\x0001Â^Î\x000c¾yãh\x0003</p><p>
\x0000\x0000I'¯ÐÁ~\x0010\x000c\x0012 ÐeEá</p><p>=ÈC'r¤Ûû Ð\x0000\x0000|0\x000b\ ÐeEê\x0015º¬\x0002</p><p>
\x0000\x0000I\x0014ºµ£Gsº1\x001b»\x001c\x0002?Ä¥Ð·þèG\x0015\x0015\x0015±+e\x0008vìÚM=7ÿÍ\x0008ÛüÝÐ
Ò\x0002½äe(t\x0002</p><p>
\x0000\x0000IÇ:\x000bÝí]\x000e\x001f­Ð_ÿú7*T<öø\x0013ºt4v%\x000eJZ\x0015zsõV}¦J`\x0002\x0003</p><p>
\x0000\x0000IÇªÐDÃÖØý\x0010xR\x0002&xü9rù,=PhÄ 	(4\x0000\x0000$\x001d[æ¹hdt\x000crJ©ÐZ>
i´NSó²Lbó|5¿Ô[qãÜ2È­m\x000b\x0000k½dÃç°\x001e¬ås\x000bôW6±~SúúðÃ´\x001a//ÛV3:ÉGd[ßI¡u\x001fÞ;ÏV¡ÈB\x0003\x0000@ÒqRh8<GíB\x0014Ú*R\x001d\x0005ÍÐ0g®À^ÊúªeXì+h-7ZpRhÞP¤TÑûÕséT7á</p><p>Ü\x0007®`mÖÐu'6Þ.ëb\x001c>/ØÖwRhîd÷ÕÞ¹óæÓ2\x0014:Ñ\x0001\x0006\x0000¤\x0003N
£v¹ÐVÖÉõY/µøÑlhª^</p><p>âÕÖ\x0016\x0014Z\x001cÛðpë\x0017\x0001§D\x000eiûcô6¦Ð\x0014ÚVõ®
½·­o«ÐÜ1Iäàh(tr\x0003</p><p>
\x0000\x0000I\x0007</p><p>\x001a<GíBf¡µÎãéÌ\x0004à¤Ð²,Ò«3\x00198B(t%|*´î¿»Bë½\x0018÷Q\x001a</p><p>­¿w\x0018®.ù!ú]µÖ·Uhë\x001be«Ð\x001c%0@D\x0001\x0006\x0000¤\x0003N
£v</p><p>-*ë4\x000bmmC¡e®µb`fu×\x0014ZÏB»\x001fÓÄ²\x001f¶}Oô»¡ç­³Ð\x0002W£\x001d9Õ÷3\x000bít;!YÙM7ß\\x0002\x0003D\x0014\x0018Ph\x0000\x0000H:PèÔà9j\x0017~;¡1\x000bm­ã®Ð²ªb`ò¾cÎ½</p><p>ç¤eñUCéuþ³^66wWhÝ\x0019Ãù/\x0014ZD\x000e}»%Upªï\x000bMË¬ÐÛvì\x000c\x000bÝÔr¡rÔ£ÿ1cðÿþuìÔggFä\x0008_\x0001\x0006\x0000¤\x0003N
£v¹ÐN\x001aiMEpQhÞÖ4Ö{±Þ¾§[Ô\x000b~^\x0002ÍaÌ\x0012÷¨,\x0008«Nóä&D[Ö[gÝy­$¨Èû`(´ÎÄ\x001eÚÖ×
òVìÞ$Ïº\x001bµÛwSèã'Ï\x000c\x001fý.\x00199~Êè¿<mzoooA^ð\x001dPh\x0000\x0000H:PèÔà9jã\x0007¾\x0013Má¿NxäØIçÊQÞ6l\x0014-\x0010\x000f=ñTwOÏ3Ï½üà£¿¼ûÁ¿úl¤p\x000c(4\x0000\x0000$\x001d(tjð\x001cµ¡Ð¦p~ã­E/½ö¦¼<~òÌ\x001dÃGßûÐ\x0013dÑ\BjÝÖÞáò\x0011Z°x\:ö\x001e¨ó-\x00083 Ð\x0000\x0000t Ð©ÁsÔB'b(ôðÑ½ùÎ\x0012±hw<m\x0006]1xüùß\x001dêß\x0018©>mK\x0006ît\x0007\x0014\x001a\x0000\x0000\x000e\x0014:5xÚPèD\x0013¹B÷öö>:å×dÑwÝ÷\x0008ßNè®Ð\x0019Ì<G\x0017Ph\x0000\x0000H:PèÔà9jC¡\x0013Mä</p><p>­Ë9\x000bÚE¡\x0017,^æ4íLå|1<m\x0006ð2\x0017Þ^9F</p><p>ÅÀMè/Á\x001fãt\x0004\x0014\x001a\x0000\x0000\x000e\x0014:5xÚPèD38\x0015\x000cYÌ*ðrf NsþF¦_¡i\x0013Éè M¨}»¬¦¸¡Ð\x0000\x0000t Ð©ÁsÔB'Á©Ð\x0019¥¾RG\x0017ò\x000c³.4.A´\x0015UÉê2	(4\x0000\x0000$\x001d(tjð\x001cµ¡Ð&^îsÈÎ¨Ô\x000b'f=Î(6\x001aBC¡\x0001\x0000 q@¡Sç¨
N4±+´~"G_>\x0007£Ï9S5øA\x001cbÎÈ!ÂÌ%Ph(4\x0000\x0000$\x000e(tjð\x001cµ¡Ð¦¨</p><p>}ç½\x000f
\x001fýØS¿éþ\x0003r`F=¡ÎövBÛBëí¼C¡¡Ð\x0000\x00008 Ð©ÁsÔB'\x0012ÌBG\x00152»70D@¡\x0001\x0000 é@¡Sç¨
N4+tíÎ=#ÆN\x001a7iÁÈñSÖUmÐ\x000f3Ph¯B\x0003\x0000@ÒqQèWç¿{Û°QûëóKZ^±¶J¯b¸Â¿ÿæ\x000fR"åºÔ¤F¤D\x001a\x0004PhàNá</p><p>]²È@¡½\x0002</p><p>
\x0000\x0000IÇS¡É
ÖjÍ>,Í«t\x000b#ÆM6Õæl]\x000bBã9jC¡\x0013M\x0014\x001aá\x0019Ph\x0000\x0000H:î</p><p>ÍsËl¼²@ÞK«¤\x001a½\x0014ÍöThmL>\x0017	ÏQ\x001b</p><p>h|*týy(t\x0002N\x0013\x0014\x001a\x0000\x0000\x0012»B³-³\x0006[]!\x0016O¶*´älfKÊÌ]Hð\x001cµ¡Ð\x0006</p><p>¦B\x0003\x0000@ÒñTè¶~g\x000e§ÐN©\x001aWÂñ\x001cµ¡ÐF+4[4\x0014:¹\x0001\x0006\x0000¤ãG¡Ii(<CcäQ\x0002ñ\x001cµ¡ÐÆB7æ\x0014º±\x0004\x0006(0è45æ\x0014º¶­­</p><p>
\x0000\x0000IÄB·å=9ªÛ	¦¬AxÚPèDcUè</p><p>ÝB</p><p>ÝÜ\x0002NDä\x0014º¹e5\x0014\x001a\x0000\x0000\x0012OÖ\x001cmv\x000fµ³µbã¡v´9·i»-B\x0003\x0017 Ði</p><p>(4\x0000\x0000$\x001dü´Jjð\x001cµ¡ÐÆE¡³¬Ð\x0017/5@¡\x0010
Ph\x0000\x0000H8PèÔà9jC¡\x0013BwuB·¶wd[Û>WèÆ¦\x0012\x0018 ¢À ÓSè*(4\x0000\x0000$\x0015(tjð\x001cµ¡ÐIÇE¡/e¯\¸x©©å\x0002\x0014:\x0011A§NÖêªmíííÝÝÝ±\x0005\x0000\x0000\x0000\x0002\x0001N
£6\x0014:éx(ô¥Ëdeç{{¯@\x0002\x0011¡N\x0010&:Yk Ð\x0000\x0000X Ð©ÁsàB'\x001dã×UH¡Û;»H¡¯´¶åî(¼t¹9G!éÙÕÞÞ\x0012¨ "DÐ©¡\x0013D§NÖÍPh\x0000\x0000H*PèÔà9vC¡\x0007\x0015\x0015\x0015\x0015A7±Uè\x0001\x000få¸x©)\x000e}®áüsçN>sâÔ©c'N\x001e=vüðÑcuGÖ\x001d>ò)QwøÐuê\x000e}</p><p>"ÞÌü»Jo/½ÉôVÓ\x001bNo;½ùt</p><p>èDÐé B§&ÅÑÜB'kíæí\x0008ÝÓÓ\x0013ûX\x0000\x0000\x0000 \x0010PèÔ\x00006Ø±k7iêc?\x0011BnoýÑÚ7jöòõ¯#ÐVZ¡·íØI-<:ñ1Rè	N¤åª-Õ\x0017.]\x001e2d\x0008-×o<[ßpúì¹9>},úø	r¹#GÔ\x001d&Ö°ïBPïçá¼9\x001fÉË3½íÇsþ|N\x0004\x000e:)tjÎ757_¸@'kí\x001dPh\x0000\x0000H"PèÔ\x0010¹BàòKrÑ\x0010\x0013§12oþ!dÅ[ä6/NÓ^\x0002\x0019>w\x0015ú¹ó¨?¼õVQèÍ[ª/^Î~ík7ÐòÚõ\x001bÄ¢O9³è§Èå±K\x001f?³;2j\x0010)ü®æÞÞã'è­¦7Þvzóé\x0014hæ)h:Yëò</p><p>ÝÝÝ
\x0006\x0000Ä\x0001N
ERh\x0011ÈÄ)tT[ì\x0019é 1î(lïìº®ÐÕ[ù¦Âë\x0019ÑMlÑgÎÕ³Hót\x000eÒé\x0001\x0004\x0005óùûy"¯Í<óÌòL§àº?çeG'N\x0013¬õÕ;y</p><p>úêÕ«±\x0005\x0000\x0000\x0000\x0002\x0001N
ÅPhÎ7àhC¡ù%\x0007ðüí¼ùoòK­ßÜ®ÜÓ?K,Ó°Ü onm\x001bÊÔ7=Ql­Ü30êð/WãB½Gi·âó\x0008½	÷Cæçm\x001b7B*[ûl¶=RÝ=.\x001c\x001dý</p><p>½ekÍå+­Co¹Ù¢\x001f~d¬l²jõ3çÎÎIÉ£Çà:}_øÃÌ¿û»¯ñ\x0002\x001fÃuxÖ\x0012´°âãU\MÚú^Ë
rãº Æ¥J÷xN=Î\x0018ÍêUz\x0017¶ÝýÞxãÒ,oÅ«Þ\x001cÍ)ÞÌ~Nes¾.Ï¹üçüü³øóÅËY:Yë·îâ)h(4\x0000\x0000$\x000e(tj(B³\x001f\x001a</p><p>ÍË¬âxN</p><p>­+Ó_©`5a½#£q'±tiÜPèælõ|p¶-\x0014æ]pÚÆue£cÜ¬áí</p><p>Ý£f¡í;w±KwtuHÓruMm¶µ\x0015$möìWháåY³Ï76­Y·þÅ^&#\x0015¼éæIêV­Yóê5kÎ«W]¯¡Â1c\x001eâe\x0016WZ j\ßZ9óE*¤¿\¹ñ¦¤\x001dÞÖ¨Æ\x000b²\x0017nY/[{¢Ë¹5Ý
î§µ5½_êlEËRÚ7ÄéÍ18ËÔ7\x0008ôn\x0013õç\x001b\x001b\x001a¯O>7µ\ÐþL'kCÍnöçÞÞÞØÇ\x0002\x0000\x0000\x0000B§")´±y+:)´1Û¬1Úä:¶;¥KãVÖm²µ·ëÎ;)´¶YÏÆõl¶\x000bú\x0000Ã)tgw\x000f+ôÖÚmWÚÚY¡IÒ6Vm¦!C¹ñî^zy\x0016¬]·¾¡±¼ñ¡\x001f!Ç£BòjZ0 r®@°¸Ò\x0002Ù¸Qnl+5m¡
isjÛÑÛäS	ýå´JÚ±í	7¥{+ÛZûI­qeÝ=]GïN:éòæØÒ\x0017æüÛÞsyfyn¹xIû3¬µ»¯æ\x0003</p><p>
\x0000\x0000\x0003</p><p>\x001a¤Ð=\x0003\x0013\x0015z,Oº.\x001cÒ`(¥lb§µq\x0017±toÜ]¡eÙsjºÇò¤\x000eyéÞxÃ7tbF$</p><p>]S»­µ½ã\x001fþIÒ.e¯¼òê\x001f¹ý¯}í\x0006R¸GÆ«\x0018\x0018\x000f?2\x0004\x0016n\x001e2\x0016\x000c¤\x0002A-\x0010´°nÃF£ÜØÖ¥5	jJ^5[º'/é/×§F¸Ü©'7ç=¢C¶µösZ¸PwO^êÝIeÃq¡)ïÌLÎ<ÓI\x0011¦µ©ö\x0013öçk×®Å>\x0016\x0000\x0000\x0000\x0008\x0004\x0014:5\x0014O¡E\x0017m%Ós\x0016Ú}ÆÕH\x0017qjÜE,\x001a÷£ÐÒ¬*¶í.ÑSô(tWÏUúSèmÛÛ::Y¡ÉÐ²ùß[!g«Ú¼JÆ\x001bÏF½±j3\x0019</p><p>\x000c\x001dj\x0014r9Y7/³¸ÒÂMUF¹±­Ô\x0014f¿òªlÂ\x001aOÈZi«Ñ_.§f¥\x001dÛpSÖn\x001bÍJk\YwO×Ñ»ÓtzsÜ¹wfÌÙ*Ït¦MÛö°?ÿõ¯},\x0000\x0000\x0000\x0010\x0008(tj(ªBËL¯~é®Ì\x0015Ä\x0012%%¸ÂtÁúª\x001fïæÔ¸ôµS\x00129\x001a÷i¹,ðNò¯;à\x000bm4Î3Û¶ß&¬íØ~­0T:ã¤ÐµÛwttv±B¤U×Ôð(9[öJ+\x000c½å\x0016²¸\x001bnøú
7Ü@\x000b$u¤Ölw¼5¤\þjÞ½é%-oÊ\x000bù¸ñã:\x0002­¢</p><p>´	W\x0012^ægîÑ2!H\x0007d/Æ²mOoê?\x001cy)kõ2·ÀÝ¤\x0017é¤4+\x001dvzs\ ·W mÎs¿<?·wvÑÉªÚ¾÷Z> Ð\x0000\x00008 Ð©¡¨</p><p>Í\x001eXáúD\x000e]¨çuuÆ57E×¹µm\ò"ô¬µKã>\x0015ZÕG*MI÷´Ó\x001a\x001d¶m\?sÃÈ!Ý¶¶=R£3Z¡ùé\x001c\x0014\x001d]Ý?¼õVZéh\x000e2g&hYÊÿøÚëTÂeÓSÐZ®Fk	Ú</p><p>7Wo¥çëP¡u[Z+»àµz\x0015ùçï±¾J÷xCn\6rÛ0\x0015*hs)ç¦ä`u'¥5c\x0013k'åÛõÍ1É¿·VXÙeò9çÏ]ÝÄæ¼Bÿ5\x001f±\x0005\x0000\x0000\x0000\x0002\x0001N
+4\x0018ÌÈ/\x0015Êc¢ùIÑü°h~^4ÿü7Ã</p><p>gE\x001co°A_\x0001ØüÃQ]SËª_²\x000e;½Ãr</p><p>øðÙá3µyÇ>öçÏ>û,ö±\x0000\x0000\x0000@  Ð©\x0001</p><p>]Vh¶Z´´¸´aÔ\x001fVèÐo­ÝF</p><p>=áÑ1\x001e~çåtÈ	¢µ%¯Ðå#ö±\x0000\x0000\x0000@  Ð©\x0001</p><p>]n\x0018\x0016m+ÒÚ¥Mòé¸\x001fÞz+)tèÍk¶m¯èÿéâðnë3"§iËÎýõGìc\x0001\x0000\x0000@Vèl[×ëï.þÚ»N¼8ÿýÆ\x000bÙØÅ²|B!VÖ"mÕi\x0010\x0017ÆIá3\x0005\x0006\x0000ä\x0012Z¡wì;B¼sÿÑsM\x0017­Ì~ëCZ;sÞ{§êcwË2\x0001</p><p>]¶ø\x0011i0HÐçH\x0014þyÆ>\x0016\x0000\x0000\x0000\x0008DhÞ¶§$ùØó¶k_]°ì¹I¡gÌYtäTCìzY\x000e@¡Ë\x001c[W\x000f\x0012[¶þIÊ?ÏØÇ\x0002\x0000\x0000\x0000(B\x0013$Ï9~}á¾Ã§b7ÌÔ\x0003\x0006=þD\x001a\x000c\x0006èdA¡\x0001\x0000 ¹\x0004RhRâ\x0017æ.vÉ~oå&®ùÇw>zéÍ÷Ï5]Üuàèóo,&þäÐñØ%3Ý@¡~jt"Ý\x000f\x000br Ð\x0000\x0000\\x0002)ôÛËÖ±\x0018Û¢-z×Ác3æ,ÒvMÛÆ.é&</p><p>­©°BýâIÝ¯´\x0014	þ\x0019í®HÄîüäMmåó\x0010n×ü{7t^ÿÆzPa¶\x0002\x0006àÿ³w®ÑRTçº^òó}ÆØ{=Î8çGDwLv¶\x0017¼\x001bMbF#hT\x0014IÔ\x0008\x0002\x001asTî"\x0017\x0005\x0005\x0015/ÜD®\x0011QPA\x0011E\x0005ET6Æ ¢\x0008bPCäÒ\x00054B8ßêõå[sVUW_««Ö;Ç3zTÏ5oUÐOkV5!é¥TôÈ°½âÉ\x0013\x001e~J^^¼ÜÙu÷Cs¨Ðµ&</p><p>mÿ:\x0011ÆÏ,V±B\x0008¤ý)ÆÄ»Tg\x0002ç=þØ+=|\x001bÂáåM£ó\x0015â(t.ÿ\x000fB\x0008!3eùo\x000eúð_nXWSª«ÐÏ½²Zð-Z¢B\x000b+Ö¬=ïÒ\x001e5ª<</p><p>mI*</p><p>]]\x0017/\x0003ûßi$A®|\x001a©Ð\x0010ÒøÔÁ«®ÐÏ.])\x001b¾ES¡Áw:uÓÑ5ª¼ê</p><p>m=GÌ\x0001¾\x0001ÿ\x0007"9zãdÚ]zHÝ¶VLu8\x000b9Ð%$Ä«µNa\x0004\x001eÑ´\x001d=Öï¶?"Í´ýAÒ\x0019Ã±ØFòjçM÷úÇ\x0006¶½:EÎÔ©FwX°\x0002i'Yò\x0005ä8®¨M;'Å¿H¢'ÖQèÀ>ÛaúgD÷j\x000fn\x0007N¾V\x001b8¶\x001b¢ëX0À\x000b¯T¨Ð\x0010R\x000bêàÏÕUèÇ\x0016.uî.|ýw°«B\x000f©³ça[6"\x0002¹²·vj>¬X³¶¤C¤c5í[=\x0015Úê\x001fÊØà*|&Ð|\x0002·õ\x000fëZ­´jã(´Ó|¤B;fè\x001f«ÈÖà¬0±¶\x0016fqN\x0014Z,pGàÞÀð)</p><p>h¾³íw/B¡dÞ/\x0013­Ð\x0011\x0013k\x0015:pm[òjí\x0014»ì±öEô÷¼Qhg\x0006l\x0019§E;èyÄW*ThB\x0008©\x0005©ShAo-|ûý±®£¹\x001a</p><p>ýNgÉçJrB×ZSmJUèZSO¶ù0</p><p>\x001bóÂJï*¢VÐ\Q¶²|©-Z¡US\x0003õõÕÈ_HàäèDÅQh_§­»íPh\x001bd\x000eì°v/Z¡\x0003/\x0006g6"\x0014:zbmW\x0003'Ùº±3\x001cíÓíR\x0015Úqã\x0016µÃÑc	\x0015\x0010BjA\x001a\x0015ZÙðÉgUThùpQ7¶</p><p>-Û¸)RÖ¾UßvÞj\x0001G³åp©\x0013»T5\x0007±\x00192¯»Ð\x0013)`ßÚcý¾Yÿwº§õhÈ=E</p><p>Ýä¥0\x000f	Thû7q¤</p><p>mÿ"\x0014_¡\x0003µÃ÷Gä\x001b¦ã¸«oqÖ?íâ\x0001$ëa{ã(´4¬{5Uèèµ]
d;öÀ?g\x0004~#hª@¡µXÞµ\x0018qáôï+O&ÚP7Îµì\x0003¬ÐÍm_UhÙ¶ò©6«z¬b½Os8¶Z«¼ªñªÇ¢\x00154§m+wZ\x0014P=Vs¤0jö»§Ã)ïÃÆBû\x001a\x000e<°)F\x0014ÚJZ©QhÀ\x0011Õ4</p><p>í\x0010¶7uQè®F_6vÞ\x0002g»©JQè°i\x000cÀ\x000b¯T¨Ð\x0010R\x000b\x0018v\x0014\x001aò¬</p><p>­ÚluZ\x0015\x001a9N(\x0018a^\x0001º«Ý¶58\x001aÜì-äÐ|«ÐplÛ\x0019y\x001bØ=Ä®Ë¥ª+´Úÿ¯Ðí8â\x0017G¡\x001dW±qÚ¢k¡í\x001d^iWS\x0007*tØ±þ¦KsýC\x0016\x001b[ÏÄ³Ôü!çÛ¯\x001föm9po åÚùKv£j#\x001a­Ðvý³Ý\x000e¼H¢'Ö_\x000bíL2î»ô/6í¶=³¾\x001bGL¾£Ðº-%µ\x0015'ô\x001dgb\x0003Ï]\x001c¨Ð\x0010R\x000b¨Ð¾Öj¤ÐµI%V\x0003\x0015ÚÑà\x0008¶
Ù(·]\x0004b»êt8p°
\x0012¶\x000fÍÐ]BÛòÑ
\x000fSè|û¥\x000b¾ôÚ[ÆÛÇìßÓ5\x0012XV\x001d¦ÐÇú3`Gä¬9q*±¾\x0007ykj{\x0014\x000eS×\x0000XÇÓÎY\x0008ÜëO²ÞNhgÏ\x001f£í­¶©BÛX\x000e¼HN¬ÿÂÈ\x000eÙ_È5áÎøÝ\x000e|§6jWeø¡i»ÆÃ¹U6bThB\x0008I</p><p>*´¯¸ðØø\x000b95Ïþ\x001a\x000f­\x001fo¥Æ«uéu´B;\x000bK°#PèwD÷ÊEW]¡I¨äaË¥\x0012½þÄ</p><p>M\x0008!µ n</p><p>½{O\x001e4¾B7\x0017\x0002¼a·\x00136Õ\x0017ðU])gÐ9·\x0001Úúq ¿\x0003·\x0010ú</p><p>µ\x0019ÈÑ>èîìíhËÞêhWYk\x0019¨xàÝThR\x0014*t\x001a¡B\x0013BH-`\x0014ºnT²\x0002ÙGo\x0018löÄ»¦P¡;2Tè4B&Z@®\x001bÕUèf\x0013^®zÍ\x0011P¡	I\x0017Th=÷\x001eXýÖ'}-èÖkä¿¾úã\x001d»÷'ÞOmê¨ÐûÛ("i¥*ôÓKþ\x001b¿´òÀÌy-\¸*g\x001b*4!é</p><p>M²Ä;÷M{d¥xò·.\x0018:zÑ¤\x0019+æ-|oö\x0013oMýãÊIS^»ëþÅ7
{UïéÝ{Í2\x0013§¿¶£9xIVéÀçÛ¼sÏ0\x0006>õEQheì´Ç?Ü´5qÉÌ6ThBÒ\x0005\x0015dÝù¬~ë\x0013\x0011ã¡c^|úÅõÏ/ûxÁ\x001f>þôÚ?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
Instances: 1
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 274 [https://authent.webinaire.numerique.gouv.fr/auth/realms/master/protocol/openid-connect/auth?client_id=BBB-Visio&response_type=code&scope=openid+email+profile&redirect_uri=https%3A%2F%2Fwebinaire.numerique.gouv.fr%2Foidc_callback&state=rt4ICBhRa7VOj2Y4&nonce=nnAww3neUBVzEg0R].</p><p>Predicted response size: 574.</p><p>Response Body Length: 795.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Parameter: `session`
  
  
  * Evidence: `Set-Cookie: session`
  
  
  
  
Instances: 3
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2dl-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2dl-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-adm-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-adm-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-2d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-1d-sort.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=43200`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-complet.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/](https://webinaire.numerique.gouv.fr/static/misc/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-lms.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt](https://webinaire.numerique.gouv.fr/static/misc/ip-fqdn-bbb-dinum-sort.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/images/favicon.png](https://webinaire.numerique.gouv.fr/static/images/favicon.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/toc.css](https://webinaire.numerique.gouv.fr/static/css/toc.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/css/global.css](https://webinaire.numerique.gouv.fr/static/css/global.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css](https://webinaire.numerique.gouv.fr/static/dsfr/css/all.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/meeting/mail](https://webinaire.numerique.gouv.fr/meeting/mail)
  
  
  * Method: `POST`
  
  
  * Evidence: `eJwljl1LwzAUhv9KyPXoOltt15uxDS-8EgYOREdJk7ddNE3qSdrhxv67KV4dzvvFc-N1a4Q_w_Pq48ZZiIeDyFFtXKctX_C9G4k0DNN2EkYrJGw74comN3rWaFgWxPA5pinWUQsEhl5owzbsOCcGN85p-k_Ae_ELSvjpflpw6amtg_uG5RV_VCialVrlQhRpmkEV66cyzbO2FBKlbLJS5UUu1xFJRiLYUA_kpghEsa3QitGEaCr4oK0I2s2r5xAGXy2XFzRR1ITEjj1I_4xIuoiWtBQ9I12P2G1JdP28DCudgqoJfnDWg1etMB4Lbp2V8ePWbi-XzOJtd7w-d-khln0QYbYo5C_73fkgiuPr18N7zu9_Oo96zQ`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/ColorSpace/DeviceRGB/Filter/DCTDecode/Height`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/nico3333fr/van11y-accessible-modal-window-aria/blob/master/LICENSE`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiNWRlN2IxZDE0YWE3MDAzZWQ3OTY4MDQzZjhhY2U4Y2IzOGQ0NzRjOSJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `eJwVjMFOwzAQBf_F5ypNicFpbi3iwAmpEpU4RRt7nRqSdVivGwnEv-Mc3xvN_Cqb2PcSv5BUpx4dmuHgDhrA1HWDzhyf2lo3vgWLrR2a1mmj7VHtlM3MSNIvHO_BIRfboYc8SYEOkwQCCXGr3kSW1O33Kw7lDIwV5Rk5fGesxpjvlefCJhtnLK5nGOetjGSjQ9czpiVSQtV5mBLuFEWyZSmi07o2hO_n68_LWF-KnARkQyz69fl8u4C5vn0-fGj19w80pE-i`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `Creer_une_reunion_Improvisee_V5`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `eyJjc3JmX3Rva2VuIjoiNjZiMTBmNjQzODcwOTY5NzRhMjdkZDQyYjAyZjJkNzRjNDM1ODg1ZCJ9`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/1.Creer_une_reunion_Improvisee_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/ColorSpace/DeviceRGB/Filter/DCTDecode/Height`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `8/Filter/DCTDecode/Interpolate`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>wOFF\x0000\x0001\x0000\x0000\x0000\x0000\x0015H\x0000\x000b\x0000\x0000\x0000\x0000,�\x0000\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000GSUB\x0000\x0000\x0001\x0008\x0000\x0000\x0000;\x0000\x0000\x0000T �%zOS/2\x0000\x0000\x0001D\x0000\x0000\x0000A\x0000\x0000\x0000VI�N�cmap\x0000\x0000\x0001�\x0000\x0000\x0001n\x0000\x0000\x00056���glyf\x0000\x0000\x0002�\x0000\x0000\x000e\x001a\x0000\x0000\x001d�\x000c�8�head\x0000\x0000\x0011\x0014\x0000\x0000\x00001\x0000\x0000\x00006\x001b}�Vhhea\x0000\x0000\x0011H\x0000\x0000\x0000\x001e\x0000\x0000\x0000$\x0008p\x0004\x0008hmtx\x0000\x0000\x0011h\x0000\x0000\x0000\x0011\x0000\x0000\x0001\x001cH \x0000\x0000loca\x0000\x0000\x0011|\x0000\x0000\x0000�\x0000\x0000\x0000���maxp\x0000\x0000\x0012\x000c\x0000\x0000\x0000\x001f\x0000\x0000\x0000 \x0001V\x0000Yname\x0000\x0000\x0012,\x0000\x0000\x0001\x001d\x0000\x0000\x0001�\x0014���post\x0000\x0000\x0013L\x0000\x0000\x0001�\x0000\x0000\x0004���Tkx�c`d``�b0`�c`rq�	a��I,�c�b`a�\x0000�<2�1'3=��\x0003�\x0003ʱ�i\x000e f��\x0002\x0000&;\x0005H\x0000x�c`d��8��������\x0003H���L\x000e\x000cV��@����\x0001+\x0008HsMap���э��\x0001�\x001c�\x0003\x000c\x001f� 9\x0000y@\x000b
\x0000\x0000\x0000x����m�@\x0000\x0005�E�I�9�s�6kp�W��r\x000f����]\x0019G��\x0001\x0017L�.�n�Y;�\x0015������z�љo�ߙ/�ӹ�p�*~��X�\x0017�������آ�^���\x0006h3�\x0010Ì0�\x0018�L0�\x0014��0�\x001c�,��\x0012ˬ��\x001a�l��\x0016���\x001e���\x000f9�\x0013N9�\x000b.��\x001bn��\x0007\x001ey�\x0017^y�\x000f>)�i��h;4�����WtV�+��p'TE��Uw�K�V`{\x0002�\x001bؾ�����\x001a\x0008l;��j0�C�\x001d\x000e�H`G\x0003;\x0016���N\x0004v2�S��\x000e�L`g\x0003;\x0017���.\x0004v1�K�]\x000e�J`W\x0003�\x0016���n\x0004v3�[��\x000e�N`w\x0003�\x0017���\x001e�|u\x0018أ�\x001e\x0007�$���=\x000b�y`/\x0002{\x0019ث�^\x0007�&����\x000b�}`\x001f\x0002�\x0018ا�>\x0007�%���}\x000b�{`?\x0002�\x0019�2(\x0001�ԵD\x0000\x0000x��Y\x000bl[g\x0015����<����K����q��a���rZŹN�Gh��ЦY;�f\x001dc���ѭPM���бʠ�G���д\x0002�xT02	\x000c�xH�\x001a�@\x0015Hӄ�@\x0010�`�;����Wꔔ������?�;�?�;�!\x0002!\x001f\x001f0m\x0014v\x0010;q�5�@HvȎ\x0015f�,�\x0003��E,\x001a�</p><p>x)��6���P\x001c�p`\x0001�\x000b�؉\x0003�\x0006\x0013��}\x0007���F3ݛ���2r��3�~�����Qv\x0010�K\x001f�\x0015l��u{{Gg��z\x0006\x0006f�\x0007�@*JpE� �HH�7�ȝGل\x0003\x000e�\x0002�@�:d�\x001bh��ߌ\x0017D|���\x0006]q\x0008��n�@(����vG\x0011r\x001d\x0008\x0007wt���O�'Cǟ�r�P���_^�[[��\x001bw���f��\x001f\x0006�����g�!\x001a��\x001d��}|�\x0010n�z��\x000eG׭�/2<�^\x0018Z;��\x001a�x��X�����]�'bH���Č�\x0012B</p><p>�Q�vGp="a),�$_�\x0017�/g�-L�����vv���tZMg��x��\x001d�"�Xdێ˹\x0001�a\x000f����r��%��\x0001�"\x000c�y�3�I�\x0016�y$��g�DP3�j\x0017U�"��
ZUn�\x000b�Ia�؈DV\x0011R\x0005\x000e\\x000e��-N\x000cpy\x001c�\x0014��/=\x0006�\x0016�na�ne�\x0019�5�
+�TU\x0015V/����a�8\x001ak��\x001a�%{���D&à�����J�XN\x0003x@@_��[N�v�P�=\x0014R��Z�\x001d���S��\x000c���w�?�yRIH\x0013�U\x0010C\x000fГP��\x001e�\x001eNB��u6>\x0002�\x0015�_t'ç�+E�XdC�͡c�Cڛڬ\x0002mW��,ē�s\x001f�Yx�~�d\x0003:\x0015�U �	�3{��G�pF��p\x001c�'	�r\x000f����*�\x0012�\x0006�Y6\x0003�R����G��t�\x0018=��:�@�=��9G_F,l�d��\x0013@H\x0001�zF�ހ��vQ?g`OF��8���\x001bJ&o�D_����e�\x0000{�*�\x000fqe�-(�</p><p>\x0002��\x0008AmN���Ou�g1H</p><p>^�c;V�\x0007#\x000b͑Ap��\x000c�\x0007����\x000e�1�	0MM�\x0008�f�\x00117�\x001b\x0003��/nɆ�q���6����L�6���+�,\x000e�v3l�\x001ef\x000cƼ��F��v�E�_�-8�D2ּ\x0010'le\x0000}l�'�G����]�?��\x001dJ>F:8\x000e3x�p'�\x0018�t{1�7	��\x0006B�=6��a�@8�p"��h/�
O$�</p><p>�;��#��~���\x000b+�R\x001a�S�3Z\r:%a�)e2�\x0013#���\x0017�{��L|$�\x0018P��\x0013n+H5{\x0018\x001d�\x0008iI��<�h�Icz\x000c\x0005��jJp����\x0015�-�ƛW�B7W�V9=i{u�M"M1��\����쇘\x0018�����\x000fxb\x0014ש i_�\x0016���X &c����2\�{Q��\x0006�,��a����\x00144\x000c/�\x0017�\x0011|�1��\x0001s�\x0001].�����i�S��S��r�¥ie\x001a��D�n���1�k8'�Q0f�h^��U�#\x000c�W�y\x001c��y�۹\x001f�\x001c��80Bͅ�/\x0012�xXβ�0�Q�R6�+��9m/�;�W��`q@?�\x0010yN�\x000b�����b�NV�<R�p��U�m�z��\x0004����\x0016�a�\x001a�"\x001d�\x0004�������&�!�ZBbȮU9�N	�\x0016�`�u(ژ�u\x0018��j\x0015N@��m��\x0015�M�\x0000�o'�Ă��@4t3V\x00193'��\�}֠e�j]�;���~[��R�.��k;�o"VR��=\x0000��H�:�OR���&7[��β�&E��\x0016\x000bʴfw��\x0014lZM>��\x0000$V��E9\x001bnBǡ\x001e<�e���c���W��\x0014x�=z\x001a�*�]�.;)9�]��;j��\x001e��\x000fc\x001d�\x000bd�\�Y�\x0015�X���u̟\x000fl��g^i�U�7\x001e?���}�������=;�\x000f���u\x0003�w��0�\x0013����#�\x0010�v{��	v\x0010V���}���=}��5�#[v��2Һ�0��1\x0015\x000f�1\x0015\x000f���\x0003�z��\x0011\x0017iB��0gE�nP ���\x001aJ\x0017��\x0002\x0016hÓ\x001c\x0010]4V\x0011�VS0\x0007�.*�f��Y��\x0001�o�yeՊ;�=�\x0014��|>�Jx�*�x�w;&['w��i��9�5��\x000b�\x000f����}}�����)�c��ݱ=�\x0015*�K\x000f\��֧��J.x���;�\x001f\x001c����5]��5��vN���9���ղ/9|����U#kV<���_�\x0017~N���\x001dz\x001c�75 ��!\x0003aU.\x000e\x0001�D\x001d\x0013ܙ\x001c\x000fì�J���\x000cK\x001f\x000c�c�S�M��8\x001d'"�	���9\x0010��cH�6_\x0013</p><p>��x�.��DA)��Zz!�}	ch,c�s05��I\��W$'j�[�N�\x0014�h\x001ccJb�+\x0014��<�R\x0013@�1)\x0005�(a�ו+�:k\x00064�ݪW\x0019�E�\x0017x㗳{\x001c�ƌ�\x0007OQ���`CIԯ�A�\x0013\x0019z�v�\x0004�<�d/\x000b���\x0011\x0017�Ln�Ƌz\x0000���\x001e�]l�b���ۂ(R\x0010n</p><p>�j�k�	��#\x000f��.���gkU�l'c�!���z�`\x0007̶(��\x0012g\x001b�\x001eK���3\I���:��\x000c\x0007���4j��"绸��\x0014���)\x0001�;�Z�r��Ȱe+\x000e��^?�{	SI=\C:o�"�
\x000fr��k��\x0014�2E\x0010�/�N</p><p>������NK�~����[b�\x001c���	2۩�\x000f�b�)�:�FF<:�֡\x000e�?�\x0010{����V�#\x0003c8t\x0017��\x001e�+\x0014J�\x001f\x001cܟ\x0008��f*���Hh�_(*x
�|�G�\x0004\x0012V�XхV\x000eiI@�<�i8�\x0003fԔ���V#?K�T�-I �\x0002�H"����\x000e\x001e�#�J;=m3�ب}\x001f�7\x001a��&�\x0005e�1毑ZQ\x00056O\x0015-\x0016+ܣ\x001d�>+�\x00172p\x0018\x000e����=
j��h�wa����n�^[ f���c-�}xq�cٗ�y^��gYsr��9\x0007Ў��O�\x0005*���OK&�I�@�k�Ϧ�/\x0004�GZn�\x0004y��\x0004��(
\x001e�sܻ\x0014��E\e�5\x0000��,���%�TS=WUU�)/�5�ڏ�j*�3�$.�\x000b��\x0010��\x000e�\x0015D�[X�Ţ�\x0011�\uu�Ƞ.�S�\x0019�T1#��J�!n\x0001)�Fև�X_\x0019�c�5a��3jM.9�1�'��c=/r�X6��J\x000bˉT��4ց\x00070H3z���\x000es����R*%aC]����x��n��*O�e�^g�Z@�ӳ��� ���\x000fؗ�Pk��J�:s�\x0002ͨ\x000bW�z����JU�\x0017�^1�?��Hs�</p><p>�\x0007��He\x000f�R0�.�U\x001dKE�\x0014�
2m\x0013�]���¶��\x0015\x0011�\x0012ū����}��
]�wWt��M-.�QvE\x0011�:Z۳��DP�\x000bڝ��5}�NiC����Ў\x0014]\x0017�-4�\x0015{�6\x0010ًK\x00173��*�Sr���=��ʮ
w\x000c��4�\x0005�\x001b�\x0019��{��l�[S�uڃ�n\x0011�C�o�%�z\x0004\x001f	/aY\x000c�\x000bf\x0019;`�W\x001f\x0010�h$���K�����xL���\x00177vv�3}���\x001ev�2.�\x0005�Q�3�O���l]U�|n@{s�&~6���>�i�p\x001f_\x0003\x0002,�qg�@tB��M����\x0000{\x0017���}v�\x0010Ž���\x0007\x000f�j�5y6���מ~���O\x001c>t�\x000b?h	Z���������������np�<�/N�o�N�66�\/��#�ڟ>���\x0001�\x0015������*��e�'\x0013{Or,����0��,/����KZ�m̐��Z�dU\x0012\x0007�	s\x0014�aC�	�⎔g!R�:��m����\x0011��Z�\x0008��Oe\x0013�;ml�܌#X���K�6����Dٸ�g\x0019�V��Ͱ�£��K��6=t�d_��sl\x0010~\x0004�v���ࡍO\x0018k��l��Ts\x001cy�4\x001b�ߍ��䥾k���\x0008��\x0019ެ$�v>�O�/\x0002���y4��i����{��p�y��wl��	8���!���4�N�"��\x0008���M�G�;:�h\x000e\x0006�\x0013C��
\x001e�g��0[r�\x000fry��ɤ\x0015ٷD������K��\x0005(*jP�SP\x0003�^\x000bj��Ǌ"|[\x0014����\x001cR��w	�G?��Ԋ��T\-�\x0018�b���?�T\x0011`��\x000f��\x0012��\x000b�,�f�J��UV�YDm\x001e��l</p><p>�[�{�:\x001bϲ���������\x000b�U֊��{�p��#�\x001a�[�\x000e'�{\x000c�+��b��\x0019�\x0005r`Y\x0018��W���W~u} t�c��\x0002�A���U�\x0007�R~X\x0003��x1\x0019��ꦗ�%ϝS^{M9w.Y�\x000b��]�O�>x��A��}P�n	\x0007��X�\x0003�Ht\x001cG�8�Zn$4-</p><p>�r>�I\x000e�lݜ\x001c��h�2�#H~�\���ݯ�Mn~�����Q��\x0019S\x001e�\x001e3=7\x00165��.��%@/���#�/A\x0011H8\x0000\x0000x�c`d``\x0000⥅�n���|e�f�\x0000\x0014a�}#�1��\x001fʲ��\x000f��``\x0002�\x0002\x0000��
�\x0000\x0000\x0000x�c`d``>�_���e\x0003\x0003\x0010��c`d@\x0005�\x0000V�\x0003�\x0000\x0000x�c````�0��a\x0000\x001f�19\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000L\x0000�\x0001\x001c\x00014\x0001d\x0001�\x0001�\x0001�\x0001�\x0001�\x0002\x001a\x0002.\x0002H\x0002b\x0002�\x0002�\x0002�\x0002�\x0002�\x0003\x0006\x0003@\x0003T\x0003�\x0003�\x0004\x0018\x0004D\x0004v\x0004�\x0004�\x0004�\x0005\x0010\x0005|\x0005�\x0006</p><p>\x0006:\x0006`\x0006�\x0006�\x0006�\x0007,\x0007~\x0007�\x0008</p><p>\x00084\x0008d\x0008~\x0008�\x0008�	\x001e	Z	�	�</p><p>N</p><p>�\x000b</p><p>\x000b^\x000b�\x000b�\x000b�\x000c$\x000cp\x000c~\x000c�
\x0010
N
�
�\x000e\x0014\x000eh\x000e�x�c`d``pg�e`e\x0000\x0001& �\x0002B\x0006��`>\x0003\x0000\x0017�\x0001�\x0000x�]��N�0\x0014�O��h\x0010\x0002!1��\x000bR�3�\x0001ڙ\x000e���I[%q丕*13�\x0014�<\x0005�ŉ{%*l��;�\x001e_\x001b�\x0003~\x0010�[\x0001��v��\x001b�\x000b�Iw�\x0003��\x0010!��GT/�c�b"\x001c�	o�\x0010\x000cn錑	�p�Z�O�]x@�\x0010\x001er�������\x00181��CL��>5u��űL�g_bm۽��<�y�ֵ��әڞU{*\x0016��*��R+S;]�F5�\x001ctꢝs�r:�ŏRSa�\x0014�n��F�#J$�W�\x001f�LX�tZa�\x0008������g\x00128�\x00193[�Y[�8{A�!�Ι1�H+�K�܆N�{\x0007:)�\x0008;��\x0012S��_>�W�0�Sb\x0000\x0000\x0000x�mR�z�0\x0010��\x001cI�4M</p><p>��,W�e�r�\x0005</p><p>��Pd��l\x0019����X������hwV\x001a�[�x����},`\x0011�p\x001e\x0017p\x0011\x001dt��\x0012�\x0018`\x0019C�`�1Vq	�q\x0005kX�\x0006��\x001a��\x0006n�\x00166q\x001bwp\x0017�p\x001f[��\x0003<�#<�\x0013�x�gx�\x0017��K��k��[��{|�G|�g|�.��\x001b�c\x000f?�\x0013����^_Hi�$��H��(QC\x0011\x0004���Ԋx�q\x0007zB+�
\x0015�rk͑\x001f�����ųv�V!w��xV�ٌ��9�)�K1ѵekc�\x0015\x001b\x001dL�<Y(kD�qJ�����"%m�Zņ
㎁,�H\x0002a)�\x0019���T�?U��\x0013s�	Im2Վ�Ǌ�K��*W�Wc�p�j#�)�*��%\x00189m��se\x0013�\x001d�\x001du��}\x0007L\x0018ra٧��Ϲ��h\x0004I4�\x0010\x001d�P\x001a�|݆ѓDIhl,��$�='��6e\x001e�H��XD�5B\x0014A���ߩT�\x001d\x001a����vV!�T�\x0013�#DWOm����G�	��o���3F]V�VeS�	���a�\x000b!:q���\\c��\x0015��</p><p>�\x000f�-O��`D�\x001d\x001a]�\x001c=��\x0016�\x0015qQ��9�U,WB�+�~��]��\x0007dYx�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js](https://webinaire.numerique.gouv.fr/static/js/scampi-modal.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bFROM\b and was detected in the element starting with: "          // we remove content from its source to avoid id duplicates, etc.", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js](https://webinaire.numerique.gouv.fr/static/dsfr/js/all.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="'+i[r]+'">`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/cgu](https://webinaire.numerique.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/3.Creer_et_parametrer_une_salle_de_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/donnees_personnelles](https://webinaire.numerique.gouv.fr/donnees_personnelles)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="/welcome" class="rf-link rf-fi-account-line rf-link--icon-left" target="_self">S’identifier</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found with a target of '_self' - this is often used by modern frameworks to force a full page reload.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/](https://webinaire.numerique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/welcome](https://webinaire.numerique.gouv.fr/welcome)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr](https://webinaire.numerique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 3
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/home](https://webinaire.numerique.gouv.fr/home)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/documentation](https://webinaire.numerique.gouv.fr/documentation)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/robots.txt](https://webinaire.numerique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/accessibilite](https://webinaire.numerique.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/faq](https://webinaire.numerique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/sitemap.xml](https://webinaire.numerique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/mentions_legales](https://webinaire.numerique.gouv.fr/mentions_legales)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Other information
<p>In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000690`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001755319`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001345`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001049`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001009`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000650`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001436`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001214`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001305`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001744`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000092560`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001082`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001704`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001730`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001173`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000000795`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000095119`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001765752`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0001672462`
  
  
  
  
* URL: [https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf](https://webinaire.numerique.gouv.fr/static/misc/2.Participer_a_une_reunion_V5.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000001770`
  
  
  
  
Instances: 1825
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0000000690, which evaluates to: 1970-01-01 00:11:30</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
