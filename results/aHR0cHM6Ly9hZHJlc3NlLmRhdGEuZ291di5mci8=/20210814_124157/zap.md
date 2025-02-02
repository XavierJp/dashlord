
# ZAP Scanning Report

Generated on Sat, 14 Aug 2021 12:35:48


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-10.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-10.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#tb37E`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-01.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-01.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#jQrA`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-14.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-14.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#Na7f`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#tb37E</p>
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=§õ-Ö&&óÇÇÛïÿöû?\ýrûÛ?\x001e¯1É\x0004l\x001ek/Ó*1\x001a\x0017s_`Æà[\x001a¬«\x0010BLM§ïÎÿ
WI\}{zry¹#<IL+\x0001òÕ§éÕ.\x0015kZ\x0015ÐËjCJ#kÀ8hbMu\x001eÈÚ'6bM\x001b\x001fzY½ÄJÕ\x000e-)\x0003«K\x0019g`
É\x0005Ø\x0015\x000cVÓÏ\x001aBrWU\x000eCÈ\x0007Ö´) ´\x001fb#V¸ëv\x0005«JÕ3Àª½H\x0003«O	X]Ú³\x0011+Ü}×ÍAX\x0017\x0018¡@V\x001cC¬Âoù¶Àªòýç\x001d§t®XÚ5eîÔê-o+$±ÿTqz©O¤Âó
PÂ²\x00140[¾,Þ%Ò}\x0005ìá°\x0010®\x0000è}lC\x001c®@ò±\x00016y\x0007\x001b±¸+DÖÿSñ*Sé	\x0002³êÿ2?w×_FªöÃÝ5üSÏwT^²Ua«gbÞà|h`Eë Ù\x0008Nãèúpvt\x000e¬g3&\x0015ëNÕö°b Y\x0005NÃ\x0018Xu
Y\x0002+ÄlÄºSµ]çêÒ°m`\x0005M\x001d\x0007Ã¹JI¬8òv;Öªí:WRò>rAß;±¦ì\x001e°Z)7dÝ©Ú®s¥ÁÀ
W7\x0012«Lñ\x0017`u³Â«u§j»X-0C\x0002Uå;ÀçêÕ	ÓÊºSµ]¬ÞÖp®Xe~[.ex7bß\x001dúYE$3\x0016\­ÉóÄªù\£ßug\x0018t±´r\x0011ïÀ\x0010ÝL¬ÏÕÛ9Ã µ4\x000cº`iP\x0001À\x001a\x0005\x0008ü¸Â¬âj-,NXÃ·@a¦`-ß-_\x0017\x0006.ä
±%dj7\x0004X?ÌJ°`Á¾5[dÆìºj:_Y$é¥\x000cS¤«²¤Ýô©\x001f®Ñ6¸îÆÕòÐ¤pq,O¸­õ³ÞB;îûãïÙùñós¼{(ì£ûÏ·71¤\x0006ÿõ\x001fÿyñËíR³Ö\x0005j\x0011ò\x0001÷^¤\x000b¡b2\x0015áÿM0À`\x0016\x0006\x001d\x001c\|{:mÛ\x0016ÜIÿ®ä&Eº|ÀB[¸5E\x0012¢bÒ7ëæNºx\x001d·õ1åÛF,ã\x001c¸µcnc6çNzy%·s©rÝ\x0007\x001c$cSäFËT\x0013q¼úæÜIG¯=oÆÂÃy;6à¼ÓÊyà¶rÊ´ìåÆ¦:¹úaþw\x001cx+ßftN2e\x0008N\x000e26â¡L4;ÛÐÒÿõïwÅ\x001d?»\x0019"å\x0007¿ýï77?§ªá×¥\x0002[c(ôNY9Å(l¤Ø´\x0014Äg'CÜüàèàÍÉå»Ë\x0005°XöõÓz
õ8å¨¢\x0019h\x001d¹KAJ½!-Öã_Ý´\x0018<M´\x0018\x001eÖh\x0001­¶t¶ W§LºÅ´ÿsu\x0011Ú\x0003hàÍ
£\x0019¼\x0017À\x0019¤PFÐ©zÚb³sApgÇÈ6r\x000f$9
ô\x001a"¤±×@\x0018f¾û\x0002Â¿ÞJ÷']¨ºon\x001e¿\x000cy²7\x000f·_ñ^>Ü.üêØ
¯)ü`Üaº¢Ô\x001cÆ8Ex?ê7'ïÄÙÓø?//N\x0017 ³ôûgþËç[ygGQ>\x0000=~¾{xZ;x\x000c]Ö Sy\x001aÕ 8nÔa\x000cÇÎ.®0î"f4>~`\x0014*5ÇÆ¨§\x0004é´\x0010îâd­Vq_H¡½Ð\x001f\x000f³öz\x000bã.æÔÈ
¥CA¬\x0007ß×`é$2Z¡ÑÅÍ\x0018w±¦FF`ÀÂ
d3K5Åðr¢ /Cñ7bÜÅ\x0019Õ¿\x0007Ä0L¬\x001e\x0010bD·Õ{Ió:þhÊ:¦\x000f\x000eîLH¤\x0011WÜ¤KiÀd¥K©ýªÃüÉýõoÿ\±±wsðííã×aQÄ\x0012ää\x0016|tE3¢ÁØz*Î<6öN\x000e¾=½ü8¹:¢BORi%zÄäaX7éÓ`%¡\x0007-¦Ö
tVTëØ\x0015ö0ùí&ý
lv´\x00190b­êUÕÎþãí³.nÌ»ëÏ¹çäç»Û¯K#$X¯,)B\x0002\x000f2§T)\x0019)#ëÃ\x00196@\x000f}='ïÎN?NH~þþ÷=\x0015ï¯ÿ\x000e¶ÖÓÓRsKáÖù\x0014~²Ö\x001e\x000e1\x0006¡b$@ÙYÑ6×û£ÿ\x0001&×ÕÕÕõ£\x0012e#´ùá
üA1üñîúàÝõãÒ\x0003ÖJY¿?L\x0001³H\x001bC\x0014ÓáÝ\x0012wG3ñ'ÆU%®êÅcMÎWa¦â}\x0010´G;ø\x0008sñÈ\x0016^]òê^^oèB¨`¸Ö\x0006§èÒñ
1\x0017nÁ5%®éÅu&í\x000f\x0005^ìMÅ\x0016àPQ@\x000ca.BÝÂ\x001bJÞÐ}¼\x000eíÄ\x0017Ü$\x0005«>P³ªo9.õaóc\x0013½¼Apí\x0015\x0010¬&^g\x0019XÍåVZ«ç&»ß[ðì7(c)B=d\x0006E7éã´\x0002W\x0017XvßàH\x000b2\x0011Xä\x0013¶ìG'7ºÁTÓÊÀ¶\x0013\x0018ËÓ£ÅTÞ¤ùÃl\x0002«×U¼®\x0017XôäÔp9\x0003v\x001c&nu#|\x0005ì;­¤å\x0005(Ó<Ö:\x000f&\x0004éE¡g\x001d¢\x0006àJ¦É^¡æ±,0nÈQÂ¡Â¡Ø\x001b±\x0011p¬cï	+µFä\x0012\x0007\x001c\x0003 XËÍ»sËU%U¯\x0018ö¸+9EÅp3\x0008\x0005Æàâò	Ã-Þ\x0008¸2ÒT¯ÃãÒ\x0001k¡YÍá~:`i7²zTm¥õª
/ó°Æã\x0002ÃÁÇãz\x0007Ì§lÄ[i
Õ«5¼©E\x000exA
Ë$­LÃR\x0000ØLf5[+­¡zµu\x0012\x0010 ò\x0006m¸\x00111ò\x0000ÿ#àJm¨^µá±¼,\x001d°·Xl\x000eØºì\x001aÍF÷\x001ax+­¡ºµFÐlY\x0006Á!¦\x0004;F6nu+­¡ºµR\x0014ð\x0016\x0007ÉÑ\x0014=Ê¹\x000c	Ui
Õ­5b¶ÝÑíÐ2­¯°­n\x0000ÖÖÐÝZC\x0019~s¸\x0005)U\x001d*Ö\x0019j>ÊÖ@[©\x000cÝ«2
Xh6\x001coØH\x0005\x000fT{*Ål=g\x000bp¥3t·ÎÀùl	\x0018×"IºÀÔè\x000f\x0007\x001cfkwZk×¾×·wØ­qÔLL"ÂHÅVÚÊÓÓÝZNy*ñõ8×SSäU\x0019\x0016\x0011Qnu+¥¡»\x0015Tç\x000bÄ\x0011M¶\x0001Ø±\x00106z³\x0013®°î\x0016Â«u°\x001ak»\x0006`Ïårf#OÃT\x0012ÍtK4GÍÊ\x0016¸\x000f¸Á\x00086Ñot¾¦\x0012j¦[¨¡ÎH\x0017bØ8ÎÕgì\x0018ùD©$é\x0010^d×\x0013ÛªéÁ@
AQF·Õ¨ÌJÓkVÊÍF\x0004Ä$ÒB`	±U¸ÒTVéµÒÐUvdVj\x000f\x0018ë\x0012ïvÀ0Ý\x0002âÿÝ«¬4Ók¥y[0¥¡9\x0018\x0011X+\x001b±Î°°½"Â£f#`?Ì3O®§¶l\x0007oeVÚêm÷	c/&Õ,aLa2Ü#Ýak·qå, WÀø¿÷\x001a\x0012qX¬ê±ªïU9Lñn\x0015³Ìíø»¸e±$¢1t)}\x000e] <Â¹\x0001)\x0012¨Ö>>\x001c$]åæð\x000fÜÜëÇÅU\x001a+©\x000eNrªKÂK/ÏGóZ.æÃÑåL1dfU%«êc\x0015já´La\x0019©ì\x001eß^ys\x000bQuª;U¥±\x001càeøaSLB¥ÈG³}\x0013VS²ÎcØ3°\x001aMéC\x0019¡sÅjMXmÉj;Ïæ
\x0003«u8Æ'«§s
q\x001bTW¢º.TåCEÙ\x0008\x0007LýM¤í|_ÎéKNßùùi©\x0011\x001c©\x001c/¤#M\x001b¬áHíkaêe¬9¹¤è<TEçxª\x0001½ êÇ³ÁÐ±ÒØäÕ°¸}ò
\^:Y\x001bäPÊ2)åßæ¶ÊJ\x0008È>) £&£Ü:¯¸Û\x0015sC	\x0016ì²M®¬¬ì{[pÔ0f\x001d,G°êæ<X	ÜYUk­¾k Á \x0018Ä«5XH®¬ÓÔéèu\x0010\YUÝ\x0002Õw\x000bÔ¤\x000bÀ\x001e\x0014Aàê$ãÅ+»9 ª[ ºn¼
`Û¥Æ6c\x001dÉX\x001cò·	l%eUÅJäDZ\x001fDnË¤Fbï¬Ü5T¬¡ï`y¿
<$ÌP$Áe¸@\x0007ìÚùêÞÅ°±}\x0007«pù 
¢§b"}U$
^
×,cÕúÒ]êKõOIw«À!£ÕÒÜv¶õ}9lå\x0019è>×@FÃºÖéHQ\x0004Ð\x0008:`·9ÙJÈê.!\x000bv\x0001×ûÚa$^:YaIn	\x0011_	Ñ,d­}>ç@\x0006É¢À!¶%íEm\x0012Þ¼\x001a!_\x0008[i\x0004Ý¥\x0011s<]ÄÂµ¢R'	ÿÇÓu1¼Vµ\x0010¶ò\x000et{+ûR¶Ïb\x0002\x0005­CP
¯ä\x0017²VÚK÷i/\x001cw¼YÓ\x0011Sº`]4¯Å7\x0016ÂVÚK÷i/\x0011-93F\x000e»\x0007\x001bF°¦ÕêµØ¬öÒ}ÚËâ"L\x000e\x0016wå¤\x0002éÀ3§\ó=>a+í¥û´\x0017NêHÑ\x0016§;Y`e`kv\x000cÆbVSi/Ó§½LäÜ©bðÃñ`½#OÑ½V\±\x0010µÒ]¦Kw©ÓþVãðdÀ8\x000e\x0013àZMX+u`ºÔÂ¡\x000c\x0002Ð\x000c:]\x0001£¥ekËmbsJÂ.	«"83>±ÂÍ%Vm³\x0001³Ñu­\x0004¬é\x0013°Ø2¸28\x000e\x0017\x001fÙp[Yf¹`¶Ñ²¦¯¦K¾øti\x0016=\x001a¬¸À%ï\x0000mX+ùjúä+jÄ@0\)\x001cz¯ÕÃ/µÌ²}2\x000bwý_êÞ.Y¯#·\x0012
'à\x0013	$ò/úè*:X\x0012M¾O\x0015Äë¢¯Jª¦HGÛOßú±=Gr\x0013;ü6\x000eýíÜYªvW[<R©×ÆÉÄ\x0002ÀB{\x001c¥\x000c$Ã2ÑÉ°LLÅÏÁjbØ0\x0016Ãú \x000bp¸ê\x0012D\x0015Â\x0012\x0011¤´÷{\x0010¬ñZaÌkU0ÒÝ\x001a zX×*\x0005\x0010äÉ§Õ§$´Á\x0004±a,åZFë¼$N¾snÕ\x0001¤âX+Ø\x0012÷­±«<\x0006^8/5\x00185¢Õ²~¯\x000f÷ XãdÃõ\x0000môR\x0004\x0011ê©7W&7býñS`\x001cW\x0018s\\Ëø%÷£Ê5QOßÔz>\x000c6\x001ag\x0010Ç\x0001V^, § \x0006GN\x0001Ì©tGã\x000câ 3ðãìåÈÞ¤=ÁIGRb)`Íýc÷+fÙÊ\x0019­gY%£ÅÒ3Ú)ql4qA\x001c\x000bÕ¼-âæ
E±åQæb	aJh\x0018Íõc×\x000brá]¼\x000c6\x0016\x0019ò¬\x0006Ë\x0015ó¦
éq¨&ëCY\x0017Fîè\x0011»òþv¹
è	ðsÂ­d"4\x0016Á@(Z'¨\x001eJä]ëi\x0015©\x0018Ó÷dò®4wÒXÅ,½Å¤ó(î÷v\x001d\x0004k\l\x001as±5¯\x0012ÑTØùË\x001abÙIÉw2.6¹X^ûÛ¢\x0002*<÷ÒAµA¢î¼×Às\x0010¬·ÒX¼å\x0008EÝX\x0012¯u¸\x001aÂè<\x0007¬á4Æ\x0007Á(Â\x0010×ça9'\x0013Ã9¥ãdÂ­4\x0014n±¼Ôä)ð+m\x0003ë´V\x0010kø=ÇsÙÆ1ò¢zî²ôÑÖß´®WËî5É\x001d\x0004k(!Q\x0002\x0011ÈÜ\x0005åJº®ÑWÌIÁ\x0002M9²Ù¸Ù<æfk\x0018¨ùLõ\x0000\x000fÍËFòY³Ú9/3Ù8®<æ¸j\x0004 Sz5EHò2SsÐ,^6Ý×:<\x0007Ö8®<ä¸ \x0007/Ã\x000bÄ­ß¾ÉÜä(A7\x0007S°\x001a¿Çü\x0016ïÂ\x0013Â²úi1,xÍ\x0010ÈÍ1¬q\yÌqeÉÕ°1ó\x001a°Å°¨µ
Êe\x000eXã¸òãÂ\x001d.u¿Hî%ú\x001cqM	»³	»óPØÍÂéÕR
h\x0008er-qð5\x0003¬ñ²yÌËò0Ó6«9
Í:\x001c\x001a Ná¯b"ï2\x0014yCªü\x0015Å²´èÀ³eùæeyâf\x0006XC	e\x0012*Z\x0013«icùÍÅ² Ymsú ¼ËPä
<rÕäãXL»\x001arÜ(
À\x001a\x0002+c\x0004Æ{°\x0014µÆµtø7ËÒz\1\x0004VÆ\x0008§ïY\\x001eh¢\Ö3Ks°\x001a\x0002+c\x0004\x0006 Ë\x0015(úÔ\x001e=\x001czÌÑoª¾\x001fÇjø«ñW,N)÷\x0006G\x0011\x0013ôIíê§8Ùbè«Ñ\x00178¡ÜjW\x0010\x0001^¾æÕ°{\x0003Àíéç?\x000eY¶æíù|nñVHÒ
\x0013÷tÁ\x000e\x0002õ\x0016è\x001f`ý]qZÑ%yûä¶¸ÔNÉ½ÀöÉó\x001fÇRp'ý¼ÄÎN\x001b¨¡l¼/p|\x000em²hÇ¬Ã"èÕ.Yã\x0016@K1ns×Îq´Å¢\x001dbj0$]²\x0014²öDqj\x0007ß9<\x0016ì\x000f\x000cE\x0006Pj\x0018##o\x0007A\x001bPk\x0006Û{a£µî`¬i7Øww¡ëóö¢S\x0018\x000cÀú\x0004\x0018ò	ÀÕã,¶åy\x0014zÖ;C2;\x0003øh\x001eaÌ¶úc8VÛ&\x0015WiO^â Zk[\x001c³-ÏÿïKQõ{;å¦\x0019Y\x0018 õ·8äo\x0007,¢]ð6iýæ4£mF±nt9´+V´|2]IwNS\x0004àj®Rà®ç*Ïuyëshýç(¦"¥ú\x0014¹\x000e>eàã÷ÿëã\x000fm¢®·M~8Òà\x0017µi.øÒ\x001a\x0003»°Ö7éæ´Êà'ÆaK×ðHÒ@y3ÂÒëÙhç¼,z\x0014;aFT_\x0002fQßs*¾\x0017\x0003Mzur1'7
\x0019¸uJ\x001e¸ïGJwÂÒÑjócÄ\x0019F\x0011³ÊlÔö$\x001dÈv¡èc4KBM9ÌåÃ\\x000fs\¾[Zí>Ðþ\x0002Q¯ä]açÓÍÿÛ¸à5¸i5·Ü
÷Ag2©o'ò^ãßß?\x0002Í!ñ\x0018f\\x0016OJ,ä=¿¬J\x000c¯pN\x0003@µõ'\x001e¶²A\x0008\çÍ2ù¬\x0013.æÜÂø{£î\x0019k\x0002÷ ¥iO\x001aprÈ!p\x0012wS|\x000câ(dâî»æ8r
¡ÈÓ\x001aé\x000bë}EûéÒ'\x0002£Þî×çt3ÃÚÐÃ1RÖÚ_(5vÆ¦Üg\x000cSSüËá\x0013R	Ã¤ât\x0019,U"ä\x0005]Ëy.Ð{òü\x0014¯>!4J*ö©8É¨´}*s4>êF@9ÍO@öÒ\x0007'É9òIT7jg(¥hNý\x0007õIÃÅ¢¯±yÎû\x000b|Â(0L)Ë2îÖ\x0016ÍZ²\x001bW7IÄQæÌüûOü³\x001föÏ!gy1»)ÖÓv¸IIÊ§ÕhVÅmýÍÕ\x0011:\x001dýf·'I¿ØZRc\x0000+±ÃAÖßþëßÿãÔF\x0017d%£& {c½}2TÂN¯üÞ*\x0016×hq\x0014-è\x001eé3¬2d\x0015¬iìfPt\x0018¬_õ£`}P}W6-Æ\x0006IIkii.\x001c\x0004§¦õ²>³\x001e\x0004])\x001fx¯ß\x000c´a6¢eC±-éèo\x000e¾\x001fÛí¸í0Ú¸F\x001bOBÃÅ¶ý$ÈØ\x0004Ûv³\x\x0018mZ£M£hk6\x001aÅ´7å5y ÔÁ9¦Ík°y\x0014l\x0002tÍyYÌ° -"dS]Âöøïa´e¶¢ÍÚÜ]m²;gu	´­\x0013v\x0014íMÐhá\x00067\x000c×©à3\x001b\x0017\x0004®ëäàófió0\Ke£\æc\x0017ï,5ÀÑe8èûòó)·\x000c\x000cÁ(ù\x001a\x001c\x0007Ë*í\x000b%v\x000fFÛÑ\x001a.Q2ó%ö=d¼¡	û:]¥ZBÙ\x001eP:\x000c×Ð\x0003ò\x0003çõâ\x0016JÒàeÁb°ÝÅs\x0018®á\x0007\x0018%\x001a\x0013Þü\x0002©R\x000c¯ªë>w³\x0018x\x0018®!\x0008\x0018e\x0008â&Ö­}\x0013ÉxÛI·-\x0015s\x0018­a\x0008\x0018¥\x0008ÏÃÖ¹ëRSët ^!l^\x001eFk\x0018\x0002F)Ó8¬°È~³mê¦Ý\x001eZ<
\x0016
Aà(Aø\x00185{(¼^Q¶caVö
sÎ-\x001aÀQ¨ì*Oâ¹rne¢ùC\x000c8Å¡Mv\x0019\x0005®äà¢^_tA¤ä*m?\x0011\x001ck(\x0002G)\=;ì{*%jqû\x0005æ0Vìàh¶ãkô\x0015Åq\x0006,¡B\x0014Q¦\x0012òÝÝåçà\x001a:Ãa:«ìbÚÖò¹X\x0017ÔÅ´]>=\x000c×Ð\x0019\x000eÓY)º¶ x^«ÁÊ¾¼]<\x000c×\x0010\x0004\x0012\x0004¨[­YðD\n 5.lK3\x001dEëÏõ£>TS¿`uª<\x001dÊ\x0018×\x001bëG\x001dnàýÆrnY\x0016YÎ-v¯°ÓS\x0018®q¸~Ôá\x0006^lë\x001d\x0005UÓG\x0011\x0011âå×Sn·å¥Q\x001b\\x0011ù³¼f1®ê¦'·­L\x0018®q¹~Ôåò>\x0005êGAÑê`\x0018\x001f)\x001e×\x001bëG=n`U\	\x0015j\x0002ÑïÆÝ\x001eÀ=\x000c×x\?êq\x0003ÌÔ³ªHß\x0017ÛÄ2'Q÷ÆáúQ\x001bPÕ.*Ú$£¢\x0015­z±ä¶5\x0019\x000eÃ5!¹\x001f
Éùä¶f;¾\x0008Z]\x0011ÍÓÚ3Ðñ¹4ìs1s\x0002ÉpYý¦Õï\x0010u½|òÛ\x0012sÑ\x001aKÃ.\x0017£\x000c/Tã:®7´ºÒõ¥¦À5>}®'n\x0012XË§¢íª@]þºèúMkkúÃ>×;yÂÎ®îªÅPô0à¶¸Ða¸ÆéÒ°ÓåQ\x001bhÖõö\x00027éº«\x0014auM\x0019FË ¢0\x001ap7¢\x00047ºÚ7\x0008M\x0001k|.úÜÜup²çIÇÆ¿±¨mß^ûp\x0018®ñ¹4ìskÐ
x\x0019zLE×e¦²Ýâr\x0014m01y\x0018É¹w¨ÅäÕ¸E^!ûÄÕ¸s¼X0\x0014\x0011)"\x0002?ÿ/ÆåÆ\x0016Üx§N·\x0012Ç£\x001b\x000cGQàg(ß[ßÖ©)êÌ2éõ,ØÉQ'\x0016y|aA[YÕ\x0016ÛöÕÊ9nwY\x001cFk|X\x0018õa<ÝH\x0002«ºÍ-\x0010ÞPaù÷)p[\x0008£n!Ö&\x0015<L$ýzHº± ä¼Ý\x0016y\x0014n4~!\x000eú\x0005rNwíÔ£«rÚXúj«ê\x0017æ8Ý¼n¹\x0011è-7gH\x0005Ë³w*ÿ\ÿr$
ÌÎ\x0001ÿæÑKÚ\x000bOiú\x0008¼~Kë½\x000bs¨\x0018Ýc3£\x001b7ó¯U<'øäpÀ8êÀ»7RÑ$»H¾hÛó\x000cÇû>1õ8æeBGG\x0005s±9e\x001d\x0017\x001eC\x000e\x0017 s(LýE°Õ\x001fÖ-#aNqÇ}r8.
ÐÈ±î=D½\x0019#L:\x001cå1èrá\x001a:xÈ½ÝE×vy
ãÃÎæû]Ì\x0008Úõê\x000fz»ÞÇ'_xóÃÑý}P³Omp`f%\x0002.ô®§míð×O¾þæé\x0017\x001bÛû\x0014+®±â\x0010V\x0004/µÔÄ
ÒAZõ \x001fí©éÃPý\x001aª\x001fºHÙJý5c[\x000fQ$Ôç¸½\x0012í0VZc¥1³V¦\x0008jÖ$á%dGú\x0000\x0010¶3úÃXÃ\x001ak\x0018³kÑ\x0005\x0002Õ®×ö4»¦Øí:\x0007k\ccWW^¨\x001b(}mW¹Ùu{Dè0Ö´Æ\x0006íeÅØbW\x0010»¨w+n×¦\x000fcÍk¬yÌ®¹/¬æóeÌ-u÷\x001a¶#àÃXË\x001ak\x0019ÃêÞ-~\x0007uQEÎKÄmÎ=õÖ·P\x001b\x0003¢^.>°mÓzý!áÜ\x0003\x000b·\x0006\x000btfi\x0018\x0012°1iR\x001cw&w\x000f5Ä\x0005cÌ\x0005\x0011D£&ñzLq±n½ÅÛMÁ\x001aê1î\x0002@	¹rýWJ\x0008ðÀ«Xæp\x0017\x0018î1òúÏ4³®I:Ën·\\x001cFj\x000bÆ¨\x000bDô%;^â&fÍ½0ngÁ\x001aêAî"Iâ%®bzUËn«ÿ\x001c\x0006k¸\x000bÆÈ\x000b H«c^vÉ¾¦¬\x001bëãNÙü0XC^0È^Þ3
hd(âñ©\x0017J÷4T\x000e5ì\x0005ô\x0005YÔ\x00112/K\x0016\x001fµl\x0013ó¶\x000eÅQ¬hØ\x000b\x0007Ù«\x0002\x001eÂèæÑTº]§X´Ì \x001fðÍ½XÖÏV_ '\x0016·[\x000f5.\x0016\x0007],\x0014\x001d)5ô"u\"FOsÀ\x001aÇ\x000b½¾¦Ö\x0000Û^\x0017°¥·cÒf¹à0Vã
pÐ\x0015°d¡ø-ìÛÐbÞà¸]­;
Öëå\x0007¯\x0017F}àqäU\x001dxR}Ar¿¼¹_~ð~ùÒ\x001f©CÖ£\x0004Ú-\x0018Kâ¸¼¹_~ð~±e\x0005ká¢³\x00186t¬S\x0008Áëå\x0007¯\x0017ô7TWcÚ¨\x0000Ú[á¶|\x000f5÷Ë\x000fÞ/.l\x0008{Å"]úÀ»9\x0014ìû\x0005æ©Db^<<{rQ´\x001c\x001eHDë<Í­o`|\x000c\x0019ã0d^Ø\x0003ä\x000b¹ä/\ò\x000cßU\x00127åÎÏ¸{¶áåÛ\x000fï>¼}R!\x001f~êSqöÌ´íQ\x0007Ék\x000b@¾Û\x0001ðòÙ7Ï¿yö¤âÝé×0ý\x0008Ì\x001f\x0014¥\x0001¯£cé®C8\x00033¬a\x0001©þ²]kVAWÓ"\x000bÑ*È»µ3 Ó\x001ad\x001a\x0002ÛH\f
@i\x0011
ND\x0015*L¼\x0017\x000fYÖ0Ë\x0008Ì\x001c\x0006Ú\x000f\x0018 [Óß\x001d=\x0001\x0013ì\x0005\x001a¹A,¸ÜÆ73V*HòëX³¿«p\x0000(/Ñ²\x000f\x001bõ\x0007|ÓÿñOo~ùu\x0013~yòâã/¿¼{ûþía
_tâÕ6\x000c\x001f¬t.¬Lp\x0007òóß½|úõ×, ðõ\x0017¯¿þºþüÙò Ç5z¼Ê\x0013P[¤ÝÐ«Á!ÝÝ$0Þ¯Ñûè£l«OÄ{QHÊfï\x0012ð xZ§«à\x0014lÒ2å\x0015T`(+ú»µÛAôa>\D_TSõùOì¶/w\x001b\x001f\x0007ÑÇ5úx\x0015};á\x00190e,(¢ÞÕöO}ZO×Àû\x001aÃIµ¸9@&o	\x0014ûÝ±à«ã}ô\x0000\x0014üê\x0001èÛwo~øøýQÏNªzP=;hK\èA\x0007îe!ß>úÅëÏ÷Á5Ø2\x00066ÃâM\x0016°à \x000eÆ>_q¯0u\x0010íê]¥¢]½«³måô,MÈ%iÏV@­JäÑñãpÁÀAë&¯\x0001=Ô¿l+1é\x000e£ß)ø\x001cë
\?\x0008·¦y¾Ö2\x001dIo[Æ½G«£`É¥Á£\x0010cSB©`½¬ÂP\?¸{¿£hA\x001bÆÐ\x0016^%®ó`Qê1G=	±l/k?\x000cwUû«pWµ¿3p	¸ªcù¢#êz÷ÛÌÌq´ÆáâÇ¥zýEû=eÊ²\x001dÈ{ÐlÊö`þq¸ÙÀÍcpÉeiáä¹\x001a©YûÛu)nwx\x001fk\x0018\x0002Ç(x	¶Z·cûê,Ôº©Ì9ºÞP\x001f£e}ö6õu\x001bNQØ,<\x000e×P\x001f£\x0008"\x001fù\x0005s[óÀ&dé\x0003t¸q×]\x0019.Á
Ü\x000cÛ¬r\x0011mE\x001fAß^×LkHÂ\x0004\x0005$IY+@>z=ºè×\x001b§ë\x0007n^\x0016!§\x0014¼¸ø¾¸ TÓN²­ñº~Ðë\x0006dgo
"k^$'A»ýÓöÞËã`Ïõ>77ÛJÅm-z
ÕõØâö2ÉãhËõ.mb[Í&¼Ø¶×*2M
sÉø0\x001aôa<²Ôà2\x0001KëcÖp¡^³IpMKca.\x0013@\x001b
¬GA¥°kfár¿fsN.\x0004I{VO\x0003§\x0002È\x0012÷?·T¢ë§Q=ÎeÑù|\x001aQ§\x0014zåE7àå]^\x000cÌê¿ÊÖ9ùß-Çøó?¼ùéÃû7ï~:X­®\x000b¤Ò\x00133«\x001d/ÒÝ%4cØ\x001cEøü·O¿üæÕÓç_nTe\x0015-®Ñâ(Úz\x001aÚ¸H6¸B\x00179ÒfgÑ\x0019¼~×\x000fãEtbÍ{¹
¸à%é3Ìa{Ð\x0019¼a7\x000câå~Ðì[IXê8ÎE¾ËP6#³3xÓ\x001ao\x001aÃ[³àÌÎlÁ\x001b\x000cKÔôUÆdÞÄ2\x0007n^ÃÍæEn'XÐbXº·RQTõ²ÛÎÙVp¿óÃ_>¼¿\x000f·¬áÑÓ@^üoô¬9"¢âªÃå¨-Ö8aÞ>(Þ:O\x0003æAò&Þ\x0010}!~`b\x0003s_o\x0003¸)Pv\x0006°u¾ÃÞ\x001fhÄÂÕµÕS¶,$N"<\x00116\x0007Î\x00006÷
\x0006/\x001cÄ
¸5ò°«Õ#\x001c´¤×ÐmSLü\x000c`saô\x000cSu\x000b-N¼	>6\x000fìIï\x001cnKÆ\x0000æHàè \x0016dnNi¸v}ö\x001dðæ3
eà(g,\x000f\x0016^ÎpbìË¥Ó\x0017zg9a´³ÍÊ\x001a¦7´Ó7®z2
\x000f\x00072n¬L­GySfí\x000cy|û\x0002l\x000eØ$\x0002ªÖ¦¬\x0001\x001c¸Ý[}\x00045øÇïèÞ­\x0006\x0004÷ñ?ÿçÑ'ÓQõÐª{[ÙOòûéÜ×O~÷úëg\x0007°ú5V?5«*z	ø `}V´ìÕ\x000fB¥5T\x001aêä! Z\x0015ºê\x000fR·ê¶¦Òa¬a5üU5®¡ÆA¨ÐÍÊpª±¦4Ñm«\x0003\x001eÆÖXÓ¨Y¡\x000fÝÕ(Ø«f0¼­\x0012y\x0018lY-£]FC¼iÒ÷aV!QåØmÈ£`Áú¬Q§\x0005¨µRÿ2Êõò}­GÜ^´´\x0016Ã#\x000f[Ð=ìÛ'ß¾}ÿ/ï~:Üíà°O4¦ü \x001b\x0007ëKHv¶B}ûìÕ·Ï¿Üì\x0014xÔÄpq\x0010.\x0004\x0008µú ª\x0004\x0018½Õñú5^?W$\x0000Î¤©6à¶Ò	¼´ÆK£xúã
?\x000byé^W'F5D7¬ñQ¼)q±wÁ\x001bH.\x001bÏªk½%ªñÆ5Þ8l_èÚ.\x0010oÓ\x0001Ú\x0011Hy»¬~\x0002oZãMÃöõ:Ç\x000fÅ¨{=»B¯ÛÞQt\x0002o^ãÍ£x½.\x0013\Þ2Ü7\x0000Ò§×MÖá5Ü2
7&É~Ò¢h§æÕÛ¶»Ãì(Üu3»5\x00137oïKÌN7ÓBÒ=Õ¼{û\x000f\x0003¶ì6Jo<ý¬t5i\x0002Ayûð\x0004^Co0ÌoÔµÒj\x000e^ÑiG\x000bá\x0004^Co0Ìo¬-ö­ÁNa]ß¯Û¶Rï	¼Þ`ß|ÔóÀ«E[+õÎ¸½ëã\x0004^Co0ÌoeQM
 t¾ø&ÅH&ñ\x0005\x0018~aã­àrWã¥E'6÷Ú\x001dN\x00006\x0004\x0007Ã\x000cWÓ\x001fµpìÊ>É­bg\x00016\x000c\x0007Ã\x0014Ç3O3\x0012-Í2\x0013«G\x0002öÖ?\x001f\x0006l8\x000eIÎS?\x0012\x00015ÅHNÙ	·x\x0003FÃr8Ìr¨\x001bãYFÕsbX#·=É{\x0002°a9\x001cf9ß5>j*$í\x0004\x0010KÇë'E=h¸a¬u½\x0004ù& ¢Q¥/~
Íá0ÍÕc >\x0002ºÒm\x0000Ùi\x0007ÂÐ\x001c\x000eÓ\x001c\x0004m¬ÿy@\x0015¨Qû¦ix
Íá0ÍÝÖu¦\x001a¶¦a,Úmäó¶\x000eØ	Àæpæ@¥PS5«4!V\x000b«þ´\x000faÖ34Ã4Q¹bÎÒ U-¬Û\x0005¿\x0013
kà0kðÌ¤ZØÉ4rÌÝE\x00047	¯7¤áGI÷j´\x001e©ÈBêb_P%QwåÎâ5á9£ÚW\x0014·"Ý&Ô³¦rÞÏ
Ô¼­¤
ûà\x001aYJ®Ì2ÏEO°îÃô\x0008®7NØ;aö\x0012îá±\x0016ñ\x0011já\x001d\x0001¶\x0013\x0017öÃ^¸\x0011ê#ªCVåÈ¢J|\x001c+O\x0002l¼°\x001f¯¦\x0006j¡zá¤Ù²^:\x001eË\x0004Øxa?l¨²~tzrý\x000cï¬9\x0001Ø$\x001b~8Ù¨¾L
\x001cUy\x001b9ÔÀÛí'ð\x001aÖðÃ¬\x0011¶¯JsYß\x0007Ä¾¶Ûã%Ã\x001a4j¤"{,R\x0000/Cí¢ª1áNÈ	À6h¼ 8©_\x0000,oq(ª'¹42\x0006
g\x001a9Hà\x001eçÑ_t\x000ey\x0016'¡8\x001a¦¸\x0014´Ú\x001eH_eë\x000f\x0005/î¬8×>\x0016
3\Ê\x000fÔ\x0018\x001f5³çi¬\x0006\x0018f½\x0016a8\x001af¸L*ÈÀ»D\x0013µFÄ
ø®$ÇY¼àhàríW\x000fêÍªb\x001fºYõv2\x0004GÃ\x0004WUqÛp¢&Â\x0002¹za[\x000fñ\x0004`Cp4Lp%>è°¿èÿ×S\x001dú¼ü¬\x0007\x00182üF£ü¶LîªC\x0003EØY=Úö$Æq¼Áð[\x0018å7Æ«b
éVû+ºË¢Ró,À0Â(a°ì\x0011ò\x0006ê¸\x001ed¯ÊÙàý,À3Â(g ×!D\x0015aÒ-\x0005]*$À¤\x0010-\x0018Ò\x0008£¤©\x001fa\x001flQÜ\x0013OÜ¤;\x0017lÁ(i ï-hT\x0013OÑb!$\x0003h{øø\x0004^C\x001aa40D}ó¹kÒæ(­©Ååí¦¹\x0013
iQÒ@
²\x000f:ñ:`\x0012\x000b\x0007}õ\x0004æÕ\x000ciQÒ¨y¥z5^{Sd\x0005KÊ¨Gx[à\x0004`C\x001ba6\x0002è0'ñ&\x000bñj¼§YxV­'\x001aÚÃ´Q}Då\x0015=Òø[}îq¼\x000ci\x000e`\x0016Åá6º\x000bµ°ÓÀ=GÅ\x000bn[\x0001ø\x0004^CsqæJÒR¯Û
v(¨}2\º\x0004ØÐ\\x001c¦¹\x001a=\x0013ö©kîWÒèNmÖ«g44\x0017GiÎ{§G÷\x0005¸v$TNr¦YÑ°\\x001cf¹d8²b\x000f¢·Â'BiyGzÿ\x0004`ÛI7Js¼>Á8Îp(I¤?s
³Z½¢a¹8Êr5[Öb%Fè\x0006î³D%Ï{¢a¹8Êr¾-çaÂêÀ\x00028£æìiØ\x0000lX.²\MæÔG E}E,AçOKLî\24FipÛÿÈûâu7GI}\x001c'ÍºsÉÐ\\x001a¥9ÏZáíÎñ\x0016:©_ÕÂ³º¡¹4Js\x0012OïÔµüÓçÛ\x001b\x000fN\x000064Fi÷í6]öÄ»l¥}ªï~älc\x0016`CsiæÈÉ«\x0016Æõ\x0004#NòÂÉÐ\\x001a¥9/Q\x000f¯avj]\x0015,à«Ð\x001aKÃ\x001cçI\x0007f\x0013eÝU(\x0016\x0004Õ~l»ø0ÉyÔ¥Süt¤Ç!JÉ½Æ4fH.
\x0007Ê`\x000bs_l¨\x001eM,LÓ^¸!¹4LrRìá RÑ&y?d¸Âöl\x0018.\x000f3\x001c/þæ\x001e4+Q	#¤Iî,\x001bËÃ\x0004\x0017H\x0016H'\x0017Öñ\x0005o\x000fÛSÙ\x0016I<\x0001Ø0\\x001eg¸Ô\x0015Xx»1©Õ¾³²!¸<Lp¡w¯ºJ\x001dN\x001cDQ	\x0000Þá>	°!¸<Ç\x0011»±æé!ê	V\x00190í+\x001bËÃ\x000c\x0017\x0015\x0016\x000b×\x001cT9CJ=;D'á5\x001c9×ì6\x0003ó²y©¸×¨]ð¬Î¿l\x0018.\x000f3\ð\x000fâ  êrÑNÅvö¾Àkø"\x000fóÅm÷··ã<C-wVd\x001c\x0007\\x000b.ã.xéäY¢ÊÈE]pÒ´ÓÏª\x0014ãÒÊ¸K2AÀ\x001dÁZ¾.=\x0006NÓ^ñ\x0010eÜCxÙ\x000b·º«\x0000Í:g]¹b®\\x0019\x000f*uÿ\x0013ëSô¼>ÊÐd¦i¯àÅNõ
ß¹×K©Ç!i#]É*4Æz^S\x0000Ã£!p7|éjvÑiç<¥Ñ èÂ\x001cÝ¤V\x0019°sÕüÇñÔ¾i\x001f\x0005'ö¢{äÝ¤$\x0019ì\x0010-ÿqã\x001c7Ï1Z`')·{ÉãRÉ\x001aò!<;\x001bö\x0011ÅGðÒc\x0019+*ËSÿ?UûÃß÷èIã»¿ö7\x0014-æÓ\x000eb®ÿG0Çõ/5|=|Ê,vöÉªT.]¬]¥ò¯·5Gç#\x000cÛÚ\x0015\x000eßÛù \x001e.hP\x0015åkT4\x000fóGß´ûü2oUùZ@Ó3=+¶¨gúûGgúûñ\x001a\x0010µ45áö\x0016Ð«,\x001dM\x000bé«ïøáïøaÔÎþAëÚIÛª
Ißð¢s0ÍÌo\x001eyôhüjµA÷ë¸â9b\x0010Åë\x0017hG>ñêYù©{\x000c;»qÜ\x001e3Oõ´45ëªÁ\x0012PO5à¬\x0007h´7±êÑè¶}`¤~¬½¨£,;èf=?¶u¥q[{ÝNËÒ\x0012:â\¢¬`Ê\x0019/§\x0010â#º\x0010W"J/üùï~þéè\x000e:\x001b¸ËQúbª!¯^Ù©Â½|ñÕïõå>^\ãÅQ¼üø±Ø7°h´à±ÂlÃ»?B~\x0018¯_ãõ£xÙQ,EúàyxQì\x001bEÆÃ½\x001aÜa¼´ÆK£x£ûõ<@ü*Rõ®çáî¶Ï³xã\x001ao\x001c>\x000f Ïº!`ê]Û ;­\x0012á^×öa¼y7\x000fâuEÞaùK\x0019TSE\x001aîu8îã¥G2éõ\x0007Ý?ü×¿ÿÇWxwÔæ\x0012â²T\x0015åM\x0001}ÏK6ª.h|õÛç[\x001eI¤3R\x001cCZ¨ie$=Kèûn³â·»µ\x000f"õk¤~\x000civ\x000fm\x0006&]÷Ì\x001bbÒ¼}`\x000f\x0002¥5P\x001a\x0002Êk4d\x0011t½õ*èï¹\x0000ÔLÊM£×Æ5Ò8t8b¤tpSYô©]ªÒºg¯#Mk¤i\x0010i\x0012ºÍAÖy\x0019©0ËöûÆAy
3ÿ\x0015\x001bô¦ìµx(7\x0006\x001bèÚ\x0006F"m@Û¢Â\x0003»\x0013.>\x0018\x0017\x0005c>+À!7¨¡toûï?l\x000fh\x001cj®>\x000cÞ}ÔñdîeçdmZ@\x0005ww\x000fê)Ç¿\x000e½óï÷IÀ©û;G]¢§Àm·Çìáå\x0011¥Ö\x0018I(õwÿôþÉË
ëí\x001c\x000e|öö\x000fÇE­=QÒ\x0015[åYÚ
k PÍmUºßýæÕõo={úCÏývGáZ¾\x0003×ß3¾#$m>(E
\x0010!tQÞ¸Ùp9ú\x001d~ý\x001d~Êïã¦Ù\Se	#¤2Q\x001fó\x001c£ßAëï \x0019ßQÃxy:­\x000fW-ï]\x001b7ãV9ú\x001daý\x001daÊ¹r:"V|iï}È»
ô3þ"¿¸þ8ã3NE
>ËõèËãv?òèw¤õw¤)¿\x000eh{\R©Õ½UºioüG?#¯?#OùuP¿\x001diQ
^¾#ki:Âf\x00126|;\x000cÛ-7DÙîoéÇå§²*?ýòäÕÏ\x001f?¼ûóÿ=¼ø\x001bkJ¡Ê¬<\x000fË©rDÔ\x001bï®-o)ñ×O^}õúç;+ËËã*TYU¡FaK¿3ëÀ\x000eRé+~{\x0017Á9Ø~
Û_Ý_G+lß­­2äy/Q>\x0007Ö°é
lÄó ¯\x000eÊ
µiwÞ@¹]z?:¬Q\x000b¨¡\x0004Ya0,òs^\x0001k¶¿3és
v\ÃÝ¥¾±,õË\x0005v\x0017
äL`\x001eì´.Y»+\x0010{^]«ÖF	Þ	;¯açK°£î1ðÜ#bíþøO;Ï3§`5ìr\x0005v&UaãV\x0000hKÒ|\x0017øp;»OÁ^
mÜ%s£
6z¥¶QOIÐS\x0012wÞ¥Oá¶,y&ùå\x0003trÛËK[Ô\x001aetG`û\x0014nCp'y©Îô'mó®¸UøÃíí½8Û\x0010\x000e\a\x001càÂØV\x00047jù\x0013özrNá6\x00038×ÓÉ<wà/`Ø\x0015µ*GáÎ Û)Ørà
ç°F¢è¾ë×\x0012ê\x001b\x0001î<DÁÆà\x0015wâXÛ\\x0004 ²$ÚnÙ\x0006(\x0012\x001b;ï§`ÛàõÊ­¬ª*[sÍ£½9Èº­\x0017âöºôs¸Mô\x0017Â×ê¼I;å¸æÔTòøþ¨½Ç:h¼	^ð&<VÈ\x0012y
7IË\x000b\x000fN¨EÜy÷;Û\K¼p-k\x0010ºF\x000f/\x001en1óNÝIÚ:Ûx!\x0016d\x001bMñ)/{¢uº¯³ð`ß<Ü&\x0016Ä\x000bÁ`
a\x0008PU§P\x0016=wñ`ØÛbt\x0006·7nÐ_pk4(}/\x0016ñ©\x0005·¢.;»¸N¡61¿\x0010S±³Ð#.ÑAÛê´3­=\x0011·ñÞþ÷fQ/½©®\x001eí\x001a3èv´BOÁ¶¥+Î;ÄÒCØz)Û×ª¹\x0008\x0013A\x001bÏí¯xîìz×ß¢³×Nvî<¦á6q ¿\x0010\x0007\x0002·GI@ÅsuÔ<	u¹SwV+Âm\x0018Ç_aú?ªK)ô;Zd²#}
·a\x001cqÈ1Y/\x0005\x001aãxÔ\x0000Öi¼7ã¯0N\x0005¬5*ö5-[ìít\x001f\x0000ÍÃmÊ\x000fþBý\x0001X­J\x0004Q=×«Ú\x0016ã¬\x0002ÚÕDóÌM(é
QÆ\x0014{ \x0018G=Eâ	ºnçæ"ñ¸
UÒ\x0015ª¬Õt½¬\x0007\x0015-*{=Û§p\x001bª¤+TÉ3\x001eJñ¸©\x0016ÒÉ]IyOÍê\x0014nÃt+Y5LúxÑij×\x0012\x001céóBØY·x
·­Ó_¡KÖ\x000eBñAÙ2¸çÀæÃóIØuè
ëPq¢\x0016¿\x000c¡·[IN÷\x0010¹<1­$C:ttø\x0011J\x0014I±â\x0016çíÎt3qÎÃmH®\x000e÷?IùÁ\x0013I$è«oT\x0015Ê\x0001,\x0019Î¡+¨Z\x00183kp/Ö&]?î`bh\x0012\x000cç+ÃuWQ\x0006Æ\x0012X4fáÊþn_Ãåyæ\x000esÂ%Î®\x0007á1j2ìP·¹¸£h|
·áps\x0010ny\x000e\x0002Gá\x000bn¯Å\x0007\x0017ò¼!\x0018ß\x001d®øn&\x001a\x0019de\x0000'çÛé¶rW&Æ&ÁxpÅp#µÞÈt\x000fÂ]z,N¬y\x0007ãNÂ\x0015wR+¥xÌ5íIÇEÔØ$N|\x001eÆÄ+þÄ%ÏÊ\x0000\x000bn_ø)cÃìµk\x0011&VMÈ®\x0016VÝÆ³FNK¤~ZÚr£åÛhÙÄ\x000e\x0008ÄÇð\x0011/ÁÇz\x0002{¥zßI½\x0003ýÐLlðð\x0018¾kÖ¯\x0011yW©ÝÇ¤[ÅÍÏs1\x0015ý·ï\x001f¡çG·\x0005µ\x0018äKa½¸%¼
u\x0002N4~p\x001fÜÅ£ÏCäè·V«\x0016.z­QÀj¾+Þvqwã*\x000eøíÇ÷þÏÃçx\x000fvÉ.\x0004Ü@Ïç=\x0005TE\x0012·ûRõÛ×¯\x001d\x0001kÀ8\x000c8\x0004~ån3G[\x000b`"÷aýãý\x001a°\x001f\x0005ì\x000bH\x0013zÌ,ÑÞ\x0002£6oç\x0018v\x000fõQÀ´\x0006L£Á\x0007×\x0000'îCõòV\x001cT:Îï\x0012ÐQÀq
8\x0002v¨\x001d1¡nGrõ3\x000e¼ïæ;ÏðÚåµs¼öx'
Í\x001d¢PcÞã£r5vÁ½òu
÷ÚÕÅR¬z¦á\x0006\x0008Ú`!¬¦°|óäwo~|óÃû·ïß\x001díã]T\x0005\x001a¹¹´©q\x0018µ4¸úÉ§O~÷ôÅÓ/^={õ|«W°ã\x001a;^Â\x000e<Ø¦ÛëH·ÁEÕ\x001a,öÖ\x001eÄî×Øý\x0015ìXj8«ûöÂÃØ)y}+v{ú\x0008'±Ó\x001a;]´{Ôê}®ï£ÐÚík\x001eÖÐÃ5³×©íÙw³\x0007èÙæ²ÔIìq=^4{_£\x0012tÙhÐÅ´§\x0003z\x0012wZãN×lNYe5|ÊºE|ïì-{r\x0004'±5ör	{®d¤
§rXxPUKAs}ãªáýº»xZæËÁ§\x0007/\x000bµg	ýÞúßØ-']"%Ì5^A}ÖD]K±·oú=QÖà
)Á5Vr%¨¦7«Cäi$]²{+ÜNb7¤\x0004×X)»ÞÊòp\x0012
 év´«Me%0¬\x0004×hµo.í²\x001c±o7í,vCKp2?,cOSÃ¨ÍLKÝLðà\x001a1¹LÝÕðà¶,ÇÒ»Uö6\x0004oÈ	®±SÏ\x001f´0ç¸g±CÊúÄ\x001cödÁNbÏ\x0006{¾føäz]+'eÖ¾
\x0019òÞúæØ
±Â5fM]·ÇÚÕ£\x0016=¹ÌsÀÑ&\x001d\x0017ý»\x000f½W¨-T_2¦ \x000f\x0016@;3(gÁ\x001b\x001f|$êÕÅê\x0004Afæ!ôÎÚ]íåØÍMÅ7\x0015 \x0017\x0012\x001d(±»
?ÎM÷Ð\x001cw¼vÜ£÷*º¼xÑ¸rõ×qtró$xobI)¬\x0011¼®\x0005_ú+@\x0002xÕ9r{}Íg±XÒ_%£Ci²@nªlf\x000f^·ù25\x000cöÆÓøKæW7»q4þ¢£\x0001Ôw~¢Ï±7·ìmÚ8	Þðª¿Ä«5ë£Þæ\x0017âC¼\x000ftyb©\x001eÌ]¥kw5×ðÑkKQì¾ô5Lµ;\x0003O×\x000e<·(=\x000c¤Ô}úûÐfB·%±kç=cêí\x0017,ª\x0013%eí¸s¹LüNâ÷½+ð0°ldÀÐú¹á\x0018»J×îjÊý¼sæ$ëk²G=szY±|¸fy»#IûDî®ÒSÔ¶\x0000Ú[¸w\x0012¼±|¸fùP¼Uð'ä\x0016ð^\x001fj&R£ññ\x000c\x0011ôé\x0000kXÙ
\x001d.ßÂ1{ä£qñ\x000cÔçú\x0010Ü`O¾\x001f=âõT¸ip·\x0007§7WËØYÊØ\x0018õÂÆ¾\\x001bqogØÙ0þ¦z.ü\x000fîlJ]%.s¡÷¤ïm4:tß\x0004ý%íþî¿¬Aeì\x001e§éUÔ¯®ø,»Ï\x0016ãM?ÉR_	]\x000fÑ\x0015ksBß\x0014íÑi©ö¶Rþ\x0005¼yô\x000b¸rþÕÂG½ºöð\:;¾F{:æï8|\x001e°ësçSCËzq¿tq¿ÿ\x001bº¸~ÿÏª\x001fÿ|éÜxUæ6	ìAû\x001f9+êõ+üï\x001eÁ¿æw~eøå÷o\x001f\x001d·KçÓÁNç×ÿÝ#ø\x000eÏ¯uß<:û×\þ¯{öáã3ñû±d)ü@Ør[ Ðu/4·\x001e\x0002îqÌ\x0000îbÐàk^Â={-êD¨+k
Â¦`áÈ\x0011úþÑ\x0011ºø;p}\x00142©\x000c&¡ô\x0017óÿüè\x0006_c/'Å9}YvåV»üððû?<2ÿ\x001fþ¶nð\x000fnð¥¥zÐî²ØGÜ\x0000{ªîwæ­ÏÿÝ#ó¿û0?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-08.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-08.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=yîÙÝë°Ff	\û!É,:\x001cB\x001dÞ¤z\x00155Æv\x0005¡\x001be\x0018#¾\x0010µZ¶9ÎÎ\x0011Ú\x00034L6\x001fKÓbN\x001bOù\x000e\x0000MÓ\x0018\x001cçdkå¢hË¦Sâ\x0017t°Xz¡ \x001c­¬sbqô`ì®á ÞèGÍûºQâ>/b¸ì5ÄE»44Vd&2¹SCn~üöü¶íäae$\x001c*À×¢\x000b\x001f\x000füî&^}\x0012Öð\x0016º=²ë+l:¼Í¤ºç¤ºmq\x0005\x001a%ÜÈ´\x0017ÉXÁôhuÑ#q@Ûg­xw\x0007¯\½µB"¿°m\x0007£QlâB¹OÝn¬rõsõÖV²Ð^¬]ÄE[öm¼ï½W¹zÏ¹ú\x0016^'´vÞ\x0016\x0005¸BÞÜA¥øjû
ÿ\x0015 ×Þ
v¢G"j\x0014YêÌ\x000f:M3mùv\x0011/Ú²LgÆ
³ToÙ4Eîj\x000b©ç¤ù¼_ûçkÓdsÝ\x0019\x001f\x0003\x0005dí¥à´}û*císSÀ¹ö»kíÉáÓ\x0018
\x0007ñ¥ÙFú¤¡ø%Ø¾çÈç\x000eÔÒâ\x0003&85_e\x001aÜ\x0010&_&	n7\x001e½ívØ\x000b²¾n³\x0016á°s©Õ·\x000bÛ·~·þ¶õï{lú\x001f5±é¡Ð/r!Dà+ªGï&±û´m÷ï`÷«Öõ ì¢¼Öã-^{6ÿ¯ýºq¸Æj{"6^þÿÌ½Û]Çq-ú+\x0008¾«£îGÞ¶CÒá±\x001d:&Ø\x0016Û\x0006\x0001¹eE(bÿÆ~ÝOÖwðOöÌkÍ\x001a£ªæj°ÑhÀPP ÆÊY÷LÚùEMÎÔáxüQélºñ\x000f¤ÚwÜk\x0004"qmH5mY³%|ü¡ly-y¡ÐJ#pÔ&©C$é|ü\x0016Q>Rir»¯ô¾r
ÃH¢:\x000cãÐ&[Ë\ÕY¶ÀWþùïÓìÅâ2æSôíû×óììÇÎ;\x001a
³rÛPu.\x001b©ØØ®íÝÕ?Wð­m¤yØ\x001d¶/ë(D½f\x0008\x001eDÏæbyÝç?lIÖÐ¨v*cµKtëÞ\x00132\x000f\x0012©ÄÊj[
Aqq8(ü9\x0001c	¥GÙ\x000ee4«;Cæ	¸;:¤É!kd®A\x000e-$Ç¸t\x0007OÈPw«{ª
1\x001d8\x0003G\x000bÅ\x0017q\x00002\x0004õRÄ`{nM/<§¢Õ¦/üª\x001300(qð#´MÇSAJ`Ó(»fÓ-\x00134p8?ÏÙsº¾\x000cã»bZ \x0019ÈÍ'ñ\x001bêe±_wu¢eë\x0006ê6\x0018ö\x000bÎ­\x00075Æòµ\x000eª
tí\x0013^@Lü¼Uã×	^Ï»Ñ·\x0016´.ôÅh¼¿Ygð\x001eÔñûQê\x001f¼hfæ~\\x0008Y3ô4ÔÂ
Srãrpö\x0019\x0019Ëâ\x0013\x000e-·1p\x0014wVßj\x0014W\x0003O;ú\x0010\x0019Ô©¬\x001b#Ó*ôþ\x0018VY<ø0\x0017\x000bÖÝs}§MOt\x0013Kn*§èÆÃt\x0013DNÓsåÜÄ8\<û\x000b\x001d<Ò\x0019ËØQ&f¯¥þºÈã}B=(Ë=!C·Ihà\x0006ñ¨b*\x0006n1	¹.³¨UðïoîÿüdC+=§\J0¹\x0000Ð\x001eS·xðg¼ÊEò­\x0016ÜâºÎÑ|ûÙ°ßÑÃe¤èÅ¡bLï
¬°¢¬ó[XñYîÓ\x0016õ> ©4N¬\x0013?
 ¢µX<ç
¯£^n\x001cXW´\x000b§
PS`\x001aB¡y+¸^DÊ'mRxhG\x001e{ÜÓ8\x000f$Ïf××[µë]~#ÿq}ÿä5\x0019ÕN/ÎçùoÎDü\x001aR~>fY\x000bÿèX|§Ó\x001dB/MJT Úâ\x0018~ùgÌ¹é÷ºUÝÿ\x000eÜ«±Ì©ó\x000c=ÍãRµÍÈÞÍc\x000b¾¦\x0001Ä¿½~\x0001+0±<
Jµ\x0006ÌÑBDPk@Ë+ÿÀÝBßÍc\x000f¾øÁÃé¯\x001eØgõÍÛû×oüñæÝ/nÞÿâw×wÿqófÞneýj»Õ¾Ô&h\x0013Ç\x001e\x0014rê^bº)åSðQ¿\x0003[ÝV:¤èçoº²Yk]é8^ÞÆ×~`Ç¯¯ïîVÞõ+6\x000cÙ0fO¦¼çÙ©6X\x001c ¡Ç´5r¹pýå'M[úq'ÏE\yø\x0011¾dÊ'ÿhr®-öú¹£ð7\x0002¦×ë¬sç¯Ðzê\x001cëÝ6%äù¯ÂÛ\x001e4ù¶\x0013\x001b.B'­¢Ð\x0019\x0011(6áÏÏq\x001em\x0002Èûþ«\x0010rîíÖr8<Ñ#êgF\x000ee¶'\x0001Ùwäâz- \x0017\x000f3,\x0004¸bO¤\x0000oknÂ\x0011p×@Ú¡fj\x0007\x000e#`Qke\x0018Ù/\x0006\x0002rìÈb\x0011¤\x0000a \x0011µã°\x000cg\x0011¦\x0003\x0000§\x000e¬%åp\x0016\x0015
ûÖdÛó\x0011rÃ « kîo\x0010Ñ\x0018\x0016cÊ\x0001yß\x0002\x0016|!x,<\x0007½<B³ñ¤èCiQ×z\¿z@ /
ó\x001c&éÐ}»@»^\x001a'Ð6`T =N\x000bºVtQ
Ð]R¼\x0013êçáj¼ÂÉ2òÅ´Gb»¤¸T{UGÄb(.ud¾³v1¡\x0013 »¬({Ë¥^¢ÁrG¡Ú[&z\x0015y\x0005ä.+Ú}\x0012\x0001YDÇ£°Èy1Ñ~+\x000e9\x0016Û¥ÅE¨ ÜÎ#3ãÉqä¹ì\x0004»´8Ñ£ÈÓ±`KÔ:\x0014\x0016\x00167W\x0000p\x0017\x0016çsO\x0005©SîCãp\x001aÎÎOå×b¯\x001c¢¥­öØ·2©Æ\x0003RäåÈ'ÛÙ&£~©Z\x001fóg±Z5\x001f`µ|''ÆO¥\x0006Ø¯à\x000b¬Çôüiö¾ÞÙç\x0005`\x000fÀëvÛ$\x001cÈ®Td;\x0017R\x0002ò.JIwß«Ö¼ r¥yÓìÓ\ï\x0008Èù«\x0007îó\x0012+,Tø\x000e¼«ðdM\x0005éoû\x0008=\x0001GFÖDõêÐ{\x001aJ =4\x0002\x000b´/TüiÔW"èS©ÜÑ\x0015vE+\x001a:¢-F\x000e\x001a¶\x0006sýìZ»Ê4<\x0012/\x0011\x0017Oêd¿¾Ìiq\x0012\x000eU¤Üª·®9Y\x0018ÌuJi{}wýýÜQòHk¹:Ö >¹¸eËY¾Á¦m\x0014Ñ\x0017«\x0002ZÁÅ`-§po\x001eoZ¶0>zs\x001b=\x0000CºXLhZÂ®á5\x0019\x0017|Y©\x001d9\x0012²ïÊÅ§U-!3°],n\x0004àDÀ®\x001fÖÀ¹ÄÀlÅ¹8ïm\x0004äþÆz\x001aD\x0018%Ð0³¨uôäÉiØµåY\x0007Ë3YZËú\x0013D¢8ÓiÈk;·\x001c\x0002r·<®3ëÖj)\x001a>Óz&ä­Ñ5^\x001fÞà^s(9\x0017¥n!ýÖ~µpw}{wûDÞ²ÆhPÑùØÖ°ã;[	\x0011\x0018_þËk\x0007ù\x0017#\x001fùG?\x00012RòùÆÅñó®§å\x0013Ê?0ÏEíGãÌcËY²·	È]NS@7ÓeÅá²â<ü
0ARîm\x0014ê±d}yÿ<k\æ`1 w9Ê¦ôªEau®\x0011ä2³zt«çÿ\x000cÝÿGCÏ\x001eå%\x000b\x0002-Æ é\x001aK\x0001\x0018Ö\x0011ß<ô©ÐzágYÞðHª\x0017/¿dÿ\x001fÞÞ¾{\x001aÓ_õ\x001b±g=J¦ÓrMçA'Ú+§Ï"÷.=¼Ëo;¬ñÝ¯¦×HlÏsÁ·®ÒÔ¹ö<\x001f<ü<§W¥3ôð¼ ¦G¯BdÔÐõêXÅíÂlµo__¿z ?úØ;\x001e#>>vã®Ú¾\x001fzókø²/9|òaÎ\x0010<z\x001eúÊFþ|·µ5\x001c!wõ \x000e@_\x0017 Ñ¿\x001b¢Î\x001c\x001eBiu \x0017ú}®îá¼y3ç¿\x001eù;ÇÁ&ß"'U¤­Vh¸&\x0014á	\x000ffÄC/)7  ý´%j3gUÚæ¿ÏR<ÔÀ\x0008¬øÙ\x00108Ö!)¶Á
§æ\x0002U@îæ{É\x000ec\x00036F2ýwÅ:wä6\x0004Öù?þéúÝ»­ùë÷7×÷OgüÍ	º¹½/6i¥'6Ú~??=¹º\x0008°ÁÏ5f¢§ùþýí\x001f(\x000e'úÄ²>IÖíB¬=Ý¡³ª\x000e¾_øk<Zá1û>HP»"\x000eÑÏ/$ÇÉ,6à\x00022ºá\x0005\x0015u\x0010+<h9Ø*^_\x001d.9>,ÿíõoîÞÞþå\x0017×÷ùÅ×oÐÞp0«DùY'x£bºNð\x0005òN9ìÛG»5a¦Ü=M¹¤ç\x0011ir\x001eÁ\x0007ñò\x0014Õ_Ì|½»º(ô£gVY}ñ­%¤~N¹Ï\x0001sJ¶u´Y}þðO3+?¨o¶£âÂZ4<ÙoYËñÁ\x001cÉEg	â\x001boçu£¼WoiÔ··>9_ qHÇ:b»b\x000bdÏëF\x0001Ùw#ôª\x000bÍµ\x0010gÈN6+÷\x0018ÃÎòâ\x0011õn$!¹P3^®¦Ð\x0003+ï¨\x001fX@dU&,î³HrILr´³ã
È	hv½SCiÎØ¨®}û8-Si6s\x000f\x0008 çNsI\x0010lòÅ&\x001cì"\x0017h|`ÛXàr\:ÍÞÀ#ç\x000b4ÃèðÀì\x001bÁõ\x0008¶v3áð­&8ÎS\x001eÂhE÷íÐ{^ÖëÌêÞï-BnÉ5\x0013¢]!1±ÁÄÙ«\x0007h×¡uÀJéÐ:E #yõ\x0002Ð$Ð\x001e	Jo\©ÚÞèác¾²$%°E^\x0016ARJ\x0005SÔW1/«oc¢£¶[Ãí¤ôª(B?h}\x0006¿\x000b³ÇvÐGb»¤Xãz9©ÐÌ­Ù"&4\x000e@\x001f´í D¥\x0003¨UD\x0005h.Ô¦Óôd\x001b\x0017£p\x0001¸KÕ¿\x00004ç½Ç¹ïRm\x0001{{$,û0\x0000Á
¹\x001eß\x0006z¼A\x001aÛ¤\x001cÝIîHX\\x0017\x0016ù(Þ¢ç¯fo#\x001dø\x0016u\x0007\x0000Èö£>\x0012C×ÅÐVß\x001bij3ìîÐ\#=zªLuGb¸ïL\x0014ªsíc\x0013ñÜ\x0015"ÛLaLaÙmÆî\x0018º\x0000DÃ\x0000;%ºb6ºS\x001aSn\x00035ÄÐE\x0010pD¦4gô\x0008UÀ\x0007Î­OÏ\x001dÉ¡ërèt\x001f±íD;\x0003ý´EÜ.u~»Ä#9t¹\x001fj9\x001c\x0004 âb3\x001fõ6<Ö\x001dI¢ëè\½@t½rh
ûâèÐZ-Ý$º.:?#[q%P¹=½,ämB¥?Dß%Q\x0008_hs%êZ2SÝâýþH\x0014}\x0017E«\x0013÷A3©\x0011Ï¸«¼/õGè»$j-\x0001þð\x0001{"hÏÐ¡µù#Iô]\x0012ÅGé½>*/a\x0017ÃÖ®k[þH\x0012}D1®\x00008\x0007,jMC,¥?DôÃª!qÑ0$Ù±}ç¶}2þH\x0010}úXäÐg¸Â
,\x001dZ¡B¤+Ìü\x0004Ä­*óH\x000e=Èaq\x001c\x000b&ù&ñêÈ\x00163)ô ú
çá¡®/È¿×
9à@\x0006\x0019ß*\x0006Ã \x0006\x0010Äúh&=k«{\x0014íWZñM8\x0012ÄÐ\x0005QçÀbª´\x0010R\x001a±ÊómsV8\x0012ÐÅkØ\x001fÄ¦ZQÀ#\x0015Ö
\x0019m0I8ÐeE\x000b&-<µrìÈ\x001cÑ\x0019VJµù\x0015áHVB\x0015\x000c¾Ö\x0005ì_Õ\x0015T(4­\x0014%tañ¸\x0016S MÀÑy:¤0\x000cç¼m;<béÐYZ+
´¼â\x0014i1X>êmðÀ\x0011ßÅÎwZOZjçpÊ´@\x0017ÊéËVk|¤¦cWÓ"Ã}\x001cü5OZµÈeÜoCø§É/¨ \x001aId&÷5\x0010*èÔÏ«nYÎ·ÀÄw\x0007àÆõ©5Uì\x000c8Í©\x000cN\x001føðêð%Øç¨²xª¢l"ÊÙÑÐleC?¢]+¶>Rk\x000bÑ'Øk@ÔÀÎè}U\x001dø*ÐÚ0ø¹Í\x0016qoOým?uuÂ^×Q<OÅ¼l\x0000GÿøÅhÊ\x0017\x0003ËÐF¶ý\x001a§Ï\x001bªÐÐf~¤²æ!°	\x0018Ym¹1CÞ§ýTï^üêîæÝ¹óû±±ÊXØ hËÞO¶úé\x000eg\x001b&ûÌ±J×öe}@°s§rÃ\x0015\x0016¡\x0008ùÑ3ï;\x0013ø\x0015My^ \x0000È\x00189\x001cy\x001f\x000bñ\x001dÌû4t\x0006dpþÈºWï\x000eK¶5Ü5 û4w{\x00002¸h>ôIJsäh¥Èê`'y# \x001be`\x0005*0CAaq£Ê {[SÆÂÄÊ\x0014¢S\x00064PÏßì T/.\x000c\x0006VHsÙM\x0007¶à¬9û¢T\x001cDÑ2EÑ\x0004:bDJÌÂÄ\x0001W\x0006§¡ní®Ðm¯Õ\x0008]T\x001dM¡\x001c\x000fBRBRêê`»\x0018Y£ëg=Aû-vt\x00109KØ\x0014{ùoØ\ñÍZÅwò\x0010ßqÒ\x000e`SxfimbaèmïâÑ-B\x0010FT,+4ÇL ¹ÜÓ´Á³þ6\x000býýËû×O§¾ÅäL·¡\x001b\x0016\x0006\x0003Ü:- ?{ªI\x001cÌ¸Pß³5£= ÿâ§¯ÐqHV\x0018ÜÌ­}?iT*ä\x001c{¨ÆC\\x000b]=®Ï\x0018?,Ùç÷Sû\x0007*XwÕ°Npið·\x0019\x000bérÃ+g5ÐHÏ\x0006µ\x000fÕÙyq\x0001 W®\x001eÓ©§ôdÐà\x0016-<xåÜøÊé.Z0&Ì\x0010Z·\x000f#GÎ±h¡\x0007Ky³êh=¾Ûi¥iÜ¸C4Íon%JÓ±Ä\x0006·©µ;H\x0015;¯ë5Ý\x0017«h!EsDýÅ\x000f_]À4TíÝßËÇÞ¼¿URæ\x0012Ä\x001aì\x0012[v\x0003O\x000c\x000f\x0007ÚFçÎg¿\x0014ÝkR¶ã\x001a­uñ{1æ%fCÀk°1°q³Í×µK¶11@Õ\x0016¨#z¸`W×iz\x0006e£#U#çL\x001bK8õ¶¦¹0
w*~÷âw7w·ïqt}$çõÍy0\x000eI¥ÊÄ]Uz\x0017|3,©8"ÿÒ¯î`lB;øÛ×¯oî_?ìzç\x0017"í¦¤® »±µt=ó\x0015èvõ\x000fR u°Ôlá¼¢Æï\x001d}yf9mªó\x001cû=!CÆ²°èÀÙJÈì<¸Ôº#ç\x0000­ãN1EväÂ«kE\x0012[9çÝº\Åq?×¶F"9¡=¤`²\x001f£0=èZ¦öÍ\x000f×w?*_>\x0015SzË[M¾§\x0012ÕÝè°/÷A±fxPT¦zbÐ\x0017ui){7D­\x0007µjfä÷Z±
®èkâÊ!¶grk¶\x0001\x0019ÜN\x0013úbC-Á\x0014ððÜ±¯i÷1j¾z Ôó\x001f®§¢ÞÆ+aUßyàuròùu6ÇThm.r§,kj8qy§f/ïÜiøù5Z¨Uù_¾¹yÿ×Û·_Ís2_üAEe~DmX	Kº,,µòä~|»fÓ~<zX¼®}ï'Ùîd[¥Éeù8\x001f\x0011IHðº\x001dl/`Tª\x0003ö÷Õ*,ñ\x0007·
0î\x0018Û1víØÖ7ã\x0014°_üVué¡}gE·½ÉWÉv\x0018ok24_Èn	p\x001d:Ù	¦\x0012+Ù4\x0019Rs\x001292Ý~\x001e\x001cJØ±Óís+ô\x0002ºSA\x0019ª~à¯ù-#hÎÐçä	´§\x000c\x0015ÏJT»y[\x001f!çL¯P¢=Ô\x0013ÈY;Z\x0004¨4Ï+¤\x0008ºth¯,\x001f5Ñhù´Ñ ÜäQ\x0013týê\x0001y¼ Ése'BïµÚãzmçF¶CªsÉLõ¶ûX ­Ã\x0006Ot;lblG\x0006Y4\x0012v\x0017H\x000ejáH4AÂî­\x001b8Û,
G	\x001cD2Ã¼æpºKO±ºNù±LÚ\x0000§RXMÕcIÃ±9 NØ ÅôÉ\x001e'ÂéÈ#-DPÂí\@Jà]*+ÎöÐ#·XÆ]kpqÐ¯e\x0011¯'p\x0010Ì
õ©òv¨M|ªvuäÇ¢i»hV\x0003m\x001b³d:ò2ªØ6WÆ\x001e\x000b§­\x0000\x000e%Ì\x001bå¥ä2P\x001eçZR\x0004ß«Iu\x000eëYãíÌ
\x001eKtn ¼MuÇòéº|ján\x000c¤Á#¾\x000e\x0014²üÄ¹ À»ÖúÔ´òDÜÝp¡ÛÒ£c\x0001uÀmfÊ+ÛAæÊO|(n±u\x0007èZ\x0018ú´ÙúX%ZPÕF|ìµÝÓ\x0011º1Ì,[¦ÎwÁØË#\x0004^þ+lK »\x0004^0!çÒÚ\x000bu5\x0003ü5pc\x001c¬ ñmâ@ýÆc\x00013$\x0014\x001a=.ÄÑÄ)Ã²T\x001f<ú¢{§\x0012k2|õÄ|#©ÒØXS6\x0017£ðw<ÿíT"ÄÚ¿£VÖÈ\x0001ó¾×­Ä¿¿t×ïá G95`©¡w\x0003£q¨ôò/·1¤ÿìÌ/ÿ,6=\x0010}"GÆÄAÁæ|þ
¢\x0011\x000bÛ{îY<\x0019/\x0007þ §>£ÑÑY­È;\x00113ãb¶ûÑLóÄPÂîz9Í&\x0002ñ¥Éq0\x0011\x0016+\x0008Û\x00036i·\x0012
\x001be¦0Ù~\x001e\x001aJÈÝhJÙ_ñ5¿n(w·\x0013=*|î
?¹Ú»Ó\x0014;bÓ±`ñ@\x0016ca\x0008»L\x0007ìws\x0017\x000c@ç%{´\x0000»ÛK1CWçf¢Â^»ZÄ\x0000¶ÌÑ¯<\x000e\x000e\x001eÇcÁ¹\x001bÜ\x0002\x0005'cl\x0002÷y\x0005~Ì`¹?òÈ'ë\x001aÀÓG\x001f_(\x0018À\x0002\x001fÕù¿ýëMøî/\x0014ÆmãáoÞ½øv}¤2·ßwëQ\x0018HáG1Í¶uÏ ÍÛ$º²	ç#bGKª/~ñtøþû7o¯!'û[íñ¾}³+ö¨/<þ*´\x0003uµôÞX¤6jsã\x0011
-ËôÐ#º\x001dÎð&\x001fz\x0006V¨öáXòWY\x0004 ®¢\x0000
o¨Éà8\x0015Ý\x000cEqrÔÐ¬Ø~»MØý
jh\x0001Ùa[PÔ±S¥GT.gnð&ì®ÀbÉ`WèÈ,Üs.Ø¶JZ<£\x001d\x0001\x001bý¦bSÅROÅ.tÞÉ-æo\x0013vbºlWìêÕ+
È\x0019+v8]O\x001f£\x0014í8r$Ù­óØ ¯¯ÿzs»ÚjõH\x0001ÕFëNKª[Íøö\x001dANß÷`¬¦Íþ\x000e\x0011um·ÈC":e´fÛôÈfqÊ08]Ô~äï5ó0(@\x0006+À\x0004Èî%\x000e¨Â	Q«µs13 ú¥wäÃ\x001d9,²§e	Þþà£ÀG\x0016ÿ¥Á©:¿}ûþöÝ»\x001foÞ¼ñÍÛ÷mÒõý¹¹ûñ©\:WiOÉç5Q\x001a±\x000e}Ww,NF?G\x001fi^^a¦\x0006b\x001f0®]G\x0005³óòµÅÉ)Î¥û\x000cap×\x0012\x0018g`\x001e\x0010«ÇèH5æS³Í\x00110À]êÍ³l\x0012§\x001c´ÎC \x0000\x0019âß\x001eã¥r\x0018\x0003<ÞÔá0üê\x0011Ú!ú½äK<µxvÜD\x0014W¤Ø`3V£û\x001cË\	È\x0010õ¶µ\x0017Êèd¸Äþ¡+\x001cÂI¹
©\x0018mþ\x001d\x0019²Q:¾\x001a8Ã\x0018ì#VÙõÔU\x0013tÔ\x000cÉ(\x0003c\x0008äKKÅI{èâ\x0000©¼ ËtÔ\x0019\x001aQÞ@\NX0s(ÝU¶}²Ý \x0004\x0005óE\x000e\x001c7\x000cv0*t&\x000f(¶{\x001e14&t\l¥\bÆ\x0001\x0018ïK«Î\x000cízO®\x000eÏ\x000bXDXæ\x000bµN¶\x0019&G<
î¦B|+4I¡+y0|ZF{r7whL\x0016²2Åx£\x0008cý´Q2é\x000b¶(\x0000þöî§¿?i\x0012§ðl5¡\x0007"¦[z¦'Æò\x0001þ\x001eÏèíä\x0008\x0004g¬\x001fËñl[·È\x0011,x:Ú
¾kN8è@YØmqKkêì?àÉÚ9ÃÆy/ÀHµvwÿ÷ýoáÁ§
p´BI ÂÄórÄ²$\x001døÇÑ\x000eÎ©Qø0ã8UÝ^y\x0018³ØHü8ÚÌ	Ê´²lv\>üGWYUÎÑØâé\x0018]q+\x001f{Gö_á!C\x0002^ôµPÌ\x0019¦\x0018ç­×\x000cå6±^U:HÀ%0pk®>\x0001G\x0000v½\x000bO÷B%ÎëÛÌÁ\x000c\x0017Â*F½#÷w k{c×ubl4GNSÅ¶sirjÎÈ\x0019h\x0015\x0003º%«ÇÌaÜªÔf\x0007.@2l¤×Ãp¸\x0019µ\x000eã·ô0ÚPÑ´Ù+AÛÂÚNHfmWï86gh0mô`=$~Å¤\x000c|ÎåÄÅÎ\x0015F	1MÑ
W8\x0010½Ø\x0005¸H\x000e 'Îâ\x000c\x000c%M&·
L¦\x001d:\x0010túK-â+\x001cÃ.&¨\x00012JJèõór\x0018n\x001b\x0010\x0008ÁÆ\x0015gle2íÐÎp¦Mh@9£5ò\x001d9uYí_|1V¶Ø\æ4»æ\x0015\x001cß¡Ùª8Ú!G+\x0014ïÄ\x000c#CÛÚªÒ¦â\x001dÙ\x0011r­ q$ºð\x001d
qGçñ"ê~5o\x0006hvåäi%/Gìá\x0012ACÑ¢¦þ\x000cK8ûµòÌ4ªnÑ\x0015¦\x001a$<¤K\x0007\x001dW\x0013²:®\x001f®\x0010NÃçñ4ØÉ·!µ7öè\x000e=+\x000fHÄ%ï\x0014öð®è¾Ò¿MÓ¦\x0000zP\x001e á\x0001·í´W6±7à£\x001b¢pµ\x0004ºOãè¸ØL{ÔµÕ±ESnÐ\x0017zf!\x0007¤ëw\x000c\x0013mø8ÌjºR\x000e4\x001e&Ç8i\x000f®â\x0012×¶3G\x0018\x001c\x001d¾ó0Ö\x0015³^bþ0q\x001bûst\x0001.QÿBg½(\x000bUAÚdé¬MólÃÑ-\x0006¸ÅÑpÔX0ËadyÑ.¿M³\x0000\x001anQgÐ÷[\x000cq¬ËÀºä¤vþ6M*êÀ\x0011îÐÛÞÜ¡ë\x0017ih\x0016|8FN©ãÑ\x001dF¸CûüÅ¶$qÐÓ.SøWE
}t1\x0010Õ`áùºm\x001d\x0001ª-CoÓÙâÑ%F¼Ä\x0007\x0012å (9ÏØúãÑ%Æò±Ð«\x0002³nçQY\x001a¨%­çGë&±Míw\x001b.üB\x0001\x000c\x00065\x0000ÙÈaÙÉ«UÄÁáçÕ¯oÿüvµØùQ|^|®¹Ê=c%¦4¼iEN½©ñgé1±\x000forÞNhôuCîcRcÖ\x0018yeMËevYµ\x0003½\x0003uËÞ\x0001ðP8Ã<-\x001c=©Ù\x0002\x0014\x000bßPDÆ\x00048´Øä$ûg`Ôß\x0005²ë:o\x0007\x0017j6\x000bm¶®9_\x0015g_\x0017N"Ñ×æËpMã\x00164Ê\x00196Ñ[fº²Òõ]èJnR°néèÑz÷`\x0008ëàp7\x0000'¾¼{\x0005=\x00153ÚgA7»pC\x0008ó\x00020@®D0ðD¥ùÍ\x0016á3Î§
Û\x0003dòr-Æ)j
­¢CW\x00163\x0000\x001ad/¹>þJ7\x0005U\x001c¥Ð\x001c\x0002ÑQEKG÷\x000cÍþFo\x000fÐmü¬P²N\x000cì¸h¨fp\x0018áU\x0017k¸3ÚÍc<\x0012\x0012ts+ì"Ö\x000b½]ÂeaÙêÌ¥{NLu':9\x0016l7Ô_G±\x001fnî\x0019\x0019\x0004%'(ã0ú\x0000Ð1[v ÅÜ\L
\x0007äòÑÇq$,ÐÞséÛÃ´øÄ²ã\x001c·\x001aÄ­©ðHXÐ®°paK±\x0012ÍÑr²+¬[;vdû±Ç1ûægh\x0015m\x0002¢Å¯#1tó*yË²Nm\x001d;4¤m\x0000³©xÝ\x0005¯ +Üë¢hK·ÿ\x000c
X+\x0016'ù\x0018qu¨\x001e\x0008»_:\x0004sÕ1²C´$Î\x001134¶Aº+ º\x000eÅÃ\x001a>¦óØ\x000cÕ9 pF.¼ã\x0006q\x0018
\x001f\x0006g\x0015Kn#ÝæÂ	\x0017\x0003
ÅBº¨¨WÇ"\x001e\x000c)ºÍT>à;ý\x0003ä;\x000bù[\x001d+JjÉ1ÛmP·nÐùÎb5_°C³ÛÄF8mäv]Xëû[ËÖ:\x000eVm­ù\x0010f\x0019úYk(\x0007­ ]_ó/¬éøÂ%ÈóßÜß½¿ùnµàð±=¬ãmo:÷ü
IüL\x0015l©ÅW\x001fö\x0007òtÍmÊÓö]x+9\x001d\X;\x0004yÌ»¶\x001d9]äß O\x001bÙCG\x0007\x0001*hX\x0003ÕBºï	ÝÐ\x001d\x001aRSU³~=\x0001c	ïÃí\opkw+pbãº.?wd¬SHX!c&Í]8»\x0011W\x001b~\x0000\x0019joLEg®Ìé
y\x0013\x0006[uY!³#W¢¹#	5ªcmEÜüÿ\x0015¼AcKõ£npaQ¡ÖÄ\x001aì÷ªÕ\x000fDs¨/´ÙK\x0005«Ð¬`Åõê=æÅêú\x0008êuìÔÅf¹»ö;\x000b
·ÁÉM\x0002¾Ñ^ðÀ¤Óy²\x0015f^øÌ?°TM\x0017tÚB·ºqOÛýon¼yûÓ?Y#Ü6?
µJ« 7­1ôgR¯\x001fVÃ¯'4¨W¨à!V\x0006¾qßMùü°T¯n·èâ7\x0007ùÇPp¨Q«äâ°ç±#sÝ$\x000eÐ\x0000~\x0012Æöº\x0018Vu;2ÖM¾ÊÁ\q©çP\x0002à[_ò¬bÝ\x0018\x0019)Á³ô\x0010öfäm¢Ülfº1QÁx¹¶5z¦«ëÝiÝïJ0ÏwÈi+Í7QíH?ÆÞû°\x0008Úeùþëk]üûêf1ê±5gT>´·`·~²1ø%:\x001b:<OkÓA\x0001ÿZÊì®Ûè4;QÃ\x0014Rãí{òooY9³`G{"U,!Tßf1{¨'å.v4'\x000eùâ\x0015-«RNÈ\x0010Ðø@²\x0006\x0005\x000f{_\x0005Øm%x«¿]=rZ?ÓÔæ¡4ÅäJ¹¬`gNG\x000bÿ\x000fooo^|óöÇ\x001fïß\·>¾§/5õZÚ½Ð­$rtìLþ¬ì>×ÍÖ³êÉLÏ\x0011
<Ò]gÃs´*ÖÞ¹b\x0016"ÈZºí.h1]H½.;:Yu40\x001esl	n¬z\x001e¦äeSé\x000c4W
O\x0017qõ©ÐF£a$VY\x0007ÆNÐ\x0010\x0018S\x0007\x0019:Vôt(\x001dâë\x0010Q7q\x001e> ´\x0002¯÷\x0019jÿðøj\x0012éc|, iS¯Nß!*\x0001ÊQÛdgbòµK;"É+ÒBÈ/ê\x0005Sý4 kÁebE\x0017°@«æ¹£d°tFÿº\x0002®L^æF<\x0011]ßÚô½\x001aë5
Ú¡q\x0014T\x0000ÿ³ASìÆèVÐó#wæAP4\x001e«r²Ä{î"=\x0018\x0004µ#\x000fc xì\x0000=~=¾ê=.iâIdó&¿\x000c´¡yÒBZ.JÚZ¡A¡´)J	.q1Ei8Pû\x0019\x001a\x0006úèfô@TSî(8nY\x0011ÏÂ.#ËghDTxÀ^ Qf(S\x0016µù·Õ ¢\x0013ôG!b
ë¿z`2ç7oï_Í9ýrñúYÞV\x0002õ6ÝuM²OXiÒG4bÐ\x000f×£ÙÇ=ï4<b0gL\x0007súoþ+Üþ\x0011\x0006sª\x001bßv­¿{·5¨|óÃõ^\x0016¿eë/¿,!Fª'&µößíBñ=Þ+^	×Û7ªWåÁ!\x0008çc"_A(Î°÷ÔG§µu¾ÖÐ×ï?O¢$ìØ±Å[\x0008¡F¤ª!&²½õ$[d>ÆÎÍtªT±QI\x000bï\x0005?;\x000c]>îá±Eðý¹\x0015ð\x0004{\x0006\x0005<Ó\x000699ð\x0019B¸õaÎ\x00138Ü¦î\x0018@Ê\x001dz~\x0002^ñ-WÊÓbZ\x001fÃ±GnN¿\x0005àèWDí [X\x0008îÌÇù ù^*]ö4\x0011¼÷÷A(­±AJ|ÛÑ³}x\x000cWy¿Ü \x001d\x0000¶<
\x0008m?ñå`Þv@\x0014Ì·Ð.$g\x0016äss%Aò1Îý<Ü\x000c¯³¡lG\x000e\x0019_L¡kAöa\x001e\x000e\x0005È]±x­¥Í\x001dÙ62|Gö5ò\x0015¹¸R,;rW+ì\x0007m¾"\Ï\x0004m4Ü\x0018+ÀsX²Gí¦¶²GB·ON$äÊ¬5­ëSì\x0004[\x0004¾½yûþæÅ¢
îì]%\x001fKª»\x0011\x0010\÷´½òB«£ùôì\x001d¬\x000fÆª·£\x0019Ø;\x0005X\x001aà%t£brÒÊÿÆ)T
À]Õ&\x001d/Úqu>/2wCÞ\x0006F\x001e\x0001w±IÚ\x0006\x0007È.cDII&Þ\x000euK©\x001f\x0001w©Ñ¶©~{òz`#À)òYlË(Ó\x0011rÚµå\x0006Ô^Í\x0016\x0005âÉ¼¹L³<»<ÊëG!¯~F©Æv±`Æ÷lG.p\x001aNC\x000cZèi×Ó°Ï¹qF=B®_= %\x0017%le>¡ÁxÐ¢qxÁ±\x0012ì\x000csf5@îråÎ2@RÑr¨ÔÖ)nÓbú\x001b@;¸ÃØ\x000få¤\x000bM'Õ;ôä:ÄÍn°G²b»¬´\x0012Ø­\x0006\x000cB2ß®\x00146\x001dC'Zkè+\x001cuÂ0\x001e5[RjpÎQ\x0000îrXNå\x0008g¢åõÁòBuå[L¹
M´GhA\x0010CéÝBµ£\x0019ÖBu\x001c\x0018¤E @wI,9#´ÕI¿ ÉzK·¨e+Órî¢¨]ÈU	ã8\x0005¡:³I\x001ck[ìbdÑÖ=ëÉf=CÅëVz¦:\x0017ì&Ðª\x0004:tª19\x0012\x0018ç>\x0016ù«]çj¶Q@\*¦å\x00048\x0005Fí\x000eÝÑ\x001dº\x0002ì\x0001½\x0015êù\x0016ìÑ\x0012öp,ä¢~¦Mù[üÒ´ÉT\x0003©]ãþ(ûøPF-Tù\x000c¦kUf\x001f`ÚÁ´ÑÉn\x0001M\x0013±õs\x0003ùcÑºyó\x000c w\x0006ê\#r¼ByÌ\x0014¶Uyë\x0000×\x0003Å\x0010´U\x000b¤òKc¥êÌ<\x0016\x0003PìÀ7
5eÒN:^k°@òÕT\x0006«I\x0019coVÛÆc¡Ò<X ¾?\x0017Êº\x000cV<|ðäm°\x000c]i\x001eìmÌBWÁj\x00129ï½eúâfÌ¦*ÍlÆæ\x0018 \x0017@®½âF\x001f\x0018Ï\x001eÐÌÈ¹Ì=þ\\x0001Ù¶2ÚýÁµlfÚ¥§qd4Áh¥à\x001b`Ô¾ÎD³¤\x0016Ì*Á\x0001Ð¶ðÞ¿X=\x0013Íl·í¤^\x0019 e0@´Ë\x0015C&c²­QÍÊ,EI\x0019@\x0003KË\x0012á)×1ëÄÒÝÐ\x0014·ÉHG<
\x0006ê$à\x000fÀÉn\x0011Õd©
Þ,Ô#¦\x0006\x0003DÅÞ?ª×mþ\x000b¢OmþGLm©aÆÊ¨ê\x0010{j³6VFB\x0019\x0004.ð¬hó¹¿\x0000­CÊæ\x000c\x0007@[:\x000fß©6H¶C¸¬¥{VÆG\x0019\x000fÕw\x001dÕ	Gg>\x000b>f¹¿Åz\x0008@öÄv\x0005tG¥<}£m±í]S\x0006»Få°vÞpÉà\x001cr¥:ëÏ9Û\x0003Ð(,\x00191«\x000b§\x001có\x001bcÑG\x0000Ðéï¼µW¬<Ixñ\x001bo\x001cÉCY)$f\x0010ï¼Aw¤¤]¥Ã\x0000­}×¡íJlQ#vö Ñ¿~xÁmf}W7è#ÆóÈxlS]\x001d2¨A\x0006\x001bò\x0011sxd\x000eÕ9ÚÔ4\x0014\x0000³\x0005sã
t\x001eoÐ@X6ê4ÆÀè8/s\x000f²Eµ\x0012Å"#î¼C©\x0006Û#Ud
ûs:\x0017xa°O«ç_üÓÍû\x001fn^?Í^"_»|gÞC8Ú]aájëÎ\x0006Ý\x0004³Øaºàò<ÚìX¯"_9A#\x000e\x0018©×\x0012\x000e¢í'd`rSÐ\x0014ñÜï$ÈCÀ¢ÖJµ`ò<ZÀP«´q¢C\x00052O%Ú¹õ\x0017\x0013\x0019®-k_\x001c\x0003ûy\x001c\x0000£ðti×Ù«þ*q±\x0001PËG»Ðªy4}>¹+»7\x000fv¯ÎvñLp Zù\x001d\x0010]}d÷æÉîÍ½X.WdåùÈ,ìb\x001c CX}-Ó\x0017õÁEÇÞ©^
¡)lÓB¥®¬Þ<Ýpí"\x0017ltÐà©\x001b.ñÀæÍÍtQ\x0014\x001d3ÉtiyÎGÌ\x000c6o1l\x000f!¹pè´0sê\x000ebny¹éxGâèÂç\r\x0018YúÈÎcÌ-S}E£\x0002àÔÕ¨^\x0014\x000c\x00014\x0004À5d\x0000Ð>ã(?½Ãè£[\x001elS\x0018ä..\x0007ò¶K,áYwä,\x001eÚ¹Oå×?ýýÍO¿»~ýâ·7¯^ßÜ½z77«Ç\x0007\x00149kÍùÍME§´ìÇtBZ}\x000cw\x0008\x001f\x0000äf\x0015RÀÂ¥$O\x000eMv. B±5µFµªâf\x0015AÖÊïÝéHI{W@ÔAGft:<jýs³ k\x0004<\x0003ÍÔù*4{,³Ws]ÇÉ¸YEÃÛ¶w\x0012«%.ÏÁ\x0010²\x000e\x0015Ga\x0002rì4'Ûg	ÍÚPæhø7¯c¡]¹\x000fFi.}ú´ÒÈfÊÁ\x0006¦yk®[¨W\x0010"4gX)È&Q-zh.îÀVà\x000e\x001b¡¹ÔÞn$b2'åà(3åNÃ¿\x0016Ú\x0008Í¥à9'KSRæR7¶rÌÁÀSB4\x001cn ¢ D'lô\x000fZBåhù¬\x0003§\x0008´ÙÐ3Õ:iß¬uêÌ){t$Ýb8ÒH\x0017µÙAzqîr¨Ë\x0012^)\x0006Å\x0016\x000e,á\x001bÕGØTpÛOmÕ!2µXÝ¨N~1j\x0013 »$fõ\x0015;Ñ!ãÜ ðèzdçð\x0008\x0012!ºÂ¸[!ºxª\x0015Êú"´sy1j\x0013 »(j
í\x0002´5i¤ªKw\x001aX¼²GxRÎæ¯}zl«Àg§S\x0008ºôÊfày\x001e,d`.Ã#ýáÛðr@Þ)®e<tC^¤³Î#¥gY`6¯k\x0015ÑâÉ\x0018ªJ\x001f´¦úfªnÊünú~n±Ç.0s4\x0008	L¶\x000c\x001a$\x001d"öÈdÐ¨§¡$\x001d:
²·îû£kì¡§¤=¸ @\x001cM'\x0017ä\x0019¹´óXE"G¶ùñÅ¹$åÊu¦¶RUè)rè©©=x\x0015ó¨"\x0017ÀêÔÛt\x0010{\x001c{J%a\2éÓJTûL\x0002c·9t\x001en1×«þ\x000cäS\x0006\x000c´\x001e_¢
mL8ºÄ\x0000X`¢è&Ç\x0005¤9Òêa
l7	G·\x0018à\x0016u*h§ºD"\x000b¤u¢GËY\x001e]aèWXu_<àêB R§¥TV§©M\x0008=ºÂ\x0001ÚA4U Ù\x0007ËqÐLÎo#%®0ô+¬¶à#Put\x001d¾/ÉR\x0011;ïü<ºÃh\x0001\x001aª/SÍ\($È,-ÞlÈGW\x0018=\x0013Ý\x000bûLF\x001bz\x001e.1Â%BxgèZ¨*Z 3Cm\x001e]bK\x0014\x001eÞ_ÜÆ1Ñ8ÚmlýÑ\x001dÆJ\x0007\x0001ú´ú\x0007ï$Ü§V\x001bâ2¼|âk\x000c/Ì`I ¨ÌïydÚÝ6
8L³\x001f»é\x0007t²!x_UÛî
\x0007\x0006ßBïÓ¦h´Þù\x0003LlUÒRà8<eô\x0005¦4c8ø\x000b_àù\x0017J\iÒ^[>BLØÝ¦áËzã³,
gôóåi\x0011yõ§ÈÃïÞÞ¿¾}óD!þX¸ÀÜFÛ[\x000e2ÛÓ1>a=}áÁbÛá\x0011~\x000f£\x000f´ùR.\x000c{£9Öu¼!q¼!F]6\x0001!\x0012Fy=µ\x0001\x00089·Y0\x000bíÆÜs`\x0011\x0006íõÊ\x0018VK´\x0003r\x001doH\x001coÓH´\x000f¹\x00182cµØ">µ¾þÞMcVB\x001eÏ}(¸ö\x0000\x000cõ"É8FÞ\x001a\x0016^N\x001aÓ\x0012¦Às\x001fÔ¡¤\x0010´ÈÈ>\x001eÄ\x001bÒ\x0008bÅC-Ú°ÜA9\x0003î'z\x00002ôæd¹ \x0018NÒÄT7L>¨ËICrB×\x0014z¸A;dcæ®\x001fWëQ¼!
	 Á(¸BK;NhÎ,ùSPàH
!A\x0011@±ø\x0006RëqH»Ãbæ4ä'\x001e\x0007|$)x\x001cð\x0011;Cr"hÊ±r\x0015ÇÈ\x0018ª£¼­üi\x001ar²BäP}k¿Ù%1rz}°5uLÂ8ì¥a\x000fCîþñæúÍ¼¾¿ûé¿¨uK\x0007Á±iÃ9°m2\x0018P{"<Oo©Ëõ\x000bf4Ì:a\x0001}âZm{zöïÍb®jÖ\x0003vä&ø
\x001abU÷ñ¢y\x0013\x0015r©ÿpT¤n!u3tA%­N¤ÐW¦±\x0002mËbø\x0005@\x000e­\x0003\x0016=@;6ql×Ú£jonU×8EÇWl©< ÛÊfþ¶þyUqµAÃ-O\u;\x0015ZÊeð¶½ñGeQ\x001b2\¢\x0006thù\x0006ìËâÉ²)×|\x0010Dâ&x\x0011X@]%->¦pL
C¥Í2XEmÐÀ\x001fµB1PÍÏB\x001eúêtT\x0017e8>%Bî0ýQC¡\\®c£®l¯X¯\x0017ÀëÊK\x0012\x0018U³hÍ!Nàª;ªº2\x001cúÊrå\x0018°\x0013}ãº8\x001ehrò&ÿm\x001a\x000cÛ¡}gkëì\x0015\x0007/Î\x0010¢k\x0018Îc\x000b}\x001dqµï\­eglq.¬´!SG×ÜµpÝ\x0011WûÎÕ6XâêYëUÇAF×~ü\x0011çù\x0004Lm¡Y0i³ ³SÙ\x0002\x0010þ=<°îÝ\x0008¦ò\x0013q\x001b [ª)\x001cÝaèwèN¹û3´Q\x0014ö°,aÛast¡_¢\x001bjvÅiè\x0003q-~\x0019n1ô[\x00144°SÔj[÷\x001cc\x0014åµ2\x001aìWS¿·NËº~*!WÖë®-!<¿6\x000eÓCò­à\x0019¼ÓbÍq·ãaïTL¡]\x0015Kýg\x0017\x0006±\Ì°\x0005d°aXÒ­\x0008\x0019Õ_
Ï:M´Z¼4¼=Úlú\x001fã\x0013Ë¶?µGì M·<ëa\x0018\x000c¡«öÃ\x0006¬£\x0017\x0018¹×,46ïbÖÞ7!}\x001dÙ0\x000bIu[EÐÑ\x0005vÇ¦ê"Ð,º\x0010{åÄä\x001bÞÝ²\x001b´ÿê\x0001v¾(
\x0007)I^¬S¿-¦Ã«h,J±\x0014?¼\x0006íE_%÷6ä
\x000fX¦¶´/Yßá1hUÃ«ä^CîÉ=yf*\x0014~·8¯!í\x0007ãi\x001b°JîmÐþã\x001eYùåiØE\x001by}{wûd-s»Lt\x001eÄ^çe}©¶_åY\x001c&_ZBî¡q7z>c\x0004M'7Aÿ§ýL­¹aè­¯ó\x0010X@Æþ³q.eCn©ñ<F^åy
, w÷=éx©\x001e+q\x000b\x001awä0Ðìòº\x0003þ\x000c\x001dðÆcÌ¨¨\x001f\x0016\x0019¯>\x001eTnÈXyú8äY(OÈN£÷Ó\x0004Í¯Ò¸"Aæs¶ÛhY(OÐ0wÁ@y¯ §+î¨>2r=(È8!Ãà\x0005-\x0000IÝ
\x0002{A$?ºÆç£®ì\x00134\x0014FØ TË»C=5Å2rI\x0007U'd¨â£íÉI1Èò +*-èÙµbÝ¡ÒRBö\ÄÉãµmIÏZ=\x0001Ã
Z4ETØÝ\x001dªSÎ²ðvOÈpKUwQK®\x0013k\x001cîu2Ùûëû\x0017ºÊü\ß?ÖÖ½HOm\x0013_ÏUÐ\x0001«ÂÛv\x0005>ÚÁ,\x001agµ=,»ßfÏE$94'¾î0zî(;áÍ µ\x001f3ÔniZz\x001e×©eì°dÛG¯\x000b\x0001hºH¬ÄÕ¤uýç%\x0006'ä^§\x001c¢¡8±.º!àd\x000ebæÞ\x000cº5«Öîc\x0018	¸i@§¸pnÎ]G\x0013ý\x0010MÔÍ'ØÜ;,ð\x000eÉD&ZíjºW
\x0000ýêíýÝ\x0013Iè¥á%U\x0015wzßu\x0012p$Õ\x0012e<×\x001d1\x001fäê\x0005võ¢¼
}\x0001>
ç\x0008ÑRD}\x001aÊAur`O¯õ\x0003Yx)Åò(5)rh°ÍÖYÄ\x0004Â !D\x000f o\x000e
¡CÏsh©¦ÿ\x0011Ø<º¾W¿ö!Ã è¡&2HD:©E#²ÓdB8J¼AÐCÊW`Qê¬\x001f|s\x0014S=êÞ	Sr,#ÍZ%@ã´ÇÕ6Æ}\x0008czì4Òl¿A3\x001cGà\x0019Sa\x000bí\x001fq\x001dgAÌ\x0004ä
­{Fvn°üJ:j\x000c
vz\x001cÛ­üÞ0X~AWª©\x0013='Ö£\x0003ßmË\x0011\x0018\x000f,¿à°QJcùô\x000eZÄz>r©Ã`ù\x00051}ÁãÐ"W2W££§ËË·ãX&\x000cO'Â	CGC½tD9=:¾~¡ÖUÂ0\x000f±¿¹þîæé\x001e\x0003n±Ðah¡KX\x001a¯\x0011·ÑÜÍZØÜv|\x000c\x001eçù.|j;ùÔ	ê¤¶Y1<\x001fe*g\x000e\x0006áe;¾3ëc¾xEËç \x000f!EQB¼õ¡8M´gdoÖ½*'äô±§±ðÖíà­Ô×Éë\x001c0\x000cêÜÅ\x001eEâ'¡ùÖ\x001dýöæÅ¯·°Ñ<\x0013úñ\x0011ó@£èµ7Í¨µé\x001c«m÷³EÌGþþn\I´pCB'¬En/\x0019êM^Å¾\x001b\x0017\x0007iE{À²âÖLÀ\x0015í4®ÊY[W\x0015Lß´'P­<\x0017Ê{\x000eãÚ­\x0011|dÁïÆµAÚîPû8½½¡ÔU<\x0006¾ù¸M»\x0019#Fghl=
\x0001»ÔX¥ ¿Ï\ÎiS
2$;t¿@ù»\x0018ÖÖuM8%{\x001eô(æ¶Y\x001a\x000e;4tÓ¹
õÅ'î<òÌ\x0018·tt}Ðf£\x0014cý}¥]Ubf\x000cQX«\x0002\x001d\x001a®PgòBUk\x0019r§b«3ÑÁ/+$ÎÐ½B"\x0015c©!AØ\x0012àbu\x000e}X[ÛïÑ\x0015:A\x000fÐWðñÒ\x0006
>\x000f\x0013âÊ{\Ìþ\x001f¯Þ¾~ªÉÐÚ\x001fLjk[ûv\x0016É-iúd¶éNÏ ùr«Ly8ìhyÒQÐPLt¶5÷rcÝÉ_ØòÃdhAÎÐßº\x0001=]èP¬\x001e×Ú\x001câðÂÐÔ÷äý¥²0ÔÌò^³ß¡kªb~S§$QçJp\x0014¶Ô6ây&\x0000£²öÔFl"96ÂUTÈ*\e\x000eÊMaÖI÷\x0014×þÀDïG¤¸³­¶ùyj!uÐû´vqø\x001dëTAfI\x0008sº¨f\x0018r\x0007­\x00132\x0015 :ÒÛ¬Î:\x0013½å
\x0018\x001a;E\x001f\x0003=ë0Ö\x001cÜ
3Ê\x0017ÃÕÿmZúe4 
Z<åç*·­er@f	v|yl%;*¿½ç¢.ëÃbõyG×A]_xàuµ#\x000ef\x0011ÑL\JbËèNÚ¯\x001e\r÷æzÞââjkÊ¾ÏE4oê\x0017euñ\x001amÊÖa¯x\x0019EÿmÜö(c§áçoM\x0011KlØb_þë¾rIò¿»¾{ûæÕÛû»÷#\x000bëgÎ,l\x001fØÁ%Ï\x0001®ïñrðû^E÷ýÌ6º¸E\x0018:ÿ¶\x000fý\x0014\x000cìxOÂùlÈVaÿVø\x000c÷¾k>×¸2O l×±\x001dÌÆ³ÚÞ\x000cÕPUCt Shö_]:éW4½´\x0004\x001c:°èÏ½îÛ¶ñu¦ ª×þ¥9\KØ\x0011ÎýQ\x0014ºk¦Ý§B7¦\x001fuñ\x001d½]ûòßÿúow­\x0019÷ìïêN »?Nµ\x0011coyàQ¯x\x0013Z¥~\x0017µe\x0014\x0004?aLÊ'ãp[Jxp\x0019Ðùl\x000b¨¾øÅÓ©×;û]½§(Ã7?üô4ÍùDz¥\x001a\x001cáaî£Fkÿ\x0004y6\x0008Ã§S-Î?8\x0013î|:£f)P§­DW\x001c¼¡âOÜ®eÞWOØ Y´¦µìØ¶xxwE2\x001aÄ\x0002\x001dmZh\x0016\x0006Í"ÞãJ\x0016²µ`Ì\x0002À¬`×<fõô-wð\x0008ÊþpóZÞ¡É/{ì;T\x001dÑ!æf\x0012LÌ·N\x0017°ùç\x0011Tüjk×È0z>\x0003»\x0008)|¡YGyâÆâÂSßÜ\x0005»ìÈÀ,ëÓ¸x\x000bnÙ;¯\x0014¶+t§íÁÄá\x0019{]]Õ\x0005wh\x0007W(ø\x0007\x0011kÀYIBrB§\HÞJúÇWhGîoÆç\x0007\x0003¦)æäRç%C\x0000AnÒ\x0015\x001eEB7D¥\x001d[½ô,Ü¼y\x0004+Èú¶+f¿>Ê\x0019ª°c/º2F\ä\x000c;´\x0005\x0015åC\x000fÆ\x000btñ\x0003t(¤¢L¶cÉb³Û^â¯¯ß½{¢÷XîI°¹~\x0016¸Ä[³M\x000fy\x00061\x0017ïýáùþÛÑ\x000cb^\x001d\x0004\x0006ä5v¼~8Z[Iu{ñ\x0019bnÒ æqKbnÒ(æ*~ýµq¶êTnGÀ¡MñÅÜ¤AÌE\x0006ZùíN2`)É\x000f£,êË\x0001\x0019Ä\W\x001ev#G\x0007
Ì¨U4\x0005v\x00008ÁY\x0014|y½Æ´é,¨ÏM§ÅµüÕ¬@L\x001a\x0014V\x0019\x00188åäéámë
\x0008Ù9Ë\x0004È¥#kÑOèr¢Ã^Iç\x0005¶DNÓNfÝdÒ Zî»#;\x0017\x0006Îpüh¹Ò*¢Qî\x001bE¸So½²¢{\x0002	l+?\x0001uQn\x000fÐðÔ\x0006sÕý'=GÌþT]S@\x0016±KÛXª#!´\x000e !	)\x001aÕSßPÍÆqn®\x0000`~j\x0013èºb1T)À%ðI/·"\x00014H¡Í½\x0019\.í
%Æ«8BUßÄ­üöH\x000c-¡à.\x0013²ì]×\x001cØPõf±\x001c\x0019 A\lAEjµ´z\x0010qg\x0017ë\x0000\x0019ú´¸ý,4\x000b"\x001fµ)Q§\x001dºïFv";{W¨´\x0010 ­VN:¦Ec\x0003 [²k\x0003¢
Ç\x0004jò|\x001cÂÕs\x0005.@\x0003ëYH\x0019¨ú°\x0018khY}´&î?\x001cZcË\x0017üâë?w\x00024òés\x0008ä8Ä ó )°#Ð[­ó\x0011¸JÐh£U\x0018Ì\x000eµMmÞ?ºE\x0008-êZr8j£)\x0015¶N#ÉmëëüÑ%zO4Ç..&E,\x000f\x001bì^\x0001\x000e-RëîÐGb\x001eåòºèË¸KwèÍb^>@Ã\x001dÂ¬$«Ú\x0001Û³ñØð°¦µ\x001c£ã\x0008p\x001cbT;ð¶\¦%öÿg\x0007Ã¶Îïpt\x001e\x0001Î£nz\x001fW°áJM\x000fÃ6µiµ¼áïBç;íOGwK#9dáåÊ>ör-\sXÇuJu|ýöþ½¶\x0019ýÃÍÝÝíÍÝS\x0019ï©\x001a6³\uçI§å»¹®Ò3}p\x000f\x001dÞ\x000ej0ÞS\x000bKvãÏD6¤´L??\x0001\x0002än7èìõ\x0000\x0011®\x0018p\x0005dd8x[W±â\x001d¹súÁ9_¼£µ+ÍK´f\x001dqPÁøKW\x0004\x001cHÄ\x0016\x001a{}\x0015uÚí|ÿâ[aÁû'ãÁj\x0013Ç\x0015íyõ­Æ\x0015k/©Q\x001b"¶þÖçàAS9·éÔÕÎ§Ð_¥×Øqì/Ñ¹ÛºX~\x000bÈ`»ê$°{²áhÎð¬9¿\x0013á¡Qû`þøúöÉ\x0002\x0016jè\x000bÛõJV;Á»oAþå¤¡ôÆ;u±¯ùP\x0003fÞå{=\x0007\x0005ÄVYÇþìx§Zud\x001c<û\x000e78
2
.Ówß¯cÖ
z%»NÕ§øÐ:ðáÜÀ\x0003È
 èàV=ÛW±¹g³ón¹*cw90(´úÂÑ\x000e|µ
wy(\x0015øöõõ«Ë=º\x000fo³°/¤×n¦Pq¨CßÊ§cñhÍ\x0007±¸·#'è!\x0010µ-Ýó÷Zþ^¿fqoG\x0016\x0017\x0018Àà
\x001e\x000b\x0018U!\x000e\x0006«dÈì?æÅOÈÀâº2\x000eiv8×¶!3Éa^ë\x0003Àb-®×â*É5IµC[\x0001\x0019dGç\x0003Åe°ò-{òÆW»
\x0015ûñux÷â·oæj½GW'd\x000e°Tß_\x0006Q~\x001e\ E÷9¨§3JMîC¬5
\x0012\x0007Ö®¿¶Ø¹Ý\x000bµ¡wOÏÂã
ö\x0005kV×¹püÈZÑN[h}e ¬Ø¬\x0016Ë/,·Õ¾~}Ö²ßÞ¾º+x*ë°`¦TO¸ìjVAÍ´µ{~¾tÿBÍ1¸¦ùâ÷®\Ä¹\x001aî7×â"~"?±XÅø6\x001dí\4\x0012ú,\x0010ñ24$òE\x0015]èiOÒæß»AY>}1W5«Ú<õ³çzÁºV/69åKrÐý¨/S¥+"înTåsMå{½;¢\x0000\x0019­\x000c×BqçÓÐªSE\x0005z²Ý6Å|adX75tÿ<ºPÇTwæ«m\x0006áÂ\x0016\x00185qk*ï${kp±zQy,å\x001a+9ÜW\x001fPBù_¿øÝõ«\x001f~úûÝÛ\x001fúû[^\x0012Ù
*óª r¯õ\x000cÉÃÔ_q@
å!$K3³su\x001aÆJ[v\x0017ï¤__)wX\x0003\x001fÇËûwù7Hw_øòÓÏRé\x001e¨\x0012\x000eÁQÉr\x0016®õç³\x00127ÎJÜÿ2¸·ÓÇ¢¢á;\x0010ÎçE²$ß`ÞK\x00107¬ÐTà\x000b5£æ\x0012\x0017N)aï]\x0008!ï¼Ï!óá8wÐ\x0006Ã@¼´íï
ÇØ¡Óã>0D 
O"	¾R/]çn\x0001N\x001dZ´@p­<ãTX'%æ^vÂÎ]¼ìÎ1ÂÕÔÐ$L]Cû\x0005\x0008¹ôÃv©÷Xk£L \x0015AÛ×êmmU=ÆÞ\x001bCÑ \x001d[´\x0002-\x0012Ká\x0018r/íM~ûã ®~¸ùñöMó:¾½ûéï³×ñ8´ï[öâöÃw¦÷è\x0006×&\x0010»Ï ¯¢Rôa\x001cå5\x000eW±\x001d\x0018=$ò
¦öÎ\x001eù\x0006W!Ð\x001bt¶\x000fñ½<Âó@\x0015Î¤ú÷9\x0002-¾<6ÀêOóÑÚ2ZJî¥yû?½yÝoùW7w?6wá·b³ÞÝüéO³ú¨{NÚ¶C<WÎA\x0019t\x000bü>vF#¾Ù\x000bÏÑKÛiÔËÛ±^>ú?]ÆÛ¯1`¥°ºl\x001buO#l*¤%º°ùÚgêª°m\x000bú¾;\x0018\x0005b;©I péëgy0eHñýúí÷×\x000b§áq\x0017`\x0003µègq\x0014Î½à*Á,Ïæês\x00087mØâx\x0003£\x0005¡\x00075Ø\x000f>².¦v\x0007ùPzó64d4\x001evØn:xï{ù\x000e¢	4þ:X\x001a³\x000fsH\x001b»áÐù:â\x0017l£
\x00169\x0008»äÝ°\x0003wFôÆõICJ±¡~å`cà³ðve7ìÈÝjpò\x0006î[\x0004Ùò"Ô »Êø=ÙfØ\x0003è>\x0004'8\x000fµ²¡¥õq¨@\x000fÇ¡c×'ñ±f\x000e|{wóî»ÿz¿y<î-1ÜI^JÍç·$¦z[°Ýg{Kr~Ø\x0011ß\x000e\x001cq­zÉ¨Æ¡&\x001dÇ__[õôJalÙê¼NÀ¶PxQÔ££13¥l\x001b&É?#Ã Áö\x0000·y¶´X=2\x0000i\x0014GcIfööþ}³C~ÿöÏS\x0007é#¯§\x0012±cquw"Ä\x001cOûsÍÇÖô~9Þlº]9¬Ñ34\x001eØ¦©\x0006´4]eç-U7·\x00030¸n&4õµ\x0003;¬¯Pd6aËÜN\x0000¸Ý4\x000e\x001aTéZ²øÐZ-úuñ.È,r1\x000f\x0001dð\x0008O£ÝÎÈâÄE\x0002\x000e\x0014#ÐFðµb\x001f©+ÙkîKÄA!Ð[ïÃlG\x0000r\x0001S\x000f>\x000bÉº·£\x0012ÍÃ)ûVH:º;r¥c¶ýaNyéõ\x0011²(:×\x0019wèÞ~$4\x0017\x0005n.\x0006\x0006hàfoZÍò~Òá*\x0011rbd\x0017\\x0000\x0019ØÙ>/R
OQR¢é8j«#y!Kã0/5\x001bú¤Kù1
\x0005óMÒ~õÄyX)Ã¡1ä[y>Ê
&¼\x0014-YÝã\x0012§ìä9äqZóòüP·ï}\x0019:±Á0È\x0012­\x0011\x000c:*¾Þ.¢ÂÜ5VTÙ	i;H\x000b¬\x0010²kÍÃ\x000b5Æ°b¬m\x001fé\x00199ðÌ\x000bñ\x001a\x0012\x0019¹µ´hÐBe\x0011¬x\x001aÂsF:Rt¬$æ\x0005Ûêc\x0016e2=\x0012ye\x000eÛÊ\x001e
}Ä\x001dÖ4ôÑQÛ>êiÅ'Þ#©GýÀBµøõëû¿jªø©âzÁ³\x0013O·ë\x0018­U\x0007îôØ}±6º\x0018Ûè!dÓeAËù&<kÓ<ù\x0000û»\x0017Mî¡¡ÕÍàX\x001dE\x001e\x0002\x0008ù\x0004\x001cyb¯V3ÎÒ\x001arâg©ø^¡Dñ\x0003
¸\x001ei¨S¿nÔµm±?¯¡ï\x001dÇÔÄiÀÅ;Õ¼£amß¿Àñ\x0016Zùzüç2\x0017¡\x00020z\x0000rC¦b[Z\x001eE2UnhGö`ÓDb÷\x0012G»¦\x001cÝ8(¨árhm+Ly§Sî^ß>âÙ\x0002@K=\x0017Dh\x0019ì\x0008Ún9\x0015D|Î\x000càyÊÀ<¾¤«ë2ÉÐÄA1g=çÑl[`\x0001\x0018'÷æLåJ\x001e¯¬Þ\x0018_qñs\x001e1,è{#¿Æç\x0006ÇÂr1e­Òê\x0014\x0019Ôup\x001aÚ>Õ=a«)×8\x000fD\x0005änéio11JÂb\x0008\x000c<VçNU\x0000Ð H{\x0002\x0011-&hEH¶S^\x0008ç&\x0013Á'è(
­£(·\x0017\x000c'C­]Ijq\x000b\x0013á÷oÿ¬\x0015\x0003O$¦¦¸åêJ\x0017S
'AnT$Dý\x0007Â'i¶\x001eÓ=»Ë\x000b¤5&Ì×P\x0017å¯<\x001fz¨ÍÛ(´!òÏ)z\x0017æ\x0014À\x0005/P{¨gî°ªQï\x0016&\x000br\x000b\x0013,|aÈ¿Ù§;\x0008ÿër\x0016ZwÅßNëÉ0tOxÝöº"ÍÎÊ0¸!=àÙ¸Á³\x0011(²{Wy;Ck';ÛOó5\x000e¡ð¯ïnß½{Â\\x0012U°ÅbØ¿ÀG4#µ¥§k~ÞÔùâÕ°ã«\x000cÄ!.q4$AÞs\x0010¯ä5?V;ò£X¾\x0010\x0000ÒNb2f,u_	rµ ø¸¼F,ß^ßkmçùPã3SbÙ5Lu}ºlhµÂÁÁv°×h\x0007\x0017\x0003ÌhÖ\x0003óMÁ°½ËÒ9ã%£aH°
ÜP´3Ú«=\x001f\x0000\x000cJ½nÝÊ;0/\x000eWí;\x0018îuÁ8¦æÎ8ÿóÇ?éÀ\x0017¿{ûæb\x0005ûTÏ«Xºt|1Æ=Ñ\x001ctµ(mS÷ñÅr\x001cØÈ91@´Ìis\x0002U¾øÈÁò\x0018íÚý>!\x0003ïÄØ'gè}:¾bOÃ\x0014yÙ¼´ÏNà\x001c\x001dNP\x0019¬¤\x0017\x000e!úLÁIùU\x0004§Æ¯Æ$ëiqÖ\x0013eXm¦ãÕÄrNéê¾¾b-´D÷\x0005eX\x0017·<°ù´\x0015îü\x0005¾ \x0011¬§àM\x0015ën\x0018\x0006à\x0007UNÌ=ù\x001ct¼\x0001¦n¥\x0004Õ\x00143Oõ\x0002dØÌ¥ó}<\x001c:\x0007õÂæd\x0016Å-Öü¬\x000eÓÇñs\x0014f¨Æî%¸Z5\x0000i®\x0016Ì±%Íú\x000e¸\x001cØÏ\x0001A¨Î¯Ø»©\x0017A{\x0000«9-Õ;Bî\©\x0003,ö>öVÉÛzóú¹fÚj.KX²å\x0019\x0019ØÒÛ\x0016b:Ó¬½Ú×å\x0001D³Î+¶<#Ã\x001e3ñsBgK]ëÆ\x000cÈ\x0004/µ.Í\x0001rs®`¥©@iËd«e.svYsFî²øL\x000enPÜ\x0006,s\x0016þ¥µnÕ´\x001bÛp\x0006î{t{GÁ\x000bÌ´Ô7¹@\x0005Ú¶\x000c±\x000eåÛ\x0006Â¢c\x00062P|\x0002\x001c\x0007\x001dBô9\x001c\x0003×{¡ÜGóÏãP\x0002¸>¾i^ÇT#÷ÉÍóË\x0000\x0019\x001cõÙ\<×uThØØÂM3VM\x0010\x0018lÖ¸\x0005²fW¶\x000eÛ\x0011\x000f±zÒ\x0014}áâxg¸z.°XØ¡!I\x0017´ø\x000cRô%sL\x001b,\x0008z\x000b7×¥­t¢cYÊètc\x0004Leüi+Vóî§iªï´\x001bìú©\x0002Î¾r5½ýn÷Ò¬Î\x0001a1MõsÓ"ÓÅ³UEï]Ñ¡µ[G\x0012§\x00109ÆjÓÜ|\x000eÈ]Pm\x0005ÿ¯\x0015\x001atÓôáB\x001b2µ\x0008ñ\x0004T£\x0013Ð=¨X­¤«Ó83\x0017[´y\x0011nªC¸IK¼1o#\x001dÅß×l8mýb?tB\x001a\x001dî\x0006Á7#^\x0001´	ôÐyS|sh¬Y¦Oè$K69þ\x0005*\x001f 
ÔÊÂË¢)æ±µ\x0015?eºø\x0013Â0{qg.@UP»qzÃó¸\x001e5ë~\x000f¨Ò\x0013\x0006KHL\2¥³,éëC=\x0008\x000c\x000f»{C´\x001cKëØïÈß½b\x000fÊ¤Çg/Ðº=ì¸08Ô13tPÌl\x0006±ÀKÝ\x001aé)2,_ÄÀi±=«#<ÅÓ£¿\x0017`;.\x0019cmÂÚ\x0010\x001b·ëÊËñ÷·ÿúTá=Ï\x0006½¦@z;&J \x0014÷yb4ëøíÂ\x000cÊQårñ\x0003ty+\x0007:øÛm\x001bq³ð±m»-ø\x0003M5O\x0001\x0014b\x001a50uU\x0003óI:Rc
8±iOtE­íÖÅl[\x0006ãËÕgu¬W	¡b±<>Tuìi¾¥ª³°,)?\x0003c3ªëbåhÈº¼b>ÓºVu,iqçÝ±¢7=UÂá\x0001JÞ­Íx?ñiÆ^ñ~0ãµ´î·Nê()Ck\x001f90½ùêÁvô7Â\x001c÷æw\\L±E\x000fúYÛêäD\x0007\x0003Q¿\x000bºêÉy
/(Kèñc\x000fzÙ+LGìõI)Yþîß×\x001fßÿf2\¾ùaÕÝ\x0018Ë©Ìe!O6E\x001aabrî|<r\x0017½\x0000Ûê\x0004Üa\x0016Êù?Í<øp ë|Fdú\x001f\x0012~ñ£'á&lÿ±Øù\x0018;\x001cö -/OâÇAöß^ÿùíí´Qùq<ã"5Tyý/N)\x001aíëº\x000bc«÷[ÉØ3ñL5åÁÄÌvBÌ1\x001a\x0003»êT;+íáCÁ\x0005¢\x0008ó¯\x0008À®\x0003g\x0003£ã«®mê$9:ã\x000b#Ï\x0001\x0000\x000e\B_=Q]¦½àºÀwdÍ\A\x0004À(\x0001MËÀ\x0003Å\x0003²ñs°\x00083 û+\x0004¬m£¡ÁV\x0002¼Ø¨\x000cÀe\x0007¶&Ãèê­GMcbC\x000bæÖ#äÚí¾ GÓb
\x001d9gFÎaaêwèÝÔ·å<­û\x000c\x001d¶>ì\x000e]ê\x0000m\x0017+>\x0000\x001a¸¹V\x0019\õÑ1ú\x0002\x001d°GÏ£5(ÙQ\x0001îÐ¾S\x0012Ìº¯\x0007ñHu
.Q\x0014Æ\x0012Êèïã=¿¿Ñ
ÄPÒNèÄ\x000cZ©À!]´ÜNòHõçp\d2Í&8Ù\x0013zÐ;éF<¡XO÷î[¨(7ª(aÄ~àÖ·oèª/Ð(ÝdJ£Y»k¨¬ë2\x0000TFDöF\x0011%íÓ]«(7ª(gahmÕ1¤Ôµw\x0003r\x0007\x001e\x0002rê4kïz×$¦\x000cÄSs û<¯
\x0002dP~º\x0005[÷b7Tæ\x0016Ý_h?®&\x0013\x001dY±F$\x0014Ê²_#[l!\x0002ä
È\x0005Æ\x000e\x000bCW¬SÓ0|\x00186¹\x0003åçXùét\x001fà9åÀÇl+é¾xÊ¾­tcÝ'îTlQ3´<åN#[Ò}ÂWu\x001c\x0000í\x0001®Ð\x0004ÏK¬t|öß¦\x0019\x0000\x001dûyxßJ[Ñü
\x0010ËÇÑò§vjíChTª¹\x0004/¯1uª.\x0008$ü'/ìåI\x0002?¨xã±e`ÓÂ¶DÉù7°é¨jtÿùtkÈ\x000fOÀÝNh´+å5ó\x001e¨Î\x0016<{)ÌÑ$@Øº>tCiÕÚäÖ3²g^\x00012Z\x0005F¼WÝaX\x0008Ù\x0015¦9æ¹¥\x000f»\x000et"\x0016î0+²\x001dx\x0015hR9X°á4lüþÅ·×ÿq?§Å\x001eÉÁÐ\x0018ÔXãþÂ\x0017åÑV«\x0002}ÍÁ%øa"¸>Å}å¹È¿<E\x0001µ/Øn ¿íÜ_\x0003À\x001e^5\x000fFl©Å\9zÔhÔ¤(.?ÏN\x0001``BcaBbÑ-u%Ð%a´TW¬bÆ­\x0017ª\x001eÉ.>Uö
S´=ÀßDHc3']ÊÃ[)·C\x001aÂ'\x0007T_üâµ7Ì½:jjBl]×âmâÓo5VöS9PZeä\x0017]D\x0001êÐGÜÀ¢f¬cäì\x000eüaî¨ÑÒ\x000f&XY©\x000eHd­\x0015\x0016ù)@NÀã®·½)Í4^[¥Ç0rnÅ\x0013\x000b§í\x0008Í\x0005·)re/ÍWÇ7Ó¼ü
Á$´\x0011­

ÄSÌn¥:°	Ë`\x0013V DózÐìZÚP\x0016\x0015\x001f\x0000FáfmïTÛö*£QÈçá6ø¥-¨VyÓ=pß·"GFÖÌÅ\x0006\x001d\x0017çÒê²úÞÝÞ<Uä.\x000cîkCUÏª¼À\x000cïêê\x0012x&]åÚî¥å¡CJvèµMJ¶ÇÙ@òÉ®pÀÀµD½>~y
ZÅ_ºW4\x0012v`äu4vLÆ¶ÍK¯¯ßüñÉ®wc$\x0013ªï\x0006¨GKíQî§ù2ìæ0Þj\x0006r\x0015÷h íD³å×\x0017F3§`Õ´¥ÍZ¬\x0016àÉ\x0007OksÅáùÑ`^\x0001á\x0001K`5Y-</5\x0005ä\x001eë°¦öZ2õîkë"Ø¦c'\ìõ\x0015\x0017æÉ\x0012ÚòHOe5óËª%Ù²»5Àzê½\x001dV¹\x0011ªÅp·Æ\x0016X)\x0010\x0014GÈ\x001dd8\x0014èBsÄÜ#	%%J\x001f\x0002n¢SMÂ6Ë~u©vV-¸~óæéÞ\x000by\x0017¹ªR}~ø<Ê´S´<ß¥Ê\x0013ü`yÇvD£+´&ûâ'¯~\x0018Óÿ­(ôW?Ü¼ÿtná8sÙz®©ÀUùm¸×æúñè\x001fn_{\\x0019¡\x0007\x0012aË®¥¡\x0018¶¾Gq\x001eÈ\x0006À\x0010\x000fN\x0005\x000c\x0000ÕÅ\x000bóCBV÷<®ïÀ,__ßóúíÔOûè|¬\x001bâ©ìÏÍ°±KUwïýÿP)5\x0003«\x001c}ñùàÛÂËêF¾ÿéï¿xýÓ¿ûÅ/ïßßñ´Æ¶Ã .êGÜÙÍò1Ê°÷qk§\x0019µÔ\x00141L°
Vü» ßõ#êG&r\x001eSGb\æsxyò²¨3C\x0001Fö[î\x0013Ï½È~EN\x0001?2ÚpîõõÑd\x0018¿b²WEEe¯ã'\x001a+Ôä\x000cÓ)\x0001 äk¿ëäG¥\%\x0006j6OajBd×u\x001b\x0002\x001cÄ91\x001a\x001c$¤jâhZ ²ÿê#¿t[£!Àq\x0007Ö=Í\x001e\x000eÃSÑ«\x0000ÓVAAöc%ö¶L4£\x0004Þß]j\x0001}\x001c?òÚ\x0004\x0017Ín?\x001dÝÞZ÷ÐN\x0010o!m|¨²étT#?j\x0002Ê\x0002õ	\x001fPùrCºõËãÔ>ÈÀº:udgq¼i\x0019«[\®\x001dg(·2ûzûîæîú\x0003·$~ÀýFK´é8}\x0007úa&k!O\x0008Ï~¿%|Ø\x0005\x000fÁ\x000c%ß÷\x0019Ð"c¦à\x00105ýôÄ2fóú­\x001d/ØÂWA´\x001e}dUæ&\x001aAßè.Qâ\x0016Í¢¥&nËÉ§Fä\x0000Ñ'F	p\x000e\x0018Ö³¨t\x0016¦¤\x0003Mf\x0007M¦[ÛD+±cd\x0003!Û<MÃDä\x0004$ÇîSö\x000bXí¥4g>X§\x0012'D.Ä\x0019\x0015oEÆ\x001cHéÐê½8î
Ð{ÜU¡sÏ=\x000btL¸ÐEÃðqd¦à(B;¢\x001aÅÑ`mI#Y£%\x0012í\x0011oXäÐ
~½Âãä\x001b²ç+l\gîÐ&b»~\x001aVØ.2ÍXK&.MiõÌ-÷~%åú÷^>¬\x0008}À0Ùó"7\x001f*ndTy·ÇY\x0011fc\x0017Õùë1|Ò*^öB\x001e\x0007E\x0018¦LDFEhû\x001c\x000bAÖu¯Äí®ÒëbS¦¬ ò®	CÑ­\x000cäÈ"Oº+ËÑ´\x001b\x0019C?àúz\x0010=ý{r\x0018\x001fDy\x0015&÷\x0016SGv½T(®\x001eë\x0004\x0005Ø°º²&­ÕÕPé®sÝ
\x0015Gþ
µ.m !Ê6®µÕP6)ÈÆõ\x0004 ëT.OÇ@Ð±§Ú¡VØ\x000ejeäLÄvð\x0006»Â
ÀçLZËúäW
 ­L¡oÞ¾\x0017÷ÿöß\x0016-ñÓ\x0001É:\x0012\x0004-Ú-vy~\x0002ØtÛgV\x0001µ,¶\x0002,4@\x001aM!!\x0017ÜZ\x0007tð¼jRÐO\x0012\x000cÑR`s5XXÌòÕLÓ"\x0011ØÓ\x0004ÀÁfÎ Ï¨u|Sk;Èð\x0006:õè,®'"Zzéææ!,XAÑ÷Á,{ZÞé-¬®«S^\x001bû\x000bj=4»n\x0014\x001bD-7çÌT@È\x0019¢^\x0001°\x000bê<{~òn¬õ\x0015/µ;\x0012R6æË\x0011¸vkè¥é\x001bÉDq\x0008qqÈ+E\x0006³ÍÞÄf*M\x0017«çû³m"§==ÛeÏ\x001a/²FEè\x0018\x001d¨vkð\x0004ÝÅO\\x0007ë2f³JÛU4\x001c´ª3\x0011¹Ë\x000cý\x0005s\x001cØy«\x001e8\x0014\x000b\x000fµ\x0008ù82ê¢dÜpm\x0017=bhá8Ä-\x0003á\x00166t\x001eÅ³ÒðãÂCÁý¥ÁÝE¿ÿ¸¾ß§[ßÝ¼¸¾ÿË¯ßÞÜ/ú\x001fõèhñ\x000cR%6TÜ\x001f\x001dmÜ\x0007éêÜ\x0016f>·áù`ÊOÎíÚÑ\x0001? þâ/Þ\x001dÙ\x0001r½ÚÚºíÉu4UOÈ.®\x001e\x001d¹3þc¢ÐgGî/íßó¶F×Uá0X¡Ù`Ù oÅ>£HíÈ]¤b±\x0010YÌÄ÷ÉF¬Hvú\x0017òâñÙûã\x0013ÄÝÛÄ¿¶4\x000eVNö\x0019
ÍÑM\x0015üÜe5¦>öc\x001bzU\x0011Øz>\x000cÑ7Óø%\x0004îoDÛÀ¬3ÉÎr¹\x0016Ìiµ¦]Íî#¾CV\x0008ùNÂ{qkÊ\x0003ÞÃ)\x001dNKzW\x0016íj\x0008ú¥)lM'p\x0010³µôÿÔ;J4$\x0014_ô¼ºÅÖV^ó\x0001&m\x0019Ë\x0001ù¾|\x0015còç^*öîÅ\x001fnÿø¡\x0005jñT_µôÐ¸Ì\x0019âE)´Èâ\x0017q\x000b\x0014×B\x001fñÓkH?'µø»?Í©EV©Å\x001aËElïÔë}ö§(ëJ'f\x0014M¾Ó­iYt¶,Sgr\x001e±\x001aÝZø\x001cDá¼ýîOï&O÷ïuLÕI%èWÏÜ.s£ÖÕÑ`;söçÒÉ:û¸\x0005\x001dBjÝèã§¢¿[¸¹ü\x0010O\x000bBý½×B¨¯\x0016óÜòáÖ9­\x001c^+\x0002Î\x001f\x0005<¶\x0014
D÷WEðÛ<\x00138yÝ\x0004eá'äA,ô\x0013q\x001cV#èöÕíüøCg ß_ß/æ\x0005>o¼´@¸È¸\x0013õU;{÷­>ë\x0012Ñçg\x001bQF«§Ä\x000eW°\x001d\x0012:i\x001fpñÛ§Ó¿ýñ?¾\x0005â+rûâO)¸>2µqgÁ­Ý3VÁõµ\x0001ð\x0006RÕpïåÇü|Nø7ùò-¦¾@ÁOùøTÿÊ\x0003\x0019Ûwl\x0003\x0005M)\x0008)ØÔ£¤\x0007\x001b§Gêå°0\x000bú_Þýéæn5ùì×¬Ãâþ	é I­\x0002÷y¯Y4Q}¨\x0017æt`Ã%g]Íí:ùºÄ©à§;æp\x001d\x000049ì:rL¨>¥\x0008§ GÆ½#®\x0007ÜØsÈk0H&¸\x0016q	²\x001aº\x00119täzý^eÅH¤ WæÉ-&;>;p\x0002å=ïÚ\x0014j2¿h®µ ·6²tÜÍ¨b`z "o\x001b}º\x0019eýÀ¹~ö\x0006\x0001¹¿®Eã»\x0005\x001eX°~-a¬QÐq`®®ª\x0011~ª÷ÏÕL£¦t¥çY.uÎöU×c\x001cHø,bÙ
=,Õ\x000cR©;¾÷ô\x001e~ÂÊlÝË\x0014=ÿ<¤
»ôèöÐÅÁÁ\x001aÙ£ÍL*Ká©§j
0b°Ø¤/WEÛä¦Â4\x000b\x0001q#àº\x001e£Ñ´Ø­«ÀÌe±\x0018ÓÇQ<K\x000eÏ\x000cV\!ÑW¦\x0018§º:R<\x0005ñ\x0001¸tà\x00003k7lÞ\x001a=ßÝ¶p\x0008¶wès°ýPZ.
Ú\x001ck\x0007änÆ{²D¡\x0003Î+Ð\x001e\x0003ËÐ6/ª/\x0000Úuè²-8ØoÐápf6n¼Â2\x0007Û\x0001z\x0017ÚÊ"9\x000c\x001cµ·V½ëø¹´\x0003 \x0003\x001dHBhy´v ü~¹æ@>@´¬Ø#a±]X¬õJu$Ý\x001bÞ\x001a&T·Ê-{$/\x0016åÅ÷\x001cúY	·#
ÕÞð»\x001bÚ\x000c){$1¶À5ú¾ÏT©®4Ñkd/±l	5;®u#&A'±\x0015ù\x001b<\x0017j¡Óé=e\x001cÛjþÀ\x0004òBuÊsì\x0006¡*<\9qõ\x0012Oò¶Ýñýíëw:<è©ü¡áYò©»C" \x0007¬cûåã\x000eís\x001eÁ\x0019b=¥>´Ké\x001f\x001e\x0002ó¨_T¦\x0002p7c¨}mª"SZ]½,\x000e
ù±\x000f ¡Îu©__¿yûÇ§st+Íü\x0017,Ôý\x000bNÈÏ¡<R¬Ohjùú¶\x001dn6éÌ\x00123¤ÈÆ¹üWüªFwpµv¸Ú¤sBG.Õ±O¬\x001aÄYÛZ·j'\x001e{Á\x0006O\x0013\x0016xj8(®Û\x000b²x@(mu|\x0017Ù`mlQÚª\x0005\x0013B¯Ï\x0015d\x001d¿O\x000e?\ÖNkG¥RÚªÑlð=Õ\x0017²hE#R H|÷¸¶·¨&µÑlÐÞòÕaZIEUoMíÍ«GÈ\x0015!aå[@âÓ°\[zpeÉQµëYÏZN8
@Utu\x000cç
í\x0008
A\x001b1Uh]ÙËÇA<¥îÀn±l·4åj;sDn½Pi±7uénN\x000b%î_üîíýë's7Cô~àÑ=LJÀgZvú²O¨\x0004ã\x0007Fê¨\x0003-L=\x0014ê­i]$]SÅÁ©ó|PDF\x001dèûø\x0002EÎX[¢:°°\x0005Vâ@TÚh¦\x0000Òl
Ñ\Ë@óA¸¦\x000eZP_®¶½Éÿ\x000f£Ì\x000bW\x0011¸+Á¤kA¡xJª\x0011Aëñt·æ*\x001b²#g8Á6¯yxÄêÓÉË5\x0019û¢P,`©\x0012|Ü1/t oíh4ç+ÔÛ\x0005+Çd\x000e·w[×.ç	\x0019ØY\x0007&VÐ¦\x0007hZ×¡;\x0019æé{\x0008íIR\x000c¼c¦pØÀ§<ÈàFõ"°YÙå,)ytuÎz"¾sØ?,ToÃà\x0017ªû\x0004²\x0012z¯ÉF5E\x000eü$ÐPÃÚ/<A\x0003O;ò|\x0014Ú[b\x00103\x001eH+\x0000<b=[?Zß\x001d©R÷Ñªtì\x001cÂÇÍÂcYß¾¾~u³\x0017ÔÝÞÍl|0EÛ\x000f±þ`ÆRúxß\x001a~ßk8Èk/¼\x0006\x001a|¨äW¸¤äGì7¯qCzÒ¦¹\x001bÁ!\x0014Ó8c~\x0003{\x0004Ø\x0004<Y³Êº;0\x001fKòsÀÊúæ\x001foßlÃV®o_¿¾¾®\x001fëpZ\x001cq\x001b½\x0016ßõäaèå»>Ëÿó
/+0ÚZkê/~øqFSë1À\x000b#z\x0018¤ókÝÁòíÍÝ«\x001f,0xd%×~·Z7
\x0011»\x001aZ\x0015âs\x0007\x0013ý Ë-y¼\\x001d!\x000cÁ8D`]æJ\x0012ÌÜ
È ½Éöaz-¿áC	è×¹\x0008\x0016!\x0010\x001d_5þ\x00114?[èq®\x0005`\x000e&@\x0012KÛºè%t¥/UXÛÑy
&D:eqùÍ\x0010Là`ô<À\x0015!\x0000×ûÀf££yÞj¯ã\x0008'ÔBLQÑ$\x00182á®\x0018¶GÍª[¬C£·/]@¢PB cf·ÍwKkã\x0004NÖFc»¯ÕÉç§ú}%}mmÌÛ\x000ff"<¶B#DV)!÷
¸ÌÛ\x0019Ü\x001d¶~J×¼5]À{á\x0006tÕ9§¢<ú¹Á\x000fÌ¾µØ,\x001e\x000c7<\x0018Z6MÈî\s?hx»ÖUÕ
ºêàÄ/ÞÖ:òé\x0006eÜ6î|'9àÀ¢æ\x00130²÷k§¿ºA[é\x0002VDÖîVôs)g	vn\x0007d(uµ\x0019ßeí\x0010b\x000fº\x000e¹Ä°vú«\x001b´\x0008\x000bx\x0002N\x0017ã)§4%m§ý\x0008Ü\x0015®xÆzl(m&÷7älc[\x0001\x0000¹;^E\x001eD²ú\x000b'ÝÓ 
Ë¶}n\x0015øt*\x0014s\x001eH¹Àh¢!ðû\x0005®rØ4s_¡SÀ¸s´L[ãÀOgÊ<^\x0015¡\x001dÝ!\x0016\x000bs\x000fÚ%B\x000fÂµ4Î_¡sî\x0003mÔðü6d;ä\x001f=Êa»! PB½Â<såÊÀ\x0007YÙz}V¡`Z\x0014 éN¿\x000b/î
h	§ZSÍ«:b\x000fg\x0000¸öÙ2Z)e°H s\x0008\x000c=.-ÞpÇÛ÷/þùæÍûÅHÂÇ¾d6ÑÙå¸§PåyÇX+$<Eim\x001bj>à!£ö\x0010%ß¾p"buíØe~¬sï\x0019 »E^0z\x0019Þ\x001c\¦°Õ£¡©±C¾¬8íBà®»\x000fîò\x0012\x001b¬¸\x0011ðq¬òSÇqÒð5à\x001cà\x0011RâùÃ8\x001fÌiàÉ¤\x0013r±Æ9q"Î\x000f¡â\ìAò7
<©\x0011yìÛ¨	G ¶ôÄp¦æ \x001añÙ\x0006Ûy·ÝJqÑÀ61é ÖZæ\x00159xªÑ89ß\x001d¹úAý.C\x0008ózÞ\x0017ÿ|}ûæý_ÝÜýñæþ/O¥)ëPrTJ·ùå"-æC¶)\x001a_hUv
£ªÔN:Ph9`Çd+\x0018\x001ej\x0012òª\x000c£ªÌ\x0011\x000bÛ¼uW¤vrfûys\x0018\x0017\\x0019\x0006®|DC×Z\x0005A\x0005\x0017\x0011QÌóÀ?Ël8yaò´ù\x0000ÑÖ°}Bö³\x00066\x0016{ëëÜ¤\x000bÈÝä×!¼\x0016\x0003úW;JÚ¼
ÛÀÖeUØ	Üòb+Vè¡äÀCY½\x001fe\x001câòÿ×ÿûù>"ÒçâP\x001arï±¤sÞËäEBÝ\x0003\O\x00075\x0006[\x0003Wqº:mÙÁ+?\x0008ÓQ½G±L\x000b¸H>s\x001eÐÖ<Ôþ4FúÔL*ä|[çÆÂämnÉ"Ô7>\x001cªF<\x0014±\x0015\x001a\ât±äðp\x00064HR¨\x001e;¡CíØ\x00046-CÜ\x0002\x0014gt÷µ\x0001	Ý}[\x0003Ç¨³üÏê©ÇÎ¿»¿ûÅSöÙ88&!¸ýt²Å\x001b\x00155Ò\x0014Ú\x0017Ñå·PÀcøü>]Â×[Áïé\x0012þáæîîö§ÿ¾\x0013#øæÝßÝß=Qi«\x000fc·«å\\x0004\x001c\x001cµÔïp­§ê¸\x0006;¥Ú¿\x0003{©ñ^}ð\x0001\x0017?~¸øÕC=ã¯oïÞr)\x001e½6	Íâû~\x0008HÒÓ¡©ºâq\x0003u\x0015\x0008:W[\x000b]°QÜ'A}¦á\x0011Ýá^~¿øåwµ·7shûÿ½¿¹Óñ\x0011#çmýP#çÅ\x0007Æ\x0012lÀO\x000c±÷µÅ\x0016\x0002¬ûé¨¡QÐýÚ¾÷<¦º\x0007\x0003Úç#Bóöê_<=í?\x0016;\x001dc§Ã\x001eÄäå«ïþ\x0012ï¾\x001fæÝo®\x0017ã-\x001eÇ2ÖåZ¬±µì\x0002\x0015c\x001fÚ¢Vêû,ãóÃ5Úç\x0003bÑ
^½O5µÍ6¸Kõ\x0000ñ6wd\x0019Àö\x001d;m\x0003'wlÆ´ÎFÃq`mf°A}é,\x001aÀ6\x0019}¶+óMµPz>ÆÎ\x001d[{(\x001ca{Ò´|³aÇ9vàÖ4øèÂð}âÖVÝ÷Ömh=w\x001a(ªwad=w7Ú`ñå\x001fsxÓ*|ÏâôVë\x0015D\x000bÿÓÍÿ¼ùë\x0013é`qýèkcµé¬\x0015¼ËÝYO5{×ò0Ï Pb\x0010ÅÅþ©2\ÀvDh\x0000\x001fS}ñ§ÃûÎÄëï\x0017ÿÍ\x000f×wwoïè	Ô×Ä	.¦ó^·$LÒ[ Åz©[ã9½|ÔgÛ!
úìê_¼Ðgí?\x000e{¼Ú½ý÷ÿ\x001fûÕþVç*¼yõúí\x0013½Q¦FL\x0002ËcY\83§.\x000fû\x0007$]\x0000^?§DÖÁv8u°&úâ÷N§>¯2QÓ@÷éÝ\ÏÓGJÆqéþýy\x0004M%lðwòV¾ú\x001cÖA.ñ\x0003¤iZcb5g|Õ_*­ª§
âÛÓ\x0013+¯w¥\x0000ì:°\x0018\x001d¥\x000bR0\x0005É\x0015CFÇÖó:Êè´Ää±Àá\x00088t`17öW9T1
«Ë!ÇË#\x0000¸Û1\x0002Ï¨S\x000couÉÕA§,¬ê\x001d8\x0001Å\x001euÌk¦Õ¥\x000130R|Y\x0018H;rþÈC\x001e\x001fÏ\x001d¸tàR{Ñ\x0000{Ãk\x0004¸\x0016r\x0003¶é±õ\x0008¸và
ÙF\x0001¶yX fC.f1M·C÷å³B³ë-Vz\x0015Ûõ02ÓZ\x0015=\x0012?k?òíüÙ¿É¾ÝA\x0000ïAV9\x000eýGZP8>6,-\x0000\x001aDÐ%ÐE\x000eKý\x0004×dæf\x0013\x0017Mr\x000b\x0012h<:ÚâSYÍE"Ù8\x0006Ë\x00147áûÒÌµß·@ÉõSÅ+¬§ýDb¶·\ÄÉä×9m
uòð39Á§Öl\x00074</ú ì!hQña,xx\x0016\x0008\x0014Sò¢÷\x001b;klOÆ	²î>­ìÈñ4e[>0i|`¼<Ý]Ö¦:¦9d\§¢7æra@îìÝ6mì\x0017(¿I\(V
Eµ^Àíï\x0013\x0005åú+®C!\Fà}\x000f\x001c\x001aÅó;ÆwÀØëïäÚ&t\x0001rá³paî\x0003äò±4Ï/A\x001a_\x0002-æ\x0003\x0013ÞøJÞî\x001e\x001cÝ¢d¸CÃKà´N®\x0008\x001aí¨x\x001c>FH¸õ;Æw@i\x001dØh)|½DórÏ\x000e@wA±5âÃ(PôzÊaµj[Lz\x0001è.)N§÷\x0003ÕÙaÍî3Ç\x001e&¡º,ä\x0000¹K7<DPbÅìF\x000bYÑkaÖoA\x001aß\x0002­<©J¤¨oiM¼ÃTçA/\x0000ÝåÐFG\x001aZt§ LbãÆ'\x0004Ñb¼*ã\x000b¦a7\x0016\x00172GRKlÚ#A´]\x00105s\x0004¤bq G~\x001aº^SÙ`Gv\x0006hN½\x001fE¡C\x0013\x001e zÒâwîH^\x001c4ÅCtH5MþÐ?NÌÔÛNmw$/\x000eäÅ¾\x0006P\x0017V¿Ú¡qP®àÞÖ¬\x001d1µ\x0003¦v¾gzSu¼ÁMæÞ¢B\x001f15fzLByqfTÖ¡M¨\x000cÝ&Ü\x0011S;`jÝ\x000e\x0007T[\x001aÇ®Tj²Ö¶IQî©]gj]Tÿ\x0012P\x0014maïÓÚ­Tç«\x001dpµ
-\x0010½C;Ü$T[\x0016\x0018+jR¡Þ\x0017Wj×[R\x0014ºb/ R=@»ØÊ\x0017$ÆÄØ>JL3-\x0015\x0017¢-ß¢k³\x000eýÀø.0:ï«\x001eò÷pün|~«]:\x0017\x000fòb2>ä:¤,ª6|¾=þèyñýyÑ.ð(ê´/ºCKÕrZ	í$Ñ\x0007¸Âç\x001c<E	p\x001dnÐvÎGè#ÐìæÌO¢kÙvù#9ô	n0÷ªWA)fálnlï¸?C\x000fr2ØÒU{NèÝ\x0012(¾Ã\x0016 ðGbè\x000b\x0010]IV´¬æ <ú\x0004ø#1ô ±`\x0010Þé\x0018\\x0012ÃÀw[â)\x001cIa0pNZÎÄ\x001eSBt>\x0012Ã\x0000b\x0018 !I\x001dQK¡ «\x0007BÐµÕÌ#9\x000c\x000e.1ÑyTìHjwÈ\x0012^ZwO8Ã\x0000rh3\x0011xUÓ\x0008-ï6\x0012L»Äp$\x0001\x0004Q| \x000c¹:uøËG±Ï¿ÅÂ$øÑ&ýþÐüxù=hêÔ\x000ea·\x0012â\x0015=_.yér\x0003u\x000cþ
H7øäÚjXj´\x0002Ñ·EduN vÁ¡ô¡.ø2 ¥`|\x001d
©Ué©ípÞßÜ\x001dºæ/ß·F«+\l\x0011N¿ÂÃ\x00197e\x0016å Ö\x0005uü\x0001?@W3¸þ¾ÎÁ­\" ¶²3\x001d0íE¡\x000fÀ\x001fÐ\x0011Mþ\x0012\x0002\x0013mªðsö\x001b÷\\x001f_ð5\pA·ZNwH\x0010û8ð¦Ùfh|wþ\x001d sn¸x\T¤è\x0005\x001d>>G»æ	Äï^üËíë×7÷¯(¥ÅQü°´æãS&Î¥>ALõYåuÍ0]T¶Îêg\x000f+Í
Ú\x001c°]¾6\x0008êCjç\x0001\x0005¼k÷,ÿ@\x0011LÝBÁQ\x001e¤\x000fG\x001bN\x0001\x00192. ²Ë\m¹#\x000eçª1°\x000cwñXãF3»dèt\x0013£©\x0003ÉsÉ,\x0000wÕ^ë%wJr%ÃPg\x000eÇÜ&	ÍF\x0016Ï5Vä\x0018éé¯þÿgî]-;+Á_Iã¼Òâý\x0018R©T²b\x0019M¢±°"®*$\x0013H\x0016)3õ´?¡¦5éÒwðOúKÚ=öÙ'Öò}3yqq\x0004X7Nl\x0008,_n6ÃÐY|©kÓ\x0012 CE¥Q
Z¹x@K\x001b)Àm`r¸ÉãÕ\x000fdq¡\x0005ï\x000b*})¨dz?\x0007y\x0016CQÜ¦ÝtBC\x001a­Ç#òE',¨°âÖXô>ÙÅ²ÆÃ2(ÄÎTÄ´\x000f/rØ¤¤X{x\x0014T\x001càfzGÛ¦y/WöÚ-bßÌ\xVn@+äRÇ1ìãVfOq6®bV>¾Ì*Añ'ûy-2wª\x000b0UoØüÚ¢Î\x000fm½\Xu{§ÌwjqØ?¬È\x000eåµÕ\x0019÷ô:#\x0013¸Þ©!;U=f\x0008{b.8ÊR=æÂ%²4¼Õ
oÈw+/XñULµÐÑÀÎrÝ^ª7ä<UÙl®9Qpé¢YðÊ]oÔ\x001b,3; F­º®Ðq§Ô\x000e6×t¨æ¯7ê
¹Nd\x0014¨ÖR²g\x001fÖ\x0005.ËF××\x001e~@ü®\x001e"ÞOY3\x001c\x0011×L{\x0011ëÐÔ^¯Ô\x001bn¸¥!¡1Á±)\x0007GWjôãuÙ\©\x0007ô¼Rsw\x001dmyL¾Â\x0015'ÇkV\x0015Ðmiâ<	Çâ9O_Y´J04²8®\x001fÄ¸ÑD\x0005äI7î(^®·Q!^ªfVù\x0003æ£Û\Ö7èyLä\x000eÄ`Xun1dÕX­.\x000c\x0015Mýà\x0006=ÏÄ\x0002³kW µ¼Dûá¨¤é\x001b<Mýà\x0006
\x001ci\x0015ÍXHèWU4øªKñÐ\x0006¸:,³~ Ð	³Ú*\x0015\x0005-ü
Í1|
£ø\x0018®>c±\x0016¢G\x0014	-1{4\x0006t#töGiCwæ±\x001bA\x001cGÔåÕQ£
%¥Åâ[Ç²-ÿþÍ7G»Ëûçã§Ä*'Ýß9äQ¬~rÈ%à9\x000eî_ ·Þ\x0001i-ão×üèïÝ}ÅýùîÕ{x·Jè?1í Õz\x000fFÔç&Ôó¸_<¡¤ÏÚuãùT§4cà\x001dÉÓï)âôwðñR\x0000\x000cÁd¦\x0013«¡5E9Ù¼C¾ú­ßß#+¦Ì©Ú	f¿ÃÁS%jm\x0007d%!?­\x001baÖ\x001bÍFìyÉø<cñA.Ü:çÔÃ!ý»^åÉ¸=Õ)ç\x000f\x0002_ã§WÃä5ý>LÆë\x0011;vìÂ',\x0004Ë3{ÿqmê\x0004Ü6qSÇc,\x0019\x001b\eÅÞxÙ«j\x0011àvX¯
¬®ìÝbsfsÛ»<É¸<²bõ\x001a1dÅÎ8Ù5î}d|:Ø(Óà´a¹\x0011´ó¼ËGzwãô$ãôÈª+z­¹TòLT®2\x000ci\x0014\x00006>O2>Ï¸á ùT	]ölÌ\x0017ô¹d\\x001e9|¼©íùk¼æP/(\x0013É¸<cÑ)w\x0019Æ%æKô\x0007±áê¤x8)¡Ïtzå\x0017Jå%\x000eävÚs&nÐíg?&¾Cÿ¾¨+\x0003rÿ¡ÞÐ1\x000eèç¼¨\x001c\x0002ÎaÑóâM\3¤\x00147t\x001b4\x0017qÐ\x0002¸\x0012ØÐ½\x0013oe?.è\x00187h|«2òX³D©¬:ÆÂ¶w$â¯b£X*2£ø± MîLÇCïù\x00187h81¥c²4o,$s?Ëº÷¤\x001b4uÍHo«:Å.j.kÉþ=±á\x000c¶§ü3F¨b ÈO\x0011d.jå<èKÛ¢Íù\x000e \x001fÿTã.kÕã|ogÕc÷âòM²>¹ú\x001c´GVßxõ\x000e±\x0006
åü0IõÛuõkEè¾ú7°ú\x00087ÊX<ÙKä\x001bö¶øe\x0014\x0016úN¼ø¿ÜÚÖÊN_Ò»©V«ÙÑÊù\ñ\x001d?Ù¶í;v\x0006vö¾ýððÝÃÛUà©Ýp$«.ÿF¹·ïtm©\x0004rÆ_¨¹WNÒçµï öX³Çç3Þ\x00183ðs}\x0013RZ\x0005N\x0001\x0019î]ðÔµâÒõãÓU÷\x000eM\x001eÑ\x0005§6x¾wdÏW@¬Í8me\x0019½!ûã)å\x0013Å1æh©tÜöí;4ÒdT+2\x0003Û\x0002¡£¨·éß¡&£@\x0016
Ò\x0012Q
ÍD±ä°ïß¡&·ª\x0010<mrõ:H.fÍCÕoÓÀC3M®OÉc\x0007ì¢cæÜ
`t)\x0016.8©\x0006û¯es\x0004¢\x0012¨ë÷Ìu\x0016ï²ñL÷rgUN<«á¿ÄU\x0012Üg(Kè.ñMuV"¸ørH#ÀêþÚ°½HNà0	Â\x0001kãÒ\x0002íb®»nÝ;2TY\¦ti4\x000c0ñ8,9\x001a»äDFZRB\x001f+ûNE\x000bAf7ÚÚ\x0005,§\x0006\x0012Ç _-ßy#xúÔ×Ì²	Gãùy¹0?N¼ÛöBÏÙçÙ üjðJ\x0005\x000b\x0002*C\LDo\x0008a_kä0nZ(H@ÂþUÊÄ|H\x0005¯¯C[¸\x0008=NýTEn¯\x0011«¡¿æUO\x001f+=í\x0008\IaOM;O»ëð\x0008¥Sõßß?|÷öûgôªäh1],¸pþZÉéWM¶\x0017Ò\x0018\x0010ëø¼¶µ`.Ã±ææG"\x0016~/ç$VÞoíÅRu620\x001f"Íë\x0015à\x0018£ÙÈ}*3\x0004cU\x0013`.¡qø#17#û°ï.\x000bF¹GÖ\©mAõ®xÍü.û£àµ)J\x0005câµå\x0011qÈ*(kÖÌfåâî\x001b\x0013ÿ/o>\x000c{y¦ÇÞ·f[´ï\x0005\x001d×=å!kf\x0019ß\x0000Q-Z\x0003W2°Ã\x0018
¥W®1ö<}Þ÷ýGóÜF% (Ä^30çT÷´½Â£}íåããÔ\x0004u#d)\x0014gyß\x0019í¡Ô®\x000bBNÜÕ§?ÞD;«J* C7ÀÞ4\x001e5«í¡öPjë\x000cdÜä1½\x0011=\x0014qðýÖÁ4À`Pö=vèGË¶½Ò¡\x001ciÓ5\x0003\x0019iÌÀ ¨Óí§ôä
úlÂÊÚ/H³\x0000\x0006±>\x0003
N®gÓ\x000c\x0010L¼ÓÃEZ=^ÿ`	AÆ*xn\x0014O>à(0ìHÒç	$´ü`$HæJ<9\x001bL«?(\x001b»¬Ì\x001d$¢\x0019\x0018\x0001´\x0013<Es\x0010ë±\x0016\x0017\x0012°*¤ÿ\]o\x001eVÎ§Þ®{5\w÷Á©\x001b\x0004dæG4ñ\x0012·kêu3ànc¶7Ý«°;¬Y¥ÁI¸Ì\x0012°SÛu£%ëº^0Ò.7êM÷|È»ÏDÛ®å?¥´utÜô:å%ÇU\x0016á¦f3¨`©M,>w$7\x0017e¾:\x001dÝ¶Å¬­ó«»`SEKPu*@\x000fÊsÍ¶Æí\x0011úÏWí\x0011q×\x001eqaÕ«lÜµ/h"D\x000fÚ\x000cCT3OÃ§ÔRúÎµ\x001a5
aõß?äEè|\x0018äÚ÷Tê\x001cÍ{s_HQéó$:Gçq­rÆÜ<ñ¦ó´om/yqCkE\x0007àhú£3ú\x0018V\x0001z@\x0006ßê/\x0017ÝdÞ2h	\x001fé¿};¶÷¹,ÅóSÉnÜ¨\x0015Ù~R*Ù\x001bk&\x0005?úKw§sÓ¡£êß<WÜ\x0013t)}ù\Ï\x0004Sir+&8òáe\x0012L\x0017âø{ÑøÚ¯ùÑß»\x0017-®§ ó'?û\x000cô×\x001fÿå_\x001eÞ½ûÓúÇ÷v¤èø q§\x0007=³`J¾>({è*N}W\x0015$¤¤\x001c3zÐõ>+v³¿\\x0017Ú\x0017%°Ò\x0016|ñ§ïÿÇW IúË?ÿÇe¤;k´f9¤cOÊ}oR\x0019#+o\x0013å®øÔûã¨'÷I¦à¹C&uZtºdßÖâ´¼÷¿í \x000ekìY
Ì\x0012\x0002Þ¥æ\x0005»²\x0002DP]9ÂnG\x0007ÆGÀ¡ô]Zj	Ìzã¬¯Ü¾Z\x0008/ô\x0018ü?\x000cÞ\x001cÌ/\{÷å[\x0010ký{ù?o>\x000eµÖ÷oûí³\x0019(uo¤Xj9u=«¼4³"Ô|+«¼¨æá}Ê@ÍZ\x000c´Mö,?Ñä%5"dËO?ØzÖ@\x0001{\x001ah-G}æÄn1`IÒ´Ù\x001ao\x0011ö¼3uPCìÃ.Núäu·´¦\x0008;ýPìr]~\x0018¶5ûß~ýíûûW|n3Ë¿{_ýÃûÍ§\x0019¾S.\x0016¬&ÕïùÕ,_÷~ûÈ3+SyY»÷½}²pnqóöôw¯ÏâèýêÃÃ·Ã=X\ë§î¤+<ÕQÅ¿ý>¥cB«~üÓKn\x0014÷õô82¨ãø>gIVr¢ô¶\x000eâÝJñ+\x001eg,&7óÔ¶RäF\x001d~YE\x001eïíråÈ3\x0016«7ô\x0002IòºÖ=}ªÝZÕ;ç·¨\x0015ìFb²;fÉ#òZ\x0003\x0005àæ.z¹\x0000®£ä«6;\x0016ÂM}uªãÎ©\x001e½D°bÝtjòl¶r±¯Í\áûÕÒ5\x0017Òwp-»Ê{×ü9 Ï´Ò\x0010Ò<ò:Ï\x0019®@!ÿ¶Pé\x0001yvdëXÄ\x0006kV	®¹ÖÀûÜwí\x0013\x001a\x0012^)û¡q?äÔ\x0018]¦é\x001c²è#±è¯Î H\x001bn¯G/5å\x000fÀó\x0008¦&{J#SÉ\ö¶£Æ£×ûê\x000c°á ü§	XK.mS\x0013è£"ä¯\x000e!\x0013´éóÞJ%Ð*ä¤Ò­eáê\x000c¬aõ\x001dprð\r¨¼ä£	ïê\x0010ªaòÐ:¨Álw¨\x0001[7cd³ýÕ)\x0004UC%\x0003áYqh\x0019.S/»@¯£ø\x0006nÞ¸(Z§øÍÃo×"ÅÓÈè)O%¦töÕ·¨\x001ap÷\x0019PÊ\x000c{q\x001fE"¼ôÉZð±YüH6í¨O\x001e\x0016ß©\x0016\x001cÃ<ºüðì×Z0 ¬\x0014¤2u´}Â-ÍÈvH:eÜÖ \x0014\x0017eý-£ï·ï\x001e¾{.'(;
AäÍnwñå$_¸gxï
å%¾p\x000c\x001eqìqF+PÅ\x0017WBä'ýÝ\x001b©d\x0000\x0000\x000cù
\x001cù\x0015ÍÚ\x001fNPßz\x0014d~k1Â\x000b7È§ü<×°F/·f\x000fÛpúæ\x000fï\x001f+p}\x001brÓRÒ0ÉTîÉð:¿ô­Pã'«\x0018ÇFK!$ ùêÚ3Ñ|åw#5Yw]«\x0018</ s¢ç]\x0019\x0003¿Dï± ´½w#\x001b£,Ù|æyÛ¸4¶{.97þTÞÐæÍì8Ëý$Èk'KY2¹äEþm~"\ÝÌ\È6K={Q%iÍÙ]¸¡ÝÐ¦DÄ\x0000ß	>Q]gþ~C\x0004{ãFöBï Ú z¡Ú¨Ö:¿Ç\x0007´ÙÀù\x0005g.ðêÈ<zÜ6çÞsÿó\x000fßýñÃ«|øæË7\x001f¿z. W~\x0017K\x000e?<sÚÑÏó\x0013p\x0008ÖäÔÂ\x000c\x0006n_¬½ò«}×¬·ú
8§áÐtOæè<\x000b ÷eÌÏ\x0004¾ßQgüQ¾¯\qlÈ"v
¥XÙ"	\x001fó\x000bW\x000b>/)5áöjß®ýÑß½óÊÀé^Ùw¯~©ÓË¾ývÇ.~bVÜÄâ%{rJë3["\x0017Ü§Túý)yÞÞzÞCÒ\x0017.éR_G¼J\x001b	¤ë\x000f?&©X\x0016\x0008#\x000bD§&LÑ9Ý\x001dÓÑÙHÜ]ÿ@ß]§~Ô¬z)ß~ÿ\Ù_U}Bo.GwÞ¤7z\x0007j
mð\x001eÿú'muu|µIÂýÚ\x001fýÝ»ûÎN×2ÿÃ·¿Ö\x000c¼1Äµ@ú\x001dæ%h
;3\x0007ç§tÕ%û¾]ûõÞí~ãÝÿJrÇáÛ\x0017ë(ª\x001eµîàÝ\x000cµÜê~¥?m¶¿ú\x001aë~Í´RÐÐ\x00034äöÙ\x001b0TýÄ\x0011M\x0013X¥W©èyCÅOYÙP\x0000<K~-Ã2Ùî\x001cH»%eJ\x0004Å\x001a6ò\x001aGÜg½¯\x0007\x0018\x001f,ÀáH`N\x001bHÈ\x0016d\x001fÖùÊ<«}âsOÖ½.¹ÙÖ}J+ÆâÎÖ}¹²õ_¾}6\x0016òÀ.0Z\x000boÆ~s\x0018J_%þTó²Xú_L¯ÙZú
xZzqÈ\x001dÝô	ûÄÜÞ­Û~ö)jÑ»7øÓú¿Þ|ø?³~ÓTv´¢»Y\x0007/Æwç²¤ÒrÓörÎ¤Ä_³\x001fj\x00004f>;\x00183\x000byÊ¬ù\x0016;ÿö/¾ÿç¯þç¿\x0002§è¿½ÿþAÜÕoÞ~ûý«wr¿{/\x000fª¼¥ß/&ÊÎÄÓã&s(xkËé\x000c\x001d¼vÀO®eèÁ\x000fÕI¿ÿÇi«ýÅsËØÀ}ÏØÊ\x0017Fc|Ã]±Æ ?{£ÄJÐaB§\x000c*¯AÅ¿CAèÅ\x001cÝÑ¶¶Ü\x0011vØ±\x000eÍ\x0013[Û}\x0008;\x0015^vX%S	:Ó²§:Mèzæ=-»1òFæ ë\x000f6þùÒý±}¼(üêý÷o?<,Éó'¼ëNyîýt!5ä\x00045Ð»Ý_Ðâ]­¤Õ{e,¾i\x001bV®¹K´xï04Õ_½ò\x0007\x0008zZ|ë¨|¥ÉHh\x0010è\x001eÙâËÊY"è»\x0003ã«Døü\x001fUÍ\x000cxÓô©J\äXÒ&vXÍ/>h¤ÿ|vSH9[üCx©\x0013w§&A¨­³ÛûcÛM\x001f­)²{ën5!ú\x000cÝæ¡úÃ)r®$¶ª®k\=\x0001@\x000e\x00139:\x0010X\x0014äc<ãD&}zEÞtÈ\x0003rÈ\x000eµ*\x00170½â5\x00072Ç¸\x001b\x0003\x0000È	3´-ªÞBdäLÈ%­ùD@¾ß¾A\!è\x0012ä5oA&i	E«~
 ×¬¶6\x000f§¸Ë|ùÖèø\x000bUf\x0011\x001b\x0000ÇÑ>Çá¹\x0002\x001cPI¹!kZ\x001eû\x0004V	6°¹êÇS=ÏY÷tSÅ6m\x0013zCd+t\x0006eC\x0010tM7£nÆ^\x0002ò<(û\x0003þèÝ°28\x0000y³ÎNb2¡¹ÎG°¤LFä¯\x000c\x000eö,®Èì«E7¤ô	rco"¹¾áp\x00002ØsÀÐ\x0002¯Ø3n\x001aå+Ãà\x0000Ü2qÅQ½ð4îLsám£|å¯ÎÉ$pH¬çÐ2±¨Äõow¹Ä" ÃAqÀJ\x0018u\x001e¤~É¢çE1A(\Ùó\x0014B@¬Ð6×Ê¾&\x000f'\x0012è~\x001b\x0015nó®xZ0ï*Æçé«R=]yïÒÑæ\x001c\x001eÁ\x000f\x0006ÿI·È¢\x0016×5áGBõ¡ÒöT¾GòBWX¿u\x001eÎ¾áWo>¾úÅJ^}¢\x000básJ|k¹{Y²õ\x001e,ÔùÑ$ú\x0013ó=u¿¬çY;èæÊÂÝ`¤Í\x001fM3RÆ^\x000bð\x000cgÆùÖr\x001d\x0004äú	r06ÖmÕ\x0001Öã\
\x0011\x001eüN\x0013\x0003ä\x000fð«|µã§\x0014:Z5À¯~ýæÃ·Ïd3Ýw>ÞI¨ [yiÁ(´ÿÈ6ãÛ§y>Ç\x000eY¿S\x001eÐù2)?ÂóFãå7\x0007ï·&\x0013\x0018`H*2:ï¢¶Æ(_wÓè|}§£Ñ\x0003Ð;B '\x001c\x001e ß©ò«§­Û\x0019\x001e`P1ïÈ\x001eIO\x001c
{-Îöã
\x0003·Ú2\x001f_ýíûàùo6:^O´FyøËÔî\x001fµg\x000cO\x001c_2
J-|rpÏ±SÖ\x001a3\x000e\x001b'Ñ#·E~´¯ì÷\x001f)Í
f4fªF¢¯«_\x001ao°Í\x0013µÛ\x0003À\x0010\x0004`<\x0011ùâj$c¬Àuå³\x0001p\x0006`hÞ:b z°[ê&\x0006«Ð< OßîÂ<\x001e5­m¨â\x0010L\x0018#cî\x001e3[ÜqúH\x0017¸\x0010N(\x0018÷¢%¾¦ºKü²\x001d³ªýax¸§tbBG3³§«ÓùÑô»§ÇoæTüÝû\x000f¿}ûáý·K½õÉy\x000fº}Äßõû¨(×ÊÜ¡\x001f=í\x0011ú3¸Ùýl¥NêÂ\x001b7¿FK¬ÕÜ·eÿFølOejË3îÄ\x0016·;Þµ²}#¼*¡ãà@&5H¼Éï8Ö\x001czß¥ïÈpàC\x0003}&Ù\x000bÇáKm\x001c¾Èë³ú\x0000\x0019\x000e¼« ¶\x001cJî&éÙ1Ô×mÒÃÑ\x0012ãûeØçb\x001cCùl³}ÐQÖä7C dÍ\x001d\x001e"\x001fÒ¨5³ÿ ¡o¿¸MÌ\x0014\x0008É6Hå'´Ï8ØHó\x001e.ªVß&;áÍ\x0014\x0008íÆ¥Uk5­:zº´å[läª\x0000z\x001e@ZâA»3)'&È[\x001d¯2\x001fÞ\x000c\x0008ÊÞ`\x001f¾U{nCÞL¾\x0002äL[=_]-JrâOa8òKWv\x0007IP(]{áÇQÅKy3(Ã&àÍ \x0006¹\x0008"<èI{¿\x00119§Æ¥Éì1Í\x0017È\x0001SW\x0005½¬£^9wé©	~Ì\x0008Wû\x001c`}¤à¡ýÝG#õAny3;\x0000a§Ã´¦ì$j
²stwhÉúßá\x0001\x0000
G<z:,ä·GfÚ\xGCäÕVÇ¹ÕO¨/ë%½Wo÷4g;¶ôlÕè\x000fÚÓÓþÀÆ-A9á\x000fï¿yûí¯FDò7ïß½ÿæËç\x000bG¢êØ\x001ctÂS7¹à^-oí	N§`CRB\x0013
4SJôsî"\x001a1­À¾÷DÕ\x001e\x001a¨¼\x001cÉöµí\x0000Ó\x000f\x0002^­f\x0015\x0000ÖLÜ/ß(I÷¹2pÉ\x0005.Æi0©.­
\\x0018)ô\x001fÙ`$rù¬"Õ\x0000\x000e>\x0007Ü}MjQþ b\x001deÕ­Á\x0004\x001b¾º\x001eñ~ï<ÎPK"¿B=¯­§\x001clüêQ\x00053´~åK(Í.®ã×\x0000x:Ê.\x0017\x0010b\x000b=Ñ¦1ìùÎi¸BëcguêÅb¡F\x0005\x000eiCô¼æ¶J¤\x0002òtÝ­Qõ¾fRÀP\x001båÈXU\x001b¡ê¡BÅ¬\x001dûx0SçÌ<Ñqë(ßûÏ>qZ\x001e;h{?9Ø¨ÛB´£D3¼\x0004¨r\x0011Oí{ïÌ\x0006\x001buË\x0002ïsç~\x0002}M2Á7\x0013b\x0001yÚ³üÃë\x0002'Eµ\x0010Ð c,ü	óFÕ\x0015ñn­c÷3HÃ°\x0014×\üf+ \x0012æ\x001d»¶.âÅUdã(côÆÆ½A·	­,OøÅsè§G\x0008º\x001eQCÙ¹BçÂ)uÿ¤¿°¡ì\x0018ë[]º§z(£º4\x0002õÑhA\x0003@b4¬\x0006ø#¿8¹lì¦\x001anø£ò·×°nqX<ýÀ÷Ü2+¡\x0019á\x0018eOE0	¿É[+>¥®\x001aFïD¬\x0001Z³ç\x00109õ´O Üç»àÏ
õ_	øè×ÆÏoÞ?\x000b7àB\x0017!ä|Ú+\x0005×\x0001.#a°)\x0017ó,è<\x0012\x000fÈ!²\x0019ÃÆmµ©\x0017ÎÄú.\x0001\x0003lòM]x\x001eÊÎ¤t<d;jGáWÁ÷f\x0007nÆ\x0011¨Lè\x0016x/\x00065ró(ÜÁ+Î8e\x0014^¾X:CGjì·eóU¥¦\x0007K\x0002dT_ì
<ËïÞêWo~ÿñá¹.+YyZïªnâeVâ½/èãO0
¶ÖèåN\x0001÷X_
âP$ãÃ²¿¬­\x0008zq5\x001bï\x0008;±3§ùÐÌß¸f×\x000cB°±\x000b\x000bº\x0013»	Ã¡\x001bn\x0012jÿîÃû¯¾\x000fò<F\x0013\x001b©×T	GûI!w=9ø!zW\x000em2\x001ayÜç\x0004+\x001bÍÕÂ\x001fýÑ»3»\x0015¥ÿû7:Òý\x000f;Åá§2K¢!Yôt\¯d'\x000f\x0004Ç\x001bûruÙ\x00107,»nó\x0015ªT,þ`
\x0008¾4s\x000câþä\x001a5\x0010ß:Ç\x0001iU¾¥Î\x0007·¯âô\x0000<õ­~ô3í¯\x0004£3â¼¬\x0010#\x000eN6!çÎq_Uï\x0001xF\x0001òÏÎ[}X+YzvÕ8F«¾	\x0011
lFÃìAcý\x0005Ý\x000cã
ÔZö\x0005\x000f+Õ¥äQ¹/:¾&
¢\x000f¹S\x0016µÂñ\Ãúó?u\x001eIÊ¯ß|ÿöÍÇçÊ8ùdR¦÷\x000e ³T!Ë­U½ü2Ø¹ñóÌlEY8ò4ãegºRú&\x001ec§6äànÒ
ÞsÍÐ\x0017î5H¼vÛ\xÝæ\x0015äá\x0007?O'\x001d§@6	_.êo7hp1\x001c´øF1Kõdòûkj\x0006MdVÄ%×Ñ\x0005áP6<©°\x0011\x0003h´\x001a1ÒµÐI´ã"\x000cÛp^v´ãÎ\x0019 Ãñ º¨Îñõ\x001a»7t#7´µº)ì]\x001cG\x000fÛ\x0005õ¸s6$hï	xéÚ
ÁQ\¤|ÄõýzÜMÕP>\x0012ó»ªÙj0N>
Ë´j<0T\x0016\x0010\x0003{-T­¤Ó\x001fè\,\x000b[o1¯òimº§ú)-Í=\x001d"¯2R´yôü×Ïå2&S¯ñ]\x0003FìÀ é
mò|\x0019ÖÍdc@ÆÆ+M\x0007)\x0012KÅWÓ3R7Â­îOA¬1Ü%~$>Eed.¸hæÕþå\x000bßØ£èòñÕoÞ¼Süõ×\x000fÏÄ®+SÉÕvúÍN)§g$.E\x0019ô¯\x0017³Èæ>/xIf°6\x0003B\x001fÒ\x0016(ë|FEíªIµ\x000b4]´@üzN\x0019óc:)<H)\x0004zKýÂ&Í`\x0017¯ù¹köäRÄÞè\x000e54Ìê«Üï¾ëÚÓ'²fYÁÚ£\x0001ò\x000fÁÑÕ¥8 §KáFu	\x000b6tÎ²gä+\x0007÷<ãÏ2s]>vG\x0019Å¨:+>|Ý{\x00147Üû\x0007Ô\x0011>P¶\x000fèF\x0016ý\x000e-·.oF>äs×·ù\x0006ç\x0003\x0001½ê"bÃ_\x001cT%\x001dMºoÈ÷§YÎ¤\x0003bX]x;qdÑ#ß¼)TÜ §q\ñGï\x0007=*W[\x001dæV«u\x0007è\x001e©B&\x000e\x0004å£\x000eäÕÁº!§,\x001eD\x0005ûÐr;ÙG®l\x001fÑfß«­\x000es«K)\x0010fJvtqNèDe=¹JÆc\x0016¯V\x001dçª³l@\x0000\x0003³Cû\x0011\x0013-ZÉ¥|µè8\x0017­V<\x0013q¾È?M«\x00100\x001dÃtxÉûçÌo³pk\x0004½Û\x001f¯<É­È_RBÛ]\x0008èóüüÝ»·g:èþùá\x0019Ûi\x0002ú©wÏtÀ1vÎºaF?9\x0017+\x001ae2qyJ+(G£½ì#
\x001f÷<úh\x0014tÊ°Óï*sãz5Í7Çt»õ6¼\x0001ÏH%\x001dÒ\x0001w\x0017«R%¤¸\x00112"A¿ïô\x0016îÀ3È\x000esWUåÐ3\x0002\x0007\x0013\x0012½Ë|¤µîù·¿ýø°DüÔb+&;×Ú=b	\x0012Ü*ú(wqü¼ùd	!La$ÍÌ\x0007¦=d\x000cUÃïs7d¨&L9É"Q
lk	»+f8de_äy¾/ËWµÒ»îJ\x0008>unI«/\x001aÅ}6ÊÛ\x000f\x001bÝ\x0018£u«=gqÄ\x0013Ø³îì0ÄA
Åt\ÂyCÌHºulX\x0016Æ³½ØëG?ÓE~Õ¸ª|}K¥DÞ:èÈLÍîíP\x001e\x0007:hT°h½r\x0013í3'øn½V;\x000e7)-:|òlypÌ]
Ý_qp¼Éh=qÍ´¾qº\x0016Sñv¢×g\x0016*
\x0007áavºA#ºq+C`»+Þð¾GØ¦-ý@Æ¶ôÞ1ã¡\x001bÑ:ä\x00112í\x0017~ï3\x0007ã3\x0007/Ç;qÕS·kö{§9\x0018§9HhJ½9i$&rd}h£Íeã3\x0007ã3\x000fÑö~3\x001a*r·l'äâåÁé=µ\x0004WSeÚZ\x000e¬¿sO<ò\x0007<ÿ\x0001Ù\x001a\x0019P¿0ÑiwFCö\x000b\ªCíøÞ<|ûý«_¾ùþë·ÏUOÉÅ4}ûéUÔ@b\x0000½ûà'WèÅ>\x0011­¡ðê^\x0010í>\x001eÆ´\x000bÈñÚÎ¦kÙ\x0012ªtÍ3­2ÖL=X¹³²¬yß\x001a-¡êâ3>f\x0001ÛRg´*¯ò0PTr,õ\x00059#Ï\x0010ëg\x001b-¡Ê·\x000fÅY\x0015ô§\x0007Âò\x00069i}á£áS	nB\_¸6[\x001cóê%¦Þ2¬ÄÅÇW¿|ÿñÝs%Qs0µ¢XÓé\x000fzå®\x0000}UsÁù§Ö·s%äö9WB\x0003-Ç·z°MáG\x0012nóÈYY\x001eq¤ºlI\x0019ÌÄ\x001cívÖu°\x0004 Ï$ª2Í\x00089á ©Ae³\x001fj\x0015\x0005d`!K\x0004î0-Üé\x0015
÷+Ç²Êøù±¿[mËA»}øþ¹b\x0014qAx\x0013U³zÆæ\x001de?Z<¼ÛãÝÆü\x0019AÊ\x001b}¦M\x001e¤°FL0-¤½2\x0019<ÅQ¤´6yG~ô\x001aé\x0002k¯Ñ\x0001è<å¡\x000b\x001b¼ãÎ÷G³\x0015\x0010H41ýNyPÍgJ»F;2¨f(\x0003\x0006HÈ>\x0013!FÙiI¡ï¨6wäùþd-ý"#¦ã\l×ÿAë³ïÏ\x001d¸\x0000°G=¦=\x0013Ù\x000c¿y~îÀ\x0013Ò©^È´i\x0018\x0014g:<S©;e;p\x0003à··2Ô\x000b}¾¡{q( Ø â\x0006:FV¯\x0019\x0015¹¸cb\x000cÜãEo\x0014\x0010~á\x0013$²þæý÷ãqSµùgª\x000f*G³Ò³>¨£jf\x000bOâjLb}\x001e¹ñKÙ"¾F®\x0016þèÞ\x0015hqº	vy>_}Vn0\x0016MµÏö	%\x0003¯º\x001c,öØþë>kübáþè\x001d½÷¢ð_Þ|x¶b7|äµ\x0004­+:6ÆÊüT\x0012¸~)%èd\x001fH\x0003¸ÊÜnhO)®£e\x0001\x0018\x0012þ\x0004ô²,\x001f5áGmÍ¤.Ü2\x0010jx^Ë\x0004¡üæwoS\x0003YÉpN®Åß]=G\x000f½ÔÑø;V¡Z}¿ðGôú¢\x0010\x000fêÇPÐjFDvN0	Q\x001cÓ\x000eÑº /À¸Øzë>~¹0®\x0016þèÞl}\x0005ãÿ1HòÝ4dI&'e©QQw#ñW¾Ð¬ý¥lù\~\x0005©þâ2gÚC³ß5øÞq½Ý=µ;'Ï±¤oÆY-qsÄ¹ïG`PMs´ï3ù C3ÐÓ­ú	ê#¶$\x001fÊAq¹ÕÈÄ_u¹Ì¸\x001d`pGÆäCãa
Ê=$\x0016MUá±Íûw\x0007\x0001\x0003ÍSB­,ø\x001dQ\x001bî9b£;2Ì\x0017È	ãZ«\×±Yì¢ð?ûÔT¯uXËÏì@°\x001d(r~'§\ÉZ«A\;¤öêiåj\x0012ë\x0013EüTLøËÈ&\x0015þÅ_|ýý\x001fýwØô^/Tóæ£â÷w[{\x0010Ãö úÇ\x000fbª\x001eãµÜ \x001dm\x00127\x0012\x0006 ×¡2hXÎøÝ?Ê\x0011C\x0012øñ{õÜ+ºY5´sVv\x001dÕVÐ\K5TG\x001f·ÍVÂN\x0013;¶;sPí¦ #\x001dï0 »´z¡|CÙë\x0006ö¨éþKF¢àÊ:Ô\x0005á¹â\x0010¦wUGWe¡ÝhXIÐÝØ$Ï	»Î5\x0017\x0008ê]]|b»Ì;Ý7ý$Ý'¶¼\x0001wªI=\x0015Æ§ÕÒ$O1[·S]Cì{\°UÅ$MlíN(\x0008Î'âÈ@ùëí¾s\x001e/Ìc§m¥<\x0012v»cë
:OM¤\x000f
´Cé¦ñ£Õáz»ýÜî¡Ù<·;é`uÀÿ'ì2ð¦êØ÷º³ü«\x0015zÀeá½b2QÀ\x001b*#	x>À¯¿å¼ÊsíPuªú\x000eÃë\x0000>2\x0014±¤ºVµ	<ÌË;Q=ì
q@´¥\x000e{Æ¶\x000cZåõ¶Ä¹-µDÜríj\x0019W\x001e3mKL}øÒ`Â\x0014JÄò\x0003Ba³ü¨Àø\x0003|'{Ô\x0016aþÆCGÃG¤àÈß(írQò_|ø\x0017¹v}ôþöÏÿñ»7\x001f¾\x001fµ7ïÞ¾jn¸¥ÏðêéàSúr=óÆ\x001c\x0003Ö\x001f\x0013U\x000bÔ¤~¼'/äÑ\x0015f<û,\x001d;e¥Ý\x001fû©Ç\x0003pËÓqíwý¿ýÝÇ\x0007ò×Î\x0006¥xûÝG	)¾þððÝÒÑþDO&{ô®[ÔawO[ï/¬8êë?âw­ÅmÆýÙïzìù®ú¢fXu8ª2ó\x0017çF¼\~óm\x0001{~Û\x001dyt7ê\x0003a·];ÞÛðÅ¿î\x001c%¹Ä7³b\x0010ü^\x0010pm+\x0000l³'©w^\x0004\x000e\x001eú4Êñ-ß¾úÇÏåRg\x0004Y\x000b`\x0011\x001c\x0004ßekxÚíçSË\x0017Ü¤¬!:;`I½Þ>¤¼z\x0018#ªÛ\x001bè÷¶\V\x0011\x001e@\x0006¯7{\x0016¤ÈßÒ °:Ô.mìû\x000e\x000c~XìøðyÕÇ%F­\x0006xqãôÞqÁåU/¸Ó¦Íªëè3\x0003÷U\x0007§w§á2-¤d\x0015¹tãJßqûüxÞÁ\x0016«J%Áy'JÙtfOäy\x0010³\x000bZ¤\x0015×È+6{áüÊ6\x0005èéxuM\x0016À!ïÄâÐ(²ÅÕ¸|\x0003h\x0008\x000fo³lî\x001b\x00128<\x0011ù¦º!CQÊ_;ßÔéDBöäÑoD¶°mÚ\x0001\x001aÂ8_gq»\x000e%¯ÆAmfè\x001c7êÈ\x0000]ç}êÊ\x0008	Oèæ\x0011;oF8Zá®ìyF+O½4på\x000eÝaÅu\x0016äëh\x0001/\x0016mö9¸Íè¦	=c2Ì*¬$\x0012\x0004:ÌPñ»På\x000c9'\x0014ì_\x0013×¸èÄ¹Úv\x001dk\x001cæ[\x0004êc§éETº\x0010ït\x001e¾:,a\x001e\x0016¯\x0002Î\x001e\x0004<Ä¤=\x0004]oÐW%À£Òò¤&éGÌXöU\x0017sßÁ\x0017\x000cW¯Ê]ßZV-QwNÔ\x000c'\x000eÆE\x0018wG¸:¡ÐNCF\x001e\x001cÔÐ¼\x001dýèÐ½:.\x0001K§kZ¼\x001aßø\x001b²§×wÂÙ\x000c§eïq<ê­ìØ\x0013:ÂiQFyÐ5"½LVÝøqÑ¹áÿ¾hr\x0003ô<.\x0012lÃ7ê<£ÉÍQÞªôc|éÕy\x0001®ÉúT.ü¶È;e\x001cßmW6\x001d\x0013qÐ@­}É\x0008m\x0016åý8:ãéEp×\x000b4ÓêWt¯É£.\x001c	>F¾Å«û?Îû_ûPã´ª¢Ð,ñ;æW5]z&²'pÄ½êîcº´	\x0012A'?Jóååiy£-w^LÍ÷×h\x001d%ó5-æ42±W\x001bçFëÀ(@V-õ;Ýx£S\x001füÑre\x001deZGv 	+È1à$$\x001bÈðR\x001eÔëru{y{È!ÇÖg¥ëvÜé^h?$R\x001c\x000eïÕN×¹ÓE[ç\x0010:\x0000Ç0i\x001b/\x0001\x001fb³a\x0019\x0005o\x0000¦ä\x000e)s\x000e¦\x001d'cã;µÅMáæIÛÉ¯Þ½yønÄ?Ï\x0013ØíëBÖþz£Í\x0001å¦Ô§ÕÁ.Þàfßà§@o>+Õþë7¿ÓÑÐG\x001dúáÝ«¿{ÿQáçÓÆ\x0018"_ 'ñXC÷\x0004Ã\x000bxOÛÆEf?ífÿYöüp¯*xnúæÑ+W8`W\x001f\x0001\x0007c3®ÂhÐ:Di2ùm¤¬\x001bY×	Ã\x000cjl\x0010[\x000brâêZ0n½<ùqWó9¡gÅG ûdyÕ1@| è<?ríP¸Ý¸È,!þÄUo\x000cÝoî¯_èØ7\x000båâ&^cbmw'@»u¦\x0013 .ô Á½÷õfã£.\x000fëm6ù¹d\x0015pB\x001f Ñ\x0018Pù¹%®:®<Ï¸­SÀRu4*ZK­ì¶²
8\x00030¸Zµ S[â§\x0016*áC4bÍÙñæì$y6\x0013,¹\x0015lEÍ qpòºp\x001fàTMB·)ÓQu8"ÄRè&÷·RìÆma\x0019\x0017
M ³«\x000e\x0001$ÎA;*ÅF×Ò#1øóøê£6Ð¿XèO<;â\x0006²CYN}\x000eùªZ\x0016Ló\x0006(i\\x0008/qvJêäÓ\x001e[4ì\x0005Â+\x001c\x0011"kHò£ò:½/\x001f\x0017¦\x0012 Ïè*zÌûÈnt*\x0012äÆq[\x0019\x0013ï6ç½ó\x001eµ@J¸\þ\x0001ÞÙ
ö\x001d\x001cÅ¨xûFö]é×ï«\x0012¥\x0006Kc
áYiÇÈe44\x0017ºi£Ûjv)¦d\x000báûE?úw»_7Ü×ô\t¦2\x0018rºèYûìú\x000c5BL,¤ócò6"è\x001b¯ÆæÝç~ç2E& \x0012éëÁ­\x0015\x0000\x0019ÒoÅÃÕ+È\x0001q8\x0007ìÛ:p\x0007¡¦SÛë\x0004EæqúPÒ}gÆQNëdJ@ô[<Ü¶;©;\x000cSÊ¼æ.\x001eæjË:\x0011\x0006XÈ
ÝÇVùÖßxáÔ2\x001f÷Òæ\x001eµ×\x000b§¶²S{É¼\x000235ÔE3E*zQm¨\m\x0010d7\x0013¨!ª\\x001eî³OäY©\x0004ÚfÂ\x000c CËÃØRåµE~\x001d|¢Ýð¡m9Lwä¹ÑJ§I\x0015\x001b*ñ(Æ1)\x000eÚß®(P¹([KÖ\x000bÉeNÝ»Nµ8¦CÈnW\x0015¨\\x0015ÈUÌ\x0003ØKªÛpÑRBIG{]T\x0005ª½²»8Mp\x001a»ÇÞ\x0019ZNm[îÒ	Ì%9ÒÀû+b-¶ºðc\x0017ùÅÁ\x0018_='¹§T
AÓ\x0018\x001e?^5e?]û¨\x0003\x0002þªIÍMÝÍM­E\x0017ww/£øjô\x0006´bÎôý}Úù>­.) "¡ô\x0012DÖ\x0016BB\x0016·Ë|H÷³O2´ßþááÏÿÇªX
vÞ±´O3b\x0010SäÍCÔzkhÀ1Æ>Evº3|x\x0019OàiG-/Ð\x000fÿâV°ÞL>|Øt|¼3e÷¸)Ë¬¤ÓäÂmäÑºG\x0012ÿÊdÌ÷ü£\x0018ôÁ{¼ëèØ%\x0010uß\x0015dÝr\x0005Â¥§¿\x0019\x001f®\x0018\x000fFrº\x0002N\x0000\x001cç½$Àêy\x0010nëÛËÊ&\x0001à\x0002Ày2\x001dt§3°cÕ\x0012\x0003£¾*\x0001n\x0003\PÙ\x0010\x0013÷Ôú¦Àè\x001c¨ánðÒöpx´;xnr\x000eq\x0000teè\x00186ãø\x0000:Ð¹\x0004ä\x0018pþÜ8Ïåáw\}@~È_=\x001a@/¨³²Úüö¢DÂUz{ÏÙ\x0012\x001c÷_}xøv\xÏuØ;Q|ÔðC;÷ \x000e­æ\x0010~©Ã®)ÁÏ9ì·\x0012\x0003\x0018KH3u+/+ÐÞca[~s>Ü+ä8U¼\x0007N{Fñ\x000bÙÌ£~t3Ó\x001a\x001a\x00010Xau3\x0018P[AÉ1%t\x0019à]^\x0011ó\x001dØ;®+>¤j&r
Ñ\|ë4\x0018@\x0006óîÆ¼¨®ÑÍËª[
Èu®9Õ¡\x0012w"ýÑ]Ëß,\x001eËöò»!ÏËÏûtF¨\x0011^çH¡%·5\x0017
À}\x0002«ÃT`ÉÍ,9ãÞñ\x001bë­z@Ã­ªÓÔ'ªÒ\x001315¬_0næÙ\x0001ô<(*\x0007E©6	¡«¯Æ867'%Ý5°;\x001d%\x000fÈ$©ÛQúþ¾¾\x0001Ï¢¾¨#¨:7\x0011×ÜyÉi$W\x0016
\x0017vhN7ç'ºêÈ³y,Ã1)\x001f>*¡õ¤\x001b»KPü'}Ds?AL\x001e÷pt^½Ðí{ÊºÊÆ\x0010­{\x0016cgg§á­¿Ùñûî6jT<Í%f?ÙD/Aö|zäj±9\g³7·ûÿû¿ÿ×ÿß¾{øîÙ\x001cïÐøWæx¾ÅU®ÓjÐßL
÷Ç}Ãhôz<éïf.êL6Èº[IõöÊ@i<ªa<ë\x0010\x0008ÀôÆ\x0007°t¹ÊÉ-|F[Ùáçz5¢ñä\x001e'ò\x00077îqoûWó}_ðÑ¯¿³ÄU¡ïb
Ù\x0013­°­ë­ÞÎ­M\x0017\x000fÀ¿Üõ\x0012Òý\x0019F\x0018­\x0011ÊBÁ¡Èò:GÞz~3âá\x0004m..î?ã¼¸²¼ -0ráÝ\5¾\x00018Â¹©cñ	¬C)°ôæ\x0015hyÕ,\x0003d°ðÔÑ«/òP§Jß¿Òf$W×\x0006\x001f@.\x0013Y§\x0003MóÐ~C÷¸&\x000eZ¯\x0017~\x001b7*(ó4M	EÎè¨4M$eF>úg7î\x0015w\x0014^×\1¿/Èã¿\x0014\x0016|÷Å/\x000e\x0016Ò©]ñæÕ/'óÒ~ÿ<§²F¡úÿ·
S,:,qz-¹Þ¶zó%ÄùÌ²C|t®ÖýÈ/ÞÜ\x001e(,³Ñï¿½ùöÏÿï¦õÄgÙ³×\x0017N]1=¥Àñ×Í|?ÛßòÞ^[­ß-²l1úH¯²Ïì÷ÇÁ°ÜdSXjQïC\x0007\x0001V'#oosßwo7³pýáÍ\x001fäÇé`çú¦ÅÜËõQ×â`õÜ¯Þ8:?þº\x001fu}å<OußRy÷uWdµÊoÎ_ýSäÝâj5¸!ó-S\x0001)ÎÄ~K-V\x00020|:cÿþý¿-ÉúâvÉúÓC÷òen´ªÜ­Ûå\wø-Nü/eÌ`²¾N¾Ù}	y¢^¢bymè÷~~÷¯ÿãûü³\x000bOíÕW\x0012;üçÕcÓ\x001f¼\x001asxÜå0û
¥£Ö]8\x0015ÚBkÚÔáï[ÔosÇ¦-ëþq\x0006Ææ]íÍøÜ'2dUí©§o¯Ö9Ã h!wÌT\x0010\x001e¿××Ñ¢\x0019®±ÃÄÎ÷\x0011ocCBAm\x0012õçî$¤c/Ó*_KÐñ\x000e]S½µÓ\x000cdßP«Yîø+Å²Ö\x0018\x0008:MèQ1ÌR\x0005¸Ú\x0011;uö\x0010Agî#	vBþU\x001dÍJÐâ\x0002ÙãýEý?ýkù\x0003¸@o¿{õó\x000fo¿ß¨4?ÑÈs í=¨õü
*Ã\x001bï\x001f5*?¸ô\x0017±òÃ'\x0015\x0008Ïí1V~±èGðÆÊ\x0001;üPlk~\x0018¶5\x0018yeÌ\x001bÿ+yÝ?¼}õöûW?ÿö+ù~óðöÛ\x001c÷$ãi.§{;â0â|ï\x000f=´|>z\x0000t\x0004¦o/a<IÎÞf¦¶5\x001eÝ*6¼;IIãÌÆH!\x0004l)ðuPÖx\x0016ç\x001a«;{QÏ\x0006ºë´¡¨ðmàÖéi\x0000\x001c\x0001¸\x000eú	¬Î?.¹FwzLmU÷\x0006ä\x0004ÈþLb\x001f\x0017\x0018¥ÞuÉÝlFXk''²XF«Qk´æj®Æ°Â\x0000ä2K>ã|KÛÂ=ßç³V¯+¬9\x000cõ\x0003ÙaJl¾ßf\x0014à6Øåü\x001a6YûÈ\x0002}¾ÅâÂR9\x0001àN\x000bv"ö¾ésá\x0015nø¾öºËgOî@.$\x00124ÚîxÍù\x00183zu\x0000½E\x001fÚ\x000e÷E7lÖEGþ~ix(þê\x0004z8:O\x000b åy\x0006\x001du]uâ/¸©È\x00000À_P9ô\x0005«ã}Nc^¿:\x001eN AaÉrÔAÿ³9k\x001b¥lf^\x00012À\x001aÎi\x0007r#Fv
Í8´\x0002® #(7\x0010îsKÈF?ÚS\x0008ú&÷pu\x0006}¥K´\x0006.(÷0n¤ÆÐiÓ½\x0000Ðp\x000có½úu@Ó\ÑGâ\x0019z$ïüÕAôV\x001dËîÄÌ\x001a«Î\x0004Ýv
\x0007\x0013:ÀAÌª¡
K\x001bôpu\x0012\x0003ÄÒNrÝ\x0001]ù««®l|mTÎÃÕIðR\x0016u¶\x0013*´VÒ=AGÇ±\x001dcy¯Îb³¨ý\x001a\x0008í\x000ctöü\x001a¶1Ë-\\x001déÒ\x000b\x001e \x0013võëa¬l!ÇX´«\x0013\x0013àÄHðØ# 7è­
\x001ewyÝ\x001bò!ÌpubBE\x0003¸Á\x0007<²óÜ¸?ÂÕq	p\äau°äÅ	\x000c­*\x001e«Ä\x0001@wÚ\x0006«\x0015º\x001bdÓi'Ó7#äÏÒù±è*&Ì7ur£Z\x0011¯NKÓ"î\x0000x\x0007ÞÔ \x001c?)á\x001fñê¬D8+ñ¨ØÞ¿a\x001b
Ö\x0013ØçÌ»\x0011àÃÕYÖa;¸;:ºx;Â\x0018\x0017¯\x001e®\x0008\x000fW¤°Z' ñÃåª\x001eÝññê\x0018F81Óª;Å«¦³r\x001b¿\x0013¯ac¨\x0002m\x0005Ã`dÎX§WÞê8*Cñê\x0018F8·;'´JQÃë\x001a\x001bH\x001a´xu\x0012ã<\x001aeå\x0005ObB\x001a¡±úaÔW'1ÂIÔÞ\x0010¿\x00113\¯Â[Ý~Nº:iD9Âgã\x0001Ý°B\x0016M\x0019F
+nSº:ÉÃ~\x0004|\Tz¤Ðvxrl²\x001fwiº:i\x001eEíÉpVL¼á\x0011WÉk^ó@®Nb'1DÜè¨:d\x0018[hc	!·á©§«\x0012¬¹\x000c½sÑÄûtÑd\x001c²ïz¦«sæ9\x001cáü<QÅIÑ¤ÓÔ"; û\x0007®\x000eb\x00071¤n¯\x001a\x000bÅ\x0017©\x0007ziuâóªb\x0002Ð\x0015v:%c«ICU·ÚÜÂ¾:	\x000eb¬gïøXµàqIÍÑ\x0019Ïe´Ö¦«æA\x0014ïë\x001a«ÎObJ·-Gòê æy\x0010µiw\x0002\x0007í\x0005!`óç£\x0016~u\x000c³\x0007`ÿ\x001a|Ø\x0003ËZG¦\x0015Ô|u
3Â\x0010ÈîüÁÈ&\x0006Èmô3å«cç1ô\x0012OÄyì¼hNaqßå«cá\x0018ªâ\x001b\x001eý;ºh\x000ekó\x0010\x001aÌWÇ0gX³\x001faì¹fM`ÑëQ6Ò9\x0000\x000cÐS'c,9Þ6ø4:)åhoÏW0ÏC¨å¥é\x001c$¹HÈ
Nk\x0015ùê\x000cæ\x0006»ÑñºÓÜùn\x000eñõ«Rà¤èdkØhÕÿ´êÜÙ8¼J¹2é\x0002å¶ÜÈîÄå#ç1N=À\x0003úæÿg«Ëq\x000bèò\x001cÑmCw½\x000c\x000e\x000cÄ.ì÷ãµýþíË\x0007÷ïÇ8ó=/£Aï~(qB"ÿ\\x001aé"~\x0008ÿ\x0002ïÏÖËñ\x000b49_67ã÷ÕCóãú\x000føÈ Æ³êÈx~K	\x001cJßäÁë#?¡ò_\x0008\x001cØnü©9òíø	Ù\x001d"y×A>3~'E!i\x0019RM~$	=qJ1Wó0\x0005}ä#8ó\x00110Ã*á\x0019%ßKó\x001cSúÓØ¯÷GÌ´uZÕíôä\x001cfÇfê\x0016¦ Ò`­?\x001fÕ¿ó§7\x001f¿yû\¥ä\x0003ù®åYZq\x001e¢B_s\x001f·þ\x000bVRÈQÓ=2¥0=º!Ù\x0013ÙaßÈ\x001f:CËÝyÂ¢;\x0010!é[¯\x0003\x0001sÊçB\x0005\x0000O~\x0013¹:Ås\x000eä¦H¶îk]{ê\x0001\x0019<g\x00189Ljc3è¦ñhíòfÈðfû|rlY?ÃnFdß~\x0014\x0017û\x0004®øñ àuè-%^­3àS\§k\x00032xÍÞC)H6Ñã´6.):\x0005}¸ Ó|"Óì\x001dÄ^Ç®\x0017r`BÉf3ú¶þqúÆk¥9\x0017â:PÓ¿sÛÖ?Nd8%ûýè¥°­Ðá.úê¨@\x0001D\x001fc?i%5\x0005N\x0015'é\x0010ºC&f­SÐàÞJÜÀ¢½)ÚÄÎ5H
·u\x0013ºü\x000c½ý2o"Q&YÊ}\x0013´?æê^\x001d\x0017¨S¨öQ÷\x0000Mîm+\x000c\x001b¶%\x0013µýÐ\x000fxuT B¡AÄôõ}Ñ0\x001cÐ\x0016xý!{uT B!NÂÉ\x0010\x001f\x0016G±ð¢i7ü-ÕuT @áïã²\x000fZátL,\x0018\x0007*I­nÔ\x0016\x0000\x0019éo	í¹È\x0013Èèª«\x0004]ÌÇZ8¡ã\x000f]ô\x0012bÈÿBÎÞ¶<q"\x001fìwñý¨×çUIm>µ%{¾?bÅûÃi7áØïßww\x0010Øï\x001b)\x0003ï­BLË\x0015\x001eZ3×¿Àñ/Ð·ÎWLg·w²òÈ\x0014µ\x0014Jxä\x000f\x0004þ\x0003O8û«ãÚf«ï^ýêíÇß½{P?îyèdµ&~VËM¦\x000f]ÒúCy\x00116YÏí38ºAK¦þ\x0008¸'-¦Q\x0003\x0004\x0012\x001f?m¾¸\x001dì<dµdò\x0002µ8l/Í¯³KÕ×\x000e.@\x0006ºä\x0001þeddCò\x001cõ÷õé,3%À¹GÒÓOß¹ªss\×g¾ss.ÙCàêüëV\x001cÌsÝzÄU¦\x0004ØwHÊ%Z,8\x0005³ä¼NÄ\x0004ä
á '+ÎCXY©¥;eU\x0002ä>\x0003¦!e3ºYs\x0016y#:¡=³¯l\x001aÇ`	\x001d9y*\x001bí÷Nà
\x001a¬N\x0006\x000f}J£L\x0007Ð±2´_é®kÙo>¾{õ¿yx÷öÕ?¼ùö»µ÷äÑu3\x001f^bý|^¶Ùõ³El8JÓO/C\\x001c	Ï¸§\x0016âb\x0001\x000e<\x000fµµ;ãf\x001dïÏ\x0015p\x0000àg^µÕ(s(ÈtM8¸^\x001b±ÄEUL\x0003Ô}gÖC­L\HK\<§+ô}\x0007àbHïlôw¤î;p¦ÍÀ4Fwl¨­,F¹¸¦,mQWÜç5Õ %»Í`O@®?Ð0Öh¤[Þbªåì\x001c<ö"óçkÎóý·x\x0002Ï`$5¤%ÈÃP±Ãi!V\x001c>Û&lï¶¨ÈÐ³¡Wv«\x0004ÍYj_Ý·xBÃùkXx*±Í)
Ð8{Þâ	=O vJ7®#ïGN´hW×àê\x0004BÜZ='~\x000cd-Ù¡ÕÉ¿Ç[íêFü\x0007 á\x0008¶Ä¯Aç_ó½ÄÜ÷ÔÅ\x0013\x001a\x000e¡òç c;ï\x0007×ÊÅÂ/\x0012\x0002Ý\x0012\x0017spP\x0001k¿rÐ2\x0013¼ÜmçÕ)®9CZÇw]ÖE7\x0003\x001d6£d\x0001\x001aÎ¡|µ\x0006çÐgÎù«`È&ôØ¤\x0005º%.Êsô\x001a\x0003s¼!­ø¼É
tË[Ìrô:|Ã9áÐ=»8\x0012¡Å}Z [Þ¢¸É{Ñ¯y?\x0000"\x000f¿ßç\x0005ºå-ª²@¼Ê.c\x0016TîNöÇ+{u\x0014!/ê¢¸ä&BÕ\x001fÆ«>&ß^\x001dEH\x000cè\x000fÈkr'xZ5S\x001eÜñ¶l2\x0003Ý\x0012\x0017\x0015Rh:\x0018\x0005o=wL#Z't
©b.\x0007DÚ à8NùÊ\<\x001bo\x0007d3RÌ\x001fÑ¤3zÛLPÐÀ/Ì1cÉ èÄ ÚÕgÍc=¿ðÆ÷\x0012ðÕE¦rª¤\x0018mHh	J\x0000\x001dhÕ`ÔZH¼èD®ãåZ	'r¤o×M\x0003IcÒ;¦9¯üÂ\x0013\x0019l:\x0002`L\x000bh¼Ñ!ò:äÕë\x0002ôÂ¬\x0019f\sb¾eË&íÇ#°ò\x000bOèB\x001bÝÀò¢)aKHÉwpîW~á	]iÕ\x0013¸¼Ó9ñõá\x000e*çÕyíòúÜ¼M.4-½ðDç¥÷sXÐ@.I\x0003r:8\x0019Ú\x0007\x000fdå\x0017Þ _3Ey\x0004"½/®åÐ#[ù'´'/\x0001nêMØÒ;riË/<á jï\x0012Xµò-\x0011¹ûÊ'ñ\x0018)µ\x0012\x000cOh<\x001eÏxvfÍw£$ÖÊ/<á j¦\x00066Z"g~m»±éC·ïê \x0002¿P÷\x0019\¦*\x000e$\x001d&ÍÈµîù'4\x001cÄÒàm).1ù´\x0007Çðè\x0011[é'2Ã»(à±hÇ\x0004¢¹\x0006ij¥\x0017Ðp\x000e+ò-}Îwº\x0007dk»Þú\x0011._\x001dD \x0017ªuEÇÀv×B-|Äó]x\x0003ÎèæÝGG5ËÛÂn^pdÑíHì¯üÂ\x0013\x001a¡Ôå\x001a
5é¨?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-07.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ºf+¯Xñ\x000b\x001bZ¡j\x0014Úf[\\x000c¡ë´f\x0013WÔC\x001bzFÿvûpÿþ­öê&\x0007èZîQÎ³aØ¢\x0001Û\x0007rêæóSëüÚA~îxJ\x0006ëG'zUÃÁ+¯]#?·$E-kã
ãï¦õQ;¯ßBÓù¹]!î/ã)ÓrZzõ
\x000fôË±3ï-<\x000e
\x001eÌÔe¡ÐÜS`&ã7>àã\x0004\x001bÇp\x0004å±ø\x0000P\·z¶"å®5ì³u;ò¼§òÑ\x0013}BÐ°=6®ò^¬½×\x0014!\x000bü \x0016ïOd6lì0\x000b\x000cÒh§¦8ÏAú²Õ ,BÝ\x001d\x001bBÝJC\x0001[Éí@\x000eh3$t\x0002³\x0013èÑ\x001f°\x0016KósñÓLµÉó/áÍ¡C'\5ÏRêGrH§;Ùk·üÙ!ñxH\x001cUýkU:yv;ÜÅmÓkV\x000b\x001d\x001bçùE¸5ÙÑª\x0012&\x001b¹U·¯òý
\x0016òýÍ©6Á,ÊÊÐxÃÌmâë´fE ¤cã\x0014ÌB5èIm\x001c\x001eË8yu",\x001cô
\x000eºS\x000f\x0011 Ì
Åg¹6Q c=)ø÷sÁ¿V\x0012 fÝZå\x0006væé\x0018r6ÍúîîáT¹¾|×*Ã/ZÐb\x0008@,>®Û1fr¥;aó	ÛÂåó`?Krz\x0016)t&gÏOgqû\x0015§_¡¿\x0002¿Âia\x0019êÄ2\x0005\x001bÂ4*Ì»- pú\x0015vò\x000eC\x0005V\x0017y-R+ÃhðÇ¸JFU(pÒé?ÿ½E|?}óù×Wc]È\x001admc´²·\x000e¯êö<±IìÂ5\¼WÕÍ\x0001_íf}Ïß«êx¶Sñ­¢~EY:5\x0002´ÖbhÖyhÜMkXÓåNz^\x001b6ö¼Ê*ÁCÙÆUÉÓH*ÓÞ«UL¯cSx¢ÊPÙan=ç¶©jóÉø¹
\x001aÃÉÅ\x00029´)\x001a#ì\\x0019»Ï\qZ7h\x000cûf2jª\x0016{QØwÒtQ;iðìØ£àíEDiÕO\x0003ìÜN[S§p=vdÓ\x0014´ªVÄàUæ²ÇÚÓà+Z[7ÙèÚäªNã\x000fe\x001aQÔ
ûl'\x001dîäZ
<ªBNìÓc3v!¦\x0019½µg½q qÅë88Ñá0\x0000ÌX\x001acY\x001cS\x0003)ËÒI\x000bfÆ\x0010~ÀaÖ\x0002\x001dgó4³HzC÷jÞoÃ¦y¿ò7\x0010Û\x0015N\x000f\x0017OS\x0011t&;1Ù;6ìbV³mt°
@Fî\x0010\x000bó´#£yê\x00032ÚmEÃMÚÔ®$¿»\x0013ka£´å\x0000âF/fè0\x0015¡µ}Ûy_¡q\x0000KPö"«N-l\x000cÇÏòªmkC\x000fgG;àÑ¦\x0002\x0002\x001d>4Ùcµ®$²ª½ìØ8ÜöäË¾nÇÅ	Éîä\x000fõ6h4#E\x0019b\x0013Ñê7%\x0016Je´\x000ew­L[·\x001fà{\x0003¬\x0013Eówt'§Â{Ûj×eIG®«æÙv>A-­¾\x000bII~z\x00176&eÑE\x000f²y*ÇÜ .4SÁ3¬¯L\x000f_¬ØÌö/¸/\x00088Öººi"g<Y]\x000eQêÏÏù\x0017øù\x000b*\x0006±5`hø\x000b¦\x0007®Ö-Úpþ+¸\x0016ëÃú¢\x000bh5îí\x0011sR,Ï«1fÛÄ\x0014\x0002Éw¬ñ#KE|\x0006É\x0011ñ\x0016ÒóØ{Ñ\x0012WÈÔ3^¿èiÜ°Â2ÅI²Õ¯#Ä\x001d\x001a\x000c\x0010QÄ\x0018¶Ìd
SaBS¤¦»\x000c\x0011´ñI\
±j üXøl¤Æbz¹Ô²\x001de[7×(\x000e?nrÀ;­!É©ÒKoÄÂ[,Æ'¯n?o¾ÚÊ\x0006_©µZ\x001d\x0014\x001bs°Ã¹q-\x0002rRñÍ\x0003y\x0005Sö¨Fz\x001eÃ~ô\x000bó¨(VY\x0001t©ú\ÉÕ^|üæþíÛûë\x0014N©ÉKÆ¤©ì[#Î=\x0004xøäµlA®öb¦å*ÈyH®ë|B(¨°\x0006}
¹iRioàÂ³ëÐ\x0019¡Ät®|æÇI×U7Û$N#\x0004ñSed¡æW-à$èØm\x0005µIÃ¶Hm\x0012#zHÑQdA\x0001h\x0000èU{R½Ò¡ÁiTac)rk\x0011ûHíÛlH»
7l\x0008§D5NJ>Lûè&²>#måýwè\x0012±¨´ãæBÒærÜüèU¸:L>ãÉ}zô.ÂÃ\x0014
×<\x000fÒ¢ÅM§Í\x0018\x0008Ær\x000b¯b¿
\x001b¹£\x0012\x001dî\x0010æ Qdâ;]û*[×&Zmºtå[§Úèì2Á\x0013<¯ÿrûêöþíµ,.å#
\x001awe\x0019CL£e-{Òshªô­QîW¤QSá4jT
µLð¦zº\x0008b\x00071ÓAéÁ»E\x001fKac.*ÍÞ\x0018à­r¦â´!ÑBÔÍ_9©PïÐ\x001e¡ðè\x0006®\x000bXÓTI\x0010@mTº(Á\x00115\x0017¿Å30«éUÎD=B\x0010mÕ£®ÒÛH¾®
zE ­÷zÕ3T¸5ª\x001eÈ kG\x001d
Í»Xm{VMZSýC\x000câò
Q;ãhüª(\x0018Ú\x0007£­\x001a4\x001br\x0001yd\x000f¾ªW"îÈ¢¦\x0012Ö ÞwYÚä\x0017h> \x0005vqâ:oü\x0004úP´UgYáxwä±ÂZ	O\çz®	ÚÛ÷®#\x0007@Nøz[¦»\x0018ó2ÔÜçãkç:ù\x0016'¹`WjXUlæÖ¨¥¿Óg\x001bii#\x001ddtpÛ´îH³§£éä³'ÝSÛÙF\x000f¨É\x001c¯ïª\x0005dNñÌP]	+\x0017È®
¹>}#
ó:%8ú¸ÓÁrmRãf\x00178"q5¶øúS?\x001duå¬¯Ò\x001cvJsX\x0017`´7ë#\x0017×i¿_<©7lÐH5©\x0003o1,v^ÄêUmÉ¢@q\x0016Zøú°cclÒc-cçßÁHp>ÛØ8\x0004WÛ
;bM«aãL¿9)\x0007ZcÕ\x0001Ù±yX\N<>.O6\x0014§ý
M;,H6lä\x0007v\x0018ÃpÞ1=AefÏàü6Lç\x000cz²X\x000b{+^\x0018\x0017ÇSÚÆ[\x0015ÏÎ_Dæá\x0005\x0005®Eõ¨ÊD\x0016Hie!éì\x0000&ä:5	«j
¦U·ZU3xFÊÐµ\x001axL(ôÙ\x0011IpD´81Ã6jÖãg<ÑYÓ-}Npß\x001cÒ\x000cG¤¶n«Íí7: ©
ê]\x0018¡
»w«Å	NëäÐ£_YÜñn«c#ÝVq8ßÃ©e@4=ò0ò\ÊÐ»YV\x0019¼
\x0019¼KýÔ\x0005[N ¥u[êJÖ¹'­	gèmØ\x0015×\x0001Ë6\x0008¢~G¯êlÐUÉ2\x000e¾i\x0013®\x0002	=½q\x0011»\x0006I£0\x001f}°J»ðÊâ"\x000e®-Ézxsÿ·+½«F¹Ô"\x0016Û.ØD]V¾ÇGeÀs!Nn:á\x0006vsÁQH[ÝSW\x0010+³8N¡êl¨B%å(¢i JùT½CCø*+\x000blB(L²Ì\x000eK®Å%¬]9NÝ~p)ÁVrX(¶·Sã\x0014cÚLî\x0015sÃ\x0006\x0002çk¦2Ìl|ò\x0017òT½bëâ\x000e`.¨\x0007×ÿéáþí»û6@õþöõ\x0017×
±Ç¾:®sÀ¾í¨þÔ_e£Àbczâ\x0003«¡bÆ®ü¨¨1\x0015[§VñØàER½CCR]g¬\x0000­qP.lÒ{!N\x0019V³x·t
NCHX`«uv>\x0013´á\r	,:î [\x0006\x001aÝ~q¥(Ö3qYª5ûg\x0018qÍi\x0008l7\x000få<£Õüyjµ=Q½m\x0003Ù¯rk×S;.Ð0ÐÈaå½üSâ¬cW^rûÓzO\x0012\x0019:®\x0014\x0006Íéªé}\x0016Ï#-V½ OíÐ`lð£ã§å0Ã$tÜ=âTJ5d¨&O[Çí7lx\x001b\x0016\x0011\x0003¶¶¸áFêÐ`Â®v\x0011\x0008èû· øZIT^}÷êÍµÂ\x0001Åp¡U2;J°:³æ§oj]Û-«K\x0016ùÉ÷\x0018°âmªèóÔ)%N|9¹dqêï²êÁ¸\x0014x¾`1<Ë8¹Öí~4.6è«\x000e-ìøÃ¥#-b¥¾BSçÉ-\x001cK~öeÃx;kûøì}án\x001a^È\x0015
²ðÐ{Þ\x000eå8\x0003\x001d\x000bZ\x0003e½VÛD¿0M±W&Åmp«&ß·/>\x0016;æë«±hô}¸°?7².
÷>-á©Öý+x×ÝÌßªe9\x0005|eSx¦¤e*É ,äëãÚ¡¡1Ù\x0002\x0007\x0002ÍýÃJµO.§3é¤Ó±C7«ì\x0000\x001e¢\x0007v\x001a\x0010ê¦Ûò­ÇxJÇÆ"ñ$þ=yÊ.p\x0018ÈÙ\x0016t[Í7lL\x0013{hòuN\x001d|\x001a>à§x^J~Ý±·A#]®AÞ\x0001ù^Ï!&}¢	;»\x0016Ù^5{ì{IÍ\x001eÚ¸ñ¨x\x000e«8S+ïg]E¶Ë"²Ý|pqFî¯Æ4uãi¹é:ÔhaÐ©jÕôôÞÇ¡a5·ª´è68\x0002\x001eÊ\x000bO\x0014Y©<»¶ôåÊ¡íØðæÔXoF4\x001fY[\x0012E.ý:ðbâÊKxÿâ_ß¼hD\x000f·_½¿\x0012\x001f\±Ìp¢$²xý\x0000$Ê´j¼µxíy.lã8ÙÆòo§ÏÉIr\x0017\x0005]Rª^¿Ö°\x001d\x0019\x0008/Mär§\x0018ÆYh"d2c¬jãá:6sFZ`¤µ	m\x0001m@¹tý*QÌòL}rÿÕÝ×¯¯5¥ÕØÎÓêö\x0018ësCêvòs<O+\x0012@Ã%\x0016¾3Pü2÷Oç\x0005*¦6aQc±Ac{J¥ñc©°\x001b\x0003­o3\x0001Wúo¦\x001fÓ.ÄULÓ¨­\x001c¦)uiE.joõ0}|ÿãí¦$¸\x0018©æN<ù=$\x0016µöjdÔ&´\x0019bÏ\x0013naêØ)\x0011<«`XÍ-Úe\x0011\x0012÷\x0000}áYÛiDhTÚp\x0018K¢iÕ)é³B
`Q×m\x0013×\x001fF=<uh­*_\x0002é¦°-Þé
ÛHb8\x001d¤F^§cPUMJ>kalwl¬Ø©@!§æZ¹Èã<Cª½:jñÊØ±¡aãVÖÔ\x000cdÄ&d\x001bN¦)vl¦xvì\x001f½2­MãD&n\x0004Oct\x0001ÇîT1¾©\x0014Ceì6ÞoA\x0005´a\x0003\x0015Pô\x0018ÕH\x0011ÙEZá9a7æÑEUæ
ò>·ß\x0005[{ýQÞÊ-OØåuÑÉ·aCN¯\x001c\x001cUÓn¡kX7-»ô´ë¢ZaÚVô
[©m\x000c´j\x001eÎÔl-zí:2ôÚE­\x0002\x001e3ëµ\x0008mtÑ¼jòª\x001dBiZÂþéÝëÿÞ¨X¯T¼®¬\x0014ÜS\x001f\x001eð@k]læ©×C]DªW²q2\x0016äðÙõÊ#AíO-8d\x0011j§_Ô÷ÆÉXð\x000eqÉ³2qsæØX0ñdwÆ>mGM[áÐl<CÛ³©Ø~
ý5^ÐéP`\x000fGZÇ×7hdC#Ö,\x001axÑ®pú9ëmåéÕÓ<å\¹\x0003\\x0014È:^¹Ac#«xWÐD\x0018ÂD)-ÐÓ(ï×U¤\x001b43hbý·ìÔÌD¨Ñ!á\x001d\x0019;â\x0005\x0019\x0007²ÀuQë\x0011ËÖ[=×¢\x0006cFúÌLóÇqV\x0002+W\x0001´â¸¼öðI«\x0019
Ô©Ê$z	
hàj°C9\x001bû\x0010Í\x0010¯'\x0005VdÊ|\x0002SGu<;V{»y^ht«\x0002À·K« /Ö&ÿQ6 2¿B0\x0017Âöe½é¶p\x001a\x0013':\x0004(¯Ú^à\x0004.¥m,Ó>.IßüGs{×¾¾}wwûþJ/c¦\x0006w¡(÷ºhtàR\x000bü,_Æ\x0015×<%Îå<#^«£Iñyî!	¥E¾WF~J\x000f»ì K 1ã±Ö43të9^½1óÀ5'6,¾1ÆpAÎÉàG·
\x0008_½\x0004s*@\x0015\x0006ÌL÷50É8'\x0004­T'úÚOúÚù@JUgÊ`ñEW¢mDa«jq?±ËGÏôYëg#_°­Vj/\x001aé×x`svÄ%Óbw~eãøf/C¢_Ûõ±Ì¬b¢fã'pWOéä\x001a6$¬\x000fcWï¢#V©ÈÁ²\x0014Z\x000b±\x0015í¼Än?\x0018U\x0004\x0015$Ú)Ø¶L2)+;¿Ô¹Âi;òóß¿{ÿÙ«û¿^+Ô\ËTë\x0017[EìfH}d¦>ÈàÉäËEø®¾äÉ#Ê\x000f\x000f¾±\x0013\x0005\x0011³pÅÎ¾ÝÕ\x0013á}NÍÏÀN\x0004s\x001bmæç*âXg'RµÚ?Ø¸\x0007´§$¡\x000b\x001bIÐÙªüÅ'Õ\x0019|\x000f-\x000f<¾
KYT|uhäo\x000fÔIÚ
À\x0008yj?ôélXJR½Ê´\x0003Ìðmþ\x0001ÓUDGç=\¼J\x001d\x001ay Õ\x0000\x0007WP\ÿ,ïI(­Fg¡;4è`v¦'ÏÑè-ÙE¸*Go5\x00077e\x001dÛË»WWG¤\x001d\\x0014\x0003\x0008±
ØÛj8\x001favr(Ï`lûIµÚb\x0018K°/§a,uÌEÏq¡\x0005fG¹kæ¤sÌÍdXEb\x001b4DbCÎXJë2?ìÚIÉM$òðuÙ
E:¹&´ø³¼i°+\x0019
:	4DK;6\x000cû.rB
¬[y£1\x001b+"!<¹æM,è:6Ð7R±~ \x0014ÃÜæâ<p ÖÔ\x0013²¢\x000e
dE¡ý@ÅsC-[TRJ«¤\©_Íè©ýÛ·ïÄ=½ã|¥\x001a\x001dÃå\x000c.¥²\x000fÖxµ\x0019´´±ôénÏò-\x001e²§,nÇóò=É·Ð3tøÉæjñ÷ÅkÓ¡áµÑ0v\x0002k< #\x0015Wê|\x0013ÅÝ¡AqkA1(îX
×è(?5ï`=©àïÐPÁß¨\x0005pXMúË*#çÎ\x001cµ\x001a\x001f§ê\x001fµñá%k´\x0019\x0004=q-¦Ü«
yª6mA\x001ep\x001b¦Zî\x0018z=ç"ÕãKöþÅ¿ÈõºVÒSM¹rÛ_¨Ù£\x0012/@ù[¨­ã9F~V-\x0015\x001d×¯¡PéÃ9#giÄE\x0010\x0017¤4þOÖVTp¼aÀ>rLO\x001c:ññ²¹²W\x001aÕ-\x001a\x0017ËÅ<§ã*q\x0005e2Y¥»í¬©ß¾ø§\x001f\x001e®V´_ÃL?ïÂ¸	ÄÀ­sÁLºµ^$Õìä\x001céDC ´\x0017«mÔj'Ôi&Ï±Kwä\x0001µésêÐðqRE'	t;ÅüOÄÿèÖ­«õ;4öÐF#¼efÖ8s£\x0013\x000fÊ\x0006\x000fJ"f`­¥¤úy"W¶}²Õ1bÒ±½·
Ý\x001dÐò\x0008«¨ý¹Óªð{¡×Un¿\x000fOZ­´I~\x000f=dyµF\x000fì|nöÐ?\x0008Ùq2ä×$÷Ë·\x001c¢ÂB±ÓÖ-téÜm£ýz²\x001cákmÿ\x001fuï²cÙq%\x000bþJàNzÒHøû1,²%Õ½ê²Y\x0005N\x001a
"DÈÀMf°"3Ø\x00024íOÐ¬Wß¡?ÑôZîûmægíP6ó¨#
U¨ø°ÜÇ·o÷õ°eÆñO\x001a¤wk\x0014°¬ôg\x001d*	ÆT\x0016\x001eqa!ëm\x0010À²F.KÍSß/Öàc@IÄø¼	Þtëövý×Ûî®d\x0017ä$ Î¼sgî\òÚÆßï1¥­¦\x0017g<\x001d\\x0002ÆÈj\x001foe\x001fY=ú=Ï®\x001dðNhÈû|îoöªEðÛBxrÙ\x001f|\x0013\x001aN¾äå\x000bØ\x001bTÃ_fJA\x001aû,Ì[:.\x0013\x0019l×Ð1¨"0Ò´Ô.¡Û¡"ú2[ô1!ãj%rãö¯@wo§ï\x001b4¤ïN³«\x0000Ðúf]xkÖJ0¾«ë2	\x0017Åc-]mèTs¯þk1cÔ#^ºf$\x001aCz!pxR­vE\x001dÙíô]ÉéÆê-mh¦[Ã/× 7R1Ò\x0012\x0013Sx\x0010¨oÕGÐûæ÷§¢ÃÆWíAä¤j«'Ìj²ýT7h¤p¥\x0008Ù¯\x001a\x001eS9@î\x0015\x0012ô<|rÞî\x0000]<ÔÅ´~GC$£/\x000bÚìî\x001c`{\lÉ\x0015w¢ÉÐÍ!%4µ&"ìRëÑðËtHØ·Èp9çnY5\x0011[]°\x000e
\x001bØx%\x0004 mÅà\x001d/wM¬øÑghX$lØ°Þ\x001aÒã\x0006ìl\x0010µèIÐµNºµi®yZ\x0015£:8\x000c=HÆ><ü\x0013ä5ñPÇ[öÌdÄÃv\ÖG«SÆH5/î?\+#-K»¶Ý E5 ù]ú\x0014Õy!³Á}Íka/\x0004jÓ\x0016ð½«¬=\x0015	Ô7§Ø§æ\x0006
4&{©]f3\x001cß Ý\x0010=e= ²¬BswYÑfO¨Ohd7ÈY~b\x0012B\x0013Ï­t\x0016i¨ÕäÉ\x0014kèdÈ\x001dÈ¹º\x000eµóà¹\x000e9\x0003J\x0001\x0001óVÇTðKÇÍæ\x0008ª\x0011Õâ]¢Q|é]§9	Ù&Ár¹%\x0005S\x001e\x0004º\x0018ôy£j)PÅ ºiSd¥`«_ºÎ3oNkLh,0òæ²}\x0000\x000eÞN\x0019]Ý\x00133,RíËÞ°Áñ)«Ëöp°íM\x0005ÞÖeE\x000e\x0004\x000fNØÀh	ä®kBfo)&~[Íóh¹QÀÏ©4\x0016®w_Ö$Ôå¹­)ÄrA\x000cùêþ\x000f\x000f7ÿüôÝÃµ\x001aS=\x0010*x h¼	u\x000cZòË_2\x001f©,ïf\x001bå\x000f~Î³Ka\x0015¢mÏö··7Ý>¾»{¼¿\x0016[§8^k®î\x0014Ämð¥^cWÃ¨e¦¥\x001a=b<ð TÂ\x0016ÙÎ¸ÅLÔ
\x00075k\x0010cU:òôËj*\èÎ'ç´\x000f²Æî\x000746ÞT\x00199\x0005j,ÌN),(O® »½Ø\x0014|þýíÛî®e`Üc_Ë¯»DÌ ¨ó+Û÷\x001a÷EU\$åçt\x001c\ÑJ&ñÖûb>Zâ/·(ñdsÙF{\x000fu\x001e±¤EÞ\4to\x0004]¹ÉÁFð\x0003Ú8ºy:}v'{éWÚMj8J£\x0010*Ær®çøÞ±I\x0019tnèÅë¤É»`è\x0015X-¢ÎÛ)Ëm=h§j¦¤&8Ì¥ÂîTÌÝ{k¸­/ U\x0016\x0010puÛ¹¡qgTcæÓBCËCíbæÞpàD\x001e:¬<þ~`Ê³!órtX\x000eyÛ(²ªëÁ\x0004þîj.\x0003\x001bk.Ê\x0016ß½\x000c%'\x000cÔ\x0005á.´D`´Ø\x001e\x0016û`[>»¥õ1J~\x0003;@ÉÏ
\x0004ú\x0010T«\x0018ÛsR6ã\x0018®´\x0006|'t&hT\x0012udï8 yî¥\x000fÆ9\x0014:°¡\x000c¥õ2|lå*âP¨ÌÏrêÔip¨V«\x001dÉ/ÿùîñ·ò­]Ë9BSé¾\x0018©ä°çÊºbrH¿øxÏÇ\x001bGÔe¾'ê·»ëf	La«<Iõy¤«Õ\x0003éº\x0006D²¨É©Ð\x001eË,\x0017#]­\x001e\x0010ë*ý¨BÎà±ÝòÔ¼ön\x000fzÔÕuH\x0002qtÎÎÊ^ ¿eD\x0002Æ´¸®®C*#yç ^åÃ]w]< }­®Czx¡\x000f2Å©ìÔ¹ý_\x0004ç\x0016fVËPm6E\x0016/_cþ@iÃÆÕ\x000e8=?\x001aø¹Y\x001dYV»\x0001£5ñ°&§Ëâ¼&Sî\x0016HÍ®M°!è\x0015¦\x0002/A/\x0004Ì\x0010Æ\x0019lT|\x0006tÀOIhßËbß¹(\x001dJ\x001atñè.\x001fO
8?\x001c1\x0018ìI¾òKa\x00083ÿ±fîN_<\x001b?Ê·Xþß=¿ÒÚ.¤S§àë¥÷æùù\x000bg&â@pH \x001eÓc¼_ºáxîÂÌ¯¤B=¼ÿ÷§k\x0005­¾U2¹øó¨Ú&ï?ÂË¦~
²¬\x0007¥\x000e£S³ø=\x001eýg×Â\x001aM²ZÃO*}öîJ>ôÑKÚÍü¿ÞÏaµG(E#/þVlé3ãlmo2Õ\x0000_\x000fý5ÅÓJP®+q0\x0016¿!ïï[Éf\x0010ÝD¾¨r®~¶Ú\x0005Õ\x0012óßßÞÿt¯¿óJl\x0000\x0016R,§Vä¼e\\x0008'Rn£´þ*»ZFA¿.\x0002\x0012ñx\x001ci5q\x001aVÂ¢üÓÓ\x0001§ª.sÿêà.Mõ\x0013\x000bø«*mä\x0005F£.sÿ*ÃÄ V\x0002M(\x0011¬0t<ÐRØ ¥ss8þÝ$r!³¤ÒØ,©¨±Oá\ÚÊf¿z¼}÷íÔ\x0019¾RÊQW±ò´Çº¨Ã<"^¯x0+i\x000bcE÷!©Â-\x0002w\x00120\x001fxa[ùFXóJ¤BEæ\x0019mv´\x000fy&ÝV¾\x0011Ö|£"S@él#ý\x0000è¾@\x000f\x0001Q\x000b_\x0017*DÆDÄ®Ñz,	Xp\x0007óð\x0013æá3Ø·\x000fÍ\x0015è©ó\x0002=Fí­à:¬	\x0004ÀPT\x000fE®\x000319BÊQÂ\x0011ãdAuÂ_áH*¦VÞ!Âc\x001b¦ÖÃuà\x0000¾¨Ð\x00113äöX{%T#ô­\x0019÷×ÍòÜüo·?]M¯UþðLäH¯ã¸'.Õ÷=\x0005ô¥Ë\x000f\x001eÅ«Z\x000c\x0011.YÄ¯IË«õÂù|(=H:\x0001_ZåÌÊ§<¶¬1Å7aÏ«3a¥,$©\x000f%²>öh:\x0000\x0019g ÿÛþü×ÿû»·÷ï¯7>¿|@»CHLÆ K~Å$\x0007c¼².\x0007w,DÙ\x001e\x001f<^	F¯|ð\x0007¢
&Æ\x0013-Us<²ÖÂ2^C³ù8iåãÄð\x0002½ôPÖñ\\x000f\x001d#V>NTÝ\x000e|êÈ'`ó\x0017¶äÍ¤}lÐ¨;\x0015;épÕÄÎÃ=xr)í@º6U\x000e·æ\x000c=¨:¨\a¤\x0005)|n'7É*\x0016îôà\[Ð³!ÐÛäIzõiåõ¦ôËÇÛ?\­¬¶«kX9«l«r\x0016Çi¤¼|Sýc\x0019u²ü¥Ñ\x0005ß£\x001cÓLkÁÆµ1)	
v\x0014I\x000e»]NB%\x000c)ïË1É¯Hö\x0018ýÄÆ1z\x001d:\x0016Pê<+â\x0017ò´Ú\x001f\x0010~êBøQ
y \x001a\x0004µÝs\x0004í©/¬b¡øEq»jþéÝ7÷wïÞÝÝ|!\x001bõZ7Ne\x000b=uïÎ\x0014ïe\x0008â+ðË>
3._¿P:t\x0011Ãú¶\x001aÕA+e´\x0014{Ãú¼FÝ\x001bQ\x0019¢nNpò"º$9®5dyÛè\x0000Ò£,Æ¨\x001cØo%Û\II±»ÚµW)ÚþòqåÇÑ~díötÄ`\÷:ÑØ±B=SäÒta´f4\x0016
zôaÙE×82ô`;Z6´SCî g&ïÀ¦Ã\x000eÍ#\x0018ê\x001cgå)\x0015¿}tûÝ¼ï~õö\x000fßÜ_[[_B©]u"ªZ\x0015¤æ²þ/^ÃøXn¬ßÂí³Í³\x000ba¼\x0004e%Râº{ÿ~>å2	\x001f¹8\x0011wþ\x0018ù\\x0000+¼ü¹þ±ji-.\x0019ÚSÔr¾ÔòÕ®.¥µº\x0014#1±åk[´q×<zoWÒZ]J¿Ëh\x001aá\x0000òâ±\x0010Mv_³¥O¿xU½\x000fZYôyä\x000c:g¥]Îà¢«^Ô/Oàýh»\x0018ÑZ}S 6\x000f\x0005GwéG5ï\x0018\x000e\x0002¶Kv\x000fóôAãDÀgd·¥½6úÒ°I{§ÎLòÄJmíÌ!M\x000fG\x0013	}vûx=À\x0012YÅ1ôm\x000b¢´V³KN2½Ó<7£ÅdÓo<gïÁ\x000fzv1F\x000bå\x0000»æOÄ6¦ÌÌÑÜ÷7_Þþáwß^ËAnqF\x000f­÷]û¤å¡V´ý¦\x001cêïÁgÈeßL\x0016paü¤pê£éz¹/E`.D\x000fÎî Q£¡LIó}V;´çBN
cÓ9'4kÄ*KK/Q9dØ§ÙËûè3Ó`×/·\x0010(øõ¥µ%gprvÖ¦ôT§BÆ«<<.'|~ëÖ	 æ´ç\x0016 ü ¥kG\Bæ(~\x0016íÂÅ¹´Aý\RÁA;A÷N\x0003Í7\x001aé÷º­Ñ?o\x001dCCòöññþîZ)«¾u\x001a\x001eëý³fù{¤|ÐÃP(~i5Øå¶ûÁïyv-¬üo\x001dû3ý¿þÏë©YI²ÌC­a¿ÈU&\x001aä¾ü¤WÀ²°¿E«\x001cÙàÍ'ê\x001d\x0016=+q)*iú\x0011É¢­S%`·v8xt_Æ=z3ß,\x0017Ø¡3ùðÃ×K)ñIRõÒ¤óåUh¸\x001e\x001c½F@\x001d/\x0012J½è¨\x001aHÔÓ`Çâ ÞQ\x001e\x0005'ô¥§Ñ\x00061ëô'T·$ì^"³õ\x0017lJBç\x0017ß<¼½\x001eJ\x000b_\x000b\x001b|ïJf\x0018ï¦âÏ«<}/<¥®\x0003öÏyv) :Z:REùíwï®%zã4\x001e¢~B83Ýß3N¥\½\x0002Í×-ÞË\x0012.%WU¹Ù{9ÿ°ú^"Úìÿ
\x00198*S\x0005®hJ\x0011$]Ö¨~¤¢\x0016EÀ_P\x0004>\x001b/~üç+\x001dÁ=/ÍNö4J\x0004ÍüÐV}_¢e¸vÚíóìJX¤o®3>Ä;í©}ñöáZe²º
·ýÝ$Ó\x0010RÚú­×à\x000fdÕ`o\x0004[*8,k¹!ï]\x0016âø¯ûbT²:µ\x000e¡¨~Ý\x0011;4(ºzù[D}AÔ·i¹YÚ\x0006Ñ\x001d¼úw²\x001crY~só×ÿçª\x0012d>Ò¼*ïe}FM \x0010ëø|_g4ä¼¢¦1ÁÔ ý]\x000cWe¼¤§¿pû´¼®kåDÐIq¨\x001bR¯ý\x0007¥\\x0007åà¾!ô3ß\x0010&¿æ¹U°ÞN³â÷çôþZtýÀc ÓÖó°·Ê\x0014aëùÕv\x0011ê`jkzoþgWÂ\x0012u\x0019|ÍîÕNàîZzçrþvÖ
NíÚWïÁÄ§4?\x001a$¯òu$Ë\x0019J'\x0013pBìßóìR\x0018ï#_æßáä?<º+É\x001bûÊ"þ1·sÁ%µÞÏýveè^C\x001bî£õs\Ëó\x0007b.¾AzEK¤B\x001fUJÑ\x001e=È{	}\x0018ì´S_B#ç\ß\x001c¹çÈ*\x000f¥oK>/îh©\x0015\x0007_r!á\x0002_sÀY\x001cn]¦uóÄ\x0006ëæTÕ2o\x000ftüÈ,%\x001aL\x00151	Fpß.N`ï\x001e¿»»\x001e\x0001¡\x0014ÊMCméTªè@âß=¶¯~Z^½ÊSÄ ì8&\x001a\x001dýgÂz7xÜÊo{öíí·çWôðt/'ÊõÔº\x000bL\x0011\x0019öÄ[öå\x001aÎëõ/nÖöÑ}ý~QÑë\x0015h
#\x0004iÐ[ëK6\x000f\x0004\x000fújm©VÌ\x0008­öÉÄcï#\x001f¥\x0016\x0015,.SB)\x0004Ô¦DçM'- Ï\x001c@V7Ú=#	¾jl-Ð2\x0003Z\<\x001f`\x0005²úÈ¼ù\x0005û7²Ô¸8¥\x001cýg×Â\x001c\x001e\x000eò®¥¤iÿ¥Ý>
ë\x0003ÎJê5ûò±õ\x0001ßÂ¸Û\x0017o¬ ÞHÄ47öGKV³\x0015,ÞkÃbÆWÀ6?°Èk9lqûökß>|sûV\x0017íâ÷&§tÏó\x001f¿þLB}SüZß÷Cbk¦]ë¾¨ÝÚ\x0017ùù}Q´a~'1\x0017ý!(+%?¢mZÊj\x0001pø±~û¿üÓ\x001f>ySüÜò ~&áÌ÷ÊB}!q·~FwO¿»ÎbÅ\x0012ví&Y¬áU4ª)IúÄ\x000bUË=WÇùÿê
Ëa¿ÖÐâ··w\x001fnþåjk
èpèªÃ*a¬R'zs^¤¤_;(½ì"Q\x001e'÷ãÍ¯\x001fÞ}wõ	Ýí³øºr9õÑ ÖsãIvQªá.\x0010y­
;ôI\x0017»¿{úýöÛm|dZ)ñ´L­i\x0017 )\x000fæØAãE)Ñ>ºÿãøÔ~ó×¿¼ûë_><^o©$bßåêtKÅÂéìò¬ú#[*º\x0019L¾¾µj|0½}x¯5àÿöðî",ý\x001fÜä\x0001wT\x0008.>¼\x0000Clr2uMá\x000fb \x0017]%\x0013}{óùDFzÕ}uûtI³úÙ\x001f^Åuªò?áüåå]£R"\x0002ù+o\x000eòÁ]¦e3=Êfúòá\x000f×
\x0006w\x001a·;ÛÌÈñÒó\x0011ÚÑ¨Ü®Oéò'Þ|&Òýå4áÏ\x000cºÏxÅµ1\x001d>7Põýì^,GwÍspàÕ­P´\x0011}ùykäct\x001a%j\x0013R½;²$M:fõõ-R¦Óh.Ò·:\x0008?7J©ÞkÞí\x0004çÄ[ÖHï_enÆÏ¿ÖÉ;]¤÷7_ÝgßýÜã(Çåþ¯é|\x001cev\x001bSÅ\x000cuM8à\x001c¼è:5X§ßÜ½»{|x{ó/\x000fß^ésSf*.QÍ1?·TÎ\x0013ù²D%ÇAÆ|uKÔùLúÍÃÓÛûwJ_øêîÝEègn¥\x00108{ëg½ÐzÛ\x0007§åj+å¸\x001aü²ë\x0014¬«×\x0000jçü->µV´è÷O-Né×¶>Þ\x0015ÚG*²øáþîñæ¿?Ý½¿Ò>ÊÚ2U*%ôsF
ÜC¿6¾ÂÄ;tEyüë_Þß¼xz¯AÀO£ÑÏýàünx7b¥ÏÁRWý?áUæn¤T!\x001bjT\x0001F=àÊ·OT89\x0019ÈhÌ]ÏÂQZ7QiØ×øåaai¤l7¿¸Ö\x0017bs¶
\x001dì¹>>¤3Ñ\Ó6-c¿ÂôVâu}®x&ÉÏ¦\x0018 ôêÏGw+g>,Pqa\x001cQ¯n\x0012oO\x001fØÍíö¯V\x0001ÐA.sï§·*¥´\x0017º£ñ¤OÎ¤¯îß¾ÕÁë±æJYnñ\'É½{¶rrçÜ"Ðë[¥`®Ò¿>]m¢ç2nOç\hP<7\x001d._mö\x001f¿w xzwÿÍý§EÛVãâÇõø?¶\x0005ù?qEÎ¸Û¯Ë\x0015:BYÕÖJÄq.þ2Tþ~|øñIþÚ½þS\x0012\x0019¸ÓzXÏóÿµãºl\x0007W¢ç5ùúß¿ùæ§Ü­#æJ5Ø\x0002nZÏ	}-¥­ì$»HmzWÿÃ¶Ãß§øðwÇNKF\x0003D¿å¹ePÉ1tø$èÿX^ó7\x000fß¸úaÍ¿xÿãä½¿ù·Ç§ßýîáíµ^xl	ÓÉÖê¹»ÜJ©g}Fnåóÿæ\x0001÷Ïóñï½ð¹xüÂ~ËsËpñVî\x001fÿøý7ðV¾¼ýI2üK\x0002ÈÏÍÈ¨s­Bü§+=k"\x000f%¢êþ±WúÏ}\x0011\x000b\x001fç´b¤røkY7ñtûý#æ4×oÙ¥>lÂ 9£ÔÇôÍ\x001e`¥2Õ_ÝÛXÞÅ\3þ,\x000e~Êspñ.ò7üîG¾$\x0005¿ÖP]\x001c¬1×iË=¿j×ÂYÕTÎZUú¶sþî«hEyZïUÌ%[N¨ßòì:\x0018w\x0012`OÅÇØñS±Ó1vú4ìuþñ·ÿ\x0003Me´-ûýÃ\x000f\x000f\x001f®ÕNS7JÇj=\x001f\x0016U§ÒCÙk×­qß×\x001e5ÍE[¢¦ßòì:\x0018[\x0014°Ã§a¯¯ú¡ç·\x001f~Ú_õ¯\x001eä÷}¸\x001a\x0017Ïç5Ó\x0016ë9U$»<ëhK0ü	
WzÏsÅø=\x001fýçÁxÍ\x0000\x001d>	úâöÿ!ý_áßáöx÷íÓ®ýÚ\x0013n³\:wê0ô\x001eÙ»ÞïÄkÅs¹Ößþ-Ï®ñ\x0001;|\x001aöú¿oÿã÷OïÖìÓ_ÿç\x001f¯ùô^(æ\x0010XÔ^$ôy¶!}öÚc¼¹hK`qð[]×ñï÷ùþ\x0003TìN¨oïnÆbÜÅ¸ùVYÐ¸Ò·èB§èÓïlÞ¦\x0014ø=ë=ËãåÞOÍÅR±Y\x000b\x0006c\x0015÷sð[[\x0006«\x0016±CO^Ã>\x0004½nªöã¿\x001fs:|¸½ÿî%ó3oíâ2Eµ3µ Ç]\x0002K«5êèøàL+·\Û\x0007¿åÙu0v\x0012`OÃ^ß÷í¿÷\x001f~ÿ´¼ï»Ç{Ã×ágéÁ\x0017\x001fJoí´c%\x001c«çj¶\x001f\x0015¡×~¦ÏE[Îßòì:\¼÷þîñ\x000eâ¨\x0013_õJï"u.\x001e¸\x0013Äcíç¹Å1Ñ\x000f=6^Óg7Wly\x0017\x0007¿åÙu0>;À\x000e½¾çß·©}\x000fYÑ^ÞO?\ì*³Ûb9_Ôµù7i\x001f\x0008êø -K¶\x0006Röoyv\x001d\x0017
ØáÓ°×\x0017-÷30«þéíÛ¿þe\x0013\x0002y{wµn9>ê}?ó\x0018r¬\x0010\x0015¤¤\x0002ÿHÒçÏ|Ýe-TëÊ\x0019SPáª³°þXÑçIØªúÞ\x0019{wÑÓeçÎqf\x001cF\x0016lß*¢ÆæÖÛÎöÛÖ+õzñQéÅ÷tnMø¶«(Ë¾ÕÑ\x0017nW`ñRØ\x001bFJ<ûÖëO)m(\x0013Ã2PHß*×­÷	9ï	±:ç\x0004È\x0001§R\x0007ÇiÔu\x001c\x001c%\x001f@s\x0013»\x0007Ý«ãcC¾GFn£"·
\x001b¡wacyêR!Æ»D\x0016KJ=\x0013Ý+x\x0019c8i\x0014
4O%Ò¿Ô<ý¹½³ìéw¦ö3©·³¿\x000eXu7[^Û\x0014/Þ¶½å¸¿í\ë(ú5zKPë,\x0014jeçõLêGÐ}.¾6Üi2ùF\x000bt­´À¶ºò¥yû&4­
\x0019×¢¬xÇÁí`×o¤ýSJì/ö²\x001f\x0011ãëÂ-ÁF®»ïâø!s\x000e\x0007\x0016¡{ZT-Â\x0019y\x000f5äåãç\x0006\x0013
x/½1rOFUà¼×\x0004~\x000e£Æh\x0005\x0013<³\x0007ú_\x001e*øê¥fÑÿë¹<?7` \x0001©?g\x0004à0\x001c[a\x0003Ó£ò0,GÈ\x0005;Î¿¨AToLdGA¶":LeÌk\x0013ÆNÕX_Êù\x0006P\x0017Öóå>	_òr·?¦Õ¹v®Ú×è\+?%!õ?ªo\x0002ò?@{Z\x0005ù'ôsê\x0017\x0017åÝá¢	4ÁÎÔÓ\x0005¦IiÁöy¸\x000f\x001d`GØîì`6^AFh%\x0015×Îo/NûÕ5\x000eÖD¢P\x0018\x0015uÙ3Y9
\x0006TôG¸\x001epC§mãêúÌTpVó4¾Ñ6èÄË\x0001o1¤Õà.FÕÑV³¼°ù\x000f\x001fTyÿJU\x001b³pû÷íS>ÏÆÉÂ\x0008ª$TCÅãå¾+YÉ¿o\x000fOê\x000eÈ<\x000b\x000e½êí§TvÁ}$W3½\x0011	aÊ¥óÖ\x000e\x001dá]wTì\x00186øU¥QÚÃA¨a\x000b3>´;;Æ+²üA\x0014Ùæ+AÏÍod\x0013º t\x0018t¿ózÌë\x0005 [áõVBGÐ\x0015¡+>õAåXz§\x0002ÝÓÈe`9±\x0003\x0004\x0016ÊaÄzbJµðkô}\x001a%\x001e`Ç¼cÛýÙïD¡/Ö
\x001aÖáº¸\x001bäE%?ÁÎ¬(àóð\x00013\x0012«\x0001
B»qC 5\x001bL\x0004ÍA¨ÆI}y\x0019mØp\x0019ÉúÂøpê\x0012'E\í(án\x0012êéÚ\x0011vCl\x0004î|\x0013µä\x0016àÍ¡ý\x00008Ãm¡µ¾½/õ\x0010\x000eX½Á°Ó'.Èå¹Þ,ÿåÃÓ}\\x0003Ò3Çé¬\x001f\x001eJãÏ¿~ÉIû°	ym\x0001ñº\x001aM\x0001;¾ôÚà\x0012Ï^òÁJ
¡\x0013	]ã>Lx­ÓfbGÀÎ\x0001æT\x0005»Ò·å\x000b\x000f5Qlc+Mì\x0004Ø) ôæÓcG:õ°ìvè\x0006Ð.
\x0008\x0014ZO\x0008O;ÃEÞ\x0019ã¸Æ=:°ã~\x0016¯ÀQÝv\\x0012ù(x×á¤\x001dÃÁsÇ°?·¤\x0016pJÊsÇa+
Ø4&Ïm44ä5¾®é;xk\x0018\x000fþ\\x0002N&åîë¹×%gz³\x001foÅùµ½Üç%AÈGUrdíJN|\x0004HÐÑû¡\x0004'^§e[O÷©7®®íñê$\x0001Dªt/\x0015:M\x0003×sC\x001dLoÜ¸\x0013\x001boÜÍùèÓòÜNÇ®\x000e C¡ó\x0000;à
ãÓ\x001bèu%&{
´§\x0016HHC¡3\x0018À\x000e\x0000í

E3\x0014¾¼\x001cÝæ:PçÇô\x00116Ä7ròAmb(ËE¬îÖÆ­\x001b¹\x0018þMlLÿÔ£©\x0017ØñËrWBäkI\x0003Û\x0008U'6ª1E'-Ø0ÂQ]!Â}2\T\x000f°\x0013>wÈ°½sØÖ»ô@ÛÄõ<*AÆQ9±!å¾½¸\x0014;WnÆ=QWG¬\x001eÀÄNíÎv	\x001d;÷\x0000JåJ½+£|f`gÈgB­\x0018\x001cÈ1K7ª\x0004ntÂ÷:¤\x0018	Í.Ð¨\x000e$öÄò\x0006ßdn\x000exÕgS¿I£U5 \x001b´ªäú@è\3úÜÉS{·\x000cY:L¶\x000eÛs"Öß½F\x0016Gn\x000f#\x0005Ù9t³Å\x0010/o¦kÏ¶MëTp	ç2Sûa\x0018hQ\x0007¤\x001c\x0008Ñ0¿þ]A÷|)è®\AcRM»ÒÄêâãFÅIÍÄxCÞO¦&¨~¯àJ\x0000ÒÎ¨¿à²·[`'ä\x000cÈ	Î±,ß\x00195E\x0004e	ÜÈy¢á"B?e\x000cwÝ¬é¥\x000f=#\x001a¼¿Üú\x0008}õ\x000fÉï\x0001_\x0004¼áÖ§Äµ{?Ìg+zCÞ¯è&û\x00119#òÕq2%á6cK´i©\x0013\x001bÂÔÖ·þ.Üu\x0019ÏG\x0015Ø¥».¸£ÚÞÄNÝ±Ú,w´ü\x000cL^åüdì8ëG«\x001dá q\x001aºG-Ú8wìÆáVÈÃ¥5\x001d}3	Êr®½Ù{rÁOi\x000bn|rÌëß¸ê6èÝÞÀÁâ2G\x0016Úµ#h×\x000enº
\x001an:\x0017<ä`òØõ
\x0017}\\x001e»ÚÉe¥jÃJÓ\x001clïw\x0007%\x000bRA<ñ1\x0012óønúÆ
õ
\x0017#Ée	vÅ5Ú\x0019'ì|y×Mì\x000cwÝÁAþì% Ñ$\x0018Ø\x0004\x0001¾w}ÎÁ.Ù+l¹sëÖ»qL\x0019ü]©_PÛXÇø¨èÊÒ\x0016N^Cz´Þµaã¤ÏpÃÎ\x0012ØEb\x0001ÔN\x0007·º½ëÑT\\x001cA¾º(y¨\x0013vãÓ¤¸i}\x0000Ý°o\x0003\x001e9e.\x001esÛD¾£q\x0006\x001a\x0011Ñ\x0006í\x0011ÚÁ\x0008KÑs£VRã\x0014¨\x0011¶£\x000f¾Á\x0007ïS"[QY\x0015;0öà\x00126<0°±Æ+_åþÁKÈåcUÊ'èXuµûÑ\x0006ì¸\x0001\x000bvÀJÉ*\x000cI\x0005p\x0011»ú±IúÑñÚ±¤ÆìûG©ÜÔ¹@Ò«*ùb_ä\x001b6¶\x0018$/ÙU@\x0004Ûóµ\x0003§ÕªK¿,DmØ	Kê\x0015\x000fX\x0015°É\x0014¬T¯±ùAÕ8zl¸Í$\x0007µ YL\x0013\x001d
Í³ra$øýèìîØe²àcWÞ²%yIâôÔ=Ø&\x001eí£±_Â5\x0004\x001aü4¾Z\x0006ïÀ»Íí±¢úÀp\x0004VM(Mqvw£e¦)GàáK¶¯²ÊÙ](+\x000cÌ\x000c«uÜÃÞ\x001d\x0004\x001eL\x0001wpÇ«)
ÝÅ3ñ¦\x0016?\x001fü \x0014ôHê	%ÀèOÑF\x0017ÑÃJô\x000c.\x000cä\x00157\x001e\x001dQ¸þ÷'ImîÞÝ¾÷îÝJ¥\x00168lñÄHNÛ08>Øg~þÚ8üÁ
JCùÚ=(=ü1Ï­õr é«/äM\qÕ
]ò­µ| i¥!UrvhÈøÿÏ+é*Yôw\x0019W²n\x000bãªÔ>üüCÒ\x001bOk5\x0018÷Ì\x0005áê\x0004¼\x0013®$M \x0012¨6ÆËÔ%L,¶Õ	6\x0002lF\x001e\x0016}\x0002=p%ÑùÖz°ÈV'à\x0004À\x0005XY»\\x00088.å¤Ñ\x001e¿<6ä\x000cÈ\x0015»\x001cc¯\x0004B^×øÂ\x001dMq½E)}/;þþñ´ç\x0014\x000b\x001d¡\x00023Êw*±×0X:¯Sê[Ù>ÜÊ\x0012\x0011`\­Kï©Q=Ìop7lä\x0010kö\x0000ywAwh9©ó$Kì/ÇWd\x001fõ½\x000bÉÏëUû<3º\x001bôÂ­L¡ì¦½ü,GãÐH{¹j_.Î8ðl#°'Zhµ\x0016ìÃjñ¯âÞ©øÚãä\x001e\x0001G\x0004F¹O\x0001ö#÷\x0005`¿ Ûü
\x0019Ê
\x0005Et	ã¸b¬	&CôßÈF'tÇ
e¬Njiyè2®gèÝqR {Á:wsý
ÆÔÑI-	úèl\x0019î\x000e\x000eªf®ÁlAn¡0%ÎçF½t	:\x0006OØ·\x0003ìáÕ´aK0ê¡\x001a\x001c=\x001d×É\x0017vYØp´÷BÀ%¡wsKéßG{eMF=Äà\x0000lØ	* ö'úìç=H\x0000GÏ
¯²ç­óäe
+·.Ì!0#\ØX¹Í\x0001úÛY°\x000câH\x0002\x0014\x000eH\x0003\x001bHònü\x001bhÉ6¡1$Ï¥ìÜlzÁ\x001c\x0010¹Bò?ªä¡\x001b7
ÆÔq4Jû\x0013º`iÕ!	¥esÚ6â`¥\x00197ÓÆ\x001a¥\x000fø\x001eû¦Ú\x0007µÕ\x0017èqú\x0019)Ý] ®ÎDå\x00109Æx JNAy;zîuÛQ_o	ÑURróvt`×Öië\x0004ú\x001d\x0012­1¶ç5ñ³j®\x00140L*©q)Õcâ®D¼ða\x001c¸0ò¦Úß>Ý|qûÓÕ&KÊÂÉïgV\\x001d4S#Ô·1-öÊ¸]ÆîÌk\x0010îâh~Hàú¥,\x0002­Auq\x00143="½Â¨	-5æ\x0005¸D^ÝY&©GÈõ¿<³øÑ?ÿâÆ©{ôÐp|\x0015DOèØ,ÐÕ\x0015ó@?î\x0000í1\x000cÒ)},¹
tX\x0016Ä\x001b³;tÄ§@\x000cÉY>§ÄÐ<\x000fÓEï0\²\x0005ÖO7¿y¸Y¬%\x0003d\x0003=tzuØJLQ"¹ð¢d.ÙBùò2ø¼½q¸Ë\x0019¤ïä<÷r%«¥áR\x0007sÉè\x0013Olè\x0013\x000f\x001erÚWi\x001d\x001dmJUÂÔv@\x001aÐHÊZÖ7\x0013Í>¥"¿½\x0014epÐ&6ÜÜ\x0012\x0018>Ñ	[ò@º\x0002;7IäÌå9±¡%¥ÇÌ^þ\x0016lO\x0003lYÞ
«\x0002ú1ff4¡'6\x000eh\x000b ÁsÇÀ\\x0002<m\x000cØ\x0004\x001ar)\x0018ÊÈC7ê[.ó²\x001e£¹\x000cÎNÐ:øý
\x000f\x0008Q\x0013\x001bÖ£z\x001a\x000cP\x001e&EÙ§ÄK2[¢éhI\x0012,bïzÂ]Å¦Ò\x0007µ(å\x000bã]\x0001;B
tR\x0016ï"Á.¼Gúh¿Xôý
»d9ÐÊMJåÄ¨4ûÊ½rÄÑ>ÀÎÐí\x0001µÓTu "v\x0008üMÊ»\x001fØ\x0006qnbCsQNqH/d½+Õõr©\x0019òæ£ï=Ã÷®¹áNKjðQè¹yX\öÉ<¸L¹6ì=åØ\x0005×Ne
Å^×1Î\x000cgIKñ
noõ©\x001c½ç/g0 ³AÀ\x001d1NJ@
 \x000b8uÈ¢\x0016(;°Cì\x0006\x001c\x0014{§XZ°ëòÁ\x000f§\x001cmÀâ\x0019{ßQ¶c®üØ¼Öi*ÊÑ}SÂ\x0002
Øåâ±ùÜªB\x0006ëBC³µm6çÓ5NNÁ-WÂ¸-råÄ\x001b¸IæRáx\x0015\x0000¼mt³Ü6ã±v_¡ÝG_¤äëÔÛÖ\x0015¡)Ì,)5u_.Â¸9uE5§\x0016+óò³;\x000fÝ\x001c`Ô¹hú¢Ú§)wò\x0011ª/¹¬õEùq{ÄÞz\x001aª<{á2\x0007®eÄ\x001c\x0019×ô\x0006Ñ\x0017I¤\x0012:k*MBv%©\x0011v\x001a\x0003Tªê'l¨¦!óêØ.±µ¥L"ç³"\x001b¬å\x000c¥Ü¢\x0015V¨Ii¶ÄØLpsVÒ\x001f-¶/øÔ
){\x000c\n©\x001dnÖ.-õ]qµ1(Ê\x0012£SP$Ø4vØ%\x001f5Wã\x001cØ\x0001óÜ^qZ\x001b\x0005·\x001dúN\x001fõÅËL÷]éM¦FØüØ\x0017ÄÐ`\7èe@UªÏx¦\x0015ó{áèE\x0006|:h£\x0004Å*Zõ\Jãö·¢ýÝ`±íÃåÙÉ.ÔMl(Ô
)\x000c\x000fØJ"ÁÏ½\x0006nU\x0012gLt\x0019QËÄBqÖÆ\x001dZî>jÔU\x001fs c3\x0004<&2
x fÅ®ûEô§Î\x0012àÑÖ\x00062k\x001bÕ XÌ$ÜXjæ68yV.1±à+Éê\x001b.\x0014C%µå¯Ý÷\x0002\x0019áç\x0006\x000exÏ$ÂjçFÝXX\x000fQ\x001e;_ú{hR¿T\x0017å\x001aýÛþüïÞÞ_Ë37Ê¿Æ¥\x001aÏ~%\x0014P{Ðaéñ«^\x001bâò]»¡\x0006úkí'{jØþ*Ë²*e¼kã\x0014Èxiq\x001dq&¹\x0002*9,È#f¿ÜD\x00139ÃIæ\x0010Þ¹¦\x0016hØ*6\x0016Üiaþ\ôÑNÀ#¾Ö8(v;°ëËHÙìnÐxòÊ\x0007
¡«ÅË\x0016\x0012\x0017/k7\x001aì.T#üìöñÝÝ\x001f¯eoã{§SiH\x001cm¿¢\x000ei½¼ëâì½\\x0000\x0019ÆP·AëºiÒ7BÃÍrÊA©Zû\x001eHèó5J$\x000b\x0018Áu_
l¸¯ª÷~NS/NP¯',AÏ¢Z2®«\x0001öëJþrÀ¢Úhs6|}G±$f©\x0007ãý\x0003\x001bÆûkPô¯jÏ
ëàÁ%&º8¤<5±WGæ·?w\x0015Ë÷\x0012P]MÝ[yMêÄ6B½\x001e5\x0006äìgW
uJTðÝ
ü8kª5ªØ5ÀtÖ±®%ó«4Òb\x001c\x0012\x0010õh¹+.wÍØ\x001bpJDN]\eì¤Û¤Z³Å\x0003»\x0000¶2ÒaIZ¦Öz@91X³äÝÊX¯êã\x0010\x0002×)b<kVÊ©µª(\x0001æË·¬UQ)Ü»ê²»ü¡ôa\x0016a_¸ñUK\x000eæìÛ\x0006´dù® \x0010c¢ÜLþ\x0012«À¶ÙÃöVµfäfP­Ñ
Í¤,|&ÓÜG­ihKXS¶\x0003\x001b§lU|læ¢)æ)~­òö\x000f\x0006(&4\x000ePÔ\x0010¡4îæR8!Ç\x001c­[¸l¹ÉU{÷ÍÓ\x001f¯æFDVÉiNu·Ëgif_TÏ-ºl´Ü<%\x001bä)ò/BÆ){íÑ±­iÍm\Ö\x0005> ¡µê´x¸ïÎ óå\x0018a:Ï"cY½\x0002µNsíáÔï
S·ä%#§Ûª³@OÍ~$°\x0006ÌÛØ¯By£ÀSgW\x0012P KÎÞµ©XlÍ+8T¯ªúXîUÐXJ§U	:óOûN\x001e`[R\x0004\x0003¼\x0000xî¨ÎWb!¨\x00102k-»0T%¼¿dÌlà\x001dÀ\x00032O¢\x0004\x000fo
F\x001fõ.\x0005|Ã¾LÅ7ì\x0000Ø\x001eæJ'v$ìLìË¬aÃn;¶oP/\x001cØ\x0016ÅYÐáèe\x0006|\x0012GÂrkÞïR2o^î±\x0007­\x001aÓD\x000e¬¶\x0001 \x0003%âa¡Þ	´3\x0012qÊÖ["þK9zä |wµ©R\x001c~¤ôT\x0007q \x0006-Û/þc
ëæ ÁF\x0012ÑXä²Ê³Ë`\\5\¼··ã­ÈZ\ëôB6"\x0012\x0007äó+\x0016"¬\x0002áE	Xì\x0019]\x0006K{¥\x000eI¦å\x000c#!:\x000cÌL©´ûQåFÒ2¡¡^*\x000bCò¾rQ\x0005O³\x001aÂÎ«q`'¸\x001a³J^Z®¨#´ï\x000cÝÆô2bÂ	°\x0014Û+å
qh\x0004e\x0002%\x001eØÆ
0±ûRÚ;Ï\x001e\x000f\x0014£¸²£¹ÐÍÎ@¿VöX\x0002öX	o2¢\x0014/¥ÛÓè\x001b´Gè\x0000ô\x001cõ,^6I¥zE#	0¡±¦\x0019ðÔª6Æì1&_Kh1µî/¥7ìÄØ@/l¬åg`\x001f\x0006÷\x0013;òs'î£¬p\x000c=g%%w9æÇ\x0006½íÜ#ë*vdì\x0011ä£Ï&#YÏaã%7\x0016×T^$¿È<¾l?&tâM\x0002%ËÞV!¥;òÔ£§rèÆr¨@»ÐÎËRhtT×I`ÈFsnBW®áÂÖ.!/åáÂ\x0007Iíé-2±£Å¡\x0012\x0005±Y§²¹­{´$x¶ö³%E"kYç×ü`Z£½]po+­\x0005®iUdåïf\x0011q5â£ýWhÿ9<ÿtbÓ-¯rA\x001eòPGÇvcûàR~öBWì£Õn°Ú:EØ%Jt\x0015³ú(Aô£ÃµÃáÚtÌ\x001d\x001aýÊÎCî£\x000b,~¦MÚ1ðÜ\x001d>\x0016;XÙfy*ÚIþ
\x001e\x0011£«Ø\x00022J\x0012«ïý¹1~i`³@DèÍ\x001eýß°+b\x001aWÃläÅ3 rg?z\x001dÞ¥\x001cT¨ß_Æcìý®À\x0000G]&W\x001fîï.<i«xßxc¶q½;¸+=öäu¢\x0000Z_<7\x000f\x000b¹BN\x0001nS'8ô-»/¨·Õ+\x0013$éÜ·©Uk\x0018Ø\x001eçrJÙ<9\x0002*1òR«Oô~&ìGØ4ãáÓ«ËÀI\x001dê\x0008|Vð¼7J\x0013Ægp|K®!Qf
98>Ï\x0016´Ñ&öø\x001bm¤§G\x0008ÿú×¿HFñx{-?C_q\x00063¸\x0002\x001e¨^ûçRÇE÷ú,P\x0011¸±/ð37	+\x00102~»²\x0002a\×Þ\x0018»\x0004<
ë\x000e\x001d
g¾>!áUû"#¦+ÆhÚÀ.\x0005±± «/\x001fD&ì\x0005º[IuÆ:\x00072÷®jP\x001f\x0003÷®åF:S\x000eÔÀ«áE\x0018Gßï\x0005³ê!óúwçdé¾^­\
N«æ\x0010Y¶ òô2Ä9Ø´A#+&W²Ce.Yu\x001c¿O¾·Å®c<r\x0010\x0017&Ùì'¹þ\x0000\x0018Ói5âä1%N\x001eKåtzËy-BÖÆ ØW(½Ë/(TOk;Å5Ö¥7Òéí!\x001e3cð\x000e%\x000b£tºp!Xò\x0003\x001bÖ:uÔ"PE®0ÀÝsI:TÇ\x00076N\x001cËGüQ¨\x0014\x0019\x0011O!v\x0019`ð'6(Eju\x0008§ô%¿¡0x\x0006o%\x0018a`'8ycn ö4ÂàØ)wf`ºÑ@4é^\x0003\x001bRÓ¨>S0)]g:¹c\x0017¦¹)Üe±\x0015&6$yª]\1ÄÎÜþIÉsÄ7¢I¬0 ¬ \x000bN4ÝÔ¿\x0011µõAÐ}\x0018B\x0019Á.\x0018¨Ô\x0013Ð»4lÅa\x0018_VdåhE
¬HÐA@o8F«£^ß*ÝÄ\x0006Uº\x0016\x0002	ßkîD\x001d±À
×mºJÈ¿v\x0004½s\x0019ÇäPF k4TÎ¨ûüà11±aþàj{îV|k\x001b{ü3¶\x000eýd®#E×ªÉñïÖ9ø(}\x0008\x000b6Ä¨²Ü4ìz=4¨;¸É\x0002ÜdÊÀÀ]n\x001cZ°(.÷²¬[uÖ\x0001\x000euÖ\x001a[B9½:GI 1ÍÛ[ÿ}ðài'UÑ\x0019,¼ªÁ\x0013¸ïSÁÝ¢æ+8Z\x0005Ü\x0014ý\x0004.WC¡V[d\x0001ÍæðB°ª\x0013<Â÷\x000ezå¥êV¡Îi&^ÛÐ
Výo#ý©;\x0018æ\x0016pO\Y\x0016Þ,µåMØþ\x0008<ã²dNJõJ¹\x0002N~~½\x000e`U\x00177l|\x00017bQ:§%gÎZóØåÖ4Ú\x0004\x0007R$18V\x001b\x0004Úì
>°\x000f\x000eÚ\x0000õÅ*1\x0008Ü\x000fE©ïVHë,x\x0005khlbã&W»JÀÖ\x0013±¹ÖP§J¶¾´ßÞ¿?|¡_ëßÜ\x0017Þ£\x0015ÂÐ\x0004äuçwªÄ	ÆLçnàW÷ßÜª\x0006×Ò\x0016¹Ô8üñä\x0005ÒJ\x0006*¤F£{ôê\x0018£\x001dó!;êpJv\x0002PÈ+·-¼dxé@¹!ï\x000eÊ\x0018âRV&*ñ\x001dw\x0019ë¶è7«N¼>4\x0014«óÔ°\x0004ä¼tÔ\x000eLß.£ 9H.2«ÔÊ\x0008\x000br\x001bÅ#hlè|;txò\x0012Ø­\x0006VuvY\x000e \x0003\x0019;%¹P\x0013°ÎZ'¨p½¦aúf1cV½«áÄ\x0006	b©DÕ\x001b7ðîH£\x0018fQ9WÝüR\x0002{ÕÙ¡ÐÆËz¤¡LhñWá|}ê]@P;Òä0Û\x0016¾oÍ\x0016IÔ; ÊíÍo¾¸¿{|¼ûîñáýµF2*Éâóä ¯ïT[Î¸k¢úq¾èHÆGÙ\[ÊlÚ\x0001înteèþíõ}VmJ¦6?Û
\x001a>Û¦Éô\x000e\x001d\x0018@íHãö¸\x0003hà*5åÓÃ°Æ$8£$\x0008¡mª\x0006½\x0006á¸[÷Õonïß?¼»ùöoúó}÷í\x001f®tmÕÆ1ÕÁ¨¬§Ç\x001cü\x000b[úâ
¯\x0010
Ûr2\x001fÀ\x001cC	ÂÜg­Ëå2«@GÈx¹l\x0012<ç5êËè\ÍK!o*,Ât_>â+Ôaªè\x00004k\x001eV7 /Ä~NÐ(öÃF9¿\x0002ì
¿î
[Nq¦Öp£ªXð\x000b]£,+7èB\x0016\x0015»/uÂ\x0012È<%ûDg<5ûå>Ít´ 	\x0016$dR\x0012©8\x0007·\x001fUû¾Èxß\x0006ÒêÉ8·ptÙ:\x0010Z5.÷7¿¾{­æMf«!f²\x0011ÉAÏ>ªTæKÎ:\x001d\(¯`å\x0013@RS¿1uâ\x001bgIm(%OÛ8Ò\x00114L\x0008ÔFC¿ü£òd\x000eÇBÚ¼²\x000e\x000b"w2Þë\x0008ªY\x0015\x0008Yþ)cû\x000cæÐEl¢ÛÇÇû+ÚHûÄÕtYå]V\x0012ò]¹WrÁ\x0017ögÿè­\x0014ÓrtO'ZUÐ(Ë.´C·ÇE'2:\x0016É¹\x0003NtêüC¼\x0003¶pÒx±Ü\x000cA®
8À\x0004\x000f¨/ÉGrxhò_­ÀÄØHO7¿¹ÿöþJ\x001bÈñ¹|ç\x001czÈãÎ¨¿¤±j¡·Jkl«´½\x001e«dSãõ¥V\x0014ö8ÈDÜÐ¤Æ\x0007Ç\x001e
¥öz9\x001e\¾i¹|\x000fÖÿ¹W§µo#b\x0018È(8Ü()A\x000fë1¨¸.\x00017ñÝºyEþæþ÷W»$½g?ÎvÊ]w-¢³ýE¯J{\x001cÞ¸u¶KDEÃÐXÄB%ÃØµj?\x0019ÀnXu*úí¸+´1ª¸u\x0005/a×	\x001f°\x001e
\x000b´rÛ°9SÌÉ\x0016ñÞ Áyt²ìÈ\x0007¬ÔùC<è\x001f·Îýã)
\x0008®fq\x0011TrLõî1$+8L\x0016¿çýÍçw÷ï¯%2\x001fcX\x0018Å¹«\x000ejkEÁ:ÛË/&ºðq'sZÉ=ÁQ¯ªÑ55\x000f|Úc<\x0018QMËjÓu l×ÐióÇ°L¨®ºÍqÐ
¡\x001d;¶\x0002Íîçms~<zl-2\x0001¯Zâ\x0006bãÊ.^ÈÏSwßn\x00076\x0008fë6MQÄHÍ\x0018ç=çGê\x001cËe>·awÀnHIìñ%Ð})Ö\x000f>¡¥kV\x001d EJØT0ýÀ¾,\x0018bïågûow·ï¯÷áÊ×¹êëìn8)\x0002÷·¸ìÆ}m!¹QxKîkp)¹Bû ¸´Vµ93Qq¤`\x000b'4\x00164R$[ë\x0016\x0001­\x000b\x0005£Ñ0´ÿ'4\x00154\x001a1ajLp\x0018è3
f<E>wáÈý»÷\x000fï®¶<ýÆ¢çÿùGl¶\x0016óWDe.½¨\x001eÊ½ñª½__u­à\x0005*?¥¾áî\x0016ÑRN¨ü\x000cgÆTû æÅ¤\x0002ý\x00059YJ\x0014hµSy?»«8WzÓ\è8ÞW'ÒøX­ÓýE¸FÇçÂÙ)ÐøTMÜqµs\x0019C<\x0007½ÆpQ\x000eÎd&³U DÉ&$óJ³:aí\x0008&ÒÚÓÐ$Q\x001bsi6ÊK\x0007-Á°(åæK¾J&S¸Cº=nö1	ÃS\x001dH\$Z9Xû&QO´8ì\x000eÎ¸­#òåíO\x000fOo¯¥ø\x0003ËZõÜÎþYUyàs*vyÑø¶6Ý½\x001fãåü×ì¥\x000fÈf$T$óÝ^È¢çÒ\x00188´Q"!Ð\x0015ì6\x001d»GN\x001bÛdè
jÐyÛçt1ûè\|ãr·¬Í'2\x0008ææJ4°¨J¨\x0005íq\x001c$&6hAg¹?@±1zÞüÙñRìCÚÈrR\x001aÐ\x0001sG\x0015×Êp\x0008ä¶­òOô"ÓÞ6\x0014C7l|Zfé±s]°Çs\x001bóý\x0013»b\x0001ücpD É>'Îy{?\x0010ßÜ°\x001b\x0015\x0017àXå.tÇfÏ\x0016=}é\x001dINHZÑwVÄ\x000f>,ØC}ÛPÛß°QZ*\x000cÚ´ÇÕ\x000elh§\x0003yÿa;²\x000f`tdW*p3uÆ¼3ÓÔõ4Fà7l\x0014±\x000eø?\x0004¼\x0014\x000cú¦]d\x0010¦7lÔPOHØ)ÚEw]ö¥CSö\x000cüÄ\x0019øÞ2aËÞ¥N_V¢\x0011·TF\x001d3\x001f\x001d®¤Î;\x001a\x0008ªp	ßs¬<hêf÷~RçÙ£;®jÖ³Ö9OÜö´iÖ\x001f½Ëï²Dà1©Ó!%â9vÒÚïÙõ1=}t¾f\x0014$¯h¦Öñ$äå\x0005$Æ\x001e=lØKMl°ÒR|µ\x0012ON«Ý²H#^¿\x000c·&6Hõõî1Ü*jâCë½\x001a@«ó¨M­ß°á×ç}¢#:ôí$\x001eîcjÌ»Ô£=Xi\x000f}|_;\x0014%ª\x0016Ò\x0002=æFêÑqRñ8!\x001en\x000b~Z¯%ì>\x001cöêÑ«¬ð*kuØ¸\x0018
nt
Ö¼`\x000fêX;úä\x001b|òµx´ÛVå)´É¡p!÷0±/h'ì²c·D>õË\x0013:_g\x0012¹ªÅ%\x001aÐèA-A\x000f&
yrÈ<§ì!\x000e·AãmfG´Ï\x0005Ãöý\x0006ÍpeÚà&ñ¼"JÒeèf\x001552t\x001aÏfO_Ýß¾}¸RÀ_*«,\x000bÊó\x0010]×îî¡\x001eÃ/j\x0013U\x0017³¬æ¹!\x0018å\x001bC±ÚtÊôÎ« ïÐTìÇ.^en\x0008*tbIRõ¬JÐÆ±ªêùô\x0000\x001aÌÆuh§\x0001r¡Æ^\x001a¤ËÕê\x001c\x0006?@Þá\x0004y«Ö k'å;ÕÜÆ\x0013\x001bªp\x001bp\x0001`Y]69©|=\x0016á\x0005øú´c²X\x0003;ÀC\x001flÇg·²=°·a£¯;\x0005äcAð\x000e-µ°_M­e?:±Ïq\T\x0004é-5ÓHsincÜÃ¸/&t\x0007h_A\x0012C \x0013Õ{Kóäj Øã
GË\x001d=`Ë\x0005Q
`7²z*r\x000fòöÓ<Â¨ËB±\x000eê²\x000f?üpEßï¸ä
³Ã5\x0014ÙCÕôóµ÷ÐÃ\x0007&ÆtÕl±$u
Ãqé´\x000e#¦\x001aÙ>A\x00033FÛ9°J+¯!TÇA{\x001c`F²;¡Q\x001b"dâÕBNÊòÐüîJ°®ÂÔ/÷ÑÍgwò~zº\x0016q+;\x0019iøü\x0015ê±\x000ekïtXûE7v}ß\x0008¼ÓÂÅÔ\x000e
ý\x0014I¼Éû0/PM\x0006Ë\x000b	«×"\x00124rbâ=]XMk¤\x0004UÎ½¼ÿù÷·?üxóëwß]çek#G_O/»¶FgFRvóËªî¶`HI\x001asÉsKPÂ\x0004mñ2Æ~p\x0008³\x0017®GØmJÈD\x0006\x0005Ø®}S\x000f¹a!õ+eeR]¥¸\x0016ì\x0000eb£tm`¡YÔ0\x0002C\x001f	©ØwI2v )0¡Ar·\x0000Bz\x0012Ueªë-\x001e/Êu\x0019ÕH£%>«û(àÁ®yvÇÙÁÏ
\x000b2\x0013°"ÎSÁFå\x000c8WqåÈ
hbÃÔb\x0010\x0016È4@Ái×\x0016YaG^ÇP+°h\x0002£\x0005ö\x0007?kµ­éâÜ?\x0011Ùþ\x001dÈ8ýûó-Ê@nlhÛLdÐ¶ùÈGÏ\>í/Ïôr¡Dû^Oô§ß_é0ïHbj×{&f9\x0015¸\x0003ï:g*ÿ\x0013\x001cæ%¬¹ÁÆtÓ6Ü¿T\x001a©3o3Hx\x0003\x0018Hxµ«\x0019zf¢Ðn\x0008åm5¦i\x001dp
-[ùKh«©³õ6P
üÔÎç6\x001a«\x0013\x001b\x001a«\x0007ïöÙ}¡Ø4ÂÄ\x0006	ZIâë	[OIT\x0018èÜn«¥øq	\x0019×
\x001fUo@DOê\x0018íi½\x000b	\x001fUÍ?\x000f®¡×b7Ø$¥Îb³UC
7£±?±=cw\x000e\\x0017ä#§»\x000c¤å*å}±µ`\x001drIPÙ²3\x000eVl<Z\x0008D\x0007×Ñ'èMJ¾\x0003u5\x0007\x0004;#Ð@q=ÀôRÕ\x0015¬\x001bÄi^ÕÀn¶°ASÄ%´\x000eª¿HK²È÷ç8t#-1ë²Y{GV·jj\x0008-c³7½×PS\x000fØæ#Tÿ÷öáZóè#\x001f\x0011¡¨zÛcÏ{2¿,ã\\x0007g?wå¦¦\x001eø èØ\x0002\x0014Ïä\x0014¦*e=\x001dù ,\x0007\x0006\x0019\x001b4ôCä@Çó&¯}JGeôZ}ñfrÆÖ`í=ø±þoÎË»v\x0011\x0017gW\x000b:çç¡=S¶Ac\x0008\x0016RÒ¦y¢\x0005i|H¦r@öÐ:fxêJy>5?t5üÝ|òÆ·¥Ójÿötÿöîj\x001d)w¦HäâOÏ=kzIr\x0017-ÙÃFF\x0007`&«ð\x0001RÐm2ÕN9NRZ
--É°\x0001ÃFRú6¨&í}%\x0002æl®üvN:û\x000fw4Pr]R¾¼\x001dïMl\x001cº¿\x000c¾ÙeR5S\x0000î3V{¢\x0012ÈÛçöÔg\x000f÷·¸\x0016\x0013SR>>Bv§È~øÁMÛñ^[Ê:û\x001d\x0007\x0012Å;\x0014 :&
'ò\x0014èB\x000eC\x0013>\x001a¡æDÞCÍâT
£ï¤ZH
¡\x001dí|Yà\x001bÕN\x000e íõöÝ
öË\x0011v\x0003l\x0015ô:C«®8N\¸\x0014ÙËÌO=(«r0¡qE|\x0002\x0015¨Mw²WòPfìAÑ³Ì%\x00066\x0010kª\x001c\x001a:U¦ÉËòÑ`ç`\x0013kNØðÜ\x000euM¢D×¤-Ø»ÖSØ{f{¯{¬ê\x0004üØ´ñcÉ}±Æy\x0007t\x0000h¹[w»Ç(7)å#.¬iõÙmÔB\x001bÛ\x0003©a¹öá±èUD\x000c\x000e2·ÈQÉX\x0015çê/Î1	cùöV¡¯5<Ðg|a[õ\x0011\x0015kR\x001d;Èä~4$F,	s¿4TS\x0003tÒ"²XYe\~y·Ûá\x001b2ª\x000e½fôõ$`%OÌ\x0003G6í{\x0007V]Têp¨\x0018\x001b©B«æÅ4#=BFµ¦ì Ë%"7\x0016x°«ôi¿fÉç/\x0004fu2F7$i9	ú¶Â4x\x000e\x0018Ì\x001b6÷ÙæTã\x000eô©»FÀ¼A}\x0001Ó¸¬T5\x001aÿ¨,[r?²éÛ ñ©\x001b©ª÷\x001d	®´F\x0017F+aoØW­ðaMó­/+2Ë«±æÄF7\x000eûÓöØ\x0018=Ý\x0003ì\x0000[[ñ=TÂè(\x000cíØXÝ-çÃ
ÂÀÆ
Bç\x0006WÐØ¢OÖô9ÊmÆîÄNèßÑ|Gerñ}6(töÈÐ~BC1²I \x0001z¾\x001acS\x001e0f\x0001{\x000e2GËÆÆ«È<\x0012ÝýÌOOË­ätt*Ð©CÂîi\x0003·ß¥\x00070%¡ô[Ô\x000cUå²ã1¹½5:U0b\x0013$ÿÇÛÇkMÈID.=Õs¼Þõ6p@2PuïW¨¤e\x0015çÜOê5,{9nhûËfXY
Í\x001eqÐ	·QG"¼<\x0017jvVÐGÈPÐõÇ)V©¨ï..\x000f\x001dìÁî
\x001aÖ#U8\x000e\x0006¡¨)½q3XÎ9V°Aãg\x001d
\x0004D5Cä©\x0017\x001e
÷Uá\x001fÈ\x001dÑ\Ý>%È}aªs½_zmÐi.´?´_KR\x000cÊµbèT\x000fã\x0003\x001bã]]\x0013°#'é\x000c8É?Ì{¯Ì¬\x0004z°P½ý·Ç»w×\x001a¼N1S³¡K\x0008¦Ô¸âGÙa;ÒZ²×6Iij\x00165QµUÂù¾®#NøÍÆ@xw){óÝ áuÚR\x0000hç\x0006ã\x000f¨o4K)2¢H«À´H~v§Jð`Rx\x0014ài5\x0003 \x0006\x0001`ãÛ^æùÝ&B+ùd.\x001clÿ
\x001a¶¿SGË=\x000fh\x0012y`-;ÅÕ¤ÀgS^·ÿÝ\x0014qº}||x÷îþîñJÀS<ëôÚ\x001aÜÅ\x0017æ%ÚÅUKýq\x0016îµwÈÌJ\x000c'ü¢£­Ç1LdD\x0013\x0019\x0018\x0012é\x0001çW\x0016©-ÒoUÁã\x0014b·\x0014\x001a\x0017ÙâÞ\x0002v\x0000ÆÈ#5\x0000¢_§öãÑrà\As8i¡J\x00194\\x0015\x001a±Í»nXËh\x00086èýáGÃÐ-úù÷·\x001fîÞ><]©,Ñ\x001c\x0013»¦\x001ck
sª8ÒWÖZó\x0017o$OYm¿'j#U)9$Ê£]²\x0008C¼ÂÈ8D_ó(È6¨ Ó»Ö´ÓÛCôùR°Ûã<ºà(ë¬½,\x0019íà»[þ\x0006Ë\x000e\x0015h¤6dí~ñ<ºc¹Ö2Ë}»Ád·WBeBG\x000bQw6\x0005.þ@*_\x0008kÿ\x001ch#î1dDn¾º{{5¨Ô 'Í»Bõ(SÔÔYö%j}ã"\x001eº 6\x0013
\x001aÇË\x001d¿\x0018Æ´Üñé _½AÃ\x0006Uá"ô\x0011­¦ècÌL¥t!Ø:¥\x001b4\x0005ië\x000f=\x0016ÊFÌódHvÁo&)'~·\x0002Ãjº/â\x0002\x001d¬\x001fDÔÏmµÏo«YúÍ¿Ü=ýîZ\x0015éÌEB5\x0004ÞKG	-]Ey^î~ Sj\x001cvm-ðÊÍ\x000eEG%\x001a\x0015:¢ÙoE¶õðr®AbW\x0008"\ÃªcR
ÜFa787\x0019
Ýò\x0014Rì\x0015MçA¼K\x001f¬ $a\x000cËc[ÌË
§ÝÎ¦ÿÕÓýÛïo~¸\x0016À±ûs÷%í¥1s´¶×ÆØï+Kó¬\x001as]z\x001b:6\x0007r\x0013êÏJÅCÙ
ù8ýµ É¸ \x0018ª\x000b$÷Tï¡sÔSÉhwNèÐ\x001e\x001dj\J\x000bt)Ë»«\x0007´Ñ\x0001Þò¿4IR¨Ã!ÈÌPÐ
óQ]¼.uñFªûEþ\x0001®Í¸Ä\x0016L^Õ	ÚrqÞÝüëíû·oïï®\x0014C'×\x001bÑÓtÍÏU°ï}ý<ïÈ×¦
i
\x0004\x0016¾îe_4\x001c6Ì\x001d·ªÖâ*Èu\x000eôg\x00066êÏø\x0008g y¦ºèNBè\x001af·ßýUè\x0004ÙS[½\x000e«TÇ@U\x000eG\x0012\x00065ÍÑÎfÈ#\x000cìÝ\x0004míJiú9ð§ÕÚ<\x0007>¼³FiËðÞ±kÊð\x0001D
Ù\x001d^[*mØÝ¹7øÇ\x0013\x001cøÇ:\x0002Ú\x000bQþ;CµÓåRº÷ã]\x0015\x001fcÏ.èÉ³cag½pqU|ë4d^Å9ÿ½{óÕ½ìúÇ«©ú%Ý|xh¦uÚ<i«ëJ­íÅÞì\x000cø¢\x001e-k7òÔ½\x001ezÀRù2õ¦x#2u*,càvWKÛTWe%¦æ°¿0þ>AGF>ì Ö\x001dzgVpWÊ¬[ 3=uA:`aø¾°\x0001S,fÅjC\x000e¸\x001ehÑ4F×
õ\x0014ø(\x0013hÛ\x0008åÏ\x0002á\x0012ýqð¡rt\x0004\x001c»\x0019\x000fZ.\x0008ïo~uw{­ôe	|îg©ÕÅé\x0016ÓJ8ò¥×6Dkõ¨W\x0002eù¢IA4¢(\x0001\x001bGþq*ãXD\x0017Ö}ÐUj &Ð³Ý\x0003ëK</6û;hT~ün¾°ç÷û9zµ>OìK¿³5á]ìÔfS±ÿ\x001c\x0002»«8ä{òSö\x0018¨DIÊ\x0002¯\x0002-ÂÁü¥\x0011y2mI\x00069IÅ«	8µ)Åyí±7%IËnÍ$ÿ\x001bÎ#¡\x0012³uløÄ£\x001eCºùêîÝ+í!\x0015! \x0000²æpÚCcòm¿¿ñ1ø ¯n\x000f\x0019U¢ÂwOí:H\x0006£\x0007©\x0003\x0012\x000c³ H-ñ¨l¶yÈ*e\x001c\x0019JêhY³£¦rÄs_\x0006&jø\x0013ÇlÔc\x001b§áÔu¡-S7	\x0006rÄ{ÉÈ®w\x0016­ÓK½æ|ÚGÍ©ïã~=+.¼¬J¿IA1\x001eãÈëAð^iÌ{\x0008£ÅqTq.±ÚB
Ó+Û8æ\x00064´XÖh<@w`Ñ©6F\x001eÃBÆôý\x0003sAjÛéÕqÅ Æéoj\x0014vãZ18xµÏn\x000b
½\x000fk`cJã}!CèÄüèèW'ëa¹\x0016q@G\x0008$Ôò\x001cè-MÞjÄRw(<}¯Y{<qÃAY½°8µÄ=(ÑP\x001eÈ0\x001c«\x0016\x0011 +¡ò\x0004$¬\x00137\x0008Ý½ÕãôÞæ |ñxÿÃ|NW;\x0012j¤.gãl\x0017ô\x000e\x0001\x000eÍ()ÖHW_[PjQ|\)ÒÎ\x0001»Q¢º\x0018ø±\x0002KQÉ!\x001fZ\x0000m¹,S_:^²Äæ\ÃÜÓ\x0018ºÔþJüC_=\x000foÈ\x0007uu[\x0018,ZÆDwy\x000eÔ,âR+ÚAìÀüo¯!är\x001bÛ![BÒ+ËRÒ!4B.Ë¤h<`ÚoÐ\x0019 uÈ\x0012B\x00080x\x001dÃ£1u6ÞLÕíÂõ£7ûì®°å\x001bv@ìÚ\x0008ê
CÁ&·ï*·C?¨{º¥îYUFjÝ\x001acï¨
çk¬§ÐQ@Ø ëâR\x0005V`\x0007bÄk¥sÁ\x001eìoÃ\x0010gÃ\x0006Y\x0017W#
*Fµ$Ý¨¦¦ò\x0005ÞÖ]Ø°;<wÁÊ½¦4 &èdD »T¤\x001e¿½Öl¢J\x0010²\x000cQ9«ô¨\x0003}P®éhþúÏ\x001a7yóàìé'?y/Î'NýChõH)r8Øe£.²/\x0004ÜSfWz¶m\x0007Ó\x0003\x001b¦\x0013Çd.\x000fýôõÉ\²;Ö`;5\x001aØ°Gþ2h?X¢³õ]gÕÓ\x00146\x001aØ\x001d±Íóì®;6_´Q1"-9kS\x0019\x000b
Õ³.mqs<Ñ\x0012
\x001aØ0¡\x0010{!!ñ<7$ËÇtRÐë¼b¼QcÓÀ½§Ú¨èØ«GúF\x0003\x001a\x001f»GðsbÒFªåák´ô	eìnÅç\x000foßÞ¾ûîZl§YT?NñMtjL¼\x0011BÞñ/\x0017ÈJhñõ,®W Ëëè§<»
S)%8T#¯ó:Jõä\x0002Ñ\§ \x0016\x0002f9]âø<^YïÈà=\x0004éN{ñû×4³F%3Ý\x0000Uë#J9ÀöeÇî\x0010¢\x000cÇ\x0003Ô¯­lÃ4\x0005}½ñUOØ\x0006°\x0011Ý\x0000eñ\x000b\x001d¢LQ¼·AM°D\x0002;(vBCÒ\x000e?²I\x000e£\x0013vf÷Æ8±ã¾ïµÎ	\x0015¼Öù £­T56÷é´èïèä*+¨Q\x0008u\x0015=+].=ÔBûñáWú¤¢\x000eÆqWÏl
\x0018Ý\x0007-$\x0016\x000f/,ÌùÑQUY9[ð\x001erõ\x0014{"êX\x000c1²â\Þ6sx\x0006\x001e¢/¨¥ÕÊbß\x0019û\x000cå\x0003RY¥½\ó¬@Å*·h¢åv 'Z\x00169Q9c\x0002ýÄÌB*QEò\x0019zp­¹·©¤\x0002Ð¤¬ë} \x001dW\x0017èq~Õp\x0004\x001d\x0000:9Ì3t%%uõá·'ÂÒ-[¼µ§Ø(\x000f¢Qz_\x001d'BavÖ-µµu\x0010[}«\x000bæXÓcÇÎ,/G<éË"°Ú¼$-A>ëÉ?ËK"ÿ¶\x0015PA§àÌÜGÍýïµlô¯wW:sä\x0012ësj\x0019î:¤?ã=¸\x0017ZIóøËÖ\x0011VU®7´\x001cNÉ«Z	mWI\x0008èz	S \x001a_b¿qÊÛÕ\x000cµÿk¢&fHüÚUTh\x001b(a`Wè>y½\x0007÷s§j\x0008{JûÍk¤0¾5h!àÁQñ¨£ætÇ¶\x0014aÂB\x0010vS0ÑJ/\x00068¤\x0017¥ë0\x0014\x001ek\x0006á|îËWÜ¦x1\x0006X'x* +p§§¡ÚN»Ús\x0015¦ÎG=xão°[/0üÔÿ\x001c+j9WÆ´QU\x0013>ÀÆE}·ÓªÔ è
­IÉ¼&SêÑ *r\x0004vQ\x0017±=yNÊ@
f\x001f9	UeÃ1Ö\x000e¾ñ7Nàî¬¡¤LZÔ$`l÷¥h\x001döà°Ï-E¸£äöÔs\x001dËÍñ\x0018gµ¢\x001d7\x0004`/
x¤hØqûJ°»5Öl¹Ç_ßþtûîÛ«µjÔm\x0011óm?¼6N¤Ê"ÙRìkkÕ\x0018\x001bµb8ê~ncnQdeàVÚí ­-uvY¥îÊ%Ç\x001cB"ÍÌÐ9[c(\x0015\x001c\x0017 Uÿ«§»?^Ï\x001f¥Éçy\x001eA)ä¸}5¯lnÀê0F¨:\x001c¦ÉN-­°ë-á'Ý^¡\x000eZ¥g2 qÜ®WºÐõza±\x001e\x0002n£wljõô%D<Xþg_ÝØ²Í\x0013\x001býpA&Å7Oâ±±\x001fc}LQX2ù\x0003\x0018dò93ÌÉ?E}	9395O>\x001b±§wÆàÝÍ\x0017wx¼»ùåÃû÷W\x0013ß,,îãÏ6Ó=lÊY§ $¤Õ6<8êL»ÝÊ<»Gî\x001eXãHGåÖe#(õ\x0008»\x0002v¶`Gâ%Â?c;ë{\x0016ûÅãÓ»»·Wt**~ªºoäóOQ>ðºS;\x0017­ßÚ¯ÜòüI\x000b¡QåVÑZOË÷8t¡ÌIZä\x000e´Ï&6í¦\aK£±ÓÄ
ê®Ê
vé¥üÃh\x000f¾ûðpÿþîöJ£AÙ×Eí7¹~Ö	\x0011\x001b´:Ïü¢rH\x001f¯\x0000\x0011/\x0014 \x0002\x0015o\x001dÈ~n¸:û3òªRå\x001ch^O²êÏ\x0011rqÅ\x0016\x0016Ð
¡=ø¤ì\x001dËVÈÕÃT2\x001aäzidn6®ª\x0007þ¹mÍáÍîÌSé7ýËû+öR\§7»]\x001aØ\x001b\x0016§\x0019Ðz@M\x000cCc\x000eÀ ØM{áv#\x001b$eA³7Õì\x0007\x00181G_'`\OÜ=æ²)9\x0016c
.\x001d\x0008@ôuHÅ©Àk£µ¯ôÌ$öôµ\x0003ñ\x0013Ç\x0011i×IÍ\x0006)Bë¬\x0004\x00169\x0003§\x000e\x0007Ú\x0012}UFSîhÃõàì#ÅX\x0018Ú\x000fK\x0004#ÿÐ0%èrBEl·©IÂKdÿ»àºE
éáò«\x001aÒ?·÷*øz¥Î`ì¤$Xk;±£SM®Ï©½¬°ÊÑtýå+	ôYE9©\x0003öÙr¤s6F i\x0015ê¨X{4Ð\x001eÕEìk4´\x0013U\x000fdä6f"\x000cöFgGBA®èj­;í`ãR
®½\ö\x0001Å/\x001f4¸µQj}ñ|öñ|:'5üÙ4\x000e^Û>²hÐss\x001eµ!Sôcj\x0017ÆÛø°0ÞÛ\x001f\x0013\x001aÌ\x000eP¡±ûâm©³\¼ÂC\x0000ÂàïÅõDR¹V\ÿN=Uyw%/È\x0016'6_êOÿíOþ§wï\x001eÞÝþáJÛ(6âïÖ®@@u(øÊ
-Öð¥_6Óáîý}è\x0005fÌr\x0019/*
Íyó4Ú ©¦5\x001c\x0010h(¯y\x0016äd\x001b¨lÈ8ûî±#Ë_h\x0000 É§Pø\x001f\x000fm\x0014Z&6\x0014Z$\x001bF\x0019¾â¹!Dn<X\x0016Òp5tÝ'vÆ/¶F{bãCT©\x000b¬v\x0015ÆÖ\x000fvqL)^içûÀ
g-} UN\x001dÐ)\x0012\x0007Õ×·õ
Þvè\x001cvµVi´Vs\x001bREô<Û¦Ø¸q|NdTâ÷¼÷Þ²¦6xzzOBy­M\x000fcwNd(\x00036ÕKÚ ÉOLµº6=Ð,>ø@F
såÍ$x¯J\x0005Eè\x0018y5¢+\x0007í	Ó¹\x001d{\x0010*ÐËôdZíÝª?xö3ÞÐÏn¿ùþöJ£\x0010i`\x0010\x001fäÂô§_UøÚ³:º{/I¤9¨5\x0019i¼_l«ïÀv©C\x000bQ/¼
.\x001cÙÐú¹vh-\î
¿\x001a$"-]Ñð.è\Õ8\x000b\x0008Íg·ïn¾½\x0012A\x0018ªôËEUIÒÞlíÝûå¥ðF»;Æ\x0016´»u0¾Fø%&ü|æ!t]\x0004ðªCáW]ZÆÑ©Ôå&@S¹þ\x0016z\Ô\x0008£I3±\x0013`\x0007<AÇsçF//0ë"\x000f0c\x0012cÃÞ+­¥1\x0005@gl*a\x0017·<÷èw\x001fAG®1
-S£&u"ÐûÈE¬\x0016ûÐuÍFûs`çôØFK:_¢\x0012>ü·ÛÇoï¯%\x0010\x0013;ÇvÕõ¾w¤Uçûüq
s­á\x001ed`FÛ8\x0013ËW~£h]\x0014y}Ìªký "4Ñ>£\x00062\x0000Úø;p uÎ\x0007Úf\x0013\x001atªz, M\x0014ÏOEÉìØ&*XöÄÞ­öÄO7¿¹ûãõ\ÌäÎaÿ¤\x001cO]6Zh!ê^¶Í}@\x0013¿ìÄÍRÐNt\x0012KïÉWÒ»\x0004«\x001c;ÍW
%mQ	æ°d\x0016C\x000c4&\x0014\x001d[ÍW9\x0007«×9®2)t@~V\x0008\x0007]\Þ\\x001aþhÖp_àÄNIhH
¾\x0011!N\x0003È¢\x001eH·;®`©7qG¥ï}1å^\x001e$o³í\x00166è\x0006O­¶Ç°Ö®\x0011\x0011I Ù4\x0007£¦ñë\x0010óüZ{ç\x001fî?Ü|uûöáJámV7!êìör.°\x00065T®°\x001cm/z*\x001fLÂ,oã·òO}ÊÕG?äÙ5°!AQ\x0016²lù×SÝHh\x001b\x0012¬¹³êFr\x0015'Q+\x0007/:x}Df0xêIeYa¬¶%ùôöþj\x001cSI%¦I:¯¹)\x001co,*6:UË}\x0005\x001d(·\x0004k\x0013'jH\x0016m&YoÛÖXùü{%ê]ïóÔ§;íAQ35÷2§\x000c_[cÛH.§¤3êÒàTÖs<ï «ÐòAÆV\x0015
\x001d¡Ðs¥YÌØ+E÷aiq·&4ÜUÙ£ð\x0002r!O;y!ìÑ¦Ê5±»
¸Ô\x0014@\x0001k<5ÍRô¼~7+p÷\x0011Ê\x001f_¼½ýFEYeWÜ|ùðÍ÷WÚ¥³#VM»æ6ö×7»Ë×\x0016µ_8\x001bÈ²ÑýpôC]\x0003áÔ\x0001
Â©?\x0017ÚêÈ\x000cèôiÐÆ1Ýùtóù¬ßb¸ÄQZ\x001fÏ{Zi,>L£®\x0017E3÷5\x0001±Z>VÁ\x000f¢¨Ú\x0011Ý;Ý±¾QéÈó1¯£Fª$\x000fÐò'S¥¼j:æ$&>\x0010Ú ñ,à\x00088Ô^A×	}\x0018B¨\x0007jR\x001b6ò³+zÏËÛS?°3Ò²3fY1]p\x0016OØõ¿üóì®;\x0018|Í<ø\x001aZs\x001e~3ÐÙo,VBêa(½Zs¯ç^Uí\x001bôßÄpwèÜø±û¨ª£Ç\x000eøØê
¼?vPëTîÌy\x0015£F0 \x000bè)H\x0005~zY:þa ´T\x0002èáRQ6IÎ²ÓÑ0<\x0008Ö\x000b¿ÈÅlõÀ :ßµ\x0015¿|xúNéö\x000f×#zUÏª\e7Sï1TbvÿÂê\x0001öhõÂÚBA¾1üÌ<!¹_øçt`Ç6¡¡¡ªÓ@\x001cÈë©:ÇÄÖ2ø.Fâ=¡x\x001aK=sf3ëÔÈ±¦¤\x0003\x0016 XÜõIJ¹©\x001fM	ÖRZ;\x0012ÝÁ¯HÑ¼¬böG\x000bÞÅßF.½\x0000\x001a\x0014)°Ä\x001c\x001c\\x0011­n(ü\x001aõ¬L<\x0005\x0007âÁI=>´.\x000bÌ#²ÓPØP}Ð\x0005 Õ\x000e\x000fç
ÃBtìU F\x0007{¿.{ßµ\x0008flcÖR"sL\x0004z
x\x0019ò¢\x0003ÛÀ'=Á¤Êu\x0008¹¸¥öd_\x001bvûdì`Ñ\x0007vp}Y-«ÐÇøõíÍ¯\x001eoß}{óåíÕ\x0006Mäâ¡ºzoî!ÃùððxÑñæ£ÚÌE­¬fÎ\x000e~È³k #àøIÀF¯
FLöö¿ýéÏÿ|w='¢£\x0017ø0-:ÁÑ«áêÎ(mìÈW×jðÅj*%ùúÊùß\x0012°©TÔ\x0012ïx
µ¨\x000e¡vã02\x000e&øù¤\x0013ðäAf¤´À_uÀ\x0002»\x0016Ýe7Ls\x0006xu\x0000n¿gßà\x00007²­	\x001e\x0000¼"i¶´<5vðÄ¥ËÈäªQ\x000cà
À[A©Ú®Ú]xUº)Q3r¹Ýv¶¯÷\x0001U\x0016\x0005+?ê\x0004^å\x0005Q
ª6ØN9s»·Xúß\x001e\x001e?Ü=ªîÓÕ&WZÔey\x001f,NÇ\ë\x000b\x000frÙõOCü2¥)\\x0007÷\x001cù)L]È%e^h\x001b°nÐ½\x001f¬Ò³+l+Nh´|«(½\x0015s_Ôå0àBz\x0019nZ\x001fsX8kE ÅêÍsÇY¬yC¸ðÅã_ÿr¥\x001dZ
Û7×\x0016ÓY¬µ­Éâê\x000bÓ\x0016¦K
aâÁÔÚÏSuÃ@\x0006¦d8]ªòdìK\x0015GJfi¿NlT>«\x001d\x0003õâ\x001dQÇ¶½\x0018Ûr\x001cu¶ï¯ï~º}w­J¥/l\x0007¨C·§=;\x0004<w6¤6\x001eâ+%¶\x001aßg¹ü\x0008®ÙYý¡{§e`o>L±,Á-#{m\@	\x0016i93äþél\x0019\x001c¸jdüêñîÝÃÓý\x0015/ IÇÚÏ\x001e³5'X$9í^Z{ö@±È\x0018è_t®ºtï[7j÷©q©¾m×³=\W\x0017\x0017	\x000cÄ­Èþ=\x0002LÁLÕÎfv¿AcÅ»c	VëX,Õs¢<Y6Ûav\x0006Y\x0015rÉÀwi­¦/$­É(9zèµt\x000f"H±êÜ'=4;ÙW?\x0015Á°qBS\x000f5ÂªlÇÆìÒ²Á\x0008­\x000b#´ÕT\x0007ÍýôÔ-
oß\x001dpã0R1-\x000b]*ª¡Ò \x0003[=³·qkì\x001aè?\x0018`?a#i-ïé¤Úx³»FËÌ8òihðz#+ÐHµs\x0014Sév!\x000e_K¬'î§·Å4­\x000bÓ´É_éË¨\x0015{\x0016\x0004á\x001b¨úÉ\x0010\x000cý©b\x0007\x000cØ$\x001e©Ý2w\x0004[`=û ÿ²uøÂDÞ®÷úË'¹pUÄáJ9vè	=Ó¾Ò2.×Â\x0008¥NqF^¡u-#yU5¨vqî\x001aäìÍÄ\x0004«a~\x0003¦PûZª*í­»ª:]Ì2ó°½$®V\x000bØzáïo>¿ûöjÞ!Zßaá:×Ûyü59ôD-m*É½¶LÏ8:2ÏmËOQ
s\x0008uk\x001bØy\x0019²g¡.ÿ¶ÍÒÐ\x001d eÀ- ôF¹ý¨ \x0011ô¦6i¹{+öno¦SÂ\x0005.\x0017y\x0003l­
ÏÎ=f\x0002âîÄ\x000e0Ü\JÇ1í\x001b©\x000e*Qÿ¬I\x0002Ñ¿ñáñáþÃµê}©,	Hû²#¡[\x0016ùI\x0007Cæ¤(ûÚÈ/	
m2òq\x0016<¥È©n\x001e\x0008¦\x0014j$~`«\x0018Þ.\x000e»#\x0012öÝhß·àãÁu<±ñÒÐ/\x0000v¥Z&Æ®Fþèª¥Uóö\x001fÐ&È=.ì3ÝEòÉ\x000cëTÔVùe§íÍ¢#GÑ=Äÿc4£\x001aÉrußü¡%úbÔ:\x0013Â\x0008²Ü¡\x0018¡ë8\x000e{¢\x0017KÌzT:3öÛ»÷×)p'Üût"\x000445Ù\x0006½æ\x0011\x000c¼¶÷mL¶L5*(bFwDî:\x0016S"ñµKÍX®ÊTïT\x0003õ%àªA*Ô*ï>DKè§\x0019qÌÓü¾{51ªèÃâÑ8¢êSù£\x0002\x0001')ËùEÙlö$´\x0011Z¶E§))§ÍT8V,QkãEÈí@0j"ãhDuH\x0008HúÜ××XúÁà\x0011AY~t!\x0019^íÃb»\x0015ò¡Ò
I²\~¯á\x000fK/òc ·ü\x0018?\x000cV§lHP6\x0008%\x000fêÂ¹ÿ]h\x001a:ê\x0004\x0003õ¿{4%y,±ïßÜ©ÏûÛël~Í¢\x0017ûÇ]â[	ëuç\_ÖVà T²¬rº2\x0012À*G\x0002à\x001a\x0018%$¬ÌmuïÔ·]-©+Å®0$«å7õSïÖ\)°We\x001d\x0013^VãrBO¾ÜG._FJïoN~\x00159\x001e6\x001bôÌ ð	ÙAIÎ¯Ð£ØèÆÎÿ\x0003j'	Z±!'Ê\x0004S\x001b¬A\Áó1¹ù\x0012àêÕ»#§@\x000f

\x0002\x001cêÁÄÜAã§:(» Ñ))ñðTíÌ\Í\x0008»þö§?ÿâ\x001fï®±Å¶ÌI¥t\x0005U±Cè¶êÕõ\x001awóD9ÿ¤}ï©,w{CjOsiSäÝb«\x000fhb«§\x000cþ;Ú[ \x000fa\x0015u!èØ\x000eôr6h¬\x0007ìÅ\x00143\x0011óbË\x001f;8kØ\x001bM §/ÞÞ¾ûp-¹ì\x001c
\x0008RwÙÆ"ñÃ^ÌÏèEKvQÊ¸qdáøÆéz\x0015¡mdO¹ìXºÈ¿ªGQ3XÂ\x0003º\x0001K¸\x0004¤ÊÄ \x001f\x001bÎVÒÚ¦6p
ÀÄ\x0005¤Ý\x0006xfÏìþÔIE°û\x0015G¿=\¯o÷Ç®4¦\x001fñrÏ·§úZÚ·¦öÌç\x000f?\mwÆäXá×]uI¢Yð:ÈªYñ²áÖGËøÇU\x001ci¤\x0011~J \x0001ÁÈª	²
6Ñ|\x0003H·
¤¬*lquò¬rì£¥®\x0015/åîn¾¸}ûðÍ÷×6Hj{.º´ë\x0013j1íü)h'ðkFö}fÐ\x0003¢gz@Ï0Àé§´Jnº©\x0015J+%«òÍ,oÐ0 ÷^}ÐÎ\x00179 ¶\yy½]Ø°\x001eõÙä|ÛÛÐêsÎÃ)5Ò ÿè¹X©\x0019Ô{iâ7\x000fOoå?ÝÞ|uw-
K
yi´vÖ(T§¢½\x0000\ýTt|ÁY;Ó÷Íø°{^XôªÁ·K$%9\x000c\x0013åù­ofÒFæ©\x0015¢Ê»eÜ`ç\x000eç'2¡®n³_MãÄ©w×R\x0007ÈÔ\x0008z#\x0019_\x0013\x0019>,§meh²¨í\x0010\x000e,Júrµg7\x001b8\x0007k\x001d \x0018kïg7ÜAohÆÑ¯¦QÚx§\x001ar`>,öQeÈPeê1àÅ 8.^¡\x0011£Ú{­\x0007\x0002\x0003\x0003\x001b\x0005\x0006Ô0*ÂÄÎ#\x001crKs·lðEã*Ø¤\x0013X±\x0014¤\x000c
Ò±tÝÕ\x0005ÛTÕEüÓ¹\x0010ôáñmÕ{ñ|\x0018«\x0003¸Fy\x001e¿:é\x0010ã^ILq:ú)Ï­E^4EeªÞ=ýxMc\x0010¨xÚ=~Þµ\x0005Ã,©ü«4Æ0Þë\x000bíLsx'Y2#6÷\x000eÅ^Ë¶L§[#Ñ®\x0002 »æCL$\x001a ËfWÐ<úbBÆ÷7_Þþt5EkW\x001b\x000fÖ\x0014ÎØÐ\x0012\x0019Ih-ÿ\x0015\x0012*A\x001e\x001e&\x0010io;\x0015¿3Ó$\x0002o\x0002ÄZ²å\x0011¿6ß´¥Ì0÷ÌµHðÞ@ê)Ø*b/ÜÅÒW12±÷é\x0014IK\x0001w¤ÖXu­1\x0013«ÖÑä¨GÏ]á¹c!÷ØÔ=9
6+É>±eÉÖ\x000c\x001eÂ\x000fWÛ¥±Å)°g¥uO¼ÙoºPçú¿º´ÆsYÄSG´ç¯rHÈëÎ|j,Fë£"kÐ\x000c\x000f2\x0010\x000b$$¶\x0010¸,°½&2ì#9ÚÜ\x001b\x000f.ÄÝf¢<\x0005\x001b\x001c\x0007oÍÝ§t¹nþíñö\x001bIn®&!\x0012Ù\Xý.ÎM× ã¢;W Å\x0017Vþhùþ\x0016Î³êa½±¿JÙ-}ð\x001aìô8­deTTX¥ìxN(Æ´Ò¶aéÇ.@órÿðIÐÞ\x0019òeSåúM\x000cår'}FÓ<¿¾êåãLúêþ»k
nÑlCOå,ò;UVöþG¬é >rwÜ ¢ÑÁ/yv\x00154µ:B\x000elp5X®c£æüæöþíÛÛ+\x0015ÕÔºO°³ds®\x0001-WB¤2J¯©a
«6:4¢S[,c¦\x0001Ú¾
	\x0015Å·A	]væ]\x0003(\x0002BU,\x0013BÇE« LË÷£§Þ]öè\x0014Ú@VèÂÕ\x0006í\x001a6ÛþÐÙeô2Lj¤ÞhWp|TÚa²üfla\x0002la\x0005ÉKdié\x0014­Õ\x0005Ó6ÏÐÜsî3Ù7WË\x0005UÓz¡(3ãº>dò¶Xë.ýE\x0013\x0015Ú²ï¤áÃ¼ß>U½+q'ÕÆ¼´\x001aÛ\x001c37¸\x001a
î÷Î+\x0015
x #;\x001dj§\x000eBuÆ<Ûg\x000eMäjûüö··w\x001fnþåîéwWÊüSãVÂtª¾ï
çTãô^ÝÛ¾ÐNA NqðK]\x0005ëZ;!OC6F) «Úênoo%©ú wÛÓûw×\x001añuáñävPÚn\x00079­>DÀ^[îo\x000c\x000eLUÆsÈZ#H­»y^\x0000à
$[\x0007{Ã¨Ì\x0007ø¦\x0017¶]ð£h\x0006ÐAÛÞz\x0013:\x0003´wCÕ\x0004Ö\x001e«·Á'>¦Eµ5¡1a1$=ÛëÙE\x0007è	8ÈÈVYXr£u{¾¿ùçûÇwß^QÕ!HÀ±È\x0019ódWñ~\x001729ÏZÆ+\x000b».$Ceáø$ï-@¡0æ\x0014I<$OuzelV{NhØÅyÎ<§¡:~YÞ`\x0013¼&ô^ÞÕïóÇ¬lÐ$àKÏ£ãbÅË8êT
²Øù©Ùb6¤Ê¬èám\x0019WÃá\x0018©®u§µn$\x001dT´$oU¼\x001eì8?{xzüîûÛ+í~mñS\x0004#X`\x0005æ^ËS\x0007äµ]ÄÆNJ\x000bUpüã%1t¥Î¬\x0002i:È*äjï¤	]\x0010:@\x0000/«ßT^_:D{0um\x0003Ô¥ÐWò³··²b×ª&È·J?3ìæóê\x0006)NQ¹ºü
åAÛ'$¾}ä§\x0004Ø·ª`¶hrÖÊ«à»©´·!£\x0010|"pQ\x0017`²»(n±Öóí¢óËPMÐøúñAµ\x001aÿp-\x001eV
ÈýÍµÝÛÙ\x0017,£ª\x0010Õ*>Ú%!·%¸>ø%Ï-Eþ5uXùöîéj]ÎÎY¶êØ3³\x001cD 
\x001cJ\x001a}ÿ×V
6rÏ2Þ\x0007°6s"¥`Y~8IòÑ-r¾\x001eq\x0004\x001d\x0010º`4\x0019gUÎÞXà,¦¡moÓ'4Ó5\©ÀN\x0010Úå}¡½gûëàôÊöóªþõ½¬àíûk\x0011ïbD$oªFt:²Ê®îåøÔfçµ\x001dà\x0002÷.-å`ý%½Ò/W¡.«\x0010¼ù\x001c\x0008ywk´ §u}­Ø\x000c\x0014çöØìóïo|xº\x001eÛ[n\x000fºNZ\x000cçëºj%{ÔTøWX\x00113Â'6\x0013×üÈ\x0011®T¢ÆI\x000eêi	´=læ « \ÕúïÎpÝI^\x0008¡¶SüÂú´¡\x0016v¦&½½C³6ÌúÀf®\x0007\x0018PËÝÇUîüè»AÖï\x0006ù)u\x001f¢ÌJHC~¬\x0002È»©}o¹-z%\x001c!
\x0018D½lYà\x0005zZØ\x001dA£ÓÀ®> ¸mÁ]Ü\x0011ÔèÐrùF¹3³f\x0012i¯\x0014_d¨ù nDç¹RÀ·(ôè^ØÉö,ÇìÅXíè§<·
ÖÁm´ÿÇÁýáÃÝNsòän¡c¾çÚv÷¤î¦äk;¶­´7qÚÛsMøK²ã\x0012d¤­¼l\x000fÓLè\x0006Í65fg+¬Ã[ò\x001cÙ×f}{Þ6@Ó,\x001d¸Òç§\x001d\x001av
\x001d\x0004ãy\x0005\x0005õÓÜ¥ÛJ×v\x001b\x0007­_bðQæØ\x00157eã$\x0012\x0019ë	~ê\x001bo\x001f´\x0013:2´U¯ÂQñ<,ÅÉ>\x0014ÿêe|?±+ÚðÊ¿>¤J\x0003¤OT.¬êL±\x0004\x001e5ÀÿåíÓãýµDåà °6¹ã0GAss\x001dïtX+[¥\x0012Ç@ß\x001e
øî\x00173=2«i\x0012Æàþ\x0008:\x0010tÏ§4\x0002(XàÂñt±¨q5\x001d\x001a,W\x000bë¼WÖl'q±0HTð-ÔÖ\x0007¿þÕ\x0018ÆÜ"#]äk,.j87¶K\x001c¿ª²¸ìÆU\¬NÝ0
¬Ð8ù-+L¬ê7IØ#è\x0006ÐZ;\x0004ñÑF\x0019tÎÌáÕ\x001cÍ:1,¾êÍ/ï\x001fÞÞýöþjÚMÞ³@gËgVuSµ½]Û6ú\x0015zûXêEÛ¨Ù}±¶¤Î4Õà#\x0015Ùå«Ù´ù°AÍ§In\x0012÷H&o1Xc&V«FÒ\x0001iµ¬¤UÅçVl¼ñ~A6u~³·\x0006n~uûÃo\x001fÞ½»\x0016gÕHE4
²OÜg	r
\x0015v\x0015êxQJÆA\x001ea©î(\x0001'CDpð[]\x0007ë0\x0018\x0011á°<¾\x001aXti\x0003ÖpNð\x0004\x0011|Î]QzÑ2ÐGÒãâUõSÙë@C°\x0008\x0003µ0ìq\x0015>A±L±ShI\x0004\µ\x0008EÈ±{[+~BïZñ²þ¾áø¥|Ñ4Ú\x0013ZYÞTV÷\x000fz½çm	:¾½Ú&rHü
N¶}9')É»A
êwû¢!Ir(F7L=ýuøà\x0006/öôSTs\x0000â\x0002\x00157ì´\x000cyøëV#á\x001dØ\x0015ú¼!tð£¯*lwù·\x0018º\x000fqj\A\x0013\x001a\x0018\x0003Aç\x001b@\x0017b¤\x0007G­¬=4Í?±aó\x0007	·ÍPÙ\x0018(n4vÆ\x000f7ô^&v\x0007ìfU[>Ä*q--kÒ
º!M\x001b\x000e3÷òò7ïê«8É"³m³¯{¬TyØPý"_aWôï>'\x0002¡ÁqðK]\x0005KSË\x0008_ÿö§?ÿÓï~'Oy¥âw\x0004Ûv¡.¶&\x0000£Öúu
ÅkËw-¿ñNPçoL»ï?%'\x0014À.ò\x0004B¬nP¯c \x000788º¶}À°6O½Îó\x0007ØjÔå®3¹!Acî_üþéÇ»Çk½n9.(ûn5ë²l[ÔTµüíu|lï2.´3¼l\x0015P'"hTo Z9)pÙºÜ¡uÙ\x001dp»ó°oFªi\x0000®5«¸áéýÅãÝû÷\x000f÷×âD\x000e¨ü\x0010\x0001ØË:··Sú-õ²Êl\þ¿Ô½[reÇ±%8\x0015¾[°x?êOÔëÚ5ê^5¥ÖG¥!3Á$¨$B\x0002¼$ÍdV¿5A«û·gÀÔH:Üc?|ù\x0000UÃÆi«ºâ&\x0017âxDxøsy\x0013\x001c&.k3\x0003åð\x0012\x000b±×Ñ
\x001e75è!îÈN 7+\x0012dä`èBð\x0010ÅÊm«G\x0014.b£E\x000bÿ\x001f®¿¿>\x0019M~@f´j¢ßRO®ùèUd/]æ^è³Ûè\x00019U©'\x0017­`×l?ÅyF\x0014ßø¦1\x000bÐ,XI²¿z\x000fæQàt½fc\x000e©çòñR__üñúûûë×w'kÚð\x0016kbk*qc1l§XD\x0012ñÎ¿¬\x00055£k\x0018ÄñìXQ>h\x0012ûå·ÄR¡$Á«\x0016µú=6-ØrUH8=ÜÃí©Ø(0æK\x0019¤/¾¸»ùòËÓ\x0011¦\x0010¿&z\x001dÖl>cuÚ`±ü-1X_ÜaH¬@\x0001_A¬ÐÜ ÉÛÉ¤
Í\x0019ÑzG#MèvÈX\x001cßqq|a*¥À\x0018zßü#p³)±UGD\x0013í$¶pê¨¼B"SEà\x0011ó©µføFüñtµ	UMâ F5ÍÛîÈ\x000f\x0004\x001b^º\x0013~ât²£\x0006\x0012OÓßò¤\x001cFYqÍ?³Ñ¾¾<Q\x0015!1Î!Oc*\x001b\x0017R\x0014c7³]ü³ÛAµvâ >ù-OÊad3\x000fúÿxýpóÀ¡Þ»\x0013\x0005é(÷\x0004\x001eóûe	²Ë \x0010¸$òÜ¶%\x000cÈ\x001d\x001c] F\x0003M~ËSb\x0018
H\x0019OSýýÍ»»ÛëSÙ¸ÑVh2ªíÞ/©ÌM»Z
¹\x0007­ÏÎê\x0019Ì0ª|üÉ}^S©@AO¤à\x0001¡Çß\x0007ös\x0016ös¶r\x0016`Û_\x000b£8b3- J\x001by\x001e·È4³ç«ÛÓ=¦É\x0010sÇ1­qÂv2ð\x0004ÕáøA?»ý\x001e\BE\x0014\x0017k1")âs@÷Õx\x000b\x0018aePÏÓ¡½H¡wrîMH	&h\x0011 G8lþNÍÞñ\x0019Ñôð©­¤)ßÎâF?ÊLõ{³O \x00063\x000cA\x000e\x0006Öd\x0015ªp¡òeÞ~Ñó0(\x001cÛ\x001f7DuhñÄòX¥ÝW
\x0011­ç&`\x001c«\x0014Ý¨NÖäq­\x001e\x000fÃ9-£NÈ\x0015u×`¶ñGÕ7Cz§\x0007§L0ógÛ+;\x001aä¨{f&?åI1ÊßãPé~~õæ««Ç·§Ùv¬+tÄf·\x001c5ï]ËE\x000bufÏÀc[\x0012öz¨á/yR\x0006#\x000f\x0001µ¢¨D¼¾ÿæTÞ\x0001¥@qÁn¤S@Üm7\x0013^¸>í}\x0001äð\x0005$NE9¡²ºÄyï]
º»Ù1ñK-Ç/¹ìEÃ\x0003¼Áh[hú(ÞÚ\x0011c¿ñ­þxñ«7Won®N¥
Ûy\x0007°Isë\x0015µÆIª\x001a¢
4g\x0018«\x001f\x0014bõAïbîÉ\x0010äi^"PCfÿ UÝ¬Ë¨#\x000b\x0002në\x0008èEÊÈIz\x0010\x0002'¡.½üØ÷wo®ÞßpR\x0015®sÌÝ½ýyÿê3#\x001b
?¿&kèa­O=\þ\x0010G'Â?}"kÞÖöbÓ<¦À/xû±¹¦äÌîïØÐàTÿ\x0002½Ó¿¼~øåïï\x001eßvBÅç\x001eO\x001cÇòy\x001fù®Õ¼¿úþ4²²¥ÔÝ%\x000e[Ç\x0014Ë*ØÃ²2Ô÷Ïé,e%\x001e]P¼bÓ\x001c+K³\x0006¨ù±\x0014=ç\x001a¡ØMTÜ*{¢r\x000eDõðÐl¡»Ç\x000f§\x0011Oµ\x0008!¦ÁÌzr±\x000b\x0015ûÝsÄ\x001aò
I¼\ÿÒþ¿«G~¹ú\x0012O¤¦b0I'¢\x0003H«ª¶î\x001d\x0006ÖP\x0003=×ó$ìë?\½oüãÃ±¡äÓÔS-qïÉ¡ã½Ë«zÊÙ:fîg*£4ÑÅþÇ§%*¶( §µ«¾ÉZ
6~²&§ö¾ëç²ÓÇæ¡Ý_±qp;gKµû¼\x001bºs6xñÜuÞ§åÎÕdU»Á\x0019É©\x000cåô/W@þ'^<k½|ìª\x000br"jæêë²Ô¹oÊy
ÊK\x001bêzÉxìË:"ß\x001bwéò\x0018ÃªÈKuBVdÆ«j¡3¸|\yqñ»YO¡\x0019þY\x001e¨T\x0016º\Iq/z&;«\x000fuþ¹´ÿúÝqûæñöæÍÍUj8F+bù/\þ«\x0014Ì\x0006½-Áj]3¼%\x0001/¢\x001cá\x0014ñ4Ó\x000fw\x001f\x001eßwþÿdY2YÑÿª·¢éÆTP0¯þßZws¬ÕøxñÙ=u!7µs"{ÈÇ\x001c\x0014@²nÎy+\x0000§|VUÒþxü#OÓ]âh$[\x0005{\x001fuñ0Siÿ5ÉíÏ±§êö ÄÐ\x0014­\x0005\x000bÚS-VIiÌ½½\x000br\x0010\Ìdb\x0003g\x0003/\x0005Á\x0013·\x000fX[Ã\x0004?mÛ¤YêA£íÏÁ	¥ò¤.\x0017ì\x000c>=µÇO\x001eíçØ~KÍR.)T\x0019ÎrÄä\x0014\x0010Þ&WÙ`	¿æ	HÙÅêãXÍ\x000eï÷¹\x000c\x001fVø<Ï;|ÙÍÜZzp°¥É\x001b\x001dó¯¾ûð]Ì£iåDûÕÕ·§ò7U.¦º6\x001f¹\x0004yxj¶j~æ\x000b\ãÊOõ!öêõ®wùQÔo»\x001e«Mû¯±\x0005¶ÜzëPçÒg¹\x0019´\x000fn{,Ìøh@tÅ-³!D)äfñxE\x001fçÐq¥¹ÝûYõÄ-\x0008\x000bo<«
©4IH»Lò²Øuí62Ñù\x001eDñ&\x0000zä1²!ëk¼£g¿£Û
è\x001ejÓ©¼\x000fÜ K~\x0010£Ï×ÅÚ\x0017/tCOpÓ¬	%!:\x000f(²>¿\x001füêõ/~â\x0006<y{ú\x001f¸zê\x000f\í &éêÕ\x0008¼¬\x000eÐCµYù\x0007]qeÿj~¸ÅxÚÛ_~ñxªð,\x0011fAÜÃ¬`nÿ==bWÓ/©"¼ãîé§\x001bV¡É\x0007âTá%µ ßyÄ]vE#Ò²Y?\x001b4}Ú­É"vÚq)*|5ic\x0001!·%0!¾g\x001b:ÚªU<\x001c~:Ðýÿ¡+º	NéHôµPÑ\x0003¬=z¸\x0006Nj7:\x001e<ªË9}wl\x0017w[\x000f'(T%\x0017ï2¢;ææS©Ó§
Ý×=	ÓÐ=¤¤\x001bzB»å&F(Úözv©× H\x0003iíÅ´£çà\x0010=ÄADÏB21ÃÚ©MÇ¦\x0014z¤\x0016Mïµ²¡{¿(MxbÐJ!³\x0005ånûÎùÚý¾öl\x0002Ê=©ÓNÿ\x0002¢3sOnª¯»Ý9Q:Oé+zS¬6õ7pú´[ôÔ\x0016ÈSt:£Ï\x001eÄÒm\x0012"·\x0012·ý¡\x0008¸'WÅ¹vYà\x001a#oh¦*ÉUÃ;ÛÐ½Ñ¥\x0017þÕ?Ü¾;Îe|ìlÁÜÞñþæãÇ\x0001+Í§>,\x0016\x0015ªÍÿÈ\x0014Ök`/\x0017U\x0013ó\x0012¯
sn\x001dª0Ôæt\x0011ò«²;a\x0006s\x00034f\x0014Ô\x0004
M\x00019ô|w0±6t·X¦4î\x0007¢{¨âª­\x0010Au\x001f\x00162½&ð¶S\x0014/¡(M \x0006õU\x000cä0Qeî$\x001b£VC\x001b<}ÚRL5K\x000bË:|Z|1\x0016ÒSÍÆãÕëfq\x0001w?¯Øbd\x000cÇ6*Eß¼:\x000b^*²Hô¡èqçO+|ÜJÜq/\x000bb¢z\x000f\x000b$îÆ«f
]Í\x000eÝÜgé\x0000GV(íà\x0003÷ÐÓë9º\x0013è\x0015Ñ
½¡§è\x0016ßÎ\x000c?­ðÅÚ\x0007®3\x0002
MìÉ ¦ûXÿ7#i\x0006O¶ÕïIIO\x0013\x0001A0g\x0002g«côvzWCzõv¿­tàw-M\x0001`¸­Ù:4wh1á¿y
ÿÍ_@UýSáõ
	MµX:¾v)\x0000ÿê\x0017OiÎ§4.c_?}-°ëí½zv-ª1ÓGmôåSà_
p\x000b\x0015mØl*
¦\x0019k¯9À½ã'ÜØ m\x0012\x0007¶`Ók&\x0000ÿêúÑÕïÊàüýõýëö2Ò3ù¯w·oNUÂà\x000bÜòÌä.÷[\x0004óHsEKdÖ}%\x00039Ä(«Óïd\x0017#ÅBx'³¼\x0019öxx#\x0014M?½Ç\x0018î¾ÇpSò¢_ª=d&à½¶èÝ¥Â\x0008külíüiE\x000f\x0005Ñ³Gtb_ð9\x001a\x000eEÄ©høÓ
ï¼úÚxãÚT\x001d(Ô¦dø\x0015N\x0007÷qOÂ}$\x0016\x0007\x0011`Fl\x0019b\x0015£­íö0|Ãg\x0001O]PbõV½6øV\x0001¾ûÕF?ñ\x0002\\x0004õè\x0001Ø
º\x0010¹ïq½ä Ù×Ò­+mY¯ðüiY®ÝsE¢sR\x0002Fh"ÇÐi\x0006_ÙáÁÝðÌ!¡T
½v\x0010Â
1tøÙ¹áO{\x0013À'Þu³Zä3oc»\x0004Üqáf÷[ÁwC'î)\x0011t6¡lR1\x0000o#§FÚ¿¨ù
ÞÙíÍt\x0015§²9¯\x0018Ô0*Ho]í\x0011ÛT§«Ou_=J±úæØ¡è]\x0010ùl\x001acÖÏàùÓVíâ½X}0	R\x000cíú
;Ûnpæ×Ó\x0013Ü~pBrõ¡]QiF4å\x0019à\RÅÉ1rø!UÿåAa«yùñ\x001f'ªOÈ.C¨´g+\x000cJ)^
K:ûüâ\x0006OåÂßOÖEÈá=ìíKöoµ\x001864-\x0011r
%°WÓöh\x0002Ïö£e¡@(CÙE£!pØÉÚCZoGßÓzú²K=Üj[ã}Éì!±'Ðý\x000e·®Y»\x0010© õÔ9áøÕÓg\x0001>îð\x0005RÐÏ\x0015ÑÙlOÞT4Îì¢\x001cÔ'\x000f9Ã§9|\x0012ðÖ	míR-\x0008w2Õeõp¥ßE\x001fkj¹\x0017Ôf\x0014|O4K{\x0006_Í~*£JF©lð\x000fl{ë,<Ä¾?Íò ó§­)\x0015yn\x001c@;ÆE\x0016\x000cUÏ±wÁ\x0010=´À¶ÞJÃ³ÁWôÛ?9flóÃÍë/E	ÊçWóááT¹ÚfÁBÀ7ç7\x0003Æsï\x001f\x0011¹"ç'sµ½déiB«UnÒjþs\x0014ÅaGâmù>Ü
^7n%ûæÃÅ\x0017W\x001f¾ºúñÿ>LaøÄz\x0018\x0017\x001dD\x001eÚ}«o\x0013\x0001¿_íöÿzç\x00194sÐ·½ËYîwwÊW\x0019áwÔi\x0006fwµ\x0005ë?Ønµþ\x0010\x0016\ÑùÓsj¯zâU\x001f¯\x001d^$ãª±RW¢ú¤SÄg¢Ä^¼r|þ\x0005¼ÈÆ
ð:Ä\x0013Cød»p\x000eÉ\x0015\x0001\x001f\x0011Þ
xsGë"òdU\x001b\x000e¾æ\x0006\x001f¯YÁpu\x0014'l_\x0012|rÝxá|\x001fQ\x0014MáÃ¾µ5ÈØ g×\x0013àm\x0006«Gm0üì\ò§\x0015Íx·û$ÁãÖ\x0006pÄÉ'Y]ÙéÉÉFä\x000c{o¬J\x000f\x0005xC-\x0012|Û³\x0019<}Úò8±HoÓû1°R­\x0007x\x001f<îlõüiË\x0015T'e\x001f¨ú@FÛM\x0002Ç\x0017Îù3CÏ"¥\x0018­L\x0013\x0007b½çÒ7KNK,ð3Ùð§
ÞÈ´_ !\x000e°x\x001f¼Gx\x000eÌ9\x0017Õl\x0013
ý¤vçåÁ_[áùÓ\x001a³ö\x0019jU\x0002\x0005;eH<x²ï\x0001÷u\x0019á·2Â¦þ J\x0011©G¢Gç\x000bî¬Õ\x001c¬þÕý»}sm^_|öxÿÃÉ¯MHroØõ£AFûÄ¥æåÄMZ/[8êhÛýðúÌvéq]Æ®¨ÍLÄ£\x000f
A\x0016\x00105#Æõ)\x0002æZá­ÙóO)\x0007\x0011û2µ9\x001c¨ìè¸'xzP3Æ)|{$SmFØàSÁæ{Èp<×²R4¶\x001c\x0012\x0015dÚ·=Qr±ûk/*qé\x0003Ö7´C[û\x001fÐ\x0016ø\x0003[¦%EÑà×\x0016Ï©PoS\ûå\x001d]§\x0013\x0000ýµ@Ïû\x001eü\x0001kBRàxåÜ_íwöÛãûxñoW÷oNU©Ý´d3ÍòEHÆù}*¹m¶Ì.µÚÚôê²cÇAÉ%ß\x001d`0¨×$!-»Ü,¯ÔçþiËkCw{¬9¹}µÝe;C\x000c>àe£\
UpÔéÂéÓfO\x00045VEÅÈsÊ°Mÿ^\x0008®\x0015Ñ
Ï¶\x0008ÞüÛfN[\x0002÷Âý\x001dF\x0018²=zÈönØÞÚ×"K¸,\x0015Ècx¿«a©a÷v&\x0019þ´Ág\x0019LkF\x0011ú\x0002=ÌM{ZùÝ§É{cx×ò-Qæ´\x0017ORoWØ\x0001v,á\x0018EÍµ~óÕëÑ%îÍÄ`r¢lOàV\x001eÛ¢ä40FJÝð\x0005®rbj«¨¾Pò\x001c¬mN`ðªú¶iúÀ6SÌúÔnèôiO^²U^í4ðªìBÅ¬ÞT¨e6\x0001½3\x000eWb.­?Üã
:í÷8úXå\x001e\x001bµoM¥¨D`Õ.þÕ;ÿõÍûÃÙ\x0017?þ÷7wïO×--¦ëMØ]@¿³ÝR\x0001½|és:î+Ð\x0007©KN\x0017
\x0005#Px±ª7\x001a®ÑãêRS¡\x0012Ñ'U]ê
¼7µr\x0014AP-}|¬\­AÕ*½gúÕ:ø;¸\x0017\x001e¾QrÓ<1\x0015ðÐYX¨Û/×\x0014\DªÇZd£ê3c¬(äúà)x.\x0002\x001cEn
;%4\x001aLjáÐ\x0014´W±òäqåh\x0010ÕÇ÷ä¢Ó§
=Ã),Ö¨êu1Õº£§c\x0005è_¿¾MUð½|vÝ®÷'S
Í©ÅgÞÉ&\x0002\x0011ääÝÿ^ê\x000eÿ\x0010ÁîRÃ\x0008öìç<%Azöí×îQ+j&çýñ¿¿{?\x0018ê÷º:9£J«öÌ\x0002±6¦½ªÒÝKwÅP\x0007ó\x0006éM\x001f\x0017ØoÒtîéÂw¯%ÛgD\x001e3I+xô\x0000.ô*S\x0012@p\x0013J\x0016¨Ô×q³¨VÚ;x\x0011J;9\x0000÷ð\x001aÔ\x001a»XÍÛï_Õëúþá«AõÚVá}J\x0002\x001e\x001cÖÊSFq3¿»ô{lx_ø¶O\x001aÚþë\x0010\\x0017#yXv\x000bÁµgF²vYnJJ\x0019Ô»÷½PÚ\x001dÊ×6x'Ê×L}zô°`§XâËÃ8ó¼£ïgjA¯1ª\x000f-3+\x0008ftjÖAæYÀ\x000bçÖò5CÃáqjÎ­	\x0006fúm2Ó\x0017cO¢Ê©B=\x0004\x0011â£ÓïTÏo>$§\x000f÷nçOÛQ­^FÙ¸cIÖ!e¬°onKÏ>7{l\x0006O6xy­M
2ÑiÚ¡ÏMeô:ïé¡äO»»\x0000K\x000f\x0019«÷) ©á{ú¡BKÀï\x0015Z4C\x0004\x0008£Ko(¥ÞÄÞmH_´÷·bó§
êNvìæ8¡kî \x001a4g\x001aÈÕ_¾×
>í}¯¡n¤ÊMæ\x0010\x0014\x0004±\x00186Å|98i\x001bvÙ´¶N\x001ew\x0014A=AI\x0001%Óó,Á\x001füâ\x0015?­ð¶
C\x0002§\x001eËD°Ô´\x001dÇÞÿT\x000e9¢
½\x001a\x0017ê\x0005\x0010Ý*>\x0018D\x000f%*±\x0002þÕ\x000f_}sózÔ½þÅ]SÐ'²%ÛqÆ¦Ow\x0012\x001a\x0016²Ç\{nª©4Zrt£DBÖ¡ø.<îòÙBñÒ²ËG\x000c¦J\x001b´*\âP|<ô¤mÐqïIk²Ê\x0010_£ã@ÎØ4\x0010R±Ã¸¦@÷;zÞËÁª^öÂ\x0016ÊG5[}\x000f6èl÷æ\x001eb¡\x0011qGW° ßWe\x0012ùÞP²v¨6ô7ª¬
gE·\x0018Õ\x000c6Éè~³ê_ÝÞ¯¾º?Z¸EûäütE5`x\x001f7ÛÊEEÏd	Ì½~a~ý°u\x0019ra·¶ª±NCýÏª\x0006BuÑ´§¢lúYÛÁ\x0008\x0003X!©\x0004ýÂÞb<ÇÞ0-¢¡×eXs*ªI;bßö¡À¾Õ
Üî}«©\x0002KD;ÉVu:W¯VÎ}ÔÇÐ\x001d\x001d&!\x0011ÝÛÐ¼Glq=pq(\x0008\x0015ÐÒe\x0012q(
b$NjÕ3\x0013R\x0013\x0001-z\x0005¨\½\x0010Õ9\x0010ûWÁþÍ?\x001e»b¿üÃÕýÃÍÕJÈÚùJP"òFK]÷»&û)¼è
\x000e&
Ú}· l\x0017"ÕÒ\x0008¦VY&\x0015-¶Ù9¨¹$«Ët\x000eþÌ\x000e-ülöÐKZF\x0011Ä2Ð¿¹Ð.ÇaÛ¿~ÿÍÇ¯¿<lûÿüoÿãÿøøæ=±h]\?\|qsýøpw\x001aVH[Ö\x0002/®ù\x001a«\x0006o6*´ÇåeDÜ\x0019î>8]ô|ïN¡Ï{2Õ&1$©Á`>2ûÒ\x0007Y\x001e\x000c\x0015Ø	Æ\x0017#\x0012\x0007«ÃÒXSÌÌp\x000cØðÝ»«·ûþï³±~wwóñT7\x0010Ëj7o\x0005\x000f(\x00164ÿÆ)âû³\x001eªUºôøýÛ[V&¿çIY\x001cI
Þ=¼ûë»A\x0008Mª\x000b\x001aæ}"ÿÂø
oO{YÖªì­ª	^~kÆñÀÕ\x0005(Éê©î°È
xK]n ÛÃ\x000cæõlNùCSÆî÷¦\x001c¼,XµäAa`3µ1*JiCý»woD}ý¯î?^¦ÍÆiÊ¼NóYø$.M\x0019.ð­%ã\x000fc_Úü'+ëYbý'EqØïó÷7Ìþ?a§kÏã*
øí¬AD±-\x0011õó>¿8÷ÔÄÇ?¸t\x0001"\x000bM»ñ}«bFÊºéYL~Ä
=íý3q=%i\x0002?pÔíà;G]òUê\x000fãÅHá0±\x0019{KW\x000eÚ\x0019Û éÓÖY ¥â=fi,\Ä_\x000f\x0015;ø^á¢ \x0014*]\x001eB{¿pé1èÁaþÕ\x000fß|¼þZP®þïä\x0013\ßÓmà2¾\x0013ÝäÐù\x000cf#\x0003H4\x000e·X\x0011\x000b1/ï\x001düsZªKOõÿL~Î¢8ìËû¶è\x0001ÑõÅo®\x001e?|us{w\x0018núÏG»ö\x0010ÆJÕ®µ.Á»ÈåÄ3­È:Túuáñü¢íû­BV\x0013Ð².\x001e\x0002ÛÍÁãÿ¡\x001f{\x0007ßû±ñPFX<4\x0010\x0015<2UÏµ4D¦9çOÛÃ'GZj\x0016WÍ\x0019£\x0018Á\x0000B{3\x0002~ï!Lq§\x000etÉ`3v*	+ ·Ég?ÅûíSq÷Ë\x000cÄ@Õ-i~é¯Þ¿üæúâ7\x001f\x000e
Ç»Ñ¹\x000eOk_]c\x0013Â".sHM3ãn\x0001ûèm_aÖ\x000cOjzwÿãÿùíõÿ'\x000céCIZ\x0016\x000e½>ò4Ç»·÷wÇÉe(¤÷R)\x0012RósÊ*¤Òð¢Å7Ç\x000fFÉ½´Òñ4]w+îÝíÑÂþD)²/Sý®É%­RÙó<EJ±XÕ\x001by\x0016b*xn\x001fîn>^\x001fBzÙ¢ËVãâÐekÖ§ý\x001cE{ò¹IÈº_\x001cò\x001c¿\x001dV~¢ÚÉ((¡°¡ºÕZxÌe9;]$'^AëW\x0017¿¿º¿¾½=:
Ä\x0014äE\x000bn\x001d´nÛ£#BÔ×Lãt½\x0017\x0013÷ü«·+rýË¿Ü\x000c>ñ4%\x0007÷ÍZ®ûZNSíS\x0017A¥eXØ	êpß¸2ð_î>Ü<\x001c\x0013\x0012*¥\x0003\x0000ë\Nk°­
\x000b ^ÝaòBkÿñýÕ\x001b6\x0001þ|ýÍÓ\x001d#QÀJ'm.\x0002j÷m«B ÞÿÂCÉÏKD!\x000eôÒÇ>þó4ª;\x0018çÁFjËØ\x0012¹zn\x0013\x0012StÝ]\x000bé\x0017\x0003CòþÝ©ÄSä$^íE.Óþö;\x001aêx~hø¸ýúº­íñ8&ôS¯Z
ð´ùèw]äÄ,0\x001f0Â
\x0019Êá\x001453òáúêñT\x0012²;ÿ\x0010IÈ\x0014¶7­¤=ðëcnO\:?	Õ¾î¯Úoåî(¦æ±¡ÎÎ5l\x0007)\x0017eµêìb.óÙùlÑ\x001c¯\x001b½k··7§ÒØùÙÄQbÖ.#o\x0005;O;J4øìTv´Ãwíó«\x001bÍÈ')É\x0018\x0010/uóI(©÷\x001bW¹<Î-i)øÞÿô0Hà|â]³5$püíÒ\x0007XhênþH4ù2ß\x0016u\x000c©\x001d¢oºèêñ»SyþÁËØ)9n\x0012ZêÚ\x0016	ùØë£ÎJBÖÔÑãÿ»ûëïß\ß\x001eyC>M!æýËÖÜÚR\x0017ä©²Àm\x0001l¸´çv¬×þÚãÅ\x001fîn\x001f¿¹¾}¸h©ýûSJ\µpël1"rë.Í®\x00060Ùú\x0015N¿{ \x001b\x0016\x0014Õ_}|sª R0²\x0006°ë§º½s\x0018ö¸Rôù²Éô\x0019d\x0003N\x0002h\x0012CjqõÜJb¤÷%»³\x000b'á$çÏîn¸Ë­]»w÷w'ºlY\x0012Ó³9¹Ví\x0011/\x001du\x001eÈmJ\x001c\x001183\x0019U)£Ûß?^ßJoS
/¼n¡n\x0017Ìæû§íÚ\x000c&\x0017ÏM:ÞJé<~ùåõÅ_*:Ñ\x0005s9J¹×ÃSÛ;¶¹"ÈgÃùIÇtîßm\x001eÛw\x000f÷W§üç\x000c¹REä?µC³;lþÐÙp\x000eR
Âaû¼\x0019Íí}u{K\x001d ÇòxÑ|\x0002!Y²Öf\x0013^m;bA±<À$VNk|\x0018LúTUíåeó6oÎH	)°òYlÈRÒÙÙ)ÇEDdí'sgK\x00196ÌÒÐîY°#!Ë\x0011"v!w~ò±#ùÜýp"s¨ýE% RÖ\x0003D
®[I»o¯^á¬ö	HÚÕÅ&\x0019=^üúúþf4ÙíSuQWÍú´&³.jv¢ðiÛ¿yiÏÎ$Y\x001f¤÷WãîÕOµN\x0012ÑÑÜÉºjkî5tæ³ëì<g&!ÔÖíO^üúîñÍÝ©bÙí>Éç¦ÿ¸-H[vE\x001d¢;»èãg&tzÐèTõ41+ÃoÙëH7ª\x0010vºÌgwÁ²\x0002ºûxò/þmÐJõ©n\x0007¦Ô¨·°nn\x0007eöÚµÔüzwvÖP\x000e\x0003\x0001ÐZ\x000c ¡
8XEËÕ¶[X¶s\x000bx¤~õm{»N'\x001e_k©ð5¯u\x000f©"ÖO4ÙÇÝC\x000b>ôïï\x001e~º¾®E,¸6m\x0006QÓÌu»f¡±³+øÌ\x0014©h^ÇÅo?¾9YÎºýgIª!ïâ\x001f*6øKñÕ\/ÓÙù÷U£_ÿøÿ¬½v7\x001f¯îß6Q*ºï*FAL°kp?E\x0019ì\x001e\x0006¡ Ñ\x0015?~f¡öþúñ»5\x000cò«SUöÑàYYþÐÌÂ6MÔ¯JLãìÌd$-Æû»\x001bÑ\x00177¯O\x0016Ë§º\x000fù¦5©ìe4µ2J6]^ÿ3k­\x0010uµF\x0008}¢\x0005«(½¢ß¥f6¦ýYkþëùÝ3\x001bAB\x001fI\x001býît©ØêÏMÕnÏ>QroÏ¾\x000fÙß³o°\x001a{û¦\x0019F=cýww·§Jx4ã\x0011\x001eµXÌö¨\x0011)ÏÞòPhI9·GÍÊ õï®¾'~nî\x000b»{\x001cÌ¹ø4eD©½<J¡¬±4\x001a8d\x0003âQåÜü\x000f+ëB\x0001ùû«û«ï;×ãëëû\x0013ÉÉç¦¡ªß¥ÝB¢\x0001£Û8ë¦´)ïì®\x000c©u\x0012_*·Hd\x0011¥\x0013ÜúèSþÞ\x0019Û¤ÓôS8·0Ï©<ýú¾¹²§sd\x0017^Öx\x0013Ö'ÍZçYç\\x001a}\x0016\x0012JB¯¯Þ,m\x000f§8úêÓ¾9¸yuiïo¶	ªy)sjç%¨,\x0005uõöþúû^\x000frswûöTj;Ú\x0004\x0017\x0005ÜtK	­
!DQ9c¸ræÜ\x0002#}èÇ®·©Öáâß\x001f¯Oå©Yo¼ÔHT¼¶ß·fdïl©NôÜQç²\x0008¤sßÏé"Gí&IÛÈ5yÙ-ïÄl:²/\Ùfâ)R<ï{5_û¿nO­Þ\x0007u[Åc¦R>)#\x0019ÏÍu²¯Ý±?^?Ü<òÕÏ\x0015êÓMH«\x001fk3µìA5òBÎ­5í3çT¹Ã\x001foÞ|ÕÜÓÅ\x0017\x0019!ÞnñkÊÄjPºwg×éðY\x001f?¼v:ÜÜ^¯½ºñDRÊ¡D¥Ö$£)Ép5ãzÑÈ\x00079¿TôAº¥®4~ö¯_wÆÓ\x0004 k\x001cºhÖ\x0003ÕzÁFâ-1½§s3#×wî}û·¿¢ØÑÇÓåÕÈ]3¨»cXé\x000exÆåxL9&6*ÏLNv.§Y\x00019\x000b2W
´Õ°ÆeðË"¥èâå¹Ù\x001côÍÞ³núýÕýÛïO¤\u\x0010¨u\x001c\x0003X\x0002µÍ*ò
Iì\x001aöì´wpê\x0010Ýÿø\x000fÖJ¿¾{ü8à¥ûÔp­\x00079?»õó¹jDõulªþÜ¸Eä#·¨=r§ìãÏ\x0019K²Ús¿:lÔ÷À%ék¢h
Ï-Bâì\x000b¹¹{$\x0001ýi4å\x0013/[¬+«öBbðHÚ5´ç\x0017­u)áeûâæÛ^BûøöTÜ"¥TÈÓ\x0012ßË^ù\x0018ºi´h$_5·ÚY\x0008	\x00067·?@jè\x000551;HÑ¦\x0010¶ô££\x0012£íáÏ(ûÎÎiKu$¡\x0013VÔÀïâæÔZG\x0010» Üü#þç%\x001fY	ñySAW·\x0017Ln~2jR\x0002<6csk\x0015³\x001c| \x0016rvÏY\x0015&ö®ïï;\x001føo¿y}u²~´Ð\x001cCÁ%H#	Ë*$7VkOóÏ¯lÖU{ÐRd|÷p÷x¢êâR\x0014ì\x0016¢m¶ä¥Ý\x0013k6ã1rC!õ\x0012¿ikÔ}[÷¾#FÊ(\x0008E¬?Ã7_N¡Üdô»ë»Çw';F&ñ\x0014ÁÝ0j®GÝ£#^DG£áì,Ç\x001aGBº¿¦öé\x001a¯Û5ö6´j³²\x0015¾l&?iTÓ@L\õþîñtw.\x0014g¤¡hôÄªl\x0011Ó\x0001½±çØ]äd­ß.(¦ôþp:Ä§9®ê(ÿeézôîüJÌ°îïNy*\x0004¢Ïe{äÈÜÞC·6ûók*öfd
|~õæ«Uk¥\x001c¡jÔ\x001b·7c\x0019Ë¬\x0006«b²æüÙ¼\x0019\x0019\x0002MD'{âl®\x0018?r[\x0013Í&Irº\âù©noüHB7ì¼Ýã0P5\x0016Ø\x0001Tà¶\x001aKÉÛË¸Û\x0001¨ÎOJ#cé\x000f7<cîDQ6ç«TÚÞ¥­v$E#\x000eR¡Y(áüD42¾øñ\x001f'#Ê´\x0019i\x000e2GÝ\x0016	µöGÂù%$½\x0019YIjvä÷W§j m\x0016£µÑm\x0005Èèäó\x00181Í\x00168;¾\x0003oò@L¾oJûDê¨=ýxÕLö½K\x0011\x0015H
Gý¹ù·Þ\x001eÃ$DuD¥$§òÜÄ<æ\x0013õ%ï!m'cþÖÆóµyY ñg\x0012Ñ\x0019ù]ûóm|ªþí4ÒÍÅ©]¹õ@\x001cúüÅ/ñ4åôì%Ì¤vÓ>þpw²\x000cR,0~ªVSÝ\x001aûÏÄ+º\x0007Kü:}æç\x0013ÐþË±òøæñöæÍÍUbëÕ¿-Eñ_\x0016YüW)
t	¸\x001c«ÍUNÎ
¦\x0002\x0012É<-ûÃÝÇöÏnèßr~¯\;¬äub:\x0002¾m	âÕ×ùoÖ~³ÿöSËùÁ{âtÚb\x001c4|f/j4øâg;\x0002?5¾e¹\x001fñ-8ae\x0015\x0018o1¿ø_ò¤\x0014ÔTðÊ~ûñáæ
¤
NY¥ªRv\x001bÍi§R\x0018ãí\x000fø\x0017á'w¢8\x001a~ª6¢K7ÿ'@\x00030çØîyØzß»ï^Ë0µ¤àûüîê°®\x001eNFõP¹\x000b
­7>^hiF¡ý\x0019ÝÔÚóÐx~òöuñáík>ø\x0019\x0001f\x0006¢ô \x0002¯èæÀN\x0000\x001b17®a7LÌÕ$*_(Ù²ÍÀ´<Nu\x000e\x001e\x0005xØ'»upx*K	Á\x000bMeJó§}å®\x0004A\x0000Û6·È±\x000e6¬¼	)óPº9ø¾r:9\x0012<\x00079\x0011ûxê©H+/ó\x0017±r=/ÀÛ¥\x0013Ó¤xô|Bp&UçàUÇ¼\x000f°%ð Gõ5ð\x0004üÕ4:\x0007nû)ºõ\x0002\x001d®çÐÓÀ.\x0012·}àö\x001c:HhYÔOb\x0001t¼æ&\x001e4Ïwåñî½¬ú¤8}3;Þ¬ü<Ð¯þÅ\ÜÖåéìEÿb¤1a/öÆÌôÚ.3õÆL~ÈB\x0018¼1\x0002Û=\x0017ÛÏ±ýs±Ã\x001c;<\x0017[«\x001b\x001dæØé¹Øy]æØå¹Øu]­µÍWþ\x001fìë]Ûìdú'W8U]VïA.¥\x0018£SÍÏòúISbù'\x0014N\x0017R8\\x0004&¸ÊåvTñÞfèj¡BèR\x0010Ø^`\x0017Y³@Ø\x000e^D$.$ì8¸¸\x0002[Ø	Õ²¼bû Í'OÃ \x0010»iåÁÅ\x0015ØââB\x001a*RøÀ££\x000eFàuë\x000b °«X·ìùÞ@jôEÛ¹´­vU¡,\x0011´?*äÝ\x001a¸'kÕÎÅm¥AqÙN\x0019V-ÜÖ±ºcKcÕú}>)a[éû±jÕV\x001a\x0002\x000fsð À½\x0017fvô.É!à T|ª#Kx\x0007\x00170O\x001e®\x0002Ü+ÿ )lß§\x001cO±3¾L»9Ù°ÂÎê\x0010zÞNw0'7t'ÌÉhDw\x0005æJ7ÝìÏ6¹\x0016¶3ütíÎïkNö¸³v\x0004¡»¥J;j>ßR'¶t¢{ÔÛ¤²\x000e>ÂîbÅÑ\x0000Z)÷ÀõFB21­\x001dæ»\x001aÄ®æÅÜÊ¸`\nÓ#±"ºï*ÑL×N6ôew3êÌD$ø4ÙVÏèÓµG¡rs\x0016b1\x0019\x0015\x00001Ï\x0000´³ý\x001eM\x0017ÄÂKJp`¬Ã-Í8ö¯ýïÀèqºpú´¢Wrè\x0012ºx« \x0016ÿò·¯E$ó¤
#Ë\x0018bÑ\x000caöÎZâç\x0017oh4îg¤üÔ8¦Ú.-04¦?äI!\x001c#\¾¾¿úJ1ÙÉ<é|,^®vó1ëµ\x0016élÏÁµÙå¥L¾É\x000fyR\x0008\x0003\x001fS`»çbk\x0003G`ûçbk\x001fS`çb\x001fBZ;v|.¶6U\x0005vz.¶ö1\x0005v~.¶ö1\x0005vy.¶6±\x0005v}\x001e¶Ö4ßùökÿnìc¶L­p§¢ÝÎ¥@%S.q\x001b\x0001@ÙÝîö¦Ùi?_&ó'NbM+C±Ë
ñíwMÃ_âh\x000c´ò]§lÙ¥Ðì\x001a;½îà{ìÕ\x0005
¦o/¼+&ÁéÛý\x0013\x0006÷\C
`\x0003·V"À\x001dÚÊ
¼Bn&6ôÎÁ³ÚÐÃîYÍvøÉÓÁÞÏ\x001c=
t¢mßIÉÛÏ\x0002{³\x0019âû] ô&9^û!X¿£'^\x000c »$¡\x0003°òÒÍ£¡¼Cg¹ð$Ç\x0014ÙfóÃqiÞ+¢;\x0006/sð"ÁÅ¢}ÄKC ðf\x001fHâüGqÌÂmÿ©ù^ð$¶ýäP½Âó§\x0015¾dYî³1p\x0016hä~VÚ\x0014Ï¤Ô\x0006÷¤oR\x001bcÕû\x0010S\x0000øf\x000f2|ÃG\x0001_ð~ÚÑ3\x0002;\x001a¯°ma§p*\x0019þ´b\x0007A
¾ZHOýåçðYÀGjK/\x0012;©±\x0000mO\x000f¦ëýûV¡]Ýóã?®NÕf­ÊÆîåù4Øîä<&ûßéD.D\x0016\x001a®³\x001fò\x000c\x000eÛðí7ùîNxrËL¿ßÜ½y¸~¼¿ø×»×\x001f¾ºøÏÿqsýúúý­&ýÒÖ\x0010Näé¹êdXÅ:³Î\x001dï\x0013þâ\x001ebËÎÿ\x0013\x0012~ò©·<ÌZoÓAwwqBèHéDfº2Íêp"tóíë0\x0011ºïP¢èO¶I\x0006"Ú5gîè¶¦ÄaÎéÒmÜó\x0001\x001dÒÏ>Øè3þSpgvðBuzYÈÅ(ðÕÒë±ÈãúáùÛ~ÿr}wª1\x0018\x000cµ{Óñ6^ÆM2!tþe<]V:Å:þ!O
aàþ
l÷<ìC­Ö_ßÙoZ­?½¹9U-wpPòîzº\x001fÐ¶~I\x0005(Fóit\x001fþ¢KK\x0005&?äI!Jµvl÷\l\x001dâ\x0010Øþ¹Ø:Ä!°Ãs±µf\x0013Øñ¹Ø:Ä!°Ós±uC`ççbë\x0010À.ÏÃÖºà?^÷=\x0007\x001aVvðïïo®OFN\x0013\x001cä\x0012\Ø'Ç\x0015Êzî}\x001d¥\x0004¶N^H\x00174{~`h]Ð¥¥\x0003Ïã\x001fò¤\x0010\x0006º@`»çbk] °ýs±µ.\x0010Øá¹ØZ\x0017\x0008ìø\l­\x000b\x0004vz.¶Ö\x0005\x0002;?\x000fûp_0îæ\x0003¼Ý¹{<U1¥ãpB_\x000cÛÜëD\x000bÞSBb/ææQ\x0016öx_\x000f{ÌÒR!íÉïxR\x0006£=Þ±ós±µ¾\x0017ØåyØúüä\x001fÞØ¦î÷w7÷W'cÍ"n\x001aH¦&»³f\x0015/÷,/Ußþ|SæOdäw)¥OÞ³È6Òì¸"kZ]ÂI|És¥¯VÌ\x0002{WÌÕZÙm¢g!mØÑ\x0004(Í«<Êû7ñnßèÿ|w{Ý$öpóñêöêýõÂ({º\x0004\x0001\x001a8-Ç¯¢bÐzsyN\x0012§OÓ\x001bè\x0010\x000b\x000fý:k¨_WP+zY¤ïU#ð37ïºÇ\x0017çØî¹Ø\x000cÀ\x000e¾g\x0000(j%Æ<Ç´Wß7¯F9t<Oox{-ûî?¿¾øÝÕi?}©\x0005j;LY)RÚÒlÄ!\x0017æ;ëàbÒ\x0018\x001fò\x000c\x000e`Þþõoo?â&ÜßÝþp¢~õf\x0005'¨(³.çõý÷.Ë=¸TRù\x0019çÒHuwy©(ïøw<)Á5\x0016ÐîYÐz¯ª{÷p%âø§n¶\x000f\x0015HÒ­w\x001bAJ¥á1{X,4\x0011þÜo[\x0017ºm\x001fò¤\x00109ú\x0007óµ½Æö	IXjÐ\x000bD\x0007iÕØ%fY Ì-/f&ýsOfz2'¿ãI\x0019\x000cîÀvÏÅÖ\x0016ÀöÏÃÖ§'<|óñQ]¹ºàQ¢§9?1\x0014')!sôyã;äiëò-e4^®¦oéÑç§K\x000bÏO"³ÈíühÑXèæÈ¶\x0018YÓ¨äp~\x0004¶{.¶>?\x0002Û?\x0017û`Îíà¢T>\x0019#KåC,XâëKÒêfy\x001c\x000b\x001d¯>|ý`E\x001cá\x000fWßªÜ4'\x0005dÙ¦ÿÐ¬ÿ´O'kúg\x001ct"+¢Ë
\x001fÙ\x000fyR\x0008£)°Ýó°õ\x000eø²|||£ÔÏû÷W·ïN¤lØ\x0015êâéi.uR6Ûè2{YqzÂ&?äI!\x001cöâÍWöã\x0007YÞ½\x0014ûõA\4jêD¶\x001dÕ[É\x0018b.~µíJ5I¤3ÓPÕ~¸Cö¿Ë²Ü{öø;\x0014Àa;®o¿ùú+ADøÅõ÷÷'+¶7Ì£³_NWbý¦\x0013õIí.Ü°vÖÚ¯\x000bK;³ã\x001fò¤\x0010\x0006ÚO`»ça\x001f\x001aÆÝßìÿñ\x000b 9)ÿ­fûvìÂJNá\x0013l¯ÓÖ§pÕ];T¦vijñ/yJ\x0008øëûûô|h¢ÎÕ\x0013Í\x001d\x000eTì
U-ílE%©©ë\x0019-Ö.ãÇ\x001e»¼TMÉäw<)Á}\x0013Øî¹ØÚ\x0010\x0016ØþyØú\x0004}ù}¸¢)ç´ÃÐ\9k¶	_L÷½ÄúY^®\åó£º°Ôñi\x0016%\x000f'Ù~HÁö·T\x000b\x00162ò£\x0004ö~|j1¬W_¹ÉÌJw¤d¾²¯£ã#°ýs±m®>íVöJf#-¥\x0012"\x000cí´Î
\x0012jÔà.&åb©Þó/×·'\x001b­**¹ø×í£U©\x0015E\x0014%§Ô;_æFÏ\x000cMú\x001eJ·Id´Ñ{á¶9ÊA\x001f)Y$+òèð8zh\x0006MÔ+rÈb\x0016v]ö>\x0018´#\x001cçT\x000e	\x001b¨è\x0010.V½á&å\x0007x\x0018\x0001¡u\x000eyÎ\x0002Z6«7hÕ©ÚÜA\x001cf\x001fõ|¯ÐY®:½WBpã6øCÇÃ\\x0004r!@|È¸è\x001dÓÎDÚ¿:®\x0012Ú
k?¤và¡¼¹d\x0019¡yÕöP1»`[#±=J·Umc²XMYYÖM/Í°«À.`ÅÒC\x0008ëÆ\á\x001e\x0010{\x0000­ÈÓøOH\x000bÏ@ñÆ\x0016\x0016¶=´§¯Ø²9}îB¤\x000e\x0007x¬Eà¦©hçÐBµ\x0000GA^Ul·	Î+6²,\x0018¦HÉµ\x0017\x0016\x000f|\x0000\x000bv\x0016l\x0000\x0015·Ñ:x"baÒÚüE®Ø½¼=*·À¦¨ô*²ÞÝ\x000e.sM°Øp\x0019*\x000c®LµÖ"vèçúPÅÞÁùÃñ­rá¾Zln¢¿\x000e\x000b!s
»\x0011+HÎè\x0019*%#ãE{|\x0006pË	4k'ÕÚ]³Z¢\x0011+oÿ\x0004\x001aÚ\x001fw \x00103GNÝäæð\x0015ÜÛ
ÝG9\x0003}\x0001ñº\x0003Ái{];ø¡¶\x0005\x0002<H\x0006\x0013KÀµ´®&¹¯KcÖlå^®¼\x0004hl2\x0018óåî$\x0000O>2ø¡-k\x0005ß²\x001a¸2§!	°¡²'Ácf+ËÏ¢\x0017G±Y/\x0012¼y\yÌØ6\x0015âÒ¯6\x0013ËÎÔÑ,bÙ9ÙÀe¦\x0017#²ë2í¦\x0017»\x0019¬l1¡¡\x0012 ¯Ì\x000c\x001c\x0015"\x0001fðC·×
¾÷zYïÝL	ZL\x0008\x001c¯§wa\x0001­<MÂ'ÍI²õíÄNã\x000f+xE±\x0014Ñ-#ÀKÎýÐ#kÌ\x0002.8c¨FÅ\x0018ÕI\x0006;[î%u³ëéäõ¬ÐJêjÉjå(óÒô-»@nbdò\x001d<ÉÞãªNK\x0003ÇR©v.\x001d79-üa\x0003¯~GV\ÍD+ ðT23Ý¸ÙÆ\x001fÖfÏöD\x000b7pàíöf\x0004çÂå0yùÃm÷\x0001P®\x0004T´m×¡ÞèÞ+9y"l
¶¶c÷W\x0003)\x0002x2|ÀãDÑò
<VÁÎãrÍð,·ãº\x0007,z£7A\x001fÛS\x0017hÑÚ~³|ñ\x001dÕÁÁº#¿\x0010Wh]p½A\x001dºHÒ¯\x00114va\x0013û;Ïä¼=X²ºÊ@$É¤àoNhpþ°õ¾§
+7ª<	®%\x0006÷%vð±
Î\x001f6ð=qÓÔÏ\x0006µ	E\x0000\x0018yb\x0003ñ
¹\x0016¡d]¢\x0017T^øì=\x001cðÐ}KWgW§«³\x001aÞ+8\x001dIÙ±_\x0005pr»\x0019|&ð*\x0004Þ.\x0007¬<ª\x0017\x000b$ï
Ü³XêLÉV`\x0003\x0008\x0000\x001e0ÎDw\x0015®¦_8ëì\x001cV \x0003° \x0010\x0015¸Ï\x0016ÁÙ[£Ét\x0013ð]É6pqT<v¥\x0013\x0017GdÛe2q"øÃL\x0002(ö¹ö\x001fT¸>>³%AÏß\x0010?\x0000ø®\x000b\x0013QG(p¸ø>q?©7\x0013»Ð\x000b\x0006é¶_üd­:*5àÊ#ËÞL\x000e9ØÀ}\x0002p£\x0014mECÂGæ\x0019ð3¿Þ\x000b¿¾]Çý¡Q(5ãù6l)û#WÇ
,:R\x0001\x001a\x0018ÔÓÓN\x0014¬Úqã±·\x0007Â\x0015{g)ìª/	l§Ö]`¼)Më\x000b\x0018(üa\x0003§°Éþ¬E\x000b\x0014Ì4z\x0010uxÛ\x001e>3·Ê\x000b·ª=\x0016;rÈ\x0011úf"âÙ^Ð<±\x0008½°\x0008\x001dóÍíò\x000eÉ#]É\x0006®¼s\x000bøD\x0013zAóçr\x0001eE\x0004\x000cr3}sÁv¥4Ü[å&=ØÁ3 ÄÐõÊ1\x0003¾B\x000bæV[PÁ¶v`ñÉ´]É\x0012kÍ\x0004\<l4'G(\x0014v&2ûàñX\´´k-1ñ_}{}K$\x00084ýºýß·'k4±&`>Ù=Õ\x000eNmäÍ~±JV*èÏÿD¹rÛÕ.î|ÍjËÜJ±÷¥
e¬¦ó\x0016êäÊ\x0006,ºÿ²¿\x0014\x0015®È²\x0016\x0002Î
¸³\x0002ÍEë_3s½XrÓó¢M©!ó\x001c=³aÒÒÃÁ_Eã\x001fQ÷1 ÍðOÐ@§\x0019þ\ÊÆ¿
9³\s¾,\x0015ÖlÔÃ¨MwC.\x00029Q¸
¹\\x0016ÜÀâ\x0010yÄô»\x0001×\x001d<A«hC²J\x0016¥3RM­8rMéz¶\x001a@Ì±bÒÍÕ\x001eAC×Ï"½ä=&ä¬ÒyÆÊ"7dq6R\x001c¿q±.\x0004tRÐ#³Ãa\x0013ÈC ·wYí ±\xìÂ!×³"Ðä.t|3´h(f¢x4ÇgçÎ\x0016ô\x001e7h«ö\x0005åQ\x0010¹²8f\x0007ÏÊg÷Yê,h\x000bW%ZµfÇÏáíY7{³C0ãÆ æD¨.aï£\x001di't,\x001a\x00198]BÈ\x0015¡»ëphúX¡\x001dî¡<\x001e\x001bP.\x001a¡{bÃÍn\x0013·%Jëu^µÚÄÐYgÐ\x00016Ñd±ê\x0004Ü\x0001´jÕ=H8»NÜDð^ùäÁ¤¡\x0010¬ÎÙó6În¢\x00137±yÂAè¡.¶AWµjßÃ\x001c3hq\x0015P¤¬\x0015¥P\x0008~xBfWÑ\x0015ØF¹èrÊS»\x0018B÷gÈ\x0015Dí*^\x0018%jµh\x000eÜ\x001f-ï\x0005Z° \x0008æ\x0013\x001d§w1pÃÏ.£Ñ9ÕT?+Ë.\x0008Z©S¶^g÷ÅËûb.ÒÔ i_¦f[iv]|éö\x000b
ÞD«ö½ìÙmñâ¶·%ÈÜ\x000b­Y)½ÎMïg·Åï·\x00081Ã&Ô\x000e\x000eðõÕp©Òå1»-^ÜvóÇUÃéða¸êÙmñûm!Zú 8Ø¹,°jô[!wVÙ\x000eâL\x0004ú4\x001a\x001c`@¹c\5ç·ÃìLýL»\x001aEÅ~jìük\x0016\x0001ÎÐ£yXtBnê
-é.ª¬RQ¿].¨EÓK\x001ef\x0007$$D§:\x001eQ\x001e\x001dà£û»@G!j\x001fA}ÐK\x0006FS\x0006ud+á\x0018ÊX v2Æ5a¸j:/rBä\x0018`\¤e©Y,È\x0016LB9G¾-G}Á\x0015tuÄy V\x000co¯Êì\x001cã>U,ÐU\x0008Ã\x0004¦\¼sÓx¸êlÂ¸:¦c[ánåR\x0001»¨¡`>9t12WV\x000cjX\x0016la®Sê]ëÕàóâr?K7×gf¤\x0015f$§õZÕ±¦ú$Äf
r¤\x0007\±%9`¶\x0012Kq@&¾àCPmÁ6Ñ!V¼\x0014ì\x0017½ª;ã½ò\x0006ÊBk8y\x001a­x\x001aE.®õC;°SfÓB.0{¿¬x¿r2R\x0010	\x0015èTïÂæti>+4\x001fQ¬CÂÌ·pH,Ò\x0019\x0012Å%»³\x0014
*Ç\x001bY°-19øâq\x0003\x0016\x0016\x0006*£4\x000cÎ9·zP\x0019³\x0000\x000bí}*Kóå.º
e_
»óR\x001e³\x001f\x000bv6-ÖíÌ\x0001\x001b4\x0014UI3ölÝY®ÛÂºÀ¥f\x0005ìÇµj\x000bp\x0011v	¶Ðe\x0000Æ(µ\x001c\x000b²ÇÍ\x0002\ÅmBiTÜEñ±Ë¾Ü1aÓ±\x0011¦\x0002
q\x0017½ÞÅ¤(:9ÈïÉ\x0005Ú
h\x0003SHv«\x001b¡Ùç?ÜY±Å5O¹\x0002vôx]\x000bxøBÏÍn\x00137&%\x000fØ©(\x0018Ý\x00116'2ñÂX \x0015qFr\x000cøÎ4Ý\x0011äöÝG/î£jÃÍQÍúl;ç\x0010ºO;Ì§>lÁë
3&\x001bDb^6×ï
êVì(°<Ý\õ.O7ã\x0001vè·cAÉ]\x0004v\x0011a9{|
\x00007ÇE6GÂìæ\x0004qs&\x0001ý'\x0001=Yw\x0010¦NÌ`cç\x0012ñY7µjlf] ®\x000e7Å.ÀTÎ\x0008çÏ@«¶uløÙã\x0018Äã\x0018\x0005û\x0014\x001bÐ"
¼3®öõI@>lÀ^\x0016\7STÍísMÕ\x000f\x001f1ãoØbÑ\x000eä\´ÇÑ\x000eªbåìÜ7\x0013JuûH!?Bf>®03²0²£±pàL-\x0019®_\x0007jMÄ\x0011å±Ã1f\x001cÃGZ\x001b\x0011»(\x0007L\x000b¶°°£) ê\x001cð5 ý\x000fØGVÄYD<x´¸î\ÔuÁÜï%×qf¼Ga¼G#q«:zÈo×§aÇÝ\x001e½\x0015'£\x0004ÔÔ}\x001c\x0000üèÆÙ5â\x001a\x0006H"ÇRñxªìö¯ð\x0016Î\x001eÆ\x0018%6èºNh+x:ÑqövEñv\x0005d!/5ÃÁ+5Át¾Ì\x0001­8{_¢x_Bw± $\x0012ÑzòM¾83ù¢0ùBÅK
»(¨°¹3I>ìØ^^\x0018\x001eÌ%\x001dÞÌæd)½(^\x0008\x0015\x0017]Õ¢=6ß5Â©¦(TSÀ\x0016çÂº}H]{ËÆlÝÂ\x000c\x000e\x0018\x001e"l©AÚqD»Ì\x0017Ö|i¦ùÐ|<L#	ì
ïb»F\x001eïz	}~ü$DÊ
"¤¼Wò¶zÝ\x001cK3\x001b;	\x001b\x001b«\x001b6G4léÜ¦\\x0012cÏdb¥L¼4ú*\x000eû$l{îÑL3­V
¶Ât\x0018Z(¥b\x0019ïµEiïI"ß\x0013l\x0016ÀvmÀ©(yð¢gS\x0012S0\x0005Î¶\x0007à¢9µfÁÚ$µÁGZ½Ò~\x0005\x00132í_ç5Ï$\x0003êvJ\x0004¸\x001atBC¢\x001cm¢\x0008Yøz$¨s]2RQS\x0015cO_A`ÃÔàªBãmÝ	\x0014k³\x0001{¯äL&â\x0019óÐÒÓÖ­ó\x0010±:MÐ³w,wÌgTQ1ã[C4o\x0008Í¥
i\x0016\x0013I"&ÂÉ¢\x00158\x0019%k\x001fmÏ\x0003Ëcö%ñù\x000cC}©ë\x0001±\x0003Þsªleì@\x0014\x0005`Á\ÃöJ Óì­Iâ­ñ	ïc¶jÝ^\x0011ÏcÊòì=Èâ=ð\x0011ÒZ`\x0017-ÞõÐ¤Íéµ«i~íÕ\x0015äª Õ\x001d*ëÃé×)¸\x0003ðc.\x0013s»ì9E\x001e®ï§Ù»W\x000fÌÆ¿ªÖ"ÐSóãÄP\x0019Ä!±O^ß|<½¢²,"sÊºÀ\x0000c·ÉôI7fú\x0017Ú7ø\x000b¼°ý/Ð¨Ä \x0005ä\x001dÆ´­aGõ	\x0011\x0019\x0014QñÝõÝ~Ui\x001bçT:\x0015®\x000bs!¹BjwßÉóÚMJ¨Sp=z>ÿ\x000bÖ«¿ð)UQ>L\x0010'´Y÷L¹!ò©ø"94õCî5\x0002O"§Þ¼PÅ_(Ê¸È\x001c\x000fï{B@\x000e\x0005\x0014Û=\x0008Ò\x0007W!«¶ehuy\x001aW¸\x0008Uí@\x0011£4¸\x000e+Q%o¥·k?±ÇVýO+ªª!\x000bjJdaPõQk"&£óO¬ß«õ7Ý#3þ\x0014¤ÅÑR\x0018_i&â+£'Jäd´ë÷W\x0017_Ü}¼¾¿:Ñ\x0004¢ Èñå²R7÷¦Ê\x0011hªZÎëhB4©Ñ6}\x0015Ãµ\x0011;%)2È½\x001dø\x0018gíØVJç4[\x00122r¸ @\x0015Mïðn) \x0014;ý¯Woþöxýñâ7w·oïN8`\x0006~g­ÖïÛ~ÝB5/¸Ñ¡ÏäüéêoËä\x0017²ú;\x0006ù@\x0013ÕgTUXÀÈÐù)\x0011¼\x0005xàñÄzñæÄoNtª ©~\x000cBm\x001dÚcú]û> 	J\x0013îÀ¤¤>z\x0006-²9¹B\x0019§×"2B÷é¡\x0003ÃÙ"	\x0015R@¨%\x001e\x0013û\x00194¦ÔNÇ0pd\x0019[æÈ±|áðºØ\x0004D4T¹ÅIÐ\x0019¶\7
Ý
~
ì)ë\x0016éQjî\x0007\x0001 ]%6\x0004BÑ6XKÿÁßG³
\x0017hT8¸O]jÎÎp¡\x000c\x001cxÔ¦iðõ¸äÊeñn\x0010èèØ²°5\x001f\x001bMR%¢\x0011\x0013ð¦ûö£üjÇGDv\x001fØ¬äp°KSÚ\x000c<»2NVK\x0015,*ñU½æ\x001fñépÉì\x000c;Kl,\x0010Â.oÂ.ªF3 >¤\x0005[8ÉUVðD)æhVMÜ;>»-NÜ\x0016\x0003µtªÈ+Z,4Ëü ?ÉØ^ä'¹[LÔ»Á¹\x0016ýî¶h®\x0010\x001dÄ\x001c;°9VèÝkªZåõÛViìÁØ\x001d[\x0004Pj,PbcZwV¾Gåøñ(\x0019Ü±¥°SÆÂÇ:\x0016ÉZT2²I×\x0011Ë\d½¯§Ç\x0012È ¯c¨àu`\x00061\x000ei%æ}¼øc3\x0001È<ýóýc{úOÄåfrÙÔ\x0008Â¬´¡Þ[½\¥¡-/g²xCl\x0007å\x0018ïkâ{%+ ¬\x0011\x0015P>c²#\x0008í\x0014\x000bKãliÇ1ÉÈØ\x0016Ä!T³¦éÉFÛÖã\x001dëØuoì¥h$M¡9â°ìv\x000f³Ïçûk\x0007\x000f\x0007Ûýá ²4É\x0016×[C\x0001\T\x00170§DèEaÇ£cïAòvg¬¬\x001fwÁ'hì¥\x0002=ìHv®\x000f\x0014>>\x001e\x000cî$w^M²HÎ9\x001d²¦zÐLt£fÐt¼`×\x0017¿þêêÛ«w·§â]N9z$úJqñûÚ:¡J±I¥[w/t·-#w`\x0010e­'\x0002GLgóúÂ½Ç:=Ã\x0015e\x0014ÞeB²=¼[È7\x0016ÖU)¹¦¹ÀHM=NTG¥;\x0004]*,kÆví\x0016R¯1¸\x0015eo\x001d¤Ó}"ü£\x0005{T
G1ý(VÏdJ»\x0019Rl×+\x0014*jg\x0015ØcMèÕ\x001f6OÄÂ\x001fÖSI¬AÚÐ$x 3\x0015ÅKp·Ô\x0002·LÔ´Ûî¹XY\x001cI4»°ðT\W:ÐY/\x000c?Dí:EyTB3\x001aÁð£«\x0008Ì[í?èà£\x0014\x0006\x0012Mïê÷#º£â\x0004æ\x000eÚ\x0013rrÒ?ð5cqBjö\x000ec¥´Ô1²¬Ì\x001d´gY3±ì\x001aÕrÐ¬x ©Éj\x0018eC\x0019|÷\x0010\x001a8ÐËqÆ\x001cVnç°rÇÙî1¬Éjÿtuu\x001a-\²jÿtÙÖ-Pl"T\x0007.Ì/¥K\x001dX8qDÕÑe\x001bD|,\x0005e2G$
MÝÀ!\x001b\x0012\x0001\x0017>nkÒ{U´Õ.
hf*p {D\x0012Y	\x000bl\x0007\x0015ï^·äØq½ÒÛ9E-ËÃÀ\x000c\x0016V\x0004.¬Ýë±ek\x0001\x0016-[ÈÐÚÔQ6*à³p*8Q"évá\x001a{\x000bÅªÉËB¦)°XÚ»Þ>¢!ä(éÉAò0øÁÝ\x0013àé\x0000µÏ\x001dÔÉ-à^QJ	\x0001æ²÷O6?HpYÏf²²^\x0002\x000e¹tÀ©ù\x00163pY\x001da $NsZ48®|éÌ\x0019Ô¸tpYãâ
¦¾
ºÉdwa5Jæ\x001a\x0006;¨\x0019YÀÅ¥wÕaqÓF\x001d¶­rß\x001d\x001a,Ð²ÔÀ@DXPI\x0015#üs~\x0014Ë\x000fâÑØ\x000cø\x0017¿zÿþúT\x0013dNÛ´ã±OvFmÌRôöB\x000fG.¬Íñ\x0005\x000f=Ñ¸»¾B[ÃP\ jxÐíÉïéö	´ \x000e\x0006T\x00199jm\x000b8\x0011ÚLÚù\x0003¶óS5\x0004h`Õtª\x000eÀvÏ«>\x0006A\x001dZ\x0004
\x0007~\x0003g2flV«vÝA\x000bBò YÀ\x0016¤Ðkn.ÎHË??\x0005lÄ¢àiµÄë$\x0010í\x000eÂSª`\x0002,ç
ýn&{ÜE_\x0010{'F±IFö2§7¾@O^>®°a\x000bêþ\x0014`\x0017
ÕK\x0004µìf²p\x0019ÌÀÑèØY`' à®U\x0005 B¸nÏÏ»Û¡\x0005!yÊ0&Ô\H YÊDË,\x0015aà\x00070tp\x0002zÉ:¬Ð\x0011Ù`\x0007jÐi¬½}ÐÃÞ±ÃM\x00015á\x001dÕ\x0010ð`Ó\x0004ì¸\x000bf+èØ"Ü]\x0000l\³MºPK"âî#Ý±EÆ:#Ýyµ \x0010,Ó£EÅIsFÀæ\x000cKª\x000c\x0017\x001bcÇFR¨&L.\x001aØù\x001d;
ÝvêÕû§z|\x0010vÊEªü\x0019Ìlî¬M²èáñâ7wo\x001e®\x001fï/þ|÷xõñãFûÖjQ\x00197S{	jr_è\x0000{Âó\x0008Ñj¢ûõO\x0010¢© íÐuÖ¯U\x0001\x0003Ø\x0015°»Õ¬zvàgÀû4vÞ%\x0007Õ¯\x0011ÅV\x0011íêAóµ\x0006jhÔw\x0012oF»Â\x001e\x001dj±Ô\x0019¤\x0006e»\x001d95[Y\x001f@Â\x0005Öì0¸³`\x0006,ÞÏå<zKu{¸ä Q'Tk\x0015*\x000fhÉæRdÊ\x001a2¬×\x0004\x0005ËÃ\x001af°Y<ø)YVØvØ½TçÎªª >7`ÐNÐË\d\x0011f[°e~\x001dYeØSàwy@ßÓ«\x0010r£lyh¯1æªS/{\x001dÅD+Äb¡\x000cØdmþ$¬8H¶»q³ûg-,ÚÊ0q¸L\x0001VAKú8;\x00167°$ÁuHÈ> Q·©ó6Ìå
ì¬\\x001b4²ZÒ¢¨Cg)A+X¢,³\x0016¹üiTXõF\x000fú¥U{¡7l¾DI«"¯0c´ëÀâ\x000e¾i\x0002\x0018îW.t?|v
­¸dUIi\x0014&×¬¤Ñ)\x001bf÷Ð\x0016X´\x0011q7[ùZUC¥oæ\x001cÂì\x001eÚ
âà5cÙ\x0001²3JÐlBBÂ\x000c-LAªb\x000bü¼h%\x000fÖ£#N»\x000emaÕ\x0016qÍ\x001a¸3\x0001Ëk¾Sóø"ì¡·x<âÑ®CË{èáYq\x001eë\x0016­JKÛ>q`\x0006\x001d`Õ^BGY`K«ÆPaê¾Â¨Ã©j\x00178;Ycnì@Ú¢ Ýv®Cg¯a[u\x0004Åd³^5Ëzv_¼/FPRQ\x0016L2@Ò	)JÖì)xç:´¼0öÒ[îä<¤U'µj&&\x001c5ê2´\x0017/tSkB[ÞE\x000c\x0008$ÇiD®Óqåm1xÇq\x001a\x0000\x0015©%spÄ­Ó¡Å¡N}<÷\x0006]%#&A\x0007\x0005Í½£#Þ¹\x000e\x001dÀ\x000cö÷JÐ\x000eKåR23â¹\x000e½\x001fjj\x0004!Cç
]j\¥Ùëâ\x0013X\x0008rÍú":¯"$½gv¤}\x0007Ñ' ùV=ãÜ\x001bnf'ÚïLÍsÆH\x0016Xçj²h¢×\x000e=bchá±*=ßf£«ÙxN
ôã#\x001dfz:8TK"\x0012eíOêR%ÎÓ0;ÑAè yi­Oê\x00050ÊäM¬ÂìD\x0000ªC¾\x0000ÁIÊ[Vx
\x000b4G½\x001dZÖµ·ßCr\x0014ÜÃX©Áð8âÉëÀ	uùùË¢Ô\x001d¾µ¹ÂìDýDe\x000e¥ÁMÿË\x0012Êì0\x000cU»k8j\x0017eh\x00113í\x001aJd¼ßÙa,ºm9,2\x0003v\x0002ØÊV\x0016j\x0013]iDª#phÔÚ¡÷ÓÑt£ Z\x000eÁJ'ÎÓ|=µèÎ1ÛÃ¸ï¡¡t§8\x001c´ò~c\x00034±\x0018pül\x000b£PJ*Ô\x001c=·Ë¢\x001eÃÜÛÍg[(\x0002rÆ\x00039hÍ©\x0005)£oQ#\x0017w¥Ù&&±\x000eHòü\x0000\x001aóÚK¢ôo\x0014mb\x0012ØÜ	Q\x0019b\x001ebVfº\x0004=ÛÅ$vòRMSåV6M{Æ¸\x0005u¶ê¼w@·\x001b!
°<\x0008»ö¨\x000eWÝ#\x0013³EgÑk\x0012è¥ö\x001e\x0000m},A!s`)ÏÎ^.°hYí|\x0010iÑX\x000fF2\x0014õ=\x0011°
\x0008m½U~­Êê§ØSï³ð\x0018£Ba{\x0019´1«tUUW9S\x0006\x0013C:´\x0018ÒnÌ~ò\±%kÑ¢Éý=t³7Ü\x0005
|)\x000eûÌ\x0003\x0017\x0003vîÄÓ³K.fÇ5\x000cªè]Æ¹/´ß ¦>ê¤B¿cgÉ»\4¶I]Ü\x0019¶8 >ÈàxtEåfÈ:GìN×>ªEdì*±ÊÉ\x0019£\x001cbL\x0013O>lØ\x001es¥ðS´\x000f{sÁ¨ä®\x0003ü.ò¸ªnÑåè&Ì\x000b\x0018[&ð<¶\x0010¹ª\x000fI:ý½xF3lq\x001b=ÔÄÅµ\x0004dÇö\x0018R/¶\x0007¾g×ÑËëh¡¶Á[5åÖ(×¹¸n²Ï#/#oàuô6bÓX¯°\x0010ÓÏ.¼\x0017Þ\x0004Uî"Î"v%L;¶0Ì\¶*ïÔ\x0018nzå\x0000ÛO\x0013¦\x001d[\xWà\x000cz¯újQØÓ#£iÇ\x0016Ò\x001c×ÜÙ5)àXºï5y éÃ\x0006\x001c±ê-*6ñªæ>jÈ\x001aHØA\\x001c\x0017q#£âõo\x001ejÄÚ5Éºë6Xõæ°\x0003j×Ù\x000e³K\x0019Ä¥t\x0001\x0008´}Rüû4á\x0017±9Ì>ÊOwl'±¡ÎàÐFY±©aÇîÎdâL|Å=«Î®`ÌLï\x001ffÊ$\x0008eâ¼ug5\x000f£Z]8ì\x0014fñ¡ âCìèÕ¿O\x0018 ;öþ08qÑ°V½
_Q1@\x0007\x0016ZÊ9(\x0005ô0á¥Zu#û\x0018°0óÒðÒ³ ¢OÁR¥\x0006Í·fæ¦ïÄ\x000b¶\´;`ã²Ù®\x000c3o:\x0008o\x0013"\x001b.êSG¡êàe&êp\x001c$º\x0002W\x0001\x000c5.4nUc;ÄæÊî0{\x000e|\x000elDlÅ6\ª:ÕµO%\x0018Q/ul!kõüj\x000cL8(2ó¨ð¨\x0019[j\x000eØjÝ©¯{¶Â§¦R0ùUE=ß\x000eZ÷\x0012%íe¬-eR\x0015×u\x000eJÞyRAÓ±-ïäsP\x0003Ö*·­ØÆôÒID>ìÀ\x001e\x0005b\x000fØøDVz0§¼bïÄÂ|_\x00166<T\x0008ØÜ\x001ef\x000e{\x0010\x000e»3Ðî«R$¥àÅ¡DØ3['\x0008[ÇVuH\x0014Q­^w5Ü~\x001cF\x0004Ì\x001dÛ
l¯×;a¢ªa÷uÏä-ÊüÚ+òVÏo3o0NiØ\x001c\x0012ì2vØpá¦ú/\x0011Ó\x001c¤È\x0019{«¢\x000f\x001bvæibÑÃ½Ä
ëÍ
\x0004¡ÎÎwÝÏ·M\x0015±á¶ûª\x0004ÂJjæ\x0005áqwÄJx¯Î\x001fn\x000c»-F\x001b\x001b\x000bÊZµ¿\x0017\x0017Q\x001eûQã,\x001eE\x001eÝFµn5 8£°;ùë,Ý\x001dEºÛ"Ñ)aV°W½a»\x001e\x001aÜÉ(LK+ØuUTÉÇ­\x0001óK\x0016gÙî(²Ý¼h)ìúSæ×=Î²ÒQd¥mÄT\x0018\x0010\x001b\x0015U'\x001bðìÄ±
Àl\x001f,\EäB'iôÂÄÙ\x0016\x0004¬
àæ¤Ñf0*¤h{8{feGaeS¶G¦$\x0016ód\x000fÂW\x0015ï³kã,U\x001aEª2v°nE7PQ»È.û°A®c\x000ba{\x0008*\x0006Õ\x0000ÒÖÔ)=-1I2±¸Þ!W,zª±8b#íØâd#'z°ÊlPá¿fi÷eÏD"Lm+ÃðVûå1Ë¶fæa\x000e3õ\x0014zrà\x00116xìY\x0019ªs]\x001e³³-lmkå\x0001Q\x0004\x001d9G\x0005ÜÇÎ\x000cí(\x000cmn\x0017v§a+ÄÞÉ0ÛÄ(6Ñ\x0002§gpjQÎè|T\x0017¦4à\x001d[ì¢µpi2´sRyÍN\x001fgve\x0014v¥Å\x0018Zpö(ã§Ý©Ügvev¥àsPÙúe\x0011»ó¹Ïl¿(m?´+SooVJÛ)y\x0016\x0011µà²U$ «þN\x001aÃØ\x0013s8f¿ÆUuFG\x001fQ\x001bóìÒä*¬aÅPÉÛN^>\x0013´ò\x001bx\x001fW\x001a;û\x0007Û37Q,³KS,b+(lüvSÒõ-v±àÓëU\x001c*{§°;\x0011ÉhÒDÇ\x0016»(rLÁ«±/Ùkas$~ÈæÎÀU
\x001bÕªW­ÅÙUô }îØ3\x0008KØdà`\x0008Þ«cmõî9U\x0018g\x0001Ü(\x0002¸FÔGS	\x0003J\x001a	F©¡S¹O\x0004¬a°2ÂJE\x000cxeTÕV
l¤Yô6è­I¨²VÙ\x0006\x0019ßjg \x0005o\x0008Þ\x001a\x001c@Ðh\x0018§+COîL\x0012å×&YÜÆ¬Q\x000eÍÂ¦=shphLDËÏ«ûØ|^U~á:öLÚVÖ_ u\x0016Ôã*\x0012i\x0010÷ðß'ìö-\x000e\x0013
î¤×ëVÎR\x001d{&oáw4ÏépJ<`c\x0011ví#Ìù\x001d[È\x001b7°L P¢¨W,tRþ¸E\x0018ÞÕ}Q6å1´\x0012Iî¼ü3q\x000b\x0007Á\x0004¨\x000c lÜÊbÔ²{}Ç,§DNÏx	¬¬ì:Û½édfÁ'aÁ\x001b/\x000f_U¨x#kdzÜ!+?\x0003Ë2+AEE§±u!Mèÿ³\x0003\x0012e¦¬ÐQú)ELË®Å?³8eEV-\x001aÇXÐø\x0017<Õ³4CNþ-\x0016m­®,RØÊ7èÜCN~Æ\x0016f1	´æïK\x001eS¾­Õ43û4ûLÀZ+\x0015ML^Yð\x001b{ÿ-(	´\x00069Ô,uÜÙ%Ã^EÏ ©ÁFI\x0013&v§lÿ-Øþ×^Û
;©[n×Ñ\x000b5ÓÌ\x0016IX´Ò|5qüJy$£°;BÙ"©j+6Aõ¦xDðð±\x00015dk"à,ù\x001dXqê2\x001aL\x000fÖ>Ã'É\x0013\x0005É/µ\x001eKid\x0015\x0000HCàåP%jÁý*õSûd <³o²d¤Ì@+±Î©\x0012ØJ\x001aC\x000byfd+«xÅ.ÊH%êw\x0004fª¼<³@²\x0018ZV3FùJÂxH,ê\x001e^;8³@²àd©	¦z2£-b+åQxôfY	Y
%)ieîÅ¬|ÆÂïxÙ\x0008Ù	`á\x0019U<Â-¤Ñ]¹Ï'Ïl,xdª2÷jÔëFdXäY/\x000bª¡µ^®\x001a(\³rÏ«ås=ë\x0002È²\x000b Â` PU¶ &¥=ºOg\x0006H\x000eR"è\x0013TM=Ô}¬¹®Îd"+ßCÒØ¸îXÂfyÏì,xua@pñÚ\x0011\x0008Y,,ì
\x0005ýRõð\x0008DÅ\x0006Dv\x0012ÎÕ0ü0æ\x000531qèÈÉöVÍ!NQ5sYp²¬æµ(\x000f«Õ\x0005º\x000b\x001dóÙ	Y\x001ecº>bÕ\x0019aãx;ÓS\x0006yögù\x001b\x0014·UPMþd3Èeö4\x0016ñ4\x00169Ê]-kF:\vN3ðDØEÐÔ\x0013Ã´ÜG§Ý8
¤Ëì\x0011+â\x0011+8¹°áüµW
y¦]§euÃ\x0019\>mà'¦*ÖpYdA¨ç>1Q!qöË¹euþ\x0007\x0000ùS¹\x0010\x0019Ì\x0014aøb¶"ÚÆ5\x0019{ÓÅãaõÔý)[2¨\x001c¢$EÅm·¸ÇÓø/$\x0003Áxw)m ¦#Ø°	«f+×¹ÙÑ`þ\x0003\x000fÕmr¢Ú*X6«jkl§)¯Þ\x0015X½k"O²rL½ýÕy]9ÆDoÓíµ°½FwáªÀ·/R:Í&,¢ÛghO¦\x0011&\x0012=÷ö\x0012\x001b^ÏEÿZTÐFîÐÞ*hUX°bqF¡éØG*Ì4 %~¼øÓõýý:æ×w4iê\x0004ôf.Ô&M¼+ñ·eûYLû®Õ÷¦Ò¤âÂ\x0017óH7çWdÿg?äI!\x000c6\x001fòÃÆüåúöáî4ÛA3@¹º&
õw!¤,f\x0004Ñaân¿³âa\x001fÐ5©½tbÍ¡3²g 4\x0013\x0000\x001ffçöòd&Ò
l)\x000fêú;¶\x0017ö}Jf\x0007*ùfG`\x0013úhé	°¤ÎPxOµÈÈXØ<-$èíi\x0006Ô\x0005[ÎSÞG¦S½D5;ÕÊr\x001c8±2 \x0011í¨ÂÅ\x0011¼Ô¢Æ"îm¸\x000b£p\x0019'±\x0016h99\x0018F34ÐN¼ó.Øn0àÀ«QL¼úöÇr*¥&\x0018w¹lïïn_-S_ê\x001eqFø8Ï@oB\x0013\x0016?72)f¾¸ "UjÀ¨éÅ0©\x0000\x001dWFÿ-NOñFâFcB£3¸à¢ÐÜ­¿Ø\x001a\x0017\\x0019ö@_\x00195pÊ\x0011\x001dP{\x0010}\x0002-CÆ\x0001ï£¦TN\x0019Ç\x0013\x001b®\x001b;êÀ\x00059cEzT\x0019"¯%£Ó^rÙe\x001cW\x001aÑ\x0019'å\x0017\x0013\x000bä\x0018\x000b \x000f\x000fÝ¯ïïNDªJt`	5CÌ®µD(ÆÕ1\x0018X×ö
\x0006ÖÍ~ÈB\x0018&\x001cN©øâî±-æáD\x0003`!\x001aÁ§´0ô\x0011\x0011x¸´;aÎÝóÒ	jJEñ\x0010Þ\x000fU\x0012kç°Ê*Ú4f4Xp÷PTáR¿ã:T\x00139VLãÅÞ`9"Ñ±å\x0014\x0000µ(<è\x0001FT$ì¤&½ÉÝ¬1*QÍà*\x0001*
ÓÝ#9©o_:AÌh\x0012d\x001f²$°¡+$\x0015yÎ±`ù ëµû£A\x0004\x001d\x0014·ß\x00140µÈe«¦\x0017×Ic\x0007¼-kddÀÆ\x001e&@tÁÆ:,ãÜ/\x000eãDÿçû\x001fÿr÷áæáêý,\q`aöô»EÑéþ¾¸oû®l`©ý4©¦s=$ªJàgØä$·\x001a\x0017¬¨\x0006~Ì}¹ ûg#\x001f£Þ\x001dZ2\x0018E¨]´ô&C¦\x000f+ÂS	\x0013ê\x000cÔ)+ªòølUà«\x0002\x001e¤r\x0018×:U¢|<-O4\x0012Æ ÈØÞÈ\x0006F\x0010¥ZUÇ@,\x000e?H$.Ø¢\x000c»Ï}:\x0012¥Fz.äYæsY°E;|\x000f*æM\x0015¾G1j´&øxñÙõýíU»O§¢¨§\x0014°êÙºÿì uDÖqz¹¨!*ÄC\x0008çèÌV£N~IçPh\x001c¨ZEò¹\x000f{0 ãJúgl(UcÚI´¨$8>\x000c­Ð{ÉPgª	^ÍB¾*§¢N4\x0019\x0007¿¿¿ùöD\x0007Y\x0014Ño.²\x001cÑ	Î-c_ò%\x0019\x001e Á\x000fÇÁYYg\x0015ê4ê.ë\x0002®\x0014Â7lÅ\x0015aXgµêLEÓ¬²c{Ì-Ð²ê¶BÅ)*N±&¹t4E>kgB»o®\x001f\x001e®/þíîþíisÑ\x000flé£GVðâ¥¥]ö¬Æë'ìu\x0004Z!³ñ¤\x0008þ~äöÞÝó\x0007ÌazýÇßÝÿøÝìÉ\x0019¨.h&êºËÔ/,	pS°/9Ó<rûO\x0007ÔÐT@­¤VÊ
1c]ÛÜM 	®¨K-Øê£A\x0007\x001cÒÓÛ\x001a\x0007ã­\x0016d±â\x0002-ãIóUe¤#jÈÑ
MÍ\x0005Z<¸¥B\x0015z
j¨)9x Ò0^·"E\x0003¬\x001a%¢ú\x001a¬\x001b\x0013-¸â)§B\x0002\x0018ë[0qsÅ¼ye&&îÐB\x0013W\x000b\x0005ÑÉ\x0019dPÊÎ¬W$\x001dK\x000eWh1Õ\x0005\x001ct¬\x0018Ñï¶M5=:Y¶\x0008@Q\x0007\x0010HÄªé;T}\x0001Ø¥COmå]=´½&«¸
ÒÚ[2\x0007±­dëOW\x001fnnO¥·â9Û\Ñmz\x0013>ï~Z2¦ÿÏ\x001aû\x0017ã`øê °¬
¬G\x000f?½Æq\x0015·\x0011.TèÁäA`½ã\x001a\x001dØ\x001fU\x0013Ày\x0003«6ôñïðw\x0016áïh¡¼j6W¡8Ý\x0006Ç\x0011³A\x0008¼CË	KµÊ\x000bU¶\x00048b3\x0014Øà¹Æjpê;¶<õÄ©/<ûZ3>\x0012.BwÃæÂ\x0016;Hçtl Õ\x001fÆ'O2×µÌ°Å;ÁEãE`«á×Î\x0016ÜÉNÊng§ÏÓ\x0017ÜÊd¨î\x000cj}Ã\x0003\x00189I2\x0018\x0016»`\x000båÈ4\x0011\x0002ÛéA\AK©s§O°8ÝÞ\x0017\x0000\x0006²îä[1±\x000b®8\x001eÁ
:¢ÒUå7
»Ï ÉC2ù9`\x0016iØê\x0018µr!qiXí Î¶Ý/M¢v\x0006¤\x0015)Ym¢õ\x0003;ç\x001cS\x00157¯Z?ËaÁÉ]4uvóºK\x0014"
yá\x001d9¯Àçñí6\x0019r\x00154
¦GÕ¬®\x001d%Tð÷Ñ8\x0015Ú	h«¨ìc@kß	{\x0006U6\x001dW´»eÈ6hÅ\x001f\x0018£ÅtBíU¢Gs£C÷"â
¹F\x000cÓèÆæç±m×¡å®ñyò°± 'ØVJ¤J\x0002Á\x0017ò\x001dÛapÀw\x000e\x000f;0£;¶4£-\x000c.ËZÏ4\x001dDâ
·¸ÁäOÆvB§\x0017`b	ìÑI=*Òa¸f§ÜÒ|´îþpuÿps{ýpªÐ\x0015ÖK©>ns©Ê@;ÿ©óT°¡uÁÈÌà@R\x0003?ôÊ²B£\x0006î´\x001fÞ;'Ð¢Hh"¢'ÅËm>\x0013hQë\x001eÁèkÖnN\x001a
#\x000cïlÎ@pI¤;\x0010Ïk\x0017O±Cp­ûÐiÊà4\x00116JÄ¨ÒnbyBl3ÊÚQØöâw÷×ß¿¹¾=QÖ>fpÊÅ¸l¶¹zí\x0015ïoÿ!z\x0012_îð8\x001cN{´KzUí®çÚ?ö|¶H\x0010\x0003'¤)TÎÓLW\x0016¦«CâlGh¢ \x0005ìÜUÿ t¨c'íeËD&.;ù\x0018:aÔ¶\x000b;\x0004ìÈ\x000f!p+ü\x0010G¯èØóK#ÁSt}6óDàV4÷úµ\x0003c=7\x001e\x001a,C°\x001ex\*} Õ(¿ÞÁ÷FYj§b	\x001ecaMI¡ÙÀùA\x001ctèuì½C¯agIXI\x0007^Þ\x0014\x000b9"º)¼êA«Ûì\x0004r	 \x0012L½6p\x0007Éb¾\x000c~ÌL,à{fÂ'¨,ÍÜ\x000cà\x0001j¶\ªL\x0006¥)\x001d<
pHBuð*Á\x0013\x0004ÎÞÙ Sj\x0001O\x0002|\x001f\x0002×Ñ@
\x000e;ùLl\x0017øäöð
9XIò
¼B®»sã\x001dt\x001c-àU,;I/«îäöºâ¼k\x0002O\x001d|¶ò*V\x0004rþSBÎ¨®m\x001f27»óÅ\x0008à\x001cA$9MÖô^RØl]Û2»:E\T$2:Ã¤N\x0010uI\x0019\x0004\x001e:®\x0017¸\x0015uI\x001eó\x0006
\x001e\x0012gú\x0004»D\x0005êKÂCR,*ª½U\x000bgO{P¤ÞÁÅÌk
A	ó:'dc
ô\x0014À­¬&ôY\x0010G¿ ûÝ/\x0008ÆËPuÎ® 8±û\x00038QÓ\x000cìë2°¯üÇÇ«Ûw'KüØ¦>7:/Ñ\x0019ox(ÐZ!\x0011û4¦³2¯Ú½IM\x0015<¯$]ëïÀ®@¯#Vzx`\x00124E%hCJUïÔúÜ¥O;\x001a¸Ä\x001dZ¸ÄÜ§³âæ 'Ô+\x001eìÜ;ìf¸2~ê>¹¨¹ÕíaTdæqF)ÊÕfÞ(É° Ñl!íQq]\x001cE>¶\x0013t{õøöT\x0007¿yâ»ö \x0002CËEK?ßL\x0018G</Ô\x000eMªaGC\x0019b¦ñÝ\x0018³Ì7ãö_\x0012P
Y*"h
²÷!\x000eúÊ\x0019\pÀ[b
Ú-=G6ª´<úÞ\x0013\x0013,ßÌ1V;¢XîàråVÖ¹;æj¥Õ4Ü\x001eÀS7kF\±\x000c.»Å|7W._ZëJÄGÚÙ&=]½Ñ?_ßÞÞJ5S|W\x0006eÛÊ7Ýì©Ø\ä½¿ô/Û\x001aëæAùsª*\x000cêV,û¿¦^ î\x000c³Ã
\x001eá\x000e-sô^	E=\x001ak¤\x001dBs\x0019±\x001b%\¸ÏTNVE&¡:\x001bÁV9\x0018U{Ç2[×ÇCé,LSÓcÊ\x0016
\x00133Ð\5¿q±LâÛ9üÛçÁ\x001fm\x0013?VÒ¾{¼¸¾¿~ÿþdÅkÍ>W³¢Ì\x0016\x0001Ì\x000eèÒ]ê
\x0000g¥«\x0007&Ï`¢Ðï\x0000îOT\x0004Ðeì0È\û;°P:²ÈC	=)Ýq¡G\x0016mÙ¨!_zÑjÄMîÃ\x0012\x0006aK¯ÃÙ8VA:\x0017Éf\x0001ê"jã¾¸{|¸¦6§ßÜ=~w"
Ýü\x001fCvz%\x0005^\x00034®Ù^èhV7ª\x001a\x001cÍâõ\x001c\x0003PgPÐ¨ó\x0016JØL,n\H¿@\x000b-\x001a#\x0014ç\x0010Pù{E#\x0016sïì;\x001e \x000e-æb\x0002®ydº
\x001acÓMO\x0008vh9Dp²±O\x001e\x001e\x0005`\x001a§\x0014\x001c`Ód7Y7\x0011\x001cr ¼Îd\x0019;\x0008>gJëÈlCòöæò&iöÔæ¶vìc@gÁN\x0002»HÓ?ô\x000eï
X°rwä¶NÇÀ\x001d9í3Ríª¡ÏmÛ\x001cé´\x0017é3r4}üÈ \x000b¶ ïk¦Æ
Ñ\x000bd\x000bfï\x001axÌ\x0000Þ\x0007$¥#Qù\x0005¶\x001cuEaO\x000cp=Ó¡×u\x001f:\x0017Vì*°%°\x0014t\x0011o7Ã¶³È°³\x0017\x0004Y ÁÊ-´ÈfJK®¸f~(ÂÃ®cï\x001cv-\x001bP\x0002M²¯¸\x0005NHª\x001c½
yíàÎ ¬o\x0000âD%%8$)³¡\x0017\x0006b\x000b¸àp°\x001aHà¸rf+	Èð\x001dÔÂ÷£mJÒØ;YIg\x0007àºã0\x000c/àÑÀé\x0006pT%
<D\x0004ïÓ^\x0006á\x0005<Ip\x000bà)¡*)ÉáÊ\x0003ÇýB9v\x0014uð²c³È%¸Gÿì(\x0016Ó\x0007\x00153Q'ÅøéaqOÊ¤7rA\x0000wEVêÄ\x000bd£¯¼eÇZûxAír\x0007·\x0002<\x0014 {À\x0011'
<æàýÙÃPÄÃ`÷\x0012uÏ¥zp\x0008-øñµiýAºåaÚ|èû«/îÝr*{+\x0007ø¥Øº=ÖÈuÙ¾dØ&Ù2¨ö\x001c5\x0004\x0007å\x0011Ç\x000c
Á	yÞ\x0002M\x000b\x0002\x001e»\x000c\x0000 Ks«U\x0005+}DWÀfgÇõ\x001dZÖ{VYÁ\x0010¸4\x0000l¢\x0004ò\x0014z¢U\x000frEí\x0005IÃdc<\x0014ÜÅ<Ã\x0016ÁPÊ¡K³%-\x0002§>#lÔzMÀr [,\x0005ßFÀ\x0015ç>Ø,Í61y)
úËze}\x0013»æezU;è·dp+û-CÜ\x0002\x0003d\x0000¨èmÜIË\x0008ÙÚt\x001e\x0010#vä,	äõäÐ)\x0002e\x000cèÕÚSrMä\x000f\x001b6ÔG7ì¨8Ç\x001dÆÈõ
ÕA
\x0001WAqIÍ\x001dûÉö.(úÂà@«\x0017\x001azÁà3©TQBSb\x0011/_g¯nà4¿\x0005ÁGn®):¬N"ÖôÎ©\x0014¯GJ¼ý¦xcb\x001dÌKòíL\x0014ï±Ù¸dÕ\x001e\x000c\x0012¥Æ¾/X9I¬|FgÐ\x0019 e\x0017v\x0013´¢\x0000\x000eÉë:¶l\x0002I¢5òD\x0008yt¨;)ü^Ô4Pßå]@\x0017Ê\x001b1mÆ6Þ zfÁ:Ý\x0000=\x000eOÔ¶°nÕØmc¯R\x0008Ä\x0019õu\x001beª>ªu[ö½\x0006qß\x0005[>¡ã³þä=á¢ÌÙºE\x0007k\x0004\x001f°%°C\x0006à\x0006Ìð\x0003v×\x000e,
\x0011	+Ê¢0jÑ¡Ó\x000cà\x0017lÙ\x0002pç´Ma\x0002\x0006.964 Ied9\x001dù\%g|ó\x001dÆî\x001b\x0008Çoül\x000f½ÜC$»µ¹â;ç\x0012Ú*Í­£\x0000ø \x0000ðñâ³÷Wo¾º:YãBC¡½ [Wf¦gN<×4¨ûåhÆ½·\x0003?ÕWÝ¥gã¹\x0005\x0007ê³k\x0006\x0007Ûön	²\x0013éèåÀgÏ|y À¼\x0003S
ß\x0006¯kÐU\x0018\x0017¿þêêáúêñD	ä¡Û:îÅ]l\x001b\x0003/YâJ\x001dDw.pe&\x001að)g¯8SÁT5½N~,Yòô\x000eb ¹?\x001fZ}\ç\x0018<\x001dZ\x0012Ú\x0005\x0018\x0018³rQxÎõÑA\x0003µ\x0019t\x0011ñ0Ý¬è\x0019	)­+½q@öÂØìE
áZ\x0018\x0019ÔÎ÷¶>;ÈËwl=\x0007e×EÏõ¦\x0008Ø»¨\x0007LX\x001dÛ©á\x000e²±Ï9%\x0013qÝçyf2vc\x0001\x0006$§\x001cÑ{ÜI×i8'âÞ#ßÄ¯\x000ftÞ9ªáAíà\x0001ô8tvL$\x000f'µdÊeGU\x0007ß¼j<&CöiÀ­ÃØI\x000eé(\x0019E¢ ÅÞ;×I\x000fF±:¶\x001cK\x0001)\x000b¸ìä!¼Ü£9Ú/ØòV5âÚôïã\x0011B\x001d[òA\x001a°f-u\x0013)åÝ°~)\x0008ËàÍ\x001eØèÁ~ûîýÍÇSñf¯t1\x0019þò;Ú#º§øqÛ¾\x001c'Ð¤iptq)p¢Q\x0013²÷è6ÕÎ_7³Ä2ÜÚPÔÍÊXñ½Í7AK\x001dq®.ý\x0008\x0018?ê²æé`B\x00181ÆÀtw6\x00075³·\x000eÓâ^tåÚ¿¸9Uy+9A\$¸ºF\x000c+c\x0005ÓµKKðð¬L×QÕÅÔxóÐxÅ]RUì®¤\x0008§`Æ<¯\x000br\x0011ÈN¶Z6\x0015©IWJAäÊ@\x0013ù8ÒDW\x0017_üø\x000f¯ßßüíñTÚ¨¤ã\x000cãõÔZÊùÇþÒ½XNdN¦*ôLä!yîL¾µ­«¨v\x0001\x0014\x001céPj¯Ê\x0001ïíº¶Y\x000cEÌ²jI3\x0005Õ8ÎL3C\x0016CC½Ã²+×\x0008îÀÿ/sï²cËqd\x000bþÊæp7\x000f%¤ºR5!\x0015\x0011I2Jàð$+)\x0005\x0008(ôì~Âý«yÏzÈ?©/i7÷\x001d¶,ÌSìâ\x0006vâ\x0002\x0017E\x001drØ\x001e\x001eîöX¶×ïlDÆ+ÜC\x0013Ë7$7u\x0005WÅznnTXÎ\x0017ð,Ô\x0013ä	l
±k%åÌKÓÔp|\x0018SúîÄyïÂ\x001dX\x0015×ÔäæFpy®ímÀ\x0005\x001695Xå\x0018Þ^euê
¹G®wàIÔû\x000b\x0015\x000b~ôAÏÚ\x001bre\x0016oüEVÜrÊ\x0006À¸³'´¸³}\x000f­	\x001f:Ë¤©j\x0017Æi+oXÐnÐÂë<»;iøËO
ÛôTè|êÕ7(Fæ{#<g¢öVªÑGõÐ#?]}^|¥ÞeiZÑkµj7Í8ºÂ~õ\x0019ú\x0008ÐQ|ß©ÞQy\x000b:Í9§Õw(²jq"¼Z\x0010ÔRdÃ\x000eo\x0016\x001fb«ÃH>5HQ\x0014ÇïO\x001dì2û\x0006]Ä\x0011eØËªÖpBWü\x0010Ó$]}^|=\x0006±½8ðP_±­	´n°óÀ\þ\x0011éu²ÉÞ\x0005ÿÙg©rP¯Q5\x001dFîhx\x0013oÈâ*¤*×¹_X\x001eTYõç\x001a­¾Cßaº\x0013>x¾\x001e\x0019í\x000cièp\x0019U
Yìh\x0015\x0013ºe?ÉÚ32Ò	-2R_Ø\x001aj
¾&å\x001d\x001cF¿>­9yø¾ÁKY\x0015rzÜª- mêî\x000e`Á(\ÕqúB+Çí:MÙWÐrC\x0017l£é£\x0003Å\¹f³\x000c6è"\x0017\x001aÓ ª8a3zÜ+d)¼£LxCP»£F¼\x0010ÃpìJgKª=¤\x0011TÿÍ\x0008Á·\x0015ºo\x0012½_¸9ÃÆ\x000e°K¢Ö3\x0018ÊdÚÉí\x001f$úõ`)¿9\x0013°ìUY¿oÄ¸þ\x001bØUK:²"\x001dÇx9VÜéÚ/ÍT~3ÔþããóÓ§¯¯8Àóp²\x0006ÔÃw¿×½°Û§ß2A§l\x0019îþ#2xXr².\x001d¼E=\x000bÕ\x000eç
8
à \x000bÓÙ\x0004E\x0004Q\x0016kCæÅäaÂ½ðo½0]=q\x0013OÜ L3²VjOt\x0011çâ½Xæ(BûÜ¤)Tm\x000f<\x000bÝÎôÆ
5\x0008TPLÏÊ[·¢+ïW·û
;t\x000f\x000c2§òë°(ëYG\x000bÙ[ê7\x0003WÔæ÷àò\x001bÔ¶hXöÕÒc!Ciòï_\x001fyç_i\x00102^/Á§ýG9÷Ë\x0011ÜÓãwçÜvæ:\x0011Ö³úH 	«dGú7VÕ\x0002L­ÉóKÞ Á·
\x001cúBSanÏ\x0002UÉ`|¤\x0006CP\x001e¡¡J\x001cÇ\x0008¬'\x001c\x0008í¡$1¡Å±R\x001c4\x0017Ç|³\x000c\x000bt\x0007G`¶.ì\x000e­§DJ\x00114%§²QC±¤&	¥&Ùµ¾`à\x0008ÀY½Ä~¬\x0019¥Ãbº\x0012}ö§ûOßÿø76¨üêéZýï\x001aÀ9²Oå\x0012\x0019ôTChWPk7¬\x001d®æ\»SN\x000cËÕ¤+\x000ec×Øp\x0011úA>"n#.\x001eØIÆÅ^ÞØª\x0012ùâC\x0016\x0016Øù\x0019Í¯°Ä\x0003º%è\x001eLuàhMyÚ*\x0019Z*\x0013»È¨[\x0005ù©BÃ*«\x000c\x0003Ãå{`WAÀ
\x000eÅÐ³-
!ûíØÉ²0l¦Ì×Çû\x000føêñJµóÒªg\x001dDÃ±mj\x0006/ÞÌZ6·#µæ\x000c\x0006§½a#¯ïz9ú³öD/=ó1÷\x0016\x0016à\x001b®0¡Ê`åÞW\x0007ûµ}eQ\x001f½¶©mc0¸Û\x0014ø\x0012ØU*+åèa|¼cWÔ½­¡\x001a41ï
«½Í,êáùÛk	Åù \x0016\x001c\¸¸aú"¤ÄJó·ÌJ\x0016âýFpâ\x0003ÒZ|jH)\x0005ÇÓÅ6a\x0005ü´M7T´&öÁAó5!6v;v(MmèZ`\x0017ñÜAvKÉ8ÏA|v\x0001¶«\x000b:êÄ\x0016tT?Î`ô-Ã\x001ee¢g°é¨\x001b¶Ð÷°vÍÛÍ&vN`Aìôý\x000e7á\x0014ÛØûO<-é,ß¸\x0001\x001c\x001fcßÒ¤Luÿ9À¨b%Ö©¾Xf18ë\x0007¶'\x000eÀ\x000c÷\x0019½#ÂVJõn±?¼(jõüYfÅ}_#¥Ø+N~\x001bn\x0004°\x0013ü \x000c°ÿ§|rþhàÉÙ\x0006\x0012Á6rÁ¬3ìwÏ÷¾¾V\x000398 íotI®
\x001dg|¥\x001e`¶Î¥ñ=Ñd\x0013J¹T9¸\x0007êB\x0006ÔQòÂÆvB\x000b
Z\x0002*WÏTm»ÿ\x0017 ðÖß:Ù]*T\x001d\x001alB:´¢Wú ¡OqyOè*\x0016¤É\x000c½(1"æ/\x0014 i¤ÆD\x0010!½²§\x000e4Ú³.Êû\x0015ô°
1Æÿ'¶\x00174Å,6cöÊ£Ï\x0003\x001fÜ\x001c-°Å\x001b\x0004nÿß/¸Eëô[\x0001²\x0003\x001fÆT%F7I\x0002K¸Ìî®°ÎüÑ\x0003v\x001càÂÔ]$öùË|ó^ÌÏ
à\x0008\x0002 \x0010}5×°\x0013Ô_\x0018,\x0008\x0015¿Í\x0000/°«ÄóÜH}T¡G²v´*\x0006\x0003\x001b*\x0006
°k£\x0006W\x0005Qv\x001dÆý6°P.\x001ei½?°9{J¸I`½\x001bÕÈdD\x0012\x0013[ÊÄ¸*#éV*G¨5	S'ÚH!7l(u@ç¸\x0001\x001b^eØt+JalOòT-rJ¤ä \x001aY\x001e>¨¿)\x0014¶8W½¤öæ(¢	¯Õmð±ßëSÕ§"Aó¸y¯êJ\x0001j4\x001d{Æ²Ã\x0004Ïr{§\x0000ÑJQ}ßÕ­ÁnB\x0003¼È2\x0006y\x000c÷i\x0004\x001aMðÞ\x0018©ø¿&­j\x000b(~÷Ä\x0015¥Í\x001aïÚkk{²\x0007y%AvÑï\x0013\x0004å\x0018o\x0018T$«¥\x001c¯ÞÆ_ú²iW\x0005Z{ì!FÂ\x000e±j
eaý/À	hñg¯¨G)c\x00137;.uA\x0016t)ò\x0013%Õ~Ó\x0011"\x0017ä;LîÞ÷;²ä;Ô
¢ñ©©vªðÙ¬ÆÕ\x00059JdX·aóø<\x001d^;®øó
5\x0011\x000c«²ìßõ¸áVÏ\x001b%?/ÃJTôæîÐQX¦LÌjcH®C¸\x0001/|4éÅ~N\x0001Û\x000e[eÿ\x001dØ\x0019éDÀR-17%?ªæ#\ \x001b@KVR³\x0008µÁ:³Yr¶jø;´¬_z\x0010J¤Æ·û© §KÁ\x0002Z:Qé\x000cÎ@áöi\x000e\x0006{ý&H~ê\x000eìÐÛEÊ18ªµnÚ5n^õgC§\x001d[®\x0008\x0006!)«Ô¦¬ÿfxr\x000e7\9\x000cº8¯ß<ëG|¼xæ A
gÓ\x0012l<=ãEcþ0¬>ï\x00007ø«\x0014oÂS\x000br vl ÂT:jUíê.TÇØ[8\x0005\x0010;v\x0007©Lsù\x0004£;e*W\x0002Ø
X\x0014h&çXéJ¤¾\x0017%=ISz8®Nÿ\x0008§ÿAÂbÓ#\x0004ÎøµôÈx<ô)2ÞÅ¸°/RG)U\x001eùFâ\x0018\x000e\x0018öhÅV	Ù±EbÿÄb\x000ej$¥õ`vÌOÇSðzÁ\x0014Îz\x001aÕC".HÉù\x0010w­£\x0005¶Ü!\x0019¬8Ù\x0013i\x0011y\x0011a"kvè\x0005YÒ´Aøs3üÐ_wß·£>¸:¢leîoâ^­\x0008áäAmmqËÄ&Xo¨cÛp\x000e~0\x0001ºd2Ó¾
:É¯&GÜPµõ6ÔÕ+Lð
áÛZÕ\x000bctqnræt\x001dA\x001e²ÆB¸ËMÜ`\x0015àÜ<Ç\x001bÌ¾¦,FX1û?<<??Ìôt¼¾N\x001bú\x0015nÞ-ïmïÉ²A¢ÍöFSK¹å<gLÜçÝÕ\x000fys\x0011¬á"Q\x0015Þ^?üëÃ·ß}¼VM8'5ÎFñB\x000cè¿ëNX¾3©òr_s\ð'L\x0015ÍÁøãÛÿ\x00171
Øl3+çzÅñ-õø\x0005ù R³ÁE\x0011¹a¿\x0013+¨"å)ÜT©6æ\x000e&r\x0004d/\x0013*Hg!þ·É\x001eÿ9Ë\x0004ü·VÃK©Ðæ&¤ò¨\x0010!'ÆE×\x0016s\x0018\x0013Z¬\x0007ñæa7!ãÞ *ò0-f%&r\x0016È´^OÈE!·Åt@UÙòÆpíïA\x000fµ3Ïs?\x001bÚ\x0018ÄÐUBWèþ\x001en,µä7Ü,WùÔ0|ôÚº\x0011N\x001bãÀ\x0013Z\x0003#½14UëË	gvé3Cêh`Kí'\x0017\x0010O*-ÊÅ+fykvcÃ\x001fL(øÁxµÚE
_OJ¼_}1^~1¡Áx®çÞýc4ÜÅ§Æ\x0011Ê{?°\x0005ÃWWºrmXeãà­\x0012ZªÂêµç\x0014c ô]Qs¥[ê¸¤{\x0008Að´±ø\7k¢å\x0012\x001c8\x0006ª£_A¦uG¦CÍÚ\dÖÎ>\x001aP:ë;\x0008fc8\x0003\x0019ã<déÛ28%\x0001\x000e%£J\x000eÉ\x0013!x6è9NÂÏ f¾¸|íx\x001dr\x000e\x000fx¨Ó#\x001e³Ñ\x0011\x0004Ux<ÐßßXÅÎ9Ï^E1Ò¨üð÷\e´Ô¨bA;7¢\x0018¯¢\x0018Ïö\x0014R9¯ÞA¢\x0019NÃÍ>Îâßª¦T%ýÎâb:Ú«ðc\x0018Ë,cú]<³"
§²>Uåÿ{Ël\x0004\x001a\x0013Y¦ÝaL4gÆ!¢ Ù\x001e>UûûT2>qÅ'öÆ\x0013[÷W\x0001Ï	\x0017«TAw>\x0006È
Nm$\x001b*QÏ£[ZÛ¼WVKLb#c&E®g×#ªÕ#\x000b1\x0013\x001f	¡\x0015·¸º¬z4\x000cQÂpjQ\x0004m®P95F÷Ã¹¼¹|À£/TÈÙ.ÄÈ­Ë«ËSù\x0018\x0014Ä×è/\x0006ôêë.âëØ³*\x0008å\x001e)B±¡Ó¸~ÀÎ¶ÍiÞÔèü<êê©«xêT\x0010\x001aqÕüa\\x000cHl¸M~PRS\x0012{Úßa,V ×\x000c+­ÿójZ4,X­Ï_¼4\x000bM9æ[Ú´Ñû)\x001eâZÐhÈ\x000c	#-üý3Í¸\x00065ÙD-R,ëmÄLY©¨£H0_ã}rË!¸A²&\x0005}^ý7ßÜä¬°ãò±µµ´y\x001bØ>ÎõÜR«ÕCÏHñÀ\x0018\x001b¦"¼9åØ¼sÖ=u°$NIÌÒäµ\x001eÐu·Tµ±A\x001a7`/´ [pÿ¾U/Ôú/¤¿V\x001eø×çû¾å¯%oVSy~Åqº9I(|\x0006\x001fÒ§©¥\x0019\x0007ÝjÒ¶\x0016K?êÌÔ)\x0004¡Fÿ\x001d`;\x001a·ä¤mvA­ÁèÄ\x001aóv\x0013:Hh'7hK([^û_V\x00154X\x0006Ul>(@\x001e²º\x000e­ÆmSmê©G´a°&´`\x0017yQük Ûw\x0004ö¥#bÁ&¸Mè#h\x0012ÕH\x0000\x001d\x0015tZ+h\x0012ÐÐM?/tÄ C\x0017Ö»AÕÀ*IKj^).jAÈ\x001elÐ¦è]Åw\x0001RM\x000eÛÞý©£]ØÞIlh¶C95ê×Ø¡ùCËOä\x0007\x0010?Þÿp­È ±õûþ0Ãâ!¤Ýb3\x0006\x0018'Cý®Ú\x000bÖh`ü\x0002$3Ø.\x000bÜ³Ø\x000b]ÒôM\x0006\x001aÈ*ÙàÄ\x0016`?Ó±:Núè´âÑ*§`ÏËl¨âé\x0010³è\x001b\x001a|\x0012G\x0000\x0000\¦Z!¦:«\x0000\x0006=þôhxæ\x0012°ëè¦y/;v\x0013Ø\x0015¬Ä( ÝWê\x00079xÿôÇö ÎÄ\x00168q\x0017Çß±3ðÚ:v>rÝ±i¤`d\x0008NlaÛ\x0016(\x0001vijMj=yçFqz`\x0007áùe}?o~x6S~\x0003ö\x0002¸8x\x0015Í\x0003R\x000f\x000f
b\x000f¯\x0019C÷j\x0016ë\x0001\x001aÄp\x0002¾C§k½ñð,}b\x000b'±0Ô¼ÂÎU-ÉÐÜ1F&¶`ÖD.T\x0008WàpÈ,õ\x000c\x000fö_iz\=w\x0014Ï\x001dk\x0005lq0\x001d°³[Pñ7lá97twà ¿ ¦B\x0007j?C&ÃÍ~þ\x0018¶î·}«°CrÃ\x001d\x0005Sq÷tèt\x0007ý¢\x0008tÿ¹_>?÷ÿI\x0007ý ~¹ÿêJnÉ(>íÓÞåf|\x0017Hw\x0018Ù½«\x000ez\x0017_ö5Ú°ý\x0013ÞüíFýö\x0002\x001b~\x0016ì©­°ã\x001emÿ\x0006î9viî\x001c»¼~øìùáõ/ûðïÿ÷§kqVb\x0003JT(¡Õ\x000bÕ\x0003T©Æ[*íÚ3W\x0010Ùl«\x001fòæ"Xãü\x0006hd¯¿}¾ÿôÍÃýËò×cÎòæÌ«»ã·ô=\x0006­aþ\x0016W£\x001bâïé»>óDyí¾\x0000h
,"w9¿]âüî\x001fJZNq\x0010õ\x000cwÉ	,Ü%{ê/oJ<êJN\x0014\x0002¬msqhN¬°À\x000e\x0007ÂÜ\x0014¸Í2JìÚS¥óÕà\x001c}ÆÒ¿}~|¹þúÃ¯_®4ÕÏ\x0003Ü2Wâ\x0019÷]ãUõïü1
Vßs³]´\x0010Ñ>]\x000f}Ý°u¸ú\x0019o.Ñ:¼ ÓÏC>×¦yd|þx-WË##\x0006
~/uõfE¥1mé½éß\x0018UM°\x0002S"\x000b\x0017]E¾\x0006¨Þ@qxô=\x001btÐÒZ°´¸à\x0015xºÐ.{O\Á^X,ý¯Í®LlQ#)±È±êÒXµ
\x001e»$Äö~\x000e\x0015ù\x001c\x0003;\x001e|\x001e'ÃÌ®uá 7ÊS£\x0006½}ÿÒcßì+x­!=LqWGú?C±L	4Ã6Ç»²±0\x0005DÐCåß!k0)xÅ
ï7)2ÀÂ0»3{I\x0017L\x0017KôæòÕÇ
Z\x000e¿ú£ªIMyXx4YqÕÉBãs¸bd<\x000bê(ç×j\Wá|±Â¸jíÍ\x000f}¼ÿóãÿûùZ¦=\x001ay\x001eÿ<;)c ý&d^ t»\x0016}.\x001b}}\x0002\x0016\x001f\x0011òIQÙR\x0016c\x001c5éÊº\x0000NQULïó\x0007½Rq¨\x0007Çc|Í:'°èF6'åÌ:_àfØ=h?©äOpÞÀ&1\x001a6Q
ÐJbß8}§-W2Ú Ö¦Õå\x0006Ì\x000e5)¢gÙ\¨g«,îM×Á-ò¼RQ\x0002t\x0001©/ñÎW¡á, [Òî{g½yÄ~´´µ\x0002 9Zl		ªü­Dìßº)dÔ´\x0006¶°Ûä8\x0012\x0006¯<:Hu6{¨³ªÅ
lQ£ÁÕ\x0014m½X\x0011; )\x00140R°Aaìñ\x0007x9É©á°¢³tÏP§aÓ|¢f}\x0006x;v(0¯8Àåî=a\x0004}	·\x0015
Å\x0001\x001erÊê\x0005¹E\x0014úK®\x0010ýB&QmõD\x0016¶Õ«íþæ§2ÁÏ5
\\x0014ÁÞªìdnñä ÎÔÁ§iºa½WYÉAGa/C¹S:¸Gp?E_nÇÄn\x0012»ÀGU'Ð¥§~\x000c¥9{ºÀ®N`\x001fj=P­°\x0005yT	\x0015NXí8$õôéÃo_\x001f¯¥´×?_vi\x0008`n~ub()¶\x0016nXÙY2gj¯~ÆK`d\x0010EÚïôüß?õôÝýëÄ¢O\x000eü\x0004BKi'wy6r9R¡ÊG1oÔweMNç£¢¯\x001cß)B$.$\x0019T6k_³ð1³Ró¼®VÐUB'Ql«ìr*¿9f\x0015@fÞ(L\x0007Þ\x0015v\x0013ØYrjÁùfÆ\x0001?G2§ö7h1µïñd®\x0005çW;t\x00065+ÓÃóÌpÙ°Ä%©\x000e;Å=XËªc\x000f\x0005pV«Þ°\x000f\x0001EJIéMêMV§{,1\x00111¡eô\x000ev»#µÚpµGÜ\x0011<sN\x0000-ö_u°\x001cÍãrlÌå³[È\x000eÜ~ñw¾Ð7¿î¿âd\x001bv\x0011ëA2æè\x000fÝ$°O¸\x0018àrÖ^¸àÅ\x0008rÖ»?³úb¯ø5¦i%sîmOì(Ä1¹è$·\x001eâxÇN
¿Æl5 )Øøñé3ß±\x0017ÆuÎÞ!¡L\x000f!÷\x000c¹Ç\x00130Ëér\x001eBï¤g|±}íð
¸ï\x0012H£q*\x0007Þ\x0007.
Vv°è\x0017\x0003:\x000bèTÄ\x0002Aí\x00177¨Å<\x0006«¯^±5\x0013xlF¸J¹\x0002C6£Á[OTGPlñh&¶xh\x0014­èI±Zèa
%Mdq]TÜÁuéñ\x001cÔ³|¡Ã1\x0006Ø=ý\x001fÜB#Ø"¿	\x0004kÂC\x0013òäíÑ8åö÷1=·ÅIa]41Ò\x0003²Ê\x0002áØr¡Yî c\x001ee \x0013ÙÈQq:²\x001a-\x001e*Þä£0°à£pD/Ëió>>R²¨§¢Õ\x001f©þ\x0014å½ò9óí\x001dèJ\x000c	¥E.æ¢<Ñ*YÞ}\x001bÊÃZ\x0003té4\x001dÔ\x0017m\x0014r÷é 1+u#æzÕ¡ä=Û¼A\x000bò+Htî\x0004G\x0015-Ä_L6oÀE\x0002Kÿækã{Ð\x0008\x0006v\x0014¦\x001e\x0001D\x000c³6¯ë\x0017cQ¥É\x0011ñFãþØB}\x0011ùcYKÕ.Êý6\x001fêF{yb\x0017A¬\x001d>'\x0002»\x0015\x001cÅ"F9mjU£i4°«Ø²uSZ\x0004\x0003¯I¾\x000c½Z*\x0005)a\x000e#'\x001eóõ0¯/=*\x001d\x001aýF1±A\x0017ö_JÊ´Ú'¬µµ4
R\x0004cb7-å?;¶\x0003ôpy\x0016aìV\x001bÛ>ZcÓG©QÞ¶fe[Â½\x0001n\x0004Ô\x0013\2Ýa,\x0014ñ£ö\x001fñs-§®=N]×]oáÒ÷ÆÞbÉY=ö\x0008+\x0016kB$fÅ£Ë\x001d¤#B\x000e\x001eª3\x001c:Lqñá?¸t-#A°\x0016ìæ\x000c³âÄAjDÕ\x000c\x001eÿDÉ\x0004=\x0003¥?\x0004¢Rñxòhðs\x0007x\x0014\x0012´£â(FÔÑ
j\x0017\x0012ÿ'sÁÏ-}Åý\x0017bÍ{DrÍÃÐu9=FµìÁÌ	N\x0006Y#!¸ÿòþÓÕ\x0004zªSj8^\x0014\x0013ZËQðF³ò=é§\x0014ÇxÙ\x0014±4I\x0011î1¹¿+²å\x001arÆ\x0016f5ø\x0015ò1JÂ¶\x0013Að8(èi'´Õ®yp\x0019ÎÃî\x0005Ýù«tNægÎ
\x0019¤¹Àd\x000f\x0008\x0017\x001c\x0010v­\x0006È\x0006BT£¶QeGý2\x001dQµ\x0015¡\x000e5I1ÄÔ@\x0004<\x0005"¼L{ÎK½M[ÙþdÇ¨øâÕ8v¿\x0002q±§å1f7±I\Ô-m otÄ® 4Ç\x001fÉlQ®°L|+YFíÔQjLàÓv¼/°Å<Z« \x0019HÊ¯qØC©VïD£Ù9\x0018k¤#XìT[°ßó}.|mØI`{\x00144ÓþWlØsúÂò\x001aØR\x0019(?3OH TMKI\x0003y5!áqBë"iL\x0018\x0016\x0015Ev¶\x001dYMHh¹TÓ#!\x0005lÂMRêð­3ª\x001b¶XlïÁ$=¼`ä»\x001f\x001d¸ VUð(íÓ\x0016\x0012\x001cÐ
&\x000b9h0zä=VU7Ð\x000büý»ÿx5î\x0012z\x0016\x0016ò\x0017â>\x0013sèØî¬|\x001aoWý²ûäÆjfë\x001b9¢ZpÐÙ-/eôÌÎs¦Ü\x0018"¸à7\x0000Ç¯×^\x0006¤lÏû\x00055n¤\x0015´ôl0:T\x0015À:\x0002ãö\x001eàÚàpLhJç\x001að©zj\x000fÃ¬h{[oÐ2\x0003Ëpíz¢ÇfkMA×å9iI\x0012Ï\x0019)þYix\x001a¸´²\x001cØÒjr<Å.ê\x0014ã\x0011\x001fÀö#²¶³2:g±>»` ¡A\x0007vê¡ã\x001c±7(D\x0013X8$ =\x000c·ÂÕC{õa§°2Ü±åC`
\x0011NGwl¼ûK\x001a\x001bÛ2Ü°E¶\x0002¨mxíÏÚ/.\\x0013\x001eæ4ÆSÒ/Nj\x001býð]?®%¸\x0011P[Øõtö¢xÔÐ3ßx;æÍê4îÁ`P¥\x0011À\x001b6$\x001c$à"fByHW\x00181GC²4C£YnR\x0012\x0010!`hPS\(ã4$KóêÃ÷\x001aPÏ§C£u\x000eÕ¯iÈîÐÕCbçndÓ)ÂÍpÓ·÷\x001cúõ7\x001f\x001f¯%.Ñã\x001f,zºCÍ\x0015pH3àA3
gÏ4\x0014\x000e\x0005¹BÞ,ø»*¯\x00135ÉÆZÍÌR7d¡ÈæQJ´lö­\x0008Cà¥nÈBÍIIÈp\x0007¶Å\x0005¶²
Í
5ÂóF)3å0«îÏ«ÔY­V»!'ù¼¨b©áKVºJ!Úrl\x001brg.
Þ^·WZãhÙ¯\ wR:epe1Y­s\x001b\x001aS+ä*ëRo^4ýÕ:û#°#7xfÑ(e¡0\x0000Æ&yM3·\x0005²\x0017_÷w$V#ê½¡\n"
\x0019ÕWâ	VC¾À¨úJV14\x0000ýê+ñ\x0001¹IÉ-q×a\x0005®ÅÁ×1dY7hù©4´ðæð¸íÚvuz^­ ¥´d?OE6ÈHÑúeÓ¦bÄ
Znép\x0017¤"[\x001cßX\x0010­È6'ÉW{Ú=Mî®È¯¥ðÐj¥G ·m°\x0018B\x001a\x0005´\x001b.W1vQÂñ¯ñ\x0013\x0003ùx<1@W,kµ)¸º\x0002\x0016\x001bÂ\x001d\x0015\x0004¯°\x0012WN+Q¼\x000c\x0001Xé\x000c\x000fàÕ¾.¡âØ\x0014\x000e·rÕw£¼·Ú\x0014$7E\x0005o¬\x001eBU8BkSúÓ2fõö¤#A¦\x0016W7^äDÕL¸wh¹\x001a\x001e¡±\x0005Â{\x0019Ïº92o\x0010d<&ÜÛY÷C\x0016ÛÎ\x0002t\x001eeÃ¸º\x0008c^>uVý½[# ÀÞ'0T±`&+j¼¾?\x0010º\x000cQ;C|bN\x0018 
Ímqxúò.´)÷XØVZÜ±%V\x001a¿î2¦(óê3ÌòìGyÒJXç,Ê­cd;®\
ÔÝ×ÆýàW«1\x001ayuæñX7\x000e\x000cÔ3Ð¢æc5¡ÑA­\x0005]äTºml\x000fC2Óc5¡=ÒnÚyh­Çófûô\x001auß\x0006§ÿð:\x0015Â\x0007¶ÕÙäe\x0001¿F¹Ú'G²Iéôs\x0019íð\x0005¶8A\\x0001!¼Ô\x0018cA*ws:Øp;qÚÛ}Ð½\x000b\x000eèÅ7Ãp@#*ëz5!rÏ\x0007ôjE\\x0011(\x0001ÌÎßÑ\x001aÀÁD(»!/¹\x0001Ë~FAÏº¬ú\x0019<nÉ°FN°ôåÝ`\x0016ÝW'Y\x000fñDâÊ|ìÕWãÅWã\x0012÷RËê\x0018qÀmîéovÝtºw-$»¨vóÝ ¡Õ®Øò¹÷õìoq\x000e_e\x001bNÔÆ´â-Ö;IÑ±­\x000c/sC}@Ö\x0016\x001dAÙ
[~º;¨\x0019\x0019Q9u\x0012»¬^Ý\x0004cÂNà)\x0017ºg÷^\x0006¶Fµ\x0006°ôÙà\x000bÒÜ:6ºíõ3b1#±aË\x001d@.1óM\x0003\x000bRÙïÒh
P;	§ráõOW\x0013:öè4Óo±x±¼e
¿\x0010O|\x0011¿3cK1\x00185S½\x000b9â=!\x000b£ìË\x0002¿?\x000c¿\x0013cx¢¡îS_þ¡²4Ö,«ê\x0019¹¯¥èê£ü\x0010x.\x0016%DÜ£~Îds7èò³ÚR}&UÎýoB\x001bqÊÄqJ\x0014U!p\x000cËQ\x00087qÝ
ç÷Ë¥þâþXl¶·\x0017;\x0004<H#Sx½E²F×¥>ú­ª>}ýá\x000f¯×µ\x000e\\x0003G\x001fûay¶q\x0004T±Ëµ¦»x;Â­1`¼íq
ö]\x001b
ÇËNÊEÖ
j~3\x0007{-¾¦1\x00026qIp(\x0013\x0001n­J\x001f·*è2µÃ\x0017Ð^B£\x0010@UmÍpV(È\x0012øØR8%À®Z¸B MÜe\x001fØ«çÁ)I¢ce¶Ân]-ÓÅ\x0016Ï\x0017Õoîû¾ùþû«ÝU9;ÌsÛçhYgá.Ø
Ñ»j\x0011ZwUTwUõÐ èá?^W9£r~?ú½÷\x001bîý¹B\x0012::
"\x0003Ìi]ÜQÝÕ«Ô#¡xGNH½w@l°7hñÔ® t\x000e­l¾#\x0019TV\x001fýùt~ýðyíW:{ø\x0006dc\x0016Î¿L=8)7sÛ­\x0006Nª7=Özôð.úï ÉìÉ}Ë\x0005@³T§1A¿\x0019¸\x0014%³\x001dpÇ­!®;Ô\x0015/³Èh\x0008ÊÄ9µ!o$q§kÞ\x0005W¾4\x001a­¶tæ´Oà$yþE\x000e'¨\x0019ì`Ø÷j|Gç{o\x0003÷^\x0005AÐy¾f\x000fÕº=.¨dèöLl©ï/§52j\x000eè\x001bÀ	=·\x0001\x000b>/Út\x001e\x0016\x0011\x0019>
|æ2\x001c©ÏÃ;´ Ýð\x00133\x000fÙ©¢+Ä\x0004Ò\x0011ø-°³ Ü²Û°\x0017\x001a¹0<6ªø!­Wo1{\x000c\x0013=9\x0010\x0002Ê«KÆS¯\x0016;ÃbgÉçÐ¨»®°Ä0#Kóå\x000e\x000c¶~Ô1\x0006²AÀr\x000cØS\x001d7¡w@\x000eÀÌ"¦\x0005\x000eìÅ·eüÒàÉ\x0005Y_zgSÏÆb\x001bt²]$¶-RQ{¬fRú6e¸Ïgõ5±\x0005ëËFvÇV~
"®I\x001díÍl°¾&vØ\x001e&cÜé\x0018Áx?´>.°\x000b}½ß±v Áý7ÉÍeõÝ\x0014yú\x0015¹ñ¤ö¶\x0003\x000e2õ\x0000pp%ÏÑÏ
é)_ÔôT
{\x0016þW->\x001b\x001f<@£â\x000f[Àãû#à\x0014éw÷/O>=ôKþZ¥.+tÑ\x0017æ¢\x0007XAÝÔÒ*±ÂÈO 0õ%ûBQxhE\x0012Ü]\x0006Û2Ýì¢Ab?õ²wä£ÍbÒÒ;OaðË«\x001cåÉtÜ\x00059£/}\x0010½áFÖ\x0002Ï¬<íh42N½\x001d9gÐ÷Úã\x000f·<ÇaÙ¢1íÈGPN9¼¤\x0012åÎË\x0012uË¨\x0002ÈD>Æ´#gñÌI(ðög&´ ¯\x0015å#xÌÔ¢1íÈE »A\x000f»¬s¼²¯}Ád%¤«EcÚ2Ã>¨8ÞU«â\x0004m¢¯\x000bdQôbä*öÏw\x0019U7Û7Û³r&	]á¡	c\x000eÝ¬mw\x000e47hÑö#\x001dø ÷7jS\x0015.¬¶t\x0010[\x001asØ\x0018 VÇÐ7\x0010ì¡´
9Ê!)æuÁC÷lA±?¼M\x001cØ EvL\x0010\x0015©9m]]íìx\x0016\x001f¢$¬è©Í3¦~¯puf/p%9C5å\x001a3j9Ù
±;®|^\x0018YEÍpô\x0010\x0000[ûyä
çXm\x0016ýw
\x000epñíyuæéYtÎ\x0013&°tL§_JS\x0013\x001c}'àÁÑ&õÿL±Ù°<Ha¬ ±6/`c;ÎùT\x001bíà
Znâ±¤ØýK4µÿ\x0007Í\x001e³Ø°åZ7Äz(\x0019Ü~þg»m»a¶m\x0010Ç?_,PHê\x001bH],iöl\x0017\x000fMâÒ\x001a³ ¢õ¹uä\x001d.H\x0018}Uc6bG±Ø¡f\x0011<nÖ`S¿ÇÃKwõÁ\x0008\x0013U`öVL7ÅB'Ù¾ªÀë/º\x001eH\x0011n\x001e¶±¼´Z$Ö±\x0005;£GË\x00128a\x0003ü\x0018S,«k«k+»ã
Ö\x0004ÕØsäÁÙ½.«/±/1[ª\x0005æ\x001f#\x000bäÁÎ\x000b4ùÓçúÖ\x001d%v@lå\x001a*\x000cjù0\x0007
EÐ
[|©À´]s¨,ÆÍ-Ø a*­¥ï\x001fqÞ\x0017üò\x001c­ÈÑ»éÞÛ,8¤/\x001f_Ö\x0001ÿáq\x0006¶»¦þ\x00028»\x000bêØ¿À¨ð*Càßß¿|õñáåj7v=Q\x000e­>\x001fÀýb""¦6:¡ï«Wn¤ÉM5	¢Rx
¨\x001eÕÿUE}¢1®hUUURðê°ÁHÖ3KÈ°¸à~ð\x000eE#=î)`_Ã\x000f9\x0001«þÓTL\x0002¨	$Ê\x0008\x001d¼S;"ØÎÝ\x001b´\x001c}ÂÁåDpØxä$¸aYhU&¬xb´-MÒÆl\x000b¡"ÉB\A7\x0001ÓkÃÏ\x0018N§\x0018Ë¡Y~JF'f\x0017\x001a|ýËuº19WÔÅþQ®)ùÈ\x0002\x000bõÍ\x0012ng\x0010a\x001b¤\x0019­¦´(Jª2]É°S&\x0004é¨\x000fµÍ2°p\x0003)²|]Xú\x0003°ûy\x000c¥²â_T&ªLNkCc:4\x0019È\x0005G ©ð¼áæ`«U²KÚÿìËûÍuN|ï\x001cÄEþ½áÌ\x000c\x001cÐxì!qºÜ¢ãl\x0018\x0018T<ñýð!£Þ"Të/\x001aùÐìIf\x0013WHR\x0002e\x0010æ¡´,áÀJ\x000eÓ-xì@\x000eÇ\x0005å¤Ehÿ;`Ôo/Y¶\x0016\x0015ÉÊ, (\x000fdâ\x001a\x001d;ã0Zÿ\x0002-Â^<]Ûð\x001f^ÿãjjâ±"¼Ù;c(Ç;x÷æB£ö®Âb°R*·ýË÷ø\x0004Ê}\x0017FÔjæª\x0004,\x000bS#èüª\x0007¸±ô%ÊC(*ª~ôp~9\x0003ÜÒö\x001aàQ\x001fs£)ØD\x0015+_}
~QZ,Éø\x001d¸\x0015)Ã¤\x0010pÇ\x0002*T~óe®\x0006c×#\x0019$:L]zúÊ\x0014#p,Fw\x000bv\x000e9#\x0007¡C\x001e(ÉîH¬\x0015\x001f;àÈ.ªl*>2t\x00142»!I~l\x0019\x0013ïa¾)ÁcvÁ\x0018\x001f_X\x0003ýééÛ«©
ÿ\x001a\x0014j\x0007Ï¶yárþóÉ\x00137Iþ>kÏMg Y®f\x0011«
\x0011bÃ¶@Aþ÷v¹zåê*Í<G\\x000bÄõV³®-&`ªf\x000c%\x0016®\x0001U\x001e\x0003«Á9xkHMlQUfévùf[Ã\x0004¢\x001cXJs\x0002ÖÊÄõ\x001b\x0007õ\x001b¥\x001bÊÌn\x0014Oàâøbvbb"Üèõ_¡£Þ+ê³µ:\x000e\x001a2f
§]R!Ð9
\x0015¬]\x000f8\x0014ö¨&Xtþ-*(âÜÆV]âÊ gBËl-`w :\x0008:5\x001bZhbG6ì(°Q\x0013 :²©ÆCÙ$2WÝdp®PeóAÅËà\x00180s-\x001e3M\x0002l(§ös\x0012Ëâe8®Z*g\x0003[ª¥$¡TFxÉ±tÓ_m³*>tÖHû£$õ\x0012úÍ\x0007Ë\x0005~ÃÉ1\x001c"±hi¨CÇ\x0005ºzjqò%\x001eN»
ä½£9Ïj©ÔOdQdM#hÆ¨rjhjÀ>Æ%S?±EÝ:{Ð4\x001a*är=¢ÚÔy¨\x001b~\x0007\x0013Zø\x001d¸Ayí)ô¬è·<áy<u2\x0006À§ã(3¾A>sÆ17­GØmÃ\x0015Ë1\x0008²²ÛZ5UÝ\x00034ÖÃàÈmØâlªª§·.×ÄÕ\x001c®\x001fäðdL1mØâ¹CBå\x0016§°«\x001aLöc^1\x0019P\x0013[ÔjÌøÜPÂ`+A{dRr,c²-ÉV\x0011ÕÑØH?\x0017\x000bîEéÎSá¿P£ÝWé8=\x0010\x0017Oî}XÏ=®²ÉÏÝ·\x0018q\x0013Ö<}\x0010Ü\x0001^EâÓÓ\x000f¢*°@;8ÊÅòDÏÈOÚâ»\x001cp\x0001Ï°æ`&²·UÍê¦Ìè\x0002ÄP$ùÍ;B38
AIòLéK²DL'8	ð\x0008£Û#æU!©ÓªÎ\x0007_Di$\x0017Éo\x0003÷ò}Ê¬-TÔ=\x001a}´ºtH\:ìKCTyêÿ÷[i`/N,\x0012\x00078Ñ&q!\x0017r|Ç.\x001e2»-> ñ\x0007;¶«0Ób»<¾¢ÌÂ!ûÕ\x001fá·½~øÝãÇû+¹Hôû\x000f CÚY<I(dX÷%Ý,i[©\x001b³V±@þãØjHTé4«C£&¾¨FEÍ\x0018\x0007À¼\x0010hP\x000e\x0001Î)éËb¹©ÏtJM\x0016}þñþ«\x0015¡tNÏIë¥­×O» Zû>ÝÝLÙmaÎw"¨õ\x0005S\x00045ûW¼õû¯-­&h¾ºReéýXÙì¶n%,'³åÙ]ºYuõ¹\x0019ã\x0012}Ý¸w0øÙó@ü½v=ðõ\x0000Ä
9	dJrJS\x0008©AýÅqZbÔÃr;p¿zzýøør­Q¾þíWÔà<çrn`\x0019)û}r¶\x0011°ä\x0006µ0ÖB\x0002\x0011p¦iBÃÎJmÇ \x0011RLhÁ7·ÖçÍ5'Ã7Ü"/\x0001\x001cö\x0014\x001b$\x0001ÚÁ&£g3±½\x001aP¹fÖZR\x001emáØ1ÏªÔ\x001a;ó³§}øøøÕÓ÷×Ú8\x0003ì\x0007ålãj*UØJ-ð÷Ô=¶ªMq]Goÿ
[Qäøõ\x0001´\x0011}8ÉîÜp¥pS\x000c $Åf¬\x000elÞ\x0017ì½Yqo\x000e3Xv\x0014Í©\x0004\x0017qõ÷\x000b-òþùÃ÷ßøýëãËËÃýëâ\x00104¿¹\\x0006-ØnH\x0016·â-¯±Å¡!ò\x001eªªÇ§zJ¶7!á=LCso7¨nô¤³IîxÃ¢\x0000!tf§\x000bhÉð+X\x0013NA«liÊÛªØ|¨ñ4%pÇ½bÆD­o;]ÍV\x000f-©©ÂfÁuÖûl´åÒièdMAÀbé/jáeÒÚ¹ÅÖ²Û¡%\x0003)!tTDJ¯*¡¡6ó|Ù ³¤cau.&
­òô©åb°\x0015b+¸¡î\x0001\x001a«¬\x000e\x001d\x0000Ø¤ÆJIÅ\x0005%RR\x000e.4§§×çkÑSrPt\x0007¿÷\x0014=ù*5Ý&¢÷®@È\x0010\x0000\x0018´3\x0012>ÂûÉge\x0008MÚßs°-\x001fë	]%Df§Y®lU^\x0012iÔª,é*m¦yüEìRïWÝ\x0003úE\x0005?Z\x0018Ñð\x0007v\x0014~ÍJÎaÍÍá¹ÓvÒ\x0018"#\x0013;Kl'©rÿbÐ¡êYfáWAæê¿}¾ÿÄö)¯×`Ï¤>otáeké.Ê\x0019pG·\x000bÌl Ô¾\x000c3S\x000fû\x001aÿ*¹Ð1«rL&UýºO§Kê\x0002Ý\x0004´ÄUÖ\x0018Ê¨å1ì\x001eõ¤Ð\x000e\x001býÏ}â¨/©\x000bôaAÖBÚAÇ\±çª*s®B£\x0017è#\x001diýþ\x00132 MÍÆ$\x001dÀ´©9±\x0002.?\x000føôåïÀR\x0004ÈÄÝ×c`\x0002=9\x0015½LZ¶l½\x0000ÓÏ\x0004Ö
â\x000b°ºì7P\x0011A\/6µçf×Éùö.²®]ëÏD>®;²\x0014Ñ\x0015\x0002¶4\x0001\x001dÃZ1À(£ðWo0ÓÏ}èÕBç,>n\x001c·\x0004í¬ÆÞÊÐHÏ«UÎõ\x0017ò´
Ü2\x0014õå9¯\x0000§Àj¥Eßÿÿ\x0007.«\x0015.Íb«~ñ_\x001a-á\x000e.Ù)Áñ:	V_IpÈI\x000fVî\x0008Ï8u`¥X½»"Þ\x001d»L
V\x001f²ô\x0007pQBRý `äÕë+âõ\x0015X
¦jÂôwjX'â¡=k*b\x0016-\x0003¶X\x000cAæÇGs@'ÕCì1¾U'²éá\x001c|÷ëøãÇ+úbßÈÇa©c?\x0008¯ã«¤é'OêÞÒe<{ÓÎÍ(ê¨;Î¢!ÍwÐ¬+×{ïfr»A\x001fÉm$/Í©XÞYâÆc"h¬íÔ´¶HfÊ-pK\x0001\ÅºëÑá\x0011î\x000cèT\x0016M­
ûè]Æà%\x00115Ò\x0011\x0011[bZt­¬»Õys»
¶Å\x0002;	ìâá5\x000ewàö3í¨¡16M\x0017\x0017Cïhb\x001fzG\x001ddAM!y`JeVØã\x0006²(\x000b\x0003;\x0008ìä`½\x0015a0%Q\x0004Øa¡¥´aG%åß)óÒ\x001d³ZAÊ«½ÅÞ.P\x0013\x001a\x0013ÓZñÙ4C{`·#-J\x0012¥cY\x0008YoêG{}\x0012¦½
\x0019¢i\x0003\x000eÑ4Ï$§c£PS
å}\x001f\x0005Ø(§¿JO§#ø\x001f\x001e¾}x}~øðO\x000f_}¼ý+%ý¤À^\x001fR\x001eóFq\x0015\x0014ÿóF=x_}CC\x0019Ò³W\x0017¶ýÿA\x0007¥¢~_\x0004$Wó"Ø³/\x001b¶ãEãrþ¶²ïõ	Øë3Ø\x0018ãÎýüáùáç+]¹¹ÀÑhLhÌU¼ìÜaa{³"À¢[\x001fQ¤ÆÄxy«\x001fòÖ\x001a\x0018_ ¿@îýúßþíþÓ7\x000f÷WbO\x001e\x001f<l«ùr¤0\x0004k¶*onÜï©_æöe_º/Fçô8\x0014ììib%(úW3]2ÎWó\x0004\x000fM¸Iº 2§\x0012*}\x0003§<Á
¶ì\x0004\x0017lY\x0016£w\V÷~ÿÏ2ÜC©Xcm3\x0019Ú6Ó\x001f\x001f{ }ÿíw÷>==?^©¸´{\x000e%¤2á.\x000cóÝw¶°´\x00104 8ob\½ÑÔ°¯åÇÈ·å®2ô¼:h£­iÓI@lÌ¯\x0018
Ý	e\x000cf"#)Ë#UÉnd\x000fëZ\x0007Ñßô[áëûïî¯5\x0018és\x0012Jà1ÂË<aj¢üR¿ñÍÌµ\x0017a1÷]\x0019k?78êHÍÜcV1\x001dÄz£×8°Å8/$ÙÁUKd¦çûS\x0003v1#¿\x001e\x001eX¯ûW\x000fÏ}9¯\x0013ïU\x001fK¨õrVô§\x001afp;ÁÊû÷ç\x0015lè¼\x0016äh°)´\x001cÝC\x001eT\x0017\x000e
U\x001cIÌ4\x00143\x0006¶çúÀ\x001e\x00122âëi&\x00184\x0015­¢1à?°£\x001e%ï`Ü3\x0015-=­P\x000fVÿê¹AFÖG÷lxvl<é\x0012p\x001bMZÉøÙÃóãËãÃz³1âaDSªoÎ­JÃZwþ¹\x0000úÞ¤\x0003¬n¤Ç\x0004«\x000fK¡7O\x0001}²¨Æq\x0018äauPìAI\x00188Æ\x000c¢Z4«Nd5:Üø>zpaK®xÈÅ\x0004s\x0004=´öÞ¶ÛpÀrBQvB\x001dº &G­V¤Õ4K©Çì?þÏo>ÞúþßÍu8J1\x0006WÙ÷fêp\x0000ZF=\x0019Ñ×­D\x0004\x001c\x0007£Ô\x0017Nqr\x0000
fÈJ;-ªÖd¢FQ´iR>ÆåÓ\x001fN¡l]xyNÔ \x001f¸
TEª!\x0014|Z2{;®è\x001d2Û\x0012lÖ\x001b/Å®Ó¬\x000fm/mÐYBË\x0005.jÑ\x0017xÁE¸ï#\x000cµÕ#+Ïy3ké÷õ-}÷ðüç+~JÕ±KeO&$0l\x0019n\x0016uþÔÄ¥¯bÎU¸ÜUÑÅ\x0000\x0001Êä\x00147GÒ\x0016ÐÒ\x0000°¡· S%ØþWã(Pö£ÿlÝMliv7æBOVL´ZðJ< oÐá
c§×\x000f¿zz|ùðõýçÿúåË÷×\x001aØ\x0008fÔJ\x0008;»¿ÀxÿÊ-S\x0018»¼eT2ûúa%sõCÞ\\x0004+Ïðúãæjã¿>½öu¥D£ g\x001f-\x0016Ý¬c·\x001fÁÎñv1\x001ckÍü$"oñpI2ËUªÊä(5±+«ÎÀïO£*a$\x0013W0l\x0007Qü\x0018Ñi·*KcÏ¶)æÝ°A&?5yfô¥Wi@ÁqMÏÖ4¶*ß~#\x0005¬Lb\x0002Ü@
w¬Æ94ÜpÄ ¨]R\x000b\x0005µËÚ\x001cF^\x0000{ibÁÐ,n7ýíZæ¶RÄØ¢+0lL¢\\x000ceÇ ?k\x0019m&K¿®(ýºækÂç>¥rI­ÕdFeéõÃoû·u¥¢\x0012\x001b"Ë6t«qW\x0012ô\x0013·ã\x000cÜS½á8ÈÊmÏÈ\\x0012ì¢þC¢,\x0012Ç]lG6\x000b,Â´³¦K\x0013Lvè é»³5ÐÇ\x00113¡G=À¡Þ°\x000fÒvÌU¶Ä¸º
}~V/ÅÇeáL¼aW
\x001aaa\x0013\x0017ý[@NsüyµØ$\x0017»IgØÜTgX\x0018OìjøMö\x0008øØû¼ÿ\x0015«zØÃWªÉ\x00075ÞâeF¯úâCóH~WÁ\x001aÅ¨çßñÖ\x0012iÏýË;ÞÅ?ÏñäOý÷°õáõ?{\x0003ú4¾í=~G9
;ý<Ý,¹Þ×Q¤ù_ý_ûB\x001a¸,ÆKð×³Ë\x0005~.ò¦¼#|â\x0006îÈñç"øÏ;rúyÈF\x0008nvvþøãß®%ÁCÚDÊûL8\x0013_*#ºá	´¨RYQV¢\x000fSV%é«gÀ\x0011U\x0012²Ç\x0005È²Y÷Ù eg°ULÛ¬ÿbgh°\x00191\x0008{scéß|g¶@Ü\x0004\x0002q.IOöØ¼6W\x0012¯q-É-\x001dêAØ86óñ¬PÐS{ÎzÐIB\x0007ÙöhN\x0019Ó\x0014§Fïmh]¿ýjU¾¿ïáe4uyÛI@%Þ¬2âéJ?½Xáhó
wlú\x0012P)\x001baÊÖìÉÆ¨'\x001b\x0017Ç±í\x0016ò¡ââ\x0016Z¤´Q;#êU)rWd\x0007\x001cOchÒR\x001fÐ¢ÂÖ/cäv©ÉFÑö¤CÅ)\x0010\x0012ójË¼¹Ý\x0018Û(LLlQ½¨/³rBöM=w\x001c¾W÷-;Á\x001eÉ)£v!9´>éI4ýÕôÝÙ°¥õØeçOô"ðJÁ»hg$\x001b°|Iz¡¦\x000cµL\x0016ÈÀ®\x000e\x000fÃ\x0018g\x0002Kc¡ '\x0004PKÆ\x001a,y$\x0000ö#Ú<»\x0015\x000c°Åòýó×\x000f×®gb\x0015ºÇ$ª{´ºò3Ê\x001dï.Ý®Þn\x001façÊu_9þf½h¢Bö\x001e¤ÔØk\x0019]8úF««m\x0015w×¸	!ª¯kûà÷%¿ä¹Ða\x0005úÀQw¼
vX0âNÂ¸`ã``XÆe¯VùÞÆ\x0008½ß\x0017ßÛ
á
[ð
\Jº\x001d\x001bõ%:6\x000e´¤0dñ\x000cùë
[XÈ:VPTÏ-×¥ÌÕs'[&ub\x0007Qüãñ_QDsUÕXCEã©\x0014G<¬;\x001cÏÍ\x001e}ðÜÜóØTÕ\x0016ârÁr\x0012\x0019ØM`{)æÇ¦
È\x0011!åD6\x0007íÕ¤cM:¶¼6r¿ÝqPÆ}-\x000edæ½·ð_ÿù¿~ýÕÓB±þ1\x00108Þô\x0007
Ç'*\x0012yÐfogRR,Îú¹[0oì¸ypîrÎ\x0015æüj\x000e0F.éÆº#\x001fóxìùì¥t\x00067Vö|F\x0013âéf~\x0012ÆØÃÏ}fcJfB·;´½rÎªNI=ô\x0014z^AFí\x0014Ð=t:û=üX-NBQé©/p\x000eäT ±©LFèQ\x001b>yîÐÇè£Ï2=Í):5D\x0016ì¢:D\x001eäºYµQ;2\x0017\ê0dkZùÄ\x001dÅÇùÖwm×Ê7h¹C$®7PÒ/ÐÏ }µ9pp$Á2ë`"¡4¹Ùb7ZD\x001b6\x000cDØÓ^9ÝsØaHá\x001aÓY\x0013[0 G¶.Ý]Á¶Y?\x001ab;ZLñ5-Mé\x0002\x0018¤gÕ-9âÊï|]`\o\x0007.æÙ£-k¿áÆïÏ¬+(%}\x0005½|øåW÷_=^krHa§\x001f8¹ZÀ,¹'ïEkð´RBVÏã@!79*¶Tµ/ìv
6ÿ\x000e\x0012:aç\x0000Õä;´vÉ\x001d¬\x0018cvpBG	
®°±"®ReOÃNún¸Ià\x00169ußÔRdÄn¡Xdþ¬#£×\x000føþþëki¼¸á0;N](Ñ\x0019ô	ÓÆ»»UXÌÓ)BÍ\x0005kï=°ÖF)¡GP¨Õä®g\x0019+3ÄØ Å\x0005\x0012R\x0004l\x0014Vf>\x0007L\x0007x\x000eóm>Ç|
µäTU\x001eÓï=tÿ«ÅÞ\x001bt\x0012Ð-\x0000.>rRVÂ5¯Ô¹@yÊµx´8:pÀ\x0007n\x0004\x000bWL¢}5mÀâjU¬¢/Õ¦ôtûÎöÝ1åÝ±Øâo~\x001e£ú½Â\x0013\x0005ÀmIC´NVÖ³ØqOl)IZ\x0013(¨ç*@Þa\x0005)\x000f}\x000cÃze\x0016Wu&`ñ¥s¯ÍÇ¬ªS36z/\x0003;ð%ÃpÜôÈU{ßPXÒñÈÁí
;Jlñ"ý¿QÀC¥5\x0018µâ	,ÛÜ@\x0005/y`Ttl´Fc+U?2ó\x0015¶à)±J\x0000x!U\lÊ\x0011÷kÃ#Ûèìä9Õz|»ZêåÂT\x001aTÀõt(VÙºh\x001b¶Ø%£ÝHUºKA§[3äû~ENL9þ®_\x0017ßÜ?ýÃyz¾R\x000b¿maýÑrsq
qX)J\=«·kh.b®SkÙ\x0011äæ,t\x0014î»ù\x000eUx×¬Û`6Ú7äðsÏö
9þ\äs£}C}RwMï}Â\x0003½\x001f(áØ3=KMÁ4ÍýýSÃ//÷_])!H\x001eºþ="¤KFÀ2Q@égÃ]¾\x001d×Íæ»:
\x001eûJD D]B@Ò\x0018\x001bAÊý`Z´}\x0010ÒÆ"	 UNµõ~N®1\x000fåÕ<\x0014K%qnÆ\x000e!¥@\x001a{dÚçzìÝÄc^N	\x0005ý0û_­öÅlã\x0019=-KD0kØ±Q¿¸iØCÇ"øOlé\x0002>"e\x000câH\x001fT L<Õ:"±\x00156Iìë\x001dAç§ccÕ$ÇaÜ×r]\x0004¶Ô$)c\x001e§\x00016 gÖO6ô¬OÆ\x0018\x001f.Öî«X\x001b29Ò>ÛÂv ¬Ò/Õ[RÎì\x0013ÁPþu*\x001d+	,\x001a}qkpê¾.£6fÄ\x0013WÄ¥È²[CB"\x001eQÆ2dûo¸2Ô©r \x0008kb=·¬8&óÆÞv°ãïóÍ½°È=&¶X\x0006ªY\x001d;+\x0002º)ÅÁë3âá-5ÿ"\x0012¨\x0005Ì²8h\x0016\x0019ª	-[.\x00109%<
ÈÑñ,Ü\x0008'v\x0010¹:k
\x0002¶Ì\x000f^êhRE¸:)ÀÌ¾{xþúõZì»äTH~éQ5GwFåv_¿]9÷¨"©\x001eUcy¨¹0&ôÄæiè+;jÌçæFÄµ\x001b$:¬º·k*%ÃQ\x0019×Â\x0017ä\x000cÈTá\x0013r\x0004ìÌºÙ8ÝK;²\x0010¯í±çd-Ê\x001ca12\x0008§\x000fôÉhG\x0016Tïä*c3¹ñl.>ò`"¤÷w`¡jÜ¦c~TasGÖæ½ÓÑÎ £1CÍJl[Õ±D¬på\x000b¢yÙó÷9m- %ÑÿÛÑ×8÷E7h¡S\x001aTLN®áõÐ>¬y¹9\x0010q®\x001doÐ	VC:XVeÀÌ\x0005eX:Y£\x001eOº8`íÔOþ ¤q\x0002'·\x0012m3
Z\x0016C¯Ðê\x0014´v\x000c¨còù\x001cëoÐE^èËZ±\x000cØ¯Ë;¤2áº9¡\x0005E'"e5\x0003µ\x0003;t\x0001>
_¯ãsYA7	í°\x0008\x0013ñ"f^*B8~ùø²<ó¾à?¼ü\x0005ÙI¯±ä\x001dÞÆ1©R 7½Zªðîì×+ÉD
¤ØmnÞ&Ö:\x0015Ú¼}ßÕÛyQýÔ\x0008·"Ù¿ÿ\x000c\x0007ö$)xLS\x001d¥FÞ$\x001elÐÒ9Ó¡»eh'hUwÅÕS\x0007ùÔ\x0011JÊ:I¢Vñ,óu1Zq6¡¡ZÐ\x0002\x001a/Ðése0É&r\x0016ëAE\x0017«Ñí\x0013É\x00019p¦\x0016×\x000e-\x001e:{uJhýÀ\x000e¨XR\x001eù¿AõÈE"g(ú"Åúd=N[qv\x0018«¯§ªUN^_FFKÒRBß_×M%DÈâç\x000c½\x001e?¥¿´»p»vøO¤ÆSÄT\x001cRH¬ì\x000cî!! !gqÎî<nÐÂü7$Hð|\x0003¯OFßöÜ\x0016vw¤\x000f<DÆ«ïµ%T2.·Ã¸\x001f²"bA\x0012ð\x0018:cúS4?ª
º\x0008è\x001a\x0001: N4ÿÕøÔiÔ\x0002­ÑT\x0007áÁ°b\x00019\x000eÂ9\x0004Zô9L÷i£6:EmÔsÁR.µkj©Zj\x0017¿Â¯\x0011\x001dù\x000cÆµv
+á\x0014\x0016ÂÙ\x001bö¡¼ä©eÄ.øÜÕ\x000c\x0015
¾á<=±ót?ÑqMÔ °g×d\o3 ñ¦ZÅoï\x001f>}ºÖtOô@á`¡±uaFW"NBÚíÈ\x0013\x000bQ§óeå=2z¸á-¿«æÑ\x000eÊ©*Uß²9Ú7¬W7¬\x001b½Í\x000b.ÞV=|\x0000¯­¾ÒqÅCõuÑ\x0004Z¬ýïm$+l!r\x001aH7·«]4Ï¥¼\x0018ÙZ%\x0002[\x001aG
+ªaLMwCÃ\x0005'>©_ZÒîs\x0005\x001d8¹ojD\x0006ÙôÿþÃÃóó¬?\x000e\x0003ª+UÂ'y\x0008CÿÒêÂ>½CebÜ£^Dº¼ø!o.ñb\x000bÉ~Ö=½~ðçx~|xýË;ª\x0010L»èöòäæçwzÖ~³ßNg¡÷zNUúÊaªâ\x0003ÛëV*\x001ew\x001däë¾hÈP\x000cäcx- å»<'\x0007G'jÎ·Îï:HÊ\x0004ßkÿtÿï¯\x001fù?»R\x0005:+ÿ°\x0014.\x001aLl¶\x0005>¤íîvc\x0012övª\x0007\x0006w*Aç\x0006%Ì\x001e8&¨\x0007VÊÛ<ÁOåÀ ¨\x0018S\x0019úèÙ§Øò\x0000EÌ\x0002}ÝÑ\x00022Ë\x001b´,\x0007&Ðçco6,¬¨µ@½&	
M¸Qâ\x00044öäÚ&ï´®²j\x001f®êV\x0011Ú'6?èuÆE<±½\\x0011Â·)°6
¬\x0008a\x000cZ5\x0001ÞÏÔ_h~í4)þüþùñZ\x000e×\x0019\x001e\b¾´u,OÇ[\x001aÖAÜúû\x0010ôWUâ]Áþ\x0014l"å6åcÏ\x0003B\x001b®0%,Y\x000bÆ$ØBM÷H¦\Ã
YP\ºó¢LGi4Ø\x0004UHy_Ñ û:\x001br\x0011ÈuÜ~*\x001bî\x0002YyÑ¨JÛ/\x001b²h¿é\x0016xYz'çVZv(3Ë\x001dU»ý2¡¡?\x001ap¡U¥:»¤«ÍîÀlÐboT\x0007~\x0002=>Wv]Ar4º$A\x000fî¶\x0004l§ú
Ù)¿þ+G"º&ùÐInèÔs\Ü\x001e®©â0¢Õ&±§k¾\x0013¡>Ç\x001cà\x0015½Sº)Â¹Z\x0010y7\x000b¢îìê¯
ËE³Cnemw¢jÙs¬\x000c[O%Uk\x001dÞ\x000c,S#½«tÆ\x0007us´ýWÐÒ.ÕK[f>]\x000bìjuó/ÚS#\x0013Zª8 \x0014$r\x0012*®ó¨\x000eÇÕ'\x001e\x001b\x001cK\x0000«hãY×i\x001c¥FwnBKÑ\x0014W°{àñ¦Ï¡ªc©©ü,Ryçñ
n­Ü\x00039F,ñ©ü|¿ÜÑ_ÜÃö Ùâê\x001f&Èßø¢:\x0013dúóX-®\x000f=~óÔïÉ+]õµ9\x0018à°ãâ\x001c\x0003´¹Ð\x001ao\x0017@ÛcC°UÔ\x0007È>ôßmïÚ¥SûQúWÃ4ù|Üo¬¹!ª+¡¨é\x0016
J·\ÍNì\x0006-:±Ñ\x0001Õ^\x0011\x000c{Ê1»íYÀ¸ß¬q`{9¬Qù<\x00117VOøØÅ\x001cAl*·\x001bÛóùéñ/|üøå6)×°
\x001f|9Ôèû!\x0011EâØ³ïª÷b°\x001c\x001a²\x001cz¾AP²44õê\x0007
öÿ\x00166=Ôi7\x0014[Ä\x0012)®ªë'4ú¥PYP\x0011\x001afL\\x0002t\x0007nÄÆqÇÍ\x0010Í\x000478\x001fæ¬óLDù¡
æ°§gFª£êÛjrx`\x001f¾=:\x0011À\x0014tÝ\x0012Ç^ûÅmm
X\Xìp!ß¡àr¥µá\x000bt£n8²lÀRF@õ¬D\x0015Ñ©*ìÙ\x001cYí\x000e/ËÚAÚuì¢«Ï¤>¾Ùõ³\x0006í\x0007¶é\x000f\x0015v\x001e÷x#`cS'x¿ß°+ã¥¤\x001auâsã\x0019\x0016¢%Qh(yÜøãÓÿï÷×\x0013U-È/R\x0014ÑûuowÃ.\x0004\x000c%A\x001c,ÕúdÙé¯Õgx\x0019ý.J6Mz"o5\x0012¨Z5¦QòYÅ °ÿû+ùÃc\x0017\x0003\x0004õ¡°4\x0006\x001e-¹?\x001cYehì` \x001a\x0011o	ýÔßm\x001c\x0015¤\x000chÁ{i%a]Ö7\x001c´~©×Vp vhÉºm\x000btT=jªêÒ¢\x00115±E#*@Sj¤\x0008ÇyôfÑØR¯-Ã\x0018Có<ÆÆ9Í0
L¾ô-wI\x0012Ý3«Äf_\x0013;$Èâ	È ÖØ)ØhÍv$Q\x0006ü\x001fß~wÿò2Ã¯ßÿø·Ç¯\x001fú\x0017}µØ\x000b)\x000e1ì\x001e\x0007Ü[wÇ\x0014k¬\&xgô7c÷$¬Ap¨!5òc=µH\x0013r\x001e\x0005iV
6háØÔú\x0018Ðð²\x0012U\x0018
3óôÐÒ´Ç#tRjAcÄ¡$h0\x00139Cx\x0016mJl24¯új#_2Äå&t]u£ûÑëQÐY.NaEc\x0016cB7	\x0010º©`4c\x001d\x000c\x0017
é
i\x0008F\x001b\x0015µC¢ê4\x000eòmÐ²Wdù$¶\x00014ÔN:n5b\x0018
"\x000f\x0013ÏïÿüÐ?+\x001d\x0004¾ªR-¿ÖQ@$\x001a\x0008|{ïÂí\x0002ÓÈè\x0016\x00075ëk\x0006aPy²\\x000111VÆLQ\x0008*»ã(Eì 0È«ÔÜaw2\x0017w\x0016àVÐÂ³BÔ¡\x0015Ý«¶Ã\x000bk@\x001b£í\á²È\x0012¿¹½3wêA¢Ü?9´\x000f\x0016ßâ+`ÑæQ¼~OûÇ`Êº¤¾F_\x00023Ã\x001f\x001f{1ÿvfîg(\x0016\x000ePi¾á$¯qW\x0007Þo¬."ö$!zK\x000eÁ}\x0012à\x0005¸½\^W6\x0016äÏ=$¶N ²´]_>|öÄ\x000e\x0007ÿçûo>]i\x0012\x0015O@tx`´ÝÊ·ÿçÜ\x001f>®sº­:¢]µ4hweßVUæ\x0010ÑeT#Ï=[\x0003÷\x0012sµ#Ð}D \x001d¤vZ\x001c¶j¢²ÎvU\x0001°Ë\x001eª1u=°ëÑãÊ
dûX¿\x0013»_xH¤æ\x0001hÆ>g\x001bö1'Ñ!­'e%Õ¼=b\x0017BÒøB@\x001bã\x001eî?ý\x001fý»Ö±G5\x001d©/\x001f¿Dn']Rj#b¿8CJ·ST·wê¹ÊCÓø¨òPÔ²8Á\x0016r	&¼L^Äbø\x0000#FJ.¢®A\x0015\x001ecyÓà\x0019\x0006C{``\x00071ø½dÐÐ\x001e#\x0013µ\x001cÔ]Æî+44l
ªôÄ\x0016/ÙI5Oâò=cT¡k0°\x0003Yn¯ÖÓk?N\x001f?=^ë0m¥â@!.ìá)ªY&f7ÜíÑãððS\4Ü6-$\x0014¹\x001cV6JEË»â\x001aa\x001baT·i!\x0001íA¯U%SÊ-6£Ö\x0013ÏCÂ\x001bt\x0014Ð¢öÿ\x0005\x0018\x0007ãØh\x0005«\x0001'Æí ô@ÿ§%\x001e´Áx\x001eäÝ«@ÆýRm\x000fF#>ô\x0010¶*Fd`\x00179\x0007`Ð£8§F¦\x000b*¿û2ìnªÁC\x0018ØUÔ\x0000\x001cØ¥BºÕ\p0Ë·A\x001b÷$,{\x0011Á­>¢7?À\x0001n4J&¸à\x0005\x000b¤jvºTì6Ç)7k(Nha±04)ìÂkÇmÀWë¸qÖÔ\x0016¯rüÁQÄ\x0004%xÊÉºG÷zßß\x001c\x0010³_\x0017mlâJýñPQ/¶xáJbµ_{î.ßnþÓÌZ\x000cQ7?æ¨[¨ø\x000f\x0007c\x0001ù<4{ZhâJaá\x0000K_\x001e¯Î´²ØR]Te=N\x000b1¶<\x000b-ý\x001aÑ¦\x00130CÐÄ\x0006\x001aÆl_ýééÓË_¿\É\x001fE\x0013å0hó+ào5_>]þà\x0006÷ç]Í\x0005MÙÈ\x0001rù3Þ\\x0002«Ï¡\x000eûãÝ|üt¥\x001aV¿Ô¡\x0008H5¦=\x0018\x000fÁñùÎQÆPÎíBE8Q\x001aGõ!©26CÌ(0]Ý¸\x0013\x0011ê\x000fìtú\x0001gÅKMñQ\x000e,àÊè´4cn`·ã&ë/@N\x0000\x001cq8úüòJÙÜìEñBgÇ¥¦\x0016kÈX?ú
2¡T¶y%Khl{\x0001%2h\x0017uä\x0006Ô:b3LcØ?0æûk5¢û{Çö]q\x001fa©\x000bé\x0015âËdÄ½«³¨\x0013\x0006/`¼\x0011ñ2\x0016¿äÍU°\x0014&Ì÷ñ§ç??¼>^ÉAý²Õ@Aû\x0015×wä Ûí$­n¨¶\x0018Q2\x001a35*"¯\x0004\x000fJ×U	8Ñ¯\x001eÐRÀyXfT\x0001­Ì\RË
ÛÒÉ"ßÌç³?ÝyÿéZTË~¢Wlíöüc'\x0010K\x0006\x0018¬gE74×[|~VMÅëÊâ¼¹\x0008ÖØØI»°\x0007g\x000fÏ_??^k:0;$§\wãnÇÚ|ùØWý\x0011ïÂíJÈf`Nóû)Æ7K\x0017
'%Õ¶L\x0005$Îû\x0012¾å4¶A\x000bÒXÉPA`P ¸$äºjÍw9Eæ¨Bi4Ñ-'Ô¢)É\x001ajæ0ýúÛçûO\x000f×ºVÙ=§a]ÝÅ\x0007Û7ÌnëB\x001bk1\x000eqãNU~À 
Çb@íQ\x000f|Õ±Ì)r"èÕ\x001cOp\x001e¡\x001bVæ¥©>´A\x0004ªÔñé¯Ê\\x0005¥\x0019ú[LóMh9Í·x¯oî	û\x0003Ø°IÞjQ\x0000k«&FcÇ`\x001al°¢èçÇGF+sm¤\x0010ëÂÒrC\x0016cá>EXç ¼àRVÅÕ6­8-vª\x0007v*ßØ
ZMjtl§ê3³`H´5c\x001eÑ\x0000\x0014\x0011"Ä\x000e	ÇéRÿYV	ª/ª¾üþ?®«/ð$ÑûÃ
\x000e-[¼©)¯=ãl(>4}¾øòDÊð-©Y¹\x0016/y8üI­Ã£+\x0013j\x001eF?6!_5¡õÄbñß|q®ÿÀ\x0006\x001b±\x0006ZLàÑî«ç<´â2Mà O\x0017ÐÂ©øÄ\x000eº!Ï\x0014{µÐð5%¨r×XÆwØ£L#òëYýùîþ¯ÿü_¿|þþñåþÓýêr\x0004kb\x0014ôÇNF
G\x001d¢Ùc1qÿ¾*A\x00065¨\x0016$õh\x001cx±lí\x0006¬#_ðu÷Øka¶a\x001fÚm~hÙ\x001f<ä1E\x0000ºGÚÓeÁZÅ-5ý2\x000cbõÁt§\x0011Pýesè¦s\x001bp\x0003\x000eâ¡3ìÑ\Ð4ÚSHðÅöM:±W\x000f-(^ÜÄþËØúbl\l\x001f³q¡P2È|¯\x001f~ÿøñO×òq\x0018¾è=³ºö¥&\x001dj\x0010\x0006¡Æ:ü)ÞUÕÁ\x0018òéË¦|b¹d>,Ü Iò9Â
´Agzì\x0004\x001eKM
9\x0012\x00036ÆZÊðÁýa"ÕùEÑáw\x000fÏ\x001f¯5ÜÙ22eñÙÃÄ\x001fGë\x001fÆûí4ÆN1¬\x001dL\x0001%Waª¹À!ß3þfËèÑ?ã¢\x0006ÕF	ö¶\x0010\x001dÞ¡E¯9>Kªc«\x0006;Óôw3¶æDÎê¡Ô}l§F5 f¹ÉôÌ:~wÿ\x001f\x000fWª{f>íeÀ\x000f\x0016Ïä¦qC;_J\x0000¥öÕJ·ã\x0012/('\x0006Ù ðí¾Õû\x000fñ
\x000eÌtXIv·,²'vØ\x0011°\x0003¦Ù9Bì!Ä\x0018¢êN@{© ××ß«Çö­%\x001c! í\x00056\x0011<vD&Df;\x001dµ/1Æ1±IbË`§ÔÊÒ8\x0017ÀÎâc\x0004Í\x0013;HlÉ\x0014ëØõË]F\x0012\x0011	\x001d\x0005vpÐRÛ\x0004d\x0004vÅ5©;l´ë&öÑ®ëÿsäÒ¼ÂV#n¦Q6âýx¿\x0004O]ÐL2S¡í@ycÐÜÄ\x0016BsÜ|Î=
¡C\x000eHõ	TÃ\x0010^]}:E|:\x0011öIuÊ7\x0010»eK!ØçÏ\x001f?½<]©_Í^}(MPòÎ\x001ep}½A06\x0013ëwu\x001bNJ'	\x0012dÇ \x0011%dGQx÷Éj4\x0002%OØ®Ðá\x0012\x0011Þ´P¬l6;+hQó*.ÀS3\x001e ±DÉÉ©ß 
Y.\x0008\x001d\x0003*ª+X¶/d\x0004=·;W¦þõõããwW\x000b/kFnÏG|éY¦NdZµÞ°¼\x001a\x000e4Æ?#ÔYÛ\x001dèu9Ë­YÆ©¶ó\x0006+Z3¾R®\x000e#5n]\x0002r*\x000b\x0003¨	-"W_Ê¨5¦*èbõh+Ùz<;²|hÐQÉðöL
×¢ÄÅÀáÄÍøÄ@ìLpthÔÖíg\x000býìÐò=.\x0006*´ªÖquâ\x0016ùÈ¸8À«\x0001Å.¿]P«G.øÈ¢°R\ÁÏ¿§ä¸\x001aÎMí_ÎêêNm{úþñååáÛOßøçÇa
ùtP¾_¦B^ìÑ]Ú±K<±zlzo.ñúÜ÷Ã±À~Ë=DY\x000evQO©`F \x0006g*Øí¸\x0007ß©/<Z\x0018\x0017Í1úY\x0013\x0015tµ¾¨\x001dZøLD)Ùì\x0011»ð9âÔÄd»>¨\x000b²X\x000cp¡\x001dÈøÐé`¥Od«CKÑL1¹1û5÷i¯5³êP¾ÿµ\x0017Ï1'y)òÆ\ç,û{êñ\x001bõ±þÁ>êr497ÕoJ\x001dÒxÕFAs>
®yFÏ!ÐCÎ²(È8\x0007Î\x0015^Îª\x000eëp,¨\x0019¹àò9Âù§§OC`øjú\x0007É§«T/ò-¥ï!áÞ\x001b(ÞPEzÑ(°"ZE:\x0003S;\x00113¶@¦§¢îmO$«ymÐâ6ËUÎA¥à2Ll ÈìhNüoÐbâW_²¿Hé\x0014ôí\x0008Õ®\x001a\x001c­H(YPGÉ¸\x0008"Ã\x001dð³ª1OìhÜÝ\x00046\x0004hE\x0013\x0014Xy\ÎØ>Û»\x000e
õ¾=î¯U?\x00069wOÞ·Ë0NËwÂ½§2Âý[5Kú	w;¯\x0019ÞíÎÁ^\x000f²\x001dÆq9ª6á\x0014ð34²¼q»Ñè\x0005Zå÷«\x0013834}\x0018R×\x0006ÕÔ\x0000Ð\x0001GÃú{êÅ9ûÐß åU-\x0000­ª,^\x0019\x0010zÎ´M7è(\x0015j%nR¥i\x000f:î\x001d·V;R4·¡+p*¦£'
\x000b\x0015§tY¬W¦%;Æ±-ê!5\x001b_ÍBÑo^\x001fï¿¾Z2\x001e¯Oj\x0015s9êéÉ%÷þæ\x001a±òª("`³æª*R ¼ë2\x0015;IÜ \x0005Ç¨\x0014hsC\x0006¾TeÆK»°yÐ\x0014QªÃÚö\x00012[nÈ,\c&´$?÷K\x0018Z@5&|\x0002vñ\x000b×
ÛKl`8º¦E±\x0001y"F	Ê\x001aéùðÇÇûW¤_ö§q\x0016V\x000eÛ~G­G\x0013\x0013µ»rCnyEYÊi#Î9^Fåxá(\x0008p\x000f\x000féuÔï_9\x001aMä,³L\x0013ó8<%eGd\x0001:N
uã"\x0019ØgT,ÀNx0W_À;ºß#n!_±a'\x001d¥»D^Ia·Ï~³EcØE`ç\x0006«qÊ¸\x0012JV2áÝÛ\x001bv\x0015Ø0
Ñ×\x0004Û_Ðü\x0014"«¢ÈØtÜl\x0017\x0001kB
£T3nþä\x0006uÚ\x0019ô\x0013¦_}üøúíÃÏ\x001f¿»ÖgÛ
Zöpþr_%*»tà¾ÜBdPÎ\x0004d§-¢K\x0002ÍCj\x000e«=7À,Â\x000fÙVsë´sqIàQJÐþ@ÛóÜÌ\x0012Ï\x000e-¯Ã$¿D¡þ=hÛItC.\x000cýÁe@u{îÇØ\x0015\x0005w²nÁ£,\x0011)RE\x000f;\x0010:ÁD:\x0007\x0013D \x001brAbü(CXýË²ïÀÎY`GùÜ±8dM¶~tAXGuÔ¾Ë
»HìC>²Ö	,\x000fÀn8ð4CMc\x00007¡¦¼|q\x0016¤/\x001fvCEùþ¯\x0011PC\x0017`\x0003>Þb\x0002\x000e»ºcã\x0007ÃÇ\x001ec¯¶u\x0013Ûzq¨¼y Xlñ¥{ù¥Ç"óÈÈ2\x0018@SW\x0012óÚ ì6cÖ``7yÿ7Yâ\x000buã0\x001e·´p¯\x001cd¶85\x001e1#1Á\x0019\x000eîÄwp5ÙáRÎ\x0008>-1É°'¯Äôb\x0008¬Y¹¬"¸¥MGd\x0018ùq\x0006õp%Ç£È,t_\x001aÞq\x001b%r³>Ûë5=ó¸\x001dUnA4f·©¨UÒýø\x001dPwr\x0011fVF¸²Hsªò
Ù­\x000b®R
v1fµ¶V²\x0010LK÷ßõÕûæZ
P\x001a)ÿú}Ü¶æ\x0004ÍqcA½§~ÑK
è0Î\x001cä²¡¨ù!W_\x001bá+\x0019½ðMâ¬È!Á$/\x0001«]IQ)¾fO\x000bÆÏÀ\x0016dü¤\x0014½UòmeMVºÌMtÿüøÕÓëöP\x00059ßFEcû\x0015\x000eFN«ëvPNÉ .ZcÕ°²ÐWúø\x00159&G4 ã\x0010ÿÕ4uØ[÷Ì	y°\x0002î\x0003ª	±*K'3Ã\x001d\x000el/M.:6\x0016.+â\x0011ÛÇvù-\x0016ÄKÕ¾&\x0019\x001ep=FØ¤Z&¤Zª\x000f*§ÜðjÊ¯Mçrc~h@\x001fÂöN|k\x00073®¡h=qÀMN*ýÇÉAáÕ\x0002l?^¡¡
µcË3  6óª
®Í­,åÀ\x0016éqÂ9ÂXòé¹\x0001CMáWØYb\x0007\x0019üåPÁVJÃq-NWVLÈ¤ÎÅLÒæ.\x00075\x0019×E÷*Ó'¾\x0018åÛ\x0005p\x0000»ç\x0008ð.K\x001ccfÕb2v\x0015eB0\x0013\x001a¨`´í¨\x0000A¦§z\x0016­Z,Ë\x000f=½~|øáùJ':O«Ã8H?§.ÒÖ®\x0007©r \»a\°\x001a1¾®ªEÌ+ÐM\x0002L`\x0011âH\x0008Ñ*\x0019ØApÎFö}d\x0011Ý&­4RtÀé»Ö\x001a<°O=Ðÿõ\x000fßÜ_)Ð	«âë\x001e\x0002²õyº\x0007;½§ã
yW|%ãºRæ»ü;¢(àþQ1ºápÍæ6D\x0018\x0010p3ßu\x0002Z
½\x0017fxihµ¼Á¶ôÊ×¡ÀUòL	Eùµ\x0005{èo\x0002¡?Ö°C\x0007Á¡QPdÍ\x0001Eøög¶	JüæáùÛk\x0019\x0005Å±#<¦!6\x001eEßB
=¼ê»I5ý -¡j>HEÁ«ïy4WõäÇØ7\x000c'v\x0013Ø\x0019Èº£/ 3ÑXQ!¦£¹2î"\x00030vK©8R\x0018ðí)To\x0017\x00187léåAbAöß"ÅÂ\x0008Ó\x0013Ö\x001e6`Á¾ñ@)EÍ 5'h_dJ¯Ï\x001f>½üø·ë
+ú®ºI¸\x0013\x001e¼t(æ9ÝLisu	^tPÏIÜÞåIÓM|Qk\x0010ÍyC&ìÀ\x000e9fm¤öýv7HEýåýâ¤¨úòá³??\M\x0008+4jYåòé¿\x001e\x0017Ô;4\x001fX¼ðÝÍÞ\x001bÎw%@±­ÿ(ó¤ªjuPCÅ\x001cW\x0006]¡æ\x0005tÍ	\x0001l½Ôpðªõ\x0014ýe'÷ü|nÐB
¶P\x0012|\x001eÄQ<}¯VÄ\x0000ö²\x0015Ñ@»9QÃN\x0018aähÄt\x0016"Ð$T8Jíñ\x001e(èÎOÂ~\x0017,2)Esîþ³?ÝûÝË,DþÇZ¹âdÏeq=Ç=\x0018\x000bäÃ
©:cÎ	¤æ\x000e+42Ë»wE-9à
\x000cqd\x0008OLì*±I\x0016zÈ£ôR®\x0019£¨\Õè.pOÛÏ__ozOÅsLIÚ7mÏEV\ßÃ7¶9ë»nXnîYbÃÖ¨$7Åôû~\x0007Es¾Æ)K~yAõ*òàìÿH\x0008:¤å¬Bëõ4+\x000e'Pr\x0019q)Å©ÙÔ©Ù\x001côâÇd\x0001>²¢¦Å¡eH¡Ll\x0012,¯\x001aH\x0000«)±¨úÎÑ$
VÔyýð»ÿxøt%ÿÚÓ\k»"G\x0019EJéÄ\x001eÇÑ{Ó¿³*À\x00059XmWõÝ/MñL¬\x0001ª§¹÷NhÐ0îÉJ(\·ç\x0019gHö`\x001d\x0015õuÆÍböÊõ¢\x00156÷\x001ckM\x0017õF^M^Y·ªäæl5 ]×Ï$\x0000)@Ð×#b\x001cÂ5v-,³µ\x000e§\x001b¶H$C`Û`¶X\x0016¤\x0016¤¬°^ÙÀ7§´FÛÁ1ôï6\ÁZ4½\x0017¤Äû°©?E\y\x0002C+#f\x001a#ñ²\x0011þ\x001flb\x001c,T\x0004³ùd£ôúü0c¾¾÷ÑénË.àîqp2s¡ÔûÒÐ5"ÂìÛ ¤µ\x0016?äÍE0"¬\x000bV¯\x001f~õôòï¯\x000f×ÑPc¥#üÆýp8\x0007bÑ41üPo(N°d
BRV3pÀ\x001f/\x0015T9cKwô 7ê\x0006\x001f)#ù¶Cç£'\x0001óÕpr³¬÷úÉbTgúîÿÇã§+½èêqHÉöqetå\x0014ßß6Þ\x0006*ÜòÏ\x0008ø3Ô\x000c@E\x0017wÇ\x0002\x000f®¼ö\x0012\x001a\x0006º£juhUôáä×xÑ\x0016\x000bªÑ¯ÿöo\x000f\x001fþøðéJ_ueÑ7yºø°Ë»Ú2	ÇçA©Ï·#æÚC³Æ\x001b)8äÔ\x0016éä8\x00044½éK`«nÈ¢íÙ6µB±@\x0010\x0016 \x0018õS`Ð`¸NhA\x001eoANfuhÔ\x0005¨Á!ÁÁsØhcjî¬ðýæÇ¿}|üêq»®ûùñÃ§ku4Ø\x0016
\x0003ù!×0ÉëþY°ÝÁ{k¶\x0006ý¨¼J¡Á\x0010a0\x0016ÕÐpWÚò\x0014°6\x0002øMRk°4(éÌ}\x00031b\x001d§\x0012Y-\x001a1\x001bÙújËêÄ«y`[Ý$6°±9 Æ»-\x0015d¡\x0015«óàÙýç®Ûý\x000f×2Ea\x0002hM§ÃÎüC1ÿi\x000c\x0004ÞnÈuÙv8¿¦=P\x001f"{ÿ±Öq\x0011b\d>\x0013ûèÛöëLt\x001e\x0018\x001b{L}_\x0015m	i3gÅ~ÿø%G4×âyÄ\x00004<\x001ao;áÐËh¾Þ2u°_´¡¥5GâÅØzsR\x001a¡\x0017Q¿!\x000eöç\9+fÌ\x0004\x000eì,Â\x001cX Tûu¡\x0007àT-µtÛä?è¾}¯TaïÇ	z'Jé2]eÆ\x0002\x001a·s]ûÉÊ§¾
½hH³\x0006èù\x0017\x001c)è;åûÅ\x0014ìºÑ:¢
¡£R7*\x0019®\x001d\x0016ô/vqgB\x000bÑ\x0006WÐî!«2,N³.í_mKÀì¥bkaF"LAçÑ\x0015\x001eEC~üþÃïï¿}üñ_ËT²e¥oRs»TLÇù)HÖ)¿¿V·Á\x0014åÔFÛ§RïÔÀ?NÕZ\x0017µÇ¨kýU\x0002ô¦|xÔÛ\x001bX0åÝJ¨\x0016ÈãúÈëÇ§¯®Déá\x0016ÎíVw\x0005S4\x001c+ßS&eÍ&EU\x0017oÍà\x0012F§}Ù»Ù¤Û\x0018cIQï\x001eÔvÜä\x0001dr\x000e+4iÆ+è$[V"\x0017ç.=Á#«ý`ÅÒtà`
+_¿¾V¸a\x001b÷°úP\x001eJR
!ò@Þ»«º\x0018bWÕLRr\¥ÿ\x000e§´p\x0012N)ºIU4Þ-mK\x0016À\x0004\x001c³
Ò+lN`
Ä&ß\x0005?ß?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x001cäRm.UÏ%xn4÷\x001aÀØ½jZ -\x0002Óm0]
¦CöâÉù\x0001R]\x001aZ\x0011isj.®E&AT)K\x0014\x0017,FÖkåjëûb0Û\x0006³Õ`Væ~I\x0008\x0016o\x0006WLqB\x0007ìdRV\x0004æÚ`®\x001aÌäsì\x0014.\x001e\x00060íyÅº\x001c2E`¾
æ«Á@Äk^1\x0012t\x0016ÆaÔÅl\x001cXhz0Ã8\x0017Øå\x0007`\x000f¿èò&\x0014Å6X¬\x0006ÃfvÄ\x0015óÌ»¤\x0015ÆÆâì0LJ¸\x0016ÙUIºZ0Eñ\x001bòpPò,j×l2\0¹,ö«å¾\x00121ÑV*\x0002ã&%Vç2\x0015-	~Y-ù¶l\x0002ãEGdZ69]6H\x0011Ù¼õ\x0002#RwzL*\x0014l¾ L¯c)&[º²þbâÜ/&T©\x001e¸:\x0006ÀôÈc¦Î¿ª>ÿÒóÜ\x0013ìbÁÇ\x000c½£ò(Ó©lY¿¨W0¼âQi<ÿ.	¶Å\x0019¹jIÁPÕ\x001a²¹ÍuÚLÍ©*Ñ&cmä{©4\x000cU¯bxÉâ\x001fÇ,\x0006Oâ¿É¡RéJÉT\x000cU­c(Ðb=§eäÂHÒL5ÇìQ*M)ÙÌPõ2Ã\x001bfÖs-?\x001c³Æg&âØ«¹¤d¨z-\x0003}³6f©·\x001ecñù\éZ
¶$ÌT½0Ãà\x0004f¸\x0000+X\x00179³æQuX)Ø¡Fh\x0019&å´"\x0011»$Ë<\x0007z0\x001e;\x000eL/IY]/eC£ÉZ£w=K^±0òÁÔK2V×ËØ!¢9a¸b4iÆ£êQK¦äÕ«äªÕ{3}\x0018\x001a)\x0010@úSKp«¹®C
®À}å\'\x0007ý­\x0019LµÁT=\x0018N\x0007ËQu-
g&¬Þ#ÉÐt\x001bM×£9Eë\x0002¶\x0004¤ú>Á\x0005\x000cVØGå9Åh¦fêÑm&
\x0004Å	ÕR6hñQ\x0011n1m£Ù\x0011\x001bÊ\x0013éâ¹ï¸¡z#Ì£\x0002ùb4×Fs£.§Y\x0007\x0003uYðg4ÿ¨´\x0018Í·Ñ|=\x001a±ó]¥ó\x0018áÑT§L+B\x000bm´0â\x001aÈ]\x001e~Ãs |\x001aèF¢£ÓcVD\x0016Ûd±Lk.#EÉËGÍ4c ¤\x0019»-;\x0018å­\x0018±¡2<À²M]ý^pY\x000fÎ\x001a{Cåò[0â1ÀÒ>\x001aíå#Íqñ¢InLyª#ÙUc¸Íq{\x0001U#ÆÁ`¯^¶¥ç@x\x000fãjôñe7\x0017Ü\x00130úNßF\x0011ÚÌõB×GÏ
\x0006¤ö)Ç\x0004Ìõ\x0018i>\x0004fÅ^¶%É&ëE\x0007eMÒiS2µ:G¶@\x0013±M|¡]¶$?d½\x0000\x0001\x0005S\x001f%XyÔRôÍô=mÇ>ðÒ¶¢ÓyO'Õç-\x001cÆ~YläiGþZ\x0013¢\x001a«µ\x0001ÞÛ\x0015¼·õ7Õ²\x0003£òÀàª\x001a¾\x000f\x000b\x0017\x001f\x0006¹7\x000eôJ\x001a£S\x000b¨3²hZ»H½:ã¸îjîjÌë@éå8³"kzõHmGëoaùä\x0011\x0007\x000fcd4Äø¤h"jGE_\x0005pzÕi\x0006¼Ý\MoîwÎ¯nïï\x0007f}[8tAñÅÜI\x0005ÝÆÂKcQß\x001cì\x001f\ìï^\ô\x000eüf8ÝÓ#à¤àØ"PÔ\x001a.)§ã¸ÔD¼\x000eÎ¶áì\x00088x½nàrû½¨\lVnÉgZ\x0008·Ú{O¯Ne~3»»\x001f(q>c\x0006\x00032[ój öÈ`8Ú\x0003¼óþÃ¶ÚzO¯Î`.¡>7²ÏXyL\x000b<üMæY\x001dQ¥ÛXº\x0016Ë:.XóBÐèS°\x0019\Õ1»½\x0008Ë´±L%\x0016º\x0003¯5\x00071¤2\x001cÒn$mcÙêM4¹÷i\x000e\x0012\x001bÚC\x0016J¯ªE¥T®Måj\x0017Ëù4Â+Å¢\\x001eI\x001bºIêf\x001cocù1{HÙzÛìâ\x001e6ë©èEX¡\x0015j±àä\x0014L\x0010ùyöY\x0010Æ4	¬«ÝãJ±b\x001b+VobÌÞ!ÄÊÿ6Ñq4]Y=
«ezê¥>e\XzH«å\x001cµ\x000fp» ÿ8©%E|­Ç²iM4:å\x0017IÈã\\x0012¦²VZ­r\x0017S\-ÖÃàl5¹\x001aÒ\®%±%kå\x0016öÂçÃeúµ\x0018T
\x0011F®×µ"ÂÀµ÷\x000e;"Si²iêZc\x001cyèî¢¬½XÆí9í@4eÜ²©I«\x00153\jéØ«Úco¤àf\x001cN[æ
< 	«ðÇ=jéÜ«Ús3Ò\x0014/-¹Wè"´#Ãª/£kéÜ«Ús¯i\x0014sª-ÒÜn"XÙÈ|\x0019ÕÒ¹Wµç^°o¸$%Üø`Z}±Æ{µtîUí¹×&pÀÉeÄû(ùma5DQü\x0008µ,ðü\x000c½­<úÜãJv¨2ß&©k5DQ¬?·\x000cÜ¤AO*B\x001d|\x0018R{\x0013ÔsB#\õjÇË\x00012tJ.AÉK	²âb>ù>ß%¶çÓÉÃ§éÃZ4µ®¦gÁ9£¹# î©\x0016\x0017s¼\x0008íâlïÍÁÙyâ{~°wùçÁå\x0010jã©1xh}ç\x000ch)¹ù1(B¡Á3\x001bàé6\x001eçxÜGÄÂÜ\x0019ÆzNùªð 3m:3N/çÙÓÞJ®ßÇ\x0002Ïñx¶gG-É1uX¼`²f½eºhâÄ\x0011t®MçF]\x000cîS\x000eg­m\x0006OE»¦\x0011x¾çG-\x001e÷Fr~aõ4\x001f=Ù$À\x000bm¼0jõ4uª{kRÉX\x0012+²¹·Í\x0004¯\x0011x±\x0017Gàa`E\x0011\x001e\x001a\x00074ÝZhb§õx¼ÆÊBYY>oòx\x0012X=ûXï(Ê\x0008"yüÑËOÆ7#\x0008E\x001138{ìM°Ø\x0003Ï\x001b/WäPã¤²¥\x001eÎ\x00113Ð	\x0002_=^\x0019à±úàîO¾Læ\x001f\x001e\x0006-@Ít>r»<°©³3ºqv·ùö÷÷Î^]öj\x0004ze~O\x0002T£\x0000Á§7\x0017°vÄ\x0008¦k\x0001K\x0001u\x001bP\x0002º\x0000+\x0018\x0017-hD3ºKôò6\x0019ÅgskÝ´\x000b Aóv
Ù\x0000Ð¶\x0001í\x0018@\x001c\x0013h\x0016;,©¡\x001d·{\x0000@·É
º6 \x001bwG\x000c¥ôD\x00146VP,`§)\x0005ôm@?j\x0005ÁÖ µ\x0019W0[AQÛæ\x000eûMøB/Ýá<,\x0007ø4\x000f
;ºÅ1\x0002pñÂ%)(F\x0011\x0006É²A¶$=5;vø\x0012\x001b¹KbP©$BÎß]ô\x0006Bµ KrF\x00124\x0006\x001bÐ\x0011 K­ºR+AÊFrèu©\x0005\x0014}ÿ~÷ùÓ7zìðÛÿ8ý2»IT\x001f'7÷Óë+ä2Ä%½|þÎáÿVTðäº´V\x0018Ë©\x000eÚîæY¥××	ôô\x001cMwo\x001fî'wÏ^^\x001d\x001füëàìÙþ\x001f\x0007Ç'ð½£Ëý\x0002FØZUË\x0008W"Ðõ\x0005UJ¢×\x0007\x0018½´<F\J´à?Eÿ¥1¿ß\¹¯]ëx·órò0¥Þy=.¥%B'°­GB«9\x0015\x0014\x00044vG9ÿÖùäûí¯Û®<ßy¹wyvØÓJo	qe\x0019K\x0010½RôÀ\x0006LÇ@D£(¥\x0000DtÜ*"\\x0011S¨\x0005\x0019q8\x000b¸¨y\x0011v{ðÖ¹jBcMÁa\x001e\x0015¬X"44'@{£ì6\x0011á÷úê}\x0003Ð\x0015\x0017÷´·j««\x0008&T¯¢Iþ>DÌc¼ò*Òc\x0002Ý²=DøÅêU\x000c¹sJp
î<­"µÔ!uî>ì¼ÂÁÓ×³i§à)§Äw\x0019ÿÔa¢2Ë\x001d,ùT\x0012\x000b¦h!§ãø|2ßt\x0019ñYµR'H»²Ã:\x001d ò:ZC=1¾í\x0011Â\x0003êÐçùÍHèS(\x0011
\x001aªSÙÈvw\x001aä¢¬\x0001\x0007ÐBâÅ·
¢9.no!áÔàÊ³hP\x0002&%\x001fFOhÈou\x001dAzËZ	y)²\x0005ëÓ³\x0004·\x001cÇí\x000eÛ[G8Û²V§ñ¬PK¯DÈ½Ia\x001dÍ¶\x000f$übY+Ä\x0003:C^H1nn¶ßâÍÆB[U+\x001c£ò»ÖÑ7j ;âÙ³ç·³»\x0017ÙU5~Ìßm\x0006
g\ÕjÁ°~ë4 \x0005Mgr2tLJÅ\x00167\x001cÿ{ªö~\x0007×è>ZKL\x0010Lë)\x0003Sâã°9åíÍçß?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/adresses-addok-13.ndjson.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ü¸oNw\x0003íÈKÆ\x0008;SY§ÖÉR\x001aQëåHÎ±)éÃì¨ÝkÆ¬Ø¢èuXº4`d1X9\x0005gSy\x0015em°£&¤\x0005ØT`Î¸\x000b`ríM\x0014ÀI94¶I£îÓ\x0015ÙOÎbÆF1\x000b¢_\x000cäôÅqØ´àºËL5¹âÚ|k¤)±øÅºÄO½¿`\x001bá?B\x000e÷\x0007{eîsce=âú_cEfÎ¡\x0004Ë\x0007\x0014R¹fýFª+òz-.9ñÉY\x0008\x0010°Å\x000e[fäúÏ6²d\x000b#\x0014*ø[4²ÏFº\x000bpMÂ[£mY¯\x0005{Õ`Ãy¦0ciÁ\x0015ZÃÎ\x0010F¶\x0010ov¸|tuÄ\x0005WäzJø¢ã§Á3¡Îí°à±B[±®,Ù

3\x001a\x0004ím,\x001dG\x0012+t=)<þ"ì:\x0007¦¡Ùu%!0\x0010I¶Ê åù,a¬ÊË+RX\x001aO·\x000fn¤3¸"×Ch¸«PÃµaaG§öâðf$	¸B³\x0012Â­Øy!É\x0000}4\x0016\x0017ÙÒa$
¸"g°tåQóä\x0006>\x001a´Èw¦xà\x0014ÛF\x0017Ð\x0016v\x00140\x00071;¥5,È[ÚMM¡«ãâ`
ßEqz\x001f±6 e­\x000c- ](´\x0015«o©­Ã==§H¶öt\x0007¤\x0017\x0000:êÂÀ¶B«î&Ív}±B mXVmÝÔ\x000e\x001f¬ñÊ\x000bcÀ\x0015¹îiK¯w\x0010\x001fm§\x001e½úÑ­=Êt§æ·"×-M¯fqr×íaÇ6éÓ¢\x0008ÆÖmjµ8âJ^Ô\ËòbÊÑ ôÄÅ¸µñª¤\x001fm$[\x001eV±=´\x000c=TnvÞDDÞ©Î­Ðõ¡¥3+OKÊef¬"«¾/OÝ:â¶\x001eqë\x0011Y*¥XB»Ã\x0015µN!nAvÂÐ)àS1¤ono¼8\x0012s[¡ÅAÔ²?­¸\x0007\x0011 ³ÇgÂPwmöpÆ½\x000e¥¿Fq$\x001aÆDÚ
]\x0017õWx\x0012m\x00194­ÈQëæ´\x0014Î÷-{øj\x000f£ 7R<\x0006$ó\x0007\x00128%Õ(æ\x0005u4
ræì\x001dÇ\x0003W
séhÉ%÷*V¢ÀçrÝôgS?ãnB`G±Ä%ó\x0012Uâ<\x001dWIÙ£\x001c÷Ê@×9½Ë:a\x0017è]»@ãR´E»âÏÕ!K#µ\x000fÊß4±	\x000c^è¶ª¹¥äi»Ö±\x0008.\x0004uDi	°sq³(àÞÀdÙãY(.ÙÀp wØ²BØ¹¼¤=	Â-ÌíÄ=a?$üeÇ\x0004|r\x0013rò¥èA¤Á\x0011.Ø©¶¡sñ¬6D:ÇÁ2³\x0010#N»òz¸\x001bW²bÕK¬ÏQ3WÌ\x0006]BþúÝ\x0019D\x0014y\x0001ÊU<ò¶
¶åmR· §B^ómá\x0001qüU¾{ò\x0006¶Ï\x0015;¨,Êó\x0007æDäC6ÑÀLÂÐ¡\x0013³¡C\x0015³¥ÀT4ÍDZ(¬¢y®­ãÕ.Ø\x001bÛ$SÉôÛÕ"<wÐ	\x001cPlQa\x0008]ó\x0002][Ë2\x0016ô\x001csÊÖlïñ¦w©8/±\x0015¡£\x0000­RýìYuS@nc¹	Æö[Ø^bçê
x&>\x0007ø×T¶¥f\x0019ÓÆÞæ?X÷¶3%(Y°éjV\x001f,Lððð!/d\x001e9t«Cè»D\x001e¶²þ-aghV÷Z\x0015ç(çïÎ¹~7?J5÷:=Jòê\x0006\ºò A'Å:k!Åè7
QSÏô=I\x001eÊ-^Ûè&ðñ?XÁ9\x0001Q7'\x000fÁ\x0007¸©àõSú^<Þ(å\x000fä-Xó÷>Y\x001c=ðÉ \x001bÜ<:JáÑU¬°JT¡¼\x0005\x000b8ùÉë$á³Cû´¸Iôàïªò\x0007+8Åâ®J<#Á³ÉL\x0002SÂ#nÿ`\x0005Nøÿ>ÑååäFÌÐ\x0001á½&Þu\x001e%=\x0018<×¤\x00073\x0007×î_\x0003%\x0000)3AÇòÈ[ßÅw'\x0016×­F!\x001bÀc\x001cT4°Uø)à\x001b¯Cù\x0015>T \x001cô­¼T¸\x000c\x0000ØÉ1SÕi|OØFh|§¤8@¥[\x0015åc¼![<\x0014\x0015¶ÀØô\x0005\x0001N7uðåð@°«U°Ó R,ØÉ\x0000v\x0004b\x0002\x0013Øp|\x0019Ý1zþ`lm$v\x0016\x0004S\x0003\x0018x!Èâh¨Qú¦\x0005< xJ\x0015ý\x0000à\x000e°Ó\x000fò£!cû1dRùJ_\x0016È3º
ÏZC½Ñs\x0019±@om\x0014/ÄàµËN,\x0014\x000fQn\x0014í
>Ó_VJ°£\x0008À ³£{»Öf"ûÉ^s­AS$\x0011GÝ-íüð»ûÃÓÃÝ$t-uE\x0017aç\x000cVîßìx¢
Åå\x0016ØIüõJ¦t6#Ök¶~×K&\x0019¬o(·¸\x001e|¸ÿt<ß|yÇÍ\x0012?^±ù"\x000eâTa]%\x001fR²\x001c:	ÚÉ*½Ì@Z^/üZz\x0015¯¨\x0004YJ	ÃBà\x000c¼ÞX>\x0018_ä\x0000faùuöæ"°Ñîè\x001b9]údI¶W>Y$åÊ'ÛæÍ°\x00148#»úÍÁ
ÖjZsìË\x00017HÌ£\x0006\x001f .
½ç»çûïNÇçëíWM·!L\x0001®T»<Q(¸.Mv»"ùßêéé\x0016¨å÷|ìjuÙ*\x0001¶ØêÌJAaX«×Ê\x001b.16<c@ØA»\x0008Á4T¥q±o®Å>OÞ\x0018\x00154Lº-sEÚa\x000fI®t\x000b
Ó\x0019ºnXÖ|¯3½\x0004@(vH°\x0008= ¶\x000cRëfû®«Çn\x0012ý\x0008-Ýèº\x0006è½\x001cAÌfÐ6º;þr8âa:\x0014OÇ\x0003O\x000e?ÿpwÍ\x0016Rç ÃrÖ~ +\x0012]\x000f8­ò(¨7&è\x0006[Ìá¹\x0008s\x0006BÆdðk
x.\x001bi+¬Èu<sÔ£w/\x0000GqÙ¢µ}ã\x0013ç\x0013G§èÎãû\x001f®\x001ae\x0000(F©ó\x0010º«¶ìª¹;ù\x000f\x000ftñþxÅÝ¥SÄ\x001b&\x0016\x0002öé\x0017yNÿ#\x0013íhè7vW±\x000beÀ¤¶öy\x001fÐÉÎ9B>Z§G¬9Þ\x0002¡Ù\x0002%óZ9ÈÁf}\x0005mHÅ\x0018¶ÌÈuÂ 8ç6É\x0018\x001cûÌÞæö\x001ag+)	·×ÝÃãÍW\x001fÎ§ãÝ\x0015w\x0017özè×ÛX9è\x0012gmìýÐl\x0000öë\x0014­µñ»¶
2Z¤´µH\x000fz©Ï?2íÁõ\x0018Ý°\x0013i·vz~(s
{x¶eÿÄì'¦ÑWòO\x0012\x001b;5ûl¢Q+$oøó¡!f'ä$$µè\x001f+;B\x0000ÃíBov\x001e6ÉÍ¸ñ-¸Í%²\x0003£ÉkÅ\x0019­4ú$ÖÇ%ÍÌK¿N³<ü°û¡+
¾°þK>D6hiPu¬h¥\x000fÉsÇ­$fWVvàQby\x0004:>Ä\x0005Ú	hnöª#[,+/s·v\x0004þÉT
{|öì\x0005²\x0014·\x000cìVÃ½E\x001e=.¤+]T¼í\ó¶ÌéS	·\x0008âfÕâ}ßl'ò-d/\x001c`sÉ\x000c.\x001d\x0008Ô\x0011O®Çô û¿`kqg\x0017J\x001fÙúÕVv$\x0011vyËäWOØ\x000eÏ	[\x000b\¥$'lY¥Û·YE[r\x0014£\x0016Ð´\x0008Ðw\x000bé0Â6\x001aª5Í\x0017Sé,ë5Á\x0017l'WÒ"Çí\x0007´8ðÉ\x0019ÌÁ
\x0014ÛüäÔ
ÿÅéþñéxº¿ù÷koËúàcP2LE¯	\x0005CîøJ\x0001\x0019²âÙÇýÈyX\x0016_qùÄæòá`±%""(ÛÕiI\x0014ì[f.ÜØ[±Ù[\x0003\x001cSÏD6ARçYò¤a\x0008GhJÜß1',ØÝpSW®·DÙj¢§uJ#`Ïý¡\x001bÐF	hòÂU½3ýûQtÓEgeAã¿T\x0008Ä·>ÛÏÖ\Æðu\x001f9ì\x0001^æ×h\x0007:K\x0017Ç\x0006´«\x001dÄû|×Y©\x0016ÚÝºÅ.u\x000c78É\x0013v=É\x001bùÅíw2}¶wh©Fâ\x0006/É]_\x0012cø\x001a\x000e-¤Cè»¥v!C.Qß±÷ÍÐ>ÍíU
¯¦Ímaoë8ØÛaÐë\x0013§NjmgC¯\x0002=^É\x0011¶\x000bp9\x00117R°°\x0008\x0005b\x0003Äd\x0008{[«Y°·¾;ïæê|}\x0003ÓÜX\¿;(0·ñ%a\x0016·v`\x0014;Ðû$½
ú\x001fäx¨¥è6;<ªôq-ì °YÎ´¾Ç\x000fÄ¶h< ã&Ó¶ÔõéüÏ7ûó?ÿóñêUôa¼<¨U~Áø\x0018+½3¦ÈÜË2unþKN\x001b6éHNÌ3õâX@EßFðå´êÆsRá9Q-yÆö-gFVì°Ã-\x001d¸dR«[\x000fAy]Äs\x0000[ùiTvË NÜù\x001cúJJBLï|ün\x001e£fìK;agm\­1N\x000e>ØÄG
î[öª\x0004[ØQ`sa}P(\x0014K0)AWE\x0004vnàà\x0019«-{'aoËüõ»)<½ï	;¹\x0000írAÞøêdÄWsÈSw	Jj4ð¥\x000f+"y\x001d½µI¬$¹Ö%ù»`Ó\x001b \x0007¢b¡gÂ\x001a<ó éµ`g%Þ*\x001dkk\x0013Ý\x0007\x0014_É~ø\x0018å¨\x001c]%!ógçÁ[5A·Ê\x0013¸¹°!J;6qW%`2\x0007oÕ-Þ*\x001fLU&l^W¸1ì!\x0017[OdãïÖ¢#ÞPè!#AV,ïIBÏ~åÔ\x00017x\x0006'hñ\x000crZ]HEw±Ðq!d¨Í3IJi\x000eÒ£°§`°Ç\x0004òEc57OúÁh©Â(sî±Ñ=\x001fñ-<\x001aæ\x0006Rë7»ÖÁÂqw¡\x001cw­·l¢MxÒ>ÕóN·º\x000cY*AÃ6¡\x0007|êÜ\x001bÄ°\x0005Üha\x0014:áº~·ÇÁ{Z[\x000bÛÛÍF1\x0018fÂ\x00161\x000cE?âXÆÌ"=r\x0018\x001e\x001d é!Ï·<:fË*FX%YS+K\x0004n,^ZQ7Þ8\x0008b5xf¹x8ÏñýÌ¢yeßÃÑ:
.\x0007c\x0016*0ÏÄfëS uedr/ÎÇ8¥Ë´[¯Â\x001c\þ`ùi,kV?ë\x0014 qVÓKa\x0010\x0005xSÿé\x0016¸È qUoRzÆ\x0014tqÒZ\x000bMÙi\x0000n\x0002\x0017\x0001\x001cy¸¹Îa¢ÿ!Å¥è¬&\x0008²|*ð®¿Kgp'Áp\x0014è<Â=Íà\x0018Áù05·ºÞ9Á\x0000×¾öÒvRá\x0016><B\x000e)sÛaóûh|Âö"±6ØªPÈ\x001aló½eq/,Îí¾î\x0015nú²ø¢P&û<YÜomD/6"Ï®}³ôá~bÏª\x001fn\x001a«Ì·Ò``\x0002\x00173\x0004.:\x00162\x0007ºÀÅ¥<$Òs´Óhö ¶Á«¿àr2rsw¾$Jç$=%Î½çik¯¤ºW\I\x001cW;\x000eä\x0004¸â1H\x0000\x000fÓ+úù\x0019¼Î?8r7n+vÐZÌ¹9zÔ\x0015l\x0015
!Êræ­åÌF|7w\x001añÝAfè»c@\x0007c§ÖÙ1xùÕâ>Öæ\x001bÞ\x001exCx~ÓãF\x001cqÇ\x0018Û·\©¡WæéðË\x001fo=>\x001eÎÚ'æ2½	z´¡1\x0015&Ùy%t\x00123d\x001c]\¹½¼0I½­,í.rËº¯¿\x0013cp\x001dáÌQ¢{rH\x001c² \x001b,\x0015a¸w·!×RÐ\x0010´·Câ\x0005ÙVdïÐ_)Ë ) aÄ;éIRºkY@VbÂ»X\x0003:»\x00142Ë°5øÄu'bA®'|ÍÒÉê	® ×Ùd3j¹XÅ\x0015ah&cÄRÕÝ¸9	\x001cQ¹uA\x0015ÜP¡;\x0019)ÄO\x0015ðU¡øèÆ$\x0016àT¹õ,OÆÁ\x0014­ÃchÝdAÎâm}\x0000ùm\x001cd¯ORÓ0dïïÏÈÕßw!'¡^F\x000b¨A\x0010Z³w\x000bXÎIÏJ²@#ÈÜ!boÙmÄ½að«§Àpë\x000cÖNEÖs\x0012´2õ\x001e=|µ2¸zòd¶\x000e¡\x0016Â)'\x000cb³
Ë£êñ«Ãd®§0\x0004çÛjøjÎ\x0005\x0004Ý-h/\x000c"R\x0007\x000cmdºØñ\x0018!oÃÚ^I\x001fmjq5ä;\x001cÿ|¸îÔhvÁ´Ôßð«Q¸9ßó÷Ëóæ\x0017½\x0003æ\x0004¹\x0001~iôç\x00165ä®¸\x001dû)\x000e¾Ó´Ô[¿ëEôkdàUFµã»Ãß¯uçº²ÃºbõK<ýÿ:ì\x001f¿â7°V¶\x000f	ÈªÂ\x0016!ÁÆ/{Ñ*ÕrIu\x0012c«$ï\x001f\x001e\x001f;I£K=Ç\x0000·]dw¹>J®¶-¥@¿ã7 ÄÐ=.dÈæq\x0019ÿ®\x0017M2Ð\x000e\x000f}"iÑ\x000e3,]Ïw\x0003Y¹\x000bÉ3Lawd«x\x0003¯ýü\x0018«\x001de^éç»ÐøùÉ\x001aIãg\x0003Ï6ÊyC«#Ò?T)uí\x0008G¢QiÐÉbt«Ê)I:Ò0bãÊèuç`,¸²À[±\x0010Ö!õ¤Îø½¹4-tÞÅ[ç9q¡Ä÷Z 4ä\x000fn}\x0018¹ø\x000b°àA0¡~\x0013°w0ÆD&èìbÝÈÇwí,\x000b}²\x0016¾Ü\x0010X¤£\Ç¿ ×\x0001t«¬ç$ä3â&Á84!§!uè,Tëd ä\x000c×·g6­\x0006yäã/À¹îä¥e\x0012\x0018\x0018Ë5>á'\x001b£Nþ\x000c
ú?®tý­Ð\x0016¦[i\x0005qÐ\x001b=vò\x0017h-v³Hp1´\x0002\x0007|\x0003\x001dN¾kÇÕS_Â
í\x0004\x0013#Ù\x0003ç.¼òO['ELÊsßæHÈÑB>\x0014nhS(­zoÙµÃH©Q[Ì\x0003è\x001c~µ-õéýe\x0016µÁßJd\x000fiJúùÈéí§zi_ä\x0005÷\x000b+='q%1y\x0003XZ'|WìhÊÅÆÇÿpøÌÞ"ýçé|]Y\x000eÚ\x00119«Ò¢ÏÖÊ3Ò\x001cÇ×¶µ1¶ölE\x001dÔ\x0003ÃçÀ\x001eÞ_£ØÎ¨f\x001dz=+ÜBë§öXKvøhÄv^"{U³d\o\x000e \x000ci´Ç\x001bº&\x0007^®Ëíê²§î\x000eÏw×Î²¨¼d.WÁ\x001c	;ê¢¯ÜÏ{ÙXã¾öþ\x0006o%<]J\x000cÎÑïÒÅí©&·«ËÃÁê\x0005X&i¼ð\x001b\x0012Ýçp\x0017jþ
@û¶k&Ðå«
\x0018²\x001d>bnÐOí[È2EeÎª¥\x001dcc@:Ì¨2<Ò\x001fÜ&Jé\x001478ÅFá|¨&íè¼\x001fzQ¹Í})\x0012Ò\³o¬¡ñË`Jÿää6¡\x0019È9M5m\x001c½©l\x0013Ú9ÉgdvÔ(ý-$tÜã\x0006^CîRÜiUS´öàëa.2é\x0010\x00077éw]æ\x0003Ý3ÇçóÂ5ÚÅ@½gÉEYÚØ#\x001d31eË\x0003¼æÕ:mdÃâh¬;uø«^4Ç`a¬ÈR!:~\x001aÎJ¼zñâ\x001dHpÀÔÜgÀEïz@¾ ïhÖ®Ü×°îMñM`ÊCA"Â}
¿\x0004tdMliÎèç\Ý\x0018g³Ìç%Û¦\x001b\x0005Þ_\x001e\x0000\x001f½	\x000bpud,·=Ö[§¤\x0013«S´\x0016?yÈµ±\x0000Wê\x0002§\x0008Ryd\x0017htÊX;cÕÑ° \x0016(\x0003ëU\x0019\x0006Ýð%cÆãÊ\x000bp\x001dW¶Ü	`Å¶Ä\x001a¸f\x0002tÜÒnÈç¿ ×QE
*ä+ÆV6I"\x001b¬÷oÍ1&*ÕÌª\ã\x00159àò\x0017éâê\x0005¸NXÓ\x0019\x0010/úd\x0003ã:ÆÜ|òD^Ö½b3´\x0018ø²NL °µì\x0018.JyÕ8ø] ë9±¼ë¡YÁ\x0017¿º¹\±G\x001fþ.ÐuCo\Z/^xÃ2Ô\x0002-;RDZÜÑ<ÜGeâ·ÛÚÒåÃÌ]ä+tÄv±¨\jöGÞÚÓ1Ó3ßy­pee\x0013v\x0017y
$åÉzï1û\x0002]7µÑ\x000eV1O
;+t\x0008À¨B÷µ\x001aÓãÏÐ5h÷Ìù#í¼:Ô8\x001aöNÐR,Yêg~J?\x001fï®ãæ0¹&Ì ³pÔü#rT¾YECK±§`}ÃÓééÉ¼:¾xë½hÑò¤nyhmÎ%¡B.Ï_ç\x001fO§ãù*ÕS\x0016Æ&Ø\x0010WUZeP\x0002	,É¥öSî¡\x0007Ì\x000fxÅú.:?{j\x0017]¡¯\Z!°fäs·ÎÈK+ÐbNný!-ØZè\x0019D\x00138Y,bk\x001e\x0003abÚ\x0005EJ WÞ ­PÞÐ<Ôëg³b\x001ah	 µe 2>¸\x0011\x000b¶«7¢eê¤\x0005®ùKqDûÄ\x0001¶)ô­Î÷¯Ïí«²B°gÊ{±\x0005\x0003~wt\x0013\x001btÝ\x0016lþµÁÛÖ<ðT}ßí\x0003Ú\x0002Ü2ÞwôOØYtôûÚ\x0014ÂÃh\x0010\x0003¬EÁ«\x0011}~T½ü÷ÏÌÐðÿ_wùÿÇÞ»ìØv\x001bÙ¢¿¨\x000fØàûÑä²]ºVm¸Q\x001dcI{YÊBîLUî¾¥\x0002\x000cß¨Þi^ßöý\x0003ÿI}É ''GL)!×:À2pZ~¤=4WAF\x0004#ÆPNÈÈrÌ²¿±S¼ñ.@#³ïn(Ï\P\x0005Æ\x000c[F¢ 0c¾^},/º¿¸Ã\x0004¹ÊÉÌ*
\x0005¼üa7\x001b\x0008Ó\x0004\x001ew+\x0003¦½ÿÏÊîUsmé\x001dl+vèC¶</ÔÉp¹_X¿\x0013Í«!\x000bìXó.\x001dÇñ\x001dûøEiìFá&yÔp*CÛ­Jm'\x000fÛ\x001fï~qæÅ£sõáÌ D5\x0005wÚ\x00166F§þ\x001aG·j
%k¸-<ç\x000fôc|GVåh¼óÀý\x001dx¥²R4§Ëpñ¨CS±C×¡1Æx(úg®\x0000{Ä\x000e\x0007-!ÊÓ
WÚxNnØpN\x0007¤a[+d¬èð\x0014\x0014*ì"\x0013[\x0015;âx»í1/$>D©\x0005
5ýKºÆü¢B§_\x0018VòRÝÜÁ;!G'\x0018» ÏÓ©\x0014:6ßøý\x0002µ\x001fK öÅË¿¿\M#Å#\x001fN\Ò\x0012\x001de@~Äñ¥2~#þ°jÊ\x0019Â\x00062äáÍvñÃ^5Êd&Æïüâü§?Ç67r£ù$\x0004\x000coýbòµ\x001c½å\x00056r|Ýöú\x000cÕ·¤ó±ú6ÿ]¯Úd²<\x0016DºWNÏîþùéN»»¿ý¯kwéSEÙb]µ³ÓòGOß#\x0011ávüVx;®\x0012w!?üÄO{Õ,\x0005+á\x0005>0Oê·Î/Ï5m¬v\x000fOW:ýä¿7UÛ²>/¤\x0004-Ý ·³ZÁ\x0015)Ä,ÆI\x000fí½Er²ÿ,ä0&tP	D®ôLJæ
¸\x0013ù¿N<­
q\x0014>J¾ßÊO=äÔ
yÏ©#Oó÷|É0#\x0004±Zæ³\x0012ß\x001c§Ty
8v`\x0000÷°ÄF´\x001bÙv\x0001mòZ=äÓ
9Ã'»Þg(ó\x0013Ü]t \x0005i\x000bæ/\x001br/åFC\x001f	\x001dcJê\x0016X><\x0005rÒóYÜ\x0017¹ \x0003lxV²Ô\x0008}à¥L®ôuÉÂ\x0006Ý\x0005f"Å \x001e2 ³P`7tßNÏ\x0007H\x0016ðµóÿ¸ûç\x000fôo¯GKJÎ! J*Ö²6\x0007¥\x0018ë(Ùå÷÷[9\x001d~&ç-\x0019ôðTÔ\¾>\x0018ñÞ­ùm\x0007M¢&ÓÄ!\x000eÌ´ÿáH	s~á\x0013½¦\x000bA´#Ú:åÇ8¾B{ c*Ó¡¶WÌv9k\x0004¿3³\x0016ëäàòhöÖ\x0013E\x000e\x0014$ÜO:ÎÞ\x001at\x0007Ù\x0003çPá\x0016ú½ÕLÎK31Ó\x0019Dæ<ôV»è@QÈzÊì°\x0013Þ;q\x0015ozÄã¸á\x001aÀ­²¸;®\x0012
+ùD\x0005p©\x0000IÂ\x0006\x000cIBÀÇeË\x0004\x001f¢\x0019Õ%ñÜbmå¤\x001c½Ì\x001d.4B~M\x0016ÜÞÅÃÁË\x0000åx6ä ÜG3é³ ôNÖä-KOïJw¸+é\x0003<Ùà¼=§of&¾Õ6ä\x0004ß¬AùÈ\x0006\x001bßÉõ=¿N¹ùã\x000epr\x0004_\x001c½ þ¤$ïÐÃn71µ\x00052´@óÖè¢a6Pl\x0018\x0004t2VúwíS^¹	´@³ûCràÎ.±ëìTvU\x0008j\x0012:¸CèÀät¢õg\x0013å¶\x0012ºjLb\x0007w\x001d\x0013D$_\x0011¢<x$ )\x000e¾\x00027hp\x0016nNv®d¯Îú00PÛÍW{\x001aÕ
#´2´.ízè-âL¢ë1VÒ9xùC\x0003ÜÜ\x0000ªuÙÈY¬EÉÍ;ãf×RÀ"ÐóéÏtà\x001bÏÿ?~÷pÿqu|cêÊ*â×½ÐàXbJÝ\x001bªís7óäN\x001a="CÿG"µÚ$T(\x0001²IÊ¸ÏèÆ\x0015Ù@Ï\x0013\x000båbTþÓÛ¡ôÌJ3\x001eîºôß>=\x000c+ÿÆ7uå¤ª¤wzF\x0012¥\x001b±?°©mzçVV~^´\x0018¥åR¥\x0006i¹Å\x000f{Õ(\x0005\x0007%|ÿáéñýÝ§'ÊH®( ß)¤ÝÛ;½¦ì£ë¿ÒÍkÊxÿm¯ÑèC1\x001cú\x0006\x0017¿ëUÌ(\x000e>Ä\x000eôñÓýùñ±þyþó53G£¥\x0016a*Ý^+3Ð!`MeäðVVëç¥ÃHÉ\x001b\x0012Æ@<\x001eõÉRÂ\x0006}Ã\x0014Y\x0019§?\x0015\x00111nöÔâ¤	û\x001f?=Ý?\µh¼\x0019²M;\x0001\x001bÝ
 [e[\x0017Ú,ý¢j0Fñ(e\x0011¬Æ±=\x001dä|¤f ´
zJ\x0008Ó{=Ê±&\x0005IJ\x0015EMÑêXöÔ(mÀ¨Á\x0013Þ\x0001.Å7¢%9ÉpüyöÀ\x001cõÛÔüû»_>½<×#æÇï\x001e^\x001e¯¸·¤\x0017Ô9µO{}N>jbx(óöïéÉÖ:<\x0005­~×k&,T+àëÓ·tO ¿/ä\x0006?^'¢]h9gï[¹02¡ÊþD(YHeúFV'À­\x001b?}C§#WHH¦³Oðï²böÕE1Ñsþ]áö"w@î*\x001e#\x0014%\x0001\x0017½P*ÏÙ¤éDV\x0003v\x0000\x001czRÆÀJ\x0008v\x0010²èÎÍL°?=P6ä\x0000È¹Ó5±)²¨\x0013rß\IÆúÈ:r\x0000\x0012tB¶Nâ\x0013² ãÉ)/
\x0002\x0015\x0019Þ\x0012c>Ãòm$Y°|"IÉL:m\x000boÐ`èl÷Þmþf-'ÉYRÈµ\x000bzeèÞ[\x0011¹¶{Ãxñ\x0013nÈ:ÏÓþê\x0000\x0019ô½ù£\x000360´èígCÏû«7èÞ\x0013¹é1=×ché(\x0015rÔßnÈ}
¹7XÃæÈZT¹hßU©öoî?.ýûüG\É]óþ\x0001ÑààtÌOßldäõÜ¦ør~¸ûüùåñüéºÓÜÑ"ÍK´Âmè68»ô|>ÝÎ\x0015\x0019µî®ñ\x0010ÎF\x001eÂÁò(ÿ>£\x001e\x00021ÇÁK{ø0\x001d¹mÀ]^	);ÝhäùM¤\x00013^t$\x0015ÂTû¬!ÛþÉÜ\x0010eû:ä(Éu(\x000em\x0017Çcg\x0003îº<Ó%Kb ÿ(è|ÂWBvuD7dß¹@Ð¹¬}¬\x0002¡ýÆÐÓñª\x0006\x001cÀÊ\x0001y¬}ÖØ­,Ø½\x0015\x0005AÓcCN`\x000cdÿLÚî±+Ãg%?¹\x001fõ
9wd\x0007å^B¦ã]ô{Ð\x001eÄ=\x0017ùÙz^Z¯Ð½´N\x001f
Óf\x0004M¡\x001f-\x0008té"IóÊú~biµ(ÚàÄv&äZþ^yJ¿HUÀ\x001bDÐÚ\x001eÖPÈ§\x0012´¯\x001c +WÑà*\x001bUn¦QèÄSaüÕµAxå,Úý\x0001ÈÊQD\x0016\x0010öp¥¯bR³ßÁY2h?óÎ£lEF@çz)­Ü¥_ÿ© \x0001Y%QW%7ÔÒ\x001c¾2C\x0005û
y/Ø\x0007J&ð\x001cõé@¥\x0016\x0015N¾³#ªùäVîX$\x0000I_ñ$¥eÇ*\x0004BãäFî®èÈ÷:\x000bw9èÛÃuXð+ö %ð\x001fÞ¬]#\x000c\x0012Ú\x0016C\x0017Õ®6\x0016 Qm+²VEÐùp\x0016!%³ÚÕ¦ïjOQl\x0017\x0019¡+ ¡"3ÉKµ\x0004åÊæHØÜ û¶f½Ã\x0004ËÈÜ{\x0002ZéÃQ]&pÌjó¾ùx#k¸Äi/
eÅ$&ðøJ¬3Ò«ÍgúæóAu\Ê¤´À\x0015J\x0019nÊ\x001a®vÉ`hÓi·#3R\x0004<\x000eZXL3S¢ÕImûIíïu2þhI#kR<\x0004\x001eiút³\x0005¿}zùÔ\x001fO\x001eÿtzütõÙì³ü.nLmJ)ABüÖ¨n¨\x0004|
÷"\x0003©4»k\x0010l¡l\x000e¹ú5\x000bq\x0008Å qlò0r\x0019\x001d\x001bÛÿ+´öÿ "jÁPú^ÁZ0B\x001f'[[eâfwTi\x001b\x0002Ý2fqÛ_Ã\x0003\x000c	½5Ê#M¦µ\x0014-Wß\x0012tQ	}\x001cN÷PXbñu¶`ÒKWg\x000b@÷$Sp\x0001âOÜâs\x000b,E"ìMç[êF6Ñ;(Ù\x0006ÆD¸©\x0013ñmQ\x0004¹¹\x000cr\7j:\x0014p
\x00114-;Ì[$®\x0019\x000bõ\x001dºÙ\x00056-V%pÌAêØ"ø\x0001B¬d#¨ãØ\x0017\x001d3ùÊvgFý§
»ë?Y£\x0012\x0004»Éò¨4nÂ\x000bR\x0015¸Ó\x0013þÖ
\x000eü­õµú\x0006·Vè<¿(Ô?h\x0001BX\x0019<Á]°½+'e,\x0016\x001dlV\x0007\x001c\x0016ª+±Ò¨\UÁcW®²ö]NSÙ\x0008ÏÌÚKùbúu~TßÙ°»ú¥ã±Ë£³U\x0014^Z,3)$\x0005é:¨ò´«=®qGá N¬Í	ý$Üå¥U*ó´"2vùÃ~Èsó\x0019\x001còAä\x0001¬N*ÓOãJáÒÅ¡Rþp1ø8[¼Ãl1¥}ä¯§4\x000e\x0014Ï\x000b¢r\x0006/]Xf¢¦ÔÀ½\x0000\x00075¥h\x00136p\x0017p¡ÎfÌ¬íRº¼ä~û|¢ËðîëóÓËuù,$+\x001fÊã%ý\"Bx:²|dÞÐE>\x001f]H-æB\x0002±K-fNXbß2E$\x0016)#Æ QÑNgômglØ±÷± )\x0008ô1¶dª¥\x0003½Ð·Å\x0015v\x0004l
·-a§¢òÖ¡ìy4¦ðÓ¸1\x0005ªÐÎth\x0015\x000c¾l²(\x000e&öÑ9ùÚkl©cOäu7ì~X0ù+Påqßàà:Xñjjj\x0000=!ªØ»\x000c\x0011w\x0012=ôÏÅy~úni2\x000f ø\x001aÜ¬°»\x000f×rÊ\x0003ÄÞ\x0005·\x000eÅ>òµWÓÿfðf]ù-fÔ[\x000f§»_=\x001eéßýþû\x0017ròó5[ú£\x001c¼ Û`§ßÒ\ÄéCg©rLÞ¸_\x001fÍzdßâf=èËð^ðB\x0005/^bÈ9
»á±èµ\x0003÷\x000fÍDP}z\x000b¡|B&:XÙqR\x001eÞ{?\x0001KrõÝË"¢ð ]\x0016\Vô?¨E5z\x0011ÒlÓ{µA¤ÙÚ8Á)dì6³úè^¨óLEÑ\x0019é©#À}ÄAö1SØà¦DH;4\x0010!\x0011Vo%¥\x0015Ì4L	!n:\x0007lí®=&ñ;tË`=ÝÞ\x0001iX¦\x0016\x000b1¬¢"\x001cöáÔ\x000f/<¿~ùîéî\x001f\x001f~¼¢ëf%X\x001c)2Ê{\x0007\x001c+÷ÂV\x000cÁøñV|wÎ=1Ù­§\x001dî:\x00042)þÉ¢z£\x0015Íà\x000cáçÎ{ì|
À'Ä²¨¢íUÉ±7õl\x0006pGí>ÐX öupb7Q\x0010 \x0007wCíÕ>VõväÞ\x0003VtúD]!0\x001crð³}jå>ýòéãùïï~qO\x0017ÐÓËÎ®¹a\x000523÷ýJw&´Ë«X\x0005&od¿.z\x0000UL¶æÐ.\x0013 
¤°#J9É\x0010&©|öciÃ2÷\x0014AÂ8\x000eë\x0002\x001b\x001cóJYôÓ[®7Ïv\x0000Ðæl=[_¾\x0014¼ÓO×\~')½©wìÒ1{4liýÕ
W?¯\x0011myðîü=4´ÌÐ\x0017=DùF¥\x0019-ñ\x000c}NÁt±µ\x0014\x0012à\x000c°vI\x0004´G'¯¤;rgÕ»J1á
:Ü`úË§çÓÃý¤»ámT8á.×ÉäÖ^\x001aRÌ ^¢¹åö	\x0006&§J§Êêw½jq(j\x001cVèÏûëûóóý·w_ÝÓg\x001eúÀu\x0004èP\x0012Ü¶¬\x0002Ú:ÁéDÈPÎYù\x001a"Ó

§\x0000ÙU\x0002¥¯9àï\x0012loâý
¢f½À;,Jéù2Ã*¼\GNr\x0018é\x0014g\x0013;rêÈÉ\x0003\x0013P.åg\C+\x0012ZE9ôIìÀVÏl¼\x001b2÷1Ò1ÅA|²S¶Ø\x0006Ýû$¬±@4H\x001f­=\x0016Tø¹IB\x001b5>iIxøÍÓËÝ¯xzå+7fiçÄcM
º\x001eÂwáÈÀÜ\x0010\x001fä¢Avàõo:Ú¥½ØLù¤Ju" ", vdà¾fQ¢þÆÄ|{¨âAÐ1KèRÈ\x001eSY=¤²ýZÃj\x00181RMör%õìÐÈ
T¦!\x0015ErÌh\Ö¢§ Pä?ë)hÐ½§ @\x001bØC1\x001ehú²_\x001dæ=\x0005;tÿjËÃ`\x0010V±\x0014\x0006ïyüÕ³\x001d\x0019X»öÄì\x001eØVÆBÂ¢4Î\x0013\x000c=L
\x001ax»CBÑ\x0014Þ{!	OÿÁÆá¡[aFân\x0003ý{Lr°Öò«ËøóðºÙûë&Ïº#×"¿½y±«ÕaW«<k*Ø»'Zºm3¬¡\ñÎZé:v'Z`×Î\x001aº{È\x0013e\x001bµvÑÈÏÌrS¡ãÝ§I¾:=¿ý"ÿëéüxÿÝÂÈàÅ-ÌdÚ­\x000eÊtuÈ3:§*uà­ÅÙê1¬ \x0007\x0011ï¨¤Ë\x001cmé\x001bDÝ:»¶\x001e4¼#¿?t2cJ\x0017¤jåóB\x0000û8SáÓÒvT¬\x0010\x001f;2ÝùÈøÍJt"Ê1Î((ô ´\x001d¹ä\x0010Ñ\x0018AdjöÀcOßìgD\x0011z\x0010Ä*hÈ\x00015\x0004[S<<käRo\x001e©A¶aÊXÙ\x000elDc\x0017\x0019Cò¼ä0mßÔ\x0000t¤¸\x000b\x001eqA°fØ¨$·EÞæ VvNHú\x0008Ð}äÞ\x000c1¼a%S:LÉ\x000bvä\x00151ÁV\x0000spw\x001e#3 MQ\x0018Â
ºwvñ´zO]i}FOaÕY\x0001\x001dê¥4ï\x001b4ô\x0014fníê_mYï\x001eM\x001d\x0015\x0007*R=Ã ÄlÀ\x001e	3\x001có¡¼\x0010ÙCÃ/nÿìþá'\x000eÄW\x000fÓéõß ûö`I¨\x0000\x001fMÛ\x0003§7Xý2	hUGNVû\x0003:
Sr½{¿:½\x0013È^<æÒ-UÞPÆ¿\x001d9\x0003²1V"2n;nÊ\x0002:Åùõ¿A[Ø\x001eÊàöðtFã\x001azÉPÂ£¿óë¿!÷B¹ëÂ+<\x0017#\x0017Ñk¡\x001fï¶Ò\x001d\x0002Ï\x0006ÝYSÖ@Ei\x0016ã¯BX±?(\åÝ|\x0005
[/Zx	#K\x001b±äwR[\x0015Ö$;D
9Ãè\x001e!ÓÕÄ"ÊqFGé,f9Ð\x001füêüôü\x001d[\x0015E½»ý§+Q³"ìe@wk£P÷6'úG¼»pe{Å\x001fæé'¾\x0010äQi¸CÎ÷Ü±<Í!·=¥á¢P+¿:v<vLèÍù¥u\x0010¸øB¸¶6>N¬àúÝÉè\x000e2}»¤BÆMe9\x0007\x0011}xÞ\x00172®¡¨A'ødnëR¤t\x0017n´ÔôÚÕ\x0016ú¡ñeÃÖ\x0016ZAMî#nMPÆQ\x0007lSÙ.
,ÓL;Õ;ÝÉÚêè\x0004µþ`ìJç44b4è\x0000½
ôì\x001bÄ w<w°\x001e:*s¥/\x001azj\x001av\x000eV\x001f:Áaà\x0016ã\x0016^I+6\x001fEHåúXml\x0003\x001b;ÒÙÛiÖ¹ñSèX$\x0013\x000eØ¡4T\x001dx
\x001bÌ\x001dy\x001fl¢Å0\x001ca'I½­«©úÂÞÐ\x0008jx¼\x0019:\x0003\x0017©p\x000bZ§\x000eß½¥\x000bl\x000b\x001eÉTýQóÐ°1°«³ÛÕw[ønVRýô<övr#û2<¶^5hØ&ÜÕnúîæÙgMYbjÎØzµA;}Î±s\x0012´
RÚÃ\x0019Y	È®x[YÛA»0·«*h»ÕAzN°r\x001e\x0015j\x0018{\x0010]hØ\x001e¾Ûz\x0018\x0012IÜ&ú)>\x0010Í«,ÕÉØCfÃNÍ\x0005ä~P9\x001fd¥Ú	)\x0015úGWâ@¿:\x0004=ôÅÒ©\x0005\x001d "o\x000cú-EªFØ$U0¿Ú&\x001e¶I¡T§½7]ÔþÝY6¦* îW\x0017!S«ºWZ/Ê\ôÝJ\x000e©b±Æ^¡Ïö\x0016\x000f\x0013ztXcw\x0001X:|ø³Ãê 
\x000e·É,jy5àaèÕ½\x0010à^ÈÖA»mQ¯\x0017ÆvZ~u(\x0012DaeìÆÖ\x0001@~8Qx±ÞÀ.÷{\í¿\x0008p\x001eÆHR\x0013;=\x0002¿\x0004]÷H\x001c{\x00076l§«+íÌ{)ÔÊ9\x0012+28ÇÂ(¼·ãjoG<\x0002Y³\x001e¾µõÐß­>Tÿrí\x001f\x001bá\x001b6y\x0013`ÖÃ(]b	À\x0013¼!Ç´QÕ¦ag¼áÝ;x>°NP"Í­ÄeZ;¡¹¹´ÖýFG\x001d¢,p$2¸ò V;aÐÃÄz0Ó ç\x000exi\x000fµÖ²¹ó0Ò°Ag\x0016Ñ8vÀLât¥ðÍ'I^y{Æ°D%\x0018\x0010NZg\x000f^EX|p\x0014kD
 Ãí²çO×i1à±\x0010+2áPvB{Úý°<\x0006Pj.7l­¨æìdÓòÐaùÃOü´WÍ2.
Ð_T:!ÏÏ÷w?~<8?_/#¦_ Þ+è(Þ3âSÍ1¤[âZt2¡\x0015²¤è À\x001cX§Rv\x0000\x0018%&Ö¹;/Í1²Ú ÓÅÐzd+¶ÆD>ã¤a<6ØZ,$¹­¯³i+d8\x000céî\x0001`:°´8U¢\x0016§
%V\x0005Ú\x000f=\x0011\x001b´ïêwi@nØ6cQ´(÷¯Ée^}v\Õ\x0011,|·`aâ
D8|w¹ÖÆY£
Û`âÖ~SlÒUâ\x000b\x0016±5?ÆLÜ8nüãujT\x0016d\x0005½ö¤ÈlÁ\x0019nPåË\x000bü¸ðâ\x001d/B2#û\x0019õ/~Ø«F\x0019BØ¾<¿û÷Óó¹*ÄluÇ¯NÏï_®ÔsG\x0019\x0006º\x0011¦5r\x0006Ç\x0004h}¸²¹2\x0003q#ëôs\x001b9É²kõ»^3ÉìÝ±\x0001û\x000bç\x0006\x001c/\x0002ì«C=»lª¯ÏÏÏ\x0014i]ëêfºIq¸\x001c\x001bS áI- ¿a	ì\x001bê\x000cZ§IO \x0019qÙ|0we\ðùz#hG­p|\x001eÌ\x000e\x0017nÐ¶\x001f*:EßYB9+\x0015SzmÌJc%ª\x001a\x0003
»\x0007\x0006ßI`²}\x0002¡\x0015&úòÌ:Ò\x001blØ@o Y\x0017\x0008êÎ¬ïE¿HIünUJE~Lf*¶WÑÜÜq\x000eþ@ØÎÉFXÒR?¾ÒmØ\x0016°9¡ÁrD°DØþÐé\x0017çÔ	
\x001bm\x0012MÆ­\x0017\x0004¼Å\x0017ìC\x0003Pª¾\x000bìßD!Ty%JEÑxYtñ1ö\x0018nØ\x001e°sF?e¬¨(F\x0013%
\x000fKo0ôXaØ £4·Ç3Áâ8-\x0002yò<)¹qÃ1~:oloéç
UúxV1öj)#°`(vË\x001eq+\x0004y,É!ª..z_Âõ\x0005vï.3¿M0°ÏØè´|iâæSÆ\x001e{66l`\x0006aF60weÓìÐÁÉêå5h$ïhÐ@ÞÁ\x001c\x000c\x0011Ì­ëTCÿlwXJSvwZm\x0004(½½\x0019´\x0014&%l%$ì\x0003÷S%F*6Fx\x0004\x0013èRÏ*£dzT: óXeÝ°¡ÊjøÍ¿/%7I\x0003s*·õ(±Mq±ÇÔkÃÔöHë<±Ì\\x0017$v\x0019H\x001b5¼\x001b6jÓrÃI'JÅàÍ õÁ	»Ö´Z\x0018¼üa\x0007OX±IÉ7Èu-\x0001^ªsZ-¢ñaÙä\x0008O©ÌÀ¶ò»é\x001a*Ø«XC|o¸Øì0×uHWÇÎ#¯b«+]\x001aK\x001b8,¹94ba#Èóß\x0012EÞk¾«\x0017Û°üa\x0007Ç¾5fÀ\x0010]|®yùþabqM=IÔ7pHÔmD%îÈ¯«B\x00108Jofû*{E/Bò\x0006Î#K®;';âùõ8Åµqwh³8±Ê\x001fvpnA|:f¤ê¤ÝH\x0012\x0019£ë,¶Y\x001cYå\x000f;¸à\x001b*D_"HIb8õÚ©W\x0001§Óx»p\x0010û$£Âth5§X\x001bäW>dÁø¥\x0013\x0018L\x0003?|\x0002vÖN¸§\x000en2èüØò[2¯N>?\§Ì@&6\x000c¹Ï!rO8ðk1¥º±U¥pX\x001dÈ2Yä
§	l6Ü.½éªIîÈÐù®å·öX^"Ü¬äKfª\x000cYCÅmî$Þ\x0018d>-Y\x000cÊsiî\x000f\x0014\x000b3¸\x0015´Ch1
@\x001bYÎå\x001aÉOb%'wC3`Î\x001dÚzhèÈÍØ¡¦\x000f´¡°\x0016Nn×ÛoWÏíÙ¶ã:Vß\x0013ìä`\x0004ÓµwÝ\x0015´\x0006kD|±# yÙ\x001aò\x00113q¿Þà¼¾¼\x001d@­à7§çóã§»?ÜÓNýtÚN\x001b9ìó!d%EHmiS½\x0015ï+E\x000eÅ'²ã¡øèì-S<ëë\x0004Í¦åVoa\x0013«g;²\x0003dÈÜ\x0013$²\x0014^¤rF\x000f½#÷º\x0016\x0007:8E¬\x0004«\x0018!KN\x0005B\x000e³Áç\x0006Üû4ió\x0001Ûc 5jWF\x000b¬áöz\x0019 )³l¶\ÛÃ¦!w¾ÑÄý\x0006ðÉ\x0014s£(\x0004ý\x00069©\x000b\x0007ÀpÔ4àÞw\x001cM8\x0012\x000f!÷¯µZNC\x0018_º_Æào\x0006ÖéhÄàºãY)\x0001mD·åö¯¿Ì\x0018g\x001ato<^xé«\x001e>ÓkÐÝQ8¤É\x00029á\x000cs«¬æ\x001b¦cz
¹;
Ç3b
¥ª\x0000EíBsÂZUe¦W\x0002\x0013\x0011Áeä>p&	i\x0008¶´\ÅPWqå+À
\x001dTè\x001d³Ì¨e¤5eÈb\x0015ù$^Î
ºoê`¡¯ ½¨7ÐWkik
\x0001ç#\x0011\x001b4Dx&NÊ\x0000íegº'\x0007÷\x0002În#x°Ö\x0000ºXÚìüéîtØ?Óa<
F¾QðbZì\x0010\x000fQ¹Æv\x001bÉ©{\x001d]\x0004,´y;dZÑ(ÞcCÀYËÛeWò`5>üàY9
§L\x0010.XÅåÂ4j\x0007¾Î
ÚÂLç\x001eÐý	\x0007Ð\x0004Õ»;\x0008Y{.uÌKä\x001bvÏË	Ûöb\x0005sßg\x0001«\x0004l7û1ù¬À>\x00010Ú]ö²\x00122§Î)\x000cµ}á½wUlè6£\x0014Ü²·ÞHy!\x001b\x00023ËÛo¬×Vìèá»\x0015ð¦GÏÕ\x001b\F\x001bÄü\x001b\x0019¬(\x0018¤Õ\x0016I°E\ýXöÙæ\x0012m"4"ûª\x0014W\x001fá£y$`ç\x0013Aq=\x0004
âedäY:¯\S-¢¡S=\x0016­µý\x000e\x000cÎéÅwË]Â#$\x0005|ñåå\x000fÝ&xw3á'2!ðRz+ÁËH\x0019aÌ÷IùÃ\x000eî²ørn¹EU'«Å@¦Êø.ö`ùÃ~ñ\x0018y×	5\x001b5m?\x0005¸	}Òõút«Wp&§Ô#Z\x0000wâ\x0006'¿\x0014£äwuð`òrUÁáå*ò<|§Ì	<¶z\x0006,
Øyã\x0007pc\x0017^Åv½\x000b/Úh÷\x000e#Nºh©vh\x000f@u´jx°Âö\x0002ÛuUª\x0018<?\x0008¡ú\x0011ý«v¥«â\x0011+CÛ-\x000bj÷S,Á¼ªí\x001dçÂËÌÄj\x001fFØ6¹ï_Î-4ØÜ k\x0003_ªÊÃÊÐõ)ÂØ¢#¥ÑJ\x0010I8Úóhq^í2× f!\x0019a\x001b\x0008É¸øØ+ð1\x0003\ÛiÉ\x0019\y80\x0013Ú®
´]­á]bÒ"a\x000bZ¿À:¢\x0012\x000boà\x0006s\x001ef¼\x001a¢\x0014ðÅ1n\x000c\x001cã\ÊP\x001aÀ­¨ÇÐ\x001fÁ«:ô¤Û°C·!å\x001b\x001afÆ#\x0013G±^°\x0005:ìËzÚ±¿j\x0003Ïxf	³³Za\x0016Q;!p:,ÊÍXÊ®à0;\x0011w°ÉéÚ?\AlîÈ-Ø\x000bï4\x000e½K`\x0011°ÝÁõ5\x0016ø}¡&)à\x000bï,è\x001f®@ñ¹½AXÅH÷L²þo\x000bp\x000f±\x001bÏ÷îQ:¢`\x0011cB\x000ciõÍ·Éu.-*N\x0006í­\\x00107Z"~C\x000eøÙ¦×\x000eî°¼ÀÌ¢\x0002:VíÉðÄ\x0006­a-}Ä\x001dî­x¬q,l%Ö×KßÊ"	-\x0012qz5Æ$\x0005(èÄ÷H\x001fu(\èV-N\x0015\x000b£\üìl/Î#©7l³DðÑ¦r\x0001qãæ\x0002<#¸+À\x0013ÒñÚ,&x\x0008;pÙN\x001aM+64FæZHÍ¹Ø*YlÂ\x0002]ÈÆl\x0005ÆÈ5õ>_<w8 ¸\x0011:ed¥\x0016<!ÄZ	Ã5ÓÓ§û§ÇërN1
\x0016r½ÚééfW3º««lÐ¤¨\x0016ËqðLz çü0_µIÌ³¥ò¯,\x0015ýk«ç¤äÅ­¤è»võ\x001cC\x0011J¯G)¾âí´Å-\x0008SÇâ`ð~ïS`ü»´ñ\x0016Óªlòä3\x0006Ã¡n
Nó\x0015Jöw+Ïc\x000b"\x0001OF\x0019üÔ¹®ÿ\x001fÎÏïïÏÏ×deç>
ø\x001a\x0018:+;W"ûÆÅMI'SÒ<ë\x001e\x0016h 4æ9&øYV
\x000eæ,­íâ½ \x001eä$}ÑáêÞÌ/&\x0018ç²AyT~¾«³W+ät)òHÀ³A\x0003Ï
BmÚDMñ$|gòy%;\x001eD\x000eß\x000c=^åñ rÈÂÀKjøÄJ¶ÎAdÁ§õæìxP9ô\x001c\x0002i¿s\x0007è ¤{è«u±õ$t\x0007\x0011;2ís¥ÅTûñ¨©øj3c|÷È¤ò
\x001fïþpÿ\x001d]àwµ
ÿþåã\x0015\x000f
ã\x0004¸)B@Éx¨¤ÿ.Înidb~EL|ÃJv1ï9¨ëäÿF¶õM¢¸6
³YLï
\x0019\x0008\x0013ß \x000c1làâá\x0019üéåþãÝgÏ\x001fNï¯8îæeÓeÒ¹
Ë\x0018ÊK Ñûìndå\x0017uc:LÃ2´ 	t\x0013­e\+C£\\x001e\x0004ÆúCæ(Í¢\x001c\x0012*É\x0004íe\x0018k³èX©Ú aJ¯Ü\x0013=üÌZ\x000e\x0016+/u!ëóÞÀ7`øf>o¡\x0015ßÛ\x0012âôoNF¶\x0012-h\x001b44¢sô786GÂô\x001fódûvÔ¥WlÌ&7h\x0018HóÌv§\x0011e~x ÍÊ\x0001\x0002[8üÆ\rÎ\x0008\x0005Ãgô·Fi9\x000c\x001d]­
¨\x0015[C\x0003jPJ`\x0007qoZ¡_]+ÓcÑ¡AÃgç$Zü/Lº"°}í\}54q\x0006
\x001b[$aå ÝÑ"µ\x0004»r\x0019Ô¹äQÂNæ¬\x0012iÃÆ¦¹N[®°ÅÖV8èï\x000ecí´µe/1\x0007ååze\x0013h\x000f
Q!sµVæ\x0018ú ¾\x0016sU¼[ÙÛ ½çGï«Çv)ò¬°q$×Fä¿â\x000e\x0015l%f6¨c#[mAxje¶ÒÝÛìmÐ¤(9Cbe°\x001b£Â
\x001auEÉ\x000b]ÿlGq0ñ%(eí+KÐÂ$Øu\x001a\x0003_¯¶8ÛÊE`ùÙå\x0011Í­üÝ¿'mF?\x001bû|Érî	¶\x0018{e\x0012\x0007&á\x001e&à`\x0015µ;ä\x0004v%	Z!#m\x00123w\x0001µ\x0011ßØC\x001fÈv´òÑn1\x000c\x0005®ß\x001fökÿ:
\x00136kñj+[/ÝA	_@7Ï«0\x0004¯dG\x0019¼.~Ö«\x0016\x0019'\x0005{\\x001fOçóÝ\x0017ïï
%ê5\x000bëDýßfÇ±W
°£¿IÒÿ6ÜÐò,Æ|å!;\x001er\x000bEÇw_\x001e§\x0012v±s´à´Y\x0019Á!ënÀ=ëæñ¬N[©Yª\x0014µÐ¬\x0017ª\x00186ÇBÊ4nÈ|´Òt6\\x001fEÿ\x0003}ð\x0001Ø­R¦òâv¢Åù¡Ìø^©3Ê$Aql¸É\x000fûe\OSyà\x0015Êa]Ø²¹ú]¯Úd²68\x0011ñO\x001f~8}üXut¾zy¾§¹îë\x0000\x0005Q.Í¤ÝãéÆÇ«6[X\x001dÈÇ¤íùG©0ÿ]¯d\&\x001dAKç·O/ôå=~{~|<ßýöS©\x0014}z¾\x001fÖÉ»7%ÿÑ\x001e´Þ¹n(é¦9@}éZºZ5Á\x000f±5´\x0004¨ð\x0002ßI\x0005½
tuFQ!&\x0007,,#·â\x0006
ÜVSºÑûÈ\x0012E»øÎÎ\Gâm6Ò~ûËLÕ¶A\x0004¶f²ðÌ5QzVR07ú\x,Ý¤7è¤³k¤a\x0007#ôÌSN¢g/\x0006Sz/ÇYå
\x001bg\x0017ÛèÕ-X~AêÙ.má-[í-\x000fÅ÷d
ìýtè·a#O+ó\tpâ(øN\x000f_\x0004k\x001eR¤
9cÄÍhìµ\x0018Nd]/°³ª}+lØ¶lfÅôv¢(]ìíd
aC\x001eÚÇ\x001a6\x0012ÄYl\x001fãiáwkø¨Dg\x0000-\x000f Vl1ÊíbÝ%ý±&âd/SÌô]å\x0005dHe6l\x0003©·¾\x0013ÄÄ½ýXã¼\x001d/Ð¤­s\x0002\x000b£?4pJ\x000c±¥!\x0018%Y´Ç1Ï:áx¨pmà\x000e*\,×Û\x001f1\x0013çd\x0001÷·²QÓÝ_ÀÓb«?lààà%\x0015H(x+Ô¹[ÇûÊ\x0008í·ªsu¾gb÷÷ß^®¬s%Y¿\x000flÑ
[$ùen\x000bCiÄÏfcÊØ¯\õü^Å$\x0006¶´IÔ%Êó/£´Ê\x000cÒ:!\x0001õ\x0005ïy!I¯.ûÆô\x000c\x001aWA¿ë\x0003-2Ò2°\Äúð~Ì|v\¯ñ+»c2`¶ãÂH+ýÏ¡BÈb6Jà*É´Lá¼\x0018ïÈ \x0013e\x0003ÖP4wÂ\x001b¬EHè]¡\x0000\x0019\x0011\x001a´\x0005#Sfà-@\x000bNW6$Ðõ9Þë\x000cäÿûlËÝ×\x000fgú78?^iÖÒäîéã\x001a-S`5oÛ\x0013O>«ý
E.a[%å;PiÝî1\x0015\x0005gQtéYåô
Ù¤n«á²Ü {H\x0015xð\x000f\x0004j¸;añGY)Á\x000cÔ%8Y@g¦ \x0013\x0004{Ê\x0013KÀÌBz \x000bûËð¦²CA~\x0001çè`Àa,Qs&sÔ {|Øám"p¹vÍ£æZy\x0016\x001f}	Éu\oek
¶æ¶\x0008Ë\x0018*quÇ\x0016A\x000fýç|¬·ìÈ}è\x0019Qì%%±ôÒ ¦J\x0001±ë\x0006\x001dá£S@\x001aï\x000e\x0000AKm$f8\x001d\x000e~~8¼|8ßýêôôr­Ö\x0003¡çég÷\x001e%î,ÞE
\x0013?ÿÉ\x001b9\x001d\x0016Å/\x001cW¿ëU+D+7®ÐËÝ×/?^¥<@0¼à\x0011\x001c³k"Ó½
'E`\x0019é[*·Í»BÆþj6â\x001f\x00059}àaýQRYE_¸	"4ò>TbI\x000eU±!
ô_Ã@H9ÉÓ³l%`\x0019I'Áæ©g¾üø|ÿíéùýuVßÃTdqgH(ç`ÿ\x0019¶*@ÞÈâ/\x001aCfëSâ*X\x001fÏí}R4n]üÝ&FÚÄÖÂ8ÚµaÃhW¢+2q%\x001aæ,EmÂÛxzCØ±8T±}/\x000e±B§AâA½¢Å,J&ô½|¬ß=ûmØ@î\x0017\x0002\x001eVLÈ#G\x0002(}v\x0002¾¥j\x0013,°#`Ó¦ê$H1Ø\x0010$»¿çw­¿Ìô\x0003\x001a6Ü¥]\x0006|M;)KÉ±ÀöUÙ~xÔÝ°%o±ÿ_u¿ÌXÛ6h`m\x000b,\x0018Ö;²)TR?©ä\x0011Q»8Æ´
®#\x0010úÙVBG\K%[ÅéXÔ\x0015|±\x001a5æ¼M8t\x0019²\x0016ÓQÖHáÄ`êÐ¶+pk1¦±°S¢YJ'*!o\x0018|\x0002Õãc÷
Ý¡PíôåÌ,Ñ=ÃIlðà¼ª5±Ì²a{ÀÖ¾7D\x00106ÓÏa,ÈedLóK\x001b8Ì/{XÎ¨,5#a-ôc\x0006³C\x0006£éâëgJä:9*l\x001aúo²4¹®_>p5ð\x0008à¾¿\x0010v¢å\x0007éåÇR\x00156c3GÅ6ÐÌ\x0011#togüåÂñ¹I³u¥¹1#Eë\x0006\x000e\x0014­V\x0014Ý×SdHÞ%9gl\x001dv[XÅU¼W\x000eÝ2%Çhrc\x0012_n+w	c*SÁ\x0003\x0010?Q´Õr~¢\x0016;ÑHaûÈá\x0005|qØ\x001a R-³1\x0019Áxþ"ð#ö$ ¥cU> ÿöGbî~qzùî|]xÍCþ¢BRæä[C¾G,ÍÔ|·\x0013Û.¾íEÖ<¤\x001d!
Ù%öA0ÕIËr"Å7zBz´#÷Ñ(.ª£Á\x0014§«StÂñÿ~2\x001b±\x0003Ãl\x0004\x001di¦wO)î\x001fÅU²[Ò¹8ã<Ú{»CYã,Ö\x0018çgûÃÌ8\x001at¿Á=\x000bJêþ\x0014Lw¨8"4K¤Ë\x001a¨
*ïÐÐ³Î\x0015`øê c12¼ì¯£\x001b<Íæ9vhç\x0008 mB{ÃÓ\x0007#d±r\x001bB\x0019ê 
9\¼Ú\x001dÀì÷6äñ\x000eÙû\x001dòVäÕ\x0012\x001as)òj\x0005
Nä\x0000\x0015
Z%A¥¤ãaßÑEY.ÕÕ\x0012p1ôj
Mº\x0014z¼«7h¸«ß\x0004=ÞJ\x0019ß¸*(Oìý÷ÿü¯Ï¾ù/©XÍ`Ë¿¯~k-	3øÅ¿ä¸HwwSç!í|;CLÒþsZÈ®ò¹~8Çi\x00059\x001aÄÈ÷NU'òWÈ¦#S^¯\x001c k9¥5òt2òt\x001etG¶ðÍ®Ë\x0001\x0010²Á¦æ×b±YùÙWCv\x001d9)ñÍR5¿9\x001dÍìÅ«\x0001{ødD%à#+Ë¬\x000bäfÜ;ò\x001e\x00068Ö§s½ý[E{¢ ïõü8>\x000f\x00036à$¬ÜgëX6\x0014Ûøù\x0005\x0019\x0016ýËóÁ\x0018\x0007lÈ\x0019>ÙC­|É\x0008r&úä(¿¹\x0011/ {\x001cP¼\x0014¾Ùa+|Ù\x0018ò©´×+`
ß\x001cJ@Ú£/ðÍIî9\x0013JÚ·ÚÎù 1éK¬Þ%hxµh²gR&5êÜ¡û¶K\x001bk`æ¤[ø \x0010ðô%E¯ö}ÇÓ)½Q5¬c\x0014Ð\x0004»­WûCÃþàü\x001dVQw\x0012Y¶`¨XÍj\x0015
¬"\x0013F@l\x0018\x000c-í\x0011rÍWÐ°:Á«jªª\x001d7K\'Eæ¨GÞÃßî\x001f)\x001b{z<}ºûç§±Ðü¶\x0017 ÇÅ\x001dY\x0017²í}8f-^\x000b²þ$÷BHJó\x00185eløÁ¤W']0F\x0010½lvü²Xê\x00086\x000e×]\x0001/Ø­u\x000fÂdÔåEÅ¶\x000cop9>\x0011Wl×Éwt×
ÁoUýÃùúõÉT«+cµ¬û^-+ò.\x0019ëÍÎ+¡ÞKà¾²ñØ¬à¡\x001fU\x0014¤\x00179\x001b\x0016sY"yà\x0019+\x0006\x001fõ^6pÐ{)½9½W+Dë£0ðæ@¡g±ù¤½G´¹0\x000b\x0013\x0001+\x0001nô P)²\x001a\x000e
{\x0004CA`\x0010Ì^Ò£»¬\x000f\x0015JUJ«&»\x0015¸ëà\x001cµôêgbýLä¶IÖ0\x0005ËvÎÊS±\x0005+\x000fKÞí¼î1rÕ!\x000fW²íó&\x001b?V+8t
\x0016±ÎhÍR@b;¶Bð\x0010Êp\x001fÓ\x0016NÁË\x001f\x001axH\x0016bµ\x0016ª\x0015\x000c	ó	¹Ù\x0011ãpDSbROé¯NÏè?q&Ðá=øm\x00075åÇ²âkÒ~P;fÃéuÑ\x0010)¬²·Ã\x0012ÀµêI\x000b^\x001cO\'û5MÛ\x001990³ö¢ä¢ï1.1ã8:Ç\x0006Ý¯iÃº¢ý@JI\x000cb:eÅÜµç\x0016\x001a"\x000e!QÅÖ\x0010\x0012\x0015-îy\x0014LÅ¤·Òój\;ñÝ}Ã\x0019\x0015ñ¡'\x0019/Â-eå¸\x0010]ïUyÕ\x000e
Û\x0006°ê\x001a\x0002dnÎ(\x0004vGó¥È\x0013sìØc9Í=G})9\x000fBÊD:]äRR¦ÃÀ
»\x000fÕrË\x001d^.LQ/ü  ë \-\x0005Úô«Å²(\x0014<À\x0006¦/\x001eãEÙÝ²Þ[«¥4¥ì\x0017K!Ç]bM\x0016ÐqpõÍ\x000eÌaÛ¼\x0016É«:<¤\x0007kÊ°®\x0019x\x0010\x001a¶¿\x001c{|$Ù°û#S\x0001æë
4n\x0010íµ\x0004\x000eõ\x000e_\x0019º?í¸2°\x0001ÖZä\x0014ø~kZÄ\x001aí§Å9ÂØ±ih\x000eìÅÌð'öõÃ±moÃÎðÝ:Âø\x0019Ç»¢\x0012\x001aùÙÁWÊ¾­­\x0002[gÑQêµ%\x0017O`­¿Ìh¹\x001b¶Ø\x0018ëç++°½ôXØ4íjÿYØ%\x001aCª[¡LØQ\x001eÆTÄÕþ³¸ÿ¢x\x000eA¾þ3ç®ünWû§W6qh\x0013\x001e\x0012îßÍl\x0011¨Å@× \x0001
:à¢à9¶\x0007¾µÌ\x0003¯ý¢\x0002ÇeRA>èê¢ÞãÝP\x0007Û ãO\x0001?ý~÷\x000eòY&·$ý£\Á\x001eêJ
;õÏfÖ*HfèüCvQ.ç\x0008skS\x0006¶èç-°}îØä*\x0010\x0011yVÕÀ¥TÐ>l5«3²a÷mÂ#Ô@ÞV°ál"3<Æ.K¹òxß=ÞfcðvwÙ¿Ã\x0011¶,c@­ÊW§aÄxCN}ÄØr¡ª3]RÈ±!ÞRD/(niV\x001et;ßå\x000fÝ)
TKb\x0005ÔÜ\x001f+7 \x0013}\x000c!uR³¦×5¦þx÷õßþçk³3:¡Éîu%È¯\x0003@)¡¬\x000e-âm	\x0011ùYñc(OM\x000fÕxk\x0015ÌÖ\x0019\x0017hªVL²\x0008&1®2ï´ò\x001b6ÐÊ;.vìÛÀ°ª\x0018JP)ÄÙlXpf>\W¡a¸Î²Èe¯j\x0017àáY{¼¯´O}<\x000b¶\x0006>K10\x001cr\x0017\x001eÂGúGG\x0011r'Hm¶Y|¸ªå\x000e¾ÞRF7ºFR\x0016Z\x000f#wàV\x00189*¶\x0001Î!K\x0005s\x000e|ÎH
 ýNÛXh\x0000Í$ÃßÀ%oÜ±íÃùÙ\x000b\x0007à¼$æzeØ\x0019\x000bY\x001b8Ì\x001cò#PÏ¾èò\x0013[\x001cSv)h
õwm*¸AÖ\x0017Êå4²ëéäLæ ­÷ÆJz\x0005\x0017L8\x0014Y°ùRÆg¹ Ì\7uÙCûxÝã£î÷|¸½<\\x0011Àð¥Ü?©Pí\x0004,¿WïCâA/u;¥Ew¸Èé½d-¶p\x0007#>Ó\x0018®«
øÒ;\x001c 
¹÷\x0010$£eÉRtÍVtëJ2®Ú\x00052d\x0012
¸Ï%:)ö¡P\x0002AF9/úm¢+óÃC\x0014×\x001d\x0018CuYÊ\x0016d\x000c)FLÈqöÙ{W\x0013ÇhæEï3e¸*¢s7\x001bàkÈ½ë!¹ýR6D$q§\x000fó{Üë7{'mÀ½]%¤Å'[AÇO¨9|r\x0019I\x001e\x0002ÚÜ»)ø\x0002uzFvÂÌ>\x0003r=6äÞ0Yñ\x0019hÀås[~ó6\x000b5\x001c\x001b44LÑÿ\x0016\x00145N¶±Ò
\x000eJ«Ó§Ò\x0006
>È®\x0001Kèxt$KÇÃW×6¯¯hð\x0015\x0007hÎè\x001dB')÷\x001cè»SØ*|gkÝ%/w8
2µoãÌ\_ÆË èÚ5³âý®\x0005\x001au¨\x001a£·rðÎÙ+Ã\x0016§\x0018¿\x0004ÈÕ\x001f9·D{ÐÞr³gæÛjª\x000f\x001d\x0003Ì
\x00140XÑØ\x0017m\x0010Ì
\x0014\x0000ºé3ó\x000e;46=¶\x000cNP¨©E\x001bfäÉfrÀòÓ'Âh3\x0011P¹Ýuz~?^êoÜZ:Â#3æ¦}ki\x0014«Ô\x0006äFX^å§{hÙ ò¶É\x001c¬ô§u&u\x0016¹\x000b¥\x0005Jn¯TBÒãm³#}\x000bW Ø}e°ï[Àæo\x0016H²£{GÞîÌ/|\x0010é¦(3ôßj\x0001³¯
º¯9;
\x0017eQcÉ»íaèY¿È\x000eÝ-\x0003¶ë}	h\x001f¤=BQ_\x001fÄ\x0006ÝÄÌÕäÐÙ\x000f¸\x000b0@ÃÅ`ÅÛ\x001e]Uímà¤Ù µ\x0005èM\x001b¤A{Ùµ\x0015)\x0014t]\x0014÷éCÀ½'\x0015ÍzC]Z>Ëj\x0015ëÑ½Ç¼*Ó}Ãv\x001dì	ý\x0008\x0016V(øÆ$i\x0013©°\x000co#
;Áwóèw_Éì2ÒkÒwË	2ªÜ \x001b±\x001b¶ó\x001dµH5`[\x0019±F.©
l\x001dkup±û\x0004\x000cc;`Y \x001dH{\x001dkß1§¯Û26z4ìØ±\x0003\x000b\x0006¼=[Q¨Hô?8­åíÏ¯¶·íÍ5\x0010
g¯®>Ú×R´"h\x001eíÜ%ù0\x0001\x0014ô_<=¼Ò£²aæ*t\x0008¾9Ú$\x000fóôÇ\x0007°ÜßÌ°@9Èümõ»^µÉl¦sÀ,%r~þî|÷ÏO÷×\x00131L|+êrÊ7úÅ Éfã|e¦¼¥úyB2lRÄ2\x000fµJù0	¤dRÚD¼u&Í²¹âz#qNry\x001aÊò\x00052\x0017ýMàêý\x0000núÙãûç¿ýõîóóÇ÷Çuc+ºÊâÎüþÐ;«\x0015¨Ö%Ú½¡¾E/úpø³\x0019%\x000bS&¯(XhÖ\x0014B£0\x0005÷_&|û
Ú\x0003´1°òL¯-¥SèÂ\x0014Ór·y1oÈ\x0001\x0013´
$~Ï\x0012,Ê·²H\x0007ÅL
\x001a
ë\x0011Ù\x0008ÚÆ=¼¤­Ëº(ë\x000c/N
\x001aÞ#Å\x0007ým<y'è·	:X¹ÿsâoØ\x001aÝ=\x0008ª&\x0016~ðØ¿KÉ[Ûlò¸\x000bhhh¦8ñ\x001dØ:jÉ«RÐ®êÀ\x000eï\x0006Ý\x000bß<\x0004,4á\x0013=yZ+A L\x001d+gÝ
Û\x00026\x000f
Gøî,÷Èa\x0016"f¯êSÃ
\x001bÆ¹[ºk\x0013\x0012¶`©äÞcñ²Ãøu yenôf
¨ýL\x0006\x0011%ï¸=\x001d\x000eÑiÃÎ¤\x0012Dbfd9¼¨üäÒÞ5¾04äÖ°ï\x0012 ëpXE¯å\x000e©y×\x000blØðÀ@Ø\x0011Wûì¦\x000fr¤:*<Ôã\x001a6\x000c.$£½:1B\x0012;$hÁb³Ù^F\x0016Ø\x0006±=¤^·e×{\x0008Ò&yR5s\x0001õ\x000eEèóùéã§û÷ÛSÆÓË3³_)ü1rúÚ²Èq/aBÇµå) [È
fÚ¦>8]¨\x0016ë>CÊiyB\x000bÛÔàcî¿Ú2l
¹¿xRDfjÅò(H\x0017¬\x0017\x000fÖWÖ!·jÐ\x0011_\x0004<t0Xv\x0015ìó3FöUr_á]}u¯æWB°\x0007köÊpP¼ÓZ¾¬æ~ÅCÅ¼û}Â\x0001"Û4ÎB®åUË\x001b´\x0007hÚÂ3Yak%ôöt½²\x0008\x001c>ñ<+|vTè¼ÆKc§ÚE8^U\x0015ÛÀ\x0000gâ
G·vfÉk±^-Ø¨7Ùâ\x00156ì¿D\x0001Lï­(ØX\x00143F\x000c¥\x0010tU\x0013Y}6px¾©ú¹os4ò\x0011FGqîÛ\x0016m
\x001b>;Æ\x0004ç¾eÚVì35:ÈC*&;Î´ºàÕ¡òóùÅ÷§OçÓË\x00149:*\x0001ÃU\x001a]ìRWI:ZZ£³J
øBF{#Çç"yô\x0013N\×÷pÝY\x001bg\x000e,J1ä¤]N¢âÔte~3Eç¿üñ\x001d¥©öôç+´¨¿òÿ\x001càéÌµc!Á\x000c< ­\x0013àî\x0013YáÿÝ¯ï?\x001eÞßßýöüÝhÿ7"¬"£ÅÆ-\x0017yÚs×PÊÑù}C´w©¡mÍúGÁÜÉ´í@\x000fO·¡\x0011«å¼\x001cW^Û©\x001aZ\x0006míÄ=ùÝfÜ\x0012 TÁY\x000bD@«*t5FÞ\x0015\x001b"ïÈN\x001f´Qì8Qè\x000e-l§]\x0016½Ål\x0014¥½pÇÉóµ\x001aêÎGt¿¤Ò
Q~	??@~ÌJ¥\x0003ùVvÖ¢Z14ò³-ÿ(\x0004JSWm(oÐÉÏ!|@L¦\x0004&#ÍÔ
4S$\x0007èdåÿ+ÖÀlé·\x0014ï\x000eiÞÈÚ »GèBqÞ_j¹	:Bóaü\x0008\x0014§}¬
ºW\x00154·vÝRZú·0OòÕ;Â¸`1\x001cë\x001bvîÇºöd>]Ã\By $#*8§ê\x0018{\x0018ökØ}ØOGN\x001e:6S¶A·^T)\x001f\x001es-\x000cqÅÖ\x0010\x0019Ó¶ð`fb$ä|Ø%\x001bÿÛ¨ã·\x001fwØBD¯\x0006\x00075Ãèà8<!US\x0008¼\x00007½£@\x0019ú\x000cs\x0010gåö*Q2W¹rê,,^þ°xN¸S¸j\x001aÚgùÐhM1\x001bÂã
ÛØ\x0012=ÏºT\x0017à»£W\x0007R_\x0013WÞ£Á{\x000cw[ö@S3}\x0018ºO¬\x0019*lÃ-®\x000fCê·\x0007P×`UTô\x001fdPò1\x0006Ñ¤Ä¾Y\x001b)F¾°\x0006\x000eò\x001aË¼ëSôÏUx\x0013r§xÏ_¡PEPt»\x0002\x0007ì{g\x000eK\x001b0\x0002^¾ÛQdUÒë?4p¦È\x0016\x001a\x0011\x0007ë(C¶²ßnæêì³Ú³Õ\x0002ð¿ýõãý{¾5î>??Ü}v?ÜWÑwäp{å#smî]\)yÅ\·µc³ÃìxèS[ü®Wm2Y\x001f\x0003³µÿúòÃ\x001dkâ~x¾ÿöéùñJ\x0005%ë.1Z·gÀ=\x001aý\x00120z\x0013?¸íÕ9>§Èç´ÅïzÍ$Å8¥ñð´ÍgÜ}ùôñüÃ÷WJP`C,Z­6}hË2å@¸µY<u®\x0013½ä:Yü®×,ò	Z\x0003Iý7\x0000ÜôÄ$ÇüÅéï\x001f)iÕ×ék£JÌ8éd];6¹j=!YÕ\x001e[Yü¹cºqñSQ\x0014uûâ¯~Ø«F\x0019WIã¹«ôßÿó¿~ýô|ÿOw?¿<¯¤-B{GÔéø?ïu\x0004Vî4\x000bÛôíÇ,Öj9ézvùÕ\x000f{Õ(µ²0\x0000òkúÓËöòû§çW\x0012ç
\x0007B\ãUhý=e­{¡Ç\x0004\x001e\x0004¹t|±@a=%ÿÈÞ\x0017¹øe¯Ze²BØÏ+Î¼w¿9mÊ8=ÜýîÓÖ÷qEÖkÒ­)+\x0017^HÑ4Î\x001a17¿h\x0013¯ª]¡Í«Ö?ìU£LÖlqO}}zþÂ{Zµów\x0013·¶`'Áu`YÎroU¶(ëèè\x0018)ÅÇÛ^¨0P§t¹«B§N[ý²W­2[©<_©óË\x000f\x000fÅµRPw_|_ÄÿÁUÊëôSYmErK3gí5@¶\x0019y"²³uäñF\x0016\x0012eýÉÀL{\x0008ü\x000b@ö]Èh\x0012\x0005³DWÜl\x0016n\x0007^J¥´\x001d8©2#Ý-ëeíùÙ0Ül;²AjÈì\\x0012SZVÇ ¸\x0010)¹Q{îÈ®#o=7
;Ý
ZÃI:ËËò±h³#ÀCÄVkÚ>^\x000eXs`­5ãtÂ\x000e\x001c:pp ^TF¸¾ÌQ\x001dÛ wà\x0008ë§ËëÎþÅ¦yÁú	_¦/6q2ö°#w-§5H/ðü¶`Ó^.Õy6°ÖQqL)4evYÔÿÐÎJkò3\x000cTìÐÝOXVµ×Ú¹ÓRp´S&%ÉYéÀ(%½§hì:Æ\x000bZBÙ*`?¢%¬%Ô§ôQ8&x\x0002\x0002â)NXÚ
å\x000fò:P±rNK\x001e¬\x000f0\x0005\x001dsF\x0000²2i<\x001agó%;rw\x0015k°W£èÀg-\x0014\[ìV¾Ò	ÏER%:å²Ê
Î\x001c\x0012îÈÝY(ç/¢¦<útè(×0­c\x0005:4ëvfy@\x000bUÁ,iCãÖ)¹rD
Rw	Õ2ó=Cùi\x0005t\x001d-Y9"H}ð\x001eÆ³ÿè!\x001c,=Òè}V;öæAö×÷\x001fï>ûó\x0003ì/ÏÏO\x001f®\x0015y#(\x0017X·½Q&îèÇ1±R\x0007ÜH\x0004°\x001az\x0018Ï\z§:óýê½fqµj\x000bÏ|µ>ûöôíýi¤,x[ñßqó(·W\x0016|\x0019×ì½¿,utKQõ mà,:-Kgz/ëCWiJHÚ$¹u\x0019ò\x001eÞª\x001a4ÈÏ°É`P¡\x0005Qº\x0017³T¼\x001fÙÂpe6ä>ã­èúÎô° ìÈ®\x000e\x0000#4\aØ²
º\x0013-0«eß²©bo°/ÃÔ\x0000\x001d8A\x0018îÌ\x0006mÁÔ\x000e\x0018_
´ÐúñF\x0012Ç7èáÎlÐN¬bÂ¯Nr¾À[-w6læivái[¹ý×/¬Îs¥\x0003QòéìÃ~ \x0006\x000e¼{-Rö¿·\x00107Ù]U#¸\x001f\x001föM&Ë\x0014 ·½Tý«\x000c§+µjYkD»7¹<§¯õ\x0002ÜÛ\x0008ãt\x0003ßþÞx¦\x0003wËêw½jÉÚ¤¹\x000bm%»/Ï§Ç\x0012]|y÷Ëóóó0QùFWÒYËèàUk´LL\x000bÛûK+ß\x000eåÃªx7Þ\©øíÏ\x0017\x001föªQÆ\x0005³z^\x0012úÃýÃÃé»ÂÌñ»§óýµ*A	àIuÚi\x0002E@}E]¡¼¥AÿB\x0010\x0019ôàYõªIf l.E\x001eîêl/E\x001e®êì.E\x001eÒÛì/E\x001eÒÛ\x001c.E\x001eÒÛ\x001c/E\x001e²Û.E\x001e\x000e/E\x001eËL\x001b4JÁ¾\x0011zåúb/\x001cËL
úb7\x001cëL
úb?\x001cëL
úbG\x001c\x000bM
úbO\x001c+M
úbW\x001cKM
úb_\x001cKM
úbg\x001cKM
úbo\x001ckM\x001b´¹Ø\x001bÇ÷¬\x0006}ù¸òFs±7\x000e*C;ôÅÞ8H\x0019îÐ\x0017{ãÐÌ¾C_ìJâ\x000e}±77½q\x0010`Ü¡/öÆðy¾Ø\x001b\x0019»\x0006m/öÆJz¾Ø\x001bíÊ\x001bíå!êÊ\x001bíÅÞhWÞh/öÆ¡É|¾Ø\x001b\x0007%\x001dúbo´+o´\x0017{£]y£½Ø\x001bÇ\x0014¹A_ìÃTjv\x0017{£[y£»Ø\x001bÇú[¾Ø\x001b\x0007Ý«\x001dúòqåîbo\x001c&xvèËsÆÕ¾\x000e\x0017ïë°Ú×áâ}=©4èxñ¾\x001et¥vè÷õ ÿ·C_¼¯\x0007Éª\x001dúâ}\x001dWû:^¼¯±·\x001dúâ}\x001dW·L¼¼\x0018²ºeâÅ·L\yc¼Ø\x001b\x0007­\x001dúbo\x001cæº\x001atºØ\x001bÓÊ\x001bÓåõkÃÖá
ùÿbûñ\x001f.Æ^ì?þÃÅØ
¨/¿\x000eôê>Ðß\x0007zu!èË/\x0004½º\x0011ôå7^]	úò+A¯î\x0004}ù W¾üRÐ«[A_~+èÕµ /¿\x0016ôê^Ðß\x000b:­ü2]îiåér¿\x001c¨Ö\x001av¾Ü/óÊ/óå~W~/÷Ë¼òË|¹_æ_æËýr nØ±/÷Ë¼òË|¹_æ_æËý2¯ü2_¡d¾òË|ùÂ/¦ðíØ\x000b¿4¾$Oþ\x0016æu¾¸ÿTfð\x001fÎf*Ý?ï¾æ\x0007ÿÓó@¥ûÖqE+¨\x0007Ñ;Ûu4Ýq\x0007î-MÃÍç'å2ëd¹lõÃ^5Ê¼¦µAçË Ç=à`\x000füæéÓýÇç\x000fçÇOµ«	±>î\x001f¿=]©OÇ*ÑCäãNÿ­%ÚÒ\x001c[7Ö\x0015
Ã\x001bÙ\x000b\x000b¢¢ÑgÝ\x001fî;¤·&\x0006SoC\x00166É&¦i÷Ç\x000cÝÅ¬¯\x0019;²"¸,\x0000\ÖfÞý±![@ö0mæ]Äo\x0016R².å<\x001d\x0003jÀ\x000euÛmÀI¡v\x001e\x0001;i¦X;²\x0017Ü9m¹T\x0010Ñ'Ë\x0001áTjÆ\x000btCÞ/PÚ\x001aæÓ\x00089Ñ%æªw\x0012y>\x0008Ô# GuöÆB\x0003îâ¥5lO\x0019/Ï
9uä/b;ig#ùË\x0011xÚû±\x0001CÓ\x0019K¥\x000eÌíÒ¢£=\x0016r\x0017jb5èÞûAÐ\x0019hf¼vYt\x001e\x000fÖ!Ï[?6äîÆw\x0019­\x0010X÷F0@\x0011®Ï\x00175àîõ1ºhæF\x0015È>IkD?ïûØ»\x0007\x001aÌ©#DUèx´ò£sÏ\x00175èîÆjhôdî2¹ëä\x0014IW°\x0013ö¾\x000fN'­mhPîí!¦ShCùQ\x0006/ô\x0019T\x0008ÉÉÎaDë°KÁÍ®½0oOýåóÝW÷tô\x001eøò«Ì ÷ß&·oä\x0004Pù@ÑgCë(Îô3ÈP³ìþûë(&ÓÊoõ»^µÉdÉ^E*w	§õåßëô¨ª\x0005»\x001fùjL8.$TZK~#R»Åb^±øÓ\x0002-'2ª\x000c&èw\x0001\x0015s*\x0012Ø(zÃ,¦8\x001d)n¸¶ãFWH\x0008½h\x00138\x0001\x001c\x0005'ad±×é\x000eºd.\x000cú+É;I{¥r\x0010ü1¢	:5IË\x001bß1\x0006d:k\x0016Æ\x0010¶ÈVÏ»=7à\x0008FFõÁäq8PH\x0011\x000f\x0006Ûém¿Á&°í\x0004`U\x0004%\x001f\x0015OQJäù@qCÎ\x001dÙËÝÎ£æÂ\x0012\x001euWY9¡ª\x001b×}\x0006Êý\x0010-°ï05²¸áhci HËiæ÷}:H´\x001dH\x0011ÓW'!CKÎÒ¿öó\x001bîn\x0012Y\x001c>Z\x000bNÓ\x0015.íQ¿'\x0017þ\x0006ÜýÅW,"gIâ¦LÇ3i~áoÐ®C$t]È\x001c\x0016Gºs\x0007K«E£g:(Ö±$\x001dðä\x0016õ\x000b	m\x000f>HÊüÂß \x0003X:@KÂA/L\x001dÒÁ]æ3Å
:
[£\x001eb,l\x001d¥A(Ø7znÐ	¾:\x0002é\x0003\x001dJAðth%+4©\x001bç\x001b4øbÕ*mÈ\x001f[±AÔ\x0001YØjVWJZÖÈÍ}¡ÑÜ°ªÁàæÞÈÍW\x0019íÕÂc\x000c^,<\x0008³:p\x000e§Ã\x0011Ê\x0000·Q\x000b§1ârñ¡³a3M¯8ø:Èv\x0014Ù\x0003£\x0016^czªÊE%Ü±Þ$\x001c¼&§jÛ\x0018¼º¼`BUÿN|¶TIaJÚjÛ\x0018qw9Pl%è\RL4ß¤\x0014®`/üÆàõEG¶YÙ(4\x0015èÄ>LÚm,üÆà\x0015F\x0017Ï\x000eâ*\x0008LAYWÇå\x0017^cð\x0006cf\x0006Ø"Ñ\x0014Mñ\x0008½ÄÎsÕW\x0018ç°µTFå-"g}¹wÍê\x000e3x±Aú}\x0010èzë\x0018ün±WK¬L3îÀ^8+Îj%põÕ%fà\x0012ã7`\x0011XIì|0Hi7«[Ìà-Æ
ÝgâINV\x0011¡\x0012¶­Ø+ÄkLX±å-6\x0005^y#^b,©\x0006»/U^@6ò£]®Æ^y£¸Å4õ*ðt\x000bvv³ô
æÿ0½úÅÓÓýã¹ª!ÏÃs@z¤B\x001bc\x000f»¤\x0010]+Bº<ªräÞHnµPAøòa\x0000<Ó½\x0003±w\x000eGQÓE;\x000cG¹~èæ\x0005Ä#\x0010\x0005¡Gv¬P/)A:¶u\x0019'C\x0014é0DAÈ±ßÚ¬"øfBÎ\x0002ÚøIîî4(ª¶
U_ÊSÓ/ï>??>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ywqúÕÉÅ\x0017û\x0008ëg\x001béò³M'¢§«\x000eAå\x001b\x000e¾`2!ªf®#4¶!4¶\x0010uæu&´:ÞaÞ\x0008ùÄÚÏõæëBô¾Aô¾\x0017Qi®Ò\x001e\x001b!dD.ÚV­6Ô\x0010a\x0010
a\x0010½ÎHOêØAoèñAAÝä7!ª\x0016Qu#\x0002Ê³gDM.EÉ\x000fFko×ØnÐ½Y¼ úIé\x0012¹:ßCD¯Ý*µ´\x0001òn>n\x000e\x0019PR¡Å\x001c<ó¨Ë\x0011ëpJDLá.ÄÈðL\x001aBô¬ü\x0001ÊT«)9XÝÀ\x0011±m\x0004½\x0004\x0011h\x0005)Ü\x001dÐ­4ÚÑ\x001e4¡÷\QÞ`}ÊÓA\x000cÜ®T\x001b3\x0019¹\x001cQÆààÏÞAäê(89\x000cJÚnä{Æ\x0010UØkpáÔê\x0008Ôº(nf(6ÑÌ´\x0001ëCÔ-b¯ÁQÞQRVF¤yÞÄùtæ\x001eBÓ\x0012vïçÀu:\x0008ÃªNrøVë¹\x0006Ï}Ð"B7¢'Ñ(HÒ\x001b\x0017å!ÀÖÃÑÝ\x001eNÜ,äÿk\x001b
\x0004XÚëTÇ¶\x000e±\x001dCÓ;q\x0016)\x0010%$Qé\x000cç÷h\x0005+Ý\x0007m[c{
NÜ+èxeBWkËûwü\x0013¬µ¶58¶×àÄHÏ~	\x0011h\x0014m9ûÔ¼²A\x000fb»mïvÿ\x001b¤\x0003\x0013\x0011I¿Ökv\x001fZ;¾Ý*¾{«\x0000+sÅ­¢(@\x0012»¼Sjé:Äv«øî­\x0002ú\x0019Ý\x0005á³Ù\x0005S\x0006Q®\x001eDß\x0012ö^W4\x0004ÊBü\x0002b½(\x0016QÉµö¦½¯èîûö\S\x001d\x0011\x0005\x0015XX/)è å\[æBã§ò\x001eâX4[ùöêèÅ§ïw4¾3°{-¸©\x0014xM¥Â[*ÎO^¼~ù|\x0006±Íô±	ÇÁUïä3êÉÇuvñæ8;pÑT;lã¦K&&vec\x0008°¬×	ó\x001e×r:ßÐùN:å2Î¡\x0000M¦cÁ\x000fðëfµ\x0011F¸¶¨g?\x001cVXÈ@ô[sÁQñU#\x0017ÅY
WEW#Ü\x0013\x0005¬=p:\x0004YæÕYsÅ+ëÂ¼ºNU}«p^5táa;5zñ
Y\x000bÇ¤¬µ¡Å\ïåxºzÈO3+ûðææ\x0005Xáá\x0004Ë'Ç3rÕÐíÌêÎ©EíÕ\P,Å\x0015´\x001cyU\x0018PXµîthéB\x001fóìQYý¼¹ó0k6\x00189_½¸\x0014ÏffèY\x0014%Î¹-\x0011/ÐyÄñÖíZ«}?»ð4+ªXwôD§XjÒ
±jìlOpZtÂ)TRóØ©Ò*Ãùå\x0002<4êº\x001fs¬«Zö7×\x000fWßm7Å\x001aÛ6lC/fó bçJÙß^|µJËJv`\x0015áÕÔÞ²\x000c\x0004z\x001fkçD\x001c\x0016rUw\LS´=\\x000bâ\x0001K¹ð\x00026
¢Ý\x000eÍB,ëk,ë;°\x001c·]Ãv\x000e>%<§ë¹Y¹ªeTMU¥iª*÷ba®\x0008«¡éÜ÷ÛIÃâ¹Ñý\x001aÃº&auL¢ÁË\x00167P¶hÀT\x0011S3ª¾Át\x000b¦{À\x0014°ëá$`~R\x0002³®4¾Ðs*{ÁB6[\x001b\x001b\x0011¯0hpÎ>þtõðÜ.®\x001f®ïùts¿½à3þæ.°ûr8Ï-(ËZðÎ^¾9¹¼ÌÕn\x0017§§\x0017ß¼>»ØUñF¶¡´QJ×Pº~Êx\\x00015F×ô@­+¼Ðd*R2ôSFÛëRIªèÂB=¶w®NÌ\x001c¤¬d®"%F\x0007{)äBÇrÅ\x000cMÎ÷°~(M³yLÿæÁè7xE,Añ2	L\x0019\x000e0á¦Ù<¦ó(/Ê¹\x000bkº\x001dðÅ®]änJÜä*S-aüYùR/¯þøt{u·\x00100ã5ûy\x0010|é+¸×`0b6$õòäß_¼Ú\x0007Wç[aü\x001fó­Ã9°Y\x0007\x0011\x001fX\x0007Q\x001bV\x000eIuÍUBu
v°%Í©¬;
\x001bY4É.z\x000f³²¥p¶³=pSB)M\x0018\x0008`\x001d½è5ÐÝ'y]×p¾ê¿\x001dáðg\x0007\x001c¾çg^úGæ¦ÒÚÔ\x001b±­ê\x000clVw±E§h;XQ´\x0014»÷a6\x001c°\x000cN
ß\x000c\úÝA§¥å;cJyÍ~©fÆ\x0005;\x0008gìÐ"þÁ[²»ßw\x0015M\x0011ûÀJ\x0008Ê´R¢¨=Í§\x0016¼<yõ·½PÌe¢JB*\x000b¨\x0016\x0003O©Äìýz\x0019l är¨x®Ò[sÒr\x001cª
ÔüÍu\x0019k¨\ÇPù½=0HÏXRö0ÿr²*4T¡Ê²¤r(÷DT\x000cåÇ¡ Yê°x­kl\x001eËufÂsÐ\x000b(ÂSÃK]jÕV\x001dTÀ]_\x000cj<9:øaÉ7½×;±\å:°ââø×hºh°hµÇó}x´Tõô\x001f±Tûô¿ga\x0005ÞÚF*Ø®°ÞâW,Àª<[Ä2z9\x000e¬ÀOùÒ9a\x0019t³òEXÈ\x000eb\x0005»\x001c\x000bkó×Rn|	®\x0005?\x001fæ]UçéD¬'y:{°,¾Nfå\x001fÇ­* ÁT\x0005n^5o\x0011iì{J±X%e´©¸úIËo¯\x00010ßb\x0011kÖ\x0016þ\¥mÁ\x0017\x0011:Çç\x000eluº`Ù\x0016kùÚB,j¦¥@¤CÄ*òMz¿\x0004ËµXËÏCÄ¢%¯ è;ÇZ? Çwbýæ°\x001fR\x0003+\x0014Êö\x0015ÊhÁ°×¾]ò¾cÉkà^,Ê:\x0016<Xe´ìðA\x00127
VÏ÷\x0014-UÑÓR´âK\x0000èù'eTí÷\x001d+ÞH[(Í½\x0001#\x0016§gÏ}\Õ®xß±â±m±+XÔ¡(b©5nM}»â}Ç7¥H\x0002±x#+nÜ>öì	ËÏ\x001e¬Ý Ö§Ê\x0018¾ð8ÇR}ÐÔ½ôa5m]ìÓ¶.{F3BW2I£\x0015¸`ÃúqªÖ<\x001eó`úA\x00129§\x0015\x001føra­\x001c6¦V7N ÕË@4\x000f¤- Q3-°'*áÍ\x0003´×Cè¸\x001fJ#¸p\x0014¹XÃ¶\x0016¼1rx\x000eÁ6?Ï!¥½§[5õ#¡F¿ØGeØ6 >RÍäG\x001dPÞrud	`/ù&¦\x001dvihfÐ\x0019\x0017DEX^ õJX\x000b~´_¥Z¬\x000eåõ3¢r\x001d­Mö¦óÃ{Ðµ«Ýõ¬ö`°Ùa¦2T³\x0012þ:ìæU\x0017aé\x0016K/ÇRÂiÐ\x00014_-<\x001cHØ\x0016\x0004\eMèÌòM¨ð0ä²	Ïíx\x000c¥fÏ!4Q6ü¹JIê]©CòJå<SÙñ\x0003Ýb-?\x000bQÞRb¿ÒT R5_µ\x0007Ë'!­ø£	i=\x001c]~¸¹º½½ºÿvû³P¼ß\x0014\x0011åå\x0013QªE?£¾<º|qvr~~rñÅÎG¡¨\¨\/b4ï\Ú}è5¥Ø"-­ÂÜ]£±ò¢#cãD/dä
aL\x0011\x001d\x0001\x0019V¥ö ÖÂá8ÓM©Ó²©\x0016òY>ÏMÐü¥tÑE±³éÀ]'2JÕ=AQÉ1Þr\x0001¼REÇÌ:ÿ}¦4ýóª±¿:Õ+UT\Vïºª}ÚAu\x0019#8j \x001d\x0017dmÉÝ·³çY\x0017¤imé6>\x00104\x0016óÆ`\x001eHé\x001d/I9[iÒ\x0005Y%½"dôº\x0018Ò\x0002Sw\x0010²0ÎYï\x001eÆZ¥\x000f-¤ègÄ(\x0011Í¶4|òÅ?,Çkýlt»\x000fÒ·¾\x001br¾\x0013¯e Kq·\x0017j5d»·ÕÀÞÆ²s²"Ó$ÈÒ"ÞÊÖC¶\x0007¢ì?\x0011¥ÂúÀüa¸Ñ´Ä\x0007zÌ­\x0001è\x000c-dÿæ\x0016~\x0003©9ü,%{Ô\x000e`íæVªÝ8ªãüO@ª\x0016²ÿPü\x001fXº\x001dIÝ=(ôGO3ñx¤\x0019)8jçækfº\x0018m»¹m÷æ¶ÑÙ¥\x0018\x001efRxXxôwn¶ø²\x000bÒ·¾\x001fÒ$õ\x0010í¬B\x000c\x0018:f[>{é\x0016\x0012ú!ý\x0006Òòsª0åÀq³\x0001¾\x001eH#\x001b×Èn×¤ÞµXÒJµýIã\x001e1W;åÆ4¢1Ý¢%5D\x000bÒñ²\x001e¸b9^\x0013W3B³µ
toíxÝç¦`ø¾é©\x0010Ós\x0010\x0002¼Y\x000biÛÉ¶ýõ¬^ÓÛ°¦[¢õÅ\x0000Á¼ºM\x0017¤n¼r«»½r­MyD\x0008@^¹uP=`¯u&£k }÷q\x00137\x0006_oâ^¡Ê\x0011\x000bÞó»Ðjç\x0002Dc@tÛø\x001bÝ4Û6ÐûBô$ù¾íæsEû }\x000bÙ½·\x0015Ößòl\x0007ÚÛ\x0000\x001c÷#ºöH¹i)Iû\x001bÿV¯\x0019
ÜÄN\x0005KÇ·õÎ¹ÆV\x00061ª®#NÝ\x000cæ¯¯\x001e??`(¨¶osÃ¹\x0016`¸HÒzi¸ôDÔ	~u\x001aó×'ïÞ^b\þ»}¸uQ\x0014U,æ«2Çðþã¸7S\x0008µhÆ\x001aÞê¢Ã+\x0007y±å\x001dõï\x0016URÊ=l²ÄÃp]ëÆpÓL\x0012ÿ	r­KU¹®&\x001cjxCÃ\x001b\x0006yãuÍS	K4	4º®ÀZ4á­5¸Ð¬\x0006\x0018^
¢tñ¬Wl£Ì¼Zo)mèæmv\x001bî¶èr"k)Ôª\x0016Ì+Üa¬iÇ×\x000c\x000f°L\x000f\x0002y\x0003wfsÖ\x0000\x000f°ßRÑ\x000b\¶!0¶ýÅ¡\x00051`¼\x0004PÑã\x00155\x001bà`47çVuáú\x0018°J*Õã£rO2±±øû«?¶\x0017\x0008JÏKV(y½ù¡\x001bO«y}*,#þúäßw\x0008f¸ª~\x0008³9'ª\x000e;á\x0014ÞCs\x0004fBSúst_¨CÏ\x0017æ,s
ës\x0014ûpP¯{®~Ñb>_h9]hè&¥ÿ»éâý[°cÿ/~ü3<±b^\x0016t1]:\x0014éÂDéd7]´äM\x0005 ^ÏÜ4­óÏ¥KÑjÑW5\x0011}ÝÏ\x0006]Ò\x0000,8\x0011,K:Ä\x000bÝVQEtª\x001989ÕÙMç,÷\x0008¦¤\x0005GíÉ´²Û5b\x0016áU²\x00047%Øç9ô\x0011L)º
\x000b´1§h\x0015mÌ´}öD{OÉ\x0016qj=+«KÉb"qå­\x001b<hW\x001eô­<­Êcn0¶\x0008¿kÁxv^xj)^Ý%'â)Ý÷ÿyôj%C5Q2ÜgP®#{\x0008Á\x001b¬\x0005Ix\x0010Ø¬Ìg.§ó-ÝD=i7+\x001deÒPÀßÉÀ
EZ\x000e\x000f0XVWùY\x0002Õ\x000bÐÑº@ð\x0008÷ßÿñ'w\x001fn®ïî®^<ÞïP\x0015±Ü\x0019Ú*\x0014¦´\x000cE"õÚFÇ\x0000ÕÂ#âÑÉ«\x0017g§¯^\x001e½xw±Ôá\x0007ÿonþÆ1þl\x0007òùÕýÿµc(\x001dÆ\x000cÈ\x0004Zn|ï,æþä6[gúùÉÅéÎ±ÌUÛ7$\x000cO]ª}¡\x001c¾Æ;CÙ\x0004\x0018$b\x00014·Uwg)¡j	\x001e"û\x0008QØ.Ð^6\x000e£EÐ²\x0010Ú¢&½ÐVïxÐÊ§îË^BÇbÍ6U\x0005e\x0005\x0012Lr`ÏtÛ~Y\x0008X½E  jmö\x0002
O]\x0016[½ç$\x0002\x0007¦lh·Mg\x0019 Tq«\x0008?;\x0001­¢v\x001b/MþïàÍ\x001cpÝ>J^\x0006	íSø¯\x001eB/\x001a@?±Ùû\x0000Q\x000fº\x0006¬<ÉFXºt*½U\x0019m! i\x0001M? à0_Ð-M<ÙáÒ+÷±\x0010º	£e¤M\x0010Ê*\x001c6¤"B9_¿Ð¤Håê¼ ¿¼¹»ÞzI²ä\x0006\x0019\x0012Çd¸è¥ÒãMT¾<ÿót×Å<ÕÉæîØB\x000fð»i¤ÕÔ\x0010»Ø\x0012U0_
V¹cçzÀ6qZ\x0019Q\x0014\x0001ÙZ5[ý»¬\x0012\x0007d^tÍ¥å\x0014\x0019\x000f,4\x0012XYÆÎ+Ë.$«Ó ¤Aî\x001b4Á\x0015Ó\x0012]-
\x001a+\x001bÛh7¦Z4ÕV\x001eÝ¤\x0002î\x000c§óõ¬­\x0011[&[4Ù\x0006sd\x0004(jL¯%·\x000cè+Ètuº¢Õ\x0010¶\x000c£é\x0019Lþ´üàkæ¥\x001eösy^«*Ý=º{o®\x001ePâkQ#SÜ\x0002Ü)IÆ¥ú)¨ºV\x000c#'_-løCp¡\x000b-¸*w5ÂáúkÐ©¤ [ÕSã¿³=¥^|ÿçÿý|uóÝÝÍõ\x000e)%\x001a³\x0015eùUD;>­ÜlÍþ%^ ß}õêìt§RâO\x00179¥õ# ¥CYéZ²\x000c¹)[×K9ÿªÛE
-)\x000cÆ\x000b/gfa£sC¤\ªäçµª;IhH\x0018!uE
\x0004c	Ô¢È³<\x001fßè$õ-©ÿ\x000bBK
AR©Ñ¬\x001aî¨ãI»Û­\x0015<ÒÛz#ªp&ï^\x0007Éú½RÎ? Îûù®\x001a\x001e\x0002S5Ø¤]ÃN°"wäâÀe/\x0010;Ù°Þ¶\x000fáï\x0005\x0014¿ª²@\x001c?ÍÉútÿ~ÇÙìñ)\x001eæ¹FÂçð}R'M(y}ñ|çñÑt¦;ÑÊ«¶n´f6~î.&«;yccºÈ´ánÙ\x000ee2²\x0017ôC2½F.fsÍ¨¹¾QÎ3] \x001dºÙÝ\x0002¬\x001aÊl³B\x0014ÑB\x0016úÐâõ*Ä\VtËñ\x000b\x0016W
zK¢Õ"´Z'7m¾)«$)\`gÁæab¶±Ïb¸J[\x001bá\x0014ôÀ9où)Á£Ôfq\x0003I¹Æz°­\x0008 ÛÓ¤ò=lö»^8ºzÛàÍ­\x0013^ÌVw¸l\x0010ºØ°/\x000e[tWr
sÜ\x0015lïÉµ\x0018Îù\x0006Îù¾\x0015ç1k<Á\x0019Å\x001dUr·\qÕ-\x000e"YÛâ`Á(\x0019¶® ½`\x0003¯¶mal¶1!ÊvÙ\x0010ê\x0019ùâá-5$q\x0016\x0014·Õ°aKÅ2¶*ÔlOb={Ø Þs5·üð\x001c\x001e3
#[5pUÊ0Â=M\x0019Þ3p¢Èß¦H7´ÜU\x0003f_ÔÃµ#çûFµ\x0006Ò¤æ#Ë°f\x000b¢­TmZ'Ät-8Àx"Ù\x0010gI~'®BÎ\x0005~öee\x0001
O¢ÑOµGÜ«ûûèï\x0008\x0018Å·\x0014]	nÃÇ-wS\x000fäùÒèï|ÊMU©?F\x000c')\x000eÿzÄZó="Êi;}Ø\ô\x0010ñõÇÓ+i\x0000,Ñ[Ã\x00172*×0*×Ï\x0018];m\x001f^Ä³°zÜÂÜ\x001d\x0011åëWB6ÏöaîÙþ_:Ù\x0006Ò}§Rã'Å£/¯îwÄ"ñI+¢°óÈih©ë"U\x001bÍ*u\\x001e½<¹Ø\x0013'MlUþqd³¡Ma§ÁÄ5QØX¿Ôé0ïK-cOÆ­wàþÁÉ4puÛKxù×ë_®ï?o0c{\x0017òX@Ð	6)a·ÀÍo_¼`szñv\x001f]Ýì"ÒIÑÕ\x0005"\x0014ÇnÙÂË\x0005ÌÞ|\x0016ã)Õà)ÕçøîãM gÛø±Û2/P»\x001cÎµp®\x000f\x000eKØ7°7êR³"¢WüY\x0017Z¼Iûä=xrãZRþxºLí|þãb¼êrxz\x0012\x0010Û6¼\x0017\x000b¤\x0010ë\x0004¿ØÆ1Gµ\x001cÏ·xî{FÏQ5²\x0007nå#ùáæ[-FóíÈù¾K$Yß0\x0004àuçç5ÌâévätçÈEWn!/\x0000A|y)¶6s^\x0007Íè=é\x0011±\x001fOi
+zïIÊ
\x0016lðÔn`\x000bèTÅÊÊMQÇ²½x?¿úývG¯QÌªeÅ4Ã´ð\x0004wê\x000eóMã/üí|·GÙBÃ\x0016zØâË @\x0015-¸¸è¸IÝ"¢´­~°PO\x0013\x0006ö²\x0001u:0(dBê%\x0001,¿ù¹Ù¾ËÙTÃ¦úØ4GØA»gvk~\x000fn6)TÍ¸IÕ7p©Ù:×êQ\x000eº\x000f²Ô\x0016ù°ÀR6Õ²õ
\x001cêÐPï\x001e\x0000öã¦å\x0007\x0000Üý+à*ñ:3Ð\x0005'JQ\x0010F\x0008HÔ³jªNJóCp\x0016á|¥S\x001f9þ<~s{õ!W.½ùtÿùêæv·¤\x0016/Y]O*>ÀtÓöèÍùÉ\°ôæõÅÛ³óýxU2âad«\x0003\x000fåH\x0004*a\x001cð\x000c?:a\x000fuxÐâA7^Îx\x0014ÿ&%ùÄ¼¾(öã\x0005Ñ\x001eþìÃsT¢h¥WFEx¶à¹U\x001bªÜ\x0017úð a%þ%é¸\x0018RXÕFÕñã\x0001¼º_OÄC×')\x0011ÔÊhüHwDZ.l1².ðìÂÓ>ùvó?Cø{ü]\x001f}\x00199¿ÿó¿î·\x001b\x0016%,Bâ©\x0006iø¢¹aè`ëW\x000bêówzôe\x0004ýúôb§eI|ºJ|ø³Oi¾À´®Ì\x0007|d\ÅWw¢Ås\ÈN¾¸y)y\x0010\x0003*yø¤(^®\x001f¤ºð gÿTîh·6'ÚåÍÇOwG_<~Ü^J\x001aÿ0\x000c_tõ\¬É\x001dsXbÄÍ\É.Ï^¾gÇ»;+HÎ4t¦Îp_ð¤$Ãs,K8¸\x0019¹.:hè N\x0007¥PT7'ø$\x0015n¤³¬Û \x0008÷*:ßÐù¾±\x0013cñÊ\x0003Wß\x0002¦uä±Ã¼Ú5tõÓ>®^¦\x0016\x001d^f¹wbm-Ì¡±\x0003±®Ù\x0015¶sWÄ«§î\x0006Ø`[±÷\x000e0Ó\x001c©\x000eß +ºô$Ý3x¥~%]me¾\Ø²gÕÌÓY\x000fmö¬´]6é\x0014<µÊ	*§\x0017\x001fZ°3/T\x001dxuWWwµY¶k%w	\x001e6×¡YÁòxVÏÜ\x001aáù$û ª\x0016ÄòXUcl©ûùæóÑóO7;$m£3mÅP(u>w]
\x0007Àl~>öÕ}{ööèùë³\x0005¶!´Ýñ\x0014ËþÖ\x001a\x0003Ýû»\x0006u\x0011Võéø¯\x000f#\x0004hø¦J6\x0002Î\p{\x0000eeü" ¬ßå\x0011úH{¬ÇíÌA8¹<àf\x0002É=ñªÜÌrøË
¢®ò,#¡®ó,ÿõh±?¶®õÍ±~¢\x0007üfßI\x0004Tc`5{\x0010/\x001dýf¹¥häÍn¯/Õ\x001aÀ\x0011ì\x0006ð\x001e0À±Ê`2ò"(`³]\x0012\x0017U·
\x0004ó¾\x0003L
~[±ÎQNH\x0004sìÉÙËÀLÕÿ\x000f¯.ZõXÄË¤&.vCß\x0012ZYÄ\x0005Í\x00123ÐµÄDQ®AAU\x0002+\x0012gÁÏ6Y\x0008æ%?\x0017A(°Ñ«
\x0019\x000c\x000c'¤Ê-¢{À\x0004Ö×Ô}:{Ú§ã_}¼Þ\x001ak×¨À\x0001É³³\x0006\x0004]Ö	\x0005¤FÜ3Áöÿ}òòtW¤]ãê\x0015%N\x000bþ¬\x0002\x0001§\x001f>íßi°\x0012¢¬B\x0005ß|îËÀÅ¦é\x0012º	\x0003¾x½;|Gh®Es\x001d´ \x001b4Ô´\¦½%\x0019O\x0003ê¼¥%¬é¼2!ûpõíÕÃçûíd¦%3¡Aó-ÿ« IQ\x0015æiê¯ÀæÓµ°2\x001dñV76H\ww»v°ß2\x000b\x000ciDÊu=(ÊÉ\x001dóo±Xu
º^½Ú¹C¨ºF}ª§²\x000cU9<Þs\x001e(¨E	ÜlÕ\x001bê#u5éS©«Åê¸
ª`
LÔf#T1ß×©\x00035÷­.gØ?öIZÏÍÝõãö¢\x001e#E ¨ö.pG¥èhçOóy=g¯Nßí¬çÉxÕxnZpþ¯ÅkGÏu^´ÕYsY{	\x001c¶p	Ò[\x001a¡ìÇ³ù^[yxñÆ£êëÄË«?¶»\x0005FzU\x0008LéÂË¹ÈFÍ¥k½ÃÎï;L\x0005¶¦\x0002ÛAåRÙ`¢rªtÊ²ôP«gßÞ\x0017`\x0001Zé*ôi1KËTOR¸m/þüçOïoo~~Ü¡é#5ÅR±¦. ÑûcÀPÇgÙXã¦½8}óîùùÙÿywº9ù/VK\x0002­]Å ÂPËÙ8xÝ\x0004#k«ÜÐÇ)ë'1(d?'&Ð\x0014þ%q\x001a/Y;GÀ\x001aPÈ-ã7\x000b2®FÙ,ÈËÏWß.*j\x000eÂrS{¬\x001fÌu¸Îq\x0012\x0016vîNôîèòíÉ\x0017Mqó^Z×Ðº!Z\x001cLzq\x0000EÈpjm7@ë\x001aZ7H\x000bzë¦
¦\x0001¤ý©Lh>¾Ö
\x001b\x001aØð¢]\x0007bÖHî;â5½bo\x0019ÎTmÝëÝW9tfTVL»¼¾û\x001cý $}~ýðáqûE\x0015þ´ÝX¬\x001cE×K¬ªu¾P.íòôÕÛè\x0003!äóÓË\x0017ïÞî`\x000c)^u\x000e®ô'O²nG/n¯nî.£§~³},¥\x0005Î#RÊ\x0017	UÁÍ@Ôº¹IÑíÝÑó³£8§gÛ\x0007ñ@K&ñ	êâÅ?ïyJ.Ú|JÁ

³±LîCÁ\x0016ª	ôÏ¨ãîÃ+	\x000ff=|ÚJ\x0012Ä3ñ$¢á³.px
È­â+1Â<|²O¦-\x0010(RB7k\x0015B}d\x000eÑ¹ÎõÑ)ð,Vê02_m¢çÁéNnõè/tò\x0005Ã\x001aÑ\x0018âsieÑmX9~ÐÌ.ôÎ®.Y\x001d.F»Ã9Í\x0011º¦ßé\x0010_³; {wØ²{-×X/8¶/\x001aQË\x0001>Óé\x001d@±$shÓ\§\x001a\x000fnÎ¢[É\x0011À\x0012}Ê\x0018}ê²ØF²±dz\x0005	S²åÊ\x0011,Im\x0004\x0008]2æ=ïn;?\x0017:c[Û£ËÇowÜRÍ³¼îP\x0017»¼[GT#kù	ìg{tùî-$êïðÃ/?üü@^wãk³°ëÝ\x0015°@Z\x0001êøÛÛë_>}¸ºûpP3&û, Eâß`ì3lÜ¯Xgçç§ß¼~qòêÅéDâõÕI¥!ôáÓÇwS>ÜîjFxv\x0001_ÇT9|&gÿ\x0003jçèDÎ¯[\x0018çàØÍ(÷îGè¨L¨)º\x0004q,1-\x0011R\x000b}\x0004¶
\x0010\x0003kÇjN8z?¡Q:g±ÅU±0\vÁ[Çc\x0018Ä1\x0014¿ÞÈ»\x0017\x0013ÿ5¶iT|÷q\x0003\ï!T\x0011\x000b¯¦XÇ¦He8X\x001eBá³|o
¸é<x\x0017qËl\x000bÐÕ\x0018\x0004Âÿ\x000c\x0010*ób"¢\x0015Ô\x001d
Ó\x0013mf"L¦y1½^¥O?¤\x000cÔú\x0019°è=BÜä\x000c\x0013¡\x000fÀ\x0008Ç9|dªU\x001bc>Y\x0006Ò¡ðubt¹ÃÏ(ä\x001fí¿_%\x000f?þ{0Nòéæ.\x0014;¨\x0015T·\x0010§7ú¦ùÄÅ¾rD%Âd¼y}öjkÊNÃ\x0011\x0017ZÌ¡²ë\x0004ÑhZêf\x001894íUA}!Ç@âìë¥ Ñª1H¼á8Aðw\x0002!\x001fx\x000c$þ¯Å#\x0012²\x001cp\x0004qÄv=8\x0006$\x0010ë'\x001bo9\x0008Z¬¥ :ä8\x001fNM ò\x0011ïRÒc\x001a7Y¸ËAâ¬ÂBèTg÷?£\x001eY\x001ed ].¦\x0007ÎrxUrK\x0007$ÞÑ-\x0007:wZºbÄ?AX\x0001&w[ÉÃË¡¼3Ì²\x001eÆ8Lú,\x0018êbó1æ)[Ü\x0003¦GÑ\x0019¡WÅKlúü«P>ÞþøÓ\x001f¹¹Aëÿ¤#ÒWÑËåÄdZåB'\x001b h^6\x0018<IdÊÒåpÞþ_\x001e}\x0015}ãÊquÿáú§\x001dÓs´RHtC\x0012SÊI`1Q\x001a39\x0010æ)÷\x000f'u§Ï\x0008¨\x000e3b#h¼Dä.á\x0011¿².ì8Nû@Q\x0000-}ÆFto"((ÒÞóVy°Ã8 nx@©]HäÄÎR< À\x0003:sÞ\x000c¢\x001bå`|#%Y¾\x0008*-\x0015F{¼ä2¨¸
C\x001b	Ié34 r]~¤Ô,Câ1.ÄëS\x001fj8\x0015V÷¤Ï\x0010¨¥¾X\x0008Êï\x0011Ô\x0004\x00065;ç>Ðt\x001fV£#5]¼ãY}Æ\x001bYFÔËCíøÔjG=íå¹\x0018T\x000f#\x001aØÄ\x000c(\x001cjË+\x0015I1PE8¢®MÞ\x0008y¿ãö¹\x0004ó»[ùûÍCu%9ÿôù&B~¼¾û|ôöúþþê6½Ôï¼ÃkÍ'\x0008[ÞDã%Ý-ze®!Ï_¿=/O_½=z{zqqr~úvK¡"Ì\x0011ÂÈa
\x0011\x001az­Ã\x0004[MÔ}=b¾Æ bqKö,Xz¡\x000b!ó%Ä0ê1Ä|Á\x0019A\x000c&[õè5åÙ*\\x0010QOã]cùæ3BhIX*\x0012æÎ_i½æA$iõùN44Ï:{o]xèª\x0016²ìEB4S\x001fs\x000c1_F\x0010±Èæ\x0019ur¨Æ\x0007\x000eÊ)\x0007\x0007Bÿ\x001a?¸\x0014u~D6fM\Êñn9Ô(æÛÞ\x0000¢\x00152÷3Æ
­¨÷z\x0008¨¿Fö0Û\x0005óLå ]´";8Ów´wÑO\x001dYÆ-ñ×
$zRzl 59G\x0012\x0004`\x0017:ÞÔ\x001cî1Â.ëìKn#Ä5
c«\x0011¥ÅB^.ç\x0007¥©ÆÎ>Péefg7!ª\x0001º1Ã¨ã~¡¸\x000cFÏè\x0016l¹ÕL|h\x0000CØ\x0003q²p\x000c ¬\x0010½ËbP\x000e
æÞJBLö	V\x0011Û%\x0017»M;E\x0017«½ìpÞIÚª¦ÏÐ¹âù\ÁôD ttòE×ü\x0000ã\x0004£Ògd
â ;añêBy°ñPì&Î<S\x000c ¢¶}úld|\x0000ÈÛ\x0004oY\x00007\x0004`DcÕ!\x00101¾>#ó¬LÖn£è%©\x0018EßPñá¬\x000e±\x0012Ë#ÊÈVFÁ¬\x001c\x00157Ñ}Ð^Ìø@N£>\x0003Xd>CG35Sh²dÖ#\x000fÑØÐ,G\x000b¹ìdÞIzc¥Ï 9¤'x¼Ñs|,{chsÙJDlI¡(¹<\x0000²´q!ÅGÎ\x0001,Îæ?2DùÒ(JÉî
hÍ£8ó\x000e0\x0013=èÜXKÙzq)JÊ ÎòB<ÀNI	é3ä7gt\x0013\x0000Ö~¢cOC*)>>#\x0018¹Ë;\x0005AÃN\x0015Íc¨C8w,Bú\x000c!JÎ n\x0018y©\x0011HZ\x0006\x000e±\x00081M*}\x0006\x0000A¬\x0003ÎðÌæd\x001b!¡¼\x000e[v
Ø\x0004Ògd`vK\x0012UJÒV1	í\x0001ì¡F/8}F·\x001c\x00053Áò^\x0001N\x0014\x0006â\x0010c\x0018Ò=jðP±:§î\x0001*Q±YÈå 9:b\x000f°\x0012PTú\x000c\x001e*ô6h0§îz£`\x0012¦!ù\x0001D¼¥ÏàÑLwf,§è\x0008$a«dpì\x0001æÙ`\x0003ô\x0019!."Äèêp(Ñ\x0006Q¢á\x0000ólñ5#}\x0006\x0010±®Ës@Ö\x000eR°x\x0012â4\x001dh\x0004Q"âØRD[MN¢AñkòoD¹òCø7>^ÁÓgÄn{Ãi\x001f\x000e=C4Ú^pXDO³`\x0006ø0}>}\x0006ø0C=\x0010Nýb\x0010\x00113\x0008Ñ\x001câ:5ÒÇé3r®D\x0007Gÿ\x0015ÝL(Rt®¸õ7\x0001%ð½7G¶J¼ÍSRuÃ_ÆpvN\x0011µè/\x001dçï \x0013\x0006tovmbûÏ\x0013í§\x000fÓý&y²fÔõé/1zW.ÎXU§Z,|\x0003ÚÍ9\x0008ù;\x0014c
¹T82\x0012ÖömNü³¯·9
;!\x001dçï`w\x000c\x0000©Õ\x0000\x001cKDÙâ\x00030¢ì_þ\x000e\x0005dÉU,÷BÀ\x0017\x0001ò\x0015\x000fa\x0018£øûû\x0007|\x0006Âÿ12Ùq\x0015u4Ap\x0014¢Äq´X6óÏ\x00037×w\x001f~K]8ÍéSI³ßß|z¼]ðïùí\x0019¬çD#£,?i\x0016G¥Ó~qöúÝvm
\x00113Y¡i»\x0010Qc»@\x0013M\x0000\x000b2ÊqéöÆäö7èÑÏInDçáY\x001eDë=5Îp\x001cPÆL_$\x0000ñ>ý6'B`\x001fzIíï\x0002\x00151DL\x001c/`Ð81>
4ED¼¶\x0010¢·\x0010ã?s\x0010DÕF1b<S"p<%9Ùø7%#ÂÔ\x001dBÄpKhÔÛ\x0017#\x001a5³â(
A\x0019/q\x0014%e
ÆkïJ\x000eDlR\x0011ôÐD\x001b\x0013Ýã(z ­\x0002IÉ=\x0011Ú]%?{	üx}õýuGRÕ\x0007,u!`ó\x0016gcMàÃa°#­mæµt;bÎ#\x0019@\\x0014ODÕêl³s^\x0015oqW	C\x000fbÎ#\x0019\x001bEÇ£(°£\x001a¢çQ&!b\x001b:\x0010CÖð[Uòw²\x000fál¹Úiò\x0018#?ê\x000e0F§AÒ5\x001fÛØó\x0005Ud\x001dÉÊ=xB\x0005\x0018[ßÓð±*äó%\x0007BM%ô°;2Õ4sÜß1\x0004/Çh\x000e¸y;\x001dÙ2"'¦c,´Ôã\x0011ì+\x001ehOKl¾>\x0003Þda\x0014|õót¾\x0004\x0017ø®/Ã¦zózÚ\x000fi¤cëhÀQCàùeRI9¹^õ0Úßßþxrrp Û\x00060'x?ØçrûM&º-ÊAhéÙ¾XUQ'x=¨ÀöN°ÁÃÉ\x0013
°ExÎ¬'~\x000e§âøL\x0019ÏL3ÃFðâ¿Äø\x0011¼ÜD\x0007é$\x0019D_®T\x0018oÚî@,§¸F@
Ð\x0001Ý÷"3äj{@\x0010>÷ãmò\x001fºùÍ¯¥\x0018]2\x0014ðô\x0007âT\x001f`íIl(%ý\x0008\x001föXÉ{C\x0003\x0007p¼\x000fä}áüNvïoþº\ð\x0014þ;\x0019^ÀÎù&eðk½¼æÛ²rãï\x0007ÿË5üVei^Í«û\x000fû°âuPJ1ÎXÎp)ñQ#Í7'\x0017/¶Úº
)ûª\x001dHÑ\x0015pÊ¬\x001cuVHÀv-'\x000eà\x0012$ûÞ?þðiK.{¼~\x001c}\x0019o!ñ¸ùóû\x0013ïAÈgk.\x0002Éù{W\x0002\x000b»\x0013æPµáËx\x001f§ÅÙn&
ó4»½\x0019=~Ú!Î\x0002\x001do8Õ\x000cíw?5PO\x0013Þ»©=\x0005q¤#f¶¼­-©\x001f\x0012z\x0002ß
meNÃB?oüÞI>¨í»³z\x0016ßM\x001d¯^Á¡&c¨<ÖþàÔÓLùnj\x0005XT¨±ÓQÞà¹\x0008\x0006Äîó\x0008õ4y¾Ú\x0008\x000e¸`ìEqzY×3Õk©§ùôÝÔ"Iö'êÀíô|<Ûh]Ãî¤\x0011èi}74ºõdö,Õ\x001fyR\x0010»;WnÝû5Ðè¢ÙKIDÍK
f|éµØx,®<\x00171xr²áS´@\x000ceãï«°\x0019¡Æ¬èg\x000cF\x001fÈ·u3\x0001=àÝ>\x000fvêt~Xl\x0012>Z\x001dí5ä+ãÎ6DPÝZÜSçm-¶;Nj£ë°=õòÒ\x0016Å\x0008>ffBÖRãã§©¶ýÔÔ\x000b_\¡¬láøi\x0019ø\x0010ö÷?|üá\x000f¨½yn«÷öS¤¿¹~ÜM
©}b`K¬TÍ\x0008R\x0001WíÄ?Á\x0004´4Ø{û:\x0002¾[@Ç¡É^<¼ÝÒ\x0003lÀJ|2p\x0005f²è\x0007ø°ªø8}z\x0001µËOr(E\x001dã_:Á²Xbê&\x000fð©äÑã§\x000fózt\x0006t:'¥HáÉ·ÔNOmì\x0008\x001f¤'v?À§©W\x0017v¹¬\x0015\x00019£Õ¹éF\x0019àÓè÷§O7\x001fjÙe>Thõ4ô\x001c´÷Ó\x000c\x0001ÀÔK'}z\x0001ãõ¥í°}Gêk\x000fé4óM\x0003\x0019#xX0>ÝxØ))ÓÙûÚF\x001fÛ\x0002e¡D~ùµx:¦O/ÄÌ	\x0002ÄÑúæµ¢\x000fç§¬\x0003\x0011éÓ
\x0003HªvÑIÂô\x0008-¦x\x0004Ý!f\x0018P,}z\x0001ö9R#\x00089Z\x000fñßGo­:úþ\x0013y\x0004\x0010ç!}º\x0001£ÝËÜ\x0012\x0014¨\x000eZg
S\x0007ø\x001czÃéÓÉE²9\x0003"EÈoþ¼\x0004Ã\x0001To¾\x0013?Ö¬Hô¿¾¸ù|ôòÓý>%ëðO¯nBäØ\x0004*q\x00164Ó\x0007ÖósôÅÙÛ£¯/v\x0008-U`\x0014®ê\x0002êm©\x000cËsª<gNË\x0019³ÜÏE\x0001©¾\x0001ó\|j¬¦KpF¹usQÌ©+X®|6ø¼\x0007Ls\x00113¥--×¬|N\x0005E!¥\x001e¨8,\÷e¼~f²éG.¿ÊhÌ²Ñ²?\½LÏ¹2Éx5-C>EþùýãÝ^/Þ¢\x0010\x001fzñ!ºÉ$	ÒÙw3kU\x000f×Ñ~ñîÕ¶w
á\x0013]Û\x000eB«sî;j¤(V
´Þí\x0015¶9\x0008!ÖpÂ\x0010¡ÖYP\x0014)¸[Ç>Å4rêà
\x0011Ò]sÐÈrÃ\x0004à· ËÊzÑ«^\x0008ñÍÞ\x0010bgNzä\x0008B°Z&Ê 1<Ì:¤ïÀ\x0018F'Ek\x001aÃò\jUàPß´í\x0008aÊ6cáY\x001eBï-oeËz3Ø\x001ckëZ\x0017 ÃòÃ¡Iö"ÚâV.¨&\x0000\x000cÜÔ\x000b#ÜöhZ\x0010QÑÏ\x000cY\x001b\x001dMLAô®í£ÛÂ!$¯\x0016íå½á\x0008z\x0008Q\x001bìH\x0011
=\x0000Å±µe\x0010·¾÷\x0010¦äôéGT^rÔ\x0013G1ç\x0019{ø.{å è*K;tð)Þ
åXÑùm':/îÀÃXG\x0007\x0018¥cÙ5o8eÍ+\x001fÊÑ\x0007\x0007aT\x0018WR0Ê ²3A\x001e«\x0011\x0013#§þ)í\x000fù]L\x000eF\x000b&¹\x000bWR°é>ÐzÜ\x0006\x0018µà\x0003Ðç¤:/]áÊ3ð¡ÄùqútóiPÔ	\x0004Óc-zdnlÕæ¡ë\x0010C(!¹²0äÌFFj¤èkKÔ
Ë]¦¬a³\x0013Ü\x001a\x001fâá«_Þ?M*I-ÿügü^ß~züm_¾Zô\x0014ó^Á\x001arkÓ°\x0010ª\x001b¬ÌsÊä ÇGoNÏ_¿û·í\x0017
b¾n *à\x0003\x0010´aM\x0017Q´H*¦\x000c2V0R²Í±!uÌi\x0016c<\x000c\x000fÅo|#Âó~cÇ2\x0006BsîÑÓä÷AÆüø>ÄXê0°Ø&Ð\+\x0016È5Û2ú\x0019óSû\x0010£cF¢0jSö<Ô8æõ\x0001F\x0017\x0017aÐ4üÚ8TAþÐ|ÒX7#¿¤@zÀèC^ú"\x0004QnúFOU×\x0006!éÝ|\x0008Òç§\x0012ì#áñU'C=­]êaß>~§~ÀH+J!¥Ï¦ìæåÕí÷×÷ï÷væÀº¯ì~§±¹m\x0014É!aáÍö¼Ô£'ç_^<ßÞô¢BÄ\x001b×C3t\x001cEÒÖ\x0016§ NmÏ\x0008¢ÃjôéGô*w\x0003Ñ³Ènc°5åÌ£Î\x0000¢T\x0018]ËßnFì\x001a7\x000e6WiCüC+\x001eE3-j\x0019@®\x001fÞøÓ·\x0017\x0011\x0004\x0016\x0007åVT3QhO\x0019)ìE{\x0019ø\x0015~½ýc.ö\x0014·õÛO÷%	xA59-di\x0011 <Æ<vºÛæûâüõÛíñÏ
\x001d^\x0001­\x0019 \x0013\/@ð5µ¼\x001c«i"Ô\x0008[\x0000\x001búÙti\x001f#\x000cPÛ3/,_óã½zWúûRºìüe#G=§#]¼ëSö¶ðN<ïw&ç/¤èj¦O7cuh.7O,_î½¦\x000eàú><\x001dBQ¨÷O»B*¾§¨\x001dUÄñjúôâI`µ`Y«]|¥\x0017Ôíµ¯ñ\x000c¦*\x0018×=¹ÚYY\x001a<Å¡©°ð,²Æ£xïo~¸ýüCuËÛäO7ÿøÇÍõ>\x001fÆbN¨¥g(©ðå=+\x0019S\x0001¶ v\x0014Ù_¼>ûòË³Ó\x001dNLAT\x0017>ý.m>?K¥.\x0004¤5S\x0014Ûuþ.R§0¢V\x0003E=\x0003U!\x0007n0ËÂq]©ÙUã¼òêZÁÕO³Q:\ß_ÝÞÞüù_K²<5+\x000bi\x0014t¡ZW4ë¦2\õüúäü|w\x000e\\x0001E¥ã Í (&\x0007Ê5³5Íâ­ûDÂöÇ´nRÖ\x0019\x001a#
ÀI{ØØn+Ö\x0002º«ºª\x0003T¦¿C¤Ø`(\x001f6\x0012[\x000b.H\x001b\x0012äÎ:«töõùö\x001fßþã×tT£%Çÿ<¿¿þ|\x001d!¸wêÍõýÍ. TM\x001d\x000fs_­ tþ¥Ó;ôóÓ·§ñ7÷Q[²0b\x0004æ8}ú!QÌ'e)eH/¹ø!§gb\x000fã}øõFÊÚå©êa/>½¿¾ßS
\x000b\x0011Åà-:)\x000bÍ\x0005à%)wU_¼~~z±½\x0018¶ðÉô*}? Â6B\x0000U~\x0006\x000cúòæ¶;\x001b[î\x0001\x00147ß_îªñë«×WË'\x0018È¨\x0014%A¯[bëú<Áñ
4á¯O^¼[2¿\x0015^}öâ)lËéJS«åîD§¦oCt9êÙ=x¯ô\x001eÓ
5kóR\x001f\x000c9#Ü3DãÝcçCvhã¥$(\x0016\x000b\x0003I¥ÄÕw\x0018¼\x001cêìÆ\x0003n\x0004æ1\x00174¸ØBGº5\x000bO~÷ËÏnvá}õéñÛ«ûo÷B¢\x0013\x001fK}º¬\x0018
(Y2|BM\x0003J\x001b¼¯^¿ûâäâ%x9¥ª\x001b\x000fÛøf»,LÎöÂ\x0008\x0005j¤º6Cp¹î­\x001b\x000ekte\x0019»ü²\x0017´§ÚØ8vÓ\x0017Ò!¼\x001c¿îÇ\x0013YB\x0016ÇÎ±Êö\x0014\x0018ùÀ<\x0000^\x000e]wãir¯#P¬g$\x001c\x0010¦µ¤#x\x001cµîå®_î	cåâiølàµ'§ï¢Ëù¾ûñÇÏðóß«n+o®?ß|>jºr¿¹½º¹Û\x0017(4YÄ1k»ûÝ$X[\x0014oÔO9ß¾={{Ô4ç~s~röª
Æ=Ò+¸Üze\x0014\x0017%z\x0014IòbÁ	5¿°E~RL\x0013ÖÇq7m:7(n¤åD pIëî\x0002sÏ++x"Äøø\x001aN(F\x001dWïYò\x001cE3×Çv·ôÈ\x001cç
¹ñ(Ê\x001a*\x0018{_òøú©ZøvÞ-ý
néD1«¹¥G4¤®#å×åôh|x7í
yÁaB>õ,ÈU).É¢¹Ó\x001aá\x0015¸EØ~\x0014\x0017°b¦µö\x0019=z\x0004î\x0001aí´\x0014cv£q?<¸^c^T\x0016º\x000fùé\x0015°Ç2ãNckpñz+×^
\z çv|yàv9\x0016¦÷³nX÷ñð­®iëC<pï¯ï®?ÞÃgP<ÒsÎ>âlk¦Ãy~ò"\x001e¶\x0017§¯Nß¾ÝþTqQïú..\x0008¬\x001f\x0001¨¼B5ÝAË¨ä½\x0013ÿ1\x0019­o\x001f.?=þr}w³çja°\x0016Braã¨ÈæJa=5FíwG¯ß}súêìbÍ¼³|ÿÞÍG¨þû?þóäöú·½Á©è7å³3úñÒ¶<úS\x0014\x0012S\x000fWÛÑÉùé¿mÓ\x0000úøÝ÷¿ÞWCWÂ\x0015éÅÿè«Û½\x001acÆ\x0018ÍMµ\x0002ê5êKû#¥Ä¨Ê;|õ?úæìä|ÎXEúDÊ²\x0014µ\x001eòS«·¥ëµä§ÌxÇÝ®fÙ
úDÐ²sH]\x000eT¥\x0018\x001f):Ç!å\x0014.5}¾\x0019\x0007}"kÙ\x0007ªý³\Ù¡\x0002`<t8MANÕäÇ9s`c\x0013\x000cOD_îI¾v6èäüÎ\x001bá·µ\x0015¾íMs¹\x001d)ÊP\x0007ÒÉ·O¢5û«òdÒTÄóBL);¾7*Jäô\+§þòJæy\x0019¦®´4E\x0011/TÒ¦|¯PÆxwÇ\x0001ày	¦®eAý9PELX\\x0017\\x001db§u
+çõºÒê6ÈNÑ+~ç\x0001#½B5ÈóâK]È&WªGw ®\x0010\x0012Ó\x0017¢7pè¥</½Ô\x0018hyû	\x000eÞF¿ÂC/yá¥\x001efç³|*³¦<A\x001f\x0002'xX½»ÁÕRæ\x0018yýÓ\x001f[
óÑ7W·WwoöVfyI\x0007\x001dæ°²Tdsa÷I\x0017\x001d}sr~òêíÙ«% söx9¨bo\x000cËÕª(üÃ¦Ø¸éÝz\x0005ê\x0019^J^Ò\x001b\x0012KÊ\x0001gçÝýß;AçÌïrÐ"\x0001\x0005Ô+pö=g0ÏÕK£ÎÝÅ¨°I¶Æ:Q\x0012Ù\x0012jcq÷l«.Ô9s»\x001cU²<,
dætf\x001bÏ³}\x0012U]¨sVv1ª©^¹\x0002¹úV\x0017\x0001Ï}þM\x0017êq]jèÁ"`¨U).\x0014f\x0015>3Í\x001c^:§e·\x00185:·\x0014ªp2P¨\x0002³ùâ½»;_\x001fé¼Ýr\x000bà¹\x001d|ÀGð¬]'x\x0001¨éëí
ÖYÙº¥¬Øì¤ßÒ[fEC\x000ehìUìbÅÀÆðiBT×\x0007&\x000b?aÚ\x0015w:1{ºâu¢Îêê-G¤¹]\x0010=\x0001,\x0013ifÞÇ{IÅ·\x000fNÔ¡¬êµíþ*\x0002}ÚÃ\x0018ÇMsþ\x0008\x0006ÿrÿ9Z`äg¬i÷Úêµíâ$þ\x0017¯\x0017ñMÞÉò¹gôliåð¸#Ù\Ã1¾§)\x001aKù´ÀlÔ\x0004(¨\x000b\x0006HÎÅ×ZNû?ñM\x001eò\x0017ò)M:d\x0002=&\x0016Â3ÜsuN~\x000cpò¿\x00100\x001e9RÓ\x0000tÒ$ã\x0005(§÷ê1ÀÉsþ2@T\x0007 EôL¢IÉ-\x001d²3Ý`9 \x00174t\x0013ºh\x0012C\x001eÂ }~+\x0005iÙÓ(,x\x0008ÂMÂl?¢HaÞÜC2I#¢ñåi\x001daø#üúCef64,´0ù\x0000»Êl²\x0015lj~Áç ð»R)iho\x000eBE÷Ì8-	eÚÀíå]¡Ý\x0013ßOk1\x0017.}Fy·¹7\x0014¶LÐ¥©\x0018Qz5ý®à\x0005ô4Óg×ü;\x001f\x0002u£\x0008ÅU¤Oi¥kß«Çü!æÌÞÜ^í+^ºáöAVyTÂM9ýßñQ&nâe°ÔÔó·[R+ª'*fK¨\x0000JËX< M~Q³!P¿s%Õ\x0013
³ETÑ\x000f×Ô±JÜ9\x0006Ë]X4T%»UTO\x0014Ì\x0016Qa\x0003(j^\x001b
¹"*öhµ)vî¤z"a¶h]IÉ	\x0017Ø9Kd*Å­°käJ(º]w
UüÌ[Q\x0001ä\x0012/­<VRÑEºwYeË\x001aL©Ë4wÁÖÓçàN*º3÷M e*ì@fORôAc×UH\x0006­BúôAaF3ùRñòæIÞP°,³iÔ¹ÅÚkE-\x001eªéÓEfãYJùPØ\x0001Ëd²MRi\x000bÒ3`\x0016K\x0006Óç/7`H>52*BéÓG¦\x0002æ³%2EÒÐ\x0002ûn\x001bÏ>²Ù©t\x000f·7\x001f~ù;>E%Qm×Téß^\x001d}sóÝÝõý§»o÷\x0015pCt&´«!<óä\x000b«¢]=íVÞ$\x0003}söÕ«Ó×¯¾Øãò\x001f<6kBãôÙTÐ«ËaÔ1\x001a¨P\x001b¡`,Kq1ò®ÒüÔ²\x000fþøôýOò(ÃÕÇ÷ñ¹zÜë÷\x001aÇ
8\x0000«¹ÙKçf'ÆM\x001f^ÄëÄó×¯^¼Ûîùo½üé»¤%ç°LR¾°\x0012§W×gÇ1\x0017²é\5\x0004¯;0#i¾° g©\x0000n¡9ø'Wàª¬e\x0019×£\ä\x0004ÅÊãÏç\x0006áBR{2Ã¸¨Æ½\x0000)"\x001f¥Ô¹âòºÁ
Ü"¡?+M\x0016tC}zÀÄ
¥³SIß5¸(ºáÅ\x0000Ïl:\x0008ãRÏB.(cýaç§\x0015yÝ°w×JÿñUÌ0=\x000euµúÿÇ>|øôñúv_x=zZ:\x0017\x0004\x0019¸\x0013\x001f(\x0012þ\x00136\x0015p.9n§/^¿<=ß\x000b8WÈ¼0:ðXn \x0010\x0015Ë2¡sSiâÅ?¼\x000fw¿~Dy7Ô#IÍYô%J§]~ºHW{ë\x0007½ç\x0018\x0002æû¨\x001c¸¡t<Lwè|òi¯/â{²+Ñé§ïo\x001f2O\x001c¿½¾ÿ}ßPb3\x000f\x0003Æä¶/èËk*ø=U_^üm\x0001O\x001dì\x0007øÜF@4³$¾Ò])òíjz½/hÜ.\x0003|zãÚ\x0010£2[ìðP\x0004Å®¦®KùR¬;}z\x00019\x00154Àí\x000eÃFzFe9 \;ÿ]'qúðÓÍ\x001d\x0002î\x000b\x0000E¿mçÖÌÚ·ôjØszùæì\x0015r\x0013¾l¤¿ÿðÇ?~ß=»7.e\x000c7È¢£$è\x0019\\x0013a*¿9Q©;2g\x0017PbOÎ"M¬tÉ¾Ô
QîH]@é4çrkTßñý K*ò´å\x0010åÙ\x0005Vbx7gÍZÞÀÖ±tÓ^\x000fC;2f\x0017P²±?P"\x0001±TÓýåÿºwM¶#7î}§²'à\x001dx$^ÑvSL\x0007Ù¤øè°î\x0017Åf§\x0012ø¥óÉÓð\x0010Î8îL<\x00042QU«Ö*dÕ¾ác\x001fÕá¢Ü\x001d¿B\x0001D"óé³ÿÇ/µ´tå½ÿüóýÛk\x001b1
(q÷òÖ¯z4»ÈYg·ÛÏ¼üÝÝ÷y\x0003¾ÄQ§~3\x0007\x001e\x001cA
uÙb2Ç§´t³·ph¼( 	\x0003Å¬³\x0001t\x0019±+ÇÇ\x0013%\x001a\x0010¼õü®<6X\x0017)}M}KýÐã\x0006!i);º\x0003\x000f\x0017å±u$ê¶\x0007Ä+\x000c\x0001qª×¦j\x0013\x0008ÖöÇV\x0010¼q\x0000ºÉ³Ü\x0014\x0007\x0014·\x0015òfÙ\x0016l\x000bÅðNyl\x0004	yDÌt$ÜÁ¥|Çµ\x0005$O-lÇ£6Î·\x0014+1¥ïf­âV\x001a¥¬\x0000$bÈ¡<¶3Ô¯(\x001f5cë\x0018ãyÑÀ\x001e¼[@\x0012:Øå±\x0015$o¦*M®éÆØñÔê-eeì\x0006\x0010«qáÖçV\x0012¬Ï¦Ù
£\x0010 |ï¬¢Ä Y×jõ¹\x0004;HU\x000bÏ3\x00147­\x0013KGm\x0013\x0008n\x000cõ¹yØÚJ<\x000f	6H¤>9ÜJÜz»#o!1*/úÜ<MRÍêÅãª \x001bN\x0013N[~\x001c6¹>7Û\x0012¨ ZWSó¶Ñ&Q³)\ ùÕþío÷ªyôOññûo÷¿â½nÌ¹yu5\x0018S\x0013\x0019ÃYL7I\x0000\x0017YÎïßÜ½Ä¶$sóêÍ97¥á%ÔH-\x000f\x0001ÞÔ
ïheåm«õÝRjq\x000cO+UÒ\x001b/éU\x0014pÃ¬Æ\x0010iÆp)A:ÊW$ÊSÀÿªñMM½Ã{°©\x001aéáò9\x000c
§dü<gPj¥\x001fÿgïy?\x001fz¦õ)à\x0003UßðûF^²Nñ°¼Ò\x001cåeü¢lü¼¯ç!lØ+pÀ×Óàv|ZUI\x0008Ùú¤\x0017]Õ\x0015ÈYp¾ñå	}\x000f
\x001fÈÆÏÜ\x0002©)¸6|\x0002Ï\x0018äQ:¬­Ïa:¼¨f¿\x0002\x000fl{Y|`3ÊW.!ÊSÀç\x001c'³\x0015ÅBâsÍº¤å&?Ê\x0017Êì\x000b²ÙM
µÄ@>\x0012ÈNm|{­\x000b^¿«OÉø>\x0018ü})gÉ·ÕáÎÄ	\x0006ù)IæFb]Ê!9\x000cmyüÊµ,¨Ý|%²<\x0005|"¦Dðí\x0002,poWçw_T¶ÿ®>\x0005|Ù% '8Öv/éÆ·Ìþ\x001aä³¨S\x0012>?ñiîì\x001a\x0012[Ü\x0019QÇQ>(\x0003ø\x001cç3*\x001b=>WQ$ºëmüÔ9ýåç·_Òß1fååñôþæÙýÿ¾¿bR°\x00053w´Ô¦î\x0018¨È±+íÏäÇÜÝ<»ûî.aD\x0008å±	\x0003\x0012VÒ\x0014
y÷5`d"®ð¶}B£\x001aåwõ¹
\x0003»Ç¨É$mx4Ôîã[8|áðÛ9XOÕsvµ÷)êøi8\x00060Â_þõO;+\x0008ùâ\x0013^\qÙ§Ð4&z¶äåÏJáÙj5ÅûÅs¼5¹Luª\x0003¹Ê\x0005\x000c¤\x0008$p­:\x0013²Ùôk÷'ùIÏò\x0012¿v\x000e¶\x0018­Qõ\x00163\x000f1Çó?A#¤Y~®gyU=\x0005þÛ¯ÿxûó,9p[Js>uÓu\x0007v_¦KéU"Uý/Oâéã\x0004æ%\x0004N?Ö$¹é/¾sS»rT¬ùøñÓÇû+\x0017Î(à-¼©E¨ÉaZ\x001aMåe\x0004\x0012\x000enî~øáù\x000fw ¾\x0013´¨çhQ£iL\x0015®«,ï×¤ °ô:£ìvÆj:§p¶³\x00028¯9¶ý:\x0012êtJ³¢û\x000cõS¶vkz
×}Ô(ø¨*\x001b%ªKÑ!Ñ
`ÊSÊ5Ó(Æ¶ê;4/\x00187,+£ª[·\x001cÇé#&¥3]°6~ÔÐÁ\x0005Á¸å=EUSª³ÿ^Ó	\x0012ßWtæ²oÓ°¥î&Á\x0017Õ\x0010¹Ûv6§·¤\x001d\x001a=Ûx\x0017®\x001f5­Ø

¾©c\x001fÅdSk\x001c}Sª¸Å]YJgbG
¤Ã\x0016\x000e\x000f\x0015¼R\x0013\x0017ë8O]®¬ÒË4°t¶³qøS0v=ªx^Î³\x000bËxÔV8×Ã6\x0007ÇëÁ\x0004EêFycç[&6²~Ò\x0005Á¤ËÛ:\x000b=Z­ÛgMiê©!¥Ëÿ®9\x001dÅÆ-¾å~Bª\x0019Q\x001f¬uì±K\x0015«-$\x001fPæhøs|à²H"\x0012Oòá Øy
K\x0015Çm\x0003gt7åð§\x000e0®Sè\x001c+M$oyA,\x000b¶²¥M2åÜä+%h#g¸¸Ci²Îv\x000e	þ\x0014\à	6E\x0016ÍßOgÒÆ7ÒAÿ]Aò]k<¬~W1ÚB\x0017ÚwUË\x000e[\x001bé|¿&¼`MXEy.:RâI;§ÙìJÇ®÷æÄ³ÙQ¢\x001d\x000c{ãQ¯\x000eEÝ\x0008pÚ]5&+p©ÛÀð§\x0000NqÌ\x0018°©\x0003-ØÄga-ý®ØHx\x0006?á ïýÔ*\x0008\x0005%Is=¶rí%)[éLO'Ø$P\x0000ÂaÖYî]\x0015\x0013¶&	Þ#Ì\x000fJà©;(µ'eì°+AõÔS"\x0019
«K»L\x0011U\x001d\x001d\x0016g
ÓyÎéR(liIÞW³WEÍBºØ}ÙR 5LZ%\x0014òkò\x000c79§¶¹\x000e£\x001e3º\x0012\x0004\x0019¥\x000bùs\x0006®Ó2j\x000c&¬:±ße£dõ\x0000-C ¯
ú²Ú²\x0002^êØaþ\x000e\x0004;E©9¥\x000bn,ô¤\B.0\x0002³L%Ü\x0008çú\x0013»`H\x0010\x0011+|­ÇS\x000fí±p¦\x0001ÆF¸h$÷ÅÜX\x0000¯\x001dåqqf\x001bÎF\x0019\x001d&qÍÏ×FB\x0017}\x0015cÃ÷V9ÝMN¬\x0008g:o£\x0003èèòÏaº\x000cw9ô\x0011ª÷Y3Àj7)\x0008W,æÉÌé¼À\x0016Ghw\x0014Ù«]#ÕR×&èJL\x0017P\x0002¼¤\x000cgÝ\x0006h\x0015ÆàZÊÂRf}#î£\x0013%gf.[à@\x0019\x0015*ÊÄ:õ`E©\x001bñ\-)3ãxÐ²/Ã\x0017[BJ´2\x001f¥dÈtx­,¹0%ª\x001aN,\x001c<õpÙ\x0004\x000eOâ\x0007$4%dóòw¦¬D\x0007|b,]ÂExúdehÑÊ ï\x0013-\x001e5sp®e³.Ë·¢Á	Àâ¥ ±\x0004²¦RÄ\x001aÞÁk\x001bíûx®w%Wf\x0010\x000feBÚM¶ª:Z-Ç.ÛÎnÄó'£çÇG\x000f«h¸\x001có(½If\x0007OèCÌ\x000e/Ï;<U9Ñ'ãê=»·,.w.g#^:\x0019½$\x0019=ì·Mi2Ö°Íóýcw¦(n+^<Á\x001bß1p¨jNuôªÆ±c\x0005ÞRßp\x001b\x001e¦ítáv3nó0uSÜònkèÛr³rÏäÂý\x000cv:º \x0018<ìÂF^(\x0016\x0007s	û¤&µzæd¿0ýÂk\x0016¯­	F\x001dÿ #Ý/l\x001f¯(¿Çñ°Å\x0001õÿñ¦6BÍ\x0005NmÏ£'ÜmÑ\öxoë='Gã·méO­ÞÌ-x6âéÞ¬ào\x0001^¸MÝ\x0016";ñQñÁÖyaP@[Ó\x001beü=Ô>nÝpãûéËÖÜáYÁ%×hThaä?jê¶«[¡Ð c¢X\x0007\x0007ãw¯âÝ6iÍ¢kÑ´U¥¬\x001bñÂÉ%^\x0018\x000f\x001f{SK+^`aV$o³[ Ümí\x000bo\x0005.¼Ï§W\x0016èÖí,Æ©	0j¡ó©¸ÇKã\x0001\x001foÀpÕWÂòïj±M\x0017ÞRïb\x001b;99ÁùÌæÆ|$ÃÎ\x0012(i]îØ\x0006O\x0006çû\x0018mù=\x000eÜÌ\x0015¨ò6ÚhÏpvn¼\x000e5 ætE\x0013j.hE6¥\x00052jâ"X\x001f9¯ÒyÖþ\x0002õ\x0006^~{GZUOß¿}÷ùþëûkÂ­áw(rÖÔq!qk!ëÏ\x00187I©êéï\x001f¿¼{ýd®Ýz
içV\x0006Á¨Y·þºãº\x0018X\x000fÁÆe÷\x0018#Ì\x0019AÄ÷\x000elUà\x001c\x000b
´aÔnéQ
!º9¢!*E­w\x0013~öDÃèÉ+5öLÓ1H?ô2H\x0017\x001b¤vÜ-\x000e<!ÏÜô
A9d\x0010B[[{j¸\x0000\x000c\x001b-·\x000f¥ªú\x0018c3Fá×[ZØÆ²¤D\x0008\x0014¥7y\x0013Ýù±Ó1É\x0018óÂ¶ÔFE%nL))\x0015\x000eÜR^}\x0008R«ÎD*\x0019%^d\x00192?R\x001eòÒæ\x0019yær±7ã2;ÞDJ±[
45*voòHî´ãº³ãZfÈ}²­¹QtÙ)9a	ÎTfQv\\x000bMy¦HKª\x000fÕl<Ê7DÙ\x0019s-´æ)¶¶NyS$\x0013Ä\x000eci¯º\x000f²³Zf(Qf\x0018hZb!qÝr¶üÁÓÃè\x0010eg)µÐTFËÇ\x001c\x0006\x001d!ÇúL$n²³Zf,¶·¥ÄÇ¿¸;ãH@ÎV\x001a­Do×ÑÚñºõÎUl,á,Á\x0018eg-ÌZbG\x0005X`W}|îâ>SgºzA\x000eÒÈ ³»F½ÐTëò\x001bg\x000ep&T2\x0004ÙYt#³èäaÈ
%Í\x0016=\x0019¦tf§ãk:nd\x0016\x001dÛSx\x001eËXÏ¯8+¿æôNÊÎ¢\x001bE\x000fØò®®\x001dÔ8¶Õ¤cÕ\x0002¥[
¥üpÿ×O_¾.!;÷ÜÈüsÔ\x000e4ÚsßÃ¤&m§nº}Ç\x0008÷\x001d,ê©#i55JB &[¦F¨Ûul×	Úp_6Ô±&¿¼7¶\x0006RË2ø1Ên×1Â]\x00074;¿\x0001L£ä\x000eÙ.¹\x001c´Ý®c¥»«YúµÅe¢I©Có+wî:¶Ûu¬p×\x0001_ûSä¡t
Ã}Ò+^ßaçÒ±Ý¶cÛÑXy[ýJÌÅ$Þ!\x0014;ÚEÙGû\x000e´6q\x0001xy,¹ÀËÅÇvû\x0015î;8\x0019ÉÑp®ÞdeJ\x000bì¤'»ówûî;©&¹b¦­U8Àk|ßAÂvÛ\x0015n;6´~ÞT	?9ÌGòLø~²Ûv¬pÛq¦íàÁ°Ï\x0019þ<;c\x0005¶Ûx¬pã\x0001ª?Ä±L·ìfð¾Ï\x0011;²Ûw¬pßÉë¥jh8\x000cZø
3\x0011vAB·ïpß±5p1ÈûÈÞï\x0019©ú1Ênß\x0001á¾ã÷\x001b³#¬XG °¼¶9Ö9DÙí; Üw²wèx,·©Î\x00067=i?\x0004Ùm; Üv0Ú[\x0003¿\x0005¢2\x0004Õ±\x001boÏdy£\¹Òþ&B¸ë\x0000`¼·6üÕm×qg¥Ý¹7B·ëp×
#-u(}½/.Ê	rchhm(»m\x0007Û\x000ez¿ä²¡¦\x0003{¿lÜÞà/tÛ\x000e\x0008·Ä÷\x0012¦	RªbïÎ$Ïd·épÓqê\x0006RS6YçcÀR1ml »M\x0007dNÔ¦\x0016#¡Ð¿bEüx$ÃÆ­qe$]·é8á¦ãÍ9úl(C;F¸¥ìÉÐPºnÓq²M'¢9¯s2åSïlân\x0013ÎtÜ\x001a£ì6\x001d'Üt<`Pº\x0006
JÛº5\x001aÞtÎ\x0014î
Avm:¨\x0016J^%æÉÛZ^¨[  Ø[£ëv\x001d'Üu0ï<6o¸\x001dvìUî¼£wý\x0005¸lÏyøIÙm:N¶éD¼À³t¶õ¨DEVm%¶\x0012ÛEÙm:N¶é<ü¬ì¶\x001d'Ûv0³ú? ÃA\x0005á*(vØÔÆ½q²ÛwlßI(DýQJ^s\x0019JJ\x00047!.ÕX\x0018}·íxÙ¶\x0013³+\x0019h$S «¼Ó4EÁb\x000fe·íxÙ¶©Ô-\x001bÖÖÑsÎe[
Av\x0006ÝË\x000c:~n\x001d[\x000f~ï\x0015/ÃwæÜËÌ9.\x001c§É§´ÓÂáuãÎHd\x000c
dgÏ½ÌcÛ\x001eMë&#ê\x0014¿6ùkaoöï,¥YÊÝ]H¥%p[lc\x0012*#ìLzð¡ôBC	Ñ±'T2¼¼ÃÎ;Ð­ \9ÝP_\x000eå>/#tK'ÈNÑã¯g¨miV¾¬	f©/;FÙ­ \;Ø­TÈ,
dàÞòiÙ\x0016n°óÌ\x000fB·"\x0004É(Ê%H\x001bR³\x0007²Ï\x0004\x0014-nÿ=5
õJ9\\x0019ÉÄa«\x0004gji(»Õ\x001dd«\x001b
%ÝÚ&«¹ÕfeÕì¬í¼ \x000b\x001b\x0014DnÃvTø£­Â½ØkÊ°à\x0019È\x0011ÈØy\x0018Qäa¦qÄûLk\x001a\x00178\x0002ö^ÆÎNFtù\x000cÏµÚª\x000c#\x0019y}i9FÙ\x0019Ê(2NYJ\x0007ôèí7Jk2\x0011ª\x001f£ì\x000ce\x0014\x0019Ju¤P£3¥a5,õ\x001e{ ;[\x0019E¶2CZÖäÀÊHþÞ\x001c¡¸{Vv¶2
m¥\x000f·$«­¦'½Ð¨ÛÒ	»ç±Ï\x0016YJ\x001d»CUüÑª\x001dk'ÈxFÓtÓ@jWD:§¢
lÅÄ&èÛÍïß}ûÇÍO\x001f¯ttÅ>TÜ,Õc\x0003_Jüô®%à¬Ä(ßÜüøäñ¿yñü×ëxfg\x0004xÑWå\x001aL\x001f0·\x0013UK\x001f8¶ÙFgçtV@g '7d×LÕ«îè¦D°«mx0Ç\x0003É·í\x000eÌä£M¤DTNL\x0004¿r¸
ÏÍñ\x0000Ï%\x000eSàè\x0005Â\x0003N\x0006eW\x0001:?§óo\x000b·>´$ CÉåO0àWR\x0004¶á9^\x000cåì\x001f_3¿jÍHÔ¬Û8Ç\x0012¼xËùÔØ¬û´+Õ"ÛàÒ\x001c.	àL©úâê\x0006O6OAxg´	7ãME"Å$+\x0001_><iÝ¶oÛrñÏëlÇëw\x000cÉ§Pú¸ÚVç \x0016\x0013\x0003·rÓº
¯Û1´`Ëpù$J)^yîs\x0010PH³swX=ÝY=-0{ÙâK`J\x0018T6Ç'<\x0000³áëú,L×\x0015-°+.µæß®ªÆÕÑãH\x001dØ-veáRÚ|r ªâ\x0015ïÑû_ßa×+-¶ó¦¹Â+D[5X·Â¹'juG{ôäÙclyò¸ÁÑÿß3jÓ1j#b_\x0018Ú¦£yøÞ¬óma´§Yìö4ýÑçOïÿ~öþË
Å°x1¨XÅpßí½¨öðRdöÑËçOþ\x001dÿüìÉ«WzÒTÉg7öô\x0006sÜø\x001dÖÑ±(&7\Ç{Éµ\x001e\x0006E$ìiDb\x0014\x001côTêÙåöÉp\x0005`¸\x0014ÁÝN®õI]wþ\x000b<"<úåÝ¯ï?fÞ/7/>ããÝOßþqå £\x0001XýÈ î0ù\x0007âz<~ô¯=ù!³¾ÂnÝùñøéó7ÿ~Æ´\x0012¨\x001a)¨iZ9:¶6\x0012yÐiB§3äGAÓ\x001c4	A±o\x001dg¨@9,ÉjÓòè`\x0011®X\x0001íU×rZjHKM6Ùó\x001cû\x0001V#l-ZìgçxêþÃãO!ª¦Tê\x00035\x0006+ÒãNv¨SnCAÅä\x0006ÙÇO©º (°kÉAN 9µ7I²\x001aEM=ªtjÌ
â¶\x0000±
Åàâ¢Ëx¦}Õ jê'@N\x0000UX²º\x0012Ð
¿÷¡©¬±\x0018)¬k¡À­xðfÙÓêçTß¨\x0016>Â è^@1\x0005]8¦\x0003D	iH9Ä\x0011Î\x0014þÚéJ\x0002Iñ§\x0014\x0012\x001d×c\x0002Ü_ËÅ	ð§\x000fj©ò5ÊzN±áÇ\x0006%dø±ß\x0018Ý¥føýR%r\x000c\x0015R7Kñ§pHâð\x001bv\x001e¦&9º\x0006üô1Tç»¯?e¨¨$DÑ$Ìc4@Ä¥ÂÎ¹?8ÚO\x0000'\x0000½Ô<å¾ä\x0001\x000egàZµÑ\x0019\x001dÎ1Toº}

Q!ðñÀçÕÏy\x001bÜÃ)ï\x000eKñATèæ*þ¢ê¦\x0006á5ïS(ôÇ5=Ël¼Í¨ö4ÚnK´ýY>Pÿ¿ÿ§\x0003^ÝûûußßæA\x0004²R[ABâ+ª õâÎâY>P?.Þÿ«»7?¿\x000c°§Ñv[¢íãx\x0011¸\x0002%¢måsÕF|ËÝ\x0001>;ç³¢áRÓóø9\x001e?Ýø\x0016Ûæ\x0000\x001eÌñ@4|¦vúD<ÒcÇáS©
ßÂ\x0001ÝÎ7\x000bîØ\x001aÜ\x0019\x0007ô¦J;×ñ\x000bõ´¥¤mü\x0016kd; í¿¯è\x0003O%o1:¾ï)B.´/Ý\x0001@ß\x0001z	`Æó«Ñ6\x0016ÀVî\x0016Ì)8óÙ3 ºìãyó£\x0010\x0019
vÖè,´¦ öðM7àÈ¶`Ï¤¢ÌTùø<Ï\x0010\ÄêÓ2\x000fg3 6Ý\x001a.³y\x0010%vy\x0015\x001b®Ê²Ð\x0012hõÒØNh»O?\x0005`y\x0017	U2¬1í\x001b/7åíÁõfFòuTU½\x0013+_\x000c\x0017:å¿ç\x0018h\º¸	î÷9-ÙéLu¼Ê:®=>
aËä\x000e~y³¼Ðtc?\x0005ch=Ë\x0014¢Ä¨¯+9oÀ\x0017Ê²KÀ\x0000aè	%»ö±|W\x00184°\x0014lßNh»¥?%ó°ä\x000cÔ^_%å]QxàÜèeíÃfBÛ\x0013Z\x0019!ñÔ0QØ¤|dîóq¶çâ\x0000 ë\x0001%Ó\x0010c*$ÉfPë\x0016¨XfÙl\x0007\x000cC?\x0005\x0001ªz"Æ§4W
incâRßí±['øS2%¾1±ª&"Fm8õ4zÑGV>üñD=&\x0014õ\x0018:>ýæý×r)±¡Ûxö»<_Úl\x000eë9\x000fÝ\x001a\x001aD³ô\x000bùìôäu¹¨­Ç× çL¡T2I 5°j­\x001d\x0005R±Í6f9#z®÷\x0017¾Ã\x0012Lì\x0006J\x0008V%Ù<YÔiy?9ïÎX¾¸\x0013ajlS?¹É{tmZ\x001a5'~i·\x0012[OÍ(K'ªqJ\x001b5«Ìæ\x0013\x0015Ð-I\x0008@	²:\x001fýVãz0C\x0019Ê×îtXs®I\x0012,cRÛw}&\x0003~òoß9%Å¿\x0012À\x0006\x0014ð\x0004«H¥9\x0004í-Ã®Ç:Ú{'w"©ÿâ»©­Ùïß!É5¶êÐ&Ù\x000f÷<¤ZfÍZ³\x001f<Æ¿<¸qz\x001dæèæy\x0004+\x001f\x0004¨Ão>\x0002@Pf¥ËfkôZ÷Á+\zPz­n\x000c,bGijQ8\x000b6d7û¬®©ø_å=W\x001cäÒ\x0006ÏvËsâk\x0008±5â3å\x0016[ÀÌÔCªÌ¯©ÔF0\x0007XCSkÊë\x000bÑ\x0006nÁW/ÛÀ|èÀ¦¾ÛÀJÓ²*<o\ AÎ<ï\x001cµ\x0014P°Ö¥ñ\x001aXð\x001dØÔï`\x0013\x00188g¹¡:f\x0001\x0008g0Ô\x0003Ñ¤Õ~`\x000cvÎN`DbNÆ¨,Æ'©Ë»¶tßM]hÞc£;ÑhÍf§ªÓ<ô\x0019ó¡(ÕùeZmLH\ÑaóÇM|\x001b»\x0001³qpÀ\x0012ª¼Ò=~ºu¸8§?­v²¼Æ:oÓ ÅOÉpfÎ®¼®Þq6@-ÿLýê\x00160èM>\x000cÚ|ÀÒ\x001cÅSÌÑåWÔ­å¼Ðâï¾#þ\x001cÃ²mÔUE²ÿÑ\x0012\ôZo+`Ît\x0006¬\x001cFÀtö%hæ+ìøÍgY%%´¬.\x000eljRµ\x0011Lªmi\x0001\x0014Ê´÷À\x0000k\x001d«¯pyè¸Àæ\x0010\x0017ÆgëTX{¡):Á*ëx©%\x0003óÐMÝø¶ap9ó¿ìâ:Aó¹ÆØÆ:ÛêÓmìgqÏ"eZ±Õ\x000fÒv­WÖU°Ð
N}cCÍØÎ`AqÖ¬mÏ1Ñ-Þ\x0002\x0016zo:\x000cºÓù,ê9\x001bNYÇ©äù´¯yî\x000býé\x0000\x0015\x000b0hÅL0Õ
CÑ\x0002ÓbØ¥rò¾$³ú¡7¯aÔ¼æý\x0006#\x0015¬¥[îoÁÖú(^\x0003ë\x001d0èð@öDøb'M×\x0012\x00006\x001aQÎQ\x0002Má\x001c\x000caû\x00122\x0016òÙÁóxE}FZq\x0013í¦~´Sßfï°°Ë\x000f]Y®Y\x0015Ïü\x0008ÝÉ(ÂØÉ\x0008ìÌê\x001bj\x0012wØ,m«S\x0004Lw2Jfìd\x0004ØmEL¤,KÍºÆ3ÉõÀf×\x0008VdmÀ<{®ÙÎÖºÞÌZ\x0006ªÌêkÝÏ°ò{ìd\x0014\x000c7ÔÕ\x0005$bÄ®ð«u?bå÷\x0010\x00196g¢LH"\x0017T\x0004\x0013[ñû¹*Mdþ$^á\x0007÷pyçZò\x0018Z	â\x0012\x0014Öú«]!3ÐM\x0003_3#±Ø\x000fv½T¸\x0001VûÒ]#sª's+\x0013Ç= È5º\\x0004Ìµ![\x000b\x0015®ÞM,¿Ç¸²¯Ã
\x000b xeÆÀéBçô¨·p%Ós¥AÇ:\x0018Ëã"ó¤ö\x000bÔ_\x0010±DÞX~Ç~áï1°ÚÔ¢\x0006\x0007|S½2t\x0008·êL4{#;!\x001b\Ed\x000e»ùÜ\x000bÔäG¬Â»{\x0011ÙÁQ¢u¤E÷F®%Í¾\x0019¹3uþ[È¢î¿fÔ_\x0013\x0013ë~étdÉYÝZ\x001aF9óZ\,SÄ\x0013ªAÿ\x0002E\x00124¬HX»kkþØY*k{*;\x0018LA*nºìÈªFEa1\x0013ó+¹~¼J\x001fñ\x00012Þa¨3ß)¾Ç[P_F\x0018\x001eÐ)öcVÔÚÈ@q\x0017W¬\x0019ó,ÃA9í\x0016¯¶%df&LUcèaÌðcÖ/ydÎG:dSA
2¬U²!3ª%ßc`Ù»ðuGÂÖ<$É	bÕx	+ò{öÝÇ,¿ÇÈ²\x0018\x000cî\x001dSmÌ\x000e¦'\x000bc»¥+erÕõÖÑÅCrt³Öiý¶	,¥\x001e,9±\x000eÃÁªZ~OËÒÈXé@ä\x0016,\x00037V~\x000fa\x0019M%Ò^\x0005ek[o¬¥¸ü\x000f­µD¿BfC?Çl\x0018c%Ý\x001a\x001bÅ%A9nnµlöÏk_*Ùà§Ì»NUJÉc¢÷59?\x0018òúÏéGmá:q.Ì¨sá,êË\x0018âRè\Qñ5\x0012\x0016@ÈÈB?Ëð÷\x0010\x0019¨ÀiM¥ÃFµ\x0017\x0011Uê*[¦Pn"ó'\x0017ô~0¦è°h¼~¬_òÕÆ&ß:Ç{Ñ\x0001.>b\x000f6\x0018YqÎQ®\x0008¶î.É-Øõ<'èc:8£ë±ìd[ò£ÛR)P§!KM@-%ªM±¨:)"K®_\x0000É
.\x0000Ül5þù\x0013Öû"áHcæ£\x0015\x00193ÛiQ`+.=\x0016Sw>X% T¼"4ÜÃþÔò\x00160ÝÉÊï!0\.Ñüwµ¥\x0015ÞÙ³ßïÎè\x0016m\x0002ë¿eù=\x0006g\x0019mäIC½°D0
`X¯ÎtfÙDæOÌ\x000eYôå\x001a#	îøü¯eGÖk»	,¦\x001e,\x000eîKxìµ4É°9oþ&2Y6¢\x001dÓ¤©ØÑ<\x0015\x0017°>¦u¥#\x000fYË\x0006ñFfe­1ÐAß\x001fÛÐ9Õ¥1QW\x000bëe~lù\x0017t`atúcO´âýh¹õS\x0006Îòé Èåh:­úS§U/>½ÿxÿåZXÏ
~#×\x001axßÚü¥æãÿûâù\x001fî^\x00195uZô§Nþ¶Ñ\x0019Ë*q\x0011EÅjØ33q9rX:gÛéâ.Jè<µÞÄ¡«\x0001Fß\x001ajø°Ô\x001eØÌ6+ÒÀs\x0002¸\x0010Y­Wa?j\x0012ÏáPv¼Îv\x0012k©`¶pV4ã\x000cÊýÕ2ºVã=ÿZJÌl\x001e·ÙÍ/\x00060½\x0000\x000f¯2§\x0002«@\x00028­V_/\x0013E6ÓMÝ(Î\x0005ÉàAÇq4¼\Y\x0006þRÍÈ\x0015ºØÍ¹(sØéÞ×½T«HÞw	Î$ouz¦[f\x000eëG.ï¦Æµ¢*ª\x0015	VñÝ¹¿T|xyè´6=ÄÔa0Ò²p­5e^¯\8ç\x0017)ÛùRÏ$ëBqJ>n­tâS+J\x000bËPÌf>è\x0016\x0006þ\x0014ðE¿×\x0014\x0004Ë%\x0003¥¤R\x00109qÛùúñ\x0003ÁøAL\ ÿ3U½M­]Ç¥êá+|¾w\x0003¼Ä,ÀÇ@¼ú'«\x001c>[yÙ¦ZmnÃsS%q\]\x001fZ]i4Ë\x0004í|±çø\x0002¡etdJà\x001bp\x001erÔr7JO
ä\x0005/Äº¸&÷
\x0016¤ó­\x0010­Dfe|¦_½F´zku\MRK\x0014\x001b/RÞ£vIÛá
^è|b>>û,\x001fÅ0OõÁp6dZ
\x0011nÆK¶ÃKV²v¡V#ÅôÈºx¹VRËãÅV>è÷\x000eì\x001d½CE:¶Þ\x000eZZpXÊlæ³q\x0001+0.\x0001i*o0íRÞqÐ¼hÂKñz\x000f$N_þ¾\x001cÔ1h¥ëìÃf¢|3©Fó2³íÃ\x0002×Ò\x0006J½pu«Xë9Åe\g3Û¿,r­©}É3\x001eð]á\x000bguISä2Ý<s,Ó%'Z\x0018ss1\x0015Êrú\x0018\x0015X^¢^sáTX\x0013TÓÞ÷åæõçOï¿Ü¼úôáÝû\x000fWèJP\x0015YpÙ\x001aÊ\x001cN \x001b_k1öêæõËçO^Ý¼zþôñ§ç\x0010N:%!æÔ)i\x0013õô\x001cMAO®_²Öq\x000eR´+Ý\x00166rêª&\x000e§J"PHU\x0017¨vT	,\x0003eâd\x0006W\x001aèlåÔÝxâO!§C\x0015ÕjpJàªªÀqB\x0004Jì\x0003\x0019m\x0004µN\x0008IÔg\x00031$WçÛò>³¾\x0007Ac\x000f\x001a \x001dÄ)L©éê\x0005Ç#
kRÆ[A¡_ñ [óò1YÓZÂ\x0000C]óØæèJ3Í¦Ç4RÌìæÐ®%0ù/òNñfÐÐ\x0006!¨ky2:\x001fK=-%Ëõ*)¹Ã\x001a\x0002É¾\x0002É¾Ê@CÕÒÄ\x0011\x0005ÎN1`8ýÏ¬õÍÚ\x000cÚ\x001bQ'5¢6ò®§þ?F·	zÆ\x001cãô½\x0011õR#
¦-ùì_V¹°dæÝ´Ö\x0003h+h¿{jáö	);!1N_Òß¢o_>I­½ò'÷\x0000Ø\x000c3/ùß»²õÏî?¼ýöþËëºär§°×N¤õÏ¯[\x0001eÆÁïßÜ=AåúgwO¿óäÕ«ó:%'òz\x0008\x0008\x0012À¸©H\x0006
ÜØû:Ä¥9\x001aÁós</Á\x000b»cW%C
¼º;s\x0018\x0001sÀ(\x0001tMóÊGBÕQçÐ±ÓË#ì&Àxâ\x000fç¿õ¢zöéÛ÷Wû}cïUM\x001f7pð$Û\x001c×¾îZ×gÏß<}r\x0001ËÌ±Ì \x0016æªÒ7­\x0001JÎß\x0014üj"ÂZ´Â *SÁ(\x0015å\x0012b\x0007¼\x0012\x0008ª­\x0004·Ò§öúX¹9\x001b¤È}ñâsó"°(å¼cs\x001dËÏ±ü(j\x001dÎTâ¢QT°çÑZéòz\x001d+Î±â(f \x0002à±èàwF;m#US¥Aªìì{n\x0007ÒÔ¾P,¨ÎélÂ®uP££åXÌá©NÓÜjM`å|«·Zf+ê&Q\x0010S}d\x0005¬WÂ@"û02\x000b\x001dÃJ:qwuguË¶o7Ó¶è\x001c«³\x0010zÐD$,\x0018ú\x000bµ\x000fË÷ÂB¾mT¡£
TØ|þ\x0010øà\x0018Øp­v´ZáºW'©#wª¦<ýô5ïÔï~}÷ñëÍ\x0007·¾:f5{\x0000\x001fn<·\x0003\x000biÙÏêéó×y¯~üìñ\x000f¯o¸õ\x0004É85sX#õ¾Ý\x0000\x0007KÆ\x0016¶|¹Ü.e¬vÎje¬Î;ò\x0016Ag1î\x001e
ÎbÈHaN
Â)\x0000xY]û-'\x0014ê+¬\x001c<G¡ÍÕÍa\x000c\x0016uy\a\x00175\x0005bXv
Áú9¬\x0017ÂÆ\x001aöÇ\x001bw`}ûÌØd`n§\x000c6Ìa\x0004Ö)Óú\x0006 Ê\x0010Xî\x001bQNj°Æ9k±:Ç\x001bcûqX¯8&ºÅÉ\\x0006æ°I6\x000b\x0012\x000bÚ\x00166§e|SDÚ< º\x0019(Ù¸ZÅÑX\x0014¥æõ¢>h¾ê~ç\x0012m]\x000e¯é\x0015u92|ã¢ÀÍbÃÑv[\x0016í].3¶ô\x0007,q x'\x00161ÓØ.Ëhñ¶íä \6·~\x0017ØMîß¾}ùúþ§kÉ®\x0011½MO+©\x0006k¼²AéV¸²0\x0006­Û\x0005öû·7¯^?yt&\x001bW¶nVµu³\x0004\x0012l=MdÈH¹j\x0019²eWCZ:|cv\x000eiÅ#Ù 5ö¡är®x¡aÜ\x0016ÈËL-C\x0005!û¨®ñÌQrsJ>8v9
Qú4§ôI6ùÌH\x0002MÑxW`¸ÊÙ\x000b
¸6PêYw{\x001cËèEèOQi	Ê\x0008ÚúÉ\x001dß	Û|8Ùi¦öÎeñ¨ ÃD÷(\x0013Æ¹\x000b¥æ|Î\oiµr(\x001ed*{%µ\x001cÀÙêäO\x001e\x0014\x0017*ØåuÖ\x0010eê&f¹\x001cÌLßtRñÒg¦æ
,©çÒ\x0006L;í\x0017S¤£\x0010Óð­p¿y> s\x0011ÃÒÅ\x001b¢
y
¥Wb»^\x000bsµ2¶6¯+ú³tÓ\x001aÔ¾ÍÇÆnóÁ"L¥¹²\x001fø¾NMk}äÚ¶e@r\x0004\x0013tgBÄ´Gö;tI»¤R\x001fMæq'Z#8õ7ÀÍ\x0013U~ûé\x001bÒ¦ÆWóÎóÁî\x000e°µQ
\x000cFÃQ\x0008ÿÔÊ\x0005Öo¿Á¿.Ï]`Á©Ã\x0001î;#¤¬w\x0007µ\x000b\x001c_Äh¹=;§r:içVi\x000cNiç+¹ñîLÏALc\x0010ÓqàXô:Æ\x0016ÜD×i'¥S:\x0019eÆ¨ë'c\x0006Etõõ/;\x0011ý\x001cÑK\x0017\x000f°ÚaðsÐb\x001bÈ3­é\x0006)Ã2\x0008\x00072ïZ(bz?o´ÄËÒAÊ8§Â±ä«tüÜ­ÉZH¤\x0010oP,b'fc&á`\x0002©j`\x000e©iéÌ\x0003 ÞQ\x0007\x001aÂÝ¨nTF9K~Gýæ®\x0012ó2âo®ãjÎÔFÊ~ó\x0011î>X\x0006È]Ã²]W­\x0010K(Ý²ÁÂ g·ýháþã0R[of£Õ­B\x0006¸Y²Ç>äû8»ýG\x000b7 §Õ-uËÍ¾\x001cõ\x0001ôM}Õñ3\x00071»ýG7 j»\x0019\x000b­\x001f%ª±á<Ó#}³Û´p\x000b\x0002¬M¥éÝ\x000e\x001cesê_\x000ebv»nC\x000f?Ý>¤\x001b\x0011X;u>Sõ²×ùÈ³óÌÁw\x0010³³ðZhâ\x001f~8Mg<Ôu8N­OV\x001160züéÛÍoÿ¼öµS¬I|\x0018ðp\x0014w\x001e»JÔËjµ&Ûò77/ÞüaY·_¡fE?(Ù1(Ì ®\x0017¶Ý
Lõ eg\x0014@Í«l5UÙ\x000ePÙ<TP·\x00170¦J`Y.M6«\x0012½©é¿\x0019¤Jµ´'UÐ\X6£3µ\x0001×©ÌLÉ[c|ÊQdJÖ`ÑXÖ¬ªÏ4
ÞB4G¢I&~\x001bµ|
06rù1·62úÌmÈ\x0006(i,`¶CPFGÜÿ\x0011JGV3&pç7\x0015Ö:\x0008]¢ÒÖu\x001f¯ü\x001eÀ*áwlú2XÔÜ\x0005s\x000b¶qMòs)OÅ@H,\x0017\x001fîÂ¦Yÿüt­[Z\x0008¡fDc\x0002'±ÏÆ#bÝy^<½{½²þðü\c¯x\x001aõ%ê1vòíb0\x0014¸ã¨ebÛ&$;G²££ä(F'JÂQj¹vK½MH0G±Qi\x0002kUziÎ³#ù!¤\x000f3Äw9Ø­¥o.+Ò.\x0013)ýÇNÏ\x0004'ºß3}¹¹ûuC\x001c¥è²r#MC'Vo¦^\x0011«aÈW7wÏ²°XwlÒ¿F2§FÉüTÛªj"`=ò;¾G¥\x0018ÒF´Ð¡q4§fý[é\3ù{\x0019È;%[û±ûqø{æÓ\ë\x0012#[öØÄ\x001a.Ý\x0010¯\x000c¶§¶ez¿úzóòÝÏï7Dh)E^q\x001ag>)süò\x0012\x0006\x001dÑW¯o^>þÝsþ§=ÉñF 3\x0006dØ;Û\x0016åÀö9\x0005°MLvÎd\x0007\x0007Ér¯\x000fjÜ$òb¸\x0012\x0016Ë `\x000e\x0005cP(rMPÁsÐ $îUìôù+ëPn\x000eåÆ °.µ2¹ÄâUQs£qHËd³mL~ÎäÇTK
ö¾E÷óÞ\x0018wÎò0g
Ã\x001f\x0002Sh²4GM¹M\x000bÑ
Ú\x0006\x0015çPq\x0008*\x001f§0ß¢BEÎ\x000f.ew|½4J#59\x000cÐ´³Â\x0002\x000fÎ"¨ÙÑÏN\x0019ðç®3RYJ\x0001Ís#v\x0010Ï×\x000b4ªÅþ§Ovt1åw\x001fzÿîãÇw7ÕY~~\x001dÈÖ÷¶¥g÷ËS\x0015\x0001Kñáyp±+æÇÇ?üðøæevã»\x001f«¹ßúÄÎâ\x001bØÞ D\x001en½5®7H¾½ÁqünÎï\x000eâm5ÖqDË.&{½gº2	ÞÀ\x001e«Lw¿üèÓ¯_¯º)xOK11¤XöÅÙó[\x001dú(?{}Îµ3§G+Ó](oÄÒ\x0019\x001cÐ³£\x0019`\x0011wëõùÄµ:^v\x000efÁ\x0014Â¼Ñ\x0018\x0006ãdpgWJt®\x000f\x0018Ì¹`K{6æH1ðÒK\x0007lõ^îÚ¹9\x001b\x0005Sa`\x001ekÁ
jáO»ÔÚ8`~Îå\x0005\\x0007ÌðÙ!s±3ìÎ(\x001co\x001c°0\x0007\x000bÃ`P\x0015^1;Aãek\x0005cõHw®Â¶\x0001s®8ÌÅ½àQ9/×Rl*ÜúÍïµ\x0001Ks°$\x0001mÀ&0Û\x0006L¸$gw¼¦¿ãÝ\x0004æçÈ\x0016Ü9
\x001b\x000b\x0007L÷6ÔèûÔZÐ\x0007m[:Qâ^[\x000eÎôÚÚ6bqÕ£Ö5ÿwò¢§\x001e`ÜÏÁº6Ç\x0015¬ÎéQ\x001bæ£k	$ØÔº¦E\x0016:pn¥¶ö\x0002XéÍ§Ü,\x0019=»\x001fº2üÛýçÏÛî°K\x0013åÄüGÒÏ*B\x0011õÎ.,ï\x0000fÑ»{ùrý2¬FFN"¨\x001b\x0012\x0005\x0004\x0013_.úõ¬Úm ÉÎAzÝÔ@QO6ÔÈõ\x0008aY2\x0006jæéØ Å	I£JÜÓO\x0019à\x0002J\x0005#fÙt\x0010Õú\x000eÕz)j\x001eT\x0015[«¥t¥õ#\x0015y,ë\x0006QC7Oñ§\x00105[CBóé¸*\x000eæÀRVÑ-\x001b£¡vIËê$iy\x00085\x001aÑ®¡Fª¡Ò=xF:d\x0010Õt£?e¨Ùáf¢Ùÿ¢m\x001dxùÇíË¿\x0017#LÛSü)§\x00152ïBÔûHkw§3:¶Ãiûá´òáT|iãI%ÝÚ;=<+¨\x0018K¡âO!*6\x0005 Ù­ìo{úô\x001b\x0004ÙNÔÐ£\x0006é×¯ÕñUÉp["íZcÍ°<\x001a\x000cÌRá(5ü	­½'Y#Ïê¬·f2î[ÇS«Ó\x0006¥\x0016r/>Ü¿ÿxµõN¤¨5¶÷#
4¨­»ßRs¹K®ñôîÉ\x000f³ÜúÓ>&5sÒÓzm¤ØXÚýåý*içv°L"\x0013Ú9éiÍÜÆ1
¬±è\x0014õÖÆ1ÕmP!R\x0011*ÌQOË6¡®éuP\x0001ÓTê~\x001fLân°Ìã\x0011¡º9êißÆQõ,fæT¬ÍañÂªe3êå¢­¤aNzZ¶4;|Ü)<¤ÛêA'Þ¬	K¡Ås¤Õ4­aÆ9æi5Õ6Ì¤YÓ7#³§,×ÈxÁnæLsÎÓâ´m\x001f^~m§©xcÂÀ3q¦\x000bg§­¦ F6C½­á:C#5X3º¨\x000b÷ð\x0003StÖ/\x001b\x0017ÓiÚ6Ö j8\x0012\x000b;M-\x0013È¬vj8»Ì²°úuQP·ÙHA3§µT fLêÎÃ_ßwFßË¬¾õµûCmá««²n¾-û\x000bþÓÈv3ÕËf*:&dKÃcTa
mòËvÃ"ÖÎz5u
jè\x0004? «Ù`Úø/\x001cI\x0007Xï,Õi±â¶e´u\x000e\x0000:VUÑ!4Ù\x0001c·m§&«vÝ j'Û£¥5åqMÑ *:<Û¼ä6Ùþ+ªCç¢è rR ¸ÛXg7Ò=0èC£jÝò\x000eL\x0000ktg«ð§\x0004ÖZª÷ÆªãÍ¹\x0008\x0015.\x001cM\x0007PMjd¨ª\x0014VÌ\x000e©Î_4aã²\x001aG\x0002ÛïWF¶aa+ZEùUW¯lCâÎÕþ½ÕôÖÕÈÌ«Må£¬¼ÎTÝ±¢²­\x0001ø\x00155°¡s\x0002ñ§hwmö\x0015Ãè$]ÿY*E-æ\x0005°xí:?X\x0005Ñq5\x001fLÚf KC\x0014õÑòye) &b=«h`M±®yXµ¬$yÎÞ±Ø\x0012å\x0008ÖÔyØv!\x0000±Õ§[ #«Ñ¤/òO`à\x0008ß\x0005l·Ç\x0015m²Æzv]±=)¨ù\x0016	È3÷I\x0000Ð-ü)5±\x0002(A\x0011Öq3¿ìg/\x0013\x0004°N	D°\x001a)i\x0016p§ä4ð$æ}\x0016\x001bîÎY­ÈÑ\x001e¸Y\x0018T½
«ÙÝ6ÇÀB\x001f¹\x0000Ñ m¨÷¹\x0018fi
®!Äæ\x0017\x001ebcëÂl%Q^\x0000\x0017?~
_Õ
\x0001f²5G¬/\x001fN\x000e\x0007¢i÷,\x000e°C^jÕÈZn;Ýí#ìVè\x0003­øS÷T\x000f] \x0014o\x0008 YI+{òG\x001cdBêL\x0001þ\x001c\x0005l\x0010H¾¡¶Ñb\x001f\x001bUËú|\x0001l´}\x001cËJvZH\x0018¾ª¶ o«­Ï5Ü%í<"æ\x0019GÄ	\x0016\x000b#\x0016¬Ïî¿|¹êu>À0]Ê'ï\x001av	\x0010¹;´^VÞu¤Ïî^½:'eS\x0001§-\x000b\x0001\x0017;Ö&À\x0010oIm\x0007\x001b½VÀ¨\x0003ëUÅ\x000bW×\x0001§N!\x0008èN\x0000Q5ÏTBªà/ªüñÇöñÂÚuBoæþÔn!´àni\x000cm
ªçÏ=µÚ>Óá\x000cáÉÕT¨íô\x001c\x000fó©|ØSÄ§\½äÏîo]Ýã²Ra3_ìù$kÄhwKýÜRÔm^æ g'?\x001fV/o@\x0017ø|7\x0001õBÔmÓ\x000c¤þÌyøò\x0004dÅi\x001bÌ Ï\x0005¼h;¼x\x001aÜ
0\x0005Oçí[ÕÛ§`9`\x001a.¥\x001a]Ãs=Þ©3´iöUÍ±<uó£Î<ÎÙÉ\x0007­+\x0002nØú\x0017%3\x000f
©à%Åhu§¬\x000fË\x001cÝí¦Å¨Î´àOm	.ì4¦æàùÁ\x0013\x0011.e½\\x001eA«;>ü9ÌçVMû\x000e#6$w\x0018xmxu9òqq\x0004mo]*[\x0008cPXæZ\x0008\x0003õ/GçÑó\x0008ÂRüë\x0008ºnÿµH×&>oèÄGÐÖ\x0014\x001cÔ8ä{àÂ\x001dØÎ\x0000ÚEDv\x0013b\x0006q4ù8CW±69^Æ{v`°Ý4Ä-\x0004LMjÏv&zÉºEà®Éÿ®cÝ\x0000Bì F\x0007Ê]Ë-\x0012ç\x001d®êF#Nw6Ú-\x0004u·9\x001eMK5Ó¦FÜ\x0017Èk$\9W­óyÓ­\x0011¿\x0008]o²ÓÀ½÷òçµ(&\x001bjàhpÌ§l)\x001ft\x001eViy?ÎE(\x0015Ï¦ÚIªÜ\x00070Z¦ooÅë=h/r¡\x0015¦zÐ.\x001c,«c\x0007Ó¦½PË~/ô\x000ej8¨¨ºÅÓO%}KÊ¾û\x0000\x0006%´s\x0006ïm>zt)SßãYDOmÂÞÿýÓûÏW\x000e\x0001ã*÷"÷0K*´®DË¤cn\x0011öôîÇçO^.¬^\x00033s03
fJ7¢*ãÀ=\x001e±ê\x000bò`éX]\x0001ÃÆrè\x0015à¹ïl\x000b÷ýû~Ù X\x0015ëåv®Æ£c>\x001bë\x000b[Ú«ïÞå_ã+)Ä9)D	©rþst¶f^2ÌÛIg:Ý4z\x0001©M­
	³wxL9
n@]Òm&Õ3°\x00082\x0019	j\x0008,Ié©y1Ù`ûËÙï[AgZ`\x0008j´\x0004\x0014N\x001d¡@-oA\x0005.\x001eYVPA={O¶ç´"NØ©:2ÿ¨O\x0004¥¬[6ç\x0011LR¥ÿø¶cýîí0ª\x000bVs\x0003o\x0015ÕÀÆÝ\x0014ó\x0017ÎòWÔ>
6ÿ\x0005ÚôY\x000fô\x000fÿýÿõøç\x000fï¯í9àQÒµ~z\x001b¸F-ÆÄµögZM}ÐÞ<þÝÓ'g}ZB´sD+D®	Õª"íÈH9[Xhr¡WûuF7gtBÆ\x0000·héV&æS=ogr
G\x0010Ã\x001c1\x0008\x0011¯Î#Ê*Ø:%Qµº³ï¸k\x0018Ó1I\x0019)D7Æ\x001aE£*£oÂ\x001dË0ì\x0000£îWtÉ8Ù\x00152ÂVl\x001d]Õ2ì¾
ò´nÞÎêæÑ|ôíóU¸Lä'
:w\\x001e\x0004qÙ^K\x0002Ñ|ôæå\x000503\x00073£`yéR\x000f8cgM$3IU¬\x0015¨_\x0007³s0;<b¶¦YÕ\x0011s´vÝ\x0004¶t»·Á\x001c\x000cFÁ¬­úVh\x00150c+JàVª;/¥S}¤æÚ\x000c/>Ü½ÿx]\x0014L\x0019\x0016ç,j-$Î	\Ù\x0005°Ò\x0000\x0017!=½{}÷ÃÙrtÚ7©¹BÃF8Ì Q\x001bGª!ª&ÑqF¡s3Ùñaþ68r³¥\x001eÃ4ÕÌÚâÜ\x0002\x0007s8\x0018óÀ}´Qp\x0006®µ4>sÚææhNæÚñ$j.#\x000eMÜ\x0002ÌR@p;Ãùq¸¼áSÑ:æÖ2×èSä=\x000b?¯\x0018.ÌáÂ8\x001cÖ_QoÕàné£ê¶çóâ\ÛØâ-³Y;	U\x0002©ÇÔlÈªlÃU´@BR@ÂV6ÔyáöÐ»V{ßüâ3é÷Ûé:\x0003§Ç-\x001c6\x0015¶ÓÐ%\x001a9IÈp××êI\x0014\x000bÉt\x000c+¿\x0007Ù|ñÖkWe7³-x·ºÅ\x000czyJ»\x0006\x0017OÏ;1Ì:É¿xÿîO¸«¾øôíÃu?]±`«7åh"ö ¯CçWT_ÞÜ¼xòø7¸·¾xþæézÎÄ[eôIÀ-o\x0019öwï7u\x0004åY\x0000À\x0000IL\x001bÏzzni÷ò\x000cþtÿ§û/_³kÁ8Å9\x0016lÇ²¨AÒ\x001cÊ\x0010ñð\x001dX}]-c§×°ô\x001fí¾Þ4^åV-àw7¯îßüzs÷ñOï>}Àßß¿ûüsÓ¤Ì©+âÇwßþþî_þôî_ÊAuvÉh·Ñ\x0001Þò/¬<¶\x0018ü§¼ïºægþðøÍÿå7ÿåûÇ/ÇZÁo^Ý=ùáõÍÝ\x000f¿yüü)þ.ÿíù\x000fÞ½B^ÈæWp¥\x0012¾MNjù\x0015p-W°Óú>ö\x0015ðz#Ú#Þ!dRÌMÂwÀà²+bSJMï`¦Ë²ß!MtG½jï@/a<z\x0007GÙ¸}\x0017Ã1/P[÷\x0017pz§\x00026hâwx WÈ#þçWp\x001aÅ\x0016ù\x0015ja	ö
m¯ðPË9ÏÔïÒ!&	Up0ªÁï ë;$¼¥wxWÐ\x0018Ð)\x0003Þ!"Þï\x0010ð\x000f_!bï§ú
zÒ½;ö\x001d0¯<\x000exD9\x001f'jÔ\x0006\x00131Ù ©©ÛÖ±oÕå±ÿ
¢ªiõø\x0012.[-\x001e^ôãKdÿ4=ÌKàS\x001e\x0007¼Dö^ó\x001a¨/\x0001T\x001b b[Ò>M×Ä¾Áòò8â%R9õáKXO%
ÕLé%¢z\x0005a²;ð]y\x001cð\x0012Ù¸ò\x0000ÍFÂôEz	û@_Ââ°Ç|	?íÒÚó&ðÆ²¾×\x000f³&\x000c^
Ç\x0001/Í+	]j½ÊKà¡¸¾}-¢¨GÇ\x0001ï\x0010ëe|y\x0007HVÉ)²°þ¡5ÚVsM·jmÂ '½\x0003¨z	ü\x0010þ\x000fêKä3Ä²TÂ\x0004Xz\x0007ò,f5Ç\x0001/»D]ÖÆ)²MZB§ò\x0012\x0018U|ÀÐuy\x001cð\x0012^ð\x001b¾e§C+¥p³Äßc_\x0002¯ËãmQ¦VØ&¹¾s\x000fã9\x0001nÕpÌ~bs:t^"X2N\x000e\x001eèK/\x001c±°
êðÂÖx.ªkB>Æå%ô\x0003­	ø%â\x0001_\x0002_Âµ/a=¯	m#­	H\x000ft°\x0006\\x000epÄ0ø/ã½N×R^Â\x0005Ã/ñ@ç!ÖÕ\x001dabóK¸Ð^BÙö%¼'\x0013\x000b\x000f\x0014¢)åqÀ;xßfS6Nµ\x0003ÖÁ\x0007~\x0007x\x0018ïÏáÔ\x001dq0Å\x0008ìu(ÓÐl
ìÂ{ u]êzÝ\x0011î_~à¦°ä:a\x001a:¿\x0004LuÇ¾\x0004º~î\x0008ÿ\x000f_¢º\x001cÊ³tA~\x0003ÓI\x000fõ\x0006\x0006ßà@
¾A\x000b6©ê}Ôí%\x001eê\x001dp*\x001d´ÏMu)Ú£}\x000eã\x0002ô\x000e\x000fc<.3ÄÙ:¿C2¼W+£ù;\x0018îw°I?ÐK aõÇX×bRk\x00009\x001fQèXªN´¦mäÒ}	4¬þ ëZß\x0000òá§Ñ|\x001ddý\x0003­\x0007VÕ\x001fcZµæ8
\x0014g^Â*þ\x000cþ¡æ\x0012Füü\x0011a¿ü\x0012\x0006ÚKxî7¬M;\x000bY\x0007K(\x0005P\x001eG¼¯o\x0000Ï\x0010\x0006ØsµXwð\x0010o\x0010Ð$cì®r,õ%|³K(\x001bO/a\x001fæ3\x0004Ü¡Ã1Û´\x000ePDqóKÄ\x0014ª#:â\x001c}5!>×ÏW\x0018\x0007WGD\x0007Êôü)|Jìö9\x001fh«V)<È²ÎÆ\x000fßÂ\x001dó\x0016ÙÆÑ\x001e]\x000bË\x0013*FòÀ±xèABf:â\x001eWûß\x0002ÛæV·	Ðå¨;]þkS\x001cPä\x000e|¿üôí/ÿø;%ÇõÊÀùeþþî?}(Ù,WC\x001b\x0011+ð3·i]Ü!Y
5®a­^CSéX~\x001f\x001fÿáåó§«y-3Þ"ºw¢¼7J\x000cÀn)= @ç\x0003D$èìº\x001e
\x001d0! Ä=Ã\x001cU´\x0019Hä\x0012"X\x001eh\x000c`\x001cÀÞ~ýâå<ùõ¯X;Xf÷»Ï5Sçz¼+\x001bvç\x000còÀ\x0015Dmùj'­à>yö\x0002ë\x0008Ë~üòåjÅLZç°\x0010ÕnR\x0015Êz\x0014¤vV\x0016\x00084o\x000béÿ\x0006P\x000c\x001fá¤_¿V\x0001+VnÚ_¯bÒÚþ(b\x0005¼¢ÿ¿bT=^ÅÿÏ%ýü§¿þüç·³|¸É\=½ÿøå~\x001bgB!ö²öR@Jù\x000c\x0001Õ¼æÃuSõôîWw[@qûíuÃGH¥ ;@¾\x0005¾¬\x000eLªW|\x0007	i>è &
tÏ¤n
½ûFºv1(!ÍÓ$\x0011©Á,\x0019SÃ\x000f@î|¯n>Bª9Â§`¦ø³eRX³Rã¤xpû®<d¨U\x0017§ æÕèÔä,:·\x0012E\x0010bZDy\x0008I\x001d]9fÒ\x0016Ô7¥m@E]K\x001e\x0015 \x0006D
RT¼9©çl§ÚMU\x0018t¸î»nFå° 3TxîO4ªAvô·¥#jAMaÅø£\x0016¥è\x0013¹è\x0001T£TCÅ¶f4ªÉ¥2Æ\x001d¶ª¦Ô\x000bÙ¨&×&@hwü6Ò\x0005T0\x0016V®\x0002\x0005¨8íËC\x001aL\x001bÕ8¡º\x0008\x0015Ö2t\x0004¨8M|®z ­*\x0014¢º\x0001Ø|*$T·v\x0015 â)¢<£\x001ax\x0002è\x0005ðì©`9ÉA¨º:å)ó\x0000\x0002¯aÕÔ;@k\x0015B3¬G­+§0é¡>Å³5ÑlÅl@³u\x0002vï\x0014/æþÛßJ¢tþú©?ý½¸ÿòÓýO\x001f·Àj¬\x000c¦ÛÑí2_³\x000bH\x0000uÄW¬ÀÌ±Îxt÷ôù\x000f×y5ZÖò\x0010\x0003\x0007Ígëh#Ý9[£]=]¡¼äõÀvà)â"\x0006ÆxE=¸`£Ãj¼¬qTPâµÛpt\x0019\x0001F£`öLd83\x0001Ö¢Å²b\x0002^Í%\x001c\x0001Vî/éWÿÇÚ·tßýñÓûéPaÞ\x0014\x001aJù\x0017]³ë°f«\x0016)xµDX;oýøüÉt,Ì¨¿[\x000b5X7\x0019å!¥2ál+GðE" à®&ÌJpKkòâ\x0006à;HG9¥>ybM:®Ø\x0006\x0011ksg¤¬¨uíU·J\x000fÍ3!éµ:\x0011.&d\x0014\x0017o\x001djÂ×\x001a´ª`¸&"­&<ÈpÙ­\x0011ã\x001a¬ý®¸Êçó?(é*Ù°ru%Áµ¸û\x0010\x0017¾Sò§7-8\x0000ß´%P\x0007®3öËî0bÙ)í\x001b\x00117ó\x0011\x000b@\x0007GTz8rtq\x0003.\x000f)n¶b¶nÂÞ«6ºÜ1ìæxàÜµØR\x001eR\ì6G¸ÑTùn¬\x0001ã\x0016Ìw>\x0010\x0017Ýa\x0019oÌ×´~Ä\x001ax©%s Ý²wàÚj\x0019²·Ñ1.yz-(¡\x0005¼í(\x000f)m(*V6{\x000eUØ%ÓRm¬ÇcÑ¸è9\x0014\x0017+ú\x00197²aÈ/ûç\x0006\x000eÜÔr\x000cìð\x0017B\x00133B\x0015ÊÙñq\x0002\x001c](\x00107fÜÖ\x0016ò	\x0016o°æéJh\x001d+å´-Çá´ ±\x0018)\x0005Æçiqàæ0
Z\x001eRÜ|<«c\x001buÓ\x0002¨º¥å\x0018¡õVÌa\x0004¨<Ä´=Ýh|¹R7=¦­\x001dÛ\x00126¥¸Ð\x0016¢ShËèjCSWÏTa\x000fÀÅ0syHq\x001dð7µ©N¼Ç{äQbÊÂâúVO
\`¬ç3{ZãpËEÎOÐNì Zñ\x001fÓÕ¬2\x0011-\x001e"ü\x0004fC\x0017T?U½ÒM^vÕ×J7$¨\x0001ÅÊCT«ÑÍ;q\x0007ª*ó\x0014\x000b\x0007NÛ\x0016&ì8EÄÔÒÏËå.­²H£7(ö~\x001c.º5aoÔ\x0014\x0019«wÑ\x0018(-	-{à*\x000b\x000e\\x001eb\\x000eíg'ãåy2Ð~fÒZàQDNXØáa§Ç7³ÚJÄ\x0016bM\x0007z\x0001÷±°c3Ã\x0006\x001e5\x0014âµ¤â¦ñhRqíZF\x0016·±°c/KÆQÈ´s.\x0015GB2í^XÀ&ìpqSö½"ÍZ<\x00063-¥¯{kÌ¸Ñ\x0015\x0001 \x001d¸yÿª\x0017è²®\x0016,m<ÒàF\x0005qÏTp\våµåºÆ®\x000bôÈcQWÚ±ó&Çwþ^»VQ¢\x001cM\x0005ÐGNþWÚá¥æa\x0017\x000bÎú)âÝ\x0015÷ÈoBóöØ°Ðhmù4*Rj>SÚ\x0003÷ÞW\x0010iÇ=\x0004²JV!ñ}*Ñ:¥\x000f¥ÅÁÝ\x0011bJ#bÞøI Q\x0006w«iî\x0002\]®~ëSÊ÷\x000f\x0013ÚóyWÆ{gÍc©ØãÚd^[Í®UîÖS¦T@uá\x0007òúÂ»g±¥¼fón(yÍ{ÿ÷8C¦Ë·ªO\x0011.f\x0005FN\x000bÃÜUÅ7®e°Ixu)ÍÐbË¹\x0003VÉpº%°_îÍþ.Põ)ÅE/¬òÓ\x0014Îsc!>\x001eèërªåªÈ«±íCÆÍ6ú½híI¾À\x0007k;\x0003ërç§å7\x000bE
\x001dym"ÙÖ<¼\x001cà\x000fGÞMe\x0017¤L\x0007ñÖò\x0010yk««ÍA¸u°IFÈ\x0007ï\x000f\x001cßrÑ£å×=¨\x0004¡°ß(òzì$L¼­C´kºr2ÞXxã\x000e^E
\x0017ÛÐæ\x0002óB8r|Ë|°{æÒc\x0000y¡åc¡\x000bD¼îHóPî¦´ü
ço5\x000e~æ9ÄÀ°~--W\x0006\x001b
lØ\x0001\x001bn«×\x0007Ïk:)Æ
\x0007Æó4T=JØ1\x0017<Ë)å]¡U}\x001a\x0014W¬¼i­\x000eZÆ[æØ1Ã¹ë¨ÖÖû\x0014nYÇMoR\x0007Þ¡h(b \x000eD£þEó{K\x0002\x0006å¿\x001b>\x000f§Ò{ê8^SxÍ\x000e^7À×bÊË¦7iw ^2ÑêS<}Yù({	¡\x0015Á\x001b*-óÉ®	ixSá\x0015Ûp|[¨,ÔN
5Óª ×é\*÷£öIªW\x001eea\x0004:W$w`8GÛJ-¿³¬14\x001b°¹	°$\x0002[x`$Rë?-¿\x0004D%
Ë§6¼\x0011æÙ\x0010\x0017ëP\x000e<Åû?-¿\x0005,z\x0013¥ó	òúÒ¿«ð&GIçÊ\x001d£})=òâ\x000bw,éñ¥Shá53a\x0006ªÉñ÷ù\x0013þñ\x001eOãî»{y(=11VKhë\x0018¾t·îÈä]ì.xbÞÿ_sqßÖ\x0001~+\x001f`õXÖ¢ÿ\x0007Ø\x001fÕPÛ7¦ÿ\x0007øëÏÿûOù:«ó-¬¿ýôù§w¿ÞoÓ#(µ³¾ùdïñe\x0014K<.\x0007{ûüå£ÇÏî.\x0008\x0011Ì\x0018«\x00101>aÈ¨¡ÕÌ\x00009\x000bÁ\x0019»CÙÉ·BHvpó@\x001aj¥½\x000c\x0019/&
AæS\x001e\x0008 1~§n=UJåËrU¯áú³pÑ°\x000eAV1\x0007ÑHzlJ^GÒRÓ<­Hîrq\x00082\x001fA½p$³§ô\x0011ZÉYHCùep Ã-#Ü\x0006
ÇØÄ%Ñ\x001f6ÙÝÂq´\x0018x©\x0003\x0019\x001a$ø\x0006¹¦?\x000eYU;\x0006ÈÒ×6ýÓl\x001cC^e@\x0016Ï_	r²@:¶è1§ÞcAÆQCu-Ùpª	
d²[\x001ayåØ¶ãÄÃÆ²4.\x0011Rz¬\x000c©êf¥Sí_LJ\x001c$\x0016©
â¡låä\x001a\Ûr.^v
Q8²h
²ahñ8*`A\x0017ã°±\x0017à
Rj®\x0015\x000c¨P\x0011#[ó¤Ú\x0016Y;F4©t\x0013$\x000fÃ²Zôä«­UdSb4U²é %pÑ0*34g-6<ß!J¼\x0000\x0010n;Z·ñìcxòÖP=}Ã(\x0013\x0016Z­¥¥­àÍ©\x0019Jk=)Ku°pßÉKÇéÉÏ\x0008¼z\x0019º\x0018Ë\x001b¢Ì{î;¡\x001dt¬¡Î´hø§5éqJ<é\x0008÷\x001dÍRFewdÙ\x001d¸ÝdtÛ!@koù[[öÍÓÅ\¦!BÀ2ÂQt·l(\x0003^IÖAdí¢ìb\x001cåø²n\x0008RÝ\x0002-\x001b\x000bØí´\x000e¥kÒ\x001d6\x001e\x000bÊ¶ÑîøméR¨sµæ<ð¦
]6ºÀ>F:ì¨½µtÓ-aR3Þ5Êaî!JÒþ\x0012 ÅP^=¼é$6çéb]á\x0008¥-µÑBÊt\x001bÚÎØìd°mg<QcA´\x0011¨4CF*Ïª¹Ù!¬±Â-';åºí!§Ï}ñ¦s\x0008\x0012kÂ=\x0007¿	2Ýz:éxÃV(\x001dfð0bÛ\x001c¡¼7r¾NPÓæxØ¬ÄRgé¾\x0013°åc¡\x0004Õ\x0019\x0011V­)ûSz,w\x0017åä\x0008åÝ1pG\x0016ÓÖÎJú8e^VºïÄ[ \x0007½ª\x0011×±ô<\x00175P #â\x000b²yCÖ·(A¶vÖZC&,ÀÛsZá`©')\x001aôÀCy1¥\x0012J?0áPúfB³Á·
üb5å\x0010d6º ÜvÐ ÓÒÉXÍý¥r<\x0017/ÿ(
\x0002\x0008)'g(oÍXÆv\x001e;,\x000e=åA¸ï I§8\x0001¸R\x001b\x001eËÃ>8^êH÷D6ewd[\x0019UÛÂ/
ð\x000cQ\x0016Y\x0005\x0019¥õ,(¨!5;\x0014§i¹¦|7Né±Y²yC 'HÒ8;rsÄë@\x0010n;Ù¢kò~±9ûE·êbmÙ\x0010dÄ}Â4·¼5N~e´áð½\x0011{³pÛÉ\x0006ÝÍ&¥=±èV],ç\x001f¡tE4C8\x0016µ~xslàn²èGAæ·uÒm'4H§p~A×\x000c\x000e\x001bJ\x0012\x0019b[iÈûuú\x0016èà\x0018(:X,m:\x0012°+ØVò¬ô3S9í:Aâ5½Ô «vGæ\x000c	©¡­äY©\x000f»5ÁH\x001aôÉÏÉgKmV^¬¡\x0018\x000c(-"ÞuøöÉÙÛÈ¶dX\x0010v\x000c$â½ô{\x0007Ò\x0018ÊùÜÃ#©xVêÃ\x000e\x0012¥²]h+³\x000cô½½G¿¨Rrn¦5e4a©LRj*ÉÿÇ¶µ,HÍ¢\x001fgÒ1£'
}tìùBGÇà8oT7Í^¬­\x001d,Õöâ\x00085¯\x0010ZïVß á¨,¥ÊÒ\x001dò±\x0006Ðê@r\x0014ÝÚp[É:Ê"H ÊïBÉåMH}½9Ñ(¥¦Âd±EOäY&©b4D	kÇ)K½¬tZÒ\x0006^U).Ä^»(d4ÂhjÑ©|$«­4ZqÖr\x001eI¶þ¨ K-åÞ\x0001wÎ¡õ\x000få[pë
þNM3$µ³G0FñÒ1ãb9ê{Z\x000biè×²
T\x001eHÏIÔÙÏà\x0005î¹èZ0&ÄtMÏßØY·UÏðÃRÄt)\x0014óÂ\x000f\x001e<7s0(VÆ­H9ÜT
kú¾ÓA8±uG1Þµ±ä~©\x0001.kI`úa©?õv5e°ÊÊ\x0019-Sªµ^ÍÃ½îù er\x001cÂ2¾Ý:\x001aß\x0006S\x001du5Æí;#ÝzRóLlÍ»çÐ*\x00188È`â\x0007úÎ\x0008­\x0011&©5²\\x0000\x001c3ÂEí\x0011ÆÖ\x0008GÂh¹a\x0017\x0006Yx(­QÀ
e¯p?ê*·ºù\x001bV±§\x000eî¨tô\x0013qûQLk\x001caÂ­'JÒ\x001dt<Q]\x001f¤Ì[ÚË­ûkâpT&I¹:°Â%>kycÁ´NR}"\x0008G%@Xô-­ÐÁDLKVqÈ cz\x001eÌrGC8B\x0007S§n4É{³­>2æQ\x001f½¤¼\x0008=Ì¼\x001f4cdZÑ4(ßFó¨° EÏÍ
Ý7cÜ4mû\x0001Ë~\x0011\x0004Ðfn]Ibj>üX\x0003\°\x0005f\x001aÍ£|\x000eæÒ
m¦1æ-»%ñi¤ä©éÌQ+¨oN0HÙz1çÁLí·ÝÜ\x001f\x0015\x001a,!\x0008+\x000c\x0015\x0015	³@Ùa\x0008ú\x0002î¨\x001cà"óbn¦Á;\x001e:X`Cñ@É\x001d
á°8\x000c¨\x000b!ÄôÓi25M\x0004\x0008\~\x0002Å\x001cÙõJ\x0018Ä\x000cÐ>º²Íj&®yË\x0002ã#XÙ\x0000Â\x0002\x0014O@v}\x001bëÙ\x0002b`sd*\x0001Ü~@º\x0007Ô@¡Åb q\x0019è£1¥\x0015"\x0008Ï\x0016V©67C¶uÂ>*P
¹Ajð
Vzþ#ôäæ+pT\\x0018Ð\x0016Ø E\x000e\x000c\x001bô6Én:Öc°GyqEòÄ	ë\x001fåiÆÈ\x0006¾çÃlc\x00181wÌ	\x0013È\x000bç["\x0008 ZÀu­Wñ0eè\x001a\x001d\x000cúÃÑLqB5.¦8áQ·S\x001e¿µ\x0017~pÌ+áØji
_\x0004\x001cå
\x0017)\x0013/4\x0018åàDÖ©jÞ0ù*\x0000\x000eÃì»/ÆXà(èh[0Ó·`¦\x0007m?\x001eC^\x001c'TÓe_SÚÏ+1ÍÎíÇ½
ÿë?þ</íùý·ûÏ_ß¿û|óèûÏ\x001b[Ob£hÚ&!b^\x000c(YßÊ\x0019íW¾úïßÜ½|ýäñËGÿz÷òRßÉ\x0013Ze¤Ámhgí³\x001d®^K@){P\x0008Ê[z\x001dRêF«¦\x0011]ñ6\x0005 «%\x0003õ®Z×æh¢ÖQ8¤+sT@Ê\x00122RàÝ(Â¤c¥&ÒÃfié:T\x001e"T¬"¯\x000b\x001f\x0002Ë½'ò^m{·ó?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ùã²\x0010P
\x0001;\x0008\x0001Ü\x0015 åÐp¿1°æ#l\x0014BB¨~!¢+\x000fli%M³D!tÖcÌ\x001dBèR\x0008Ý/\x0004d\x0002b-s]\x0011·ñìoè\x0010ÂB\x001d®¥I¹áK$Û\x001bÈéÀ°Jn\x0014ÂBØ~!"rIoBivÜâøÊºI\x0016Ù\x000e!\)Ûá:A&ÄîS"	ñSÙNr\x0005v\x0008áK!ü\x000e_ÂòÖâÈÒèyn\x0016pÌó\x001d2R°\x000cÍ\x0004.ÃáÛ4ºÒ»0F1¥\x0013ý2ÄØMµËýîBg7CNV¬;¤¨íõ\x000e\x0006Û\x001a^¿¬.ù]ç®U¬9vHQ\x0019ì§MÓ·0ø\x0014\x0007
ÉKêÀìïvÈÊØ=q¤\x0008ìw\x0018$O\x0007"S\x0006êÉ^Ü\x000e)*k÷4ÜiºQúÈ«Ü+O¡Cq£ÌdK_\x0014Â=í,vEg1®jøæþýÛµîwt´Dª_["R®ß³÷êâ¢oÎ_>÷õÃ»_&áB	\x0017Úá\x0006æ¾µQ££ê£­&¼\x000b\x001d\x001b«áª\x0012®j\x000b\x001aL¨éÐ\x0006FëçK)«áê\x0012®þâáú\x0012®o«,§xb/ã¨ÅûJUwé¹Éêeû\x0011«Üþk­\x00181\x0013ï\x0005>¸ù¶»-«cíçC¾ôè0Z'\x001dt~y\x0003r3f¨õD»¢À\x001eYO
åÞ2ëwaùfÌJTÊBô(7²éÖ\x0008ZB\x001eßß¨wC\Ý\x000cÕ~3¤â¹Íh\x0006\x0016ÏkÇ§l\x0017ö:nÀ<\x000eÉ\x000e:Îô¼ÀÀ7CãcL/\x0010ò\x000b\èwÚÙVm3fáóÈ¦Îa×"ój³·\x0004ÙT~iw,ËÇ\x001cO!+f©÷f2¯·\x001ds¥4L»Ò\x0010
;\x0006\x0012æÜ\x0010ê\x0015³<z3·Ø¹ò0L»\x000bÃéj(I\\x0006\x0011³Ë'÷2lÇ\©
Ó¬6prÇB¾\x001b\x001fò
·Þc¹\x0019s¨0ös¼\x0014Üã¡Ìíèõd"e3d[]gÛ|U0\zDê\x0008ÍÇm YèMÝ¹º\x001a¶ãj\x0008^3ÃéÔtÏy½¿¹º\x001a¶ùjà(£ »ÃQä\x001f\x00013Çy­vó\u7\ûÝðFw-(^Céó¢;¯w³¾Bì;\x0010\x000b.rY9>À\x0006Öp7ÿÈWvÛ7ÛmÜcÇþ\x0011ò¯ÑG\x0008¬èÔ<È\x0016Ì¡òB³\x001dÈ\x001cU	 f.Àõ°\x0019vÄ\iÐ®5l`N0+\x000cóÜ9Ïä¤^ÍSZlÀ\ðù\x000cQh¿\x001c\x00162¡E\x0008Lè\x0018òÒJô
e
Y¶CÆ
-Ñ+¡kì\x0004;\x001b0½T{3è:zm\x000f_Q¼Ô\x0004I¼ÎzVurad{\x0003æ:\x0012í¡ ÒÙt\x001b¯òxáY\x001a+Ù\x0000ZWè°k·\x0015´äÜq\§ ¹­/ê½Ý^¡©´ÝÀWÛ\x0008Zin£46Oô;\x0017 ýTGÑ/ Ç~ùÍ !SÜ\x0019­è\x0019\x0002°.F{aöõAûöÆÝktÐj3âöfçöS\x001d>ÔÛ=;	GtÌj|\x0012¸ÙÓNv\x0014lÆ\x001cjÕ\x0011ÚUÐ´`ÜèLïDÆì\x0016\x0018\x001e¶`®Ut»ýhÿhq±A¶8Ú\x001exÚÙõç\x0005Ð ªG\x0008¢ù\x0011"hÅ\x0014I9\x001bAóIÝ²2Åvî\x0001´l¾\x001d\x0010\x0004÷/1¾ÇËuC;O¯»	´©A7«\x000e\x0008×A¨E6Æz\x000blûp·\x000e5èfÝ\x0001Ý©¨|àf§÷

¡v; Ýí®\¶àØrÍs|&×cwK5èæL#xà¹\x0019#Fåá-¸^ Ø\x0002º¾\x001dªývàs*ß{êÅG\x001aÌS¶\x0005:q\x000eísÀ5CÔf\x001a_d`î\x001duvj·z\x001bèú uÇA\x000bìH %\x000fäYcs»ÇäìÀfÐµS
íNiÄÇ\x001d\x00058eBk¬áÕ\x000fnxy\x000bh[¿CÛþ\x000e­dÆTì ¦ \x001c»\x0001\x0019ô<=í&ÐõõhÏÝ\x0001\x0016\x0007Ç&Ê*Yåòò\x0005\x0012
 ]}=\ûõ0sþ8Û\x00104Î¾ônÁ!¦#*Ìí.\x001e¨ö\x0012fCÛrÁBîÜ÷°\x0019³¯o´o¿ÑÚåÆC¶óÌ··Ô´·\x001dríúv§T+&\x0000ÖVqÝÛÈ£Rû9¥¡>çÐqÎb<gÞe¥Íc\x0017X@ÖcVuÛ\x0012íc@H1¿D×y`ìIÝ\x000eY×{O\x0000Æ1]ÃK*
ò?'&;7º
JM\x0011ÜÁûy\x0006Ì9³k\x00178Ï7av5æöG\x0008Ñ&£¢\x0007ªùtÐ!\x000f\x0015ïæ()U\x0019\x0015üµ\x0019´<¢\x0005_Z\x0003GÐÜQ\x001aÃ­ý@Û\x001atsB\x001aÄH«\x000cÓYl~·ÀPÕ½\x001cª½CÜ¶U@\x001bn\x0017µn¾o\x0003hSë\x000eÓ¬;d\x0010¼à&Þ\x0014¦­4fØ
rÝÔÞe ½Í®\x001cêC\x0003d/ÝïB×]ÕÙ^\x001e\x0011¥Z\x0008Ys(.VX\x001dvÃ\»IªÝMBÎ\x0013¦d5D\x0003\x001d1ëÌ)»Ë¡êÌ®jÏìÊ\x0018Ë:f ä\x0015 `çøíäÑÍk7Iµ»Ix¡
sË¸YgÎI³[\x001f¦
µý\x000eÍö[ºÜÐÔP4gY\x0002c¨µ\x001fèÚ\x0016¶×À£ëÉ)%å5±DÐÌ~oÝËSÒuÂQ·'\x001c%®ðb\x0012.EE!#ó9/m\×t{MHb\x001d¨xqCVRÑÚ°Gjö\x000b±t}9tÇå\x0010k³ÑGä\x001b½°\x0004Úï1µwgÚ½»ß\x0013t}Òæ«8iéÃ\x000foV
ß6
=¶T¥\x001aÜØ&\x00019Q:¿g[pXQxxÝ\x001cÒê<{l}Î\x001d÷9ìV
\x0007i~x÷´:ô®£\x0010ÇÇ
¬øÊ:Ün\x0005üxI®^ÖÓV s/¹P\x000b\x001c$âòºýZ5n,k5ã!àÓ64í\x0016;gLMØ-c*ÍSÜ¦ýv]¸ ØSÈ3Ý2VwÄýö)îfe"4n\x0003Lçíy*Ëå-çnj|S÷\x000foo\x001f+ííáß´6Æ:Î±>7Æ²y÷f,\x0019(óC5\x000f\x0019ÿ"ÏC~:¼þùþÓ:´ÑÆpFO\x0008eQÑÊôó`ß\x001c^wþf\x0019'8¡\x0005§Î#¸ÂC\x0011O ÍDjiCî: ª\x0004ª\x000e4pÇ\x000fvÏÓ~ Ì­sý×\x0002Õ%PÝt¢Ø\x0019H\x0000-7÷ÛiþÂM@M	Ô´\x0000\x001dëó8\x0012dó/äôÀ¼\x000e[\x000bÔ@m\x000bP¬d®\x0003È\x000bÄ$å&®\x0004éZ@ú¡%;fÈôf#\x0001?.\x0015Þ\x0001¨/ú\x0016 Áã\x0002Êt 6+¥2Ç¤çÙ\x00044@C\x0003Ð¨Ú9Ø×¸~M\x0011qYÞm3Ù\sl\x001aT½h\x0001*\x0014ö>¥\x0013µ¼JUià$æ»sÖ"­RUòJe%\x001aÔ\x0010R/C>Ó=´½¬Ìl±KøñÝH}?¾ÊI]¬Ô½lÑ÷^»\$HÄ\x0013Û\x0019é.÷´Ò÷²EáãZv&!Â+k\x001d-+|µ´¬n\x001dÒJáË\x0016ïM®j¨¡·)\x0001Íõi^ÔM@+¥/[´¾·giq\x0008*
¦"ÑßÈo½ËÇ¯©lÒ¦6÷ÓãðSjgÊu¢ùjí\x0002Îkx²¡ð\x0018ÒÂ³û·7ïo>|<ÜÝ<\x001e.n>ýrw{ó°a\x0008\x0000fÅ]m¼\x0013\x000e×¨Éa³ó×§WW'/O^½>\\x001d.NÞ\\N»þY\x0004(E~\x0011dîFÆ6=*Ð9É½*FM¦:P¥\x0010ª_èÑH !xYx\x000cÓCþ\x0012MB\x001dBèR\x0008½\x00103bØÀ%¼\x0018³S¨c`Y§C\x0008S
aºÀã§n-CR\x0017f\x0006`3íkt\x0008aK!l¿\x0010Ñ\x0010±\x000ccÒG1\x0005\x0011ã]»R\x0006×/\x0003®{JÆ4Þ!
óâ½òü!¦\x0003ç\x000e!|)ï\x0017ÂäUéàÍ\x0011PÃ"ð\x001al3ÉkÒ!C(e\x0008;ÈÇ5±yÛñmâ%\x0019FORp´\x000b£dèÄ\x000eïZdåä}Þ\x0005«y¸×h·ÿ§µ¹î·×ØÔMÁ:YðÉ+¸\x000cìoìde±e¿ÉÆoAÜö¸ÛñøKØÏ de°e¿ÅÆW¡(&\x0005 öìø*²\x0014ÎûTYlÙo²q¿­§ì$\x0018"&DýÄoÛË)÷ºCÊdË\x001dl6ÎßR\x001fôL\x0012dsj\x0008÷¢²Ùr\x0007£­\x001c\x0013v*)Ð-¯TÌ¿v\x0008Q\x0019m¹ÕÌ}\x0004^Óø¶	z´wA?UF[î`µÓ~L\x000e)$uÁøÑ\x001b\x001cpì¢2Ûr\x0007»\x001d\x0003#âuz)7\x0010{f
1Ø\x0019¿·\x0014PÙmØÁn#M;Å\x0014\x001fEü\x0014ìÊÊ°¿±ÊlÃ\x000ef[\x00035ád'5+9-\x0018\x001dòýß6Ôö\x000efÛ\x001c¤j\x0007YS\x001cFL&;¤¨\x000c7ì`¸cG)Zìü¦=¸ºMRèÉ­\x0017\x001dBTv\x001bv°ÛÎ2\x0015/½6ø+\x000b1\x0016ë¢²Û°ÝFG¥@Ø4\x000bÊ&OÉJ^\x0014Ý\x001dì6v'o\x0016cVª[ÏR1Äø\x000cß¢2ÜÐo¸\x0007"\x0002s\x0006<ñ\x0015
\x0015µ¿\x0010á~Ã]ìy\x0007ã2IàOa&k\x001dBTv\x001búí6Òè÷Hë¢ÒR9¶c`!ÊOí\x000b~êÇÃÉ»û»-
$TTp©´\x001aHx\x001bFPëùx\x0017åÉó³ÙÎ\x0017ÿÚ\x0017üÔÛàj\x0001G!3\x0017]oîwQ<k\x001cÈëÖÃU%\Õ\x0008\x0017$c|@kÀ[®\x0004½¸és-\]ÂÕ­p
7p9Ì£\x0012q«å-pñ-.­V]\x000b×pM#\Yá2é9pE,,E¬kK¸¶\x0011®òä\x0015;­Ø\x0013ó^åÃ]è[Öh]#Zwý8\x001d4íúáò}Ïv¯EëK´¾õ*\x0004N<;e3É~\x001e¼WaiÍýZ¸¡\x001b\x001aá\x001a`¯ÜE|DN\x0011\x0004³¼\x0005cvº\x000bP.´\x001eo"(C@hÓñr²&aÕxU¥ÇT«"AoX!£f°ù­í¤Èt¥\x0019t³jP\FÅ\x000bÌm|V¼;¯\x0011â\x0015­Âó89öJjæ~ç¾C\x000c+wÂ[Ý_Ózgþ°cr4ÃÙkLH¬+ÿ¡¢}G®.äß~ñóÍûÛ\x000fØpq\x001f}ËW7Vî<Á5qt½æíX00
GÐ\x0012\x0017\x0003N\x0005½/¾;yyú
\x001b\x0014.Î£[ùêäÍÜÎÜ\x0012yü­\x001d¹¢U\x0006\x001e7ÓÓ´#.ÂV4\x0014M°u\x0005[÷Àö\x0015±%Ìs/uR\x001a|/´\x0001¹ÔÕUÁ_; Ë¡N9\p\x001f¨}\x0011b<Å~æôW\x000bôpxÃÍÐ1@\x0005#'fKã\x0012_pã¸
È¡Xa\x0017\x000f½
íÈ-\x0013L9ã2Pæ[	nruo\x000br¨.:þÚÜ\x000c±HÎÝØ`uví$v\x000btUCW]Ð8\x000cÎ\x000cHÀ\x001earwã&àB>°å\x0010a¿`où9~wýîözí
Vd~HörØøì¸Å4\x0014Sªüe\x0004{LÐñã\x0017§Çs&S>
´å\x0010h7£®\x0013=M¯@i¾©äR\x000bfUbV\x001d!nNÄÌ
}À¨NöD­KÔº\x00075\x001cùd4ã¤ð\x0005;&³.R%-¨MÚt v!{VãÈÚÚðày°ùÇ\x0016Ø¶m;`ã{È-£ö9k0\x0019Ù¶ v%j×\x001aI\x000cÝ\x0018SS-v,0ì=ï/aû\x001eØb<l\x001cUÆs`>õh\x001dJØ¡\x001dvÀ±y=¦R§½\x00119 SM`
°\x000bîY\x001a§Úq[(¤H\x001apKËORLvU´à®íc\x000cc\x000b"¤ä\x0018âf\x0005\x0008ÅÖ\x0016Ü\x001d&2`!Ö"Äð&2äxýw´ì²²²ÇL\x0006ËdCÎpÇlÔ&&+A¿£ê=2jAâ)¶èt+ÆÍë>¬Þ\x0013we)e©\x000cÊs\x000f CªâtÞ&÷\x0006Ü\x000b³\x001fîÊTÊ\x001e[9Î\x0017cæD±t<o\x0016åÚÑêÈÊXÊ\x000ek\x0019"XÆ-4/\x001dÚI\x000fNö4µà®¬¥ì0ñ\x001e0¯S\x0008\x000eý×=QWÆRöXKì£ÅAAò\x0004ÉûþÂdv¸\x00016TF\x0007ºNfj·ÖfØBç­;Þm¨t7tèî 3Ï+.8å7\x0019\x000cÛ\x001c;YëhÁ]é@è	\x00170 ãtÌãÞvÂ­'©\x0004\x001bp«Ê§R=>\x0018&¬ÓyK\x001aV:I[¼\×Ô»ºÞªçzGÜDk\x0011\x000fm\x000eÎd37Ä$ÅV\x000bîÊ§R=ii[â\x001fÅÖÑåó,·à®3\x000f=>\x000f#\x0017§o1Ôá\x0002¯×ô\x0016-¸+JõøT>'\x001f¬VÔ¼a<ë\x0013³ëyW¾êñM\&\x0016Gî\x0013M¾`&ëÞ°·\x0005¶TO\XÜ9Uo§þöúáfeMGðN@gcàÀË|uNóe2¶o/O\x0016áj(ájh\x0004ò7=\x0000^M\x0000þÈF¼ã\x001bÄ[¯¹Ù7ÞdN6D#ÉZEÎ\x000eO·amÃ+ÇÌðp\x001djë-ó}\x0010!¯\x001f£uXA´
¯¬Î÷Éª·
xã£û Çv½`Öµ 'ç±6âÍ
z	/V¼6¸á\x001e9\x001d²Ik\x0015àQ­
k¾å-Çå¬Ap\x001f\x000b¼\x001f9\x0015û°Ö\x0001v5`×
Xcý(%@ØÉ}>áNÕõ\x0013
Ü¨\x0015òîö¹gÖñH\x0010+¸¾Öá­n}rÑPxò½¢\x000c\x00138uÌ0m\x0004l*!M«Ñ°{õ­\x0017Ä BÙ,ÉÁVÀõ\x00156ÍWXrñÜFýFÝ!ñÍq\x0018\x0018Vì÷^\x0005ØÖJÂ¶*	«¸cÚFì´øÝyàÕËt¿ëàÖJØ¶*á\x0018[Ó}À9õ&ø¼hÓ¯XÄ´
ï¸ýeÀ[oÙ7/q°ñ¤ivÚyn¦À¼\x000fÞú|]óùªl3b|ÊÍ\x001f>ß_¿bmó*À^T½h\x0004l|¶\x0019*f\x0000ì¸Û¯Ù8±
p¨\x0001VÀT\x0006sD;*ãÿ\x0011\ç\x0006Û\x0000WÕpUë\x0018óZ\x0006¸»Ô¹¼\x0013{\x0005'ä:¼µkvÛâ!ZkdÞjër\x0016n\x001fýP6ÿ(ÚàÊ¼r<"Ô¼îx9\x001d´\x0011oí´C³Ó®î¤\x0014'\x0007^Àår£·rû\x0000P\x0003fÀúZ\x0008­\x0002^7a½çc[WUêáÉVÇ
xE\x001e06¾7òx2\x0017uØ)+\x0016:&¼­QgåÍÏçksÑÒ¬Xç¸\x000e0Ô[]Jìá&Õa¾\x0010ÌÛàÍ»«\x0000ëúuó	Ë\x0002§
9\x0015¸Ó	×Q\x00064G\x0019c}Òâ(\x001bé\x0008\x001dr.m²o`#`S¿9ó¥¿9£k¼­açï·6r¦ÕÈ)Ë©?+
o#Âåq|!&»[7\x0002¶õ°­\x0017B\x0019æ§±2olt:\x0017óÔN/ÎUQ'¸æ¨\x0013rjÊË¼Á \4Ý+\x000b~¤xg?íº
3²º\x0013Qºw¸)'yÂ
ìß|kÌx\x001b1ãÃsôð\x000c\x0016Äèáñ\x0012\x0000<ñTñ\x0013Ìºù\x0005O
xK8!9¨ýNO\x000foÆÛ§7ãmcd²Ë&\x0014ñ½Â°®b¤	eÌ UÝ\x001dÿâYe/ï\x001fopf{%fëòÌ \x000eÒ§\x0016\x00183ÕÊôàù\x0008ùòüê\x0004§µWà\x00127ôàö·\x0000\x000fd\x000c©Î(\x0003d¦\x0015ñÝ\x0006àª\x0004®º\x000eÜòÔ£B7ÎÑóüâÁ\x0006Øº­{`\x0007A\x0004OÞb<lö]tÛÚ¨M×aKæV¸ÙÒaçÍ>aE-l\x0003p[\x0002·]×Ûe¶ÄÄNÌ°MuGà®\x0004îºN\x001c8ñ\x001cò4/\x0011O	×,\x0006Þ\x0000ÜÀ}×k&¦Aàî¸÷yÀ²îÞ;¸C\x000fn\x001b¸í\x000c\x000bëõÈ»\x001aVÓ×\x0003/HñÑò®\x0013\x0017\x0019÷\x000cÆ\x0013çE°z\x001b+ðÚdvÙL;.\x001cq¢ç#'Ü+\©
°+)»L¦Ë­9Z2?K<ov\x0002­l\x001bÞ\<\x001bQû(\x0017÷\x001f×6ÄÌåP¢IZÏä!>¬X&}q~õz\x0005`(\x0001C+`íx="4¦ñ!'\x001aÃu°+\x0001«\x0012°j>á±=À
tiì~,UÊå\x000b½\x0012°.\x0001ëæ\x0013Î\x001eõ@× \x0007+òJ+\x0001\x0012°i>aÓ\x0008ñùíxÀ»áµ%^Û|À\x001a\ð|\x001d¯ÏÕ\x0015¥ëp]	×5\x001f¯b'o8^\x001aYwÚäó]6$+\x0001û\x0012°o>_ÅÛ6ðYEÅà0ÉÒ¹\x00150Ô:­Y©)3£1Ú\x0012Øeî\x000819¹±\x0019qõä ùÍAÞ\x0013byO\x00088ån½®\x0004Tw\x0018/1¢#XÍÔ\x001c2ì\x000eWÕ6£ÙhD\x0007ËÎ¼\x001c¼Û\x0015©ò%Ä ø\x00111¸~Äéû_®\x001f\x001f\x0019ôÕÍíÝÝÍÇµÀ\x0007bZ\x001a¦4w:Ác\x001aÆ»)à§//¯®\x0018üÕÉéÙÙÉë5\x0002@)\x0000t
\x0000s¤\x0000ËtðÛgíÐ¹¯\x0000ª\x0014@õ~\x0001!½Ni)#²d&¹.ñë\x0012¿îý\x0000aØ¢>\x0000d\x000eø<<\x000bÙ_Ú'\x0013¦ñ/Êõ^/¯úpw{½òÍºÌ¿àbèZó!ä5XA{³o\x000e/¿}u~vz¼X\x0012±
­ª>éE/\x000c§Ú\x0004¦\x0010ór
bPO£\x0015%þ¹ÿôðnKîÉ\x001c\x0002QF Îd«Á\x001brþæòÅÜõVOã\x0016%þ~Ù\x0002}¤\x0018öBæä¤O\x0013±+õÊJÔªDý[¥²\x0005u\x0010\Ê÷:ÏÊ\x0000-RÂ\x0003¼&mÐu	ý·úd\x0013tÇ+A}Ãh¬
p/AllmnJè¦ï\x0007.ïãR6ú§®k2NhnKè¶\x0007º¹×*ºäo)Ð¡É$e\x001btWBw}\x0017FqðKû\x0018º´ÌÏe&]Å6è¾î»N\x001d\x0013\x0010µ\x0013HZ:@7ÉþHd_[éz­\x001eJè¡÷Ôù®[ÞÓ\x0011OÝ\x0005>õÉ:u\x0013ôrõhâÂè8v$ûKÐ$@À9VÉ6äµ\x001dí2¤H\x0012 øÂ(æ1\x0002£ì\x0017iÃ^\x0019RÙeI0"f¤k`íè\x0019\x0000ýdv»
{eNe=Efìi\x0000c\x0003vëIÇLÒpnC.\x000cÔ\x0017na(\x0018¼_ü|ýáãÍÃÍÝjËqµ:n?É÷Åñf#Xh²¿:¼øîøÕëË³yZNB\x000e%rèAnpy\x001fq§Gc*Ó+\x0015DüïÜ§Û «\x0012ºên1¦J¼¹Æ*ó~2¹PVØ
]ÐõW\x0005ÝÐM×U×Ìµ\x001f£	¦\x00017VNR\x0000¶\x0001·%pÛuæÀ«\x0011\x0005e_âóq/oCíJÔ®ï¸5çÁej&°¡ÃÂ<ÌVè¾î»\x000e\x001c\x0007\x000bK®Ì=ñï\x000b=ÐC×©{£s©ÉÒTÄÎ«=\x0014ìª\x0015\x000b
24E¢ëØãý6´$:ê@ÇnÔ¨[v½ì²6£}vÔç\x0002¸¤Ø\x0006:w®X\x0019»Ðj¾\x0015{eHe%ÅØNñu·Dëª g\x0017\x0017[WÆHvY#\x0007<\x0007\x000f6dùh\\x0018ÓÞ
½2F²Ï\x001a\x0005Í­\x0005j`\x0019\x001fî\x000bd;jw¾ë9]ö\x00085»\x001d]\x0005ÒìÕã$	\\x001böÊ(É.«äqóeîLCÆJY\x001e\x001a3J/\x0011üo^\x0019%Ùe<¯	©	<©|ÛarV\x001böÊ*É.³ä5p\x0017|`\x001b5®öSûZT¨Ì\x0012t%\x0017ÄÉÇN\x001e¯ÊÚqçSÊ(AQò^ wE:uË7F+^ÒdÔ¾!\x0012ÔÑ]QòR2ë\x0017 {\x0008\x001d{,^~Ü\x0006½î +¼\x001bø©?\Pµ+:ïvÕ\x000bé­È+{
]öÔëLÛ>;ÕaT¦\x00114°Ð\x0019¹\x0015{e Ë*y\x0017\x000fá.5¢SÁeg`aÈd+öJµCj÷\x0018e°EuìùjÉØ¸¼cGèªÒªK;z§Ì\x001bY\x00053cæÞ	\x0001Ué\x0018Õ§c°YeGYßÇ§*\x0017&·b¯ªê{ªQ¡SM}X\x0014¯Ål\»ëSUÕSU}OÕÛ¼\x0015gØ\x000cc\x000f'ë¨ª§ªújÄNS\x0008Wë¼\x000b~zOM\x0013v]½UÝ÷Vã}§\x0018U\x0000±Z)ì]dË´¸=l\x001bôê©êÎ§ªò¬\x0014KCÈ
ìªÛu0í{¨Q+JFnó¶\x0003ÈÐ\x0017Zo·B¯Þ©î{§Fñ¸b:M\x0015Y \x0014Û
¼z¤ºïêLµ¹^ö\x00052ù1vWïÑTÔô=Rb"TBqé1\x0002çøTO.dj´¦?¼½}|bQñoú\x0014$äp	XÉlSÝNîïÓ.$¡ÆOç·7+W\x0003aC	Ï ZîÔÅþ\x0000æÏf¼9<?=Û	ô´åH¨qTb\x000bN\ÌÀý¹H\x0005ÓtÜòêÔl¶k-PU\x0002U-@¥\x001aÜ\x0002±X(Pc÷þü éZ º\x0004ªN4p_%\x000e(9\x0006?ý.\x001fÞ0M\x000bLì\x0002ÉlÔa\x0006k@AÎW®Öâ´%NÛ3'y"ÑSËöyg>¹¶\x0016¨+º\x0016 Èù@[\x0015ÈßÝæ­!\x000bÙ¨µ@}	Ô7\x0001µySÌLó1DdZ¤>ß\x00044@C\x000bP­yQ¦Îy\x0003pãZÏ=4SQk¢\x0016\x00069Âqaª§Ôµ7y£çBwì: µMj1JÎÄÆã¸j\x0002\x001aò¦ß=Þ¼¬l²JVçÄVp\x001b\x0012:ï\x0004l®ß´Rö²IÛ»ü9\x0003R§¹qT\x0001ï?\x0008nÂu-ÒJßË&\x001f\x0003zÞ¡\x001dãcÊK(éÆå»i¥ñeÊ\x001f;û]ÐÈÛÃ(\x001bäç9GÖ"­T¾lÒùhèLSóóTñ(/®¿Ø\x0003i¥Je.õÂ3¯¾9¬¬æ\x001e¾é]\«Ê§£°Faï?}LNÿÉÇë\x000f?­]L²Ì\x0000¦xB"SûÌÌÒ¿y\x001cþ×Ç¯¾ãÒ:Z*i´´\x00151Á\x0005\x001cîHx\x0005OaéiÒÞ­xeWv\x0000\x0016XV*Þ¢\x001e$q¼N±nÅ<ÎæIÍkÃl\x001dË'b\x001fÁë£«Êç<MÎ¹\x0015²ª/rûMitÆ`qÞ0d~RClÅldue;fÃ\x0015¾¨×<Oûðë\x0013ûÝæÐ\x000e!ëvÈ#U½Ì¼ÎA¸L¸6mÜ¶b.³q¸Û6c6\ÑC\x0012>bv\x000eÙõ±_y7ÈÕ\x0003´\x001d\x000fÐò±¨+âÕP\x000cÙO\x001a­CuCÇev|3ò¼6$B&W\x0012'}wÂ,kë7ìQn\x0005M\x000c\x000ePÓÝÈ
wÎLÓ\x000em\x0005-«\x001eúÛA+\x0002-=/ä\x0008¼¶\x0018%í¥éä\x0013#Øa\x0005#fÍ5S\x0016§Y¶b.6\x001a\x0008ÞhÐY³IÑD
\x0011\x0015\x001d3\x0008Êéxc#â¢Z0Euó)ÓØL\x0019\x0010j\x001aÕµÓIÆ ¬,í&\x0005G\x0017r}P;»ínOPÕþêp¼çfWÌô[\x001aÔUc]h:Âß
ZUo\x0010m\x0006õ\x0006\x0004½g{ºõôtñVÐ\x0005¿+\x001eø]\x001bA«²]Qs[¢Áìå$é1üCÐzÿÚ@\x0007Ëç eÖvÛ°õu/Ð¾º\x001eøk#h#äM×Cê\x0018nÓIç~
-Õ^\x001aO\x001atè\x0002M½7\x0011^ö:4{\x001dZLn!Ý
ÚÔ\x000fÑ´?D#\x000c_\x000f«%HMkæÃQvz¸b+èú¤MÇIÇLK¯\x0005&¶)&4¬òÔL«ÐFÐÖU&\x001cm\x0006
á²Áøl\x0010
óøÀäB÷Í½¯0cõ©\x0015sÔx	²\x0006"ÛÃs¦|\x0001¨iîÑíZº /&=}Ý¬¨§!\x0006\D4\x0013áæ¦~¯\x0014¤ý¡Z¡uÞ´B0\x001f\x0006|ã\x000f?>`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-o6SzLo0nSCdCBEYjdZOGVJWN21I`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-rpPbH+r5j1NzG2GyMan0I5SObJ4`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-pcxv7aLUCsuwhJ4o8KofXmZIwV4`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-gfGw1kpQ+EJogII9kXj43Vg/Now`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-I4yE3PIZld6+Dw7ui6/n+/XdeBw`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-V0N3GOwLfxfZye6BpnNSJtqxbVU`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-I4yE3PIZld6+Dw7ui6/n+/XdeBw`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `8f3c-64ROtMCiCMBF6duBFW5QwXZk2B8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-lTD2U7ytGDdWgxuYMMgNb3kQuKA`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8105-YwDlAzhdlF5SM86S7Iiwf8f+U3U`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>������̺4� �\x0008\x0011\x0018��N\x0019RV7mH</p>
  
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
