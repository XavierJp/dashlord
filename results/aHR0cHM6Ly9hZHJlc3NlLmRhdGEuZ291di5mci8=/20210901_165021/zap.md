
# ZAP Scanning Report

Generated on Wed, 1 Sep 2021 16:43:34


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
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 11 | 
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
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/azay-sur-cher-des-adresses-d%C3%A9taill%C3%A9es-hameau-par-hameau-et-rue-par-rue-6ba16cd18738" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/azay-sur-cher-des-adresses-d%C3%A9taill%C3%A9es-hameau-par-hameau-et-rue-par-rue-6ba16cd18738" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#ni4M</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun
Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T
T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ó\x000c½ÞO\x0006ÁoÄ\x0003f´`º\x001aº7â?±sOÀI¯ùFÊÁÎÁfç'7@ÇÃÂÕg^êÆáF>·\x00013\x000fÙ¶NÞìhk¢hÕÓb\x0006ýÍgÚ¶\x001b1\x0007w\x00046wä&p\x001c3õ7Ç¬x£ÎäiL\x001cÜ\x0011Ü\x0011\x000bd%Å,2
&e­."ÌI¿ÕFL?`z\x0013fÉÒ"èØæCÔ¦wPC?lB8¸M4¹MÇ\x000f2Ö\x000bÅDÔö[ÅE\x001b0qÀDÛjÞ}DÁ]Z\x0002³HÃR`r\x0010sðîhòî\x001cyìM,=¢#è\x001e\x000eçG8xw´y÷Üë¢Y\x001bZ\x001b¯½W\x00135ÜlÄ\x001cÜ;Ü;\x0007!mÓ
¨RH\x0019µæ1pBw\x0010sðhò®ºw\x001a¯
 ªÛE7îA6`Ö\x0001³Ú~ô(U\x0004\x0019»ßtY-=NG·aÁ½\x0007£{÷2Sþ­ ÂÊ½Ë\x001eB£±2\x000cn3ØÜ&ywíXKÇ$5J=a<\x001da¹	s¼ì°ù#ÊÝ´9°è,2ô¤«Y'
\x000b\x001b1\x0007C\x000f6C'¤Ah»{½I\x0008óa«[0ã°5£mkæ~-\x0003î"©ÐÝ&\x001dÜ®f\x001cöf´íM2tYMà:\x0006±ó*^3úÃ÷pqØÑ¶53j¯\x000bpî\x001eÕ\x001duÌÃIq\x001c¶f4nM\x001dø@§U\x001d%ÎºPâ5#LZ6b\x000e1(Úb\x0010kÓÈjÂÅk:=bDÌfß9Ä hA\x00114[4¤AÄ cN§@oÁL¡'¡§Òtt]éEetxÀîQCO¡'¡7éÍYõ\x00026U\x0019à\x00041Üx]Þ9Xz²Yzê\x001dê\x0010WÂu¨«\x0019ÿèCRlI1ÙM+ \x0003\x0016va*\x0015âåsGM(\x000fÙée*#\x001d°zRDo\x0013Ò
å
ÃG¶Ýxx­Ô ãUÖ\x0007ã\x0014dt$¤ÃÙQ\x001ef¶9MòFB	ÏI©C×Bá¨G3â2x£bóF´òÎÂí×rZKYÏ\x0017q&0³\x0011sðFÅæèPQ7Bï¥ý/é\x0001=¹é<M/*6_D0rVãÎp§kÙÍÇß¨!Ú9d\x001dÅu\x0004¯á~_¾×nÐ}Ñ
U
ã\x0003 Í°è;\x000bbÔ§µ¤DØ\x0019\x001dÅ¬\x0001U\x0001a\x0018Ê_¥þðF_Ú\x0006ÌÁªÍð\x0012BU©AòjBx£Lz\x0003æ`BÕfB\x0008\x001aÎ1¦{'¾]¥õ)Ñ<üjU\x0007\x0013ª6\x0013¢ÄMÞ0\x0005\x0019qN?yUK/6ë`BÕfB<\x0015V,=CßQA)\x001dÎáê¸W[âÎ:líè\x001bN\x0019þÍõG¿Uøü$¦wWoý6SÄ\x0012Hm9\x0013G÷¶z\ã\x001cä(çøØïl¶Î^]²¸âù\x0015¸qÊ\x0014 â¼Q0¼s|îw6cK¼,I_ÒSÔë8¾Û>Ê9>ø;µC\x0017ÖÁ\x001a¹æ¶%2\x0013Xtí(çøâïlæNI<\x0010\x0004\x0017¤5>-ÂÂyô¦Ë_ÕÌØf\x0004¾\x0008g½×åÔÇtðG·çUÍ­hÆ]$'Gi7#NÍàS=zä¯ªfle3\x000bRäg§\x001d \x0017
I»¸!»£Ç6U7c+q¬w-n\x001e´±®xUÎÉX§£\x0019Ù*gXÄR.\x000f\x0003.º\x000b'Ê\x000cÈþFuïÓcå·ÎP\x0010¾\x0017+¢\x001cT.\x000fN%Ìr4\x001aÁUéÍ\ö\x0015\x0017èä!¥	£Q¾Õ\x000b²s4#[ñsQE\®\x0019²VÃ\x0002\x000fb=Ê9­.E\x0005t=cÇ$\x0002Dy££t\x0003åhD¶z\x000f.(\x0016Ä¥|ò£ÖuåÃÀ~,÷ð¦z\x000f_k\x0017äv\x001a5õT[é\x0001\x001b9G#2URx\x0016êèU+)\x0012è#V7º\x00197pâÈi)¥ðõr~K}\x0004<eÈ]¶Ë\x001dvJc)7ÕRxV\x0012É3®òºH+OB:Ê\x0019GNË¬_¦\x0018¨Tïýªñ[a"\x0005¾\x0011sôI¦b
ZÎ £û\¨þ2E\x0017s2$b#e\x001e)-\x0017Ç´AäX\¢óax+«txs¾ÓTóA«©\x0012åec¤Ð'y-¦Èùè\x001fk>¼©èÖÓ~¶KE¥#øêCÎí5L§joá\x001c>¼©êcQ¨\x001acZÑË,&=pä2Ó¸ØÆéGNKU¯½ó¬½\x000eû\x000ee=oõ&oà\x001c©>Å×RÔÚ£\x0007¾oë©eÆ¹\x001cíÍ`ñòÓ\x0016|)²åedX\x0004-V¨ép0
Wm\x000f¶`Ä\x0011¨ù¥Èe\x0000,yÍAêq3\x001acQ°Å"ZÃ6ès&ÙSõCoi´oÀ\x001cc©ÞÇó@\x0012IAÈ^´Þ'9\x0019\x001f	ÅM&2nä\x001c£Q°E#:¾µKº\x000c¹b\x001eÚ\x000f¿\x000fú0\x0006£`\x000bFÅëq#bQÁÔkTÊr¹vs\x000cFÁ\x0016\)Ç.ÓqX'ÝöÀQ§4yyS¯¹?kE
ÖõÔâ¾2ÕØÚÆ9\x0006£h\x000bFt\x001cKºLÇvye½Ä2è£ûs¬Gó¦4ÏÃäñþº~éÙõÚ\x000b\x001c¾Mc0¶`D\x0014Îeé¹ìÝÌ´GëõýX6çMusgÌHÓXL¾O`®Eeû\x000f_ÈÇ1\x0012E[$rØm=:-<\x001f|\x0011þ[j\x000fr¡ÈTßGËÙ[¢È0Äª75\x0005\x000fgIqCÑ\x0018|7ô\x0018EX5E*FwüZv,Bô¦*DÏ\x0013ò¤(òD{qHÚ[]ÂÑæj?\x0016!zS\x0015¢ç¹ÊRPSâ<¹-§TW »1çiÌ±\x0008Ñª\x0010	nR\x0014WY\x0013ÖýåGYýià4¡R£êªg\x001eã×0'¡Ão0iôîÉäÝKEB<\x0010\VÓI\x0011\x0008ºÃE >«m«ÉÏ¬Íq\x0016WÔqêC&:zÒÈãjfÛjÒl¡r\x0019\x0003\x0010\x0012½`\x001e\x0017Îc´Ì¶h\x0019CVÁ£b|,SÎ3\x0019ë»s\x000c¦ªNÊ2.'æþ£ª\x000e¾\x001c¾VÈc´Ì¶h\x0019Q:·É;r¾ÌZ¢Tê
]Ä
£Ï6\x000fÏúJíg/±O\x001c\x000eôÏ²_ÙÇÂNoªì¤åôzÐHÁñÅg[Nì\x000e[Q\x0019}R±ù¤ì5®¤þi¶,§w3\x0015çmãAÃTêk Sz[N²{©àæá9m5ý±\x0003\x001b(G×Yl®eÜ¬f\x0010¥NZM9\x000eÑjæ£Ç¶±TÖjeÕD1vÊ:£.géóRv×û±VÖe\x0013d°K¬\x0004'Ýð¸\x0011]}Øc\x0014éPx\x0004¶Pê5üÑ®F?\x0016ÊzS¥,1Æî¸1\\x0012ø^>WãÑ*n?VÊzS©ìò\x0019$s½¥$F½øHÉ8\x001b1G\x000b2Ê\x0012¦ã'v\x001dî£`\x0006mÐ¡ÃçÑp9ÊzS­ì2B^je3·¾ÈùRU»óöÜ\x0006ÎÑLÅ²ÄÙ[)¿Ô{ã\x00184ý¨e2Ái\x0013'¸+Á\x001c\x0019\x0001ÈÌ\x000eCè3¸~tôH\x0004Wm¦*Ôe¢yÒ°S14ÝÕ0\x001ct0V¡©
8A«;s®ýþ\x0003zz\x000cG;`\x0000<	À'ù ËÐ\x001eÑ£	^^³øÈ~t^ûÔ}ÓI½_T\x0001d\x0014_ï7Îz´ú\x0018®tsLÂ9\x000fÀíÈîé\x0004Ôç÷y\x001d~7î7`Ö\x0011ÓvÚpIÞ_\x0008³Þ\x00079mð«KÃ\ª\\x000fq4`¤!ÎÀ!}ádi_\x0019(çäê8
UÀX¡\x0004¶
¥â}&s²ÂSVN½ªA8ÑÁXù\x0003¶ÊâHüxÏ\x0005©È;Ôí÷ñU\x0018l¯ÂòÍ¶=}êú$X¢nÏr4ùñU\x0018l¯Â%:{áÚ/YÍ¤Ç"òyG­}|\x0014\x0006Û£pæ»Ø64Æg\x001d\x0018BË)ç
ZÎ£\x000b0¾¶íµ5ç$w5ÒX­9Ç¬/0dOGüø	¶WÌtçyJ»xzLã\x0014II$wðÌ\x0001ãë Ø^\x0007s\x0006iÏ#ÎÞ
Yzóè±\x001dÆ7°½¼å>ü\x0016\x000e5ùD\x001d\x000f\x00016¾Áø¨\x0005¶G­Ìã«äwG¯jþÖ÷\x000cxØÆ×"°½\x0016å¤ºÆ\x001e¸8^~w\x0015?gyñ£Qs|\x0001Û3LUý\x0012ðg<ôC8ãÑC\x001c¢\x0015`R­ð~ì¦}¿\x000cÔ1¼Aj©øÕõ¨½ïE`{/Ê1Ú\x000f­gÖ\x0006R\x001eI"ëyT\x000e\x0002FÕ
0ÉV\x0010fº\x0017Ê:§(åñ_}´öd³ö\x0018D\x001d8òÆ)Õñ\x0018òÑz\x0000H£µ'µG/Gb\x000ftÔ\x0014Å,N­½\x001c­Uñ\x0010lÏ9$yØòÀ\x0005È\x00125ChÄÊÇG9G+²½\x0013òý\x001cáÐõnq
B GÅ_`|\x0003Û\x0003\\x000eÀªI\x000b§÷:$ùÝy;\x001cå¼µÙQpí0³N§3*æQI\x0018_¶Àö²é|Ù*<=\x0011©Ep\x001a4±£æ>¾líe+c&\x0013ú7v!êrÂñå\x001cõbûÕ!éØW$ï)åÇt$R+:\x001cÊè<Íy\x0002ôÕÌüÚ±Pú¢6o\x000ez\x001a³?zµýè¾êPZ¬NKè°_ÅrT$\x0000êè;«Íw\x0018{½\x001cÜ{\x0012¥vGOÄuôÕæ;}Ð\x000eRYNogãñÛÄ:\x001aQµ\x0019\x0011!¶Ý\x0019 iâN\x000fpÇ\x0005¾`Ú\x0000Ö\x0006qf¡ê\x0003jC ÓÉé°ä ºQàÚÙÌÈ-\x0015 ³¨|\x0016*äÑ¸\x000eGH
¥Z¤qÃ\x0007\x0002²^®¬\x0010N<¾qä4Ù\x0010sFáä¢\x0000/R\x001b\x000eÝAÎ<r(Õ\x001e¸\x001bWNÃ\x00147¼r\x001e\x001d³n\x0014;v&#JUK|(:88\x001a{:ÚHþJ%ÞdD©.5Ü³è)\x0013JÐõÌG»\ÑvämvTªT\x0006,Ã.+
§f \x001cÝAÎÑ¼ÍJæ\x0016qæäFB©¤££r£ÊièG;ò6;*ý-VëW\x001agÒß½¦Ãë9Ú·ÙQéç"n|Ëº"Tùðô\x0017\x001c^Ñöô\x0013YLâÌ!CîG\x0013yÑÀfF¹ð\x001a.Ú	IË{³?Z"ã\x000b1Ú^\x0013·ì\x0014á¬ú
IÄ!³\x001e¼¤Ãñ\x0018m/Ä)GM¹UKÄ\x000c ©\x0019e8Zßã\x00131ÚS\x001bd¼prI²{ÒÜ3ãÑ78¼\x001aZb{"NI:\x001e}LIõ VÅ<zÃ«ñ\x0015¶×D\x0019\x0012Ê¯Î¥üU05hætt>\x001e^Í¯°i.ð±]:úG½­\x0001é\x0016ç\x0013ÇÑ$yT]@êBJÚ_ächëéûz\x001e\x000eîW6lª\x000bÙ£^Îrò)*ç\0ÛÏ£ÞójÒMu!ñSL\x000bÉù{d)H/!æ|´1\x0013GÕ\x0005´©.PTd¯|VU3 LìÉçaÎÑ+ÙT\x0017RL,%\x000fZî	AËùs9Z£\x0001ÚÔ\x000cR\x0004~g_8!èe7\x0004-aÈG_4q¬\x0007A[=H
/\x0016L*æ	(ZÍX\x000eW\x0006àXi¶J\x000b'j¢ ´²NE\x001dy¬p\x001e5ö±.\x0000mu\x0001	³vÎüè U@å°\x0016ïíh{oO<éIV³õ5N­R+ñ¨\x0006!ïíh{oO\ÛÝ<_6î\x0013xí',É\x001fuJãû0ÚÞ\x0013èÃ+ßÓÊm"x\x000c¹Ã9È8|\x0001MÓ\x0017(¶¤ýà\x001e\x001a;\x001cþÙÇwl´½c]ß×ö³SÒÞv\x001d[CëyøBq|ÈFÛCvò:0Ï³EVN½¨+õ¨b
ËB®9³©Ì"q£VKåy\x000b8ÍõÂæ8åhD¶çáä2þ,«@%,X¡QV8|í9ö¢­2K=\x000fó\x0011)Êjª¿:\x001e\x000eã36Ú±cÕN\x000esÑ\x00168õ-¦âÑñ²8>c£í\x0019\x0019ÑQò¦\x0019²ÏÑÕp´3\x0006Ç	!h\x001a\x0011B¿{?\x0019¥Ú;N è\x0013\G{àplxE[Ã+\x001d|´\x001c«Ñ¥´Û'\x0019M5\x001dÕ4À±.\x0000mu\x0001zÊóAf\x001dyÉèô~¡¤xt9Ç²\x0000´\x0005DJää`Ä=\x001d¢£å£^+ÕT\x000fsNÞÖðXHr\x0010§Å_À¾¨-g>ÚcÇ+Ú:^cÆ¾;y²°åtêòQQ\x0003\x001c;^ÑÖñÊt{î×\x0013ï	¨\x0001%\x001fÿÙG/_l^>iß/-·B\x000b\x001fôþ«£ý8­ ­l\x0005pÒÒt¯ç¶qÖ£/îX®\x0006¸Ú¼<%ù\x0014ÍåUÍ¢ÂÑB\x000b\x001cëkÐV_\x0013c/í.-µåÔ9âaÑ>9v\x0011£­½§¼Å°ú\x0008×ÐÇ^8Ýá7Í±\x000e\x0008mu@1ôkd\x0016G\x000eïE0 \x001cÚ\x001aËÐV\x0006$\x000f0\x000b&yQðÞ)&\x001eYc\x0019\x0010ÚÊ":nq^8kÖ\É;¹
îøEÈX\x0007¶: å\x001d³yùêû\x0004=WdjUpé¨Öl\x0018KB­$$²gûÝ+T5#§sßËGEGÃøD\x001clOÄ!jæ2.FºÇ\x0017õ¦Ó\x001f~	c[a°µ\x0015òDÖ\x0010\x0005® ¼rDÊ=Ä}\x001evòa|	¶Ç\x0018\x001ed²Ä"ð\x000eåW\x0014(£PâÑ.o\x001cÁöÆÁca:\x0019x\x001fÄ+Åªóµh±6iQÌ3ØÄ<£Ëz\x000fÂ]¢0ìD\x0000\x0016ûh=\x0018u\x0008M0Ô(sÀ¡6Ò­çè\x0008'ñhÌ\x000c£Ä_°Iü\x0005\x0016ê\x00061ö¨ÁÈEÅ<*±\x0013Fé¼`Îã©\x001b ¦\x0001[T3ÄÔ\x000f\x0016z\x0016üÏÖ<-ã'Sý9öRd"ú\x0005ÄÞv\x0010\x000e_vÇ:¢òµ¼\x0005ï»õpÄ6õÂ[¯BòÑ+\x0006#jp\x0016Rà&|\x000eäyöð\x0002AÕaBÚ?!ùÌ \x0017õ
úàOýèþÛÝ\x000f¿~úòáãoûHÝò`¸XSt\x0015å`¼Ôø/¨éÆ5ØÛ»\x001f½|ýîÅ«·Oñ5o°óÒÁ³¥$Ä[Úhù¥¢Eq§çøí¸iì¸\x0005¤\x00084r,EYÞ,çäTãT\x0018{\x0003oL\x000bo?°E\x0008ëç÷¿Þ½ùôÏÇ#[IEf\x0011Õ~\x0004:Ö,:ýéùÃË»7¯xv{÷
.®qÑKÇûv\x001ce÷¥Bf)Jy\x000b7ÚxÃ7À«å#<ñY/ñéïÖõÍFÞ¸æ'ð.ïK}}7éÁÖ÷ksÛÃÖ¼ÉÎ[ò}¾¬¯ÔÞ¦¢	vÞîÁÍkÜ|\x0002.\x000eÛWqýeyM¸e[ì¸U}o[]Q¥çæ\x001aYÝÉ°å=¼uÍ[OàUÑ¦¶¼2ä¡îÙÈØ\x001d¼yóuV`pÜw³Z`É\x001b¤\x0008××dm~\x000c\x0016æh±Ìo[-°LíËN\x0017yM\x001bâ2©s\x0001\x0006;0\x000fÏ¹,pÔÄ,\vð×yù\x001eà!¾ys[vD­\x0015öº#r_aÛ\x0018\x00027G8:Õ{ÙÁ-È(\x0005´Àñë:Î=¼Cóæ\x0008·\x001cu ß²ÀR Aey¿¾DØ\x0003<D8o\x000eqàR}Yaé\x0017ÎE¯\x0013bô5ï\x0001\x001eb7\x00079Ú\x0011áÞ_VXªÓ2úË
ÛlnrÞ\x001cæè¼¾<¼õ\x0015-Qcì+lójCóæ8\x0007.KÒzÚÔwZàI\x0007Â\x000e^\x0018Â\x001c\x0010æ*ÈÃ²À¢ÄQüjmÀC\x0013â\ÓrîNB¼ZêO\x0014
ì\x0001\x001eâ\x001cØãw¡\x0007f\x0007zWº\x0013\x000e&ÁEÀ	."¾!x}Q|ïÍ§Á`qpÅåÐÏ\x0019«°\/¼&\x000fCÃ\x0013¢\YÎÛ\x0016¸hã9\x0003Ò0X\8Áâøn\x0007®FîÒl;Ø¯®û$wÿÉIx\x0004ßrK	Ì+¯6é÷Ý\x0015ç®Ë	ÌÅ¯ï#²xbö ê)\x000eÞG$¼ºâÊg¹Nû² ÿãýNX(K#\x000b×<\x0006ß\x001bA+Ê&ö¹ÌzÞ-¼ß?<E
kR0²ôHn¤<LÃ\x000b©¨Æúâg\x0002c[IqMVR©ãá5Í\x001aÙªN¿ôy:Àm+i\F+©kSixMA0ådÌ2½\x0006Ì²Æ,FL®tN
+:§­ZïK	0o$]]8°99#*÷=¬ÖÕIE±/Ñ°¨~°'o5¨\x0008­ø9Ôè¼öáTçuUóìj+j\x0018P\x00115ä6P½×>ÛeÊOC-nRq¶\x0015u°(o5©è[Ñ\x0019m\x0000:U|Ê2AGöêLd+j\x001aPuU±\x0015Jñª\x0016í!QÍ\x000fZÔY\x0011ôVÒ<f+©ëJ\x0001K¤¸^AUÍª'¶¢Ö\x0001µ\x001aQQF
\x0013jõªLC\x001b´
j)ÎmD!ô5ö£o	7£VM®ôÒ\x0007Ú\x001c\x000f¨0\x0004T°FÔ6¬¹ª®çFjTyöö»\x0015u0*0\x001a\x0015eL­(:Tn!,YÏá²UÉ\x0011\x001cO¨`°*0Z\x0015¥LíÖVµænU¬5ØPãlì×VÔ!\x0001\x0000c\x0006ÀÜ\x0001,ÕÜêe<ª\x0016unE\x001d\x001c\x0000\x0018\x001dÏI÷jr\x0007\x0008ªn<«CÜC²ÆdÅgß\x001aÚ	Â\x001eTt>\x000c%qÇ]\x0015\x000e®
®IÅ«&(:Ò¤¸(^µÎÞL7£\x000ei\x0015\x001aÓ*ÏÅ\x0014U\x0016µªdMéc¦ilE\x001dÏ)F·êL¸h¾*ë
ë¾jV÷µ\x0015uÈ\x0000Ñ\x0001ú\x0014\x0000\x0014¡\x0012µ>2U©eäËaÔ!\x0003Dc\x0006èé´\x001a¢\x000e§Ì5*êtüßVÔ!X¡5XÑ\x0006-²\x0001XrGoåQQ;U\x001cB\x0015ZCUì\x0007\x0000\x001eZ§ï3U9ý¬ j+éàþÑêþcè6¼»È%i ò³ÙÓ\x001bIÃàSÕ§F×&\x001f0iQÙ\@Ý?ÌôR·¢\x000e*X\x001d\x0015Ùdª,µ%JÎRâCût¦h²
\x0015pÌTÐªDhãcµö2Å\x0012t«N§e?s\x001dï*2÷^^>|ùíîÍ§þÇÇ}¸\x001e2Ügðr\x0008t²já*¹8©¤¦?½x÷öîÍëçÏ¿ñì	èK&ÀÐèÏ.\x0005T\x0019Ú"ÃEb?d¥i4Ø\x0007
\x00034\x0001]U'8ZôV\x0014\x001c>&ç&Ú;Wú?\x001f¯Öúñ\x000cî|\x000f
;©Ô;aK\x0017]Zîzk}
g`£ÓráàB:XµE Ö\x001bïI»¸ºâþé\x000cîÐ¤à#\x0007í\x0014\x001bz^^µúç+êÏ¡n¯¹ÜhÕ\x00024QKIM¶îÅþý
û÷\x0013°=J\x0006aÜFöÊ=	×Û¸ÿæÞ&»\x001c¹÷Ü
ï
\x001e\x001bß\x001f§F7"¨Læ Cd0Ô\x0013\x001df\x0006IU\x0004YÅ\x0008fUi¤mh	½ÞVÒf\x000e3\Ç%ü\x0012îÀ uN½EI¥ãÂ\x000c\x0006ÙßåkMÀìMö#+µZ\x0015üWRãÆ\x0012 z\x0008Ý^u\x001eµÎ§çxº\x0003ÏP¯-¸^CÁ\x0004ð\x0019Í|´W\x000bóÙ\x000e>KÚmJ@ï\\x001ee9RçH¬ÌÈkÁós<ßç¸³Eá!ÿ¼4ï\x0005øªµ\x0010¯âÅ9^ìÀó§"­º×\x0000/÷Øºy¿Æ'Kãè±\x000en\x0007@\x001eeîYúÌLã$6à\x0015Æ!{¬#¤w6À\x000bæ4Ó1¯4ö·ð\x0015Æ!{¬\x000b\x000c1}é%ñqmò`\x000b_a\x001d²Ç<"+$@Eg¹GqÄW¯×|\x0015¯°\x000eÙa\x001e(ÊDë\x0007!R`óÈ}i¶¢\x0010Ø\x0000¨
óP\x001dæÆÖ&@AIi¯à\x001fØV.%-¨\x000e\x0003\x0001Àj«d\x001atüóJ
B\x000b]a\x001eªÃ<"¹ 8ÛBÊ\x0002\x001f\x0017[Â=y÷Sy¨\x000eópdO±{a\x0011w\x000cX
b^å+ìCõØa÷¢\x001d.8ð*¹û\x0006<]Xî±\x000e½\x00169v	\È¥Týbö*`\x0019[õX¥\x0019ØýKàà
B®Mç.\x000cD÷\x0018ãÒH)ã)\x001f+¹Í?ëÂ>t}xè\x000bxúTò\x000f£+YÚh\x0001,\x000cD÷\x0018Hn\x0002ÂÑG\x0000Ìñ¨hl\x001c\x0005\x0007­v8½67"|ÿýþËçy-1L*9Êê¬EÆbÒ¦¦ñõa÷éÇó÷ï\x0016ÓZ9³â¼Ãc\x001bg\x0018Á8\x001eèJZy5îMmÎN+¨-@m\x001f¨¬\x0013]©üBê<)µ\x001eô7Î\7î]÷Æ\x0015¬OÆd©(ùzO5ónâ4å\x0006íÜ¡Ñæ\x0011Î&^HK?<NwÝÌé
N×É©P¦dâ´{uLÃÃLtMû\x0015P\x0007?yqÇ?äûüý¯¿ß}YIiMO.V ¦!Å\x0012ËOîÑ×æùÛ\x001fÏÞ¿Æhæ¦Qsà-p µ\x0012­	ÑU&µ·!Ú9¢íAD-\x0000KË(éá\x0012î\x0003ä7q\x0019+ÁE\x0013£3ú.ÆiÎWbÜgÁ\x000fÌX\x0011\x0013ncsÆØÃ\x0008AZR(\x0001FM%6zË¿uÕhZ\x0018s\x0012bbÌIm,P\x0002æcÚ\x0018ä\x001erã-
)»vdð$è%PñÆ\x0003LÑ\x000cAÖzÇ \x001d){¶¤4\x0006\x0005ø\x0019¼ÝLÚä¬Lªi\x000c\x0005dèYÉ(ÓËÀ9o¬A$\x0002v-UßXXì1\x001b®®\x0002Çl\x0004RE³t·Q\x0011oÙ s\x0007Û\x0004;Ø6Aj\x001e¨2ýØÔ²/\x001c) Â]ëÙo,l[õØ¶UïÀl,\x0015K	ãm¯içFµÄ¨º\x0018-)£\x0008\x001cã¨ù×Þ\x001f6µ<OÿÉotìn{\x000cÇRºGà°\x0012\x0018\x0011roÝ~­uëhËØ\x0002e\x000f9¶x|þ¾iüié%¬þ<Í\x001eS\x0001kú_0^Þ|Z\x001bÊnÎè:\x0018]äQ\x001a\x0002·§æ)\x0000:3Ö~ï&Æ0g\x000c=>P\x0001ìCWÈQs\x001cécÍ·0æj1WCl\x0014¤\x0019*°5U°(\x0006\x001bêÜ±\x0010U\x000f"6Á(B§,fKIH@¬\Â\x0010\x000b=&\x0003ÿ	43EXÑh\x0002¤·ò¡v¡mb,,Fv\x00164/E`×¢Ë\x0017[uõ¤iB,\x000cFvYÂ'"$ÊòYôÝfÄJ·S\x0013£*v£êÚRPÆJ 3gõZÒü\x0000Æµ¿´Ñ¥´\x0019þ¡6{þvû\x0004\x0010wkÕÂ¼¥Ú1«a\x0005H¿\x0016\x0013*lªú÷õÉëÝÕ»óë³¥,[fvsf7ÙPÆE¡úR~'µmb®t®C\x000esä0\x0004yêË±º\x0005#ë%Í»Væ½»YÅ\x0008h\x001cEÐÖ³ð§\x000eüCu\x001cæ\x001afU0«!Ìù->\x001aEC\x000cpj
ïgakk \x000b\x001bCÐXV[MPÄ\x001eb¬Îë^\x0003]\x0018¡\x001cb&\x000bËE¸ÒB»@ÏBp+é]èÂ
å\x001034ÚP¬²M\x0007§bõt§çP\x0015ª!V\x0008aC\x001aF¬P	=òB+z?¶×u¨Â\x000cÕ\x00103ÔF\x001c©úý´£m^iUU ^\x0003]¡\x001ab'a¨ §ôn¦âd\x0013kwuÐ\x0019ª!f¨5¾MÐJÐã\x0018Î¦çí\x0010«ÃÖ@\x0017v¨Ø!\\x0019#m\x000f¸§Û#Î7%\x0017BUï{
t, ã3<r\x0015Çið\x001cuÐ3sðÕA\x0014+uÁ¬G0ã>¦ãÐ\x0007G-,ðÏÔpaBE d\x0015³)Í\x0008æ¯íÊ£WZhãY¢2êØè\x0015Ð¶ðÒvbª:±#,VXÞÐ²R\x0004³Y\x0016ÌrÄB\x0007.¹\x0007hÏªû\x0013\x0000]0»\x0006º8YìEÂÿìiL±%¥ÁESZÙ\x0004Uë ^\x0005­\x000bh=d¥\x0015ÿx\x0013´Ò®\x0004UkÐ\\x0005]\x001cvÀq(\x0005\x000e; hgÒÃ¶ÅCuUQ|
³-íö.	ö$fO\x000bÍ#\x000b\x0001ºR\x0008¾\x000eº8Âí#\x001c\x0016Zsy³Çaº9pñ:\x0004P½Ì¾`ö#\x0016\x001aê$\x001d°¹\x0013³fUÓàº]G\x0011uØ\x0011QG%Ô|8\x0016%\x001d,nÐYh³Ð\x000e9\x000b­£4;\x0006JWy\x000eí|¯×pÅ¡â\x001c*8´:\x0001ËÝ3\x0013Í\x0011´S¦\x0010ÍÂ?°hÖåç»ïßïN~º\x0005u¸J¹À£=$\x0011MµepãòËX)>¿|wöéÓÙÉO»ëëÅ\x0013æÕs^ÝÏ\x000b'	éB*Ø\x001bi
\x0017: À\x0002+zã+x÷/éÈË/é\x001dÀ<\x001b6©¦î8/"ËK+S±¹5´¾ õý´xP§å\x0005\x0017GOF^Zö\x0011ª"úÒÄ\x001bÊv'üÃfævùõ§;\x0000KÖæ\x001ayCÄ+_\x001aô\x0003\x0017=Mµ)F²\x001c¶«*¿½]~xsu\x0006X6· \x000f¶oÈ
P]ÀÂZS3{JÈÀõ_3±\x0013Û~b-´*\x0013G"vtïÃîõú\x0005»ØÏý\x0000bÏÓÏØP+-N¢ó¸\x001eP4\x0013Ç9q\x001c@\x000c®,f`CÀÊJ\x0006^8èZeiw\x0003\x000cÏ\x001b·iF¶ï{n)ùÙ\x000c\Ø\x001c`xr´=O&hXð\x001a»J\x0017Î*äÂðä\x0008ËSá\\x0005JÅ$à\x0010x­ë\x0004.ìN0<\x0000NÃ\x0014L0jOÌÎ¸>×j\x0005qawráqã§ÁD\ }¬(p^tndUld5b#\x0003rª}3>?¥\x0019!\x0003Ícr¾\x0012\x00015!{#ÊC\x001aþÀôÇÛ/·\x000f}^[Ì\x001caGé>já£\x0000\x0008\x0013L¬ÞúJïÑÇÝûÝÅ?ß,Æ\x0012©æª\x000fS[Ú¸)³~¡òQà¬9kåÔsNÝÇ=ÿ6qâ?j·£z=o+»µ\x0015ÓÌ1M\x001f¦	ô7ýê1Ëãç½ÒqÛÊiç¶ÓË¼;­¡·\x0003ç£àå"öVN7çt?;I1\x0002§\x0011¨mÖT\x0003a=+å=­~Îéû8\x0003M¦\x0007ÌÀÔ\x0008ywÚía\x0019:ÓÒ¢Åc§MxrúÀY9§Z9ã3öp¢l!õT\x0001§cÉû <QÐ/=}#§,¼§ìt\x0010PY\x00174Jç\x0005ÝÌY¸%Ùé"'í&¿Ä:^|U/¾\x0015´°wÙeððËýy4#@uvL5IVÐÂd))ªð1ÿòdñ:¨\x0001Ifý\x001c
D~é;â\x001d]c'R\x001eeè	\x0002÷èËKák¨!2b?ì#¦ç/'o¿?¯ÍÃ.¤yCà³ô¶æÒ$âÇÝÍû7W7n\x0016Ã;ÕsXÝ
ës\x0015JûPVäô®I\x0012­ µsZÛK\x001bD¤\x0013_ü¶ê²Ò¶¢¾¸ÖÏi}7­´tÉÆÛ\x001au&;\x001dhVÒ¦2ìm\x0005mÓÆ~ÚÈ%ñè\x0016(Ö\x0005cqxý&ÚÃbé0+pß>þ}­ãÂÚ>êI÷AF\x001c\x0018ågTQ©û`ß^þË²?8,\x000e³¢éÍ¨N¦Ñ\x0016ø<¦8EÏ\x0015\x000c>VR \x0010°\x0015 1ôÂ>¢«©
Xìóã~\x0013\eôîk¬\x001eGÇÌï{øÙ¸wß~½ýüø¼ò\x001a\x001d!¢"m/\x0008QQ=ÖNR'tÄ:\x001bbUóãÙõÛÝ»Ë×hÍÖ M\x001d\x0008p`9ò[@+ùÒ_kåXAëæ´®VÚ¤qÖÖ\x0012­T¼¶µÂÙvX?õ½°SF`¢\x000e\x0014e\x0004k*
+hÃ6t/-v	ï7Bj3\x0012Üh#Ôê{Ûiã6öÒâÛAÌK«iiáßñÒölÚ\ñ=±ÎF³lÝ\x0008ÊóC
\x001cø-*	Õµ7ýv\YàÊîµõ4õ¦ÅMMIF\x0018÷m]õ¸
WÉÂ%(Ùï\x0014pðUr¸Ø}èÉ)DË;WÖê\x0007_ç56\x001618þaþ´øññáûê ÖägEdMqq,jjª;>^^|Zc2¨ª^P®7ØvJ¢\x0016è\x001a´¦ÒÜJªç¤ºÔQ¡ñb\x001dPÓ£õ\x000b\x0015ÑM¤fNjzI¹Î\x0015H\x0015\x00132Þ°aá`Í¤vNj;I1/H¿¾²ôÐ	¤>Ç0;m3©º^Rn=\x0006RXSúõC\x0008|ìØ§~Nê{I
¾qO¤zò\x0002Tò>
\x000bÏnM¤aN\x001a:IÆ\x0010;¼¦QÆ\x001cÁvüúqN\x001a{I\x0005\x0017=`7\x0007i\x0019À ±2k´\x0015t\x001f\x0005L~_ôÆlQÆ°<\x0014vM1jmèI+jyDõQÎR*Ã`Ó\x0017M=2à¨¼Y5£\x0016®_öú~oøíÝÛÀÍòpÕâÛ\x0014\x001d¨G½.5Ð>u3\x00186¿\x0006/\x0014º4Q\x0016>Jö:©¨NÏoÀ8#ÿôJo8¡¬
å©\x000fÈùÁ§û¯÷ßïÿXuõ1P\x001c¦¬9	g='²EE¼óãÕùóOç?/f\x0004ÔÌIM\x001fi0ùÍc/}²|§r~XÖ[IíÔvâ¼fIiI÷-²¢¥Ý\x000cêç ¾\x0013\x0014ÎOz\x0006ö.Ïdu2ÿø²¢ãÑL\x001aæ¤¡4\x0018¼JO¤8é&­)Nå%RU¹K5Æ9iì$Å±,H5¿\x000c9\x001dL&­<a5îÏR$å³t3jäöië1ÃF\x001a©	P+ÂÍ¨²@¨pì§Á\x0002ÕQ¢ÝcÐvTU ª>Ô3-¡Z<\x0005¦w,%y\x0003Tæ\x001c7\x0016\x000eUvzÔ¨IÿÊN%¤ôà¦\x0003¯©®´½JêHº>N¿Ñ>7ñ|¿ú0Åîí¨r\x0015\x0008\x000f\x0011ç]\x001aëó¸>Þ/\x001f¥Léæ®\x0012_©ôÇ9Ææ%Õ/úÅ\x000cp\x000b§sú.Î\x0000S\x0012´\x00113«äô\x001d\x0015ßÂ¥¥&¨ÑÈ\x0019æáÿ§¿úÞ"å</¹e9¤Fr\x001b%ÏrAÒÁä©'ùqzQÖùá\x001f8cvuûËí÷ïÏ+)V,\x001ah&Q\x001aXC\x001f
®RXqµ{³ûôi1¯ÇzN©û(#eLÒf!K#2¥\x00196RÚ9¥í¢4å6-¾§Ñ\x001fKz\x0007@Y¹Ö7Rú9¥ï¢ÈS&\x0019"Øù\x0017w\x0014¨à+Qh#eS\x001eJk\x0015ÊÇM\x001a¨xÒ£egTµÏ¾roåõ>LEÿ	3\x0007Ê"8Í\x0015EFLU`ª.L\x0014Y\x0019yÎôf\x000e\x0015iÐFÌÂÊeOÃ|\x0008S\x001a\x000eæ\x0004\x000b\x0015¨\x0010+ùÛFLS`.L¯è@\x0007L\x001e\x0005)ag\x0014*eÜ± ]v\x001eb¾Ã»<«²ö]ðáe\x0014×©óGu\x001d@(dú'C';71ïÌÊ1ÙHYxvÕåÚñl4ô+É!±<¦6ÄJn¹\x0011³píªË·OJé0\x001dæí'LÍz«¢Òý\x001a¥5\x0007!Ír\x0010\x0019]Ýþq¿VcÎ(\x000e\x0000.¢\x0014Vò,¼ú(Õ«ÝÏçK2s\x0019SÍ1U\x001f¦né\x0013&8&ª9\x0015\x0001ÃòvN3ç4,©\x000c\x0011ç\x0001%NºWÚ\x0018ëe\x0010M~Îé»8!æ%u\x0014lÓÉJßL\x001dön¨\x000e{mâ\x000csÎÐ¿=i9ç»Óæ}3eSÆÎÕ\x0014§4)Uú\x001c\x0011ü£Ûz5I\x000bæ,@B[\x0017«)H0	Sò­R\x0018Ë¿z­Ï·³ôI}NIC$ÇS\!DÒ4éÒÑto¸lÔúÉ\x001aA\x000b¯$;Ýdõ:ðpË sß{¥úÀô&ÎÂ+ÉN·\x0004ñ0=ÆÃ¯Í\x001aÆBQ\x0012\x0011¼|½L¯	Ô\x0015 ®\x0013TPp\x000c \x0012ï\x0013¨lð¾R\x0007Ý
Zø%ÙçtdÁ4#°	VTÒ´7[*o\x0004UÍ«>×ÁS³\x001bZ²%7:\x0004ºýDRå	ßgK:Õ&PÅêF1\x001avNn»³W1©>cÒØøL\x0012¶CóÙ½Sõ³\x0011´0&ÕgLÚY\x001e*u-´ Þò±äj
h-©N[BY[2úTýn9\x0004é\x000eFtaKºÓæ ¥\x0000Oå~ý\x0006­Ë >àL;ºyÜ=\x0000ìÿü×ï\x001eþãqí\x0005\x0004Bb¢ÕÚG~µ
JW\éÕÙ\x0005\x0010ì.~Z.\x0015d`=\x0007ÖCcj|Ô\x001aSvT7\x0010¨\x0014ÃêÚÌ5Àv\x000el\x0007\x0001GZáhH.Þ\x0006j*°:ÈÊ}y\x0005°\x0003û\x0011ÀWìu§ù\x001a{K\x0000¸\x0012\x0000®\x0001sà8\x00088Õh#sK¹
lq:ú¾v\x0005±,­nÙa­¾"äHJ/Lf\x0007M%%µ\x0002¹°;9Äð\x0002©má\x0014gj4@bÚ\x0016FVÞí×\x0010Ø\x000c!¶$²«Ö<ÍÆr\x00194 WÄiÖ \x0017¾Bq\x0016!]\x0012Øc\x0005\x0001cyT\x000f°+Ý\x0008`Ëî8Xn;p\x0007V[Y\x000fqáÝä\x0010÷æ-DOkl²\x0012
4«\x000e\x0016¹\x0019\\x001c
ä0d#\x001bOÈò×6²Ð¼QÔÁ\x001aâÂ#Ë!.Ù\x001b\x0012\x0003ÖøÈæ	\x001fS­ÑA¹+÷·\x001fDæÛOç"K*LÒ&æú§\x0012±é;§Uq¨1± Ñ\x0002o¤ýa=ÕÑ\x0001rE´`
²*ÕEæ!\x001aç1R\x0013E®¨}Q¹\x0011¯A.Î=5äÜs$Sµñ,#\x0007«Lñ±Ú5ÄÅ!¢\x001c"În1Êýæ»*,lï¾E.ü\x001aã/D^ä(ù!q\x0012¯!ä.b]¸\x000b=Æ](Êáx\x0012\x00169°9\x0013a|å>º\x0006¹ð\x0017z¿`!9óÁï\x000epFsxQÓäX\^öÆÜö¦ýVÙR\x001a\x0005Î\x0011ÁG_]µ.¬O	ál\x001a\x001a¥­ú°(£}Ú
]ÄE\x000c§ÄpV\x0018«\x0008)\x001c|?µ7\x0011]DpzL\x0004ç©\x001b\x00075$hÒ\x0000^E¸/\x001cÒE\x0000§Ç\x0004p^ü0CA9!Xä¨\x0019¹Vh´\x0002¹ðÈzG\x000e8¶2!;~\x0006²äÍ\x0011¹k\x001fÂ%1.9¢.ÆÄ<bÕab7!÷Ep¦ðÈfG§´-°
£!É;YVJ#×\x0010\x0017\x0001\x0019\x0012ÀÅI\x0014-!\¾/,ïdYy$Z\!fLâBþ\x0008Ä\x0018fÐõw²¬\x0014Ç¯A.2\x0017fHæ"*\x0012¥ÒXWGÁãÆð·¾0Ù\x0014Ç\x0019rì\x0005Í\x0011Ü\x0018!ò9ûÎ=S{fÈ¹\x0017Y;CcY û\x000bÉ\x0003(­Ò\\x001c$fÈAÂñ2!;ÍGÒ²ºÒ°\x0006¹8HÌì,Ï´\x0007díTi/³Ãèsq¶8Fìc$
pq\x000c\x001cxv³cÕWo\x000c]ÈÅ9b#àéZmáò'Ù_¸Ü÷cÄ8H"Î¥%ãóµâ'g8Á»\-\x000e\x0012;ä Fëè©¢\x00169GDFömåâ\x001c±#Î(&·6\x0011\x0007\x001eUìXÕÒ¢ x\x0017qùX6ä\x0018ûHÙÓ PìcäSÄôÅö¶pÉvKJQ«\x0003Öðå6ã\x0019ÙW!V »Â]¸\x0011î\x0002·!w\x0001\x0007
UÌÁ¾ \x0004u\x00155Èí¹\x0011¶:WIÓ\x0004gDó´èÜi§Ôr\x000frqMuc®©sà8\x0010oë$d¯kÒ+³Ú
9«S9êô£eN^xÞËÞÛ®È\x0017.Î	aiÓ"»üöë\x0014\x0017^v]úTyéScn}û²ÆAå¤¶\x0015-ì5AÏr®)ó¤çÚýê)ô´&g`\x000e#GË®+\x0011nMI
\x0007à\x0000ê(%µËÁ	èù\x0004Ô¡kºhmÐö° Ç\x0016\x00059vûp¿\x0012\x0017<ÅiLÃ\x001de`a4t\x00194\x0014H¥â\x000bøÓùîâü5^5çUý¼\x0018 '\x0019J\x0019}.s<"jéèk¤ÕsZ=æHK! Õ<îSZ#Ð
^;çµý¼èU^]!\x0013¯ !/\Þ\x0005GÑÈëç¼~\x0000/ëä)%\x0005/ 6\x0012MùÔzéá©7Îyã\x0000^GZ\x0004À\x001b¸T/D¢\x0002¼\x00155õ\x0015¼²ô\x000e\x0003Üå\x0016¥åò×\x0010yf®õ(¯\x0001.\x000cN\x000e°8kHL)­Oy\x001do`\x001dÝÃ[\x0018\x001caq:ï\x0008£xNmÝR\x0005N#paqrÉ)ª3
¡¨Æ	óá*jok\x000b#lUUrÞ\x0015\x0000Xó
ûÐµÂª°95Âæ\x0004Å=\x0000ÌÑ\x001a\x0000+>4ÂÒe©\x0011¸°95Àæ°à&Å\x0010pÓ§¹\x0008L¼q©ô¦·°95ÀæLÈ>\x0002bt\x0006Þ\x001cDÄ°ok\x0004.lN
°9ã©Õ]©ÈO¼\x0000Lú ÆÔ&Y­\x0001\x000e\x0005p\x0018âÕ²ÒÊ 	s´Âpntsóò
[Wlw\x0012I1^\x0017v\x001cGP>\x001cr¢Ë©éÂGè\x0001>\x0002°dÚ\x0011Z+J¨ØÀÝ\x001eÆ>ÓEØ®\x0007Äíà#R\x0011¤Â#Ú²S£ÀÇ,\x0015Ñ7âqû\x0008&y|<n\x0008CFà\x0019ÐÝ\x001bÂ\x0014ÀfÈú&\x0019F¥$\x0011y<y\x0007W¦I¬á-|°\x001eá\x00055)(<ï\x0002y y\x0003Û^Ë
àÂ\x0007ë\x0011>Xðü\x0003¼%Q÷'\x0000³\x000fvá®k\x000b\x001f¬\x0007ø`\x001c5ñ\x001ais\x0014ÁåóÆÊ¥ìI#o\x0011§é\x0001qÎwOíXC\x001c{*x\x0007ûúÝ
`S\x0019fÀa$×6*ò)\x0000{\x0002¶ª/°4Å¡a\x0006\x001c\x001aßr\x0015vÚ³O£pcBeË\x001aÞÂ	\x0001NXSa\x001b\x000e\x001a¢\x0006\x0010\x001b| ÀÝÄ¾«)|°\x0019àa\x0007§ç:þÞñ¡L5ªËäLáÍ\x0000'¬¹\x001eAa³ã\x0005¦CÎjÿ\x001aÞÂ\x0007\x0001>X\x001bv\x0011ØwÅ\x001bÂ3oe´ß\x001aÜÂ£\x0011\x001eMpB\x0003kÊåÁAT¤W\x0000ÛÂAØ\x0011\x000e\x0012N\x001eÍ3°ÍÀ}é?[x\x0008;ÂCpçàdq\x000eeoL¶¸.\x0017a\x000b³\x0003,\x000eUÅYK½@\x0000¬ùÌ°}¼ÅÙ\x0001\x0016§ì)­¯ç\x0002G\x001b\d[ªòhÄ-b\x001e;"æáÇ\x0017\x0008\x001c\x0005\x0007Î\x0007Û¥BFÞÂCØ\x0001\x001eBòàBà5§d\x001bØàª
\íÀ®ð\x0010n\x001088\x001d¨ý\x000e\x0007×ò}\x001bØ\x0015\x001eÂõ{\x0008\x00159°"\x0012®æ[\x0013]\x001eX
7ÇÅÛË+aÓ\x001b¾\x001fÆ~XTo b×ê±ÅSíä#~éw\x0012Ê ÁK\x0004*\x0000/a8î©\x0008,7 \x0007!}ñä\x0019¦l6i%Ü};¹züzûp÷í¯Ïw+WäG F7¼ÊGA\x0018Ì¬½PL8»>¹ºü°»8»þçÅAë\x0019ZÏ¡õ\x0010hÙU hG*4°«©¼\x0003 +Ýw+©íÚ\x000e¡v/\x001dA\x0005¬s¨\x001d`¬\x000e5[GíçÔ~\x00085Îä#j1ã\x0008Ü1uMÙm\x001duSÇ!ÔZ¢KNÔ2ï\x0010å\x0015SÇªÎ*jY\x001aã\x0018kT.[£\x0011ü¦/H ÝÄÚ(Ô5Ê1æ¨<ÇÈt$j\x000eå¢®\O\x001b±(o¨øý
õ\x0019AnO>Ü?Ýþ\x0002ÿ°\x0016\x001c"Tð(dV÷\x0015b:0ÍZÍÍùõõÙîæäÃùÕî
üÃkä® wÈcÄ·	]äû¼\x0016Þ­%\x000f\x0005y\x0018Cî¥¡GH w,&$5vÄq9wôè¹4}BÏ¥é½èàIHìDäÑVZÏ«îkw¬Vt8\x001eÊ3ÞaÌÊöyr}ûÇãýÚá\x0004\x0002«n&ç-­Ô\x0019BÉyëZ×é»³ëÝÏçKÃ	2¨êNP¯HO_BG¢,ÕÀµ\x000f\x0015\x0019fP;\x0007µ Ñcñ\x0012bÉ1Õ\x0005YKe\x0015ÚÇJò»ÔÏI}\x001f©Ä¹n>bA©£ø^\x001eu×Ic8Ø¥8]yOz÷ïÀ°Vÿ_SHÏº:*M°`WÜÁ\x0014|å2¬g\x001f?}X>=VÍiU7-Dùi%Û¤·¢¶¢·¾VÏiu7-üøITTGíiÎ¾;Ô¤:ÛYíÕö³\x001a
Fb·ãÄ*i,aªLè usZ×Mk¦:°´²ÆÊ(^ÙÊ»Ò
X?õÝ°8E6­á>%\x001b´ÊKkëî 6ëà& úqù\O3Ì)iö¸Þø\x0015¸¥ÿêw`8ûV×	¬øH\x0017¶²XyPZA[ø/ÙïÀ²_´&\x0017®9Ïz¢R2±¶°2Ùmfz\x001f1FLËs).kgPTÛ«
\x0017¦º}\x0018¾6ShÔ£áçé±\x0003·p\x000bªÛ/`	
yu)LYÂ;øê|ÕfÜXàÆ~\Ý\x0018jáñê²hjðòv\]½Ý¯\x000etÜu«"SÑUWà\x0016¦¦»M
6\x0014,1 %a¶ëDÓÅÖÕÝ[\x0017Å\x0010©ï\x001dç\ñ¤\x0016Ãj$ÁÖT³ÛqC\x001bºq÷*gQF¹[Þë:ÑtahºÛÐ¦I	.o\x0005O5ÞC­,©\x001d×\x0014Gé>Ò\x000cÜ\x001a­É±\x0018i ð4^/¶O?M´¦V²ÈD4à\x0016R¢TÜR\x0019î»¸Åfº4ã-Ö2³\x0017£vJ¼´óÖ­Ô\x0000¶ãÚ"v´Ý±£	Å¶¢T}Æ2Ð²+¾±Eìh»cGô\x000bìÆTÖUÒpÀà+Å2+p½kû÷®ç\x0017#\x001da\x001bk²4\x001eéd£ªdMWà7Ê\x0001{Wc§CÌ\x001dEëX__Ô&\x0016´ã\x0016'°í?e9	\x0012¨þÚ	î²±Ö¹¼\x0002·8mÿ\x0011ì|¾¦yÏj9Rlj¾\x000b·8Ôlÿ¡æ4
¾ÇÎ\x0006Þ»"fÉ}Ui²nÇu#sýÌjÊò\x001b¡òDy\x0011²©-¤o\x001bi\x000b?æúý
ÔÀ5m]\x001adUË`çöx]W\x0004\x000c®?`°Óû£¹\x001b$ª-`C«
 \[\$\÷EÂX\x0011"Ì¿¢©4û®`-N\x0008×B\x0018GÉ|\x0003Ó© Ù+>\x000fàð×©\x0015¸Å	áúO\x0008Ø	\x0006`\x001efÚdmÎXÓ\x0004X[¸\×ïr¥¾à\x00144ë~\x000bo8ÕTqÑN[x\7ä\x001a!i\x0018KzO´"\x000f9ÙæÃ¼(êñ\x000fÙ¿¾{ºýËï«§D\x0011ð=\x0007P\x0001ÏQòÙa¿ú
aME°àúìj÷ñÇÅé!SÏ9u\x0017'*ZJ\x001a\\x0018\x0005ÏW4üü ¢­äÃZ9ÍÓôqâC^ õÔYµô`=+\x0002²­vÎiû8qøJât!ð¬\x0002ÃÅêª:Í¬ÓÍ9]çï\x001eÓ\x0014\x0008XNîk=ðö¬e;Z1ý\x001cÓw.§¢JNXN.ÎrÆS£<,g¥\x0008®sÿÊüÊ°y=Õ)#ôGúÙ#sVª±Z1\x000b¯$ûÜ\x0012\x001a§R&¬Ga©yÃzþÀYIÊµ\x0016æ.;íÝq&\x0019@-ýê*ïN³}9\x000bcÖnÝ©¥é´pñæEåa{VDå[A\x000bkæî$\x001fG\x000e5IS<
7\x0018\x001eP[¹ª´r\x0016æ.;í\x001d\x001bD\x0013&Ü\x0000éÔ4:òi¤+qt+g(8Cç\x000fÏ9·éØ\x0014´C-)Ðà±¹yªÂ/©N¿d\x0014.x&6Fö\x001fGª\x000c:\x001d\x00136¥cÂg\x000eZP­²\x00196·r\x0016~Iuú%e(¾,$÷Ü[üö¸N\x0015\x0016¯:-^ìÀh2aÍ!U\x001bèÓÊYXê´$¶¤1ä^SÇ²F}ÉûÍ.T\x0017¤;-IcBñ\x0010OöÚ¼æ\x0013)÷\x000eðôKÉGz½\x0015ü\x001e`Líj"\x0006¯²Êò7/å,TþíîäÝã3v9|_I«,DÉé9ÀCpÂ½ExSÑ\x0002Ú\x001fàfwy\x000e^aÅyX©!F@CGyàI­\x001b¢4å{¼ª$%ÖA\x0002Ú\x000cÆÎ8M\x0012Öè\x0014Ü©\x0007\x0006õM«¶\x0002Ú\x0015Ðn\x0000ô4{#m\x0002>)%ìXù6úµo\x0005³/ý\x0000f£!H0\x0014ß7è^KÖ²Ô¶ê{W@\x0002:\x000cYhÏòÞÁ¹üè"¿"ÊÈ:èX@Ç\x0011+íx¡÷"ëê9~0ðZW\x0017íÌYjbf\x0015ª>3Äó#UÛ{¥°ª6=\x001bðÜ:\x0008Ó:\x001dÒ\x0005´\x001e±;¤¥	ØX>MÝ
\x000eþÌ\x001a¸¦wK«âdQ#\x0016ã÷¾C(7Ml¶¢©¶\x000eºp\x001ejó0)X Ìµ\x0007ø° +Òë\x000b3T#ÌÐ¢\x0006|²C\x0014K¦Ñ\x0000Òä²`UÑ_\x0005­\x000b;ÔCì0\x0018ÖûÆ)_Ês\x001dªGÈ+ \x000b;Ô#ìÐ¸W\x001aÅ{é5$æã°\x001e,¯`.ÌP\x000f1Cpx$\x0005·ÑTá\x000eÌühîk\x000cÐÆ
\x0004(Q7Ç\x001fwO÷\x000f+;\x001dGÙ¤)JQÙÜ\x000ceXÅNDY;S~>»:¿Xlt`N=çÔ}fÊ'NOs\x0017pÐdÎJ1`+§sÎõÔØº<qB\ÄËÉº²ÒÍ×Jiç¶R+RÖÕ¬1#%MìÕ¬tâ´rº9§ëüÕ
#ÁjFîD	"^NS;ÒÚ8ýÓ÷qBd^À\x001aÁi\x0018\x001d,gE
²\x00153Ì1CçÏÎ3Ý%¶P?r.å¬º¦6Î8ç}Ç'Âr\x001aJ7ZÅV7[úìnStþè\x0004@a5UîÆ\x0014!Ûz¥~§\x0015´tñ>^HÊ9H¬ïTÔcLoè6\x001bÑìµ\x00069UçÏîéÆ.±²s¯§\x0017tóî>^Ì'`Z¤pwÒ)e¥¢³³p²Ó{
\x0019ð\x0004ê(É\x000c¿»gs\x0015©«VÐÂ-ÉN¿$\x0004=/Hì¯r@i\x001a\x0006ªíAÈ<Ý8\x001d¿ô¹Ð©;Ù¤ºy89Y\x001a\ÄJõñ«¨þ 1\x0014ÅÈf5e÷_!\x000e]Iª\x00148ûI|ÂD|¥×)Ã\x0011xx§Rr¡æü\x0003Ä ¯²9«éeÅ¾/;±â\"*Òn
þ^¯kcusV×Ëj©G	Yí)¡JcÃÿv½¨	uö\x0018\x0006¨Jô²)!>í\x0001\x001c\x000e\x001f\x0008VÒ;=:°
°p¯)\x000bà\x000f¹5øùäúûíçµ\x001d×\x001e.Ò©ó\x000bnuË5­!\x0017omm·Þ\Ú½{SÏ9u'§ÃÌÊÄ)];L\x0005dÞºÊYÚiæ¦\x000f3Dª'Å	Süc\x001dÕÅÃrV6i#¦cÚ.Ì0éEN*ò0=ì]'J_©'hÅtsL×i\x0019!§ä\x001c¦
û_½V×Èéç¾\x0013vd$NÍ\x0012Z8ëH\x0012ge.H+fc>LeèÅÎ¢À\x0010y{'H]\x0001~öJ½K+gsÆ>Ní©XÐâ#£ NEºÞÖ¤c\x001b9÷7\x0011äÌ=ß\x001bAáúF\x0005[¬(¡\x001e#§©\x001eÛc«úfPYÊ>PËº\x001aØ\x000fÉ=\x0004³M°¢µ&ÉFÐÂËË>7\x001f\x001c\x000fÁÃ6Sº8g) ñNTäjZA\x000b\x0007*;=¨\x0014ãc\x0013ú)ÍsT\x0001g¬VÎÂ3ÉN×\x00144\x0004£°*¿Æ:Öåö®6ð®\x0015´°yÙgôQp\x0013\x0011P f\x0011zIPïÔö\x0013^\x0015¶¤úl	û`=ýòÑp\x0007¯çi\x0000ZS'i\x0004-#»¾Ð.BÀ\x001c»B¾óO%Wyµlå,l^õÙü\x001bñÄ©IcÐÁYÄ¿<ì×Í El§ú;pôff±î;\x001f\x000c/¨©Ì,o\x0005-êsNøË\x0007ZQ©ø¡Ìó#;VÒ·­ E|§ú\x0002<ì¿sÄiÉ²§7Û$UxPÕçA£TáfQ9Ì=
v Vmöôª\x0008îT_t\x0017\x0003+\x000bLTÚ\x0018$¥Ç\x0000´¦CÔ\x0008ZxzÕééÃô¢8jÒ­\x0007N9ãf¿¤èNwEw
>\x001bûÀÒF\x0005\x001at>lå¼³8t×4q*ZÎÈ¥·\x0010àózº\x0000çkÞ\x001fd\x001aàc9Ëüü»§û»ç§Õ ÒÓX\x001e\x0014\x000bà\x000554\x0011\x0002BÊ\x000f}óñìêüìæêUT3G5Ý¨áÔgOO\x001dÍ\x0010E³\x0003ÕIèí¨nêzQQÙ(ÒÝ[Ë¬¡r*5³Êb\x0007Èþ-Àcb\x001c\ÅøÆ\x0014r\x001eÇkQ©,x
\x0016\x0013kEÂiÊ´íûW?=>?­l\x0002T:ZÒ\x0010v\x0006U	'R¯©!ºLË§Ë«¥þ¿Liç¶Ò\x0007z\x0000Å"vºØy-©Ê\x000b¼jU\x000b»3Ì9C''ÏcÇ¦\x0000*û\x001f;Fæ\x000cÕDs\x000bg¾)O3]´M \x0010¦\x0017z\x0008@$=2yåHÕ3 jÚfPUª>Píª\x0013¨I\x001bß+ï#Îj¹	³Ø²sJIã0\x001dê.¤á^iÅ\x001bT×R ®\x0000u ä<Ý$O?¼¼ ¦Ëi\x0004\x0005hì\x0002Uxt)aò~y¼;ÒVÊ
_\x0005ÕâÀä!xÚüÛOO·_\x001f\x001f¾¯~\x000b\x0010°>\x0017úÔ\x0007mQ\x0011»)\x0019Àû~wòéj÷áòâÓò\x0008sç¬ÞÄ=Srì\x0003\x00174\x0018ANàÅL­
n-¸*ÀÕ\x0018p\x0011YÖ¨,W\x001d\x0002÷:À\x001f«[y\x0015¸)ÀÍ \x00157ä,p+ëúÁZ\x0007®+³¬\x0002w\x0005¸\x001b\x0004n±p\x0002wyPI¤r)kª©VnW*8á\x001ff
NßNôÉÇç/÷\x000fk%ð¥\x0013\x001fòøº2\x0005ÆZÍivUÕ¨¼Æÿ7ïÏ/\x0016½²å»:þßÕon\x001f×ú<XK¼Ð:\x001c¡+¦æèóL~ýÇÍ\x0017¨7W»W\x0019õQ÷0FÁãÍd¤C\x0008\õ¡j\x0005÷mvÎh;\x0019i0ªùì0KT¨
m~Îè»\x0018!>LxÒYF¤#ªrën#sÂØE¨ÈÚ\x0001Qr¨`däÝè+oM²´.ß7©x*Á·Lä(WÉ¯µA\x0016&#ûlÆðÜ[é"GFIÞW6ÆÂddÍ°¾70j*ÞDFª\x0005÷ùò~Ý\x0006YØì3\x001a\x001e%­§\x0013\x0018cÆÊi\x001bca5²Ïl\x001cw6_­Òì Måù¹	R\x0015f£úÌÆó&iì)y\x001fexCêJób\x001bca5ªÏj\x0002O\x0019ñcÓæñÖªr¥jc,¬FõYM ¶\x0017`Ô{ËæiªpÙxÒ¨ÂjTÕ¦¸k=\x0005@ÀÈsãª\ùÚ\x0018\x000b«Q=Vã l9@r
Ç3 eeU\x0013¤.¬F÷XCqÄ(íiFäó°hC,£³\x001e£AÄÔp£$N\x001fb£á\x001a|%*iò6ÈÂjtÕ8¡H6\x001e 5\x000emIìZ\x001fr\x001bda5ºÇjÐ<9{,Ã\x0007"åò \x000eª\/Û \x000b³Ñ}fcx8² Wë\x0004©yÔ%*}­Ôª
U5þ|ûåËãJ\x0011\x0005%päi '\x0011½Ïo"õWÐwïß_.©(dR;'µ¤Y)s*{eU³wª¦Ù
êæ ®wIC®ÏÀçezU\x000e.W¼Ô«ÇÚHýÔwzMy©@^l£Ì$ZV+IÚHÃ4ô
|\x0004K?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=bº\x0011 (\x0001E3`nL¤µ9
fcì`)¡,	e3!D70ÎÏ\x001cÀbÙÐ\x0010dd®ÞfDU"ªfD\x0018Lk\x00137Âßßýv1¢.\x0011u3"\x0017¤<!k6ÑHúÎÅ<Ø^BS\x0012VB\x0005³ylvÐ1CmÅ8}gf\x000e%q3¢-\x0011m3¢³C\x0008WR MrorêùâËâJB×NÈ)	LÁÀ:Tg\x0002'vÀ&ÊCaØèKDÿÛB\x0014ì@jCnCxÞ<GMÂåæ÷ÏáÅÍ}:2^ò\x0007ijr\x0018Ô\x001cUÞ*!UN\x001a\x001dtïåMÔ&ð\x000f¾	oîø\x000f~Nt¢NÅþ¶@¼>HG
{a\x000bédI'Ûè45\x0018ÓáíOá/è}D	Vø)ºèTI§Úè$6äÑð'«©Óälà"\x0002Ð\x0005§K8Ý\x0006çcIl¼\x0016A\x0011ÓÎ	A®ºpAuÁ\x0012Î´ÁÁXv)Ë\x0006Æ\x0003`¿0zî;W<sºèlIgè ±\x0014u1×(P\x0006ç(Ò2ºà\	ç\x001a¯!S^Â \x001dt-JãIøßÕp¾mç \x000fÖä<X
$
KïdQ°ßC7õQ\x0012³6<&²8±Ò¤Ìy@q\x001eø"¼ZQ´i
\x0005Ý$0/å<¡¨
ß/\x0013Ä¼R\x0013¼MO¨ðÕ¨'ÎA\x0015a<}Ù2\x0014ÕWé	Þ¦(0\x0004ÒÂYné'¸$¼eWj·é	Í\x001d½´¹ kóRõ2-&j\x000b íÓ
\x001c"ä ÃÜ\x0010ÊSáÞ¹²ð§\x000b¯Ú=Ñ¶{Â]\x000b«s}&ö7\x000ft/\x0014xU4%\x0019xÑ-Üb	pÊ\x001dÎçÌãps)Þ#:¿ð\x000fA¤\x001cd>9è\x0015þZï[\x001f^·G\x0001þ
ê}j´ÈM$ùHLt^óÛÌ(JFÑÌ(XNïcvÈI¶<3¤.4"Ê\x0012ñpÎÂ\x000cD]tb\x000bÙ!ç6gl\x001a¿|\x001bUÉ¨\x0019¡\x0003§Ê\x001eÈ\õá\x001deoúÝ\x0019uÉx8¶àUF¦¢\x00132L¤âGÃ\x0014cÙ\x0003¦d4ÍºÄÂHÅÜÇ'Ü\x0013òäz¶ü[ÛñpÊ}ä9S7h¼6G\x000bØH\x001bVFW2ºfÆ Sr6±;!Dí\x001a9RÑèKÄÃ\x000f¯#/õ±¶Ãq'Z.?ÙrM\x00125BB°,!\x0006:YcdHælñÅµiÖ2ÁLÊñpÇV
\QAU¢6BVZ·ª\x0019ç<Ë­^-ÏUÎÞ)#m\Z\x0019+5Ã[õ\x000b0Ã\x0010PÂ4M²G¾lÙ\x000cYÉpÞ*Ä\x000f\x0017[P«g;ü:{=ó]Ã!+\x0001É[%$\x0018dq\x000f@BEr§fM#_v	k¬Ä\x000fo?áH\x001a|½ÀTöÜÉÌÛü¹^\x000cÉ\aæ¢(¯fk\x001c®\x0006iNyÖë,ÎG\x0012rç¡Â<HKCCw·_7Û??ßþøüåHóÜØ
rY#rª\x000fv#Ñ»ÝÕfûO7»w7o¦6éÃÔ&]ä@Ì`\x000b\x0017\x0002ßjx0P\x0017\x0013ëtöµ\x0017E\x0006Ml²dMl\x001e9¡a\x0007nBÓ/â9mhªDSmh&w]Ð\x000cl	D#íììË@\x0013.Ùt\x0013\x001b\x0014OâÃ/¼
rfK¶n\x0016/ÂýMl¦d3mlºt²rÙn\x0015Ë®-Ùl\x0003[Ppd¸ý\x0019JÓ\x001d%\x0004qò"\x001f¡	Íh®	Íç\x001eL2\
»}\x00103Ã°ùÍ7}R\x001eÄÆ°môDvRç}3>i¬\x000eµ~Sl²#SkN´\x0007(éÕ)ñ"£	®V\x000bMz)I²W@Ã±¡Dä[\x0006Wé\x0005Þ¢\x0018 üÒÂ\x000fÙ®^iïÄËL&¸Júò\x0016ñ\x001b÷²ÿmpK{N%8É\x0017õMpã-2.¦[apU@¬à$åbZ÷²Tµ	®\x0012$¼Iï\x001a\x0001k!YN0±\x0011Ù¬x6×Â&ªË*.k0)ÅDH§xOMº¬y{Ð\x0006WÛIm÷Å\x0016	.ÏeñdÂYH]^VÝ\x0006Ñv\x001b85ÿhT-\x0014Þ\x0016Äö2µ­º\x000c¢í2\x0008\x001a¤\x0017Ù¨XÎë\x0002nV\x0015Õe\x0010mj\x0015üËÃW\x0015¬8YÝ\x0006Ù¦ºtóàD)ãT¾
Ì_YÝ\x0006Ùv\x001b¬¢~zB\x000f 68Ë¸ErDV÷A¶Ý\x0007¯!õà(	"ØH6Ã-º¬²º\x0010²Í\x0002\x000e/\x0019LÆ\x0015JçCzÓX§í[u\x001ddËuð±$\x001få6ùÄYïª(9\x000bî\x0007fë7ôð\x000bxC¾}¸
x7·_\x001föO?N\x0005\x001büDá\x001bÕå@ª¤8QyÔ>ïÎw\x0001lófwu¾½|÷:(Ä|$pwbV\x0001'¦ËÉáU±f*YRÉÒ¹?`YÚJªs0;ª\x001bJPªa«ð¸;3[³-\x0014¬HÝO¤K"Ý°Mz8JfI]"ÓV\x0017Ñ¨f(SBùPFQ1²ÐbøvÓÇc\x000b l	e\x001bvJàÍ\x0013á	Jn\x000e)çS?/|\x0003\x0013´Ôt¤x~\x000c\x0017ò@.Ø)^Ë¨\x0006!\x0005Ù;¨u\x001d\x0006\x0001HE§ªLäiÆª$\x0002o\x0010	AS\x001bÒÔ*Ú\x0005AJ7\x0005XÕ
ä
WÐr\x001a|*\x0014ÏºFªáíÛþ
Ãò 56ü¢Hý}\x0000º{Ø|z|¾ß\x001f\x0010^¨¡!×\x0012'\x0004§áÎ»\x0017¿\x000f\§çO\x00177gÛ£ ê =\x0016\x0008E+¡ÑÔ`9.ÈnCÂ!ßN-&%¡l$Þâ3Ë¡\x0017\x0004\x001dê |\x0011+ê\x0004T% jÝÂ`Rc»ÌYF¨µöEâX+.ñt3\x001e;á\x0018èw\x000fAäô,£_$\x0018µ\x0002\x0012Ð4\x0003ªÜJé\x0002ÐË¬C_$\x001a·\x0012ºÐµ\x0012B\x001e\x0002ê.+'ÊfÓcñ\x001e\x0016\x0005]ªÊüyKl.L
ÿ`PVQo	¯\x0004
o4ÁÞVp2tû\x00106Ñ$»ÏF<,dàE!Cx¯|øõ?¸¿|®ÁDÍQ§NÜ9é8Qk´ðVù°}s¶;òâ\x0005\x0002¼(\x0010Á\x0004¥²Xj&9%@(2n&U2©ÙL"\x001c­Ìäó[]9CÅ(Ú¹n(]Béù\x001b\x0015\x0004\x001cµaCÆâ*¡ÝP¶²ów
ê\x0013p£\x0006¼2¹vý_ÏL~>\x0013säÌ¯G7P;¡´êâõÕ÷¸gäÖ\x000bú3\x0017Á\x0018«\x0001÷ý¯L~M0'¿ÎØ±!¤
lÔ#\äý\x0012ýbÁÆyk\x0015\x0019üb.\x0019l\x0015íÊ#µ².³õ\x001f0}¸kºe×d\x0010¡$$ÂÕt\x001f³/t3\x001a\x0013-ý,ìñ7û/ãñþñáÛíÃþ¯Sh:»$Àl´"\x001b£V
¬þÂ\{³}\x000b9\x001eï/Î¯wçÛyQ¢Ñ±Ü±Ë
³,5ÔcÙ\x0017ÖF3£,\x0019e3cêã\x001f\x0019ÈÙ£Úà2·\x0002¢*\x0011U3"8½éS\x001b¨îÀbrA»xx
;\x0010u¨[\x0011¡±1}éT
&Q.3¶/«Ø\x0019MÉh·Qæ´umEÎËä*×í½{\x0019mÉh÷\x0011\x001a<¢0\x0014üPt«í¡bë`t%£k¿1:Êiãò;vèuçå\x000b\x0003½\x0019Ñ¾y\x001b¥¡"(
M\x001d·åò²Õo'c!dùÎ\x000b	~i4bÌ ø\x0004S¤ø^zT\x0019k%Ó¬eT´×Ó>f°\x001e$¸/\x001f:ÍáÍJ&öT÷Y»ü\x001aË×Ú\x0015\x001d{!+%Ãµ\x000cTö¢ëBC\x00179§\dÙÆfÈJÍðf=\x0003\x001dð,ú&vÒO¢Ð/Ü\x0017Í\x0010çÍR\x001c@H\x0012^¸Y_\x000bëy?7óU\x0003²(J³Ùû9|t=Ì\x0013R\x000fJ±ßDãæÐQ`²£ M¿=Û??Ý>|4¼ÈfÐ¹@Yç^C\x001d<
ÒÈÛ³íÍåîüúu2Q\x00062\x0018r-©\x0008ÎRÃ/msc\x001fkü\x00120YÉ-³*'n\x0008GÞðwå¼
/©\x0012L5í\x0018\x000e(ÐAæzéð0 ¹	nÙ§Ô%nÚ±<Ð\x000fB\x001avÊ\x0016õ\x0017\x0012Ì´1N\x0012æg\x000br!\x0018
\x000bëÃF#+É\\x0013&\x0006IüyD\x0015¥ÜB¹o?Wá5wv\x001e\x0010¹Ð.¼>)\x0017^íx/df	Z%0xÄiTXêX\x000eOiN\x0001=£^VÝLÞr5µ²ÄÁ©GW \x001f4cÔÆ«+ÀîÏÉÝû|\x0007ÂvÍñE»VÝ\x0001Þt	¼¡gyøßæh\x001eLT@ÁÁÝ\x00124Q]\x0003Ñt
Â\x0001Ã@£\x0008f\x001dË\x001eQÊd-gKvÕj³é\x0016¤¶±+û\x0003¨¦ì\x0012²ê\x0012¦Kð÷%ãU§o\x001ed°Í\x0003â\x0006,Æ¶\x0012GÖ\x0004ÁF]Fú®ãÆLÝ\x0015\x0000~\x0011­´ÜÊv÷õÏÏû¿nÎ\x001f¿=ÝnÞí¬è\x0004\x0018êÙÂª$Íèb1AÚÙî®þéfû/óëËðãöã±¢.Sw\x0007¬¢u\x0008ÆC·\x0000ÇÂ½ì
Ý*KTÙ*ò|\x0008è±ÅI«i\x0012NËÍ¡;XUÉª:·Uæ\x00003Ï%Ú\x0002\x000c_·
ª.Qu\x001fjP(\æm¥\x0012cðÇ¬»­¦d5}¬ÁÌ¢¼\x0007!\x0007ó¹è­Vº´úYmÉj»X¹Ë£&$4@¥åsZG
¸Õõ±ÂØ(Ê'ñ¹:Ú(;ê­r\x0006
OI\x0015û\x001d°Ìå¡eÒ\x0013IG:ÙÃ3~
ØJ¼ò>ùú_\x0006ë+Xß\x0003\x000b)æy
D\x0010\x0005èxWP\x000e»y-<²îPÉº¢e/\x0004úÞ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=»|v¹Ü]Ð+Çíÿrhÿo¥4"t\x0014\x0002¤\x0002\x000b®½Óµè¤Ô%¥î¡\x0015B¹Y¾;~éÐ¡~ÞîÄ´%¦íøäÞpª@\x0000d=¬üÒe:Æ7÷%¦ïÀtdI#f zU\x0008y>Þh\x0006t\x001feáñü\x001eLGKE0\x000b\×hd=±·³:A²ã\x0008¡È\x0012MjÄ2 «FA½uít+§\x001e+ÈéRAîÕÃÓc¼éÞ¯¾ìùâ4Al¨ï2üÅ¹VI)WW7×ñ{¹¼Ø§K<Ýg\x0003÷?a\x0017+¢å»¤Q\x0013\x0013çâ\x001d¡6UãÃÃ×¯¿ÿûî®cÛúå¼t|û0vº~õêÝn\x0001_=vÚT\x001d\x000f3¸\x0004*?¤ojÑ\x001b¦EË×Ô´xË\2(Éà9ÙÌ6Elxd¦\x0008YQÆli\x0011	æJ0×\x0006V4=[\x001a{\x0000¹µ\x0006%àûÀìx÷Ûñ»Ñ¼\x0013@ÅÈ\x0003\x001c­Î38ÅÖ\x0004ø\@(\x0001¡\x001d0^ÖÝÃ4V5h\x001e\x001e\x0016	·¾Èì%4ã%4UÁôEt\x0012;ÙÖ=s8 \x000fÍlÆNø\x0017Ñ9ÌÀ\x0012\x000bZ°L>	Á°ÀM0\x001cQ\x0019ã&/l3±LeZ°\x0004õ
à\x0010N.ßÖëÍô\x0015w\x001f±ÅLê\x0017Ë_oïºXÝÿôtûùáÓ®T±\x0011¼SNjVÝ±Û|jÉ\x001fÎ.£ºX^¾¾9ûîêt?¢.\x0011u3b¶Q.\x0006 \x000b8}¡ n$ìB´%¢mFT\x0002í®¥\x0019T^\x0007Ü\x000f¢Ñ\x0007\x0013úÐ?ÇE,¢cêÿ!cu\dûyù#\x0018«ó"Õù( ~Êx\x00196úâvñ\x0006ÕZî\x0017¿ÿïÅxÅØy¹Pü>\x0005ñ®FF'Hû§êäÕÅÙâ
Jµ\.ÈúþÅ§ÕçÕ×o[éd(éð±«\x0005\x000f':õÜ5Öú*^ê|é\x0006Þ\x000f<®'±²\x000eúåáëjg½\x0010ø\x0013js;©ã6Ï~	r2r7o®Þ-wºqµfÐ^4¯Nôn\x00112ádCÈlIfÈ°DÈåEKÅº÷\x0003^4=ég£ù\x0012Í7¡a³\x0019iîïÆg[&NãÎ%+M²¬
æ 
õhÍÓ)Å75þ jBm¼­:\x0005²í\x0018XÃ/ñNñs(¶ÿf¶ÃÐªS ÛUav:[ÐozJö \x0001­:\x0006²ñ\x001cX~©uñ/=­\x001a\x000f5
rK$º-ÓËAºVß><~úy·^äf\x001f%òdóßfú¶s³x{u}úýÎØx$ôã"¾ÓÕ·W»£xmùÎ3\x0008£qÉT®N\x0011jë}ìtùþûåõîÎãá\x0000Òïs Áåæß\x0008©³ÒwfÜz«Ï¨KFÝ±\x0012k¹\x0012£åÉ80­åó!m	i;\x0016\x0012°+A:Ö¾ó!3êC>ö¸ãP¤C~,úý·åÇÇÛ§_\x001fîv\x0016ç¢\x0017=\x0017\x0005ÔÔ"g¤¬z¨_\,/¯Ïn>\ïªÍ\x0015ãË¥ò9k.a\x0004ÑôÜ\x0016W1¨G\x0003hò¤+3'hÆÇÚøºä\x000cÕjVß¾íçâxJÃQzIÃQÕk~[!ÊÔ,ß¿ß)\x00139>-Æ×%g3øB\x000c¤D¶Ñb\x0007\x000f\x000c\x0015c`kÝ\x0003hK@ÛºÑTKñøFN\x0003q$}á Ä¶F½F\x0008Q\x0002\x000e¿odtµû\x0008EÃp\x0004µ[\x0007\x0005jKÙ^FÜvßX#þðã\x0006äm^daC¯\x001dS\x0002YHY\x0017\x001btmÅª¸pØuqáõ\x0014ã´¤\x0018ÒË/_~ÿwRñýiµS9ßàô¿áêkçÁu!828RÖJ}Ëøgð}½Ü-oGñ´H5-lÑ^[\x0013$uD¼¯\x0013¨kæÃÁøÝ\x001cÊwód¯Ï~úr÷ug\x0000F÷JÝ
Tõ\x0015¸3\x0018\x0007dn>÷¡©¿?·ë£*7ú¨16/rÍ§\x000fOØ\x0011¸Û\x001b<ªN8M]2Ø@Ap0}µ<½ºÁfÀÝz+n´t8\x0007¯ÎBNó;Ê	fZ'©
J6h]9G1ðÉñD'9÷¬'\x0006I´Ñ¹Î=3ãûÑuÁ|´t\x0017«ûÏ»Î\x0000A³\x0006ÐüÆ/~ùB²Ý³],/¿Û9\x0012{TD-eUD}äyØ¼riþjvfü\x0017c*(©`>\x0008\x000e\x0012UnÝÕ.°¨µÞl»±>
ÞK\x0006~~y\x0019ð\x0002ûâÍí·ÕÝãÝíâûÕÓ.§eð\x0014¤ü<\x0004#¨ÄHÍY3:_ðæìýòüúülñýò¦tÿÛÐlf\x001bÐPT$Ã\x001b¬ ÖøC­\x0008M×w6©g¼Ä#\x0010?æl]\x0003Þa\x0000Îquyd¬_\x001f«æëi(ýÃgóW\x000f\x000fÃe"~=üuºzüøp?$-\x0014$\x0012H~|xü(JÆ\x000b\
ßQ\x0006ú
,Mv\x0002\x001bd1:àÕÕõû\x0017§ËëWËm[ªäÀë\x0007þÃ\x0011OÃ	PE\x000e©lJ\x0000DG\x000b(·;pÈõ´¶y\x001c?ÿÝHñ@1.E¶\x0017Ãýô·Ç/·»W%\x0006\x0013
\x0003oa­KUÚ\x0002R¸\x0018a\x000cnî
æb¸þùúêbëYÓ?ÈÛÕúçá\x0003EÛ¿.n\x0017¯£!ÿ´\x0003EÅ+gR\x0015ñ\x001aÚ\x0014pK\x000fæ\x00035ëÌ\x0008±,^G#~ºÃýË§¿?"\x0007j4á/\·_\x001ev x'}añ[\x0001}\x001f¢\x0018dÞÆ+òöâjûj\x0014\x0014ñÄ_s(\x0014Ð$Da\x0002\x0006£rÀ0\x0005n\x0013_¼¾´r`b\x0004ÍZ Ó+PäP4ªT`K"mWru½\x001cñÀA¹\x001eÑyÊôQH)\x0011\x00030è\x001d>K1.¼\x0015#ÚÈ\x0017ZÍ]:ãr\x0008\x0013rHZ
%M7F\Gü5\x000b\x0003µÖ\x0007#b±X\x0007gà&Eá#\x0014ÓxçqÜßþôÛýp!±ú\x000büu±Z¼}\}¾ý2ÇØb\x0004ºÐÁ\x0019|RB \x0013\x0006èÀkåâíõò»³øû\x0019$\x001cÃ_sI°IM&\x0018¼S&Aô}që\x001expñ×l\x0018ë	,ÀÍ+óK\x0013MÐ¦F>üMüóçÁãÄ\x000f¿>Ü­¾ Ê®Ý"$}]âa'	E\x000e\x001ba-â¼\x0001åÃùò\x00029vXx\x0002)]Î<hNÈß\x0004áÒÔ·è%,ù\x001b'\x00034¢|üôíÑþFqðÁÆ/ð?ºúi×÷Af`\x0010spÒ¢(íiQñ	Zào¯·\x0002%~[3\x001bÅa§X«\x0002\x00025¤B\x0004Å\x000e ÿ¬I"ÖÃ]%àT÷@Ñ$ß\x0007~\x001c\x000c´ÄÃçfÄK\x0013-I\x0013¤XM[\x0002	jlf\x001bH0ß"Ål\x0014!*[dAÑ+>ã¯#ÂFTÒ[vþ
*Õò!
Udàáqê(,ÑH5ÿüÐ|DdÑè\x0013Óù¡ã£¥8ä\x000bÅÿ\x001b\x0012æ£(\x000cç\x0007\x0014\x0013Ò+.¢SÆ\x001aÌ\x00032ÚFü5ÅÚ$ÄGÈ¥æóÈ\x0002Æó\x00112ãp©%d9÷4ø_;±´sÂÒEÑ²ÑìxåÜó,&\x001dfauÈÞ0Fu´s£\x0007°Ä%~6\x000b¾É¥S¤½G'0¸Ã`\x001d³È\x0003Ì\x001cV	Q¥Ð¬OäR	S:Ñt É;7\x001c¢¢Ssí\Ü¹¢'kbHié\x0013\x0001]8pªÝ\x0001§\x0008/M0çFCÇÆÅËÔ29\x0018:^\x0017µ\x0011í7°`otM*ÄH®E\x0006öDl\x0016\x000c\x0001õü8!Þéó&\x0004ÅqìL1G­\x0003%þ³zþy\x000e\x000eg2\x000f«¢ \§ù<;8ÀÌáÝEÏ?CÞ¥FsBä¬¤`\x0001ëyúYÌ\x0010ß¶l\ç³ùÏ,>GP\x0007rXýk\x001a<¦ªÅ»
tó'²ö#èÍÜ+\x0005Îý£À\x0012\x0013§{CëF§èÝé}Ó´sMB±R¦¡B¸ss°`úÍ\\x0017ç\x0006Î5¡Î¸K\x000e n\x0018\x000etlö£÷Oß?©í\x000c¥_~Û)uiö:\x001en¾rX¢ÀIAp£]L=g¨úòç-¯\x0015\x0005*±Ô³Á²%5ÜhùÈë±r4cú©|Iå\x001b\x0016K$ +?êÉr`ád?¬wVãÖ\x001a´¸p±Dê\x0007Åoèy¿ûQÀÓÄeªohæÄÈeN\x001cayNrª`?¢5\x0007`
+´|E\x0004Ó%ËÑmÂ;Ç·¬î¯\x000bb\x0018k°Z³7½\x000b9X´"Ã\x0005§c{÷t­_ÿ`ÈÛ¯Ëîê"w\x001f­)´iÄû\x0010¶åh¶Â[\x0017Þ­K\x0011¶Z{ÖLóú½\x0014(lþiü;o£Ùÿ¨ßÝþº\x001aZ\x0004¶`\x001eÌ%,Ä0Æ¥\x0007(ó6`Æ\x0015Ýð§ËwïÏ¢\x000bx´ß}X\x000c\x001b¬©fGùÌ7õøïü~õËíêi\x0018BzöõÓêñ§§Û»/»g¼7\x001cÇKN*ea@PRÎãÍøýòÍÙòfñÝâìÝéòúõÍÙùÅ~ÎPq\x001eN«N(3\x001e£@V;Ætö`L#KL¬TjÆ\x001c\x001eSè]%åD3bjâV\x001dÀi7xXsZñ"þîÅ\x001e¾ý\x0016÷×ÅÙ×]\x001bSaoJx\x0018T\x000f\x001d\x0005ÑfXJjSÈ7
xºzÿçx¼ßE¼]Û1
\x0006õÑÁI¸ð{?L\x0003,cÜ\x0017£ô.fÐ\x000c%0ëF/\x0003\x0018¾rï!KC{Ëd¨ÃÏd«\x0008ñð´wÕltoq7TJsõUD\x001a7ñ<´¿½ºÙ·r¨3Y\x0018í¬h~ëeÂºzºÝÍh\x0000èaÑ¢t\x0008- 4£(±ùâ\x0011¯n*È\x000cç\x0007\x0008k+\x0013/<x\x0003|û¸ú¶¸|xúõv×a\x0010\x000eç¦¦°@[?\x0014¢DS\x0010øf\x000bª>
o¯ï\x0017W7\x001fÎv\x001d4)FéÌe|K\x0017÷\x001fÿ÷/ÆSÈx\x001cÄb¡d{ØiÎú\x0008¤âååw×»\x0007a
Ë´`96\x001chê(Æ°¼XðÃùäÿÊÅN|Wøúô\x0005N¯\x001e\x0006\x001ff\\x0002\x0002\x0002»-þ{"nÊ¦m\x001fÝÖi\x0019x¡z²T8-#Å}\x0014A0\x001exwsEN¯®¶öºU`ø,Ù\x0008¦Ñté\x0004ªÎÈå÷¸ÜZ\x0015»+n)Ý¼`éÅ\x0007±|r¥¸^Â\x0010\x0017ûÖkõøéöo; ÒûS\x001b\x0014?Í)\x0014¡HE¯à¥¼ZfÝ~ÜBõ«ÃÑ'<ýyõËß8#aÜÝxài\x0012¢21IOÞñÊgÒ¤F©SSx§Ño¾Mq\x001d)äný¦\x0005èú>sÐôº÷ß\x00004:\x0003ÿ|Aù\x0016~¼ã\x0000 ¹ý\x0015Þ¾­\x0006iûÛÝ|ÒA\x0012TÖKHÅìà¡\x0004U/\x001a/x\x0017z¿\x001cÄí·ÛåÕOáçß\x001e\x000b»ünöi\x0006tðR\x0006©\x0012\x001bmÍ§yÃö'y\x0006P:Ì³´\x000eiü ÞiB;¢1ViêttkbÃIÌ\x0001úû?~Ô\x001fÿ¹8´Xñ%úÒ=ßÌb3ï°>Ú{®ÖÑÚù4@ªøO¹Íoöö":Ó3²sÛIèÍ}&Iüï
l$ÞZ=Ù]\x0004¨",ÆF\x0012\x000cùñ×L\x0018¡\x000esñ¯/ä£ÕO[Fj¿ñfTÑy(\x001eõïÓªÄÛ0F<\x0008\x0003NQL¡@Ïü\x001afÛfÇßV¿Õµ"o¿<ì±>£UÃÆ8-=n\x0017Hppðä\x000c­¶\x001f¢þûí?{¶L\x0016ï:Ô:$íõx¬ãM\x0015F\x001c8
C³/a\âä«¹< N(îCI\x001aK6ã«R®\x0007gòag\x0004\x0003©æ*þ0r`´£/åÝÆÞÏóùï÷ýUfõ1þ7?Gÿ±ú¼ÈÙ\x0013b*À¬°çÈØ\x0014×ó.~\x0019ÿüÝÕååò;>VÃ\x001f7q\x0005nÁÁ¼¹O8Aà|ú`dóâMÿ\x0000¸o &äCEv¤±Ì0©6\x001cï9ê\x0000\x001aª6j 	\x0016{©\x0006\x001a|ÿ\x000e´yØab¦\x001b'\x001cÍç±Ô÷¿Ôì\x0016c\x00196ÌÎ|\x001e.jià\x0006'$\x001e4Ú8ò\x0004>\fÊ ïæ_©T L?àÛçÅ\x0003JÔìùfÞ¢\x0010Öpà\x0015)\x0011Ä-Ùútà­ºH]\¡>ÍÖ`0c©\x0012KÍÇ²\x0000é1báXï´³£I¢P\x0007\x0018º\x0016,(± aµÀ§ö\x0015\-Úßâj\x0001G`ñ\x0010N]çb\x0012Ë4`)H\x0008¸Z4U2bÉ \x0019kÃj·`Ù\x0012Ë¶¬Và\x0000Zæ\x0000D\x0000;7°\x001bÆ²\x0005ËX®eµÜ	o­ô®7\x0018pöpvò>\x0017ÊP¾\x0005ÆJD*4[Ð×Êu­U\x000c·jó ¨ºß®îþ¾Ï¬l"¤Jí6hÖÙ\x000eãèz-ývy¾M
»ÀS%jÃC!qG?^\x001dù\x001a¢\x0014Etn}#]=\x00042ý`\x00106øòðuñúîËÇÛÇo?Ý®îï\x001fö,¡
\x001a®ßÁ¦Ç¾øu­å%MwzqõnñúüâåÙõûÅÎW7ûQuª5ª-Qm\x0017*\x000bÁ$TÅtÞ ÇÖx\x00125­ÛP}êóªR[<¡\x000e;u(+H·5Å5iY\x0005"­Ç¾·qYÃÈ(Ñä"n
~b¸\x0015\x000bÄí\x000c`D\x0012ÂO.Yáôkß7>þÜ\x001f|3\x0012L½f\x0019\x0011¬êµV'1\x001bÌÕT	\x0011 Ý\x001e@º]°\x0005vûF¨&\x001c\x0011/ô..ÐÀÈJ¡\x0007ç¶
v.ðîÕÕ%­~þ«kJ^Ó»ºBq>Oh\x000b=äóHú\x0018WWnØ¯®Õµ%­í¤EY<I)dÃÙG×`Z^±qSè^^_\x0002ûç\x000c\³K?(ôé¹
hg~Cãõ&%¤T\x0012áGzõ1!¥ýTü²»\x0012¨@³%ÚfA×ÎìKµS&S\x000f\x0011:-!\x0019
¦n;óÑÖ28yåð\x0007
1\x00020	ÉOYñúèüøîêÓÝõáéÛ\x0000öf¨MJÂ\x001a_÷ÇÎJ­÷ áØ9ïA¹ñu¯nÞ\x000foú¤$³±Mb£À\x0012\x0017:q=5`ÊØ¤F:Ì\x0006pD\x0015é5íÄÕ%®îÃµ\x001eèìh\x001f\x0014Ó\x000f'\:~0¯Z¸¦Ä5¸ñ>Ì«\x000bÔù(`\¿\x0011«ôâÚ\x0012×vâbB:á¢8j¢Uüz aóBÚ	ëJX×	ã\ÒV\x0008ñ\x0016hR­\x0001×Écm\x0005_âú>\<]ÀvÁó;·Ù,ÀFÖ­6W;ñÆM%ª=ÀZQl¥\x001aüê@\x000cÆóÞU\x0007\x001b2=¾\x0016h±¡\x0015¯¤øôµøpw{\x001aÈ÷\x0014dPV\x0005ç\x0014j~Î\x0010\x001f\x000fì81V©\x0007á»)>->áß³\x001f^ðc\x0011ÄFxç$xF|
Ù³üÔ Ì\x000e%;\x001cÆ\x000eö$½²\x0001noJ²\x0001çdÌfúö@v]²Å\x001d\x001bÙLÍ°1¨pâDq&Ã ·Ý(;ÙMÉn\x000ecÇî\x0000z¾óI^	Ùù¾\x0006Aöì¶d\x001fkV¶±£î°\x000ct÷\x0002uÁü\x0014\x0001GÞð®wÿÍà}	ï\x000fÜ5>\x0015còÙ¥NtÜ6À9\x0014/ÆÆ}7üôuTÂ8Û\x000bÕXè÷Èõôeo_`c\x001c¦a\x001arzjãAõÍÞãÏn¶
8\x0016P"B3"V\x000eQbÒíS×SlÔ;´#ê\x0012Q·#zÎ\x000b\x0017\lõ6£ÄtÚ¼\x0005Ñ¦\x0019QXö\x0002;\x0012¨Ü)dD¡\x000fG´%¢mFT!çÇ9\"æøÔK3õðÖèKDß¾îsb2	DB!øÅRªþE\x0014r\x001c±ÉÍíåþwñÔ,?8Üh\x0004Åî*Putùy¹Ü*ñX@ª\x0012r\x001cÍ4ë7VëÒ8\x0018¹¼\x001bC8\x0002$ã\x0010l?¤Ký:©d1¿"*ËÅMØFq0£.\x0019Ç¡ÖD\x0011hr6Þ¥Nf¼©å¬Òö4m\x0003¤-!ÇqÉ\x000cÈàréT9w\x0008ë-¹a\x001e; }	9vá3¾¶©0B
ï¼Ásê\x0010vÇ\x001c/×5%\x001bj|²Uz7NWGìÒûÇÝWöe<M\x0002\x000bM5\x001cùëü+9vèýåüâûå¶ñG\x0005!ÐN¨ ¿\x001eã\x0004¤dÁãß\x000bMô4G\x000b¤)!M3¤ñpâÙ@:¾	\x0006ÅÈZo<À·3ÚÑ¶3@5¸ñS+N\x001dJ)ù\x0019ÞÙ-)\x0016HWBºö¯\x001dW\x0003³èt¨¤[B.oT\x001b	ívF_2ú\x000eÆÀUbÃü0ÊY ê<7lÄ\x0014ÍÅ;±JïÄÍç&pÿóiä\x0005\x001e\x001bv4e\x001dªbT]_[§$\x001bàl]Úë,Ú|o¡Ô\x0015¥î ´9Gò4\x0004)-\x0017\x0005nt>Ìü(<TvüeüÁÐ\x0004qûø80¾z\ýöõënGãAiÎ`ÉTzi±FÛ\b3ÞïÎ®¯\x0007ÄW×Ë?¿ÛªJ_\x0010ªP=GB(	¡PäÂsìª&@\x0015ø­×n
Âm\x0005\x0015°Èõ\x000e)×ûlq$µ\x000eµÔúÓâúöÇ§½ÕéÑÔ(j¯3'üàçMnÈÙÌñ§\x0017¿ë³W7¯g°AÉ\x0006ml^pX¡·¢;¿w¹súB=\x001fÎp¦
N[\x0014
M\x0017OíUX)Å+'6ò³áÌø«V\x0013Ð¯\x001f°ûkß\x001dUKop\0×øçb_Øoèz}Ý_».Ñrô|ªOåo\x001bi°ÏRÂ\Yb¶T@6\x0000B	\x0008­(uÍUÜ*iu\x000cùvkÌf¨=\x0002Ü²£×Z¤Ó­tX¹.Ñâ\XWMËmé°¹Ë·gý':6 PðîödÀÍWïY«G\x001a\x0012Å-Êò#X·xùð¸¿µBSm\x000bó\x0012g:¥ç·à·ßì± oñòêzçÔ³$v%yv¨ºDÕ]¨N%!\x00005Ì±ôl³¹·H¢Fí1PMjúVuÐ6CT\x0017D\x001a\x0003×+jE­íY\x0006Ôâb`©´Õ0t\Ö\x0018ê\x0008ËÅ®º½¬­
µÚ«²s³*rÚÅK6gõcV³ñ\x0010ßÆ*aì ò?°xûpÿmy7Fñüø\x0012iü>3\x001døD\x0003\x0015ÿýWïwÖ	m\x001fu\x0008¼\x0019æ§ì»Ääv\x001c>C\x0018ÅË\x0008`··\x0008¼\x0019Æ¨ì'\x0010Ú	]ÒÂg#à:;	¹ÁBoI· \x0012Ñ4#Æ;µÐ¹ÁK¾TsÂÌl46 
92ðBÒà8KòñÛÝ1æ¯`-aN\x0011l®\x0005Ù¸W\x0017yÇ\x0005¦ÙÝKC¨P¢B\x001fª¤(É\x0019Q4\x001eBÑ\x0007ñù¨ºDÕ}¨Z³3Â&rJ©\x0008Í-\x0002JlDÁ]¨¦D5ÏsU-lÍcY\x0007ËþáîóêË¾w/æ\x0002w¿»\x0010r_\x0000L\x001e¦Á¦8ÿny±\x001fOxª\x0011O\x000e"®ürèèÊã~è]n³\x0016p\x001eÞÇzÎ\x001ff\x0003Ò¿\x000eÕ\x0010G\x0013t°Jß¼¢ä®ßÜ\x001b!ÛºÂ3¨.Au\x0017(\x0008¾a`Bº ¹Hª\x0018t£& \x0007Ô ¶\x000bT{Nî
¾h8ú\x0005¨éjçô%§ïãt´=u`w\x0004¬\x001da7\x000b¸\x001a@µ\x001cmÑ¸Íâ\x0016ýîá¡jås\x001avõÓÃÓýíî*\x001f¼¦"u\x0017£\x000cÞ£|HªAñ\x001eýîêÍP­ò]~\x0015]mGÉ°ªU}°6M\x0007¬ÞqE\x0003Hê¬Ò\x0014úA¬P²B\x001f«\x000ei\x000eC5n\x001cNÑ Ò\x0008kµ°ºÕÏ{amÉj)«\x001dXa}º¢/A
<\x000bq}=Z°ÚáÚßT£¥±Ü\x0005f´bUrL"ÎÃ\x0011×w¤±òá&u\x0012¶\o]\x0014¶úÝêãêÛ\x001eÓuö­1¨t9Ìo\x0016&ÇQÎÓ\x000cûnùrù~·árzd¸^«à,.ozÜbwÒæBuaYÄI\x0000?ÈMU©¤³¸<{½Cç*£©\x0012Mµ ¡\x0013Pæ\x0006l\x0012v'>_3¥ßèökCÓ%nB_RQ\x0019\x0014IL\x0015\x000cýÙÔ*Ñ&µ2-¹lÓ×t$WA»'å\x0005'YPsszVÌd¾iÅðFNû\x000c5\x001cÓ>¹;
g_\x001f\x0016J´Ð´hÖpÃ¾¡6\x0018'B.RÖ\x001b±E\x0013YNa¥Ã)VMHÎ´hõ\x00065é¸jÀi6µi¿Ïdu4eÛÙDpj\x0018\x0011ÜêäTNª©Í0gÖ¢	Rí-\x0005dêJÛ§=/Ø\x0018wÙ<OE\x00151ø\x000ek\x0001-Mc1V<»9µ\x0019§£x¡Ú¨Ê7,+IB&^	Öí\x001biÈÙXPbAãb\x0019Jä\x001a¡\x0004GÖqµø¿)K¥K*ÝLÅ\x0015í\x0018	´yÏvlG=Ç>*SR6*mÒ\x0000\x0016´a4M\x000fo!ÙmÜvS\x001f~u\x000fòs)ýõöËêÓð*\x0003Îb.§j\x0004ôÓêîËÏ·÷\x0006¤hï!5\x0015k,mBe2<Ñâ§qÌÖA1|y~ñýÙåé·\x0017ËÓá5\x0015ÿ#Ë­ÏY\x0015^µkÆ³$×x:õ®Ä\x00056è°Þà\x0018tI±NÒm)E ghcCzGE¼bÐü!xI*µ\x0019Ï$Bx22¤$pvV8\x0006\x001d+µã¤x·
ñì\x0011øJ¡Éçõ}ÿùÇ»Õ·Ra»\x0018p\x0015ï\x0007\x001eÀN>\x000b*ÅÞZzçI ÂÔÒªkÛñòÐ«xCØ*\x0005PÑ%ËÒN\x0017c\x0000D'Ó40:¤
Ê'Âæêuà%Áf<,p\x0019jË#41âY\x001aD\x001fñ6
_\x0007]²{ítN'©ùHÇ\x000eÌh%ãM;¸£|Ú$
ÞNgdj\x001e@:%V\x0003
ñ³xÉ,·ã¡÷§§Y8Å\x000cû-á\x0015éà%EÉ\x000e<w¢YÁ1\x0002\x000cÊ\x0010^QH~\x0008^ò\x001a]xStî¸tÑ¶®­çSj\x001c¿->Ñàyëy8Ua§Öqpm=|êÆ£Y|ryVðÑà\x000e>nÈçÓ¼-´,©p\x0013ù¼?\x0006\x001f\x000eîð\x001aTfYR
ÑM\x0016b3*èà£yÂ\x001d|ùtXM\x0002(Ñ©yËxp\x000c:\x0012cí\x0008|Jm¢Ï\x0015t­6^\x000f\x0010ï¯ëVJÞþZ\x0004,8f\x0006!Òl«×L²1DÆ¾0ÄÍ\[bú`'*\x001c9?I#®ò§++RRDî#]\x0007ÐbA`\x0002¡¶ÁÉÍÕìG%¹ä>T\x0017øØàl¤ä\x001a\x000fu*ùCTwÌUeò.Ô`9xÐ1Dôi\x0006¯\x0018uó|÷¦\x0000§\x000bÔãÄÄd)\x0001ºM¯OÁØÍ §&\x0004t/©'T£(Ó\x001d\x0014xIµÙ¼'oAqúII»\x000f\x0015oôÉB\x0001\x0000Oö=èÀg
úýS\x000cÔ{üéÅPcÂJ¬âñO
*go\x0019«\x0002¢^\x001a78$å$\´©éE+*sÄ­¥Ë;Q5_û!\x001eGFUXÚ\x0000ÑÓo^múY)NêdDvJUü¨R\x0013\x0018T\x001cÑúsÀÔ{ª\\x0012ÃE\x00154oË\x000c
Õ\x001fs\x0003PðÔÉê©;\x0002YÃ	*kØ¬\x0016B\x000f?UYÖ¾Ó\x0003\x0008ôO\x0003ª\x000c$|ax\XdÇt\x0001ÑÖ¼ýÞ
;9è\¡hú°]­ã*uÔ-\x0010ýìõW^`}\x0013E+\x0013×UélY'òºý{ :+Ùë°¼0*5\x0002GV¥h
\x0015Fæ=\x0010¹®Ñ¤È^-\x001e8ã$íWl\x0003+xÇ¬röºÎ`îJöº,/d¾È£É¢Þ¼è\²É
³íÀ~V\x0015ýêõYÑ\x000e\x0013¡Ø\x000ft\x000c\x0005S(²\x001eq\x000b`Ý¶êwYf¢cÆf\x0018l? :JßXïü1\x0015¯W\x0007Ü¯Bjh¬1,¤Uì`8b$ ¢ÃR\x0007Ü¯ ï\x0000\x0003ôtgÑ¼\x0003z\x0019@OÕïµÆ-¶DÃt²Øky\x0007Gô°Xv¡ú½\x0016ø4\x0018\x0005Yí&O\x0000F1ëD¢»]£õSý^\x000b	\x001cYa;\x000c¬X7ÈVàÖ5\x001dìdõ©ó\x0019­«Ê\x001eÖIö\x0004âw\x0017ÔÊTý^Ë\x0007Þ\x0003èµ\x0002±\x0006\x000e^TÇÜ\x0003Ñc©~¯ÕÃ"\x0017V³¬Æsäbh^q\x000e6t{-\x0019¯W@ëj\x001c=ÀY)ó\x001e8**Ï\x0015ìDµIù8åZ\x0002£:\x000e²;b@%
Ðëµü $IïÉJírRPm¦û\x0015½^\x000b`r,¡uþr~®eÆªF\x0005ÝN\x000bÇó9MYA ò&+\x001dïÕ h¯âþ\x0005tû¬x¥Âçâ\x0001\x00157i\x0007 *±\x001esUã¾n\x0015ÿWÎ\x000bèèi-í\x0000O«¡Â17ktWÐí²VÐÄÔÚÒËÖÓ³¨c^^p\x0016=t»,©\x0004\x001f,
.\x001b\x0001Ðy]ç\x00023ö@ÜOÐí²°Ñ'7\x0010ÿ\x000eÜ\x000eJ¼\\x0004x´ttWºÿ¢\x0002×´®\x0018¶Påzt´ä\x0011÷+êmên%âõª\x000c\x0000g ¥u\x0015>'\x0006ü\x0011·\x0000ª¶én%¬ãj\x0012ÔPÙ¶ZÌEÍ\x0013cûH%ÛV°\x000f°
r °ù|ÞÏïXý÷,\x000c\x0000Õ\x0013ºf\x0001G­îïØ+«\x000fÈ
òóFÙ&Ja©ü<\x0010c#¢Æm¯û/Y&Wiérm\x0004½`B%÷\x0008¬ñ\x0013éþKVº]'ËjsÊÕiöXrþE{\x0006kôVúKå\\x0006.wUYfõ¿»ý¯{-|Q {±¿.Î>}Y=ýãvoÍeDâ(À\x001aK#\x000e\x0011\Ô¨¦Rî¹\x001bûÝâìôbyó³ws Sm@\x000f¤òD(©GÆ\x000c\x0003{pâ\x00020E¸Õê¯	ÓKk\x000f¡\x000e¹ÌGz\x001a|
dTåcÕ¦\x0019ídLï=FæR\x001f-(01ëúU\x001c}s$H~\x0006ì¢Ì\x0007'\x0008\x001e»\x0015)9,Õ\x001a6\x0001;Rþð\x0019ÏÍç¾\x0003'i1m\x0016©1¨	0åT]W7æ
1W]ØRCç;îQªþ0§g¢ªó\x0013r~ê[NI.Óâ«\x000fÉ\x0005Ð¼\x0013Þ½\x001bó#b~ì[Nß:-'K>EsÉÖRØÃ0þÍßßO\x0014©?-.n]Í¨Hw\x0018øPHN\x000fM\x001ff"ÇÏ\x0005i7³\x000fË\x001d\x0015i\x0005]]¤>\x000eh6h5\x0004?E\x000bä=ãí¨ÖlÁ«ÔgãÅ;\x0010é\x0000Ô%éôèê"õùÖr\x001d³\x001b\x000fdöfâÁ¹®.RKg¼K\x0012Niñ<\x0015
;\x0013òâm/\x0014nÁ«ÔçÚü¤èÖÍ9	xõ&2=xuúìÕÃnC²+8/Ü±ù`l¯ o¡«kÔç[Å9¸ó¸ÿÀ#ï¼ºF}6q\x001c×ØàiÎ$¨[Æ;Ê©\x001d¨Ïÿ´[Ðæ\x0005®\x0000×kw\x0014<.QÍ\x0017ãUª\x000fr\x0012xëAÈvÅÚí5Ì-|£\x0012õÙ|V¥±¸~<ûÚh­9±ò(gc\¢>Où\x0013Å|\x001eS©ûEe>u\x0014Ã7.RÍ\x00072É­á÷u|ÃÓÂrH0õìßÃGåTÍ|qÑÈqÄ0½.Ðd\x0014äx:íá£\x0012ªïKæ\x0005ù¨\x0018¥ø¾N\x001eçûRÙT+¶ö¶24ÏÊâ\x0016\x0004å&M=xT)Õ\x0017ÃPK|\x0000x\x0007>Í×GÙ~\qôlù¨t§/º\x000fjÉvø¼Hß\x0017¸ÁIùZó\x001e>ªiæÃÑãø$?\x0010Ù½\x0015=\x000fâ£Zf>TS§ãa¹§x}áp\x0013¹øÙtw¿\x0005ýø±¸­¡ßéêñqõõëÝïÿg\x0010åØ(\x0016üP °ÇKKbºB~§Ëëëå;\x0014Þ¦XÑ¥ÛÚs¥K×¡çJî\x001bÏÎþz÷ëGQì»H6\x001b,@\x0012ÅÐ2\x001eXrgäÃuSæ$25 Q÷9!¥oø_ôÓ/«ÜéÅjñæáéËÝý*M×Ø}u62Åè-Ø,@\x0010\x000caA!7½~TX.Þ\Ý\_.·Ï×0?ü5üúëç»ªoñêáéqñûÿ^þ¼zúûþ;¢$?ªGE\x001f°TcýÿS3WW7×åâôûåÍÿÜJ÷óÇûððÛ\x000fXUezø\x0011îóí·oû\x0016Í`nr *\x0008¾\x001e\x000e\x0012Ê\x001e@lÆo/#ÕwgïßoS>*°×gøÃ|$°Ôè¨â5æ>f\x001e&4ö#ýô7wû`k³0ìøÛ\x0019\x001b>únzeQZ(³^ËÃ'ÌUiªf0e»0I8\)âqCXàÒjè\idÊa>S¾*!8Ù\x0010\x0002W! å8\x000cJáëðùXCC\x0012µÎà©k"\x001a¬+$\x000f]+\x0008XÁhÀòJr\x00196å¬¹Oªo[}zøõn¥Ó7ÔC\x000fOõÓ»_n¿Í±ïñR<´\x0017¡%õÁ:©Ñ»¢â¥yªîaqzþæìýL2\x00147\x001eþÐD¦C\x0016Á@p¶\x0008\x001c]çâß0\x0011N·a(ímëa÷ \x0010\x0019ÐpP¼§\x0007&È³µ¡u÷®\x000cÒH$³ü°	¹2H;7õÖÞF6\ûf²a\x001cQ"\x000bÜ&\x000eÜ\x00195-\x0007a}µ\x000fÍ`4Î i\x0015\x0000	»BõdR\x0013XÀ\x000by\x0010­`Rào\x00023ü®
YDKOE^­dh`l&SØÈ\¾è\x0006\x0016R@ÍÌÉÐG\x0006ÕL¦)Ã'P\x001e2|\x0010xÉ¾60ìæ	Ð\x000cf©¸$\x0001Ç\x0010ò.ð­`¶\x0008º\x0019ÌÓSð\x0013ÞlÇ9|¹Ðôf§¤\x00045\x0008\x0014¡b-\x0016wX8Â\x000eCÛ\x001fm¿R\x001dÈbpïXáI³»\x0014\x00131t+\x0019ÚþÐlû\x0015B²üà­uL6!¨ØJ¶?4Û~eé­;9\x0016	Ðkkq&ÂÁdCsM³ñW>iF2'Ðt$É)Rd\x0007[\x0010C+M³õ!'á¸åË`:É	5¢V2ì\x0011ÍÖ\x001f{¼
ü¼-YÂà`¦CÉ°OF4[`,n8X!/Ø¡Þ\x0012Z
ÑlúÁeäe~ogÑh\x000f\x0007Ã\x0006\x0018Ñlú¦!ØÚ`(MFÖ¨É÷\x0019d\x000fÿò×ÇÏ~¸Á¡)Ã?Ì-+BdSB@EgNåOà©ÍÍÅëÛærm^àoÿúõoCÖ\x0004-\x0018þáÍÃý·»¿Ýþcï2	42,S¼Â\x000c¯ÿ\x0008»ÈÅ÷1JßÜïo®.ß¿=ûËö5úñ\x000büË?`3;>gã\x001eÊkÚÿépÈ^ÊQà<\x0019ÒÒåiítój*©}=\x0003JÉ¡\x0017\¶Aé¤zöSf¾Ôh\x001a:SSkêl(\x001fe¤c\x001d_¼ê2Ó¤Ö|&ph\x0014\x001c´09;2LñZÂ.\x0013âzR1k/S<m¥\x0002yúA=îýãê¸ïW÷ûÓ(qÝ$½õ:Ë.>hV\x0013TvóÂ¶\x001e¢öþzG`y¹=ÏqU«zq
\x0017o;kO4Ñ
²\x001a '7úh¡¤NÚxk¢dó¬îÃ¯ü0ÕmÖÇªKVÝÉO­ôl\x0013)&\x0014kÊ°yúpMk:q£eÔ´\x0011¼EÃôâÕ¨âïÃµ%®íÝ	\x0001³¹é\x0001§ ¸X^MHöÁº\x0012ÖuÂ\x000e½F\x0003+\x000e£ß5@Od
ûh}Iëûwà¥]ë@` &Ìl\x001fn(qC\x0017®\x0017XöMÕ\x0017ø¢Eét¯y/è¤b\x0017.õ`ÿ z7gý~\x0017£GÁºyáX{WÖþ¬Ï¡ÅxÍqq\x001fÎ&±ÔÞ%¸e
ô±ì¬\x001cìóh\x001e§Ú\x000b®YvP¼àÓv$ÜÊKÈ>7ácpÆ}ÉÑeÐ3ÂZT)âNÔþµñ
3
oâ\x000frxó5	w?Ý¯î÷F_®ºö$á\x0017ãø:6ñÞ8`Þ`=ÂùëËåå~BU\x0012ªfB¹r~\x0019¬Â@h\x0014g%ÔD¶°\x0019\x0012JHè\x0014T\x0017\x0010Ñq1 £±H\x0008¹ÍÑ¶@ê\x0012R·koÒTêß¡(\x0016+±r\x0016eQm4%¤éXÉS=XlÁUh&_à!]	éÚ!Q4V2\x0004¾ÜÅÓ+°í>Ð\x0002\x0019JÈÐ\x000e©X{H\x0004\x001c	DÛóÛ¯1\x0013O&­²:Ý²ýxã¦LB´\x0002\x001f«³\x0001²|¼Ã¶À¤²:9²ãè\x0004w\x0002iW¢\x001a5u\x001fâh\x000f¢ô\x0013
^ó)e\x0018Ùòx{ËýëbùËß~~x.ò«t\x0012\x001dJ½6,:\x0017üÄ$\x0012\x001eé¾|óöû«ë\x001d=h\x0019Sª\x0003Ó,Þ\x0014CgZ¸\x000fÞùmÞ±\x0005\x0013JLèYÍ@É7\x0019Ã\x000bé4[Ë0UÓN©KJÝCiéùqXLAÏ	ÎeÅñ<S;¦)1M\x000f¦O³½,ªáy\x0002¥F¼èÁ¶Ä´=:kuY³Àuðâá?Æjú\x0012Ó÷`\x0002§!â
Å5+\x001e ¤Ø¶ð½\x0001s}5\x001aìè3HÞfé3A
b\x000eSo3MA=\x0016É³>äh53äÖ|\x000bduÐe×IÏM²¨y§Ùºµ\x000eú1üáãÝ×Ú\x0011á\x000fZim¼a\x001aåÑôP\x001dÇ¬Ðç'f\x0013uÏ1­î¢5.\x000fAC+ÊæÉú¬"3ñ.5V/k.k<´ðÃíý·ÛûÕ^ýS\x001d²\x0012¶á\x001dÝÁøûá§îí<½ðÃÙåû³Ëåv¡£\x000cªJPÕ\x0001\x001a×»\x001b\x001eV²P\7ê$\x001c\x0007T ºgEå«ú à©&äÖý©ëe;¨-Am\x000f¨\x001dôC\x0007Ð¸¢¹¡Kq¿è\x0017í\x0000õ%¨ï\x0001*·T¯«{	t\x0016SÎ©\x0019´HÜ\x0019JÜµâ\x0000z"õèQS *¹h×áAZ&Ùs ÌôFã½éã+Àé4\x001ceÊê8Éó\x0004Ø÷\x0002½mT:N4k3!,ÒAZ'Ùq ,â¥r\x0017\x0015ÿ%XÂÆ\x0004Ú§ÑZ\x001dáëcAaiKCÙ\x0007\x0013ò\x000cG\x0019x°\x000c_É&\x0006é5¢dnA:(è¶JÍ/N>Þì!\x001d~	?¿PålFµµ'Åß>×ïouª{VU8OÌ
\x001fª.4Ýãõd¢¹\x001dÕT&\x0015ÛG\x0005+!
©\x001dk%9c°róãAKTÛµªFÐ#ÂÉ\x0002!JþüoúÍ ®^S×µ¦ZP\x000b\x0015V\x0001\x0019®¹á¯\x000fz"n'U5i\x0012XÞå3j*9Æ	\x00032£\x001eT×¤=~*þkèq \x0015iQ\x001dëtÅ\x0008ð\x0008¤®þú®çëÿAvÊ9Y£vT£ò¢F;Ej\x0003¿{Å35qEmFõÕ÷\x001f\x0006¡¶£\x0002Ð/~ÿ@Ó\x0019´µùû\x001fÃ¢¢r^\x0019M«Eõ^ñ(SÙDkC¿ÉJævR¨v*þ¶Ô
jÌ©AÛ¨ÆåE\x001a*ØZ/*t-ªåôD<T\È£gõH\x001cò|ó_æ'Ø\x0006\x000c\x0019gg\x0006Ä8G!Ê\x0007å·w÷·Ø(ýðe\x000f©WÚ¶ pF²Æ©
<E@G÷½í±äíùåâ-6L_]ìGU%ªêBjM¨*Ïh\x0001ÉO\x00110ÕÜ
%*ô­ª¡¯pqIåV\x0005\x001e{¢ÅDw\x000fª.Quï\x0006Hµ¯\x0002µ?R6
7ãUhïìA5%ªéÛ\x0000Æµ	¬£y\x0007 yT×ªh\x000f©-Im\x0017©±ùTé@\x001dp\x0016ÏßÛ\x000bJ#ª+Q]\x0017ªy«\x0006\x001a(e_!'tsz0}éû¾=¤÷q\x0017ÿ*ÐçB\x0003¼j\x001f\x00054 ¡o=\x0003\x0015ï¡¬=\x0016
¨`¸5ÍN\x0005«í¨EJM\x0014µp¬\x001b¯°ÐPÓR÷×0ÿé`­ýT£'ÞRi\x0011VÆÓÒÜíÊ\x001aGa­\x001cìóTnH÷§3¥h¤¸EÁ
b=¥§®ÊQªz\x0008\x0000\x001fÙ)9
kåªd¯òm_O½Z/«º[w V\x000e@öy`ÖÛÕ²Á2\c¦'º\zH+Ã*»,+ÄËµY÷D§J3\x000bvÝz<Ñ\x0015×Áª*¥º\x000c\x0016\x0008}ârsmj±¨ë>Ñ£DUªUûL\x0000Öï­û3\x0015¡j`V	G9Vª:VªóXIv\x0013Y\x0015õFså3ëöâ³&Öê\©¾s")\x001ax*\x000b(irçßQ,«ª\x000eê\x000bYRäêL\x0003OU!WËÁÄ0ì&Öá\x001d½¼\x0005Fµs½^ýþÿï}LG©\x0012Ò\x000c21hµÔÞÏéNªíßþzy³ë\x001dèTI§Zé\x00147ÄÅÊï¨1ò£§~±½èy\x001e\x001dtÐFgÄz\x0016«wk\x0001<âÖÃtº¤Ókç=³\x0000lÛó\~À%(b*kÒBgK:ÛJ'(ù,ãe8@»õè­aò<:WÒ¹v:ÍûNSªÁ@\\x001b¦Þ[àB	\x0017Z·\x001dGÂqÛù\x000cçYØÎ{}ØµAi´(¨Cg\x0016ã5*¿\x0005\x0017ñ¶\x0013óè*"[-\x0003*aZ°_6å|ß~3WYÙzh­¡Ñ\x000f8u*pÝ\x0008ç
BØ~yGg*:Óúi©÷7\x0008ºØÆïêdþ®[#yl=­\x0006å?Û\x0015±6âùF¼\x0018¯R¹F-Q²Æ2ð®)\x0005Ã&¼Ê¤Èf¢X`\\x00053úÒÇÍ\x0016oGÍü,<UÙ\x0014ÕlSò;ÄÓ¬[ÆÑ´÷\x0013ÒxMxU\x001c \x0003\x0001±IÂSô\x0016ñÔ\x001aï°½§*g¦Z½\x0019î½õÔE\x001al5´?ÍÛÞ¦3\x000b\x000fª\x000b­!hô\x0012d
ÞêÈa\x0018ËuÊuQñ¨Õ!¨Ôe\x0008ú&bìý´¾¥(*þ¥¥ªhÈ\x0005Ûz/o\x0016oâï÷³éM·±E;G¡\x0000CùÀ¦ó°j5¡Õ\x0004çK8ß\x0006çì"ñäG\x0002Dÿ\x00168Ú~\x0001Þ	·ß³ºö,\x000füâÅÅÃ·ÅÛ¯?­\x001e?ßÝ\x001d@\x0007YÞ}¨8\x0010¦\x00177 <íUNå.®Þ/pÖß×ß_¾\x001b°\x0007Þýàª\x0004Wå.\x0006§À0äÂÝ\x0008ÿ\x0000n(¹á\x0010n£ùâM\x001cêÍ
;Ci&¦Ø\x001d\x0000®Kp} 8WJÛ¬-\x0012Ás¥ôî\?¸)ÁÍ!à:\x0006çNéÀîäîg?·-¹íA;<ðEÌ(ÃFK\x001e\x0017:%>{\x0000¸+ÁÝAàY)\x0007ïk¤\x001a\x001aCy*U\x0017~J¢ª\x001fÜàþ\x0010p¥¹
H{K\x0005\x0001Æ(`p;%Æ×\x000f\x001eJðpÐKêÎÊ`rVgvO\x00153öËÚý\x001cäPT'ÎkÖòÃñ¨D.'ZA\x000f ¯ü<Ì\x0001e9 Å\x0003g<,§&\x000f÷W\x001eH\x001eäÈí·\x0018×Ë\x000fù6vÌM.+\x0007$\x000fò@2«\x0004iEäIF\x0002ÔQ÷JåäA.H
ªÞ\x001aõÌh\x000b\x001e'¦\x0004,\x000e ¯|<È	á<Î\x0014ÊFÉz<FRÛ®\x0013n"Ï{\x0000yåäA^\x0008ûÎ(²U³¬F¹ì>{>+/$\x000frCEdâmkmÍsó(M9¼rCò0?¤¸©\x0006[I\x0003\x0005x\x001cÜNI9wçgÕt\x0010¯çk ò¹ÀúnñÿÏàg3y²Æ\x0012
®P8ûúéá3\x001aAcph-T
2¯âû¯ß*äc|ß^½y¹³mÕµ	\¥M0\x001b\x0013ß7,aæC¨ÙðEÌm\x000fìMºÄÔ=«iYé\x0001'uÐ-XK~ñp\x0014LSb\x000eL\x0019X\x0000WSS¶(ä4´ÚöèÖiKLÛóÑ=\x000fóP*pÎ
K,x5w4ÏÇt%¦ëYMÉ\x001a
Jqù/Î\x0010È{s{;ýlÊBÀÕÚ\x0004³1æØ^ÁPa\x0012¬L	Ûê\x00140k{Ôa´ÜG\x001fw!
à1\x0000.O»9\x0006fuÐeÇI×^£Jß©\x0005>K¤++Áû­\x0002m-Õ	\x001dGH[ß$´âîT\x0000Öö\x001aÁé+NßÃ	>DNÒ\x0019\x0005w§júÍ)aÄ!}þËßpÞØzq÷eµ\x0013qµÊj]4$8\x0008\x0016øÀþô
Îó7oqæØÀzq~±\x0001ªKPÝ\x0003*B\x0007à\x0014w!¨÷AåÄ+h\x0003¨\x0002=ªÿ>¹\x0006}·º»ÿ¶xw÷ËÃÞ	ßS(!\x0015*}{\x0005µ\x0019ÍDû\x0004£¾[_¾_¼;sµ#XbX(a¡\x000bVãh^båÆT£,7¦ÂÔ\x0010ë.VS²>Vð¬ê£§\x00192*w§H\x0011wÁº\x0012ÖõÁ\x001aHUüH\x0004ÒdØ.ØPÂ>X,ú¦®o%\x001f\x0000Ö+;!Ô\x0003+ëóÕwÀþóiE°µ5?(­A¼>½~ømO¥@ÊHÖP\x0001Gí; ^^_ýy?!ÐN¨H\x0003yn'ojdö¦\x0003\x0012Ð´\x0003Ú\x001cÙãâ5Ëax\x0007(Ç_YÖ
ó¯V¾=Ííf³ÅWñbG\x001anô9EÌÛú¥\x0006¹ØWËÓ÷7;¦fP(A¡\x000bÔðü\x0000\x0012Xtrø\x0001VMXÐ\x000ePWº.P\x001e}%%
ðÒÑQ<è`ê§SêË\x001eP¥ú£1Ê3º$OBt~«\x0016b\x0013©­Hí3&õ\x0015©¤ÖÎ}¼W»\x001f\}úy\x001fR\x001e1¯Â¹Èé@pU£Ñ;nÊ¯"ç÷;/#©JLÕ9ÃI«\x0019í\x0014Íçð;$ÜÔ\x0014ÅvJ]RêvÊ ý	/ÂF\x001d(½Î:ìHÌÆ´%¦íÀ\x0004M¦\x001ca¡x)2æ¶Ö¨&L_bú\x000eLÅRÑq5%óëØÔ¦fÌ"'Htp¢\x001e
9$\x0001ì9½çû§\x00131R;gudÏ\x0019Â=ºÏK{BÆ¬ýæ\x00116§¬Îì9D\\x001bw)EsÜ°ãµ<ÂÆÕù\x001d\x0007\x0008Ó\x000c sfGñ]\x0014nÏI¢õ\x0017Ç;í:ì<]}ý´BªÅË9Ùq|6éJ\x0006¬JJ¢
Ñ¤²vÇðótùîtÿËâåÎ\x0011íYÌºY
V~`Æ·>KÌÀªxfâ	¤\x001bÚÐöÎ/
\x001e,\x000b\x000fÑ\x001b6øÆ¨vhcFßÒó><~Äù×ûw±\x0015<ß\x0004Õ°9\x001d%óÞvÇzuý\x0012çÍíÚÄfÞCLÕ©¹ãT\x001agÛº«hÃö,d\x0003'ÐÃÅ´1ø£9¤^ð<©¶N¼j\x0002Õ%¨îZPà²i¬\x0002\x0006\x001a|\x001eXÄ\x0013½Ã1@M	jºVt\x0018Ë>Ánî´¢\M)óåmÉi»\x0016T­9\x001dû¸ \u#w\x0005\x0000
 ®\x0004u]\x000bªH\x001b	+Q&\x0006®'W5­\x0013ä8}Éé;w(ÕXã\x000cÝ\x0000¼C3h8hA\x0015µ{`Ðîyûeõïy×\x000fàùý·åãO·÷ßö¾äyÓ'Nã*«$Ïé\x00137x{±<å\x001bßõ\x0015f{\x0016Ëë×gï÷£C\x000e¡£46£<ºÒóUÕÛ	]×\x0003Ðu®¹ê<\x001e¡\õcÜ\x001cHnñ²ÍIÁ<&#w\x0013\x001bí\x0001è®Dw¡;Ï5×*9Fó´aÒ%G$÷%¹?Ü:.¾RVò\x0003±69m'J\x000e@\x000f%z8\x000c\x001dåÖ(µ`³ÑùÓÛJ÷~tYFy mn1\x001dòuÉN´0\x001eÀ^\x0019\x0018y 1=-»ËoõEñpí\x0007 Û
Ý\x001en°\x000f8±\x0003\x000fÚÆeôcZ\x0018YSyàA]_YÑ®k^váþ3ìz¡à\x0002IÁå ê²awæ$\x0017Åñ9u\x0013Å\x001d\x0007 ×!Ìç4^º\x0005£[,LJì:oö	\x001d\x001eöQ£\x001bþ Ty|¸ÿöO·O?îÍ]Ç¥.^(L´&mVÛr×7·Wï\x0017g7¯öcB	\x001dÑóTÚn±ùò;¤(çc\x0012Ót`F_NýÆ¤3g\x001d°_\x0017a»\x0010Ù|L[bÚ\x000eLËÉñoÌ2ô¿[ç¶blÀt%¦ëÀ4'eÈà¸Î;~k¶\x0003b[1Z\x0013¦/1};¦ÇæôÑãç0Ôå1hNo+çlÂ\x000c%fèYMË/\x00162HÌ¶§ÕôÀo©ÛR\x0001-¥ô ª¤\x0007g/'k'Li¹78AsÛêå k«Ùc6Qh&y0¬±Ê¹°í\x0001½SUªc1±\x000b8Å^R\x0018L\x0008\x000c«é¹êÔMõµcVÖ]vw¯eþæ*O¸\x000clÝòGpB¥Ê ªT\x0006çcz\x001aa+E\x0000®æô¥&<ÆjVNHvx!÷2 LMC>dÌíúró9+/$;Ü\x0010r¦¤ðùÙÜKj¶nÛ`±&ÊÊ	É\x000e/ÏæD\x0019ÃhCïTü\x001cmÞ.Ô6²òA²Ç	E6`L\x0017\x0013xà¡
G9é\x0013\x001d^È\x0007Ï\x0013ÇvP\x0014o¯tcàUåT\x0017òÓ§Â
\x0016ÒòC$ì%9\x0002geàU\x000fBrÄ)tÎyëózNô·sV\x0016^uXø`O\x0004VË$\x0014@q$¶k¥4`V\x0016^uXøHD\x0002e"DN®>\x0011,gåÔp¶fÎÊtª\x000eÓ\x0019âµ8uÄ\x001bâzí`ùroÅ\x000eaÖùñT\x001dÆ3xXsZ§\x001e\x001cëGà#ÜÛTe>Uù\x001c8é»ÇÐReNÃÔ´£fÎÊ|ª\x000eóùÇ¬'Tæ\x0013:Ìg\x0008\x001erc\x0004¢IåÚÀ:1\x0004=Âþ*8>X\x001eÆj!Ü¾\x001d\x000c÷\x0011Y¹cÂÁ|ÎÊÌC»÷èÑ\x0006HÅåÙ6\x0006dÌT¿C;d£é±ñÁåAõ<àÆ\x0004ïxoÊmGMv\x001bï\x0005ê(
0<ÕB8z\x0019µ\x0006&\x001e_Ú9«0\x001eÚÃx³Ì,íÍ\x0018*9>C,\x0011ìõ\x0011L\x0012T®\x0008Ú]\x0017Þ¸¢ðøÕÓ hFÙt*u\x000cT¹"hwEq9\x0015\x0015ÆåÔÜu\x001b\x0002çæwG\x0008A rEÐî¼ZñâN4Ì\x0000+ Sl\x001b\x0004ßÄY¹"hwEñÖ+XÅ>¨@%V¨l&\x001eÓ1uåt»'ò\x0012è)0\x0017\x0014g-
]%Lía;uåt»#FÉÓp°\x0018\x001fk\x0016\x0004Þ\x001dæ1\x000e»®üîðC2ú\x001fC\x001aëZÑ3¤¹\û\x001dÃ\x000bæsV6^wØx)õÕãÕS*´h
kç¬\x000e»î9ì1O\x0003a)+tà\x00050h55i­ÓTÛÓtlO©<ÇsXQæù\x0018	°\x0012¶Éi4qV!i\x000fA"§àáJÞ\x0004J}YÉHì¯3²~%êñìÄa7Ç4=\x001eóÀTª¬Ò Ã`½gy5\x0012vk»hqô\x001b=qKï°÷>½\x0014®\x001f\x0010qáÅ®Åõ8[QRðÊ*ìì)UkÌD1AÇ
d\x0016óVðc\ßEïbý~H¯
.WT9}Tã\x000fßn\x001fGç\x000cÒqô\êóéñØ;®]³vjy{\x00080^Ü¸çzv®4@oÝÃ\¨ks\x000f¡¶SÓ6gÓJ	u\x0019ÄÇ°\x0017/¿ÞÞ'ÐÕýOO·\x001fö\x000e2¶Z`xÞguVïÓë0ÅDÔòÃÙe½X^¾¾9ûîjÇdPU%¬ê
<ËV¡"\x0007i$\4:%ÁÖ\x0005\x000b%,ôÁ*{Â¦VsoQ!Ú..V]²ê>Vð¹-*Æ°,Æ\x000b\Ò*&úõºXMÉjúX¥eVét\x0016à\§åü¦Ýêbu%«ëf¥:'\x0019]4µN£Å\x0006ãÀ\x00126\x001c¾°Ãkca7+Jz`×Õ\x001aÝ\x0012Ý´ô\x0004¡\x000c\x000b_¯iÃDØE[[ÙN3\x001b#Y*ã	Á
» 'ÆZvÁVVVvY¼Æº¼\x0011èÙÌ`ÅÅ7Befe5X¤EeeZçBßÀ\x0003\x0011\x0002ÓE[\x0019ZÙgiM\x0000\x001e
\x001b\x0004òõº\x001eêH+[\x0019ZÙiiñ
CDuC
WÂ¡>ÓqhmEk»÷A\x001aÅ\x0019ÿFG-Rq\x001bä#6\x0011 vÁV~Av:\x0006aYUX\x0007<µ~b\x001ck\x0017¬¯`}ßÊú0\x0015J\x0001+	á\x0015\x000b¥&îa]´\x0017½n,pK¼Ûñè\x001b£X\x000e'^\x001b\x0013$ªÊ©>7ö­­ªÜêtcÅ9cnwj§¤ºhëÛB\x001fûãÖ¶òcªó¾=³ô²\x0011\x000cf\x0018\x001fÕÄ¼\x0016ª}\x000b½áâi\x0012ØñoY®ç`Z=QsÞE[í\x0004èhÒ\x001d<ÑJñK´<V<zº#ÑV1\x0002tÞÆôº< ^Ï\x0003Ïtñü\x0006ë&*)»h+¿\x000b}~÷£­|\x0019ôù²?VW§Lw2çi&©ð.Ïè3¬K\x0011MÆ²3º:eºóýa´uÊ£óýa´Õ)Ó§ì\x000f£­Nî<e.pMÎ0kb°àr5ÁDAc\x000f­©Nyæ§ÌT§Ìt²\x0018\x001cXM©e7\x001cÉâÎÚLLì»CÉpºGâOõURþðq¯ùØwT\x000f#¥±jÖÞò=ÝN(nôå@6V\x0019zW¹L.¨\»¥=e;8Rº1®òj´Ê«ç½ÊòO#àOÏ\x0014XZl¥V,ìÅÃããêî~¯¢Õ`©$\x0001Ç((¶À\2³µPêlqqu}½<¿Ü¡dÅªTíàI+Lxcò\x0000&Íï9\x001aMðÁPBBÇJ\x001a¾
ºßdº\x0002ë7h»­ ¡\x0005Rº\x001dR\x0001)\x0019¦ò=~mâoÄVýÊ\x0006HSBvHëi8¨ÀvKKQ¼'·qµ@Ú\x0012Ò¶CJ;\x001d\x0001à¡âFré[5¶\x001a ]	éÚ!µ#ajáqàä[\x000cïÉm"
¾Dô\x001dë(©¾@`\x0018\x001f\x001b~C0rë\x001c\x0006ÆP2\x000eûc°6Õ\x0015Úüâ¥a]W¸]èy.dñÚ¥Þä\x0006Jáéíh8ÛÐ\x0014Ü±\x0018Ïöá\x0006HÖþ¦ÃáÄ\x0013-U¶åü½U.y\x0008Gp8²r8²ÃãHI]óq-U\x001e?'yÐ\x0011;$ÈgSV\x001eGv¸?²r9²ÃçüçîKoFq7Õ\x0010Û¯«/w¿ÞÝ>îS¥ó\x0002B®w>H§úLÁÞZí\x001apönquqþáüìz×¤\x0019¢U%­ê¤Å\x0007b\x000eÝ\x0002y +,_QdçH¸ºÄÕ¸\x0011JpÑ3ËzÄÅ5¹èy¢éª\x000f×¸¶w/pÝpxï\x0007n `?¥JÚëK\ß÷¸@[Wa º°²§\x0013¯Y]¸Â&ºxq4\x0002exYÂ®ÖT\x0004\x0019\x0002óNøý>Þê¬É¾Ã\x0016yMöÚ&Vp\x0013¯°}¬ÕA}'mhoLöÖ\x0006Ë\x0015!\x0017:À\x0016[\x001fmuÎd÷AóÔË."Ñòh\x0016x<\x0001Li5ÒÂ¸
\x0012*ÈRGëâîãíã·ßÿ}ï½>\x001e³$X\x0002FQ÷ÀÕ¥a"oRÊg]¿<»~¿ËÁ¸\x0008\x0012`¬[:5ÞP¨r\x0017°¥,OH\x0004Ý­'8\x001b\x0016JXè
x¯\x001f`u\x000e\x000b\x0001ëÌ\x0013,ìQ?M«KZÝK+N\x0002Áz,ÐH+kÕoÚ.VS²^V÷ÿ¨{¿äHn$Ïÿ*<\x0001
ã¯õS\x0016EIlc5,R¶3/²¬\x0012[ât\x0015ÙÍ"µÓý´¯s½ÁÎïåw\x0008ÝdO²ð;\x0012\x0011\x0019\x0011\x0019@¤d5k«\x001e-©?D\x0000î\x000eû×©¾\x0014T.-\x0000\x0014}\x00059¢^Ó\x0004kKXÛ\x0008+\x0002\x000f	\x00070ü\\x000c¬
oÃØà&ZWÒº¯|i}	ë[ÖSpÛÑ:Þ´$\x0006´GZÚPÒö¥\x0005¦\x0015(Jk«öÊâRÚ"TdÚº¸$p\x0003Òïö­Ê¸#Ù &Ü¾\x0017kucXoL;W\x0002'4 (
n\x0018y\x001bjÂí9²¡ÊlÍê²'N-¯®ä­+Fúûp{®L6û²Ý<ê\x0018å½«XnûXaìù²¡\x000eîòÕÍVL\x0018~\x0001a\x0018ym¢íy3ÙìÎ,O`\x0002\x0015!äÙºa¤~³	·çÏJ½5+y/x®ã\x0005gÙ\x0011)&Ü\x0018ªóÖø_ËjÈy\x000c\x0017ø¬dêFD-[pUÏì\x000e\x0015ykVçA{yÊ[7Ã\x001ePX_\x000cÛ\x000fÇ­Ø\x001f\x0003ÛÛ·jE Æ-T¨\x0014\x001cx#dÝý#í[Ñ×în\x0010ø¯ô\x0012a¯®V\x001du\x001dîÛ§ÇíÏ÷'WO\x000fç\x0008ZTÈâ!h3ä'\x0018BL¿ÅwÐo¯¯n7ß]\]_Ì
\x0014dvU²«uì¨BF»\x0004g¤\x0006®Èâé2L?s7ÁC	\x000fëà} KRpÊè6OC\x001déÂ]®Kt½rÝ\x0003\x0017pàqÔUX¿iL	oVÁ»\x0018qò:9\x001e%-¼ãítm\x0013¼-áí:x\x0007fãdECÒº*dEòRUð®wëàMî.SVSëõl\x001e½imb÷%»_Çns6KÜÓkC1Ó\x0019×Ä\x001eJö°rÝ]\x001eÁj\x0003wüGûágÊ\x001c[àK­U½ÎÉ\x0016z¤,
È [ã\x0004§\x0011ýJó*ø¾s]ç];xÚ6(l>ßÅF\x0014HWÑ÷Ü«\ç_ÿð¥ï¹W¹Î¿:\x0007,W\x001f&¸>îþ#oúë<¬ó»P\x0012DI¨¸z6¨©ó«è{\x001eV®t±.`:2%L\x0002Ñ:É.6ÈkÜ*ú+}l\{ÉéuMJNqµ_\x001cð*ø+}ì\x001f¾ô='+WzYùÍ\x0008²ÅA{z3\x001aQ&[Eßs³r¥u9{\x0001 X×ÕqGgP3Åã-ðªçfÕJ7\x001b\x0014\x0015I×*ÅsÚ9\x000f\x0017°\x001fñ¨ô=?«VúY/x\x0003hÉ¥HqéyãÌ7Ñ÷¯±+ýl\û$È\x0017×^\x0017kÏùp?2$e\x0015}ÏÑª6®½¡C«\x001d¢ÆµçWi\x0018)UYEßó´j¥§\x000bN*\x0012\x001a;Di\x0008\x0008ò©\x0013rd¦ò*ú§U+=­ç"¬Î`
2Òí\x001eÙ\x001bå¨§U+=m°§.E9:Þ
©4Ï\x0001O4\x0016pä\x0018Mõ\­Zéj½Â»T·öNí\-_«GÞ9=g¥V:+\x000f<4\x000c¼Áâ­äj¹ð%\x000c^\x0003\x000f=s\x000fkÍ½æg
\x00086/½âgàG´,WÑ÷\x0013k
fÎ\x0000ªÂ¨=ú#;+è\x001cXkr4\x0007
ZìjU\x000e\x0014Â·=ô\x000e-¬=´³Z\x001a\x001eèë\x0014Ï&ïr¼G¥ï\x001dZX{h
_Mâ­vwhù?ÌµÀëÞ¡Õk\x000f­ål½F\x000e¾XQqÃ;èQá{gV¯=³§\x0002j
;£yß\x001c;ñª{gV¯=³4?¥¶zgqH>Ñc	ºwfõú3Ë\x001b\x0007\x001bò®çiíbD¦r]2¤÷(\x0012"e³ë¹ÒÃ_BéÕ¿DtWö\x0011\x0004.9s<h9u½/a×ÿ\x0012]Ï1ßWø¶¥rÜ\x0006Ç~5ôÃ_Â¯þ\x001d¥
Bè
Ëç\x0007832g|Ýuwo3©õß\x0001X\x0001K\x000b±þ¹N)øc'ÚÄÞf\x0012ëµÁ\x001dÄU\x0015\x0013\x000f<
Í{q¤\x0013¡í¿ýãè²ÓèõäfûÏûC\x0005ï¸¬,¥\x001b¢SKuÙ:.{ÚþnTô"¼ßÜlþí|¦Ü1U©\x001a0±9Q:A\x000f':ÆÈi]\x001e+\x001f¯§4%¥i Ä\x0011I)s\x0013w+¦ :LÉ®Iãs=¦-1m\x0003&Êý'Ì yvn\x001cN©h×cº\x0012Ó5`\x0006ÉêÙèóék\x001b[tDv²Ò¾å[ÞXtÂkIýq-GdGë)CI\x0019ZÎÃ»YÚ\ù\x0017\x000f\x0010U0ãÎ<Â'/&\x001a£5\x0012m'ÈgL>çf\x001f"æL»ÐAL)Ì `JìµgþyûüÓÃãÁ¶¦\x0018-³\x0016&¦)
í\x0004ä8Å<
zþþäÏo.®\x0016°BÉ
m¬Zç´`dµ©¨Ë:½;\x001a«)YM\x001b+fþ(}L£\x001a­×¹ábDû°Ô\x0015;ÕýéC\x0013,\x0016QRÎO+Ylñ88\x0012ÅWñ*p\x00037ù<äö§×C\x0006g£)\x000e\x0003êÈuu.×{è09ááöûë»ÃpPÂA%&Å.t\x0005*äm¯GR\x0018UlºdÓUl:\x0018ªD­­\x000eÍòCFª'Ç!,c3%©d³¹"\x0016,kBféÙRËØlÉf+ÙänÃYv\x0016Ùxh ×vås%«óÓôJñ´«\x0008Çn¯Ö®/á|%\VªU8Þêó5Ï1ôjzôï2¸PÂJ¸xS *OËù:¬
©®­a+\x0007´q¢\x000e.\x000f\x0007ëjI!\x0013vÃ äÈ{u\x0015]ß\x0002×`mÍN>ðÈ\\x0000\x001e¶\x0015ÃÛußuWçÕÑ©ÊµãyÓJXW\x0014Nä²i±òÃöü¬s\x0010Úx¬BOK\x0007¹»Uq£àX\x001dB\x0015\ÏAÈJ\x000f\x0011¨Î ^EiZü®¬\x001bà±8n\x0015]ÏEÈJ\x001fã|H¾\x0010o£ä[³~°s+í°ì9	Yé%\x001cKïH\x0005ädyÓáKÉ*¶N\x0002Kw+G³$ ×087=Ãk\x0019]ÏIÈJ/\x0011è.'C§ûv\x001d+âÄóut=/!+ÝD1\x0005\x001dØhö¸WG<Ò\x0000Ö­êYbUiãe±Iüà\x0007\x0007/;=¥ðµ®gìT­±ûO¬êÙ\x0013UiO¤ xXªÀò¸¨àÁK7e®[ºÞ\x001c³´|Å\x001c³¯b\x0005ûYcTj!Ý®%W"Xq9jcàâ"¾¸-^>|~zýòðxÏJº"ÂÅPt¼r< az\x001eýåÅÛë»÷\x0017W\x0011U¨\x001a\x0010\x0003ÍL£êH¸EpôHme5"P\x0018\x000ff)Aóqì\x0004 ÁH[{5¤.!u\x0003¤ +áÊb¦}ÖSb5¦4õÒ³,,ÖFz\x0012T<?[=ÑUCÚ\x0012ÒÖC
O*\x0006Âµä	o¬$h¦Cüå®dt
\x000e¶áj\x001eÅcâÇ\x000cW3úÑW3î&"Åu\x000c4<\x001eì,$gGf\x001dTC\x001224@êSV3N\x0004³\x001eHüØëv©\x0005âËûðbÈxa7¤Èç¨Ã[{¾\x0011k7ò\x0014YÍØ÷4õ®Æ`µ0Ë\x0006
~0Å#Ï_{ýÉ=_#ëq\g\x0015ÁË\x000eÒæÉãn¤:²²çnd½¿1ÖÑÛs¤\x0014|-u©ÝÈÛI5eÏßÈzc¬ÄóÔk
¿EhÃÉAííúèBö\x001c¬÷8ÆìÆ\x0015ÄH
©5ö\x0010åt¬»Ò\x000cÞîã\x000f\x0006o÷o\x001f\x001eï}z8ü\x0004á\x0004 -ëª9¡s¹½}|{qu~óÃõÅÜ	áB\x000b¸ñó{\x0016Eè¼zj¬Y'f^xªpu«[qEnÅ0]¡kÂÍÒDcf\x001d®aðÂ×oÖµýròî\x001fÏ¿ý×ãoÿuðí4\x001e-Ý+T °]<kÚLÊï¾?y÷¯7çWç³/¼	%&4aÀÏ\x0003\x0002%&\x0008Ts\x0014ê G\x0000Õ%¨n\x0002ÅbtÄÊfrò5\x0019ÊVqÓ´-¨äªø¯ã;¯\x0006çÛM½\x001aTº\x0012Ô5jØ
S§"\x001d~­ØÚÉ$}\x0015¨/A}ëI¢~[aò»n<K<'n¬Õ¹\x001e4 ¡	\x0014xú±\x0008.§;X\x001fÉN¦k0w\x0019´L¢íË{~\x0000\x0011Ææ3\x001f]\x0000/è×¯"íÛÐ6#ª<=ïV\x0014gRP¬Ç\x001aæa*-½\x0013k?{¶¾Û¬YÃüÓÿý_ÿ{óéáãöñåp¥!t²\x0013\x001d'®(®8ÎÒ¹)\x0000'Ë³ÍÕ¶\x0010£ª\x0012U5¢ú¼Iu¾¾çwôhf§\x000eS\x0015)¤ÐFª\x0003åý;Rª\x0005¶SãffTT ê\x0012U7¢\x001a\\x0010@\x001aþþÈ6vê
ZjJTÓÊÕÉ"Ä¸"T¬pgÒ\x0011ñ®\x0006R[ÚFRI5È\x0011UpÄz\x000eûãµ`z\x001cD\x0005ª+Q]\x001bª¥Ý\x0003´O\x00037Æ\x001b3Ò2ÖÀ\x0019JÎÐÈéùã§éÑ$\x001aÂ¤zD9µTEÅ\x0011ù¾w¶}~Þþöÿ??}:È\x0019CQ2§NÒ=éô£ÕÙ\x0006§BÜ\_\x001e¦T%¥j ´XT\x000ed d\x001e¡\x0013²)\x001dÑ~¯Ç\x0012\x0013Z\x0016s7®  1\x001dyÃûÓÆøï\x0008ºäÔ-Ë"<t4×kÇ(O³½¹æWpÓ´¬§\x0016<\x0012ôiÖ£u\¶rÊ.UqÚÓ¶p
ÅÃU\x0002>´SRy\x000crõU¾äôM]·òKw9Äík\x0018wAsgD\x000b¤ÉØçÉµ°|#E»õ=$[LÃ\x0002ÝÞ¤|½e	º¸5±=$lÒ\x001fÂÙ3I²Å&ý1½£.Îú\x001f±={']6\x001dõß\x0017sPÝuºöRgÛ\x000fÛç\x000eß;q"^HÐ\x0016gÍR\x001e×S\x001e×I?òZ\d\x001aÏ6o67ßÌ^>	V°ª
Ö\x0018îÕÃ©_4ÔÅ³\x0014Ã±¾Ga\x0015\x001a\x0017\x0016¸à×â³\x0008E \x001a5\x001cÓ?oÕ%¬n\XMCãÂ\x001aZÕÝ\x0016\x0010³©üå¤¦$5Ëª¨\x0000Cv\x0003Q©ÓÑQ\x0016×©±ioM°¶µm°(\x0002%	Öänk\x001f$ï\x0019)M°®uÍ\x001breVÇ+\x0019lX%æf}ÕÀú\x0012Ö7¯¬y\x001bäõ\x0019v$ß\x0004\x001bJØÐ¸²ü@bq@!}x*#A\x0005Ù\x001e¸Å¬eðçmpËWVsV?ÞX«ß\x0005*|´#C<hûÞ«Õ}qOZlÐÕì¾\x0016ÄìCÙrÚûþK\x001bî³°\x0016vkK¥qmG@6Ñö\x001clõ`[
-j3éá¾ÕGò`²çÁd£\x000bÓ¥Qº!Ô$Ï\x00114¯íW\x0013mÏÉV7¶£Åv/ÅkK°f¤Ø¨	¶çÅd«\x001b³Ü\x001bi/iq~ÃQh{nL¶ú1	ª®}[\à%ÓÚRÜ&Ú\x001f­Lçx&¸¬\x0004\x0015X\x0007Ayå´=G&Û=àµõÜbçxLSn¾ë|1­ê¹2ÕîÊH±Ç	ÁE¦G\x0010Åµ\x001d©;l¢í¹2ÕêÊ,·¤:\x000c\x00169LìÊü|EÍrÚþM¬Õin|ÃtV\x001c	Ü1?¢ÔÄÚsdªÕ¥63ìGç\x0003Æ\x001ad\x000cTÏ©V\x001f¦YxØÅh\åØ/7ÇÚ\x0001=¯ Ú/7!U9#²¨¼§-\x000eÄ|êÙYÕ~a`Ëeg:9O\x0012¥vn l\x0005-ô,\x00174Z®\x0018Ö:²\x00058+ÁsXK§\x000bäÈCF\x0013mÏ\x0016@£-´ÖÖåÉt\x0005­\x001bc¼VAÂ+þ\x0000\x0013^g¿Ü~xÄ·Áw÷Û×ûçC´ØªcXjWr) Hê\x0002öwÂÙ÷ço/®ðuðÝùÕÕæîöâüæ0®*qU#.ù\x0004-í)LTäÚ\<ÉûÙ6V(Y¡\x0015±äp¢\x0007\x000eí\x0015çfDÇ¢Õ%­n£Ek\x0016á{Â&\x0017¦°,áÂÈL\x001b®-qm#®Ó¸\x0001Ò¾í\x0006Äv¸ñú¿\x001fÍ´áú\x0012×7áZ\x0017O\x0019\x001al~tIRGû¬TésÊ\x001cô\x0002þe£YàªËÎ*xnà;¾UèÏzëN\x001bþ 	:i8&êÝ\x0016vÅLÅÈ\x0003m%µ\x001cööI_\x000e{{=¹Ü¾>o~Ý\x001e.k6NpFÁ ?Îõi3Âw'»ÍwwÙ*l9l¢¾\x001cVk
ÏaÆI¼¹g \x001bp,Z]ÒêFÚ\å*£Kæ1t\x001fÁ\x0018ë\x0004kÃ5%®iÄFÝ°\x0007lÝN¥.ãT\x000f·áÚ\x0012×¶®.×gvÎ<q4Äl\x001f`¤R§
×¸n\x0005.Õj\x001er¦UÈ
©zZÔ²Ö´¾Ö
Ã1XààÜ\x0008nwð~$phÃ
%nhÝºï¾hÁö«]×ï~\x0014\Ù·º­f×äk¥\x0016\x000cëY+,Ì´ÖÁöl®l5ºØ¦AÚfÞrëKÜÄÌ;¦ãÐÆÛÛ\x000b²u3 $Ü)7ã. GRbM¼ª·\x0019Tëfð.ÏIÁÍK>Øq»^32Öu¼½ý Z÷CØ)\x0010]\x0007Oê'uÜ¹%f\x0014«ëx{nM5ú5+E\x001e$\x000e<ö|×ëìÃA\x001bnÏO¨FGa¥Å8,ñªSç©}\çÑÜ3\x0003êx{ÇMµ\x001e7lâ¾C£\x001c«ótã\x0011\x0011&Þ]"§\x000b!Ek\x000c©óX\x0002?ôÄ{\x0010û
?"éÓÆÛ3\x000fÐ\x001c¢ÿQë+Cï\x001eLp©ýaGû;(ºBü§?Ý<½¾DZ¬M°O\x0007{|%\x0000]0þÔt¨:äüq#/>7×w·ôd\x00131¯gZ|\x0019Rª\x00012Z±Ôz®â-¦iÅMËO~V5OTBê\x0012R7@jGú²J8 7\x0008\x001d@ÐÙ\x001aïEª4%¤©\x0017\x0003lè@H©y>S\x000c\x000fH\x0006ÕYí×CÚ\x0012Ò6¬¤\x0002\x001aè\x001cW2°\x000e5¯M\x0018kX
é\x0006ãâã\x000f\x0006Ýgç\x001f?=-»A-Íæ\x001aHO\x0018§ªÎôÅ¿¸¼;ßn0\x0019\x001e1U\x000b¦ÎÒö\x0006[¤ø"N\x0002<N©âÏ\x001aL(1¡\x0005\x0013BNÆ(Ã\x0005Zz\x001e9\x0017Ff¿Wcê\x0012S7aj5nv×_ó¥\x001c¹kUSÒ´P*ÏÕ\x0008ì)!\x000cc
;Ó\x0019µ\x0014Ó¶	s\x0017èeCÈ«9RãWéJL×)¹\x0016=bª¬¦\x0016 ó#ìL_Rú&Jà9\x0001Æ8lÔQz~j²¹¸\x00023¡\x0005SX\x0016\x000bE\x0003jè½Ëq\x001d²\x001aÉ­,¦T0g,Ïpû¼}üû+\x0002\x001d^É]þ\x0007\x0007a&gyJöÈÓ\x00062ÞÞl®þå\x000e|\x0018Ñ¦\x001aQåéO¢â´\x0004¾
Pê\x0008¶D´õ@/\x00188ä½£\x001096î\x001c\x0000Ê0|\x0004\x0008¾l8x÷ðñ\x000f÷Ï/\x0007¯À\x0012G?fÝ7ò9\x0000#Ú\x0016üRüîâìû7ç7·9¡ä\x0006N\x0013\x000c?¬àÀ8à¬C~Òâ
P]ê&PÏ>\x001dh0;!+.\x0006=r¼\x001b@M	jZ@Mg^È\x0012îÖsä!»\x0001Ó®\x0005SkíàT´æÁ G\x0006ìµpöß\x0000\x0015Ð°ªUo\x0011WrHL\x001dÈ»\x0006W\x000cU3ERÍÜÍ¬ÀYUgO¯?Üz:\x0000ëÎbéÚñ\x000b¶\x0015:OÐ³s"LÝª³ë»·oÎ/¯\x000f#ë\x0012Y·#kê:x
#²àgì¹Y@Ä¶$¶ÍÄ1ü\x0014»HÔ$àèç9\x0010\x001dºÑJìKbßL\x001cý¡k\x0005z\x0015¶Bòìk	#­ÕÈz wíM½R\x0001$Þ~y¹ÿôiûøpÈÙzi\x0004O\Ó\x0001¨\x0012ÖJÇ7fáfë\x0005yóþöüòrsu1«3\x0010\x0006\x0007\x0010OÍ\x001alÃ#yp>K²Â\x0011;¿ºúlz;6Ø°\x0002\x001bòÜÓxÓJÌ,7\x0014·ôkgÖ%³^ÁyÈ|Ião"µÏW­fÅvjSR\x0015ÔJdóá¸\x000eÆJP´¯¥\x001eI^´cÛ\x0012Û®Ù ç1ÐP¼ÚlAF.íÐ®víÐ"\x0004¾S`;«¥µ\x0016¹\x001cÆÌ@lÇ\x000e%vXíñ»\x001aÉ\x0008Ã%Õb¶Ê¯Zö
ö
-¢¦\x0000ÔæëºÅfwn¾\x001ais]q Ë\x0008/\x001dÊ~Wå\x0006y`U÷¤T9Ù`FrÝõôJ\x000f.zñ\x0007\íÝãÃá2&>5SËÏ Z<Qm¤\x0000%g\x001dî®.æ\x0012Ê\x000c	%$´@
\x001c;ÃTó\x001aL\x000c9¿YÈhJFÓÀoô´\x0011ÊQfÄð:ÂâÒ\x0001Fa/ZF\x000ee\x0004î\x000f&â·äJ.´½éJïs\x00049ß\x001dv~3\x00063Ã\x0007-#ê\x0001K\x0018%p³\x0002¾ÈÒ§æ"\x0002\x000c1ç«ÿ\x00171BÉ\x0008
ëh¸EÁ\x0018à\x001c²gÑWÌ'\x001ea!u	©\x001b\x0016Òd;d²p¶÷<ÃUª¢jHSB´ødî@\x0007û 9,ì|#Í"H[BÚt4ÀÕ`97}m_Dµ+¾¶Ò0´ãPªûÞ>ß#Ña!â]\x001e\x000cÀs±\x0003GxÊýdaÊÛsüù\x0002LUbªzLo\x0014pÀ¬<\x001doÍäX©n=&Ð)à¢Å÷¢n15«\x0006Æ¯¢Ô%¥n ÄúwZLÒrÖñJÊqèõ¦d4
XeE\x0002ÙøÞFû2KÐ\x0006å§EcÚ\x0012Ó6`äb0åøéÅyÁ§gFÎw9¤+!]ËZæ>ÿ.V£µ´üú\x0012F×SúÒ·,¥åËR¼Í±ÆËe¬jj*j\x0015e()CÛÙ¡ô1 çÉÇ«A'_.+(eßª7u\x000fVÒs\x0017sùsO"«bìtÙdÓ%>³±M'Ed¿0\x0010/t+8\x001ajh©Ö·O¯'oî\x001f·ð\x0016åe©ó"\x0004K²ÚZ\x001ay\x0012cøéhãÛë»«7ç7W¹4¼\x001aJh©V
«\x0010xõí*}Âþ·cL£fäªX¡d6Öx÷I¬\x0012õ\x0012\x0000¶ë»´y©Õ%¬nõÁÑ\x0004ù \x001d,h\fbu3î«XMÉj\x0017D'âi§¹°qa9_¦ÍH Ò\x0004kKXÛ¸c\x0015/,jÑá\x0002YGdM¬®du\x000bk¹éÑ;MéuïÞ\x0004+F¢§&X_ÂúÆu|óÚÓ\x0014Ù¸²ür<ö\x0014ÐÂZÈR©¾,Õ×\x0008Û³±²ÕÈþÎ°Ò
®wñ\x0007è¼Þ}Ú~Lf^?\x001d\x001e7¤È\x0019\x0007\x00118\x0012Àd"¿\x0006\x0004¨ï.7giÈÌõÝåì¸!7¸5!$ÔCc=î	{à¬ÜH®\x001aÒ¦i%©K%º'|å¦ty%÷?y5¤+!]=¤ì\x00126©~Vóø8er\x000fã¼H5c(\x0019C\x0003£ã\x0007÷îù\x0016ÒzÎ\x0017XÎ\x0008§~Â³ËÊ_v\x0017\x0007Ë­tP<¾Ük\x0016½\x0000Ë}>~Nx®KÈ_vÅ\x0017sUW0È}"î^õÅR\ï©\x000e½«±ã2@~Äò°\x0019É:`(¡\x0019Xî*îx h\x0016$ö~.ÑXÇ«KÞ½Z
^J1#¯à\x0005Î¸Ç¢5%­i¥5\x000eã>Þ¾õ\x000eBæ=Xs\x0010XaáPýãöåäÛO÷¯s¥xÖ(¿§¢£âáÞ|Ã²^În÷'ß^ßÍætÃ°ø?¨þQ[ji²dDÍ9\x001f°kYå~f\x0005*¨Ðê3*Éû÷Pg$\x0013+PMjÚPwÖKXî\x0002\x0000\x0016º¨³æv\x0001*\x000c"ªøÁ[Ø§/½?Xç\\x0002¨\x0002¥iYäSRÚ\x0002P7p&¯ÿæúý¿ÜÏÖä
ræHªH
ð\x0010f\x0013pô¶J\x0003rÈ\x0004(;RÒÜB
%)4ZÍãZ# \x0017:ÁÏ\x0010
FrAU¨Á\x000cM)ËÃ^1ü>Ùý²}ýC¸Jp\x0012 ðª¸£IY\x0016="ßÅõwx\x0005¸9Ù}¿¹û\x001fU¬¦Ø\x0010\x0015´YC(Ã\x001d`ZN«\x000bÕ"C\x000cÍÈÐEä<ãGH.0z¤ÿ¢\x0015YÈº\x0019ÙqkWx~\x0016;[\x000cÌh8Õ"\x0012Ù4#cÕÍ«LæLè<6*¹\x0015ÙÈ¶\x00199°VK\eD\x001cÿ!>~JOWúÔ"»\x0012Ù5#\x001bOóiã*+nÞ\x0010\x000b\x0014\x001eQehE\x000e%rh·\x0018U*¬àõl1d¶\x0018#C¡\x001aeÏÈÉf+\x0017c\x001bnÙ
ósFþ\x001eÓ¸oeî\x000cÙl3Àg\x0001à9coâL3VÞÆ¬to7wÇ¤
\x001aûg4µf£ú=Vyî£0fD2ºù\x0008þ¸í\x001fÂmëae'(8#\x001c\x0019è\x0004åQâÚþøq¸Ø\x001f[WÛ\x0019jîl´¤j;ã²'\x001c\x0011\x001d©å~PAÂEiàöäÝöa\x0001ª¦\x0012\x0008\x001a§¤>cy\x000e·\x001fÃÍõlw\x0005ª$TõY¤_©|×±\x0004ß§K^#B\x0008Õ8\x0016Ñä©¶ØH#¥åµº$ÔõèxÞºJ­Ñi\x0011ù¹>.âÔãírDS"ZÄRt\x000c4\x0017\x0019Á³\x0017=LN1^hKD[ÿ³\x000c°Ry$öTZi½\x001aiæ©Et%¢«^E|w´½I?Hå½8òF[èKD_½Áq	-®"M6ÓAÙ¼k	wO\Q\x0014õ«(¹ë\x0002/bU£r6N­?Ñ²g\x0016eµ]´Jäü¦â\x0017ncäþâÕ§Eöl¬6:VSzWàXÝÀd\x0015Á±$ÁbÄ0ô~!\x0005ï\x001e\x001e¿<=\x001eÎcEKCÊ\x0006\x0012+i=?fÿsj$.Ê¾/®Þ__ÍÊd\x000f\x001d`\x0008e9åRH|Áê\x00187\x0018/§'\x0018¶:N4JT3BÉ\x0008
\x000b	4\x001a;\x001ayðÊ\x0001n,ÍZ
©KH]\x000f)\x0015\x0012\x0002³üÅ3?íL\x0005ÓbFS2\x000cü((bXA¦G\x0005z\x0014´(`´\x001eÒ¶\x001e2\x001bwVÑS\x0005µ#
uÕ®\x0004tõÚ\x001aK_Zóä\x0006\x0010$¸jQ\x0006r=¤/!}Ã*\x0006ÖO\x0012&+ß+OÕ)Öb÷êjÈPBzH\x0013ø¹\x001fåäir&(.û³näº\x0016²ð×¡ô×Ë)çe¡vyÐ´ÔÑ©ìû\x0006g\x0013w"i;bë½`JvÖNÍt­¡ì9\x001bÙàmP!R+6\x0012\x0008Q¤¾ª){îF6ø\x001b¿£>¤1Ò%J3ÒATMÙó7²Áá88õd@l\x001f~q>áf¤+½²çqdËñã4\x0011/ô<mèLy\x0000Cö\lð9ñ'.BWXúà?¸\x001aÑõ­ì¹\x001dÙàwP.¶%¾ªÁ\x0013®\x001dXMÙ3é²Á¦\x0007-\x001ai)U\x001e¹²FDk!UÏZªzk\x00197\x001dÍÀ\x0001%ä×pÏ\x0012¢&p-§t\x0007ÆøòþðöõùápÓX¼ù+
\x0004ªè¤7/«XGÇddÆ·w7\x0017³McÌ¨JFÕÀ¨)÷+\ô@©l;2R
þgª¯¶\x0002\x0012JHhäñ$Â\x000bI¯\x0017VY\x0012Î±Ú\x0008ÆVCê\x0012R×Câ\x0013K2AÎ{ºr[\x0016´1t?ÂBÑ40jê\x0010\x0014^vR§C!mgZ^\x0016CÚ\x0012Ò6@zÊ¯t_ÔZp2UþÚÓÆ|1¤+!]=$Ð~TrºÐçÆ8i=¡/	}\x0003¡¥ (~kG)Ó\x0018|[üÖ##Fª!C	\x0019\x001a \x001d©L	¯\x0005K(ÏÆLü«e,î\x000fhÆE=$ýL6ÒÇp257YÅ;Eõ}gÓàmðÖ@K\x0013²\x000cSò¦\x000c3w±Å=w#\x001büQT2\x001c?x Ò\x0018øð5'ÆHGøâ=#\x001b\x001cN¼Ì\x0002}ñxãQ	RÒ¼LÛM\x0008X
Ùó7²Áá¤\x001bwÌ\x001f\x001c$§þb´â¡¸(ÅE¾mPb/UÖÄÈZ(ñÆè¸­ÖÍ¤¬Î67\x000b1U©Z05wW³Ü£\x000c,ck¹A,Ç\x0012\x0013Z0-¿=ÀnÌ7h¾\x00057ã\x001bcê\x0012S7`zÉÍ\x0010o¹aÓ¹\x0001ØÌ±©Ç4%¦iÁ\x0004N§Ï
À`\x0004w­Ú§øzLWbº\x0016LÃï\x0010àù\x001e\x00111¹Ë\x001fûý×SúÒ·}sºÝâ7Ï	¬ ó7?ÆA\x000f%fhÀD=S>è5CÁì0'ß@+06:4¢e9óiÀI|ÃÊ£ÌhÂrÎ¾yo±ï\x0001x^\x00158\x000e3±Ú;ÔíHÿ\=gÏpÊ\x0016ËÂ!sªÜ\x0002OÑÌm|9gÏ$É\x0016\x0014\x0002u*u3DÉÀ;\x0016\x000eséå=$\x001bl\x0011=iS±Ä68³³ðÇXÎQ
V	eÃ\x0014ÙNSHsÎ-èc\x001f²gdYBáw\x0016Åq2§¬\x000fù¸O§8\x0016sªÞqW
Ç\x001d\x0013oTÙ%I·Ly\x0004©z]5\x001cvì´Di-W®ç~´`&\x0015íj8{]5\x001cv\x001cñ@¶\x0013³T2$8¯\x0015f|SöÎºj9ë*ðûY¼PrÐi.ÆGpEªwTË\x0019\x0002R3ÌÉ2»Õ¹¦/ÆÞ\x0011#\x0004\x0012ì\x001d¦fÎl:Í\x0006_=gÿªÑrt?J±qGYO)ì ÉÃ~¿\x0019Î\x0014[r\x0015\x0016ÖÐD\x0011ã,¶p4xÆÚ\x0011U¤²á\x000cG-£U%­j¤59\x001d<\x000fÿµÂr\x0019^tñsÝ½5¸PâB+®¤òÐ¸¸"æxãg\x000c«Ff ÕáÆß}l°ªL6|Z Bd}à"Q\x001cç\x00189¤y<b\x000eíÏÏ®ç%ì°éÔª2Ñ°\x00101Þ>¨c^E7ï$!Z.{s3¯©K\x0011¡DzDQ|ê=Ïb+wÃSfäù"ê\x0012Q×#òqï¦§P©Åa¨ô¡gjc"\x0012ÑÔ#:6òâ\x0000íEi\x0018ÑÏ\x0008w-E´%¢ý*÷¢+\x0011]-¢\x0013ØîA.ÈJ¾¬{\x0019Ù¨ºj ¨\x001b1x//ICtêTZæ=Ë0!k([?²¥üá"ÒÞÞ.\x0001V%°j\x0005Æ§@*wÔûøÀ\x000f¿ÖÎÎX\x0004,\x001aºøÎ¬÷¼}üé$n!u\x001cyâó*Ï?6¹\x0018|dÀw7«oNâ&8Ì¥J.UÃ³@¹\x0004\í\x0006ÅæA¼Êìî
0(Á jÁ\x0002÷QõAZ0Ï\x0007FéVé\x0012LW\x0001Ï|UÂpË²Î©V\x0014ª_\x0003fJ0S\x0003\x0016M\x001f]hQ­\x0012.Ú,V\x0000ûWÅ
0[ÙÊ½OÑ\x000c»®¼\áÅ\x0007©\x0000s%«Z1àt4öÎç+-ó§Ü¿¿Tù\x0012ÌW	îÀ\x001eb×¯Æ­V.ÈîW\x0012,ÔaÖÞf0>\x001f=W\x0015\x000fÜhÒDå·L±ôæ47øe®\x0011\x001dÄ
®¾Ý¯2üXä\x0008,§Ã´5ü)ýH¢©¬gùeéw¼^"÷nZvHÎTKU`õÌ«¬²¯ÎÚäd´hÍ\x0018kÙ:\x0017ÖX\x000bÙ3c²Ê¹,\#m®¶/É É\\x0008\x0018ä\x000fp¼ã` Â/Ûûík7[ù|ûz0ÚÄæÇT¯gã\x001a¦%´\x0005 áXþ÷ÛóÍÝÉ7'ñ?\x000fc\x0012Û¬Â>ÍJ\x0011x\x0003&qz\x000bì\x0004í	îJp÷ß\x0000\xpüAN.¼¼}x¼þõéðØz\x001boÃ\x0005Õå\x0008¬àZ¥\x0000#ûø&¬{qu~óÃõÜÄz¦T%¥ª§tBN\x0004ÕwPt0åØ0øjL(1¡\x001e3z\x0016\x0016Ö1\x001e¤7mû<Ãè\x0010ójLSbÕÔ»×bl} dÍ)Ð©ÇÍ*J[RÚ\x0006Ê°\x001bà\x0013o&\x0014\;\x0010,°¯§R6U®Ät
Fçü\\LÊÚxöéÁ\x001cccú\x0012Òµk\x0019JÌÐp~¢íL.ñü¨,¸î²5\x001aS¬Æ,"Kãve\x000c\x0015XzÊ\x0005KVrNÖåö`¦\x001aª8{VS6Móùí\x0008pDRâÌõ_f*ÓTÅÙ3²ÅnÊ\x0018çñw\x0007Î3yÍ{ê!©âÔ=NÝ° Oy9Mþì.WÙ©qëU=Ã)\x001b,§ÏuUYßÄç¶à¦z\x001fêÖ²7>8­'þ¤Õp§7V(R_N'¦I\x0015\x0017#SÓ
5\x000c§\x001d\x000cÛ<o?\x001f\x001eæ\x0004O\x001c\x0014Ñ\x001cå÷\x0003`ùO#í´<ÂÉæfóvv\x000c\x001a¼Ã!¦jÁÄÊsE\x0003\x0010kyuK\x0015PbB\x000b¦RTU'|¼\x0008ój\x001a®\x00072rFUd1¦.1u\x000b¦\x0011Ôá\x001fWÓeL\x001e\x001f}fôÝRLSb¦®O©¬;~¦oÎFM\x0016WUPÚÒ¶PZN~ÄÅ\x000cùsBåÅ¬ä¯Àt%¦kÁÔ\x001a3ßi5M¾i8®ì6jdúl5f(1CÓÖ´¹{\x0003\x000bÐik\x0006~m7j²\x0019x\x0001¦á\x000cNðÅåòö|>\x0000ØÉÅ¤;° Õ h,ùÍ\x001aôôuíöû}{Ldª,ÞÊS°\x0011áÇ"£n ÃMê¥pPÂA%\®ùÀ÷`Mp\x0002`ÜëØtÉ¦ëØ°NB\x0011æ)éhj\x0018nú®³\x000cÎp¦\x001azg1\x0003\x001eU\x0013RsS½³Kál	g+á ÂÐÊÉSÁ[N;^¹éûÂ28WÂ¹*8\x0010\x001aÕÑºCI\x001bZ¹Ü>	aêÅ|)/á|\x001dÚÁa\x000eà\x0002Ç]ÉóUp¡\x000bupRpªÏE\x001aÞs\x001fLµ¦¸\x0010nwSí\x000c°¨¤³tùßÕÐåÏWù»®[9Ù÷\x000euî\x0001¤9¥Ój4·\x0015ç\x000b46À¯ë9\x0008Yç!pØÔô\x001cvßËõ\x0008g\x0015]ÏCÈ:\x0017KG.ÂÅ«å¥ã¶ñIqÈCpÒéAJÙiôú_ï\x001f³
Z¡¹ñå¤ÜÕUØIà÷A+ø\x001dÎ`ãÔ\x0010tóÃùUÖCKÃT01~\x0018\x001aJhhFó4Î©s\'&9®\x001aikf6%³ifv"äK	Xî¦Ù\x000c¬Y3´+¡];ttÒ\x000c­\x001d\x000bKÆ}Ì\x0016ÀXzèa5LÕP¥Ø>\x001f\x0007\x0014¤çl¹	ù©/^µx UÓ	ÍÍì4 aíLµOUx(,ÀxÀ\x0017\x0016\=¢R¡[L\x0007%\x001dÔ.£È'(Ö3ö>O\x0014wÓ^h!.ñtíâ9òà\x001d¤ôSÐüm'¥¾\x0016ã\x0012ÏÔ®åîCS\x001còê\x0011]\x000e~\x0016ÒÙÎÖ.^îàw»Ýk\x0017åî\x001c¯Äs%«_<Kx:÷DzÏ£åv\x000bñ|çëWÏ(ÂãCK±ÙÌ]e!Y(ÉBýÂQS¡5Å½'\x001f\x0018áf^a\x0016á/0²÷\x0002³lå4\x000e4ìølàBi\x001f$/\x001eLõa/æëûja¸¾Ó:ÏþØ;Rbtjd*A\x001d^Ï_Èj¡iFÄc¹\x001c\>Åx\x0013	®Åx=!«=¦à[Zì#±ü\x0006È«§§\x001aÃ\x0017óõL²¬¶É¹\x0008\x001f\x0005()ì\x001dUþ ÿô[Õ2¾ÕÕf\x000fø
ÕE\x0013C5SÞY6{ccÕêøzÆEV[\x0017ujÓ÷Å×
\x001a&á¹ÇÖ©0Õ(¶OõN¯ª>½»,\x001d1¾>Wõª>\x001e|AÎJç\x001dÉö8SbWùzÇCU\x001f\x000fÁ:ÎvCpñFºÀêðz§CÕ\x000e¼+%:g{zGÍ\x000e`Jò a·\x0017¨þp7Û\x0016Ô\x0015*.Ü\x0006rí*?8;8ï®Do6ßÌÖ\x0016\x000e½@õS,%Tø[ä\x000bB7óÚ´\x0010JB¨&D	&*³5,©!\x000bO«5/'Ô%¡®&´\x000fq\x000c±X]£g£Ey¦]hKD[hòÌ\x0018eq«Ö\7êÜd\x001b÷rDW"ºjDa¹ÕK:~0à¹?Öù©4]\x0005¢/\x0011}5bô \&ì\x0004¦cS·q\x0016²w³3\x000b!\x00121Ô"ê`v«\x0018²öu¹ú{R­n1b!\x001c\x0003j0bÙ2zc8Ø¶9çéÂÌ£ìRÆ¾á®¶Ü8Ý;[<`H\x0012<\\x0011î'¥23ö\x000c£¬¶((L±ô\«¶Q®6;²g\x0019e½iTâ+þ]>ÓÁç\x0016ÉÞÈå¦hêWQaï\x0006÷\x0004\x0016ØâI°nRy}9bÏxËzë\x001dÃ\x001c>ÔîxàµÏqý2öL£¬·\x0002N}^Eª`\x0000çBÞ«\x0003	Õ³;ªÚî ¼åÞ+±Ó¶6ùKL¬eìcÕñ\x0018*[çO\x001d¸(q'UåÂìø£e½C­ª\x000fõ\x001f²½#£ªÌ\x001fÂØ;2ªúÈ å¡ºcj\x0001lÀsâdo{Åí ,ìL7\×Y\x0011à:z¶£c7m,\x001fn·~1\x001cÊ&RÁiX©=k®kÍ½ÅnZ¢ª"\x0014\x001fÚ\x0016R#¨2-ºÆ<KCgÅDçGô`\x0016ÁÛoüAñPöíÓóÁ	ÙÈÇíã\x0018¤ñ½\x0015U¼.úúöúfv4¶\x001e\\qØR\x001d\x001c67¶å°"Æá¬
\x0011¦_ô±AÉ\x0006õ\x000bG­ÇXÀ)yáxôÚLÆn\x0019.átõÂñ,ÊKóu\x001e®ç§Cl1.\x0019<Íú/¹zzy¾?ùfûyÁ]_²B\x0005\x0008±û°\x0017ÌxD{u}{\x0013!7oç\x001eýPPÁç|I
áN«Oä¦\x0001ÍCmÀÏ³\x0016Ñ¦\x001a\x0011\x0014ÅÜ r\x00011Znn®¨Á_Dh\x0006¥¤(\x0016Sö)~yyÞ~:üf¡ø-ÏIË}~	Å´ödÞîâýíÍæò0¢*\x0011U5"\x0008|*Ëï\x0002ôªâ9í>×\x001a²\x0010\x0010J@¨\x0006ÔgÞ\x0004Ie"q
gÞ¥"ê\x0012Q· þf×pÁ<ýXMÊØV \x0012ÑT#\x001aËcÖôø§\x001d¢
y\x0015§¤Þ+\x0010mh«\x0011­eí°B1Y ù¬Ø\x0006äZBW\x0012ºjB/Oi
ãuæx\x0006+ø	ÍÍ5ý,$ô%¡¯&Dw×F\x0005\x001dt^ÄéWÈ¥¡D\x000cÕ!pùS¹ü"xàgz7%\x000c·\x001c±|¨÷ýVÉ<@ù¦à\x0005\x001fçI-®
Â¾c©õ,\x001egVQ\x001bKI£k8¤çÒÕ[Qö\x001c¬õ,q¹\x0014G\x0010á¦\x000f½s-n®s!cÏ·ÈZç\x0012#ÔÀb0.F\x0013"Íà\x0011lrðýo-aÏµÈZßâqH"©`ûYªéMSÒ"Neâ+\x0010{®EÖú\x0016#\x0012\x0015!¥\x0015ày/Nð¬`ìù\x0016Yë\"#Ð|¸DÂ"£eÃèGÔuj\x0019{¶[Ö\x001ao/l.ß\x0015k:FËîÅ¯	tÔà.óS
ÅÌËí¯ÛÇ\x001e~û?ÏÕêP×L\x0010`\x0010\\x001c©
Èx?å©;ýÑ\x001f6Wß\ßÌjÕ©au´Ò¥xf\x001d­?õt\x0013ôsJgL»¨Õ¬¦ýÂþRfÍ²ég·JX[ÂÚFØBw\x000fG8ÖÝL;-üYEëJZ×¾´R)^ä·kî³òÎ\x001d	6°¡\x0015\x0016øÞ\x0018ï\x000e§O`¹¹9©ÍE´\x0002\x0006:<ØßÐÓÛÄüÞÙÓë§§×Ï\x001f\x001eî\x000fÞÆñ3¹R%ð\x0011¾cÖÁ³35ñj´Ç¼Ó°Ä\ßÙõÝåõÝÛ7È~\x0018\x001dJtX\x001e$
>S"hªÌè\N\x001d#ü9Qååèñ_ß_uÛ%§Óß=?ý\x001a¡\x000ew{Ä T§î² $çÓäÍlÌtÃ»ë\x001fâ_.T%¤ª\x0014öp\x000c,To$ïa3ÙP\x0003	%$TCÆp\x0014ÍljöÉ/\x0013Ç?ÌM/gÔ%£n`4Ô':MÔq¢\x0003×\x0005\x00193ém+\x0018MÉhê\x0019½&\x0005)¥jnõ¬ö\x0018ÝÂ\x0011 m	i\x001b %\x000fÃþ\x000e\x001eàx01 õ®tõ1\aõ|¡8e¸@5SA`
£/\x0019}\x0003£æYº]ÝdS,íôõ"Èx¹\x0019¸&éRÐÏèK\x0017ÌMÀÝHAJôû§\U_ëõH\x0005N)¬¼y|é+\x0003±8äUÍ¼¤zâßÈ\x0015C>¿?Ú7ì¸PâB+®qøäÌb³\x0003\x000b6F®~Àº\x0004Ö­Àñ*}~7U©\x0015,G¦§TòJ#yyÑ¯W}»}x~Xà@\x0005µ\x001aJer.OgQpo&'w}Ù\x0017\x000e1ÌÎ~Ñê2Ì¸z|g±\x000b»u.ÙñS\x000f\x0008UºÔ-ké°	¿£ÔË0Tsé'»3ª0MiÚ0\x0003	s\x001b×VÂä·èI\x001d*L[bÚ\x0006L\x001caLÂæZpùN­§C»
LWbº\x0006L¥qSÂt8k»ÃTyìjô«Â\x000c%fhÀÔ,ì"»	ÌÉæ]bÕÎt\x001bGüÁþ=ïêéùa{\x0013ÅÙÓ\x0019\x0012ÑtRÓ©ñ°v¤R´Kºº¾¹Ø\x001cU%¬jE}¶´¨ñsÔºM\x0004ëF:&`¡Ý».\Ù|ì\x0005Î´&ØÀµpv,ÄoÕ%¬nÅÊ ØÀ/Æy^Y;ÒÚ\x0004kJXÓ\x0006ÃÉÝ\x000b%wS¸íÃ¼z6±ÚÕ6/CSKc)Ãcz;¹£°ºÕµ±\x0006ÁU"Þ\x0000H=VpÑ¸Ð&V_²úæÓÅë\x001acjOá=p$ÖP²Æu5¬Ä\x001cm6_Q-´X52 µx E \x001a\x000fWnêÜkàäâ&Ø?\x000eÁ{ên\x0016!X\x001eô\x0017\x0003®<nNQ¾¶gce£
:gø\±\x000fXyËØ¿V©¡VòÃ[öÍÓglN<|©rÀù\x0000\x001f^QM0Y¾óÐµõæºëR\x001b·¤\x0002zÊ\x000f/Ùqãm*µåt2ô\x0014\x0010 å¨<P\x001b.¸ÐËS\x001e\x0007På\x000epÓ#sÚhuI«\x001bi¥ [øx7àWÁ&¬»\x0019\x001e\x0007×¸fÅâ¤«Î¢\x0007quYÏ'ÌF35¸®Äu¸ZQñðñvC\x001a\x0017!7æé±Ò6ÜPâÖÍ Õñ1ó9ªíFî\x001cUöX\x0015óñ_Ãj\x0001¸ù(þ\x0013#0c
¸u¼1b\x001eÜ\x0019âF³pöËýçGr\x0010ß=o=tiô8J§ ¦«%îXU'Â«ø\x0010õìûó·\x0017Wä\x001d¾»Ùü0;i\x0006\x0006!x\x00045M >g^\x000c\x000e®M eP[u
(*z\x000fÅ]\x0003À»OÛ÷ÝìÍ§/Û\x0005)m\x0010v÷ÚäéÏ5µ\x001fhß]nÎâ§?Ù\¾ßÌg´\x0000²+¾htd[Q#\x0019ÙVY·oZk\x0019¡d\x0006ÆxÍ"ùFßÕgw8P\x000e½Þ\x000f\x0005j\x0019uÉ¨ÛÖÑÚ\x0015
¼6/ä¾eª4%¤iYH¾gx¸Ú\x0014ÿ!GRÕ!µ\x0019\x001c¸ãûóÞÜo\x000fêRX£©O8Tq£;«å¨zn\x0018ñÝÉóÍÍ4\x0005AB		_\x001bd\x0018$Øâ\x000fqôw÷÷/eØIx\x001bÇY ókFôÓþç»ó«óÛ¹0H¯!ªjB¨¶Ùµ[É\x0001?\x001f \x0007óÏ>KQ¡D&T¬R"Åqa± 5UDÕ#ÃA[HuIªÛHå)E¢\x0018hDy\x00086#j5¤
`pãÃ±ôÙ0½Æ@éõËÈuXÆÝx\x001e$#BtêÜ¾ä\x0015Û3¦lÓ]îÞ¿ÿÕ¼;\x000cî{\x0011V5ÂòLÏ\x0007>²,n÷¼z\x0014X(a¡
Ö±8H\YÉ\x001dð\x001aSë¼²ÇaÕ%«þºYMÉj\x001a7A7\x001c5%Tt\x001eGgàX1¬jµ%¬m
g\x001fFó§4z\x001eæ`åH±r\x0015¬0\x0003[\x0010Ð\x0015¢=½¾tª³§Ç¿¿\x001e,Tçêtm\x00025sÄðt/ÐcÂT×w·]êìúê_îf«\x0014Íà`!&|¥ñkøÕ 1@á¶nT2òTJï)|vR=Y\x000eA?nÚ~yy\x0006}Ð\x000f/b\x0004@\x001f\x001a'ý&NG3\x0015\¼4¼\x0000×sþ¸\x001dnëQ½ \x0019Hñãód)\x001c\x0015©ùã)vÔü^³<m®]¾7\x0004~gÕ8¨;­­\x0014Î3ï½*Å°:EtÕ)==ìï¶ÏÏ\x000f?¿\x001e¼£\x0004ÈâA\x001aô©¡UÀCÍÅ!jO\x000cû»ÍÍÍÅwó3o\x0015 ¢«\x0000iãÅWay\x0003+\x0019y÷·m#°-m+°tÜj¡µß))S½\x00130"]	¬ä`Ø\x0018fg\x00067wÿx1ìÂuÉÍ}RfQÔ¸1Þ2}÷¯71ÛÀ«J\ÕË5ÊRª<5Iç{ÌXkq\x001b-´ÐH#0Iê\x0005§É²¶]VÒ\x0011£Û«K\ÝëX°\x0017K/³Z Îµ³
\x00015¸¦Ä5­{\x0001¸ÜN*ËMÜ\x001a\x001d\x0019­îÈÐîÆ­[º´}ñ\x0007MÔ1\x0006'Ù\"\x0008{\x0003½a¤þ®Z\x00061(!
bÏ>|Ú¾l\x001f\x000fãb\x001bwÊcY\x000e-2¿\x0019ãd×¹wÍ{¹¹Ý\-ÁU%îÐ>,ÄÅ¦!G]¶Æf\x0013Ã]¶ Ì-|\x0010WÀ0\x0013\x0007ÃLÜÙ/ÛÏ;¹zzx>Ä\x000bÂ³\x000c«CQÄt#yç\x000cD7Ãûí»«ëÃ¼PòB#¯Ê·²Nuª´¤Èº¶rDº	XÞ\x0002ã_6";°:d/I¥Up=éeT\x0002K3T1jxÞÞ>|~ú²]0 Vò¸½\x0010
\x0005i\x001byËÄU¹ß^¼½~¿-v\x001eHß",4Áz¬¢Î\x0007\x001dh`	Nr§öµ¬b8(HèÁQ»Ü>Æ¨ì§§í®È\x000eÎà6,â
#\x00138p¹¹AÙ7×g3\x001b×\x000fÀz»_ºùíöÃóÃß\x000fG\x0016<
\x0005\x0002D®Ò:×\x0018Î¦l1üvóææâ_æBIF\x0012y¯&r92Ëm`=§ú¢Ü[`Çêß«M¤ÃÆ\x000fÑ4|Ú¾þóéõ\x0010,NÜ"å
£òÄ\x0018§øB\x001cF
Ìù¡3ÚËÍÝ¿]ß\x001dæ\x0013Z8M¸3ñ
$yð»ãé'bDó \x0001Ô ¦\x0005Ô\x0002\x000f,À0N
ÀSd`ä®V\x0005:|5¥:Û7Û×¿ýòðøÛ\x001d~LôØìÚ­\x0008¦5k´q.|FæâÍÝ»ï/®f÷çðÉÓRhË)µ!ñW\x0011ºc´Úø\x0015$\x0006¿&K \x001dPÆõõ2 Ìýø­:üÝ
%?£eåfÜhn³h2Ì¥ñisó>ý/åü\x0012ÿÉ\x0010XÀº\x0019\x0018Ë\x001a\x0012¯à\x0016RõadØQ#®-qm+®qù#m6\x0000!Ë\x0000ÃHËV#°/}+0Û Ø øaÌZËÚÊb¤I·
¸\x0010üÆÑð¢X[\x001e&<ð,\x000eÔgâ¢²\x0016b#D¸ûëÖm±Óö*ãö;ùÆJ+£o\x0019\x0006`Ûß/^N¾ß~¾ß¾vqØý¯ÛÇ"ØàC\x0013â2+ê0ÏÅEÑÖ·Î\^ßÄ@ü|s×bç?l®n\x000fS«Z­ Æê\x0013Ry¬egj7Ñ¼ßF
%5¬ \x0016Üìfcs§|\x001eK\x0006\x0013SmØºÄÖ+°ó4ÙN\x0010W[îù¹Ø¦¤6íÔÆ\x001b*¨-óà\x0000\x0007îwYl[bÛ5{¤«\x0005`\x0001#ÆÆ)\x0007,í6.²ÒíJl·bµ\x001dß%¶4Ñ< <®öXl\x001bv(±Ã
lc8@Æµcºlý&æ\x00046Q\x0017
#ÂeE½¶ÕÖü\x001cçTî\x001fÓ&óGåîYm¹ÂlÇíÀ­9¨ ÉwöÄ¸Ò6èÑ+¬¶ó­Ø²E]/à=H=!YÙÆÝ³r\x0001\x00146[\x0012áy\x000838u,Õ\x0011]»ì\x0019@¹Â\x0002veÄ´·}VFÃ×`ÚÛ#O\x001eíØ=\x0003(WX@å;¬\x000e\x000byÊÊ¦v¢ï¼Û÷¸ýíÝÕI&åÁ<ô®\x0010\x001e\x0018dß­z&P­0:Ícî°ãU\x001aÓÁ
¶&á§Rõ\x0003×\x0015&P;Å}ÊNkîû\x0007Ð¼½ÃHoO;w/\x0006T+@­Yß+q§Øµ[eæ>¢õV=k¢VX\x0013
¥\x000b\x0016¬­¡|\x000e\x0003ÃÂ~\x0015÷6Æ­?]4\x0014ÈþéOùáËûÏ÷/;èw\x000f\x001fyøp¿@?\x001eIRí}ÎË¬¹©G^w"úÅû÷çoÏ¯nwì'ï.Î¾¿xs~³à·Ð½ßB¯ÿ-´c%\x0001\x0007f7Äk'Ë9ò²ú·0½ßÂ¬ÿ-pLÉ\x0016`=ìÔµÿKøÞ/á×ÿ\x0012
æ~Å/Ñ~Ùt÷¤þïÀ\x0007úþäÓÿý_ÿûúùá~Éõß²¯õÞò\x0018.ÃóFV#©Øò·à\x001dùÉõÍÅùüÑî\x0017Ët¿ZÿK\x001fÆ½Ï³*=\x000fëÿÔühù\x001d ü\x001dà\x0008¿\x0003\x000e*Muv>ìfpðÿÔ¼ujù\x001dtù;è#ü\x000eiVm÷;XÅßË­¢Ó\x0018éd^û;òw0Gø\x001d¢\x0015ÉÀb3×(\x0016þ×r$!½ö°å/aðK(ÃýÞyî@ã(þ\x001d>+\x0007wßAÑa\x001f\x0003\x000fGÀ6ÀÁ~´±öwðåïà± [Wåð>m&\x000e­\x0007Û\x001aÊ_!\x001cãL\x000bV±;\x0012u.\x0019»­ü%rz'y9qß\x0002K{è·Ð*Ó9Á\x0013µýHÉýÚß¢ï«à¬
&ùL°pNç3qtG'{ÎZ\x001eÁ[[)wÂó¡0-,¸v­µ¿EÏ]Ë#økÄ\x0004$öggÉc·Ó(¼åWèyëáU¢éWÐ"\x001cñÒ\x001bäê±0\x001foü%>Në\x0015²»~
ÿòOËÝ¤°ä\x0011B`q\x000cí=¿øã\x0012\â6Î¦~üûÇßÜ\x0002S\x000cGÏ¶ñ¿¿ÿûÅ\x0013JD?½vWÈc@ Ì0zYÀz8£§ü\x001a\x0008·Ù¾¹ëâû³ÍÕæýíyüÁD»I\x000f'nS¨Àq*)K
Ö$Å.\x001cÎGi3\x0010°fÙÇ\x0019/§(ql\\x001a[±<Ò4A)ò\x0004ª Ãë\x0004û(äÎZÇÅß\x0006ÿX¼>8t
Ç¤aìño4y}
©¸&ø±ñ¥<JètüÀú@ä1Î\x0004z2Q¡\x0018ïÙÂã£ßÄ?\x0016¯ôÚ­ É|¯Öx	Ëyþú?ÿãË_ÿNwW¼±~óôyûðØUß½òr²yýùõËËÃã,RÂ¦÷%\x0011pcE:©Oq\x0017Ùánúæúíæâª«¾{\x001fÿäöds÷ÝÝûÛ©NÄ\x001el:{­°Ñ;w©IÀZÔ²dªâ]no)§a·Ï\x001fïÿ6GúãOÈúS+¬W5ö¡Áé¾<çCí²¿G@ý¨\x001f×UAÊá%TK\x0000DF\x0015C»\x0006ö#Â~l&å",\x000e¹Kë\x001a72\x0010¬\x001aJÖ'ûËÿ\x000c]lµÈøÇåý³§Ï\x001fº^\x00194\x001fºä*DJ]Å[	½Ã\x0000íòüýÉÙõÛ7eäÀþõ£ØúÇ\x000e'nnüã2"¿ýçÇO¯_æM\x0002 áîÈ\x0003æ4­\x0014X6Ì\x0002[ðòäüìòîýù4Ì¯\x001f^Ýß(Ë¹o^_º:ÏY\x000e\x001aJ\x000f]IuÚ^ù]\x0015Lqa#o¯ïnn¯ï&9îrÿñw
A»Àóíöeûú%î§\x0003ÈTg\x0016\x001d&tÞ!F8t*AÅ@mÀòvs»¹{µi°¬Ö-¦¾²SÆ@J(`N4õ@]Yér\x001aý×\x000f)¶ÅøÇæõäÝýÇ_æW\x0006çNÈä	PAXçÝ¢ìÐ¶Æ õÝùÙ÷\x0007ARÁZúÏe(¶«t@\x0014'BRÈÖJj2G^\x000c\x001dø!\x0012ÿÏþýÃ3åSþD+òúð2ãïLU\x000c1\x0012Õ$Ù\x001bÿFIõÿ \x0019~\x001e$¹»¸>Î\x0005J4\x0006~1JÜ)]åyD1ÔD\x0013Ä,\x0014HéÇ>ÏB\x0014\x0017¿\x0013\x000bY\x0014Ú6Î\x0004n\x000c\x0005ò²x?öfYìÏà?<Òý>ÝêïOðyûó\x0013sgÒ\x0011\x0012Î§7\x000fð\x0003\x000c\x0003Ãèüòü\x0004ÿróÝô\x0011*hâªv·ó¥4:¤fiÄqIÕ!®¤ç£kSÇ\x0013ÿéîºÇ¨Tö\x0014yp|:ÕÑ]\x001aÞ7a\x0015\x000f¾ã\x001fy\x001cõ½§#EÑ°4×Gè}\x001fYÃ\x0013£Uüc1ti6PäQjgâö¡Ñ!ñ.jÖáD[,ÆÁ)Ü..¶O¼Òü¹Öà@üRPóµ¤¢\x0000¢Ã¡»pùpÉ04u<ñdAÅéòÎ0Oü;ÒÈ£\x001có\x0014oxðz\x0002u<>©8\x0019y¨{)ZD¿Êú`ö\x0014*v³÷!ÍlÀÓ¥ònÖôì\x0008Rì\x0005Çu<q÷á\x001fË×tb#Oô\x0014x\x0014Ý.A\x0004¿jÿ`æ\x0005ÿXÎ\x0003§tØ%$ÙZÄ¡j ]uÚ1ñ¢k\x0010\x0014r9#hû\x0018Ï.»wù®âÁèÄÔlg%É\x0018Ú I>;\x0006Ç¬L\x001eï{·*\x001e\]üc!\x000fÖ\x001c*Õ}\x0015ÔÄ\x0012cõ0y\x0016àü=~nÿ·"sÒýÏ~Ü>Ú\x001e¸Ð;}<©\x0003JDð>OyÝÈ8`éþülss¹YÂr¤Y\x0002N³Ø9¾ôÔ.\x0003\x0016`\x001dNÊÓ,ÆAÉ@8FYâì%z\x0003«Âp#/Àùë/ößÿúSñ¥Î»;oÿí?ýíÿKí¥³\x0017OÁö\x0019/FÓÍ^ÙâÍsè.Òý÷$^8ÇÒ!èþs*-R5R.©\x0015B×¹\x0000@\x0019\x000cNp[¹Q>õú÷\x000fî~;\x0010\þ\x0019]RJ`Êâ Ïî3\x0002_Gã1\x0004+r+Å\x0017ÅK;½\x0001Oá]0ÅVKòþR	Fì^\x001a¡n/A¹xñ¼ãÈÖZöu2\x001a
Ý¬Ý»¶.ÅÃ0»(SJ?(FâÖ;ÿò²ýðéþåP@Òx\x0014©.	\x0003\x0004Éñ\x0018úcBtrþþvóæòüv2Ë)UI©Z(ãÍIó½\x001bR)§æ\x0004\x001f^\x0011Ö3BÉ\x0008-A%Ñ&\IÉàx{Ñy)&¯
Ó\x000e?¸-?øöäÏO¯\x001f·ÿx~:ôþ©\x000e\x0019\x0017Óâ\x0010ª\x000eT\x0002g\x000eúæ?_ßmþõæzî)+Ãª\x0012V5ÂºÝõÐ2«u²ld\x0015\x001aY}ê±Åà_çÌ\x000c9óp$V]²êFVÈ'*þ©¡{¥¤þõxQCËÞ\x0008kJXÓ\x0006\x001bo
òKX\x000cêøÖÀ\x0006`hæÇQGûÓ¶Ó¨SJÉy oè|ù+´\x000bVú\x0012Ô7~ýÇîuÉÇJð×wjÊ¤Ö}}ª0b{%\x001ai\x0003G!Rë4\x0012³;W²ÚO7îU%ºò>è´\x001c[¶B`¿*I£#3¾\x0007$æý«J«á"µÌlº¶mG\x000c÷*í]y\x0015?UI=édkö.>Lö`?´-®MSpq5=Oªn"<-î^¾¹
V\x000f+-úê0\x0007_,@\x0004*¾Â3©$Ç¿1pâ%ºÛ½¢¬bÒ=]Lx=ªt\x0017UUá\x0019\x000e¨lÀÄ¤\x001a
Å5\x0011{\x000fµtPÒÁW·xºÄÓx`NS}÷úsâß§\x000c¯Ý~\_KgJ:óÕ--ñl\x0015\x001eî,T`íòP×Þ\x001f,eM¢!Ú;»µx®Äs_×êeí\x000eþ¸Ý#hÕ\x0002\x0006I\x000fq\x0001m\x0012[\x000bè\x0014;x/Ï®P\x0003Ã'z²XÛ³¯Lp
é2$a\x000b-\x0015×¤Å?Ù+Ùãù?Çm\x0017¨ªDUm¨2I¤EÔ@µãø@Ü÷6R(I¡\x0014³¿©­\x001bâÇ\x0016Ùh[Añ¥r{9¾6T]¢ê¦E@5nNÆë¦H\x0001¦\x0014$¹\x000cq+L\x001d£:TS¢¦U\x0011\x0004PÉ\x0005t¯Iô\x000e¼ªî8\x001bÀ¨¶iUuÞ\x0000Ò\x0003?\x0006JIñTã*W¢º¦UU&ib!a3¯D`Ô`á6T_¢ú6\x0003 Ð@u¨BQ3nP.\x0000Ò{9á6ÒP&RiB[\x0015ïDÞÊ¹\x0000Û«¬mA-nmh`EÛªR\x001b0\x0016"k®\x001eYÕþSV\x001bkÏ\x0003È6\x0017\x0010o<&]0UÐù\\x0019¾`ÂQ\x000cìy\x0000Ùæ\x0002pFPZUj@\x000fæ\x0000
z\x001d\x0005µç\x0001d\x000bèìªK\x0015U÷!]%³ªÍq>ÏªÊF³*Ó\£HªEÒ{FgEá@ïå\x0018ÛP{¦J¶Ø*ÀWaG¿\x0019Ö3áÚù£¬j¡UC+üAK àùFb\x001b\x0007\x0002\x001cOw\x001ea\x001dq©.~ÐYO\x0016÷	8{®Ä¨J­q5
ÊÉ;ñùÉ\x0006LªJRÕB*bHeTî@±~\x0010\x0008
Ø«jC\x0012\x0015ZPãÿKÂÙqUQôV5\x0000nÂ^\x001e¬
U¨ºiUOø°Þ\x0015òÕÏñ¢*=i\x0006ªHMIjH\x0003Í6ÃKªc/ \x0002W=ES3\x0019²T¡Ú\x0012Õ¶ j¬_£ï/E\x001aÄ§õùûéèº
Õ¨®\x0005Uª@ç?à4ÓôùG\x0006ÆÐz¯¶·4¤¡ÉR;M)¸|\x001c\x0006jÒ\x0019UÝ¬å#Ê¾Im³©\x001a¸á :)´\x0004\x001dªWlT}X«X{J6*Z¨@\x0015ÏÅÝ:\x0008^Wo&«*Ö\x0001M\x0016@\x0019»K\x0002Aîi\x000b~\x0004:\x0005½c%Î²ûïP.÷Ð¼\x0007¼µV±ö\x000el;YÖ¢áO¬&é¢¬	7y·W­ÝÄªzgKµ­èú\x001díWïùÖbºI¤Õ®<[º~Ð\x000f­>mOÞ=<þö~:\x0014\x0005 N\x0006é\x001aì\x000eíP±oÞ\x001bå´m½Ü¼»¸:ÿf\x0001©*IU\x001béîÝ.H®41¹­Bi1\x001d\x0005TBI:\x0005ÿUêT7ÆC¥(mEÚ)\x0004PAQ\x0001ï\x0008 ¦\x0004\x001dN­_\x0006\x001a×\x001aÍÈÕÉÇ{Ä]¼ßIÝBjKRÛBªEÈé5\¾ayÄ\x000bÞe¦Ãê
RWº6RÍkédR\x0004A\x00195sÓà\x001aR_ú&ÒÈ³×	Ø¥ò×wÓqU\x0005i(IC\x0013)\x000e-ã}\x001a8¹Jñ\x001fÆ\x0006ÇØ¥E\x0012\x0010Í¾ømì{¨F\x0017õÇ ö\ü}ìù(Ùä¤\x000cjYR\x0016\x0018\x001d:S\x001e÷ªUë÷jÿMU\x000fÞT+QIó1µ\x0017¨\x0014¨:°«:ñw½ÔZgV{©µVËÊÞª´¬Ç	ªÀª\x00118Ú­ÜÜ,h\x001e3¶oáZ\x0007,ý ^Åk¿÷çO\x000fä=ì:\x0012§M\x0019r\x000fN!ú½WÇûÝåÅû\x0005ª$Tõ^eA\x001cìQärèÜÈï÷ëÕP"B=¢óüªO\x00119\x00128zj%¢.\x0011u5"6[qÁ6@.}7\°-ö(«\x0011Mh\x001a>´ÉUy·b\Å»Q÷\x001e|«\x0011mhëW\x0011;jdîC§g\x001e\x0011tî'ÞKðU#º\x0012Ñ5¬¢Í]uñCsµ«ÎéòéúÑÅ¾Dôõ«¨E\x001aIåØüLëÜÕTµèbÂP\x0012úE\x000c:÷\x0003ä\x0003md>-{ZDÙ7Ü
û÷ÿÐ²g\x0017e½a\x000cJñ-CÄx\x000bï½É\x001d7k¿´ì\x0019\x001dYou2»ÍèXÀKx{\x0003Ö»\x0017ùãËýsßOã\x000fj?¸\x0012§Îä~YA®Úr\x001d»°{ý©õ¾zHªH½Ï}VJ§i3¸5!»ì=\x0011²5-\x0003µnMËêõð'@VÛ#9¥à¹%L¸½$HÃ\x000eHU\x0013©\x0003Î+	É=!¹s{ïaa9%\x000c{­À\x000eÊ ¯?=üzøµ^ÞPÛ"E\x0018 Y
 \x001eÕzëË\x001f\x000e¼}Ã°Ï
ì \x0008r!¨\x000fJFÕ\x001fGO\x001f8ÕÞ¾¦Sô5 PB\x0003(Vèñæ<²v2/èt¦Sú+þò¦\x00045-\x000bj\x001c?Î ¨È\x000fI¹Þy®Lk9¨-Am\x000bhü2\x0013àÑ/\x0014z:\\x0003êJP×\x0002e\x00043\x0004îU3
²K²Gáô%§oà\x0004Á\x0015ÝR5±áùg¸ ëÎ¼\x001a¾\x001e)½»9ùóöù§ÇC\x0002z1þ`\x0007/õ)ÉÈÝ]|¯Þ-Yù÷'ÞÜ|sqµO|êëã\x000f*ù\x0000~x\x0013dåG\x0002áÌxÌ±NÊa&Câê\x0013àÏ¶_\x000e\x0008$Ò6ýÅâLö«D÷ÔÊÙïg÷ç\x000b\x0018uÉ¨\x001b\x0018
ß|ð] ×0Èü.p\x000cH[BÚjÈh¨ð:[öà9³\x0006fx«hYÇ~Ôk?¨]N\x0013Ò(rÌ\x0002\x001a~f\x001e'r5L»4°ª!«jbQ»\x0008»ÒpZUiß«^¬aa¾\x0012R¾òéõ%"vúâ\x001f\x001eî?\x001d\x00085fI%)T\x001aÏ\x0015C
\x001cÊÅ¦ÃC~}w\x001b\x0001O®oÞ\_\x001eæS%ªå\x000e1KPyÇ	"ã\x0015óí_'*ù äj>Ï²¼NB\x0016 ³Fð|_¼p\x00008ÑE
Ã,%¤,eÝ×U6+NZÀ ½ûº`9½¦öúÑjÏ¶\x001a\x0010gÑ¨¬ß\x0017R¼\x0003Þe±=	­Z@_\x0002újÀT(ÍÍtQüL\x0012ÿ©u|ÅC)_Q
\x0018DVòtÀ
HZò»³fh%aï\x0004Ëê#\x001cÃl6ÙRÐ°{4Ù»~ë½\x0016ZÂÞ)ÕÇäw72²wJdõ1\x000e\x0004ët;À\x0000¬
b£ñá%Ü+Ø«$T½m¨ª·a<ÉùQ	Ý\x001eÕh¹¼{lí1é¹ätTº¬OÝ^DÈ§ErÕÎªk#"+µînÈ©\x001a0ÿ
©÷S·,g³;}\x001d®%ü|#öä`y¿n\x000eI¯-#ðíïlû·NMëÝÓë<
Ñ%s6ÒiÞRÝç\x001e»ÃmÞ]ÜvRZï®ïæ\x00160U©\x001a0u\x0017É&7mr\x0004iUû^¦\x0001\x0013JLøjWSú«Å4%¦iÀ´z[âG\x000f\x001cYHØi(íI@¶`º\x0012Ó}}r-vXuññé¤\x000b¦ \x000cçò
jHÍ5MÂùé|þÙõl\x0019³\x001cfÉ¥\x001d\x0016],\x0001TYÇÛdq/©s+÷Ä\x0006\x0017\x0003j5\x0000ÔC-w÷Ï\x000f÷ÏÆMtz\x00104H+Åe\x0000Áå\x0002rºéýÉ»óóÙ\x000b+ê\x0012T7\x0006#²Ê\x0006ÖÜRÃ-ÏëCy$érP[Ú\x0016PÇ\x001d×\x001dhàÁ\x0003Üp+fjBk@}	ê[@ã§×\x001eÑ\x001b½HgùÓ\x001b=Í]\x000cZ\x0016îu/"\x0005\x0011##&
]v²k^ùÓï¤5­è jm¤uÙÂâè<\x0012û>\x0015±_!½©9\x001d\x0005¸0ÔNk\x0013UWO/Ï÷'ßl?SÎ
¸\x001d\x001c:cÉ{Ú\x0000oäq	8±/öö,'­®®oo¢ÍÚ¼¥ü\x0015\x000eu[\x0000¯Jxµ
>H_%Pí´Þv/|fo¢ÓJx]Âëÿf+oKxûß\x0005^\x000eýTåËËÙö×í§\x0005­åÊd¹Íx¡rRá³Ü¦Þëäç³Í\x000fË\x0003ÏWrèë¤Ú\x0015\x0019~e¦4_\x0017ä¡{C&\x000eh}¿}}ùQØÂùHX\x0005IfÀ\x0018~\x0003+ øi!ïO¾ßÜÝ¾ÇXl7,é ®*qU+®£ñ\x0002 å)O\x000b¢UE\x0011#±BÉ
¬\x0006ø
\x000bñÆ\x0000ä5×ý@ØÓ/nÅÕ%®þêw)qM#®7\x0006ãXdHq\x001f|ÄÝîiÅµ%®mÅu,Û\x0001Úó³â
@p{AZ+­+i]\x001b­TD\x0006ââ\x0002w)þ<5
ü^Ýg+®/qýW¿uC\x001b\x001aWW
,SM{ÁÒø]àÂ_p##vhóå"y\x0008Ñºº[@z\x0016RßóÀìõo´òö=Z«K\x000b_\x0006@)V\x001fÂùnÌ;2c¥·çÒd£OC9cO­§!ÐØ®Å²ön­¼=·&[ý\x001ah\x001déÖW\x0004ÖåW9×\x0000\x001aµ\x001fz~M¶:6u@]h>7!ã¬sâU{Ã@Zy{M¶z¶ày`ZÜ\x0004¼Q¦4¯ï¯ìy6ÙèÚpº9µýèfá¥ýË\x000fHÑü\x001e·ç,d£·2`+bÇ\x000bíYÜ\x0005¼\x001fìÞÒ	ÞÑ\x0008+á¹ìª^hÒýb/\x000c§$¢gxVLÄ¬£\x0018ö:¾Î®oi°ý¢EÃXWv5ÄÕi\x0010Z\x0002UüÞ\x000eFgÐ½¡6M ¦\x00045- Îät,­P\ÙÃg~_à£\x0005Ô ®\x00014îE\x0016èïg%UÈqõ\x0013{IÒ\x0016ÎPr&NIêy*`©z<÷÷ºýÙ\x0006NÙ?I-G	¦Ö]Ý\x0019iQ\x0019SÔíÉ;TÆC4¬Í®6÷Ý§íÇü(rýñåùéáPÚY\x0012\x00138è¤\x0013Ý®ûo¯\x0015ýÝåæÞE®Ïno®/\x000ecª\x0012Sµ`z\x001foP´(­Êíuë!¡¯\x0014Rú+4%¤©!bíYÔêÏ
ý"÷*î¹¢\x0006Ì~»Uwð\x0007_åöÛí:VüAýÊÆ» +Pc0M¯ §Ø½Xz\x001fvjèÆ°ØTïZã\x0017N¡³ÀÙ¢Ôý)\x0001v³EGËÝy\x0012õÌÒ°ÎTïZâ¡é,cXù	eÅp\x000cëhu1.Ñt\x001d§¾®g®sR:~x\x000fãí~Ñlf«Ð°µKK=uw*ã\x001f¹\x0017VôÈæ÷+±\\x0015\x0016¶Léü1CV¶Î%S{`é
+)tWIñîþåáåþ$\x0012\x001e\x00007\x001bîÛ&÷íZ3]Cñîüöâöü$òÍ=2\x000c\x0005¹käyÅ·%n\x000e}JÈ/\x000c!÷y°T]\x000cÉ'¾äÙ÷\x001b\x000ck\x000eÃ©\x0012NUÂåB½£IÒc.ÌÜ\x0017ª®e
jÙ,ÍÅ¢Lîru
ÇxÓýa¸\x000fØÎÑÏY \x0011)9\x0016\x0010\x0006Ã£Ä0\x0002Ü+ßä¤\x0012%W\x0010N{ý RÕÝ1âE8þëÞo\x001f\x001e_N6¯?¿~yyx_ANù\x0014\x001b£æÓî\x0012%%VUVì
"y¿¹¸º=ÙÜ}w÷þöâjNþø·WF|¦±kÛ¸Ú¾<<=n?ÝÈ.¥L\x0012Ùöáç\x0018ýG2ï]\x000ceç°t\x0008>I\x0001xsC;6©eÑ·¹ø.Fô©öòjs{q}µ¹<ïþ7Æ?q\x000f0MX­\x0006ô(-×Z#°[P'@«3`QÛ¿
0
Y­_A\x001bÈ¯jl¶ì
Ó½úï$N@>\x000e`Ütºe\x0005e dS·>±&Ã\x0017\x0001=\x000e`MË
ª@*ý\x0006\x0015\x0014°Q
W\x0010hôA\x0004ÔÇá¿¦máÃ"\x0010K|.eëâ\x0002
«¯¸	¯\x0002®Ñµ\x0000Jn î¶`§Å\x001e\x0017Pisì-\x0018ÿ5¾\x0005Ð\x0005Ò\x00102(gey\x0005I#Cê#­_4U¡\x0001ÏzIw5ZöóV8>!à;
 ¾'ísª\x000c7JÇ\x0005\x000c)_FFñ\x0019VG2Ó*-ÄÆû.ð'¶Id=®¡\x000cîÈV\x0006¯¢²Å8\x0013£\x0004:ÆxLKèD^ÂbÚì*ÀèEd'1Ñ\x00173`ÒVÅvÏàv\x001fù8|ÑÊ\x0016Gâ´¡$A·!\x001d<¢¦\x000b}\x0002\x0018¿lq$\x0006\x0001\x001d\x0001®Q\@	\x0019°hÌYE\x0018Íl±Ô&Z¿L(é\x001c\x001bO\x001c¸p\x001cÀh
d)Ñ>½T\x001a\x001c\ñ!\x00073Ç9ÄØ\x001a¦Z\x000c¡0µ\x0001Æ\x0005´©õ*\x0019»;ÅG
\x0007±\x0001\µ\x0018Â?ê\x0013ãaS-vÐjKó\x0010" K/%q	º\x0008â?äãKð\x0017U-P£|çsÖ\x000fÄÎÊ\x001cÇN£æ³j±\x00164\x0016·'<J[\x00105¤	Ð\x001féÄßSµØAm,]7»-Øé¿Ä%\x0014	å¾püEUKHm³\x0018$\x000cIÉ\x000f£\x0005É!µ:RH­¢V-ZÇx?r\x000cú³3.\x001f\x0012édgâ¿FµÄÔ1úË!a\BKÛPPÊ\x001eðHÛ0î\x0015ÕâK´èêxÙt#â\x0012²Þ\\Cs\x001dDO\x0002-Þ¤¸PÉ$èÔ¸°rà(ñ_\x0003-Þ$^=H³¯»ÚuEq
e¾Ø\x001dÇàÐVhq&&\x0006Õ\x0016\x0010ÒàÚ¸Êð9\x00068Ò'ÆìL/\x0001\x000b´	u×Üõ¯Â\x001fi	£¥\x0016k
NÒûµ\x000eñld"\x000cL\x0008áHQ+>	@µ6Ñ\x0016\x0006>&&¥Ã Ð±K\x0006}û1¶/BµþC"\x0006ì@\x0016[mT´3´~6ûcoÙ\x00109\x000e FP7\x0019B¹\x0003t\x00001Ý !\x0002´ÇqÇxÕ-v&\x001e
zWê\x0008é\x0013\x001b°Ç\x0006Ä$kKP¨½Éù\x000f/ïÑ~sÜoõq\x0002\x0006|
Õ-§XãènO±J·c/MÞú8¶\x001aQÝrL°ñ.IvÐ¦\x0004C´à-¡>%4ñs\x0002Ö\x0014Rå\x0012lµ±9Ëu\x001cÀ¸MË9ùã0î\x0015ÓrP°CèíOÙtcÈ1Íqv!>sò-!\x001f·]àºm0ØÑá	/ñ\x0014¸]ªÐ\x001dg#
è*þ\x0004®KeÊÐQf\x001d{;-§\x000c9Ô½j\x001dåe"qúFN¯ò}\x0014o{\x001e(tÎ{ãD:)\x0010¡n\x00025R o2â\x0002gÆ§ìRÈZ¬\x0001ýüéoý\x000b+\x0002=àÝ¸åÛ\x000fÛ/\x0007V\x00124Å\x000e0äel\x0016ÑÚïÝ\x0008J¹ÂÍÙæìb3U Ò\x0003L¯y_\x001bàU¯\x001f-VðöyûëýsGc\x0015ï_\x000e¼Ö\x001aGÕm\x0006¦ù±1X2VíyéÛÍ\x000fç7\x001d\x001fÎT<¿]\x0002ãká¢ãlPs/-\x001dê%6S¶\x0001¬`K/ñµl\x00108aòôD¦8acµ9
[z¯^7ÃÖZzà\x0007F4×9`nèRàÒ\x0003üWºãÒy­^9Öä1ÝÜFE+GúÁÒ
3\x000cüÛC2ËI £áT$\x0001áîTXÉÇBñ±h_?ûùõç_ÿRËû7O¯_þþzJyÅ(ë5ÝTAô\x0014ñÖI·bÔç\x0019`Eçðæúîý¿ÜÍ\x0000ýúø_ÿã\x0011ëÈPq¸ûôöõËÇíO@\x000b,E$/]ê¡\x001fÏØ\x0007±ôöîýÙæ4U\x0005U á³	\x0015HÊpO´Ö\x0000æ5Æ¥^\x0004±÷¨¹\x0004)|úé/ÿR^É7¯'ø?¾ýùþÀfBUÚL8¤#½£ÐlcÕÞ3ðæî\x0004ÿróÝùa\x001e]ÈÝ,\x0005\x0002¬\x0010£x=\x0018"î2Êò'ìÙ®%@¯1ÿ|(ËRAâåÓËCtçï\x001f\x000f}¸Ào½\x001au¦\x000cåõrQ\x000e°\x0017\x0001§²ÄËëÛèÍß_ÝR}n÷û`T.T\x000b\x0016#so\x0013\x0002ÊËÇsÇÖ\x0000´Z\x000bFU8µ`¶ÓÞ¾àÓ\x0014Ô\x0008æ$\x001b\x0004µ\x001f:ÖåòZ2ÍòÑÚ;Ë¹\x0013ÃÁ·
a/uR	Æ5#Õ`\x0016O`\x0007fU*LG0CAòn/íTIÆÅ\x0018µdqk¥WW±l¤#¤µ%Ý/Æ¨Üe\x001ao§\x001a/§ÕG\x0013Hì¯ó<\x0006èh*=ÏÞËÔ\x0012¶¯ÿþWUV)m\x001e?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;zs|y¶\x0010jBè&4iTq&\x0014Y÷4\x0002bÂyKÛE¨jBÕMè\x0003¯!\x0005&>'é©Óéù¬K\x0017®ùt7£ç)g¥µa¥~,ËÚLhjBÓKhe·bô÷´\x0011<\x0006ÏÁüÝ¤ÐÖ¶{
¦7.¬ÉØZÆ5.]t®¦sÝëÚ%´\x0003Á{ÕFñ>'fªå{\x0011}èû?1}à\\x0003?°¤!\x0007\x000b£ÆºðB\x0017ºñ£ÒÄô°ðpò\x000b\x000fÍ°õðÕùÉÝäÒO\x000cäDP1	G%ÆòziÃüÕ¯±õ%ÝÎ$ÞIù\x0019Ð¯ÐXlã\x000cÄ¿[\x0019\x001bo"»ÝágùÎÏh\x0015µ*Cï¶èÆÈno\x0012Ï2¬-\x001ekIÆÐ\x0007\x0005Û\x000fl\x001cìö(Ö\x0004­j°\x0010\x000fçr©ëO\x0017cãRd¿O	ñþC¹S\x0018\x0019­peå\x0000D/cãTd·W±ô¥²3íH~*\x001e\x0018Åë\x0008ó¢î]ÝýÛ\x000bm+Mã~4lxÄö3\x0003q~ã\x0018#0$Í¶uØ}ëù'\x000eF°Í:í_H\x0011¨?#F9S´Æb8
#6[GÓ~l3ðµ
\x000b\x0001òÒ8y£¹®#Z§íávh\x001f%Ð]ó}ªÔ\x001a\x001eåmÐdÒ7·e¶Ü|v\x001d¨|(Ê)5ß­Înïo¾`=ñ·w·7\x001foïïöpºh+\x0003\x000fêãA(Ñ\x0011îæ\x0012ÍÏ\x00188;¿|ù\x0016¿½8ùâüòb?.Ô¸0+å3¢d$3µ J(>?5{VÕ´j\x0016+h@¬Ö<=ËIk\x0001½Û\x000càê\x001aW\x000fâ*Áu±\x0016øYA[­wqúì¦\x001dÀµ5®\x001dÝºTP\x0010c¥Ý^p\x001cµ[;ïA\x0007h}Më8m\x0015ÊK]Bùn\\x0017Ê\x0000Ï"=©]\x0012÷Ë[w^t|·±\x000brÔ0üv¼ÍQ£g
Çù\x0010©Â.íà Ä³\x0017¦\x0001Þæ¬ÉÁÃæ¤wvÐPÊ¼Nq\x000bqócs\x0006xÓ&\x0007®\x000cwr®(ÌçM\x001cè¸AsÜ`ô¸\x0005®*Û×ÒÓiªR®UÝ°\x0013\x000fxH¼<¥îÛ«7_\x0011úäúÓõ¯W{ \x001dà$\x001dêè-\x0003\x0014)ÜôÎÏ\x0013ê¾=~ùâå;\x0004?9=;}ûîx\x0005¸lÀå\x0006p,Ücb´\x001b¤o\x0006\³\x00043O¯[È¡!Mä\x001d´Ü[ÚÖ\x0010#
\x001eZa§Ý\x0016[ÈUC®þ¯lº\x001d8§vàM»Ôðpt\x0010Í
t¥\x000c
f* Ðex\x0018ÖÝ\x0018Æ»ÏWw\x001fóÀÑ»_n®¿ìë\x0014L³É¤@\x0008¹á^Ëâ`æ\x001d^¼>¾x\x0007^¼zyúöÑAb\x0019Æ¥åÞ\x0002\x001cÓ%iÜ5&ær9üÒh®\x0011fU3«qf|u\x0004ZgÀÌÀï\x0017*Ì\x0008\x0006\x000c3ëYo`æ9\x0000\x001eHþ+2sòó#sÇ M
m¡µrdû"´À¾Í\x0004]2\x0014Ê\x001fr¥m
m7@ÛgV\x001a§\x000c9Ve6úá]Íì1IEy¿ø@\x000bqõef}Àö5´\x001f_è ©;B³«Ïwíø\x0016&ã@\x001a:lZizEQ i¥¡Ø»ù"Ñ!èúb\x0018ÊÅpÚr@IÉùLå8¿®å|\x0016fºuãþ0\x0006ÿ|#P ©ÞN+-\x0015·ZÍ(r\x000eS7\x000eQ{DmxÚ\x000bàäRçØ\x001fð$ÊÆ!ÊqTdaö@6¯t\x0004Ï×\x001cA7\x001eQ»D-J"\x0014µ³
Æd
·5ÎL3\x0018¦n\¢Üà\x0013e±zÊ\x001aN5dõô!íGã\x0012å¸OTØ1î¨e\£pw\x000eM\x0003CùbÎ1êÆ)Êq¯\x0018c"Î0©\x00183YÚ ¨'O\x001bäg±q0rÜÃ(c¹>Iò'\x0003ûr|<\x001854Û\x001aÆ·5Nf¦\x0011m|T¢ü*aÔá./\x0006\x001a\x0013b`CXí\x00052\x0001
ÊXÚ!|\x0018_\x001aÔØOmÛÓh7\x001cG\x001d\x0017»8FÁO¨ÊÒ¼0³s\x001a\x0018ÄÂx\x0010¢½àB\x0004°\x0013¨\x000bN]\x001aâ;B\x001dZêñã¨µ§ú\x000ee$:ö\x0004#\x0010É5.o\x001c VíZ«
k
¶8tëPÙ)ml\x000e÷ì|nr\x000cºÝÖj	\x0006ê@\x001a5ß\x0007´]8BÝn\x0010µe\x0000ÉÆGÏ"hV@Ü! \x000e÷²ºø¬Þ\x0012ò)®ÿRøÒ	-Ù9.Íý\x001d 6Í\x0000ÿ\x001c¦¶}\x0002Î> b&U²î\x001a\x000eç\x001c±Ý¯ÁÞ°GPg|º\x0014\È¦°î_ó\x0005©CØ®µ"n\x0015A!\x0016:ØÌÃÍÔjiýPV¡\x001d`ÝüÚþ\x001boQK\x0000;]Ò=ÝsÝ	Ó¯fÇ\x001a_s8\x000fÁÝ6pÇÏvà\x0015É<htþsHÒz\x0014\àRl"W\x001a{f³E\x0011\x001cLi	lQTXï*\x0017È{pÇ@Z¤¯¿\x001c}uÿõýíÍ\x0016äè\x001d\x0015éGÐÅÑø"Ü3ßPò-ß\x001f_¾;9ùX\x00132!B\x0008ýJðåV¨íúùF®é\x0016 í0D\x0017¤ª!ÕÀ:ZjZ\x0003QF|ÄôôÅ!\x0006½Û!u
©û!ñ1(\x0007Ë\x0002ÓùfÎ^I?oÅú M
i\x0006VÒÓì]@õ] ¬\x0000æî\x0000¶´\x0003+É½Õq%=½\x0008Æ\x0000\x0017ráÝ¤ÑÕnèÜÝyy>7ü¸¢MÛ!}
é\x0007 Ó½>Û\x001fOÃ\x0008ªQÎ<­öC\x001a2\x000c@JÎHÜV!c`>¯ÓÐ\x0003Ye¸ñ`\x0001J(§\x001bgk	
\¶)1Ç½²õ7\x0003\x000eGÅ`÷¬,©Ê ÙPº\x0003\x0018JÙ¸\x001c9âsLYË]\x0005,DÏ]Ìù\x0001¾xãsäÓQßçP2ILÖ\x0012§´m¦l\x001cð:¨GNfH§\x000b,!3tl|\x001cp:.Ýû\x0012¤(ÄJ¢¹·âì<\x001a¨ÉÆãÈ\x0011c¨\x0006Sb ÆÜH\x0005vAng=aãoäÃ)Ê\x001e(EÍQ/v¥³ª¦Ú\x001f¨=\x0008\x0001\x001bYFaÇpA\x0014Ü\x000bz¾r±k7B\x001bð\x000eXÈ¢ù\{®WT¢,äÜÌÅnÊæ\ÃÀ¹¶¬\x001e)\x0003õ^GÄ©5\x0008+>÷^ÊæØÀÀ±ñkUQÌq¾ÍZèßì£l¢ \x0018\x0008 \x001eXYôS5N­eÈù+z\x0017¤j\x000e\x001a8<¦¤nd\U\x001fø|si8À¶TÍáQ#G=\x0013²PRÑ\x0012¦|ðùïJJxØ¾\x0002¹}¥ð_Ýütýu\x000f£Ð©C\x0001\x0019=fzIT\x001fÑz`!üW/¿»<}·\x0010jBè&Äf¥|lââDB/<­¢läÍZDU#ª\x0011Ä<\x0016üN=Íªù gÇ{\x0011Mhú\x0011y\x00161øHk²\x0004\x001c{?\x0007êEt5¢ëF´åPG[m\x0019ûûb\x0008¹<i-¢¯\x0011}/¢»A\x00076P¡ò'\x001dX5éîE\x000c5bè_EùÉ´1(w´À/Õ8:w#¡lMN¿Íq£³¸¢T6eTèçT¨z\x0019\x0013-û4Æ¸ù¼¸ài°|dtWñz»aÍýgÚyÎí:N_½ÒÛ¿us¦eÿ¡öÀòöÎ9Rý¿õ#3»×"6\x0007Fö\x00180­·³|wU¾ä"ã\x001e]\x001e'¿\x0011#\x0003ýG¦fÔ,ÀÚ0n>2Ð\x001c\x0019è?2Aò«CY2O\x0015T]\x001eª³±92ÐdòÜÄ\x00082SÊ[ÇBC(V¶±92Ðd²½É\x0006/Ñ3â\x0001±92Ð}dânã4¤µªD?Xôf^Nû\x0010eöT÷Ç¨¢Ó\x0014^\x0014VoùíçR¥\x000f GgÁ·Ñõ§û£7Ww\x001fõÓÿçþåúÃÏû^êðE,¢.gå<°¤ljÉó\x000cË£7Ç\x0017Ï\x0011üìèô\x000f§ñ\x001f?v»y\x0018\x001b]O}\x001aA×
\x0000\x0014^\x001aéä;¼u\x0013úÔYnA×5ºÞnéº\x001b£\x000fMïP\x0018¹Ó¢\x0003L]è\x0016r[Ûmäq¥EX
FXT\x0005îa3SÑ-è¾F÷Ð¥Tt_Rà¹É \x001eÍÀSLgÆ&l@¯ß3t3Nh\x001dsÈY\x001dQ¡ YÞ1\x0001MA\x001eo)¦\x001ed]>|UÍ«úw×¯÷ÉzÇø@àü°T\x0000ª=MaÕqóð+µüÄñÝéëÓG½åÃ7uÙ¼©¯\x0003Ì*W\x0019ÐàÄØ\X¡Kêbd-ªùT/\x0000Juk¼ïQ6WÏÌ\x000böÐéNw¯à¼'f¼©&pmQË5\x0013kùLÍgºWOó\x0003ºö;\x0018TQk0vùUh- ­\x0001m÷ùP\¹¦½b½µx[æ\x0015´\x000b#!:\x0000]
è\x0006\x000e°áéuE\x0013cTÀ
íó¢Û=|¾æóÝ|3_Fz¼1SE\x0017Ï\x0000\x000ca1\x0011»\x00160Ô¡\x001bÐ\x0014\x00113c¸Û±¤³­Z~«ZÉW÷µ¯å+Ï°æ$±ICI©²Ôrx/ \x000fT¹\x0013½ýáq6\x0017ïE¬i\x000bø,ã:c\x0003wl/èm]>ßej,Ó\x0005Ôî§\x0000GæYÂ\x0002n_h\x0010X\x000bfk0Û\x0003\x0005Ò\x0014Mz BXe\x001cOÑ\x00007¿ÛÖ¹\x001aÌu®\x0018«\x0006ð0v\0ævÛ\x0015j¬Ðu~9rª4G[+13)|=W\x001döÉJsÕ,q9M\x001f²h\x0015øÌZ\x0007Y{"û¤áÐ9ÞX¨h%®ö%üÜ´fª!SÆTÖã.ã$%4÷Ýl9²9²ïXJ\x001eo§°¤Bñ×T¼ýTU×5û_v\x001d\x0000ôÕ\x0013Y/=\x0000Ïr\x001eÊ,É®"æ\x0004@ß	0Ï\x0008\x000c<M£Lñ·\R^ÇÕìèÙÿ!n­yRÑIR9²§Ì+·ÅöÛúù\x001c
¹ïZ2G;ñ\x0000Pq\³Àdr¾Òz/{jrº\x001a>ùüîêýõÝþ2pÉ¯B:«Dµàç?#\x0016Gd=¿8>9½xì¦ê\x001e&®\x0006P®\x0004\x0004Ã-ü\x001a'£æHÃp©6Ó©NuÒi_R²XËZÊ5ËÉyÙ®\x001e@]\x0003êN@TOQ4\x0019'\x001fSýd¾Æ¡\x001e>SóÞ\x0005Ä=ºHkÅÀTG¤øª*7\x0003Ú\x001aÐö. M-y\x0001-_dd)Y5z>Fê\x0001t5 ë]A\x000cÜtIå\x0008\x0018a\x001eÏtðùÏ÷. \x000eô¤ Øg@Ýèk¼­ï¦ê\x0001\x000c5`\x0018øÂ¤{ÍÐ9¦Ó)«N_x¡üj= lmt¯V&°,/\x0012\x0006Çª\x0010nµ2²1²×\x000eÆ` \x0012Ço*Z\x0012¶x]º°±3²×Ð(©hØ"èzL\x0012a\x0005\x0016gH:	s,{\x000f²\x0012ÑénT¢Hmo>ÉÐø\x0012èv&ÿóG\x00195§·Øà\ûcÛ»\x0011Ü¦\x0019ð3\x0018<O$7Rlô'¦
¸ðÏÞK\x0014Á\x0002¯¹½In¶\x0018Ñî37Ëï£¨[Äî\x0018/E\x001c6àÌ\x001c6p%lï,îYÅ6®\x0011Ýg¦¸e&Ü÷~ÑÁg[¾ÞÀ\x0006Û*ÍN\x0003ÄÜ[Q!3z^§\x0007ÑµÝ§9\x001aj 5ÄQm\x0014Ú\x0014I)³ tÔè[ÄþèF=\x000b\x0014_kV\x0003l7Üè@íÝ\x001fZóx%mÊ\x0004\x0007÷
ÚóÊØ=íwîö|xurü\åJóçêI£\x0016z\x0015×#ö;îï¬5¥bSZ>ÓÀw
pæ\x001b½;\x0010]û]÷M%zçòäRÔð¥.¢>a>g´\x001eÑVS¼JUsÖ×·¢|%@ E\x0017¶ëºÎ7mòéJ_¼^¹\x001fà5
\x0006ÂÇ[=k\x00189/´S<\x001cÜ'Òà>Ï=¹½ÿtõy_
Ò\x0008\x0015ÈÔ{V\x00127MÎ\Êéä\x0003ÖÌ=9¿<;~ýX¡x8¹O¤É}*MÔ´49\\x0017­Y.[òÓEìFT5¢êFô\x000e»mÒ*Zjâ\x0016vìðj>]óén>\x001c\x0014C|8)\x0010è¨\x0008i3 ©\x0001ÍÓ[@[óÙ'¸¾\x0006ôO\x00100ÔáÉ}áÊ¥<\x0019ï©­ lì ì7ÿsK¨\x001f\x001aj]F¬\x001eúõçÛÏ\x0011òíõç¯×7÷ÞùÕÌ­uT¸\x001b¯¥,ob3\x001eïøìÍ÷ç¯#ëÛÓ×ïN_¾ÞÏjjV3Æ\x001aoV$ºc«â\x001c"Ü|ª©\x001fÕÕ¨n\x0008Õ
z-\x0003ã ¤\x000eÜä`f#ï~ÒP±EÕ
Úp\x0008\x0018¥v´ä«V<O³\x0017ênÖê¼ëÝ$Ì^X\x0015hX}¼\x000cÚò($Ëõ~R?¬l`å\x0018¬)-\x001a\x0016c"zb+9)· »ÓOÛØ\x00019h\x0008ødÅu%Í\x0018ËÓgó\x0012\x0003ý¤º!ÕO{\x00134&KÙ¬ßÆ\x0010T©\x0002½HÙ*¸Ã-ÞÇX~\\x0017(+æ¥?ûi\x001b\x0003+²­&éÝ\x0018Í§ºa\x001bw Çü\x0015e4|z£%\x0010B©\x0010?\x000c,4þ\x0000¶?ÆnÁÓ¶[Ð\x001c/\x0018;^øÎCO\x0001»W3¤ÄçEý'°\x000b)laüz}÷ÀÊâ?\x0019Ú·Õ\x0002ñ\x001dÃkÞ·å\x0001h6	¶zuß\x000bJóV8ÿà\x001büó³ëû£\x00177_ÞÜ]}åÞã÷×_þ|¿'ãd\x0014NÌÊ2^hÒ%FÒá%¦zrg/O/pöÑãw¹säøäôíï/sO\x0005Ý´èf\x000bºÒaÙ\x0010.xÐê\x000f*¡¹\x0000Ó×¢Gà^\x0008^\x0006\x001eÿÜ²îÞ\x000bºJ(lÊ
G^ÐõLiú~|åµ\x000f
<úÑ-ðAñ°2\x0019w}¾úJ¬¦ÌìNO\x000cÉ\x0006v\x0006!öøç\x0016ö <õ/¨¤üÑ\x001d7\x0006
?u/[Ø]Ëî¶­»\x0014ôø¨d$\x001e«¤"H©§¥\x0004ãð¦\x001e&xüs\x000b<¶+\x0019jÉt$IEE\x000c\x000fSI¤
ðº×à£m/\x001a\x0016!H*iO¶5nZ\x000f8nk\x000e-ü¦ãj%Î¡Ï«àlÜ¿\x001dÌ´\x000et\x0003¼iÎ+þ¹	\x001e$»Õ`\x001cõ§\x0004\x0011Áë©ØÎ8<ÎªàÓh©MÒ=/$ÉI³\x001c³µ±ÓÚø=\x001f
ÍÃÖLÝ´f¾¾}ÿézOß\x000bÞRã1\x001a\x0017ê}È3­sËô²nëëó³ÓÇú~ôÃÎLÝtf®ãÃñÊ\x0000C\x0001Òd#\x0016Ñ:\x0000U
¨z\x0001£Y+ýòÀ
-\x000euÚx\x0005\x0017\x0005ôÖ\x0002ê\x001aP÷\x0002Úx¢n \x0001Ü=e&f^AXlíZ\x000bhj@Ó
¨I7)\x000ePÛ¾ÅÉ´zó'¶5 í\x00064$\x001eV0KYÇ\x0015\x0014öp+èj@×\x000be¼ã
"|°y\x0001}Íç»ù\x001cõ}AôJ¤Kf½äWeÁÁxu·m~\ÇsÍø\x0003;Ö¼°¥gè1qÛµ\x0015Ýf\x0010oñ4)XrMQY\x0010Ïl¬ì63Ê±\x001dDB²v×¥)¦÷îMØT[¤Xª-À^T\x000f;dTÝ!óævßÛó-k\x000c¢¾%Ë\x0018ËÑ²Xj\x0013¾<zsþèÓzØ\x001b£êÞ5hÈCWWp¬7a$0^,Æ]¦j4Õ\x0016hÕp¨,0å[õb½ú:4]£é.4ehjQü \x0006é¨$@\x001ft±Ôl\x001d©ÑL\x001f'MøA

:V&©¶å\x000f:k[fk4Ûw\x000c\x000c©ý*sÆ©íÕJj.îvÛª¹\x001aÍu¡i[288v:\x0012Mí\x0017\x0014~×,<!Û=fõVÓÖ#\x0008V<¢¦´\x000bK§y³Í?ò¬·\x001egP\x000fêðV\x0011:Ö\x0012Êàp$ä&ðhD¶Þð0ô\x0012â¥P\x000e,	Ð\x001a-e9°ó\x000ev-¡üñªõ\W_Xï¾0/-Öd±oíQ¸÷9g¯ Ê«oðÏoÞ\ÿýîúèâöþ§=\x0017òÔßO®ZiV²3eÞ\x0011Óä7§ÿ~qztq~ùÝ£Y§\x000cgZ8Ó\x0005J½ôæa
«ZÁÒ ZO\x0013Ú]p¶³]pp¤IYñöM\x0012\x0017\x0016,KGÏÌSès-ë\x0013<\x0012\x0010\x001c÷JF8³\x001b\x001a9Ú»à|\x000bç»àâL±b½xÆ\x001dõg<LÇ\x0015v¡\x0016-ô \x0005,\£	WØPL;ÎxzBÙDV4Õ3\x0019ªwù¤½ei2#íAÍCy\x0001¦åk\x001dpÚ©\x001a\x000eÿì²"¾\x000csÀK6\x001fT\x001eïQàt\x000b×gâ\À»L¶"ú"6\x001e\x0011¥§EjëÑL4ß5Zúûé|Õ¸û+×Z\x000e\x0004þ£\x000eFí¸jj³U®´­`Ò6+\k±ÃW½&ÿ\x0005Ï!qc·Ù:÷Ïõñ9¾M@\x0000ØÅZÉ*§JN»AÖðáÔK5Ê\x0006íb3Ê\x000fW\x001fþ|¿÷êoUyÁ´(	OIRCJA1S%)®Mÿðèãç¿¿|4\x0007@¸PãÂ\x0018®+aÑ8\x000bÎJÅ»#\x0005Í&L_p\x0006qU«\x0006q!Õ5\x0001ë\x000b\x0012®÷´º)¤9\x000c®®qõ nòó\x0013²ÑblÎURZH¸3'~\x0010×Ö¸vpïâÌk¼¦\x0006Ï\x0018Xº\x0013\x001b5U¸\x001bÄõ5®\x001fÄ5t{p@\x0001)«Æ\x0010\x0016×`v\x0010ÚZ]\x000bþ.\+XMÕ8KÜ¨ÒÄ;Mn
â6A\x000eZ\x0006\]zÒ1\x0018Ðêz6\x000cÚ/¶!tâ6'M\x000e\x001e5ë\x000c]q\x0014Öùeß «/\x0015\x0007:i²9irô¨~¼èÀ¸L)ÍõQÆ\x001d×ªf7àcÀ^±L\ô¸üFª\x0014o\x0007;Uj\x001f4
²Ib$Oÿ`Ô\x0019â=Y\x0008¬¨ _<½!õB»ºNÖïãïînïß_}¼½¿ÛÇ*c\x0004+I¹Í8\x001a{\x0010Y¹n+^ù\x0017\x0005dßÅ\x0000çäøÅùåÅ
T¨Qa\x0004\x0015û3%i\x0019\x0002
\x0013·càÇ^ R[Ú±EõÜ±©ÌF,®©fÕÅ\x0005²nRWº¡5Å­JO[NQ·\x0012¸\x0000¬\x0013¾ôÀÐêkT?j%)ã(tfÁßK, ëA­\x001c\x0003\x001e*=Ä\x001aÔåÝ?çÒ#+«[JÔ¬;\x0004k³¬rl]qú\x0017IÐJ\x001e\x0007^²\x0012!e\x0005ä.ÖÐ°!VPø>g\x001b¹\pë)æ\x0014ùGX¡Ù\x00030´\x0007d0\û¡PXÚfV­w°/ï]¬¦a5C¬:°÷\x0004>[Ö»¢yz\x0010\x0005i1Û\x0012^ä\x0006$\x0015\x000e.Â§È6\x0015L«4¥"\x001a×lõ¾hïN\x0005X\x001b\x001b\x0000C6@¦\x0011ç¤©\x0012«qEïù\x0010ßßæXY1f[q\x000bw\x0001ól3ð\x0018adÖ%
·NXh+\x000bCá\x0015:\x0002Ø\x0015\x0019ö\x0003¶øCØ+ÛîW;¶a\x0001óú$É¬\x0004Å­\x00112X±z\x0008X¥\x001aX¥Æ<æ\x0010\x000b\x001cPÂ\x000bçÒqÐYYÝnY=¶eA
7Ä;­uäµv*ïËEl]¬mäªì+öþS®\x000b°è\¬5¼\x000bì´fìBÐ´*¥K\x0001w*õ\x0012\x0007z\x0003Ä\x001eËâòj6^\x000bð\x0003Ä"\x000e\x0012×5Z=¡A\x0011QXÖCk¬
\x0014ñÄÂ<¸\x001fâÌ½Ýv8¹½ÿËÝõýÍ§}³\x0013åûA\x001aÏKß4$cKBC¤'ç¸8½|y¶\x0002\x0014jPxÂ ª\x0006UO\x0018T× z\x0000TÇè\x0014ä²\x0011
;}Åà\x0007 \x000býDijJ3B©%Å%JÃjý:Z.ZÎè\x000b\x0017Cå´5¨}ÂßÝÕ î	ú\x001aÔ\x000f}zÏ³.ª¼Z[Zé\x0005
5h\x0018YÑ\x0018ùÑdh«t\x0011VÀ²\x0015kÖóÑsTkÿ¦Hü©}vÙº¤!\x0014ã½@2 xo5¬\x0004Ä\x0002+\x000b%=ëÙø#9âPcÚþm\ZRmÿÅJ`Aç°\x0007³ñFrÈ\x001d¡Ñ¤Å´*Ò¡S÷&j\x0012Ö¦Ó\x000eù¢\x0018\x0016):éRTÑÈ³l·\x000b:ºk÷¦}N·9Ç¡b{Üç¯7\x001f~¾ÚÓ3oqr0]÷S\x001cØA:ê¹?næn'¢\x001e\x001d¿~÷òù÷ÇÉ\x0011Ø©tSé½Øï,©ó\x000cÕ)òu_y°(P¡x3¦ª1Õ]MSc\x0001Ìhz¸)\x0012'âæÕ^È]ûø\x0001VÓÕn\x0000SÅë}nù\x0012û®\x0011s×n(ìôiµ\x001f3Ôa\x0000\x0013/:ÐÞÌ½ñÖ]rq¢ðzFÙ\x001eósþ\x001b@6§G\x001cx¹¯%ÞI.KjQªªÃ^q7gs|äÈùù
\x0016³9<räôü\x0006ÍÑOîìøFÝ×åTÇÿåúî&
ú}sýSté{iÑò°r\x0005xC3ó\x0000ûP8Ó4\x001dÌÈïäÇÿþêôâe\x001aôûæô»èÝWÁë\x001a^oÇpt±³×ñkä#9½mð¦7\x001báín:´Á\x0019×	^qµ Øé4ñmð¶·Ûà\x0015pu\x001b8Ö8\x0007\x0017\x0004'(ÍAw­£ÂÈ.ä6z\x0013v\x0003,\x0015Õæá@ypÊCnÂ×¢Á×âÿÔÎqÎ×øøçÖSëÍÌ©õ\x0007?µòáB¦+ÅOW\x001f®Ë8ô>Ý|Ù[¿í|éÇ\x0006_KõÛ\÷ íLýöÙñóSþÝÙË·NAx©éR1\x0000êËÐX|¤õTh.Ëc6r\x000fª\x001aT:TäL \x0016p?gPÏÕ\x0019I&e3¨®Aõ\x0010h\\x0015x\x0014c´\x000f§%/\x0003 ¦\x00065c F,GP\x0016ÐRø¢È ê\x0010{ÔÖ v\x000c4iïYÒÒgI\x0013U\x0014§üÔ~
º\x001aÔ\x0006n¯N\x000fÇ$\x000eí\x001f¬{1mÉé\x0007
5hxº õ\x0008ð<iøÉ¶\x0016Ääûh;øª.½ÅçØLZL¾iì'mL¾\x001c³ùÿÃkªÄ\x0003/ª\x0004¿c¾¾ýzwý»\x0017W¿ìo0r¬2EcÜ\x0014(v/Ú³ïX¯Ïß]DÌãW+ø æn>É²\x001dVîö]IÛüdÖ\x001e<Uã©N¼\x0003)â\x0003\x0014/ÈíOe@ÊR\/®ùt/\g%X½ã\x0000_×Ôx¦\x001bÏÝçS#~Æc\x000c,TØ
hk@Û
\x0018ð\x0012×/PH¯,'YÁÍËÆôðùÏ÷ò)UêS£1$<\x001dLY¿Í|mí21\Ø±þ\x0014{QPTä3|±2f¾¦c\x0015§\x0008\x000fÌ Þ\x001bw#£n?Ýþòþ&UÓ<(ùK£¡¸×\x0004\x000e'\x0005Àâè­ó³óW'ø\x000föBB
	ýÖ¸c\x00148­5Ab©èü\x0016\x0007\x0012®T5¤ê&Åo"¤`Â#\x000e\x0003©kH=ð¹5OÔKñ95ê^ª\x0018\x0000,N\\x000fijHÓ
æÑg\Ô<Ö%ZÝJN\x0003ò~H[CÚ~H!d§çÎ\x0003l bý\x0019±<²n=£«\x0019]?£â»bT4qBYÃ5eq;\x001dàkû\x001aÒ÷C\x001aIÝ}\x0010Là~yëùí>\x001fàÜ\x001a2\x000c@¢Ðê$\x001bëBkØ¾uÁFø¦\x001eÿ·\x00162\x001enEç&ò.¢\x0003\x001e3\x0013Ü´3®²u8ý\x001e'`®\x001c®Ì\x0014²>\x001d¿Ý\x000eÇÇÿ\x0006®\x0008Ö²JCbúÜ\x000b=\x0005]Ãý\x001e'øPVÒî.ZÀ³\x000e_è&è¢l¹ì¶æéâjÉå8 æ\x000cå´áó\x001d§	w\x0018¡&\K¨L¹vEQ<6\x0017<\x0005\x001d°Ð çU¹ö%Ì¨¾w°:x`â\x001d¥\x001a\x001awúåÃ§«»_n?Ü\x0017X÷Øè\x0002K`7\x000e8¡(x.æ¬Oß>?;¾xuþúÅ£\x0003?\x001f¶»¶Ý|=k8½\x0006`©]7^{,_vä´hU6¬r55æå¾7ÿL\x0012j(moÓèh\x0008\x0015\x001aT\x0018Û\x0002\x0015Ü°<?ßÁÁ\x001bS²,Óc5Äª\x001aV5Äj5wÄàq7à\x0015+\x001cJì-ÝÎju³®øç\x0013Ü¯ïã¿n\x0013à3\x000c@ß~ùkàßÞ¸ÿº¯\x0000.ÞÑi*s¶Xü*à|t\x0005T\x000173)áùùÛw¹\x0006îùùåóËwË\x0005p\x0005ÓÕn\x0000SQè&W\x000bõ¼aÅ7k¦ª\x001b\x0013Ãz5õ\x0008¨á·\x0008*¸¸\x001dµÊzNÂ§\x001ePÛjåàÍ\x0010\x0013¬·¿¢:¹ºÿu\x000fa\x001aÂ¢P\x0019´Å×TÝ¬=¹RáÕ4\x0007|þú\x001dú§ãË7ûà\x000b5\x001cþÙ§é\x001d[â°\x001a.¾.\x0003î¾c¯Ä¨Ù«òãnGçWww×G/n÷\x000f*ðN(\x0012½J¥Y\x000bYïî¾RLeO\x001f_`&æ|Ï\§¥«ñðÏ\x001e<ÌYÊI\x000c\x0011PB,\x0013S\x0004/§Ýk
ÞÕÓÒ·x¾\x0013OñK®ÀÃª¼áv`a§9·.<Ý®î]=UjãÍ>n¶2$Ø<Éùöà\x0012^$<ü³\x000fO ÌNÂ3@k8\x0000ó.ÓfÚ.:\x000eçòöÐÅýFá¤p,½\x0015é$\x001féKm\x0017]h>-þÙ½v¡¬\x001d
!kÇEl~ÚÎÓgmcVðÏ
x\x001a¦x\x0013£Ü\x0017Í\%VGvïê	}^\x0004|ÿ\x0010ðý0}¨«òð±°â|ýáëí]ª¥<ÿòå~OPÀ+òdA£,ÕJ\x001b\x0004skÑôÎwÃïO¿;¿8zqtþöíåcÕAêaÑ*¢8O\x0014U×¨ú	£ÚJe"m4;\x0002ë1?IÃ%±»
'aÄªæåÐ;YU³¬øç\x0010«3ÏtY×¬P©C y]ç3\x0019+Yßçz\x0001é+¯b3ñhÜÞ}L\x0005\x0003'Wû"nTsSÔóì=uIh]î°Ê«ÉÕàäüâEª\x001489~,ØVØg¤+ÁeÙA
W\x0018Ï^\¼ÝW\x0017r+¡F­\x0008à:\x000e\x0017CÒoná^a4{qúâüÑ"ÆW«Ê_C#Þv|÷ùêþ#®àóÛ_~¹ùüÓ^q1@b}¹²RÑ´)Ï¡3\x0013.K\x0005ãÅëãË\x0017¸ÏÏ_½zùú»G%Æ\x0008Ý5èîÿ\x000e:¨P£ãØÝ3É³°¢e\x0000V\x001fcÇ:\x0015©}}ézAìV4ìøçÆuÏòÎíºëÿu·J6ìJncW¬¢ª_ª½M\x0019ÿ´,\x0014;¶gÜ2íZ\x0008pà_!F<³wÌsÜ:å_a:3oð_á¡¬M\x0012²ÔFr}æð_ÿüé~ÏÀ\x0003+vÒø\x001e\x001fìÊpHÊâxm§¾/w\x001e¡Y<ýî²{ðÏ×|þÉñÉfýäZ@û ÀÅê\x001c1$£ëÏ·7_Î®ÞßíÏä·\x000fk\x0014'¬4§ï\x00181dyÊÓ×ç/ß\x001d\x001d\<\x0016\x0013-Ô´ð´i­S5mJs\x000cñÚÀc¨Á83	\x0012²à0kæg;cX&R6´JõoðÏ\x0018Ý|Áý¹N>]}þóýÕ¾1'8<_ÌP>tØñ±1gUä\±ùÉùË·¸g	ûìøõï/G\EãÔìc´VP$ýÃÍOw\x0015¨¹þðóþZY[J
\ Ì8Iðç7æiQS\x0019Iúß½æRÔ?>ÿ~yµ\x000bº®Ñõ\x0016t\x0017áá-!+\x0002åâÙR³<Åv\x0000ÜÖàv\x001b¸W,o³¿<7P8®ÑRÓ\x0006-è¾F÷\x001bÑ¡$çd©@qµÑã=äÛ¥<ª&t)¶±§ö	\x001dE½©v¦»é¬-äÍ\x0019\x000eéoK.l¥,F»\x001dÿÁÆ]\x0013(i%=>|Ð/»fZÄ;ðoØ\x001fÔÝØJ$åèÓÕÑó«û/_®ö¾lF\x000fÄÊh](S©+@5%3¢Û9z~|ùöíñê\x0019ÿÃCRÕª\x0011R'ÊÍ*ªÀ\x0005ê@¤RýØ\x0016*FÌºËéìêËÑé¯W?î°\x0019?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=J-o¡±¨%}V@\x001b¼5ä RzÍÏ\x000cÊ\x000f·Íö¶BcHý0\x000eÇkv@;Í\x001dÁFÀÆÍÑ:ãP×ò|Qc-²ýxs}Äx>\x001aL´\x0005kúäüës ªØÅR8÷ é\x0018\x0014ºi\x0017k¬Ú¦kh\x000b&õÉÉóNà¯Mmå_üG÷+&ôñ¦¢G­·?o®¿n*îå.hKÅ\x0012\x0007ÍyzØ
Ebe_Ñ¶àòñßÏ\x001fO]Ì·h£ì4\>,\x0003Ê>ärÀ\x0018raËVS¦{@úô`z\x001cRåj\x001c>ígJaiÒvû;j)½øt¾I\x000f(\x0015¶'Ö7?Þ|¿º½­\x0019.Ïù9Ø»KBµ\x00124í\Z\x0015få\x0014Ruóãã}ñúõTãõ\x0017{»q>ÆtKÃrì£×¯u5Á
®>T\x0013ì1)Eð,*Wç^ÎÏx³µØ¯^\x001f?©\x0004Þ²Ä\x001aºY
,l>Np?\x0012(Y")\x00148Í¬ÆìÝ\x0003õ¬ûóûÆ\x000fÚ4F[àYÝ\x0006°(iæ¨¾Ä\x000b â	À¨~¹üû?ùõ\x0007¹×¡RE¬ÞÈÚ¾\x0003õ\x0012"åþ¹(=¹_ ÒA\x0014â\x0017¼¬¶­PµæP°/c'¥\x0007ÃgT«¨\x0004õE\x0017%L¿gv`&uÛ]ãTË\x0019\x0005Ïç;° y=1\x0004\x001a]¯¬Ø_ÁÕÃõ%'\x0008\x000e¸àõeð¹nG
\x0002ë¹óòüxjâDR5\x001e>ºº»þtôüüîcM²!ð[\x000bögÕ$àç]©÷inQ\x001f½xsöäèùÉ`\x0002¾v¦\x001b6\x0008ÍÊ¬\x0006Âk\x0019( 1\X\x0012LÓ"ì×óøåý»wÀ»ÔP¤\x0006uÓ>_þv]¥ÏS(±(¡LwÒû¢[©Ý?\x0002b\x0010åÁ>}y6­Ð*¿É?\x0004¾¶y9äã°Gÿåæ²¢\x001a\x000eû1e~Sÿ\x001amT%\x0004©é(ëfßÞ\x001c½<~º\x0000'UÒ`V24Ó¥I¤ÙxÚ`XÐK¦û}{\x000bifl_:\x0003§%ä3\x0005&-ØÇÙTb%Kt®N\x0007:Ö
gæ@G"Æ@7[ç8G÷Ñ\Ô\x0006m\x000fï¤Ï6 ~¹¹Þ|¸¨É\x001fÂ]µµq¾GÌébëHµ\x000b-ÓØÔËã³ãN§b¡&g¥O\x0017¦Ñ\x000f\x0004ÙG¬\x0019ÎN\x001a\x00007ó\x001e¼\x001e\x0013]BútaZK9c\x000bdn¬@¥
¦´zïQ©¦|wþùÓmª<Àf¾ñ¸Î¿ß]×\x0005Á\x0018üÅÁç/ªkÆXòá	\x001f¼Q<;ys6\x0013\x00053¬4&Iþ'º´Ðz|?ÏlVgû¨é×Çz¹ÀEÚK÷Ç\x0012{û$·:+ÿó\x001fÿu²¹«z^T§eÐ³+z^
<:úýç~tÏÌ2+Gð]bÖ¸­Òg
5*îp\x0006\x0007k)¨ÎYÆ2¥|Q¬zóEÉ;ÌªNfu7¼ûÛæò²&\x000c
RSOW27ln§KÓþç¸Qx÷·ã§O§Â»B\x0004aó·ÔÉ\x0008\x0017ø\x0004
ñH.Z@WOªÎÚ°\x001b\x0007õ~øSbhÏ¥\x000fÝ>µ¼£¿oÞ]Õ(\x0004Y)X{\x00036¬â*Í óK~\x001bÁ®ØÛÑß\x001f½T\x0007*Ähq\x001e¦O71 ÙTÌuãÖ\x0017Rð\x001fOÔôõ!Ë$
¿ýÌ\x000e\x001b bfÆvûüX"CÞ\x0013À\x001cë4õæÿøGøË,°Ö\x000fÿ\x0018·Û¿ÜÜ^Ý]Tmb¬x§;4ÒÑqS!\x001aî\x0000h
\x001d÷Û¿<~ýâÍéôV.Ä\x00013qéÓ,±\x0015ÂSKMà)Å\x001bù	WL\\x0000ÛíÇ?n.2©KI¿4ÂVÉ¼¦^Ì\ê°+\x000bÒF¸°:Òæ\x0012ûÿ
3Ò\x0008:-ôÊ¨p\x0015J\x0003ÝM7«\x0001\x000fg¹z¢¦±âNýóêê91þ !í_x8ìzµ¹øzû¡üÍ_ÿgSuâ ÀrßtQ<) Ô\x0010¿ îWä(¯V¯O¿N"8áÏ¦ú
\x000bº\x001a¢«uè"Ç_ØÒyÖU¿ÑÝü#+º\x001e¢ëuè^P¥\x0002ÏBu®Á@THèrai#º\x0019¢uè{ÿ\x0014ædX$Ç°æ¸sô¢Û!º]\x001e4Í\x0008V\x0010\x001dã¿E\x0016s¡\x0002\x001bÔOjZõSêän\x00159¶5äë¼Q´:¼æX-}@p?\x0004÷ëÀ¥$aE\x0005>·Ýag\x0010ämß/\x0001ÕI\x001eäa\x001dyÑ\x0007à©ø%ØR£öË$wÇ!x\\x00072fTWdyÊt0\x001aÇXÐx@¥\x00189#±rÑ#K\x0019´Ù\x001bYIÅõ°ê\x0007Ü-rìF×ùÑgZ)IÛ²¿
G\x001e\x0010}äFå:?\x001a¼§QÕ
ëBr<\x0018pv-¡Y¡ßVô\x001bëüh\x0014ê\x0001-º×ep×|\x0007r\x001bøÈÊu^\x0014õ[³Ì¯Òa»]Ê\x0018\x000fI>ò¡r\x0013°Ñ³\x000fÅÑ­$9ç4Oã\x000bm\x001aÉG>T®s¢x\x000b\x0016Ù¸h§¹\x000bÏ\x0006ÅIñDN'úÈÊun4B|åJ º5lÓ¥z-\x0019íBÓr\x001búÈÊu~\x0014ç\x001f±uÁIud]¢/\x001bf¡9³
}äHå:O\x001ac¤\x0006\x0001¥"\x000fP\x000e.$ò6]\x001c©ZçH£,½©\x0015g~hrºFÏ÷ÑµE\x0000jäGÕ*?jE\x0019N¡sO	iæjb\x000fq¡\x0018µmÍÇ×Ñu~4\x0006¶<m\x0017É
ÇÃv\x001feÝºì#¤Öù#ÜêYpB)oóËGj¡\x000e¼ì\x000bmì#¤Vy$S8²A\x0005/Ë­·O©Ø_\x0012Ö¹cF\x001eI­òH\x0016Ñ+- HmáìKáO\x000fèÔÈ!©U\x000e	îÊ4¾°å.cà¹a¡Ö¹|äÔ*\x0004k\x001e±6'kÇ÷:¯¸\x0010b\x0003¢ëQ×«º\x001586l#\x000erôTUF/&à\x0016d6ÚÐGf]¯3ëÒ\x0004.H@yÔÜµ\x0018\x0002g0¤\x000bòVmè#³®Wu+¬¢Ga\x00054q\x0019\x001b8xÕÚ#ÚÐGV]¯²êV8\x001e©$ê\x001fQâS*æ'6,£^g\x0019e\x0011\x0005UR:Î2\x0006¬îÍûÅ¦´ô\x0002úÈÀèu\x0006F¢6;
¥åRBWêuhºÛ-¸R3²0fA¹!²0ÂxÖç\x000eê^`\x0013µ½\x0006Ì/»\x0019\x001dS³î¢BHÖXQ¨f"5Y\x0018*\x0013.ÌO­lD\x001fe1Ìª,5ÚSû>\x0011>p4ÓÝ±KÒÒ\x001fÐ%ñcÀ:\x000bªda\x0004¾ÓQ\x001c )Zwö\x001eÉ,Yia¤¢T#Ü,5º)2º8è~\x0019ÝKÍª{©8³"\x0019G	Ç#^ÖW\x0005ÿº\x0012b\x001f¹\x001d\x0001vU\x0018kM7ja¤É¾\x0014ËN\x0005·\x001aÊýñè#ûb×Ù\x0017¾4÷\x001baw± ká¢E;?«\x0015}d_ì*ûâ´<Ú(\x0002:M¥4¢\x000cB5Ã¡_ìVÝíq¥\x0005\>OÅüQFw¨2p8ôÑ\x0015É®º"9ãSRB'A\x001b³ì(¦gì\x0001\x0013¼vd]ì*ë\x0002&;\x0015\x000c§ñRR<Èä^\x000b¥´ÈÝ(zqë¢¤.\x0019\x0010Ç\x0007T!i`!Ä\x0007%\x001f¹Q·Îb\x0003^\x0016ÁrùÜ'h£¤"ìD=~'ú(Üu«Â]2£i·hç¨Ã\x0011î\x00024=+*ÈÛ\x001fm\x0017¿j»8ÚÒLî\x0000¬¹\x0000Qù¬\x000bi Ù_Ø>rF~3¨Ãè\x000b:ÿ4Y	V],¨ý·¡¶º_·ÕcHJ\x0012iÃàC)¡\x001bÚ\x001d9ÄÓ×;êÖ·¥Rà/J¥\x001eÞüv^S\x0000l´+Ï\x0000\x0001Õµhül y[e4÷\x001fÿíøåtåoAUCTÕ*y TÀ)ÔS8® æª#RgT=DÕ}¨FQî3\x0008;T\x0000ÕpWè3oF5CTÓ
÷I+5P\x0011\x000f4Ä\x000e\x000byZV;dµ}¬\x0000[¹Çê\x000fb¥(Ui½¿X²\x0019Õ
Q]\x001fªRü\x001emÝ¶¤á9
üÉ|XZËê¬¾\x0015þ\x0013~õmòÉò4z\x0011X÷\x0015µ¬qÈ\x001aûX\x0007s\x0002#k¥z\x001czAÝÇaAê¼µTþdÛ*º`±	@\x001bê¶Ø\x001e°Î²«RjAàºÎ¸Ê±\x001fès\x0004)ýKó\x0001¥$\x0001\x0012ïLi>_\x001a|P»°#ó*ûì«ô,x¯ \x001ecR§©ÅSÉ$A-ëÈ¾Ê>\x0003)S2°Ö)º[{[ª\x0004¥[\x0010¯\x001d\x0019XÙga%\I)åe£ÌWRXXIÙ:|$xkaG&VöÙX\x0011
µÞ©4ÕçU¤r¨¤Y\U\x000b;²±²ÏÈJ+JA7Ö¤åù¶6òù~!;T\x000b;2²²ÏÊÂïÍVÖÂÈ¶\x0000­\x0001oÙù¹Öµ¬jddUE¥KêU6ÑQYeÅ¹ðy¡Â¯\x0016vdeU§U\x0006çl¦µ:\x000fAAc\x0010Ù\x0018Øy=ÉjØq¼Ý\x0017p\x000b]Þ©\x000c\lrÃ\x0012êX³F^X¯W\x000b;r	ªÓ%Ó²Ôu`XpÙ£®V)Ý?OP# ú|\x0002ªO9MeÌü(âuô¥y!V\x000b;ò	ªÏ'èYïÅæÑ×ÙÌ\x0016Ë¥\x0017¤¬kaGfVõY\x0011\x001cM9¶2R_ ·Üw©¤:1\x0018YYÕge±W|­0T<èMðl¸¤8\x0008«\x001eYYÝeeuê\x000eTÓ+©½Ä§hª\x0017äëëBY=:]ºëtÁ-Ð?T«Z©ùtI.'\x0015\x000b-\x0002¤££¥»«\x0000ËÿH\x001cã\x0007´G\x001d¸rÄ-TT²¢-Ý\x0015mi\x0016¦\x001d\x0000\x0016\x0017½ä¶.\x000c\x0017\x001er+YGV@wY\x0001ðPú¥°t£uQÒÈ\x000f¬°8È\x001e\x0008#ÖÐÅjÌ5ç2¢\x001aFu«Þ¯O×:2XºË`i'"7<`²b·-Êõ«^W&
æYÍ(Ò2]¶Ör\x0013Àh6£²\x00113v
`Fé\´Å¼+­*N\x0018ËFÀoëRüÂìJÖÁ2}\x0006ËÄÈ¯P1$X5¥µ$ª¶\x001cÕvíÛ\x0001
\x000eÉE\x0010I¾6¯+*?gVì<8Dj[þû»¬\x0014³ÍÄã_èÊp+aRÜ@·o½ðPV	\x001cwc/0:<E¹ ¨ò\x0011õ )Á\x001cÝ\x0010\x0006+ÀFÏ\x0007©$lxùéêËo\x0017ç××\x0015Ú\x0000Æçú£¬j\x0015¹åA[ÃW'Ô^<{yzrvv²«¸º\x0017\x0017gPRÆ \x0006î\x0017ÔÓ²\x0010ÉÌÛz^3ä5½¼Ö{B(º5â\x000e¸¼vk;qQKFS
Q¢u06\x0014â%ÛâN=0\x0012­\x001bÒºnZÏÑEð\x0004geòâ.\x000c	«_]?äõ½¼`\x0019²~Bá)ª@³²\Çz.ª7\x000cqC/®±¤mF°Y!äÁ7\x000eyc/o\x00144Î\x001dWn[,Ë=w!3S»º\x0006h \x001d=4áúô\x0004ÆË\x001bh7h½5
ó·Çêå#O!{]EîÁ6
ni;p\x0015"òÎûµzÞ«¾Âaãjî,ÓX\x0017¦ýHe¨:\x0008þ%ì|Ú¾wä*d¯¯VÜ}^àH¶%÷\x0011\x0016âózàùö×b-jy\x0018QEôØÚb \x0016\x0012KõÀ#û+;
°\x0015Þ f"?þqº\x0018Ú\x0013·`!FöWv\x001a`Â½¼¼Þ\x0000w\x0010;\x001cÈþªES\x0016ÍJi¹s\x0000\x001c¬ÚÆózàqìÛiÑ¬Ô
[\x001ex\x0003S1{ðà÷@'NLê4\x0011ùà._\x0004öªïm{Ä3¿ÕÈB¨^\x000bÝ\x0002±ì\x000c«¶þ¢Öþ.°Nê<mNâh!p\x000f>«\x0005¤W\x001e.LpÕWy^=:mºó´Á¥½´\x001dYcò\x000c\x0007¸Ë\x000f½zAh§\x001awtÖtçYK°\x0014LêÈ\x0000XÂÈ\x0010\x000b¥\x0014Õ¸£¦;OsFÒÐx\x0015\x001cÉ^8\x0001!1kå/\x0014(Ô»AâÝÅ(óÐêà¨×\x0015-0Ï!\x001eÜ#{Ü¦Û`Kå¬¤\x0017\Yí\x0003\x001ab±Ë
î®½µä.W¬cÉ\x0003?Â¶òJÚ\x0005­-÷æúýùoîî\x001e´Z±Ø1r+7HS¿¢\x0017²¼·«UÐ.u¥\x0008'\x0002`ºòÅ+ßW	Wâ4´Ði\x001e8
S\x0004áÙoãÞhåÛ\x0013\x0014¬Ú\x0013r7&)ÖN\x001axòÆ=¡shõÃL:ñbÑHª¤ºÔ@\x0003·Sb=_2ãÇNÌ\x0017mä4CNÓÅ	îbõ\x0018-¶¿%ÐÀþ¬Ðo$µCRÛG\x001a¹\x0002\x0017\x0016ýôÜÊ5-\x0007ùéÝ\x0010ÔuÚH\x0003+T´©=?íj>ø\x0010^î÷Á¤~Hê»Is`\x001e½Ä¢a"å»û\x0018_#i\x0018\x001eÒ4í8JAª!éå0ÁOHÀ4Æ!hìZÒ`)µ\x001b@?½ãK+&æ)¶qnScScí+
2\x001a«\x0013 !ªøÚ`¦:\x001bIÇÞ©Ë=Y<íd¢´á5e?9ß¼\x0011tädwr&Ò¤%
\Ç\x000c\x001eåDá¿q]*GÞIv¹''Í\x001c\x0008¢æó¤4LÄ&¤#ÿ$»\x001c\x0003\x0013Jã|ñ@\x0012mÊrëPÄi$\x001dù'Ùå b1Ù*2\x000eTi\x0012ò\x0013£°\x001bIG\x000eJvy(ç]yìµÚÜ
ªÜº\x000eâôåÈCÉ.\x0017\x0005¦\x0013ó/ÙL)ÖÑV8øìÔaÎÔÈEÉ>\x001fµ}\x0018Ió)ó\x001b¤`e[31§¬tä£drXDE·nðWAÄâU6T\x0013å	;¨\x0013wn¹îîl&õ¢\x000c\ÝRjY\x0017UÇ	æ¶EU#7¥ºÜÃ¤\x0000u³áóy\x000e¦ç\x0010£'ÒÞ¨ã[T£òXJç_\x001aÞ©å\x0005D\x001aûFÒR}~*ò4Z8S4æ\x0017ÎãÓ)Ù\x0003üêòS^Gvþ\x001e M~gÔeª»êoD\x001d9*Õå¨<üæ$¨\x0008kõªù÷ç»\x0018\x000faRÕÈQ©.Gu\x001dÔ³àÃ482TÚN4Þ6¢\x001cêrTp\x0003á*Z´U
\x0017uè01¾\x0011uä¨T£òNcUDZUÏ-lAG©\x0000ú çä©T§ÿO\x001aØÍL94Í\x0005ÕJOTi$Õ#O¥û<\x0015\ éÖïQ\%\x0007*F8>US\x001da¨#O¥»<\x0015Î&¡\x0012eSùTq©oÖH:rTºÏQÁ5:\x0011jcäÇ"=1J·\x0015uïëòTøû\x000bêdöE±Ë\x0008Ë¿¿=û×#W¥û\Ut<\x0001Ï\x0017\x0006\x000e\x0013¡ª	ÕëFÔ«Ò}®*8KN\x0015]Tâ<ª6\x0013¯¨#_¥»|Uj~S+;ÕLBXÈQÕÔlÐFÔ¯Ò]¾*\x0008ÃïÛÞ\x0014ÁSH¿ÿA,ÕÈSé.O¥|ÔÀ·+:TXP@Åþ I_=òTºËS\x0005YÊø¼Þ\x0007q\x000fx£jC5#ûoºìP¦°*¬K¶\ÐÉ z¢ªtdTMQ
ÚÒ{\x000f)¥4\x0004^T1¡Ô:²T¦ËRá\\x001bMþ_ð8µ°mÿKá!B\x00153:þ¦ïø£R°,¥óôûoûU³°ÿftªL×©ÒR2c\x001fX\x0016\x0014ÙT¡¯:\x0000ª\x001d*Ûuª¢Ñ¦v°WIÙ)\x000e«8Ì\x0005À\x000f\x001f©é¾\x001e©;®¬·l§BjëËe¢¬5\x000eØ%X \x0018Sd\x000flätÑõA2\x0017Zÿûf'"ÜtÆÙÒ8\x0017ÍÝU\x0018h\x001fÂ%\x0008³»¾¦sy-l\x0008~\x000fÄ\x0016+Mo¬lÃìÊQëÅðÞ\x0016½\x001b"\x0014µ+¼\x001fÐä¹¢ ¦ê®\x0007sõ\x0015ú\x001e¬îÅ\x000cV\x001e+\x000evWRtÁ¥èÊÕU\x0005ÌáZ¹ke'n´\x0016[m³à\x0019s©Í.ãÊºÝ°\x001fWìV¯T½òäzó\x00150¶\x0010NXyÃT$-%ûkå\x001d?\x0007B\x0000ÝnUþ]@5\x0004TÍ\x0010{~\x0002\x0003ò/®ÃþR\x0016@=\x0004Ô­Ø¦J&É\x000e[À½¿q\x000b \x0019\x0002f@[\x0000£®ÏfS\x0006(î
«Z\x0000í\x0010Ð¶\x0002ÆøÀ\x0017
;ª¾\x0015EgKïO¥µà¹!ëÁ#\x0019\x0003	\x0012\x000cùüþ©\x0016@?\x0004ô¨ËAPÈR¶¤øö\x0007£-a\x0008\x0018\x0001e¹,ã\x000b\x001f­ ÛzñýÙZ\x0000ã\x001006\x0003\x001aô%\x0019Gð\v ýþ
ð\x0006ÀAÁÈ\x0005'mE_á^GuF{u5¢k	Ç¤ÕXYfLav,ð\x001ar\¹ß1·ðülu$Ö\x0001ÞI\x0014 K+(-çlõþÇå\x0016Â#­\x0004Ëóøý+¤©z9v\x0014åýk­#G"[=EÁ\x0013_î\x000e¥HëõpäId«+A5\x0006zBÂÊK\x001ccyíZëåÈÈVgbyÀiCÇµ¢RM¨ö¿Æ¶\x0000|lv&FÌ¶\x000fÜ*'\x0005«Ç¥û#g"½IT\$âÁæÐo,=ËGNe´Z\x0008GÞD6»\x0013¼µòC{ è¨qßÿÑ\x0000¨FÞDµz\x0013',x\x0001\x001b0\x0004É¶ýj@-#o¢½Ó%Áê\x0004\x000f ¨¿<[í¯«m!\x001cYkÕl­±>' ,P\x0012$7hµ?¯Þ\x00028²ÖªÕZc"Åý.j¯¤_¾|úõK8²ÖªÙZGÉ\x0012^«²
½ØfÑ×ZC52×ªÕ\;¥iúAÊóR§TÛtÃÚÈZÌµj5×Ø\x001dL?2$Ñ\x000cåÍ\ì¡k!\x001ckÕj®\x00118{!-!\x001cjªé*ùF5Ñ\x001dÑ\x00028²ÖªÕZ;é¹õÓÃjR\x0004N\x0019+Ï\x000ek¡\x001ekÝl®­`sílI**ÃR«ïzd¬u«±þG¬à(ø×­Á?\59.tÊ\x0012hÏ\x001d³\x0013ý$-ã$R«7q:<à÷$ÁWx5bZ½#g¢÷E+J	\x0011Åzg^ÀýE\x0004-#_¢[}3\x001a[\x0012 7jUÚ\x0017;³¿ ·päKt«/ñb+%\x000e\x0017dEåR\x0016¸6,Ô#g¢	<£Ã9OÓÛ\x00026]ð\x001aî\x000ch!\x001cÙjÝl«QyÎ³[KÈÒ»jbÚ|\x0003¡\x0019ÙBÓl\x000b³fwg¸¥<b¯=ÈfdhL³¡»e_â9\x001b¬8l\x001f{5àè æj´	Q\x00176¡Û¾W¯N2Ñ11ÍÇÄKn£Äæ{65åNÚ_ýÛB8:&¦ù\x0004Ï¼NÉÒò\x0011mywZ\x001d2ØÑ1±­ÇÄ\x000bWÊ d _YË­ÂÍ~1Ò¦|æè\x001d/ç4ñ¯ü¤5a
ÇïwøRê&nßoÞ_lnj\x0016\x0013Ëgß§C72¬ñ-cÜ9ÌÏ¯\x001f\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=J~ËKÈºxwzñâåa$T\x001b\x000c$ÈËÂ'pô"\x0013\x0014Yú©\x0011¡Þ`\x0010Á6\x0012EO:é\x0010'Ü:$Ô\x001c\x001c$³;Ó"ÕÖ¥²N6MnÏÊ}CÝÁ@JVÇgu\x001fiÚ!Ì"¤©}Å\x0018\x0012j\x000f\x000eR \x0006	0±®8¡	)ÔÓ½\x0008õ\x0007gßj5ªa°
÷\x0017äz¼5D¨A8×-Ð:\x0001a$]7\x0014Á¯\x0000IÂF\x001e¢¡\x001e¢% \x0017\x0005iÁú\x0011\x0001póáÚ\îHÉW\x000f7_~¹ü¶¹½Ý§f¡ç<¦}gßªèY\x00195é}=Í)H¯NÎ_\¼=úåä×Ó/÷)Ú\x0019Ò\Jv")ª0\x0010\x0007VñÈHÖþ,\x000bch.%»°*+D}\x0012)Òõ4ÑuDs!ÙMÖcÀ`XF¢Y^ÆHs!Ù$§ø£NI6Å&×îÛ\Hv"Ñ{n\x0013O$¢Ã-µZ4}Hu´Yné\x0008ÉÓéëæB²\x001bÂ\x001bÞ``)\x0001Q\x0017s/¦¾)cHs!Ùä1\x000fË\x0005hÊIkd¦ª« 
\x0005þb!ÕFÏÐ(Rã}\x000bº¶UÕn\x001d\x0013¾L\x0012Éb?8`ÔwÇ\x0006èbzÿmsóûf¦MÎï\x001f±Gé£\x001fï¯¿B\x0016çÑ/÷%sÂ\x0000Òÿ\x0013N\x000f¾Â½ÃøHRu\x0007Ï__`Ò·G?¾~þ\x000e28~<¹xu²/s\x0006XtË\x0008 Èõ{Ù2Ð\x0014/4É/\x0001úïÂW4Í\x0018\x001f¶\x0019\x0011Ð½øÈÙ\x001b
|Àðû½ùGöòr¦KÌ_\x0013ßÿùÿë@ùo°®¶óM^$cÝZk¦§ûs0[~<Xõ;ñÐÜo\x000e\x000f90Ù-Çþi4¶Â(?\x000e\x0003­­µdÁ¤³T¦\x0010;(ä.e¾É!oÊ\x001a¹\x0007^\x0018=Çxt\x0012\x001cÌ\x001f¥bLj¶x&\x0003Ïcr!Gfiy\x0014öUÐB\x0013¾q\x001e\x0008[ÞaÖÕ>p0e\x001b;»\x0019ê¨iµã< C\x001co} <\x0015c:ÞÑ\x0003WTdBÙ©\x0011*\x001f^Ù88&?õf\x001c´\x00088SHGã@ÛÀÃVÒÅUq5T^}£ð$zTX±[Ôp ÇDK\x0005\x0016\x000e\x001c^ª¾\x000e4\x0006úòä¦¥ùÃ\x0000
\x0012Û9èþ\x000b\x0014ªÖ°³Ã\x0003@9mµc&Ô2gWhä1tÝ¥\x0018?@SkV\x0006OXí þ,à\x0002¹z¿¢Z\x0001\x0004.ùÃ\x0000J\x0014
¦VPNÐuLXqã§\x0018\x000c e(·ÁéxÝ%É«´b*\x0019âãx0»áÃÀõíÕEY\x001bôAP²\x0000Í\x001aô
\x0000åü@ÞO\x001e¥@
&\x000c½\x0007Am¡ý
(A|åO?ÜI\x0007Ê\x000c\x0007ÐxI\x001d ¢\x001f?@S?E\x0006\x0010LÇ\x0001FP=éh\x000c\º\x001fz\\x0006©Ü\x0017I°¢\
¥%5ô4 \x0001­Ð\x001a*·F\x0012,!¤®\x0008(¥!É¾ðÔ*-\x001büøVàÿç\x000fÇ{êØ\x0001\x00056Ë£Z;«\x001aæóÔ&\x001c\x001e{ìêÖýmá@¯Ø®:c
;H"º6Â¬ó]çÏZ|\x001e(£Ï\x001f\x0006öy²
­±.xQG\x0019·âÁ\x0014¼üa\x0000IÊ¢Í+íU\v\x000cÁ\x0007FùÃ\x0000\x0012²ÊDxY/'ÈYJ31¬X!ðPò§\x001fHá{qÖb\x000cEgª[hÃ+\x000fÞüa\x0000%çB£a\x000f\x0013±ý¢Q2Ö­ðsYqþp4u²3 :µÈx5~¦î¡\x000c ©é5;?Ùà\x00145ãèÍZòÀ\x0008Ò<KHÎâ.Û\x0002\x000c\x0015% 8.¦-$\x0005çO?°\x001eðø¸¤%æ	-\x0003Õ?\x000c ¥É=´¡*zMÅÒ$/m\x001c\x0008ZåO7NPÌØëZi¥)CÃ\x0004?®:,ÜxËºö>zGá$qpPPVÔ[¶"<å@Ë;ª÷1ÝuýË¡LjåéÖh=~íóàlÇ:ÔiË"»XÇ-3u\x001eß2\x0007üámÙÔM
=ze<µS+ü\x001f\x0007cY\x001f>UGÎÂ47ìë\x000céV·Âú¯gùÃ\x0001Òh-\x001agÉ£\x0007«¬ðè5\x001eÎgùÓÏ\x0003u©\x0006w,9÷T\x0010(ÅÇè\x0015æ4\x0018åÏò\x0001ä¨ÈA8\x0006¤ Z\x0015\x0001{\x000fJÌ³4\x000f6bJ1tñuRL£º\x001d÷ §Ø\x001c\x001c7\x000cæ$ L\x00148«M\x0018÷!EüçÉè\x0000M&M5<¼!\x001exÈ\x0015\x0012(?\x0008æO?P\x000eÉº_%ÏÐÃ`GÚ°8¾B\x0011Îrä\x001dh\x0017ë\x000bzn\x001aSJ3Cttå\x001f>ÐRÃé+ß~"\x0005MH*l\x001fÖ\h5Ë-f\x0013ÅüZ¿ÝDyV¤¢¾e
ëµ\x001ct¬*Då±dH)¸ïåÛO\x0004-é°+UÎì-Ó+²ØI-iýaÛCe;Hñ¬!§ÒÅ/uÖ;\x001aLê47,®ðÊ¤×¿]èâ\x0015+¼èhüw2¥°ý3¤fS8/+\x000f@º.H×\x001c¤dÜ\x000b´Ñ¼Ãë\x0006suÈ\x0004µ\x0015\x001cqïaÀÁç,
<î¢Ï©y*9Í¡Å\x001aÿ\x0015Àå0A|ra¯.¬¦QÒfÍÃx2c	¬Y\x0006ÚÑ´G\x000bQ¾b=
Q\x001b\x0016Ûq\x0017
®\x000b\x0012ã8ùä\x0015Ö'r\x0011ië¤©ý£\x001b¿uI-Á2Êå,ÞÍ¬§\x001cÈä9²Óç?ß_ý[PÂ¤t5ÉÊÍÑ+èãùñîòzÏIéHSt&\x0019ý%#ÓªÉK³Û+tzô
wþ|vòü \x000ezöâÄ¤4uÝ0LE±,lcÝ¶þgàLexý<VT§1\x0019´%ëÉ\x0006:ÓÐ\x000ck\x0005\x000e<*Îâù=ËS¬Æ£Ñ\x0003IÛe]5ø×ðÀâ,ßÁT\x0008>Ù¤Ö\x0004òXEû%ã¶êç\x0000ekD2sZ IOfÖÚÙ\x0017HÒy\x0016;áX\x0016\x0010\x0018lRq \x001dµ\x0007¼5Du\x000b\x000f\x000bèTï¼r²¶\x001eî{\x001c6» u©²Ép«\x000b\x0014Wñl½wð$\x001fDá\x00112Ô§/Z_U¾Û>\x0008\x0007\x0008R×ò§\x001f(ÔòF+\x0005*èÆ5¬\x000e\x0010e\x0000%\x001f\x0004Ã\x000eÑå\x000cD\x0001tmWI!0deä\x001c!¤P¬<Xëä\x000c=y$m#Á£D\x001e³n9<ºf\x0019Hs.G\x00082\x0011H¯Qb¹\x0002 úÒo\x001b'?_â
¡±FµGÃdþtó(Uëù¡·½)bÚ\x0007</Øy¸ç\x0000Ï~ !r\x0002\\x0006+ï-+Wb'²Ç\x0000ÊùÃX¡\x001a>×Ê¡÷ôXº\x001f+®Xn}o,k%!\x0004¶>JÅ ©
´nÛ9ã\x0000Á[ñ¬\x0005°C¹cÊVK\x0000DÍ bnÅZ;w\x0003ÁÓ4Zb,-&aý¶+4}:=¿]Ý|)Ç\x0008þ¦¡AO?Çg°è*Ð,w\x0019v=\x000ec9óí\x000f}=ÏÜ\x001c\Êxø÷¾¿{¿ÇÀ÷¾n\x001c´\x000f@í¡¬ªÕúS'óÓ£çÿÛ\x001bÿp~°~<Liñ\x001c"µ{I"
ªÝQ$¼½Ã\x0000a\x001e<\x0007HbB\x0017U­JQÖÔþ\x0001\x000fäÕçÇÜÃs¾g0$ù§w\x001fo6ûÚ\x001fÁòH¬gØ\x0003ZÕSµF^\x0001
\x000c!9:=ûùÅé¾G3i¯ºH%D-aà&®\x000b©Õ`¼\x001d&6©oM\x0002ÍÄYjfm\x0015\x001d\x000bÃ(¥ø¬\x001f%ÖJoM¸	*\x0006ú²÷¡ÄOAßyS(`ùesyw·9ú9Ï¬yØst£¢eÌ\x0018dÓc	ÿ\x001a2ß3Gùåôäììôèç<°æ|ßÁpÀ31\x00135Ëm,%ú@$kÊ¢
«,<\x000bÞ\x0002MÖ<¤íJàOt÷`ÿøã1o\x0019øÌ\x0001~ÿ|ôÓ¿ÿûáòq\x001f\x0000ë\x000b%«ÆÚTÊæWG?\\x001c\x0006±îFôÔü¨UÎ,Ïn)EÆ¼q,d¤|\x0010\x000fóÞ\x0012ÀñêòãíÍåÝýÿ8¹ýp³y¸Ù\x0007\x0013M-Á\x0013ô2\x001fÁ¹ÀÄd\x0015Sóêäç/NÎ^\x001f¼üéÅéùCLS\x0007"\x000e\x0014ô\x0001Â6Tª\x0016áÕ¼.g\\Å¤óÛ\x000f	Õbö$\x000c°ð\x0018\x001e£¬\x0013'gï\x001a#PàÙæ\x000fk¡\x0002Öu`k`á»u¶¦·
«\x0013ê÷øíÆ~ÞÒZ¯.\x001f®AJ¿ÛÜ½ß\x0017\x001bO÷üØV¥\x0015©£¯eïjkÎ~wzöã¾øê¥\x0014Ow³$Ë\x0002u\x0005tq*(*¢+H&µÕGBõ#\x001evXê4YË\x0001R-ÍÁv\x0012ÉïrXHçÑ<\x001b¥\x001f>|Ú2·ÊìÇ.\x001f¿|Ý§Í\x0015uqÉò+sè¢:¨ØØ\x0015eèãO'\x0017oß\x001dæm\x0007Ô%OÁKã±6\x000cº\x0010\x0010mï\x0010c2µ:8D ãSI#r¦ºz%dk³@¦»Ó³1\x0001õ¶O²\x0016\x001f#LÅÀ\x0015qn|E¦«Ó·"¥AWª´N-Í\x000fêLõö\x0016³@¦kÓwDJ\x0018ÐKok¡z$Ç z7\x000eRZ\x000bô\x0008<«*ÙâÔ&*\x001a/«f9\x001a\ÒQ AÊ£8Áµ,\x0008\x001d ÆAJ\x001fþ\x0005	¸ 4È\x0000ºÐèñ\x0013BÝ\x0003zA\x000cÝ^	\x0001ÞÞH¹!ó$\x0003.\x0008¶\x000cè\x0005©í°Tþik\x0002-Ik¨°HfNR\x001cÁÊ\x0005ê\x00146Íé\x00106¯	XK\x000c\x00161`þ.VoZF\x0012$Á1uÍÕ§o÷\x001d÷õñáîæîq_¹¿s\x001a\x000bmö5µu¢A§P×r¼»8?{qv±¯Â1Wy\x00071\x001c6lÏF\x0000UEo«ÛF\x0000\x0007c®ñ\x000eb\x0004¬\x001aMæ¢ÀÄdPM[0Û'µ\x001fc®f\x000ea$ß\x0014GP\x000bÌ£È\x0018Tn\x001cæo<=\x0018î'cú\x00058#'··ÿþïÍ£÷7_÷üðþæ~_\x0003)?¨¨ËNÄÁØÚÍ:ÚÔ»\x0003)
§o^¾¾xñ6yÏç?¾x½¯TESs4ÅD3e¢RîI\x0014©6µM«ìÙ\x00116=gÓL6\x0018u=¥¦î\x001a8É©qô\x0008\x0019îªIlw[ìR§Ôê\x0005øéê Ù9å.$ß6ý=5Ñ¶ö\x0004Í\x0012ãlnÎælJÖuZ6ÜÏ©¿¬²r
£yîcAgÍà±t\x000f¼¬Ë¦Ö°9[`²]»½\x0011ÚÔåu9\x0016çh»l2Ã Y\x0017\x001aÓzêî.ÖÜQ)\x001a¡+l&\x0003:(8h(Dzj¡ÆkàZÀU	:L\x000b§(ªµ©\x000b\x0017Ö\SÙè\x0004ÉU
¢\x0016ÒE+ióÂÑ+n²»V-\£\x0013$W)h]g)\x0004I\x0006µ
ÓÂ­ak´dª\x0005\x0018H#éÄyréT}´ôz^^\Å\x0000v³¯\x000b)]ZU}*üª»Ú(\x0006ÉÔ\x000c>Ù\x001eY_WñÈÕM5j$\x001bÍ ¹ªAÑd®2CN\x001c=Æ¤[uä\x001aÕ º\x0001ÆkHl.kkBU{ÜùYñÛ\x0008\£\x001c$W;HO3 `åÈ\x0016\x0011ÀxÃ©F=(¦zðÁcà< <Z_¨®¹ªªQ\x000e©\x001c|âÁn\x0013\x0011Æcb`7\x0018ÚTíÖ\UÕ:\x000cLåà ,1X7:qÎNs\x0014Vmj£\x001d\x0014S;@ÀÄÒ¦*ô´¤¯rDÇ5ZU5ÚAqµSÇ´nS$ÖL	$ëÖ­Q\x000e©\x001c|²\x000cj.5\x0017ÂÄÞÈUprP\åà\x0004\x0015ØÀÊ\x0002¨&#SÇU×¡Ñ\x000e©\x001d¼Üà\}rpn0´
®Ñ\x000e«\x001d¬%¯&\x000faÁ\x0014!=i5\x000ejb*\x0007\x0017\x001d9ª ò\x0015-Æ¬ÑùºQ\x000e«\x001c¬ÈU\x0013¸«<¤Üd¬¹\x000eºÑ\x000e©\x001d`rDUå£_3\x0019\x0011Î¯ÙUÝh\x0007ÍÕ\x000e\x001e¾ò\x0014z	@\x0010e¥­Àº'1µCÒ¦T\x0008\x001f§\\x0004èùW\x0013ÔV\x001d¹F=h®zP
 ÏPÃrªùövÝ}hôfê\x0007è=ï¢ÒØ!,	ãÊ&ÖXKºQ\x000f«\x001edò U}Óó«\£\x001e4S=@ËTOG®\x000e4¦ZvU\x0014S7êAsÕÃÔ©/êiWC\x0015s6¬q\x001et£\x001f4W?ÉSÕÎFÕmUk¢\x0010¦Ñ\x000f«\x001f\x0005¶P¯©Qy÷åVÙK¦Q\x0010« | «\x0008sðp[kz·«Ô¾i\x0014á*\x0008èMbÎã8x0ÑÉ^
\x0006\x001ck\x0014á*\x0008_\x000bN@{¡O\x0008Ý\x001bH\x0004¯:rí\x0003W?LIk\x0011Z2ÓÂé¡#p~0\ý\x0000Ï²*/Ïê,VÊ`Ó(\x0008ÃU\x0010³p&ÐàÂ:rU\x0014Â4úÁpõ³5d\x0017ÍrRªÞÕ¸ê®6úÁpõ\x0010Õ$1® ~j~6gÍ6\x0012Ø2%0¸\x000fØB\x001ebÙhÝ¼ZÅÖÈ8Ëq`¡£ZF5¨¹,%ü{¿Ê³³\\x00117õÞÚPÆ²\x0016ÎÉU\x000b×È8Ëq\x000e\x001a
 §\x000fÃ\x0002\x0019èuWW=ÙØFX¦\x0018qÁVå`cM·4u¦,\x0004]WÀ5rÄrå\x0008t<õÕ ¡A^¦*x·\x000e®1å,×3±¾ÄéP]\x001bA=Î=\x0004\x000fÇá\c-9®µdLzJÝ³£õ²:·æ²ºfá\x001c{á&5éü@p².ÜªûàóÜÓ¥ \x0012ÕªÁY¡Nû\§\x001e|#æ<WÌA\x0013\x000eWUWiÒ\x001e§\x000eX~Öt\x0004®±<×ZJþ\x000cMWCà¶újgúUv¦o\x0013!¸DMU|VPq\x0004\x0012ÜªÇ\x0007ß\\x0008Ï½\x0010É×'¿kR­P%U\x0015Ä\x001a1\x0017\x000b\x0011¸\x0017BÖ6p\x0011\x001aQÒÊÕñÀaÕ\x0008Í\x0008Ü\x000b!"%zÅÙ\E[C8A®zð2¹Î·}\x001e_á\x0005úMõ
§\x0011ÝÊ:?xÍú)·è\x0006\x0010e­<¨5FÔM}â7zÕCIØa\x000c|Fë(o\x000e\x0002Ä£¦Ü\x0012cVEëÄ6£\x0016\x0003*\x001catuÀ×WHe¢èÿº¸Ø\x000eãÀ:ÂÜ)Èc(Cr\x001cW¹f;Ëh\x0006QNÏÿ0§¸ÎD\x0010×ä&$Æ¯-Fø\x0015\x001e£Ê©0hýÙ\x001a+«\x0016Öª+cÔÎ:ªuÕBÚR\x001a\x00158mµY\x0015\Ùf@:BJ\x0011Jðd³Rá·1¸.Æ²Ã8 \x001e¥\x0001ðÉê"çÒ×7n/Ö\x0018ÓfçV[-T}êÀ\x0001.cí*,ÃUÒÎµ¶ük

þ±\x0015(9¨e¤3¸qçÊXþI\x000bV!µ\x0013Ð\x001d,±U\x0011?»sc,ÿÆ@8^¬Ï\x000fX\x0019QW{lp´;\x0017Æò/Ãúã\É.ÉfVÕ Â à	â·6\x000f4\x0007úms÷¸9úéáßÿý~óps}ôêæË×Ëýf£ \x0001ÁÑP×Î(Ì\x0014ºxüzzvqzôÓùé§ç/\x001f½zñöÝùÉADÛ Ú\x0001Ä:\x0018#\x001aKqa¦f\x0000z\x001dá,¾\x0008s|K¨½ªyïd{×ñA^Ï3C¾Aô#ÚÛ(é\x0011\x0015þ©ZÑ\x0010W"Æ\x00061\x000e­¢rÍ18þ©:«Ú¯D\x000c~\x0008¡UÄ~²Á[JN\x0016S¦I!ÄØlt\x001cÙhAî}²zò£MA¬££ý*B¹%r\x0006d
ºß\x0007@`ìFQ\x000b\È_Ç8{ü\x0005Æüú;À]-\x0014e¶
zþuNÊ\x001ce¶êÍ ±å´Íï7G¿n\x001eÞ?îk«c>¡ÔQï)H-T¤^	Bmïï§G¿ÿx±¯¯NEÒs$Ý\x0004
ßÑn
\x0002§q¥\x0013W;1	»½ÝHvd»à\x0012÷Yz(dIBùµAì\n"?'ò\x000c¢)\x0015#ÖöbÂÖáÑJ\x000e/R#E\x0006R¨m« 0El­,\x0015£H²=ÝýÇ\x001bæ7\x0006S;Ðñ¶4>=Ìº°õ2I­²ð¯Ë\x0004íd oâ\x000f÷·oÉ|\x0003¬³ËÞ\ÿ±7\x0011ÉLòº¦\(EAS;«¡ÿáõÅËÓ_ù\x0006hg'çÿ÷çÿ×^6µ%
Ò/4xþióùæ.\x000f'u÷qóõëf_IlE%!\x0003¹,Ñ5\x0003iª^xþ\x001f§¯^å¡ä¯^ý|úîÝéÞºX"Ss2Å#0øÌ</61³7\»\x0006MÏÑ4\x000b-DO\x0013ab¬QFê*F§ðÔ\x0008£\x0019æª*N¡)2¢\x0019ê\x00134Ï Ù9e®ÌW2K\x000cAU<FP>YGÈÜÌ1\x0017­VE\x0017(ùÞ\x001a\x0012½Ý ù9ç-Z°µr\x001ez¤`yg¬]|X\x0016æh½j
]|oV-¬º q\x0016y«\x0006\x000cñ¨A\x0016#­\x001aµÿ\x000fjT
O³¼\x0015ÌU5\x0017*Ù;\x0018¼1·\x0017õk []ÀS\x0006Á&áák\x0004M­\x0008TmZáÖ\x001c6Ùh\x0003ÉT\x0007É¿S¾Ú\x001b¤¨¨&Ðd°5ê@2õ\x0015\x0018óÐ{ÐJ¬ª¯=<×Ü\x0003Ùh\x0003ÉS\x0007Ðµ\x0001»÷¤\x00113ôuÕÌ*¶F\x001dH¦>ÐÚ¶YE=A´¦à¤[Öè\x0003ÉS\x0008 à±\x001b6<2\x001eMÂ¬»æ\x0008W£\x000c$S\x001b\x0008s\x000e#^ziçÉêø°F»ËF\x001bH:\x00088\x00077\x001bß
aµ¥îT\x00153ÂÖ¨\x0003ÉÓ\x00070\x000e& ³â]m'\x001bj»Â`Ö°©F!(B/\x0016³Y49RëØ\x001a x
\x0001ú_RGà´nÖâÏÐ\x0018c
[ë\x001eð\x0014B\x001e;Ë\x0016ëq®\x000ekôjôâé\x0003\x000f£ð*@¶=Ö\x000e\x0007R£a\x001aUBPL\x0000Åý¦ÞR2è0]ÒU«Öè\x0003ÅÓ\x0007ÞY²>dRöø\x0012¬\x0008-°ê¬5ú@1õ§®Q\x0005±\x0018µ©ç01\x0002Ö(\x0004ÅS\x0008PÂi°]a2tQ¿+PT\x0016M­\x0012ºªQ\x0008©\x0010SºÊÐÉn%-]s	t#r5Wä*Lô0¨\x0007\x000b_åQÕ¨ZcëF¬i¦Xs\x0006É,2dçjo«Y´*ì¡\x001bá¡ÂÃê*×&?yæ\x001fÌR×GØ+ªW4)\x0018«iäÉ¬1\x0019ï×Fº¹	y\x0013dÀç³ÄféÇÐ×ÜQÓÜ\x0004Ã¼	Ð\x0011\x0017ÕA¨1\x0019-uUð~>0ÍM0Ì\x0000Ó<±Ï&$2!ÃÃ\x0016¥_#@L\x001bdc^\x0004Ióü¼Æ¢hIY"Q¬ò]Ls\x0011\x000cï"@ÏPÔ¨¬m¦.ÇÂéÑèkJèJOÍíñè|ómóåúr\x0019\x000cº\x001eP½³z!xMÊLÜ\x001e\x0017Gç§¿¾}~r*9U\x000cýTJ¡\x0017êÑ$Ò ç'\x0013ÄÎåìSí\x0017@ÁýTÐ+ÊãZYª\x0008u\x0001\x001cÁQ,ÛbY\x0006V\x0002¥.é\x0002TNQé@XvçlõbMÙÕ\x0019+H\x0006\x0016ôrÃñPüã'ê]?z®³ßB)\x000e¥<[§\x0015Ö\x0008ö^¡rÃXj\x0016\x001bMXð#c\x000b#56rZSuAÔ\x000bQ¹T³\x000bPÍc.\x0007© \x001d+.ªå«9cw\x001fTz©T#\x001abÈ\x0006mBÎ\\x0003*Q{{ÁäMÄÒ~GÌ÷bv±\x000cg±\íFL¯\x0015ê8Y;¾±Å\x000c,#"MquÊ\x001fãT\x001a]Ç\x0000Û]¼\x000f»ÚÞÅ+Æzyª²±LÅõò\x0014\x00045Z­8]¿]o]3ÈDvòÜ@\x0001÷\x0008©ºLº\x001d×²,lYÓI«5ÖôÑíåÑùýãÇÇÿï=ã#"¼Ñ¡¬÷&\x0016S\x0008ÃZ³k\x0017\x001e½<9:}ñóÅÓó}\x0013$NÎÂ N6qÐ><W\x0017Á:¶}r¢¾©¯ä-_dóÁØi|ü\x0011'©ÄÌÎZQ\x000e\x0011ZÝ\x0010ZÍ%0a\x000078	:,
uTo\x0017^þ9|Î4|Î°ù #Ç\x0015tÔÊÝ\x0005jIi\x0001u\x0005a£¯B«¯:	½¡>8ØèÙ\x001b\x001a=cÝºS¨f\x0001ùL\x0018ø*@ ÷\x0012¦ÜûZlWî²Rí\x001a*þ\x001a\x0006Gï¡\x001ej+\x0008ôNÔ]\x000e»±\x0018\x000eáÌ?\x0006ÂÆAî#>§¥eBC~¨÷noýBâ\x0002P¶Oh)%Ò'Ï
ãYÞS\x001a¶
f%a{\x000e
û\x001cªd\x000c4Dq\x001aýZo_xäà\x0010ºv\x001d{Óåª\x0003¶líþ\x0015D=\x000b\x0010\x0016`»¿ÊÑTz\x0000t4òTøï\x0003\x0018\x001a}\x0002?r\x0001;!1ëUÔ(WPTÉåÔÂc\x00110¶O®/Ù\x000c0Dæýóc£^¥Q´l\x0008µä\x0013:G#yJ+ù)\x001c	wM{\x0016¡ndM®,`\x0012Bÿ{WK\x0001B­)tBîÆY9Sñ|&ôK¨aÞJñp}d×ÀÔ
"»C\x000eallÃÜ^Ih"fÂ%BGùá\x0011¬B¸N¡Ö¸6|ãZ;Sa\x000cY·d\x000fÓÔ\x0011fÕ\x0012\x001aÝ\x0012j>a\x0008µ
@[g RÄÀÉ°û(Ç!´ÍE\x001f¹ÉlÀüÕ¤~o'"(V¯#\x000cÍEÉÍ)y\x0006\x001aI\x0016@©s	\x0012\x0000ÖaãNÙUÒÐúf³~â\x0001ZåkMr\x0018QÒªÖ»ÏM\x000c@ç\x001bq
?2\x0001\x001dt£G@]Rs\x0012¡¦ÞïN¯4ðè7\x0003\x001f~jt\x0012T¹Ó	Ðh£tò*}âCsM|`_\x0013°\½%V# 9yn]\x0018Z?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;ÚÂ³¼þ·ù Þ \x001aÅRUOüZ½xì2¢\x0018H¡4ciHÒk·£\x0003ëæ¶t9(¯\x001fg÷\x0011­\x001e\x0006p\x0014Å\x0011¥Á.GÂEY\x001a
ÿa"Ïê)hGZvxM4´g\x0011+²\x0010ÕSÉ;@Éàç¿X$½\x0005NÇåç¿ÿC\x0007®£\x0005«¡[ÊnÈ¡ /\x0003§\x0005KU¹gÇ¯èÄ­nµ\x0005NÕpj\x0014\x000e¼AÇOÑûDI\x000cËe8W
\x0000§k8=\x000c'¨Ø\x0011(KÐKË\x000e´Õ;ù\x00048SÃQ8\x0019¨þ\x0002VÎÒ 5/
Eø°
þ,8[ÃÙQ8p¹Íªï/õ\x0017¼©u×ß	h®Fs\x00136Z¬c
¦çþÌ</PF©çÀÅ\x001a.N8«2û=øª¹_rSURèV¸]n4óñWIA@ôc©r\x0014\x0014\x0015ó"\x0004>\x0011¾j?¾x²Ñ%rXcæIê_u&¯\x0011]'À½ýÉÅÛ:\x0006]¿9cêÆ«»_¯./nw^\x0002
|¦­çI\x0019p?äõ\x0008[G#ªgLâxutþ
ÌÅé6\x0003Q¡Q\d\x001cMr»Yk\x0015]Q\x0000¯(iÌùL4J\x0005\x001aF\x0003Ó\x0010	
ÎBn²¯½/«¦êÝÓÐ(¢3¦\x001c·2±_WàrBIØnPÎE£bÌñ

\\x000co¢¥´rí#wRÛs\x001cö}^~¾môáéÝ§wË«ÝÇÑáËrP\x0003\x000e$ú³*õVô¶\x001fÖb×OÏÏ-N·9¯ÕçKìÞÏ;Þ$ãÀï1Y\x001b`\x001b\x000cú¼n«Dû>_
4÷~>XNã¤t\x0013CXùómVf×çÑG¶®ëûY¡i>\x0010*\x001dC\x00154Æ8üùuhÑö|_Ká)¥ÝXe¨D\x0016×\x0000¼ñÃ»fÅ§\x001f=\x0000 ~ÑS¾£§Ô(¡§_ëE[£Û\x0003R"Õ í\x0005\x0008ê´áúdèV\x0019\x000c_,\x0007\x0001,Xìô£\x0007\x00004(m²`\x0011Üb]3\x0012¨\x0017À"@ï\x0016xª\x00137\x001aîÕvGµ­¿u}\x001f¥&ýèù>øÈÆ\x0005Zî\x0000áHT\x0017ÛQ¶]\x0000ø~t- ì"\x000c3Ó´@GÒ\x0015\x0019\x0006(\x0002±S\x0004dº\x001a$\x0000´§\x0019 \x001aÒåÇOaL!Ø·\x0005\x0002N!
\x000bÔ!G\x001bJ?{ì\x0017Ó«ÃÇ·Û'Ì¿ºúû?\x001f;_Bã~\x0006\x0006x\x0011¬ãU0M:8ßÍspç^RiÕ\x000b\x0012©å Aåàòb8!yv!XïI\x001c¥Ú©\x0003;tG\x0002Ñ©x 8z\x001f³&\x001dO\x0001á£^\x0010\x001bX>qpNnO\x0015\ ÷m«×²\x0011\x0010!¥\x0001\x0010î§`¤ùÕ 8ª\x0000ÃÞ«\x0013)`\x0015µ\x001f #âh_\x0004_êWl4Áo²õÀM\x000f\x0008*®Ï	8vr\x0013×Ôç\x0005\x0013¦	\x00086\x00192\x0003j¦ñõ	$W(\x0006o´\x000b\x0002Rj\x0006$Õ`7ñ¬È\x0004Fª²\x000eñÇnÂ¿°%FÜ\x0003\x0002ÿ53 ©à@°[! ZÁI¼"ÛÕ= °f@XKY\x000e	ÄØ\x0015\x0008w-§É*fÏ\x0001YÅ\x0014óÜÐ\x0008¸Ãæ\x0014Þ\x0010"+\x000fÆfK(¸\x0003\x0004[\x0004Ø\x0001Yµy$q\x0002\x0011¦Lài\x001e\x0003\x000eA¦Þß\x000eÈªÕïÍÝ9«:
º:ã`£iö\x000emµ\x001dU\x000bv&{ X±H#uBTìrÛ\x001aH÷Ú\x0001Yµà\x0001ä\LLÐ y!\x001a\x001eY«ê¦C  ¨v@XÜ1&GH-!\x0004\x0017òX¥·\x0015í\x0004\x0001}Ê­½WÁuEß\\}úù\x001d\x0011l\x001eõdÆðìÁB85$ª\x000cô\Ttröý}C;
®qt'Nû\x0007æ'?1\x0019c¹nv"©iLïâ\x0004
&Ââx*ï\x0004\x001a\x0015Ëâè8¶Æ±8A\x001dòÚXN*2^ð¤2Yw¥\x001b¢q5ëÝ*áU^\x001cM£wmX-Îz9Z/¯q|ïâpßì´:ÒlÊ¨(YwÌ\x001d¢	5Mè¥\x0000\x0006>$¡sY2-*È±Æ8ç¤Å¡\x000e° ùV¢3QË[BÂÁ·ý<84YcgÜ¼<¥¥¸Îå#\x001b\x001cÙ\x0013)Õ\x0004Ç°\x0012´Â\x0014­S÷î\x001eâit²ìRÊ\x0006ÿkèJñòp¶\x001a¥láðÂ#\x001b-(»Ô âxòi\x0000]	ceY\x001eQ=3ñ4Gvi\x001eLæã¶ÄCC¿­EzìDÍ#³.»\x000e;òTÛe¸]h©¥Fi8ªÁQ½8Ø\x0011MºæäÖ;VÂLäÑÍa×½Ý[rw$¶$ãäË°âÑ\x0013]\x000cÝ.Ý{ºÊ=\x001b\x0000G²¡Hý§\x0008GMT>º9]º÷tEMmë¤ÂöTYù8YÌº\x0010\x0013OnNî=]Ú¥¶KrOnÄYw3\x0006AÈTÇAÛåårzxü ô¤\x0012­\x0004ñ¤»ýB¤yî\x001eÖpÅeÔ]z%¶i\x001bT®J
Q Òx\x000fd÷ÎÇaËáo/\x0017Ø-Z<ô÷w\x0007'_Þýý]%×Ñ2iØø¢\x001ceAÂÆÆ\x0005RÐ¿9?8ùñÙÑîT¿B¥k*=@å\x0005µÔFòs¼QBò\x0013iõ,9\x000cej(Ó\x000få4%V`í3+\x0002,!¤\x0017e,<\x000cek(;°RÎP®\x000c¬\x0014?¡\x001a\x0019©»\x0000vÏ3Ó©\Må\x0006JI¦²ëú@þéeUé!U¾¦ò\x0003ke,gR\x0018l×ªL\x0013ºzë\x001a
5T\x0018X*ÁÝ\x0006¥5îié¦MK¥«{Ú0U¬©âÀRå4Ä\)å¸æ^\x0001ä±~\x001a\x001e¥Z]J
/%½X\x0016ÜÂ²Öbø;-§K­\x0006×IMÇ
\x001cX-IEeÖS\x0016\x0001>pMY\x0015¡\x0019FjÔº\x001cÐëÖùb\x0018X³$V\x000f 5Ó¥J6j]èuÁ]YãÜrX*t\x0002NÞ\x000cªF¯Ë\x0001Ån¢wiÑð¸¼Vºä
Ù0]ÊF³Ë\x0001Õé)$WÞób;ÊåÝ\x000cYo4»\x001cPíÖ¤J¼XÜÒ\x001b¼OîÑ"Ü\x000c#\x001b-*\x0007Ô(ÆÓ9/\x001c´\x000bÅz¡\x0001>\x000cÕ(Q9 E\x001c½Å\x0017\x0010O[è¸Ð0ÆªuÉ(j´¨\x001aÑ¢X÷I[¯{zÕv@¸\x0019Â®\x001a\x0015ª\x0006T¨Ã&³d\x0006áòC¸Ë¥á]©Ö;\x001eQ£Â\x00175\x001aRì;­,íu\x0007Áa¬Fª\x0001=ê¦Ä)/ZF5\x001aÉê]Ì\x0011¬Fª\x0001EE\x0015\x0014¨³¡\x0018`Ë1ôrl5T(R\x001d¨Þ*å²&Õ],\x0011flb£IÕ&\x0005\x0017*gÀbñDìXDKÍØÃÆGV\x0003N²Ókä­\x000cd\x000c±.E«®¨\x0018Æjô»\x001aÐï\x0006ô!¬¨ò^ûRþ%ü\x000c/Y5
^(x,$§+aä\x0019RB\x0014ª9/Ýèw= ßÔüàp*`®óVpÆxÓ·P7*^¨xpþèU!]
=ÝtÜêR8\x0003«Qñz@ÅÃý\x001eÀ±¦	C³\x0005·BÚD)¦ß
u\x001b\x0000\x0019Ðð6rSR¸\x0016zvh|9zúõK7T\x000f(R\x001bdÑ
VS¾.ÞöËõKÏØÁFê\x0001Eª"\x000f+Îs
»"w{4~\x0006V£Iõ&Å¦4´à\x0007\x0006r
¥\x0011à0óé\x0017CÝ(R= H%Øhr´¼­¥çvJºéfG7T\x000fhRéºêÉ¡U\ig\ìM£IÍ&¡¸ÞÚCZ+ÇR3â¦Q¤f@bø1ð\x0015LQ\x0018\x0019n³dÙ8}\x000bM£HÍ"(ïÙ¡IñÛ,ðXÏ%ÚÓ=xÓ(R3¢H¥ :GX,CÅØJaÝbl\x0018«%\x000f¸ÊØøâî>(d\x0019N»Òø"8\x001d«Ñðf@Ã\x001bLÓàP§¾¹X\x001fÂ®²Ó3°\x001a
o\x00064<f@dú"Áâ×\x0000­¬\x001eM6&5#T)~\x000bØ\x000e;»Yº´ÐUÎO÷\x001cl£³ìÎ\x0012¥è\x001eë0\x000bvÔi^«9²mt\x001dÐYü\x00069ÓYª¼b\x0003-êqÃLÂ²\x0003
Kàûr^(\x001d)ä µâêEUÏ<\x001a¦j\x0014\x001dPXXGI¼^\x001auQq&N×W¶ÑWv@_a£öm	ø\x0002</ÚB-ÃtínÛ×¯\x0001}\x0005F\x001a½Àb9Ê5ÑN\x0017'+Î¾ÛF_Ù\x0001}s4\x0012þ\x001a÷J§ºF­í8m\x001cR;àÂÝÃ3\x000e¯d	\x000efI=#e\x001b=j\x0007ô(ö£¨;ÍÈiµæÄØlãÚ\x0001T<\x0014,SÍéÚ\x0006Ãm\x001d.ð®Ñî®_»\x0007ÌÑ&í\x001e­¡U­bÑ¡\x001d\£ÝÝvÇnÉ¬à\x0003\x000f©ÒÖñÛ¸áÌ¸F¿»~ý\x001e¢õ4VÆ¨¸\x0006\ò\x0018\x001amôëªk\x0014¼\x001bPðØÖ:V^hJ¢ÖXz@åg\x0008V£à]¿\x000fX\x001b© òÊý§5Çq)tvw\x0003Ú]a#\x0010º~II­fAyR.Ø\x001c5CÚÛä~í\x001e"öuÉ-@àbÂO`RÑha¸LÏ\x0008d¹F½»\x0001õ\x000e
\x00010òjaÅ ]ìÙ\x00113\x000b]£Ü]¿r\x0007Ç.7À\x0011.rhMxöû¬a\x0007]£ÙÝfÇ&$î^.²/cTqëöö£X¾Q¢~@\x0007C\x0012³z\x001cm è\x00036Ì¸ÖûF]ù\x0001u%Íê\x0010ñ\x0011´ZÂrç5c¦ß¾|£\x001bünÊñíËÇâÌè@9êZÙ\x0019O`¾M1\x001a9ãXAjöü°S#ß¾fh,ßH¼\x001fø4.K|0\x001ak]\x001e*Ò<Á©X¡ø0 ñÂHN¼\x0008Nð{¡*é<ZN·¡\x0011ø0 ðB¦ÔD\x0015yvÆ70¢2fú\x001eFàC¿À\x0018\x0005çiGÅ\x0003Ap&,{~~ÆcSh\x0004>ô\x000b|ÀZ=\x0018EG¶ØUÌñ\9fulÆ\x0004gDY-<ZñAdsèg$ :\x00078¡¥\x0014àþ×{ÃÉÉÖr»?|½//\x00033\x0002GmÚ4=Ðaã\x0001~MÑ<xW;Ç^³s^SÜ\x0006\x001b¢Ã¹Ð´vÞ\x0004\x000eÚXÅq\x0008ì06ãÉuN\x000cÑaSÐÜ´\x0001»"R)\x00061¢nÞ \x001bÃ |¾ÐbNµ\x000eSÍùdrJ¨DHØ
H©e¹t`qµ¼ý²\x0006©åaRÛI\x0007¢ïb\x000b¿8Yþ¸\x001fDÕ ª\x000b$b-Àyà\x0010§:'qC×\x001cº#\x0008\x001d
kC\x0013Ê8lí §\x001aÄ|½\x0005±5íàÀp\x0015÷\x0019áì¹à%×mÙ\x0010§¸\x001aÄ}½\x0005	5GèáÀ\x0011Ìá±\x000b¥ª\x0006¡\x00016\x00138VÙØéè.\x0010ÏÆ\x0015îp\x0015\x0007 \x001d\x000eNø\x0015ÍÙ]×\x0007ö 5\x0003*\x0008fµ7ÆO!iN¯ì9¾Z®~Z\x0015õ\x001a¢âªP#Ý\x0014æØÈ®s£\x0004
"\x0005\x0012Éè!zP#¦\x001bÙ\x001bÙupð5ä\x0004nçÈ\x0015fý$mNì9:\x001a§Æó\x0004jugBÙ\x001b?Eµ®\x0012\x0013GìáÀ\x000e,%UIÔ\.\x0017L²"ª9Ãªç\x000cká¸Ä
¥ú\x0007vÜQJ¦¬j\x001c\x0001Õã	`ß·<AÂýúahJ}®uS<\x0001Õz\x0002=Ú\x0004|ÛâH,öRyþ\x001f\x001fº@h\x0000¤Q&ªKX{HÒc²YJ\x0002ï¶7+ z|\x0001\x0007næ\x0015á\x0006°$÷FI$VS=Z
+¶¨Ê=å¦\x0013læ$\x001bÂ\x0014F©©\x001e¥\x001cs,\x0005gUzV¯¡HÉ´ÍiêRjÊÓ¨L ñè\x001a$1\x0011E^Õ4eÒ¨5Õ£ÖÌ*{ß`\x0017GÚ\x001c[\x0006k9=ÅäèF­é.µ&\x0003?\x0008k¹\x001a]Ê¯çØ×p\x0012I£ÖtZ3¾¨5ã8ñÈ
\x0010\x0014®ßj
I£ÖtZ\x00039¡;3Ê	GÁeW¡®Æ\x001c iÔîR'çm\x0002áäò(¤ì\x0014
«\x001bu¢»ÔI0¬êã(\x00151r½É$ÏD7êDw©\x0013l\x0004¦WKÂWµ·$¾!ñ\x001d$Vp	&[ìóÄ\x00158rÒ4zMwé5í³&4;kQv8ÊN¹^F.mây yr×,¸°r×¦liÎ°é:ÃÎR\x0007½ìÀæNäVÉèÂN±¦\x000etaçø=\x0008×ÄÐØbu¦¹°¦9:¦ëèØÊ,8î\x000b\x0014Méÿeì\x0014ÇÑ4\x0012kº$vT­á\x001eÈ
\x000f±\x000fS®¡¶XÛ%±Øi@"eè\x0018K )\x0002k\x001bµ=\x0002ý´	$(¾úÅÈÚ$D7ÅúÙF^m¼\x001a¸è\x0008Wl¡'³¦\x0017Üà¢î£;\x0000Ò«í\x0011W#\x0002=
êh©³°MO ¬°m¤ÕöH«Që?S\x0013Ù\x000c"K\x001f\x0004\x0011§¨W×\x0008«ë\x0011V\x0003·\x000bRô8±Ê$K=¸t/w¸.!¦_J\x001aìIX½F%¦Hkc]R"\x001dÇÖ\x000cè!1I´rp\#&®OLR\x001dnnÁáF\x000b·H&1vÉñø>9«9bJi`MBéF1E`}£Ô|R¥øÝ\x0015æ3Ì\x0003ÄTê\x00190¤\x0011Xß%°°\x000e96óaò\x001b5ÜÙ\x0008Çzû\x0000H#¯¾K^A	"\x0001ÓçÉm,þköã\x001byõ=ò
ûÀe¾\x0006¼¥ü\x0002\x000e\x0012Ôïã#¡úÕÂ\x0015ÜðiÏ\x0016YvOð~\x001cÉðhÄz¦ÐH8i\x0003H÷\x0001¡kÂ!¿UûhJÈÏ»)JÎu oú,\x000e\x001a¦¡XÑ7Ìq¢RîêÀóùâv\x0007ÿf?-MJm´ÔvÊÊ(W³#²¼\x0004ÿ¦~\x001c]¤;È'¯·ïpbÖÉÝõÅÕÕÎQ
§ÉS\x00133\x0013)ágCíY	Ð«Åé³4-ëüÅÑÉÉî\x0017Û\x0002¥j(Õ
¥Á(Ñ N\x0005~DZ"\x0007{F\x001aÐ×q¸a&]3éþ2\x0006åÂ?¼Ju²÷Õ3á0©ÌW]%,'nv.Õ\x0017¯ò¡\x0017×o.¯/îlyyýùàèÏ»_ÿþÏ.qÇ\x001fçìá4Àü\x0004 àÖBçÏÖh)#`ñâõËã\x0017i.ÛÙâøÅë£ÿ}þêèÞSIÔ¦¦6Ó©=¸¬9=K^%\x0007	Ìç©Ènshútj[SÛéÔ\x000eÛ\x000c§û»Âþ&9¦¡âRÒ\x00107Ë\x0010§S»ÚÍXkligJl-\x001bóZ\x001bÒ@`E6,§SûÚÏXktæ3µS\x001as¢Úknq\x0013·d;N§\x000e5u±Ö>R4_ÁU²Êa­é~¨´\x001bYaÓ©cM\x001d§S[@µ9ÅÛ\x0019ß¤<·G5â\x0001ÅZ6\x0002"§K*æÒ|#R´\x0006.\x0013áfÖ\x000f§÷d³ÒrúR{,Êyi8s\x0019ÛkðÁýÁ°«\x0017e42b\cÊL\x001eHEdÖ|f\x0006ho\x001fN]W¯ÏH-g,¶äV­:½OÛ¼Ø|e¸`ÈÓ|ªµè3L:\x0016~äDoìéE­0`±)¡}x@Õ§\x001a®æØtp?re·&Æö(¢7»Nnl£c\x001c¥!¯SáÀ\x001fr#Õ\x0007ºq3Qv:vcfÔ\x001c;#<
AÇTr\x001eKw XõÃÖ\x001aÑsÔVÔ=\x0008\x001f©Ò7
Ub\x0007êádD7çQÏ:Ü­[aë1O]\ì(Ä\x0003b7¢­ç6ÇÜVa³À|óÄ\x000cT¦Þl?4ºl=C²±afo(«h¥K\x0007\x0019¬y0fÓµ!ÖØ°(]¦AL.Ss6{Tn#}:t#ÕfT;Ã6åU`Íç	äôÅÍRéØíÅqAQÖY>|\x000cØd\x0001± £Ö<mÃhf\x001cF\x000bp¹>\x001eÅkãr\x0011èþpÔÍa43\x000e#¶xË¡r¦Ê\x0017\x0003Gaa#ãfEñdjÛ\x001cG;ã8Z!Ø
Zb6RÛà\x0014ao6GNÝG;ã<b¾FnSIñl\x001b­£÷\x0011ì*ôpm\x001b\x0011±3DÄ\x0000\î\x0004×\ÍjÄòSQá\x0001=\x0011ßG?ã<
§èÊ-~¨òT	E\x0017\x001acý\x0003^\x001f}³Ú~ÆjÃR9u*5I6]Ô\x0000Z[<\x0014vhNd~"}ü>³±\ÌØÒèp¨Ç\x0003b7¶&L·5>jACà²¾
1¬îêêád$4¢\x001d¦¶"Ô\x001a\x0007\x0018ºõ\x001aÆv\x000f¨µC\x001b9.Ú>DOU \x001a\&ò¢$v² ì°YÐ?#2Ò<wåèHU7îlÛH¡\x0006Y^&{®QÒ;¡ö\x000f±æ1èæ)
ÿâIUª}ñéàÕÅ-üáÝÏ\x0017»æ×à¨\x000cêð\x0007&Qc´\x00125\)AN	Oë%Gg\x0007\x0006xöýÑ=l\x0018P×z\x00100M³\x0005ø¸/\x0007àmVH\x000fâÙ\x001aÏâää;<8G\x001dýo³
ÏÕ|n/`s¡\x001c±QR
¨+%\x00188ß,_\x001d\x0004ô5 \x001f]@¸X\x00160Gå3á\x0001W0Ôat\x0005cñz-^1ò\x0002\x0016¯7\x000f=Ç\x0017k¾8ºØ\x0018&\x0005yý\x001c7dõË·*'L\x001aF\x000c\x0002FìâU\x000cö¦\x001dmõü°¥Æ a«\x0003G v\x001bPR¡óz¥eü\-³*Ljt
W8( W\x001e8ø¢\x000b£0!÷QÂFMËQ=
`	k¨(ÞëJwk\x0010ÃÙl\x001a@3\x0006¨@O\x001dj\x0012C\x0013è1Î§7-á\x0016ê)£¶$XEEÉ i\x0004E\x0016]\x0010¡<rni:HØ\x0018\x00139hMà²;\x0015N÷ÈUl^H\x000e·À\x0005x®55£æ$\x001aÇ\x0011)ÕetNx
&Ï\x0006l¬\x001c4'x©¤Þô°\x001cDñB\x0017B»ù&<JØØ\x00139jPÀ# ¦cé ä°«lQð Ìu	UcQÔ EQÂüÖ\x000bK\x0018ðâÐ\x0018>Év¶®QAQ\x0006Ea¿!\x0015\x000baNWð¢¼ o>5\x0008ØØ\x00135hO`\x0005-¥ß¯ (\x0011\x0018\mÁ{ìÄlÂÆ¨A{¢pÄo.4GwÞ´¼àÃfkïAÂÆ ¨a\x0012xö Ø9EºÆ³[¸¥£Î ]cLÔ 1QØËó\x000es@\x001f\x000e-;¼¥'å a£ªÕ ªVØ«I\x0010fìE,~óýo°ÑjP\x0013Â_\x0006¾8¸<å<D/b¯kÛÔ1BÝhB=ª	¥Ñüþá¢¥z)/=\x0003ÆÙ®µn\x0014\x001eU4\x0012»\x0012Ó»ÐÔ	\x0000.Íü®$ÅlE£c¬G1Ü@ù\x0015Ú®	^	*\x001b5RÎöºtãuéQ¯\x000bÜ+ª'Ux[¶D(Y×ÀaöõÄ×\x00110ò¼êNT}pÅª`«Äì¿zÇ:q3¿fXc¯c*3©°Ï$«Æ`hÆ\x0007I-ÇZÏÉuP=\x0005Ô¹"ÒQW9¯¸¿\x0017¦¯!7V4N\x0000ÝÎYÿ
sQè\x000cIm\x0018TliËÜ.oß]üºAébÙQåGÿãî
ø-ßÞÞ\íÅF\x0014JêE\x000e\x00107\x001eK$´7<Î|3¾ôó\x0013{¶xzúòd÷
2®Ùô\x0018\x001bÜ§h¨²²Þ
öý-î\x001b8\x0006gj83\x0008'h²B\x000e°n¥TÁo^\x0003ÆØlÍfÇØ\x0014¿|Ie\x0002\x0017Åâ8+\x001b·¨18WÃ¹ÁÓTulù\x001aotÐeá6G\x000c±ùÍ\x000f.\¤"3¥%·&ÀÂ&®bØL©\x0019c\x000b5[\x0018\7ÇÍO°üF`bV\x001eÁ9;sáb
\x0017Çà`¹¨Ò[×%?V.Þ¿r÷*¸U\x0015Éª\x0010k¯\x0016É·M@ã\x000eÅ¨EÊ¦n¶\x001cZ·Ux5ÑÉá£bm¥<µmseá6cFctqÖ¡R$ð¹\x000eÕà\x0018H¢3CjÇè\x001aó \x0007íf÷\x001eè$½#ÂÚÅB·\x0019\x001e£kì\x001c4\x0010°`ÔçDá\x000f¶^­Ù|;\x001c£k,\x001c4\x0011_á_0Tùg,ªÎÈ
d®1\x0011rÐF`ÓÛ\x0004=þ©É¡)ÅdÉvch&ÂH q²` ããªô<Ë*\x001b\x000b!\x0007M\x0004\x001c\x0008*çÁQ2\x0017lªà\x0003±e,É\x0018]c"ä¨\x0008<G2<\x0016\x001fÙ3\x000biDCtª1\x0013jÐLÈQ\x001b\x0002\x001dM\x0002Ë\x001c\x001d\x0008·etù\x0018]c&Ô¨øo¯]{\x00185\x0013[Õ!\x001d/\x001d÷xt[¦Á5VBZ	Å-\x000cd.(¢å¥³ÃKÆè\x001a+¡F­Däy	î°-k§xífºÃªÑÃjP\x000fKâyc\x0015ì6Øtè6û¶Á5ÚN
j;ÅU°±f0%+á¶\x0004éÇà\x001ae§\x0006\x001dvÖÌ\x0007VÀÙå{ui­	B7o_u£ìô ²\x0003wêÇ%L,¾	\x001f	3OèF×éA]'\x001cÕFI|Q|µæ\x001edÖÙt®Ó£ºN²K\x000cgû<éh:\x001137¶\x000c*;a\x000e] µ\x0013ôø\x0007kÇä¬Ý\x001c\x00031F×(;=\x001a3ñ<\x0016ÇU\x0004¾	;\x001dæÙXÝ¸ÄzÐ%\x0016Ç \x0008¤ãP\x0018\x0005>5Iåct*Ö£a\x0013Ë\x001d\x0011KO\x001dXÛéÍÉRcpS¬Çâ9ËéP\x0018Kà\x0004gxòÒG¶1\x0014z4r¢9Æ¯´](þ	ÎeE×X
=f)Bä\x000bÀÑ26ÖFR(VÎ;±¦1\x0014f4x"Ø\x0001\x0010Þ\x001dr°N\x0015srf@Ì4Â\x0019ÿúÊ5vÂ\x0006Ö¹6O#\â<1ÀÆÍ©Äcp0cfâ¿¾rm`}ÐJ\x0008\x0013\x0016ØuE\x000f\x0017ÏiÞmÂ4FÂ\x0019à5¥k\x0010bQÃÜÀÏÍÊí1¸ÆFA\x001b\x0001f+'ñÁÊ	\x000e&\x001aæmõ3='Ó\x0018	3h$\x001c?Ôà\x0015å\x000bÀÒñsÑ3C¦1\x0012fÌHàä³ü(Ey¤µ£rZðfúÄ¦1\x0012fÐHØHÑ	|~å¶ô\x001a¶\x00133åÎ6VÂY	T'ÔItÅÀZ\x000eÄZ³Y×6F×	;h&¬¥â]\x0011¤£VFKKrýgæÑ5vÂÙ-ZC^»`x6¶ìØ-³9Çè\x001aCa\x0007
åç	\x0015ÄvVRï\x0004¬ßwfmc)ì¥\x0008AST\x000cÌã ¶6+3¶Å5F×>Â\x000e
ãé-<&Ãe8Á!;mçnlc*ì©\x0008APÊ¼V·uSÄNl¦ÌÑ5¦Â\x000e
` ©óÜHÒh¢çjÆNØA;á}N¡\x0016\x0011a(èd¸¡¿ÙR14\x0006×	;h&¤®¾Â[ÍÓvT¼rjsXà\x0010kÌ\x001b4\x0013ÞæÖ\x000f"
#+ñ:³¥\x0006b­1\x0012nÐHèHCN\x00046^¡`¢
,6\x0014E×\x0018	7h$Àë$uØ©\x0004çL°ÙTe\x000c®±\x0011nÐFh_Nz*¢¥3D§âfÂØ\x0018]c#Ü p:úóQÈúk\x000ea\x001b7Sê\x001a\x0013á\x0006Mvô
+0×N\x001bZ:\x001eòÚGÌ¢k\x0013u\x0006mó\x0014`\x0017Qè\x0012êäb\x000cXº\x0011v×(b7¨±Y,_'Â!Ý&\x0014\x0015,ab\x0016o4\x001fÔt8#XÒ-Q°\x001eÖª\x0008Ý¼uó.ñºÄzª£\x0012ÁYêªC×ù\x001a¶¥\x0005Ï\x0018]s\ýàqµ®8ë8\x001e\:ISÎnæðÍð'Â
2þA²­¼©bæ=Â7ÇÁ\x000f\x001e\x0007ÍöÀô+êva\x0014Çµ2óÎChÎC\x0018<\x000f8ÁÅe8%ø\x001a¡JÒ3½M\x0017êD]Ò&U¢nß¡\x0015ôd'ÐSQ$z\x0013ÅL=`ZnÇe\x0008Ë°\x001cMï §(8\x0006U\x000cÝ±'Çnì©î#Nñ'ü!O¥L.ÀZ¾<0\x0000üc]BPfflc§ÍøNG,\x0018¥XáÙBÚñ\x001c\x001dkgdã7 ý¸8rHÐßjÅ#æ»n\x0003Ò¯d\%ð5£få\x001aÍ!ç\x0019uHo!­¥\x000c\x0010ÆÏq\x0010s,Ü,¥\x001a¼P®CÚq\x0004\x001f"-Ñp­\x0012^,Ù,ÇÉî }Þ®i·cÚÇðVK¬Mã\x0014$YÔÏÌ¤r§6t¸\x001a_EÉ&âT`rnÊ¸Yã7ë\x0007BÖ!ÛÞG5 =ªøµ4ðà\x000e»Ù²vÐÅÙ83ã\x0007Û8ª½\x0010\x0001Ë0È\x0018bT¦3-¶ÜÃd(=	»µ³ETE$÷8ÚÛ³ÎÁj«C<j<åäæîòÓÁÓ«¿ÿs{yóy\x0007XÀ \x0011çJi±\x000f>aè[öÊÅ¹\x001a'/ÏÏ\x000e\x001c\x001e¿|½{íÌÕdn\x000c®Ã>wQÅ¡¬dØVªçÓÖ­Í\x001f$\x000b5Y\x0018[³ÀÃ\x0019â¢\x0015ÍMzYk>Æµª @.)FÀð=2¿n(\x001cHó4&:\x0010¯Â\x00044Õ ©!4,ÁÍdg,h)#7ÒÂG§\x0019dÍ\x0001C'\x0000u\x001cõ@/ã´\x0014t\x001dÑÞT\x0003\x0013È\x001a1CrZáS\x0017kpYr7C-5Ï¼	RÍY4Õl§\x001aÚÎà\x0005=Ë£Í¢ <\x001cN*ñÁ¶s\x000ejöSi4\x001bh?E¡\x0019ÉýÊ­rsÈ\x001a¦Æ4åº(\x001c·HÖTã$SB«[<M@kDM©4ËE\x0016ÊâõVM³æH-ï¦£éF©éQ¥¹\x0014§F³ÜÑIIK\x0016b;þ	ÿâ	~~w»ÜA\x0003\x0006\x001bGVR>ªüçí*÷¾Áy~~ºx½Ãx3ª\x0019T\x0017çÛµ3<åÕ[S\x0018ÖÄ¨\x0007B×\x0010º\x000b"*\x0004pei^´·Ôõ\x0001[Ta
SSN
[ Öæx÷0¸Áu0 wbx\x0016ã;ºó!¼[(öÊ¦¯A|\x000f\x0014/¸.V£Ô\x000fxíý\x0014XÄ\x001e\x0010\x0007»BÙ³9+X®îQj\x0004d	¾|sR\x0016èÜÃÎ>»üyÞ-ïv°àh=î­£þrz{ÄÆ£¹¤Ý×Ó	\x001d¿N;OÏ\x0017çûqt£»p°ô¶¥\x00120j\x0002bB÷4Fcj\x001aóÕ\x0017ÇÖ8¶sqÁ'ô´82
FRbj©4Û\x0018«q\\x001f\x000e\x001aÅ<Ø[ã\x0000ö\x001357
\x000eºê80Fãk\x001aß¹8S\x0012M¶<ÑNEáÿgîÝõºq,á©\x0011(H×¨§#ùØ©\x000e]Üº8ªú¥â8­ÎRRê¥ª~êiô\x000c:Ç3ùGò\x0013\x00007¹ÏEÄæÉJÕí¯©Øà\x0002H\x0000\x000b4\x0014q\x000eNêá¤IãDlßªÀ©=è\x0019Ýn.\x0014êàä\x001eN´N¹ïÔÁ.t9pU<K+ùèIGn÷±

ÝÇæ<9Õñ|¤Ý"U²|@Å»\x001a\x001d\x001c;À±pRâÒ2 ½e<)ÊÁ²ù,í\x001c)\x0017×0T¤­xJÎ®Ìª\x000fåkÁÉsn\x0007N¶s¤\ÒÈ«\x0005Ð9YÍi¯Ð`8g`e;GËås'E~«Î.\x0006/ö1'Ç\x000e´lçxÊ,´®¾Ig/¯ûÔÑq\x0016Ì@Êvs&Éb\x001c`M¾ìäJP|9$\x001e;Ð²ãe\x001a1dA\x0012C\x0013«à\x0018*\x0002w1û³Î3ð²#fG\x0013A^ÎáWL+¹Å>gS\x000c;\x0010³cæb\x001fÇÃJHû°\x001dãq^ìsÒ{` f#fÊÖIócC\x0013\x001d?÷doeg\x0001½ÆÄ303Ì13­r¯â<%r\x0006nÒÏr)'>µÎ+Ï&Ë\x0008\x0003-\x0012±\x0015\x001eÄ\x000e3ð L§§±¶á¡£G	¦e\x0014w1üTÖv/ú\x0012HépÎ°Ò,*¤=\x000b\x000c*gË\x0018­ä?h¶2\x0001\x000fO$\x0001Û\x0013É\x001fÞ}üüþâñõç_¿þþû\x001dIæØÈ§%¦®½®	vÙÃÖ÷?\½xõôâñå«Ço_¿¾gÙ² \x001e\x0019¨¹Èµ\x0005k£\x0017ÅKn	KÈ°G*dôfÉò	)HãNÖ^4\x0002Þ\x0007í\x000eu"<ªa{_ýÒ:iIhµ
I4áÚÇô=4¯<KaÀ";Y:j4y
Xè\x0005\x0015°hE¹fø\x0019Äy¬æÞOùMd±G\x0016UÈ¶\x0005\x0008\x0015X®um³YÌKÈR,é>&6hd¸ÉEi]Æ®\x001dÍÜCËóÐ(¯ò¼be#\¡ycr³]¶Wþ6¦5º\x000fºõZ×7á¦£W.\x000f¢Ug\x000c,a\x001b£"\x000c¸-Ï¯Fsü¤Sâf\x0013Ñ£1\x0015`C\x0010°(@\x001ftÛlV\x0016[Z23óÒ\x0001µC\x0018°8à(¤7j7Ù>YèÖ¶sà 
À*BA5¨b6ÖËÉ6«­¹Ú\x0010	¬"\x0014Õ\x0012ß
·(Å¢\x0012\x001edª$\x001a·m\x0008\x0006V\x0017
çvfÛI75»¥%f³CÊ¬Ñ\x000f¬(7äØÎ®ÅÑx\x0017µðr\x0017\x001a"¯h*\x001cç[8MKg¢\x0018°o*Ý\x000cH?è\x0002¾×t\x0001¿©Ùs\x0011"e8
aÏýðáo-w¯\x0017Ï¿þ^þîn
¶Ô>_}ÏJ_¡7"T\x0013rß¡ùìÙU¹\x001f¼½xþöõÕ\x0004(×r\x001aPQDs­OläÐ\x0010\x001a¨^ØO	*ô \x0002\x0014 ¿²\x0017PmjÎ\x0003JqµW\x0019VbJ=¦¤À_o\x000b&ÙTí<Jî\x001dR<ýõö¤@QÒ1*ñ¤WAeùvî¼4Z\x0014TÞF58ºÕxºk
ÓÖ\x001bióõmÐ6¤ón\x0007O·\x001aW/\x0006\x0012W§Y[ö*WÁyT«[¯»¦\x0008D¹MqC\x0015(ºÅ^FhDuW
ýÐô´AÒ¸zð<cn©¬Î_/(¶\x0013\x000c\x000e\x001aO/©D4æ\x0018ç[à	1Þi§o¢\x001a)]ãét\x0007áë\x0008z	>5i´>`k¾\x001e\x000cn\x000e\x001a7Ï<q\\x0010%\x0011õ\x000c6¶¯×Ï+í4x9(¼¶\x0004p{ÅÖø\x001f
}
*sþë
\x000e
G·Næî
*Å\x0010e(0ôÝ­JT8x:*<\x001d£ØÊòn5\x0017\x000c\x0016\x0010Ï£\x001a<\x001d\x0015n½,9²\x0016²Èì4AÑ~\x0007«\x0012Òàé¨ðtÊà½mXhëbePá´Sáàê¨qõyÑCr´Ù7T§³\x0017\x001c\\x001d5®·w9ìT\x000bÚ\x0001´§Ïß0sÃtµµæÏb3
+¶ ÂÜA6FB\x0018\x0014µß±¿Oð·ÜÔ¦
g\x001eñóDÉJy\x001e<"6\x001f³ç=?\x001c
Ag¸ä¹D]\x000cWò,þ¨ÐÞNµTà¼ócÉÁ\x0002Ö?ýÓ{÷ç÷\x001f©\x0004òã§\x0012¹þçõ_îÄåå\x00035)s¦åMàMJÞú¾µà\x000fWÏ¾ RÈ/_=¹úñò	pØC\x00058A¼âÕ¡±mr
xd¸ ë[x\x0014àèEa°\x001cý°YîS-\x001d}¸¾xõî/ï>|¸Óp!0\x001aÚÈ%\x0011*ýñIH®{A|ò²V]^¼ºúåª|ÞoC\x001e\x001ah EZ"\x0011Ze-úmú\x001b,;\x00069\x0003
{h¨\x0006ItÌ!Ê5íëâ0L§:t\x0006ë¡9\x0015´°\x001dË
\x0015]_OÏlµ~tô\x000c4ßCóº\x000fÚ\ôAù{¢oÛrÂÑB,èæD\x000c\x0019,pR]\x000eº2ëâú\x0019h±\x0016UÐÊmM AæÛßdü*´pê|LËHº\x0019¼Ôy¾þúáâÉßþú¿¯?~¼ûÕËn	Ò²G\x0014]0®cHãÃáÏo]<¹ú\x001f/^LÀ\x001e\x0016h`\·ðn[mÑ\x000b7u¡]Â=.TàòåÞjW\x0003RÃö6Ñ¯#å
pÑÁ
=¬ E\x0002/µà\x0016£<2ApÜ¦ãâ¡ð¦Ãz\I\x000b\x000ck1"]¾YëÆy\x0005W°çqíÏ_×\x001b\x0005°Xª¦Xþ\x0005®;[Ñ¯v\x001eã½`À\x0005\x001a\®îªª-E¾>¡` -E\x0010Që×\x000e,ñVÖ\x0015Ã?»¾øùÃ5ýËïß]<¾¾»6Å"Ò\x0007%jÖ
)Yéu*)Úîø¸~~vùâÉË\x0017O¯.\x001e_\x000eãGHÐCï\x0002\x0012öð»äzHî»ä{Hþ»\x0014zHá»\x0014{Hñ»zHI\x0005	=ÕTdjÀnÑ/Ål¤y·W®¹\x0005R}¸<âÉ=ü=\x0008\x0006ß¨s_ÃµúÒðµú
_|úz_Úiia)²\x0008Wµ!ø&sÕw1m/^¾½?ål \x0007\x0004ÊÍ.d²eqÆà³4È¹\x0014ìY<ØãÁY<17r\x0008Åj #j\x001eýèó\\x000fÈÍ\x0002*W*Ã\x0012Ñ=ªx¼¼;}ögñø\x001eÅCë=Ä@Èr,ÁCÓ«\x0006\x0013Î\x0002
= 0
(r\x000fx1á\x001aoð2W_,äóY@±\x0007\x0014'\x0001y\x001aò`@\x0001yEkp¤FÉ\x0016:vÍ\x0003J= 4\x000bî,\x001aÛ¡w²µ\x0017\x0018WÂÉ=<\x000b$ìBS\x001dÈaS¡qæì	ë¦»ß§»¾	ÈÉV¢*ÍB\x0003\x0014Ï:\x001dIz¥=½ÁÊZ\x0013Ã­;´ÐY\x000e½t\x0016ÑÀÒv¦iÎ\x000c¡\x001d²Úr\x00120FCî´\x0006¶³DíRbù\x0017«dØ'\x0018Ñqºt\x001eÑ@Ôv©KºÃ\x000b_\x001b\x0005~9)ö=>§M40µ¥êâ·|§-&b¥Ò>5¿¶§½h`j;KÕ®ÐaæoVZ\x0003ÒgªpL³p\x0006¶³D\x001dMà¡WCB5Ð¦øÃÉÐùc6\x0010µejºâK°§µË\x0015\x0011$éwqÉ¶ÑÀÕv¬ì\x0008°²7+`[\x0012ìÒùX?\x000eíl)lÉb#e`°IÆ&\x0010\x001cN|8â\x0002\x001d.NfIê9©dkòùúÇSm6{Ä
\?G7îË}\x001f¸ò\x0011WÇUj\x001ehÞ2\x0014\x0013%Ei\x00199OU7ü>Î\x0003sh¸ønrmmÜø!·%\x0000Vë÷%E=\x0016\x000cB½N~øô{}¢üåúÃ»ÏÿyçÃ|ùpUÒ'»Ö¤à¢(` é\x0016\x0013?yöòu}¡üåòÙÕ«ù6*èQ\x0002UJÜ]\x000c4~Í
mX¶ÿ¸\x0005XØÃB
¬ º\x0006ÔwÏ½/­ EJ¿~\x0001ëa9\x0005¬(»%Ñ\x0008ä¤U¼Á]o\x001eïay\x0005,'êLHr¹­e04k­øVèa\x0005\x0005,\x000fuIH9wY\x001a9å4têW\+ö¨¢\x0006\x0015rÝ\x000eh\x0017\x0012K];\x0019Í¡(XzXIãZÀ·s *m®Õ\x000e"Äo{XYs\x0010
µ¨×rbú\x0004\x001eº@õ«	ãíãmoÉöZøäó§÷ÿA8?úz}²¨3¾àªU(\x0012S¯3¶ÞfþÞô¿Ï./¼zùô©\x0015çñ«o/ï\x0016?mÈ G\x0006*d6>
\èÌu±¼µI*Q}ú~\x0006\x001aöÐP\x0003Í\x0005ÇýØ\x0005Yæ´ËØ¹K¨DËû ÝÚ?Ûp¹\x001eS\x000c'F\x0011\x000bSÔ\x001dÛ4,'Åá^}^+ô¸
×.ÌTÈçKº½\Ïög¾dìE\x00152·Ë\x0010EàüÆ[eð=Üû!¿,÷È²\x000eY­¦{Ìç\x000fÙ4J²½÷;~\x000b\x001dùBG\x0018ÅLõÁTñxa²L+ÓV°
ÇÒªÎ%õFT%y\x000cQº¢\x000b¶ÄÜiQß
6?`ó:lÈ]h\x0018hÁ\x001cÝ\x0004[êZEÏ`\x001b\x000eÕ:¿E\x0001ªù³»%n*ñ¦\x001fM>-
Ø.@eéw	!
w\x0011q¥ìýR\x0018°Ã\x0011µº3Z¾)pðô$gÉÔJðÄ¥£\x0000Ã1\x0005Ý1
¹éêÆB5´&\x001bYM%³ÁpLAwL\x0003rk\x0015uåð GÁf$|öûeÎ`\x001b)è)	_×£Ü\x001e\x0010\x0002+ÙücÑnÃ1\x0005Ý1¥eKüM½Ý±qFT\x0002ªY
\x000b0\x001c\x0005Ð\x001db7/ØdÈìæ\x0004[Z;¥Ý+Túå;Êt\x0008A\x000bÖ\x000fp¾+\x001aÿÅnVÔLZÊE 	\x0012Jô\x001aä8NÄGìhïL:å&VPùAzHëz¾¾ûý·;_©J\x0011UeHå|­ù¼_ðªíFøéíÕë\x001fîy©\x0012XÐÃiXFöyk\x0003¤ÅE'mõq\x0001\x0016ö°Pa­Â¹h÷¦s¶V6VÎ\x000fbÝ:X®å4\x001f\x0011ø\¬eXÄGi\x0014¡Ñ\x0005T¾Gå\x0015¨çnb,'ß6\x0015	¬%×
=¬ UnTA\x0006\x0007<ëÜøD
"\x001dô=t¨R*i<\x000b\x001fñ\x0017$Á"Ç%£É\x001c¬u¨r*+PÑª\x001cfÅV%K\x0013Xç1íý¿\x001bc\x0019_Á\x000e*qE©øT"b^qw;2©J\x0013´ÙB²­ü\x000e+®k`R;O¥&àY¼`Õy1Újók³ì@¥VÃ¥´`a¡pVõ7\x0005_ðx;P©Õp©mx'8®FxZÒp­|ÆL­M-­\x001e`(Y¢Ø+ùf¯Ã\x000e×À¦VC§Á·á`x\x0019§O?Ä\x000c+°\x0006:µ\x001a>-°Xý
x¨ÜÉÛ7Ä\x0015P\x0003Z\x0005Ò¼9OúËÜuâ³mâiQa`.P0uFD2 \x0006í
\x0017¤6æWpI º\x0012AïëG¡Ó¶É2¥\x0005~¶@A[$Ãã·@¥çJ§Ù\x001bÑBê¥\x0016ô¸\x0006Þ\x0002
o\x0015:\x0015÷Ø²­ \x0013è1ù\x0015\\x0003o·h¡;û|Éq\x0012ûV\x0016Â\x0018\x000e¢e:\\x0003o·,U)C;|ëN©É}&\ñ¯8àó¸Ê?·,"\x001aÒ\x0019¡¶\x0001R×iàÊY\x001c\x0008\x0015\x0014Zþ'¨½dA¦O¹Éâ%»b¯SAÁ©H9GÃ:\x0002\x0001lÛï\x0017âB6C,ÕÚÌ¯:\x001b§Zö{Ê\x0000'ÒÂyÄëQÁõHW1Î#p{°Ûì\x0005Ýy\H\x0007qàzTp=)éÄFÓxµõÑÆè\x0016b67~\x0005ßcÈ"%\x000b$ÌâÙ¿B³×Ê\x001f\x0007¾G\x0005ß`\x000cË¥\x0001:É»2¦ö\x0019WÜk {TÐ=ËYds67ÔÛ\x0004r\x000b
°p½ÆîQC÷%h\x0011ä&E;hbá1\x0002\x0007ºG\x0005Ý\x0017ÂçºÛF\x0013Ý+\x0012Úï8Ð=jè>X­©´*iN\x001bÇ\x000f+§q`{T°}q0j=¤°î_/æj¬ï{½¹ck\x0005å\x0006ªw\x001aª\x000fi÷ùÄká|\x000eMi7¸\x0005p\x0003¥:
¥ÆR!ð\x0000wI½lû°à[n|­ÔPW\x0002\x001e\x0007(¸<ëù`\x0007»À\x0011nà\x0008§áÔtb\x0001P®þYjà\x0010\x0017\Þ
'ÑiNbö»µDAÔçÜË§\x0005æò×{×á,Â&11V$(£_y%ñË{ËCíÄ¯¸Lã&"\x001aýÊÍß\x000f.ï\x0015.O~.æB\x0016\
%Ì
m­¼uùÁá½Âá)\x0017×2Q	"WR®\x0005âòË{Ë\x000fb-ã9ö\x0004\x0013C·Â§aðø ñø\x0000,²\x0008åòX»êI»µpÁçÃàóAãó14Ú"m+v®¹Ì
®ÁçÆçiÆÊ6\ì]¶e6Î.\üÃXþÑ8}ÊtK¬°\x001b,ëw\\x000bÑ'\x000cN\x001f4N÷h]pÕÖ@ká"\x001b\x0007¯
¯Gë\x001fÉ;\x00057ÁÞbtiÁ\qðú¨ðz,·\x0016,7Ä¡	Î{³@\x0012qðú¨ðz,·°S=ÎÙ(%âAüKkpû¨p{º5{y\x001eþ(\x0017³=b»\x0015\ÛGÛ£K­\x001ckc;´{Z2\x0005ÿJÛ'ÛûíR-\x0019\x0017\-ë
\x000b¹s\x001aÜ>iÜ¦Ôå®aX\x00119ÙÜ>-}\x001aÜ>iÜ:QâlÚRËç\x0017\+
.4.lk"¡·ú	\x0001Û²°òÆR¿ÆåÓÞs\x0003Û¬vÅÕ\x0002vp\x000b1\x000f.5.±½E\x0008\x0005±\x0015\+G1\x000f>\x0015>ï!}ÇÀú{¹^6Êý¿}ÇY\x001e|>+|\x001e#,»=é;y\x0010{Å\x0015ÿòÂ._8doÇTBA¿¢¨hÄlfÏ¢óJK	\x001cÑ\x0006\ÉNÇË·\x0006/îXr¶õw­Ü<pØ'Â/ä²Pd.(\x0019Y'BÌQw® ÞX6¬¼Ê\x001b_V÷aMß¼=ºrjêãcÈ{\x0003Ì\x0002º`èÊ\x001dIåwÁµ&9ZXùä$\x001c88ÈfètÌ~ët¼üË»¢Ð÷Ëõû\x000f\x001f®?~¹xòéë¯ßoNpëPY"5\x0013þÂ´;¶\x000eb{²KÝ`àå/W/D®ïË§Ï]¾xsñäåÛ7o_=½zõmÄÐ#Ók÷èeg\x001665öaÛí*dì!ãy#cë+ +½g#\x000boÇ\x0014\x001f\x000c±ë\x0011»Ó©]ªè7l¡Í­ÈÙ]¥W\x0011û\x001e±?8÷VÄ\x0017»r;D5âÃA\x000e=äp\x001a²ÇV\x001a¥ù\\x0016ã6i/õå\x0007zÈé4deË\x001fu\x000bð\x0012N4
±}8OÎ=â|ÞÈÐîU\x0014ÍX\x001bn¶\x001cÂðÁèbïåÜ8ÙÆLC¾õÔ¹îÚ/,XÄ<ÆóîÕ{rª\x001c?d×îû]2¿y$ö|()9
¯£\x000bH¾*Q¹]Ø¼y0w¶C(±çc	¦\x001es\x0014ßØ/äöÁ"¶\x001d=\x001fM@ÄÊ¶{10æö·³óç!Øóñ\x0004­¬\¢\x0007\x0006^Ls Ù?X<±C<±ç\x0003<\þ,ë `³³{8ß\x0003æxÞ7|Kçì&}_Ï`K\x001e\x000eñ\x0010\x0002íé\x0018\x0018oCå>\x00195dÄðp\x0011e\x0008ö|\x0014ì\x001f¯,\x0010£wbÁl\x001fap:
ÈL©²x\x0006/\x0003µ¹\x0015(0?oÀ\x0010\x0005á|\x0014´­®|Lt¾3vñ«ÇëÔé \x0018ò~¢R­Ü\x0016s\x0018ø`Ü\x000cC\x000cÓ10fÛz¾ôÚ;ÀVRø`q\x001b\x0018\x0008§c`\x0001Û^\x0003ÐË2\x0008m?¶\x000fÆ\x001a0Ä\x00138\x001dOH¦6ÉÃ^zTC`ßÜ\x001fÎÌC8Óá\x0006ü­¼Ý\x0002=^mãþèâ\x001f\x000eó\x0010Pàt@	TN¼,»9ÍÞ"\x001bì±\x0006\x000eä§Éy\x0013\x000c¾¸ÀïFåd¶°í\x001f.¥\x001btñø6¸m
;yQI{#~àÛàñç\x0007ËêÐ\x001ca£YÀíIÕO,\x001e¹w¦üÜU¼\x001e@â\x0011:Ä\x0005è¡äÿ2K\x0006õ·iaþpÙñGè~ÅY¼o¥³:nY\x001fÂP`¿dñ$ðòñA×ÑõÇ¯ÿýúË]Õ\x0003\x000b±UA£c9\x0007Ú,Ú¦ÎÂXyyüêòõëË7ß\x0006\x0003=\x0018\x0003C¨|ËËû\H²V\x0003=\x0018\x0003Só;jDØ°\x0004éÖHæ°³g\x001aë±¸°a|\x000fÆÏqöÔ²ÄÇÐÊMæ¤YB$L%Ê\x0002ZÈÈíÂ.d +¹4\x0003\x0013{0qÒ,^vôö`¢\x0006æ¤eR\x000f&Í	¢\x0013niK#ß|"#T0`OZ&÷`òäg2$5U-¸ï6òaR<e,ÝøÎÌIÒ?å\x001a[\x0013Ò\x0008^Ü\x0017Ü9(#õNr¯\x0017¥°Eô\x0013]äõ¾	çÐ\x000c\x0014c'9&·1+$Ùkv\x0019'`Ðó\x0018;Päàeh\x0002i5ø¯iþÏ\x001d&;Ðã\x0019ºg1ã?në×cÛàIÛ\x000c<c'\x0004¿\x0004
J4"ðÐ¯7f \x001a;Ç4[&ÉN\23ÙÜºÎÒY\x001f\x001eÆN2MLÒG¦á5Úú'9\x0017&a8Þ0y¼·­\x001a\x0015Èµ\x0017ª{d:é30&VsUÉ8%\x000bE\x000eò\x001a\x0007»\x001c\x000cCf\x0005©U\x0006iÛB+;#h+t;OþÜék`k
ññË&\x000b?d!¾}k°?f8Ý0wºÁ\x0004Zª\Ñ\x0004î\x0000t[MÑ\x001c¦âgÑààÃ8çÃÛm§iØ7ªqá\x0013ãÏ¹
u
ñÑ$\x001d£iëX;wºqð\x001aó\x001a â*\x001a¢mÍcP.4Íà58é5%ùDöa'Û\2RVOálL\x0018.Ã\x001cÁ¥éA<·tÓáØæR¿\x000fJ\x0017¥n J³¨v¹\x001duI+"4¶:3ýJÍýÕûñ6Ú´ïD~õõúë\x001dhÖ\x000bUá\x0004T<Þ'%Ï¯£¤\x0006Ø-6àuÈ¯Þ^¾ý6\x001cèáÀ\x001c\x001cZfÈÒJ\x000f¾ÂIìÑ¾$¹7WZÏÁÁ\x001e\x000eÎÁ	Qª
\x0018\x000cp}6²\x0015¦\x001c¯[vÏÁq=\x001c7	ÇÄG¬\x0000[þøÊ=y\x001b°«h|7ì¯Cã{4~\x000e
íø®ä\x0010ý\x0016$2lH\x0008Mê*Ë:0¡\x0007\x0013&\x001d§|©ÄªÂ\x0001Å³\x0014]þ¬\x001fÇ\x001eNãL\x0012©5Ü¢r0üDáíâ¹\x000eNêá¤Y?\x000e¼ \x000b}¶,'Mæa7íéS{8yÒ:Ùq~T*`×	\x0000²ó9§§¼]Ç+\x0007Ió¯Åë.¨"P[p3­¤cóÐØÂ9<\x0003	ÚI\x0016\x000c9|7ùu­sÓ7bgN9¤\x001d;ÐäH\x00154Va÷\x001eu6<Î³ôt"°sx³n'\x000f{tv)Vê	,om\x0012Uøp\x0016Íp¶ìäá¤VÁxî\x0006múî+\x0015\x001a\x0018|\x0019&}9\x001b\x001fÊfàmåì\x0007?ökTUxÆ>éË%t/;*xWê\x0001Ï\x0003ï.Aw\x0007Õá\x0019|\x0019&}:¢Xâ½$]
Ob-Z¬9\x0019·`ðeôeÚÝT50\x0010sà\x0015\x001a¹àd<½\x0000\x000eÎàÌ0éÌÛÎ&\x0016_.~]³ÓìXÓÎEkO2!\x000eÞÞSæÝ:åbj\x0007wv-ÿ$\x0013z\x000eÎ,ãl¶\x000clêæD]jeÄ\x0012§§9ÜñµîØ(Â`s'ËT{Å\x0011\x000b®ú¾}Û;\x0014âÙ(ÃÉÂ¹åK²Ø\x0001ª\x0017mxZ
\x0016Ðäe\x001cN\x0016Î¬-Ë`W¦;WmHÈAF°Ogg\x0018ùá\x0004~Û$7¨º 9|]\x0012ºå©Üuçr>\x001d-n`yP)&J
7Rlr\x0019\x001d?Íãöfp0\x000bú\x001bi¬/<"jõ(gOÆ2k°¬¶VHÞ\x000bkº\x0008,RGë^dóq'Ó3¼\x0001\x000bçaÑ»ÚÌ<]ÉRå\x001c°hâz,êo#Øõ5Dò?ýù×ëÏïîÉ§«\x000f\x000fÞÙ,#¨\x0014a¥%\x0008\x000eãÍ$ÿòùãËWW÷ä\x000b(èA\x0002\x0014>âñf[w\x0015VPMÓ\x000cL<\x000f
{P8
\x001eÌ²ôÃ{^&äJÔúá\x000f%\x000c\x0015(×ró¢©:Û>\x001fð^´É÷ü¼¡¼¡V\x001a\x0010«Gå}Ò/ Ç\x0014zLaÞNÂÞÈéÙ£¼TÝ#Ú\x0005=¨8o¨`hôüpÁ;»Ð\x0014+\x000fM\x0012*P©\x0007æ-UÜhïßæ\x0016\x0014Z÷(ú\x0005Ê=¦¬0ç´¥\x0018JVÎºìf\p©½=`cN3ªÜÝ¤iþÏÞ>³ÑG5òù<¡#iØæ6È¡ì,qç	Ý\x000enç\x0019Äcø\x0003Z+óOÙØ6\x001ao\x0017L5\x0010ºU0z1\x0015W­À\x0002j1UëHñüù³\x0003{Z\x0005}Ä\ I{¤jÅéç¹ó \x0006¦²
ªòû
\x0008äm:Ów1O¿p\x0000\x0007V°
ZH®}¿X¶B?ç*\x0018h\x0001\x0014´@ÏÒ>¤CÉáîHs»^¦ \x001a³)Åá£éu¥÷È7ú4ç)\x0001Ì\x0005æSíëíCÉõU¥|½&ë¾àç£XFM>¥ö7\x0013\x0003¬ª§\x0015®2ÄLKaì\x0002ÂMl*pHâé2Çæ[Ö°\x000fù;>\x0019®¨òE5àRnXJn*´\x0004\x0012\x0011S8OófÐ\x0018©·\x001c\x0018Ê\x0000÷Í:&Crm\x0015\x0004®¤Êöh6«²\x001aÄ}2J\x0016ù¹lv±J%eØ\x000c·Búa»\x0015~úZo©o>_ÿùÓÇßîº¨Zz\x0012®\x0017Õè¤~«?ó+Z'\x0018ðêåÛzQ}óêòùË\x0017?|\x0003\x0012ô`\x001eRù#W1+=?ì¡±²øs #¦»¾`=,TÀ"\x0001b~n´L\x0015\x000e!£ê\x001b¦Ô \\x000fÊ)@YÓ¤&ä»j¢½ÍVa\x0001ïaùyX®ð|æ%¤ôÜWµmK«°`	Vèa\x0005µ$7¼ÔªR¹\x0011Ê\x001eM×Ëp©a¥\x001eVRÀÊ
\x0018V	Û\x001dÞkQ\x000bÏ\x0002¬ÜÃÊ\x001aj°¬sA+ÅYäJú °zñ9-¬v\x001b«e4¸@úRÈ\Í\x0015à\x0017ÍeG&ÕP©
²¶»¸}ûÉ·m£yÅ^\x0003Z\x0005;{=1WÝáYüßH¡$-á\x001aøÔ*\x0008ÕRõÝ\x001e
¿H&'3	~\x0013h=k T«àTJR=sjíÉû !1÷³\x0012j\\x0003§Z\x0005©ÒÕÇ\x0008®ÀÕÉÇ NóÛ\x000fj\x0015¤J*¶µ\x000ec\x0014YÖ\x0014P¬\x0015WPÅ\x0001UT *üÎ«£Éu\x0006=ZïÚBü±\x0003Ñ[\x0005Ó\x000f'Í-\x0011¬ëråoq±®Sã\x001aÞ*¨\x001e\x001fÐñëH`d+7¦O\x0008\x0003Ïçé\x0015x&?EÏûÆvH=®çAÁóeOYÁyUm®m\x001c^\x000b×ýÅÓÁíñ}°}8¢+\x0007é;\x0017oÀ*xHÃþ|÷\x0000Ço)\x001a»'®+ßÖ\x001fáy\x0015:S0 GÌàùÍ>A[\x0017nýÊÅèÆ§Õ}YC»¥*¶<\x0006JÒ/ÙbL÷äÖ·¿p(yÐJÿíÝõÇç¾~(þó\x0001MkÔzû(rË¹gHk\x000fÏ¾ÿíêòÅÅóo¾ó%@@A\x000f
æA(bôæ¿eCÙÏcÂ\x001e\x0013*\x000cåeó"\x0019Ö¢§à<&×cr
LÒ\x0006Qìm,È]Çmj\x001aP¾\x0007åçA¡/&âÉ (ÚºÅP\x000bB)(0y)W¡<Ï¸E\x001a
7Vj@Å\x001eT\x0007å6\x0005õj(y\x0000p%mm.µòõR\x000f*Í"\x0011D\x0006UPØúú\x0016Ì\x000b^V
*÷ ò<(ÒÈeC5ñ½de\x0019ë\x001d
H{ÁsãM£øzVfÎh]¦ÅÛ}Hö¼¡ìÈæ
:/É3ë±Ú`øð%ç\x0005T>®aÕ\x001aØÜ*è¼Ð\x0015:\x0017Õ\x001aÚðm¸±xXjàs« ô\x0004í\x0003\x0006Ë)j±ÊÇ\x001ds\x001aP\x0003¡[\x0005£îø¥G\k\x001d?¡|Éó\x0006>·
BÏÀÝëÅPþ¶vAHÃAÈy\x0001Õ@v=iCh¾9JË¸÷\x001b\x0005R\x0018ÈÓ*Ø39ÙÅGÎ½\x0019ÉCË¦kW5¨\x0006ö´óôI­5­ÚE%»ØÔ¹k\x000b\x0015¨` PP\x0010h¹"°z¤-ºÕ­rs«\x0005V@a@iájÜµ÷mk¸s[ê×¿]ÿþåóÝ¨Æ|xA©Y!\x0007É³\x0013\x0008\x000bn\x0005\x0003Â<ûUë8Ô
uÒ\NÚzç\x0019\x0014\x0006\x0006y\x0006-wÒGÒ\x0014yÄå`÷Êæ¯\x000fé'Ìçå\x000fmû&l\x0014ù\x001cÔÐ]\@5P(((4o
ÝÒá\x0019Õ¾\x0008&,\x001cÀ¬`¬Ï"\x0014·-Ùª«_\x0011Únã"f\x0005(\x001cX\x0001çY@±(ê\x0006
\x0019Ô\x001dz\x001d*L\x0003'à<'8Ò·ÉÄ>å\x000bÔÖ3²\x0000j¼$ÏsBù×E]
\x001b}\x0016Cán©óÏ	8p\x0002ÎsBÀmû¬í­iËí¢?«ãWá|^E¶Ên·8USôX²Õ@U8OU´Ò©jVìË¿Ùv
\x001cW«j@
LóL\x0015ÑTé!L5d{8í¹ÁpbL-µ	Ã[ØmuÜ¦A5\x0010(*\x0008´ØÊA³\x0015È\x0011tM¶f!3vC¶çæ³=oC[MÏ²ìW\x000e­2?nàu§àuºn5S¡Êïluþ\x0005Æ
ÄîæÝWÑÍT4"S-\x0015RÓÄ3ç=7\x0010»Ó\x0010;H#çh*ÿ\x0010¦\x001aß?çÝ{hÔÙ±v·ôÄÈ¶:H4©P
Äî4ÄÞ.Ì£­ÒCØj v7Oìä/Dk1³r\x0007Ót\à¸\x0018Kj`v§av\x0005&­}\x0008[
Ìîæ}+\x0011M4ä\x0017+»­0Ï×ÝÀìnÙKòHÝHnEs£b*<o*?\x0010»'vê\x0010Å6Ù&éq\x0017\x0002ÃÇY?ðºçõHv/[`®¨\ÛH*'çQ
Äîç=ú$sWh\x000c«Û\x000fØt`á,æ[o\x000b~`v?ÏìåOmû-iP´ò\x0002%\x000cÂ¡~Á­\x0006f÷óÌ\x001e÷4¨«\x0012ê\x0017ÌÍV\x000bu\x0008?¶æ*Ê\\x0004(úÞ'ÑOÆÏøüÀì~Ùcn\x001cJêÂý*&\x0016\x001b\x0016l50»gö$}ùÔk^o\Á¶»ÍùtÝ\x000f¤îçI=æýiÃG6SÚe\x0017Ha u?Oê¶­ïÙ^®¨\x0002ì2Õî|X\x000e\x0003«yV'\x0015\x0014ÙßV\x0008Þ3) I¨Y¨DÖÃ<­g+é:)z×\x0007GOOÉbª¾0°zgõÂDmr	ÐuÄ©$¦N\x0006\x0016?\x001f\x0001ÃÀêAÁê¹µ\x0006pQ¢º\x00154·ZÈöÂÀêaÕ\x0013ä¶MÁ\x001ae5^ý]°ÕÀêaÕs*û:¨ãË5\x001aZb|þ%-\x001d\x000bó¤ ¶sÉðh1]%³âì\x0003©yRÏÛ\x0002\x0012\x0012ýb^µ	Ü\x0002¨ØÃ<±'jT`SÑÀo¥PßÚ
ñÊa ö  v\x0017¸\x0011²½j§´_¶\x0016ÞÖãÀêQÁêÄOò\x0008#\x0014¾ÀÚ\x0017WËq`õ¨`u¿?X\x0019[kÞ~k~aS-$\x000bq`õ¨`õrÍ\x0004%é¬8¶	¹¼àéq`õ8Ïê¹Ükâ®~/»·¡\x0002§Ï8zT:i«ÛæU|/õÙ6¯òçCM\x001cH=*H=[)¹ÑeËTþ®©ûÂBÃ^\x001cX=Î³z¦iKfª,÷ÒMhI=ÏÔãÀq?3)xï)(GåàeµbIAÏ£J\x0003Y¥y²Ê¸¯ï.·\x001aA\x0015öÄxá\x0003¦\x0017Ò</\x0010«;Ù*
URRÉ\x0006ÏóB\x001a`?ÙgÑh¦\x000c¦ªtùsË\x000bÄ\x0006gO
g§¾/©$\x001eµ'foñ=oC÷v;§±»QáêÑ·
ë$\x0017X#`´­æï¹*ß\x000b)\x000f~\x0015~p\x0004òí"ä½àÝôy/¤Qõ[d\x0012{²ñ\x000b¤åÙ¤D
¶u\x0013Úó9¹~ý]FØ§Ì¶\x000bÎË ?Ñ¶Mxk/ÿñ_;¼gÿ6ýÊP® ­\x0002±*»­\x0011\x000b]½h_\x0014­æR\x001flÏ\x0019ú\x0018Ú6æý÷¯×oZàñ¢8ìu¦Ö@ uÂ¥Joù®<|×?N\x0003£È(EJ\x001bè}Cu>wáx\x0010ÊGÐX¬äÌ=ª¦nÏ\x000e,\x0019ìËÁ`_æ\x000b\x0003n\x0018Õ`¾ù\x001aÆv\x0010V\x001e ç 8Í9 õ×²ºÌ3år-õÌJÕé\x0008Î©h7R\x0015\x0017/ÚnnÂÖà,äx8ó \x0001Gë¡Cl7Úµé]K`Ï
np\x001b¨¸­ ¢6à Üå\x001aQB»_¸±¡=\x001eR´ªCZhÍÅ[h-?\x000c­ýz8¥¿jê¯°w¶¡DÐVç,Ô_¹qLêÚýiµ\2ùbi[+ ±\x000b1þÆApªà© %FÇZ'~S\x0010ÏtÞÞ²¶?µ\ªj\x000fqo!Yh7
ø¯×GékÍMS6§fÙÔ^nûE³\x0010Hó/UÔ^\x0014()`ñ\x0017u¶=n.\x0004yÌ·%GY\x001cH?n­]rXÝ]«¥Tü{ã@ê@ 
ÞÖËBòTQÞè\x0017B	[HÈùnÚNe¸¦w5öÄ\x00070\x001cÞð;Tù\x001d\x000bá\x0016pî\x0001ÀÅ\x001bQ5ª¢j\x000e°wR`Õ:ôÑ@+Ãçf´pãÀ\x0006áè]{Lâ5Ñ%õm¡\x000bÅxwÃãÊã¢Û&ãëGE\x0016·ö\x000eÒÞ/wþM-Ü8ªAuT\x0013Ø¦G*T\\x0007(\x0017zIqáÁÏÝBu%~é¨.§Ô\x0004¦÷\x0010V¹V¬_\x00017\x000eê]Ä9É4--y`Y`ÓÆQïyl»÷Á\x0006ý
&ñªÄf\x0019½ÞV^sC²kËþì=)ðíÈ²;È\x000bd×ä\x0005¶­îÏ®ÿçõç?\x0015[ßÉºò!ù\x001aHïI5-\x000fØÆ\x0014n,ìÝ6¹?»üñòÕOo¯îþ\x0002\x000cz` \x0001VÐø½B^_·\x0002îË\x0008)ð/\x0000Ã\x001e\x0018ªa\x0013-N¢)VÁ^Æ\x0015`®\x0007æ\x0014À¼\x0001j±\x0015`µ&Fb\x0016
Í+À|\x000fÌ«Y![*\x0014\x001fKmÿ'\x001e´ÃÀB\x000f,¨½\.+dË?Åæü¸äc±\x0007\x0016UÀr£WÚa]qåæbh\x000cz\I«D¦¶~k'`ÎìéÆ\x0012®ÜãÊ\x001a\Û\x0006ôÌ·äà ·h~Xô­Ãµ\x0010lìj¾\x001bÙö5¼ïý¾ÿDªr\x0005æöÛÔÒ´\x0003ï[
ñ{tBn¾_ÓÆò1÷e»\x0012ì@üVÃüvkí\x001bÜëM Ø\x000c\x001eÆË\x0006â·*æoý\x0019ª\x001b*ýy	Ö@ûVÅû\x0011Ú©DÞ÷\x0011ú.o¿k`}«¢}o¤¡,ÆÒµa§U
´oU¼°
"·\x0015)¡íÜ!¾+È\x0006â·*æ\x000f(s¿Ì32÷ÝÇi\x0005Ù@ýVÅýt\x0015Ù[Ñ=ÊÜ!!®äc0p,h8.ÀRÆ ÞáÊ±ÞøÖefV\x000cÆÜZÅ±Ñì
	Ø8¶u%\x0008+g\x0013\x0006\x0005
Ç\x0006³u"T\x0000/5í\x001b½òJ`\x0003ÇccjGú],³Yn%°ô1\x0007\x0005
Í\x0006\x001bi\x000e_Á«ôY Ù	±ÙRÀhAE´Å·Àµ1\x0003ä$#ïÈü
t\x0006*:ë´\x0015bä\x000c:ÍÏ`ÉÏ\x0006:\x0003
\x0005È,)\Y®à\x0005¿\x0007'\x0013VB\x0000\x000e¹,jrYZ\x0017B+÷X9¾Õ{ÒJØÄhQE´\x0018ÛìdÈ¼/!ø½naVÜ\x000c\x0007E
Ï\x0006\x001bZU\x0001\x0006ìfÐÍi¬DM\x001c\x001f1T<ë¶2gE¶í\x001fÜv'§\x0001é\x0005d\x0003Ñ¢hÍ­ª\x0018dË_±YvG³t)ÇÎPCg\x0016CíCò\x000c\x000cåY6¥[9\x000ei#jÒÆ\x0010üÎfÈÅàS\x001b2K×L\x001cx\x00165<\x001bÐ\x0014uÏÕb aéK+oR8ð,ªx¶ÄóÖUkY&7\x0004Óns6¬\x001c\x00007ð¬Sñìöç·¾Ld	gÄì
4ëT4Kr\x0007ò$j±)\x0014ÆØ\x001f>WhÖ
4ëT4K:\x0003aïdå\x0019w­¸¿\x001bXÖ©X6»6\x0011'ËÓC¡\x0011xK\x001bU$ë÷ù3Rwã1æf2·rirC6ëTÙ,r¹ÕÀ#6\x0019îo\x0006K¸\x0006u\x001a\x0006Z'\x0011AÑ\x0002¬é¶`\ú\x0003Ç:
ÇF4»¢L%\x0010Úx\x000fK°\x0006u\x001aB¤È!\x0018f\x000bß¦½]ù~àW¯á×H}ïüüã\x000c·\x0000\x00175Y°ôÈâ\x0007õ\x001a%½v\x001eëEÄ\x0016Z¶\x00182\x001f?ð×ðØß\x0019ØXYÒ°E,hØÉ}T£Cííó¸-P	l \x000b¯¢\x000bL­\x0017ÈyyÇ\x0008MR0Å¥üÚ\x000fçÒ«Îeâþ¥BH2:b<\x0015Æc<¢cl¥èç×¿¼¿þpñówï?¾ûãõï¿_ÿéã=\x0008ôÇÑÚS~Ð\x0008Iòì|xÐ{~ùêÍÓËg\x0017??»zúâêÉåë×?½@
=R8b'SoÕí!vYO\x0000\x0016*öPñ{6ªëºSHi\x0005\x000f\x0003^Ür¤¥§)Ãmþ\x000e¤·7L\x0008LßÃôß³AC4óR/#\x0008\x0005ËJ¸\x0013yïl\x000eÕ³@s\x000f4\x0002J«©+RgAÒ²Ë\x0014Ý Ýë¹\x001bEs6Ý#b2,ÄHV\x0005±jx\x0018¬#âÓ@ý3õD¹ºJ´ÒJsTr>\x000buàS{PÛdLQkB5×ù¨q\x0016ë@¨ö\x0014£à\x001eñù§\x001e
~ÛkÎz¼
E:\x0010ª=Ç¨\x001eä}E«U¥[/\x0003>\x000cÖUí)Z
0T:ãþ.mÈ\x000f\x0002u U{WÛöóò\x000fô\x0002QÍ*²§ÜýC`\x0003ÖxÊ¬\x0018ä½\x0017³p\x0004ïZ\x0014°îa\ 
XÓ9»fé\x0000q¬\x0007\x001cZç_vÄ3	\x001d¢=\x0015®\x0002\x0004yBD*B³¯¢À\x0017²\x0002ú-Â\x0010¯à\¼*\x000ejÅ¦Å\x0002UoÄ¨þA|\x0015x\x0005§âÏ IÖ&\x0005×îçÙ<H\x00081ý?\x0015®B9J­J¥\x001ey\x0012m\x001eña<`\x0008\x0002p*\x0008Ð\x001fßU\É³8cñ1îYÀ¤\x000100+bÖPße*VÛJÞ¥\x0016°\x001eÆ\x0007\x0006¶Sl\x0015P6\x001aPlå7^ï¼myÀC Å\x0003ð\x0014\x0007\x0004\x0000áU¤\x001e\x001e2åÁ<\x0008\x0007àp²ðÜÉ2©ÍïÀ¤\x0014\x0007\x001cÛ¿Ïb\x001dN\x0016:Y>5nÅl¥üìtÓä£@ËY¬ÃÉÂS'«ëÅÞ\x0016E\x0002·<\x001by±Èöaò«aêc¬ÌJhÝ6µ÷í$ÓàåÉ@G¶h\x001f\x0002ò°¶/Î!þ{_¸
\x001e^Úè}\x0015M¾~x÷ûÅ/ï>ß\x000e!nt\x0005ô\x0010\x0018¶Ü*ùÌ/ÎÞXuòöÙÕë_®^Í \x001e\x0011Ì#*\x0007(\x000b¨\
å¢\x000f9m:	{L8ë,,lùh]\x0006JßA£Â­\x0006ëA¹yCmÃ\x0000\x0015\x0013ò¼B
\x0010åãù£¥\x0006ï1ùyCAdFHò~up\x0008ü\x0006O¯:ñ<¨Ð

PÈ\x0003\x0014Å8ÀMÑ)È(Úç1Å\x001eSÇä¥\x001d\x0014b\x0002YÊ¾©ôTLG!=
¦ÔcJó¨jüñ\x0013­\x0014\x0011;ÅC8PÊ=¨¬2ã®Øl(\x0001»\x001b\x0015 ºÇ?¢\x0006£@%Ò\x001aÅT¹*ûæçGu

ªËçÉ\x001c½å;(ÕìÛéËÐluR× \x001a¸ÓÎ§³Èí\x0005\x001bQ\x0001ï=<÷BDµj O;ÏJ¾`}u¡VAÅoK4\x000c¹j`\x0005« d\x001eñ	L2"çäÅ«rX8CF³\x001dÂ6¯:G\x000eu\x001b\x0012å
õ+\x0006Ù ç\x0000\x0017\x0018ËÚ#6kUàh¡\x0008FªHQ&R\x0001öÝÜq[·Û·u_ýöéëõçß.~¹~ÿáÃõÇ/w¯@\x0004ûÑµZy6¼\x0017\x000fÏíW?¼|{ùê_.>{vùâÍ·áA\x000f\x000f´ð$¯±%¹ÚØnÂá\x000e¨G=:Ô¢3¢¶G\x0015úC	BÒ5r¸õéÑ¹\x001eÓ¢\x000b"Q_òC,/¶kó¢\x0007 =:ß£óJt)Iã,5iðcTtm\x0010&\x001c\x001eMôðB\x000f/háyÙ}LÙ\x0019ÏD}ÉûUÏ=¼¨W2
y\x001c)\x0017N.E×ê¹þ@Äzx©´ÖË$\x0004!íT;
ÚÑ£½\x001e]îÑe­ñö¦½òmy¢.ú\x0010Ú·]C·gm®Û\x0003>\x000f/¶b­\x0005i)~ß¹æ\x0017iÅ\x0011C\x00192\x0012i\x0004ù ñoj$Ëð\x0006N¶JRN&HIÎ\x0006\x0019ba5J¼b\x0007R¶JVNÖ÷JÄü°]âÜ®z¿\x0018pí@ËVÉË©\x0018Í*8Ên*O\x0018\x0017®\x001dhÙ*y\x0016d´Á6!­riR.y\x0015ßÀËVIÌ$Ê_ÁEÄ\x000f±Xo('ëÁ
¬l´\x0010i·\x0011|m$$.Æ4;Ð²Uòr*\x0019|ns!¾òJ²ûF\x0016³ÈË0ð2(y99ØG}\x000c¯!
©5¦\x0014;.&T0ð2hyùïëz0æñÊD¾Ð®lÒö^¦DMM*Û­Â\x001b\x0006ho[\x0016! \x0014S[[F¤º\x0006o\x0008\x001a 
\x001aÅfa_\x000eËAmd­¼\x0018Ô`\x0008\x001a 
\x001aå<È¼½¼¼6$Ä¶à",¦£0D
ÐF°Ü¸@Ï\x0004\x0015\x0008l?/â\x001b¢\x0006h£FHM\x000c©xbÕ\x001f\x000f©uÄcKo\x0008\x001c 
\x001côÚ*\x0012Ç¶ÖU|íø¦Uæ\x001b\x0002\x0007h\x0003G	\x0017²;ózª¼ÙW\x0003,f¤8\x0004\x000eÔ\x0006dÚÀ#ÊK^Á×DùãêéÀ!p 6pÄ$ý\x000b´¦\x001b\x0005_h\x0002Ö«9\x001f\x000e±\x0003µ±#ûÆ. \x001b×i\x0004@NGÈy\x000b¯@ÚàAK\x0017ät8N.ÓØÅ­~ß!z 2zdã¨t^í\x0007òX<SÅà\x0017/\x000eÑ\x0003µÑ#yéK\x0002¢¸Ú­d÷W"\x001c¢\x0007*£G¶NoMW!æ~àÐÚÐA½1Ì-AÞ2RëÇù\x0018=¼!r 2rdpí¾f­4ófëålx¿¹¸s1D^#»)\x000b´ïÕ£á\x0006jvJj¦\x0015OrcCYÓLKoäè®2³\x001bÏ)/ÛØ4BAêyådFh\x000c«/àn`\x0016§d\x0016ò>Ñr\x0004Ëý#ÅûDª9\x0006·x:Üpxòð\x0016?kÊF6=JõÚ[õ%ÕÏ;\x001c^§MûÍD©z\x0000øRÚ[Ú±	@oÈû2ïËnë_«æcIÿrvÛÕÃá³ëµg·äR²CÂÍ¹Æ{«\x0017^?\ÿ½®pX×Ài³TLç3Ô\x0016'¢¥à\x0019È¼x\®Nº\x001b0\x001efæ	U 6Pæ@ðÍ
a5\x0002û^>3,¿Ï\x0013¬\x000cÒ\x0002f\x0019©ØÊ»dÕwq<² PqÒ^çz4\x001diy¾ß7^-Sb¾ñÅ³þ\x00170aOk"î\x0012.g5Þ\x001eQz{\x0002enáÖ91Ê¦Íâq5:ß@éN ,ß\x0019÷ë]$¢¥°!¯VDÒ
ÏLzÏÄ$\x001aôÆ\x0015ø
VÈË\x001b×7<óö\x0011Ì]\x001c´Ò°Ë¿¼+ÿÖÅoï~¿xþ~ÿôeû_p{´Ïô&Cí%¤÷\x001dX·×ñ\x0003\x0008fÓ	$^þrõ¢ ûáêõÅóyùúå§¯ï6 \x001e\x001c¨ÀÑ7å¦½
\M"LH\x0017p]¡ÿ\x00148ìÁ¡
\x001c
E±å|¹%7ù.'àì\x001a¶ýÙw3Ó}Vô¼ ·à	Òýî¬©é\x0017¦lîÿ¬÷:Üþ¢ºA\x000b:h\x000e¸
Ì%¤\x000bTEÖuÙÃ)³¥\x0001[RÀWÎ\x0002ÎÉc¥C®°\x0016tòß\x0019tûkàæpF.Èø\x0005­ÕßÆXA×Î*\x000eg\x0015uÕG/È.\x001bÞ²\x001a\àfV:¬è\x0003Ê\x0003Ã£|d\x0012'\x0002øDsi
Üp$Pw$5<·^Ðyç/¬ÒÐå5pÃ@Ý 9åúDYx®	\x0000xÇO¨ç\x0016¿«\x001bÎÓ	\x001aöãVWZr\x0010eÚ7t]eõ\x0014ºáL8Ý EYµ#\x0002hÓ\x0001·ùÈÚPûM\x0015çÜ®OOØõè\x0017U 3ÜìW¼/ÉÙð¶
kWS#HÐb¤L9\x000bFÙí\x001e¶ê\x0005\x0010¿v~
Þ0¤Ú%â\x000euZ#\x001a¨³<ÌhN6@\x001c³\x0015Ú\x0011°g+OþíúË»ë¯¿~~ýñ·;Ð¡¡%ÊÕ\x0015\x0013]âjû5
:\x0007xdüáòÍUùåÕÓË\x0017?|\x001bëá9%¼[\x000b6FøÁÀ=\x000eàæ9VÂó=<¯W\x0000\x000b¶3ë\x001f\x0015;z·l¼Ð£\x000bJtù\x001aDW	é÷/§Fzë3¬\x001a/÷ð²\x0012^À6æ\x0012Û·uR$ÜÔ¥Öàí]\x0004ÏZ\x001d>z?õ®
qX\x001e\x0015\x0004ß8ð\x0006¹(ñÁ\x000fö£F{\x001e2	å7\x000bÜÂA\x0012¯7²R%¾Y¬Z¨zdÜ\x0004Ú¨¥t\x0014;ëÜ\x0000¢Ä7PUr¥!C:Òb\2Ðäãâéµ\x0003·X%¹ÐÒ@³ûø	ùúe¤çà
äbìBåÚ´[>oÁ\x001d¢oÓDa\x0011_\x001að%­û\Ä£3üZÜ\x000fÛ´S·§ì\x0014¾½ùðQâK¡Ñ¼´)\x0005Y\x001fLÏ\x001cì\x000cÃñ\x0005åñu$ØÎYÆqS*áCè¥_«p\x000eßp<@y<¼\x0005Ö§¶?ÖqL)Kø0yýö\x0006¬
^TÂó¶¹\x001fõ×èe\x0015y1»ö)ñ
Á\x0017Ñ×\x0007Y\x0002\x0004Ûe©/ËÈ3ñfz¯ÃÃñ@åñp15|YíSjæëE\x0004ÎÁ\x001b/*/½í¡xá\x000e\x0012×©÷ÅÓ\x0003;£éQ¨v8ÑMG\x000eít\x0004ýB§°\x000bÒèÉë÷ïî¼\x000eÅÊ\x000cYqÁ Í­\x001csPá¡«ÐgO¯î»\x0008\x001d\x0005Ma\x00174Aä%q j"¦ùPzÑ@Â\x001e\x0012NC2(ÍÃ¸W\x0006\x0002JK9\x0007ö4$×CróÊ\x001fÌÂ6\x0006X!µå­T²<\x000bÉ÷ü,¤}\x001bøóMÑ)ì©;o¥áâ_?Ôwf\
Ú¦</·ê\x0010|«§¨7Vðat)ZR+3éÛöÝwÿüéßÉxÁW,Þ#ûã-òU	§õ}uûîÕ«ç/ÿÇ·A¹\x001e\x0007eÊ\x0005ºb¢ÆÍNÞdÁT®ÿá<&ßcò
L¶ª× Í¥ñjìMdÆt\x0014Ñ@
=¤0
\x001e§·B!Ò\x0008nfH	ÅL\x001en[^?)ö¢\x0002ô #]?ë
©\x0002Ë\x000e%@\x001e¦ö4 ö1\x0012-Õ\x0019Tµ¼U<rÛ§7¢Óîòq^_høtvþÛa\x0006Î\x0014
³\x001aË¢êR´\x000b og\x0015\x001fÏD~{A\]°[n¾rõM1w¨ýZD d&jÆR$Îë*(ÚÏQQ\x001b¹ òî¼©öI¨
G\x0015-'¢H\x0014ZÈÊä:G¯çQ
d\x000eólNÒ
ìêt\x0011ª?n+DVTö\x0010U¨\x00066y:·AFQ(«\x0016¿]\±*óÖ
ï¨Ò*M£2'ÅÐ9ÏÕ[ç3W[\ôf\x0001T\x001e@åù\x000fhå~åcqpqñÈÏ;ñ8Ñ®A³ã¼³Ó\x0006Q`T%;Ï®¢ÂÀG0p>úá@ê8Oê%ÿb\x0005<$ÁN9oD¸&\x001a8\x0004qÌ§æ 
¼Öò,ºr¨zV. _\x0010\x0017è
#³G\x0010sÒî´¤¹¦yÎ9ËÄ\x0010`!Á!¥Âù
HjElå8©*'O®ó\x0011\x0017è
Ð³¡¹Ø
\x0013w0"±|}"t$àÐ<äyTClÆùØ\x000cÖ°\x0004n¢º¹Ú
­ø\x0015\x001cÅ£4¨\x0006\x0012ÅY\x0012-¶2¢ýRBO\x0010¿B' ÈÁÎr\x0003]¹yº2¤æÙT²d©P;\x00081\x001cÕÛ4 \x0006¶r³l9Ñ\x0016æÊVÅ,0\x0014\x0007x\x0013ýy_wÃ	tó'Ð*2/EÍC½¨ã¸p\.¡B5øº÷uC\x0014Å¨\à=lò\x0004F\x0015Ò
T~p+?ëV\x0017\x0012ÇàøñÌ¡Ìg9ê\x001e>j7~6Þ\x0014TÀ{a6í¯Zt\x0018Eª0\x001a<ÿ\x0001ýxWu«J\x000bÎ2-\x0018Þñ]hA®7\x0011ÃB\x001a3´±0¹7´\x00199\x001eÁâj\x0016ª\x0017pÇ½ ºkÎ\x0011\x001cypæÌK\x0014kEÉÚÒ\x0007»:ïºûó\x0011\x0005
¸b\x001a.þ`¨ëT}ñ\x00116[v\x000b÷è±Áù^Ì\x0004¬\x001d{­,àÈÏÚ)¸ûhÞÚ½z]nÑÃ{öåv­þ§zòþK}ëûñÝ×ÚÈýþã}O~âk°égY~ò«M>ÑwÕ¨'OßÔ\x0017¿\x001f¯ÞÖFî§/îyøk\x0000¡\x0007\x0008ß!@ì\x0001âw\x0008Ðõ\x0000\x0016` ÍHåøOÈM	º\x0017¯³\x0010}\x000fÑÈ=!%\x0011aémXè«üÚ\x0015õÎ"\x000c=Âð="=Â¨öCDÎ¿\x0001ëÅ³Ö¸ð]<±\x0013º=\x000b1õ\x0010Ów	1÷\x0010³ú;\x0017æòü\x0016{ù°Dh\x001fº\x001bÒ8	Qþ\¦l£ÇèØ\x0011è~ùØN³í\x0000µ\x0001ò¶iòìý»¯\x0017?¼ÿrñæóõ?}üýâñõ]è\x0006Ékç¼³.Ks¡;³w&ítóìéÕÛ\x001f¾¹xóêòùË\x0017¯/\x001e_NÀ\x001e\x001e(áÑÖ
²xnß\x0003àg5\x0012vÃExØÃC%<·µtmÖCæd\x0003w'yÌËÆs=:§Bô¢U'y©@ Ý
\x0010Y\x000bÝ£íqçàù\x001eW\x001a6{\x0001\x001b\x000f¤+ØÊh'5-ÇEx¡\x0017ÖÃÄ×þb½À«'I¤KthºÎ½sðb\x000f/*­\x0017Øtíõ&Þ\x0011cëK+ç°¥\x001e[R®0I­f\x0014Ó!\x000fF$È1éüªãå\x001e^Ö.q/³f«îoÖ\x0013yaÕz-fTJ6JóÑ~F¶\x001eH×\x000f\x001a'ÇÖ,\x001d\x00036bDä[\x001bõG1ç±ÍxañÛÚ!`X]Ä@ëåãë¤!ØI\x000b§'E|CÄ°ÚA7òT¿n,\x0011í'r\x001eÝ²ýaAÃ¢eÍ¹\x0012½¬d\x0011q\x000f}K×9xCÌ°Ú AËê8!U|ù0ë*Ýçð
AÃ*£µó)Ì9\x000b·`\x001a´\x0014a\x0011ß\x00105¬.l %\x0002õÕÑ\x0019WLÉÔÌ/i%%ÀUxCà°ÊÈaK¤
l¾ä¤ß¶$¡AÜÏ®Þ!rX]è Ï
jTÆ|äyT\x0008¸±¡\x0003Ð\x0001ÊÐQÎ\x0007k¦aþQpÜïÍe\x0001o[´\x001f\x000cÁ\x0003tÁ\x0003m[\x0019D\x0005×GÑñ,\x0013×RH\x001ae\x0015ßxÝPFmmgm7\x0002ÑòM1² ¨§Jü\x001aº!v.v`ùzÜXb[æÂyr\x000eÝjâ\x0002\x0003ùürløÐpù.¹ä\x0005ß2»À@~ $?ô¢ËSü/ÒÜËv:\x0012\x0017¼Åî6~\x000eßÀ~ d?Ú¼\x0017Ùý§/Ô557åÜ
ÓÊÓë¬'ÊÛð5\x0014üL/xx\x000eÞº 2uùû\x001f\x000eÇ\x0003Çã¿\x0000ßà~¨t¿¿?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Xí-8
f>5µVnµ\x0015¶Å
¯Ç£wöH\x0018­Êà)Óx!@Ï«åÕ|ÍÐ½w\x0002}Â<\x0013A;\x0014½èN.\x0002ßX\x000cgæÕtÍ©Ó½Ç.Îû\x0004ðRPÓ\x0019»Yå¹3XÙ-óéØX´¼\x0016ü«²áæþfÑÞ\x0019ö]\x001c GcüÄsh\x000e]\x0008öÞ=»¸¾xÐ1`B¨	¡\x0010­YÈñ(øiåÁG\x0005"áÁm\x0001\x0017./ÓÙÎöÓY·K"\x001dù/9\x0013]+ í¼U®Ftý¨å\x0013ç\x0005Ú\x0013¢Çl«ÝBÐ´\x001aQ·§pà\x0018b\x0004ï\x0011}\x0003N$¯åÍÐÅ\x0005\x000fu=có¥õÀ§þ\x0003ä\x001aÆôeÉÑè=c&\x001fúå»·\x0013ä×\x001fÞ~ºý|öôæýÛÛûÛÏÿXm
ZÔ7yý!ßn«A2ËÑ\x001f\x0002¿|zñxBþúÅã×o®Ï^<åâÍÿ:\x000f5>lÅW!/\x001cê\x001br¦\x000c¼¨&5cº7±Ýl\x0016½$ShVt^K¢\x000fñÐcÛok|»Yô)7`èM\x0012BÒ/ø2¦ÿdø±Æ[ñµæ\x0010\x0008¥oå}\x0017ý©]ùÁa¶\x0005_7\x0007_o>ùy6\x0012ñ+ø©\x0005õ<ýº*1~å÷.®IS×ÒÔèñç\x000fï?Ý KvöòæãÇ»\x000fïWD\x0004\x0018\x0006\x0004Î-%$Î9Än·ÉÎ{rj[z=þüâùë\x000btÑÎ¨ÀûêÅÒ~ªê\x0017°õ/`·ÿ\x0002Fªð\x0017püøn©EOÂè0\x001bq
ý
\x0010ö\x0014\x0010ª²îÕÍ¯w?¾_ \x00111\x0015¡Cº\x0006¶OÆ.æÂ_]|{õäùC	¨çv2¢\x001fC\x0004Fô&/NDD-É2+Kä·@\x001a2\x000c@¢¯\x00198Uí<YÍ(Q½øø±\x001a2ÖqD«.¦l}â,\x000f(ùØÚ.VX\x001dÔn?ºp¤\x0015\x001eÿtûóÝû¾\x0000#äé¡\x0014`@ÞøC\x0001h2ü¡,\x001fsùìêù:·©^FÐ¸MOnßßÞß¼;ûööîÝÍû\x001fVå´\x001cQHz'Xkøë{s¨¼î}rùüòúâéÙ·W¨~¿~0\x00066{26¦qFÐh]@\x0005\Ðý.Ãö¿·\x0012]Mö®zþ\x0001IýÉ=qáQ&V~ÍW_=úðùWRÆ?£\x0016@ñÂ±èÖóòmïRÈ3È\¤
+ÄùâÍ·¤P¡&ýêÉ51á	>Î\x00055\x0017ôp!Í4\x0015ÁÊ[4\x0011ÌåÙã\x0008ærõÀ(©ÁL\x0007\x0018jÈìÉ[«h\x0016}Y\x001a9\x001d\x001a´J6[ÔQ0[Ù.°ç\x0019#õyùØ\x0004¦\x0019¹\x001aÌõQ¾Á\x001cäÜ\x0001Uø)þÔ@½\x0005Ì×`¾\x0007\x000cÅd2\x0017ðÌ\ä
A¸Ô¶³\x001fj®ÐÅ¥³Ëoé
\x001c\x000c+g\x0010LçiS£`±\x0006=`Aåúq\x0004Sùàk-ÑÄ¢\x001a¥J5Uê¡r171Ðw49uâÊkW§I\x000e[¸8í-ªUu2¹LËD\x000fj\x0019L;ÇªÂ\x0004g·µJ¿GëëÀ(2-ÚÕ£\x001a,Ù-ºB7j_÷è}Ð>Ï¢"ù<¶ÀÓ^\x000f'2Ó[Î¾nô¾îRüÉdo\x000e¿ÉÏHfµó\x001f6³Fñë\x001eÍ\x000fnZ'2É,Ø}÷\x001e$ã7$Ýh~Ý£ú§6W&K!Ot  ¢2`Õæ×=ªßÐ\x0005\x001f3\x0017r\x0019÷¦k75ª_÷è~ò\x0016§2?:ÿ¼Ï\x001e¿åîøoÁj\x0014¿îÑüÆ£¼|ÆÂ\x0018'f,\x0013\x000c;\x0017Æ¸Mdò×=Ú\x001fð\\x0005>û\x001dm2#òÚæ&B£ü¡Gù\x001b\x0000äè[^¯é½U`Ebv"FùCò7c\x0013$óQD¶Ó\x0016¼ôq\x0014¬uù{t?mÎÌ\x001cE\x0016Îó\x0019³ÎÝæ'B£ú¡Gõ¶\x0000þÞÓ\x0008¿¬-|K\x0007DÖ¨~èQý¨§rDæÎ}Vý6\x0016é-z\x000c\x001aÍ\x000f=FË\x0000K\x0017ós&Õ¹E8FõCê·ÉæÜ\x001cÉ\x0012\x0007ï\x001dï¼D2\x001d7\x001d³F÷Cî7ò%ihW,_Òæ\x0015\x0002£Tê\x001eÕOcë
IÚ%1yÞ\x0014`dVÆÁL£aM¥ZÁ0ôÈÉA$sm\x0012¥¼¶5\x001aÖôhXÚÆ¢Xd*H\x001aÆl{m\x001a\x0015kzT,BP ;ÉÌ\x001b2éD\x0016\x00122·ÉÃ0mZ¥GÇRª×Ì@\E\x001fL¯¹)è5*3=ªF º,2
òÍ\x000cÖ
\x000fDÖè\x000bÓ£/¨¨ØH»tøc\x0006\x000bò178?eU£d|èÏ;òwèþxN,RuxÊù;^Èà¨vËåX¦\x0012ît\x001aýdýyC§L¥rGC¶éh;º)û£Ã> \x0001]\x0012TâÙúÜ\x0005|^Îñ°%{P­¶ÜYÑ.@ì\x0014ÑÌç¬\x0000F;¿ÒöUÅ×c\x0010}óyÚeyyóù\x0010ÑFH#sÎ
¬ømüv^#rÈ4\x0018úâÍÙ×gøïÇa¡aXÈÛ¸Vçyí\x0014Ç\x0007	f9¸Ïc¸¦Æ5¸\x0006\x0019%ï&\x0003\x0010(ðQ2áþÀeéÄÕjï(hEGa÷øÅc¸Î¾½C´ûÇNlH»È³{ZC ®\x0007Wj÷\x0002Æ3¸Î¾½Â¿v½ô\x0014VaC
ãØÔx!¦Ñqñi	%\x000fnÚ\x0006lSc-Ø>\x0017Þ\x0010vÊ»bÈsÔEÚ
l\x0003¶«±Ý\x0006lk\x000b¶W¹ú\x000cCIZY8P\x001a\x001b°C\x001d6`\x0007ÈCjs"D¼ao%p\x0001Ä\x0008¶2û
Ï4\x0003ñ|¦ÿI\x001e\x0007ü `¢<ð)zçåGCmý¡P\x0000?ysõü¡!À\x0015¨­Am7¨Nº·üàg¸ÍVk¨$ïj1v\x001f¨Ý·wyì¯þåÃû_oÞ\x001dSÆ&åÂô\x0005\x0011ØeÛaÊë\x001fD8p\x000bå_^<ÿöbi\x000bB\x00085"ô#êóÄáãì¸\x0010\x000fîn<Sãn<\x0008}ÔsË ¼\x000fo0îãºýåÝí\x000fSãÓOw·ïÝ\x001b]äq¼7ß5hy\x0018WÌV÷åÕå×SëÓ7WKEP\x0013[Ø
µÕEyÞ½ÿøÛ1[ëxe\x000e©Qn!C£¥ò?t\x000eD\x001d¡<¯¿Z*©\x0008MMhº	éMN^3M\x001eëM âÀÆABóÝ­{çîþ7K±¹Ì¯o?ÝÜý'5s\x001b»JH~E-ÿ\x001b¹©Àcøác¤ Î«\x0008ÜªúÜJ5\x0011éê¿îÎàëË×\x0017WO\x0016{)\x001a(üÅ \x0017ÊgoßÑò\x001d\x001a#HX\x0006²°\x0010+ðü-Xø	M/\x0016µñ§,®D56Y\Þ9ærÒº\x000b/¾íärÇ¯£¼§·_â²\x001eËQ
s+\x0017JÜõrÑ\x000b¹ÌÔf2}Ç\x0004ò\x001dùiÛwBKüÍ¢UÓB^"xx'
Î$t.\x000cJíï~}k>T7²\x001eHùîöãÙÓ\x000fï¤i¾ÿ<EÅ&Ä\x001c¤9\x0013©4;eBåù~:'Mv\x0019±\x001eAùôòÕÙÓ\x0017ÏÐ\x0018ß³XM×Ðæ«:L\x001bUÞp´4iÉ0mbXRÖ|7±¦\x0019Vý»ÀæKý¯!Ø|ÑGY-^ôÀº;Mc&VÔ@\x0001p2§¤Å+ê·Ñ:vü2¬\x0002\x0013Ã)año\x0016þuD¦?þË\x0016\x0003´\x0001\x0016¸ö\x001bi\x0003ú¼lØeX0§¼bTØEÿ\x001a\x0017­gÑF\x0005ä gÑ\x0016«`eÔihÉm0b°lño¦7\x00181k¦ý~\x0013-<\x0002.R&ÜxRáâÕ\x001bìØ\x001f,\4bz!ûiÑé-¦\x000c\B¦·¸LÙ÷ªÒ)iÑé
¦<¦³\x001dØG\x0012ÊÅpRÙ¢òÖ[lÙ\x001f{\x0012Ðé
¶ì\x000f-\x001e+½ÁÑøi
3ÒRdÈ¸:ñÁÅ°Ì\x0010*Õ`5pSÁ
FpcÁ=å=£ò5ØdÎ\9\x000bÉ\x0015ÇgäõU§tl¨¨
¶Ø3µn°K\x0001\x001bDºÐæ\x0006¶â¢-MöÌä)2¿z¬tÅ·1&\x0012\x0017/\x0002l1h°tÑÁ&¦sÛ\x000eIWQ4'°DºpÒ£¿:l	Îþ`áâï\x000e[LÚ\x001fK\x000bç)ñ\x0005SâkÜÝ
¹Úb	G\x0019þ\x001cK\x00041Ä6m¿oáþ§OÁÍe¨_~ø|ÿùO¯nîÞúÓõíÏ¿=M´ÇÂ8«éM³6p\x001a$¦6ì©¶x¾¹~söêâ
¯/-gÒ¿ÿ\x000c\x001f¡æÌÝäÿþùîìÙ÷|óùì5M{SÛ(a:uëêI¤¨ÌÄ\x0019§\x001boÛÇQg÷¿<»xsö&Ç­âÌ@Ë\x0016ù~\<´vÂM@ïz¢Ðz³\x000evf$ùî>½ÿÛ\x000f¡Î}PWþý\x000f\x0012\x0019ïå"¥¤	>´N\x0012ß\x0006\x001dÛ<\x0007uÝ_?¹\Øµ³£Èeeùß×Ðb\x001dçò³¦yL'Îº\x000eb\x0017?þï|ª\x0013Ã7gÏnÞÝüp÷p¦fûe½î\x0010í¨n)ï\x0019G\x0007T·G
A]<½øúúj\x0015\x000b§RW²Øi+íÄb§q\x000f9kîYcXe÷rEÖåg@Ãë¨ê­£Ç?\x0016@®·q4\x001fJlÕ\x0003÷hRÚ;Éed\x0003}³¥ËVØ f>¶`r£\x0019:	Äg´Ñ±G\x001eÝfj4Ó¦M®@¡bºXÎ¸²|ÿ#D·ÍÖl¶
Ã.ï\x001fþu	dlòÌ\x0016R{ÿºÙ\ÍæºØlâ\x001c\x001c~Q+v\x0013#\x00021Fj\x001b¯É|\x001fqy>\x001e¢éiI¾ FÔ'-ußÂ\x0016j¶ÐÇFí³)³¡"ã\x0007A{@cµ6¡¥\x001a-õ¡y)NhVÞÚ¦IÃ-À¾%ì`+\x0015ÎrØ&#Ôs\x0017ÐQ3¬ÞPíZ¾\x000b&\x0016[¤·Î\x0012ÝrWÙ§Xè 7o*®dsY4IØ @º­û®Ð&s\x001eøÒjÊäKëÊ¥Ý¦ê`\x001f\x0010ºEh4;cVC¢ª\x0008AR7ÑÄA\x0019Ú3° ê5õ·g×\x001fùê<}ºÄIg71ä?ªs6s"\x0015`¿xÀ-`¦\x00063}`!/@2¼\x0019^\x001cXöGÀ¨M`¶\x0006³]`4ä$á5¥\x0011áô1æû Õ[À\
æºÀÌT!;ILM#Ó&q/MÖûþH\x0017¯É|\x0017u¹D¦¨Åp\x0012òZd\x0006ÈBM\x0016ºÈ|¢i"\x0013\x0019­6Í7S\x0019V\x001dz6L\x0012®ÙØhw'\x001bµ1ÝË*[Ã[v/ñn*êãÎwSË
Ø·\x000cÇÙÔ¾¾PE_L÷·\x001f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=9¿>8º¹<Ù£¼GÀ¢\x0004\x0016ÀÜg	\x0011¦óU¢äó£/\x0007]À²\x0004ÝÀ¨!ÌáA©tE\x0016Î+t\x0001«\x0012Xõ\x0002CÝ0¶¼À\x001b#\x0002\x000bj,óã\x000f\x0007]Àº\x0004Ö½À&\x0016'ÙHK¸,§O¼\x001e}Åí\x00026%°é\x0006Ö¹ÁÌ:ºÉXâ£%]À¶\x0004¶½ÀP¢[Â\x001b|\x0016óã½Ü]À®\x0004v½ÀÂ\x001fêÄ\x000b=<.ñ\x000eV-,ûZ¼¾äõÝ\x000b£cX`cÕ)k\x0019Öw,¤èá\x001d"è6X/0ã\x0007Ó\x0016ftg
\x001b\x0004o\x001f{åè"®\x001d]¯§ãÃ¤k\x0018çpáÆÕjVW÷ºº\x0010\x001bcéDì4¸ÆÞ¾¼\x0018#é"®\\x001dïõu\x0010ÁÓ\x001a0S 1£Öt/V3l¼òu¼×ÙA
1ù\x000e\x001de ¢*²çÙ;Êvw\x0011WÎ÷z;Èµ^A¸~¨,5M=êÜÅÅ]Ä·ã½î\x0019Iª\x00152uH»>
\x0014\x000b±æj¸¯ã½Îé¬©%ULfEb\x001d\x001bíéè"®\x001dïõvLåG/)\x0005*B8owÎæ`»+wÇ{ý\x001d\x0003y\x0010\x0012/°
re¡Q
\x001ebQ¹\x000fÑë>ÂîÊ­ë"Ü\x00120£[0\x0019K¯\x001d!f©sÇð\x00071wüðüt{p¶}º{¸ß~º=°|Æb°k¨
fBxÌs\x0015BÚÄ\x000eÆÝDÏo®\x000fÎ6×'çgÓcø¯z\x0011W¸²\x0013×XzE\x0000r
XÀæ¸\x001f×zhuI«;iaFw
/-sxÍ\x0007UØtÞ\x0010£SÆ{pmk;q¥&û\x001b,\x0005-.e\x0005A~m-\_âú>\Í\x0019á ¥rX1ê¤ã£âv\^´Î£¦Âå\x0008EcÂµ*\x0003óPn§y^WT¼¢W0Jù\x0008\x0012z"/&ââ~¥³Æ+ËÀ;Mb\x0012>;z\x000c\x0012KÖ\x0002ïZ»W¶¿zãÀ+ãÀ{­Ã¿\x0019
ª,Â
3IÃ!üãW'Ú~ùr{pq\x001bgTÊx!)\x0011\x0011ûmul\x0017\x000fj\x001e\x001e>:yw±¹º:>¸8\x000e¸ûæ#¨«A]\x0007(³Pú@%Ø3XUïIUÌx9f\x0014\x001aA½ª@áeµ}Eq9¹IïË°*w\x0003¶~¶RÒôP*J¢\x0002¨v\x0008+máé³\x001f4Ü[w£¡W{ýýeûüiN7&y\x0013n\x0014¾¾ÅÁ:ø*+'G\x0005À¼ï«ÍÍé\x000cFY2ÊvÆbBq4vÍ	zÕ´õq
ªdT]ëHq\x001aÊvp\x001di<ÔÜh`Ô%£ngt4æ\x001dFÁ\x0008Ë8ln`4%£éøÖ*«)ÀÖÄo\x001by­¬ön´%¤môü;·\x000cUB]\x001e8nÇSµ®dt\x001d\x001f\x001b-¾á®j£XJèKBßLèØ0hP±t:ÝÈñ¨®	rÈ\x001dGûÈ:(\x0005$^ÓRJzøp\x0006ÅZ9)°Ü@Y[ñv3î@\x0005ZãZjÌm{g\x001dÈÉòò\x0006HQA¥Òälp­ËZzÁÙ,?Û¼r6¼ÝÛ8a!¢LK\x0019\x0013(ÒÑ h«&;n\x001b(+wÃÛýM8Ë \x0004ª3Î\x000b:árR\x0000¸²r8¼Ýã¸\x0010\x0003Q°\x00168Q:5lË\x0015\x000eOårx»ÏùmÖ²ò9¼Ýé8\x0019KÒZ:ì*ò.ÔEj¬\x000eo÷:NZð6\x0014cXÔ:\x001bb\x0015²r<¼Ãó¥¤\x000fn\x001d¥\x0013b\x0002Ör9¥¨<èð<JQÁ$<W&ké9Ï¡ù¤°T\x0003dåxDãQùQC\x0016\x0014/*Ëìx"©
²r<¢Ãñhg\x000bÂô\x0011KéÝ\x0001¨\x001cèp<ÊPJpTuã¹\x001arµ¬\x001cèp<ázci-\x00059q/òÈ6¹Bh)*Ç#:\x001c\x000fL9Åm\x0019n=´"Û!5Y×@Y9\x001eÑáx\x000cM3\x000ekÅ=¼¤\x001a
«Ø
G¼²é¢Ã¦\x001bÇ	ØRà\x0011W"\x0007Dl{£\x001bÚéÒgûún<BÕa\x0005)áüxÏ\x000fu¯\x0013åÎ-qÛww"·Ïí>Rü9øHÊ\x0016xãÉRò\x0019 Vïd¯Â\x001fPöêj{wÿtpüËóO·¿¾\x000cÊ£·\x000cÁñQÖg÷ã&?ûÕæäìúàøßn./ÿü2©(IE\x0017)\x000fnÈà\x00144b&¸A\x0017p2Õ\x0008+KXÙ\x0007+¢\x001a\x0005Å©+Õy5x£ÉDL#¬*aU\x001f,3"[(5<"[(=þ\x001eÐÎªKVÝÇ
"\x001bý4èØy¯êÓCf\x001aaM	k:a}Þ\x0005Úb	W9lZiYmIj_ù~u%¬ëT½¸ôXª³m\x001d-ì@õ%ªÝë:dê¢/`¯ÚÄÊúpÅñU]¸\x0016ÕÓ\x001b\x0011

Þ+G-\x001a\x000b´¾¦íÜ
aq)\
+\x000c-nÖ\x001e} lÇåÕ\x0011¼ó1\x0005
\x0010\x0011×\x000b\x001c.\x001d¼\x0002£NTã§nù3qÞ\x0015(Ð¹söûç7Û/\x0007ßß\x001e¼Û>ÿ4§ÓW8§\x000cKC²Á0%\x0019ëµØäýïë7«¯\x000fÞmn.öv&ë]\x0002;g{-¥ð\x0001\x0019ba\x0000yFBoF%²ìF\x001eäºHl)`Èw5bU\x0012«^bÐÇ7\x0008l©V{ÚÆOÊ_·\x0013ëXw\x0013sM>\x0003&§¦*ðpðHòÏñÉ\e;²)M7²Ø¹'T¾û\x0004|äb=b[\x0012Û~b\x0007SÇB\x000c\x001byÊ/·\x0013»Øu\x0013î\x0002
Í©#!uÞÉS Û}ì»Ëstø\x001c=\x0006	-Ã79þ¥\x0015¹xªÔCãl\x000f³¢Ü\x0008ñ&fÊÐ91é¦Ûk××íûÂ\x001e á?apd	0Ë<\x001cvzÌN3såûx·ó\x0003e\x000e²rVÒ@[¡(«ì¦³ÊíÌóãÝÞO\x0006KAGÐ	\x0014-òäu§&'E·3Wî÷û¿`6<Í:Í½\x0002?\x0012³\x001cÇÛÎ\9@Þï\x0001Y¢^R=ÔßéôjW\x000e/ð\x001a+$\x0008½£(\x000eÏãÍ¤öfG(WäQc0·í\x0018ÁØ{T.äNÑtY>ùOÍÕN²2ü\x0001ù>Ý\x001e\x001c=<ÿ|ûø4£!ÃIMNÐ=Il>§~øT&ýôôøàèüæýñåõö\x0011\x0002\x0015%¨è\x0002ÍG\x000e@ñ½\x000cô1Wå%§|µ\x000b*Uõåá\x001f;P'§|$¾¢äâ\x00176¥±Y¡~Ü~¿ýòô¸\x0007µ%DØm\x000f-I`kh¤FX¯¨ÊÖò)<oaµÒõ
\x0000GêèÇÛÏw÷Q!ëÝöîïs¦]úÀ½\x0001Ú(ÐÇ´Lh9?f¸¾=~wr\x0016\x0015²ÞmNþ}ßN%¬ìõì\x0010GÁ(\x0018tfq\x0001¯ÅjKVÛÃ*Âÿ\x0015jxS%Pá°CRvúÔ÷r\x0005-B4X\x0004jÂÃö'5\x0005;ZfÔ\x000eËëýÚµaÃ5ØÐ´%¸^ðT\x0018\x000e\x0006Z\x001fW­ö+ïÚ°\x0002fÓPë.l¶\x0011VHJÿ:7si'
\x0017ÑêV÷ÑêÜ×$=L­\x0016ÜK£®¶Ú´¼s×BTQ£hEî·jt´p;­¨v­èÜµ6ß\x001c Â9¤ÍÕº|\x001dË%ª]+:w­ÔÕPlÚ<ÄÂþ*°Õ¦\x0015Öæ²|xÆÌÛæcØÑ\x0014C\x0007lå\x0013D§Sú)\x0014\x0012³©T2Âì/ÜpV­Nè<aVä9f KéwN\x0019O8µÓÊêÉ\x0005'\x000c%avBZ¹´\x001bUÎì ­\x0003Î#f$uP Uï\x0007Zç(ñÑGÌ°«\x001cB/øè\x000b´\x0006ÓîÕç,\x001b©ÑiëÝeæ½Ð5§à\x0006t\x0007\x000c\x000bU\x001b½âöláê\x001bcÛ»3°$\x0014vF¼éÄOÝÒh,ÜúëÛCø¬X\x000b
æOOÛw-6×YÁ\áì\x000e\x0018ú>©î	Êå××	EI(Z	A\x0019Þ%D\x0013>=¶[Áãz²Cf>¢,\x0011eó"êáöÅD\x001e\x0015é±ËÑ19©¸?\x001fQªý;[ºsiPîDD-öÞ\x000fÛ\x0008uI¨Û\x0017Ñ\x001dz¼\x0014æy±Ñ\x0005vz6Ä|@S\x0002f@çK)a\x000f9u`f}\x0019393x>¢-\x0011m3¢á\x0019ÑI¸³¤E$Å`1§^=æ#ú\x0012Ñ·#Æð\x000e/ÔPEz\x001bQó&Ü©§Eç"\x0016ê«lxDÏ\x0008Eèôª¨9i£{\x001fôýb£Èk³Ýn·MµQÐ\x000emd\S\x0012I1ÛÙáæÍÛzE3«e\x0008:\x0014\x001eiÍ(#\x0001Gg)ce¹y»é¶\x001a\x0007	\x0006o\x001fÓèéPSgãr³È+ÃÍÛ-·G)9ì#r0ì\x0012\x0015Ã\x001b\x001c^\x0019mÞnµ­!\x001d6¥\x0014ÍgpnÞM¾Ìg¬ì6o6Üá0ÀcjR·\x0013Tá´£}È'\x0007Íg¬\x000c7o·ÜîLËoe«ìDW1ºöu¤«\x000e¸ZWiZ³gE8ó\x0019+ïÂÛÝã4ØVIÛk%Ý\x001fCL¶Ø.Ê½v÷Â²{á^CÝÔ&W\x0006ùÉzýù\x0011íþ%\x000f\x001dCµ\x0008N!ØYì\x0003E}1hö/!®áºi\x001d-\x0016uÔy\x001d'\x0003ç3VþE´û\x0017\x0017_cÒ:ªü8'³z©ì\x0005ÏXy\x0018Ñìa~pGTnF´»\x0019g(i¡ Ë\x001fÝ´¢û¿_a\x0015+/#Ú½PÔõ\x000bÅ¨ÖæËÕ\x000e\x0002ó\x0019+/#Ú½Ìo°\x0011íN&YT4\x0003ÏI\x0010SO\x0016¦Î\x0007¬<h÷0gË\x0018\x000c¹AËHÅ\x0016^\x000b4¶ ÊÊÁÈv\x0007#Ù!Õ
y\x001a6í¼¦\x0017 5Ù<\x001f±ò/²Ý¿xGYi\x0019\x0016T\x001dE\x0011?Ý#?±ò/²Ý¿¤tyªmsô¥=ÜÝ°¶m²w>cyjö/1¶ÅÌi\x0018bÛ¼5ó\x0019+ÿ"Ûý\x000b¤Æ±Þ\x000e®[*irYãbÂÊ½Èf÷\x0002-ÉÚ@\x001c´¡4¾\x0017\x0005ó\x0011+÷"ÛÝb\x0014Ø
£h~FÔ4ÆÖÑG§6ÆÊ½Èf÷âø \x0018
\x0012×xaµ*«\x0003O
Íg¬ül÷/ÊQ\x000c:	ph.TËQ´³\x001c±ò0²ÙÃ8nsmÒP1×Ôúåö[Uö[5ÛoW¨òKR\x0007Q¬«<=åg6ce¿U»ýæ¢\x001d(´¤j\x001få2Vö[µÛo!¡­<1
RñtÎRÔ8^ZÒÆX?\x001d´Ûo­h\x001dðÚ\x0005U\x0012øIù\x0005Wí\x0016<Ø©\x001fG¢éñ¤\x000cäìdßØ|ÆÊ«v\x0013\x000ecp\x0019%
\x001eôÛFUÙoÕn¿eîmÆÅEÌbé{ÆÐÍf¬ì·j·ßÚç`"\a\x0018ÊÜæ>!ÞÄX\x0019pÕnÀal8\x001a\x001e.\x000eI5\x000619£\x0016Û\x001d]]\x0011tû\x0015\x0001f/y\x0012 Jw/é\x001acíò\®|n÷1a\x0019Q%\x0004
Ùx^GJLèå9Q]ù\x0018Ýîc % Á\x001cåÉ|îË"áÅÑí>FÊCmp\x001diê¨\x0013âp\x001d?¹éÊÇèv\x001fc²\x000e&¶£e$\x000fc&ûëç\x0013ÖÏÓí\x001eFjhN«Hz§0^\x0016q9aå_t»1&·¦{]½^å¡ÃfR¢h>båatqô\$¼ #íYnc¤ÏXy\x0018Ýîa,£\x0012´ð÷aNëh²6Éò®<n÷0*ß´D\x00144N\x0018AQÖø6!ÊÃv\x000f\x0003/¨<\x00106&F;.\x0008VíjC¬\x001ciw0ðbI	ì`ò\x000c©à\x0016\x001f\x0018SÙnÓn»\x0003	\x001d\x0018Ø®«ô¥Å
_º²Ý¦Ýv[mãP\x0014Í\x0011Q[:/bRËg>be¼M»ñÖ¹0F\x0018Cä@
/·¶//"3uyQ»ù\x0006½C,.\x001fÚ¬=½fY¾¼¢ÃTæÛ´oU\x0018àN(I¶-·Û¯ð¥+ëmÚ­·ËA#qDud4Ù\x000b²å÷\x0003SYoÓn½µ§Á> ´À)øÎÞlràÀlF[oÛn¾¤|#L`¤ä·¡xÇÀ\x0000¥ý¶íö\x001blñá\x0012®\$\x001dIÉo»\x0006cuA°í\x0017\x0004§òÜp\x0017´\x001fsg[^\x0004e+'cÛLðÏX]\x001dlu>×yÔq\x0008n¯cådl»qC+ÔO`<aèÂjìòK­¼m÷2Æ\x000fjmÊ²°vtÚI\x001bcåel1ThÄ¼£\x0001s>\x0017Må5\x0013¶2á¶Ãç2æ±Ë
\x0010i1nùv¬L¸m7á\x000fi(Aï^9JçÙIeÐÙ®2®Ý<\x0008\x000f÷ACp»ÞÐUæÑuGUßÁcAuYúÔ$¸`Ô¤FÄ|ÄÊ:ºvëhsÑ\x0004\x000fÛQâ§ÖônõòR(WYG×n\x001dÃe\x001a«ª¡ýS¢·¶t!\x000cn{ù§®¬£k·á\x0003Ë¸@ÑyÊÒò£«Â[×\x001eÞ\x0006ÃCóCÔ¡B78z/¯rÙqífÇÅ'Ët©ö$©âAÄ\x000f\x0019\x0017ß\x0006}eu|»Õ\x0001y\x001a°+Þ¼\x0019\x0004SÙrÆêHûö#í\x001c½÷ó\x0010£¶T\x001eÎÍb\x000fã«ãâÛK`tC¯±PÄ@Mª±Íg¬\x000eï80>«õ§DEbäY!c±ùæ;
n¬}CzNáD¼\x0011¢±´\x001f\x0017\x0003Ö-\x0008¬}7\x0006ãÍèªe\x000bÀ¬×::\x0019¼
²®ógíÛ\x0011<\x000czA¡©ÐßÃh\x000b\\#Ãëî§([Ó
)³ò-çô
ì)\x0013\x0015âÆå_».Pgí&<0R8Á|w`MÝ¸øÅïv\x0017u\x0019E¥þ9\x001a\x0008ñ\x0018A.~òç;­;í½;.\x0004µ
¯	>?a:o{WùN{L{\x000bw,¯2Ó£ÈpY¾õ©iï=ñ<\x000eKK<õÇèô6K\x0013øN_G{c\x0007|lÌ£À°þÚ/>ÛuÓ\x0004oï¯ÍP\x0019\x0002&Ðá±¡bøÓÅõ©iïH\x0000FêL·"'\x0000\x001cûi-óùõ±i¯÷wá@c»23üÐÒ×\x001e$6&Íx]KÏÛé=t½fSéw&?øÅn».VçíÕêiªb\x000f\x0006ÊÌòÞ7^×óöbpÏ\x000cåö\x0018Ôq%FO}efZ@»áò:è:àõuûêî¯áo\x000bÅ\x000c|Ó?iïç¡Ç.¸Çæ~\x001eª÷ú
½[»¨Á¥õ¡þ[Üùòò\x0015~y¡¿{º}¬S\x0005ÒÞµ'©ÛÌ\x001d
jÚ£&R³<\x000b\x0014Hw?¼îøðÿúN¤pSÜ%ËcÇ\x001euªùÂ~%íyor²@MPh¨Y©7©ví\x0014\x001eq(Miiú­W<×P-/ÒÝ9Jªã(Áû\x0012é\x000e-.FÚå­¯ìMSÏ\x0006eÚù´7õµ\x0012ãKª\x001a¶µvÂª¯¾ºø´ýx{pqût÷\x0004\x0002Ào¶÷O·^feÌRöW@Ol\x001aýd³:R0\x000bcwóÓÍÑñÁÅñõÉ5(\x0000¿Ù]\x001fNk\x0014fèï~©±éçÎ\x0019(BÅA5\x000c«\x001fmÆ\x0018ç\l­v\x0016\x001b\x001e@Âb|þiûå\x000bÈ,?~Cë\x001c\x0007;\x000e\x001eÀÊÑ(åäÝÅæê
ô/æPÊR¶Sz¼¶\x000b&òC.i¢
Pk0êQ÷0ú¡P1OL	ÿRzÔ¢6cÖúc
ÐN\x0005¨ 4*!üð6Z5i^ë;AÝ4<\x0000=<?ÝÂiº~|øu°4^v½\x0014à]SP®Á)9.\x0011~s}\x000cçèúòüÏû\x0004Ç\x0010´TçI1¤KJm\x001b\x0006¡\Ñp/Å¦\x0017\x0007rtkÚÔörRL&ün|\x0011
§	
+î¾e´ú
Ô¿Ú%å²^RÙ³¦¿Í>åª^TÕ³ªÒäÌWòÉÂ¡¡
¨£jsQAô¬rMð\x0007¥k:	ÿþçï\x001fæ=rà=CÊ{ç'j;ZÕA&êäìèüÝù×ç/\x0012Tt\x001c©Í
\x0013¹Z4GÓv´>¯\x001dU¨²\x0007ÕðDPY\x0014ËsÜ\x001dµÜÚÑÜílÒð_¿£ÿ.´.F*Üä7Û»/Ûû\x0019;5Ê&à£+\x001c$¶\x0011ÒÛµªQ\x0000©züfsrµ9Ûs¬V´¢VäPJä)o!À\x001a^¼&ëf\YâÊN\É¨ÀYå²®pâ(\x0000àSùñfZ]Òê^Z\x0007½sG²CÆÏO½¿·¯m\x0019`¥õÅÖ+\âàvêý\x001bþ\x0000öï·w\x0007ßÞÞ?Þ\x001d\x001cý\x0018..Û\x001fêå\x000b¢©µtäìa"¶¹áÔÊÑëÀn6'\x0007ß\x001e]\x001c\x001c}\x001b..÷çðÇ/R«Z-¡((\x0017\x0007ïJÂÎsÌG\x001fÍz±Mma[\x0017ì©Íú!\x00073Ú7ÔíJl·\x000c[ ¶Óte´n¸èêCwb\x0017²±yg	·È%\x0013 wã[æç
éå®$_t&E.Z÷4V\x001a¸E¾X®¸»yu(ù¢S)ð%[0OS\x000c\x000bl;:g¤\x0017»:|Ñ©Ì}Î[êª±Cºa4@êÅ®\x000e%_t*5éÆ	å)\x0004µ^.\x0004ÔÀ­Æ-ªS)\x0016JC­-Â
bÝ>kE¨Ññ\x0013ÍÜ×a)ÕÑPÃÛOÿóÿõíÃÓí'ø÷wÁÓ¿L\x000e\x001aÞX¶\x0018\x0015\x000fÑ|szAñlòa<Ü¢N\x000f¾=¿>>¿}\x0012üýËè¢D\x0017Ð­ÌY?©=ÌgèFgMÑÍÒ.Kt¹\x000cå@\x0010FK¢þ®\x0015Yªl²\x0013ª\äjÙ~Qºêa.Jm\x001bçºÚÉWë.tS¢enrI¤4\x000eÃB\x0010©Ç5WØ\x0015ÉmInW;Ýèn\x0019ºµ§\x0001ý.+ç\x0004\x0015þùÑ!BÝä¾$÷\x000bÉYÖ¸\x00086.îÜeÜ3óµ\x0005i\x0011±¿Ð¿\x001c¼Ùþ}û8ãf¢
'\x0019[ÆàXæejnpK{³ù÷Íå¾ÜÝî%a2{\x0013¦À²;©\x0006ÕUèÆ&\x0005­é
1R²Òj¨¿J4Ý *'ç'ßl[0U©^ëbêRwP:6,¦\x0000u´jÚôôò\x0006L[bÚ\x000eL(¿C\x0019\x0011(È"1r\x0012¨vnôJØ¼ej&­(½·ÑòAB
QU\x001eU>þ¬<\x0017Uò\x001d$y4IoïÓ\x001cÜ·ÿøïûü÷ã6\x001aÔ·ÛçY\x0016\x0015\x001a¥ÒAå¥Áb\x001de\x0018
cAÏæýñY\x001aûöøìør\x0013MêÛÍÍ~wÀw3J<\x001a«?@\x0019\x0010¬Âô¤?¢¡çuå Ë Wø	áz?Áe-dééB«íh³À¢ Ê ÿ\x00040u>ýpd±·\æÖ\x0016íF+U\x0016ý\x0004]þ\x0004½ø'Hç©l
J¦u2ÜÂçæJËVÿ	¦ü	fùW\x0000½*û\x001a±ë[
ëíê\x001bÉ?Á.ÿ
a÷`ê0\x0015Õo%Ï3âÌh5æ¢àÊàVø	Y<ÈE2\x0012k¤ìÚ?Á?Á¯ò\x0013°2$¿¦@5Æã
cK~Bå)\x001d»ø<+RTbY¥XxÛâGCïE?¡öÍË3$IÁÃë*$j>°£Ã\x0007\x0017ýÊ=óåþY\x001aPxTß¿ÁÈÜ	·þo¨ü3_î a+á+<ô%¡|o±Æ*\x0016ýÊAóå\x001eZb\x0018Í\x0007Éð¿A©çÑ\x0004Ñ"þÊ;ó\x0015Üs8Ã¤\x000cÃ8ÝþÄÐ?âF+L\x0017ýÊ=óåþ\x0019´vé3c¡S´-àµ\x0016_AG\x000bd\x0016ýÊ?ó\x0015\x001c´­z\x001d±\x001cÉfäF\x0011\x0017ýÊ?ó\x0015\x001ct¸óÏ£É$qg=ëÑ~©E¿¡rÐ|\x0005\x000fm|ÞJ\Rï°ô*cüèmsÉo\x0010\x0016Ë=´ðY\>Öà§ßÀ\x001dËj°£ï\x001c~Cå¢Å
.:ì%\x0004¹¼r	ñè£Þ¢P_ {è`C©{P­\x0002BÜè\\x000f?±Zô\x001b*\x000f-VðÐÁ\x0014\x001a ÷\ãwYKjõ[T\x001eZ,÷Ð0í\x0003\x0003V!ò\x0005\x001424Tß?ª'¾è7T^Z¬à¥Ã
4æ g>TØQm´E¿¡òÒb¹!\x001e¼%yé`q©!p\·qÑo¨¼´XÁK³\Ú!X|\x0007O¦57áw\x000e-ú
\x0016ËÝtøÿÎºF\x0006\x0014¿Qcæê¦µòÒb¹\x0016ÐMÆ·¹\x0013¹&v4Ë¾ä7ÈÊKË\x0015¼´ÐTmã\x001cõæ\x0017,§GGÉ/ú\x0005Ë}´\x0008Á\x0005õùpE?\x0001²õY°qíXIVNZ®à¤Ã}&vÀK":8I2¯îàdæ^î¤\x0005\x0014à£#-\x0017(
¥ïà×6¬²rÒr
'mI\x000f\x0002^ qº\x000b×¤äÕêùIY9i¹ÜI\x000bÏib\x0010â>\x0003§XiTaÑ/¨Ü\îÞÀ\x0012Ñ¬9aè¹\x001bC%³vÈ*+ß Wð
Pa·d\x0018í\x0019±rãÊË=?3U¿\x001dÂ\x001färç£íývFgñhÏÅçÊ\x000b3Õ\x001cX6gé¦¾Ì'J>ÑÎ§óHÑ`ñ-ÍY*àR2(ó\x0011e(_ß\x0012ªO½>>]òé×ÇgK>ÛÎ'r
!$ìi\x000bJ\x0011'\x0008_Bd^í´\x0014Á`»¡¥èß¶?ß%Q\x0017ú´d\x001e\x0008ï"QDDÃuÞv´ÜÓMôo÷'Ç/AÊ\x001a\x0012þ±\x0019çQÐðö\x0001zoQfKæ'¨)Õ÷9ZîTShYVS><ß}9¸Ø~yº}Á
YDüì0§\x00053&r´\x001e`F[~z~srup±¹º>¾,JdÑ\x000c\x001e\x0014£ú<7\x001a9¬\x001f\x001d¤×G,KbÙMª,©;iH;Ï$ä}\x0011p#²*U7²Éº\\x0002\x001aî\x000bNÏ.\x0013ó{úu¬»\x0012ÿLòÍ!.§Y\x000bjÔ8ô\x0011Øt\x0013Ãô\x000f¼ÝY\x000eaaêåÎcGX:×x\x0010óH«üK/4ãPªD; y¦Vû^fR+¿Ó1«|ì=zêÕöãÁéö/Û_ofÄ«.\Ù¸A
"KibçH4ÛëÑç£\x0018¢^m\x000eN7ßlþ||}½'Ø&dQ"~dA³©Âµ2HÎª|Y\x001b-cèCV%²êG\x000eJÈ\x0012wÎR/Y8ë­²)M7²ÈZ·y*ÙqÓüø\x0018ú\x001ed±³1XÿÖ\x0008ÐÜghNÒJÔ\x0002\x001e ÇrBmÐz·\ç2r\x0008ÞmÃ¿ÿåönN#LEEYN'X\x000c\x0012Ë\x001cïfÂpèÝææèü,üÑ>\x001dÝbrÉÛasÛ,ÓÊ
bå3Ö¡&
;`e	+_õÊÊ!A\x001eaëÃ5z¨.ãÃ\\C\x000f¿rjêl#®©6B¼¸ôàjFªÃF\x000e\x0003ÙhJQS]Usiö;\x001e#8SÌ\x001düñv{ðîöñóÃß_$e!¤x\x001eP\x0019s6ÏeScÄÿx¼9;xw|ùîüß_æ%§lç\x000cÿ?2ËAÁûÄéò+¡,3oâT%§êZÏAß0\x0017\x001c<yäÞù©ëz\x0013¨.AuÏBÝ;iµ\x000blß\x000eqM.\x0007aã²5­ ¦\x00045= \RÆKjë\x000fn6\x0017\x001bÉ!M ¶\x0004µ= ÊçÆò\x0010Ä¤95Î)ºELÔü5º\x0012Ôu¥\x00014Ä´¨X\x0015"]z`ë¬¨/A}\x000fhp£a`Nä\x0015ÕY\x0019Ýjÿµ\x000eE¸*Î\íúö*\x0000W8!|{µð§2`M ¹ç\x001dö33h=[\x001c
ëÜ0!ÍûÏ\x0006åv'öã6çÜ¿¾ýòåöñéö~V\x001f;^n\x001erÚ\x000f\x0015ý{ºÉ®/¯Ïöu¯\x0013¥()E\x000f¥ÊF\x0014V\x0013³­Í~~O7l\x0003§*9U\x000fg\x0008M)zÊS\x0010âh/äsoâ4%§éúê.UÐD@ë)éÝ}zÈÀ\x001cÎ\x000f\©jw¾	\x0010%U\x001f\x001eAóíþó¿6Ï\x001fn\x001fï~ê\x0015À)'XjrÕ\x0010ïâ\x001eUbTBéâü\x0012dß\x000e67o/OÞÏ\x0015%¬èdH!\x0016Ij\x0016ý&ÑgeùXJ®\x001dV°²\x0017VRW3"é<\x0001,¨ñ¼r;¬*aÕ+_YSÂNØp-I[Ö8^ñ\x0003«"
}áGýVÖaDF:_¢÷9\x001a!ÒI¬ZJ?î\x0003.FG\x001eµâJ^--üc§APà©h'Ä\x0016h0\x0008d»VÛ	<\x000bl£ýÚv\x001b°4PAA\x0011¯Àeü¢ÒûTã>uãbË®cØ"§c¹N¢e£%Ç=¸\x001fjÜ\x000fÝ¸
qÃ\x0005ÆrZ]Ú
\-âevW\x0018ÒfaHxº½Ú~ãn9Ib@¥PÍCRÃcór¿¾tàËx²Äx¬ÀTÁ\x0016gÚ!\x000c¯fâ©\x0012OµáÁ³·Â\x001aAéHóß2\x0007S,¥Ó%n¥3¹ÜI1*Ù²T6àØä³¹t¦¤3tÊ\x0001\x0012\x0015cÉ´vpy¢¢¸}U
³ð\ç^\x001d/ñ|#^\x0008â
î<E¾Í3ÍÇK
ð)\x000e	pÛH¨\x0007Y\A/íÆ
»x\x00015ÛÍØ³A£3ðTÚÇH«ü!Øc$\x001fe »\x001d5.Q(- BÚ¾·S¶û¤Î\x0006MÎ\x0016JÍQè!\x0016àÜGë¨d!,ô¤Êb\x0003¦)1M\x000f¦"1.\x0006\x001a+éóT³1kÓJéJJ×Air\x0000Ó\x0006Ôæ8^¦££H\x001b1tf©§»ÓfL¦ÿ\x0019sì\x0002ÔY\x001d ÞsËË\x0019®AøÌá\x0018q\x001d³VÎê\x0008ñ3d\x0005ÕJ0#DúYÃì°ÑÖVÎê\x000cñCd%¤·\x0013§\x0002ùÉÄIñ\x0006\x0015Ç¥)Å9$h\x0002èYP\x001b4\\x001dHôçÇC6*HÖ\x0008jªã\x000eÿØ±C5õZ2g]1ÆbÄ´øèË\±\x0002cÅØ6ûÕÝ#¼ÌÏQQb9^*&\x0018ëÊüx<\x0015¯¸õÕÉ%¼Ëï\x0011S2»ÉY3$g/\x001eÿñß\x001fïn¿Ì©"`.â\x0002}eù$#&]]\\x001e\x001f\x001cß\í¹ØÝä¬\x0019³MRÒË&âO|à¦,á¢y³!¥1%$ücÇbj\x001aG\x000c\x0013"ÑÁ;MÊiFL¾\x001aÍç´Õ'ìà\x0014Y\x001c%ìO*\x0018Ð<¿ÀONÒÁiµÛ½Í:ÚWÛ»û§?À+Ç¸S(\x001cq tn5<_ÉÄäTÃ«ÍÉÙu|äxR¢ÒÑÖ\x0014&\x0019Ï\x0000NEpbªL¤Q²\x0011ÒC<D¦·7W¥\x0002CµÆJªRuPÊ<MØ<ñ7¬/UnÊQÙiJLÓóÁõ!­¥ ²+\x0015ªÜ¨Þ\#¤f%¤f=6÷múÜj`²\x0016p0JSïÂ-Õ\x0019×=\x001cÌ9Ö¾ú\x001c\x001fNË9YËßÄY ÝuÜ¡BNx¾FÎl2²ÑvòÜt~é2HÞçÃn0ß!ra¼Ì´Í!5fw¡Óõ~¼ý|w\x000f\x0001ÝÅÃóã_ïæ\x000c\x0001±\x0008áT¡¿ôÆÓÌE5z;úöøÝÉ\x0019Du\x0017ç7º9Ù\x0013'qµZ
P6=<ÿ|{ÿ4\x0003Õ¨|´%oä\x0015=c;H0O÷Åß¼?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÿú0¢Z"ª\x0001DG\x00028\x0002Û©}+(s¿c g?¢^"ê~ÄÈ\x0002i\x0015IkÐ*ÊjaÇë<£Y2~ÆP4G\x0004Øwj\x0011VÑ5â\x0004ývh»\x0011\x0008\x0014¶y)4
mB\x0001\x0005G±)¥ïgtKF×Ï¢Vy\x0015á:\x0011	ÑÑ[J®ÏEôKD?H½­Rñ0C\x0014y O\x001dZÏØÏ\x0018¡\x0011ßNR±²(÷N"\x000frêø§»ä\x0000û\x0018ã1\x000e¬£Ë\x0003	¼´f Á2RF]¡Üÿ,âB5JmC»Nu¤|ºX¥Î"×q\x0005ë(k\x001fÓïd\x0002*¶äîV	Â²Ì¡´;µXû +/#\x0007ÜL$éVÒIîZ\x000fe%w©ÜöAV~Fö;\x001aÞµçaOò¹£q¼'ç~ÈÊÑÈ~O\x0013¤¢÷2\x0017á^¦¨ÿ:ËTSÓOXù\x00199àh´#ëã±òÎ\x0015\x0019EË¨~ÈÊÑÈ\x0001O#¹ÏÈÃ?î\x0011K\x0007ö48Jk±ò4rÄÕ¤â«´«\x0003Á\x001dR-	üô~ÈÊÕÈ\x0001__;\x001brÓ÷\x0002\x001f^IÓ¨£ôCV¾F\x000e8\x001ba©!Ü(\x001f\x0005:4ÿS)1É¨*g£úM@]Â\x001c	¸{Ó \x0001VÂØ§)ïg¬|\x001að5QÐk#|lÇòÈÎJÃ\x001fÛNqUßhú}MÀl/ù\x001aT$Á}ËöÇµ\x000fý¯Qý¾&\x001aîäðX©LZa¾\x0016¾)mêg¬\\x001ap5ÁbÅ";mþÚJjÁiÏºªò6ªßÛDgIU\x0008/°4§ÀrñjFô#V¾Fõû\x001a\x001dó2úÀªóÎ\x0015\x001dæc\x001fUù\x001aÕïkàL°ðI±0­£çCãÝN½ö>ÈÊ×¨~_\x0013ÄåË'Û\x00111C]ß>=ôCV¾Fõû\x001a¬v\x0014Y8ÿ(¿=h\x001fHÞZáN2êÊ×è~_\x0013Á\x001fÒ%\x0016¶7_´\x001dO¬R\x001e®g!+g£»\x0015ÂÐ\x0013(8\x001bAÏaÚGËé3=ïµuålt¿³V\x0002|írûòZò×¶M7k?d@ëv6\x0016\x0002(\x000e$,¢A\x0018múhëÊ×è~_=&"4\x0013ñþíO	ÈÍ
Ç¦ò5ºÛ×XÜíOê¼Mëh8®Ø9©¥\x000f±ò5ºÛ× ®,gÐ¤§·Y8'Í¸¿ÂêÊ×èn_cs$açÐXÒÁ\x000e^¹õ\x00024]ù\x001aÝíkàÌH´ù¨Ø!\x0006Q\ÍüµFW®Fw»\x001a+e¸t®óµ¦e`¾|úÎ`*_cº}
ìH\x001e¶¤ ¯-ÊJÊ¤ú +_cú}\x0014æI\x0003¤a\x000bÉ3OàÊ×n_cÁ\x0011Py"\x001b\x001e«±7ÏÍüBV®Æô»\x001a©Ìælsº¬µBàiÈú±¦ÛÙXQFö¢©áE°Tç	\x0011yÓÕ\x000fYYr3`É±!4¯MEðº¸\x0015¶de%Í\x000bvÙ!7lè(8i\x0001Ë;\x001dZØÊ\x0000Ù~\x0003$%ªFeDÅº\bã|zÜV'Ûöl)ùö\x001elèm\x000eUe
äø·«\x001f³áß¾ªª|úøå×ÿr`(zh¦\x0004+ÉMôÚ²ý1¶InÜ¼xþúì¯÷Ì\x0013eLµÄT#A PÆ4$÷©´Û`69\x0001L½ÄÔC«©©Á9ÁI©\x000cSêý¥+GS%¥\x0019ZLùHEZÌ¢·§\x001dÇjÆ6Aï\x0000¦]bÚ¡Å4Ò>mMMßÜR³\x0013nÍý¥Gcº%¦\x001bÜWSsU<lÍ¹¿ªêhJ¿¤ôi7ç»ðD9?MÀ6@\x0019a2r×\x000bË¢{Úrî)\x0000:\x001a3.1ã\x0010&\x000f§ON"ÚÄ²÷\x0008½\x001e¹yéN¶]\x000cq²à\x0015p²ªæa/
\x0002¸ýµ_GcV¶]\x000e\x0019wï¹´ÁCÌ.ø ó%Ü´ãT\x00068+³)ì¦w4{Á¡ü´'L®d1®QiïÇ4Ù4CvÓh\x000e×q\x001c ÏN:Ê{ZYÅôÕæôCÓZ\x001aËé°¦Îs/ë³$×Ï\x0019«åCË©%ª9Ôé§®
-HtFY5¿²öøã\x0000¨$Í&è9öPÆ*ªÄ'1·lÒQR¬Iì°|UäàÝÚ{Ô\x0014\x00055¾>íC.\x0013çä{\x0010î\x0001ÚTNó\x0006½O\x0005ëXP[¯¨\x001dZQ°íY\x0004\x0016@Kïºò\x001cvÚöá±\x001fÔÕ+êFV\x0014gäÖ"\x0017Pù>=·\x0016)\x001bî<\x00164Ô>Xz\x001f<Éa¹CÇ3§	|äÛÑ»ÝJT_\x001e\x001càt=R@\x0005Ó\x001c{*6¡n\x0005\x0013ªt\x0015!ã\x0003»\x001cýÒÄîxF?í:u\x001dè¡PÄyÍÏãxHOò\x001b\x001aÄuÓW\x000e­«¤õÈIr87h L¶\x0012¨\;ªª\x001f4T;T\x001dê¢"jcÊ/\x0008Ã+êä|~\x0001\x0007÷V #\x00108+4±\x001aakÝu¼¢a\x001b^vJä,CÝ'Ñ¶¡ÚK\x0017SÒ6åÒiV¸(ÙmZ;Jû[Þäµ\x0010u.\x000cþ\x001b;ñæêäâ×ÿx÷ææÃ?ï\x000eZ'\x001c­kØ9 ê%àò¹³6\x0006\x0018ÏOO.Î^^>>öçË#HÕT
ª@¦?J[n2ª¡ô"Àî|îïÕKX=\x0008T±,kL3¥Yqe×uKX7\x0006\x000b÷c*öH+{\x000e\x0013ä¬\x00006ìz\x0013îõKX?\x0008\x001b\x0002iGÌçª\x000füø®¬ì®çÂ~Ø¸°pÑ\x0017²ÀæpÅØ ìº°&\x00014\x0005bVEºøÁ>PTªk,\U2­ÃEY¶6\\x000b\x000c\x0002E\x0004ÕÚ:Svm\x0013\x0011ÑVö@\x000e\x001a\x0004¸ãQ\x001dP¦¥µÕÌªV1\x0007Â|d5¬2Òe í\Ïd}°=X\x0014é#­\x001dÝµ\x000eãk6µ2Z+CqbÍ¹1ÚÊÔÊQ[+\x0005=?%[\x0001X¹¨ÊÚî*\x0011ê§­l­\x001c5¶èÆÊ¦Udk\x0005+\x0010ØØ\·Æ`C\x0005\x001bÆ`
Ö,ÒÊj¼v§å\x0016"XÙu\x0019Y9\x00069ê\x0019¡{\x0017,­¢Ä?Ö4\x0016ëÕ\x001a¢UgPÁ\x0004V%XZ\x0004ãèÞk»ëý¹¶ò\x000cjÐ3À7Ç ×ÖJ¢5zÝm«ê°v0®5®q¹ðÿÊÂ®´
*'¦\x0006ñT\x0003Ö5ß\x0018á[
®ë®\x0007þ~ØÊ©A/\x0006ÿª:ÒÒzZZå}YÚuölåÅÔ \x00173ÎæNÒ¼´¼\x000fdYÙUlª|\x001aôaà\±\x0002.¯¬ )\x0015½W\Ø*\x000eWU.L
º0
ª¬lð\x000c[nb;\x001b\x0017úi+\x001f¦F}\x0018"Ò>\x0010æ
\x0019í7¦k\x000bª\x001atb°AiX\x000fr®\x000bG§lÖvm«+· GÝ\x000e`FÐ\x0011\x0013¾,m3v\x000c¶ò
zÐ+è¦ç óü\x0019S¼	64*&c°u²cÔ/hQ.\x000ch½²AÐ\Âkv<\x001fÑV¦VZÉcT`i-Õòâ[
\x001bÛÐäæÇh+c«\x0007­öÜ¾\x001fEïÐÜ\x0001\x0017Þh+k«G­­ %\x0008·E6\x0008ÚâNu~ÖÊÖêA[\x000bX¼k\x0005fÉÖJ\x0016Ôks´c°©Õ¦\x0016íAäÕ4¯\x0006\x000cgØvÅ\x0010­©î\x000bfð¾ m¤\x0012±ÚÇ2¬(é6Y?\x0006[ù\x00053è\x0017tT\x0014zàPâ*Á\x001a\x0013­_'ëe*¿`Fý\x00023Ùv	Xãü \x0003Öù5\x0003ýÆX+·`\x0006Ý\x000eÔÆ\x0003çË³ÃÕZs¦¶­r\x001a­®\x000bfðº ó\x0014¨Dã³UÜÏ\x0003ÿ\x0007¼Ù\x0018måÃÌ \x000fCÛeh\x001f8\x001ad»Ø+fÑ\x0018måÃÌ¨\x000fSÓ\x0007"\x000f^2;UëØÊAÿ¥­çd"\x001c\x0002*t\x0004Ë%9îÚ©Ó\x000f[903êÀ°\x0013,\x0017&\x000fhËZÁfVÚU6­|\x001dõ	¥*
ÉÍÙp\x000f|Àv÷yõÓVNÁ:\x0005\x0008i9ìRÞñ9ósr§úT?må\x0015ì¨W(Ò \x0011[þ(3£tq¸íÌ1ÚÊ/ØQ¿ ,
õµå\x00160X[Î&ÚV¢q¶r\x000cvÐ1(ìk S×\x0005r¹cZ\x0013wöYõÓVÁ:\x0006XÐH´Ø0M´¶¼åÊu^Ålå\x0018ì cÀµ¥÷QìOe\x000b¦XFÖìn´ë§­\x001du\x000e²\n¤æ´²2\x001b\x0003¶N\x0008n+ç`\x0007
u¸c0üÐ¤\x0004ÕÂ£xÔ:\x0006¬ºÞØÑë
X-Ë,àÝ!¯-?=[±Î\x0003©«\x001bu\x000e°WI×\x001e%<\x0014Ñr\x000f+lÛ]ý´spÎAùH£7üÒ¤xº1~0ÜU¾Á
ú\x0006\x0005ëixi
g\x0010âW<ÓVÌÑV¾Áú\x0006\x001fxlZôTüRnÚ¡¢c´uÏ¨µu\\x0014"\\x001esO¡/dÆ6\x0003óÆh+\x0003æF
'M$
\x00056Z¶_¶Q\x0018\x001f­ì\x001b´_*pÕ'
\x0017p\x0011\x0012Öí¬è¦õU(î\x0007Cñ4CÑÚê\í
K»Ù\x0007z\x0015à+cë\x0007­
¢ÀÂU×P HÝ\x0019¶\x0019Â3F[\x0019[?ll%OlÆQ«)\x000e\x0017`kkü*¸¯¬­\x001fµ¶8\x0005CÒF0FPËGX¶²¶~ÔÚºHO!êâÉd\x0019á`ô:\x0001¯"q?\x0018+Ïóh#Å´\x0011
¬që\x001c²Ê5øa×àYÜ?B+yi
G4ª\x0019.3F[\x000e\x0006â¸m\x0015ù\x0006\x001dQ8xËíuru¾rd~Ôá\x0014Ú¶(_îimIë¼úÊùQOö\x001fZÛPy²0êÉÀ#X¢\x0015åQWz¾îJ¡reaÔát\x0002reZÑ£îÂïêuEBåÉÂ¨'¥Íwó\x000017¿8I_îæ¢\x0019?4F[y²0ìÉÜ#:cÊånXÙ£QëähBåÇÂ¨\x001f³ç\x0018µå¬,¹E½[:¬¶òcaØýGV¶rcaÔ\x0019Oà!)\x001bFÚ2üeø TN,\x000c;1SâZ¬[fcÀa­lÚ¯`ce¹â¨å²Þ`a=©Ý1`\x001f¦£]%e\x001b+c\x0010GUÔ*\x0014\x000eE3ëtX§\x000e!V\x0007,\x001e0¸Ñ+/½4Hg\x000b¬Yå¢\x001b«]\x001bGw­	Å+xÁ¥>5çöë¼Äºýf41åZ\x001eã\x001e\x0011i9÷¥ýNÙ¾^Z¹Õ'FOáÌkyqy^Þ-»Û[·´Ñc¦-)Ð`K±¢4Õ]çÒ «&R»pðO
ïa%WÚjL:çF°)\x000e_§âÚnC+;\x000cmÀüZî#Sü,mt)\x000f^eÜFvr\x0018\x0019\x001f§#EæQò:«R,nÂNÁÞbñfÍÔ:\x000b.d,\x0019RS\x000bh¡×Éf¥Ç\x0017Ú)¿ì,³Ü\x0017ë
óÎ\x0001m\x0003\x000f=ÛÌðß:¾;\x000c9G°õ4ÌÖ¨Mç±X©b´Yh=¾Òu\x0001qÀ¯
×éák÷Æ8²u¬=\x0013!\x0000à>dëJ\x0007_§z4¨mh°F¡Ñô\x001dPÐ#"Ëo@¨:¸N\x0015Î643Ã;Z9Ò\x0002îöüðîJýZ§Ï@»fG»qèßº¸X¤¿,e;CAyzsóë¿\x0013ïÛ»Ï?Ý ôç\x000fï®?~ùp}shS+½ÏRBÍ
¾:É¶¹þôüü,q?¹¸|õêÅ9À¿zöõÙó×ÏÎÎ\x000fÓ«%½¥;ª£¡´ÞPm,l\x001fÍðM\x0012{\x000e^/áõ,|à¦*ø\x0004ÚÄâc^zÕ´\x0006ÏÑ%½¥GéÜ¼q,ÎY¡Ø/°«X(²&½]ÒÛIz\x0014l¡[-ü&\äe#
D4¢\çèÝÞMÓGK\x0017°\x0017>	G	÷MZy\x000eÞ/áý,¼áÉ\x0001.c8ã!Á[np\x0011­Û\x001c}XÒYz¯ùfÊ\x00086ã\x0002µÀéèâ9ú¸¤³Ö	j\x000bÎÊ\x0012Â\x0018¾°IßèÍNÑ/$ÿB\x001e¸9ÏqAÀH\x001d­å\´Mzg\x000e¿vµÓ¾\x0016ö\x000eÕã T\x0010Ý<Q<7Óë&ï7G_¹Z9íkCjüMç6\x0005gÙeûì6^9Z9ïi\x0015±¯\x0012^"\x001cÑLc¯Ü¬÷³\Í<\x0015u©@ì`§Z5Æ³\x0016Ö¢â\x0002\x0018Â\x0004Ãå}k[{Y9Z9ëiÁÞsfàÎG}mEÙ
ÄÉ«Æ	²rµrÚ×bò>',Ä\x000cÙ^:Ç/
Â4mysô³³ÞÊYKøØ÷øsÂÕ1¬\x001bç¨ÊÜ«YsïàjEA\k\x0005wXÒìº\x0001²ªoVÓæ\x001ev~Öù\x000f¨\x0001Â¹]\x0016	4B5\x000fìsøÉWÓ&ßòÌOÀWüleµ+øMRl\x000e¿²újÚêç\x0011è\x0019¿<\x0007ln¶¢\x001dþ:_Y}5oõE¹^¡\x0014?ÑK¶¦i­£¯¾6úVÓ(è` qqÀ7åä6å²søÕ
EÍ^QðJH)\x001dËÇVò¾	Í¨)t]\x0005øz6ÀwNÓA0>Ð8\x000cã<×§&æ5ñ+¯§-¾S\¾\x0018ü[2ùß\x001cS·ýøÉ×Ó&_Jê%Ûa 9ípTKJ\x0007õ¿ÖÀ×ÆÖLø*ùùäÛ\x000fï?Â¿Á/òøúêîöúýÕí¡\x001e\x0007yç}õ¢§£ÓæÁ\x0001ûlæ«o=}\x000eÿ\x0006¿Éã³ÓË³§§\x0017÷y¢_@-\x00015û\x000b f|îê\x000c*\x0004\x001cY~\x0001\x0016¬ÑÁí5£¿^þ\x0002zú\x000b@Ì ù\x0017ðT" ñù½7ÜÑ_À,\x00013ý\x000bxÇ5Ü
xò5k¨t\x0017\x001fKÖÞBvù\x000bØé_\x00000)¹¦"k¥k\x001c\x0014È¿ÀÞôÔè/à¿?Ä´ü\x0002¶_Ò\x0019öÚ\x0012lÆ&Ìòû%¿æÇÙ.Ù\x0005`g\x001b\x0019¡Å!Eká°ü\x0005Âü\x0007p4æ4h­)p/ 8Á)FøÙ_ .8û\x000b¸P\x001arð\x000cûü\x000b H\x0002½ÞÁ_`¡\x0018~LLàè¡\x0019>Aà\x0001©(L`e#*k?<íáþH\x0005:\x0003y¼¢Æ¹yùÃÚ^XV^XN»aï5
\x001a\x0001\x0013$HÄ\x0006ÐÅ\x0006­|\x0002dåå´\x001fvFòFÐ2`Æ?}\x0003OÅd\x001a»\x0000Wþ
*?,ç\x001d±,\x0017\x0001\x0014<ÉYO]dGÁ
í
EGÊ\x0011ËiOªõÔ ±?!{b\x001d\x001fô\x001bì½Êþ\x0006'ó®XD»\x0012fW\x0016é7PÍ<Ùß òÅrÚ\x0019[ðeÔ\x001c ç\x000cá¨áß`íhHVÎXÎ{c¡ùÅKÔú¾Õü
lS?û\x001bTÞXN»c|ôrt±-2»c¸ßoÐ\x00149Oþ\x0006ªrÇjÞ\x001d\x000bC5å\x0006þ.¿`h\x001cKA¿+¤ªòÇjÚ\x001f[\x001f¸\\x0000|\x0000HÔ*Ò\x0013Æ\x0006úb<ígÅø\x0006ºUµ|
Üê{¨òÈjÚ#ÛÜAÏq õw¾ÅV+`\x0016¿rÇjÚ\x001d;\x00138$Âª\x0007E\x0001E0å%¦Ñòý
*w¬æÝ1¸\x0002AÎ,X*øÑÆ3ÐÊ(Îþ\x0006;VÓîØÁU@ñk¦2_\x0008ê¨(RÇØT®Ïþ\x0006;VÓîØÑKªÎJEé\x0003k¥kÆFÏÒW®XM»b\x001cFïÅ`.óSª.¢`I²e]üÊ\x000f«ùk±¤Ý
&Ô*Æ\x001c»±FÖlò7Ð\x001fÖÓ~Ø	\x0016\x000fC=d\x000c®Óo ùEooµä(åõüµXùÍs¶AEê¼\x0002½Æ¯L_¹`=í1æÅ\x0017$Í¡täí\x0013ýÚË_ç¦ç]0¶\x0007Óþ×X\x0015\x0001öÁ~í\x000b¥®|°öÁ8¬KQàvLy--hn8\x0018Õf\x0006ÃìoPy0½ÂÒÑ©=+\x0014Ä¡44e%V?Á\x000bÐó.À¥¡\x0007ù\x0017HBÙÑ \x0019Ì\x000cí«\x0006\x001aü
LeCÍ¼
Õ£¨ÊI´v#i±¶\x001b6\x001d2óW\x0001Xx*(\x000b\x0000=Îkmø Ê½5ÿ£¿AýÆ´ÂAv4»\x001c®cæ\x0011%XÞ
nc{KÊz\x0001ìB¬Z«Q³o9ÇüîäÉ÷W_®àwøp}{\x0008»\x0008\x000f;¬ÛÎØþjEÓy\x000cçåÉ?¾>\x0005ôgg\x0017hÓÌ¬§wáb\x0001P\x001eÉj\x0005Knh%yÈ-\x000ed_7Ö¼q×iJÃe+PûVlJRÄkðÚz}íàúºQpX]E¡b=\x0013¥ÌÞ1ì}°\x001bÅ\x0004\x001bå\x0010¬\x0005ËLÏ¢6âM\S\x0003-SÁ.n\x0004¤\x0006y]Íë\x0006\x0017×\x0006*úu8s'æ­Ð$`¬vBú§\x000eÁ:I#Â\x001cÆµayÔ½«\x0018\x0006­«½?áFMÓ`À\x0019\x001a¬²Ë\x0017!~,÷gïÂ5\x001b
OÄÅ\x001fp=
ÿ'íPëîmÔsªD+s4DkëÅµ£\x001bàCNBÉ@E¯Ú\x001aö\x0012¢\x001dn7Äë6º1È?\x000eñF\x0017ù I\x001b©¾[{eóQ¨R¿\x0006oðÕnHM·#L¢\x0010^^_©UVD#I¸²	ßFp%î¯¥\x001dÃx1[h³ÝuÎZj !»kÃvæy78QñâÏ\x000fÔQH\x0011¾«ô<á\x000fçéO×ðvrþéîÃç?ÜþúïwÀõáíÉ×woo?}>´µg©L0p4°SûÒæ-T#>yúíÙóË³ó\x0017Ï^üáâìë³gOà×xrñâÕAü\x0010øø\x000e8õzt9W\x0004¶u`]RØá«âËÍS)âËôV:Å\x0013H)9h½NË/y\x0002iR\x000cZ?ÖüÓësÕ9»ãøZèÕ&·ì\x0017¢\x0019þÍÌÄeSü\x0001®TBä2ùt\x0017,ó»fæã\x001c½þfvý\x0003Dü.µQJ\x0003ðòBäìÔ\x0004¿\x0012\x0015?þ8Éï¹Õ\x0005Cª¼û|£Õû\x0014ý¦Þ*Ñ§«9zYê­PE ï~çJjÜÈ5wÿ"îÎüv?
ÊlBPLeÛ°yb©Øk\x001b\x001c§ðëÍ3m|PïJ»2txÍÝí£êí£¦·\x000fXüE¥Íe§7ü\x0004ø\x0014m|Ô´ñAÙrzÜEÁZÙ=ÊPÝ|Ûµ0ÃïªÐ\x0007\S/\x0016|òúóP5Ï3ü¡æ\x000fóü«\x00138h$ïUÖ±I\x0008NðkQñãü2r¯\x001a¬9)íiËêÜ\x001aeìÖä×ÕþÇ\x001fçø=l\x001aÊÇ*Y*¬\x000b´|lëÜføMe´µ?^1\x001f
í\x000f\x0015(EÉû_®\x001a¼i_óûiþ`9x8\x001fÖ\x001aµoE;§øc½âôþÁËK>¿Ò8NÖY\x001a\x001f¨½n\x0004RgðMí¾Ì´ûò\x0004Ë¯r\x0012v¢\x000beÈüÀlMóoT¨ùgcÿT®\x0003H0?¼üco<Süº^=½þ^pì/Á\x0013XÇMS÷O#î8Åï«í?Îï\x001f3F=MjVP·¿h³fðC½üa~ûK~¤2¤D¨­tõÂ¢ù5ñU¯fñ­âÑd(JH\x0016Ç-$üvhÒ\x0014~m;Í¼í´«\x0004Ü\x0005µ<JNü¸\x001dÝ"\x0013ü¶}ì
±ç^k\x0001a4%\x001el¹¸»vüÏ\x0014¿ªùÕ4¿4\x0018Jhû\x0014zZÍË¯Û^©\x0019üÚvÚyÛ	ß9\x001a#\x0008¡\x000f¸\x001dU3üuÞÊNç­¼LñBâ©:Z,Èx:Õ·z{õîêóÛ½üõÕËN_½°S-KÏÂþ\x00017ÌÏ=\x001c:;½îñuõú»éõxÙ»
?Î»5nÒýSü¾æ÷³ü.¯Oü8P\x001e\x00075·ª9ÝL(ã5ÿ´ùW<½\x0003.Y³£H°£«z/[¿ZØég\x000b\x000fk.5á+®11{¼lÛ©9_;_;ï| ÇZ\x001f£ñDÚ\x001e¶Þ­yx]7tóyC!(vð\x0011¯Àtm§kK2B+Ò×Y\x00077uÀ:¶\x000coÒ±$@é5ãNW'
ÝtÒÐ;áÍ"fVteÙ!´1Ãn«¨\x0001µº|}ÇVÓl¶Îªkoëµ·Ók/XÛ
øSw]îeá+5~M¯å\½þn~ý-Ö±$~° N±×*üÍ8å)þÚk¹i¯û'+aúÊn÷\x000fóï\x0010òá¯¯¼núÊë§Ç\x0001n:Åü«¾ºÚíºi·ûÇeÛ\x0019ä-\x0012 þ¶Èhß×ËO;.T¨ ó\x001b°\x0017z%k\x0008[ÑêüÌð×\x0019C?1D©uÁëï\x001fÑö\x0017ÜiÅª	+_çËýt¾<åí\x001frùW.\x0000ä®p\x0013ÅA³7u©¾tá°3Ú>Fq'\x000b\x000e©'~×¶2Nðzûùí\x0014Ù|âýÌÿ&î4;*øgøur\x000bz6åæ fÈ5x>HÉ.Ø6ti4ºíFáwõú»éõÍ'lFüÛÄ¯xÿë¶Æm?Vå\x000eøã,¿¦©S\x001ehá¹\x0015n]\x0018ÿ¬Ê\x001fjþéK»0¤°ä½b@lä²Ìß\x0014LÏðÇ:é\x0016§n6r
ªÇ¾|RÕP1ðúË¶\x0015p_úÚ~ü\x0005L bI\x0003D\x0002u/hîÇW«\x0016lH)ª\x000f~ý\x0005x\x0012G¡XÍ½"$Ô\x0008¿Àªüõ]úy_Ðð§ô6ú\x0002G\x000f2´ÚD3ðzkñç·?Ø\x001cÊY¡`¦§_ òôkæÜ¤´²þ\x0005ìlüJàY¥Ñ`X^\x000c¾\x0000ÏÒ¬\x0019¿Ié·¾ÀtÁ Sñ/ P¥:ý\x0002Ï¯\3þ\x0001^µÅ?\x001b@\x0018\x001f\x001f\x0011>uñÊÒ¾(W
\x001eäV±¯v3à\x001fv\x0012_\x001eeynõYóü*·õ\x000bLg\x001fP;@Øü\x000b'¦Ý\x0003n\x000cðnÅ7\x0017©¶¶¿ßþX/FûGrU\x0011\x0003}\x0001\x0011Ö|´\x0003k¿õ\x000bLç\x001ft´Ô\x0007îuô4ÞM\x000bMc\4þ§Wü\x0005ôÖ\x0016ÒÓ[\x0008\x0015drþ
¢\x0006nÕ\x0014JPþ\x0004\x001fªVåW[ü³\x0006\x0008kÌuvaX±\x001aø\x0017à\x001b\x0000üw®\x0019ÁmUÉù1­\x000c_á±	<·»¨h¨M\x0007~¾Ï\x0003gØÔ\x0019èôóä/à%MWð°]øáZP\x0006\x0014bé53@Àk¶øÍ,¿ö4\x000cÚ+ãh\x0007©h©fXÅ\x001dsQ&~\x0001·\x0015B»é\x0010ÚHÅ\x0018©%ß\x0001\x0004OÂRØ*¾¦\x0017pâ»«Æ]Íz²À\x000f`IÒÄ²'sÅ­Yýàt¬\x0007|\x0004ü\x0015\x0011ÔxRÑÜ¸#9\x001c²jÕ»°b9ñSRû\x0008þÑd\x0007Iàa)(ïFÂ p;.êb­nø\PôÝf7½u
\x001e$Ñ=pµÐ\\x0007'\«p5WJPo&,&ÜL\x0010NB1°tµ)èN¬ÙE7±ïÞ6w³·óWcz\x001b0yà\x0011ÜÌ8°¦Y?y³ùî]s·y7i+Ñ)&Ú)¼¶\R#u3B{Ö(½Ù6J'\x0001
º}T¥ê\x001cJ²ÑûX33yÊ(Ø\x0018%\x0013W0J.Pm\x001f\x0002 WJWjËÚA0gáMs\x0016&¿\x0003&*ÊY0æ¬ÔUËê\x0019Ö\á7ý\x001d°ÈkD±\x001d\x0005dù¹Õ©UûóÐ²¾Ù¶¬_\x0002ëä¸Î\x000f"
®Vñ¡XÖ5Ý4^\x0010¶¢%¼2Lz\x0007¼3ä6C¸3\x0008ßÃ;ç;ÃªU\x0007ðßQ\x0006lôý\x000cCêôáá\x001e\ò\x0014Vý\x0005\x0012ß]/\x0001l5¹}¹we<	ö:Pá
[$\x0015Ö½77Á^ºûO\x001fh\x001d\x0015_~4_&\x0017§ø\x0001G¬ÛpåìÖNÂ
¨Éä¼(% Ö\x0016ÍX*/SÌª¿ÂÕö¯0y$}ô5#,Å;¦UM\x001e¿m\x001f¿Í\x0016`z\x001e¸%) \x001c¯úUÃ\x000cü\x0005¾lÿ\x0002_f]àÖOxú\x0006<\x0017\x0018~5[?SQû\x00052&÷\x0015|ÇÜ6É²JÏ5ìR·\x001a&î­H	îÉã\x000cëÏ7\x001f\x001c\x0017Iðü$+W½¦­ôn{+MÞ\x001b¼\x00043D;Ir')ÃÛ¼oäïf7Û¿Á¬M\x0005·\x0010¨\x000f\x001dËJ©,S\x0017}S¹n\x001f±n®
Ø\x000b=\x001f®F¾E\x0007\x0016\x0014e8ÏýqÕ¨\x001b]ÃÛm×0yN\x0005¼Ûf\â¶\x0008sdÖÝLï·7Óû\x0015"nú\x0008IÚ)7¦Xîé^ó4$tÕØ¤éì¤-¯´^bÀ³õª\x000fÆ¶Ñ\x001eæéç£=%Kª\x001b_«l¾7h\x001a`¢bXµZ\x0016¯omÅëÛ¬mU?EÄÙb|}ãzÙ¸ªº3Û)\x00193\x0001õ\x0006
û³Þ¹IzÓq°jÍ&^Þª\x0003·Ùì¤w$5\x0018\x0014ª$z	à¡\rÍªd®¶Òì¯óo6VãU[RJ¨:¿®YzÛ¥Iß`dÄhÙ,\x0015µ\x0006áx¸4jÕ4åOî©2ÚJùÒ\x0003â+ÃnåíOhÞn[¥É/\x0001\ÿ¢ÅlxÆÃ!0ë\x001e·Û\x0007b6ÐJQá@lú/æX·Âl¿Àù\x00178-J\x000f£E=©hÚ[e×ÙH:/>£RçFLýîäéÕíõûq°¢Ó\x0008kþ(ÑZzªIhÑë}c\x001c.O^½>Ì§|ª/Ð\x0000|C&óbe\x000c\x0005°-Nî\x0004ÔK@Ý
¨ñû&@í\x0005	FXéYª2HµG?ÿh@³\x00044#_8? ÅTæ\x0011é\x0013Swñmub']òÙn>¸`\x0017YWÞ*CS\x0011á<í?p4[ò¹n>\x0003ÇBeÀ\Û\x000f_jãMØÑÓIçt¾.\x001aPU\x0014\x000f`ùø\x0000\x0007Óæ;\x0001Ã\x00120ô/~diû9AgÞ~²\x000f1\x000b\x0018±\x001f0Rê\x0016çöÑ»\x001eX\x0018AsÂö>ÀÅ<ã4Ñ ÿ\x001bGêïÄ,L®¥ol©¿
\x0005\x001f'7¡¬H¿\x0017ùí×°r#²ÛH!¨F2bÁj %tÌ·obãÑ|ýV\x001a¢dæ\x0003mÈ°\x0011ÜQ¿v$¢vÃð\x0007_m
\x001e¿¹º}{òøÓÝOW\x0007\x0008-.øÖÛ¬0|½hç%åÀæÓ''_\~{z\x0004§Yr\x0011N¸\x000cJÂ\x0014Ôe)S­Æ{bà.H·t#8îÂ\x001aíhø\x0014ÜûHf
[r÷D=²úèrä«\x0007\x0014ã#P\x0019èRa¢s\x000cê÷ivV\x000b*GV\x0014â,ÔyFP\x0019¸\x0012\x000e\x000eI/\x0019g÷Ý~º@C\x0005\x001a\x0006@½ÓÖJ)*\x000cû'¥^ÛÛ°Ó\x0003ºéSHç]FEY.Ø­°GU\x0006åT\x001c\x001e¾\x0006hµ¢jdEaÅh\x0010`ù¹	¥XøÄï-Rë¡ÔÕrê¡åtý¢2Ï|5ÞÑèipQûè}ß}í¤/ÿn\x0015gêJúô\x0006\x001dgþôåËï«°éD½ÚB½z°»të Ö·#¬æ\x0011íS0«ù\x0019\x0005£7¶¥f_£U'ê-Ô7\x000foYÃvT\x0012RTrqcàNÜÞ}þüéæ\x0000#Î\x000c¤\x0007Â\x0008\x0001hVZ5ÊðÍÖ4'ÿâ\x0012Ç¾<¹¸|õêÅùa<½ÄÓ½xÂñ|Òèù	\x0016\x0002x>E¦¹ØöâÙ%í^=­B	Ï¹gdÁkd{ùÜÏuòáã¡åsù1J±COoÙs|~Éç»×O³Ì~â£Y<í9ðÍ®_Xòn>Ë\x0013º£å1bÀG³ik\x0018:ù6÷ZäÃ{mÿñ%>½8½¼ÿlópÐË'+>ÙË§\x000e{´¡\x001c\x0010gÊ\x00026½ùÝö\x000fÅªh\x0005áF&i¸ÛØ¿í·¯²²Û\x0000Â\x00022\x001f¦~Ï\x0013Üôõõ\x0002
Ð\x000c\x0000Ò;Ü±qk\x0006,GØ4·Å^ÀÊDËn\x001b­Ó¾Ë[PQe$6Êó\x000elÄ{ù*\x0013-{m´6ºØh\x001dË\x0002\x0006\x0002Ý\x000bÛb/`e£e·Æì<í@I£P°E×¯\x0019#Õ\x0017+¼ØGãÜàóF¾³*¯\x000b_£¹ØÉ§*\x0013­ºM´uü@\x001dµ¤B\x0007\x0008	Ë\x0006ÔMÎ§\x0017°²ÑªÛFkN§\x0010P\x0012 \x0017e\x00036éï^À:Dí¶ÑÎ²¢lT%FÕËMsçëÅ«L´ê6Ñpj5¯#í\x0019\x0014¢)ë7»|VÝ\x0016Ú)\x0006å\x000b¹B\x001fVÆI\x001aØ³|VÝ\x0006\x001a04»`]Ö/(þ¼¦©àè\x0005¬,´ê¶ÐAd:ÁC@äøøéÏ[¨ª;FÍsþ¼c|-8@PMg/_eU·}ÆaÁôyÁ\x0015çQ`)\x0015Ê§·Q6í\x0004ÔÖÝ\x0006Úo\x001c°RÔ÷n´\x000c\x001c£ªæÞ\x000bX\x0019hÝm  q»!iÃò\x0017V\x000cØ(#ôòUöYwÛg\x001fyØUD\x001d7ËG¤X\x00181yuDè¶Ðà@Â¶\x0007Ö"â'#,]YhÝm¡#×?	ÔÜi´±lcdSZÛ\x000bXhÝm¢±*cãB²<\x001c\x001c\x0011\x0013\x000f¼§ë*FÕÝ1*á\\x0010\x001bP¾×ð\x0019ìCTÓ·Ò\x000bXYiÝk¥¬\x000fíA¡Ê'¶\c\x0000ÿûÉ0ZWfZwi\x001f\x0017Æ\x0007ò@Ø²V³a©Ì´é6ÓXGaû×\lúzz\x0001+3mºÍtÐÔü\x0005+(8á"¼VÐTfÚté\x0018JªW¸b\x0006­(Ìl¤`*3mºÍtT_\x0010b©\\x0005|FdÓõÔ\x000bXAÓk\x0006QÑD: `\x0005K,(í,`\x0015©ÞHÕH\x0016a\x000c!X\x000bç®ò'¡rß}I\x0013Ëá4þIgLhp®RÞúyRõ_ÙAµ©:/ÈààtîHn\x0000«É#Þ¤¹`tlô
úWs\x0012V³Òx\x0012oÍW\x0014J\x0004[¾º\x001d6ÝÂ}W\x0015Èâ\x0004\x0019ÆÓwn~üþúäñÕÝ\x000f7×÷3`ù\x000eï\x0015ÜIà×IÅ\x001d+²éÖGÆÓ¯_¿üãÙÉãÓËoÎÏ\x000esª%§\x001aátdÔ*:ÜoS)v\x001d ^L½ÄÔCË\x0019ð=1qBpëi¼µ¤8,ÐÚõÉ{9ÍÓ\x000c-'Ä:¡hrÑX\x000b§(¹	·À¦-}Ó.9í\x0010§#ùK86XU1Yy«\x001d5?BénÒÐTXøê¦\x001c"Ñ°´qWÑËé~3H\x001e¦¡á>\x0013I¬ÆÝ\x0019éÙ#aÉ\x0019F8}¤¢`Ñ\x0004g\x0004\x001b%g×8íqÉ\x0019G8£Ãw,îèÊiwTé¦bÛþ:À)k#?bå£T474é©\x000bÜÈÊß+VV^y|¤1SZ¥°\x0018A=_&`Ew¥|z9+3/Gì<j=e]X¼áR¡çÜ-J¡­pàeeæåÇ×qRÿÖ\x001bÙ?ox¤·+xYÙy9bè±Ì@Ð÷{z«Ë®pâeeéå©Ç\x0005%A~å
ëÑz\x001dyµ^ÐÊÔË\x0011[\x001f] ä$|mnEÖÞ	.va#_Ùz9bì£u\x0008ÔS\x0007\x0000nQöñr
c/+c/G¬=x\x001d\x001e\x0005fç&uoy|njW\x0006]¼jb¨,VTQÚ\x0012KEyR¥'L¸3­°ªrJjÈ)¡­wE$Òr\x0016ñ¿y­^Ìúâ1äåÕ¾\x0008DxE¥n\x0010î,é\x0005­|\x001aòI¨\x0013,Ëþ¤sä\x000c\x001føÐ\x0008BpV>I
ù$8å.sJ+9ºóÒðê¦åg\x0004´òIjÈ'yEã¾½eöw¶h¯á<UåÔSe4ªTm½\x000b\x0005åÎ²^ÐÊ)©1§$h®p\x0005?½¼¢jgÑJ/håÔÐ
$hj
ñR\x0018ÖTIEÌiEý\x001aq¨ª|\x001aóIªhËÀÂf`DàÈÎGÜNP]ù$=â0á`òâôm
D¤\x0014­ò­ÌÎ\x0008håôW-J\x0003\x0000'.ySÔÊÍÎÂ¾^Ð:Ó4fî5ÚÎ\x0004
F£y§¬úÎ\x0012É^ÐÊê13\x0004®8×T8#§ÖHéÊ8é1ãä\x001e1¦|d,ß@TÉ®à?uuæõØ\x0017Ô´
á]\x0019ÉémZåÈê$±øN³m°WI³#\x001aPàÔèFV'É\x000c¤È]ð^:Ã\x0003\x0016|à\x001d\x001aÌÎWô^Ðê$¡\x0014#ÏÓX{B¶)*öófÄTGÉ\x000c\x001c%\x000bÿI\x001e»'­ ñY\x001c Ì\x0011Þ\x001a!³©\x00198Jÿ?uï¶dWÛy¿J>A\x0006	ð\x0018u¥V¥«Õ¡C9%u}ãÈRå¸\x0015¡<:8Æ¾òkøî»¾ÿÞ ßÄO2Ä"À½¸¹wæ&Öê\x001eÙ\x0011\x000e+Óuø\x0015\x0017	 ð/÷\x0003Q¦¿(\x0013ðl«òw\x000c£\x0015¾;H^uèÚÁ\x0007©\F°]<[À|²`\x0016´OÖ«ö'5¢sdoü\x000fmAÓ6×\x0019ÓÑW¹y×vþ{zûrõôþóû/ïï??¢cãM\x0002yæ´.òöÌm$^Ä±¶v¤ß¼¾zzsûìõ³Û\x0007Ôk\x0004\x0014Ö  \x0002¥ñÌi¯M=ïÙ	'\x0012ÿ\x001aN\s¢ÓZÉá«\x0006¶k\x000e¢r\x001cí8%]CêÖ¤NE3áÉO\x0001\x0004tÔÅÖú5¨WºÈ\x0001s²$CV\x001f¹\x0011Ö\x0012Fu#
kÒ "%i4&-ñHÍÙ;C¾¨jsåqD¦4®I£4´j4kÅ>9\x0003\pXHÇ
iZ&
)\x001cÔóLª§w&Ê
aTÏÓæ5iV­iö¬\x000cÍºç}\x001a¬iÚe®úñÈê\x001bÕ¢ÚÀóÉÀÅ&Ë,¹àÇ¾_
jï T\x001e
ìêû[\x001e¢PP¹8»|ÿ]\x000eìÊ\cµ¨
*lD¦Å\x0006xÎ»6"«¬sJa\x0001Ó\x0014£Î÷Ó\x0010£²\x0004?¸{·Tä|¸»úùîýÿ~lYcj=?Ö°Î³¹*\x000e=\x0003??òt)Éyþäêç'ÏþÇã°F\x0004\x0005¢ãA]KmS­t)­\x001euPþGÄ5"Î#®
*ËÇ\x0006î<3­JÌ\x000euåónÍè\x0014JQë2\x0002ßæË2Ê§>Q#6Ïè×~1V¶h¬èÏ\x0000\x001c
?S>Ï\x0018ÖA±N¦%\x0004É]ÆµZ»¸ýÈ¤5cR0f>\x000bdëä³|£\x0019¢ÇÆGq¬×¦²\x001emúÅ,j>5}hg¨¹Q\x0014W±Ç¤IE[wZùëèxQ¥÷¡,ª~s\x0010®r!JùâÏÅÝ|®U¾ýrÿùëû\x000f£\x0006\x0003¿&ëéY¯	cÅb
?\x0017s[«-_½ýÝÍíg/\x001f\x000750è«2èÒÉ6¾\x0000[6 Ñ|^P\x0011ã\x0018õÄwCYbËÔX´")eº\x0017±_\x0013{51MÛaq/Ê>²l_HødM¸8¯³8z\x0011wKÒ
U\x0002Aiwx²P\x0003lûs§?x4;!1²§ÒÂ\x0005\x0019È¯ânkl»gÿ;\x001c=Û\x001d=«?{4lÍ\x001bM³¯È ¦eOfSUÈ®Cvÿ\x001dV¹3\x0017Vo/Hµ!ÓLÇe½ôëÆ8ø;5rèÃU\x001drÔ"[¸¤"Se/\x001b(7\x0007ñ¾\x0017qg­Ú*SÆ=³³5,ràÑp&ÆE?\x000cNÖ"CgAmIÏ²ªs@¯ÈÒ\x0017óÉ÷\x0002\x0015rgã@mãh®v-«ÌäMÓKbÎ%8ùr0Elá(P~ñÃ¡ðÃýÇÞü¯o\x0004þHd&² p	â
aWí3ÙÄÏi'=¿ºùû·ü8%¬)AAI\x0012c/nÅkx\x0016(\x0002Û.nx¦«p\x0012×¨YKÊs	¥ý.-­\x000ciÏtHM@º5¤S}p_-²9ËRrr3¤_Cz
$\x0018yÓ¢ï-T2o ·ïÊ°¦\x000cª¥\x0014Q ZIé/\uî
/oóq
\x0019UK¢ë@u`O¼ïNöÄÍQ¦5eR\x001d\x001d»¦L¼+Q4æ0\x0013'¸òu_¥Qazi\x001eN	Dl\x0013H¿M\x0016óLûõ\x0004fg-­Æ\Òñ\x0001Iw&vs8>çZJ'(;CdU¨ìLäo\x001eÓjg
ä¹>ç	ÊÎ\x0012Y)Ê"ëAe³Yç\x001em\x0017 ì,U"H×ìy"\x001côñD\x0015\x0000Ó9y·	ÊÎ\x0014Y-òòÅIW=s\x001aÎÇ&#4¼\x0007Ìcv¶Èª\x0011bË\x0016Fl~<Äý\x0016\x0013:[\x0004*[©EnÑT\x0005ÕO
¦ÝÙÅ 
0IºQ\x0004+ 	¿5Ý28'^;AÙÇ*¢õ^\x0016+)èûIÛ]9tñ%¨\x0002LgÛ\x001b\x000b¹uùäIXO§\x0001ç0;Ã\x000e:Ã.·Ì²¹eÛe8rYÍ°ÙCgÙAeÙ]Z+^ñ7O±	þ\x00134 ì,;¨-»\x001c©íLÛÂõs9\x0013É\x0004É\x0004®ê+×Hä[zÁ\x000cíîs²Ao
\x0013;:é¤\x000e¤Kä²åÑ9'e<ÙY#ÔY£Ø\x0014¿
¶7À\x0008íÝ<n6GØsTsg¢\x0005R0Åj:{²w\x000e³;A¨:Aâ3ò@nP.9+:5Ù\x001d!T\x001d!o©0.°\x0000)wª¿Ø£
aG9}¾¨üb=ðþËÕ»ßî>¿¬6\x0006]¸v5}àr8\x0008õò'7n\x001cGÛJcÞ<yñäöÙC\x0012\x0012Ö ¡4MmÖÃAÞÊ\x000b	CSkLT`\x0016+ÄÃ})o,¶\x0011ãPw¢@tkD§AÌ-d÷\x001eEo\x000c=<èB*0ý\x001aÓ«>xÓßöÖQõVÍj±4~0
Ê°¦\x000cªÅ4<#³Üm]\x000bäiß¤¡9\A\x0019×Q»+we8ÚaH\x000f*\x0010ó\x001a1«\x00162PX]HO"\x001bõ|\x001fVò|áó£Å8\x001cÕgEèéî{ÿqy\x0008øÓÝ/ß/
e\x000f·	k¿¸ñà\x000fâQÅ>ó#8ÿccùô÷7/½\\x001e\x0001~ÿäw·Ïnn\x001fåÄ°æ$\x000f9\x000fJ³Ã \x0016sé¸ATJ	zÚ·ú\x000eÔ«@áilÁÛÅ\x0011Um"ik0dc\x0014 Ñ®AI\x0007a\x001aä7k/\x000e	\x0012ÑÜíÚrÛVtÔcW¦\x000e4©@)Ó+¨Ë2=DÑÎ\x00023h\x0000}w÷ëÝ¯ÏÚ*g ñ\x0017£úöu©Ê\x001a.xÆ\E\x000côñ7/©]5¶-¤^³¦4\x000f+©õ<p¸WÐR¼4ô¤ªó-·¶\x0005\x0017|SNCßÖtÈ{(HC¿¦A·¦Èú÷ô'#ïÓ`Û\x000e·u
iìI£òë{ùúQF£\x0007é!(¤¨4æOU'
4p8B:¶îðõSçGt¹\x0014*\x0006K4!@zEí¨õ¦!í÷iÒìSR¥c\x000fåÊFH"E\x0018\x0004tvTÙýÕ@¾jùï4¦_ÞÜ\x0016ÓoÅô£m¦\x0017Ô_PQ Ò(Îúý±¬"[#;Õ\x000fò\x00003¬åÓßË/¤âö/þíß®n?}{ô\x0002\x001fR\x001blJõÐ<6²zªþ8õb}{óâ\x001f®n_½}èî.t°¦yº E)±ü±¶_\x0016<[#\x0012oóI\x0019@\\x0003â4`°¬HU/K\x0004"T\x0002r*ý1ÃçÖ|n~\x0001½\x0014"Eú¼¼"F]n[¿°_\x0003úi@'·ËL\x001d\x0018¾>\x0002ï.ùdçÿ\x000c`X\x0003ù\x0015Lµ^¤9é î@Pð\x0014\x0014oäk¾8Í\x0007Òè3Í\¬;0\x0004Ã\x000bæ¤ØØ\x000c`Z\x0003&Õ\x0019®5	AÒ×Ñ±Å.w·¡7d\x00160¯\x0001ó4 	Ü?)#,+È\x0015PThx*!<Áw¨áXL´\x0006Ì»½rò­\x00151h¬\x0007¿u\x000fÚÞÌ{rtkÉ²PÓ/\x0001y\x0017­áÆol;Gbç=Éz
\x0013ÙD^C±3þd	Ù\x000caçIì¼+ùë¯açKì¼3É2m'*t½x5Lb\x000bÃÖÒj;o«©\x0018´dÊ\x000eq\x001f|tY\x000eÊI9\x0019ÀÎ\x0014Úy[Hq ïÂ$âä.z.y¡^¿ñ\x0002t¶\x0006\x0014¶¦\x0001S×f#<D4f£?>$>É>¦¦Ë@MP:©mòxº¶i\x0006°;&0}LþzåßûOô¤¼\x000b±?Ð2ûé§\x000f÷_¿Þ_ýøþ7*úþôHÑ··¾õãS_$G7e\x0005¸\x001f?*ÊOê\x001cî§¯ß¼yssõã³\x0017Töýê¡BõJ½nÊ/ÔKW¾Zº.\x0012é®ñldc¹î²PÛ©Ï'\x0001+õêzMÔ\x0014Ki©iÎQ6ÀÚ Ùs­\x0001ÆtfæýüBç\x001e9ëMö×õ}Ê¦$êÙ¤L\x0018rBZf\x001f:æ¥¡CËL
û¬Û@B8¥@t\x0010`Ð±ÖR\x0007×miúQO-e¥Dð²\x0008"qY6\x0016»<\x0008c(©co>â\x0016óa@\x0004\x0010IxªNÄE±Ráò¦=q¥}JÔÔP¬]k\x001fkg¤ªm¨»JP+´Ûm8íÙo`ÎÈo1a\x0010Ñ,ï\x0008èüð4£]é¼¤±?ÐJjcæ\x000cX&qIw1uü0¸{É½\x0005Éz\x000bâè\x0000Ö ­X8)ë/Ö.ðYD;ÌPRÛNJÍþ°ü¬Æv\x0012¹Å@µ"öÈMQ4u'\x0013bM0=v0jl*\x0003fYZ3×æÐD\x0014V/\x0002{­6®^	~VcÛÌÕnÊpÙ7ú¦·¶È\x000eîíûÕ¦õØÈ¶\x001a\x0019\x001c?î\x0007Ë\x001aÀ9zvJê¸\x001aJÔô³: \x001c\x00157èX\x0002¥,;ç¸Êo\x0007Õ 5¶=¶S\x001bí\x001dX¹%Ð|øZß\x0008A°ã(Ë¦ÅNý\x001e¡ÕØe\x0004_±\x001drw%B\x0019EÅìeHÒªÝ°ég-¶Ï5H\x0002õi°T#M+cì±æKM\x001d¨õvÄ×¢¥°ôé$F6²ÒÚ\x0019a\x00033etë³v6QÆ\x0007@\x0000~Ö\x000ecQ\x001a;cÕÑj¹G®ð\x000fÉ·\x0018
ï3å*9IÝ\x0010ù­^\x00109öûE\x001dü\x0015Ï^ßHJè\x0014äJ\x0002Û\x0011t»\x0019íâÈ{îÅµkÁ]òÈ3ÊÚ² C¹qÁ[YúA~zCvaõºÌù;}Á¼Ú`\x0000N°\x0015%\x0018v¼­ÿÓ»ãûú;ý5!rÁIOÚ3©:ð=Ú½V¼Ü\x001b¶xù¬ê-n©c ¶dfîp¸HîÄ½lñwÃ\x0016×®xÙâF$Ö}¹,Ô¦oªÐöø^ä&äØïñò\x000bý\x001e7ÁÉhl\x0016EÞÅ¨d1*~X²e«Ü\x001do
à [ÜYé85Mf?NÒÛbU~9¶*ú=îk\x0001ó\x0005i1V®\x000c	®Â
qU¯+Ê±Õ"-ªôÑ\s,[þ;¸ìª\ÎÄçApIüåØ$êçßÎ$Ò\x0001ýåøêÁ\x0003²\x000ci¤~*#û\,·¨Þ\x0015ÿõxÅýþWò%½eY2(ZÓ²ÌË¨O°1MÎÚÑ:5¤Ëó\x0017,ùÝñëmböÒ\x0015ºdê9éídòØ©z
m{cî·x¡ìX$6nÙz#¡¼æv/dý±î?è\x000e}»úé/þHH\x001f®ß¿ûpÿùÝ#ÌT [§é\x0014\x0003ÌLb\x001f,îÍi¥·W?Ý¼,?>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun</p><p>Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T</p><p>T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-qclg2PPNe4bIZY45QOQfUuiJCOU`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-9dsHCSh8tdBXqDCK/WLDC8hitEc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-9dsHCSh8tdBXqDCK/WLDC8hitEc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-4ctOBU9pBi1A4oyznWd/HHPdwzI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `95ae-srHAyIJK7YgFWVVSZDAxZyffYcs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-f0rYb0YdLZP2YJu0VzUwBozM7P8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-gEgaLlH2zKGrOgilRvIU3ymMhhs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8110-ymd3XaCoAxAWaSgPtZdTbB6+9JY`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-zfO8340ugbbSPDQlINrkPJEbOyk`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-QKodHt7+KzPB0jlPSwM05TWfWLs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>魴��%�c�5�\x001b!�8�\x0003�}K�$#�</p>
  
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
