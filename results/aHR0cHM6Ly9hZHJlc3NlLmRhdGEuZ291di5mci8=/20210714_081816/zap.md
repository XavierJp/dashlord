
# ZAP Scanning Report

Generated on Wed, 14 Jul 2021 08:10:12


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
| Source Code Disclosure - Perl | Medium | 3 | 
| Source Code Disclosure - PHP | Medium | 9 | 
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#7cF8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#neSu`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#7cF8</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=?9|uz~öDÐ ãF@«¶ÜòbyìfÉè>\x001bUÏ~ÇgÙ¤¥¹0Dæ)`Àã\x000bO~¿\¼_Ü?¬Í?lr«6·È­¨\x000c<1Á*©à\x000fð\x0014ËjÁ#Èu\O#ÏÏ¸\ï\x000b\x001a¥À¬¼¬t0Ü´ÉÍ4rêó÷\x001bØQq»û;Ü¶ÉídrO5Òð% çJYnw\x001aAîÚänân	Øíëh,lSÈj¹\x0007GÕÖFû6¹xBÅ>Ïós<\x0006\x001eÎgsuºç\òÐ\x0006\x000fM¢¥éRíkÉ6ÉeY2h\x0004ylÇiä\x0010\x0019ñxÛ¦\x0015þS¼WdÏíS
Þ\x001e°)Z#fF7F\x0011ëåéé\x0008Ó.þÛ\v/Ði7¨\x0012Z?Óª\x001b.²YõgÜè²sÊi¨ÇÂ?\x0005ºCm\oôçÜ/HN»\x0014l\x0012M\x000eëÏ¹\x000cËÏ¢\\x001a:üBØ®¾Î\x0001ü\x0005ú[\x0000À"Ð?bÈCF3"\ý\\x0005`c¹ê\x000fúS¦\x0011ÐQûù$ð`Ýï\x001fV\x001fo\x0014¸³Êc³Zþ\x0013ßx¼ø\x0004ÈËî\x0017ä[àü§¼Xü\x0001ÿk\x000el\x001dD;\x000e\x000f¡×`¦±°\x001c6E0>â\x0018TU\x0011l\x0013þñböo³ù\x000bÊxï\x001dÏÞ\x0015UÇÜïãU\%:èàÏãå}Ö¼ßÊ\x0006Á:J£gí-8týpÃFh×¹/òot°rY+²TÕa3Íì\x000eÛ×?ýý§?\x0013Ll¸û®{/¯\x001föf·W7ÕvB8!p¥iÜwØÇ\x001b1\x0004\x0004B\x000fÜùËâÇÓGç{/ÞîÍ^¿:ÍË«ÕâákíÑµCðnñãþþz¹Z\x000e\x0000\x00149ºFe_ã#ÆÜ\x0000èÎia\x0013À{\x001ap¶÷nöÏ³3ì\x0003(Â-þ¸_½ÿÞ=\x001aÏ\x0004àrt&pÑò0ÏL"BOáqxÚ²¸ß¯ÿXÚÅ=E\x0016¿¤³°w@#e·í¶4	W¦ÝfE\x001a§»Í|ß\x0018\x000f§8<½Ûöò\x0008Ùl6
DÊã|üg\x0005:y\x001eÞzô)PÏ\x00126§¤>2Si¡\x0016<Ï.\x0007`î÷Yò;pÅî\x001e®ïï\x0010ª¿X|þîÍÝã÷\x0001°ÿ?uï²\x001cG¤é¾
v³JÝ/Â\x0015\x0008"H\x0001	6HPºzS\x0012$$ @\x0002D&«ÙÍÙ7y~ó$£jªêáððp³ð.éÎNfW}en\x0017½þQ\x0010ãÊf³p\x000bPh¦dK`MÚAÚ³×'¯^\x001d??\x0006GýèðùK¼ö^]üûÖ÷\x0016¸{îc@AÐRaS	¬-ÏzÓí¹Þ\x0003Cy¨7ë ]\x001fÒ5@FªþxÍ<B\x001c!\x0013
ú\x0004H;xPÖ\x0018\x0007$«z¾\x000fèë\x0001QâÑÐ*\x001a!±\x0002\x0018¬bÚ0ô	C=!ìFµÚZ¾3uEáÆ\x001c<E\x0015±\x000f\x0018«\x0001±þ^:xÒ<VG\x0017@\x000f\x0004$Ü¿\x000faê\x0013¦ú%Ô¬N\x000eK3+0ÈM·¼t\x0015¹Oë	¥\x001aÖXÔÞ,oC®¾5ôeÀã\x001eì1!zfÕh¨$;âD±n\x0011}Òh

D½¨ëwb24Ô\x0016\x0010Sñ×\x000b¢Qr»8xW 5DÓ0ÓG«èqV6!ÊY1jÏ³¢×\x0015]ÿ®`\x001a¸´âq¶8F¤\x0010*+7b4û"®ÝÙºþÒVÎ.o,º},\x000b\x001be'Æ=¯l½veëú;ó¹ôc\x0007(EyÐkÚEèÿùÉþ|çßöLêÃ?ð§\x0007Ï7·\x001fXÕtw	V7Ài\x0016òøå\x0012\x000b\x0000-ø\x0012T1.\x001bJ¾ùh=Õlk4\x001b|A{~ÅJÝ_\x001c¾9~qq|ðìøìüÙ1:w¯NÎ\x000f_?~wóåËýõRþç\x0006&Qá¿ª9SÊäÀ³\x000cÎ<\x0016\x0015"§%ï\x00048#7³qâ\x0013ÿªç\x000c½wz_Eá\x00068\x0015ÅK4ÞI³rÂÛÿªçô	Í/ZÏôH\x0017L`FÔ
\x0013Ã¸ø¯zL !Á ²%´
ðDwËiçãÄ\x001cÜãòS\x000fª#ëõ\x001aï<)k\x0003¨\x000b@µBe£Ù@Ñ}+?õ pà
x\x001aV@­\x000e\x000cªq´Æl h.jÐH-0\x0004JÂbÀÉíèÈ`gãD­¯òÓÀé	\x0012\x0007&\x0019¦t¼?µ	s®&ÖzÊ »{)*\x0006æQÊÊ3hq>\x0017¨Á÷òS\x000f
~l"Ð\x0000~l¦^;y4Zóâ«Q~êAM\x0017)h£Ö
¨¥\x0011M\x0000\x001a°\x0019~6P/§my:\x00114Ò\x001e
VSÊ§ÊÇpó¢rAù©\x0006
A¦PÊt5)/o¼Î3>\x0016\x001dòSÏéàË\x0013¦4\x00180©+\x001fSÏøÝ±óè±m2ÀÖD;¾;p\x0012¦²jÆÓâ3\~\x001a0-7*Ár²\x0016\x0006rz¹èã¬\x001d½ÒòS\x000f
îOï\x001e(çëQá@@Ó¬+ýµå§\x001e\x0014îMÏ\x001fÞ±n+FÛ}ú99Ñ®³MÆ\x0007\x0000\x001bÜ\x00041\x0012gX-hñb²8n´üÔÆÄÕqå$Ñ+\x001f²ó«³4çG5îòS\x000f\x001a*K\x0001õrâ\x0000	~\x000cvÏ\x0006êP¡üÔé\x00054ÑÝ\x0014²öV8ÓÆ\x001d{\~ê9Á¬§ù\x0010ÀÑpFPØN@ó\x000bJngßéu\x0012G)Ä2Ó¢FÍ¯\x0012ªRÌ	ê\x0011´éÐkÿßxQ®Ã\x0005
I8Ñý\x0013GÜjN\x0014ª\x0013ó\x000eì\x0012Ë \x001dj01:#(.hÓ-êº<¨°ó(h\x0006µÝó\x0016-rÎå§iE\x001dùÈzn^F¾£dûÃzòSSl\x0004ë\x0000\x0001'o#§s=ñX\x0006PÖR\x0001MDð\x0011Tîz;ãÍJ}µì¼é\x000e\x0012ºô®`Æ$\x0007\x001e\x001d¦\x00199
r¶øñÎûÎ\x001aÉVÎQäúO\x0004¤ft<±kðqù©\x0006µÉa\x00116F\x00057\x0013=àÈ÷³®(æ¹ËO\x0013¨O¼¢î!å¬Ë\x0019ñLjJ\x0003êñMD	ÄÂécàÏn1ÓQÊp.^\x001d\x001e\x0002ÏÞ¬\x0018ÀMQ\x001có9hEcfFü(YA±Ya±\x001c´ü4ÀrÖÃÁ_GZVÖ±WfÏ
°¢¯üÔÃbE\x0011±:MÍwÈÊo¨¨×;+*VuM<+Âd£IÐÝc\x0004×Õ\x0015\x000brNØG ü4m\x0002\x000eç¡ddN²	5£\x0000Ö¬¬N\x0001«k	\x0018,ÞJÌ\x001aV§Ë${]qºUùi`-A\`µ°Hý§·a}\x00193\x0003ëû÷§«\x0005\x0017®<^íßëüòy(\=b´,ógÐ¶
Sb *\x0017Ç\x000cªß\x000f_\x001cüã
jæ¡XõnP\x000c¿i×Dª5Ë²\x001a¬4d\x000c6\x0008é¨Í_MjK\x0008²Ô®Ö\x0014v\x0002y'Ñrµ\x0017z5fýU>HàÕ\x0006+æ\x001f¸
\x0018kVHàÓ|¤\x001dHmk
SRáÁJ\\x0017¼\É5Z?æB×n¤Æ¦£\x0006eJÅ Ò\x0002óÜt¤c!ÓjRi'oHt£\x000bïÿè­î\x000e¿óH\x0019,F)?õ¨¥¢)p)ÌSÐâ *¼\x0007fDÅ ´q-[5Àß{$YqEJ$@jÄ\x000cTqÖ3eÑ®¶=ãº\x0014ÌÔ(éf/éæhä\x001dÇÑ\x0013QoùÃ%UhRµ	ÍOnHÅpëÑÏ\x0006,\x0012ö9û¨Ñ±b±\x0011%®±üÉ\x0019*\x0013vkÃéÏv\x0000fø/þ¸üÔ\x0001âô\x0001ºT\x0017»J\x0016q\x001c)\x001eÏY\x0000ÑÕ+?u&¯6êf\x0001Ô³\x0000jì\x000czL¿U	\x0007N\x0011`.SÐ\x000b a÷>\x0016Ït\x001fÀÏÑ}\¼Ç\x000eþ\x001bïîàhq{»¸ºÛÎ\x0017qº<Åî=Îô(³#}v)S{Ba
2é\x000eÏÏ\x000fO_
0®þl'#ÆÇ¬¯eÄp¸0\x0006ê\x0006\x0003F.ÇAF4\x0012öcüöçõ;ó\x0007F\x001e0X~Vßùèvq}·x7òqR\x0014MÐÞÒE4]¤¹¡:Â×Ç/s~øâÕáÑÐg?ÚEOlù©¡3Ö`Àè,\x0017
ÀßVQèði¦ËÎÿ±üVºç0Ù¥â3R:Ò¶ã%\x0013%ì°T\x001fo ä­ÎÞ[ºdº\x001e³7OÎ·ò\x000fmáüøé/coÐ´À où\x0011Nló»ûzy½¸»#Q-¬Xj\Ü\x001f@D_Ù{'fEpF8~õòäÅá«W(°\x0001yÐÿÓ]X\x0013U~Z0YÝ\x0004¥YI\x001e¤²SÓüf$-cDËO=)<]ÊÎ§ð>9¶Ô}Â¹%ûþq³4ö}±°ôÆ­mÑ_\x0017W\x001fï±\x001dlì\x0012Â8*ñOâ\x0008\x0005\x0013\x001ep\x001eó¥\x001cjð=þõðôÙ\x0005M~\x0019Ø½?\x001d¦¼þü>\_\x0015o\x0012+íR\x001fòtñçòöúÓÈ[S\x0004\yl\x001cFéË7O\x0011þ\x001f\x001d¤äJ\x001eØ8ç/~Ûr~øÏvàY¬`/?U|6iÎq8\x001fyì=x¿)1`vè>
Ä/¿\x001d^¼ÞÒa0¢üTQâ(jøvAeÒ\x0002CÃQ3\x000ePbEÃ|\x001e+»ËO\x001d¥r\x001cqÞÏwN,³æoýñúêæór­:Uøî\x000fDº\x0012\x000bÒG6¶BÓ½®ÁóæT#ÃÆÊX\x0017 ºXw¾	zq°öçÃ°¾]Â\x0001l@\x00137lØ¹Ï\x0017ß?-Gí4§¸\x0018Hu1c¯"MÙ\x00023²T\x0015ð×¿\x001do7Ôº?ÞfZX³Õ¦bbíIcq¼L!ÍÖ2©¥#4\x001b©/!\x0005Åf"
À 3^ä«=¸b\x0010y1±Ì¹üTcÌªFq¸Âi;\x000f"ä9>}úúåþQªW0­ÂCÒåíÇÅÛ±\x0007ÈÇ¬9¦¡5&KÞ¢\x00116¤â+??>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?={1ñ.\x0018\x0003¯þâ9X\x0007áäág\x000f~¸º¾Þ|~\x00019d~¸Ä\x0014\x000eIÊä\x0005Ù2þ?so\x001dG¤
^Å/\x001aOçáaå\x0004=¨\x0006	\x0016ü;sÃç$<H\x0004A\x0011äª¶ÿ\x0011ê\x0006Uwè]Þ¤NÒ*ª"æª ÌMÕ,î¯*­\x0008Fdé\x0007QQà]©\öáÿýíðèhþª_\x0019vÀd\x000eL¶\x0000Ó\x000c?KaxJ·\x00010Ä\x0012BÚ)ÀT\x000eL5QÌáv`\x0019g,X\x0004fbÂN\x0002¦s`ºb2Î E5&H^KÕ©±)¸LË4áê\x000c=Ó\x0012=txnq9\x0005ÍÙz`"\x0008ý=Ôo\x0006ý\x0003.ßÙÀ~
*£rMä
X\x0012µ4²Z\x0017\x0011Á
Ëç¸|\x0013ß\x001b\['¥à)T\x0006|KÆ¶±j\x00020:4\x0001zzd>
\x0017\x000cfÉQª{LL\x0001Æ\x000b`¼Á¸ÅÍ\x0012ö#\x0011YN\x0002ß)3\x0005Y!õyØ\x000fÈ\x0018.×"ø@¬)ÑÉ
>EñBìó\x0006¹\x000fkÚ: øðdË8Õ)ÉI
\x0017r7\x0008þh
¢\x0019[[ ¶»M;EÀòBðó\x0006É\x001fèäb{\x0002H2§ÒÂúàJw\x0016ÖS\x0004,/$?o\x0010ýÁa\x000b\x0001«H$\x0002ë<+­'=ÍBôó&Ù\x000f£\x001ddÖ¤²\x0005ìHúãJ®±È
ñÏ\x001bä¿å\x001d2Û]¦¶\x001d2?IÎ\x0016
7hð\x0000\x001ci&nö,
3±\x0016f\x0013`Bü\x0006ñ/`ñBzñTN\x0011è%\x001dq¿¤ÈE!þEø×\x001c×4G\x001eCñ¯aÂ\x0010ñØ\x0014î\x0017¥Ñß"þ9s3
»=\x0010ë<\x0011e'Ñ¬\x0010ÿ¢Iü+\x0015ÓÖ\x0011Këq\x00022¦È}Ôl,\x0013\x0015MBVz\x0008%Y& ¾(Ë¯å\x0014ñ/
)+¤¬ð\x0014Å@G\x000f×\x0019â³I\x0016£(¬h\x0012²P¡';`V\x00100"aHV\x0008YÑ$d\x0019[ërÊ[\x00032ÍHÈ:?Í
!+ÌlçbÓC4fyG³îez;å2e!fe
8ÿaF\x0019ñ?ÌÀ@+{Ì
r6:\x0014¿\x0015&íl\x000e¦üSYY°lóå\x0017YÁf²I\x001bI>\x00134l)²Ìl'ÍÔ\x0014dª\x000c¯4ÙÏkÿ¨B\x0003¨&
\x0000¥\x0006\x0014·ii\x000f3ò¹ÕS\\x0013Uh\x0000Õ¦\x0001DÜì\x001aM3¾\x000e°uÄfv4S\x0006PM\x001a@¥êýÈf&-·\x0000\x0013u9\x0004;dÅÓT;ô4Uñ4UÓÓT\x0006á\x0012Í\\x0018eäÚM\x0011´ºP\x0001ºÉÒ	Õ¨\x0002¸HClÏÈÎplÊeêÂÕMá\x000c\x0019³\x001eÉÐ/É4ëìIþ¯.¬YÝdÍÂø\x0017ÓIYÌ=\x0004)Ûyæj\x0001¤\x000b)«¤¬t\x0014\x0000\x0002)²f»äë2Ý$eW3éBÊê&)\x000bíç¿±\x001e¦êH¦Ô\x0014ÓÌ\x0014ïÒ´\x0005@}'eí:Î¸¶fÕ$ßÜ\x0014\x000fÀ´EóâÊ©¤2=YT¬OÉNy¦`3ÓÄf>\x000e=!\x0017ØaØÀrõçÐ¬ÐL¦-\x0000Ä;a\x0016n\x0013Ë\x0011´îTæ\x0014XZ2Mj	:EÉs¤Êïâ?ÆMa[Øÿ¶)Îò¼F-ômÒK8\x000b\x00053¾\x0014ÌXg§0¿-¥myÏ\x001aÿÃ\x0007
\x0013µ	3ÕÑöuB6g\x001d5dÿ3Õö]ÂpÙMte\x001f°V\x0014

Å;Ýä&¥\x0000|û\x0006páÆ\x0010Kµ¢Ë³:2\x001bí$=ÂÖ\x0002í¹sÂØk»TC\x0005"\x0006t¹ÔGT\x0002!\x001ek#\¿\x0013
\x001cLØÄb\x0003"ö\x0018dM¶aÓ\x0007e±W\x001d°Q\x000eQH1-îøn-/5\x001eµ^\x0017¯áaè5\x00186)½¯Kpºí¡ú.Æ
Æ.*RßUk×2µ\x0007\x00000|\x000f#·\x0017«\x0000êæafRõC\x000b\x0019Ý©H|ÔX\Iz\x000bÒ\x0017ùÉËEÀu|>K#©\x0006Ñi£úÖ\x0016tÇ^\x000f\x0010#\x001c\x001b®\x001dË}\x0012Ç¹"\x0004ßÎ\x0014´3m´³!á\x001czz°¹\x001d5ªbÂ&8VÔ\x0012´À;\x0001ÙâîÃÍÃíýj¶º\x001d?Ü}X^lx«JD9á8).!T÷V}ÎsÓãó³Ålq6;>?=¿\ô\x0007\x0002g\x0018t\x0000EfðåõÇË+\x0000xµ½½ÝP¸\x0000\x000bËªT
Ä»\x0015ä)(VHá¿Ìß@w\x0018\x0000<ÏÞô#ïýãýJc(7\x0006pÿ²ºý²\x001d-?Þ\x0006\x0000J£É"\x0003¨+@¤½sÚ¦ÎBZE3âµS,¶[ph·H.òÑ)tÔ½^\x0004$¯N\x0002®¾7#¡muUH¬ÝG\x0001\x0008¦\x0015¾Vâ6uïèQÖ\x0003q«ûï¿eÚ'\x000fÐ}}\x0007¥Ò÷7\x000fww±ñ	,\x001e¶l@ç@\x0000c\x0019j$k\x0018ÍñFc9e\x0000sr\x000e×§P.}\x0016Øè´·Q¾ûðû
ûxßÑÐí\x0008ÂíÀè\x0003#\x0019yxÊºÃÑ£CÖ§Ó½\x000cî1\x0019\x0018¨à ø"\x001eîµMS¼Åâ³¿«¿êbòElïû½Khãï\x001d\x001b[R\x0017\x001e¬®SH¡»³Sï{ïÉ_/>|ùå*atró\x0010¥]ï¯ÍpóHeÏ\x0013=Ht¨6ì.ÿø<¸þóÔuY]Ôu1Å~ðiùåëìâaöö&6¾>ÉÐ\x0002ÅÓ\x0015\x0004
\x0006\x001aÎ\x0019½
¦õ\x0002 dßÎ^ÏÞ\x001e÷öºfxLÇTá½_iPMx¥0Ä$ãæ"\x001eh\x001cÇ\x0016xì¶ñàô\x000bÄ\x0003\x001d\x0005U÷\x0015\x0018W%Á\x0011¸\x0004\x0007´²Ñ}±xTGÕâIÕ\x0019\x0011Yó\x000f.&MPj$\x001e]àÑu÷å­I\x0003yÃ}ysM¬TxÂ+Ó#ñ\x0014ü,+ù9üþ{éy\x00012T:®ã<\x001by]ªxîªö¹\x00071äq©Þ3^\x0017®3m2f${T\x001d÷80cÛ*Ü\x0016­µíÔO¸-v<\x0005÷¨:îyFi¨
îQuÜ\x0013®KCè&ÒÑªàsyb\x001f1\x001aO!
U4|Æ×.\x000cºk}±Ü¶6q>rùèáo¶ôîÏzA\x0000Qð \ù1NüG÷ÜZ0ýU2v´é\x001e=s\x001e¹ZgÆÎß^Å)?ñÏPt\x000eEo\x0015É¡:(¬\x0002Ô!\x0014ã\x0011
Ä#Ç@±9\x0014[K\x0015#**\x0015\x0005Á3'¬UV\x0013\x0010\x0003qÕ×ã\x00109\x0015x= ¨q×ãs(¾\x00160\x001d§HMPtÇ)n\x000c\x0014ô\x0011Jì¨ÂÂkiÊ?`ÅÂ\x000b(¼úxwCÆýüÄ(,¢À"j±HõÄc6Ó\x001e3/D\x001c¯q\x0019»(ó3»zÍ\\x0015XT5»ð]ÒÐ¨]Ì8º\x0014òW\x000b\Fwäq\x0004\x0007`\x0011\x001dëÊQX
)Ç+Å\x001cOó\x001340\x0017°ð\x000eË¸wT\x0008:^)éâ\x0004%ÂÒ=#B2N¶\x0014bWÊ¹´\x0011>àÕZú' j\x000c\x0012QH9Q)åxlbE(ha\x0019u=¢\x0010-¢R´ð4Ý\x0011°pÜj\x0004X:EÖV,Å
ê\x001bÊ°Hó3Qw$\x000bºÈjº8ù\x0004]ü4º¨\x0002ªÃ"\Za\x001cF\x0018ê!LNP,\x001bõtÁººuM\x001a@\x0006P\x0014î,2ðo!\x00163î\x0019éBCë:

õæI\x0013\x0005\x0004\x001d\x0016«]\x001cõtqEºî¤é°\x0008nH`\x0017ySIG³Îµ¤¢µzÑw:ÚwÖ¥êôâ8]¤\x001eÁQõpþ|«®+è<Z0\x000b SUtá\x00024¾%&²tWt_\x0005$(^,¿_ýó¿î ôvu{ù¡Ç{
R\x0004ÂÒ\x0010¡öPG\x0015Ñh®R\x001c3ëÖVÃùßaÆÂâlövqrx°)N-²)\x000bIÔcr\x0006E_À\x0014wGLik\x000c@Zg\x000bZ!ÉL²Nñ4Ì/a\x0012)À!y3\x001d-@ÙzBY\x0005©É\x0008*Â ¸§Ë³Ì\x0005¥X\x000e
fù5rR\x0001Ñ\x001cò	3¯F\x0005(Ù\x0000Jï­oOãí	fºÛÓí¸Í*×\x0001\x0013\x0008Û@ð×«ÛðïÂ¶\õ·Ë}É)ÏÂë3Ij«@6AZMU)Ùùx¯\x0017'\x0007ó°$\x0017°ýíðUo¦J¼ûæ®WWïÀxm
ðåÁòövøâýýó»û\x0007£=:TÏx\x0006AÑX¯.¬ói£\x000b\x001aw¡\x001dÇdåÁüädÃÖÞ\x000cR÷ø©\x0002âå\x001eâõ,*âðÜ\x0013¸t\x000c@wï\x0013EÞ×!&\x0015\x0014\x0005LAÇÇêê@\x0012(vMP\x0019K\x0012À²LXUX8ÇR N&a J­þ@\x0016ßÕåæßõwÀ\x0002\x0003âçdùË/«>\x0010\x0007\x0005\x001aºÃ?\x0014\x0003`ñéj\x0012Qä ù_þ²8>ï?ÿwi?ÞAFU¦Y[ëÍyA^Á8ºÛû4Üü	(0K\x0000»å\x0003kTÞ"`7Iª|tNd|+à>éNÎzG\x0017°`è\x0016|Z`q\x0017\x0005`\x0005mO\x000cai¨dvK#QÁð-ø´ r\x0016û$½°"M\x0012ÆJÅ\x0011VÞ7	\x0015ñ¶\x0011æ< 
/=Î\x0005\x000b¨\x0004\x000eÔ\x000b\x0017\x001b£ç`A}tm°d,Ø°¤\x0006ºÅ+ySXO¾C\x000f°|#¬Èå\x0011\x0016¬DT®PK?\x0011\x0015èùøiâw³§ñ\x0015:T\x001aÆ(ºÂ`ÎM½BÈyÆO\x000b*\x0013Û\x0001\x0016Ô¾¥\x001b´Éç\x0005Æb2­@d©F¥ãtãJXWXó\x0016¼#5RqH`£¼b)\x0015\x0000\x0017\x0018#\x0017\x0008øÒ\x0005ò©l\x0015{°ã§\x0005ØÖá\x0005ÇAÕ F\x001d¢qES%CçÖËG«\x0005[Òâ+F"X\x0013gM\x0016X8²O6ÂR8,/*C£VS\x0019^ê\x0004L·\x0002sXÌî¥\x0014i\x001c SD0åÆ	S{õl\x000f
\x0011>GËÛËååUÿÕII\x0001L\x001c&P7X\x0010ëtêÈLPæ'óÃ¾±¥Åñ0G\x0018>Ç{l;\x000e$÷\x001c©`Ú\x0001Ô~:è]ø\x000cîÓ<úpºi>øËkêCkëÇ\x001c\x000fú5\x0000\x000e\x001cÏÓ4pºO{\x0016Ãép÷étÃF\x000ej\x0014>§\x001b\x0018j\x001d
øËk¢½Vc eü\x000c\x001cÏ'Ì]:>õëÇã
'Ú§±½ÍÇbÏàñº»z'RD\x0005Ç©ÁáxmÆ\x001c\x000fãzá3x¼C»%üò\x001e\x001d\x0017c-öãÅ¨ãA\x0001Ãgèø >\x0018\x0012ßøñ W\x001fmöãA×Âgèø ÿMÇkÆ\x0006Ï\x000eçnÔÍÇù»Ã\x0012\x0007;QÓïÎHZ/Pb²ùxxzXâ	ÆöÒ¯n½Nq`XÑº#
÷vÌá ðô°Àã+@Â+\x001c
\x0013Nç\x001e\x001dónÌñ ðô°Àã2N}I÷.éÑ{H¤g£Ø\x000e$\x001ex<åÞ¼Ls¾ë\x0019I<5êæ¡Ñ:~\x0006\x0017Ýo\x000f\x0011A4À;\x0017JËQ|\x000fÑø©\x00109L®å=I<O"Gë\x0011ÄYÞû¾âx\x0006Î¬HÉ=4õ­ÒÄzñZ:âãgè\x000fbÆã//q\x000b=HÎÐ\x0018eåèdþi0ÿ\x0006¥Nª]RGS\x0008Ä:Û]>\x001beé$]¹a\x0004¦µñÕ~¸ÿö¾ä¾nýõòÃíê~Ù+ÿÀ0tðE\x0012ýÁÍB:Ô*0º¥×óÅÙ¼g&|\x0007\x0014°\x0011
xÒXU\x0000d\x0002_Zpò\x0013iÍG\x000f 
\x0002JO5  S´ët³78Ù	§Å\x0004@à.îÇÏ\x0000MÅñS
\x0008¶":\x0004dAªD@\x0014È\x0010.\x000bd¹1\x000e\x0001q`ê÷õ i;H:\x0019\x0015^f\x0013NN¡\x0011`Z&LË\x0006Îö\x0018ß\x000cOÍìáµ\x0005\x001dLÍFéâË×»»oØÃ±§ÿç?þ\x0013\x001a
ïûâäA¾¤m}<Z&ÞY\x001aÜ\x001d£ä\x000c:¹\x001f»¼3è"<ë\x000fg`p\x0015ÄN¡þÕ`x°	\x001dÑ\x0010*x8·Çü\x001c\x000fhÀÛlv\x0004)+ñ³3"Z(ôìã¡\x00005~êÑÀ\x001c\x0015ÑS\x0011WU	Å±óÕÁp·v@ï¿ý°|DÅÑP\x00077W`\x000c,UA¥{(Ó\x0002êÀ6½äÝ\x0019¬þOX\x000eZÐV¢m\x0003\x001eñ³}$\x001eø\x001d@\x00029øÙ6\x0012\x0011»`Å\x000eÜ\x00009\x0010?[B²\x0014ïo,4ÿÇ®Úøé¬Ó{\x0018Jð¥Ïzê\x000bt\x0017%ÄçRÅ\x00014\x001a%ó\x0001JD~6\x001fNÏ`$Áë\x001a@\x0010®O- 	6L2CãTh¨Ûð¯&ÏÁF\x001fb
 \x0008àÀ§\x001aÕè9\x0004¡kÓÚÂ\x0000H\x0010 Ëý\x0013C\x0003 \x0008êxÛ\x0000\x0008By\x0008HyH\x0013\x0001Å2±\x0004?añ5\x00000w
<\x0004«d\x0002\x0004UÕ8x­bÚAÜ\x0007>µxªÄý6ÖKK,$\x0008å!f@
¦TÅO5 âpaÊW¤À±áÂ¤G\x0000\x001eÑpa0W&¹10ß:®L
\x001cäqµ:\x000fO\x0000\x0004»\x001dY\x0014
®^¬¿
\x0014r±³$\x0002¢\x0004±ÁO\x0000)\x0000¤Z\x0000)LXYo8\x0006ñà¥\x0013O\x000bõDü¢\x0001\x0006@
b1 GÏÓB¹ªA
iM<¤ø4
\x0019\x0000Ô \x0016\x0015\x0014[wR1e]{oéÆ\x0004F \x000bxZ¤bÐ¤i\x001ah=%=Æ\x0019N6\x000e Ý´7\x0006ã>XPÔQ\x0014\x001a\x0014+\x0012HÀR\x001aT¬nbuû¦MJ;\x001c&e½	×äHmh9åÆ`¨Ñ~üT\x0003
z,¡\x000bg±-\x001eD!h!\x0000(î8ú+s8´/X!<Íñ	\x001cn$Èþ+s0ö2~ª\x0001Á$ÔÄÓ
vîYä!
7ÁÒðI\x0014\x0000j\x0011Ï{eÁ.ñ/oòø× ÁÈpwV°>lêq\x0008$\x001d_K;\x0002Óû»ë/w"\x0006R9\x0004Rcæã¢¿FÕz\x0008xÇ»òá©QåÆÒÝ øÉ\x0003ï/7U§v;è\x0016Í;¯p\x001a÷í¥à¶rtt\x0003×\x001dýUÝÿúÅbcÐ~úµãräåí*Måz²6SàFÆ%ÚQ;	)7'¬Ïmäy\<?Y¼ì;Uà\x0008MJµ×ààqö\x0007à°\x0006--\x0001\x0013c\x0008G\x001eÃnÄá*\x001cL¤Ä;àÀ¾ÃxK8¬\x001aCïï§üw
=lÚ«\x0012p@[Azt82£qýý\x0008¯£!zÄ\x0010zÄa\x000f\x0005ô\x0018{-ð«ìÇOõ½ Z2ýè^\\x001båjys}\x0015-\x0004\x000f\x0016Bî¦¼¸¼è¯'\x000fY¬\x000erð Ñ1Q\x0007þåORëÅáK¨*ïË­Á@ÓüT\RÅæX`\x000b5£®\x0018c\x001faÒÀ9~jÑÀþ\x000cÌ\x001eB².¡Q¦#ÂR©G\x0003î\x0012\x0017
´ÑèÞBúC\x0014D\x001c)û¯ª\x0002\x000e8K\6ÀQd¥èà6	p¸ 8ê	}W\x000f\x0007\%®\x001aîJ/©\x0003¡$RGQqà~\x0002\x001c\x000b\x00127~jáXuÆÁìv\x0018#·Ð\x0011ÖÅ³& \x0001K"~jÑ\x0004\x0003ÎÓ]u±#&twWþ	\x0003®\x0016\x000e\x000cÐÝjâhu\x001b£Òø \x000eU¬söTú²\x0001N&\x0014!Á\x001f\x001a^»TøÚÓNøÚ;\x0006â\x0013@\x0005!\x0008&%ÈÂe5 \x0015§ÎE³Ö´1f÷Sµ\x0002
ò'!\x0012
¤ÆUGÁ\x0004§º\x0016Ë4ZxÛ)\x0012(Nìº«\x001e\x0010G\x000e¯Þ¦^Ð\x0017¼Ó\x0017í^ÿþõæó»|¶&¹ZÍÎâ\x000cÛ>Å\x000e½:\x0019\x0018R¹43FÀèu4@5SO%æ\x0017³³8¾¶\x0002SgîTcqÒ<aRAoÄÎY!S®ÓV?áN®1õiù\x000cSeÚ6ÑIòÄH\x0001\x0013¬æ\x0014NPE0§âZMt
¿n»»ÀÜ6\x0019©æø\x0003&ì4\x0014F°©wç÷ã\x0004é\x0006L´T>ð·i\x0006eÀ¤=:\x0012ZÙ'\x0004w\x000b&¨$4¬	ÇU\x0001¤®?)XÚ+\x0019®Ê\x000eiÀä \x0000\x0014?
L\x001e\x0008eE\x001düMì¡±3.o#W2\x0000ªéåA\x0018q9ó\x00187	"+m8\x0008·§í\x0013V@\x0013(ð:dÛÓalÄRë§ËÇ¥Ì4Páé\x001c×.\x0017ã\x0015¯OÅ1ÍñõÙ´Þ\x000c^¥×Ç
é´IÎ\x0008Ë4Áâ\x001e%p\x001dSa\x0015%HÎ/Pê}¤Ôû&®Òiáx@¥ü\x001eG¦²X\x000e¢ýSñÓaT_~ùôùËÍ»õí£ÕÝlq±ºú}uy×Cf\x000eö
¦Þ" é]Ì!3\x0014PÖ\x00059£\x0011´õ¿\\x001cýïÅái¿þÍ\x0004y+jw%ØAa\x0011¥&:£³.Èf Î®¦Ç}ð\x001e¶¼Å´¨TD\x0011\x001bI­@À+Ú	@ô§"©0nä\x0016D\x0011\x0004b\x0018C+\x0010(¦Ú	@]i\x0003E°)\x0004F'Çn¤",Ã­@ôÕ\x0014a¸JÆyÇ'&ã²D\x0010gÆã@\x000b¯#Ð­p\x0018ÜeÀA*¦hTi\x0005"÷ãhÃí\x0003	ÄäÕ¯F0¬\x001ep^ã\x0000``VÌ$\x0006$z¼d$-¯æV\x0006}ÇgãSô  qÔIbt®[@EY5»J¶FÂÒôÖÄ³î\x0001s9\x001a	\x0014-j~\x0002k§ ½=¥Y\x0000	U\x001b5\x0001Ü;è«\x0018iB¤E)\x0000FªñO\x0018#D5ÃJÓ@\x000fHÓå(Ì\x0012\x001a1^ÊCÙ¨æ×\x0000D¹®÷#¿zj55ÜN IàUQÏ¯\x001a[`d
ß\x0000\x000cK¢ù	Ú§\x0018\x0017O\x0011®-jâþþÂÇ¢o\x0015kJ?ätùþáöbù¡ÇU^¤±ÐÁµAÂ©­³Jc\x0010 ðîÓäéüÅùÉËùA
®\x0018òoÂ¥ãà\x0003Ù*¹
®ÃÂÈ­zªG§
\x0017\x0004ÿE+.&j$\p;b|ÚÇmÁ\x0005Y\x0000ÙK5.}°û\x0013®§j\x001aqá«\x001aq\x0019UóÒ\x0004À0Ë&\x0019\x0006*¬ÖÓqA½iÅ¥|\x0002\ªÃ%4Á2O;p-° lÉ¶ÁâÊ&[08^Püáîg\x00075:O{àõ¸x4Åx#A\x000bµÃìq°W¥OÀ°7\x0000	æ ò1~\x0004X°Ý)½®e´\x0017\x0018æ	kÅHAqy{wÿ\x001bìw>ñýø9ZÞÍ\x000en\x001e¾¬nozë/¤ð©:
(Kñy\x001däUâx&evÎ\x000eÏ_/Nû%ü¥{øñåXèå¡Ð+j¾ÙÁòË×¾| F*@ñ\x000c\x000c\x0012½¯Ü;Äàri\x00003Ò^¿\x001d>ÞBküT\x001cÏéx»G-ç)
§k]}úí\x000fW&5ÄAÃÉÙãhy»ºþØT*\x0007Lh¾Ç46èQ\x000307O%\x001eÍO\x0016o^ÕÀjv£àH,à
\x0012\x001bCy\x001býT:²\x001e\x000e\x001bÛ\x0000GtÅþÊ·\x0002\x001cJµq.
¬ÕÂÇñS\x000bua\x0001ÈK`K.3XìÍSuãµh ß~ß\x0016\x0019»ÂÚ¶àc·©¢1BÌ§|%\x001a\x000f\x0002É\x000bYK\¢
EìË0áßõH\x001c÷TÊo\x0000ÎÝõ§û_.
»¾ºËÙðooª	¤P©489àýD©+Q\x001bÈèeÿ\x000chöâðÍAª¡éKhe°p½\\x001b,ç÷\x0014¢r\x0018ì\x000c¸\x0004{©3`\x0015ô"ï£	g)Ý\x001e\x0005¨`\x0012§\x0006=\x001biC&a,\x0005kF¦Hz¡¨\x000eJ*4b¸c:2\x0019ÀGÐL"ÍÔ\x001a\x0019¥#Âm>i;6"\x0003A%F ã\x0016IÔñL\x0010²§ênZÅé6ÍïÒïÑ³ÔÝ\x0003\x0010)\x0012\x0001lf^æ °8èÞ²ö§ú/ÑL!ÍÄúmþ	4ûÓÖçF²¹\1¢èè¦\x0014±#óÍàï\x001d\®~ÿú\x0016ÁSû8¾ý`ùqyO=4um0¸#.\x0016\x000b\x0005Ó\x0004\x0004¦Ë¸¸P\x001cÅ9î\x0007óWó³¸ásÖ\x000bÊÿz÷ýòw¨F\x0001%\x0019?\x000f·÷iò\x0013H \x0011\x0010¶¹F£\x001b&\x000eE\x0012¹8÷4Y7ôâà¯ó³ÞíÉÙù\x001e.=~\x0006Ï×épë%µPy\x0006pFLýáßî¯äÃhBAw"|În_VwËï\x001f\x001fz«¾!eUß\x0016\x0004ºBcöª[é3ëòìdþzq:ÿû«óE\x0001i\x0006\x0004LKøÔ\x0000Ìa\x0005µÌ`ï
S¸\x000bÜ*\x0005
@3"|ªp\x00047,\x0019Ö8Üí\x0005[Ôø§l\x0016m\x0005\x0002]ð©\x0002¢\x001dV!Ú\x00181âÔícJñ\x0014I=\x0012\x0016òéUX Ôú#L¥©
ç°YOà«Â"/Ìo÷\x0011K4>
ë\x0003\x0004ÈÕÍChä8.8©\x000e®Q\x0002¯\x0008J\x0000Ð\x0008 AÏû=Æ\x000c\x0012X\x001dÙ1\x0008I¤¥@qÞ*«âæøF¦\x0019ÒååêÇG\x0003 ¹\x0019?ëÙ¡/n ÀñGhaÐA/[9þÖSGyÝþzrècnü¿5ày;Û\x0002ÉxìaÕcA\x0014Ëcÿ¡ÌsQ£\x0010ÅmÞ®\x0001\x0011L\x000báIêh®ÐE¡Ì\x000e!Å\x0011S Áw¾\x001e\x000biÂ[\x0013\x0014~°Hèµ)a§Ý\x001b¬>zHú,\x0007²8Çtbf\x001a \x0012?c\x00119õ\x0013¢§æ\x001bW#²@\x001eÛF#hñM û8áQ8\x001b×Ê¼°g\x0004 \x0007¼ø©\x0007$\x001c½\x0013\x0014j\x001aah\x001d#ÊG=ÿå·Oýñi\x0006ñ¼ôõ\x000b0Ëx9ûËÍõ=®ï-ôO%¶ááY(,ÖÕhn)Y\x001b°\x0001F\x0019Ïg9~s\x0006ËåûM?ýõÖ~þ×\x0004³ë2¨´\x001e$`ûî¥1Ô±b-r4CcÃy×\x0004»ë0è²á³-Ó\x0016gk\x000e.±ôÙ+ØbÇ+J/zÏÇ\x0000p0d+~\x0006\x0001H¼ \x00100Ð\x001b~ÿnuËå«\x0001xÐãñó¯\x0005°ú ?8ð\x001cø\x000eñóËÛ^Ë[3
Dq¡tÚ©\x001d,n	¦ ª²úÎ¿\x001c¿\x0007_¤\x0006\x0007\x0000¾\x0006@Rá|XÈÇ[ÜÒbs:x¼»àÜ/ïRÂ~?~^­ú\x0014É5\x000e/2õ»\x0018ÜOÌZyµØpðýõ\x0007ÆK:(³ÏÁòýÍÃÝ]oæ%ø\"Õj»`Õ+¢<çaÂ³yH§§\x001bÒ-\x0019\x0004\x0008ôÃg\x0010`´ßÀª`äs (¬\x0000±2{~M\x0008 ô\x0002a\x0004cB?x\x0014\x0006}?Çµ$Á²|p\x0013\x0004ðþà3|\x000fAð!
÷!|O$p¼\x0001À[qyýË»lØßüú~õáSÏá&(ý8b4h©À\x0003i¦âÊ\x00078Ï"Áó7gÁýíu8»£
ðMül<;<=øMc\\x0004\x0004qJa¨\x0018Ê\x000b¡:¼æ÷N\x0003þK5ð«´ß5üî^\x001aI\x0019\\x0005ÕÒ\eÓ\x0006ý_ÿ\x001a\x001f¾\x001f>»¯Ë»;Ø ÕwóÐþ&hÇ{|ÿ\x0012G#ÛË´8}{8?=ÝYýòç÷_ÜçËx\x0005\x0012®\x0000vóû¶\x001a\x0004ÇÓb®Sq\x0018q\x001b= ðú¥`û"Ü¿Çàû×_¿GÎ\x0007»Ö=
\x0016\x001f^]ÝôA\x000b­qY\x000bÎcRAÆÉ§Æ}\x0004s\x0004ºþñ8HB¸ÇxJî\x0011L\x001bÆu§°ä\x0001dòSMlCx>ç_£dpàªÅO\x0007z¿nÚMcã<Èfçêp+F·2ióDG/ô;¿Ýpa9 x1\x0000iYI²=ì>\x000cúÓâz(OÃðxjÖ\x0010¤Õ/K©SÍB
\x0008^^,{\x0015h8ÏRØP
¾µ\x0016´¦Ê\x0017×/\x000e_Î7¨Ð¥üøíÇ

, 9\x0018?»\x000fË«þh\x0015*\x0005\x0015AkÕ¡ ¥âYqqz0?Ú\x0010é;\x0018ãgèxçÓJ\x0012ÏÂSI¸\x0018\x0003-ÓÙ&êã\x0003æw\x001fÒïÿa\x0010\x0001×i\x001f¡âiC6Ô¡ø`*Ëßà}Bð~;W\x0000\x0008.\x0012A\x0004Ìag óVÐ-¨\x0000\x0001\x0011ÄÑÖc\x0010,\x0013å \x0002Üà\x000b\x0008¤B=\x0006Ö\x000còAÐ¨õ·ðë\x0007ýõÇ£í\x0008Y5Ï«Ûå^¯\x0012<û$\x0014\x0013XhÂ3F_B\x001a÷t)Ï«ù?úSÊ\x001d$èCß\x0006H
\x001bI±v7Ðü|ÙW\x0000
ÒÈ9\x0006Oµ\x0000\x0012\x0006\x0010\x0018«±\x001f\x0019j\x0001\x0008xº?²\x0012\x0011Ô\x000bî{ÞD"Á Î\x0010\x0019¦.t\x0007i
"ZÆäO=c\x0003÷&Q½ÀµY\x001a\x0017NûF`\x0002Ê\x0008P·¿]}ÍÿÀñÓ!:¾»[ÝõfÊ \x0005F¶\x0019Ç
¾r#!é\x001fm§êIOO\x0017§U``.B1ºi\x0018Lâ¡\x0008&	½\x0000\x0013\x0016ö\x0004qjÑ8p9]Qù3FxL\x0018\x0019
ó`\x0012i`\x0015l£´@\x0018¯óE\x001a}8\x0002GH¥J´aXú\x0013¬¦§FX\x000c \x0011nÄmÜ0Úm¢Ízë?^÷[(Îk¢PÈº-\x0004,\x0010¡Z:þqûâðÕ\x001b°UúDb\x000e(jë\x0000éC=&>_°\x0005ÊD°"	\x0012{z\x0002ATC£¨<\x0003¤\x00062é¸b\x0002 \x000f\x001c¨$ÖÒ°\x0019Òolyóù:kù{\x001dÔèý²?\x001a\x0016|`G<a\x0005FÃd7ÈÇ©Ì|\x001d\x0014éÙ|S8ìÛ\x001fþ|_æ!
}{Ó\x001d\x0004¥¼¢q\x000c\x001fª¼÷\x000crÑ'ÇGGý\x0018>è»åwpa=Æ~üïÓ¿\x001bW2n±\x0014j°Â¿c©5]g\x0013{ÀåÙ0\x0006B}ý¸ú\x0000©<\x0007óâçÍòýeßþ\x0003\x000fÃL\x0013\x001b(\x0018³\x001cÁ`Ç¦&)ïm6þíÍüÅaÿÒìdÔ\x0007'ÃÙTÝ\x0002!uE8\x0015\x0010a1ÈöûU\x001f
¢\x0014>6\x0006\x0007j±83E£ûkÐM«r[\x00084|6\x001f
	I<Ùàf\x0017X\x000bÍ»ké¯\x000fß¿ý¸F\x001a¼5ÃÕ®ýá\x000foRñ	djS	E'ñ®­Í\x0005ã|ööh~¸!òáÝo_®Wq$\x000bíóu:4®v|è\x0003¹¸3º×{c`¡)\x001a@°-åq&îu<ß\x0014\x0011Ê\x0000Á\x0004\x0014îZ\x0000\x0019\x000cÌÆ]¦i(t\x0000¤hù2ÿy\x0019m\x000b \x0001}F5\x0000
j"$/¸¢UL1Ú$¬Ì\x0014@\x0016$Í³U\x0004m§¦Ùo\x0000(\x0014ü¾	<\x000c=Z@\Ðâ\x0016øçÝª&ç°ÐZ÷Sjv\x0018¹þª?Ç	±qÂ\x0008|N\x0012ý±a*(nt\x0006¡5\x0007ÇB)æÒÎ.è È\x0012é§A{þcSyY\x0007\x0000æ¦îÇÏ\x0000\x0000Ãº\x000e\x0018X3Ä\x0014×¸i{ñJ\x0003\x0000hA\x0000\x0002\x0016çD\x0002@ã"F´Ej\Ö\x0006ßp¼º\x0014\x0017¿ÄG\x000cCcßñò{ÿþ\x001e\x0005Ù´ÔÑjº1ÊT\x000e\x0013\ |@ãß7¬ìùþñúþ	ÊúÀr\x0011¬l¸¿]~ýÚóû\x001b\x000eä\x0014\x0012cOK\x001dÞâÓ\x0008RÍ?å:ÍÏNæoßöS¢C¤D¯CUß²\x001e\x0014L´É\x000c\x000eÜà=y©zÓS\x00029ê3Ó.M\x0005\x000f:ç\x0003åÁ_\x0007õsÙ_þ¨p£§Ò\x0007³Þùl¨SÐ?\x0007\x0007\x001dTÑá,øoâaµTQ;®\x001fÅÂ__.{ÙWÂx0\x001b­\x0001¥¡{=ò/H,4×Ü=]\x0001üúp¾^~º|EUPä\x0001ùõÇ ÓzÕ³àj\x0012iw~fØµ\x0000{Ò×4ó*²
ú¹;?\x000e6¡ó\x0016èæÂS<a¬åR4þ\x000fÆ-\x0002\x0000±eø\x000c\x0001\x0008lIZFBf.UIH«%U\x0007ø1çCL-~\x0006	ÀmÊ¥ê\x0004A\x0007iY\x0008û6Ü¹½7\x000f_¢m\x00085,ð9YÝýö°ºîívæJ¥jº`\x001f\x001a²L=í(
¿Jf\x0013,Nÿý|ñ¦ß\x0017èÎ÷P¥\x001c?Cç3aSÔÅ³  °2ü\x0019KÎ\x0019×Ù\x0006ÆA\x0000w¿ÿt\x0013stPR\x0018?G«×½U\x0013|-\x0018\x0019\x0001éy\x0010\x0015)è£\x0019NÈv0k1ÙðêÍ¸ª¸½f\x0017qÈ-\x0004cãçôæáêò¦¿:À\x0006"Y]Á¼P\x0010Ô\x0000ëÜ\x001a5q.Ï\x000e\x001e\x001f\x001d\x001eorÅoê·/Ñ\x0017Ä0|N.¯/ÜâÑ\x001eÙÏFï\x0008÷_*\x001cYa¥ÎâÊ'o'ÜÚÉê\x0000ø\x000c\x001d\x001f\x000e§ò\x0004ªÍ1ÆyüõE^Ê5tü\x000fûáop¼ã'FÕ\x0017½ô·01$)s\x000b~iÊn\x0018C\x0005ÈBeÙé\x0018V¿ÜT¡!/¿J°vÁ\x0015·P¥õpÑkäj\x0006\x0005uÑC-\x0008\x0018*î\x001c¤ltÉ[(Ì:Ù{øÃõo?àð\x0018Ú±[º
¿üª¯nM;Ú&äÿc±6#ÈAì
:)\x001bu\x0000¿ÿIøõ\x0017ý\x0015k¿^~¸²å å\x001däa{\x001f 4A\x0003¤)]J\x0006(íã\x001cw^C5tÞ\x0006;?\x000cì7h>®Ìû4Ý\x0014R°ðÅA½Þ1ã´§\x0003x=æ¥9\x000e{0>O\x0004ÇÚ ~ÇüêãgÍÿÀü\x0017Ëï?úe\x000f\x0014£¤Ì¦P¡£KSZfPY#Ðùßÿw\x0002Ð\x001f~>\x001cÖøÁgàpÞ½s
0+ËÒd\x0017,ølDÌÀáÜ~¼¼u`ÊÍ\x0011?/.W\x001bRÙõXLºÔH\x001aLV®1e³éÕ/\x000e\x0017\x0010úª8\x001az\x0011á³ùh¸p§1)0\x0012\x0010\x0004qMdY<¤úp°lãgà÷6.uB"Ñ¢½¥=¦©LÝ~8øñ3t8T\x0010ªQ×h/\x0004å\x0010ã\x0018éæÃÁyÏæÃ¥cédî1ä
	 ºp-ê¨?\x0019îÀgàdX"ðÂ=Zx:F\x000fðÂíÃÛÌ ·ÁäHãð[:â~ÒÈ\x0011¬\x000e=~\x000e·8?\x0003,r\x0002+ä¨xÀÚvVhé~ü\x000cp\x001bt{îpÜ¦µ¡Ã}õáï/ÄÅWQ´f\x000c6d\x0018ê,ÒéÆª§
p2×jT]q6õ`\x000cme2)álJ5x´ïMæ£Ñ\x001a§¡ã=NsA<¸[\x0004Ìhúå³¬jÃáÔZ1P\x0008\x001f§i`gY8cCÂAÓVs3æø®b¨\x000e\x001fè-°\x000eßÑ\x0012''©\x000b?Ø\x0012bÌñÔ31Ø)ap\x0008@8^Ð"»à\x0008tÇg!Ëêã×
\x0012m\x0011\x0012¶\x001d¤¾\x0008*5´NÑf\x001déÇ\x0010Ý\x000e1t¼ä8×ÌÂø$n¬[7ÑqW}º½7¿§3 â\x0007åÿÝëK)cÀþFO2¸Ï\x0012Å\x0010Y|\x0016æÌOÏúeÎÕíÝúQä\x000f··ÿü¯þµ>ÁlgýÒX\x0019.À³.Åi2w"\x0018Ó'
VU ®fa\x0004Qµsj¥<ï¤®)J\x0007\x0010|¼\x0014«Ï&"ð9Xþóÿû%ðA¯Î±>Õy\x0006:XZ©_PC\x0018úÓFç¥ÎçÁ¤>\x0019>ßÁÛø\x0019:?6Ö&\x001e Hñ\x0014F\x001bcwL·ïá¿äÓ
l>ß¬[\x001dà)\x0014Ã1x¼¬ÿõ¯?ÜòÑ££)²ËÙÁíòý?ÿ»7$\x0005ÇÓ 
<Æ\x0018ì¬ÄÈGiÏg\x0007's¨ù­À\x0000Ý¸¡¦\x00021¸FÃ\x001b\x0013»Y\x0001\x0004¬E\x0010ºh¹i\x0001A³R+@\x0017*Õ<p¢r	Áel;=\x000eDÜIåqÅÕ\x0010
Ùù\x001e¥âû¸ÉÂ{®\x0005ÄíGþõó¯ïÖ£_®®/û¤A°ì\x0019 8|0þ\x0012$´Öhø´\x0014O¹xs¸Á¿d¿¾¿ù-ï9\x0018X
ÏispJ``W	tt\x00043¦¨[mÉ\x0015GCXI
\x001e\x001dÞ\x001dz¶NÒÈ\x0003%¸Ñt6sígÓó³¡É\x0000Ï¶\x0002\x0017)¡éh?â·\x0006Ja\x000b~-4à\x0006T%°Í
B9Â8\x001b"iÃ\x0014\x000fê6î³9ò)AM\x0016,À[tc\x000cÿÚ6Ù<é²5Ç_[Ëî²ÇüÚÐØh/¥}8áÔp¶£³u¦ëêÏ¶\x0010¼\x001c<Û8Ü\x0014' Ü+%p,\·\x001eó{ÃR7x¶Â\x0000)jÒÏ\x0002Kpcc<NÍ\x001bþ­mr/ày1,\x001e
¿u'V¼\x0018q¶#ó\§kálcÒÖlEÃg\x0004Ëç{Õ\x000c=\x001f\x0016h\x0016s0êu\x000fÙûîh5ây#dåY¥\x0016ÙÌxl\x001e\x0002YJ,î2_¶þl¨Ì­hn}6QÃÓ¶\x001dÉÇ\6\x0014â\x000eK4¡à=\x0013É
Êq\x0012h¹éP{²\x0002­B¢1Ùñ¸¦19äëümD\x001b\x0014iá\x0001%\x0001\x000e5ñp&è¾­i×\x0006\x0002\x0007ñ3$W\x001cFê`X/¤aB\x000e½n×.O-Èÿø\x0019:Ü¦ùàð;lWèºÃsÝ|vì,Íg\x000bÎVÜã` ¥4Öè\x0005Yï«ùíúê×{\x001d«i (REéòõjÙ8d!ÒÙRS¤8,9xqEÑÛ£yÿÙ·÷¿o\x001f¢¥\x0006µ°Û~ìwßáJ;*Ï\x000eÌã´xUJ\x0002Ý[ýßÏ7ú«Ùùq\x001cÒðùà#¥w.]Ð¨\x0016ÇvyÚÑäó1)-çÇ`]Åù\x001açó»JªÀ\x0004X*ÿ4æ|\x0007g»\x001a\x0000Ö)d=i\x001d­\x0013\x0012ÚÒê%èÕ\x0003¸ü$ÿP±¦	Úâãç/ÁYþÐ_\x000bcU8ÜÅ\x000ctZ«Êq\x0008½²¬5\x0005À]>¿ì÷:\x0000\x0012ÇÏ \x0000f`Tr,@ÔLÀyª¥r¬±Z¾ô_ü\x000co¹ÄZ.`dÈ\x0019(çÃó³ÔÈàñ¯\x001fÔÕe\x000cY«\x0004\x001f:¾7l§\x0003ßcØÎZC­\x0002Òà®\x0008«s\x000b\x0010ôGîî»»øò5Ö¢Ce\x001cAø?ÿñý©p¥Å{°:-lÐ»=âù*ÿ­9\x001döeÄõ¾O\x0007\x000eK
çUÐ\x0001J\x0000p\x0006gy`óé¿ßqmáýyÈÆÅ\x000fÔá÷Ö¾ÀÞ3j³zOsØàßÁ2>+²x-Tá÷?¼O¿]¨Ô	
EqôéröoË\x000f¿=@¼°/\\x0008«rS×q`}J\x000fº}S ÆH/ÅÏþm~\x0010%@?ý¿ýþ\x0007\x0014\x0000:~ \x0002àäò}ÿ0îøêÒ \x001a\x0000ÇÝ¢®`rè¼¦òtvrøb\x0003)®?¹øí(\x0004!h\x0008×ËÛð\x0002úçònHmè¸ÙPÛ"Oöz~\x0012ø¿ÿø_/Vß\x0014\x0014\x00183¨mw±#åöãV&:óà×°N!þò8]	~ù¬\x0000.ýªö_ÞúñÛ²¬H\Ý¥JÄÞò\x000b\x0019ø.Õ?)\x000f
P\x000bg\x0004"+@b\x0005â\x0006>¼ÿ¨\x001fî#\x001f\x0002ñásüpÕÛà´÷©þ\x0005Ê¹\x001d¶½[Õ\x001fÖqÍgò§y¿òS÷\x001f¿_>Q|Ó[}\x0004\x000b?òe±\x001c?½ü.[ä!]ß\x001dÊoÎzÿöÁý²Å1@&áøÛû
µOÁÆýg0"ESí\x0013ëÆØeó0ß\x001e-ª\x000e\x0007¹\x000fÃ¹Mj\x001f\x000e§²\x0017côúpéF\x001c\x000e#Yà3p¸À4I8\)lI	Óîài\x0011É\x0007Ã¥èÈ\x001e@S
0E\x0007cèÍ³ÁÜnøÊU×c¡ôºÜÚpÍTmýáÏÐ/®¨Ò4XÔoklwå8\x001cªõãgøÊñ7çëIöF«®ÿÆ¸rpnâgãáÖ{Sþbó&
ïèl5â¡A\x0005Dü\x000cüâ\x0010ÿ×ÝÙ8?ÓÈnX¥ÈÊê\x000fð¡W\x001e~q\x000b<·\x001e3¢á\x0017ïzzx\x000c«=ÜCÀ*~®\á\x000el\x000fÝW^¹£ß\U?4-~÷ßÆ¯£á\x0006+jìðö[ø®{Hf©øuN\x0005\x0002êô\x001aF\x0010®cÂt¸Ù]×8\x0004]kW\x0005
lªø+\x0010TÝê°á\x0011® ØyV
aÝÌUA\x0004Ko\x000fº¸°À\x0018Þ{×Å5
Âº}k\x0010\x0002\x0004n=öm\x0005K/Õ¤\x0018kéý[S,Ã\x001bðQ^ë+ØJ\x000b»RöãçtuÛ;úË\x0005G\x0006#õPKNE\x0001Lt5,\x000b1.Næ\x0007\x0015GG\x0014?zå\x0004·*þ¤Ð­GÇMññ³ñèpÇT\x0007\x0000EÞ´ºÑà\x001ae2¹Wy44eìÇÏÆ£\x0015C:pí
M6¯´öd¨»Íô\x000eïÜáÑPf£5ùòÁ¶h>\x001aìÁýøÙLo©^\x0018³Þ&d©BO×z4ÄãgÞ¦»jð¤Ám7\x001dÇêö£¡T'~6\x0013Ü=Mde*¶\x0008ö\x000c\x0017ÄÞY\x001dqåÁ\x001en(~\x0006É­RÔÆ§y\x0002Ü\x001eµfµGÿñéó\x001f\Å
\x0014ð9½¿¼ºº¹î%¸u0ª8m¾±XÑjì&±,N~z\x000675Çõ\x000eã\x0005ÇÓx\x001bÈUÐ$üÝ¡§{Üñ\x00102ÏÀñ0«=µYo\x001c¦÷-<¸t¼\x0015ÙHËãÁ}\x0012uèx«Uãñ©Èá\x000e?8=Óê
§\x0003\x0001¡«vÆTâ\x0007¨ÒéA±b_QÝÙp:x\x0010ð\x00198]ÃÍ§A°ä"ÕÎ[Ø®Çç$«W,îÄd\x0015ÇÇ\x0002t<®¥\x000eÇK+éx=â·50ñ3D{i¨¸4NWIÏ\x000evÚáñ:«/l8\x001eög°W/LJUÀÕS£å\x0013ñãf±öãaCT/C¿=Nköb\x000c\x0018XZu|/Æ\x000e-×lXæ(N3¾ìºßrãö¨¯?\x001e¶R²a\x0003±)ÊÉ¡c,\x0015×XM#Ày~\x0014íÁaÃ2'Ð6Õ×Ó@mr6H<Ú¼Æý¨ß\x001e\\x00196,t4çèÉÁj\x0005n\x000ec\x0008¾a~Ä«qMS#òÀÑ¹ÞyÈÇÃ!ÆScHo=Ô|øa\x0013Çõ¢®5dÐ´6:X*®ýx\x0007e*ñ3Dzah¹¹´¶\x0001\x0004
GcAãüéæãAAÇÏàñÖÞÃ\x0013@ÓN8Äå\x0008Ú»\x0018\x0018w\x0015"çÏ¤ýo·ÚÿòÛ»ÇsV·7Æ4ñ®Ãu\x001fßmJ\x000c¸|aÏüälqr¼!=ôýÞ|3\x0005Á{³Õíþjnp¢Ò:Joa?NJÏpf[/]VÉ\x0018\x000e½!2ÿûýýÕò÷wÅ¸åìló	Ø®zxX¸\x00006{L\x000e\x0007IlMQL\x001c\x0006!¬wF
B0^P,ã:ÕJXM£.d¾{\x0010ÂoÌÈ\x001f0.CÀ4~ÎnW},h5õg\x001ct¾Â=/Ñ·)ë\x001b8Y\x001cn`ÀîhZÄÏÆ£¥ééÃ4\x0015w\x0005Äô¨Üg[¿k\x0006g.~6\x001e­DÌG¤õ\x000e{rµ3ÝÀ|EL*KãgàhÉÂ\x0015S\x0007OÀ¿5Ï\x0014}åÑ\x000eÊ\x0000âg3ÁOj.ücKnô\x001fÞµi'x,ÍÍGÃo\x0008\x000e\x000b¥LGS\x0015kð«³ùê£Á{WCw-µ%«`Y¥Y::8qÈfN\x0011GCïµ²\x0004g8úCoª¡-Ì\x0012èàH¶\x001f
-Óñ³ù]3\ÁÈµbtÕ¾cp\x000fµËu'¿ç\x0006Ú®adJú\x0017á/öU\Jq}?;]^^ß÷n
TPî{=¥ÆÕ:Ðýî½\i\x0008Yf§óÃ7gý\x0003@\x0010
,yÉÐÀ5pDx\x0001©h?¨8\x0005U!\x0001\x000etò$4qe@\x000b\x001a\x0008!Å^\x0005¾¿þ}¾Þ_x×m±é­P6\x000ed¡\x0005\x0014\\x0010t<`nÃIhái·Æ¦R@\x0007NäàD#8³GØ\x001c69\x0004l´Ùêlä(l2Ç&Û°\x0005G§à?3\x0006»\x0018Æ7'S98ÕL8´l`\x0004	çH9r)¬~b1e\x00138Ómà`³tÂ\x0006ÃMÂÆ©&Áf=ú£ \x001ci¤N£ß\x0012Ý\x0004½\x0006Õ]jA\x001e\x0005Îæàl\x001b¸à¬¤=+\x0005W-i1¯ÑX\x0001y\x0013\x0019ÎåØ\3áDG7enD¶Ìª\x0018\x0005ÍçÐ|\x001b´à^+ÌO1M
^Ó~*ëü4~ã¬¾¬n
\x001dÐH¸¤)\x0003áº;Í[ùF¡+uCrÞaD0Î§\x000c¿^le½&y¡\x001bx«rPX\\x0017IF~]æ\x0002[\x0010§¡+´\x0003oT\x000f¬ë
5¡\x000bÆ\x001e¡*æx¡\x001ex«~¸P/ÒÎ+¢]Gºà
õÀ\x001bõ\x0003siÐ!(\x0008F#Ë´]_¬¦¼x¡!x«@Ý\x0015Lê4{"·4&y¡\x001fx«`8F>ÜªÄü¨
\x001fdËM¼ÕBAðV
!pxC$\x001diV¶~­Ó.U\x0014bX´aNó\x0001Æ÷ ¼ï¹ià
),\x001aMt\x0018°Á.%´åp®PÀÆÝDÊ\x0016z«\x0014æ8\x000e%R¬9å;Q"¦©~QHaÑ(\x0004Ñ\x001bÑ\x0005_P Àêÿi\x001aL\x0014RX´Ja\x001a²\x0012íP÷Ó<\x0011 \x0006®Â¢Q
[G;M¼7£qv 3qüä\x0014t¨\x0013¢Î+Ì\x00189\x000f-6	Ã$µ3nê\x0017¤\x0013ÎøÔê<C\x001cËn]?LWXÃ¢Í\x001cÖ09 e ¨#%|`\x0003¢3VMã:Y\x0008bÙ(!FæÖ^5ÎtZBLó¿d!e huª÷tq¶]ÒaVP¥É¯BWHbÙ(¡eÝw¤#Nu¤\x0018Èe°¤M\x0010\x0007\x000f\x001aû\x000eê§R#\x001d_Hº<\x000c:
]!e£ J\x0013ô¬¡E\x0006Í:µö_å4ËI\x0016X¶Ib\x001bÌíÀ(¦·]M½QÓô¿,ÌaÙh\x000e\x001b»×YÄÝ0J¹t\x0013Ñ\x0015jB¶©	íd§Ä¤¤\x0008"ý%Ò±Â®P\x0014²UQØÎ:ö0K´ë¼	5Q\x0014B¶)8b
¬ Ö%\x000fk\x001avrUP­zÂ`c\x0013´B^)Nv:5\x0011]¡(T¢\x0008Æ9¬îK¤ãØóé\x001dUR\x0005ÒMd;U(
Õª(\x000cud\x0002í:]vaõ*4jÓ\x0014&`Ð(í¸Ã¢zï\x000c'ÂN3T\x0019VoS\x0014Ú[ª\x0014r?Æe¸YÊig6³]æêCW(
Õ¦(\x000c¸®6y\\x0001æ£¥7ûiÖ*4jÓ\x0014ÏO»BS¨6Ma\x001fU·qRB\x0002çÉ\x00173l\x0001 
=¡ÚôÄóS®Ð\x0013ªQO8\x000b	è\x0014Î°ñ\x0001\x0005¡èéBQè6Eñì´Ó¢ÐÂQ¨Ó9­qÝ«ï(g'ÆÄt¡&tx~Ê\x0015jB7ªN$Y\x0007ÉÐ²ó´aÜÁ\x0016¾i´+ôÞ1=¡Ëük°LcÜ	
^)è\x0015Ö½9-'F\x0014u¡'ôé	]è	Ý¦',W8\x0004Ø9FCé¼\x0007ç:¡\x0013b¦Ð¦Ð;¦)t¡)t¦°PîL;ë8Ø vªm5ÓÓì\x0013Sh
³cÂ\x0014Â´i
+,\x001aíÐPII1oÈUÎM\x000b BW\x001dÓ\x0015¦Ð\x0015¦MWXap%­}Di\x0011H \x001d\x0019wÊLL(BW\x001dÓ\x0015¦Ð\x0015¦QWÀMè`â¼§7«ï4æB\x001aFi\x000cíÏÉö´iÓWÒd¨ÈÔÄÈ)¤i´aQ@²P,\x0014\x001f
´Ppfb6Ö\x0016ÂÎî°³°³ífqÒ±VK\x001cêàa¬\x0006ÎN|¯¶x\x0011¶ÑË~npñdwÌx²e\x0001[£­\x001då¬íb£1%´+'Ûf<\x0019g0\x0002\x001bâ°éØÃx\x000b¼Y?1b\x000bqb\x001bÅãá©(oçº\x001c\x0016\x0013±\!O\<1Pe¯Â3\x0018_nÔæ\x0013ÍbWÈ\x0013×(O8£1X0@\x001bß¬\x0013´\x0012\x001a#¦¡+'×f<\x0019ÉÓòrpÇh@wÓ«|Yì
ãÉ5:ÚÌQÒÓñõ¥¼ZÚiOÖ\x0015¶k³L@Ä0j§4ycNR!\x001b®Ð\x0014®1qç
V\x0013\x0007Q~Ç1O~6\x0013Ñ\x0015ªÂµª
¦i\x0000í\x0002PR\x0015\x001dé&\x0016î¸²¸Õ¥dvà:Ù²9U)\x0004{Úõ´óÖSÐ\x0014Þw\x0017eÖ[×é±qâ=÷0[X»u×ûðãþ«\x001f«ûÿûôóe\x001f(\x0007ÅÍIA\x0018ca\x0003t\x00132CN\x000eË¶\x0004¼:ÿÇâlvúÿ\x001c\x000e"ñ¢@\x0002ã¶Ätà$Î·\x0019BÂ\x0019ì,H/PCÉk\x0004"5öôÃ\x0000\x001f>\x0002*h\x0002?n\x000bI'\x0012\x0012OÃH\x000c£¦c\x001dd»@(Ý<ÏDnbJ(¦(Þ\x0011\x0018®*!Á	ô°W,«n@R2«` \x0003pP4\x0010Å \x0012®hx0|\x0004ËZVÐ\x0004~Ü\x0012£XfK$µÇÈ\x000e°\x0008E\x0010\x00125OlW\x001e@}Øv\x0004íJ\x0010ÚÚíØ&¶&ÁâFOOsÜÕ\x0011X\x0016\x0007Ë\x0003ËÂK(¼\x0006åiÊ<\x0018\x00126Å×\x0002®%N\x0018\x0001¥äY[õa@âY©cûkb¨e,¥Ö\x0000ÅPªô1\x000cRIDqq&j"J'R\x0014\x001b!Ü¬÷\x0005\x0012Hè\x000f3-\x000cïJ&<4~¨D\x0014ÅÈÔ\x0013RxÉ\x0015j\x0010~\x001c&
´á¦}]4R
 \x0008IÝXL(1\x0006,¡ÈJ(iÐU\x0012\x0007¶F(¶2\x0006.Thd\x0006\x000b\Ñy\x0006$(ht4Ddñ
PL	¥BûD(k0EHdd\x0014Ql¤æ%\x00034B9ð'¶wE(\x001d§ÈQâJ(5/\x0019 à\x0018¢=Aé8exóÌH*^rDâÖD\x0006ÐÄ\x0016!FH7Ï\x000bõ\x0003?Ö ±S\x0001$8j\x0017â\x0000Î\x0011Px	¥Fý\x0000\x0014¬
wªí"\x0014ÕA\x0019Ã´¼\x0014o¼N¼YìÀP\x001c!1\x001d1ÂKéÆë¤Eí\x0003@4\x0014e2!FX\x0007«\x0012IÉ\x0014\x0018ÓA(ò»Ëáct\x000f/Å,¯\x0013³\x0016Ä\x0008\x0001á(Q\x0014ëX6kÞkRY^'f-id!c
\x000b¡¬©2Â8ð¢³¢NÎvM
Á\x000eHC)\x0000
\x0005øX>ü¬\x001e)_©z=ª\x001bH\x0005«;D(qÀùçÃ\x0018÷>\x0007Ã÷ß×Ø´4Ç\x001eê'Sû\x0013xëÈ¢\x001cÁ·eYbYþë±Hæßåí/ j\x0016:Ì.V³«åìlùÐ;¸KhKS£\x0014\x000fì\x0013C\x0008Ü;â_ÅìoØë0{¹Áì¨ùùÑÑ*Ê\x0017¨|\x0003*è?°	\x0015l=â	Ns[\x0003*9ñÍ¸ºþÒK°\x0016\2m\x0000SÁ\x000fI}9\x0000\x000b\x000fIîì\x0014X¼Å[`±dK\x0004\§ú~À%ZÙ8vX¢%Ú`Å¶\x0003¸E²p\x0000«ãå\x0014\²À%w\ª¥v\x0005.`é¹ESà2mo1v\x0017\x0000.+ÇÇhè1fûØZqe\x001aàZHH\x000b\x000f=\x0018!¼Öj\x0007Å×²\x001e\x001a,ÑCh¥rÑ\x0000
·'«4ãI\x0016®ò\x00112ÓÌ¬fYê\x0012ßv·)F@\x0013\x0006RDjmØ	è?\x0005¥\x0016wMÝÍ.\x001eÖ2èõJ®ï\x001c:¦×Ík\x001f×NÎ^Ój\x0001`f\x0001`qO-° lÒ2°\x0000\x000c\x001aâp°º¦¤µWÝ\x000eÌÀl\x000bÅD7jF2Zgâ;×ÉZ>b¶¼JÛr\x001c6	áø nh½cë\x0001\x0007\x0019û·\x0002\x000bLµfâ²e=¶`°Óð6ëÓæbc½#h·YLJñ.\x001f*÷BBÎÿäòæ\x0001\x001eåÉM°W{\x0010q&Ç´Ôq:.K¼Eï³\x0019Þ'Ççð OÉ:GäxD\x0003\x001eµÆ\x0013£°\x0011%@¾\x0019\x0002ÁåÖ,\x0005\x000bÍàÇýÓåíí2
.;{Ù;w\x0016fB²ô\x0008]êÅ¹³ps\x0011Wy\x0003Þéüäd\x001e\x0005\x0017L =Ü;1³í2\x0003:VÊø4\x0006÷òn¶º½]^ÝÜE7\x000fßû9ËCÛ¢ í:\x0002?]·\x0000²dkÂ%`³àv¼\x001f\x001dF¬Çç\x001fà2÷.9ö\x0002ö{¥\x001a\x001f«ÙÅÿüÇ.®gíß.'\x0005,\x001aK\x00086X!\x0010^\x0001*ÃI\x0016]ÿXÌ^Î\x0016of-sC°Öq\x000eÃjq1ÚË\x0004³FSïgÀE\x0013u¹âr<.]àÒ
¸8Ì}+¼Ì´Ðàò\x0014ÀÅøx\¦Àev\x000472Çå±n¼
\x0018ÌrLÓ:\x001dÌdÁi0 .R²\x0011\x000cÆ¸|·"0\x00183\x0016×¸Îoï/?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¤1ÁË	&­x
nù¬r%Y´C°Ð/ý9\x000c÷ÃSÔ·?¤owIú\x000b¸H·7_~úÿü¯Ó/k?¶\x0010¼wl ;-4µýÔ(åxèå\x000eü£Ó\x000fG¿;+°1bõ(¶bA\x001dÀ\x0006+OkÔQ\x0014\x0008;\x0006\x001e|qläÆ[·£Üà9¥êfì¤ÄUI`«XÿØp0û«\x001b> w£Ü¦hÙ¢8£T¬íÊ|\x001fÌhãh\x001a¤\x0018^(h\x001eò;A\x0015$ZJÏ}\x0004ä7ÝÕÜûÕiSÉ7\x001fo¾{@ð·_îñn¾¹ý|³ºk·¹öB=ö9/ù}E©ù®ªo¾;}{vìo/?ã?\x001e}sz}2ß3£ÐãÄ¼J?FùUTô¢\x000bDO4JÛH§]X(\x0002\x001e\x001a\x0000ú¸øcø\x0003Dè
XHãÉ³O¡ÍB+~z\x0005eéÇ0}Ð2YËøX\x0007@Q\x0013eÃ¼äØÀ\x0000<>¨§\x001fã\x0003àn\x0001kwòÓ.~\x0001Í_`Þ[\x001a\x001a\x0000Küñ:\x0000z~üc
@YõåßLòk¨ñÐë/?~¼[	«u/[ìb\x000ci'(<Çàì\x0001õúÃïÎÖaf¶i'£j\x000f88%ªg0**@u¨Ù\x0013h5\x0018jâÿo\x0003»\x0008Ì\x0007ÊCé#?\x001f\x0008ã¬\x000fµL£À[úÑ&M¤T,ë¤dé|m²{\x0017bóIòkÑÒsOúÑ\x0006·£|{kK_:­e\x000e*èã¼\x0007·\x0016ÍâEúÑ&0P.3\x001aö4Ï¡\x000fésR\x0003 Ùya5Z©mlCnD	M\x0012Ë÷\x000cÌy\x0019_k\x0016\x0015@Ó64A5fq\x0002\x0013Í´	mØrxpô_¥\x001f-hp9ã\x001eÖà\x000e%%0Xc&æS^W£¥{oü 
cëù9Òb­fi\x001b¸8ÛZ´Ë5ýhBóÁ\x001dçïigÝàò[\x001dùùì\x0003d¿üÇÏ_n~\x0016ãóôø·ÛÞw9­¾Ó\x0003àn\x000fà¼rN¯\x000bÎÞ\]þëéÚ\x0007	ü.ò?\x00029Ør\x0019Xò^ÂäD\x000cµÜ§¶\x0017~÷\x001e0\x0002\x000fwAÎõ
¯¶éiz¹\x001c>èeß+\x000e°{L¶6>UÊ\x0014]iqìÅr¯^ø]yâÐÄ\x0013¹Ãà°HòÖ^fÉì\x0011Ö»¥nÞÁÜÑîürÚW/ü®øpdÍMä¬)\x001fI\x0015\x0010ÓcË_.nëßU\x001bþ\x0003Âïª\x000bÿñà§åÿô÷Ô\x0014zõãü¢ÃÄ98ûùOÊûËãýíçÏkß`¢JA§\¹\x0015)z=þ¸rKÍ÷Ì={ûîäýûò\x000esy~z}½
;»\x0005ÿ\x0018Øÿa\x001f~¾Ù>¿9zÿøåé§µ¨àÂr'BÌ¾'àhJsÜ\x0005U{à{ùáêw«ðò¬6ãÂMÌ$§¹ªáê§ç\x000bbðè\x0001®\x0011\x000f\x001b«IIauG/\!\x0008~\x000ePó¯×MtÙaj¦Ãì~
ú+Ï«`\x0004wÞ3ó¯\x0015MxÙ%jÆSÂ\x000cx[Û\x0007èÓ·ÏlÂË~OûìiÌå'\x0013½×å­g!rß=f<Ì¿¤§¨\x0018À±5ü&ç#}MxÙwiß¸âàÁí\x001aÜDÉÍYaglcVèeº\x000em	Y=¥1;áiþ´z¾ëQ\x000b\x001d{\x001fíx\x0002oÁÙê\x0005\x0014ßKx¥ý¡o±z\x0018ÏÄ\x001f?}®ÛOGW7?ßÞ|ùëJ>k-eÃ`¹>«ú»Hºª¨6\x000fxúþèêäíéÉYHÇÆo\x0019s7~Ãt~ü\x0011é\x000cùÍ!þ??=Ø{@ø\x0018~ $\x0002ÝÀ^ÙRcgöä\x0012]ö\x0002
Î\x00155	·©\x000bÒ\x0002&þ\x0007'°­ç\x001bQ~üA|þô¸?;\x000b.\x000fwM
xÚ&\x0017oø¹Ç6\x000eê\x0003üö\x0005.ãr«Ë³I=x\x000eMön\x000cUVÏð\x0018$-\x0010ðpYÅs6`\x000cËÑþ1`TZ«MÆ HÅ\x0017¿C=!P\x0006:vúx¡1`x">4\x0006C*\x001cÁ;]äÐ\x0003çÓ9g×dÑwaOuï\x0018¤¤TêrBÔÇ;ËûÁÏ÷T\x001e\x001b\x00036¥óÛì\x0007¸¨äT Yo¼§Yr\x0003LgXS\x0000Ö1\x0006ì×\x0012Â\x0016cÀ¤1\x0015Ê\x0018¨
7dMa\x000ck²°×áÏîã§ÿC@¦ü®ü\x0013O¿ÿ\x001f\x001f¿Ü=¬íK\x001c¥Ín§\x0011\x0001¶@öÙµÒÔöÑX3ß9\x0011\x000fÓ7\x001fÎ.æ{\x000cêG3ÍÉNÙb\x000f7¿®]\x001b!Q¥t miEÙ2QÌ·\x000cÇü°?¬Ã¼ª[Õ\x0006ç,½´\x0004«$k\x0006>B\x0015ØñùFòèþýñã¯7jz\x001f{ü|÷éÓíÏ·\x000fS#ê»õÇ½
ªm\x000c\x0012¯¹)©%wá>/øz~y}öþýéÛÓëÔúâäìdéàÿ³ýÛØ»d¬ñå×§DÝ×·O÷w«ß
E8Î¦YÂÎ\x0012ôÀêÙ$ÈùÂ¸óÓ£×§WçgðE%ÿøüOþ^||váxsóôQÌ¿ÿßÎêX5Ìm½\x001dç\x0002bvn¾\x00179\x0019ç\x0003\x00060oN®®(|ù~
íîîÑEk\x000cí¥\x0018Ð1Í°dt4¸\x001d\x000b¹Ùí°»[H\x0017¬´·\x0000Ö¤ r\x0011 ïvÓC»»tÑbO\x0000êPoKq4ûÖÚû{\x0007íînÒCE³2Ç¹B(s+\x0005ékççe¡zh)ÜÕKmrÐ0DÃ©ÙJï\x0000v^?©\x0007m÷ÔZÊ\x001cQp,Ô¢¦¼f\x0017æÛáöÐR,¬V¨\x0013\x001c¤ôî\x0015:içKx{h¹j£ÖsiV\x0014Ó¨D ã\x0016çvþ\x0008k§-±²^\x0010\x0002Þ)ÒºE½{ªräö¼\x001an\x0017âÒÓ\¿ÁeMÂ\x0008ç,.âlp-\x001f\x000fÚ[®xì¦µ%\x0016\x001e¥æFJ°.(Øì6=xYþ±V\x0014Y²
\x0015+ÛlÓ¹%W»\x0016]\x0019ò\x0013vZÑj^	zùR°
÷§\x001f?
û×Ê\x0007;zóxÿøó\x000fw·Ok/]B\x0012¨\x0007\x001c\x001a\x001b¹qzTó\x0003ð\x0012ß\_¾}
k\x0018Ùójf4("SkÆLöd­÷¤° ^ÜÊXJö\x0019}`B
ÒËuî\x0016Âüëp+$ûY\x001d\x0013©Xk\x0018uª\x00045|\x0008TÛ\x000e_Û/8-mì°´C×êh"#µÅ±V°änïÓÈnJ;"va$ýyøîÔÅÐjN\x000f\x000c\x000bZG­¥J³\x001dÒ\x0015i\x0002¿ÄÚ]¾ÙlErM{\x000f¥Ñ\x0014\x0004õ¨BÅH{ÀÃß¶²?¬¤Úµ$
§Ç¥æ	ùì±FóTbBõFåì t¬hjy\x0019±¨Ôº±y¼óÑümb~Þ?~ùtôÍíýÍÃÊn-¨%"Èg¢+¤êPiâüÕùýå÷Gß\üOÓOÎòùéWùóçÉ18.ÉÎ¯ð°½u
õÃüÝn^ëw\x0011<ãÂø¶t,Á*rùg»\x0014Å|?Nð|`n¡±\x001cHc\x0019VceÃ\x001b,ÄY«ß	Wñp\x0008á1 ê¨G§V\x0004ðk9	æÃ}àT;ÜvD¡\x001eK>\x001d\x001c¹\x0002°¸»\x0005´ù\x001aÊ>ðì\x0011·\x0018\x0011T£ät,u\x0017\x000f\x00037Ü­Jö\x0013ÆûbU*^"«\x0011\x0007¹ùçÈÆ0¸\x000fRptE\x0010¥|O\éäÎ>ÏøÞ4¬è<={ÈÔá\x0004¾æ\x000fí>nvlÑ¬%¯pwG\x0002ElAù¹\x0013â\x001eÃàïèÞcù\x000fI\x0006.#ðóÊ%à\x0014\x0002\x0019\x0006ëº#pÔ~ö¬\x001b[ÚÌ\x000bPvË<L\x0015ü$c\x0007()ÆJ?\x000cb^Æ¨\x0013Üèáþ\x001dàYbÆIo5iMfp=_qÒ	Nõø;IçS\x001cÓRQeÆíÖ'~yö\x001dnË!Ye\x0015ë}¨\x0007D°åªµ ûÐ\x0007NÚ\ãþx,Ú¼Q\x00151ù\x0010ØÉ\x0012óaNrRìÚ¢ ßÁ%Ë{âÓ+OyØd­È\x001f~}È8»TZ²v/JÏ\x0015\x001e[£{.wdó· S.þõ\x0000VÉÄoÁò^â3 #5ï\x001c\x001bÎ\x000elr¾\x000ew\x001dVÉqoÃ²¥F\x0011|ºÅó\x000bÉ«°JòxÓGT"k- Qü ÃÒ."Î«\x0001­£*YÙMT&\x001c\x001bÂò¥ùÉD\x001bY,<8­Á*o6\6ð\x0013\x0011iÈâ¸Ð45næúñãO77\x000fu¸ûÝãÃç£ï\x0001cm"ë\x0001%hbkê¬í&ýªÕÒ\x0003èÑ»Ëë£ïá?ùeÀ\x0012Fn\x0006T`s<\x000c\x0000\x0003¦o$õ}©ÕÒ{òj@~¡ï\x0000ÌªR\x000c¨IâÈ±º£onßÀWBÜ\x001d|Z±¡¸??½)§(åP-=½­æ+ñí\x000e>EÚAÃ\x0005QdþZP4o\x0000ä÷\x000e@ôÒ-\x0001r16ê\x0012\x0002ÙMk\x0001'\x0012­XI3\x0008§kjÏ¾Á2­\x0003\x000fîÇO\x000fãþ÷7\x000fwY\x0017&åf`Søa@\x0004G&Ù,Ü\x0019~rqö=üßE¨lù\x001a¡´ÁkWÂ~Ø¤z\x0019©\x001b¼4j¾sô*¨ì´B	n4jÀ&Ó³\x001c¥:ÊUPÙ\x00047BaM
£+n\x0017\x000e\x001fJ³pË^\x0005Ín#\x0014¸jÔ\x0002Á¨RÒ)
_ç\x0000jÖU[\x0005mm#T\x0014¬nà\x000f$3è98kì¼Øë*¨l`[¡bîY\x000f\x000b\x001dZëYûü4£ç\x001f8WAe£Ú
¥©6
L¥¶?è¦Åb\x0012Æ ²!m\x0002/CÐL9C/Á°%)I9ö3q´®u÷\x0005·h,¡.ÙoÔQÏÞEWQ;ÛºýXîÌk\x0019X3X\x001an ¢\x0007·\x001fÇÙÚ¨\x0014ØLM\x0007
\x001cÒTl+\x0003_ItR\x001a ¢\x0018Z#Nõ\x0011ÊhêS¤¿à|é**
µR\x0015\x0005\x0016
¶\x0005	Ëk=\zÇV;E¿\x001a©P¿?-èIíÙq_!3ÿ:¿
"[PàÑS8\x001dlqN\x0003ß¿ÖcSEa«Ö©,\x0019e¤!	éTÙy\x0015¸UT\x0014j_Vô>iáÓFqâ±\x001f\x0012[¡"+\x0007µâg\x0002\x0013ç÷ÖP±@|#U\x000eC'*lBUdqÙÙ\x000bóåx«¨`QªvË:äXYq§|2³ó/ã«¨ÐYo÷ÖÁ.\x0016
fx>éh¶"\x000ePôªU»·î4¿>àw ­*;ç_Åd°_Uû
"rCB\x0013\x0003EåÀ]àt6,Î\x0019¢"=ÙF*©ÊR÷\x001aã*á¹M¢zl©c£vw\x001dåLüÎ,hºm>\x001f[\x0005ÝÞÚÝõò÷\x001aº:UîZ³aUHØ«Ù¦\x000bz}2Fr\Aè\x001a:e¸B»È:Î\x00100RsôÈ]Ì\x0016JøÖ0i0åºÙ\x000bL#%×\x0005l(Ít|÷3óò« à­­¹_44\x0003OTE»\x0019³æ\ÞJeH\x000c\x001b|Oð\x00172T¹<\x0018Õ³¦~¼ý\x0018Ä4+ïüæèÛ§S¿ö`<Âj[ê¯\x0008æ"ò=ÂÎw\x000e;?9úæôêmêv°
¶HZõÂ\x001aÏºl
&DrdÉÁÓz>Õ\x000c[Õzaµæ§,Uz-Ãz`ÑJ¸¶m\x0007[ô®zaE¹z+8ê)æ+¸­µV\x000bV­¬åa°\x0015¦­r¬?\x000e{\x001do­\x0017EÄÚ`\x0014V/¬\x001cýQ¾bÇ\x0013ËÝ\x000e¶¼möÂq,\x000f£RF\x001a×gX£¶[\x0006E&«\x0017Ö
~eTØ´\x0012r¹}\x0017Àn¸fËûl/,vR¥5uwRB\x0005o°ÌVØV/-¾KÑ¢Åór+l]xlÝ=1÷ÂâÚª\x00189õ&jDk¬\x0013ÚË\x0002{iSÖ
\x0007X£fnXeev>\x001b®KGúi)ÁFkYV*§m\TUkCå\x0002þe\x0000÷.Ã¡GO\x0002d4w1/ßÞLË$\x0003;ÌPãÖò\x0006ã4T#ç\x0003ZÍ°\n9d¼$½`Àqæ4ç³ó\x001dD/è´ÒRp­8fX^\x0007:,¼ÿ·ÂRÜp\x0000ÖDô	r\x0018_S\x0017W<ÄxùN
Í´\x0014P\x001cñ\x000fT¹ÌHwLPBÁ»Íæ\x0003#®¥To-i\x001dÀ¾<³~¾×p3+\x001fG|ZE¡\x0010-b<\x0018®pÕÛ¡RLräª`Hï\x0002l¤Dt,d(\x001bl;\x0003´X}OÎ/Y\x0006^ëmØlq\x0014s\x0000V9viµ4t)*\x0017´\x000cæÛK¬¤}¸ñ.5KOñ1üqr\x0004ÅÞ<Ý~þþéÝÏ\x001f\x001fZ[¯åt!\x0011\x0014µ}UÚsGbX\x0019³\x0007ïÉùy\x0013{suzý>ýÓ»\x000f×ß]þîý\x001et\x000cVÑýq÷\x0007î,yÄÿóÿuòôùîÓÍÃÍÊ«p>ÈÒÎÃ+n/ä$×&87_ÇË²hG'W×gïO.Næ{¯2º\x0017St/Ø¥ Dp¥¶üNàVt/nA÷\x0015º\x001fD\x0017d\x001dØ=Ru³,\x0014-Ý^¦Mä\x0012¶ú\x001c\x001dA!i&vp4²ø6®$(ëùüÑ\x000exUÃ«1xL\x001a Úz\x0017%¥¢h\x0013Ânâ\x000fªb®b
¯äØzExß'¥ñ<ó:rn[Pëw5¼\x001b§¶ÎN\x0014¥\x001dSÞ\x00158, Ù@îcE>\x0015ÁìZð\x0001_3¼Ç?/x.QtbþªÒ\x0001\x001fêi\x000fÓ\x000e\x0007bxA/¼ÚX¶b¾\x0019B\x0007{¬Ùã {\x0014ÔÄÍ[p]\x001cÍ{A?¨×¹\x001c{BLÈS\x00113£
WqYÔÇÌñ¬âh²
\x001bHø\x0015»\x0019ó\x0008q¬\x001aVÓ©j$¿t\x001fîaß´UÿøÃÝ§çÛ\x0015ÿ4¸p(­\x0001wl9¢¢+;vóÕ?V(GÔ«Wïîo~¼MäÛ»O\x000f.n¿üeµ¼\x0013^Ú	?_¾À)cï ùKæ»ó7§É|{röþòâýÑÅéï\x0017¤@Ë Ôt\x0010j|\x0010¦¸	©¬\x0006ÁÊuÒÇùÜþAèé ôø #\x00113\x000fåC
ëÇø0bØ?\x00063\x001d\x0019\x001fC°f1ßNæã\x000bþ:ëòô\x000fÂN\x0007a\x0007aÀk \x0012BÈÉCpüèÝ|d³\x0008n:\x00047>\x0004¥H\x001cÑ{\x0013ùéÖ\x0004~\x0007óÖÍº\x0011ýðÓAø
\x0006\x00118¹Î\x001bÍZE&¾`\x000b)ý\x0008ÓA
\x0006\x0011I\x0014Øc/+ÅcàzT=_ðÛ?8\x001dCÜd\x000cä\x001byaðù'\x000fï\x0002~¾ËB÷\x0018v·tÎMV\x0013;§ÁçÌ\x001eØ\x001154Ä|æEÿ êÃzü´Æâ\x000f\x0012ÂZOz\x0007g·\x000fCô¢:­åøq-:¦åä\x000c9¬2RSb<éæS5z\x0007\x0011cµð×ñ³Nar{¾ÞkÎå1ºì
1å×>\x000cim\x000bøChùxûóÝ\x0003z¯m
Òþ
À;)4«ç\x001a©³Ç$]\x0012«?}{vëFÌ\x0005ÚVÐ¶\x001f:¢J\x0005BÈ¢\x0000M=Å2f^=¡\x0015z\x0017\x000bBh%û¡­!çÔ	+©¡\x0006oÏ\x0013õÂ¾Ú)5êGuSKz×KÔ4×rnK\x001dª¹\x000e#sí22X\x0018Ï\x0013M¯{<_ãØ\x001c«\x0003\x0013m\x0004ÚD­-åUkmÈe\x00162ÎK-·RKé«$M:±±¹2a£\x0004'lêQ'Ào6ÙR
\x001b}z±£\x000b
`\x001bÊ²ÐZÅB½\x0019´®Mµ\x001e°Õ2UìºÔ­ý/­%=«Á¿_nf¬1_¾Âv\x0003Ø\ÞëàF·rk*\x001c\x0017ÒmgB°6bm\x0006l2Y}ÄÆè00Sóºv\x001bÎµ«·£\x001bØÃ8\x0016¥3\x0015Ù>áJCù´¬fìPoÇÐ¿\x001d\x00056Jr\x0019Û\x0005îC£à?!ì\x0005íVl%*7$É÷bóE/l4\x0012\x00084jü\x0013öBGflU4é\x0011¹\x0017ÛsÂ©`üT>Ó¥Û\x0003vÀÚl\x0003YaÛ~;ÄÒlcG0Oò`ÀéÈ4c»\x001aÛ
?ìJ±\x0003.sÂ\x0005ÃØ\x000bÚ»­Ø¾:lð×~lK¯65¤E\x0012I¢^\x00087\x001foÇ®l?`µ\x0005g~Ã"Å\x001f\x0011¦\x000e³½ÝFEUaãt\x001f6\XnQ.Z±ÃE±Ø\x000c[ï"Ö¿öÏv é4Ûd\x0000µàÛX¨oÆÕÔr`KþoÎvíÿé\x0011ÿï\x0013ÛÔØæ\x001f\x0003;Ô{\x00188Ü¥é\x0003\x0006PP3Sç
cÏ×Û­Æ¾NUÏy'ð\x0007|Î{ûøðùïÿÃRon\x001e\x001eÖ\x0006±8dd%3ëÈ\x0003\x0004\x0013>¯÷öòâú4Ç£Þ\\,Ä¡[UÜj\x0008Üª¢/ºÔÊÃX\x0016À
ó[:Àc\x0005\x001eÀ¹.3hS\x001a>Zk
x}ìj\x0007×\x0015¸\x001e\x0002w\x0012\x0003ÊfFu\x000fÀ¶\x0017ÀÑôç\x0016%	<zJíQ6\x0008\x0013Ôó\x000el;¸­fÜ-@A ³\x0010I^*q}Ë6ñà§à8%\x00033.|^p\x0006¦¬EÀq>¿¿\x0003¼ñ04ã^\x0019\x000fç­\x0017ºè&n¸9cµÆãÈ\x001a·pmÈáâ`b<¦~ñ­¡Ñ\x001bZC)ª	Ç_\x0007f<ã@àJr£0'X	R/ÈÆ´ËjÆñ×\x0001ò I9\x0018N¡E^Úë3\x001dä¡&\x000fCäÂy]	ºÈÎË2·«zÎÕÐGÎ\x0005\x000fø¨Ég¤&:0çrö\x0006ÑNîê9wCsê'YÓÖXKÍ`{¶åq¾Ô¥Ü»\x001c=ÈÉa1p
Þ¢\x0013ç<ÎW¶\x0007Uã\x00017´Z\x000cÙDîL
à¹Qóé,ÍàJ>ómG[+¸ßV°\x0018¢¥)T6
æ|C£¨ê
ª\x00067¨9¦næ²ý;±ëf>_wÔ\x000e®u\x0005I\x000c\x0003SnIÑ)À\x0015\x000e«T\x0013¹âná°ô·$w5ùÈþÄ\x000etZì?BäÒñbYhiÛNnêenÆyÑ\x0008¶¦\x0014~9¥xúùÔïvr[ù·IB|ÜS÷¨`ÁIäo)>AÍü3f;¸«/nÄÝB?¹ÅFcñe±\x001bBè+OÁÃØ*gÑæõ\x00191ðZ¡ýiÕ||¥\x001c;,Lojä\x0014²¾¨ÙcöUÈä^Rs	àÞð2djhÆl"ùå'`\x0006_î;¢¼æàór\x001dä¦&7Cs\x001eók,LyqÍQxÀÕ|1|;x¨L"þÚ\x000fîTjJÉErnõ\x000bS>ÿ´ÙLnEµÌñ×\x0001rëø\x0000õÒrb[`Yn<J·$×5ùÈ2GrÅË¼\x001cýA2ç\x001b^*l	9\x0013¹\x001d!×Û<x\x0019YNÍG³85_\x001aÛN®«ë\x0010þ:@­yÎ]sÏN[hmÓN^;-vÈiqp\x001dÊ
\x0017©£\x0011p\x001b^+b^#¨ÛU&1%WvsûR²\x00033.8`\x001e%\x0015|¡¾á×>\x001dòY¼Ò¤t\x0014°\x0014ú5DÎRcjÃ0¨\x0013¿Ì9Ë\x001eÁ§A$rµóùÌ±vrYÙDüuÜà\x0016\x001eý$ó\x001e5\x001f bÃ\x0008«}\x00167ä³xïðÍ0DEJS*zªýÎ1Ñ
\x0017Ë¤6°,\x0018üSÿ\x0000¬g×EDVgúE¡Ïµá»VÏùC\x001cÃÇÇ\x0016j<\x0014ã±ã§\x0016,nèwÉ Ãc¸h\x001eEI¤ø\x0005¢S½%~±áêÑú«Õ\x0003klõ`-¯.\x001e\x0001]©c°Åó/Xéy\x0008øê\x000bÑõ\x0003\x0003\x0010"¼¦¼2ò m·x\x0016ÞZº\x0001þ¥\x001bvïÿ÷7Gïîoþ¼²£\x001aj\x0005PÍ\x0016Òæ6Á(+JÙ}BÏ·\x0010Ù%\x0000\x001c½;?ùötGþØÄ\x0018K\x0017ú±¯$åYMïÚÛ³pMZl­K^á\x000f¯ô3ào`¥ÜÜ=¬e\x0016JÒ\x000eÆ²ãé!y1rEZ\x001f
ñÀb99»8_#o¦øf\x0010_y¸\á\x000c(IônþFÝE¯)Óã¯cü°"\x001azMiÎÜßð·
?,¿zñÀ\x001fpñ¤¢û/G×_Vû\x0001+QR±º\x0017,Ö\x001f\x0002kÑ\x0006;ÿ¨jí?\x001c]_~¸:j¦¨¦\x000bUs¡\x000f®\x0004.BÔ\W?³ÚBº«ÍCR<\x0011úféí âyTn\x000bæ´ÑJÔ]bYTÑ
'¡ ÎóÚà?æK\x001b\x000b\x00055_,ÓÂºK^FV¼Nõ°
îõ\x001brî\x001b6vaP1/Þ\x0002êªMå:w,KÕ³\x0008\x0007Þ¹)±OmaÝUy!k=¬xg\x000f,Wa);Y¢F\x001dÄ|k&Öj_¾}%Jk\x0011\x001f\x001d6¬Î¬E\x000c!Î?Dµ°ÆjcÅ¾%D©µyäyåZÖ0ß\x0006¥\x0001Uî²4¹\x0012¶k
\x0004Ëk\x0000ïô\x0010\x0014÷üðþÜJXYÍ«]\x0013ë,\x0000îÎ\x0001\x0019\x0012Ã¼4I\x000blI\x000fÌ°:vÁÂtR?Mð\x001d9A ` ÁÎKc¶À\x001aÖôÁ:ÃJÔ^Å\x0012`ÜüÓëÁsË©g%×ðWSYµ\x001b*\x001c¸ýüy¥Û¥Pï?/^øo,)p\x000cHª&ùF,,\x0017tBUã\x0017§××\x000b~\x0017óë_ò\x000bî\x0003\x001fQ«ÚÕRr´~>Uª\x000fßTøf\x0014\x001fð²¸Kt\x001b\x0004¨È\x0002
ÑÎk~vòßò\x0017M\x0014äW$ÿÉ\x0011Tä?¨±ÖÆoåßÊQ~\x0007aâ·_\x000btÑ4f¾_S\x001f¿«Ö\x001b]?ASZ©:r\x00133-¹	|Ôóå¡}ü^Mù½\x001aå÷Üy\x0004ùÉhjÉ>	ðo¼þCµ~Âèú	å£2|­ÒÑùå\x001b`;5ÿatþ£æ\x001f\x0011£z´~XÒ\x0008%·Å\x0015~\x001cÆç\x001c_Àg=VÅÅÑ?ÿ2Ü/'Réðõ£ü\x0016\x001f\x0012Òõ!c}Ç·8_ÙÇ¯lÅ¯ì8¿`~Å1U­,­°PrÒ7\x0000\x001dª\x0001àSñÈ\x0000´0å\x0002ï-ufA\x000e\x001eÀ|RD\x001fÿÎÕLü&òÓì%,\x0003ÇtæÕíúèCí»ÁÓ\x000bÎYÌWÎá\x0013Íe(¨EC\x0003ÐvÛõ¯T5ýøëØ\x0000Àèù÷¾´\x001c×¥Á÷ó
Þú\x0006P»ojÔÓj'àå\x00025¨ÓÖîô\x00117æwÕþÅ_\x0007ù-Ëz ¦W)Ô\x0013(Â\x0007rÛ\x0006\x0010ê\x0015\x0014FWÒ%Ð]aø\x000bp×s¿ÐÔ®o\x0000±º?V:Å]\x0003Ð\x0002o]e\x0000\x0004[¹\x0015¹?pEoå×¢ò ð×á\x001d`i\x000b£3T>\x0000\x0007Åâ¶\x000bHPóî\x0000mø\x0002ùN\x001b0po1ì.²í\x0000då\x0003á¯\x001f r\x0017\x0006\x001c\x0000e<k§w\x0003Øö\x0014TÂ§\x0001èÑ\x001d`\x0004w"ÆP ßÁ¼ÛI9\x001e\x0014xo\x001b«¿\x001bý\x0002FÒk­w{¨á\x0000X2zA;«o\x0000¡\x001e@\x0018\x001eÀ®-IÛ9
 p\x0003\x001dç¶µ¡¦Þ\x0002fx\x000bX_¤\x001bÅÎ\x000b|\x000fpjc7Úèz\x0000zt\x0000Nñ=ÀbY.é¢\x0004o\x001eÜ8\x000cdêk°\x0019½\x0007\x0003Ê÷\x0000Kå\F²dºu\x001b{q&ÖAÄ8êGÃÕ\x0005(_dX%»qöÐ;të\x0000¬¨\x0006²¤G§Âp\x001d\x0015åó/`\x000e¼J4\x000f ÞÁvx\x0007\x0007Émç`2P¯#
@q Åêy\x0001Î\x0001Äz\x0000£~(\x000c"\x0011V¦ØZ­·Ý\x0003VW¡\x0008üup\x0000\x000f1\x0013"×\x001fÒ¯Ò¦»Ò\x0003x\x0016\x001e
Eëô\x001fÓ\x0000|)Í4\x001cË²bã\x0015$¶àxÐ´ýDoH\x0002*Q\x0016_B±?\x001dÂÆ¾\x0008òù0ÀV\x000c\x0002VS ¸¨\x000eÀqõ\x0012\x0016[}
/R2,\x0017{øCêüíxóËýÍÚ\x001er¡\x0005E£#e´káK\x0016Ø|\x0016\x0015bcãÉ»ó\x0005}#ÂÕr«e\x001fn\x0014!§$GÔ 4¸´g×_/5IoÄu\x0015®ë]'©%FD=\x000fNæE\x0001\x0017ålõ¸»GFÄåGÆf\\x000c
rFc²\x0002\x000b\x001a_¦·
ÕÜÞ¹õ©>Á\x0006*Ñ¬ÿ
w´Öíîæ`}çºK\x001cñ¸§üV\x0019dY¸Ëï&ëy£òFÛ9¹ÑP&Mn¶
à×zÝåL«qå.ÿ/Y1N\x0000ìáÕezIì[Z_fw+\_ãv/\x0007ö¿#
,ä\x000c X\x000e$`\x0005ÀóBðmÀª\x0006V½Àbç3°\x0014X£eTeý.·u[\x000fll}¬u.àhÄ±\x000c\x0019XYn\x001a©$¯\x0008³ºÖÀ[O°é`TzPÄ+	V0íBÂ~\x001b­¯Î	üµÖaØ*Ójí\x0001`Ê"é¯íh\x0004®ï]\x000eÖ³\x001fáÿÑ³»Æ	\x0001Ûå»ÕÀ\x0007#\x0004.\x000fFÀ\x001a,9é\x0001ºCö¬bK1B\x0005\x0000ë]Z~òtè\x0004ÆlÄëà¬Ô\x0005\x0000&>óÂÕ|\x0003Nï\x001et\x0013/?è¶òJìn\x0002ë_NÅ×Æ\x0004\x0006\x000eË\x000fAëM
l:E°lÑsTÔc\x0004åÝaOÙm,Ú$X]ß>xc>\x001dôX\x0006&£fì|IO\x001bp¨'8ô®\x0008Ørùq9:ï)3\x0010\x000e2Ã\x000b2ÝmÀ±²\x0011IA©\x000f8Ò5\x0000k¾
\x0019ï\x0004Þù¶VM¼FVw7üµW³\x000eztpé§#ã)ïY\x0003Ù+ëUåU&Ñ>`I\x000f5\x0011å\x0018¨oñ|.[¬	Ú\x00068ÔÀ½K\x0018ÎåH¼+Ò§ðÀ»Q¼×T+ØÞ\x0015l
ÕCE\x0014¤áÞ£1	6\x001b\x0001ÛêÎilß¥3u\x0015"Ç\x0007«N"upTF¯­\î*½\x001eØUÇ²qÇ²´^«#IQï\x0001+è¥\x00087ºÕ\x001bW/a×»±..ß4<xj6Ë\x0005sà6r$¯×°ï]Ã`z\x0003M°åU|÷´[\x0019áúÐ0½\×©îXÚx\x0003/à­x­¨v\x001cþÚ7½Q\x0014^kyÇ¥÷\x000clô6w#««C\x0003í`%èm6úPb~6°ciÝhMu,'wª\x000b\x0018¶\x0019\x0005Ò|`Ñ!Ô\x001d\x0008x9£e=p\x001dK³Á4­Àd\x0016=\x0008§9f·Tº:Æî:ìè\x0000ç×J\x0003Wz´Ær\x000fx\x0013Ëï4+h].ÈßÅ¬{ÖùêËÑÛOGßÞ>|¾]Û\x0017ÜÁq\x0005°¨\x0018¼5#É³lPöf\x000b¬?\x001c½=yôíéÅõéRgð\x001fkü8o­Ï¥`F88©sñ"\x000c:¥\x0019l\x0000·%¾ªg_
Î>>Ë§â0À×,\x001ec$
\x0007£Õ¼£Ñ\x001fwa\x0000ÄÓêü\x000e|	ÌI(É\x0008¯\x0003Ç[,ßVÁ<äMðC~ÔÛµ\x000f*µßÁ¿ÝúOß\x0003ç_×>¬Jµk/à±Q\x0016e("\x0016ó);øw°o¾ÿÂ¿\x001cWSx5\x0006/\x001c\x0015%xêÂ\x000eÿè
üuß\x0002¯§ðz\x0008^ae¬"øÈ:ÉZSÇ=\x0017¨ì7Sx3\x0006o\x0015u\x000cp\x0018QÀ\x0003\x000b~XZ\x001eÖ0i·Sx;\x0006\x000fN\x0017xÊj-\x001dá^\x0000ÞMáÝ ¼'\x000f\x0006àbµÓz\x0012óÑþ>x?÷k¾²*å8\x0006üty\x0019\x000ewl\x000fSø0\x0008Ïz\x0016\x0001@K..}\x0015
Zl\x000b\x001f§ðqÐT
ze#K&·eÙÌ×\x0012vÁï*±ª_ÿ#L½ªO©±cJ9Ã\x001a­Ò)>cSBD¦×óuÌ]ôº²ôzÐÔ{CÙ>A¢Q\x001aÚ*iÍ¶soªc\x0006W\x000eV\x001eå#=½$`a\x001bÃÃÍ?Ûà«c\x0006\x0017\x000eæÑ\x0010;Üý\x001cÃG?Ü&±	>T\x0006'Y\x001c´õ±z­ÙÔ3ü¦K^ÚÊ?À_Ç¼bX*doÂ.ÃRBÐØ\x0014>Vn%þ:\x0004CsÉÔKCMÊ\x000eÜMi)Ï­\x0007_Õ^±\x0012£øÍh­Y6
Û¶\x0011~Ï\x0017éÁdË\x0007Î\x001fÁÇ£:ÎDGEÆ\x0005nQ°Ð\x0012ªÞú\x001e\x001d¡ÇfPY\x0006\x0012_â¹ÑÔ¥OÚÔ\ºú6¿\x000eÑÃõÛJ´(Ýð5÷\x001búÁ>÷ëð­õe\x00163«2ooÖ\x0017y)J@\x000bØµ£(ª[ì´àoO®t		ØLM7°¡çy\x0000XcJeu\x000f5\x0000)pè\x0005ÖiZ\x000flJRM_\x0002\x0003Ïë·\x0002Ç)pìaMu\x0000øòD¤ÓS¸5ÊC«U½»\x0017±æ*\x0015 ÖåÈ\x000c\x0005xMÐ*à]m\x0004\x0002×¥\x0011MÀâyE\x0011çñl¨s[mº]´4\x0001»^`Ì,!5ª`Ù\x00117¥p-â]\x0005\"öÝ«¸´\x001b\x0010àFyÏµxÊ*`S­	Ó½&àj+\x0004ðrkaÙã\x0016Ö¬¨lXG\\x00196ÓmÙPX\x000cE\x0010ÔÒÈ²íì\x001aUÀ¶::l÷Ùá\x001c½y§)ö\KexM\x001cÐZ]\x000fìä\x0014ØÉ^`L7Ê¼.°;jX\x001fVÞòÙu¼!vÝØGÊE	Ö¬¸h\x000cw\x0011vîÏ*b_í:ß½ë`áæôDbs¬¨>Ð(&6\x0019¶P-âÐ½áÄ`;á<uK[¡abM9Ý*àX-âØ½Q@Ìµ\x001c@3\x0003hBë\x00155¤ë«)ýS\x001c8T,æZ9ãlY\x0014ó\x0017©6bY{ñRôî<ì*x=[mncÀs<\x001fkj%v5q¯KaÃTÊ<ÉÅ7_ÿ^S¸
Ù
Ù^d\x0013¹-
Ø\x0005V5³*òÖ[£·XÖÄ½{\x000fþÓcZÈºHv[]î\x001e«Êÿ×\x0011û¸×o3àiÒ\x0014c«+EÄ·\£¸ØÕ«Âu¯
\x000c±\x00131ÜMiÛ¶Ý\x0014ûzQøîEáwg\x001eVP¤Åz6\x0016b¾%A+²­{iã"Ï1¦ÒÆ+öxË*àXÛãØm£¢æ 0\x001cý
[äoãr¥Q\x000bq¬{¯ýXH/Ó°fùÂd}Q=¤B¾\x001aYÕGê>B°¬¦#\x0004»lpmU4ç{V5"×7\x0010Õ}\x0005±F\x0017aLt=©u¯¼0Üükb#rí\x000c©noÈ:Nmö\x0011\x001cN\x0012ÁqA\x0014)áù\x001c£6ä\x0000Tºûë^=5\x0005!kÏúäÞ\x0004VU[yõZË\x001a¹×(;ì/¬°A®P^3ðV>²®Ã\x0015º;^a\x00037?ò!î^\x000e\x000b^nl«x\x0005þÚ9Ç¥XÕG\x0005®\>ª½¼å\x001aQéUÈ®e×;Ë\x000e/ëHcÂsö¼ól/Ä\x001a\x001dÅuÈuàÍõzpN;ÌñÈÈ²Ì²céÖ¸YèM»za¸î¡eQ»Aq\x000bïX&+Ê­.Õº\x0002èî0@jn\x0011ÊAB\x0002ÝA³.P´ËÒ\x0001
È±¶Ê±Û*;U\x000e\x0012iø\x001a\x0004+"ntyÒ±Þ{±{ïùÝ)",¿\x0005©
ôV\x0016Î¨jñ×ÞU\x0011Yv5â^\x0004MÉä25bE«k£lº2Vó(Mçâ/xznÁÍç¢¶!Û:Øb»-Þq{ÚÔ³â\x0000Q\x0005\x0016§¶kÔÙW!×¡zÛ\x001d«\x000fà*{êd<ß«cÐ,I½JÑy\x0015²­¼{k{½{Øh,õ\x0014ÀköÙ(ÇHÁd@V\x001b¿m}Øîs$àk:\x0011¡Ñæ\x0013ð!«x}e.ð×^^ª©ó\x0001»ü\x0005\x0002æ&\x001b0­fØ×[Ï÷n½ Yé	\x0003)êR¯!QZt#âzMøî5\x0001ÛtCÎDÓb'c¿ÙEÄî$à\x0013o-\x0001ß´&\x0002¯aÍ\x000f"0Á»ü)½Õ¨ß\x0017l÷\x0003C°q=Ó¶ÓåþN«¬Éd÷*ö\x001e\x0018\x0012r~N×Â±21¾«¯Ô®ûJ¢¥+\x0002v¬L\x0004ÿ\x000e»ìê+µë¾R )\x0005\x00009ö\x001c\x000bb«W\x001c§cMÜ\x001b\x000bp§æÆ\x0011¹\x0005CB\x000eÜV-.´6\x0010ÊZ8Óm-`Y°u\x0013ËaY°Ê|Ü*kÁÕ!8×\x001dCdê
\x0011\x0004§6\x00032û\x0015>ú6Õºð²w]D'(6ë}ðCVÚx\x0014Ø\x0004\x0018{ÊMS¹\x001e`-Áwãö\x000fVbN@)ò»'­n{±ãØ;ÇZZMm¦½ÏGv¥ñ¼ùôVÑÖÈ¶\x001b\x0019Ì\x0005\x0005QcÀJ×¼W5y[\x001cª;5þÚ¬¤,Í\x00181jh¨`UsK·YNöSýYJ&«õg[r\x0002°pÒ[{Ê'¾¤¶le5¶¼©\x0003¯nz¡\x0015ç\x0019ÂÕó"£æç_»abä\x001fxÆüCon¤åjÈ9ø_'×ô\x000cXôTÏ3ü{çYRé\x0003§ ¤\x0013Ç¹ëÂ¯iV²\x0016úgÐ½\x0013ý¿\x0006
{ç«­h+Z·D¹¤¥"\x001fµæ:To¸»7áä7:¼³/z\x0002Àz÷óÇÏw>Ýþ|ûðùèþþó¿.þþß8OGo>ÞüüË§Õ±Eî¥\x001dôÜ\x001f)pV8ÊÌîóËë³÷ïOß^\\x001f\x001f]^âÞ\x001f½ùîäí»÷G¤¦#RÛÈiI\x0018¹áÐ#¾\x0002å\x00110ë¥\x000cHOG¤7\x001c\x0011·d\x0011In\x0011°F4oò\x0007Gd¦#2ÛÈ°mÉ[§¶aá2·H18";\x001dÝnD;QGtæIß\x0017¡0'æï\x001f#rÓ\x0011¹ÍFd£ga.\x000c'\x001a\x001aQ`%1'ç\x001fv\x0006Gä§#òÛ\x0008\x0015*ÉÖa\x0017\x001dz)æNXøf\x000fÁ\x0011éÂ«»SF¸Óõ\x0006V\x001d«¢Ûh^ê\x001bÅéâ«ÎRx'z\x001fé\x001e\x000f«Æµ
óI\x001e}#\x00126Ë\x0011M\x0012\x0007QÈNT\x001e_ðð°Ò5à¿à=\x0008Ç\x0011'7]
Íö ,X8.Ã+ÞÁÅÅÄAx=	Á#¶\x0017cØÊ²@cý\x001f2µ¢\x00048h\x001bQz²Ãàd£ñåÉx\x0015\x0005l\x0011#Ë×Ã\x0019sP\x000fd\x0015v\x000c\x0015v\x000cCØ2Æ¬¸\x001dÈ\x001eÁ\x00157Ù>¬°\x0006[j¶ñ×!l0£9a\x001a°\x0005õb\x0012ÑSmuJ£Þ\x0004Ûê
Ûê1l|¦mHýCÄ¢O\x001cä|/&lWíHüu\x0008\x001b¯ÎYM\x0008Mo¼\x0018$,d¾óU\x0013vmHÔ !AeÚ\x0014AFlG\x0005ø0ÛÅ\x001a&Pïºµ'ê Ç¨Q6 «°Á\x0014E¡çã\x0014mÔõÊ\x000e+\x001bJjZÙ\x001c\x0012\x0012Ñ±Ø}X\x0008U´aÛ\x001aÛ\x000eZíó]¬6?ðÃÕ>(þµ\x000e;ÔØV\x001bnúé¥Á`Ý0õ¤mxe/d04aÇzCÆÑ
©ó\x000b±
©!v`ìùà}\x000b¶\x0016Õ"IR\x000fC;Òdf\x001d\x0005oGÅ+ä°pÍ:äP#/\x0010µ\x0010\x0011t]Çæóq!\x001aÞhûªh\x0016Ù?üÓÐyã¹A\x0018lÅã`2½Åq=,É·L/\x0012½PÅ\x0006¤Y\x0002ù¯oîï\x001e×vúp>PÊd@#Éfujd<ôöðúôêüìrAowE÷H<)ºo$\x0006_ª·\x0014¬\x000f\x000e¹YdV©ËÎFÄ®"vÄ^\x0004®oPFp;âC«kw\x0017\x0003$ôým]\x0015Þýô»IE/Ø
Õ\6\x0001Fû4\x0001NÑÒîuìXïÂ*òsC<\x0018·\x0016ÙTs\Z\x0018µ#\x001bÏzz\x0012¯í`Í\x000fØpk<¢³\x0016y÷R'/Èz7Ë¨\x001e)\x0004TÖ:øª³\x0016ÙWÖbZrÖ:Ëuÿ¤\x0007ÔÖ\x0011\x0011\ÊÞW"«ÚÀ©~\x000bçÉEÂY.ÒaA\x0019¶\x0017êà»ÈZd["¶û\x0018qEVªî4åX+Þ~rØÄ©)v=åà\x000f¯P~ÿä/·ð_Ã@ÙÓýí'ÿöæËýýú2qKq\x0000Ë·ÈI¸`Ê\x00118;Ý'ß^\x0000þïN®ÎOßã0¾=ùp~¾ðF£Ø­\x0015\x001c\x0005.ÁQ\x0018Q¶&Ê\x0002Ó ãAè8û\x0001ú\x0007Q}
=þ)p\x0010$E\x0002>\x0008IÕÃ(¨»mÒpÛ|\x0014®ú\x0014nüSh_Faí\x001c{\x0012pÓ¾HÎoîQj\x0014aQ \x0006}\x000ba©EYéüÿS÷nIväH~÷Vr\x0003\x0006Ç\x001dVOIV6m¼dÔ/cYU©jJUä\x000c/-©´
í@zÿv0;ÑJ>wÀ\x001d\x00118d\x0013\x0001£î1\x001bMÔtÍÏ\x0011¸8\x001cî×pF©ß\x0008ß\x0018á'|
àÌ	HA¼\x0002kD\x0000ü¶¯ØmDj¾Dð%jósÊÚ^kcÕÁÜÎí·¢ù\x0014iÂ§ÒS0RÜ³\x001aóuUøÍQ¯\x0015°\x0014ääÃ
r©^[±Åäc¸mg¾Û¥_6Z¸A]·Ù]NÜ4iÄÅín\x0015ýV¤Ö4Á
K¹gÙ\x000c\x0007hKIFò1ôvcÍn3\x0004Öl\x0006%°\x000eaä\x0008¦¶¦§P\x0018¡æoS+Ýl°4ÐóK¼4(FÆf\x0004é¥p&ôÑok­°Û:]Åª½ô5ÔUíÙlw>í7Â·FLØluu¤pÓãb
Í4Çd¦Þ°\x0014\x0007\x0015Ï\O0ÃÖÍ\x0016jQ¡Jo­Î´uí7£Ý¦ÂmJ\x001bÙlÁ\kªÄ\x0019·\x001b¤ôZ¡U³¼éç¸\x0015©J¶Úª
·È]\x0002l?8t\x0001ÍÒÈeV3>FX"EFg%¡¶Å¡»ÍÐÍM~Aý\x000cø¾§ "5ûª:ó­­\x0015\x0013Ü\x0010*èáAQRÞ§\ÕFÛ\x0019ÝfØfÊ¡&|\x000cIv&á+iJbåäÛö[Ñ®\x000c;¾2(n`yJY_Ý\x0010èÒaºk«]»2Ü\x0011\x000cÝ¹\x0019ù5&¡|\x000cjQ<ÝÔ1~hü?1£u
õ\x0004§PÇªl¤ù µ\x000cÀ ÞNHë·¢Ý§üø>¥ä>F\x000bkË·p²2`;\x001f£ÛÐÜ3èç°\x0015)qv \x0019@MÛ²\x0019K\x001dÉüK\x000eí·\x0008\x0013¾EZäÂÐA\x0017#LUõôó­í·3¾©"^WoJ')Û°Û%ð½f\x0018Õ|ôsÆádJ\o\x0016õh³-®Òm\x0006Æ\x000cJª\x001c5\x0003Ï;nû7\x0000PyG ÿ5Lk`^*j­Ý\x000c»èü|\x0017Ý´áTEp³0ôä¶;\x0017t[ÑFuÌ¨\x000eXRIöÜ15©«¥aþ¡a|;§ü9¥ª¢\x001duæa¤Î:åv7ÍX4RËË\x0012_­°NÉ\x000c¶b~<Ä´¯\x0019fÂs\x0006u#wlö¢hM2µU\x0010qºnRãÚÒÏa3á$©l\x00067ÎÐªÊªiíÕkUM¤0K\x000f¡D4\x0014ò¸Õ®º;éLnq¿\x0019±5c?ER¼Ûâ\x001d¼äth¨ê«gÒ_»­öcÀøÇÒÚ¼¨Ò9ytÕJÉ:£ÅÒmiV8ý\x001c7ÃTé\x0010\x0006,fdõ\x0002þqú
·íÃð0\x0003E\x0002®xNÅ¢\x0015ó\x0002¬o"	ôsØ
(Z+jk¥T\x0003\x000f\x0012\x0011rn[å·ÛöÔ°\x0013N
\x0008F\x0006i,q\x0014\x001d|\x0010Í\x001f7?âéTó5èçø>J$\x0001\x0017x¼V²OyÑÖ=#îÙm\x00054ñ\x0010ú9ü1(ÅHÄÚ\x0008P\x0013ÁÏ8ß\x0011qºñmsþô¨\x00156r¿¹,¾Ã9S`\x0008¢ÁüK¸Ó¾5cÂÊp]ô,Cgy}Ë\x0011ívEk·\x0015¦RfÂ²\x0003"\x0001Ûú1ðR[5½¾\x0019º5c<@¥Z%\x000f\x000fÍ\x0008ò¢\x0001ºÊ\x0018ªí\x0012n3lû5ì\x0005®8'\x0001w[\x0004\x0011pJNp·Ýªß\x000c×1Á¢»,J'8ë´=¦ÇüÊµ+ÜMXáÆÉv\x001b¢\x0017ám\x0000.$æß^©aÚÚ\x000c?îOqï;Ñgã2
ü¿$k\x0003¾Á\x0011Þ>»	\x000fáT\x001d£E³-És\x001fT	´sÕÝf´lnB*\x001b>eZ\x0004»xin
íÂ³­ðíC¸ð\x0010N¹\x00086T¥4~Q\x0012+\x000c~~V¡ØZ1~{\x0005>2|ò×çöò%`[£¾Û6§ÐOÈ)$\x0007Ý°\x0019Ô¥Í¨ºõþL~3tkÆ\x0003\)\x0016C
A[i×¡|½ÖÎÌ÷¶ñméçð^>Tâ\x000fÄmF)ÁÌ\x000f¢ûö\x0019ÜOx\x0006W¡Æ
Ò\x0012DWÒ\x001e(ípº\x0019m&ÉFí¬Yñ<Z¡\x0002\x0019ùj9ÛÔ1á\x0000OÒ\x001e7[¸\x000e~wQÒtqúÉ¶²!{ymÈ×\x0008²áæ}Íø\x0006k#¶;U±S\x0019~\x000cð¶ªä(x£Â¿4Ú0º\x0010FW.²p\x0001\x001e\x001bK~\x0014@=5æ_ûB\x001bÖ	\x0013Â:ÊUéaïå
©bFÜ\x0012í6£õ¦Â\x0004o*w"æAÙ`·ÛT]\x0011=}N\x0005ÝÌ)ú9lµ,ÂîéI¼è.¥$q\x001d\x001f¶«%»­h#"aBDÎ¾ÈßÂK©IîæT¾ï ö\x0004\x000f3NðZº\x001a¨åUyy-©\x0008åcøù\x0019`¡=úÂ£OCÝ¦T þóÙ\x000c_÷©ÜÚg²\x0019íÑ\x0017f\x001c} J	h\x0006p>\x001eõgCºóL6#æ\x001d<'ÃAý\x001f%Xè/wWL`çÖ¥m­¯n+ÜImâðÇ×¤"ãGµæ§WH¬¡\x0005.lwë¶¢}_ãïK¸\x0006È«;R½Ì'8Ä(}Î©é÷¾¤)E?GÍIR+J²Md«\x0015Ówr'5\x0013fö\x0012
±VÞ!\x001aQ4·ÉO?3RhN>ú9l«ÂìÖGvm©´R>\x0006LÍÇ\x001bZ[¿¤Æ_f:µ±&¾¡Ø§-vÔÜ
üF³W8Ô³çßãkC_\x0003°\x001d\x0015!C ÖNO¹Íõ+\x0019vø\x000c\x0007êÁÂ®ñþ\x001aÊ~Ka\x001e¶CoË«ôÚ\x0001­w\x000fÛQ®{Ù\x000ePüT\x0006è8³/B\x000eã7\x0008Q­¦$LE\x001a¾»kÃýD VñæX1Gªæg­âõ{Q®ûøOã\x000f±uÛò*Ø\x0000\x0018y4óf~¡Jþô» \x001f1á³ü¿¨tÇ»À\x0017\x000clÊ$ó\ú\x0010\x0002é±YdÖJÈg~6®ûÒ\x001a7Ç\x001apZZðDtè¼@É5=êù\x000b´d~9]2¿ÌxÙ4\x001c7Á\x001b\x0016GÛA\x0004Y!7#ÿ\x0006ÜZr?#¨(jü&¦\x0006Üåº~F[q üýtQ	üÕoëêà©ól^ýÒP[Ã7x\x0005	æ\x000bk(2cõ\x0007Ï²¿9²¼"HXKÍ¡Yöóé,ûyFz	§,á\x0001)qF\x001aM±3ïï.ä#f¹lQwOüîO>Ü¿Cò»Ï{;-Ñ\x0003s*Â£.på5\x001f£¬öÛ«üÉÝÍ\x000bD½{ssÕG.P\x0006h\x000f(®b[=^\x0003n5.F&MÛ§Þ\x0011R×º\x001eRj¢\x0014\x000b©à55/-5@º\x0012 
tÑîúøP^"üüõßèqt·Aön¾~\x000eT\x001fF¥|Ó¨IQ[Ì\x001a¹o5S&*vA%E}mX\PfTöh\x0010uÛm>ê[TßDv8hS[øÙ\x0010¡ÃfTâ\x0008jjQS\x000fª\x000f%aÌª¨-_F¬$\x0006kãvã \x0003¨¡YU¹aÃqTçeT£Ò¼§"*ë·Ó-\x000eÆvUÅ®Ueà%C	[++ÊyQÚ©\x0017m)Â¤\x001dVË!E©IIGtû)ò\x0000ªm¾=ýìAuER¾½ÈÚY<Q\x00055Àiªm;ª¶oTÕµO<ª\x001e\x001fÊ¨r\x000c\x000cGu»¶ö\x0000ªoGÕ÷­(#Êÿ\x0011/#¥Û\x0011.)#s5nÇ ¦\x0016µoÂ¡dRE©%ÔqC\x0008"1¨¡qSèg\x000f©«¤FÜ\x0014+\x000fNHº-\x0003{t)mÏ¤TÚÞAªJ\x000e¢R'?\x0019T\x0016´6mßª ¶*v-*t©\x0002\x001fSÆ×ê8Î¨ÛªûQMëøÓÏ\x000eT9£¬\x0015'ÅFî-ÿÉm#ºåÔ=Ab?ÅW\x0003§[}Z7c2µQ\x001bú.R[ç©ãI\x001a8Zs¾|j9»ö¨7=æ,óµ|üÄÓÛ¤\x000e êvHu×\x0000D!ÅÁ-µe4M\x0019Ôl'\x0019\x001e\x00005Í\x001eE?;@\x0013ÔYJ\x0017@¥ÚB;À\x0004¯Ï\x0018×¢vmüÉW
\x001aTÃA¾½òí]»ð]×Â/\x000e\x0014q&\x0000n\x0013`©\x0017
£n?¦\x001c!5-i\x001fMÍ¾\ù"¹R\x0019Ô1Åi04¶¤]çSJ¤IWH%|Xvûê¶kã\x000f úvEù\x0015-o´øùUuP\x001c·µ@ÒíÐà\x0001ÒU/{"¥Çã¤À%îD\x001a¹Ô\x0001wÑ Ûß\x0016Û9ÚºR¦Ë"ÔX¶þD^_`T¹J¹0Ã¢÷5jêñOv%¢J¨KÄh\x001f©\x001a¶37 ¶\x0007jê9PEÚPC\x0000¶nþaFt®æëà$tª±\x0015Õ$.:§e/s5©)¨¶Eí«E¬8£ZVÀA8K3âh\x0016BKÚµ\x0001°Ü5\x0006M9Wé4#f[ÊvùSÉ¸R>j©eÍ5¯)Ç\x001amÖ«ízÅ\x0003¤æ$Þßu¦ZsÍ{ªË¹ÏÔs.
üÍ µßh:H5ñdÔ 5÷´éË \x0011!<Ú>Mt½M$JPáQ
P÷T*¨gÚF\x001f@uíLu]3V\x0012oTÔq\x001742µ~ûó\x0000i\x001bE·=Qt'³øT´öÊFå#\x000b`Ð¢p¦ÚÖ§²}>S´=eÔ¤ù\x0012\x0007UÞ&¼ñùÛèíN%ïø>\x0005J-§2òùív¦á\x0001ÔØD'égÏ \x0006æ\x0014ÙjëbÅ\x000c3¾}j\x0017TêZP47¡B¨®¿w3\x0002\x0014®
M¹®ÐT
\x0014 ¼øâNy©Ù9£Ày³u¦\3\x0015XÅ\x00009©z99ÖçÃ¶.ó\x0001PÝ\ûrÿoÏ*\x0008j¼»$¾´Ûu\x0007PÛèëNPî½\x0011TÏN¸1+9M£j\x001b·/×\x0015ö¡ò4õ%EèÙ}i<«&ÜûoGÕ÷ªæ\x001fà\x001dU¨^±¼
z»&q?ªoÝ~ßçö{WÄR\x0011z²;%ýâqT·5\x000fjÓGþÔ5¸2\x000fðTu²\x000fp\x0016
zø^YÕdûÜà\x001f(ÛçÙûOo?~|øýáÝ§«_>_ýéþÝÛ¿¾ßÛS\x00128ñYÌ\x0015\rÏ\x001c\x0007Ï^¾~úêÕíóÛ\x0017¯¯¾sõ§\x0017O|¹Ý[¯\x001a ×\x0006èQ\x0003@ZÆSÎMÍ\x001d\x000bkiÍvò{¯\x0001fm\x00195Ú\x000f@|"!©Æl»½üvÍo?¬}\x0012Þ.Y"ilìvá|/½[Ó»Qú(~5º{\x0004é\x0013¶Û\x0011ô\x001aà×\x0006øa\x0003(çZ¤[*,E\x0013aû©¹×°6 \x000c\x001a ¨Èð\x000edEÜ[Hÿí¾?®ùãè\x0007\x0008©V­8'-\x0014Àd =¯Ì6 ­
H£\x001fÀ(ª\x0018åx	@¢ªÜò\x0001üv¥ÓªxXÎ05j\x00015¢Jµà¦\x001cb¼Tjù\x0006´ðð)Ì²[ÆÔ\n\x0010Ñ\x000e¶âzé\x0013\x0018F`(6
¨â
\x0010\x0016\x000b¶o@½\x00164G0Áä%y\x0002Ñ{C?FªO(c¶\x0001Í\x0019\x000c£°.Í[J\x0005 \x0013/Ââ\x0005m×*÷ZÐÃ0z\x0010ÓÍ9ò.jë&${í¹^þæ\x0018ÑsXQ 
ðUÓ!Eí¤xq[sµ×æ\x001cÑX[i½®"ÉÒ2X\x0010¶k\x0017z-hNb\x0018=5:@¡d\x0016Ò¢\/®Ð\x0004Ñ^\x0003\x0018bç©aN9ýµgáTÝi¿×inb=|\x0014ã]U\x000b\x0002D
lu&¶\x0015Ò{-hÎb=z\x0016«h¥\x0000\x0016äî?:ûF Û\x001bñøXI+Þ¿¤ÎUñ;$\x001eÇÛ52½\x00064Ç±\x001e¾\x0012Sp×ñr\x0001\x0004¶Àéí¨¯\x0005Íy¬/Å&pwv\\x0006
JX\x0005Ä%òfú$jÎc=|1Æ#½R¼\x0003×¸Jö\x0019\x000e¶åz-hNd=|36¢2e\x0003Ô±H¢\x0001Û*S½\x00064\x0007²\x001e¾\x0019§%6\x0001\x0015`³\x000c3\x001fgÛo½\x00064ç±\x001e=UTr5¶èVsï\x0012ü\x0002ºz\x0014Ów¢æ@ÖÃ\x0007r°U°\x0005=
n"ëYø\x001blWñtZ`\x0003Ù\x001fÈ¾®c\x0000~F\x000b|EÛÕ}½\x00164\x0007²\x0019¾\x001c/\x001dp(¨,P?Àô»¥iNc3ã4æÃ8TÝ|<åfs¦ßéA\x0003\x0014þ\x001fhëñ\x000fôBp÷ù¸\x001f¿ÿíýï?½}ø°4÷ìAZzø¥õßn°r÷æ\x001f¿|öòù£§·w¡õ\x001aZ÷CS\x0003PéN\x0007Ò_Ö¢|rÛ×°ãÌfÍlú)¯Û
*\x0015êqóÞ\¢ÇíÙö3ë ]-p\x001epÝ\x0018úe¢\x0001Ü¶£\x001cÚ­¡ÝÀÖ×ÀÍ´¼\x0015ßÞ¥:£ívùèqh¿ö\x0003³#Ö¦S.¿ç\x0006Ç;H2ÛyåÇ¡Ã\x001a:tC[R
â½ÃiiàjH3s ã9\x000e-Cé\x0008iµx^I\x0010*éíHþqè´N\x0003ëÐÔÎÁHÓ\x0006_µ\x0016Ó¶Ùaæ¥QQ>XTÿì°þº,ÃH\x00023åPÏ¥QE\x001fÇLÜ¤¡=
ûCkháPù)ßJ(¶ãßæíÒÐ0p\x001cB;Dò4B©GË¼9
Íy\x0008\x0003\x0007"¯ó<©U=Äµ²õ\x0014ßôúS7'"\x000c\x001cÔýS\\x000fÇ)+8ÖP}MOï8ts"ÂÀ¨\x0015Å\x0019Ë(\x001a\x0008-k\x0011wïÍ éqêæH3±öÔ¢]¯d²áVj÷ÞíìÀÃÔº¡Ö\x0003ÔªæªPzçÅ¨Dø:åÎIÔ¦!f`Ð±è«ÿÁ ôNMõ?æÍ\x0010Óµ\x0019\x0019k#÷Þä(¹:AìD÷Ô6CmGüÓÀ!«'¤\x0013\x0007\x0004d~íVÇ¡¶ý#mS\x0012õQ*,<ÐÒW&\x001ek/\x0002c7Ä¾Iõ0Oõ\Ô\x00137k×\x000cµ\x001b\x0019j\â¡Ø¹h\x0016\x000fuÞR\x000cíU`ä.`®\x0015/E/`\x001a\x001a¶»¼\x001d§n.\x0003¡ÿ6`£´ïÈu\x000c]Ûw$Êï\x0005¡N\x0003C\x001d%æ\x0017áÉZ-\x0003ñL	Úqèf¤ÓÀHã	..\x0008RsÓUW3¨bÚN=J
êä\x000e3p	µi\x0010\x0015)ó%Æ9\x0011ùLÛÚ\x0019©¡¹-ÒÏ~j[&'%ÝñXSó.\x0004 ÛÁÖ\x0003í¨\x0010Ç\x0018ä±ò(\x001bãvéajÓLlúÙMþRäVe¶dlS[Tûyë\x0011l{g´ýF["6\x0019b{ZK\x0013è· \x001f§ng¶\x001dÙäòÌvn½\x0005»ªîÚ4o\x001bíM&\x000eé\x0006¤/_4Jú\x0013+ÇBÔè\x001e~Ñæiþ6\x001eÿåá÷·ïHçô·û«\x001f\x001e>½ýôðO?¼ÿÛn	}È\x000cùq&Õö1\x0011¸¤\x0008èï[øÿxûüé\x000b\x0012:}vsõÃíë§¯o¯\x001eß½üóª
±Ã4v	và5ãädin\x0005 kÊUÑ~;\x0016wì wvü{È
Â&éÇfÔ¯\x00117'S¿\x0015¶\x001bYAÒn£VÞ\x000f{\x0004\x000e´t
¢ù\x0002î\x001cx¿\x001d±±#Î°\x0003=dØT;\x001aø(³êL\x001aH¿\x001d©±#Í°Ú1\x00143tcÉf8yÃD¯xóÚ1`\x00064fÀ\x000c3kx:gù\x001cr¿vaÛ÷é¶\x0003 Ù¬èçy¥ª!¤!óJú¯¤mo¨ß\x000eÛ|\x000fú9n¥\x0010úD\x0019Öó¥ÚjÈ¶¢c·!º¦édCèç°!ZKð
)/_d'',\x001bâÍv¢~C\óEèç¸!Æ_ó"å¢\x001d.-v|®ÛcPÏ8\x0007\x0003Î,à¶vÊpQ.ÔòQðg\x0004òû
Y´²!¤Í4lÈÒ£ÈÕ\x0002M<\x0000%¡ÖÛmÿ°Û¾`v°(>3l\x0008yXÜJBô©Z\x0014;¾ÁÞk g¶¢£vxô×¥+\òôLEB]"¡\x000eC¢1mª	þajrwÿÿóûÏ{ï\x001a{\x0013wI$\x001d\x0008ÏMåS}+¶nHw7øÃË7gn\x001aÂëÖ¼®\x0017¯ú Y\x0004Nºd£{(i\x00046^ºî\x0006\x000ekàÐ
\[XÈt~Òe¤g\x0001§5pê\x0005¦®ð\x001cP¶µ%R
\x0018&³ßxwy'ÞÕ;üA`·\ëGz[GØ-Ù0öR\x0008|7q³æ {Ñ9_ç\x0004énq"²
õäb$y7q³ê {ÙÙ$\x0019Ô±0#*\x001cgíkËQâfÙA÷º£ãß(ñ\x0006ÌO\x000c ÷^º¿Ï\x0002n\x001dt¯;«ê4\x0006¼pc%-E\x001aÔzØhu¦s½y=\x0001?RÏ¿Ü¿{÷ðq'7©0Å|úEíÍµ:½â\x001fj}Fm¡\x001e~¯¨ÇÍïo^¼¸}u\x001e\x001az\x0018Ã\x0007*_ÈìAJåéùÚ3¼Ý%}ð\x001aÖð\x001aFáE«#jüGÍ%\x001c\x0014¡\x001aÐË¥Cø:\x000eáÛ0ï$g\x0003ñ\x0004ubÂùtÞ53ÇÎ\x001c<wÀðä1Ò+4)ö¨ùÖåPÎ!þ`ÖüÁ\x000còP3\x0011ßqº.ºW\x001cßDüË·cô¶¡·£ô÷wÜv,ë@RxÍÉ¾³\x0010ÖÇ¹Fç>U¦ºmò½:ú:üFÏ=\x0000ÍøÓÏ1\x0003(·-\x0015\x0003Jp6Àr\x0012P¹DL5@·\x0006èA\x0003b
×ü\x0001Ð	ãHlÔ¬xMA¯øM3èç\x0018?½zò\x00026ëxðº¡e\x0005¨íêì>\x0003\x0016¡ñl\x0000åÃ\x000c\x0019ÛáÓKö\x0018\x00049|éxÌZþ4È/dÈ\x000fÚÛóD5`ò\x0016
í\x0016
£{(5y%«¹ÜC \x0004¾Ða6y\x0006v	Ñ%7jÇKJÙx\x0006yq`û®ÚÇ¿<¤dþæ%¥\x001fàÈM;Sd¡\x0017ü¬\__T&\x001bÐ:ÏiÐ\x0007EÝE\x000cð\x001c®§ \x000c\x001bàç.\x0001­/@?\x0007
pEÿ\x000cð$]\x000c0õ\x000bØ¹×\x0017­RkÀè&¤%ø\x0006\x0004®\x0014 Ý2æ\x001ec\x001aÚ/\x0000£_@³X&\x0019°\x0002¦6®=ÓÁ±Ó;Øà%,D/\x0006hüGÞE}¬·0·¬ÖgiÎá\x001cz\x0019ú\x0002*\x0016òÒ:\x001d L!·­U|Ô\x0000§\x001ae\x0002úCV&XbðøO»z~ÿë»·;ëiM2þZ\x0017©e0Ú¬«*~Ç\x0012FúÛ?_=¿yòâé¹rÚ¿¼²\x0011~ûÈÖ\x000fAô©¹v,\x0012¬Îpþ\x001dò\x001dï9ø}ÃïÇøñ¾N¯i2üÒ:\x0004´\x0016þm­¬NþØðÇÁñWêñÑ°/ÙÝq\x0006\x001fÂ_²c\x0008¿ÍéÃ,ß\x0012\x0007Q_fÙîÒ¯\x001b|=\x0001U}T+ÒðGÑÈÝ®eíã\x000fÍæ\x0013\x00067Ú\x000c'½Çô{Á\x000fÛZ}}ø±=qpöPO²à\x000b¿­-lâK$òïy»<ÄßL88}b¬³ø=w×K~òÚ]Þó3½\x001d¤\x000fÀ\x001d"ÞÖ\x0006¶!Êâ
ÛÂLüÍÖ\x001fG·~r\x0017?-Ý"eòÄ=)ð?\x000eîü¹u`Zð¥ ^ø'/ÞÔ,Þ4ºxô?ÎüÒ[0¤Tùç.^fú\x0000Î\x001fÃY¤æè¤5â9ÄÉ\x000fÆs£Cü!9îè
@2wÒÒ]zÑEµÝ5¯ÓØ\x001a0¸\x0002È\x0000ÃÛ'= 96@ZUDØÖ\x0002:h\x0000	ëï¶ôW zyÞ}¸zòðîßþ÷_wæÜhÊev%rB\x001aÑ Õz¶¾^l_{ókéíÕÛ\x0017·?ë\x0007P)CÀ\x0001:]i\x0002SnûÖP}²ËívµÀ¾\x0001ö½ÀH©J`Á¨ª×A÷u¹Ö^P7Ø
\x001c\x0011½#lcñãË\x0010%\x0017ý×Ún_C\x000eñ6k^úÙ9Âxñ\x00128è%	æÈ\x000bÐ¼ýÀ©\x0005N½ÀÆrÞJ¤Î\x0004\x001b[\x0019\x0015b}AÃe7ñÿkYïabkj8ðøº${ÞV\x0001?\x001bÚ\x0019\x0011ºgwõIVzÛi\x001f%\x0010£Ï×ýìÇõ-nï\x0016Ay´¥D\x0006·@ûqÞ"Ì²EL\x000e!´À½§E±s¨%\x0000èÆã»ín\x001f\x0002^ÅH	XWaÃ#l<§ÃGC¢\x000be
X/Ô¤ï\x0007N-p÷\x0016A9âË³v©Â)¡d
Ãv8â\x0018±nXw\x000f1)\x000fy\x001ebuÍz!YWÃ·³Û1îÞ=pÿk:é|\x001dcW=	;gÙ¡KÒ\x0000Ûþ!N%¥\x0014·$	AZçZã9À¾\x0005öÝÀè@\x0004\x0019áª\x0014\x001b«É%ÛíP\x000f\x0012CKÜëüx#¸³9*\x001fÍc\1ÌöSôA`Ó\x0002÷\x001eu^±.AÔ\x0010¯eðõÝðBVô~^×òöz\x0012>æNóe$ÊG³ÍÛRò\x0007}KÜ}:ÿ»MâU\x0003r"v`Ù¿4J2ZpcuáÃ¤1íV\x001c»·â¯Ya\x00165T"¦}ÄAk¹%ÀYOh¿ª.üöcÙA`×\x0002÷.<¼qÒm9O
mé­;\x0013Çzz\RL¨Ä?ßÿrÿñÓmâØ\x0012Çî!\x000e%¦^\x0012CKëWVx/¤÷ï\x001ech'\x0005tO
çY¸$¢»#r³ÉXqäÕ¬il[bÛMlÒµ¬ó cäÑüÌóK»}Kì»ñ**g*NLìå6
Ûéz\x0007CKÜ{[
\x0016$¹G;[g<ÍnûCÚøvåùî'!A\x0017¤×K2®âÎYu\x0016ÍB÷Î&zRQZz¼l\x0013°­Ìp×éÆ¡pº×¡HäºO-îÊ[¡¡NL\x000cl`Î|í\x000cÝ3TeU¨7%ö±5E?ÎÙ%\x000bM×Ø\x0012Ú¦¿tró»`eFÑ­qÕ\x000fuHëSlò,º¹|)ð¢Ò\x001a®\x0011·Y;rÿü)\x000bê4\x001e\x0006ý©ÓÉÀ
CÂ\x0016I*òb´âyÂhÅrýÏ¢·£Kc»÷?eâÇ\x001fîßí-ºJSÅ\x0006ò&ãyë0¸	br0`÷å×øñÝÍ3©Z\x0002\x001c\x001bàØ	\x001cR®ÑÈÀ$Âï
±æÍÎètfJ\x001f"\x0006ß\x000c1øÞ1\x000e$~\x001d\x0015h¨EJ¡x\x00186ÁYÄ¡%\x000eÝÄ»\x0006$z½\x0001AfM4cÕvÏ¿È¡\x0016ù\x001d²\x0013\x0019¸\x0004\x000c¼S2ÊéLGCÈZµ3Yu#[Ë\x0002ÚÉë(Qïäùjì¹¼cÈÉ6ÈÔ_©\x000fY'®´@÷"HCÑä¸\x0008ÝØx&dx\x0010ÙµÈ®\x0017ÙÈ\x0011#kD:;9+£\x001cÏh·\x001dDö-²ï\x001eeCE \x0019§y-9£×±Ý¸û\x0018²Y\x001aº\x00102ýìGö9\x001c\x0002õÉååg¹Ï©qp&\x000ew\x000cyy\x0012ÉÈùI¤\x000bÒeËÄ\x0008ÔFîªAÏT¢\x001f$-q÷\x0001pí\x000b0E\x0006xW\x0016oÎ¸3\x0015Ò\x0007\x0017L_\x0018úYó'Ñ2tNnR2Æçº1\x001c#6í\x0018î1VÛr!rW¤¹O&"$?lÛµg»×\x001eh\x000ea¤ \x000bÏðÚ3\x0001ûc¼®åuý¼ä\x0003\x000b¯[î×,ÍÈ~Ò!ÿª\x0016¹ûÜ«RI\x001c¥Y\x001bºóQÓvÌå\x0018rh··Ð»½yÊÈbdt;y\x001e«$Ä~[¥ê(q;È¡wé¡\x0014±¥\x0010\x0013K¶é\x0004]8\x0017Ï5\x001fB¶ªA¦ÈÈYF\x0012\x0015¿xváeGÙ«íò!bg\x001bwÈÙ^wÈ{_Âö\x001aprS2ÆÁÍrà¼j½ê'\x0006î\x0015\x0012Î\x0010Þ.b1\x000ego\x0011[Ó\x0010ÓÆÙGìb¹XjÜÉµH\x000c|PËæÜ\x001cmÖ1u"ã\x001f¾3ü`v÷þÜÿ¶?z$¡\x0010oû2%Rbµq´\x0006Î¾Ü½üO7ÏÎÉ\x0015R×ºnÒòº\x0010h\x001a[!å7'ïÍÙHçNÒ%L¤\x0012C>FTÂáÇ¦ä¼æÎOóÙ\x0018ýNÒÐiè\x001dÓ\x0018ÔWÇ=Iå°Oç[Àí%M
iê\x001aSi7\x001a#Õhû\x0012ù\x0007Ç Îg9î\x0004]ªb\x00084ªÞ\x000f\x000cjª×B%=¦²´ùø±{AñêÚÁuE
S\x0016Ôr'ÒäºÆÔÉÒF\x0012îðãKu2å\x0006Í õ
©ïüúÝ\x0001élMOÐ\x0013¾üªÑ\x0004QÖF\x00131\x0003ïPÆHëÇêxð\x001d \x0014z?}y\x0005Ç	g\x001aÐºçó)íÒ#¨¾Eíýö²¨¬|Q"	æ|/½¨©EíÛM]Eu°\x001aU+¨ÛMØ\x000f B;ªÐ7ªÀÏÑÊÉm}ô|úÑ^ÒÐÎAå>`ÂZ\x000fêù¤ËÓO&Õºs¦zÞO\x001duÌä\x001a\x0005ô|ÚÜ^ÒØö¹RÀ/T1zMy\x0004eLeõÛ\x0019þ	vLMßB\x000f RI~1YNµ º\x0019§éªLAí\x001eTvQ^P%\x001d<¸)\x0007kGÕõÎTË£\x001a={SF-~_q=Y2dÔÐ³QQ\x0012\x001eU\x0015G\Ê!«§ ¶N
t{)eQ%Ò}ïÏ\x000f|úL½ê~ÐUñ\x0002ÖâÃ[*\x0017Þ(¯s×T<ÿ¾\x0017Ô¶ ]¾4^OxJfù\x0002~\x001aÓñ\x000eâ\x0001ÔvõëÎÕ\x001f%\x001fz'>¦Ëe5ú.3FÕ¶¨¶\x000fµ\x0006'(ø#\x001bUMvþ|rÓNTßlTÚ÷mT\x0003®jXQÜ(i¦¨ç«Äv¢vQEE1âü%E²\x0019¼¨@üÔx>\x0013v/)´¤=Î?EUËTÍ¤¡ÍöÐTy<´½ôë®[¤^\x0010<¦xë÷¼¨$\x0014Ý¬³Å4{IMKjzHaùúÚTÊ\x0018ÙüÓAmìYþ4¨EX\x0010\x00075W!A\x0005YþñÌSÑ~ÔÔîÿ©gÿ*ÔJA_/S\x0015dTgì©)µ¤=W¿\x001c*ïÊ$®\x0005Äï/\x001bURçù÷¡öêgº®~Q%JpÎ¨6PP½ ó`Æª2ºYÿF÷­ÿÄQ¿¤¼c\x001d^D\x0015:\x0019=aS5í¡j:\x000fUôþK*E`Í\x0003
¦É\x0006àv­ªÍ2\x0008Fuí¨º¾QÜ®-©\x0000f´¹¤t	Q_ÛFÔlWD&@(\x000f® \x0013çù!ª	p6Cx'(4?ûi] eM\x0001E~dMñ×7¹=Ú8©i¾ÖôD}#xR$\x0008¡T\QÌ3"Öø´k£¢¤'þø4O£$Òr¦K>\x0007ÆQm\x0013¤ÊA\x000eÔ \x001b\x0015DbãAåì\x000bu¦\x001då\x0001Òöêo»®þä¨(\x001eÔ\x0018¯y*>$±£Zß©ï\x001dÓòH¾VÖh\x001buAãd'jëûÛ>ß\x001f\x0007\x000bIêØË6ÅmUñh5\x0013T\x001b\x001bçßÆ.ç¿\x0014§SÖü2¤Q4yD?ÀÙ.þØ·øµä\x001eëU4Åò!¨Û
(\x000e ¶¾íôý\x0012×&m\x0015÷|Ãé©dõÇ3L»Q]ûâº\x001eShT£ jÖ+¾ ¦í¶\x0018\x0007PÛØëý\x0010ª*çÆ#5È\x0004\x0000\x0000i[üð\x0008jhQ»v* åB²\x001aòBQ³¡Iús\x0002©i6*úÙuMá\x0011ËÇç\x0010\x0015rÎH pÆ´]×i¼Csú¥¦\x0014\x001eQI\x0018\x000bívÚvDmßZÊª+\x001f?HÝ\x001dÕIPg\üM-j×>¥UEMæ:É4åm
A'ý\ë¤¸N'ÅrªO¢\x0012;åÄ:cíûöûûÎ\x0015E\x0013\x00055²\x0012\x001b}\x0019ÕóÃ;IÛ°ë\x000bûiyôÃk³ª¿ãT\x0003~ÊÞ\x001fÚï\x001fz¿If6ÊÔ[å\x00005é\x0008k}\W¶O\x0004Ç¢UË_\x001cÎN10åÑþ%
jï)U\x001cc\x0014U~þ)§Tj?êûüóiö\Ac*ÿ¼\x0010Ø>P¯\x001aP¯zAy\x001aÏâê\x0008Ê²8!Î«Sí%õ-iãç$bÐñ×	+©ë\x0010aÂò*´¨}óTÓ:*¨þZ1ªãÆs:cKõÐ¸)\x001ezÜ\x0010ÈpR5$ÏzÉõÃ\x001duÂò­;í;ÝiÏC¸øn(²öI°e\x0002§k9»ÂSøõ
}gêÑ¿|ýt^u/jÜ\x0017ó«XÆ9Îò¥¨n÷;\x0000j?\x0017t)ï§Î×´4\x0017ÅEM3rh|6ï»òæiHyBg\x001adDy?Õj
h\x001bðó}\x0001?º Û©¡\x0006*\x000eªóz&{IÛYÚõ0AC*¤Ñ²ì\x0003\x000eªÔë)ù³Þµ¨®\x0017IÓ\x0012òqF\x0006Uo\x000b¼Ô·Ç©ï=Nù
Õ*]CÓÒØÃhs¾5û^ÔÔ¢öÝú\x001csBÍðÜ?\x00059Ï·ÞÉÙÖLø®¢\x001cï)\x0017)\x000b+¯ûÝ\x0019ã\x0013v©þ×Ï÷+y\x0012Ù¬ø¯}[Và=+q¾?M\x0005ûPçÅ®vçû¯Å`bÉù\x0017-OUJrj¢\x0014\x000e,* ¹¿0#\I\x0003}\x0002L£ÜGC\x000cÀC£''í·u\x001bÔ)0=\x0006t\x0002Ç	¨q¸¯÷W+¯3òÀUÿ|2)Õ95kÌ%Ò\x0006D\x001bk$1ãQOF;GX³ö2ÕU\\x001b+Àrõ\x0019»N_LbJdé\v¾f\x0008\x0019¹+Ð\x001b¦<eOñk[Í(¹Ùv\x000e1\x0002ò¥Á\x0000·Ð^_ÃÃ+£±ñ\x00120:¸¾\x0018Rf\x0011\x001d£(I80£H\x000c?%¦$¿.â@qXÉÄ]v6ÅOÜ4Íç¸æ§;\x0005íÅÝÇ\x001doÅn}¬w\x0019¡9¼1ñ\x0012Ð7)4H\x000e¡ö\x001b\x0001\üÍ;ÅX\x000e1\x0014)®Eí\x0013rÿk\x0011ÅûxõèÃûO\x001eî?ÿ÷}ÀTèP\x001e¾¬ÚÒeØåÆGÒ7ËÆíÞ×EïìÕÕ£»¯_ßÞ¼ù\x000b÷)¯kxÝ\x0000or%÷x´©±ç0ò^ÒJÜÃ»\x0014»\x0012oHý¼è	_á¥Õç¹¥ Ì\x0007k/Dlwá®j´òð\x001fà¥æKe|\x00135Uë\x0002_à¬Õ4ð÷\x0000/q\x000cl`\x0000ØaÀF\x0006qXùåÖZu¾®t\x001fð	W&°\x001a\x0019aÃÒ\x0010\x0018ýµÂëe½©KÀ{pSFpñlËJr8!p,\x0017g°4¦3îü.àÔ\x0002¬8Á¥\x000f \x0002;ÙÑp+ð%\x0005Ç\x001dÀZ7;°Ö\x0003[0"që3åºæ	ìXÆ\x001a}ÞßÉkZ^32Àº4+"^Mc]\x0006Ø
°0W\x0005\x001d\x0019Ø\x000f
°+~¥è6uhæMgNºÿì\x0002¶-°\x001d\x0001öä\x0001\x0017`]ûè"±\x0000_´Þ\x0005ì[àS\x00037üÚKÀ"\x0013ÀÞ\x0008ð%-ù=ÀKï\x000c¼ôþé95ì5\x000f°ª^\x000b,Öo©Øc×~öòâ©\x0010ÄMsQÉ±ìÅÐþÊënÞØÌ`\x0013ûg0R\x0006zKË¼6qºõ©Î`ãÆ'UÍ©aUÿ©g1ëC\x0013°\x0019\x001c,\x0011ø|²â>àØø=6öû=\x00164×*[¼}Z\x000fgàÀ==,äXó0p;Âq`	XxÕµÂ÷ü\x000bÖ\x0005^\x000bÙq_©a\x0002ú\x0011ë¿Ý_=~ÿéíÃw9ò\x0013®=\x001f\x001bXr\x0018,\x000esnO;ðg7W_¾~z{wN\x0011áõ\x001a^ÁëÈ÷\x000eîevNòÆlú\x0014}èfn\x0006Ñ\x0015m\x0018ÝsÈØænãÌ¾§\x0017ì\x0011x»·CðÁp\x0011!Nh¼úq\x001bXàÅi½£
ï\x0011t·FwÃó]ó¡h-EhË¸³*Í÷ÍC±\x000fÞ¯áý\x0018<\x0005
S]¬EcÎ*
ßl±5|\x0018ñèäñ2&dä¥{³1ÛÒ×}ðq
\x001f\x0007GÞôÉ²\ùäT\x001fR\x0011~Oçò\x0003ðÐl0¶Oz\x0012tçøWÈmn^Óéq\x001dÏ¥÷
½\x001fÜå)%«å®ËnªNñÛz\x0015=ôà%K?\x0006ß¸RÇJ¡\x0010ÍÊÞ\x0016\x001cK¾[\x000b°ù®Ò¯c{ÂÆÑ¹ãË»<Î\x001dXÏ\x000eçö<wÎ¤\x0010ôáÇ\x0016lázÏ²\Oÿè\x0004}\x0004g¶St{ð
4ç,ý\x001cÅ7å¸$&+WóÜwn[\x001f·\x000b¿ûftîûXt1ðÚ¢%\x001bñ£L3\x0012\x000e]øKzGÆ§ô!| \x0015¸¹ß=Pui;\x000eß\x001fÚÉ\x0013\x0006'OÈ-t3¾Sü>j©oQÁ÷jî¡eRã¨ÑÏ±Ñ·\x0012ôN¸\x000c¬ì<\x0012Ñòz[¶¸\x000f¿ûipîã±\x0015=ãKëA\x001c}	\x0017y=÷Ðµ­Ë`G}\x0006<j=/Ý¨9`«)¥ÐéôØEoËU\x001f¢ç4büâWÄ×ìlú3×]øíÆcG7À}Üñ_¾²ì\x0010\x0005?m?Puá·+×®Ü ïk@r\x0008'S+À\Áµ[ú9\x001f]©ÇY\x0004n£FÑ<ÞxÞNïÂ·M@~~¤¶¡üò\x0012 5§ÐÛ`·cûðM?ºt£L\x001e \x0006åAð9H\x0019Ü¶ê[\x001f~;yìèä\x0014÷+øl-Ý\x0015\x0005?Lu8©Ø°Á\x001f<µ¨\x0016ãk%\x0017]mÌ}·ýP×ßÞVÜèm²SÁw5í\x0011³ÈmÛ*¬}ø©Å\x001fÜ÷©õ\x0013ã£ë¬êÎÃÑ©¨¶zð}\x001bàÉÕECø Ç\x0016%ñ¹lÛÆ3]j»ðMo\x0006ñC(ïe qã²oÊëHÜVnïwÍ¶\x001f·\x0006Ï\Éj]\x0003Ê¸m²Ë\x0010ÝÜ3×Äx\x0006<¾\ÒAS´ç³2í½zbùÐ\x0006eÃà"¿d\x0003eÎÊ%ÝÉ51&?wæÄvÚÇÑiïø\x000eÚ+\x0016Z[Ïûí6n]ô©¥O£ôÜË\x0006_Õ¹c$&\x001eÓ¶Ft\x000f~hÝ0è.\x0004%y&@%o\x001cbÐ\mS\x001b¢È5½\x001b<¯.\x000fHO±MÞ2aG?Ùm9Á.üö¸
£Ç-.\Íø.±|\x0007%ÿþv-O\x000f~lã;q0¾C\x0005²º,\["¬\x000eüv× m5¯\x001eüÔ¾ÝÒÏ!|¤('\x0016úe×<wb\x0010zRVJ\x001f[ú±À2µãK"z\x0006uÓ|Ewêæg\x0017>4Dú9:wø^e½¦\x0004v\x0011ßLui"\x000côslôk|\x0007¯ò¨¢#¿J8Pñm³ñÐÏ1|_´\x0003\x0010ßC=r\x0013·Nuàæ:ÊÉµÇ
N\x001e©mB|\x0008\ªkI:ñ·s#ûèMK?æ)\x0007º×òà;W_´\x0012\x000böáào×
uàÃi¾\x000eý\x001eã÷E\x001a\x000fùÑùá¸¸ö\x001d\x000eo3O-PK^xá§Äð\x0011~\x000brêz\ðbH\x0010;÷º9üèÓkôrKÄ?|GÄ§¿ÿËýÇ\x000fÿû\x000f\x001fö\x001bóÜPT­\x0008\x0014Õ^\x000f R}Úö>ÿáæÕ«[±à7ww»lXêÖÉ\x0006*[\x001f´ÁùEºÈv
(\x0010Q\x0008¿ÝY©×e\x0019
´GmHÒrÑhCM9
"\x0011\x000bg\x001aíuÛà\x001b\x001büø\Ò¢ËeèL\x000blC¹ä¶/\x0000Ý6¤Æ4þ\x001dl¹Ã\x0014%r\x000b@\x001bT\x0015íÙÖA:l\x0003xÕæ@â\x001f(\x0007r1áãÕãûwï\x001eö¶ÁD_áÚ6\x0013t®¹Ò`ÛWy¼
ì uõøæÅÛ3­0\x0005\¯Áõ\x0000¸FÍÑSiñ@ñJ÷F\x0017Òæ9Ö\x0003nÖàæ\x001f\x0008Ü®Áí?\x0010¸[»\x0011ð\x0004,©àõ45{{;é±Û¯¹ý?\x000ewXs\x001cî¸æ#{¡òåVÜx©åFÑ¾vpi»·u\x00078´øÐ.®\x0003·`À]ÜÔ\x0011\x00102Ú°ýrÒCÞìâ0²;U{Ü\x0005
Ò8Úké\x001dàÍ¶Òù\x0011r¥OÎ\x001f¥óù#¥\x000e7ï~~û°»y4\x0015:\x0014åÛýÇ\x000c
µá\x0011ÕoAK¡ÃÍÇOoÏ5fâ¥?\x0017\x0011êFÆÝÛ\x0008²´Ä\x0013DqR\x0012ëvû\x0007Ù´è¥ðª)\x001at\x0015¤\x001e8³\x0017­1b6¶Ù\x0007Ö=AæÈê½\x001aBà\x0006c:iãlaûg\x00069á\x000b3wÄÀÞÄ|±lg7s37lÿÜðî:Td#È6ÎG^Gì \x001b\x0019ï	E+\x001f\x0017 Éùddy&ÃÙ|¾KÎ\x0011dß²ï\x001fejå«y³*Uf\x0016-b\x001cæóùÇvµB\x0007ï\x001c"ÐÑ³y¸ºC\x001b#Î*þU\x000búv
Ünt\x001fËp×øÎÆÓÉ¸3:d¨?MÞóBðQd\x0000½Neÿàv¦M>§q!oWT8wRíG¦\x001b¤.ÈÔ^Í22÷\x0000v\x0006£/ û\x0016ùôÑú(²ËÛGð)I\x001b0D\x0006F>Ó\x0007ì\x0008rlO\:GÙ§ MÖÖÈÛúT\x0007m3éçà(\x000b²\x000c1'd ïÎ\x0007¢\x000b¼¶å=}R<ÊkeVhV ä ÈS&²køpòQdS¶\x000b\x001cP\x0001zÑ\x0000CodgþYd«Q¶_$\x001eA¦Þ\x001b.\x001fÁ\x001aÅpÆYîÁp»³Õ\x0001ävíÙ¡µGM²Üm0¬Æèt\x0012\­ö½UÇõÍîF?\x0007phR­*'ð\x001a\x0007Üá\x0018ÌÍÍ¦f\x001aÓÏ\x0001bd\x001a#'Å#\x000b17¼\x0001\x0013v&á\@Ö-òÈ©§¹ø\x001ammÏèd·\x0005µöãºÖ­pC~\x0005ÞX¹¡TÐ1Ð»\x0001ñÚÈ¯fè\x0001ì,Ã;\x001cC³êèg?²Jõ
}\x0004û\x0007ïmÊí,´>\x000cêäVC;
¥Pñ°Pü¸jÐ{+\x0013Y%ØRóuæ Ñ\x0013\x0006å¦?<"\x0019%úù\x001dR^ýáí»O;Iq\x0013ç\[ê%&^[tK\x0005þ\x0016'¢]ýáéÛ×[x¦ædg<úùwGm³Ú;(õÑZßA_?|ø°_îB\x0007:ÊJèÊI¡¦zb\x000e]9uQøíõíÝ]«vqzÇ\x0010èØ@Ç~hJ!:RûÄ][4É\x00162µß\x000er\x001e¦^õlFê¨\x0006¨-y7:)vtèú)c\x001dÏ÷ð8D±N#cí%\x0010Û$r;\x0007ÍÍ\t Ï:\x001aTCM?G°µ\x0008:k®¿"l#ÎC\x0015»±!5Øú±­âå\x0018M¬Ô\x000b&uÐç;\x001f¢ÖÍ\x001e\x0002z`\x0013Á]ZR#¶Tã`s*¦p\x001aör]ÊØÖ\x000e`«RYØNs\x001a\x000bbs
\x001a¥a^\x000cÎ\x001e#z+Ïupèïpªü¤LûVÿ\x0008ÿ@oõ?<|zûéêÑçÿòöÝ^÷Z¬\x0017¿\x0002\x0012-{+}«vÛ\x0007â\x000f·¯¾¾zôæñ\x001f¾¸\x000c«×°º\x000fôì²oìU´tÙË°"¥­è\x001c\x0003kÖ°¦\x000fVK\x001f#¯¼àÒmOi½
wÕ®Ym\x001f«ÜlÓ+[\x001bÄØÀ1Me)¦Àº5¬ëuº\x0014#¬Îù\x00196ñ\x0006ÿíc°~
ëû`}¼v\x000c«\\x001cpPBQ\x0010s\x000elXÃ>X©33.%'íaf¹VRp4gã\x001a6öÁJu\x0010Â\x0006ÏKÆYÖ=¢ éæV{\x00046fÎÒÏ>ÜÄNGí¢à\x0012ÄÒb¦]¸8Üi\x0006ûnõ¨ôøþÃ\x0007ü\x000fP\x0002ÚÞ·\x000eJÜâLÀK-E9ÎJ\x0002Ëo»oîî^¾xAÉggÿÝi\x0012[?¢÷°[éÌ\x0018ÝÒð,xN\x0000ôv»~©Ý¬ÙÍ\x0018;Þ,³ã\ÉS\x0005gb\x0014ôí©Òn×èv\x000c\x0002Ü®²kÝ7QæÝ\x0016¸èwkx7\x0004\x001fiÎ\x00011\x0006~Û3 ¤§\x000fç\x001b¹\x001f÷kx?\x0006ïêÜ2<îÞÜ4\x0019ò'-ðç[Ñ\x001e\x000fkø08òr3L\x001a©JÎ±ä~û¸-Á×\x0007\x001f×ðq\x000c^ËÞð®ö\x001fÒ	ÐÇmm>ø´Oð¯yä¥×v\x0006qþ;Õ\x0005¿ä\x001då\x0003Jm71qîC"\x001d2àF*FZE{wù¶x¾=^\x0007ÏWïK²I¡\x0006uIý@àÏ·\x0006:\x000eß¯0xÀRÚIéºÀÖ\x0018Tâ
aãw(£\x001f£oNX\x0018=btÃNVñÀó³\x00102MóÍ!\x0005c§Tp¾¬ØÀA\x0006yr1gêúàC
ÆN)ª²âvXÑ\x0006VÒÉI;,¡aúnú$1sè\x001c%yòáþÝ/\x000fW?¼ÿÛÎ×\x0017 ]qò
\\x0001AÉÓrÀ{ý\x0016ô»\x0017ßß^=¾{ùçíò
kÖ°¦\x000b6Äô®R¾Ì×­ ¶c¬ÇXÝÕõ±F-YI¸ÙqÍ\x001d²òk\x000cÞ·;w\x001d
kØÐ9\x000b\x0014åJNÀ&\x0016?°]y5­YS\x001f«±r\x0012Te
ó¶qÆnx\x001fvyu®/Êàõ\x0005_d!HN\x001dþÓ¶ñ.Z*SÏ¹KfkRßiñ=>_="=úoZÓàg\x000cU´óµv¼\x0017èPvn\x0003{sõè__u
¬ëõ\x001cÛÊH\x0004
yYûHã&vþ¸ØÍkÁµ½«
GÐ\x0015ÞÆRI¯Ô&VÜm¥©c¸«ôÛ´J¿=+¹hQ¡KÁ^P\x0015µCGâBïý¼Ítp½Ó:l\x0004gå$±\x000byY\x0006N«\x000biä»q\x0017I\x0011Â­Í\x001fâÒæU\x001e±T{¡ÖÀÙTÓ<göj¦\x0003ýì\x0002¤¹\x0000\x0018\x000b#¯àZIÙÉ9ùcÀ®YnK[±£À.JcG0\x0018Le`ØV\x0001?ÆëcÃëc//pÝ\x0008Ös/\x0010
Üs
hÎßvó7ôòêüy¼\x0003!¤áóDZæ\x0000GÓ\x0000GÓ	lS\x0005vNf0b\x001a\x0019áó]w\x0003kh5ô\x0002\x001bsÍ\x0013"ø¢w^&½PÌ³\x001f×¶¸¶\x0013.\x0013eKÃÿ}n\x0008¬Ay\x0019_7é@Æi\x0003¬{·4ÍÒ\x0004\x000cÔ·¶0ß\x0011xÒ¡]sfÐÏ.`Bij\x001dq;æ¶\x000c¸ñj\x0011g2Úñú×wò²ô@é°ð&I°¸|7´îoè<2\x0014õ\x0002ö<À®\x000ep\x0010\x001f\x0002ýù9.°N­\x000b:\x001er\x001dÊ£n[¶\x0008jÂ%;j\x000e®QÍøÒÏ>\Ï£¦þK%D¢¬Ì_/sÖQ©åí]oô\Åó×ÆëÄãkÔùÁàýnà%\x0014k,ê(°³×'°süHEW\x000b)ZÕ\x0017Ú|î\x0006vÍA?ûK[ó\x000cì%¯\x0008RJRýi.¼f^\x0004¾WF7á²\x001búÂ}çÙûOo?~|øýáÝ§«ïßÿ~ÿöè¼¾G¾wûåT)\x0013ÎÝåDÚH\x0011ÓvÛ­xöòõÕ÷/ß<}!&¯oðï/¶/üÕ\x001c½6GO4®ÕE[\x0015ÿ+\x000b,eï³9&n.Ò\x0001sÌÚ\x001c3×\x001ci=æ4=©°9ZÌÙN\x001d0Ç­Íq\x0013Íä+ÒÂR9ÏZ^üupél:\x0003æøµ9~¦9VT\x0005©å(ëÚ\x0019Åñ14g»ç9amNûuøã ç#ß3ãÐí+ý1qmLûm\x001c\x001b\x0003×,º¦l5fûºÜ\x0018eRûL@XrM²ÈÔ¿ýòùò÷?üºû\x0015Õ«¸iQüUòøèp±g0ëÆåæ\x000f/ßÜ=¹hÃ"\mpãFx\x0010\x001dèd\x001b¼èMpIÔá¸
K	²ÁÂ¸
ÔúÖ²
jy\x001d\x000bü\x001c.=Æ\x001f7Â5F¸	FPÝZ¹Å¨y·Ò$SÏFø\x000b÷\x000e#\x0016åq2"øq#tâT H5Ð¢5\x0014ì¥NðÇH\x0011i\x0011n;Ù\x0008\x001bD#©(ëÚ\JLé0"5F¤	F\x0000_ÞH\x0010ÅZ\x0012pã\x000fÊó»fpØ\x0006fI\x0000LX\x0013$ÇVØìj\x00151E_¿ÄìÝ	ÀµVLØbIU]×òÄJýÎc-)¹ðxÜå\x0006­¨7¨~+<nJ¿\x0005­ò\x0012o.\x0015^Ä:¬ðí·ðãß:Õ\x0006þ\x0016VªXu\x0004-¥&f»B¿Û
ßZ1¾CÑÝIÖ\x0005qKRÔõÔ&Éþ¹Vè%ËØäG`=n\x0005©¤ñ×\ÎÈ	±Öµ\x0019;û[è%û²X\x0011Æ­Pá:ÊgäÈ\x000bôÂÆ;í¥RÈãV@³ºú\x0015Qtß(£ÕÁÛºÓn\x0017	\x001d¶\x0002W^öeëyøÎêP£EÐ;¼eì,\x0017Ð
\x001dAÃÒYÁò}\+Ã9^ÚèbÔhÒk4å\x000eï\x0019gj\x0007Ä\x000eÛØqªÆÑc\x000fô	\x001d^ô\x0003\x0015­ÌóbÀÔXq*)ßõ5¬{Æ/\x0011Y£Ù\x00194°\x001d»ê·Ãµ\x001dî´K\x001dÖ_ó¤BwPÌ !ÞbÆNöcV4_ãÆ(]V\x0018ÎÃB3ªF\x0002	7çPÂt;·\x0013²#jftÙ\x00118m< q±¨Ò5Î¶3õúíHÍ÷H3¾\x0007~,¦¤,¤äDMÑï\x0014-9b\x0006,oÇd\x0006ý\x001cµ\x0003\x0012%°,$^ùtILVR7v¶>fFlÍ8Õ\x0008éý\x001c<­jBó=¦N+]®}KV¿N+5ÑÏ¤zþéáþóÕ£ßîßý¼÷\x001ck%ÊY+\x000fF\x0001\x0007×é\x0006{þ\x000cCç¯ooÞ\=zvóâñEzmÖôÚÑ~YÞADÅë:\x0007\x0011&Ò¯.zº¹èuâ\x0003pÉj¢tÏéåë(¤v)#h'¾Sª-©À?|·¾lÿßÿù¿nýíí^\x001c"¤¹3\x0015Àv±y)1þêÙÕígO_À
³iÍ\x00183?í\x0011s©½&fÉpábìu7µk¨]?µNÒ«#R;ÖÒ\x0018ý9àI¢.
xî§ÖÍXë±Æ\x0013tá
uàj!¤¶F¨/$»\x001d ^²az\x0011Ñí F\x001f¡éY«$\x0014&áá>mV/Ý2s\x001aaöf
Fs/\x0017ª¿$§Ë¢½Ð®ÔndR{µd¾y¾ãÖç$óírn7u3Ônd¨@\x0010 ;ÌZº:º¯w©i?ukê\x0018\x0007¨\x0013=k\x001aëâ5¢-\x0012\x0010\x0005}9|µ:5ÔiZ{.\x0004Y³½­\ËÁl÷\x0000?H
K'oÖë\x0000ÏqìP±á\x001djä¬\x0019²rhËa>2Ø åA4æ#Këqo¢ä\x0001lÓìÖô³\x001f»Ô/gìd$_]FÚ_|¬Øl[·É\x000eøMºÜ\x0013
râf¯${^©§ù 
Öø \x0003\x0013\x0004èÙZs\x001e¢ý\x001axª\x0010§\x001dçàý\x001aüÀh9?\x001a&pÆr\x0012ßéBÁÈ\x0001èh\x001bèh\x0007 ñR\x0013\x0004:I;
\x0008\x0012täfí|z)SÎ\x000e\x001fè\x0001lãXvK²uR¤rYØ¦qD´\x0019ðDHdõýð>&ç\x000c\x0018#	æBí\x0001lßº×~À¿\x0006*î-^I"Z %NªÝ%ý\x0003Ø¾Åö#Øµ4lùY\x0013@Ühfí#ºÝGôÐ>B¥\\x0014Jbó¼$ ;;kn\x001bÝ\x001c6F\x000f\x001c6 \x0012¹{%Ì¦¨\x0011K©¨Áô3áÛÃØ¶Å\x001eØ\x0000ñ%9R\x0006]¿ÒÙ\x0011oçIçzÚacÚ3Ò«/Ýy¢\x0008üQB¼¼À\êg²º½\x001cÛB/W¤U¢äåÙ(JßMsH,4\x001bD9#ïDÖXÙ¶\x0011êx!rvÚ4·\x0003úÙOm­Ü\x000e¬7\@¥´$\x0012XuIåk7µSÍYC?û©®{tèBÉüPR\x0017²Y·GgÚº\x0019Ø±\x0015$Ñ¿uAqæ	zÜ\x0012rj[`o7¶	ùG/¹\x001a¸èõª]àã÷ï~ý·ÿóáì\x000eP:~Â
É{©È®\x0001Jtü¶÷ki¤öøå'·wÿé"ôò\x0000MÐÆöCThQ\x0014HAK³qÀ²ôÉoBÿ|ÿËýÇO\x001f6¡\x0017Ùo¶z\x0000Ús³½¢kqÐÛ»ÞÑ¶ÍHÛ\x000e¢4ðb\x0013\x0012C³\x0017\x0002;Z\x001bîfn¦´\x001dÒ¸\x000eËe\x0006gG}Úx\x000eôÑ@ï\x001d\x0017¡S\x0003ú¡)k\x0007:\x0004~¤º
½]\x0003t\x0014Ú5SÚ
LiK}Êìð\x001c¼6^&tØn|s\x001896Èq\x00009r\x0005?"'\x001c0¡îwa[~ñ(´of´\x001fÑ%y.C'+©\x001d&H¯¬í7ã[ôZ2·iúK÷Z4Üå\x001a§µtL'ÕÙ ÓZO#EwvÑ¤0¦hR,íÿrÿ×û_ß=ìú\x0006ôð4´t9
0\x0012ÙôöwöÇ¼ùñæÉÛsbåL`M`^s§2¤¯:+PóÛ\x0015l?àõÑ7c\x0006Ç¾n+H¯êØ<µ§×Ó~z0
=1|µàÈÔD,/=×Ò\x0019Ù«.ü`\x001aü`Æðýr\x0012E#o7ù¶-;ä\x0004¬\x0003ø©ÅOøNóÛuv³¤\\x0019ì8aîà/EìÞÑãÂõ|<ÑÃpÑÊJ³×q¿ÜÓ	h?¾VÍÔÏ]ÉFðq¹ëät%G@æ;w(n¯\x0007ñA$Ò\x0011ßpn\x000fQB¿­\x0001×Co\x0017\x001f¢§\x0003ôY\x0015\x0015ì¢\x0001nD\x0008AK\x0003·h·\x000bõûð}ïÇðu\x001d|j\x001fã\x0018_ÄôÑ¼mm°>üØâÇA|Å:*,aI>PFèÃTÁµsÇ
ÎàtU\x0014ôµ±Ák\x0010¾Ég[\x001e¯2~´cø:\x0012jÄ§r²ï8)Ñ\x0010¶Ã·=ø^5s~\x000eá<¿\x0005ªL,\x0005íàXÍ\x001e?Îöµ>4O?Gè½7\S§¬Z§°ç:¢ìQ7ìQ±»À¯µÁãµ»<|ÚhÄß.\x0004íÃ÷-þØé\x0013éZü¤zRðå6\x001bÔöÛV\x000f~\x0006?k¢àã½Ö@¬åú0°Þ¸*\x0010;	_ÛPãêÔc\x000eªªGïÿéþÃ/oÿíØ\x001bñ
8eX*tøÖ)ú\x001b.Ü\x001d5U^>ts÷=	\x001e_4`%k\x0019OË¹»\x000c0ò8\x0007T­\x000e¾\x0016è]Ò(?jo\x000cðã\x0006(\x00124(Õû[£\x0001rM§£a®\x0001Ëm\x000cHfØ(e"!Y\x0011+JQ×\x000eÛ=l{§Ð:ÄÃÓhi6ð!j	´Ð\x001c\x0002âá\x001dy{ì¸b­\x0002&@myO\x0014L~{(éñïî÷ª¼Oô\M\x0016àKg4"¥ëHQl[ìãé«W·Ïo_¼¾zv[2ä_Ül¬Ä'm A\x001bB\x00163È6X`?\x0008m\x0010¹O·-0ÑkBM0É&x3n\x0002}`\x0013T\ÑÑ\;\x0016ØkB-þÊ&Pñ× 	1rc¥2	^:¦\x0000	0lBª9Þ$ò­
¢\x0019ãÎ\{mH
iØ\x0006Ò3à (Ù\x0000l\x0003^ÏÄm¥½£6(gOÎgg\x001bÙé'¸¾ßÛN,Ä@cÔÆØiÍËØ\x001aË\x0002WVÃDä7WOp\x001bÅ_¯Â\x001aÞÔÇK\x0017Þ\x001c2D^\x0017Yµ×\x001aÉy´Ún+¼·¼Æ75o\x0008¼Æ\x001b\x000bñºë¢òn-p_Lä½ K°76¼±×úRùD¼[cZÄ\x0004á½T0·\x001375Ó!õN\x0007\x0003¹9áêkRÅ½(ë½wU\x001bG¼ëÚ¸cÀAÓÓT\x0001\x0006N8±ÖñK&\x0002ëK;M³?ÐÏ>à(~\x0005¸è\x0013ÚÀ¯\x0004<gFÀªÐWºÿÇ\x0013>\x0005\x0008lu\x001daÞ­¾$¡±×µ¼®7)¸æ\x0019l
"\x00197Õ\x0005w)Cw?o;]ç\x000cN*Ú·²C\x0014^§\ÝÐÌ¤ùàuÃëu'/èR\x0003L\x0003ì8Ý\x0001ÿ#QV¹(*»\x000fxõB@Àù \x000bØÅ³À\x0011¸ÈvÀÀ~;¾{l\x000fnïgìFÔûÙaO"\x0016ýÂìH\x0000KKJi\x00109\x0012ÔÞ/Pß£÷|¢,\x001bÔ©²,R¿~ÿùÃ^¿-ÚëhJ$¹\x001cUq¼¹Ñ;Ç.ß\x0013á_¿|sw\x0019]¯Ñõ\x0018zâj½\x0010qEr4Â+!WÛÙ\x000e]äfMnÈ½\x0007\x0000êÄÙiIûñß±Ýø¦\x000bÝ®Ñí\x0018zøsTVW(o\x0017»n»ÉÝÜ
DÎg!W¬¬­ÿób©ÇÑý\x001aÝÍtÏ}\x000e\x0010=ò\x001d\x0017×¨érV\x0019õ8yX!rÒ·çA7µ°"yèÛ®Þ\x0011p\x0015U;äôï\x0016Eó\x001fh·@¸ªP¤Lä\x000euÚFW»R](]~sõ\x0003þ:§hÎ¸:¬quèã5).\x0014þ\x0007*/ÞÂ%\x0003æâ}p'ïRÞ×tòF]ºR7\x0010k¡&2^¨GØ\x001b\x001bÜØ«8f[[\x0010$kRMqÑ|¼Ñ­y£ëäÅ
Úpº¶¯ÂVÃ\x00152\x0005\x0017T3\x001b@õN\x0007º¿òø:'`Koi×^¼oï\x0004^I²åÂdÛ\x000blÄíHÆòU5ËRÏYn`Ý~öñZÏûY@4yv2IÞýÎe´\x001e\x0004\x000e-pïfá\x001admM¦¬8À\x0017¶ï\x0006^	ªå\x0002êÔ	¬\x0013kåà\x0008+Q¤5\x0001$\x0007\x0011.^\x0008w\x0002·[\x001atïi ê\x001cÚÞ²T¨±,>\x000b1Å9{ÚªÖ;6µÞõ5gº©ª¶g¬\x001c\x0019g<ýc[°òëë`q"V·Á~DjP^­\x0017Y\x001fg´äÕ^\x0000½\x0008}¯ÕÉmP+¹
^ýöðñêOô¬øî#¿3þð\x001b	óï\x000e\x0019@)ú±@sté,à\x000cgXzñ:ã¹]=»}uõ'z\|ñ_\x001bxFêüÑkcô$côµ-¶hÏâ\x0017k[ìö«ï-fmc\x000büF6FsîuZB#x?Û]¤ß\x0018»6ÆN2\x0006JKÊbáH\x001a°,	\x0019ó¾[\x001bã¦\x0018CêY!\x00011\x0006÷ÔåËmcÓo_\x001bã'\x0019Ã©Zh\x0011Á\x0018[ð6äÏ6ãè7&¬	¦Y¨_Æ\x0001kÙá8%\x0005~\x001bcâÚ8É\x0018ÏMRtPÒ]Èé YÜÖs\x001c³%­mIláo4&\x0001\x0017ñ¢1|uµIm7U\x00182¦Jl#SÍY3¤ëÂÆ"\x001e½ºð3\x0011zßfA{þÏq\x0000èYÑ±\x0003à\x0016k¼«kæ\x001b}æü9\x000e\x0000=éB¨çå­ÙFÙ·S~Çi\x001c\x0000ã\x0001Pû\x0011Ã»ÕÒýÍ:eªkö>Mã\x0001À\x001c\x0017\x0000¯ëÀ.@\x0000î`Î\x0019¿ýÅt6mdÀÆ\x0003I.\x0000ih§Óý\x000c­-@oÌwØ5¡³<Ê§&E¤ß¼zòðnwcDCeÅ«@Iæy^\x0019Gê\x0007\x0019\x001e÷åÍåùÍ««'·/®§¾Eôw±.×»ÿ½!VaHÂ0o©ô³\x0003\x0011ÜuI\x0011	Júf\x001b\x001b\x0005°.ÉÿñBG?{è¸Ó
âAäp\x0004â9vqõo'g\x0010U2í\x0015þð]UlCÈ\x000f÷ïèþøö×w\x000f\x001f÷ÁöRß¨(¼hP
¬fB¼¤ÈÀw7/èþøôÉÛWÛQ\x00141À­
pÿx\x0006,ÊdÀ"¼ùcÁ?ú\x0007²@ûö¾Aø®í}öû\x000f\x001fäËS±f¡'\x001f£äC\x0019E·¾L\x000f»ê\x0016\x001eÿñæîî|Ò?£\x001b¿F7~Â
±ÀGÇÏ{F¥ ðzOÍÂ~øE\x000bàO\x001a1öÀ'\x0019ùÈ%Ê\x0008ÏÕùT\x0006f²Ý\x000c²kV8Ç÷×Æ3;§y\x0019ºåM
|\x001c\x000fúº4\x001e0*Aìx,É¤¹\x0014zÝ5\x0003ï\x0006\x0007Þ >uHàê\x0016\x0003ÔÓ±À¹3Þ5ËÕ
.Wod«Aö"j\x0000*ù£ûÉ=Ò
nÿÎÃîÆn4EÊ\x0012É¥²K¦R	o.¼Ò\x001f_Z\x0018\x0011|PÕ×ÅjÅÊ	Ñ¸X/+Ô\x001ea_z=ê1v<¸CQÓ9Ê\aøËBÀ§fàÓàÀ§XÞ\x001f\x0010\x001eo\x001cW«cG\x001eÿi;Ò\x0005ß|\x001a\x001cù$zÌt\x0005\x0003O\x001bÇ*\x00028ò\x0017ÉÂ7çS\x001a;èåGÉÈ{NJ@ø(sþBÊ1vXz#\x0012;ôF<\x000cOùÔË´)m"\x000c\x0004îîHÓf¦?¹*\x000bÈôvlÒ'\x0012=àycD\x0010ÖTá\x0015²cS¦\\x001biË·\x0012©\x001ayôðÛo\x000fý¼ÿpªm¬È\x0019ÓÏU]\x001dÉó-É\x001fÝ>{vûãË´Ì1ÑÊñQÚ 3Vò×ÉS	¢Ïï+»i\x0006ÑÊMã(-î&~Aë¬®´sÆv¹Z\x0010­\-þ^gÂÍiC÷Ø*¡5T=_Æ¶n\x0015\x0017r.ÓZ(\x001aµuá\x001f¾Ó+a¬ÏWßÆ-âaoÎn2Uäi,ð(í·ÓE(âÍÕãoò\x0006qÜ5¹\x000f#äÔ¥]\x000cp¶1:#¬>×ümÿ»<5äi\x001c¢H7\x0006z¡ò¼c\x0018I«×êÈoV¢2ylÈã\x00109â¦ü\x0016(jëÛ½\x000e\x0002\\x0016Q;0æ"\x0004¯åë\x000eGJç-Yõ\x0001ýî¢\x0006N¬hïá\x001f§7+4¬Ð\x0018äøÛP\x0002ZÒ\x0019Î¼\x001f'`ÉéçÀtQºè¤ÄõFxË¬ÚW\x0014þ7èÚ­\x0013úxk¤¿ì¼57mBï¶\x0005ÞÐÇØ¾ìÓ\x001fVí\x001c?^½Bè÷o)ýûZú"V\x0019^íÈ«RLëBôö\x00152?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-14.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=íU¶0I<­e\x0016|3©H\x000bK}í¢¥"\x0007-Å\x001aë÷ïwU\x0012¬¿\x00190WÏ-Ì
SìâzpÞ
ÅÍ 'OÁ\x001a)â\x0011TY¢Ê1³J<
3Èfã\x001a\x0010º½nd[GPUªFPµ×Ø>î<LÃ\x0010§,\x000erß\x0010=\x0019aÕ%«\x001e2«¤AòÁ®:'EîÍ\x0016ºQH<ÂjJV3dWÇñùÅÓd¾\x000e)\x0012\x000fà¶qA\x001eAµ%ª\x001d2+74=\x000bZOqô)rí¢QD6êJT7dUm°ÌÝy\x0008
\x0018Ì´ ©T\6^µ\x0006XºGÌ±\x000fÀ\x0006ÂtûqÁí2\x00037T2y#_=ÂZùV>ä\5g\x0018\x0008þ\x0001\\x00034x«üyµòX|ÌeA¯>î,F¥<\ÎhkÆÉ`µò\x0002|Ì
((á<ÀÑÕ$ÁÃ]C(h\x0004¶Ú\|lw¸¥R,09G¦s2½5¬aÈ½V5\x001aÑÅÂ\x000fF¢ÀdºóðLH^ÖÑ;¬à¬^\x000f2_WâI1êÃí×8¢\x0010ô]?ßî-ØôÊ:ê\x0017\x0006q|¾@²¡7ðáômK\x0008ê®¯Ow\x0015lòõî\x0002º\x000bº1S\x001e!?l#§\x0015ôÈ\x0016+LçsÊS\x000epz\x0006§Õ\x0018³\x0014ËÀ\x0008Ò\x0010\x0012¦!4×Ï©KNÝÏ©Aô$¥ìBLÉïS\x0006:\x0012g£Cv:&\x000c©o\x0002p\x001e(ÊÃFú°Þ»I?\\x001dV>;5¡.-Û,\x0011 â°>\x001cGMï½´Ò´Òá\x001aK\x0005åp( 6Fíéeõöáç}¸®Âuc¸!¨2\x001a×£r3­6<[·!+ÔËÝzÍ¶Û¸\x0015¾z|ØO+õx÷v,\x000b§ÊÆ1Üï\x0012
¸¯./&Ñvýè2{£ðiÇ1gQá]ÊBZÖh·í¤]ï5ä²´íóâÍÃó=Î8þ°|þs\x001f³e¤­\x0015M\x0005.«øXßPù'âëÅëstüáøúîç\x0016%·Åm¡0:eô5g\x0000
ÚqY\x0018 %¹A\x001eN\x00088\x000c®f"\x0008¦¼L+;[Üz\x000e··Twh@y\x0010W·!­o×\x001aý3\x0003Üàv\x0016¸LSa õÃÁM\x0008-U\x0007]ä¾$÷³JîYQjµT,r9×x\x0018\x001c\x00007ëÍU&5W­jÁ	^Þ>=<?ÆcÇÓ\x0006\x0008KSg¨
nEP÷ :\x0010{vt\x0007GWxyúþâú2\x001e@ö\Ì!·jÙ\x0015N\x0001QjOFz;ö^v²ö/·µ½oç\x0018\å¡ïÒÑV08UÙjËvµw\x001bÿò±ÿ8\x0003^+¸è£Í]®^;7£æ,ô\x001aýf\x001e:¶*I\x0003.3û®Úü\x0001ö¿ÕìÃG*3®qb
²7Ê©f±ªÙ?Íc×¶Å.\x000e
#L}py\x0011~\x0010'~Ü.N\x001e¾=ÝÝ/.\x001f¾Ý>í»~	O­òÐ\x0012»"Å[B\x0008®
	põ:¹¸zv¾¸¼¸:}¿RªÒI¬D	÷AK¢Üyô"²!{ÒMiJJÓOi9fß!\x000b)=\x0018ï\x001aùÌnJWRº~JÅ¤D[²Àð4¥\x0003\x001a&Ç¿8¬Èõ\x000b·¨.Yß\x0016'_~û¶x÷ðøñóòîëþIo\x000c³nI¦(ýna\bj\x0014­Á?ùúrµ8y}üæÝÕâÝÅeøÓÙÛóéÄÚu üQÌ¡"\x001f*úÜâ¸(!¾1Mq\x0016½,éå<zP0CÓ\x001b:/Á\x001dÆ\x0013|#4\x000b^ðzÞÂ1*õªÛ(³K\x00037­ÈSVMcö.úmB;bí|\x001d~Î5juÂ\x000cNI@Ö0gpîzuìF·¿ü£·?ýcá±K4Ð\x000bg\x001eZÅb´ïÛ±»éu.ë¦J\x000fü\x00138t¶,\x0013Zb3µ8¥ÃA»æA­ÿWmý¿f­\x001d`Ö á­&ïX®\x001bÅ7\x0003è|=±ÊmîÍ|^/ÿx¸{Ür
õ\x0011Cd4YP XÒhj[Y÷u8)}¸8»Üuëµë©\x001d1§\x0012:(OHåI9No"\x000cõ-uÜÓ	eI({mè
%÷x\x0008í\x0006ò9P
\x0017ÃÖÄë>@U\x0002ª^\x0013¨d\x001aMÈ£\x001ef2¡ÄQ 0ÅdKUîtB]\x0012ê>B\x0001âÃVâ2Ô¨Á\x0014LÈ¤e¸MÒf:¡)	MïG\x000e×*
¤\x0010$Á\x0008\x001bµ¶$´½6t>µUh±iG:&\x0015\x0001j¿¥º}: +\x0001]¯	Í¾\x0006
?é#Ó{H¸\x00107"j\x001faQ\x0014\x0001Þõ"ZF\x0016DBE;ÙYy8ÂÊ\x001bò^wX:ìÈ99l\x0000;\x0011khÈ\n8a/¤xÈ
\x0019ÓçÛ*;öt1\x001e:îêÞ\x000fÎè+<XØ2\x001f6ØgÍÝÑ¹PBMË^¿\x0013ËÈïxz9âJe¿3ÐÖ&´&\x00140ÖË+´¡Â&àxD>BèÆôÃ>ÂeMØgÃHh\x0010Ð£@5\x0000:ÚÕ­
Ò	7Á1TG°\x0017á\x0007õÛåÃÝ\x001e:Æµ£&\x001fÁ4äâ»«\x0015Yí¶¥çµÊå_^mOY\x0010¡(	E/¡4V¨(@ÞÝÃ*DBÛX²$½ÐH=¶\x001c\x001e£
YVGo©\x001dt\x0012ªPuÛ0`át.Ã²ú-Ló¥üFçN'¡.	u/!¤øh~XUWxÒ5VçÿNÀÕÛ\x0000n}Á§d+ÊøG¬Qp´WZc3»!ojÈÞOíIGpM\x0002}ÌXêãT6ÃnÆeÍ¸ìu:ÚÞDð?|NÖìobÈh$¯½bøA5Åû*Ü¡\x0016¯n\x001f\x001e½Ý§q$Âù\x00155 BÌÃ/.-\x000c;¢¦X»c@íU¸@¿_¼:½¸|uº=õE,Æi4,ÒÑ\x000fÈ:?¨]³]§!G­ðµë¿)êª\x0017¯_náÿìU¿\x000e'²|?\x0004\x001d\x001eIúgLQ\x0004o]\x000fSáÏõâõñÓãðv©ý\x0013¬(aÅ\x0018,ø6å ·Ip@ä\x000fÐfk\x0011X\x001f­,iå\x0018-¨ôaá\x000f`âGZ`åæÒ\x001a¹&	åpµÈø»ç»§}I«¨+Jíç^°Ìc<Ýç¼ô»ë³÷;Ö+aÊ\x0012SöcÂ \x0007Â\x000c+MU2\x0004'S~×Kü^Ng[{>ñkÏ'áð¹\x000f3ökãâ|UUM\x0015\x001aNí*T¾\x0002Qù	¢\x0014ýFÁsH\x0014+Qp\x001cÆ,±fjgu\x001a¥*)Õ\x0000¥!AyéMî©1\x000ce\x001c\x00149Ì§4%¥é§\x0004Å5|#ËÒ

ýñ©£9ow2¥^¦Ó\´\x0017\x000fÏ÷·,\x001f?áKùÛýÌá/ä±\x0014ù}nO²1[ãÅÅõùéãËñüíÅ¶\x0012\x0016½>L§AdÝÊ{PaD-K!\x0011yM­ÍÒ6B\x000bu«U\x0005[+o
?ÃKZþ¤\x0018EÊûï
ûQD\x001c\x000b¾!Ç\x0018êM--\x0001ðKÇ¯\x001c£HIÿ]ëeI,ÿO V%±\x001a%6èVA2C£U"Ö¤!©X£©M¼%é ÖÏX×~
ùéi¯SÐ\x000c:>p¾D8¬ .5ÎÓ[P«Ù½Tè|
Ëùýû\x000eL¬?\x000b±./=¸\x0001\x000e\x001fË-·I#»ÊgºeI,G<Âq#áª ò\x0013³Ì£QäsK\x001f°*Õ\x0018°þk|ÙsÅñeÙsAÄ{ôÆWÀ»°.iõ°y\x0005UOp)óØÂ¾¦¡*:h_[\x0012Û\x0019Ä\x001a¾%¹\x0008\x0000æ\x0004Ü¨µ\x001f\x0004ö%°\x001f\x0005V\x0016D0&-YK'\x0007ó}°-Wd{ã¦»\x0019\ÄÒ¦¹\x000eirN*VÖù\`°srNÇ*Eö7\x0012/GYÊ¤Û8ÞÝÓ\"ês
\x0017ËÆ»|\x000f±Pk:ÿÐXèºüçÿ:ýõþîÛþQ\x0014VBMw¬a´ZqÂI\x0012\x0008¾Qü@\x0002
ÓWçgW»\x000e=jM9?6O`\x001aAsÝUX\x000eXé\x0010Îu
¯Ãð\x000eµá`uvýçÛ?n\x001f¿í}\x0001Vw
\x0003-\x000b1\x0019$¨w\x0018ocáü°«EáçÓ\x000f§W»^¤nVuÖ+ü f½n\x0017o\x0002ÐâÝÝÓÃÝ¾óÝãx#3¤\x0001'M8ë /\x0000S·j\x0003ß\x001f,Þ½¿8ÛæruÐðÈ¸\|¸»½®Á·_ö7_yGuÊiÒ\x001dgXÚ\x001c~Ü\x0018ä\x0006ýag§gÐ4øòôòÍÎïÎ×¿;¯\x0007ºÜ/î~ýú×Þä¹\x0001Ï\x001a¯)\x001d=ØÖÁ`5äüøýÙ«·ÿë§ËOËoO·ù\x000fë¢ä\x0014\x00030Â¢"æ¹
EsÒ\x0016·9¤áBZ?\x001f¬©ò¾Z>î½úXúí×<"U!»Ú·\x0015â¤\x0006¶ãËÓíj½ëV	¶V9ùz\x0019\x0016èþ\x001b\x000fã
Á(PhN7ÕÄR½3Yðú8,Ñ«í z]ÙF'eú\x001b|èÅþ\x00199Q\x0012_Ò¸a½Ò-9Õ¸ÍÔ7ÜÅ\x0005ÉÙ+KÜ¼ÁdÜÜ¼\x0013\x0007Ö¦¸\Ilä8xuÉ»?ÌËAÞÈàXGIâR¯$º7\x0003é\x0010¯-yí(/jÒS° »\x000cgj¥ÆÜ
îâ5v½¡Ë²¢jðêi	\x00133o¿þû¿¡oøþßÿ½_%\x0004\x0003¼3Ð×$&Fíãf{éÖÕûc\x0018 yúö\x0014ÏO'\x0012\Ì\x0001wá@:X0çØf\x0011^i|Û¼!rYËYäá\x000cã\x001d¶ìÛ,Â==È\x000bÝ\x001aU6L®Jr5Ïæ\x001cZrÈæNÍém4Øü«Eäz\x0016¹`(\x000cé<TÚÐ¢¥ñp\x0002êI\x000eGnJr3Ïæ\x0004\x0017ã:'rÃüÿ\x0016ÛÜÎ"ç\x000ee7ùÊ\x0016lN\x0003Ò\x0005ß^Z;@îJr7ÏæòÈÍiæ«ÑmîKr?Ë;¥4.èà©5¹s.qµ\x0004Ï¾µà¬×hV$rFSc«\x0011-\x001a},3ÛfM\x000e¡W¡ÏE0¾>½jCµvÖd´Xå\x001e¬Þ\x0018ðÜ~cøÚ-Õpº¥^>|ü|û\x0018«êöHêpBÍ¶Ö0å\x0019**rjýÆ%0`^Ãöe,­\x0003\x0005É½¤¢$\x0015#¤Lá#G$Å\x0001¤ÊQõkMº\x000eÊYs{á\x0007ÑíÑ5ðåò~¹7\x0002%96=sÂ\x0000\x001cORÉÌ®\x001eà}k<\x000bÝ\x0002_\x001e\x001fC:%¥¦â¿¯\x0013úÐ\x0010æyMp;Kxyìhå¤öÓÝHS×/¼\x0008?¨Ê¢ÊÊòc$ý9üpß^0\x001c;·Lî}
#ïÅÂ4ârýMÔZ9>Ø?\x001fîb\x0016%³ÃìQ\x0011^1x¾Y\x0005TjóSfÓ¼Óù/ÏÏü7ñ\x000f¤¬eOÚ\x0004Çúp÷%à\x00011*ÜGb6Ê\x001b\x0011\x001cj\x0005"M \x0001?x)! é3H?ýSzí½Âùýý¿Ld\x0000Y
ø×ùrñ&8ËûÛ»¯Û1u\x001e\x0001C;\x0011üd<\x0006@¿,<A\x0004\x000cÐÿt\x0005ÆñâMpç§g[/Bü?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þå¯?w\x0017ðx4^\x0008dwî-ÕY§\x0002³Q{/,â_ÎQO`ysysýn±«'\x0011\x001b]\x0012\x001bÝÅïÉ÷\x001e\x000e\x0005T-i\x001d»IJXÆG.[m\x000fÙ6#GK3Êz\x0011¸aÖ96X	îtQv=d×ìÑÂ!õøz'hç±^kÊ÷F9½hB\x000e=äÐ\x000cU\x0012\x001a\x0003ÎHj¢ÖcatòD\x0007k\x000broööég-ùCÚbÈ>
\x000c\x0019rÛùhf°\x00059oX\x001d2ïW-\x0003ÃRºÈâF\x0012Øì¹)£\x0018-n¨àU°ÿô\x001f\x0004·¢ÛG\¿®\x001fáä¾\x00134zìã§\x0017\x000b8\x000b§Zµ ,	"K=ôYãÓ:,Ã÷\x000bøc?¥.)u\x0003%>9\x0012$_Ï2Ú3ä Ö³\x0001Ò¶\x0001Ò\x000b.õ\x0015Åd±:ì\x0014µ4' ô%¥o Ë\x0019m\x000c\x0002'S2ÖS2p¥Û)%\Kû9\x0018åò;ÕÛÇëÙÛÕëËj·y\x0015À\x0015¬\x001a«CÖì´ÌFfÐÅÛÅrövþ°O[meHUBªzH#I°\x0000µ$Ó5\x0012\x000eó\x0019Gçx\x001d¡.	u=¡t;aÊ·é`¸\mâÔRhJDSÚìó\x0018è	
¾´Ï©àAÛD\x0003¤-!m=$JüÑcJ°d\x000f¡\x00169£)®t
\x001f;ÐòÓ9f&IøÚ6ÏQ\x0013êJH_BújH\x0019}~ä\x000b\x001eÈu\x001fv'jÕê C	\x0019\x001a>w$\x0001¥nõ!-ÖÀ­&\x0010É\x0013|íX2Æú@ÂÚM2ËÚGªTÓAx\x001eãnñuù\x00192-ã¢!Ìu´ÙÀ×Ü³åFËÁ*)ûMýn#=!¢¼QúØ\x001eí)£&È½­FÖï5Xn\x0003éè¢\x000c;?á»ÑnJÊÞv#ë÷\x001bl| :\x0003¸1s(=Ïm£F'\x000fb\x0013U_û\x0001ÀýæâÓoÀ°¯>=~^}ÜÓ¥ç`%6~P\x0010 ¥¦µ¦þ\x0011©ì 9}qu\x000bÿr1;_]\Ïß.Æó¿Ï|®ÏÆH/£ÀghÂ\x0018­è¹\x0004ø\x0006\x0015æ\x0003¾½!ô%¢o	aj\x0010Cûc\x0010A& \x000eä«\x0011ó|é\x0010q¾T\x0011¡0Z®ãÅ2'ftaûtVÏØ\x001b²z(v¥X.\x000fEÏ¯¶lv\x000cCq{J×3öF£¬\x001fØNoQl^\x001d\x000fG3hX®g\x000c=ÆPÍ\x0008÷ëÈq¹ïÚj(Ú{0"\C¶nÙZäë\x000cZñþí¶S@-\x001f_=ýkw®\x0013ý¼Î©\x0000"\x001cø{»ÑÚÀÎ÷¶\x0013B-/ÞÏ/ÿ±\x001fW¸ª\x0015×äÄd6Ö3îØ¶ØB«KZÝHk\x0005K
Åù\x0016\x0014\x001fÎëæh]c\x000b®)qM#®fSZÀµä?e1qG[B[pmk\x001bq§F+dn s¬¥\x000b¸£×ñ\x0016\WâºF\ãè5\x001f¢Ë\x000eÎ°µÍ&ªÁàK\ß\x001b,Å@t\x0005Ý3qÇ\x001dP[pC\x001bZ§?cZGe\x000e{H'×ÛVÚXÒÆ6ZTáÔ4ÓÁKë\x0002µ+=ÚÂÕ»©Ùì6	Ñ:Õ"	LBx%uï9Å®íÊÚ\x0010µàö6	ÙºKà\x001b-å<á®G½gpâ]BÿµðöÖ]ÙºðF´þLaáås¡\x001aíïªÁe¦d\x001fðÈÀ$cþy¯pD'þº`7 \x000b4."Ñ\x0000ë\x0006ª¶|®I:æ×»\x0004#2¦*1U\x0003¦\x00144^\x0001SÓ\x000b\x0013ÙkÂâïñºÄÔ-Ñä\x001eIÀ´Ü~(ÏÑ\x001cØë´`Ú\x0012Ó¶D3\x0002O\x0017MÚ¹D b\x0011À\x0014Ûã³\x0006ÓmMÆf~Cøïö\x001eW»K¼bt»0ôÖjÚ\x0004ê\x0007eð"¯«ù»ëËùÎ*¯­áéÒðl!y¢ë$Röð¶ah"Õ%©n"õ\x0011µARL
6t¤ÔÆ\x000b!|äª\x00025%¨i\x0002
Üö\x0002!gôí#&Ú00Ën\x0002µ%¨m\x0002\x0016;
RD¹é8ðÛ¦À\x0007ðSº\x0012ÔÕâÖ0¢@\x000c9¤Óµ¼\x0015¤¾$õM¤JP
.1É\x0003\x0005kØ>Ùú
S\x0013h(AC\x0013(lL\x0007©=£j\x0007é@;µ	4 ±	ÔJ*\x00150
{C\x0013(·Â\x0006zåis8í|Ñöé\x0015)¨\x001a,ÖôéÙw~øàÐ\x0004Úß\x001a6'\x0000\x000bá\x0006z®\x000bN)þöÃf1Ô©:ß¾¶DâlØ0 põyÖóòÄ\x0017?ÜN±âËÞ/\x001b|¼:\x0019ª\x001a2XÆ¯	ÕoÒQn\x0013jo)mk©\x000bìõ\x001b~HãÔ|"
<[\x0013jomk\x0014*a¸¼ãG"eC¯\x0013\x001d¢¤øiµ5ûWM\x000bjÜìúäta´<Z'Ë[\x000e¡t_Î]v§¿ï62¥³§ÕìüñëÎ#´\x0015F\x001a>BËô|\x0012\x0005KÁR;¸>gÒÙå|N\x0017û	UI¨ê	f?o\x0014\x0014J-QèÀ{¨\x001a,O
¦4Ø_/¨²Ñt¢ÄÝM9 ¨{DY»ã!c	\x0019«!£f
3-Pt\x001052\x001fíÅö¬gýñX; \x0001\x0012åúeL(aã~\x001aJÝ£ÔÕRDÃ³[&óëà4oíèè·\x0017q\ßùlÏÖGô§ÕÇ
z\x0008:°Ü#\x000c\x001f\x001dÅ@E7³Eý·\x0016\x0001ÕGÒéXM0Ü Iã§¶ê¯?µ\x000b\x0010Ö|*Ji\x001b¨¯"(Ç\x0006~Î
ê[\x001a {ëª_°%/Ý36BÞA\x0019ËëÏð¢Ñ\x0000Ù[Tý\x0002\x0014¼;£¬s|mÃîÖÉKÆáNXj\x001e?v×"Ý\x001bß¯\x001e?ïéÇ3XòiS¿À
§ÃYM;·\x0016Çð
å÷Ëë²\x001f/Ómõ4þÈ®~e\x0004o_¾®\x0013çîÞàh±Õ\x0010UÛñÅ9ÎRÿ2¶ï
âíÍò~P§\x0019×\x0012×lÏðowÓ\x0017×ñv}qmÀ®o\x0012ÆïºYº]ÈÃAøaw3´=h-Û£JÏ©íPÃ\x0001T!½1\ob\x0018<<¶cÛ>¶mÇîüËº-_wöÝ«÷BÐ\x0000­õdØQô°ñÏVl§¹á®3¢H\x0002ÿA\x0004ÆöÃjVl©Toáèþnæ\x0018³Ñ\x0007ú%nô	'îasj=7ÊL÷î'øCçO°þ
û\x0004¦øwRv>X\x000cÏP9Æ|&71TäÝ¢¼]Ü£õÞr`9c©\x0012KÕ`yÊê`\x0017/Ï\x0000VÚ\x001c\x0000K\x000fZðj°t¥k°d	,é\x0006wwÆ´}
+±\
ËpM\x0008\x0000ýÖ\x001a(Ô`ù\x0012ËW`Á:)\x0015E+æhQë\x001cFkó¨Á
%V¨\x001bò>¢ÓdÌC^q´\x0006	\x001a¬XbÅhqu`\x0017-O¦y6ê\x001c­í³e\x0005Va\\x000b¨àR
A°m,OEzTÃp
\x0012\x00035\½\x0015BÖ,\x0011)½êTJ\x0017\x0019\x001a*õÖ@\x001e©bm^l\x000bD\x0005îÄ%u\x000eÖ1\x001f±·@È\x0015B
z\x0019Å\x000eõü\x0011mÊîtñjY!býÝ\x0007~(<@Ï{åw\x0005+½k|³Mm
Ò+EÛäðPB]ËÂ;Mlª-éäwlNÐIz­Ø[ÈvÓWÀé\x0012NW\x0007.-c\x001a3Ê\x0003'#ÃKå\x001f\x000egJ8S	ç(\x0007¦ñ+U\x0001¶\x000c7Þv8-ál%\x001c¹[áí¾)éR#ÙÀØ¬Ìd®Ì:V0öäoJg]gå³Áp¾\x000e\x000eVþ¦>`akÊpã=)Ã\x0012.Ô~S²KU­Éñ«òd°\x0013º\x0002¢Å\x0012-V¢IzPëüÔ\x0004³¹Ù&\x001aÅ\x000fÛìíÝò+ª¿jº]©\x0018É\x0019?*O¡Ï_%\o\x0015µË<#\x000fÂÔ"³\x00159ØN\EJ\x0013º´°VH
¢¤Y±Ù#¤ÏëI°RÚÃ((9¤rc\x000c~hEsvþáWìªÍ÷\x001aý8ø\x0004¸ác>°Óéú$$\x0011âhsãüü\x0007lªÍwû\x0011\x0011¤%¤µxá¤fVãB ¶e+©ÂTÄÑS@q"Õo·íPMas\x000c8þç§ç_öeªP3ÞÇ\x0000\x000c+¹±\x0008N\x0007~ÄsÃ\x001b)}çó+<GÝ¼Û%\x0013ÈºÄÔ-n\x0011F#!Lê\x0012Î\x000c4ãZ0MiZ0
\x0015ÃC4Ù~ÛaË-GspÙ\x0019ÁÜýÅmÉh\x001b\x0018Q´Biy3vÚs
Ã\x001bÈñ¡t%¦kÀDU6\x001eòL¤âl\x001dåP[«T2W\x0015t2ÔCêÜrk´WôLï°À_w\x0006\x001a\x0015±\x0014zË¥\x0013Ø\x0018Í=~ùúøq={³~ùeß£ì\x001a
Ç@É·\x0018yú\x0004=(uM®h\x0017w÷\x0017o\x0017³7å»\x001d:\x0019T ª\x0005ÔF.$ë\x001c\x001a\x0008Ô0¾\x0008f ºØ\x0002*û\x0011m\x000b©Åe(4R\x000e§QÐ\x0013Fsu¤.¤.´ÂLdÞ§Ùø\x0016vp®Ñ	~´Í¡4öHc\x000b)®òd(\x000c¥?dd\x000b2\x0011ìIi\x0010%i\x0010
¤¨òN\x0015\x001bAi2+Áu£\x0014Æ\x001b"öIÇ»\x0013¦Ìþ\x0008i²?B]D\x0003wäÀ\x0014 Á$=\x001f@ì¨\x0000UeD¥ë£º&Tô9×ªèA\x0004>~`ãÆáH\x0003ªR½¯TË×Çå4Y²\x0000ãÔQT#)-H¡G\x0005Êk¾¾Ò}NÝÄémþú°zZ£P@%q\x000es-!Õ¶ÚôõUîÀAÅØXÜ\x0011ã c¤: ^÷(½n C\x0012õfÂ·g.½í\x000bô\x001eòhjÑûðøg\x0003§X6Úqâ#J Pîr\x0014ÃF¡ã	Æ-¯aø7{ê\x000eK\x000föHX\x0004ª4Ü/È\x001dï^H6°ÂG²\x0011Lj\x000eKoW;t,2ª.Qu\x0013j\x0014Ù\x000eÇ²¸\x0017\x001b1Å¨ùH=©)IM\x0013)z
§#T\x000cì\x001cï;MCj»\x001bU/©Gu%ªkCU$\x0010uR\ÚÑ\x001dÏ\x0012ª\x001cU¬©G
%jhBÅ®lrló\x0014µÞÁ	IGWÒÃIáûô\x001cº¡°ijëj\x001f?<x~}\x0002ðÝóßËÜåìðq+ÝKPù\x0015lÌ@è[Ûº\x0002âóóK ßá\x0003ÈÈªDVíÈ.k,\x0001²fä,
d\x0006O9íÈºDÖíÈþ,¸,#!o4xN\x0018eS"vänYÌö'E¶%²mG$HÆ2!SYÒ\x0007+]3rlîÝ!\x0007B'\x001cËÂn­\x0018øC¹b¼Y½ì7\x000fP\x000f²Q\x001bÊ\x0005ÁñòN\x000cÌùf¾Üå\x001céTI§jé,÷@¡K^ò­5&°hÏ Á[\x000bgJ8S	'"ù|a3&£vÓØ\x0006o¨µt®¤sµtÓºÑ°½¥A_\x0015Æ\x001b´Öâ\x0012/Ôá9tMf<K×gtÉbK¯¶Ó<µx±ÄµÑ\x0013´\x0017\x0019ìz\x0008¢\x0007Þ@Ë³.?m¥I+j£§I!\x001dð"åì!z|Â\x0003¼ícs-_oÚÊÊyëpÅOÒÔÐ1f¾)±­Cùz_WV~^\x001axô	ÌcPîv \x001ffÔ{2þÐ?ÆaµåÝó+Ü¬vBÂq%¡\x001cf°Î\x00106\x0012Ô,I{HP\x0003ãÍ\x001ew7\x000fËóé'®êKTßª-%m\x0001Õ¦ï
¨\x0005áÇ©ùR\x001aKÔØ\x001aØÔ'(Z+\x0001Õª:P7oBý\x0001Ð6\x0002`[!¤¬\x001b\x0012«ß©i^Çª{¬º
Ç¢\x0006\x0012@uì1\x0017:×m¨¶jÛ&£m¹.%\x0013EáÇéÃYÕÄ*\x001eáirá\x000f-Áµy è$\x0001Á\x0019xr/ï\x0001fs~¨Å¿ù§ÿôF¢èÒNÏ¯ÿ>»úëÏ¯«ÇG¸&¯~ÞóÜ-¢\x0017xÖè²xÞ?ß9g\x0005+7\x000fÿ6»ZÜÏ/\x0017pM¿)å9¤Võµöð\x0007N9½_}ùðÑ|·ú´ÚOÖE\x0016ÕIÈ¤ÅÅ ¶F¥ÞÏïÎo0ïæWóéÏN¹é¥cdû¢*HC%\x0003ÞZ>X\x0002%IKÃ@\x001a´µÕS
U\x000eÎ\x0014M®\x0010©`
2Ð9\x000eXeNàhzï\x0006ÖÑb½ÃXqd÷\x0015tàR\x0010rö÷ç/ëß~]®???î~©µ°ò³ß	\x001eLw}¾=üÛÅ4QýýænqûÃìrq}s±ÃºqU«\x001aq£?#Z\x001f1ßÑFG\x0007ÐzÛVZSÒÖà
| ïp!Ë\x0008f\x001cëN\x0015\[âÚF\l·4\x0016ø5\uÞ`4\x0016F_\x001bZp]ë¾õ±\x0010JÚð­ÒJÓÀ\x001f²ïùóççÔ}³zú×êÃî±-Å±\x0010:é\x0015\x001aó4Ø2\x0002ûÃÍõMÊê¾_þc~¾\x001fÕ¨¦
Õ\x0019¥·Ð5RlF9úÞ\OêJR×Fª³½g`¯6@¥t\x001d¶nÔ¤¾ÔlÕ\x001e\x001ce\x0016á\x0016\x0018²Ïô¨\x0007z5i(IC[L\x0005»h¡¨!\x001fµ\x0003x ÆÑ­jÔr\x0011¢f+ôÊ¨\x0006Ú\x000cUÕ¥ÊQ\x0015£5p\x0007³ ú½øC)¬÷:#¦Ýy\x0000TT\x0015$^ã\x001c\x001cºR'¸ÈN#~¨\x0005K"+\x000f3úqW®9UÉ©Z8a\x001aAÏf{û¥ÉïÝª^\x0015§.9u\x000bçf9Q@ö2Á\x0005:ý+?ì@ká4%§iúî\\x001d\x0016Ã%u\x000bObe°¼\x000eêÖ[(mIi¢)7ÑdKI&¿{øáõ¿Ó®ÓÄ<:}V¸pÔ>!'¥\x0016ÎPr&NuFÞ#ÎqK@Éñ2\x001a¯ÁÜ$v»EI4ÆÓÐwG*ÅñäUiÒÅû\x0010P-L_ù	è+?]=þçËúq§¨\x0015X°Ü
°ÆZ\x0002£¬\x0016\x0010ÂàÌ¿é\x0003¿º¹þ~¹¸Øá)Ê¦Ä4ß,¦+1]\x0003f`E m¢ ³ñ:ê\x0019whÙdÌñz\x001df\x000c%c¨gÄç¸ÖÇLI\x0007h¤£.©¨ã´¦ÅÞ8
µå°?äJçÏ_\x001f?wç»Õãç¯[üûëoýùòÇ¾,¿%Wk"÷ê,X%aµ\x001am¾¸¾¿¹¸î\x000e"wóëûÙâß\x001en\x0017Ë\x001f÷³«]\x001dÅîµ£4µµB\x001eµ1}\x0003Ýðâ8v]²ëãâ\x001e">$§¸;|\x0018H¯?\\x001cév0Ç±Ý\x001c\x0017waX\x0010\x001eã®èåÊnÂ~Rr[Û#£®Ñs0Em[Ñ\x0004*rÔG»ñÚÙ]Éîc÷$ êùÆhà\x000eÂa\x001fí5kg÷%»?=°&¿¤û]ð*ã\x0007sÇ±=\x001cÉÞùutqGey©N\x0012Î£Í\x0016Íì±dG²\x001b6Æ2-ùÝø\x001c÷®2]·3ãàáh\x001eLm§¬@Æhü\x0004\x0005\x001f¯$nïo«Gî«Î±§5®©øÝ\x0018ab^$GÊá{ûª<ncu*P9D>pÕÎ\x0014.:µ·Ã÷6VyäÎ 4l¦×\x0016\x00186!G~ 
{\x001c|oGnPX©b\x0008Þò"¯=üÀiì¤¼ì-òòÈU\x001e¾Vå\x001dJj\x001a61?P"j×Öoû¢\x000cüóúi'§×p
`\x0003Ñ²*òNªÂ¨CÌ-@^NUûû~ÛiGd\x000f'òtPà\x0002aÏ|á
\x0018íxÝ4\x0002í+\\x0005\x0013û{\x0002\x0013/\x0002\x0000Åo\x0014*ZÜ\x001f\x0008åK(_\x0001¥yO@ÝÈô@iU~ Ôb¢\x0016þ ¨PB
¨@rù\x0000¥¨Ò\x000c"EG9ú\x0012} R,b\x0005âk\x0014!\x000fqNH­\x0006yÃ¡6\x0013\x0008Å»üAT¬æ\x0007TÜn9ç-±9¬\x001dJö d\x0005 ®_ÚCÅuZz\x001dH¥zTª*T©8\x001a¨ìr\x0014*¾\x001fj=\x0010ÝO¥¤íWCã\x000f@èVúÙ{ø?YÞÝæá­2<àá²zñ\x0008g,yp*1.{V÷÷\x0017×çëé&\x000c©JHU
M\x0012ØÑR´uFç\x000cöÀ\x0014v\x00089ºÚgB]\x0012êjB\x000eÊ]\x0014ápB\x0019v»y\x0003\x0014j´³2¦d4
Qt´39lKù!bà×
7jê]\x0013E[\x0012Úú(Zs¦Ó`Ä¢µäCm5Û}©®çúè0º\x0012ÒÕÑgotì&H{©Ó£è\x0007uµQô% o\x0000T-í°¯v{§¸:Õ»Q\x000fÅ\x001aÂP\x0012zBø¸Án\x0008#\x0011òt9\x0001a,	c\x0003¡$­\x001d \x0014ô\x0002iÌo<n Ã\IX¼<[wÞªÏlH
°»¡:I\x0003Q3"Ö´\x001cØß[ê7\x0017lÇ6üÞ,ÏhÙÖ\ÑíÕÀd°°·±ÈÅ;ê¸Ë¦Í#íÆ\x001foÈ¬@ô½ úú (IKÎ(¹µÑHj¼½eð\x0010qø¢ÆEý×1øj\x000bÖëÙrõøé9½<¾¬~_í9éDéhÖ`\x0008É
ÏÆÜå\x0012Ä ½*½ä-ç\x0017W7éåäb9?ßq\x001ac`U\x0002«V`áùúèEÈ\x000e\x000eûaØpÕ«K\ÝË\x0012A¶S\x0000£ø¢º5ÅwÂÄ¯\x0001ØÀ¦\x0011\x0018\x000fCã\x000c'--Dë$å@£\x0019ØÀ¶\x0015Øåk
Ö ¤þ@zÐ\x001cáÁA®\x0019ØÀ®\x0015\x0018nt¹pì\x0007¼¹úP\x000efy}Éë[y­#µÓn\x0008'\x000e8íÑñ	ðÉ\x0002\x001cJàÐ<"\x0014^ÙRáäî\x0001Îª\x001ca=^íQ\x000f¼¹w°h%6j_$NÀÆoOµHÈþ®Ñºm\x0004´&¥jjôµ!âèxH\x000cRÔÍÀ½]C¶n\x001bØIEõ.9.ÙÀÞU\x0010ßA2­\x0019··\x0008ËæUX©µ4Y´í\x0014#âg¹ÕýF¦æìM7Íõúõ÷=}?\x001eû(Ó@Q'eZ\x0005ÃYñýÏ\x000fî¹æzñð~ØH¹TÉ¥¾\x001d.]réoKªìV¾#þ]\x0016à("\x001c:Í\x000bêædÓ/T\x0002Ý¾ìA\x0013Á­2Xô¯!
ÃõÙùú÷õç}vEÞjÍw\x0012\x000e7N³PÁè»\x0006\x0014/Þ/®¯wÄ¹~~\x0007¨ª\x0001aùVTúl#5mYã%#Z9*D{\x0008"\h¶<ºá²Ãèo]éó_Î¾Yýòüyõòq',\C"íF;AÅ*\x0004º
§GKÊ»î\x0007*þ~9ws=_¾ÝO­Jju\x000c5ç\x0013ÚQí
²üSâªÔº¤ÖÇPK6GÆX§¼\x000ePkÖ1Õ\x0003gµ#¨MIm Fa\x0006u \x0013\x0015bYS3\x0004h¤¶%µ=ZlF¤I¨BDÛÓQ»ÚµSë(ÏXÕÐQ\x0015\x0016ÝÈÐfôQ¦\x0011ÚÐþ\x0018hA;EçÅGþqp^ÍKÈ¨¤l#u(©Ã\x0011ÔøðL¡öô>®È?¨\x0014>á %s<\x0019ÎÙ,ºÍ4\x0015µÉ®«£¥[mÔüf·Åc°qÛË±¦îE8¾ò°¶£=·Øýñ­\x0011ClTÞd$E[Z\x001e#æcDö¶FyÄÞË]äh\x0007%\x0003lÕ²Õñ;:¦ÒûiGôÈ\x000f½NÝíëï_ðsþ+\qöÐ3(\x0019 à¡}FKCNp\x001c­~&ÁºÛ÷\x0017wxÑ9ÿ\x0001î9;ÏP]ìê8vk¨¥ÄX\x0015Ïß½}Ø^\x000b».ÙõqìpÒ¤\x000bm$\x001d\x0001µTÕÅÙMÉn;{ÕvFu!¡»ã>6C@w%º;\x0012ÝW\x001c=P\x0001\x0006\x00196\x0003\x000ebôê\x0008øPÂãà§âmçV\x0005\x0008¼d-ña"û8ø¢Î\x0005\x0017\x001aqäJcI\x0006\x0011è]Ê¹ÂJãC?mäeo¥G.5íé\x0000Þc¹LG¯Yy8Ñ\x001bÛ\x0011ô½ù*°h]zè¥Î±\x001f\x0015¡?¾7eåqsÖÆ¬\x0013Ã>9¸H±Y)'*¹á{SV\x001e7gmT|ýDçÅô4¢Ed_?QñU
ÏÞÏ=)úíÎW×/¿??î=\x000bs\x0012çq\x0012S=TÄª9¢Üà\x0004\x001b\x000b¯.®\x0017Ë÷7\x0017\x0007pêS·pÂ\x00159Õh\x0003§ÏÕñÜR\x0001\x0002ó\x0016N[rÚ\x0006Nô\x0000\x0008>s¦£¡Ù\x00172çd»s\x0005§/9}\x000bgôªÛqØ¢\x0016zÃ9ÙH\Á\x0019KÎØÄ©ÉP¬ãL­FE§2çd#ñá²?Z&Å+næLý\x000f*z\x000cbNöçV`ö¦lGÖ\x000b.pÃÎ|R7Q\ß\x0006}î\x0015½i$æ\x0011Ü\x000cmÈ$g©¼ÞÌ÷\x0013¬K²7dÓDÂQé3(Og6óh²¼³7dÓD²÷J©ÇEYïOÁ)¬Øzw°¢xw@\x0001Î\x000fë§çÏ{ÜÛ:MKê"í3¥¹
½\x0008£¾c\x0004çùâòæz{\x001b#ª\x0012QU#JÅÕ\x001aÀx\x0016Ò¸UÊwÆûê\x0008uI¨ëØ(w\{	1$HéÆïÉu²\x0010£O­\x0004+@\x001d\x0017íãI/Õ|£\x001fõÏøaÕÀá¤në?ð|³~ùú²úüqv¹úôüú²~zÚCj0YÆ¥z0+¬\x0018Í¼Y,ïóë·³ËùÕÍÃr\x0001³i?®.qu+®e)`«å¹.
\x0005J+\x0007s½\x0019ØÀ¦\x0011Ø*OfTXÈL\x0005/\x0006ÿ"`;ÚÃÖ\x0004ìJ`×
ITÄ§ÑU¶{ËÎ\x001fv´¾¹Wö\x0002,#\x001c»îº®36°~\x0008\x001cK\x0003w$ÛÑ;a\x0013q/Â²5Ä°\x000ePÊ¬ëåõt@åI7ÑÊÛ\x0004\x001czÀ¡\x0015XI®ÚêöZ\x00026$t6©§u\x001b»*$f·ª\x0006âÈ¥¨\x0016\x001b¨"50rQ×îØÍ¨­u\x0018ÀuøöiõK|¯WÿZ=îQ]M²×JJì¨ª55
+\x0007}K·ós.ò½ÿc~±ÃÜ5ê\x0012T·
ÇÉ#eÈG¯ÂÚ\x0003@\x0013¥-)m\x0003%Ê¥"NX¶¸³\x0010ÎÔ1\x000e\x00049@}	ê[Â)Cý@eWEÅ(\x0002ví1ÚÄ\x0019JÎÐ\x0012P¸ÿBÝ!µ Â­Î®CË1Ì\x000f««Î?x
3ñÛF²\x0007*¿aR\x0011JÑãôõñÿ=\x0003`\x0016þÁ±·òã\x000fyå?Z½¦$åo¿íñ\x0016Öe\x001b\x0006\x0007ÇÄôt	'l2Ù>¿?¤Ääíí~HÓ4
Î³Ío\x000c|`\x0007i4{EÄÑË*J)mI)YÉ \x00063c;\x001a\x000fQC£2{VÕÐ6©RÉþ\x0007-Á´T\x0011Ñä9R,eöÝíÊÅþö?\x0014yè«Õ/\x001f×OëÇ}WA©1Óï:CôH
¶Ú;¶Í:''®æïÞ..\x0017\x0017;n\x0019Qª\x001e\x0011ÂèÉ6Röl½D4b¼ \x0006Qº\x001e\x0011®û*R\x0018\x0003ìiÏ¥+Q\x000f^;ë\x0011Mh\x001a>´À\x001cnPÐ\x0008qpqªG´%¢­G+\ðÒ[C!ázFW2ºzFÉT7ãb iø¼6[*\x000cNîõ¾dôÕ\x0002\x001fòèS£_z¿ö2qàúP\x0018JÄP\x001fFCNôXÙñyºÃ£-Åñ1%`¬!ÜÕÉ:Ã\x0005KÕh0þ\x00023\x000e
ª\x00197EhÝÚ-\x001aæ´¢jq\x0008¤ã÷fo]^\x001a'\x0014k {«·lX¾¡\x0004\x0008@<«çÅÑ\x000cjíë!{£lX\x001d±\x000bÀeHAÓZsS4\x0013]5½¥G6¬=¹ÁÒ iày\x001dØ=Ü\x000cg\x001a6ëâPN\x001b6þP½gwÝs	U`Þ\x001eQ\x0003Æ¦Ï@vþpT+]ÿèc1´­]®~ßc`\x0005vR¦ÆDXw<?F\x001b(W/ähÏÛÙåüýN7\x0004fS%ªcBÒÁ×h\x001e¶h=ié¡\x0012õpºÓp\x000ec\x001aÁ%Ã\·z´%½\x0002Îp¶\x000e\x000eûÇl¯Ç'Öà\x001c\x0017H=hè­%\¬3ADË\x0015*ÆËôá:gÅT bGû#\x000egýéP3\x001fà

÷ütU1pòJï\x0016\x0000ËSýxWÏáp½!'kÆ\x001cÂ\x0005.±F¹4æ\x000c¼îyäg½1'k\x0006\x001dÐ¡\x0000}×È®éN)ÅG^e+è|Î×Ñ)©®.J\x0018r\x001euØ·@t£ª:Ã©Þ¨S£\x000e+µ¸*Ze8Å\x0015grÔ\x0000¬\x0002®7êTå¨3,¶f¬eÑgø· ]éÊ·\ÚÃò[îk÷ì+\x000bGVÚÆàÂ:?¼T3þÏ×Õ×õK\x001f~«!Í5Æ\x0018\x001a½\x001d)id	?®2V\x0005: üV\x0010[m°"½\x001boV¿}}üòu=;~úyý²[rÅJÇ²»>y¸Î¢·Â\x0002\x000eTQó®\x0005âÍüöþâî~1;¿¹ÄÇ¤	q\x0018\x0002}àfb\x0013
W{i#V\x0017!±âÞ@=q¢\x0019GÞ\x0017æÍ¤Gj¥ÿPû\x001eµo\x001f\x001dÒÐë­\x0017Æ õO7:\x0002
3ZÇÓÄ,¥îÿ\x001e¡Þ$vS¨{Í_±ö¼¹:ìp§<´eûZ-Æ½°á\x001fWbã­Ø\x0010d6Ú×$'[­<ùA£ãê© Ñg®Æ?ÿ;\x000c\x0018ûØñX{²äDÙ|²0P°×d×àÃ\x0017ëÝÔ6S$êîïæhkImþ\x001esÛÔ9¯,e´µ\x0003×iî©·Õ
÷Oÿ\x001cÿ³\x001d]P÷\x000e\Z<Ç\x0001'%J÷\x001e\x001drøßß~Á\x001f²Ë§Õìüeýá×Ýi\x0012¸\x001aH>¿¡Aoz\x0013´%³` ºó%\x001fáóåâü\x001dïX¨KD]H
-xÛO÷B¸¨*zh\x0013rh |(\x001flÔ[ðÃÆdæãËzvµþòeõËzÅ%®\x000c$Ð\x0013¬¦\x000e\m%\x0015ØÊ\x0018&tØß.\x0017³«ÅÝÝüÝbúô1U©\x001a0màÎ6:åA­éF-ok1u©\x001b£(=\x0016%q0Y\x0019e´_²\x0016Ò¦\x0001\x0012.;iãEé(*QC+fzZ\x0013¶\x0001\x0007QÂJÝw
Ä\x001f\x001cÞíËúë¯³Ûç×÷Vza±\x0004	LÀIL
\x0015`\x000bc³À0°7§[Åírñýâ~v{óðfg¡\x0017ãn:Ù\x0010ë\x0015kyñø²õ.J25\x0000ÞH[\x0015ÅTjwôja]\x000fÖ5Â
uà\x001d,Ð%\x0015\x001fï-³\x000bj7Ä¶\x0015§áP\ÕëFD\x000c|hô^¤\x0012\x000b¤æþ\x001f?9úg8å÷åà\x0007\\x000bÞ>Z¡ÝÂíúëãWª°Á\x001dv'pD!¢ôäé-ÖtKw\x001aBÐµy\x001bøíÍÕ\x001c\x0016n\x0017÷\x0017÷Th\x001bìé=ñæÒ¥\x0017KÚÑÀ(½/zå=å\x000b\x0003¾Â'`\x0015åöòÐ\x0006¬z\x0001VÍ\x0011F¥æ¤óê5äá\x0012¤¡Ü°6Ã+}\x0013°É'Ä\x000e\x0018ÿl$FS+\x000eY"U\x0006¢Ö£¡kÏ°£e\x0012wræÉØ·oÇ\x001fx\x0011¾~üð×¿ý.¸×ëß>ìqÀêÉ\x0002×¸È§\x0018¥µËå\x0019£yÆëóÅí\x000f(\x0019q}±¸=\x001fj~eFS2fÆÈu\x0005|ÁwÌ8Úq8£+\x0019]#c Ûãî4\x0004b\x000cqt½=1¡1r
0>KB\¡\x0007¥\x0005UZZ´0Z!»gîT­4NÁJ/\x0006pº\x0019Ûc\x0007iªo\x0013Ú\x001e¡m$Ìex/IÏ·Jçf?ª/u\x0018 ë\x0001ºF@\1ÓËO²Ø@\x0017¸À%^ª\x000fÃó=<ß\x0007[Jõpmg´Þð\x0019\x001aøFOú\x0007ñIÑãÃ?â§;£0\x0018Ôè²&.v!ö l\x001b&\x0006Í+bPêÏQ÷Z\x0012Å¸Õa¦7¥iÈÆðã\x001aöþyÊÄËÀ×ãæaé\x0012Ð6~f¯yç\x000bpýÔ\x000c¶ÜË#Âa;ß(bì#ÆFDôç!DOßØ±@´£b%»ù¤T}\x0007Xü\x0001\x000e\x0017~4¦¾|ÝSR^\x001f&\x0015-y\x0019Ñ\x000e\x0002ßä.\x000cN8\x0017W·ð/1stw¿+)£ìVRFu\x000e¯Ulª\x001c`q\x0016T³\x000blt¼ÝAú(8SÂ:8\x0017©Ø\x001b®\x001fwN\x000b´bÐÜRÉfK6[É¦sàÐò1±)F\x0016CAýJ6W²¹:68ÿÑã#lhd\ê\x0011á\x0006·ÂJ8_ÂùJ8C@Þ92NpÙB
5¨ªd\x000b%[¨bÃª\x0006G3\x00150Ó\x000b¸óyÐ.¥>Ûè}Iz·µÀ\x000få\x0012¹ïV/û\x0005sµKO´À'1¡RUÂf¿\x000cF
`\x0006DÑÜwóåhî6¢)\x0011Í7èJD÷M"	\x001eúØøÃ·Cj´í{¡à\x000fý\x0017»ç×\x000f«ÕÇ}\x0007+¸»¥+Ãï$¤w$zÿC«çÉ¤þÝÍ\x0003ü\x001bó·;Ú»\x0018T º\x001e\x0014\x000eùmP£Òä{\x0012I¦ZÃZPS\x0016PÍ
È\x000eý\x0010£ï]  £çýjN[rÚ\x0016NØõºC1ÛgÂVY
çxÑk-¦+1]\x0013&ky9Ã¢\x000fx7¡´®H×rúÓ·pzKÖË\x0016:=\x001a,m¦f"\x00124´\x001aKglTJã\x0004XUì@á&5¡îR\x0007\x001aKÐØ\x0002£"\x001aò³³aµN'\x0000Í\x0015 i
\x0015MSÞP¯\x0012:\x001fa\x0001hò¬êcÍ Ý¼´¿Ú7,÷0Ø\x0001f£¢hexA÷E\x0013§êqª\x0016N\x0019ØF\x0013\x001d©i
uÔp£PA÷\x0014 ½]I6mKxNB^ÆHN\x001a?½8Éú${ÛlÚ\x0004K&9\x0014îuBñ<ï'ì$*A{ûlÚPfB
\x001b¨õÛ\x000bÔ\x001eQ\x001dhog
[\x0013>|°8\x001a,Eg°P½^­\x001bÕ'­&ííM²isÒì6\x000c¤.m°@±û\x001dO2Wö6'Ù°;¨#\x000b
\x0002u.ØñÂfÒÌüÞî$¶')Éw\x001eæSÈ\x000fI7|{ó¨ê­ùªíïÎh)M)Ê4ïY²ÓÆì÷ª·ªµ´{örDA/U\x000e¤'ùª·D©%
f¾Ájôí=?(ÏÞ<6êüWöf¾jùÝ|"¡I\x000b\x00036y:êëkïÈ/³XB[ìøÿõ\x001fÿyóôøûã"\x001eoEàâ7T:O\x0011ñ\x001a9É:ZÇ³Ë÷\x0017»Jx¶5´½Ú·Ã\x0019\x001d;­ *8ù1\x0019Ï]ÀrJÒ¯Ñ¦\x0011»"=o[þÞÖ¨, ÍX\x0012½\x000eÒ¶\x0001\x0012\x000fÉ\x0014GC"ÂÖHÃï²bTý¤Ñ®1`R8Ç\x0010ÙÈ#\x000eÝ@ë\x0011C\x0018\x001aÆ£öùyÛF.È4ùaV
RÿÕ\x001b1ú®R^´@<i,{.XÔéÉºsdÊñê1BT½0ª¦8æá¾u`ü8Ñÿ»\x0010¯½,\x001dþY:N$ÞþúøôøÛoXqsþòüú¯Õîjf8¯Eê·UÃV7qD4)Y'Cðr*¿}ûÃÅåÅí-Ý/o\x001eþ1ßa´ÌØªÄVÇ`+*{\x0004lKï@(Õâ\x0019ÛNeA[°u­ÀFA\x0005°
7t\x0008½\x001dÅ \x0007ì\x0018lSbc¢Ý1¶LÔ:úL½½K\x001dCmKj{\x000cµ£\x001e| ö$\x0015±\x0007ËÄ1Ø®ÄvÇ\x0011qæ7±&j+6Áz\x000ck ½	)ldÖ-$\x0016\x0012í7\x000bÉ	¶ìE[\x001e\x0013îÿ_¸:ü$`_âÁý\x0006M;º¿¿»}ùëÏ/³'ÔüZzìmß½üõ¿þµç%H:lDéÎe\x001aýF»\x0002\x0016\x0015°\x0007Ô\x0008ä@½øv¹¸]¢ø×âê¢³¶}·\üc\x001d\x0005s-ns\x000c·\x0013¤*£C\x0010é¸\x001d«ÊH?¨¡äjýan+ûÜh¯ÝÊí'ã\x001b,\x0005K÷	ÌÌ°4\x000cÃQs¼Ý\x0016·;\x001bå\x0016ÞGgÝÊØQr¸Õ@­Û¸îSn2ß.Õá¥£Ó¿¯;³ÿ±~ùåuý´Þ]ý\x001b¼ëº\x0006±ú\x0017çdº¹¹;Í¸ÇÐï\x0017ËÊÿX,ß=,.\x0017ÓÕ¿ÒÊ¾a3þPH¼|¿þüüú¸ÛXÚÂþnÒ®{ÚÜ\x00141zGqÕb<·ð0û~q}óp1í'ñT§jñ"54¾Èzªø
TV\x000fx\x0013Í\x000b\x0007ÓéNWÑu\x0019$R?\x0010>$:G©c¡å\x0008ÍÁx¦Ä3Áa§N±L¥\x000eÖ0Ý±p¶³±\x000b\x0016~\x0003=Cµåq§¦s%«ý²Ó.øä¢(vn7!\x0019q0](éBåUôÝ1ûÏãÎàC\x0018Ñí³ãõ<¶ÑôìÖ\x0013Q;c5=ówlæÏ£N¿¥\x001d\x001e:Ù[PdÝ\x0002_ý\x0002±~[óåfR=,ÓªÅëMYY7g»^IV	\x0013":är'{BÖÎ
¬[¤Y\x001bà{²g®\x001eï\x0011©áëM\x000bY;/àZ
¸¯u|QçI;!2´\x000f\x000f\x0006Å¬U¹
÷rýñåu¶|~zzÜ}$ð\x0016öÄgM´ÖHÅnÜárñvù0[Þ\^^L\x001f\x00052*ùT=%MLkÐúÖ\x0012")\I7.\x0019\¨KD]è$ûïYX\x0006±\x000e¢CôÇ.\x0016?Ô!\x0012ÑT#Â
2{ð5é
Yk7f\x0016£½:D["ÚjD«r\x0014±::½*¸\ïåh\x0007P\x001d¢+\x0011]ý6h\ÒE1pE\x0006\x001aAP\x0010G5ê\x0000}	èëcè³?\x0010Z\x0013&@ø3[-º)Ö!\x00121T#ªÈ1}J\x001b¬G¢\x001fUN¨C%bl\x0019ì | 	Y\x0018ôx$½9\x001eq£eÓ­Ú¢>Ùÿ\x0007Ãh(Á\x001cÆ££Ø9ë6\x0017î®Y¿õ³´ò¨32ÆòÚhGEö\x000e\x0002\x0015ÆöÛ¥ñ2Å¿ó­P\x0000u÷U>FÕ^Pã1­AG\x0006O¯eñïü\x001fóËÅ[|&5%©i"5.\x00171)ª¶
û4P-eª¤
Ô ¶-¤$¢ï6Ib(»zZ3876º\x0012Ôµ\x0006.\x000eÁÄp*¸	(*Ë¤!ÚDêKRßB\x001a°³j\x0017M'gÞZvxi5Â®"
%ih©Ô\x0003è°y']i ¦cê&_¿ªHcI\x001aÛ¾>7¡\x000fôá¯/¸(ÐN>x\x001dBj´ïë
ã\x000fä¥°N÷ë\x0017þ2ûø_ÿñó×ÇÕÌ°¶óB)¼Ú&/5'Ù¶\x000c~¨õAÎ@|¿X.\x0011ÿnöv6X^ÌÏ÷Ã\x0012Þ\x001c\x0007BÄ6\x0012¼dÇJç|`øÁþ8xWÂ»#áá¦2DJFÖí\x001d#Õ\x001aÈà¢;Iäÿ\x0000ìÞ°ù\x0011ÿwÀ°Ù¤¨/W¿¬vÞ=-zCð8ÁäQÒÊv:ZðÁn{hoòÒówóéËgæ3%©åõ,Ég\x0000\x001f§£!)ñ/GTð«ù\Éçjùð¼\x001e&°oÝwÕ\x0006Ñjz2f¨®\
èK@_	:4.¥¢EPdI\x0006XIHGF«\x0006\x0015ÍÕ¡\x0004\x000cµ\x0011\x0014*Uæha\x001c=ËG]Ñ)ñè/\x000fÒ\x001d\x001f\x001e¤ë"\x00184Ý |L\x0001.É\x0011ÔGbÙÃ²v\x0012û ðLÒ\x0011ÂY:½£F\x0013è\x001d\x0015\x0008þÆ¹Ê2­2¶ö#;s£ÆÙà\x0017O\x0008\x001cØ\x001bl\x0013×ä-­>ü3\ËÕÏë§Õ\x001e\x000bgïUà¤òMÒÁc¹ÎÿexýXÎß,.ç»\¦\x0019Mhª
Í\x0005»&ñ©¼C³d#½cÕÃÑLfªÐ¬§\x001e\x0019<§¡1nÝp}\x0018­¨;\x001cÍh®

!	MåI¯6\x001f4\x001e÷AC\x0016jÇ¦±®ÜÆ\x001aÅÑbøÁ6Õ}Ý$\x0010Ud°\x0005\x001ajÊàè\x0012\x001aX¢MlÓx\x001d[o\x0016Èºi×DMl§\x0019Í¥w\x000fGëÍ\x0002Y5
ÐãÈ\x0011\x0019ëZçYvÀ¸WD­Ô¦£ÈqåÀà	×\x0010\x0008^ Ä`,#\x001e»¼m#V\x0013Âí/ÒçÅQ¨icÁG?\x0014ä8PIÓoôÇ\x001f¶Ùx~yzþeOÑ½Á#T:¢h´ÔëB(½âí\x0015B<YûÃÍòòæÝ\x000eÃ\x001b4%¤i½"Þhñ#FÃýµ\x001eÑ®\x0001\x0011ö´Ó\x0002£¡£dÅYdê]81¡í[Kb}-iµá·6ÑÅÉ.Õ!eï[ËÏIé>Þdg\x0000·Í@·(örô<ErcýÑ!J\x0007G\x0012Kt<Í\x001aG{\x001d¾Åñ¤l¨:\x0008\x0011fL{N³&ëvV}qEvV0*¹\x001aFz*åÃQ©'{U\x000e:?}îOÏ
\x0013Ü·4|tOTX`F\x0017%\x0018£­ û8u\x0014}Û-ü¡\x0010 X®~ß/á²,Ð¹Á)~û¢/?Ùê¹¿ßRÆ\x0002T% ª\x0005ÔñL¹\x0004\x0018ØàÑZ¶çI>¨Ú¬\x0006Ô% ®\x0005´l 6Ù¡Z'Èû\x0016\x00028ªv}\x0008Ô¦\x001f@ü¡d\|x}Y¿>>ídD9\x0001Ç}\x0014AÁjn¾\x0018\x0011tH\x0013\x001bî,Ó¹¹ÅùÃrñpqy\x0000§)9M\x000b§íÌZ;N¸}¢kÇI»
*wäá6 ã5GLiKJÛ@\x0019:	Ò*Üy\x0010\x0012öHb ÆØ\x0014MWrº¦¯®è\x0018)QxÎq4)«	7\x001dùä
P_ú\x0006P\x001f¥{CH\x0011eÑ(\x0000uæ$ ¡\x0004
- °?\x0012§¥ç\x000fà$\x0007i¼Ú\x000fºæ8cÉ\x0019\x001b8w©\x001c\x0013N\x0001*ÎS8ç0;Ò){ËlY\à|Þ\x0010(ó 2½&B@Ã`÷i"Õ=RÝòåaûÖ´rÆFxêoqÒ\x0006´½"X²ûüV|\x0018¢}I~ü¡¯ÇÖ\x001dæO«Ço/V(8\x0017'7A×Ùk¦\x0017eÏe*ìzýsÒür¾¼~rÉ¨ºDÕm¨X\x000cK¨ÁJ+ ²&J°Z¦&TS¢6TìcU{\x00080EÕ&/DuGAÁ~T\x001cðý\x0000ø\x000fïV_¾>½Y}øu
¨\x001fw\x0002ohÒÕHabQ\x0014aô÷n~w\x000e1ç?,õí~TU¢ª&TÅf«\x0006©®\x0017ë°D\x0018-Z¬GÕ%ªnCµt*í¤pSñ" r!\x0018½xÔÔ4Jn·A\x0003JªâöÂråÀ¤á)PmjÛP#u9\x0004ØV»Ý
I£Ë¤GÆ(\x00114K
ã\x000fß±ÒðåóëãÙ»×?w'%ö\x0000á¡ë\x00148\x001dÙÁÔ²þ\x0000¦ÔfÝ<\ÜÍÞ=ü\x0008´{\x0019½)\x0019½©gä\x0013Á0êÚ\x000cÊñG\x001fOT1Æ^\x001ccC\x001c\x0003\x001b¥\x0007´jÄ\x0017&5ê&WÃ((\x0019ñÏZHÌ0\³b«
\x0011eÉkcGë¨\x000f4Æ÷3\x000cøÃ&Ãðevÿòü×ÿ³÷\x001cÑÓ.zGtºKo;QQ6\x001b\x0019Ç\x001cîf÷ËÅ®\x001br&T%¡ª&Dÿ§ô$}\x0007Iì×¢Q5\x0013êqY
B]\x0012êú\x0018zÎ·Ç`Y !*ª]URN$*\x0008MIhêc¨ùÁ'HÂ\x0008h²Å_yB{±\x0002Ð¶>u÷ºV?úÈE%õ ­³Ð¾\x0010èR\x001d ¶T \x000cRIÒL\x0008ÙU\x0010Æ0Ödvþv¨g^U`Î°d©´£F\x0014uÅ\x0015(7)âA\x0015»9±éÝVå=ú>u\x0010¨ÞêÅ\x001fz"ëõìnýiõq½³\x001e+}\x000cùfà9=%\x000f£ñ4nà*<%Ï~{±X.\x0017³»ÅÕüí¢h¤ß¦T%¥j£ìÊ}Ò\x0003³úÌRÁ \x001c,\x001a\x0019mo2\x0013«Ò\x0018 3êQ7F2dñFit5\x000bçñÄ2)Kp`$MIi\x001a)\x001d{ð
\x001d½\x001d¦c-áÔ±¶Ä´ß\x001e¦õ[ãÒúrÇ¾ûº~zZ=¾ìá*\x001aÅ©âÞÿÔÁ¥S\x000cÆM(XÝÍîî\x0017óåÎInýÖÐ´¾Ü¶\x000fÆDãAùñ$&\x0010O\x0010í'Çc\x0012Ó4`J
¥¡{
0¦òs@4jêlQhKD[¨±u;\x001dÇe:É¼bý+\x0015Gë8p½k¡t%¥k	¤¡·®ÿB©Xú\x0007
\x001dO@éKJß\x0012KKyìàÉð
CiI\x0013_Oîâ5¡\x000c
¡Ô\x0012C\x0012¯\x0010f¸5\x001cKÜÆ,µ§}!¯V3Å\x0005©yÃÀy%ò§¸\x0018íªåì-²eÅ*N)L?:æ1Çì­D²e)Ü¹!Qî>{TTv
sòªs\x0000§±ÔO±Á\x000f¼°¿]}ZÏ\x0012ÐîD\x0010æ¬ÉyOÁ6;­X¯Î#Î¯\x0016³ôãÄ\x0013%ÃÙ\x0012ÎVÃeÉ\x0006å\x001dµ\x0000`¸0~\x0015+èöFÏ¾\x0016P	Nþ(8Nz\x0006$`Ýèy
_,ùbu\x0000\x0003õ¦w|$§£YÿÇºAíø¡|F{»u¬ð¶
àÖpË
tªÀ§)ªüD[hºÞØ0ÐÅË×\x001bîVÙ\x000fiJHS\x000f\x001bÝ[2ÆRKô\x0013¢U¶´õ¨\x001eG2ÂZÉä\x0002®9OÇS«b\x0005¤+!]\x0003¤¢bFg&ã\x0015¼èd­ãQ}§JÈPBzH#7ÒÑ\x001aÛn;È[X£¼r\x001f\x000cYìÖh\x000c)ê)±b¥¸;á#éÄ¨\x001aÁ*ÇrfÀb!^b¼ûëÏW_¾>®?ÏÞ?þõçî=\x0010s\x0001i\x0001ÂRÁ¤÷mÊàû0:sî\x0016oæw÷\x0017ëÙû\x001dÊÖv«Ä¶£TM\x001d!­2i£ALª¤[äèÅ¡
Sf×\x0014L¶x­\x0002Å\x0012þÈGé}\x000e>ÖkÚo¼\x0019M\x0006Uq*ÙãT²3\x0006¼!"¨/Î	úîntc¬ãT}NÕÂò9c*Ó\x0002ÎÀ;¤s£'ó:ÐìK@Ù¶. Î²­*¬\x0017©`\x0007@\x0015­Ih=¶OöAGjL\x0019û±Ò\x0007Ö:2pÑA_m¤d??áìh *Zõ@µj\x00025Ì$
^Æi\x001eEïø³\x001fiûÓÝ6Mw«-{7v\x0005¸ixÂ~Iñôb´¨
Ô^<h§±Ê
Z:Æ\x0004=\x0015\x0004*Guê@M\x001fÔ4*O~0¦\x0013O\x000b\x0013ªp\x0011¨\x001a­°¯\x0003u½OÖê`©äÑÀZ\x001ey\x0014ªó£Õ¸Oxçûáô-áÔú>	y¾KÇ~Ô^\x001d¿Î»Ðfh¦É×\ì\x0003éÞ\x0000Täy4*yx0½î\x0005Óë¦`\x001aÁ£\x0006âªR4Ed÷v¯D¡?ÛCÓl×Ú°\¡EiÜ\x001bÄny>>Õ\x001f\x0006ªÙº5w\x0003 u+=_¿vcWÏ¿¾¬?î)(ÕG`
Nz9ã\x0014o­æ·p3¬Ì¸y¸ïÊÆ®n®ï·;J
ô¶\x0017´&/è:LÔ\x001b$æä%vËuORÁ¡ì\x001ebjióCÌñþämOhMÐ¡\x000ch\x0012\x0016ËGÉBØqý\x0008Îø\x0013DÒ¦!XÁd\x000b­à$ec C
¹ÚHÚÑÖGÒ9ÉÅ\x0005\x001eÎqé\x0002ì\x0002í2êaµ!®¤tõ\x0014°ü$32\x000fÿ	ÒH<&×¶ÚHúÑ×OoôÔ©ß\x0007\x000e[TÝü0\x001eYàPÆ\x001236\x0012®é<&
eeµ)¥\x000e\x001c©Õ¨ä¦ñº[(E\x0003c0d	[%`#Ù¾ë\x0011{ZÄÞÔ
s[`\x0017¬%DK]ØÁvÎÔq`ÿ^
Ù5²eÚ8>\x0005\x0003¤K¯Q\x0000é|6ÃKZ-dèA\x0001é(\x0005\x0007\x001eusÓ¤Äv¨\x0003P	©z#RµH8òzdd¹;zÖCÆ¡Xs-coHª!©ÙV´cT©ÞjBÈÞT-CRwÏ\x0012\x001d¤\x0012g\x0018©\x0010\x000b\x0018ÂÒµ½\x0011©ZF$&µÌ1íÛºÇO\x0002©{#R·HÕ\x000fdHd~O\x0002Ù;Jê³d'lN«¤R´'\x0006ÔÙbÈ¡ÜB-doÞèy\x0003g³@óF\x0019Ò\x0002È¤hÃêóC!Ø²m\x001f¾K]RýÒë·Ï>=®_öÔ\x0015`L°ôÄ,IIW(©,¿1\x000f\x000ej¶£Û««ÅrG¿.sÓ´p
n*Æò\x0016vñÂs$s\x000eæ-¶ä´-À$\x001a%!\x0010FGÄ9PQiÁt%¦kÁ5Ý\x0010e6R*fÊíco\x0003evÞî(±¦\x001e3r}­ì\x001ePitF.Ô@-\x0013ª\x001e¨júìöf\x0011\x0004§Ñ	cg\x001aä[8{³H6M#/I\x001aIz#HÞ@(ÏÞ[jäãá½Y$[¦V¶JO\x0017é\\x0004{|àï>ð\x0012háìM#Ù4¢§f\x000e'õíjôÅ\x001cÏ\x001díïú\x001e¨oúðK°»ÐÐº\x0014\x0004éeª8¸UÂrÒïêÀ\x001fÊÚå«Gl×Ú]ÄF$Rh\x0003*Àv\x001b¦½ÔÎâà\x0011KX¯.°Uk1íN\x0001u	¨k\x0001Q:=÷ÙààvÖ\x001dt¤½\x0001&ÝzDõÓ×d¾¹#þðÍ²¤"Nüá[á4Êõ\x001b^ñÂ\x0001ënõôIà\x000fÏ¾î\x0016V4°÷XÒ+Â"eàê²Y*H6Z6S?wóË\x000bÌ\x0003ß\Ýï\x0010Ì°ºÕÍ°d<å¤öle\x001b^7n\x001e[\x000fkJXÓ\x0004«È
êLÄ\x0004\x001b#ÃâE#¬-am3,õ\x0017¢$]êérìdíÆÅ¿êI]Iê\x001aI¹û\x000cÂ
t6ì\x000c\x000eÿÓÀú\x0012Ö7Ãjj-\x0015Ú6\x00016äÈXÕÃ\x001264ÂZºN~#ËOÿÑÑB¾zØXÂÆ6X8;Ùu'ïH$ê(¢?ÑìÚÔÒt¬h¤lÃî±\x0005Ì\x0013-Ã¢ÁÚI`U\x000fV5ÂMhÅ¦fWrÏ¶\x001f>gµÑöVYÙ¸ÌªÜtì%½\x000b\x0003­fó°èG[ö\x001bFméUB;nn\x0006¬ßÇû¤Á¦\x0010x\x001fcÇ{3¸üÕ1ÿ,yçÁûF¢!\x0004\x000cÞ»Õãç¯ûûzÕ)/¿yyý°úºÞëp@¤gX,ÖOZ\x0003h¢Ãú\x001dqPbu7¿¸¾ý}1ï\x0004ß,\x001fÎç÷ý¼Á¼¸6¶ðv\x000eY©Ø7\x0002`Êü8g¸°r¨9Ð\x001b{¸±\x0011W{.hqèi\x0012+@k©[9\x000eJ*q±)­¯:\x0012\x000bÕ×/_W¿¯g×««×=\x0013Ê°@õàV1K \x0002
F4'\x001eîîçï\x0017³ëùÛùÃ.Åm½XèTAFvØt\x0010\x001dû*G1®QÉhJFÓÀh\x0015)"\x0019
\x00080Ù8ÄÑ%¶\x0016Ó¶\x0001ÓñC\x0013`:j½t:(¦\x001cmk¬¥t%¥k ôº\x0013d'[8P¿é\x0004¾Äô-ÁÔäékPèØÜ¦\x0003Á\x001c[ók)CI\x0019Z(e¾\x0008HF´Q*õÔ1nVOTu_\ÓÛ¢Á½IÒ¸bÃyXÊÞr)\x001bÖK­ý\x0019Ç\x0012îWi]wy\QÍZÊÞz)\x001b\x0016L
K¹ÞLrG\@\x001dâèª\x0016³7}dÃüÁÚ:kxdÒc­3d\x0014sT¦gs¼×!c\x000f2¶@jr?7h\x0006aè{ç\x0018òøPfmå´Ë\x0016JK\x001a
\x001d%%}çËS\x0008£5óµ½©ZF¦	$\x001c×qÒzÔ)8WR©^\x001am\x000e?`\x001aíüñëzvó¯ÕçÕ§Ùõó×õß°]o'*3=*\x001aXÎ\x0002×2i®G\x001fÜBÎ/î\x0017³Ì¯çW³ëûeêÚûî\x0003Äå\x000bü3'iUI«¾uZ]ÒêoÖ´æ[§µ%­ýÖi]Ië¾uZ_Òúo6´á[§%müÆiói5í\x000eâ[Çíof­»\x0019^P\x00087hr÷!7}º0¸FOðîÛ|eo;ßú~&{ûüÖ74ÙÛÐä·¾£ÉÞ&¿õ-Mö¶4ù­ïiªrüÖ§êM5õ­O5Õjê[jª7ÕÔ·:Õ´5¡ßJ\x0006?\x0008\x001c¾[¿|ZíóGY¾ä(d±÷^%MKï#\x001bÚAçèÜ»Åòj¾Ã.>ãª\x0012w¨tx .\x001b\x0012\x0000®¡î7ì9bÚÁ#Q3miÁËz:hM%\x001a\x0016\x001b\x000bÙ<ÑÓó¼\x001c99LPfjº_¯:EV³ÛõËóë=#W:4@7pñí3a
?(³fÌËùìv±¼y¸ÛaÛÄ¦¤4
KÖÒ
«·ÚQ$öi\x0000Ó®\x0005SqKv\x0010âL\x0011%u½ÂÿÍ¤$g
e()C=%Ö7Xz)ÐSi\x0007âþ5vËI\x0016à¢¬Ë¿þDe÷ç×_ÖÏ{ü\x000cò3£~3c\®lÐ£I¯Ë\x0005
»ß<,ß-nv\x001a2¦.1u\x0003&ºAjzÃ
Þ°LV+\x0012ÑÈQIòJNSr\x0006Nk5Iâ¡1üÐ©\x0010Ï\x001b~µÔ£\x000eµ¶ä´-ñ\x0014$\x001a\x0016ðd\x0005j´ö:ó\x0004²?:['þ\x001f¦Ê\x0005A\x0006	\x0010LÁEmjTÓ ²,À$R®µ¨¬\x001aà¡fÝNxå¨üÆ¼(÷Úï\x0007\x001frT¯\x001f?<?­¾ÌÎ_ùü¼»XÔÂÆ\x001d¸mv.YúvÍa=b^_ß\Îïfç\x000fïà,µ\x001fÓö0m=&Ö\x0003é®\x001bÀjeHkPc\x000flâ5ìÝzsü
\x0006N½õ\x0013(\x0005þß­?ÿõÝç\x0005\x001b»\x00191Fª\x000e´u
TÂêï\x0016×û\x001dr~Ì§J>UÍ§ÏljÃ0\x001e5ó±Ä~JVýP>]òéJ¾ ô\x0019ÏÑnáóGË'jðLgjÃ\x0007'x¶\x001e0Lo,z²QøÂ@£¼Ï|¶6|²»V¤øy§G¾ 6ÃÏOÉ\x000c\x001eÊçJ>WÍÇZ\x0010?CJ\x00156Hï9~GÒùÎ×ÓQè\x000cõÅ\x0000\x001a-\x0010ºÁQ·\x0016.p¡\x0016Ny\x0016Ðø\x0012Tü
Ä'ü¨âT
_,ùb5¦v\x0008§±ôð\x000cxd\x0007¥¤\x001c/<\x001coS¶Ñ-Ì¢\x000fæ«ä¡§HÈÔbû-ÇoRJ÷à¥¥4¬KËKéÖpØ
ã\x0015¾wXâFfâ,{©ïÆ\x0015ÐÀE£¯u7\x000fÌÂýºþôø¹«!ýºú¸û\x0012£QÉ[u;°Â$}2E\x0016äl"C\x0008v{\x0014ÿ°¸º¸îGïçowÈ\x000b1-ùl\x001d\x0011ZRi\x000el\x0015\x0002Ë0\x0011PFó0\x0007)¡Z@_\x0002úZ@¸G+\x0000a¢t
Ù\x0000èÙè\x001cÓaGò/Tói\x0012U\x001eËï\x0014ñ)\x000e`\x001c4äl\x0003¯Nö¬\x001c'±%}ß@\x001d
R:\x0012RËíeº\x000eO÷ðtíô@×>ð e\x0010Ó$©½2vZyÇ}^Õ#T\x0006å\x001c¡ñçRQ\x0018Ì\x000f\x001fxø
Ô«\x0001{\x0013XUÎ`\x001d±á×§\x0001R2i"ñÐ\x000cúæ«	{3XUNa
3NpIì\x0006þd\x000c/í ïPË§eÉ~[õ0­\x0016®òFÓ ä5Pèã¦°î@]=G<Û±*k<Ýá¥T\x001afãP\x001c¹\x000eÏôðL-\x001e0©4AàÎNÞXR\x0011à©d|\x001dëá¹Úù\x000bçfú¸Xmü$¯,}\³w\x0007Þ§ìO«­ù»ª\x000c`è\x001e\x000b:B\x0008`¤\x001dDç%F\x000c\x000cs\x000e$ý·\x0018üá»Büàuvÿë\x001fvÁY¡L \x0005ÚKÑU÷¡t/\x0004Þ&ºÊ\x001ff÷?üxµcêÆ°uºá;U\x000b'èñ¢úJ\x00021>Ø¬¢5¸\x001fUÂé\x0012NWÂYOý¤°,k*z\x000eÛó`ßõ\x0013
\x0007ÒÎÔÒÁ\x0015|Ò\x0011E:Å2En°*WÒÙÎVÒ9*qö\x0012½rÓ
r\x00037P»¬s%«Óä\x001eå%\¼%:Í?~ÐwYIçK:_G§\x0005.ºD§è¼\x001cS,6g«£èBI\x0017*c\x0017\x0004¦¼Dû$\x0014´á);i/(],ébmì|VC:ú²Îoè&Ä>\x000e¤+,\x0008p)\x0016µx\x001a=½t"½Â\x00052ëaÅÁQþ0:\x0005ÿÌÞ¸Ã\x001f8\x001bôÃêõëî
Ìk|öêrö°¤Ñ\x0015Òª\x0018¹!Áf~?Üïxc¦X2ÅÃÐZG\x0013J\x001eö\x0000\x0015$·Á¦z8ÔæU&\x0011\x001cN\x0005K&\x0019_\x0017Ï\x0008Êg¨ñ§Â\x0003¡t\x000fJW@e»ok\x001dçà7ÜÜ¦F3=\x0007RÙ\x001e­ 
lô>\x0016Z\x0011Uàö\x00115ú¾v Uo¤Ë¡\x000e\x00074McÝHvªUÞòXtÉ~*×¾_4ÓMÅ¶ÎÕãÓÓú·õË××=Oh^lø\x001aKéÜa\x0005\x0011bÓê´\x000eÐÕ\x0005üËÛÅòþ¡|EÛÆT%¦jÄÄ\x001a\x0004røAÙh\x0015\x0012¦&\x0001\x001b¥õ ±3Á¹*}A\x0019r£¨ÔÅÒµ\x0006S
êVw
÷ú4
ódZ\x000b\x001b×SÑÜ(*u ¾\x0019T³i-*ª¥b	+¼Ì ¢\x0015TØ\x001f(Ø_<ôÝ<=þ¾þúuo >@¦[¬û¶#\x0019-E:onÚúæòâýâþ~yNFÔ%¢®GDi¿è\x0005µY	¸,ÒEÛè´Ö3ÑÔ3JE6ÊJ\x0006òyAHGV|ÎvuWBÚ\x0012ÒVC*´&H9\x0001,ÜJ`pø3$Fÿã!]	é\x001a ÙÔ[©ÜU$íæâè\x0011¡\x0012Ò¾\x001eÒùt\x0013\x0002ÄLhÑq\x001cñ!¡\x0015\x00116«¾V=þ@·Üu\x0004§Ç=Ù\x0016þ­@×pmñnÔ\x001d ¢w\x0001Ñ
K7k\x000füzy±Ë3;c\x0012Ó´`Æ´\x0000ië;×ÍDÉY¾è\x0006oå-¶¤´Õ\x0002_\x0003%\x0005ÓsÅA3¶!L?(ÎkÁt%¦kÀ.røOrÑÃ\x0006Î\x0003ï»\x0016L_búh
íÄª
ºoF¯\x0002\x000fM?P kÁ\x000c%fhÁä6d
×¹3þæ´ñDø·O0òå³£¤Ëg%¦¤nÀÔTn\x0002§?b\x0006\x0019DZò\x0008è\x000eDMíJGÏ¯ÿó\x0015\x0017Î}\x0006¶ràtý\x000b°ÿ	\x0003\x001fNÎ©vÕ£Ëÿã\x0001ÏéWl§úõ£øC!ê÷ýóëË¬]¯þÞµ;\x0017ú9ÛÂÂ-L²°_ºWÀº:z<z}ó°%ëù?ÐÀv?²*Õ·6l[Òð-Ù\x0016qõéuý4»z~ÙSJl¥5tD3Tð¬¬qT=îÆu2îæW\x000fËÙÕÍrG\x001dq&T%¡ª&ET;"téLY¯¹ 0êQ*B]\x0012êjBáéài­$Ç®LÈý
~´Ò¢\x000eÑ¦>âch©»\x0005F¦Õ\x001cÄ¡=@5¡-	m5¡dP
AttT\x0002D{DFmðª\x0008]Ièª	áÆkt\x000eb*9S&Ê\x001cÄÑ½*Ä\x0018JÄ\x0018ê¢!Á0kQëØÑP4y>J \x001cÄÿ?áfÉ»%þð\x001dþÙARoÍíê÷ÕgØw:Ô\x0007K·rï\x000c=ÝvOË¤Ä&F½©³ævþ~~
ÐÍ^Øì`Ù\x000b­\x0012VÇtÕpØnêîá¶É\x0005s¡3¨<ucvÚ±f³ÓJV|ÕÕYâ\¥¦\x0011\x0000»ÿhÀ\x0000vôáHM?ª¦-ªF¾=L\x001cOª²p=&û)\x0015õÐÈ«&ªð­ûÙ\x0019üa=ý×üçâ§Ç/Ý_ï^ÖÿÚsãQué£´\x0000$v\x0008À>ðVä\x0006çéÎ9»-Þ]^ÜuÿúÝrñ\x001d½­Kl}\x000c6,\x0004&dìNô\x0010°c^üÝ x\x0004¶)±M;¶Åê³´6Ò °ñÝÙËÁ+ñ4öx¡>3ÛÙ\x001eÅlè$ µ\x0013¤ì\x0004Ì®¨£½\x000f-Ä®$vG
\x000eA{®M*Ô82\x0014áCü\x0011##Ìá\x0018f+©,\x0004±;fÿAf>áh%s<IÝ ÈãéÝ\x0016^Ù_ëZì<Wa[K\x0016C\x0010fÝa5?\x0002»·ÖÉ£\x0016;t\x000b¤c$¬\x001aA%n\x000f@þ\x0004ÃCÁ6ÚïÝU*ðÍ¦L}³úíëã¯kL\x001fü¶^½þûîu#\x001aI\x000e?ZÃIÝ¦k\x0016
¹\x0018îdSßÌoï/îî\x0017F¸]Ì\x001fþm?µ)©Í\x0011ÔZq
IGM\x000e°qsªwC\x001bª#°]í	¶¢Ë¹FË`ÃÁö±ÃX']+v(±ÃqÑöDm°_5\x0005Ûj¦\x001e}_m£VY/lækâ¶NúZc;¨Lá¦N\x001d\x0000·£nñ\x0013àSÇÒ-^Tò½Cé»ç×Ï¯O;aöîxÆIGzÖF8Ö7\x000f£MmÜïóðöæáòb×AË\x0003\x00179u\x000b'Ü"é	*®e2ÝÁ8£\x0015 ð¿x«®[¾ûnþûúsJéõlùÛã§Õ¼¨,\x000f,ÑÒ§¼¨à.[4\x0005ÜN¾_\§l^Ì·\x0017Wó"ÎÄ¸¹$F¼ÔR¢-\x0013¨ I\x0016\x001cNûýÍÅ°sH¹;6ÿó\x0013h÷w5)ÕÑw×h\x0013]¶å\x001eÉ5þôÏ\x0001ë?«a!n\>û\x0003\x0015ÙÀ¾!~ m[Áþó}\x0002,ò¢9µz}yü°=|}y|zÚs\x000fõÊµ\x0005ÄWÑ6¦\x0015÷sIõäÃ¹t5X^/f\x000f÷ËËËé{h\x0006U%¨j\x0002|î\x0015°8)M ÔÓ*;o¸\x0013\x0012Ô´jIu V0%÷Il\x000c?\x0005¥+)]S8Ù\x0005\x001fEÎ4w:áªa]H\x0013§/9}\x000b'ÚÚ§~Cl¹±f«U]¡'r\x000bh(AC\x000b¨Ty"iË­ÿbÐÑëAÅV¹\x0012©Ü¦(\x000bÂBµ/xW¸ÃÍtÏm=âfÜ dÌÉRøÿÔã\x000c{Áô«\x001d\x0016®Ýá]á\x000e·Ô\x001dw\x0005¦V%µ:Ú\x001aÜG»z&Å%à0õ\x0015eNµØñÖ¸M=.M$¶:d}\x0004²	ÉyÑ)¡Ï\x00088ERÕ¹-a6%³9\x0019Ï\x0004Y²\x0017\x001fî\x0004£<Uhß\x0002mKh{\x0004´4Ô\x0002ÔJC2ôò\x0008ÔÒÐ#¨]IíÚ©\x0003\x001e\x000e|.xä«ä·a#æ\x0011Ð¾öG\x001akf¨þQ²\x0006\x0013°zÇ¡.¨\x000e%t8"ÒÞ±\x000c¬räÜ\x0000ãU'ÐÉótÔ±¤ÇP[òphtý:/x\x000bd=4Pû\x000bþPÊó!õ=\x0016¾>í}&Ô+a6é\\x0001«\x001dÙxÂ¼ôvJê\x000cï±äôáò\x0000TU¢ª&T«XdÆà&eËDê¶m¨ºDÕm¨__Q«Q\x0010ª¤\x001b/ \x000en\x001bª)QM\x0013*>\x0017zB
Év¬ËøfÔ)áÀ\x001eéTëâ¶t@ìÖ±\x0006L\x00171å0uª§Ã;/É³a\x0017ÞA{#\x001aJÔÐª8«kàná4¡Ê<N\x0007Æ&TÙR²mNiwf]\x000e«Q4ýcf\x001d\x001c×Xm,Yá¯¦¸zöÊ5Xám(®t`·vPÜ\x0018ÖÒpB[êrV\x0010ÀºD¨\x001abè1Ó\x001a\x001e´nðÆvøä\x0012Zô}4ð­'ãùËÏÏ¯_\x001eûï®»\x0005ß °¬/\x0006{®£v\x0018\x001d'Df³ùòÍÍÃÝÅb9]¸È º\x0004Õm ê\x0005\x0014:gÃ
Éí\x0008#Æ=\x0012+AM	j@cD3ç\x000eTn"êÈ\x000bO\x00189Q^\x0007jKPÛ\x0004\x001a4Vý&PI
Äx'v\x000c:ýtV\x0001êJP×\x0000já,·lIÍ¥ xåO¯Æ
h+A}	êÛ>½`½SÙn
h`Î)E¨8
¬*ý\x001f>\x0016öN~X]ûþy_\x000b\\x0010p"_4\x0015\x00039;©¸ÑAÌfmÂÚÚ÷7»á2¨*AU\x000b¨ÜA¨°¨Z%PÉ\x001dpT9\x0005§.9uS@-%h  j\x001cë{ ç 3Û\x0004jKPÛ\x0002êä\x0006dáhª\x0019sPñßéKLß\x0019é¢ÝÅ3\x0015²9-G\x001cÏéÍ³\x00024 ±\x0005ÔK^08ÙTÒÆÁ{x[@ËcI
jÿTrp\íf>Y²Ç:ð0
õ©mnãÚV\yFËTð$Å
¸lgù¸¶é¿«\x001bq±ÞåÕÊÑhPÎæÕê¨å
®ýeÕh?¸N¿¬>ý_«?öhô ¨YÅÈmÚ\x0005¿)õÙy8]Î¯þÏù;ÎÓjJÔí;êa¨ÖÓ±\x000fP\x0003);igsá¿Û¤8\x0018Õ¨®	\x0015.TJ'=ií8¦~Ð\x0001Ô\x0006\x001aJÐí[êa F¦6:\x0008©Â6qæ¯?ì?­"Áõáñ\x0007zÿ½CåxdÃ\x0014N­åóÏëß÷ØwÃ±Ïó¾%íé¨*»Üvz¡\x001d4QÎ//ñµXâp¬Â)¶¼y³X¾ßaâÉuI®"DL
¬Wd+áÀÊ\x0005\x0010ú´ä¶$·GÇ\x0012t$ï\x000e¹æ¨Ð\x001cAîKr4¹Î\x0012\x000fi"öÈ\x0007E'Ç¡Ç\x0012=\x001e®X3CZ\x0001¢ÓÂÇ±FÜvt%Jt%cwlð\x000e\x0000Ãn¸&	ÓV'd7½±n\x001cì$We°\x00176ÿH¸\x001c±í©\x001a$\x0017B·ýiz\x001cºÊ\x0019\x001c¬MúnØôáyÈ½³¶³»ÞhwG
w<è\x000bK«c<i¸£æ/kü\x000c<w²\x0017£\x0013¸ïuÔX\x0017(uÏõw%;õ¼¬ÛÁQú¨ ûÞäÚÓ¤\x000b<~]òí*ØAñ`sÐeCÂ?ÚL%¥¬ÜR"\x0008\x0015ÞY»ÇºS.ìRöFÇ
\x0019XXØç\x001d.6Ö\x0018X\x001f	¾rî\x000c{]Ç.ìÔ!<B7¬ÙwFªµ=ôáÃqðB²`3û`¦²±f8Ñêh]¿Ì\x000f Co×¡?ûþiýúòºO\x000cÝ\x001aª¡r\x000e¶$An\x0015¤# \x0003\x001d~C}¹xX>ì83¢*\x0011U=¢8s©v\x0003ëQÙ$MyÃ²O{\x0011á8lú\x000f\x001b\x0001µms.ö\x001cH\x001e[ï\x000e\x001e\x000b¦ºò\x0001zm*Ì?-S)·að\LXüûâæv1}
ÏºDÔõ¼¤v\x001f\x001a\x0010Uz%\x0000Ä¡\x001dZ=¢)\x0011M5¢µôî9ôâ\x0002"é{\x0001¢5ãbJ5¶D´Õ(|ç\x0012¢¤\x0010JãÏ\x000cîVõ|®äsÕ|JÔZ%±9ØIü\x0007"8¸CÕ\x0013úÐ×d.W\x0008ÔÎ\x001f9I¡\x0002¢\x001eíz¨C\x000c%b¨F­^ÒTQ:Ý Vç(\x001e?SbI\x0018«	µ¥N\x001d\x0008bÀ#JGè\x0003Ï\x00143jÒT(ûKbõè¢#UY`tIã\x0013\x0018U²âDÆ©Þ
ãx\x0015¦v[6|ð\x0003¯Ù}Z}¿~yùcwNJIÃG¸L\x000eØ$Ù%¥Ä¸Ôß\x001f.\x0017w³ï\x0017ËåÓu^\x000c¨J@U\x000b¨\x0004n$\x001d Ê¦ì^pôþ,ÑùùH>]òé\x0000ÒÛc\x0010
¡S\x0000¹¨YêT5 )\x0001M5`¤2v\x0003d±ô¦\x0003£íl\x0007\x0000 û/øC!\x0003,¿|^í1Ru¨ñÊ¬CðèÚ\x0007\x001b\x000e jp¹ 5\x001cøéâÝõ|Úö5óÏÔòA\x0000OÂ`\x0002?ñi\x0016"02ðj@W\x0002ºZ@\x0011I\
\x0000³Û¯µ¬`\x0019õ¸O
`(\x0001Cu\x0004Ék
>°9£ïkmä\x000f<ê¤XW
tÉcÓá#°ó?ê\x0000Q>0ê\x000eß»jù¼,ù¼¬ 2LøÀÄPð\x0003{þÀã\x001aÂÞ\x0014öÕsøÿ;B\x0003\x000bØÂì
/7âfIyënõôûµÐG6É;©fëQk\x000cB!)Ã\x0005énÝÍ/ßO¯\x0019Ö°®	6 1CÀAËñî6ê×ô®©Ìðe«\x00116°¡
\x0016Mã\x000cÁrÅØÈ²2fÛjcÝèÀ#+Îô\x0016X´\x0016£Q\x0010¨\x0000I=Á`mU=XÕ\x0008ëyq2³@@+iù´b°º7Òö&la¨)DòBÆ\x0018\x001e´N	\x001a´vÒt¬\x0012¶7Ádã\x000cË×Xø©õ\x001cÓU´\x001cXy¢\x0019&{3L6N1Ï2Øó@u\x000e&?ÉChÝá\\x001d­êÍ1Õ8Çp§OM;ÆE:5¡51ÇÖØÓ\x0004ÕdªmEå©&\x0013EÒè
ÍxéslO´$¨Þ$Sm\x000c\x001b\x0008Òó
sC«%Ç\x0016nmGÑ\x0018úgøÃ&ï¯ëß_Öÿ\¿bYö\x001eý`4SNKÄwyJv8:t¤÷n 9VÈþ°x¿\|¿xÀÒì\x001d)LBÞ\x001c\x0005\x0011yK«µÙ96}\x00025fcÇlÙ¾Î{=8*´3«\x001e³jfýA\x00103V\x001cêÄlÈ²Ð{9È5L2\x0017À3°î\x0001ëÿ\x0016\x0003Ãõ]sm¤M
X»ò8\x0014ÜõÌ¬wÉL\x001fÆ¬cT½5þPÖuo0_go\x001f¿|^¯^w.\x0017\x001aÎÞô\x0014£$\x0010'µv£RÃ}'>U~Ø=¿ÜÏÞÞ\Ü]/æ\x000fûyuÉ«\x001by\x0001-	\x0018²Å\x0013ÆdÜÉ"Ôj\[âÚV\íQGªãÅÊÉ$Ùo¼`5|3YÞ[
ìK`ß\x000c¬©zVI\x0008u \x0000;K¾N\x000c4°j¥r}õaüá»½äÛÇõëG$?Ù'å\x001fmp¬\x0012\x0003[\x001e|\x0010ëíäÉçbñð\x0016ßÜíôÏÀº\x0004Öß.ðÏÒúðÍ÷»7ðÃwÝßß¥D'Æ\x0004Ç7/»Ç£\x0018½,J,jIJF\x000bW´í	Î\x0010\x0004\x0013(Þ,Àç\x001dûÿR÷nÙÝHîT|\x0002\x000b÷ËÒG¢(^t2û¥\x0017¥`Jì¦Ù\x000c2»²j\x001aõv\x001e«Æ3©\x001c³
ÃvcÓÝ7¶+×öU)ÒS
}\x0003f\x0006Àì7­yÕÅfÝµ\x0002ØX¼YøéáëëV0\x0003!"öÝÅZdEýw½pÔ~Ò¡+\x00050«x«ðÓêòöýX,³©Mg\x0013Äf-\x0015\x001d\x0003%q3RuÓðLgFâ$\x0017-÷Rgj\x0017S03WcÑ\æÆ¢Á)6æo
µ`æ\x0014õ¥F
úx¡Ä\x000b³Xtxà.Ýøþ®üóoOÉ?<=¿ü¾=ã=Âi¤³-1j|¼\x0001D\x001fµðY?gP\x0016÷³ó³d»WçW×\x0017[d3¨.Au\x001b¨\x000cY8+zGYä>Ê¥iTgÖ\x0008kJXÓ\x0006+²ÜÁæ\x0017éTå£pk§\x0003ÁÚ\x0012Ö6ÂZC7X§­^í\x001cüÙ\x001fU\x0007ãOO6¸ÍJóÇo\x000f/Ï_wµ+¹-Ã\x001cÏkh¢¡D åLµ`Ë´wÜ¼¾ºÜ"'Q]êÚP]¾³°¨¡è\x0008«rÛ
ßÆ \x001254¡
j	\x001c6ÞN\x0017WQÓ«-Vb£@1Vá]Á$:>¿<ÿ
þ±\x001d¡PÊUÒ¤"(c\x0013bÐÛ«ÉJÈ}}\ú|}õÓÙåÇ÷£=¦*1U\x0013&|õºÀ)A\x001d\x0010\x000cV¼dÌJÃ}\x0008sçÔ´\x0013CjIFä5\x0014Ï$R½¥±ÞnR©ýFB\x001d|Ó
V¿?\x001b]>A|¹\x0015Ò®³\x001eL@ÁZÒ$Y
]\x000c¶ë\x0008\x0018<éò\x001c¢Ë* ì¹TÉ¥Fry|ËMÏ\x0001NÅ¤~O)\x000büÐký>`OØè\x0019ó]\x0003ó¤Ø)IPJ£üiÎ\x001cl
³\x0017\x001929vÎàÀ}â{)QA
\x0003üZòtðùv/0ÍÀôX0\x0014ÙÏSõSïò-b¬{\x0019\x0006fÆ\x00051é­s?Ö\x0006\x0010W\x0018¿÷\x0003³\x000cÌ\x0004C¯\x0014\x0001L£ÁC0\x0011s©d¨nvÁù\x000büåßvÑ\x001dFÍûF\x001cæ¹¦nc\x0010.¨ÜB¼×{.´·I7eDU"ª±`°q%ÄüÂi\x0001¼G|ïªr'!DÜÝâ\x0007Ùæ.¿<À\x0017û¥\x0003½}~{z~ÛÑä%(0%I\x0003Å\x0018gj\x000b>ËöU{¶êP_ó\x0012ÂåÙ§øöêîüênK³\x001eYÈº\x001dÙ dSBÎZ¬²\x0014¬\x001d\x0014\x0005mC¶%²mGVô\x001cgÏEÝ:\ìæ\x0006»ý´\x001184\x0013Gµ^\x0017
\x000ffld_äfÅÁ\x001cD~ïy ðu\x000c\x001fl¤}üíaG»<ã5½¢´¤C:oª×¡Û\x0016ß~üaµµ­_ÆT%¦jÀt2§ä+´\x000e)h\x0004#1Eå\x001a[0u©[05¥PÂt\x0001\x0008n-°¹MÅm_LSb\x0006L\x001fI»\x001a»°OJw¨\x0011.+&Ê-ª\x000e;1aÅð\x0012\x0007ü ÛØÓç_Ñ\x000f|ý²Ý RO"\x0003NÂZ­µYµÉ\x000fåR®®®OÑ
\~ÚÍ§K>=ÏÅÎ²RÉI)á2à Võ(@[\x0002ÚÑª§#8TýÍpC\x0017,£à|	çÇÂYKÀg©Ù¡Ñëo×\x000eùÍQ|±ä£ù\x0004\x001dR/Ðý\x0004\x0000ª^4l°©ñ\x0018@É·Çèýaev1RØ¤Â:k[Ál÷QlÈÑ;\x0004\x0008\x001d\x0011JuY6Y+ªRÀÝ\x0017\x0010\x0013ÇxB>|Pz¿îAæ#ö\x0007ýúº½C¨E ºßHÂ§\x0017$ðÔF¥±\x001ebù÷nÍºgØ\x001eôòvKÐ\x001eW¸º
WÇHO"èy MÌ\x0018VVGV\SâF\|\x0015I³\x001bLHç Àµf×ªw%87pK32«-Ym#«
ôÐ\x0004SëRÙ0°\x001ajG\x0003Sû®\x0006ëØ©u%®kÄE]iZëS§c#uÎè°\x0010\x001cÖ´¾ÖS\x0013,\x0004jc´>¯[õ®&ËXÜXâÆ6\å,6ëpûb"ïþÀ* rÂ$\©âFz¯ëõOÏ¿¼>¼½$êÓÇçíoËAÜ\x001a\x0013ó¦\x000cK'sÀ¤Ü`õÎ§»Å§«·«»ë}zv}µ-× nDN¬E¯æ,@¬'E×JÊ©ÁÇÐ¶¶íÐ©Y\x0007
QLÐ¢WýwÊ
ö\x0016lö%´oVîÉ\x0003iÊôqÂåÆ©®¾Ê\x0000\x001dKèØ\x000e-\x000c* $hOg\x0000\x0007M6\x0011D\x001b´äÛ°}\x001fÂðs\x0016¹Å»6KÔù}ã½\x001a«1ÌàU\x0008×wß}\x0006û_ÓApõëÓý××ÇíYv`Þ"I¥i\x000fgVj¹d\x0015©$\x000béª$\x0001´sËÓt\x0018\//oÏV×[\x001eãÂF\x001bzü »¹ìÛ\x0018]Ü¿<üòÛýÓâÇç¿üeGOw\x000f&9w5p¸IâVFÛwù\x0016âAßÎèby½úøÃò|ñãÕ÷ßoó&a£\x0011}\x0007­Ú¡ÑÿÌwt¹o\x0015e± "]}ï:\x001a\x001aþC6\x0019>È>åÃËÛï÷;\x001c\x001f^§nÝ±"ÝhFGÕÒ\x0010µACñáúîby¶\x000f*ÉÔ(2Ý«\x000f¢QzÀ\x0012ý,;ì+å¨qhºDÓ£Ð Ku5B1<ÃÒ5ÌZ%ß=\x000eÍhf\x0014Õ\x0014ÈtªÒé\x0018û;1\\x0014½?-Éì(²¨ò¤¡^_òIÑÉ|Ä\x000eq¨²'\x001b¾\x0017ÍX®Är£°Rã\x000e+d/°-9£Ð¨J dÜù\x0012Íû.
ÕÇ\x001a¼\x001eK=\x0011#>\x0001g´A¡ýÑB\x0016ÆÍ:ÉdLaÒL?iC9zû­k
:&F¡yeþàlLQf´Qdæ\x0006ßâv²ÁY`#'\x0002>èóÌîß\x0016?=¼àKá\x000eÏ`¢¤ç.\x001b½ÏEÅpð¤(¸û§\x0006RwçV×øX¸\x0007¤)!ÍhH+ò\x0005¼À+BT¹3\x001cVþ\x001e	\x0019JÈ0\x001e\x0012\x0015\x0002Rh\x000e\x0016%ÁYUÔûc$d,!c\x0003¤£|"¡d®q7bZ9Üm\x001cb¿[:Ä¼[Æ0*;	åèÀl\x0003´Ða\x0003%[²aM\x001aq¢R~\x0000¬täèÊä5éªÜï\x0011`mY¯Püzæ\x000bç¯¯}xzÚ%ï\x0001$÷ãÃ$ëf¦Ì\x000eéët|pquyûyu~Îó3£ß\x0008¬ñâ
áóËÃ·Ç/\x000f__\x0017çÏo??lOÇ
\x0006¶x:¸`ð\x001avãÁ\RX=ÑéçëÕÍÙ§ÕåíâüêîÃjKf®ß©;^ÕÌ\x001bR¶\x000c¬Ö,Pèú
s0nòX^ì­Î¯h\èç÷ûüçüçËã/Ço¯/;dÚàÔ\x0012sóHy>N-}§a	\x001d\x0008÷?­®Ï>..Înn¯·é³¹
wÔÁªVXú\x0004â-"UUX¬\x0008"V;øä>Õ¬¦Ua\x001aCèa=\x001d\x0007ïYNÜãYmÉj\x001bYû\x0006j°\x0008²\x000c«ÖfØê\x0010ØÆêJV×È¹7®×tý\x0002ßõ=\x0006SÊ+ØÁ@½'õ%©o%Í:nÝ¬¦v\x001f]I9MjÕ¨mVcÉ\x001a\x001bYÍ\x0015O\x001aIÿPÊgU\x000fæÒí
«ÕFç$ü`33äòùñÛÃÎ»!8P\x0007ó\x0019ïzé ¬XçêúêV¹L\x0014¸¼:»Ym¿\x001bêqu«\x001bq1Q\x0012v!iÅuÂjj[imIk\x001biñdNÐ\x0001\x0002×,\x0012cN\x0016¨h[²È\x0018\_âúF\÷£É@fë)
\x000bpß}o\x001a\x001bKÜØ\x000bq\x0016iº`6VRI6kxêZ\x0015µVòÖºÓÖµ\x001bè{\x001d¥äØ¬¢«¤ø6\øJ\üµ\x0017nhz=\x0004·´Ó
Ã°­Ô¤à\x001d.7È°Ã6ï4Oup\x0000\x001bOÈ,,¤½Û<¶\x000b\x001697òø¥e%\x001cO\x0010Ø~ÙqÁÄÜÔSÞ9ÛÝ\x0015Sb.Uïxõ~Úë'h?myjÔr3£_ZV½±'¡ËH¨Ù H\x0017×gõ3\x001a[	U4\x001bM££a=?/0\x0005sÇ)+Ú»ë*Ù\x0018l/ãôn­Î\x0005&^¾ß,ãiQâi1O\x0019*<\x0000>K\x00026ÄÊÃ\x0013ù\x0014ãS#ù¢ÉI\x001a¾_znÓ"\x000bK¹ªbc,\x001eûvõ¸¯7\x0008¼8'è¡
Ûçd1)ûn\x000f²½§¯h§°ì´×,\x0006IMr\x0006Ë¨è}XRÞ\x0013Lc¥´1z\x0015Vb<&ö
ñýfI\x000eÇF·\x0011«"{bê¨x\x001b'ü \x001fD¯\x001f¾ ë\x000e;ì,IÆFJÛGG6¯Fl[?\x0010'_¯.IÏõ}»\x001ePz$`'IbcÑLN¢%k\x0003æzè²q\x0014 )\x0001ÍX@ì~\x0019\x00080×9(sH¡ÄàSô(@[\x0002Ú±_1`¤y×	ÿPDs\x0012d\x001c|\x0000\x001aÇWì\x0014bÄ\x000fÆaâ]Z°g¨^\x0011|MÆZhm\x0013s8Æw»Ä\x000fË»ç·§N­ê\x001bÞþmWov8£çºJì\x001dAÏ£*`~]WP\x001fß­ðuùêî¼S¬ºÁ»Ñ¶5gï¡U	­Ú¡UÎ\x0003Ö\x00065S·'é§\x0018t\x0015¥O`Ö%³ng\x000e:e¦k\x0003G¢Ôï
\x000epyz'ý§\x0005ÙÈfÂ4k<4jB¸<Í¤C\x0003.k0¾\x0011ÚÐ¶\x001d\x001aUøhA3èÔïq¢³z\x000f\x0019öÐ®víÐb
­sÎò6Vàò\x0018ô
#¡ã 9~PÞñ\?þzÿ¶==ÛÁ\x001e\x0015Að"Jb\x0001CªüAÝÀt\x0011¥ã»ÑèõÙéòîýôì\x001eOxz$P¤sÛá¥nØ(\x0019¢2^õP6\x0016Ïxv\x001cÙwuxð0#-ÏÞ{·!ûâù\x0012ÏÄóTë/7ÑõïM@÷®îÔv:\x0005q\x0019Ïå²ÏZýááëËãâ	Üêo÷¯\x000f;Å¬>å¦X¡mÊ	Ö@\x0005V\x001aÚá?¬.¯Ï\x0016çà^XÞ®Î·µîqU«Úpñ\x001aê\x0010c´ôt«¬¥÷F	\x0001ÕéoÁµ%®m]aó»\x0008æ¬\x001aÝÜ\x0005KBà2\x0014A·àº\x0012×5În\x000cÔ³S¬^¡\ni(\x0007t[i}Ië\x001biC~!·Â\x0006¬ÈèÖB\x0019wß¥0\Ö@¨¡VVlL)ÖQ¦\x0004\x0018ZQ\x000f´lUwvYN<\x0018Íë4f\x0010¥¥ R½¯².[~eªÔû¼ÒÅ¸ñ®\x000bîØ§ûÇ·oÇ§ßvÙ(ð4±\x0019T\x0008IBF*äD¯CåõÙÝÍââìüm¶¶ÇT%¦\x001a\x0019ðbzùaÍwrV\x001eÎ\x0003*WPW	³#0
.YÖ	~PèÁ¦ÿÅòmûý"ª\x0014XÃ¤eª$©\x001aâ;Â\x0004©æ\x0001[ZKgFÉ\x0018åhF\x001b=í%©°\x00124IEÈ­zTÕXz<¥\x000e%%ª¥Dù\x0010(CL©\x001cdûFÉJ]iHÔ°Ø(=w¶8·Â&(åé~\x000eè5¶t².w:TQ
iÓu}\x000c~À@å|¹¥\x0002y\x0013Q\x0016§oß^ïÿ­àîßP\x0005lûÖq.Ëeà}.«	k\x0015\x001b;t¨>½»¹]þÝàw¨\x0002¶T¤ª\x0014em\x001cª¾\x0013\x0002]è¡àÎ`ÅôhT]¢ê6Ô,k0ÝÜeR£¤\x001e4GãImIjHá¬/¨¥\x000fv¼Oj\x0019!æ@ZêÁ\x0014³ñ¨¾DõM¨QäôøP	5
¿ÿá\x001cô½QEØ\x0010Å\x000f
¡ÙN|àéá÷û×ÇÝ
/ÁhJ§®qð#5Þë®N7­h/«~³øx¾ºXÞ1¾jCoèuF\x001c\x0010^Ü¿¼<w
6w ¢LY²O\x0016m>¥@Y¯rÊÞpr!ò],¯¯¯ºÆ[\x0000U	¨Z\x0000¥\x000b|\x0000t§nmÐ:\x0003\x000e¦½\x0001u	¨f0P6®uß\x001fh\x0006)¯Y\x00061
Ð¦i\x0006}ªìø¨"Çâ­Ræ\x001bî\x0017·O¸
Y7ü\x0000àç·§¿Ý¿|é¤ß^^\x001eïÙ¾§1¡ÙÓw\x000c[&8Á%Qñ\x0006|ÇTÙ«»óÕOËëO^ðÕÝõõÙòãûÚmh½u°ª
\x0016o\x0016Ói\x001e\x001by¥îbàÐsB&ÆF`µÚè\x001fäÍýùþç§çÅåÃËÛûí_;Þ\x000bzæD®ô­!V§¯0xûyùáüjq¹º¾û´Ü¨JD5\x001a\x0011l¹¢v)Va§×.³\x0019ûÏtVW\x0002-ã\x0011u¨G#¦Nì\x001d¢\x0014¸Ñ»Yt9\x001dÈÄÁSå8DS"Ñ\x0010[¤sÅH\x001eÑêØÏ¢©JÎÇ#º\x0012Ñ_]]\x0002b´\x0014C\x0006\x001c\x0016Ý\x0007PZÁ_añ>\x001d\x0018NáÿºX¾ü¾SÄÃxq4±Ø\x001e\x0011UÔ9\x0011¸¾Hì²\x0015áüý§Åòúb«Ì\x0008\x0011®{#a¾4\x0018¹\x001e*+E¾EéAFÉayð1ôÿ?þRBve\x0000\x0019Ë	çEü!jè¤Ø\x0012½Èe«¢ê^°7¨P?&â\x0007h\x001a??Ýÿòéôß\x0016Ë¯_^\x001e\x001fv´,é¤üT\x0005çÚn2\x0005Ý\x0015É\x0010\Bóù|ùqôg7\x000b@¼>[½_¸Ücª\x0012Sµ`:\x0018µ¢E)"Q\x0011Ô«Ü&J]Rê¹Næº6®ûÎE\x000b§\x0016´43R(\x0004á\x0019µ\x0013\x0007Òj\x000f\x000e§Ç\x0005µqÄ
ÊnjÀ>|}øÛËÎ-`r\x000e\x0010¶M\x0002kN\x001a%yUUÎZ¦ò®.W?]oÍìqMk\x001aqaËSA\x001aj\x001d§K\x000e8Yd\x0005\x0003­ß\x0015=\x0019ëJ\×[$uJM¹éNª\x0013Ôù¸I¸\x0010\x0005òf\x0015øA)búmqö\x001da»Æ²9J\x000cÒF¬Ì*çÞTÇZùìû=ØTÉ¦F²å\x0006\x001fÎÁ©1\x0017ùëÌf+\x0005öýØ~\x0016\x0018n0Gô\x0001ÓéÈ\x0011\x0015Gðëçßï\x001f¿~[¬¾m½/°R	C­Í\x000c	*`YlT~ítõöV\x001cÁ¯¯.g7ÕÍj/×ðÃæünýÁwøkÑíóËý+Ø¶÷aS£¤Æ»{S\x000bLèLÅâ²:\x0008­û°}¾^Þâíý.l\x0019Õ	êD\x000bª6}Y»Ê)-Z¨\?®u%U9\x0006\x0015ø*UÓN§äÃËã×_wU%\x001aÔæ¢b$íó-Î:»ÒêJPi\x001c}¸>»<Ýö,QMº)$¶'*ÆJTáCÙüV÷Gu=«\x000eAjKÒM\x0019±ýH±¯\x000fÕ÷hiç\x001dªîKçê\x001bã6TW¢nJíÚ7T\x0007¾¬7n»^,ºUâjoÒP6RA'9Ø]^0-v\x0001Ë+U\x001fäû·\x000cÕ¶±ìó\x00010ö»Àá¬ê÷B\x0014Æ:4\x0018\x0003÷Qø\x0001\x000f¦\x0016×{~zÜ\x000eiÓ\x0005MVr¤\x0002ò¾×z×Ñ/®Ï~º:?ÛÀ\x0012¸:QÇhÆ3bsº\x0014X¯)ÿ\x000b\x0018M/ÿTõmd\x0019¢\x001dhJ½'«q.W9á©Ñ18û|wþÝ/}Í:ü[Ë%ñþF	bº\x0017ôLÏo_~{ÞÇ\x001aQF;ù%8=¥ \x000fq^ö÷nøÖ\x000bÂ¹kôKWw~¸Úq1MiZ0µ&=*iþIäÄÛ|=\x0007 oê£A]	ê\x001a@eßì\x0011@-ub÷êu³zd\x001dÃ)£Ú(\x000fòîÓ)^Ù\x001b\x001796XÕ0Dí$NwtïÁ\	æÆÁl\x0005\x0002óZXis78õ»7X,Áâ¨\x0019st\ÇÕøcª#¦o4VÇõ1Xk¹Øµ}\x001eùM¦\x001bk\x0014À¦[BI
µÀUõw\x001eÅ¥\x0019\x001eõEÊ¬¬ãE\x0007,M¹¶\x0012LÝLoôDÂ\x000f\x00061¯ßþuYcCÊ°\x0011¥,Ý\x0000ç\x001eéxÊ\x0019N2Èj|°Mÿ´\x001bT ª\x0001\x0014bY*\x001a²Qº|¦EÕ8\x0002­c±&P]ÖÂ{
EÍm4.X\x001bïÔO%d\x001c¨)AMÓW¯©\x001bX\BWë1aI9ØhüW_Ä\x000fôõç
q¼Ñ¥ä'\x001b±¸ÍÑ¼Êü">èLö¥5bãM\x0012?(JT¯ß^\x001f~~xûËVDÂR\x0013(Uß\x0019åcnÊâ+\x0001¨tµq}w»ú°ºû~7*áÔh¸HÞ\x0018øä	áå\x0012À«ÒGÇâé\x0012OÅ9ÛÞ\x0005\x001dsõ¼¦·QÀ«\x001e)Æâ\x0012ÏÄsBgQ[Ä\x0013Ô;NæX\x001bø¦N-ùìX>i©ÛB·ú\x000cµbSQ÷«o*+ùÜX>¥ó½\x001fòQ?C­³YlçZY®û-Àù|­\x0004|úø×\x0017»º{zrô`"	OXÒâÇ\x0007wöéÙç\x001d×ÏNÉNÉqx\x001aoõMÂó"Ua(\x001dH¨ÞrÊ|ï¼<\x0010fpz$\TäU§Ô§\x0012\*z\x00076=X¥¸7elvä÷*\x0005\x00065È×&@\x0000\m÷ÿb7R¤Q0£ÌöZ\`íäóö¬4¼\x0006§ÐUaÊ|êx
;Ìä\x000eè.¼q{åW[²ç2¤.!õxH¼ÿNÏtRç¸_¸ iý9UUJ4@ú\x0012ÒÄ$©ñ\x0003DþZÝ¥\x0015z1{"¤}ÝØön$¦¹[74	é);Z¹{*\x0007wÌÏX\x000ffÚæ;ú\x000f(w¿\x0016§Ïo¿>ìèèêT¹íwÔilîé«E¬òO×§Ww§«mgýFY/~\x000f/\x00178²û·Åç\x0017ð+OxÓðôüõ×íÊ\x001bpèÔÔà¤¦Ü^ã½Ëw
~Ð_Àï«åÝâóê\x001aýÌ9Þ:_]®¶\x0008qø\x0002ß\x000e_MÄ7Ý3]é)øñ.·É\x0003ï>\x0014ÝNÁ×%¾\x0001[¢Çæy©Îgi\x001e\x0001ÁÓÐ)w\x0002½â?mö½\x0000|ZiY\x0014¡¦d>w

ª¿:û²\x0014¨Hë?\x001fÚ×Ì\x001d£p¹\x0019/¥TjSU6\x0001ffC?
>`úiÀþøKªÅÀ\x001c¿nå\x000eÝ\x001b@\x0012v&wºFCç¦\x0008Öè½a\x0000?û20Óâónh]Bëvh£s$J\x0012S*§±Ô$\x0012ìù»M\x001a m	m'@\x001b*öø\x0008 iÀL¿«\x000fÓ\x0000íKhß\x000eíH7Û¡zQ* ÃÔd:öÇX\x000bßg\x001e.%ôªá\x0007Ý­è3l¿äÖÿ÷Û.úÝùV\x001eíIJãa¾³0¹º º-Üú¿ÜmwXHívIjw\x001c%¦\x0007¥g-í!4Nò\x0012ãöD)L]\x0003³IùËýûoØ\x001fè]Ê>\x0005cÍùÑÓ)©>ÛÀR:q:Mg\x0005>Ð«}ïéf£i\x0000~P¾¿}ÿõõ\x001e"¹í\x0006×#H%ï»¬¥(ê\x0016ye~¿¼¼]B ·pÝ.\x001b	¥\x001aIJ)ã\x001c³BR³
cl~uª
äöf\x0014\x001aõ\w\x0012\x000f¾Ã_Ñ==ußõÓýÛ¿/_^\x001fùíþm{\ì±\x0006¥òÃH¥Ö¡êEJ®¢ÏÏ»¯ü|±¼¾=ûøÃòîý\x0010þgø#XäöAÚ.õ<¢Ó¯ÿøíËRáy2]¢)Øæ)±\x0012+ñlN¬´\x0015d²?\x0010\x0012­òQw\x0003ÈØ\x0012\x0008óóF\x0010¡OçG\x001dm²;`\x0015\x0005õd\x0003¢*øÚÈ3"?ÈXÉ\x0006"Ýá\x0004×_¤°i`öÀ\x000c'ÃÁè.¥nâs©0Èæù©û÷î\x0006²²\x0004BÍü\x0011@!zÊ*AaÅ$Ü\x0001@Âä)ÒUì°\x0007fDz\x001cÏnx¶ë\x00145\x0016µ÷ÕÛÊ\x001e@lQÛq\x001a[.IÝ\x0003É´¨½\x0008>\x0013Uê{\x0010±EmÇ-j\x000f«HÓ¦R¢²N¦w2\x0000ª*îwó86CnÜ\x000ciXDéíZa\x0001³OHFAËÚ7l{µ¾9è,#Þ\x001c@Âô¨,®\x0012\x0018v\x001f6NKwm¡ÒBfH½ÝÎ\x000eÆnôÿÃ\x000fÊ®X\x000fß\x0016\x001f\x001e^~¿dO³£î\x001b\x001c"Uù[ìQ®5L0ù·ù\x001bwÐÔaju³ø°º>¿$g³µþ;s«[MãÆ:7KGTµôLÞ	\x001bfÓ¬nC\x001f\x000c{n]rëIÜ\x000e¢\x000e
ã,,Sº\x001aÀ\x0014â¶Õ#c;·+¹Ý$n	ç#:KÃ\x0008Rïjí½Y\x000f¢òbSVÊº@¡[ábâR±8Ï)ç kÁJÕâª¤Õæ)ïoC\x0013¸\x0006®C\x0016áÀ\x0014±|ë(ò5Rpõ\x0003j3x`àa
8Ö\x0012\x001aöd5DÜùâÅV7ø-\x0005;VóGø+5}xø\x0005V/\x000fÛ\x0015ö!"ìX:í«,\x001fãËê\x0002ÚUE\x000ckù\x000f«p¸º^½¯¯ßsÓ4qf9eý±S=\x0003\x001bN'\x0002­·èòì\x0006E-:þnm×Ü?=|½ÿúËÃâÓóÛ¯÷_wT5àý-u¨êº\x0017Q¹~ ¥+]\x001c¼AU°¼ü\x0008ëàêîtùéªv	±8øwtð\x001fO)}
Â\x000e¸Ôd'\°_\x0008ì\x0005	Ûu£^\x0016>XWá}ÏÃëãëâóÛãëú\x001a-³8 Q*÷§r`ÉÍÙú-1Yá]Ïêöìvñùîìv.`Fµ%ª#ªÑ¿/â\x0007m*nïçmW\x0019?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹
ÿãø¿½\x001f\x001f+\x0000Ã+\x000c;Î·\x0008: AK	GzIÖè¾,Ôê·øõöþæ¹ìW0_­mé$\x0017Ø<\x0002"ðâÃk#°F&,=îí+úY¹Ë\x0001\x001e2¶ãc5¼§êÀÿËÛ»%Ùu#Y¢S	t\x0018Þp\x0018¿BT\x0019i|ÈøH³®²H)RÉ.Lã#­«¿j\x001a5ÛºÓÐLj$\x0017\x000e¸co\x001cÕ9\x00006\x0010·ËªÌ^íp8\x001cîk\x0019½í¤Áixé\x001d´\x001aÌzÁÿ]üÛWP\x000f;¶¶\x001bÅ«¿<|ùÇû~n'¥Ì!A\x0016Zò\x000bÊ\x0010¥¼¹úËí\x001fïÎ\x0012:íÀ"íq°.hYv¨\x000eÌ&é!8öív:Ø6Íe\x0019¸qÿ	ZÛ<\x0004«i4-\x001a\x0003mÞ\x0019\x0006à¦Wé)¸ü\x001eázÒZBZ\x0012ÿÚýp\x0013ùáÔê*Ë'ÅW®F)Fë\x0017..\x0016¶\x0014Lì3\x0011\x0004½èj|á	eóuh³ab£©Âñ{^	
û¡°\x0017FDÇá Ô\x0004\_6Zk¸kÅYÛ¬K\x000e EÉf?ã
"å[V\x000c\x0005$Õì\x0003km9Ñ~qîGÇ¥
X<pÛÚ\x0006~ \x000fÅ\x0015÷Ø~¸øcå\x000c\+iÈ6.®&ÞNlL·ÝW\x0011¸$Ã<\x0001WQ#¯.¿äïVwa\x0014Ã;¥33p¬â\x0002y/Q¬Ý\x001eÖ\x000f÷tøô\x0000\OÏÊy§ñ4Èv_m÷îöÃÅñ1
cÀ¬Þé\x0000T2²[\x0018;/86\x000e­Ã
f\x0013"\ÃQ\x0017\àÕí¨ù\x000fÀµØd<µºEl¼O\x000br\x0006[a¡/`ãÂ\x0013)¦\x0012\x0006ÁSqu%¶\x0019S.gc¦ý\x000cÔ7u\x0016Ë©å
ûÚÆmç)ùà\"g\x0018Æ¼Aéãë\x001b/\x0010$Sm2è\x000cäÍ¦\x0017&çÎÏq¼FÑXò\x0007ÊÎ*ëkU¬~¼*=
ú»WÂ1ù.ò-d5\x0005¤ræ\x0014R\x0017E\x0019Æ«ñ\x001aþÀË=u\x0011¯"±\x0014©JÙDgß\x001d$òéãpã\x001e®\x0015>³*(Á*Õâ<«þ8\Àû\x0004L\(<\x000e6ú-å¹yPRÝ¶n³\x00197f\x0006.)J\x001cc-\x0005Ì\x0001)äÂ´ÌxÄë§ðº\x0018\x001cò]Ø\x0004ÏcÜZ13NÎ¥\x0016áµX@L\x001cÆhL³;ô(Â\x000béØ\x0010ôºÃÂâ³µ3ëkæ¼×\x0000_À¨Ü¼\x001añ.Ìt\x001cÖÜLáÉc\x0000\x0004×{½¦à¶\x0008úñâ\x0005ÈÍÜ¼5<ð:âe6B1Þ6GL?ÞÌ\x00037ã¾ød¶åÍÞk-I+ ÜË(ÐÝL*iã%3Pt\x0000Acj·xo»]¼\x001f/¾{9?×i\x001aÇÕÛh¼\x0006y¦A÷~\x001d^DôÄ©í\x0016/BÄrl
a\x00108\x0011Ì#øÇ~8¯fR_\x0017ó]­K4ù0vÊð ÖE_×OE_§¸Ñ:á
×Ð\x0003îb¼ØDáÝ\x0014Þ\x0018\x001eT8=Ý/4þÐ\x001e\x001aÀoäSñ\x0001{\x0018.s9\x0000\x0016þJxXè¾\x0018\x0019üTxÀ¦ @á\x0017Úö\x0000/Ì·=uÛ\x0017_ÙÓ\x001fÇñÂ\x0016Î@aâäd\x0007\x0016¾«¤'Fª<¸\x0018ÎèIÐ\x0008dS´.xÛ¼\ýxq+ÀT8ó"\x0011½d¼ÃÙ¶ºa]êÕ'0UwðÒpðµBÑ {Dë|J»³\x001f/þwÁTnlKÆ\x0012^Ã\\x0002\x0014ü\x0012ÞuEIÀ÷[°Sëk\x000c0$y\x001aÚlÁp*\x0019\x0016V¨\x0001Kp`gRIoB)\x00083î\x0017D¹Y\x0004¿î¬\x0000<&`ê¬É\x0003M¥~\x0001ÊÍ@R.¹.0\x0004¼\x0001©kÇä \x0002\x000b\x0015Å[1WÌÄBW\x0008Ø\x0014ä+ÄàÅ/m8gMKË½
rañ?àëpy"ö\x0010¿¾ärº¤qNðå%¨cB¹\x001f.\x0016sÂTE'\x001e1×\=u4$\x0004ÀLã¨É»\x000e-ÆÛ0\x0015tA[nâÂ+ºQ ZriY\\x0007\x0017sÝ0ð&uiò\ãhl\x000c²®\x0014OW67°¦RÕ¢} iÀ¤æYÜü¾âCÁ,Æ6ÚCLvÍ\x001dU (ù\x0005Úv6´»B¨ÿÍýo÷$\x0000AÒ¯¯¿=\Ý|üúéãû¨Uñåk¿\x000f©{$ÂµZ0³\x0016\x0004GW!ÏBgñ¾»½ºyùöÕË»(YñæíYY\x001dbjAlè²\x0019\x0011[\x001ax
fI¼<ß{\x0007\x0010³ÈÆä"ç9&«7B÷àe|!8\x0002)Åg |4GÄé\x0017XÙèGüü_ê'Å\x0015t2ü\x0017"N2~ýëý×÷ë«ÿë?þóæo\x001b{_~úÜ¯±
q\x0007&+0DV\x0014Küï8ÊG+¾zñÝÍÛÿí«\x001f^#!7þã¯^SX-\x0016ITOK,7ÉS¥Û\x001amY®9ð4÷ê¼¶ø¬M&\x0011z<ÂgB¡BmrºÙ\x0000\x001bÔÉ&{^VqÖ&©3ÖÛä-\x0003Ö
`mÓà4Û\x0014.\x0014A&m*Ê«mr\x001eyù³M\x000eKÖÉ¦èlÓ\x0005êÈI ÑX<Âw²29¤`ó iÐ'Úüx1\x0002r\x0005<M@\x0017\x0015Z'(F\x0018*\x0010Åït¡ÇîM\x0010>þío\x000f§gÏóßûôñþóÏñ\x0010úÛ§/_Þwâ¤û¬âmê³q¿pkr\x0017¯Þ¡\x0008Ä«7¯¿§Ð\x000f¯Þ¼¹kbFòPü×\x0014f|´ÙðèÑ´ß#æ\x000bý	G0èß\x001cfÏµ\x0002Ð\x000eÛ3fR\x001eÏ\x000bê\x001dÁ=\x0004zvãYA#n»\x0013fÃMð\x0017X( &%¸9ÄÇÛ\x001a\x0004Ò
¿DÄ\x0017^G`æþç)ÌG
\x0010s°\x0019³eÄSìQÄ©\x001fDÌ"\x0006fFÄ4\x001cf,\x000f&ÅU>ÿD}\x00043\x0012¸Ïzs¬V\x0006F^R0Ä©n¿2<\x0003\x00194\x0017>À(ê\x0004Ú\x0012æ.(\x0006\x001eÂ4'1ãõ0[¦\x0008&°²ºô<y\x0000³O\x000fÖ³=£`ñ&ó|\x0006+DÙ\x0017\x0006<Æ1ï\x0006\x0004'@k¥ñ½$/41ÈÅ\x000b¤á@\x0007\x0017h>\x000f`FYÚôÇ\x0014æ¸º4²bBùî\x0011¬£^\x0011§ÅJÞõNaf\x0011L\x001d\x0014°Ê¡u|nÇ~ñ\x000e8
\x001a?[úc
t \x0005\x0014ÉÞQ\x0006Gµº t\x0000sâ\x0017ô\x0001\x001a9-¨­\x000c«ùÂ\x0013\x0017úòÃ\x0001ÐÈÞþZh\x0010Ä·¥qÀÖY°?«\x000b½DãU\x0012JVé^,Iº\x000eëÓÖ'\x0015´]ºÎi	Ò\x001fS µ Æ\x0019s,Yo/$ÉÜ\x000cú\x0012EØ\x0011Ð
A«ÙvTï5\x0002\x0005R\x0019´$Ðñu¾>Ý
úßøEº
õóo?½øxõÝ§o\x001fzIZ|@ý <+ï¹à\x0010\x0004Ò\x0005\x0011uÈ77DûîéÝíË«ï^½{~ e\x0007\x0015×w\x0002ªðÜX)(c¿\x001dc½@9µHv\x001e\x0006[\x001aP\x001dªUSÙ?\x0014z\x0013}á\x0001k\x0014,\x001ewåÈ;\x0000\x0016\x0000¸û\x0014y<é8lÍÞ¤\x0007FÁ&¹0\x0001\x0016Ö\x0008l¼Rg:¾»ÑÊÊ\x000bl7£`±«\x0019fÀæwµ\x000cVÒÈ\x0015\x0004Éä\x0002R\ fì\x0003ûoÿød¾ü-í/ìmÈX_~úúùá|ÿk7R\x0017/¤Y_Àª ®éé](~¸Ô*\x0010¾|õöõíÕ÷7/Ú0ËÜû1¨M¯éu*Mº¦ö\x0016 ö\x0016'¿\x0018\x0005\x0006âQÀÇÁ\x0001 7UÞ\x0012\x00198`C\x0006jÃå;þ\x0008Ð]Ùç\x0008Ð@Ç¬MaÒ\x000b¥½Ô7\x0008tWí9\x0000Ô\x0005ºIX,ùÐk\x0013KnE þòÎ\x001f\x0001
8ïs\x0018h<TsKSüôt\x0010!~qÅ+z9Û\x001a\x0000º¯\x001cYQ9¸â\x0007V\x0006\x0000I}¯¨}ñ\x000e<\x0013%\x0004/¨\x0017Óz\x00048=ãôëp&	¾Ã8ejUÉ\x000bjK#¦¡4\ÐU\x001f~æ\x001f\x0000
\x001f9
¨éÎÐáþbÞ7\x0002\x0014ëÌÌ\x000f\x001cE=17ÆOO}@¸§Víyìb´n&8eæ@H\x0004	'X^ÐË¯\\x00038÷Õ¯#.ªJ\x0010kËÝ·ÆØt¹\x001fe\x0004(³\x0017\x001c\x0002\x000cd¾¼ÓÄ\x0017\x0003^\x0012.\x00103
\x0002\x001bÞ\x001fßô`ù Ç\x001dbèäO//Ì\x0001ÅWEÇ÷âV$\x0015\x0002I
\x0003(zÙA «p2\x0011Ä1ÂÒKC:\x0014y¿%$«SÀÎ¿Ã{É\x0006O
qA~·Wü´\x001dÿóR¼º||\x0004©.Éhá&HuÙL\x0017\x001aÆ\x001a,±Ã'E9\x0017>ë\x0003õ^jÏgýªÜI&Q\x0017søh\x0001æ\x0002Òa\x000ftØ-Ë³sH?~¿ý#$7þ\x001e({úñýÃçÏ\x000fW/îßùrßÝ° \x001dÕ@à
¨\x001cqØ1BýñîöuÄúâæîÍ\x0016Ú$a)ùât\x000c.rÕè\x000c\x0017DIO4¥Ü%Qîq¼Jã0^+ê8âÕ4r\x0001+SN\`å\x001b/\x0019ÁÅR\x001fy\x000326ÒòÎ_'/7\x001föàÅ\x0012\x001a2'D$Û_<ÁOn>|xÈí87¿|~ÿÓ·\x000f_\x001f¾}îîZ8éM7\1IØa
uuá.póüùmîÿ½yöúîé»çooß½>×\x0004Ì\x0006\x0018[\x0019­y\x0003*\x0006\x0010á¤0J>\x0005¶þ\x0004vÁ'\x0008¨1X,`E9ã\x0005g\x000fèC\x0016@m\x0001Ì[à
µ$\x000b¨aX(Ö´Uþ¼®Õ\x0011\x000b-{gA"Ï´ÀJjA\x0003%ÓÀWbÃ)Ê«êB1ä\x0005ZV\x0016àãÎ¤\x0005\x0010²ÚÈ\x0016;Ó©¦³\x0019àô\x0013üúûû¯\x000f?}}è§#Âmâ\x000fÖ\x0012|åI\x0019-^÷Î¿Åïà¿~ú§»··OßÞ¶Ð
½E/%Pÿ\x0011öÉ¢jaâ\x001fa½1zü_\x0007\x001f*ø0¿øÌñìvËÕ§\x0008$ÎÏá\x001d@/ãwÞ¡Ç³ð\x0003\x000bEøÓqåyñíùÝ#ðkÏÓ®Î7nÜT< ¢²Ñãp]Oèéïkø~\x001e>W\x0016@Äû%=Êh%(ê|â~\x0000¿°Ç?'ñ+KRC ¥&úTÐÈþñ»¥Þ¯¯\x0002'¾\x0005Îá\x0017<`\x0014.¸æÐ#9ÿqçßÀß%p\x0008ÿ$;°y\x0003°¶¼ÒÙ"4\x000b¦
\x0005bÕî5TéÝþâÉIööùë«gïÿñwlcïgsBU­\x0014>÷e0Ø"\x000b\x000e^\x0000\x00005({LxûæêÙë\x001fÿ
ìgÍ*S\x00173â_<©¬À'Õû¿<ôç\x000eØ\x000fBùPØ
·^
Ag/\x0001ø¬zóòÙíùÔ°Ë°Ç.Ã$x$Ðbðd3AR¿2?Odx\x0000¼²{ðÊN\x000f\x000e#f\x0006\x000fDÑ
Ò\x0019Î{BOðì\x0006¯«×s+\x000c)×=0\x000er2öóÅ\x0003ØMµðfná=v\x0013íÔ%zÆ \x000böóì¢\x0007°[¿Çný$vQ°3ó¡,\x001es~\x0008â\x0000rW­º]u\x0012Ür°Wj\x0007¾#Oî\x0001ý&Rº
¼{?wèÞÿõÃÀ\x0005Ë\x001bï(Op\x000e
qIiE\x0003pçK6ìOo¾{~év%58L¼·Õ\x000eóôþógì¡\x001bXw\x0019\x0011æ	%ï#m£QÁ2¤Z`\x0007ö×¯±îÒÂ'Ý3Øþ"ÍJìà¿ÿåþÃÀá\x001a3ú\x001f Òt!3Ìn\x001fÄùnø\x001dô»g7Ï/\x001cª\x0019¶
{Ø6ÌÀ\x0006 îm´<TÔ±r\x0008»çTêíô\x001e¶ÓS°YÕìh`-\x001e\x000b#\x001eÃ¨MÚL.¶$Ðçq-õ]DÐçGÙ\x0006A£ºü\x000e4þA-IhÎX'Iã4®5Ñæ¹xô÷\x0004.Ü²r\x0011)§|Ä;ª4\x0019\x001boÞÄ½k5µ7ó~£¨u½Úzjµ½§a\x000fütôXÍ"\x0017(Waû\x001a¶\x001b!"l`ò´\x001dìp~Nl\x0014·\x0015n+gpGÖ\x00197öo\x0011ôî\x0018\x0017iøz¹ýÔr\x001bKÔÆ¥1\x0013ó¢sdÜºç&Ô\x001bÉw¸ñç\x0004níèõÔ8o¸kÂ°ÿ\x0005\x001dE¤>Üªr\x0013ü9\x001bH^%âæÁÍ¸Þ4Rè3\x001bð"Üõz«©õ6ê\x001b\x0004É¬DØDØç'¾Ga[¨`[ÝÜÛócÀÛ²§PÑ\x0005[*\x0005ÄÇa[\x0011¨¿.CY)l\I°¥±«¼ÛÔ»ÒÌíJ\x001cÍê`-
Ìb6E=
J±\x0018Å]fî¬t<°\x0017q\x001bîa¸\x0003ã>ßl=Û»
·w\x0013¸5¾ì'ÁÂu>+cÊMË­eÏÕ¸\x000fv¨®
øs\x0002v\x0010XvN°av¶xÝ¡à\x001d¯i\x000bÎx°4à´ýÅ]èFIê§>þôéóÏÝ=;J\x0000ÏHz)Y&@\x001aâwJ'Öfàñï¯¾zùôÕëïÏêi3vµÇ®æ°KP¬M\x001dÿ=6%ìR1öÔuµ\x000e»Þc×³ë.¨\x0000ÜüÌ\x0016\x0013M&\x000f0í,e\x0004»Ùc7ëÝ§ä3`yàHÂ.q^6é\x0008t»ng]Æ0/»÷ûÑ¥\x000c²p¦4/l#ØÝ\x001e»Än\x001c¬úèùT%OØ´îÍ>\x0002Ýï¡ûIè¾Èú [\x0000$ÖÈhNÿ|§í\x0001ìÛûb0»U5\x0015TðBâVeþ\x0017±4ÌèÊgô¬ÓÄ¸ãÙJ#Ãqµ5]>n_>\x0007ÀÛjåíäÊc/\x001e±ü#)2ëE±p£º0ßz\x0000»¯Î&?}8yfåô^ðíYª²[Ýyåç\x0003à¡:`òt\x000eö¡\x001aò\x0002³øóýûG W\x000e\x000f³\x000e\x000f\x0015\x0013=VçÈá%G\x001a¿tÙCå3aÖg-ì<¥-®;ð|¿8ß:\x000e^ª*ÄK5\x001bäã¦='èø\x001f.K¿\x0012¼©\x001c>ezSàeù)O#´INÙ§Bw5ôYÐÃ¶Y\x00037:xu\x000f5ø0	^Zz\x001bÂ.ll¢MàYY\x0002÷ë\x0018\x001f£\x0014kJ\x001eÙ\x0012T7ìÛ\x000f\x000f?}ýü\x001egÚû_å4³\x0002©*Ó«ÍÂ#\x0011ûyÅÈíÚwûüöéÛ×w8Ø~öîgDÂ¯ÊêÇ¿x¢ª+ë³O¿þþ¿~î¾µ:0û¾$6ýæYêz÷ø;^/Ý¾zqûöõùk+AßN(^w,C\x000fÎ\x0010×<fbLz-µ¢~\x0017yA3c\x0004»Ma^´&þER}ß°ßýúÏï\x001dyÆZX®q8\x000f\x0002ü\x000c\x001dò\x0005£Úwî7Ww/~|}÷âÒC4ßº\x0005\x0011|Ý,x\x0000<N¢(\x0002ïË\x0014¢"æ\x0008Þt4{õW\x0015x5	>ºÎàq»ZM³TD\x0001F§ý=\x0002ÞUàÝ,xAý.Xá!\x0015/¼fðf%x¨Ü\x0006fÝF[j\x000enc¸\x0007ÀcC\x0007¹M;§\x001c\x0000\x001fô\x001e|ÐàUÀ«\x000c^q©'f¼½}{\x001dÁn*ìf\x0016»"v\x0018¼¨rg£\x000bMÏkX?ö*PÙ@)Ø\x0003\x001c^ÂI	Ç\x0005Y<¾çå´\x001f|¨ÀÙ×ôràð\x0012n\x0019¼g¯¡£\x0002ß\x000b~×àO:ò,½§óÕI\x0000nÈpô
F¶Ê\x0001ðRTà¥\x0005/©¸êR°³×ô\x000crôC75ôÙí*,7"cn@Ï®8MGo\x0004¼«ÁOP&0åC\x0004ïÊ~u¾$6v©×ø\x001a½]zC\x000ce\x000egVé9ÁÑ\x0000\x0013ú|Ï\x0018b7zU¯½^{Eí¸öhö°¡w¬êy\x0018îG_¯½\{Té\x0013äöø\x001aO£xË&×\\x0006^WIeÌ\x0002\x000fZbÌâ6yéI«\x0018óÔ¶FogÑ\x0003\x000fô>ÎYÍ9±8Ï/p\x0000½©ÝÞÌº½g4\x0015W*:9
PNÙùÍ®úÑO²¤\x0015×^³*·c¦¸ö+ï#ÒÖÇ¬<fO}3yí-U\x001dÌ\x000b\x0012CG°×{ÖÎîYg¨p=]ccÀñÞ®8V×è'/$¨\x001b\x0002>~\x0004`ô#NÇÔ\x0000zWûõ\x001blH¡ÌØ\x0007î\x0005rRð]°kÔ¶\x001f}½önvím F|'"t|Vu\x0014éGÐ×\x0011ÇÍF\x001c+\x0010rF¯£Å	\x0012Z\x0000ÝÕDÛÞ§Ø]vì$Ç\x001fÿöéó¯÷_\x0007+®qãÒ9òLÉRqÍa'xß3*|÷òW¯_Ü¼m\x0014]³\x0011JìPb\x0011ÖmF(n\x0017¢\x00137à{vï	P\x0000\x000bL0.4Q3
-è#\x0016ìs6ÿä$e;fAQ{\x0016\x0014âT-éé\x0001èÙ
#FØÊ\x0008»Â\x0008ÅÚÑ\x001eG¡Ù["_\x000f\x001eÄº/AoüÛÆ7þ²§ÿüpÿñêùÃÏï\x001f¾õ¢\x0017ØÁE*¡NÑÑGÐôd(üyi¹þÏ·7/¯ß~wûî,ì j¾\x0008Ç¤ÜÃþøÅ¯>ÿÔ<5ðJtwu·\x0008©@ëå\x0007¿ËÏ
è^ï¡{=\x0007ÝÅ¸oXë\x0019½,¡µw\x0007
yE\x001ecN¦ÙIJL|Ç
²@oÔú¡KQAÇsØ5	'ìDã\x0016\x0003/Ø-;2\x0007ì±ËIgwJ¢`Æ.Iµ\x000b¯çììá<iw?vëBÝxfqvc\x001f"ûú÷I\x0017§úq)\x000eßóhv!E1¡ã }þîí.
L\x0012ni÷¸¥\x0000S´t'Ç`È Ò\x0003\x000fÙÚ\x001eFNà¦\x0002næ+wm2nÔ\x0004¡¦§À<(Vv¨°·+\x0015Â®oTÃ°Q×\x001c\x0005$K\x0013Ù	\x0008lÏ¤	º\x0013K:i±¢J'_üþÛ×\x0011àøB% °u\x0015sD´\@Ðñÿâöm\x000fn]áÖs¸Y\x0003Ó!s¹£2w0\<ð=Ó7¸MÛÌáæ>(.	7Ë\x001fô\x000etâö\x0015n?[x\x001arÊ\x0004æWr ¸:|ADm\x0014·ªp«)ÜXÕ\x0016´Þñð§»¶+¯Æ\x0017ä"aC\x0005\x001bæ[\{Cn¢JÀë²-MG<éÃ½]\x0010w}1\x001a_nÖÃþTfEu®TS/ðß\x000fã®Â
'\x0006J\x001dU\x0019KkØkØ=4&°+ïÖsÞ
ºtt\x0018É8Î÷íêo\x001fì­ì°ëªû0l\x001fø±FYsMB\x001eÎ¸\x0012¼Ï3¦\x000fã®ÛÌ-wL¥\x0014\x0005\x0013\x001d°->ã6\5u=Ï}¸muÈÛ©CÞxKz$é°ä÷%#9t\x0015*:qW¥:,Wtm¸\x0015S8\x001e@Ü\x001d}n¸mÛÎâ¦7%3\x0013q³»\x001e"Î>Ü®Zo7·Þ¸È²\x001c\Vgïö=]J¨«Õvs«\x001d\x000f\x001aIM>Z\x0011ù]¼q\x0018(:îh}°}µ)ýÜ¦4@WtäP7\x0013ü~ÔÅ6Û	[V°åX~÷RZrùÜIË¸mX\x001bªÌ\x0004æ2\x0013\c_Jª;QÞ:\x0006÷ºqW	Ìe&VRÐ)\x0015J\x0017,½\x0001v]ìê¹3\x001e\x0003\x001fû	p}Ó\x0006]¶åy}aÜ¡Â\x001dæüÄ\x0013`\o(þM\¸ÞëRÁPá\x000e¸\x0005÷Ç*ey\x001eØ\x0006vokVÁâ¤þ0W\x0010åÆ #nb?tÀ\x001dÕÖô°t\x0002¯/òbî°T\x0006~¢'jµ´àÞ+COÉ§\x0013¸­Ï§Þ£§1`\x001boiì*j«\x0004<|(A?	9¢üþ\x001b\x0001ÿùÓûÁ`èpä:9\x000b*\x0000R0T|øX\x0004üîõ«»èãcýn\x001bÿb÷nûòSü__;A\x0008\x0016S@¤,x¼
YÔ¨ø\x001dA7òª¯âÿzÛ\x0000»Í³¹Ôpx\x0010l¼\x0008[\x0002\x001bWØ\x0013X·=¯\x000e6\x0000v»% Øí0\x0008Ö\,6Øx_\x00152¤g\x0015±¶$\x0007º°nÙ\x0013bÝ²§A¬»t:µRüôd}k\x0016¹\x000fl¨À`$¨Is\x0019+¥\x001cÎêVG\x0017T¨|\x0000ú@¼³\x0010§ÌUà d`¤¾uXw!Ý¢\x0018"
î R\x0019®\x0015\x0001\x0015D\x0012¢ã\x0016¬­·\x001e¬»6~Äºkã\x001f\x0005Ëã6&¦öôò\x0015Ñ²¼m\x0016N»Ðª\x001a­:Ö'1sr\x0002<Ò²è¶%\x0012Ö\x001d°V 8}Bò_ÿñ¯>¼ÿg<Ìz1«x\x0016\x0008\x001a\x0018¶õ"f!ã5wÐq\½z~÷x5oOF|ÿdt\x0008:JZû2"O³X\x0012«\x001aDMÐLé¾I- t-'¡»@4çø*"}X3\x0017Y\x0008ÝÔþ2ë0\x0016 Ys¨Ø«¤dÆ\x001fßÃÄÑ	ÝU«îfWÝZjØÐ
Ó*±q*¬[tç*än\x00129Ê:ÒxypÜ\x001e®0·'èí\x0007¤nè¾îg¡#ãIîá\x001c\x001fyÑ%OÆÇÄy\x0019ô­TÐAÍBw¬H\x000fBñ³\x000c1\x0007Ú\x000f\x001b½ÐåÆ	b£²³Øí1\x000bnU¬û\x001eo¹=TEØMå1'L\x0010ãØ±\x001f9\x0017?\x0012v"\x0010|êkÕf¬îÆnë3ÉÎ\x001eJBsxDî\x0013nØÙC»S§\x00039#	ÄîHúñþ\x000bêuõæXR\x0003Þ\x00061k\x0011R\x0013\x001dqÐ\JuF·&®~¼y:]-¸ª«ÂUB¡Aâþ\\x000c*LÎØÖÜ~\x001fÚ[D´W¢+j\x0015-®¤ù \x001aDpqW õ\x0015Z\x0018­\x0010Äd\x0004RÑÚ:\x000exF·ª`}pww®\x0008w»s
Â\x00151ÿ ÊÞøÁhÈ4¤Ü)ÃU­S±\x000fn°{¸Á\x001eÔê\x0006,\x0004(¾ÀQÍ¨Ös\'Z¨ÐÂQ´(*Mû¬È\x0006\x0004EÌ$\x0008·ÕÝß\x0005w7xpwÇ£x1/
´º1åÐ´ºÌ²Ö\x001eÚíÃ«k¼ú0^íHc:âµ×t³\x0005ÏqLWA\x001fk«¨»7\x001b+\x000bãd\x0008:ÝtØ2llxm÷ðfSoX\x0001\x0002u\x0014bå×W¶\x001e¬:ñ\x001ao87î1Åx-
@ÀÖ´¦±úàº*8àÏCp=º¬t\x0004×2.«ÛÊûàî®"\x0008w»\x000cÃu\*\x000811¦\x001cG\x0016ÝiÝª}÷Á
õf\x000b\x00077G\x000f ÞÂP.ª!þlqÙÍ´}Ì\x000e/<1ªz\x0017ùñ÷ÿ÷§¿\x000fÍäá,	½YFÔ4d×Ç'ù\x001foþéÒ@\x001e#
9L"W¦¼¶\x0002ðÁ\x0002wAXÙf[ìî«E÷³Î¯ò¡\x000c4ØÀ]L\x000f½°]\x0005ÛMÂ\x0006Ö@Iï­À\x0014\x001bÜ\x0011kêè½ë¾5B tj8\x000eÝ (p^sSzK\x0005SXÙÓQÐ¼Zt]toC)^ÿy\x001cÃ\x0019îú¶ºÊ§\x0013z¨\x0016=Ì.ºåµ\x0018éÚJ¿\x000f/zkÀn\x0004y\x0015[ÂllÁ¾°Ü§¥cQZ\x001csàEïaøë¾\x001böBè<ì5±êþ9bJÍ\x0004ª`UOO[/ôPC\x000f³Ëné]ÃiQ*ìñ\x0013\x0014ìj¯cí{]ÎÆt«6Ñ¥1\x0019s*ruË®L\x0005]Ùàh\x00075B\x0017Ø~JÑQ2ô>NìºÆ®g±c3µ')ú~N,@µF\x001bG°»\x001aûlh×W.cwEä*(>OU['vS¯»]wµ\x001dKBóx£\x0005­\x0018{\x000fI'v[c·³ØcH\x000fì3¢\x0008.{f|²jÍ^Í\x0013»*_8Ñ²üñ!bì'õ.\x0006Å|#J\x0004\x001aÔ7æ\x0003ÓÞèÐ#¬óãmüÇ\x0017xg3ð]Ç\x001b\x0002?éx\x001bEn*cÇ\x001bÜÑk\x0007]\x0011æ2ð dª\x0002]\x001aÿâ­ZQßÜüúéãÇ!ñSaK\x0011H
Ìª\x0005ÒmO³õo_½|y©qÐØ£\x00071\x001e1r\x0007\x0019 \x001d¡
<\x0015KcÈÊôPôÃß\x0008D\x0011~M :\x000eß\x0011ä\x0014\x0012_4\x0014ô\x001dyû\x0000z¨ÐÃ4zÖüMè\x0005\x0013E³0zß\x0011à»áKUÁj\x001e?Ð\x0001W5|\x001cø®rý\x0013ª§Cð\x0003UÃóò³¾Ú¿ã¾Úß×øý4þøßðµ×æqÀC\x00155%LM\x0017¤$0@á#*s\x0008/\x0018¿^ë<õÖó{×K±©Çø²þ\x001d	N7~µ)«!~ü9?^\x0003ó6`ë0Ó8(ÏW»$§\x001f¿®üGéYÿ\x0001
ë@j-°LÏÃ\x0007j÷¸uâ?Qª\x000fâT©þÍÃçÏß>\x000f\x001d»È3NéH¥K
W^²b:´XK\x0012úÛ×¯ß½nWÆìÁ+c&Ñ{EZ0	=	\x001c(~×èmÏÚ÷¢\x000f²B\x001fä\x001czÔ*#v0l^¢¸ÖÎ.^{r\x0006UÊ7ñ/¢ãWà¿~ûùý§^ä\x0011£ =k\x000ct
ÖÑxs=æÛwßß½j6\x0015h3\x0005\x001a«\x001d@kJÑ5Ü>ãD\x000fß@\x001fì­\x001ea×Ó°\x0015°X'£µÆGÜ÷ÛSVíC½Íj!êzVk\x0014u<hl\x0001#LÚÁ\x0014\x0012*\x001bÚÝ¨¥\x0016{Ôøs\x0002¶¬ò^ç7\x0018\x001asÖõT[°ÍIãl0uãì«·ñ\x000czøÐ/­
Rò!dg¾Í:Âô¦\x0017Z#-\x0008\x001cO Ûç\x0017ÄU	úÖ¾Ðë¹ýaè"pîn0[ê³qÜ¸\x0002=\½È}ÜO"\x0007 ¸ø¸*mÐCíÛ
\UÀÕ$p" 28]\x0014¨\x0011Ë\x001aS/t\x0016¨\x001cf\x0007
"tà!\x0008e xKO²Ø	]jÑñç\x0014væ³ÝÓ\x0007rqK
q\x0004»ª±«IìÚ\x0010Û\x0011ÖÑj\x0010¸gÀ÷T{±×¡QNÆFì;
°3u<J;ïa4éÆîkì~\x000e»kîDiG-M}\x000b×|\x001b)H¸ÁZb<F\x0013H\x0011>HÃ
âÆ÷¼À÷b¯C1ñê&8\x0007é''\²H7\x001b×ÃÜÓÂ.ã§MY9gø\x0017OTÉ\x0014ÿåþ×ÿô·þÂµãqF|,o\x0005Ä6bö
où\x0017·/ÿôês-²\x0000ÐF) H\x0004üÏß\x001e®n>þòpõýÃûÏú3rIýË\x001a¶he(t\x0017\x0018ÚÿrûòÝíÕÍËg¸Þw¯_5`oñ\x0010a§px\x001c¶fYr\x0000E´\x000fÁù*-.<\x0012\x000cÂÞ\x001f\x0010v}8\x000c[pW\x000eñºéxµ©
[e­ö&q°ÄñqØEH=\x0006mb\x0013°éñÑi}¡\x000f{\x0010¶«ÄÍ8BÑBjiÕz»¶ñè£¶f\x0019lo÷°Qtê8l\x0008DÊ\x0017a{"'\x00177nÒ×ö\x0002Ì ìP­vÚ"Ð%Bc=Ñ\x0006ÚÅI.ñÝ°½ªÉí0+Oäv\x0019öÏß®¾»ÿáÃ{îyóío8{Ã·Ò7§Q\x001fï$+\x0013ÅK~3\x0014Æ_ßÝÜ=~c>oÞýðCü¿i²½W£)é¹zÞ\x0014T¼Ì´¥\x001aùCØ\x0014Ig4åBsôQSvêhhJVG[`1¹\x001dO\x001bÉÇn³£\x0015æØ¡k;ô\x001a;¢{©\x001c\x0000_@\x0005a [ô\x0005Rã¶ØÚ\x0016»È¿\x001cïul0ôR,è.\x0012¿Ëæ«Ã¶(YÙ¢ä\x001a[`\x0007è»XÖ\x0012Ò³-ú\x0002Åïa[tý]ô¢ï\x0002¶ì\x0015V%S\x0002Õ-2Ã¬7ÅÕÛÞ­Ùö"°¬z\x0011mÑD4å\x0003ÏÏ`4~Ïâê­ï\x0016m}$Æ´ÅßH\x0004\x0013~õaLêdQbÍÑ"¬Äý·#n$\x001fT(§ä#XbkKÖl\x0016¤t¡¬O\x0018²%Aqã/Ý-1öây/Êm\x0002ñvø\x000e/ÈÿüÖ+H\x001eÊ

\x001bê@ý"1Vyÿ¾TÈè¿ÃËñ_ÞÕ¢'Ä\x001b¿7"þ8d¯ä èriÓ«@Ú^hS\x0018¼ñ½ äD÷r\x001026wÓ\\x0016Di\x001bÊû`ÜL¤:!ëÊ/ôcØ°AÖûÅÇsÚ] \x0006\x0018¼)Õ d#C6ØÀâEÒãgP\x000feGp'äm<.í>8\x000eY\x0003\x0007\x0018û2\x001blô°ÝÑÎ¿R!®\ÙM¸²($\x00113ÍÝÏx\x001b^´È¾ì' ÇÜÒÒ<¨úì\x0011Ú!ÄÛ¼:"\x0006s\x001c±ðXÕÉuy×ñRE^\x0014/BåÉá¸'#o \x001f$J9pkKääÂ\x0008äÝ½*\x001d$»{Õ8fn:Ñ\x0001\x0005À=aV\x001c0.uªa¶5f{\x001c3ÄÅ¥ý¬gD#¨k¦Y²ìÅ\x000c5æ	ßðºÌ©ÆuÖä\x001bª¸Æ\x0005Ñ¶!Èºv
=á\x001aNÁe)¸}@¡ò3-ó~¤1Ìu^¤'FÂ
.Â\x0007,
ä×P\x000e\x0013s`r\x0008ò6` \x001bq\x001c²	×½,"æÍ/¨³
avõ2»eÖ¶\x0004gÁÏ§}Ù\ Æ\x001c\x0003\o¿$\x0003å8a¾û\x001a#f]0_èò\x001aÃ\x001cjÌÇÏläeàãDèG¢¤F¬Iòw-Ôù^2áÌJoû¯ä\x0011s(\x001b°UùíÅ\\x001f'~â8Që#\x0010\x0004ßÿ¤cIJ­`\x0015fWc>~5\x0011\x0012\x00183ú\x0006JØPbó"wÞhâ\x0012dPG!û#à²$tÜYËr5Yihý¯}ÿåô\x0018Ä¿:|ªHfH\¯ÍôºsQ=>»Ó»««î®O\x001f¾Ü¾zõåË§\x000f÷ýAÏqQ<«©X\x0016\x000fp¦\x0005öÚ·`?½}sóúêÕ7¯ß4 ïî°®ºÃ\x001e.¹&ctÑýñY\x001c½nù÷\x0008r¨Ã$rMò¼qÑÕÖ\$\x000brÛª&
@·~\x000fÝú\x0019èqr\x0019/.ºâFhiméº¸ u7\x000c\x001d*)ñÁ+zé51\sË¨Ô|%GÊÐM\x0005ÝÌA\x0007~aL®^VÝ¥ùþ3\x0000<Tá%L\x0017oÓÆÑk =*§«\x000b\Þ£Ðw
\x0008]î*×Ç°kªDìÉÝ¥pÅ_ä:Wß=ç&ì»çÜCØqÒ}=^%ó½L\x0004(Ø×Eu©«]*õä6÷\x0006ê^Ôª¤Z\x0002GC2ô\x000bêãÐU
]MB\x00174¾<²qá·U_¹ìõa*çNS­FÔÀ\x0018Ó-îJ\x0017Ne·\x000b×Ý\x001aûdxwbG\x000cÜ\x000c#JQ
;4ÖawõNus;\x0015Ü\x001d?\x0001a×¥{y¡Ñx\x001c{\x001d!Ýd\x0014ü^T¦\ý\x00118?JØÅÌ\x001eìÊø­[â_dá\x000cýöÛ/¿ÿß\x000fWßúxÿóÃûÞ,\x000cuåÓÙ¹ò@f\x0004\x0017U¤lÞCoß=»E\x0001óW/o¾¿½kàßb
âßÃøæ¤´Ã7I\x001aÝ<\x0002#®d!þÍw\x0010ÿÎuâw|Fi\x0017Sy\x0006¥2þK\x0003\x0007ðÊÂ¼ÿ\x0018&+ë/HOÅ(Ò
uñÄZé>;Fs\x0019Íçðã55ã·Á3~àr³°j)~¨?÷¬Oá×Ògé\x0015m±·º{ù¼J\x0014Xëàëí]>íÞÝÃüQø\x0006®=u
ne0Ë/Ç\x0016|³ÖÑgÖ¢n¬±o¬Æ\x001fÞ¸ÿåã\x0000kD2dQÄU\x0019¦É{7þófcÊí«\x001fîß<{y~Úo³¥ÜË9äÎ^\x001bFî(W\x0000\x0007Ô\x0016_ /\x001d®+èz\x0012ºÁ\x0002MîO\x001c¡{\x000eÍVå\x0001èPù\x000bÌùKÜ49h\x0015¾æ,¯é¬òN^àG\x001a.eå0RÎ{LîÇ·È¸ï\x0002E\x001aïmöõc×5v=]b¡#a×dêÐe\x000caïhM\x001eÀ\x001ejìa\x000e»
ÔB\x0011±»¢¥\x000b\x0014 ½³Í·\x0001ìÆVØÄî©m£ãÅ*c§äÀãñº\x0010;ÔØaÚgòM0a\x0007Æ\x001e
ô[ÕÖîngÝ_Ð-^bYË\x001d·ªnvc`×5öÉèn\x0013ñwÂní50vÒÖëÞ¼\x0008\x000e`¯\x000f&9{2YS°#µ\x0013\x001fªÃ»¿@)4}Ë$\x0013ö]&y\x0014;%\x0004\x001a|áØ\x0004Åa&¸u[u×&Ø«6áCØí5EHpE\x001et~\x000cw\x0018º®]éÙe÷èãÝ(G¯7\x0018eÈÝ½Íù\x0001ì¡Æ>y2\x0019qmLÆ¢DmÊ¯Á\x001e)g×a·U"Ø;§°\x001bêþ´Æ¹³Â±÷V¯Äîkì~\x000e»\x000c¤8gsÈ \x0019·ùTõØJÆ±C}òT5L)k\x0007XËgwïhåï\x000euÉ(<\x0019¹ÁÈÂåUo_TG ×«\x000e«®gì@
\x0005àPp°_ [\x0019Å®ECj1CJAá´î4ÇmH\x001d.cw5öÉ(£='b\x0006iÝ\x001d\x0012Æº\x0010º¬Ì¾4s\x0008º`ú)kå¦¥ è1Á#Må:ì¦ÊµÌ\x0005wêFìîÎTÅA&B_èíF×Ð'SHTë3t(u\x001dv·.¶kS»u\x0019ÅÕ0«,Ù\x0013v:S¡ýî7tSÝ·.ñmu×ºtÄ\x0004\x0013Ì5%Á:`]2YÀkq»^ \x0019:\x0010'O-ÀX9iê&KK]ê1\úrLµ§Göí\x001fL{wÖ\x0004Ü\x0003ö@ \x0005¾j\x000f¬)«ZU\x000f fß§ÄW\x001fî¯~ø|ÿñ§ø\x0003E;¿}ýüð?^tËvBü\x0017°3îTAiâf±¡'Éÿàê×7/Æ\x001fW¯Þ½}}{õâ¼'\x0019µ«ZF£ªªå¬QÈ3\x0017hF6fÄÄ%\x000cÛd:ÊGlÚµµ M²J+¦²±ïýûZ\x0003OeªfèA£¶×Üd\x0012K¿!juÙ\x0007ëq?N\x0000·ÏA«\*o\x0003,ñ/ìæWÐßÿOï¿\}÷ûo\x0011ñ/ý\x001a¸H¹ãs#(Ã#ñÃQAN6;4\x0019¯îÞ\}w\x001bÿé³¦\x0015ÛK5Z±{©±"\x001e0D×\x00048h¦¨¿«¹Ò5Ãó°\x0019ÕÇÐk>FÐDa\x001b?ÆÖXE3ÿñ[4ûÙF­0\x0015f\x0015Øwoécà
ÉQf+\x000fI£Vì
\x0001Ñ]\x001d`Æ
\x0014¥´dÅ6ü ¸b\x001c,ÍØ&7ÐÝàÆ\x0019Z7m2¤\x0014Ðfö8jÆ&áf^b\x0006v2³\x0019@e \x0015ç_\x0012GÉ¨\x0019¡Ú\x001aaÍÖÀrpî%CµtCf \x0007a[¯NÃf¸Ê\x000c·Æ\x000cA\x0002¨ØÑ£¹Ùo±ñÐh%ôfHQmqü¹Â\x000eg®¾"1£ -¿\x001bËKÌ­ÇÌÕáÕÇ\x0016\x0001XIÈÃÏÁÚ°Ç¥¬?\ó9@ã/Ó\x0008$;t1ÚqAöeÔ\x000eçÛ·Z&²j\x0019¿ÿös4àýOW/ÞùúùþCÿÁQ:´·L\x000côþ¨õ¦Ù;ôÃëÛïo_ß=½zq÷æíëç
# 2\x0002\x0018íd\x000eT\x000cF\x0010\x001d³~Ö\x000eT#F`\x0013íÎÔS;m\x0005ÄTÝQ\x0017\x0017V¬2\x001fT¼ÿr\x0013 ¸ â4fELBR¾\x000e	lù.F<»ÿëç÷\x000f\x001f®nþ\x0008T{-ë]j\x0003[\x0002L&¶\x0011<\x0019?H+zvóÝë»ÛçW7ß%\x000eÕ\x0001¦2ÀÌ\x001aàp¸´²³ù^ëñEðûfã÷\x0018þmÂ\x0011ñï\x0006\x001câ ¹Ô+z8÷`x<F"óÓJ\x0003 ì
0mUÄ#\x0016wmG÷PúH¥o\x0012#Áß±Pò(üìõ\x0019?\x0015±\\x000b¿¹ðc§Ø~\x0003K3m\x0000^\x001eÈ\x0000\x0013¨ZÅ´¥Ò5ZÆàïxõ\x0010þWï(üx)Kð\x0015­¿\x000f÷¯m2\x001d\x0019°õ\x0001ä\x0000*¦
fk¤\x0006\x001a´ò¾09KÛL¹\x0007-Ú\x0002¶@8æ:pHfÏ\x0000ì®#\x000bts\x0000¥Ó\x0002\x001d\*mlÕ³é\x0004ðÙï¿}gñý\x0007¬¤=»ÿöáC÷\x0010³JM\x001a¬æa\x0014#ÎCAû\x0011æÝ\x00156%Çs\x0018khÏnÞ=~v 1r1JQÏ)öº3áqOÕÞØ\x0007l1-f-17mÉ\R!ÈGµÄVØe\x0018&\x0013Â¢fcm¹ \x001evÜ\x0016_Ùâ\x0017Ú¢Ø\x0016Ç%¸×iHyÑÁi8j­\Ì®s1M­\x0012\x001a\x000b\x001fqÅöãñ¸1®ú2nÝ\x0011Ìê
øÂÁ^¦\x0003\x00072ÓAÿ;l\x000cTÆÀ²@æ3\x0017ðÆÑ \x0017óo)ßn7\x001b7ÆWG_vÄ(C\x0010\x0015\x0004\x0012´19Û.6\x001c7¥Ú1~Ù\x0011i\x0008#;Yà·\x0000]æòU§ÿ-ª²E-û,:x£-\x0002;1ògáÒ¼B\x001d1EW¦èeÅÓ4°\x0006ì=2ôY\x0004ïýÐ,}\x001e1¦Úû~ÝÞWYµL+c\x0004@Ö|ý;`\x000cTQ\x0019Eea¯)¹ÀEPÍ¦hÑ\x0001:`Jõ]`Ùw	¢L\x0019\x00046S¦Ììº²IÖwÄP\x0019\x0013}\x0017éq2Æ\x0017(ÍìßñË¸G8úC\x0015Ãº¨¬?"~\x0019Y¨oZö\x0010M\x000f\x001bSí°nÇl¬RàXÂ\x0013s\x001a6¦.Ð\x0018¹\x001bRÆÈË|jÓH®T íAI\x000bZ{Âå1¡6fÕ¦AmR:e°'¿.âBz}`Þ\x0011¤&cäª[\x0019
iS
\x0015PÇ­Q¦|Ç°Æ×Ö¬Ú5h
ÓEãà)\x0019#È\x0011Iç×\x001bSû\çg\x001e÷}6Ær\x0019\x0003©WÙ\x001a½>8ïØ\x00065j£Y,+1É&\x0005gÏRsZ·'8ÆÑU¢¹ç»5Æ\x0014É«\x000f\x0010C.Wæ\x0011.;VÙdYv1ÛÉiÉ$:\x0018\x000e
ùþúë¬ëerYÁL\x0006EÄcÝ8ú4®P·ÇË\x000eXSÇ\x0000³.\x0006\x0008Ãåo£)Aó¦h94ù\x000fX\x0003µ§Á*OàJ\x000cðU\x0010µ/|â¡MÁpÀÚÓ`§¡(2q3\x001bQ®^q¾éÚ­óãÖúÛußÆs3ÀA\x0018wâiFõç\x000c[S6aÙiãÕ5ø¢\x0016$\x0019S\x0004«UÙ -ÊV_FÙe_ÆûMaV°P!>¹5Ö­¯Ñ¨ºØ¬U%Îo5Ú0y«¶ü:cl{¸í5®¶Æ-û6ÌÌb\x0012\x000f0Å\x0000Ç\JÆµçÝÆ­©+´jYVb³\x001aÉ¥£\x0010e\x0002Ö\x0015¡÷Çð´ºH«Ui¥+µH£ïéÖÉO³Æ=B5PÕ¥Mµ¬¶)$%Þ$íÍIa$ãÚ\x0014@\x0007¬ñµ5ËîiN0\x000f²°ÅP´±hö#l\x001b¨¿
,û6ø\x0006@\x0014*d\x000c÷ñ\x0018ìgXoLýijeü\x001eN\x0017øf8©ÁûõÆÔ\x0015Aµ¬$(­eJ\x001câRttRmÃ6¡Í\x0001[ê£&,;j,=¬Ðìe\x0005f§É¸1º.;éue'C54ºH$êJl¶¢=ï8nª¶\x000cþ\eL\x001cB\x0019>\x0001fSÔ#TitÝ× 56HÍßE*T'Ù\x0018â\x0008'æ#2ík'óËL\x000bæÂ19c)6I\ÎÚGh9Ayá½5°ÌüA5(¾ÄÖHv´ö\x001cÝ¸5FÔmMbYdF\x001cQ¯ÒRÝçéõðmª2\x0000ü¹È\x001aÉôcF	Áý@1öS>ã°n¹5ºê\x00080zUKTS\x0000dj¿
\x0019#\x001f!\x0008\x0018[\x001a»êÓ\x0000<xsâ¬\x0002n
ø\x001c°&Ô&,û4¨çC\x0016¯7T[çÎ¹¶NÎ\x0011kêo\x0013Ö}¸óóíYÙDâ¬Á	5²æ\x0011\x001a\x0003lÝBkõÐ
°×8Ñ\x0005
Ô$c\x001c7kzÑ¦>\x00187ÆTÆeÆK=Gvz34eù]Ð6Ò\x0001k ¶fUÓ\x0000Qt\x0002âÁC´Ê±1Pr²uÆ.+Ò\x0008\x0007ØÖlÁ¦@\x00124õ\x001a\x001eÃÍê²]VÖ\x0010X\x0008 [\x0014ñéâcZ=yW²ê~&åâYÌ¹YS\x0019Ñõmacb^±7\x0006®û.\x0004\x001eð¥áy\x0000ïôúw'§ªö\x0013ü¹È\x001aãè¥ÆÄ\x001bÚµ#k¦Éùð\x0018Æ¸Úeu\x0000§YkÆX(òîÜ²\x0005ú\x0011\x001ai®.5N¯ºÔ<Ûü\x000cJ#½RùÇf®~©qË^jP,ReM=\x0013
S,\x0005È×gPÐ\x0017àN:éµÒ\x000bÍoÏq×X~IW8Ò­\x0011bý·ñu7_ÖM#\x0004Pvf¼`Ñ\x0008R\x001dÙ\x0018Ûæå\x001e7FÕýçjÑíÙh\x0002P\x000cáÕ2yü\x0004Ì#¼:ùz.È/\x001b\x000c\x0012È\x0019F»\x0006\x0014Ñ\x0007D&kZrú:ÕôëRMaóL¯±RqFfcà\x0011®ØÜ²7Æ-ó³à¨\x001châ5Ú0é\x0003÷Ó&T_?:ùUN>Dç¢·Z«hÊÂ\x001f0¥noð«Ú\x001bâþçI\x0007cåû´<K\x0013dTxØ\x001a¨MXl&/Ó´g´e3éyÏ\x0004Ñä\x00169`¬ö\x000cÈu±YQÛ¦A!\x000bº9Ëò¶\x0019\x001e!£º\x0014\x0008«JÑ@ÝÉ\x0018*jHËÇæã\x0018£kc\x0016]6cÏZÞÆÆD\x001a©¹\x000756Áï\x0001klmÍ²\x0018\x0010\x000f~C»\x0006
[!zrá1\x001ai ®7ÁªzS\x000c@$®Æ"ÐË[Æ=Õ\x0019\x0000¬Ê\x0000âÑ×äeA\x0016{ÃéLpÐ
õt ¬\x001a\x000fß%°vr¼\x0017k4\x000f\x0008ÐfÔ<`M½gV½\x0008ú<ÙË\x0004n§'Ñ\x0002<Bâ\x000c¾\x001eÞò®4\x001eû©Îa»\x0016)·bLN\¢-á~ÀP\x0015iðç*OsåÛ`\x001bºå Àß&´\x0015«­	¢ªÒ\x0004±¨JãÚ24g$\x0013jHEýZ>
Á.·FVQ ÈeQ ÷Ïek ¨y+&ÜLÌ*Ë­QU&¨Eeh
3Q\x0018ç\x00043ÒÆ(Àûæ1Ê4AÕßF­û6Ë4HbdhßHV\\x0010²©nÀú\x0011-¬zDKd¢\x0016\x000e[g\x000b_¢¤fçøm\x001ea¶>ÔD4a\x0015\x0013\x000f\x001a¸gÃa#y\x001aÞgÈ\x001aõ\x0008ÖÔåÍ°ª¼\x0004Ú©Pã@Sxþ6ñ2ºÞú\x001d-¬zGKí:ßÓ\x001c¾C3°â(`\x001fö$Ôã\x001baÕø`Ù\x001ao\x0005ÎsezjÅüÔÑQg®Ä\x0010¨9`/0ùl«9ÁAñP2*¡ÜV\x0003ñp#Ô©Qø®¶Ì(	ò:(£·ù´ÀÓ\x001c ¬y
Ñ§6a1zM>\x0004àn\x0001+ìV(4«MEò\x0011£HôÉÛwü'g²êç\x000f?}xøüS÷>²d\x0011\x000fåAJ°¡\x001cz&x~ûôùíë§
36^R4C¹QÚç(k\x0007°2M@A<¦\x001eÉ?û\x000cÙ^;Ðs\x001dÃ\x001fD\x0012\x0001\x0001ÍbXAl$éaä\x0015ªÓ\x0010U\x0019r&S\x001b5ÄiÒ°(\x0012q\x000eI² \x0007rèNC 2äLcÐ\x0010o\x001dmv+añÉ ©&è\x001eIjú\x000cÙÒM4ä\¶9ìZ¶ðïãÜ\x0006¹\x0012\x0001(1r¼ô\x0019b+×²«\Ki4Ä|P4IÆUbXXlHåZvká\x0017¡\x0000$×\x0014}\x0015_¥ÜÀáØg¯Âï¹Î¦aC4\x000f\x0000\x0004¬Óæ¨EMZ^éKY!PísCÛ£@ÏA¢`Ú\x0006\x001f¿Çò½\x000eÕ\x0016E[\x0004²Í zcù\x0016Ë[d¨¡©Ó\x0010S\x0019r¦P6¼×å5ä\x001dÅ\¾&î9¯:ÄÑG
	Õ\x00179×Ì|À\x0010j1\x000b;] ÍêFªM_<j\x0014Õ\x0016Ák|K\x0012åIJÚìÕÛFzÿ;ípµ\x001dgª\x0007¾°dâaf¡ùF¬¼^\x001d}wä9Ésí>ÃÙoàð\x001bðÅ\x0012	\©\x0018#Îì³DU»]k^\x001c>H\x0014_±\x0008Ks2©n-\x0011Þ>KôÉdÕ¹æL\x0000Ão/§±¼V#äL@mÉ¢,ÅxÎR,
[ÂÚÂzg®Ï:m«òF[ÚHPK\x000fEÍ	°\x0016Ë¯$H[··Ä­Ú&Eõ\x0008_\x0005o\x0013>\x0015µ\x0008Ë-ñµ%~%\x0006pgçòL+\x0014IÔÄm2ò\x0016Þi¯-9Óq5jvDÃnãNdrÉDÊ-1«ÏE%*CXdpÔmiã/:ß!°¾v#×}\Ü\x0017ÝÜQ-ûEî\x0015\x0016üA]½I©Î\x0012u®_dø\x0008±"^x\x001d\x0007l^\x0017¼>K­,qgz\x0012F)A`®\x0015ñ,É}\x0010l)¦¬Î¸T\x001d¶Ôª°%ùõÞ²\x0000}\x0011°\x001c¶`yî¨Bí[çÆ\x0012G¿7T9µ1±Æ]²D³Ò§ÑË\x0003°V%úÜ\ò¨%N\x0013¬¨\x001fU¥\x0003Oó{cg\ºÎ\x001dõ¢Ü\x0011-qÙ"PêhÜÈI!¦*fësü£\x0018±É\x0012+ix\x0007â]·»\x001fyBí´\x0004jK\x0016U'møM45SÆoÂ!ÓV?\x001b¶ÄÖÎunF|ø\x0008\x000e]H\x0019Ö!Æ.Þ&0ò\x0010ÜgI\x0005ëEY°g¡§}\x0012ÓHOù¢ÄjÚbÃøêX<KÞ1j\x0002\x000b³\x0012U°ó\x0007 ¶\x001boÅòQ×å:½¨^çqS\x0010ö¬¯\x0000(Kß$¨åA8ÔßäÜØÁð7IwÝd	\x0012_çOâÙ¹¢Ë-\x000f]ÁÕ¬©s¥
OA\x0018\x0002\x0015µc\x0010¦vãè\Ëß}L}31n&^ZNèÊ\x000eFpÜ_dÕòobdmÉ9îîQKå\x0011Éâ\x0003\x0005aË5\x0015«G¨ z«Áû¦\x0008®\x0008k\x0018~8a5\x0002\x0013â¥s}©¥¨´ìÑ:\x0010o\x0007}Ì»äî öðéó/\x000f_®}û÷\x000f¿v«þ!\x00195\x0017\x001c[à|Ñ\x0007m¿a=»}õúÙí«gïþçËÛ\x0017ç\x0015M\x0016¨ÜµíÝfGè\x001fþý§÷\x001f\x001f¾ô®¿\x0007`\x001eÐ6:TVµ\x0002YØÓjÓ?"òçÿóéÝËÛ7
äÚîïg<@·dA
èëÀÈêQtÌÝö#ß_Ð+QÙcÈêîÑ7b~HÈ\x0003)\x0013öN?p[9ô\x0016kiÎI\x001b«©Ó,"'-_\x001b:\x0008)û¡»Ê[Ü¬·økCÈU\x001e\x0005F2g(ÀR7p)*àøs
92\x0019ä\x0000c¤")\x001d@\x001e@Â®íºE[7yÂ¾ï&?´êi´/a\x0017\x001eø·MjrÍT{\x0000»¬±ËÉu·D¥5²/R	¦`oK\x0018õc×¦Â®Í$vÎÝt<cñiü \x000b³pÙM½ìfvÙ=>L0ôÌvË\x000e\x0005ûÂe\x0007¨°ïõ¯\x000ea/Â*º´O Ö\x0002arÝVU²Zw%'×\x001dµÁwØÙÝ)µDìë2\x0001U\x0019µ ÌXÚª¢c\x0016ÃØuS£}\x0000;Tá]Álx·Ø\x001cØ\x0015NCq¤ò£õA®Ä\x000e5öI·ÆQµBò Ê\x0007<Cï B\x001f9Uë{H>Y÷÷ãéÒºX\x0000Ô\x0013h]\x0013mTÊh6àø\x0017ONh?úö«\x0017ñ
rÿ±÷æ!´,ÓÍÚr' 7\x0002ºxêys{ýêÝ·W/â%äæeÃÝ\x0011«ìióò!\x000bç\x001e\x0014d@Ùxb."í\x0011\x000bTeZð
X²)~\x0003\x001aÁIñìo\x0017}ö\x0005\x001b«1ZpBj|È\x0002gÍÚ"m\x0014·\x0006]a\x0003\x0012M-5aw+Qõ­ä°	¥)ËêÀÍeñòZü¨ëícÀ\x0004_}\x0005¿à+ ñJ($\x0012)XUù
]³I\x0003&ì\x000ehÂöç1\x0013$Sü£#\x00011Èù\x0010#-ÞÍ¡¨a>¢J\x0011hîÈzYT¾%Ýp]Ð]Ú\x001eý\x0016ìÄ$Óp"&yì+\x0004äÏ_Á^\x0013!Y`é \x0016T) 6aÞ¤ðLEhÀ?*ÔEà;`ªfµÀ´¡Z­±8¡ÇÂ*Ìt½Øú;¨\x0005ß\x0001å\x001dm\x0007ÁÓ8{]ãvXü\x0019L½\x001bÌünFÓ½&\x0010¸S,^\x0008øx6]"*]6è¤u»{Ü\x000b¶{ÛÿÓÃÇÏï¯ßüúðá×îIH\x001dÏ3J²]D¬²\x0001ñd£o ÚÜ"º}ùú.þ³oo¿8?/àËm.\x001aáËÝ\ôAü1Ã\x0013ùã\x0000ë-\x000f\x000bäñ\x001aÅo5õ\x001eáu\x0019k-ë%K×|÷\x001e¿{)Fø»â£ð¦´7\x00129Q3ü@'ôM\x0012´!üHMÂ¿\x0013©9\x001fKY´ü6Q &üØdñÃRüjw\x001eGüjw\x001e\x001fÇÏî\x0013×Hèbráyý¡Qá÷5~?\x001fp|&áwÉ§-Ó*Ñ¬\x000eÁ5|9
?Æü¬:ÝwÜÌi\x0003ÂJ6[$ðë\x001a¿Æ\x001fDîéBÆ,<Óë¢$.6¥l?CèëØ¯æc¿\x0007~»ð~s\x001en
Þ\x0013®¾
¿Iü\x0007TÌcì\x0017yÌ\x0019f[Rmö¸^üp2.ªa?.á¿¸ÿúþËn¾\x0001
Ò¬ë%){\x0003\x000fÌägESz5£qóöîÍ\x0016ø]gP\x0004\x000f§s\x0014|¼\x0003\x0003ËÅ\x0019âT\x00040|4¡YÛ\x001a\x0000/w½¥\x0011¼T§YÛ(úí\x000eK/\x0008=r´ÑÒ7§¿\x0007ÐÇ ¶G?çÐ#FR¸\x000c©@Ðk.iYÝ|[ïCïõÉ´w<éwS;~¸ÿxuóþ§ûÏ?÷Bw2¥h\x0011ºC©QB.\x0017\x00144'\þ|{óòêæîéÍëï/ãÚíqãÏ	àÖ\x0018XuHÇ
ÁK¢¦\x0001å3ÄÝÈÕÆäÈÕÉé\x0000ò\x0018&Z+.¹¥A/°\x001eyA¦¦C?òP#\x000fsÈM"kMÈAdIJ0$)¡-¬Ñ[oôó[ïèç\x000fáf¥;±´eà¼\7+<ýÀC
<Ì\x0001$\x0017ÿ\x000fCÁÍÇiL\x0017ÃNÝÀ«<Å¸)OQ.Ð«´W\x001aî~FåùÜ4§\x001dú\x0007¨\x0007\x0003®¨zà°\x001dZv4³F\x0003*Ê¬BnwÕ\x001b\x000cä»êÍ\x0001äI4\x001a\x0008y	+Ê\x0011sovUÈ7ú´|GvdÍÈiñr&°\x0012ðàxÉUsza\x0000¸­Û©%\x000fº°ãµÔQï²\x0002\x0012¶À×\x0005Dg*àÎÌ\x0001×xÝâNó\âz1æû7p/«¸âåT\\x0011\x00004ëPwòDéH®\x0012Lî¨\x001b9\x000ehì§y	ä
¨4ì°Äã\x00084¢\x000364\x0005]G\x000eýêé\x000eþÝÓÿ\x0011Aª<q(\x0003\x0014\x0017ªëEçiJ\x000f\x0019ð5õ\x0013W\x0006à_ÍÄGEj¨ÉÃ\x001fñFªKª»â\x000bL"·e\x0001A<©s\x000fW?ÿ×üçÍÈ¥wB¬ ­\x000c
8ß/´î/o¯¾¿º¹Ðð±ïz\x0002;O74M \x0008TÏFðt1Õ¶kÝ;Áo:liáÝ,ø\x0018dr¿½\x000eDæ[\x0006H®fëÐ¤a\x0019\x0001\x001f*ða\x0016¼d\x0005i\x001dpTÜ\x0006äÎi×ã\x0018\x0000\x000fÛÀ´Û8Ç\x001d
(åC}`5U\x0004QëÀï_¨^¡wÁsTÈÝ"ié\x001dkC\x001aÙu;íD/+§ÇèÇ®uÀì=Jo*¼nö6\x000e ß\x0010ý®ttí\x001d©Ùê`\x0005IY¢¨æ=Û\x0014\x001e@¯ëµ×Ó\x0011\x0007yv©\x0012¦\x001c\x0011Ú\x0000¾ªÑÚ7Å\x0006ÀïJ\x0004T\x001es\x001cKã-RfÇÑ\x000c¾Ý\x00195ÞÖKo§ÝÞ\x0003wQ\x0008ÉÊîà
èbÇÝ:ô»û6¢?¹o\x001fAOzqÏrmÆ\x001bÖmY»e]¨±ÏTÎ\x00159íèë$ôÛÑ°¹h\x001dz_\x0007{?\x001bì½å'?#P>*\x0003|Tæ»Á\x0000z¨×\x001e¦×ÞKîÇ\x0014ØF¤híP'®}ú¯\x001fý¾òÉ¥>h­fb#Êuôf#¡¼ÙtÝ«:Ñ«jÏ*5½gQ¨ü^[j6\x00002¤µ÷n!z]]Jöo­G×^ÐÂ³ Q\xíyáÖ\x0003Ðë`©æ¥åÅ\x0006\x0014RN$ôØ+Ñ·¥îFÐ»\x001aýôA¥5\x001fTR(®\x000b»r¥²za£ ^{^ûèéÔè)?sÌ\x0011Ñ7\x001féûÑëúZ¢çï%\x0006xD\x000f¸\x0001\x001f@ñ\x0000°
MæÄ¡«xUÈÉ×ñ:ÎK­£ÙNÀn	\x001a\x0017Ü¾®Í;­µ¾\x001f±\x001fxþûo>^}÷ûo\x0011à/ýÃãZ%F4JU¹ÅÀâ\x0004 O\x0003·´ç·¯^^}w\x001bÿÉ³óÃã\x0004ë0@ø»\x000eð\x0015R
Ò\x0000
Xî\x00105Û¨a³3Þé=z§§Ñ#ÿ.6\x0010xÖn¶¡\x001f\x000f¢ò\x001c)¦]GÑ¬¡sn/fY3\x001b\sÖp\x0008¼®ÁÏ/½Ö<çKïYá£\x0006¦\x0018Æ\x0010~_ã÷Óø%NnÄ\x001fJk´'îrt\x000bñ+WáWn\x0016¿D²\x001cv¦êqü÷ºLÄ7èFào
\x0007	þ®áà0ü@Ï\x000f1î\x0000O¾iëx*ÞBëÐ\x001dÂ\x000f5þé¸)£ÏS[¨UþZç°¯æ¸\x0019Vn_U»¿wnÐä?HÄáOF}âÍháú+Y¹¿óîoY\x000cB[\x000f_\x000b®%¥áG©*|*5\x001d>±"·\x000b¡Ï\x0013ÿ"1~Õlt\x001a;»ö\x001b_»Ìíð\x0011f8ât\x0006
\x0007ÄSùgtsÐgÌNÍ@W7ãÿ?oÊsÄ»Ý`nûÏ?_Ý|þxÿ­÷)\x0011	9òõE*ÖwÑ<<ï¬\x0012=tó\x001a³ç7ïÎ>%\x0012x\x0007{ð\x000efÁ+K¬FêÀù³qåîh/\x0013Cð·7-¿{Ó:
_KªîGü\x000e5Ñ\x0013~
|s×Mµ!üÁïñ\x0007?ßIn2Æc3CÂï\x001d\x0017¬pàm\x001dþ\x001dÉKò}%§
ÀN\:ÁmL<õ&Xþ\x0000¶kïv\x001b`*ÿßó\x001d5 ¦Bü\x0005l\x0011¤°ªT®lSJ{È\x0000«*\x0003¬5@+ÁSÒIÖÍµVp\x0001¥­q2f­
°ó_À\x0013£h4@0\x0007å)É¿U\x0018Â\x001ft?èé\x000f\x0010aRÙ\x0016;ÖhÊ$\x001eÈìAÞ,õ M\x001c;\x001b`æ
'¿XHÔøv<¤Ä
ëM©Nü.o\x001fÀ!9ø\x000eîêÃýÕó÷E6Ä¯ï?õ©z\x001f£ûY\x0010{>°$\x000b\x0000ï¤ßG+n®ßÅ$âæíÝ«³cªÙ\x0008#ÅÞ\x0008ü9mDL$ÊØ¶´L÷UÚzB\x000f%ß
Ûcu²A»\x00056\x0008\x001e·5V{\x001a·`Ø\x0006µÚÝy6ì§Û`
%)Ó'8[(\x0000Úü_CFÚÂ\x0012gÚÔÔ¤fÔ`yx)ø6sö
VTÎdÅ
gW{K\x001aêÊ\x0012í`ð\\\x000f¡Y¤\x0018´AVÉÊ\x0005	¤¹V¤\x0000-=\x0013Ò¸\x0014B[ÈrÌ]FT<~?B\x001aùd)\x001fÅ
l>Ç`j\x0013Ì\x0002\x00132|6ÁPÅ(:\x0013°Jºì h\x001b2bè¡\x0011{9¥ãFÐnð¾H¢\x0002\x0010£tm²­1\x000b|m_a#?ãP>\x0003Xö%»ø ¶u¶a×d\x001bu\x001eR:æ\x000fá½£6ØÚ\x0006»".YVFô
âf1+Ñî5\x00183ÂÕÁÕ-	®\x0006èùÌø\x0018\x000cÉ;
V;\x0016m¡1\x001bTõ!Zð!°Ã/²ã\x0008|@l»\x001aV\x0007W\x000fÎ­8\x001f¬á;tÜ\x001cL¸MóÐm²Ñ\x001dQ"iWTt}ª\x0010\x000fÅÅ'íS\x0008ÁÑÚ\x001cÝ\x0018§¶àæXc\x000bóD¾BZ\,ó&p z)¼gp»'»sûù§oï¿\½¾ÿçÃ×^ð\x001a\x0007îriÏXÏ]FI¾Ó9h^«_½»{sõ:þzÛ\x0000®Å\x001eøNûû\x0000püsD\x0008\x0018£"\x000e^
·Úf?N?ð]A\x0015\x000b\x000fajÅ¥(7S\x000eg­\x000cçª¦IßÖ\x000f\x001cä\x001eø®è\x0008pd×Êçqg\x00065·°ov\vã»\x000e[î[X¬xi<Ã\x0015'\x001d0­¸ü»rÅwíÝ	ù®½û ¯äi\x0012\x0013c\x000b÷vkÅUGvëJ?òP#òrµ1E"rÏc\x0005¸_ç,ÖUÀw=éG{Ëâ¶\x0006ÿm\x0006î¹3·ýbß
Û×°ý\x001cl¥Y¤\x0004{\x0004áæä ^\x0003ÚOLýÈkOJ1\x001bF\x000c+åÇ\x0014«	GWi\x0017v{ïH%ÒÑ©§\x0002¢×\x0012.j.Ê°1\x001buÀ]å,ûvÖ#g§\x0013|-±Ò\x0017äØ\x0003Jë6§\x000fuÞýeÿ}`á­fÙfÜ£Î\x0018TáÝ&cS\x000f~oþµÒqª\x0007óâþ>¼¿ïæòöH[R\x0000Iï¸\x000fTòlc[\x001béöÍÕg/_=¿»9ËåMØw·r|qÓØ£×\x0008ODYPÔõt!ú2m\x0016é~ðû'¼\x0008¾\x0012Ê>\x001eO¡ÜÌä°Zh	½+\x0014Í'Ô\x0011ô®r\x001béfý\x0006\x0019f3x\x000c\x0004^Y\x0016p\x0012m%Ó~ðj\x0017ß#xµï\x0007Á\x001bâÍì:OâÒkFß&Ê\x001d\x0000¿k\x001e@ðÁÏ{½%nÁxiµ4h¤øÝQÉ6_t?z-d\x0015nD\x001f\x000c¬ø<µÑ\x0003o^FÀ«\x001a¼\x0006oXÝÆ{A´\x0011<\x000f*­\x0017nY}\x0012é§C½	Ø)i\x0011SìÉcìÜ4\x00137oS/zSÅzmf½1ôZ­!^A æ\x0008Ì*èÛ|û#è]ÞÍz\x000e³
¢z\x0003\x0011*GÏ)GU\x0010w\x0004ýn`!å\x00080»öÀlÊ\x0010Óúâ9ç]ÝJCàC
~6Ø[Éì
H0HÊµÀ}&ªÝè3\x0002~4JàAÌ®¼CÊ¼òdpÏJ^y¿2â@\x001d/a6^jÀ'·^3\x000b4 h\x0003ÏIµÛ\x000eÚ*³§ÃöDìæÿ\x0004Ö§òÙdñ¼e6Ù.\x0015¼\x000e\x001bTÊîwÎ¯èïÐ?ÿþÛO¿ÿpõçoïû¹Ü-\x000e¨¥ãÿ# t(õÌ«¶¬Ù»\x0008ÿõíÓ?Ý<¿úó»»óÕàlÂ®7\x0003)ka	©oâç.TP®ØÐ!T2`\x0014bo\x0003þ7"B¥ÌÇ\x0018OIò\x0006$ë¡åR#6%ðdD­\x0004~Ð\x0008\x001d¨ãJk|Óå	\x0006Ò[±Ð!}Úk\x0004¤éG¹m\x0018Le8y¶zÑÝorØtI\x001fÀñ\x0019\x001cïëìE²­ÍÞE.¨Í\x0012è]µ\x0018D¥4\x000c\x001a\x001c½KÅ\x001cDñ;!¾ëðÈÑ"ÈFì!Ó^¤¡u\x0016Ü×ovÞði\x000ewÖ\x0015èÓ·å!Ð*cbz1(Q\x001dª>Ì»XÀ7¿\x0019Ì:\x0007µÙ¨J/¸½\x001dk\x001d ¡\x0002}Ún7è\x001d@Ê¬Âã3H\x0006]fèTGÑ¦\x000f4T+
+MC:$mZiy\x001dåNÐ¦\x0002}Ú\x00035\x0004Z²KÇôÉúbèà\x0003'4;¬»AÛ
ôiÄ\x0010hG\x00046:F>*m@TtÜòº0ï[ñ`\x0011§mN ñH{Mã(\x00115=ýâÑÞ×*×º>\x000eÅÄyOT\x000fPÑ\x0000*º[ÅJ ;EÛ¨eu¸È?´M\x000fzu\x001e\x001b	HØ\x001d\x001aÜ¢­¸·J¨ÿÐö3Úó%4/L\x0012=Q»¶(T'j]å\x001e)0ÍÄjF\x001doAô8`<©¢Yð- \x001d¨¡F=uÂ\x000b¿Ö{>#jI¨­\å×¦:aj\x0015çaÔå®¬µÚ"\x001f\x0014ÔjQ\x0006"wOwÚöl¦M\x0014ùf\x0011aã©®ezz\x0011j_ïÆ?tCD>ÁKIú¨
ãZ³ô±jrXt£®×ÚO®5é\x0006Çâã^êb¸^°Ô§Äµ¶"®Mõ÷¿~úÒ]=Á
ç5ñ¾¢n\x0000Í	
æ\x0002Ä¾êÉÝWo.ÔN2ì]¿HÀy)Ü\x0011^ îN\x000c}4¡iXÍ\x0003%l\x0001ß\x0014\x0010¸\x0015SÀ­º¶PK\x001aíµüÂÈ6V\x0001ßÝeÂÉ]f\x001c8î\x0017²T\x001eéuÜu¢ZËpïveM\x0010|\x0004wÌøí\x0012Ç\x0018
òòÈMt®ú`\x001fîzcÎíÌ[ñ\x0007\x001a,@à»-Ý;¨=î ¦p\x0007¦L¸%ÍJjÕ=CÀ÷\x000c>\x0012XO!\x0007O].:xÅzË15,1¥I?Ñ\U.¾ç¾9\x001c\x0005Sº:bk\x000bV³2\x0013êj.\x0003\x001ejàSa\KK3\x001b:¤¶î\x0008¼0w/óq¹{­M\x001cÀv\x000e·ç»Y\x0000uÍ°Í»«C¡\x000b¸©}üô¡v\x0010¸v43\x0018hY¼®(ÇÆ£ÝîÜ¤S2r3\x001c%WÉÇ53eññ&©ß\x0000òÚÉçr\x0015¼):ò7½Ãx;cñ¶``?r[Ç\x0015;\x0017W\x0002×ÜS\x0007W\s(,ÝMY~ä®Ê²ðç\x0014rËuùr$\x0014\x0011A1M´h\x0012Àô#÷õ\x000e=í\x001bD\x001eÛ1§¾cmUWÈ+Mú¦«×;ÔÏíP/\x000b§{ÐüÊo¼æ}M\x0014=È¨¼E9o	ºåB\x0008¤´\x0013Üë²As¥ª%WjjÉT<óÎ\x00029(";+;Kûõ¸\x00039èÓG\x0006½dxñéËOøúõ}ïU\x0019	¡s;®ÂG¢%VL.Ém\x0003uÄûôO·oßÞ50ï+ßz_ù>Ùæi\x0016¼|Rg\x001c»\x0008^ÜVAv\x0015d7\x0001Ù9b\x00025J\x000b\x001eó»@«@ïØO"è\x001dùÉ8hïI=*®³¥>oYÚÛ5o\x000f¥ª K59\x001e1¤¢âaÏ\x000eÍfÎy×Ù½¨w\x0003	z70\x001a\x0013À\x000c\x001aDáóÿ@¦Äe7èz©õÌR\x0007K\x0014«	õ\x001fôr\x0016¢6U¼ÛZ
£ö5ÂQ\bÀ\x000fA7_{A»z©ÝÄR£Ô2Á)<Ï©\x0017gÉ|S$½\x001bs¨1vL(¡¥êC\h\x001e:ôrÙN\x001a5Ì V\¦7ZûkËí§Ü<ëMó\x0018ïE½+õ ê]­ç\x0010jò\x000f-]ïP\ÊôªI÷ÚzíEÔûlo\x001cµ_#EX- ¼yqï¬ªc\©sÜBF ­$:H\x0000cØ©móMµ\x0017µ®ò%¥'\x0012&ì©¦ì#¦y|¾<t%³½¨M½Öfj­\x001d1oj¯øxPG«Zï
½ }íÓ~Æ§Màù6¼Ê\x0004RÀ³PÇf[C\x0015?Rgùq\x0007ÑÔf°ãgM\x001c\x000f¶ð«Ü:Ôn\x001d¦ÜÚàQPÇ¤TIÀq5\x0007Ts8¼\x0013µ®£zNÈ\x0002Ù®âN\ä\x001eZV;QËè Lë¤Ô)XÃ\x0014tò£??­:Ó)GÝu¦\x001f¸\x0011(f
Tn»-:~Kpí÷Éþ³ñ\x0014<3à}ôkâøÐz?¸)9\x001dv\x0017'lÍL\x0012ÿâÉi-äÓ·ú¡{\x0012@C@¬¹\x0017\x0017\x000fM[nà\x000eÐÁrø&B\x0017ß-0òP!\x000fsÈ1½¦\g©÷<B÷¬{á1e\x0000º{èVNB·\x0004ÆlJ\x0017\x000fë¹#Ðtt©uC÷\x0015t?\x000bÝ±JdwÐõJñÃÈ\x000eC÷<¬KÅ\x0012´eWïi
ìF\x001e*äa\x00169\x0010]ÆTEó.\x0005vu¹pÑ¥°{èøsvÕ%a÷æw)\x000f(@_¸\x000f¹T\x0015r©¦w)5\x0013hgXZ[U:`×â\x0001ìZWØµö\x0018zkÅ4vu[ærD%\x0003Ð·1\x0004Ýé¸N²Ú\x001akù Õ&pOX\x001ef\x0004»¯±ûIì\x0001\x0015h¸%Kµu²`_\x0007ÝÕÐÝ\x001ct#ø¾¬µTø\x000eH.ÃÝ¼mù\x0001ì¾1~.Æ v"ü@ì%²[_°¯2JTç©:e\x000f\x0018Æ®x\x001a\x0016{i¨\x00052º\x000cc}­?Øu}.Ê\x0018Á\x0019Ê{ìÐ£\¾n«>äºò\x0018uÚ2ºQ]¸6´ê¾ôøji
öf\x0019n\x0000{½SÕäNÅv\x0014\x001aºT^Pÿ)l#\x000e¢yÓ\x0018^'j2{D­1OË\x001eoxDx Æ\x0011±¯\x000b2ª\x000e2j2Èh]ºgã2°Ë(æðFY·Qu]ObWZq\x0001Ê´de\x0010Æp>JB\x000b°<)ZÞâ_<Q5QÃ«\x000fïÿùþás7ô\x0010$Õ\x0016\x001dûæÇzÌ¥EËwu0½z~÷»Û×-ä» \x0013Äqä]	ºâüäe\x0004\x001d:Û»¡o\x001do\x0008ý¤ám\x0010z¼ôB¹\x001f]'dQ=%-\x0013Ý¡"ï2è[Q\x0017¡{1\x0007\x001dë¼ê.¨A©B\x0018×GAÕ\x000b½r\x0018?å0\x0011:PÓÛ¯âÖ\x0005â¸í\x0013ìF\x001eä\x001eysÈíÆG{¯¡:züÏwÅÅ^Øª­æ`;AÇQZqòr'wuêõ"w\x0015r7¹àr\x0000ßÔvÍTe¾G_¥\x0017¸\x0014f\x000f\x001cÎ­9ð\x0003\x0013\x001eë½yÑ¹í:ôq\x001eubUTr2,@Qª\x001d{%)¶csdnZÝÕØ'=Æëâ1V\x0014¾\x0011äÆ'éºßub¯S\x00009\x0003 7·
9äZ#]nDÅ{u'ö®&a×a\x0012{$HØ3E_ÆÎÌþ¢j§\x000f:ø*:âÏ©\x0004\x0006,õ:aþBTøÒYftîãiê\x001eª(\x0003a2ÊÄ)Ç8~\x000eñ\x0014¯z×äUwÜ¿&q<!i\x001a\x000f6®¨1óµXtÏ\x0004A¹×½_r®jSSÒÄ¿¨(i¾]IyõòÓ?\x001f~ýëçn×\x0011¬Jk\x00056÷e¯Á¤õ×ÐÃÐÿ\x001f¿úËíï^ß6àë
¾\x001f¯\x001aÕbÜ\x0004Od¾gVe\x0004þ&Dðw:GW\x001fè²qc]\x001bIð)\x0007öF¶¯{#ð·^~¿oå?\x0004?n~zJµ\x0012¹Ùóæ\x0015@cÞèvõz\x0004>TÎ\x0003³Î\x0003ÈÉ¤2|ÅÕÈ\x0008Ç¶¨Î\x0000ü]wkÚº»îÖÞ¢\x000fù%; *s>m¥¥Æ:¯\?y\x0004ÿ6)ð[1»þ>\¼þJÐv\x0010\x0005«ÚSÎ#ð}½ü~vù\x0001$F¤§´ãM.D\x000bñC\x001f¦Ý'Þbó\x001bÁ\x0004ÂQÚÀ\x0010^7ûçGà«Ý_¯öo~GàÌkf~BíÙù}hc\x0008~¨áO\J\x0010üxð\x001aªRÆã¦,=nïøU½üjrù£÷x¬eï%q£®Íèür¥ó«:vªùØ)\x001dÒ\x0013¤åwe¼¤\x0000à¼Ç®<º©N^efÞ¸Ò|ôÂú\x0014ñ{vÐnª\x0019ÁïªÄG¹éÌGJb­J\x000fPð\x0011T¸ÄÌ§yC\x001fÁï«³kßz<s£õ×Ör·$\x0016\x0017ï¬Z\x001fêõùÌSÓ+rÜ©Ø\x0014Î®à,gnMù¢\x0011øz#uIiÿïì`êF\x0015X+c\x001c¢ú\x0008\x001cüM\x0012\\x0007_Õ·\x00165y\x001ab2µÒ27qt)>Æ/={uúè\x0005©\x000f Æ$ÇosIÝÚ´##ð¡
øs\x0016¾¥\x001b»Ás\x0001_ø\x0000\x000c¿]b\x001bÀotµyÝ¼ààòfd¡#ïq\x0013Oß~\x0013ïo3\x000bîæ=\x0016ëuÁçóýÇ_\x0006ª%¸à¤Û\x0018SZj£©(+ÕÅÕéá6zõúæå³KÕ\x000c}Ó\x001fCèÆNAW»ûPá:#7ª0\x001dæì\x0008r_!÷sÈ
Ñ\x0004!\x0003FaÛ1<Gmº\x0008=:ïnö\x000f|RãÀ¤¸Ð\x0019=Ê¯Á)¡eÈ7j:DîÜ\x001crÏ/ù\x0006\x000b)Æ\x0018&0¦ý¥\x0013ù6·ÈAÍ!Á\x001eÛ\x0004Îfer	ÁóÆÈu\Ï!w:Íãë@oé°L\x000fùb7ô]çp~Ò9<î.ã¢3Ggt\x0017Ê'#ôa\x0011»÷\x0011]Ì9\x0016\x001fq¬øjÕ\x000eúºMºãEMÐÕdHGó\x000c=hzW¶e\x0002±.²\x000e¹®\x0017]O.ºfe#pÔ,\x0010×ãUwÍ	æ\x0001ì¦òõSÊ aìjÛ§6\x0005»\x001c>\x001e®Ãn«TÚ¹£T£f*mT|&$q<hÖ\x0005Géjq\x001e\x00137§Vå,%ê:¯9ñê\x0013¬ëîkè§\x000f£Ð±õ3\x0014	L¾\x0003|&õ0\x0018wc\x000f5öÓÞaì_8±¥\x0012^'<¯»oW:\x0006°ë\x001aûÜã\x0014\x0018xi(²\x0002S;Î§Í.ìû\x0016Öý´õ\x0008vêv\x0012^ÐØpÄÎcI\x0013bá±T½,ÓÑtú²<|°*l½Í'k¡SÅz+¬í\x0017\x001e\x0013òa[þDù°-ÿ÷ß>\=ýý·ÿsÿñcï%ÕaW¥ ¹~\x00104öç±çr]ç?Þ¼{~õôö_n^¾<G¥!y±\x0007¯v£-GÀ{,É2¼9	|(~\x000f¦Yà\x0018À¾±Ú%ì;V»cØ=Pi;ÞH\x0015S\x000b÷Ëà]\x001dn\x0000|¨¼F9¯ñÂ)ö\x001aæ&åf!!	lóM³\x001f<RZîÀãÏ)ð\x0012Uf·Ùºæ\x001d¾-¯\x0000\x001fý.\x0013y\x0008ÿøþáóç«¯¨³ôþáêé·øg¯
Î:zu"\x0014Z-°Ä[\x0010s·æQûãÝíë×·W·oQkéîöêé»øgÃ\x0018«÷ÆX½È|\x001fAc¤Ü¦ìM1Æ4\x0003è\x0011c6Ê\x001f4fÇø3i$6\x0017/\x000fE{UÓí6\x001exÍ¢ñ\x0011cÀï\x0001¿È\x0018,ÛÓ1ê\x001ax
ßòñÍ÷Ã#ÆêËU_\x0006Õ\x0011]6ÆÙ¢¦L£\x000fHÀØº\x001d°eÇU¶ì¹'q\x0014Ä\x0004{íYâ×äs\x001bL{ù5º¶F¯²FZ\x0012PtI ÕC%[£¿\x0007¬Q'±yUp¶\x00108)oY\x000bÕ\x0003i\x0000	ME#Öì*\x0017hÍ®r1gÕD6ã°æH\x001aQÞ\x0010:Øf\x0005ã1;Mi4f¯)=g\x000c*\x0008¤1ÞE\x0005\x000b\x001a¡dk¶Ë\x001f±ÆV¦í*G3ñèOÆÄ\x000b7\x00074¯Iø\x000fâiú\x0008I±ÕQcì¢³ÆJ¢t&3\x0005$c¸±\x001b:ø	\x0018\x0003\x0019XågBSß³Ò\x0011S8ÚïàeSÖö5vc^LùÙyqÊ\x001a\x0013\x000eù°q¨­¿
ÒgkÐçÖ[ãdõm\ôm2+\x0013\x0016;ïld\x0014lj2\x001d±ÆÔé¦Ytt"YO®0»Dø#³Ä
\fðm`7ùæn"eÊ\x001a\x001dMÈâ\x000ed\x0011`µ	Ð$«8bLýi`Õ§ÑÎáe&\x0019cJ\x001e\x0010ïh¹\x001e\x001aDFý5õ%
VÝÒÐ\x001aIÖ \x0003¤ak,YÓVå<dMýmì²ocñ=[\x0003ôd\x001d­1ümT[ä5uU\x0001\x001a+ï!\x001f7qës¶ÈÉ­Ñ\x0011 Á×ßÆ/û6Z\x001döÐxö4S¬irx[#Oê\x0001é÷\x001asÐ¿«áð.óyÆÏ Û
ÍGÌñ¶6Ç/J:U¼næÔÆà¨§\x0012#=¿ L³'÷9{ÒtvÒN\x0015ÌµO'WÖ\x0015ÙM&óÆ§f5pÜ\x001cmN.Ò«Î\x001cu<ò
\x0003ëÿ\x0011sl0®ÉfzÄ k[Â¢DMyæòyg\x0002KCoçØ\x0012¾>\x0019¦¾«¥ßk¬Á¨j\x001cÞÂ3S¢µMe#Ö\x00045³*¨¡\x0014_~/Ö¸¢É<Ká\x00112\x001byrYËnk(c:­±ÝX>p¬oòè\x001c0Ç\x0014ÓìªjéYfJñVY¦\x00076¬Û\x0017\{fè9NÕ_\x0007¯1'^Òò
Ç#Å\x0001C}´\x0001\x001f£\x001eÁ\x001aS7Î¬:oTÀjm²F[\x001a&Å\x0002'ó8\x001fçäøtËOå)ö.º¤ãS\x0011Cxã@×ÖÀ¢;R\ëô\x000e;CÉ\x0018Êl¢ë\x000b\x0003Ò\x0013cÂ2c\x000c
ûxÇÁ9lesÚ¾\x0007Ìñuå6ý^dà¼\x0013\x0005X$o\x001cÁ\x0006Ív´#æÈúëx¹êëH i\x0002ïA¹¡d¤f©àY_!¾~òH¿}Ì\x0013åã\x0012ìF4"\x0012_?B\x001ame^\x0015ÖP\x0014Ì1Áò×á°\x0006íÿ#æ½cVí\x001d¬¥ek°â©Ø×\x001cY£\x001eá\x0019Wzsâkf¯IÉÖÄÔ\x001cÉ	\x00016®>5'®¶,!\x001aEn\x001fCU=Íæ<ÂÛ§ôöÄUÏ8J°Òh<_$u
Gs$ï\x001có\x0018é¯KQé÷2sro%ªaY¾\x000eÝstG9Ioü²ôFLÚgVd`[|oë5'õh¹¬ -Qå;oøAP§#[CÄ !Hx\x0000¬91gQ
\x0017çó5ã4³Ò\x001bÁ·¶ ýc|;5¬ºSKP|§\x0006\x0010üÊ¦rB°«
R»ÝÖ¥\x0019àÉNñysÿí÷ïùÔiÀÚf)Kì1õüNàDè½®½¹y÷»g¯\x001a\x0006xØ\x001bàÿð®6j@À+Mf¶ ©¾écH¡nG)zK5}\x0006ìù
£\x0001{~Ã£\x0016DùÆ¬-v\x0006¤¨å¸¯ú\x001c:ñKQáb\x001a¼\x0017kr¡\x0010¨é³/'ÛÒGc\x0016¨Êä\x001fßf-("®ÚåJ\x001f]R{»TÍÁ±1øû>ÂÿcJ?\x0008ßÛxìåne\x001d´àU¬]§Ûª\x0019\x0016Ú?ä"£\x0016\x0008T\x0013È[À)E>\x0018WiJBê¦vÆ\x0005»Á ´Àÿ¡lØx\x00031,0Ä#ì ¦hAïéÖg\x0001\x0012\x0014ï\x000f\x00029íE\x0002\x001cq¡ÄÅæ\x0003Í\x0007Bní\x0017Øit'üj6z\x00113>Ò0ÁîqÇø\x001d!×ÛÔi®|è¿éG\x001cµ@£\x001a[>Ê¼\x0017E,ÉÐS¶·ÆÐi­}èW¤Q\x000b¤T8\x0003}(\x0010\x00118ÄÍûØ÷\x0016}z-ÚÙ£ ZÀ|^\x001a@ó@k´©Ì¥ók¿«cü9k\x0001*Ë±\x0005ûY1\x0010ùÞÎéN\x000b ¶\x0000æ-·,O¼(s\x000fCÝ#\x000bì\x0016Ô;\x0019¦w²túU´óÅ\x001f\x0004lß`q4
Õ¬þ8R0þ
x\x0000'Z\x0010XVI8\x001eFkVZ°SµD\x000böª\x0007-PE\x000f\cS§"\x0011\x000bÍÒ§miÜ1\x0003öÏÑ?¾\x000e\x000eè9\x000c\x0000à¡\x0001)T1 =º8d\x0001Ô\x0016üñ¦<ü	tbJ\x0007ðÄ\x0013dê.wZ\x0010j'
óN\x0014äÜ¯©Qª]g\x000bb¶\x0015Ø¥\x0006\x0018QÈFLÈøôO_@z®ó+±áoj\x0016\x0019°#JÝÓ(\x000f\x001b\x0000¦5ÊS©¢ö¥x[X{=6\x001aj\x0003¦3
EIE\x00068îöSE¹»\x001b»Ó\x001d»2\x001aàÿP\x001c6@I¾y$\x0019ÌøÁ±\x000bÞÞËN\x0003ê0ôß4Á\x001bPn\x0006>ætÔ`¡Z\x0012¢\x0005~iVjBO03@\x0002*º\x0018X®kk¥Ù\x0000Û¤Î\x001a2Àê\x0013Ø?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÀóÓæ2{à¬«\x000b ?,.ÀÓ÷wo+Wks©ÿèW?Ôÿùáîí[yÒÖ´RàþF5ÜØ¼Ì¶5w¾ºyQ¼Úhu\x0019\x0000\x0001@°\x0004\x0000 £\x001e/I]X*\x0008°)äÛ\x0001øùî»\x000f\x001fßo\x0003H\x0003d\x0007¨déÌ÷\2ÔJ°¡xiL\x0008\x00107u+fv \x000c\x0000á\x000e8\x001eDZÚ\x000eTkÕ8\x0011¹ÁMv\x00006\x0007ZOìÀ2i\x0005Àóì\x0000x\x0011^\x000c\x0015\x001eÚòQtCxùøþG?|2üþ¥S+~çñ¬Àë¯Fª9!ÄMÿjbýËÀuý<pæ\x000b»\x0000~8?Þôü8Õ\x0012çq¯ÒÕ]-¨^6é`f\x0007\x0013ä-O\x00107á4ÀE±¹×>µà7\x0007*N¬Q\x000e_×ÏÊáfë\x000fÚ\x0005®\x000cà¯s»Á £â\x0002·n\x001a¬ `I\x0001\x0001]«}õõ\x0004q°´¬ß{Ä"
88\x000eß?Z~ÿIü;ì,:£È"ûj6\x001f¡'6`U[\x0001°¬Ý\x0005 &\x0014jZZáÕ6\x000c~ûÅsbýðÕº~.\x0004þÂLhKÐßá;ËK\x0012ÁÕ[\x001cåy ¥lå\x0016ã#ÜÍÐòÚ*ÊkmÕ_î~þ×O÷\x001f®¾½{ÿë§û·w\x001fO\x000b<GIÞh!IÊ°v\x0017â6\x0015ó\x001bí_nüÏ7·¯¯¾½yõôÍíï£Á\x001e
Z£)ÒT\x0017Î2 r¢þÈE»{\x0015>'¡\x001e\x000c\x0019añ²¢q\x0006èf¯\x0012à\x00044¡G\x0013ÑTh
¡ ¼Ö\x0012!iÁßU\x0018=\x0001MêÑ$c4Q'.AÈ"ÃKDkõ\x000fíVÿ\x0000¦ô`1\x0004zÐBRSLä£Ú\x0000Ü-îG\x0003£E³6i)IÂ\x0013\x0002w\x0008°Z\x0001Øm8?\x0001Î`\x0005ÀÚ\x000cä :?\x0010jØ$f\x0014µH\x000bÊnëÚ	p\x00063\x0000Öv /Ze\x000b\x001c¢yYáÈô
Çúê\x000cgt´ÈÉ\x000c\x0014\x0016©>°Ú6ÖS\x0013\x0017võNáÈ\x001ewkõ\x00168y®dªµÁ\x0006ÒO®Ò2_/yäô«'ïÞ¿½¿ÿp"\x0008:nªúrQ"EÒÙâvXT\x0012¯¯¼|õâööõq\x0010Ø@C\x0010ÙË8RàV·EQKé ÃÑB	\x0014Ô£ ;\x0014¼ôñ8·(Uä^_¢âÎ\x0004èy\x0010¾\x0007á
·Ë}=vÙñ\x0018å<\x0005­	JÉò@\x001eE0Ü
în;QW-RdX\x0008°î»\x0019ØC\x001báü¸¤å¸\x0008E6_¡ÍP¤\x001eE²CÁ\x001a¤­¢¿þ³ü\x0017±^´=Gn\x001eEîQdÃãÚ'GA\x00054|\x0011½zH´Íó(J¢\x0018îEPå>ËÁÕ¢\x0006
]+±\x001aá9ÃÍ\x0008Az¡])EU~¼¾+'·­É2b¤mCÞöäõ\x00056\x0007í!&Ô\x0019Y5TÙ\x001e­1\x000fc n0dîÀ\x001dl­ü¢T\x0012\x0017ÊSï#£Å\x0017\x0013 \x0006Þ\x0006CâöP®¥<¹DyÜ'ø\x0010XªÛ\x000eÄÀÛ`HÜ<ó8âm½S\x001eÞî\x000c·{ n0dnÏml­ÒÅ3RIý°F\x00071P7\x0018rwpYZWªÑÖ\x0010ÊYïÅñJÑ	\x0018\x0003ë!íq
·×á\x001aÌ
ëÅ
Ô\x000c\x0005\x000e||ÁÊîM¡Þ\x0015\x0004ÞÍrY]hgiq\x000c\x000c-­ç'µ´²7jÀºÂàY°f0\x00063f\x000egjÑèd&JÁ§íi\x001aó®\x0014¬eT\x0012wßÙÝñä¥ä¨þmR\x0002¯ËÏêl'®NðCºú"KJä2fWd,{³»-¥qÊ¶ü<nËÏvÛ\x0012I^|X3Qõ]kX\x001bÕ%Ù9!ðp[ÈtW8#*+Þê®(¥my\x0013Ü«\x001fÿýõïvÇ«\x0012¢Þú W> v²íHZ\x0018y¸%ÞtKêAR\x0011ê-j(\x0018¢F\x001fÆæë§ñüd^*Ûà¨H¿\x0014\x0005\x000b\x0000n4L\x001c>Ü\x0014´Ý\x001a\x0012¶\x0014Po½j\x001f¬ùÃtæ_äÍ;¼Wë\x000fú^Ý´ÎÿöÓýû§Y:  s¹YÌaÎn÷)´é?öõí«ïw4ÛuýØ¯\x001fMÖOù\x001aÚòW½.Y4ÖòNÅê	Ë§~ùdóù5st:ß+SqÕõô\x0018®ß÷ë÷6ëOòÀSZ
ßÚñ!ýþÛå'¬?ôë\x000ffÇ¿MÈ<^O¿.§\x0016}~ù±_~4Y~\x0000y,¯7Èl]Öñ\x001ee÷}yrý©_²ùü$ÓÚ3\¡^_OÒ#\x0006ª=zý¹_¶ùþ^:²3cè´yu/xæÊñ$^é×_¬¾¡=¥Ö¿¿íZÕùå/YÙ\x0003y9õWÙ\x001e*2Ð!Áa\x0008\x0015\x001e1¥ãÑ\x0000Föµ¡ßUÎ±õ¤C§½$kê¡rÇ\x0007'=zý\x0003û
ýF/]cõ¬çkùþZA#Áñùb^ÿ@¿`Ã¿õ\x00027åªzÖýuzå\x0000\x001d\x001fYóèÕ\x000fä\x000b6ì\x001bõm(³\x001bÚ#\%]ýüðÙÒ\x00060°/ØÐo\x0004~kö3é°òºnPû¹ý,4\x000f`à_°!à$Qr¬½%\x001b \x001c9ì$¾ç×?ð/Ø\x0010p=ANNPÒ0Å'H	Ìï
	M\x0002\x0018\x0008\x0018l\x00188/U\x000fÕä\x0007)5w¹81a»ÝëÕ\x000fô\x000b6üËXÛ×N\x0007fV§\x001dh¸ýä0½~\x001cø\x0017mø·8uCuÿø?Eß\x001chWÃ~\x0012ÀÀ¿hÃ¿©ìâ@T_\x0008\x0005@özÊî8£I\x0000cøkCÀ\x0005%çXO{Ñ9eÅ­\x0016hWgnrý\x0003\x0001£
\x0001óúå\x0006«L\x0003/¿è
ÞN6¹þÑK\x0012AzØÔò¹¢j9¸í\x0017y\x0000\x0003\x0005£
\x0005·JÌ\\x001b\x000fYW\x001fõð\x0018&p _4¡_®Þ×¯$\x0003M\QÑµì÷gGM\x0002\x0018ø\x0017Mø7:%\x0000®f1õ,+¬§'\x0019^ßÀÐÀ"\x0016)e­\x001b \x0005î®\x0004©Ï­\x001b°[s<\x001b\x0000÷#\x001f[\x0010<N|<=\x000e\x000e\x001aÆäõA­ÆaNÓpÞÐ\x000c­Ï\x0004]*Î
Æ\x001fCx\x0008\x0003\x001f\x000eà<Ý©Ó6þÌ5¡¤nuRRÞ¦>\x000e\x0002\õ½Æ\x001e°úÃSÿtõÝÝ{~(<MTßs*¢\x0014ëZ,Ú&\x0001\x0019i×­{sõÝÍ«'ÇWýÊÑdåÕÉJ@n\x00152Ô ®|×\x001bzìÂ©_8}A\x000b÷ýÂý\x0017´ðÐ/<|A\x000býÂ£ÅÂ\x0017Ñxy¯\x000b2u¥s×çº]Æ}ìºs¿îlòÁ«\x0010Û4¡ºr©.à¹Êòjzì¥îQ+\x000fõÏÃQá¿¶øè¥è¬³\x001aÈth\x001e)_\x001d·5»µÿ³¦êqí?þõ³ÕÿÕbù9I)×±Ze=5ÛUýùôõ TT\x0018+>ùÛÝ¿Ü×µrÌm\x000ct±.Y\x0006pøÔM ¥ã¢Tüùæ»Ûú·CÁ\x001e
ÚB)Ð|NNtâuk
\x000f\x0000Ë^T»Ã\x0011%\x0014ê¡ù®,¥OuW0HB¿+;\x0007ë$,¾Çâm±ðü ¶-<\x0000¾uï`
\x0000RÛ\x0017ðG«Êç°\x001eK0ÞØ:ø\x0005)¨­]¡^÷mÏXì±D[,e_bÁp­r.M>®²?.9\x0005%õPñ¶PSÁÍÑ{¯3·¼y³\x0015Þ&{\x0012ÜcÉÆÛ\x0012¯Û®d öðWw\x0005å\x0015´Ø|\x000eIé\x0014S$,wïÚeY´ðcB\x0011ÅyÚ~C8\x0005ËAhy¡Ig»-õ\Q\x0003B\x0006rj\x0003íu(Á)ÙWÉ^²\x0013z_ÜÊ¶;3Ð\x000b\x0018ó\x000b+Ëu\x001e\x0018²«\x0003cJ0d0¶É\x0015KRÞ×wE|ÊûGÕ¼§°\x000cv\x000c
\x0019ëµ}á\x0002hjzO>\x0014Ý\x0018Ü~>\x0005\x000c\x000e×\x001f¯hê\x0015\x000bdó+&Y	f;\x001d{\x0012ÑK¶¿üº/\x000e%ÆX@}`êÃàpùÑúòG®A_?z]IRÆN\x0019n?ZßþÖ!^± 
CUi¿¡ÒÎö\à°\x000c·\x001fo¿V@S}³\x001al\x000cy\x0005\x0013·Õ,N\x0001CÃí'ãÛOxÛ)£\x0018ä9\x0006ý2,o\x0001ã«O\x0019î?\x0019ß\x0004\x001ew³¡´qQ\Ì`{ch¸þd|ý]\É*ú§6Ä\x00079J\x0013\x000f3\x001f-²Ã2Ü~²½ý)gî]Üå\x001aþ{ñA±\x0004ã\x000b3Ü~²½ý)ùëv_°\x001e1qüEhÛ8l
\x0019ä^G\¾ÃÊ\x0011\x000f \Ô!õfkúÏy3\x0007µuñgî¬ñ,¢P9au\x0008zÍ¹\x001d·LþhùQ<M\x0003\x000eÓâô\x0007ÎaÞüÛýÛõAðéÝûs!KLR²\x001cxtªÄ4	H\x0015asJÉÍ\x000f·/Ö÷Á§7¯\x001e\x0006{4hÆ;ëÓÔyzµ)â®ÑgE!\x001aêÑÐ\x0005ö&8y\x000e\x0008õmo"×\x00004éÔR¶ò3' ñ=\x001a½©^s«
\x000eXM¤\x0002RÒª\x0010üfyð	hB&ØïMnÏ/Á\x0015Ò<s ©ÓæÛ
lN\x0012{(ñ\x0002Ç,'ézáþ/®^6Æ«B5[=;4©GìÑ¤2¡08"ØÀ\x001et½ÁÍ ó\x00044¹G/aãº7Õ%XÍ3
\x001aþÕ\x000eMéÑ\x000bì
éPO_²æÎ©¨\x00144Í§¦y0KZóÀî\x0002{Cî:·ñ\x001eè¼¨Q`¢H\ÍófÓ	pFGà\x0002\x0000W\x001c·¢-ÏÍK­y\x0005±Ä\x000cÀvóÏ	p\x0006O\x0000ì]\x0001Ê¥H-c¤Ó¤0"(yÆÍf¬\x0013à\x000c®\x0000\À\x0017ð<Õ³)x'X\6Sÿ	ãâæØ²\x0013à\x000c¾\x0000Ø;\x0003´¤Ð¨zõ\x0000$j[Eù©!\x0018\\x0001¸/À\x0002`~¡\x001a\x0008\x0004ñÓ[\x0005Îv6í\x00048;\x0000\x0017ð\x0007|\x001c¬{ã&\x0007]\x0014¡¿àò¦äÑ<\x001c\x001cÌ4^ÀLsSTkÉ÷ÃÍL×à/«]Û|H?\x0001Îpsð\x00127bÉî°¿Ì³Ð\x0000`3 >\x0001ÍpÖð\x0012gyØËÕYgýB): ÈùÍ¯Y8Ru\x0008
ø¯/à°erÖlô2ç¨Ñ\x000e=ÞûÜ\x001ez¡\x0001è\x001f÷]\x0010Ê?cÂ$\x0005¸\x0001j¬ #HbÈêèlràj\x001dtõà\x001fì£\x001aÊh'ïä\x001e%J^\x001dëh\x0015&¬tãÑûë½Oí\x0013^d£r°Û\x0000 \x0018\x0001×\x00012\x0019è2gïÒ\x001bÕòxH!ê\x000fB|ö÷¹ûð¡ÂùïÿøÏ·ÿûÝ§Ór¡Ri¡ªã\x0016eº!!\x0006-VWh+;õìÛïn^¿®(®n^üååã\x0010°\x0010\x0002	ý «\x000ev«º^et1¦ÍÑ>Ó\x0010¨@»\x0010$¦®Û×\x0001T/ê6ljLcð=\x0006ÿEnCè!\x0004Ëmp¬÷Ñ dÕtäRfÅ°YN>!õ\x0018!\x0018xî²\x000b*\x001c\x0008°Bð[8
¡ô\x0010%\x0004\x0014²¨\x0001KÑÂxt!+Í0y\x0016\x0003vÕÒ°$¯\x0018\x001cué¨«e|J\x0003\x00117æ¦A\x000cf	,í\x0012ßiÁà¸Ì´a \x0015Ãfòh\x000c)\x00039ø\x0007m9{}÷ÛÛW7ÿöÛéc û×ñ/\SÖNR=J2*\x0005öÅ|^ß<{ñýÕÍ\x000fÏvf¤èú±_?Z­éíkë\x0007¡ÝDàu|MÜ\x001d16³~ê×OVëç·p\x0019¿Y\x0000ÅKÛú3îuýÍ¬ß÷ë÷Vë 
]\x0001ä1êùÑaHWµY~è\x001f¬_¼GËç×i\x000fIGmÕÏ¿×Ø5³þØ¯?\x001d\x001f\x0010Òåúzùþë¨0.¥2Zê×Ö\x001f Èhz|41B\x001eôô'ØkY~î­>V*Í\x001få!(\x001e¬gÜSrYé×_¬>¿:²%¸(R2T/uQë¹Û9±þCùýÂ^Î
Ë<AJÍ¿\x001cÿ"â¶lý÷º\x001bgÖ?²¯\x0015ý.c1u\x0003P\x0014m~ý°«\x00038³ú{Á|ùÊf]½Êç9Íòùwf\x0000\x000cä\x000bVì\x001b«ùñ2Ðjoó\x0000Ù\x0000+ç\x0001\x0006ò\x0005+öe££öÇEn¨æ3àz­\x0000\x000cô\x000bVü\x001b=®î;è §¸\x00020¢_\x0018è\x0017¬ø7pËßâÿç	Er\x0003tìs=A1ý,Á#Ç/j@ýµkí¡¹\x0001\x001d\x0008\x0018¬\x0018|ÿ BÔTí×ïoå¿Á@À`ÅÀs½ê?\x0017\x001d¿\x0019]¢Õ62¡8001pÒ)>u\x0007¢NwõÙ+°ù\x00144\x000b` `4£àD\x001cö6\x001fÎë\x0018¢\x0008yõAwÅ\x000cg\x0000\x0011°\x0015\x000bWoS}h¾\x0003E¼\x0008\x000cÖW\x0000\x0007\x0012F3\x0012ÎN¾~Ñé\x0011W\x000f4\x000f\x0003¡\x0019µG6?7èTð¨3*\x0000«\x0010\x0000\x0007
C+
èu<3\x001f(\x0014\x001càp~Ö?0\x0018Z1Xª~?\x0013ZiS¥%\x0003º¬\x001fa{`ã$ÂÐÂ"\x0015\x0011c¬>Ó\x0014VH¸ZP+'\x0008\x0007\x000eC+\x000eKì¹\x001d\x0006|öD\x0016+µé\x000elf£'\x0001ÐÀadÅa\x0016\x0015@õâDÝ'ÄÕØl\x000e]ÿ@adEaU\x000cÅHAçdVË$6\x0008ÑÈ£ÁÈÁâ:!Þe\x001cys²\x0000lOÈ\x00040&q­(,qlûþÙk\x0014\x0010Z íþ¿ÉÕ\x000fQ$YE1¡FÁ>d
ã#èk\x0012U\x0010@\x0003\x0007\x0015\x0007'\x001eM*\x0018¹h\x00188f
Ø\x001d>\x0003`à02ã0.Í4hu¢eBlZ/\x0000ú]Eü\x0019\x0000\x0003\x0019qrXV©«PÂú\x000ccEÂ4p\x0018qX\x0013²e\x0000±ZÓÖÁGI\x000b<\x001b\x0000~à0oÆa\x0015¦²ÖLht
0úþ~ 0oEa\³*\x0007(V
\x0013\x001bA«	µâ0?p7ã05\x000fadY\x0002vêÌ\x0000\x00188Ì[q\x0018kØH.1r-Z3¢9è[\x000cÏV4\x00020¾DÑX5ýëSêÊ\x0002Õ»Ö\ÜvÐ,Æ¼\x0015åêû¸";P´2%G/<Ldåú!ôf¡dñÒ*ÄY\x001f¥±xxNÊ»3\x0000\x0006\x001eöV<ÑÉ\x0018äjÎrÎ Ù8ÝÉ\x00043\x0000\x0006\x001eöV<\x0000D¦4\x0004Ôlî2¼¹±Øî`£å\x000f,ì­X8\x0013h2[LB\x000b\x00042I\x001f r
0°p°banZÒ÷¼P¤G¢ÎØE®!5\x00020ðp0ãa_¸ Ù $íË¬
jÀ(\x0019\x0011\x0006\x001e\x000eV<ê\x0015ÖHZ\x0011\x00113®É\x00084º\x0003aàá`ÆÃkY\x001c¤Ö>ÖX \x0007Ý\x0001«\x00134Ðp°¢á\x0014Òp5\x0018Nú\x001eÀÃÖ?X°"1ÖÀ÷Â\x0001\\x0011'Ë×ªDVÑ|\x0018( XQ@váZLhð"BJi]~±:>q° ÑÊæ\x001a}i \x0010ÌVcY"5@»ÃÉfÖ?ØherõÚçç¬\x0014H\x0017ÈÊ`\\`³þáúF«ë[ªë,\x000cÆ³í\x0014@Ô@Ì¼è8VÄYÝß\x0016	>õ¢¥¤,ç\x0004«\x0017mdâp£Ù\x0005þÃ\x0000@?z\+St\x0018Çù/Ã´Ôãê»0ñ"ï¤åMV'	\x001fâh£+«q@dÿt¹\x0011T4(0K
Qy\x001dTxÝÂ\x000cÄu\x000b3dm|ÀVÅðÙ¹²±¨\x001fFI´8}ïã©­éF\x000cç£4ö2ÿbôjF"{\x0004Á£¦L×î8²-K=´þìX%ÃcåÒú\x0000\x001e\x001d?Å¶S+ðÑ\x0015«\x0012"úìX\x001dXÏUÑR´ æ*Ã¹Ú\x0014Õ®åýñ_?Ý=8Zå+ùÍ¨*\x0007Ö¶\x001aDhQÎZ\x001c¬ÂP÷É2´X!»&xÜP(\x0014\\x000bd7%¦Ë{?;Z&+Tp­r$}
p(±°º"Õd=ÀQMÝ\x0015)«o\x0018HÅ´«É"­TÈJmÓÅj\x000fq ³Ü\x000fU\x0001n\x0000	²\x001f®¨é
`´\x001føÙ~ å~°LcáËáÑ-é±2«»mG4Ü\x000e\x001ej Æ*¦¸:¼¤YKí\x0019 ÓÖê3³kfs½Ö±qK\x001dJ\x001fWÒ\x0017\gU\x0008La C\x0010©,iãæ$êhFJI],Vù?\x000c]`iªp}¦C]¡'eÀr\x000e/Ã\x000b]<ôeê\x000fÝ(À¯ï¿ºù7jna=ör\x001bXgIËGÑÇÅB~7üûæÍÕ×·Ï¯n½:¾rìWç¯\x001fàr[y½ÇIVNò[ñVNýÊÉ`å¡uñ\x0016ÏS\x0018³,\\x000eK¡ýFû~áþüó$j9,ÅIÿbE	¶PÜ53+\x000fýÊÁÊA\x001e;ëÊQ§FðºðÝÆÅÇ~áñü¼ÞÏ¬³^\(ÒrYW¾Û±;³òÔ¯<\x0019¬<m¯+OR¢PW¾Zcóè\x001e½ðÜ/<¿p\x0016ÖOÒ¦åBÖuýiÙ\x0013\x000b/ýÂÁÂe4\x0000[Ä o!<dPÏJ
\x0007lV¾ôW\x001eXÈ¿ôÊÊB¤\x0013ÊkX©¶öGÜO¬|äO\x0003\x0002]éx\x001eÒ¾`¥9Ýfå\x0003\x0001.
]má^ôø«1§Ý*À\x000fü	ç\x0013(æ,îVñ\x0014$·è\x0003½¢\x0010l\x000b\x000c\x000c
çS(r¹ÜQ\^ý Kw»éÝ¥\x000f\x0014
çs(V\x000fäòSeÜíLî®Kß\x001fy=±ôDá|\x0016E\,K\x0007ÇÖ}YºÜÑúßgô&kÖ©¦è\x000f«w~õûÿÇÞþZ\x0017s¾À^ö\x0013nÇt4®£õöîÚÉÛ«çW·Oë_îÉ¶u\x0002$+\x0014º\x0004\x0014­\x0000äB\x0016iÆE
ä§3Èá9hµé\x000fº)_³\x001eÏô9ò)]Óbì3ð¶\x001b¼\x0014Kä´|þ\x0015x/\x0017ûåâYËs\x0003ËrKâ\x000eÇíz²^Ú-µäz©_/·Þ(ú(y@£ë\x0015ñïºÞMáÒõú~½þ¬õ(!hÎ¥\x001bÏ%"ÖzFv»ñ\x001e¹ÞÐ¯7÷}´NåìPÚ\x001d\x000f]õúMqõõÆ~½ñ¬õú$¢É+Å°íµQ¡\x001eÝ\x0018âëMýzÓyç!/y`jõ¤³rÚïÏäzs¿Þ|Öz\x0011E>çj\x001f\x0016cV\x001c>Ô{ÄøÈõ~½å¼ó@×²\\x000fò P\x0003éqHåüÏÛ6n
mN\/Ïglö¡ÀjÏ¢Ð¬ß×ï>=rÁ#½Ço\x0004×bÏª)&ÉLe	}«ÑØõð\x001e¹Þßà<s¾Í«\x001fô©ËÅ°~à¸[~ùÈ\x0005\x000f\x0004\x0007ç1\x001c\x0008æºû\x001c	´\x001b'Õ6Õld#<0\x001cEqÄp2j¬¥9è2r2 d\x0018(\x000eÎã¸jxåÊ¹ \x001aYõÊI|Ur<ß¤Á@qp\x0016Çq\x001a[8¹DhT.Dáõì\x0016°>r½\x0003ÅÁy\x001c×Æõ² `_ô\x0003íù³_ðÀqp\x0016É-S2Û;A5î×EN°&\x000bªá°°\x0011\x0003ÉÁY,W##ÉnÔµ%H¨_XT~Ø4½^\x001cH\x0003Ï"
ª1©ËzåI åõüoÐp°Àx\x0005¦ä¥ª s\x0004Jr\x001c@*ö«ÕØ\x001e\x0008ùø\x0005\x000f\x0006
Ï2hÄ»òy\x0017\x001dgL#Áuç/x°\x0010x PDß ^¸2B¶z¨w\x001fµ`ÂÁ\x0004\x0013\x0017g8×d*Ç¹kq"¼2\Ìç\x0007q \x0019=kèóó©\x00079°øE;\x0017\x0014û'­z,vKï\x001f\x001bËýøïc4÷ïg¹ï:\x001d¢ú>Q\x001fáÒzSÞí8Ü^òò¦1¬Ù\x001eý³=ß½÷÷û·w¿,	Ä×~ùêTí5Ð®>."ÅÐí¿:q[×ð»W/¿½}qóÍJ|ýæã\x0018°Çf\x0018býêÍû\x0004®kn[¸â¶y\x000cÔc 3\x000cc@­5\ä8\x0011@OuÅó\x0018|ÁÛíCÒáàëh×Ø*Áã\x000cRè!\x0004»mH«\x0013·?\x0017©Ü	tPÒÚ2?ó\x0018b!ÚmCu\"­B0Òü\x0013e.ü"\x0004³åÊÎcÈ=l·\x000fÕ\x0007bONN¢z,Zf\x000fä·lê4ªîbZ\x001d¸t?·;­\x001eouÔ´\x0015\x001d¢Ýa\x001fì\x0008qÛ°e' h3.­;a\x0007b \x0008°c²¶¤³Ü®JÃ\x001cÚ\x0004¶\x0015:çA\x000cÖ\x0015ìÌkÊa=NèVx\x0010ÇØ\x00071Ø&°3NÙÅu'HÝ;J%®ú\x0012O}ó \x0006ã\x0004vÖ)³Êº5%U,Ïp7Ìî\x0004\x000eÖ	
­S¡k:Ô¡£×"Õu'6\x0003y\x0010£çgx±\x00194ªûU5¯Xû6/çA\x000c\x0017\x001b
/vµ«^Å\x0017©³Nk·ýfÉÊ<2(vDòR\x0001R\x0003Às
[·\x000c	\x0008,=§¾z»yOüÕ~°
¸ø±±è©ÈI÷v¨p3yy
®»Aá\x001f¾@ö\x001e\x001b\x0016[j\x0008å\x000f=`ø\x0010
ZB\x0014µkÑ7ÕÉ&)FËå³×Ö¨ÑïX$Rèêê¿}÷é÷ßÞ^ýãÿ¾úáþíÇé\x0007wg\x0014}\x00104\x0003ês\x000f\x001d+þöåçÏ^\Ý\ýpûb§;@Q`\x0002íP\x0014n[j(
æ\x0008+²óA=\x000c2\x0011È<_\x0013\x001b¨0¢>]ìªÖÍ£ð=
obÍ¢\x0015Ò\x0019·d)å\x0001æX­ì$ÐÃ\x0008v0¢RèõYK¨ôá`s öi0R\x000f#ÙÁHR\x000bî$¡7¼¸]=ôy\x0018¥Q,a´\x0011Å¹EÒH`è«\x0008\x001e«í\x0001£¹µ³·<mQÞ\x001eã\x000fÁ!\x0015o%î\x000eÇ1X*04UQ'\Zb¨C\x000b\x001b¸ ÄöXõï\x0013íhéóÍéj·8\x0008ZõPwEÑl'©N<]\x000fÑtýÕF¦K.Ë*»Æp\x0004MÚ/]}\x000cÅª®Üø¢Áj>ÝU¹{ÿóßî~¿úÓ»ÿv¢	5,dù)\x0011Buið»¯ùåæÕí?ß<¿úÓË'>\x0005{,h%k'XH+\x00137W°ì\x0016»ÎC¡\x001e
ÙB\x0001·¶¾³ÂS«.EG]¡?zaæ°ø\x001e·Årx8\x0018eÔ8¹\x0018´Ç7íNÇ\x0012z,Á\x0014\x000b´fQrG@,\x0007ÁEÚ­ÖÇ\x0012{,Ñø\x000e£äÁdbê\x0019+a½ú¶÷%õXý¾¬ÛÒ"^ÞU}3Íx\x001aÜCÉÆPôY¿^}NP±\x0004Ý\x0016ÔÃRz,Å\x0016\x000bQ\x00173òjÆüz[6OrxZÒ\x0019cA\x0019ýÅGÌËmñ«Ð$íÎmÇ2¾-ëwÒ\x000eµPiÞ>²o¦yÔÝ	\x0006ó`\x0006Ö\x0007[Ú\x0007Î\x0011É\x0019s\x0012\x000eWW`½/ûó0æ±\x000c´\x000f¶¼ï*Ù\x001d«¨JnX(kmÃ¾æ<öÁ÷ÁÑ:h_×±	ë\x0003Ø\x00073p%Ø%-å áCÒ¬FkÕIØ\x00193\x000ff K°eKW¯\x0014/ÆEÉaë\x0004¸;\x0002j\x001eÌ@`ËÕ¯a8{#)K¨§\x000cö[,¦±àÀ1hÊ1TJ^O\x0019K\x0013	\x0018WV0Îtcp \x00194%\x0019â8\x0019\x0011B\x0014ôù¤\x001aEÕúú8¦$C%g½2Ü¤Øâd%¬ÏC»m\x0010ó`\x0006Ë¦JõÅ¢Ü\x0019\x0016Ým9f\x001d`\x0004uoLÁ\x000c\x0019M-3\x0015\x001e¢ ;Ãó\x001b\x0016§Ù£ù×9,-CS[Fu
\x0004Óþ+~}\x0001}¹K¦¾?\x000e¼rÒú<ÅþpLeãÛ

ë¨ ý\x0019\x0005óñ\x000c<Ä\x0004Æê1Ë«\x001cK
·Ò\x001c\x0007ë\x00046_lÝ4ü\x000c\x0012oÓ\x001f{àó]2ß&\x0000·: >È¤KÌq\x001dÕévu\x0017O\x0008??ÃäÌ1|½X¤rõ+¼¡¶FEI1ß\x00178z2\x0014«Ò[X={kQú1¡¨Ù ç³m²6z~y{$Î:å\x0019«õV£Ñ6OX\x001eb*ö'/°T]Ë\x0019\x0014u\x001aêÞiv\x001dwú\x001f\x0005©õä<\x0016dÔ\x001f:)'ÿø¯÷ÿøxÍ'%Ê´¨¥«NtRk«pØ½9·WOn_Ý¾>¾nì×g¯; Ö¼åâ\x001a¥å±	¶'Ñn¿Úã×Mýºéüïé:Ê÷\x000e:Ë¥ /K\x0015(LÖíûuûó¿wôµ\x001fGj´s×vÑ¥xÇbÝ¡_w8ÿ{ó([ík,×)¶\x0007j+ì3ø£×\x001dûuÇó¿·\x000bâLÕ{\x0019®eÙ9ë1µÚsËNý²ÓùÛ;iC*\x0007R'éeÓ7`\x001b[ûEg\x0013\x001b¨ßÚk\x0014Ë6P?vÚ/G{ôºK¿îrþº¡Hô]\x001cg{U5A[\x001d?¢zõ¸ewÒ\x001fL9ÎÀ\x0006ÆµÃ ùÞQ«jXÕÆdá#W\x001a%\x000fö\x000fî*­Ä¸\x0016lD£/>%Ï>y©câ2\x000cíîN~eùM¬ \x000cl	çÓ%¥$tY\N«\x0014\x000fH¶¬,\x0016Ìbá\x0003]Âù|éCÒÞé\x0012dh¥\x001dÕÛ(°/füèu\x000ft	çó%E`Á.þàPý*	Eà¥þëLx\x001e\x0006¾ó	\x0007¥4Öåëã\x001d{·6_|`L82\x0017yÚ&Ä\x0001¤£[:WGûiG/|`M0 M\x0012úÔ5\x0006é's1Ë`\x0010æ\x001fu\x000f¬	çÓ&\x0001ÊlD\x001eu ªônÕëtLÖ\x0003m¢\x0001mVö	R^ç¹Þ¦\x000f­õuÎäãÀx>k\x0012\x000fÐleÀå\x000ebR@&dTÃ¾;céñ\x000b\x001fCÌóY\x0000D)6Í\x001aªER²?"úèe\x000fçs&Öe\x0017ùÞE§\x001fº\x001aPÈç.q7[þèu\x000fçS&e·º³üåE¹\x0003Q/¦ÛW£ôÂ\x0007ÎÄó9\x0013kLß¾7:\x001dyî|Ñu\x0003\x001cS}äº\x0007ÊÄó)% ZÙ\x001e¯QÚX\x0002JÑë²Yø@x>ebõas³à^V>ë\x0007G\x0015\x000eç3æ"¡/7H´}+Õgýà<_Äbá\x0003eâùÑ«öuaU1×G)_ÀÛp\x001a8ÎçL"Pà\x0017j\x0015ç\x000eQGsT&5!{\x001aHÎ'MV\x0015oZ(\x0005«\x0012E;¨\x000c=Ä]ÍÔÇ/| M:4YÉ=5¤ÌC	ÛÝà¾\x001e|\x001b?ÆÄ¬\x0001mRQ?\x001c+mºf
=àÕ2=ØbÝ\x0003mÒù´¡h\x0012Æ5Ãé£ò=Äý\x001a¬G/| M2 Mð:Ã<©îçô^Ó§ý
øG/|àM:7«'./¨\x0017µùzR¤)ºz]»úÖ_øÀ?t>ÿTW\\x0007D\x0010¦uÊ\x0002~q°I\x0003ùÁûóÍx=+ë\x0017\x000f Í\x0012Î¼²\x0015\x00164Yø`
½5"Õ^RÔ\x0018Â;uUp¬ÅãyóÇ_\x001e0ç/\x0016arh	\x0015à\x0011 AÃdÒ°Í&¾¯kÿø`í\x001fÏ÷È£@\x0008\x0015¹K®ãg\x0000v\x0015¼gÖþÓµÿt~ø\x0016äE¶\x0013°:zÔÁ\x0019¹Z~^l\´>ç¸ ,?¯Ñgu\ôÓ§])ç	:úñî\x0001!Ý[ãjfØw\x0011\x0017ÀÉ8´c­r\x0013§æîÁ©9{éÄï³E,û0Ûmõ·M6YD¢Ï
\x001c\x001bRýÙÊ©¤	s)®jbá]|¸þh±üÀñsçZÐ$î*KÅê\x0003'\x001bú¥x%§ø£è\x000f]ùÇ\x000fwþõÓ»e]'i£\x0000­rymÑ¢â@KßwçÖÕÿpóæ¾yùì\x0011\x0000°\x0007V\x0000XFdj°Í$
\x0018µXêXN÷ñ\x0000¨\x0007@f;@Q\x0007¸ûR®cÓ\x000cò:ã\x0005áÈx½\x0019\x0004¾Gàí\x0010k=BE¼ù
\x0000VÑ£ý"ý\x0019\x0000±\x0007\x0010Í\x0000\x0004§õ«<ó5Ë¼ö°\x000e\x0008ß\x001fû1 ÷\x0008²\x0019\x001aF\x00059CQ\x000bp½Çõ\x000cÙÝQ«i±E\x0019ýÌÑC\x001chgªª -'¢Úªq¢âØo(ÃÑ+-8t\x001cµ\x0001¼¨6\x001cNíâ*8U\x0015l\x001c\x0007R_kdô\x0007­yñîãûûÿñÍÝß\x001f%®ýÏ
OYe±\x001d(ÖÖA°VÝUÓ´Û
ùâå÷¯*ow¤Á£0\x0013tÖ¡ï~ûýÝûßNð+PêÏsJÿØü
)lfå#­\x000fß={þòÕ³ãëÆ~Ýxöº©p¾h;ÏÏK¹ i¥Lòû'æñëöýºýÙëF}Ï,
é¤Ì\x0011Ü:\x001aÎjÝ¡_w8wÝ¾õTöuâ&-sä\x0008ÌfÝ±_w<û{»"5\x00049eÇÚ>í|^ÃcJp]wê×ÎþÞ\x0019E#»\x001eeÇÚJ­W\x001aßr´º¹_v>ÿ(±V\x0008ÜíÖÓc\x0002Îè`\x001ff5ÒUÞlU\x0016OgçDrÖetë ¾cm\x001e;Ë_HÇ\x0011aÖò@R?û»O\x001f\x0017&ýúÝý§÷'òh,ZÃ)µú¡9»¶øÈuOåC²\x001d$¾|óýB¤_¿¼}ójF\x0015\x0000ö\x0000Ð\x000c@u\x0004¬?IÁiurZ\x000eu#hód\x0016\x0000õ\x0000È\x000e@nöº\x0013mû ë\x0016äm\x001f\x0016ï\x0011x»3­ñ!³\x0014ÅbÏ\x0003µ\x0005AÜNôÌ"\x0008=`@BÝÌãã%ËV\x0011ä,\x0008Û4³\x0008b Ú!(-½Ì¼
¬òÅ£" íJY\x0004©G¬\x0010Ô/Ïuî\x000b\x0002HòØY\x0008§§\x0008¶û\x000bf\x0011ä\x001eA6CP
èò²ën¨(HEÐt »²=ì|\x0016Aé\x0011\x00143\x0004èI\x0005¸>5n/^\x0000¤í\x0011a\x0000\x000e
@í½ß\x000eAfe\x0005BHR\x0016â¨§W\x0008a»ác\x0016ÂÈÈviÉ©\x001e\x001bT\x0012y~¤X\x0010Ô\x0018 Xñ\x0001\x000c\x000cfÐ·\x0008u\x0013ðàT$õ*Üö+ú,Á\x0003\x000f_Ü\x0018]¶
_v\x0013Ò^°8\x000ba e0cåÄr+¹£¬­Õ\x001aµÜ!ð«\x0019ÓÀÔR{vY $z\I-
¼=!t\x0016ÁÀ\x0008`F	uÕH.3H/®U©ñeÞVíEE3Ê\x001aª¹]ÀNF³¨)´¾¿z\x0015h»ýbÚ¢ö©O±ªKö\x0005\x0018Ö%¬¬ârË°
Á~ÿ·ßîßòøµ­8:T
Ûà4®\x000f1ì½ã}ÿçg·Y1ö+Æ³VÌÕõNW\x001c5&\x000ekÆªnÄÞÃïcWLýé¼oÃµ,§tI@ÖÑ¨!ïæN\x001e»`ß/Øy(@J\x001aëÓZïU$ý]W¼«\x0006üØ\x0015~Åá¼\x0015§uölôa­eL::î\x0004ê\x0013+ýãy+öë8×äöó{¯º÷1îF?vÅ©_q:oÅ,\x0008¯©â¤¥Å"­É¨½\ÚcWû\x0015çóVL "uqQ\x001bq<h\x0017h,»\x001aª]qéW\ÎZ1\x0014/\x000599Ó¾UÒ\x0005§°ûlóÈ\x0005ÃÈ\x001fç\x0011ÈÒáÔlEö¨òäÓ:ÌÕ?`°Æp9@ÒLÁS©õé@û2î*$<Ú\x001e\x001fjE¾;Ï$/v¸dÔ\x000eàh5ÉdqùBÅnfY³Ø'ßÁv8\x0012K±KY"hÇ~Ì»Bf;«\x0016\x001fî0³GPèæýo\x001f>þÆNÝûßîÞ:x¨ \x0012yn-#î3[\x0000\x0000\x000f±Û\x0001póêÙëï±g÷êÙÍ1J\x0004{$hD«æ+\x0012Ù=\x0015\x0014lñ,Ä½\x00034z$d$\x0016\x0015¯>&#«U#A²«?
Ä÷@¼)DB¨\x0015\x0008ÉãT\x0005²nß5DÓHB$"É^e1]\\x001a\x0017$Z\x000b\x0005Õ\x000fÛóÉ§Ä\x001eI´Euâ\x00027\x001d7\x0019é$êá
»½ÓHR$"a\x0011Y9]IkXXLOWÜ\x001ds5$÷H²!à¸\x001aätyÑØ©H\x0002q¦«ô@)\x0010nÄ-É:;Þ;\x001dÙ\x0005)í6üÎ"é³àî+Õ±±¢
\x0007õty}pIÊ¯+]Y¯i(#Å[r|p	t(àz¼Àgwï¦\x000c\x0014\x000f\x001c\x001fX¢\x0008Çg¸ÝszSÒî(i(\x0003Ç%É\x0007VÀGÙ\x0014®7iHtL-äýÒÔi$\x0003É%Ës*Mõ¯\x001dën5;\OrãæÔà\x000c$\x000f,\x001fÐeï=©ß$ñ<\x0011ùÊq·
p\x001aÊÀò`Ió\x0004£#8­\x001c®w\x001e\x001c©_\x000f\x0003Í%Ïz\x0017¤\x0011¼D6ÕcÉzUân5
eày°%z6Z DÒÈCô^-ñn\x0016o\x001aÊÀô`Jõð]ÁêÑêeD\x000cÔ°Ñ­Ô\x0010ïðLã\x0018x\x001eMy\x001eÃ2ë¡ðÌ«Ü\\x0016*N/JÙ2p
r
pMT· êXHn=Ñ]	¦.1\x000e\x0018M-1Vóëèk$\x0017EÃ\x001cvÇCLC\x0019Ì\x0017/Ä\x0003\x0014¾ó
IH«!6
¸h¸òdzåEd[ÿ\x0003ïOM)YÏW6²^åa\x0002¯¸^ãùowÿ»_ßÞ\x0018\x0002£÷2 \x0013Yi®\x0005)ä¼éãa\x0017G\x0014ÿ|óíw7O_üó>\x0001\x0003ö\x0018Ð\x000eC"n[0¸Ê­ÍÌeQ¢ÁÄ2`V\x0018¨Ç@\x0018P&ÑWZ,òF@K?ý!\x001eb;Á÷\x0018ü¹\x000f¡Ç\x0010ì0¼Þ\x0007pRÎ\-môá¨øã1Ä\x001eCü2÷!õ\x0018\x001dÊÙ9¶ûP~\x0005CÒ}ûÑÇ\x001cÒc(¦ûÐ\x0012@ÈBµ:ü$Ë»_½Óû\x0013g0ÀÈ\x000f\x0004QÃ@ÐÈ¢\x000fÃ\x001bu#öç¸>
\x0004Æ\x0007$q%¹§÷ïÞÿzÿáêÕýÛ»O¿¼ûx*\x000eÔò
ÃT&9§ÅXv³ÖOo_¾zzûúêÕí7ß¼Ü\x0019E­X°Ç¦XF\x000bIbÕËÑFëæ¥Ù­EæÅ\x0016
õPÈv[¨Èh]Ö \x00147êÿ#gcÞmßÇâ{,Þv[\x0002ò(íöXu¾fÑ²+Ha·qm\x001eKè±\x0004Û}©XÚ\x000b¢ã\x0014Òní¼&¯cÜµ¿óXb%~Ùûz,Év_bü+õê\x0014áH¿a/é;\x000f%÷Pò½-¥ÇRl·¥RJmÁ ²©êµ\x0008¢Úæ½hp\x001aËáÝjaJ÷Eo\x000c´oÌû%ö«\x0008d\x0007\x0001ÿ?m;»úvó`\x0006Þ\x0007[âÇ\x0000×É70\Ã)ÎLÖfUGSâøÁùëí:¾êE©ù%¢\x001b\x0003»/½ó`\x0006æ\x0007[êg³\x000cBxð#E½ÿ¦f\x0019\x0006æ\x0007[ê'\x0004\x0019ÉÈ­\x0007ËÆ6×ån\x0012x\x001eÌ@ý`ËýÛÚõ'\x0013\\x001e*\x0018Ú­È\x00073p?Ø?Q\x0014ùÅ\x001aÌ'\x0019iX\x0001ÈP"\x0008yWQl\x001eÌÀþ`Kÿ¸NXª÷?´{5Ì¨?ì\x0016DÍ\x0019è\x001flùk]ü,ªtURÀ´[F=
\x0006\x0007þG[þ¯ Õ¿Õ\x0000hÑ\x001dJÂÖ¥)câ@ÿhKÿ<»Æ\x000b\x0016Òõ@nLÜ\x001d9\x000ff\x000cûméªk\x0002&\x0015Æý¡ì\x000e>Ç2Ð?ÚÒüå}Îå¤8<VMÀìVkÏ\x0019è\x001fméj(Ä\x0005º\x0016W&ºõöGSS\x0003c¢-c\x0012«Ì)ã\x0008SÀ$y\x0011ª7f÷µq\x001eÌ@2hK2<+Lo\x000c\x001cN\x00198=eTLã2\x001aì2\x0019Ûå\x0002+K%b\x0019!j
3pÖÌ\x0012Ì`ËÈØåÄSÛÛÎ\x0004	2	ýk\x0014jÃ?þuÌ0ýÕ6dÒ{RCfä\x0018­ÌÊÿÉ[G}£®DÚbÕ\x0016GW"rò|qaMÍ¦Ý¾×S¶è§q~2Ý¢\x0018×¤9kIj`Ñ¤\x0006Ù^æ×\x0011Í¯¶\x0007Î_KÅ$\x000f_)rÞPkwôrNB\x0003ãõ\x0001Ûë,{²¶yÈË\x000c®WÇ8Ó¼èâw\x001bóíÆ\x00142[\x0013Qê¯\x001d+»«§À¹\x001báÜ}É·\x0006Æ[\x0003¶·æ\x000f=g03°5g(ò¥NZ\x001aõ! Ø¦Ïê9ûy<g?Û3é`Í÷$§Öv5ë¹\x001fwæþK=dàz_y\x000bP_3? Ko+!«Ò¯Ã Ú´ÛB@ðÐ·©¬fìÛð\x000c°Væ³¸ÒHIó«+m\x001a\x0017ÔÛs?Þ\x001eÓ#\x0007u_¤*ÜqÌÅ\x001dPoÀï{:åÔ=ô>¹÷´>t¦Î¾yMÜæócj¿´twú+úC'vü§»O?½ûôþ×IÁi\x0016z8üü¡þÏ\x000fwoß6ái~^[*jB=fjí²v´ß§þÍ«?Ý¼ùúåWOP\x000fø|Ï_\x0012\x001fioÅ·ô-ø¤ÜBÚ\x001föv"¼ØÃW÷Ì7tE-\x0014S+ºmM¬3àå\x001e^¾$<W®}\x0010|´Ê¢'ñ+*>8"c|
¾å={Å§ïÙ\x0000HÜ\x001b\x000féç\x0006àkÁ'\x000fõ!Å}ýý\x0013á
Æ\x0005.h]¨ø(
G
4ã¢í³ÿ\x0003\x00177Ø\x0016¸ q!.ziO`Áç,ïyXÿRñívuLà[¨
\x001eÖ%B«K|ò·û¿ÿöË+¿»zòþÝoÿ~\x001aËÈÏM#Ï¥\x000f**ø¹çÉo¿}ö\x000b,ß\=yõòÙÿu\x001c\x0007ö8ðËÃQÝq?ÇµNôîÃÇwo¯¿ûôo÷§:\x001d¥ö\x001fÅ3Ï\x0011.teßÓ½yýýË\x0017WÏ_¾ùávÇR\x0010Ø@C\x0010!JxÌÑÞUC¡ÃÜ£Ý´Ý\x001c\x0008êA!D×¡ú\x0010Rµ\x0013å<U\x0010»½Í\x0018|Á[nDY\x0007P\x0005É	×Hº\x0011û¢v B\x000f"\x0018¨7[Æî\x0000\x001e\x0003E\7bGx\x001eDìADK\x0010g°/(\à§º\x0005\x0005i%þy:\x0001EêQ$C\x0014\x00055\x0017GEëò(zÝ¸Ûú;	"÷ ²íy^ï\x0013%\x000f\x000eÔ~\x000bà$Ò£(v(BöJ\x0014t/"¦\x00085\x001c°;PbÏî%ß\x0015äù\x0011.u:Ä)í\x0017\x0014ÍÁ\x0018YÛ¶ëJr1XiôLÀð¸ÿ1ð6X\x0012wô×Ø\x000e(&­*`5°¶c=\x0018\x001b,©;hÅ-ð`f)\x001f
\x0005t7p·ýl\x0012ÆÀ{`I|DêF\x0011ául\x0011"H\x0007c\x0001`;úî3jÂ×É
I*\x0008Ç\x0004Ø^¥*\x0001Æ\x0003\x0001\x001aÒxz\x0008&Ù)^³5×¢è½»)Y\x000f÷!\x0018²\x0005ó\x0007:º¥,h¸¾\x0015ìKÊ! Eé»m¶lº°_78åÁ¶\x0014ã3õ\x0019r\x0011ùjWfÜ½z\x001cLKC~A8zq÷ñ·woï~?7¥·TÚJÂ¹¬CLAî~ue¨ø¿¸ùþÙË\x00177Ï÷\x0012Aá`X 5\x0010òÇ(3H«ïÈ!HÒöøùY$Ô#!ó-áXJ²¬Á¯m\>Ë\x001b\x0000Oz±Bâ{$Þþp-¢µË@¼Âç(>KÈqfÐ\x0004Ðã\x0008Ö8 «\x0006YàA*ÀàtGÒ±i\x001d\x0013Hb$ïH\\x001f(
>6\x000eÄ«×}\x001dg¤\x001eH2ß\x0012nªIòTdú\x0008²º³>\x001d\x00013$÷H²ùø #-C`-²¶'® `Ún\x000fERz$Å|O|iËóWÓ¨\x0004#²J!í4:L"éÞô8Ún
\x000fIMI ¢Ü³%/yy'N2\x0012¼9Ã×@ëZßìt!\x0016Oº)q»út\x0016ÉÀð`Nñä¦\x000c\x0014\x000fæ\x001c\x000fPÚLÃÂZ°L.­ªI­W
ì­\x000c\x0014\x000fö\x001cï°Ítco¥rcÛ\x0013Z9\x001e¶kµg\x000c$\x000fö,_¯ì	G.B)®d}?Üî2°<Ó<ä¥ú m
¨î~ý¤.¤\x0019æÁç]B\x0019\x000cÎY\x0017q1õQ\x0017Í×@ó`Îó\x0010T]¸:x¤\6I³yõX¶Õ£f¡\x000c<\x000fæDÏ"õE\x001eÚëñ\x0012ç+{uYÒN{ö$\x0014\x001c\x001eÍ\x001e<´YìGzÑÂ\x0012@KvòvßÜ,èÑè¹vLw¥¢òþaíÛ®[2ÆòæL\x000fDÒ2Ãb2m£:-N\x000fØN!Õ,éÑé÷j=¡ôec\x0006eX¶\x0005¬g¡\x000c\x0004æ\x0004YY]\x001aæ8Iq\x001däÚ;Ñ\x0017\x000eq§Å|\x0016Ê@hO\x0010¯I\x0008Ò\x0015~ÿmE±I+ÙvTg¡\x000c\x000cö\x000c	^´¸Ù\x0004¨+R²+;\x0003]f¡\x000c\x0014ö\x0014éHtSë® äðª\x0007¦é\x0014·\x0005¿&¡ÐÀ+dÎ+<Õ!Ê]I«\x0005ËÑ©ß²Ý¶0d \x0015²¦\x0015*\x0019äÉ.PvüÇå|\x0011©\x0001\x000bÛcvf¡\x000c´Bæ´²ø-b£W\x0017¬ú-´:VWÆ\x001c±5­,ª¤¤ó¨0É¼Ôº+ÞÌ\x0005£!$ó\x0008²þ[[»ââLfñðq5Å°ý2d H²&È?ôª\x000c¬BÖ¬B\x0005\x00173IÎs¯/C©á¼°JÈfÁ0
¬Bæ¬Ân\x000b_L:Ý\x0016e\x0015g\x0016
Ó\x0010xuàµìJÓXv%é¦øuS¬Î\x001føÑÛó#:=Ü|I)T}I«¸Ë\x000f\x0004éÍ	2ó`¶)X÷G<ü@ \x0006,ìL\x001d2\x0010¤·'Èê\x000bË#*Wtb\x0010_\x0012Ômw(Î"\x0019øÑóct-{\x0012ÓzË&XíîÉøjMT_{\x001aâydu\x0005qîÍl\x001fÈÑcvú\x000e±4¶\x000bï¦$ëÝ±
\x001eýÀÞ\x001bSq×m,k@\x000côI	%À¶øÅ,\x001b½57\x0012ÏkB(E\x0007´bÒr©°3fg\x0016É@Þ\x001ay@nS&\x000cPc/±ÂÞ(1WíX¹aàÆ`ÍÄ=­M\x001b\x0019_}¯j¾4Ï\x0012ÌìÂÀÁ\x001bc½*m\x000e]µ½Z\Õ!\x00167Òãv÷ñ,\x001b57Ö\x000b\x001bY9J^·\x0013éËº+f¦8\x000cä\x0018ÌÉOÚ Íàv#\x0016ÑígS`\x0015<\x001f=?Rh%\x0015\x0015)=ÆzUÈ¬V*5Fæü\x0018=éUq)Ki4âÊ*ÕÏ4»*Cv5XgW©T^²«\x0014
Ã\x0018¼z-f\x000eq\x0018¨>ØSý\x001fÈ*\x0003Õ\x0007{ª¯¾}äÄÒÒ6n
Ô´\x0012\x0007æ\x0004¹È[LqÝ ¹ô\x00104J±{~\x0003©DsRÉqÑP]pÀ%iä5ÍRÌJZâ`£¹%ÎÕ~\x0005ñËúÐ\x0015¼¯\x0005\x0011±HÒÜ~e\\x001fº046ÖèQTÂN÷,áÖGó[\x001dJßÐ2ÀQÄ\x0007}Ñªjâ¬|É4Üúd~ëS&~sl\x0011$¨/écÐ°\x000bÍ\x001c°4\ûd~íSD-F$&´Â=\
ÛV\x001e2\ûd~íGQKª÷Ãñl±ÆzW|&«74\ûd~í\x0013fUÿà\x0001^"R½ÕÅ]i¸öÉüÚÇU@=÷2\x0005Ôô<¨Ù\x0006H\x001e.}¶¿ô.i®\x000b¨\x0004Vy{»\x0007<\ùl~å£¯îW+©8	fhÌïøVL+Í¯|ôI&,ácS®P@£Çb éJëá¥-Í\x0016\x0010¿ ¶3Và!ðbÍêA\x001bÓV8 i_jy^\x000f\x0011UoÌ\x001cQuÈ¢v\x0016`
*\x001bV/¿z1ÁìÈùô\x0010O\x0017@ÄÎÐ&Bag@\x0019õÝöL×Ù®\x000føìÔ]àÐÕ½Á\x0010ÕÓw!µIKÑ¬vÇvü\x0005®\x0011%5wY(f!0HeÑíÙíÓ	E¨·OÉÜYÿ 3.\x0003«ø·ñP\x0018½zÏ\x0011·Gª<\x001aMzØ²ºÕ_î¯ÖW/\x0012äi¯\x001aë\x0008Ræºìí\x0019\x0004\x000bon¯Ú_\x001eÅ=\x000e4Ç~[UÓsZ"¦e	\\x0019nz\x001cd£î\x0017MG6ÎRÀ\x0003´Þü#'ëñ@|\x000fÄÛoÈzá+Í¬åaAk\x0012ªû¿Ï2\x0007\x0012z Á\x001c\x0008Fç×Gã¢ù×\x001cÄd\x0007z éË½ê¹Ç/CÚn«ovÀ¡=RG<ÌGÃÁb½ÉòQ£±úñ9iµzÚ·30m\x0012ÈpÓÁþª³T$¬ÐZ¯Z\x0001V÷¼ëóJ}ÝE\x0007>MËEÇeîs»è ¦7mÏ\x0016D2\\x0010°¿!°è87ù²¾yçµ\x000b:ý¼G#é:RßQd$;gÒ[\x0019¿ã*q\x001c³\x0011\x0012\x001f¼ø(\x00077ø\x000bÄ\x0003\x000fñÀ%ð\S\x0016Å\x0019*\x000fa©8U"ýåÓÕóWOÞýþîíýïW¹¿{{õôÓÿ9U	=\x0000oÌ°Â"ó8=ªx\x0000púu_óöù÷WO^>ùâöùÕ_no^\=}ó¿öTÞ\x0015\x001böØð2ØR7\x0005ªHÐï1F&ð;àE°Q.
]Ý7\x0019¤æ·±\x0011ä¤3\x0006èVñØ|Í_èL´ìÖ}\x0003\x0016ÝÎdÐ!q\x0004{ZO§c\x000b=¶p¡}+¢&è*Ë6ý\Oä\x0014\x001a\hÛb\x000f-^\x0008\x001aèuK9I\x001fY=EÆ\x0004·;\x000eïtl©Ç.fJÖ¹$#Ø«)É:Ò#Àeö-÷ØòÅd#²å3©ÿÜ¢âÉÐ\x000eÂ£\x000b»¹Ë`ÃÐ¤Ã+6nØj¦\x000e/ñy»üæ,p\x0003½Áeø
q?"]£`ó
íØ(\x0013¡
\x000c\x0000¡\x0000(	\x0008xæiÛ7¯|2fn\x000c\x000f<.\x000c½Çõô\x001fÿõö\x001fÿõþî÷«ç÷?ÿ~ÿþçÓ`ùR\x001dFUö 	"*Rá\x0002å¨CòôöÅí«çWÏo<¿}õä8 ê\x00015 à\x0000d4= \x000f×jvÑÅ"î#\x000b\x001c\x001a#ò="oè Õ\x0006_mUnÕù\x0010cÒîèÐS\x0000Å\x001eP´?s±ÈU\x0002¬\x0010(µ-\x0002é)»³NA{DÙ\x001eQÉRÞ^\x000f]X\x000f]5\x001azè¶\x001bÖODTzDÅþ\x001aiz\x000fØjåÔ\x001ePä\x0001!çÝ±'\x0000:/|í\x000c
qàa[QN]\x0012©-(»r­§ \x001aM·¹í\x000ePÓ\x0001\x0007\x0016<Îm\x0014ÂÕßE%Ó\x0006ã
\x0017°Þ\x0015XoHQH"\x0000yG.áDHõ\x0006{óÍ\x0003eXXÌË.:³Õc7¶ß\x0007pTU1cFr$¥X\x0000ÕÍ\x0013\x0003\x000eªõ\x0006;B'"\x001a\x0018	Ì)©»ÔÊe+þZ¹5àÈi»üDDi@ì÷J \x0003´sIî\x0011lw#\x0008i Y0gÙjïdjèÛ¤ ª±ó´Z\x0006ëC7P,ØslýgôÐ6úxÒH\x0006Ù\x001dË¼Ì"ÂcÑc\x0001AÔÝ«3·zª MXw\x001abOD4p,Ús,¤ Sá¹)\x0014M³¨÷å"¦!á\x0000	í!ù5Bâýò\x0002É£rìvÆ\x0006Å\x000bDH!rÁùÈe©\x000e¬7Ä\x0011J;d'ºß0=\x0014 YÇ\x0015¨^¸/ÒéU¬òí¶¶Ï©Ãg°Â\x0005pU;t\x0010\x000f×¡)9!)ß¢\x00059aJ?º\x0004°æQô5rõûÿÇÞþz÷ûo\x001fÿñ__=â\x0015®þ+¾úîÿjt\x0017r3w\x0007$µj:Wx
å=÷PÜ^=¿º}Zÿúû^6¬\x001fûõ£Ñú±\Ç¶þ6gY§ö\x001cp[¾szýÔ¯lÖ@ûÿ8.	Bàtxk\x000eiß'\x0002à{\x0000Þh\x0003b^ÌzDpõ\x001f\x000fë	Úne\x0006\x0010z\x0000Áh\x0007È\x001dv °fÌ\x0002@_!2«\x000e\x0001=h\x0004À9ÉEåP¢X"p>é\x000eì\x000f>\x0003z\x0000É\x0008\x0000+Ô§¶\x0003yð	\x0003\x0000M¦±eÚ%)\x0000¹\x0007­.ñ\x0012ç/\x0000\q-àbÑK¼?!o
Àd:°3BE|Äz	4åÌî¢ÞíÖ¤é\x001d¨~ÇHd?Ù\x0018¢zöÛkbÝ\x0004\x0014q¡z
PïqÜ\x001d\x0005;ánÄpgÄf^D«øÌHÏ\x0015Ozi?Ã7GÇâ(u¼úIçâ b}#ÉKS¥e)Ò¯8ö\x001dôc8Ä·\x000b\x000f\x0002»E7ÿvÿgJÝ¿{ÿëý«'¿ÿã¿þ~ÿöçû»O'º°T
¬¸z\x0005\x001e[\x0013\x0005hg{ý¯M47?Ü¾àáR·/_=½}}U\x001d½oo_<¹½ys\x001c\x0016ö°ð\x0002°{D[\\x0018\x0002Ø\x001b9ÒÙÉÈmÐæ°¨EU#©¦\x001d^a¹urKº[n³®÷\x000cX¾å/\x0001\x000b\)àiG¢S_äaºFR	Ë3P\x001eU¸\x0004*tú0\x0018(´Ýa\x0013\x0007\x00178±\x0015/\x0000\x000bJ\x0010¥ô
XR±M\x0015ÐÍÊqg J=ªtÍrYÊ³¹ZLu\x00085ry«®ù\x000cX¹/\x0000\x001båUÍ\x0017'!Ø¡1ëÇ.pµJ\x000f«\h·d\x001e"ÏâòYw+énm|\x000e«\x0002
wj¿]ÎÁ¨ÙÉ´4ÌB[à/`2`t2.áe@r2q\x000b\x0016µ=¨x§F#mN;\x0003×àeÀ%Ü\x000c\x0007A\x0014hÀ\x0007/·kÔ­Ã\x0005\Ìq
n\x0006\ÂÏà\x001c4
®Ub£8XÍÆf\x0005þ\x0019¸\x0006?\x0003.àhPY:o\x0016XÞ³`X\x0013Ôâ¾º]\x0017pvap4à\x0012k\x0013¡Û1D-Qÿ^/Ø¬É?\x0003×àiÀ\x0005\
Ê¹HÎR\x0013¢º~ãZ1{NÁÕ\x000bø\x001aÄåHz»hUH.é1Üå}\x0006®Á×\x000b8\x001bu»\x0016\x0001çVf\x00052	\x001b_kûps¬÷\x0019¸\x0006g\x0003.àmPÉkçA¿ÍlÄ\x001cÛK0º\x001aªãÂÁÛÀ\x000bx\x001b¨\x001ds\x0008^õùBL:Uz;7y\x0006®ÁÛÀ\x000bx\x001bTØ\x00173Ïn½ªõ0\x0004ºt\x0010\x0005\x0007VÆ\x000b°2eÖðjûE 
q¨¨å\x0012A2\x000e\x0017¡d2` :KYeùC	Z\x0008S.`4\\x001c\x001fR9Ræ\x001fþÁ`.<\x0004\x0017.\x0002Î³ªºÕ\x0006OÒÍ8×\x0004Ç¦¨ï9Þïÿúé®i4õN°üx\x0008ÚËØ\x0008à±JYB2@\x000eÉ¶^aÏ\x0002ù9ÂËÀ¿¸ÀA*:1Éë\x000e\x0002n¶`îÁ\x0001­è.rB]("\x0014R;³ñlè\x001c®Ö\x0005\x001cÏÐË\x0018j#eøOåï¤s9LÂß2(ç$w\x001eÂ»\x000c:\x000fÅ¯Ö\x0005ur<Dkç\x0012m\x001e^èhþ¡©jÇ÷¤e\ØW_=ùÛýß{ËµC_¿ûíÃÕ/\x0015Ú×ïß}øpÿá4Xñ\x0002§w¸\x000f+r(ÚjC3	Ó¹|òçÛo½àê¡¯_>{}õMöõ«¯_ßî4¾+.ìqáEpE!r\x0017Yw¬\x0008.yõ\x0003J¥ çà¢\x001e\x0017]\x0004Wâ\x0002ñ¶_^¤*.í$©\x001eÌV¦ç\x001c\¾Çå/«dÑ)©¸Tº×,\x0012QÀÎô\x0005pÅ\x001eW¼\x0000.\x000f\x0002gC´>¦è\x001eÂ²)¾r\x0006¨C\x0002k1\x001aá"»UÖÝÕÍ\x0012Íûë\x0002gðèY`¥KlVÀWQ\x0005©ý©°dÎ`µ;	×ÃT\x0017\x0006-¼æÓÇ'A\x001f®]Cã²èâzRQêklw\x000fIÅðæûï\x001f\x0003\x0001{\x0008h\x0006\x0002°±Ë52Y$/\x001bäÙÈEK\x000cÔc ;\x000cÕ-Í÷¹´ù>Tw¡aHy3^Ç\x0010z\x000cÁ\x000e\x0003¥¥0·B`5ß\x0006Á\x0017Ie¸T¶\x001bL§!Ä\x001eB4àÑ55Õz@õa«)Öm´\x0019ÙÏcH=dx\x001d¤\x0007©bÈËÚuº\x000b®ñ;¦Jöx\x000c¹Çíö\x000bïÃ!åõ,U\x0017M1¸íòÄi\x000c¥ÇPì0h(ÀfÉIÞÜ\x0007Ñ³¯\x0000È\x000cÂá
Ûi\x001b¯\x0011\x0006þøÍ´²n¥\x0015DÈvû\x0000#ÃÙQÜ2
X@TÃÔ*îëa\x0012Ñg\x0017!ÙV\x00188\x000eìH.VËÚ­u'¤7<ÇÒ)çËQ]»Ç\x0018H\x000eìX®.²ÍsâãTX´A$'s³](G´g@\x000c,\x0007v4ç«}¥" ÈíV\x0010ò¾RïÄQN3 \x0006\x0000;`É:jdx®C3°)¾\x0005×\x001e5\x000c\x0006\x0016ì,,«\x0004\x00134\x0010­*o¹\x0013®èqòvÖ	\x0007ëvÖ):º{]ýXÔ³hÕ,ì0\x000c÷\x001aíî5·\x0010x\x0014\x0010A\x001bsÖtwlºÆ\x000cáZ£Ýµ\x0014Û°!\x0010«\x0005CQ£Â9¦uüx\x0010ÃµF»kÍ³ÿ¨Q\x001dç³¤Å\x001dr\x0001¶ûR¦A\x000c×\x001aí®5ó8\x001dÜ\x001d$!\x0005³î\x0004\x001d\x0019\x00006\x0001kMv×º\x001aÓVó\x000b?0-§)8Êr­	LÀ~<\x001aÞ.­\x001dp¨2Ñ]~ Ëk\x00048kw9%ÑvÛ\x0005´'ÄÖ}¾Å×½lë¹qQË
,ñ)§æ\x001bo\x0007Î¶«ß¦·¤\x0007[R\x0019³-!Ð©Ì­Ü	¸\x0004ÚQ-UÞ®\x000b\x0000\x000fZU\x0016ËÛZ·nÞ~|÷ö··W_ÿþîí/¿½=
',m?
rab+b&ZíhÛ£}s{uóâû/½¸úúùË\x0017ß<{q\x001c	õHÈ\x0012	÷\x000eÉVÎ$ð\x0014¢ø!\x00188_aÄ÷H¼) ÿÀe_-
EÕ
+\x0012K\x0018¡\x0011,a¦õ\x0008HÊ&+ehýÓWx
ØÃ¦»±^t(.Ê$_
\-Þàn§õ4Ô#I¦\x001bßB\x0017$!JàG\x001eµÜ"ÄÍ÷Ã\x001eI1EâHÄVJ¥uND%è\x0005É»Ýû³@ºÄ\x000e¶æ\x0004ËK\x0012\x000e{¢½1õHç&Oò±¼î02)xÃçN¬ÿ¼\x0014\x0015\x0010ciP"n6"\x0004\x0005\x0007(h
\x0007ÝSâôE(ictÛù)P\x0006.\x0001S2ñ¤[\x0013çM(èUq{\x000eù)H\x0006;\x000c¦ØÇ"
<\x00159¾\x0015\x0008äU(Áôªä\x0001J6õºRÎ`dA9ñºª·%¥aÉíö9OC\x0019,1bb=,\x000e¤g\x0019üÅ\x000còvY\x001dÈí1«'@ÁÁ\x0016£©-æéö¾\x001d0@\x001d´D°¶_²#\x000e\x0018M-1\x0016îX\x0016ãößÖx.\x000fhö¥I¦¡\x000c\x0018M-1y\x0019æYOk0²dÔ£µ=ié\x0014\x0018Cl¦ÁI]õµÜ÷Fø\x000b\x0012¯Þpò»rVÓH\x0006>AS>áû^\x0014JTD
\x0018Ý
eW¿j\x001aÊ\x0010 iB.­V8fuXÖØ7ìÎH2p#r#ÁR\x000f¸@IúP\x000fSBmO'A\x0019\x00144R°\x0015J\x0006î½kÆk½+¶fx`y4ey,E\x001aÄYbùZ\x00115pL©^úäÑä\x0007¨ËMa\x0002âDä\x001bS6µÄ4<<¦(z\x0018Xo½\x0014[ÛÛ³Û÷2Ð<ÙÒ|ZæØ.PÜb\x0017(9*ÍíÇS \x000c4O¦4\x0015['\x0008"Eu½jÀ"w%ãîHi(c\x001aÒêkpØ×\x000bkÆðûî\x0002%©)Î.ÞëÉëÔÑsNEÞÈé¤j\x0015L#z\x001a¸L¹\x001e\x0000IÝÂI&í£0¶ç\b y2¥y\x0016ó¼\x0004²\x0012t\x0011Ù\x001bíÛÈaWíu\x001aÊ@ódKó.Hqü\x0012X5\x0011©øgõGK\x0018\x0003Ç)Ç\x0003÷x-(\x0008Övó¢³q0ï\x0014\x0004dàx2åxÈY^\x001døû_(=AA¡ì\x0011ÎBñ\x0003Ç{S\x0007ò­\x0016¹îGq!±8Uæ)`\x001fö\x0003Ç{S\x0007\x001etÑL\x0017ËÉµy\x0003ÕEÖ>ÐlëDúã½)ÇCQ,¥xà
Zº=r|Ù®ê=\x0005É@ñÞâ¡z[º)¡\x0008/ò\x0005ñd»ªô\x0014(ãS£)Å\x0003k\x00146§¤\x0015,z)ÞJñb~'A\x0019(ÞR|u|EQ\x0018i\x001dD¯¾^\x001aK¿Ë\x000f4ïMiÞ¥Âíì\x000b\x0012®\x0015$¨Ã%nJp\x0004e yoJó.ô@W( 1
»ó¤P,ó\x0012~`zoÊô.Fõ½ê¹6ªé^ú´;ºk\x0016J\x0018ø1ò#\x000f~\x0017ª¯±êB$\x001eÊÝ ìÎa¨\x001b*píû5|\x001aânmy¯ãHR^¹Pµ;c¦~qì%\x0004ÄÍç_,½1ÕÅ©¼\x000fºE}°ÆûÙYî\x0011¥{T\x0019Ìvx¸5I\x0010Æ@²(5lÕ\x0011Ø\x0014{8©ú\x0000\x0017¹èCBLä¢¿ÄWUíN´Þ¢["6R
Z^wÆô8f\x000f²1\x001aîo1×ú\x0004çUÒçÕXÎÎ!·¡ö..Gýý¡\x001b°ñôý?þß»ÿê\x0011"Ø{\x0003îSc¼S¬u!B8"±þôÕí\x000fÿ\\x000e{\x0000=\x00084\x0006Áel¾8èÚJ|nîï£!P\x000fl!\x0000"«,\x0010jôâ$<F¯û°?\x0015òÑ\x0018|ÁÛcp!¸ëLAÉ\x0010ñØÀG\x0008=`\x000b\x0002YN-7\x0010üTÔR`ÒÎÎeë6û\x0010{\x0008Ñx\x001f\x0008DÈ£îÃ¢Ä²ì\x0003tUÝÝÇH=d¼\x000fx\x0000Q²hõ\x000bIouÜõ¹\x001e\x000f"÷ ²ñNTÇ1uå>u³|Ð[\x001d÷\x0012\x0007Qz\x0010Åx'¼Î;äx~\x0015C×za\x0016\x001d<2Ìèq :È\x0003Ï9ã­¨.USî\x000c´õu§ÕÀúí)\x0014#[\x001bÓ5Õ(±y¹ÕIÌ×ây\x0004\x0019Ë\x0014Ò±ù\x0015Ä05\x0018³u
Ïe¦\x001c*­$\x0000=L\x0002s\x0010\x0006¢\x0003c¦#/-Ó\x0015Bu8äÁ\x001aqµ°ÅÆ8Á@\x0013`Ì\x0013, ¢\x0002jQ\x0006f\x0010\x000bÜvÛÏ\x0014ÁÂ±e\x0010â81\x0008O\x0002ÃâÈ£GXKØyâÝ\/Ë\x0019/\x000f±\x0014s,X\x0001è\x0015qQ$ýzÑÉÀ\x0019\x000cõÿüø×Á\x001d¬ÿû«¿\x001a\x001bÝ"c=f\x001c± luMn{À¥¡ì\x0000\x0005\x000fó,¯g¯|\x0001¤L\x000eô|åÝºó	&ÿì®8ó\x0003\x0006,<ÕÀP\x0006Ñg%Ç=
L8Ó+æ8ýA£ï\x0017ï>¾¿ÿ\x001fßÜýýì\x001b*­^I8¨\Õ+ÙµÁ/^~ÿªb¹ùö\x00118°ÇÖ8\x0000¥Ö±â(ª\x001fRP\x001f1ìz&38¨ÇAÖ8X P2	!ÊØH®àÐ\x0010¬`ø\x001e·Q#ÀVä\x0018hMXcfB"ÀMÙóY\x001c¡Ç\x0011¬qTOÝ\x000b!òð\x0011Ù 2!Ýº­\x0019\x001c±Ç\x0011­qEò¯%¨P¦deT\x0002n·®f\x0006Fêa$k\x0018Ù©²l¢>LÉ­×|ÏyÁ{\x001cÙ\x001aG¢äT9¯¡`öYOUÞM¶ÍÀ(=b¾\x001d$u\x0002<0Yú\x00141'©\x000ebe§=
ÀÑæñÐ¢hxÍã5\x0008j®@îGÔ ¥ælnNç9ªÓÞK×~Ý\x0011/v7ìOß\x00012Ð9óyõ¨ZEv¨QíuÒ\x001dÚ_3ndxaàs0'ô\x0002RÄ\x001c¸\Vòê9;Ý\x0011·;\x0007z\x0006ÈÀè`Né\x0005¹|pßÂ\x0001d¦}Ú#;\x0003d t0çtÎª7]ø6Øº\x0002ÑÜ¯4\x00022p:X:×6Iæ\x0001Z}ù\x0002¤ \x0012ÇF8\x0006R\x0007sV/"\x0013Æ\x001b\x0002*g³([Ô
\x0001+\x001a\x0019X\x001d¬i\x001d\x0000dÄj5O´\x0000èUçÑF8\x0006Z\x0007k^\x0007|Ó/D'S¯¹¾TÝú¿	 8ð:Zó:ÔV¯Ãµ±¨ÜVõ­üE\x001cx\x001d­y\x001dÀ7ÉØº#¬¾%¯³ '+O\x000b\x0007:Dk:\x0004(ú \x0005øÑ¼\x0001ÊxNÛ\x0019yZ8°\x0008Z³\x0008dã	ÖD·Þ\x0011¢Í\x0019\x000c³@\x0006ëÖÖáýqð¬¢ÍÔ$Bh<@Þ\x0008Ç`|ÑÚørÃHDÁ\x0001|ÈZ;¢TùT\x001cÞÈ?ÁÁú¢µõ%\x000fÜ«»\x0000iµ\x0000K¶\x0017´\x0001É\x0019Ýu\x001a\x0016Y\x001b-JN\x0012¤Õ¥JëËH\x0010!ÖÀ*¦F@`¬COxÝ\x0011\x00121~bA\x001b\x0001»o3@Æä¢µõ%n\x000eMmGÒÚQQ=\x0014Ø/\x001c\x00012\x0004#d\x001dP\x0002\x0019úÀêÄ2*ß¡ÅhAÞmm\x00012Ð\x0008YÓ\x0008¿\x001e¶)S\x0015\x0008h>®\x0001;äÝªÑ\x0019 C0BÖÁ\x0008\x000f¹A¹ì>J¥I\x0005"ÝàÕ´ªhàC²æC.ão)__+\x0015FÚmM1Ð!YÓaý[÷©¬W½ò¡à@«à\x00066$k6¬Ña]wÛ\x000eôê\x0010wr5 ¾\x0018]\x0010?Ä"Þ:\x0016ñäÔ?IÜ4"\x001bBZí\x0000»\x0005ï38\x0006V÷Ö¬î³ª>øXHR¤¯êvU(g`\x000cî­9Ý\x0007'³>UK\x0014ÐÖê>¼Õ±\x001a(Ý[SzpNzA}¨Ò;^«Ê\
ñÁÐÑ}:Ø+$-\x0007E_\x000c+\x0019ùX~`toÍèÁùk¹\x001e\x0018UÜÔ£Pð%mÏØÄ1\x0010º·&tÏªØ$@´\x0016¨Þs©j¯Û*ò\x0003¡{kB\x000f.sÒÃNHwd{DØ,Ò½5¥µ2\x0007\x001e©\x0014\x001d3d\x0003\x0019\x000cî­9½r$®yº£$ê$\x001dÝÒ	 aàô`Íé\x0001QÔMY\x0019[Ë0ëÓ\x001dAgd}Ã@êÁÔ£Õ.{ åÁª\x001d-ic­ñûætÀY \x0003­\x0007kZçq¯¡%Ox4ªê2\x0007Ô\x001d±;Z\x0003¯\x0007s^ÕÍªÇIz(êHuY\x0016­\x001cø0VÐóa=OE¬VÐ!íä=dG¶\x0014Ì\x0000Yê.ËîÌ]øò¾ãS$)\x0013 rÝë>Ñ#
ðÏw¿Ü}¨«Úv~\x0002Ææ\x0000k\x0001£\x001d\x001e\x0006ÑàT\x0017åoJÚkävõf§JÿººÒ¥øïîK­þ[;ûWDóY^IÚ»\x0015?òFiÛ\x0001éæé{F.ËãÖdó­Ix-5ug¼êo\x0004-Ø2»û]\x0015¶Þþ¿\x001a_\x0017_¤zgX	\x0016\x00195Ö2Ë¨<<cT.pùÉKOÙk
HÓ\x0011°Û\x0014=we@eTMà\x000b¼2ôm¦\x000bØfBU\x000cdwx\x0015o­ÖW í)v³\x000f¥\x000fñ`°ÇÃU\ò]ÿ\x0005:Ó@5êª`\x0005\x0007Òg\x0016:ÙÃá¾{©Dea1­Y)¢\x0018ê2"O¤Ï¶.À8Ø\x0001h×Ç_,­Ó\x000fóüÆf¶øÌµ\x0017°n¬@ _²\x0017kÌoôôX=µ\x0007Ö­zjæÖÍ7îÔ¤«0O\x0011\x0015+Îº}Ú
.þÀ!Î¬!ÇÚ<úáê{^Ø§ß?\x0007¢GÓ¯±s1©ë`P/Ó~Ëßë«ïù÷7ÏÿùT©\x0001
öPÐ\x001eJf²ÔÚBÖbtV\x0014ÔÊÎÝ\x001e9,Ôc¡\x000blç\x000c_Û\x0016¯:õögÝÝX`\x000eï±ø\x000b`	ò6\I²He\x000e«\x0005ké0\x001a±Ðc	öX\x0008$Á\x0014°ÂjF<E;\x0005h7	;%öXâ\x0005°¬=Ë\x0018r¶EK¿ÂîË\x001cÔCIæP\x0017C×l\x000b°¶þ¹ýß\x0019,¹Ç/²-)¬ÛÒf\x0001±ÄS^·Åîº\x001eK1Ç\x0012JÐ\x0014\x0018\x0010Å\x0001­íZG\x0004`&°t-)ÌÎ~cXºNºªMV*ÉÚ´µ\x0001\x00033Ò¾=ïóÎ¨ú\x0005'kä\x0001ugÌ\x000c\x0019\x000cÄ\x000f\x0017`þ\x0018Xt·µÉóàåö;mß¸+ú8e ~¸\x0000ó#q]´JWe9d\x001afF ýì\x0019,\x0003ñÃ%¿pR¶a)R\x0002ÊjÏª\x0001GÚËgÀ\x000cÌ\x000f\x0017 þ²L]U\x0006\x0005­\x000c«\x001cc\x0007f ~¸\x0000÷çxÐ!JªÌE¤Ùèw;
æHf\x0014ÊXÂCï¿!o.Yæê¥bÔ\x0012Ä@»ùÀ£ªóÍñä!*Ó\x001fÖ¨ìÓÕ×ï~ûpõíÝûw\x001f\x001f\x0003ùïîøÏ©zÆYë-2=ÆÅK®ÿv¹øÙûý»òæêëÏ^_}{óêå÷Ç×ýúÑfý:±®?^ç ë\x0017vÌ>ìN=\?õë'õW[Õ¢\^ipt!­ëÏûÑãÜúõJtgh½\x0012çÁH:Ë7/am\x00174­}ÜÍ"\x001fG!\x001a°Þ\x0002ýa\x001d\x0013ýû\x001dËiÞ}úßmõ§@ðÑ«º.®Ê­û\x0017ß°æÍ¿<\x0006\x0003ö\x0018Ð\x000eÓ.\x000eð	ÖªÕUç\x001cvÓws\x0010¨@_æ6ø\x001eÿ¢¶¡\x0012Ëx\x001b\x0002Ïj\x0010þòîÃý¿üíêæí¯¿ßýr"\x0008>ÜäB\x0016Í|¢¬ÚÌ\x000ewõLÿòòõíw¾ºyñôùÍ7ÿ<ã8àÀ\x001e\x0007â\x0000\x0019ïS\x0003À¤Ö(Ké0Ö\x0010nÏ8Íâ \x001e\x0007YâQ¨ºKkåp=_íPAI»}¥³8|Ã[âÀ,\x0003\x000c \x0006Kz®<ÊhE(ûSÖfq\x001eG°ÄQ]¦G	ÂT>\x0004#ú\x001f0Ä\x0011{\x001cÑ\x0012GÑÙ\x0018>ê$¯àä\x0004
Z\x001e«ÔÃH0¢ó¢m\x0003\x0018\x0017I®\x0005\x0006®×ÃgK\x001c¹Ç-·#õXÕk
^
Z\x0005\x0007íwÎâ(=b¹\x001fèdx=\x000fUÙâÜ ¤0\x000cîatýBÎ\x0012FuÐC£rÄ¤·<d\x0019²\x0004\x0005vßÜflnIçhù×s´$2Ô|½æ÷\x0003\x0006:\x0007K>Ï¬tÚÔo/U^1	\x001aX\x0002\x0019ø\x001c,	=FÔ\x000eàA½5¬D\x0008»²\x0004³@\x0006B\x0007KF/\x0014äyªþíE£(ED\x0000\x000c\x0010\x0006F\x0007KJOÔf¹¨¦7V
G.»Õ)³8\x0006F\x0007CJ¯Üí%ëJÓ/¯@X§«e\x0015 îÆ\x001f³8\x0006J\x0007KNO¬ùÔ\x000e\x0016KÂHóIT×\x001dò¾ä÷,\x000bÁ\x000cÞ2±YÕWöÅä¬¸;\x0019}\x0012\x0008\x000e,,yæ`h@\x0002píS3¾E®zönÂfý³úç\x0001È`|ÑÒøæÊíY­²HÄa
£°Èþà¡Ù
\x0019L\x0016Z¬u$:8Vnmõ¹è\x0015Ii7\x0001:\x000bd¸ëhy×sm
¸èd.'±ó(8Ân"z\x0016ÇpÕÑòª\x0017îÏÍöòMj¶PmoÞ-B\x0004BE~V`ÍÆ!|WZ<å!H-\x0010p5½!áá
Y
\x0019\x0001\x001b\x0010rrC<¹\x0000Ùo\x001d\x00052Ü\x00102¼!4áá\x0015aÕ\x0001iº®g\x000cÚc³¯ë×»#R'qø\x000c½!\x0019\x0006\x000e?äÔÐ°Q\x0008\x0018CÝÝ\x0011è³8\x0006.ô\X÷\x0003¸Ô·íÇ¹n\x001b¢&+àîtÔY cfÑ0\x0010a\x0015\x0008©-s©®Ü·\x001b^º®Ás+¡ÕOx\x0013WKßÓl8;®Eç gêr8ÒW:\x000b>CÆp¢fFp¢D£îMÊ»\x00032¦£Ý`jÄk
¦\x0010
Ï×>4-í\x001aóVpyw\x0005]\x001f\x000b\x0007\x0003¯#õ\x0007}\x001dùæÝÏ\x001fï?½¿zzÿîý¯÷¿#ôü\x0002g[©¯ÁEDÚ/{ùäûÛ7¯®Þ¾|õôöùq$¾GâMDÔ\x000cW(YJe¼sI&#£\x0007S$¡G\x0012¬4_8rQ\x0017 ¢ÅÇó}vÓgÄ\x001eH4\x0005RHf,UÇ\x0011D¶:â¹ºÃ¦HR$Ù^\x0013§ÉºÈú®I¯"	»9i$¹G
úïÙ\x0012\x0010¾÷xy}Ctû\x0013\x001egq\x001eG1ÅAÃÄ\x0005G$Mrx_\x0015È~åÌ$CfhfÞ\x0008I,Ò·\oI¶\x001ajéôðÅ\x0014Ê@&`É&\x0008jS­¬î¯z2\x000fªÓÅÏ\x000c»õd³PhB¦PêVdÙ\x0015\x001eê,»\x0012ÞxÜÁ9\x000be F°dÆ°»J²«Ú±Ö\x0006çY\x0007R\x001cÉ°_v=\x000be`F°¤FVä\x0012j¬Ñ®ÌÌà¬V\x0007ùýqK³H\x0006B\x0001KF	<-¸)ÁçÁQ(çKY\x001ehÊÚ,Á\x0012©)æ¸KKl*\x0004CÒ
#3-'à`ÑÔ\x0014C2Þ?¿4÷{L"B\x000ew8§¡\x000cö\x000bMíW
\x000fÕ±'rz¾È9}ð-»Ó~¦¡\x000c\x001eM/=\x0014-hàZ¨å	Dp¡F*û%ð³@;¦w\x001e¹\x001dI^\x0018ëö´Ñ\x0000^e\x0013«3\x0019vëßg\x000cW\x001eM¯<÷ÊÇH+\x0010õñöÛ+gýHìãù\x0016\x0004k8ÿeÅÁÉ±n3ùeßw¿ßý|õêÝÛ\x000fwï9õ¤´\x0016«äê}õ*ú\x0010_Âæ\x0018¿ïß<¹½zõòÅëWß\x001c_=ö«G£ÕGàYz¤PòÂ\x0002GÚ\x0017>¹zêWOV«÷×Z^SX×®-^´ØïÝr±&\x0017ïûÅ{£ÅW\x0007q-:2Õ§r_pË0M®>ô«\x000fVÇ^(\x0000±È\x0008ÎzìõA¡¸Mm±ÉÕÇ~õÑêÛ\x001a\x001e$XÀ<­ÖmJÖL®>õ«OV«GN´:?\x0014\x001dàúí5­»SV6¹úÜ¯>[ £§«ÉY\x0008­­Þ©kAþ«/ýêÕêAÔM\x0000\x0013¸7OòÐÊ]æÁqô°ãZÇÍ»O\x001f	º_ß¿ÿýÓ¿ývÿþÃi\x0010(¨\x0001äEQZFîk35ð\x000eqÓß~ùæûeî×·¯¿ùáÙí«ÞA7 ¡\x001e	Y"©!èÿÇÝÛ-Ç\x001b[Â¯R/p\x0018øÿ¾*RÕjvP¤\x000e\x0014öÜ8J-ºÍ\x00085yL\x001dö\ÍkÌÝ\\x001e¯Ño2Oò!72Q@µ°«ö®¬cbl©ÚöÉµ\x0001d&\x0012kå\x0016`¬p8A+lVÐM@¼êV\x000bæ\x000015\x0010Ã
\x0004z\x0011u\x0006"\x001dvb¤ÛB\x001e^IHBKz\x000e\x0012[#±¬H¬Ïíca\x0018\x0002ÉH`n¸¾\Ò\x001c$®FâX\x0018Û\x0001¥æä\x0013\x001dí®¾\x0000í\x001c$¾FâY(ß\x0000Ã@hªtÞ]Á\x0017$ÝkÃ\x001c ¡\x0006\x00128\x0018\x001frM-ÐDË\x0000\x0004'O\x0013Ø×h$ÖH"+\x0012ëò WB¢\x001dö!Ëd?¹®\x0011Î¼\x0019H6ÍúYy\x0015Jò]\x0016Ï	´\Ú\x000cÅáDÑ¯\x000eÎAÒÆEÖÀh¼ÏÕç0p\x0000ûÛKÑö
}Ú9PÀ(Y#cÊ§(ÆClÉ]\x0019éÆ9ayNç%"Y#Ê\x001f
¥ñÃÕ\x0011ÿQPÜö|§ÛÌw^ß?þö¯Åé:\x0019üÏe\x001b¡èö¤ñø.®Ý9×Br1_¯.\x0013eú'Þ@×\x00084\x0017\x0002\x001d#eñéêíÏ_y¯:-ýXái\x0012\x0004SC0\x0010<**."
%v'\x0008£rI ¸\x001aãàb~W\x0002±Áü\x001cÒ
¸ÑÝIæÚüÀg¾µø\x000c¤=ù\x0005F9G\x0000ü(GÔ\x0014\x0000èíªQ;\x000e\x0004Yû\x0017­ð­"ÝÈ\x0005\x0001£\x0013D\x00004H²y"
6\x0008ÁR«r$¢Óvìb\x0012æ\x0018KÆs\x000c·¤1x
]"ÁF:\x0008RôOÂÐcÉwAcÒã:DM$ð	\x000eF\x0004iFù#&ah\x000e³ä;Í!}ü,\x00076Â\x001c8øh\x001d\·\x001c;\x0015jÎ³â;Ï\x0001´ÈeÆ =©`[
)¨õ+;S1´¹\x0005ß\x000eé\x000eÛ×\x0003RÄ\X³ØZÑáI\x00183­øÎt\x0000þ@1¤m	ÈR ad\x000bBs¤\x0015ã\x0016D\x001a®öXe*WC0ZéQ¦½I\x0018#­ø´\x000fX÷Ê\x0017Ö\x000beH_Y+3ÚÓ9\x0005n´æ;ÒÞuðJá¯2´âsKº9ÒïH{#NBv­^GâkÓÞ£kU~´+b\x0012æHk¾#
\x001fß#\x0006«)ÝÖVÓ:D¶(\x001dêgwrôîÎq²)';]ä°Bk ]K?:
´\x000fbâK8\x0003\x0002ýîì)ß¥oÖ\x000f/ÿq
æþc\x001e´\x000e\x0012QS4JÌ5´\x0014\x001e°³C(Ùs³gWù2}³<¿¼MÒ?úÓ\x001eh\x0006Á\x0006Ï\x0015PZ¼2BúaYDÄ&;\x0011ûÃ±À\x0014_Û÷% þI{wùë}úO-n\x001f~zúéo÷w°Çf¿\x0019iËëvZ\x001eèÈª\x0006Ø3h»-]Ë\x000f«Ë´Ín¯ÏÏ®Î~X-ÞÁV\x001b}1#DªF¤ø\x0011yA}õ!\x001aì}VÑ`Ù\x0003ôp{ùtIócJ[\¥tÍ/É Ý]¶Û>\x001f©!\x0019~H@r*qã	Ê\x001f£v^wZ~>&[c²üR2\x001fr\x000b\x001b@áU=+dº¬pó!¹\x001a;\x000886v\x001e1Ä©¨\x000b¦~'î|L¡Æ\x0014I!9µ*bgCòyeënÎ<\x001fS¬1EvLÂz\x0014\x000cUÐ<ê4>º\x001cd\x000bÝ\x0016½Ù6õ®!6#'wâsÇqÌïÕù<	ì;´¾[þ\x000fª
¸ü\x0011W\x0000Ñs¾ü\x000båé¶\x0013°\x0006\x0003ìÈ½Â|LMÈG¹ÐD'
]DS·`> &ÞJþ\x000bcG¹uKÁÉÊÂ*ÐÃrN±»\x0008ÙD\y\x000bº5èË}$	@=QÊÆn÷Ê|PMÈü1WäNëäõ]+]S\x0003-Sìò~ÎGÔD\y\x000bRIEDIr#Á#ýr¢[J\x000fÊ7 <ÿ2é\x0000:C°Ré\x0010ÑmÖ{|ÅP¾Ïû;\x001fTGÈ#$\x0012	Iv{*ýc\x001cFN+%ÈË®ÈÍ|PM"!IhAÕ8©n·Ôì\x000f\x001eÜ TI(þL\x0002Ä\x0008ópI
º\x0016¸U°ÒSÔå?SªÉ$Ô\x00112	ECýJ\x001aEéGJ>¨á±\x001f)Õ^Þù3	\x0011\x0005ªFÂh\x001c½ø\x0007MCfÎò_\x000bUM¨#d\x0013Ò 	$0ùà\x000b´×t úãñó!5¹âÏ%DØ¸¾ 	ëD³òÎu».çjr	u\B8êÕ^¡\x0010»¼\x000fWÊugÐæjÒ	ÅN\x0008y¬óTÒ\x000fªø½>\x0005Þ|DM.¡Øs	\x001daä\x0011)Ò×¢\x0015.S_\x0018d>¨&Pü¹\x0004Ü82õ\x0012)9·tãÀr¿ê÷cÏÇÔ¤\x0012=Ð1E¥Lg¯Tô\x0018ãÆ\x0008\x0015úO\x0018³Aé&ÐGH%,\x001a¹vH\x00182YI»Owé»çjR	ÍJ¤LÁÐk>Èj;êÐ!
(øæºÉ%ô\x0011r	àÒË `\x0002\x0011Óso©Îçù\x0013YÝ>\x0004°§\x0012:ôtö}Ú)ªÇÚï*ên\x001bÒ|PM2¡L¤{T.ÈBË\x0005½\x0005xMìT¾Ïe<\x001fTLhödB(Ê
JHvL\x001dVê\x0008\x0019n	}dBäFÐtß=ÁbKòç¸JýFÄù\Bóç\x0012!åãF[\x0019+p6\x0019\x0008«,5IwÙ§çjr	ÍK¤\x0004ÉRß »+%i(ôû-çj	ÍL\x0004½i¤\x000eD\x001e¬,pfæ:Âëi	ÃLè\x0018,¾*¥])a×PJÔ»äCó15¹áÏ%<=ci(w\x000e£eé2åµ1M.aØs	\x001d¡w?×ZRZDzÖ
ÍÁ8vßgÚ\x0017xö°«75Ä\x0004\x000be¨3>PzÎ_k1M2ì\x0011*Ý94¨´ÓhjÚö\x0010»\x0012ZóA5\x000eÝð;ô®¹9ðj Çç@¢ë\x0012ÀÏÆd\x001b×gù]_HC|»±)Ð\x001aËdIWU}>¨ÆMX~7\x0001äã\x001egM 
\x0014}_:i\x0008*ð7TÙÆOX~?\x0011¤¥\x0017\x0001r$<RÆ[[Æ7øWªñ\x0013ßOøhË<G
Âx¦¡¹,©ùH¶ñ\x0013ßOø\x0010éÆkci0\x0006\x001b&´´]¶ÌÙ \ã(\x001c¿£ð¡)\x0007\x000fn¸RHU\x0000\x0013\x001fü\x001a?áøý÷\x001a${rs¯\x0007ìÜ.^0AÓ57¨ÆO8~?á£k<(ª\x0011&\x0011iª¿éÚö·#¸	ãP.J9ï¨4\x0005/MPü^¡þò÷×õËýsSý\x000eã~Ã\x0006O\x0017¨3à¥>zJlm©á
mÝ8UZø½P[\x0012\x000cè5X¨uåÀð_®tü\x001d¶x\x0004l:(wB¹£ÚI¹-åNÿÞh¶¡\x0019s\x000chÑ¢°C!h ÉYäéS!ð¿Xµ\x000cù´\x001daC\x0002\x001cª3F¡éÍ4:\x001cÿ'ü\x000eZ8Êa³\x0006i\x0015h\x0019¬µÇRkïÊq\x001cpçÿÝ<Æ²¥\x001bW\x0019OS^Òas¾Ü(ûÌ¤\x0007¼¡þå¥Y4ÿÝ\x000bÿAÓ´d\x000bC³TuO¸ø[»Õ_~\x0017×\x0011ÔR\x001eLAMøÒáMté¤u\x0007l\x000f(\x0002ün;\x001eã¤é`À\\x0007H®\x0010iºb\x001aË^^\x0013n\x001b;\x0004ZijÌ\x00170cÃHÔI¬Ù¥öqë }ä¯\x001dL"\x000e)÷gGU6Åê'TßBõwþBÛàæsõ0E3tFÇsì©cÂµÞÂµæw÷\x0008\x0006TfÿÊUQâ\x000fÇ(_m·|\x0007¿_Ôvho\x000e ï\x001b÷b´E\x000f¤uÙ¼7@o\x0006Ñ{Þþí5ü0 ã+´Ò B%\x0002\x0004¬X¢¥qÔ\x000eº­ßáóö»ôûùêz'jÎ\x0005y] è¡ì9@\x0000é¬a&­%\x0008ºKÇ1\x0019B»\x0008|« #>Ê¥/²u«@mr\x00179ò\x0004\x0008ª ø6$^ãh<9AÐ$Ë¢L/W\x000cA7\x00104\x001f\Ó¨î P'°TÝ\x000cu2\x0004Ó@0Ç\x0019'\x000cP)lfÕí\x0000À6\x0008,\x001f2]c\x001cõiÐ/!\x0008m\x0011\\x0003ÁñApÈK \x0004äÈO\x0010¨õ_ÂØç|\x0008Êû¿\x0008/u
ôÃw¨Sòé~qýðóãÀ\x0010wþ»ß½_Ã}Ê}Ëj£Ái\x0012âÂz,{\x0007\x001b»)ñ O°Z\¿½ü:OBc´ªV\x0007\x001am:1:[í\x001d²1	g°&A\x0019×îØÛjS[m\x000eµZKìé\x000c\x000e¤T¶:à(z²ºë.§Yíj«ÝÿÃV\x000f\x0007Qª-*ÇôCµC>¯\x0017g\x000f/÷³§×OÏO/w\x000f?ýmýú2·ØB\x0016\x0016\x000c¼H\x001a( Q¡0ÊìÐ\,\x0017gç·«ÅÙÕÝë«ÛÅ»ó³\x001fw·»ñé\x001a>\x001a>ä\x000b\x0007|\x001eýòÆ\x0015|£¢»à35>s4|\x0006w£L×(TGNø(å\x0010n´é\x0010|¶Æg\x000fFÈ0R1ó²B1Bø~ >WãsG[¿¡[&kz	z;ö iñõù8\x000eÅçk|þhëÚXáw¬±	Û¸vä\x0001ØB-\x001c
D-\x001a
ª4¥'DÌt7K;\x0014^¬áÅ£Áó¤©]7fÞ,zs}êõÃðmnÉRmØO\x0000ÐÐ¥YHüÞýÙí\x001a:\x0014lðÉ£áøà<¨ìYM¯6è(Ýë!\x0000ÜE\x001e-yI;Ôà	LkiË|1@Ù×Ð8\x0010`¼È£e/F\x0011\x0001UÊ*¡k4¯`É^dWöçPMö"¾\x0018AéYÚe\úFA\x000fåX+Ø¤/òhù±t+1>Ôz_ò\x0017±ë¶0\x001b`¿È£%0F\x0013Å\x0016¶¼Ö:Oba\lñ\x0000M\x0002#Á¤Ð\x0014OZ\x0004¢:ñÔ²\x0000\x001eí\x000c6Y<Z\x001ac\x001c]!ÞmIS\x0004Ðr¦\x001e\x0002°ÉcäÑ\x0012\x0019«üX´ÚÅ\x0007r2Þ\x001d)ÇVM"£È¤-êQ\x0015Ñë2¤ãm\x0011<=\x0017UM&£ÉX[\x0004]a¢\x0019Ï`Ð$ÁÖçP:\x0014`[9Z&c7µ6k<°äfF\x001fÉª&QGËd\x0012*AB¶¾PÁPÕ,mÑ#Ý%TÈ¨£%2ÐoNÔlîñ¡hÂö_\x001d\x000e\x0005Ø$2êhLºâJÜ¡Ú0\x0018¨òÑN`Ç¨£å1\x0016IdÂ²Ù¤YEwxóP|M\x001a£Æä¤\x000cPÃ^Íë·\x00018Ê*~\x0008À&QGKc ÙbÀ70y`¡\x0018øÓE©Kat(¾&QGËb\x001c\x000en%|¦}Ä>ÝïX\x001eT7I>R\x0012£cÔäAü\x0016É,]Ù ¡Ïf9\x0017 q[ÄØé\x0007z@üñ~ý¸ø1\x0019ýÛ¹bPÐÅç¥F\x0011F
½gùî§á5´èÇÕòrñcúm5¢ûE\x0010T
A±A\x0000AOTM\x000eB`f©uXB2ý³É\x0010t
A³A0¢4pz%±H¤Ai\x0004Waô~:	©\x0011\x0018>\x0004ÊQèõÊb\x001f»V\x0014vÝ·ôÉ\x0010l
Á2BÈT+½6X\x0006Ñ*\x0012%v£G ø\x001açÒ:«`¨YVÃ|\x0004Bð£\x000ex\x0012PC\x0008|\x0010Å1\x0016é;7÷hLá|û(Ö\x0008"ã"\x0004¤¿K\x00101ÍÖ `\x0010FT'BØ<B\x000cQAða\x0008J\x001eº®óYÐ(5Lês2&,HÆ¸ õÌÙVúâ'2ï$£i Ênõ6ÖÖ_^û\x0018¸ \x0019\x00037(&"½7òkmR\x000c\x0017¸Ö¡\x000c/4X|þ\x0008Ð\x00063\x0011Z\x0004¶³à\x001aû\x001d£ý¥,\x0010ôÀõ1@ \x000cÉôçF&Ch|ªäsª\x0016Õ4 ?!jãhðÅ¸Ñòþ$\x0000K|>ÕÂ¬&ª\x0008ôÖPsC\x000cí\x001c¨Æ§*>j}iî¼\x000eÄ4òk[Ö!x'ahn\x000bïº`§ \x0002Z\x001bEê\x0006\x0005\x0013Æ§*>
ºóÑP\x0006GÓR	CmÁ³­Cª*¾\Õê \x0003L:ÜªÜ``;\x000fM®ªøÕä7QM )ÓKù\x001fM­	¶<I5~I1ú%\x0010NÀó\x0010#Î:i\x0013 \x001c\x0018A7gZ3é?îþÜÈa#\x00119\x000e(@§¨K¨Ë\x0005`ma\x000fS¨ãªf(¹
%¹YN(Ú¢õÈ$RWª\x0007¤xÈub3c5ß-¢Dmï-6÷hí\x000c-Geú%âw\x001bKñ®"Ý¸PJïppå.ÁV¡ù\x001d\x0014^$ài\x0017aSÜZ\x001fÙ¶Vtå\x001d<ÕtºcÐ\x0005Õr\x0005qñ»ÎzÐu:\x0019\x0011\x000bg\x0006kæ\x001aºJáìàõPÂ¶\x0005Øô\x0003\x0015`ß¬\x001f~zMVÎ4?ý·
\x0013\x0014Ô¼\x001e,e \x00169V\x0012_^¾½ºK?î¶^×Ök&ë'á#i<Qà(,¦t9*&Zojë
õf°`ò(
\x0006qÔ.\x0019-M°ÞÖÖ[&ë£(Ìâ1\x0014ù@O÷!ß'Ph½«­wLÖÃû\x000f~{MÃc*
T¢VÉòXïkë=õ
HK\x001cRæZì\x000b×Ã\x0005\x001e)sÕh7ÎþÖÚúÀôí­@}Ðtj#
\\x0000v¡:\x001amÚßúX[\x001f¾½òDÔ¤´ û§(ÄÒ¡Ïð6ÍúMuX
\x0007ëãÓ´RÚ9e'jRò£\x0015½	Ö7ÑJr+kN\x0004¬Ge¤"ÞçMIj¢õ¿\\x000eß)LÞõ\x0011_kÓ·§W6o­l\¦äòN\x0016%\x0013K\x0015y0_\x0015óG\x001bXv\x001fü¶´qÛ/\x000fëÇÇûÙZ22×â­÷ôTî\x0003X\x0008\x0006âþÑÇÿÅåååX¢Fæ«Ú|Åe¾v¨%m\x0010Å~G¥øäÆgIö·_×ök.û-¥C¬°ÁRËR?Ub4åb¿©í7lÛ§	Z_êðÒ¶pZñîýí·µýË~gQ; yÎb¿\x0012ô\x00165¬\x0004ý®¶ß±}<¼É\x000b9Ü<<gJâ¸\x000e¯¯÷\Æ\x0006\x0000~|å@î`øø.*r<W`~¨Í\x000flgW\x0011Õ\x0015p*\x001bd ÖZó\x001a\x001fþßßþXÛ\x001fÙ>¿"¾áó[lrùóWä;~ó¢Ïðý\x001d6æÁÑEÏ\x0013\x001fNÆ\x001d\x0003Øûß\x0006^¶È\x001bâÆ¯/O<î}ªÂÓ8ùMàl×	\x0014(6\x000f\x0018§OIOZ\x0006.ë°+ÙânÜÄ]i¨©H\x0019`^rmþ&îJ¶Àë\x0005½
ÀáEª\x001a%+kû7WrE^#\x001c<¤¯§:º²jaÊÜd\x0013y%[èMÑ\x000b§¬´º)EEÎ´R\x0007Ù/É\x0016¿@Ý
·T5@Z\x0001®\x0000 \x0000 Ø\x0002@:Ä\x0014À\x0015Ïn\x001fb×å
 	\x0001+\x0004¤ô­~ù2áZì\x001f¨E\x0000´·/® \x0000\x001d²0\x0001°\x0014Ä\x0002½Éñ\x001eß)ö7a@q\x0001Ð\x000bÃö\x0015c-Ñ÷mÚ\x001a¥äÂª	\x0003+\x000c"\x0003TqX¸ÒZP\x001f\a@5a@±\x0001ë\x000b\x000fRÂ¢ñÍKYc+SM\x0018P\aÀXYè\x0013ÓqÔ\x0019Kq"vXO\x0001Ð\Â\x0014×-Ìx
S;©IR	E\x001bÊåD_Çb*&)®8fl$¾\x0014#CéM¦X\x0011¸ps\x000bS\×0 >
ÈT\x0000\x0003Fxma"êLN\x0004 0¬¹Â0P%Z¢2'hQþ\x001cÈßxìo¢°fÂ<\x0008&°\x0017V;¢L\x0014+
ë&
k¶(ì\x000fÕÁP!B[z:\x0012}uú©\x0000(¦Ù¢X(\x0002&Àx
Õº°­\x0018ÁäBu«7\x0017ú\x001eXNr.Hè´"\x001e\x001d©¥70\x0001äbLwÊm\x0018ÒðÁ%\x0010tµ¤xü(]î¹\x001cªt¿á\x0018a\x0004]`H¢¨ºU®g;\x0008Þ&dFÛ0RvÄ·©Ì_(äyIÑ-\x0012M\x001cY¢þ\x000e\x0007ã®2ÆÕØ\x0018\x0012ÕrU;ø]÷/ÊJ\x000e`x)ûÈUoô·H\x0015\x000b\x00195½É\x001d´^\x0013Þ:¶WqCi/Ë\x00194yàñ*qüÁrÒJ¬ÛXóUÞi%³rTx÷ôèÄuï­ÖI®Â/L%ì¥\x0014\x001aÞ%ä{y%úb\x0019ûâ°ÛÖv3iý.\x0019ù4w*\x001eN\x0000\x000e\x001cx\x0015èÖRÁÒâ×X\x0000Ûß¥ß®F&ÄíöxµÝW\x001ff·Ó(\x0002ìV4\x0004.;49Z±Ø×l]­9ÌÇU4[[ì\x000eÒ&\x0011R7\x001a÷µÛÔv\x001b\x0016»\x000bK×æM(\x0013Ô£,Çûmk³-ÙåyÀÆ-\x001d¥ãÑâô¾v»ÚnÇaw°tñôò`VÆ½ý¨gÜ×n_ÛíYìN	\x001a6\x000cCË*Í82ã\x001d8¾w¨í\x000e\x001cvÇa\x0016ìÎ\x0002È):QûL²ÃÄÚîÈb·¦Ç;oI7,]\x0018©Ñsè9?ØîÍ»¯­&¹\x000f2Ü	\x000fÚ\x0000Ùpl3ÚôÝ±ö5¼
\x001cñÒ	qBv["Ã°Ð\x001dvÕxö5»#\:Y\x001e¹¼-ÏÖl¾÷(½Ö¾7ñRr\x0004L'\x00051¸ú$-5\x0005\x001dGõ}
o\x0002¦ä\x000e\x0001Ð;R\x001aÓÖR+ª\x001e{TÜ×ì&`Jé(\x0007ÓÊlòe£4\x0011SrLÐn¦¡\x001bÒ\x000eO\x000c\x001f­\x0013ìkx\x00132%GÌt*RûOî\x001cÇ·¬SÎbå}_Ã)9¦WÏX¶
\x0005M\x0017bÙ*\x000cI¡l¦ä\x000e^\x000b@ÄSÒFA¼\x000frt\x0012sOÃU\x00135\x0015KÔ\x0004½I¼=øâ:Épºô\x0000I\x001dáMÔT,QÓ¡FrÚâ\x00016
Øí Îs}]ùç)v·L°B¥bÈ©8Qø5F»öµ»%j\x0006IÌü!\x0005P+\x0012N+²[sÜ{T\x00135\x0015KÔL÷Lò\x0000+WÈ«&j*¨\x0019K\x0015%¨ÂTç¬+#¸]\x0001Î)7QS±DÍ°áÌÈ\x0003Ú\x0019JQ\x001a}èØ×ê&d*	%\x0008¼\x001e\x0007\x001d\x001a\x001eúÊ(ýèláëÆk\x000e\x0007\x000e4Î%ljWÆ
\x0019}#Þ×ðÆ\x0011j\x000eGèÓý\x0001[ÔaÆ\x001c{Ì\x000fäPà&q¸áCÑ\x001c\x000e\x0005®óróÅñ\Êé3dº9ã`z\x001fK¡\x0010øÎòNI-
wì½Sê\x0007
Ü-ôBqà	$L\x0001\x001e\x0011\x0007	Ýf¿tU¿'EÎmóçe1?%±xÍ\x000fÒsj49\x0018Mc~÷í
Ó·÷:Q|´Ô\x0014ímÉZ`¸|ªßí\x001dÅ´w [Ôô\ngrtzyïâç¶ùÇz\x000b|AHgJKº\x0015å\x0006í\x000fJÒÙrN?T¢§O¯Ï??ýüx?Óz¥±Y\x0018\x0004iCM\x0003À4\x0008æÔø\x0010êjqzuwýöêíåj7\x0006UcP|\x0018¤¡9Ú©Ø\x0003äÔ	çìnÐ)\x0018LÁ°aÑ#Ý8HHâë®*é.ðOÂàj\x000c\x0011&\x0002\x000b²ù|\x000bQÑSævrÞOÀ\x0010j\x000c\x000fCòEÂ ;A\x0008n$~Ü\x0017M°)³\x000fGZðaÐþ\x0004'µÊ\x0007²Axbâ\x000cË Ã[Ò\x0001ÜÒÙßîyx\x001cÞØ\x0001ÆÇûçûõë?æ\x0001±&åýS$\x0019\x001fqP e\x0012\x001a9ÜGæÏ~X½;¿\x001cÞÚ\x0001Íéêzµ¼ûÓn<ªÆ£¾}<ºÆ£¿}<¦Æc¸ñH\x001d±\x0002ºÐ<â\x0011ø,(e!v.\x001e[ã±ßîúDi[\x0000\x0003µ?\x0000õ÷÷/ ðáþñe¦oÓð$d[)\x001e\x001a\x0015:Iú¶éQt»\x000b$\x0010>x¿º\x0005é\x000f«ËÛ\x0011/G¨TJý» Ò5*ýï*Äf\x0007Â_ùqyåÃ±:ñ `<Tÿ¤ÖõÊsqÉ­=8ü\x001fX4ù
3\x0001+PQV\x0008LÅ^p\x001a00}"\x000e÷b¨\x0017Â\x000f§éïùàÝÓëgõºø\x0001åQv	Î§ÿúw¿¤ÿ?4ø\x000fÔä\x0008­õ4e\x0002¼»9£³Av9áÞ]Ý]\x0000¦»EW\x0016¥\x0001\x0012\x001a \x0019²
U-Òö¢\x0016
"R®%Ú(º©éT tU®W\x0005~áÅ\x0013ÁÆ\x0002\x0003LæßIh|ÀuQ]ç°\x0007|É[1	ô³ñêüþáþù9¥ÚÏO_¾<}¾{fÒ\x0002\x0018ä^ð\g<Î	b£d\x001eïÏW××)ã¾¾º¹¹ºXÝy\x0002Â£j<\x001brÔ\x0001/Õ8Þ\x001dh¸XùÑF9pt
GsÃ\x0001%Dã\x0004*j³ÁêL?\x0006ÍÅcj<\x001bO¡úN»Íàh!~
bì:\x0007­ñXn<¡(6;ïi\x0008ÍÑ\x0010 nìi~\x000e\x001cWÃqìÞÀRW3Èµ$.C\x0015F\x001fbçàñ5\x001eÏ\x0007\x0018zQ¯Á\x0001E&â	TÒIa¬®?\x0007O¨ñ\x0004vwà¨Ü%\x00008q§hf3å7Üpb
'r/áý¼:á\x0004é\ðtzô¨\x0002Â\x000c8UkhÜÐ82.?Ñ\x001a'"/\x0001D\x001fZ\x001eæÕmjÀ\x001b¤­¨x	KÁÇ¤7®Ïx?É\x001c@Mn Ù\x0003ç¨ÉÑ+ºÒA F\x0005úæài\x0003É\x001dX-K/(\x0005\x0006ö\x0019.Ð(è\x001c@Mv ÙÓ\x0003ï\x001bÞ¹J£\x001aSÁ=^@Mz ¹ó\x0003«\x000bÝ
z\x0012\x0015Ò4«Í¨Îì\x001c@M Ù3tí!\x0017ç\x0005Ñ\x000fiO\x0004PéæÀ!È&Cì)1eTHú\x00132<¦èüÙÑ9\x0014A²ç\x0008QR\x000bó\x0001Ñ!\!î+j¢ªbªÁÒ\x0019r.\x0012a vô>ª\x0005·ÛVí\x0015;\x000cYPÍx 
}0ôâ®F{eæài¼¶âöÚViÒvÑÀ}u\x0000$Kgµ\x001e¥$\x0003¨qrÛÉYxxÀ°*èj\x0014u\x0003ÁabÆÓ¸\x0004Åí\x0012lºuÓT°(TN\x0010Ô¹X\x0001éÆ%hn`.Ê¦)ñ!Ý1SD~Í¨8ë\x001c@KÐì.Á2×,MQ)²Âª\x0019}ô'4
E9W "Fß­7õ+O*RÐF¾û\x0002Þ`z\x0004\\x0002r2.K\x0003ÆÚÆ¨*YNÀõQ8ÝO,íîû/·ÏëÇÌ\x0007K\x0008 `"ÝáÝDË÷<\x0011ó­HÚôÇw¸XÝ,Þ^//3'@úg#¤\x0000\x0005ª(^ &§>	"Zí\x0004Ä\x0011\x0012Ù\x001dÓD×H4÷XUDjZ\x0012YÖ¤·¿f!±5\x0012Ë$\x0016$9\x001d\x0005$ª éeo3Ä\x0016	ü\x0013KºüÀ²\x0001|9M+\x0019¯@
 ;ð1\x000bk±8V,VÓciÊ\x00030«\x0016ÑXÄâmwö}\x0016\x0016ßbñ¬XÍsü	!1\x000c\x0011µ¥Ó¢»£}ó°\x0014fÍ\x000c\x0007\x001fè5Èóxã	Nwl{\x001b«"&º2øáhÞLß{3s#Ò\x0001Üz1
C³ñò×ûGþë//÷¯Ï3C>\x0008Ð#\x0011\x0007ér5TÐ-¶-?¬.!ê/onWw×»íWµýË~/h¦^i	ä^ý\x0006©°dú¹ç§Ú¯kû5ýA\x0018z\x0002ù\x000fL%}aÞ\x0017²û\x0014:Õ~SÛoØ¾¿¡[²2Ô"­½Ea\x0019»u¦©æÛÚ|ËõùSúnL!NGP\x0018]÷ávËüÖ!Ï}ó]m¾ãúú±^©RÃl¾O\x001e	¿¾ëÞé§~~_Ûï¹>¿§^Hie)õ 7´ï½Ôvªý¡¶?pÙ¯Cá+\x0016ÔÎÓ¯D\x0016êº\x0017Ü©öÇÚþÈe?Ô½¾Î)â[å­Rõ\x0013òöWo!÷Õó\x0000°jCÙ­QdQB8!E\x0013k*6ürÅß.ÀtRîì4Ü\x001euéTêzM\x0005ÐÄ_É\x0015C>M\x001f¨\x0004\x0017|Q½é¸Oµ¾¾+üF`¶±Ø¹£©â\x00115í\x001få»l¿S\x00014áWrÅß>;ª\x001eî\x0004RÅH\v	\x0016Sþ#\x0000,Ù"0ÔèÝ \x0010\x000fH2F±\x0001hB°äÁ)q£9xx~\x0017ù \x001aêR±û25\x0015@\x0013Ã$[\x0010\x0003\x0007\\x0000Go%\x0001Õª[Eh¾jBb\x000b\x0001A\x0012\x000côÛ`ûC\x0014º¡twÀmr
Ú\x0014a4\x0014~`J%,Á0J\x0013k_Ð4/,ø.b¾æaÍé\x001cüÀ´\x001a\x0018mºð£ZyEF¦[u¾\x0018[(,#
\x0018~F94Qt(÷VXÏ\x0017
Á2\x0006\~)bkzÊ,\x0002éáD[Ô$]:õ\x00165Wv$QÎ\x0016ÊÜ¤(\x0019-,Ñ+¿pÛg\x001b\x001fÖ"\x0010\x0019Ó¾¬\x0005	0,×±ÐÛÇB3\x001e\x000bUø0@qLåF¦@üÂuÞÓQl­fô´Ò\x0012\x001f-ÐwK¼ó\x000bRú\x0014ºKÿ;\x0015Ü^\x000cÉ·\x0018@NVr6¼E¹¥äh¹|Û«\x0011\x0019W#Ú\x0013³\x0011\x001dF:5`³#þqwÀj¤\x0005óg¾\x0014Pé\x0007( ¾ÿ¼þé~q¶þ\x0005\x000c]Ü<<?=~·Çø\x000c¨8¿_Ã½\x0002\x001d¦G\x000bùI\x000bâö`~\x0017ùï/g«ÅÙ\x0012È&Vóë«Ë¥p~«\x0008ì|Å8qyÿ|ÿåo÷\x000f¿ÌuPÑ\x0011ã$Ð\x0007gE\x0001#,½h+½q¹º^Ýü°:·\x001bª1(.\x000cVBW\x000b*ØyC?FFSä\x0005\x001f\x0006]cÐl\x0018ÒÇ)2¸a W\x001fÖÁúL\x0014;¨\x000e&`05\x0006óm®­1X¾uÐ)ñ 5hR\x00012\x0012þxìBÁ×\x0018<ã:¸"'.Fy+)Q¦^Ì(?Û4\x0008¡\x0010ø ¸MþC\x0016\x00180É§RyF\x0019>\x000c±Æ\x0010ù0¤t:WA\x0002\x0016£¤¦#mF\x001b#÷Ã ôÖ\x001b¡Òèéõå\x001egOï!Ì­þëa.	<ÑfêÓà"¨äi×\x0018s#J\x0010} Ww·+C>]A¸[½?\x001fc2!<ªÆ£Øñ\x0018¯H	@ñd9 \x0004ÈhvDºF¤¹\x0011EèñÄ\x0015J¡$×3­Bõ²Hô;óç"25"ÃH¡\x0017\x000b.D£â6\x001d<×ò®¾XÇ\D¶FdÙ\x0011dSÌk¤¨wÈªt¹Â5Òýé×¹\È\x001d\x0003Ñð\x0008\x0010I\x0010\x0008\x0001ÌÎ\x0005äk@\x0019K¿c\x0004\x00196\x001cC¿h6¢P#
ÜTZ]]0
§\x0012­ÓÂâ1²ý\x0004.¢X#ìk\x0004O¸é\x0006r¼FÈÃ
Î}d\x001b^¹ã+PZcT$Nò52W\x001d\x0001Q·ý{. &\x001aIîpv]Ìù\x001bì:zÜI».Ò¦ëßfæ"j|·ävÞN+IÎÛ¥;sÖ7µX\x0018>È¾¼éì\x001c¨®¾ä<hèüæM<#\x000bwxñ´)\x0001Ò¸÷TÚe*0±MK%2-U®Ç|ú¿ÿë/?IYËP"DÉ@µ\x0007ä\x001f\x0006'i\x001eÖ÷\x0013î\y³X^Ü¤?ìF k\x0004
\x000cñÄº@9äl¤j\x000c#\x0002[#°k N\x0002®vø¢b g P\x0018dBàk\x0004o
@Õ)ófJ\x0015±µ'­A,]6ù©\x0008b 2®\x0001
°)i$¶\x0016ª\x0018IÊw9p&\x0002íAæ;É2`<Ì¤YÏ^EGºC^uCüÞ\x0010ÞòEJS]uùøéù·-.î¹ÿ¼~ü4·´ê-uø@\x0019Æ`I¸®\x0006\x0016ñûÿòòÍur­«w«ôÇÝ@T
D1\x0002±"kVQ¯L®ÅHm\x000b	\x001a«ÅLÅ¡k\x001cuA¢.\x000f£ÀF\x000b2ÂÐÉVvT¢|*\x0010S\x00031ßîØ\x001aeÅ!"\x0006#b\x0017«\x0011^\x0011\x001f¥\x0013
ÄÕ@Ü·» ¾ÆáYqduQjiÊMõFÄ¸iibÄ\x0011k\x001cw=41ñXÓr"°
ÛJ¶\x00113Xá%P8ä}%ó½\x0010´'J¢\x0018\x000b
¤ñ¼ÓõZ\x0011\x000cI:©\x0008'E$eÕØHýT Ç¼.\x000bfeè½Ôaã+äÄY¥º³?S8»¥Ü~  ~}ÿp¼ßóÃãÌXè¢:!\x0015v¹vÆç\x0015£Ou×«ËÕâ=\ù®ÏGÞ®	®QhN\x0014 J¡ ÊÁp;¾]óA05\x0004Ã	!¥º\x001e\x001cÓý5c(R¬J3LDak\x0014\x0013ñ¹:s]äÖ²¡ì'3ÊÒ2\x0011«a8Öýä©Ï	^áIÚ*ýÑ\x0012«ák\x0018\x0013öe?¥XH¿`}yÄ¶ýât\x0018¡\x0011XWC¾²¢HÑÒ\x00131N\2\x0011F¬aDÖÕ(d\x0018N:b÷°xçcôµq\x001bA<8l\x00116rBÑÄ¢ìÔÓLÄ!\x001b\x001c\x00134{æ£ÉEÐµ+ý±|¾J6\x0011\²píèxÀt¤}Uu7\x001dNÄÑÄpÉ\x001aÄØÌQHâ\x001bõw\x0015GÅí&Âhâ¸d
äÊB\x0017`ÞV~£ÝlUIÖ\x0019G\x0013É%g(·!\x0012\x0019Ñ\x0010\x000e\x0011(\x000créÿ$\x001f&KÖXî\x0019t<$:V«ËcèNxÍÀÑÄrÉ\x0019Ì¡ÿpøÂ\x0017g"í«~A}\x0006&KÖ`.Ðå\x001aOýãV¼*ôl§h"¹ä\x000cåÖ\x001b\x001aû5R6Á\x00115\ÿm`:\x000eÕrÅ\x001aÊa¼\x0002Ï¸5'\x001e×CÂ[\x001c¥*£½Är@\x001buá+wö\x0004# $}Ñ­ó
ÕD@Å\x0019\x0001a\x0016aFÁ\x0017ú-R^\x001eg&£q¹ÓåBEÄ\x0011W§%®Nè©%WÅ¯«ÆU)NW\x0005Ê$xÁH\\x000e\x0013éN®Ç\x0005Ó§áÐÍ)×§Ü¦ðíðZÈá}!²\x001c­UMÄÑrÍzÊeQ\x0000Ö\x0017$[0®³F0ÞÊu!jÎ\x000cÑ@36
g§õ@ºû`I¦\3&º9åó\x001b_T\x0015BÊyIU¡;\x0002N>\x001cÍ1×Ç<] 2\x0008\x001dÿEk"·71­2Í\x00197gÜ$k1[\x000f)ç\x000eL`¨¥³á\x00193\x0012©6óx]sÖ\x0010SRB÷YATÀÜFU«Q\x0012Ê©¥Ðº¹*CV\x0007
\x0004@$Ô\x0004E¬Ú£\x0013\x000cSÈ6\x0014HXá\x00007?RîZVa=
W\x0010¹
%}1Þ\x0011¡\¨t$Þ\x0003«Kò\x001b$ß>k5Þ14ò®Ì\x001f\x001a\x001dÝïà8^8ÆÅ\x0013òË\x0016G\x001bR\x001f·¡6'¶õD&ÖÃÁ³¿­?fûf\x0000Ð0 åE\x0013\x001dÒ«tíuD!0z×}³Zý°<¿î´_×ök.û¥¤)i\x0013-éF»\x0008Pi2ojó
ùÑSµÝDEn\x001dó¢08ø]²×{Ûïjû\x001dýÆ¤\x0018È=å\x0016\x000cå
1\x0011Ô¬¹¾}ó\x001aÐQ>\x001cF(Ú4éþ/i 9NÛÈ>AíaþC¹9ÅôCu?¯\x0017gO¯Ïõë?\x0016ï_\x0002¯4/h¤\x001c2-ký@>6ô$J\x000c\x001b6¨]bä\x0017ËÅÙÕÝõby÷§Åû»3pS{À³5<{TxQc;\x0007\x0005\x0017\x0013J8§\x001bmc0o¹\x0014MZ7\x000c·Ò¸ÿº8}zø²øñéóÃÌM.%ù, AAu\x0008)JbÓ~Ô¦Kp½íwÓ«óÅW\x0017ç»q¨\x001aâÄa\x0007¾\x0001õø\x00083}
qô\x001f×gÀÐ5\x000cýÍÂ°5\x000cûÍÁHöp¤\x001fw{] øëoÿgq»ji\x0007Ã>q.ò\x001a#=ÝPb±i8íw\x000bT~].n£\x0004\x0016Û:©®è¤²\x0001	ÈªLºÌ{@P±E73MFbj$\x0015÷\x0012G¥¡
9\x00001Òà\x00158Z=\x001ac¦"q5\x0012ÇD+Z\x0013`ýÖyB;jÂª?¾;\x0007J¨¡\x0004V(.J| N¡ÐC¥~",^Jâ¸êÇd(±\x0012yO3¨H\x0007\x001dYØ§¥¬\x0011¡Ñ´lò¡o\x0008_RL&DJ qJ:'\x000eþ8\x001c@
n1xÅÑÛ<<Ú7ÉÊÅú×§dH !ó\x0001Ø`s9R\x000ejèCL±¾KTÊÅòÃÕù\x0018©ÞfáÑ¾IS\x000eC\x0000¡Ð
\x0008à\x0019(\x0014µz\x0008LÿIq*\x0002]#Ðkp\x0003ôiåÙoö\x0017!ðýy©\x0008LÀð!Ð(N\x0012RÌÀKWZ\x0003\x0008\x000b­\x0011X>\x0004.ë1¦]\x0004Úk¸\x0004
S+kû7©\x0000\
Àñ\x0001\x0010'Næä0D\x0018GÍK@¹¡\x000b;F¹÷\x0007àk\x0000\x000f@È-°i\x0005G\x0000G·£\x001d' Ö\x0008"\x001b\x0002\x0010ò\x000c\x0019$eÀ!\x0002ã\x001d×)m4à\x000b\x0007>3ó¦s¬\x0005²%\x0004\x0001ï­fD7v*ÆJ>g
\x00084º¢xBkõ	Ò9ýbÉT\x0004'®(äñM8É\x0016Uxà H:ÊÝ1Ú} `I'£L?ÀQ>ûÛý/)1Êeï\x001e_Ö\x000f÷Óõóóý\#e¡\x001e7\x0014²\x000c¨\x0012ãË\x0014ÑVÛô?Ú;\x001eg?¬Þ¥L)\x0017z¾¿º¼]_®\x0016§ËëëUÃ0£ò»,ý\x0000¹\x0013Á|]ÀÜðÃÓËaÈ4¼\x001däþä¥L2Ré¿/´P\x001bîE\x000fBv·ùáó«ÛÝ`T
F}ã`t
Fã`L
Æ|Ë`Òa\x00145áïìx´'Âh+­9É)KÈQ\x000cò¤ûãù\x001cNç/ý\x001d¢¿òC
\x0001'`¬t\x0016óÈ¨ñõ\x0001z
\x000e[¢\x001coÄ¶>(\x000f\x0010?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;?:?ý~uqèIÒß=ÜøIrÞB\x0002¶£ÒT\x0002h(ÿE\x0005®õÆ\x001aÀ\x0003w`ÆBä8&E?_\x0011»Xß¸ÝÜÃ}~~<úíÿ9z\x000bôåßEHz°Ô`Rv«
Rq
Ê³àY\x001b~ñêìô\x0002îóÍÕÑêè-üÛÓ+òý\x0015ùåV\x000fõ2¯(°Á\x0002'¾Ï¨Uârëé\x0019\R\x000cF\x0000¶.\x0008\x001b+åºBì´oNTü\x001fätQJí\x001dEûUÎ ~x~JKSå\x001bqæ\x001dÊ¯`éÎPcáAø\x001e
È]Þ\§EL×úväªO®\x001aÉ³¶Îäö)HNw]C[?Ûô¹M\x0013wpOÁ4Ì-MA;Kf¢sK°»\x001fÔæÎ¸~äùíæùèÛÛ'LV\x0001ìÇ_n7©I\x0019Û
±7÷zó9-ß|9ÈpeÓ³x°ØØ\x001ed©:Øí<é9
>ô6öéÅÞÜ`ÊùÙéÍÑ·g×±\x0002àWßîí`3\x0000ÏEÖmà1
«KàQ`åL\x0002§¾\x0000î¶£\x0014íà¹Òº
\»ÜÆ(\x0018Hmb¾ 	z+tØ\x000eûÙ4Aë@æPÀÇ	TÈ¸ÛZh\x0002÷;| vðÜ&¦\x0019<ÉÁ\x000c\x000eÀU\x0007¾å\x001aÌ\x0004ÿçÓ??ÿ´ÞuL^ýxûJKÁö4Ùâ	\x0006}ôÕq\x0008.æ¸>¸izÛÞF~õÝÙÕÞºå\x0001l.Ä	\x0005áid\x001aÀbÂ[µ6¿ý\x0000¬ÜV5-°¹1ÇLX\x0005¾HDÍ\x000e×,¸,3\x00006æ¤Sm­/9Åå°£W¹³èñù¼³ ¤Ï°:§G ·¾Ý©\x00056÷\x0013\x000bë#F]ùÌÂ6&X\x0015|wf\x000b\x0004[9lnÄ0÷\x0018H«ãpg5&Ä&Xoù¹íØk\x0003,¾IÙ°µ®£õ\x0002g§ç­µ|Ã¬Xòq««Ù´®Zâ;B¦utÅ¼°î-üa²áØâø¼·Ò:\x001c!hE¶ÙVm¿)UÓÞ~]ÿ´~Þe°]=Ü*Öe!&%\x0014¶Æâë\x001dÐ:pLèÜJo¶|ÇmÚ«Ë×ÔX\x000fwd¦UâJ4\x0014BÂuAÒ5³ É²êE\x000b¿`s+pGZ·\x0012×àH\x0002w\x0017DO¸\x000e\x000ca· \x000bC\x0005îHïÖî.6íKWkÆYÚ]JÒàâée\x000fÃHóVâZÛ©^ëRß
Ü]C£Ñpw·K'êqí½ÿúeot¾ùðc¹å¨EÌig\x0001dÎÇ!Jì<	Û\x0005*;
ÇóÓWß\x00152o»EuÌ8\x000eòà´\x0002±­wD,·;É´\x0012\x000eÅ\x000cbÉòxëc!|Ô\x000c½#_«\x0015zdéÔC\x0007£ò¸¡Á\x0015ÔÎ\x0008
g&K6cm^\x0005½eDÌ ÆÆÍùDãä\x001a¦¦ùË@\x001d¶[Þ´R9GÚ\x001dç\x0013m5lµ£CM'Î³Yf«×÷_¿Þý¸Kt|ûx÷ðþ6uX.\x001cJü¾\x0016T©\x001b	\x000eI!Q
j¼Ä'úþìêüò\x0004<Î\x0012ää¨FÆFüùh¿¥3¶2ÎÎðG`J\x0015ñHrÔo26%
\x0019\x0019\x001cOð\x0010\x0019gó\x0010²(vUÈ#w®\x001eY\x0019uRªc\x0015ò.GÉç¢H\x0007V!D]=2>Ù\x0011²1cvÙçUC_
dF\x0015òÈµ«FÖR\x001cÓåÓ\x0011m\x000e$Ö/_,
øT\x0011ÂTõÄBá³IÞdáØ´É1'¡Â¡äÂ\x000fïøW\x0003s\x000cyÈc\x0000ÿ#â,d62·îÒ8^lif\x0010p²IÈiK\x0019At X·ÔÔéJk¿#1¥\x0019þ<ÙtU´¹+TÀv,¨¿ÓÙ ¡F\x001a<«\x0012û¨;GÏgÆ¤\x0012­óyv!;~p6RtõvAR#3ê¿¦³¡¬£ «RXiItbc\x0011b÷³ÿôË/	/XRIAòâËd\x0018aªd\x0018)pZÈ?Qa»CË\x000eÃèô\x001d\x0016bîmÐ=@\x001e9¬µÈFÊ,ä4¶uÊ¼Ú\x00042äÀR*0¦y×_¿\x0018âÝ2îî6?o¾+ó,
E`M4d0GAPp*ÎÏOßîÍ\x0002\x0019 oYEuÈà8Ù\V\x001c4È\x0008
b\x0004\x001e^¬½HûU oYE»,0ý5\x0013G½\x0010pÞ\x001d\x0011[U$à*·,Zbðùè\Æ\x001eT	ÙYF6ev\9ò\x000e}]Ë,
vHÎ\x0007#âYrp íÎ7ÌÛúºò0GKÃó>Ç¼Ïª»~f»F¤\x0011\x0019Nl9Ì\x0002CEE\x0006hî|ýhp(JíìFäm\x000b£\x0016Y;2ñ5¾<&ë3\x001cÉ
Ëñ\x0002.³Íá\x001fïüu³ËÁ>_ÿ².V"\x0016OB¤½ÇTOÔ#ÑGb½Þî°+ ðýj¿\x000eé¡tH\x001d*Ü¹H¯\x000b`»É\x001a\x001cG½-±*QG\x0016E\x0015ªS2\x000f\x000b\x0004T°&rÖ95¿lg;6\x000cÊM
dÄ\x001b\x0019iG)+\x00138w´Íhà\x001ciãº\x001dÅ(7m¨Î\x000f¢\x0011ûÔóî©Ó@:òóëH¦Ü\x000e°Ð"¾*\x0006J\x0001².ÅËP·TYÝ×wîØeùA­H0zé	Ì\x00125VÌ:Vau¬8E:³¦qÈ¬JÐû1Û\x001djYíO?Å\x000f·û\x001cÕí'\x0000{,%V2Ð\x000cÂ`À±ÄâRP\x0005\x0011´/\x001dÚ(KÔ\x0017Úè«³×ð÷\x000e\x001eß\x0010æPHIæ\x0000îÓÐN\x0004÷&Ò;.nûòàãô¤YàÁ\x0010\I\x0002\x000fÁÎH\x001døö[B=¹\x0004{üOã\x0000Õ&ã,ê (qPº\x0012³¡ü§ûûÿµ3ãñdýø~ý\x000f
¥\x0012çå¸\x0001SÌ\x0007¹K\x0019\x001bSÁ¬®àÿðE¡\x0004zdCTC[óÎ2´\x0005h$ö\x001eÉ\x001cXÊK3¤IýF¡{)\x00068ÌøÈÚPöÓv»ô®ydVü§Øçð«gÆ>½$A°OÊ\x0007Úä¤)y¦®c\x001e\x0019\x001bóC\x0016×Nv\x0019ÚH½:è°\x0001
öFðÝF§h\x0010@S\x001bEÜéí>4Ð[¶Ò#½¥]ê¡
vâ¢­\x000eú8\x001d\x000f#\ V¢$îV\x0007=¶ôþ¸;ýó?Âß>íô£ÿüðåKqB\x000eÎÐÌ\x0001!å£À\x001cé\x0013Èå\x0003±a\x000b6ùÏïÞ\x0015¡ä\\x001dªÅÚ;J·Ù\x000eÎ\x001a§9ÝB\x0014líaÔ\x001fÿ\x0015ã¯rº~[¬m»é\x0015\x0001v2bu\x0017\x001aE
\x001fIÔ\x0007U\x0012\x0019|{(O¡\x0007:ÚÓ*P0Læ4À\x0002:ä\x001dõ>d(\x001cäüüd¾º]ÇôÕëçÏ\x000f÷¥IÂùÔ\x000c	Søá¬\x001e\x0014ÂÕUé²lÝÕÍË½\x0003Þ­ø:^/\x001d-ñ¡\x0011+\x0016S@Me­Ñ\x000b\x000eA
ðVR|\x001d06üPI\x001d[|\x0017¥8«¤ ¥×b»±C\x001bïVªy-¯ \B\x001bÁ\x000bIy\x0014È+èDäªTàniáZÞ(8ï\x0003%ØqNÆ\x0011K|uÁSy
ðvÂyå³Ô+\x0015v\x001ac\x000e	\x0019ObÌH]r^NLC
ç\x0012kLõÈÙ@\x001a¬H|\x0002KÙ^\x0017AAhßxýøaóó\x0001Üí\x001cùÊ
\x0006«7\x001bÀN\x0018AÜ«aÕ"GBo~ôÏa§ãüX®cê\x0001m\x0005\x000bZâ8Y6°	\x0014rÇ\x0006è\x0005qì«
¸Ç:öªXÑ\x000c3´µJÓÖÆ`#	\x0007#Jîå°£çÏÊõ2O©\x000cNb\x000bÔ\x0014z\x0015°\x0004\x0012
&\x0014$MÀ>Ø¿ÿí6îLÆ¸Ïó§Mq¸Ê$£\x00179/Ó\x0000Äk)¢©w/Ý\x0013ó¹y½·	Åx\x0012]M¦x\x000eÂØÂz\x0004$ÖÊ0²ÝæÕ¼+\x0010[l¬ÂtÆ,<tÝ¡x<c%Þ\x0015­!Æ\x0017\x0004AÄÖa´ÉëêtQP¾xÂ]M\x001c5NØKÄÞg)\x0001j:rÜUí.æmÈ»®uÌß\x0013<6ÜôÄlbÇ¼ÈíSáéóãíny\x0001òmó\ìÆgÕjCàÜ«Î'Øº¢¥S\x0010p§7%¸[Â¢
×K\x001bY`ÝbÄZ~Ä5*RTÊ\x0017e¢Tàn	*\\x000bVp6Ú\x0015ö\x0014I/aF)Ëû~»Éz\x0013íVöW\x0015-6ûÎµkV|S>ãF
é8µ=k®vK¤ÕÑª[«\x0002­Ì´ZrÕ8zÍí¸ñëúÑ=ìt\x001f±\x000fE©9©0;Æ\x0006*ûÑÇùÙ.²ñ\x000b¬%±öW©\x0007Å~c²G;v+ióqEZ|9
-4JEÒ®¨°¹\x001cwìnÖá
ts \x000cû\x001c\x001cÓq"RN\x0016®Ä=.Ç\x001d×6Wââb>\x000bØÜØå\x0017EG½_4\x001eâeqGõ:\\x0019AÒæ\x001c\x0019\x0011I¢;\x0011\x001aá\x0016¥óãn;óµ¼ì^Àá5\x0014+\x0001ÝA/Ípx*'xÃ{ýë{¿G\x0005_ßÞÝýZüÀ\x000câ+^\x0019ÁþÍ	¡1p\x0019£öÚ©ë³óóÿ(\x0001ÞVÂ5À\x0012{çP¾Ç
L:\x0010QPa\x0013e>F9ð¸=Jå\x000eÃÉÞ\x001c&ñ@ªBÃA)©ª«à\x001dÉú\x0013!Q* ¯\x0003¿^æ
¦\x0008µ6¶äüVàn]¸j^ÌHÎ\x0005\x0018\x000e\x0006g6æ¤\x0014ªzÇ\x001d^ø'÷éÖ|í]¹/Åñ\x001c\x001d5%Uüyb\x001et1Ií¹×\x001dãÉå»ý M?\x001cVÿ\x000c¬ÇçÛÍßÝ\x00178øövóµÜÝRo\x0006íp¬y6S0ûÚ\x0017¸¢\x0002pp·¾=;ýë\x0001«\x0007½£Â¢\x000eZâ¿ì×:åYz\x0006Ë
--	,\x0016@ë/\x000fÏ÷Å;Î×Ï·÷ë§âl"\x0013ï]n¥4f×§\x0007)¬±Q@aÐã|usuv±º.Bß±ßÕèAªc\x0019°×»u9\x0011;zÒ
¯\x0002ßÒYsÀèÀ¥äG@P°ÑË\x0004k%úúµç
ð\x0001=MÖÉ{Guáq)©¬Fßð7\x0003Ú\x0004b!@8£\x001b>0;&DÎEÿpÿ÷¿»­\ÞÞþãyóTÑHMb\x0004Ùñ=>ßPìöD[.}IúËÛ³ÿëæôú`\x001bµxûácøÔSÄ<2â|}ÿ±X\x0012
,¿\x0008­\x0005vùA%cD´\l}à\x0015§EcÆýûÛCÍÊy&ªÜµ\x0003GÅç´[o\x0002@i¬ÓY\x00105ây¨ÖÛã\Ä\x0007þ/ebxo<W°û\x0003ÞD!©þ|÷\x0014>î{®x{·þPk\x0014zkìi°Ñ9f`[ç99¤cç±!¯\x000e0\x000f\x000fÿ×O{ÜW\x000f÷{(\x000e=\x0005l\x001e£x.|J4¶ÊaÇ\x0014Âæî«Ë?_î\x000f>õ·#{Läûð£øÇ>ëîúqsÿ|W|6¤ï
I°X\x0016Çøä\x001c\x0018¢¶8Q¦ìp\_^Üì\x001f)ã~øòóóº\x001bg:vçs[ìÒnØác­RÐv(ñ¡ÛFKGZ\x0016Õ¤Â^çvØûÓþaÜÃî.³üüá¶ØÃ\x001dTdG[A/p2rNUE#\x0011ß¼:+\x0001Þ¾UÀ\x0001¶X
-
·o\x0001#:k)SfÒ\x0003Ë\x001fÖ¸ÇëM6hô%±g(!ÂÇÃÈ?ÿ#þãvgê!ð¾YÝ¬Ker!5\x0006È)Ú·\x0008\x0013(\x0008ì(êûtzôfõ×ÓÕ~ÑCÞ\x0016suÈ\x001eÛ$b\x001c+ß\x0004¥Sá.39§Õ?½ß·Ço×_\x001e@È\x0015çÅ Gâ)ü\x0017
×Ka×|
ÿ.q@ývu\x0005gãü@Ìòùç»ÛÏû¤óÕÃ\x001f+^íà+¨5Uþd%½hÄâçÙ«ËWß\x001dzë¼û×æ«éAw#RÛøçOÅýâ°¤¢V9>Òk']×\x000bsàY£k\x001d½â/o^~óaýqýå	ìsþa8ÛóacN:O%RIJ\x0002Å6\x001dûOô,àìµ6\x0000ã÷ür$eû'i¶Ýÿ*7\x000b8¿\x001c5\x0000\x0007Kì°Å"wCÅöI\x001cÌú@®â\x001cbÎc\x000cüSÔÑ¬JÀ?%\x0013ßË\x0003\x0005R³©½aq\x0010¦¤\x001e9©gÚe\x0013M×#gÙÌ-ræ#\x001b¥(¨­$xÓ¹º4Ãð m\x0016F¦\x000e9
»\x000cÍ
g	ÇÜ 

\x001c½%4ýY\x0018ù\x0017]\x0014àùèÕ¿­ËóB±×EqØò aéµÎËýY\x00074J
ÔÇW7ûÕ^\x0007¬ûÀz>°$F\x0010q'>Ý\x0011\x001fx\x000e­%¶}b;8jòþ´\x00054d{\x001a°5ÛäØG³\x001dÍä\x000c\x001a»\x001d\x0018ÚdIùÍp\x000b\x000f¨êJd9<ÈóO²l\x0012)aº\x000cg\x0017è¡<ø© Q	ó`ì|þEïòaou}\x0011¸\x0001´Ã/\x0012ûkqgíñecdì+²z½?ZØ!«>²UÍÔ?É»cK]%E×ÚG\x001fh7Z¬ûÈzþ.wïTÊÚ\ûf\g+Ë\x0003µïµÈ®ìf#KOá{³[²W"eàÞÊáPËZäØGó%¥Xi©\x0002G1°Å×ÀJd\x001aÈ×OÌf\x0016=fKô±«Yì§Õ_1óàþÉù\x0017ð\x000b³q#Ñ¿\x0001bë£×ëòFá8¿×pk­_Fà\x0002Ò+X¡aâdbâ×«\x0003o"\x001d±é\x0013ÙÄQRù	\x0010\ûºº2±Øã
bÛ'¶sµ7ÔR95þ%GJ\x00076¢:08©\x0016ÙõÝ\d°;UbTn©$
«>q W»÷=hÿ¶>ÁqÆã\x0011\x000e\x001f­%:lS­£(\x0004\x001aJH\x000e>+÷Ø\x0011e\x001aóÔÑb·\x0008Ý_^`\x0011Ú"`óê<5\x0005cþ\x001c'·º¬±JÑ"à Ä±Ó\x0012ûOoÒ[kqoO¥|\x001eg\x001bß±\x0010\x0004§°ë8¡ÒOß\x001d½Iï¬ûC_\x001d´êC«ÙÐ`3SC\x0018ÌÉ"±m8\x001eèFZMlúÄf>18:GÍqÐ½aïg\x000fÄxÀ	¯v}h×\x0000mº¦¤VtÐÜ÷\x001c.çöÀÍ½Ð;ë\x001c;âÐ'\x000eó½<v\x0014ÌµôÐ\x0006Ä\x0013©\x0004ªmsìCÇùWPx\x001a ±yj"vOó¡\x000cõZb9\x0014\x001aó¥ëÆ@\x001c3µí\x000c\x0011 Æ¢zp\x0007eÃ%´Ý\x0017ì9\x00169lÎsl\x0012S½Ú\x000e¨mÃ-ì\x001e5Av\x001c³¼ã\x0006
&© G
µ\x001fPûèc'ï8R£<;·\x00062ÕB«Á±V
ÇZEö\x00084ÎÁÓ\x0014øàimbÇ$îjê÷Âù¡-\x0005¿\x0018ØR¯\x001f°èù¾¸µª\x001cåÅ\x001e9f\x0013<\x0018$ùl\x0007ð\x001c
òO^_Þ\_c)ÑÍÅ\x0001c\x0017 ú\x000bP­\x000bÈr$-ÀÜå\x001f¨¨uAPöÀËÌ\x0005èþ\x0002të\x0002°\x0004&\x001d\x001e\x000fnu~\x001aÀÔª\x0010i\x0001E3È\x0016\x0000çÜÀtRÊÒÑwÏï7O·÷£Õó;ø±<¾#8ã\x0003»K\x0000 ¸\*º\x0003#8RÞÒÑw7'§W×g\x0017§G«Wçðãô"t\x0011º}\x0011Øæ\x0016¡ºiZ2òì¡\x0018\x000e\x0002g/Âö\x0017a\x0017Xç\x0002\øî5«õQèï7df/Â÷\x0017á\x0017XÂ¾D¼\x0008è"#³Åp ëwö"b\x0011q;¡è!\x0018}
~%Q²k\x001a\x001f\x000fT<Î]\x001c^ì\x0005n¶Çü%"?¨as ZÃDàÙk\x0018Ük¹ÀÅþß·÷RØq¨Àî\x000e\x0015Ôöc±A9ç\x000cNìâ´VjÇâ\x000bó\x0017s¬`²-K·\x0010Û_]b!\x000eU©¯@¯+-$P­\x0014ü¤ËÊ¬KW\x0002Zhd6Å\x001cB;ïáùîöþËÑúèûMñ
ÆÒ9Å\x0003+Ysæ\x000f?f\x0001xÈbBCïòæüìâÝÑêèûÓÃàjd.¡ç1J\x000fK\x000b@ã®ØàpàÃPÆGÔ\x0013»±ë\x0008Êº¬|1/\x0004móCF\x0013-Ãô1Îr³Ü\x0006ZE\x001fi¾\x0005\x001c\x001d¾Õ®ÄfªX\x001e	½çK¼zÄ,²âZ]\x0014<W\x000b®\x0000Æ4ÓÌ\x000b¡º\x0011eEE¼W)ì UãøêÇ§NÖO·_¾\x0014§Á¥\x0000\x000fÅz¥>\Ã#ÀSrÙës²º>{÷î@\x000e\\x001dûØ±\x0001\x001b\x0017²iÁî#çØ\x0008º\x0003£<\x001dð)Æî«e5Ôr\x001bé8ìjb#ÕhÎTñÀìê\x001an9ö\x0013äVCvv@®\x001f7åå\x00198f¦²\x0005\x001cÄå¿2¤õ¶°.*»< OWW§\x0017cÆGÞà_ÝÝm(Ía}ÿÅÉÃóãÇbÃB@I]Z;ÍoTº\x0019î×È«óóSJwX]\¢eqrysõíåÁ\x001bÆ$l\x001e\x001dýG5e®Z:jîûÓç2W#¹ô\x001e'dO\x001e§\,stÊ^\x000f$M±Ã\x0013¶ëjù=ðòìGÇ ï¬y,¡<¸??öù·*ù­Ç4qLbM©$«Nrºh<`ÖUðë\x001f>?|ùù½,â¿¬\x001f?ÒáÚ¬ñõð\x0004þó[\x001cH§^3=Üßþ_øñO_\x001fÿt²ùò\x001eþ_|ó
lµ>_èL\x0010ßèc\x0007Ú7\x000f;\x0001-lûMhà¿þôîæêO'§ïN®N¿ùËêê[º\x0007×§«\x001b|S<ÿüþòlßºÁRr¾üÿ/kNÿó.å§§gû°³SP\x001aÂ·þòå!U \x0016¯Áa+;c°S?,Cx·®ï¹íXÆp$ßêÝ»Ë½¨\x0003þ\x001dµ\x0001³øÈÂ5zkÒ»\x0007ò;z¤6Þ
º\x0002/È¿knã\x001c~\x0013s
\x0006\x000eû\x0008XÇø}n\x0012\x000cûïû\x0015\x000e\x000bòï\x001aâ8\x001f|ã\x0008ûï\x0004v\x001cB~\x001c\x0014Eû?(jå¿ÿz4}þõÑßþý´¾\x0005Á_ÃíÁ£É1<ðÎ¤Ac	¸ùeÏD\x001dÝ\x0004ö
ß\x0012Vg .öÒ~ýõùýýÓ®Ûºúº¹»«\x0003Ö2æéL1b\x00066XÎ	8j"\x0006öÂ²úëéù^Gl@=ê.0Z)ÉÛ¬0ÙÖ%jK#\x0012ÚëE ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-13.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=^\x001eí¾\x000b¶àw/\x000b¸7\x001b¸Ï6ÍCÖ\x0001®7L´\x0012.ù÷b¸HÓ~±z\x000eØ\x0012\\x001aÌ\x0001p¢wO­K>¾\x0014\x000e;\x0001CÃô/±ÑK	°õêµ*Ù¯`³Ì&è!
á\x0012[¿ü°\x0012-yùb4¾½AsÜ[\x000chA1\x0005.9úb8Erq\x0000'ùMDÇH»AXÿQ¾rw?ù7¯ãõýâÍúöæã^Ý0\x0014PÄ¢·TpË³u7HX%5ü r¼<]¼Y\x001e\x001f½Þ£\x001aÖKçH)ñù9\x000eh\x0004ÁY¤Prq\x000e¸îkÜhË\x0005Q\x0012À9ÐVõ|»r±W©\ÉR6g)L
B¼d· ò#×öq
[÷p´Ý<×êúè8ÓrÀ\x0000'\x001fY\x000báÒAR±âH\x0006 ÈHíS°âB~¿Ü¡§U\x0008×}½\x001c\x000b§\x0003GÁ(¥j\x0006ÇòveÅ¥+C±á4Ê%¥sÄsöWó[
#¶þ«JiE§ì	ñ\x0017ê¡9þ×?ïïP_ûðþó\x000b¨ëE¢¨FqT¯ªqÛ)\x0000xÒÚ§ïF16£©`ôã\x0007FG\x0012p¡ÐéÌËÉ@¯f)£m3ÚbF/\x0014é£ù\x0018,ßª=© \x0008izÞ¶\x0006Ñµ\x0011]¹\x0019qP&3F*|·ùÉ\x0015Åì¶û K\x0019C13B@¥Sb8Â~NMìÀ\x0018ó§vÓcl3ÆòOí5Õî`\x0017»\x0012Ïã)Q<c2cîËm\x0018¹/·È%=\x000eKuiÖ\x0019?v¼gdçì\x0015ËlÔ?¤'\x001e@§!³RÊÉ»Fv\x000e\x001fYqú`êdÄ¹\x0006ªA\x0011RO·dgkË½íéì±§;oyAJ¿Ý]JØÙØ²bg\x0007±	ÒS=°uÁd3ÆíîáBHÕÙ5ªb×DM·tÃÄ+:}¢æõ¨Ô¶nA)c×ao\x001a/lJ\x000e!£%\x0019Þ¦È!Ý¶ÎG)dgÓ¨òMãQN¤ceSë¥æãGMÞØª³gTù\x0001çL\x0015Ç(\x0012L	@/H\x0001\x0002§HMvª³kTù®ù70êÎ¦ÑåÆcç%Å\x0015ÞòñãuàãGO}tg×è]\x0003(4W$\x0006-ii"\x000eÙÙ5ºf×8~:EåÚÈA$
Jo+»Bv¶®Ø6V·#Ý$\x0003\x0012ë|þ\x0018=ùü15i*Ö$öm·<\x000eÙúàr<\x001e¦CvÖ¤©X\x0008\x00193¤vÛ?·éÞ½*Ö$ì\x0016>É£¥ú4|S\x0000F»r:dgM5\x0019BÞÝ1ÒB\x001b$õpá\³jHáèôFá/0­©Úÿ¯\x000f«§õÃÝÍÓ¿þ¹7!ÍDÍ];\x0018É¥~XpE¦´}¹o¤LEþ=;¸X\x001c]ì)Ü`NÕæTUBµ`è\x0006¦\x0015ßd·j_ê u\x001bR×@rKy2&abTÀ¶Ü\x000e'Ë1M\x001bÓTÙÒP\x001d\x0016Ú\x0014yá\x001bÃ\x0003{¼Ó¶9m
§7­M·¹²¤ë¦Ã®Íéª>{Ä\x000edOûÊ)úî\x00193nGèå¾ék0Uäòö¦ÍÉN\x0012Õ\x000egà\x000cmÎP¹"Y3pÑ\x0011ì"Æ4jÕ\x0019Û±ÊÔ\x001a\x000e#Le7ÝÏðÕ7ZhÍ\x0001/j8mL)_\x0004u, "ç
¬c\x0017É®'ªrE8u&d\x001a*!4T52Ó)/;®HVù"«(!\x0008 9®çóÓÈ\x00196ì¸#Yå¤Ì;\x001e,äþ­âÊ\x0008´èvV°\x001c´ãdG2ÔN,JM*H-º}\x0013*\x0007íô²ê¨×"Ï`àòKï°ÊñÍZ;Çfêõ²ê°×&\x0012\x0001(û:üøÁX 4ëË 
j²sÒËª£\x001eÐbÈgý¶å¬WCTU\x001d¢§W6 Êði¿qJ3|wÕ
«Î&\x001c$3¨Îè\x0006t-¯:[^Umy©é¢@#MF²Fo'ËA;[^Õlyð4\x0015´\x0001¥·fjùh8çøò½¤jö\x0012Îqäçaµ
â\x0014ùÃYÐ¶ö \x001d£¬=ø\x001d¤$pÒHëpQæn\x0013E)ÏQ)[wMÕgU¦\x000eV\x0005ûWÌÍÉÂä¥àæ¸Óû>®¯4­rØ4Ê·fö\x0001&\x0007)S\x0016ÂïöáÐM°ð¿Ù¶\x000en?®\x001f\x0016ë§ÅÅ§õÃ\x001as}½·yÙ4¯èIH\x000b>\x0017Ý ´S¹/2Æáêã×Ë³ÅòbqñÃòl¿yóæè|Ø¿¶aUY3\x0005Ù
¸R¬\x001aQ\3	\x0000:Q/±\x000c¤\x0008y¡a\x001d7Ü\x001f'c'u<\x0007ÞÒøªÈà;æÐM\x0002_5à«ÿ}àW
øÕÿ>ðë\x0006üú\x0005øýÕÓãê©UÅÙuÏÛÛõóÞêR\x000c S!¸q\x0011¼3I`v\x0015«K=ÎUÜ>å.\x0017\x0017GÇÇËËÝ¥-¤T»Y$xö°qÞsE¿\x0014Taí¥\x001fÊ[\x0015!¥Í\x0002$Ìø\x0019Br¢Fd¤¡¤J\x0011R*,Aò 7XNE+çÖ{i'¸T\x00029\x001e	ûhÓ0IcuDBg\x001aò\x0018FMDJ\x0005V2$§P/$x­¤\x001cXI\x000fÔH!¥zÇ\x0002+çK9\x0005sç\x0004ß¨ÑÝ\x000bZZ£
¬£?i-	Ç9Cé\x001d!I90È£\x0008û
Ì¤BJc\x001a¸©\x0012[ ÉHnà1¿:z
°¢É'$#¹¸I\x0005-yy\x000f<æ1Ñh´\x0002&ëSDmp²W$¤ÈVÒ¶ÊJæöé·oíÎ¯køW©±ùýúÏ?WO7w7{À4
<§YE\x0011Þ5+J*Éºá¶ßëÊú°<¹äÎæ÷ËÿüÏ££\x0011¹3«\x001cÑ8J@s;JS±¶í©Æ0\x000e\x0006Ë\x000f7÷«§/-|ñéþv¿l%¶\x0001\x001c.Ö
Ðñ\x0019yd¸×=õ°\x001fNOOþrµº^=bùn\x0002\x001a,ö2\x0001ÚI\x001cÕcg:\x0011d¡!ßD$]_©<î\x0008\x0004ø\x0012\x0010PÆ3­èh²\x0015lopúx\x0004]6â;\x0018Ô±äïÀ\x0012\x0016\x0012u\x0004J\x0008>ÿñùNþ1ÐÅ.£ç«çÛ«}"\x0001>F\x000e\x0005\x001b\x001c^ uê¢ÕÔqfûU\x0005YÔ«¹\x001f\\x001e\x001fî¾¶ðzªr#ñPh?õÃa\x0000ªG\ÄÌQ¢sb¦\!]·e´ñ`IK¢sTjîbL)nøYJ×\x0013¼\x001bk»\x0018ðY\x0016ñ¼\x00187x4*\x001eñÜ<¶ÛÍ2Þx4\x0011ð¤M
¬.\x0006îÃ´~Ç ûRº\x0018_ñR¾ð8Âñhì¡vf¸×¦®ÛÐ2ÚvøT>-}¥Ó\x001cÖ £^Lç·ÅN«ðzJ£§¨\x0010±éT'-ã©Y6\x0006\x0007~å|>\x000fC	Ë\x001f6®\x000b;z÷Fñ=|½úó¶}a>^/ÎÿõÏÏ«/î÷+¶ \x0017Å¥¸ 8òY¬z\x001böx¹8_¾;xÿÃé\x001e¡\x0016Nn\x001eãÀWÔ¹j¤¤Ï}SÜ¬íVçj\x0011Oîþ>Ì»¢¿\x000fÜ\x0008=òk	RÆH]÷\Ô¦çÆv¿ÕØ¾áÙ\x0019èmxr÷óØÕ£6ö*µÜ/.íVkq\x0011Onxþ>>W:É\x000bÌ£±\x0017<u¬ç¬&±Wl§×[­þEæIGwÁòñÔ§$pÊ9wÐ\x001bÞì*ötí\x000byX¸ä{ù^ì;¾\x001b\x001e\x0012(ùnx(]ðýðà\x0003\x000b\x0010}üV
Òê»A\x00122IxÊæU²à0äæã+K'¡4¦Öý2QLþóÕ7e{Ï\x0006IG\x0014çõ}ùòÂ<±f¤\x0019Ö;Ë\x0011$
\x0018¤»K\x000ca MdDq\ßû÷£À6\x0007£Á¤¬6é¬§¤ö|©\x0002°Ñ¥\\x0017ñ\x0006\x0003\x001f\x0012\x000b\x001b\x0005Lz\x000e<p"öÇwW¥\x0008©Ì`óM\ðMSa«øÔ9£²Û\x0015/Å\Ç\x0002.7[ïµE3âb{ÙÊb®Mú~<ÜÕã5'\x000eµ×6
\x0014\x0003ÞÄNU5þb£\x000e÷ã3ÎÐ<[Ý|~Þ\x0007c!Y[D¹WIÂ¹ÄÄ\x0014d¯9	Oýx\x00134Ï\x000eÞ]¾Ì\x0017Ú|¡/\x0016N|:\x001eáj\x00172 \x001eÒa+\x0002mÀX\x0008\x0018Ó+HR@±¤¢`¤F\x001eTg\x0019Ò¾,\x0001Üt­#àF/n,¡ò©W\x0002eP$\x000f\x000e\¦¦\¿~¢Pv\x0008e)¡U)º9pÔ¢gÂÞ±RA¨:ªÐE¹ñgY\x0010¥ã<¨
[\x0004¨;º\x0014ÐkVÆDyÀTÐ
$8¢%Å\x0000M\x0007Ð\x0002\x001aÁó!q\x0015¦Ð\x0004Ëó!á\x001bO6¡í\x0010Úb\x00134þ\x0006\x0008MÉüö7vrH¹°\x0008Ðu\x0000]ñ"4Iº\x001b\x0000­F0B\x0002w3°ãLd©7c9oäôø`"Ü%¼a	Ô"¼/ÎÄ¡®£/\x000c\x0011HguÔ× \x0017OÂ3Þ¤!\x0014$¼\x0004Wxh\x001dµÎÎd"êªø\x001c"©vàX o¢ÉÛEvÇjPÞ³°s\x0010ªâPéêGBE\x001axàíh^\x0006JWM]ªs\x0012ªòÐa)G"\x0014\x0014Ü·ÓÙbEP\x0015¨rã3¡£Á»<üiP·°s\x0014ªâ£0\x0008T"M\x0012S]é¬q\x001b\x001b\x000e	A\x0017\x0011vBU|\x0014FÃQ\x0017®Ãtµ4°:ó:TS=²êªø4¸d¾qª5\x0013:\x000e\x0019¼5÷rç4TÅ§¡ÎÃ¶qb|*ï3y&úVÑE1îDÖº0²F­Þü±ò(åZà\x0002¥è¦~bÝ	¬ua`
n®¥ã§3 òYÖ2N
ºtÇ¡èBâ¤ ±\x0006¸M²Pà^<j¦\x001e×ºãPt¡Cq"æÁæXv£ãB/\x0006\x001b\x0014\x0011v\x001c.t(°Cvy(\x001eíi#,%9(ð^DØq(ºÐ¡ \x0016x\x0012Hdª\x001a\x0014Y%4Ú©'îø\x0013]èO\x0000Ð¦Æ]Ü2\x0001SI	7\x0017P1\x0019°ãNt¡;q¢\x0011\x001dÆçÁ)B°V(¾íNÅëø\x0012]ìKÉ×Ok¸ñ\x0019NB¬Íô¦ãKt±/Ôþ_¸¹G5¬\x001aêüàØ£\x0012@Óq&¦Ø\x0004Ç»\x0018ê\x0015PüÕÔ5h:ÞÄ\x0014{\x0013\x001ccI\x001fÙåÑQ\x0018þóýÓL¶aÇbo\x0002'!íbKÓ-ØïÇfpvT\x0011_ÇR_"´k½MOèRfºÉ©VÓñ#¦ÔH¯9 Äq\x0004[\x0017$¯@=9 4\x001d?bJýô\x0012\x0007*7*kJí)ZpÓÓÕ¦ãHL©#Æä="Mnÿ\x0010³H}íÍ
Â'1¥\x0004ß¼x
ÊÈÄç<t\x0001;¾Äú\x0012|còüþ\x001e
	9Z\x001e\x0012/1Å¾\x0004jO8%rX­sÎ_N=\x0007mÇØòÃ00\x0001FÌ(%wÌi\x001aø\x0017&\x0013v|-ö%\x00100øÍQM­ÞBø|\x001aN^¶ãKlqª+Ô\x000fNCNgJÅ1áà¸Ú"ÀÎQcs Q%å&ÙJ\x0003¦\x00010ðQc¦\x0007\x000cú\x001f\x001f{\x000eïcùw¦÷»f4\x0010fÞËVL½<\x0001ãªÇ¸*<p Ü²·\x0013ªµ\x0003¯Âk±?
»æ×ê4ç[\x001eÍe-	ÀÜ«Í-Ã/ç@ÔÒ©ðSüÜªîx»ºÊ}¬\x001fnV··«§=`Æ9\x001e©"V0§gn¡SÑÖõÇÅ¾?>`
  
  
  
  
Instances: 9
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=?9|uz~öDÐ ãF@«¶ÜòbyìfÉè>\x001bUÏ~ÇgÙ¤¥¹0Dæ)`Àã\x000bO~¿\¼_Ü?¬Í?lr«6·È­¨\x000c<1Á*©à\x000fð\x0014ËjÁ#Èu\O#ÏÏ¸\ï\x000b\x001a¥À¬¼¬t0Ü´ÉÍ4rêó÷\x001bØQq»û;Ü¶ÉídrO5Òð% çJYnw\x001aAîÚänân	Øíëh,lSÈj¹\x0007GÕÖFû6¹xBÅ>Ïós<\x0006\x001eÎgsuºç\òÐ\x0006\x000fM¢¥éRíkÉ6ÉeY2h\x0004ylÇiä\x0010\x0019ñxÛ¦\x0015þS¼WdÏíS
Þ\x001e°)Z#fF7F\x0011ëåéé\x0008Ó.þÛ\v/Ði7¨\x0012Z?Óª\x001b.²YõgÜè²sÊi¨ÇÂ?\x0005ºCm\oôçÜ/HN»\x0014l\x0012M\x000eëÏ¹\x000cËÏ¢\\x001a:üBØ®¾Î\x0001ü\x0005ú[\x0000À"Ð?bÈCF3"\ý\\x0005`c¹ê\x000fúS¦\x0011ÐQûù$ð`Ýï\x001fV\x001fo\x0014¸³Êc³Zþ\x0013ßx¼ø\x0004ÈËî\x0017ä[àü§¼Xü\x0001ÿk\x000el\x001dD;\x000e\x000f¡×`¦±°\x001c6E0>â\x0018TU\x0011l\x0013þñböo³ù\x000bÊxï\x001dÏÞ\x0015UÇÜïãU\%:èàÏãå}Ö¼ßÊ\x0006Á:J£gí-8týpÃFh×¹/òot°rY+²TÕa3Íì\x000eÛ×?ýý§?\x0013Ll¸û®{/¯\x001föf·W7ÕvB8!p¥iÜwØÇ\x001b1\x0004\x0004B\x000fÜùËâÇÓGç{/ÞîÍ^¿:ÍË«ÕâákíÑµCðnñãþþz¹Z\x000e\x0000\x00149ºFe_ã#ÆÜ\x0000èÎia\x0013À{\x001ap¶÷nöÏ³3ì\x0003(Â-þ¸_½ÿÞ=\x001aÏ\x0004àrt&pÑò0ÏL"BOáqxÚ²¸ß¯ÿXÚÅ=E\x0016¿¤³°w@#e·í¶4	W¦ÝfE\x001a§»Í|ß\x0018\x000f§8<½Ûöò\x0008Ùl6</p><p>DÊã|üg\x0005:y\x001eÞzô)PÏ\x00126§¤>2Si¡\x0016<Ï.\x0007`î÷Yò;pÅî\x001e®ïï\x0010ª¿X|þîÍÝã÷\x0001°ÿ?uï²\x001cG¤é¾</p><p>v³JÝ/Â\x0015\x0008"H\x0001	6HPºzS\x0012$$ @\x0002D&«ÙÍÙ7y~ó$£jªêáððp³ð.éÎNfW}en\x0017½þQ\x0010ãÊf³p\x000bPh¦dK`MÚAÚ³×'¯^\x001d??\x0006GýèðùK¼ö^]üûÖ÷\x0016¸{îc@AÐRaS	¬-ÏzÓí¹Þ\x0003Cy¨7ë ]\x001fÒ5@FªþxÍ<B\x001c!\x0013
ú\x0004H;xPÖ\x0018\x0007$«z¾\x000fèë\x0001QâÑÐ*\x001a!±\x0002\x0018¬bÚ0ô	C=!ìFµÚZ¾3uEáÆ\x001c<E\x0015±\x000f\x0018«\x0001±þ^:xÒ<VG\x0017@\x000f\x0004$Ü¿\x000faê\x0013¦ú%Ô¬N\x000eK3+0ÈM·¼t\x0015¹Oë	¥\x001aÖXÔÞ,oC®¾5ôeÀã\x001eì1!zfÕh¨$;âD±n\x0011}Òh
</p><p>D½¨ëwb24Ô\x0016\x0010Sñ×\x000b¢Qr»8xW 5DÓ0ÓG«èqV6!ÊY1jÏ³¢×\x0015]ÿ®`\x001a¸´âq¶8F¤\x0010*+7b4û"®ÝÙºþÒVÎ.o,º},\x000b\x001be'Æ=¯l½veëú;ó¹ôc\x0007(EyÐkÚEèÿùÉþ|çßöLêÃ?ð§\x0007Ï7·\x001fXÕtw	V7Ài\x0016òøå\x0012\x000b\x0000-ø\x0012T1.\x001bJ¾ùh=Õlk4\x001b|A{~ÅJÝ_\x001c¾9~qq|ðìøìüÙ1:w¯NÎ\x000f_?~wóåËýõRþç\x0006&Qá¿ª9SÊäÀ³\x000cÎ<\x0016\x0015"§%ï\x00048#7³qâ\x0013ÿªç\x000c½wz_Eá\x00068\x0015ÅK4ÞI³rÂÛÿªçô	Í/ZÏôH\x0017L`FÔ
\x0013Ã¸ø¯zL !Á ²%´
ðDwËiçãÄ\x001cÜãòS\x000fª#ëõ\x001aï<)k\x0003¨\x000b@µBe£Ù@Ñ}+?õ pà
x\x001aV@­\x000e\x000cªq´Æl h.jÐH-0\x0004JÂbÀÉíèÈ`gãD­¯òÓÀé	\x0012\x0007&\x0019¦t¼?µ	s®&ÖzÊ »{)*\x0006æQÊÊ3hq>\x0017¨Á÷òS\x000f</p><p>~l"Ð\x0000~l¦^;y4Zóâ«Q~êAM\x0017)h£Ö</p><p>¨¥\x0011M\x0000\x001a°\x0019~6P/§my:\x00114Ò\x001e
VSÊ§ÊÇpó¢rAù©\x0006
A¦PÊt5)/o¼Î3>\x0016\x001dòSÏéàË\x0013¦4\x00180©+\x001fSÏøÝ±óè±m2ÀÖD;¾;p\x0012¦²jÆÓâ3\~\x001a0-7*Ár²\x0016\x0006rz¹èã¬\x001d½ÒòS\x000f</p><p>îOï\x001e(çëQá@@Ó¬+ýµå§\x001e\x0014îMÏ\x001fÞ±n+FÛ}ú99Ñ®³MÆ\x0007\x0000\x001bÜ\x00041\x0012gX-hñb²8n´üÔÆÄÕqå$Ñ+\x001f²ó«³4çG5îòS\x000f\x001a*K\x0001õrâ\x0000	~\x000cvÏ\x0006êP¡üÔé\x00054ÑÝ\x0014²öV8ÓÆ\x001d{\~ê9Á¬§ù\x0010ÀÑpFPØN@ó\x000bJngßéu\x0012G)Ä2Ó¢FÍ¯\x0012ªRÌ	ê\x0011´éÐkÿßxQ®Ã\x0005
I8Ñý\x0013GÜjN\x0014ª\x0013ó\x000eì\x0012Ë \x001dj01:#(.hÓ-êº<¨°ó(h\x0006µÝó\x0016-rÎå§iE\x001dùÈzn^F¾£dûÃzòSSl\x0004ë\x0000\x0001'o#§s=ñX\x0006PÖR\x0001MDð\x0011Tîz;ãÍJ}µì¼é\x000e\x0012ºô®`Æ$\x0007\x001e\x001d¦\x00199
r¶øñÎûÎ\x001aÉVÎQäúO\x0004¤ft<±kðqù©\x0006µÉa\x00116F\x00057\x0013=àÈ÷³®(æ¹ËO\x0013¨O¼¢î!å¬Ë\x0019ñLjJ\x0003êñMD	ÄÂécàÏn1ÓQÊp.^\x001d\x001e\x0002ÏÞ¬\x0018ÀMQ\x001có9hEcfFü(YA±Ya±\x001c´ü4ÀrÖÃÁ_GZVÖ±WfÏ</p><p>°¢¯üÔÃbE\x0011±:MÍwÈÊo¨¨×;+*VuM<+Âd£IÐÝc\x0004×Õ\x0015\x000brNØG ü4m\x0002\x000eç¡ddN²	5£\x0000Ö¬¬N\x0001«k	\x0018,ÞJÌ\x001aV§Ë${]qºUùi`-A\`µ°Hý§·a}\x00193\x0003ëû÷§«\x0005\x0017®<^íßëüòy(\=b´,ógÐ¶</p><p>Sb *\x0017Ç\x000cªß\x000f_\x001cüã
jæ¡XõnP\x000c¿i×Dª5Ë²\x001a¬4d\x000c6\x0008é¨Í_MjK\x0008²Ô®Ö\x0014v\x0002y'Ñrµ\x0017z5fýU>HàÕ\x0006+æ\x001f¸
\x0018kVHàÓ|¤\x001dHmk</p><p>SRáÁJ\\x0017¼\É5Z?æB×n¤Æ¦£\x0006eJÅ Ò\x0002óÜt¤c!ÓjRi'oHt£\x000bïÿè­î\x000e¿óH\x0019,F)?õ¨¥¢)p)ÌSÐâ *¼\x0007fDÅ ´q-[5Àß{$YqEJ$@jÄ\x000cTqÖ3eÑ®¶=ãº\x0014ÌÔ(éf/éæhä\x001dÇÑ\x0013QoùÃ%UhRµ	ÍOnHÅpëÑÏ\x0006,\x0012ö9û¨Ñ±b±\x0011%®±üÉ\x0019*\x0013vkÃéÏv\x0000fø/þ¸üÔ\x0001âô\x0001ºT\x0017»J\x0016q\x001c)\x001eÏY\x0000ÑÕ+?u&¯6êf\x0001Ô³\x0000jì\x000czL¿U	\x0007N\x0011`.SÐ\x000b a÷>\x0016Ït\x001fÀÏÑ}\¼Ç\x000eþ\x001bïîàhq{»¸ºÛÎ\x0017qº<Åî=Îô(³#}v)S{Ba
2é\x000eÏÏ\x000fO_
0®þl'#ÆÇ¬¯eÄp¸0\x0006ê\x0006\x0003F.ÇAF4\x0012öcüöçõ;ó\x0007F\x001e0X~Vßùèvq}·x7òqR\x0014MÐÞÒE4]¤¹¡:Â×Ç/s~øâÕáÑÐg?ÚEOlù©¡3Ö`Àè,\x0017
ÀßVQèði¦ËÎÿ±üVºç0Ù¥â3R:Ò¶ã%\x0013%ì°T\x001fo ä­ÎÞ[ºdº\x001e³7OÎ·ò\x000fmáüøé/coÐ´À où\x0011Nló»ûzy½¸»#Q-¬Xj\Ü\x001f@D_Ù{'fEpF8~õòäÅá«W(°\x0001yÐÿÓ]X\x0013U~Z0YÝ\x0004¥YI\x001e¤²SÓüf$-cDËO=)<]ÊÎ§ð>9¶Ô}Â¹%ûþq³4ö}±°ôÆ­mÑ_\x0017W\x001fï±\x001dlì\x0012Â8*ñOâ\x0008\x0005\x0013\x001ep\x001eó¥\x001cjð=þõðôÙ\x0005M~\x0019Ø½?\x001d¦¼þü>\_\x0015o\x0012+íR\x001fòtñçòöúÓÈ[S\x0004\yl\x001cFéË7O\x0011þ\x001f\x001d¤äJ\x001eØ8ç/~Ûr~øÏvàY¬`/?U|6iÎq8\x001fyì=x¿)1`vè></p><p>Ä/¿\x001d^¼ÞÒa0¢üTQâ(jøvAeÒ\x0002CÃQ3\x000ePbEÃ|\x001e+»ËO\x001d¥r\x001cqÞÏwN,³æoýñúêæór­:Uøî\x000fDº\x0012\x000bÒG6¶BÓ½®ÁóæT#ÃÆÊX\x0017 ºXw¾	zq°öçÃ°¾]Â\x0001l@\x00137lØ¹Ï\x0017ß?-Gí4§¸\x0018Hu1c¯"MÙ\x00023²T\x0015ð×¿\x001do7Ôº?ÞfZX³Õ¦bbíIcq¼L!ÍÖ2©¥#4\x001b©/!\x0005Åf"</p><p>À 3^ä«=¸b\x0010y1±Ì¹üTcÌªFq¸Âi;\x000f"ä9>}úúåþQªW0­ÂCÒåíÇÅÛ±\x0007ÈÇ¬9¦¡5&KÞ¢\x00116¤â+??></p>
  
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
