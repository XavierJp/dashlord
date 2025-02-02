
# ZAP Scanning Report

Generated on Sat, 17 Jul 2021 08:29:21


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 8 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| Directory Browsing - Apache 2 | Medium | 8 | 
| Reverse Tabnabbing | Medium | 3 | 
| Source Code Disclosure - Perl | Medium | 4 | 
| Source Code Disclosure - PHP | Medium | 8 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 9 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf](https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf](https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Directory Browsing - Apache 2
##### Medium (Medium)
  
  
  
  
#### Description
<p>It is possible to view a listing of the directory contents. Directory listings may reveal hidden scripts, include files , backup source files, etc., which be accessed to reveal sensitive information. - Apache 2</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/addok/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/housenumber-id-ign/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/](https://adresse.data.gouv.fr/data/ban/adresses/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/csv/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/ban/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/group-id-ign/</title>`
  
  
  
  
Instances: 8
  
### Solution
<p>Configure the web server to disable directory browsing. </p>
  
### Other information
<p><title>Index of /data/ban/adresses/latest/addok/</title></p>
  
### Reference
* https://cwe.mitre.org/data/definitions/548.html

  
#### CWE Id : 548
  
#### WASC Id : 16
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/de-la-commune-au-d%C3%A9partement-la-collaboration-sur-les-adresses-dans-le-gers-c0d83fb20950" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/de-la-commune-au-d%C3%A9partement-la-collaboration-sur-les-adresses-dans-le-gers-c0d83fb20950" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
Instances: 3
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-14.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-14.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#G1FUn`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-04.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-04.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#yly5m`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#gNLF`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#G1FUn</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;¿\7\x0011¶n©÷²!êþèá»ë¿n\x0002mdINÈtbÞr\x0005«¥Ë£OO\x001f¯â-\x000bØv¢\x0013o8äH±]xJ¹û,¬6¯sÒ
WUpU'\Gc<Ä>xáñ\B®ÕþôU¼Þ\x001eô\x0019{\x001bûËØíÑÕûû­±\x001b·9£\x0016\x0005p\x0014¶(\x0012\x001cÔ¯7ÄnN_.Çn´±þ6¶\x0011·`\x0008\x000f|¸$õ\x0002IJ¤Í·wÀV¶­ì\x0000lnR8|v8m\x001f\x00028b1Vï¸Ü<4àvc¸±\x0019	º22n#,ý\x001eë\x001dÜjÌ\x0014\x000c\x0007ú/ä9^\x00001ÃÆ\x000e*\x0010GÂÈ\x0013B:$\x0018\x001cåfe³\x0007wîy\x0001\x000cK¬Mî a\x0015²¥\x0005éQ\x000cñÃ½äíÏ×\x001b£üØ\x0001ãô+\x001cåÈ£"\x0005Éðy&²}'ÜNWYó\x0013vYacØÚÑ vÇ¢è¦=\x0016»°
»\x0019ÂÎ%]å¸î)«\x0006Ä}V(µ\x000b{!\x0018°;>´îFe¢8 WO\x0013é®\x0000\x0012È$öÁ®S©¬ î\x0015ºwªMÿÛû»÷W7·\x001b«\x000e\\x0008dðPÜ£~c$Ü.-:L¥éÿq~yñüäì|¡ôÀ'þ\x000e\x0000^Ów´\x0002\x000f\x0017[d\x0001òCà|¢;Zï!Ù\x0000ssÐÙ\x001f\x0002\x000b_F(Oî®ßoõ \x0008B*¦¼ »"\x0017$1\x0016/\x0007\x0018£<¹8}¾ØK Ë
²ìÆ,²¨UºåqÚ!\x0001'5Âh\x0014ò\x001bæRQNÌá\x000f\x000fb;`+\x001aTTQ~[CcZtßÒÒ¼\¸×ÌÖ(?Gv\x00000w~'Ðùýu\x0000Åû¡\x0016à,E<\x000bø[;ùåúGÐº{útcEÀª\\x000c!Bñ\x0016!3)Ôl6ôY\x0019|ÚÉ³Óï@ô.ü'.$CYýuÚ3Ò èü\x0000©\x000bôdá(É¤&r6Óµ­G\x001bÁ\x0016ÁF\x0000\x001b/=hm&NbÔîïi4ÙÙ\x000cy\x001bÖ"\x0004
XãÄÅWÅ³¡ üX·\x0016? «\x001foßm­*IÜNá\x0012\x000cÝN*ªÿ¸pB¬Ì±\x0002tòêÕùÓ)½A¿\x001cÀç¬ÏÙ0~MYÅðÙáø©Z\x0012e;ñ«
¿\x001aÆo`â7á·ÐJðëíº\x000f¿¨Ö_¯¿Ë'5gÈ \x001aðÓíÅ©Y\x0015NüÕö\x0017ãûb1áúØZÄïÆDÍR$ôá/d
àóµ£ø
§é\x0015%Y"3	øI4:\x0004¦³yÉ>üNø\x0018ÅïÌ±Åý3U\x0005Â§`(>e{á\x0017"jjFOÿüÝÛÛ`Á
5ú)X|M^Ö=[róÏ>:ÿn\x001d¤+Aº\x000ecô\x0014@2ÚÖÜ¦£s{ÀäÕZòÅ\x0014\x000c®ßÄÆq~\x0016Wr^Ï^«\x001a`Ú
¦í)HËZYüÚ\x0001§(`Sª£Qªx4Fo®ï·\x0012áEäiTC\x0003{3ð\x001c¡~\x0019!åóÓôôñÙé%\x0010à¯b\x0015\x0015VÑ\x0015ä\x001a5Æ\x001e¹eÖZC_'õlÁZtl\x0004¬qÜ¿\x001d«±\x0013VMÙÖ8:çølÚ¥	«¬ÖUv®ëDqÌ4ÔRÒ\x001e b6ô{\x000fAuòàëw2~ýeÞöåÕo·¿_Ýý¸Qç×e¥41¦0¥¤tb\x001cÂ]OÝ¾<y}þçï^®¢/â þ°8Ñ^\x0013»n¸ïQ\x000f¢\x0018h\x000cÛ\x0015|Q¸\x0002\x00031\x0006>b\x0012Uj}æC"óDêM1Ð«Ã4´!Üýê§Ük\x0002\x0019®)E\x000b\x0019X¥\x000fgÃñ.ÄTz6|\x0000ä'Or³	¤¸\x0016÷¼:(Áÿ((Á@·0/JÊ\x0008ô¸ó4ª3?1Ð½Zv5¶ì@>â\x000bPÌpix7\x001cÜèbÔ¼²q\x001bvò5¢hé``	\x000e®ßs#±¨VÛ<MÀSë\x000c0t´l#©ÃE8_.\x0017FB\x001cÔ\x0013ÓÜôÝO\x001b]»æ\x0002*¶\x0011ºud,EÙlR¬ajúâÉ"ðXá*(Q~p(ùË¯ï¶¶±Im³Â#Pj`ÁPrÔÙôy%ñøìÅÓÓ\x0010\x001fa\x000b[ÂþDXµ\x0005wXc"De
µ¨\\x0008\x00002;ç¬{\x001bnSGý\x0010¤¹\x001aöý»ÍUPÉ\x000eäxP\x000bÉK=U·(^>}µàÊ\x0011rAá\x001a \x000bÙYg®bÐ.cX¹Ë\x001fV·4ðoÄl*Ì¦©#\x0008¤âÒ\x0000\x0010¯'ÎÖ\x0011ËCï'\x0019õfö4fz¸	¦F\x0015>&2ÿ§ÆL¾A93ue. N×b2	¨ý\x000e»IãQ³U¼À\x0018\x00042i¼C\x001fs$TDîçä¬BlÝQ\x001a\x000f\x001bP/XÃ?E_°Aü"_\x001e²ÀÄ\x0013ñ\x000b¢\x000c\x0001ùÂU\x0017~Wáÿ¤·\x0015¿£~\x0010\x0005c*ðÓ¥RÌ\x000eÑwâ/\x0018wð\x001a4_ºdú\x0014ÿ,h#ü7É*Gÿ0ü\x0001rô\x0011Ú\x0011@;
F$h\x001b»P=Ðæ§á<rÐ\x0005@³JÎ\x0005çñoGð·£3¨/Áß®îÞ^ÿú FË/ÑÂc?^¸\x001cc\x001buðãÒy´ÒFÌ
\x001b-ÃÕþ;ÁïÕ}\Þp\x000fÿs\x0006¢KP Dw"Ó\x001eÁ=¹¾û%üò§\x000f÷wº¸~û\x001e\x0000ê\x0010tHÜ\x000bÀZÚmB\x0008Ë0åd¼*Fx^<\x000b¿üéååÅ.N?{p\x0006KP¤£¹«BT\x0003ÿêC*ô±	i\x0016cl\x0006Ri´hð\x001e\x0005
a#ü«\x000f(7(Î¢#H\x0004É\x0001¨BápÀ\x0014\x0001õ Rßz\x0010ôAenVá²B\x0006\x0002\x0004\x0015Í}PÍoâÝÛb>\x0004GõÛýõvÌi PÊÛ\x0014\x000f{£-wbéÕ?\x0004\x001fõúr¦?¦\x0018^èhU
~`/]»aô\x0012GDa\x001ahi\x001d[\x0010\x0006¡¾BâÝÿ~ã\x001cö\x0012Ä\x000e³p\x000f½»}÷6C\x0004:,¾\x0002i\x0000ú"#\x0015:wkd©ûÌn\x000cwÐó§3}Ù%ÆX\x0004?¾>Vÿ¨ÿz\x001d\x000f}\x0000	ÙÙû»XvßÑð
\x0005<µqèC§Î§\x0010\x001f]^¼/½×\x0010©ð¯\x000e´d´N¡è$=çH%	½úz\x001fÐç\x0016{ÝÚ1Z¢Q
 ]R\x001b
ëèQÿÃ1£vÂ\x0008sZ¶o\x001ds*Ak'´5¼k\x001cö\x000c½Ýé]Ã¤H\x0016ù×\x0011æÏ]×:\x001aÆPf[k\x001a\x000fûQbjÃ±Åèb;Ä¨
\x0004b¿Þuÿöÿ«\x0003ù¿õÛ»ßßÇK]ØØð¯3Èon®~j8
!\x0013Zãu¸1\x0000!\x0005ÐÙZõ\x0015\x0017sÂKOÈÏÎNÌ\x001f\x0013N\x0008¡¤ìÄ\x0019¢²äÈbÇ"¡Ô>£,Ôp\x0006QB\x0017ü«\x000f%	%@È(û\x0003N#RºÊz¿ÛbÂé[LÏ\x00126i\x0011&­\x0003L¹\x001c7àò§í[NÏ8éokhâ²&át\x0014«ykv[Oòê}ëIj|\x001a
«Qt\x0018ÖSegÏ\x0006S×÷oþ\x0017f@bÞãá¿þù·ë÷Wï·_r\x0017\x001e&Åã%G©Ä8\x0003\x001cèéö`*©ÏE¾9}~27\x0016\bdäø£\x0003¤³\x000csJ w·[á
îMàÏ\x001fBùËï·ÿõ·ÛlÁ«\x001an>Ã4ëäLø¯\x0014²¯¥
^Ì*3×\x0018Ó=ì+ÄxÅÒ´S.\x000b8\x0016ªÔ¸ýøîÃD9rs}ôâ\x00063Ñ[?¦ðÖ5\x0005rÈ\x0011Ï4Èìb@\ÖV>üüÕÓ/\x0013çHø°^Í³\x0005\x0014V¤Æt²\x0002úÒG­°ù$ÐáÕÉÅ:ó\x0015Á
³x;ê²ÂUV¸q+8WÁÑEz`°ÂÃÞIVh¹\x0014ÃôYXzÈ
¸\x001a}\x0017 \x0018É³\x0015*E\x000fÎ9º\x0006jµÜé±3VZ\x0001Ã/ChäW	7E7Eí©\x0015ÆÐ}÷\x000f\x0003Uê&3Æ¿o\x000eÜähFâFL{Ê\x0019%Åà^fðúmð\x001dÞ\x0006hb\x0019|\x001b&ùÀ\x000c<óÃÛØýËà©ª­âÊðjH\x001bÉÉKyIoh^[<%ú¬Pµ\x0015j\x0007+\x001cÎ\x000f-¥S§R0C1Kfì÷}\x0003Q?æ\x001f§?@&\x0012Y·
ÒÂ\x0006çü±ÁèQÛTg`\x0008¢gbé\x001d ÛÖ2{a;ï¡\x001b¶P?p¯0TÓ@¢¢s#é~ËÕR¦ \x0015·ä%nÉ\x0016Ü\x001d\x000b¼¥4Å\x0005\x0017®?ËVä9BJ;Å"çÜ§©\x001aùÒFo\x0005nª%7cKNCñ$q¯pK\x0017c·X]kF^-¹\x0019[r
ÂZý.Ò\x0010­Y¸Ûí¹Ë]µänhÉ­Ç	\x0010
Ã\x0014\x000cÝ
g´äf1vkEîE\x001cX±ú\x001b\x0018¬´´<1\x00001\x001dÜ9Gàí\x0008óÊ!ÂãÈsäÑ\x000e±¡DöXF´^}¶yâfs\x0013t\x0015â}YP?¦Bý«ûÆ\x0013z\x0005²öB\x001a:´YÊ²eÞÇT±qry¶jç¥\x0005\x0015!g\x0005Â\x0003\x0005S¼u)vl\x0005Æ3,ðf)Dî² z\x0007~ø\x001d07½\x0003:\x000b\x0019üYÑ;P\x001bvP\x0005<éf\x0005ð8hö°òñ%$]êhµ\x0014\x0018Ø-.³É\x0004Ym#.÷Y¼h\x0002ÓIÆ\x0007L ²ÌÎ&ÈÚáäXÄ·\x0010BûÿaÔÎâ ¡e÷où7ï>\x001c|Ïð!;Â?r« ø)õ\x0010{Òu\x0011r7{\x0019áÄ´Â&\x0010Höþèæê>Øpòþãí»÷×GOîßÝ4
 ÉEµ\x0001²àQ\x0005Õ0ôb
\x0003:-\x001f\\x0006SN¿:úüôèÉåÓ³åc"Ù#Yid;Ù\x0013®R¢=\x0002\x000bÚØÉS¹ÅczÀ\x001eQÙ#v²'\f\x001ahÓ$¶à`£\Wøæ\x0017ë~{Tõ~ÔnïÇMïÇ'fBx?v[ýqÀ\x001e­J{@y|\x0017{Â\x0015\x0013¯\x0010àÐðd4Þä\x0002¿Z<ÛûíI}dñ{í7¼Z\x000b/\x0016\x001a?Bt·èØúí±Õ~³{í7-qz&ØC\x0003ÚN[\x001eûíq=n7{¨\x0002Á|"Ô\x0002{\x0014Ï±ä²§:Ü^çR¹\x001fA\x001aJ\x0019kèÞ~¡ýæleÝëýðc
õ\x0015h[Å×Ã(sÉ¾7(\x0002~\x0001ÿ.Ö0Jaj%±ì\x0019Ì±ÂdU¯~{¦BE´'\x0016*v1È0äñÕÒ\x0017¿\x001eß\x000f_?ûíáÕ×µzí±\x0006\x0006LR;Jô¨Ð(Ãs/!ÿ2î ü^\x0019\x0004Y]\x000c\x0002ígô×V\x001fc\x000f¹@É¿LxÀuå\x000eàq\x000f{|ø§\x001d\x0014¿i¯)Þ±VÓ\x000bR~wÿ&\x0012iØd`G"ßx]ÝÝàÄæò·FþLhPN3M\x0010JÓ{aÜmHN\x001e=;¹8³\x0012kè
+Ñ\x0003§à\x0008úðà¡\x0019ù\x0010\x0013xÌ
Ö»åwÐ\x0002^\x001f¤¨N)ê4\x0001\x0007´mw·»ºû±\x0001<¨Ñà'.\x001d~\x0011!þ\x0017ù\Ù?üüù«ó¿\ÌðØU]a\x000fÑ>ÃóCÊ4\x000fÄ Ù=\x0017kþ¶
}q¨éPïE\x001fb{µ8Kì$\x0001½È]vq°¡\x0019ýTÖècY{\x0004¾&þR­@Â\x0017[VÔt\x0015\x0016k¾t+üÔ"!¦\x001b0Ó\x000fD¥×þèêîn{jÜ9X9õtª¹\x001c´sëÂB^óäâb¡Y\x0017W]®º\x0003À` A×r½NúTßpb±JÐ'\x0004Bzû¡o
@(TcV]h»äj±jÕ¹\x0019ZvûÅ*MI,¯pTØ	·\x00185´"\x0017¬B\x000e#È\x0015ÍLBKnîf²À{½[o\x0000/ÓW:¡¬ôüö÷È4°9sèsfÊp´Ñ@Ð¼\®%qÃççSû) \x001b]B6º\x001b2¨J`²Ó\x0018ú8Cti\x0008³\7`æõu^Õ×Ahøêc\x0008#o[\S\x001a#ì\x0012JËÈÅy\x001cÂ<úþäU\x0008\x001fç¸\x0003Ü7,Ñ0ræ\x000fÁ¯\x0007_þäîêýG\x000fo¡%¦a{OïX¦L¹Q\x000ex å\x001fvµ!_n|ùçß\x001d=<^W3Ìâ7?þöëïÿýÃ4wvuF°\x0001¢OsÀ¢\x0003þñúO¯~¾¿{÷Ó{\x001c\x0006VaY*M+æÀó\x0007áü\x0004Ý³°Æ!úÕÜ\x001cj\x001a~wú§Wß_^<}ò\x001c¢Â³£4ýùµ­a}f¾\x0001áä¾~Ð8\x0017çzp&\x001bq¶ M8E¸â ÎC.\x00010·ÓûÚ\x0003Në)íqé\x0010¦>T
l)>Üýúþ#È \x0010\x001a@÷£;YÞ\x0008ÔJaÒÈº\x0012@·
d?Ç\x001eÄ"tD\x001aÀò{\x0007Iùå\x0012©Ü`üÑ\x0014úHç¨°\x000eó\x0000©òÒ!ÒO\x0018ýú¡FFø£\x000f*\x0010A¤E\x0015á\x00103	j\x0008à\x0015Aõj7¨Ð\x001fôAUXQU¡MªÂæ¥U]Þ©-Páì?ú¶j8DªÈ[\x0015ØF#T#\x000eéÐ\x0007 \x0006L\x000fâ¾Uõ&ÉLÁ\x0006PÐ¾\x0000P
áâªªýV\x0015J¾ñG\x0017T#Ml\x0002¤\x0012\x001a¥"ÒÈ±\x001eÒ¯ô#u\x0010cÆ\x001f_ýûwpÙ?:\x0017U¥»YX>/ °VU"T%}Õÿ²¿¿{\x001bùl\x0019¤ïnïÿÖpLY\x0006C¥\x0011'\x000f×E 	\x000cçÙ¾tNUÃ38¿;¿üËü9UÀÆ\x001aap½BÊµ \x00000m,CGv%:i	\x0003¦½«Éñ«çP-\x0007ï\x0000Óy¦\x0011¦ðf7\x00189w­¦N¦\x0000ÓyÐ>K«é%Áäv7á\x000bÒ}«ÉLù¼ðÒYT\x000f{3\x000eFRí·\x0018àw®¦áøÒyòJq5io~¢9\x0000\x0013
\x0006`
©
ô¥\x000b³ß'÷¾/\x001d½\x00116f~ãþ´´\x001fc¾ôìLËqcÚØÍ
Î=f#\x0010¦ÚÍiÂ1Á;;´âF>"ðÓ\x001bKNS¯ìa\x0007§»ïóÄÎ\x001c`:\x0003LøÖqg:vÈÞóý_yà®\x0004Åøãìú\x0008Dbjd#ÐpèÞA\x0013\x0012î"Ð\x000c!¤M~ÓÊOÝ\x000e\x001ezÐ¬\x000cK\x00014*³Æ\x001f_'Ðÿ}õs\x001c.\x0013bO.¾kÂçãÓT¥^RhÌ{2·"]\x0014h5¤\x0011ã@)cå?¾^°oÞÞó7\x001fb¾=f\x001fpe/ï>Üß´5ÌÓmÃ|R¼-Gý[üª=¤ü\x0014ìåÅËËð¿gT\x000b°<þè\x0002«}¸ÏÇ¢i\x0000+\x001cpX\x0002Xnß¸C¶Óy¨sëú_@Bòß?\x0000y70jÅði]½}ußðmÙpóàñÛR"D¥p|\x001fÌ#XÇý!Áó§ßÖÉóç§'«X\x0005\x0015\x001f¤_=V\x0011	d\x0004RÈ|XÕýõß`»*Èâ\x000fØ®\x000f¯î ¹×òq	ÅSÈçµ§oË)ü¶\x000c7|5\x0000xxr\x0001ù½\x0005·õão\x001fþ\x0016\x000f­\x0018ê³´°TBÙb?Ü8Ã\x0014¯÷òº6,ëJ¬¿T@©`Â4CüÑ\x0003Ó°$\x001c\x00070\x001d4¬D\x000c(å\x0007XAùÓoo7\x001fË\x0010º\x0018\x0016>¹\x000b¿_½¿º9º¡ð¥e3xëS×D_ ï Ý¡­St\x0001P+\x0019´btøä"ü~òüäì(G5ó;äç_?¾±?ÂÒÃ}MU=CÞýv]7ÛK\x0000:Ü¨È£ÎÒñ&%¾ð\x000eEwk;¦ªÕÓ×\x0017ó7\x0001øÕÿóî¿>Ä\x0010PÇ ib;\\x0005\x0013Ï±\x0010\x001bNcgS-x\x0011#ð²Í>\x0011×údÏ@³Ä,ÈðOe?L<õé\x000f\x0015O}d\x000b~x\x001b\x0016ü!Iyn>ð ¶À{ %Jk­$æ\x0007µà5øpÿáyXøKò9(¬æÔÂ*\x0003öHúê=ÊÂµ=Ú#\x0018F\x001bhìf­Ì±;\x0003i14'HEs\x000c¥Å\vð\x0003öøÊ\x001e¿=ZOÛ-¥D{Â« (|vµ\x0007¹ÎÑCEÀ~{<¹*Ï¢Îh²Ç=\){DeøÖíµwÛË½ \x0015î7naì!}?Ù\x001d\x0008¿\x0018Ì
Øã*{ÜNöXú9À\x001e\x0007\x0012#É\x001eÍùBîMW¯Gïõz¬M\x0014ÐàÞ4\x000c\x0010Es¬ { MäËØS¹7½{\x000bw]Û-
à¥ë#£ÏGíí®¯fXzI8	xð)ËÔÅ=<µ\´\x0011o\x000c'ðÔ9Àh¯I)\x0016£°\x0003"KxZ¸\x0014eKDiÉ§¬_=¤½\x0015-Q±m\x0003L\x0011ÀÒLQjùJ×k,Mùß¨ë¥HthYî'ðV0\V~¢JK>å8ê±[ªª0¸¸ôR,6ÒÚ/c.MÑû¢±\x00173§è³\x0017Q61âÄò
 ×\x0014SböùTDþT¼¡\x0000MÌO2e¥]¨×\x0012[Zò)-[%á& Ð}9ì'qÐ\x0015Ëé¥,ç\x001bz-q¥%n\x0017KL¤=¸½°%NSýDº,O¯)¾4Åïb
p\x0005àîRàÈ¢%qÊ>Y²R>ï´³êtü/¯Ã\x0014/TjWáéc2Ïx­a¡×ú ßå¤÷ZAª;ÚÂ9ÌM`ÔuxÅ¾Ì©Â«£ïrÖC\x0011/EÈÁ\x0014:Þ\,â-*Z;ÙRõ|ÃÞ§\x0012\x00049cLï*®%í1þEâ\x0016^ö|ãÞ\x0006%"³\x000fRéË?êÞÉê´çû\x001c÷^P\x0015"\x0017tbÆÒioÍ\x00179YxuÚó}{\x0013¹\x0000Rd\x001c;\x0005Sª6²;;1sx[1»­¼¾ºAz\x001d\x0000Þ`±\x0014¾@\x001byeF_¿òÞ¶l³×'gHµ\x0003ÿÞu³DiÖ§î¬ß,<ZÁ,\x0013Å£YÚÎÂ©Ðrn¶%K³>õl\x0003fÙ9·\x000eæYÔëÏ\x0004k6[ÍR¥Y:¹M¨\x0012Ñ?\x0014\x00048Õ/¥zÀZ#ëUº´êS×o\x0013Ø¡É@Ò\x001eo\x0006Ìij:àºå0j5Ëf}êû\x0006Ì2IG6}Z´\x0007×È§eK³>½÷\x000c¥P5%-P#$³,úA'¾¤U®´êÓ;ÐU\x000eïtÌp\x000fs-Ñ*Ï<\x0005®ãËåK³>½\x000fõ\x0005¬p¸\x0007\x001e\x001dW\x0012ÍÒüZîð0vt\x0018\x001f}w\x000bCy
ýpôâÝõÝ\x001dô'Ü\½ûsS?a\x001a-\x000bñÃò¢õTN%ÿãç
;úî\x001cFû 'úò\x0008\x0004¦/ gáìäù£ï\x0017*ÒÙ6QÚ&öµÍû$í\x0000¥F\x0003"±\x000b\x000bÜ`Jö\x001a¶vÓ\x00184NÆÉ]³ã\x0003(®Ñ8Þ^¸åÂÉ¸qª4Ník\x001c\x0017]É$\x0015¹bt\x0019áb¹-qØ8]\x001a§wß\x001e³EÂÒk£¤êZgà°e¦´ÌìkY\x0008¦$:\x0013I®_QbRåÎaËliÝ×²pWÁ¶C¦,\x0000ç$])µX»R\x000e\x001açJãÜ¾Æé\x000cÐ«>\x001a'òÕß¬fÇ\x0007ó¥q~ç\x0003ç*\x0006\x000cØ\x001b<àè\x0002mÙõ$EfÓåÌæ^ÆéàJÂméÓ7g½sùøÖ_öãuh²wl"0òçÀ\x001aÞ M)WFøM«"\x0013¾shÂLn³ñ
 vX@5õE­«B\x0013¾ol\x0002zAäñFQååYAaÝZÖjÐº*6áû\x0006'F¨$\x000ea¥Êg\x0001
ì¨òËs¼MøÎÁI._³È¸Æ©üêÔÊ8ê°uU|Âw\x000ePíº§4\x0008Ï¦Ä\x000f3Ô³Z{\x0018´®QøÎAJ\x0008¿°µÒå¡Òéò­\x0005ÿÂW\x0002^\x0005)|ç(ÅÄT\x0008U2[G5V!Å\x00176®
RøÎQä
«*\x0016øÈ}cf5Á0f¨Â\x0014±obÂu.)\x000c\x0004ñ®Ê`Z/Yç¿p"ª0Eì\x001c¦p\x0013ü\x000cÚË0Í\x0010"vº\x001b°/ýîê\x001cÊÎT\x0016Ìù!Ç¤ð9Aôe?;Q\x0005*bç@ÅÄÆtaé<PÔ# WÛ\x001d\x0006­«\x0002\x0015±s \x0002µ6¼\x001d$ÿRÌtõ«µÃAãª@EìEÉùs \x0016ÎÉ½|ûåAqëª@Eì\x001c¨x\x0008íuZC.,ZKTá`øÂWrþÃ_ë¬ó_ÿ£ÒÎü7µyoþÃÌ»®Í»þ\x000f3ïmmÞÛÿ0ó®jó®þÃÌû±6ïÇÿ\x0004óX\x0000X%üà\x000f1áG\x0014²÷GOîn¹¾iX\x000c"X-ÐÖ¤ÖøH!â2ÓÉâI@4²GO.Î-^\x0005¶²ÀY`¼\x0017\x0014dA\x001a=!\x001e\x0004µcå,ë°@éÒ\x0002¸ÓY`3¿\x0010$Ð\x0002\x001b¢
´@-\x0017m:,p¼´\x0000DY\x0006-°\x0018O]$@¨)Y0í"³´j·z\x0017ámdý1Z <ð(áì41þh·ê°Àêú;\x0018ÞFN \x0005*ÏS\x0004\x000b,ñ*ñåyv\x000b´2¥\x0005ºd\x0011ï² |ªä[Ã·\x000c¿	FÒøTø\x000e\x0016î\x0016\x0013­ëð\x0007¨W"qþÍÕÑãÛ»VmÎÁl+§^JrDBÈÅ\x000b\x0011\x0012ç\x001c=>¿x2O"¡Û\x0012º\x001dnÂ\x001dÿX`j3äärZX¼ípÉ\x0017¿ßVèÅ0®e\x0013xß²\x000b¤eçtÉ\x0006½M\x0003ì­Ð¥(¡\_/tN×0È¨â5L²bÚvÑé4cW\x0015v5]\x0005i\x0010»Ë$
yÒË=3WBÇ\x0001ìÞøcÈ!è4EËi»ûå¿Vð²Úî\\x000eíwï,Æ;\x000c¶¾À\x0011zG\x0010\x0006jGð¦Ú4Ü\x000cíHþO\x0015\x0012\x0005£æi\x000c ·\x0015ñåÒ]+x_o\x001b?´m ï\x001f¹È\x0006ÇÑ¿ïé#¨ ÃãÐÙd2ä­\Q&Ô®gPÕ±
#àÍÓ\x0002	V\Î\x0011\x000b³ëÂ\x0007ßBÊ¿¥»Ò¿ý&8E«ÄÔ\x0008#|"ó^°}<NÊ4Ó-\x0011äåù$õï¿ÿãä7ÿúgää9:}\x000f×â7M\x0017`\x0007\x001dªH|Ï\x001c}\x0006B)bËÒÈÎstòìáidç9:}\x000eWâK_4KêÒ,©w4ËbñÏ	{ÌpêURY:Ã7°\x0011\eÛÓ&Ç\x0018±E8ll\x000f\x001f:Þ*¹[î\x0001\x0019°	U\x0018§í·ëþ4
\x001bã½<ÌorÀg¿]Sê"ÚU\x0010]í`\x0017ç8UA|_ Dì2KÔ¯Kìûº²\x0017t§\x000b¯HÉÄJ8`ÖD)\x0013Í*Dè÷x[4\x0019\x000eTSüS £\x0019¶ìRµ]jO»£]\x0008S&³~ä×õÅ¼;8Y¢]xÜÏ.`ÏÂÆ# \x0000Èk@96¡¿]¾òðð¸ççÅVy{\x001fÓ\x0014\x001cÙåæÚ\x0001»\x0004«ì
uûÙ\x0015\x0002=j`ÔÔ\x0004'9ñIöÅ¼¡Ëé@/³ph\x0016WéMa °R\x0010\x0017îrqÀ,/+'ïåNÞHÐ\x001aEJ÷Ì²åõD<¹r»è6K:ÔÏ»ÙeA7ÞdÌaiÁ ]ålPsÀ.`ßÓ®p§aÇ\x000cÉX\x0015ÃÆn¯¨1Å
¾ÜvÓo\x0004&é2ÌÒ»½0n\x0014\x000bH\x001dlt¾\x0015\x0012%É0-Y_\x0006\x000c\x0013õ±\x001cw4ÌR\x0007:J:.Áçs4l¥Â2b­ß\x0018<ïùÆhNÂH'i\x0018xzcFê/è;r%|ò\x001eW;z{í§Kç9º{MIR£ÇU»l\x000b·­xUÎ\x0015>¸~§\x0007/n®Þ¦üE°ìô§w\x001f2\x0018Âàì@tx¡,Éò¹em\x0017g'R
ãèôÉÙÓ\x000b)\x000c2@T\x0006a\x0003tl|MySG|PSHÁí2¹{\x0005¾²À\x000f[Àé./rB\x0013ë\x0008wË¬\x0002íð\x0015+áºñ·\x0005¿Ú?j|ÿ(ïçåû¹,Xæï°@U\x0016¨a\x000b¤>\x0016Xöp¢OáÛM°å;P\x0005¦²À|c[HW\x001f°þf>`å\x000fÊ}á\x000f\x000fpäúèÕÝ¿þùÛm\x000b+»Q\\x001cÛtÁ$Hb\x0004j|Ìxx¶¬ÛYÙ_]¾>_ e'øÿ\x0001øÁÞ ×\x000c7Ö%\x0011>\x0015@@­|GðÎ\x0012<< ×aàP\x0018×áx,twPÐ¦tÓfü>BDüð8\x001fd\x0015°½Æ¡\x000caÀO,óÀµ#|i+áÇç\x0011ü
tÿòK\x0018é>ËÃ\x000c\x00087÷m\x0004«\x0006\x0018­\x000fúRÂ"QùìþèñíýÝûw7MÕ3«gÌ\x0011gcyKÝòòèñùåÅó§gëÀm	Üö\x00037LèÔÏÄ¬wøÁ:Ë\x0017bY/¤\x0011vÑ\x001a\x0011`çÖ®\x0005WãÞy}L\x0011BR\x001eC/Ívà®Ú(nd§Ì=UÁ´¢\x0013Jå\b¸._W-\x001dZ\x0017-\x001d]Ðm\x000cq+-utø|=YÖàh>W#tÎF ûpb=5¸FgqÕ}nF±Ë¹\x001aúÕÝÛë_gq\x001a·\x0018Zrº^\x000c
ôÈè¨¬09iÁ½ºäª>ò7ç¸Ñí´ä&°Wt¾\x001a¡\x001aº\x0018n\x000cj\x0014\x0006èÔ§
åkªTûåþóFè²Þ0rhÃ\x0018Úå¼¹ÒDÁÎ½_>@ÛpzÉÍÐ\x000by,&\x001cj¸b¹wcY¤¶\x0011¹¯½¢\x001fñÐ°DD	!zÇ¤4Dï\x0019Nþ\x001d\x001dzÙ±\x0014 O\x001dK]ÐCÎ±l,ó¢KËÆËôÈUåÏ\x001añçÎ«iÖs&WPõþ¼\x0006è¦>\x001a*úÊEm)©	>\V÷\uS¯º\x0019Zu#\x001f9õÙcÙ=»'LÓ)º
]ÔÐGü"d\x0003\x0005\x0015äw¨o\\x0018JË]N£+~¨\x0014Â?£\x0014òï¿ÿãüî:ZòúÝÍÍUS\~4$j¸#ùG5BåÅò;¨h\x000cÎ/N£]¯,´¼e»Di×!ùî]Vã\x0014ÓZÞª N\x0016ÐwÙÎ)Þn,
;¤ß\x001d3,ÝÅ£aJ\x0010a \x0012û\x00106pº¶\x001b¦JÃ\x000e	x\x000cf*iC<ÐBá@\x0003¼±5\x0016\x0011ÃtiØ!\x0007ïaÒ\x0010·°6Á&IR6øÆüJåvÙ°Ï^\x001e²U¦´êwðuyH(&ÏÁ­VÀÌ\x0015ZµÞ\x001a|]¶4ìwð\x00034\x0013\x0004e[t\x000bÚ«¤CÛp\x001aôM\x001bñjOÓ@yZâ'¦ ¹*&\x000cÖ²U!ß1MØ'ïñf××æ0õ¤ÊÍb\x001cp7ÿ²¦]Õ¦ý\x0007½6]¿6½ïkûÿÉ6{\x0018XÙÏ\x001a${DSJN\x001e\x0013\x000c±KBF(VVe\x000fx¡!\x0001Àª)¢4å3B\x0006=¦xb\x0014\x0006^ZâP\x0014\x001dê\x0010«·hM4\x0018#Kc>#_ÐcÇHÌ¤+é3ÁâHx·1ª4æ3¢\x0005],g a[d\x000ee [¾±ö\x001b£Kc>£UÐe?f>_\x0004§t*å<Ú~än1\x0019\x0013\x0013ñvRÈ4úùFø:ö\x000f=úù_ÿ÷}ÛÈ¤!\x001bl2úà2ÎW¤XñZø:ö
=úþôùÒäI\x0019y_\x0000£6À¬¢D\x001bbÃ|\x001a{lP[r!-6ê5Àã 
 \x001b+ÉØ\x0002F\x00169\x0016Ø2¿D
Å¼(Ø Ù°
\x00018UG\x0018Mÿ©\=ævSr¤Å\x0004k+\x0013¬\x001d6!àé5@±\x0007\x000fªbr¶)\x000bÛbS	N
`©95Ü>©0¨\x000c5 ±-SÇ&èÚ\x0004=nÇ.@\x001bÁÙ?e6\x001c{\x000bE}3`MÐÄØ\x001dßÇ!+Þ3¿,ò\x0019\x001bfjnh«
pã\x0006XHå'\x0003dÖV$äe'ZñûÚ\x0019ùqg\x0004y\x000bø9ô¡§R\x0010Ç¹!V\x0003Dm\x00187À\x001c[<uü5\x0019ß[éo5 vD~Ü\x0011Ð\x0011~\x0002a3y¬hQº%\x0018°ök6 þýø7l£Ê.\x0019­àJó\x0016Ú÷\x0013¨?a?ú	\x001b\x0006ó\x00172\x001ff
ñO½¤lYø¬Ý
V}Æ~ÆÁ\x0006"*ÌNI\x0012
´é\x001dØe\x0011\x001e\x001bDmÃè\x001cß\x0003\x0012ØÔ\x0013Þ\x0003õ4ûÐîïAÖ6Æ§Á\x0006O9|«\x0004Å§\x0001º¡÷°³\x0005²~\x000brü-\x0008F\x000cÇÖ:\x001a\x0011ÖBRxÊ6u¨m²!ÜÌ«\
üáAÙÜxvõëõïw·÷-½\x000er\x001bIE\x0013Fî#w¸\x001723£{½â¨;ðìäÅéÃÓRso² \x001c\x0005\x000baÙ>\x001b\x000c(\x0018d¡\x000b'tj1õ2\x000b\x000f»ÜIÒ\x0016#\x0004¥\x0011ð8jf8M\x00140IÕË|.À¬åÎ6bì+Ø`ª6ë\x001e\x001bløG\x0012±\x001cè½\x0003åR4båÒÜa\x0016\x0011Z\x001aÁÃ.`Æ¹dï\x001dÑr9·Ì+ÙaZ!À\x0008«Ì°\x0011&&#L¢Ôó±WlØ{7¹©)\x0012lp±)rÈ\x0006\x0011\#\x001b\x001cÍ×ñ,¼ìÜ¦ùº&#Då]áqÔ\x0008EÚ£Üxz\x001eò$\x0018qcw#\x001c«plÔ\x0008)82aL\x0013\x0008\x001ed°²ÝÝ\x0006_ùWx\x001cµ\x0001\x0018Çðp>%ñ
Vç\x0017±Î£Å\x0008_\x0012~üá°>ÖdñùXÄé1BW»	\x001eGp<ÓÞõL2/È\x0013-
F¸ê¨ónø¨S\SM\x0008DñMHM¼K!äØÂÐd¯ß\x001f}\x0013|ðÇ¬Nºø<ú& /LÛ)j4ÁPYïÀ­¥;¬P\x0007V\x001fØ
hîødEú(ÔäbíÆ\x0019µ\x0006+«­0ÃþI9ÍKÑ
ääV\x001a\x0015;ÚÕ_E|\x001e´BKÍÇ<+P{\x0006e«Ìj½»\x0011üÀáÀ\x0003`è \x0004¹Àd\x0004£\x0010P.×y»¬\x0010\x0007V\x000c\x0007ã\x001aÈd¶Âãgá\x000cÚr\x0013I\x0015òÀáØCÌ\x000e­}TV\x0004øh\x0005[©´[ÁUýqÃó¨\x0015\x0005]½e©±\x001d¦h9í(Ë÷þ¸¹ò\x0007V&\x000b,\x000c¡¦áð.rô\x0001ìaô.ä¶Î\x0006+ê\x0010*>\x000f[Áq²Ãkaè¢,ÉdºeñÖ.#ø\x0011ã.Ê±<ØÌpÞ \x0018a$\x0019Á÷·âà´àã§\x0005(ÔiÌÛxò³á\x0014\x0008óÍÛ°\x0005}\x0019\x0018a\x000bþ²ÎHsäH	F8`Ç\x000eFðÁÑi·÷aaí\x0011vØ?<\x0015W'^|\x001e4\x0002Øjð¬âDJ\x0018\x0008N|ö\x001e¢}(FÎ£\x0011õÈyß`\x000fÈ'÷$£Iâp×ÞÏÉP¿îb
]L¤è0Éæ4\x0014ê@hj½VPjç"\x0011gË¥RRtrÖ,àY\x0016.Z\x0010E/ÆL\x0000zOªöó\x0002%
\x00055a2·<D×nÐª4\x0001\x001eÇLÐS\x0005x0Q¤\x001cø#2½ñ^&¼IÔ)Syâ!P§ÄòÄëï>\x001e!°\x0017`\x000c¬zü\x000cM9}\x0007lø\x0015å&Ø\x0017§¯¾::Ã§5Üy&-á´^Ü\x001aæ\Ñ\x0007\x0001³H\x0017']Nn4\x0002ç5p>\x0000Ü8¤\x000eÀi²Ûzã+Ee¦£\x0016à2;ÿ¨L\x000cì\x0010D ß\x001aPC£·a4\x001cm¸XJm\x0003.ª\x0015Ç~àÚ¢\x0006\x000fWÎ,M´ÀÌ°#nUãV\x0003¸Ã1+RØæÃ¯\x0016\x001c§º
WËÓèmÀë-.G¶¸Éóa<ìfÈS¨¤;«\x0011¸Ýs§ØÊ\x0019ÂãÀ\x0016\x0017T\x0002b\²\x0006\x0003e#Ø²ÜM\x0013p£\x0008\x001c\x001e¿->Åb\x0011w\x000cÅ¾	Ü\W¸!Hý6p×ëÍ¿õö5î\x000fóÄ]\x001f=ú[9ztÎ'Ü*ïÇM²_+K4\x000b \x0010\x001c¡\\x0011Ml\x0002ntufÂc?pGãþB\x0008NCj\bAÞ\x0000AÊ8ðð3^%ÌD\x0003\x000b·RS(=þûïÿøþúîMÓeÒ¤\x0008\x000fw;Ø\x0002§!Bð¸½¤ÄÑ÷§\x0017\x000fê\x0010¿Ú\x0016yì`cøÃ®áØ ÄD\x001aw÷¹\x0017B-\x000b¢´c×5v=ÝZºÆ	å±m×\x000b$t\x0001þr´Õjú-y¬¼A\x0003 áÙ\x0000H	l1#I\x001a¥üò Y£\x0001\x001c$S
\x0003âó \x0005!nÄÞ{\x0001\@i\x0007	7éÈÃ´§\x0001I2@ÊA\x0003<³Ä\x001f\x0015V\x0003'²¼Ñ¨\x0011¹.vµÀ\x001eX`-\x0006ü°è?½Át\x000cÐ©ìù\x0011pÉ+\x000f\x0014\x0007
\x0008'\x0017¹ A\x001dÞr¤"\x0005ªí]_ôº¶À:¢?ø+P¼6\x0000\x0007O1CËá\x0014ã(/â\x0016ô
ôò4Ùf\x000b®x\x001a\x000e-fÃa`vÒ7\x0004\x0012\x001eÚ8\x000e³cÅÊãÔr¹ñ{fÎ¯"JSægÃLúû`6\x001c\x0007j!µ\x0015Õ~[diËühx-@ú¶ÀÇïEdx¶¬ÔÐo*\x001f
o3FCË(Í¹{\x001c
4ê$\x0019ëa Ø`.\x001f
oû`tæÜ	+ÚfÂûÅ££ß\x0018S\x001asÈÓe\x0001i¬èI¢ñN3¼ÿ¢ç®¶$M,\x0010e_\x001cþð \x0014-¿>zqõSËà;\úT\x0004g(Éà±Ú7Âl:\x0008O^<Y\x001aúHÐ\x000bÖVÎË¼\x0003;0ûà-Î&ª¼\x0010[¡°v¹ÀØ
]ÖÐå\x0018tKuEÁ­:N\x001dá\x0016EI\)onkèvlÕmª°\x0007ä(Á\x000b«î3öÝ×Øý7±Ûc\x0011ÑêÜº$ \x000b£
ýþèáõ\x000fW¿7Ô¢E¸{¦lr&{®°cÚ¬T²\x0008úåÑÃÓ/Oþ¼Ýñ
»ãcØÃ§\x0008¹ÅÔxÏ5CÅlx\x0003Ê[áûG\x0003àÃã\x0008|©±«DX/R°í¹!úYãÌ¶[ÿfô¼Z|x\x001cB¯,VoEì\x0000ÐiñÞÚÀtÇð¹2F\x0000?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=z{òêü\x001d¨ÂË\x0017\x0007[ë34aSÓU1u-Ñè
îR&niêNE\x0012)þ¦ª,Z¡êú6Ñ:u@.­I\x00154$	«\x0010IKªiÆcvOñ¿hq\x001cÒZ<3þp}ôáó·wå`¤\x0008ÇÀÒMg+\x0008OìXnÒ´Ì4#~{zôáÕóô«\x0003%\x0000\x0019Ò5n\x00002°\x001cSÜ;ç\x0012\x0014\x0016\x0012¥YO¹{"%>O{)q\x00171iõ`qËd¢´J\x0016«3\x000e	ÏÛ?ÚéM%¾Q¤7Ý_ÝÞ\x001cTÀ EÉ\x0006×Ïæï¬q-hfÛ0ùìòäüì.ÏL»02qDx\x0011Sd\x0015P \x000cÇØñÿ1Lå]MåÝr*,:¢Ú\x0003Í];»\x001báÅ\KìB¨`k¨`CYËUÃFGê{R¦té:¶\x000e¨hj¨hCáyú~F\x001c|-Í®!OÌµ.£²9URv\x001c«(x9µ1+(cù±ç¥\x0018ÀbºÎJä\x00082\x000fÄMCÁÝ<ü|Øu	ê®\x0014F+²ýü¤³b\x001a	â¸i$Ø³³÷¯$Ô¶&Ô¶\x00104>\x0017Z)ih9\x0002¼ïÕz\x0014'\x001e`\x000c
c\x0018a$Í¡D(#Ë´/Óbë\x001eF©'_Zê&W\x0000>êÅí§ÃÖ\x0000K?©\x001eÐZ\x0007%êG\x001beÔtG\x0002?ÁI½8~ÐbeB\x001dkB\x001d{	¥ç\x001cµ!Gr°=\x0006Í\x0000áúí#¬'¬C)z	%»o±+QP\x001b¥®D\x001dåÌúö>BÛ|eÛÿ5-²Vsÿ\x0016B\x001dâLÕM\x001f^hðB/s¶]\x0003Ì#\x0013ü\x0003átÑÄrB!ã$\x0000'\x0008=Ðç?]ÿ{9AY¾=\ÖiMàYB*Ð¨\x001e0¶\ÏbÝô<yú:7qÆ~u~¨ä&\x0001Ú]\x001d\x0001ñÇ>BgK%\x0002ËBËlq>í£tC\x0007"9È;[\x000e2ºïnòÇÃâ\x000b´.²gll\x0019$ä¦1ÚºïÎ\x0010ðÅ\UÆ\â¥\¸D\x0006\x000bHÏ¹FÎS\x0019ö6c\x0017s+tpIAck¼èc vòq¤ä6{ÂÕCG¤­Då¤}9úp}ûÃÕí\x0013OÆ´Æq3p¬iuñ¥Jn\x001az)§ííÑÓóoOÎ'.\x0011~\x0014Z7·õ\x0019æñ¶~{ýåËÃ#P)ý÷6{+tñâúrq'^\x0002\x0000¾}ÿ\x0016\x000cðÑ£ûñéê«/_ï¯Ë\x001f\x0012µý>È¿ß\x0004ù}nÐÂ¶¬³ÿó¿þ÷É¯W77w\x000fé\x001eÈK´ïÓOW?ÿød@Óµ¯!
<"\x00197\x000bÞBJÐãªÒuýüåÉë7o¿9;:ùprvvñþÕÛ\x001dPó¡\x001b ¸\x000cº\x0007\x0008ãÍ¸\x001f\x0014¼Ð¹\x0018WYë³À¤´Á\x001d\x0000?yöûÿå~þû§ô2ÿ4þïÛ;üuúãÍçTM¸	7Ä¥´\x00080i)s°^9E£%8T¥BÞ^à'<:}qöjo%!^QS¯óÎ¿¨ÚêÎ\x001e¾ÞÝ\x001e$i*\x0016\x00052°Wyþ0pÉHÒÂJ¬Ú)ÎÞ¿»Ø:¨ÀT
¦zÀlL\x0012ÈBÎ$!e°K×\ºËÇôjEYQ\x0004fr/¹r\x0017\x0012\x001d\x000235é\x0012£Ï¨SÙ\x0014
+M´¤[õ\x0015]
åº |E\Aæ\x0005u\x0008&\x0003	»
,Ô`¡ëÜç\x0019G\x0008æÙã\x00050§\x0018L¸!°0=÷¡>÷¹\x000fçìê×»Ï÷\x0007ùði`\x0018\x001eÿèrÈ\x0006Ç9R«X<Ë[pÎN>\¼Ú7$¤Â45¦\x0019Ái@\x0008bú³Øb¬lá0Ê
0]éú1e\x0008X\x00180qBsV&*\x0008ÆtSý;©¿ÿXêo>öb½\x001bÊ\x001b°Î0©\x0011óêe!©²\x0013{¡vmØi&Ìww·_Ñ)Á\x001fß|þòå.\x000f^?p\x0004ÐmÏWÜ\x0004\x001cóAõTÞe(kà4\x001aæ»ówèào^½}{±\x0008{Å®jvµ\x001d^æ6Ûe\x001ben%\x0006xÅêÉ\x0004³1¼®áõ:x#°3	sÃ\x0000o\x0015ÁÙÜ\x0018ÞÔðf\x001d|®ÏJ\x0007\x001b\x0011éØ\x0018»5sfa\x0005º­Ñí*t9ïl:pù`Ìâ¬²¯hÛÂ»\x001aÞ­»Ol»VåÄHvÏh9§_VÀû\x001aÞ¯7:ÇÁrLñ w2çPÑ)ÜøÀ=¬¼­*Õùám\x0005GÛómåScDÉ¨n\x0003Ï$¤ãÅÊcc5é\x001a#óÌ\x0012<6ÞúÌËFËËj\x001eW3¼
4âÇiMO	­7Ö²Ñr¥¢ÄatæCÌY\x0004ïØ\x0011Ts\x000f¡\x0015ô¶+Õ\x0015ä\x001cº¢ãåë\x001aå\x000f»\x0002½¹¯råÅw/>£Í§Æ(vlÔ®q+ß TC\x0014ÿgL\x000f?ðóËH?;g]Ý
¤µ¼®¹r,qeñÔÿtõõúêáèÅÕç«û\x001f¤&Um)ÝÔUånFbë\x0003ÃOïNOÞ\x001f½8yuvvr¹o W«j\5«qÆ<;ÀTd¶\x000bíè°ç¡Ö\x000f«kX=\x0008£lP°¢\x0018\x0013\x001d ¹\x0003=BjjR3Fjd*¤HRÕÇ\x0014þ	ß¿Ám%VWÃºQØ¦ä'Z*\x0001ÜèuÁÝ6Ô´aV©ÔµheNÜ\x001f%T¡µó¯önÜÊ	IëÑ\x0007y½8Î>«q&'¡\x0001×\x0015áº
®Ø4*Eý.ÆèóÇûë§\x0003"a\x0017·Á\x0008fvQÍÎEõ³º\x000b\x001bìN]¾âù.§ÑK)&ã\x000b1áábóyÕJð\x000eß0{l[\x000f¥©)Í\x0008¥'ï\x0001ü~%©iñ\x0004 î6Í®`´5£\x001da\x0014"e~)`C\x001f\Å]¼fî*uRÊÆ3HG³ö\x000c:\x0004*Ë\x0003ÊJ¾IV½£O\x0013öxd\x000bhCÎú\x0012ý\x001bþ\x0011óÔ@ÖX?|þz0w\x0003>WÊÄ%>xe\x0007r¹\x0002G|rücÚaýþÕ»ýÉB¦j2ÕE\x0006¾·-®,iLÐú¦¸²r\x0015®Ét\x001fJÕéPbXFfÍ*4S£>4}Ì1ìòh4%ø»WÙÌöaø@\x0006:h!ã\x0002-y	2\x0006\x001frjHt6$w\x000f_Óe}y\x0005øõúËíõ\x0013yUL.Q \x0006ÇHW
\x00003NO¯êÅûwé²¾<?|8}{~úvOÆWMAÕ\x000eô!×¼]ÝßçL+¥¦UBüóÒZYÜc	~«#¨\x0012\x000e\x001aÈOäõÌ.h_ò³ÒFþ\x0016\x001e\x0016{Ó¬\x0015ª±Ôr,g-Î\x0004\x0004,¸\x0001*gÀúï<PÛcS\\x0011,]cé\x000eia\x001dÊÒ
6¯Ê5VÈ\ë%Í:ej,Ó'­h²´$åEPZ¹\x0004\x0011¤UÒ"#T¶¦²\x001dÂ
2wÅ°<­XÄ{¾¡Y%+WS¹\x001eY¹Ü¨\x000b²R>\x0000§\x0003oµ_sàc\x0015;°´Í\x0000­\x0011à&§×'\x0008+\x0006úð$]ñ
e«\x001e:ô\x0003èy<æ+è'\x0007q	¾¦ì`5Ò=â³¥3Äge>[8©¾bXó\x0015U£\x001fTðX°°ª åÉM\x0019åL©ò\x0019úÅÜ}É\x0003¹äcúÜÃzÂæõ5 µlXsôõNwÁÙÈp:
, Kd\x000cÑé ×Ñ}½¾oéð\x0017Ké\x000c&t=Ñ©\h`Lôy·<Ò
Ù#5µÞjú^Ý%í»	![¢â è,|S/Ë\x0005-MS;²§J*4U£©>4_°¡\RËfÉøâÒ\x000e¡\x001aÍt¡¥\x0006ñ|Q\x0005Nv¥*Ø\x0008\x0008÷X­-"³S¡ÙÚí9ýzuûã¡\x000bªø\x0019°ÞÇ¬@ÈMÖ ?ÔÜ\x00158}wrþbß)ßÿâ~úñóWâJÏ¥]åÉÃÍíÕçäÃjòa%"ýrÿê\x0016Èãàa¿-E\x0018¼±¹\x0005îQ)Ësù¾®­<yv~òjoAt\x0005ßÎüY°>þr÷õ£þ¾ª¡¼:z}wscôs42¢ÿn!Ðh§9t\x001c|nïÆÂ7nSA³£×\x0017g§\x0018wëå÷7á¿~5)\x00172 oîA,¯¯î?ï¥\x0008Æ¦H\x0011 wÅ\x001aÓLá<\x001e¤xs	Òx}rùê:&Óÿ}üß\x000fö
ÿwÉ¿Îñà¿\x001f=â\x0002ëâ=ý÷äâÿýèHU1ÿ\x0015ãë«\x001fî¯¿îý\x001a\x0011ÞY&Ë\x0001\x001e\x000cTÚç5ÍH³áDu6ð\x0012½>9ûöòôÝÞ3QpT£\x0016âÈ#K#øaïÎ\x000e'àèh\x0006qLc\x0016â(ke\x0000GòYõÊh:«ÂQ\x001cWã¸8:$ÿ2á8þXà©°t¬\x001aýX¡Æ	\x000bq¬Iuø	'\x0016é\x0002F\x001cëÇpø¿²Xz5k\x0016¥D.o\x0007\x0018\x000b\x000fWvó4gY.=Ìàlk¾[*W¥×\x000bãQñ4gY.:Ì
ÿs8w6ã\x0018ª.Æm\x0017»«.\x0007yÃ,\x0017f«®r\x001fy<.\x001dr+%òðK¼§9ÍrÑqV©q0Á\x001a!ohÙ\x0010Â¸8*âêï\x0004Ä¾þLð_né	¢\x0013td&D
Ù¯§Xj!\x0015\x001clA§Zª¼

»Áø«ajµH²\x000b±ûÅ7»i\x0003\x000fhJÿøýÓOW7\x0007
krÑ©P\BìTX]ÓÜ\x001bÿ\x001eMêéó'gss\x0010*0U©.0oãq>VsÊ1t#ð«\x0004æ¹©ÑLÌbõ2£\x0003\x001aÂ"3ëÐ\æ:¥{3\x0011
,K>õ ö\x0018Í¸Ud¡&\x000b}dN\x001eKCd\!\x0003\x001fTEF«¤VY>¼\x0004¢\x0013Î³»\x0002ÿ\x0002mô\x0000E\x0006Pj\x001fÇà§·lÞoîáßþüËÕÍ~?Ø¼\x0004\x001eï#.ÝÉB&âT¹¾¹|uþüÕ³}ïÇ
JÕPj9Î[IjÔCíÑ\x0014±"sa\x001cJ×Pz9\x0014¶©æ/µ 6!,æÏPªl¢\x001f25Y\x000eeB1B\x0013^\x001aö\x001b¼ÔãL¶f²Ë¢9ÎúÞàê.²BÂ\x0011*;G\Íä:d®3\x00069\x0005A=ï\x0000%Éá%á1\x0002åk(ßq¢dn
\x0004 t9QÁ\x0017 W@\x001a*t}½Hw/8* ð<\x0000\x001d%åä0T¥BQK.*C\x000ei9 ¨ØXËq-%\x001b-%;ÔTÐET±<Ðe\x0014,*eÆ¡\x001a ;4\x0002 ÚgÖR¬:¥±n\x001cª9S²ãP&´"UPü ®NP	b¤Ts¦TÇÂM_úOº3r´\x000b^bãÊSµ¦¯ãPEkdJ{êÍ®ØÌØ\x0015JA5§Ju*lúËv\x0006×Üy¦*²òÓðF\x000fU£ÔÕr­\x001ee¡Âî\x0011OºJ;Ö~¬Ã®\x001fö\x0008®^Ì_Ð\x0005K¯0£\x0019\x0013ñÆ¯p^§¡ªS\x000bt¸\x0002ÀcýI9\zÅwS6åzà"¸¢1ëx'MùQÑ\x00193R[\x001e!KÞ¬øÈ7["8\x001cåC~8\x0001!	ÎXü\x0015².6tá³Ã\x0005Ê\x001eèÂÓG\x0015¥kpmòQM×s®HxÈR~\x0003wÁðóbÏüý>\=\x001cýn±ðDnpE@§¾¡\x0003mÙa¿ðö&êÞüºéõÝçÛ½)!|)ê\t-¸\x000bôuå=\x0001ÂtÐëWç\x0007A\x0006\x0003bRå\x0019+2;÷KL#K=P¦2ÿ\x0005%ìäã	»/½ïÈû\ËXÒGpäa.\x0013¦\O¥d+0UíÉcï\x0001ó"÷±`ÀËP÷õ´âÑGì\x0000Ó5î\x0001óØ\x000eO!%åJàÆ	>]VÙ\x0015`¦\x0006Û^ß÷ºVia&á¬púZ³Ö\x0014\x0006ï\x0002³5íRi}"YÏÚè\x0005{ùaúí\x0002s5ëû}\x001f­\x001dG\x0007iL

»J¸|Íå{¸\,¾\x0005¶-Òø¨­å\x0017È4yÙ\x0005\x0016j°Ð%00:7ÔFs¨K(~\x001a©\ó%c
\x0016»$¶Ó\x0016F\x0004®\x000e±¼ÙJÕ\x0008lõkuF\x001fçOÓcË÷\x000ek\x0004fÛÔ\x000bÞËIkÃS\x001fTú44}PÃ
\x0018Ñ(´\x000b\x0007Ôÿ\x001e¢édÈ¿¶\x0003Ýúék
"ãd¹ç%¹!¶ßvî^\>yPfu\x001b\x0003a©\x001e¬¼!c	^bá;cÉ9ýº\x0010K×Xº\x0007+Æ\x001c6&YàJwÎ\x000e\x00079÷	\x0017bÙ\x001aË.ÆÂ$ñ®\x001e$O.òÚ\x0016\x001fúþèAò5ïA\x0002;ÄU\x000fpØe6ÚG÷sJb!V¬±b\x000f;,§&\x0003VädðÓ X\x0007loáòk¨pILá
)ÅRÆ±\x0004¡õ¸´dsÜåòóApcCò\x001b(Òð)oµ³ü\x0006+¸ó.{\x000e<<¯KÅ\x00118ÕäàÛÝÛqú4ëÒ\x000eÍ;i]\x001díÂÛH/"&\x000eÑ}´åBÊq8ÙZ!9Ó`÷¾7ì\x001fª¼±0ëûâ¸â"~:\x0019¦\x000fÛP5Õ¿¾»}øùúvmBH=t9©íøVJ.uáá~\x000fÏµó÷¯OÏ÷U(ïÓ¿hû\x0003báj\x0017üßW?c'ïóûë_¯ß]?ä¯LnlJ\x0003-ÿåËÃý¿|¸þrsxØ<ç\x0005-Ð*Ïå°Þ\x000b^}¦õn^\x001amyôöýåÑÓ·g§ß¼<y½Ï/O?\x001e=¿8}¿¯/Ñ|÷Ëß~ûùïÙp~ÿ\x0011\x000bY?VisóäÇ«¿]/¤¶^ñR<1\x0016yX/CäyÓ¦Ls~D½\x001bÈ
ÏNþ}ßÇ7[üü]'ÙùÕ×Ïw·9Ð²ZEj×Ê;®Ò\x0003\x0006øyÿ»n7FdJ\x001bËÎOÞ½º8ß\x001f'ªU¬FA¹\x0004\x0004­e^\x0013n]¤5æ\x001a[÷6#Ö5±\x001e&\x0016eH5\x001e!\x000bYÒ¶&\x001díÞÑMljbóÏ c[\x0013Ûab©óº.ÀôÙ¢y\x001f,x×o½Ø×Ä~X\
#dko±_,\x0014a7C\x000e5r\x0018EæA[,\x000cé8GOQ8\x0016Îm'äX\x0013Ça!ëHªP«å\x0016üÉ-\x0000Úø­ÉÖ²J\x0016ÃR¶ix\x001a\x001a\x001f©¢ÚbA\x001c\x000f/5Ã\x001b0·fdØ¤îw³5ù\x0005	'Còõ\x001d\x000cÙX\x00119lF\x000cÎ%Íg\x0019u\x0006)[>\x0019Áì\x0006T®fn´²\x001cVË8HÓ\x0012²Ì{l\x0001¹¬;ÐÛ]?Ùhe9®A\x0019ç1åÖ\x00199ÏlHÂn\x0001ÂfJJ¬Ù2[ÜËA;%¬În\x001cd`ðè6\x0003n\x000c\x001c¶$\x0018\x0017¤\x000e\x0017g\x0019;Å'9ªÍü\x000bÙ\x0018\x00129lI¬´ÔÁbR!ËØÓâ\x0013\x001fõv
®±#rØ\x0018\x0019Râ\x0019e¬|Nî¢«áøòí.j\x000c\x001a6$6/NBÆ¦¡å¬"ie¿kj^ÏÜ\x0018\x00125lHþ¡rn\x001f$Ã¦ÄjKë:AÎM	<®=ËÙlfJTó$QÃo\x0012l®#%çp¢\x001a9\x0019Â²/çõf.¾jÌ\x001a6¸%)ð6\x001dqLbvÅ\x001cÃvbnì\x001a¶Æä²îä1SöÆ2}tãvÌýSãöÏÛ²9KcArRóqÞÎ\x0004ªÆ\x0004ªq\x0013\x0008GØN\x001cÓÂÇ63\x0007§¶;ÎIQã&Å¥@öó³ªó8Ë®øùj+fÝ\x0014=lR(ï)\x0013}\x000ehâ¢qÚ#D7ó5tcRô¸I	\x00196Pm>ÈÙiÇ~ÜNÎIÑÃ&\x0005+\x0014\x0013b\x001e\x000c\x0004r¶Þ²Åf¦[·Q®aÂeõÌu@À\Þ'>lçëëÆ¤èa\x0013L\x0014ÉÙS3	0HúÙíÞÚº±)zØ¦Ø\x0018SaS3\x0007ç<ügølí^Ûº±)zØ¦8«Ó¦#³£¹þÀëïHÎû£ãÝÌMÑÃ6ÅáöCÃí¦gÒü\x0014ô>l'çæ]¥ßUÎK¶Ý8¾Ae½¡©cëPæ¤¸±zØ
¢÷©\x000cIY\x001fÓa6\x001c9ò~»· i \x00197ÁrPÃàøþ|0´Qü~a;æÆ\x0008a#èL¹eRt\x000e(oAc7KôÆ\x0008q#\x0008[å¸\x0006\x000eÍÙyÖÔV\x0000ÿ4z3¥a\x001a#h \x0003çÙ]®ÂûÇQÅT)²\x0015rë\x0019·.;t"ÍZxÒpNËÍ<}ÓX?3lý\\x000cìÍávéHÏF~ìvÒ®gn¬\x0019¶~^ùÔîB3í²ÓsÃÎm\x0017 0õ3ÃÖÏ\x000b5\x001b\x0015ùáª½b½hµ\x001e¹1~fØøy¡øq¢­¡<«×Î8>Î\x001b\x001eÆüaó\x0003þø8KjÅ£!9l÷8±ý³Ãö\x000f| <
uÌ#¸Y-qÊoÇÜØ?;lÿ<.Ê\x0011æ$èAeÐ¾ff¿kd\x001bûgí÷©N'â\x0014ò\x0006\x0004÷Ý0\x000ec\x001b[bmÏ\x0003\x00133ÈWÐ\x0004GÚÙZ³Ú°v¶ÃÚ9}OÌ¶0[ÁqE»á\x001bPí*Êv¡òTRö§Ãÿ 5äVôk´TýP`ðËo@Þ¬oÈ¿¨êµ?\=üöõóíRÇC¬ébÉ±S¾\x0004dü"\×÷áäý¿½{µoIh«j\5k\x001d×jXÝAÆúÓëu3`]\x0003ëQàH\x00131ºoË\x000bÅ²3\x001aÚoU:M
l\x0006ÑÝ 0¦\x0006\x0003ô6ÊÝ;PqÔkk\;ë):ghprèøÂ	·ß\x0007íäu5¯\x001båÅÐ\x001c§á¹¤Ä\x001bÅ¡æpèÝ	ìk`?
\x000c®%	c	\x000f½¦"Ç^Â\x0010W'o¨yÃ(o\x0010¥ÎÁÙÜ\x0002\x0002ö¥ÊO\x001dÈ§u\x0002Ç\x001a8\x0002ëÈq\x0017³I³¯l$çÒdÜJÀ²µ\x0018£&Ã»\x0012ÀH\x0012Î'Â\x0010÷GÄ;\x001b\x001d,G°÷ñBØ\x0008ÄGËSAåFÀRÃZ-´±#\x0011³Y6±hµ2yb=p£$ä°Àý,âo\x0012"f3gäþH'qsëäèµ\x000b 
8<Ê\x0006díØ§\x000fæOßG¬{§Fï]ð®hb\x001c.M\x0013;â¸Õ©PÍ½SÃÎ\x000fNçæ¼jZ¾ÜK'9¤\fk®'n.\x001a½xÑ¤Tj~zD>\x0015Ø1ËO\x000f³T\x001bÏ4[V¸ÍµS£×.ºÀñogÔqÈ\x0002öc\x0016!º¥ÞÄaÜæÎ©Ñ;÷\x000f<\x000fº¹szðÎ)å-T\x0001¶ô§YX\x0002| (Ô!`Ý>6þ	.n.\x001e½pÿHâæÎéÑ;÷\x000f#º
m&÷Ç?;3z@M@%{AU{a¿_¡\iÙ	ý
vÝÂR#½ïú©i,EÕ½ïWGßÝ_ßÞåüe-\x0003¦(\x000c\x0015§b¤Ãìn\x001dñåéùÅþ\x0002\x0015¸ªÁÕ\x001apx8C¥2M=%\9©z6uqë[¯áÆ´5É[R9Ov8T62Àmjn³Û´8T1»$Ï·OÝÈ.n[sÛ\x0015ÜØÃM~³2\x000fÜ¶\x000e\$ÎT:»é\x0001w5¸[\x0003n,7ó\x0018ÞM\x0004à%ïû\x0002¶\x0004÷5¸_\x0003\x000eçZRò]*î6Á2PJòÄ\x0003Ý^\x0003à¡\x0006\x000f+À%ÅÁì×|7·\x0007Ê\x0007Àc
\x001e×\x0003-;à6^û])}wê@ùN?xÕbÖG¬!·©\x00137g×\x001cUþ9'X­Øx Âr@ämâ'ÙÎzÀ6\x0017;ó©ó$^Pç¥
0\x0003\x0005ü=üÂLì>höÆîã\x0016\x001føÐF£Eïs\x001c(Aq1#©\x001f^ê%rî\x0016 ã®óó´÷èIzUÓ«ô!rM¿uë¶ÓI§¨Þù1|]ãëø\x0006Ãd¹º?pL\x0012|F¶Jtd\x0017½©éÍJz_èÁ4Qý¹\x0013¥Bn~tlMoWÒkSrÒp\x0012Æ\x001a_:Ìqõâ»\x001aß­ÄÇª\x001a¾·º©=}¾¸ak|_ãûøð¶£^\x0013#\x0017{[íCöä\x001b©\x0017?Öøq%>6¶p­ºá¹(öï`	ç¬!üº£ÝLÌíÈá\x0017XÌý\x0001Ä¿+õ
[ß]Ù¨}¹Vï+QêîáSÐ\x0017«B©\x00072ãÛËßhN¹RubªD[\x001fTIîD®è³K\µ.üF÷ÈÊ\x0007§ÒñÁå©Ê¡\x0002]üã6üWí.\x0017óý	ír¡F96óñúþfqt\x0014ðÓ.Ã(qØå±H/\x0000'Û-+ìþ· Í4Ê\x0011g§guli¬jdõO¬kdýOlkdûOìkdÿO\x001ckäøgF\x0016í¸êüv$Û×£\x000f_¾\Ýÿ°PÝaË\x0011G½p+!uáâ
çÖÃùµ4´íÝÑË÷oß\~{HYÛFsz õ\x0018º\x000e\îîK\x0014!q*è@Qâ\x0008¹«ÉÝ*rã¨èÝãîk\x0002·y6â°wÛËíkn¿[inctð$%nÅ!ÌMÉCM\x001eV[É±Æ\x0000gBüG"/ÃÐ7B5z\'txî/Î"÷|Æõ\x0013E\x0011Üµ+nw®ø Ìó\x001b.UgG\x0016øSu¡½à^ë\x0014\x000bf\x00022:V·Ò<\x0013z<\x001b\x0011\x000fLl\x001a!×
¹^§\x0012ÕN%º"uÍ­)¸ò{SvÓ°5ìØ¡)\x001dÝr%±2OLx"\x001d0aß_$pÛÛuBwñÆA\x0016F°ZÜúÀ4
]®ÓèF°F÷øXcvË]m{^\x001a.W©ttW4©t\x001fÊì\x0002M-Mf·ão\x001bvÕ¨FµN5Æ¼'\x0007Ø#\x001cûÏðFiaÃÅ¦'F5þ¢Zç0\x001aÃ'&¨Òd(-åwpOäw{Ù[qbw \x001eéÈD«ù´+*ýÇ·ÿ¶èfWë4»\x0015GÂ\x001dF¶80µã¶Þ®j4»Z§Ù£æ\x001dÑÊÒäi\x0003ßT¿1{£ÜÕ:åîËä\x000e\ÕÇC·"{\x0003Ré.«ô${óÊP«\x0019\x001e×\x001cz»8¦N\x0017ïÊq"\x0005ÓÞØ%µÎ.EÉ	ßHÍªJú¢\x001eý¶ê±±JjÝC\x0003ûãhHb\x000c8ô:;ì©¦Ïy½yh¨U/
'4·ÂD­Ëô\x0014Má\x000bü\x00176}lèÆ¢êu\x0016õ\x001f,wÝT½Ê¤by\x0017]S\x00130uDoQ\x0007æO 7\x0016U¯{*ý£ÅÞ%½Ê,aç\x0017é\x0018t }öd¾8\x001b\x0006b,ü£fO?¯zu´\x000e\x000f%Szù©Ç\x000eu ¸\x000fÞMC\x000eC´ÃàõÝÃ
®2ÀMI·GÏ®¾,>ó¢äxAø\1x]sïØ{phÁë÷g¸ÎàèôüèÙÉ¾%Õ_AÕ\x0005µú¯à=æJtÅmbÚKùýä"î¿®ÿ\x0002zý7+µ\x001a\x0007¹óm\x0019M½?S7ú70õßÀ¬þ\x001b`®¢×\x001e{4åªuy¾ÍO­ÿ
výGÀ®\x0016ºÇb7²Ìñ8aã¿B¬ÿ
qý_!
lM/ÜókEÙã°¿^cð¯ [u´^\x001fá°\x0011jÜñÆ>öèy´|Ø_\x001aÙÿwS\x001a+»Pß^}¼¹»]
¯qÖ\x001díÑì©æZð\x0008¨÷O
(Kaà'ÏÎ.Î\x0017«\x001a\­\x0001÷¥7\x0018'ZEÛ.y\x0007AÔâ)©w\x001aÜ¬\x0002·Åú\x0006M3òá§r\\x000e4Û\x001aÜ®\x0001\x000f#O^ðÀ%\x0017U(\x0011âý\x0011pW»Uà\x001f'^\x0018
÷¹ÈõÑîlpûÛ¯áËy<¨úÀ«	
¸ß?_`\x0004<Ôàa\x0015¸ä"B¡ù@à¬Õ\x000fíl\x001a\x0000¯3O1eÉÍnz0üÄÛ¦¢³¦èò-Á[5¾Fã\x00056BÖ\x001fK³ã\x000c»3øìÜ\7äz
¹,S4|EäÞQÈ\x0006\x001e\x001bOÛÃÚ·¯{Ñ+Jcî9w<\x000c\x0006Ì\x000fW?\x001cÙ¼h×lÅ¬jæ=«¼$CYja5\x000f_±t´==±d9´®¡÷¬ù^$ãªÌ°_ÞðØxªW~9´©¡÷¬\x0000_&éX6[ØPª\x00068ø\x000b¶ôÉRÀÅÌ¶fÞ³\x001d|Y¢`×ôà5ïîÚ\x001dõ\x0013±Ó\x001ef_3ïYÐ½,á\x001evÃ*RB21\x0007®ä	Ú<Yòº\x0000ZNU¬j§ÿôÇÿûõúêa©Â§2¡Ç¿Ø\x0011'Ë\x001b¿<ywzòþi`U\x0003«q`A\x0007ÙÓø\x0012Qày¢§V×´z6Òü;8hiç!<þ
ï%65±\x0019&Ë\x0016e\x0019|\x0015èDØ]ÏÂf"¶5°\x001d\x0017±,\x00118Uz\ãÉ\x001a>\x001eÊÛIìjb7L\x000cj"ò(4[É\x0018[\x001aºÌÅ-&ö5±\x001f?\x0014ká-N¥UjVZ~ýTFe1q¨Ã¸ËF\x0008ìÛrtµ/\x0017ïÉÜÛÓÄRO\x0014\x001bøu\x0018!Yû_~úüãíßÚ\x0010\x0013¸m%FQ¼"\x001b)¢¤|ú\x0005fäâòÍËW/Îÿýi|Sãønçúñbæx8Ï±h­ïrzWÓ»µÂ\x000fWÃÅ Psç-M0Jì<=\x001fjü°\x0016ßÙR \x0000g\x0015Áÿåì<ýÔ]/ôÔ	Ñè¼úù«/_\x0006½§hÊà,kK\x001c¿Ì«Sû#:¯^¿9yûv±\x00035½¶"]Û5ìræe.Fò\x0003LiáÙÜû\x0000\x001b×5¼^\x000b¯8îm/ð*ØþÄí\x0010¼©áÍJxxùÒO]º´\x0015EÏÇ½G~ÝÖìv­à\x0003\x0017C¥ÆnSTØ_§0ÄîkvÿÏ"w?Õ4~oÞöåÕÃ×eüJXI¹\x0006'\x0005ïöÁÒËÇhiö:º3'ïß=ýÐõ_b_â³ç/\x0001×U§Ù:NÄÀCu\x0003ïD3ZìÏ÷þ%>
J\x0017"ÿ%aZÄ¿Åý\x001fÿýëõÑó»ëû¥	Oçhñ\x000eöp¶ÐÑé±ÊºýnÂåéÓ£ç\x0017§ï/©6úÓÕ\x000fW_¾ÞgPýýÃÝoþö3\x001d\x001a<*gÀvýë5JUS±Np\x001fï>ß"v\x001a»Uá8\x0004ï¼9÷\x0007oc©'¼¤ÑÙ£Ï.^s\x0006\x0008\x0008²O^
\x0006¨~µ\x0010Ã\x0014òE\x000c²»G	£4-÷cÀ§Òÿ·0þÓúßn9w:ÿ»ëûAí\\x001f]^ÿpw»Å\x001aö\x000f \x0013.wv\x0013\x00153\x000büQÖ,ß^¾\x0006ÅrztyúíÅ¾±b-P5\x0002Pøå\pRCÆRæ8m>6©Ô SÙ2¿¯ê¿þú7x`Wg4Äó®þv÷õ\x000bêO?]ï§Â\x000c)Æ÷ðSíÆVAÑYZ\x0011×ÕÔ\¤\x0005à­óï\x0017ïÞ¢\x0006ßìÅû1>ü×Ç_ÈïFoûìúËÑÙÝí×W÷?|Ù\x0005/Ú\ö\x000bX \x00192\x0017ð\x0018ÀA\x0014\x0015mû\x0011ñÊ]¿8=¹üv_\x0018]ÿ×póéú§JZüñ¾\x001c=û|ý÷ý< p¬Ó¡ò\x0011xòî\x0013P¡9gÂú¹Ï÷öèÙ«ÓÿX\x0002\x0004ÚÂv\x0001¹cð·\x0012
ä\x0001
\x0004$KÞ¾\x0007èúoÿóêîÿ©$¯é·Wo¿þËéÃ×·Q>ºñ(áçK¯	\x001d\x0008|bM¯æ·'¯Îß\x001d¾qz¾ÿ\x0010UL DÂé¯÷ÅU}Î>_?\x001c}ûùk*i»ºùõêþ¾ÄhS\x001a«\x000cÊ@´\x000e\x001d¿ÓXÚ\x0000#¿Íñ~uúþèÛWïRíÚÉÙËý³B#;Ò&£J\x000fòÖ5\x001fsðç#q9\x00137à"ÃÒÅ\x0005¾KjñBá)f4ðX2ZmM¯ÈÐ\x0019É"\x001a¡@j\x0018ÄHR\x0013b\x000b´¬!:ÑÁvìü5#ÞLh8»>¨\x001b>háÓÏ\x000f?¨\x0019mzôìîÓOW?\x001e¸NÊ¼\x0014&ø\x0008\x001eb\x000e\x0008\x0017Ãdõ\x0015±\x0000iÎ\x001c>»\x0000ÓóbÿÅüu×¾¹ KOnnî>ÿvÀ6ã\x000cî¬%\x0014|@§m!\x001f­¨7Scsrvvñêßöbû_\x001e®eu	lÞ}¾ùõîÀ'\x0017u \x000b±sò,\x0003
µÇ©\x001fa^2ï^}¸Øÿµ>ýøÑ}úÚøu$\x0003v\x0018\x001c(ó½dð©¿
Ü\x0003|N4o=u·Áëÿå¯ÿUè\x0005Ö\x000e}líãz))À§"wÀ)?ÅHvn\x001fÄ­¿~ørÕúüOZ\x0011e>&ph\x0002\x000e­ÎUxh§.?Ö}\x0018¿þö\x001b¼bjÅ³Ä´ië\x0001\iË¥çèH
zyTICÆÈ>ä>\x0008÷õ·[ù[ûðØúîÎç>ß~ùíï¿ÜWç3ß\x001f\x0016R¸¾\x001a\x001et)¸\x0000(>z¾ÀzÆ;ûvwVó»0ý_¾Àíü\x000bvÞÜÃåúüK^Ç´ï°à\x001c;
®×Ì\x000eìy³æ§®ÇËWçÏ_½Ù¿t©âR5êáÂ¶ô|Êt@¡'eçf\¢\x001e.]sé\x000e.l\x0008éDy\x000cftô\x0011Í:0S\x001e0¸ëÆç\x000f	w/ïI\x00050¥H\x0007®û¶æ²=\x001fR¤ìe\x0012åÙ\x000eBEÌæ&*!.Ws¹®\x000f¹â%ÉÂ¤Þê$/¿ê;+ôp)q\x001c\x000b\x0004Ì}ö\x0019K¬á¢:>V\x0014¢\x000b,¦4	yL\®Yo×5Bö¨
PüÈT!PE\x0018ÜåÉv[È+)»î¤M£*\x0010\x000c7O\x0010X´¤\Ó\x001a«\x0015`ÍÙ]\x001fLËZ\x001f_Räpãì´|'mY¢4\x0004Ö\x001c~ÙwúÓ\x0016¬^#mèS¦\x0015«× V©æø«ã\x001fBr,\x0013açN´N&É5Lµ²ËRzö´¼ÔºlNt\x0013\x0008f
YsüUÏñÇy\x001b6_L\x0001¶TD¦¬Y¥ûwÓãÃÓ\x0017*\x000eö¦û)øElØ\x0000(±Nÿ±u2>v|S§S"¾iA%´W¿i\£9íªe»ê¹\x0008|j¸\x0008%*¤£c\x000fH®R\x001eÀö©eûÔÁ¦#EÕ±xú'\x0004VÃ3\x001cól=Ù-ÿbZ\x0018puôæ
þ#7O}ØDgÀ´§ü\x0003~U\x000e\x0017[×ÒÕ\x0019Å£7'çï1kô4¥ª)Õ\x0008%\\u\x001dÜ\x0012Zb(rËX\x0002q\x000bN]sê\x0011N\íÈç
X\x00198âÇØD­I_\x001eÑ\x000bG2¹p\x001fù±'±Xí
ÜÒTpã	õ\x0019üâ\x001bü1Å.Þ\ß~\x0000ìë»û«ÛO×7{I
x\x0002\x00116HêE \x0003Ãýé¤¦ÐÜ$ñæôü\x001dü\x0003h__\??=;$Y?½O~×(ÐÂÞ~ýxõ÷Ï\x0007b
>
O9+
	\x0016PK¹Î¼a¿\x0000¿{vò\x001f{×õTÄª&VÃÄ6/í\x0008TO&CZ0]|äæ\x000c#ë\x001aY\x000f#kÅBÖ\x001c3\x0019U,dóÈý\x001f&65±\x0019&v¨SØ\x0000#IÈ¢ÊÆ»Gj\x0018ÙÖÈv\È³Âh[óÎB¬tó>0Û\x000bW#»q)+r¢wt$!»@ÄÁ<ò>}Mì×\x0008ÙR\x0006×ÓÓ¹(¡I£Ü#Ço\x00189ÔÈa\x0018Ùç\x0016b@\x0006\x0017æXC j\x0001ë\x001e¹ÃÄ±&ã\x001aNq"LÉ@õë2XÍJÙ?z.\x0012W1
´"b\x0018\x0019gç\x000cB{2
rº
öQèe¹µ|ã¦O9.iQp¬\x001d\x0019\x0012é9ß\x0018\x001f?±\x001bÛ'Ç\x001fY>-5Fº¥±|õvÀåã¦\x000f¬µ¡³¬+C"U\x0011òfD6¶O\x001b¿ (â4\x0011©2s4¬1üvzY6ÆO[?gÓ\x0000@säA	2xR\x0019ÖèíÄÜ\x00129nK.Ö/õå\x0011XeàR­\x001bÅ,Ç5³\x000b¬5N·d)[fvj;câÛ§\x0013ZíÝÂ«nrãR\x001f\x0003\x001aîhYw\x0004>Òs\x0011èq?¿$OÿjØÛ\Û\x0000o1tH³·¡Cq7³*Â¶Ôv\x0005µh|$r82ÅGZ¬>fFýâk5æ	ø\x000c~A)î·W\x000f7éúùÓ¡ìn@WÈä0ÇPI/+m=åÛ«¥Þ}{òþ,=P_=?PPàT
§:á¸Ø\x0014ßÐ\x0014Â\x0003\x001b--ÃI·\x000eN×pº\x000fÎXÒ\x0001Þ#M\x0011TA\x0005J`-©áL§äJ\x000eÀ\x0007Aa\x0012¥\x001dÇ\x001e0Cl ±öÈá/ªñ\x0004X¡~ôÝÝý\x001fÿß!:	÷$\x0007Ê:\x0008[©(Â\x0008ÚhFã§\x001aô£ï..\x000fÔ\x0012\x0017<Uã©^<ãË<2ZI­(ªý8}ÒI§k:ÝK\x0007ºr\x0015\x001e\x0007óäK!-'©áA³ÏÔ|¦ÏsÅ#ü"wZIÇÂó3J¯ÎÖt¶ÎóÑsÕ,ácÐ(3®s\x0017«ñ\/\x001eØd\x0019Zªµ\x0001<Àb2\x0017néÂó5ïÄßp!\x0002ê¼ìÅÃ/½*:oíÍ
5_èåiuj¾\x001bfpà¿ÇÖ,Øµ7Ö|±ûó
^\x0007\x001c§éûJ.v\x0017vå÷­\x001eò¨Å\x0000 ÌÉ\x001fåÁ\x0001ù\x0000ÎÅT»ä×&\x0002ñ¨Ö·.µ\x001f.ÍdM·ØQ>¶?³\x0001qS{K1eÝ¾ÑL®;*(û=?ðRIÉ8g¨ÓB\x001aAq\x0008¢m\x00027»\x0006Ûò«'ùBÍ\x0017:ùplJ~\x0004x\x0007¶BçÚpµwÖ¬\x0004¬Î!
Pü		UC¨þLbÚ\x0011¾\x001eäòùçë¯ÿøïûÃù¤_rÙpQb1tZÎ;ß\x001f=õúôÝ«ÓËC\x0019=1Íâ\x0008_\x000fmY\x0000ç\x0005vöå¢\x0001L¦\x0008®Pñµt\x0017®Ùt§àOó!Pp£kÂJ®8Ò\x0013¿¾ÎÖt¶.P.ÁåeÕ M]ªfü.8_ÃùÎÏv%Q9,"àõËåõ6<X/£Ónr#´kÕòÓýoQ3\x001cÎçÊ4º´¿Áqó÷õÎ·Â¦j6ÕÅ\x0006¶ë\x0002-FeBf3ì÷yáGáÔTpÊUïµ§L-·T§ë{$WÑXÃOp£f=¾§¬¬L¹ê¶*¤\x0015He\x0003MnÄ&\x0001ÇÍ
aÎÏ{jjû®3ê§¿|N{V\x000f\x0014¨GaÌ.*`hºÖ+ÉÂ\x0000ìéWiêþÆ§j<Õ§\x0004\x0017EyE\x0005¨Z+ËÓnãú(®ét\x0017]p/ùá-\x001c=¼áÙÍ²\x0013«¢Ò5\x0003ó/Ò§½{øz-þí\x000fü~@·áÐG*t\x000b×½IgJªjºË÷ïN³¹?ÿö Þ¯'\x000e/';HX¼Ñ\x0002sD¥]C¥k*ÝE¥MV`ÊcQ\x000e4s\x0015jTäI'©ÉL\x0017YihI_ò}Q°%/)×¹ÌuÁùö\x001c:AQèD°ùjÒ\x0017Ñ	\x0016j°Ð\x0001\x0006ïÓ4=?¿h"¹\x001dÚzV¬ «\x001e\x000b4\x0019w9ÂH'µý\x0006jAÀÚkÒh~2 ¬¹²ç^F\x0005OÓ É¨Gê&ÑÎqé.Na]u\x0003tº\x0005é%½ü"\x0012$Æ[¦ñ­_Î[\x001cüªS;**;#ë´ðÞå|\x00154=ñ¥Twa.øìäíV^LÍ¨¨ÌèB:åpJ\x000e@<â\x0001èTIL¸¹ò\x001e:]Óé^ºPÒ&ÊPu1Ði¶ò¾Á~:SÓN:g¹+ÍKK\x0013\x0003q¸d®ÏÆÀ:èlMg;éKcïQ6\x0016¹FÏ`©
û +e×\x0006ÀÒÍ¨\x0002`Ë EæÆQìüuÔ%Ä>ç/aÔÓ«'Ñ¯«£\x0017÷½\x0003Oî\x0010`à>y\x001cÃK&\x00065\x0012ÚÎ°jÄÜÉÑËW\x001f.À{\x001aSÕj\x00003:bä¢;\x000b	q_n\x0019¢6ÊÔTúææêÓã±Z{«á\x0008R÷\x0007Ff\x001duW¨ònÎâ³çKfgUxªÆS½xá¦\x0018\x0018FÞ\x0015µ@¹\x0012dòmªl\x0000P×z\x0004\x001e\x0014
gÞ¨IÃ\x000emn\x0000ÐÔ¦\x001f0rõ=V~êÈ}wüC\ûm
h»\x0001A\x001fªQZ\x0014	ò¼'ª\x000cKÐO\x001bB¼­Û\x001f®\x001e\x000eLrH58J(u¾¾-<æ_Ú\x001fNÞ\x001fæÀPªRK¡B\x001aqp\x0001?jÁuARÍ×<Á$åTÈÊ\x0002?ï¯÷×?\x001f\x0004 |Ó\x0000òäÁ»â's\x0007:
3&\x0003\x001c½ï.O_/¢S5ê¤S\x001bWäíiÆwg¼0ç\x0013ôàé\x001aOwâáº
zdàL¨\x001c61Ûµà·si±\x001e<Sã^<ÅA\x001dx]Ð³Q\x001bÍq\x00130Çk¥gk<Û'¢áà¦ÓFçj£¸\x0018ÅYw´\x0007ÏÕx®\x0013Ïs1³ÜQ\òÌ~[Mçk:ßI]WÆÇ¦%\x0007g\x001f÷²wâ\x001a/ôâ	NÀ'Àé¤E­\x0019}×wo\x001bw9ÝÝÊ]^x\x0000=ÏJk0uÑ-»}PÝj\x001aUT±ii|8zñÇï·ü~ustvýéæúþÓ!o\x000fk¤y8§¡¯Bs\x001f\x00088\x0003j¾¹íý\x00110»<9;:;}~vzùüidU#«\x0015Èà`\x0015\x0007ZEmIùÖ{Y\x0003¬k`=\x000e¬=\x0003À#Qtá5	ØÔ¼f7\x000fÕÏ	?IïÑzôÇz`=}©hñÿS÷vÉu\x001cI¾çV°Å÷ñ	¤ \x0011f\x0000É\x0006IÝª'\x0019H¡$L\x001a$ëúénã¾ÎËtÏ,C;¹+\x0019÷\x0008÷8\x0011'ódD&»ÕfEÀT¿\x000f\x000f\x000f\x000f÷¿WÍo\x0000\x0007wÚwG
3C(\x000fEpU¡·?#"k§\x001cªVy{ò\x0006~ÆíöãÅ|\x0019©Þ¿¯hQ=:/ÄÛ²Ûí0*óWå:pÀ\x000bêfÔ5£\x001e\x0018HC\x0012^á5ä\x001bDQâ8ðàÖÍhjF3ÀèË­Àr+\x0010\x001c94pqX\x000fikH;0Ù6I 'E3G~ÐÃéæ¨C?¤«!Ý\x0000d©gV:\x0014%r\x001a!¿>A»!}
éû!½a#¤`Ý\x000e\x001d"3ê
\x0018CÍ\x0018\x0006\x0018Õ)"àL¢P\x000e®¼\x0008­-ÒÏ\x0018kÆØÏ\x0018í©;õ2MJa3¤ýRnÈ½\x000c»ZÒ£UJR\x0004\x0001\x000b\x00192kÑÂ²\x0007î<\x0003¬o\x001f[Vüî¹\x0017»$\x0005\x0012ÆÉgÑ@¸k¬Y jÿú­êë÷²0
\x001c<Ã(ösîäáò\x00051\x0014µùVrªóÞ$\x001bìnv;§¤Ya\x0015GBÁ>\x0014Ð\x0001§k¸\x000e{Óp%\x001b\x000b#xF\x000e\x001fÛ9·\x000eÎÔp\x0013ô&á`v5º\x0013\x0014½³&\x0016â@ªØ²ØÝ~ÖtuhìÙï¸%fr)|´.=N9O)E°à(Õ#`Zô¡PÔ³¿^ãvË¥ûÉ;ÒÕ!²%p_Yòëçà¹²R\x001fÎCY\x000e§k8Ý\x0007\x001bx°méé1è\x0002§\x000e\x000b\x0008,³5í\x0013EõÂS\x0002\x000cea×\x001e\x000c0.`3ûÑXÓDc\x0017i¹\x000bI%ö>à *
Z\x0004f\x001e,å<®ç^ðT§úñ(\x0007üAz5\x0003:
¥p0`ÜA§k:ÝI§\x0002Å¡\x0002j<ÒØyÉcg\x000e.tÑÎôÒI¡
ábÆè$'ÍCï¢]x¶Æ³xF±z1ê~qà=ÒEàp­e\x0007«ñ\'eç\x0014]<x
þEäFw(ú¾ÎïßÞ½Ø\x000bA¡\x00175ë<iÎ\x0016Ð2\x0014´\x0010ZfûRÅ\x0018Ð:¦j4Õ\x0006æ®Zi\x000e~è \x000bZ(Þ¦k4Ýæv£fJç]ãÚçãåhrß\x000eËb¯îÞÿz;­9\x0005T«ÛåB\x0017OÎÈ¯,®.=ûW\x0016Ã{GL\x0014J¿\x001c½âlX£¿VPX
¤k ½\x0014\x0008+O+_V,n\x0017¿>\x0003\x0002µ÷.i«{×²©·j\x001a(A0P¶\x0004TÄð@µw¬ÄÅw¬\x0005\¾$Z{MÝYËÃÖ_ý£\b\x000bÛ$|â¦631ý½n6:g$6Ýl\x000e§o¼æ6úä(\x0013±¿\x0005ã`î\x0006\x0017C\x0008®#©r7­øõ»ùQ<Uã
ån¨]è^sj\x0004ûj8+\x0001u
¸6wÃì%ÃÍÏ­\x000445àPî\x0006`»Q\x0000ån\x001c\x0005´5àXî\x0006Ç\x0016ëÜ
¾;\x001fÍÝð\x0017¢üEäVãÏo>ÜÞ|I\x0005CKúª9ê$&\x001dÆöúªé6íùÙÕùÙÛT/\x001b\x001dS5êÃ&í
Îñ,\x0000lú¢l\x000búÙtÍ¦ûØ¨­ujÁfNó¸yI¹§!î=\x0010ô°©ýIUõ¤Þ\x000eµ<"ýé¦å=\x0004x^·¢9
©jHÕ
©¤=ån9úTfÆÀ	íA»ö¼\x001dcÔ5£îfÛßiÖºMJz4)Áâòà"ìc45£\x0019`Ô]\x001dÆ m
iû!µ¢g?\x0007ÛE½fÆØªTw0~ÿýÑýü\x000bí¦?\x00182`_rLMD&ì\x001eoþéÙÃ¯7	Ðxi=
ÄÏ\x0010àïÄW+}êÃ°¤äÇÓt%\x0004\x001fæåó³ª\x0013¢cGò¿ì0\x001b¯«ÁÜë\x0015Ö7\x001d¤¿Vy®RøÔ\x0015Gz[D\x001fQ\x001eö
\x001bÊ½Îa\x001d\x0002ã\x0013*
&îí(­Öy(w\x000br\x0001¤üé\x0006çüæO?ò§÷\x0008úþ¿\x0001è;\x0004}78ói3or\x0014úÜ¹7Í}Üôg$ýùO?¤9ò¦þ\x001bÊ_ÿç}ÝB-]MÁ°¿¿½ÿwÁ\x000f·¿\x001fÅ4Ú¢E)ÿ G?\x0004Ï#\x000f*fá\x001eýte\x0005;ÿìüò
Þ
¯Î¯§ÚÛ7¨Ù@¡Âüç'\x0006\x0014,÷î¨Z\x001bG¨%\x0011e\x0013ÔÜqlpTñÀyT-EVÑ\x001dqP\x0015çGn\x001bÅ¡:¥ó\x0011FU+^\x0000Jj^\x0000Ñù
QsÛÁ\x0005 Ê¨ZåyTµ*k5Ê-\x0017\x0000|¶\x001fEÅÖs2\x0002´Ì¤\x0012\x0013²3©W[Îÿ®ïëÀü{¿\x0001ÕÈl§¤
øØ¤F°Äì&¤`Kâðú|ûÀg\x0013\x0013RaL
o)\x001b\x000fYÿAP,§e\x001d¨15*\x0007&aL-µøA5¦ßÈÖ\x0015]h9<ªØjÔÓRÕ¹*\x0013® II6/U©6d\x001c>¬p0Ù\x0000pí-,\x0001%yÿû-÷Ì.@Ü\x0005¤ûñÉ6R¹\x0004\x001cEÐ|d
\x0007WØLlW\x0010;AºÂxÈ
TENÄØ>Ã¦ÇMav .Áõ~bð\x0005<\x0011+Í&,/à(V[°_þåý¿ý«¨î«×\x000f¿|¼y\x0014ÎYM"¸>VÚ\x0004È¦`ëÆ+öå\x000f/Î¦²\x001b\x001arý\x0016Ò\x00188064°íMÜ$oqÀ×;8¹qÈ½û³à\x000b÷gÁ!ßçÏ¸øaëÏBÕ\¼þk©þ&ï~¸;\x0014¥ÂÜÊ\x000f·GÁ,æ§`:5yøË\x000f\x0000\x001fdÌ`»~;ïeùòj*é­AÜP-GÔ9¿\x0016\x00115µ\rØÅlñþý\x001cAÜ\x000bO-E41êS­(ª÷úìN{|\x0007O¶¼,¬FÜë"¿\x001c1¨Sçèsn\x001e\x0010bGºL¨å!0[y\x0016é½(\x000f¢:Í~ÇÇ<\x0007}§\x0011À|o\x001a\x0018B\x000bã\x00010HMñ\x001dé&ÂËµ0ßÆÖaeÉ¯Çvß<Ëb6TÖ/J\x0003¨`·J°\x000ew
":¼\x001ceÄÒ\x0016i-"_\x0006\x0018mH\x001dMÑèy\x000eÁÅ±^m´ùj4À\x0008Î/
] cô¸ ][GFW¤@W3Ò¨\x0011Âeb\x0018ÄõÙó5ZÓáâÝVS
\x001bO\x000eYî \x000cïé1;OáE\x001dh\x0018Xtþ\x001dhåÐ\x0000Ââ¯~@Ô«1É*Ê¤\x0011/)¨¨l\x0006\x000cn\x0019àÔ ~þ|ûPÓrO'/\x0016mTTÆ©!g\x0006;ÎÑt³Ù\x0015
·lðW/fcÇ\x0015\x0014\x001dÉ\x001dP°1T¾GçrZ¦SøøËPþ î¢Cx9T°IÖ\x0015\x0019æ+§´\x0017\x0012|k
âà=ë8TüøóûÇ\x000f×·?ÿ¼(d;q£E÷\x0015ó3\x0002ò¹Õu}þÝwÓ·Ò
nÏù[\x000cs»Q>Ê.{~H'f
Èbº=¿o!Ó17\x0005<­s\x0017s¸Ø«§\x000e>Môãíù|Kñ¼¡ÀiPpË7Ù¡R§V\x001eõÓí¹S\x000bé<*IÆL'v±r«\x000cá¶kçöàCÙ`w¼ÿÛ¿ÝüÃ\x001cÚºW\x000foÿ9\x0010w\x001f\x001f\x0011\x001e¬J.¨\x001a\x001dgkò%>;FT3¡¼zyýæü{Ì¸x1}NT´{Þi/­¡òªè%\x001d}bº*ã\x00067{ki\x000f\x001e»ïì/VýÒ¸.}zÿði[eà¢ïI\x0011îÃÜSÔ^# N\x001diÏ._N¥6Lì
,f
6¦þ\x0017È\x0014Ly\x0002µ|\x0014/\x000eÁcL·á_ÂÏ¿\x001eZ¯n\x001e?/Ø\x001d
ãñÙ¿i¥£V¸Ôþ\x000fE(
¶ÚËWg×oþJs~ÿ\x001alïÜX
æmJVK`âð\x0002U¸\x0019lþu{\x0001ØÞ±\x0010\x000c\x0013«Ð&'°FÌäwW\x0000\x0007cÁ=`9¦Ø=bX^MS\x0019Uî{\x0005#4¤\x0013?-\x0016íbKÁ\x0002XöÁsK5¶Q!\x000c\x000fØaoî\x0018×\x0007õø\x0010jãË\x0015¢7'¯oÞ=|¾}|¼;nÌ¶(7ÂzÎç¹N;: \x0014ÜK\x000e\x001eb\1zvòúìéË7ç××\x0017çG\x0018Pè\x0018ªHU5\x0017\x0007!«Õb\x0003¸)6bM\x0007n#ÙËjrau\x001aW\x000b\x00145r¨Eê©w´\x0005¨°Eêêªü\x00076Ê«»ü?\x000f\x001fcªà¨\x0007zõ0ýùúcñÌN}i\x0016ò5æÛW//^<{9Õ/¤ÂT5¦\x001aÁôC\x0005[\x0016Â\x0010\x001d§zìïáÔ5§\x001eâô)ë\x00149±¹$N~\x000c\x001d^NSs\x0011NUSÇ\¥\x0002ÞIæ<xííå´5§\x001dá´3'°ÁHjÛ\x000c9\x0018(ÑYÜbyº\x001aÓ

§MÕ[i85¥R4z9÷5¤\x001fÄ¾×9·+âv"NÍi(>l²BÍ\x0019\x0006S°¿ëTÐÚLõ5i<Õ\x0016K3Öq\x0004\x0013uÅòx46w$sZc\x0003ì<v2\x0001¥\x0014èÙÂ\x0011P<\x00084rú¡Æð+\x0007nÔTVO\x000fh{\x0014EØcPÐ\x0002\x0015ò4ïu8èy}J¿ÁúÍY$\x000e#l³\x0011h#\x0019i£UNì\x0001m\x000e#9r\x001a¡0[HwÿUÒZK\x0013ï¢ÜbâÃH\x000eF°Í)ë\x0014ÛìdI\x001cïÜb<ÃHF\x0012f;dÎ`Êi\x0004\x00068]iï·
´9äÐyEDºDµi
J7GÝÕ-8\x001bK/L=Í$ÙÐ«ÑJ6¡ù\x001dª1¡jÄ¤ð\x0014\x0016Èæ\x0016]h"¿\x0012-V¨jÝä\x0011Ó$ÃÎÖc\x001fO:\x001c'jS2jÞ\x0003Úly5²åeÈÓJ
<6?ªÁ>NÙë¡lö\x001aÙGÒ,\x0013\x001b>	Ê&P\x001dËW\x0017ÎëQ)Ð/W¤J\x0018­çö¡ð\x0002ÿÕ-InsIRusü\x0007Õeîû?§F\x0011\x000fwÇ\x0003ÎÃ½3\x0007P\x0019:¯\x0000£9&¢âÏüýË\x0017ß¥Æ\x0011//¦\x0014H*^]óêAÞ$ÃqXx:C:M¬(¶¤¦R6»yMÍkFÇ7Ts\x0003ìIy\x000e\x0006X:\x001a`-\x000eÆý]
ìF\x0007\x0018ûJÅ\x0012ïÌñ\x0012£¢@ìL\x001ao7p¨Ã(°×I\x0000\x000eW\x0004°kWâh£Ñ[
pu\x0007Pº¾\x0003t\x0002GÅ[ô^\^\x0012ÚJC:9cÌ\x0016\x0012\x001b¹g#l\x0002>\x001f?¼þòÛo÷ÇÃ¦)F\x0011r,ÅÈHEs\x0018ó¡´\x0001Ø³\x0017¬\x0017oN^¿}õêrúùªà\x001a×\x000câ¢\x0016D¾¶\x001a\x001d²¬\x0006:±]fO´\x000eV[³ÚAV¡
«1|Ó
QÝÖÕ´n#Ô\x0006Ömä$\x0006w\x0016:`C
\x001bÆ`ñàò\x0019l¼¥Z\x000fðm$ãû°
n\x001d\x001amh 7ä1"¯£vÑèÚ
JÂRê`S\x0017o#ßÿ`O§ôìÝ»ß\x0017DÕ#za|J,mâPyº\x0012\x0007ÓÚ¾åÙÓ§g~!.¨ªFUC¨xãÎ¤.Æ,MÇ&AO;â@\x001b5®ü\x0007SÚ¯G@\x001dêzÓK#Ê\x000e¤x\x0011Î2©\x000e²\x001eÕ\x000c­PU:!\x0005{\x0014Õé\x0017jþÒKh&ÕÅ]¤º&Ð=Fm¦ÔS,Ë\x0008ïÈ;Ðq²ä¯ÔÔ¤\x0013"±Ç<EãRm:º\x0005Dpj©â\x0015øIóÚCjkR;8¦1ÝÆpL¦Û\x0011Á'q;÷T¹\x0018ÕÕ¨n\x00085 äHöµÀ°f©Vðf
¥ßJ+§¯b=¨¾Fõcó/"gg\x0006AbL°\x0000(\x0003\x0012FUÉ\x0003«\x00075Ô¨alT±8ÙäQU^0Ò´T­¾÷Æ4
*Ìäë¢¢SÕ`UbÉE¼/v V.\x000016ª&7DÆQ
Y\x0015Þ·ò°é»m\x000fk{TU\x001eÕ{#\x0019+GoCF¦Ri\ý&U6g\x001c;¬PiX%\x001b^Tnóà0¯«ÓÑâ\x001eÖæ´cÇ\x0015\x0016Nñ!à\x0005Çc¤òÆ5èMXS@\x001d\x0003ÞêSÚZ°\)\x0012#â%\x0010ç]À¥¨i¶\x0015#\x0019tå\x0004J¤/;KØY'p)jc°ä Åé¬\x0000·Õª\x000cX:l±³Tc\x0005Ô\x0015Àò&o¬ÃªlVÚXf\x001d©ÚÏ­Q¢M¯úþöñ\x0011þÛE@\x0006\x001bF{J\x0004
üüê\x0002¥¥ÁþõZÎN¾?¿¾~ùâÅ9¦\x0002\x001dV5´Z\x0001-É}\x0005hÉ·XÇ¶\x000b\x000cä¬íêÖ5´^\x0001MylÖÓ\x0018d«é~ZSÓqZp¶(X¯a=Ó\x0008[®fX¿³\x0019³­íªeA«Âh\x0007ÁUÁ¹röèdv5³\x001bfÖq4(S1\x0017
´âºåé§~èPC\x0015Ð.õØ¥-pìÓYC\x000bZLÛ\x000c@Ç\x001a:C[¾I
\x0015è´Ó6FZ\x001dÂÉå»ð`V<\x0003×\x0001qÑ¸½½ÄØ\x001c%\x0003ca,e?\x001aË£l\x000ee\x0010·Éøi¢cIÂÜ8zàuÆñjÖ\x001b:Ù&rü8\x0001ß®\x0018Baâ\x0004íÁ¸\x000bÃ?\x0017dè¤n\x00139~è`ÊX+êfÔ\C+¤ØÎrÈæXãç
fqS\x001e¦W(¢.bc\x0018°\x001dus°ÈñEû@\x0017;ø\x0017q¸T;*SJ\x001dZ¶ö
´_1Ô|f¹kZRZHÉ¨ì¦VÑSãF\x000fîJôíÉ\x0005\x001dâAÒ³°vÃóÐ4©
Éajsê»}&K\x000e\x0008Ü®é±Â¹âç	·¡\x001dQûìR­×Z$\x00150\x001cx¸aqõSl\x0004q®<m\x0004×ìþ¯.O±È «§º\x0005iPÄÛSäëÄtúíSl$2÷¶bößV\x000c_Q\x0016Ây\x0011H¤D\x001aò\x0005\x0012\äKªÎ\x0007_\x0008§k8Ý\x0007'-üM\x0008É\x0003©4p\x0012|ºul¦f3lé$HlØØ¼¼RM¾ý/³5íSIµ\x0000á¬r¨eOt~ò&´ÍÕl®
Õå2S¹Ù$ @q\¬¦\Çæk6ß9©9¡\x001fá\x0002¿1I)(f§^9§¡f\x000b}l`áè¥ÎÊÈÉ&)l'Õù©Ð×Q¸°oãBUúôì×/Ë-éÆÙ\x0014E{l\x0003g\x001céà%\x001d&Z\x001d\x0016Ë/ßÏ½ý~ºaR\x0005ªkP=\x0002\x0003H 6U&PE¹\B¹|óå ¦\x00065\x0003 ð@Q#<;ri¨öÅRd8(/Ô
jkP;4¢¤,\x001eÊ\x0006Tqþ3EË9]Íé\x00069cöÕ¬Ð\x0019ØcÐÛÌ»¯1ýÈ¼;{ª(Äé=½vjo"gjÍæÂ-\x0007
5h\x0018\x0001µ¥ÚQ«Àã\x001diÈ\x0005\x0007EÎºAc
\x001aFÔ2W¦äÇcð\x0013\x000f
ÚõRVQ\x0014´ bh<-@) H\x0017 l\x0005Ã\x0001Á¹Z­å¤­­\x001f1öÆ©]@Û°Î7% ­ç\x001f6Æ^X{ã\x0004ßµe]k ÕcÙël¨ÝO\x001c²%qèÍ¯üûÃÏ\x000f·'w·¼ù¼$F¢X|\x0011ÓÇ²¾
FvØ´_á¾y~þò»×pµ¹8ÿñúìÍqfU3«qfgYb.]ql\x0013!IÇÔoÒÏ¬kf=ÌlPk\\x0000ÁH^ðkÛ\x0011ÛØ\x0013KÍg\x0013Ôb1Å\x0019\x0008YI\x000fð+æÛ®ÝÏ×±%_g\x0008Øä\x0004a¤çúÔ)ØN¾\x0013ô±¯ý8r(eÜ\x000enN\x0014ëóE;µsSö·9ÔÌaÅJÖ\+ma÷\x0019²o"Hv¾&%\x0007º«#ÎîòcF ±ÍU\x001ehk,iìi¯ø «ÂffN6fNÛ9¼éK¾à¸SòÊ¬¥\x0005­\x000fë¡1Ù3GÃ¯åèñòê\x0014\x000c@w»ÕÑ\x0018\x000e9n9,ÆÙóíàNNGv\x0010¢®íäky?t³
åø>´R*pSÔto~òvÑo;d\x0013Jµu\x000bÚEö9£\ðÃÀ¼\x0019Ídç\x0011rnR[ÈYÀfÄõ\x0000îsÃ´\x0013$\x0005$Ô\x000cXz&ý\{£\x001aa)výìáñãíçÏ\x000bb9XCÃ
\x0013ïÉ¤YoMð1Ó.i*\x0011È\x0001ìg/¯_¿y3\x0017Ü1ûù÷Fí×\x000fõâc)\ðíHóX[g\x000c¿ÒÌkÜ\x000càë\x001a_¯\x001cý ù¹F\x000b~ð5\x0000Í¯\x0006ó%¨\x0003ô¦¦7ké¹¬\x000fð-¿¡ZQ\x0012\x0019äÁÎgkðmo×.}O)ç`U4=8 N\x000e?\x0001O_oFñ}ïWâ[ÏÒÀ
uHIXÁ±Â²ÐÓ)\x0019ø¡Æ\x000f+ñ½§t#TÃ\x0013$X\x00139@\x000bþã±Rª^úXÓÇôzg6Ý\x000e\x0017l2ñùAüº"L}U\x0011Ö¿x"Ëcª'³ï\x001c[ãl½üÙ+í¾2\x001d\x001c\x001cÊaÄf6<þ}½_\x0019¯u|yuóåýýÍãÏK\x001e`aØ³\x0007,ä{³\x0011Zpi¼ôn2ïÕÙÛgg×ß-\x000065°\x0019\x0006mñ=±Æ^z¥n,áUûo>j÷æsûéäÇ¿ßÝ>.(ÖÚð¦ØNÔçì\x0018\x0017¦\x001fá_üp}öãÅùõlÍöþ«Ú½úô¡ªRÿ,½f-9ëdÔ©ý¨¶Fµc¨¥it\Ol­&hg
szH}MêH%\x0017À5²Q-ÅFzúÑ¯\x000b5Ö¨q\x000cUóUX*Q\x0014$5wsÙ¶\x001d¨²ÝUcÛJ(ÎWJÒ\x0013¾¶TX§zXm%öÂ\x000e#¤Ñ\x0018¹|@ÃuX\x0003¬m@?\x0014ª6w½£[2ÀÀ»kæE`\x0019¯Þ·®:´\x0005\x000f¯n?ß}¾Åt§E}=\x0014\x001c¼ÔE2ìz°l{Ô5ïw'Â«ó7\x0017oÎ1ßi¦ëCÁV5¶ZíCJÈO\x000fÝ©ÌíH|j?O­\x000fçêJz±MmV`cçc±}éë\x0005÷A5úHêBl+÷ß$.W÷7ïoOÞ *î\x001fÿþ¸Ð-#³¦¢<5$ï
Z&~p_]=;?É¸×\x000b8UÍ©F8á¶Mõ$J\x0017ï]Q­9ìîi½ºÆÔCÊw1m\x001d\x001a£='Ûbô½¦æ4#¨ñG9\x0002ø2DÓ.7­ÖsÚÓ\x000eqÊ\x0012°ð®Üø¥)ãyðÆßËéjN7Â)BÒ"Lãi¹\x0016G³\x0008\x0007ý^L_cú\x0001L\x0019ôn·;î\x001a¨wI¯(»3Ôa\x0013L\x0011\x0005z´R$,â£ºl÷CNÎú=*K¶ôzQ\x0012\x0019dI\x0007ûY@\x000fæÚô6æSØO¼^åÎ
	µ\x001dË~?(í¸\x0018S½ÓHúB\x0008DK\x001c+#<+\x000b©¢CYÆ\x00080ç\x0007ÂÏ:UD¨jBÕOh=é¸	ÌÛ\x000fRWö¹ôÓ:nË!u
©û!â×Q\x001dxéÑC\x0000XÑ1çý/45¤\x0019Ü%'À~Wüh4S\x0015³\x0018ÑÖ¶\x001fÑ'Mü4n©1´ö¥TQùzñÅ®tý®\x0005±%,ÕSzëy íLßbH_CúnHì«Í/ß,g C9Äçä\x0016#\x001a1\x000cL¶cá-|ånÇ|ÊÍtX
Y\x000bÔË)á²Lñ2kXÛ"¾\x0016gô6ÛÈæ¢,\x001býÓ?©4zïÄ\x0013NþrûñóÝÇëO·¿½?þ\x0010là²ÆÊ²`(O©Ë©RT9¦ÌÁ¾kÈúÏoÏ_¼¹xqrýòåëó\x001fÏ/çÞ°Í~\Ú¸t?3ì)\x0006\x0018ïõ9_\x001eÃd`zY×Ìz|!`6ÂÊ\x0003[§^ï\x0006MMlG\x0019{I\x0005_GÅ-ù¤®rQMWN\x000c@Û\x001aÚ\x000f³M"\x0011i¤±T6\x000f4½3Ê¨Å¤Tç\x0000³«Ýø@ÃMÏGÚÜeSz\x001bx 1~½\x0019´¯¡ýð@£¦Ø\x001aPæ\x0018
¬ï
ö#ÔÌa|q j_ \x0015-©âTz)ÊÌz\x00195t\x001c\x001fhî¡Äæ¤55¢Âd7~èúáv§ð;2ÔÞ³þ»\x0001\x000f.ÒòPÑo7Ò²=
ÇÏÂÔKAí6"501òF|©\x001d n\x000eC9|\x001aÉK2T8Ò:P5/¼²\x0013EºP\x000c@7g\x001c>\\x000c*<J¿;\x0011É~(îû¤&]¤\x0001èÆNËaC
ëÃ1´ÚnÀúà7[å'ß\x0013\x0006¨\x001b£'Ç­^È
9:\x0004*\x001d\x0005jÃî³S¢ýÔª1 jÜ\x00048½\x001d\x001dØG49ÑÒ \i¦VWù\x0001êÖ1\x001dßA$µÔ*I$jÏo Ø§}CcÝ¶kH\x0006ï+C6[r·ot«³¦¡\x001fw^ê\x0016gºôû\x00113¿/\x0018üÛÝÂÔ\x001ai\x001dÇöÃD£+Òì\x0007[Ìî$Ø^]\x001cK©!\Uãª?=®®qõ ®ð&µCÂÈ)¸{9i\x000fþ!®¢uÓº÷
íTðþk¯	\x0007º~^ªGT*P4ª°P\x0015I\x001cÂÉuDM$õ¹|sDÃì¿ô½Þ.dlÇêÊðRàÅ¼<ig¢½ÈºFÖÃÈà!yzDFJY\x0008\x0004,Ýt*^7r«\x0016Ç6¨\x000bÉ
ùÐ`oÇ\x00129^³Ì9¢WÕ5Øûäz\x0005¹6©µ[2\x001aBqÉå6¸z\x000bzÍ\x001e\x0003\x0017ûÅÂVÙúOïîïôýÁ\x001e\x000eÒCJ¢£\x000e(\x000e>­R¦ãÓËËÙ¶?b¿QØ*§}1£6"&ÀcHaÈ\x000bs×K\x0019mÍhû\x0019Áù1Ä\x0008Æª¼\x001cwt\x000cÞÍ$¼.eô5£\x001f`Ô\x0011Sí\x0014)²«\x0013¦\x001531t3j\x0018Gê)\x000c¾s¸È	V³mò2Æ1ö3Ý\£\x001a\x0013½ý\x0019Éã¨ç4\x000b\x0016BÊvc÷ïlÌ\x0001¥¼:±Óaµ%F\x0015f2È2ýªjSªª¯\x001f~ùxó~Á;\x000bXFE)â\x000b±|\x000c$3y,]¿üáÅÙ³ãp¦3ppÃ-	ø$!EÉþìq³Mÿô¾¦ÓOÞwá¡j\x0006ÇG+Ð\x001bÖËfòZK\x0007\x001d¼wÂ¶"`Oá\x000fðPIùd{Ö[µëY¯èµTxåYÀ^\x001eTÙNIdÔ±~jü
 ª\x0001U' ö\x000fÜ\x000cBQ\x0007k°ÚÜ	Æ¨ÍM»\x0000u
¨{GÐûÒ­\x0002E¤t\x001eA§¸­ÊáKG\x001f`åð\x0010$þA'§fÁ7od\x000eÝ\x000bo©Â	0Ç)CØçÜöK¸
=ø|·¢ïîn¿\x001cß*Þ²>8ç\x0011IMÊ\x0015©+}0ì}yòüåóËï.ÎßÎ¥ëîæ)³§÷ýðñó
ÜÞºò³Jí\x0012nnªô4ó¤9&ûòÅ3¸È-IQûÂzÊìi\x000f}Ãm_î\x001cÔD\x0016ÕCùÎqD'²ÿ\x000btý\x0005zý\x0017\x0018jÂ"Ào§{´	å§¦ûI~©?À¬ÿ\x0000Á²¹\x001a\x0005\x0003}*7Õc*Ðý_`ë/°[|¡)Kæ/ànhR#ý_àê/p«¿À\x0005ÎmÂzªl0]\x001c©§/.£_àë/ðë¿@aå'§6ræ­/xÇú\x000fô@¨? lñ\x0001\x0014ü0C\x0008\x001f\x000bÌ¶æ5\Ë/#x\x0002\x0003ë\x001c{É:ì<Ñ­wq-nö\x0005ÒGfÀè¢ó-\x0000¨\x0008ÝØ¼m·ÞÆ²9Íäêã\x000cóf\x0003WrGò\x00171o?a»E$Ü~PÇµþÄÓ/_\x0016\x0001BJ\x00170ðl§=gÑJ?­¨¸¾|ûã±\x0018Ûó\x001e\x0000W
â¢Ê\x001aWó@±_6;=G"«ËiuM«\x0007i/\x0011\x001dª\x0005ÔX\x0001J¸³\x000f\x0017áêý;¶¶Å\x0015,ä÷·÷\x000b\x001e¸tj|_\x001dfa¥ÇDê|^§\x0003\x0001W°v_>yóóÍ§Ï°Yø/ö)uM©û)=,Q³Âf~òMÆi@aN°r1¦©1ÍÀ`J[\x0006Ój)\x0005G¤\x000cæ¬¨ÃbL[cÚ~L§4?ÅZ­xÎ\x0015)ê85ÓCéjJ70çBáZ¢T|:K]2\x0019uÌ¢êÁô5¦\x001f\x0018LT\x000e§t
'È	\x0002×AQâÖsZ\x00121C\x0019\x00060ÁÅ\x00144(¨Isî#a\x001a1\x0013ð[L\x0019kÊØOi=vwIc\x0019\x0005\x001e'ÏÛÇN;dË!+\x0017FÛZËbùX\x001aÚwàXæøA\x001aK#(oä\x0016\x001b¨
ñê&Ä»|4µN2mÉjÓH$Bd£9÷x³²9äÀ	C\x0018Ø\x001a±(-êÆâØ\x0015+ót¢YÂ\x001f Ïô#ÆÉ?Ü<¿ùp{s<Pd\x0005*å#Ý£bfN%Ã$|¤\x001bPÄñG\x000c_<?»:?{{\x001cSÕj\x0000\x0013c+ùFÝ\x000c3e0ühnâAe¾^J]SênJ\x0003SÊ	õÞ#!åmJòìá²^L[cÚ\x0011LË½ß#Ï\x0017°fÑt5¦\x001bs-9Ü\x001f\x0004WBJ\x001f¸P×ê)ÿ½¾Æô\x0003£éì©ÔiIRT:\x0016h\x0003ÙK\x0019jÊ0²Ïáz\x0011Ê`R¼/EäV\x001f\x000c®÷bÆ\x001a3\x000e\x000c&Ì¹£Á4¥³eiúµîå¨ÌVS\x000cpÂ¾¡"òàDÉÐÖ¬´e?ä¸÷r¶Ö½ß¼·¡H·?\x0004G·aé¸«²óhtÖeüéñ×ÇÛw_È$¡!º¼»ýròÝÝç³/\x001fà\x00040\x001d\x0012\x001e\x001c~÷þ÷º¿ù'ü[¤S\x0006E¯\x001d×à\x0001eÏ
îV¦ímPØý\x0015ï\x0008uþäòâüíÉw\x0017oNÎÞâ\x0019yø"Ù°¡V!þêC%\x000eì~\x0002|k\x000b1\x0006Ç\x000eöâ(ÔJ>\x001c»Á3X§\x0017Ïgó\x0008|ÙYC<¿	\x001d\x0018nüÕ=µX\x0002áD\x0012B8ës£@ \x0013¬b¸\x000e\x000fØ'ø«\x0017\x000fNbh¥Å\x0007\x001ewyðLVè\x0004¾¨7\x0019>ÌÁ_|:ñóyñYëP\x0010\x0000ùÏwYÝpÃ8»ùô»¹!\x0007\x001dg7>Þ\x001e£²ØM*Ò¬¢\x0002>Nh\x000b\x00075¯9)\x000fÚ³ë³×/&B>-\x000cìRó§Eïþkaþåþã·Iê\x0002\x0018,Æ_×\x000fîn\x001fâà«yvDa£\x0005ï\x001eÚ	\x0013³ëéº~ùz:NÛâÀÚÃ_q"µýÃ}\x001f²D\x0008à° \x000e[Ç\x0003¶\x0004-å:¦¨+àhÀI'\x000f\x001cGG\x0003Æé\x0018Î?Ü¯û¿\x0012\x000exÏøëò6u±øô)%.Í\x001b$¸\x0018f5l\!RÙ°Ö*f_×å<´~.ÏSÿ×¯_¾<¤ÿíï¿½ÿ\x000bb¡ç¿\x0010ëñá_¿Ü\x001e7CüZ´OâjH¥4]»¬6\x0003\x0017ûT×/ÿùíùI¨\x001fÄýßÓ6Ã1þººù\x0015\x0006óèÔ\x0019\x0014É ¯\x0001Î$ÑárÞgÖ³p^Mtuö\x001cÛ\x0000.Á\x0018-Æ:GÄ\x0011'ð!lr\x0005â\x0003>L\x0007\x000el2üµ|tH\x000cFGÒð8·ÑðÀ¾À_ËylÉE2\x0004S\x0006G\x001cXÓÇ`Âw\x000f"VÇ\x0005,ç+p}ï\x0016ì1KoëÚK\x0004Êª¦;ó£\x0008{Ëù
üãé-¶CB§ß÷1¹t\x0019C&ÌWt&3Q
­-
«ú°*k\x0017\x001e¢?ÀðÐ\x000f7\x001f¾=¹þrtî4jôû¼÷\x0005¦%+	S$\x0017NF{ÀJþp}öâ»óë·Ó²À©\x001aNuÃ9Ep2ç7%8Ip%;z\x0014N×pº\x000f\x000eÃ}Mé\{\x0000lÑÐ2S%»|ÍÔl¦ÍdíYd\x0013téRV¸Âf\x000fXô\x001e6[³Ù>6kN³ñ\x0012p!yÜ¬2´à<dL{Ø|ÍæûØ°Ý9
\x001cÊzä£Ð\x001aËû´<Â\x001a.tÁa+\x001bC+\x000e{\x0015'#¢ÒgU®\x001c¹XÃÅ¾\x000b1tRíB~ãóÊñÈÅupR4FNô
]\x0010¼WÁÈ9\x001a¹èwFîgÚ\x0003×Zà>\x0013½Q\x0014ïó@Go\x00088tjåÐ5&XöÙàôxMt
lpóàÉò¢;àjô°5\x0016Xö`çh¯[-óv<©þÀ©ÚÖ\x0018`Ùg=Ø6\x001bÊKï¿0n^G¦3ë\x0007Ù`ÙgaÄòC\x000bNªã
á\x0015;mJu\x0007D.r/t®Î:õÎtÔ7S« r8ÒÉtÍ\x0011!ûÎ\x0008¸#åò	Ü®!×IÂØ9¾.)%Ö9%²9#dß!áçx!Öïd[\x0012¤\x000f<tv¥-iÎ\x0008ÙwH`"½ Î¨S\x001a¹ Ë\x0019aÖíXÕ\x0011ªïÀðo {$©K\x0018ºÈÎ¦
=tÍ!¡ú\x000e	\x000f^È\x0003aU~±å\x0006¡õº#Lµ~zß!\x0011rïÐ|ç
9\x0011R+Ì|)w®uÇj	ÕwLÀÞä\x001b¡\x0000\x0007ÏYÚ\x0014×+éBõ\x0014ÁÜ\x001eÆN\x0017·.zÞ\x0015Z»¢9)TçIáMñ=iÂØ)\x000e¡+ë×ÙbÕ\x0014ªï¤À/²vÒRI%\x000c0¼î\¹gBu\x0014QñI!ña±Ul}XwPÍI¡úN
Ø|Àp²ôøÀ\x00171¬ÊYG×\x001c\x0015ªï¨\x0008ÖK3[Bí
ö
{(ëæU7'î;)0\x0001Dg[9ì9,¡¥ðäh§×nN
ÝwRàºõÅ\x0016lí¢\x0016n#[¬B÷\x0014Ià1Ûb\x0005§¬ÉÑ9©98çÝÊ¡k#:}\x0007EÀIÚ\x0012X\x0018É\x0014ó=QK¿rèBw\x001d\x0014Ø;(5bÀ¡Ó.<Z:~mÕqí¦h\x000e
ÝwP \x0002cSl)F®b´MñÊn\x000e
ÝuP\x00180|P(Ñ²óÖ\x0011+ïØº9(tßA\x0011aféY\x0008ë1òG\x000bÅ^»Ö+M±n\x000e
ÝuP\x0014¦ËÇXjØFë-±QzåÄ6çî;'¢)7Y|\x0016É¦X44ÜÊÀi,±é³ÄId5\x001d\x0012N-¢0åX·[McéL¥Ñæ÷\x0008\x001dÈ\x0008[f\x000b+/b¦±$¦Ë³9Y\x0015÷ª8¥­ê¤å­º2ÌiO5¯ø'=ã\x0017Ê \x001ec´c%iï¥sl]xGû}H°)½¤´Ñ¬X:Î´ÀTEòðôÊ±úésûºó¹÷Bp\x0004/äVËøLaË3ÅºU¨íWch»ÇPäm"(\x0003(\x0002Ï2v\x001f\97í\x0000ÞôÀ\x0019çs/¾$F<àÒ\x001b\x0014\x0018éÂ:w\x0005\x0015È[¼w]ó«|p_\x000e\x001d`B	Ð®\x000cýù%ÅÁ\x0010²¥JBÓª%
x\x001c\x001bD\x00161Ö\x001aVô\x0007M+\x001bLòüòã\x000c¦:Ò(ºËñ°Ý;\x000fãN\x0013½Écaùö3Ìò|û£ U´[ìZÕwZTåy9êòÌb}ä	×¬nRÑÚoa\x001b%¶®Õ%k\x0014åQ(£K\HÙ\x0003û§Wí/\x0001U-¥é\x0015Âºâ÷£&&e
ÉÀþ×¡GpªÆä<£ªfT\x0003;\x0000.ørÅN¢1C¹\x001cR×z\x00082Ò¡\x001d
åËaI\x001e_\x0002L<pàôB\x001aÒôC¢4X>´µ\x00089ç\x001c«ð8ÐkÌå\x001aH[CÚ~È ØýõetzÅ'ÈyÉ½®týÎQ¢\x0001

\x000bE\x0003©ÉûA'm=£¯\x0019}7£Ñ£§.ÌÂyß\x0000\x0019mnë\x000e\x0005{!C
\x0019º!¹]:B\x001a:´|É²îPÐ¦\x00172Öq\x0000Ò/äÄ;@*_\x0018×o\x001bÓl\x001bÓ¿o0PR"!¾l\x0012¤\x0008)ã¡\x0014Ù^3ÙÉTVzË­¥É}aÿ`)\x0019\x0019"Y\x0012ûÚÀ\x0010É}V9Ä\x001a*ËÎ	OàÆ±dÌ¡,¶î\x0015Z9ëiÞtÏ°õ"%Ënw\x001b¡Å\x000ccVej9ÿ\x001f}À*­úý¬Åªkù):xQ\x0002?BçF\x0014ZEÇ1ÊOºÅo9±ò(¢ª\x0011U/b\x0014_\x00050Ñ\x000eJôf{èÛ¨kDÝhðÕÌ8z||kÃÁ½CÊ¦\x00064ýM6/õ&w5¡­	m/!úB´Y\x0014ö¾ ¯Òòû­ë\x0007Ñ7èûG%]ð\x0015×e½ÔdwÊ+î¡\x0018nïf©íNeôniWö\x000b]s£ãDd@\1Fì\x001c#Zí¡\x001foîïÿøDûì×?þß%g°ì^b\x000e5ÅP
\x000fé¬?ÁÏ	þÙóóYsiÄ-2¢\x0015"êf×1JÌ (±¤ð¥âÀ	rÚ\x000f\x0019×5¼^\x000b/²\x00029&Ù\x0019¬ËòZb'­ê\x0018»©ÙÍÚE£ÊÅÉ{ÌÍ«Æ\x0014§jæ<\x0002okx»\x0012\x001e#Ý´jd[,K:¾q\x0008GØ]ÍîV²+Q¼Yç¸L\x0005Y\x001exy(\x001fs\x0005¼¯áýÚüzRáÙ\x001f31n\x0004/÷ídÕ?\x0018pï\x001f>¼\x0001'òxMÓ.õ	K¡éÀ%\x0008ÜM\x0002cÓ~êÎ\x0008/_¼\x0001?rº¸U4\x0019U
¡JK©ë\x000eÜG
\x000b)Ç\x0015ààL;=¤º&ÕC¤°óõ1R½£þ­z¨´i\x0000ÕÔ¨f\x0004ÕF.Vp¨ö\x0010©Ì#HN¹­ö¡Ú\x001aÕ\x000eêÈ\x0013ÀrÒwðÿ¤Sâ\x0005\x0000~zrysB/\x0015¯înß\x0003öÿù_ÿ{qá½§\x0014¤~\x0008É\x0016Ø %É*\x0004HVáì.^]?\x000f8VB^4Ý+Ç©\x000eaÿxûøñöËÝýñåà\x0003*±Ì,Pa
gT\x000eµüx~ýâüíÅåqLUcª~LizôÖbRUFÂÂ\x001bÛ´_´\x001cÓÔf\x0004Sð\x000b¹ðW¬
v0Õ¦ÒÕîO;¡Æ\x000c\x0003Kswº\x0000¦\x0013|ñð~\x0015¦ÜßAÒî7\x0018ûåþîÓÈÀaXÍEJc\x000e¥ð@ÏLûåÉù\x000f\x0017¯gÏþý=$í~k±å \¶©5=X!(ovyHÖ¢\x0017´.1±¥b'),Qzà\x0017Ø±+{)ãÜÏyÇHß	\x001e(,\x001fm¶LÿÕÃÝÇÏ]6ßDË%\x0000\x0001¼«¼tP¼ë£6ÔVÎN^½¼xñ¦²öSõÄW7¼zWY9\x001dYºFRÑ|ä}\x0015\x000f\x0016=/¥
?=þýñËO\x0018kðp¦ß\x0000óêæñÔ!Étéþø÷OÿtþÛo·Ï:ìôºiì0\x000bÅ½r\x0002­«\x0001Ï_¿zuþ\x001a	¯Î®/gD"ÂOüï¿Æ¬Æ p(WòÝÃ$Ð/\x0002\x001d¬¨4­ñÎw\x0001RIó\x001eë@3k°æ\x0010,y)ß½¼J"Íù6PðsôûWà\x0018à
a\x0003pM/¾ª³ö­÷.Ð\x0018\x0007Sç¬nÀÒ{q\x000bn|è¢\x0001#6¸Ì
ÿ\x000bk£·\x0004X­$Ø\v\x0006&Êù2â¬/¸àõeq\x0003rÌ\x0000O¿­'Ù\x001a\x001bìkMÜi"ÇÄ«-Éñ\x0018J¿­''\x00151ºûYÈ©\x001esß\x00089m@Ö.ý¶Å+ÚÂæ~ÍiÌ	Üo»ÊÑ¤ÈMì
¬òÔ­Ò 6_\x0011HÜÀm}¡\x0018&ÿõ^ýö	¯o\x0006+ÎÓo×\x000f_>'à×w¨ùóq\x0001­EÑbÚ:Pü\x001d¦\x0000\x000eøò ù~ùöM|}ê?/\x000e\x0011¢#T½ç?Ø½:9¼ywûi\x0001¥³¤\x001a\x0011CôYÑ\x0002,u tB\x000bûäâO×gOáO'\x000fE\x0006%¿@w~[\x0017©\x0013T2\x001fC Ñ\x0019@¥\x0004´Î§J\x0007©nTiN¼Í¤.«Py\x0017¹à\x0005Íñ\x0006¤&Ô¤&\x000c\x0006CÑÝ%4¦\x0004\x001c`GéI\x0013ÖAjmMjí\x0010)¬N]@EÞLêÖ\x0010t!uÍº¡!Eí\x0004Á¤N²Mî0j4ÍÖ7C¨*é#ò zZ§$þFÕ®G{l÷c-4Ù©À£ê"y\x0000<´Ô\x0006¨TrÌ¨J¡\x0006JÁÇN®©<\x0005Q½-»Ò£é@5-ª\x0019CõÂ ÉR¥[;°ZÁFÕÇ
\x000c´ªaµj\x0015­°:£Ë\x001e#l\x0003l¼\x000eu°:Û\x001eUCÖÊãYº[®>ûã"Xë\x0016¬Þ7¬Þ«¤0-°ÊÜÜ\x0019ÇÔ^ÒÖÛ5´ã\x001aÆ5(Iu®É¸ê¼^¥4|`9¿ÅzíÞC{+(MÞòzU\x0018»Í¬­+¬U¬>=èÝA\x0000w\x0003M\x0007Á«GøÛï~»¹_â©:-Ø_1àºH=+VÀ²JÊ©#ëÕõÅg\x0017¯Î.§\x0003#\x0005Ô6 v\x0004TiÊ\x0005P\x0012®\x0003PMÕ°\x0000j§´\x0003Ô4 f\x0008T³
@4C\x0003J3RäWcZQcZ1\x00198RüÄ\x000c$ãsjãw`\x0006Yc\x00069i<%¬¥^JÖ'§	Yeâ÷×\x0003ÚL{\x0018vÀñy}Z%\x0011¨g/EMÞO;8c3ïqhÞ­§·$\x0018PwJÔK\x0013Ç3L9SË9¥Ð5g\x0012ê\x0007uüL\x001b­ötæÃOðN¶÷\x001d¤²%c¤öTÑ\x001a5\x0002­T&¥gz ô¤zHmK:´HñvJ\x0014#n4r£UÞl0ûÓHÝ\x0010inv©S\x001d¾\x0008#yH'oü\x001d Ê7 Ê\x0006Ó\x0002aD\x0003ÅÓà¾Ï\x0001ïö5q\x0014T·«T\x000f­R¸ïç\x000ch1\x000bT±_ªüd¸´=@åÐ	
\x0010¾F[NÐÁ\x000b??Ô¨0éAwÚÆyÂ\x001fGH=;%+ Ô*>Âd\x0008­Ôµ³ïFf?É:Òì;]L3i`k\x001a7ðó¤kw¾\x001bÙù\x0018eòSÒ!\x0006&øåK5.£ ¾]¦~h*Q&ß,÷¤Oüè6\x0018Rß\x000e©\x001f\x001aRM}¶Tçô_ ->T\x000c\x001bO¡]¥ahb\x0014:º7ÁéIYdVÉøI\x000fihIÃÐ\x001a6ûºÂãîæÞn`öck¢â\x0002\x0007Zð&íï\x0014\x0010¤\\x0001Cª6üØ¤qä$õ:R¶#%³\x001dqL9$©Ådì|9©j]S5äz|8¡\x0003*Bóf_Ë
\SÕºQjÈòÖSZ&©£±SÉ¤bêÁ¯4¶¤qèâçêÍí¾àu\x001a'T;HU;ûjhöÁÝ§\x0018¯Ã>\x0014àãBcLÌZï*eZÒ¡½ïX\x0003Ö©ÊJNHÊO'ºQ\x001d%5Í-\x001f\x001c 
&Mù.ÂYºB¡|Ò\x0006¤¶%\x001d:õC¹"©¦×\x0008KO»\x001b¶\x0001\x001e5\x0014áÁ1uÖ©ÏY£iLTM\x0006Í{HÛ½oö~ü¼ëÀû£ä\x001bQ^¢õ\x0006·RåU\x0003ÊYZ] ØõÌI|Ç\x0019+p}öeò7Øú¾5R~ÄH\x0005\x0011N
Sî#\x0007¤Qó2[vLÃÐ\x001bíÔàÓI3çä3t\x0007glMT\x001c1Q¨\x0017miãë4¸3P0ç}\x0003ÒvDãèò\x0001¥5ÝJñµW©Ý ¸«EC?\x000ejÃoeø\x0010áè]O\x00056QRó0ilIGLT@}\x001aS#s%?jFê
^\x001f´lT\x000e
©1\x0014×w0¸üòdTY¥\x001b¸ûºuøôÃ\x0017\x000c«êÂZ~\x0006\x001fGÔ©
æ¾u£ô\x001b\x0015¬¥X$nüüTâ¥
ºlü
æ^7&*\x0015â\x000fz\x000eòàs\x0004\x000f©ãØvný
Jæ®?\x000ezÉhg
§!ÊòH®.b£¤¶¹Aá\x0003¤pm"\x000beIªÕ{%$ÛR·A,R·\x0011>=\x0014áCÐ¬\x00121]ÒÛ\x0015§sh¿ÅÜ·q3=\x00147Cå`Ï TÏ
 \Õ\x0008¤[\x0018ý6v¢b'¨Ó+xú¬ræSe\x0006êõ¾¾i ÌÐ\x0013TsÞ\x0012)¦sePçxãG¹ÞD\x0019iZÐ¡!5ªø&NæçG¯|9ðýú©7í%ß\x000c]ò\x0013'#Hñ,Æ\x0012X'1­Ñ7CF?\x001aÃSm~x\x0006\x000eñ\x0018¹ä\x001cÍÆ7|ú¨îø7\x0003×<o·\x0007×\x0013MÁ(S\x0002|Màønª^uYdªó\x0011R|S´0Ê¢¼#=Ê¯ôT(¬w§\x0014¶¢Cê
gäæ\x000bü÷§÷ËÒd¥$éh°;7en¤Ó/ûWg×ÏÎÏÞÂ¿~v=wDÄ¾!öÃÄJq¸ß\x0008O\x000bÂ\x0005ÎVLùª½ÄÕc\x001f\x0010ó[ß\x0008± \x000eÞQ\x0007Ã1êÀÍ\x0016,\\x0008¦N^ä*\x0019\x00119\x0017q\x0000Ù°*t\x0004ëÊ\x000fjÁY²dRMÞ\x0008z}³ýøJÆQÎWmíb\x0016N£Ì\x000bCNfüö"X#8¬%]»àÅß¡x
)¥r\x001bâØ\x000cr\5ÈtÿBdJ±\x0008£\x0004rú­­\x001b¹\x0019ä¸b\x0005_Â5\Â5-e£i÷x¸¬¦\x001fYJQ#K)Æ­²§\x001ehà£YÎ·R\x000f(Âdà \x001bÙ·È+Ì2+PGT²j\x0019,3oe¥nY\x000f³°§ª ;Z\x0019ÓpDØjÿIÓ,füqxe4\x0017'\x0016¼\x0001%\x000f³Ùje´§\qü	Å\x0004*
\x001acÎÉ\x0012fò5©\x0017¸=HäøIdiòRV^QÐÖùÈo BM¦æu3·ÛÏo?|¬¡Aöë`\x0001Óý8^·a®r6s6FuY\x0018p­ó¼ÿ,¯
5éÚw39¯
KaÙ\x001aÚHk#8:\x0000\x0005\x0016ímÃ\x001cÛµ\x0011×\x001f!\x0014j¬\x0018ZÏÇy+Ë¬Ú\x0003P\x001fËAÎÂ~ÙÌyO5Q¨e6u?íe6-³\x0019g*]L\x0014v£ËËÙ;ÇÌå\x001bÝÈºE\x001eÞ6«- ²\x000c´}áµ5½À¡\x001dã0>ÆÖóºNnó®R&j¹þ*%jü\x0007µhÜ¯·\x001fî>¢tÐçEÞ§/	´`¢\x0003LXNK5u¨Iïêâ\x0005ê\x0007M©oíp«j\x0019LÙ°¼Æ:>G¼\x0004Ç9ßI`7Î(3#¯Ð\x0005ì\x001b`?:À0ª\x0007XJC\x0007_	·Ìjpô\x0000W\x000e\x0011\x0000[3:Â\x001f¼$!9\x0018`m\x000c\x000f°¬¡íã

o\x0018æÜd3zÅ%t`ÔHþÈéWÌ>`Y=\x0010b¿\x0016~ ì&¶¨\x0001MÁÍ]6°\x0017×°\x000b\x001b\x0011«ÆFàÄpGÍí}£·\x000bê`\x00032±|Ýè$®âHÌÃ~bc8\x0001ÃïF¹¬¾Ä´\x000c\x0016[mCÜ®
=¼*\x000c·*ÞËSZ\x0014\x0003Þ~N6¦·ÊlK=äðp(GØQ\x000b¬	\x0012£\x0005âiý>b'\x001ab'F]À·ÎDl¨\x0007\x0011:@íäáÜG¬D³ñÇÑÃÃñK¦\x0008d1!ÿúMe³*ðÇqâ@\x0002\x001cp}tg¯Ådý@'qkÛÔ°mÃÂ[J*KyÏ\x000e¼	¡&o¦Äº\x001dc=<Æ(\x0003ÍcÌ9.hÇ\x000crZã¦Ø¸Rê$\x0006Û&u!\x000e´\x001d¿Z¹Ñ:öªÙyøã\x0018±\x00124Æ(\x001fÉ\x001a+Ëqdðè·\x0001(YX½ìcQÚÇtÛ8Tî¢:©í¥Å\x001cË©7ùlº\x0018[e\x0001¤M%_¤I¸òùíã»Ï7¿,zé\x0005+AÇ\x0008vtö©k]Þ~Ó¥QI¾òùùõÕÅ³\x001fæ$3²jÕ:dºä§\x0006·º=d7Ü\x0006¹ºH£\x001eG»\x0012\x0005ìÑ«ÏÕ©ù&{õjZn¦\x000bÙù\x001aÙù\x0015£,¨\x0011ctQè\x00142gS\x00191}ÓëCöÍ(û\x0015£iÚ}Fp\x0011ò§hÌ´\x0012]\x0017²r
²r+\x0015÷¦X¤\x0018)ËÆDv<µX½Eú­J\x0004\x0005gQV9Ï~ÿmYx%8K½íct²È¥x¾ë93}9ýõÕÈJúÍ4 f\x000c4P\x001d®	æ\x000c\÷ãÔä3H\x0007g	\x0008ÖpÂM#[2L\x000bX\x001bØ#vb2ÙÃé\x001bN?ÄYòj£âbO¸kÐ"uRÍÉ¥-ä¬ò\x0000ÓÛ!ÎÈyKh¿
'{fÓo¹\x001dU´\x00128\x0018âä\x001enY'2¿\x0003û7ÖO \x0016J!\x001d/ä\x0008iÐ\x001cµ\x000eØ\x000bSS\x0006(o%ûiºtÏ6\x0019'{óR\x0014Õ©ç\x000cP¿¯\x0007U±5¢qhH\x001d[Ñ`È·\x0011Õ<¢fZçu9h%ã Ú\x000cª¢ä¥\x0003gÿÊX®
z2ýw\x0011iLtÕs=fBï¢\x000bo\x001e¾<~¥Å~\F±§e¼*ö,\x0007îËÌmòÍË·×\x000bTÙwìNÖìN®d÷¤ðå¨}Wÿ-íL|¤]5ìj\x001d»\x0017«Ø|)ËB¥»ÆwÃ\x0007WÃ\x0007·ràñÕ6û\x000bÆE*Ä\x0001¯×³\x0005¡ÛÁÇPÃWJãc#/
\x0007àÛi®:±yCê¢Y6R¬]7Ê`V^óÑ\x00070©6\x001cz)¡Ç\x001f×ÑkÉE¦\x0006%Ë\x000b\x0004¾×)9­Ë8@_\x0015\x001e!½2ké\x0003'\x000b¡ª\x001cÇ\x0017IKé\x0000¼n^¯\x001dzL¦'\x0013
»PL>-Û8@îÛa÷k\x001d\x0018)à©íNè¡h&aÇá-½Ê³§¿YÉï©\x000c|*\Ïê\x001f®þÜ\x0013åW\x001f0Q%PèßíÓ¿[Gê\x0015\x0016½£\x0007a8¹T¢gËNÐgÇ«ÖS\x000f¨§~ö÷Û_X©þ%*õ6ZÉw//J\x0019Näb1ìËz÷ìÇó\x0017oYþ³F#\x000c[k\x0015'Xà2Dkì)ÁªâÃ?¥9q0g²¶Ö\x0004\x0003¤	6:¸\x0014å
ó/`t9=\x0000ÛnÂëeÃ\x0002nC¼¨³EW\x0007KÏ;p\x0008)¾ä\x0018yÈd÷ãÆfåâc¸`\x001fT¹=fX+v\x0002Ë¬\UÕáÊÅ;þ\x0000¬K­I-ÁF\x00122ôºgM4ó\x0019à-ïØà:!\x000ck\x0005Ï¹¾Ø´ðºMÖ®Ò{aÌ48"l,\x000cmN=­XzCø*'ý¼¶åµ£¼;ÑÝ\x0010Y;ªäa±ù&¦LùÆác¸`\x0010¬¢`¢aÛ`\x0014\x000bHÁø\x001f:{xmÎÌÚ
/É®\x000bé«û¿Ü>>|\Bk\x0005÷^\x0001Dg1\8\x0007WëcøÕåË\x0017?_¿j×½­Ôm\x000161Ø\x0008÷ªÄ
s2·¤îpÚÖ£Öå!ÖîÊC:Y¥$ï\x000cÛÄx.2µòB\\x0012­Ù¶:!6Æ!Z%d\x000e/Â2\x0000>KHzgèæ\x0001ðÇbZ%BM?\x000em\x0014ùÂ¶­Ó\x0017;¸Å:hú©mocTÝ\x00103b½¹[\x0010¼sØÔ3=ì\x001aì\x001eÍ%¼ÆñÅ\x001a%\x001c¦\x001f0\x001böùÙÅlênB­än\x0001Uù1T[P½æ\x001b)é	ÞÌt\x000cXêQuc£
+@\x0013i<ÍÀ\x0002jgº\x001b-\x0007õÍú¡1"kIbK®Hõ\x001eÇ¾\x0010î!­\x0004\x0011t×5¦TQ\x000cÅ`}j1XKSÐ\x0003[*E?\x000e²r'BiOsN¼Çf¹Ä\x001afú\x0006-gÍ\x0002(UwK5Ð\x0004°êÒ	\x000fî¼4®aº®£µêÅ¬»^,]ãJ\x0018Ù\x0002HÚ(iX\x0003÷òq:o¦\x0003Õµ¨n\x0010Õá1Å­\x0011-¡òu<Ì¤«-G­³ëÐ¬ª!T<\iPÁ\x0013 <\x0019g¸¶.÷^TÝU¥ìª\x00126çô\x0018¼Îq3\x001eg85øÛå¬u%°8ÆJOLÀ
®«ò<®u¦ÉÑrÖ*í\x0016Y\x0018bEnC¬6+2SÁÏew-GmÀØÑ]^)å\x000fþ¦SC®`0¼³üt¥FÅ:\x0011Ë ¾\x0005õ îÔÑZ\x0005fÚVûð°dHg1C;õalêÁCÙþÃBg\x001d<çyKE1©Ø×1÷ºò¬Qþ¿xÖ[ð\x0015Ü\x0015Í¦JñÜ;·\x0005«lÆUË±qµ"¿·\x0019\ø§6ï)ÏîJyòYZë
a\x0006Ã®s\ß°¡h\x0008($àÊZiÿA\x001f0T\x0019æI¨2\x000eoN.o~_\x0016Õ\x000cü\x0019­æ·\x001c-\x0003ça6øt\x0012Ü\x0019üç¯³I{æ§¶\x000c\x00062}¤¨È¤Ü4Ô«ÒI\x0000NÙ_JªdCªä\x0008éN#:E5C^6\x0012ÎLJvVÕ7HºëoÚC
\x0007¾§1ºäó]\x0016ÜS½´¾AÒ]\x001f¾\x000eÒ\x0010\x0003G\1\x0010Omøà\x001fà¼B3]Õ´T©fC)5²£°¹¡¡ÌB/Kdå>gg\x0016ÚfL\x001d\x001aS0ýÔ;*bÈôÄ\x0003ËÌ%ge5©ov\x0014þØO
\x0013Ó 3©c\x001fUØ²NçRáÖÂ²xe\x0013#;*õg Ù\x000få\x0015\x000ev+çkº<ÝÅ¤¦±§ÚØS/\x001cçòÇPji¢å|-ç'[ÈtºÔ:À£\x001aÌ\x0018EIõ(\x0015nÖ=]J\x001auªÃÈ:up²åÇ÷ynÈe
é\x0006³oDCjÄ\x0010©	,Þ\x0007\x0006\x0015[äd½²÷§U;;HÛÓÔ\x000c¦(_d4rS¦Pd\x0006Ý:#\x0015#zRUÙ"J%íe|9y\x0005ß¢§\x0015I\x0015ä!\x001aÎ6%F\x0005÷þ£é\x0019oO^ûw\x0014¸\x001aY\x0000VûéåNÏ
cI\x0006Ý*µko»\x0011±nõ8±°Ü\x0005#5 Ï:UWÒ \x001fÏ"Yì\x001aä¯rL/\x000bØaTà\x000c¶\x0000E\x0011ÒºÜìÔÎUd÷\x0011«x?C°Ø\x001aCËÂF`F]:	O_µ{u¬ÿü\=\x0012\x0000±÷zâºÙ$\x0010fýÈÊ	.$\x000fV*ª=3ò´hØ>óT\x0018&Ýl«6$°\x000cm\x001d,üòxûËÇß\nába¬Â%}Z­¹ [»ù'£·×ç?¼øë\¸ Ýnªt(@--\x0012»XáàPÌ:V´Ý´(}äldk!jý``ö\x001e\x000c£\x001aÍ:[`jË!'w}½æ[\x000bY«ÒDdõz\x0015û\x0010\x0011+bÓ¸\x0016}jå&[åu±úÕ°J\x0014
 VUSM,-\x001dít:v\x000fkhYÃÐ¸ú\f±\x0002«u¥«ã&+ ©\x000f§UPêÃ;EÑ"ÂÂ?EÀºôËìI´\x00109$7²²\x0005á	lÙW7>Ýü,íÕÃû»\x0005©\x000e\x0016SMéì5Nc¼;_ÌT©*8h·^½~}öC²³W/ß^^Ìæ:$ZÙÐÊA\\x0017=åE\x001aÔ%ZÍ\x0012v2\x001e¬¢í§­ü\x0004¼\x000eèÁÁUEJzZ¹æe\x0002¤;X§ÜE%©ªç\x000e[U¨âÅçêæñþî_Z\x0006Ê!o­%Éúz\x0013¸d-ú¹7\®Î®//ÎgsË2qU¾IÚ~Xñ²ÖTEX\x0006&«ªî\x0000®T´L¥¢Õ
,\x00155[ÈCì8\x000bÂÇ2Ä\x0000×^±\x00176@l³¢/\x0012{~\x0007±ØÂ!\x0013\x00075'^¬1Þ½ô#s*="\x000bl\x0016½cd?­UÖìEìÅ028\x000f!?6j°\x001aÔsÍ)¶lÑëù`NÇÖkOº´ýª®\x0013\x001cßñ/c\x001déí	l_\x0019ëùØÎ\x0002ðÜtSçÀD6«ãõû»ÛÇ»E\x0016#\x0006´èX°ãÃÏ%vîl\x0006Ü×Ï\x0000öb\x0001­khÝ\x0018­\x0014\x001cã©ÂûV¨\x00124l"ÓIë\x001bZ?JkJ\x00173Õ9ZÂ £¯\x0011Kqëk¼yÒÆy;peMXg¤íd.\x001e\x000bqë\x0017ÉøÕd\x0007¯Ù©\x001e8ÉN»uì´§
x²5/þ8Ä«TiÔ\x00151"\x001fÎÎç^u°¥W¤åP\x001d\x001c\x0002xkËÏ·7_¸j®\x0019cÆ28øÏ\x001fìç
Ê=?{s~öö(¨	5¨	# »R\x001bìq/¸3+§{¨0/\x001cº\x000cÔ7 ~\x00044HY®ÃÎcb\x0002®t\x0017ÉZ\x0006\x001a©\x000f#SÍ9õîºF>$xLåº¶ÅF[F;\x0002é4õAóÔKÅ÷	-¦\x0013=\x0016Ê*#E`R\x001e!µ	bóèH7KGgGwV\x0011&QG:H°ºÄÂ¼'!wo47RPq^ru!©iI)\x0017%àìs\x0005½WÂ°Ý¤L~\x0007©oÇÔ\x000f©øØK
åð/©ïá®3«ÎF\NZËó\x0000i\x0010#¤pB	ê('%=¡zeXæZëi¹Å¤uQ
\x001eObÄF£KãC\x0019¹\x0018[,?­çÅ¶;Jì(¸\x000fÊÒø\x0010¯ää¥K#ÑéÎ\HÃ¾,{ØÉ²'\x0007åúáËÝýý\x001fÿ±è½W+~b°p¡ðW0\\x0014eæ2ÒÁE¹~ùöâòò|ÎG!àP\x0003qàFcK\x001f<\x0000¶l¯Ì\ð¾\x0007¸*N
¶.Nê%¦ìô¬|\x001fIù\x001e;\x0019x>¦´\x0018¸R\x000fü\x0000°à*\x0013cQQ-½j>âf/&vÍ\x0010»á!ÆW\x001cÊ¯À\x000cìKÁ­:\x0016;(À\x0013Ïda_	8Ø¦V¡\x0013× À\x00182Eý{+Z\x001fÉ[Y:¾õ=&\x0011ÛqbÏêØEÅ3réä;Ó¿¡\x000fÙ4KBá5aLÕÏÙp÷"­GéAr®Ø®\x0007Ù¶£lGY\x0007Ë½Ã°ÿx~èq¶ê=?\x001f\x001b]Lì\x001b[¬ü°56Ú\x0015ÿ\x0001\x0016µÊÆ
îhìiM¦.äZp9ÔËÝÈ
¼\x0007*\x0017ÃÚì¼UQ2ò3\x001eÏ2âw\x0014g,cOShôÉË»Û/'ßÝ}>¹¿=ùþæË?N^}¹û¼$½\x001dEÒbò(Ç°RZ\x0017A½0Ö\x001fÜ|\x0017çoO¾»x\x0003tòýÙÛ¿¼z{ñf:Í½`«\x001a[­ÂÖínä[xÌ#nwÐ
\x001eåÖ5·^ÅM¢ª\x00013aóÝ-$ÙN\x001aî	åcØ26Øøã
p\x000cEçuB¹æiÀ%\x001dÜÆñ¦NrFkÖwÒJ£t­ÔÊèþäé
ìÇ»ÛÇ%Þuì.Ã\x0015\x000e(·\x00118ÉE¹É
Z\x0019]<=
yq~}XÕÄj\x0018N\x0016Ê·*NUbÕt*Q7±®õ0±ô,n
l,\x0016v\x00139`ÖMljb3>Æûª`\x0003\x0010îbë8¯_¹ÉºînbW\x0013»abì¯J\x0014kJ«`ÃÝ\x0012TP­ãP\x0013ab%èmÅzE\x0015.èù\x0010'ÓuzwõhÉTñu\DÄ-*âswGÞyZÙvx];ï§Û½÷óð0K~µÀ¸\x0015·w,®´ÜnaèÞ·Ðï×@\x0002Íw@Í";GúËu\x0019åY3\x0003g»lø\x0012<'«ÉØq~×ó»ÿ\x0016ã¦¾ùó/\x000eÙ.\x000e9¾8°µ/ÖEÀ<×8Û°´oEß´+zx ÿóV´lW´\x001c_ÑFNøH\x0001:§ÊûØÐtüÜ\x000eô°6¾¬hÅ9>èÒq¥
´jGZ­\x0018éÿÄÕqÓ®á\x0015ýàíÃµ~PÅ¯ûùöäòf\x0016¥fË)¬ÚÏI¬¾ÔÀÎçrÌÊ_©}M)ÕhJ-E4%Ð°y*Jx%1yx,E¬rP{Ót#ZÃõ\x0006¿÷k´¸µ5vl_IX
á4ËþA¹ÒÝàÚ©$>U*çKó\x0013Ê*OY¡÷k»\x0011uÌE\x0000¨\x001c%I/ß\x001bÉ²í^ÏGÙ0º±»\x0018\x001f
P1ÌîT\x00199çÛi9¾¶e´ý0U­TyëE,,Lw[[È\x0018Õ(Cÿr\x0012+'²B¡V¾"Ê!Ï\x0013N<a\x0010nñt?@AÓ,¶å00áyî<\x0013\x000eo.\x0006I,ÍÞ{æ¸¬C©\x0004¹\x001f0Ç\¾ìCX¹\x000ehl¢\x0012ýFQS}Öâú\x0008ÉoA\x001d\x0014îaÔªaÔjd\x001cIü\x0007ö\x0007g^\x001aÉåÁÌ?-btÍ~®Õ\x00163Ê"û¢\x001c§9\x001bÁ^[\x0008óï~\x000b\x0018cË\x0018\x0007\x0018\x0015Ki?ÆbË¦´4+gZËP\x0013â\x0003£H
µ*ZaÑ(rÑÃ¬*å"ÆÖrë\x0001Ë
N¹§$ki§#Xä\x0013<´ñ]-}QUâÚþl²«¿øøùîãíçÏ²Teä`«1ª\x000b­â
p$?áû/Þ\¼8ófVP9!Wtx¹qdZèrS\x001b®Kw®\x0014êÌ't0×ÕþÕ+
g®\x0018ëD¥ãHÆ¹ÓNèÐ@qhðØ)É'G2üXÉËÐv>#x\x0011tÐ?µIÁpÎïI>\?|ÛÚÎXÖ\x0004.7\x0013Ì±Y8¯\x0002døéúåk¸¨Í)keRÝêAR-Ú\x0019¾XÂ]GVÎIîP§\x0012@ôÞ~CN7Ä=Û3(\x0016ØðV°}P3'Âò!­V, îVl\x0017ª7lÈ4Pf
ö^ç!qS£V¥pX\x0000äÇP%·jÑAR¥< \x0016««ftK£úfTýØ¨\x0006®hÑÆu\x0005Y\x0014Ýi\x000b°T
Qâ#¨Ô
\x0015\\x0013à\x0007YÃLýB\x0007«lYå\x0018kÉcÖ:PZ\x001cu\x0014a¦ö|1ª\x0012ÍZÅ\x001f\x0007M\x0000ÝèXi¡h5-V½\x000eÕÚl@'ªlÀO'¯\x001e>|XêUyêÆ\x000e2¥ï\x0017ç\»¬[øéÕË««E°h\x001dÀî4ë:aCÑÃÖ|\x000cËI÷NÎ¨ÖuÀV×\x0000[÷Eí5Ü\x00031`ÛiG°,ù2\x0019o^\x001ae
ßU
5²j1|òúæÃÃO({xÇ>ÃJX*cÑ%EÜÌÕ¾>»zùöõë¹b~"5
©\x0019#üôà¬8-%Låàæ\x0004ÖÖ]xTÉ!ÔÔÄ«à¾@³/¸%UsåQëªF@­Ê\x001a{Pm(q±ñ8%0ÒlXÏ¤\x0016£VÂZ	\x0017ö »êwM|iS\x0005ÏL`¯fÊE²jÑ°j1Æªc.xÎ\x0006Ó/\x001cú,
Ø¯aÕvÏ\x0002hÛ4\x0019¿¼»¿Yb©PfvÆf ô6\x0016yPµU\x0017gs*cV\x0005­¹+híÁlPµ\x0011,\x0011¢wìXÍ\x0004w\x0017bÖ¢\x0002º\x0011\x0015XÎ	¦ÅQÐUÍ½Ðë\x0006²3]\x0005\x0017sV>5rÖNõbN\x001dY	Ð(AzY\x000eÝ\x0000	Ì:8UuGÕ nú9±zÑ\x0002\x0016*¿²ôU=Ü)®\x000f³\x0002"ftýQ\x0015¡Z#li\x0018h9gB\x0019åïã&\x001d¢Ui\x0014P¨<«Ç?þãý¯7_þ±dH}à¤\x0014'ÃiiÚÎSI®s\x0012õêìúüÙó³·9«\x001a\5k¸«±CÁ\x0019jß\x001d¸^\x0005îYkyE\x000e\x0011V%¬þI½ù=üëÛûÛ%Yº(HÍ"\x0001°éÙ§\x000e¨C\x0011Â\x0019\x0019è×'Ï^þóÛóËó¹\x0004]Â­\x0001WùA\]\x0016ÑªäsX6ÿÒë¹»\x001c·Z¼(*Fq=×\x0019m©;à\x001aÅ¸ó½Üã6£«G×rà5 Òf¦åÇgé&³úh¬i\x001c¤Ul­Q»Ô\x001eS¢,NÏy\x0002KhK+·2\x000cîÚUa^Ý~ù¸,Ñ\x0004ö\x0013_²1ßÞ\x0001¥7¥®y®=ÜÕùÛ\x0017ó9&\x0019´ªk\x0006Ðª¬¹\x00034\x0008VÛN T}\x001fyP\x0001t¦¬y)¨\x000b5¨\x000b\x0003 XR`v TÔ¬ÃN%`¦\x0000w!gÝ<\x001b8ëæÙ\x001d Nå§K\x0004Õ§úÇ¢M¦^V>\x0001\x0016 Ô	ìaH\x0014#¬\x001eûEQöÑ\x0003^\x0008Úô×qU.Pì\W*\x001eXÐÉRñ0]¶\x001cÔ7s¯üÀÜ')]\x0016	îTQ6Oð¥<xN\x0014ú8©L\x0011 ªøZ¶øúÙãÃÝ?ð¯>,i]¥©å&TS\x0003J @N×9ä\x0007¡g×//þýôål\x000f\x000c^Ý\x000b\x0000¼ë%G¹D[\x000eZ*Vt\l\x0004\x0007í\Ë¥nò(kò(W["ËÙ\x0003ÔÇÙXt	Ã¤f/ºª_\x000faµ´ÏÝìX´A\x000bFê\x001cãrvw°s1®\x000et³¿ÐÍÞB¿º¹[¤((c-)î/æJ\x001cÑðº:»\x0017A"ÖP³1V¸B*Z\x0019Ö\x0000\x0012*¿ÏÎ5\x0013]ÎZ+ý'ûB\x000baaÁr#dXÑT¤Ï\x001dÒeÏ!ZJZ_)EåwJöqÀþã|ä^R2Ì¼#wÀÖêÐâ±c°¡¨C\x001bðÎ#½z±@¥<®¸ÕÊÕÊ1V_bsx9#q	pË
ì\x00115¿°®Ù[nlsYl~é\x000b,E¾¼áZ\x0017¸I\x001eSJ\8²»lu\x001aÛ±ÁU»¯ _ÂyÇéÕÒËy[{W\x0014\x0006©\x000biåêjöæñ\x000eîf?ß.»IÚ8-%þe¾QTA¸iÇ\x0007~zs}\x0001³7oÎgë~\x0013®U5®UÃ¼\x0005çá2kìH'Yz\x0014Ü\x0004Ø5ãë\x0007ØsLá\x000b.Çm¸(½\x000eo\x0002\x001c\x001bà¸
8ûÂ
+¶è0st¡æçÜu}9°Ü[Áb8¾cJ\x0005®ú,3\x0002Äqî¹y	1Á5{\x000ek¬÷ÕýÍû,ôtóÛÝç»·'Ï¿|øp{¿ÈÃÑ»^$\x001dM,mà\x0010Y8x{uyö,k>½ºxsvñâüäùÛ««óË92eLTîÔPðw·`Ü\x001eovÀÃeeD\x0016;²ê%e-G²\x001c;ð¾;¿¾FõÚ$\x001eðòíìÝ)±\x0007Õ°\x0007µ\x001dÅõH~$p@*ê\x0012ùkQÚAî³ Ô®MG©r=}\x0005Ì¨Óðì×ÛÖ9¾Tð[@ÀäÛtuâÊ"i§{:¼=y\x0005Ä(ÒðìùùÙ¡«P·u(­\x001bÚDÍë\x0004¸9ní,wÙf®\x0015P'¶iÆÚ¬\x0018kã;§MÅÎ÷TÎaÓ5RÝÔ¾\x0019l¿f°.®(\x001aZïrïfÚÕ,ÆÎå}L\x0014\x0016$î¤9Â.|¼í(í#ï.bFJÃp¥æ$/Â\x0006¼>?R×gõÞ«\x0011
\x00004ÒW
Cýüæþ\x0016,ø¢WNj\x001eõµ<",\x0015®G<úü
a´]\x0001\x0007Ö#\x0005ãx]?Es?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÚFlÀT´¯\x001f?ÕZ~ß´ýÎ÷§gª>Y-ÑQÈ°gìÆìÊ÷þç\x001dîå\x001c`K´\x001f\x000f³ºÄQgi\x0011P¾·ñ<mÜkÝ\x0016Á3íwõ7<ç²sJ\x0008»\x0000v\x0005\x0005wÁÄ´Ìå\x0002öèí$
\x0004/°å\x0011ÐR»\x0008ð\3G´1¦+\x0013øtN@\x001f8i¯0WÎµr|¥Í{u°aW*ÒZ£
ÆWeÌ+y»\x000fË½ãéøÁ BÒÊ\x001b\x00125ÜÅw¥}%ê½ãW\x000bà\x0015Òp\x0002îhV¶&æ\x0017ð6¤­Þgç©ÚùÐúm0­S[t¬Û^'l\x000fØå} SAï\x0014h~\x0012ÆT\x000f5sÂ_  óOñ8\x000b\x0019y+<µ¾òzouÚaÐau°r=]ÚñBrÒ%¦Óði\x0002\x0007[	HÝKúµs´ãëe\\x001f\x0014x{ÝZ3¯Ûð\x0018~p§ªÆ£%®\x0003Íbm6Þ\x0011\x0006t0Å0á¤=¹ø-ë\x0014:±¾ö[{\x0019\x0003®\x0015]Â9|/it\x001cbíb0±\x000f[0·÷¹ù m{\x001bc1©<ö¢ð\x0010Q¹5GkÀ\x001c\x000b¶À57ò\x0008îý²/,#q\x000f\x0000<Â Ö$w=µ\x0012¨>0/Ý¾ô[c·\x0006]\x001eµÌÒÞ_Gk\x000fü}¹½uíL9YUÁÌ®ò¡ðVÓàå¥÷}¹õ$kÀ´90ÀÊí²/Ñ2xÏ
Ý[º\x0005KWõ\x00130j\x0016[l\x0004kï\x00137v&ndYnÖ~6\x0001{²ÄÌ,qÑ¶ã÷ù\x000f;ó\x001fÚO
s7\x0004yÄ)-Ë¸6\x0016ÀÚ{S±°\x0003\x0018bY>s:WÞÁïMe&W¬N\x0008µð%R5O¼[YÀ]ß{SìN\x001e@;\x0014ïÇ,_YîÄËºOXHÄ\x0018ú0ñÊÙIùq1ñv'Þg),d)bD½Ðæ@È)Î-»â{Óÿ}.ÁB.A%SÑrà7¢óü¦½)Çúûñ°3çòÄ7K\x001b
ýÞ\x0018á%|\x0001.h2\x0002ó¿w<Ö8ÖÀkãý×"Î¯ER¹#Ø\x0019/\x001cºÏü¹{¬j¼wÒ8´
·}gµF* Àô\x0012\x001e_ºxïIqzRö$Û¬}\x0019Ð\x0003_\x0002ªìÜò«÷\x0011F\x0011F\x000eØ©\x0013µG\x000cß¡%0QVÑE¦ÛxÔ¦\x0019æGc) £Éä¥÷û+Ý\x001fj
\x0000°ÝO»,sUÀû¾Üi3Õ¶^\x000bàW¾ä\x0013U ·ß\x001f)¼Ïs!Ù\x0005Ç´\x0018·Y6½%píýS×ÂSW\x001fúØ\x0019G\x0004e
(Ö²ÍØï\x0016E/ÈJèô~ÑÇíÞv¦Ü¯½ÀÚeÛá®nº~U6Ñ'û3-óLKÅ \x0002\x001eù\x0016HÜo¯à\x001dýþPáIZI¡¡ãÈpX¸Ü19Ö÷~Z
 ×÷\x0008¨¬¤È¹\x0011ÐÀïÏ\x0014Õ\x0019¸\x0004z\x001d-=s\x0016Z3§
ýþLë<Ó
\x0005{c2ß^Õ5\x0014ºz½?Ñ\x0000\x001aI¡
\x001d3ó%\x001bÎÿi¢­¡ßh\x0013M\x0006#;ùhÐç4»mWZÞÿþiçài§HÅ\x0013:6Çì7KoÉys{¢ÎÀÊ\x000b\x0006\x001f\x0019­¿%¸®½£ß¨ÇWU9\x001aÞ\x0019º\x0003¬Ñc×ÝýûÈÍ÷S&¾\x001b
·nÌ
âúEj{ð0Á«ð\oÝ>H{¬&T¾½L¨÷g\x001aÍD×b\x000e[j>¬\x0012L.à-oäîc\x00187c\x0018·Ìiý´ôåz1MüÀÝ0.Â¾Èc\x001dÊ\x000bx¢¥×¸¢·}¹\x000f2\}QÖ\x000eÌe\x000fÜtW×éé¾¶´±»\x000f2Ü\x000c2äH#êÃ)ç\x00023SÕò$JAo:\x0019î>Êp3Êp^û{`g<ìÕr\*ßÖv¦÷QQ\x0017(oËÒ¹./àü©ö\x0012e¬l¦\x000f¶üãwG6Ó?ÿôõiMÿé¯^>~xÒ\x0019Ó?|øúÊ¼Ìb|µºß¤o<\x0014SÓ&\x0004ß\x0012¿)\x0005µo\x0013Þ¯óBÊ»ìMk¯½ÑÐ\x0004nTÙFn.®½%zõ\x000fÀvÍN²ï\x00147\x0004Û,Ø\x0007)jÂö\x0013[m0\x0010:jó\x0017Þ\x001buÑ\x0010Çn\x001a5÷Ø\x0001°\x0013Ö<\x000b\x0004GDö	\x0018ëK\x0019 ãv\x000eZ[m0¯*Hë²Ã>\x0004°§OW[ñå\x0010-¿d¢\x0018\x0018»î² \x0001Ûâ}\x0011M¥v£Z2ksÕ>ÎwMª\x00006P+å£îaÙr{²\x0003~YvNÝÉÌñæ÷N²\x00126K°ÖÞ\x0015´Q\x0000:À²ñ=¢ùL"\x0006ÖÂ¯\x001d\x001d\x0012ØßR÷à@=_YßºíN\x0014!Àý\x0016;)\x0016N­Ì\x0014!\x0001oÃ-Ñ4Ág¢Iþmó3\x0014\x001cßQ\x0012|Æeåé ÷LàÀ#¬\\x001b=Sø§Åµ\x0013\x001f\x0006°§gæpn£.<Ó/wUíûÓtó4s¨©Øøì®©²TW­­çe#­\x0000ø<Î\x001cq ­gÒ,u.·Uík÷Wø$­¨\x0004\x0006jHéÓ*W¯ÕùN¼\x0015\x0000\x0007[\x000fB&çÄ\x0018FXL¥Ý\x001bû\x0003°çeÁQ\x001dq\x0019\x0003]Sb>¦j\x001cn\x0011Î?¹Oÿá\x0018á|þúÏO\x0012Ú|ø·ù×?ûòééë×
g¡êXöÞSlro­<¿ ï?P8sÓn\x0012×¦\x001f\x001eüÔâºÛomìvîßý÷>þötîÚ_ôWÚ[òÚýE\x0012Í£Vß¾\x001e½&¨gÌ¼Z	}NßÛ9ð\x0014\x001bÑëÛã®cÁ S7GÇC·MòT\x0007÷.Po¥|[æn½ \x0000{\x000e.\x000cJêÉ\x001294ñÎ\x0011ßµú^b[¿e\x001d\x0000»`U£¨Nd&ì¸¬»iè­ß2ÀÆ©Gù¦±\x001d¢LÀN°n\x0004\x0012+
 È¼j¿O´#ä9mÊ«þëL5Gaf®ÚQ}­[\x0016\x0000z
¸/:ÈZÐ±ËfÛ}¨\x001da×¹ìc3õkË
­"ãê]g¯ù=\x0015è³2Hh³#Õxå\x0015¿\x001aq§\x0005\x0000·´pÈa\x0016g)ù*\x000bOËÊ{j÷Þ--¸¥ ktl8¹¥ÍM04M³-ª\x0007p\x0018(Z\x001cp0e5=]8\x001baÏwß»%L\x000f\x000b4KÖ½\x000cAµÑ±\x0011TN
\x000b\x0000\x001eyÝÐüf,±¤tá\x000cnúáÞ1§\x001a½¸O\x0004\x0001¡¤³ÔÊä­_îªÎ5¸wMiáSõ(Éç4Ò=`WyùS7\x0004`\x0017ÀöÈ3Ô@T\x0015lzëÈÂýñ­\x0003à\x0016\x000e\x0005\ò{6qzÈÂí©\x0019bBÃ08ñ¥Ó®+|0xk\x0018ÛûV|Ý:\x0016\x0000Ü\x00118Þ.ñä=\x0001Oìçg\x0014\x0007\x0002/`ò\x001c!\x0003k[Å¦\x0012;'\x0002Çïaª³ãÆ2Ú¸ÿ\x0000\x000e¶=ÒõrMÄJñÚ\x001cÀçÙ^\x000c÷çé
a£\x0017Ë#	-Ï
ÔÄØé\x0019\x0005Ø°gÅ8åTéáªØ´ã®WÒ¿»ÿþÈ\x0010(¾Ç++ð%Ï²\µ{2÷¿çøÃ\x0017è§!ï_IøÏ¯\x001bíf%\x000bSV?<Dé°Ô$ù~Á\x0014¤ÿHÑ®\x000e(ÿùtm?\x0011N×Êæ\x0010/Ó:»=³ÉJÓ'Y?M\x0000\x001c\x0001\x0018\x00186ÕR25Ñ\x0010c\x001b,¶~:\x00008\x0003°Ç&=\x0015¥¦~¸ \x0018{Ôz»\x0003v\x0005l\x0014Ýl²Ô¨>'Ø\Ñq\x0016§ðh[Üj\x0003Êe©õbÑÂyür'Ò)\x0012\x0000pØî±9Å,JHYä ù;\x0004ìL\x000bÏPÇô»Eå©Áfbâñ«7Á¡\x0005P<\x0012õýkìõ\x0004_9\x001e¾WÔî·\x001c8p:ß\x000er³Ñ(/Ú0%ô0}û¤\x0002¸\x0007LeUì<-|¹-ìaÙ(Ì\x0017µM<,TNÛò\x0000â¨Rçùc-àÜ\x001b\x001a\x0017`ûäMlé
Ð´--\x001ffbrës1î÷Ûó~cuÔ;
\x0004tÃ\x0019Ü¶÷ÜÖ\x0006à\x0001vÅ\x0010\x0005KÇÃ\x0007¿T¼Ó±s\x000cÀ\x00138P¦/³ÜÅ\x0002[i}ù\x001bÝ\x0010°Á9sl=\x0003;¾§ÓÌMÅ4pÁðºaS\x000cnó¦ø\x000fÚè\x0008\x000e\CW\x000c\x0016ó
GÒYÙ\x0011\x000f".ßýøÝ§\x000fßÿüüéËË»_}ùüý+\x001aòMd\x001e¡¯úªTÌ¾eßVaX\x001f@¿ ±ÖÎ«·¶8\x001cÞÜ7¸q!ÛôjËþ\x0012\x001eàðý+Ùà0\x0006¥}\x0010¸2ùr°©l\x0004\x000et;ß;>àZÃfÛ\x0012Sa\x000e9©\x0004>\x001d¸è¨XÀ.Üÿv¾.9°=n&òd}iêÒ\x0000ó3V_Ë®\x000bÕÎø£.\x0000ÏP©hv\x0000¾~!SK¶^
ËÅÓÇ°nO§\x0001\x000eAA\x0013Þ\x0001pÏÏ8\x0007¦ü£|

\x0000|\x0006\x0005*óØ¨ô\RrËi¶Q½û;{ë­æiå8ÅY¥\x0000Ü²òó;{\x00072\x0015×KiÊw`+qùû÷\x0001|zª\x0001\x0007ÜÀ¬øÄ3Ïw>>â'8\x0013VéÛ]èIÙT\x000cûS5\x0014À§\x0007Õ\x0018\x001bb¬ÜS{sÉµø£:\x0000\x0013)ÓÛÒÊÙZY\x0002\x0003s&¸G.,
ci\x001aîÄ)LÎöµäº·shs¨ê¸JÉ²ÄôuÙ®>yoç¶tãÄGÕ.\xjå¨\x000f\x0000È@ÉÔé³\x001daQ\x0012+\x0017ìÖ«¾\x0005b,Ûå0CKX\x0003ËÖ­ßöÃ2\x0002Eù6\x001a#ÑuK\x001f:\x000bãt÷fèÁK_	ïILâ®°ìJh»rOy\x0000×æ²dvN4ñÌ¬\x0016Ýòz!'8ÄõÑ\x0005Q{dþ.?7|mÁï¦=\x0000à\x0016VßóÂé²U¥ÀeámÖÕV\x0013ØL \x000f2(Ã4pC·JM«­´]¹7ò\x0000"\x0018&¾ç§\x000cE+yiµóµ}%ÂýE\x001e&ñDG\yºSP\x001f ¬­Ó²î¶á÷\x000e\x0014Ò\`àI5'\x0012|.u¹°\x001aö½ÿ\x0004ð\x001fb¹íVAÝ¨Rì\x0002\x001d\x000fãÅ\x0008»\x0000vF2*Ñ­R,|i]0\x001bYz\x0003YZ\x0015h#p2C¹±\x0016ðF8÷\x0017m\x0019hOÇÂ
6ÅsM/¼n<l\x0006#Lq¦íæI>Ü
SÛã\x000e ÁNJ ¬K¤\x000e+=îT÷¥¥¶>2\x0000ÃOrÄ·úò\x0010¯_V®^¿\x0011¼'6\x0010¼Uñ\x0002¹égvjÍòä\x0015Ï\¥_ìOÿÝü·Ó³ô×O_?¾ûÍ×'Ößý÷?JS ,WQ¨#	èyÙ«\x0010ÙÛb{x{P\x000f]? ýPôwq(ÃU\x0003¥ôIÍ=§´z.`ã{7À<\x001aÁæù¢KÖT í¬\x000cÐ3A¨J¤s¼É\x0013Qôô\x0010a>/ñ\x001e\x001b\x001e\x0019r\x000fÌ\x0017L3\x0017nÐ²3\x0015Sk¢×ë§	°á.ÑÜÔñÊ^ç\x00136U«SiSRÖ\x000b\x0007ñnái}¬4®b;ÈTÌ®\NØðB\x000f\x0011²ÈÚÎÄ_Ôäe·W×z\x0001t!hË,r¸ã£¦|¤A\x00036¼Ðuê*.kìKÖ±öé¶\x001bdBò¥\x0004
ØÞ0tI
)·Àk«\x00008ødFÚN\zø_²Åº\x001b\x0004ÀÁ)s\x0004u=\x00017ïË²)'\x000e	 O
\x001dÂ\ÏÂåûÔù)÷>iñáßã¢yDvQeâÅ\x0002ã)c1±1c¡sÕà(\x000b©\x0013«áÈQ=\x000fûáÃç¯ßÒ!þõË§ç\x000fA/ÿ>ÉlËíâ¶©j]t÷O$öú¶\x0014ÔS¬\x001fÿ¹Dl?\x0018þ0ymD!¸\x0013x­\x0015ø¬sñÔé2¡¡Ó¥ è`;ÊóT1¸`Ô\x0001\x001bZ]R\x0000îij·òÄæ'°DrîÔé2¡¡ÓE®\x0017Z6>kje~£.ûpÃ\x0003t¡UCsD\x0007QõeÕënÊm¡×J'ìÂ²µN¸4ÿdÞx$Ü\x000184[ù
Ý«mágèÂÝ±fC·\x0015Í>óÀgmÿ	Ëa¦c#Í\x0004Çv«\x0008s¼ÚÊ=m¹á¬Ü

\x0000>­P\x001e@m7\x000bkÂÇ¸®üH¹\x0003pî¸'°®ÜÒynÞsî\x0000ØÐ\x0001=)4c¡\x0006\x0006îêÐu\x001f+

F\x000e¤l\x0001²Â\Öí>÷\x0016Mdè-:_äßü\x0008Ê\x000c\x0013|\x0019
\x001d¸L+÷d)\x000ceï-àÐ[Q\x001d+&²l2¡\x0012ÇÎ¢üÿ÷v9ÝVèT\x0012~ª~(ÿ?¶lWÕëÂW.Ôk!
KQJeJ\x0019¶e@@O£gÐ=I¤÷&¿s¸\x0016É\x0013ÒCÜ(Ù¤´ò\x0004ÉMîßµà\x0008*\x000f\x0006}52WjïtJâ.O\x000fÐ0å\x0012\x0003ª¥ß6ÐLÄà¶1)­CK\x0003\x001b$JqÞ\x001d¤®ªÙq5Ùº}#\x001f\x0013U´\x0015¶²°Ì{M,_Vlï¬_'¢\x00068NDE ìU±<<§C\x0002Ónú]
`\x001aJûÐm%/(Æ[5Í+ÞGK	\x0000°-|¸á\x000fw¼ä\x0012\x00059þðL¿¾ÃqÚJuHð¬\x0004³Û¿Üw²Ýë3îazÎQÂ.)
¯Êd÷áF\x00132·8â­r´8ª
\x0005lÆj\x000fP¥É¿ÂÍX¶óÈ;÷öúÀ¸ÿx;ð\x001dU\x001atå\x0003áO7¹k\x000båwï¾ùø\x001d^õçw\x000fÿû>Þ¿ùíýÃ»ûîË\x000fO\x000fïï\x001e\x001eï?¾ùÓÝûO\x001fÞüîã§ûwï>¼¨§\x001d­\x000b8N(!i	GËWÅÉÑA[½3íç~=ö8ÍìCõÍ<íBÊª¼Àp#«sÊºvRÚÙú\x0000ú´>¯o×\x0018¶PA+lUÔ=ÃÁ\x0019Á®Ec~º\x0000;\x000clkAµZ'LpJ$j\x000b\x0019ê6l\x000ew&ýùopz¿¹ÿîáý¯d\x001e>¶ÀPg\x001d¾ûðþe#Ãè<÷cT¯þHûÑ49É\x0005M÷jAþõ\x001c×d½Ý\x0015.ÏÛ\x001eö?v°z\x0016°¬!P;p
=VYçgOh\x000fÐÅC×E¶\x0008ÎrÔ5¸6ò±\x0014\x0019\x0007ø(2\x0006­ë\x000epùp.~¹¾¼7,®Å\x0000?]«#óÜiÛ\x001b\x0006ö(7hÆ\x0013\x0006¹³Ñù\x0003fÕM	lZ\x001ema!\x001fØ\Yo1·m¢Á²Tt¼$¾Ç)\x000b7@%É\x0001ip¶ÔãgÛÂÚ®\x000b%/´l\x0003{Ð²¬lé£\x0007[uË-\x001e\x0014\x001b9ëLÜhi\x00138|¸àß&yäéfsÓ$Àn¹Åek\x000f-ýVÔ\x0003Ò\x000bZ¢\x0004Ü¦cµi-\x001d}Ü\x0007ë­ÙÒhrÍÈó~ÿðÒ\x0017¦<\x0016XÕòJ\x001blÇ\x001bêLb]|ï\x0015Ý¿¨|Ô7ËG^ç'öhm\x0003øPÚ\x0012y]C\x001cí\x0000°Áwøh\x001cU¹U\x000cöc	v¥÷=x³+\x001f\x0001´'èmÞ«A[Æ®»1dÀ\x001e¾CÑq\x001c\x0017M[ry¬å%éL¿sP\x0000Ø\x0011°-D\x001c²$®yñÑCæïnÉù}\x0002ì4°5}\x000fØ¬!ØØ  Ý\x0002ö9|\x0004è: knFùìÈ;©×<ö^\x0010k[ðÕ\x0007Þ"\x0001·ØÎ¯¦Äíl\x0005±\x0000\x001c\x0016|oûÏÞ\x001b»¤\x0011\x0017øò:8æí@Sms2Ýæ\x0010.=\x0003{ôx
v\x001aBÄ¬«~xeðÞ\x0019´g\x00008O0Ò[CB.XÝNì~ó6öLÚ5\x0002ìÀaÅ
Ö1uU<¯xîs%×Ûé`;
\x001e>üÆt\x0000gÜð{»\x0011b'ð\x000cÆ\x0019`;`Ý\x0011¶åX'ú&ãîáwO\x001fÇï§Ç»wú\x0004ÎR¬¿~ûöîÄ¾ÿðþMÌÿíËK)°[W@îÜ\x000e#ñÅÁlÅçWô&î£å\x000c÷\x001d2z®ÆâäÄ\x00065xLÝx5­mFk`CFK	Æ\x0013% yt(k-½xu
\x000eíQÇÅ7®I§é²ÈÌ\x000br­´âÕü\x0008\x000cì8rÉâ\x0014jªé÷ÈºWµtfÚtýái|øÅy|ö,+ø|Ý\x0001øÈó%yfAé[É¦¨V\x0012Ï\x001açN6¯¿<ÃS{h\x000eò{Ñ~N­Ä5'_w¡Ä\x0000/@6¥M!ãËm.4qY³åéîÐF\x0014\x0016¹]!'ì\x001cFWÎ2²{ÑwG×KolÇ	\x000e²\x001d;l¼0Y^zAV÷³\x0005ËË\x0004ö§ïÿf¿^nÓ¯ÞüûÝ;4ÿñÍoï?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-01.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-01.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þãÝW\x000fÏ?ßHä5ä)-f[]ì\x0008u<&g	½wöuºÙé^¯3qdÃ\x001a%\x0007Jï\x0001õ\x0019ÃòJ¬E\ÆÜú\\x001cÐã¹Py`è»oBê\x001ffã.\x001ef×`\x001dÛÂD0íÒ\x0006¹\x0000£e´J\x001fSÒÖ÷VÍÙìØp6½\x0012 à&.Ð\x001cYA<³Ö\x0014±\x0006Ú\x00076\x0004Ú^ió k#aY hN5ÚîÖA#{è\x0002Ûm"F5Fû­p»\x000e@Ø±E\x0006nÕÔíØ\x000e4u]á\x0011DJa uOt3\x001bûHØx²Ýú°¼e4¡ä5v]úº.\x0019\x0003¹Ns\x001eÑ0
\x0019\x0006ÒéÖ]¼ë­Á¶?	ÃF4 Ü`zè4Ì»WWã\x001b\x0018è#7 ÿ\x001f2j
h÷4NÊcÀNÜt\x0015^?'u\x0015ª(\x001eNî8dÂaÛY`ÂÊvmjÿ\x0011|êÑ£VøËù??=¾\x0013ã÷|3+¦ÞïÑ]¨w\x0016Ú|i\x001eÎ§0
g-nÄYÇ_\x001et,ÊHüÂ<ÑÂ
/ò[\x001bGj-\x0011td°î>\x001eÓ1'dÝ-2ß«\x000fkÆ:Î¢**e\x0001\x0006XÛô¦6é©'¸vÏ\x0013ä¦Ý\x0008¢íØ4À§bX-ä\x0016Rµ±ÿ/\x0012¯PùÈ»ÚÒJé\x0007ôð{9\x000f\x0008çXñO%·§Fº®g~\x0002\x001a"Þ9´½Úxå¸î0ì¢_kDw`[|3
¶ÿÛÊ]A\x000ca§>S}3³8ÎQx¤¶&¥<%~5fW¡5\x0015Þ¡\x000cé¶\x0004G$f\x0016rÈÕþÌÛä«;6ä«]¥*¦ËÓÉÞp×¬?Tgë¦\x0007ª¯.M#v²\x000c\«£ÛzbCô\x000fã\x0015íZ¡\x0017hy°ÉËÃü¡L_×ªÆ
Å\x0018âpKÄ\ñá6ó4RÎÿÜ±ÿìr&\x0008%^Nº\x0005+\x000fÞ] P·ÏÐû»¿züæþÃw\x000fÏ7ë\x0015Õ\3åZmîbn36\x0001jÍ¿v'Dje ù\x0019ZCÉÚ%É §,.(Hh¿.É8öhJ÷\x001f×±,\x00074eQá\x0015Ð½(\x0007q\x0017öÃ+ñnº	;FI
\x001cq?ó0Ä¤3¥¦\x001cbgÀð\x000cIH
²\x0011Z¥\x0004nìTíùØÕ/= ¡ì¸fU¦	»²hNán\x001a×\x001cÉ\x0001
®D5a¯<\x000b«dÎQ#¿\x0000\x00072<\x0015ª\x0007	Öy§äMsX`n
\x0000\x000ed·jâ·Rçx£\x000b[Rû×lT¥ð¼Ç¡¬U\x001e;\x0016Î1qÊy7AïµÝÿ\x000c´%C§£NÃ:dÑïw%Î !D$uPqRþU
êA;»Èþ1	\x0019ÕÅ©b_ÙÓ¬¶ËXÝCÇ&&è\x001dsg5²êSÕwJSTU*\x0000ítJê½²°6\x0010\á\x001eªþ\x000eQý¢ÿ\x0004!wÊÜJP¼ sê\x0003v£é\x0013NÒ\x00075ÕÞxsÌ&¨?kù/í´ÙÊ1\x0015e\x001b\x0018^ÖMáÇ¬}Ã	ß=È\x001fî~ÿôýã­*-f\x001aQ Ûu:ªv>@\x000eG\x0003B=é@?õØÕ_b .Vr#Ä%e\x0005OK³×tn|Kä\x0001cÿ]ÂY=î\x0018T9vtÊIÐÖª
gÈþW.yCü[R?nÉ\x001bÎUG\x0006
g´èïh4È¢Þ±NqU\x001f÷p~í×Xð@Î¿vÍ\x001bæÒìý}$ò
Þã\x00078ÏJiKÅOZÞ¬û;wS\x0010~:Åþú'ØmG\x00126òC¨/ÉÌR¦n"\x0008kwM,óôîÛ\x001bY«L}@)[\x0019éu>ÀKÙ~Á'½Ú	¨\x001e\x0003×úñ\x0001¤bHHò}xz¡?\x001a\x00146¢;¶\x0007ì<@-{rí,{J¦ìæ¦gÃN=\x001b*w\x0013\x001d£­ÄÓQÉ"îCÌwy;1æ½ÎÒ\x001dí *¥ÀdLi·\éò'«ö\x0005V-q\x0019Eç­yGÐ¤ÞR\x001f
´cÌÛ1/;â \x0015\x001f[;X¢-¡æØb£/µêÜ±Ã0ä\x001f»î°Îd9°ÇL³\x000bôÒÝkiÎ/\x0019ñKj#èøÕNdü)*N¹KîÇJHÃÎxJÊ1r¶qñ	z\x001aÙsüqéìÈ#ÓéÅ®
íà\x0012»ARq­Î\x00147tù=èòíl²RA¹c=OPk´È´\x001d;Y<Ü¡ñ\x0008/Ø1s\x0017KN×Ýii\x000bïØ\x0011\x000f·V»¨j\x000cT*×\x0001¼®»nzíY2\x0003Û\x001e¡åQÎÖ\x0010®J
¡ËV_ÏM\x0016k[Îþ«çûwò¾øáþùY3Y7JdùÈõ@GS¥ø\x001c8ÀF©ï¯=¸T"°Id­M\x0000²kêË@\x00138\x001c$!h&-Ô4M:Ê¾7o \x0003CÕ\x0019\x000b\x0015{\x0000Ô³¯ÑºÃ6åÛ\x000e
Å	ç
ä*gndHÁÌ>c\x001f\x0019t\x0002\x0013Q|¾À\x001e\x0012ú³\`²éDåïÀ½V2=¿Ót.%à$0àS\x0016úhõ©;°a¦ÍÔw¦Y\x001a½®\x000f\x0014aÇ.ª¼\x0010:¶\x0012ø¤\x0005=gÄ\x001cO9í®½6\x001dØÐ\x001cfi\x000e×u;\x001e\\x001cÓ$¼\x0019;yk\x001djO4d¬Ê¾ãðø±\x0010\x001dËÕø®åÃ&·Ð°Ã.¬óÈ PIad¸hxà¥ï¢2~õ<°AÖÓdÌµ8\x001byKBÊåðN¶ÛÃÍ±\x0006'¬bg\x00122÷¡ÇÓô\x0003Ö²Ê
e\x0015S=\x001eo\x001f,µl¸\x001a©,\x0017õZv\x0019ææµ@YyÀÕªå=±<âÁº®Ïz²ÝÁávÃ  Yv=ñLÄ¸t\x0011ëMê³AÃP^
f |2Ü\x0013Ø%e¶ì
e¨cCUùäÝyñÍjNâÉ§\x000c \x0010dX\x0013M§¬»\x0018¦IÁ¿g\x0012v)ìÞæ`Ý\x0005\x0013«²óº§ù\x0014©¥\x0012ãª,y`\x000feI«mÂ`½uä%\x0015
ÝÄ4Q2Nóå6YÛîËÙí\x001c¾ªÄ¾\ëäuÞxv²î4ªV6 "©\x001dh¼ÍTäÐÉô\x0004YÝ­\x000e»¥£
±Í*¨\x000bÐÓØrØõtç
\x0011´CªµÕ\x0001£ðæliî,{Òñìs>ó\x001er\x0002ì\x0012iæj\x000e,¶oò4=·%ö7=m\x0007tÍ\x0016O\x0004wdâ¯ªY¢\x0003(§»³<9yÌ\x001f°\x001aªáá\x0016ÓB½·Æñ¬bßE<W«÷\x0000L'g\x000b×í$Éê&uv1\x0001ýto\x0013ÚÇ\x0001Ç¶\x001cò\x0004 !\x001c6\x0013µ>äí©×ëô_!£¹\x0004\x00033wbihh*N\x000eV\x0017Q]\x0015lÆ\x001e
®üÓØçµ ð1\x0019fñtÍ*\x0001Yúf\x0006üèÇ\x0002\x001aÑ^[|fÒU¬s¸tn\x000cðû_·ö5;Oêû_Êÿåýí «ç²\x000e¸Ö¡´ \x000e¡ÔÖmôª1xÛ;Ã5#çTT'	G`\x001bâèp¦Éf¶æå5öíÈ0C'@«xS\x0018 vîÈÅýèZûÆ/Ó¡/\x0013"Ì×2u\x0001Î®Fms»7mÑ\x00074\x0015Ô; eQ\x0014±\x000b\x0012\x001f{\x0015'nUÖ\x001dq(àà\x000cÍ¿\x0016cì¸d¦SÖ¼\x0018X¡.àØ\x000c¥c\x001fáSê0,ªµfvX½I6`n$\x001b>úùV¬yÕ\x0001¡ÜCîØ£ðLt¶\x001a¯`pv£Ú´áB¸\x000bá\x0012>ªb³"K¸iæ2Þ¦wt¬^ª¸ ^½ë¡~\x001euô\x0016ÝÓ\x0002õYI Ôb°5&8 r°É¨\x0015ýá2@*3SVÚuFËÖÞ¡#ä\x0004å{Ø\x0010*wåjyÉ±U»ë\x001a"uÜ
ÝâG\x0018£US\x001aóºâ	÷\x0019°«/ÖëF\x0016
\x000b\x0015E?¢?\x0011°hâ©|{\x001fÍv²jèëåß\x0003÷_'Tp1´ØÄØâÔü²\x001dûvÁ\x0006=l\x0017Àcª@ºÅ\x0013§E°{Sú&²ëØ £l\x000f22¤Êó\x000cÍßÑöe¯rí\x0007ôkW)FH4hê%ª6ð§´}ÐÄ*bu`\x000f\x0011+oÅÝò°lç¦-I¤¶lî2ó\x001b¿ÚÍBÞn/éY\x001cXåÇ<CwÂÌ&q}\x001a\x0019ä«Á\x0013è$¤ÊjùtÛXN[\x001dz$·Î¬ëK¹åNì\x001f\x00043¯²\x0000\x001fRsD¨Z->G!èÐfXí\x0007ÝÔ<è\x000fpG\x0002½ÉI¾Ì´ìÚä¶:v\x0000l\x0002U\x0001{\x001f7\x0012ìæ\x0000ír[\x001d;$»Î»'èLÐ¬\x0005¥Ð-¾Xu\x000eè\x000cÛ­:(cKZ¶\x0015¡#V¹E=µurHüp®¼·\x0001:X\x0004ºRù)\yÙ¡©¨m}\x001d\x001b}º#\x0011±ó=oIH=ÿtòÖ1AÒ\x0007c@
JY?\x0014E§î#um9¢M>¤cC\x0001TI#\x0018õâÃl¢Tb²
Z\x001c¬=´þá
-ë\x001c\x000exT¦$Éÿ0A·,Î{×¡\x0007÷ÎKX\x0006P\x0007íÑt&%ëZ3\\uå\x000eì¡+';\x0012±þi\x000bËø¥ùJºFì·â\x0004º ²>Qõmr¦ä`·5ò¼á&{ML:¯Ü\x001dývÓ\x0019tGØ\x0002ïq¶w¨4\x0015Û83¾3úuââì¸ûêñáÃ?\x001fþáùû\x001bEµÖ\x0013Q.(Eò\x001cQ÷Ð
ôE3\x0004õd£'4!A\x0006½àI/ï:+9é\x0018iüáE»Uné\x0004z\x001cN§\x0002PÁ×y,\x0018\x001e\x0006Ö\x000eTÁ^ÛÅé
=Nq\x001cYtäNÀ©:Õû^!·ô
G5ùl\x000b\x0015<·!ét\x0017îd³-¨W\x001aWÁ\x00124p|æ4íÏ\x001dÚn»Öæ\x000flèS3GNîºîÂ¤S\x001f&UöCðgÍº\x001eØP³5:\x0019\x0013\x000eNÝ l7íIôÝÑ:ÁvÑ­4±[òòçÞ9å÷@ð\x0004ÛÊêÉÍ|ñR7¯b3¬ª{\x0015#[\\x000c4Æúâ<ï¶
\x0010\x0010th¢p~Ø\x000eè\x0011±Ùâ\x0002¼übb§¢5$h,Ø]HaõX.Ø×;isðoàpGÖQðµÎc\x0001bVXûÉ;t0°l|~¯jµnªVÐ!©¾©m\x001c\x0003ÛCþ<e<ª£NMvf\x0012|¯©_´Ñð¾nH\x0007WL
ä\x0012þ\x0010¼\x0004ïNÜLÂ2~}¾¸~~ºw\x000cÙÚÉëöPCò©¼ü­kõu_¡6tMIÞÏ
\x001bj­ lÔïÀlx[îK~ýê"uhÐüË\x001e%fBRuy³És\x000bSnEZ+\x001d9\x0000\x00125F6;©´\x000f©3Ó*¦>eõ\x0018;2NÁG\x0019¾¥OÔ\x0019ã\x000cÜç'ïT\x001fú4\à¯«¥ª^M´ÊÀ³¯äu\x0011«õé¼`ã$L¹f9¬`å+OðNñH6a£*¥¢¢\x001c\x0000*áFyÍ(cÊ1æäX%-!c#vÒb\x0017©´0¯R>d\x001d¿i\x0017êÃ¡]HÎ-\x0008bMåvÚ\x0011Ûüs·iê9 áK&\x001cgÒÆG¾Ä\
­Ç²×\Ó
2Uº$Da\x0012¡uäSÒ¤\x0019Ü&!Ù±Çóæj¢>o°;\x0019î Íî2AkÌ|4Ì¯A\x001f(è8\x0013J£ÊåçoJk
ñrÛ¡\x0013Uãuì\x0010\x001fïI,8µ1Õ~à}5Rð\x0004e\x001f°70ÅB»¢{6S´Î°eá\x001dÃ\x001bX·*\x0018Ð´\x0014Ï|'ùw_Îækí|mõ¬,ÜNm×ÀD\0LÞ¿{@[w < ?¼{úÿïç»¿ºÿùÛ½£ZÄÕ\x0004å#ö\x001fJÅgTãëôÚ#¶÷\x0015Êuîl××<wL'JÁÕjÅ>\x001e¡ÀÜÊÐuy7©®\x000e
uÄLÓÒXEmÇ\x000f5>­@±ÑßêÈ0	ÃdÝ@¥E\x0003:ÍÐ=pÙÐ6\x001b6Ò6?nÕv'× ­ýµÐdTv¿\x000ezS\§\x001aª7zÿý­ØÏSºM÷\x0012ÑD\x0014ðòtnÀkwñW³(³KÐ7\x001e1t7
Ýuñ­×£t6fEóÞ\x0019íÈà¶ }¼«\x0012j°¸çV\x0008mÄ¨'õÃÈõCY4ÊØÉ%I¬Ìâ\x0013÷«rÖ²í&Ê¶­µ¢lkv¬«*áQaä\x0016ýï\x0012è­ GhVÐ9]ÜM-\x0017=M\x0012õ\x0012â	¶µ]\x0002{I9Þ3£(Ð½UÛÿÀv¸Ù\x0001t¶åÍæfÍÔûíW.È\x0001
\\x0010c8^\x0011/c:}nz­»Ü¦9Ù\x0012g`KXV9\x0019Ã4ßyQº´o*8}êK\x001eØÉ7°«;ê¹ßOÌgVÛò8k¤ÕG63«s0&ú\x001cÞ\x001a\x0017gÒ_/è¯RI\x0007ôJ²§%ÎÓ<¦p¨wkùU\x0005ç@Î°hKjÄr)¸Âyn3\x000f²}öé
VqÈÁÈYI§ì*¡¥qªOn{°4«(ì;ÁÂÔé\x0010zK\x0008'×Fÿ0 
\x0006Jú 99ÇD6uhZmèäøÅ\x0011{Ú¢\x001cj =é¶ÛÄB\x0015bi{qèäKÆ¡âiu8\x0017P|µ2\x0014*\x001bË\x0004Ý{ã6½\x001fó°
«ÓL&í\x001e"ªh'aÜ\x00070n\x0008\x0003½ï.\x000eì\x0010©Ï!O\x001fÒ\x0006\x000e}ðýE8¹6}\x0019
·#¯\x001cºwY§Vtàâ;i\x0006.Äù¸ÓÙúÒÛN\x001fh°:M\x0014¦\x0002µg>!væýPc-g/YÁÄª
\x0015á bG¾¬;(daÍAÞk[k\x001cf?]:Æ]VqëGìÈIí¬kýçÀ\x001eõ\x001fJ$¯¾R^En?µôEÓ¢q¹ykÈ|¹#d\x0016?°gó¯~ >õòI©F! +óù
ÿíoþùºq[&hÕÙøâéíÓß<><ßÈ]N}»Ôæð\x001düayvÀ\x000c$}<_]Õ<ëó´Ô\x0010WC\x0013ý×,dè´U\x0016\x0016Ï\x0003\x0018Cò\x000b¹÷\x0012¤õäwä4ü¬&ôLÈ4e&²´^îc´7ü\x000e\x0001X3oH\x0007'¥ù[µüÚH} Fjc	t\x0013A²|äSá.ÄÔZ{6rGF
¹Ä©[\x0015ì¥EWî¾SWH\½Îmoëbôp]u¡¡\x0015²j\x0016\x0001Km?ìæõìÐ\x000eÅiÉWÑ¤\f¥A\x001e(uøÊ\x001bá\x000eíQhÐ£ö¢
0q«ñ\x0015Æâ»
Ø\x001a\x0004vì\x0000j\x0015évAçnP¨¦z¯Ýxkv#9Þ±ArÜ\x001bº0ÚFÈ»A²)gD¾QÖ±PôP3MêÕ¡O\x001c`Ú> 3¯.Ö5ö¦\x0001±ccëîGb×ÕÇêØÕðnWÚnzd¿ó´ßÑ\x00176®ù/\x001f~~üùîw÷nöô&%¾Ebò"qâÄ³\x000e$qÔMíÊ^$}£¢Û\x0002}°/9[Liy\x001dv)èPØ\x000fèr}\x001b©Û\x000eì\x0000Ø`\x0011N]\x0000â7K\x0018É
Î¹\x0015ËWÂí\x0001=\x0008·­¤
\x0016@©Ó<­;°\x0012 ï}q#5Ú50Á8\x0014\x0015önþ[&ñÕÜÔ@×Ã~ Ãa×±1ÐÈk¹ Mñ¼ä^%[s©\x001d\x0019s©:ÿ
ª{ª©Ks´åçp"õ§Ù(Ævl\x0003\x0012©\x001fÃÛi8#ìXâ}`C³íe\x0014à5zcî@d]	í$·{Jö\x0001
'D§®XOÐDÓ\x00002\x001f{yoeÀwl\x0007­Í
Ï¦Ó.\x0006\x001a_Âto	²ºªûNyºëÅÃº\x0013½¨®\x0007±WâÒ¹\x001fZ\x001aÒ­LÞ\x0003\x001bºÔ«Ö8!XvcRÒ\x0002íä6Ùk\x0017¶­5_Ý¿}{#<Lc¸¢^È#\x0007WÅ¯t×wÇK4\x001bw|\x001d\x000e*;ÕÌàÊç\x0004Q±¼Ô"æ¹£}æÞ¾¾ wá°ÍQìÔ\x001cÙl½Î+{­#gð?] =W1¡ù.½ßcµ\x0007tey
úÅýniá\x0001ÍbÄ¥3ùWªó\x0005\x0019\x0016-qOB6©Ñ¢;\x0019Åê7¯yeÄtlk1@±Ð\x000e]åÜMÜÓ«.SsÈO6Ä\x0002'A5A \x000b¬õ
ÒIQ=fÂ®Ç\x0010÷3lÔ2\x0011ï\x001e\x0006FKH9Mï¬l ÏwØgÆ\x000flÈ[@2DJÌ¹Ó8ô\E´ål»\x000bNï\x000c-z-Ì$ööµ£°/?NÖ½Ö;ìîÔò	µ6kç\x0014ËÃ¯DØ
j_¥ûº!$\x001eesK
¹³ývXHå
/;\x0013tÈSÙ§è®¡Ä\x0001
¡ì\x000ffùH]©¾ð¤¾^<ÝÐK\x000eh h°K7kk'-Ë'¹4&ÏË³Ù¡õ\x000f\x001aÍHQÖ L\x0012\x0007íxS-¸`üþ\x0005\x0015nÇO²~ÈÉ\x0000¶üaX¹S\x001d;\x0000wJ\x0005ØP:Sª*\x001cÃºÓ©öbÁJ= AÉdÿR¾ôÈ¶bÁÉÑ\x000e\x0010kã"îv]4iXE·´\x0011kamî: A¹H¡q³5Ú\x000cÈõP¤9;Ù\x0001OvÅ	\x0005¾µ\x000cCÀ¶ùñÌD´"&aÈP»?áOõp\x001cW¶×\x0001íPý*¥Z%¤Û(Ë`ï>;[ÎÁÊ®½\x0010d×ª \x0005ÎÑ¥	q\x001aËÝ.M\x0017e·÷1e\x000foßÞlü¤\x001eCX|]wUuÓ&÷áÝú¤ööµE÷M×nÍiå\x0016\x001c:P\x0002\x000e8È\¼\x0013&©E æV·Ùdâ:2dâ$²L¼×y}ôziÖb¨\x001b·ißëÈ\x0019Öì±öëuÈ3Cç(ëÕû¼g\x001fä} \x0012.ÄX·Ã7\x0013É\x00117ù}'öKª_\x0004í\x0018ÅÑÖ\x0012û@ÇQñ:6ðbr T£
),Ãh"i:¨&}ãÙnêá\x001d\x001bF\x00073\x0002Ý}ÓÛAhî¨U«Üý·5ç~@W8#úbânã
c§ÐsgËÎ pOÊ"^õvhòFµ¼#É¸\x0013ÒDH\x0013}Î\x0017.´ëéºjB\x001f~z\x0006l\x00118µçáíü\x001b&¤PZÄ³\x001b«z Ãm´\x000eH\x0008,ª>$AÇVÕs«ð=ä\x0005Û½óa=÷U% L§¬Aà\x0001
A Äxð,û$ïP¡\x0003bé\x001d«;³\x001bJ}Ç\x0006J½Ê\x001e Çk\x0012Î\x0007ÅÄ\x0012$6àMv¹\x0003W\x0004¶ð\x001c\x0014ÙP3ßrñcG¸QÈÈ]¦\x0010äf\x0005BOÚ\x00064}Dn¢N~S¢êÈP¢\x0012ã\x00034Q\x001fg[-Äî\x000e¹+\x0014\x001c¼`P\x0012ÆcÃUÔ!
vü´¦jzÑZ~8°A¸]¢í\x0011Zj\x0006¹*\x000fÞEw'åì]\x000cð.ª¼ÌÈôú(!\x0004õ ±9M]¡`ãi\x001eÈàiêV\x0003°÷Y*$c£uÇ¶è
ÙýEË\x0006@å>ªCae\x0014h%²-{£ÙØ±A³Q\x0019V\x0005¾£1<@®\x0006ªj·Ñ\x0002Î\\x0008®B(\x000eo¹j\x001fQ\Y\x0003ßdz\x001b÷Ù3\x0010é\x0019(¸'\x0012ì±$©¼VtHäè·îó³=¸'ÁâÈ·e	Xyeé[j\x000bJ¾VþåýBI"U<\x0017,O£T*Giê0Ø\x000e¿21®ð0lS|=àä8¡TãôÚHðºqÂ\x000b¤e¿|{ÿmOÌþë?ýóo¿ûøþVªGfÖ\x00103#7ÛÎ9\x0010öRn&æ\x0013h·Þ¼ùe[%ÁM+l^{©ÙKp\x000b9¥©_¶CÊÜC\x0017ù\x000e\x0013ïy\x0007ò\x0016â)ðYNÐ?\x0012Äsô,×Iá2×¸\x000f\x001b:2
¥ÐÇÌ¸\x0001²\x001d\@\x001fÑ³5gÐð\hz\x0010$¾Ä\x0007¢F7S¸¤¤Ü-\x0016?±1xpÜBèÕ|p¿3\x001a\x001a¯xCÆ*s3~<ôk¯dÔÒäV\x0007rZÄÚ~Ù)Ì\x001dÈË&Ó\x0005\x001d¸Íkæ\x001b\x0017úÃ¼îÐ 1}r!_¼Ìû\x0000­Ìâuê\x0002tJ(ÓÔw3U2¢kb6\x001bc~ \x0007Bäøí%ThVuK³®> ã¯]ôÙN£à^¤.+ñ¦¨SF¥\x0017Y°Ï¾Ü\x0010Ë$Ò¤9.¨ì´ù#î![¥ZÒ>ûÝ1ûý1Û±/ÎSþ÷§÷7L©±y\x001e1×\x000ek%åÁ9×¬þkó/¼ø/aÓ\x001a¶\x00120úX²!å\x001a7
V
\x00158ÄW¦ëúfµÂ:Êû
ÞE*½8pA·jlÑ9Ö&·\x00156jWôû_¾¡´\x001d
Ñ¼\x001bcâü®$®IÖT«ªúË¯9ô¶þZ¢l[¢dKç4ª3ÅiX£Î\x0014Ü>Ô\x00074<Ô¶Òðz?õHÏ\x0015,1!-\x001cXY%Ç\x0010x\x0018~H\x0018YYèî,ìBk\x001bíÓ\x000e
¦ØB¥¨\x0019!2¯^E©[Úð\x0004×BæÆ\x0006Lí©°
×j¦N\x0017éÔ=CÎ´\x0019\x0006)6ÓÔÃÂDjd¦µÃøºÏ(Q\X\x0018¾F\x0016ÐÕ²\x0018r_ø\x0019¼ü\x0005áÅyCM{YF8y[òV\x0001ySAPõã\x001b¾ iJQ\x0019§ö+d\x0001Ì8\x0018½\x000eüº\x0016 »í²õ\x0000õ\x0018rä_$àõÐa#ÛÃ\x001aæªÉGY#SZÜn×1¢\x0007¶\x0003\x001d3\x001fGÒ\)%lâàT\x000e_Ü'´íÐö:¡tÔÍö	±ÊX& 8óM\x0000Ä®,ò\x0003; ,´Âº½Ådy\x0014\x0006\x001dÖÚéN \x0003è}iâ$\x0015ÊÀ$	\x0018»sßÝÚOr`{Ä¶@v¹°&´®\x001b·Û×Ü\x0004úÝÚcs`­à-Qzf¦íT[\x0015l(ôÙv;Úî\x0008Ôz§½SÖ#6\x0015\x000ewo\x0004ÄUîzºANEíaWª5oè\x000cúÀ\x001b^Ânh«ÙØ>}êýÝW\x000fÏßþpÃ9ê¹L~OK	\x001f¤g1Ðyc¬ýé­fgkVgÃtN/Là\x000f\x000b­ÌÆOeô9t\x0017²M\x001cÐ8\x0019:&v\x0015Øre\x0002¶µíx®Í\x0007t\x0000hï°¼UëÄË·aJ¿±ù¦× `hV­T©Ì¤a\x001a2§¾«´ºÆæh~®Ôû»/¿}¸a	Ýs×xDåò\x000c6Ù¤Áõk×sË¯Àóyã\x0008oÄÅm÷V±\x001cí°\x001c-Þè4\x0004À\x001azªbç\x0017Å5cÕ¡#f¬"¸«\x0002í'èè'è>e£±Ñè\x0010Þg:?vdèÌiñ^LÚH1ctéØtÌ\x0013½¦Å¦#F\x001a6ì÷nÁ
ÓÅUw\x0008V_\x0011ûeÙ®»\x0005gÐPI:"\x001e¾£&±hÙÉÌÙüxÒpÒ±¡$f\x0016¯Ó×)õèÌTèM½;Õ'Ûý\x0002èw \x001d¬¦[#¢c¢b±co:Ö;vfA³ÍÍ|ñVkw¶nëVn@UÎ§\x0006\x0010Ç¼\x000bòFã¥#C_	 f,«F
ÎWã%·ÚßÈ^t`P½Ô¶oø\x0012kqÊ$pê*¨RMy7\x0012/½¤cö5C1ÉÄ	ÛRÔ\x001baC»Â \x000bêãV\x0017GEiÍÞy^w/Â¦Í\x000e	:\x0007äÚ\x0004À>F\x0000ÎÀr±Ñõ\x0011´+½òÀÎØP ¿Q>d¡²´d\x0016§ÑnÛy×4Ï­7±ò´ÞúëÊ6ËFßü°×mÓ
ú\x0008-QÞ¦\x000f´ûGp.kH»\x00058T'P\x0016
}\x0003Û¿ï¦5±ûGÃâ6bÈ\x0005W@I\x0008Ïñ¹	½¿tmw0G\x000f4Ê	\x001c3\x0000½Ó<[¡E÷:\x0012ð\x000c\x0015g2Tu¤`ì´¤æ\x0008:n¯=Ù¼½OÆà-Å¶X1òZ!C®,ÆÜÞôÅö\x001eô¿p\x0006_<¿ïr
¯êH\x000bØNí\x0014:_,ËÆíÊ\x001d\x001bÊUüÚQbw*¢@\¿ùÁ·±K¥odM\x001av\x001c²&\x0002r,®P ö8Pp[çJZE;p
0`¥ëZ_pÅøâØ8\x001dÎÅù>È&oè4
:\x001båkå´Q_b)jÓ[Î.o8\x001d\x001a\x0004ïµq B,m-ÆT«}ÜÈÍp¹±«6Ák¯ó[=\x0012&\x0004/\x001b¾vù]ÙçÃÝ\x001f\x001fþü§\x0007	^¾{þó­*?\x0013Ô«8COÈÚë\x0002ã`å\x001fÒºPøÑVaÃ´\x001bH®6R¥S©¹Í­­\x0016\x001d\x001a|:¥»e°tSuD7Aw+³²è\x000fäa\x0008´Û\x001eØ³r\x001cùRÙIî¹5ãlèù\x001d\x0018èù©âTw\x0001.\Ô9BÜ\x001bEð\x0003ºÀ+ïÆ\x0014\x0008©²\x0017A÷á¨\x00166?·°éªA¾\x001c£RaÕLo­¦ÕHÖQô\x0017hT^® \x0008Þpi?\x0012ó[khÙ\x001br&\x0019ÃHTbí
¡7ßÈ«îtvÓØ±QÕ9~±ùæÞx>!]mÌ®e£\x0003\x001bÊF*·c*UY1Úñ{ñxmWw;9$¨ü |\x0010-k\x000f\x001b\x0015r[RkWßd£\x000flÐ4Q}Z\x0008òsõiÝÄðêS(WNÃ\x0001
\,\x00149:\x001a1ªÒQ\x0013¡8µÔëêP\°a»ÅlÀTu¤h¹DÆö}@ÔfND×\x001a\x0006'+kç\x0013\x000f. íörr}PÄÔ]?Üý·§??<ßJö!ø©½°4²Vû
¶Êw\x0004"SîsRÿó\x0013¹k{í\x001d²Ø\x001ef=\x000cw\x0008¹\x0004\x0016Ãñi1]Gú\x000c\x001aÂöÛòâî\x000bÒab	2Igñ]h\x0010°V
xÑM³êlÍ\x0011Ö
N/_;mãònÑèjõPÙ\x0015É0Ô.¨\x000fooW^`éÐ2/ÉîÄã£{Ûï'ÀfX-NW\x001d\x0005ºJWLÓI¿.§iq\x0017ÄÞ¸D\x001d\x001a\¢¦ä\x0001¬C[Ú\x0013\x0008¥\x000bÞÒÔ\x001a\x00007]ýt, {Òl\x0008Zk¤\x001a@æÑË¿jK;< #B#¼\x0011<iàH^¨¥¾Jë_ =ì\x0007:E;\x001ai?¸8Ö²\x0019\x001c3«Ò:¹XáÒA·Äõ{Ë«®-\x0013¿iÆíÐ\x0008ÕâY\x0002èÄY.æUKÌ[·ÄÃ\x0003\x001a^\x001c
ÐÙÑH÷I\x001c,ê\x0008³ÍÈ«5ÅõÞýw\x000frn\x0014\x0010UVmK*äu	\x001e²\x0003\x0013V£N\x0002|í\x0012N\x001f\x001f5ßþu\x001eë(Çfm\x0012NTÒ-ù¥eþåÙ6oz3\x0003§]È\x0005Hl8È\x0006ªæÄ.XáQRýÅ_¶\x0012mîÐÈa:\x0012`ÉÂ©Ø(bÊ²{Åbc¶:¶q«	$Cbk\x0013%èÊ\x0013sUÙb_h9 \x0013\x0016ÅKv»¶pt`'l Ëî¢
g;RÆ¨ÐÉÛ\x0011iJ	ã\x001axfO m:æ\x000fñ\x001d\x0018\x0011»?à/^_öÚ\x0007\x001d;\x0003v\x0006BlÔ\x0013\x000f_5T?è½%XÝÊÄ>\x0007\x0013[N\x0008¦\x0014u\x000bGÍ:Í°ûðOùZ)IÇw\x00048F`påKZÎ$TOü\x000b9%ic¼LY×ïî¾Q\x001eGöÄ\x0004×ÙQÞ¹á~õ±\x0006\x0001kÓ\x001b0	y\x001dæ\x0000c5]b>K\x0002H&7¥l¸ð
¹©)\x0012aá±QIÔÞcB6ËäÞuA©\x000bÚGñpa©Ú`Ý9'6Ï\x0015®'\x0015Ü2\x001b\x0016Y($ç£æý1<Ë
Èº°ÝÌÕìØ0W³µKàhn\x000f\x0010óÇÓåú7®Ûq9°GÆE,\x0007\x0015£!»%ùJ\x001cô¤Ùè\x0016ïn:\x0004zQaX-ä¶,Ç¡ï
¯;4"ÛÿíØ0þWì+~KoyÑDuKÚÎÖ×tñ\x0005\x0019LKô\x0005$r¢Gyãä3C¯\x000b`V¾øááÇÇw\x0017Í°?¿½S4áÂ&îj\d+[Þâj\x001dû¬ÔWm\x000fÈ­>2\x001büQ7.ãL:UN\x0006Ó\x000c\x000fNªer\x0000rs\x0000V=¸\x0003\x001a&;«´1|Ú¹·6É½^`wU]³ù¼ïï¾x{ÿ§[6\x0003Î		ç._X^ZÝYE¹ÙF&fSnì\x0018PT
{\x0010a±\x0013oI§êpêÁïcÞ\x0003\x0006m÷åÅ=Õ wS´ë©\x0018 `$ñ2M=ðÚjHÐ]\x0016n¼@\x0017Z5"E\x000e§eÑ<yDÕ6Çr/SøÅ\x000f÷?)ßà6RK	\x00162É_\x000e¥Øs|4ÕõvØ\x0013ºÁú^\x001dùÁ1Y!gÕ:õ$Â[Tñ½}3la­a\x000e_gZ \x0007FÙLÆ4'=aêI´)%\x0012ã×A\x0008\x0001
\x001f\x001cñýOb%s(Ü\x0001¶!Aªu{\x001c" 7±íÂ.«\x00018°ÃoþÂAyñôøÍ
w\x0012w Äª×Q0Ø\x001däóÔ\x001ddrOónd0:öÁ°-\x0018uçÈ\x0003!ôî\x0012vé2tgûí`¿Õ\x0004\x0005ê\x0003\x0000ÅWgËeBê\x0012wgØ\x0019°-ÊNúZ¸ô ã°':pO2ÖÕ\x0015;4îF:(í
Î`ñÔÓ 1#ì÷Æ]\x001c\x000f\x0017'\x0000'E'(ÑSdÍsÓ\x0005XüÆÞvàaomÃ\Î£|b\x0006 D8GUmu /fd8Vû\x000cOWÕ`I"\x00036¯æ<­æü§ç\x001fÅÖýp«.AÇJµÉ&\x001cqühq\x001av)æSp0$n[>BjÒ\x000f#*±^J0Ñ\x0004I\,%wrOÓ|O³Ë¨g¤ô÷@6wÉ^«´\x001eË\x000e]aÞL
TH\x0008oAS7ü±ú¦cÔ°ój5 íµ£\x0004¯¼\g\x0010Wx§¹·½ÏÍÏèòw\x000fÏ?ßêl²\£õéª|\x0017t¾Ü¨?\x0018ñ'Ã«OÆ´¨]»×O»\x0018¤\:\x001c2)\x001a(Ê$§k]\x0017¼Þ¨uï\x0017Ú>*äe\x0004M± s\x0015Â6þÄf4T\x0007\x000e¸äeHåQ?II<
Ü6å±µ\x0017ül\x0012fÍ\x001aqÂH¥©LZ£ò5u3èha7(Ìh©¶cvvSáìÔ\x001d~úðs;ð¸|÷óÝïï?<?¼»Qá]µ¯øÄÛ®/Åd~o¡zí\x001açÖ\x001co\x001aëÔ l¸6ÐLR\x0003Ç}¬ììÅ¦ñµú\x001e\x0017`ð=\x001cNA\x0016ÓëØÿuéÅ\x001fëó	O°\x001d\x000cqÓYs0VÑ¤@¹\x0002\x0015æâá_)vÝºµÅ´c\x000fÆm\x001d\x001exèYZÖÍ÷4û°+½ÍÁüã\x000fOboEEÌ\\Ð-¾I¯*°£0áT%ª¼r
ûDÂMÉÆ\x0019íf7\x000eìC#*XÌ,\x001f(\x001efKÚúÕøtp\x001fÓª|aè=\x000b\x0014ÙÐ
¹\x0014¥zX³ä\x001d<\x0014àkû\x0008N'$z¥8ÃxîÅH»î\x0004¿MS~ñÃ½<ìò)ntÄãbRÑ_ïÉ½#!W²yu³vrVOÐ÷D%T\x0013µ~$ÏåAáÁôb|¨ü£][Îé\x0001í .gpÊc\x0014×;Â
K\x0002I\x0015O\x001eÜ\x000e\x001dà`V\x0003ê¤QuwIE´PX%È»ÂÝ\x001d\x000fw+\x001fåî«§·7+¡É\x001bÈwPöpàh×\x0002\x0008^Ê^;ÝäÒÆ	\u»lÿ\x000c¨Û%w\x0016Ä(Ï\x000be¹
s/SW«v\x0000\x0017Ð8*\x00152 ²+qÒ(.uÚÑV\x001dÙý;6Nf;Ùñ\x0017¿VKÜ®o¢ïÍ8Ô=#7\Y×tTÔ°;ÕmS.:°\x0003S¸
Ð:'?!ÚJ\71Å¡ñÎ7­Ö\x000760]¡u«\x0014(­ç'\\x001bÍbWº.\x001cõ|hÓï.K·\²P\x0019©ÎìØFÞ:îëgoß>\¢¶¿½þéFCl$B#RoLq\x000cµ4Èáñ$?Ô¦Sß;Îà­þÅ_¾íD; ¡\x0013í£ ×ï[òê\x000b¾¿û¿?ÜË^Ü}¦R\x000f·ë7¤(%kËÍè$­dHrßÿ)\x0014\x0000Öô®ìYc\x0008@Ó§÷ÀáI\x001a0"ù &Cã¢Ä&÷1\x001b{ß±ÁÞ·ñ\e`K¨B\x001c@§Ú{lÝÚUÓ¡\x001döI*a*]7ÍÑ1Õ¦fßÉGkèv`Ã0´\x0014ß$;°m µ#Á¦\x0008+Õ>çÓ­ý\x0007\x00076ô\x001f\x0017OZ«Õ­²\x001d
Û\x0003Ù^BéQÌIvvC¡>Ì¬\x0019í^\x001f\x000e
:j%Àvç8â£wJÞ¦ëWA\x0003\x001a\x0004\x001dJpø]Ø,\x0004\x001d.?;\x001eÎ_ÑòÂ\x0016'ÁsÉøÕÙ¶Üô¦\x001fÐØ\x0012a§6:S\x001d\x0015F³F-SvF<\x0011ÑàÚ8\x00172}È\x0010'ì6\x001f*¬Ã`;va°:#\x000bÎ¶\x001cáG\x001dýØÇ\x0008î°É\x001eØ &«M*#\x0001­õ\x0004î	Ò\x0001>íÃÚìñ¹Åtë\x001f\x001fÅÿáç»Ï~|úp«AÐÙ±ÒZ²cÈ§\x0013W\x0006T\x0002céSí_õÍÖ¾ÒM
`\x0019ZøÍ½X\x0007£çöËñ§o>\x0001VÕÿp÷åó¿ü»÷\x001foÌæñ¾ÒxUqªKºÈFlÔ*UÏík;Oû\x000f1¿Nß\x001c}&P=Yü?¼cEo¾½ûØ"J^óE¯Øõ_¿þÜ äÕoßÝ}®Ì5?\x001bw(¿ôÄä{o©õÀ¸6[eÉ:\x0001à-WP\x0002Dûwßý__<µlñ¯øL\x001f»-Öñ¶\x0001ynd¥Ûl+ÞSms
­qÔ×­IÑ4Ëø©l
Þï/~>8Àkþâ£6F§¹cÏÉ#q\ë¢ÉUÈÊ\x001b\x0012[ ù©lLk'¾ÈëËËó_äýQzÛvÆ9,nëµ§£\x0014ùPß³Y^ýð\x001f³1ã\x0017\x000f\x0013øãwß>þtÙ©c\x000bèß[ð?=ø¸	WÌ~\x0007\x001aÁë\x000f2I*lÈ\x001d0­>ýÓÓO\x001fäzÔÈæë\x0006Ì+ùwØøé£\x001bl¥Møúþá\x001fù°©+|ñø¿oôå½wÔV ÿ7Õ]íh\x0005ÖD*&M½|·ùôé¹;îÃJnäþ²_\x001aë]cúÓ\x001fñâ\x0006LGþ:ýð¿~ü	¾Äý·º\x001bÝ>åÓàí+mäF¿}^b¾r
m³kí§ó
&åÏËNµxû²9ý\x0011/nÀò
îúæùGð(~ßä	ÞäR>î&dbãÕ¡¨69\x0017F\x0013åÓù\x0004y¾\x0005mZÒlØ¼í/xé§/Û?éguSô¯ÿôÏ}/ÿInÃó­<;p|§U^ÍÕ")A!Ë\x001c´Êù\x001fðJÿE\x0007<\x0019Mµ/å÷8}ØÕU0¡äÖèê¯¿@\x000eúÈÚë¯·\x0016õ)ä×÷J¤9î²²\x0007´Î)\x0003Ú×ön\x000fh·L \x000fUÄÃ5°¯\x001c.Áv##Ðrð\x0002{SQ\x0003W c\x001bjÃÙ²\x0003,ÛT\x0017lm©#ìxGBo3
óÁ¿bgÂ6°ncÆøí{kd<ÃJFr\x0016«\x001bEå\x0016ÅîC"Óül]õÅ<`Ñx-Ø%½I3c»ÞÂ4i\x0001vúÍ_¸C/Þ¿}¶'	÷Ä\x000fj®\x001bJûº\x0013/Ûu
ôü\¡+@\x0003P¡íh\x0018ïÐíl\x001fu¶%\x0019·D	lF\x001fÁ\x0010\x000bL·¤\x001fïrvs
Ü\x001cSiÝ¹vX· Ûr\x0006]®Ða\x0006»­
5¼lLª\x0008¶q&¶ìËÎxsZ§{¦SÙôNw[ÏNISbâu¥ëN#ÿÙ±\x0003mw©tgÜ\x001eÛ]»!uOÜã\x0004;\x00146&°\x0011,µí·¸\x0003ûÊ\x0015TlC2Øv\x0000;Ò~>\x000cÇl÷(\x001b(4¤ß\x0005ÚÏz\x0016\x0015ÚïÆ\x0002ö0&bÓFÒG\x0019©ýí\x000bcg6ýÐ\x0001Û
6bÏ\x000fç¡d\x001b6Eèí`Ýeºbû7\x0004í*]øC\x0011É½9\x000eÞ\x001cÒ\x001bØ\x0011;)ëø$»sZbmÍZhp»ðÌ\x0012KÔx\x001fÓHsÙ!æä]LÓÈé×r¦U\x0016ÞÅzYý\x001aõE¶¡3¤åzO\x001eKö\x001cFúÊgÐ\x0019¡Óh\x0010Ó°\x000f¨¬\x001d\x0017Ó\x0007`[\x000bØµ?Ç\x0017ìèNDÃæF]í¶Ùè-\x000chÐ¢Õä'\x001f®\x00123\g9vìõÐ\x001fØàhÏENuT·\x001bvÁ§H±»ïéÖ§èÀ.°îfW\x0015Ç2aW"\x000bvWsð«ÙíØÞ\x0000vÅçB;:\x0012c×iÝFìjc\x000elp´tÀ+|Ê,§¦Ò\x0010ÿ[ßF¦VÊÕ	v$ìën£L\x0010O`\x001f}eC8\x000eá
­íó\x0019-~V
Í\x0005-Õ o{Ö/Ð±Òá?Ë¥ÇÙV*NªªÛ´
ìËNoÆ¨Ês´jªMj\x0003{\x001f]r\x0002í<@Û:ºØ4ç\x000fù
^\x000b­\x0017´º»\x000f'\x0007Ðq\x0000O\x000cíFº×\x0007´cC\x0014¡.ÁÔ\x0014äTOOMØ±·¤\x0013câÓ0&Qu\x000f\x0017iÝ´Vå7>ë\x000c\x001bìk2cô§@çÀ>Å¤²&Ëns°«7Þ \x001dÞx m5Æ\x001dóJ\x001bv"yH£\x0012\x0003
ûÄN\x0005[\x0008{\x0008	«
\x001bL¿&ì¦\x0012Î`#\\x0002\x0001d¥)4
;óv~¼C<±S!zÀÆòü
äÃ:6Mæ1:Ù¡aÜø\x00007>Óv=Jìðúq¬\x000cz£¿¬c®\x0007vò´'c¼¨Nµà ÙÌÑ£
%æäVF3neÒ¾A; K\x001e³ì\x0015Z\x0002Fºñ:/®éa;ÀN¨«j\x001a\x0003\x0018¡\x001dMçV±ú6ÉõÌ\x0006F°I^QN\x0007#\x000f\x0012EÃN$Á-?9Ì\x001c³NgúÍVêO;ÌßÞ¿{w³´h
¤ð`Jº\x0008\x001f\x0014ñ\x000fj;âÇo>Ü«{ qKü]¾E~\x0002\x00193}9Ú\x0007U£¶u¢Âw¦Ié&ôwtc×§-
]ÇÜT£ÒN¾²'J±Ü¹¦TlÝj\x001fá'`\x001f+²%®q\x0013v&ue\x0013k× ÉëéìØyÎ¬cé
SÚ\x00069\x0016:\x000e\x001c±ï\x0004Ú´^ª>E$K¥­÷C]Q^ª0\x0018}\x001d=?uÙô¦êz]\x0001;dhb7\x001a©S'ÈØ¾õõûo{Ì\x0011\x0019o¼uoÆTG£êYyíºüó®ÌN¾¥÷	°=h\x0015\x0019\x0015oô°\x000bC§.Vzò)=~Ê<kíPC»]HqÒ£×}lÌc\x001fÈ\x0001æ1\x0008»\x001dMnÅ°\x0019w¤ø¦\x000b\x0019ÂêXtì0\x001c\x000bÕ°Î`Sd·+îvòÔz¯Óºûkt¶n8'öêE[§ØgÛ\x001d`»Ó7\x0002M\x0013EBè8Aw¡¸Éi5è\x00089­â\x000b(\x001dÉCG¥agâÆR[68Æ-\x0011¶äß_\x000c?yé:4¼t\x0006­©°cÊjfw¿\x0016IÄûÙ±Áý,ª©Øeè)6l\x001bxÙ±ÝÉtvº\x0013î#¯M\x0013ÍyB.M/Y\x0004DÕF\\x0000h`Âvhºí\x0012i´Eç³Eç±èªZµã)ËêÓ\x0011t&*«\x0014\x001b·b\x0019¬}D\x001fÞ>¾»\x00157©ð7\x0017C<¸IÇpÉ\x0006Ø\õW÷&Zøer]ßª¯\§ë/\x0010Ýª¤¸óøÓká¬Plu,¿:\x0013Ó$demùÑÖ";S9s#\x000f¡ç,E¯}õHvèP`Ñ0¼\Sp\x00127²jÎ­X»\x0019{\x0008È\x0015\x0016í0Ý¤\x001d³d²h&èÖL~¶èÈÆýÈ\x00056=dôØÛ>\x0002uS\x001cëÈP\x001csÉaÎYn\x0018C¦qDZÚÕWsSÀ: a?4%1êÚKdù|\x0010pj¥±²^ý\x000e\\x000c\x0000[¤;Êÿ{C_°p°"¯±Zr¶\x001b\x0005w\x0003ücE¶Í\x0003èø67\x001f¢®á1'Û\x0003´¼; M¢Ý`ÏÇäffëÙª+¬ZÕN\x0003Ø\x0011\x0018sÖWMF*VÐ
³öä#Z[éäAS>Òhè;Î\x0007ùÇrj»_¿¾\x001dÛ\x0005X7\x0015}McBÃÎ?¤8ú-\x0017y²'Ö'Â\x000e-\x0001­KM¯Î¤kÉÈ³=Á"¦°bµTÀ×ëÈØ.ôi'7}ÅPì<b\x0006ÁÖî\x001a¾4ËµÍ°\x001b\x001f¢c\x000fÑì5ð%!/VM\x001f\x001aêÒ¸­¸[\x0015\x000fw_><?}¸\x0015%&L\x0005Ñx\x0002¡CÛ\x0012´ZöhÄÿWÓú¼{6×w3ó ¢£úu¾ÈéUq*\x0000RºHØ&ÝyÌúØeÈµöB_ \x001ab°ÄÿPVC<Ûêå¥L\x0000mêTC\x000cÁò\x000fµó	´GèØá\x0001­Ò)\x0014Ì\x001a,}\x000emXÀÆÝ?dX ]\x0002ðxüQ¡\x0000äÈ¥àÐsfg¸h`ÝX	:ð¢}³^@¢C'v­é
m¸n S?\x0019Z·#­	 \x0003\x0019êÀzy9×3mtð|<\Ý9Í~k:L\x001fnEÑV%VöñB½×s~2õ<åÐÿ'\x0013â¦TÖûä¡T¶ÿ\x0001/þö]NtÆcÓÝgz~|{gk+Ý®ï°\x0004ý`º&hÿ´)tjË«[cçó¦&¿a]Øn×®YÑÁ\x001cCjÇê8$(ªt·§_ß]b@N\x0000-ßuÈ¬[e¡¢£ ¹BÐ©{ª«\x000fÒ¡\x000b2Ã(u	´¹äèeþf¹ûÍÉ²­e«ª\x001cb»¡ä¥ØÁ	»\x000fÉvëÛgy\x0014`+³\x000fv[!ãn\x0007GÕVÁî9²'ú\x000bv0þJré¤ëÈ\¡SÎuóT7Õ¨\x001caGj*mÎ»#lÒ-\x001bÒ\x001aAí&0èØ\x0015w;Cé¥©2¶µ¼#çÎvÛán\x001f3&.ØhÐbìùøcºÏ¦Ð# §AªTäBt\x0013\x000e|kTysC±>UôûûÇ\x000eÐG6üÈ_?¥«
s6Ó\x001du\x0010Ù}S®o\x0002Îvë·ëñïò`\x001bUñ\x000fw¿¿ÿÓÓãíÚô8ÿ!¾hÀ°\x0007R\x0005ª\x000fù\x001fÐsõ±\x000fú&&ì.,Æ»\x001fðâoß|°N\x0004yû¯ÿôÏ¿ýþíã­o¼uÌ9¹´\wª~\x001c^I±ñê_!{»\x0019g¶±J]bßq³A¤\x001f@u\x0003ë¦\x001eÚ6tkF2°&ÖéÞ¼°««j&\x0000W\x0002ä\x00023!Ë1·Î9³\x000bÊÝ^MíéùO\x000fïß?Þß¨Y%DÇ¯Q\x001dçG¢²\x0002ÕeÅÊÿ	·XNÙÇ7í\x0013}&ÙhPE7\x0005Z?õ-Fc\x001aráW­g_òz4IjãÁ'\x0011]ì\x0013¢¡\x0013d«í©Å5\&©îûß¬å\x0013Öãé:å~øTÚ2 sDE3©»hûNsN6|\x0016×ëãÙ¶Õ1Áôr%C£TÝ¡À2ë°\x0003¶\x0005l;JZJ4dÇ;RûÓy^ýµ\x0003Ú\x0003´\x0007q
Á®TÕ\x0017lbjq¢WõO\x000e\x001bÍR\x001fíóÉè\x001f~\x0015öjhÊN÷³ÍÜ{~Ûúþf	\x0000'*b¿RÁ]ÈÄH\x000eñÍ'Ô¨»¹´¥»ýüÞþ\x0017üÎa8õÿËýóýÍ\x0010áPÁÖaö=<â:Û\x0014\x0017>\x0011·aã@\x0007\x0016V³o)0	Éb&³ß:ÖcH\x0006¼(\x0011¹46\x0005ÍÕÍ~æ
Ç´e;\x0007Ë¶ÀoïË\x000e\x0014K§\x0014¦eï\\x0007¿?C_<½¿Qù¸ËÜý\x0004pcl\x001cÎ¿æhGR²è0ÃO'\x0004ÛTmúìx¬ÚìÁ¿þß&3ãµ)\x0001´1¢ÊÌÜÞoßuÉÜ»ÏïÅ\x0006?}øÇù{Ù­"P|Y\x0011¨\x0006P;V\x001cl,W9ðz\x000bm¿¶ê0\x0010þ^OÏò\x0014<}÷\x001f-\x001b²ÛÖ\x0005vÕSyþV\x0015xîþZþûýRú¸Ñbaw4\x001cÝÚQeÇä³Ú$¾È\x0012þgn\x000cÏ>üã10¡\x0008ßî&4}ä¹%Ò¹tÐT\x001f3ªÄµ\x0015}>Ý\x0001µ/><ÿüx÷7Oo\x001fotb2\x0015ÆäÄ4µ»~b¼9è²'¡>=©Ó¼½ûÃÓFÏê#\x000f
(Ú¤ªôî"9V­5\x0012Y??]q``~'ÿìÝ\x001fïõ'ÝdO|0¨\x0004¬dl{¹<â¾ç\x0011?VoÕ}\x000cÈÀí¹¬£\x0004÷ßßÊ¬Ø\x0018é\x000e59ã°44lÅèªÔiý46\x0006=«ß?Ü5GæîË5@úHÃRO*\x0017(]ryiy¤ã¸¸bÞ|"O4AËKÔvåáýÝWhiâøÈ­¡b:í¢m\x0013j± Y]¨÷\x0012\x000boÍ¡ ü8¾7Ú\x0018¥N£Ùu)]$áBÑt×v­ÿhzóx/	Þ¢¦Dú^«\x0013ÿíéÏ«àÇ\x001a\x0018D`j*WW\x0016¸«±ª
?i\x001eÇÆ|õðüîþÏw¿ûðã­\x001ei'áª§])\x0017i"y½3´äV«}³î?àA\x001a?÷7I#ïòoõñôÇ¯úxWåmgìPÞ\x001f]2\x000emÔX\x0008	¥:.²>^IWï\x0004WññÚxÅÛÈ?þë§zÿüðÍoX
ìûç\x001foe3}¢Î[ùÕ\®JMr¯>²©õ\x0008ÜòcÿEmõ^d_s(¹lÔ×4>÷ÿgîívõ:®kÁW!ü\x0000Dýÿ\Æîcw\x001fX§ÝIà\x0006\x001aÄDÛ;¡H\x0014È¼FnûªÓ×ý\x0006~<IÏYµ¾UcÔªÚÒáÞÚâ9\x0002Ö`}µªfÍ1Ç,ò\x0002\x000eFf4\x000e¼zq¨è\x0013Ô:J¦&\x0008>\x0008¸\x001d\x0005¼$Vð)\x0000Ú;õ½\x0013x\x0018à¶@Ð¤!e¡[þhr\x0014\x001b\x001f4l·eTCQ5ñ\x0008+ Â¢è¹Ú)Øv!sEè\x0011Ðý #
z Eû:
C\x0015t×y$ÕmÑë©°¬]B/\x0001Üg\x0014Y\x0017pO\x001e@±½·Îl¿(qÕ^²Á\x0015pgp\x001c;Ì\x000bº±«Éô\x0006zJt\x0018=M\x0013t\x001ad¢k?äø·ßtö\x0004í@AÖ^\x0010Ú ±6
NÐu@:ò¤j\x0005
\x000e¶\x0014\x000bBädµ ]ü&l?¨\x000bðAå\x001a²=nÓ \x00065tR`Rôê\x0017ú7\x001e\x0001Ý½t°ôºù
_ß¸ßò\x0008[ny_¬\x001f0
<²uÉµ	¤¸²?.e\x001cí}Ðn·ÓþÖñMÅÏ\x0019d/yü*Ô\x001bº)7¦µ\x0004{»]»·°öä´®Ý5Ý±\x0013=bö[Á\x001bGv@àyl{Í#·^]~²/1Óa¯®÷Àî?*Ì,ÐVÈ1ÞºoLÁ\x0013\x0013='\x0002s\x001f·ìë~cÆTB\x001dL6\x0014ØÔç­Át¤\x00022[CëVMÛ\x001aÒø¨Zë´Ry°\x0015\x0014Ý\x0017
P¦íÌ,\x0015\x0000èC, ïg_\x0006\x0000£Í±»T'ðÖB¹©#¼ÔA{n\x0000=tk6Ð!ÃCìè[\x001b\x0013ý°1!¹Ñ\x0010[uÀØK|4Ä\x000bàÚ'_E¿}ªã\x0018 QTF/\x0004²11ÒÆÄé¢\x0013\x0017_½®¯_ûïØÏëé_ýéÝÛ§mà§7¥x¦i¢\x001f\x0007?ÖÄÍÃ×sö\x0005ÿo{õ$ÿU»î­ñ£öß~º\x000fdsRW\x000f`»Çbû=¶,ö|2\x0001;\x000cìØC\x001b¶¥±{Í\x001eª<­Y{\x001d\x001f=[IÀN°'\x0005ýSmÖNq ;¦ÊlÊÇÙcç_Ð1\x0007S >^¢uÊë.MÁ«ì±ËÀ. ÿÜ×iÝ)iÝì³Ç®ÈÉZ
c'Þï®Ý9[ß\x0001>Ç¶pgáî\x001bòðtÎ,ÖG¸Gk©#IÁªh\x000bk$dKµ\x0018~{íEð\x0008ûÓ¨¿ê²ÝÐ3mà£ú÷Ûâ|~4zÞÞMÃcÑÃÅe?ÑÅÓâ!w%ÛîFå±í·ý¢¾\x0013_?¿{û×Þ¤÷\x001f¿ûÛÿóþÉ2¶r\x0007èh©Ëqû\x0011ÕàuÒ6æ,}\x0006/RM{ßªW4f¯Öè\x0006×G\x0013itBëow\x000e5ÿ&^[Å\x0010<ó£-\x0014ð\Ò)ÿgöª°ÿîì¡º7Û\x0013\x001c\x0012\x0004ºòy(\x001d¢\x000f\x0017»æbXVÕ\x0010/1Zò¯y·}ÐìÜ²Aèc×Å½jÚ¬7ôàøICw¥0ú¡=_,@¯Þ:?ª\x0003½ÆÇ¢»8Ûâ\x0013ÝñÐ^·\x0007ÒÕðXtog\x0017ìD÷\x0016\0\x0015l8»Õ¹Ù\x0019Ñ-µùh^¿\x0005N³8\x0011¢Éi¼ö:?$\x0003}L¯r\x0019!Ñ¬\x001dH/+SÞÇ¨8bÓ´ÛnLî±K\x000fqûQC|ôG
q»íúG'º\x0003%ª	öÉÏ+(\x0016!è&ÏÜÔøêß¾úÆ¼
Ú\x0017wïïÿøöÊ|ÿ´\x0007*BÆ¨&[nÕÖZí\x0010\x0015©®j&âk!?<IÜ¯Xï³²ÿm^¡¶¿þ\x0000ßt?n? \x001a\x001cþ(?Þ±\x0013/ç¡YâË¹\x001fè\x0015ÑÝ\x0000\x0014t·ÑcW÷¯³ó\x0007è\x0005Ð
¦ßuòGat¦²U×äá\¯Õ®4ÐA»]zñ[}&ô8eTÃJg\x0015ÐÒê'£ÏÒ>Ä?£øP\x0014*ÜEÃWå\x00170çÖF>¿!'v:ßh-Êc\x0019,\x0015§$r®#&i.)Ï\x0001~¦<\x0005Ü%Ì_ESøÀÈ>³\x0018cÙÑñÕöÞÕ¯=ø?ß½ÕiÄßÞ¸{» ¶~j4Ò\x001eª)¸M$Îâà\x000cqk5¦ýÇg5\x000b½h|1\x000b.Í~Hß®W¦ýÑ\x000fü\x0007ýåCüáã_?þñ\x001b`ýéoÿ÷·¯ï>\x001eLõÿþîíW÷\x001aJ<Y\x001d\x0013\x001b¶Åqw\x001eÝû¡#4Z¢þsø y¶F}×^¡Ëö\x0007<ôÛ/ã«ïþí_Ò¿0Óä÷òR>U(\x0017\x0002Ín\x0010ëk¸½ô^§\lzsö¯DÐYÍ?\ìÛ4%\x00177Ëð§/í\x001e=ÇBí\x001f=»\x001d\x001e=Û\x001fÀÅ\x001f\x0019ÀNÅ=\x001eÀÎÅ_uÀ.Å£ZÀ®Å¾$\x0017\x00078$\x0017?	|¶^Õ~÷ý\x0000Ö«ÍB¾{óõ»olÊÒùÁº\ËÉ6Í\x0019]*\x001bÍË'æ°â\x0003âýl\x0008úNµ\x0000w\x0018õú\x001füéO`lZ	\x0000}Tj«N(üöªù©¬<(00i|	£s\x001b\x001c$\x0002b\x0013N{ÖO¼®ï\x001asM_B7¬ÝaØ¬-cü»¬ÞDª\x0010\x0004\x001b¢ç_Þº.QÅ
\x001arvê[Ü44¯\x001a´ç=Í]ã{~£nÈb0\x0019ÔÅ:rÄEê\x000bC[\x0015¦\x001aÐÃÑ\x0014h?TÝt\x0002[àý0³:ÊÏ¸KjNEøc\\x0002\x0007!å^_\x001b±*@\x0000ã^~\x001eùùõ::S©0¦:céòK¨\x0004dZqÿÂ\x0006¹áZ(æi4
\x0015 gÇh\x0006\x001c+ßsáÐ¸dâkEðÃ±fÇÐ¡^\x001f\x0006´cè\x0002\x001518¤ÐL5/­(vÉªÝ !§¦Êße\x001c\x0012ðG<\x001c½±\x0015	/U¥\x001b2Ö<z$\x001b¡
¹\x0016\x0006n%Âr1.\x0007r\x0002a\x0000i:]³#òG\x0014C5¯¹A_LÀ
\x001a
É!`\x0001\§7%ª\x0010\x001a>\x001eÙÌs\x0015¶^¶¾~ñÅÝWOÖ¤\x0013\x0013¥Â\lL\x001bg¨ÀäoEÎgn~\x0010Zß¨W(Ö	è\x000bjtª©u@\x000eÙ#{\x0006¬Ç\x001a^/!aE©E<Sw°5ënÕ\x0015Vís\x0013¼A+;(¬øB.ç.º0+µß\x0002ÁL¹&,'Øk©\x0012]Èå\x0014Pç¥*xÃ\x000e°në!¡îuÈW-\x001a§ìÙF1½:\x0017\x001dÛ
ç¢$uòìÀ6\x0013}59N%5µ9ìÐÃ\x001c
4\\x000bX#º sô%S>fZÌáÇ
\x001b©!\x0001EÀë81­°màwÛÃáN¾Â\x000bá	ÄR«JVLó·ü¥ÔxÃ½¾õ\x000fZï¯³Nì1«Hy\x0005{rÔ\x0013OP^M:J\x0018Wì¼¹![À\x000e¸î`thã ÖJû\x001drËá¯¶Æ®Ã(AüÛQÑÑ²C\x0010K±]6´nkîAuã]]\x0004l\x000bn¨×Â®Ã3(\x0007®¼Î\x0015hR:ý®aì·j\x0008FX·8)DBVW°Kªe·'eìËâ\x0007+Hþ¼\x0014¯®\x001d*5
·àµ¦\x0019;\x0002;íÎAïÊ;gécê²\x0006n×'Ü\x001aë\x0001Ü Ç@¶%ú¶x\x0006ï³ÍÆZY\x0008ÚÊ¡\x0006RÅ\x0012\x001aÚ\x00167moÅh{
+\x001a¶³¿\x000eñå²Jé=J#}m©jyóë£ÒþàÄ¶ è^µ{¡¹·'xH¶bþ¯E£êKfHxÒ#x­\x0019Ùïª¹§p`ïôA9û4T~v\x0001qxís³kÖ)ÙËG°ýù\x001f	+\x001dOöQõ\x0003®?ô»ûDÕë¡? áÐ+ujÄp^\x0007-\x0013\x0013¹Ðv\x000eé*ú6 \x001d¬ZÎ¸ÅU6E|@§\x0018º¿t»U{Xu
Àð:gÞ~y­è6vS/Uâ\x001br\x001c\x0016¦ùçÃ4êÀì\x0016FüÁ	¹Uü.\x000fÑÆCÔæý\x00148fú\§t¡ëö]J&7h(\x0014\x001fgïÛ,+Z´óü~ú6Ö;ïv:ÃN»
µ1YuláË¶ÏK\x001aÏæÝVgØjç\x0007Ã¾ÝÈD6ÓÃìêÚ¥\~C>åêä\x0017\x0011PU:[­S\x0006	:.,ySmðÃ¿¿ÿóëo¿}ª\x0004¸¥ó«âëY!Ö9ÜðNk\x0014ðÄ]ÿ?añM\x0014ë\x0007\x001b\x0012u»^a;¢®>b<¤É¯lñgÇ\x001eL'Ú^Ú3\x000ehë\x0010Ú\x000c9a6ÌzKê	\x0013´¶®]Ãh·yû	\x001a\x0011BÓIg
-;âGoxÚ÷³ÄÒíÕ¼\x000cZ¼Ü3Ù®\x001ccÄ\x000cLt\x00085!{N&Û:pÒÅ¤\x001dÐidaU~	Ø4º1ßÍZÙ\x0005ºÍ\x0018]¤`Ü\x001aÎ\x0001©#\x0006by\x0005	ÿÝ­åÂù= G\x001eMyÍFBi	-(n\x0014ä6¿ìÂ/º!WD.Í\x001b=(ì°8j\x0017íÖ½¶£_¨&\x001bÐ«vÌEmÜZË
±Ï\x0014t\x0017*ã\x0001íÈÄU>M\x001d7ÍãO
\Ý7]¤Z\x000fì\x0004ØeL¿Qì2¦ßtì2±s\x000eMñÍ\x0019\x0019Êß²L\x001dÅ
ùam5ChÇ\x0007;Ö6èóJµ¿A\x0003Ñ>[Ìå\x0008´£Ý®!LÐ¾óì¯\x0011LÎ@\x0006v]hþ¼4ºùdËÌt\x001fmZrøOìmÕYÆÒ²
a\x0017Ç)âÚé´»\x001béàFfTpïÙxLJ>u©Ð©º×\nÇ®@¿N\x000fw\x001e´-Klê´îËñW®cû\x0004í\x001eXé:\x001d\x0012mÑTËFª7OÍvë\x001f#âu+4²Údû=7\x0005¹N£½0\x000fì\x0000ü_\x0015%K-;\x0014)\x0007]\x0018Ú÷lKÝìþÁ`Ð\x0006,«Àý/ò;ØJÅ\x0016¨¤«gÞ¡\x0013°7­ù\x0001\x000b\x0018§\x0016¬0\x001fng®NX½ù_Ü=]¬\x0016RM¾ý\x0006Ù\x0011ìû,Y\x001e¹ç.)»òGÌd£¦f»FVÔ5Í\x00064±©É w¸Í\x0010®aG¨ØO\x0016 \x0006Ç\x001f×M=p5wèkÑõ.`p´BW\x0012>*DÐ¥µ\x001ek~»c3¿\x001dÕ®áðú=ÓéÔwmÛtÈ²\x0008ê:v\x001e\\x0015Û\x000f\x0015°
¹Ïrk-o·iÉE	\x00067Ø\x0005Ö­í4\x0016°3\x0005H1«l\x0016$i4Ï­\x000cõË'\x0013Dó\x0012Ù³v'Ë±ú\x001deÙ×Æ\x0019|VÏ¹'G.e¨-ëm\x000c¨@DÏ©\x0001ª\x001dcÆz=§r.@\x0005»éD\x0006õ
C©\x0000¨TÍ¡±ÖAe\x001cÃuõ.¦\x0019B
_B-ÇV\x0016ôÄ%T\x0006a1\x001e\x0000qÑeLnÒ /\x001d!sZOÇ.i"\x00072h¿héf\x0010¸½ÎX¥$Cb\x0005X×»£.äð\x001brj8@%r]!q5^nsÙ··ùA(µ¹J\x00128W,\x001bÍòf®Îóeë\x001fJ¢!ù3\x000cÐ5pÕÌvèE¥ÿ\x001f4\x0001t:1UÌTH,v±öT¢ÙìÈÑ×e'Ì%ÊcO9ný°´%:\x0019þûäË
{\x0012|1ãD,@r2+r±OÑôpÃö5v<§+]ôÀêÁõ\x001ch¾zÍ\x001d;ØKXÊÖùÖ\x001d93×Z¸v¸\x0015pµ/fdtøYæì\x0019ÉëH(Ô&ótÍ\x00184ì 3'\x0017°B¶¼<\x0018üøÌ<\x0013çmÓÖ	\x000bG¿C\x000fG¿¨\x001e5\x0014V]J\x0014jú\¸FîjóÆçYí'v\x0004{]T\x0015&c\x001c\x0002ç\x001dóMN¡ÆÙ\\x0008ÚWÊ½\x0001ãç$ú¦b\®¬táàÞl>e$qªWÒé
Eìî\x000b\x0002vÓ¦x°Cç@ÐÃcó¶drO\x0004Ú3´kÑw2&\x0019H:{Ú\x0012«®\x000fåù²;ÓÕ]©Nè\x0004ÐvUA´Ì%Ûb¹hk{\x001fÓ"gÕ±\x0013¦á+©×ÈÒ(Å\x0011¹ÇÙÐ¸%)íÖ`Ý!à¥´Ú£Bu\x001a¸Ô\x001cÚéN\x000bJBÇ\x0006JBI\x0006:Ï½I\x0013q¥ð}·¶Eöâi¬¡³S"Q\x001a\x0014=´BNö¯øÀË6\ÝÆdW\x0000;7êÄY!-be;Î¬×æE¦a¤Ñ\x0001Äc\x0004
~^7¿7Ú*Øt3\x0016Y
 jÔâ(2&\x0012$°¢SN=ÿ¸[7ÔTª3Tfá\x0003asN¬ktU·Yvu(\x0000È1Îf$¾À	 1¯©\x0011\x00126¶»¦á\x001f¨)ujR.BjÛìk]p§:6p§´Ô\x000e©<}ðKê0*1\x0006y³q\x001d¬\x0001×Aþeÿ´³1â{&Á'Ü£`]ïà#»¾p\x001e\x001axZï¸íóïnàvLäRðÎ6\x0019àn-4-ék]XÂö\x0007'ÏY³õ\x0017c\x00076\x001fÍj\x001fÁußxceÛ\x001fà.b]\x0016·>h¦Ó@±;Ç\x0017QÄ\x0003ÛCçøA úÕ\x0008Í¿7¥\x001ab­}Vû¥Sõm\x000b`\x0007¨Y5",eðMôsººÑì\x0016\x001d\x0006¡§ªÉÖl\x001f
	h*g6%t¢½üßµ
opÇ­öúÄ!pfõ¹\x0010û$Ó6ÇDÿ`Ðá
Ðá\x0005;P\x0014¬úÄ\x0008!·3\x0018òælpÕ/\x0019»Ò\x0011ÌeÂ.\x0007öú1n0°36{¹8e&ÕÿpÈn¼ïö\x0007cS\x0002V§äY£Ò¦2lxá®sÓã&\x001cip+Ûc,\Â»bV\x0014NXky¿\x0011ß/â\x0007x
p1+j1jÖÀvÕ9\x0010
;o.þÁÀ®cxº++)\x00138\x000bb]h7³,ê_
¼@ýË:?T3å¹¤#(7í¬üÏÖT¹È\x0014Þ°H¡¼õ\x0005U}ê|\x000e-\x0017Á­x
]AÅlÀ+4²ÉÉ\x000er\x0008H¥$ÕÞ#ìØ(°òznJ\x0005)+¹Ê\x0010:è\x0010ÀiW2?É\x0012wt±\x0005Õî\x0000÷\x0004²VótV
uø
ø¡+³û\x0015?g@©\x0004DBï¦¬\x0006PXÓë»â\x000bíÀ£-G\x0018(í£ò\x0002L¶;ê&:n0ÀQ¸±M¯«¼çSë1}å\x001b×°ýÁ	.FË\x0006\x0000w¤)£,\x000e_ûý¬e·ò\x0002+×	`ã$jL~§z>-gKýlNbû\x0013;¹ã ªÿæhSÀ+¿vMñØ\x0001öú)Æ\x000e°`²K!¦ü1Y£b¥O=5é\x0007+?¹Ñ!ø¥lÕTÞ,þÁ\x001fÞ\x001e¼
´
¾ä«oÐÈÿ4èKà
:ºGCÏ¾Å	\x001e\x0007}-Í$\x0018M¿¾³ótô5qm¸aIÂÂScÕkK\x0006T°\x000e±ÏÏs{9ºa|2U\x00172åN3¹40Á'z¢Ja®ÅÎ\x0003\x0019®8EV¶¢AcéË\x0004\x001d[éµØy\x0000m±Oïì\x0004Íñ©K \Þ\x000e\x001d@IÀ$`Jp_é\x0018°\x0000_ñíÙ[Ôõ;n\x0004\x0015\x0001SaOZ@4àX3³Ä¬î×¢¯äF\x001d\x0016	»¡Ãa#A\x001b^uöyÝ|Ø¡3êAdÚ¨³I\x0006óªC¯üî \x000bB;¨GÈ7äB:>a{§/ò\x0004\x0007´Eq\x0002uG§äJ{\x001d\x001cGýâú4ì«\x000bp`\x000f\x0017ÀUl\x0010\x0012ì8íaz@Y	C\x001fº\x0018áúÝ»¯ZÏ½­ÊÐøðâpÅdãþ0ÓhÇ6É\x0005EèÚ=·\x0000Âw{=>¦7\x000bÀñ\x0011\x0013\x0000¿Uâ`|@äs\x0016Ú\x001cM`W\x0013Ð¡8äu\x001a\x00056±\x0016\x00014gÍ\x0013V´ßÝ}{ÿöÃ»÷_?Ñ\x0007Î\x0019R>\x000fÒ4Á´»X[\x0018õ\x0019¨*\x{\x000cò\x001dþp´\x00019ÑxjÉ	©°]ðjÍöïÐ@ Ô\x0017\x0008é¶jË\x0012?LÊøQS|­wè\x0008rIÂjR3Þ1ë¶dNêå}í49°+`'ÌÖ\x001b\x0017¨§Rù\x0016\x001dãUÀë¨7_\x0005?þñN>Ûû§ûðµ²M)\x0013j	8L&æÐªSòÊ5\x0001ä:A\x000cflVÿà/_\x0015+ÿÅ\x0017òûtöú§ù
Iû\x0014¹ðtB\x0019åx\x0014¸\x0005ÞZ÷üæa-lá.FÚv¦¸;e\x0005MÐÒà(ÌÊCLîCÔ©\x001cøË]s§\x0016ò%\x0007'?\x000edo\x0000äaÒ8\x000b\x0014¨¢¡>,×LVög\x0019qXñu4 %¹Àí6õzÛ5©ß±\x0001\x0011G\x0015÷\x0000lËâ\x0016)W²jr\x0014Z
®\ùí\x0007öÉo\x0017lï±\x0006iU8\x0003Oáî9S[\x001cX®Ùñ\x0003úÌ\x000btµ@¸ö*xUÙTÊÔëZsÜ´£6phGÕ1\x000b\x00112Ø^õ´1-åGroNSÍ\x0014\x0017éÚ}Õ±Ã\x0010äô	yùâç&\x0000rb[\x0016¼vfm\x0006òJãâÍÝ¿¿ûæËû×O%¤¨ìgRÝ-ñ6êZ_ûØ#õ¤­ûå¹ÍñÚ\x000f´é"Smú?Ò\x0010©ÎZA\x001cG¨­\x001f9\x001a:õ$óoïÉÊ|µöÇ?µÏ¥\x001axt\x0005<\x0013ÝËq9K÷µ.¾rÜ\x0019ýNÁ'\x0004S¹[HÎëÐÝ(ÖvöMìå3ÈÌ¹ëWÝÚR¸D]#à·*ÊÌ\þÄ-G¦\x000fáXôïEîßÓ\x0004Ø%Ð\x0003\x0005ÐÜaj\x000bq¯]å7hÐ×¼\x0004TEÄÜ£§\x0010-'Ñ­i\x0015r5ö\x001d¹@\x0003²\x0014\x0006°ªã\x0003®¤Ö¬kýW;\ll\x0008\x0005¢*«bÏ¤$ÏheäUècêÊ·ù	äacLcÊæ\x001c²G°Õ®½gî9Ü¥¢\x0017b\x0007ýC ë\x0011u½óHÁsX\x001fû0Ç+ã¾C³îlm¬Òóá¢rÄk~âAuÙÓ«%îÐ0. $M¼\x0014ØóÊÞ\x0018(Ëj¾ÓJ\x001c¨ó5G[¾5
áÈOæ±DmÌÄ\x000b®K\x001a]:
{k\x000b6h\x00038Y4JY\x000fÁ]ö.EXÕÓ'\x001eëê'ïzÎÂ.rôivºÆþLÇºêf±\x0015.U¹PÐ2d\x000b©Ù\x0000Na6#¼ \x0003tdèJ\x001c·\2ÍâòJWæÄkö\x0017Ö\x0003\x001aç¹F`Y¶®4·´ÎE\x0003Û\×\x0005U¬AÓ4Wãq±\x0019¥Uçä&ÊUç\x0016-è²\x00076Óeqf©Özd)>\x000f'æ]cU_g¹Þ°§I®0\x001a*\x0007Kjï:Êu\x0013Ûtq®³\\x000flä\x001a)®ZD«v¬\x000c(¨\x0015Ñ\x0016Ù\x0003\x001bæ¸G\x0001Ì\x000bmÕä¶ÊS¾\x000eÁ´ë\x001c×\x001b6MqíS÷Æû=A,ý½^±ú\x000fìJØE×¢XK×\x00012\x0018¥)¦]§¸Þ i«C&nw¢-IÜî_Ú¼p=¡q«¡ym:Â'¸rò?þ%/£nØ8Àum\x0007\x001f´¡ß¯\x0006¸Þ°i|+Ê¦´©XXðÓ\x0000.ÙíÞÀ»û4»5âü¤¤
5´l3\x000f\x0011-ëÙ­\x0007ö<¹\x0015Øm:¹^åi\x0002È*_Èê\x001dÐ !§=\x00020é0\x001b~µ°cíE¾Í§¶VÜ\x0012?iÈ1«ZOIý~5µõ=Íl\x001d\x001f20É¥]F¶\x001eÍ\x001f/É\x0003[Èá$êg×­Gº\x0000\x001dêz^ë\x0001ÍÓZ=òÅûå+é]µ\x0013vyºÃÆa­¡OÝ¾a«ûLÒ]uº¾¶\x0002å«t`Ã¨V\x0001Ã/©4Çªå=Ie=«õÄÆI­\x001e%4tÔ4Éö\x000c]LX©
¯Ò0\x001f^üæÝ·ß¾~*âl6×aMëBëA9Bð&kSq£,~\x0006ÉØ°¸Ní\x001f¡ÂÐ§°¨Óßhà©«,kS\x0017ª^4W´Ä³Ò\x0017õFZ-{ ´ge6\x001bzÝ|qt2\x001f\x001dÝô
iMm¦«*\x001f,ÓÃ,_¬õR]õµ\x000fìè~ñ\x0003\x001fôÁÃ Ø\x000b\x001aZÇ.\x0005°
8B\x0012ùy·)³Ð¹\x0004»uW\x0018=VýK¨\x0019­@tSL&5[ZPMzý\x001c¨&ôÝä\x0012¥æ\x0004\x000cìÌS¹Ì¡:¶¨Ùvl\x001cöV\x000cQ-\x000bÓ+¢&©\x001açW°®ýêÍ»\x000f?Õ:)Û(2u

Xzy³Üs«ùµF±\x001fîý\x000eÞoí1\x0000\x001d¸§î8Øâ\x001d¶~¿ë1:¡\x0001W\uH¼\x0007\x00072¹ùÇÐû¨¯9£æ\x0002Ä	S#*^7E\x0001¬,\x001b÷k^Ñ\x0001
\x0001KÐûã\x001cþ@Ô¬vðÝ\x0017þFG\x0006Cwz8ÓrJBk7EOûa£¾ ÿI{\\x0016íqDÏuj³çö\x0002çûÃ\x0015I§a[\x001cHy¯ÜX\x001e\x0019:\x000e}
\x0014\x000fh\x0008\x0014C\x0004õq/>å$QÍÂæN·hÃÿ9°\x000bm	¶#û©UE	;6¡\x001d»cêØ #i={_8ËÓg>¶\x0018À^ë¥7l8Þà­ñÚ^Dë.Jõ]þz¡kp@ó\x0001L\x0008]'èÊ\x001dñò=V2\x001bq4þÕ»÷_½~óT\x0013ÞbÚJÉî|UÃî²Ø<»µ-\x001a«^\°ëu\x0004D
U\x000e9Ô\x0006\x0010\x0004	Ô84HM`åEC\x001eX­±\x0010?bÓbÔÆxÎ^ä>äz:ðèm­U\x0015± =/MuÄú,Åî]Ï{Æ1¤â\x0001 sQ\x001e
@ ¾î½èØä|Ç®\x0011ü¯}íAÂ-ñ.Õ	[-nZ¤+\x001bv:Óz

KëTÐIò[Ñ$XïÝÕ;ìØË\x0013þàíhÐ\x000e»\x000elk85"½ÊQÞ÷é[¶Ô^¨y4ìì\x0001;\x0010UTbsj%ÑðÙ#ØÔY\x0017í§\x001d;\x000e_Z"\x0011\x001cO©Ø8¬F\ú'ìöz.:ÿ:v\x0002-/-²Â·+JºI1°Ã[|;'y!&×±K\x0004ìBW§\x001a\x00121rûÏAU.÷3vºÇØoç,§Ì-%Zc2f(®`)Ñ\x0001»@v$«Ò9IIÙ)©èââ­p~)oö¤\x000fcðaúðù4¶\x0007Ç\x001f\x000c@~nÊ¿¶Öþ\x0008Ï\¶=sí­¤\x000e÷èVÉøáÇUIÖ2;d\x000fÈ\x0015óâ\x001a´¼Yo«ÙËi¿!ÇÇ"_Þ\x001brzìn\Nú
9ó#­\x0019çÅ[ñb³nÈå±k¾¶,\x001eÐ\x0016?aÄÌ¼ò.2Ñª\x0013Ó{Öâê\x001eÈ\x000eYÕT©(rEfìÄª¶Z-nÞlþ\x0001Á\x001d\x001b,ê%vj&\x0008GÿöÅ±:°Á±R\x0017
+_ÚZA\
6=\x0001e¯Ï
ÊÂ\x001b;ò 
j\x0015­
¶ÃCâ0\x0008rù((\x000elÚ!È¶¬+Z\x000766XTÒÕ²\x0008æ\å[Ö)\x001b6Zº7l\x0018ª`ÈqçA\x001dÉf%ØkEkRîÀ®$<öI>m¤uÏ\x0005Ð\x0006®Ù­í!»\x0015Äs\x0018-Ð.éÐ\x0014ô¿'æìÙjä½æ¡?6©î?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹
ÿãø¿½\x001f\x001f+\x0000Ã+\x000c;Î·\x0008: AK	GzIÖè¾,Ôê·øåöþæ¹ìW0_­mé$\x0017Ø<\x0002"ðâÃk#°F&,=îí+úY¹Ë\x0001\x001e2¶ãc5¼§ê@%!·\x001d{p*\x001azãö%ÕÂeûæDTç­ÿËÛ»%Ù\x001bY¢S	t\x0018Þp\x0018¿"TñÆÌº~ÊB¡\x0014o3I\x0019\x001f²®ûUÓ¨\x0011ÜÖFÎ¤Frá;öÆa\x0003`\x0003q»L,\x001dfI½\x001cÛáp8Ü×Ún\x0014_®þüðåïïû¹.2V
z\x0004YhÉ/(CpòæêÏ·o~¾;Kè´\x00034¶ÇÁº eÙ¡:0¤àØ·Ûé`?Ú4!fàÆý'hmó\x0010L®¦Ñ´h\x000c(¶yg\x0018^¥§àò3zëIk	ieJük?:öÃMäS««,4\x0016_ý¹\x001a¥\x0018­_¸¸XØR0±ÏD\x0010ô¢«ñC\x0016&Í\x0017Ö¡eÎ¦
Ç\x0017î9z%(ìÂ^\x0018\x0011\x001dKP\x0013p}Ùh\x0011®á®\x0015g\x0019n³.9\x0016%ý+`oY1\x0014T³\x000f¬µåDûÅ¹\x001f-\x001ef**`ñÀmk\x001bø<\x0014WhÞcûáâC3p­¤!Û¸¸x;±1Ýv_QFà\x000có\x0004\E\x0005¼ºü¿[ÝQ\x000cïÎÌÀu²\x000bTæU¾D±v{X?ÜÓáÓ\x0003p==+çÆÓ Û}µÝ»Û\x000f\x0017ÇÇ`*\x0001³z§\x0003XRÉÈnaì¼àØ8\\x0016¶>\x000e78Mp
G]pW·£æ?\x0000×bñÔê\x001a\x0016E²ñ>-È\x0019lq¾\x000bO¤J\x0018\x0004OmÆÕØfLmºö3P?ÞÔY,§7\x0004*îk\x001b·§HæKsa\x0018/ò\x0006¥?¯o¼@L!¶ÉX¢3P7^o:?Çñ\x001aESbÉ\x001f(;\x000fª¬¯iV±úñªô(è'îj^	Çä»È·Õ\x0014ÊSH}^\x0014e\x0018¯Ækpúc\x0002/÷ÔE¼ÄR¤*e\x0013u}w\x001c.È§?Ã{LºrVøÌª \x0004«Tó¬úãp\x0001ï\x00130q¡ð8Øè·hçæAIUvÛºÍfp^Þ\x0019¸HV¦(q\x0010\x0005¶\x00140\x0007¤\x000bÓ2ã\x0011¯ÂëbpÈwa\x0013<qkÅÌ89Z×b\x00011ýq\x0018o¢1Íî`bÒ£\x0008/P¦cCÐë\x000e\x000bÏ\x001eÖÎ¬¯1ó^\x0003|	\x0002£rójÄ»0ÓqXsr3'\x0001L\x0012\ï9ö&vÛf"èÇ\x0017 7s\x000bòÖðdnÂëÙ\x0008ÅxÛ\x001c1ýx3\x000fÜûâ3Ù7{¯µ$­p\x0017.o¢@w3©¤Ì@Ñ\x0001\x0004©!Þâ½ívñ~¼øîåü\x0014^§i\x001cWoc¢ñ\x001aä\x0006Ýûux\x0011Ñ\x0013/¦¶[¼\x0008\x0011Ë±)AàD0à\x000f\x001eûá¼I}]Ìwµ.ÑLæÃØ)_ÂX\x0017}=\x0006^?\x0015}âFë7\x0010^C\x000f¸ñb\x0013wSxcxPáôts¾ÐøC{Lj\x0000/¾OÅ\x0007ìmb¸Ìå\x0000Xø+áa¡ûbdðSá\x0001\x0002_\x0000jÛ\x0003¼03ÞöÔm?^|eO\x001cÇ\x000b[8\x000b\x0002Y#\x001dXø®\x0018aªòàb8£'A\x0013"tMÑºàmórõãÅ­\x0000SáÌDôñ:\x000egÛêu©/V_ÀTÝÁKÃÁ×
Eî\x0011­+ò)í\x0006Î~¼øß\x0005S¹\x0019²-\x0019Kx
s	xRðKx×\x0015%\x0001ßoÁN­¯14Âäih³\x0005Ã©dXX¡\x0006,ÁI%½	¥L"<Î¸#^\x0010åf\x0011üº³\x0002ð©³"&\x000f4]ú\x0005(7\x0003I¹äºÀ\x0010ð\x0006\x0014¦®A\x001eG
,T\x0014oÅ\1\x0013\x000b]!`\x000bRS®\x0010\x0017¿´á5--÷6ÈÅÿ¯ÃaæØCüúËéÆ9Á 	å~¸XÌ	S\x0015xÄ\sõÔÑ\x0010\x00003£&ï:´\x0018oÃTÐ\x0005m¹\x000b\x001f®èFjÉ¥eq\x001d\ÌuÃTÂÔ¥És£±1\x0008ÊºR<]ÙÜÀJUö¦\x0001SJkfq\x0013òûk6*\x000e\x0005³\x000c\x001a\x0003Ú\x000cj\x000f1Ù!6wT¢ä\x0017hÛÙÐî
m¢þ_î»¿'\x0001\x0008~}ýíáêæã×O\x001fßD­/_ûÅt|HÝ#\x0011®Õµ 8º
y|\x0016:÷ÝíÕÍË·¯^Þ½DÉ7oÏÊêì\x0010S;Ü\x000cbCÍØÒ,ÄS4KâåùüÞ;E6&\x00179Ï1Y½\x0011º\x0007/\x000bä\x000b9Ä\x0011ÈL)>\x0003Yä£9"vLW\x001c¼`Äê¼ÌF?â_äÿ¥þwR\A'Ã!â$ãùé÷¿Üx¿~¹úõ¿þã?oþú\x0019y¸±çùå§Ïý\x001a«\x0010w`²Â\x0008C\x0004h\x0005I±Äÿó©|´âé«\x0017?Ü¼øß¾¹ºùé5\x0012rã?~ùêõ9ÕbDõ´ôÇr<Uº­Ñå\x0003OSx¯ÎkÏÚd\x0012¡Ç#|&\x0014*ôÙ&g©
°Al²çe\x0015gmr:c½MÞÒ9`­\x0000Ö6
N³MáB\x0011dÒ¦¢\x001c¹Ú&ç?Ûä°dlÈ6] ´	\x0012Å#|'ë)C:\x0008&9\x000f\x0006}¢Í\x0017# )WÀ#Ø\x0004tQ±©ub¡\x0002QüN\x0017zì\x000eÙ\x0004áã_ÿúpzö<ÿã>Þþ5\x001eBýôåËûNü\x0014órU¼
R}6î\x0017n­QîÂðÕ;\x0014xõòæõñ\x0014úéÕ7wMÌH\x001eÿÂ/0\x001b\x001e½2ö{Ä|¡?á\x0008f\x0012ýÃì¹V\x0000ÚaûsÆLÊC\x0011óyA½#±@Ï®s<+hÄ
rWqÂl¸	þ\x0002\x000bå\x0011Ä¤\x00047Xóx\x001bR#@ºá×øÂëÈ\x0011ÌÜÿ<Ùñ¨\x0001b\x000e6c¶ør=8õYÄÀÒÌÃåÁ¤¸Êç¨`F\x0002÷YÏpÕÊÀ\x0008ÒK
8U\x0011óÒíW&g æÂ\x0007\x0018E\x0000ñR[ÂÜ\x0005ÅÀCÆñ$f¼~\x0011fË4\x0012Á\x0004V\x0016R'\x000f`öéÁz\x0016³çq\x0014,ÞdÏ`([ðÂÇ8æÝà\x0004h­4¾ä&\x0006¹x4\x001cèà\x0002Íç\x0001Ì(KþÂ\x001cWFÖPL(ß=uÔ+â´XéÏ»>Ó)Ì,©\x0002V9´ÏíøÏ/Þ\x0001GAãgKL\x000e\x0013¤â1Ù;Êà¨V\x0017\x0004\x000e`Nü~2@#§\x0005µa52_xs2ðB_P~8\x0000\x001aÙ\x001bÒ\x001fS\x000b
ø¶4\x000e8Ò:\x000bögu¡h\x001c²JBÉj2Ý0Ñ%I×a}ÚÐ:ó¤¶K×9-Aúc
´\x0016Ä8£q%ëí$A_¢\x0008;\x0002Z!h5»Òê½F @*\x0004:^²Î×§»Aÿ»\x0013¿IwR¡~þí÷\x000f\x001f¯~øôíC/I\x000f¨\x001fgå=\x0017\x001c@º ¢\x000e¹ðæhß=½»}yõÃ«wÏÏ\x0011´ì âúN@\x0015»2\x0010+\x0005eì·c¬\x0017(2G±\x0016ÉÎÃ`K\x0003ªCµj*ûBo¢/<`Åã®\x001cy\x0007À\x0002\x0000w"'½\x0013­ÙûôÀ(Ø$W\x0012&À"Ñ\x001a÷SêLÇw7ZYyíf\x0014,v5Ã\x000cØü®ÁJ\x001a¹ \@\x000bÔ}`ÿ×ß?/Mû\x000b{\x001b2Ö¾~~ø\x001f?ÞÿÞÔÅ\x000biÖ\x0017°*¨kzz\x0017ß#.µ
D /_½}}{õãÍ6Ì2÷~\x000c'jÓkzJ®©½\x0005¨½\x0005åÉ/F\x0001 x\x0014ðqp\x0000¨æMe·D\x0006\x000eØãÚpù?\x0002tWö9\x00024Ð1kbd ôBi/uç
\x0002ÝU{\x000e\x0000un\x0012\x0016K>ôÚÄ[\x0011¨¿¼óG\x0002Îû\x001c\x0006\x001a\x000fÕÜÒ\x0014?½"\x001dD_\ñ^Î¶\x0006î«$GVÔg\x000e®øå\x0001@Rß+êd_¼\x0003àD	Áã\x000bê\x0005ã´&A#NÏ8ý:Iï0NZUòÚÒih&
\x0017tÕßù\x0007ãGNäa\x0003jº3tâc¸¿÷\x0000Eá:3óå\x0003GQOÌñÓS\x001f\x0010î©U{\x001e»\x0018­	N9Ð&\x0012AÂ	\x0017ôò+×\x0000Î}õëª\x0012DãÚr÷­q%6]îG\x0019\x0001Êì\x0005"\x0003§/ï4ñÅ×¢\x0004§\x000bÄL@ã÷Ç7=X>è1#¡a\x0018:ùÓË\x000b³fc@ñU\x0011äñ½¤¸\x0015I@Â\x0000^v\x0010è*L\x0004q\x000c§°ôÒ%Å_Þo	Éªà\x0014°óïð^²Á\x0013¡B\Ð¢ßí\x0015?mÇÿü¢\x0014¯.\x001f\x001fAªK2Z¸	"R]6Ó\x0005¥1¤\x0006KlæðÉdQÎÏúÀg½ÚóY¿*wIÔÅ\x001c>b\x0000¢¹tØ\x0003\x001döbËòì\x001cÒ\x001fà¯\x000fÉM£¿\x0007Ê~~ÿðùóÃÕû÷_¾Üw7,hGµa#ãe$P'¸\x0002*G\"vP¾»}\x001d±¾¸¹{óæ¦6IXJ¾8\x001d\5:Ã\x0005QÒ\x0013Íe)wI{\x001co¡Ò8×
¢:x5\áÊ\x0013\x0017Xùáâ\x000b£ägÆcp±ÔGÞ´¼¥ó×ÉËÍ=x±Ì	\x0011Éö\x0017Oðç\x000f\x001f\x001er;ÎÍoßÿòíÃ×o»»#NzÓ'WL`\x0012vaB]]¸\x000bÜ<~ûo½¾{úîùÛÛw¯Ï5\x0001³\x0001ÆV\x0006àekÞ\x0000¡\x0001D8)d­?]ð	\x0002j\x000c\x0016\x000bXQÎ¸bÁÙ\x0003ú\x0005P[\x0000ó\x0016xC-#É\x0002j\x0018\x00165m?¯kuÄ\x0002dËÞYÈ³'-°ZÐ@É4ðØpòªºP\x000c9d\x0005ø¸3iA!¬6²åNätªél\x00068ýä\x0004ÿç_þöþëÃ/_\x001fúép\x001b§8äµ\x0004_yRF×½óoñ;ø¯þéîííÓ··-ô¦BofÑK	Ô}²¨ZøGXo\x001eÿ×Á
>Ì/>s<{¤Ýòeõ)\x0002ósx\x0007ÐËøwèñç,ü@ãB\x0011¾ât\y^|{~b÷\x0008üÚóå´ë£óä\x001b7\x0015\x000fh¢lô8\×\x0013zºáû\x001a¾Ï\x0005\x0010ñ~I2Z	J!¤:¸\x001fÀ¯$ìñãÏIüÊÔ\x0010H©>\x00154²eün©÷kå«Àosø\x0005\x000f\x0018Å£\x000b®9ôHÎÜù7ç#ðw	\x001cÂ?Ià\x000elÞ\x0000¬-¯t`¶\x0008Í©BXµ{
Uz·¿xr½}þúåêÙçû¿ÿ
ÛØûÙPU+Oç}\x0019\x000c¶È\x0017\x0000@
Ê\x001e\x0013Þ¾¹zöúæç?a\x0003ûY3¤ÊÔçÅø\x0017O*+ðIõþão\x000fý¹\x0003öPþ&&!¶Â­BÐÙ\x000bâf\x0000>«Þ¼|v{>u ì2ì±Ë0	\x001e	´\x0018¼%ÙLÔ¯àÏ\x0013\x0019\x001e\x0000¯ì\x001e¼²àÃÁ\x0003Q´tóÐ\x0013<»ÁëjåõÜÊ#CÊ5c\x000fL£¢ý|añ\x0000vS-¼[xÝDa;u1Èý<»è\x0001ìÖï±[?]cT!ìÌ|(Ç\x001f8ÜU«îfWÝ¤\x0004'#·\x001cìÚïÈ{Àc¿n\x0003ïàÏ\x001dú§÷ù0pÁòÆ;Ê\x0013B\RZÑ\x0000Üyâ
ûÓ\x001f_º]I
'\x000e\x0013ïmµÃ<½ÿü\x0019{è\x0006Ö]FyBÉ{ãHÛ æhT°\x000c©\x0016Øýõkì¢»´ðI÷\x000c'$¶¿H³\x0012;øï»ÿ0p¸Æ>ç\x0007¨4]Èæ\x000c³Û\x0007q¾\x001b~\x0007ýîÙÍó\x000bjmÃ\x001e¶
3°\x0001{Û -\x000f\x0015u¬¡ Âî9ú`;½íô\x0014ld5;\x001aXË£\x0007áÂÇ0jS¡6-	tày\K}\x0017\x0011ôùQ¶AÐ¨.¿\x0003?gPK\x00123ÖIÒ8kM´y.\x001eý=\x0001¥\x000b·¬\DÊ)\x001fñ*MÆÆ7qïZMíá¼¦ß(j]¯¶ZmïiØÃ ¿"\x001d=V3§È\x0005ÊÕaØ¾í'açF\x0008\x001b<m\x0007;\x0013\x001bÅmeÛÊ\x0019ÜÑ£uÆý[Dáb%½;ÆEZæ%¾^n?µÜÆ\x0012õ¦qédÌÄ¼è\x001c\x0019·î¹	uáF2å\x001dnü9[;z=5Î\x001bî0¬dåãAG\x0011©\x000f·ªÜ\x0004Îà\x0006W¸yp3®7\x0014úÌ\x0006¼\x0008w½Þjj½º¦å\x0006A2+\x00116%%\x0011öùïQØ\x0016*Ø\x0016fw¥'÷öüXf%ð¶ì)TtÁÖ¢J\x0001ñçqØV\x0004ê¯áPd
\x001bW\x0012liì*ï6õ®4s»\x0012\x0007f³ú XK\x0003³MQORçg,Fq×g¥;+\x001d\x000fìEÜ{#îÀ¸Ï7[âö®ÂíÝ\x0004n¡/ûI°pÏÊrÓrkÙs5î\x001dª«\x0002þ\x001d\x0004\x0013le-^w(xÇkÚ3\x001e,
8mñd\x0017ºQúé§¿|úükwÏ\x0012À3^J	xá\x0012çµ\x0019xüû«§¯^>}õúÇ³zÚ]í±«9ì\x0012\x0014kSÇg	»T=u]­Ã®÷Øõìº\x000b*\x0000!7?³ ÅDÉ\x0003L;K\x0019ÁnöØÍäºc÷)ù\x000cX\x001e8\x0012¡°KM:\x0002Ýî¡ÛY1ÌËî}à~t),)Í\x000bÛ\x0008v·Çî&±\x001bÇ#«>z>UÉ"6­{3¢@÷{è~\x0012º/²§>(â\x0016\x000052Ó?ßi{\x0000ûö¾"$ÌnUM\x0005\x0015|§æ¡¸UÿE,
3ºò\x0019=ë4ñ`"®æx¶ÒÈp\mMO¥ÛÏ\x0001ð¶Zy;¹òØG,ÿHÌzQ,Ü¨.Ì·\x001eÀî«³ÉO\x001fNY9½\x0017|{ªìVw^ùù\x0000x¨\x000e'<¤}¨¡¼Àì%þ|ÿþ\x0011èÃÃ¬ÃbÅDÕ9rxÉÆ/]öPùLõ\x0019g\x000b;Oiaë\x000e<ß/Î·¡ª
ñRÍ\x0006ùx¡¦¡i\x000få	:þËÒ¯\x0004o*OÞ\x0014xeY~ÊÓ\x0008mSdö©¥Ð]
}Öã#ô°mÖÀÍ§\x000e\x001eeÝC
>LÞ°\x000b\x001bh\x0013xVÀýº$ÆÇä(Å\x0007c¶\x0004Õ
ûöÃÃ/_?¿ÇöþW9Í¬e ¤@ªÊô*g³ðHÄ~^1r»öÝ>¿}úöõ\x001d\x000e¶½û\x0019ð«²úñ/¨êÊúìáÓïü¯»o­\x000eä¾/M¿¹cºÞ=~à×g·¯^Ü¾}}þÚJÐ·\x0013
¡×\x001dËãÐ3Ä5\x0018^K­¨ßE^ÐÌ\x0018ÁnSW%­Tß7ìw¿ÿýóûßG¡±\x0016k\x001cNâ\x0000?C¼aÁ¨öûÍÕÝ_ß½¸ô\x0010Mà·nA\x0004_7\x000b\x001e\x0000(Àû2¨§97\x001dÍ^ýàU\x0005^M®¢3xÜ®VÓ,\x0015QeÑçiw\x0015x7\x000b^P¿\x000bVexHÅ\x000b¯\x0019¼Y	\x001e*·Y·ÑÃ£Û\x0018î\x0001ðØÐAnÓÎ)\x0007À\x0007½\x0007\x001fô$x\x0015pä*WÜ_ê\x0019/boß^G°
»Å®\x001d\x0006/ªÜÙèã`Óó\x001aÖ½
a6PJ ö\x0000pRÂqA\x0016ïy9í\x0007\x001f*ðavá5½\x001c8¼[\x0006ïÙkdè¨À÷ßuä#øü#Kïé|u\x0012\x001b2\x001c=¢í¤r\x0000¼\x0014\x0015x)fÁK*®ºTg%ìì5=\x001cýÐM
}v»
ËÈ\x001bÐ³¤+NÓQä\x001b\x0001ïjð'	Lù\x0010Á»²_/]ê5¾FïgÞ\x0010CÃUzNp4À>ß3Ø^Õk¯¦×^Qe;®½&=lhä\x001d«z\x001eûÑ×k¯&×\x001eUú\x0004¹=¾Æã(Þ²É5×UR&³§À¥X'³¸M^zÒ*Æü`ab&µ­ÑÛYô@å\x0003'}¡sVsN,Îó\x000b\x001c@oj·7³nïY!ÍaÅNN\x0003Sva~³«~dô§,iEçµ×¬Êí)%®ýÊû´õ1k'YãSßL^{KUbÇ#3æÄÐ\x0011ìõµ³{Ö\x0019*Ü¤`O×Ø\x0018p<£·+#Õ5úÉ\x000b	ê\x0000¡\x001f\x0001\x0018}àÓñ$5ÞÕ~ãfý\x0006\x001bR(3ö{\x0014|\x0017ì\x001aµíG_¯½]{\x001b¨\x0011ßI$á¥#\x001dU\x001dEú\x0011ôuÄq³\x0011Ç
Ñkæhq\x0016@w5Ñö ÷é%v\x001dû''ÉñÇ¿~úüûý×ÁkÜ¸4e<S²T\sØ	Þ÷
ß½üéÕë\x00177o\x001bE×l\x0012{#X`u\x0011ÛèÄ&øÝ;d\x0002T&À\x0002\x0013¡£\x000bM a\x0014âLC\x000bz¢ç\x0005ûÍ?9IÙYPÔ\x001e£\x00058UKzz@#z¶Â\x0011¶2Â®0B±v´Ç&ehöÈ×\x0007±îKÐ\x001bÿ¶§ñ¿ìéy¸ÿxõüá×÷\x000fßzÑ\x000bìà"P§èÂè#hz2\x0014þ¼´\Fÿ/·7/¯ßþxwûî,ì j¾\x0008Ç¤ÜÃþøÅ¯>ÿÒ<5ðJtwu·\x0008©@ëå\x0007¿ËÏ
è^ï¡{=\x0007ÝÅ¸oXë\x0019½,¡µw\x0007
yE\x001ecN¦ÙIJL|Ç
²@oÔú¡KQAÇsØ5	'ìDã\x0016\x0003/Ø-;2\x0007ì±ËIgwJ¢`Æ.Iµ\x000b¯çììá<iw?vëBÝxfqvc\x001f"ûú·I\x0017§úq)\x000eßóhv!E1¡ã }þîí.
L\x0012ni÷¸¥\x0000S´t'Ç`È Ò\x0003\x000fÙÚ\x001eFNà¦\x0002næ+wm2nÔ\x0004¡¦§À<(Vv¨°·+\x0015Â®oTÃ°Q×\x001c\x0005$K\x0013Ù	\x0008lÏ¤	º\x0013K:i±¢J'_üñÏ¯#Àñ$K@`ë*\x000e7çh¹\x0000¡ã	ÿÅíÛ\x001eÜºÂ­çp³\x0006¦CærGeî`¸xà{¦o:q
·ÃÍ}þ.Q\\x0012n(?è!\x001dèÄí+Ü~
·ð45ä	Ì¯ä@puøÚ(nUáVS¸±ª-h½ãáOwmW^/ÈE\x000eÃ
6Ì-·¸öÜD\x001a×e[xÒ{»\x0018!îúb4¾Ü¬\x0001ý©Ìê\©¦^à¿\x001fÆ]\x0013=\x0015N\x000c:ª2
>×°\x001d×°{hL:aWÞ­ç¼\x001btéè05q-ïÛ=Õß>Ø[Ù\x001da×U÷aØ>ðc²æ<q%xgL\x001fÆ]-·[îJ)
&:`[|Æm¸jêz'ûpÛê·S¼ñôHÒaÉïKFr4é*Ttâ®\x000eK;uX\x001a¯èÚ\x0010q+¦,q<8¸;úÜ:qÛ
·ÅMoJ
g&\x001cãfÿv=D}¸]µÞnn½qe9,¹¬ÎÞí{º:QW«íæV;\x001e4|´"ò»xã,1PtÜÑú`ûjSú¹Mi®\x000céÈ¡n<'øý¨m¶\x0013¶¬`Ë9\x001f±üî¥´äò¹qÛ°\x000c7T	Ìe&¸Æ¾\x001cT1w¢¼\x0019u\x000cîuã®2\x0013ËL¬¤:¡S*.0Yz\x0003ìºØ
Õ\x0019\x000fsg<\x0006>ö\x0013àú¦
ºlËóú\x0008Ã¸C;Ìù'*Á¸ÞPü¸(q½×¥¡Â\x001d&q\x000bîUÊò<°
ìÞÖ¬-ÅIýa®\x0000!ÊAGÜÄ~è;ª­éa-é\x0004^_äÅÜa©\x0014
üD\x0007OÔjiÁ½)WO'p[\x0003;/5O½GO)cÀ6ÞÒØUÔ\x0002W	:yø\x0016Q~\x0012rDùã\x0004üýçOï\x0007¡Ãëä,¨\x0000HÁPñác\x0001z\x0012ð»×¯î.¢ÿõ»müÝ»íËOñ}í\x0004
"XL\x0001]²àñ*dQ£âw\x0004ÝÈ«^¾ÿëm\x0003ì6ÏæRÃáA°ñ"l	l\aO`Ý\x0006ö¼:Ø\x0000Øí`·[Â X\x0017r±Ø`ãY~U\x0008ÊUÄÚ\x001cèÂºeOuË\x0006±Z~î6Ò)êÔ
JñÓõ­Yä>°¡\x0002\x001b\x000e- &Í5f¬r8«[-\x001e]P¡ò\x00018ê\x0003ñÎBn2WúÖaÝtb4¸He¸V\x0004T\x0010QJ[°¶Þ6z°îÚø\x0011ë®\x0014,ÛÚÓËWDË2ò¶Y8íB«j´ê\x0018ZÄÌÉ	ðHË¢ÛRH`ZwÀ\x0006Z}Bâô		ÊýÇ¾úðþ\x001fñ0ëÅ¬âY h`Ø
ÖPcÖÜAÇqõêùÝãQÖ@¾=\x0019!òýÑ!è(iíË<ÍbI¬j\x00105A{2¥\x001bú&µÐµî\x0002Ñã«4rdöaÍ\\x001cf!tSûË¬ÃX@PfÍ¡b¯\x0019|\x000f\x0013G'tW­º]uk©a3B7LsªÄÆ©°nÑ«»Iä(ëHãåÁq{¸ÂÜ ·\x001fº¡û
º'¹7*s,~äE<\x0019\x001f\x0013çeÐ·R
B\x00075\x000bÝ±"=\x0008Å\x0003Î2\x0014Æ\x001ch?lôB\x001b'dÊÎb\x0007*¶Ç\x0000.¸AV±î{¼åöP\x0015ub7Ç0AcÇ~ä\üHØY@ð©¯U±º\x001b»­Ï$;{(	Íá\x0011¹O\x0008ºag\x000fíN\x000eä N$\x0010»#éçû/¨×ÕcI
x\x001bÄ¬EHMtÄAs)Õ\x0019Ý¸úùæ
êtµàª
®:
WI
\x0006ûs%2(ª09c[sû}hwn\x0011Ñn^16®¨U´¸æ3\x0002j\x0010ÁÅ]ÖWhýa´B\x0010_\x0011H\x0011Fkë8à\x0019ÝªõÁÝÝ¹"ÜíÎ5\x0008WÄü({ã\x0007£!Ór§\x000cWµNÅ>¸Áîá\x0006{\x0014.R«g\x001a°\x0010 ø\x0002G5£ZÏqh¡B\x000bGÑ¢¨4í³"\x001b\x0010\x00141 ÜVw\x0017ÜÝà1ÂÝ
\x001eâÅ¼4ÐêÆCÓê2ËZ{h·\x000f¯®ñêÃxµ#é×^ÓÍ\x0016<Ç1u^\x0005}\x0004®­¢înÞl\x0014®,!\x0008êt\x000bÒ	bË4²u²uâµ5ÞÃMi¾a\x0005\x0008ÔQ\x0003^_Ùz°êÄ\x001bj¼á(Þ¸Ç\x0014ãµ4\x0000\x00116\x0002[ÓÆêëªà?\x000fÁõè²Ò\x0011\WÊHº¬n+3î»» Üí.2\x000c×q© ÄÄr\x001cYt§u«öÝ\x00077Ô-\x001cÜl\x001e=x\x000bC¹¨ø\x001f²Å\x0019f7[Òö1;¼ðÄ¨ê]äç?þß_þ64³$ôf\x0019QÓ e^\x001f+zä¾}ú§K\x0003y\x001c*ä0\òÚ
\Â\x0007\x000bÜ\x0005aem±\x001bº¯\x0016ÝÏ.:¿Ê2Ð`\x0003?Zv1=ôÂv\x0015l7	\x001bX\x0003%½·\x0002SlpG¬5ª£÷®\x0013úÖ\x0008Ð©\x0011â8t¢ÀyÍMé-\x0015LmbeOGA/òjÑavÑ½e\x000e¥xýçq\x000cg¸ëÛê\x001e*Nè¡Zô0»èV×b¤k+ý>¼è­\x0001»\x0011äUl	³±\x0005ûÂr\x0017EiqÌ\x0017½á¯\x000fúnØ\x000b¡ó°×Äªûkjæ)5\x0013ü)ª:U==m½ÐC
=Ì.»¥w
§E©°ÇOP°«e¾µï=v9\x001bÓ­Ú\FÆdÌ©ÈeÖ-»2\x0015tef£!\x001eÔ\x0008]`û)EGÉÐ{úh:±ë\x001a»ÅÍÔ\¦èû9Q²\x0000Õ\x001am\x001cÁîjì³¡]'^¹Ý\x0015« ø<U=
nØM½îfvÝÕv,	Íã\x0016´bì=\x001c&ØmÝÎb!=°Ï"¸ìñÉª5{5O8îª|áDËòç±xÖ»\x0018\x0014ó(\x0011hPß\x000fL{£C°ÎÏ·ñ\x001f_àÍÀw\x001do\x0008ü¤ãm\x0014¹Eª\x0000B\x001do<rG+®\x001dtEËÀ©
\viü'¶jE}sÿñë§\x001fÄO!.EP"50gª\x0006\x0016H·=ÍÖon^¾}õòå¥Æ1B\x000fb\x001eÄ$zlÆÈ\x001ddt*ðT,!+ÓCYÒ\x000f#\x0010Eø5è8|\x0017bFSH@JB~UÒPÐwäí\x0003è¡B\x000fÓèYó7¡\x0017L\x0014ÍÂè\x0011~Gï/U\x0005_ªyü@\x0007T^}jÖ0òqà»ÊõO¨\x000eÁ\x000fT
ÏËÏúRj[þûj?~_ã÷ÓøãÃwk¯Íã*jJ\x000c.HI4aÂGTæ\x0010^0~½Öyê­+ç÷®4cS;ñeý;\x0012nüjSVCüøs\x0012¼\x0006æ7mÀÖa¦qP7¯v\x001dIN?~]ùÒ³þ\x0003\x001a(×ÔZ`\x000f.ÕîqëÄ¢T\x001fÄ©RýÏ¿}\x001e:vg\x0014ÓJ\x001a®¼dÅth±$ô·¯_¿{Ý\x0006¯ÙWÆL¢÷´`\x0012z\x00128Pü®\x0011ÑÛµïE\x001fd>È9ô¨UFì`Ø¼D7q­]¼ö2å\x000cªoâ_DÇ¯ÀýöëûO½È#FA{Ö(\x0019è2\x001b¬£ñ
çz2Í·ï~¼{Õ\x0002m*Ðf
4V;\x001cÖ¢\x0005k¸}Æ\x001e¾>Ø[?=Â®§\x0011\x0007a+`-	#±NFk\x0014¹ï·§¬ÚzÕBÔõ¬Ö(êx*ÑØ\x0002F´1)$T6´»!;QK-ö¨ñç\x0004l#Y\x0017\x001bå½2Ïo04\x0018ç¬ë©\x0004·`ÆÙ`êÆÙ/Woã\x0019ôð¡_Z\x0015¤äCÈ\x0008Ï|\x0001uéM/´FZ\x00108@·Ï/«\x0012ô­}	¡×sûÃÐEàÜÝ`8·Ôgã¸q\x0005z¸6{û
¹D\x000e@\x001cq\x00119ñq\x0007U:Û Ú·\x001b¸ª«IàD@epº(P#5¦ _è,P-9Ì.9\x000f\x0014DèÀC\x0010Ê@ñd±\x0013º\x0014Õ¢ãÏ)ì8Íg	»§\x0007\x000f\x001cåâ&&\x001bâ\x0008vUcWØµ!¶\x0007#¬£\x0017Õ !pÏï©\x0000÷b¯C£Øw\x001a4ag\x0016ëx\x0012v\x0012ßÃhÒÝ×Øý\x001cv\x000b×\x0004ÝÒZú\x0016®ù6Rp;7;µÄx
&"|\x001bÄïyïÅ^\x00189\x0017câÕMp\x000e\x0010ÓON¸dn6®¹§]ÆO²rÎ\x0014ñ/¨)þëýï\x000f\x001fÿöé¯ýkÇãø$YÞ
m\x0018Åì\x001bÞò¯7/n_þéÕOç\x0016[d\x0001 6S$A\x0008ø\x001f\x000f\x001f¿=\Ý|üíáêÇ÷?õgäú5l\x0011ÑÊPè>/0´ÿùöå»Û«Ïp½ï^¿jÀÞâ!ÂNáð8lÍ²ä\x0000h\x001f-óUZ\x$\x0018½
? ì4ûp\x0018¶à®\x0018\x001dâuÓñjS\x000b\x0015¶Ê,[íMâ\x0018a'ãã°z\x000cÚÄ&\x0018aÓã£ÓúB\x001fö lW9q\x0012¢ÔÒªõvmãÑGmÍ2ØÞîa£èÔqØ\x0010/ÂöDN\x001a/nÜ¤¯í\x0005
AØ¡Zí0µ%E KÆz¢
´%\:ã»a{UÛaVÈí2ì_¿]ýpÿþÃ÷8ÝóæÛ_ÿ\x001aqöo¥-oN£\x0004?ÞIV&üf(¿~¸¹{þü\x000eÇ|Þ¼ûé§øÓ0e{¯FSÒsõ¼)¨xiK5ò°)ÎþhÊæè£¦ìÔÑÐ¬¶À\x0016cr;6\x0005ÝfG+Ì\x001f±C×vè5vD÷R9\x001a\x0019\x00014¿
Â@¶è\x000b¤"Çm±µ-v9ÞëØ aè¥XÐ]$~\x000bÍWmQ²²EÉ5¶ Á\x000eÐw±¬+%¤g[ô\x0005ßÃ¶èú»èEß\x0005lÙ+\x0016­J¦\x0004ª	[dYo«·½[³íE\x000caYõ"Ú¢hÊ\x0007Áhü\x0008ÅÕ[ß-ÚúHi-!¿\x0008 \x0011'ü.ëÃ\x0012ÕÉ¢Ä£EXû=o\x0017GÜH>¨PNÉG°ÄÖ¬Ù,HéB\x0001Y#0dK4\x0015âÆ_º[bìÅó^Û\x0004\x0006ãí2ñ\x0003^ÿñ­W>=\x001b\x001a6ÔúEb¬ò<ÿ}©4Ñÿã?¿;«EO7~oD,ýqÈ^3ÉAÐåÒ¦-W´½Ð¦0\x0004yã{AÈîå dlî¦¹"-Ò6÷Á\x0008¹HuBÖ_è	Ç°a¬)÷ÿç$µ»@\x000c0\x0004ySªAÈF\x001el\x001c±Å¤Ç)Ï<¡\x001eÊ*7àNÈÛx\Ú}p\x001c²\x0006\x000e\x001e1öe6Øè!a»£¥\x001aC\¹²pe-QH>#.3g»ñ6¼h}\x0005ÙO@¹¥¥19%y\x0008Q\x0001\x000fõÙ\x000b#´C·yuD\x000cæ8bá±ª\x0011ëò®ã¥,¼(^ÊÃqOFÞ@>H,sàÖ*É\x0005É\x0011È»{U:Hv÷ªqÌÜt¢\x0003
{Â¬8`\êT\x001dÃlkÌö8fKû\x000fYÏFP\x0003×þL³dÙ\x0019jÌ\x0013¾áuSë¬É7Tq\x000b¢mCuí\x001azÂ5,ËRpûBågZæ\x000býHcë¼H\x001fO\x0015\\x000fX\x001aÈ¯\x001d¡\x001c&æ\x0002Áä\x0010ämÀ A6â8d\x0013®
{3+YDÌ7_Pg\x001bÂìêev\x0013Ë¬m	ÎO\x0005û²¹@9\x0006¸Þ~\x0013I\x0006Ê=qÂ\x001c}9÷5FÌº`¾Ðå59ÔÙÈËÀÇÐ\x001bDI?XäïZ¨ó½dÂÞö_É?#æP6`«òÛ¹>NüÄq¢\x001c×G \x0008¾ÿIÇZÁ*Ì®Æ|üj"$0fô
&°¡ÄæEî¼ÑÄ%È Bö\x0001GÀeIè\x0004¹³åj²*ÓÐúßþòþËé1uøTÌ\x0002¹^éu\x0005ç¢z>}v§wWWÝ]>|¹ÿ|õêËO\x001fîûãþ¢xVS±,\x001eàL\x000bìµoÁ~zûææõÕ«7o^=¿i@ßÝa]u=\x0004]rMÆè¢û\x0019ã5³8zÝòï\x0011äP!Iääyã¢«­¹H\x0016ä¶UM\x001aný\x001eºõ3Ðã\x000eå2^\tÅÐÒÚÒuqAên\x0018:Tþ\x0002SþâWôÒkb¸æQ©ùJ\x0004\x000b¡
º\x000eüÂ\½¬:»Kóýg\x0000x¨ÂK
/\x001eß¦£5\x000f×@{T\x0016OW\x0017¸¼G¡ï\x0014\x0015\x0010ºÜU®a×T\x000fØ5»Ká¿Èu®¾{ÎMØwÏ¹°ã¤\x0005ûz¼Jæ{\x0008P°¯êRW»TêÉm\x001aï
Ô½¨UIµ\x0004dè\x0017\x0018ÕÇ¡«\x001aº.h|=y\x000ceãÂo«¾rÙëÃTÎ¦\x001e[¨1¦[Ü.(Ën\x0017®»15öÉð\x0018ïÄ\x000e%\x0019¸\x0019F¢\x001avh¬Ãîêêæv* \x00175¹;~\x0002Â®9K÷òB£ñ8ö:BºÉ\x0008)ø½\x0006©L¹ú#p~°7=ØñÿV	·Ä¿ÈÂ-\x0019úí·ßþø?\x001f\x001f®~üôñþ×÷½Y\x0018êÊ\x0011§³såÌ\x0008.ªHÙ¼Þ¾{v\x0002æ¯^Þüx{×À¿Å\x001aÄ¿\x000b5ñ\x0003ÍIio4º#y\x0004F ]ÉBüï þë\x001cÅïøÒ.¦ò\x0014-
6Keü\x0004\x0007\x000eà\x000fÿyÿ1LV\x0012×_Q¤\x001bêâµÒ}væ\x0008?3ÏáÇkjÆogüÀåfaÕRüP-îYÂ¯¥ÏÒ+Úbo\x0001u÷òy(°ÖÁ×Û»|Ú½»ù£ð
\{ê\x001aÜÊ`_-øf­£Ï\x0000­EÝX\x001dÿbßX3\x0003?½ÿpÿÛÇ\x0001Ö\x0018/dÈ¢«2L\x001b÷nüçÍÆÛ7W?Ý=¿yöòü´\x0003!ßfK\x0011¹sÈ½6ÜQ®\x0000\x000e¨\x0001-"¿@^:\x000e]WÐõ$t\x0005\x0004Ý18B÷\x0004\x001d­Ê\x0003Ð¡ò\x0017ó¸\x001dirÐ*|\x0001Í=Y^ÓYå¼À4
]ÊÊa¤÷Üo\x0013\x0019qß\x00054Þ)Ûì'ëÇ®kìz\x0016»ÄBGÂ®5ÉÔ¡Ë\x0018ÂÞÑ<=ÔØÃ\x001cv\x001b¨"bwEK\x0017(@zgo\x001b\x0003Ø­°\x001b;ÝS!ÛF\x001fÇUÆNÉÇãu!v¨±Ã´Ïä`Â\x000e=\x0014è\x000b·ª­ÝÝÎº;¿ [¼Ä²;\x0000oUÝìÆ\x001aÁ®kìÑÝ&âïÝÚk`ì¤­\x001b×½y\x0011\x001cÀ^\x001fLröd²¦`Gj'>T%wRh\x0018ûI&ì»Lò(vJ\x00084øÂ±	ÃLpë¶ê®M\x0018±WmÂ°Ûkà$=è\x0002ý\x0002\x0019î0t]-»Ò³ËîÑÇ\x0011»Q^o0Ê»{-ó?\x0003ØC}òd2âÚ\x001dE5Ú_=RÎ®Ãn«D,±wNa7Ôýi\x0015%sgcï­^Ý×Øý\x001cv\x0019HqÎ\x001açA.3nó©ê/±c\x001aûä©jRÖ"\x000f4±9ÏîÞÑÊß\x000f\x001dê(\x0003Q\x0006;y2r\x001f;;Ë«Þ¾¨@¯W\x001d&W]'\x0017ÏØ\x001a
À¡à6a¿@¶2]*Ôb2*ÃiÝi\x0005Û\x0008;\\x00101\x0019ÇîjìQF{NÄ\x000c
#Óº;\x001a%;u!tY\x0005}iæ\x0010tÁôSÖÊMKAÑcGÊuØMÿj3ÿ
îÔØÝ5©L¾ÐÛ®¡O¦"©ÖgèPê2;ìn]l×¦v\x00193ë2«aVY\x0014³'ìt¦BûÝoè¦ºo]âÛê®ué	&kJuÀºd²9×âv½@3t NZ±rÒ\x0002+\x0013ÕM\x000eºÔc¸ôåjO/ìÛïL{wÖ\x0004Ü\x0003ö@ \x0005¾j\x000f¬)«ZU\x000f fß§ÄW\x001fî¯~ú|ÿñø\x0003E;¿}ýüð?^tËvBü\x0017°3îTAiâf±¡'Éÿàê§×7/Æ\x001fW¯Þ½}}{õâ¼'\x0019µ«ZF£ªªå¬QÈ3\x0017hF6fÄÄ%\x000cÛd:ÊGlÚµµ M²J+¦²±ïýûZ\x0003OeªfèA£¶×Üd\x0012K¿!juÙ\x0007ëq?N\x0000·ÏA«\*o\x0003,ñ/ìæWÐ?þOï¿\ýðÇ?#âßú5prÇç>GPG\x000cã£lvh&3^Ý½¹úá6þÓgM+¶j´b÷R=cE<`®	pÐLQ	Ws¥kça3ª¡×| Â6~­±fþã·hö³Za*+Ì\x0012+°ïÞÒÇÀ\x001b£\x001e+ÍV4\x001fF­Ø\x0015\x0002¢\x0015»:À\x0015(JiÉmøApÅ\x00149X\x0016±Mn \x0019»Á\x00193´*;\x0003oÚd\x0006I) \x0019ÍìqÔMÂ
Í\x0000½Ä\x000cìdf3Ê\x0004A*Î¿$4Q3Bµ5Â­åàÜKjéÌ@.\x000f2Ã¶^Íp\x0019n\x0019\x0004P±£\x0003G!s³3ßbã¡ÑJè\x0007Í¢Úâøs\x001dÎ\\x0003}
EbFAZ~7[!«Ã/«-0\x0003°7/µ%\x001faKY\x000e¹æs,Ç_¦\x0011Hv0éb´ãìË¨\x001d>Ï·oµLdÕ6;3þøç¯Ñ÷¿\½xÿåëçû\x000fý\x0007Gé|ÒÞ21`Òû£ÖfïÐO¯o¼}}÷ôêÅÝ·¯o7Ê\x0008Xb\x0004¶/\x0011:P1<\x001aAtÌ6úY;P\x0018M´;#ROí´\x0015\x0010SuG]\X±Ê|PñþËMâÓ\x00151	I)úF:$°å»\x0018ñìþ/ß?|¸ºùK"Píµ ®\x000b\x001ev©
0n	0ØFð\x0008fü ­dêÙÍ\x000f¯ïn_Ýü8T\x001b\x0006Ê\x00003kÃá\x0012ÒÊvÎæ{­Ç\x0017!Âïßcø·	GÄ¿\x001bp<?æ>R¯èáÜáñ\x0018ÌO+
°7\x0000Â´\x0001V\x0011XÜµy\x001eÝCé#¾I4\x0006ÇB)*\x0016Ê£ð³×güTtÆr-0þæ\x000e\x001eÂbû
,Í´\x0001xy \x0003L j\x0015ÓJ×$j\x0019¿ãÕCø;^½£ðãi¦,ÁW´þ>\x0008Þ¿¶Ét8fÀÖ\x0007\x0003¨6@­\x001ahÐÊûÂä,m3å\x001e´\x0000j\x000b`Ú\x0002áëÀ!i>\x0003°»,ÐÍ\x0001N\x000btp©´±UÏb:¦+\x0012Àgüóc<ï?`%íÙý·\x000f\x001fºôTjÒ`5\x000f£\x0018Át\x001e
Ú0ï®°)9ÃXC{vóîùó³\x0003Íl¬«QzN±×éT\x000c{ªöÆ>`©l1Ël¹TlKæ
A>ª%¶²Ä.³Ä0\x0010\x0016m4\x001b\x0003lË\x0005ñ°ã¶øÊ\x0016¿Ð\x0016Å¶8.yÄ½N\x0013DÊ\x000eNÃQclåbvijÐXø°l+Æ´\x001fÇqÕqë¾`VoÀ\x0017\x000eö2\x001d8\x000eúßac 2\x0006\x00052Ç¹o4\x0006½Kùv»Ù¸1¾:bü²#F\x0019ªh¬  ÌÙvA´á¸)ÕñËvHC\x0018ÙÉ\x0002¿\x0005è2¯<ýGlQ-jÙgÑÔÁ\x001bm\x0011Ø?\x000bæ\x0015ê)º2E/û,¦5`ï¡Ï"xïféó1ÕÞ÷ëö¾âÌ\x0012¬eZ\x0019# \x0004²æëß\x0001c Ê°,*\x000b{MqÌ\x0005.j6Eö\x000cÐ\x0001Sªï\x0002Ë¾KLÈ\x0014eÊ °2ef×M²¾#ÆÊ°ì»\x0018L1¾¼@ifÿ_Æ=ÂÑ\x001fª¨\x001cÖEeEü\x0011ñËÈBÕ\x000c|Ô²hzØjÇu;fc\x0002Ç\x0012Ó°1=tùÆÈÝB4FÖ\æSFr¥\x0002i\x000fJº\HÔÚ\x0013.\x0007	µ1«6
jÒ)=\x0001üet\x0011\x0017Òë\x0003ó 5\x0019#WÝÊPHj¨:>l2åÓ<5¾¶fÕ®Ak.\x001a\x0007OÉ\x0018ÉDH:¿ÞÚÏä:?ó¸ï³1Ë\x0018H½ÊÖèõÁyÇ6¬Që\x001cÍbYI6)8{Óº=Á1n®\x0012Í=ßí¬1¦H^Å|\x0018¢tQ¼2pÉÜ±Ê&cÌ²ÙNvLK&ÑÁpPÈ÷×_gd]/Ë
f2("\x001eKüëÆÑ§q\x001a¼=^vÀ:\x0006u1@à\x001c.\x001bM	7EË¡Éÿ{À\x001a¨=
Vy\x0004Wbw¬¨}á\x0013\x000fm
\x0003ÖÔ\x0006Ë<
EÙrÝôóM×n\x001f·&Ôß&¬û6Ñ\x0004\x000eÂ¸\x0013O3ªG<gØú´	ËN\x001b¯®IÄ\x0017µ É"X­zôÌ\x0006mQ¶ú2Ê.û2Þo
³
ñÉ¬±n}FÕÅfµ¬Ú,q~¬ÑÉ[µå×\x0019cÛÃm\x0007¬qµ5nÙ·af\x0016x)\x00068æR2®=ï6nM]¡UËJ´\x0012ÕH.\x001dE(\x0013°®\x0008½?§ÕEZµ¬J+]a¬E\x001a}O·N~5î\x0011ªª.mªeµMé$)ñ&ioNÒ\x000c+$\x0019×¦\x0000:`¯­YvOsyõ,¢ÝD³\x001faÛ@ým`Ù·Á7\x0000r4¤P!c¸Ç`?ÃzcêO³¬T+ã÷ÐttºÀ÷4ÃI
6Ü¯7¦®\x0008ªe%Ai-óTâ\x0010¢£j\x001b&´	m\x000eØR\x001f5aÙQc¡ì\x0019df/ã, 4;MÆÑuÙI¯+;\x0019ª¡\x0019ÔE
$QWb³\x0015íyÇqcTµeðç*cÊä\x0014Êð	0¢\x001e¡J£ë¾\x0006½¬±Ajþ.Ry¤:ÉÆ\x0010GH<1\x001f!i_;_ædZ0\x0017¶É\x0019K±Iâ*tÖ>BË	Ê\x000bï­eÖä\x000f¬Añ%¶F²£µçèÆ­1¢nk\x0012Ë"3ª|äÈzêÎ<Oç¬ocT\x0001àÏEÖH¦\x001f3J\x0008î\x0007±ò\x0019tË­ÑUGÑ«Z\x0002¤\x0012\x0002($S3ümÈ\x0018ù\x0008AÀØúÓØUF\x0004àé´Ä\x0013g\x0005Ü\x0014àtSÀç5¡þ4aÙ§A=\x001fr´x½ñ¤ÚÂ<wÎµurXS°îÛÄoÏÊ&\x0012d
N¨5Ð\x0018`ë\x0016Z»¬V½¶Ä.P &\x0019ã¸YÓ6õÁ¸1¦ú4Ö,û4^òì9²Ó¡)Ëï^´ù\x000eX\x0003µ5«6\x0004¢\x0013\x0010\x000f\x001ej¤Uy­4vYF8À¶Æd\x000b6\x0005X¤	¬×ð\x0018nV5ì²²ÀB\x0000Ù¢O/\x0014\x001fÓê\x0011|Ì»ÚU÷3á,\x0017ÏbÌÍÊ°®o³\x000c\x001b\x0013ó½1øsÝwq$ð/5\x0014Ì\x000cÏ\x0003x§×¿;9UµàÏEÖ\x0018G/5&ÞÐ®\x001dYÃ4MÎÇ0ÆÕÆ,«\x00038ÍZ3ÆBwç-ÐÐHëtu©qzÕ¥FäÙîägP\x001aéâìÌ?F4sõK[öRb*kêhb)@¾>z¾\x0000wÒI¿¬^h~{»ÆòKºÂæl\x0010ë¿¯»iü²n\x001a!²3ã\x0005FHêÈÆØ6/÷¸1ªî?WnÏ>D\x0013b@\x000c\x0007¬Éã'`\x001eáÕÉ×sA~Ù`@Î0Ú5 v<à$2YãÔúÓ×©¦_j
gz«4\x00124\x001b\x0003pÝÄæ½1n\x0005Gå@\x0013¯ÑI\x001f¸\x000eü#4¡úúÑÉ¯ztò!:\x0017½ÕZÍ<\x001c<¬\x001cDS\x0016þ)u{_ÕÞ\x0010÷?O:\x0018k,ßg¤åY Û¤ÂÃÖ@lÂªd3y¦=£-óIÏ{&&·È\x0001kdµg@®ÍÚ6
YÐÍY·Íð\x0008\x0019
Ô¥@XU
Æ\x0004ìNÆPQCZ>6\x001fÇ\x0018]\x001b³è²\x0019³|Öò66~$ºÔHÍ=¨Á´	~\x000fXckkÅxð\x001bÚ5P¨Ü
Ñ\x000bÑH\x0003u½	VÕbh\x0004"q56\x0014^Þ2î1Ü¬Î\x0000`U\x0006\x0010÷¾&/\x000b²¨Ü\x001bNg{\x0006T¨§\x0003aÕx`ü.µã}¼X£y@06£æ\x0001kê=³êEÐ\x0007äÉ^æ$p;­<\x0016à\x0011\x0012gðõð_t¥ñØßL­t\x000eÛµH¹\x0015crâä\x0012m	÷\x0003ÖªH?Wy+ß\x0006ÛÐ-\x0007\x0001þ6¡­X5lM\x0010U&EU\x001aÔ>¡9#PC*ê×òi\x0008v¹5²\x0002A.\x0002¹.[\x0003EÍ[1áfbVYnªÊ4A-*ÓDkÂ8'6F\x0001Þ7Q¦	ªþ6jÝ·Ñ\¦A\x0012#CûF²âMuû\x0003ÖÔhaÕ#Z"\x0013Í´pØ:[ø\x0012%5;Çoó\x0008³õ¡&¢	«h|ÐÀ=\x001b\x000eû\x001cÉÓð>CÖ¨G°¦.oUåÍ$ÐN\x001a\x0007ºdÂó·ÑõÖÔïhaÕ;ZÒl×ùæð\x001dI\x0015G\x0001û\x0008´'¡\x001eß\x0008«Æ7<\x0004ËÖx+p+ÓS+æ§~:\x0013t%@Í\x0001{1Ég[Í	\x000eQñ\x000cå¶\x001ax\x001b¡NÂwµeFI×ùC\x0019½Í§\x0005æ\x0000ÙdÍ;T>µ	Ñ«lò!\x0000w\x000bXa·B¡±\õl*\x0018eD¢OÞ\x0006¼ã_<9U?øåÃÃç_º÷u$`|(\x000fRõ\x000cåÐ3ÁóÛ§Ïo_?m±ñ¢\x0019òÌzÔ\x000e<GY;i\x0002
â1
ôHþÙgÈöÚ{ì\x0018þ \x0008Ð\x000ch\x0016Ã
b#I\x000f#¯P¨Ê3Ú¨!N]4DsHmÌ\x0004=Cw\x001a\x0002!g*\x001cxëh³[)\x000cO\x0006I5AoôHRÓgÈn¢!ç²Ía×²\x001fç6Èµ \x000c@ã¥Ï\x0010[¹]åZL£!ä¢!L2®\x0012ÃÂbC*×²k\\x000b¿\x0008½\x0004 ¹¤è«8ü*å\x0006\x000eÇ>C|\x0015~Ïu6
\x001b¢yð\x0004 `6G-jÒòJ\Êú\x000cj\x001bÚ\x001e5$\x0004zÎ\x000cª\x0014e\x0004Ó6øø=ïu¨¶\x0008,Ú"Àm\x0006ÕC\x001cË·XÞ"C
MÊ3²á½.¯!\x001fì(æ\x0002ôE4qÏyÕ!>jH¨¾È¹fæ\x0003PYØé\x0002iV7RmúâQC¤¨¶\x0008þ\ã[('LºTÒf·¬Þ6Òûßi«í8Sµ<ðE%;\x0014\x000f3\x000bÍ7båõêè»#ÏIk÷\x0019Î~\x0003ß,HàJÅ\x0018qf%ªÚíò\óâðA¢ø
EXIu£l	ðæôY¢O.$«n$Ì5g\x0002\x0018~{\x0011<åµ\x001a!gê´\x0004jK\x0016e)ÆsdQØ\x0012Ö\x0016Ö#<s}Ôi£\7ÚÒFZ
|(jNµX~%AÚº½%nÕ6)ªGøü*xð©¨EXn¯-ñ,1»<;g\¡H¢&n·ðNK|mÉ«QK´#\x001av\x001bw"K&RÞlY}.*Q\x0019¢Ä"C£nK\x001bÑù\x000eõÍ´\x001b¼î3ääâ¾èæòlÙ·,r¯° ¤ä\x000fâìêM¢Lu¨sý"Ã_DÐ\x000c\x0015ñÂëH<¨dó:¼àõYâle;Ó0ZL	\x0004s­gIîK`K1euÆ¥ê°¥V-É¯÷VÄ\x0005èå°\x0005ËsG\x0015jß:78úE¼¡Ê©5ì%>^\x001eµª,ÑçæG-q8d­DýØ¬*\x001dxß\x001b»<ãÒuî¨\x0017åhË\x0014¡L4RGãFÞLú\x000c1U1[ã'\x001c5Ä8dMXIÃ;\x0010ï¼ÝýÈ\x0013j§%P[²¨
ì<i\x0013Äo¢©2~\x0013®\x000c¶úÙ°%¶v®s3âÃßDpèBÊ¨Ì´\x000e1vñ6à>Kê,X/Ê}<\x000b=íFzªÌ\x0017%VÓV\x0014\x001b¶ÄWÇâYòQK\x0014Ð\¨w<\x0000±Ýx+\x001fº.×éEõ:Û°g}\x0005@y\ú&A-\x000fÂ¡þ&çÆ\x000e¿Iºë&Kø:\x0012ÏÎ\x0015]nyè
®6dM+mx
Â\x0010¨¨\x001d0µ\x001bGçZþîcêYt3ñÒrBTþt0ãþ"«\x0013#kKÎqwZ",\x001fH\x0016\x001f(\x0008[®©X=B\x0005Ñ[
Þ7EpEø\SÄðÃ	«\x0011\x0010/ÜëK-uD¥eÖx;ècÞ%w\x0007ý³O{ørõìÛ¿|ø½[õ\x0017\x000cÉ¨¹àØ\x0002ç>hû
ëÙí«×Ïnß\={÷?_Þ¾8¯øk²@å¾¬mì6;Bÿðï¿¼ÿøð¥wýU<\x0000óx¶Ñ¡²ª\x0015ÈÂ.Tþ\x0011?ÿOï^Þ¾i ×v|?ãq\x0004º5$\x000bj@_\x0007FÎT¢cî¶\x001fùþ^Ê\x001eC\x000eTw¾\x0011óCB\x001eH8´_túÛÊYì¤·XKsNÚXMf\x00119iùÚÐAHÙ\x000fÝUÞâf½Å_\x001bB®ò(09C\x0001ÞLºKQ\x0001ÇSÈÉ \x0007\x0018#\x0015Ié\x0000ò\x0000\x0012vm×-ºÜºÉ\x0013ö}7ù¡UO£}	»PôÀ¿mR\x001bk¦Ú\x0003Øe]N®»%J,­}\x0002L0\x0005{[Â¨\x001f»6\x0015vm&±sî¦ã\x0019Ocäï\x0004]Ënêe7³Ëîña¡g¶+\v(Ø\x0017.;@}¯u\x0008{\x0011VÑ¥}\x0002µ\x0016\x0008{\x000cë¶ªÕº+9¹î¨
¾ÃÎîN©%b_	¨:Ì¨\x0005aÆÒV\x0015¥<\x001c³\x0018Æ®\x001aí\x0003Ø¡
ï
fÃ»Åæ@Ä®p\x001aC$\x001f­\x000fr%v¨±Oú»õ4ª\x0015\x0007Q>à\x0019z\x0007\x0011úÈ©ZßCòÉº¿\x001cô\x001cO\x0007ÖÅ\x0002 @\x001bìh£RF³ñ\x0004Ç¿xrB\x0013üùÓ·¿?\½Wû½7\x000f¡enÖ;\x0001¹\x0011ÐÅTÏÛëWï~¾½z\x0011/!7/\x001b\x0016ìXeO\x000fY`<÷ X$\x0003Ê\x0006Ä«\x0014S4t\x0011iX *\x000bÔoÀMñ\x001bHÔ\x0008ÎäLg»è³\x0007,ØXÑ\x0013RãC\x00168ÃlÖ\x0016i£¸5è
\x001bhj©	»[ªo%M(MYV\x0007n.×âG]o\x001f\x0003&øê+ø\x0005_\x0001WB!ðLÁªÊWèM\x001a0aw\x0018D\x0013N´? â\x001f\x001d	AÎP\x001ciñn\x000eUD
ó\x0011U@sGÖË¢ò-éëîÒöè·`'&Î\x00131Éc_! W|þ
ö\x0008É\x0002KÇ\x0004µ8¤J\x0001µ	ó$g*B\x0004\x001eü\x0019Tq¤.\x0002ß\x0001\x001bT}4«\x0005¤
ÕjÅ	=\x0016Va¦KüëÅ6ÔßA-ø\x000e(¯ìh;\x0008ÆÑÜë\x001a·ÃâÏ`êÝ`æw4î5ÑÀbñBÀÇ³é\x0012Qé²A'­ÛÝã~\°ÝÛþ\x001e>~~õüþã×\x000f¿wOBêxQí"b
'\x001b}\x0003Ñæ\x0016ùÓíË×wñ½|{ûüÅùyÁ\x0004_nsÑ\x0008_îæ¢\x000fâ\x0019È\x0017\x001c\x0007À\oñ|\x0008\ _?ÔøÃ,~«©÷\x0008¯\x000bÌXkY/Yºæ»÷\x0010üÝK1Âß½\x0014\x001f\x000f4õ¤½Èá\x0007:Ñ¤o 
áßDj\x0012þHÍAüXÊ¢å·\x00021áÇ&û\x001fâW»ó8âW»óø8~v¸þDB\x0017\x000bÏë\x000f­b\x000c¿¯ñûiüã3	¿sL>mÞTf\x0015t\x0008¾¬áËiø1ægÕ\x0019ì¾ãfN\x001bø\x0014V²Ù"1_×øõ4þ rO\x00172fáY^\x0017%q±)Õdû\x0019B_Ç~5\x001fû=ðÛ÷ópSpô°tõ\x001dTø\x001dLâO<Ø¤b\x001ec¿ÈcdÎ0Ûj³ÇõâqQ
ûqÑ\x000cÿÅý×÷_¾tó
xTf]/IÙ\x001bx`&?+Ò«\x0019ý·woÞ´Àï:"x8
£àã\x001d\x0018X.Î\x0010§"á»¤	ÍÚÖ\x0000x¹ë-à¥:ÍÚFÑow0\zAè£¾9ý=>\x0006±=zü9\x001e1ÂeH\x0005Ò^sIËêæÛz\x001fz¯O¦½ãI¿ÚùûW7ï¹ÿük/t'S\x0016¡;\x001a%ä¸xAAsÂå_no^^ÝÜ=½yýãeÜR»=nü9\x0001Ü\x001aC\x0013«\x000e	ÒóX!xIÔ4 |s¸\x001b¹Ú\x0010¹Ú19\x001d@\x001eÃ$QkÅ%·4è\x0005VÒ#/hÑÔtèG\x001ejäa\x000e¹Id­	9,I	Æ$%´5ºqë~\x001eqë\x001dýü!Ü¬Ô\x0010q'¶\x000c\ëf§\x001fx¨9àóâÿa(¸ù8éBsØ©\x001b¸q§\x00187å)Ê\x0005zvñJÃÝÏ¨<æ´C?ð\x0000\x0015ð\x0000sÀ\x0015U\x000f\x001c¶£RËfÖh@EUÈí®z|W½9<F\x0003!/aE9bîÍn³
ùFïèÓ¬¹\x0010¹3-^NÓ\x0004V\x0002\x001e\x001c/¹jN/\x000c\x0000·5p;µäAQ\x0017v¼:ê]V@ÂÖ\x0011øºèL\x0005Ü9àZ\x0012¯[¼Ði«R\/\x0006Ó|ÿï\x0006îe\x0015W¼+\x0002&r\x001dêîQ(\x001dÉUiÓ\x001du#Ç\x0001\x001dò4¯1\\x0001\x001dr\\x0011FtÀ¦ ëÈ¡_=ýÓÁ¿{ú?â2Hu'\x000e\x0012e¢ðBu½è<M©ð!\x0003¾¦~âÊ\x0000ü«ø¨HM\x0013u3yø#ÞHuIuW|Iä¶, 'u\x000eðñáê×ÿúÿ¼\x0019°ôN¨\x0015$³\x0001²\x0001çûÖ]\x0011òåíÕW7\x0017\x001a¾3ö]¯QÀqçið¦	t\x0010êÙ\x0008.¦Úv­{'øM--¼\x0005\x001fLî·×\x0001È|Ë\x0000ÉÕl\x001d4,#àC\x0005>Ì¬ ­\x0003ÊÛ\x0000Ü9ís\x001c\x0003à¡r\x001bv\x001bç¸C\x0001¥|¨¯\x0011¬¦1j\x001døý«r\x0010Õ«ò1ô.xî
¹[$-½cmH#»n§èeåôøs\x0012=ðØµ\x000e½çPémQ×ÍÞÆ\x0001ô»R\x0012¢ß®½#5[\x001d¬ )K\x0014\x0015Ò¼g"Ð\x0003èu½öz:â Ï.UÂ#B\x001bÀW5Zû¦8Ò\x0000ø]RàOÊccÉq¼EÊÓì8Á·;£\x0006ÐÛzéí´Û{à.
!YÙ\x001d¼a\x0012]ì¸[~wßFô'÷í#èS/îY®ÍxÃº-k·¬\x000b5öÙÊ¹"§\x001d\x0012s^s;\x001a6\x0017­Cïë`ïg½·üäg\x0004ÊgÓQeªÐ|7\x0018@\x000fõÚÃôÚ{Éý\x0002Û\x0014­=\x0011êÄµoRÿõ£ßWÞ1¹Ó\x0007­ÕLlR¹Þl$7®{U'zUíY¥¦÷,
\x0015ßkKÍ\x0006S´öÞ-D¯«KÉþ­õèÚ\x000bZx\x0016$\x000b¯=/|Óz\x0000z\x001d,Õ|°4²¼ØBÊ\x001e{3ú¶ÔÝ\x0008zW£>¨´æJ
ÅuaW®TV/Ìp\x0014Ôk\x000fÓk\x001f=ð\x0011=åg1"úæ#}?z]_Kôü½Ä\x0000è\x00017à\x0003(\x001e\x0000V¡É8t\x0015¯
9ù:~RÇ9r©u4Û	Ø-ACñÛ×µYr§µÖ×ó\x0003ñ/öó\x0003Ïÿøç§W?üñÏ\x0008ð·þáq­\x0012#AÀF¥ªÜb`q\x0002§[IÚóÛW/¯~¸ÿäÙùáq¿u\x0018 ü]ÁAø
)\x0005i\x0006,wmÔ°YÉ\x0019Aïô\x001e½ÓÓèÿ?CLL\x001b\x0008<k7ÛÐÌ\x0007ÀKQy\x0014Ó®£hÖÐÄË9·\x0017³¬
®9k8\x0004^×àç^kóÄ¥÷¬ðQFMS\x000cc\x0008¿¯ñûiü\x0012H'7â\x000f¥5Ú\x0013w¹E:Çø«ð+7_"YE\x000e;BSõ8þ{]&âLt#ð·\x0004×pp\x0018~ ç\x0018w'ß´u<\x0015o¡uè\x000eá\x001aÿtÜÑç©-Ô*­sØ×JsÜ\x000c+·¯ªÝ_Í»?N7hò\x001f$âð'£>ñf´pý¬Ü_Éy÷·,\x0006¡­\x0007Æ¯\x0005×ÅÒð£T\x0015>\x000eØ?ÛÐç\x0011GÄ\x0018¿j6:]ûÄÏ¯]ævø\x00083\x001cEq:\x0003â)Æü3º9è3æF§f +Íñÿ7å9âÝn°ON7Ãýç_¯n>¼ÿÖû\x001cùú"\x0015ë»h\x001ewV\x001eOºyÙóËwg\x0012	¼=x\x0007³à%ÖK#uàüÙ¸rw4Í!øÛ\x0016Âß½i\x001d¯%U÷#~è	¿\x0006¾¹ë&ÍÚ\x0010þà÷øÆï$7\x0019Kã±!á÷\x000bV8ð¶\x000eÿä%ù¾Ó\x0006`§K.à6&z\x0013,\x0000Ûµw»
0ÿïùÇ\x001a\x0010S!þ\x0002¶\x0008RXU*W¶)¥=dU\x0001VÍ\x001a à)Cé$ëæZ+¸ÒÖ8\x00193ÀÖ\x0006Øù/àQ4\x001a \x0003ÎòdÄß*@\x000cá\x000fºÂ\x001fôô\x00070©l\x001dk4e\x0012\x000fdö ozÐ&
0ó\x0006ÄÈ_,$j|;\x001eRâõ&ÍT'~ÉÁ·\x000fà\x001c|O\x0007wõáþêùû¿ \x001bâ×÷zÇT½\x000fÀQÈÄý,=\x001fGX\x0005\x0000ÍwÒ\x001f£\x00157WÏïb\x0012qóöîÕÙ1Õlbo\x0004þ6"&\x0012el[Z¦û*m=¡oÈí±:Ù Ý\x0002\x001b\x0004Û\x001a«=ÛB0lZmÃî<@\x001böÄÓÇm0Äé\x0013¿-\x0014\x0000mþ¯!#BíLa3mjêBR3j°<¼\x0014|9{È\x0006+*g²b3Å«½%
uev0x.®Ð,R\x000cÚ «ÈdåÈ\x0004Ò\+RÁBi\
¡-d9fÄ.ÅC#*\x001e¿Ã\x001fB!|2Â\x000fÁb\x0005B6ãGM0µ	f	?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=:{1»¿:p\x0003ç©\x0016\x000e\x0005º\x001f-7?!\x0002²Á\x001e«%\x0003_Î\x0012\x001aªbfw£8sbrï·¢
¢Z4Ç¦\x0013 iÊjXAºrØc\x0000màOTo6KN\x000fò\x0013y³ñSw\x001eï¾\x000cN=üþ>ü>w\x0012î\x0001l>à±^åÎ¿\x0008'ÒqÀ+vÆ0sßó\x0002æb\x000eÒÄþßd5ß¯hhMÎ/;h½
\x0016£\x0001ibãïA$\x0000\x0011\x0016Êd\x0017Å[~swZÎm­J¤
¿\x0007)ÈlVq\x001a8Nx>6¹íT	4°ôûÀ«Ì
°F*Ià%"Ï/²Îh·\x000eiâäíûl*çç`Às§(Ù\x001bW6·[4pÖ+VIÑt\x000eÕs®\x001dÊ\x0013³fåæ\x001eøã\x0015HBU:\x0015È"\x0013d6]/¹\x0004iàrW iGù\x0002krc)z³\x001b\x0010æÎÝÌuD#¯ºf{ÃH\x0016ÀïF"3h\x0001Ä:;ÉÉ¿¦URy
¶\x0016ô&k Z]·½GÎ|Íþ¶Y&\x0018­à·h\x001fË}bVZJ®Éha22\x0019Hdò¶TLIÅß.Ä¸\x0012MßÎgmq´\x0003íw\x0010Å4Y½r¨>¤É*jÎT\x0016\x0002Eúv¦PY¿Ãí¬d"Í&&ªóDS\x0010©ã¬Ë´Ò§Á\x001aöÒbÂ ç½\x0018¸\x001cÖ§Ák²a£uÂxÚNXyG[ÜpRÂë¤äk\x001b\x0013x(VÑv²%Ïç4;\x00041,1Ww_0\x0013ÞîãÁ»\x0014]}½þû¿wT
@\x0014\x0013ó\x0018¨IR\x0005üq-¨(6È©XáòàÅéù\x0014\x001dÿ\x0004±él¹@\x0007²ïÿ¶AÊË\x0011\x0012V0Ç\x000cZR«\x0011¶cLØ­E}¸\x0005ÒG|(	\x0019RÅl5 ²!
/\x001b ê¸¬\x0017Qöä6J\x001frë\x000f.¥J-y)þ¢ \x0002ÖRM\x001cÚE}Ï¹q-UÖC\x0003JIÕy\x0018Àf
`XK7e\x0017Qöé6Ê óDj 4Ie6SÒ\x001d\x000fgG«'¢ìû×+¸qY5­¥£l\x0000xS\x0011÷"Ê¾ËÝFéä!p\x0015Jßñð<\x0015dß	o,¯1æeR9^Ê©\x001bo	åÐ1oÃÄîôòÁmÎçÉ(\x000båT*c\x0011åÀWo\Lê:Bÿ,còg¡ñ§²C÷½
\x0013â\x001dAÔ
\x0019SR4©¶§ZÌCßD\x0019,Ëb¨\x0010ò&EÊò¸\x0011m|ªÅ\x001cøøm!ð\4T2iqJ\x0019y\x001b8Áä0\x0007n\x001b&ÙàjbAIÈ/
\x0014}|²o>\x0008\x0004Ú(]~ÇÅòPÒ'ç\\x001cÜNOäºq\x0019û"JOO0¸xIò£|à¥\x0014\x0013yE\x0008¦ùS®\x0015"\x0004¶%
Æ<a§²ûekïm¹R;hËëÛ%oKõDîÆ0ðj\x0004\x000f]\x0006ZJË,Þ»üÅÌb\x000ec±6L¸Ë©Y\x0000§
\ÏÇÇL%ê1¯?|ùí½|@\x0015×»Oog#FZ\x0018øPè&¥\x000c¸-)ÃæPê|*\D
×ó3\x0012Î=áKÄ~\x001e­³
hðË£¶zB2t¾yÈz¤áKÄ~$ð\x0017sßð`VrÇ¹ÇvF©ª
Òð%b/4Q0ª²¯`§ÌtÖ¨hø\x0014Q±H¹ê\x001a¿¤}\x0014èi\x00045$'Ó\x000eõ<Ãwý+ä¨§;É\x0002Þc´p\x0010ë:¤á;Ä^$áøU\x001e³ÈÉ\x0008`õ#©ÁO¦ê¯\x0010û×\x0008n¢U\x0013\x001eåóY\x000bE\x0019ND¿ò¬
_!ö¯açR8lÌÄ¢f\x0016æº¯6~Ød>þïk`²¬<(Ò¬5L£gýL\x0010¸&m\x0007\x001cþ\x0010\x000emÞÝò?°Lf2]4zØbAùÀ9\x001b¸\x0011.S\x0011\x0004äÉW¶z¦Ñ+Ä~&\x0011H#\x000fgdäº	X&\x0013©\x0010&®E\x001a=BìGÂçuÚLt\x001dRo\x0008o¦)ï¯\x0005iô\x0006±\x000f	væ"&Øì6Si©Á­»ßN}
\x000b¹p\x001dÅø\x000c\x0015¤Á\x001fsq}ôoí{6¿ý\x0002AËt	Ú÷w·\x000f_êñëÕýÃ\x000egN¢àDÖúÄ6Ál\x000e¢¤¦\x0016\x001f§«¾??{ó\x001að.:¾ÉÙC\x001c×#Jz¨	à©¤ÞPLé¬öSæa\x0001â¨d®\x0016QáFËÚè^\x0015Ý\x000eË«¨ìÔ[8ªõ®^EÿÌMJù"wâ(1\x000cVd\x0015âïòáÓÛ·sNû\x000fû÷8\x001evö¤æ§ì\x0001\x001ae\x000e]6mZs_ÐÓWpB~8ºø\x000eÇÂî\x0007ðÞ÷Á\x0001 ®m°ø^Èa1YðË\x000f\x001b\x000f\x0016pM¸ðû\x0017,8¾2
Èe.íØÊ\x0005­ç,o=Ø#¿\x001f\x000c\x001b5²©oF\x000fØ]D>WÓuEM`\x0013þü^0ì ¡\x0005Ã1ÎKsÔ
\x000bö\x0004\\x0013Nô~.ø|åKZ*^÷¥7,¨0w]ÕsM8®û¹<ÍJÄ\x0005STDç7e­Åô\x0014÷rEI?"éTÓUªH\x001a\x0003ÖkØ¸T\x000bfoÿ¼ûöyú:ýáú~óø~×Ã£\·Æñ¶3¹Þ(¨a\x0003\x0002\x0019×\x001fN..¿3ª\x001d¢Ñí¹('6\x0011\x001e.1Ç\x0019H\x000b\x0018¥Æ§Üü\x0006¢Ñe¹\x0008GîZZ#+³Z\x0002 iê	2©±\x0001it9îEX:\x0017pk\x0003³ùBxò¨áÖÜL
H£r÷½H¨ÞF«Äré=?\¯\x000fs	Ò¨i/´´T(äÂ\x000b"Òr2=Ó@4jXÚGäQÞÓ"T~û\x0001\x001d/Ò¤»Ð4êIÚ¿HÙmÁU2µäU¢ò\x0000Ø`+·Ò¨íhÿî\x0016äòi\x0014*H\±\x00007Ë´o_42àuË`AD\x0018ñ¹ww¯\x0013z	Ò0¬®ØLXù\x0011
Iè.¥Ýé\x0001]Mf\x001a!l
QHÂ\x0019Hd(kýTO\x001fnÝ\x001b°\x0015LZý­#úÑiËL\x0015µ
L÷ªÍ$óÌ\x0018ÜLá\x000c£2:°Þ%kõH¬¦Ôd\x0004=Úi°¤"#ÙI·¼\x0001DZ<'üÁ2Q¡?î&
aÀ,\x0014m`"õ¤\x0016&|u'3³Ói³d8ZË%Lróå}/!NÞÜ>ì4Li,oÔxßQéG±\x0002~Ô2\x001fµ^Bt|töf?Ï°o/vy>bÄù£Y.\x000c½%JÌàÄdé^5Ð°`o/\x0010Ä)\x0016ÈSb±{V(ØéGÔj amÞ\x001e ¬\x0019¢L¶1Ò%§	¦H\x0000wû: a\x0019ÞÞ\x0015\x0008ÓåOÃ¸éìGK{:\x000b4,¸Û·@89 ×	\x0019¼k©\x0016Ð*ªPr²¤·\x0001hX[·oPû$_k^Ñ\x001fáòª\x0010§Þ\x001ax\x0005jûy,eðÿR©qöÙèN\x0018j²¨¦\x0016h\åµÿ¬å\x001eÔ6¥=Ó!£Db\x0014Á­2CãR©ýk\x0014È\x000e\x0001Q®ÓÅ5
äDâídQB5Ñ¨Ühï¹\x001a\x000eÖï3MÃlmT#õ\x001a¢¯¿_ß¾\x000b	ÌWûÍûëù"k¸ÂH3\x000eg!sÑSÔ\x001dâð
JI¼:º8úîdî.ë\x0000
\x0013û\x001c\x0019"iUùfN:zâÇù¶«\x0019Ë½@ø|ÏéM&okG\x0003uròåªg¨Ü¿@¢\x0010	\x000e\x0019w ;©\x0019\x0008\x001c¥U@Ã\x0004å^ \x001féÜãÐSªHs\\x0001ïüÌ\x000bh5Ï°à`ÿ\x0002yjW\x0016\x0013\x0012´>×G¯û^Ã<é^¨)\x000b\x000f^«Ì
3\x0016ì4)¹¹0§©\x0007\x001a\x0016\x001bì\x0005Â«¼-Î\x0010\x001cy>afº§\x001ah±Ý¿B1g·¥³y@\x001e.´¼@y*ìbq¡Á^ cId\x001cÓ#oÊ
MÕ«6\x0000rÇûÐG\x0014´ ßõ^s%VPëlÐ¸Æ`¿Qtl\x0014ñÚ\x0008Ù=sÊý\x001cê\x001c­"\x001aU\x0018ì]¢í©ÇN>½·é5®0¨&\x001a\x0015\x0018ì]£\x0010ó°j¼8DÆ¡Õ	Ó2\x0011Õ,£NÂ½«#¸\x0001\x0008l´ã¤£WäwvëVgÔHXõ½\x0014EË\x000e>8BÅ,\x0005fÑ_Ç»/SO¹\x0007¯®?\ÝÝÞî\x001cú&\x0004uzHÀH\x001b'\x0013QçµÔ~2
zuòÃñùÙÙü\x0018°\x000eÖ0®ÀÂùÝÎZ8¤*\x0007GÃ.h±\x000cêúîZüùç´×x¿¹¹»ý°c;e­þ\x0014Oë\i\x0005î2¦\x0013\x0007¯.NÏÏ~Ø\x000f4ò\x001a÷\x0001\x0019]¢!\x001fÈ@¢æ\x000e\x0007CÙâzÓ¸G44.5Iû\x0004\x0017
ÕBS	\x0006Ó¸÷ÙÔ¸DÑ¢¢\x000ff¹i-+­\x0016hä4î[ ìªÉ\x001f,¸<Ù
¤á\x00169¨\x0006\x001ay{\x0014Vêä-\x001db 4ØRDa\x001dÐÈoÜ·BeVFQSzºòå}\x000fÂÚîÞ¿Oõ\x000f§\x0007ìÍ\x001fînßÏ?`£C#jÃ2\x0017¨	f©\x0012G¨¹J£A\x0014ûÝì<ï-ØD­Ë^0QQ¾M|.¥=4.z\x001eû\x001cÝT
´k¢Öe?\x0015\x001c_ãäÔHf°÷\x0016ÌÎ×cï\x0001ûí×ûk7e¾\x001f\x000f.®ï°+b3{¥X\x0010H\x001e!ÓwtÌ\x0008\x0010éNæ!.NÎ±\x0019âhîNé@
/º
('éé\x0008¼-&@I®\x000b²q*±Þ\x00045ÌÓîÂá\x0008>3¡Ç7ÃâçÌ4e\x0015ö#=º¿ofj\x000b/îÞ^ßî\x0016&UM!\x00141ÉZwR³88,Ôô{ÖÅùó³\x001dªr\x001d¬Q=B\x0005VI\x0000
\x0015ã<AÒmÖ©ÉÐ{?øü>N\x001a­/\x0007o®îïqZ÷äL]=\?\x001c¼züc\x0016Òâó»¡®\x00160ùyy¸è@*=\x0019K½>xs|q»_'çêÍÁ«ËUð¾n3/\F>äÎ\x0000Ø2óÂmÅ
\x001dE|KqG1Í¸Ø\x000eCÍ\x001eAÐd"¯#\x0017¼Â\x0016~D\Æ;Ú¥Í¼ZbðÎÒd,¯\x0005Ý²NêÉc)ï¨¤¦\x0017ß÷ò\x001b-¬¯ÏÊ\x001dÆ\x001bL\x0000P¿ÑSâÊm×\x0019*.\x0016\x0001BÐ¬zî5ÊûPï\x0016\x000b]Æ;*Æi^^#¨^[\x0004ØÉ´\x001deÿFÙ\x0019\x0013¶wT©Ó¼¾X\x001foÔ\x001bJµÇ^ÅÒ£7]¹³wTÆÓ¼¾JS+pl³Ì\x0015Fós
]E\x000by'äc`l\x0011ÎêY\x001e\x0002]\x0006V3\x0002®ËÇEIí\x0006ØQ#®XëØ\x0000³l\x0010_\x000c<\x0016<n^aìwË\x00172¶ä©\x0003pä¨\x001eÎ%Å§\x0003\x001e×Xµ9Ë¾3CÎ\x001c\x0003+?¥º°\x0018xw\rg(*^@Í§B|gpê¤\x0000ÜRÞqÉXû\x0002\x000bdÄ\x0014Î¡×Ô\x001fÀëk'\x0015\x0019ò\x000es©K\JÁUðÑ(ºm·~[;L´.Á-ý¸Ñ\x001bRÊöøwtàÔ¤èíBà[;°Ã\x0018Îã¦oåb¹3Ì\x0013.ðHêm	¯ §¼Éegµ-ìbJ`8\x000cjp6r_ð¬8êJ98éÊ¥Àð\x000f¯Ö8|\x0004óì¦HD`áM1\x0011O¹á¼©ug\x000eü\x0004ª@Å*\\x001bc¼ô¼#ô¤nA\x0013¯ûòçù 7÷W×7³p2\x0004^M%HÑÌÀ ~\x000b;]iõæâòøät\x0006æ\x0017óñ½ÿ¥\x0003süåóÍævóþ\x0013gÿõåúËÃN	E\x0005÷\x0000qE\x001am\x0008î\x0001Ê)ß¹h_¿:=:;úîÓgÇ¯O^¿Ù!¥ØaÌQú"Æ<h1~ÍC[Qä?l·o
bÌ-££÷þ´1÷ *.5~ÂeÌÑø\x0012F	w\x0012uÞá¦©"Ò\x0004\x0013{\x0019­59\x0002_´¨è©Ë:æ¶E@5åX¯AÌQì2DOÏ¼\x00191ËÛ¨­ëÿD1Ç\x0008á.ß\x001eéÜÉA² º'AäHjÙ*FR\x0016(£¨\x0018R²ÝñO´\x001c,\x000cÔk%P 0¿Ä¤\x00197|\x0005Ú57¿}\x0010o»\x001dNÿÜ|ºÚ<âmrºy7\x0002Æ!¯4A\x0015ó'y²¦çî»Â?^\x001e\x001f]âerzôb?HÎÔü¾ '(Q¦®an\x0004ÉÛ¿\x0012\x0004\x000bàCYHÓrh\x001cÕ*\x000eNoÔ¨ü$W$kI\x0003HgEÌb\x0012:m$>æÇè¼$Ù\x0019\x0002\x0012á\x0012\x0012µ$bK\x0012Ë(#~\x000cèi¤6rÐÑ®ä°"+$b± \x0001`oLáX¾I(P\x000f"hJ¥°¹\x0016/ð&±Ý{¸2\x0003$&æÌ&\x0011\x0016\x0013$®+!ØHB1=c@úUHÂÛµ7¸ºÙêIòS\x001c{ÉÏ~¶³í	i5P^¡\x001eDÑ6¡\x001eý%ñ]A\x001a\x000fòÓû\x000fWáäÓg\x000c°äùæÝÇÍ®É_Dò\x0005\x000eWô4ùXÐ]I¿¯0BçG/þy4\x0017MuxrpPÏc±M4;a\x000e>Ë\x0017Ú®£Éq@\x0003pE3+j\x001aç\x0019ç|°ÀªÖ5@Ùéo\x0000Ò*`y¨Þ\x0004-eY¡® Ð\x0002 ìá7\x0000\x0019îÉ\x0010é:ÊUØOË+Ôµyµ@×_ùý©
sã>nn®\x001eæ[\x000cÁÎ²2Þæ¶^p­Là\x001d¢[¢]pnÜ?NßT@
vu
µe\x000c	<ïÛ\x000bTé\ÚI-PÍ]\x0003%X\x0012N\x0019ëèy\x001cE\x001eý`Cúx-P
^\x0003eôv¼ÊÝ}\x0000\x0015x\x0014ëùæ \x0006¼\x0002ÊI\x0005ÊèXVJñà\x000eë»ñë"¨ü\Ü´R(çDS2PH/ZÎ9ÞSV­Ýè9|iZ©­^µÁY^y£;É»ÖvKÉ\x0017AåP¦Í$DV¡\x0007#gØIeÀ2-P9¬iZ)¯x¶Á"9%­~´RÆ¯ÜS\x001cã´- æ\x0004e¤ìpL\x0013ØòR©¸Ò&p¼Ó´VK\x000bF· Ï<5â¡u=ET\x0014û´Y\x0005ªT\x0010Sy"\x0018\x0005ÉçOº»ã¶m\x0015\x000eùöË@'\x0014Ï\x0017\x0012få-ÃÞÛÇL-J÷¹¢o\x0017ÅJÀþwë"ùcH\x0008w\x0014OjÇ+y\x001d\x0015?Þ5QYÉ;JIÖêC¥C6k\x000f\x001f¿Ð5Aé2\x0015ÜCL\x000e5? q>àíÏ_ítØòâãßÿõ\x0000ÁÔ¬ã)°3 _~\x001a\x0002KÉ¢¿ä	ES\x0016á\x0012Þ@Dµi\x0014ºT1åj\x000c¥q¡<1\x0015.åÔB50\x0002ýL.ä7\x0016¥\x0015¸êT&Ð[Õí¦Z4
aö#¢ù\x0006\x0010¹¤\x00127dÒ¤]É4bö3EAu)i;Qi`0^í´iàßU1q\x000f\x001c0i\x0016
¶¸çÒ.ÙNâêöÛ?ç«»yKàT\x000cÊ\x00044ï3àÐV*È7³×ðéù¬\x001dè\x0000M\x0004V»bÈZäÀc9-Ë¿¨a;\x0017*ÔáLT»q¢lTÑ9ê¢<ê-«&Â©Ý@AÑÓ TÎpÖK¢òký\P\x00074\x0011Jí\x0006rtÁI´¿P;g£:fõ<\x0013QÔ/\x0016iô°TèÃ)Ê\x0005òaÝ\x0002MDP»<k}K-\x0005©vRN6Æu+4\x0011=í\x0001òô \x0007{:RQ:\x0000±DÁ²=ýëïl>lfîþ»ë·÷×³þ@\x0019×\x0004ÚÆÙs\x000bUãaMîi0ç§'Ï/Nö\x0013oÙ
"Cç^\x0007³È3\x0011L3ÔµDã\x000bm/¥<ªTÚj[Àa	ôÕ¤N\x0014îFúùË½wwGª2\x0002:\ëm­¢ÞnëÍtr BÄµC6´IudÞq±=æ-´§2.Éò²zÒlD\x001bZ:4pÜ\®0Q\x001ef7`ûr\x0011flf\x001bÙÐ,Ô\x0019[$©).dóÓ[pfé÷÷Ùö\x000fpÇ\x001dÝÜ\e»õãÝío×ð·óÆK;÷[ØNÆKXEgáÿ¿c+NO³éúñüì?.Oàog
*ã©.jÅÃ
ü
ç<á xàÕÆuxº§[ñ¼É\x00151¸z4Ð\x0003*\x001fðêu?à.iÅS¶àIVÆñ¼WÏËux¶g[ñ0Óß¥£4§ÛÇXööq\x001dëâ¹V<; \x0010Ï8ö¢Jq«}W`	ïâùæÕËÅôq\x0015í=J\x001aÁ·u+\x000fnèÒV:0|L\x0017l\x0004\x0001:Mº\x0012ÖHµrëÅ.^\p2\x000c}[å¸4\x0003þKyëÙ¸nëÉ¾Un6Ë\x0000\x0015\x001d\x0019ÈNn6\x0002yï­\>Ù³{²ÙðijÆÅ³\x0011e¬¯\É×³,²Ù´À]æÈòAHN¯öXÌ|]É%|½³+\x000f/Ø\x0016GÇÃs¥"\x000eä¢{Í®*Õ¢k÷ßo>NçêÅ?hÜ*ËdÂj\x0005ÊSÓ)Ñ¼\x000b\fc´¹¿\x000cËË¿ÿú²¹ý°k¨ç©XÒách~WÐàbhË²¼<~}töC
×8Ñ²Kk[T¢ÀqÉ+Q{\x0016ÓÉ¿]Ç5Î¸T¬\x000b©è9©W9
*¢\x001cÃ\x0007?÷äXÏ5N¼T¬ÔÔ-/±¶&íÚÒ\x001dæ0f]Ë5Î¿T¬u¤Á\x000cßÑ×\x0019\x0015ù%\x000eGÖ­Å\x001a§a*°"Ë\x0010Iç|Y®ÒH\x0013I4ìá²åûO¿Ï\x0004­ÿ÷ýó·_®î¿n\x001eî®ïçK±CÓ \u\x000b÷ +#Bä:ùØwpzpþüõñÅOGoÎO.fGl\x0011'³\x0001\x0011\x0007Â\x0013¢#Ùh£Ë§8\x00135ò
OhË\x0012FÖ¿ÁZ{\x0012åÐÊ8¹ñ\x0011µ\x0001\x0011Îiþ'µ\x0010eT³¨h\x0015Ç9jD]Dg)!J_RºÓµ\x000cÍÃ3Ü\x0018-\x0015¦Hô¤\x0002!\x0006¾(¬~0lF\x001c§Sê?´¢çCÎ²¢i+¶¤Ygjgê\x0010ýï÷¿¿ÿ6Ý|µ¹ÿ¼\x0001Çäîv\x000e®#È&£Íã¾P½ª@I!§3¯.^\x001dgr~¶\x001flä¬\x0001Ã\x0016Òç\x000cAf¿\x0013À\x001cW<\x0008=Tlá\x001a¥:k¸tn@.¥x¸çÆ¤\x0018µëgw#ý]ÆÎÅûëOW\x000fóÌáù¤IZÎq/k\x0010_;tëøâäåñùýµÅ\x001a=¿V`iC3«³\x001a\x0002ÊD\x0013ûõX£×Î
,[:\x001d\x001d\x000ce²°º\x001e°\x0006YÎ*¬2%Í;¶TK/4\x000f_«WkT§UÅ\x0015\x0014©\x0012
Ô\x0000å\x001aÊÄà¦Ç¨\x0015QUTÑr¿¤Ó¤mÔµ"¯ÖL	D\x0003×°(ªË\x0008\x001ew
\ßCdj\x0017§èM\ÃÒ¨*.%h¸\x0006lúÈ$é"\x0017túéz®Q\x001dRÝî\x0012i,\x0002\x001dÆ¬Ó\x0011¶uæb¦ð½\x0001kXTw\x00185«qàrY²\x0011¥\x001e_L×üì£ÚÄ·2ÎÕ¿º¾Ï!@ØDE`45?0\x0004C³Hs\x0015[¯NÎfÇ¾nqÆqú\x001e\x001cnWN¯Çy\x001em\x0008E|\x001båLq~?{ømbu^o®o\x001f\x000e~Ü¼ûíqGÅÛêÉ c^"§Ùauaêè½>:9{sðãÑÿ¸
ì:`ýuª\x0005³¤\x0004(uTT\x000f`äë;7eª\x001a¹ú^V%Wà&\x000fJ\x0013sv\x000fÖEø'/ÂF°¾ßP	æ5?*£&.}HËÒ\x001cÎOE\x001e\}Ç¡vÁ\x0002ÇæhO
-gw\x0017ìÄeØ\x0008Öw\x001dêÀ\x0002ÄY\x001bDâ(Uª.)£Ýä¥ÓÆ5ô\x001d*Ápn¢-%Mð\x0010Dò\x000e²Z5`?_Ýýñí~Æ\x0016áÙ\x0007eøh4<@\x0004l¸ÊbK¡È\x0004\x0018?É+Z\x001fû¹Æ)Æ\x001a.K\x0013\x0015Eð!ù]	Ìpë½63f¾\x0001lË«\x0000³çg£ÄZî¯Äa½¬¡¡fz\x0008\x001a¸Æ%L5\"E\x0014ÊN\x0000¹\\x0011\x0011Ó&°qÏE\x0005qE¤\x0010¢FÒØ4E\x0017EÆÜz=×TC
\x0018gï\x0000L°\x001a¡±ìrÉ¨f®î\x00062j¬n$Ó6Kè\x000b\x000c®i\x0012º1U>á[¯\x0006£öæV0MÚVhÏHÖð(?¾Z\x001b¹À)¤3\x001dvÄ¥Ù	^­ßc44³\x0011\x000c«Òó©ôÜ]ëá*'ó*­É°×ñèÌ60_$ÿ\x0005N­Ô<¤½l~3Ái#£	dØ ?¦·EÞKa-RÍÕ\x00187Ñ\x001cÍF2|öÊÛßíp¤ôWäV¥òzjÈnãïbó¾ã½ºÙ¼K\x0011\x0007/7ó*Ö8Mêû¤ÒTª\x0016Ñ½¦G\x0008ß-|uzô"gøßz4+`ýÛ·¿î¸\x0014\x0017w\x000f\¢öróþêæêúv>ÓoI&7þÃÚä£©K2!\x0019ß}s¸8¿|Ãõi/¾;>=>9ßbå»	\x000b,©ÈÚ¨øDnrc\x0015\x001a'!Òãs÷µk!X¾¹ÛÀ\x000c¶f\x001b¡|,\x0013®¨ºÖÚhÖ/X¾¸Û¸¬6dì­T¹\x0015\x001fH.\x001díÞÛ-X:}÷ÇÏãíÕ¦=à¤\x001efy\x0000\x000b7cî÷Á@NÂ\x0019kGPxsÔèö\x0013å°¶ÈbE&Yx/(ÏåËèo0ñb¼­²ûÜ$EL\x0000>\x0003\x0015#á{¤ä"Q?þtMH9m@RøH\x0010JaM\x0000Cá8Îðzåë\x001a$\x0013ÉÑ.Ï#¯¦\x0004IiÖñd;^Ï\x00038¦\x0004\x0016BSz\x0019\x000bVYÇK¬Eê\x0019§ª%Â@¾äW¥\x0018b°µ§-ø-[[E\x0010iì\x001d?:YÔ`»çKz²j¤`\x0010\x000c¦yäÇ\x001de^Ä	½\x0004W5Å!ÎpNÂ$Âº/Ç\x0011WÃ:inJÿmEyw\x0017l\x0014+èñ¤edä\x0007\x001dÔ!ÏÉ"§\x0002gd\x000cëL7G-\x0017\x001c\µÚÒuâè\x0005ÓAÄÀ>¦wël7?æ4¬Sªì&ª°Âu²EâZëDÁhË·ÃÁ(4hÄåÎ\x001bÜásÜÒ­³\x0003ü¶Ô²L2§Ó´\x0000µÀ!X\x0019^H\x0014\x001a7Ù\x0001Éòúø(Rqs`ìºâÙKH\x0008 i79²\x0003xèr-SN¬K\g.ùõ­\x0011®^³
2\x0015=×±\x0007ÞD/o-H\x0010kjv+Y¾\x00089èÉà.a"!î\x0016&åÒ@à\x0014ÿ:¾|¥ãaDÒ®<t¬µÝÀã
¨!Êeõ
'E)`j±d-íE\x0002çßãM/mpÜ5­XvâÌo·²\x001f3=æ¬ÅÑýû»ë/»\x0006]y0¹6\x001c\x0000õ&àðö\x001c\x000eHßUÂº¸Ì)£ïÎO^ï\x0018sÕA¢ ©\x0001	VÆH!ÖÆÐèRÁÅ\x0014²+È·\x0002EEÓ\x0012{%ò;nÔ[MËî;î\x0012$
\x0008\x001aÏÒ$Ê"Y_GÍïæ\x001fíûÑVÂÀóûÇù|\x0000D×ï·ô\x0008ËHS\x0004UW
/ó`>\x0000ÿv¶:a\x000bÓÝDûaÀ\x0000w+ÏµË^z®¾UF\x0016§\x0001bî¡¹F`\x001ayÎ$xEE¹Û½Ò\x000cÓÝÌ\x0015+ÓñýñE`cOÛvÛÌê`ÞJûå­\x001eì\x0017\x001f7·`\x0015_]Ý¿¿¿þ6»c¬\x0000±Rnú°pKùín°6/þyt\x0006VñÕñÅw\x0017'ÿ¹h»qêÀú\x000c$=\x0003V«¢½êV¢.!Ú~°Z"ÉodÒZ}HK¤Jýuë¶¶§ö£9G2\x001f\x000eì3¼\x001e\x001aÃ* â\x0017q3q\x0001\x0014Ã\x001dU6\x0016§åö:\x000f÷k$Ñ\x0008Gjd¨Á\x001cÆ¦\x0010 À\x0018ÎVÙtpú\x0017Ø~\x001c\x0013¸[ÍKVL\x000cÊ¢;\x001c&,s=N×úT® \x000b\x001eb\x0010Ïc¦V,J:ZÉÝ(RÈ-³Qa\x000b\x000e%úZ\x0016ÇÑÚÄÃH4ü\x001aa¥[µ6ýK}?ÌS7Æº\x0019¥I·\x0002þS]UËv\x001cÊðÕ¯M,úÙpkP-¤rÅÃðztU´àPz¯\x001aGPµ\x0013®çzd¥èµÔ*)VáPj¯~utV@'§AÂêH>åaÕê´^ýòÄ<\x0007Çð1ça6Í\x0013ZÃ\x0019½j\x001cEÃ2\x0001ÇX\x001a\x0018\x0015eyâÇ\ÏÃù¼Z\x001eT^"¹q\x000cçI5GÐDt«´oÇyûîÃ½ú<¼"¶Jbè½ØÜüý×\x001fÿ÷ýê/!é ¡(¢\x0006S\x0008]=«Ùöß\x001e/»¢bè½8:=þ×ñÅìûq³c­\x0017pÚHYJcu\x000c²È\x0002hfd»rv,ç\x0002Î\x0010©ýDiË¤pý²ìOµ\x001d\x0013¶\x00003\x0016½`Ô/àåD\x0007Ó\x000e÷äBÎ1i\x00078¶9ïNZ<Áé¢+\x0001y\x0013è/º/<É§úû«û·7àî\x000cqxÈ&H®AJ²\x001eOª)\x001fíï/Wº#\x0014î`õ=À:,\x0015yzL@mÌ¬ÒYâa\x000b\x0011_Õ÷\x0004«°´YX1`y\x0008wõªí´àVcõ]ÂºÕ²µc°Z=IOe`õDÎ§\x0002ëÆ/¿ÝNä3þïÿú?'>cÃýõ|µÅBtVX¤×\x0019±$
øE\x0008\x000fN^¾Â\x000eÙD[¬~f£\x0016Ë§;,aÜ.¢ì¦`éÑoÄê§\x0015ê°à '³Ô­	+òl+äZ¬®K]åê"Ä\x001c¤6\x001eùÊÄ8Ú[5TèøM|0[/¯\x001eowîv\x001cRhÈ¬ÓCÐÙ\x001b\x0008^\x001e_íØç\x001d¾±Ú\x000fc5«Xè*ó\x0016\x0017'&*#&,B=NßHíÅQ` +\x0006Êd\x001c©Jô\x001cÅDLVÓ7N\x0015«\x0013óY¼],\x0015ð`}áÛÅ¯Z~¼Z±::kEäf\x000cÀêp4o¦"Öz~ÄºuPÄ4\x0007\x001dA\x0018ÄÕáZ¢bK;M?BÜO\x0013E²9)·àr·\x0002*Þ9~¹« ùík|x{5}ßïéjÇçÂìzC³÷,Æá¤\x001f´\x001b\x0005\x001dØÐ~±³½C4º:*²H"pÇ8|wje\x000f½^¦\x0005HýÔx
\x00123\x0005Z%§s¡= )î®\x000fvüÙF7ÙþUÊÿÊkê³ø¾\x001eø«É©ë¢§{ä+HiÞGjÈj»ÂÄÆn"\x001a]ªû0HûÈ\x0006Ök\x0010CÖ`üºEêæª*¬£g\x0016\x0015¤Ï
u\x0016Õ\x0007\x0019©§Ô»\x0000©k*à>µ´<M[\x0003$GúÜð1G\x0011^\x001bR7gU»Jº¬%
\x0004\%J\x0007û¨â(OÔÔÏ[Õ2©<V\x0012Ehr!2Ö«\x000f>v=R/WTäÕ!ï%êÕ¨K1ÑO9²õH\fÕ\x0014\x000cõdàtÞ9\x0007&M}?\x001eÅ]V1qMS\x000bSÔ<\x0006?¢U¤rÄs`Vï&. jarÇ\x0019`sY$Y#pýÉ.`úôñ×Ï¿|\x001cú\x0001\x0007¯þþ\x000bÂ¿ÿ{W<ìe2R)K3ÉÁ6.p5
ö÷Èw:wn\x001dq*9Ö©-DT:K\x0018ã ªáÒ\x0004Ô¹á*\x000cÛn\x001e.É\x001b(m¶+4NÙí\x0003úüÍø;1Y=
u®\x000e^ÜÝ\x0002Õ?nnþþkÂSqP0C\x001d\x00182:S6ù18ÊU;Ç\x0007/ÎÏñ é\x0015î'\x001d¾æ·ÂîÊ\x0015Ù8\x001e;W\x001a`Ìmxë'$í;
Í¤¥\x0014:7Ö\x0014\x000c
ªÉ\x0002E¤ý»T
¶\x0013D®¾MÝlvC.%YB:¼<\x001bQC´¼¨\x001e\x0019²ÆïQ;~äX:¸T[QL§<F=#©L	Ì^:¸l[Q½àau8\x001fV4¼ªrô:³\x001cup\x0007·¢B8®iUQêVUÐ£\x001b²@¡\x0005U¿W¿o¦4.þþëÓÝãÍÕãÎø\æBÚ\x0010+z\x0011\x001d§½üTÉÚÅñËóËÓãËÙ\x0010½ÃÔO}Õ0á[4åõ æ\x0007l»ãÄ³HÆµ0õó_UëcR	Ké(«ÂMcV¹±\x0007ÓÆÔOU­\x0013DW3=2=!*ÅYB\x0019Gå}mLýLXÕ:i¥\x00171s©øÑ@(]2SOð-LýtXÕ:PÞ½c\x001eöë$UÉMU¶0õ«8ªÖ\x0006×¤=\x001eÊÈ½JËß®¨«Z'­·i^GEõ\x0001\x0016*rwêA¾©_ÏQg\x000bH·&g3sC[Ø'9~'hB\x001aÖtT1)#¬\ÖçÀó¬\x000c~}\x001aVvÔA©¬ðÆüW\x0006QHá&\[ \x0006å\x001dUP(¦@\x000b\x0015SÅ\x001b2YnþËgÝåÒw#*dîpO\x0019iÍ;*8WRÒ\x0013\x0019é¦Mt×a£ãÿÓDæ·åãà6Zº÷L,ÕTc\x0007¼\x0002íÛ»ÏÁOÉ\x0017×?ÿãÅÍæú~>\x0004´6Uÿ&õwÉ²d\x0012k£s\x0003¾4ã"ï\x000f^\x001e\ìÇéUèTààéüå`\x000e5\x0017±¢¿\x001a\x001d»&^\x001dN\x0005
:vô<\x001e5ÏA\x0015GÐÓ+·©Àyv]úV/\x0014©¸J«Ñ%×Ó¹âêpdY\x001d0GD.%W\x0006j9zÁlÂéUùìÇÑ°$·L§,	§R½?¬Î¨Ä¢	§s±ÕáäQòäu³êmÐ¼:ccÝ3¨-ªàxJòæ\x0011|£¡\x000c(­Q¥b\x0013O÷>«â±9¨Këãéý\x001bîÿ2xG\x000cëëÛxºWY\x001dË¸C\x0019\x0004døÎÐrÕY/]ÇÕ<Ògin\ÎÜ¤²Åè=¬§{­VñçÈ^¿ß\x000eJ¾ì\x001f3ôf÷ó\¿½ºÙ<\x000eî­JµC­ä(\x001cwE2{ïU#Ü×\x0001ÚÞ\u@°2¯`\x0005©8(à³ü\OM#Ð6¢­]!}HúØ<\x0017hè1Å¹bó\x0002íeZ¹@Æ§Ü\x0008öÓ`Õt\x0006²[Õ0²\\x0005´
e+\x0017ÈX\x00062@@µäN)þbbX,Ý\x0008´½ß+WH±öAj¢ÁÂ8QWhø®Ó\x0008´½ákµaËà\C5'Y\x001b6rW«¶w|í
	\x001eÚbåÎ\x0011S¢{sj\x0017ðl/ùÚ3&Ó\§tè\x000b\x0013<EÆ
Úº×|í
É\9}Ú±×ÚÄÄ0Û×HÔ¹è+×H\x0004¶CÞ(DÀ¬(-\x001e¶>6\x0002unúÊ%\x0012¾l"<÷´D\»~:w}í\x0012É*øËúÙ'çbÁ×* Îe_\x0007d£`e\ì¸!ïÌh\x001e&\x0005hÕA+â"õ\x001f
\x00020K.þ+*±ñu6l¨k$ê¼\x0001T®\x0011\x0004=|Ò¬á×S\x0008Ò¨ì6ÈaQW#\x0011KÔ¯×9W¾äÌjÉZÞq\x00185\x0012Üf\x0003\x0011\x0019ÅtDîG²Õ|ÀGYuøYg³Å\x000bÑô\x0004\x0006GÍQ%>¸i|ø½\x001a>Ö4\x0012¾f\x0003\x0011ÊÁ\x0013\x0011+\x0019ºÓ\q\x001c×í#ÖÕl3\x0014ÎáØÑ\x0012ÙÒø\x001cV9X5§ÚöµP9~â]d¸V\x001aü"»n\x0017ÁVMûÚ<1&\x0011iª\x000bFQ*\x0016Ö]jØÑ¥öµõ÷µÅ»6R²ï5D\x0018~4ík\x0012P|X\x000e@(D1¬#]¨öµµoD\x00058:ªrñ\x000f_?\x001a`Wë¦
°¸"Öò=«âárIÐh¯®åÛo°\x001a¢ü××WÀ:O£ n\x0015Y
¯[[r\x000e<©ÉNTL½>9~~|ZÒ«Ú\x0012cn\x0002À¢¢\x0001n :`Â\x001eÏ\x001aPzRûPpx\x001b¯òçP\x0008ëYÏ¨/×HÒË¹î%	¡Ì}	e$,÷»ÐnøòÚÒKpîEqZ¡`«2áHò}FúEõ(dâ^\x0016+xÛbýE\x0019ÅzËÂÚå_h¸ÛË¢"y\x0011^
zÀ\x0010¬;+Ür¢WV»W.sTK\x00055¯Ôè¾uÊêX\x000cÊoÑ	Ê\x0013$ÒÔ)·=AËÍJ'«Ý+.n°õs>(\x0012J,~\x0018jíeq\x001bóV|Ônz³¹¿¿¾ÚQ5|¿\åä"KÞb	\x0003÷\x0018LÕ
½9º¸89-Àìð\x000c\x000b0÷òlå¤\x0014¦ë<ñð\\x0008ì\x0014MªG\x001a8U,§\x0013¥ \x0010&AÐè\x0003%=ö¬C\x001a\x0016î_%j\x000c!)Ö/AÁ\x0005^¥ñåÔÔoV©Z%ÚÒs\x0014\x001e£yùp#\x001bØ4,<Ý¿J^sE¸jr¢W?j0hAêw«T®¦\x000fÛ2\x0005i²R¯\x001eiXôZ±<yÉÊ\x0005PdH\x001bËV¸~·JÍ*°Eò´»=i Ñdh5Ñ¸Þ¶b/9RU\x0016Ë\x0014	+¨\x0012Ó8ûÓÊÔ«Ç©\¦Ò\x0019á`~áMÏ
Ì4ÖZic\x001a\x0015ûî_'§²\x001c
0\x0015Ýëè%×"»0VehcêºCÕÛd\x0001¢­\x0004QéÊÏ6*2Þ¿D¦Ô@[ÁI²\x0008A\x0006%7£XÏÔÉmV_»f+\x000cL5m%10kµî\x001bW8ïgÒBSeÀ$Q\x0001ÇÖÛ­¼âºÙÍjS\x0019i6²ÚÓ8J"Z»µ\x0007]O5DÊ°»dÈÍ°H`ÓI¢%\x000e4[:\x0019×êU\x0012Å,á[\x0010­RiXsfJ¤¢©h970IÍÞÁæÞì`ÿ\x0011­\x001fK¬µ1uòÀÕ¦Ò³¼\x0015<\x000b7¦§¼Nz\¹ØÆÔ
Ø*.gN)v,\x0016ECi¥½ìf§«×I²^Å^â0\x00156\x0004ãjÊ6¦n0Y¿N,5\x0015#éG§"¯n\x000e©gêFuL,u\x0006H¥à0Îª°Î~\x0017Íë6\x001eºç4Îm¤5\x0012e/Eß
¼nÖÚþ\x0001F½¹I&ËÂýñp½cf\x0017·»¡\x0005>\x000e\x0007ê©¥y
>©\x0017´Ô\x0018áþõæd~^W!S]2ÕHÆ\x0003±\x0012>§[yd÷q¨\x0019LwÁt\x001b\x0016\x001c\x0005\x000bß\x001dsË/uîÉ¨Â
2Ó%3mdxñEúÔ^Ý¼÷¥ëÚ¬f2Û%³mdF\x001d\x0012µ9EZ\x0008)²R²«Ö\x000cæº`®qÉ\x001c©A+°4¥»tÞË^sc3ïùÆ%4°TÁ8÷Lc(L¥V}ÌÐ%\x000bmd\x0010bñ\x0001À.¶,¡¢¤)dr
YìÅÆ¯ir[\x0006E«Äñkò63kÀdßÌ6ÚYïIÀDB¬[h(`V¯°²²gÌd5\x000b\x0002ïï|\x0001H©XÊ\x001a|ÈhqÍõ¬l4gp\x0002è0ZU\x0017ÑjÐDB/UW&¬\x0019­gÎd£=Ã\x0011\x000c\x0015N47o\x0013ÝÀµ¬gÏd£A8fÈGªäkÓ\x000eR\x0015÷¦ì\x00194ÙhÑÀÀæÓ)±£$\x00144ºÑÁ¬YµE&M\x0004\x001c¬©º:If\x0004F\x000bqÍªõLl´ià¡Ñ»t É¡©QbHÑ\x001bÖJ¦DÏA\x0013md¨[%é{ªr
\x0004úïiW\x000eÕ3·ªÑÜÂ÷\x0014´Õ?$¯Vò×T+öêû´mNmðù\x0002\x0004\x0005Â\x001eå¯i»­\x001fÍh½@µ¹µi<í3+ÓE4Ïþ¶X³Íz×j»\x0006cñ]\x001cìÍú\x0013ÂR_\x001c©\x0015d½[@µÝ\x0002I\x0018v4ÉLd¤bébt+"\x0001Õ»\x0006TÛ5\x0010*hp
\x0004R¹Ræ\x0011jÕ\x0019è]\x0003ªí\x001aÀNu\x001aæÊ'\x0014¥ ±%4áÖÞ5 Ú®\x0001\x001cßÇ\x0016Íhjë1°(\x000b¬ß¢k òlí\x001f\x000câôï7_¯\x001e\x001evÔ'¡okrý¦ÎÙMl\x0016§fC\x000c ¾?ºüéøÍýhª¦ZÑÐ;ËM9ËÚòÁóÄ\x0018«§/öj:Ý¥Ómt8µ2ú©=)ëP\x0007\x0008ühíP+x\x0015éÒæÏê¸m\x0001k¾¨¯\x0003u%hí¬´!Õt¶Kg[×ÎvZ»xlÿR.õ¶ÓÞG5ëÒ¹ÖµÃ\x001aÝlI´ÐT\x0010pH!­_\x0007ç»p¾ué¼Ëã1°\x0002¤h`é47[8¯×\x001dÙÐ¥\x000b­K\x0017=WÍjÅ/¦!ò´\x000cì:¼U«éb.6®\x0014r\x001f\x0012»â#ÉC»È]\x0018b=¢gEëÅ\x0012
²Ä8¶ /Ý¶ýAÄÉû«®M4Þ\x0013^j®\x001c\x0006%\x000er²Y¸­ª_·x½«B6Þ\x0015iÚ¢¦Í½ù]\x0005¢qn\x0016Õn\x001d^Ï\x001aËFs\x000cà\x000e\x0000\x001dÍ!	\x000f\x0019nÙZ{WÈ½\x0006Ï\x000b\x001c¤G
\ÒÄ\x0007çÂº­×³)²Ñ¨`}\x000cû\x0001\x0006_éÛrþ\x0019èüª»LõÎ­j=·2òLDÀãqN)àg¼¥;Ï\x000fÝ;?tïîn\x001fÀý¼\x0003ÄûÝ§Ã\x001e3ò¤µÎ5#°ûìdÆëûó³7à\x0003èE\x0005¨êªe Ñp\x001fÂ#\x000eJ(#\x0005ÔdìßHª»¤z\x0019i04ªOa£Aàk/:9coÚ@M\x0017Ô,\x0002Å!3è0£øZN°7#ýôÜFj»¤váÇÜJ¦°×G\x0002p+í\x0015].&u]R·lM±wt^½es\x001e¤/ Ó\x0006©
ÔwAýBPª±ñÞÁTB¾µq\x00048»²OòñC4,#U&5ÆáF\x0005ôM\x001aìÊ\x0001¾ÚHc4.Û¦Û5UàSsq´Û¯?lk#í:~äLÖ.*8mãÒ\x0015sÀiãVH§Â\x0013|~Ù¿¡\x0016^Q\x0010.\x0004ò~ÁM\x0017\x001cN\x001b6SnæoCíY~¹ÐôúB\x0008r\x001cÕ¦$u-\x000erà6=Ó?t8«/©@\x0012«@*\x000eé*jÔa&Tl\x0003íÙÓ¡ïY\x000b
»SÓÇ·©\x000e8	NïÅS|ü\x001aº¡Õ\x001fßGA\x001d\x000c%8Sl¦ä\x0013||Õ;üC´Ô³:º\x0006\x000f{'\x00128¬_^
\x0006»ïÂ\x001f\x000cÜÓ\x001f7÷ï¯çgGz-\x0005OÛJÊg¹¸Rknf·Ó¯c?\x001e]|w2;<²©.j\x0002SØ©IûÑå\x001ci\x001bg\x001e4_¹LwÉtÛåg~\1áh8}ÔJÝ³J0Ó\x00053mK¦-U¼HìÀ¢ZyÅ\x0013ÊpÆå
0Û\x0005³m`Qqp«CäêF-xÊ·ÓÓé¼J2ß%ómdAp!FYñü1UÉ¾;5\x001dìTÅ.Yl#óÃ0m5WÎ*ï9â\x0016ÓÑM\x001dì6¡¦PVc\x001d\x0007­\x000b%K¦&¯J²ÞÉmG\x0013\x0006ef1GeÙÊ2Ó~A%Zï\x0008ÈÆ3`Ê\
Mã\x0011Í\x00145LcV¢õÎl<\x0004¦èÐ "ÙnÍé½3 \x001b\x000f\x0001F$´h\x0008ÉóO#gMâ\x001a¦z@5\x001e\x0002!ËÛqIE0§Êù\f9¬\x0018\éV\x000c®ôûû»ÛÝãâ²<t\x0004½zÂè.v2êxytqq~¶kh\!T]Bµ0Òì	)¨Ð<\x0011òC	\x001b\x0008uP·\x0013\x001an=X@M\x001e\x0008\fdLTö3\x001b\x0008mÐ¶\x0013ZErM"ÆÀ©\x0005¯¹JAùéªÈ\x0006B×%tíÚ\x001f\x0012`0ì+y.Û]:ý|\\x00058ô}mÏ÷}<xù÷_ÿ×Íü`\x001eÔúÏa\x0004¸\x0010EZÊI7iüyyðòøèt¶n©TJµPy|q'*kI¥Ý	¼\x0012Jw¡t\x0013÷,\x0014C%HÜ\x0006ÏPa"Á^IeºT¦ÊØÿÇÜÛåXvãø¾S	ÜDê\x0013ç)\x001c²ã iDd\x001aÝç¥\x0011eG\x0003ÈÊ,äG¡û<õ4z\x0006§ÆáôH®¸DjK{¯\x001d!®\x0007÷v\x0003
{;«úg-¤(òON«.\x001f\x0010E÷*´\x000f¸\x0012"MRùÊ«¨Bà\x0006:*wY*\x0000\x0016)>ÖvaÅ®MB\x001e*èÊpË*ÍVQ \x001e³Pùç¥IªØSEÝ^÷\ÊdäN¿ÈÍñ\x0010QïÜy¤J=URQÑ5×
£H*yÑvR\x000e*÷PY\x0005ä\x0001Î,ã%,Àö\x00011m5V4çbBn_5±\x0012Nq·hZÒ¯\x0015\x000bVj'±FË®2íø\x0013:yÃJÁp}yÙî+wôI¬Á´[mÒQGÉÅZVK¦!\x0019]k¯x	ë¸\x0002Í¶
´Çê§ï>~~ÖG»\x0012+:~Û5¾ÎsÙÅVõàÖTwoîuÐÇõg¶ÕMa\x0016Kº¼êÖàÁ¹ö¨{&BäÂ\x000bU\x000bfx\x0003åÌ¢\o¡¿{\x0016Ì÷`^»`E\x000e©+9ñ\x0019yk\x0008v\x000fXìÁ¢
,\x0006¹a:j¬ã-f%\x000f\x001a\x0006mA5XîÁ²
,\x0018Nz\x0017«.\(Os!­g2æ°ìx$Ug\x0012+^´jQ¶X	ì¥&¯\x0017ù¾@\x0006ö(<-?\x001cÝÝî\x001fþþÌµ7Xyê\x000b/á)Lñ¸Þ"yõó3·^ár=Sq>\x001aÏ|¥ÒbB	%\x0000Öß.ç¸BÏ\x00154\`QæÂ-\x0013À«Ú\x001fIè3]SãJ=WÒqµ44£ª\x0016ö\x0016.ï8\x000cþæ\x0002;:#êã\x001a6þýãPCõ3bÆ·çò\x0012>×\x0002mæV±nþÚ©_\x0004\x001e\x000ct`V&9[¤)\x0004õb"F\x001aÖ³þ³`Ø¡\x000e\x000cEÏÀbìzB
qØ\x001d­W?Í¢¹\x001eÍ)Ñ¢¤¡\x0016Æ_ÓV\x0012¸ Eó=W~N'ßt_SÒO!­g\x0016gÉBO\x0016' He\x000b\x0015ð"£Y/3%Ìz¦x\x0016-õhIFÓ%ä\x000cXO!Ê÷´ûgîÑ²\x0012Íp·«¥I,Í¡½d¦õI´Ã%i1iFÇ\x0016L-AÅ¦eÓ\x001eLp586Z[¥¹µi\x0016°I$F\x0011¥"u1Y¶ÁàZ¥Å-N\x0011£ÈÓ:#£ÅéïÙmv°¹VitIþßÍÛ[kY·Ôv¸=Ô\x000eF×*­n	øBW¼Ã,ª¤\x0001×{ÒgÙ\x0006«kµf7ñÛ¡ ÞeÙ\x000cû.²ÁêZ¥ÙåDÁ\x0012xx\x0019\x000fQ\x0002H1»n½Bw-\x000elQÇ\x0006á0ö(5ã&æ×/Â³dC°J\x0010âeæ½¤407gåÓ/
Ù\x0005¥ÙÍ%\x001aâz¶pPkG'·N·þ°9Ë6\x0006JÛF=W­\x0019Ã\x000f'\x001aTìA\x001bÌ\x0007(ÍGrâä6¹Å¶j´Þû:Ë6\x001cRP\x001eÒr%q[(íGÈ»N\x0002\x000c'\x0001'ÁWY%Çaùf\ìÄFÑ¸=a8\x000e'\x0001'\x0001åQ©x+ÃÓÉKpdíLÏðKl%\x0002?ê0U¦ê\x001f\x001fx`ëÕ¯\x000f¿>=<s\x0011,ÓH\x0016®ê ÆAf\x0000ÇÁWýróÇµ^]_]ß^½H\x0006=\x0019èÈ¸Ti¹";\x001e\x0014\x0016³äËí"Ã\x000cÕk\x0016ëXÇ,·AÆï¾%6\x0019>§\x001aÍõhN¹hP§ÔyÜ¿§72{7\x000c^Tæ{4¯\5#Ã'#ÉiE^µ6*ÜBÞ\x0016z´ D[ÒÛË°w#I¢,Ã`<D¿ë{Æ,ª\x0017Í\x001dòjõ5³,\x001a\x0008\x001aìÛj©GKÊ­fe|xq\x0001K±Ü²jYRXiéÈ=ZÖ¡*jD«Fb ¼jÀ·\x0003Ê\x001dh]c\x0002Ù[£ÞkgN?\x001b\x000f'\x000fÔÛÃ6ú\x0002¥3(7ò\x0011Í2(ÔdÝÆö#5Ûà
¬Ò\x001dÔF\x001fSãY\x0012O%³kÁíb\x001büU:\x0004\x001aBXOi6'
ÄlÄ!à G«g\x001b\x001cUz\x0004ª¨ëV¢Ë*ÛYÖo\x0008¾\Q÷x\x0004;x\x0004«t	¾K#6zaDÞoQæG\x000f¹z¶Á%X¥O(\x0017=SÍ[9mNPp24>]6dp
Vé\x0015Hµ\x0006m%jãâÇâå[éÙå\x0015ìà\x0015¬Î-Pá/rUr#5Î´¢\x0012»Ç-ØÁ-X_À\x0012áV\x0015\x001aÚ\x001cÜaJÀu`;Ø`ð\x000b ó\x000bô\x0014ê¥Â$p\x0019@Ùc\x0012¹9¿ÇÀà\x0016@ç\x0016¨\x0000>qEx¬d<Êª%³çÂxGÐy\x0005R:°\®5í¶ºif÷\x001cR\x0018\x0002èB1^<`°Yõî)Ç´²y³ËðÂà\x0014@ç\x0014hÈº¡,åL&³À\Y7³mp
 s
TÞQ+»KÀ`Ù¦E²®Û¾à
\x0006§\x0000:§àÊª>B\x001ad°<å	e@¼}lS\x0000SpN%`r\x0014loZ¾ê®o:8\x0005Ð9\x0005 \x0013©,´cj½oßÔìqô08\x0005Ð9\x0005W:P
E\x0016kBlû/¼\x001fÆ\x0000«Ùpp
¨s
þ0iÍø\x0017jÝ(\x001clHÈ{ö\x001b\x000e^\x0001u^\x0006f°
±¡ê\x0016\x0013\x001bHêö°	\x001aíu4E£Nc\x0003\x000bUà¶°\x0008\x000fÖló¦é¨À¢üÐ%Ü®Þ?þûÃß>=^|ÿôÛÓã§s|tc`·µ<\x0011±ÜL\x0004hRætÏ]½ºù«×ßß\x0015ÒÛïooî^\x001e\x0012¶@bk¦n\x001bi\x001e\x001eúyµ®Gt\x001b\x00109]³¼ìJæ¦¬cj\x001aopúµ¡\x000c\x001b KD,`\x0018¤,6E\x0017¿^ÒB¦\x001e2mÌË=b)\x0015
õ\x001c½<Öø±\x0016O	\x0019e\x001a\x0003vÇæú÷OïË©þíñâ¯ïÏWðÒh'974 ½jã$#5@>ë\x001f¯î^ýýÍÅ\x000fWï^¯ä\x0015Hè!a\x0003d,\x00017(@heÄØ¤âiS
=$nYI\x001azÆ\x0015eò°±\x0004¦®D§jL×cº-kI\x001d\VRütM\x001ag\x001a®.aø
0}é·`È`\x00053ÊL­^4­ÄjÌÐc-îðF\x0016#ÏÏ)ÊÒÓ7Ø±Ç\x000ePàSÖ\x0005ß0kÅaù\x001b|ôÔc¦-þPîÃô L\x0019ü\x0016¢\x001d<7bæ\x001e3o:BM\x0015ØE\x0019\x0008NG¨½Ùîÿæ]F<`\x0011W`ø{Çi\x0016@¥J^Íµ+sô@[\PôÈOàTÂÈ*)ËÞ4¨z7æàì&'\x0014[ó\x0006U¯°\x001c·JT¾spCv\x001f${S
<
-¬·LüR\ãN#85çàì&G\x001cvþÒñz¢¨kkö7øî#²<\x0011)òÔ`³\ø9úÈ2	º#÷HvpDv'ÊM`Øó´jâ.¿@ýéû9\x0007Od7¹¢,#©,Õ¾p#v­ö+~\x0003\x001bo\x0007Wd·ø¢\x0012\x0003KøîYÕ8TÏ\x001a\x0012\x001b1\x0007Wd·ø¢DR\x0003|å<PòþÓ\x000e3-Î\x000eÈg§	ÏÕÊ;lÏ\x0004û×\x0013\x0006g\x0004[Q²QW1¢lY<:¯g2aÿöñF´Å\x001b%LµV8]\x0015õ\x0014Ñp¦oðÝ\x0007o\x0004[¼Q¢î¸IQ\x0013\x000fÄ0b=\x0013¬<Â¨1\x0007g\x0004[QÇÑÙP¬'òrzÇ\x0015ÆÉåýÖ\x0013\x0006g\x0004[QrA2H\x0001]\x001b0bE&0Ñ+ônÎÁ\x001bÁ\x0016oM^\x0013'¥yªÆÍÂþ\x000b\x0007\x000cÞ\x0008¶x£Tn\x001c|i\x000f$mÇdPTªû\x0006f\x001e\x0006o\x0004[¼Q\x000e(½Z!/\x0015£Ëx1
Jé\x001b8M\x0018¼\x0011lòF%ö4lÊí#ò)²bÂJS3Â-Î(û¦ÂT¢
\x0019$W\x000c)\x001bùq¿UÂÁ\x0019á\x0016gD¥/<GR`®N­2R±\x00192\x001dÝ3Â-Î(§ÄµßÅWíR\x001a\x0019(\x0003\x001a2Äý\x0017M\x001c\x0013t[|Q¹\x0003É¤­\x0008µÊ\x0019µ²+µ
jÌÁ\x0017á\x0016_T¢7IÖ L¨`\x000fËù
B:\x001c|\x0011nñEå³JÇ\x0010¥Á\x001cÛxàú1úìû}&\x000e¾\x00087ù¢ÒkB	¦ÈÆS\x001a#³[)¶Pc\x000e®\x0008·¸¢ì¥\ÅF\x001aW)½\x0008eÿ
Ò 8x"Üà±"&cé*Ç\x0013ÛjopkÇÁ\x0013á\x0016OC\x0013N,^©ê¸ÐØËÐ8Óþl\x001b\ÛàñI\x0012È$ß\x0005¼ü\x001cMcö/§\x001b<Ûä²çqî%Ô\x000cõYlHªPBd?çàÜ\x0006OHîã¤d¹ºÛ\x0017£\x001c3­Ô\x0002«9\x0007Wä6¸¢ò©YÝ8½ÄÇà¡­ç78ín|,ÚàRñKs
÷P';clÍ"P¾sðEn/JT\x000ffxð" L FÀNã
¿Áq\x001f¼Û`äËþLÒ\x0001½ç\x0019ö(µê4\x0000î\x001b|÷Á|º
æ3QMQ\x0012N/Ó©Q$¢Yy»ÖbúÁ,ù
f)!Ä{*Fgµ\x0007\x0011´$]õý\x0011\x001fN»ßrÚIÅÂÈ ã\K\x0001¼¦`Nß \x0002Iÿöç§ÏGî~ÑïQ@ãpÞÛ\x0016F\x0019ñ\x001b¼\x0010;s[Üç6Ü\x00042\x0008\x0004i\x001c\x001fýVùÝ7Ø«\x0005÷ËRëÑãÒ/úEµ\x000c\x001c5+2\x001f,/7ùìü\x001eÚ\x0008ÿ6D\x0018Ú\x0017/Þ?\\¿øûÓ\x001fÿçÓyY7_ö+r\±¦Úhüxk\x0005|\x0017¯®.®_]ýL\x001d/\x0011BO\x0008zÂrm¯éOS\x000c?¢ie|iµ4SC=!ê	ãË&nz
®\x0015hÚÕ\x001ao
¡ë	Ý5\"eD×\x0013m+ÓÜû}Ïçõ|\x0019Ø§\x0003Xû<áA·r÷&\x000c=`ØtL\x0002×|{ÑË\x0010åÃq¼Ý\x0016ºØÓÅ
Ë\x0017¥Ò,zä\x0016iDÉÒç½©'LjÂ`j\x0017DÊ¹X\x0019'ß½·/Qû^ÀÜ\x0003æ
\x001fè%Y
ç14ÕMØ»]\x0007Yj³\x00011Õ\x0000\x001aå@F\x001capÒ¶!Ô\x0011¾DïL¼:\x001fãBÈªÔÎfYD»Ú\x000b¬A\x001cÕ{@~;!Só&­Ð\x001fíj\x0007©\x0006qð&VïNBË;ZùÌÙò0£rEQË5«]è\x001aÂÁX½;	%\x0016÷¼T½.r3­E8Û½88\x0014«÷(¡\x001c°e	©Ð^ÔpÄÂf\x001dÞàN¬Þ\x0004HÒÏ_ÎG\x000b\x0019ÈC<½\x001bê\x0008\x0007bõ>
ØYü1£¹ÌìS¶\¿\x0012kë\x0010\x0007b78\x0015¢×@%1<h\x001b\x000f*\x0017«=ô\x001aÂÁ©Ø
^\x0005b\x0015M&Tÿ²Yztqµ×T\x0008W
^\x0005¹Úý]\x0013AJ"b\x0002°Ú]¤A\x001cÜ
lp+Xkê\x0017\x001dãË>Í^mTÔ w
n¥ ²f	¹e\x0011E\x0008f-Å7\x0007hUjì¨RóõâÇ\x000f\x001eÞ_¼~úõãûóm=Ñ\x0015·\x0012¥ü\x001fd¾ÇÀòJýò÷ï.~¸y}swõêâõíõWç»{ì±4\x001d¥a\x0014 <mc©®O¬³ËNlóWµÓ÷~\x000b§§¢!®[?ùØT\x001bóÊK½\x001e4ö q\x0013¨måT¹ÎEÌåÎ%\x0005Yký\jÎÜsæM¤\x0014ÇI0s0Rñ\x0012mø\x0006_ÞGiÓY¢j[àzkc9ÐÍA´>B\¹t8KvÓa¢:Vk[e82\x0007­äz¥íGO:&»í8p\x001cÔy·CåC­úö\x001b\x000e§Én:N¡xrç¸\´MÄ.SÊÓJÕµt8OvÓ¢:¼ÌõÌ	Ú\x0014(R·\x00125}\x0003\x000b\x0005ÃM\x0007ò\x0003Rn1«ËBurkejÒá@Á¦\x0003U\x0016MTpFºOyrq%¤S\x000e\x0007
6\x001d¨C[ÓèeÂV\x0012Í°â79ú¹Ïîó^í²û\x001aà\x0012D­Ê¦µQ:\x0019\x001bÌ·p¨`ËÝ\x0008\6\x0000w\x0007Q
\â9pÁJé#¥\x0015v\x0000C:ýÊ½õp¼þç×Ï_>\üðé\x0019Âò+[\x0000S"Ó6Á;È\x0008\x0008ùô\ýÏw÷oo__üp÷2\x001aôh B[¦\x001eÔ\x001b\x001cD\x001eB(âÍVÊ1\x0015d®'s:2\x0013Ø\x0013ÑüxVêÌåOÉ\x0000Âµû\x0002Í÷h^\x0016R°<yÐ\x0004W\x000b0ËE¦çÖFNûÐB\x0016T«Fõ\x0018.µU«\x0013Í²AÞö®ZìÑ¢rÕ+oL°AÂcS[Èã¤h5ZêÑzÕXÜ#Ñ\x0002Êªñ\x0010ª\x0000fEM{´¬[5L<ÿ\x0016|Å^È¢íùÝÜ.²iF·f¤PX\x0005*R4|¡ÉälÔl\©àW°öVep©*ÿ²O\x0012õ¯ê¦i\x0019È°,ZZS7U 
öÖª\x000c.y#¾\x0006\x001a\x0002¨)Ç(±`ñ{ì­\x001dì­U\x0019Ür>³h\x000c¤ðXÉP\x001a\Êõb\x0017Ú`o­ÒàR3SõR\x001e¢dð)YõÈo\x000fÛ`p­ÊâÒ®âq3eÙêÄê\x000cxÙÌJ¢D6X5«2k%
â'\x0013êÄm"3r[2nÛÑ`°\x001e ²\x001eË	å·æò\x0019ùªQv \x0015»Wrï
¶1$R\x001eÑrµ¬µÅ½s
\x001eí6ÓJÈ®`\x001b\x000e)è\x000eé2Å(\x0002\x000fuOËùÊ\x0016W.>
¶á$î$P/\x0002ë&¯²2P$rÀ=§\x0014£\x0000º£\x0010ln\ØHé Jý&gE0ôÛ<\x001b\x000eg\x0001ugÁ\x0017\x0017Õ@2PÙ Ë\x0008Ì\x0010vyR\x001cÎ\x0002êÎ\x0007Éh>Ë,áBÉËFSLö 
G\x0001uG$é3³¿¬³
Ë²±Þ\x000fk:\x00063lxTÓU~\x0018ý¯\x001e~}æ
"×9¹)G\x001a\x000bÕ\x0006\x000cp\x0019Ò¢F¹¾ºº~\x0007z\x001eæÁ\x001f¤ônÛ+¬ÈKÚ¸ö
;Å=\x000fÎóÔ
µõ3<!Y¿zQ`q=e!}ËX.é¹Ç\x0003\x0019/Ì\x0016ÖJ²¦|\x000fäghL]\x0012qÈ\x000eÛ[Ü¼@¡ç	³<`üÒéL@FDbr<wÊ¸ÒÔ1\x0007\x0014{ 8½@\x0000õU*e_Le\x001d·@¦ÿ?oWSþ\x0013@©\x0007Jó+dk1lY!gæej¤\x0014ÛØq\x0006(÷@y\x0016Èf«çOV»\x0019\x0017
Í¶BaM\x000br\x0006¨»-âX:õ<Q¹7È¬	*b}ÊÛ1Ñª\x000cõ\x0014Ñh¢§m4¥¼å]\x0014¹¸'F+vÈ¬ÕÁM\x0001
6ÚN\x001biªQ\x0016CD³ûªjý!¡dÒÚÓõ³DàÌèÅÊ\x000fceò/~+\x0000ç-<[,\x0013wåÙB&¾°:½äâ»ïË\x000f/`a\x001a,tml\x001aDÖ$.¡9ÌªÜNå{*¯¢ÊÜKcåáÄ\x001dfX­mLSÅ**¨"\x0019ÿ!\x0012A-ÖRô/W\x0014+¦¡r\x000f5P\x0016¥Ûd\x001a©PIÊ¥~µLc
ËÛ]³ßIdÌÊ¬@¸,%õãZ\x0005¶s
ûÝj6|¤ê\x000bæ¢áêùHñ$ßõ\6\x001c¿jåUã»_ß?þãáÓo\x0017??|þòøõ¼Üfql2÷Ñ\x0004`#\x0001\x0018\x000b¾ïÞ¼{uóËÕÝ÷\x0017?_Ý¿½ywVgS¸ ç\x0002\x0015W\x0010Ñòr¹CÎ\x0015eðb·ÐôÒ{j0ìÁP\x0003Æði´.À"\x001aIý9èsXj.×s9Ý\x0001+
ÛE¶?ðÉpQ^gM
æ{0¯\x0002+·ºÈ\QÞxÁrÙ^áê¯.j®Ðs\x0005íñ\x000b©q Oº \x0013ª
X¯P¦\x0006=XTí0H2,Ù\x0006/O·È³!C¿gç§+é\x0016,Hó­)$µ0¯,¼2â®\x000f{®¬Z/%*\x0017\x0018\x0010ùKôÒÄêB\x000cÛÁºx9Ô×\x0015Å%Xú\x0015Ë¢Þ\x0005Íè#ö©[5ÙhõUf\x001fí
õT\x0002d	u0H\x0003½\x001bª,ÕdÝ·:Ã?Â£x2$Q\x001b)_{G²µ:\x000bK/ëü5ç[k\x0006U\x0011pHªÉ\x0006Kfu¦¬ÉÉÌáRÀ$nÅ¸gÅ\x0006CfUÌ\x0015_ÉºF4	­É®
.ñô\x000ea\x0007Sfu¶©®XÙf\©],ñO{¶ÿ`Ë¬Ê9J¬e\x0013eÆMvQ\x00195l'ÁÎåÌ5&åËêO\x0014ùH\x000e¦þLM6\x00183P\x00193\x0017Ü²·x¬:?,ºöÒ¹l\x000cbUÆ¬Ä"*K#d\x0010xÍD\x0019³ßC6D± 
cË\x000füL¼ÜG¸V\x0014\x001fdáp\x0011\x00063\x000b*3["{9\x0001\x0016"Ï¨ÍhEØØ\x0019»g
,¨"Yzáá¤\x0005¢L%ÌÁ\x001eî¼»¾æà\x0000@å\x0000ÔxÍÐHñ\.$\x00042;<\x0000\x000c\x001e\x0000T\x001e¥e\x0004½;\x0014w£\x000cCöä×·
\x001e\x0000T\x001e\x0000©wÍYù®¬÷2%,ÛÉ\x0006\x0017\x0000*\x0017PÖ¤¹\x0000pÜ`C\x0008ûÌ\x0019\x000e.\x0000U.\x0000s\2*´f9Ë\x0001p \x0015.ì¹\x0002à`hQehË\x0006\x0017=¨åµÃs¤Á]t\x0007Øñ5q0g¨2g\x000eÌr\x0019'2ÛîåÎ·H\x0006o'\x001bN\x0000ªN\x0000
\x0005ñï\x0000¶¢\x00162©¯
4,q;\x001böSí3jUB\x0006sr\x0001.ÿ+Û,á\x001e°a9Ý6£\x0001|Õ$IÙºdÞHº$ÝvÙ\x001fÝ6#ÝÐêÀG\x001e\x001eVb \x0010Ck÷¤ÜàÊ7¹dE\x0011|¹\x0004p\x000bZ;F½l'\x001b\x000eÓ\x001dbÎ\x0002\x001bØF\x0013øv4=Ä\x001dæÌ\x000f\x0007Àë\x000e@±®-\x0008<W5û&OîÁí0g~8\x0001^u\x0002¼iÎ	".¦\x000bY\x0003ÛòÃ\x0001ðª\x0003àMlY è%Ôö±\x001d\x0000\x0008;¦\x001f\x000eW\x001d\x0000O\x0003Ár#ã,P	\x0016]#ÛaÎüp\x0000¼.\x0006J ¾6Çæ5­TcØÌ\x000eÃ\x0001\x0008ª\x0003à1æ,%8×\x0012L£aO}l[YÞLè\x0007ÅefEpò8.¥Ý>\x0002dCôxÆäñ9Ò¢å<]ÿþø·§\x000fK\x0003õÿç]ýíéËÓ\x001fÿ<ÇVb°ª\x001cÙÐ,ºÀÝ#7\x000føhú|Ðõ7?Ý¾^:¨/®~º}{{¾¿é §\x00035]=g0\x0004~ØÅê2\ÿð«gÃ
Õl\x0005'\x0016Ó\x0018;/+\x0017\x0001Ãz:×Ó95\x001d8~1^òØy#ºD1örõl¾góz6X¡
ÃÈ5O&Kñ#ìÚs¡§\x000bzºÀâq%ÏUÕÖëJ¼¹\x000b.öpQ\x000bg3Ô\x0007E\x0003¤^Â¥GAÆ¾íMÏz¶¤fÀ\x0011!ÍH.ú9ÔE\x0015ïºkÓå.«éHÝ«\x0016:Çum"aH¥£{ÖÎfXm­\x0007~Z7P:Z\x0017åËÚ¾íG7Øa»Á\x0010§ep\x0003}[\x0012©g"X±'ÃÛn°uVmìlpü@Eò¾<p8.sO¸dyßâ
æÎªí]¹Êð¡µ%ª!]¤ªÒùöX\x0014;;«µw¤ð3+ìrnÅ\x000b&\x001c(÷xY;\x0018<«¶xå\x0004pí±/ëöÐ\x0005»ÇËÚÁäYµÍ+nZÂ§%1Xñ)lã¤q×Á\x0018lU\x001b=\x0013ì¥hÂÒ=Ot)>æ0yEM×I QpgÔ;/Õé:Ëìw\x0017*?KÝ¼vÏâÁ`AmËÖ\x0011ë²$ümQ\x0014Z©óq\x000fÞ\x0018\x001akMr1i"xlèé£\x0006Q>X\x0015ïw}Û!8\x0006utlÚÃ\x000cå\x001dYTâ\x0017^»{l\x001e\x000c\x000e\x0003´\x000eÃg\x0017¸ð¯8îú¸Kçxd\x0016IîZ¼Á$Þ$SÛ4[dP¥\x0004wB7¼ëé\x0006\x000cZ\­©ãÆ¨ÆgJi§°'ÌÁ"Ö"ûL)ôz,L\x0014é(mKÿÂ\x001eºÁ Ö ~à:2ú/ãÞî²ñP§=x8XdÔ[äbòêh\x0007Râ¿ägPNí0\x0002KO7\x0018dÔ\x001adË5Ûq¤\x0012ÚíÇKLÅ=t=Fµ=Àã&HS$\x0007i"¹åù>u­Ç\x001b³\x0015Z\l\x000eWú´õ$z/njXÛ7XdT[dëLí[.«ç¥Æ&xËyO\x000e÷Xd\x001cBxÔðeÌrXiõ KìQÌ\x000b»íà/Pí/\x000c
â©
@tC]<'cIwuIÆÁa ÚaØ\x0000Wîd
0}[gä>³2x\x000cT{\x000cª\x001c4,¸\x001a-\x000b®Ò~\x0012f·\x001d\w uG	Úëß\x001f~{üðL¿ëRÝË×Tg\x000fS·"¤vu\7y×?^}óú|¿« a:´róI|/#\x0011(VFÂÏ¸ºåfÉ|Oæ5dT%R{ÒS\x000e±ÚäIÎªõë¦d\x0016-öhQFóÍt\x00027ÂD42° ¬ä.´Ü£e\x0015\x001a{v¬
r\x0008Àó(B\x0008¥(®¿W@P£ÙáZÕ\x0017-¯_fP'?òä!l»Ç&kw±¥-©Ø(\x000f+ç\x0000"\x001b·ej\x001f{uÔlÝ\x001dÛ\x001dß±_fóï\x0011ÔþÈ¡p\x0006w!a×=»­»Àºã\x000bìËh¤~\x001cÛåº6ªÑ í\x0016j®§cgÙÜÀætlåî\x001c*a\x0010\x0003¢dÙÉ9ìa\x000b\x0003[P±ÙlY\x0005ö¼×%\x0017EbÝU_:Ë6\x001c\x0005Ð\x001d\x0005[.\x0012bZ),¤\x0001RâHÉãogÃá( î(´ü:9ù wêEUÝ­§fÑ£º£`­«]·4£\x0003.¹WZ$-phÞÖ
\x001f\x0014u\x001f\x0006r°\x0014}^Ò$ÁFaõ°wÍ\x000f\x001fÔ«>hñFuÄ¢ümYA%¼.©§ï±m~ø ^õAK\x0000â$Þ$æo9\x0000×\x0012;\x0008\x001déÙ\x0006ûáUöÃSË\x0000\x00178MT¯
Ésñ¯+h{ì®\x001f¶Wm7OÏ­üI\x001d=ÂÖ\x0010¤0GfsyÏºa»\x0005Ýv£BsÏlÔ¹_/	Ñ °a\½$Ì²
þ*¨ü_Þ¼ª\x0001ÁxàMÖß¾¦c£a\è\x0017¯OÜÙF %©È°Æ!¸~Áz\x0011Ñ\x001f_°üxÁú¼Ìûíã\x000f\x001e¿<#ÖÊ5·>\x001a© ,UçÉØµTõý21îû7¯_ßÜÝ¼}\x0011zFØÂHã¹\x0018\x00192r\x000b&É\x000cîÇÄ\x001e\x00137`ROee^SËþJÕ°f_®Çt[0
Kloî¤Ì\x0014%¨tgmG*)CO\x0019¶PÒ\x0006^LwÉk\x0019e|@´g-c8:=å\x0014\x001cNÏõÇ/ËÑþÛÇ§g\x0004{Q\x001aïM"áèZÚfD+¬D«þt\x001d¯ß¼]ÎöOon_\x001e\x000etpÆ¶\{¤9°U\x0016'\x0003GVa­²MÃ=\x001b*\x0017®|N\x001e\x001cGJªÜPb$%VB¬xúi5p¾óÊÃ Â\x0006aÕ¬S\x0018!X³òð©Ë=\VÂEI\x000b\x001cé®U]Ð9%FOÞ§vP\x0001gÇó <\x0010&ËùÂâL\x0017Åo²çì°ç¬vÓa«»ëdM\x0014\x000c\x0013p×Ò\x0019?Ä
ËÆëB¹\x0005ÄÊ\x0014&R2¶~Ýv.LÓhf\x000e\x0011­\x001d\x001eÇ
>>ýûY°HÎCj=\x0013\x0019Z]öj-j±Åwonÿå%*è©@CUªå.CZ.V°	Òf\x001eÌjªb\x0012\x000b{,T`¥r#ca\x001d[B\x001d\x0011¿ÜF¹õ%¬\x0005¥X®Çr\x001a,G´T½[ëÄrñQRÂÂÚ\x0005c\x0012Ë÷X^l«ù\x000f®VÕrVê×Íj|<\x0015z¬ Áj°\x0016¯m¢9F[¯¾¤=UT-Vlß0bíª¢ÅÊmkåµÿ$Vê±\x0006\x000bã%7 aYkµú®?I{ª¬\,`,_¥2ÅJÒ·w|Ã~®*.b'ó\Q\x001eÊA4u$_Òh|\x000e·C\x0006^cáixXør£©é´¯VOB
öÝj\x000c|*VÛÈÁ`5ð~É!W(\x0017·\x001bR;Øw«0ðBÄÀª¹Î«¤ùõ(:ã\x001eV_d&¹\x0006\x0003oU\x0016>\x00037e,R5±\x000eª7¾é!í \x001aì»U\x0018x\x001aÃ²Å\x0014Áë¦'uåCïà\x0014Ã\x000c×`à­ÆÂgæ\x0008mµ,ðo}ÐiÇæ\x001a,¼UødhÏKO;ÈG$'Ñ»°Ý\x001fÚÁÄ[§Ò2VM\x0003àvÆ²\ò\x000cYÖë\Ö`k0òVaåIëh-\x0015ç§j¹Ð\x0004éf\x001c¦+¹`°ò ±ò2q|é\x0018lß±\¤\x001dW²\x0003Ó\¡\x0007¡O4úVH$\x0013ªñB0Ò\x001aWß\x001e'¹ÆX^cësDo\x0007ô¶W×ËzY.¿ã8\x001a\x0018ïftÍ\x0018Ò¸/G<Q¼£[îK8(R[.¯\x0016ñ¼@gýÑ\x0005&köÓ\x001fÿüüðá¯Ï¤FKü«ãöôi\x001d\x000bç'\x000bëfÿ§û«×?Ü÷G÷ ¢C-\x001dm1\x0019¯\x0018¤×\x0018AiõÅvÎõtNI6ð :ÿ3¡ÞÊü?¿sí|OçÕkç9ªö!ð/Ä6æÍõHq\x0016.öpQ
N)Û.rv\x0016"t.#0\x000b{¸¬±Í ´^¤ÁÐX9\x0013ë\x000fÞÓt ?³'ðÊ9å°æ`\x000b\x001eJâ8ù3Ú,Þpd­öÌJÿ"áù #ÕÐKËvaÝ£Îâ
§ÂjE\x0001÷hd}v»\x0002M\x001dÝ7\x000b«=\x0018\x0018¥\ËÆâÇèëÄZ^oµÇ\x001bNÕ\x001e%ã£#<\x0016\x001aôr4
é®½\x0007ÃÑ\x0000íÑpÅYkh\x0002uMÍ §xÃÑ\x0000íÑp^$c¹ø\x0019\x0011Ý.»\x0002ÃÉ\x0000íÉp\x0011Dw}\x0015G<çßËiY-AÇ\x001bN\x0006hOK(\x0002û	R\x001b\x0005\x001fùu4\x001aXm.Ç\x001bN\x0006hO·"iO\x001d\x000c,X\x0014lL·\x001e~¾Èâz/?ô©÷¯\x0017w\x001f?ýããÓ3\x0012\x001fÙ/zpX\x0002'jý¨Û.Ê
fî®\x001cw\x0017w7÷7w¿¼¹=/òÁpØÃ¡\x0012¤bsÒëFÓá|Z¹ç(à|\x000fçpÁ48êö\x001c-7~ÖJ¾T\x0001{¸¬\x0003?\x0008ÁJ=4UmËÊ­ö\x001eOÁåã=×|þøõóÅûÇ»ÏL-J®JQQ?åa\x0018Éµv#H+U\÷oÞÝ_¼º¹¸{s~nH:ª\x0008!4P¡ER®¶Ü,¶¾lSù=£Å\x001c¸\x0002
{4Ô¡ÏÈ­\x001e4Î\x0017MÔØ¨j\x0017ëÉÌG©½Ï&Ë¤%Z,)fL»¾§ïÑ¼n«å$Ãi2	\x0012ò¤º(ý1åpì!\x000b=YP%puø\x0012uÕ¡4{Ð¹Öì¹,ödQ÷9¡Ú\x000bþµX0ù&°R,¨@K=ZÒ -E\x0000õîE³hë#»$ã|\x001a\x0006Eë¹rÏ'À×ü%K8aMõì¼dyåc\x001e­\x0013¿'ckTkF½\x00132HÒ o´²~¢BAeO{ØFG ó\x0004ÅòAü\x0004ù\x0010\x0018¡²+i\x0008\x0005Û`n­ÎÞ&Ì<ÿÁ,µ<,:ñeYNc\x000f\x0005Û`p­ÊâR"_EO"\x001bM\x0011\x001c×\x0011áJ^ZÁ6X\x000f«2\x001fK\x0019\x0011w:3ÉéLrZm^ô.óacjUç4Z\x001bKìSÏBùKËUuÎÉPU·R5Ï\x0006ÃY\x0000ÕY4ú¸\x0016L\x0012cõ[_¿¾?\x0005Ûp\x0016@u\x0016\x0012\x0004¿¼¼/ê¹¦ÆáÔÝ)ÅCå^zIP°
\x001e\x001eT.>ÑCÔxXWç\x0014¶í-dÏ'5aÐ(\Ü|Ýóô\x0007e(àbäâA±cÛÈþ(Ü-&aÌðß}üüùé¯\x001f>¾®\x00126TÍ	ë²\x0015UL\x000cRV·Tp¯ÝMïÞÜßßþðúÍ«ó·SæÃ\x000fÕ|4Ö¬~^o\x000fcx¢\x0014ZDw¦*e\x001eÐõN
è\x001d×t\x0016À ©ôrïJ
p=o3\x000fè{@¯\x0006´iIÅ-Ï$Ff¡\x0002ªß	\x0018zÀ \x0006¤\x0008kÆ\x0011E\x001e½èÓ(×©\x0007L[Î\x0008\x000fÃ¡\x0015LR..yÍxîYs\x001a°ð
àQÅÏÔ)òNi	N\x000cc;$)¯\x0017+¾\x000c\x0008Çb¨p,zÿðôáËÅÏþq¾S.9ò,h\x0013.õR¶Kåõ\x001eû«Û×o/~¾»ýå|¯
Ø£	Óå#À/\x0017?=|úòûãY\x001b]®[¢°HO<Ø\x0019¬ÄÈfµuëþíÍÅOWwo<«T pÐÃ\x0012®|HéLõ«\x0018]\x0002/â1iÍ¨ð\ç´xåúZß¯K \x0005Ü¬\x000cdòå/Wzçñ|çÕ«\x00179ëoÊ½\x0005FÊêEþ¶É­%85x¡Ç\x000bJ<¤w\x001cl
[{\x0001I°Þ7\x0017{¼¨]½ 9\x0006#7Ê$0^.A~]Äx.\x001e\x001fÛxT6~ÿðéo\x001fÎwñÐ\x0013úemXÈÎq«G9\x000c|ë\x000eàW5\x001fîY¹ûéæõù\x0006\x001ea
l±Ö¿,pn¥è9¿SàÎTuÌÂa\x000fú«IS.\x0018ÜsYV.ð[\x0013äU\x0001¾y8×Ã9%\x001cÕ!×-\x0013+,§(sí\x000bÛªñ<ïÙ¼ö«¶\x0010éðUiê\x0014¥\x001e\x0006-¬¿ Î²-èØ2Í\x0004Ñ£¢ÎbëßA<Ó±0\x000b\x0017{¸¨+·[\x000bËndÃ\x0010j\x0016.õpI	¹Í õ\x001fKRrR\x0016çÊ"gár\x000fp	XvÏJ\x000f\x0014åSÔ\x0011aÚõU\x000fçb\x0012
Jkè¾\x000c#­wÛÔªó\x0011Wë<Ýè\x001eþ!g/\x0017\x000b\x001a\x0015i¹çÉ¶~\x001fÜà\x001f¬ÒAäXwÚ²é)II>«_U\x001bL°ÕÙàHá:\x000f%¢áZE2D±%áL×ÅtpÔ-V~\x0018¬ï\x001f?}:\x001b,ÅÕ\x0000CYªúI=uùó»f\x000ekZï.îoîîÎÇ"pT+IP ²2\x00052]`£tÎÔ@$\x0019³ò3\x000b=\x0014j d\x0004;¤\Û \x0016(Öe)+µvçr=Ó|>à¢H\x001aò¹èÆ,£ÝdÜZÉæ$ï¡ü<Td\x00018¢¼\}n|¾íH¡G

$úb(Ä¶ËÛx¨Id%e3Éz¦¤ÙP¶\x0003+Ña¬á\x00055\x0018a
kÂÃsL\x0013±áéE(ãx®\x001b\x001aÃ"a´ËÁ3U\\x0013h¤\x001aìU\x0018\x0004*à²¼T¦ÖÔ,­E¡üJºü\x0005¨?Ûä\x0007Ëù]ù,ç\x000f{|øºõ_þúá|\x0011Rð^ªiL*î0Ö0zÉTíÕ¼úéæêÝbÔ¹ýáõÙ*¤\x0006\x0006=\x0018¨À\gÀDåH5Ä)áª\G ÏPªÁ°\x0007C\x001då\x000bfJFÞèK\x001c-\x000bfò\x001e.×s9\x0015\x00174\x001d\x0001²í¡\x00066h\.\x0007&5ïÁ¼\x000e¬Í\x0002¡þ:~ë@kÛÁ\x000e®Ðs\x0005\x0015W±]¬m@l,÷Y|pAß\x0008¬\x0006=XÔ\x0019I\x0013Ð%ÎNµiæ@ÚÎÛÁr\x000fU`Å¢å½o¥¤\x0001Zð\x000cvËÑ\x0014£øÏ/ÙÚÛ¿ýýáóçÇìêýÓç§ÇOç£ÓCúÒxõ\R»\x0018G6!öÙÛ~¾º¿¿YØ®^ÝÞßÞÜ½H\x0007=\x001dhéè\x0015ÒUº\x0012\x0019;Z\x001aùûð°ÇC-\x001e\x0002'\x001cÁ»:3Ü8×òáû)[è\Oç6ÐÕÇ*Xf\x001c&	¥Îö·Ý-t¾§ój:wÉû&\x001dI\x0008²ñpçÒ\x001e.l«\x001fÖ(Ñ\x0019£
²[Ðb\x0016Õ\x0007ÖrM\x0008Ð#.H;¬ÜÚJü\x001f÷á¥\x001e/mÀ«m\x0015P.¹5ÅBx,A\x0012\x0003ý\x00076áã,·©Yî\x0001ïëÿøçß3Æf~Dî«tâ%BdA\x0000\x000eðÝw7?ß>cÍq®ÛÔ\·\x001a*,w~R\x0007/\x0013\x001e\x001a±s:gg	±'<¶z\x0013¹%ùh\x0006:×%$	ù`Ý¹Ó;KèzÂcË7A\x0018|áàföpi²TÃÉ`ûç\x000eñ,¡ï	­ßÌW\x000e"\x0002%\x0004M\Ê\x0012¸44\x0004cÏ¹¶YÂÐ\x0013\x001eÀ	Âr<\x00027ÓRgt}°*çcµ\x0003y\x0013aì	-á\x0004aô,PfÑÊHµD2GòÓ9[8K{Â¼i\x001fÊ\x000cßrOä\x0002`²L\x00186oCw¬\x0015åðØ\x001c^?|zÿ\x001c^ù\x001fX
Ï2õ­i
qhÏ,àõÕÝ«\x0019<èñ@\x0017Ìrt\x0017<Ûðä\x0014\x0013Þ32=\x001eªWÏp9p¹òØúºV\x0016\x0015"\x000e²V[è\Oç´tåøV#
Öyn%È\x0019Y@º[Ïì½Y<ßãù
ß6ðÖÃ(:o\x0019Ù\x000f\x0017<»\x0013/ôxAW~H?¿­Í\x001c\x0003B:çgébO\x00177Ð¹ûµ&IC|¹PÊ·-AÂ>¼Ôã%5C\x0004\x001aé¼õ,«ýRÃTÚ×©:¹äÔñø^ Ùe¬¬2ÊÞó°ÏìÙÁìYµÝ#e§\x001aãEÔ\x000cä¹\x00010	Q_ÄóéÈiø4:EôõáÃ¯Ï$dÁ×qvù«Ú
¢èÀeX_»EïõêõõùI4Ì\x0006=\x001bhÙ\x0012û3\x001b
v^)¦&\x0012ïÃ\x001e\x000epT\x001eÌ+W©ý¬õsÕ#1Mæz2§$+\x0008{áÑ×Á¹å8464ûØ|ÏælA\x000c±ôðlå0Hµ£[u\x0013Ól¡g\x000bZ6ä\x0000ÀRã\x0017¹MÑèÉ$ø·\x0007.õpI\x000by\x001a¥8Y\x001c¬e
9¬_t_\x000bîÈ\x0004w\x0012y>}úõ\x0019\x0003W¶x×b.\x001aí8Ï"U$Îp.°»½»~Æ¾1\x001aôhÇÖ÷y´h"K\x0003©\x0011zö
[\x000c¢3pÎøN¡av\x001cq¾°j4\x0013\x0004xÕ²|Ñ¬¨QV-îBs=Úq¸ùÒ\x0007­`ÆeûÅ´±;-1Ý..ßs\x001dÇ/pQ7aõô4\x0003É×H$Y\x0018=å39´Ð£\x001dÇ/}MË"\x000bZ\x0013© JiFËæÜõa
-öhÇ\x0001æ\x000bht&eÕ²ôÄ{\x0015´}\x001b-õhÇÁå\x000bh!òËù2Ê¿'pÖ¤Îsï\x0015sd¹'ËÊ­\x0016/ÙnÀ3rb\x0015¨\x0012\x0011KLu\x0001/\x0019Ûã÷\x0005²rw\x000e¼hé\x0010²9.Û\x000eÎ½\x0004Ì±@é	Bªs
M_sjdçîS`\x001b8Â_ò\x0003¢ï\x0008hmÛimóë1Ñ,Úà\x0006¬Ö\x000f894àÐåÈÂæúzh=Ûà\x0007¬Î\x0011Dk¸û\x0003\x0010m­ßZâ\ù¢!îZ·Á\x0017X¥3He¯%þ¤ íeÉËk¢óv\x0017Ûà\x000c¬Î\x001btWfté\x0012$Êe?5NÓ£
ÎÀê¼A4FÞ\x0011éºv©jôÜØ\x001cÛ`s­ÎèÒv«2YÞðÓ:m7ù¤Éíù¤06Ð¶\x0008®
f\x0010[\x0012¥¢lä\x001aï²ÝèEUË\x000f}{ýþáéÓÅýÇ÷OïÏÂ¿oÕÆå,THí«RÍÚG½~uu{wqÿæÕÍí«ð\ç´xåÖÇ­ª¦ÜHyí\x0016áÒ\x0007+UCç{:¯¥³å"xñâeæñ\x001em2\x000f®¾iðB\x0017´xÅò¼\x0005SB\x0011n7RIîýÎÕ=^Ôâ!H«)¯«Í\x00159´Zr\x000c+\x0019$
^êñ\x0016/<¿\x001a\x001aßÇSo¬è¾c\x0008+ÇV{¼¬Åó¡õ0¿t|p³­£ûö^\x001fÎù!4,V^¼Lâ\x001d·?NXS\x0003\x001eª7_{2,W\x001eärhGw\x0006Ôñã´H\x0018Ò"_+áãsp¡xÅðì\x001bÇ-Q$Íú«Ã»Êwóö%4èÑ@æËºñT`X\x001f¸ÜUÛ\x000c-³\x001a:MaOºEQ\x0006÷PdÉcÒ¢Éí¦ñì!s=Ó­
2\x0011Òü\x000e9´\x0011Uf\x0017ZèÑr§\x0005Q½¡ïÉ\x0012h\x0010ÛçÄ]\x001b-õdIù9Ã¢«Àd ³éñ¬¿ª¾V\áx<Ë\x000fÇYË\x001f\x001e?|yzxî=¿\R«*{ÊTÃ_³Ñ4\x001b¥Æ 3Ë\x001fn^¿½½zæmF\x0000¡\x0007\x00045`GLU\x001cKÎ¶ÕA$ ¥3wÃi@ì\x0001Q\x000fèêÀº\x0001\x0018Ðba8÷¦?
èz@§\x0005´4k±\x000eQMü\x000eGVD¾ÆÞM¾\x0007ôê\x00154ü°O+èero\x0012ià²ççÓ±\x0007ê\x0015¤dpn<J59~\x0016!À­{\x0010üqÏ?©zùéñÓóE\x001f¬?ZÁTL|bwîùü§»(ûßüIÝË\x0004`AÅÌ\x0018\x0019Fdx|¹P¹rO\x0003b\x000fZÀHf¦êTÆòµ¹AÚµIå\x0000ñÌ'\x0006t= S\x0003B­\x0017"@
X\x0004Í`Ù¢gRÓ|¾çój>W§ø\x0012_ñx¦~á²óä\x0010sµãÓ±\x0007j@oX#µX\x001cùÀ\x001e9!U\x00160lýÀöx¦«ÇòÏ\x001e?~F7øÜ\x0015-\x0011=K¸ÊX\x0003tkw´\x0012$ü|wsÿ$ïñHW\x001b#åÙBä\x0008¦Þok¨\x001cCj·ïõ\x0000f
{6Ô²ÕçeÝêø0b×tt«oÂól®gsJ64r53\x00189u\î\x0018-k±oÙ|æµh®5C\x0014U\x0003D[MÏÎÃ\x001e.(áLIAËP\nù32\x0004½]¿fÌÂÅ\x001e.jáòrñYV.\rÛvPa-VgK=[Ò±\x0015Á\x0012Ë«spË%È¶ºZ$>\x000f{¸¬KÍÂÑKn³+YV\x000ewN&Ì¯QÒ9à'¨ÅÔt\x0000HwØ·nvô\x000cJ×àøgY8)\x001aNé £±ª¥\x001b|U:\x0007\x0007Ò8L)\x0013¾@¦âMeåp\x001fÜà\x001c¬Ò;88,\x001d[V¨Qh«Ûy¸Á;X¥{pæpZ
HÐnCnO\x0002n
¶°J\x000fá,HgN¹J§\x0016ºVå6Ð
\x001eÂ*]\x0004ÆÜDªRk6±((´«uþót°J\x001fQfë¥)\x0015¼vNSq½\x0015f.\x001dÝ\x0016iÄùXîúþáâîáËãû÷g\x000bé¡q\x0019<\x001b&\x001f×VE\x00082ë&\x000e\x0003;»BºWW\x0017wWoo^½:[J'Ð\x0003\x001a0¸Ká«!Ô2RDSÃjQ=\x001enÁc\x0001\x001cOÉ=á~6*wÞ	èz@§\x0006Lå\x0006!^&¢õM\x0014VÓ\x0001
@ß\x0003z5`l]D>Õú\\x001aÉ|¶âå£RÎòÃÑ\x0001¹ûøùá¼¦!=SÈP\x0012¾s¯¢GQD\x0017×ËsïÞÜ_½\x0005=\x0016¨°l}ÃK4êIìx½Äuë·ë9,ì±PU"õÈT¦¥DÞ¸P­·îÎQ¹Êi¨¬_$³\x0008ÚdH\x0005oz\x000c{¾¡ï±¼\x0002ªu<BqU£IÒÖ7õ\x0014Î\x001cVè±\x0006D\x001eyk\x0005¼¬¾ÊÅÀyâi×Ù³TâèíÐ.ÊÀ?¿øõñâêë_¿~þòxñö÷_\x001f>ýv\x000e-:ô¢JcÂ
OÜ\x000b¦ÉÞw±åÏ¯®®o.®Þýð\x0004FßþøæÝÕÝ÷/ñAÏ\x0007j¾r\x0014kÍIá\x0003©
sA\x001cÍ;\x0001±\x0007Dý\x0002Jo¸)öG\x0002\x0006þ¶\x0001L/½Ïõ|NÍWÜ»qíí$\x0017\x0003b\x0005ÐÚ­Çbr¦ÉUÀï\x0016eÛ÷\x001f?E#\x0019\x001dn!¡´Ì#÷ÒA\x001f0\x001f}·Ú¾zóú%&è@ÁDÕjÈL(õò>D½ÑÄÍPØC¡f¡"&¤	\x001a,ÐN\x0003w)i&×39ÍB9.Ú\>^D^¨pøz'\x001b\x001aÊ÷P^³P5$³`¹\x001c²Ä>r#HÛ?\èyfôYëÚPÉx¨99|ÓP±
(e2²%!«Ê\x0014åjR~Þ~ìRÏ\x0014L\x000eyÚµdP\x0017&\x0019óî\x000c8¡i¢Ü\x0013eÍ*9¬*DVZ¡©ÇX)nþt]e>ëíÍ¯oTTòËs\x0005­äFíõ7T£\x001d×\x0018rkä¶f1UÕ ²VMÂí\x0006Ê\x000eÜjL9½FÕ\x001bõýÔO\x0019ì>¨¡)©\x0006Sn5¶ÜXÑA¡\x0016{®&¡yY«Ókj0æVcÍ½o_0Ä¶VÀ¯Ûe­âöµ\x001a¬¹Õsã¥à¸\¬¹ê³ì++-»}{`\x0007n5FF~ñ\x00195\x000b@kÕîÖn\x0010úVR
FÝj¬º	R_l©r\ÖJ\x001cÆy³T0X\x0006PYÄ
ke­Zøîe gY+ÜN5APÅSMFÞÆÀZD%ThPÛM;\x000c\x001d4\x001d¥¿ÕÚ$El]¬àp»aÁ\x000bÆ
û\x0017§÷m20¾yf\x000c\x001bÜ¨¤J?\x001c®
×ï\x001f?yú@3½Î\x000fÆ.¦\x0019O«Å\x0010ÄÄÞ{×7¯nîßÞ¾¦©^ç'c\x0008\x001eôx ÅË´ßRMÏb½®É²»Ó°O\x0007=\x001cjábjåÖÙËHJO"f\­îw®ëñ\x0012o&\x0018/¶\x000f®½bÆ\x0013«¯Ãó=Wï<É\x0017OÍ¯L£leñÒI\x0004¦£\x000b=]P/^9ñt.XþÄgä\\x0013«Ã=^T\x0016ý\x0018J1³­Q¢oûÞz¼¤^½,Y}S>s1ö¾­Þ^¼Üãeõêe.\x000e/«\x0017E
«ZÉ¾Ñkäøîb2»|àZNÊ¬.~µµÁø´oùìè3´NDu\x0013?\x0007ç ý¹>´äNðû\x000e\x001dì²Õ\x001af/=DåãrXIoqß
n0{Vk÷È²°<"\x0019>+y\x0003l\x0017v~ÜálXíáX$a9,7ÕÔP36Ã¼ÏÛ£ÀÛ."øýá/ùúx¾}\x0008Ê©
2i$H\x0006\x0016r{æÇ\x0015öãÕþôîæ|ã\x0010#¹\x001eÉM#¡ÁCC\x000ez4*C8ÉÝÍ\x0012((\x0002÷2[ã¢ÄshD8rz®CJ=RR ÅúÆUk2ë.ÒÂ\x0013g\x0000§ûi¨3³¨3³/"Ð\x0008¥r\x000b5mà4°d\x001av·ßÞHåúl\x0017(¡ÁÓ9mH|%u0Ë4lo«Øß`\x000eN*¦rÙÕ®í¦­\x001bÜ\x000e\x001bÜ*v8x)	¡3'Û©;tvó~\x001av¸Ulq*¯äPÛ;\x0011ÝCÑ	Ë¬mL0ìqPìqtmj\x0014µçW?S.v²­ë\x0004£\x0005Wìqª-u\x0002~äCç\x0005Ó\x000bÓ$Ò°ÅA±ÅÛ»cAòâUÊ÷jËtúþ2Ë4lqPlq¥+gj!»\x0015Ìm;å­æ	-\x000e-^EÖ«¸çæ¶Â­Ømõ¾8lqÔqlq2MõäýdC+[?ÍÍ2
[\x001c\x0015[Üä¶Å£J\x0016&{H¨l^§a£&LqËÃ\x000bO-ÌIÖ·ôæ)\x001dÍ(?\x001c¹ï?~øëÇ§óú\x001c¾\\x001bäC\x000fÒ7§ïß¼þáÍíyat4µpÜ,N0vaà\x000b\x0017Ç¼!6ÅÎ$#^\x0000²æhBHùá«µg?<<3|)x[\x000b\x000fudmV®1!^¡kÝÙ\x000fWçGB	\x0015ôTðÿ=Õq)qÝZ}¥¾ÇÇO\x000fïËwüüù¹RZÆ6à7\x0015¡qNDB_z[8a{G}7wW¯Ê÷¼¿\x0010zBÐ\x0013æÖËBÝÌ|µòór§)/- ö¸\x0001°ÊZ,KíòçEôÞö"º\x001eÑm@MÖ½§Ù\x000b";l\x0017ã1Ó"ú\x001eÑo@Ìò
\x0008%lNT\x000fbNüÊC¼\x00161öQèëä\x0014\x001882)·|¹ÑàÀ½©GLzDcDD\x001a×Û\x000b¯DA.zR-bî\x0011³\x001e\x0011Ú\x000fxÛ^OR1
æô	SØõ
\x0019×Ýq\x0015Ëèºùå¼à\x0012,±=IÇ¼×êØÑpë-7UU³²%2¨Ax0¦­ãÞób\x0007Ëm·nÏsH-P\x001d\x000b?öx\x0011vri·Ù±e´zÓHµ6ÂØúÖèPiL°×zw½0Æu×vÅñÒ½\x0006å/\x0013ï,.¾¯k\x0019\x0007Ãc7X\x001eLm;B{9\x000b&¶o}ú(ªdáXÃc^^÷®ÂèÚ:îv`vôgæN\x001a93aqË£·¼³¸¼ÛÉÀpf`Ã!\x0012FÌ¬\x0005P\x0010¥;ËåÝG\x0006#\x0003\x001b\x0012sS\ËÏUTq,nwÜþíÏËý¨ó×ôÚ×`om$\x0001%,Ä×¬\\x000ffIíq¿í*\x001f¾þûÅþü&¤§\\x0018AÄå|:i·âe®ÞýËÅ7wß=#ÛbÛ lWÿ;\x0015åÖbé\x0002re\x0007ºÓÚy¬Ðc\x0005
ÃK©¢qr,ÚMÅ­t\x000bÌ2¥)©¼\x0000ÑR\x0005¡v;çÂ]Æê\x0002-Û\x0017Îpy¸ä\x0017³løV\x0017ä£[¹ÖÍS
ÛÝªö»Çe:Í\x0015.¥\x0014Qb\x0001'GqjØíVµÝ]{;.@¢ú`Sã+\x001e/rñ\x0013Õ!\x0010¥\x0004þ×øéá?¾úãÿ<Ýp\x0001X\x0011Û1Ù`þðzN\x0013Ô5½ñÓÕÿºyu{óLãøñÓöó\x0011äXZ`Á½ìe6R\x0001<}üP\x0002b\x000f\x001bÐÈ÷-´~,\x0005LÜ>pê¬t®'t\x001b\x0010/\x0013\x001b\+\x0013WÊdh:ÙJ>ßóy=ÏÜ9\x0003¢}{ÞÊþ4®Óñ/lX¿p8$éÝh	ðdýN°\x00120öqÃ\x0016´REß:µ|û¾Ã\x0008ÏM|©çK\x001b\x00160ñh½¥Á\x00069JjEâ¸\x001b0÷y\x0019ä#L\x0002Or%«áÌJâE\x0005ØùÚáá~0äCYB'À\x001e|ÌJó\x0012qt%[|I7\x0005KÙhö%ÖµU<}ÏW"\x000e¾Änp&	û\x000e&îVðØêÌ2îE\x001c¼ÝâNZû=*L¼\x0017­mm\x001e§¨\x0012qp'v?!U\x000féË-3­¾Dg·!9ËV~8\x0004
÷\x000fO\x001f¾ü??=|úõñýû§gjÏËgf{\x0003Ññ»H\x0008òJêáô{uûúmá»»¾yõêöl	ºðaÏj¾P)ºl9Ruò<é­9ùÆJ@×\x0003:ý\x0002\x0002O\x0013(\x000b\x0018ä2Ô2¨rà>>ßóyý\x0002Ê]
h¸õ\x0003á³§%\x000cJ¾Ðó\x00055_Ì2«
¨ÉoHAn\x001eN+÷±\x0007[\x0016C\x001a"±C«!ÉÅ¹\x0007Ìz@¦\x0016^
ÖB«÷.[pç\x00119¸d\x0002<¸äù3¸?¾|ãÌÒ½9D'\x0018Nr}JÂÁÊX½!Ý4ÎFÛÖÐJQº\x0007{r3Q\x0012\x000eÇØêÏ1æöT\x0013c;'VÊÈJx
%cO\x0002ixÀ~ûûãÃç¼\x001c=zH\x000fa\x0006&\x0017EÞ\x0001¬åßþxsõö\x0019\x0007\x0007Çö\x0019Òð&ü"\x0016\x0004õIêÈ±lT%9ÈkoT¡§
**l\x000eÊÉeEr±\x001eÖPÏc¥\x001e+i°l|<uòÌXÒìå`ånù"Vù¯:Î½\x001c\x0004T¾|YÈ~úøáËÅOÏÔ(ù\x001ce
R7\x0015ô\x0014¸pò%ß¾]ð~zS\x000eÀ»ó¥J\x0002\x0008= h\x0001©ò%sn\x001bhüááêøÞ«\x0005Ä\x001e\x0010õ+èdx
Ð½<²\x0005n×¶ûÏõ|N¿2/ÊÒ\x0008MyÆÈ©U¿Ø½¾\x0007ôú\x0005l\x0019@J^Àd[ÁA<>\x001eZÀØ\x0003Fõ
\x001a8\x000f\x001d\x0002½ÚóÊI\x001c5\x000bXî»ã!¦\x000b0\x001dâO\x001fÿöøáá·z\x001fúïÿü¯«O¿þþø?þùëïüóÙ\x001bG`±bÿXÈ ´$V	û`àîÍO7¯¯¾¯×¢âÊ~¼ùåæ¹F\x0012{ÜHbk.u\x0013l¹\x0008±Ú«É±Úm:ØÍXÃP»½\x0015{VÜÌjåEÕdÒbà3$»
c\x000fÌVX×ÃºÍ°å®\x0014\x0018¶\x0004\^(?GYØð-vAèaÃfØ,#M¦äR½ÅÇÜ\x0004¨|¯¸\x00196ö°q;läÉ\x0019¤\x0001/f¹1Ã ©y\x0001<\x0018²«¬=1\x0007\x000f\x0017ß?ýõëùx£üÇdMË\x0015t\x00110XæQ±¨-©îá9Ì«ïox÷\x0012bWbOpòù_B,K=èßW:ÌmÊ¬\x000bèÎ\x001e§9@\x001c×\x0010Õk\x0008åûÖ\x00163C]oP?5HÝ½w8¼.j\x0010\x0001l~ùáÈæòã×OËØ?~úòÌ»^¹H.qÝ]1£iW\x0017³¾#KxùæÝÝ2½àç7wo\x0019?GFha#­*r_hnZ,'R!]?íj\ìqqëâË\x0017÷òñÒ,\x000fíÍÊÅ3>Jë{\¿\x0015×\x001e¶´º\x0015×fy¥tÅV}\x001bÜÜãæ¸X\x0016
Çzgæ0ÔoÌîmí2,È\x001e[h1Épd4â¢:*g£\x0014\x0017ç¡r\x0007¯\x001bxÝV^\x0000¹\x000b#=øs¿Ðú°î\x0002Ô´a 
[iM4\x0016KTÇK¥>íoÂ\x0006Þ´õ¨QS4_úJPÀ%ØÞGü¨´°\x0017Ý\x000b[w/åÏ]âÝb\x001a ®\x000fæ\x001bñ\x000e»\x0017¶î^(×\x0017+)9'oµ\x0010°¥5ÏZ^\x001cÖ\x00177¯/¦V\x0002\x001c¬¨\x001f\x0000Â!QüxõÅ­ëkS\x0014ÏF%]</×\x0006'®b\x0018I·w8o¸õ¼Y\x0017ÚÃ³±Ká\x001eñ\x001eÙ[¿ÓhyÝ\x0010ç¸­\x000eU	åÔ	?NÐU4­jÞa?¸Íû²lÜ\x0005OÏÈ¼rgDï¾Í~p¿p[ý\x0005é4:N\x001e,9#M»çÍ8sq¢ô»_¿,Wë÷üó?èúù ÁpÛ^ôüéZ"m\x0003åÝwo\x000bÄõÕ«½¹{
z6P²9HÒçã!	pIÄÑâ \x0018¯s=Ó.iò¼¤PÍÏZ\x0008õ
©öÐÃù\x001eÎkál{s£ñ1\Kíá7ÄþpëáB\x000f\x0017p\x0010Û"zw@öDI,{\x0018&Qêáb\x000f\x0017µpÅ­#\x0007¥\x00146µëªÀõQ-õlIË\x0006µE{Ùr^Zó éb\x0006x»\x0003.÷pY\x000bWnH,ùèôØ\x0002i$T6oö\x001c^7Ë,W$\x001d\x000b\9I]Fuîd\x0006/c°{¾ª\x001d-°Ö\x0004Ó¤\x001cr\x0013+\x0000+©Ûr+{è\x0006\x001blµF\x001e<Ø?!\x0002£\x0000¹\x0019á¾½MO\x0003\x001djéLS¸wÉ,29Dgd°}Áßcèìà"¬ÖGP7	²\x0003C'*9-Xb}ûnð\x0011Vë$ÀHÇR\x000f#\x000bpi#l°\x0017»ÓÓ
NÂj½\x0004	ñóÀÎ²Ã¤Ûdi\x0007(¶n\x0017Ýà%¬ÖM\x0014\x001a]±Ê£g/âüåOì¢\x001bL±ÕÚbdâ'sj¼âJqÓêtI=u\x0007\x001d\x000cÆ\x0018Æ8$ï¤ÌÞ\x0019Ï¥\x0019©I@Ò0=p1\x0006¥1\x000eeÉ@\x0001çQ\x0016_!\x0006ÅôÒÅzº1 V\x001aã0\x0004\x001f#[$)¢<ï`v}ØÁ\x0018Ò\x0018ïfÙËºÂYßtRWüò÷¸1\x0018L1(Mq1\x0017F
ù0yëR4r\x001d\x000b\x001e÷\x00040bPâP \x0017¦åHDäJ	¥ÆäSöÐ
¦\x0018¦F­-Ý´v!Ê,Û â\cc\x001en°Ä ´Äå@¢\x0008ÞÂ\x0012\x001f	\x001f¤àß§´ëH\x000c\x0011;(Cv¤Õ\x000e½a\x001fBËº!ë¦§\x001bü\x0004(ýDÙVAî°@*\x0006u\x0010°·bì|{â\x0013\x001cü\x0004jýDäGå=#òàÓÐÚ$\x0002Ø=\x001f\x0016\x0007?Z?\x0011 p'\x000cD\)/sÐd\x0018÷yÿÇÁM ÖMË\x0003!§}vRØ\x001fì®È\x000e\x00077Z7áiÂsj"8<Õ\x0019y\x0004ô¸ëÄâà(Pë(Ê'¼ßy¬&¸¦rë3î±v88
Ô:
_ì	ñ¡§_ÏcÅ£\x001c
\x000f»,\x000e\x0002µ"Û\x0018Ï\x0015§RoSíC)òÑí¹áà)Pë)¨ß\x001biíê=;¡·­\x0012Áï	ípð\x0014¨õ\x0014Þ\x0005\x0012x2\\x0010E\x000cïv]wpp\x0014¨u\x0014\x001a\x0012¸6¾»\x0015@Àt£p£pZG±tÙsõc±-µ-±\x001cöa#ìù°nð\x0014Në)\4ÑµD±¯tñÑîJwºÁU8­« Û«Ô\x0006;m=±è Ù0dN\x000f7x
§õ\x0014ÔPÌ
t$á<û<ÅÃ\x0003ÀCáÆ\x0007\x0000­§ \x000e_\x0015ÉSÈ¶sÝñy×UÑ
Â©=E	¸f9e#\x0017\x001eÌ©~YÊ¯ìñ²nð\x0014Në)h|\x000bw\x001ebmíH¶°+Bq§pZOA2}ü\x0008²4\x0011'©¬Å}ìqcnp\x0014Ní(² =°ÊÜâdEi3EÜõa\x0007OáÔÂe¹g§rW­\x001dEDkv=(úÁSx­§\x0008`D\x0017¸²µ+VOlÊ¸'zò£ðZGa£ekWþ9°<AÌÈ!@\x0004Üµíüà(¼úN\x0011´º\x0016wÏïÙÉ;IÛÑUc\x000fÝà)¼ÖSPçY½gÁ*MOkgåÈÏ»Önð\x0014^|ö\x001cI3	9ãÉ!@´y£ðãS±ÖQX+µØ`ÊUÖ/"¦ÀA;\x0015í	\x0001üà(¼:÷Ä\x0015Ë´ñÛ	É1\x0019jÂôhðZ/a}\x001d"W\x0016\x000eBàö­,v×\x0018Ü×gÚÀÉLï'ué¸9Ú]\x001f|×ú\x0008SÜkMÙ¡\x00081Éô6Z¸=\x001e,\x000c>"èÓN¶\x001dV'e©Äºxéü\x001eK\x0012\x0006\x001f\x0011>¢X1Ë­rQ2vô±+\x001f\x001aÑôp\x0008Z\x0017\x0011iÀbõ®¹\x0018áZ\x0012\x0002ºÀ+çÂ\x001eß\x001f\x0006\x0017\x0011´.¢\x001cwîC(Kç¸õ6&ÚÚÁ3\x0011\x0006\x0017\x0011´."BÛ©.Úr¶Sè,æ]k7ø õ\x0011&	]Y;»¥µC\x000e×'Ûµtc9ÖEÐ8Ãz
+wXn&K(ÚéT·Ë\x000cN"hÄ2iÌ¶\x0003[\x0005­k\x0018=t\x0008Z'AïþÜMf=òrÑqâ`1îÚu\x0008Z?A}W5aWÖ.ðtbvb÷¸ÿ8ø¨õ\x0013KN\x001d¬1Æ.WXÙw°+ä£êË\x00044,\x001cbÊ|K>Å=û.\x000e"j=\x0005M`áÚT¶`­ì,Q2µÛå)âà)¢ú2á¯ÿà¨ê8I`Wá	»np\x0014Që(¨dsb©MÐLäÒ¾I^'\x000e"ª/\x0013NèÀ9ßî°ÀB¬1 ì¢\x001b<EÔz
Ûºc
xêXê\x0003¿<Årx÷Oq¬<Uß'ÅõÀëý°1[NÅÆaì­mp\x0014Që(l\x001b3\x000eÔ8\x001c<EÃßµ¸=+\x0006S´¦ØRvâ\x000bL£9Ãb9I±KZcgËÕÕ1]6¼é,\x0017FwU¤Á$­9¡!K5f\x0007z;±\x001cÈäµèÒ®ì4\x001cØ¤=°Fô&Þ\x0013se³Ü%N3iv­ÜX­=\x0012æ\x0015Ôë?\x001a/÷(S´iÖì¬N\x001eDV\x001e	³ !\x0017ìPW\x0015´]Õy8\x000fYy\x001e|.²Î\x0004êû´¼p-oâ÷Yá<\x001c¬<\x0010uê # ¾Éêû¸ÉìÉ\x0010çá8dåqðT`ÇV\x0018r\x0010+\x001c<Ë¼\x0014¸°Ç»æá@då(ßÕp{\x0002+?ëÕï*>Â{³ã@X3\x001c\x0008ú[í9ñ¢à\x001dÛ»÷a\x0017ÜXdo´>Â¨o:¤4îÙï÷aOØdÇN'ú[%\x001dsò%EIÆkÛ.ìyq²c7\x0011ý­®l¶è\x001b\x001d0]vþÛ,^\x001añÔ~";ñ¢n\x0015)bv\x0014{Ô\x0019£m	ÔW\x00199-\x0016ÜÐ&<j%âÕÛs.O´Ý'd¦¿mòr0²-\x0005°'mú;´
\x001eÁçh\x0016\x000b\x0007N²;4z|\x000fÞx2´=\x0014ai®[Ïy'\x00169·\x001bpÛâù:®ã¡(\x0011ä øýáý?\x001e¿ã¢JqéÚ%tbý§¢MÍzýÇ«W¿Ü¼}	\x000bz,P`EËµ8ÉYÔfØä¥\x001c6åõ«õ\x001c\x0016öX¨Y­\x0012s\x0001Q¤±Ûµ(Y©H$ýíX®Çrªè¥\x0005\x0012ÿ\x000eø#J\x001bgÆõ^9,ßcy
\x0016Jan¹ØË\x0014±ò+·
ålVï\x000csT¡§
ª­e¥9¶ÌCÙZò	ãzÈ;G\x0015{ª¨Y+Êªò'tÅs\x0006ÞY"\x001e©\x000el3Vî±²rgq¡fY\x0017ÑðO(³FÉ²mÆêü¥Ç£NÒ>bÒÎGeA<ÌF]WsZ¼Òªµã\x001a­©ÆFî\x001e-1\x0005\x0014¥À×ò¯»\x0003i°¤VeJ3z\x0007U¹j³ràjX.*;>á`³¬Æh¥CW!%í¹5g®(,Ðo·¥v0ZVcµ¢is.S3\x000e¦A¹\x001d5Ø,«1ZÉ\x0017£ÅkÅ­ðJå\x001b¦õ¬Ú\x001cÖ`´¬ÆjÑ7Lí½Ï[ù
kÇO\x0003UÒPQg?<àòj\x0005¹ý¼^"=Ç5ØR«1¦ÅÇ\x000eTvUv¸¤Jµ8¦\x001dÆ\x0014\x0006c
\x001acÈ
2\x0017Å¦±rImo´gÚ{æ¸\x0006c
\x001ac²ÊÔLµ¶råVÄàw`¡©Æ fr^0gq\x000b\x0016õ¨Jqà\x000e\x001b\x0001Cl
à4QvÅ¢¹¼ëc¼¸^¶05ØyÐØùG:\x0002©1-Èæ¸HQ_:ã\x001aì<hì|¢ºçn7n
HXÜZ¢û\x001d!3\x000c\x001e4>cæ2\x0000 G(SÏ¢
(«\x0015óÕ\x001a,=h,}&µrä¯h.ù#bÛó\x001e¶§0zÐúÌ³V	ËçK>­\x0008\x000bÍ£8XzÐXúLÍáõ¶Oâ)ËWd°õâÂÁÒ£ÆÒgÏõ9\x0005+ÔÊ¦\x0015³`Ù\x001d\x000e\x001b\x0007C\x001aCO\x0015¥åhå\x0004Ï"®×GÌQ
v\x001eUvÞË4
 }\x000eù"\x0018Ñ­'3ç¸\x0006*ÊßÄEb:iá\x0002#¯]Ö]ç¸\x0006\x001aIô4ðHª\x0005\x000b¼¼\x0011ÂzEä\x001c×`RQeRsïô_\x001d#HNÚáv\x0013AEAÍyÑÛ *tuÎ7 PgÚ©æ¨\x0006{
{\x000c
há×\x000f\x001a¯P×
Ñ²w.îà\x001a\x000c**\x000cj2¤' \x000f\x000b¦
Õ&o5¸}o¹Á :AMÖÕ\x001eåY¼*\\x000e¤Åy\x0006ã\x001alSØ®T\Íò»ìùT¥\x0018Ê\x001fòN
âa½ÏakQ"F¥|\x0016·%/\x000f¾7Å1ºà·7nL *lj*¿.%/§1U.o\x0012\x0007ÏÞÙíip7ØT§²©Æ¶Õ«iñA"ùE
Û}£\x001blªSØÔT¼ 4ùP]\x001eÖõrIö×¹æ÷9®Áª:UBÂyNÐÓxZEëB¿\x0005+ºõ"Ú9¬Á¬:Y]\x0004áùe/£DõåãÉö2ëSs\Yu*³\x001a\x001270"
ýãåBQEKhÖUG¦¸ü`V½Ê¬¦V§\x0005ÑËöÇ<vl{?\x0004ª^ÀÌf\x0002}ð[ê<õ*\x0017¡íæÞ\x000fæÞëÌ}{]Dï%ÄqAÇÏµñÌq
æÞ«R\x0012`ùE\x001bI\x0008Ý£É²¿Âv£ê\x0007cï5ÆÞú$×
µ\qqâ³óöPÂeª|Áo\x0018"\x000bÅR\x0016e;S{Vk0õ^eêIÁ®TgjA\x0016­\x0003y÷\x001dï\x001a~0õ^cê#UVÛ\x0015)ÄÉbêy½¢Ùs\x0016\x0007[ï5¶Æ×w
ð6Öõò,\x000fð£\x0012Ù\x001d¶k°õ^ õª\x0003^Ë}Cú&Dâ\x000e\x000f\x0014\x0006K\x001ft\x0001t\x001d&L»+»EvV\x000b½xÆ\x001cwp
>¨\x001eò¢T2\x0015Ëåê4\x0017ÊÕ£F¿#P
¥\x000f:K\x000füz
NÌÒ\x001fjÄü`\x0018,}ÐXúHC«c]/ÛÃ»\x000b¹\x0005'=%\x0008a°õAeëcZRá´^'±P$!-i~Ïëg\x0018¬}ÐX{O"o¼^T\x0017ÌÏýÀ«eÃ¯8FèÂzÇùAÇý\x0019´XÙJù^^ïßÃ\x001aL}Ðz_\P5©He©j¨Gé+LÁì\x0008oÂ`RÆ¤tJíOÆ`«fÔ2-ÓDÙô;ÂÔ8\x0018¯¨1^®Ï5·>\x001efy4YòÙnßôq0\x0012Qc$H)1W¹\x0019\x00199ÉÚÉêã\x001aDT"\x0004#ézgM­"×%ÄÁ\x001d9Â8\x0018¨1\x0012º¸kã)qÂÓ°
WP¥]Y8¨ªF\x0000G*GA½m!áì8ÖPiì\x0004f\x0011½CG\x000bµ\x001eÁK\x0004½\x0018²ÍXCD\x00185T%ôâÏ\x0008è¤\x0019?çìëz-s\ù\x001aóEíuN\x000eÐq!\x00062;=·ì4ÄIUÜd¾\x000c ûj&rr-éµã8¦Á¬&Y¥fT¾6ò¼4\x0012J b{r)
!aÒ\x0015x\x0005.X.hµo,õjÖk]êqk°öIcí\x0017\x0007n\x00193»²sùUZ<ãºôù\x001c×`íÎÚË¶G\x001fbÆ\
\x0012@¼Ðí5XÕ¤«ñ±`åö¥lÉ:hÂìÙ_ùJªr*_k¨(Ê!-\x0011^/\x000c©öÛÕ<¬*[¢®fN\x001cÞ¬Ì`IaGyP\x001ecÖ\x001cÇTÖ¨¦ÆË
YyJ°\x0016$¶;J×ó°í³jÛCûÅd-=ÿKÁKËØ\x001d7¡<lû¬\x000b&\x000c½Â\x0018¸ò¸X E¿.Ë1Ç5lû¬öÚu{Q\x001aË©<W>§dÖå8g°ú\x0006º¥òYå\x001d½]\x0014®Z\x0005M`ÀuÆ)ÙõI&s`c±Qù!y\x000cc±ìN
½e¡«\x0014Óú\x00009°±ÐØhv~\x000cv© °\x0008µ'ÂU®õJ¤÷·\x001dl,ê5ªVà¹z©\x001cI)A3RÄâ\x001e¬±|Ö¨v¾C.p\r_3YêÙ°nÏNØ£¢]Õ?åykÒ$Ú,3³\x0014ö\x0005Û~ï°G%öª\x001a{JØç¶ó9¾"²ñ·ïû£\x0002{U=i[ÎÇ¸ÜØæ
/\x0007òÌÖ\x001cØ¸ïUÕìê@ù;\x0007G¬	8bMÑmO®Ú£ÂqUå8	ºòÚ\x000cH\x0013Nn.r3ÖXmU\x0005Ú>H©*F\x0013dhZL(\x0006Ì®Ot\x0003;j-Ñì{ïQÞ`\x0002Ec[¼¸\,Å\x000e°që«5ª)\x0013@\x001d5sâ\x000c\x0018l/\x0004°cy¯UÕ÷R\x0002·~{M£A¬Bj\x001f;VlÜúªJZ ]¹
fB\x0016cÒ\x0004@3¾¶ÛÖ±dÕªjV\x0001QÞÜMÀK\x0019îÉmÇËo÷cu¨UX+ÔìIHUÏpÌ·îb5vp[_U\x001eJ_µ\x001f\x001cÞ×\x001dfô{ù´®]<\x00076n}U\x001d&©\x0001s­600\x000fjCiËqÔØ±\x0019lÜú¢Ç¨ô¥&*L¹*\x001f¤\x0016\x0013`{@MÝã~úÜ³9ó?èù7\x0019ô\x001cô\x0000P\x0000ò5=å=Ý&Æ\x001fÓy\x0015\x001c³\x0003°É\x0018\x0016\x0019[FÞKï¦Ôf>\x001eYÇÅïÿû?ÿëæó\x000f=»lHCµyÐ¨­c\x001f¨ä*sÃ}fµ½ðÕÅÍýÛ«×?¼ÖõÌå£\x0013lZÚsðªâàl\x001d·Z)ý\x0012éß\x00061\x0000ªKê\x0012/~þú\x001fÏÈ[Ç5£ei\x0002Ë\x0014;ËãvIïvÅ Ý_üüî_ÏÊ\x0013\x0008\x0011ôD0MD©úØm"ò [Êð'4amb×\x001c\x0011öD8¿FT'ZJÔª
6fY"·VD1\x0007äz 7\x000fTÖ¥fL\x0000`]äÅt|^\x001dA0ä{$?DqU»p¶EbÑfam\x0016Ç\x001cQèÂ<\x0011dùlGRq£ ¹µøy\x000e)öHq\x001eÉâò.»,\x0012\x0017ö.c|2#­ÖKÌ!¥\x001e)M#¹\x0012\x0001Ö\x0016¯rþ\x001d¿\x001a§\x0012D\x00041\x0000kþy\x000e)÷HYä8Z6>f(HR"\x0015®Xf
éX¬¤f²Ñó\x0008ÆòÏ|sõ\ÂîSZËÌ1{ÞtÓ¨\x001344¡7ð¨\x000fi'¡uÚºì`»í¼ñ¦©Á¼Ã]\x0006§¶*^§¸ÖÖ5Ç4Xo;o¾I÷¹\x0016\x0018*à¹cÖ´C·Ù4ÙÁ~Ûi\x0003^Ìa\x0012kIz²õ\x001a\x0011=&Y&»Ö¶;Ç4\x0018p;oÁÚú)eÖÝd<åÓm6Nv0ávÚSM\x0014g
	)Öi6Ñ9\x001e¤¸ô7oe\x001al¸7â4&&Vóäh^\x0007K±rO~MJf\x000ei°ávÚ{zª¨\x0014NS=uùZJ
\x0016i0âvÞ®\x0019:Çª¦åàxÌÚÌµ) \x0018L8Lðr¸\x0002OF2¤¡_÷wH\\x0000^<ÍZ×Ã\x001cÒ`ÁaÞ\x001b*]©^rW¬Ö\x001c]íÖ\x000eÎ1Ñ÷´\x0005÷fåÔ½ù\x0001?8ÖB)Hkéã9¤ÁÃ´\x0001÷´ª\x0001\x0012f¦ºL\x000e?]Hkµ\x000esLµikY¹\ÐËR[QsÈ3T|p[ý\x001c\x000c	¦
S±;2Äúoyut2Ó­ ¥Ín°\x00020m\x0005#;0·
à\x00157çåË­ÕN!ápèpúÐyzâl,\x0003áT&'¶)¤Í\x0000Ç\x000bæü\x000e§7ðZXN	À§\ç_{¤#\x001aö7Îïoz×Í|æ\x0019¨¯"\x0011¥
Ñ°Ù4á°Áq~V¡9lp\x000eÂÁ¶Nk£ç
ó\x001b<ÄØl\x0013=T2SK P\x0006{#\x001bv¸ßá³m*\x0001oeC#±DMkU\x000csLÃ\x000ewó;|Q­ç\x001d\x001e"KÝ\x0005o Erk½£Ï3±cê«ü0è`Þ?<}ørqõá·Oüól^ÎÛª\x000bh¨|¡öí$dó°ª\x001auuûúíÅÕëïïn^\x001e\x000e´pÅ\x001fs«¹!5°å\x0018µ´4,\x0011ÄjBSÁçz>§æ+w«*Ég(V¯jMÖ:Ãn×{\gøÐ\x001f­_1=ýúýòðëï$¿z6ºÊ\x0018êÀ©]ùËZxNE5)ÕÎ¿\]ÿxó2ë¹+ÒpI¿`y\Q\x0012æz\x0012\x0016\x001dÖíX¡Ç
\x001a,*\x000c^.\x0011)Ó³®å§-#~ÑÄÕJÄI®Ôs%
\x0017V&ÂÊyMõÊ2¾¹|ÍÕ\x0013ð\x0002V\x0001\x001aM\x0007\x0011éøZmÙÕÓ3º¾¶«Úiå\x0002ZSÔ¤Öë¦wn\x0010·zW-ÙÕís¾&\x001eóÄçýû§ÇçhSÕ¦[C\x00126<2Ô\x000c+\x0013øÁæ\x000bÓ«W·Ï*
3\x0016ôX0\x0015H§Ó²ý\x0002\x0011©%«ÁKeÝ0·D=\x0016*°r\x0002I	"\x0018ÏJ_%\x0003!TVbù\x001eËk°\x0014L
µ.°djd°ixQbÅ\x001e+j° pc¾¡Iª<-*QÝ\x0015Ä!½ ÄÊ=VVî­Ä\x001fÆ½\x0005iûjÙñ$*b¹?ØÅLÑ\x0003VÙ\§ÍRy\x0013s
=Ê³\\x0016,X\x001e ¯>ýúûã?þøg1¨g=6©Np;-ÿµÚe¸¡!@Ê'ÆëâÕÅÕ]±§¿Üÿó\x0012 ô \x0007t\x0014\x001eVC[7"Õ\x000cñdñTxØãáõ³qmù/\x0013ítzõ\x001b^'ô¾\x0007ô\x001b\x0000I£¼>\x000b8¯\x000e\x0014*\x00190Ø}\x001f8öqË\x000et<|Îäbå2¯ oÆ×\x0013s¢\x0002Ì=`Þ²µÖLP¥Qi\x0005S\x0003<ñYs|pt_¡Ì!\x001fáï\x001e~ýõ÷¯Ï=Ép\x0017Ê±­c"\x0012µp
ÎGçâ»«ëë\x001fß·'pt?!\x0018	¾Áxä^­âß9ÓDs\x000fâ&\x0018ìap\x0012ÆgÙN©&\x0013@\x0014é-*IÂñ²fÅ¾^|÷ñéóÅ/üó?}8»}2Mhå"\x0014_ó:²¡"\x0014â.ß]|÷æöþâÿuûú%2×9
Y2¯;>ÕY\x000bX\x001fËA¥¸t;YèÉÊÄªzs(¬eyC\x0019ä\x0011â8\x0004]Kz²¤#£.£*w\x001dl®9zJó\x0013TH\x0016w|Í®0¾-\x000fÒ
´\x001cóÛP\x000c)Ôj'4¢Óüð²9@náã<~:n¡ ß\x00083Ð$ÊÅ¾\x0011-\x001cÆ7ÿzs÷\x0012ëAÜ\x0014H\x001a"Kï\x0019<\x001b\x0003"HZÇâ\x0016Ð9\x0010/»V¤\x000en. r-ÃQÊm\x0016$õ i
$\x0003\x0017®Z:kÜ	EÒ
\x000bz~ûæ¶}_"	ü$°$þ6\x001b`äØ=KÇq1\x000eqñÃÅw_\x001f>üöøéé|Á=R{_Ê}\x001e/}ErAÎ¸ÃÓ\x000bÎÅ««ïÞ]½þþæîö¼ÇÇã\x0018x
®,RÍz[RHm\x0008Í-þÏ¬Äs
8ìáP	gÃ²\\x000b\x001c¶Êv/Á¦sq%VRÀ¹\x001eÎi?«ÈùX+É]Z9®h\x0008c\x0011¹í8Y-Ysýð¿'¢Ò¸:e\x0002ÐJä\x001bdØ'U>\x001dí³ë«?ýéE\x000eè9`ÃÕY|\x001eRÀ1Dà'÷ù)\x000cì1p
Þámãð²\x001e\-´Ãõ\x001cnn9\x0012+5ÒÔ\x0003×IßEÎÿ8Xf\x0016Ä÷ ~nAì\x000f°r·\µÃoÀ\x0008=FÃ\x0008]&\x000e\x0013«j\x0018qx9ÕáØkM¤\x001e$M$Qhµ¤&x£\x0010Q@6`ä\x001e#Ï­Gó\x000fËþ\x0000^dÛþ@=Hç<É~¹\x0005q\1bI<ózÈy\x0019\x001fg9F;6gÈÊáy9P.\x0015A¾,HÈ\x001b\x000e\x001d\x000c³d¤zÄ 2hHR[°ÁØÁÙ9cFe«lÌlM/×o#7lYÁÙ9km}÷¢%1m·J9AY\x0012¿áØØÁÙ9sÚÀ.°Fº¥ÊÇ²$nË\x000c\x0006ÍÎY4ª´â8%G\x0019i\x0016bn¡À\x0003\x001c\x00078·$Ü4l©\À²e¥\x001eS±¬[¾Í`Yíi
Æ±\Ø²"À»$\x001dÂJ
$qµsÖº§ÅÛÅÐ.k\x0012ÛÁÙ`Ô`0®0e\\x0011aä²$¾jÄ²;DÚ[H\x0006ó
sæ5gÖ«~5ÓÜJd²a¿Â`Õ`ÊªNa#cóR·%.g\x0003È`K`Ê\x0004#åÉçöqßpp`8Á0uµ\x00151r¥\x000f¹\x00195¿!HáÜÀÔ¹	Vô²ËvÍ\x0012ÅGÓv+ª@Üñ=ÚAÿ\x0002}ýð÷¯¿>}xæÝ+Btfb`k¨°/ö1­<A__ýüîúöõs³xïÐ\x000eú7èÁ\x0012zb[b\x0004NWG\x0000Ù;kïÓ\Øs¡Ë¶2\x0002\x0017\x001auÐÒ\x000e{À\\x000fæT`å¬ñ\R\x001bj	õà¥¶³òÊëø4Wè¹jÈ¯\x0003fÖ1Wpb_y\x0006=XT%\x0019eËÞ2à¥ïÔ$±\x0006,õ`I\x0005Vn.Üªk1sf+\x0015*z\x0006·å\x001e,«ÀÊ¾bsn(^åO(©âqN°\x0012¬\x001fÊ\x000e´ú¤\x0019;Q°VË
Ê§FvòÀ« \x001bíëÿ\x000c¬\x001d\x000c¬UYØh\x000375³ÜE\<²|Ì+\x0015\x000fÓ`µ*\x0013\x001bç\x0011ª&f0w\x0000²iÛÁ\x0006\x000bkU&¶ü?A¸7ðÂE![+õ&ó\x0003×}Ëª°¬­.\x000bò1Ãq<®"\x001b¬¿Uÿà2·=5dsrí\x0012á´p@A6«²ÿÅc²Ø5®ÊöÐY	Ñ\x001f¿i¨È\x0006ûoU\x000e  HµüÃËZlZv9\x0000>ïùý·*\x0007PäcJ|Æ\x0005Å1É\x0001pk\x0005³d08\x0000P9@Ò\x001cÙª^Bd©eÙN^1Ud\x0003\x0000\x0003 WÞÀ\x000f\x001aX!i\x0016ýãZ²1ÂV9@wx3Üò¶@`¢mQ\x0002³\x001d»\x000c\x0006û\x000f*ûÿyÅ\x0006\x0007\x0000*\x0007@ZcüDm\x0013cæCnWüã\®lp\x0000 r\x0000¡isZúÊý÷Nd´J0{µS
\x000e\x0000tñ?¢Ì¬¶lqiÍòá}dÓÁ\x0001Î\x0001øÄ\x001d¸¤ùÊ-7Éåö²\x0007ÇÙ4\x0015Ùà\x0000@w\x0003(>ÜËA`9ù\x0014 åùòZ\x0005ö4Ùà\x0001@ç\x0001 K.M=rÛ±ÿq°ÿ¨»\x0000Ð#\x001c'ßlæWÉ\x0014¤ÒÎÓò?\x0005Ø`dQ\x0017eg\x001a\x000eêÉK|ke~µ°xlLdèÌl	Ç8a`\U"[\¦<£{âìQN«Þè\x0016Å*ÅÕ)\x001d.(My\x001açå÷x\x0002jÀÿ«w»|\x00024ë$J+CR~ÏÎå\x0003íòuñ\x0007¹Jó\x0018Z\x001b¶\x0001\x001eWz¸C[Î×ëÇ\x000f_é\¢ö®Ô9RNY\x001bíöyì\x0014Þ]\ß¼~ûLß;.ùp±+O}\x0011¨\x001cÓÈI\x0017ÇRÛmø´\p\x000e\x0007{\x001cÆq¾\x000bR£\x0004?A\x0003ÏñãÂ4ëÜ<P¼\x000c-'Å­\x0011Á6#ák¬§y|Ïã§yYØ\x0016HêRlnWñ;Ò,PèÂ<È\x0017 Ãv>\x0007Qb(+tO\x0005=P\x0006:Tç.b\x001aüÉ ]¼ÃJEó\x001cPêÒ<Pæyè£±ü:Íû°õå\x001e(Ï\x0003\x001dötù%¤$\x000bt\Ú4ËcG£8o\x0015©ÂcÜ\x0015}\x001dÔ<Ç½.
Fúï\x000f=ß%ì£g	Ü%t±5C%Þ\x0013\x0015¯~x\x0011\x0007{\x001cÆñ±h\x001f¿$à[^ðäMh\x0016È÷@~\x001aº¨9\x001bª\x0010oBðWöÑÉSÐ,Nìqâ4\x000eøå±`Õ!±Õu§ÎÛYÜãäi\x001cx¥%	^Wï
h¥Ä\x0014ÓÉcÁ$\x001d·óô~¦\x0019~Rè]\x0016»Þ¡Õu`Â\x001bÈ\x000e;ÚNoi\x0017\x000f\x0003tØ¸u)8q\x001aé¤FøE"üXíÛcõõï\x000fùË×Ç÷g
\x0010zÛÞ\x0004ê\x0004eÒnçÝ\x001dG×?^ýéOïn^½\x0004\x0003=\x000cLÃ ¼\x001c\x001a\x0012ñLÓêòýñõ|\x0016\x0007{\x001cÅ¡ÎÿÔv\x000f;øÅi1Îq¾l\x0016Çõ8n\x001aGÓ7E\x0019Þ¶\x0008ú¤"g\x0012Ç÷8~\x0016\x0007«Ì"ïdùX.µð\x00077â\x001e'Lã¸f|R«WB×^*\x0003lÄ=NÅ¡|ÎaïÔr\x0014ì®`Ç¯3³4©§IÓ4i-Åqÿ/qïGräùn\x0005\x001b\x0018ZxÜÃôbaª0\x0007\x0002k@²ì¨_d(\x0016$¡EÝ¼èúi^g	³£uh'³\x0013éî\x0019\x001f\x0010þ¥ÚN·\x0011Æ¢Jª_yFxDøåïA\x001cÇÎºy\x000c§e²ä\x0007xÜÔ\x0010E)R^Ê¬íÖ\x000b£4×a·Cª¸\x001dª¹sR\x0012ã6%¢/áÄõK9.=\x0011\x001f?ýõñËÅßþøí9Qºf"WÃd
¡ú7s\x0011>¬K\x0015^ß¼ùùúíÅïxÿÌ\x0013>®_Ìqi\x0018\x0003Ë\©
7¸à¤9À¬[\x0013U\®år:yÒ¤­`ÎÕ²´Þ?b/ßry\x0015Wác\x0000A
ä\x000f?['CU`¡\x0005\x000b:ER®`ÜC]
&ý@ëÆx\x0015Wl¹¢Î`Y>d}ÏZdpÌe\x000f­üÔ%ÁxôR5ãÇl°RÖ\x0004ë°®
,·`Y\x0003\x0016ÒÇè¹Ö\x001e%ÙbëÎW\x0015XiÁÎWXÒ»\x0001Ta£Çmp¡²SG\x0001Ö\x001c=±é\x0018\x00193\x00198ÉÐâgeY\x0008'=ùÀ®Þïë\x001c¤ãR?&,\x000eV2TvÓæ£!ë\x001c?¨<À­ª@:éÍ¸HÇ÷
ÛZ²ÎõÎ÷\x0017 ¡ÇÕf4fÐÇò×´ëÐ²¬sþ òþÁÂb3Vå)Rpâ·åÑ\x001a°ÎùÎû×c)°¥I\x0017Eô3¼=rCçüAåý\x0003^T¹Ûs}(²1]_
5d÷\x0007û/®§2`ÃB- õÉpduî\x001ftþ¿>Ä,×à{i¤5RÖ\x001a\x000fmÌÎÿî\x0000Àîv²Y¢é%¨®ÄËl­; á²û·:÷ï4m¦ÎDq`ßxä¶h;÷ouî\x001fS?T:ì"\x0007äå`:âþmï×¹Ïz³`¡:ú È*K\x0007|íÜ¿Uº©Q$í¨ÊË6ÛôLiÈ:÷ouî¿>Ý» ]IYùdìÎÿ[ÿ\x000f\x0006H'¨Ú,r¶1¥\x0014l\x001dYWu'Õ\x0000a\x0016äl(\x0005Y5±Ù¦½XCÖ\x0000Vu\x0002 X\x001cM©È)\x0002ùMüMCÖ\x0000Vw\x0002\x0004Ë_\x0013[²\x0003íM\x001b¤%{Óý¤!ëN\x0000«:\x0001\x00026V&)Ró,\x0010Çzi<`3×\x0001Nw\x0006 {æÏÉR}\x0007læº3À©Î`\x0012ç(#bé\x000e\x00149ììý¯éº3ÀéÎú §fÝ¼\x00030ÑÍ½cGvë£?ª3 üÊÐ³)\x0007Q©Iöæ¦§YCÖ\x0001Nw\x0006àõlF\x0015S×K¿Ý¦\x0015^CÖ\x0001Ny\x0006\x00141ÖÇ	?´\x0003º3ÀéÎX¸´ÕºÄ
Yðú4\x0015Xw\x00048Ý\x00117\x001fæá|]ºÑ.OàF\x0006¬;\x0001î\x0004¨\x0017\x001frf\x001eX	cuâ^ÅÕù§óÿà8ñ\x0000õnX=R\x0014Ã\x001bï¼¬×yYÒ>Y_Ã\x0019ÏÌmúJCÖyY¯ó²YjB¬Ï,#\x0015#'kê}÷\x0008Yçe½ÎËâx.IãTS8CzÃ\x0011/ë;_æu¾Ì²"èÔþM\x001f3/b\x0005G\x001e'¾se^çÊ²8Y\x001bN}4\x0006sä:ë;_æu¾Ì:4Nà´5s¹Ö>VuÎÌëYq$Ú[mæx¦:V|³ÍÜ¯Ù¹3¯sgXp$ÔBc\x0001B1:Ç\x0001î:\x001bt×ÙÂ#EÀF'Ï¦x\x001dNÎ\x00057Ãbd2Y½
ÑúÏ\x001cj	kh\x0015WçËÎÉ,nÀ¡Ò@·²\x0008­lÐ\x001a²îÆ\x0018t7Æ"\x00156\x0001ç~c¼üáHr"tÎ,¨YeùÇHR\x0008%\x0019õ\x0010`S£!ëYÐ93çi4L}\x0001;ÑÂ\x0017}Í#WÆÐ9³ rf\x0011'¤Ò:Ki\x0016@¤Zx\x0003ØC6ëYÐ93ïäkÖ³\x001e&à%hp`Åîf\x0016u73¸ì
_T\x0016AnfùHÌ v>#ê|\x0006&Ê\x0017ÉJ¾Y.×Å.ç\x0003dÝý'êî?ÁKD\x001b'ßq0ï?ùH
8v\x001b3ê6fHÒ?æÍ¤<3\x000cDm£Ý¤\x0001ëVÔ­þ(Éi[I\x0012±\x00181Þ¸Ï'KÝúOºõ_É¨D´®,ö²\x0012ý)\x001bÝK
W·únõÇ$>¶n\x0004#µêY®²\x0007\x0016YêVÒ­þ\x001cå\x001c·Å\x0004|.Ù#\x001e#u«,éVY	T0n³lÙdÎw¯EV¤¾ìÓÇOO\x000f\x001f/¾ûôôôðõô±\x0014È\x0001GÏ\x000c\x001c\x0006Ä)à\x0015×7·W7\x0017ß½¹½½z÷\x0012mÁ¬\x000e¬Þ1
gÀf×;\x0006Wµ{×ë_æ[4¯C«LàBÌÏßzý´ù&Ñ¤B-ZT¢yi\x0006Ç\x001ey¡%pKÙÈú4W¡å\x0016-ëÐêEÛK¥\x0001z&+O¦m=¬­\x0002ZD×Ñd\x000e#KhU6]f×\x00033tlÝ6\x0000å> Cêà"	Ú9ÙMNÅÖí\x0003Pn\x0004_&';\x0015ve~\x0006ãÀ_fÛÄTlÝF\x0000åN\x0008Qªá0ÅCl2Òi+X¢cëv\x0002(·\x0002Î¨ ý
/\x001aÉq\x0015vY7\x000e\x000f¢%¿:\x000eê#¶ÕRùôïß\x001e>>~øôõ9e\x0004?åô]1ShzÂ¹º\x000bG¹ïõ¿ùïï¯n®_¿ywú¬"8ÛÂY%¯7¢y\x0006\x0011$$\â)WÃnÁ¹\x0016Îi-\x00074¢\x000b³ul7\x001eÇ\x001dÒ¦ÃHæ[4¯DÃi	óô«ISà\x001cÝê£aW¼g\x001c.´pA	W7*MKÄÑ¹~ÊÀ\x001fuÓ©-\Ô®¸ p®§¹¤!¸]Ùq¸ÔÂ%½å"Áá>++?ÖÏ\x001aöôUÆár\x000bõüm8í\x0007ÏûÁm\x0007t¨ØJËVl\x0019¦\x0008ü´\x001f,ÕãTÇ\x0016\x0004nÕÁ5\x0011ôÀFKç¨©Þ\x001c¬¹ú\ :»\x001e4 ¤ëÏ\x0007å\x0001±Ê<Ñµ,Ñ\x0014±èÖÙb%]w@ö(\\ÿ5\x0013eÙs\x0004qÃpÌ
CçAé³a­¾ºD¤­ZÂ3áÎ8]çAé3æhÉÔ&íè"ûº°¨¢ë\x001c1(=qFi0þ²sléÖ
%\çë@éì²Ç1£?\x0001VFâ\x001b[g©td¶s&VéLPN9ÐÇÔÆPØì@\x001e¢3ëË¦é/}À¡°Ï\x0014lb_\x000fÄDNÖ\x0002+Áø²Î¼Ïhwß_áTØ\x0017ÉlKfd~)Ø\x0004¡¯:4×¢9\x001dZ
,ªFKÜ~$]>e]\x0019¯Có-WZ-½Jf%Æ;¥©8pÈj±EJ«TÖ½ÊõÓzªXÛu\x001f£h¹EËê\x000fÊ\x0002fÖKiüûÎìÜ1´õ`Õ\x0004KpðË×ï\x001e>~<©P9êV¹ròs·þMÞÌ&KÆåÍ\x0003úí»«ï®nnNk\x0014¤õÕ\x0004K`p\x0000ª.1*V¨çæ|
Ô¿É\x0005²kE0\x0005k¡\x0002
5m,Y
x\x001a¦ÔßP-µö±
(ßBy
\x0014G[C\x0005JkWCmÃFÃL¡e
ãLØdá#AÍ
\x000e\x0008ÅxÕP°ÎÎCÅ\x0016*j <\x000fB¨ìÉMP Zk.* R\x000b\x0014PÞzÆ^ÎyóÕÛ«¬óMé8Tn¡²\x0006Jº%ë'ê¹\x0011J\x001c]Ëº(JËT\x0014Lõ\x001edÛyëÕ+\x0017ÈÇ;{·¯8hBÊ#PÀb±Ó(è\x0019JÜ\x0001¬¥]FòúºM£çôý§\x000f_\x001f¾}¾¸þO÷=\x001dx¬¯\x000e\x001a®W©Ök))±e=¢ìû÷\x0017ß¿yýîêýÝÅõ¿¼¹¼ûþ%@×\x0002:5`½å'ÈºdceÚ3k
\x00065 o\x0001½\x00160\x0014CãMAåQ\x0019¾Géb\x001b×l5`h\x0001Úâ.PÏêÉÛÎóoXjmÝj­Æ-^ÔÛ'\x0016Uû%) :6Z¼Ôâ%½õ2g
&ÍzÎL\x0004Þ\x001e­\x0003Ì-`Öï`Ç->\x0006+\x000fÙ~wðö­\x0004lÜ\x001eº\x0018£ßÂV4f(Þ1ÏP£J\x000f~ã&DVMè\x0012	\x0018¨J>Y+[dó¸Ó\x0002v>\x0006ÔN&\x0006NÂT@ÃÍÿÉ;&4\x0001\x0005ãë\x001cQöýdèï¿}¾úpZ¹¬>Xæö·\2V(¯£e}¸l\x00038Aøû÷w·¯9àÖù¡ìû©Ð/aÙ\x0011\x0018Ðó3\x0007\x000bÁÖ]ö*0×9\x0015X¦T\x0005«OvÒz\x000b)³ÅvFt(À|\x000bæur1¬\çà´\x0010ç\x000flÚ\x000eõQp+h¸²1Ó;\x0018Áì\x0012ë3\x001cc¶aÝÉ®\x0002-XT\x0019,RE:~IÏB!Ðý	¿ä\x0011å\x0016,kX\x0010Ä+ìa¯ö@h³\x0019c_Ô+\x0018\x0000IjÕÝiØ`;ÓÜÈÂz6ïxõáÛçÇçZÅ±ÑKã¤¶g#Eq;¡ýíÅÕë÷w×ÏTc\x0011Tj¡\x0002
»w%zç£/\x0012ØKe'\x000eô\x0002\x0013¤U!Vý\x0003öªW¿~úVO¡>ÿÇß~ùÛÇ/~<É¨zÓçµõ
G×rÔûêÙ®¾ó¾\x001eC\x0017?ÝýËï¾ûÝÍÛÿëú%Dß"z5b6À×\x000eï%V
¿Nqäp:\x0018ZÄ ·"UKNd0ræ«[Ü(\x0013ê	cK\x0018õFÄ}1¯AïgµÂ\x0002\x0003V\x0008ÃQÂÜ\x0012f=aN<Öû2ý\x0016\x00119Q\x0011×­zÄÒ"3Vba\x0018ï3÷ \x0008¸VLW#..\x0019\x0011Ù%k\x0018KæÖ*ïì\\x001a¦²`Ú,ë\x0010="t GtË|A\x0001¥°ÐNLë±s ÷Å¹æ\x0007<N$­\x0019\x0006B´ëh\x001eÑuNoF¬#×]khÃ°|½\x0003\x001eÝ/ÐynÐ»î
è6Ì\¿­c<¼a:×
zßs:ÈX\x001f\x0017\#ÇÓÿ	n\x0007:ß
zç]ê¡Rn_ï©\x0014\x000bÅ~F\'lô©cLg|j+¾1æ¹Û\x000eý\x000eÕSÅ¸Nßè\x0011»\x0003\x0006ô'L©"*<÷nKVtÜ¨\x001b7CSôÝ\x0001\x0003ú\x0013¦\x00040<×AV+Ê´í\x000fiÛ0VÂ(\x0002ÞÍN\x0007Dð.®«Ðõ|ÝñbõÇKq;Å}\x0006vÜ¼ËºïA\x000fØ_¹Ï8["\x0017¼Ôæ¨\x0001Ú»c^÷eë\x0019»ÃÅê\x000f\x0012Ñ9óBÄ­=3&³uÐ3v§U.õ]`XF\x0007E5gÇmU\x0014bY7kè\x0011»ÃÅê\x000fÚ£ärÊ$àVLIfÝ\x001aªGì\x000e\x0017«>\2\x0001á\x000b#jFÎVx¯;Xì\x0019\x0007Kñò¶*e¾
XÂ\x001eØë¸¸±;Y¬údÉ88Õ\x0016v9sr\x00015\x000c@Üö:ê gì\x0016«>ZênqC=á8\x001fÐË;q\x0010òQ;ºîhqê£%c
{°r\x0017Ks\x001eÚå(ÏÔuk±;^úxÉ&:Öû\x0008&Î\x0005G\x0001«SÄG\x000f\x0018×\x001d0N}Àd°Ràê«z&t"b\x0014ÍáÇ¾ëÎ\x0017§>_ò4ýcv\x0001H\x0006³2\x001a
éW+\x001eÞ1®;_þ|ÁÒ{\x0001è²ªÌ¦ÕÈw×²Ý\x0001ãÔ\x0007LÆñ«¼cªw´¾57%³n¾\x001bg¬uQm!èÕ\x001f?Þ?}}®\x0004®bÍÂ\x001bSøºPï)I¢êª\x0004|þpsyûîÙ
8"³-Uy¬X¢\x000c	p)>]áÒZèNGæ[2¯$£J÷9ÛeF\x0005[ÖOQ²õÜ°,sÃ®þòøñáâoÏ¶:ã\x0011:å0ÿK\x0013\x0018cyL[ÖõTW¿½¾¹ºøáýõ³½Î\x0004f[0«\x0003Ü\x0005UHZe\x001aï%1½\x0010kÀ\\x000bæT`^b\x000bÕð$ã\x0002?Fl^ç£U\¾åò*.Ç\x001dm¥ºs¬raóz°´+´\AÅ\x0015ô¸ÉÓä3\x0004KÜ®kËºP\x0005\x0016[°¨\x0002Ã¡(sb<$¹xÃ=Î6¬çøiÀ ßºMªós÷DAY9 2®\x001a3J\x0003Ö-}Ð­ýâ¨s¢ð¸r\x0001GPë\x000bãÅº5\x0006ºEVx\x0010w=<ÊyQ±q-Ù "K\x001dYÒùêUKUF\x00056ÞqH×MHWCV:²¢"<\x0005Á'²0_*wB¶ÖßÐÙný[Õú÷õPÙ+tøËô\x001dë×7\x000c\x0015X·þ­jýc®2*
Ê¤¹G&sëP¬Û\x0000Vµ\x0001¼\x000b¯¨P/\x0015Ökð2 Ðnò\x001a°ný[Ýú\x000fbÈÕgxV\x0006ÁÉÛâ3\x000e¬Û­«[ÿq\x001eU1ñ@õR}\gÎZeeÝÈQ -Ùú?ÿó_}}øüñÓ·`ÆqgI(Ø6ßc!¼\x001dEqsqõîêîæÍûÀl\x000bfu`Þ±ÇHÁÐ0ç
ÆE\x000f&m¿ÇÁ\\x000bæt`¡LÕ*\x0015\x000c+\x000bâü&)|WÄÑ7çsùËë¸"¿6ë\x000csí"beþ[\x0005q®Ðr\x0005\x001dW¶³¤ÁFMrcõÊB\x000fupÛÒ8Wl¹¢+ÅW´ð\x000c\x0018â¡3×zr§\x0006+µXI¡ÀÂö/ÖÆs¾\x0013;Ï§Ê-UÖQ9Çþ+eÃ7~Ã9ÎzBmäF¸ÂÚ}6>ð_?=}½|zA¢Ú)PnÒ°D'\x000f\x000fÛ¢ìúÖý¯onß]^ß>çWÃÚ}6<0\x0000\x0016<?ÜludgTHÃc	å¥\x0000s-SÙ Ò(F\x0002ÍìUÝ\x000cðÖpùË«¸ü4-{²Wa¥ù(i·`ö:Ì¹BË\x0015tö\x0002Q\x001a®\x000bß¯e}¶\x0003X±Å:s\x0005Ñ³C­\x000fRÚþfî°+µ\Ig.I©Ùê÷3mÈÌÂüÁm&kÀr\x000bu\x0006s¤1fCf-÷(¹¾`Ö)S
WS\x0007\x001eÌèÀi6\x0019à/ÉçP\x0000¿SÜ9LÖ¹0Ðù0Eÿ\x0018åwx\x001374\x0005»-NWu¾\x0002tÎÂIr\x0019\x0018I\x0013F\x0013\x0017/¶#]0LÖmKÐíKçeÎN
¢ix\x0006VXgNÀÀ¬¦\x0005×?h\x000fÊ\x001f>þíÃsXãq\x0019\x0007gÌ\x0010VX§ºëß½\x001eÁ²-Õ`A$Õ®z\x000b441\x000cÓùøÎëH\x0006ËµXNeaI!M¥\x00169X\x0011ü^ßý(o±¼\x0002+Æ,\x001d\x0017I<\x0007Qp\x000cvÏSb\x0016+¨ÖVâ,b©K;*Õ~Â(Ul©¢ÊXæU\x0014é\x0004K+Ë¸Å«\x001eXð©¥Jª\x0005\x001f¨*\x0014©\ì¥à¶\x0012ü\x001a¨ÜBe©\x0013ýq\x0000V÷Á<\x0003ë\x0014 \x0006«´XEUf¥¡i]\x0019\x001aôç\x0017ìI\x000cRAïI5®´z\x0007Î£>\x0000CHËÍ~'%9ÊÕ¹RÐøÒè¼8°Ï¢¢Züù¾\x0014:_
\x001ag\x001aT$BN|ô °è«ì\UG¹:g
*oNTgsõÐ³\x000fìË\x001cØ(VçLAãM±ÍÇ!Åùþ\ÑÈ=U¦Q®ÎÊ(cG3¿\x001b³w%R9ßI@çPAãQQØ4r Xzeod¬ÏºsFÕ¹TÐøÔP¿\x001dé ¸\x0016ÕN||ýÿó¹:
\x001a§q	G\(¶?ûz\x0017\x0003Æu=¡\x0002«)\x000c6©#\x001bÀ\x0002ôÆ\x0005KXnsþn´³·\x001ag\x001flye«^¹\x0008k\x0019M°ç©Áê¯Í\x001a_\x001fÈÑCàW½&\x0019½®q\x001bZ·\x0003\x001ai\x0007üõÛÅ\x000f¾ýõáóÓÃ_\x001eN\x0017cáÉ\Ùf2&¹)lYd\x001f¶¾ëýÅ\x000foÞÿ|uw{õÛ«ÛòÅ\x000cç[8¯\x0003¾Ô\x001b\x0014­¢1[Þr{\x0018ÄõDs%\lá¢\x0016.SF-§È3Í½ã;Hkq%[nÙ²
\x000fÊ@p^Cõ2Á¢\x0008°Õ/VÁ5\x001dk¦´ª\x0012terúH
%å"Ø^/ttÝ\x0000íp®Ö&\x00177ë"!\x001dÃ`\x0019¤aýîéýùþéÏæ#Aæ®çÈ\x0013¤Â\x0014¶=Ûz¶ÏäDî.oxÆÀJG\x0007¡¼\x0006j9PLbÓ £÷D\x0007bË\x00145Ly\x0019\x001b$ ¹\x001a
ù|¨ÜBe\x0005TâE_ïúë<[fYíÞõ í\x0008¦e¾Hcu)TnÊýruÝ¦©º\x000eÝ'ËuZèu}ó½õÏgWá¸
D×\x001fï¿}=)z¢É<¸\x0013¨Æ""B%¯üÁïß\x0014;`\x0010ÛØ!\x0010g©¸¤þWfå¯Iéf\x0001Yßl@\\x000bâ@Pö<Êzñ0\x0017Ç\x001cke!\x000eßrø!ú|¦à\x001aW³°óbußó\x0010HhAÂ\x0018HFÏÓ­xVø¡õº.\x0014\x0019Â-F\x001cÂ\x0008Fæ\x0018×/ù½´c\x001d0~Ã¯wh\x000býøðôùñâûoO÷Ï\x001d¤\x001e¨~\x0012¦\x0013\x000eÒÂu0,³â¹º½»®Çéíås§¨_ï\x001fQ\x0016\x001aÃ
2"\x0012å)Í[Qé7Y\x000f\x0015Ô`¹\x0016Ë)±\x001cµ<\x0005Çe°\x0015Kzi×E\x001a,ßby
Ö2èÜ×Gñüø¬Ç\x0016pïç\x0011c*¨¨,+:£\x00160éÎ\x0005\x001bôØ­]\x0002+¶XQ2?±%å$XgR5X©ÅJ*¬À¹\x0011ìöã3Ãfiã%\x0015P¹Ê\x001a¨Ü@6$Î\x0007aª#°´XEåiä\x0000zðSiiÅâN¯Í0	\x0005V{O[´Æ¸êEÖP'\x001f\x0018.¶\x0008eH°Zý|®ÞÇ«|¡®\x0002\x0008ß¢¯{f¬¸N»i°:\x001f\x000f\x001a'\x001f0)Bæ²=\ÚRX×Ìh¸:'\x000f\x001a/\ÔºE\x0004TÁV¹ØqÅu0OÃÕyyÐ¸y,Ê¢¨Ç6ÍM®\x001f/
×ïØùyÐ8z,å)e\x0004¤a	£´.\x0015ÓPuþ\x00144\x000e\x0015T '\x0011çòÅú<`¬\x0003{±s] ñ]Á%Ö¾ÆÒ\x0019Ò\x001cÖËG\·\x001e)¸lç#¬ÆGz)ô\x0015åF(ï¹ú7äs¸âú~\x001aWÔ×_~¹?E1UÓ(2ª\x0007/ýÛÛòµë·ß]¾d[$«@ÊH\x0004f æró¤ùr&o¼\x0006ÈO5DÓÆ²O\x0003´Íç\x000e\x0012Å(j\x001cWÅ\x0004\x0003¯V\x0013\x0003°õu¯2y(·DYAToW4r8À,(H6p7.l)^DÊë¥7KûÃiÉòè\x0002	óäå\x000bù3
Ô\x0002¬{*\x0008éõiÉrfr-Ó0\x0001iEgÅIWT2) \x0004ÈÛJQ¨ØB­WÓsP\x001e¦\x000c\x00112\x0019ÏÓê\x0000èV\x0015 lkGrË´^OÏ2Õ{'<¨î1\x0017ÖsÃPí\x00054wâ/>?\x0017( Uuâs\®ÇUàÏ·7Je;ªµÃ|~QU¯DTÞRø¹.*M(j\x0004ª¬7a¾þòôðñô9¿\x0014~	KUè\x0012[§Û¯ßÞ^Ý¼Äa[\x000e;Æ\x0001K P\x001a÷â¢\x001a¿	\x0014\x000e¸\x0016Ä
D¹U¢<\x0005ð4v.»r\x0006o1ü=Ô\x001b`i8\x0017\x0012ós·iÉ\x001e\x0002	-H\x0018\x0002IË¨ik8\x0003\x0019d}Ë\x001e\x0002-H\x001c\x0002	EV\x0008\x0004VÌ]Z\x001d\^ëÂ\x000c¤\x0016$Y$ðX¢º÷_±AXmÃåulb#·\x001cyl¥zÉ­¡K¡\x001b=HÜ:³6QZ2Zv¦ïÂï\x001d	¸MÅÎ\x0008HëõlíK\x0006)2pÙW\x001eR¤ãÒº\x0018f¤wªc^5\x0017ê2©nUjäKë\x000cÕ\x0010HçUaÌ­¦È`â+j\x000fòE,²Ö)\x0018\x0002éÜ\x0019ù³z\x0007¶1Òc1p\Ý¥õô³!ÎÀ\x001bÉÜ!^A,'\x001fn=\x001cs#¿ÿåñKïJð\x000fF¾P\x0010D.{B)­Wsë\x0007¦ë¤pnîÿzÿôë3%?\x001e§\x0019Í\x0017¹ºät»¤ks{5?7?_Þ~ÿL\x001eÓ­.¶E\x0004/Cá\x0008£ùÊ[êå Ì5§X¿¾ív2¾£X®År\x001a,Wæ>b\x0015
\x0007g\x0008T¿_±öJG±|å5Xq\x001e/X !¬ìø#¦m\x0013å8Vl±¢
«z\x0000GXÜzá\x0003¶V>ò\x0011S4XØ²Rf¬z\x0007-ü¢hpµÖ^Ýð(Vn±²jÉ¹R±bá÷$kEêvúåÇ±JUÖòV°\x000c[ÇO¸¼.,P`5g>z-£Ú³+§Å\x0015ËGö\x0010y¯Z~«÷¦\x001awê¼K¶¤øTßÅ<çÛ½ú§Q®Î¡Ê£\x001aº´U®Â=.\x0006õ5và3v\x000e\x00154\x001eµ.\x001fï\x000eg\x0005\x001bn\x0011	ÞîUAru\x001e\x0015T.Õð8=´ú,V?v£wk9a
WçRAåS}dU
ce¸	D\x001e»â7S1Æ¸Ö¡<û	M7\x000f}8\x001dà\x0008ÙÏÕG\x00185,©á,OõÙÖXãÀ«¯N\x00078\^_!r?éy¤-4b.nª\x000e@¤`8>µ½×\x000c3¹ÉiÌ\x0004sWâÌÄ5òÜLçCù\x0016Ê+ 
Ð@¦T\x001fþólçì\x001c\x0015)`+îNô|)´LAÁ%
\x0004\x0015¹
7;`geÍ¶
w\x0018*¶PQc(;W!V¨XÑ9x´Ó8\x000cZ¨¤±{$+\x0014\x0016(pÍ>K2n¦Û*rË5Ëª\x0000p\x0000Vüd(ËKÊï%d\x0006¡J\x000bU\x0014Põê\x001eé\x001eS£s\x000c6ÛDê:õ¡³\x0019Þoj\x001c'
BA*à¼JÅ³ªÜNeò0Uç¦@ã§ì|\x0012#U5#[E^Un\x0013\x0013UPu~
4*\x0005¾·gï¨¯ÎYÃK=íÉ\x0010
Bu
4
æÓõ8Òàl='\x001c&MÞs©:§\x0000
¯àê\x0018Ôlw µüÄñv-×§ êÜ\x0002hü\x0002ªà_@$òê¢\x001fëÌöÊ>LÕù\x0005P8\x0006¬ú$5<\x0013\x000b\x0005U3Ö ­ð½z&UÓ¸·\x0017£°\x0015N9`weI"#ÛÂ\x0013/Ýê\x0013\x000fSuîÊ*ÜË<ÃÎÀ\x0012ÿ0Zñu³;ôoª¿é)®z\x0001ÇÑ\x001eÄ1«d«ìÄ]mU\x0015©:'j\x0015N\x0014\x0015c©-\x000cê½Þó<î*|¾¥:\x0017j5.\x0014%)É±×ËÞÜS\x001d{â@QÙ´Su÷*«¹XÕLÌôdËqcÌ{ÚdT·²\x001aoU\x001d§¡iuò>g7_öì£Ùu~Á)ü\x0002zvO\x001dçFcìØ\x000fÜ\x0017\·\x0001b\x0003NÕÍ\x0004å\x000b×\x0002XÖ \x000e>Ü¸nY9Å²Â\x0018²MäØ3)cfH#\x001ey«\x00185¾Ø»èÿ¼à9ü?vñ¯h#âô\x0015º6$.3ñ°§Aù\x00127«W¼7«Wüã/\x000f¿þãï's\x00136\x0006NB×#kÃm`­GgÖÓåëú»«»gº4üº©ÐÕcþe²9°MCÈ©OÃzNÛrb;¹Ì)ÉÊ|\x0005¬dÖðxtËp«ÍN¸¯12ßy%Y&ÅÇj³Äm6·¨6;á-ÆÈBK\x0016td©.ú 6£\x0014²\x001eÄf\x0007Àb\x000b\x0016`+Øá;j\x0005\x0013Áþ²1T¥,)ÉdF\x001cnÍlåNNÞÇÈrKud9Pî{2\x0019%ÙîÈò/-WQrÙ©ê,Få\x0012uéýSY»ðf5¢úe´BÒµÉ\x0012-ÿÌµOÇl\x0006ý\x0001 <\x0001¨×}e´\x000c²3·21
´î\x0004\x0000Ý\x0011à(k&+´Ê¸\x000eM¶ÿL\x001bãêü?(\x000f\x0002<¿
\x0019uãX
UM¶ÿþ\x0018Cë\x000e\x0000Ð\x0000ÎdÙ\x0002F\x001aãY\x0016Ú^ùø0Zw\x0002ò\x0008(»ãp¡Q½½&\x0013göJ5Ñº3\x0000t³ÀZ£õ+\x0002u²\x0007\x001cOÐ\x001d\x0002 <\x0005pDDX¶'o\x0003©\x00124'®ÚchÝ)\x0000ºc ÚRS\x0015-ó\x0007uVj Ì;í\x0018Zw\x0010î$Àm\x0016«3ËÙ¹U'\x001aG³ÝI`u'³«0¡GdÎ¤»µÝI`u'\x0003]TÉ\x001c·¯ºe®ûTdýS@y\x00108Ã­ýÆzyàÜ²	Ò\x0001k»³ÀêÎ\x0002\x0007eùÍeiÛ#íN\x0002«<	\x001c?QL/r,Qä`]§âê\x0001«;\x0006µ\Ljè³N\x0006ã&i\x0007'r
chÝ1`ÇK¬Ñh¦y'V;â4ºSÀêNj\x001e\x001eimp\x00027\x001bmùG¶;\x0005¬ò\x0014\x0000\x0008-rÇ´\x000b¬ê`[Ð¡@ëN\x0001«<\x0005,eg4Þnù'òCh®;\x0005ò\x0014ðI®ÞÌíYh5!XØ\x000f\x0017¡uÇS\x001e\x0003Î°N½q\x001cÜ«Vã)·Î®\x0007,©ÐºsÀ)Ï JÆ\x0007Ò-SvÐ¶âÓ
´ÎÝ:¥»
QÐa}.\x0017Y¿Ã¹#\x001e×u\x001e×)=nõ\x0018Ô
h°]J\x000e\x0003ù G\x000e)×y\§ô¸!ò³88ÜÈC7;´Ô:ë\x001e×\x0005Öc1Å·²ÒDÒ\çpÒáÂ²Áõ®8ÏYÅÉNv¢Vf\x000c­s¸Népë\x0001J÷õ?â ÎËÙn÷:<GÑ|çp½ÒáFûö\x0000J]ÒQ Í	îÈ+ÊwîÖ+Ý-§R4
s)lV¸=àTâw\x000c­s·^énùÒh4ú¢©_·ÈãÓw·n¯¼uÓ$ÌNEçó¥\x001fì§ruch·õJo[\x000f&d{ò\x0004ØÀ½àu©\x001d¸ªùÎÛz¥·pÄ\x0017\x001f9ò¥Ãíµð\x000e£uîÖ+Ý-¶1çF<G´r|\x001eÙ»õJw<\x000bíèÅs\x00149	üïÜ­WºÛ`YYÍD\x0011{­\x001756ßÖ,£ÎÝ\x0006¥»MK&*&3«ë+
Ú\x0017{è\x001cnP:Üº+=\x001d\x00051¼}µ\½}<Ö9Ü t¸YZÑjôòÀ²fnGT[ÖyÜ ô¸M:êò¦Ã¥xêZ<°CCwõ\x000eÊ«wqïH\x001c·ªÛÏ)Äy>ë©<\x000c°\x000e!Õ\x00029ÜXíÀ9\x0015ºÃ (\x000f^\x00051¥1º\x0016Ä­\x001dÉ{î,\x0008Ê³ Y	v$n.(S©\x0012\x001bí[ë<nPzÜÊCBYfè\x0004-Ëç<°?cçp£Îázìt-ò=Yø[\x0006Ï×ïyà\x001a\x0019;\x001b\x000e7[ÙÓ&½tÃüÇ\Gì\x001cnÔ9\Ô'\x001dICzY¾>íØdÛ\x000f
®ÎÛF¥·EoÚIâ·\x001eRøglØyÛ¨ó¶\x001e\x000bK\:\x0012¡9I²û#YØyÛ¨-2	ré°³>6ÊAp$\x0010û"\x0013³õ(h\x0017oK\x0007»ãdö¡7AìmÔ9[oD\x0017W\x001a©&{+¹ìc³»yGÝÍÛCÔg]i4Ï{\x00160v'ÚoÆÈºc ê\x0001ìå8G½èR\x0005X=1ó?Ãh©;\x0007ò\x001c\x0000\x001eB·[²Xs\x0008\x001c\x0008
¥î\x0010HºC`\x001aeñùäÁþ3ÎÔ\x001d\x0002Iy\x0008XhNÏ£\x0015DÿÆ\x001fq¶©;\x0007î\x001cÀ¯	-)N4YMB·Á\x001dAëÎ¤<\x0007ìR9\x001a|P©5¬o\x0003\x0017ÈÔ\x0003Iw\x000eTïÅÊ&Ã+:¡$ËÂØmêÎ¤<\x0007l¨2Îä"Ç\x0011ÿ\x0019w´Ô×\x001a*\x0001B'ñLhåv$@ºc )\x0001g8Gã£~Éùø\x0013m`cdÝ1Ç\x0000J\x0012P$![Ù\x0002Ë}ãH|4w§@V\x0002.JUBâ®ñâè$\x001d2Zî\x000e¬<\x0008\x001cõiÏFã\x0018Gä1(ÇÖ\x0003Yy\x000eP¶s2çÇO^VÚ\x0001_»c +\x0001\x0014±f
¿O¢á\x0017¬rw\x000cdå1àã\x0012\x0017<\x0004\x0007Ô±ÑN´¡uÇ@V\x001e\x0003NæE¢Õx{&·¬´\x0003î6wî6+Ý­+,3_ÍÏ£9|$AØ(ÐúÚn¥»
F*õQ¸®\x001c9/wÛ\x0003¯¨ÜùÛ¬ô·Þò°n#ë<­Îr\x0000¬tî¶(ÝmpRÍ§'}Î²D8D KçnÒÝÎÉk6\x0019ùXîë¨Ñ:w[î6DI|â\x001cPÚ%Éö<R	Y:[þÖG©7Ì¥J}\x0016É¶x¤\x001e¸tþ¶(ým(\x0012IÈý\x000ffñiGÖ¹Û¢t·>K#A.ËI 1«¸§¤<Ö]»òÚ\x001d\x0003çÀÊøÁØÅÝ\x001eùÝIP'Au·´	
PÓiÝ\x00042µ*n'f+Èº (\x000f\x0002ìgæWTb}Ú`¼Ø7c.5h}ò @µ@ZjÅqQ<F`Øjáü`\x0002î(À¿Ô-ò¨jÒO+\x0001¤ 8\x0010\x0018cë[}ò0\x0008A.kEºCPbÙ\x000eÜ ïö*UvK¯ÈåÂe\x0013\x0001$\x001fµ\x0019é¤BëÛ}ò8\x0008"±okEÂjñ@\x000eô
ø:³e\x001egb§´\x0015\x0002,\x001aÁ\x0007WÐ·|â_êì&'\x0002*Â¦ÕQ\x000eô/Bßó©µ\x001aÍk\x0000#O½ £R\:\x0010W¾ë\x0013ÿR{X9f+ËaÅóÑ·jË*¶¾ãÇ(Ï\x0004T\x000ccýå$Ã^Y\x001c²²yýHëFöÔ7²ÿöþéÛ×§¯NÂM\x0003 ÜÚ¨É2±*\x0001Æ°vïº¿½¼}ÿîêöÝõÛ\x0000m\x000bhÕØ´ÜxyâL^böë¯\x0014¾\x0005ôj@\x000b<HNF5%Ö¶ïU\x0000Æ\x00160ê\x0001ã+.`³|~%#ù÷\x0013EÖ
¾Üòe5óò±x\x000chÍR\x0005¾{
\x0001®\x0007@ø²Þ#?üéô\x001cÎ\x0010I5§îÝzµ±\x0007¸õöÔö¸{ýã3[w=Á^Oá%¬$õ8Þ²¸¼áùÑ°\x001fÛ\x001aÃò-×`\x0005\x0019ö\x000bõÉE×¸h¹4ÝÃþ?\x0015Z¬ ÁÊ&Að,ö\x001eØj?J?\x0006\x0015[¨¨ZY®nP/¤Gû\x0013ÍIcT©¥J*SEN\x001fC\x0000¾µÅºÎ\x0019k¿öj\x000c+·XYµÞUí,4\x0006Åóð*\x000fû/¾1¬Òb\x0015
V1<¥
°7>¢ô¯x`ÕJ'tÂæòÂI6pÁ~QÇ\x0018í¸¬+s¯ Ú+¨\x0010{ï\x001f s[ ò[ÕAPª\x0000|ä:Í\x0018"\x0008×ùX\x0000@Á`6gÈ
\x0015k_2a«Û Ú¨~A¾Ë[.Ì2Á\x0010\x001dâ²Ý²·ªe_·#O~ñ°Ì°(Âµ¯e5ÆÕ-{«Zö%²R\x0002¸"£`\x0012OVõæÔ
ìY.·\x001eSídLõ¯ßé\x001fÿð§ûÈxsÿõëçöÝý/|úÛéÛXÝ\x001caFÑ­ÙI\x001eyÛ$Ëû
z3#¿{w7Á¿»|ûöúÛß½Ä\x001eZöp=Hå\x0007¾P)0\x0016a®ÍÔÌ#ð±á\x0003n4úïæ Dö,¿PÞõn?\x0000ZøtÜò1Ra4Î\¢'n}y,¡õs=·ìù¸áy·I¤ÉÜZÃ\x0014úúgÁ\x0016¾\x001c7|%æ)SRP¤¦.m\x001eÇç °zEÕs§E=|ýüéß>î7¥!=+\x0013\x0015nõõÛnlÞ\x000fUþöêÝÝÞ<3ãàl\x000bgõp¦XG\x0016ám¿ÄhÍµlNÉ\x0016Æqâ]Z';Ð\x001eó-×\x001a®n{'zS\x0014öÙÈWÝ\x001bº©\x000b-\PÂÅYÍoêÉ_
FZ1a¿j\x0018.¶pQûY­4E\x0000°\x001cÏ¢\x0007wÌn©EKJ´\x0004¢\x0000á\x001d\x000b"\x0006\x0010ÙA\x001c\x0014z\x0004.·pYûQ
\x0007¡
$n^ÏIQkÜ¿â
²5.ôqFk9©ºsÛ\x0002HM,¬u*áz\x0007¬õÀõñÅÍÜKTµKù!'\x0007\x0003­ËAÄÄP!LçVÖý+ò(]çå@ëæ²\x0015¹\x0016\x001f^y¢³Ò	oOxGé:O\x0002ZW#"ÅføÙv"Uq¶[g\x0018Âa¨WÇ_\x001f9\x0019\x000c\x0017íBJ¤Ý[P\x001an³(\x0011½¹\ý\x0012kaÜ K´ôm=Þ\x001dß=¸ ÜãpP\x0015K\k\x0008GÓ\x001aæÓÓ×\x001f¾=~üxÿí/'¿[v¶peV\x000eaª\x001f{\x0015LäQ)Él\x0004Ù+ÕÛw\x0017?¼¿¾¹¹|ÿÛÓ\x001f.®ã¢$<ÎçÂôÝ\x000fGIÌ#ìë+Äg6ÅêZ@×\x0002:5`ð,C4Ò~dO
2- o\x0001½\x001eP¤wª5ç6x\x0004ä)n\x001c-`h\x0001\x001a°ºÉ$Ê\x0019L2¼3J);O\x001f\x0015`l\x0001£\x001eÐpã\Àk0\x0019Vþ+±jÀÔ\x0002&5`ò\ÅcC­õ\x0013\x0017^Û\x0019"Z¾Üòe-ß4Ñ.|\x001f#Q(¸:M\x000b\x0016°´EoÀÀ\x0005ä\x0019KÛ3\x00190±\x00057E\x0005J>è½´ÞM§¹b\x0010\x0001±n*ò\x0017f7èóNlcpý°ò°~óñã§§¯Ï\x0006;©\x000b\x0017²\[båIïÖO777on¯Þ½\x0004c[\x0018;
\x0013%°ß\x0002û)	Ìº·o\x0010Æµ0n\x0014ÆMOøÉ2Eð£Ô{¿.t\x001bñ-\x001fIüÎ$¢ª1q_wëk÷ Llaâ(Læ:Øê
^q)ä\x00136ã-\x0007YrËÇXbuL\x0014sây\|fÕ+¿ix%®÷xþéþãÇoÏNH8ÈR"a¹¬®®b?]ÞÜ¼fÞ4ÁØ\x0016ÆÂ2\x0007$\x001e\x000cW¢H	n÷Ò oaü(L ¹O\x0015ÆÎwT«³[×'\x000fÂÄ\x0016&\x000eÂ¤À©	Àp	²~íºj\x0010&µ0i\x0010&'ÉZ-\x0013¹[,FnåôöôAÜÂäQ\x0018#\x0017qõª#ï7S\x0017\x0007aJ\x000bSÆ`¢ÅÅ¨f"1sK·ëdý\x0018L\x0013Ë\x001cä\x0017MSD:\x0017kR¸'Y)ÿÈÊEÖ¿$¿\x001e\x001f>~¸xøñüÇ×ßêÏhø<³)uoQ	\zgã:-øÓõÕÝÝÕÅÕ;L
^_]¼~_¾ÄéZNw\x0016g4Sh\x0017AcbÄÒ6¬KRÏÂô-¦?\x0007\x0013ÇEÌ\x001dÌ&×S
ñl¦è\x001bukÌY¡å\x000cç3ðÔäÃþØ>·\x001b}£³@S\x000bÎ\x0002­\x0017¹²±\x0002kI¸â8º¿~ÛÅ[Î|ÖÏ¬f2ª\x0017ÓO\x001cw\x0005·ï\x0005ZZÐrA¥ýßT¼)Uýj\x001aÀ\x0006Ý¨\x0004\x0003
½g:Ï5A|UÂLj¨\x001eÖë\x0011µ\x001cÀY¤oó\x0013xïGøã\x000cwÄÁúu¦\x0004µ³%õù¥²>\x001eC^¬åÊ`<zæ\x000eÇ
)õ(;sèÞV¾ÛÓ#È	Ç¶8v\x0014Ç%NÖá¬Åù.³çB`\x001f·:c8®Åq£8!òÕÒZG·¹\x0013÷Õ\x0004\x000cÚã[\x001c?lÈïi\x001b2\x00109KíH°ÛI\x000ec8¡Å	£8ÆQuÜ¬3p\x001fH­üô\x0018Mliâ°q¤ °:ýé·ÝÒ	v+0Z4C7è!POz¢±RF¶	Ê1ÜÒäaã\x0000·Ì[}ÅOY\x001cå}\x001eNiqÊ NÆÀ\x0010HøcV\x0002Ì©Èc6mE
pû7:A3Ê
ñÄMjóÆZBCy;Åk\x000c§÷ÉãN¹ptÈzN ×¯ÅmçÁ·Í¡óÉ0êsÉ¼Ïi*Ò\x0018Î{VCiÎ'Ã¨SbÄT\x000bU
eg¿<§×\x0003lKaÇx:§\x000c£^9ã]Rwõjghñpan0ÛvÚ1Î)Ã¨W®`ñ\x001a+:Õ\x0019\x0013Ä³Íòtn\x0019Fýr^\x0014Ñ/ÓÔ¤tÍn%1Æx:¿\x000c£¹\x001eßÓ5g*¥ó²|
Gh¶õÊc4_aÇl\x000c\x0007"pÊ¡#Çl¸Ç"x¦u:Ç\x000cÃÙó°dÀ	Ä\x001c·²\x001dñ!\x001eÛyf;ê\x000bí¬é²OSàg}Èg.\x001dÛùe;ê³\x0005Y:ÑÐÌædø\x0008~[#=ÓßÇýräyµ8è\x001cO6üH\x000fe;kf§sÌvØ1Ì¾±ÙS¥ÚÇóÚëØý(Oçí°cös²\x0013yê\x0015¬ÐZö²|ÒÐvÙ\x000eß!q±µúXëçêáuc<g¶Ãj¬¦õ\x0013¨¨8'iä\x000e%¹;Ïl=³³ÜââÌ|Æ#å.ÕÏÝ_o¶£¾\x0019}!ÕñáX§\x0010yýÐz°U\x0017\x0019ãé|³\x001döÍ(=¯gõJ´3¯çsßÆ®sÍnüÒ\x001c9jí°Â;1\x000e\x001d¤(p\x001eOçÝð­¹\x001e¥$ÞæItk\x0006ïÙ<ÛÖ1Î=»a÷\ÏsJÊcH|Ñ°Ì\x0013Ï[Î®sn8z\x0000aq?,ð¥Ú-sq:ïãßëPäæcy¾\x001cFäÞ|æ×ê6»\x001b¾Uçl[üâù°@IÉó\x000e÷ßÿòøeuÀãüÿ|Æ§
VR`ý'¸j»bÚ¾ã§÷O\x000f\x0017_>}ûrññáâîÓx)\x0017º¨Õ«^!u´\x001cYO Ä\x0013ÃXº¹¼¾½ºxûæýÛ«»7¯_Âµ-®=\x00137;Ì¦ãdd\x0008i¿·COë[Z.­³e
P`ö\x0004ÏC(þdÙØ²Æs\x0017\x0002¶Ê$ÂÍlÚ`èSqónK\x001e7·¸ù\Üº­ææÀºn
e³rp$HTq7µçá¶q2»ê!Ðð\x0016®,¬ÿ;ºYs\x0004Ï¼qF¨7¯3ÙÙ´É
ñîóý_\x001f>y8é¬+EúX||ÅJø¢»³éY¬®ªþïÞ]þ|u÷öê´ÇÊë
ælÚDÇ\x0008\x001a
ÎótIÔÏåù\x0001n\x0019{\x000cÎµpN\x000fÇK\x000fµw^ö÷h\x0005oá¼\x0012\x000e²´uÕóÚT\x0017É3³\x0017\x001bPÀ\x0016.há\ÓDdÀ-6;sVUd±%J2çe\x00142F3X¥9,­z³F\x0005Z¸¤5Û2Ç®>¸¨ÅKd×m+up¹ËJ8\x000f\x001cMÀ®.î#LÜrfw_Ë
¸ÒÂ\x0015%-"T\x001bÌ+Vyùbv/D?ÎÖ\x001c\x0017è~Öraò>5xÍ
2~Óñ®ëÏ\x0006åáÍÀ\x0003\x001d·û´\x000cÝ6Ä©è:\x000f\x000cZ\x0017Ós\x001d6¢Ív+@¬¢ë¼\x001chÝ\x001c\x0016«QW\x0017¦\x001a¤ÑQè¶ºg*ºÎÖDÇÐBâéÈõïbÕ8·\x001dL¢ëö+h7lB\x0007	¬¡¸(mïÑ\x001a:Ûm
«Ý\x0014	8Tzl4*<è°º½XÁ\x0010Ýº ¦+íîþ?\x001eORe¨KbÙÚ¹h>(ñÊ7Iì÷\x0017wÿrý"mqì Ã§ÙÌ}]øü!¸iò\x001ddq-\x001b5Í²\x0013SIsR«F*HKm+ã\x0010oqü(Î(ÉSX\x0019KAú¡6S,¡e	£,X!8Û)Ù\x000f`o\x000cj,v§³r\x0008'¶8qx\x0011GV\x0001ÍØèI_*DÆß NjqÒ(N ir\x0003:h§rÃ Mniòð2\x000e¼¥\x0012\x0016ôfnFdMÂf¦´4e\x0006ï-¤\x0007(Ç}i%ÊÝé<\x001cÁi¯SM\x0007ÿÖÀýÊucÏ\x0005¸É¹*Mù× Oïýqr\Ñ°ñ\x0011fÌ\x000f9oB¦<?Q\Ot\x000e¸§Hù©Y>Û&¸!Î%Ã°OÆîÉ<i®úÄÎÊ×¹lêT\x0006y:\x000cÃNÙi0\x0015ò$3ËÛT\x001eÃ·µâ6Ê<_aÇì¥!$á«ìãÅ1ÍÄ AÎ1Ã°g6õ\x001dð\x000cí#GúFGu§ó0ê\x000cíÒJàÞûzÃàï\x0015wÚbç)ë`Z1}ýîÓ/ÿøûßþñÿ~>YÌ\oÃÅÌ	Eæ´_áX&í+\x0011Þ½ùîêwWw§ËË:VL\x001fQ\x001fr&ÙD]r9\x0007mPoh»\x0001ÔQ8×Â9µå,µ\x0011ä$a#×ú\x0018Ô{=\x0000ç[8åædÒT±5Y¹qi7	1
\x0017Z¸påæ(~\x0002\x001ebW
Ç7ÆoÔÏTl±eZ6ÇâßõÚI´\x0006ÓªüUw\x001eÁ\x001a¸ÔÂ%-\x001c¶«Ïé¹é®Ë\x001cQ3'$|Gár\x000bµp§+U¸Ì	rÙ
v[[¯A+-ZQ/¸@E\x0015
^Ñ7ÜRj`?#7ÈÖÜÿYe_Fàêco¾\x0007V8/\x000e¾ÈG=\x0004×\x000eÊã!¡RØ|ë©7Ó@=ÿ¹HèÀì\x0019hèºã\x0001Ôç\x0003æ\x0003y?ð÷\x0012Oü0Ö\x001cYtÐ\x000f < ªíÐaWê¼!åtZ)ûúW£tÝ\x0001\x0001ê\x0013"\x0005ÊRÇl9óYF\x0004÷Än*u\x0014®; @BpGA5ÔFå(«nÖÐÀu'\x0004¨ÿ\Ëu'\x0004¨\x0008\x0014Ä§
Ë\x0012OèM¨I¼.ºc[¢;"@}Füç®;$@}J\x0004:÷ëm\x000e¸ßÈ'²[Ü\x0016\x000c)Ðlç­úÚfs%AL2ÃõVBÕ^¡¢ïêüÒuÎªoÂ±á,PÞ sB¨Zn£*¦bë<U{ú\x0016µ´ä¼[	Ð³4\x000cG®L¶Û­V»[s)$µjPÏØñ\x0001Æ5©S±ë\x0011ÛuUa³ýª°áS¶ð¦õÀ7âé
\x0010JÚ\x001f±1|#^3&5bb
ÝéÖ>ÞÀÖ,ös\x001f±ë^ÜÒõâÞ}úð§û/_>.­«ÿ\x0017YÈÑYCÕ*XÁ.
!;¡»7¯¼|ûöÍ3õueÝ[º¶Ü\x0001²\x000c|y\x0002µ¤sz\x001eàÉÆq.×r9ÅêðThë,Ï*^*[ãö£Aó-×\x000c»éØÏE*%q\x000e2íÌ@
YhÉòc&nuø\x000eK\x0006P#}ÏØ¢E\x001dKRÈ]1en\x000bKù{\x001eAk__}è\x0008[,Ü¹Â~Á\x001bîÌ°W;¶®~-¶÷\x001bÏ¤kë2»I\.¨@\x0018çW¾-Ô¡\x0019lØkS¿{ó\¢¶¬ë[íÝÅó@eêNG Ë\x0003\x001a*\x0010WÚ°-»\x001c\x0004r-\x001b\x0006ªç#\x000bYéU·|\x0017ök!ß\x0002ùq ?N\x0011\x0008ç=\x0001\x0015\x0006Û±<@¡\x0005
Ã@6ÎåM3\x0010LÛ\x0000í\x0014
\x0001Å\x0016(\x0003Ù¹o4ã	V¦°PÞ«¢\x001bâI-O\x001aåñ%Îq>4\x0010~õBm\x0018(mï@¹\x0005ÊÃ\x0006e×\x0007 I\x0019;\x0016¶Ð&2
TZ 2l¡ìfé\x0018ÜdÄ¢²5öÝöË<­Ç¶+ý¬cQh!GQ<k\x0018h¯¥c\x0008¨÷ÓÃ\x001aË¹húÅæG\x0019D\x0012\x0001
õÛ¹¦¡óÓ0ì¨}*sI
n2Ï=AÀRõÕD{%¾CD£aOí«{6³Rq\R\x000eË¾ßQ\x000e\x0013u\x001a]5ÖEöE ?¨sÕ0ì«]ö³Çl£ù03<Q¥h÷\x000e2ÀÓyj\x0018vÕÞY¢\x0019ï\x001f.lõ&RØBa¯Ñv¨óÕ0ì¬Q¿Ì{²Ä\x000c+åT\x0013m³YD³aoD£ñ|G3ÁËÞ?×D³aoíü¬"&ÊÒ»a¬\x0013\x0013íuú\x0010ÙÎ]ÛawïÀËº°¼áÂ±j¢p¦{´¿¶ÃþzR\x001d g\x0003EÑ*\x001bÕUW\x001bmó@DýÅzØaOÚl\x0014ù6µÈó\x0011rîWëÜ£\x001dv®\x001e²ÁÉWeØRI\x0010h¯öüY¢z§ê_CxÉ¢ööþñéëùþÓÓýiÝ^W\x00027Jj$±æeÆÉfäüÛËëÛw\x0017ß¿¹½<©ÝËL®er\x001a¦ù%;Í}ËÒé-43Ôæ¤U@\x0016*Cùúí\x000céø\x0002ðHro@­W\x0002*¶PQa©ºÓHO\x001fxñÓ.¯ÕP\x0015P©J
KQ;\x001eBYÃ\x0003¼Ì\x001b*ka\x0005Si©>ÙHø¸º\x0005\x001aë½\x001d/ë\x0007À8\x0014ô{O±ù¼$1\x0001Ü<ñ\x001e©´ÛõS[AÕí>Pl?¼VFRwssÖDeNéZSKAÕm?Ðì?»È\x001dºBÑüâ¥dÑuOª[ê Yëõ³\x0015éê¦÷ÁDe4ïY®Ê®}ºm*ÿ'®«/ÿöùñ4\x0018ö"P5KAE\x0005Ús2Ð¦zÜ\x0019íêíOw×/²ÙÍ*Ùò2\x00142·L\x0018\x0011Òt°\x0011¿ÑÁ¹\x0016Î©à&)Lê³1ñå\x0013o\3\x001cäÍø%\x001doá¼Òr>âl½Ò¦$®\x0003µy§"^\x0003\x0017Z¸ ´\x001cö`sð"ùÄ"\x00156+:¶Ø²E\x001d[Á\x0002ãEÕ²g8»3wFÃ[¶¬e3©7°Ì\x0005T\x001b\x0012mÚ\x000cCW±-\x0011¡É\x0018%\x001cmP\x0003ËÀw1»3ÅV\x0003×ù\x0011Ð9I¿ÏÎN.çBJæ9\x0005'²Æ;ãzÆèÂÚ\x0003þVýÃÃ§Ï|æª\x001f«±æö\x000c3i}Y\x0012à.#\x0008ë:Ìë«7w?<wÝ\x000fk÷+]X`\x0001HÄ è\x0017)ùÄ\x0019#Hë¤©
Ìµ`N\x00055å\x0004\x0006@#eë6à\x001aîÍxO\x0015o¹¼ËÑ EëïHùËs0"B\GT\¡å
\x001a.\x001cEC'|6eN¯y\x001c\x0010Å+Ì¯µT`±\x0005º¥_¦\x0006Ébä|ëE¹Ö\x0019f\x0015Vj±Ê^qÎwOëË°D\x000bIìµ\x0016=Vå\x0016,ë>d¤VþIïÞ\x0003H¾qÄý;ä XiÁ
¬þãùC4=4ÑbnÙë.\x000f
X{.-]£¾ÂÈ·\x001cH©&ãç\x001c#\x0012z·¯òû¡>æNj3Ç~RØ ­S_*²ÎïÎñ×cÈÍ²¬/sÑ­Yg\x000bTdã\x0007ç\x000f(\x0015ÈfV2Î2aæ Í:×\x000fJß\x000fÔFmr\x0001Ê\x001exÏ¯;\x000bëY)*°Î÷ÎùcN¿\x0003CVMfSéÉ:/\x000b:7[ßé6s¬UçäTëbJ\x0015XçÌ@éÍ\x0002?©·
,Q\x0011÷Éi;au>£L4\x0003\x0005»©ÀÁE	\x000fùÈÎ´ÝÎ´ºY\x00162ô\x00193XáÎ}kÖÏ¦A°¸¾]ÇþvýããÇûÇgJ\x0012]ýÇ³ÀL}\x0007$ãg°ûwÅ\x001f¯o.¯OW$2m¹¬«^®Y\x0006
µ³y\x0006H\x0006Åý ñ kÁ
Ì\x0015\x0001+% \zÚ\x000cù\x0016Ìk-\x0006$xS¸Ñ¯Z}¿ë\x001e\x0018\x0015XhÁÎbNädê\x0005§daÙ\x0001Yl]=¬\x0002-XÔE:-\x00010LÒó=Ömb@*°Ô%\x0015õ<\x0001fJ%Å],¶ëÆ\x0006ÁJ\x000bVt`uÀ\x0005ë7]^G¦4`Ð»1\x001f³Àÿ`\x001dK-áÿµ*ð\x0018\x0017¬Zë\x001fôîu\x001eÉt
k$
O\x0016r,ß\x0015mAG»[rÄô\x0012m©¬*úW\x0014iÏMU¿L;]··h¨\KåT¶*¯(SÝ\x0017Ï­+©ö¯;cT¾¥ò*[%óA4À×ód2"ú4\x0015[¬¨ÁJU'¬¡\x0001ê8×O!\x001fÖ\x001a¬Òb\x0015µ¨q
&VCêYtÍýÌÒ\x0010\x0015ô»Pµ
ëG¤3\x000e¡ÁÑs{æü\x0015\x000fÝ\x0007Õy.\x0018B®L#w
.uæÚ\x000f<q+¨V\x0017°Èº\x0005Çi¥(1~¿.¾\x0005kg
½3ýùñéÃÃÓ3SÝ<õßÈqÕµ(¿í\x0007\¾¾}}u{:D
°ö§ÐûÓÁÒ\UKÅz\x0015íU¯f»»q\x0010Ìµ`N\x0005f\V£¸ú9Xßl»ÏA°Ð\x0005\x001dX\x0014­ÒdæLMåâï<\x001cáJ-WÒqeê`¬\¥\x000f«3åÛ½ß¿H¼\x0008æÖkßukÿá¿¼~øðøñôôõJ\x001dî%\x0015ÑdÝÌaÀ®.^_½¾¾yfSºõÚwÝÚ\x0019¬Z,\x0008\x0017
¸\x00179\x001d\x001b×CÌTX®År*¬z*\x0018{ÉÜ\x000cÝY\x000byoù\x0016Ìë>d4`½}¯XzmZØ«ÀB\x000b\x00164`®$Ò2â¬«	§ïn\x0006×¨Àb\x000b\x0016u\x0016W©/4P\x0007\x0005¡yå§ÝCr+µ\Ig0 ùCST®æ1Î¦Ýcr\x0014,·`Y·öE ½\x0014£ì-O`·i×ë\x000f5Ù\x0006tbFg²Â!ÍRò=k$yñoÚUd\x0017\x0003\x001bÃêMCÂ­8¦V\x0019\x0004\x000ePçõHZ\x0015Yç/@å0\Ý´
E\x000eë*ìÈòîkíe°u^\x001eBW\x0019õí4R[V^w'·Ò\x001b~}\x0004(YX-ðþe\x001cÛâØQzç¢r\x0017¦ÑÔ@5îõ»Wõ1\x0000ãZ\x00187\x000c\x0013çá\x000fhÀb/õ2QØ6~¯@f\x0000Ç·8~\x0018§Ì%¤³q¨Þç ¢qÎ	-L\x0018\x0014ê­Ø¦PS\x000b\x0000mö
\x0006pb\x0013GmóÙxáxêFÎ¦Ðí¸\x001ag·èe\x0000'µ8iÔ:Þ¼¢/\x0015,7"÷L³®\x001f\x001fÉ-LV|ªfÝPÕ#p=tµÍ¦Qc\x0010§´8e\x0014'Â<ºâDÃ)'`©áúß
{åz/ã´§Yèkºå±E\Næ<+8Ê3Uëì¢\x000eát\x000e\x0010F= öB¥ec\x0019î¢¹\x0014è·*C<ÓQ¯BãÌ\x0013\x001c\x00150B*lí\x0000AnÃèF¯ÿìùU«Çså\x0011ÄÝ";¨/à¬ónÐäÝþúøôÜEÃpHØHÛ¼^4X ÕmóZõqù"mIì Q=Ðå+\x000fG-ü¶:}\x0004Åµ(n\x001cÝÑq¶O
7ÝfÆé\x0018oIü\x0018I=¾3Ðc\x0019:_·XËÓÙó\x0012Z0â(\x0018lKçw\x000f\x001bÅ¬«YÇHbK\x0012\x0007$*RÝ]æNæ\x0002Ûæ\x0011Ô¢¤1£HíÍ4J_\x0010Ü^­²}A ä\x0016%\x000f¢\x0014VêF
=a@üþÛé9\x0019A)-J\x0019CÁã¶2HØÊ\x0007î\x0003°;ù¯\x0001öpÍSï\x0005\x0016ÏÃ\x0003ëñA7ÊÂõº¶¬5^ÆXz_;æl½³$\x001b\Y¬hå\x0013mc\x0007#,·1w+\x0004fªg"É»º\¸\x0002d\x001b\x001a!é-y[\-n!á\x0006<iK:\x0013¥ó¶0æn±\x0017Ép\x000ceé\x0005\x000c^B\x0015ë$c,»AKå_Y$ë¾Ì3²y­<ÆÒy9\x0018tsÞÐ,)¶dyî\x0013W²êí×\x0017Ü>÷\x001fþòøô|~\x001d#\\x0014Sª\x0011wJ5¦M\x000bp½C]ýöúöù\x0004{^ß^rûì\x0019Ë\x0015
Û\x0018\x001c,í¸ §[CØßU`¹\x0016Ë)°¦\x0008\x001cÅ¹pº"÷\x0002ób»¹Eh°|å5ÖJ\x0008¹\x001eéd¬,ýXgÙÊ®k$¬éVÖÓý×o/¾ûôôôxÿù×p\x0001¬ôOcþrU1JNhg\x000eÇÛ«ÛËwWïï.¾{s{{}y÷ýK¶Å´ç`bý6\x001do1I®/JýÛ:éZLw\x000e&²ãËcf\x0007²Ì\x0015pf¯ÝHé[L\x0016&\x0017­U?\x0017é]_BÉ\x0012Üßë\x0011Ôb\x00163\x0019T"\x0019§¦Ãù\x0012±\x0013_Ô"Æ\x00161eÉH-\x0006SRöÒ\ö\x0002\x0012ZÈÔB¦s Q0_ØtC5><>Ó¦a\x0017
ÊuHÛ~ÐÄ»û§§ÏÏ=t¬Ü]«ô|ÊÉdÔíôI¡óÝåííÕÝõ3Nr\x001dÞ¶¡\x001f31V¦sdBs$TÈ\ä6\x0015?:4×¢9\x001dZZ\x001eBu\x0013Gº8\x0019nsi_\x0007{\x0014Í·h^iµ,3å0]Ç1\x000e,ÄýÜ£h¡E\x000bJ«\x0016f}Uó;É-s\x000c·[V\x0016[´¨´\x001a§1àK\x0003¬«Õ\x000c?²·â*\x001a²Ô%¥Ñ\x001cÇ¬\x0000<g\çÿ¶m[VZ´¢C\x000b§¡B}kÎóBK° mTÍ\x0014hÐ»5¥_óéâØÈ¥áVö\x0007r¢u¾\x0003ÎÃ%\x001az1idÐ\x0013ÝBÆ:í:JÖgAjn¥ïþô¿ß}î\x0002\x001f¼hdTez\x0016¹¢Ìéú¤z÷ãÕå»çnÊi}\x0008¤æ
:À\x0014^qsy%cOEwe3ÇgÈµDNC$Wv°K¨§ÈÄÎ²®þ\x0019gò-×0\x0001Ç*q=qUx\x0008oÖ¢9ãL¡e

&¹p\x0011ð2ÎßNvßön6H\x0014[¢¨!
\T\x0000ÞL]\x0010Ó_.\x001f6;×ÅA¤Ô"%\x001d|8 õ<Dâ\x000bÎNþs\x0010)·HYÑ\x0005Úr>²ö¸Ob&Øy\x000e2©hÌDP4@L\x0006ùt;©¾1¦&ÜÞÒ( ¥^\x0000¢[f¨ó|Ñút?×9AïÂ5>\x001c·?}<¤EZ\x000cµón\x001bdê\x001c&(<&fÿ,-r\x001c¬I_\x000f8âmÞ¦"\x0007¡:_\x0000\x001ag`,ó\x0014¹sÌ»$
!\x001b%ï¡Ü:,äVSÿÞ}Â\x0017ãçoÏFAÓ+\x000e\x000e\x0007>ñ2ÈkñÄ5ô
>\x0016ë½\x0008g[8««0kÆbÅ°}\x0008,od·\x0007²\x0012ÏµxNk»z\x000e: \x0017ªªÖ\x000b\x001cYÏ!»J<ßây­õ"ð\x001cNã-_\x001d"wû88qï\x001b¦\x000b-]P\x001b/J\x000fßf|`[1Þ¦PI\x0017[¼¨6²þºEÛÊ8ã`«t¯ÃK-^ÒZ\x000fµX\x000c¸ë-¦-'â\x0001Ãx¹ÅËjëÅi&!U`xîfAv§\x0014ã\x0016¯h­¼t¹@äÖ\x0008Kúô\x0018]sÊ»õ\x001cÀ\x0011ë¥Àg\x0006£¢Ü³\x0014Äxû¯Üa¼þÄP\x001f\x0019ÙÈÖÄ7\x0011^>}Öòu^\x0019Ôn9;9Ä¢\x0001
ã%!}"è3×ù=P;¾¥/ÇZîn¯g\x0014\x0012·ó, v-eg3á\x0005\x001f\x0007o¥$æDxv®Û¹ Ýº\x0008']
g#Càòvgö\x0007\x0001\x000fóÙnsXíæ\x0008 ³å\x000bmË¹±\x0015Þ×ñuÃj7G\x0008\x001b
H]­àÄ¹\x0008¡
óu»ÃjwGÀ=æË\!\x0010¥}ÁÙ\x0016¨¯Û\x001dV»;°ý6Q ^\x0011èÎ×lnáUòuûÃª÷G²R\x0002SQ]á>\NJº­\x001e½ÏuûÃ©÷GÊ¤\x001f6µK&ÊOI³äZÖL½;Ú\x0019r´Cú!r#ÎrÞ þ-\G\x0014\x0004çí¦Á`\x0018sÝ¥è¤KñÝçû¿>|þòøì|»µ¾¤,\x0010x\x0000BÝ\x001f|ºyp+´ww?_Ý½½~fº\x001dSÙÊj¨b¡>-\x0000Ç\x0002uÕ\x0001Sá¿ñ¹T®¥r\x001aª¸ÇzÒ¦µ\x0016¥\x0005¶¬WÊ·T^CUw¨eª@S\x0014ñvÇ{ ¬¯w
ªÐR\x0005
UñKhÐH¼Ìte}î+¨bK\x0015U¶¯xYYêËËY¿¹§+rËU«ªL\x0007Hk\x0015b\x0014mý|\x0006ÔºHËå>ZòóÃãÇÿøûi¬X/\x001eÓ°ë¡báê1\x0017×B(³ÏúùêúææêE2ßy\x001dµKB1°ìxZê½SÚM(\x000eÅ,êÈ¼\x0003A\x0006d½È´ï\x0007p\x0006ÉRK_³° \x0013.2µOFÞÛî\x0017
YnÉ²Òfi\x001e6\x0007ìic²K^c?Ý?FÖ>ýòêé7°Ð\x0012?LÁ[\x000e\x0017&ðqûÝ»ã ZèÐÒjôxlÓ£/ÙEyÿÀ\x0016n¡r¥QÑ\x0015BMV\x0015+q¬\x001cÎ\fe}Ë)íÔË\x001f~½zI/p\x0017\ps·ÚºýA?_Ý~yû\x001fÙ\x0016ÌjÁ"KçW¬åÊºÖoG\+¸\Ëå4\8\x000c&\x0001ÀÍÕÙ;)NÛª8Ìå[.¯ãr¬zÃÁ-é\x0005Ë$\x001aë·3£\x0015`¡\x0005\x000b*0(<sE\x001eµæt
iKÃT±¥**ë©Ëdªj¦Öfï¹Äµ,
,µ`I\x0005\x0016¦ö(ýåÙ'ÑãÝÖ+¸rË5\	\x000b1	\x000cSYóº\x000f.s4-®{÷U`¥\x0005+*Õn!\x000fV]«#°%³¶7ól«
0npæÅ Px´~ÊÈRì!dI¼\x001càê=¾Êå×/I\x001a7æUô\x0019eäEÞÅ8Õù{P9üýM¬
dY#g£Û½9ßÃX»\x0007¿G,Ã#s2Ýl$3ºÉ¼kÀ:\x000f*½ã¤v^L\x001e *Jy-C­"ë\x001c>¨<~ò,!6)£Ì.,\x001aé*Ø\x0016ähÀ:\x000f*§²§pSýnªG2\x001fyñM#¬sú òú)\x0001×R`v«©Øf°7|¬sû òû8\x0015f¤\x0019ÅAdr 98â÷¡óû rü8tdR§âÙaÄ õ³vo:ñ(í<¿Uyþ'7aé\x0002
=
\x0012yÚ\x0008mªÈ:ßoU¾?[ÃQMã
Má\x001b7ß\x0014\x0014jÀúÛ¾Êûçì¤c*ZÒyÊIäÃ¦èJ\x0003Öù«òÿÙEIaW¿6{Ùå©ë6R®*°Îÿ[ÿÏEêÔ\x000cúÿYì?e1Y:rµ¶ÿ·*ÿ³Q\x0006^ñ§ÌRü¸
ê+À:ÿoUþ¿Ló¾ÀäÀWE\x00144bms^#d~=ÏËd¾\x001f?|ýôùâ·÷ß>?||&üjd«ãAÑÉãm3¹äçë×ïÞÜ]üöòýÝÕÍK`¶\x0005³*0{\x0007\x0005æê`\x0017r\x0000Ìµ`N\x0005\x0016\x0003),cö+7\x001cÈ\x001d#Û\x0003\¾åò:Å%í¦¢ºÉ`Y\x000e¥µz
,´`A·Ä"W\x001b`ÕmädLW\\x000fbVqÅ+ê\x000cV(n1å)\x0003EQÔwë:\x0003\x0015XjÁÎ`{`çúè9\x0000åÖ2¸*¬Übe\x0015Vq¯¸«Ïp3G"Ïëó\x0001¬Òb\x0015­µD
ÈpsZ\x0014\x0001\x0011·®äÖp5¯p¿\x000c+\x001c\x0003Æ*Ã$óÏu\x0018Rcî;BÖû|¥ÓSÆ{2ôåD\x001fä·?@Ö9}PyýXOíÂí_kkªÍøÎxWè¼>èÜ~\x0006¹Ysò;HêÔ¯³H*¬ÎéÊëÇúfs<q;à^Û¼®\x0012Uu^\x001ftn¿Þ«­\x0015Q¸\x000c$:ñ\x0017GlÖù}P9þÉfÞÆfÒc¸tªÈ:Ç\x000f:ÏO±ÉfÓ[ÕfìËÂ³\x0012:ß\x000f*çß®3«B·,SÔóz(¬sÿ óÿ¥s\x0019T«ÚK)\x001fø¶;\x0000¬ò\x0000B·©à
y¤5¹À\x0013Óvþßêü	ìÿÁÊA\x0002Á¼V¡Qõw~¥ûçÑS¶>±ÅxÀ7ëQ\x0015Y·3­ng,FõN©ÜÅ\x0018+ÙZ\x001fWEÖíL«Û\x0000¬Î\x0005M¹gáÃÜÃZ\x000eBCæºõïtë\x001fâ+Cd1r]Â \x0008µi¹\x0003\x001bÀu§¦Óà¤Ë\x001c\x0007\x0014PR°6â*¬îÈtª#3ÄqH\x001c­+³ý\x000b£ëV¿S­þ\x0008/?òÔ÷1qÕ[§nT`ów*ç\x001fÁD\x0014@ö,·\x001f15BMwëZl
ï|¬WùØéö¤\x001c«¹ºÁÃgï.²^uÅ¹«Ç\x000bÍÓ®d±/\x001f×ùg\x0015Y·ü½nù×Åü-m½QÝp´ß(PuËßë¿M\ÏiëAîÈd¼ÆòºðBÅÕ­~¯[ýØ\B\gVIqÛF9@C\x0016ºÕ\x001ft«\x001f
åì+Y}\x0014"ãºÎMI
¬[ýA¹úEÊÆ\x0006à§oq\x0013Á¬Ë´Td}L·úr,e*¼--\x001dqþ¦/b\3?\x001a3p¬åqÏÂSÉ¸çy§æZbÄ§®ìñOÏÄÕ'Ç9¯\x001a£·ÂêËõÍ³¾þáö¹ úZaÄ§®ì\x0005$¬ïÅ\x0014ñ:Kêü\\x0007\x0018êq/4DäZ"7N\x0014\x000ce¸\x000cÖÒ9)h¥×êNßË×\x000c!ù\x0016É#9;Ké\x0018ôa4ú\x0002¨¢§Þµ7ê\x000bÃ@¡\x0005
ã@Ù\x0005	³
,\x0015jv$®Fb\x0014\x0015-Ñ
¢\x001a)L±é³y±ÒF,t\x0018)µHi\x0018)\x0004¢bRâ\x0000fÏï3Ø¶$\x0012å(+dÉ-Õ\x000bÌ\x0010°<a!N\x0007ìH¥E*ãFÊsN\x0014TW\x0015\x0015:9	É]ë°\x000f#µáèÔ\x0017½ÀzÖ³R½[yÃÙÂ7\x0005\x0013×i¾q¦ÎOÂ¸£\x000c.¾
d'7\x0007WÑN¢\x0008iÒf\x001aÅ0Sç)aÜUbåÜ@6¹'s+`EÝuÛÈ0ÊÔ¹J\x0018÷¸æ~¿j\x0011î¼ªëÌDÆ(Sç-aÜ]â4\x0013ªMË	x°IH×øv\x0006Í0Sç.aÜ_F,\x0012\x000fÞÔ!\x0003÷Í¡\x0006Ù¹L¿q^ÒSÝW=z©TB:w\x0014&F:	ã\x000e3.Zá	\x0007ÁQù±ã\x0001uõ¾~ö
ï\x001c&{Ì=`Ták¹/c£-ÙÉíVG0ÙÎcÚqÕÐìrT>\x001eK`;síd»Ë®\x001d¿í&\x001fJ{K\x0012¡9`U\x000bÛéÜ\x001bío»ã^¼n;öâ¹\x001e2tKÁ\x0001Pd'¿Õ\x0001\x0019eê¼¸Uxqiî5\x0005¤Ú&$\x0019Ý·ð3u^Ü{ñ90:Yl\x0012&\x001e°V_[õÈQ¦Î[\x00177EÔ`\x0016]@&/Å?n·(o©óâVáÅ±³qÞwõãââ õ5\x0010Ï¾\x0015ØÎÛq/\x001e§|Iµe/\x001eD)Èî(\x00022u~ÜûñT\x0004qöÕ+QõJ\x000e"!\x0003i]\x001agêü¸\x001d÷ãuãqçT.g\x0008\x0006#­-v«1Èä:?îÆýxÝô¤Öa2©ÚL'°Ì0g¿Y\çÇÝ¸\x001fÇ³^\x0008\x0005gd\x0014jµjðÍìq¦>F \x0008\x0012`g%­ñ\x0018ø^\x0000Eî*å\7î:éÆ]f6s\x0005ÈÔ_\x0013¦Sf*\x00007l¦ºàÎeê\¦SÄ	P­>]}ÜÍúÄÙ6ó¤6RûÃLËtã.3ahn±ÓÜã%ü2Õúì\x0007ë\¦\x001bw\x001eßy\x000e2iÔ×sÏ¬\x001cGê<¦SxL\CtË\x000c'¨×;6Ó¶}~©óN\x0011+eBM½Ï)Ò<ßb;ë	|ç1½Âc:/L8§¬pã\x0011÷Û³¸ï<¦\x001f÷Á[^WSá¸Hoo²ïãHÃôã\x000e3Ôw¯ç^#ÃK"\x0003µßl4ÄÔy'?î°uÙ7rÀR>\x0007çºÎ;yÅ\x000e5èÍÂ\x0003i²/¬Qiýºu\x001c©ó\x0004^ñ\x0006öFÆÚS`lzÛ\x0019y\x001f¬KB·ë"B\x0017¹ô«Úi\x001fÁå\x0014ýÒ\x0016|î}.t».(î)õÂÄ]\x000b>\x0012QÆ¹¬\vv¬ tïÍ H¯`¢e\x0003X\x001c£ârØÌ\x0008ÝE%h²\x0019\x001bÍQKÊQ\x000cZäþ6\x0015hãHÝ®\x000bºä\x0001\x0018` ò\x0019ÎIWënÚ\x0010S·í"V_æh8µ%ÓÕ)àÃÙÁ°Ø-¦¨\x0008AcÁ [ÉÒI\x0004\x0006	i#*?ÌÔ-¦¨\x0008÷Eæ!)Ê:9eÞnCÚ\x0010S\x001a_M¡	Ð%Ï7LeìâvTý0S·¢Â\x001b#Á°hZgöò®+gû¦Ôùð¤\x0019Ú ^l?&¥\x0015áü\x0008têxRÄç0eGuë(\x000b@g]òX»õ2ÊÔ-ñ¤Õï\x0015Þ.ê9®ûôÜnÏýP\x000c\x001a~ßE¡á7÷ãXsî4\x00061ÈíI	àü´tÅúeõËø)yhd®^¦¶×S#bççCîËB&w¾h)\x000e¼òÜ"Íaybº\x0015å¸Õ\x001fu\x000bfM\x0016, dv\x00102NÂ\x0014='t°<ò½äÑã§\x000f_¿J8\x0015ø,+ø`\x000cHÄÈÖÊ3Õ«wï^\x0006³-U\x0005^ù¬\x0016y×ßs
ñþÂ\x001fär-Ó\x0019ÌËdY*vJxRyçþóx\x0010Ì·`^\x0005æ£|É\x001c¸P\x001dG®p\x0011åZ
S\x0005\x0016Z° \x00023]+T¹\x001e¶^#Ù`»2\x0013£X±Å*,Ò>\x00123B÷ç\x0005æ÷\x001fð`©\x0005K\x001a0\x000býBð¼òkJå\x0016,«ÀêûÞ^P\x000c·óÀU$>nut\x0015`¥\x0005+*0\x001c\x001eÇõÃ[ôåO[yéq°¶Âe%{ô2Y\x000cRÙ\x000c2\x0016Æ`¥5\x0015êî;ýA²Þï«\x001c?NH 
¾øÍZ*uÜçu~\x001fT\x00120ç}iùvX´h¬\x001bAU`ã\x0007ç¯ë
Lð\x0014âÀhöï6£ã4d\x0005x³7ì1\x0012Ëð\x0015Ëo!ïwÕ/FÉ:\x001f\x000b\x001a'\x001bQF\x0011
ûþYaÂÎ£3\x0007ü\x0005t\x001e\x00164.6\x001c§\x0002!^cóm\x001f;\x001cÅ÷\x0001VRým\x000cßVuS¾ý÷o÷\x001f.~xøøíäâÂË!Õv\x0014\x001c:Dã-D¿Ê´×Ö·ÿýýåÝÕÅ\x000fW7ï_b±-\x001dcñiQO\x0004Ã
ÖÁp\x0018\x0019J;±m\x0000¦ºÐ\x001e\x0006}j!åãY5ôÿüÏÿ}ùù\x001e¯Ð'eC#êEO[°z*\x0017ù»9OñÐ	¹\x0002ò¬\x001ezqywWéê¡Ìè[F\x000ec
s&\x0015\x0019\x0003	¾8KñØ¦\x0014þ÷¿|ù×/é+¥§óå¤²zñúO\x000fO\x000f¿<>|n üo^þÇßÿúéÛÿ@¬êól®JÍ%û¹qöU]VÚ\x001f*â$]õúîêç7ïÿïß\¢ÒêÅë\x001f¯n¯¾»¾º{¨®sü¥!ªé^XìüúF"N4ùùi{6Pµ2þÒ\x0000¡$'\x0001¹¹O\x00102\x0015hútç\x0012a¾Ë+?\x001a\x0016WòG3ó¸*4\x0011\x00039«ÿfé\x000f\x0000ìÀ°ØV2ý\x001d'
÷~÷ñþÃ\x001eN\x0013ÕWo¦¬W½(ÏsuRT\x0016òËaÙq¢rïw7\x0015ëE ¬±ýpðE%»>Ì½c(QKsÈÁ\x001cbÂ|
Fi¤º©<¶âMeÄÈMÍ³ÏG²duH9s\x000b\x00086ÆùÃeCÓ¤ÿ6SD3E¥ê³²ß(ùgÈL»	r¢Hç3áúÊõãëèÓ¡\x0018/§ÅNG°T{ú¡A
^ÊcÓ¬òH1ò¦ýL_þ`sø\x000b]Ö§+úåÓÇ§§»Oß¾>\x0003°"Ï§pFI3ÇG	¹¥TÚ¥tyûúúêööêâîÍûw\x00034õã/\x0015½vÂk]i\x001cõNWåà|\x001cL"X
N0n^Ô3=#M¤Jê\x0019ò\x0001ã`i	þ\x001a§\x0001zL!ñ2\x0019øS¥ÎÇÁW\x0019ÇRÛ\x0017áÐÊÉ!Ap>\x000eziü¥À¡v¦Sì|vTb\x0018gÎµ'ª>'\x0019î¯MÆá\x0006UæðÊ4I]\x001eê\x001b\x0017×Ëd<\x0017¸ Mfã\x0014|>Sw\x0001þ\x001aÇÁÖXGÆ)sûnÅ±ôdó8÷l\x001c°\x000fÔ\x0007é§¢`t³\x0014&6OÄÅ\x0007æ\x00038\x0011q4æf¾2ádÞèÀWI3]ó§øÁþ\x0001¨³£ëçøþóýßº×õ&Ö·ô\Q[f3õô\x0012ìÂö\x0006ôöâû»Ëßx^·8±lKï_ÆÁÌg$ùF8ä¨8~{ùy\x0001ç×o\x001fÿúí3½÷ñ_ïóy|âgâ?þ×O\x001fù`\x0018ù/\x001au=×Gvd¢Ä\x0007Eè<s=È{};?\x0013¯^¿¹9õÑ\x0016,\x000cÔà/%W`¸ÃræX\x0012Ún\x001bË\x001eÂâ§«\x0016\x000b;`-kjÔ­T\x0019¨\x0014\x0018­U\x000ea¡±ñ\x0016ËÍý%åH§½ry*ÛB¯\x0014Îàòÿj>|úºÞzoï\x001f¾^\>}ýôøô\x000cT5\x0005}Á\x0008\x0004EPC©÷EZZeªÕ.÷·×·ï..oß½¹>1F®âo¨ªWWGa\x0011K{0 $­«»Çµ\x001e
"Þ*¡"\x0015'"\x0014]\x0000\x0002ÎU\x0014¨îP9\x0003ª~}.Ô@Ùùà­Gl½à\x0013\x0014'úÂ1(|¦Eíç\x000bfÖ¾E¨9W8Q6ï"%S]Ñi`VZ¨LÔh¹õ)£¢\x001b
Ê»¹C\x0000
\x0005s B\x0019'Pþ¥ðõ´Pnúdd(?!ÂïµìúøÓ!á&G%|a)ØT\x00013<\x0005pÜ1¨ºIrÑB%¹Ôù;AYöq\x0013PA\x0001&<¦\x001f**3g'S9.Y©8ñ4	\x0004\x001f¢Â\x001bpÜmÊg?w\x000f"<\x0016Rq\x0007\x001a~ÀuXBG­\x001dà´Tø6p´ýæ×DE\x001d×=úT­\x000eZîCàw/vëMmC¡ø²xªrh\x0007\x0002VP\x0003QÁ4Ï?À{ÂìµÐVËé7Ï,?
ÿ¥¦\x001fZÇ@¦ÂÑ]· ÀbÎqêÿúç\x000f¿üúks]\x001eT\x0017¿~»øéþó¿Ý?~üøéé¹ \x0013åÁè1<-vT\x0014ðËs¯3\x0015>«.¾ñÓåÝO×77on_äÂ×ôÖÙÐ0&ù-r\x001c4(Æ\x001d\x0004ÃgñÔ}­\x0003Ã	FËs=Î\ÉHà)ç£\\x0014ÓrùY!c;ß\x001c\x0008G0vñ8±á \x0018¶8:ýôó¬)66W\x0000!X\x000e\x0012ÇLG\x0018\x0016ëO\x0005û:0\x0012ÊGwaZÌ\x0015Ybé \x0018çD=XsÎ\x001cc\x001e¤WÁxd\x0005\x000bñ\x0018\x0018`\x0006qú¡#C\x001fFñ\x000c³Pß\x0014X¤9l>|Ðdoé¬DÈ\y)V8\x000b<%'\x000eaqúôC	\x0016ç§Î
{ÛÌe&\x0003wpù\x0003¶N?´dE2çXD6óQòÔîèÇÄ±9Ó\x000f%Y«çÌPÀ8x!³\x0007Éðüé¬8	Gâ\x000c\x0017Ö&×d°\x0007Áð
6ýÐE\x001fæÚ\x00164Yæ0òÔñÇ\x001f\x0013\x000eaqÌôCIV\x000cç±¦\x0008î¼\x0001l\x0010W9ºÌâ6êd3\x0001iª®Éø`ò\x0007MJ\x001a¿~èÀR}`\x0017¾U÷A\x001fÓY¨`W\x001fq\x000eÊHÔ\x0007@27,Ïd~N\x0003:'iÀ`\x000fz3·é¬z}C6Ë@y\x000bÇ#\x0010<N;\x0006\x00160¸8ýÐMó¨¬\±§^øhC2ü1S<Ïg|ùöë¯Îo\x0012\x0007ß.¾û\ÿ¦§ÃÚ@Úõ·a~âº$o\x00117\x0005
ï/°°ëºh\x0003\x0003Xâ	Rç9@ã«<±\x0018(Ì%»õ\x0011\x0003\x0019¨Àæ\x00119Lcñ0ý\x0018¥	Îpð
'ü\x0001J\x001cÇo\<@.Ã$c4aÜ]i\x0012MtÂ\x0010á§¬+Ó0
:\x0011k54\x00018¬ifØ\x0014äLnýhë Ä8
Æ/¬SÑD)×¨Ç2GÞA\x00025!o*¤icx&K(ÒÍ³Ê\x0002>W%j6Å,Ã0x\x001d~\x000cÃ Ò>Åÿ
¼\x0012\x0012ôç¯\x001aü÷~\x000cÃäôjf'²LH\x000c6a\x0018*sN¤æ\x0006`¢Í\isà
x: .á³··Ã\x001fg\x0015&z¼/\x0005)¨,±Lì\\x001aLE;é\x0019\x001f¡Á¦Lv6\x0005¬\x0008`Ûl\x000b²Fi"OQsHa@\x0002\x001aØÂ>uåà|a®ì3æl_3Õ\x0004N?\x0006a¢3í(Ô2
{¸19ÒÙ\x0018ÇLÿfú1LS"GíÐJs ^Ð3gÒÓ~¨ßþðWh\x000bÕèópñÓçû\x001f¾üû·ûg³\x001c³:Øg\x0003\x0005)È³öÈêsuñÓÝåÅÏWXkÿ"\x0018
®¨Á¬Ô³ÔÓt»V°Èq±hÍÎ]Z\x0005­NøK	\x001b~~ä\x0006
v"ã(\x000f¦F\x000fe\x000bK\x000bfó<\x0017Á0÷O°¢Ù{\x0015é°ª­²Ú^\x0016£ú\x0005~Á¢yË~]Âz\x0006\x0018fæ\x001e\x000cGüÍ»1\x0018Rê®`k%B\x001fr\x000b\x000eúMÓ
\x0002É8ºo|â8J(vçé¡"Ã.êé\x000cêù\x0002Ö\x0018i¦Dã2W(V\x0017wÔfX19ýPÚÌ\x001aº­`Å+/yÇg`È}Ù½\x001el\x0013z\x001a5Y6\x001cáñ(\x000c2LÇ.>p\x000c]ôôCû1R"Ø×\x0011è[F~z£\x000eÃâktú¡ä¢ÙÉbf¾\x0005G3I\x0004±Å\x000ez\x000c«tú¡#ÃT
ã
©=áuªñ½/GMêÄÓ\x000f%XÊb²`¨è\x001c\x001b\x0011ÙÉº|Þiù\x000f³_æc|ïüæ7?}¼ÿ0]w~~üøñþÏ×\x0014\x0006©u³Øá\S(5²Ý+ø§Ë×ÓççëË\x001fN¥N\x0017$î`Ò ÄµhÉ\x0017êTì<r¨êKä92×ÏD¯¨©tç£\x0008_\x0012øKE\x0014gÍ\x0012LúùQFrK´<êþãOÿ\x001dh\x001bêÿÛýç_\x001f+Åó9s,ºÌ\x0001u3r·\x0010
\x0008­ïÍWo/þÛåÝ÷×·§
f\x0017)¢äÉ\x0012P©\x000fS\x0007TþÉQ\x0003|x\x001c\x0000Ây\x001c^	d¹ cjÌ£zTã9ìºñe \x000fOöÿ	kk\x0014*ÏÍ?þþéâæþï_Cõì):\x00084C­®!\x0014BX³«7\x0017uýÜ]Þ\C\x000b\x0012>iAËeg\>ê	8¤]Y¿MUL(?ÈúÔ£L.´5$¹¢l\x0010ïµM¤PÅ³¿xþ×ø·WóÔ\x0016\x0003ôíÜçA¦úåY;püÛ9.\x000eJõQ_<};.\x000eÊÓsî|&¬Z&/\x0011ðä¬'»Tá¬ó*$\¥(êNÚ½üô[DKÏ°=òé`ò\x0004F»ïêÂF¢ÂOÀ\x0014¹ý"Ã¦ÖZ\x0005W_`Åa(T¤ÍÒ§\x0017øÜb)wÈR\x001d\x0002\x0016Z\x001c
N\x001a¬1µ	ê÷¹Û!;8â5\x0001C\x0013\x0010î Ô#ãø/Ùñ\x000b\x001eeÙ\x000f@Y\x001cbA¹Ð\x0003\x000b¯Îõ\x0019v>_Äù¡ãÅ¢¼ÅôCÅT7_roJt- Öo\x001cøqdEõÍºÃLÞ.}jfú-2ñÔ¶
ÖÙ\x0016
Ã\x0018\x0003­¡°Ó\x000cEúe¡øãUë\x001dq\x0008¨¿ñéÎ!Pü Ï#	ñ¥²AÝ\x0011+y|jN?@|\x000c¸0â6\x001ca
øÊ~¨êMÒõ\x0011<øÔ£k÷c²GÎ¼éÞ<ýÐÝ¡\x001c\x0017¡"ã;\x0014ç7c\x0008ët\x0015\x0014\x0016ºD§<_\x001c6'	Ç\x0006ËPxô¸

SÑko(ÿÀáþÌÝt\x0011¸Ëo\x001aVz>TÁ=W´\x001b\x000f[Tè5\x0015QÎC\x000e=~ÛG\x0007õøôáÓÓÓ·ÊÁ\x001fþü¯\x001f¾ü~WDQE\x0012:Á\x0017ÕÝã/Ïuh&<]bsØRõ_à\x001bpÊ]zV:Á\x0017ÕÝõw'[4\x0017 ©Ö"(¬Ü¡Pß*ØBáXJ6[y\x001a\x0005\x0011ugjP¥P\x0005:|½]zçý\x0001 ;E[u@)Êå	ó d!)=O]õ¡\x001a\x001ew*\x000bô\x0012½kH%þ\x0015Ão&r\x0007\x001a\x0013)ÇG±&KMô«dV\x0015jcDÿãÏþá?ÿ~\x0016sD	Ç¥i\x0015¯?z¶\x0019k¹c¡Umb\x0011E!ØïîÅ¸åë»7\x0003Ds¨IGd2±NãäÈIæEO¤K=A=\x0012Ë\x0015^¤à¨ìÑÄè@áA,¼\x0016í÷s.r\x0013ÊÁ\x0018JÔ\x0016\x001bäÅ¹ßr<\x0005ñÿcîmë8<ßWÁ\x0013Ð"<¾+\x0010(Ô\x0005	\x000e@Èºg#$\x0014jPDMU­æ5f;«Òlîæ¾\x0001ßdäGºGfyNxf-ºÌ¦C³Vý*2ÂÃÃ?þoN/].ÀÈ%q9àÓÜ¶\x001a\x0015¬Ú[?ý]ÿç£kú*ªvÎÙÃo\x0007§ìÅQN;h3héã\x000cW~¼j{Q:TÎ9»x»(ÂVq0]3ÎéÁÁ\x0002>S[þ9Dgjg½ß«Ôè§Áÿ_$4\x0010\x0006!cÔÖTTÖ®\x0002þÏâJÐ]'NòU\x0004G¹ª;\x0000³cì>U\x000fÆ¢\x0011]+GzpL¬u\x001a\x0001G¦³7éØGr{MØ\x0002\x001e¼h5H'Ð; £y^Úcö¢'\x00021;Ý¿{HAsPøà¸âÍ3«Y^¶\x001eçôà°Î(âè2]`Vò=kô\x0006\x001eLçh'âAEG.6
þÅHeU«\x0001·a;ûâ<>\x0017ù\x000c¦Çç{*\x001c²Æp½\x001dÔX9Sþ\x0010Øe]
\x000b\x001eRdÑÕ°_êåÔ
tó;òØD=ª\x001cñGíE\x0001òÀ]øó_þR¾\x0016vjùIzéôéÇ/\x000fßþùtÈw,²T/3ô\x0002P©,Ém;¥÷6è9^¿¾º¸¹8¿^ô\x001f+\x001aø©N/6Ü\x0012ì\x0010\x000bÀrëì\x001bqÍ¡Ûú"0\x001dªÙæ¹!6¹2\x0003	Éª¶¯\x0006)\x0004kê¯\x0005`hÁ©4\x0012'!\x0011£Ynè\x0002Ûñ©ò\x0010Í&Ã\x000ex6W1ÏhÖp	)ìÅ,ÅhMi¶\x0000-¿½iÑÂ û\x001dê×Ì¬Ûfúõ?þ\x0007*m9|»QÓúäì×»ß~?yuÿt÷ôË\x0001PD\x0007³\x0005£f]ã¹\x0017#¿ÐgTGÏ¾?}ûþäÕùu&<B¦ËûwøS\x0016ÀÇjÌ\x001cMrõ:¿>9ä\x0014öÚhx,?h6r'O¥\x0016
É\x000c'ÍÚÍ(öýô×¿üüû?v\x001b|n\x001e>\x001eë9*»z"-[Qà:döªÜo.Þ\x001cì6\x001aaj·u'\x000c\x001a\x0008Ê\x001cÄ¼:e>,»
0ð Ñµâ>&6ï\x001cJE$!ÉÏùË'õ×\x001fÉ\x0018/§B[h
>ß=ÿr(­ÊÚÖzÁ\x001b\x0007\x001c÷5\x001b\x001e¬oK´\x0005ïNo_/V\T*\x0016\x0013aA\x001c&ú\x000cñiè¿µ>oÙ'o?\x0016þÿãÿÉ°ôXNä\x0012«lZW%\x000elS¾Óõû?¼ùõ×²ZX\x0000\x0019j$\x000c=¬_ï\x001e\x000eÌe\x0012U\x000bT°?Baõù\x001bM«XBaèc}z}q½T/72í\x0008~w2\x0001çb^©\x0014C\x0016íBpt«5B¤jAÀf\x001aw­¯.fÂ¸×R¦X\x001f¾õ.Ó\\õ(þøÓ¿Â»úÏ'×÷ýö¾\x001e|?RrIR\x0019
®ÖðÀþ{æö$ÿ:ÿpe§Gô8\x000bÜ#e
ôt°5WÃ)D(¿ÿöëo¿ýÞt\x000c(7÷OOÓ±vd*àºÆZó±\x001f\x001f¸=¹9¿¾^zÀ\x001cS¹¿.\x000eàÚX\x0014¿ð\x0014\x001a\x0018Å/Þ»ç{Q¸\x0002µ\x0017%FqE\x0018º Të\x0006g\x001a:Qòel½\x0000ÅZ
TT2J­\x0018ô~5Ê´¾«\x0007%Ôjr±²:«å=\x001böÝ(µ¦\x0013%8Í:\x0011,ë\x0019ª²YtsÝ HôãÏ¿ý¹\ødÁÿ;ût÷ûÃý\x0013«­?¼ûå.Ö\x0007:®¡¦.k¯Ó\x0018\x0016µM,àìòô}~i°âúíÓ×GÑôPK©ålÉpP2¿@¨\x001bD'í«\x0003í6£aÁ\x0012þ!E\x000b
,¦\x001ai×M\x0000-ü\x0004_î¦eÃ\x0017¿ý~÷åKÙ^o>eWè°l¬«\x0015ùÒ
«vKS7|ñöýéÍMÙco.³#´Äôp§?Þq1U´^µ7\x000f÷ÿöÏÃ\x000fÚ¡'«NTÕ=4Ô©î\x0006÷½7m~Î.h\x0011ô£yþûßþ?_þ.\x0012èøçe¦yu÷ù3\x000fB\x0003Oö\x000bOºÿòåîcþ×d"\x0013ñvÇj	«\x0015VUâ\x0019TÅ-æ: eÂOwzûêüææôÍ»óçÕé»w4\x000céî»/_ó)ç(¤~üûÏ¿>ý\x0019qð)\þ@¦ìm<ùBÕÕfX#ýÛÇ§3\x0003e,?:\x001cNc/\x0000Þ(jz2Oö[¯®ßd\x0000ÄÉÆíÍÍRiµúñÞ¥ß LJ«/ïO^?þv÷ðùþä»ÇÏ_ó{èþóý\x0012R~î¨@u\x001c\x0001åõ6:_dÃþÎm\x001a¢×WoO/Þ|wõîC~\x0018/\x0008Ó©\x001fÿöüpÿ\x001f÷S§ºîï¼Zç¿?üüí»ÅÅÂþ9Wº*°\x0013§ATÑÒÀ
7Ìþb´ºÅó¢¿¿8;?]Z²	\x0018eâ`q+-2±ÖÎ\u\x0006£\x0006ò
\(¤jÅ\x000b\x0007ª¼pàOIëf0Ç\x0003c¨N~\x000bWÄj8ù¬!¥lÈé+REUþO2\x001b©XáZºZµ\x0001K=¯VÝ^^oýÜ0#\x0004Ãb=^._jä\x0010ÌG`°áM"\x0006{¼ûÇïjÚ1r¼{ÈüÓ2\x0014xKih\x001f\x0012Î\x0010B\x0015$ÊV5ÎB¼»Èæ~¾é¼AB-F\x0019Ktß\x0014¤\x0012Û\x0005\x001c¯\x001b+RÚ4\x0014{Veu2ÒP-[8êæt?~3ö×¯fúîx
?<Ü?ÿ-_>ßþÏ\x00013_È\x0006Q~\x000c\x000cÍ!Ud´4©ía+Öùí¿
³·âqë\x001co¨¶ÂWøPÜÙ<Èeskg÷
ýí W-] ý¾ã(\x0013í³ì\x0004\x0012\x001eÅR6âÑ\x0014\x0015KgéÈ7L}A¼ *\x001e¬Æû\x0018ÿþå÷ÿl·wO_\x001fî¿.»9ù3rMtfxæ/l©~.ûAA·NÅÛÓë\x000fW·×\x000b¡\x0003õcøËGø)¯-ºTÃès½Ë\x000ehöå­)§ÒË"\x001fCê@4\x0000@ý¬ÆÄfs¡Ëõî<¯Ìõ\x0015}~Ö±Sëý\x001dúã\x0018Å~úöÇÉî~þÏçû\x0003V>?nÈ»8ÔÚ\x000cÞ\x0003\x0007~­nnküh§oxâ«Wç':=ûo·\x000by r0¬+)2±XhíX
¬\x0005m6 ÏÿßUÉ³c\x0011k¬ïî¾><~¾ûtìò&ó.PYM,M/<Ê\x00024\x000b84*¿;ýpqõî4ï¸ü¯>\x0010+±4µ\x0005c4hØoÅ
aq½\x001e\x000b\x0005¥^?DXfâ#\x0016!w±lÅ²&mÃÂ¶ò\x0008+¿bêJþ%&±j÷S\x001b©pÖsùCB\x0015ÒºNÄ6*Wìa\x0014c7bá3\x000f\x0014+°(dÆ¥\x001e\x0018±<ö\x0005ç·íxÀø\x0016z1½«¥¨69:\x001e7«Åâ\x0010ÍÆ\x001d¦\x0001¤ö\x0001ew qÄÎ%¢rº¹¥MßP+|÷\x000f
°bþO	Öd¬hHæR2\x000eNùm[^£|ÐËáO	\x0017Öä\x000cÎ4Ni.\x0013à0Ë>X\x0013XU©psaît2PehìA$ö
ÛÇË[¼ü)â\x0002nD¨¯WÔ®\x0000\x0007Ü$ö§÷Ð
.ëUþq)ÒLÃ¬ÍÐK\Àß$Í×s\x0012ò§K)r	Q«Ä¡ËP7_zãw,j?Ö	¹0
ÀÎ}\x001c>K\x001bÃëµÑLX_¸¼\x000b»< r
\x000e¡ÒzRÛÎ£-µðåO\x0011W¶ð¸4ð¾·K÷´ÙæGè"|3ü)âÂqeiäò\x00033Õ~m´\x0013®T6?E\*]äÊæÞÒzæõòÛ«¤?%XÆ%jî8³,
XÆÕ'·ÓÛ¶+æÞIÍ½±4,òrñ[;{Ã\x0014aãíèõÐ\x0002"]/\x001cÒG!
HC1`jÍÄJ0{ó\x001fÿ¢dék+ÖÉÙão?Ý¼ºÿôi1
àRÀË¼\x001dnê¼X,\x0013\x001cÒÔ5än¬³«·ùöêüra`ßHhí°i\x0016ë$D\x0001®ÁÒæëÂùÙês)rTÆlCÌÿ¦	"d\x0011-	ÕG|áÁ[§®Eªc]OèýÐ{9ad§B¨ÈJ6ºµË-À6ÄìfO\x0010£#&Å¯\x0014oÜ\x000b\x001f\x0007Dk81iÜÆ­\x001aÄ´\x0006$±¿b¨GÌõm\x0010-l\Ål ¦Q\x0018±d2\x0011¢\x001a
÷3¢Q`hÛiÑºÙZË7#Vã%Ú\x0018æ£/]kÌÛ\x0010Mc\x0015ñ§\x00181»Ã\x0010Q£p0:ÂXâ¶1ÚÐ0Ú°1UFl"ÃXû'R­åzÆÐìFü)ft~(VA)Ð\x0003°²\Lzãní§+>µ+a¨Õ ò¬qJ t\x000bbkvô
»\x0013½¢\x000eÌ\x0018KÚ\x001d\x0019
éü6Û¶ÿ7Ný\x0008\x0005rÆ ÙaEÆÒ\x0003Xß\x001e*ãÚKPA"½µñ/òÚøéîäÍÝÓ/XÚqÈ×\x001c\x0013pùÆÖ|\x001dìÄùÍxyzòæôú5Öv\x001c!4~Jh¼0?½-5¹#\x0006\x001d	¾¦wa\x001b¢m\x0010í
Ä|M\x000f\x001aÏ8âÔaJ\x0015¼µý¾AôrD\x001c\x0016Dw`~ÉñqÉÎ{\x001dcü6ÄÑ0"bk\x0017û\x0010\x0001^PDÖ
r\x0003ÆJ\x0018f}~ÂÑ\x001dCÂÖ\x001dë#Ô:S"Jÿ\x0004F¬[1ÀFÄd§É®XÄXß.ãÚÙøÔ\x0016Î`f\x001d\x001eDçI\x0002düF\x000cäùäýÃã§CÉLá;,`öº^ÐúÕBNfØnOÞ_\]^,e3\x0019Ë4XF\x0015p\x0002\x0000\x0010V`¬ªà Ú\x0007\x0019V)V\x0000\x0011\x0016\x0006\x00168+gØoU\«\x001dtX½\\x00137\x0006¹\x001a7æ8XiÇecb(ìSÕåÊGuÆ$÷a¬wº¿´\x000cXö\x0002\x0007Ü\x000fåd>Õ¡èy÷Ï\¸GÁ TqªùP/Ñzüõþ3Vtþßÿù¿Îûééùórî×äw\x0007üdGoô\x0005ØÃã	v<\x001fÎßaIçÉù[3q\x000c,LÁ\x0010Ì`\x0006\x0003$°Íu¥ìj-Vb%!\x0016\x0017wf,=` \x0016H§ÜúõÒÍÔÂ/wÓ``!r\x0010\x0012{¼*Ù@æ\x001b2/\3OÕ§\x0011((^3\x000e\x0016Ø¤a5\x00194k\x0006Ò5KeâLY3?LXAáx¶dn5i°\x0010ËÓ©Xt\x000cÒwBëåÒj0k¦`¥½K\x0000\x0016¸5/É4Ôe2ÏÊy6õ_ÒAcÆ@H¨\x0013#b\x0015\x001cEõ¢7¼fa½½p­}\x0015~Ë\x0018H\x001a./\x001bzt3XàA+ø¬^Mæ\x001b2/$K¥Z¾i.cl.Pq{5Wl\x000cY~«Y½=bAª\x001e6YÒ\x001c\x0015³aý·ÔÓw©\x001aºX$hVUëï\x001c\x0015_dy.fv\x0014WLhO&\x0008&VBÐS\x000f/®v)Xç®Y\x000bjµÑÀ\x0010Ð\x0014-ÉÐ¼VÔ\x0019\x001eu\x001c¦df4íøgUû:éCË71Õïñr\x0002vÿ¥T1þý@Ý >_9\x0001I)r2lÕLuÞù\x0019²óRËøïå\x0015ÎOá¼\x0014\x00157J&bì\x0019ëû¢ÝpZMá°\x0006AFghªn4~Æ.tºÒÍÒ~ºfé´tí\$Ûfð\\x000c÷ºõèD5·ãºáL\x0003g¤pÙP1¯Éw8\x000fÁZ®
u1-t¶¡³R:c8;k}\x0001DgXÇÁÍ{kÝtã5tÓk¾\x000eX´3¢3\x0012éÄç/Ì¦mçcsb£\x000e\x0019ÒÚeÏ-ÑÚ)UêRÚD\x0017µÒµS<Z*ÓÅ\x0017\x0003áª\x000e»\x0013\x000b²\x0011"d+\x0011¢n6\Dcò0éU«ÉéDä\x001bd\x000bní0þÁÀO+\x00127¡\x0018ïXFû¹k¿\x001bÏµØLqÆ3/
«=[;£+-·\x0018þ{\x001a<Ñ%ñÆ*:«,W×Yâ\x0004?×Òùvñ¼tñ t^¼Äib£|]¼ÙHC7^jñ\x0014J\x0015¬ÑÅ½Ã4M¨Bå6l¹Æ°c©a\x0013\x001e,{O8*GS¦Ëª£®¶ÜcÜàáO\x0019\x001e	M\x0016¼Ä{°<IÏ·­b<h\x000c\x001eþáùD­¨ÓB±]0Ürî·ãü/jètñÐ½£C=cËÉ`[ñÌ¦Å³íâYéâYÿ>-¾Ã\x00068eªF^eÊ,õü\x000cñ*ÿEéz¸>yýðõäÕÝCIyÜÜ=|þzòöáç_ï;\x0005MÂDGqô¼-\x0019\x0003\x0010i*\x001a\x001e	ãåÅùíÉë\x000f'¯N/JÞãæôâÝ·\x0017gß/\x000có\x001d\x0002\x0000í\x0013\x0008\x001f\x001c¦Ê-\x0015á\x0003I\x0019\x000cN¸bq\x001d½ªÑÌ\x0008PÈ\x0014¤æÁ¡|Ìeõ\x0014Ëj\x0001\x0005ÍIÁü\x0006ãhNªz¾m\x0019\x0011rùË¸<§|±[©î;Û´ýÈ°\b¹(Á2\x001d;Tn¥|L²Áñ\x001d\x0016\x000b\x0014O\x0017\x001eÿ¢£ºÚ(¿ôéî÷\x0003h\x001eT\x0019äXF`:JçýÅR66ÏÄQV\x001bõ.Oß\x001f¨\x0018>æ¤\x001cÐ)x#ÝÙã¯÷'§¿Ý=\x001dZ»È=SÉj5\x000cáÁ\x000eqÏ\x001dââ\x0003<»ºùp~r-Ê\x0011FTÍ0âO)¤×\x0015£°q|(ÂÊ«ÈCÒ\x001d\x0006\x0005ÖBz\x0016-\x001eÿb/&Èï¾ýñéáoÙü=þçó\x0004/6Qñá¸®ÒGî=óÍ\x0008¿;¿¼ø·lö®þÛí1>g\x001b>gå|#Äù\x001d6(d>ÅÓü|ô36E@8:¢Ð+1!8~\x0003¡Äðàîù¸æÅÇ¦±\N\x0018[Â('T®(ß5\x000c\x0008^&\x001cg\x000cÅ¦äEB\x0018ÀÊx³ñ2Óãüåä»ÇçO¿`ºõì×oÿûëýÝó«
\x000c+?\x0018¥KÛ\x0000^mìý9«çl5ú\x0008ß]Ý^^½»ÁôëÙ÷§\x001fÎOo@Û\x0006Ún\x0006Ù`´~AÉXKÅÎ=ærf­\x001bfü¹\x0001Z±¶;ú\x0013T!Wº¤lR3Ûv\x0015õÄ\x0008Ö\x0008È©­ã!PØ¾Áùe¶WÎéíÔ(nÔæónWúÍÓÝáÞv»Jê£\x000fUÔ!qÓ\x0002;s¹#èëÓC=î\x00070Å\x0003òiÇ\x0007|Ò\x0018Ê¼ñ:*XØ²tÎOéÒaldx£¢Hg3À½&ÊÆ\x0019«/àófÊçÏRª7eÛJÑhëê¹y÷¨\x001b/4\x001f7?n~g%î\x0004S,`VúXõ½àÅ\x0006/ñXm4ãÙah\x000bâ%\x0016ØönÛÙzÊ\x0017µÏrÑ\x001b6ÜReztüuÃÜ3¦\x001f\x000fûÊ&x¥ÍLÆ\x0013xK2ÿÛ8DÐbÍÉ\x0001A7 ¥ù °ä¶Âæ?zp9Å-Ya# i6`á*\x00034u13ì0û8\x0003òÜ\x000cè6}bp- \x0013\x0003:C±ël`¸9ûµ	pîi(à\x000b¡á\x000bAÊçòXtN\x0016&=õÀÂÖ	\x0018\x001b\x0003?¥ÃÁ\x0002h«à\x0015Ðn²F7&\x001a
\x0001S Ö¤"Ø@~Á²6y²\x0002Ð´â\x0015\x001cnL\x0017_0ÐYÖ«ËOâM'Ø´&ÆÈML\x001am`\x0002z(`\x0000¿¯NÛ¾/´ \x0005Ì·Ø\x000bZÀÄ\x0019O\x001c_N\x0007\x0018Àlû¼£S]øvê\x000e>lm\x001a\x00005æw¸òd\x0004L\@K\x0018
\x0001±b0\x001aH\x001cbmVt`íLl¢\x001fÐ¶\x000e>þ\x0014\x0002F ¾ö\x000cè¨Ã j\x001eÕ\x0001ý&\x001bhMsñ§\x000c0\x0012Ld@\x0016\x0016B½¨ÄaÓ!¶­jÅ~*¶OÒ\x001c{]$\g¾ÎÙ\x0006úÕ·-Êmz<$ù«èé\x0019)R[\x0017_~^n¸By¹È9PÓ}I^®|Dm\x0017Â '\x00177g\x0007º­\x0006:ðS:ðRº¨XEÇc¦lsu\x00109Ì?;á&u\x0019Î\x0014.)n6ð¾¦C¨­Æ\x00166,\x001e« ÊÕJ¢\x0001µG*±\x0014ylªç¥lÚfdÃ<¹-¿9¨'\x0018Å\x0015dQó®KJoÁ³íÒYñÒa¥\x0011\x0010^öa\x0008µ¤m«b#¥\x000bº¡\x000bZJg#My¨½Mû.:N¾'cfoN¼\x001a¼¤xÙo¦°\x000bN/Ö\(¬Ùðm¡=\x0016 ?\x0016\x0011¸6\x0000çJXÂK\\x0016â.x¦Å3b¼ìIRQvå9½47Ì%¯·à¹Ö\x001e;©A¶ÚrØ%ß²ÜZê$èDãDWâÅvõ¢tõ²\x0003Á©hÍ³®BJ0ëv²¢
­/ÜÃÍ&¦J¯QaªcêÔ¼·ÜGgZ7ÀýÍ&a8¬å×8ð¨:½å23&4x&Hñ<OÀÕ\x001b&Ó ^Õ­3\x001b\x001c\x0001\x0013[º(¥Cy±\x001aLd£â:òüN÷ãûð¬nðð§\x0010\x000f'
	\æc8Ú6¬mm\x0015Ûìpï\x000eNI4\x000b¯«èr[è|ãªàO)ãb-´\x000bô\x0004Ò<WBk·á`Xß~[/þ¶vTøÊ7\x001b½/´®ÒP[®\x000bÛÚc+¶ÇØûÁ;/Ò1t¦ê\x0001ê-\x0007Ã©æÛâO!^àTlÌ¦F)h\x001bªò÷\x0016ì Y¼¢Ý&£CeSàjC:°Q;Ï;ÏnÙyÎ´¯\x001f#}þ¸h©\x000f6aí;\x0004
pH»-O\x000c7\x000c\x0014<#þ¶*\x00022^ \x000cB^=[5Óæê>ºñ\snñ§tõB]=§©a1¯\x001e\x0007÷t\x000fîuâµo\x000c'~c¸dJ;,â-âqËÏ
vÅ«fïáO\x0019\x001e6n
ÞJR1U£"Ç¥´ªtâéæ	äµô	ä\x0015k\x0012']ø¨£g<°\x001boO®\©9Ðew*ßòã¸ò|-G/iáÄç\x0016GËy¢ÓÃèH(Âr\x0004·Ò\x0019?\x000e\x0013dÆ¿x9)%ûå\x0019K{ï\x001e\x000eÑgÏÎ²¹æ \x0000:w¤\x0000³Q[,í=½8\x0010Æ+dS{\x0012_NÍI\x0007â<KDWo(~
us&M÷ééY(9-AShY¢Æ³tWö«høì\x0015Û6Éÿ Ú4ÿÓ6ö¥¢ú4÷	F]Ñf\x0013¤hÓ\x0008Yl#d\x001dhX¦ÈæUb*G\x0016åðzÎ¼õ¢¥\x0016-ÉÐ\x000bíPÐd9°FÑf\x000fh'i÷í5WhHKQ[àÖÊ°á\x000cøËË¸­
+Øb¨«
CLsH/Z{\x0006¼ì\x000c@zÁ²­«Ù­­²­ÑmØg±1¶øSB=^jXô*±¢¬\x0005îâ³ÿN²Ô®Y­r,Íá³áUD¦ë\x0018VµÁÚ\x0002è)\x001aþìFÃ^Eà¡$\x001ejw±¦JÈÎºäh¦¹¢À\x0008î¨ME$3ij\x0000ÇøÉháõ\x0017\x0001LÄÞ\x0010Í{\x0011Z~B³Ø©s&\x000eÆÚÇÍ!ö¢µ«æe«fÃ¨q
\x001c¬6V´ç|µ£h¾´(L$'òév«=>z8¤Ñ?"m5Þnä\x0004\x0013õ\x0013k³py^Ý^^,«:\x000c`\x0013V¦ÀP^:]\x0015\x000b¬Ñáæ}½`¡\x0001\x000b2°\x001a:7ÎQ?G@¹\x000et
K\x0016o\x0019eß\x0012\x0013JÔ¹>*Ô\x0018ÅK\x0016âÕè\x0000ÓJ5L)\x0011Y¾ÒiEËö,ZÃ\x001dÿq\x000bÙDÔªl'#såR*½ÃºL\x0011\x001aêc¹1|>"ÝfÚid\x0013]Æ±ëËÞGÍÀV¥[\x0006-\x001aÐB\x0015uÃ\x0002J.ÉÆ\x0000\x0000¡Íµõu¢oV
JÐfY7g5·ªe×ÝGëqéE\x000bEÃ"4(\x0006ÄR#Y\x000e\x001eë\x0018Ì\x000623QÍdøS@fQ#ÔÖ5pxÒ¬ÌÿqáVïB\x000b-ÈÜâ©$áLÔª¯TÅ^w²\x001bVÍµ«æd«6¢z4í($Ã\x001diXã·\x001e-Ø\x0006-X\x0011\x001a\x00046k>³DÖrÕûõ¢¹\x0016Mdq-\x0000\x0007ë=¦Rér%Uö ·ìµØ®Z­1TÇÝ´!2YÁ¹e>Î&ûÈlë¥YfyÐ@p\x0014J\x000bÉ³èhvl×ûBÖ5+flÅáÚ© ÆéÚ;ÆÙ2N2ßl³&å×CV;	\x0003ÔZv°,õ'`PC´(òlLÔ\x0019ÑÒ\x000bZ3\x0008|6Q0g=Y»hQ¶hÑQ)zÌ·\x0011§\x000b\x0012\x0005×smø©ÝiI¶ÓR 	¬1XEj±IB
w÷¡9ÝÜ\x0003øSæ´*±½RÈ¥j\x0005:ª{\x000eh\x0011å\x001e4Ó|Ð\x0012g ¹"°Uª¤\x0014yÞQµ4[|\x000eçS?%hP3ÞXÀå4W30]
)w¡é\x0016Mdmóß³\x000f=
*¦ÍhÀ\x001fÔnx|ºööt²ÛÓQ\x001dc)Ü2$Ý*\V¶áMàbó&À\x0012²üú¤ÙiQ\x000fO1áÕ¹æ×Oß>?½ìùy\x0001CUGÙ1
)ã\x000elZÒ\x00164Ý¢É¶Z~\x0008£\x0016\x001eËRxZT³E hº±¸^,.æ\x0005<\x0017º©ªª	¬]ÒlÛO'm,®·2
\x0006éVeOr>Q;ÇM·z§æ[ÏÛË<o?¨ùw3îµÂmYómxÈËâC80Èòeª©"\x0018®\´K±ø\x000e²0i#ÌdÁEÑ¢¡L6ÍAµ+ÙÛÖ\µ\x0018Í\L'ZH
ZH"´Q\x0014cßCè6£ÕöFµþ|FhÈ"ÈÈp2+õmåè]DÙl¨uEë¿gl\x001fíQöh÷\x000b)\x0002û4y8s!×ÎØ\x0006o£,zëó\x0004êetêcóÂ;F\x000bKùÅ\x000e´\x0004ÍÕ@tµûä¸Cq\x0012/\x001aÅBF0[¸{\x0014Ìá\x001fÙù~9þÅË\x0019vòîþùÏ£0$\x0000s/HË;)Ï#j\x000e\x001dwç·ß\x001d\x0001\x001c§." 9\x0008Ç\x0008QHòÙñ'Mooë nuèyÐ\x0018\x001aÄ9+r\x000cÑ\x0007~]af%¥4N":t3ô Ææ3Ï\x0005?!æ÷| ¡X¾êï§ÄÁ¼lJ\x0007ãD*\x0015\x0019Tª\x00142Ù:%ÔfA\x0005\x001cÜ
¨­µ\x00112´36æ($pÊÏEÃÕYj2¼k¶aP\x00029êA\x0015H?ã\x0013\x001fÄö\x0012Í8g*Êcà\x001d\x0019f÷E©\x001f\x001b¬Ü&uw<ô°PI×ºA¦&íÊ¨§"£Nïï¿>|=9ûôøåäòîç_ï?\x0010Ýwo\x0016Èÿ¨XïuÞL\x0019#ùþüÃÅ³Ë«ËÓ³ïOoß\x001fA\x001dKX
*¬bµÊ³v\x0015\x0018Ë\x0013Ç¥x¿3íÐÍµ¬£#¬\x0013?ZÄýÄ
ÅÆ\x0017ÃNN±s¡TC³\x00014¬Û\x0002\x0016\x001dÄD¨ôj1²\x0017+ì¿56«ªãºe-\x0015Äª\x0006rª¸gÝÀLJVÊ:UaM¤Âº\x0015=Ýáhé¤(Ý\x0018µ§x3ÊÎÄrÅ°¾Ù\x0004Óê\x0013\x0011l\x0014rK:²\x001eJÔ1pÑpaÇÊð\x0002;©\x000cÀz\x001c\x0010LÊ\x0005\x0011jcG~é0ì\¥\x0018vH)°\x0013\x0014\x0011¬¶üàÑÁ²\x000e	¨
\x001bçZ>¥°fTìAX3Qì\x0011Áæ'-yóN¯\x0017ÁWI\x0008?ç£ô³Z]\x001c¾±J;ÿÅKÓ¤£ß?~þúðéÓÝº¤JøT2\x001fF4(B\x001bË\x0002Ûz!\x0015ñþêÝËËÓÅÒ¤Om´È§\x0002*Ïþ¨5¡\x000e\x0002¬¹\x0012ï\x0017üÑ^ÀQú£\x0000&-\x0004,	9\x001e+Àý>EW4Ò¼×	\x0008cu\x000b\x0002B[ÝÒ\x0003hò>Tà¢ÈÅóÉò£ÃÏ§t\x0003:hVÐt\x0005QÂ\x0006Ë\x0010X®Ø¿µ	Ð¶V\x000c=$z¶e\x000bCú8>_ë<Me!B{/ßkÅù\x000cÊ\x000c/ûû§oô©M\x0006\x0016ÚÆâGRáò\x001cv´ÑÌêüeÊëó\x001e¡É\x0001uRÐWVd\x001d+Þ4©æ©\x0018Ò[.\x001eZÐ´\x0010¢N\x0019µÍ5
P©\x001f#P375s6ß/*£ÔÓ²á¥\x0006µ\x0012\x0013#\x000b,%\x0011¹&Ñ×´íl\x00145´¨a%ª3üäDT=Xt¼/ÿ¬65¬6­dÅfb­Òb«c³qX¸}$°©Ý\x0003ií\x001e°ºê\x0012@\x001dÏ	Y\x0010#ÍêË`A5»\x0000ÔÚ]`\x0006¬[²|¯»h8K¢\x0017Âu"Xh-+¬´­\x0008\x001b9Û¤(\x0000a9f¬`¡½B\x0004ë=\x000b~íU\x000bôÒô\v{¡ÑoF
-jXê¢j[\x0000\x0016/E=gÖ3öÁ\x001aÝ\x001c/£×\x001e¯¼®¤%¬çÚ0çb7X(\x0014\x0016ÁNÚF\x0010vÇêU)
ÅJÓÕ²,¬VKN©Õ47,þ\¹°O\x0017&Ø öc2,,´ `mc
ðçÊ\!²ç\x001f¨\x000fÒFÎ¹AÚî\x0015àÀ\x0006Ö­Õ,ý\x001c\x00027F:ÃýÁÚ,48XC»\x000bÂÊ] òãÉS^N¹\x0017zÕ-\x0014HXmhL\x0001þ\Ç\x001a\x0015Îpó:Õ¬8jaûÂÚIÛ\x001dÂ¶mw\x0002Ø\x00109Ô«uà	<ÎTùÛ\x001bëÚÖ­½hU0T\x000cS&etPûíÛQÆ+aÛu«\x0017Ö×©\x0004í\x0019ä\x0015hÚ^ÖA:,Kî"£\x000eÍøW?\x001dî\x0002( JÕà&ð¼o¸¥vAX±)ÿêÕò|\x0017B¤å±`nÆ1ìAÕ	Xù«¼c\x0013=\x000e¹\x0013!{\x0007|>Ô|£LQñç:V\x001bX\x0015ÇÇÈmM\x000e\x001b\x0012\x0006VèyÐÉ:½¸2ëÜÅÕÅRT\x000e­j¯\x000b\>Í¬Ó$~fu3~a\x0017«®sCö\x000bÉ
8\x000e©are3ê4S$\x000cUAiÃ=áÎ*.ßÓ\x000b.\x0002VH
+ÌÅ2zX®(£²Ü~dùÅ*È­¨Æª)*þ\
Ðcé!*Ñ\x0010^VØ[¨Ö\x0014ZÓ\x0018VkVYVYg,Fìî¢Nm\x001eî[[öª¥aÐÕ²Z\x001c\x0006Ý
à_?~¹ÿôðíO÷ÀZq3·ðbÀÚ×\x0006\x0019 ×W7ç\x0017ç×çË1V\x0008m¦Ö¬@Äñ\x0010Ü±\x0014J5 2*n«nÖ©@ú\x0006Ò¯Ìo~VhñÎR·¨Çö/\rï\x000c
dX\x0003\x0019bÕ3ÆÂg6z?Ô@N²&8Y¯ôCkÞC\x001dæV[f§¹I\x0018µm\x0018µ]\x0003	ÀÉ\x001d\ÉáLtË»q%u»zÕRfcNW;súÞ!²py\x001dá\x001eJUæº©r%Îuk-Ð\x000f\x000f\x001f?/óa\x000f
¼X)6ÑEm \x0014\x0019Q{ö\x0017¤Ý¸xóî(ÚaD´i±\x0007
\¹\
¯õO)ºêÄ/>èb³Í²Yá²\x0019à©\x001bàLÄW¬8oæ\x0015zzÙ&¢éÍÍ²{fZ¯Y\x0004×ø¹Z§n¶Ð¬[\x0010®\x001b©E [ðÍ\x0000?ÌâÒ8>¶Ø°E!ãa¥\x0015 T\x001bbbeÍuö²%?eK^Æß³0(\x0019B2¥¥¨hrOI³\x000fÚN6=!&D\x0019ñÂ
b=eØ"+ñ\x0019.X³jÉ\x0012wÁMë¶Ý\x000e~Ïi°ô\x000eL8\x00142È"Ô¡³1÷n6ß²	¿jp&H*s\x0004Èxµóå	Ýl©eKÂu\x000b¼ã\x000cæø¤ÒÅå¬üöÂµ7^
¨/oè£ê"E3ôñðÐI¿ïk¯\x0006-½\x001b¼§\x0017r2V\x0017ÅARWÎ.ÍëóÍÝÐÈ¤um9ö?qBÅ*ºS­Sk¶ÜO\x001aÊ°qt:ÆmptzF:{üÿÄ±é÷OO÷eNçr§E~kD\x001aîîQÁ^\x001a29ù\x00087\x0016ììêCþ\x0013¦_çÛwZ.*(LAá¿0¨ÿÂ v
jÿëæ¥ôÍ\x001eÅ¿À=úæéîsF¼^\x001e}<\x0004êu¥ÇØÈýÐ.¨©Áys}ú.S]/O<f\x0018Â@/Là\x0010±ðâ/Å\x0013ÐÐ¬A1S\x0014Ó\x0012UªJëB-)5 ì|£dÒÏb§,¶Ek¾\x0014ò²\x0012þ/ÉZ
æ·L?Â¸Þ	/T 1\x001c*wß}®\x001dþÙ\x000fã§0¾se@sA\x0007ÎL¥JR¼xeæ¦~0	0\x0018á¦Ýë\x0002®qÀ"®iWëgSØ»0ÃÄjZ\x0018*ÌÃhk]¸
&MaRïþ\x001d\x001e¹eaâ\x000c®.Ìª-3©±@§:ipd\x0014&Çº\x0019\x0018è¯K³ÎÌèÖüvÚ_ÜÁT8k¸f¢&»\x000e¦1¿ºÓþjk¹Ú\x0004}(K¹ûPb}SÌÕOÓX`Ýiq\x000fWôB×=<®
¬¢il°î5Â®äè@qÖ-²,k´ôÃ46Xw\x001aa
<¼µ,
õb\x0004¤.Í*»§\x001b#¬{­pF`Ãg=ur<F\x0011ïí°¦±Âº×\x000cçG]ðL<\x001aÝ¹É¶Yu[êÆ\x000eë^Cì\x0003á¨-J9¥*YX*¹ÖÀ4vX÷\x001ab\x0013^LVÊ¼
Û\x000e\x00144v\x0018zí0V2ÑÊ\x0018O\x0003J×Ü`éÜ:Æ\x000cC¯\x0019¶5£KÃ\x0015V¡*Ò®´ÃÐºÁ½v8;lùLÕTõÚ3]·k ±ÃÐk1`bê\x0015e\x0012'ñyi`ÕéÆ\x000cC¯\x00195@³ÿK\x0001à},kWù5Ðaè5ÃNqÁcÑåKaôaÝ®iÌ0ôáT3íeB&\x0017±°f%ÆîWÑ4f\x0018zÍ°³Õ5wÂymê
¥×-Mc¡Ó
2õ¾ÌÎh¢ò[}¾vèe?Mc¡×\x000cç½bô¸4t{WIÖvôQ7iÌ°é4Ã`\É(¥1\aì#O´tV-iì°éµÃ e[ãêJÖo{wÆ\x000eN;\x000c&Qëg^\x001bK=XÁ'ÅkcÖ\x0005GL\x001bèµÃ~b
kã¹çµ	«¼sÓ\x0018bÓiÁÖ\x0011\x000bF»ÚQª ¹Q«îoÓXbÓkq>ÜøÞõìLÔwT[}ÐOÓXbÓiÁúê\x0010ë*Ö·n57jÝj,±éµÄÑ°`0Ø\x0005\x0005¨Òñz7a\x001aSlzM1v\x0006¸º6Ô\x0017Tð\x001bÏTcM¯)NP
S§\x0015¨eÁº4\x000eV½£lcm¯)F\x001fÂVs£wT¨s­\x001dÄUØ6¦ØvbÐ2ÚÙp<£ÁsÇ³j\x001dLcm¯%öãwÒÀ± YÒ_å÷ÙÆ\x0012ÛNK\x000c¨ÔÉKã©¶$øÀs©òÚ¬£i£Ã½8@
¯©ú
uÌ\x0001¬;Þ¶1Ä¶Ó\x0010£X\x000eãÒ$î\x0008ö\x001b·Mcm¯!Æ!C\x000fuª±êüã=¬Ò:Æ\x000eÛN;\x000c®VÈ\x0019T#´Yª4ûç«n\x0005ÛØaÛkQ\x001ewæhu°ÕïÓëÂ ¶±Ã¶Ó\x000e·õÆÌo\x0017Ok\x00035òhÖ\x0005m\c]¯!FU
Mû&÷&ÒTEv·îD¹Æ\x000e»^;ìÓè Gn£\x0008cZÁ¬ò³\c]¯\x001dNU©
°ÛÏÑÊDö³ôº\x000bÓ5vØõÚá`j.*?ëè¾4<°*»\x0012ë`\x001a3ìzÍp¬¯\x000e©6éåG&\x001fo½Îò¹Æò¹NËgT(ñûB\x0003<+%)^\x001bµ.\x001bå\x001aÓçzM_\x000c5¼=·´kê}	ëlklëµ5ùëÐ\x001b£H\x0008?'\x001e[ÿßV\x001d(ßnßyºqüUâIX]|aòS\x0001Ö¹\x0012¾9P¾ó@å\x0003Ãæø@'*Ô¼^õúö+á;]	£\x0015Kµ\x001beê\x0010ªÏ§Ã*3ì-ì;·0î[~·(¨4ãh0í×Ñ4{Øwîa4w¶^ÞÔÃ\x001eXõ/Ã¬\x000bf\x000fÞ=\x000c\x000f\x0014^\x0014êËß÷°6«\x001cÐ\Q¡óÂbHR¤@Lï0\x0006&V^Q¡ÙÄ¡w\x0013SºÐø:³JÕµ>wÃ \x001d9®MFÉKsñÛïw_¾Üs\x0003Ñéç\x001fî?\ûãËýÓ_\x001f\x001f\x000e \x001a\x0016ñI¨4ä\x0008ÑQÙMöØaº³/Þ¾?½¹¡>¢Ówg\x0017çïN®ÏoÎ¯¸º¸>B­\x001bj½\x0011;ÔiÂÕ4¨Ì³4mêP¶POÒ&¸Öf\x0013µ\x0005Ú	/\x001f ÉoÙÓå\x0002ÏÆKØmÅ6Û\x0016ÛiÒÏIh\x0008y\x001b×µnËR·PO^3\x001a_3\x001b¨=åì\x0001Ë&;&Þ×¦\x0011ñÜ\x0002í\x001ah·\x0011:°8böd)$²á\dû/böÍ®öÛvµ3µ\x0016\x001dÕ¶\x0007¯´sÿ*êB¦F--+\x001d)E°n!\x001emUvÄ\x0017ù¿
[7ØzÛb³\x0010uÂÒDªÒAÍ\x0015ÆNÿªÃ\x0018\x001a\x0013\x0012¶P5ð±zÒÈ	\x0014[>Ûô¯ÂÖ&µ×\x000c\x000em®çW\x000f_NÞÜ==Ý=ô`ñ\x001c3OÚs\x001e*ðxw÷È¬í¸=yuuqsòæôúúüÃ1ÊØPÆ\x0015Ár	EBRSx\x0016ïÇa
[)Çà1RZ½ÒpÊ>crò\x0015EíÒÙZB9>\x0012\x001fÉbJ¬¾£\x0011GÁD[Y\x001e\x0006ÒÊ(¯£\x000c
eXAé\x001d÷+gË\x001fcMbeôìÙPSæ2ª5kéY;=:WÒe-UÕYkÊr^ýØÔù \x0004=4\x0016õËÉÙÝÓ/ºWS6Ftr5\x001cý4Ñ³v!Ì\x0002beþéõëåV\x0016\x001b\x0013¼\x0008g\x0014\x000eê 0§X2ÁÀz\x0006æ-åQº Ú¤fþÔ|à³oÿüå ªO¡çù­CÐ­\x000eá5\x000bßöìüõ²èN;\x001dý:
\x001dýS´_ï;æÑ\x001c\x000e:>É5\x0010-wüªy¯¨âÜ¾=6öL#ZÒ2´ì\x000e¢s	\x000cð\x00005\x0016\x0014vù-3ë õ¡é±«\x0000Ñð§Í\x0015Ukd³¡¼N
\x001bÏ2nÁðu±Å
Í¦q¼\x0001\x000fÇ©ç¼pÎÏºh½p¡\x000bB8EIaáè£Z[×má^ëbs®aC)a3æ\x0005¡@£\x0016":\x0016".\\x0013}h±EB´H\x001aåV\x0016BØ(½,µ\x001f4	?¨áwÂT\x000béÒuì¢êy\x0017µ\x000fn¢bpå¡/Úm¿0³\x001aèZ\x0016«³­\x001eh7\þ¯û±)ýÆÿ~Ý^
¯¿ýñ×û,_ù.zìó\x001d6\¶âTòâ<k8XòK^ÿpþßo{¢K
]Ò^é!Ä¥\x000c·Ã8)':»dãºðôf,çÏ&ê\x000fÄÙVÔÕü,í×Vvñb\x0017Åx(ô<\x0004Rò;ò¡Å#¾°ô\x001aêâ1À\x0000\x0000FÊ\x0007<õ(©ÄíùûPoþ-ëgÆ÷$\x0002\x0007e\x0007_\x000cÉHÙã¢[,cUÕ>¿ttûø|ó}ñ§ðx!ù»¤c$\x0015$çB`\x001cÜc|6þØ´Óå¿x\x0019Zoøüç§Ï¼áX#èQó¬üà"\x0014çÏnöÏÏ®/Þ-zÃ\x00047V\x0014#\x001cD!]þ¬­<éW\x0004C³w2\x001cÌÇbzáR\x0003p8Lô®¢+#Ãùª½\x0016\x001e\x0012]tcå(Ò\x0019+¥³4®±(Ã¥Dtu\x0006­Þ\x0006ç\x001a8'ã9Ñ÷\x0006ã\x0013Ø`çãôtcô\x0015J^Hgé¾!jÖÿ3ÖóÒy5\x001fÙî\x001b¬å¼*!\x001cvóX¢ÒÈtu¼Kòz>¬ÚI7ÎFº\x0008B:<ô5ä»\x0004ë
pÑHrà&Jk\x001c\x001e8­Y1/xÃÕ\x0000f´uv>pÒM×\x0018â$µÄÚ±JjpPÔ¿
«cÝ\x0017ÂüGé<´\x0001Ñü\x0017m@t6yøôéñàðhn`MVs<*Ð\x000c\x0011bÌç7\x0017W"\x000bÌ\x001aÆ´1¼\x0018|\x0015h*ÆÂã8Ez\x001bâØËàÖ \x0002E¿3£! /#¿ló\x0011^Ìu26Ë\x0008kÑ%
öà!\x001aûî\x0014gÉÝH8¹Û2a{·õ\x0012fÓ\x0008\x0011\x0018ÑÖ|\x0007;Û8V\x001c!¢ßO*\x001dG@ÕºÉd\x001fuWìÍF;onº\x0011Ç\x0004\x0012"Î$:\x0010\x001dÕøåUä^¨©©
uY\x0017st¦AÜÏ\x001eGD»8,bv\x0015\x0012O
µã^\K\x0018wê\x000fò_¼Üy\x001d½¹ûýáîôLÔ,Ç\x000c{Ï,g³ÿºðð}súþâô(mÈ¬Ì°\x0018gÔeMtíL)-¼±
\x0003®&láåÎù½Ã\x001cÆýçÏ\x0007[CbU]MµRÃ;îÒ+Ò¦óßõ\x0014S\x0018çïÞ-Ç\\x00081L\x0011Ã
Ä1ï\x0012ÊYy¯Y¶<.æÝ{\x0011'a¡Øú\x0018qDã¹[zl\x0008`7?¶Ã~W16Ë¨åë\x0008yñh\x0019µ-.NAäÒ>Ê¬FLÅÈº)ù/^¦ö`\x0019YQ^&´z\x0010ÀÈV:\x0001K\x0000È\x0001,«ç\x001frù¨`A\x0019ê>\x001f\x0001\x001cÓi\x0008\x0008ZNjÌ@ht-l\\x0004¨C\\x0011u#ú\x0006Ñ¯@då¿\x0018¸-/²$¬ÕÑ.z\x0011'oÎh\x0018\x0011/!¿\x0011#ËNe\x0003Ä«\x0018Ýì³S\x0018\x001bÄ¸
\x0011èCÛq+Ö±NóO\x0001bsXü´\x0018T\x0012u¨xì@ôÜ¤cØ¸®ùÐnÅF\x0007Ú¨\E5tò\x000b\x0001ó^Dß|h¿âCA«	\x0011}íÔÓÐ çÍ¢\x0000±ùÐ~Åö<Ë+#ªrÏ ¢¡jJ\x000bXì½\x00161ìx8ù\x000cîx8ßûãéñóÉÙýç_\x000e`fO'oB?\x000eJ¤­|3r0i)ûðýùõÕ»³ów\x00072çF\x000c\x001fg^+õÒï¿W.>-O\x00148í~Ð\x001cO\x001a\x000bÿ\x00085öUs\x0004Ý.Ö]\.³jó_¼Ü	Ø\>||> 4\x000c©Öº»¢pQZ»«j
Ì§YÏoN./ÞÜ\x001e\x00197°##ÿ¢ÈµîÃåãóO\x0007\x0007
ÉµÛ|é±©éãz«çãÓè=\^Ý¾:°z¾µ5ÈçÏ)\x0016®Ê\x000f\x0011wEì\x000f"¼¨^Ê}xc;\x0005âù=ïë(g
\x0015\x0013á\x001dñqÚÏ?\x0002ºñBóuw\x000bFã¡\\x0008Ñe[3¼>UÕÑói¡\x0014ç8)\x0011¹Qÿ\x000b«õNúíÝ·ÿ÷ëA¹`j\x0003I8§ÚÐû=:Ê\x001bîtEOÆÛÓ\x000fË\x0007ÃìdFm73r-?N¨LÕZK½D\x0011\x0014ª9³XcÕ\x00037j! 	r¸A\x0004\x0010Cª/x¦»á8¡¥(p\x000fÛØãl\x0016dl\x001e_ì\x0014ñpÊÖ³\x001a\x0013Ã-ØâN8ÓÀ\x0019!\>£\x000cçU-\x0016Ò
F²
Î¦ö)ÿbç)á¾ýñåîóÇCñU²\x0005JÜÌ	LJ>Ì;ÐÈw~súîÍëb@\x001c½SD4I\x0018TE\x0004_]?®->ÐìD\x001cu\x0004L\x0011\x000e_h¹{4Bd9\x0015¬dÄÅÄa'âÿ2e¨¡\x001c1êºËaðEL\x001eKéÙ8Öì#bÐ+\x0010\x0003KäDTÃ2Ô_ÀuJ¥%Ï¥\x001315IiJ8a=1I$¨\x000bEE\x0002Dh\x0010wma\x000f"O¯À\x0008\x0012';\x0013ð´\x0014\x0005fíÎÿÅ=Lå;)»«çï\x000e\x0008Ï»\x0014a\x000f!¿\x0005T\x0005\x001eCX´7W·g§TñÝNÔ\x0003á@JÊãjØ.xªQ\x000cJ±z@K\x0017]\x001fÞ¤É,ã\x0019\x0010ã)VüÆ\x0011è´gºÅíw\x0004/ÿ\x000bl´ëò_¼Ü©ï|ÿõáëÉ«Çç§\x0007\x000e±
/\x0002[4®*\x001e$ÃÁÁùdöíÉûó\x000f\x0017\x001fN^]Ý^¿9\x0002iÔ\x0014Ò(9$j1Ð\x0019ñFÕæÈ\x0003\x0001£ÞN9
F ¥\x0015ÙdSÁW\x000b\x0003£Æ%ÃÍ¦¡4ë>¸§\x0019aÙô\x0018îff]ÒÒÖ¶26qÍZÖäIþÁÂÀ\x0015 aá@z?ô~
¤cU\x0017ß¥\x0016\x000c\x001b\x0016z\x0005\x0004Í	÷«N¸gí8oyêVI|xÂ\x0014Q¦2­¡¬S.û\x0015¬e\x0014]¥4\x000bA¤~ÊÐ\x0018¢°Ê\x0010ézÝD~/ç/ÎÁá\x0010æ\x001fV"ÊÆ\x00105(
C
¥á¡\x0017¨B>-
;(-\x000c"ã="\x0007?¥ÄQ?Ü?-×d¦ \x0015e|òQVE_\x0001¯Æ±ÆKÏw\x0002\x000fC>8¿^,Êd@×\x0000:9 yA3h5½2\x001f\x000f\x000eIzq?öñAÃ\x0007r>Ð4Û½dõ¨/?`¹JÍ·Éö\x0003¦\x00060É\x0001]Í:Ö\x00164å-?\x0003±åv\x000bßdkæ3AÌgtÑò ì2ÙÅ|üø\x000b«¥N¯N@Û\x001c\x0011+?"Æó\x0002bl.\x0012_¬\x001fx>ðÚÁ·;PÇ\x000e\x0003u¦®íõ}þñt(T\x0002(.4\x0010P³ó5ÅcÝ®ÆÍÉõyþq½\x001c-a@3\x00054b@41¤¢cÍ{[·ÿÙ\x0008è¦N¾®§ä#\x0018ý\x0007k\x0017\x0012ó\x001d4é~<ÃeÈu³\x0005oî>~¾;T\x000fé8Í\x0018cvohîáqhª\x001dG9Ù7§oÞ\x001eC\x001b{J\x0010m§¥ä(Z¨\x0019§¿2½ëM4\x001c\x001d	K\x001d¸}l®as26\x001fX(-åmG²\x000b&*îZKÝ\x001a]lyËn'²Ô³n,°á°V\x0007GWÙÒo:º.È¶ãº\x001ce<b\x0014zXôÉ$n"UI/x-]lÀ.íö·\x001eg³u¿9Å¥Á¶\x0006ÔµWãécÓºù¦øS\x0004¢T\x0003[pµ\x0004Ó\x0003YòTºØÚ³°Û§yÍc¨õ\x0014öÐÌ3Ëi\x001aý
p¾ó28S½y\CX²+\x001bµ3\x000b>h\x001f\já$Ö\x0017WE:óÊQ\x001fi°^myá6}ÕÐ\x0006\x001d$ÇÁcÜ^ç	?0ø­Wá¶Öh\x0019ÁÊê\x0002Í±Ûd½¯lKM®GàrÚQ<3ÿE\x0011ÏÞù\x0008w \x001eX<á¨Ïr'dÔ<F\x0019â|{p¾ñn9\x001eHt1Néb\x0014ÒYM¹ê¤Qçxèì09£\x0017GzèôäÍÍ\x0005Z\x000bñã6H\x001c1á\x0008ÏGnã³óG¢\x0017\x000fZ¼]Í£xÞbÆå| \x001e×û"ÞR¨¼\x000bÏ¶xV\x0017\x001d\x0005zÆÞr½º¤¸wÄØÅW\x000f\x001e¨\x0006\x000fð¢1lît
%yxµ¡?ø¥lz\x0017]»õ@ºõ¢\x0005DA'îpMvuÙ»[J\x000bwáµß\x0016¤ß6úµ\x0006Ðä\x0002àÄFêÅ0K
-Gñ\x0006E1Íÿ¢I3Ü|=ùÓó§O\x000f÷\x0007ú\x0007$®¡\x0014æ*¶Èé´eìè>ÝÍ?Ý^^^/VÂ\x0013ÝÄ	ÈtS\x001f \x000eï@Á2Ë\x0005Ü\x0011Uå)X6\x001b\x000fï¦\x001b\x000b×nZ¸ÖGg¹ÙÐ%à¹È	LÌ¿Í]µ=t;ò%6ìÈd¼Ë»Ü\x001d\x0012Ë	Ø×0¬öÀ\x0003ä!æÎ \x001eó,Ýåé?]®ù³q'7Úi°ëÜ}zþù×
VQßÆæÁà\x0005°\ó·\x0014º9½¼=û~¹ëè¬ÒÙÝ\x0007ìQ:\x0008¬w¡³+ ¦þ \x0012Ù%	N¼1xn×:}§Èö8Q^Ðùd\x001dãùEÿ³oìîB>¿ë\x001eåÃ|\x0001õô'OÉ6çC¬\x0016yùÝÅ7êá"_Ø}ö\x001cãË7+\x001dÜí\x0017ÖÏj*Ý;ùRò¥ÝÇÅq> (E\x0002´1\x0017F)MË§¡Ù~øSú}#·\x00138Gõ/Î¬&l:\x001fº=¾Z~~uÕ«A\x0005ÀÀ\x0007?ðÎà\x0015®\x0005ïÀT\x0012TE÷X±ñ\x001c?F\x001dÍÅ×í\x0011À´£ÑlÛ-{þpÿÛïùj{:Tø\x001caÔð§\x001e×àka±ÓjÉåûpþö}¾Ü®ý\x0016"´SB»Ð³(:$[Çn©ZÛµÙÝ~èW ¦rµÑÄ
ËuÞ·Ó\x0012Ä8ErÄ¤ëp#§D\x0001pÍ¢\x0005)ë.ÄØÖUæ¿hë*O>|ûãëÓ¡\x0000Z¨âNÑçHò¾Êñgq©ôÃùë\x0003!\x0003
\ÂÕD©Ï\x000bi8\x0011ÉÍ>X|·\x0001nÌp;iÈ\x000e8 \x001eèCâÙLù\x0011j\x0013éB1I\x001foà¼\x0010N
c½\x0010.\x001anÙÃ²E^9½`\x0000\x000fÃ9åÚÜJþ=í\x000fOßþøíñùáÓ§Å:Q	e	RKb1l½¬ñáúüíÕíÅååòã8ÇD\x000br:µÓD½RÂ\x000cü:×fAÛ¸3S¼ï&Íù\x001fÌæÛÇÏ_¿ýÁ­\x000c¯\x001f>>ß¼½ûåî\°¶:6ù\x001fIµÐr¶9Ìo¯Þ}8ç×\x0017onÏOÞ¾>=¤'7h\x0004\x0016+±VÑº*M3à²k~¤øÆ]I_ÛSZü¹ÖG:Q	ÅÅÕÐlcµf>\x0017¶ÑjÓ¦Uó_`Zõ}Þ®w\x001f\x000bëÙão?Ý¼ºÿt Ý+e/±Jô ¬àpã¯ÂPÐì\x0001Ü­§o
èÙÕÛWç'¯Î/¾\x0008rl«BHl«\x0012SfsN`\x0012'Ð«0©-eÊ«)]l}´ü\x0017è£M \x0007ñïòùÏ®äòg\x0007]Gtiêz\x0019¤\x0002¨\x0008Ø6\x0013²'¨\x0000qvz
@v'ËÒN§PL¥^§¢ö=a#©\x001c\x001aõ\x001bÜXBÖØûÊÙWöäÃNÍD>¢zÄ`Îý²\x001cÄ0ôGaËZ\x0007OkØ*[3\x001c\x0006rÎµ Ô S¡Ç^Ù\x0019Àÿï?Ýý\?òé|Q~¼;´\x0017Q
åÑ\x0005¢<J<¼/6ÏÁ÷§gôOoòUùæty#\x0012âdjFÄ¾l1bà\x0008q\x0011¬\x0008Ã\x0002j°ì¥¥&¾¾q|\x0012"#¾\x0008å~¬)2<YO\x00030ö
ÆÉ\»Ìa\x001d1£w<Î¨ÈA.IÕàRÍÃZ¨Bû^@\x0005é>ûõî§§oÿ<Ð\x000f;\x0014¶Q¹*XÉ®ây\x0013í\x001cßÙ÷§¯®óSá@Iÿ7\x001anÄÓJÎ\x0007¬JúBìó:S\x001dÚ\x0011 r@h\x0000a\x0005 ã
ã89«\x001cki\x0004\x001bfÏr?oø¼/Rh1º|;§ÝÊÅÐ¦Ýå¦Y@#_@£¸´\x0012\x001bÇ¹òÎs?{p~Û\x0017¶
 ]\x0001hØÌd\x0017B;\x0019¥\x000bB[\x001c°\x0002°9ÂV~
;Ña\x001b%íÁÀ£w*å\x0019\x0019ÐY1 Zºúðµ¸²æUæ/nÀÐ\x001c ?$ºöå \\x001d\x001f\x0012[k¸\x0003l\x0002ÔjÇ\x000c7¡O$>ð\x000cx ë\x0011	kw ÖqÅìãxÍ=|÷¸\4Ý,
Ü\x0003Áñ$m\x0007ÜcS¹ÞnO¾»Z®e$;E²\x0002$\x000eeG.\x0001ÃvÌAîCòS$ßï0ê.Í¯"®|r/Yô\x0002Ö"Å)R\x0014 ¹RWW\x000cwòfð\x0001)Æµ\x001fnrãCsã\x001feÊ\x0017\x0001Ç½"ám|Ppn+@&bjö·\x0016lpSgÍâ\x001c\x001a`¦ú\x0018kuELÍ\x0006×\x001dî, Ó<NÊE\x0016á°Á¯ÝáºÙáZ°Å=çg2}ÁHÜ©c[½.\x0011R³Ãµ`\x0007Å¢pÐ\x0011õxÅsml&EI Ùâ ØâÁòÔöl¿y;yÅ£V1
±©5á->Î½Æé\x001eô\x0004ð<#\x0010møj¦f`gÄÛ)j~Ù¹dX¦GÁÌË®©Ùâ Øâùüs\x0002-zî\x001fÀq\x000bÌ´ÚdB³ÇA°Ç* %\x001f5\x0013"Suªñêýd=n\x0004{Ü)ï0\x000cðµÌÄÃÂ×\x001aLÓìp#ØáÖ±J76>\x001aº®)±9\x0007¾©ÙáF°ÃM\x001açk\x001es¼\x0000V¯S³Ã`çuuHéÎ¹:\x0008º\x0015Ç\x001215;ÜH\x001c\x0015ÏÒù\x001ax£\x0012ê:ùµßÎ6;Ü
v8Î¤a&ÏSËJbVß,¶Ùã¶+Ôz0£ÂÉÌ\x0014×î'Ûzâý{\ÅªÆÃ³©\x001b!ñ£jg\x0008©Ùâ¶+\x000c·\x0012)\x001f\x0011WIq4Éé¹XC\x001fR³Ãmÿ\x000eÇÒôÈ÷J|A\x001b\ÕUÒz-k6¸lpóÂ§zýmÒõVQVîÍ\x0019Û¦qÑtb\x001a·"
\x0012\x001f\x001f\x000e5ñ±º5»æ\x0014ñ\x0007Q³æ`Ph¼¼zs±ü\x0014\x001e\x0008­\x0012b\x001dÐ²;åòc¨çÆªpÐé)!Ö|
	óuHÙ\x0007i\x0012j«×¬\\x001bü¬õê\x00004j'
ÿb&üé§ëÇç¿Ý:ß3|\x0003aO\x0004õÒsÙ¼u&íï¼?½:¹¾ºý·óËcXveXtWcý²c*¶\x001as>M7Ry	UÞi¤Ób¬¡2ùà#OÐpnæj<e\x0007\x0005ÐI\x0019Rí³ëýÃÏ\x0018¶zõ¼\¬ì\x0012¡û(ÀcGu-\x0007I~>\x000cóþâ\x000c#W¯n\x000fÔ+\x000fãã\x0002	ÇE\x001fa~÷PG¨5+AY,:Ü\x00068úa\x0008Øøa}:\x001a\x0000\x001dS\x0008ZSÍ¨MvÞñéçsÍ\x0002º\x0015\x000bX«4dB\x0015?Úp\x00163\x0019;ûø\x0010\x00106+èä+\x0018\x001db[K´eCÌüë¨\x001f04K\x0018ÄK´êpÞÄijíùe²å#\x000fÁæI9aþ/o\x0012ÁwÙÂ`Që×Cv¸ JÉaÕ9Pì~ç¿O±f3U­\x001f\x0001ïL\x0004lÒG}^Î>$ÄHæ\x0000h8R\x0010]ÏS\x001f\x0007Ôi°AªT;fÃüõ~²ùí½¿{^¶Ñx_\x000cÃ«KÅÑP·\x001c
\x0014µE4´Ù48§)\x001fÎOo éiDÃKH\x0006Éó\x0018Ë¼`/\x000c¡ÕîHüûÕh(¨<]5+[6PÛç0¯`ÉâÖÃÔ\x0004d!µß3È0ª\x0008\ç­Ë\x0002ê\x001c\x000b\x0013yV£M¥'\x001a­)Aó\x0007k¢VV-\x001c\x0002®WM\x0013
 aÃ"6\x000c-Ð\x0007M\x0005¼bÝE«×Q\x0000hÑdç\x0000Ó\x000e¾hm
ÊhÜ¹dµÛf[4+C\x0003SÛ2°í&Q\x0018ûù­ÞðA'cå\x0011
C`\x00124íkfR\¬}&.Nl#B¶Ðn¶ Ûl*\x001a\x001a¶Ö<FÓq´³¦£)c3ªÙmøSÄæL	\x0018ÁË<\x001f=¿­Yi\x0000S%+Ø²7ücS0î±}wÿp \\x000eòF£\x0012*\x0016F\x001eZ£jÔÎ~ÍïÎ/«å\x0008	¦HÐd\x001c»F7\x000câ#\x0007´¬w³\x000bÕd¦HF°JÜøWIÑàg\x001cíS£G«ìÈ
xÆxD(¾\x0002YÓh\x0008Ü\x0014É	ü\x0008,zã\x0003g¶i-"ùn$MYeåß´4\x0017ÇèWó)O\x0010}5ÅQHËOÏìIµYýÕâ\x0014)ö/Q¨\x0011?]VÏ7
¿³WM\x000fR"%Á*%\x001e¹-n\x0007\x000b\våp<ê:¤i-%
½Ëä\x0006-Ì]\x000c¬îiÀ¯fjM·Àv\x001bàÊ @p²¼HnÖ{é\x0001j¬¤\x0016ISg@\x001c?ÝeÔûJ¦Æ(iUÊ·	IJa\x001b÷b-
ZÿÝ\x001a# \x0005VÀDnH:Ç=#µ\x0000jõ25GN\x000bÎ\¾i£­å.×Ë]BX»NÐìo\x0010ìoç<Yq\x0004¸
&\x0004Åã\x0003²[·Ö7fCÿ\x0016×\x0015J¢\x001ekV=ð¿ü¬_k.¡ÙâÐ¿Åq²\x00118kÔ°\x0005ok\x0004EHÍ\x0016þ-/ÒD\x0015
8\x0008ì\x0012[K;ûVî!j68ôop\x001fTÏZZ ¹
ÀµL¦Ùà¦ëäx\x0012v¾ª0¥æ]\x00142\x0019\x0012Ô\x001f\x000b(¨?ºL%¸Mi¨usèìEz­Dïj\x0017H0<ß<¹;¸D×°\x001d
Õn\x0010\x0003s0\x00189¡âOô6\x0012}*­õ
ÂÉÌL@Lè\x0015uX\x0004TH£äµÝ9Í¼\x001a\x0004z " þ\x0012\x0006àñCÇÈÂ:nzFÉm±YCü)E«z1f\x001eXdÛr®ÁÏ\x0004\x0005\x0000ÍF\x0004ïÄHÃOì¨¡\x0013;ÊÃ^©mû\x0010Ú³\x000c+\x000es>\x001fæð Ø,KÓk\x000f\x0016\x0019-fô;¹8\x001e¨X@µ2TbÒ<]ÅmGÅ6ºd©&Fº\x001b0r¿³²\x000bî8(át{oK\x0008}sñ§\x0010õÝI4Tß%J3]\x0011_jùäXë\x00174J£áP\x0013J2\x0013¢N3Á9\x0001¢3±)Â0BDãù#ëì\x0010{UÊ=]\x000eÞ¶nÌ\x001b\x0016Ä`ÅV×\x0011Ñqý~¾¤YþP¥mæ&ª\x0006\x0011
\x0011­ä·ç£h\x0015³ñN\x001c¼Þv£k\x0001Ý*À¡+)Ùüdu4,Rs¾ÄAyI\x0010ÛÃ\x001cå\x0019g\x001dòHÆD±8M\x0003¡±\x001b¿r\x000c
a\x000cbBÔzçùÃ´)ðFÄ÷Ù&Ä\x0004Í"&[ÄTs°6\x000cC\x0010{]ónÅÁ(Ù\x00141:¹ÅÑu+æ[ZóiVr³¹Ø~D­¡ñ\x001eÊo©ûå·ÃyÆ\x001e9]ÅÔ¼fÓÖÚ»Ñ×Q\x0007n4L+sk\x001e#[ð¹1í0/Àü?u±c \x001e\x0018q.ì#@öÀh\x0018­-'©òÖ«É½ÄCC½3[\x0019ý\x000e£x;j¬U\x0011ÍNÇÑ¿\x0000Ñ´_ºÔ¾Ë\x0010KMö`¾ómÇq~\x0017X\x0004ØÛm\x0016
­\x001fQ~K\x0019½&5®¼Pó\x001f\x0005Þnó\x0018µÙÙF¾\x001d®"CØ!N¿lÊ¸íS\x001bÓ.#þ"*ÍÒRÎÖ·u®"nÜÆÑ
¯j\x001c«P¯jGÉUd4¬èí[Ç\x0015©=2ø[Êh8{×Ñs	,êmÜ¶\x001d­j·#þ\x00163Fjz\x001e\x000cCáÄT6=\x001b÷£UnQx\x0011"£*©W2=z¸d¯¦Ç©ë¨Û\x000eþ2B¢Xl^ÇÀ-+Æ;þÖn..aö\[\x0010ëÌbL´ÞðMhX2Î{·É\x0001×6¶\x0017!þ\x0016"¢\x001c9½³\x001c\x0016	
\x001a"Ëúä·Ý2;\x000fj-~QgF\x001cÍ3ÔXá°N;øe\x0000ü\x0016\x000cz®lNÄèw\x0018åëò<¡2Rî\x000b0ÐÆÛü[\x0017bË\x0018¢1DEÅ®ÉCLèÈñ0[§#`L®5ø[Èè\x0003P)Á°5I\x0010
ÿ]²nåI\x000ev\x0010ÅÛÑ\x0007Ç\x0005bÑ{Êª<xfK\x0007K\x0018}kyÊ\x0011\x00142bñð©qRu`Q\x0017.bË_fÛI©=2ø[º\x001d5Cdß"àréQ \x0016ûü?Âoº	a"PÞø[ÊªQ´)½¬\x0011FL
ÛâP0i¼\x001f\x0010A¼\x001d\x0003J\x000f\x0001*ª{ex;m>8ì¼\x0013@üNÀYfõep&\x0007Í½2·£nB@¡±&¿\x0011åNx\x0008l\x001d\x0013¾¬ù½¥y;¦m\x0011
°;ÛÑJ·#>[}yÀ #9¡r4U×1mËqµªe´òç¿ÑünÍÖº¶0\x001aÆêKM×\x0016FÔL2âoiÜQÑô¤-Y,-â\x0018Ô#ÂÞ2\x0010]\x000fÄßbDWº*
b`\x000bORdÆ°Í:Æ¤[Æ$ÎgayXEÉ\x001c¦\x0000Fe=#Â¶¬eF
;ò\x0008³S²þÀè)LO¯\x0004DÜt\x000fBv\x0015\x0013ÈW1!4:lFNuDÊNç/=×yÑÏhtËX~\x000b\x0019\x001dN¤\x001a\x0010#kÄÅìÝÒ\x001eÜ¨-í)¿¥aò¥#e#(Ï\x001aôVF·Ã(0ççÔàò¤2ñvÐíÈ¶nÇ¹\x0002"\x0001#ØÆ(¿¥0¤\x00101Aw!jgy\x0019q\x0018ý&Ä ZÄ ¾b\x001c\x000e\x0001\x0018>µÉ­!'_`vOx£çjÃDfQ¾\x001dó÷Ä¨Ù\x0003ä2ãÆ#\x0003mö­ü2*\x0012ÈùAhi\x001dZå¼\x0001¿É0F·Çh¹uLz(êÈ$\x0004­£±Ûâe¥rÊ\x0018äEZ:oB5¬£ÇQï±\x0014Dñ^m«Ò
ª;ßÒ\x00003CÜ1éÒ6\x0010)^F\x0013\x0001`í2æOôc+=iJæKÆ{þ¸\x0007t%\x000c\x0000O°Æ^WIH\÷mÃl±àMÆ»½ÄFÜeáo"¢[ æS\Ì\x0008ÖÓ8Ð\x0010b\x0015«ô³·t7ßdf$ò2@Ë\x001d¹±\x0008{E..ª\x0003Þæ0ú\x0001'Ýå\x0003OÃ¡}Þ\x0006\x001a¬TÅá\x00044½ÅW²s\x0017K?_r
_rB¾ü\x001e£~,î¥C\x001cyÀ\x00057\x001b­íæ´þ!ß´õ¯/[\x0019FËÿ\x0006ÎÀD\x001e³eócm\x001bàè\x0015À©\x000bÖ\x0007{Ri>«\x0007%Î\x0006ZP³u\x0008ý>6>\x0001déC²ùÙ7¬`\x0002àau9;Ý\x000fÚ\x0015Lâ\x0015ÌG$ú\x00010?£©Ü\x0017\x0004\x00186\x001da;¦\x0001
f\x0001ûø¢§lAÞwÕ\x001eSbÎoÿ¹[¤\x0007P\x0016ÔüvD\x0013ø<À~þåéñÀ`Õ¡§&Ce¯·-\47øöþ¸\x001dÀNß½¾¾:0U¹`Ê\x0005".Ô{#\x001d3\x0007Üíát\x00157m\x000fËL¹+_hÔ\x0018½DÔælÂØ!ë6pÙ)\x0015q\x0019U\x0005jµ&Ý7gk³Õ[ÖËM¹l½\x0012×¹c¦ø å\x0019xÖ7:ÌR0?\x0005ó²\x0005óue'*VáEVôuV,LÁ\x0008ÌÌ\x0010ê\x0005[Áìº-¶Û­®ìÔT¼ºûôóãçÂvQär|OeKQ¥¯Ì\x001c×«ÓË³«wG±`\x0005",OµÍ1£T½\x0006Ã\x000e\x001cª¿­Ç2S,#ÁÂ^\x0012
3fóæíÅ\x001dtÎÁÜöêÄ²S,+Áº¹pµ¨è1ß¦®]å¦XNe\x0015{ÀÕ"±}\x001cåÉ«¥7`ù)\x0017­Ö\x0010¿\x001b\x0016Ë\x001d£ºm±Â*\x0016+° 5J\x001d\x0005à\x00127îõµ³wv'VbE	\x000b¬¯>G76;98¯x=UR%\x0011+b$e±T\x0015Iwþ_ð	§sv¨¥½\x001b+»¬ä
ñö¡ÅJ¬4çl\x001b/qµ6^dä½æm\x0003\x001c\x000eF\x0011ðº^³þM'WcäµÈÊ\x0007]n\x001cÚ\$'ákÞ]aý××"3ï\x001d¿ÎQZF\x0001WíÖïhâz®ÆÌkG,:¤èéu»óÞA5F^¬¼O¬0_F9\x000f;n.Hë¹\x001a+¯Ef>\x00065?;XÑÅ¢É\x001bîjÝØy-2ôÁ²\x001c\x0001Ë5¸^¥jèÕÍÕ\x0018z-±ô TIôÚ<+\x0016ÔÙ*N
ß±1õZdë1ÉÆëÅyÜ÷¼\«¡ ±¨ ²¨1°D\x0000Z.jôõàxs\x0019?÷\x0000êäj,\x0017,WÒ¬\x0019dtàjUox\£3fýGÆHÈH¤\x001aÈfªÈ:\x0017®QXoàj\x000e#\x000ecJ\x001c(ÆvJº\x0019½UuÄB\s\x0018=ì¼Êò£¶×Çç/'î3ÚÓÓßÁ0*Ì
Y¦FJp\x0016h}iìZû«ÛËó\x000cw}ýïÇÐ`\x00062´üUãp\x0003Ã\x0015úz\x001c$°»f"43E3ÂU\x001b2Nåsr_°uÀÛ\x000fÐì\x0014ÍÊÐ°¤\x0002\x00006pÓ¦Î\x001ar»¾\x0008ÍMÑ\x0010-#¬\x001cûø6ò\x0000Zô¦\x000fê§h^?'ÀjçØè9Ó
i\x001bÐÂ\x0014-\x0008ÑM\x00078V²IÕ¹_v××\x0017Å)Y\x0014Õ)-\x0018ã
ÃÄá\x0000ë÷<2\x0011Z¢%\x0019\x001aN Ì¡	,üg©\x001e.ù-sòtC««jR3ûeC\x0005\x0017\x000eÙà¦³ØÚË@x\x001b$[24eÙ4);eÆpë\x000fªË@\x000bo\x0003lÍ£\x0008u\x001d^íT
¸î;h"´ÆâjÉÕZ\x0008Ö,³\x00051{¯q\x0011ZcqµÌäâUú ÚÔF\x001dê²ÙÝ¸­1¹Zfsµ6´h¾Ô{EcÇÖBÜô=\x001b«e\x0016\x0017Ã6Ô\x000fZcÕU¢s\x000bXcoµÌà¢º0	ÐélEx,%tçEÛ\x000btØ\x001a«e\x0016·ÌäE3ç¤jÀn¹Ü¡1k 3k\x0018g!ùNM\x0013ÈÖc^7µç}w±i]ØÆ:øü\x0017/#GZO^}ûãîÀ8\x0010Ka\x000cÌì¢<\x001dåî\x0015o4=\x0013Ñ¸=yu~º8
$ÿ\x000fm½nìÈ';{v÷åîóã_ï\x000e}Â£Ñ^±Ü\x0010Ne§j´û\x00148;½9}wõÃé1\x001e;å±Ý<P\x001fMÚ&\x0016hBiSâ{áÄ^ ?\x0005ò\x0012 æ	áj½´òQPx&¢ãùi\x0008ã\x000e:ûõî·ß±Þì»Çå±\x0014XÏ\x000cU \x0016§\x0016\x000c;<EUý×ý´_¨~û\x001e+Î¾»ºXKA¶a´+\x0018ã8T7p_OJã\x0000Û½í%FL
b#ú\x00111\x0001·%c°'ºq"\x0019Zñ©#3\x001aÍ£¾RâY²ùnß$È\x0010õø2FDü)ftö\x0005Ï\x00004ûQ\x001aØÞ»D¥¶´k ]M\x001bæ­Iº×¥\x0003n°z%AÇöÝ¿É\x000b9{üò5_Y÷>-Æ\x0000$pb¢\x001a´\x0017à¢\x0006êÒ°·\x0013Ï®n>ä\x000bëüòò\x0018Ö8\x000c±\x0016pù¨ót8¿tà
ôËV{An.­\x001b.­E`Æð9,»\x001dtÞOÜÅªÂÞ³ª\x001fl<´\x0005Om\x0017\x000bCXd\x0006ìté%"0¿\x0017Âí\x0006q¬"áO\x0001rTøÚØ\x0014Ç:\x000cjlËÏ¾Õ\x0012Æ-\x0005,$\x0001ÅÌÅ\x0000oT6Çù^,{\x0008{!¬n0ãOiäSZ5\x000c0Ä\x0015\x0003*\x001aæf\x000c\{OÐ~¬ØbE	É7\x0002ËDb\x001cfX/\x0013(c;l÷\x0001Ú\x0003\x0006®
bµzÍ\x0011`\x0001üÙãóïÞ\x0012N¢r<t5&ËÈüo\x0015k?1ÅïgW·ï\x0017=&Â\x001a=&Äª\x001eS\x0017W¾(Ñ\x0013ç\x001dÊe÷\x001dn®±\x0013¹¬pyV×Ù±ReþÌefª
z¹&&?s9-áïÉìps\x001a|ªÇ1í×fôrf{\x0005ÑþÂéI´¿²A
ñàXÚ3ûjû9n®ØpEÑþ
¤6¹\x0002ÇÀÐ8mW|µ\©Ù_I´¿pÌ7[¯:\x0015%ëÔ¾ý\x0012p¹ËìDââÓü<ç®[\x0000®ÁKi?ÅÙ¥Ç0b\x0015Í\x0012\x0001"(ÇWÐçü%»Hì¥fÓk\x0010íz\x001c¢K»^éz\x001ay\x001cM\x0011VEÝZ/-3_C(#_Ù\(¥#GgS0ë¿áøª\x001b \x0004
\x0014G\x0008;Ù2Xä½µ\x0008è\x0007síær¢Í¥\x0015þààU2^ù)ÃûË¯2^Crz²ëó/ÔÑë§×w}øåä»»O\x000fÿ±ü2*µÖ¡\x0006^\x00022rKD6e3/£××'¯O¸x}òÝéåÅÿs\x000cÑN\x0011í
ÄÄ­kº\x00196ÅMÁíí8)¢"z9bÐ¤è\x0015µ|ã(NBt0ó\x0008!Æ)b\èy¹ÎV\x0006\x0019\x0004à:ccÓê\x000f­ônqiÉøùÏ¿¢[{¤Ãó\x001c]$8K1«SÍa®Ìñüì{ôk«&ôniiÑx\x000fXx\x0011©]\x0002\x001bì\x000cq¬;Îx¶ý`f
f$`X[Å}\x001cAe9µa2é¹2Ú^0;\x0005³ÒOé(°}H\x001eÙh8k÷V\x0002.7år²\x0005«ãË³¿Á
LÞò\x0018=;[ÓËå§\^¶^i\/]'2PÇúÌ¸\x001fý`a
\x0016d\x000b\x0006lÔÀë:úÄêº`³_½`q
\x0016e+\x00169\x0001æ¡ùºÁ|«ZíåJS®$[°f@\x0013%®½åÆ^´N°I%¦¼Ï9n®òõSbå\x001e-«î%kí¾Èðòu\x0014M)kæê¹jÌ^²Æðk¡å×u¡\x001f\x0019Xàî	;sa
È\x001aË¯e¦_Ã\x000bþéE$\GnÍ8àý\ÕB\x000bkÙÅ@0®½¯I³L¶á`êÆi)C\x001bËSïªs&kïu{aF	Yc2´ÈfÛwc½Zoª.ÛrCs2AèÑx\x000c¦ë\x001cLH|-Ù¸ÁA³ýA´ýq¾â\x000eÖÈ­iÓ¹åÂæ\x0000è\x0000`¥\x0006õ-\x0012\x001c2³P/ùæÚãd»\x001dÚ¶îõãás\x0019"õå=¦h\x000c±\x0015k¶\x000cÿüìª\x0003
¦P ²ËÝA'®L3´{ÅýPv
eû¡pÄá\x000fèê(ÏÃ¶¬Ù+Uêò»Ï¿Deÿïÿü_ç\x001f?=|9¤\x0013ëè%úF;¾jØ¨çb.'ço./ne\x000b¦\ ã"é¼DWì¸òm6VÜ	e¦PF¸Xª\x0013Å¼/w5eÑ[Àì\x0014Ì
ÁR¯q6\x000fµ\x0010.Í<ºÁÜ\x0014ÌÉÀP"ÇyÇr\x0002JÿP5\x0010\x00016ì/?\x0005óÂ\x0015\x000bµ¶7¨:¯\x001a?e	\x000btÅ)X\x0014\x001fH\x0006óµ\x000f9ÈZáâçbÆ}`SOßO<ý>2\x0019ÁM\x0001ëzc¬:J~.ãu\x0014,î°ØÜ@ÿøüðíO½ÃÄ:
Ø$Mâ&ÞÕÙãv¯j°ØÖs{q~}È¼Æ]3\x0016¨
#bÜU>pù:\x0011yÁÑéå2S.#_3EÝ¬ÆÔÆ>gÆÆòY¿µÍNÙì5ãîòú\x000cñÀ%5ó*\x000fÝhnæ¤Ë\x0016kË©ZS¾õâ°Â-l~ÊæåËÆÝï(\x0004¼nüI÷\x0012ø"´0E\x000bR4E"û\x0011ÕÎ(â«â
3é9\x0001[²Eù²\x000fkcÉvÛ«E\x0012¡¥)Z/\x001b\x0015é9¬\x001a÷®íL0ëF]\x000b£Í}>ùîñéë[@;
ÀûæM;ÃËeã~(êöä»«ë\x000fÇp`\x00038
K±¡\x001eHÊdÚ8¸8fczWÇù18\x0016°Glý~,¸\x000fÇNql÷êØÒ¾JmÒ4tÌÆ±ûq¿­¼\x000fÇMq\ïêPfVR°ï#GqÜ¾kÓGã§4^°uX~)¹qqøÜëý`o\x001fMÒÄ^\x001aK ì\x0006Ã-z¼õ~ µ\x000bgâóá1W½ß
ÖÇô\x0014uØ;]5 Ò¾<H\x001fOsÎuïAG©VÎe\x0004*\x0019Åþ(~HÄýhn\x001fNs°tïÉÂdl.Cq¥ö\x001eÞË!®\f/ëÞÍ¬!TA\x0004¼a©« fÆæª{h½¬{73\x0012H®A²\x0013é<µÎì@³¡{/8H:\x000fácRepù­O\x0017!\x0019êôF\x0008\x001dÀPqÞ<Ý}þåäòñãÃÛ]%Í!!í\x000fõ\x0013)®*ñj®\x0006ÿÍõé»×'Wo.¯÷\x0001n\x0014=G8ç¤p÷7Î\`íC®ÅñÚÌ,Y?Ü8O\x0013á|Á¡2ãð>°ºöô;à{\x000fûy
\x0001\x001e5\x0011N+%¤Ã\x0001\x0010g-PçëÚÁ¾\x0008O·xZ\x0017Ê	@<\x0018\x001d8OÖ¹~¼qªbÁ3VZ\x0012©â9VáfSÔß\x0017Z<á¡ÕAQ\x0007±Eá3Ãz8éâ­\x0007Ë1ÓÁävì¢CýTR.±Uj,\x0014%Ïn?ò-¡æÓ\x0002\x0008?-JIPÌ\x0001\x0005}I\x0014*(Ï7ÛÐÓg\x001a£2Ln\x0015á9öx°«äUp\x0019á¹¹k¢\x001fol6*xf£N¼ÈmõÙüò¸¨ ¸,Çû}U\x001a	kÌ
8¡YÁ
\x0013êÅ¶(²5øA·ÎèÆ&\x001b-´É\x00103ÍðmË\x000c
Z¼ê\x0001\x0004½'Í!ÂsÍ·5Nøm®Uè\x000e§\x0015º¨X6*ÝbULhéÎÔ\x0015\x0007uñP\x0019\x0017o_ßT7\x000eÃ,xÑ\x000bñ²¿KMã\x000ec9MæÇdgs¿<WÚ­[Ï¸Ao»àÕù
ùrãÕSnËÉ°ºù¸VK?np|e8\x0000Î,ÇÀQÃ çB\x0004]x»Q&ÓDöîã¡èÂò5jQUcTsêÈíwaô\x000bÉÞ\x001c}Ý`ibúG©Ð\x0001 Ãã8XKÕp¡¶sóN,3Å2\x0012,e«\x0006±N|F]M54\x0017*ì¤²S*+Z,Çq_E0¼ª¬j¶Ò©\x0013ËM±h±\x0012
Ù
â9ãjmø~å%XÑ°:
¶\x0012Sâ¯Jýª¹rN¦0e
\x0012&,P\x000bu©(áQ\x000cÿ\x0005K¦XIHõbÐN£/èªô\x001fÞ¥[%±Y¨¹\x001dFM7ÊwîÎìú¹\x001aë EæÁ¸îÓ\x000bup~'sÍÖNwr5\x0007QN"æ÷t5ò@Ie?êÎd»»¹]¯EÛÞ:\x0019ÒÌi\x0018÷×lY_'W³íµhßOcÖ¦\x0016(ëQ¸a¶¨õ\x0018Wùcº¿òït}ÿðôøùc5j:Ô\x0017©3Nyþ\~Ýí\x0007ý2Ú÷\x0017×Wï^\x001f®R\x001bð\â¹(ÅÃÙJü@©©[\x0017Yn1?Pæ¶Z?\x000fS>\x001f¤|6±Ü
µÑÅúü; ýt±Y½(^=ï*]R/\x0002«_s¡OzÎ°uó¡&Åtó\x0018\x0010ý2záäO9\x00196ò\x001bjöÄ
\x0000S\x000bÄ+è9&o<K¾\x0010Ý\x00063{¿÷ó¹fûÑ£Â\x0005¬BInì\x001c÷Õ)Úüñ\x0005Ûð\x0005+åKÆ<G\x0017\x000cW*Z.òÁ©}[ø\x0000\x001aë\x0007 5X\x001aBzç^§\x0017\}Á
Þ¨¢´\x0012Oï¼£òÿä¶Èóûoÿßï\x000f_\x000f©i\x0005Trm²©ùqÀO©´\x001fÙÂÒ­ï¯Þ_|X\x0016
c2\x000cÕ"©MÔà°q\x0016\x0017dW<Îê\x0015ô¢).\x001aN1òUÛô°©5Riÿå.`³S6+þ O	ùéÇï½Ä\x000eJiUêgsS6'e\x0003¨\x00155\x0011ê[ÔúºÝfêVúÙüÍKÙ²é%ù`\x0013ê\x0000\x0000ÇÓ4óºÍtRõ³)[\x0010²a\x00016él\x001a\x001fJ¥q	¡Öu\x000bó¥lqÊ\x0016¥ëæôtÝx<Nä(VÞo³\x0015ÆliÊ¤ë\x0016ÆI\x0013ØN¨\x000b»\étéfDÑð*)\x001c>\x0003«yã.x__õqfàD?[{)Ho\x0005TÐ#oãLÝpµ­ÊÍµUõÃ5÷^\x000cËJôÄ÷©vû&\x000e\x001d-\x001bN7\x0017Þ\x000c8_Ê¼UÅ1.\x000b\x0017ê ²M;®±¾Zj~ñ«òÌü¦¦ØH°ª\x0006Ngf\x001c3¤2Y\x0003\x000e'I³è»»¿\x001fæâÛ*_SÜUn\x0003¿\Qsþå»Ó_ô(¦)QLÝDJ\x0017¹q$\x0002Ïp«¹O(íéT÷\x0001MôbLhôb\x000e\x0013¹ÐË =ü¦7Lþh¦\x001b§\x000biÜï\x0005iú¶?¤¹\x000e$¨:yÕDOÇ0¦ýB>¤v#éÞ|ä8CP¶Z Rµ\x000c1ÍÖ`÷ ¹\x0016Éõ#	@ß?yn93?\x001cÚ×H©EêÜÝ¤ØDyì¥òÄµ\x0000ø_d[$Û¦$ù²kM\x001d©Æðè8\x000cè ríVrý[ÉÖ7[ÐÃiÆrßTj=¤\x001cNßIB8ÿ#L\x0012ÂïïþúðéÓãçÃ5\x001a\x000c¢3\x0006û¨*±æËLSÞíÉûÓ\x001f../¯Þ\x001d\x0001º\x0001Z\x0002Fãµ\x0011\x000c4=q]mÍk&\x000fÜÇe&n}æ*A?\x0017\x0004Ö9ÕÊpÍ3ü\x00182ÖÎä0;ÁF¦\x0002æ@\x0002\x0016\x000c+*ãÄ\x0006\x0016{N=1°\x001fsì\x0006\x000bÍÄ\x0002°üê¦\x0015SÑsRzl3ûcqúÁb³÷ËÐÅn°I§¿\x0013\x0002£\Ù\x0017&ëçj·Xl1äª_RqíÒ¨sa`?|×\x000bfuó%­|IÙ¢$o!G\x000b\x0016ØÛ3j¿\x0005»\x001f\x000cZ0ÉÞÇÙ\x001fBQ\x001eJÆ\x0010\x0010ã/©öç\x0012væSâO\x0001X6úTç¥\x001cª_\ø\x000fiÿ²î\x0006kí¾\x0015Ùý2ÏÀ°¦%q\x0017ÅØ!ÎÕ÷¹I¸)CáO\x0001\x0018æ#èSªÀ0T}$0·þTº,\x0002\x0013áH/êoQ(DLï°Z÷\x000e³Òc½`¾\x0005ì1\x0004£©\x000c)q088\x0016~=\n'\x0012o:²\x0015ï\x001f¾Þ\ûã¯÷\x001e>\x001fèâü°c«x
Hhn\x0015Ø\x0005¿¿ºþp~r}þÃùåÅ»åN^·36\x0002é@LçÊÈ\x00083L÷â·:i&îÉ\ËàÌ\x0014Îá\x0012ª!T­wÏuf6íõ²Ëàì\x0014Î®cí\x0012Çêø]kÏÅ¦ÎMén=:ÒÛQ"mÛÚù)\x0017ÓA-SÂ\x0006rn\x0001µËÓ´dtaJ\x0017VÐ±ÄWõ÷¡*\x0002ì\x0015þÊèâ.éj\x0017\x000brG´¯\x001dûª|2º4¥Kbº:´\x0007Û´jOtªmZ{%ç"ºIp\x0018m±âa;ù@§Lí°u`à~¯®½)ÄW\x0005Dn¹ËN&E©50\x0018WßD×Ü\x0014Z|U¨AÕßÐÄ4Ö·âÈºmwnî
-¾,ò-^>\x0017TqýòXÏÅ¶Õkì±\x0016\x001bä|Ñr\x0019+.dÕÌà»?oN×<-¶yZWMÙäê\x001ceê °½\x0016¯^¼Re&6\x000f'%!ö»\x000cùüåëýÓa	É\x001bË¬ÌJåa>å#A¬b\x0018Ô]~u{óáüzy^\x0002áy7ÅóNGMÖ>[¿A9Þ'ÇºËXÐ¶
Î7p^\x000c7´ï\x0016>C/|<\x00083\x0015¥]|ùÄo[íJþf|³^ã$µ\x0003n»AÃ\x000b7¸É:RLub¦N»¹\x0001X×ç§¼öjÒ;TÓÞ©ãXÙ\x0011!ÙÑ\x001aÂ
@\x0001A\x0007q®á±kl\x0013-\>Ñ\x001e.KuÔ	û¡\x0015sQÂÚ\x0019=×ÔÅebû\x0015£ä3ú¨¨&áa\x0013ù\x0011Ac\x0004\x0019êÐÉeÇ\x001b\x001f¹ì¤\x0011©+\x0016uÂúÁÏÄD&í¯lÖÖî/k[.+âJZT\x0012ö4$úFÒX¿/kÖZ¬$Á
j¨ÍÏXÆ\x000eaÁr\x001aé+:½¯\x0012ÜåÚ¯èD_\x0011±hµLþÃÜn\x00175õá¶_»»\û\x0015è+\x00069ø+ñLàÌERþÏ¾Ä`/Wl¬\x0004þì. Ìo²&\x0015µÁÁ¨Ò®Ç\ÕJ.oõÂ²õ\x001a^ÌÉFKÁ£¼^F¬x³/Jtëÿ§î]ã8uÝWÁì\x0004ûÅ0\x0002)4\x0017×\x0001	6@Èz"+\x0010\x0005	\x0004( $Ök¬Ù±3Ú½\x0007g´ß@o²ä¸{¸geV¡23"«·Ùnk$Y\x0010E}_~·\x001bõð¶ÎùÕÍjªDVzÞ\x0001\x0004Û=Quu<þ©Z¶óÓãÝXdúHf>\x0012¼³(YIª»\x0006äNò*nÇÉç"Ù>\x0014£TÙ$aòh»Ô'½~ó\ÈÍ'
ª{o6J\x0017ó¨»"÷T g\x001cI\x0005Ê\x0006éU5ÃåÚ®£.V7«÷w#ÑÍÄÞmÌåðÅ!vy7\x0017õ\x0013)³\x0007\x0017Ç§ÇßMQõ¤/0ü\x0017k¨¢x¹=Öa1QA¨\x0008\x0003Ï¤
©O\x0015R\x0005Uô¢ce¬µE~ZIÏ~"\x0015j\x001eUô}ªèë¨8ÇÛÎã\x0008TY¨ò\x0013Ù±³¨tÏÝ\x00180¯ÍÍÇÊÊu\x0015·h\x0002\x0016ªNU*>Ùûl&\x001fRÕ\x000c\x0016\x0016Ä\x0014\x0005\x001c*Ý`\x0005¾}°ô`bi]1³À4\x0006$\x001e¦>;\x0002Lî\x0012ÿÃ\x0013u13±Ìp´LÅhÁMBnØ>$\x0011Í4)IEü{b63\x0003*gj\x0006«~XZV,
ÀcÚ\x0016'ÄòÜí¯;1ÈÔ,ÿî
\x0008î\x001fJß×¿þßÏW«Ç­\x001e\x0015ù
bèÄY,Þ`\x0002ÙvÎÈw'ðñü»¿¾=9¾À]§Ù n?Ë¦\x000e×çCøîØÕºb1\x0007Ó>©óYM\x001b\x0006´¡Ö)\x000e±\x0000­îáÑJSóD½\x00057\x000epc3.ö¸Áµ]ª%»2R×kí­'O½ËL#-Öp%v#À^)ís¸\x0018\x001bþ­½L\í\x0007ëLûÖ\x0015]^¼\x001e^ºH\x000cî\x0013ÝÍZxÃëÛ×rKP\x000c]£©\x000e÷
¸k1\x000fÂv\x0001ni\x001eUèr\x0016í÷Éô×jÜuOZÂMª\x0015\x0017»òlð©«|5\\x0003¸O\x000c
¼9\x000exs\À[z\x001cµ¤¥\Mv\x0006ýdyz-¬YîèHS©\x0015Ö\x0005öÎ
C=ÒD¯ãê¼Õ´f°Ðhsl\x001cZÝíºÍ ¥§\x000eÛmûZx×nâ
¡7~NÆô\x0019Ûæe|ý©¸Õ¼q8¾±u|)×w\x0006e¥¶,$cWíe|ó`k0¹ukÀ(ª+/eÖÂ×|
Ó÷\x0012\x0016Ü¡ý
H\x0018ñÎ`²ø
D\x000fp·\x000c
¸V\x000fö\x0006«[÷\x0006\x0014:Ë\x001b¯§¢CòÿHçfØ"÷±ñZ¼Í6ÊÙ2nâ¯âD\x0018äÝÅkÝà\x001c¶®õ\x001cÆñ-×V¸ODör£hßÚBo\x001f_~xüí÷?¾g§$º"Ý=Þ\}YÝ¿'ÖoW\x001f©ª{ÚÛt$Èß|w}ss\x0005Ï+ü\x0015\x001049Èd¤Ó\x0016nùE\x0007 f\x0013(æp\x0018áËÉô
&´Àó\x0004=zvvyzòÝñù·ô\x0013|{üêéªgþòñ/íb5<ÿùêãõ-Ç\x0019Ñ\x0008__Í\x0006Ý%`:\x0019rKî\x0016
-[æv{1<ÅýüßN^½|ÍaÈg4ð/B\x0002¹»}x¼û#ô\x0014ïÿ÷þ×ÙãÍLêI&\x0011{ÊAÛb£áÔ(Eå\x0011¦\x000e×MP\x001fàÀO\x0003Ã®_3)í"°Ò¥ô\x0017uIxÇÖ×{Ä\x001d\x0002¿àúeñD[J¯Ö\x0014§\x001fÒr\x001c/¼(i_KxáxCËæ)U¸X\x0012R7\x001föÇ\x000bÙ.¿¦èh\x0001fØâ(¡ÑKi?ø\x001býõº·¹­aßÜÿõOØ~W\x000f¯n½OØ`JÃicuil|lähUtÖs>ý8õó\x0013Ü/Þ¼þû\x000eöðþ_>sº\x0007%y0üÅêúöó7ÏV÷·«\x001fÿúç|ô\x0014¾*ìqÖ±Brp¨Ä²ÇaÊ\x0014úÅñË×o\x000f\x001d¿>~¶kÐ{à0CZ\x000emW\x0019Ü\x0005\x0000®uæApµgp¬\x0012My9¸MÝ'\x000eÃ;Ë#n\x0015\x0017)ï
\x001c­Î¬sæ
\x000bµñ|\x0016Z\x001d&\x0017f%5RøµZð1\x001eâk	Ü3øôÒ¬âÖ\x0018O¦ÇRpWÂo\x0008\x000e7*re\x00018wV¥î)ÖG%9nv\x000f\x0013Å\x0006\x0011¹¦ä(á¥ô\x0003Éí^føÇ¸ºùõÓÒ¹÷öîñ~¾©aj²àih\x0018cJå\x0011jIæbë½=»<\x0004ÆHÑË}¦Òj$N¾\x0004c¸$\x0002£¾¸uTÎ$Æ\x0019m7MêJbÔA÷L\j	{#±iOÏ#\x001fßÆÄâpHuéÒÄl;\x0001ñ¬}.1ºt\^F\x0012%\x0015\x0010±+]ÛÇ0ËÖ\x001b`:eS\x0002÷\x0007ôkÐàfCËid8ÀnË\x000eãqÙ²sª¨)Ò\x0000ÇÒÏ\x0013S©¬@YE3ë¾2\x0018½¨yÙ$v>¯§D,IïpsÛ>jD\x0010öGL­/è±\x0004Ù)*\x0010¡iQ¶	k\x0012OaânwA=/\x0006°è±7&pÈ\x001b»Ug£ÕrzÌõ\x0014 ;ûñóO\x001f¸¾\x0005«Z^~ü´zxèT^?Ü_Ý^_ÍÇÆ³¼\x001aYÌ\x0014ê\x001e\x0016ì`üî#äå«7Ç\x0017\x0017¬\x0003süâüäõËit¼\x001cã×\x001eØ3e.\x0012{(.F`÷E`\x001eÙGfu#»=¢åìX±X¦Kú'`\x000fl `ÝÞÇ\x001d\x0006\x0003¿öÀ	\x0018Ùa+ÌÂÎ÷.\x0018÷{W\x001b»8A³[Mn^3¥Õ	 'öC\x0002ºÝ½JÛÐÑÃëö2eàÖ\x0018ÖÓ]1{.ùSÈ\x001ew\x001fmìr¼/g\x000f%¦{ÙØ\x000f±¾ßhîjßK5ÀÄ¯=°+ÊÜ!vKY1Ä.6k°vïì°~ðk9»Wiìx%ó]%¾!\x0004·÷í\x001dãq/ãî|·TMÑ&#vÝ{ÞíÅncÇ\x0004uüÚÃZ--;hÜ]q\x0011ã>Ý\x0018µ5ì¿
auÅÚGýa<xv¿zïÂÔXa­iÛì¸\x0010 )ì¼[îìyÄªí/\x000f\x001f_ìò]öháÕÙE´NSSP¤µE³êk<\x0000UÝ²zV\x0011~\x0011«¢lW\x001aØTâ~\x0002ü=\x000e¬\x0016ÐÚH®\x0004Ä¦\x0008¥\x0001n.)(C4g¯Ë~ \x0016ñFEy=Ä«K¦,Î[¾@úìæsy#\x001cQ-âMÊÌ7'ÙO²Î¢^<yz¸ùÞ\x0016ßß\x0018óÍ_ÿëóì
>§`"pq\\x000c;©ÂÁ8kG»<x~~V¢Ï§gOöÉ\x001cÀ£\x000e·û \x0007#`0K:k\x000c0æéq\x000eÖÑkZ\x001bk±
\x001f¥jQÙ\x001f\x0007_sÀ\x0000ð\x0015|÷5ø¿þñçïîé{\x001aöK­rD¹ròáXîè'Q×Á¸'{ÔÛ}!îÑ¦#j4ÛN\x000b&j,æ5VËÛÌ8qôÍÛ¥çÁr\x000cº\x001d\x0016ìºÈÞ\x0011e¸\x0007Àj%\x000e\x0012w»ùjiÅSÝNy­ì~;{9«ñFüÔÆÍ¸uÒº¿|ý}{áÍýêóÃÁ³Õü\x0015¸}gÎûÐI\x0017d},ÉaØNl$\x0008Ý³ßÞ\x001f¿½8xv¼+ae-6ÝblìRÈ¡.í
5\x0000î`8Âk=g¤«¸·¯·-Üp¤\x0012\x0011EíJêr­øØã5]çöÉi!,&©T9"·-\x001cçdVtÊöI]qñp»\*P\x0008[ÉpS?\x0007Æv3L
n,\x001e<¢ÇÒù]2ú\x0001\x001c,ÒÒí\x0006ÕÛ#¯KåÒnÇp\x0005ø×Û¯YÿAö)^T&\x0008­îß×Åé,Ínç´)ºßý¨ÉqÖþÿàøüÛif×6,dÆf.å8t¦\x0017÷
ìä³díyû\x001ePÏ\x000c×\x0015\x001efÑc\x0013YÕj¯È(záýBdç)q}7ÌÆ\x001a\x0019æ<ËF\x001ag¾ûÉ_~(b¨$öêîöó_ÿ,\x0016éêÏûù©YÊe}a\x0005>U %\x001a¦Hz$%áÕÙë·'Å\x0010=þþ|WL
\x000e\x0007üj§ÅbXh1ËÍ~l\x000eShÞ½]ÔÒb\x0003Oüj§M\x000fAïa&«2¶[5#íÈ«¦µ_\x000bh=åu0-eÕ`¾´\x001dín\x0013´\x0016µ¹ñk\x0001m"O\x0006Ñr3b¤-\x001dØv$V46|ùñÝ?ö
û°w÷w·W7sqñ'a½ås.f£ÄG\x0010æÍÛ³ó³×'O¶f\x0018ðbÞVË£§XàMEÙ\x000fxuR|.\x0007owßæ\x0002¯Þÿ~÷\x000bù\x0005PàÄõ§ÃÕÁùÝ»¯~¼¼­\x0013Ö³ãÈ\x0007e½%/ËMtÉÇO\x000eÎÏÿÛÉ³óË§ÅÃ\x0006ØâÖ_
w?ÊÙJbÀæè[Äòþ=cséBl\x0017Ë\x000cñ`ïLz¤ÖL\x001dÓ~©5-B¥\x0017cgCm#['\x0019ílJ'\x000b%#7
ðôuuû\x000b	iÊès?\x001c|w÷çêÃÕãýLS\x0019×#Ü¹ùfú¤

×W¬¬È9³ûâà»³ï_\ï²×Ü[§u\x001bw\x0011i¡Ä\x0017$Äæ \x000föô6]GÍååÔ©é1É\x000b¶P¸c°%Ë~!v(ýj\x0011\x001bæyH\x0005[\x0007$qÄ-ZÁíòÃ/þçÞÑøæfõÎ\x0019\x000f^­î\x001fà×`fc'\x0017Ø±\x0008s»(?ÃgìrËØÎíÛoNÓaÿéãóòä.nôÜ6Ð]\x001b¹c fwÈ­¼59rínä.q¶Ü¼aÓì\x000eÔû\x000b§	Ûü\x001e£ÈûÆ}Ä-&-T\x0007%IZâ4$ä\x0010õnïL
÷Õ×¼úøñ©éM÷Á\x000fóëÍTÎ\x0012
)èíKÃ\x00088ñ%w3åªwÈt\x0019|±ë¤éÑnLê\x0006Z#é¼Ñ¦C\x0015y\x0010ùªýÐnLåzÚä¨®\x0013iQ0¤\x0004ÞèVUpýù0\x001bwc
×ãFÏN:J\x0011%®éõ:gfä,¬Ç-Aî%¸Ó\x0007(MÆq&¡ò¹º»¯\x0000õ¸è¾]\x001b,Ui\x0011®#\x0013ï\x0010½\x001b]þÝ=ZO[¼.\x000bh±\x000b¹ïæBñëÃ\x001d^¯÷ÅS7þþÛûÏ$gMÕ¨±ÚÝãg²;¶¿?^ýy?×aK;p¢à	EsÑ\Àb¾ÜEÃî\x001dâüìò-\x0019Ïü\x000fþ~yòýùNí_RöÀ\x000fWD\x001b'Ìêµ\Ê!LcÓõßÎ\x000f\x000b\x001a]ïß¡,\x0007âÃÁB©\x0011_v<ãÝm¶ãÃ>Bruñm¥l\x001c\x001bfÂôñFâÞÉíÞ\x0002ÛùáïÄ¯=\x000c¿w%¦üýQÙ(Ó?äTµóÃV_{àwE\x001boiDÎÚvI\x001f»ï\x0007ÍüX¶ö³ýxKê?öaci¤ü\x001c\x00110&ü\x000bÆ_cO\x0002zìá\x0007£÷ÏlÄòJu\x000bØ¤PTþ\x0000_ì/|\x000cý,÷ÿfuðüúózÙWß¹Tqk\x001b$ý\x0003ÌoÉ\x0018òADùFÙO\x000f¿|{LÍî'Á=¬Z\x001f\x0016c\x0007¹â:	°ÿ§"V¡BækZTaÆ¬©\x0002ª¤àYÓ\x0014Ap_â\x0010\J©|Ô#ÜMà\x0016ÛÓc\x0001¹¦â\x0004uXrâ\x0012v¦+CNÝ$\x001c[íîv.z,%\x0007ÀâBA\x000b¡ø5³ÓZ²ùÆ\x0002xmä8ûè±\x001c\x0005JA\x0001*¸(ËN\x0012=ÍÓ¾	Ý+ã¨åè,k9\x0012Q`\x0017HK¶#7Ï6t\x000c¨Ócñ¨\x001b¾ÂºñÃ£8\x0015Ñç _\x001b9ê·Óc)9L\x00128Ù\x0016\x001c1skà-:öLÝ è±Üb\x000b6\x001es¸÷é²HØa>§Û6t4ÃÀ
nD·"S¨h§ArîÏ~»ï}Mà$ËN¥à(\x000eX¸áÆJ%\x0000\x001e9<\x000c³ÆígsùôûÕêö¶ª#à\x000f\x0007ÏoVÌOÆÀvsÞð\x0004çä\x0006l±\x0015xH·¹1äç§Çÿ1	»yâ×Ã¢PRæÝ;~¤\x0000+Ù\x0002\x001eïÞû£E\x0007F\@¥ÝË5´#SXs\x001dëH\x0015R%ê:î×Î\x001a
üÛl5\x0017Úé\x001cåpeÌÅíÄÛqH\x001f¶Jw+¹|Ø
|o´\x0018\x000e¢G;­÷b\g_Dà±W%6Ví_K> Ýw\x00045ÐF¾Ã8¬&U@\x001c[-fFÚßL@#=ÚiÍÚ*ÂÌ\x0000¦Õ^9;ãº;\x0013×`\x0015=Úq­ãde\x0007\x001ft¶ý\x0019G
jqÑr3}ó­a.(ºÄ\x0012n,Á\x000e¹VjÎð~¸/Z\x0003Òc\x0011­bZì\x000e\x0004WæBLÓ®¿q\÷Õüøc¿öp
õ\x0001\x000f\x0007ý?¨¤6\x001aãK\x0010áÒj%Ù":öv\x0018\x001fv\x0007\x001a×ÌX&pqpn\x0019ìÞ¦vø\x0002\x0004FnÖ5FEþ\x0016»^îáQõ(í\x0001ÞbU6¼×EK\x0001ó:uG¯æìËUô\x001a3úè±\x001c?¬Ç>èb\x000cQuî\x0006únRÇßÇ¼·X\x0007èxô½LÒÀÆ~_Óþæñëë\x0015éæb\x0002IÏîx<xñx=3ßÌ{,I³ìkJìÌXR'N2?9a.\x000f^\¾Üí×¡:4æ\Ï¢«EuÎs\x0001?LÄz¸ÿ?ÏL»hæ¢b5²í¨>s]\x0017\:¼xðbÎlpD;í\x001d\x0018EuêýÝ¬\x0010¬»¬z¤¾é\x0011\x0015Ãý´BÉùÔQ&ÀA\x001d÷Hw°\x0016MNÛ³;+iÉO
eÁ\x0001nDy·âv	Az5RQËëÐÛâz.\x0006^l\x0018SÔm,ni¾ø,¼¸,\x001aQJ«åõ¨¤@v^¸+É*Ã\x001aUËSW*\x0019<üî\x0011\x0018Ó\x0015²_\x0002ì°O$»?±k\x0011ÑJÎrvgUðFä]4QvÌ²§Y«Ò\x0006\x0014yÅq\x0008\x0017þý\x0001SÂ"=\x0016\x0000\x0003VIT¶	.O·Ýîbj÷«\x001d\x001a³åÙÌKÂ\x0007\x0004L(-\x000bQø@î¦ô_÷DLçåÙN%C-ÎÁXnPÊFqÇýM	±<µ<Û¥÷/\x0002ã$¦pm
;òÓÚ|bt+ç\x0002â DíJ\x001b]M\x0013Ê#3ø½Í
£ð+Ïvâ¨£îÁÕs\x0008á÷<Q²rÒMLM=Ê³Ø`S¡"9âl%Y\x001dÝSÝLcLÎ%Æ5WíÄØ.Â\x0006&Î¬=g¨üT']-óÑQ\\x000bmæÒYgÁ´dwqJ2Ä)îÍ^3\x0001[
ç\x0002àXö\x0007\x0004uhîÔmMØÅf\x0002Ö?ç\x0002â\x001c¨­,\x0012õÆz¼°\x0006eãRX5q¦1^d\x0003\x0019k-Ûð@KF:Jtð-\x000eÏO¿~ùécìË^ô#Kç«
\\x0015(J\x0014¦ix\x000cÝô  Òùåñ$-f§\x0018»÷a¥­}Ã6Ü	\x0013M_æÓâü\x000biµØ\x0012%íhS'S530=VÔ.\x0016Ñ\x0016ù/ U¬[´2¶fDB¿ÚÉ²­¸ÆNó)j 7*j	$¨éãb6.jµÐ£\x001d×(\x0016³\x0005ÜÄÝ,\x000c^ñ\x0018W´ë©Åí4çÛqÁàáØ"OX¦õBkö·+¬µÛimiIÈF»-2\x0005j­ÿe§Ù¸[!°j\
JÝË´ZÉBófF
ñLZ èÍl²:Ú´)Ìò`I.J³7Z.I£L\Tî"`^,uÌ[\x0015Ú=â¢t?=ÚqÑÒå\x0012é\x0003v1Ë\x00059ïoæ\x001aKÇïó\x0017\x001b×²¶5êÏFÁu²/äéÛñ|\ØÙ%Æ
]øH\x000b%up¥\
«L÷¯Yt\x0002S\x000c¶n¢4±\x0001Ü.3iL\x0005¿\x001a\x0017m]·ä\x0004F\¶tQ9HËd\x0010yö1©ZZOWâ%Æ\x0018"Fúnz#4NíÄ÷¥&&º%GR\Ø
[zÏÑ!!a<3\x001bs\x000e-
<ÑcÑ¾PúFÁàÚ\x0012ºÂ© úåðßØß®K·´¼\x0008×KêÓp\x0008ß\x0005w¬°®\x0012\x0017ëìèÑë´ªÄ]¹tvI¼O~NÍÈ\\TºÒaÑè:i"\x0000wàÒ\x001b\x000fGW¤	ÃÌ4ÅÝ´¿Æw¿¹\x0007JPÄÁími¯t|ûþ¾¢¹ÁÀE\x00149±ÐÉeÃ#læ¬¶Ò]éøõ·;õlÖÜ¸ñ\x000e6ß6n\x0010q2\x0015v÷à]\x0002Ö2\x00171Ú15¦&p¼Tù=\x000c¸Òg
r³\x000fÉZ\x000bmÝS\x0003\x001bPÒ{\x0000wâWu¨b\x0019\ÊÉ­\x001dËk\x0003\x0007ªÃÖ
n(¹ysX<Ö°	ØjÆ\x0006]-æb{\x0001\x0019\x001e¸UÁ\x0004	áv¿\x0013E£UåkÓ%ÉyuX´(\x001dwrû\x001dò?ÃÕCî«Ên÷×?ïW·\x0015¦G²r\x001bL--¶¬â\x0014´\x001fé\x0012°\x0001þÝÉùñëIp¼}CWÖ&\x0006\x0013"û2¥_ÖiÆÁSÁ­0î\x001eÀ£\x0014SÀéÃEèïlÓ4#m³|+O¬<hjk@¡¼|È~¢E4yaRÁe²GFoo+õS%v.\x0018\x0014à9n:Ñ~h\x000b¹ÅNz,$·Ö@Â¦¾å\x0000Ò)ÃÏq×£b0VªÉq_açALlÆ\x001aãÕÚ×±Yþéúkþq éÔEs.V÷W35âI#B¹¢å\x0002k¡D\x0018jÐÓºK\x0000>?Ù%
¿F\x0015©ËfT0¨cVE7]dµQä,ÆZ+Y7lÀzV£¥íRÈZÚÐ ÂlÇ:#>uX¿ÜÀê\x000f×¨E\x0015\x001e+]×¨3¢y3Q\x0013\x0016\x0015.@k"«Û`¦£*MÄ\ÒHOKSÌe6VÍ¬`j®\x000b\x0015P}EFú½W¢nhO4\x000c«áÆ».*Ë!h\x0018ÖN×ÆìUc\x0015\x0014=a1¬/°ªÂ¢Âê¶¬é|ÿ¹°X¨CFX
Û\x0013k	Ã$Í%G\x001bÛ¯ÉíÕç9ùc°\x000f¿}zR_÷ü\x0011µ#V\x001f?5ô\PI²'0Â«\x000eï¡ÇÄÏÎ/I4âÕ®\x000bkâNrg\x0001±µ\^\x000cÄ^ä»uF°:\x0005 k5ÞÄè±\x0004\x0019Û¿\x0016\x0012«?¢\x0018k"Ë¤\x001dqÅT#ã1F\x0005ÈpÙ(2¬ÎàV&®\x000cÎ \x0000â±Ü°ZbrèÐc	q\x0012Uw¸>K[n\x0018ìà=N\x000b¬\x00189¢Ç"b/½k
öåË4§ÆÃL\x001es0W#{Êg[8ÈpãA}lö\x0014qå3î\x0016û$^ûð\x0017\x0010£6\x0011_üá^'¾­ÎÔ~DÁ­\x001aÙb¥#= c¦
o\x0017Ø¾ÎÊv!;ÜhÉv52j@ÑcÉ\x000e¥\x0007ì]±|©00ÊB<¶R\x000bìðÂIE§Î\x0006¥\x0013Ø;½{£Ê ÕÈÚßØeÈÚPÅ\x001a9T¤? \x001cÕ]³ë1×[=1:óí²µgµåR\x0004§±øK\x000b±Ä~÷±]¼3¿¦îèµCbÒ¦\x0007ÙÍÓ¨ {\x000b6=+akÝ3\x001c#,	ÓÃ]vÛ\x001a´sÛ7fº\x0016»U8Ù5ÒÕ2¸nB °lk\x0006A4º}dUAàÜ»@kx?`°ÑÞÎÉ\x0003êR¹\x000c\x0011(sÚ.¡U
uDFP4\x0018
¨\x0003Rt¸9Lã}\x001a\x0013\x001c«\x0002%i7Ý¼R×É\x0014Þri\x0006AÚt\x00057\x0016\x0008«\x0002µ¤A×\x000ejJHC'¼,z\x0017Çw¨ù¤kït\x001b©u¢âQ\x0004ÅÌT§\x0006·\x000cô&þùÑQàBZµu·ï~®r*/m¬\x0014ØlÖj¯»\x0004¥±ú(A}
ÿ|3´ÇÚ»\x00017±bO`N¦Å¥øLMNzOªFx¬Ò\x0007ª\x0015ÃÙ½\x00157Å%1\x0000ÔÉRÁ*]ÑYMd±\x0019¬Uïò®;W\x0018,\x0019Óu\x001ekç\x000bk\x0003¦ë?ª»¬$«\x0019Sì¨cÝ:ù«ÇÕIz\x001a&ù$®\x0015rQcM¢kY7\x000fÿêqu\x0014g%Ö$ÍGuVbýÙý­­.0ß<®J²\x0014µY[ªÑI~\x001bÈW±jTÈ GûÀFÙ`µMg\x0002w.uj,S\x0007»m\x0008TlîVë\x001dV\\x0006cAà:TÌ#¥Gû¸f¹wcºW°âYäÏ0Ç¾	Û)d-8¹2O\x0002°®%bÚêVE\x001dêºð¢y
hqcN¥\\cCv,a¹µ+»heÅä>.<\x0006P'©t+tS¨ÅÖdôhU]úot$D°F\x0006vÊ¯\\x0003KóKf\x0001\x001c³â\x000cº;º²îü\x0017cJ\x0015u°\x0018\x001c¥GûÈºn×J\x0012ÅM2²yÎ½`\x000cöÑ|øô[éµY:\x0010êÕÁÍÿç|¸¹~ß{Ì©âïFS\x000b`¹ÃbèÖk51\x000bN\x000eN\x000fN^¾¼Øµ\x001døXÚhméYI"FÒÝ(*´(c41\x000f*pñ¦ò2\Wô`ð{v\x000eDJÃ(¸Á|\zQôXÀëJ\x001d\x0000ð\x0006l1ÆZüZ\x0014®t\x001e\x000fÜÔàR\x000b:­
¯.jy\x000b\x0017\x0005ËV\x001c6f´&¯\x0012w\x001d^\x001bJ:\x0002àÂÝVwW:\x0005¨±zÒJÞáÁÛÆ\x000b¦
ÌëÙW\x0018áF#mT£¾\x0017¯tôX2{¹e\x001bð	ædör«(¼í\x000fwpH4O\x0007ÅÃBÜ8\x0013\x0013Ð°¿Å9\x000eôX2ºÜ\x0006kK£ÛáèÆ±6\x0011¼ëL\x0005¼©Û\x001cL`)£Hz7Øýí\x000edk\x0016®¶ \x0007qÀ\x0014+Þ\x001d\x000cY\x0003¯0\x001ekxñf\x001dÅA\x001dòtÀÞí¼9Ønúú)Ã¼\x0006×*ÐÒáé«c	ñãð²`
Öèìmx¢æVËÎ6¼%æÕ%\x001f\x000cy¹m&Ê\x0010ì\x0017ÕÂé\x0000Ûåù`J®\x001dÎnxÇIkq±\x000ev¡¥\x0013-o!.f1q×$ÇúÛ0¼cK³xÿÐ?~ùòá~³ªGQð¼ý¼º¾½ß£\x0007k.°whHr\x001bé(­í¨ºù¥w¾~{üòõÉ.\x0011\x001e°H±·\x0003;Ï"\x001e\x0005Äbé<\x0007£Í~j÷­\x0001î&Û8ñ`³\x0000gl\x0002È#<êQ\x0005¼i?4\x0011çÀ¥nÞy/77ÃÇèF\x001bñÔ\x0002\x001b4}Y\x0006%ÜÜTÜq;Äþ\x0010{5å®"&	.»pÙEVóÞfîî
7#ÍíÛ]´k1Àgü²iì-qx\x000cG\x0007&V:·ÀÔ\x0013÷ÓÂ\x001a1÷g\x0005yw
ë¤k»\x001e«­'îêæÛózû{\HÚÈ<6e
1VáÓc\x00011¶(
æ},½Hìº\x0006ófL ¸WÙ³`V(9?|,R³BÝX7jbªY¸W(Ç½i}Ð®äéâ¬à"Aja½øý¯úýý»\x001fÖ] Å\x0002Z\x001d^ÿxuÿ¹¢\x001eÓz8ò¸7\x0017æ¿RHØF±½S#ý^Å\x0004:>8}ùìäüí.#h
k¢s®7\x0012Eÿ\x0017åÌKMÖ°Ú\x001dUU¨EÖ¤%§óBæÜÉr¡{ÍÂ,\x001eV\x000f?Ô´!?\x0019Åwè±9ZU¬c\x0018g¯KKÚd³â:\x0004oFuu«Q´\x001e}\x0010f\x0007\x0017&ÏÌ[Y{kÃ\x001e
&
\x00181§Èiç8qY}ÒQmk\x0019æé£¯\x0002Ùâ\x0015ÄF¿\x000c\x0019Ûÿ²:s´1'§»ô¬ìâJbd__DZ´sZq9ÓKraÓ\x0018ë\x000f]Í×\x0010\x0017.@êÚW¶fc¹\x0015Ís\x0016ÐÖ!w
6 ÃaKÞ\x001eÜ\x0013¸\x0015\x000eCåyòÄ®`vX\x0010IeÌ@Yqa?LfIÛ£|{\x0006IqÒc\x0011³WÀa.ïºl\x0019ær
²Á\x001c9®À®\x001c\J»\x0015\x0018äØÆíoÌèY Ç"æ uVÃ\x0011èyj$Ry¬qi=3æMöc£MÌÙ°`4L ç1±\x001azÛ\x0006úÊwKÇ9p¢ÕNê3Á¸mCíÕÔpè£wy¡áSà\x0014y\x001e±Ìg£»qVcµÌ\x001eë\x001cè±ôv\x001d3cxç\x001eÂ*©½Õ3\x001bd^º\x0006±ôç1\_
óYÄUôzÖ0cü\x001eÆ\x0019lÏÀ{\x001dX\x001b%q\x0011ÆYÙÏêÍGÆ¿\x001eñ®]¶:Ì·-Î¯Ö+7U¼RÅLUý~Ù\x0002ÓYKÙVrBÙ²>\x001fÓK¨&FÅvz,!Ö°\x0000­\x0010;\x0019eÛ5\x0007*çÖBæßóã·ü\x0003p5Yç0½Y=üöXS6\x000fÛ®\x00144as
n\\x0003V\x0012\x001fÙS\x0015\x0007o/þ~¹³b`
j(V¶4HGà¤¯\x0019J\x0015FTSù¬\x0003\x001fF\x000b+vo/¨6pi\x000bØÍYÊ0f\x00147ÌDÕ\x0018}ÔjÉ¸¢ëJÚ|i­côÓ
nºb`\x001cöú×þøB}Â0ñVoÎ¿¯Þ\x0001nE# \x000c\x001bbý\x000c8(3¬:\x000e÷\x0007ò¸¥Èèüûñs Þå~[\x0013ãn ;B+1\>DëÁs]¿rA²ÆÇ´W\x0003÷Å\x0013-\x001fÇ4Ä¦\x0000ãÆÈ#<QÖ_\x0007ÜõÌ\\x0000\x0012@U'«c}G<qï¨$îÕ<,\x0018bnù\x0012¼/)L8ÆAìãD\x0018½\x0018D\x000eË¹
)±.!2Ô­2]\x0018ãq[¸X£l,= '89L¼*·~0Y¥\x0004ÂOU\x0016×!\x000f²õ[³\x0012µ\x0007ìYÅÆH\x0016¼c"ÕÈrÃ6dø¿§\x0015ÈNÔ\x001eÑb©\x001c&ì:dÔ'¦Ç\x0012d\x0018Z\x0019eÌa)ò;â
Þ©×\x0012\x001b\x000cv\x001bµ\x0018ìu\x0013;bVãÍNN=§÷8È\x0006­j#N·Fd4~YL\x0013³4Y-D\x0011.A+h1òÝ£Sv#Aþ»Õãsóø±hÖs\x001e+åK¾c\x0006S¥«Cç}w|ùlg\x0006ÿ\x001a\x0010«,ln#LJü\x0010`s\x0006iVAuEò\x0013Å3\x0011;m³zÄ\x000c·d:Ä\Zøª¼®HÊØO±ªE4á;÷*ÃýÀ³6JÞs\x001cÓÜOØ\x0019¨&ôä4¥AdA%ê»\x001eÄý ö
\x001ej\x0011mÉ\x0001¥Û¢ÌE\x001aE/SÑO3	±þ 7¾fÖ÷\x0019Ã	Y[éÔ\x0011ü®À<D\x0017oz´0ºÈÍÝàE»RM\x000c®·ZÆÍ¿Àv-#eó¦\x0003Wo\x0019G/wX¿\x0005Ý\x0013nAäB\x000b@ÌÓ]\x00001
c\x0018ë7qP³PË\x0018\x00129qÛÑÒ*\x001a\x000c\x0018Y/\x0013ÞØx\x001dÑ©íüã­!\x001b¸ü\x000e\x001d\x0000JÙÎ[1î\x0016Ç8L®a$/Î©6`¾[iX\x001aìýÑ\x0013ú+3!1÷\x001emIDwÀR/â\x000b\x0000i¤Ïv4\x0013îÊäJ3­#©­ôc\x000bA\x0012¸³±\x0012Wf/ç !MvÓ°h
dèVM(	2unÉ½X<\x001cR¦aÝ\x0014È,!%Ë<±Æ\x0013ÞÓëf[-`Sh6{`+r<']Ç8á.ËØuØjb\x0014}l\x000b÷\x0003.è\x0002F³E;q!	¹nTÕ\x0004$½$ÄÒ'\x0000!½í ÷³nPï\x001eMV${\x0001RuÛ¤\x00179­hÇÚU@bek0,
dæ\x000bWA¬\\x0013¢¬í½\x001cÚ\x0006/2¦å6CNo\x0000£!E\x001ddÝqc'¼]s!3õÝmô©â\x000c¼ÿH±<@îÅ\x0018ïõôjÌ¥\x001e«ÌHk\x0018ÒtÇÍ\x001b`.$dl\x001dI,±(¯;ªPÚhÆl» ù¤\x0002ÉLH¼¾Ñ£	\x0012¶F6È©L\x0003`*v¯{BÈa.$@-7Ø\x0002iÄ\x000f@±,¡/yÛc\x000ef3Z|\x001d¶åòUÞ¶fU\x0014:·\x0013ç¬Õ\x0005´ãf(óZ\x000bI\x0005bÃEÛóÛîî6°KîcÝÐ±-~©\x0002)]11:Ñ"d\x0008²ÇÄxÒØÖãF[KÃÇ#)ë¦ë\x001b\x0012í~ Qì\x001eM>HbÀ¶³e\x0007êÂ\x0000¹KÃr\x0002z4AÂâ\x000c»¸¶³ìAS¥ª3\x00191â$RÍõ\x0002\x0019Sé\x0012\x0003Òá\x0010 'ÊåfBbV =Z ±I\x00117SÛ^LÝËH¡ÉHÑ[í]£0F¥»\x0019Å/é{ô¨¸N\x0016H«\x001cÕ¾Ñ\x0006\x0014K/æ JL\x001eK}÷\x0001&)=Ú =ë\x0004Ñä\x0008CÌÇè&*Òg2b\x001cÏûF\x0017¥®#ßn²-U\x0015Àh×W°½x$}Ñ·lp÷\x0011$¼b.\x000bÎs	!@zi/\x0006¯Ç[o½: ÞVfHn÷^cÐ\x0002\x0007\x0019p\x0013\x000f­;¹Ýq\x0013\x001dË¯\x0002d\x000eëÜÇë\x000eèØ
-Þ]Ä3¦ÌÉ\x001aÖe+µ\x0006|Rf\x001f\x000b' 6l\x0010ØZH\x0007Ûd\x0011µ`H\x0014EtÒÇ\x001c;\x0001ï\x0011\x000bMBn.¸"÷o;³j9Öi\x000bcÈq\x001f?è÷ÉüQ\x001bz¯¿þùáþú
Eàá»D\x0018;Â/×W ç\x0019{ÉhòûØ+`CRÑ\x000bÖòàúR3\x0000tù\x001fG\x0017'/Î_<­ó\x001eð?ÝäÛØ =ÿùêãõ-fÆ_ß=N\x0010¡þ0]_,¼B0Ã\x0008\x0008q)\x0006pÑÛ~/±\x0002ôüßN^½|Ypç/Ï.§¸4\x0006èQ\x0007¥nxB00º\x0011È|.ÑK\x0007¸¿\x0016*Èî?¹«ûÏÂ5ÙûÕíû\x0003Àù·W\x001302Å»hv9Ð{z6Dî:6	_\x001f¿þö\x0000>¿~:åµ\x000fyÐôh\x0004u¥è\x0011@\x0003Øa\x0014MGÐb!º¬Ià§\x001dTÝ¥_?­zµ»§«·¥%Â8\x0017L8âBmñXâ0p\x0016y^\x000cÑç­ñ;=>xM\x000f®oßÝÝÞ>^u¿a\x000cü0×^Å££77«wW\x0007ß>¾ûyõñÇ»©\x0005êÀ\x0014Àò4{E*uø¯\x0014í	5[\x000bôÍéñsL
o¾zvz¶cÖd\x0017\I)\x0005Ð\x0012ÆÕbA+9<ª4ÚÈì;ãÞÿÜßÎN\x001e>!ÚùÝ«ûgwNolÎ\x0015å\x0000Ã\x001a\x0012:¹+\x0019µ.ùØwy\x0015¶7\x0008w~öâäüàÙÙ÷;w¸5!M&<Ö\x0006F¼À$Às%\x0004\x0000\x0007Mèv\x0002v³n\x0017!z(ð«Ð¢\x0016\x0010\x0000*\x0010¦´\x0010ú9C8I1ìÔDè`ëÀ"&$t¥ß1¡*kÐé­
¹þ%£ªÀ\x0011=ZÞrÂp3\x0001rã(|ÉE]\x001d\x0001­o\x0006üã>«ë+êbL\x0005\x001foV÷¿^ß~^\x001a^'®[8þ
Sy^\x001bNo\x001d°oÏÿï¯_ì ùñêÇ»\x001fß÷¶¸ç7«Ç«û»Û)ä(\x000c\x0001Ç@Æ«.­Q¸?È<®¾;ÓãËó30VïW\x000fï¯ºßÈæo§3Ê\x001d­¿qDµ¥YàëÕ§»¿þ9	+¤¢\x0003\x0003\x0005JáÀã4Æà¶Fªt\x0006|}üæìôäl¹&p
í\x0013\x0006SO
Ê\x0012\x0000s2Ô\x0010]$M\x0005F>¢Q¡\x0001±TÎ\x0002"ªu+Í¥\x0018\x0007\x0010CZ4)\x000e\x0010S¬Gô¨·XF\x0014P
b½Ø\x000ctÚ«	Q)w0&©jÄ\x0018\x001dE\x001el2FsÿG
»Ë¢Í\x0003'K
"üB¶z·Xà#ôÏeG5XÏïÿú§Ì:\x0000Ó$³	\x0016r\x0012%2XÌÜù\x0002lw\x0017wZÈTqõüüdG½U4\x000cHC\x0013)-\x0016[ly¯Kp\x0011H¹÷	ØòIm\x001dnõ¤y@ÛÆ\x0014E |\x0019S0²BÙ­½ÖQîCnëÍ×j¥ú¤TËÔ8¨ÇÔÁà¼±2¦Oìæµ¤°WôIqëh\x0019T\x0014#`TN|ÀAU÷$7P¨lEõCTßøþó¡çë0,|\x0017øý\x0017Ç\x0001 :³óN7ª\x0013¡n¦Â7(Kú­?\x001c¼ZÝ_ß>LØ:çi²ìHÝ]¦iÞ¾¶K[õWÇç/_?`¾\x0004S¯\x000fINõZHìR­\x000b¤W|w»ÏAo-ûZJ;¤´
¨ùky\x001bey+¤ì< qk\x001dÕBú!¤o´Täó\x0012îºÌKÔþaJí·P-e\x001cRÆ\x0006J¬¿gMô%Ê\x0003ÎÈBÏnñX\x000e×kY;¬ËpO0å\x0010­Ó(Ä\x001dVÜlJ?\<¾eñ¨"ÓpóåÌÚÿË­¨r¸x|Ãâ10\x0019£ìQ¶ö¨ì1/Ù\x000c(³i\x0018Kí)¹	¸+Ýèé\x001bÃ«Ç/x!ìQÒý°þûbt\x0016ÛCÉ\x001bO)Í¶?±R\x000fv¢Ò[ºú+*%AJëJÝ\x000b¾qñËÂP.<zL\x001aÌË>TKT÷Æc¢­\x0013(\x0003ÏJÒÂÇ¬-xbÌ®å}\x0017yf:Ã])ÊSèÖ\x0016û=6\x000fÞ·Í-ï;\x0018*9 4bi\x0010eí¤íE\x001d¥\x001bÎJ×4+]é\x0002H+\QÚ*Rºnû\x000b\x001c\x0005\x0006
Ç£Aÿ\x0014CZE\x0012Ç\x0008i×÷µ+ÇÙÁ.älÃ.ªl|']¤H\x0010ÒäÔE\x0016îBØ·O¾áZJ0Èi\x001b'{ÈÉÝ×û,/|Û\x0019^\x0007	¿ïCzÕ²	ÙÐ\x001dáQQjzßÊ9d\x0016ÎJ?44|¡!ZHJw|;Ë*Èí,íðÇÌ§\x001ce¡
\x001a]Ìb©|±LâìpÎ-ÿÐ§\x000cªaZfrð5\x0014ºY\x0019;¹Ùá7
©\x00052EJàë¸eJ»Á\x000b7\x000bíß`\x0006Á4Q*\x001eJ¬â(Îjòê\x000c©ìÂ÷\x001d\x0019B6\x0018:ò1¤ô¹4tEJ9Âmv\x000bðàCé²\x000b»\x0016J¾âÚ¸øûáXú±-Í!)CbWZÒ\\x0004\x0019±\x0005"Ó\x0005\x0012xCçÊâ-Ýb\x0015ý"Ê¨\x0006/<ª\x0017ÍäÊ­Ì\x0007+ÑXVo¡Ôjá­\x000cnË\x0003JÛ`³)0ÌgÊÎ\x001c\x0002z\x000b8\:±eé`æ¼N<)¸°û­µiá©2Dñ¯£B;»×e\x0018¾É!ah!\x000c\x001da,É¡(~u§·½ÕÃã;µ\x001cßXLf=\x001f:Vü\x0004Þ\x001d:\x000bWwCÊØB©Ã!;Ù!\x0005vôJ\.6/\x001c\x001a\x0019©ÁÈÐ9ûÎç¯m)\x0015\x0005ÊÎ\x0013è:¨ópÌ-û$V\x0006[\x001eJÃ-x1Ñ=Q\x0019Ô²Qc=pß{UêkÇÒúC¾6F/gñQÜèy¡_H0ôPP¿kô\x0006yööc\x0016UÙ*µåm(è¸lZb/\x0001¥uõ\x0017G§âjJ2°2ÖÈ+6-;\x001aµóI\x001bf¦§\x00032
²\wl\x0000O\¸Æµ\x001fnDô¹²H\x0013R²åsÇvñä¶sj)Í\x0006eÍ\x001d»\x001cSb\x0012=á*±Í\x0006eu&SÞÆ:\x000c\x0005ß82Ã0\x0014üîÃõÕý$g°Yò_°"ª\Ä½N¿d\x001eYçð»\x0017/OÎ§H}\x001cúØDj2eü#iæðÆ,¤z;_O¤¹]n	
k>Ñß=MÑ¤qH\x001aÛHñ,òLê\x0006:¶45c'æLÒ\x0014\x0006¤)4\x0016L82SbLIõ´6\x001c31³\x001a`fÕîõÈ¤N°:5brÎ%\x001d\x000ehn\x001bP\x0015\x000e5æCyñZ0\x0017¿v«R\x0012?6PâýÇsj´SE\x001aåÐ»ñôËAµ\x0019jÓ\x0006$\x0005.b«\Þ¬\x0014¯$k\x0006SÔ¦)ês©\x0001ARÏ2 8¤Q@Ç|\sAÝ\x0010Ô5¦XÜí\x0008êJ\x001d,Ê÷óÅ(Q\x0001ôbÒ0$mZK\x001e#i¼ê=/yíº\x0001Í#·õ¹qÙt¢d /g}ÄÔ2GU)êÆå v¸êmÛªO¥±\x0010\x0006uÈkIö¦¸ò]¹N4"Ìa¢ÑlL¸®[ÆD´RJ¢Øá\x0005{ÓX\x0012Ï\ÐáæäÚ6§¨»c>ä"G/^L§4æK:|ó®íÍ¢\x0008SVRÑQBR+¤;`+Hýp\x001bõmÛ¨/ºH
Ã\x0014®r2¦c®Äy¤N
Hj"\x00053KÆ\x0014\;Ê\x0017þ+¥\x0006¦lîJ OêFo3ò¼*­Ä±Â+Ì~O)¦0ËçiP\x0003Ò H\x001dú\x0013©ª\x0001\x001bUJå\x0011·Ù\x0001ÐÑ³¹ i\x0008Ú´ \\x0010T+\x000c´\x0016oSN² \x001eó%Ï$Õi\x001fHKKy$õY²ºrbom
nñ,ÃY\x001aÛf)¾{S@5Úø_¾çY\x001aÕr£4
¯w©íz¬)\x0017 i\x0003F~ä2 \x0018ø"\x001aGx¤N:¬¿A5\x0014è7WÞß=>L&A;Xð±ì§ÉH\x0011¤Ë:ðëwv;#`\x0004ýæä{ ÞÑ?¾k\x0006¸¦\x0015\x0017·ªr1A\x001f$'0¤,´Od\x00064Ñº\x0001ífÍÆ\Z<{D$\x0018d_u.m­­&Ú0 Ý¬ÛM\x001b3U¿PÑ©`Cb\x0019v¬:
ûÁM\x0003ÜÔ\x000b[¬eë?¯q\x001d{$±|w¼(b&®\x001bÌ\x0005×<\x0017r,ñ\x00074\x0007J0\x0014q\x0013¼\x0001î¶áÒ;\x000c®u2`\x0005hÊ\É(F6,4©Qu:îe¥Á6\x0016·1V~ ³°KÎÈ.Ãb;QµV»\x0001-~lÄk
\\®ØÞWÉÌä]§\x0011/¦5ñ1Xr_-òK«Î¿¶A¯CS\x001b6ëzfãb2#Ï\x0006½¾$\x0018-.\x000c»\x001dëkáMÃéZ§G§ î¢\x0001¬.¡´\x0015ÏµÚv¹4ñÚ!ïf×l^TíE/X\x0000Ût0¯ßÇ^fÜð¤p­GÇV¾å\x001c\x000e(NÏ¼6H\x0019jÔû8*Ìº`¥ðnÖ%Îæõ
H\x0015°m+/·(´ÛyG-´q0\x001bðc+mnÐöµr%çÙ\x0011{áõCÞæÝ!©nt­.½aÂvâ\x0006ð\x0003í7
Í²Ôz\x0014{L%/»YPëÝÁËækì¶ë¸×\x000e\x000f7Û|¸a£½\x=ö\x001fæá\x0015O·~ÂïÑ\x001b\x0006Ó\x0017?¶áâò
(ÀaaÙ1o9U?'BÆ-¼qp\x0016f#o<ÌÝjSì·1ÉjÛ.´lÁMqR8m¸FQæ\x0005í½¥d\x0010y½Õ\x0016â²³\x0002¬\x001cºUtÃ\x000bß8ÂÔã/W·¥Õéó«Ç¯Ó5Ö*°÷Û p.\x0017¿À|%·\x0018;\x001bÇß¼.=M\þcM¸f\x0006h¦\x001e
®cÅAg°\x0005 Wª£\x001e mçËÎe³\x00036[Ï\x0006¶@\x00112!\x0019ÞýG1ÂöD,{.þáÇë×ß©F,è<|úåK\x000b\x0010\x001a½fB³Eh\x001a\x0008u\x000eò$i\x0010î9¥\x00161@\x001cÄ¸u$m"vr@Û£ø¹èéôF\x0011¿Ó0!\x0015F/I\x000b0¥àÁ£ÐÅ\x001155&Ó%P÷\®hö¶\x001aôº=Ì\x000b\x000côî×Ü»	þp2\x0012ÂØ­{FN·qï \x001a.\x0016ä4¶Ó\x001frÀ:eNõ¨\x0016$»-ÑiL[\x001aü®O\x001a\x000b[÷à y³º¼ºv\\x0005r¨Ø¤#\x001cá¢¡¥Ù·MÚ\x000e\x0006®7í7Çç'§\x0013i\x0000Z %§<é¤\x0015m$RÅÕÙ±Kô\x001cH½®VDHüXOéK3r¤tV$\x0007R²Béíµ92\x000e)c=¥S«t
ú0VdÈ°\x001d®\x000b©HKH­¦\x0015*2õÎãOWÓÙ¨ÓSöÈ\x0014ä:Îö¸$·\x000cnÿ¹88>}³£ÑbÑô\x0019M\x0003#öî.\x0007uD+XÒ\x000fKA%z ¶%Ej\x0019mÑ60ZEº½È²7\x0008\x0018\x0013~;Ö[Ëèú®1ò\x001dÄ¨]ÉÈ½íÏ«eô}FßÀ\x0018"§!\x0018LÕfÝ(Ç\x0002\x00188\x001f·ï9µ¡Ï\x0018\x001a\x00185ë$
+=ÈÚÅwÛqWË\x0018û±±d¼\x0003"ú9±Øsz\x000c¶[û¹\x001a\x0011ìïR¯\x001aC\x000e=J%G\x0015Ýö÷<Æu,¶GÕ²?ú²¨\x0015ÅÈi.ZÞw´Û\x0016Ð­\x0005\x001cîß-\x001bx²T¬>Qß.ÚÀ#3¦ílÒZÆÁþ­[6p¸ÂhÞ\x001c±8uÖ¼ç°\x0016r°ë\x001d<zv\x0017¹_2½m¹ÐØÅ'¡\x001eìàºe\x000bÇ}[w×i¶ÎÕòºG®¬3\x0019\x0007;¸nÙÂÁ\x0016ç[îJÀö<ÛY/µý[·là°kAÄd²ÀKFñÝ\x001aî»¯\3\x0011\x0007Û·nÙ¿»+ª=²\\x0015Ücº3fëâUË\x0006©ÑpN+Å.¬gF+LÚÎ\x001b¨\x001c\x001c2ºþ\x0001£§ôé¢°«Ä\x001a%>\x0008ÝÒ4CÆ´\x001c2Ör Ð8Ì\x0013fÄÒþÁaëßÅÛc\x0018¸+Êº\x0019¸+*ì3Ïó2ä®\x000cûú¢Àºõ·ÇÕ6.³þðqìÂ \x001cW¾u;xË$	¼¥³tà°*3uà°ª¬Wr¥ÏáÚBÇÙj\x0016ïïfÕ´±ÂUL\x000eu\x0013;÷©7â¢\x000cÛ*´Õ&æ&kÓ°\x001aÂÛ|©À¦5ld+¦ß\x0016¨¶4·\x0016j[`YÒMÄ|\x0006vZ\x0006Y`Fm'b×/°Í)\x0010Ú¦uå9d\x0002§¨s~[@¨Úq°9¦¦qÏR\Âf¢ëÔS×{\x0016\x0015/GÝ\x0018ÒÆEåÃ!¿|°ôì®½Á¸èOÔÍ¯ÚPs¢\x0012&òÊx.at.(^Å×7¥·XÛÖ?
ÑFv*tÆË\x001djÞÖþÜBÝÑ\x0018FT
C>j#äóìñ~:\x0010\x0010\x000c5\x0008¦á4\x001c?wÞ¯×ý¶ìø:\x0010ðìò|$·}I®\x001aÐ)ö^\x001b
9²pûJÛé4u~\x0000è«\x0001µY\x001fô(Ô(×u¸lï~Ë³\x0000Ã\x00000T\x0002Ââ-û9y°Ë«¡¯\x0015í¼PÏ\x001c¾8àÕ\x0003*G÷ÉÄf¨OÚuÛä2¼4ÀKÕx°t­\x0018\x001cJ|Z>Ê)®ýq4\x000b0\x000f\x0000s\x000b ß\x0002\x0018G¼£DºõvH¾
Ïª>Uõ;L,J<g,%Ð\x000e#®"\x0015¶unê\x0000õ\x0000PW\x0003úTQSW®>ÑJ«\x000eÐ\x000c\x0000M= \x0015C"(ÉºpÞ&~ÅX8±\x000cppØúCÄ&ê¶;\x000cvéá%¢9\³\x0019¹ëÌÛ£¡yÚ§¡ùYÊw·H\x0017º0r%tÎyÄÈwØmqº\x0016N8ótïÌã%mLÚÓgõ&§ÝLÆ·´µtÛÀù½»èö41á½\x000fÒ\x001dè½\x000fÓ\x001dæ½wÇ\x0002\x001dÆ[îìïÝt\x001e#»û"6s<78ífZÆ¼ÜÉIíYT\x0004\x001e;[gÄñ?o+ßzíªåµ§Î\x0001\x0017tçñ±»¥\x0016OÞZF¹izzñÁ\x0005©Ñn<yé¾©7]FåÍoºfÑjU´.èå'YôAÙÎÅ5r±ùö7QUÃ$ÕJI\x00184ëxTs·ï·+êÞ¾Ýzû¶åí£¬½áK­ìvºx©ÝÎ­¬åÜÜlË¢÷£\x0002ØÕów	¡ÃvÆê<Lí´ôZ"Ì£´tO!ìàtõîçÕã§ÉWî¤\x001céò°t<ØmÝßÝxáàô\x0018¾ùfrADI7PZ+§¦ÇÒâ2\x0001ÅG¼³Rs\x001eeì	Ü\x0003eì\x000bÜÏ¥\x0017Â	ë¤ÈÏ2ÝDO¼ï:Êì\x0007Ù·PbC²È5G	èÄäÄä\x001c¶O¢JÈá\x000bÏ-/\x001c¶´¢xÊ½\x001847$Ë>oW®Ì¥\x0004\x001böÌ^X2\x001d
ÖÎ³«ãëéÞÙ?Ia\x000b\x000bV`]²«rÝnLÚA>;9=8~¹«µ¡@®\x0015á\x0010²¯\x00077\x0017Ò)[ÀF©¤ÑëÝë{&c\x00180\x0006F¯9Õ\x0006R-»FÎ,yy\x0000[ Ü%©\x0002Û°ô¨9»[Ðb\x001e£V\x0019IyìÕ\x0010*Ì®«Á®"L\x0019\x0017d¯ø(C\x0003eàæÑT´\x001aYu\x0001&¢¬\x001b½ív©CÈØ\x0002i¼¨ì¤\x00108Ñë(\x000bpH.\9:æ!en ôÓúUÆª²¾QÇ¥6v«¥ÎLz\x00009ØÍgC®HÙ'\x0012\x0006@HÝõIöÛ]\x0011k)íÒ6Pb\x0012)¥Îl®yÖ¥ÔÛWÉ:J\x0006Û¹K
ûyö×Mô|±c¬(+°[\x0003f\x001ed\x000cÃ3'ÔCZ2JÄhá}R×\x001b¥Q@J#]tfBæ!dnÔ*ü\x00076¶guÇ¤X\x001d7å'J\x0011ê(\x001aÌÊ¤êg¥Å%Z;ÌtãFñ,MGtóf2!£ia4\x000b2ÂQÎ±3rÜÝ®d.¥\x001fRÖoè\x0016E{ÊöZu³2³gVf;µ2\x000e)cË¬4\³­=VòDìpUn;O«2\x000f)ë\x001d\x001aKÍc\x0019­ÌÊ¤X\x0018!Ã>¿ûB6Ò\x000eÎdëÏ\x001d\x0018KËY\x001a\x001a\x0005(P²ÍÈm¬ôÃ¡ô
CúÇ¥õ²¶8Cñ¼ dÔ÷ZF\x0019K<4,q\x001d¼p0Ïä\x0008OIZ¦ç¥gc\x001aÚ©Á®\x0004ÈÀ)ÚÁaÎ%Â0²\x000fÝmgR\x000eWxhYáÉÊ
w¡4î\x0003Ê,ò=9ø2æA¦áP¦¡4Úr.ÆV¶~³cÙÎ\x000c'ðRÊá\x0011pE\x000fQS?IË³Rn·7ô^Spbt
Áö4I£W(òÊ	Q¡ÅÇNÖÌºa$Í¥ºC[¬\.;e\x000e|ÿ-Ü)³\x001b2º\x0016Æ\\x001a¶±YY´\x0002)\x00143ånYÁÃ9[æ¤å	i¢\ÇrZ\x0006Ríî\x0010;\x0017Ñ
\x0011\x001b¦¤ÅHç)i)Î»¦d\x000fd\x001aR¦\x0006J`au>ÌÓð\x0005RDÍáú³Ì\x000eÒf8%és5¤w<!UâM2XQ6Kv·ù$b¤|µ^~Aô_pþxupòþãÝíûg«û«ÏN;[\x0012_ HÊ\°Ckg¶¯\x0010'\x0007'ß¾:{ýíÁ³ãó·ßO`öÜ-ð[ò¶TcºÐIWéÀb^g%òËö÷]\x0006©	3ØN\x0017ì ³6Ò4)YóDó¹Ä-U^·5Ù{eÂ\x0007¯î\x001eo®o'ã%Þq£>ìb+úÖ½óî2áËWg§/_3êuu\x00142âÇzH¥ç!\x001cÔÒk×¿%'ô\x001ej)ýÒ7P\x001aM@×Õë.\x001b¡4»ëÂgR\x00063 \x000c¦ÒÆr·ó'\x0005H^;îE\x001fü¶ß·r8¡e,a\x0000¹39\x0016\x0019²4\x0005uà,iÛ¨¬¤\9\x0011e_Ìi6¥+-v\x0012¥«YÄHóÕ\x0010·Ó\x0016ë(ÍZ»\x0018)ñcÃ¼¸2]ÙWü¾£	K\x0019×Ù½ÄØ\x0017W?\x0002<@&ï
\x0017ÄèvëûÍ¤ìuWFÊ¾ÆüY)÷1Ìj¢bHY ·\x001bÏ4iSÞ1±¼#Û\x0019\x0007çwï~^}]M)?ÀPªCÒ4Ç\x0006TW+OH\x000b±­qyp~\x0006ßÿÇñn}©	3ø\x0012Ê\x0003NlE¯\x000bgÈ²xÂÎ\x0000Ô\Î¾è?vPïþWprT\x001a¸9Î\x0017´QÉx\x0006½-5XÉ\x0019{ÒÏØë²×d>§Ï#[¦ô&°ÉHSí¨wùgcöôú\x0010³\x0017+	F¯t¤Ï±\x0008M!fr¡\x000bS«4\x0018Nú\\x000fyÞ¼Öæp¸Í9È2Êz×­b.§^ÇÃS÷"âó9\x0013\x0018G%ÿ\x0012µ\x001f$\x0015&¥¼wïv¹²¦AáoÄ½³wÿqØ!m $øüþêáÓõÍÍÝÔþ©a±°Rµæ0y^Ill&¬Ûµ\x001c<??¹xóòôôlç\x001e*°f\x0008k\x001aa½\x0015\x0011L«$#ÜÈæ\R#Fg
m\x001aÒ¦FZØBYFÝXñ\x001dÙà¤µq¶#\x0012sam/\x0002äðiÛ`½\x0016g\x001cæâÉÐFÏ÷Lm·ë¢[`Ã\x001064Â:#Ñ}g3õÁEØÎ\x000b«õ*ùlZç\x0007´Î·Ò\x0006\x0011¨wÑÈ)m\vÛ_Ó\x0000ó ·Î\x0004°ÄêQfO¬®\x001b\x001d\x0005Ô\x0017Ãö:z",5ôl
hên\x001eB>u7kõv·zZ¯\x0006´ø±6uí(\x001dúKÊ^cy`¶$
´z0k½nµäÇá±E³°a¤(Â;ÂX£iZ[¤é×²A¨ÛÀ½]ÝÜ¬îßO]\x0000°\x000e¯c
]wglpqwÇ·Ç§§ÇçßN0®MAË]@ª!±%YaL³ÏçÈV\x0018ñ×Î\x0004ô\x0003@ß\x0000Ø]îS@G}\x0011ÃÆÆ5¸»ß×LÈu\x001c\x0013!\x0007aÌ¹\x000b·c:3Ôi\x0016\x0011\x000eÞl¨ký`º\x001e2eÖ\x0000H[R\x0011Rñµ9x;.5\x000frí&AÈ~£ùFØ:BúC'kF\x0010·kë\x0010õZä\x000f\x0011ñcÃÛNE	\x0018}v\x0008ØÖ)Ç¥fQölhZ7®ae§XR¤2ÁþÎ¡V[ty\x001c^\x0017\x000eeP)\x001f«!C¥4\x0004nHØ
£\x0008ëëà\x001fD1çQ\x000e÷ÈÐ²I\x0018K
\x001fÞãòabÑmo2$\x0000Ì¡Ô½^\x00124-ujÀyWÚ\x0000fÖ]gDÖbv!Ý¡­9¦×®¥7¡\x0012\x001bã%¾Ó\x0007#5VpU6Oy!¦CL\x0013[\x0006Ó)±24V~ò`ZÝÉìî8\x0017Ól`6ìEØ\x001d ôoC\x0005=ÉMQC`ùìnÒ<\x00133
Ïp\x001aNqÌ³ÅÂÔ¹SôÌÙ%Æ\x000cqÙndì-d[\x0016º7S\x0001à/´ÙEFÁÌ»»ÊÎÅ4\x001bM/]IC\x0013)±òÒ9Å4fûDìµ\x0012Óm`ºÑ¤ö\x000fH£\x0014
(t\\x0015J?62lP6X\x001c4\x001dMäWJûK\x001eå¼-\x000fUéõpjzÝ25ÁÒà¦F6Döy%\x001d®`Y-|åÞå!¥k¸óxXÜÉóMRz2K¾®Ê#¹\x0015³\x0018ÃðRFëOsçÅ\x0007ê¸pIK]ÖÛ^Å¹:\x0014\x0003³{Ùð#Ý¿?\x001e®\x001e¿®¦\x00001Å§Hík°×¤aA\x000c,\x0012\x000fæ§\x001d`\x001e_þãxq­JÚÔ3\x0006`¡|bÖÄNr`UØíèÇ¸îèAF×3¢L\x000cç<cú33FÓå<ouiø®SÃ»v«C4\»I\x0013\x0003\x0019
WM>!BZEè×\x001a¤H\x001fk	\x0015Ü#JM<Æ\x001c¤%o;ñ¾õui0\x0015ñc5`\x0006@naë\x001cç\x0010;¬°áÚ\x0015·­%2\x0011LÞ¡+\x0008=.0¯_~ü´zx È\x0000\x001d¼ÿïÿü¯Õã\x001cKÈpÞ&àE>\x0015ÜRTß }ùêÍñÅ\x0005Å`øû\x0007ß\x001eÀs\x0002»'¤eÖ"îÄ½aF3Kuµ7qÛw°z§@YÁ^ç­ 6¦­,Ä\x000e<{q;`l)Æ~;Á¼q´×¾\x000fÄFßÇ"lQÕÕxûHlá99§¢Ù\x0016ÌhãÖ½,~]\x0017í2ðäÙñ2R,Hý©Ûm-Vs\x000e"n]ÈaÕ\x001b\x001c\x000fÏoV\x000fW÷¾d\x0003».KhÀíÉr¾w>K{'úÉ¯÷ç°y\8¾¹Ùë£&×j²$¥c
\x0004ßîÁ>åÔyÒß\x0003j\x0018 &T¸Î\x0015×\x0013v{c··a³?»\x000ee\x0015iÀÚ8£ØÔ¤üÎÍÔP1QÃ¶J=j/ù\x001bP³jCE=Ð¢M"\x0006Ôvcv÷X¬\x0000µ\x0003PÛ\x0006\x001a4ÇuFI\x0008'nÇ$Ót»\x0007J\x0003ª\x001f úÆ1\x0015§\x0004,þ õ6ðÍ/SSå¨q\x001aÛPY7\x0007Q} -\x000bQ­\x0011T¿]úÚ\x0007¨¹	59V4L5j\x0005p?P«E$ÜÚÝMÚg£j5Øý)i¿5JO
'AÜö°É°ê0bÏfµCÖ¶\x0015¼åþì\x001a÷Wîp\x0006Na5O8¡\x001bXýµme\x0005¬£aVlÅãê°Ý\x001d+XãµmiaK`.¤Å0½q\x001cºË0\x0019\x0001Ú\x000c§iÜ[­â,#0\x0001¤¿·,OæHWq9«\x001dWø±usÍAl\x0000\x001aa:±Ø©;ÍbV7du¬*Q\x0012\x0014±j)á¶ce\x0019Ûc-gMCÖÔÆ\x001aà:Îu½8\x0007XäÄd0rOÜ\x000cªY\x001a°\x001aÕÈjåÔÊ*\x0014	Òünùé1×>¨kÝ\x0003Lw
HN"ºÆ Àvi=ëÐh1V\x000b\x0007×\x0002\x001c1MÑâ·5â\x001bPó\x0010µÑ\x0014P©C-\x001a\x0003Ë\x0006e.\x001fù»»\x0017ôlV;«¶q®¢"W&¸\x0016ð~¥\x001c¯6.3\x0006CIà\-\x0001\x00138û!óÕÁ·W\x000fï\x001eïT6¢äãº\x001c\x0002>NQ*þíÙåù³Ýr\x0004k{}ü\x0000\x0016?6Â¹¢"Ózª¹ u¡Ùê×ÍÆq\x001bc+nvÜÀ\x001cC²âO\x000c9ó¬n[¿7õÊ«7
B5¼\x0006ÉPÒ±Å¨òÝé5\x0012g«àõ~Àë}#¯Å]­\x0018ãy³uI\x001a\x001dáµ|\x001f¸q\x001b[q
ªgpÙ¥Õ
÷\x0005§}a/£³!7Ï¹\x0007)\x001c\x000f\x00041 »V®Û=Ã\x001ap³\x001anVÍ\x0001\x0008v\x0017 F\x001f×ÂÌÓlÛ±Ñ\x0006{\x0003~lÄuIÜx	ã°\x0017Ì\x000bÆÅÇÅ¸pë\x001aL\x0006úÜ¾ÖX*\x001a#Á\x001bX\x000c<\x001d\x000c*o,\x0007Ön0¾ô¹
\x0018f*7kÒ\x0001[vÑxÑÖ#òx5Ày\x000387\x0002{í¸Y\x000e\x0018¬åxN\x0005§ÃvË¦\x0016`¯À¾ÕtðF?è\x0010Ü¡å\x0011NÒ7[§í\x001aÏ\x0016à´\x0001Z\x001dÖª9âáìLPÒ¼Oïg|{J\x0005×6o
8pµ\x0015/'Ó\x0003ïH\x001a^
°ß\x0000nÝO\x0000£Rb?dç\x0006`»}£¬\x0002\x0006cÂëH¯ÇÊß@ï\x001c\x001b\x001d\x0005FJ	HR\T\x0001VôEÞ®Z\x001c\x0004zGìsf\'8"cØçÏat\x0005+Âý@IJØVr\x000biøº
\x000c¾qÔ+\x0002»XÝ¬>®nßOwøÁ­*s=­J,(cSRØo·³êòâøôøÕñëowË3f/o\x00100oÁËx0JBiÃ`Q\x001fE0w\x0016ýÌÅÔké-ÄÄ
.rþN&pË)2«ëEÿDóÎjÎ4äl{íK\x0000ÓuRìÃÎ(Â4¦	\x001b¬M(¬»hòÕÃÁû¿þÇÍtË6X&ÅlAÝ	\x0011Ékäa±t7ç'§»¶\x0015Ò~]:âLj@õFQ\x0016f¶*.RuAÒZ(÷Ïiíf-E>ë=éâóêý´\x0011\x0007hIÊËx8\x0011EÌ×E/Þ\x001e»{nr46ö\x0011S¬Gôó\x001d\x0014â¸_@²R?ë1¥
ÑÐÎÖbøÆQr\x001b\x0016õëÛ¿þ9¹~`¥)B-ZÒ\x0004Ë7ír\x0008ï>)ß¼|}2ÎÒ}}Nú\\x000fjà\x0012½NÏëú³fïEHó
i6)\x001cèËê]R`JÍ;Ê3\Iß?Îz÷\x0013[-\x0017x¡ûB²FÍvÀ¸úVÓùå\x0004®·\x0003\üØý,
/záø~¥reÉÛíÐV\x000bn¯Ä\x0017qoÅÅ\x0002Þ¬­¡D9JôÂû\x000f¶×Ç\x0001¯Í¼^\x0004»´ê6«(\x0005bÌÛÂH-¼q8\x001dbûtÄ\x000cò\x0003#ú ã«F;ÌæMCÞÔÊj"<\x001f­\x000eõ>ÊðÆ\x0002\x0010ópµ"§üzx1\x0003Ú\x000e÷Åj²QGDåì.\x0003Úr Swi±»å^N\x000e^\x001cïî$Bpní¼B87p^Í\x000bÙqQ2PEw>\x0007Sç\üiºè\x0006tÑU\x000eVppÿx¶ý	os»·Ó\x0019pa\x0008\x0017*áP¶D\x0004\x0003ª\x0006rÊMp\x0001çÝn÷ä$Ï\x0017K¥OUt®ó4 ¨ IZ\x0018ñûÏ`C¶XÉJÉÂ\x0016H\x0015ç°sñ\x001bt75£um1¢Aqñ\x001c4¸\x0007\x000eÁi\x00138®òÙ-e\x0012.®o»\x0008\x001f«àrH\x001cÚÏYÒ­á\x000eÎpn¤îl­'ÛlCÙæ\x0019lÉiñÎ"\x001cW¿:tO3Ü2º<¤ËtÆp\x001f" Ü,IZ5"Ü\x0013óás.ÕÎ¹¤$dÀ\x000ccÇ6XI^R7ÇJrgÐÙ!­ßæJàè¸¦Ìfié/Kèü®rÃiWRsÎv/6g¡K#5£3è"Ö.
tMñµAÎ~åðz¤ðv\x0006ÝpQÄêE!Ù\x0017DÇõc.9#tK×«"Õ®
Î¸E:c;É\x0018»U1R¿:IÕ.«Z:°L\x001cç0Ã\x0011ÆÕµMÏ\x000c\x0007í
%+;«\²ÉÆR<­á,7©ìíÅ>\CGè,+.¯8¨¸<\x0010êùîúæ\x0006Wøëäy¦¹7{LÔä_±ãûQ@áò]ï^âó\x0004@î¹ÑAÚ]QlD½\x000c¦çY)*3þ
Û6äuß\x000cDö¹\x001d9:øÀ¦MZ¦ªñîlë:àue\x0008\x0002÷+CªMqCFÌî\x000f\x0018ä1N»c#UÈ:\x000ef2~ld¶ØØR\x0017èJ\x001fcê9Õ©æ¸Ý\x0019ÍUÌÆ>3~lf\x000eb:81¬\x0008&\x0005Ã\x0019!<¡
Ñl×W\x0019Ú0²oFÖJ\x0017¥ö\x001d\x000e=3³-\x0012¢ßxmBÎCä¼\x0000\x0019«bMû\x0018t\x0002Ä)BÞî\x0002TI\x000c´´Åõl°Pü:\x0002ðìêöî¯ÿïótà·6ÔÓì\x0002\x0015YI "m½W	\x0000<;y}öòí\x0004aßíª'\x000c±#ú\x0001m§è¶Ýió\x0000WC@ô\x0000§Ánðæúêþþê\x0017÷w\x0000<éUÑ²±,_I¥¦æ\x0008\x001a|oL8ñÍËós8ÏÏ{\x001cØ\x0001°	K=­&\x0014¸pFêt'¢\x0005æ{bCæØÎì={ðo\x0015óA'°Ùl;9íº§02ãÇVf\x0014Ù*×dÌ\x0003b\x0017¶·Z\x000b³Þ­B_Åìì`n8Û>7"XâÝîÓÉ\x0003@¡\x001cðBa\x0005pX{2\x00118(¿\x0000ØtRË!/\x00026â$²Ln)³Î\x001bùÚða¾6¹²_ÝÝ~^}¸<$¼Î\÷¯rôì­\x000bVIÈð	\x00115ðéñÁ«³×o_¼À
CÜÐë\x0003×Å\x0001db@°Vd+ÍM9\x0003\x0017®òÃ\x0006|cã¢\x0001´ÏW7«÷
ÞR\x0018=4.*k8¨áw×Ã\x0010ëóãÓãow«*0©\x00196Ò¬KgbÔéQbÜ`b¶zwºM\x0005ª\x001b ºFÔTL°7¤9ä1Í"(æGÎÙiÀ8á\x0006Y4Ój
n\x0011¨åÀÛ±#b.j\x001aÌÓÔ8OM)Û¥M+v¹vÊÉÛ\x000fcÂµÓ¨¶ÜÝ{Å{`o\x0008$Ü=;ey%î\x001d6\x0012ëYsÀh÷®<Ëçg`Êî¶\x0014íFê\x001aR\x0006ÕB©Bj¬-±×Üu!n;°U¹Ö{AÌd\x001a0mðr£5ü\x0013\x0006<Wí\x0003å¶&Í|J­ÉÐúÈ\x000frnÝ]?à¯oî¯oßÍÈÄÈ\x001c\x001cÁ\x0014ÛîÍ\x001béåhb»Îlyvöò\x0002}sþòõó­ ó\x0000:/¦!î¤\x000eG«át\x0018¥+}\x001a+2¬îWp\x0002ôF\x0005g%µöHð\x0004&dÈHÈÚÏÿ\x0004%¹õR\x001býÑPÈ\x001a6¯w°{Mß\x001et>Å\x000cÈJ·Úeé\x0016vf`­ë\x0002÷®Ý·G\x001aÐØkv\x001bðc\x000fôÙ_ÿ|÷ó\x001c½4oKB3ö\x0005èzÁËÍ,jµ-é²\x0006}v\x0002ÿ`·f
%£µW>Qå~&\x001e\x0006¹Æé.±!&Ç\x00006\x0016jODå×¹xt\x0018\îÎndÐµd'FÓ\x0002jqrrç¼ÀÕDAä0¼»Ò\x000f(}\x0013e|CÓÓKS-tà2hÜÖF©\x0005Õ.ôAñc\x000b©\x000b<Ú±¹½\x000b\x0004ôâíÙ ?\x001aÓe!=+Ê\x0018°ê\x001cZ^±×>\x001b\x001dEhT³G+lû
vd
ÀôZ¯Àès%YÐ%û\x001f\x0015µä«§$bÖÉo[{£dÊò$\ûâq\x0012nøâáÂtpzwûa:a	[ë\x0014-	\x0015²\x0011\x0019QCâ÷«Æ\x001aÁ|÷\x0012®L\x0007§g¯_ìNYbàuì
n\x0007îº)Ø\x0015ØÌ\x0005+É¤Ýé¶óUQ[ï÷ªP\x0003#åêáàù_ÿ\x000b¹þ¤u¥//:´sîdE\x0016ö¬ÈÉ\x0005XSøíÿØ¹|\x0014\x001còk\x0000¥
Í)¼DSÆÚÁ5
`ØâDâØÙ ÍÒ\x0013R½45¸F<|¾ï-\x001cE÷.\ø\x000c\x000b'\x0003wf=x}7y$RzÖâÂÛRiáQçV\x0012·Ý¾Üõàõ\x0019\x001eB%¿!ºðCüñ·ëð3ñÁ\x001cÑ¥èÅêúö3U²S"µå«SèÈîï\x001eÿøææêáãOW\x000f\x001e&vôå`À¼ YèQÞkPÙõ[R]þÇ7§'\x0017ß\x001c¾9¹ Ö¢\x0017Ç/_¿¥ÂöoOÖ}ò\x001bæ½»O\x001fWxa\x0011ºa\x0006ýñý»Çë«ûùÔÊ\x0015\x000ePãÝ3\x00115Øö©M¿ù\x0006u?³þøüÅÙåÅËóÝì¿þüËÝ
Ï\x0005\x0001§w¯ýã\x00156l çWÔOk\x001e8ê0Jf\x000e°g\x001eFÜà½[n\x0001[__Ih\x0003üôìíK\x0000u\x0002\x0003\x000e\x001bëùÉñéNêÕOÖ|ý£7CNa¤_¬þ=Æ°¡ë\x0012éÎ\x0001+(ìæQq^\x0017Ôa\x0019Õ&*íãïwªúz·º!>ã\x0017\x0002\x001e?þxuÿáêþújþ\0p®\x0007ÂDûî Ø-³ä\x001f\x0005mûº<OP\x001e_>;9qrþ\x0012\x000b,v,·5,ì*GøÕ
K¢\x0001©\x000cjTÝrË¥\x0019\x0006Õì^msi¿\EóéKo±Wÿîúv>hÆÆ³\x00054äÒ æ\x0010\x000b@,OT«ÌÈD¥·þüåë\x0011ÊO×æÁsá
« æ¿_ý¼OP¶Óð>n³2»¾\x0004M.¹1Ê?ù·ã\x0011HÿxóõcÚ<¿ûZ\x0003ið#£ÁP¢­WØ¬lUÞªñet~ö1D<x¯¿\x000bþÍÍêØÇ¯V×0Mç/©Tì\x0011\SÒF\x0013»L\x0017yÎv\x000fëÓãçb2¿ìåîc¡c7}vó\x0016»í³Ûÿ3Ø9(ËºøAâGGÇ_®à1=ì\x0019óÙQE\\x0019lD+'\x001b^¶x)\x000e¢o\x001bìÇß¼¾\x0014xØ9zèìøãWÿauON\x0000\x001fnP\x0015ü|õéóê\x0003y\x0006¿[qk0Çvï o¯\x001eúæýÿuöõ
aQÂÍµh4\x0018¸½àÁ!\x0011}é¼ëIÞ\x0015×;÷ñ%ÿÒõÕ{©¯º{\É\x000fóúäòoß|{pö£èùñ·Ç/ÈøÝñÎ>bþ|û\x000b\x0018\x0013ä-ÿ\x001eÜÿ¼úø®\x0013s~"°ÌEUßÂ¤Á\x0003øðT$÷±×*â+>-I\x00160`#ü'¨±ûê
]0&ÁÑÕmí\x0012ð(\x0012Vc³)àN\x000b8¥Gì\x001d\x000cAóøjò¹\x000f¶ÕÑ£IàÁ\ELAµzàwï¾ýíW\x000côã©f\x0006ñ¥\x0007\x001f°äïa\x000e7
ZsKG\x0012µ\x0011ÀhCÆ)q?/íbG°/\x000eÞàUtGyªÿáþåýíÀÐ\x001bÚþ«û?ç!c\x000fo_ÃQÇ¡ÎÞÊ\x001cÁ¬éb¿syhø\x001f?ÉZóG:¨vhì<È3\x001bî§9\x0017jtæÓ&ã¿\x001a\x0019Ñ£\x001aÛ\x0014ÓUÚ*Lªà±Ö¥r	c|¸höLíÐíLæ	b8Éàv\x0005ÚÊ~\x001eQSrOÐ«Û\x000fæÏ_)æÂÐsúì\x001eþ`q©Mo Ø<\x0004Ö\x0006WC¶\x001cöñpÉJib\x0003é9)Ã?ØÎæ¸~÷)ÿRn²@ì\x0003ýâñêÏûÕãû»ÛY£\x001dC\x0012Å|­ÁDArÏµw`\x0007cgÃuáòäûóãËoÏ^ï\x001aó5=¦Îk³\x0010?âiE|úI\x0010ßåd\x0005\x001fßê¿\x0006?à²\x0014_:PÑè\x0007Ëø*\x000bþäÁÓÿÔ6Þ_ÄoP=\x0015ÓN\x0019ß0>õ[øà£Ú/\x001eý"\x0002ø!®'Éc°Înøù÷;ûçWÎ¡\x001c§ðçÁ£Éyáj\x0015\x000cÅféÖ­2\x0012b&Çd\¿<q¬ÉZôHéBÝj
z´o\x001bÑa'óv\x0011z²¬WfaÆËn	\x001b½:Åóþ\x0015è`8û¼lÔ\x0015¥#Ð¨[\x0014@.ó¥e ºwÿ\x0012t´ð«\x001d\x001dk2\x0006µ¨3]Ègmþ%àRÕ"pl0Èk\x0014Û=ñ'éX.¸GôÏø©\x0013`¼7üÕÕ_¯ngÍd+#J
2Ímö9cj¥W'ßÿãäõß'©1%Ò,ÁÐ\x0004Øê0á¶Ñf\x0019îX³±ÌÅÆÈ¸\x000b°ÑÊýPw£\x001d³\x001cCSæ&h\x0018g»h¬\x0015\x0015jÐ´x£#èà}7µk¶¹Øx¨¹°\x0000;tvzñÌ\x0015ênÿÎ¶fÿKýÔî]G­(êHÇ\x000e-MÂö¥\x001f\x0008îÝ¶f\x001f1¬°d°QÒ3w§¥¶ÍÝikÌÃqìÛl>|¡X/ú<ÂÆÔ~}÷g	LNß?3öU&h*\x000b¤Õ´+=Ä¼Xý5êSé3¿>û\x001eSÈ($|;²w%~\x0002Ìps¹0[Ïó#JÑ¾a¥¤¸ÙÊÅ3£¤ubf1`£Û7±Æ\x0006í\x0016
3ò:å"
\x0014^ñµÅÿ\x0005ÄxÇÜÜï*çr\x0005\x001a[]8ÌwéMÞ\x0013ô/¿?~}$»	K·Ò`·;xVÓ»gùR2Ö±BÄð%]Ë\x0012J\x0015~b£©Æ¡ßó®¼A#êù¿íò®|þåúúË§\x001d9\x000eo1ÇêñfæàÃa^fÍXnÃ«R«3Ä9þ\x0016³¯.OwÚ~\x001d6¾Q\x0017q\x0017¥\x0003t*ÃUÍò\x000e¨Ä\x001e3~Â«\Áýëçw¦
JÔá\x0017VØüõÏ\x0012¼Â.\x001fn®\x001fæ9á\x0002ÜµØ$\x0019'>Ýçu0bø©Ó\x001dËnNJ\x0004ëàäÅéË\x001dåM}î\x000cË\x0013¿\x0016pÛnûÆ´ÖXwçdÀ±dïÜ\x001aÓ¨èÑ\x000eîñ°\x0011ðWrO0|V0éö
n>}Ìé\x000bÕ`&]«QP!AéXùðé³à¦§9F:Kã\x0007é\x001cÅ;\x001esT|h"cí>Ã\x001a\x0011Tw}-/ÞïLëýLØ/ï(÷ÄÚ~¦fVÉ4p`\x0016\ì½ìtjÿoú0Þ{­?v¢\x0010\x0013LÄ´\x001bú¸c;þLêß{ÂZÜÜ\x0013~jý|äîn\x0006kÊËí)ùTªÃ<V\x0006ü¤?ßÿn®~ýAñ¥0\x0017jÝâow÷W\x000f¯ÿú\x001f÷]\x0002ÁÝý»9\x001bU	s\x0004ÊÂ\x0016\x0006¤\x000cÿ
ï\x0007Îc|¹û\x001bwý\x000c;;?¹xûòä¼K%8;ßQ¤áP×ïìOTþMt¯E<¥\x0011Ð»A¾Y>²(e¼Ö\x0004Ïvt\x0008:gÒ¸©{V÷\x0016¾;Æ·ßâÆÌLz´s\x0007Ëª\x0016Î
	¼³\x0008¹ÇôÔ\x0005vDì¸\x0008;¡a¢bë\x0014»ç=5pãE\x001eíÜÖsÒb7\x001eUÎk\x001fµx$ÝdÜ \x001bw\x001d\x001d\x0016·\x000e¨\x0014®IÌ½\x0019 CaßÜ\x0006}ôhæ\x000e)³¢µµ`H³¯Éë;¦)¿^\x00037\x0006!èÑÎMÆl\x0017èp%þîêü\x001faÊÚÀ^=z´s\x0007)bÄ³£)KT2©=·ùá·+éÞGÞ¸o=¿Y}ârQò0GÛswó×?ïn×'ãÉç\x0011
Ê\x0014iþC,¸+~¦HM~KÎÚ«7g§'g¯\x0007\x0017ç§ÇoF2ÇûO]­f"ÚÒ\x0017\x0015\x0011Ñ1\x0008W*ÃFJ\x0017"ZøImhC¤\x0004"BÙj\x0018;D\x00124Ü\x000bâSþ¹&Q<\x0005\x0011}iâIV\x0010¨[/DÄ¤ÍÄ¹ùè¨Z\x0019þtìÞsÐûO\x0005§æ\x0011bj\x001e¶GBtdñ º«\x0002>,\x0019Ä\x000f_¯þ\x001dë½qºØ¾ðíÃÁ3°-o&ø<\x001eM´T\à:ºClÛkJ)\x000bÜÜ6_²\x0008ó]\x001c<\x0003Ëñt\x0006\x001bi®fÃ\x0016JÆ\x000e\x0013K\x000fËÐCÐ\x000bÉ°°+õÕõçåPÈ%]cB³<j!Åhè G-Zâ½Ïk\x001bJÉ& åQ#îÓËÐÅ´<+Ùt\x0011øÅ\x0000çZ);A¶Ì!ûÅl²<éYËæåXÃ\x0010aÔÂFhZ\x0019½t\x001d\x0018\x0007yyV²)CÞ{`Ãq-Ó­8\x0001.¥óÍx\\x0005åY»xº]#\x001cl&iÌ\x000c§´Ã\x0005\x000b
p¸\x001a<Áaú(ù¢
\x0014µé:
.!óDæ«ÉàÆË°ae8Snï\x0000'U\x000bØ\x0002®\x0005zÖ²\x0005
%\x0002\x001bjASY\x0002²ñ¹ªÙ<´\x001aà2
\®\x001f8î±'p|bÉ&¢±±ìR¸vCyVÂEKzÙ\x0008\x0017T0Fm{%pQzÃ,K\x0004W}4¸Tô5	.Ê©å\×ìÒ×j#v¥*Ï:8­"yUèx,GâÌX<µôÒ\x0003*Cl¦
,\x0018\x001a-d³®èÌ`@ÞjN).³4p¶zà\x0014×ò\x0012¦3\x000cátô\x0002\x0017¿UôÄg%¡l\x0002gJO
\x001d\x0018\x0006néÙÒ\cê\x0007Î%6ÍcÄÎTØ)\x0003g\x001462X\x000cg\x0008®~Ê¹¢Ip¶r%¹
ØÂòå<±ùz6kÙú\x0011LLj=\x000fl¦è¬\x0000\Zº\x0001Ûáàò¬dÓÒ]-«Ò»\x0000'\f6mÕR\x001bÓfq¹aÆiê\x0001lIùõb`ÏÑÎ-\x001f8O\x0003ç\x001b\x0006.ípè>³\x0002g\x0019.,Ýâ\x001cêÒ\x001dg\x0015[Ì¥\x0019 eëKßb\x0003Ó1	ÍçÖÝ»ßC´äÈ\x000bt§éÐÐwÿ\x00023\x0013#¸G\x0006\¡\x00017`¸\x0001Ò[
)å\x001d7è³óç\x0018vAçPºËõúêÍ¦ËJ¢\x0007 Ó1\x0016Ý9liSv9Às;,
<¼]\x001eÑ£\x001aOÃ\x000b-WBzsl\x00124EdôLzz½Váa*z¶-x^Î\x0008§aP\x0007jÀó<x1¹§WE\x0005\x001dv:
½\x001eÙ\x0015t¹¨a8\[ítØËÂ\x0000<\x001f>^kðð|\x0008½C¢\x0002\x000f$=ãiôlÓà¥Hxg^À\x001cã\x0010\x001b-lßêQ\x000eUE,\x000f^Ét\x0007:Øá\x0017ã¡yCz<\x001dÊYáÐù\x001aR¡3^^­ÉO{¿*è"^Ì£m¢ó¥Ò\x001eñ`ÏÓ<ó"Kr¤ÓÓ××\x001a<tjÐ£\x001e§\x001bâ)S$Á\x000cØÖ¥û\x0001Þ~6c\x0014-x\x0016ñZv\x0015
%dô2åÅàèånÝv²Kððå¦\x001b\x001c\x0005$\x001cæ+$¶ï"ö¬Ñ³÷ä\x001e\x0004zTãa\x0001Vq89¼^Øg2÷ÜÓv{\x0015^@¼¦}\x0005®Ö)Ñ¾Ä$`ð¼L=¿ÃéTC\x0011Xz4¬@\x001dWèÝzòòÐÊÈ2xa¸\x0002\x000fïÅGIµ¬\x000c«Â¡g:ÃNØå<B\x0017\x0016o+[>ÿ
:,ñÖ\x0005/\x0014å<Äó`ãâó\x0016ïÆGô¨Ç]¯ÄrPÚï>Ñ$SÏî°ákðpöÒ£\x001a\x000fÌw\x0012v#<G2YÇ3·ãÞX)Oô¨Ç\x0003û\x0017\x0006¬`^\x0018.:z[\x0001Ù\x0006:4µéQOg=»ÇCñ%#º\x001cdê9³ØÊØ/Ç¦Áóz\x0013\x00153ê
\x0018oùÑcÓÔs\x000ca\x0003t¾à© /×ï\x0008 LãýôY½·¿÷¤×wÛç7w'®¶Ú%veôº\x0017\x0013\x001ekº\x0013
\x0013ûv:z½\x0001¦QÂ\x001edü×HÆ\x0006\x0015\x001b
Èè\x0000ZHY(C'Ï,2Oªe\x000e³^
o$@V\x0004d"ÖòíôñÌ#+B\x0006åY\x0006\x0013©L4Mó\x000eK1èRM\x0001ËÕítTÌ\x0005Ë6\x000côÏ\x0001ó¬\x0012¬,Ð\x0005uHq\x0017É;=3¹"¦\x0005gå\x0015õ.äB­áÈ#VÊ6"jKìÍEÃ±<ëÐÇ\x00154\x0019á©¼ZÞíXF£fªGÍ\x0015×&¢Ávi?ó>í6úR/¶\x000cê·6\þsÐl¤Î¶\x0006&ÆÎ:¯ð
ÛögþéR*\x0019ñÒß«¥xäÜíq4å-)fáÁ\x0008²°G@æ}Ãnú\x0011¥^âòàÕÙåéË×sØÐëÙBàL&ìÕyXbÕ.rgVdÛj6°¡NPÔõl1s88Ãäô\x0003Ø\x000b\x0006d>¤Ål\x0018kÁ¯j6I)Á\x000f[haÓäm@ÃRCüªFå.jEZ\x0019Ñø7qñ¨iJãÔ
l!Sj\x0010\x001d¡³\x000f\R~\x0008GèæE«\x0001\x000e=Kô¨CqZÍpK.F\x001e¸¤ôâ¥ 1@BZ6lL)l©H¼\x001a'\x0002\x0008g\x0017³¡-JZ6ce\x000fÁJ]\x001aÍE±Øò¦/½\x0001\x000eÿ
zT\x000fâ8\x0004\x001e\x0012¤ïF\x0003·^\x000eÎ5Â}úÍüöë¾J\x0014*{\x0003Î\x0007¯V÷\x000fðk0\x0013Ñ/,ç\x0008?ìvÙJ,Xâ­VmÞì/	
ÿ\x0013Çç\x0017å?1
(;p=`\x000eìê\x00029?B)	V«­cµ	P¶áj@
«¡ì(\x0000XX(£\x000b
+³\x000fÀu!e=¡³\x000bFF-YMÊgÓ%#l^h\x0008É¦#®\x0010\x0005x\x0016ºR=BùÌFòLPªl\x000fdB\x0006Â@%î4¾t4@BßeÂl9è\x0008\x001d'¸\x0016Â$\x0001 X^%)w¹0~Á+\x000e¿ß\}þ@\x0013TY²\x0004¬¿]Ý¼»}?uuÅ:QZÆ(¾@Öh±W\x0007\x001b¢Ý\x0002ð·sØ\x0012¿Ým ¯ùhº¯8¯±NéL|E·
øvx*ñ0rÒó3ÍÇ3\x0012ÌN\x0018³Ó­d¾È\x001a§w§×Õðal"ú\x0006>å8¦ýIè\x001eDÐÙ·²\x001aºt±åå\x001a>ä(Û.x1úøsnGÄ³/áºH-CÁ}QÖ)2ÿdZÉËf§+ \x0002\x000f#í©\x0017n¯x¹<4|½ÿðr¼^·Ãû_Çw)zT\x000f_*\x001d|pòab\x0000_!õÂ·óâ]:ô¨ÆZ_ÒÖ\x000eùòm%Û\x000e\x001bN6ãý©¾>|&ó\x0014²ô03ë\x0005°Ý=>\x000e#|F\x001b²JÿæÞ&¹\x001cI×Þ
7peøÿ1(%SÅ6TQbZgOdÄT²"\x0014©JÕ¨§w	=ýF]£o\x0011¹^É;Üq\x0002Ás\x00028§­8¸ç¦Ô]ÙO!\x0000»ÃýõÄç´Æ<È*RºSÁ\x00149¾	îô\x001c\x00067,\x0000dTZ
("½ÀC\x0013õc%@Éjþîh!,Â=\x001dK\x0018©\x0014\x0015ÈÉ\x00074\x000bU´óÍDM\x00035¾P	Ì1"a wD\x0018\x0002\x0013ÆÝ\x0010BÛsmd\x0016\x0013ÊB\x0018\x0014Õ\x0006h©ÖXE7ßNÑB\x0008µ7øÓµù\x0016qÑ>\x000b¼¼\x000bç¢Mx 2ouç9¦;ØÁ()KÇ$w@\x0001à|yj\x000b!(áO;¡Aõ^$t^£Lä\x0004\x0007LYØÅ\x001ajR]ÇÄx\x001c\x00002ä\x0019\@ÈU´QÌß%-ðì c×WÖú\x0019Y\x001aU²	0Ø­õ£h³\x000fÐb5m' ¥¬"U\x0003!ÛB9ß5\x0010\x001a(g6"t\x0011Zj¤×c\x001chm¡ï*k#|w\x0019/: ¥¼Gäns2 \x0019R]A¾Ïï; ½Åó\x0000i\x0005­¤\x0015Ò±ÉÑóÍ\!oþöþ»:VJ?òéë\x000fZkÒ\x0011Æ'\x0019øç\x0005\x000cQRC¨Cõâéã\x0017\x000bÀ`Sï»QÃ\x00020a"¹0i\x0000{
Md±¡Ä\x0006"\x0008Û²ÁuéFý KØÒÌ5z0Jå\x0019Õh¹v,!°\x0018íóçOþ=>+ðcà²\x001cY"â:Ï
^\x001bÈÙü²\x0010<tüP\x001cgèLèüâ?å@åc\x0018\x0019¼
<\x0018øifÔ¢\x0004÷Ì\x0010\x001bÛÇÍHÍh\x001aN\x0000þ4¢¥ÓIE*É3àôñ4oÊuigÂMüifK^Z¹}\x0014¼Qù\x0011¸}a{8lFÂcÚ\x0008ç³ü\x0003zÍ±<z¸h\x0018n&­Ö\x0002\x0007´øÓ
\x0017uqí*,OG½©G\x0005\x001dpÐUãLÇg
T\x00021¥|}©\x001dì9¨RÁæÔV\x000eªú\x001c\x000cùÕaµz¥:àà@¸\x0003|÷Ü¬
bOÏ$¥Òb9\x0010æQëE\x0007\x001cèr»Ð\x0001g8\x0015\x0004Íª\H@ýøÉ·{Ô9ØÁ\x0006S3]\x0001SÌøU\x0015eùV!®\x0018çHÛá ·¬}»	2b=9>_V-}Ô\x0002×\x0001§±¶\x0003ÎRþ\x0011^°\x0002×\x0012\x001d§\x001fUI5³\x0019PhÄækÕ\x0014Cb#'÷\x0002
jãðÈ\x001fi³pÝÛ;ß\x0019ò\x000bòÂ*\|T:ÛÎ\x0006eøÓÌ¦Qh%A\x000eIº\x001fÈY\x0012\x001aÌ:àpÖIÇs\\x001fpv%ÁÁH\x0016òäTïqøøñJ0øb

YÅ°g·É\x0003Þ°
JSñbMËÅe\x000eG¡\x000blb}l9;M>ðín"\x000fµNH
Ò&äÑõÊFèÙ@:ëf\x001a\x0007[è\x0014ôªªºau\x0019]Ìí\x0001°vPOpÔà\x0003\x0017ëlÔÚ\x0000\x0007C¥êãÖ²dKJ­C¿ëü3Õ&8ñ«ýæ?\x000fEöº½Êh¯.îî7EÒ¨AJ7\x0016Fÿò¡\x0003\x0001£ûéô(£½:8{».\x001e Á\x000bKhG\x000b\x0014=JKÑ¹1ô¶\x000cjµv[4sÇá§ÍQï,\\x0014$&c\x001ciòEÔ\x0010Ü­\x000cþl_·à3[:¨¹{ÛY+IF.ÆqÕe\x0007[©hhd\x000bµ¬S0Ö+ËµP%¹ÌEý[²E\x001cQ\x001bÛÙ,\x001528ð15­c47>¥ÑÔ÷_ÿþ+¸·ÀMÅaï\x0012Y»äÑ£á0ihÄhSRØ9;>Wä»AÓ®àá{/þ´ãiê`L»/òÕ¥4U-×ÕG/å\x0003\x0001éý0.y_Æ')Ú\x0007Á6¶%ÊP\x001dÐ\x0010½nÍ\x0017!\x0007?Í|ZSjØÆ´$i Ò¦Ë|ÆÛ5Uù\x000bù¤·üÛ
\x0008ÂË´)åÃ!`YEé¶_@ûS\x001e5¨,\x00024ô=-\x000e\!ç)RarúOÍ?6\x0000b\x00061§\x0010[\x0001¡ñØÑ'\x000e¥^/P5Cò
Ö5^,\x0006t(·íd; )ÑÙÄ¤ë\x0012\x0000.Ew\x0000g\x001aàÛø<^j¾ã ¤/<à£}øÂÝ|¿\x0007÷ÍþcQÒGà\x000c\x001e$RH±ID(~÷\x001e\x0006pYçQærì\x000c`P\x0001o\x0011) XÓê¶¢\x001b[ÛF,ëX
Ê[cï\x0001+ù\x0004T \x001a\x001f=µbñP&,jí\x0001,C~:ßÿiìn63AÛW­L\x000eEQüIÂôey©ì#Ù¬f,P\x00070X^>Ëµ^B[i¤g¨q\x0001w+\x0004ýoüi¡yÚ\x000f+esh\x000bßr»ãS\x000fþ4q¥åh¿À¢"Pû;jK.PÜÁ&®è©ÇC}#ýn\x0015¹\x001cöp¹_1\x001f!0
\x0010:0}~yñðy\x0003\x001aHÃ \x000fN\x000f4®îëT¸×æÞÜ\x000e\x000fÎ_-ÒÕ]\x0006ç¹>Ì\x000bEj6®¼lÉya±
pêË·ow\x0011ã?ÈÕÀÏÁÍ«ËË½æ^ç \x0003Ð:
G\x0011\x001f==ª\x0006ëÆª\x0007'/\x000eON\x000e÷\x00167=¯Kúf\x000b`\x001d)CÜ^\x001c\x0003´Ò\x0011°\x001eç¶\x0001ÆþYøÙ\x0002\x0018´\x001f|\x0006¶ö\x0019ñ*G:\x0006V\x000fÐ\x0016¼(;?[ðÐGî~\x000fÚSK&ýR÷;LÀÙ\x001d0¼
àO?pTLTúôJ¤î4\x0017Ì8µ×Î{÷Küøñ\x001e{àÈ/ó:¹}w{¯.¯/ï7XQ«èÛÃ+âF\x0008ÉW´²îàõ\x001dî½:<>|»\x0000
Þô\;ZtT\x00073×sU+%üB=rL}û.ÿøöñÝ`ýñÕåÃÞ\x000fW÷{×Ó\x001aQw.YÔ\x001cYZOm`2ùâ#ët|tx¾÷ÃÑÛ½ãAjãâîÃåülòüøG¼¾Eç\x0014Þ¦Òÿ{ñëåg\x0018çS^á\x0017××·Ð«¦efñÃåõõ\x0005 \x0006ð\x0018²§bS#ñè<³	X\x0006êñ³P_Aÿ"$}qx||þñðÕÑ	MQzQ& \x001e\x001c\x001f§ÿ\x001aS\x00039ÔÜdÚO
ê\x001a\x0016Vfjm($ÎD·kj	\x000fÄøÓ-D.×LØ ¤3¶*=zçk½\x001a¦´Õb£\x000ey¸-T¢Ö¥]\x001b\x0008î\x0018»Ô¶÷bËÈ]	Ûù¬y\x0007-¸\x0003>ÀKý±Aj	ú±AH0Ë\x001d@\x0011 ¾á%l!¸wÔ]aëÏæ·kw²v\x0005ý\x0000â\x0007_éå!±]ì
½Â\x00032É Øt³9Ö(ÊýãÁ¿mû\x001c\x0014\x0011ÞÐÃËyÂë9¤\x0006×Cù-°-v>\x0000¶%©UëMå}\x001dòÆ]có\x0008Nì\x0014leu$8Y\x0010°£,\x001bÄüo`KhöÆ^n(iÍ»Ä«ß\x001fàõ
I9ñ~wÜ¿¨«/\x001a\x0015
hØn} ïn¯¾þùÏËµvÏ9÷,äJ0\x0010RÊvÏ\x000bÏmÈ
{ `RÕåüA<;=zs8=¢ªÌ©¯\x000eH¯H++Aæ²	¤>ø\x0004	x7ì\x0008õ,eÀq@@.>eÒ\x0003
\x0005?v\x00043Qz!©£\x0007f°~
!Yz\x0019Ò,»¢\x0004\x0005f×Ki2\x000b!%§¦¬à6Ö|þúðqòÇ»ËïwW\x001b KÄ\x0010¡ØYÐ®Lþz) <;üùìh\x0001$L\x0018{eË Yá0\x0014å*är{MÙ»älm;dÙ\x001d\x0010 ö,m)$Û \x0010ôÙ\x0011#\x0004Æ¶Ñç)ÈH"¥X\x000eÊ6(ì
\x0011ÞV\\x0017"\x000c\x001e¤
©¨\x0016\x000fN3h7õ_>IÿE[\x000efrÄÉÊûûõ>Åb¹W*
(Êóùc@\x0006Hã\x000cõ·|ûv\x0001%tV÷Q\x001aV^\x0001µfM¶\x0008\x001bOÍbH,ÃÐ]NSEA:Ü*w¸&Ìè\x0014\x001fî7ÎbJf2öùQÂ\x0008¬\x0008B@Ú!¥\x0012l'\x0015J\x0013í
\x0013êºÇ7ã2L¨Ò§\x0003.I\x0014\x000b\x000f¹ÌVm¾¾\x0017SNí¢\x000c09,8ÂÔ\x001c]C\x0003b±z£!Z	\x0011íZÌh©º5}só¡AÍo.wwÊQ}¢ë\x0000\x0005É£v`Ìv\x001eæ0­/q£Å\	\x0002êaìÿ.ÃÌÛ3f¤LO\x0007+²9rÛîÍïö{ü"Ð\x001c¡\x001eÔ\x0018óáêâf=¤UåES »Ù­z\x0004ÄÿÔû5AýËó£Í4y8Y\x0004i±Ô\x001a!³´\x0007Br§n\x0010ù\x000bm\x0001yùùæ·ï\x000fÃ'Ù\x0002	QßûË»ûõ1$\x0014GP*JAt×¸Sì¥6
\x001a\x001c\x0007ÿ¶)N\x001d\x001f½\x001d\x0007(?ÒéiS&Loð\x001eBLj6ÑFk³=¦úÕýñEMÙÌ½7@_Ë\x0008.ºà4ËI}kC \x000e\x0000í=ìÎÿªÉXü
äÑ7Ñ­Æ·àù¨9Ëa¢Ì3A¹NÌj'xÊaã\x001añ´ÈRXP¢S9åå)¢ÕÎådF/Þ
÷î740O¶^¼
ùZ\x0003%Ï$\x0017Ã³¼r!²«\x001b¢1kÏq"M\x0019®¸ Q<Ú6.K#n£\x000bú'.¾C;àZi´ñ\x0018Ùé\x0014\x0002óäÝ\x0004¢×	ö·Ë;å¡7WAø§L\x0005öö×«Ûõ;M¥­\x001f`%è­fw;E®4GKÐ\x0012n4þwMò½ýËÑéùìf\x001b0j\x001c(ÛÎ\x001bÁ\x0011\x0017Gd{\x0007®×Î 5ÜZfH"¶,¿±1r½
§\x001anGx©Üï×wSaK\x0002\x0004\x0007äázý\x0005lJ¤s t~ÔÚQ\x0018\x001dq\x001böáÛ£ããÃóãã$ÙB@%P\x001e\x0003\x0000á3\x0013 Ò|PlÞ:»\x0000J\x0000Û\x000e¨h\x0014NZAkÉ\x0000Ðê²LÌRÀqÌ·\x001009Õ¤h­æ7©(\x0015b»Á\x0011\\x000e8Îæ,_A\x0007ifÏ+HasÀ¹\x0015;\x0001\x001cçr® =¡jË'\x0016\x001cr¥ß\x0015 \x00061fÀäà\x001b\x0012ÞÆ{ZAÁ×oV\x001bÞ
 L´¯ }bh	q\x00009\x0019ï±Ge7¤]Þ
\x0018IM\x0006J(Q°$¹ûÓGµÝ\x0016üzuá~\x000f\x0003\x0003_aÿõõÅ\x0007|½þÿü¯ÃO×W_7DðÐØ\x001d\x0019©%§C¤a3£A"ôqÌùúøà\x0005>Ê\x001eï\x001d¾<>z3w\x000cør&±/mAÒ~Æ» "¢a>5\x0015ºwðAóq\x000fg\x0007UZËY/YÄÝt*Ön>\x0019~ûôÛÍä÷½ØûñöæþâjS(\x000c\x0001\x0011Ý# \x0018N[ÐPé@
ýô\x0011Y!\x001eìýxzòöàh6\x0016þvýÞ}¾\x001ez\x000bT:\x0006\x001dµù_¼\x0016Ñ;êÊp-+ºI\x0002ë[z-å$"Ua[í«ç³~ë\x0000kÆÚð,	UDÈ+XËxñì´\x0015lÆ\x0003È¸V¼¸ÀÓ£¬\x0017?°w3×\3^)kkÂs<a\x0008T\x0004¹\x0006$zV\x000eðnÚÏj§#\x0003ÝD\x0007ñ¥¤Å\x0013¼x0\¿­ÜÑâ=\x001a³põ¬Â¾pz¥+{ÏqOHaÚEhæØð#[ù\x0012\x0005ÁT¾\x000cx\x001fp\x0003T(í\x0004o%¹Ô§-µ;F\x0018cNþQÅ\x0003Ô;Â\x0003\x000b?xJ	¢\x001d:\x001b\¦ÛÝ\x001e'é4\\x0015i´tt)rçT/+«\x0006¿#³,¡N\x001c\x001añ\x001cO&p¬B\x0006x¬L\x001bf.¶v<¸ÔBó­\x0006á\x0007E\x001aõ üà÷°ddvcù\x0014D	J4
©Ø1f%Ã¾©ãÆ\x0008awcZVÙ¢6>á²RdL\x0017,Ù$¼ÒT¢ü\x000fr÷øÓxsX
øÒ\x001f8\x000b\x0013*ò$;¢®ov
D5\x0008t&÷\x0004#\x001d5\x000béôQ¦ó/Í|ðr¦bëÇ5Pí?.èJ×niuÖleZ¾Ûo7J ^\x0004¼Z5üâánC}\x001fL÷£9]\x0002l4FEVñ<¸\x0014}ÀûÑñê_ö\x0018\x0011ä¯\x000fÎÏfú
â@Ý­	ÑæÒ\x000fÌSgDH3C\x0013!=yì\x0010_Ûk)Æ%0[\x0011aÌs;\x0012¢¡z\x001f
~ý×ÆþíîÃ;ncp¼ÍqïåíÃÅZB­£iØÞÀÕ3\x0010\x001e ÖV(CL§8ÿ{&àö^\x001flF\x0003qþüÛ\x0016ó\x000eLh)ÄÐ(³!\x0002öém\x0016qî\x000eþ¶ y¹*Dy\x0006UB£*Mè"½d¿}ü]}p|ÐÝ
ñîñÅÃ?6>¢D×n\x0000lù|y\x000b\x0014Xàq<ø·MA¦÷øàü?Ö¼¤\x000fP!\x001fzP%¾h\x0001©Ïò`\x0004\x0005	 êô\x001fu»%\x001d\x0005pËIµsôÉÓ¢ZªÌu\x0008:\x00191½[T8ÉÕi^\x001a²©IlQÒ°À
óY2*¶ï\x0012\x0015ná
³\x001c\x0015»\x001c|\x0014ì!zeé©Ix¼ev½m²:îËw@à@9Ê<í\x0008wcÅ³¨wÌ'¹víV%
+õyZ\x0007A}FZí\x0018\x0015Zßð§\x0019UA\x0001Uörcò9\x0008\x000b´DÏo¨
Ë U×\x000eHñLÈU\x000cP\x0019ks0}êÕ8 {¬Ðû¡LÏ\x000eH±ß3ò<déòG\FÝ-©B*üi'u6w}Ã¸ã(Ì)HvÕî\x0016õ·¹\x001c5%z\x0018¹m\x0007H¥eØ©\x001d£B§\x0015þ´£jª\x0005ÖòDn¡KXws¬¾øþË;\x0001²\x0015Px#9×·7÷W\x001b h2D\x00101¥ú\x0016ÖX
ÝÆãËò/
^Ã¼Å£¹\x0017¢\x0015#xÛù·Q»¬®
Þ'ùÈ.\x0005\x0010}®ÿÚ	"¨åß6D¥²®º\x000fÚp"((êJ¢\x0015Ý	¢Ç/íÛ¿´
ôÆá\x0003Ì²ÄHRÜRAÉ®\x0018#f4¢id4ÞÒ[\x0016Ì¸E×\x0004îxGf\x0013\x0002:¿+Æ Q¡SVF£¨e\x0008E¨jÒS7(Víj7&?\x0001\x001bÒ\x000f\x000cdsa·ÆÑÎ¥a8&zg\x0006*7ð·m3Â«\x0007\x0011:Á1RâÞèü®6£Æq)ù·ÑSý·i\x0010 ÉÄEèß\x0019 AÀÖÓ\x0002c«]¤ÏìÙ{OW\x000cëcZ¿»­\x0008rù·Ñzª0IªäÙ¬(;3Þ\x001a_ÊòoÛq\x0011tF½àp\x0010PfTqwß:âí\x0007Æ?cDÃÜòvdBµCB\ÅØ|\¤,\x001eÞE¨\x001a+x\x001aÂ³h|ÓË¿m\x001fZ\x0019Ö·3É)ã@º¥).ß
¡D'WölEº\x0000M\x00108P5gÍK>Ðîê\x0002L.¸AG¼Õì8Åóm¼ñÝð¨(\x000cÄàÎî\x0017fG5\x001døÒ¾4\x000cÎüôE\x0012Á:¹3Fð\x0016óo\x001b#h?\x0012#Ô%P\x0017¥¤×CP2Û\x0019#6×çß6FhO¤o-
;;0ú\x0018µÙÖ|ëoï¯>;b$\x001e&1^ß]ì½Fµ&u²4Z:-¤ã\x001a\x0000\x0003ã\x001fW@0ëõÙÁÞkü«M\x0016«wl;¡f1¦ÏÓ\x0013¡Ñôha*Ùn\x0008à`#¡`r$ô¼\x0019I¾#\x0011]­á¨Pa)!¸y\x0006q25G§¨v³^eÃ\x000fÚ
¬Á\x0016xzR´ux=|ÜWÐ±\x000b©	QUg9\x000fí¨Ý\x0000»¤b\x000f  ¯ä^\x001b|ÜÎTH¬ú®\x0008!>¦Ði-\x0014uT¤r\x0003×2Õó8\x001e¹\x0003BJè05P´ñäãx¡\x0014/aÜ-ÄyîFµ\x0012\x001b"i
bÁ\x001b5\x0016\x000bÖHS^®¯JÙÌ(EüôIÂÃ'ê^áPç½³Ïkù´H÷\x001c¼(²N:0¹WÎ'ûè\x001a\x001aììÏÓ\x000bxvðj3G.ßÂ¥¢Ïª\x001a(w¦ø©ØÈzg\x0016ëJ;¸¾üñëÍ½ÁòO14¤zsy·÷æâ&}Öï\x001b\x001aS¨ \x000bOI!ä\x0011y\x0010ÑÎ­­G9\x000e¾½7\x0007'éÓþ<Û\x0015´BIH®\x00135\x0005Ëd§£`5\x0003\x0017V/IAlØm¨0\x0005&t¢jË&;¾R\x0007*ûô°¾\x0000®4ýÛì#b³lw"Ô(I¶^Ë®©ÔXæ­»P5Ì¸§Ef|zçWo	\x001dN;D}4s¼\x00055è,\x000f\x0002ïH9©oÉ\Á"\["×Ì:>ÞÂ¼2MÏ3)D¤f"P~ã7/±¶¹UÃ5¡Mç\x0016\x0019ËùÑK\x001aÇTC\x0012\x001f½4øíUb\x0007^þí\x0005ù|!ì6YV\x001d%Ësâ°ÕÇ\x001a½¨8ZCõíWêÏûÕKQ49c`\x0001TL7lÉ\x001a/~{øú\x0007ø Ðµ?«²°7ß7Iç©<¬\x000fT5Öïr|bcèrÞª*ìÍáÏ³Ea+@¨ôÁ\x0016@\x001fM\x001eQ\x0002%\x001f)\x001c\x001b}\x000fÏÈ;"\x0004	};|â^D((}\x000fr\x0007yj/4ìÛ¢½êõ¼jb+!\x0014áØ`\x001a	¥Ï\x00117èZºãa^	ËQF7¯¢ÙJ\x0008û66®!\x000cë%­`ç\x0004)Ø¨
 »\x0002tPÅ?MQmìNNèÚ¨ù	\x001bÄwvEÅþ>þ4\x0011:	
®z¤\x001ac\x001b%uWhN¿;B	²Ðæ*hV6¨¶\x0002BG¶ÝvgÆÆÃS¦×­khò+\x0014\x0012å*w\x001b¸·, jgGÙÃÃ#þ4\x0011ê\x001cõ 0n>ÇÁhÌÍË¶ÒÁ\x000b¡·ÆÚ\x0019	8%4D$\x0001òf
>ÜÎ\x0008QìÖ7aÁ>$\x000e\x0008'ÀrH¤Ù\x001d ¼½ùÐºZr\x0005\x0012\x0008y\x000bZB'JÄ\x001däî\x0008a\x000bÖ-Nfõë@ÏÕ6\x001d¢¾»C\x0003\x0017ñ§Pbv\x001eå#½\x0005§[Óëdw_\x0019k&B³¡\x0011Y^Ïs+?Îeaw72\x000eíG9k\x000f\x000cÉ\x0003ÙÖÐW©õ*DÍt0]ÏêÖ«D±µ\x0004Vm\x0015ØwÃ\x0006ö4\x000eºX\x0017º
2\x000f\x0000\x0001'BñèËPÿ´vÎÅ]àIvÎ¿M|>\x000f/\x0001>¡¨ö)]Ãì
:Ìí\x000fû»lõ\x0005!·M´	\x001e3>ømyÔ´C¡]ð=î:Zùó\x001aËÏW	£e's\x001fÍÖx\x0012ª~òo\x000bµYF\x0013LKL¨YÊ;Ëêkf7'W*\x0018)ø@IMÌªS Z,ÞÉ×ÕB h´Ì0!î\x000ekòôiìä"
MÒâh_^ÜÝ]Üoa5ªpäß&D\x0012Í\x0004DgHIÇ*Ã9;Ïï»B4Ø\x0018qJPB¦ÛÃ*êU¶EÖU{¹KDNBúÒ¹c\x0014>´¥l¢\Ô\x0010Û\x0015âã±EPØMG\x0019¿\x001d!z\x000eGp\x0004Ùn\x0008áåx?ÿ¶\x0010tøÜ4\x0005â³¹$Â:IDZ(Mÿ][\x0000BýGþm\x0002\x000c<Ö0zE\x0002\x0001°jÉ
»\x0001Ô\x0008ØèÉ@ß·£¾o\x001f)\x0003g-­ÁÅÞl\x000f¸55cÓ9¡\x0007"ÈÅå\x0004\x001côDð\x0017\x0016~'|Æ@\x0015RþmJnyÉ\x0012ñZ\x001a$JËG1§²>ìæ\x000b§pÉ¼»Éì_4Æ#*«:AÐ\x0019¨_Ï\x0006NRVp\x0017\x0011y÷>#¾oC¾LðÌB^á\x0017Kø/±%¤½øb¿\x0018ÌMÉã6q<ÅÕgüÇü\x0014¿VàI9,\x0004$%n¸¥*\x0002d0¦ôÏ¹äÅÑ+üÇ@Èk#ii&íAMÞÎ¶1ùÀE+Kñl;å'Õ¸»Q¡\x000c4ö£â\x0011
1ú\x0001)\x000brÛIÕ±^Òz¾p+© \x0005·jÈ=óé.g%v«§D¹{QËÃz\x0007*#IúáðD@Udån\x001c\x0002ÒÊK]¨&E¦U
¥ú2Ä²\x0001&eø{Q=f;QÇQ6\x0000\x00031<kÃN\x000e\x0004éæLÇÉw\x001e)\x0018ñeÊ\x0002L®¤\x0003V4îw»OqT°ê$=\x0010\x0001Ýä\x0015ËèHi\x001cÖ³;Tn%ï@\x0005q5jÑ\x00165,\x001c8):9Ô¢\x00175}´ýè:WÕJªÐLßßÒ£úªþ\x0011«¸w\x0005:P3ë!5:>\x0012iÖ©\x0001RÍe| Ðº-ê»øþ·»Gkú°wrñçÿ¿Ö3QÞx*Æ
QGjóÒE¾FqvÂ4ßùÞÉÁÑ?R$æ©xxí"(x6§%s\x0002çYÃh\x0008\x0017Ù\x000eI?YÙÂÄÃ5\x001b"õh4×U'©,Ôä\x0016¨¢¾üëÅÜÐ_OS\x0008\x0003Ï2ÄTüVPe0ær¨\x0014	úüùÒR\x0008"ô%)5cG·\x0002;?Ë?\x001fx6 $=Z$Æ3Ã¤u}PÊ½¿þû7ÔÛZ-Ôë«Ë\x000b½®¢\x000f%a[&áGð\x00029öúèðMöaÀÈ¥Í¦HK¥ù£J¾pµwaZ\x0019¡¬Yõ1R9mb¸\x0016Ò[ÏµëìF#$MØëûØ¤ñ+Ëx\x001e|y&ÈÉ¹7]Lw¬dÑcBR%|m\x001eÎ³Î¬´1BUéûÚ\x001b]\x0004dN\x001b]´\x0014Ö\x0005	=$6vA¢Zá\x001dÀdHµ»d]övH\x001b°Í\x0013 S¨ÂEuaÈÂÎ I½k%#AÂÔ²Ä('\x0007Sv1òð \x000eFG×q\x0014 ô§Æ_[®s¦Ú A¢3ô-d \x001d¸\x00083?< \x000f\x0006oÙmVRwßøûça\x000f-¥
´\x0011bÉöþòëýÅ
É,a¬\x000eLø\x0006Sî÷#á¬Î
Ü\x0006Üäb\x0001ÔóÃ7o\x000fNö\x000fßäÙér¾øxñõþî²ü\x0003²ÄwÿÕ¿×ï&æ&~Ý;½¾úvuy\x0007LÊe¦L·÷÷\x0014\x001eÎAe\x000fût
3ÏùÙ´V:\x00128ð$1¾}@\x0006S N~::<{³uóáöææ¡^§!\x001b\x0014E\x001aÛ\x000c\x0017u~
{góDiø6³Ùè6³M}Â
dº[Ñ ÷0f4'¡&´ sÞ8­\x001b&Þ·dW®Ð±l2âí\x0006ßTêÜÞf@%6
!ÔlÐÔ\x001eUÇ'¥3\x0000ûMç[
>©a6\x0003/ÖÛ±IôT¥è\x000bXG
pÉÉy¿\x0005%$\x0013\x001c`n	§KuÀ\x0005ç±\x0018à X3æÙ`àîl\x0010\x0007áO+Á¢\x0006x¿ò.hÏiò¶z÷ÛÃõçß\x0005Làé«Jú«ûÿó<\x0019Ëûul\x0016ª«\x0013YâÉÝ\x0012ô3ZúB7É\x0000mU=ptòvïùéÉÉáÛpP¢­m\x0007\x001eÍ\x001aðgÏKhÜóÄ'¤Ú\x0001ßãf´¥|!\x0017|\x0003ÉÙ3àË¢	O6]\x000bÞ§ß¯>ý=Î;ùóÿò¼ù]\x0007Êu¨ðN\x0015%IÓ\x0010Y¼ÔY;:­ætÔ`\x0013sD\x0016e¥\x0016\x0010³ÍÍ·\x0000_=\x001dÖ	lK\x0006uò\x001dd)$Ëé0óÛò~sªµ\x0002Ý,û!­dP\x0000§7'2zjOd ÎEd£Kk)¿ÿÇ§ÛK(Ý\x0007	yü\x0019\x000e¸G\x0012*eÒæO\x0017iî\x00186hG¥µªïªãÁhÌâ\x0013ñ?\x0010Nüø÷à¾\x000fç ÍÕû«?ÿ;0Ï.S\x0011Ë\x0016Ckéñt\x001aa"ê#£çÉ¼\x001e.àG°}©\x0010P\x0011
}*@°w¤ÿ\x0003}ü|óËo\x0003Ãyã¢OëOàáA ¾ñ,\x001f0k\x001d¡±ss£ KH²¥|
$Ù2>\x0005l	ÿõ$\x0006\x0008\x0013þ«"Ýgqýi¸goï¯RÀüùòæ~ï/\x000f\x001eÖ#«
Þ[:\x0006è3¦0Uy\x000e·tõíp|úö(\x0005Î¯\x000e\x0017òóçÓu%5X\x001ejÖ\x0008\x0006{æR9x@ÿR\x0010Æúï-¹èhµqYE[?¡¦ËÔ\x0018\x0014Ù\x0012+á´.F5gÀ\x0002©¸¼\!QIË\x0005\x0003³·å¢óßÆå²²\x0015î/\x0007«¥õ¢\x001a\x0016Ü_fk°´C];C\x0014Ü`}\hVç
&C\x001fØ§ïßÕÕaAÅñÕåÃÞ\x000fW÷{×éz;ü~wñðq­\x0004s\x0002úG!aÐåæÒIÌ_GcG_óèð|ï£·{pÍ\x001dþ|vpþÃü-WøVáüS\x0005,oO\x0014P?O\x0014\x0010eT³ê\x0013\x0005,½ÝO\x0015\x0010\x0006(áÏÓ\x0002üúñþ*\x0013\x0003:øSrKXhrûpýç?×y#
Ò\x0001ïØhÎ*B2R-3AÍe\x000c±¼äôüøp.4\x000c·\x0017ßnÁA
\x00163­äÙ\x001f~½ÿó¿¿­µË\x0002f
|¿\x0010½H2±H¥Ä#\x001f)-Ö·?­qìµ¹ÿ%þ%9øÖ.x¢ÎÍ§Ëµ×\x0004Öú£Ã\x0006ýEØ ]¹7ÚÙèã#\x001f\x000fN^\x001eN\x000fo©PPøI5 8'\rÕ°ÊJ:OÕ-Åén\x0016ÈaáÏR\x0016ãð\x001cXtÀô)°Pü\x001eíDü¾\x0018\x0005bAcE©¢$åHÓ²\x0014\x0018íú¿\x0011¼AI×°.ÚÂ\x0000¡¸Ö\x0003}\x0019J;Fã\x001aY~{ò\x001aX,¸9øC\x001c_qzØìA¹\x001e\x001bÞòr#&X\x001eAêLC\x0010xsz2{nïÞûï\x0006£Ð>·¹d¤y*dÔÀKÛ" ;Jh\x001f½z
Ït\x000b²QòÛoþÓ*:\b÷1àY\x0007'\x0011Pi)\x0011Qã3\x0016ûòFl\y=\x0014ê³þÝ ´__Þ|¼¼»Z\x001aKæ
_Vq7kzò\x000cJÈ-M|á<<ùáðìèíý»\x000f_ò/S¨(!¶ú\x000bL
!@Ômã«¢ÐÂ
¦ÎEy¤¾'Þ ¢ÛÜÎf:SÑF:(Ê¡\x0004\x0018Þ½\x0014?#Ùÿïf:'\x001aél>|¸v_\x000c]P\x001cþ`\x0015g7\x001c}ÙæO+ì3eµÉ=©ií\x000cåa\x000e³/_Kàê\x000f+¿¬sâÃ\x001aE\x0013èñËÅBg·Á«¿¬lþ´ð\x0016A­SYÑ7á\x0019Ã­}[DW/k]<mÉª¥ðÖdn0´Ã[?×§D§D+Èû\x0000\x000fºÃ²MI\x0016Ó;ÞÌV ,Á®Â®
Ï\x0007óLÑÎt%Ø¨93 ü6lª^:Õ¸t>°×\x001ebºÚ=%\x0011©\x000f?á9»Í±P¦:\x0016ðÇ6<\x001b©î%m<e\x0016Ò_Ò\x000b\x0001½£mèêc¡Z\x0005Ô0Ñ±\x0008!w¬\x0000±ðPI¨\x001fÏ×ç[\x0017O\x0007ÞwÒñ£º\x0005\x0001A:\x0015qÛBÅzñbëâÁ¤ë\x0017|ÈS	v\x00131Û\x001c\x000c-ªÅ?¶áÉXL\x0014\x0014ÎÂ(
Þz^ocòt}×êÖ»Ö'Ï\x0002Û\ñL¼õ-ÐYç-ÖqÈýÕ_ì+YÑýÛErå×à\x0014Èzè4Ù\x0014Y\x0005LZá\x0003ùQÊÍ¯Þ¿\x001d¼8=ÙÄgÍ\x000fJ\x0005Ûø¼`»âAÀQg>RWHËµ¶[ð¥Ñ/Íná3Ý\x0001øÇ\RgàZ\x001d³E¶à\x0015_læS\x000e¯Y\¿ÏÄÈþ³vy	\x001a\x001c^Ø~£Ã»Ïù¬\x0008\x0005ÇÃx\x000cMÔ\[§¡ªx\x001bÀà*ÀàZ\x0001¥¡¢\x0010yv\x000cñDvøuø\x0000Â\x0001 ü±
\x0010^¦"Ù?-pb^\x0002ô\x000bÙ\x0017³>Õ\x0006@-ÌÊ\x0000&_¾\x0012%Ûõ.^ó|\x0004!ÓU×\x0010<+JK\x0018\x0014\x0005*{¢¿:=\x0019<»Ôx²Æ=|AÐDD\x0002[|zO!\x0007ø	ý|ºæÓ=ë\x0017\x0015\x0014ÅõÓø\x000c|Îõý|¶æ³=ëö¢ú,í³¼2R*Å|#·¾Ï×|¾/¹\x0016÷w®\x001fÓ
ÛÒm¬{ù\x0014Õñ\x0018
.æy
Äç\x0002¥í¼\µhâ\x0016|¦>¾¦gý¼ÄYÑX\x0018¨¹\x001e\x0015\x000e\x0008\x0017\x0006
×Ë7tÿ\x0012\x0016\x001dë\x0007uÆA\x0011_äØ(XÍõFÏU.à«Ï¯î9¿\x0015G t	û\x0014«s-^ÝçWzýLÏúy\x001e'\x000839å\x0012\x0005ï¿t@ú¿¯«ù\;\x0002}yO|Zp©v4l-ÌíäK.ÐÏè\x001e>o8ý¯ÓU\x0003¸|\x000fÊÞ:9W\x0015½ÏÕß×u|_¥ aï\x0014\x001ad¤ð\x0017\x0006Ltóùúüúó«Ïòñ5`^2²ÔÃ\x0000ó²B;4¢NäÂC×*Û\x000bF>>,ªßJö%\x0004\x00152ºÜ`/ÚZ-¦Ò\x0007¹häóÇÅ\#F_1ú>ÆÈCÒ\x001dâsW0ø0¥Üw²á\x0011âÌ*0ô\x0011Bí;UÁñ\x001c/ÌMò-mM½\x0003?\x000b\x0010ÑÏêùÒÊ		¸\x0003TÌ¨&K\x0019MÍhú\x0018U ¶eÈÇb\x0019\x001f0\x0006Ï·ÝdÄ¾\x0014ÑV_ZÚ¾Om³â\x0001\x001d\x0018*/tíµLáoDLù]®[ýÅ~¥xøáîj]¸\x0004çÄ¡®1ÝY\\x0007Ð4åcL\x0018¥\x0002WrZ/ÎNf»ó
\x001dÒÙ6:\x001d þ\x001a\x0011\x0002wL9~7\x001a7\x000f¶²ÉM6ÂÅ °Ã\x0001Lµ¢\\x0011¸Y\x0004çfn¥tJ\x000céÍIO.Tt¡NÈ\x0005å9\¶Ô\x000eFær\x001a0L»ø\x0005o.HÏt±ú²±ñËjcKÕm¤\x000bØ\x000bÎp\x00083íý-Cõg­ßUû@¡!t\x000fÁ\x0005Á	T¯¦½¥xõP­K\x0007ú\x000cô¤å<÷Ô
Å	T\x0003-¬[àézõtëê¥[ÌÒ»\x000c(à9Z=N_éæn\x0003«ñ\\x001bI\x0017¤Ç^%³LôRr¨[ÑÙ½ký¶Qb²\x0005èÂ\x0010\x0018\x0016/òØk¶Â\x000b²Â\x001b7[´x \x0005ÊOÑ\x0001o5X<\x0015¸*]ûmlJ
\x000b+¼è\x001bñà-
Hb\x0016ß\x0003<ëø¦µa«ê\x0016ß¢ð()Dõ-4fL^½°á²]gj<Óg\x0003w:%\x0007\x0002À\x000b®äýV«gëËÖ>­Ûvø¢
x¾\x0011ÏÂ¤LºÑ¼¥¢ÉôiKñÓ\x0019¡«çëë\x001b?®\x0015»ö\x0005XÀ¼zJKÃùé6åexº>\x001aºõhXe¨¸*
jpÅî â\x0011Ìå\x0017âÕW®n½r-iK!\x001eiK\x0012V\x00038»Í¹\x001dæÓ\x0000Î´î</Q\x001cÎ-åú4çà½h«O[\x0015ÝjV¬µ%üIAÐÔÿÂùVlåjWã¹V¼Ó£\x0014Å\x001ci{òêE±ÕÓõ¹ÕÍç\x0016Æßey\x0001á°Q
è\x001cw5A1Â6t¡¦\x000btðTéÎHNSéÀÎÛøñ¦öDM«'Ó<ZÃXÆwJ7óÈ±\x0010¯öõL«¯\x0007î¨+\x0002&EægT\x000f\x0017\x0005\x001f\x000c¿¯g\½z®uõ\x0007Åx"rz/\x0005+³²\x0015]½x­Ç\x0016Äh>\x0017\x001a\x0005àñÛrùÅÀ \x001f¯ö\x0006L«7àRÜË\x000e#VêÓÚ9öÃ6¾\x0015p^\x000b\x001cùp+W\x0016/¸mâG[§|lkÎ\x0007Z$-5¤Ù\x0000s|*ÔVtº¦Ó­tÉIVdS¬ÇÙíXuH½V	o«Ô­}\x0001Ûê\x000bx\x0007&á¡õ,je}Ùx¨lÚWûð¶Õ÷kðX\x0008*)-ÝÃPå²\x0015^ýq[-òÿrak£b[
\x0008¬hN$Ç¬:\x000cä\x0012?\x0006¿ÕÞ«\x0001Ûê\x000c\x0004á	ð<4B&s\x0017VÚmî3\x001bëÕ«\x0017$J6£«\x0012J\x0016^\x0007Î
D³Í}æj«çZ­^PyJ\x0012¦á-ÆáXäÏY3«ü6'Ã©*ñãTcâ\x0007µ¥ùkÒV/i	/lc]\x001d¹Öø,\x0018®Ù"z®gv§¥W­b\x000cW»R®Õ2\ö\x0006`GÔKvDí¸±©\x0011¯¶+®Õ®\x0018¨w(­à\x0010(y¢eõ¶\x001b¾Ö;Q¿Ö/²ÉÒÐ;Fjð{$¬îÚw\x0017Bç§3>\x0016\x0007Ðk8\x00125\x0001À×wéç§«Ë?ÖB¬Äeà1NpÁz°¾°:Dà\x001a\x000f\x0000ûú,ýüttxþïÕ\x0010Xu\x0003+ÏõUB:nO\x0000
y\x0002vr^¥
X\x000fu7pò»4­p2ßÔß\x0016\x001c\x0017DèqA]?°\x0019\x0002þ-áq\x001fÐ
ûâK²Â;âµC^ÛÍë\x000cÆïÀ\x000b
ù\x0002
no\x000b3§w\x0004ìÀ®\x001fX®\x00168w*!°,[XïjGø!°ï\x0007vèv\x0018ÔF¦Vv\x001føYÑ\x001a%v\x0005\x001cÀ¡\x001b\x0018´ç"Q¡Jæ\x000er)¼ÂvWÀq\x0008\x001cû'åúôo\x000cì\x0006¬¶Ñ£×³nà\x0012ç{Ct\x0012+ÈÅS¡P\x001fÔu.K¬vtqÈú¦ë¿êRLNRÉb×\x001c\x0013\x001bkwE\]u²÷®Kk,Ñ9Ä]áùÜEåXïê®Õ]'û/»Óø¸Æß1!ÑÅk<zKê'®.;Ù{Û)t"$­qNÅzYÃõäÊïêäU×ì¿ï"Ïç\x000cÖuªTÀ[¿£\x000bZV÷ì½ð\x0014<O8¾?\x001c÷\x0014DÇUxF]­quáÉÞ\x001b\x000f&3a

»4T\x001eÒ\x0001»d\x001bË·t\x0013W7ì½ò\x0014d¥"ùÅ TDkì\x0005;\x00151îÊVTWì½óP¹\x000e\x0003÷±cýih"Ûõ>VÕ§úï<½²ÇTµÄeå¼P_\x001bpuå©Þ+OAÀ!©D\x0017\x001e¼è\x000e\ÌnÝ\x0015qu¨Þ\x000bD	µ@ê7BÑëHÀv?ºòô.\x0010UcÕkð«\x0008:
zI\x000cÉvò§väjªÊ¶©~Û\x0006\x0012×ªX
IK,}äm¼F\x0008³¸²\x0014ªßRÀ¦à\x0010ÚP\x0011CÈ=(9;ðtuðtÿÁ\x0003!OòçuQ X\x001d<íÕn<]g)ú\x000f)}BJyèÙ.!ÓÖXÊwï¯¾|zøþàÔÓU
±\x001e\x0007§¥aÖÚ--\x0006Ô3Wù
,p®µ
^]\}½½A\î³A;ï\x0008Jè
\x0003ÊõÒKUØxupôæô\x0004yaJÐD§Q¨­\x001b²ª-`E.5¥çjRí×.ð[¿mé^Êª+V½\x0005+¨
g\x001cªuJÎ%gÕ\x0017XÊj*V³Íº*ªÍ©kZW/¨Ú¼ÎRX[oØm\x0016ÖâuÕüÆc\x0014ëLY³ýu\x0015¬Ûæxål\x0015«ÕeßÝÀýa­Ýze\x0007ï\x0016aØÖ\x000eëÌ32\x0005¡tcõ\x0011=\x0012Ø­W¬Xã\x0016¬!+7"¬,\x000bëË3©×ÞY\x0008+k\x001b+Å\x0016Û (n\x000f0&VÂ\x0004¯mYCµ°2ô¯¬/3d2\ô<näÁTó²7\x000bYU½®c1²&Vçâ\x0002l²\x0005Tj|0>6~Pí UÕÊÂ\x001f»iwn%ÑæQñ¹I±ÐÎK,¥­ï\x0004µÅ¥\x0000\x0015DyÔ@TZóËµe\x0008Ø¸ ¶Ö<-hU©wÒÉÐR\x0000o5¯­×jV0g!­ÕNÐ²'\x0004-¹ÈCA\x0010A/í®ì[/¶Ø	^V)>\x0014¶¯+)^Þ>|ZK(¬+ØE
.ýï³¬³Qx³÷òôüåáüsv3\x0015iK\x000bÄÓ\x0013pmí¦7¹Ù:÷Et±¢­tÞàÙ\x0006:(YÈpk*I+àY\x00027ìÂïÚHç¥eá+(5Ê>´ãïªåLËþ2¸ä-\x000cáà-p29Åè*£oçÈ\x0005q!py/¼[\x0017j¼Ð\x0007s\x0011iØ¥`N®ôRÚ6[Í»\x000cÏÖxmV*!°Q\x0010ðlã\x0001«ç¸;ÅI;×Â°\x0008¯>\x0016¾ñ\H¥"FÄ\x0017©GßEÁ\x001bå6\x0016%
.V8ëHý\x001fÝ\x001eKpF»ÙÎÈ,ÂS5jÅ\x000bÚ\x0011/¿\x000c¹èmq\x001d\x001añ´ªðÒ\x001fð@=ú¢ Sª³AÑriÛÛXÜØúquÚyÑÕ£øVhUVOosncýqcëÇÕJ=Ë1"ÈYr¨×ÙíètM§[é@ùè\x0016Il\x0001!\x000bÑÍöI/¢³£»¶Î	|úG¼ò,-¼.^ªÞÆæÅ+ÐjótÐüi¥ÆP\x0005A\x0005_·ÎÎ¶0, c\x001fO4zyRÃ¸OâRr½¬óÛ\hR¨\x0011_ëÉ0ÐÅè/pÂ/­*á\x00051WT¹\x0008OðZIá§d7^c>\x0002ð\	èÂ~ÙB>3âkô¥I~2}Ý\x0014ÔS9\x000c
KØn÷YUãÙÆ[Ã@ûvÆSkÉq|t·ñ\x0008pÃ\x0010\x000f:´àYí¸ÁG\x0019A£m¼*öÎÏ6
,â\x001bí>Ùºû¬.3U23$\x0011¡¢ç7mÄmø\x0006]*ÈW·©,;¼Ôh\x0001ÆÏóáå@(\x0019¿¹®Kâm\x0004!ÀÑ\x0002¶Þ\x001dÖ\x0012ÇÒ¬%kØzå¶úÀnÄçZù@c7PNÃWåuiâòz¶Ùb	\x0012¾âC¬\x0016>â
òµ4l_t ¢	P\x000fÝÂëjt»©ÖÛÍÉÒo®an1­_ä©\x0005ÞluÕèvS­·¹Ð\x0012ù<vãã\x0000KZù±º}#®\x000f°Ò\x0007Ø©Ü\x0006ÆpåªÜ±ïÑduñi|k\x001bH<ë}]+<\x001f}Þ4ZZ)WÙ2÷\­ÚiÍU\x001f½Êã©×\x0013º0$ÔH\x001b¡	<\x0013%JYú\x001c\x0015\x0017¦\x001aPpÜ°ºDôP=o1b
>\x000c½PAñz¾\x001bw\x00007\x0013\x000eº~ÐfB­ØÅ´9UI(LÏÚÏ
eo@\x0002ÛWy\x00175\x0003+í¼ËEcÒäÙ©\x0011ú,r\x001cgoÃµ,ÎL
^Z=þóÈôqB7SZUQZÕG©}ñY#(éà÷¶Á±R¢¶n\x000cáfÊXSÆNJèûÈ\x0011{2×¤l\x000bcÐ\x0008Òr¨mNTNôB
z)\x0003.A²
VËuj!W\x000fO\x0008©Æ\x000b!¥Ã\x000fë])oC\x00086arrÏbH_¯¤ï[IPWÎ)ó´)y\x000eMþ
/¥í<9f4kC<k®A\x0012Å¼û8\x000fgbpD\x0012õ&ØUÎ<9ºn\x0004éaý0e*,Ó¥Q¼\x001d°¬$-"\x0010NXrZhj\x0013VrKXðÇ6®ÀM®Á$\x0007;äc!\x0003­¤=0ÚÄ¥\x0006V\x001a¾â ;¾\x000b¥ÖòÄ\x0014\x001d
OüPºæuôÓÞÌ&.½rc$
»\x0016.\x000b~\x0010nxàJaRÒ³e²µ\x000eqZÄ{#Wð\x0015Wð\Å7BbÀ¶AàÒ.Ðz¹é§¢M\¦çæm\x000f%©M\0\x0008JÓw\x0014$µ
­\x0011¹ÌdVc3­¹öWæ\x0012+\x0004*ÓO\Á\x0012W\x0016\x0019ÚÈ¥MÅ¥M+*û+yRÖKÒÓ]Ó\x001b±le\x001b± \x001c*K2\x0005È0Óà`¨c,ße&ÌPò:q
\x0004_qÜÁ	\Õ+¬KÉ {\x0013ÕÕ¶?¶qiÍªÚ{ª¶¦ì®qíãR,S-×P*e\x0019VÏÈHXE\x000cÖr7MZ­¾Mome\x001b± ¡sOËeÁ/[\x0006×$¬éwäX®²\x0011Ö5Ú\x0008\x0019yÀxÀÔ"®\x00153¹iYÍL¾fòLJ\x0012·ìDØÀ¶ÔôÙx[\x001fBÛz\x0008¶NÂ;Ñâ\x0013\x0000ÕôVî£iù¢\±æÍÛJÑ{I!Ùø\x0014ãÑ\x0018üô\x000bû&.'*.'Z¹¬b1cí,ø[§-\x001bÓi}ÍX²Æjr\x0005a¹<O 4ÂQ©®u îD.×´\x0014Ðf.]s5ÚR\x0002_²ñ\x0006¢\x0016\+¹:}L¶fj=Ö<\x000bä=H|LGªèy©ú¼yÔ\x001ab¹F/\x0010\x0012ÑÒRit ËÓ|´Z}ÔùzkùÆ­\x0005	ñ¬J¸"ÕûYÏ¹SØZ}\¡ÞZ¡qkiáHÝ(G5.	Ë\x0016'pZ¿v3V½»Ú\x001f\®\x000c¥-\x0007°^\x0018¾¤5ëò²ò²\x0015ÊPÝCÔ\x0019QYQJt¹\x000e^U¶Ô«F[ªmdñpP9§ÉÞË²á»¨tM¥[©\x000cW:§hÌ$õÚïÿ'ú¸Lµßá«åyLªÑF ¥Õ*_1NÈÚÈU{Z¾ÕÓyI¹\x0004u&?ÄñgÓ\x0005¬\x001b¹joË·z[:Ec¹ß*\x0018Snê øÑ\x001bâ½.®Ú@øV\x0003aD\x0019i\x001c?Æ[ÈH\x0010®\x0004ÙÄ\x0015ê}\x001fZ÷=¤TÁÙá
Û<´]1¸\x001aË5bÁÓS~úL\ÙBDÇ\x000fÛb¦Îr\x0003\x0014õÞÂ?·QÒg6\x0012É'BÕ\x0019¨ÚVÜÌ\x0007c\x001bºÀ¢®Áb£Æ½ü\x000e\x0006\x000f
ÔTâD Nj\x0003Ï$=`²ÎÙHÙ´q*O^\x00050Ð9v¹X[òÛÓ5\x0014ó`Âgâz&ÎÞ
am÷(ÐA³@\x000c¾hN÷7g«­y}5ãNG;\x001d\x001b	A%\x0006CQ\x0015Ü(dÍvðbBS­áÔ\x0000½M=!®¨õ[ÍjýM-Ä'\x0000g+Ph¼\x001b\x0012\x0006×L(#¾gb_)3Ð\x0015/a)ðXºÃ\x001a\x001e
ÖFèbÎaqj\x0019þf"O¶\x000c[!\x000e»ÁÌh\x001cÈBÄäF:Uªðè=Ýú«"ÆõS&7"\x001aqj\x0014ë¦J\x0019É]Ö\x001aò*e¸PfÚ§\\x000c¨CõuhÿÌP;Q²¨¨\x000b®%\x000bÚwïD=5C\x0015z¹¯ë*Ãïw\x0017\x000f\x001f×¿cÆ¹~t\x0005õ^ØÀ!ÌX<dP\x0003pøóÙÁù\x000f\x001bùTÅ§Zù \x001aÏG\x0010YÄßÆÈW\ú0³írË\x0008½\x001c\x0012BÀÜFîgó®¼©\x0007~Ï±oê
¡\x0002\x000cÍV\x0012ÓÃKE$¿j\x0015\x0011úÙnÎeÃÉHr?úfÂt\x0015K
ïµÆ:
l3p¾âh\x0011¡Õ1²ù )\x0001¡}¤ÄwT%-bäl­Ì2ÀúÈöâ ½Å\x0011#Y6'¢àH6ºíöáðÒ\x0003DÛ¼6yô­áU/G\x001dGÕ@Z|¶(j\x0019¢w\x0015¢wÍä%ð\x0011\x001c}ÉI¹ñdV¾aéeâÃÊËÖ¯,J^@*1\x0007¿¼ÒÎ÷¼/C¬/\x0014Õ~£ÀØ\x0015êÔ.ÒhGØrU~»Ã<lo\x0006DÛ¾*|Dv9ËéxèOúÎÛÙÃjZÌÓº\x001a\x0001A×0ÐÔ$'µ(ïv»Ã<\x001c3~C;"\x0018D_,b¤faoù3«¨'\x0010/î>\~\x0003´5`ûG\x0006-P¿:*ºU)´¬\x001blXÃú4ëÓ¬a-¨v&!\x0018ÅªþÌªã3\x0007
¥\x0002æþ¸íº¼5é¸Ñf¯ûÌª^CÕ¾Þqý\x0011dþ\x0002mCÅÛ0êí¬Ö5¡n'L'%ð³\x0018kA9Ðg\x000f1nhê¯l¿²\x001fÞÌZ6R¦\x001cf·]ÍiyN[#bºù\yÕÈ	%Å-â:'\x00046\x0003Ö6[·ÛlÊd\x0010Ä\x0016"\CËöFnéÚfv
\x0014Li\x0019°\x0003\x00115×Äù-c\x0015[[mÛnµ½fÁô-iN;eDy'2["êÊG´ºÙGô0ÒË\x000f«j]òjørf»ólëÃb;\x000e\x0017ÅÁIç9W£;Åa¸·sq¬¯\x0011};"6dc¨\x0001Úi©Ô\x0010Óe7\x0010!,÷\x001füU£ý<Í-Jªô\x0003å\x0011¾¥µÝh{Ö]Ú>âLL;§\x000fYé\x0013³\x000cÇ\x0006Z(þèã}mé09á|wp¦\x0010_\x0013\x001eiorc\x000bM\x0017c0Ê0ÈQåüÃÞë»ß\x001f.ï×åí´(Ê$ÜÞ9,¸ÞÀ8­×÷ï½>8ûëùáÛÇ¯\x0018\x00191º!bt}' \x0002HnÂææìl\x0013á0_\x0008\x0007ù&D#XÿPYýÆÈ=PÓ\x0019¥±F\x001f:r¯´-
ÐDÌG{#¢\x001c
ðÁ¹õÄÝÃÞÛ_o?_lÈ\x001dÇ2ñZ
úÀ:°l`úÂÓÇä|ïí_N_\x001dÌ7gfõ jc³¤\x0010ó¤
\x0015sxÍÇÃh7\x001d·,eÓC6Ý¸nºÈÁA­½ãûjXóôí¼Í\x000cÙLëºYRZ
1ÑmZ7(Âvpv\x0008g\x001b\x0017NYÎÂFWfªÂ\x001b\x0000U1},ÕÊÉÖ¥|Cöºä»¦«é´Ñ\x001bÎÃÜ££\x001cÍnÈx­gò8\x001aX<(bÔÔëè¸j\x001f¦3Ä\x000b\x0017oP¸
_V´ÒiDÂÅ\x0013è`#\x001dOUMz:_Hçªµs­k\x0017
x\x000bQ9jñÆ³\Ê£ñYt¾¢ót^\x001a®yO>)bA=\x001d¯]Ñ]F§dõelü´Þ®çLA=ÉôÜ6Véjín]¼èÙË\x0007:Ò2pÂò±z«Åsõâ¹ÖÅSOmUÀ\x0014f<56Üçk<ßGE(*Í\x001fÖ1ðtzåg¤7á¥àÝp
K_{PÏ/\x001e>_^oºÎraTÔÎ\x001b£(¥ÉÜ`ö\x001f¿:<~ìÜe²A\x0004\x000cám&s4A¢"çbÒe!ÆdÊm	­Èl;)Ëuòðòs±O~h`´Ií%h¾B\x001b÷\x000c/Aì¯kYh,üàÝäCñ\x0012´P¡\x0000\x0016 IG\x00075¡i®Q¾hÊx9ï¨Ï¡\x0005[;é@¹ªÿÿü¯Ó»\x000fWwëJ<\x000cª·å²f¨ÉG45Ï­+nºÖhïôìÅÑáÙ°\x0016jÌ¥\ºË°7§%Ud£\x0015?!\x0005g'+ù7UúÝ6ëw7¢A\x0008%Ð %¹OÓ½\x000f+²é/)e
&ÛÁ¤f\x0011
\x0013=2W(Ip£û¸TÍ¥Ú¹àp\x000bzMs9%\x0004\x000båaZMbm"\x001b¿MdÃñ·\x000bÉ \x0017êò§´é~W¹~>]|\\x001a+';6\x001a,´%wDMî%µºÁ$k.u\x0005v\x001bÉlõ1mþ(jß	à\x001a\x0019!Réd±&ídJ¡¦\x0005±L°U+;èû±¶\x0018±Ýb@!×Ñ\x0005xïËÅ-VE¾4êû±þ±õkÚä©x~\x0006wÎÒK½ÅîïL&Íd5ì\x00062)ê\x0013nEó\x001açð\x0001\x001a]Ø9Ï½SÜ5Y¶¾\x0011MÐd3\x0004)F\x000b\f\ô\x0005­ç{Êa}8¢©v´\x0014FÚj'`X"SBó]@ªÑµ©ZO\x0015ÐÐO\x000fÉ\x0010\x0012R¦8\x001c0ÓÊÐôh¯éö½\x0006ýJÔã\x001cK\x0001[~\x001232N«Ùn&³#²æE3ÂzwÒzE­.7Ôt9ýF²Ñ!ÐíÀ@×Q¤±kã EM·Rm$\x001b\x0001Ý~\x0006 °´oD¾ÕC4åÒ}\x001bmä	éVW\x0008\x0016MqC\x0015¦p£U|\x0006Æ\x0003 \x0016ºµRÇÑ²Åöe\x0003\x0011l^6Ge¬6y«S°!\x0016^63:\x0005¦ã\x0014@\x001e\x000cnpìtDË¯	j\°tÙÌÈé6­^7°åæY4kmG´¬¯¯Lß\x0015jF»Í´ï¶\x0014xò\x0015
¯Ô\x000e
UÊfC]3z¦ÛÑ´cëáS<\x0003O'¤d»æe×\x00195¶>\x0007Æ6d÷¹Ã9ÁÕÂÛ}¦It\x0013\x001dÝS¶ýré6 .d°lY&] ¤¾Ð|ó-ãhÕbóªI\x0018½g\x0011¤ë@\x0008cÉ\x0017¡K;\x0012µñÀ?·iV
\x000c¾\x000cXrð\x0004I[m<\x0014w)\x0019¡f4¹r,U¨ÞS\x000fþãüòR4;Bk\x000c$\x000cã ü -½õ¹ x0G
«zÜoUMÑ\x00034×\x0006"ôf\x0005\x0005Ç.À¨ù¦»20	%Ðb3/ïÁ[.Q\x000bÊv]©\x000e5L"ïø z\x0003Bô¨ÓÇ²Õì´*ýF²0"\x000b\x001d§ ¨ä[:\x0004Ü2ªg\x00047Å\x0011YkJ!­ÔîXÓ\x000ehÆÇé9\x0012Ðd}\x0015à\x001bÑT²j.P\x001bh\x001a®\x000b¦µ];MÊ\x0011Zsd Aw
ÞY.ß\x0015¶ÕÌ¼¦hjÖ\x001c\x001aHP$ÏÕ\x0015\x0001æîeÁ\x000c\x0007Ï,6!¼\x0010m\x0014\x001e«öð\x0018"jô\x0002¨[e·#\x001d\x0008ºÛõ¸þm)Úè.Píw\x0011/¦5\x001dÐ´ho©Øu@&HæÛ¿gÐ<ó-À´¡\\x0000\x0015dy\x0000í
Ü_\¯m7j°óI<}ØÜ¾á­çáBÆö\x001957²\x001c®Ýrødn)<)Rv<\x001eSr\x0011ÏtcôF2;"k÷!}T|±ÃÌl\x0012\x000fpÂð¢©®ä
£Ó\x0019ÚO'<`Óàæt\x0018rJÁ»2\x0012Ç¸ié¹
dZÔñ§\x0016Íñ§\x0002ýfGÓàu%/\x001a¨¢S\x0011 ÷Ø6z÷ÑÍ\x000f?\x0016î\x000eí\x00063¬²£\x0006*Ó\å©¦Þ6íZÕW;þ¹
ÆâÑhP\x0015yjx¥\x0008Ð\x000bÙsµëQÎO·çü\x0014å¡\x0012@\x00104Ëra)> ÷2ãå´ØèF´ÑfÓíMÁ#*	h:*ÇÀ«æ7FK9V%Å\x001aÔ¥«rü\x0017\x0017÷·é?².\x0007\x0003Á0eI¥ %\x0019\x001b\x0015#SzRt\x001d²_\x001c¼==9\x0003Ór\x0008¦e+	\\x001bæ}FÙÛ´xì	Í·w­çrzÈåt\x0007\x0017=ÉúäØ*J 8Cê]'÷C.ï[¹´§âzï#Íª\x00041\x0002ö·íªXÏ5Hj;\x001e1¾Ë:Y²\x0014=©ì\x0001AQ'uc­¼Ç\-\x0019ÉA\x0012Ac¾ªuÅG\x001bÈÙ\x000e,¸3HÃk)g0×.r\x0015r­d*zö3<h\x0013Ó£J
ßùcÎw\x0001¯%Ó®úÚµ}Íô7ÉUä°n%\x0003\x0007ùdûvÕéØºd\x0012Â_\x0002S\x0006S}\x0000Æí4¼\x0013ô
{ï@íX´®´®D\x0000Ég$ùþ\x0015×}Ìè\x001aL7éò2\x0010r\x0003¸¤áÝïãl\x001b÷z°9YÓ
Fz­h1\x000c¿ùÀÏ×:Î£o$«Ï¥i>\x0002úÕ¸j4°\x001a©1«ÝßIfUõ1­jý\x0002$ß}ÉQå:o[ÂÌÎOiuµ`V7/\x0018\x0014:ò©T$dµ+`v¾½x=YmÈl³!\x0013'ccæ,ÒYöýu\x0008³íí\x001bÈê5kßd4Z\x0012×,\x0014Á|Á9½Éö®\x0005÷å°sSÛGoòäî\x000cmÚý4'E\x0010|ÛNS6Ì\x0019\x0000Yh'3L¬V\x0019ùQ\x001c´ìüõ­d\x001bo¥\x0004fcIÅHMÍV\x0005~ÛÑz^i-«O¦k<Pò%Vï:ê½üëåjÌ5ºdP"\x0017©\x000e3p©â°²ÛV\x000cÓ+@e[]Ø\x0008#âªÓ«4NGÑÕ\x001bß5oüd!×SZT
ãí5×ò¶\x0011¬vú]»×\x001f5Go\x0001&Áç\x0015\x0013¥)*ÊÎ}_H×|"ÿ7Â\x0011;ê\x000fLÿßþ`6.(\x0006^]_ß®­s÷BbÐf Ò\x0003Þ	òy {^/ðèøøôxkàZØÇÊ©ÿB°	³\x0005Sÿu`Ã:÷\x00046¬s_Fæ¤¥Bßè#¥.¼aó
Z´ó:©ìÑæÏ`¾\x0006óÍ`U¡¥ô*òc«¤Lxn$S¡ÞdcÁÌÍ\x001f3
²\x0017éj<4Å\x0010\x0012}k¦íhµ®YH¢Éy;è\x0002Ì>¿wÞ0Y\£z»,Ôd¡\x000crÄDæ-÷°9O#À3ë\x0003\x001b¨\x0014\x0000Xt­`FñÛ\x0008¾u~Áñ²Ìq}`VW»Ìêæ]\x0016É\x0008yv£\x000bU]F+fät\x0012v3«É\3\x0019\x0015¹Ö;­x¦¤~ÞådµÅl6\x0018 [`R	,ÜF%`Éëå¦G\x000fn\x0004óµ%óÍ,ù8ÏÐöé!ÛÖÆº¹AÊ¸B¬¾c­ßÑ\x00055\x0000¦=xN¡HöÈ¬uÓu\x001bÉufé\x001fãXyzó\x000eK+\x0016xÉ\x0002©3z\x001bH1­éÛd±Þû±}ï{e @æ"kJ86°6NOÙ\x0004&G\x000e\x0006þ¹ñk:	\x001e"-\x0019mPÓâ%³]LúºÄ?·Þä-Ö®ô/+¶dÎN\x000f¹Ü&k\x001bnD3\x0016\x0007ë\x0019ÔV£¢ÁädH"\x000bÓ%,\x001bÉ\x0006ýòH¦d+MddgµçaB^;ËG N7lFS#´f/Û
]k0¯$]ë!NölFKÿØe7\x0012\x001d¡µZÌxVhÐÊf­[#c¾\x0016ËVÌ·®Xr
Ñû1è°Ðô?¯<
ð±¾Ë+K\x0017G
¦
-ô0X°èoÃxu(Í`Rõ\x001dÍ++Û}Y\x0005ï\x0002ÐàÝ&¿\x001bUîfºu6¡©aÓ\x001a\x0006¢uÕ³(\g`àT\x0011¢ô\x000cK\x0016¸\x0011í"a½\x001b¶y\x001f@(î¸ãÛû«¯_s\x0003úë»½Ë¯÷ßÖåd¡õ\x000bÛtÀC\x0013\x0011ÍÀÜ:Í®ö¸åøôíÑ7¹\x000býõÙÁÞÉá·?\x001dNê\x0015P5\x0004U} Pdf2¨
¬`C\x0019üíGÏùs Óú\x0011\x0005U\x000fQu\x0017jÚnÜF¯×¬&aP-²5F.[Ó
¨fjúV\x0015\x0006Ó\x000eó¹¨î+H¨bä w¢Ú!ªí[Õä\x0018ø|Ä¥\x000ct@Ø¤¸ìÊì\x0002Õ
Q]ç¡ÒÏ(\x0018Ó¡Láçw«CØÉ÷÷CRß·¨Áce\x000c.ªÆî\÷G·³\x0019zèD
CÔÐJpiUÙ14\x001c²éq]g'j\x001c¢Æ¾ï/PØ\x0017Ï¤Zg\x000f½À|þÍ.H×Í¿èÜ\x0000¹<Ðà\x0014%N\x001c@ï>­ê8	ÔÉZ_U½wUÖ}\x0005Ö\x00109\x0000\x0003YK6Aïµº­dßuå@<Èu,±µãe­®\x0000Ùw\x00078HK®P
5%Ù\x0016w²¨Y}vÕù\Y.j
ñbâ$ÛÅ
 +c%û¬\x0015¸zlS<j*E;/ÖÑx×6V\x0018ã\x00081íJ0ýÅ>þyøjôêêÃ¯´k\x0008ØgàíU²p4\x0008ÆF??ÂäÕQúk-¾øxñõþn\x000esP9£Ò%RY#mä]jmà¨(ù:¨\x0015æÌbÆül³rõ£¨\x0006O=ì½¾¼ûð}
ú1Kº«iEsp4¨\x001dvjN´îõáÙ7 Å
-6¢\x0019EmQêH_8\x0000\F³3\x0017ÐoJÞÞÅ#v|ñªq\x0013wúÀs:KØTµlR5®rüt\x0003Iâ\\x0012\x0018dé0O\x0017ù´éf¸ª^\x001d¶+\x0007}hDÎ-ÓÁQZ:»þ³ÎªÑiu«ðöÞ^Ü¤\x0000øàææb-¡\x000fEf2Ý1y8RPÒ'i5ó$½÷öà$ÅÀ\x0007''\x0007\x001b0¡Ì|	|z Ø	ËYÕ(-å\x0016uäôÈ\x0019Tr|s®æfÈ9³)	3Ô_=t|v\x0019~Pâ¤AðAÊRfæª©`
[ùhhd=ZìÍÅ§
ý1Zòí\x000cÜ¬Sâ#Ï/±3Rãx¼9xyr8{\x0010ßêå\x0000øF5|\x001bù ×\x001e\x000bE)	N)Àà5]vÎÌ*/ä\x001b\x0018m\¿ÑP\x0005ÙýÂ÷\x0003M¦\x001e¤nOÌ.â³Õú\x0007³mæ\x000bÑp\«é¦|`\x0010üðèô¼S³\x0004p("\x0000n]@Ð,¶ü4T2ö\x001eÊ~òÛÐ*ÍE®\x0006tÍà48\x00024ô\x0010éuy»
~¶òv\x0011_¬ùb3D{À3Ç\x0019xA\x0002\x000eÖz;[¹¶\x000föÇ\x000f·Kãúe¹\x001c\x0004dí´üeÝ|Ñß"ÀP\x001dÚR/Ûy+\x0002:ªåñ,?\x0016PlõM¨>°	\x001fX	ç\x0013¾ZzNøÆ\x0018ØÆ¨M&pöF¶c
m+\x001eiË\x0002$\x0005¿D¢µ\x000f\y`\x000e¤Ð&	3¯bä\x0014k$\x0016æ\x001fâÿdü\x0004A\x0007\x000f\x0012_GÆc!êd\x0014s®WÉ\½\x000bo$k¤Qé]\x0002\x001aë\x0015½K\x0002fÅ/úÂÕ¶ê5[­¨\x001c\x0014âºG6.©La¾Ì=ÀÉõÆü4*¢ð«D
oÖÌ,Y*"\x000eV\x0019\x0014º¤­5\x001aÈwvõþêÏÿÞÔAÜ[A©\x0008Y\x001eûaÎ0?ñÌ;\x0013gGÏë\x001eÍG¡Lô\x0015¤ïtyæ\x0006fw%'¡*)s1\x001bÝ/dÕBÆL\x001fÛ{*KÌÈoìZÏ(/FºþÖºÑÅÈ×1yf\x0013úÔ]jµ÷Ì\x0016RºÒõPø)ÕÑ\x0005\x001eí­à·¼5m=\x000b!}
é{ A¾¶d%xãÙÃ´Ñêý\x0016þ\x0002Þo___|Àwåë½\x001fooî/®Ö6Ô@\x000fÁ*Òü$¢\QÉ\x0019Ï\x0003}}|ð\x0002\x000fö~<=y{p4,ûæ\x0018cª!¦z²z©,¦\x0019b'iöÉbº!¦{zÖUïð\x0017ðþ¹Êóýpwña\x001eÐD\x0010E$ùä°ç´²ñNsON:måûáìàÅ¬\x0005Ê\Ã\x0012*·¯l\x001bXÀ\x000eV?ÑTv	\x0003\x0015$gGg&Ü/"ÓÕé¶%K¾Dî²Ë%\x000bè\x0019\x001fá%Íwo\x0006S\x0003£
K&d\x000b\x0019\x000còÊ\x0019¼(Ç\x0011	m¥e`íÌéMhèá\x000c+ÏÂþxÜëû»»µO,é,°<\x0011d¾éÂS%ô\x000f©\x000f\x001d­y`É¡\x0002\x000cí»!\x0013¡â¹EÊyµY3Òw\x0011`¬\x0000c; Ð\x0018\x0003\x0000 ô$åëea7÷±p(\x0012\x0008åx`îfD\x0013ËcvtZC]F\x0018Úù¸z=â{!UåÖ<4-Ï_öþúpqwuy·î|`ú&¨*Gpi[Ú2öQ&þàÕë½¿\x001f½M\x001e×8*DjH¤¼¤g½ "7VØ2¥\x0005©ÇÉ""=$ÒMDÎqg¤Jp:o9s¨Sã=¶È\x000cL\x001b&o>À\x001clpÓÿºa"£ÆVm\x0011\x001d\x0012Ù&¢d\(ÝY2CÉÀ@ºoÜ\x0010Èµ\x0001eÍC\x0000rÛY \x00011Á>\x001a´È\x000f|\x001b@o\x0007 \x0005x²n\x0018S.\x0004
C Ð\x0004$\x001c{b pE¢52Z&Þ3\x0017\x0011Å!Ql!JG\x001bû\p\x0014\x000b$WÏ¾4\x0013t	Q©ÛÊöQ4!\x0019ËÊÒ:Ä%0	éõ^Tì&\x001d\x001478&¤"Q \x0002
\x0000MH¢ç»ÉÊfË&£íã¹õø¸\x000c\x0003¹GéÃ\x0005@*T§\x001fþØ²¹µå\x0011\x001c$×\x00157éÇO)\x0015Ï¸Ò¬ºCBÛñß!\x0010xøè¹
Æó9|1yH±ØÃ\x001aä9iÉ3äDr\x0002¨\x0010Y\x0015ÕN+fÔÚÎS\x0014v~6ë5ù\£RÁ\x001f[Ð¬BÁw@d)aºç8gvç\x0002²Az\x0017Èê\x0019­\x001bÉ`¼­¦\x0002Uðêy:\x001d\x000bæ7¡i_¡iß\x00065PÌ~Ô"ymãl\x0008¶\x0004,Ö`±m£9º÷\x0012Yäñ*ò¬*;?ût\x0001Ú \x0004\x0003´z:æF´äS	´Y.\x0019»¸X\x001fÖFß¿Ó®ÐnCóÌE·#ÅSY»\x0007:lúÑlfÛÐB.±Çç)ð7¼j<ð<Ì\x0008_,BsÕùT®í|È\x0017i¦\x0007c\x0016Qz\x0017úÎ§¬+ÕÑ¥(_°ö®ÿç?ÿëàêÓ\x0003t(Ý¬»\x000bTú¸¢.§ÈÀ,>IQkFÆ\x001fî\x001dï\x001d\x001c½<V¥Ç¯Xu\x0010ù'Öðè¹m9,·ÏÞYVÄjX\x0018\x0006ÄÊ·c\x001döâKêÅï5Ú>c<IU(Æ©¢b3n\x0000n­\x0017Ön³²é&+'ÀÝ%ZË\x0015¬FO¾Á5ÐºziÝ6KþÅÄ¢ôX)\x0000Y>É\x0002TÆ=r;[iMMk¶¡\x0005Y1ÊI¦\x000b(çý¼f\x001dwãÝwÓ\x0004kkØGoï-K«Yt\x000cÄÀ
ÑòÂGQO\x0003«\x001d%±¤\x001d&±V¯ï\x0007\x000fï/ïî×ÏÃÔË6½´<J*Ö÷uk9ßì\x001d??<{;ñð!\x0007ªµ\x0000¹­m\x00143Z>DM\x0000gU2õ¤ÚïbÊP/åãó¿\x0012´£x\x001cN\x001e²âQ\x0014Ã%ÊÉ¡áK)CJøc\x0017e:ç\x0007©ð,Ô`ÐÆ\x001c\x000fCh\x000c5dè\x0004]$EJo0M"P8Ì¢ðcî6H=\x0010Å =íúV\x0012faæÝP Ä\x0015Ï~M©\x0007u\x000c\x0000©'ê\x0016AÊ2Æa\x0012f_\x0014¯¤Pë«6@ú\x001arªXi!$ËÁûL´FMö},¥\x001cÎÉè\ôRjZÊ\x0014Y¬ Ysß­·\x0015¤"ûsXÞîyî¬<XÇÉÈl1¥®Lå_·ì|OïË<
\x001aí\x0007\x0013ÿ2Ú®\x0003~lyõzr\x0000h£FÉëÄxz}õíêòn}¥R°¨ \x0007)\x000b¯¹\x0003Õq´\x0006Å\x0015ã°ùì81\x001e\x001fýttx6\x000f©ª\x00132HæÜsG?oèùßR\x000f)u'¥cYÅ\x001c\x0015~Ò³Ï5£i«ÍfHiz)\x0015\x0006å	r4Õ1QZþâÎÏ÷.¢´CJÛûÅ-ylQð\x00005\x001bG6é6¹HÛQº!¥ë¤Á¢ÔW¥h¾WZ_`½Ür[ú!¤ïÄÉFÔý"bÊ\x0015¹2ÝÂZ1/Ü°r,."\x001f<¿¼¾¾üö°¶²&ÝÏÍä^RFWòÄÝtÎ×tk??<>>üé|¾UWEä#aE±è\x001f\x0018ðÖ,«\x0013\x0011¤\x000fa{H=ÔíPaNz" \x000e$A7Ê%áezkH34\x001dÉ$\x0014*®$¨â´óg{)¤\x001dBÚ\x000eH\x0013Pé	VRsÍ×\\x0001Üâù{q)£\x001b2º\x000eÆdÊIÊÈJñt©x&£
rÜÀø^8Ô\x0002´«õD\x0001Ü?¾Ø{~0÷^_o(\x00130ÃFB+I¾\x0005t\x0003$Ý¨îëø`ïùA"Ü{}¼¶XébM\x0017\x0006\x001dTgÃ÷\x001dt¦pú*UýÓÕåÃ\x001fkM¶Ò8'\x0000å+$k­xÁ:f<(²ÁÉLÿûãN<*ÆU8Ò5ðxÐ}È\x0006\x001adI¦ÆIÇr
!Læô×óØÇ6ðè<\x0017	\x001bil)]/\x001a¾é?Ó²>*Ïj\x001aô³ÚÉ.æ¿¥Ï¼öD iÖCá
Ôáã\x0015ç\x001dìÜ`$êgýù§ÓY%\x000cZõ1Ûé>æ¤J¬¢Qxà¥\x0007Á(}Ñsé	_þ/×kþb<å×Ûë£óà²Uühãù[+IßÚ¸8ßLñâ/§çÇëëës8µÔBUC\x0017hP\x001cIi½*9Ô\ëÇÃ{@e¾3Vòw\x0000i«Öð7ðé×¦í£ä©é1Ù¾¬î`¼ FCcõòÄáÞ\x001bøæëÙ\ÔC6øc\x000b§¥\x001cãi¯©?Êà\x0014e\x000bc¯`!p\x001a¾ê°ü[ï[Q7iþxqóé2]\x001b·7k»ÍÒ©Æ'x.Ð6»Íga© ægRýxpòò0]\x001f§'³U)j¬ë ßþK/Õ¼1\x001eçRacTä¡¡Æ³Ö£·¹J;¦¨²Ð?å\x000bxÃÊ1«{dN¯!éLÐã«Ö\\x000e\x001aât:¬]ºÓc@²t þ\x0001]\x0005è\x001a`5\x0018ù±y\x0002Ã·õD¨ìS!tïâ×ðåûý»\5¢pÉCØûá
à½¿>\~¿»\x0000,nëö_\^]__|\x0000(\x0018£"ð5Å\x0008\x0003
à8\x0016Ð{x\x0001Dª\x0014\x001eá¹8<:>>x±ÌðùÞ\x000fG\x0010úîýõüðç³73Þ\x000bÔPT«	,-$.©#àb5j¯Eî\x001bÛ
\x000c|XÛ¼bÿû`\x0011\x0016\x001d\x0018P\x001a\x001a\x0016Üçß§\x00063Ð÷óï\x0013CK\x000eXº
òïSCóP)\x0018!ûù÷ ]]é;3ï>&{»ÿ\x0011Âý\x0017×\x0017_°EwÉäbÌÄîá\\\x0003\x0012=rx)³Ê.3\x001dì½8>x
îø\x0012\x0016\x0003,æi°(`QOE¾û\x0004ßèÓ¿Å¿ûðËµúð7ÊPO½½¸½¾ýüþ*«p©OXwß¨ç\x001bÈ4ø\x000f6ÊºH²)\x0000M¡	 \x0005ö6F&g?å\x0010n@qz|úêùQ%42Ï
vt\x000bÖµ¯\x0013k¹2+±ê¬¡\x001f\x001cLvß!k
ñ&\x001eË²N#±Â«%ÖÀ¬$Ó»#V0g[°¬~Mëª5g!`]³2ÆX<ñp¶U\x000b´»¸®T X){`[ Ýª\x0013¯gQ
¢\x0000ª\x0013ø*¨!\x0010ªßé²¦í4ñ¶ÕÆü"\x0000¬$+X¡0¶k\x000eþwÄJN'«WYµ\x000e¶\x0000¶ê\x0002j\x000c\x001aÅ.5Y¿Ø\x001a²IÅeØº*ÐâàåvÇ
a÷Xÿº\x00056]R´\x0005¬ÍºHUEÇÛUí\x0010\x0015.­þ[+,}\x000b¬PÃ-\x0016wî$V\x001bvh]KüÛ\x000fËv@æ)0yaÙdéü¾
ì{{uùûÐ\x001dÀÔîÅõµlÉ5\x001eä¤ùÍ`îsR\x0003Ú1ÕhbB÷àøõ<ËÿüùúzÀrvùËÃ§Ë½/·×þ\x0013ng@\x001c\x0000k0\x0012Þ¹\\x001cáµ
Y9(M¯¼èìðÇó{'\x0007¯O\x000fOOf±.nß?¾\x000foK\x0018\òçÿwyñ°þ\@êÑdsU¨\x0007YTÃ.Òè\x0018g¼=<8I=\x000eaÊæZH\x0013eÖ\x0007ÆÝÄ_L)SÌ\x001få¹[h.ßp÷5\x0005ºX,a\x0003ýx{óqÍþðb¦\x000cfÂQÇ¨¤÷,H¯³<P0^0ª
ôãéI%]Ó|ü{:yYÀ@ö|ÿàÛeúÐj\
Öþq{q÷qí*ypk\x0003®\x0012TÛ î¸ÔèÒ7\x000b¾^¥\x000eOÎ\x000f¡å$¶\x0014´ýÇéÁÙ\x000f²uþÝ{\x0011¢EþÝs¨iôý.Ùxrýv±¦H\x0016\x001c=¦Ý$ÙÌF'Íãïwøã\x001eD<^¦^°Â¤Lª)ðrtþ¤( \x0018zd\x0006\x0016Cé!nJ;Ý\x0012¡ÌfòJd&ÝÍdL¦)¢/Pô²\x0008>
\x000cet/\x001dBÙ\x0016¨ä\x0013ã\x000c%	Ê:UVª{K¹!kryJ\x0016@¹¬&
VS-ÕÍäL¾ÉäzP`²
e{É\x001b
t@É°\x0017*\x000e¡b\x000bTr¶Éæg7ð¼óÓ 0éÛe\x0011¬¶¹lÚç¾8Xàn\x0007r\x0006/_oì¸.¦Rµj2SÑa³\x0013PE³ºûØí¤BÒCU)Õb§"ô¶Ð\x0017esÊ]åL7Uõ\x0005UË\x0017P\x0019©Ëù3ý\x0004]î	?a\x0019Ue©T©\x001e\x000bGÈ¨ÇÈ_°¬è5\x000bª2UªÉVE(týY\x000e',¯½VDøú\x0013-_\x0010\x001a»*mül\x0018RÔ`Êfï5\x000cºr^t÷\x0002µ\x0015ùªÊ¼P:÷ÄÂEìýzº²
ºÅ*Ä\x0014YË|'G\x0015ÙyÑ6×º\x0001éÝéºv^¬B2æVJù<ð3QÔÍvTUÐMV\x0001f\x0006\x0012Îe<iO\x0005] º®n3
sÐÐ\x0013<\x001d?Ê?z\x00145ì¤ªn2
.fap Ê/ÿx\x0005OìE·¥Ò\x0003£Û<\x0018õÌÑ\x0007\x0014&+Æ¢\x0007ÃNq\x000cÝ\x001f0TT¡Ê\x0007R-\x001b0äÀ^È.÷½LW¥[Ü*(ëäëOå\x0012çdC	³L/©Lºi1é>EËÂ\x0007Ãñ\x0000J±nM¯E7E7-\x0016\x001dr\x001a\x0002R-1S\x0005¡rÐ|ùénWÏTFÝ´\x0018u\x0007å\x0014ÓÞ´ËTÚ²£ uïF7Q7-F\x001d´Eþ~ÐÆ¬|¦R&Bõºz¦I[ºKF]\x0003*\x001dj§$ª\x0010=»Å*ôº/¦²ê¦Åª[\x0018©HÎºÖY6,Q\x0019ÁVQ{¨*«nZ¬ºK\x000bÄ»\x001d0d¦
fu\x0006U/UeÖMYw:K7]*Ê²¯ìø©h9UeÖMY\x0007yrO!<t¢R\x0012ÍXò
Ýûª2ì¦É°§/È6\x0014:lr\x0010(¤æ/è{
­\x000c»m2ìé\x0003ZòA!Ý\x0005±ÚìPSU¦Ý¶vïÊ9P»'(Þï5í¶2í¶É´Ç\x001b.r\#97[bÀØ\x001dÅÛÊ´Û&ÓnU«¨\x0002éÂ£JnÁöú{¶2W¶É\yGÃ.±G\x000f¨\x001cù{\x001eÆVöRUæÊ¶+/³\x0014\x001cR\x0005öB\x0005«Dõ(é¿ª2W¶É\x000bU6ÏØTe)\x001cð®²($P^Ón+se[ýPÇTÔÞ¨hZ/P¹Þµr½rMö
Æ½Ò«¿È³0·£ªìkz\x001aI_C.\x001d9fÖpÈ¥»w»«ìkÊ:ºÈî\x0015¦d,?âÛ²V½¡«ìkË:Æõ°!w>'*x=ÊT¦×\¹Ê\x0013uMé\x0005cs\x000fI\x0002}fJÅpÚ8A«SUæÊ5+\x0002nöc"\x0014d*£øûÙî$WY+×`­\x0008\x001e.ý{òp§\x0004\x0015"'=|ìµV®²V®ÁZ\x0019á¹¼Ê	*Êq~(N=u/ò±ò
Æ
¿_~cvB,\x001e\x0005ßÏó\x0007\x000cÝI\x000f_\x0019+ß	M\x001f0N¤\x000fhòËwÚëüÀåE÷mã+[år¡ºøV\x0011rÆ\x0004%$gh}·­ò­ò­¶*øBÅ	>gøföý\x001f°2V¾ù+\x0010UàYIÃ=È^?ÔWa³oJªÛ£\x0013UÀÉKølªøböÝ\x000fÌ¾rC}S.\x0014j\x0016"YP5 >Àñ^wª{³W&Ô79|íù\x0004® m¡êª,¨oò÷Àà\x0001ïåÈ%Âd
¸mºwU¨Uh\x0004É­\x0002¡lÔ\x000fe£w6¡2
¡­¼#R\x001c®\x001aÀ³§hOI1;©ªã\x0017_²ê/@KÇOé°ê­\x0010\x0008\x0003\x0013Zâ-¤\x0006Æå\x0004zJb\x0007Föûz±ºjb[ÍP\x001e	¹PuôÐ&hî\x001cð¢Ù¨k'ëâ*¨öI\x000bþöòîîrïìöáÓå:&)] çe§Éd=s)§!o\¨WêíáÙÙáÞÙéùËA«EY#9.Ì¹0\x0007\x0014Do>\]ÞàtÌõPiïÒb\x0001îgäúÁR^?¶\x0008{\x0007'/\x000eOp*æÁË¹\x0006æ\x0001a\x001c\x0012ÆvÂ`ø&tÁqc¥Àq\x001cvµ\x0001ªaôþ¥øçfÆ\x0014äx*ÂôÔz¥dàz¾qáÎ2BóîÒÞý~yó.ý\x0001äWóïsPDøtÛrfÿ§ëéï/éÏï\x001e®¾îG(\x0008Øè\x0001É6®Æ}(ö.§Ø\x0016
ÆO\x0007Ç?\x001f\x001fî?\x0007-§3µ!¤%ópò_<\x0007o"½Ácðüö;\x000e5f\x000baÿÕíÍýçÛ»«}x:,\x001eðVK,òO6Ehüñ\x0006À\x0014À7x"þ\x000c# \x0011\x0017Ë¾óòÜß\x000e*{\x0007-ÔÏ/\x0013Â\x001f O(,}F»ÿ<-ÓW¨ÖD\x001dté`BRcéq\x001e¶là\x000f$µbðQçùùÑ7P~9è ~~ðþ\x001d4j&\x0005\x0006*¶Ü¸ÓÊ&S¼C a>,\x0016Ì$8r\x0013\x001c$Ý¶ËÝ/ÍpôÎCá²Ìc´
¬íÚ¶l¹¤M\x0004÷¦\x0014\x0014yV V<úwGh¹
£\x0019Íâø\x0005ü¤\x0011ÇE\x0001Ô<@Ùaþ»MÜÿqÿ÷ï¦¶³Ë½×éÐ}¸úrGq\x0006*Õ_0ò â,"àÆ¢Btv~¸÷úì(Ù²×\x0007ÇÓ2 ö¾úvýþÁ±<úü\x0005e¢hþãÝÅ÷ô§5DÐïÕ$´áÎ\x0012jR³yÀO:zõ\x001a¥¢húãÙÁÏéOj¥+®¼DO+§Ç;\x0014\x001eWn{z\Ù<<\x0011.\x001e£Hª(ù/öG¢(Ù~­µ]\x0011eVQñÆäy;\x0006ád»ÂúÛhåÎì\x0016ÃÉ
nê2_³r1äW
­XmIJË¥òa;<]áMÝçkñ\x0002>oèÜád²ÞRM|q4ÖÓÍØ|³\x0015ÜÔ}¾\x0001N\x0013\x0004\x0003&,Á)\x0016Ó~Ã§Ý@ç+º©\x001b}\x001d]Úk>Vt´%9bk0*o~¨§ÿbäB¾º|¸!\x0011ÙC!,T	xÑÎKgL,psK÷êðüdRgÀ¦lêi±é!~ZlfÈf\x0016\x001b²¹§Å\x0016lái°©ñYPÎÂë»?ÿ	76\x0010z!YÚÜÈc\x001a±Ù\x0002\x0011Sd;g_!çÉË\x0001ç\x0018Ñ\x000c\x0011ÍDtCD÷$\x0011Ã\x00101<EDYíEù$7£¬6£|»QV»Q>µíhë{\x000ewõ\x0008ñòûý:´\x0018óxa°1ÐÄ&«yä½ù\x0014óh?¿6zä¸ÀÌÀÚq9¹úp{½.\x0011\x0011@TÔ¬¥\x000c4­Z{åK¨!æ\x0016íäèÅéñÁ$Îº©º¸£\x001aÕ«Ù|2\³dÖe\x0005Z\x0003AÎ3b10Ê\~:çu¾iÂy&Îã\x0012S5 ý_\x0006¥j(õ4 l
e\x0004¯¶òÿÂ=¥Þýâ>o_¦²§8ÌíðÓõ\x0015ù2f\x001eµÿ<\x0019³ \x001dK@t9íì
vÛBöTAJ\x0010sF9r!ÏÏ\x000eÿ\x0003-ÓJ}÷xïðåñÑéÌz÷ñ÷\x0007}9\x0010ÿ·»«\x000bÒ\x0006\x0001KÇ^â\x0000íµõ4ëGIAK\x0005Î\x001cÎ~y\x000cöfïßÎÏ\x000eNf4+²{k%s¹\x0004È¢Ì%\x001b@\x0007:%2¢³-Ù£Dý"2h!uÌEl|\x00072ÒÿId\x001aõÚ·#Ëù·V²`PD	×LgÁ§D\x0016r\x000f®Ùô6k!{ô~°Ì)Ó5°Ïò?&2©eä}¦¶'{ôz°Lg\x001dEü¹\x0013É²8\x000e|Íí\x000f@Vj\x0005ùy;9\x0018¸¹¨8q\x0005éØ\x000eìÑ£Æ"0Éf öQ"ó¹H\x0016¾¥ÙzÉXIªyEl®\x00014N»ÁÇ\x000cf±åg;´dvd»=s&f4Eh&®Ð¶_5òiFó+S\x001ba@]&+ÖtÚ³«;ÿ·ß>\x000còö«+üõíÃW¸?báÊÙ»3ÄÜ8îN¬ÝÃ\x0000¥ô\x0019O¥+uÒtï½>=\x0003w(>ÉÏ!~»{ð\x000f\x0013\x0017è\x0003\x0006$øãíÕzB\x001cTow¯Uâ¨ÌÍûFY9}\x001eÎÁç\x0007¾\x001fOðÕ×h\x0003\x0012;K\x0012K)ð\x0014Ú]ò%¯LP\x001f¸\x0015°¾M[\x00160äúcX@+Ñúi:\x001aÊêHêâûÔ½Ëv\x001cG`û+øeïÇâ(H!)ä\x0002\x001fVWM´\x0002 DB\x0004\x0001*@P"Gý\x001b=½[uÇ=¼3ýIÉ=Çì\x001c\x000b·`x»\x001a(RÅÎv÷ãî«p_ÙÊw~ÿ¸ÊÃÀz_Q©£\x0003Û«Éíð4 µemjMÝBvþêâ´³x·fúí·¯¿IÓ¹tÏWË;8¨ÓÇÇdUHµWhEz^A\x0010Rô\x001d­`.^Âáö¬!ª0òÑ\x000cÄ0\x001f$v&ä}¸ÚR\x0011ñc1²m1\x0010ÃæÝ4dSk1lÞ¼\x0005XzôqdKb S|y¹0\x00088\9\x000eåGGÖÏC9r*?q8ª5\x0000\x000e§Ã\x001c<,q(£$öÛ\x001a\x0002	å@jË½\x0005tï0\x0010å¹,VBnjÅ\x0011låQa,\x0008¼\x00169üÅÐ3Á\x0013Ñ.WÂxÅF½©úÃ\x000cÞ\x0004r¹m\x000e9Ê\x0011~ô;.¿ È\x0018\x0002\x0010IÛ|p¿0¿Ýñ7\x0004Þ\x001cþfBÊ¿#Ô¹\x001a,½AòÔF+Gb ÂRÃ_\x000c8¸.\x001fÇª4M Â\x0003vÃÖo\x0001±OÒ¤/\x00063:ùø\x0010r¡6Z
M\x0019/Ç¾\x0018ôïÔà\x000b\x001e\x0019\x0004Ä#æ\x0001\x0002m|2îáV¾½ÚZ¢ôpðÃòóÍÝ.\x0013ÙxÍÑ\x0008&rjRØ(C<:O+<ëJ
°@\x0017?\x001d÷¬%ª¸6K\x0006q¼7\x0013M;á\x000f¥Ë\4O\x0007L;¡Çq-ß­ä*ÍsEÿ\x0017ÿÂ¢Î?ÿó^¯VËO{
O\x0017òÂ6{1'\x0008Aþ\x0016fý\x0014¶\x0017¯^\x001fåâW§ó\x001dFúðáòëCçk¾¾]^²\x001b\x0000¥íýdJ§A#é¢\x0017e\x0019±ø-ß¯´`kÍöúdñ¬ÔÝ\x0000gZQ¸íËýýõÝmÇª:½üÄ³Cw0¥.¼,\x0005&OQÄ!y¸\x0011ÎÖÕé«s\x001e\x0018º%\x0007\x0006³¸\x0005£òBål¸
P­¼Á(*W¦c¡êu8'^\x0014«\x001cÝÒÁ(>£§\x001c÷±À±À'"\x0014]ëÏ6lt\x000e?\x0016\x0002|é\x0013¹Ü\x0001Ç\x0012rö\x001d?Ñ\x0014lx\x000efy­=\x001eË\x0003|\x0000ÅçJ1< G£p$h0KÐ\x0014RÎç¹øäoGÄ!Cx0\x000cH½ÈïHæÉÍ\x0000#ò\x000cÄôÂx\x00182\x0007ÃÀ·É\x0017ÆÁëùÂ8ïËÁLxÓl\x000f\x000f¿½`\x0011\x000c\x0013J\x000cÑÆr{µ\x0018{Ù(\x001e\x000e6	&æéaø,K\x0018]\x001b\x001bm0d\x0018\x000fKl?O\x0003*ñ1Iß},\x000cYÇa°·ÞÌ}ëpe¤b\x00169A#±<Å*Ö\x0003(|)êT²ïø·-(ªåþÚ¼ê®L¶»$øüEäñ"möáÊ:\x0017ÀÈS\x000ccÙpPb¼Èc»}¸\x0014iÖr\x001236\x000fAAÓÁ°È\x0013a\x0002LÄ5h-Ê (I\x001c¯ÃÊÀzúL6:9\x001a\x0006Çê\x000b\x000c\x0017%fÒyHÒL\x0005Æñ/­ôáÉCÓ\x0003J)Òk²vÂ\x0005Æ
\x0010Ýp±¹(\x001f\x000c¦-ÉÂÃGÄbZÏå{\x001f_:þ\x0001Oõ|¹º\x0002çàÓN·Ê\x0006ÁñäVq DsÄ\x001cg¯|\x0004NÕóÅé3ð
Îûüª\x000e\x0019uí´áÊ,xÓ&ô$\x000ft2Zoûnmd¯0,Xx`9þ¨L\x001b\x0006àñóîØÔ	Ûh\x001bXe®\x000f\x0006Ó\x0000ÎÌùzð5;3Îo\x0013\x0002md9ÅÛø1=ØÍ\x0014å([Á{W¼w0U·é×&²
ûyè¡9\x001cÊÅ8\û<=_àéÌ|r\x0011&Õöë`2o\x0012L?¤Ø!E¾hq«ã3\x0000í÷_~]^~øVj`¶òîÓõ§\x001dTi,µÉ\x0001"\x0015C6\x0008d®?\x0015Øn¼Æ¨Çù~¢JZ\x000c!²\x0018ËËÁ\x0017íû)M\x0013,ÌÀ¬Þö	\x0013mD7ö\x0012\x0019û4\x0001Èàê\x001côu¬I\x0005×~»Ê\x0019
´\x0011WØ\x000f\x0004ÂãS&
\x0002ù\x0018Õ[/ùp 
~\x0000P´iP\x0014\x0019ÁD\x0008[¥6v»½½\x001bèÝ7wÝkýÈ¡²§×«·×«=¡²bQ\x0018Ä\x000fÈ\x001aöý`ÖqÃ¡¾à@ÙÓ£ÓçG§Ç}²\x000e×ºµËùTûò.\x0017;at¢\x000eê\x001b\x0017r\x0004\x0017]ñ6.¸Ø\x001aåø¼ääó"\x0005ÝÆå\x0015W\x0001\x0004"Ê\x0006ý0JËmH¨\x0011\ô\x0002\x001bÏ+Ã`PÓ8>¯È¹ ³¡GpÝÐÆ­q´Óäob
¹Èjhäò\x0014­08®0ZR®\x0002À\x000c\x0013¹(ü×Æeó8xÊx¬á~ÕeD#¸J`§QPÄC_îWô%é©Ç×ý|wóuS~=\x0002Ó×]Îr<¯Câ\x00000½@c4fA¿å¹\x0000ßÏÑWû9¬O\x0011\x001dCfÍaöÓ\x0003-B\x0001{ÆoÅç@x\x001aaSø\x000f\x0003?ªó
:¯©\x0000\x000eá¿\x0015K\x00039:âh?QT\x0007*q ©ÏáÑ@M±ÓÎ£#~\x0006G 7Jâ^\x001f­é»d1
\x001cª®ámá {d\x0018\x0007¨ýà2T\x0014\x0018D.\x000c\x0007-f EGè
ø*\ZÆ4GC
üUT]5ÙÂÑ\x0011rû9¤¥\x0002~k/(vãC¹¥2½¥ÅA\x001b\x0006\x0002OU{z.¦\\x000fÉ·C|+c\x0007b°76ð<<\x0015_É@#¯ÒyDYØèó "Ö¡ jøF\x000e\x0015qä1ÂÀáTÛx->ßl\x001aËqÿðÛãnã\x001dk~1Ø\x0007â*¡\x0005Ù£~3¿B(¯ÎþuÑk»wpjÙ>\x0000\x0007'f}\x001c\x0011À\x0012\x000eÛU^l\x0017$Cyjá:ÇSÊÇàH(:\x001diX
Çº\¯\x0015§±ûqBÐ\9\x001100KeÅ¥\x0002ÉªI§SÚ\x0001§£\x0014×\x0010ã¶&©èxJP0[\x001fÔNß~_Ý¼ûæ2gÃéþñvy·ßvú\x000cN
òëp\x0018«Ïtzuq²x¹Ëzê°}ãe
dSbí\x0000\x001a\x000eÒâ.½\x000e`\x000bÝ7>Í@:7÷`\x0014{l¥Ë>ç¡­sËØ,ÄJÓt\x0016òI,û\Á½t¿\þúû{ñ­Uüìöþ\x0013R>]®ò`»Þ\x0016Î°Ëd\x0014Ðhr"¢ÔvË3xvòê\x001c	.Nq²Ý>°J\x000e\x0007Ã\x0005
1³)Z}\x0005\x0012ÃPw\x0015Ø$öÛoÚÌVÙÎÃÙLjløNIz¦2ôSÙ*?-8
Xl=v\x001a8¨_Háïélü\x001fÎæ#½\x0004\x000bê\x0010pc\x0003½\x0010Ä\x000clÅÛpn¹\x001d
Ù°zÎpã\x000bÉ·à·i¨F´Ê\x0008\x001e\x0016±&+_7¬\x001431k+Í\x0008AnÕml\x001bñðs¬JáÜH/À¹En\x0018
^M§\x001bæòð+\x0004<\x0006.!\x0013Z	Ça«÷ß\x0008WÐ
U%pB¦|F\x000b\x000cgä6\x001b­\x0011\x000eþ\x0011rÄSÅå%:\x0011Í­d!éÈâWë\x0019î\x001cWë´ÁÙT«ÑçF?3Qü\x000cïAÁ[P#ÞC\x0004m\x001bI­ð*/³ÔÄ\x0004uK`®\x0019\x000eý÷\x0000JUG$´Ï\x001cà\x001c»\x0005Aé\x000b\x0003¢jÌ{pE;À+\x001bq\x0000\x0017\x000ciU\x001fç89P
jzÀ¹r>«\x0007\x001cÏGêÁ\x0008\x0003{\x001f¦ß9Ü\x0017¬ÇÜ¹èÈ»²¸Æ>«¡å³\x0008·5~Ô\x0008\x0007÷M·ß9\x000bÿ?©M\x001eþ_5{ÆFó.µ1ï><®¬Þ0~­þüÏ×ÿ×³ûëÇÕÎ¢\x00130Ü\x001c%\x001c¼Ì¶/öMQ&&B¾¹mÏN~ßWG\x0017§ûÖ¦åP$'È÷\x0003k¸mÛ2sßèÑý<Âuî~«OúûÕÛ=>H¡¦äÊ¼;\x0011*QR~îÛ+O5û§Ïû<\x000eÑ¦':(R1\x0002¸\x00074ï\x001d=)Qîü·â«hÓûÜOd%\x0005\x0008Áñ4y\x0003\x0012¦aJúQö¥\x001f\x0007\x0012múû8¤k#
(/ÄÕµ¸:ã[£b/Ð/¿~½õW[®ÑÿùÿëÇ?ÿ÷ÇOË]%g\x0016÷ø\x0004IÑ1E\x0001LaÖÁh·^¥\x001f_½>>_ô\x0015u°ê»4\x0018ËrE\x0010nª'±©×¹c³õ¬SÕ_o\x0018UR5VþEIFk%\x0015*¾-X©ßÀ]<¡D¼£ \x0019{½NÆ1\x001fQ¼\x0013Þ½ûæn=\x001cüs¹z³§!\x000bE¥\x000e:ïs/\x0004VKXÇEbË\x0017<;øçâôþn¬\x000eQ÷Z
$2÷÷XÄmXhr£Ý\x0012¶h!ê¨Dá\x0008k8<\x0001Ùuoß¸]\x0003P÷\x000f\x0003\x0002	@'\x0004jEs¬-)lÐ\x0004ÔM§\x000f\x0004²é¥ÎeÚWjE±ÌÜì\x001bi$*},-H¾ô¨â\x0006J£;ëyH\x001fñÕ®þòû\x001f[­\x0017Ë}aLaS³\x00065\x000b
Nwè	²¾X\x001c÷G0;LuIûl\x000ciw2âD\x000e(ILËj\x001ee7\x0014iÓD\x0019pLRcÒy¡rá«rLzâ1m#
`\x00021iI¢\x001f\x0013Jkèv2iÓp\x001arNK8±PÄèVk-g'2m!
9§R\x0010ÆÓ: ØxÚ\x0012;mbÚ,A\x001aÀd\x001c9\x0006¼ó\x001ckFIÀU6bzÿõËo\x000f¶>»×÷\x000fö\x000c6PiT}Jæ\x001c\x001bJ
Ønr}5Q¯_\x000f Ú¼M\x0003b©¶Ã*S\x001epÀJ[0gÓ\x0008ßÏ\x00138´¦¥Ò
!dÙÄ\x0013Ú,\x0019\x001b@d©Â<Õi\x001a#\x0013¹¥\x001e\§ôÝ0¢ZÇ
D
T\x0012\x0005HykrB²eL£ì)a\x001bÄ]
H±8O`5Câ\x000e\x0001'û#\x0007\x0012}SQ7HóT\x0015T'¿(ßMêiÔ
Á\x000eE²ådo%LQpbÒk+]-D´b!ë\x0012G¦	í!F]â&!~ÅáHh-±zºmÉ!j\x001bÍ$	Pº\x0016\x001b¤ Õ` IrUkÒ¸e@O\x0008=ÖÒ@$î]lA24A\x0010D©bU\x001c\x0017°AøpòêîÒ-\x001eåëÕÿ±ÓìÆâ K\x0015Oî­\x0017JpÖÃo­^Í®÷Ãt\x0015í\x0010\x0018%K
\x001c§AmQrÒm)R\x0019\x000cS{¶ûa¬KÎlª±\x001cÁQû[\p[\x001da0]v\x0008\x000c\x000eº"«ßÑÜI\x0001÷\x000b*°H`4Kí`ïg\x0001§ÚxúJ4m
ë\x0014J¸Ûæ\x0016
éÚ°`b|¬c
$ÀWFL¸1µ£¿ÅkJ¨Ãß\x001a
®)ËÇ¢·Õó\x000fEéÑ\x0003Pðù°ÿ\x0003æ4¥UðE¯ë	\x0017¦7ì¾\x000b¶±Q\x000eN²\x0018vvK\x000en(L\x001dÚ\x001bBc}q/¼á¦Hí$\x0017
êmEgCi6\x0002\x001fûiÈ4M)æ°\x0007&OÕú1M8n\x0011Á \x0010i¸I*ZT¹\x0012E\x0000)4u:Æg\x001b\x0019Ï\x0006SÊj¾6Ûâú;YìÝjI!³¬ÎWËÏð¯Ké½óÇÕåýNÕí}©j3¥^\x0006&\x0019ïu}Àùéâ'øÏÛ;¿8}új\x001b?¯n~Aw\x0013ðyqìÕýÝ]²%L\x0002\x0002Õ|
)ËÇ\x000f×\x0008$¢\x0006µÎ'x\x0015\x000cîÌÄ\x00047XôékY\WhóúÙÔs²¸xqÖÇþpúêåö)S5\x0015Ù]©°t[\x0012UÚ¯¨¨Üâ°U7
Ï\x001aÿ\x001aNeò¤U \x0002ÛÙÊLå½&*-ÃXªw¿­Þ½Û-\x0004X|¾¾+6áóåj7ÏÓE\x0001M4I\x0017Ñà©Å¦RcÓV4¸a/ø|±}YMHÕ\x0000"Mö\x0001@\x001fÐÍÏÊ3 R³\x0001Â\x000b{¢\x0001ÈÑ\x0007<Bí¤jãÐõÝ¹fBÛ\x001dÒO\x0013¢\x0004D\x0011\x0015¸%*#j­&@´~"¡»z÷Á<vçctÖH\x0000ÌÿùöÏÿo\x0007£ÄïÓ\x0002\x0001÷Tcw"0zirE ¼\\x0011ÿYÿþYkÈÎF	ü³çÛ\x0007%v)á@°PK´cJ!¥èû"%üóòuÔZ¡£9\x0017%îZH?­\x0002´Wòô\x0002\x000eèFÿ\x00010]´¹\x0003\x000001f?\x0017¦ÂÑÌég\x000cf~:VâRIÆÌ\x000e `ZÔ3aâ>'é§\x00193<(ÀKÑX¨0=½pm\x0004:\x001dsabNúiÆä&Õ`5øFÂgL¡i1.3\x0017&ª÷ôÓ	0ù05V=fHÅÜø8\x001f¤ÁDúi\x000cy \x0017P4<aê<$\x0012ÿÌÎw3±ÿñIúiÆÔ*{ i%Î²Lä#¦,4½þðkì\x0006æÖÏW z>}Ú\x0005)A¶çfó\x0000n¨Å \x000b\x000eÈ\x0008\x000ciò\x000egï«ë­Ï\x0016Ï@õo\x000fA\x0001¢ôQ¦éL(,kÉÿÜ]Æfã:8x#Xü\x0000MNÚ[cÓXÅ?..zLÿ.Ì.lå¯ò\x0000\x001fØÖFé\x0000È;;¦óá~,iE# y¡È'S\x0003)òù ù\x0003\x0007åæáÛ¢¶\x0007ñÅúÀù:\x0004#ðÈ\x00170ÎÄYôÓÈ§r³\x0017>\x0010W1ñy[\x001eH¾23ð¡Aá[ßTO\x0006|>Å¹2_`>WHOçÃäjúiã\x000b¶ðáp3ùh¸0òÍó<\x0014F+ÓO#^ÈR\x0001ÏYÌåæã\x0013||zø\x001b¼eÕ''O\x001e}R2¼-¨aÏxrô\x000b_ïõ\x001fÝëÎ
\x001føÛÏKð:0Ð±CÏa´Ag¿^K\x0006¯+þë80«7Û(Ï\x0000óè§ÅñÉ	\x0006Hö ¦Õ^Å\x0006Vcs¾\x001e-ãHÝy\x001dÈÂ±2\x0017\x000eûÎ}óø>i\x0015|5Õn$4\x001fÝßýrûx}wµÓ5´E9{©<\x0006àÐ5\x000cÜ.+}oÄ¤² ½zù£ÏútôÃKµJ×\x0000íðz5×ÑÃÕíòó2íNï7vò¦0t\x0016tj4B['M\x0014!f¯çuvptöìdñÓbû&õ\x0012\x0017X32kÉCÔt .¸©â^¬SâÿêôÓ\x0008*£
¹g\x001d@}¤ \x0003³Aq"ú hßÊÊÈ\x001d
jhü\x001cZ%é\x0008ê#û²Jî5Å[8QBÉ
15S\x0005¾à%1½eg6æù8m*o°#85
O\x0000P«@\x0003¹6*ú99Ó"X%F'Î\x0000ù
®Ýnï\x0014\x0011Ò{]Åý oÕÕÛWI¢ñVm¿K±5\x000cÓïÄt.-CFÝ\x0004¢_Hº$(¼w»OÞ§è\x001aÆì÷BºÔa¸\x0019kÙ\x000f©50¼ÊIÜ\x0004i,Qµ
S!ûåþæám7l_1þ¸ÄQÏî?\î\x000e°I[!Çt³w9\x000e(é¹£Y7è8Á&9Çn\x0017O÷ò¦:£ô3
\x0018}Z\x0019\x0016\x0002Í7ÏË@ß?D9;0ÆÒÏ(`,¶R\x0004¬13iñ\x001b\x0000¸×j\x0006FaõMPkð	G²P\x00036Üy

ÛÜWlmL\x00199ÕåíG÷©ç
cãÆõêÃÍ§åÛ&Á$_½Ë,;¢½Rd\x0000\x001atÜ÷T\x0007?\x001e¾8>_lï\x0012ê²ª»Sb\x0014lÚ*N^\x001e²FËË¬ÕÖÎúéòÍ{©úïÁåÍ\x0003&Ñö\x0004\x000cÚªÙOV8·7[ ÉS\x0001ñkw{*¹N÷\x000cói;¢Iêö½
)\x000fí¶¸öñæúqõçîÎXyrG=zöùºjW\x0004\x0002XX}é¾îöÇã£ÞtËS_>ZDÄ{³©\x000eÎ«Ý	!ðéÈHõJCC7%JûUö\x001býgÓ^Dyûå÷÷iÉ\x0012rð~\x0003\x0011÷SîbJá"|àÁcûaò£\x0004{&
\x001fòêq[å^JtShn3%´SÃ\x001fåÅs ÀLÉð ¼¦ü_LûÏgãTSàT"ÏLFNM±bäd)ªì =53Ñµ\x001d=3ûAøHÏ\x00079\x0003sª½þs\x0003§If\x001cgdNG÷\x00138
ÝÏ(£Ìy\x001bÄ×KÛ)®\¢@\x0012ýqðâþñöænw~Zó;\x0002¿¢ \x0008\x0013§×ïF?0ú\x001f\x0007/^]\x001coÝûZrÝõ\x0018TÚá\x0008¨¹É>£²622ì\x000bF4²\x001aà4#Y5}Þ`\x0015´bVBÅ®ÈYQ1,ß
Í· ÆÜJ
¨ZÞÔÎJ2þMÚ1'+ÚÒ~ämå\\x0002	§Ä\x001b°²­gÒòºé¬âRë?B7\x001cµ^NÈïÿîúöv§\x001aÅy¦ìúé@ivmE K\x0000\x0007ßgé­\x0015²\x000cxytrÒ'\x0006>¾{óõK
Ka&\x0005ÿêl,|ÚþÓNU*\x000c\x0017ka\x0006N'Ô+ÉFîõPÖ{\x000b¢®ß:¯Ëº\x0011ÒO\x0013 tl\x001a§¨
ÉKïXÕG­æ\x0002T©.Qµ\x0002b°lú \x000eÉ)¥áõ(D{e}3`D?mVÃ\x0005oqå½ÏØÔCïFÍu
¤ôÓF(eÚB6­½OÂS\x0010ßø^/®Ð¥WÒúL\x0004&ßr\x0014ö¸dKÎ è\x000c­ì38[\x0001
ÆÃÒOÛ\x0011
Çk\x0007ïÁ·ä\x0008\x000b.otÚÏõÓ<ôÓx1¯^
>H¹. dãÍÞèM3!nJ?g\x0010#¡T¬öRRe\x0007\x0010öF?\x0006\x0012~½¼ý*ßt-¡5àÃÁùÿï§]	9P6O´MZÅ\x001eR=!µê¢RÑ}Õz\x0005ðìàüè¼7#·\x0006ä\# yx:ìKÒâõE
\x0006\x0012>8ÿÙ¦=#À¿^n\x0014\x0012§×·Ë§·×»ë	]^íFO 'fäbÑÍ}"\x001b5óây*>=:Y\x001c\x001f<=9Ú:\x0015	H}wwûñs§M¶õ>\x001eÈxðb¹z8À50»uX\x001b\x0011êÄ¢\x001cõN÷qæÅ½\x0017é_µ8=ËÿªíÜ]Þ¥ÉR¸v	ÿZ¯\x0015þ?ÿó\x001d½½½yØ\x001d2\x0010Ôºm\x0008G\x001f=\x00066"e¯\x001f±^0|pôüäø¬ÏÊY>|x¯¾t+ÊaÃ?\x0014,ÈÛÝ¦#ñx\x000cÁ\x0008É\x00169©yd\x0017áÅÁùñÉ	\x0018[§§\x0000á\x001f×á]ì
ó§\x001fnö\x001cä\x001apñ!r\x0017,uÌ¢Ï_à%O\x0007?lï/¯¸LR,-\"w¼"\x0017×v\x0000W	\x0005õ×W7qq:u(\x0017\x0016Âx.LTs©1Ê	\x000bÙç\x00074qa1k8/\x001d,ÛY\x0012\x0017\x001a/å8¸«toè¬\x000b^¨ó
\^\x001d2Äj±|÷-\x0017¡k3\x000b£òMÇU²9J¨R\x001coäH£îk\x0013iã¢\x0018ã`.çXVÈ\x0006wå¢}öÜ³W³
-çåó\x0002t^l?igø5Z1ËqaD24\x001d`Û]\x001ePtëµ,Ç\x0015fyèöÄã\x0002¿QP­\x0012\x001c î\x0010\x0012®7²ÑÂ%Q6§á`-õ´ÕÄªæ\x001fåÕ\x001câ\x001e­Ö'ég0\x0018®§\x0013Ó\x0011§\x001eå^¤\x0008ö¡/9Ñ\x0004ýÉég0à¬$\x001cbÁj]à,z\x000b+yÓÏP.\x0005ÚÚÂE_\x0012x86ú©'­xÁ°.\x000fÌÇ¯qÿ\x0004é>+¼\x0005L£vÔ-*Rà\x0012tbÞP\x0006_ké9Ü${\x001b¢ÚÀ°©Þé\x00160Ú^\x0007`\x0018¹c0Q>¥Cºjú\x0003\x001bÄk
<´ÀMàYêÃ\x0015+%$~OiP\x0018¦Á`ø\x0012¹Ë3r'îPØ\x00169l\x0005[>^¹7o·ªÉçË;­V°Â¸çN\x0008*
Ò>\x0018®±LqÝ\Ï\x0017¯÷qmû{À,\x00189ô%\x000f8Ý"S
N\x000bH\x0015ö\x001eØ\x00100´æÒÏ`0KH`.ä\x0000&X;\U#å,\x0007JÓÏP.ðòØ\x0000®d Ð´\x0011 j3\x0018ÎU\x0003\x000cÏJ·\x001c\x0018\x001cSÚ¬\ÉAO\´]\x001d7ë½úh\x0000Á²«ô3\x000b<Æ<4\x0005Àrq©\x0001G$Ë|\x001d§Sá\x0012yÔÞÖ\x000fÅÂ\x0016\x0010f\x0002\x0003McB\x0016¤+õÐ8'û²¶\x0003È\x0008~uÕ\x0004%^<{úîñÃÎ8PPöNÑ´þôZ\x0016C¬Ûà¼ëâàôÇ\x0017{Á0ynm\x000b\x0018ºÛÜ\x0015nÉ\x0012óZ°Á£c_¤´	,
\x001bL?ÃÉ\x001cÍ\x0012Á
ö$6Rè,°3)£åÌÒ"ô3\x001cÍ
ê\x0012Æô\x0015Õ\x0002ýã=«¾\x0018ý\x0010´;ÿñÃ¯õ\x0014Q&ãà.8lM ¸¨åØ\x0000Ù\x001cÏ¼÷þt|r²8ýa/_\x0019ÿÔÀ\x0014*LÃJÕ\x0007\x001f¸Þ:t¿Þé¯\x000f¦[Ôy¼¸]~¸¼¹Ú\x001d²\¤MC¶Ï¯¿0±L?^,^<=~¶°\x00042Ú\x0008q:¬&BM¥Ó`åZþÞÞ7öã½¼KÆ\x001aÆiÅzÂ×ÓûÇÕòáá~Gú\x001c´¸\{Kà¢bd® ðAîæ{úêâtqvöª/o¾æK¥\x0013Æ¶ñÅ¶J|ÖP\x0018ÔHWÐÛÞDo+E¥~\x001aøp2Ð!%aÉ'Ð8Ê|j>>ô\ÒO+\x001f\x0019ä\x0001´Y\x000ex\x0000 7\x0017ë\x0003£©ó$ý4\x0001`QT¾Ãos:\x0003G\x001cñ	Æ^\x0001Ý\x0008èDÝF@°~É\x001eÀ91?aáX¹y\x001dûò-í\x0016\x0001ÛÂ=6\x0000çb
áÙbñNÌu\x0007\x001d&´ÓO\x0013 ¶[Ò\x001b6\x000eGAæ49û÷>I­y\x00001~Z\x0001)\x001arñ[\x0006d¾þnÁ|þî÷Ï÷ª[Ås¥~À*§g·÷Wïöt	*c¨ûÊ\x001bù")å\x001a¢ß\¦YS?`Ó³WÏ~ìï\x0011\brÎ1 ÊÑü\x001d\x0003®¡Ò!Ã\x0002Ç°û¹´¢Õ\x001bí\x0018Pl¼£¯j\x0000+#:ô\x001a­ã@Á¾n\x0004(&h(\x000ce°TØòéwKÈa ×òvySÕcv×Ü}ZÞì\x001aZE¯L\x001d\x001f¨\x0010\x000fää:×?ïn9yy¾8î\x001d^Õaüf0î`Fªkó \x0018±Ì ó{tM\x0013â7r"z>F¡wb´%\x0018ºGa·0VËÀ3Â÷UÌ\x0018Ùo\x0011\x001b\x0016´{Tb\x000bcÉ·1:\x0007ýc\x0015sqã\x0005\x0007ü´êm²\x001bXKõÁX·Cõ\x0007Bl^¨Pª,g\x0004DÛ¶ý\x000cÍÚ?\x0005\x0019ç uËïE«}þU\x000b#¼\x0015Ûþ^\x000c-¢ÅCTR\x000b\@F\x0003¶&1ñÝÝeÒh^tÍ¿\x001eVðÏ¾¾û´[«\x0012\x0017×A±&¹w\x001a(Õ>­ø¯ÅùéÑÁOG/ÏûDø\x0013´í¨Ú9q2\x000båGSáoàFÎ\x0011éÞ\x001e1I%È®R\x001c\x0008K¼ÒòTMï\x000f}=\x0008Ìjø?fäTXó¦´\x0018Á	ö$m¸'6ÒÀ¥R©ìü\x001f^a\x0010E1\x0007j\x0005yc\x0003w£GQr]Ñî~ë \x000eg;º0\x0002TêÒ-é\x0014w&\x0007ËõFìñ&\x0006þú2\x000f?×\x0003Oï?|¼>x¶§ªÌDV<
¦Ò¬%V\x001bP§¯^¼>:xÖ[F¶¦éNÉ\x001d\x000b.(6\x001bÒÌô\\x001dÚ±yzó%mdU¶\x0003É4{]*ÏïÍd6n\x0013È0I«dÓ'4%ï\x0016#×«õ¬ÚÞ¤\\x0013Yw£è@2\x0016ºP\x000erøNÎ\x000cÕÛðÔHÖY':øÌÈT\x0010k%\x0007I´Ö½E\x000fM\¨ÌiáÒ´ß\x0014Á\¹eBYºýÌ\x0001d«ë÷oß}þÆ|y<8¿þðqW3\x0010æsl)8\x0016n\x0019@)¿¦·Ë¶°\x001f½xÝÛ\x0002ôÅÜ¹ß\x001f7eF*ØÆD·{ôkz\x001986»F[L?³'0|Jc.Nú$ì\x000f
]­\x001bùÀïpd;;K¡\x0017µ.OTîÓ\x0002Ãù0Gm\x001aùÀÊc½/4
y\x0000¾b \x0018»Oï\x000fæÛ)
âs«\x0011²Õ.Vi»Çk Û\x000c$
¢\x0003¥EõD\x00040F¸¬QÛÞÞf>\x000cXûV>ÓáS\x0014Ñt¼®	ùÌnïr/ßÇ\x000f\x000f¿\x001bìXæ~~º¹F´\x000c\x0014¶è\x000b©\x000c\x001d$\x00064¹î%Ï\x0018ÿÙgËÇ«j\x0008ÂOÇGx00÷Ìõ\x001f$û\x0006\x001e\x000e\x00167;GË¡°vTÖ¤4÷EYÍµØ?·»eàì`qÜ?Z\x000e\x001d¸ó²õ\x001f<ñ¾^?¢óù:1íTwë²HÃÉxPx,TÐ}ÆKé\x001døçÑ\x0005ú¯Óî\x0006Öª\x000b¹Ø\x000b.DWÖP/\x0018V|ÉÞQÄº"Öcçørr]ÛÌ¯LEßW~7ØTÄf\x0014±×kb[\x0010l)\x0013¢ÏØ\x0018E\]c3ê\x001eûÒ§°å\x0004æ\x0012Ç6bzy²þ²Tèñà\x0019x}»' µDI$-x\x001a¶<Ó\x0016ì¸þ>
ÚY\x000fî^ïÜ\x0004\x0006²\x000bX¶£\x000c#ÔTÑäq­\x0004Õ\x0018ZÅ\x0015Éà\x0018öVµ\x0010úÐ7\x0011FnJÆ©Ô»\x0003`ÅâìÝÁÑB¨t°lf\x001bDuº\x0010\x0006"4Ò\x0015Â9¾²µ]Bk\x001b\x0008\x0011¿²2<\x001bÁ\x0006©êßåO\x000f%t\x0015¡k"TKJµò4gDÛ¨q²Óã\x001fJè]Ð»\x0016BÚÞ\x0008-Ap"pÃÚ9^J¨^Jhy)É%BÍCå@½³wáì®ÐÄ@@)ê§,\x0008-õV§©9PsJPûÞªÎ\x0006<©jY¨Zð@a\x001bº`m¸Ò/U«½½M±FM'\x0018i\$¸*SG<\x0011\x0019!\x000e^ê\x0012*Ñtë\x001c\x0016'ICéÎ~Ú5ÔY£¬\x0011µèì'KCÿüß»f¬åø"¿\x0014PÜ·T<¡ØßèUÒ/Ï^õÎVcFeºuÊr?£Ñ´õÀ£M)ø5;¾±¿¹ª\x0005ÒT¦\x0011RC¡Ë¦_\x001bK\x001bèµ\x001dÛ c\x0005\x0019Û UÞ%F\x0015¡9\x0005%Éïû{Z mu¶ñ$q3\x0010%Û\x000cí\x0019\x000bÅNôvct\x0015¡k$òÚ\x0008\x001e`}Q;\x0015ôPD_!úFDa\x000eíZ\x0001rwÝ:oåfùÐ¡b\x000cmà\x0000rWO@{ÒJÏ\x0005\x000eÁ\x0001\x0012«Bº\x0002Ò6JpW,[;ôÑåBºþ~À&ÈXC¶=l¤èñÐ3ä: 5õÕØMUcªyvÿ¸Ú'ÁMùÒx\x001cn)×\x0011#Zý|Ï^]î`³YÅ¬Ù¬x¢*5¸oa2·BãÎ/¨Ò5Ò;Øk}~;Ö¥¡Ë²áüýÇÎßóÕòîÍ^-Íy#¿î{V¾\x0004&z7º!ßóÓÅË\x001fö±u">Öþ\x00006§Ù\x000eSA¯[Ë\x0003n2©ÎÍ\x000c?7°À¸\x0017æu\x0005µÚé\x000ebëè:\x001c+`\x0006³Áô¾DD\x001cÇJ\x0015Þé\x000ec«ÎÍ6\x001boIY7Á«XGkv\x0019×Øè²91-rjFõ\x0004\x0013³Î»õÏL\x0018Ìf+6;M(\x0017Ö9°ÛTä1»Ìéal®bs-çÆs$xí|l,BÌN§}\x0010W]4¯ZÐ\x0002\x0007e$_g|É\x0017ÉO¡c\x0004 [\x0018þLe96å\x000fÕfHØöw`\x000eF\x0015ZlnåØx£\x0007ú%µ30-TÒ-4H·Ò\x0018¶\x001dvµEò:1ùºJº&­ y\x0002§Í2)"\x001aC&²ÅJºÅáÒõº¤Æ®Á¦«ÒX\x001dZl84_ÑÑ\x00108ÃêS\x0000>Y´ÅêÆ7jJÙ#\x000e¨ã¼Y³í
\x0010\x000ca¢z\x0008i\x0003ÏP8Ëã1°d\x0007ÜÚârï\x000cÚïaóaÃ,\x0007Á&×1ªS°Ì÷\x0018æG\x0005+ëÊ>hÉWUX·¨N_õ­/|¶â³
|ð\x000c,OÊ ÏÊ+ÇÁvÛ\x0013f\x001eÂ¦ª³S-g§!:¨\x0015ãñ0¢¸/Ù1ÏT|¦Ïp\x001es¥rªÙ\x0013|\x001cD\x0017*ºÐB'0þÄsv\x0014¢Ê`¢\x0018ö¤9ðu%üT®\x000f×äKè\x0003Vç\x0008Êº\x001ff·K=/V|±O\x001dßØÏÁ\x0011R\x0003${-\x001aøBu~¡áüàûa¿4:ê\x0012Ü)×Î°É>¼°\x0019\x0008¶+øÎöÌEÚÓV,\x0001GåyÄYÙ"÷ßÙ®¡°LhlÐØ\x0016BµNU
½~!ª8a;þÁ®"tMê}p\x0017¤tbµ¦Æe\x0003`ÇÁ\x000ek\x0007{\x0018 tE÷\x001fk8P\x001bK?Dïj\x0016BW\x0011º&Ba×Q\x0000KÛ81P»&ã#ûê¡ø¢pÄ³.4Ò\x0011÷]\x000cªÀ\x001dL\x0018+ÂØDX\x0012\x0006j=ªÖjCµ;x7\x00100TG\x0018ÚPwR6rXS¢³º@Úp@)b-\x000cÐÉL\x0015]"+eAÜ\x001eØ1\x0017\x0010±c/\x000c@Ä\x0001\x001cki\x0013\x0015ÅhK¼Ìì3h\x0006!\x001aY!\x001aÙ¨BñCp\x0005C~*Æ­\x001bîÆßD%þýÍoauÿs§¾^\x0000¶x³º¾z\x0007h^$@%ñßõôzõ°¼Jõ¤Xá7{	
0OÄó&Æ<­ÁH%1¡øää\x0008°NÏ\x0016Ïª­_\x001fNý¸\x001bº[Ù§Q!^ÂñåÜ$°©<eÜHÿ4¶táÒO3yH\x0003À¹¢@Þ`ÀØÒÜ)lR¹4\x001cÉùv8lYJ~=\x0015H§¢ ¯j=Ö~¡û°ÔwËðsgìíéru\x000b¾/îqÛ\x0001\x0017\x0005/óóRj\x000bÿ¼Å]*	N¼ß
÷tqz\x0002Þ/noÛÃ'Óð¬üÛJ\x0018pbXÁëÑÞÍÑG¬[Ï
\x000e\x001bçrË×4Â´«N\x001a;ÐåÝC\x001e=l«\x0002¡ÔLhÇ\x001fá¯Æþò>Þç÷jø×åí®¯d)±\x0007\x0002%hüºÆäiö\x0006\x001b)t\x000fÚ³\x001f\x0017ÿ¾ØÚÓ¥J\x0005é§	\x000bÔYÚ*[#ÓèHÄÒ8S6]º }ßíÄzsy}\x0013óp\x001cìüÛÝ\x0018~»ü|}»|ØÓ\x0005S*Ï"QÙhöNÙìW\x0002b°
íì\x00007Û\x001e,¶ÇwéÒ¢ÜüÛD§@zË<
ÎãD**H§}Þ¼®£Á5w\x0013é"ÖäßV:)ó¾0\x0017\x0003\x000e\Vùì\Í«ÁÜ÷=/u0J\x001a?ÿ6~Y\_+3\x001dhü\x001c1ð\x000eNèd*g\x0018EwóU]É_Q¥{W]»\x00177«å´¨~ç½ÃdIJ\x0002§¼æêÀbÕ\x001f]ßxq|ºxÓïÃSxwÓO3^ÈË´q.
ß\x0004º\)\x0007p¡×.Ù\x000b÷ñá\x0006äP
Vmîx}\x0000CìíÝõ®¯\x001a¢ô¹\x000f5¿>:%AKVýÈØþU:~þr{3KKaT@f0k°\x001f\x001dÁU¹*Îã1ÛK"\x0006Ä¶Hm\x000cæÊ
ß¹©¬\x00119OãJS+ÒO\x000bWÇ®WÒ	X:J\4Ë\x000ft7½w(\x0018®S±\x0019Ì\x001c®\x0002\x0017Çä³_c0\x00047
5púiûÞU$­\x00149¹\x0008XFÓõ
ºÏ\x001cß\x0003öþáóÝÝ=EïÔkÅ\x001e\x000eö[»Þ¹<\x0004\x0008ý\x0004Ú¬\x0002.Z~®~\x0015D;mÝ5\x0017\x0006vjæÂõõL!ym´ s<ÖàD\x001b7W¶ÍbÜ\x0014"rW\x001eql¢y?\x0011gá¶±áH1\x0011¤òå¸ÂT*vD\x001b©<mãÂ}/áÐf\x00179ÜQ\x0005`Fi`©Ì=ý´Ê3SpkZ9N\x001f\x001cdeÝD2ÑOÒO#¶i\x0019
*oÐ\x0000Ì±\x0004Y­F]ýêä]òMh\x001bngóÛíòàÕòËN£BÉÈW\x001f»¸mö\x0002"ó÷¶sa9ß\x000f§ë³):`ð¿Lµ©p(	Lú¼Ýc&éØsù\x001bÀPê81\x001aÇ\x0004`6)ô\x0018$]k\x0008'aìj\x0004ÏéB\x0000\x000b¹OÁç_\x0006±çî7¡\x0014k\x0007ÃÚ½Ì\x0015]\x001egSmsü\x001e=MÙs÷\x001bÀ@q¸f0\x0019h_5(påyÌIG\x00023¾G\x001f5á\x0016¦v0Â@	LE6xÀöL6ýÄòn¾V0ð<|Öà\x0016«lóíW8,ÄØcZ4åqD­dÒ\x0000\x0019®f¢I9\x0018$\x0013?æ·ÖØ 4Gñ=ç|\x001e<å­¤ºB\;ýeòpöæS£rxj\x0014&îÔå{êÉh4¥õÔ$mÁ-|4!\x0003£¢y[¥ 7ìd4\x000c\x0015´«\x0000\°\x0005\x0003e@ñZ%\x0014»2L¿j¸©Y\x0007h¨ã/[²JgY2\x0004QN¿jß¬p\x001dö=]dÑáLÞ\x0017
ö¸Á¡\x0019;Yoò®ïñ¦Ñ4×Öïétî\x0016\x0007ON(Ü6Ð¨É\x0014#ðfúûÄO³*\x00088NO3'uNËãU+am3Ù@ãp{ó÷4,ÔàåÉDð7Bð¡\x00197ùÐÒn²fU"?6_µ\x0010C.XÁï)ÙÓ\x000cbòUãap­hQ±
v¥àæ«f'\x001b\x001d¸8U}ª÷ë6?P\x000b¥áÔ¬Ã½M9\x0006dèÔ¤Q\x0001\x0007euÊå[ð@EÌ]G&×º@ÄéfÇÏ7\x000fÉôÀÿlý®vUb\x001c
Ìà¡\x0006ë¥êÕ1×þwá>m}§¥²`§ý\x001d8¢\x001dÁ]÷ä²H\x000e\x0008)¥·«Q!õ|\x0000ØæS\x0018\x0006\x0016Ô\x001aLäé>Ok$0±ýº5ÑÀìV°Èï\x0000ä\x0004ÐpX#G^ÒÒäI`X ®]3\x0018XÜ,"x $;´ÁìöW0\x001c\x000c\x0007\x0006Ð\x000câ"Ë[Ôò!
%Û¤õÔ\x0013Ã\x0011\x001eV7¡uFÒ«\x0002æÊ§4rû³l\x0000Û\x000e\x0003S&o(öi¸_$0êÂ\x0013ë	
\x0007Ã(o.Í'[Ñ[\x000f\x001c¨5=Á½\x0006.ø~Äôä§à°FGçå=K1Û\x0013§\x001dÎµ¡!¶s©R\x0012\x0011<Ð,Ä¬zÁ°a$Êf.-9\x001e\x0004\x001f/oIAo80×ÄÏ¶¼¦6.\x0011¨¿Þ+aH\x000e'W/i)&\x001eXòXÓO#\x0019hÇ\ô\x0005Çæ¢/K=ëÀ¥{\x0012:¹,Öá¦Æ/)\x0003Î¬L\ÂçU\x001d(*$¹\x0000*µb ûüæ÷ÛÏoºÁ \x001aVeh«åËÕ\x001esQr\\¦dÓf3²Éb}Çh6åÁâtñâéöbÿª¬h¢
2·é`Í£É#ÜÊyørÃm¤©ØFë6,¸\CzhìPt|X*->5aé§
\x000bÃX
D%\x00052B,i¹\x0010h+\x0015v¦&*\1M9ß¨E®ã\x001b¯rL\x001b\x0008Çc¥\vúiÂRBæq:ø
W©.ßPÁÒ\x001foÿxÿ®ªW-kYO«åÛÕÞ+rìB¸T3\x0003¡o\x0008BÖÇmTèx.÷V
®±6¯Ö0,\x0019ù\x001d
\x001dóL\x0001ìÊ <c­DMh¤Â>å,KãQÅ¸³.RþFx)'aY¼ì¶sã\x0007a9PÖ!S\x000fF§âª?ºïàêiÐ¢6L?mT¢bÂYZ/íÝ\x000eK¦\x0015ô\x0013°<ê\x001cßQ<°¬
y\x0012»Kns¦K+É\x0005Nn\x0015Y
Ph7KÕ\x0008\x0005ÿò\x0002¥òæZ ¢\x001c\x001a77oU;
X8ùZ6^,¬9õå¨l²iÒN*:«í\x0002k8T\x001aÇí\x001b¡¼ò¹µ\x0003©\x0002Õ&\x0018\x0015nÚY}üúð6üò\x001d\x0003çé§`-?ß?®îÒfÁþNC\x0013W½Ò ¤S¥wÒ-omÏ+<[üôêâôåö5\x001842´y¸òÆg0ãó\x0018Sï\x0013z&2)l2\x0001­hEÃíqÊ\x0012c\x001ek\x0003/Ôr\x00125ZÕ##\x001aÐTBSÍhØºáJÉdv\x0019q\x0001\x001fgi\Ï5\x001bf³j´Í7M¸áUArR\\x001aGÇæÒ6l!±5_6åV*\x0001¥fÍíÜjÖ7 yÇÐB\x0000×?WHðµu.\x0002s¾¨5z*ZÈ\x0016k¥À¡	jcÓ>\x0007À\x0012©6©_4dÇ6´Þ¶\x0010$\x0015la¼+·t\x0002\x001au3\x0001ú\x000eàÃ$²ö\x000f¥*Ð8\x000cf5T\x001có\x000b¦¡áþó'ù·
Í¹Ò<*bóesVr\x0001±\x0011\x0013%Â'ù·Í*Ç`	FZÌÍs&\x001e\x0003Øf\x0010e\x0004\x001bÖqäß66Ðã|n`ÀRm¿\x0001õÎÔT¥_ù·
÷TE\x001bu\x001eÎë%½\x0004­íÄë\x0006P:¡éf4x	Ô(\x0014°\x001a)R\x001a²mòaâ#Ué¾æßF4ï1\x0019ÐàªûÑJ \x0006\x0015§¡YÒ®\x0019
®?ç ¥æ\x0018±\x0014iñÌ$2ÞIþm#ÃpÄ\x0007f,sa±ÂIBY|X1õ¦\x0006£üÛÆ&\x0014?Q\x0011y\x0010îãd\x0015¯ÕT±«\\x0012m®]´Á\x001få\x0001l¸Ñ»ËF\x000f!¯¸Äöóäß&6ïÀT£Ä 4T`¬\x0010Í\x000f9QÅë\x0014ØÊ¿hàèù!¥#«MÃ%T¬\x0011ÂD\x0017A+Ì=çß66©\x0008:6\x0015¨OcÐSÙdbk½n Ðõ!E©%×\x000cj°à¸]ÙÆéh:¡µj\x0004oqÖ4)+\x0015Ó\x0004GsP
Ð¶/úÒf\x0013Z«Ø\x0005×S²\x0000	Öø\x0002[(Új³e0Ûõ[ù¸íV;ðXßÜ\x001bói§=i\x00055´¦¤@\x001e\x0010¥&i£ÆçùbgÂ«ã¾Q\x000c\x001d*ª_i£2®\x0004ÿ\x0005ÙMê\x00159
Å¬­TZQ9æ¸S(øPò7ÎN£ª6\x0005\x000e>+gÑ"ÍûPð¬l,Y%7
\x0010\x001a©°*\x001a%"\x0016a8n\x000bå4¯ÙLß´QIÂ/Í×Ý<\x0012\x00143\x0012>OÝ\x0002,Ú[U\x0004ÎJ¢ù$»ë\x001b\x0006>B\x0010ò¥|&\x0010\x0014«"RÓ¨R<Èªæ¥X4Ä\x001c\x0018Ê\x0017«4\x001doÔx\x000e£úðÁþæ~I·\x001deigóÏ»?ÿïO×ËÇ	%&¥åZ\x000bþ|¶¦lFÎhIÈó£ÅÅ^jü0\x001eFÌf¥(dMpüåÂ\x001615HâeL?-HÆS÷\x0008vTRX\x0005ÇÝ\x0005.\x0017ØL2\x000faº\x0014ÒSyiþ§XÔÖÃëÛejcþx³3\x0019è\x001dxB2S\x0014ht\x0002\x000eñvì°m4¦¾>Y¤\x000eöç\x0017Ç=©@ýó¿ûpýØé;Iã/.Ó$\x0002I(úÉÓÕÍòîÏÿ\x0007t4 \x0004
q\x0001Å¨Û\x0000ÐÁ=tJÇ\ë\x0011)þôôxñò\x0019hÞ4öâéâìÉÍÝÕýÝÝãuùo9r_Ù0\x000eìòÃá\x001a,0´"ÂÇÃÚHÜC6\x0004ÂëíÕÀûÓðX\x0010#×{ÁQ89\x001a"÷
\x0010iy|ú"ðïEç9\x001dF5Q\x0018ã8r\x0017ÖÀ/âÓ¨ äÀÍ?.sX%#wuãÈ­M\x00039ÒBÈÄ¡q©FÂ0.¨z4\x0006®\x000cã\x0008¾|\x0017¸'6¿\x0014à°\x0004ê\x001fGP×Ò@\x0010yãÜÓÉÃ÷\x0013*ßÅæ \x0016¥a\x001cÞ¢??L\x0016hÈ¡
HÚæ0\x0012\x001aÐyHLT\x0012Gä\x0007ã{>ÌÕòÍò\x00017sõsPÏ0\x000eö$!\x0008V0¸\x000c¢½'1\x0006¾Äø\x0003¡¾a \x0018sÎ_&í|Îo\x0006¤	HHVÔ8\x0010ê\x0019\x00049\x0017´1ñÓDÖÎ $ROñÜq Ô\x00143ìDH68\x0008Ør@4iàÎ(\x0010î3\x0019v"¸# \x0015å²j!éÑØño;7qØ\\x001cZ¦\x0015UÀ¡\x0002«\\x001bÍhm'ÍÏËÔµ·\x001cøqpû¯'çR(
\x001f0mXÆ\x0007¬Ç_WA\x0019"5f\x000c\x0014°ú0\x0012\x000fFúYÒ¯U\x0018}Yùù

«¡Æ?$#mM\x0001ÉÆ\x001901}¤8ô#aH$LqÍ\x00018\x001fúHV¿/uóÌ@¯XÄáÑ¤|d\ßÑV´éhìàû\x000b6¼"á"C*OI6t±ØB\x001co9J¼/rø}Q\x0018"J&,8|u­¤cÑã¿\x0012ü\x001fé+Á¿tøW\x0002HBÆ¥-êI\x000f\x0015\x0019ãF¿#\x0019Ò¹\x0007\x0003$®X³¸n¯e[EøÑ/I$q7TÚá{vàë¤.eüDÞð£öãÍjóó%\\x000e%ª\x0008\x0017C Í\x0015.ã
Ú$ ]¡:òdÂ\x0019¬nQ¤$ßV\x001b?|øeyuÓqB\x0001áÃòîÍêæn\x0017\x0006N§1É\x001b\x00063m\x0007\x0001\x000ee¦ç\x0013\x0002þÊ^\x0001\x0017?\x001e¿\x001cB=Ñ$&Ï/D¨SE3ø¼§\x0004I¼\x001cOÝÀ$XDóy\x0006G"¡åcX»Rû£m$Ù\x0011\x001cJÂ ó`áZú:?Óf4\x0008{>ÃH°þ7[OÎN/G\x0006¿F$vüÇá\x0007\x0003IÀã	H\x0002928É÷Äñ_½¡(!Í§OW6¥\x00113Jd\x0014«üx\x0014\x001ai0\x0010ÅØ4c!¡¤{B±¹l	QÌ\x0004\x0014ò\x0006¢à¬[þ@&+\x001e\x0019tÞÌßGN )cx(\x0012)Î%\x000b7¡\x0008þ>ªÖM(q\x001b\x0002fµÒEÎfï\x0003P\x001cË\x0014c& ?6ôTDJ0#
\x0016/fñ\x0016d¹µJN@¡\x001eâa(
ó{ùªàd\x0015\x001fry\x0008MÀ©_a<Jh:èTPªÙ|*¸Þ2\x0006ª\x0012JSîÃòá²6î\x0013Ï#Ó\x0007ÒüµãQà@Õð·,Ö\x0012ÎrWæÇ¬ÆËÚT3ü-\x000bI\x0015°Mr¼ø\x0010Wqå¢n\x001c0éÇ_\x0015µ\x001aÃß2ÜZ\x0016+VQ\TúÈgºÆPnz\x0018\x0005#2j:\x0014ÃR\x001f÷¼C\x0019/k±:X\x000f7\x0010°ÈÎÄRD\x0003ÎÄC	ãM\x0015îÿ\x001fx(QÐ3ö8¯>qøÀoG¨	\x001fZ,\x0007r`çµÉ(¦<cï"[oÂ<ë%\x0017PpÆ\x0006Ý\x0013£É-.x¾'J¿'¨¸Ìð¯\x0003&AÈÂ
|ô4n\x0000Q!9\x001bâinû]Ø´J¡;¨\x0014¸Cµ²§h\x0013\x0008}Ë0ÅhÒ\x0013d
°,\x0013Ë²Án2ÌâqgP6V$Ãøñ>¡
\x0014T	)¨2ôKY6)ÑævdÈÉ¼'\x0003ÕÐûÛ\x000b~\x0007f¥Uù|à\x001a·ÏÜ79þí5Üú?îï>]½[Ý<|sêXë£ñ\x0018ÚÈ©\x00070kCáÒ\x0006j\x0018ï«dÝ?^½<öãéñÙ9üÁË£5PëïðäðF\x000bÎKØ\x0007§Ôg\x001ebí¥µ\x0013å0Ç÷sB9÷ÞÂ£Ö<Ø\x001e¼q1Ë\x0007$\x0017â4¤\x001ciühdZzÊ)m8LíH9\x0010ÓawDLv1~6©\x000böá8;ßtt2¶òXØ\x0012\x000c1åá§\x0001èiL¨ob29´ÊÓÎHï­ó\x0014íD\x0014¸j"²iø\x0006R0|¿½R,\x0002r	ÿ\x0004&ÊÞ·09OnxÀ5P\x0006à«3ÅíL\x0014Vkºáy&8SL+!ómÊ%mX×)Í4&Jê·0\x0005*- 0d»\x001aï,3\x0019;ñSt«É¥°p:§pHÎi_ilâ0W\x0003R\x0014r}L\x0012ðÉÄcÄá®&$>Wzu\x001ch\x0002¤<þ\x001b_vÃ9îÕÄ\x0014)zn O\x0017u9&3Í\x0018à\x0016&¼Öë\x001b®éÕÅ<Ú/1M»á\x001ckbÊåéÛ¥\x0015\x0014ÄÄß.
³ÂDÑ¹&¦Ø\x0004:E;L\x0010ÖÏd\x0012p®	4rEbú@LÅLQaâ}Â=Cm\x00123bºì\x0014\x0019(-a\x0002J\x0000:'?ñ>Q\x000c±)P¤7É\x0002\x0011É\x0016Y 'Ê'&¶0iEÚ.Ùs!¿» b\x0004Ä1Å& l{ã!a9.ñ8¶¤vF\x001c\lAÂlôZ­8zs:\x0014WMó\x000c8ÊØÂ\x000b\x000cùÍ\x0019\x001claÊãú&0Q+N\x000b\x0013Núç7W8$&ágáÜ0ÑÂ\x0004cÉ©K=&@\x0014E±ÃÝ43¡M@\l\x0010°c\x000e)Òäp<¤0ñã±F!\x0010-9Pàså¨Á¢böÆ§\x001d\x0013\x0016\x0015¦7\x001eöå.åXº¡¥°éÉMSs¼Âë»	X`ÂÞ4½7ãSæ#àtH·\x001bn\x00101¸ó»mï(é Q|½é³IlIâp,>}6~p~¤ä
g-H:\x000fM§$Ù\x0012V³\x000bÓ\x0004%þ¿´®\x0007ûn4\x0005tu\x000eè~?\©`MÇ¦³
i\x001f#é9m¨n
ß]îÄWJ¤/(\x001a±À]\x0011\x0014\x0006ó%H\x0010aÍ"¦º¿Ò\x0016±õ+kª	Èdùj¹\x0016çÓ<\x0004øWéC^µJ+2\x000e£\x0014\x000f\x001eX±\x000eâT{%]/Ûö\x0014cpÅÜT:YçxX±ä\x0013©ÖÅèßÍ;\x0014éóµ}=\x001f0¡\\x000c©\n¼ðå\x0015ÚÎKÊiÌ}G¶ÔFÙ|S°5ï\x0011I\x0007\x0016R\x0004(}C%K°uZ\x0000\x0018®ûUºîßÑÍ\x0002¦7éÍ÷ã5t±\x001aïÕQâåý¥ûò['Çùú\x001bäÞÞÞ<¤vù×yðìzõùæzu½³¸<àîÝ¤´Ï¥÷ ÷
×êº\x0000ìëÜ/ôüäø,õÎ¿\x0006êgG§?\x001d\x001f\x001eõ\x0017zw¨s&ôïF³¥7êSý»Qçå7ê,þ[P¿ûýöN\x000cY|>x±¼Í³}?}Z%êóåÃÃÍÛ»/»J8p	\x00175\x001dÄ(¨þTiÁkZÔ\x001d!\x000e^,2õâüü41/ÎÎ¿ü·\x0001´X¡Ç
i\x0018\x0007âº«]\x0013.íI
A\x0005cæÃåI?SxE?\x000b\x0019)³	¼jv´sò\x001aÌäãÏH^z.×\x0000{4X\x000c5iÊ\x000e\x0007=çmÐ"Åª§àâÚ¬ääx\T%¹#ÝÓíMéÿ\x0019y1h?Sx#ájn6\m\x0007&XÖ¤)uSh#\x0005»p×\\x001aAÚsótDä­\x0003Þ\x0013y±\x0004%ýæ
Óã\x0012·ö1/·rá^ö\x0019yó¤½I¼ÊçpýO\x001aZ&n\x0008*/4ÁÍÊR\x001eSno\x0008X1¦\x000e±ÄËÂ\x0001ÇÍÉå×j¼²p.\x0001ð*¡\x000e©í6%\x0002n¬çwLÄM\x0019%=åxA\x0015ç \x0004î6*óW\x0002ßÞhæ½\x0018O?ãq¹È+isÖP\x0019Ë÷VÔÅ(Sqñ2I!\x001e\x0006M¸!§\x0013¯·Ì[÷ïMã58Ú9ýåZ\x001cÒÝ\x0005CÇÑå×Ä\x0019iS@}ÊéJ¶Ç$»WÈ4#\x0019p­b»Ìú9EÁ\x0001Qég4¯ç<×NóT\x0003k\x0003©6§å²ÁbWú\x0019Í£<ñJOaKÇ§SõàQ¸W_ßßý¶L>\x0005®
í\x001b}
n\x000f°þãúq­«Ê\x001c+§DHU´p\x0003õùMÈ2nô5ø:Àø£!lÙ#neÓ¥£\x0019w\x0001æY_RÑBßàí¡8
§V¶³)CSPÒgÎo\x0007Ø\x0004uÉ8Q÷=dËuÇlh¦ÆrlÔi¬4À±Ípj\x001b{í\x0006\x001fôå:[Ø\x0002YOÞÆºàw$\x001cUý¶\x001bh\x001b¡è-DÊ¾He#\x001dÓõ¤mpËÕÕõÇ\x001ddTûÛJsrÏ´!¤R-\x0019NjÙ"·\x0008+¡¹ÃQÑð¨$Aæø¤ÔáÞ
g5wÉ(iø\x000cVp+ÃÈÓá¨R¹\x0011Npô\x001c>ª 	#\x0012N.ðGµ3^®Xn=8\x001dËC
êL¥¤²)87³÷)\x000c`£Òåïïrenë\x0017ÅÑ¥ùÐÐ\x0012Ì_Tpù¹·nwÊ\x0015º­l oYc\x0019M\x0012\ðEè\x0019®[âÝ\x0008õÕ¤³À²\x0004'©ØÛdîH8ªEmÃM$}?ÌÂW\x0018ÉúÔ¹\x0019Ø¸\x0004´ùàTz\x0000È&\x001dÕ9K\\x0004EpÖÏ\x0001Gmp&ú2=Bâðñtr":Ïï!Ì Dp¬n~\x000e\x0006ÇBÓh\x0018\x0011-\x0015«{L«¸#`\x000e8êFosê0wãRgé3\x001b\x000fhñv\x0006º±\x0002xð}\x0013e¯ùëâ}\x0013üE­Ã¸ô©ËÖ?Y6«\x0006Ú±Ô+f9?U4gÁ»JxWÍ§çí¡ \x0007¡\x0004e\x0016¤E­{'Ç¾ÖT¡Úï/ùº:µ»cÛw£øÃ§_?¼1Ý©\x0000ÿz\®>\x0001ÔÁíõÁéãÍÃC¦Þ¦££\x001e\x0018¬×¢*\x001bi%í\x001a6|Õ],NÏêàäèàôâøì\x000cGª÷¦;Õ¯¿ÿq×I\x001câwìöþg÷b¹ÚÝ¯&¨S\x0000+µ¸"Â\x0008\x001ef
§Z+þ4@îÅk<¹\x0017Ó\x001diØ5\x0017\x0005\x001fZ¸µi
0r%«\x0003U\x00084éOÕ
\x000c£¨rÑCÛiyC%xXAF1Ú\x0011VÝ2+5´q\x0015Ï9âÆ<þ\x0008°ø+ª&«Q\\x0014¦iâ
ÆDôbrþÆ\x0018k\9¯0+'ù¸p$+°ÛS·¹êYÂ£¸(<ÓÄ°Ç2\x0015Ç\x0002\x00148[¡6\x0004ì\x0008(nÂn£·\x0007*ÂWTÜ&\x0003Rm}ë§qì£\x0019\x0017Ï\x0003E°ÈÂK©É`4È¯
,¨C:0Pêt½@xðaòõ*aV.Ç`®\x0003f´,'ßÞ\x0004\x00062>WUà
ÐT\x0010`§+1]NpÍg*ùl\x0013c&-[ækFRL¢#ç®h6bÕg\x001b²Ù\x0017H/3»íF{þaºL\x0003qs£àç¾v¬>%S\x001b\x0004?ë#a&[\x0015R'?@·¢á$¼Ç\x0019c\x001c+§
ÁÜ\x0008¬®ÃSÍ:¬7§éDùÔ\x001c«K5ã±­'t7\x001f¥/ê4O¾°6²L\x000baº¡h¾Æc»nµ~¸Ä	7\x000b¦òìdýøõmü\x000e¤LÇ&ÍR\x0018\x0017KéqqÖP¾\x001c©	ì7á¦cö\x0003ÒÍ\x001f»Pà\x0014h\x000bÇ-¼IYj\x0017ËH\x000eñÍ¼´ãÿÑ»ç£û¯ç1ëÿ5\x0004}\x0007 ß<þñû*Ý\x0004\x001fÆGööÓÁùÍjys{{ý¸zÀOtµ¼¹ÛYå\x0019\x001d§¹®\x001fÌæ4e\x001cÙ$\x000fv±Étª?\x0001ïìùùÁùñéâøääèâô\x000c?Ù«gãgÛ]É5³px\x001c]§ÑÔ¸:·oh#\x000f3´
Üo|üævíÞÖÀ}ÜW¹séFÍmþ+¹/ûòïvÞ\x0001ïIzOlirÕkO´+ýÒ&ÔÝ\x0018ó_!øÄòß\x0002~à\x0013oÊ_\x0005þà\x0004èà\x001exþxýåÓNu)\x0014¥S\x0002\x0006£Ø
IaÛ:dÏ/þí¼W\x000ftþõ9Ê³ÿ_¯\x001dw7§?Å*hELÚÔnnþ÷\x000føã9ÿmÿ~vÈþb«·÷¿?ÄÎ÷?Y\x001eÞ\Þüù\x001f«]­Pik Ì¡\x0019ãí¨8ÑYò7¬àÅÁéñSla\x0018BBÛ\x000bÿ»HníÇxÙ¹ÏÞ]¸¹+] W÷·;p¹\x0008õ$(Åq\x0005¬{¢x-Xp\x001bs9^\x001c¿¤Æg¯N\x0006ñJ&2-¸\x0007Ø)Ü\x0000K\x0016\åêV¿Qd¹×§õÌp\x001c0ß¥ @²ÔÒ®Ãïj\x001cÙýoï¾è\x001cç\x001dø¸|H}<\x000f\x0007Õûëf¸Swdzx¯ä½à.\x000cî°uràøÅëÅYêß9;Xþðêø\x000c.\¿\x0010^#òï\x0017Ña;ý|wrå>ÝÛ$ß·\x001f\x000e\x000fn\x0001òüþñöþñay·³cË\x001fÉÁp1\x000f­Éº¶bSs\x001d¯ù\x0011®à\x0013`<uqòêâlñrG£Ö\x001armÃ`t<ÅãRÊ<eOûÒF\W÷´\x0011¾»½§¥Û$dþyÿøöv¹ºÞ¥l\x000c!\x000f\x001eÒBõNÊh¬Ùª\x000eí¯.,Nú5S\x0007#§\x000eaxÇW\x0003ã(¸2>7\x0000\x0001©²8r5ç\x0010\x000e Rk\x0016\x001a´t zbk8#Öö5G©´æ`u\x0018\x000e\x0005\x0004gÄqa3\x0005¹\x0001¤.Ùl9\x0010®ê\x001b\x0006âsaP:\x0011A#\x0015R\x0011\x0002ÀÇ\x001b}"\x0014e\x001f\x0006=ø>_\x0011\x000chç\x0003	¼jc/L\x0013\x0007U\x0012\x000e<\x0010çò\x0003Õ´IBá\x000eD~2¶çªî\x0007\x0001Ùr²åfè%±y*\x0016"\x0006\x0012yÊ\x001aZwU\x0004jô«)bn\x0018õyM' d£\x001e(ë\x0005\x0008b¼ q?ÿ(¿\x000cD\x0001ãMd\x00148\x0001¾Á§Êù¢bÒ©P@aà\x0007\x0012ÙÈ\x0005\x0014\x0010't(¥ud·ä\x001aI®
6s@@9YO\x001d4f´<YG\x0006?dE\x001bÖ
\x0012m>2ÊxÉ\x0006$oäÍ@­\x0003&+\x001dLØyzÉ4Ù\x001dgÆâþ¿.ßVáY2§\x001f\x000ep`ÅòfàQéäÔ\x000enR¥`·ñ®C]Ç=}vS+\x0016Ç»,\x000e\x001dïøk£s^\x001cZÚ,.ÊäD°«(®
vÿv?d\x0008ÝÇ?®?¯~M\x00057iÅ\x0019NàL¾¾¹ûó?w9!Î^\x0012d¡á ðM\x001d](áêÄ+ø¯\x0001¥ß÷øõóê÷ðKç3þ¸üp½|L\x0007õz\x0005þNs\x0019s&&wW
Mõå`LðÎ#íëE?.^\x001c-.Ò!½>\x0005¿ÿ>\x000cË»+ÄÂávJ?\x001c¼ºÁB¤]\x0011x\x001bBL­Q¸é<JÆ«tð$\x0011-Ü°ê\x0005¬vÀê\x000fÄ¯apbWTÃaPS$\x0016¸Öé:¥\x0015§\x000c\x001b\x001bd3Ëû[¹úèëhÈO×«=÷\x0006ô¤æ=%p¡¹\x0008Vó\x001aãf\x000câ§£S¼8}¼\x000b\\x0019Üq:%?­\x000eËæ\x0005&¾\x0013ñ¿¾{ß­íº}?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=a\x001c¡)	íá_>ÿöÿzyøú\x0005\x001blb¸\x0006*\x000c¥*¨k	Xv\x001d}2¤÷,PÒ\x001fti.ÿåó\x001f/o/?¼½<$?ÞÜý?·7××K\x0015èè¦\x0011Ô%\x0017I1ª×\x0014÷}"
\x0007}í¤£÷&Ré}*e¤z(2\x001eH)\x0000\x0005\x0007yí £×6P\x0013VJ\x0004ÅÊ\x00165
ïéã2a?ÒÑf\x001bitÈCÃÃòFÌ§
¤4;#©\x001d?~üW¹nRíTE\x001dc³Ô%¹¿HZ\x0008On'\x001d\x0015%4~ýa!\x0013©Ç²ôõS¼\x0013I\x000b\x0001Êí¤£§¼FRªöq\x000eBiiM=}½\x0014S´âÜ\ö©°ùëkgÔº\x001dQ©+©\x000bÕø¤3¨Î\x000cE±\x0011ÕÄ\x0018R&Tã7þú÷ß~þuöùû\x001e'W¾¼Pkê)T\x000cÍ27i;,
¨:è¤É\x001c¿¾PGwêõ\x0005Î°¼½\x001dÚTWÐN\x000b¤Zh¤!«nx6!Ñ:²ªX`\x0006{Òßï[×®½\x0016§ÎÓÚ\x001a²¬:TvOÚmm¥MJ\x0003­v8\%Ñ\x001aÝ\x0013uZñÕªÒÓ\x0014nZàÆüá¦5{ÂK%\x001aaIØ\x001cNÔ;Ä*Rgsd-Jèv+Xk¢u6xÄ¥ÅI±´gUzg¸Êîi\x000f¸±\x001b\x0017\x0000A°Ê`\x0006âzÔ²#n!¯»\x0007.58vãOå±n¨RÑpi÷´^ÜöØ\x000b±¶5	\x0016U\x000ctI7\x0002k\x0006á¨\x001bkÅ¥^Èn\;h".NûÒé Å@pÜÕq'âÕõ>­.
@J^]Þ¹Anß\x000cßÿò÷?ÿõkáxKÅßÈûòüø7Vÿ½xùy
¸ÅBjM{Øó\x0015Ì\x0004\x0017È iéæ\)ÿ\x001bÑoo®þ-I\x0001_Ü¾Y÷\x001b$g¼Ço\x0010\x0003\x001d²q.\x000c]\x0007Ão`@ñNÑÿÿü\x0006é¶Ë7P\x001cµÙ0
¿\x0014µéÙ+[ç/ðô\x0017ûýëÿË¼yýömÝv÷(b(\x0012±ÃÜàH\x001c¢C¤{\x000c\x001a7w>\x001dÝê\x0005å(\x0015ÒB)5»Hv>@\x0001##´ÇÃË\x0016ÈQØÞ´.=QDH¼\x0008¹´R:^ÊCYíVÊQ¸ÞDIµ¢N`±ð*}pO×5/Û·\x0016ÊQÞDéÏ!/e2Âq)É\x0012àRî¶+GÑy\x0003$9H·\x001e1ò¢\x000fNâö 7Gï\x0011-£X·Ò«ô\x001cC
R:\x001d,Sî¶0l=f@Ói\x0008Óq\x001b¼£¼\x000bv¯µ\x00044-(·âh1\x0003\x0018(ãåÅÜëOâOo\x0002tÆÆpføäVóÆtÇóÆ'1ýËëóÏs®çÓã¯_ï¿½{yþöóó·ï+|æPºÎºôÃü¶\x0008ë¤â%
E\x000fÇ\x001cì§«w\x001f.>½»½ùôææÓÔjÅ<rD\x001dÌ^¦ñ\x0010\x0019[±\x0012r>RA\x001c÷G\x001dÈ#·Ô³Ìá<yP@\x0005COÈt5\x001fÊ7wF\x001e\x0019ÖUöd¹¢á\x0017Xò70\x001bÚ\x0019ZHut\x001bw0Ìl3³³
`
ç\x000cÌ2 B£×ôväIb¡Ù9Ú\x001añîHÉ;\x0007ô\x000c\x000cú¯í@\x001e7t áX\x000b_ÆJÌÂR -
µ-Ð¿(õ­ºú°ÏðkD¾|zº_µ#$[\x0011\x0004n\x000eD\x0015Î\x001a¶on\x0016\x0015\x001b\x000e?DÒ«ëëeBm\x001eþü3kñ\x0012óù·û_V¸¸tî\x0001`P!í[
©\x001a9þÌL*à\x000f/~Xv\x001a\x0005é47¾TÆPk\x0010Ú¤\x0011NX\x000c	%pÔ*´Nóâ
¤ÆÓË\x0008\x00187¨ä&\x0013DûNû[ÖT&\x000b\x0010Aùâ\x001dAbPy*EÓ\x0000:M7jÒÆDÒa\x000eÖ@jRw1ª\x001dI§ÙðÒ?]n@U:Mb¨!Ð\x000bCüøI+rj{*oß:é"lA\x0015N'aìè¦Ë\x000cb'cj7G\x0003ð\x0015¨ðâ~}Vs±íO+ß\x0019vo	q\x001b¨!ØòJå¡;þtÿÓñGÆpdòW\x0013\x000e\x0012E)LA=\x0008\x0008ã>"Bï_·Ö\x0013LýjBÔ ²tÁ¨$\x0011bÃ!­¡Ùi	Gvs5`tàdâª\x0019,óD@¬¼â\x001c:zjÖ\x0013\x000cæZB/\x000cé8i¾!ððFÓW£±èzÀ\NOZ\x0012X\x0000âxÙÐzÂQ\¿~	]\x001a<\x001cWÐ+z)öÆ\x001a>ÈâxµÐjÀ\x0001_¿ÖcølÅæùÁÖ\x0008®fsîxÖq=âØp7,"Uïã*j,¿J«3Pböe¢\x0003qZ(:·©&\x0010Û\x0005EB´"§äq¿²\x001eq|Z\x0008Þ\x0016\x0004Æ\x0006\x0010u6âøg5"+fv º0ÌFÂÉð\x0002ïgHè\x0004\x0017\x0001Úù÷\x000eB\x00125ìØApE¥7(>7ìÄ Ðm2ÿ]ÿ<0ç\x000fußÿþò<£=ùz$\x0002¿z\x0010ü\x0017\x000c]j\x0016³ë7¨¿ÿûíÍâHZù'ñç?¿üÍÔ÷ØÏ\x000f/k\x0003Äà(\x0019.©\x0018)^\x000eEÈÃù\x001bìçËÛ!ÖZ*è-°(NhÂÂr@7Aç7]\x0006\x0004\x0000\x000c\x0002Ï¹è\x0002ØÄåÝ9ÝQÇ fX-A\x0005q\x0018NÏ^¥°(jiÁ\x0002M£
\x001dêPñ£ÓÎñ-ÏÍ?Ä7qQ¬Òö\x0019\x0001\x000bDõ²COÚð\x0019uR/\x0001ìmÝöM\\x0014¢´íúúÆãzIAuâq×s¢\x0001o [¹²ßo\x00023.Í`\x0002è¡\x0011GYÞ`aÖY5±·o\x0001Ã×\x0011Á·33ïf¾wÉjJZúÁhêÇ}j¶?icc¨\x001cÔÊP6Îø (A+»ø\x0014³?.ªÎû±eR(I¡T¹äL£SäLq(1%eÁÍÝ9uÉ©ûVÔR¢Cj#È¬\x000c>Þ\x0005Ô ®\x0003Ô`ß Jw^e\x0006Ý0\x0004uRZJ¿\x0007)MHåM*zPã~ä
U$×\x0006TÅ"ÌæQ«]*{¶i¼jø¤4\x000f\x001e2	&þ\x0005FUs¶h5©\x0018|Q|þõìâË×Ç§\x0015[U" mUÓ¢©üßòVå\x001d3Ñ?]¼}{wyu}\x0017J^èå5á\¥§Qm%ÆB~
Ò-\x001a«F^Uòª^^¯ÒÈt|IR¸ÔC\x0017<¼$9\x000fÐÃ«K^ÝÉ\x000bÑ­S
\x0007g{&\x0015o)\¥*íl®÷`\x0014Di\x0014D%ÁÁ. >IÀ\x0014Yê\x0018Ií´\x001fd}Þz\x000f\x0012.Í¼\x0011=Eè8V\x000eOðô\x0000W\x0007Nö8Ôº¤B3e,ôX\x0010\(g_Ázx«
,»w°\x0013ÇUñ
\x001c\x0005°¼#DØ\x000bØTÀ¦wG(uN\x001b\x0002\x0004[4ÅyèØä¢ckäµ\x0015¯íÞÁú\x0005#°¢í+ig;E{h]EëziÏq\x001cT(åÕ¶¯ð°×òú
Øw\x00035\x00130×@«$o\x00067ûîÔC\x001b*ÚÐKr³i3@(?8\x0000ãkN\x0002¯Cí\x0000Ê_@¯¿P1à¡\x0015F-BêÍWkÞÀv'\x000c¿ná\x001d½XÈ\x0018Q\x0003Q\`\x0017x¯õ­ã³^w¡MR/ÈkÎÉq\x001d*Â/\x0006¿¼»^w¡\x0005iôa°\x000eT6c±\x0004õÙÚ\x001eàÊ]@¯»Ð¤\x001e\x0015`B­ÖÜ;"fë\x0012zp+o\x0001½Þ"Æ\x0007çTüC0R\x0017¼&ÍH\^±×þ­ü\x0005ôú\x000b\x001dÃ\x0007ÉU\x0016·Æ\x0000ìéîÚ;\x0001«Ê ©^¦µCQ¶\x0001X\x001a\x000eµÉÀa»E³ã\x001b§\x0015¥l.6\x0013ý\x001cÿû×5Ù¨\x001b\x001aM
åp<7íAÍq?\x0008ö\x0011½A¡Ç»Ó¸ªÄUÝ¸8Ç\x0013±¥øÌ\x0000¹í\x0018æ,Z\x0017±)M/1NÄ	*7J§Ö=\x001bw\x0019÷î	·Û\x001a»Øu\x0013KT?1\x000bçÔ/\x000f|'Rr6­Ü\x0004,Ý8_êFùÒ÷÷/ë=,gx§OÙy\x001c²È9ÙFÎC~çýÅÕíÕ±T\x001b'LÝ(aÚJÓ\x0000"*\x000cÔ	Ô\x001d°\x000býxnw-«.Yu\x0017+\Û\x0007-PªD\x001f¶ílõH;«)YM7+\x001f174ú\x0013+·JËÙ*vV[²Ú>V EÅ\x0006"ÊçpzOÁ¬ñjçt%§ëã:k\x0010Ä ÒÓ±2Ò0ë¬\x0012I;«/Y}\x001f«XúzÏ%½ a`§ ¯=M¬¡d
¬¬ð"£ïÅçaLÒÜÖ¿\x001c·°\x0016Y~7Îò¯Åj\x0018ê5V\x000eÅõüB¶\x0001nùºÓÄZ»>?\x0000oLy~,\x001eL¶\x0015\x000eú\x0003~9qÓf\x0003þôóã·Ú\x000eà\x000f:·\x0002ïZ3¦h'ð¦=ñ²z#ãfè%Æþ<Ú\x000fRñu\x0007¤äÞs3+¤ÔÀ<m¥-âog×÷¯Ø'ÿm³\x0005É\x0007Í@
ì!Qß&Xv¶"ì\x001d¶È/	\x0007\x0016¬P²B'+d\x0003¦\x0004jFVjÁ-_sÖ±Â\x0015FA\x000c6D¶U\x000fªî°o©åC\x0008NSqã.'ù/Ï¨m$þÅcÛ\x0000Fw\x0006\x001eÛÐ+øÑ'^ÏP\x0005.ñr\x0012$Z½xuÉ«»y}ÒpD\x0007I\x001e\x0002\x001bb7ØãÏÀëymÉkÿyyAÌBüAñÈúéùõ¯\x000f_\x001f_VÝÆòÃµAhàÍ\x000bby3Ü}º¹ûéòÃÕíiR(I¡\x0014R
¿­úsVË\x0010|5Ùb¨fPUª.PT»¥Gkí©aßðìF\R}$É¸TT
Kzñôô,íçÇøÇ×§UÖ\x0004ö
ØKèøÅZZ.¯ñsßÿâúú2ÙÚÏWñw×Gl-óêW÷òj+\x0002@¡\x0014ýÀky½ó\x000c=¼¶äµ\x001bxÎæÀ\x001bh}­Ê¸s·\x001e\_âún\MÊ\x0011\x0017åeÜÙçÔ\x0016\)Æ\x0011\x0018L×ÇûoßîesûÃãï«Lm<_@«\x001b\x0017Z\x0000M.»Á±®3¼¹xÇæö«÷Ç\\x0018G
b8m¼\x001bw­ÍbÃ0¯7ÒC«JZÕK«l®¶¶ì\x0018È\y7\x001b÷àê\x0012Wwãz~\x001aêÚ\x000cñjö\x0010ó]\x000b-¼bìw¬Òt¨<ôõ\x000câß±×sÇ5VäQ\x0018Æµ7n¶\x0018Ã³\x000féÿÑIX(a¡\x001bV°ì\x0010V\x0007Ú\x000c9ý\x0001öhP³V´ªû0A\x0005"imÁ3ílWÿjÚpÕFx9¦ÑÔî7ÏßÎ~?XÓJ  FÚ P«b¸I\x0006®\x001cÓp¼¿o+xõéì§øå®\x0002æ5÷\x0016p­\x0003×ç\x0006\x0007¤\x0016g5K´j{Bae\x001d¸±\x0019\x00062ÃO÷_\x001eÎ\x0006´³\x001f_\x001e\x001f¾®òrs¹\x001aõ3\E\x0006jVBëãõÅÛË³á§g?ÞÅ_àÃÝ¬ÆB
âío\x000f¿?~MÏh
\x000cÁq\x001eÿÝ2\x0018.\x000bÐz¶\x000eòí\x001f/ß_}H\x000fiy\x0017k¶YÖÌýÐ¸3È}\x0004ëó[°áw\x0013ëÌÿhöã·)?Ê×ºpkí²<®Çéôªf¸,ÇÌ\x0015\x001b\)	·<À\x0006Ï£ÒÕ¶~#°ïü ZqÝ¤Z¡Hµ\x0002\x001fdd\x0005¿²Ù(%+®I²b\x0019Ó¹³ÃdÒO\x000f¥\x0010È\x001aL\x001cèçèÅ]y.p|\B4·°.Kõ\x0015®ät=ÁYöwv,Éïp]¡Í6\x00124ta¤ä\x0000ß%P\x0015ÕrIËl3N+©¬?}Ï·wÑ£3*\x0016É§ê¼xÂl..9¯¼
Õ?góû_fç|xýýþ+"*7 \x0010ÿåÓýë_\x001f\x001fph5ÂE+;zï4©1BÅ¨Á
ñ¹
\x0010\x000eµÿòéâ.¦bÄðÇË»÷\x0017\x001f\x0016t_j¼ñµx2!^H·gÐ©
ª\x001c¨¸\x0005o<Wb%\x001eö[û\x0007:Å\\x0011O§özÄ+&¬mÁ\x001b)¼¬Å\x001b \x0012Ð)Ñ¡p£[4;mÂ\x001b\x000f»XÕRÃ\x0004\x0016\x000fÁ¦ì¼V1e¼\x0011¯>¿\x0005o<áb%Ðé¡#âYZë"Ng\x000e9îMxã±\x0016ëðâ¥)Õ<D<)Saª\x001aff&º¢§e\x0013ÝxÅJ:jâ<j³&W\x0012×\x000e\x0014ï<}&6ÑÇW¬ü´àÎÓ¹ çôa©Ç4Â)ØåXLGV¬=\x0017tïxN¥H\x000cùØè\x0015»l¼XÂZ>\x0003éE\x0018\x000f\x0006ÝÛÐ¬|0\x000ee\x0001ø&s4Vò9É>
Sýlö¡õÂïâ4&úó«ù\x0004e)}\x001aï|éÚÝÅ\x0014ê-|c¥\x0016¯F|Ê¦Ç\x001ctº¼Tnï;ÖoX?M|ØR\x000f¼~ü}µÜ%fÈ`¬>\x001f\x000e\x0003½t~ã%Ö$>iØ¯Y½Ï÷vYvØfäKÓÿ<6`\x0018Å|c>½qòO÷¹ï0äÙ4y\x000e\x000fì×ÙWÛËP\x0012\x0006\x0006ÿ»}\x000fêôä=jSÑ'Ö>1úÜ@ùE/º\x0017Nµ{ºýåõekw\x0004M[©dÊAøR\x0005Cý<\x0004äD6ìuõ3Ç\x0003'Û]_Üýpw»4(±\x0006£x¾	\x000c$n6\x0004ÓÞÝ ë\x0012ÇkpÐ3v¥\x0015"ù\x00160aBÒ`Ê1óÆvS3\x0007¢\x0015bø&0\x001cs&Okðé¥\x001aPÓ\x0011=h$÷QôÞºÇhx¢\x00164\x0004÷\x0018ð\x0015j|ý`\x0014··\x0005ÞcÊës+\x0013XH©Ù\x00086w.×qßdðéõ×h\x0006ë\x000b(¬³¨0%e\x0013&Ý´½\x0010úHÀþéîÝåJº±pô::)n;6^\x0010\x001c`¤£\x0017|T9\x000b3[­\x0003o,\x0012½\x0012ÏJô\x0019\x0016\x000fu@Ï&
\x0005W16ÖGÜB\x0003Þè¦½\x0012\x000f°Ð,­.UJ+\x0003é
5Mt£öZ:î°ó)\x0017\x0002&ðiê
ÊÖË}¾íXM{\x001d\x001e\x000e8µôm±¬,á)zgx;í¼ÑMv-ãùãÖ\x0007j\x000fWF+¯ø`\x001c»h7àe½WâHúR¸x&É\x0013ÆÅ³¿mð»¬ÞTÂ{íÇ\x0015©»\x001e\x000f®à`Xéäôñà]ÆT¯{%Å'R.@)w°+»|ÝÉ]v5¥»D<º\x0012¯=iùRI³B\x0005Ò#wÙ\x0006¾ø\x0011d]Fñäo­Ã7\þ¼)B|pì®ÓÀ7¾k¯6Ì*évE>ì;Wd-Ù\x0016\x001f`ï;¾k¯å:©ÖyÐÍA\x0001\x0000E\x00051\x0006=ëià\x001bßµWóAÒD>Ïõ\x000fèø\x000eY³=øÆwíµ|BÓös¤}\x001añ¤`ë'Ý\x0016\x001bðÆNÖ-\x0001R]däÃAmÉµÉ@YZ-\x001f;àMÔ0×âÅ5K7m|N½\x001d\x0011Ï±çõ>ìrzñ\x0006:3Î"tz\x0005d¾@2çµÜåób2\x001azfãèy*®äL£4õ³G2)
|ñAuF%Q
ê­ÑéåYáÓ\x0001YèÞv9½ø	=Ö\x0019Û£õ\x000b
iÐºX¶.Òmø¾÷êÏßþlænlOñJùæùõáÛ·Ã,7gS¦G\x0006zÊ@5\x0018JHá\x001bð2#Þ-ßÜÜ]~ú´\x000et<\x001e£	4?§Å
\x0014\x0017#(u"è±´w+èx:F\x000bhô)&q\x0006ÆS)\x000b\x000f¢ñÞs<\x001bc=gS©ÙÇ}(PM\x000c¬½¦//8\x0012Z·ÇE·¢º¡Ï	ñ¡÷1V\x0010\x001dAÇ3<Z@£\x0011÷6¿,¤[¼4\x0011\x0007_\x0016ü\x0011Ø
:áÑ\x0002ªôô4-L\x001aN\x0016Aä'8qì«\x00154åÉË4ù?úËÓo÷ÿ3Ì[RäüòÛ\x0003ÉG\x001fKÎ\x0005\x001cù*\x000f/ÖÒ×T\x0016=BsùöË\x0012Ò5èÄ¶F»D'\x001fR\x0001Ï@ª(*ß\x001bubK\x001bP\x001a$öÒcH³Q#ª\x000fü\x0016+ÜoI'Ö´Ô
âdN©jVi£¡EµÇÞLQ'ö´	&DÔ¡º,r*{0ûG¦fÎ9máôÔ­\x00109c|\©¶Fñ>=wlF\x0018Ô\x0016Ô\x0018*§#åq3&¡,¤òñÌm>Rßþû/¿E3õòð:È÷Hù8\x0005\x000f8( ]8è½Å\x001awbÞ^Þ-éöÔ3æi\x001d öI\x001d+\x0002C.W¥ª¤èÅ¹	qÆ,­Ct¼+ÃðÐA9\x0017ÒØÖ\x0002%¸wB±G+\x0011%],C\x0000~¾\x0005ôb"¡6'6ãjÂ\x00193´ÐÐÄQ\x001cªrâJ§¼.Ê\x000eîög,ÐJDC+\x0018¸H\x0004;}y	OøÕx3Vg\x001d\x001eh~<õq\x0005uºü\x0002=¸Åâ¥Ö\x0010Ç3ØÖ"âkez¬t6PÁ'\x0001
µ×.\x001c½-4\x0000
6N\x0007~\x0011^Ñ.4G³÷§\x0011Íøûo¯s\x0016ûÝÃËÏÏ¯OÏ_O8\x0016ÊÄOÑ8yh¹ÀK/yë`Ý}Þ]ÞF¿r}³ÐÖR\x0013LözBMå\x0005R\x0004zA\x0001½9b
\x0000G\x0006{5 t\x001eGT¦2\x0018\x000f^/^\x001få2½pd¯×\x0013J¾ã\x0004êN!}dkõ|5!¬áZD\x001bÐÕé\x0018\x0003Ac^	t/(\x0015[7!,âzÄ\x0018Ö¦<AÀjúA8/"Ra©\x0016Òé½Vqd\x0011×#Z¤}ÀqÊ\x0011\x0013 8.oâ\x001b\x0019Äõ|Þ\x001bâuÅ&íWi
\x0006TG\J\x000bàä¹u5¡\x0017VHnO \x0010åpËÆ¶(º\x0011\x00068V½yñ«ÿ\x001fÿùðeÎd¿ýíþõ÷\x0013¥s:\x0017)O\x0019
O\x0013Ô_ÃÇEÀ·¼¸{¹\;WàìõJ<,\x0019z:"¥jÔaJ/^\x0011ïh\x001aµ\x0001od­Wâ	Y£\x0007<7­õÉh)å1Ü72Õ«ñtRà«\x0017|R\x0013x.©\x0013ÄÕsòÈ	iÀ\x001bÅÕkñ¢§\x001bÊ"\x0007º*'øÛ\x001aw$UÖ@7r"képÈTHt3øÊÒÕN¢Û@\x0007/ÏðXÛÔF|ýüúøíìýýßÎ®ïÿzú\x0019'(=\x0016¦'k\x001cÛ*\x0015/)ë2ÓÐ?5\x0012_ßÜ]}:{ñog×\x0017?
\x001a¸?K£\x000fýñ\x0007oâ\x000fþ=ýâ\x001eg·÷¿?ýå=T
(ñ\x0010|"G{(Ïwú0sS¹8û	e=În/®Þß|øá4¦*1U;&Dwbè¶Y!ÂÛÃ\x0007ëæ
=1u©;0ã©!Ì¥)2ablÂ\x000cvÕ´%¦íÀ&!DL\x0013Ð\x001fb\x0019h\x000cµ\x001dßNg|`3¥+)]\x000f¥LMRÌ'Å7\x0014´n6ÑØLéKJßA	Iê-\x0008TïTQ\x001b¦[j¼[ï±1CI\x0019z6¦Lb\x0012Aà\x0010ÒÔ4Ä´>Ìµb¶b¦	.Ù\x001aA;'êÿº@2eÁãrj`N¿99\x001döH¦1ié³k®§äW~æÎÚ\x000cY\x0019#Ùaö)Ô6½ÐÆ°ÃxJOø¹.ÃfLSa\x000eÌ\x0000Tæ\x0010Ï
$Ù¸FsBÔé\x001d¬¦ì±j¸ü'ã.ÙU
sË\x0001v0H²2²Çnê4´ãYq¯ÚB	ÎìÍ5\x001f4cVvSö\x0018Îè+\x001dåÁ£w÷äÒ]¦{C^©ÇñÖu[Â \x0010sûðûßOEtÎ\x0002gWt°6Â>{¼g\x001c«\x0012\x001aÄan/ßÿûiV(Y¡Õz*\x001e	(>\x001f\x0011´¨ªPÚÆªJVÕÇê\x0014ÕfÇuÍ²ôÁòÂ\x001e+wh5%¬é\í\x0012\x000cöC%V)i\x0013hq´P¶Õ¬¶ÕxAUÑÁ86TqÃ:Jdi©Õ-6Àº\x0012ÖuÂ¤ÑýxáX½0ÌzLå Õ¬¾Õ:Î\x0004\x001b¯Óp\x0008k$ÅÍ\x001aÃ7À\x00126tÂ*|\\x001c`H¢¾\x0011VsR\x0018ç\x0013ì\x0002+EecE\x001f­ñl\x000cpâvH\x0007\x000c»1öh­c\x0003mí\x0011ú\Ñó°¸i\x0003­-°»öX[I\x0003må\x0013dS@!LÊ½\x0018ü\x000fK\x000bAÎNáX\x0011}\x0003¬®`u\x0017¬ÂÎÉÛ:céÕ\x000ffãeÜN^AV^Aö¹\x0005%|Ê7FZT#Nkë¤¤«	s±k\x000fmå\x0017dcËH;Á\x0005C%`--­Ç=Z`+¿ û\x001c\x0003\x0008â\x000féZòF@
3ÎLmeâ\x000e\x0010U?\x0018´;_¿\x000fZq_¢ÕÉà\x00008;å´Rl\x000eP\x00163åüôÌÛÖíÍÝçA\x001cîómR³:Í	%'tp`Ò­5rF·ë\x001dG1+:Ý­\x001d º\x0004Õ=\x000b:\x0008:GJ£h*©Ò»H)f\x001e\;(mIi»(}þì,£¤æÕÔsÉ¾\x000eN_rú.Î@ nxÀV\x0004
¼=çºÚAs\x001cÎè$Ma\x000eçH
Ã¤ôéµÞåÓËê$É£d%÷¶Dï	T\x0003\x001f\x001f\x0014¦!vÏçÉ$c?\x000c&iÇ\x0005¼
\x000e[Àº4ÿ	Ï\x0014Bzì\x001aÚÂË¢Ù¢è&É ¿{¹ÿúËªw\x0013\x0018²+ÎbýkàKK w\x0013¡f\x0008ï.ÏÞÝ^|øaù¥$£A\x0006Mh@\x0012èÞ¹ôÇ\x0001
Gf%´OÝ\x0000¦J0Õ¶f6	u9kYFL	îOó6\x0019sÞ@¦K2ÝB¦&)g½§ãÚ\x001cÔ\x0016îäL©h\x000b)ÑLÓ¢Å (y\x0017kX¾Iñx\x0003ê\x00133&¦Ìd¶L\x000cý	éépÈ\x000e\x0016HRÏ;\x0008Û\x0016Íh®mÑ<52;Uy¼j»C´ ù\x0012Í·mµ@À	¾æBð\x000fçLb¦\x0005,`¡iÍBZiÍ¤ä+­\x0014ç&G\x0003ÙÁÝ\x000e¶V4¡)I\x0017¸hæp5\x001f©g$}ZØj?Ðæ\x0008¤ôµÃÜP*ªÄe£°ÊßôEeå\x0008d'Ðô=\x0003×£*Vqà¶aUÆV6Y[c4U®Eßé¨BQ	C2\x0003ÑwÎ\x0005x
lµmæ6\x0000\x0015 ºaJ&EÉTß\x0019ÿòL\x000fu\x000bZene½µ'7×bV?;Ï\x0017Ñ\x0016°ÊØÊ6k\x001b8\x0007âb`\x0014dÓ©!ia«¬­l2·Æ\x0008ê°p\x0016-h«¤\x0000
ülúPY5h³jî\x0010t(sN_Ô÷´væé¸¬\x000e Ûì\x0017ç´fÒâ|,\x00086ifÊv@íð@}\x0000\x000e\x0013¯T1'\x0002IXx«ì4ßÖÂVí5hÛkÞ 3àøm ð)p3¥\x0015
dªÚjªm«áíp£h|2\x001bCoS^üRË\x0013)×W>p\x000c\x000e\x0013fû6§Ú×dCÆÑ4"ÆhRO¡¸8Ü_ âjÓÖúO÷#§zßäìå9û{Ë=yø$Á¦.ÌÔ[¯ÂÓ¬^yøAwÄ\x0019\x0015Ï¿ÿ|\x0010oõòPk®\x0004> ³19ßéq&ÅÍû7+0¡Ä\x000eL|"\x0001GA*7Ãï¬óep&¥ß\x0001ªJPÕ³Ñ¡Ñr\x0002+¿*y¸´êú×\x000eNSr\x001eN7\x001c%PmRó¸\x000ekgv\x0000µ%¨í\x0001\x0015\x0014VËâ\x001d
ùF;wÙn\x0007u%¨ë\x0001
Þqâ×\x001ej´\x0015U$ú;øÆ=@C	\x001a:@\x001du$£X\x0014\x001aÆ»\x0007úsUí ²¶M=ÆÉ\x000bHãg"ñ$»\x0011ÿ\x0011R¯ñnF\§\x0003´:L²ç4yy¸\x000c\x001bÃé=åÙ;?ÓqÑN
ÕBÏ\x0006e²½J¦â\x001eå8ÒÍèÝ®\x0007ýYÚ/½ÁfªOK¼Þ¼¼>Ö.$·9TszCåH0\x0008|\x000fOxÁ\x001e+îÈÅ^onï®	Bgp(Áa\x000bx¼EÃÀ­ãÝ0=C\x00008H¯º\x0012äL.z\x0003·*¹ÕFnºs0-FÉ0p@\x001fkak\x0007×%¸Þ\x0002\x001el*\x0006\x000cñ*é)K\x0000\x0010\x001c¯øÑFÚfnSrM;\\x000eÉdÂÖ	Û¤\x0019-}TZ¨ÛÜv\x0003·?ÔYëøÇ4$\x0000¤\x000c\x000eÇ\x0006\x001bµ»\x0012ÜmYð\x0018QM³\x000e@ýÌ \x0003ï\x00135ÛÀíKn¿éd
ÔO&½!\x000c
ådRæ:CúÁC	\x001e6L\x0012¥
B\x0005\x0016\x0019ÛCÓNúXaV3xQLÎGl!ñ\x0011C¼Ê\x0019:êÊ¥8ZZØN^»ÍM~3M(M]\x0010¼¸É-Ul\x0005qL8±¼òrãtXVBà"JCü=s\x001f+kç®ü¦Üâ8}zræ\x0015\x0007ZqÍ5óÑ¾\x001fSÃh&¯\x001c§Üä9½d\x0018ÿ]IÒ?îrÏ\x001d3áè¸¦vòÊuþÔ½Í\7ïù*ù\x0004ipÇ·Õ*EeQYÆ\x000fMÝMY¶#q"«ùQ÷Ö¬ú5z{WÓûyz~\x001f¸#s"Ã\x0011ÑmÝ¥2Ê¦T¿ö\x0003¸;\x0000÷¿ÃY±3¹ZR]ÈMG\x001eôú\Ä³h¿_à\x0011Í2\x0010ô»\x0002ýóo'¼Yª'0Ç\x000eÑ\x001alç\x0010×\x001fûA ß\x0015äg?\x001c;4ì×|\x0019?jÖB£L=Y\x000ec|
òè\x001d×t§mÏl§Ë©\\x001e\x0002#{s
AØ]l¼LA»\x001eÚÍ\x001bºËäÐÛÊH8ÒO×ï\x000c§}Ï¼2âöTCGª«ëÃJ\x000fr\x0000.gËA\x001e:Ì\x001bÚDî\x001b(ÛPÞ-h\x001egn\x0017!\x0017=t·´ù+å\x0000ï¹3\x00033È\x001bU\Í5
zèt¥\ßÒS­¡©1²¦ÃÚMÎ,tî¡ó\x00196íZwjpÉ&´»ñ¼þü1\x0003Ýbø])Æ\x000cuN×²¦íµ\x0018\x001a[`YSB\x001e£á|8tåÑÞ rë.S»ñ\x00126E=C.ÛvFÀëÓ\£\x0016øiê!¶À|pq\x0011ûh\x001dµTFx¹\x0008Ct3Â\x000b)í*´ØS·T9s9è!ºÀ|xq%zs9jÄvÏ±eLîY\x001e\x000cá\x0005æãÝ\x0015ÛPÙe¿Ääv/máry\x001e\x000cñ\x0005æ\x0003³­â«\x0000réoq!R(\x0017×æ\x0018LS\x000f\x0001\x0006æ#
ÀÍÔùùF'æBÌF}úö{T¾ã\x001eñÔõ¸»~zÿëÇ'°ifx\x0010ñÞä³\x000cÈA¦^ÓT'N]·Ë¹ë§»ç¯N\x0000Ç\x001eüàjA\x00013kvå«VêXbqô|T\LÏm{î«\x0005
·óÒteá¦\x0000\x0003dÎ\x0011ºÌQ»\x001eüàfA\x0003eüI6N+\x0005\x0004ÑÍÏþXo\x001eÜ÷à\x0007\x0017\x000b*pyÐKÙòü\x0004ÙÚT6tIêÐS\x001f\ÉN
¦\x0004wSçºÓøu\x0015ÿ· s\x001f¢{ò\x001eç\x0014n\x001az²w±ûf²ÿýáÛç÷OhRÏ\x0017sJK<wi¹V+ò¬ü\x0018yõÃ»û»ÛmÝÓ\x0006i{H;\x0001IÏú\|J£"?ë'©ÒÚ¬ç8\x0019Ñ÷^\x0018±5gyã¥3\x0007i°\x001a3®e¢JÈÐC	H#ï$0ê ©òå4å×\x0014¡µ±\x0013\x000e¯Å¢Ð`x¿r¨EL=bAl
Jc\x0004R®ÊÇ>\x001b²;æ¡
ïtÊ&s\x0010=lmkwKrí>HI	\x0003%è)\x000b\x0006\x000fôôöÊUeÎåö½7k N\x001c$LxÉrl\x001d·yW\x0004c[%·[É¶´n t3FîÒè`ÌR\x0011ËïfÊíJÂ)\x0007\x001f\x00043Nj\x0007ù{;)~±­`ß¯¥#'BþÁ8¾Ëf-ð@êïrÑ/tH¨X÷ÿø·\x0013ú×=\cÍû\x0012\x001d{ëY,Ø\x0008Òm¿r\x0016[æÍ,å£oèpJÏ½ û\x0001ÝÿwB\x000f\x0003zøï\x001e\x0007ôøß\x0000½D±¸÷\x001eV<\\x0000~»JW/\x001fÞ_\x0001¾Opn=pÌ,4VÜF\x0002i\®³ßÑÿÊÍ]ý_y\x0012\x0014{P\x0001õ©õ8Dh®\x0003Qú/`e\x0006Ô\x0004hìAã\x000ch\x0002\x0016æ,7H2HÓA¤ñg­ÂïtPpû\x0017nT¼PHàXlÏ Å¦VA½ÜVç\x00159ÞVx<Û;\x0004\x0010¬-H|X¡\x0001äÛWåºÚh0Ãê{V?Çê[Êl¦¢¡Úa%\x000f[ií\x0005QÅûr"¸÷´üò\x001fÿöùý/ï\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ºæ+ÏTñ\x000b;Z¡j\x0014Úf[^\x000c¡ëðÍ&Î.R\x000fmT\x001a\x0019ýóÍýÝÃ{íÕÿ\6ÐµÂ£8ìg\x0017Ãá\x0006l\x001fÈ©»ÏO-®ós\x0007\x0011ú±ã)\x0019ä\x000eòªW\x0015F~lIJkcqÂwÓú!Ê¨]×orÓù±]!ÈÝ_§Lé´ôê\x001b\x001eècWÞD0\x001d\x001a"¡ËB¡¹§À\x000cÎo,}ÀÇ\x0002\x001bÇp\x0004Õ±ü\x0000P^·zö"å¬5ìÕw;¼¦»òÑ\x001d½EhØ\x001e\x001b×äò^¬½×!\x000bü \x0016ï\x0017J2\x001b6vD\x000ei´CSç$}Ù8\x0008TwÇT·ÊPçVrÛ\x0007´\x0019L\x0012º\x0000Îj\x0007z\x0007¬Ej~.~©6Dþ%¬Ô\x001c:tÂ¯æ9R*ýH\x0001ép&;wË¯6ÇMâõ¯¬tì
w¸/Û¦×Ì\x0004\x0017:6Îópj²£\x0011U%\x000c>rc·Ïêý
\x0016êý-¨6Á,¡ñÛ\x0004%ÖiÍ\x0004DHÇÆ)8èI}\x001c\x001eË8Du]"L\x0002ô
\x0001ºÓ\x0008\x0011 ÌKÊÏ27Q c]\x0010þýHøW&\x0001Þ¬[«Üy:ì ífýp{¿¼\_}hÌðË-h1\x0005 \x001e\x001fóv\x0019Bé.Ø¼P[¸lq\x001eìg©SN÷"¥Îdïùa/nÅòWè_¿Â)±\x000cïÄ2$\x001bÂ0*Ì»-!°ü\x0015v\x000eC\x0005U\x0017y-R£aÀC4døc\x0015£*\x0010t:ám\x0019ßÏÞ}ñÕÕT\x0017r¥F$ù¶c´²·\x000e¯êö<±Kì$4¼WÕ	_ífuÏß«êx¶SñQ?,\x001d\x001a\x0001Zk14Dë<4î¦5|ÓIå\x0016=¯
\x001b{^å+@ÁCÙQÆUÉÃH*ÓÞ«YN¯cSx"f¨¬0·sÛTµy1~nÆtr± \x000emfá\x0008;WÆîs gÖ
\x001aÓ¾ªd/Jû\x000e7VÔ\x0016
\x001d»r\x0016üP{\x0011S\x001aTõÓ\x0004;·ÓÖÔ%\\x0017Ð|þRUF\x000c¾Ye¤=Ö^\x0006ÉÚºÁô$×&Gu\x0018X,ÔÈEÝ°W+ép%ç×À£WÈÂ?íØ8¦8c·ø\x0019âÑ[\x001bHxÖ\x001b×\x0005\x001ag¹\x0013=\x0019\x000e\x0003À¥1Å±4ª,-Z0;4¦ð\x0003\x000e³\x0016è8º§MÒ\x001bºgó~\x001b6Íûÿ\x0002±]áòpñ4\x0015Ag¢¹ËÞ±Ñe\x0017·\x001am£Ux\x00072rW¸§\x001d\x0019ÝS\x001fPÑF|\x0003$
7kS»üÝ]XkÖ
\x000b)±¡MÂRÖöAn3å}Æ\x0001t.\x0001íE¾:µ´1l?Ë_m[\x001bzXmí[\x0008\x0004:|hðÇjYdÆ½ìØ8ÜöâËþÝÉ	Åîä_Xõ6ht#å2Ä&\x0014£ì7%\x0016Je´\x000ewe¦MÁÛ\x001fà{\x0003ª\x0013Eëwt&\x0007â½mÜuù¤³ÖÕåæÙv>\x0001VßÈII~x\x00176%)Íèr\x000f²{*ÛÜà]h\x0006Â3|_¾©í¿à\x0006~AÀ±ÖÕ
\x00139KäÉê²R~Ö¿À¿ b\x0012[\x0013ÁðÀÕºe\x001bÖ\x0005s±>îRt\x0001ÍÆÑ½ñ{q'Åó¼b¶M,!ÙuÇ8ªTÄgP\x001ch!Í\x00148Ï½\x0017­pJ
9ãñÆ
),K$[ý<CÜ¡Á\x0001Ñ\x00195(aË(¦0\x0010\x0013ÚE:iºëÈAHÄU\x0003Õ/ÄÃg'5\x0016ÓéRÓví»i¿F	øq\x0003iMI\x000eL/=\x0011h
ª\x0018¾¹ù¢Åjÿ*\x000b|¥Öj
PxfnÌÁ\x001eÁk\x0019o\x0011È³$LÙó5Òë\x0018ö7?ñs\x001e5Å¬*\x0013.|©/T\íÅ'ïîÞ¿¿»\x000eqJ]^r&]Le_\x001a	îJ\x0012tâásÙ\x001cíÉLËYóT\×ù@¨°\x0006c
9eRioà$²ëÐ\x0019¡YÄt­|æÇI>%ÏY7Û$N-\x0004ùSUd¡æW%p\x0012tì¾ÇDÚ¤a[6\x0011#¤è(³ d\x0000\x001a@#÷ª]°W:4\x0004jl¤©¶\x0016©á³}
igð
ðã¤âÃ´n\x0010{é3ÒfÑh\x0011vÜBH¸´9¥\x001c·8z®\x000eCÌ¸8OÅU*<\x000c©p­ó ,ZØtÚ¡A`,·Tø,÷Û°Q;*Ñæ\x000eaL\x0012åÁ&¾ËµÏªumò©åÜ\x0016\nð|ëÀMÎÎ´(\x0013<a¨óúû77wï¯åq©\x001cI@Ô¸_1Ät´¬eoSz\x000eM¾5Êý2j*\F*¡v\x0014\x0013¼©\x000eøA¬tPzònÒÇRØ*³w\x000cDðV5SqÚÜBÔÍ_Y0Ô;´Gèé"<ºs\x0002k\x001a\x0004Q\x0005Ô\x000e¦
\x001cQs±Ä[<\x0003³>Yeeê#\x0005Ñ¾úàUz\x001b)6Ó¯&B¯\x0018¤õ^Ïz
\x0013X£Þ\x0003\x0019lí¨cP¡y\x0015«mïÒ¬Ikà?Ä !ßajg\x001c_\x000bò&¡öÁh³\x0006Í\À\x001eÙC¬êU;²©Â\x001a$ú.Sü\x0002Í\x001b¤À*\x000eZçMß S\x001f6ë,+ï<VXð¤u®û ½]¼w\x001d9\x0000rÂ·ÔÛ2ÅÈ¡æ>\x001fgµ¯-îëä[ä]©aU±Y[£þN¯\x0016ÒÒB:HÉèà¶á»#Í¦Ï.º§¶½\x0011P³9\x001e\x001dß¯\x0016°9å3Cu%ÌB ;#r}öN.ÌëPpôq§åÚ¤ÆÍ/p$*ãjlùõ§~:ê,X9ìPæ°.À4io2ó#ë´ß/.ø
\x001a¥&uàÍá\x000c\x0017½ª-YÄ	`¡ñÄgÒ\x001d\x001bs\x001e¹]\x00073Áy\x0018úlcÓ\x0010un7ìu6m®%£üæp9ØÔÊ\x001c³\x000eÈÊÃ\x0012râöqyð¡¸ì\x001flh·ÃtdÃF}`9\x000cç\x001dË\x0013TVö\x000cÎoÃtVÐÇZÀÜ\x001byá80<Ò6Ýª¸Ú\x0011#\x0012
\Ëê\x0011ÊD6Hi´´Ú	µNMBá*§T-òáÓðÕ«0k\x0006ïÐ(\x0019:¿\x0006\x001e»A\x0014zµE\x0012l\x0011%'fXF­úrþg0:kº±XGè\x0004÷- Í°Ejë¶:°¹ýF\x00074µA½\x0013'´a\x0017\x000erµ8Ñ)O\x000eHÙúÍ\x001d\x0017r[\x001d\x001bå¶Ãù\x001eN=\x0003éçRÞÍ2«à5l¨à]øS\x0017lÙ¾ÛRW²Î=iM8³BoÃ®øÝ°l@)ë\x0017xôªÎÆ\x0008ý*æÁ·ÛY ¡7.f×d2Ý(¬G\x001f¬
ãN¢²8ÉkKòïîßÝýÛÞUG#Î\j\x0019m\x0015l¢.+ßó£Ï²E`¦¹\x0010F7p\x0003M;ª¹à(¥Â­î©_\x00103·8\x000e©êlN¡rQÉ4M­¼\x0010UïÐ¾Ê*å\x0002\x0010
,s\x0000âky	kg`·?¸P°U\x001c\x0016ÈòÖssj\x001crLË=\x0013pnØ à\x001crÍD\x0003É¬Æ'ÿA\x001eØ+¶NÎ\x0000Özrý·÷wï?Üµ\x0001ªw7o¿¼V=\x000eâô¥Ôã8\x0007ìÛ\x001aO=ù16
L\x0016¦\x0017>
\x00153våGD¥Ø:´Çþ\x0004Oê\x001d\x001aê:c\x0005djaÓ½\x0017âP±iüÉ\x000b¼kp\x001aBB­òì|&hÃµ\x001aÕ\x0012tÜA·\x0000
4ºùòJY.å31-ÁE½5ûÏ0\x0012Ó\x0010Øî\x001e>ËyF³ù=ãÔ\x000ek{¡zÿ=¶
d?bÓ¼\;ÚqF\x000e÷òO	Y1±Æ®¼äöù\x00004\x00142t\)\x000cÓ¯¦÷Y"4ùêxj\x0006¯|±Àn\x001f¦Ã$:6\x000eÐq÷8W\x000e2J)Õy¢<\x0005n·ß°ám4J"\x0006lmqÃÔ¡Á]í$\x0011Ð×o" ñ¨¼ùæÍ»k¥\x0003a¢U2»J°:³æ§ojû-³C\x0016ùÉï1àÅÛT\x0003\x000bÑç¡SJø²8dqèï²\x001aÁ¸\x0014x¾`1<Ë8¹Öí~v.6è_\x001dZÚñ»KGZD¦¾BSç]É-)?ûgÃx;kûøìýÃÝ0¼\x0019
òá¡÷¼è8\x0007:\x000c\x0017´\x0006h½VÛID¿°L±W%Éip³&ß÷/>\x0011?æ««ÑX4{É1\Ø\x001bù.J÷>-á©Öý3t×Ý¨ßª´\x0002±²)<SÒ²dP\x0015òùvíÐÀcL¶\x0000ñ@ ¹X¥ö)ät&-:\x001d;4D³ª\x000eà!{`\x0001¡n(Ø¸­ÞzÎ§tl$'\x0007|\x0004ì!RvÓ@Î¶¤Û$m¾acØC¯s\x001aàÓð\x0001?äóRòó½
\x001aår
ê\x000eÈïõbÒ'°³kíY³Ç¾Ôì¡\x0019·ç´3µòzÖYf»L2Û-\x0006`äîjHC7ÒM/¢Ô¡F\x000bNõVMO\x001f}Ì\x0015\x001afs«JËnC`Ø$àæ\h|¢Ø"\x000côìÚÊ³¶cÃSc\x0005½\x0019¹¤yËÚ(séç\x0017\x0013gQÂÃx÷pßD÷7¯\x001f®¤\x0007W,+¨ì¥&Þf?H¤*­Ú'o-G\x0013ß8\x000e¾±ü¯ÃÏÉMIr7\x0005]R©^?¿a;2\x0008^\x0008Åå.1³ÐÄÈäÆX½\x0011~ëØ0\x001eÎ\x0019
jAÖ&ô\x0005´\x0001uÔÒõ³DF1Ó=õéÝëÛwoß^k\x000cKãØÓêö\x0018ù¹!u?ù9î§\x0008 aoî\x000c_Ræþé<¨@ÅÔ\x00063L8\x0016\x001b4¶§T\x001a?
q9°Øú6\x0013pvÿòcÚXÅ4ÚÊaRf"èríÍ\x001e¦Oî¾¿¹Ò\x0004\x0017#qî$ßSbQ¹WGE]eB#ö,5á&®\x001dò\x00181È³
eÙÂ¢Ý\x0016!\x0011½?l\x0002èÈÚ\x000e#B£ÊÃX\x0012-Td§\x0004Ï
)tu	¯Û&æ\x001fFÝ<õpÑZ\x001b\x001f1_\x0002ÝMa\x0013+¼Ó\x001b¶\x0003Ä\x00028\x001d¤FQ§Ò1URÏ8Û\x001d\x001b\x0019;\x0015$Ä³ê4Ó\+\x0017ygHµ³£&¯\x001d\x0014\x001b\x001a6.eMÍAFl²I¶a1M±cÃ4ÅÕ¶ôÈ´6MÜ<Ñ\x0005\x001c»SÅù&*\^±Ûx¿\x0014Ð
R@ÑcbV3Eä\x0017)ÃsÀnÊ£\x0013Væ
ö>·ß\x0005[{ýÑÞª-OØ]åuÒÉ·a\x0003GJ§W\x001e\x001aUZÓn©kønúìÒË®\x0013¶Â\x0006
ÜFz¥Ô6\x0006új\x001eÎÔlMzí:2ôÚEe\x0001\x001f3ë\x0004LÂ6úÑüÕ.å\x0019\x001dRiJaÿìöímR¬W"¯«*\x0005÷ÔGç¡\x0007<ÐäZ\x0017ÛMóÔäõP'ê\x0019Q6\x000eÎü |v½êHPûSK \x001e¶\x0008µKÅOø½qp\x0016¼Ãa\ò¬\x000cÚ¹&v\x0016L\\x000còîÐØ§í¨i+ºgh»íÔ_Ó\x0015©\x0008]X\x000eE\x0005\x0016xs¤y~}F5\x0014Ùòè=éÉÃ©?ÚV©\x001fK¸ÞV^=ÌSÎ;Àå\x0002ç+7hldè
\x0008C\x0018$¥\x0005z\x0018å]óEºA³&ò¿Ýà§f\x0016B¾,wdì\x0017d\x001cÈ\x001e\x0002ó¢ºÖ#ÒÖ\x001bkÂÁØ Q>3ÓüqUÜ¦¯N/g	4Ó¸¼öðI«\x0015
¼SUIô\x0014ÐÄÕ¡\x000eålìC4ÿD=)ðE¦Ê'0uÔYÇ³cµ·Gè&G8#H\x0004>]Ê\x0006ºXüGÕÊú
Á\\x0004Û§|ÓíÃiLÜ! yÕÖ\x0002'p©lc\x0019Öq*úæ3¶wýî«\x000f·7\x000fWz\x0019ã05@â»D¹×Æ\x0000.õ¹ÀÏòeÉySâ\.¨3â\x001dM\x0017ç\x001ePZæ{Öhäò°Ë\x000ex\:\x0004\x0015ÓÌÐ­çxöÆ\x0003×ø°øÆ\x0018Ã\x0000Án\x001b\x0010>{	ÆR^\x001803Ý×À"\x000f\x0012\x0010´JI.îk?Ü×Î\x0007ºTu¦\x000c/Ò ¼\x0012m\x0013
±Åý RºÚîéUëg'_°+µFú1>°¹:âi¹;?óq|ó¡Ð¯íúH3«HRÔjü \x0013îêRN®aCÁÈúpðê]t¤*\x00159YBk!¶r;O±Û\x001f\x001c,\x0002,ËM\x0012Ní\x0014l[\x0006_êÈpÚæüø×o\x001e>s÷çk¥k\x0019¸~±1b7G"Tì#3õ\x0019d\x0006\x0017/'é»ú'¨><Ä.Æ\x000e\x0012D¬Â\x0015»\x0016ú$wWOAGõ9u?\x0003\x0007\x0011¬m´¹³c\x001d\x0008*Õjÿ`Sâ> =\x0015	]ØDV_â/>á¬Îàã |hyàAômXÊñÕ¡Q¿=P'i#\x0011òÐ~èÓjXJ\x001dJ½ª´\x0003Êðmþ\x0001ËUD¶G×=¼J\x001d\x001au Õ\x0001PPBÿA,ÏI(£3¹;4ÜÁ4íLw£Ñ[²<qU¶Þl\x000enXU\x001dÛËÛ7WG¤\x001d\\x0003\x0008±
ØÛ8ªp¤vr(Ï`lû­6\x0019Æ\x0012ì«a\x0018K=æ¢ÉÏq¡%f\x000fºkæ¢sÌÍeeb\x001b4dbCÎH¥u\x001fví¤ä&\x0012yxÊ¼ÅlÃ\x0006N®	=þ,o'ìJNN\x0002
liÇaßEv¨ïVÝh¬ÆIÈ!O®E\x0013\x0013ù¦
òM¡Tä\x000fbXÛ\\x0007NÄº\x0010+êÐ V\x0014ªIØ\x000fT<7dØâ¹E%¥4+ÊeúÕâ^Ú¿yÿAÂÓ[ÙÎWâè\x0018¦3¸Ê>tZóÕæ¥¥Ow{lòå<<dqÛß|K=CO\x0018|®¼6\x001d\x001a^\x001bMc'ð¸¶È\x0007t$r¥Î×Y\Ü\x001d\x001a.n%\x0014ÃÅ\x001d«aêSó
Ö\x0005¿C\x0003¿I\x000bà°4ôUFÎ]9j6> \x000fì\x001fõñá%k²\x0019\x0004=h-¦Ü³
y`Ê² \x000e¸
\x0003;&Ï¹Hõü=¼ø½\x001c¯kU)=qÊUÛþ"Í\x001eUx\x0001èo¡vµçùµT\x000c~\k¾fB\x000fç¥\x0011\x0017ABºhü\x001f¼­¨>áñ2m\x0002ûQ£dyâÐ§=Ì£Ò¨aÑq°\Ìc9®&XP%Y¹Û7õû\x0017¿ýîþj¤ý\x001aFùy\x0017@
Ü:·é\x0019Ì¤ßÐ¢\x001d#h\x0008öâõ°Zíp!uÉ\x00152vé\x001eu@mú\x001c:4|\x001c®¢E\x0001Ý\x000e9ÿù\x001f]º9[¿Cc\x000fm¤9bÉ[Vf­+7:!iú lÐø $R\x0006V.%\x0011êkæ\ÙöÉVçIÇFõÞ6t÷G\x0000BEíÏ\x001d¾Z\x0005¿'Wóåö·ÑÉR¯\x0016Éï©,¯ÖÑC"+?ô\x001fDlOÌ88@²I jóåÛ?\x001e¦\x0018ÒB±ËÖMîÒ±ÛFûõ d\x00179Ã×Ú\x000cÙÿ	ô>k\x0005L#ýY
 1¤GXÈzk\x0004FNCÎS×\x0017spÁ°B \x0004b|ß8;t«óíú/7ßÞ^i\0*óÆìÜ¹`µ¼cJ[
OÎxZ<\x0002ÕÚVåhY]ýGm1wx;4Ä}6ÖGÖÀúÌ"øe <h\x00177_/X9\x0001GªÍ¦\x0012búÚ\x0013ó3\x001d\x000cA¶)8Ñ©"0Ò´t\\x0008C¥"úÐ[\x0015ô3!cr&ráò¯@W;\x000fß7h\x0008ßFW\x000e \x0007õÍ<ðÖfM*nr®®Ë$\x001c\x00145u¹¡S
Î#û¯ÉxêjÚT$qÒ¤ç\x001c§;ÕêPÔÝNçJn7Vo)M3}Öü2Ì\x001a\x0010äB*FbbÊ\x00127\x0002ÕM³z\x0005}l~{I:l¼yÕ\x001eDNªú¹Ã,ù<Õ
\x001a)\ÁCô«\x0003)\x001d ï
	zJ\x001cÞRÄt^®\x0000,äÅ4GM$\x0012£\x000f\x0006	¥Ww\x0016Ø\x0016-±âA4iº9¤¦£\x0008;å¼j~é\x0013\x0012-Ò¦Âw\x0017Ë,Â\x001c­.Ø«\x000baÃ\x00066^r\x000eh[ÞYÃæÎ\x0015?j\x0011'#\x00126l°·ºô¸\x0001«¡1ô$è;Ýz:\ób\x0015£Z\\x0006^$m\x001f.ÿ\x0006Y&þ\x001b\x0002êxËéxØ}4;5é\x0010ÉSgäÓ»\x000f×HÓP®Íé\x0018Ð¢\x001aEPüNµê<KyÂ}cbÏ9*Ó¦âpÝUÖ\x0004:7'ÍoÍ
\x001ahLsS=jæ©;¾A#»Á[\x001e«CeYæê²\£eÞ¡Þ¡Ý w=Î\x0013\x0013\x0017xn©²HCÎSL54¹\x0003ùk)©kS;7kÃÎ\x001cP
\x0008\x000c?)¹u\x0005?µß<mAx i\x001cñ.Þ(.zÕn\x000ebBD\x001e`\Z`f\x0008Á\x0007S\x000cjÄ¸Qµ\x0014(càM\x001fS4\x000bÁÆyéÚÏ\x000cssJaBd·)Û\x000bhàmÑ\x0005Ø50Ã"ä:ìþ\x0008O8>i²Ý&ØVÂ¦\x0005\x0012ÞæÁ"\x000bÁ\x000b60Z\x001cMLWÐ°·à\x0003¯ãó\\x001b\x0005üJc¡½ë`\x0013ïu!¦\x00131ä_ï¾øðîþÅ?>`
  
  
  
  
Instances: 8
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=;¿\7\x0011¶n©÷²!êþèá»ë¿n\x0002mdINÈtbÞr\x0005«¥Ë£OO\x001f¯â-\x000bØv¢\x0013o8äH±]xJ¹û,¬6¯sÒ</p><p>WUpU'\Gc<Ä>xáñ\B®ÕþôU¼Þ\x001eô\x0019{\x001bûËØíÑÕûû­±\x001b·9£\x0016\x0005p\x0014¶(\x0012\x001cÔ¯7ÄnN_.Çn´±þ6¶\x0011·`\x0008\x000f|¸$õ\x0002IJ¤Í·wÀV¶­ì\x0000lnR8|v8m\x001f\x00028b1Vï¸Ü<4àvc¸±\x0019	º22n#,ý\x001eë\x001dÜjÌ\x0014\x000c\x0007ú/ä9^\x00001ÃÆ\x000e*\x0010GÂÈ\x0013B:$\x0018\x001cåfe³\x0007wîy\x0001\x000cK¬Mî a\x0015²¥\x0005éQ\x000cñÃ½äíÏ×\x001b£üØ\x0001ãô+\x001cåÈ£"\x0005Éðy&²}'ÜNWYó\x0013vYacØÚÑ vÇ¢è¦=\x0016»°</p><p>»\x0019ÂÎ%]å¸î)«\x0006Ä}V(µ\x000b{!\x0018°;>´îFe¢8 WO\x0013é®\x0000\x0012È$öÁ®S©¬ î\x0015ºwªMÿÛû»÷W7·\x001b«\x000e\\x0008dðPÜ£~c$Ü.-:L¥éÿq~yñüäì|¡ôÀ'þ\x000e\x0000^Ów´\x0002\x000f\x0017[d\x0001òCà|¢;Zï!Ù\x0000ssÐÙ\x001f\x0002\x000b_F(Oî®ßoõ \x0008B*¦¼ »"\x0017$1\x0016/\x0007\x0018£<¹8}¾ØK Ë</p><p>²ìÆ,²¨UºåqÚ!\x0001'5Âh\x0014ò\x001bæRQNÌá\x000f\x000fb;`+\x001aTTQ~[CcZtßÒÒ¼\¸×ÌÖ(?Gv\x00000w~'Ðùýu\x0000Åû¡\x0016à,E<\x000bø[;ùåúGÐº{útcEÀª\\x000c!Bñ\x0016!3)Ôl6ôY\x0019|ÚÉ³Óï@ô.ü'.$CYýuÚ3Ò èü\x0000©\x000bôdá(É¤&r6Óµ­G\x001bÁ\x0016ÁF\x0000\x001b/=hm&NbÔîïi4ÙÙ\x000cy\x001bÖ"\x0004
XãÄÅWÅ³¡ üX·\x0016? «\x001foßm­*IÜNá\x0012\x000cÝN*ªÿ¸pB¬Ì±\x0002tòêÕùÓ)½A¿\x001cÀç¬ÏÙ0~MYÅðÙáø©Z\x0012e;ñ«</p><p>¿\x001aÆo`â7á·ÐJðëíº\x000f¿¨Ö_¯¿Ë'5gÈ \x001aðÓíÅ©Y\x0015NüÕö\x0017ãûb1áúØZÄïÆDÍR$ôá/d
àóµ£ø
§é\x0015%Y"3	øI4:\x0004¦³yÉ>üNø\x0018ÅïÌ±Åý3U\x0005Â§`(>e{á\x0017"jjFOÿüÝÛÛ`Á
5ú)X|M^Ö=[róÏ>:ÿn\x001d¤+Aº\x000ecô\x0014@2ÚÖÜ¦£s{ÀäÕZòÅ\x0014\x000c®ßÄÆq~\x0016Wr^Ï^«\x001a`Ú</p><p>¦í)HËZYüÚ\x0001§(`Sª£Qªx4Fo®ï·\x0012áEäiTC\x0003{3ð\x001c¡~\x0019!åóÓôôñÙé%\x0010à¯b\x0015\x0015VÑ\x0015ä\x001a5Æ\x001e¹eÖZC_'õlÁZtl\x0004¬qÜ¿\x001d«±\x0013VMÙÖ8:çølÚ¥	«¬ÖUv®ëDqÌ4ÔRÒ\x001e b6ô{\x000fAuòàëw2~ýeÞöåÕo·¿_Ýý¸Qç×e¥41¦0¥¤tb\x001cÂ]OÝ¾<y}þçï^®¢/â þ°8Ñ^\x0013»n¸ïQ\x000f¢\x0018h\x000cÛ\x0015|Q¸\x0002\x00031\x0006>b\x0012Uj}æC"óDêM1Ð«Ã4´!Üýê§Ük\x0002\x0019®)E\x000b\x0019X¥\x000fgÃñ.ÄTz6|\x0000ä'Or³	¤¸\x0016÷¼:(Áÿ((Á@·0/JÊ\x0008ô¸ó4ª3?1Ð½Zv5¶ì@>â\x000bPÌpix7\x001cÜèbÔ¼²q\x001bvò5¢hé``	\x000e®ßs#±¨VÛ<MÀSë\x000c0t´l#©ÃE8_.\x0017FB\x001cÔ\x0013ÓÜôÝO\x001b]»æ\x0002*¶\x0011ºud,EÙlR¬ajúâÉ"ðXá*(Q~p(ùË¯ï¶¶±Im³Â#Pj`ÁPrÔÙôy%ñøìÅÓÓ\x0010\x001fa\x000b[ÂþDXµ\x0005wXc"De</p><p>µ¨\\x0008\x00002;ç¬{\x001bnSGý\x0010¤¹\x001aöý»ÍUPÉ\x000eäxP\x000bÉK=U·(^>}µàÊ\x0011rAá\x001a \x000bÙYg®bÐ.cX¹Ë\x001fV·4ðoÄl*Ì¦©#\x0008¤âÒ\x0000\x0010¯'ÎÖ\x0011ËCï'\x0019õfö4fz¸	¦F\x0015>&2ÿ§ÆL¾A93ue. N×b2	¨ý\x000e»IãQ³U¼À\x0018\x00042i¼C\x001fs$TDîçä¬BlÝQ\x001a\x000f\x001bP/XÃ?E_°Aü"_\x001e²ÀÄ\x0013ñ\x000b¢\x000c\x0001ùÂU\x0017~Wáÿ¤·\x0015¿£~\x0010\x0005c*ðÓ¥RÌ\x000eÑwâ/\x0018wð\x001a4_ºdú\x0014ÿ,h#ü7É*Gÿ0ü\x0001rô\x0011Ú\x0011@;</p><p>F$h\x001b»P=Ðæ§á<rÐ\x0005@³JÎ\x0005çñoGð·£3¨/Áß®îÞ^ÿú FË/ÑÂc?^¸\x001cc\x001buðãÒy´ÒFÌ</p><p>\x001b-ÃÕþ;ÁïÕ}\Þp\x000fÿs\x0006¢KP Dw"Ó\x001eÁ=¹¾û%üò§\x000f÷wº¸~û\x001e\x0000ê\x0010tHÜ\x000bÀZÚmB\x0008Ë0åd¼*Fx^<\x000b¿üéååÅ.N?{p\x0006KP¤£¹«BT\x0003ÿêC*ô±	i\x0016cl\x0006Ri´hð\x001e\x0005</p><p>a#ü«\x000f(7(Î¢#H\x0004É\x0001¨BápÀ\x0014\x0001õ Rßz\x0010ôAenVá²B\x0006\x0002\x0004\x0015Í}PÍoâÝÛb>\x0004GõÛýõvÌi PÊÛ\x0014\x000f{£-wbéÕ?\x0004\x001fõúr¦?¦\x0018^èhU</p><p>~`/]»aô\x0012GDa\x001ahi\x001d[\x0010\x0006¡¾BâÝÿ~ã\x001cö\x0012Ä\x000e³p\x000f½»}÷6C\x0004:,¾\x0002i\x0000ú"#\x0015:wkd©ûÌn\x000cwÐó§3}Ù%ÆX\x0004?¾>Vÿ¨ÿz\x001d\x000f}\x0000	ÙÙû»XvßÑð
\x0005<µqèC§Î§\x0010\x001f]^¼/½×\x0010©ð¯\x000e´d´N¡è$=çH%	½úz\x001fÐç\x0016{ÝÚ1Z¢Q
 ]R\x001b</p><p>ëèQÿÃ1£vÂ\x0008sZ¶o\x001ds*Ak'´5¼k\x001cö\x000c½Ýé]Ã¤H\x0016ù×\x0011æÏ]×:\x001aÆPf[k\x001a\x000fûQbjÃ±Åèb;Ä¨
\x0004b¿Þuÿöÿ«\x0003ù¿õÛ»ßßÇK]ØØð¯3Èon®~j8
!\x0013Zãu¸1\x0000!\x0005ÐÙZõ\x0015\x0017sÂKOÈÏÎNÌ\x001f\x0013N\x0008¡¤ìÄ\x0019¢²äÈbÇ"¡Ô>£,Ôp\x0006QB\x0017ü«\x000f%	%@È(û\x0003N#RºÊz¿ÛbÂé[LÏ\x00126i\x0011&­\x0003L¹\x001c7àò§í[NÏ8éokhâ²&át\x0014«ykv[Oòê}ëIj|\x001a</p><p>«Qt\x0018ÖSegÏ\x0006S×÷oþ\x0017f@bÞãá¿þù·ë÷Wï·_r\x0017\x001e&Åã%G©Ä8\x0003\x001cèéö`*©ÏE¾9}~27\x0016\bdäø£\x0003¤³\x000csJ w·[á
îMàÏ\x001fBùËï·ÿõ·ÛlÁ«\x001an>Ã4ëäLø¯\x0014²¯¥</p><p>^Ì*3×\x0018Ó=ì+ÄxÅÒ´S.\x000b8\x0016ªÔ¸ýøîÃD9rs}ôâ\x00063Ñ[?¦ðÖ5\x0005rÈ\x0011Ï4Èìb@\ÖV>üüÕÓ/\x0013çHø°^Í³\x0005\x0014V¤Æt²\x0002úÒG­°ù$ÐáÕÉÅ:ó\x0015Á</p><p>³x;ê²ÂUV¸q+8WÁÑEz`°ÂÃÞIVh¹\x0014ÃôYXzÈ</p><p>¸\x001a}\x0017 \x0018É³\x0015*E\x000fÎ9º\x0006jµÜé±3VZ\x0001Ã/ChäW	7E7Eí©\x0015ÆÐ}÷\x000f\x0003Uê&3Æ¿o\x000eÜähFâFL{Ê\x0019%Åà^fðúmð\x001dÞ\x0006hb\x0019|\x001b&ùÀ\x000c<óÃÛØýËà©ª­âÊðjH\x001bÉÉKyIoh^[<%ú¬Pµ\x0015j\x0007+\x001cÎ\x000f-¥S§R0C1Kfì÷}\x0003Q?æ\x001f§?@&\x0012Y·</p><p>ÒÂ\x0006çü±ÁèQÛTg`\x0008¢gbé\x001d ÛÖ2{a;ï¡\x001b¶P?p¯0TÓ@¢¢s#é~ËÕR¦ \x0015·ä%nÉ\x0016Ü\x001d\x000b¼¥4Å\x0005\x0017®?ËVä9BJ;Å"çÜ§©\x001aùÒFo\x0005nª%7cKNCñ$q¯pK\x0017c·X]kF^-¹\x0019[r</p><p>ÂZý.Ò\x0010­Y¸Ûí¹Ë]µänhÉ­Ç	\x0010
Ã\x0014\x000cÝ</p><p>g´äf1vkEîE\x001cX±ú\x001b\x0018¬´´<1\x00001\x001dÜ9Gàí\x0008óÊ!ÂãÈsäÑ\x000e±¡DöXF´^}¶yâfs\x0013t\x0015â}YP?¦Bý«ûÆ\x0013z\x0005²öB\x001a:´YÊ²eÞÇT±qry¶jç¥\x0005\x0015!g\x0005Â\x0003\x0005S¼u)vl\x0005Æ3,ðf)Dî² z\x0007~ø\x001d07½\x0003:\x000b\x0019üYÑ;P\x001bvP\x0005<éf\x0005ð8hö°òñ%$]êhµ\x0014\x0018Ø-.³É\x0004Ym#.÷Y¼h\x0002ÓIÆ\x0007L ²ÌÎ&ÈÚáäXÄ·\x0010BûÿaÔÎâ ¡e÷où7ï>\x001c|Ïð!;Â?r« ø)õ\x0010{Òu\x0011r7{\x0019áÄ´Â&\x0010Höþèæê>Øpòþãí»÷×GOîßÝ4
 ÉEµ\x0001²àQ\x0005Õ0ôb
\x0003:-\x001f\\x0006SN¿:úüôèÉåÓ³åc"Ù#Yid;Ù\x0013®R¢=\x0002\x000bÚØÉS¹ÅczÀ\x001eQÙ#v²'\f\x001ahÓ$¶à`£\Wøæ\x0017ë~{Tõ~ÔnïÇMïÇ'fBx?v[ýqÀ\x001e­J{@y|\x0017{Â\x0015\x0013¯\x0010àÐðd4Þä\x0002¿Z<ÛûíI}dñ{í7¼Z\x000b/\x0016\x001a?Bt·èØúí±Õ~³{í7-qz&ØC\x0003ÚN[\x001eûíq=n7{¨\x0002Á|"Ô\x0002{\x0014Ï±ä²§:Ü^çR¹\x001fA\x001aJ\x0019kèÞ~¡ýæleÝëýðc</p><p>õ\x0015h[Å×Ã(sÉ¾7(\x0002~\x0001ÿ.Ö0Jaj%±ì\x0019Ì±ÂdU¯~{¦BE´'\x0016*v1È0äñÕÒ\x0017¿\x001eß\x000f_?ûíáÕ×µzí±\x0006\x0006LR;Jô¨Ð(Ãs/!ÿ2î ü^\x0019\x0004Y]\x000c\x0002ígô×V\x001fc\x000f¹@É¿LxÀuå\x000eàq\x000f{|ø§\x001d\x0014¿i¯)Þ±VÓ\x000bR~wÿ&\x0012iØd`G"ßx]ÝÝàÄæò·FþLhPN3M\x0010JÓ{aÜmHN\x001e=;¹8³\x0012kè
+Ñ\x0003§à\x0008úðà¡\x0019ù\x0010\x0013xÌ
Ö»åwÐ\x0002^\x001f¤¨N)ê4\x0001\x0007´mw·»ºû±\x0001<¨Ñà'.\x001d~\x0011!þ\x0017ù\Ù?üüù«ó¿\ÌðØU]a\x000fÑ>ÃóCÊ4\x000fÄ Ù=\x0017kþ¶
}q¨éPïE\x001fb{µ8Kì$\x0001½È]vq°¡\x0019ýTÖècY{\x0004¾&þR­@Â\x0017[VÔt\x0015\x0016k¾t+üÔ"!¦\x001b0Ó\x000fD¥×þèêîn{jÜ9X9õtª¹\x001c´sëÂB^óäâb¡Y\x0017W]®º\x0003À` A×r½NúTßpb±JÐ'\x0004Bzû¡o</p><p>@(TcV]h»äj±jÕ¹\x0019ZvûÅ*MI,¯pTØ	·\x00185´"\x0017¬B\x000e#È\x0015ÍLBKnîf²À{½[o\x0000/ÓW:¡¬ôüö÷È4°9sèsfÊp´Ñ@Ð¼\®%qÃççSû) \x001b]B6º\x001b2¨J`²Ó\x0018ú8Cti\x0008³\7`æõu^Õ×Ahøêc\x0008#o[\S\x001a#ì\x0012JËÈÅy\x001cÂ<úþäU\x0008\x001fç¸\x0003Ü7,Ñ0ræ\x000fÁ¯\x0007_þäîêýG\x000fo¡%¦a{OïX¦L¹Q\x000ex å\x001fvµ!_n|ùçß\x001d=<^W3Ìâ7?þöëïÿýÃ4wvuF°\x0001¢OsÀ¢\x0003þñúO¯~¾¿{÷Ó{\x001c\x0006VaY*M+æÀó\x0007áü\x0004Ý³°Æ!úÕÜ\x001cj\x001a~wú§Wß_^<}ò\x001c¢Â³£4ýùµ­a}f¾\x0001áä¾~Ð8\x0017çzp&\x001bq¶ M8E¸â ÎC.\x00010·ÓûÚ\x0003Në)íqé\x0010¦>T
l)>Üýúþ#È \x0010\x001a@÷£;YÞ\x0008ÔJaÒÈº\x0012@·</p><p>d?Ç\x001eÄ"tD\x001aÀò{\x0007Iùå\x0012©Ü`üÑ\x0014úHç¨°\x000eó\x0000©òÒ!ÒO\x0018ýú¡FFø£\x000f*\x0010A¤E\x0015á\x00103	j\x0008à\x0015Aõj7¨Ð\x001fôAUXQU¡MªÂæ¥U]Þ©-Páì?ú¶j8DªÈ[\x0015ØF#T#\x000eéÐ\x0007 \x0006L\x000fâ¾Uõ&ÉLÁ\x0006PÐ¾\x0000P
áâªªýV\x0015J¾ñG\x0017T#Ml\x0002¤\x0012\x001a¥"ÒÈ±\x001eÒ¯ô#u\x0010cÆ\x001f_ýûwpÙ?:\x0017U¥»YX>/ °VU"T%}Õÿ²¿¿{\x001bùl\x0019¤ïnïÿÖpLY\x0006C¥\x0011'\x000f×E 	\x000cçÙ¾tNUÃ38¿;¿üËü9UÀÆ\x001aap½BÊµ \x00000m,CGv%:i	\x0003¦½«Éñ«çP-\x0007ï\x0000Óy¦\x0011¦ðf7\x00189w­¦N¦\x0000ÓyÐ>K«é%Áäv7á\x000bÒ}«ÉLù¼ðÒYT\x000f{3\x000eFRí·\x0018àw®¦áøÒyòJq5io~¢9\x0000\x0013
\x0006`</p><p>©</p><p>ô¥\x000b³ß'÷¾/\x001d½\x00116f~ãþ´´\x001fc¾ôìLËqcÚØÍ
Î=f#\x0010¦ÚÍiÂ1Á;;´âF>"ðÓ\x001bKNS¯ìa\x0007§»ïóÄÎ\x001c`:\x0003LøÖqg:vÈÞóý_yà®\x0004Åøãìú\x0008Dbjd#ÐpèÞA\x0013\x0012î"Ð\x000c!¤M~ÓÊOÝ\x000e\x001ezÐ¬\x000cK\x00014*³Æ\x001f_'Ðÿ}õs\x001c.\x0013bO.¾kÂçãÓT¥^RhÌ{2·"]\x0014h5¤\x0011ã@)cå?¾^°oÞÞó7\x001fb¾=f\x001fpe/ï>Üß´5ÌÓmÃ|R¼-Gý[üª=¤ü\x0014ìåÅËËð¿gT\x000b°<þè\x0002«}¸ÏÇ¢i\x0000+\x001cpX\x0002Xnß¸C¶Óy¨sëú_@Bòß?\x0000y70jÅði]½}ußðmÙpóàñÛR"D¥p|\x001fÌ#XÇý!Áó§ßÖÉóç§'«X\x0005\x0015\x001f¤_=V\x0011	d\x0004RÈ|XÕýõß`»*Èâ\x000fØ®\x000f¯î ¹×òq	ÅSÈçµ§oË)ü¶\x000c7|5\x0000xxr\x0001ù½\x0005·õão\x001fþ\x0016\x000f­\x0018ê³´°TBÙb?Ü8Ã\x0014¯÷òº6,ëJ¬¿T@©`Â4CüÑ\x0003Ó°$\x001c\x00070\x001d4¬D\x000c(å\x0007XAùÓoo7\x001fË\x0010º\x0018\x0016>¹\x000b¿_½¿º9º¡ð¥e3xëS×D_ ï Ý¡­St\x0001P+\x0019´btøä"ü~òüäì(G5ó;äç_?¾±?ÂÒÃ}MU=CÞýv]7ÛK\x0000:Ü¨È£ÎÒñ&%¾ð\x000eEwk;¦ªÕÓ×\x0017ó7\x0001øÕÿóî¿>Ä\x0010PÇ ib;\\x0005\x0013Ï±\x0010\x001bNcgS-x\x0011#ð²Í>\x0011×údÏ@³Ä,ÈðOe?L<õé\x000f\x0015O}d\x000b~x\x001b\x0016ü!Iyn>ð ¶À{ %Jk­$æ\x0007µà5øpÿáyXøKò9(¬æÔÂ*\x0003öHúê=ÊÂµ=Ú#\x0018F\x001bhìf­Ì±;\x0003i14'HEs\x000c¥Å\vð\x0003öøÊ\x001e¿=ZOÛ-¥D{Â« (|vµ\x0007¹ÎÑCEÀ~{<¹*Ï¢Îh²Ç=\){DeøÖíµwÛË½ \x0015î7naì!}?Ù\x001d\x0008¿\x0018Ì
Øã*{ÜNöXú9À\x001e\x0007\x0012#É\x001eÍùBîMW¯Gïõz¬M\x0014ÐàÞ4\x000c\x0010Es¬ { MäËØS¹7½{\x000bw]Û-
à¥ë#£ÏGíí®¯fXzI8	xð)ËÔÅ=<µ\´\x0011o\x000c'ðÔ9Àh¯I)\x0016£°\x0003"KxZ¸\x0014eKDiÉ§¬_=¤½\x0015-Q±m\x0003L\x0011ÀÒLQjùJ×k,Mùß¨ë¥HthYî'ðV0\V~¢JK>å8ê±[ªª0¸¸ôR,6ÒÚ/c.MÑû¢±\x00173§è³\x0017Q61âÄò
 ×\x0014SböùTDþT¼¡\x0000MÌO2e¥]¨×\x0012[Zò)-[%á& Ð}9ì'qÐ\x0015Ëé¥,ç\x001bz-q¥%n\x0017KL¤=¸½°%NSýDº,O¯)¾4Åïb</p><p>p\x0005àîRàÈ¢%qÊ>Y²R>ï´³êtü/¯Ã\x0014/TjWáéc2Ïx­a¡×ú ßå¤÷ZAª;ÚÂ9ÌM`ÔuxÅ¾Ì©Â«£ïrÖC\x0011/EÈÁ\x0014:Þ\,â-*Z;ÙRõ|ÃÞ§\x0012\x00049cLï*®%í1þEâ\x0016^ö|ãÞ\x0006%"³\x000fRéË?êÞÉê´çû\x001c÷^P\x0015"\x0017tbÆÒioÍ\x00179YxuÚó}{\x0013¹\x0000Rd\x001c;\x0005Sª6²;;1sx[1»­¼¾ºAz\x001d\x0000Þ`±\x0014¾@\x001byeF_¿òÞ¶l³×'gHµ\x0003ÿÞu³DiÖ§î¬ß,<ZÁ,\x0013Å£YÚÎÂ©Ðrn¶%K³>õl\x0003fÙ9·\x000eæYÔëÏ\x0004k6[ÍR¥Y:¹M¨\x0012Ñ?\x0014\x00048Õ/¥zÀZ#ëUº´êS×o\x0013Ø¡É@Ò\x001eo\x0006Ìij:àºå0j5Ëf}êû\x0006Ì2IG6}Z´\x0007×È§eK³>½÷\x000c¥P5%-P#$³,úA'¾¤U®´êÓ;ÐU\x000eïtÌp\x000fs-Ñ*Ï<\x0005®ãËåK³>½\x000fõ\x0005¬p¸\x0007\x001e\x001dW\x0012ÍÒüZîð0vt\x0018\x001f}w\x000bCy
ýpôâÝõÝ\x001dô'Ü\½ûsS?a\x001a-\x000bñÃò¢õTN%ÿãç
;úî\x001cFû 'úò\x0008\x0004¦/ gáìäù£ï\x0017*ÒÙ6QÚ&öµÍû$í\x0000¥F\x0003"±\x000b\x000bÜ`Jö\x001a¶vÓ\x00184NÆÉ]³ã\x0003(®Ñ8Þ^¸åÂÉ¸qª4Ník\x001c\x0017]É$\x0015¹bt\x0019áb¹-qØ8]\x001a§wß\x001e³EÂÒk£¤êZgà°e¦´ÌìkY\x0008¦$:\x0013I®_QbRåÎaËliÝ×²pWÁ¶C¦,\x0000ç$])µX»R\x000e\x001açJãÜ¾Æé\x000cÐ«>\x001a'òÕß¬fÇ\x0007ó¥q~ç\x0003ç*\x0006\x000cØ\x001b<àè\x0002mÙõ$EfÓåÌæ^ÆéàJÂméÓ7g½sùøÖ_öãuh²wl"0òçÀ\x001aÞ M)WFøM«"\x0013¾shÂLn³ñ</p><p> vX@5õE­«B\x0013¾ol\x0002zAäñFQååYAaÝZÖjÐº*6áû\x0006'F¨$\x000ea¥Êg\x0001
ì¨òËs¼MøÎÁI._³È¸Æ©üêÔÊ8ê°uU|Âw\x000ePíº§4\x0008Ï¦Ä\x000f3Ô³Z{\x0018´®QøÎAJ\x0008¿°µÒå¡Òéò­\x0005ÿÂW\x0002^\x0005)|ç(ÅÄT\x0008U2[G5V!Å\x00176®</p><p>RøÎQä
«*\x0016øÈ}cf5Á0f¨Â\x0014±obÂu.)\x000c\x0004ñ®Ê`Z/Yç¿p"ª0Eì\x001c¦p\x0013ü\x000cÚË0Í\x0010"vº\x001b°/ýîê\x001cÊÎT\x0016Ìù!Ç¤ð9Aôe?;Q\x0005*bç@ÅÄÆtaé<PÔ# WÛ\x001d\x0006­«\x0002\x0015±s \x0002µ6¼\x001d$ÿRÌtõ«µÃAãª@EìEÉùs \x0016ÎÉ½|ûåAqëª@Eì\x001c¨x\x0008íuZC.,ZKTá`øÂWrþÃ_ë¬ó_ÿ£ÒÎü7µyoþÃÌ»®Í»þ\x000f3ïmmÞÛÿ0ó®jó®þÃÌû±6ïÇÿ\x0004óX\x0000X%üà\x000f1áG\x0014²÷GOîn¹¾iX\x000c"X-ÐÖ¤ÖøH!â2ÓÉâI@4²GO.Î-^\x0005¶²ÀY`¼\x0017\x0014dA\x001a=!\x001e\x0004µcå,ë°@éÒ\x0002¸ÓY`3¿\x0010$Ð\x0002\x001b¢
´@-\x0017m:,p¼´\x0000DY\x0006-°\x0018O]$@¨)Y0í"³´j·z\x0017ámdý1Z <ð(áì41þh·ê°Àêú;\x0018ÞFN \x0005*ÏS\x0004\x000b,ñ*ñåyv\x000b´2¥\x0005ºd\x0011ï² |ªä[Ã·\x000c¿	FÒøTø\x000e\x0016î\x0016\x0013­ëð\x0007¨W"qþÍÕÑãÛ»VmÎÁl+§^JrDBÈÅ\x000b\x0011\x0012ç\x001c=>¿x2O"¡Û\x0012º\x001dnÂ\x001dÿX`j3äärZX¼ípÉ\x0017¿ßVèÅ0®e\x0013xß²\x000b¤eçtÉ\x0006½M\x0003ì­Ð¥(¡\_/tN×0È¨â5L²bÚvÑé4cW\x0015v5]\x0005i\x0010»Ë$
yÒË=3WBÇ\x0001ìÞøcÈ!è4EËi»ûå¿Vð²Úî\\x000eíwï,Æ;\x000c¶¾À\x0011zG\x0010\x0006jGð¦Ú4Ü\x000cíHþO\x0015\x0012\x0005£æi\x000c ·\x0015ñåÒ]+x_o\x001b?´m ï\x001f¹È\x0006ÇÑ¿ïé#¨ ÃãÐÙd2ä­\Q&Ô®gPÕ±</p><p>#àÍÓ\x0002	V\Î\x0011\x000b³ëÂ\x0007ßBÊ¿¥»Ò¿ý&8E«ÄÔ\x0008#|"ó^°}<NÊ4Ó-\x0011äåù$õï¿ÿãä7ÿúgää9:}\x000f×â7M\x0017`\x0007\x001dªH|Ï\x001c}\x0006B)bËÒÈÎstòìáidç9:}\x000eWâK_4KêÒ,©w4ËbñÏ	{ÌpêURY:Ã7°\x0011\eÛÓ&Ç\x0018±E8ll\x000f\x001f:Þ*¹[î\x0001\x0019°	U\x0018§í·ëþ4
\x001bã½<ÌorÀg¿]Sê"ÚU\x0010]í`\x0017ç8UA|_ Dì2KÔ¯Kìûº²\x0017t§\x000b¯HÉÄJ8`ÖD)\x0013Í*Dè÷x[4\x0019\x000eTSüS £\x0019¶ìRµ]jO»£]\x0008S&³~ä×õÅ¼;8Y¢]xÜÏ.`ÏÂÆ# \x0000Èk@96¡¿]¾òðð¸ççÅVy{\x001fÓ\x0014\x001cÙåæÚ\x0001»\x0004«ì</p><p>uûÙ\x0015\x0002=j`ÔÔ\x0004'9ñIöÅ¼¡Ëé@/³ph\x0016WéMa °R\x0010\x0017îrqÀ,/+'ïåNÞHÐ\x001aEJ÷Ì²åõD<¹r»è6K:ÔÏ»ÙeA7ÞdÌaiÁ ]ålPsÀ.`ßÓ®p§aÇ\x000cÉX\x0015ÃÆn¯¨1Å</p><p>¾ÜvÓo\x0004&é2ÌÒ»½0n\x0014\x000bH\x001dlt¾\x0015\x0012%É0-Y_\x0006\x000c\x0013õ±\x001cw4ÌR\x0007:J:.Áçs4l¥Â2b­ß\x0018<ïùÆhNÂH'i\x0018xzcFê/è;r%|ò\x001eW;z{í§Kç9º{MIR£ÇU»l\x000b·­xUÎ\x0015>¸~§\x0007/n®Þ¦üE°ìô§w\x001f2\x0018Âàì@tx¡,Éò¹em\x0017g'R</p><p>ãèôÉÙÓ\x000b)\x000c2@T\x0006a\x0003tl|MySG|PSHÁí2¹{\x0005¾²À\x000f[Àé./rB\x0013ë\x0008wË¬\x0002íð\x0015+áºñ·\x0005¿Ú?j|ÿ(ïçåû¹,Xæï°@U\x0016¨a\x000b¤>\x0016Xöp¢OáÛM°å;P\x0005¦²À|c[HW\x001f°þf>`å\x000fÊ}á\x000f\x000fpäúèÕÝ¿þùÛm\x000b+»Q\\x001cÛtÁ$Hb\x0004j|Ìxx¶¬ÛYÙ_]¾>_ e'øÿ\x0001øÁÞ ×\x000c7Ö%\x0011>\x0015@@­|GðÎ\x0012<< ×aàP\x0018×áx,twPÐ¦tÓfü>BDüð8\x001fd\x0015°½Æ¡\x000caÀO,óÀµ#|i+áÇç\x0011ü</p><p>tÿòK\x0018é>ËÃ\x000c\x00087÷m\x0004«\x0006\x0018­\x000fúRÂ"QùìþèñíýÝûw7MÕ3«gÌ\x0011gcyKÝòòèñùåÅó§gëÀm	Üö\x00037LèÔÏÄ¬wøÁ:Ë\x0017bY/¤\x0011vÑ\x001a\x0011`çÖ®\x0005WãÞy}L\x0011BR\x001eC/Ívà®Ú(nd§Ì=UÁ´¢\x0013Jå\b¸._W-\x001dZ\x0017-\x001d]Ðm\x000cq+-utø|=YÖàh>W#tÎF ûpb=5¸FgqÕ}nF±Ë¹\x001aúÕÝÛë_gq\x001a·\x0018Zrº^\x000c</p><p>ôÈè¨¬09iÁ½ºäª>ò7ç¸Ñí´ä&°Wt¾\x001a¡\x001aº\x0018n\x000cj\x0014\x0006èÔ§</p><p>åkªTûåþóFè²Þ0rhÃ\x0018Úå¼¹ÒDÁÎ½_>@ÛpzÉÍÐ\x000by,&\x001cj¸b¹wcY¤¶\x0011¹¯½¢\x001fñÐ°DD	!zÇ¤4Dï\x0019Nþ\x001d\x001dzÙ±\x0014 O\x001dK]ÐCÎ±l,ó¢KËÆËôÈUåÏ\x001añçÎ«iÖs&WPõþ¼\x0006è¦>\x001a*úÊEm)©	>\V÷\uS¯º\x0019Zu#\x001f9õÙcÙ=»'LÓ)º</p><p>]ÔÐGü"d\x0003\x0005\x0015äw¨o\\x0018JË]N£+~¨\x0014Â?£\x0014òï¿ÿãüî:ZòúÝÍÍUS\~4$j¸#ùG5BåÅò;¨h\x000cÎ/N£]¯,´¼e»Di×!ùî]Vã\x0014ÓZÞª N\x0016ÐwÙÎ)Þn,
;¤ß\x001d3,ÝÅ£aJ\x0010a \x0012û\x00106pº¶\x001b¦JÃ\x000e	x\x000cf*iC<ÐBá@\x0003¼±5\x0016\x0011ÃtiØ!\x0007ïaÒ\x0010·°6Á&IR6øÆüJåvÙ°Ï^\x001e²U¦´êwðuyH(&ÏÁ­VÀÌ\x0015ZµÞ\x001a|]¶4ìwð\x00034\x0013\x0004e[t\x000bÚ«¤CÛp\x001aôM\x001bñjOÓ@yZâ'¦ ¹*&\x000cÖ²U!ß1MØ'ïñf××æ0õ¤ÊÍb\x001cp7ÿ²¦]Õ¦ý\x0007½6]¿6½ïkûÿÉ6{\x0018XÙÏ\x001a${DSJN\x001e\x0013\x000c±KBF(VVe\x000fx¡!\x0001Àª)¢4å3B\x0006=¦xb\x0014\x0006^ZâP\x0014\x001dê\x0010«·hM4\x0018#Kc>#_ÐcÇHÌ¤+é3ÁâHx·1ª4æ3¢\x0005],g a[d\x000ee [¾±ö\x001b£Kc>£UÐe?f>_\x0004§t*å<Ú~än1\x0019\x0013\x0013ñvRÈ4úùFø:ö\x000f=úù_ÿ÷}ÛÈ¤!\x001bl2úà2ÎW¤XñZø:ö
=úþôùÒäI\x0019y_\x0000£6À¬¢D\x001bbÃ|\x001a{lP[r!-6ê5Àã 
 \x001b+ÉØ\x0002F\x00169\x0016Ø2¿D
Å¼(Ø Ù°
\x00018UG\x0018Mÿ©\=ævSr¤Å\x0004k+\x0013¬\x001d6!àé5@±\x0007\x000fªbr¶)\x000bÛbS	N
`©95Ü>©0¨\x000c5 ±-SÇ&èÚ\x0004=nÇ.@\x001bÁÙ?e6\x001c{\x000bE}3`MÐÄØ\x001dßÇ!+Þ3¿,ò\x0019\x001bfjnh«
pã\x0006XHå'\x0003dÖV$äe'ZñûÚ\x0019ùqg\x0004y\x000bø9ô¡§R\x0010Ç¹!V\x0003Dm\x00187À\x001c[<uü5\x0019ß[éo5 vD~Ü\x0011Ð\x0011~\x0002a3y¬hQº%\x0018°ök6 þýø7l£Ê.\x0019­àJó\x0016Ú÷\x0013¨?a?ú	\x001b\x0006ó\x00172\x001ff</p><p>ñO½¤lYø¬Ý</p><p>V}Æ~ÆÁ\x0006"*ÌNI\x0012
´é\x001dØe\x0011\x001e\x001bDmÃè\x001cß\x0003\x0012ØÔ\x0013Þ\x0003õ4ûÐîïAÖ6Æ§Á\x0006O9|«\x0004Å§\x0001º¡÷°³\x0005²~\x000brü-\x0008F\x000cÇÖ:\x001a\x0011ÖBRxÊ6u¨m²!ÜÌ«\
üáAÙÜxvõëõïw·÷-½\x000er\x001bIE\x0013Fî#w¸\x001723£{½â¨;ðìäÅéÃÓRso² \x001c\x0005\x000baÙ>\x001b\x000c(\x0018d¡\x000b'tj1õ2\x000b\x000f»ÜIÒ\x0016#\x0004¥\x0011ð8jf8M\x00140IÕË|.À¬åÎ6bì+Ø`ª6ë\x001e\x001bløG\x0012±\x001cè½\x0003åR4båÒÜa\x0016\x0011Z\x001aÁÃ.`Æ¹dï\x001dÑr9·Ì+ÙaZ!À\x0008«Ì°\x0011&&#L¢Ôó±WlØ{7¹©)\x0012lp±)rÈ\x0006\x0011\#\x001b\x001cÍ×ñ,¼ìÜ¦ùº&#Då]áqÔ\x0008EÚ£Üxz\x001eò$\x0018qcw#\x001c«plÔ\x0008)82aL\x0013\x0008\x001ed°²ÝÝ\x0006_ùWx\x001cµ\x0001\x0018Çðp>%ñ
Vç\x0017±Î£Å\x0008_\x0012~üá°>ÖdñùXÄé1BW»	\x001eGp<ÓÞõL2/È\x0013-
F¸ê¨ónø¨S\SM\x0008DñMHM¼K!äØÂÐd¯ß\x001f}\x0013|ðÇ¬Nºø<ú& /LÛ)j4ÁPYïÀ­¥;¬P\x0007V\x001fØ</p><p>hîødEú(ÔäbíÆ\x0019µ\x0006+«­0ÃþI9ÍKÑ</p><p>ääV\x001a\x0015;ÚÕ_E|\x001e´BKÍÇ<+P{\x0006e«Ìj½»\x0011üÀáÀ\x0003`è \x0004¹Àd\x0004£\x0010P.×y»¬\x0010\x0007V\x000c\x0007ã\x001aÈd¶Âãgá\x000cÚr\x0013I\x0015òÀáØCÌ\x000e­}TV\x0004øh\x0005[©´[ÁUýqÃó¨\x0015\x0005]½e©±\x001d¦h9í(Ë÷þ¸¹ò\x0007V&\x000b,\x000c¡¦áð.rô\x0001ìaô.ä¶Î\x0006+ê\x0010*>\x000f[Áq²Ãkaè¢,ÉdºeñÖ.#ø\x0011ã.Ê±<ØÌpÞ \x0018a$\x0019Á÷·âà´àã§\x0005(ÔiÌÛxò³á\x0014\x0008óÍÛ°\x0005}\x0019\x0018a\x000bþ²ÎHsäH	F8`Ç\x000eFðÁÑi·÷aaí\x0011vØ?<\x0015W'^|\x001e4\x0002Øjð¬âDJ\x0018\x0008N|ö\x001e¢}(FÎ£\x0011õÈyß`\x000fÈ'÷$£Iâp×ÞÏÉP¿îb</p><p>]L¤è0Éæ4\x0014ê@hj½VPjç"\x0011gË¥RRtrÖ,àY\x0016.Z\x0010E/ÆL\x0000zOªöó\x0002%</p><p>\x00055a2·<D×nÐª4\x0001\x001eÇLÐS\x0005x0Q¤\x001cø#2½ñ^&¼IÔ)Syâ!P§ÄòÄëï>\x001e!°\x0017`\x000c¬zü\x000cM9}\x0007lø\x0015å&Ø\x0017§¯¾::Ã§5Üy&-á´^Ü\x001aæ\Ñ\x0007\x0001³H\x0017']Nn4\x0002ç5p>\x0000Ü8¤\x000eÀi²Ûzã+Ee¦£\x0016à2;ÿ¨L\x000cì\x0010D ß\x001aPC£·a4\x001cm¸XJm\x0003.ª\x0015Ç~àÚ¢\x0006\x000fWÎ,M´ÀÌ°#nUãV\x0003¸Ã1+RØæÃ¯\x0016\x001c§º
WËÓèmÀë-.G¶¸Éóa<ìfÈS¨¤;«\x0011¸Ýs§ØÊ\x0019ÂãÀ\x0016\x0017T\x0002b\²\x0006\x0003e#Ø²ÜM\x0013p£\x0008\x001c\x001e¿->Åb\x0011w\x000cÅ¾	Ü\W¸!Hý6p×ëÍ¿õö5î\x000fóÄ]\x001f=ú[9ztÎ'Ü*ïÇM²_+K4\x000b \x0010\x001c¡\\x0011Ml\x0002ntufÂc?pGãþB\x0008NCj\bAÞ\x0000AÊ8ðð3^%ÌD\x0003\x000b·RS(=þûïÿøþúîMÓeÒ¤\x0008\x000fw;Ø\x0002§!Bð¸½¤ÄÑ÷§\x0017\x000fê\x0010¿Ú\x0016yì`cøÃ®áØ ÄD\x001aw÷¹\x0017B-\x000b¢´c×5v=ÝZºÆ	å±m×\x000b$t\x0001þr´Õjú-y¬¼A\x0003 áÙ\x0000H	l1#I\x001a¥üò Y£\x0001\x001c$S</p><p>\x0003âó \x0005!nÄÞ{\x0001\@i\x0007	7éÈÃ´§\x0001I2@ÊA\x0003<³Ä\x001f\x0015V\x0003'²¼Ñ¨\x0011¹.vµÀ\x001eX`-\x0006ü°è?½Át\x000cÐ©ìù\x0011pÉ+\x000f\x0014\x0007
\x0008'\x0017¹ A\x001dÞr¤"\x0005ªí]_ôº¶À:¢?ø+P¼6\x0000\x0007O1CËá\x0014ã(/â\x0016ô</p><p>ôò4Ùf\x000b®x\x001a\x000e-fÃa`vÒ7\x0004\x0012\x001eÚ8\x000e³cÅÊãÔr¹ñ{fÎ¯"JSægÃLúû`6\x001c\x0007j!µ\x0015Õ~[diËühx-@ú¶ÀÇïEdx¶¬ÔÐo*\x001f
o3FCË(Í¹{\x001c
4ê$\x0019ëa Ø`.\x001f
oû`tæÜ	+ÚfÂûÅ££ß\x0018S\x001asÈÓe\x0001i¬èI¢ñN3¼ÿ¢ç®¶$M,\x0010e_\x001cþð \x0014-¿>zqõSËà;\úT\x0004g(Éà±Ú7Âl:\x0008O^<Y\x001aúHÐ\x000bÖVÎË¼\x0003;0ûà-Î&ª¼\x0010[¡°v¹ÀØ</p><p>]ÖÐå\x0018tKuEÁ­:N\x001dá\x0016EI\)onkèvlÕmª°\x0007ä(Á\x000b«î3öÝ×Øý7±Ûc\x0011ÑêÜº$ \x000b£</p><p>ýþèáõ\x000fW¿7Ô¢E¸{¦lr&{®°cÚ¬T²\x0008úåÑÃÓ/Oþ¼Ýñ</p><p>»ãcØÃ§\x0008¹ÅÔxÏ5CÅlx\x0003Ê[áûG\x0003àÃã\x0008|©±«DX/R°í¹!úYãÌ¶[ÿfô¼Z|x\x001cB¯,VoEì\x0000ÐiñÞÚÀtÇð¹2F\x0000?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
Instances: 9
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-MEJs95Z/omxn3TXvSLWyK5wtscM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `8f3c-gfG+P67yFyIFmwt7DJcFE37xcQc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-MEJs95Z/omxn3TXvSLWyK5wtscM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8105-2RoW8oHR+2wMO/pWUtvrTE3i1m8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-bqOfxlX6Z3R5FCK8Jng0x6UaoD0`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-ebdq7wY3Xcn1wH754ARs29ueaEo`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-KtJk4IeM7iemyszqJCGYUuf9nck`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-fp7mACB6YwkvUbxVTPtMSTkYQAI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-RNjp9qhpApQVLInQSFmngEonNM4`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-lSMIckl4Xohky11p57bEWwets/Y`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��y��	��Y����t׽"�Ȯp��\x000c</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{},"isSafariBrowser":false,"__N_SSP":true},"page":"/bas", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `366405469`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1611761132`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `273111588`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1439655420`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1919628686`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `912784966`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1838188997`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `831362559`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1745640841`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>366405469, which evaluates to: 1981-08-11 19:17:49</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
