
# ZAP Scanning Report

Generated on Tue, 24 Aug 2021 14:27:36


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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=»ø2Ö!îX«¸÷r¬¾d¶\x000b\x0015YÌè"\x0010 '\x001eQ J\x0011ÇPñë
¬\x0001\x000c0\x0011\x0001Fwµ/ò
`\x0006Mx×KÁü®:k@°ONñ¯·ÿ¿\x000f³~UÅä\x0011¦,\x0017)23gø{\x00009{×Ä7$@ùÄ-XÒ\x0004\x0012\x0011\x0003?Uq\x001aä<\x00187÷\x0002¼\x0018¥¯P>½\x0011÷£Ts9\x0002Ùµ"²É\x0002¶\x0007C\x0015ÄÝ Å¢´Q\x0014àúVT\x00004\x0014J;]»\x0010¦\x001c¹iU5C©=å\x001f+fF\x001eNV±³~úMx)LY-KüÚ\x000cSkÏ\x0005Ø¡dê³Ê\x000eu\x0013!ñ\x0016£Ê\Äù¤2w	Î@ÝéÐöìØ\x0008Ã¡\x0014+·|\x0017âÔ&Ù¾m®Í\x000b¹sn~Ýî;ß±\x0015\x0008·QÐÜe\x00029qê(3óýfÏy\x0019ý¡lþA¼¿½ÁÒæ\x001fï¶n\x001a$(%zý'9N½ôÕ×OÚï/NO°ÈùÍõùæìdGéãûí\x000fÛÏ_`þø/; e\x001cNâ+Q»R_R$"Ýò]ç!\x001dZ1j-Ö£«fQí\x001e½\x0015Ú?¼.T7Ô£|C\x0014
\x0007 \x0014_OOTá¡DI-õuÑA¨mµ¬íúum`\x001fû^Q"r¥=\x0013ýÆzT\x001fÎÐõ¨*+\x0004,íP<Ô\x001dµ¯\x0016_¿@¬ÖÇrè\x001aÃ mYÖ;Ú\x001d\x0007¡\x000eÕP\x0003\x001an\x000f9,kn\x0005äJå×Î\x001bÜ!¨Qs|ð\x0003Î\x0010¼§Y2xÜàs{\·ãZ
[£>`°}©E\x0015JOÂ¢´}ó¦#l_Ã>à\x0010qó½°;àvQºâ­ê·FF¾\x0005ÂNÊ kGÛ®dJpÑ ;Ø\x0017vÝ\x00119ª¬H°õjØ\x000ecÖ,u$â\x0012lSÎ£­ëE¢\x000fX$XoA\x0007_º\x000c©b@\x0019Ý\x000fu}©Ë\x0003nulf\x0015e-\x0008v)¾ÆfîÝ`Û\x001a¶=\x0000¶NÖ^>H"*@dÓzèG\x0018ºÝ58´M×vº\x0017y´\x001d6?­îF§\x000eíëËÆ¯¿lt\x001cÄvyîoc\x0011¶ÝL?\x0014F\x001dÃ\x000e\x0007\x001c$j¨RP¦¾ôµ2¡ÛT²\x001aí,§º\x0012¶ç¬ ÜÑº_
½H½î¶HÔè,Áëa\x001bWª\x000b@ç<v,d¬#\x0007\x0007ÁÖÕÌÒ¬kG;R\\x0006õ\x0008°QS\x001aíá¶ñ¶ß"±%\x0005\WÂ¢ØÎrZ\x0001ìÃR.®ºmI\x0015«K2ë¼®íµà\x0007U¥ù\x0000´¬ô!»Ý5º¶þô\x0001Ö_Ò¥c\x0004(\x0006g¥\x001bïf´¢Fì\x0018¶\EÁq,)Ýz8ýl1H6Ý®H=*FØIYv%llNF9RÆ !`u8FàóCUÅ\x0005;U\WÛYé¸T¹@/Mø\x001aÆ®Z\x0016é¸©\x001a³«
jÇMcÓ¶\x000e`_\x0006d\x001aØe=n8\x0003\x001b_Â80î4Ï|îy)'7»y\x001e£ÿðÃ/ÆÝÿð!\x000b~fÏ÷·>mLÝâ	\x0007@¿Üüúpÿøù\x0006!Y-`nÖ\x0014\x001cTphÁþ9Þ;ÔÑoA[J,{{ò§Ëë«\x0017ïOÏÎ6¯OH:x
Dz'K\x001f\x000b@(,\x0008L\x000fè\x0000Â$¹!Dá4¶K(èýü	©Á -BÎoÊ?HùMOnrÉçw·\x000f÷w?ÜÀ÷Ï³#$a%%s\x001cÀÅ¤ÜàA-©\x0004\x001b[\x0017t³³\ûùÝéåÅù7'ð}*+}ÀJÏ\x001dWaÕ\x0007ÒÉTt°jÆjr=°º
«[2DSÓNò$¬x\x0011V\x0012/9\x0010«·c¬ðm
VØ­J\x0012VñU\x0012RÙ\x0001§´\x0015ÎÜ×\x000e4yjLÉû\x0019ßhPc\x000f°ä1Xô¿Vuô°`S^s\x0002kð^Éã*º,å]\x0017°q\x001dØP«LUS\x0019¬é»µø!Áúu#kC¶ qdSÃç\x000465[É`]\x0017°±^³qÝÅ8Á%\x0017	¬ÄÖBé¶ÇA c=²qÝÈ¢þ«/'¬ÊXñÑ\x0006Þ\x000f×b¥ìW«^\x000c?xîÎåýã\x0017
6ÆÍ×ûÇ¿Í^¨Á©¬{^BUgiPj$ÁTâu\x0005&|¾C`d¼¿¸þ·ý\x0008C04#\x00149Ñ\x0006\x0010J´}2B\x0017è RÊù\x0003\x0011º
¡kFh%Nàdà«qB\x0008N3#\x0014ñ@Ã^G¸ÕÛ\x0010\x0002\x0010	¡ácLdrw7#Õ:ÍëP+\x001eCef\x0012B­\x0019 \x0008\x0001B\x0001Ê$oÔP¹l\x0003B\x0014=§¢\x000c2îZ!Í\x0010)!&Á&Bå\x001f\x0004ß\x0010¢§Y\x001c<*Ô\x0010[÷Çè@\x00105ö\x0017L\x0010Q`F1Ê\x0003!êz\x0014uë(ú¨óû-BL2L\x0019¢,\x0013íí\x0010mµ¥mÝÏp¸`sé´u*ÝL\x0010$\x0013\x0003\x0016å¾\x0013'{e\x0013ø|=¾y\x0008Á^#_\x0011\x00151°ø';X\x0006wà­"\x0007c=C´Í\x0010U\x0000`p6Åµ2DAC(ý®IÙ\x000c1È
"J1·A´>W\x001f\x0019|eÀ¿&·3\x001cÚæ@±ÞÎ±y;k[\x000eEëøê\x0003\x0013Øð(îZd­\x0010¨&:Ã4C4´a¯ðD£´Dh\x000f¼©n\x0016eZo\x0016\x0017\x0003»bzð\x0019\x0015&\x0015f&\x001e8ÏÊVK\x0011¿¶BåØÎRü	¢a\x0013G\x001a(ÄXøµ\x0011"\x0000!{\x001b«àbgt2D}à£IÌ ê$æÝ\x0004QÒ\x0007@«\x0002\x0019Òy>sÔêÞÂ¥òaÈzô\x001f6¨Â\x0005Ó|vÿåöóçoî¾¤ÜûÛY\x001a,¹Ü9\x0005îàØoñ\x0016#Ø;¦âÙÅ»Ó««7'çïRIîåÅé\x0002jS­À)ÈI¤\x0006]W¾¦Sâ\x000cÔiÛ\x0003¨\x001e\x0003Õk:vN\x0002êSjX
	9Ç#êw­²u@Í\x0018¨Y\x00054ò}:3PÍÅÀ#j\x000fz®õ\x001aí¢77+\x0000&u)lë3ëW+,fPdûØ\x0004Ò
]Pîî¡$¯$¦°¯ÏK\x0001*=\x00068È.\x0006¨r!Z^4ßàk±KíÂîAÔPË1B¬+jC´\x001dó\x0014Å_-~5=\x0000 ©\x0000æ!Ã\x0019$y%ZÁ^âö\x0007 ¬V¡n_¹
0b\x0005H\x001eÂP\x0000ê]ë±\x0015à((\x0011((Ñ\x0004\x00106s Ç\x0008)Ø¨0£ZÊC'Ù«1B¯\x0011úÜ¹\x001c\x0011*|ãÊ\x0008Ed»\x0007x;Âj\x0019úæe\x0008'·&\x0006oî\x001c\x001bãóPË÷ÉÈA¶\x0015 ØÜd9Z\x0011ÐåÊ±1O±1\x000fº\x0007"t\x0015B×<6·Ã1tå0ô\x001c½\x0003#êà1¬6oß(v²%Ìxv_´nãP-ÁÐ¼\x0004Á\x0007Ôá±'=D?\x0001á®ûÒPªê2Á¯\x0010eÌ¹C\x0000QÓ\x0008J>©µ>t\x00049§¶àk>gb³

(p'\x0019bÜ
~¶B´Å_Û zL\x0008"·1X\x0013Bãôj1+\x0015\x000c×\x001dª9ûáE#uÚ;ù²½ûñè_\x001foï>ßßíñ\x0004í8G\x001b\x001a³¡(Ä(w ò³ÆÑÙÑÉ»Íùë£½>=¿º8ß\x000bÙ1d|:_
¹<Èa\x000eMÎ«-\x0006´Ý0Ç
s\9p0\ràGÁ7\x001eä`;\x0001vz\x000cØé\x0003\x0000Ûø-gf(lÿD¬:\x000crV\x001d\x000e(R\x0001/iª\x0010æ\x001f?Ý~ÞF"CÎSB\x0013=ò5e\x0015û]ó´U\x0012Ø×g§WSõøf¤Ä\x0007O<%óJ\x001eØ«í-øcïï~wÃX\x0001\x0016Êl¿¹À¡|îG±3WSðÅ6o.Î§$jG\x0008Õ\x0018¡jG\x0008©/îb\x001eCçÙöm÷l¶K\x000bBiª14k â*\x0006Ã\x0010\x0019¡|öm»\x0005¡®ÆP·\x000fbåK\x0010aGÂ
¯&\x001cÑU\x0018]#F\x0015c
ágm\x0010g\x0006þp¾ÂèÛgÚær]|\x0011I
òvQ\x001c\x00150êàýbÄ\x0018£\x0011ísíÊ[»N|y9J^f×VjÇ8Ê
Âæ\x0005¶}\x001cu.\x00145©§®fUÊ\x001eÑU'£k?\x001ae§¶Q0jÆ(ãÁs\x001dª¹\x000e­s­°\x0007\x0013I)'Ö£±¼\x001e¥6ý£	c5×¡u®\x0001ã(+@\x001e3D¶:ÜM[h(e¨\x000epÌnÄè$çTê\ynê!&v}ð\x0015 c
2¶ôÅÀ\x000c©Y\x001aIÁÉòàPªê\x000cÇ¯­\x0018­ÉR\x001bdSRØ´d\x0006¨g-Ê&õ0ªöa\x0004_¢~©k'Eý¢.\x000fïâÐ=#mmÙÖÃGEí8 ¡½äCÜ:6\x001dexÞh\x0002©kº\x0019¤\x0002kG\x0015\x001c?µ<ÝòÉ#N\x0003H%²\x0015^l3øA\x0012|:ýùíçÏ)½ýýÍÃI^c.?N\x0016·\x001cs\x0018è¦)É*Zï.ÉÓ7o7WW)ÁýýÉåëI\x0001ã0Û\x0011'»\x0011£p¹v\x0018£/¦ÜNøÐî\x0011ÙÑù1FÌekÂÖYm0ÀÔ"=\x000f¢]?2¹XcÓ\x000cþ³züèùúÓöá\x0006|Ã½¦\x0019{2AptÃâÍÝm]^=_m.OÀ)ÜQ\\x0019åâª\x0019d(G¸±%£Æ»bSØ8õz¼\x0018¤\x0015H)AÆáY$§ä'Ovg&\x0013!\x0017CT5DÕ\x000cQJì@¯\x0019\x001fË8>yCl\x0007éª\x0005ºA5t¡¤Oyön~è\x000cåEv7VÑ\x000erTL «ü¤e }	¨`?1Ê\x000cÞgÄ'±ýå HbftÔß `LÕ8\x000fóaËhFë±<ÁÛÀv\x000f¬È©ÜTs¹\x001f¡õcÖ·"´¡=c\x00146\x0008\x0000¾å\x001c\x0004P\x000e`\x00080½f´ ÔØp\x0012_ñ	´§uN«É<´\x0010\x0012c*µxo\x0008\x000bW¢ÍRXyOËrSOîéÅ\x0010c
1¶BcÜ-\x000bÇ7:®\x0004ÐÃÔ^pHÙL\x0008«ÍE\x0008±ñ\x000b½8QÃ´âÚ©¬Ò}\x0010·ÂÔ\x0011Ç
*vréø/KkÍ¦#¦j\x000eHù!²ãÌ@\x0018\x0005®\x001aÃUÿìpe=ºkWrªcìµ\x0012xÆ÷>p«Ñë\x0017Û¢e=NêdÙ³5ÅýFyÛ>xuW¯\x001d^Çep%q¸\x0000[^\x0016¼à
®ùg]½B¼Ù\x0006ç<\x0017»RïÐß]\x0008!JJ0*	WSB\x000e'ÛéÝg¿J³ñ\x001dº\x001c{1\x000e÷\x0014bT»ò±\x000b@\x0006Ã\x0001-|è³äãÁH\x0011­\x0005(O'¶hW@ax>U° Ê\x0019\x001fwïÒöTCÅU\x001aH»+ü¾\x001ffÌ*H\x0008\x0013»@%Ú\x0011FÁm\x000fÁ8äE$aWu\x0001F\x0011ÙÕ®H0¡³)mÒõ0M²?ÅàkÀ´óüØxñýûÛ=\x0011£ÈU\x0006mz¼yUÐÝ|Àâ£ãsãÅ«w\x0017§{J;\x0006&Ö µY\x0004=uÅ.u\]¯v×\x0000\x001d^o\x0011(¾Þ®\x0000j\x0004\x00073M\x0014åýÖsN¿BQøÃê
©^7¤¦¼ù`\x000e=¹HsûUÜ}ZtÈ\x0007E¤Z®EÊË\x0014\x000e)rD¬ã¹»Y2«V¯×M¾\¹\x0003G;ÆçòäsAÝg´UH«¯Wî|[RÔ}ü¡ýT\x0012m9\x001céàÄ#RcÖm(É9êV(~>µì'k±k´\x0000ÝÜ(uJ\x000f@vSé\x001bK«x*A&QÊÀwj§¾´ÀZåbðQ\x0004Á\x0004Inþò°½ûþ§=w\x0015÷·Ë\x0000ÃÉZÔ\x0016ìT0\x0007½¿o/7çp{í\x0005;Ø'	¬Ýuõ\x0017
üëüÄáf°»ïý«À*cÇ`ñk;XR|dP¡öæè2×ña<à °"!\x000f\x0016P`RÆÎ.ÛÜ}{swwsôzû°Ç\x0006t&kdbVæ\x0003ÌøÈÑ
¿[`Zí6À{zr~~rôz3)î?|ùy¡\x00180/Q±\x0016âåýíç£·7\x000f\x000f·{\x001e?0¹XäN`ïd\x0019|\x0006xßóòâôêèíÉå%jg3º\x000c¢Ñ\x001f¦Øù\x0007/è\x00113©*¼úiûøóÞDNÏ\x0015Ú\x001at(_µm7ggIPáÕwë7°×3¨ô¹Ì¨12£\x001aÁ)$¹Æ05@OÈ\x0004WAÚ]¹\x0001X5d¦uÈà÷Sn.ü°  \x0017þúL+Ö\x000fY¬ÅFd°ò¥)CF1x\x0013­gd»}ÈÌ7?þú}¾\x0013a\x0003á³íÑåö+lÈÜR\x0012\x001cóâìæèíýíoÛ/ÿr¶æ×Û-vêÒ°GÊ¿z\x0011\x0005æ³¢Åî¬3àpàË/æ6zj*-a ³KyrôöâôÏwÿr/©º<Ý¼\x0003ìG÷°I§\x001bT1ã¡\x000eÆÏ\x001b1C6i]&ÈÆ\x0010d³c: ÆS0ô@¬Dnõ\x000bÁïHz8jC¬uè\x0004\x0019\x001b6â?ÐÂHÉ\x001eé£Ë8§l\x001a\x001ch\x0015ÄN'K\x001aè\ß\x00014`{>\x000e_Îêé\jÂ\x0019i¤©±\x0016t~ãî\x0001Ú"è>çá\x0015
n4Ðª¬^ãié£\x0003dÇÇFPYr\x0010![¬M¯\x00052hé£\x0003æ³qò8ëH C,ã,{Ö\x0008ºËÑ!EÖÜ"Ðù¸\x000b\x0018£í½8"b]0S3Í9I#f¯Ëqç:Æ"ôq8h\x0015²\x0018\x001f.iW:\x000cVã®Óµ"±æ8}tÀìrB8öï
¨á1YôÚø8>\x000e\x0007ÝChE\x0007¥Ñ\x0011tô\x000cÚ÷Ú¨>:e%íAåø´S±×¥Î\úè8ä\x0010\x001d\x000es
Õ&ÐI´®ï^k\x0003Ë(ÓG\x0007Ð¾lBï±]K\x0006mÊH\x0007Ó	4¦i§.#Í6Oúù4Ò\x0003èN\x000bÚà=hº\ð\x0013\x001eim}î¦ç¢@{qàyçú÷\x001fÝ`è\x0006CÌé\x0003\x0000\Ý?þ:6#¶Iä?\x001dv°r#
³ckTj3}§\x001c]]\¿lLZÕ\x0008V\x001f\x000c\x0016_hC\x0006ÉÔ15Ð\x001a?=º
h1Û7}\x001c\x0016ëuFëlî~
h-o;iýô\x0001×\x0000\x0017·[ú8\x0010.\x000fÒàº[}9ìî\x0018îÌ)±\x001c®Æîéã@¸Þô\x0000nH¢{	®R¼tý÷×\x0000\x0017_0ÓÇp±
öYThÈ¥Åà\x0003¹PÄû\x000f÷rú8\x0010.8OI»\x0002à¢ºF>\x0016tGWôØj\x001aõÒÇ¡p)É\x0010\x000f\x0006ø+\x001d\x000cBóèÚ\x0019'¤\x0005..\x0006øb°Éç@¸Þ§·\x0004×\x0019¶(;c¬íûåæ¯¿ýåßS°×âAh?\x001f½Ú>|Í	¯kHA\x000b°'En`7wÂ\x0002w=íç)¼WG¯6ï§aG%vÝH\x001f\x0007C÷°6÷\x0005È!·oÚå÷Ã\x0011c3}\x001cXæÆØËcº#¼JN»¤-\x0015FÒÇ¡½¥¼NK%ñ1 À.\x0018ìæ&È
!«\x001ea)\x0010bu·õäõ#àC­	°AÀ¦\x0007`%õ2bå	²V\x0005òt(¹
r@È¡\x0003d'sÂbL\x0016%vÔaÈvæbnÖ^ú8\x0018rô¹×\x000bBv[]\x0012\x0016Î}Q¶X¬>z\x0016^Òi¡ðàÈÇåµ¬ÔAG²þ	ü _Ð;Â|Íô\x0001ÞÑ«¶\x000f\x001fáv{ó°ÊA2ÞE:\x0012Ig\x0005`[eÉWaÎjÛàÃÓåËóóöÓæÃ]\x00087\x000fO:\x0016Ù:ý«á\x0007QÔx3\x001du\x0016Õt\x0005.\x0010¯¢ðy´±öü\x00021\x001fþöõ§»>\x0010*9âù\x0013°½||ø´½û!¿\x00127£\x0016!EêûÐG¢x²\x0017ÞçæÒY 5cf¼¼¾<Û3ÝF{\x0004Üb\x0002]þ<\x001c8«Ïóx -ç±Ñ»&ÔÞÎ\x0019G#ÔÏä\x000fRû­R\x001fr»á\x0017.îØ­²^Ú7cÒ&ËÆ¶*·SãÃq¯3¯^bG£
ó|1j,Z÷¾\x000bj|ôÚÁ¡øÉO gO\x0006Ð)é7}\x001c\x001aÓ¸Èê0\x0018mÉ7¢ôH¢£óLÚ`c2Cúè\x0000\x001b£ß6Ã6¢÷Ni:Att~Ö¾k\x0016©ûÀ\x0002Æ¢deBmØÆÆO¡~øñ?é6Ç\x0016~¼úé\x001e»p­\x001bÁpv.;*Ø®</`(( §¥Wß]`\x0017¯ý0K´å\x0010ÊæÌ\x000c3¿§:°$ÃvW\x0002uX´>Ö\x0003uØ@8?î)¯\x0003\x001flð/hÕj\x0012¨X\x0001ô'¸?¿\x0003né'£\x001aðQÏe\x0008«ïÉÓ½T\x001fç]¨|IO\x0001\x0016¿ý°½ý
ÛÉ!çüyuÿø\x0019Så/ïsÜ
ÓÂ§giCîz;ÿàMÉ#S¯.®¯0þò\x0002Sç&â<Äûï¿Þ¦ô3¸âì\x00005¥õ­»M¹Á
î7³	äð9¡&^Æ2þÁû×GýåëR
\x001dVÎ]ý
&ÄªàPmÎ¦\x0000j8N§\x0010<ÜÉrrÉ^ý	LçÒþãñ×ñ¾:¥P]ð J\x001fl\x0008G\x0005\x0007«¡JÓÎ2aÚ\x0017EéAÚ]sPËIu(TÅ\x000e]NüÎûÊ{_\x000eU;¹LA\x001dÎªÃ :\x0011Ò«@:¯lz©Kç\x0015\x0000ZM\x001b¼³HïVýí\x0017R JºS\x0008\x0014\x0013¦_=Ü|ÁÎ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¿üþOÌ\x0006¯\x001fÿ±Þ×\x0005¦BdÚçkêÛó©kÊÎ×°}¸¹¾¹\x001d^ìÎW]Îw$hÈ¡á\x0008hW\x0018_E\x0014ìëÙ\x0014¥özÓ
½¹Ã"tnáð&©¥Újâ?°\x0016â9nW/_(»ÿÛÃý·½ï¸\x00126c\x000f2©ËB{êI\x000c\x001aêésÜ°nßQÿãå*þ)6ïåü\x0017	ÚB©g\x0011(ßMÎ_ùu7,àÏ(gÎùòñÜiÏ/ûÂO\x0015ð7\x0011ç7wXÈ¾\x000frs¢BHi)\x001d\x001f\x0018Ê[jTp¨ºÂ©Û]þ³û(e(?ð­{ùô\x0005çëý÷Åêõëïÿót¿¸ýý_×_÷¹hÆ+SSÛ\x0005\x001cA&ÓU\x0004ñÄ\x0012'íêóbu÷\x001eí4Ñ6ëýõÍõ~zÓ«£é±Jj÷,#e\x0000Xi[ºPP?¾ÎñõÑøF§9Ô} êý\Ùí´ø&Ç7§;To\x001al*MD?½A\x001c\x000f9>\x001c\x000f»qôéx\x0004\x0001|\x001aý\x0013O~óÛãgàÙxeOªø.
]1¸\x001fßåøîøáOk7\x001e I\x0019\x0012|Rq¶ú\x0004Úïs|üè¤ì\x000eñþÇk×%þ©)Òqü!ç\x000fÇ\x000fÿ±\x001cù%]`âA%]`N;÷7u§Ã¶%N²xiòÇuàhògwi­öqrß=~ã\x0005Çæ¯Ø\x0011ãiþ\x0007.úÓ¶.ýÑÿ\x0007(¶^yüÞ\x001bc\x000e=eÕüV\x0000\x0001ÖÛ\x001c÷\x0007(6_yüîkU:ú \x0003\x0019\x0007´\x0004ìÔó¸?@±Éã7° RÃÔìnS
Oëéýþ¸?@±Éãw0\x000f|þ\x0011XT8òkÎó¨©lË\x0013¨ÐÔ\x001c'\x0011·N\x001fñ§pIý\x0003C\x0011}\x0005i6¨ª3ûÇ\x00183[\x0006¥·*cñRoá·¿Óýo¿ÜT`©E\x000c=dê
üê\x001ew5}üî~f\x0007<þ¶`m¡\x000føîá¿\x0016×÷¯ÿ6À.d\x0018-°v=gjuÆ\x0016\x001f.)ñ¾¥)÷²ÃâÝå¿,®Ww?\x000cÀãÿÔ^jS«#¨ã­\x001eÁ²z?\x0008\x000bì´\x0004u¨Nlcë#°ãq&¹}q>Ç+¸IN\x0014õfçNjSc¨-7ÄWÜ\x0004éÝ´\ñ\x0008jÈ©á\x0008j\x001bH\x0004è\x0004\x0019D Þf\x0013ö¬F\x000f¶Í±í\x0011Øñ¶m\x0013µ'j6.õ~ªs\x0004´Ë¡Ý\x0011ÐAä\x0006\x000f£^/`Î±§Ï4\x001dØ~«¶\x0015È_j\x000eoµM-\x000cîl4\x000fXFN;ç§­\x0016óÛ\x0002>¹æ\x0010"~ûåùõûÃã^	¡Î~ÄÔÊ§ [®Æ[tý\x001cõn±útqs÷ùòêê\x0000Lcê.LO¶Kè2{o\x000c gdD0!Ç.L©\x0011Ó³\µî\x0005sþ[M.§t],2¥Æk²+\x0002jè÷ØÕ©Õ\x0002þP¼Î¾¬~ÿ?Ï\x000fß\x0016·ëï\x001f×\x000f{åÏ]º¬ëxR¤a\x000eëãR
ó½C\x0015ÔÍå§Åíò|uµ¼?ö$ns«c¸±Ð\x001ah2\x0018J2h6PÅ\x001cþlçy\x0007¶Î±õQØÊÛ¥ÂþF¢æ´¦qÓá\x0011ØcÃÿOÝ»eÇq$yÞ[É
\x0014ß/O	\x0010$Q\x0007\x0004Ø¸ètÕN\x0002L@L\x0000\x0014©§ÙÆ¼ÍãÔ·ÚÉ¬äs37óH 2<"RÝêÃ(-	¿ðp7777ûÛ\x0014l¬\x0017\x00192\x0011ILKY|&åÀÖr\x0003;ý\x0005[×é\x0008òáßÿZ]_ÍÞ]§©W8'mµ¹"\Di v\x00183$<wCÏT\x0011Á2|}zðêàôpöîðìüt~ÔK[ÎÞHËgïá¸VÃq\x0003yáäA9'äÇ\x0007\x0019O«Æ\x0015VmÄéÓ_ÀTþÇÅ58
oVo×ËÕìÝìÍbõaÙoè@\x0015®ö´/¢
Z°{Fù\x001f\x0017óCð\x0019ÞÎ:<8\x001f5?}u°Íà\x0015lßÄö°-UÁi#Y«P\x000br+Ógx:§pÇ&wÂm=\x0004²³å\x0008Ô6ÆèR
kÅÓÃÇ\x0004ðÆ\x0015°ÊA½ñäZp²EZ#PÏä\x0003ôô*a
vkzËIó;¹Bv4g¨g´\nbÕS\x0019þ)ä¶En§R­¦==¢¨\x0012YSo¼´9Æ'§ë)ä­9.§Mò\x0000%eÓ\x001c/¾Ó®æxp\x001b¶0¸â9çcÈÛ»Õ\x0003¶y¬j³K\x001d#È_¢Ç§¸e\x000fÞ­KJg·'§çØ?æâ´\x001bØ\x0008·!_\x0000½èåúèô8{ûxýP=¨"wê\x0010Ò±å\x000eEDÙ§2õt|º½½8<_ç\x0010ö\x0012\x0016±\x0019Kl"Å¤HÖ:Ù\x0006Í*sé\x0000Üuà\x001bLìZÄn,1èÿ3±åK4ÁuÉÐJ,\x0013ÓÎ\x001c\x0000¡¨uTNÊÙñÝ·åçËÕ2ýdè}ºÒµÔIÖ¨Ig?ÎÙïòK¼ðN~:x·wzR/²i"±ÈNò=µp^\x0015eQÒÆõÑtö¥\x001cNìÄn4±N¦9»yiÊ²s2?ÔJ\x0013dEw\x001cÈa4²\x0015$½#\\x0014$J\x0006MÛ-#w*\x0010W#»¸!B\x000cÁS\x0019«D³àðý\x000bøô¤\x001b\x0019ÈÍ¡ô\x000bfHÌ÷\x000eÊs¹QÏ7LÂ"ÑÙOp\x0004ÇcË¤£B¬Äz4q0± ³a©8Í	"ÕOs(G#»&²\x001bìý\x000bOêÖ½\x0005SÄBð\x0006v\x001cÈa<r©UTÖðÕx¢çQ¶O{ZE­©,ÇÏeg¸úDAfuvæ.Ì.tè`6-f3Ù:0ÆYX7°R¬Ýb:\x001a\x0006b¶-f;~u\x0019g[v6e×J\x0018ÅÜZrü\x0012L¦"¢*D
Þ\x0019%9ÈaiË9¹µ\x0004åø5hXW\x000bA­"\x0012%$.6ô\x0019¬Dk7\x0011£¡O +Ñ/ê5®*Çç¯GF1·ö\x00135~C1¾4?
Sàä`¹Ù!rËj¨ñVÃ\x0018òÒ;ÍæÈS#ðÛuhI\x000fgÖím{ü0kÍÓ4±çé×`45+\x0019Ä¬};.
ÑV:ZÜÏNï¾>öÕjxã"µ©X§Cñg\x000eäz¹M\x0003êh~6;=ùÆÓ\x000c¸Þò\x0000PªQPãDU/V;º3ÓÊrêO³\x001fû\x0011
<Ú¢ú*£tÁó÷åâöo{/\x000f×÷éóïßüû_ 3Ñw^\x0012\x001eB+à\x0017CßA®!Ò|iê­|ÖøûÁüx¶7~xfÀþÑÁ»cV\x0003Âç&rh!IÈÜ¯*3o\x0017\x0010_!b÷|bæ`âØ"ÓÙ9\x0013C;\x0011\x0002¦ó\x0007~\x0007¼N4yÄ«I¶C\x0018ÀåiÎZðái'äQÈ²,'"GJY\x0010®¬\x0018ùùRÁÈª¬& Èþ¥H´h ËLÑpx>T1\x0018Y·õ$äP2´+qTÉÂÏ·n\x0019lZÈf\x0012²§,PþDýÓa9+D=½â\x0019l[Èv\x0012²!%\x00012¥ý\x0010[¸ð|¾E\x0015±õ?_ªK½\x0000å\x0006\x0005i<ø8º^BÂ
Ä\x0005?-Vè0h$L»\x000b\x0012.ÿ¶¿º»þþ·în¾-qÏeÁåÚèt\x0014S÷\x00146óÑ/ ts
Ï\x000fþ¶zrøûéäè§³óÓG\x0007y\x00031Â·óÓù\x000eu6±\x0007bÿ?8\x0000qøD\x001c8þ\x000f"r\x0003|L!VÙ\x0018\x0003q ë½dÓ\x0001ÃN%\x0010ËÿIc¬XM"Ö\x0016²ò2q$ý}9\x001abµK`
Àz\x0012°4ù)\x0001'§RN¡«p\x0006Îi»â5Àk¦
pÌwÔ\x001b\x0003\x000cêíÆ$¶@l§\x0011cm\x000f\x0012«ÒEâ%/\x0012«B½\x001bbmÀÇ\x0004b\x001bra\x0012\x0010[\x0012xµ\x0012¤\x00168ïÎ;"%)Bb¬
&q,i±\x0011æIk«'\x0001Ï«/_\x0001ØÀ\x0010Ãcµø¼ø\x0000r÷¨é\x0004y:Ä4Î9\x001aï\x000c
"«§ÖÏ°îÎßÍ_\x001dui0´(á8±S\x0001¬A
)}×ÖP~ý+w°À >\x0006\x001fåãß,f§KÎß¬U	\x000cò
\x00016XV\x000bÆ\x0007¯yÚóùæ³Ó\x0003Lé¬`\x00063fÌ4fOr\x0000Y)jp
n1mm®
@^OÙ)ÈîWYH'\x000e'3²µ4%Ù)r\x0000ä0\x001dYæÝ"@Ë»
ädÑz7A\x0013Cÿ¼ÈÓy1mn,
s#Ð©9Í
I²3; 6nùËã\x0002©ádG¤£\x0005¦V\x0003ë¨òiNY­$õf\x0014N²\x00162Ê^7âhi¨5¼p@2~\x0012oÌ@Ê´_Ð´ðÑåy!\x0012xÅT®æã	\x0013xÓ§g'MHN\x0008Q¨¼¿(í.Ç\x0017\x000eG&Náõ!\x0007Û\x0015¤÷Ò=L\x0006Ø7\x0019\Ë\x000bÎjy<ÃycÖ\x0019R Ä\x000e5XW)â»\x000fp¡	¼6_'ªäG:\x0012¾	\x0001\x0005§`½	
øì\x0017|à`'ñ\x0017ÙåÁÎp
Ù³ì«ì\x0008\x0017zÅ½ÄÇ\x0004\{\x001b\x0001/çx\x0000¯/¼»¾Xà	ænbÒï à\x001a²y´_HÝ\x0003vÁkH+-?Ç\x0003\x0007C\x0004èRªDZolÎÂË%vUÅú\x0012|\x0014ÜÓÅçjVéÁÅûYåÓ\x0002±ö¼·)ÑïB$¸qiØ
ª\x0001T\x0005Õ±PÂ\x0005¼¼±<i£è<W´A+FÔ\x0000¨\x0019\x000bê¡\x001f©Î¤ÞS\x0013<_²^1m\x001f»"µ@jÇ²H5\x0019®DÊNzú]¯­%
@\x001aFBßµ\x0017ù4\x0011AÑ([XÅ\x001bXïß\x0010jA#ÆÑ ÂÐrJ¤ºµ\x0007å£-¤»úøç%>F~|Xíøí¡rÎ²õÐ%t0Þ\x0015¨\x0004P9~ê,f©¤áf© !Z÷ÿZR°¥z´-ý¯$\x0005cªG\x001bÓ ¨T }}¼Âi6~þú*ìèëkØôýÉåÐ\x0003_%\x000b{\x001f=¢ÜÙ×pß é\x0007Ú  Æ:\x0006ËÁütéVÂ·Ña´Ù7 c@\x001bT´tÜò\x000e;Ú!©
»"4V|\PÁóVª4u`\x000bBXC¾uÎIÍÊÐ\x0006¬ýÅ_ñ«\x000c«ÆÃZhaDS à
	.+ÉAûÝÙ~ÇU\x001f×´;åe%¸\x0012+\x001d\x0004=Ûéo·V|¸FRðúà±\x0007×ªCÉR§ÃªÉ\x001b©M\x0016*«xÌxÅIª¼ìZM{Ð­;Ü`\x0003?\x000f\x001e=6
¾\x0012>²¥¯i"±|3çÓÎä\x0018Mt}Ù\x001e´ï\x001f\x001f¾^/ád\x000fs\x0003\x001fGËÙë»ÕC-[:^çã±õ|"!jZÈT(s\x0007³×'§\x001d\x001añ	í÷kóõú+	'\ÂOC\x0002§\x0012Ò¬\x0003Æ\H(9\x000eÎ@ÆÌêÐEöS[Î¡\x000bî\x0007s\x0019IK4¤YF¢ºFGÆ2¢ËLWc¥ÿ\x001e\x0005WQ4\Ö#£V¸ìt®d/Ìp.Aè\x000eê	³I3TLÃÕµOTS%Ka\x0007S)Ï¶"¤õhÈV(
Â¦É\x0015»ÎXÕ\ivºá\.8þx#\x0003\x000f>é\x0011ô¹Ò±4x\x0003©zå&O®dTã`,HTÍnH{\x0016ÄÒ®u¶Ëâ×bA\x000eü\x001aÆ¥"¶B®äÕå+é4ì=y×eï«ÁÀ¦\x000e6ª*Ñx÷É\x001b\x000e4b^1X0SçÄ\x0010Ýp°\x0012 YÏ`gXìô}ªÁð\x00149\x0018,§{ Ê5UïXM\x0005ÞÎ`û\x0005\x0005^ÀÒùk
F3ßI=yæ§ \x0007\x001b0å<GX£\x001caÕÒ\x0003\x0007ÛÉ`é? \x0007[°äbAq\x000bY]¤<bzº­°_\x0018>b\x0012|U\x0004K¿¥¸$Tf.ê67\x000b¢|m«2"y'®`)\x0011Ù'gÁ
\x0006Åaj¸qU1$°hØÏWúf êS(Lw\x001c\x000e&^xE`ô\x0012|2¹<Åüdã
¡%5Ü¸JF\x00060GW¸Éæ\x0007^¾ó¦\x001a\x000cR\x001bW\x0011¡³[\x0006\x000b8Àè21ÙÉ\x0012ó{é,tÌpT~\x000fÙ\äM»0}ÁMìpÃ<\x001e¬\x001bI`J\x0011såSÆÉ_\x00122H\x0006Û}\x0019cÖI\dù\J\x0007lòþ
Ñ=ØZ¤ó"× cÖ÷Î\x0016\x0017Qwÿ~ÚrÓà;êÁÆâ¿\x000bcÑÃ·#¥\x0004³o@k6ðbõ§z<\x0010vÒÃWdpY|4syÚ\\x000cf&9\x000f÷õcñ\¡Ã1
\x0018vºsÿª±0¬ü×_h\x0006¯G¸ÙÖì¹\x001avwÖq
'åÔ7$áñ&¯³\x0018\x0008\x0004P\x0002lä\x0008æ\x0003XgH5Wz13<Þ|\x001cG\x0001'\x0017A,\x0008cW¤u¡öj°´rÌà­È\x0008ÒÆ\x00030A%(Þªr8²vòL«Ñ\x000c^\x0006Òê|\x0001sÄµ\x000eVØ©\x0002Î0fð\x0011\x0004Ê^\x001c-Ig(\x0014fuÁ'X25fð\x0001\x0004Ê\x0002+Á\x001dIßÑX
]\x0019×Õ`É|Á&\x000c-ÊÌWlò­)\]
éO¹\x000cçÓ'®@º¬PB¯Ë:ñ!<äI\x0011×\x0005LÑ¹ÔT.È<ñM\x0018ìE>¤f\x0015MØÊ^4q+~°Ka!ØJÃnt,r±Tg¢h5W24~°aýó+T?Ø¬þùX\x0010\x001elUÓgâT 8Á>}EÅ\RLõtÀÎøÁ«\x0011À¼^Y\x00063»\x0003K6Õr
ÿÔ\x000f	\x001eaøI-õe¼r\x00076\x0018/UÆk2XÚaÃà(\x0005\x0015.ÏX±äöí±\x0002+®0Â|IJÌosí\x000e+Y®0Üzµ±r3\x0016×öM¨+®0Ü|%.m
W¤D ÇñL+;ókªÁÒz\x000e£\x000cØ
\x0016N\x0018eÀØÁ\x0017C\x0001	Ì\x0017°í'
°d¼Â_ÏÅd¼â(\x0003&ËpI¶÷%aAÊíç
®´¤ã¨PÓ;\iEÇá^a\x001a.¡Êx)¶÷²lÜfÕ`iáÄQö¾\x0001¦ýS°©\x001b7èÅ\x0011\x0016_d\x001d±\x000cK\x0000L\x0017°É2MÑ8Âæÿù`i.Ä\x0011F_dyå\x000cæy3e7º\x0019¨{\x001caóEq%®bóåÎ¸ÒÇ\x0011&¿Å\x0015ôS®©^\x0005$ÈÆá&_\x0012;d\x000c\x0000¬pMÜ#¥ÀL\x0011F_L¢&\x0008»"[«@\x000c5û´*Ù\x0017TGÌ>O}=õøsø\x0000&7©&Î/kë\x0011^\x0018h§Ñ§¤>gËÑC÷¤Sôb\x0019\x0018l|\x000cÍ,õUÁH*_ôfíTèNÕÊS\x0015>\x0006GO\x0008«Üæ®`9­¯'ö[cÀ :°Å\x0004S\x0001÷Ëæ©¦\x0005 %Áhú¥L´8jvÔ¨ùµ³ïlr{¶G\x0017ÚÝê÷\x001f¦àj
\x001fk5åýìÝÝãjy÷XJ\x001dC\x0000ñ(¨7uQÒÖ\x0019T¤\x000e'ýõÒ\x0007g³w'\x0017§\x0007'\x0017Ý©Õ\x000f÷¿o(\x0005\x0001~\x0007>
ùÕ"1×WÉjá,Éð¸¨8=7ZË\x000bÆÞªé7§ó»¥Löóoáz%Ñ \x0005\x001e{Ç\x000fËë·Õ Â:÷Â­«$Ñ\x0001pVpµêóW\x0007o·\x001dÛûûïÈ\x0007i,ðx»ø¼\<TíÙâòº\x001aÓD+øÖÕzÍe=É^s\x0001\x0015)-oçï\x000eæ\x0017 [{6ìú\x001a^ÈnÇx^Iºµé\x001ftª¤­Ò\x0014EJ¿íLì­æ
zõ=xðe \x001b\x0017\x001f­¥ö6-µÛåUíR3Q\x0008ê	¯\x0003!©ágÚ\x000b³MÐAô\x000bÁJ{VÚñÁ~÷JkC]3Ác ,Ä\x0000½(|îµã¸*YoÑe\x001aM\x000eyÎN%%Ü\x000cw{IöýÚWC¹1ÍsÓ*\x000fçö®õôÜ`ã5)ai\x0017+d\x0006kØð1q®@Â\x000bÍ\x0015ÈM Ö¡"òÎ\x0012aä_\x001f¯\x0017>ÂÃÝ\x000b>³óÇ«Åc-¬ÞQG\x0004ÕÕÜdE	N\x00060¡Û©?:_ìÏ/:ùßýã·\x0005òamz¼¿¾ú´\Ý=.k« /§Ìäôjj\x0001	úAÙÇIkgÐðýáþÛÓî¢ÂYð1ÑG«Á£ò(à\x0006>ÐÅ²qªs«@¿]þqs\x0005»FNÖ\x0004AöåçE½+& 
8\x000bj*¢Ì®0t¡\x0005çÁ.¼ýwó-¾XAÓ`¨ð1\x0014-At\x0016\x0003\x0012Þ-HZ'­ ®
¡ì~©sXÆ\x0006P8÷«ë«»ê26\x00162\x001dÄ­õò£¬DatçAü=4ó<ÙòI×t §\x0004ÁtÖ³¿uvè¯DhèÄtåYõtpçÁtJÑFo-ä\x0018ÙL'=y'¦ó»VÃAÜK|\x000c\x000b^²æ¦õîQ£Ê1ërûàß­¸º\x0003_	\x001fo¯ëÉ \x000e$·SÐ\x001c=Gü\x0015è5I\x001e¡õ·u\½\x000cA\\x001ezâ¥ñPEæ+7ÿD.\x0019»l+ûôëõí7ø`tK%\x001aZM¼_¬\x0014Å¦ïI\x0017_\x0001\x001béPÎp¤(\x001dtgTC:èlö~~º­DöA®¾F\x0014'\x0005ç	\x001f\x0000»w½Z|¨WÑLÜQvZÀuÅ,eCcNg81î\x001dÎ_mú4··?\x0004\x001ea\x0011·NÞß=>,«\x0004Ð»äÑ@/32ÒA\x0004Ïfºs5a}rq~°ÅWhàÂQ³¥w2\x0018WJ9dZ©9QÂ%\x00014Pbì\x0015>\x0018À\x000brKõdøðrz¡Ñ6Ò}m\x0010fÐ×|cp±®BOÀ\x0005I××¶\x0018â@¸Ééí\x0015À\x0018À\x000b\x0006K	¼.R×QedrÍ
IKPLHÓíá\x000eÆµPÒñÃ\x001b$Ý0\x0019HQ×4\x001bHs\x001b\x0004#{O\x000f}¸Wß\x001fí=Öø=ÄÇþ§\x0005P~[Ö×ù'óïá\x0015\x000c\x0006-vØ\x0014 94\x0019°d;µßÎ\x0001ð§-Õþ_å/\x000fß\x001f[{i\x0019Ó³åjUmiÓ¡1m\x0006XylµñêrHjê¼\x001d+czvpzºM³i5¬-­§Ð:K¶5Ä¬s
²*]\x001aê~¹Ô\x001eØ«Õã×\x001f7xXJ>×>òÎöVÛÛEõy7\x0004Åé¾ÞSA¾uoøL÷é¢qÜíÎçÝnßGe\x001fq|QÌ@4Ç÷Í#\x0004¦?Ï\x001e¯\x0006¬2CU)>\x001d \x0017§¢$×¾½¹@õ»ÙÑÅ~
7ýÇ
nv«GÊ\x0018î UNyó\x000eZv\x001a\x0012¢!-"\x000ehýáêAØXÜÕòzÆ
w¤\x0014Â4Ük5BèS¹Mç=Þ îë»Ç_¾I\PóëB{E¾¾{¼¹»­^
\x0004ïñXÒ	,y®­êo4b,\x0017G'Ç\x0015Ì\x001enº½Ä¬A\x000cwi\x0010R£â\x000f\x0013­ef×\x0019Ï\x001eÇ\x000cr\x0007^Ndæ3x\x0010ÎÑìHÌ¤Ê9W\x0011é«fõ%>¦0C\x000cÓqº²¸µ¶¡Sºä0£Uú.¦t¤+Øä\x0017Kn*\x0019-ä¤³è\x0017	îÅ¾ý o|\x0002lH>ÃÇú~foñÇu}\x0010ØÚÈ¥Û>xùzÆ²øQÀëë½ù?\x000f»wñ\x0006-\rÀc4mbrD¼\x000fÁIkÚÎÊ\x0011´p±\x0001ñ´KHd$ZÍ\x001eGÍÕW5-®á1Öæ=Â:-È÷L.Q d\-:oGÀbÄ\x001cÑ£\x000bwt9;Ý'û&20ö}Ï£++.B·\x0003KuùýË\x000f\x0004F%	\x0008Bì¤:ÔFÕhÒ\x000fò*¾ .Kßtììó\x001eÂ&[;
\x001aÔ½ÄÇp6\x0010dC¶ôÅ¥$8
/&¸±lÿøøËï@\x0000)Îø8Z\-\x001eêïm:éx
1:)\x0002KìBÃw\x0004Ür¯6ßo»/^óA®3>òIm°9¯\x0001\x0014µ©[rtG¬²#=\x000fLQâÓÎ \$µ¶ ,]
¨mjõÕx¨uáxp>ÈY7i«|ár¨N\x0019®q\x0014f<úróË\x001dFÁdácÿîñþá±þtkµ2,µCP2Ê\x0016áüÓ²³QÌþÉÅÙùÅ¶m\x0010b\x0006ð\x0018N\x0008ðrÕÞÐ/\x0010JHÍqnA\x0010ØÇpÂdLàËæÀK¹&¦4
súÃ\x0008AP\x0004\x001e#ÆÐJît§Í\x0015\x0002é+{þÊé¯»<ã\x0001hIñ1b\x001eBR\x0001\x0013r\x001ed2>ÜÚÎt\x001eú\x0001oZ}ÿ\x0008ChÁÎØæ)ãõâÇâ¶þ®
¥xºyñrÝ\x000cîçºÅñ}=ÿÇüø¼3q³A\x000bËÚª	´.@êf\x000e
{\x0012m	¼ôô\x0003ú@\x0011lÅÐÂ
·zÚÐæÌ\x0018è\¶îCcxdûScêaa±[3\x0001¶¨\\x0018¥\x00159è\x001e8­Mg\x0005É`X
K\x001e\x001fãGÖAÐ\x0001GV7&-iÀ¦³rg=û¡Å\x0013&,²Å\x0004`Î1I¿Cmg\x0002V<\x0017¦ÎÛ{÷«¿ú
/4 äÞ:Ä]ß?,êcRp£;\x0016ÔçY*\x001bbt\x0008\x001b+rÑÎ\x000eÏÎçÝá¨5-è±¨Vk¸´§¯mÚÙ_Ø\íàÐÐ¦§µ´Ï¨å\x000f\x001d[oHÔÏB-©a\x0018¸\x0016düM£½üíA{Ì\x0003G\x001b\x001fû\x000bÈþ­ÎÑÁRê§On\x0013iº:UÊ(]g\x0006ÿþ\x001cR~ûÑ4ø%ø\x0018\x0006
\x001b9ÇCßÅ|§í´ä\x0012õ :æµl\x0006Ò|ñ1bØò¨ÁÍ{Ö	rªäÊ\x0007×öÑvõÍÅgø¢(U
wÅÍêiÎÔ¬³a¡ð·Ú(\x0018Â\x000e¶wóóùÑ?jØ \x0017\x001e\x0003Ùl:%Rõ\x0003têR¥ÆN\x0014ª»uP=\x001b\x0004°à1Í\x0016
N\x0010\x000f¢«]/X¼.Áw}Óz6\x0008WÁc([:h;B\x0014¤òP
Áh
-êÑ í\x0013\x001eCÑ \x00118Ç¤tú-·\x0005±¬\x0000\x0005ÚßÙà\x001e\x0003\x001eCÙ¢byo8ÛÐîæKÁ`Z¨]Ö­
¢Nð\x0018ÈæD)¬×É\x0019§f_Adw\x0016T5\x001a¨âcð'up«Ñ\x000ck]¤OÊlª³Ü¦
ö+x\x000c\x001e¶H±:í\x0004ÌúÀ\x0012Ñ²»ÿr-\x001a*÷ãc(ZZ¤TÎ«q#ï$õ\x0017>Ùr\x000f\x000f	=<\x0006^\x0003\x00010´!ÎñZpVp\x0007Ñ¹e
X§\x0019/ÀØC®T\x0005M9RòÆóRítöà¹¯â\x000f
ý1¸ÓÃÑòöêæ®>\x0013PØ@à§Y&Ò¾@~[ºP\x001cï\x001ft\x001fî\x001bl¹ÛÃ`6ãHËÝ\x000bë^¼Ù\x000bNòLîIw}@=[nù0
\x0017\x0001²9Ï\x0012
Â±~®×ÝÍ\x0017ëÙrÛálv4XËÓ¸1ét\x0006°åæ\x000fÙò=\x0014²A+i\x001a·ÈJiÞÎsC=[n\x00001
t(U\x00197Ê½\x0005Áý\x001c\x001e¶ÅåÝå\x001f¿â=/l÷¾yªÝ¿~XTß\x0004¡¸ItÔÒºVÉÒ±«³È¶\x001c¼ö\x000fÏç\x0015¬Øí\x0010\x001fcY¡1\x0010+ìä2Qi\x0012TNd½}P?<à\x001666x\x001c-î¿\}¬p\x001a)\x0014Ç	\x000c\úçH{àÜ\x0015©íjÌÏÞ\x001fþÇÅ¶\x0010g!´\x0010Ç_ðáæz!\x0015^ö@\x0005Hl¶\x0004?[¬Võ¨à¹s7\x001chC³2}tl|êlC°\x000e\x000cÌOOççoêá¯Õúm\x000cs\x0011ÎzHÉK\x0010zÏÌ2ôµ\x00060kzÚb"³æ9È¬\x0005÷\x0001¶¨2÷§\x000fA
\x001eÝêªûGF\x0015îV¾ù_\x001e\x0019.@të\x0016ä¯?!X¯[\x0011û¿*óÇÅ/¿Çd+°ø8ZÎÞ-\\x001b\x000b\x0017I\x0019×\x0006µ>è#°J»t¦ûÖý`ön¾íÚ¸Á\x0007çnx\x000cçóòc6nù(Ó\x000eâxÝþU5\x001f´/ÅÇ`>\x0019\x0015]ÏX¨>¡\x0005¥\x0002¹\x0004é?ÚßÚÇ÷ùáê«úN\x0016¢Z\x00173ï\x0016T·×QP×Àæ\x001e(lAn¹¥\x0014
ôMÇwón	nË_\x001f~ù\x00140¸
ß\x001a\x001egËë7õF$WùEÿ@äÛ^ñéHuo´g\x0007o¶,\x0002§!.péD[úp\x0019Åé\x0015\x001e´Þ9ª×YóPOgÁçÇ_ÎÞúß<Ör;qÃãhñxy]]#\x001d¡®%äTêà±²\x00162\x0017 3§p\x001aÝ­X2¿Ø;ì¾Àn°A²óÙ/TÌé¥\x0014\x0013
£â¤X+:\x001dúÖ;l\x001abzø\x0018\x0006Éd9Z\x0010C¤\x0010·<bÛr"¯dK_\x0013c@\x000e;â\x000eüªéSRÀ @Ãìf\x0002Eà\x0007ßí\x0017oÇûúuuý\x000bfCA\x000c\x001f\x001fÍTþ«OËÏ³wéªG:eP/Ä\x0000¢\x0014\x0014J9°üëµo. `ÿÝìÝEú
vhõìP	Ä\x0008NsÐHrÃW­|3çáì¨J%Eóf}\x001c~ú\x0011à]ÚÊ\x0015ïßt\x000bðûoëðÿ5üvùsÑ*Å{»\­ª¡L\x000csélÈ7&XÙddqº\x000cýöàôt$T\x0016­ZåA\x0003i}ÃmCäæ\x0006PàÎ´¶¿´\x0016\x0004¬ZEA\x0003i-¤ä$»($]
XM\x0017	¶_¾`»v\x0002«¡³\x0016>ÆÂ:\x001d¨GV\x001aÚH¹b69ªÐö.¾Ú¡5\x0002»à	\x0013ÁjêB\x001bâÀii]­ÄÙ7i*,ÆÏ4]sA±
\x0010 \x000c´ÅQß\x0017éºÅ\x0012G\x0000\x000cl&\x0000ìfÃ IÆ¦\x0013\x0003Wdcõ\x0000º·úËÇF´|?\x0019ÝëÛÙÇÙ»åÍ¢:µI&ç\x000fv\x000báKgPêf ãZN´³
\x0011XÛÃãÙ«Ù»£y÷N½úõòæ\x001b*òAr\x000c>öà¬|}s3@Ã\x001bEe\x0003]còeWL>+¥5ùîÊ¤=8#\x001f\x001e\x001dmQX3B\x001a>Æ0&?1ä<±`\x0004u¶é\x0014Ï®3`YÁxýûå×\x000f\x0018ýÜÆØ\x000cKÍ¿|\x0019P­°{£SÈ%jK\x0008¾sM½×\x0006Ìß¿ßVÝ 6ñ´É\x00053´ú+\x0005g¹®Ð¨µ\x0002;ôñ° éÅ²Ñ¼W]¶B]¢viï~¿`\x0007®á\x0001\x0011å\x000f¨
®\x000b)8Ñ>\x001a*ôSétÍ\x0002>t\x0017'\x001e¤\x0015ÿ\x000fø]\x0017¡ÿöðám\x001d\x0007ßÝ=ÞZÎ0\x0019;-¬j+,ª3|_\x001b@ØÈeÊ-Xµéò\x000eß\\x001c:aZvZ`[\x000cÕÃ}üý·ù\x0002p¤\x0008Í#Å»åjl\x0015dÐP\x0015M²\x0014HI\x001eV¤*\x0015mûó\x0004ß\x001dn\x0011°Ò«oËxª_0ª6ª>ß/nªa¡×U>;èh\x001d\x001c\x00006ê\$bÔ½GÅïçG´¿^_x\x0011\x0008jQø\x0000IÃúJ\x0013 Ü,\x0000GèEßM\x001aS
O\x0019Õë>?qÝâ\x0001èÕo\x00123\x001eàûÅåm}h
J\x0019ò\x0016åÓ¶ùÂÚB¨ÈªjÙm¨Òsþêà¸ïÛÝ['\x0010¿ÀGKpïúÃrñø½U'.ZþÆC+tÜ©¼¦PðÙg-
Â½ÃW\x0007óÿì§ÖP6 [µ\x0003c¨!7"WTò MÕä +6ØÎÌ´AÜÞ?;´_P\x0004ùªÞ\x0013H\x0006Ë\x000b:¿x«"Ì
<\x001bJ.WÝaÊù)8\x0001åØÂ¿!²\x000f·6b23ìÕ/\x0015Æ²fÉUy\x0018rÚ¶²|ús\x0005SrÿEÉF°Ý÷\x000eóYòTÎß\x001eÔ\x0000a
£\x0000}$û\x000chH0Ñ§Ü\x0013ïº£\x0019C\x0000ñ\x0012u\x000c`:Ð¦	dªss÷äB\x0007Î\x001fê®\x0008è\x0005ücqýÅi\x000f,Ñõ\x001b{Ç­k-¶jÎ%ººSr%\x0017æVqIùÐÒl\x000bR­HNFK³\x001dÎþÛÕd\>>LÇ¢\x000eM(Æ«"¸»ÎäÍj2.\x0015\x001fX \x001e\x000c{¿Þ	J-ÔD\x001e3ÕeòªÁB.
\x001f:dÊé¹5x:[\x0014eÎÈóv°ßý\x0017ù\x001då§°:Ff³=PIzø÷¿\x0006DU)¡¨ý	6N\x001bi÷\x001ew0Û\x0003¤óîEÚÈ²£ E\x0008\x001c¾7éH¡\x0002èë\ÔÇº\x000fb ! §ÜHHÏý\x0004oüCªyÝ\x0015¹Ã\x0010a?S~$"D73!\\x0005gBÏÞÜÉÖpx×t>ÐáíLþÒÞÒ(R:!»×ñ Hð\ñ1\x000eR²À¨Ì\x0011XT\x0005RwÇ\x0006@B`\ûqÓ19Oü­U:ÃfÝ]_ä\x0005¥ï\x0014¶­@¼n?â¥\x0017\x001c)ñ|Tè½P/½\x001fÓ\x001a¡2\x0000ûo]ô¬\x001f« ±£Ë0\x001e¾\x000bÝ|îûÊþÇ\x0000XÑ¨£¼»Õú¿Ö\x000e*¯ÐV*«Õö\~éCw¢lr^NN_uóý*®äã/-é8\x001b¢\x0016ÇÙÏ¨Mû°³w;§:}Óùñ¼ìÊ»«ö
õ@Dú¶n©\x0017­)´\x001b\x0005\x0007"zä	r\x0000¢1~ûíWÿÆ\x0010"|xNI¯z[áE¤ë\x0008í£à\x001eÈ\x000cÉ|÷Ý
\x001eéhôê`o~Þ½9¯îôÕ\x0003ÿCa\x0011>Ò\x0004|}·ú÷ÿW\x001d#\x00130íHZéðÂd[\x0018L¤\x0000¹\x0008[´mg¯OÒ\x0012®\x0001
Eú\x0011°cp\x0004_\x001aA"7>aÑ\x001dI.<\x0018	hV¯¾`ô\x000e\x000fH\x0001´\x001e\x001f®kÕ®@£ÅÁí4j´ø"\x0001j8\x0007\x0006Ú¼tÀ½_\x001f\x001ew£ÙëÅê;A%AQ\x0000eµüx}»x¸«]#Î)M\x0015Q§ù%ÄÀ\x0000*Ê\x000e®ôÑüôàÍáñüü¤ñ2¬V\x0006CIP±\x0018°bq~üâöcu(IEGéäiÇ³4ºTÎ\x0018á:ó±Þ%Ä³óùñn\x001bø%È[\x000c#r,> zx]=ûà>ô\x0001ôHéø\x000bEhc¼´u3\x0007§G`îÛÝ×\x0005ê*~-'W8j~\x001d\x0012&\x0006Bó
k¸Î(îVQ\x0001Ç=YÂI¡éÜ\x001b¤¶ä\x0019²w¤ïÛ©+0û®\x000c¦\x00039H_5.r:V\x001a\x001e:×£8»«\x000c¦³\x0012ô8xÎåd\x0006ã%\x001dDÒØÅ.\M·î 2xÚI®\x001b\x000fàßÓ-\x0005ÐÚÎ³f\x001f]¼´ò\x001a¯~a[Ä\x0007ì¹'É5XÜÜ
QÖ\x001eYÉ@Eû\x001aç	òªÒ)©sÕÂ¶\x000bÎÁüèdËÎÛ\x0000Â2£ÆBm*54\x000b97+Jî\x0001\x0015á\x000bß\x001dê¨#ýä\x001f>}]A
¼,øõ~=Sê7`/¹\x0007sÞÓ\x001eâÓÆ±\x0016Iël_1Ç)Ý\x001bp\x0003\x000f*¦Ü\x0008<\x0007òrù~'Yc ¢áÖïQ\x000f§a\x0013ÇÇ`:ë8òá<Qá¥ä¼rhÒ0ïó7}\x001bp\x0016B
\x001fÉ½z³\x0018 1\x0007ý8)¼kQÄjx\x0013ÁnqÿÞ\x001fÍ·\x001cnô\x0007óéçfÏ·¡Ó´¢»Fëµ¡\4æÆ\x000b¢Sú¥U°q·Álê\x0008-¤ñä¸sb\x0013¥«[çá·íÎ<Æe\x0016 \x0001·\x0019\x001eçËåêößÿ·þR\x0019ºÊ±ä»ÛtBmæ3²³ÃÆù<Í\x000fNk\x0010
L=x\x000cGL\x0007\x0002O\x001buÁR³ítôà³Grø»&ß\x0000DLIÒ#G1lO¤Q\x0014/¨B¤ªsi:K\x001dû\x0001ù\x0011åòVEæùÝãêî±Zk7Ê}nf\x0015@<:7BLK6;§&\x0019æ®Íã<mÅ'\x0017Ý§Ké°Ì"¸Lñó\x001e\ÃÂ\x001f!Lô~µäÅìôîëcõ	ÐÅ6/\x0019H\x0019¡ÑpEÀ¨
Ú\x0019/zz\x0000É\x0003ÉìüÇE÷u|a÷mv?\x001dòóLvhÁfæÎ\x001fÆ\x0008Òú×1t:ecØC=L\x001bwÐFÌ.\x001b´ÇÊm£\x001d¹»F\x0018·Ëqmö8Ý	Î\x0004wÒä#£
'\x001a\x0008ßh0\x0004]{\x0014(³\x0005=Ù\x000bøãF&Ç=¼ÃÅ\x001f!ýu\x0015Èÿç¬I\x001du¤M6 8«ÃÖ4H½CHhöfþÏùÖ¶»åm\ûmÜnÞ\x0006\x0013jrÐ7ý\x000c
L§å\x0011(f)¶\x0004¦§¼o¿ßÑÛ8OºD\x0006eÄr\x001a baðKkô÷\x0007¿Lh¿Ì¡\x0013MDÊ&ÐÑJ\x001eÂçO&ZÈýà¾Ó\x001bëf±£#^Ðë¤}Xñ²¼lú@½\x000e6PÖkû¼K}&\x0017é%\x000f³³´?¨n6i%¶ìÌ}"mÐ¹"(Ûþï
1ç	ýà|vvêW[ZN\x0012µV¶I
\x001cM\x001d À.ÀYaQ°Ò\x0008ÑwÅ4B7¶9mn<´'ÐäsB¢¦«¨(:[ñÔC«\x001cë4\x0005\x001aR´¡KI¨¼}®>\x000e¯0òÆ¬\x0013tÎÿê:î':çGÉ¦<]®;Y­PÛ6µ@æáÖÐnó¡%¹B>ú\x001dQC)s\x001a+ÇR;kII-Q\x0007:l\x0018nô\x001b;Ë-\x0007"[áÈ\x0016CÎ#}VÝÎÈ\x001c<0²¤Ú\x0006¡:å¸j©ÑXï-:ýÅKøcCreñ\·õw\x0002\x001aòä¼;'\x0014ªñî+8:ÝùØy}¸Ö^¿'\x0007î§W[L7¿l¿þ\x0016AF
w:¬7ÍéÃA\x0003
¢r»~	Õ~	µÈ%Æù%È¢§wàz3ï»KòÇ¾n¿ÞÁ|JZ \x0000oïRÉÄ'cßïª
}\x000bÓ~\x000b³·0£©Âb5¾æU\x0011 Ì¿ã·°í·°;x\x000bÍâ»N8I¥JÎKn¸\x001c*ê@½\x000e­\x0019\x0005ü\x0016\x00114\x000e\x0015ß±à±%þÔ_\x0018Pù\x000eäVD^þ9Ä
d£SMÚ\x0019~¬þý¯Ûÿkh1(N,E\x001b\x0006ÊÌ³h	V¤uÜ>Sÿ´?üãôàøà »<³Ð«&½L\x000fõ$¹bÜºÑ\x001cE cgðº	¯§Â;ØÜ,ÉòXÆÂ[\x0007gÈTc£!ô¦Io&\x000f}PeèÓòeµ\x001bî:§¶TÉ¢·Mz;yìK_´4q\x000c5ìJì,\x0005êt§×<Þ5éÝôEË¢)1
VâeÉú¸ÓYïì~òÈ+¬¤äyCÒ\x0006Þs,×-â<>4éÃä+-aè5Ýc®¾³\x001fç(øØSám´Ü-(zEå6 à\x001axè;ãÏcè¥híTbòØ\x000bYdÌ¦^V>øàÅÙå¼­­JNÞ«@ÈòH#ÜÓÉÑMÛ©Á-#'Û\x001cg\x0004åXy¡\x000c\x001dÅ|\x0010uE»5¯Fá·Ö­¼pçdtæ\x0005% x±;½-\x000f\x001bô}NjM}5yêCV\x001bué±õ{¯Övg\x0017SÿR\x001aTóëø\x0003x%tùþ\x0006\x0014ÒÀC\x001e¬¹\x001d©¿VÚSY\x0008ÊC¿{JîN{\x0004Jià\x001c÷\x0008H3·R-n¸X\x001dÍí©ê\x001bkëó\x0006«¨y®³ãpf×fvSÆ\x001a\x000c|\x001ek\\x0004ngB\x0005<É ïn¤]#^OÜ	àºôø~èù\x0006%ÍéÒ\x0011CªÎ\x0014¡èÒo §é=\x0005½Ä_\x001dH\x0019Y4,·,:e,êÁÁKb\x0012ÓéÕ¼?¾¤Cëû»GèR\x001féV.PDÊ(hØÛ\x0014\x000c(Ùy#J§Õ÷'\x0017Ð$eK¤¡c\x001b:N\x0006A\ã¬ÏNÝz£NeA*ìZ\x00165\x0018ð±Ô\x0012\x0004\x000er
NG&¡I+©µê\x0014j\x001aL-ÛÔrÂX\x001b.x6\x001aÎ¦y¨<Ô\x0015»ÕÐÒ[L"-Ð u	|yzP\x0010ûz¹ZfKuÛ\x001fè6ÆÍÐ¥v|6\x0012«@Ä¹üôð',½?<8=\x0005}-ý^µéÕ$z\x0011uìC WÐ\x0016]³v\x0003w-
1±QôºM¯'=TÉóØk*TNc\x001f¹:v\x001dFÁ6¼
Ïe\x000e	^Q\x001f_ÐÍç>
q·CïÛô~ÚÄÎ\x001c\x0012ö*ú4grx¾ô\x000eI'Ô.ÿv\x0010½ÀKW)Ö\x0006zâæ%É^²3 \õþ®¾%_Ù­óèbeã5\x0017w:\%º¬
¨W½?ÙÒ¯¼j¿þ\x0002®¤\x0010\x001bÅ\x0012\x0002Úê[ò£Æ½i¿ú\x0006Z^ÂÐÆQÓ'¾$A÷ÞR
{\x0001×~\x00017ù\x0005¤.:	Ø=gìGCªó4ò\x0005|û\x0005üä\x0017°,äÒú©z\x0003ê\x0018%ßéÀ|Ð~0ù
`÷Õô\x0006\x00114@ñ
Ê*Ð±ó¶yä\x001bÄö\x001bÄÉo¶Ý¬ä\\x000cl\x000ck*\x001bá{/\x0007½\x0014­\x0017hiÇ{\x0001cùÖ\x0005Ï½i?AØí$í½@NÞ\x000bôº]Az\x0017<Ø\x0007Ò¡_nqÐ\x000b¨ö:VÓ×ñ­%ÕQ7_@·\x0004Çmf*B)K\x0008.×Ñ¢ÔÃøþôÌº7\x00001j¨\x0000hä«ðÇìû8Kd_j¹Ajò,ØÒuæ\x0015Z°ye×a\x001c²|/fé/Þo¹Ü£\x0005Üc`U\x0014t\x0005e­ñt\x001f¡ªLß±3æÑ í\x0019Z#t\x0016þ8ÖãDÆ:´Ïæ­à$ç\x001c\x0018Û\x001cWO¾|#8CSa1n.@ÝÑ\à³à-µÍ\x0005åÆÎÈL\x00150
¡A®*ã*ñ\x0012þø\x0012\x0015[!ÿp\x001f"Iûû\x0001^©xR8(\x001b¡Cã\x0010ÕùN(Ú
9û\x0010MmÏ3Ëð±
\x001f'Â\x000bÁì!»2Ho¸PÍBTlwôF´è¡mõ\x0014z\x0001BÊÙj\x0007h¹Ì"\x0001´íXßÙ\x0013e\x0010¼ôHØf®,.f,N2Ë×\x0005ì&Â£Æ"°÷,`\x0006±±.=±LÉ,ß\x0015ô³ë6»ÈnJ_Iá¨\x0006Ýzêõ¢D·ØÏ\x0008rÓ&7ÓÈuY¬@.\ñm°èN`\x001anÛèv\x001aºTäàØ\x0003îi³¦\x001c&ïÝµÙÝ4vèËKÃ®BÞå­ã&ÐÂt*\!÷mr?\Sh
=É
s|Ln¹Ë\x0011è¡\x001e&¡C\x0001I×xÚó èÖb\x0018®Ö^\x0000ÇÅ¤\x000f\x0011T{3}d¡BèÍÅøõçCð¥ÍÝüÖ!m\(7*s+>ûðÿþ×ÿ\x001e&E-£.k\x001dtðh O.É F§¢%9ä³W,JÝíìÒ»¨ö»¨Ý¼\x000bèBÙü.é¸\x0001¥\x0000ø.Üà\x0004\x0006¿KÏw1ë\x0019
·¶BfS¾\x001cúÓû\x0003\x0004%¸÷»èLÇ\x001aý*iN5üddÝ¼
d8±Ü\x0019WîHË+\x0005òwÿ6jómÔÞ&\x0004tÔ_,\x000b÷\x0006¸¥yfú£!Õ¯#6St\x0005¥è>Bñjú§¯¿,êK×¤Ö\x0017	(¦Ó1<m\x00124±¬í,\x001c8½ÊÕÃãýC(MZ\x0013oª&©ú+ê&©þ+&©ù+Ú&©ýkÍ\x0015epEÝ=>`¶ÆÙÃìÍõê®^Ö\x001dåIØ\x0007$êHÖÝ[gÊ)µûøäâ\x001c36ÎÎgo\x000eOO\x0002ï\x001bÄ%\x0000!à/|)´FÌF\x0018\x0011¬ýË9x"\x0014ÝJ\x0007Ëd\x001f-7o÷=]+:{fç¸a®ÀZÛN\x000f°\x001bµN	\x001bJFc\x001bOWesäÙqÚW\x001aæî4Ô[b¶º5ØvÊ`\x001b\x0018a]¨éÊÂ)îNfG§Öõ`lÓÂ6\x0013°A+HJ²\x001a\Åäç;_k;ÓyÏ\x0011ÛÂ¶S°çs(í5<ê2vg\x001aïpl×ÂvS°à\x0008Q\x0000m8IR>ÅDwF·Sû\x0016µdG<K"µf=ídG\x001ccëNaþáØ¡\x001d¦`\x001bQ°UÃ\x0001å¼zÆîL\x001aíD\x0013\x001bÚ\x0019Æ\x000eR*s;²\x0004\x0014çËÏ­H'[Ør\x0002¶·Ãp^\x0015\x0019­àÛ*Ûym>\x001c»µÙ¸)
èú²Þ¾Õ,\x000b\x001aX]\x0019×\x0018=\x001c»µÛ¸I[;¨zÎí¸¼q]2S·6\x001b7e³IcIÔ ÆJBfAâtJè
§n?7ÉüéÒá9\x0008Å}T}äÜy(hÞ\x0019vlaÇ){MrH4c;V¤ô¥Ã×Ç±}Ëüù)æÏ*E¥¼Éò|\x0001ä*î_·Ðû@?Êù?Nà\x0006iº¸\x0012,?Ü(Áè\x0014¦\x00180ÜÆa\x001døÚ#\x001d¸$büjy3Û_|¾«7è\x0004¶wÿ0 	|L«ÓPÍÈWo.¦¿¦"j\x001f¶§\x001b\x001fÍöçï\x000eá
\x000eZí¤r«^E~\x0017ß~\x0017¿wq\x001bóú`aBá5¢ ³\x000eQç®5;æ]¤Ç\x0008]ßä¦\x0008|yz}õéîqX¤<-Ñ¬CÉéê¹ßaÔ$\x001fÅVw§ûoO.úäxí· 18.#5wBNÄÜ®7jCÈB»Îþ\x0007\x0003eX&\x00164Y@üäÊ£Î§n ît³j
ä\x0018«ò¢±/±\x001cS1
ñzq÷¸\x001a £\x0005»²%¡[_Ö8DÎd\x0014wûW1×óÓmêYÈ­×6\x001d¸á\x0013¸¡Ãhö²@jæ$7\x001b®ós\x0000¶\x000e(ÕP¢
/1Sãýâþ~ñU\x000bß-n?Ô£\x000b8ñä\x000e3J+\x0012\x0018w!r\x0013Ð)Ìð~~v6Ã²ïæÇ¯¶ÐCh\x0015v¤rüÁX+üq\x001d±Ú_ü±¬\x0017\x001dü1C
!¼£\x0010Õ¼D.uEíâxÕþü\x0007ÛT2·MÿÓäÆ?\x0006ON&E¯s¿)\x0018s§(	D£"èDðËä×¶b{àè¶î\x0008\x00173¤Ãé¾\UÏu\x0010ÌG'×¦A\x001eõ@}?!¹¸_\x0015&M\x0017ü¿á¬?8í{\x0007ÝH£Oï [iôcßÂ@w¯<y@PS\x0016¡%«éVI\x001dû\x001e\x0006¼3;x\x000f¸&ÏÊ*ÞÃzÈ×µN³ò®hÊ<ü{ü|µùE®¦¿²¥\x0013*(®P\x000fäô\x0002ùM ¹Ôð&Í7Yì`DIýÑ}(ÛÁ\x0012¦[1fÊ«\n¾Êå\x000e>R´ÚA·0îµæÎE=G¼GÀ¬\x000c¿\x000e"@°Â7\x0005pÒÞöøÇâª\x0012ÞxH\x0015Ì=erdªT:ez\x0013mgw©gO\x001bÛÅ?çûýØ¦m¦`Kö\x00137V£"·#_\x0013º;öÖáWrëhÜðÇñÜÂ²ÖVtPÜ+X¥sãñîìd?Û:¬l[s§ÿ<üñ%\x001e¡°²mQ]ÓfC8I\x0017F^«&
\x0006+[úÎÆHxjÂ¶äºu+'\x0017ëç¬5\FZ¿Déá7×7gï\x001e¯\x0006ô\x0015óæ=¿ä¬4×¹Õ\x000fè~w\x0010¿¹8<z{ðnöîbK/Y&nT\x00001T$ö=5\x0007á<GI¯£·(hÕ\x0010»u¼¼ûõ\x001b*z@\x0007¹,äýú\x000eS8$]ºø·½4©×7@\x0006\x0002é¦lr'=´ç/l\x0016AÊ|8?<>ÿÛ^\x0007G ×ýú¤3C£I\x0003Ú\x0010JUÓ$ïþ!\x0018\x0003ú6D+:\x0012Èëg,\x000c4@°õ0AÑ4D)LÑI0¡ÈÑA0ß~YOd{P¬gïú#èç.zh°)]\x000eÞ(H´W86^«\àþe;0´pö\x000eßTî¼çºûðH9*/7³ÎVé\x000f}\Ø\x0004¹ÒxÑ\x001ecaãÉß\x000c2ÿtI?§é\x000f5i´õ\x0018@Ë\x0015Ç¨\x0010\x0017\x0000	På|¾\x0004ýÃé|iÇÛLu«âÄ2A/;ë%>íoâ\x0013úy6\x00060MýMü:@\x0003Ó\x0001Eyé É_rÇ§\x0003Bc¡Qjñ\x0004\;`U6\x0000æ$\x0004Ü	_iÍ>\x0018Ð(*\x001bOkÄä-\x0016ÖH¾\x00175¢®Ý1i3z©Å\x0018Â ¡åe\x001eBkb\x0013¡Íê"7£Ù	!4ÚÝÌÔ­!tÛ»\x0008\x001f\x001d|o$L®`&t1çî`\x001d§#QZÉ\x0011£è\x0005Uo¥QÙoMÔ\x0002\x0003F1NY)ß¿^ýñ Ñ4J+ [½ìÛÑ\x000cÜ\x0018E\x001cC%\x000c\x0002âÖw´ Í3Û+ãNu§æz\x000b\x000eÚ$êÁp^Gê-#4/S\x0008\x0007¡þLçI×b*\x001dôI4éð¦>dºèiú\x0005\x001d¸\x0004\x0017\x001d
÷Ã¨/¿]S°ª\x0015¢:øp÷¸X}èõ
`mä¥a\x0003t±E×@\x0006Úá ¾·\x001bîàÕÉÅüôU
]¼~8\x001dt\x0019gë\x0007Û³m±Æòþ\x0011¶Y¿\x0001xé%Ãp¼¨"%H	¨¾Ègd÷ -_v\x0000]²qÄà®\x0011
\x001e¤/äÁ3ÅìÁ8Çû|¥\x0017Ø[M`ëä¶{u?Û[¬\x001e>-on0´»uy@v²|P\x0019ù
6@9yÆT\x0014Fï²|g³½ùéùÛ££În\x0016ltâ]\x0006\x0015!p0\x0019ØÛ\x0002,·n'UÀî÷ÇpyÀÐ\x001e®¹væ·W«»>J(-¤þ
\x0012ÔQ?7y;ÆÑ¶\x001c­ÝòõçÇé0ÙM÷Q?<ÊEëã/ò\x0010Vò@#(EÖ	O\x001ex\x0000Õ3në<[\x001e¶®Ãì¥\x000eMu\x000eÝ;¨NJË2}ñ÷åâ¶NEA[¢³R@ó­5	\x000b¶ØðO³¿\x001fÌ;G,Y\x0004³k°´ N5¢¤¯ûpw{Ý\x000bÌ5¸Óh¸UÈJNé;Í>Ùöy3ðüøüäø°Y«&³V#uÈt(Ï¾¬óR\x0012³[+µÌ"6²»9OÕtla\x000eÌ\x0012×mßÖ¼oGy2ÒAåk>¿hó(§¹²eûù0;JÙ)¯¸y¾ú5n¯i¹¿\x0002©åjY¹Ü­	Tz&¥t¹~.ùlN\x0011)\x0014ém¾\x00025©Ó\x0003^í[\x0016U\x001eS·\x0007iLÓ«_¯Ð\x0005LªÐñÁC$\x0000\x0005\x0015×¾S\x0016¶å¤ç§è\x0007aÎ\x0005ÅI§µ??È[ÿ\x001dý5l	~Ü\KCcHÐæ\x0017·÷\x0008¦Ò×)évs9\x0003Í:ì©\x00036\x0007Ùt\x0005lþn~|öòäèð§4]v²Í\x0002Û\x0006!Ë¿\x0008Î%â\þ7â?â\x000f¦éá¤}øârqµEzcé\x000e8Îº@\x0016ã¡O\x000e°¤cS#¼Y`×½Øï×À@<»RWÑxõE\x001fè\x0016\x0011h((9ÒvÒ<ÍÕ¢I¯õû4cj1m\x0006el4%%@ØoÚØà	\x0017K\x0019+¬¥KÖ\x0008½³\x001f\x0002}Î\x0003\x0003\x00055\x0018èZ}øñå\x0012'26mnX÷×ËÕõÝÍöÉ\x000c\x0015ÆÊâdÖ\x0011%Ë\x00135²6A+Ào2±U}pzxrÔIöÃ~þ$.
ùìß=~X®®¶\x000fWLçlPÕpT§s¶\x0015n
mtbs­û\$ÞuÿÓbÐJz J\x0007àÜ2N\x000e\x000cí69¨Ø|Ãñ\x001dÍö$\x0010UÇ\x0006Á±XØPé!±iº&\x0001¶'Ól\x0004Ûf\x0008ªM«\x001c¦\x00056Ê#Ol&[z¿oVÇ&¨u¹CzNMµPü¥íY\x001f\x0006ñw=\x0014MÂ*\x0005Me4É-
\x0013cÙ¾Þ/¾J<^ÁÕ\x0007ü:\x0003G²z·­Oaø~\x0019b*³\x0010Ie)¹³fÓ¾ë²%çØþüù«Ï?üsqäT-n\x001eV=TÂ³ðrÚ\x0011%\x0011%*¸~e«±«ç*ùSgó£óÎ\x00044û³ÓWò±yó´¶¶w«ë\x001e&@Ð!·\x0012\x0000°ÎRÚ¶EÞ.s{rqz~Øý!\x001bl\x0010\x0000ÃÙ\x0014UÆ\x00068\x0004b3:0î\\x0000}lÉ¹\x000f?¯ûTXpî\x0003\x0006_\x001b\x0018J¾øØó}\x0008$<\x0019±ÁÎ»¨¥{këBØÄ¤ó\x0012ü\x001eSÇçoº¿p!5-R3Ts&Rôi­äë\x0000ã¢¤M{ßL%õ-R?ÔZË¦1µ9}\x0013<\x0013J¹\x0000ÙÍi94´HÃ\x0018ÒÆòV>W\x0017SgÙÅÄ\x001bÎé¤±E\x001aGFRx^\x000b:Ý\x0019o·'ô¦3<\x000eD
§û\x0011+Jê{"Ud2\x0013i(cjw1OIñIå(RGÑ²\x0008\x001dùØ¥·º\x0018w·iÜG¶¬\x001ae¥ á\x0012m ÒJóÔïÃ.@u\x000bT\x0000Åæ¶¼_ÚÜ²9FÃC*ý.¾jS5ÆBUõeA9úø^Ë² vaø©±4Ú1¤ÁRÇtÐÃ\x0004aô|9\x0007ë°y¨\x001aEêZ¤n\x0004i´.ý#THú¼ô£#\x0015\x0001\x000b\x0002í» mmQjÌ\x0016úu4¦\x001aj%R\x0016\x000e°É\x0008ìÂðëÖ\x0016¥GmQa\x001dw\x00106wu@#¥y3\x0015»0ü¦eøÍ\x0018Ã\x001fsgèQ4|õJîbE95£Ìi"-®\x0007áNs±+\x0015xõÃHeSb\x0008H%J\x000cý´\}¼]Þ¯¦¶0Êd>½,&?Çôutì~sþtpúæøàl{T\x0003O7ñô0<­$¥~Ät0cC/)Ãßº§v~(iÒ¡t&«
FÐ#pà\x0002ÃM34\x0014Î6áì@¸d{rûÐt¸µlÏñä±\x0013qóø=\x0014Ï5ñÜ_
OÇÖÄÃg^ð<óxÚñÑBºMOhèØqõEY¶axé\x0014iyaÄÜ,\x0010# ´\x0007Âx\x000c¡ú9Ü}]üúØLIY6Ì¡ªR\x0005%`@³SpÜÆ2Ù¼dèÒ!\x001cúsH<©\x0017ÉïhèNO.þy\x0000y²Û-[\x000b2+û\x0011Ë\x001c~D0XÈ\x0008\x0006X sÝ\x0013ç\x0003ø-\x0004Êüï\x001c\x0005ÊìGÐ\x000es1\x0000!\x0008¸`F\x0004Ð\x0002É£`QÆjÌ(P`«\x001fÁ*ÜP\x0000\x00012\x0008A¥3NF³q\x0008äÓ\x0010\x0003\x0006\x001eAº3w,A\x0004ÌëA\x0004tdÇ\x0010ð5WÿT0¨
à1ï)O\x0005çø;Èß¡Dð*\x0018"´0tT¦\x0005¡ h\x0011âH\x0002ÓUL\x0005û\x0000!5\x0002Ï\x0004¯GÎ\x0003Ya\x0016$êºÁT\x0010\x001a,\x0004"hÇfÁûf¡¤:ö3x=#q:Ê\x00171# Þg(§<\x0006!%Ye@rÔÐ0h¼\x0004\x0002\x0006\x0005\x0005\x0019pc\x0019ÒðÉ:ÛD½Ë`6H\x000bÅl¡£fó8vYBôPÖ\x0019§?ÍDC\PVY'¸v\x0000
ÿÄà\x001cÎ\x000c`\x0010605ÏÚ
uýO\x001f\x0005Uï<\x000câE¶iUÑ.\x0001uñã¾\x0004DòTu¹4\x0003F!Ùm\x0003äw\x0017q\x0000!:Ug¤Ç[dD\x0003\x0008Á\x0014g-d\x0005Âºò©ï;\x0004Ñ!Ó\x0010\x0002}	Ð\#¯Å\\x0013%¯¯Á\x0007¬ñ@\x0006	¿Í\x000c¶0±\x000ci-©*ï
zàèü) DJëR(Ç6R»\x0015x}ªÊ>ù´\x0018\x0003Óp]\x0019\x0014\x0003ÊYbà\x000cÐ~4	"\x0003Ä6ð[¤É\x0019ÖóÁdàl~\x0006ÃÕ8\x000e\x000f\x000cý\x0006#Gî%i¡b\x0018\x0014ê}£û$A  \x000f\x0003tÉ\x000cc}ÈP1\x000c¶¹4EÌÃ AÙF²$!ô3(\x0007^Sf\x0010´mCD¦,8
ú\x0019$Öe\x0002R´2\x001dV3g|!4\x0006
*v«,eÖA@¼\x0017W&nÑ0`þÅ\x00184tJ%_V+:Ö¸è$;rìù²d@U0XdKíÁ²\x0007\x0005ý-F2$v]g%­K¼ib¾\x0005mÞý\x0014ìÙF\x001dëñ©á·8\x000c8©ÅØOV®3Â¼k\x0007Y;/#Ýip9t\x0004¹(Þ*ÒÉF{\x001a\x0005\x0013a¬}¨¼©³`\x001bèK\x00088yBr¸!¹Ó#·mpM}r\x000eT8\x001f\x0003v\x0005\x0010Ë0¸±'uâf?às®*\x0019+b$\x0002D¿ªÌKgÌÀ\x0008\x0002Îzø%ÒfÍ\x0008#-\x0003\x0018*ë\x0004¯\x001e	!ýLçhBjºPÐ\x0008S¼jeòe=Í\x0006K§4!%1s=ðqH¦ÉÔùpÐ<)\x0014\x0006ú\x0012X\x0008'äØ=\x001b*4Mu\x0002\x0005Y>b\x0006¿C\x00068L\x0010ÃÈ=Û&³`+MCÀnFàÈsÚ\x0014\x0002Ò:lû$\x0003\x0019iØª¼e\x0004~4BD¶Î:'K\x0013RäÙ\x0018¼Ê\x0000*F?òd\x0005\x0011#[ç;AÙ\x000bí×É¼SEþ\x000eÚxÀ¿g«}'CAá>\x0004¯Jù¼¬`Ø|u\x000e\x0019Abq6Ñ\x001c\x0000\x0013pì\x001f÷)\x0012º­2N¨¶Cñ\x0006H
×4\x001d\x0002\x000fx>àPÁ¦­ó4æ¤çùè¡ø\x0015\x0019°<%ÃØ5\x0011^¢¤{\x000b©JèÇh2
¾Ä"ÓÙdìªHÃgë\x000eÞ¡\x0002\x001e h\x000f¹y9æQ¼\x0006åGî\x0013p¿âê\x000eV
E>ótÐPÿ\x000fwÆòtx>æÑ¿* ÌÕ­LaAu$¯LèGÆ½\x000696\x0014	\x001b«;Ô(QÂ
ÚQø)\x0019rq'ÇZi\x0010\x001cwnCD}{\x0018\x0006¯xË¶e£°aì0¤ìê¼\x0006\x001dP&
ÏÙ(Ã
ï¬Æ\x001eíà¢ÚÕ­K\x0015yBBIª¥aðÙ Z2!MdW\x001dù\x00114\x000c\x0002\x001cùQü)rIþ\x0008\x0006Ð¸õu®1(CÓ\x0004ÀÓQ\x00049\x0016 ù,¾Îo±Ý7Ðµ¤K+\x000c Ñx~Ï®`HóØ×Y'èDßÁÂmjF(t\x0008#ÏùNä+\x0003ÓªD¿Ôú¢Dñ\x0015\x0014~ä~	!_g m\\x0007Ç#\x001djàª×\x001a=\x000ei\x001aùº¼\x0002i7\x001f#ô½Ï÷\x0014b}]3Ò<Ûåë.ïÄ\x0000º{\x0014 ÷fíÎ?»,*\x0018 ± îò.¹²üy\x001f^PäÉ\x0017¿ÁgÍS\x0005Bú÷|]f¨+NqÀ"\x0014ë0vÏ\x000eÉ4:óÎ2lÒùïkl9YùçMd\x0005CÊ¡ÎB¥¥\x0019x:\x0012\x0005\x0004ÝUú\x0016#W\x0005l´¡Î@9ËWÚ éS(Y\x0010ÄÈÀ\x000fÜ<:\x000b¥
§Û¸\x0010É;\x0002þ\x0012ccãp\x0018	uyOÚ6´º
u\x0006Ê\x0005,oÁ}	T¾Ù/\x0008vìlH¶)T&\x0017(ÌÖk]Sx	¥Û¼etè!)!ÔÙ'¨òáË;GþSb\x0010ï2úò\x000eü®Pg ¬ã3&xÓM´d\x00069ö`\x0003ííCeò+ãeõó\x000cÅ£×ã<z	Á;|ÔÀÖV2\x001d¶ÙS¢\x001c¶Í8\x001fJ¢¬[É¦ðxÐ[&*ò
¢ãæÄÄºÌ\x001fðäM`_<zkÊ¡bÜQ[bÚO]Þ\x000f\°\x001b\x0007ÊÈïJØrÜ±BbÞO]â\x000eÅPkËWF¡XêqË\x0002¤R^Êº\x0017è©	ðà\x0004¢±kÛ® kç¥¬ÍxYOä¾(òâµÅ}\x0019u#\x0015fäÕmÜ^Ã6¸³ìÖ{Þ¸ÃÈø\x000fÔ¼¿I/\x0006ëó¤ÔPMy~²\x0017YõbÖ7&ÞB\.Cè\x0012¦\x001fj\x0001ÇRÕmÞ ñºÞ9)G\x0013Ò"§m\x0012R=d]¾\x0007´EÔ¾.ØPúrèvÏßeöÏKø²îf\x001b|{¯ÊM¢£ü\x0010Ë×\x0008ãüj	×Ú²òn\x001b\x001aZÑ!c¹âWºXì±f\x0002\x0014q¤©2\x001319>P¶¨¦ qÂáC¯\x001a½m@8QÖÝëz¯_hN4ð´8àQl\x001c\x000b\x0001£îN\x0013ÒMhbây\x0002¤Þs>ýóñÑ
\x0006\x0012÷Eo7½²\x0004'Ýó6»\x0001¼rYyÆC2¹<\x000c¼>£\x001f¹C KÖÝ"¹f%'CùõÒ(Îz>\x0004Q\x0001yÔuÔBò=;8wtêÄ\x0014nZ\x001a#/±9¬»ÄLj:ó\x00058óq­Kaì¾\x0001fVÖÝâ¸\x0004ÁCpErhl\x0010Úë\x0013®pdÝ=NHnµ¦Ï!±.+Ò0ÎÅÎM®ò³îöq\x001dóÌ4ë¬Í±Éõ\x0001TÞÒ$»¬
éâ=W[\x0008ç×âÙcxMn;%EUx*rN\x0010¤·sÌq\x001a­\x0018\x001b(´(ÎmM\x001dÅwå¬\x0010CUa@·³\x0011_(ÎÑb8ò(qS²
"H»RIºSñÐ\x0011'Æ³\x000bµâ»»¿Åã88Wð8ZÌ^/V\x001f\x001f»\x0010,Hç=,ù28å3 M\x0008Y1½¾¹¨B\x0000«	~\x0004)©@0!ðmB°\x0012!¬ðÍ\µ!\x0008`3áÑvÑ	<t\x0007Ê\x0004æd\x001a¤æýÚ\x0000\x00028/á£\x0000ÖB!0ô\x0019\x0014Ef@ÒL#1PucÀÙQy\x0010$
8\x0006Â¡©L³ñò¿s.8´bñ_N¡¿|6î[£n÷ôÛb¾¿Y\m9J\x000e
ÉÍqm\x001e\x001a\x000eæé\x00057½|4ß¯Éå³µ0¶ÜÿB« \x001cQbÉ
G³å{ü].>l\x000eÌãlo¹ú¸¼éôô /6õ´f×ß+\x0011ùBÞ
ÙÞÁé.mÉ\x0016Hî¸S\x0007¢#G2=tßÍ\x001bªÒ¥Ò5*9\x0007äÎ:u níñÅ\x0000Å\x0011\x0008bK¨À7NCAr¡w\x001d\x0008´M¦JQ*	\x0015T­×'&|Æ|í\x00011iø@¹\x000bs&:V2Bã	 ¹è»\x000e\x0004$Ä%x
gymø>.Ýåx\ú]\x0007b\x0014áÃ§¡û\x0007m})½\x0013æH.\x0000¯\x0003Ñ?
¨úò§±ådà¦H®\x0003¯\x0003á\x0005\x0005~¡\x0014<\x001b4­B©\x0004WãW/\x0017×­äS@Å;Ïðà«§¡Á\x001cT\x0012^¹zEÉn±\|ªÒ|áê
9þÃpax\x001d·%¸c\x0003ï5ª3í'|\x0019ª\x000e¯".' R¢òZi¾»tbÂPÏJr{\x0018 ûæâû\x0001Ù¬k\x0019LBâ»o)3BÕi2ñr=[ÃÐ1ùü)Þþr^\x001aLWxp·Ïÿ÷¿þ÷ÅýýÝ-5\x0012¹¾½ïòÙÊ]9dPQ)8ÛÏæÁÎ\x0003±1i¸±çìâììä:\x001c\x001ewÉb7\x0011á:
\x001fc\x0010
Eo\x0015He\x0005FÌ§\x000c£\x001a·mS\x0000që12DÒdP\x0010Lù\x0014âÎ\x000bÏäãÄtD!³3\x000e§ä1Ãè)´_:;\x0019i\x0018IÇ$}éÆ\x000c\x001cLùC~ü¸0üþ\x000e;Zt^XQ$Áz_Ò]8k\x001aE[GïOÏ;#Lå§K\x000c Ím?\x001er¯BÞN¡§FÉÿÒ7nìÓ\x001f_óòð\x001c\x0005S¶¿¿!5\x0013è´f¹"ØóÏËÕÚ¯\x001f½|êïß,î\x001e»&¶.\x001auIûg:0q	üó\x0016iÿh~rÑ=	\x001a\x001c-ï·#ª¢Ý` )\x000f3øÅZ8¡\x001c:£åsnç:'\x001fÊ¹Dp¡\{XOöÏ\x001eO?Â¿Ý\x001c\x0010<5¾»»¹¾½^®\x0016Ý8\x001e´\x0000ó=f,õ¦×D|î\x0018ûîäèðøðà´«Oj\x0013ªånÕQÁ
7¹\x0018Ú³µáÔM)]\x001c\x0005åäõÇh6}QdÚ{\-n®ï\x001f¶^æð\x001dc:[rQ9û_2<7N{\x0017§ó£Ã³óîcö\x001a©å\x000eV2¥S\x0008¥ÄÛE.¯.yKÞTM¬j=¡¸Æ×o'¢\x001dôhÂÇßõF<\x0002Z0]ß.g§ËE·\x00156\x0001ûusÙ1e©\x001d\x001f6b\x0012Ðméðø`v:ßwÛÃ\x0006Ðú¨W\x0005\x0014#_D;Öi^z#nT\x0007óÛ\x000f¿Ú4Îø½°Éy÷¥*bÉ\x00032ti]ädtÏ}.ìcÞ	s¹úøA><\x0013ÆJ~ÄÁÕÝÍv\x001f®Q·,\x0000&¬/*húé|\x001dìtv\x0019hÂlNå^\x001a\x0010wå©¬ÉãJ»]gG>]óõ4$CUM\x0003íh\x001fµ å/öY N4«"\x0007Ã°\x0002QýÐ¸\x0017ªT°[JFZ§®ªÁ\x0003óåö·oþ×g'ðárµ|èÞÁ@!\x0002±qØmJ6q4ÏL`h\x0000vÞ½Q4h6·Ô>\x001a\x0012ÛDãÆûó\(¶\x001e§ájTàÀ%\'Æ°^ÔZÓOÈçvÒ\x001e\x001c\x0019¿_\x001bë\x001bÓàû/\x001eWY³3³3%öx½F©Eh±áipÎç\x0017§Û¤7ýõãoòÍ¸,Íâi«Ús+¸Î\x0018b³,®&EÑ¹{n\x001e¿I\x001bU÷DþñðÅ}]6ö©óÕu\x0017Ñp@È\x0000ÐÚL\x000cÉì¥¶QAw~zXõCóêÙúC¥ \x0002ï4\x001b_äúêô35ÿT-\x0007þÐõæöw-ÉæiÇå¬\x0003G
IéÇ6²Õ¶þÜOQ~¼~z\x0010Ùv\x0010\x001ap¥LN÷Ö³P\x0003¡u\x0006ùïAh\x0005x·!D¶±lLätZ¯\x001c%ôª(\x001b\x0004qõåñ&~yzIt¶X­\x0016\x001fÝçR¸\g£½\x0016Þ°±\x0008â'Ç±³ùééüUgWè\x0016L+ÒÜ\x0007\x0003º\x000f%µv-Á¡|ÙBÜOÓ\x000b\x0013BXËg÷³ô£\x001f³ãåã·Îµ"-§D\x0013ÙPjí\x0013ëYÛíôçóÙñÁÅO[Ò!Ö`[[
\x0011ETÊ)h8/\x0008J:yfë¯\x0003V<\?Ùs\x001f¡¿îê\x001acPóÏ[×:-8JHÎÍëÓ/Óz\x001aN_ñpöj6·mÿ\x001e[þ]³à,\x000c¿0\x0018Ö5D1«"B\x0008,m´/(_A	:)\x001a\x001d×F\x001d\x0003_5?\x0018&tÜþ­t"{Ê&/$;eÁ\x0017½¯\x0010\x001bÓ¸ò\x0007öK|lýÉÐN-\x001azå\x0000µ~ù¹(ßF5úö\x001f½ütéWæ©E¦ó×]\x0000Ú9ÃÓ\x0012ëVXÏÍxzM\x0003-æ;;ê¶8ZL\x001fG(åu\x0002BoT®\x0010Y'b3p1£uéÜÃa\x0003û}N
f§ñ(È¨¶9\x0008D=ê?\x0002Î	~Âã<ÙÛë».wÏ`u~ÎZ±BÓÕ7\x001c4ó´¦SkcqLÄñáI·wóëryÓü"äuæÒâºÛõÀ²&G¹\é'Ógk5Æõ*¹9¢4?Üæ\x0007¡>®\x001a\x0016«ïæÌ\x000bø´ÿyÊðzv¹öèZæùv¿Í\x001fÍáµ¾í°]+\x0015UÙÈ·v\UåD\x001cñ³éDÝ\x0001!¹\x0002\x0019®.©*^\x0015éÞ´xïÞ9ö¿·D¹\x0012ma	g>ÂëQÿ£Ól_=?\x001a

Õ\x0003x.lT#½\x00143ôgKáÄG_E|±\x000eëP ECÿ\x0005
ëøá[ÂÁ\x0000\x001f}WÕâç'ån\x0015ËÓ1?\x001bnduß\x001a3ÂÙrÂL\x000c\x0012±×eª¹FTýÏ<=xô}pS½å
Îµr¼\x001e>Õ$h\x001bá£o)\x0016\x001a\x0000±tRæQ6ÜöÆ\x0006\ýÃAÎ\x0010\x001f}I#%{\x0005$©w6EYÒèáë[B\x0018\x0014\x001f}ï¢\`DV;Ït7Â¨J÷ÿý\x0016=í+´Ý{çJRF\x00115¬íú
ixô%¦x>µ@_·È)ªDnÍ©\x000ep|ôç^P\x0000ÏkL\x0019Uê\x000c\x0002yøèym(¦ÐcÚW$¹)åâM½éú\x001f\x000e\x0003¶ß¤K[.3×M­ÇÜ\x0011
 |ô%w¸"\x001b
Õ\x0002;x¦{S½Æ	âü
ö²ìöK\x0017¾\x000f\x0014ÄÒ]\x0015\x0003ÓØÌ\x000eøÊ²÷çKt_¨5GÏÍ)ÄàÉÆ%ßÚÐ\x0001Ï\x0005vaÚ²õ\x00040üÔ¢ç\x000eÙú"³¤$ë§¿.3\x001c7\x0008\x0010u¤·Þó\x0015D(ÊVr¬"¨2\x0008ªÝ\x0001 \x0007áË­^^~Ä\x0002¢\x0002w\x000f\x0008÷ËNäÍsU8¨}gÃ#E	¨vì\x00190\\x001dT@È|\x0005*ë(LdÏÎi
yùVO\x00171º°Í\x0010\x000cÐ\x001fY\º\x0017#f-eL±\x0010ñ\x0005¥\x0019[Å\x0019\x0016X29âúWýC~næ \x001dõ\áÅ´.Hl	$E]à\x0003J×\x0008|w×ûóQ_\x0000\x001f=\x0000É×4¬\\x0011áK³)xNªØlT\x000f\x0000.\x000b>úF @º\x0000Õ³ÙâýçK\x0000ªq¸é\x0005¸ýpuíÿÀ\x0011]\x0001;æ,foVÛÎb!ãe\x0017(M;ZA
\x0016tÍ&-óÙÓùñ-\x0004\x000bk>bctð]"~oËÕm²\x000bÝe\x0011ÉãÌ\x0017OJ@¢w\x000e;9>ðf\x0015Ûü§Óãd\x0016º	ÂâîAß£] ¡ÎyoÈA¼P'\x001dåG\x0004[Dc\x0016ÎK´¡\x001f\x0000Ââð«\x001fÀxî_eÓ\x0011×§Î$*úÆmN?Á/\x000f7×\x001fL3øóùãêGgøÍr~½\³,T\x001a 
\x0005ÅßoæóÓtþtXÿ\x0014XXÿ\x0005\x0007Eÿþóð\x001e\x0016×7Ýw´QKNX	ZrR¹R2¬nÇØÿ~3ðÎçG[nj\x000bZh¢!hi$ø*Ä'7VôìMøðT%Ú¥p\x0006#T<j{ ê"ïo\x0016·K`½ZÞÌNW\x000bIr\x00056ÐH"296­ôØ\x0015\x001d\x001f\x0000ÑìÕÁÑìô`¿Ì¶Éì\x0010²tÄÈ­V´Ö%EÕ\x0006_Mç-?ÌPkÅÆ¨-þûM:
¼3t\x0018ßÿ´øü\x0005owQèºÿ61*Ád«ÈX\x001c1¦á±í¿¿{;É2Ì;&1qIbÂ y- øHÚ¤-\x0005-û¥iÄé«\x000cf"ÅõÄO\x0001d>l¦ðvZ/ÍÚ¾i¤\x0004õTJþ\x0004_Í§Z[¯vân?mQÙ\x0001T»ê$*¾«.ãd|WÆs?k!¹\x0001Hé\x0010sì»<PÐª¨éQA»¦\x0006\x0015voªÅR²\Á@¦8QyÎã´ºáTS¹H·ûÅ.Ä|Ï\x000c\x0001\x0004Þ÷Ót_|¼íé\x0016n\x000bs~¢>Ð5o°FçI>o3ëö`\x001fÂîûiÂÏß\x001coëåÛX¾\x001e\x000b¢ï:cA\x0011'«`¸¤¸U6\x0014+´±B=âTiì©¸ÒYr±j\x001cðb©öh©\x0001£¥Ø2$,\x000bw¬TþÌTÍÛñ¡TíÁR\x0003\x0006+4t"se5Ýg¥
*]*\óR[þ \x0015D°üA½¢lJ¨sYO¬Í¢>*­ZTPæR]¡Ù¶Gp\x0003\x0015eHªmQB§Òm*]M%¡ #[,H\x000bTÐ¢¸ *z
Ã?}\>|ÁÂ)î~âçåíÇ»Çï	ÁÒ¦-h$Ü Ä¿\x0010QÔ\x0018ù"j+r[r\x0008,°:Ì»ã7'\x0017ÿÙüíóîK;¨ÕÒ@\x0003V¢\x0001U\x00124\x0006´z3Mé5z©UÒä°@6
Ð¤óuôH£=Á¤12S`¨©Z-ÇØ\x001fÀÀMfÚº\x0011\x0006[«iÆò\x001dû8\x001aê¯Vû¡ÒzòùCáÝfÈ\x001fÊ@\x000bF%áì\x0014\x001aêrVý¡²h$~(LÅ±	°ßæ/\x0015'
õ;«¦I\x001e·!\x001a¼"ÊÓ\x0006²24\x000b@O ¡Èu-Mpû4\x0002.Ã3ÖLãÂ\x0014\x001ajVMc^\x0010\x000cÄ1yEò¡ì$\x0018êV
#_Ð¬ö1Ã8WÖ·\x0002ÃÑª×wné4\x001eê3
Ô9f\x001a=:RUÓä®yHã \+ÓD@¦QSæ07§ª¦Ñx\x00054¶|)ëÊR\x0013`,õgªYï
É]ô¡ìúCqIú8\x001ajÖTM#±]ø\x0013¸\x001b\x001aê\x0015T»-(lÿ»Bä=Ê@Ñ£ÎÂwS&
_ÕÔ-\x001b&tíñ´)hÐKÕY0tÊ¬áJÜê
S£ê9z6a½aÊX<\x001b?øTÒ¿®\x001c9\x0013Øà
½>,BgBªIcC\x001d\jiÅ°(ÐÈ´E\x0011"[#âgq'j8b-\x0016Àr¢g?TI'\x001dGC
Mj&mÙWTB¤ñ<4ÁL\x001a\x001aêlR;4Ð@"[>ï\x0002pá\x001c\x000c\x0013ÍI\x0003Y~Èæ­¡®'û5\x0001úRå\x001d
\x001bqyÇICÃ\x001d6jî\x0002ÆY¨HEhØ\x001f\x0016bÏâ\x0004\x001a´	ªPAs\x0004j]"{ZÑO:¼ tv\x0003BÄ>ntÒ´QyW¶M?Ü¿yøþÃ}ÅÒüôzù8{uý0Û[¦ø\x001fÛT[SC\x0002ãøÀ¤ ËLf2bÃ(\x001f\x001d\x001e\Ì^\x001dÏö\x000eÒ¡üý?*ÈJ\x0017ÌAdéAó)÷Æ\x00042ÞHµ;àâ®¸\dOÌ\x0006ÁªÒWÚô\x000bÇq¯È!dkÊ+PZ8ò\x0000\x0019¤©ðíÌ ª¨AUÑaÃ­\x001d`ÔÒº$ß>
\x0015O­ä.Ø.ír(À$qü¤pl²ØÑY3mùéG\5ê%_/¯>aJÉ\x00163á°]ºS
î\x0005Êá¹\x0004]4\x001bCõú`ÿm3±¤\x001b"×V@$#Ïr\x0005]¯ \x001f7:HÎ\x0010^g!úG\x0002d?TÝPHjù\x0014èågoaÆmZz4\x000eªn,ÀÆØ>
\x001fD±\x000bbJç¤á\x0014i\x0010áW
EúYx:V\x0019QÎ££\x0018&lºÏÕ\x0014|ü«¡\x0000A\¢h\x0008³ÏÁS3\x0015ÜÈªfVx,òBíÃs42ß\x0003VR4U¬+8\x0014\áf\x000e) ï\x0005\x001dSH(Ì\x0018qóL>` \±MF¶j­Ê}^$\x001e®·ò¹g§\x001fK!¢\x0012B8£81,\x0008e«\x0015<O
k\x0006q<~ÿôõcÀÑH«\x000b~a:Âv\x000c\x0007éÉ0\x0014O&\x000c÷«\x001d3ô\x000có\x0011j88!ªÃFÊpdÄU\x001e\x000e\x001aµi1ê)Æ¹¡Óg©\x0001AÁûÂÃ\x0006*\x0006D\x001eDr$uF\x0019ìpN&Øüi\x0014\x0007Ìf x¸\x000f\x001f¾ï»ÅíÕÝ#H\x000cm§Á¾)"\x001f+5¨\x0001F:K×\x0005!7ÆåÝüøUú#È\x000cU!qÛõz$ÐiÈ.\x0006A\x00164kÒ\x000b8\x000f]4&!Av.ü\x001a$0»\x0011\x0002¤\x0019à0EAÃäÃT$ê{<\x0004Ir\6ùDPK$\x0013\x00057
\x001bß\x000eCòù\x0010öc\x0010
ÍHÄ&!Kö5RLÎÇ1Læëòê\x0016ÕX´ªxÚpí{¶Ll[ÉT:åæè6Ñd\x0006\x0014øzÙ\x000cD©»¼m¸\x0004>;HU|$m:/FööÏÇÌg|Á3;Á£\x0002Ê¡xRy¶¢\x0016´4TÆ\x000b´"\x0013ßfLw$\x001fç \x000fåÓ\x0001ë±\x000fó¯¢4]\x0007÷a|$¢4/yð SIWd>Uù(µÝ	\x001f©·\x000eæ\x000b\x0002Å\x000cÏ\x0007È
B>ã\x000cóÌ?vfÏ\x0011P\x0018?	².yüØùÞÕú(à._³Qqü"¤ãü+^y\x0014\x0017ácøZýn \x00119°\x0005¦\x0018È®Qln\x0017C\x0008??>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?={?\x0014.ÿñæÕ«Ûç}s}ñæêæå\x0006pÓ\x0019à>ñ«.nñÂmAUÉØa\x000fÈnn×r»	Üù¦Iý	y'j\x000f6p\x001aÖ»aænðÐ\x0019àXÊÂà\x0001k\x0011<é|£sÃ\x0016§Ýà©\x0005O3À-gx\x0015ôþ\x001f\x001c\x0011ôvX\±ûØÝX£ó/\x00158zÇfhN¾¥ê¨Q	Ñ¶\x000bÅqª>Ä:¾VÄËc>R ×õìák#\x0019vÐï\x0002v-°\x0013\x0003\x0003ËuáØ\x0003C\x000b8úðn¨u´\x000f¸»r.Ð\x001c2	¸\x001d?áð¢ÚepèDµ{#_³[\x00058î¿6×ïÞ?|yø¼W×ÏªAwsYlo-§j8y,ã;2Þ\x0002¾{~ýöúÍ=NpÜã\x0002m\x0016ë|pk¨\x0001®'\x00169¡*ï
úÄÉÅí[n?ÛhÖè	<[Ê[­u]ïcw\x0016wl¹ã\x000cn°íF!\x0011=« Ë\x0016\\x001fß\x0010uwC|ö·ûÏ9jýåË^EïàXÑ;ºDª°Ù­Ô\x0011+z \x0017Ï~¼z\x0003×?½}"·ÌÌ¦e6\x0013\x0001\x0001¥åÈsfÙ\x0004ÍsõöÂ.h×B;9tTJÀJUiBh\x0008v\x0015Ù\x0004\x001dÌ±'7åâøþþç\x0005ûõçÇûO?}üòøë>lëG½áB­S\x001ddìõñq|õüêÙÂýúÍÝÕëïnßÞýðunh¹a
·aîìßiÜ\x000b(vê§çPÛÚÎ öÇ_Åo\x0006¥z\x000etämO\û.ptìªÁÛ\x001cZò÷ÿû_ÿ}õÓýçÏ\x001fß=îc\x001cY2}\x000e8\x0019\x000c½\x001b}Ò]WÙ_\}wõæÍíÍÝ×Ù}ÇîÿPì±c$öÃh@dÇÑ\x0000v¯ãQ>MÇ¦üÕÇ\x000fw\x001eÐ\x0000E¤\x0011/7\x0007`\x0001Ä/ñkã^n_¾Y\x0007µÇjPö \x0006õüþßïÿóáóç4>Õ^wWÕ\x0004²9\x000f\35
¶_}õ×ë7o®ÿõçû_î?}~|¨ÿp
-*ÈP[7PÐ®NC³µg¨?¼Õ¶¬VÄM=ÏT¶Qó\x0019N§·ø¡\x0018õ\x000eVß²z\x0019«åÖlT\x0014
¤ì¸ÂY(ï`
-k±êÀ5;.G\x001a$»åä¼	üè\x001a¾\x00036µ°I¸°%
\x0017aN:[ÑWØ°h\x001fìá±ÚÝ¹´\x001e`$Ò.sdÖ×f\x0007o\x0001"ÚÞlÉìVÈ\x001bµ 9Í\x0017)ë«êNCå\x001d´åÒ2Ó\x0015\x0002°L\x0003V¦#æ
_E2ìÈ\x001fì5\x001d¬\x0011n\x0004]\x0004{\x0011Ö2}Þ\x0008üÈ¬ÓP|\x0007mghµÐÒÆx°\x0008¡n\x0004w¨î\x001c&ævÐºÖ	7å4¢ÓéÎ1ªOjAvÂv~A\x000b\x001dS,ÃiqX\x0001\x0019Ûjj\x001aÝ wÐÆ6hóê]3Îå\x000eê£¯K;|ÊÞ\x0001Ûy\x0006-t
(ZÈ´Ü+w-ß<á´i\x001f-t®\x0001d®!\x0002×|c÷\x001euB\x0006\x001c\x001dKAâpÑ\x000eØÎ3Ì3à> !è\x0018ÑÖ­ìÇ@l×B\x001fÓÊ<C4\x0007a\x0003\x001f¥NP!»\x0006à2\x0000k\x0000k°Ä\LK
\x0001\x000f2Ó
wBç\x001a@æ\x001aP*b±ß:"ó¿x'Å\x0008Ð¹\x0006¹¤LyøÈ´Þáã\x0018ÒF."\x0002«\x001b¡s
 s
1,Oéei\x0003§ BÕ\x0002\x0018ªÎì í.
 »5$tis$FÓø¢å
@¬FÑv\x000cd,)ÍÌi\x0012JÊû ÂÂPßo\x0007lçÈ@æÈPÌoÈ\x0017]z\x0019ãpÔç\x0015ÑÎ\x0019#ÃYTîæ¼bû\x0015«ù2C]ñ\x001d°k02×°´Ô°A°Ô\x001cf\x000f¥`e;h;×`D®Á+	EI:|Û/AB
üD\x0004ã\x0011Ç;h;×`d®!oVÎÐåû\x000eG1ñzì\x000eÑvöËìÇçeS.»8\x0001{9c.cJ'BH2`:óeDæ+ÿøº\x0014\¡E|}Ì×\x001d¦uCa\x001d´ý2"ûå±´6Ï\x0017²ÒÏè):6
ã/ÛÙ/+²_X*XòåµMJlJ,_\x0003^õ°]$nE¸×Ê°µõUÉ©To»iX6¸¶3·Vdn=6ÃD6`F\x000e»ü¿Á\x0006,\x000cgAí íÌ­Ûl¡¸$ÓH	.û\x0004Ú	FI°]¸hEábÞ	\x0016\x0005¡\x0017Ú|H´¶Éi>eÃñ9;h;skeæV{ªæÉÿr¤¹÷&©Mèì­ÙÛ|éª\x0016Ìp-Ã´ý¬SÖÙ[+³·\x001a\x000b\x001cÈ9\x0006æÛÇ\x001ev}lu¹u2s:\x0013ÁÒÒ¢@É²²V×M2à:ûådöK[WênE v\x0003í¸ÿÓ(á[ë\x00020'
ÀüRÀ_î
Þj\x001a\x0001æ´¯\x001bA
VwÐvws'º{\x0000Í¯
\x001eËrJ\x0000<×P\x001b3,ÆÞAÛY['´¶ù`Q&Á[G/zN\x0007¼¶AxÈ:këdÖ\x0016ìÒ=»Ðæ\x001b$í[84\x0019á}×uÖÖ	­-f SñB ß\x0010ª\x0001\x0013æB]gmÌÚBª\x0012\x0007Á\x0002ÎJGZãx#$¡IðµõBk\x001bBÝ¶\x000e(à4W/\x0012q"Ø.¶õ²Ø6ÿ\x000b\x001býÊ®·uF³ñ¢û*¢í|\x0017ú/\x000b\x001cÑ8|Ý+^o9¢Ù/ßùÿº·K²#7\x0012t·r60iãßæ)LUQ$«dõ¼\x001dÙ*ö°H)IªMzmÜ\x001dÜ^vrWrá\x0001w\x001cà\x0011\x000cxDåÖ#MuZö\x001d\x000f»Ãá?~£oHo\x0018#\x0004²\x0008Pû)õÆû®ï|ßè\x001b¼ãÉ'A+ª3u\x00068J0_¬³\x001fíK=¶¹\x00060S½`éÚº'ÑÄ°ðÅ¹\x0003´±õÛ-8]¯
qJ/M¢UµsÛl,Mñ±õÛ­Á\x0006ÚP\x0015®
&Ùª\x0008°-¤	\x0001\x000bÛ\x000c±ªL%È´ ('îòmÍmøâ<þ\x0001ÚÎm\x0006\x000cK\x0000Í­§Ù\x000fùqlk7VÒîn\x001e¶ÝÍ
."¯\x000b¥qÖòS´	\x0015\x0016\x000fÒvÖ6l³¶8odÉP]³ûõÝXR\x0015:k\x001b¶Y[ã\x0013\x0017§\x0004£i%:VD³I_lª\x001e íÌmØfnM\S\x0015p^1	6pa¼	_\ø7@Û×ÖmÄs Í\x000f\x000e!ß|Ëækg£­²ÝX¦\x0014:ç\x0010¶9\x0007\x00007H\x0014Z`ç`ëN[\x0013·ùÐù°Ñ7¤È\x0005`ÁzÚ|Ó\x000bØ7¤/n\x0007XO\x001b;ß\x0010·ù\x0006«\x0002/@ÊÁ\x0001\x0007·N×pqcÝOì¬mÜfm-z/\x0012m\x000eÊË^XÛËe6^Èbg¾â6óe
Ï¹
8þ¿X/çyÕÕ_aº\x000eö¬\x001e«\x001c²\x0016\\x001f\x000fo>¼wøáíñÝ«ß\x0006y%Í\x001cÔ\x0001½â ?\x001e¹¾<<¾|ôìéÃ\x000f×O\x001eü´\x0002\x001aZhøN M\x000bm¾\x0013hÛBÛï\x0004ÚµÐî;ö-´ÿN C\x000b\x001d¾\x0013èØBÇï\x0004:µÐéûnÛ
ÜÔnð]P÷.ñ;ñºóú;qºó/ú;q0º³Õú[7Ö>Þ`3\x0019o\x0018út¸~ÿqó:\x0006«\x001dMLÌWU*ÜPblør\x0017úÃõÓç_ZÉðµßr²,ø[E»üü	4¥\x000cb*¯¸8í\x000e\x00065³ qèÇ &ih"ÃòiµOiýt\x0000}{¸ùýïÈißeÚ7w?¾Í\x0008Ñ(0¶då2ÑP\x000bë¨¦K­uØ-0Á>ºùåòÛ\_äÿæ«ÃÍã_æ¦ø4p®scp@yù\x000c\x0017\x0012\x000e¢àB©âÈpòòb¸ÐÂ18­J\x001a\x001eáÌ\x0005±¹28\x0001Ùì6´Ô¢¥!4\x00026ÏLhÙ2\x0017ä\x000c£ñuZÊF\x001eØ´\x001e±jçÁYÍ,kñn\x001b]w\x001côàyÀ±\x000c®Ð\x0019MóiRòg±w#[w\x001aôØqÐQ,IfÃ\x0006TØ´qLGSQ\x0004tmwù\x0003÷y?;¾y÷ñÃáÁûßo\x000f·\x001f\x000f\x000f¿¿¹}· ÀüyUù¼ 8ñ<\x001f =\x0017hø]>zòüÙáÁÓÇW«l\x0000/\x001f?º)Ò°BË
2VçKn7\x000bT%zJ^\x0007S`c¤§´Í°¦52Ø|X,Ù\x001bÍ\x000fÀÉ\x0003\x001d¨~e3«mY­5]h:ã¸õÐ\x0017VS#t{\x0003¬ka\x00106\x0004ù\x001f»\x0008$X\x0003tèc0;iAha\x0010Ö)Æ¨\x0005Pbe\x0017¬±1ìÃZÖ$b5àK5\x001bZz(\x0003%SÐe!\x001azÐ»°êÞlÉìÇÚa2®I¶ÞÅÀ¶Û»·\x000b¶Î°«Âå\x0019v£òÅ
ç$^G)XUåkÝFdåÎL­rÍPåpòÔûÛOwóÖOG
)màÕæ)iUNW\x0016;®\x001c\x0002ÿtù\x0002GL=½z17Fe¢	g^+°fûãÛ\x000fïÞ¼ý°àP»ðå0Yüæ\x001cjyîÇáçêÜ¦âP´ÇWÏ<º\x001bÖA\x000b\x0006\x0003`8¶jr*\x0001\\x0019VL¨1M`¦\x00053#\x0012ã)xJ<ÍZM¸ÌÀ|8wï+Áà\bÐh\x001aò¹úËÛ7\x001f"·\x0014JÉdþ\x0007|f\x001e¯+Zü\Ñ®\x000fW?^?z6\x0017\x001bù_ÿù\x0017óR½¤'ûé¡þúöðóño¦C\x000cÔmáñ\x000e¯bcÀWXt\x0010\x0016çº¬K±\x000c¹±&:nÿË\x0017¼ÿy}uøùòß^<\x0013OÇ¥ÿú¿Ê­
þk\x0005\x0003.ËÖÄ\x0010°Veb \x0019ßÁk\x0019\x0002>7â¿¾\x0010½*Z\x0008\x0006%\x0008\x001a\x0001P\x000c¼Ãx%Ã_ÿþ¿ð»}}­ðÛñî÷Ûs\x0014\x0001'¸\x0002	B\x001b,Ï\x0014VÑÊ\x0019{ï\x0001\x0015óÁO7¯iíhuª\x0011V!àT«Ò
18'\x0017\x0011/C6¬U[\x0011Ï!¾.
\x000cæÒJ\x000eÜ§ÜÄË1\x000cL\x001c¾´ög\x000c\x0015\x0007D¦¬)Â/¨Eø?àèÌyåFåg
,rE3©¾Ú|ã;Æ\x000f8\x0013sV\x0016\x0015Dw z\x001d\x0008­Ë,jZSXJe'²\x0016±@Ç\x0002«X@¤¬¨8¼N¬*- \x0005\x0008Åt(f\x0015Jþ.¦ààÒÄ¦Äg&Á¹¦¬D±\x001d]\x0002\x0018^M,Yg5\x0010á/T§Ö\x000e²¸Å­aÁ5,@_\x0008\x001bá}a	\x0014O\x0012X|Çâ×±¨Ò&,Ù¼\x0014\x0014\x000fl[\x0013¯\x0017\x0018D	\x001dJXb¦¦Úbç\x001dÖr#Kìí¼Pqc\x0012× ä\x000b#£ààÌ\x001c2L(:²Xð¶&`	\x001dKø¿Ä\x0002íò¤òftáMöÅ\x001fnß.ØRt&ë,»Â¤ÊÖðì\x0000je%\x0013=|q¸É.ùÙÕõ3ª`ÐÁ\x0000\x0018\x000eñ	ET\x00014nþE°`Ù?º´\x0005Ë´Xf\x0004Ë%>cÁD|W°b½¹Ù$/ÛÙ\x0011°Hm×\x0019lzd"ÕJìÉã60×¹oHÃ|\x000bæGÀ´Æûo	Árd\\x0004æ\x0015É\x0018a\x000bWh¹Â\x0010-Ùº¢bF\x0013Xi?E\x0015\x0003·\x0005,¶`q\x0004\x000cËñËô¸7ª|HmøCs£>ÆZ®4Ä\x0015ËûJæ	sÜ\x0013\x0018\x0018 0à~7\x0011VqU#då
¯A\x000e\YZdçQÓ\x0018Yoöì~è'²0íÊ.qKd%ÓZo!ëì¾\x001e1ü86Ö\x000b	Ùý\x0014<\x001fKµåTêÎðë\x0011Ë\x001fp(f¹4bW¸#°¤9\x0016O[N%tÚ\x000fCêÿG\x0019XmÏb\x000bmØâñûOo§§ø/R%Ü"\x0016K2/ä/êKÂÃ\x0005à7\x0007ýùw|üôÅõì\x0016Ú\x0008Z"XM#.S2R1¯
·ÒJ}þ\x0005×"\x0016É¬\x0017R¸(\x0019ù\x001c\x0011c\x0017F\x0011\x0005\x0013.Õ\x001e\x001c\x0001mìz!b±J9\x00023$£@"ð¹½ú:PD ßèQÚ/¾ýøæãmÖðÙÑxêr¥åN\x0013XBùNÓ:é¯?z~u{)b&\x001aèh`\x001d
¶*ÓeÏXô\x0013\x000b@k£÷\x0011\x0018ÓÁU0ùfÇöh×Jæ&ÙÍÒØÆ®£îÂÖô¦.ñ´ôkºðY\x0019ë`Ü:\x0018^W¯Ya
'\x001aOÉ¡°Pk|GãWÒPïG¦±\x001e\x0013&p@\x001b!MèhÂ:\x001aÞi´G°\x0006\x0002]Í\x00036ÞhbG\x0013×ÑàìqúR9ìhÊ\x001c.¤iÓâ\x00034Aµ4A­Tâi±èD_r¬Åt=Çb§Qtv{ÊÖnO?ßåÿô¿\x001eßÎ\x0002eÿ\x0000ü"p<·#\x0007áØeyuæÚ¾yôäÁ£/¯W@ù\x0016Ê¯²å=6Ci§\x0014}3¯i±õ¸¨[\x000e\x0015Z¨°^R\x0018c\x0014A%Gg\x000cûj\x0004\x0015\x001c)¶Hq5Ö¦l`3ZA6Ð\x0005ÉXò¥ZÇ(gJ-SZÏd(ELÀåï\x0013\x000bôÄªA®OÍ=)3ñ=i
7åm¬@Ù¢åA'ËPÎÊ©tG¥×Sá=EUbE®t\\x0014ÓÌË\x0008Ñ@G\x0003«i@q±ÖÎÜnæIôÝÀè
"2\x001d\x0019¢ç\x000ckzÔÌT¤âùÿj\x0003í¨ìzªlº§êëL\x0015\x0014îÐ¨\x0012\x0015ºd*ãäT%×ëM9è\x001cÉ\x0012£Ûcô©ª)CgF :K®×r½ãYT\x0011K	*Ò¨ÿLåSuvS¯7¨
ÖSy\x0015Ê«S>j`.Üd¥¼DTÖ¿:­¢RÓm
J[' çëÚ\x000f¸þõíáÛ·XZ1\x0007çrT\x0007å$âðèIå=põ³ÇJÙÏîm?àêùW\x001f®®±\x0002ã«Ð!Â8¢ÖÌdB\x0017é®ë¡Þ¾]´ß¾G\x0011Mh\x00111gAR\x000c\x001eÃ\x0013cb!¦Ï/¿£¶#´£\x001egC\x0014³×,\x00167+!UÕd)°Ñun¶\x001b\D0&Dv.|÷\x0019\x0005ô\x001d \x001f\x0006ÌA\x0006f\x0013ñ\x001f'Â@¯êÞy»ýC12FÊ\x000c\x0011"P\x0015ÇaÌøçÕÚ\x001bhS
4\x0016\x0001µ?Í\x0016ò$«\x0003\x0007\x000e\x0012\x000e\x0019C>\x00158àÎ±÷yÎýê\x0019þ÷NMNó\x0005=-uli
çX\x0002æÛÉ<ú¬Öæ?O!\x000f¡jÑxµÆJ±)SÊ~ðüjì\x0019Øj¨ÏUo%òçöÅWûòà·ã»þcöÚ\x001b³g£º°`\x000c¥µ\¾*pÊý3]{ðÓåÿõï_§	\x001dMXEã\x0014­ÈÁJi\x0002údSÈ\x000b2ØÁÄU0>\x001bY*Lr)â§+OKñKÖ	iRGVÑ`
\x000e½sáKô\x0002A=\x0007&\x00050"\x0018£Z\x0018±ÿ5\x0018ãKg	¾\x0000ÅC8CÎïHkat\x0007£×ÁXSÌ%>gé
cêë·:YK\x0003\x001d
¬£ñ4e
\x001fJ
}(§\x0002Ôg¿/T\x0018®¢1\x001dYG\x0013Bû>¤,ún\x001b¦36f¥±É_ãÊ §ë»c\x0004Ù2®që`r¬¬Êñ\x000eS³\x000e8mdµRB\x001aßÑøÕ4¤Ä¸Õ,\x0012\x000c¹|«Ï_ÌÖ²tVØ¬³Â« %\x0014\x0015\x0006¾íàªu¡d:3lVá¤pág±5\x0011ë\Ê¿SÝM8H\x0013ºï\x0014Ö}'ÜyR48º©W	a¡®Ä\x001c\x0019	Ípè>TXõ¡¦¥wÓ RH:)\x000efuZo­u\x0017ð"Ë\ýîT÷ï\x001aç\x0004e\x0006íûO\x001f§Òÿ\x001fwwo^½ÿt·PäCé·ÎV\x000e+·JN?Ôò¬PmVèéçSéÿ\x000f77\x001e<}q³ô$]ø¼jù¦±³\x0003|ùºT\x0006ÞA48\x001fêk\x0002ûôà»øPÂ×ÉÏÊ/F(GÏf\x000bY|µ³K3\x0008èB'½0(=}\x000fô¶(»fCLüe»Â\x0011	îøôà×ÕÃ\x0012\x000cF\x001f×Õ'èÝF<èð`P|\¸¬5\x0006g¯ÙAÉe7={ÙÆ\x000bæÐ§mhÎväãíñÓ¼Å7õ)\x000e(6\x0015SÐÔnælO_]¾ø:ïÈü\x0008\x0019VÁSpç\x0003{imk¯2q\x000bYèÈÂ\x0000\x0019Vê»4WæÐßà1i¸,vdqDfÊÖRè¢ér,Ááy\x0004\x001f'K\x001dY\x001aYtl@\P\x0017ÆS\x0017­Õûa,ElÌ"=Ã\x000c/Ý5_¯üÄæ\x001cê\x0004\x0015U\x000b\x0015Õ¸|YùP\x00031|¥\x0012*?M@hò,ÐäYpäÊÞ¿ûx|óîöp<\\x001fï^Ï#ã\x001eÿH\x001d3 è|êÏÒiÓP?=}òüòÑ«Ãeþßn\x001e~\x0015Õt¨F°ÝB7E\x0006ØA¤äÕÞ\x0017\P­jQ­ FÜâ@RÍVOÑÝDqí¨°\x000f«îXµH\x00032 #V|táM,W|9Ý\x0015:V\x0010±Ò\x0011&²På~7íÎ\x001b0AÛ\x0015×å\x000fÓã%\x001dø³æÙ¹\x0008Us\x0004µü\x001c\x0001ÆZÊßÞvèÈ¯è­p®sß\x0016ïàü \>4ä1	£8_ç9×Ú\x0003. \x000b\x001d]\x0018¤\x000b5eÀ¹ÎUó£¶ÁÅ\x000e.Â¥2@©äB\x0012×ª»ÄpîóXf.uti.G¥|nµÃfü	.:ö0Kds\x0015\x0019í¢lÂ\x00025å]=\x000czÊ¢O\f;Yt.[Ö¼\x000bë²\x0019{Lhkýð4T©éÓiØ\x0004\x0007\x001d\x001c\x000cÂaZÒVÓ\x000bM%\x0017Ì&;Ò¼\x0005ë²÷z\x0004\x000e\x0013¥³	GP\x0015É%n)ÉÈèT©BhR§©}\x0007~ðéÍÝááûOó%Ú9Ü2\x001c@cpè(Ö,9­Íçí.\x000f^<º9<|úb±PØ\ÇæØp;\x0016iuhËÈñU-|áiuÍwl~-Mk.Ê3\x0017ÐÃÓX
ÎÏ\WÛ¯cÆxØ&9\x001fê~Ç\x0012<ømÙ¥\x0006\x001e\x0006ÿè¨w\x000f_PJ\x001fÏ«»JTòà§¯èZá²\x001d\x001dàÂ}6|÷ð|
¢³ÌõÙ[þ*,h×B?µ\x0010¯\x000fiºÏd:­ÅéîéÌQ0µ,yÍõ\x0019Öv4\x000f§ÿ®/Ïj\x000c¿Æ¿ý×ßþú\x001a10ã£+ÞÜ~:<|óñðãû\x000f\x001fn_â}LS1 Åßß¼÷?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¿¤§×÷«Çÿ\}=,²,-`ô \x001fÃ¡Vëql»º¼ºNo®ï\x0017ÿ¾<=\x000c8Èe5\x0002Â-r2Ø\x001dU\x001d\x0005w\x0000Ch´ÍvÍx\x0010­\x0011¯Èøý$\x001d\x0008°\x001dl,öÛ¶ì\x0001\x0007\x0019­F@TµPÅ~¹î\x0018ì'ìQ
8\x0008%[¿o ×Ód@EÙÊõñp$\x0003\x000e\x0012[\x0010Læ'<0 È\x0006\x0011|\Ûï(\x0006\x001cÄ¼í\x001b$\x000bV'\x0003fáoøÀ~½·\x001düÍ\x0014W#`®¦Ìâ_° dÏ\x000cçì1\x0000\x0007Áyû\x0016Ñk\x000bæ'k8l©ä\x0004\x0000·Þë[\x0001«TW«	Yn\x0008\x0008
oàÖßxãm¿pxhÝ%z\x001aÀÂ\x001du\x0015Vi¯6Â\x0000kÏóWÖ¼-\x0015\x001dÍÃûNëGöCG\x0013jÚÈn°\x000cáiªìW£	\x0003Ëq$\x0013ÒQÌoåG3áðfÖú#ÝÎ4JxÒ"äÚ£Yp\x0004kµ æ$\x0005[¹þ\x001eL(
á¸¼»pxl5¡¤>¥dCA«ÐÄ#odRgí!ô%k6$åÄ HÐòhËpxÛmýÊæ\x0000C@UCúÈëfÛí­\x0015õc{\x0000\x001bF­tàÉµ§\x0019O+ê\x0003\x001c^ËÛ¿1=v¢	5â#[\x0010o%§õ,\x0011ÐgIÂcîpk¶±p?hÿÆYP3md\x0013ù#3àÖÜ^3 Á\x001aÅ>@S5v;g>\x001f}9·>õ4\x0003\x000eó\x001cíßÊÐ¿±[ð\x0018wcVYî!ÔÐÁ\x0016!
-mÙÈf@øo©:O\x0013\x0014ðr%¦É\x001a%ø×ëQ>ò0eÔJ¨øz78}X&ãö.Â*wÔJ(Ê2¤\x0002Ðak=Ï4Â¸ò¿¹q\x000eéâþùiñáþñù_\x0007k<×>\x001b«$>È§Û»åïkÌ¸Q\x000cÙ.Î®P³ëâêÏ»Þô\x0006XëÌQ\x0003Vp$\k¬ôª'`ÕqÊM-Ë®	k1j±V\x0019cqv!aq\x000f¸5v[äÒµÎ\x00135`EA¢¬ð\x0011u©f\x000bü
dÆªkÍTëìP\x0003\x000bJGêî\x0002c\x001963sÖ:'Ôg,­rg$Ú_¦6\x001d©Ö \x0016cy*c6ÖJ>ì£-¯Å³·á:ýÓ¶
³bZ¢Êµ¸°
ù\x0019\x0003n[Â¸&¬uÒ§ÅX\x0006\x000b½\x0013\x0016jùQÎÖj6VÜv	kÁ\x001a¦zÚÌe\x001c+RW
k\x0011p\x0018Ô<®A§Í^TíjáfcUX¬\x0015fæg\x001c¦u\x001a½<ÙËñ%!r\x001f*k,ÐÐ5Hæ´'\x001aÔ¯Ñì¸ØXÛNë&ªA\x0002§ÅXò\x000b]¼a}ýè5;®¹\x0007Í\¼Mµ\x0004°6¦·ÄÅ\x0015i\x0012è<¬A¶¦Í\\x001cA Zds\x0005þÛÒþM\\x001cM£¹²KuBRÉ\x0006ÚèBlå\x001aä=\x001a¹\x0002q±\x0000\x0010rñwTc\x0011­V®a6¡Ë\x001aNª¢T9íEÃ®Þn» 5Q
.è
TxõÍ\x000e\x0007A',ÍÕè»z¸þ\x0019þþóß^GQÄçÕÇçÅç¯«ïß\x000f¼U\x001bÔN$ß%\x000cI´xpP}ËF£Ø\x001dÎ\x001fqµø|~º¼¹¹:¶>³ÛÐ\x0002\x0016og4V·\x0005Ll\x000bRÛÀ§c\x0013\x0019ªÆú.*0·Ê\x0017mr\x001aÑ\x0006'Q\x001b\x001aÏ \x00026I3¤ÕC4c&Ûà<jaÃ^ôÈÑ¡.ÂJ\x0000[n mp&µÙ-²Û@A\x0016EßTsÏön­F¶ÁÁÔd·(ÊÑd8C/æ§6ãÆº¯\x001dlô|\x001bãl
N§Z\x0017UF Âaºåxjc\x001bæ½[Ø`5&`S<![\x0019_nß[N¨F´AB¹	MJNw[\x001dx*e\x0002´±I\x0007Û SÛÆ\x0016ùd·Úq¬rNôÀl\x00172L6±Ánù2nèLP\x000bøñ³w)ÏkFÓ[@0O@UÊÇÂ¶-Þnc+ú\x0015­lm&¸Añ 6,àÍ­ú=Û\x0000\x0001MG¼
4DZ\x0012>cÆr\x001dh4Â¯\x0019Í[«\x001c*\x001cd½RÄ§ÇZT\x001dl,\x0004ÒÊæYë ±QQ²Ör]ù>Ûéò ¬f6\x001c¨FÛ\x0000xI{Ær}!\x0004(³ífH¹
ÖvSTd®}?¶V5¢)\x001cÚÑVdR\x0005µ¥èÀ{Tçut Ñ\x0014Éf4ðfx\x0008Éó4oìFÍ_m<ú¬
\x0015¹\x0007Äs\x0011¼®Úö°ÝÈ\x0006»Àtì\x0004m%+Ô#\x001b,Råªù\x0007\x0002\x000f\x0004jfs¶dÒd µ\x0014i\x000c¿#­·÷F6\x001a\x0019×Î\x0016I»\x0004Ø\x001cU(Køgö¼\x001b\x0003*;Øhd\3\x001b¢¨ÒsDÓ -í jþuÇ6³a\x0011Êú
LÑ>u%\x0014ÛÞÀ\x001aÙ`\x001fØ½\x00105ðà¤,Ïã»béïÙ&ÒÑÆæ`\x001f¸½E¾ÔG)\x0010Üµ6\x001dî\x0016¹æ\x0014B\x0015Ì&¸'Ð
Ö'0\x001bãÑ;ØXª¦-à¶Á1N4tÆJU\x00124Û%\x001aÙh²m3\x001bê
R	wVîÈ\x0019¶­Ç¡\x0011Ý¶Íp\x000bR\x0013g\x0005wmiïf£ñ¬Õ\x001c\x00085\x0007ú¤ÛS |Îëù7y,ò=F\x0003\x0000Kk-X*ØÖ¸-9?M|ýþúO?V\x001fzÃIkß\x000e%u,\x0002?x[ÈÃpØ\x0007[m-ªûp\x0003Ö>ììm^ó\x000cÄ}&ò@Lkiz¯!é(¡=Ý
°oa®Ïdõãùd\x001eÏ#/Ö\f¯½ge8±­\x000f`:Ðúz*ÖôÞª\x0014\x000e¤)Ë¡hÄm{©Ì3|\x0003\x000cäi 
nPé­\x000eGo
	6\x0001
\x001eY§\x0002A<í³n<ÃGè(yhû¶üÊt Aâx2\x0010yRÒ\x0013\x001e\x0004Í£Q\x000eÐ #;\x0015ÈÜ
\x000f+=\x0011\HYXOm9ì\x0003@«ç¯¿½âè[\x0019q
áß^V\x0007\x0006ÞZÌ{Ñ\x0011l1 ÏÅX\x0001B>£\x001ak\x001eÞ|¾^î\x001cs[0\x0014ærÒ\x0018Új­\x0016\ó\x0007\x0018|Ü
\x0018¨)~LÄ<L\x0012§N\x001bK\x0018|½\x000f\x001b»i?pÿxùò\x0017\x000cB0BÂ\x001fø¹z{|¸Yígø1R¦ÁjËË$8OãíaÕ¿\x000cþãòîâüìz¹\x0003Èüüóoê¸JÒK2þH4ÿõ¿_ö/Z«¢÷46}¡\x001c\x000f\x0005cyÀO°bC,»VlaY{ÌWOY\x0002÷­\x0007xÑ¯)\x0007XÐyR=ãú\x000fXÙ¸||¼Ï\x0002t§\x000f¿¬\x000eÏÖºÌ#ñàkHG\x000fÁ*\x001e¹åÅÅYÖ;=ÿ¸Ü=>º\x0000ê! î\x0004ÌR>\x0008!­"å$\x0001q,\x0011Òh¶\x0007EÊk]\x0010f+ª±ZH3¢\x001f"ú\x001eDç\x0017&AC\x0006TÔ\x001cäØ[M&´2Ô\x000b\x0011_qªxñöõáy\x0002"D\x0003¹\x0000Ká<.¯éyÒ3ð¡Ç=9kÆ»Óó«	j\x0008©º ±©.1¢n7½æZEáfØ¸É´3ê!£îb´<\x0005<\x000bç\x0007\x0001w\x0019;vH34\x001d*F\x001acã
W\x001eIeÊÙèFmg´CFÛù±i¼7\x001aR\x00012²!õø@ktCH×eHÍÑ«õ=àîAÑ«ãêvH?ô]\x0014eo\x000b.®T\x001dq\ÄØÎ\x0018¡ÇpdHa©FOâè)DuÝq\x0008\x0019;·MNÁ×öü.¡\x000c;r\x001fõÜ¯-kOÞãÊ\x0015æÆ"Q\x001d\x0014\x0007'Ê0NáµSVnRöùIIE*Í¤í­Yzw\MÞÎXy ÙãT.áµiyVÒ·¶\x001e×5µ#V[[öìm|ÏÎ¥\x0013ÊzÁg9áØÆ¹Õ¶]û\x0006\x001fÊrÖÁ
M	Rñ\x0018V§vG\x0007)Í8¸0£àâÓÛ\x000bÜ\x000e0\x0006\x001f§ðIæÞ©ô|ø\x0016ºÓû|º»«ÂA>3ä3=|\\x001d ñdÌÕ\x0001HËÑ¨8\x001bÑ
\x0011]\x000f¢Á\x0012;DTÑRÂñÜ\x0018ÆC`\x0011Ã\x00101t ª@óÌ\x0015\x0004gù1Ç«\x0018µQ\x00025ÏI×dUü"üá]:²pAs\x0016\x000bu(÷\îÎf\x0007äy
* ®Üå\x001c\x00174ô)ýìGÕ¶BÕ¶\x000fµÔ¬à\x0010v.AÒt³ÀmÇI3\x001d\x0014\x0007\x0007
@Ó\x001c¡\x001ePã©UY¦§qùc,\x000b1:H½ªH½ê#Ý\x001fUá.y\x0006§
TC!Ü]4\x001d\x0015ëv\x0006¨øk\x0017ª¼PQªJ¹µ¢4\x001cÄ;üz\x000bª«Q]\x001f*l¤¬å,qb==ñkCíþ*g/\x0000\x000c
¨Æw.\x0000Î*Jl\x0017æÛ§ïù\x000bÀ\x001a5tz*Aº\x0012¥]å¨³Y¡LÅlT_/\x0000ß¹\x0000¢¦\x0016g@UÔ\x0007\x0006¦6b@Ýu~6m«4d{´µðO].+%ëËÝR\x001bÍÄQÌ"6Té¼þCªyÞB*\x000fÚ<0¯Øò0o¬ãe Ç¢8[Hå\x0001R£¤f»s=Hª%©\I\x001cXäi\x0016lS1Výè urHêd\x001f©de\x0008ÜO|\x000c  z&Åþ\Riª¯¿ö \x001aÇ%JRËÈe@ÚÒlJe7^¨:P}ê;Q­ÅGXDË\x001d7]h®zTvWs
i0¢¾À\x001fê«ÈÍóÛËÿÏÜÛ$Ù#yWñ\x000b\x000b ø\y0<\x0019LaÐ£d,zÓâá\x0013I\x0011\x0006ÙÅ kÑ«¾Fog5u¼I¤¡\x0006U<S{Ä{\x0006À\x00163-ÓôÊ.ù=\x0018ô\x0003ê_ÿqõ¸äÁ4ë2ÆdF}\x001dÀ.äÑo\x001fÞ?¾h\x0018Ñ¬\x0011Í\x0000¢á¹¨xî /í\x0003¿#§Ð¾SÚh×v\x0000\x0011+8h¶
<ÆÐ×[÷ä·\x0005`ÝnèF\x0010#ÏLCù½Ò£\x0011)ÕËíK÷~è\x0010\x0017¾\x0018k
gí\x0017lûÂ}'_Xó\x0001¾×ÙDf¤údø#ÛöÜNÂ´&L#<¨##\x0015û¡&)\x0011Âö!´ðteòÊp/b$uJ@­\x001a*vòK\x000cÒR½:Å(|¢\x001eq8{¢s\x000c\x001a7|ôü¡Í¶\x001e«\x001bQøD=â\x0014½¢\x0012g\x0010øâÕ'.Ïg5cÝÂãè\x0011ã-W·ÄR½Aq¹M³&
b;ÂÈvôu¾gNÊ9ñ
<¤ÙÄm\x0011W¿Å¬Ót²uÞc86%¾QÙ3ÃÙ\x0016w &yãÿ°Üx}úÇçO7/þùüÇOüì«TqË1´÷xñ¾TªðtN\x0017ð
C¾yñêþÍÍî~-á7\x0017KW\x00187Ù5.ª«ò:J\x001cPí\x000etWãB4Û
0\x0006\x0004l\x001aÍ>³¨q8P<\x0016'.SWm_
FxõÚúÓ_ôbþcÀÀý\x000e°3QÝ\x0012×
tw\x000c\x0001{±\x001bð£ÀÆ\x0006\x0003\x0013H¡=j>a¸¨¶£}ÆC\x0010ÀØe4ºÂ
c\x001d^4'ZaÃí\x0011¶2\CÀ ·\x0004Ll	\x0003æÿìIG)Ä\x000f²{Û\x001e\x0001\x00040\x0006ÄÑ\x00156tÇb3*\x000fÈ{¸\x0002ûmÿÚ\x0008°ÆÚêõÀ\x000f\x0012çÿ!Wè©L¬Ê\x0012säuþ¬X°\x00138ÇGy¶ÃiÌ>úö|s÷é·/Ï7ïþù\x000f%Wç;~5ù¿F\x001dÙÙ¹QÛ³5gi¿Þ¿ys÷æÇÇûw?ÝãsIsÜ\x0005Ú5©\x001d"Ø³`V\x0019\\x0000CZÇÖí\x001c¼!N¿æôc\x001aÃPP¢\x00133\x0018Ç\x000bê¶­y#¤Z­I±4|\x0004\x0015ò¥\x0014\x0010\x0018ì_¥ÇPOáÌÂÙÅÓ\x0008)\x0008R\x0018$Õ\x000e.y®\x001eE
¯êYeç\x0010k\x0010¬ap£\x001a¥7È\x0001o¡L&×Tï`MJ\x0007ÑÂøõà²B¨ËjTÑnló´\x0001Ì¶=mTº©1?\x0007\x0014÷Áa´W¹´×\x001aµ\x0015*\x0019buÕ±" ¦ÇçÈr
à\x000cÉÙ\x0012l\x0003@?«\x0007á\x0002<\x000cú\x0000Ó±ÀæÝ@oùëAm¶¼íÉf\x0000VnW?º_±SÑÐÊæ<Xùp\x001d²ó^À{ÉêGYu¤ÃBfµ4w\x000bB¤þ\x0012Iz\x0000l\x0012î\x0015ÿ9\x0006\x001b2RaÍ¶¼At4#Ï.\x0013ÜgY\x0003\x0008O\x0010`Ð\x0015 \x0018P¢ê\x0013XæÍ/° ¹ºã\x0010V+Y\x0007\x0016¯\x000c\x000e©áMPWÉp¥ÌYië\x0000k\x0014^\x000bÿ9ÈÊCM2k¢ËA¨ÃÙ°(@*`Ó ¬åJ3ÌXè)
\%¥·JB\x0003°ùð¶Å\x000eÁ\x0006PD
¤«­x\x001c
ôYEJ?iR"uYÌu\x0014h´n
Tec±uÚ´´	Áòï\x0011ÖÏl\x001cf-jp-Gïrqò\x0012ÎÊ6\x0007`e0Xþ=\x0006ÒðÅ¸ð\x0015µ(%\x0019ëjª¶í\x0003´ÁËd\x001bÿ=DäTÓ\x0019J·óò>8¬\x001bJ·Ýúvv!våvv$ëÎ¡ QÒ]s®%nqÖ=¿uóz\x0011ã\x001a\x000f2'£
5]åe¶ÔH}\x000fy>åy\x000b-nt!ò\x0005\x001d\x000eÓ£®\x0017,öåÊmur²Í)ÿá/'{ñÏ§/\x001fÿ¼ùáéÛoÏ\x001f>\é\x0008´AæqlK¥*M%VÔ\x0012á²Gþ¾ó}ñÓÝãëû·7?Ü½ÿñþõÝ«v #Ã\x001a\x0019&szÃÄ,~«ñÚ£\x0012o/\x0014GíØN\x0010;uK3%ð\x0016ÖØ²$	Ð\x000e\x0013»5±YãÀZ$ÜU\x0016§Ý¶ë\x000f#û5²YdO\x0005-ùX\x000e8gµ¬2U®£&ò÷Ã]?rX#\x0019d@\x0015²ÊÛ!\x0015weä³çQä¸F\x001b&\x0019Í=¦Êð4+\x0008æû¯\x001f9­Ó\x000c²åaÝ9[çö9L3\x0018¹\x0011DºOWV3ÌUvÖ\x0018NYt\x0005âVëjYFP7Pä3\x000c_AkU5× 6r¢ýÌ ¶ÝæJ­¢ßoß2õ¿þß¯ÏOß®°jo¹\x0014%UÝ)UÅ?Rlø\x001fß#í»û»÷×\x0010a\x0008Cûp&ÉÔªhjaY#jìg4kF3Â¢`^\x0018KÙÖË¢ZGývÍhG\x0018C$Ñ\x000c.µVµê(\x0015¿õ"º5¢\x001b@Ä& âDSó"Òè³¨f\x0011ý\x001aÑ\x000f!*T¥*ÕeäN´¶µð¬X¦\x00171¬\x0011Ã\x0008¢q·.VDÒUÔáÄ¸ÕUìfkÆ8Â\x0008j\x0001§Rß¬v4^\x000cK1¿ßµ1­\x0019Ó\x0008#ÊÙ8ª/«YIÞ\x0000Tt°cñ\x0014'\x0017ÿ­F ã¦Y\x001c_\x0019KªSdïèÎ*{!e\x00192¨Ç«¡Bà©³wê3\x0007)Â\x001e3$V y&\x0006UKo\x001bû\x0019EÑ#q\x0006¯["U\x0006`y<pÕ´mãÉp?¤3z$Ð\x0000¾»\x0017FPa>6#Núp-Â\x001e3(t\x00181VPôìlÚ£E Ñ#\x0006!\x0015íÇ¼5\x001d}ëÀB\x0012Éêï×\x0007ì\x0014¡FÄ\x001a\x0003Þ®\x0000G¿²¶It\x0015ò¬Ü±\x0017Røq=âÈYæ­\x0015HKÕx\x001aR
6¶qØ
	ÂGÂ4ùtÆQÛCí<¹3aÀnHá`Èÿäz èUÔ'È0\x0019¶AX7\x000cYwÛj×]àhLõ@¨Å2iÝëR²ðÕEiÏW÷Õ\x0013á½
u\x001fiUØ?º]µ§êºüeL\x00083>ß||ºyñù¯ÏþyíHk±Fâ\x000eªg>ÜÔ°s61ïoò\x001f_<üüîþíÛöi¶ \x001aµF5j\x0010Õ%\x000eAyzM×ÝOeÕ	V7ÆÓ\x0002íT°Ç{aMUbË{v±FÁ\x001aGY=\x000b»¢Ö"Í{Èù\x0006­kT-ÓïaµfÍjÍà\x001e\x0008d'ò\x001e\x0000níÇñ·¬w\x0013\x001bñ½Uì\x0001;¸\x0007lXäå\x000b«æ[¹¼Yõ&¶®\x000eºX`
¬1TqÂ|T§>t[ó¦\x001a¹]\x0017j\x0012¨iÜ´\x001c¹\x0001.XËÿMÃ
#\x001a\x000eXU§×¨N\x000f¢âh\x0017BÍ1:'±JeÍÎÊGXe¹AËÂÙ_¤\x001b\x0014öc,¨ÜÖý=}Ê\x0011TaXnÔ¹æ,*c\x0011ÐXXë5HDE¤yVaXnÐ°\tõ\\x00075¯òª¶75Þ¤ûPa¹QÃÊy÷u\x000bD\x001aÖ\x0018Ô¡[ -\x0010\x0006·@þ3=wÀ¹À\x0012r­Dp\x001fª3KølU'\x001fðãó§\x000fâdÎ§>]Í\x0012C÷ð&9Cü7Èåµ<+;0êWoq>çÝOwÍ	\x0015\x0015Ö¨0\x001aU\x0019&íG1'ÐX\x0014\x001bõfÊ\x0008¦[cº1ÌüÿÓ+YFI:¬\x0001ã\x0015m\x001dúºPý\x001aÕ\x000f¢æSJÙ¦xó@\x0017¶­W54ª©ö¡\x001a¿yÉX}ü¿~ù×ýö¯ÿúòá\x001f7?øóë§W=@¸M¥æGP[\x001c\x0015=ÈXÝzIøëãý÷¯^Üüüêí»Ç»××í\x001aØN\x0000\x0007Ã%\x001a\mZçéØV{ûýãK/°_\x0003û\x0019àÈ\x0005kÙ x ¥×4 ÃæûýÐµ\x0017ØºÍûaþÃúýðùÏW_>\\x0015l,vÊjv¯XcW0U:kËå}ûöæÕã«fß\x0012ãÙ5íÇã\x000b4|Ý¤C«á×$«Úõ>:¿¦óýtC¢DÚ8®çBùö16¿ý°~ýaÿöôÿøÒx?~¼ÚñÓNj\x00004*ù*â\x00024g
Ç%}ÿóþíîÅ¿¿G¼×¯Û\x0015\vë¬pK}¨\x000fQ8Ð§!\x001b.ôF}§\x0003HÍÔ\x000còè\x0006£bâ\x00131Ü ív>Ê\x0010©]ÚARLô
iUW0VG\x0002\x0005ÿ}\x0017Ô\x0007êÖ n\x00104Õ
ïãòm¾lèú\L}\x0004Õ¯Qý(ª£)\x0015\x0006\x000b¬e\x001dGÍvß8ö¡5j\x0018CÅâØÈþ)²B+O;Ê¤k´>Ò¸&¤*qÿ:Í
¶[>Ujnö¡¦5j\x001aDÍ|åV\x0002ëæ±Ö¡qw¢:\x0017b\x001e@ÕÒû\x000fºë4	.àÿa\x001dáü×Êj\x000fØ«Z¸=èÿ]\x0008$7\x0007)\x001f¥é­ÌóD\x001c«\x001aõ}¨ÂÿëÁ\x0000`ñZ¢&%¤db½ó¼ªgÂx#¨"\x0000èÁ\x0008àr¢ë¾äT{³PÿØ­w\x0000ª\x0008\x0001z0\x0006à-ªÒuYéVÂò	JÅF-t\x001fª\x0008\x0001z0\x0006¸¤X!&¡#\x001dtd»RØ\x0001z4\x0008$#hØ\x0007P
èxì.®ë\x0011[@D\x0001=\x0018\x0006¼:2bÏ\x0017mWÃZÓêlàâ\x0010«\x0008\x0003z0\x000e¸\x001c²8¸\x001aº\x0004[×ô\x0000\x000fpjú]Òj5¸¦Ùh\x0006\x0003z\x0000\x001a\x001fì½¯kz6IgUÄ+\x0018W8oZp¯Ö\x0003_}@£ñ»U\x001eW\x0006ãÇkr7<ðyÅÇÀ)>St\x001ea\x0015\x0001\x000b\x0006\x0003Ã\x0007_^WM\x0013&µ³>Öu= ½\x0002\x0011±`0bùHÔ*ïWË>\x0000ëÏx¿6ÎÕ}¬"dÁ`Èr¾¾P¥È×\x0013.²üÂÑuó¨"dÁ`ÈÂA6¶k>\x000b¨3
ÒÒûj`÷±\x0005!ËEK\x0002ÔyY#ËÙyÍÔÊ6º\x001cúXEÈÁ\x0015´;­«á\x0016®\x0010x|Ujô±\x0005£!+Yr¯²y2¸#Ü«\x0011aË\x000c-T3ÓpZ×r"\x000c1qR:âmDØ2akiü·5\x0014°n®©ëÚVéC\x0015QË\x000cF­`"U$#lÙ®Qñpßì\x0005Ø\x0002òm0jåy\x0004@cvsæÂ÷WeÄý4«\x0004f0\x0012xk±M¯l\x0001Ë­\x0019>:Zúl\x0018Î\x0008«p¯fÐ½z§éñ'³z®\x0000ðÉñ¡°ñTÕ*<\x0019ôX>°\x0014ÔbY4èz&ÔG\µZá\x0004ì¨\x0013À©\\x0014\x0008Pç² Z¾\x0016Tª!\x0005Ö*\x000cË\x000e\x001aVPëTñø¿ZT¡É·6ô4úXaÙAÃÂ8\x0000t|É6Fw!q-`:Å7f¯«A)Õ^UvfÛ§!xÈÙ6K­©p6égè`lM4¤§ \x001c«.\x0006~XÝ¨RßË\x001b¶ïYaýõüôéæÅçìéJÈûV]¬	ä!:®^kÅ®û»77/\x001e^\ªµeJXSÂ\x0010e\x001dcmQ\x001cRÓ<ÁÀ½£Î4úËz0Í\x001aÓ-&`cGYÌDe :çÔ°íU£Å¬\x0007Ó­1Ý\x0008&/y`þÏ¯/\U¦ÿæZ,¦\x001e[M|µ*íïX¦äÉpJqùè®\x0003vpÕÔCË¹Lä$Nëêø\x0019~\x0010vÎNôõµe\x0010×=t1|NX©îÏ\x0018\x0004ïLC\x0001²\x0003s}¤
âHÕ\x0019ù®Âº\x0014¸ËT\x001br-é.$ý<z¥µïqLBiþöþÔÄâ\x0001®Qó³\x000b6l\x0016Ú:ù¿=}ûò¯ÿïjQE9çuÇO¦ÞWêÖ;\x0010Rþíîýc[K!a
	C3¨\x000cYg+\x0018bq Ó,¥YS1Ê¥]µR 9\x000fÑöLÁ¼\x001bÒ®!í\x0008¤Å\x0019å\N\x0011oM}úõõ{Op·¦tCZó
ªVª¶¤(_×2]pû(ýÒ\x000fQbê¡Oå>D	Ph¦!Ã\x001a2A&º-ÉK\x0019j\x0017
$.K¹wìkÈ8\x0004é4]A\x001a­Y^Î9#v­ÛÒýi
 -\x000b\x0019àÜ]¾Ì±ÖÔ\x001aÃ¨ó~ÊS{ûâÐÕ\x0010¦_:"
&ÏgÕx¿Ãµ\x0016©\x000eL\x0019w\x0002u%1µ\x000e·ÜÄÃ¢ÃÚ·ªeöSÀ£"Ïòë©r×ð\x001d®Ë\x000bË»­{ý"òlóá½ß\³.¶\x0006à\x0006N\x0014\x0003âÕl´u`Ø£S\x001a±\x000e´\x001cwºçÕltu`à³ÍÚ÷[PàrmE*ã8ýz· \x0011}ôPøq:\x0006\x0018\x001a\x000e6D\x000fÃ=NÇ\x001f-âÏöp±s5C(\x0012vËbzîØT§ÅÍÝ´\x0008@z(\x00029p­c\x0011\x000c?Ø9Ý\x0017sÞD\x0008Òc1(çè0q\x0014\x0006UB(ÖâÔÁÏ~s\x00101\x0008bÃy\x0017t8ÇçsÇõ:µ
KöS\x0010\x0004c!(\x001f"ÙÎQ5¾¹®gx6¯¥\x001bS\x001e~b\x0010v\x0010ëÂeþ\x0005­eäê\x0017ZEeû)E\x0008¡\x0010ä/äq	YDÑr¸ØºåÞ)B\x0010 \x001fX5\ûxË-¬Ã}>º¶\x001bR\x0004 \x0018
@Îx,È+k\x0019)7rÞWói½ní§\x0014ñ\x0007ÆâOÔÕ\x0017\x0005[[07&4´Ç:(Eø¡ðã²7çó7TÑëZ6\x001aE;(Eø±ðÏâ×2²\x0004PÎ«æú¼+\x0012ág{\x0003·×zx:#¾\x000bÖ±Äï® ül:lDø1CáÇ«H\x001a!FçUôäêNrû.4÷aøcâOõÔ\x0006Ä5Ø©®fC.­\x0003SÄ\x001f3\x0014|öì4ÇJc«\x0010\x0015\x0006\x0004`åz>ª\x0019yû6\x0016Ê,òòÑ5\x0006yà*aÐÓY»\x0011\x0001È\x000c\x0005 ,] ÁP,e5Cí\x0005\x0005Óª¶Ú)B\x0019\x000bA8»Üf^Xªaô&Ôy0Õöa
ïn¼»W*\x0016òÞÔ·-³\x000eVÕ~Lá7ÍßD\x0013\x0019ù£g\x0013bKÆýV8$;ä²±pD
àêÞµt+,Ý\x000eYºÏégÌÈï@>L¨U³ÚqV\x0013Ï@å¼¶}\x0007Ú{ÊÐxNãK\x000fÎßUôõÒcú\x0006ÖliÍ ,>\x0007\x0001ßÊy.¬2'+eÓ\x001a^Z§7\x0003\x0008ò\x001f6-Ô¯?||º~
i;WÖ4µµ\x0019@Má=5\x0002¿~õúî*\x001f¬ù`Ï±8
RÒK¿5µJ-í\x00044k@Ó\x000fhL-ÓÀ÷F9Û¨¢Á©¥ó°\x0013Ð®\x0001íÀ
V\x001d}t´µ&SSf'[ó¹~>pµöL\x0019VGXêvh\x0001[Ún;ùüÏ\x000fðe§è/ñí\x000bv3ß,`\\x0003Æ~@Í½g\x0010­Î)²ø·o4tí_ÁµC,«¸V\x001b\x001cùÐgYX]ËwÃ(§·*­ü¿lÕ°~ùøôû5\x0019åzÉÓ¬vï-5?ï¹ü\x001f/	
þòúîeS\x0006!a
¹ÕCÜ\x0005©\x0015
dHU!\x0015\x000f#×¨Ù9	iÖ[­®]`©s+oOàÈ¼|W2^R¿Ú\x0005i×vh%-¹F|]&×ÈãuëöªÐ­	·"Rû\x0008¹±8/câ\x0006H­©KÇåeÞ~
é¾õrÝ»@ê!sÆC³HTjÔv@5äVål¯Õ$ZÉ\x0010¸ê%Û
¯¤ÑÓV\x0013×[Ë}+éP¾¬dÕ\>YJM%¦Ýi
¹\x0015aÛ\x0005©|õ?X{ËþG³l\x00149íg<=Ü/|«ÄºÏó\x001b®Õ\x0010¸Ã1{rrùÀÐJlwSÊp3\x0014o¦äÑâ;\x0014/©X\x0019Úe¯4kÞZÄ\x001b=\x0014p¬¦9¦ÑüG²\x001c\x0015\x001a\x001d"Þè5Cl:)qår6\x0018rBÚÍS
w®GüyæaW¹\x001c¶éGjhwÚ7ÊÚ:(?×C\x000e]9Ù^¶%u¯,Ü63µÝÂ¡ë\x0011®b Ý\x0015§%e-\x0015SbÙå$¥ðèzÈ¥+MU\x0016/«HrGá\x0014MÚ-\x0019ýýÂ¥ë\x0011®²#·´ÀjK«\x000e³Î\x0012K\x0011®Ã7b;+ÆTRu%§SJ\x0010.\x001dF\zN¾é±Þ\x0002Æ Ú½¥Ó~\x0008ä\x0011bÄ¥«2©Øæ+ÔlQÕv.*ï¢\x0014>\x001d|zp(QVÖ²ÞN)\x001fø¤\x0013\x001b3<;(Å!\x0002FN\x0011X\:qì0ÛNäî·Op\x0011x`(ð\x0004àÞ	ÈG\x001dzÄËÿoø§FyS\x0007¥\x0008<0\x0012xr äÙ9ç­\x001f<Tg\x0019\x001aO\x001dÂ¥ÃKÏ<Tl·eà\x001e9\x0015\x0014{Ë8}\x00007Â]Í"ØûÅKåªÅ	ÙÇ²#JÓáÑ\x0008Gd\x001c\x0011Î.î´-¹pÕAK9«'\x0001^ß^Q\x0012,®¯vòÌJAr±yºÓð¤îák$wÀþÇ·§
,þ¥\x001f6\x0018>¥åÿ"{x\x001d<\x001f%ÁOçpðß¿>ÙÀâ_\x0006`#\x001fÎqCPZ¬yd¬	¾ü\x00079\x0007ò/ÿ\x001f\x0014óþöåæÅÓÇ?¿~½ªëí
+b©\x0001µ*ªí\x000cª=6åÇ¿¢ª÷ûÇ\x0017w¯¾÷î*ºY£It\x0017XQ\x000bÓQz\x000eUý\x000b uâ\x001cB·kt;\x0003ÞS­Ö¤ö?¬Öæ×´öìÃ\x0001t·Fw³\x001bÆ×ò\x001c<¨¸+\x0000¿bj\x0014¡5zD\x000fªjA:r!p;#\x001e¶Ã«zÐÓ¦\x0007/ÿAN]£ÿóéË?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-11.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=J?\x001e=?\x001eáÓF%íß7\x0006ñãû/\x00176ów\x0007ÝÝÁ¡ÜA7\x0010g\x0005u\x001bBøª<Ïï\x000fÊöîT4\x001d¿\x0008äÞÜßò?ÇÃ5$÷u»\x000c\x0011ÍX\x001a¤Ç¦fºàæÃ\x0015#\x001díúíWo7ÕÈÅw\x0007ûka \x000c%\x001d9c£6 \x001c¼õï\x000f¨.y\x001bÁ/¿þöñüy3\x0014/Ü\x000c¸ m,ÀÇH±2F½aS(øQçaÃ«QP\x0011nã\x0001éû±ùA\x001cèy{óéâzý.¢»Z\x001f<»qJ\x0011'Ï\x001cµH¡·\x000e\x0017Ô
$\x00029/u­î«ÓÏ^¬¾`Èé\x0014\x0006,EØ0FóÑ$\x0019º(¡yÐ¥ë\x0015±7Ø\x0005©;_\x0015Í®Jèj&tãh4x\x0006[rI\m5ÌnJèf\x001etCÀ01\x0006úAäÑ¶»m6vWbw3±ó'\x001ao»Êl©B©ì
E÷³ê¡²Ù\x001bO~¬bhõ\x0006ðDk\x0007ý³ÁWOÏ|«A*k\x0004/\x001dyá?¸±M\x0017½5¼z¬|æk5\x0012Uk`þÅ`\x0006ôb&ì\x000bC¯\x001e+÷Z?Kå}\x001aú!18EU/Vªe/|õXù¼×
\x001cå;\x0010p¡¤D\x0007â¯¹.æ\x0017Õk\x0015ó^k°¿(%¤°Zcý\x0008\x0005Ö-[TÔ@õR© ß4\x0003}ìQ\x0019}mª²³o\x0007Ó0æ_ùï\x0013amqíá's\x000e \x0018æî_*§¡l1E=­aÐ¶À\x001aÞ$\x001ab
ðYHPFD9"Ä	gcè\x0012e%¾ÚZ»\x0004a9\x001dL\x0006j-ã<	O½È1¼ÿCÿþñsÕ\x0005ã>?¼
\x0000G}&\x0015¼\x0004Qp2';\x001d-\x0002³ÍÐy¸zu~\x0018 ìòä\x001f·ü×ß\x000b\x0014¯ï\x000fþv16ªI8\x000b¡\x0012tXÇ\x0010 IM^\x000e»(\x000fþv´z±ãw«5ÿø[\x0008%£>:L'\x0007
|öpFI9`3c5ºÌå(b\x00106úþ`Ãh¿\x0003¸¾Ã\x0007i\x000bþ¶¾}wy}ðâ&x¸\x0007ß¯?Caf\x000e\x0000\x0001q*0\x0008o\x00167×<B[~üâàÅË3p¬WÏwáäßÀóør<{rópywðâÿùa¼;;ÜS\x001a^\x000cù\x000cl/á6\x0007Y]l\x0000Óg»üúàÅÑ³Ó±àT	NuS´gña²sOV­~\x00168]Óà¤ÂpT0
K#\x0018ÕF[1\x0011[äz-]a¥hð»ðôÃ¸ËëÑ\x000fC-$
\x0005åôð#\x0016tÏ¶ }\x001fÞÿs\x0018{ùâñé\x0019(¡>h"Ó|Y(\@hÈ
m£z\x00164YB»Æó$UI]g%ÕQ@bz\x000e4UBS}Ð¸§ñ0yÁ 6«¶ÀÁMØt\x001f6%ÐÒ\x0008\x0006éLÆë>õnh¦f:·MçRgn8-õãRVÒÚÚëÆfKl¶\x0013 É\x0011\x001bqt¨¥°¹\x0012ëÃ\x0016\x000c\x0007TÜÀËÄ¼ç\x0002iæ	\x0010_bó×MQ\x0003-)\x001a¯\x001bq38[WjôB+\x0002\x001b vY\x00176\x0017)	·MúÎ\x0011mnØ·y×:¡O)8')\x000e73_8½¥é»ÀUZ÷© fs&KztË¤µÊ/Õ¼×À+áËû¤¯\x0003jA|ªAéã\x000c\x000b»\x0011qrãã}2\x000e\x001aÙ©ä.(°d#I«28]W^t«ä\x0008ï\x0013$Nu\x0018=½ö³¨ªè{ª@\x0005äè©*d	rÄgú
?OüÊãv\x0012ü \x0007¢4YCHQ"éÏ\x0011þù¼7Á\x0010¸ëÄèú4\x0005\x0011öHë³97O÷*z\x00127\x0011~ÐeoRÓBm*\x0012rI·)ë'ôÜÖ\x001eºî=Ôy\x001c\x000ct* kÍ\x0011d¯ÅÄwâÈ[Ýü\x0000<£ë·W7w\x0007ï\x001e\x000e^­aÒ8yf\x0010ÂO¨¹\qªwA(fþÊ.>zqxòòõÁ÷ç\x0007¯V0Zéåù~¢D(ú\x0011º'\x0006sÃ\x001c¿U,ÙÄ.²ú)O\x0001(K²\x001b T¹ç\x001aÆÎ&h½\x000b\x001c:\x000f *\x0001ª~Z\x00158n= 44ÎÍÖ¤åS\x0010ê\x0012¡²èmÃ\x0016:¢t\x000bëº)\x0000M	ÐLÙB/ò\x0016
I[hò\x0016N&Â\x000f\x001er¸0á!¯¾\\y8A,ë\x000f\x000fë1ºd¨Ñá³É8\x001cò$½ÎÒ\x0010\x0018À\x000b«^°9?©,«gç«ã1q(ERô£\x0014FãÌ\x0007ð¾1%eé&Vj\x001aDYBS \x001a*ÅpÐsG ©ÖÉÔ\x001cÓ@ª\x0012¤¶NnÔK4%H3\x0001¤Fj(Ð2TÀ\\x001d1\x001f¢+!º	\x0010'38K2qºÄÀSÛaP	u\x001fýÎnÁo"r+Ï¨'I\x0008MZÆùÉ«ÇÍ§¼î`Cd]È©\x0019R\x0008K-ÅÉ¡Ó`VoOy<BPvÇåÜ\x00124¬\x001e\x0008{\x00178ôêõð)ÏÙ,+MÑ mònÖ\x0016ø4Õ\x000bâ\x0013PP-T$\x0001Ú\x0002ù4µ ÖRT/HLxAÜ3rfÀåÇ¾!ÉDÚ=\x0017e­\x001d'< îr¿S\x0016ôy)u¶Çå|Õ\x0003\x0012\x0013\x001e\x0010·º
Ê\x0004êÀc9©æ#Q= 1á\x0001ñLp\x001a©³°µìÝ\x000cXÍ§Á¬\x001eòóý\x0012@yÆ¹ÐóÌ åæÃÕ\x000bÝ/\x0008
¯UæÜòd\x0004KÏ\x0005\x0005£<7uµzFÿêQ,¿.QÆrìn{=à$§GýÓØ%Ãy>õýº2\x0017c?úêÚøà'ÝwT©Lß(5NÂV<ósH1ß¹\x0010n\x000b¬\x0004IÚM°#ß\x0000&çkwÉX%ûV±2>ÄÊ§A\x0015Æ\x0000p¹;\x000c^Ì\x0015\x0000ð~~¿õ¸ÞOx]â«ç>A]Bq#¾ÀU[\x0017VM{]0å\x001doTTvÇÈÏÍ¹\x0006¦"n~PD\x0018^ÝÜÞG¬§ë?ÿùû(ì½\x0001ª+ÄiÔÃéÞÒ«§g\x0011íéê?\x001a\x0012¨\x0004T	²öL\\x001b\x0006^\x0002ºK¡öÂT%L5	f\x001eã+&J\x0005	s²Ë(íÅiJfÚvÌZ\x0008MDxî\æs·»tU/PW\x0002uBxfEÛìÈÍ\x0005\x000b\x0000-üyxIl\x0012Rg\x001dÍ\x0000;\x001a=%A©r§CÒ´zJ|Ú[)S \x001bª	vï2ö{V¯OzNà0c®@Cé\x001b¾z'\x000f({'"­Þ\x0013ô \x0004\x0017Ä¶\x000c
LhMyâRqKì(«Í©ø¤
åÔõü-±¼\x001b®aÓóÏp¥Zb_Å\x0010/\x0017\x0013\x0001\x000bf($a¸ÉËåÎüAf°\x0017°\x0003\x001a<`,Øh)\x0018M.\x001fD@+¦B¦.¯©Ì[¹­Ä~Q/º\x0017(>d²úZL°\x0010\x000b<SËÛJªö S%2ÕyâIiÄnåuÛ%\x0007=ÈtL÷ ¼ô\x001dÃë&}8Eª³å³\x0012éÛ3IÛÚ
tÆdØm¨¶ø=ÈlÌvíËZ;N<ïLeV\x001e¶],ÚÌÈ\\x001f2OÒNÛÌÿÅT&éalÎ\x000b(Ðd.Bkfs}ö
P\x0012Wä´gÎ¦ñJlð.¹\x0001á\x000cK-¹Aú"\x000f"×\x0019Úv­y\x000f´Jnð.Á\x0001ÄDtÍh`uð\x0005³6¿3 UÏw½Ï8Ì\x001b\x0015Uxª\x0016\x0015<«BÌy¼z\x0004¼ï\x0015\x0004ÿ.Íe
ÈKRúÜîvT%w@\x0013Õ+\x0010}¯\x0000*.P¹KllA1ñÝöh/²ê¦¾fY\x001aJ\x0014CêXÁrÃÅ,=0(;EÙY£:ùß\x0011½Â7êÁ{À×\x000b\x000fáñ^x0_\x0002áÅ¹B\x0011^nÑ¶\x0013e\x001b\x001ak®~~¼¼>¸¸\x000fØ®\x001fÞìÑ\x000b¹\x0000XI"Í\x0001½»\x0017§Ol\x001b§?\x001e¿88:\x000b(_?mÀ)Jb\x0002NÎ-8C*ßÊ7ÊìÒõÂ%L9\x0005f\x0010}\x0016\x001bØ\¦*\x00162Ä)ä.\x001b½\x0017§*qª)8¦\x00129	ä$øh<ñÓigw9ê½8uSO¹QÄSJN<áßF8í®Ð\/LSÂ4S`j\x001aÓ\x0019PÒ@7\x0005*Â4jWl®\x0017§-qÚI89Õ\x0010Kiì\x0002¦IÐ±/r=]ÓMÁ),\x0010¥¢i°Þ\x0012\x001f\x001etOéK~
Læ¨5[\x001aü6@Ä&©cuWV®\x0013fiZ»2.×³\x001c&é¨\x0001^zC;Fì\x000cËõ\x0002­Ñ$m$\x000cµñ\x0004\x0003
\x001bÅáà	([@ÊóJ\x0019ñ)ÚªD0ð¬µL ø\x0002ZWêOÑGÀZ! ßjq
Éh·3xØ\x000b´ÒG|B\x0002 ZB\x000f-\x0002Uôäí\x0002OW
OÒHÁ`B\x001e\x0000àÔ"oU¹©¡Ì|>ÐJ%ñ):Cæ\x00157TS³/36wÓï¬íÅY©$>E')åuq¦B\x0011\x0002ÊMJâSt\x0012Â¯0¡¦N2Æó_bC+¥Ä§h%Îr]·Ú°T3CäDFÉ\x0005vTTÒ^Löá\x001f\x0010JIYQ. <E%BÅ$\x0011juö<YBÓ`3y1»ê\x0015{qV\x0012TL Ò\x0010¡\x0016\x000cû2¨;\x001dÙvÆìÌ¿ô\x0002­$¨$Aen
\x0007SR\x000cÆes\x0001ü\x0014lzà2Çg\x0014le¯!9½w+ç\x001f¼­÷ÓNÚPÎ9vIá³\x0000µÔÑ¦í\x00027ÔÚù\x0010Ü ÈlR
c!Á^Îªsge@'PYwð×)Wtã§¬ÆZTµ\x0015\x000b<úa;££vÆ	\x001bu½çPÄö*\x0019ÌîJf¸lHuÉ\x000ce\x0006®ïîö01J_[æ)Ñ.
Í:\x0007a\x0004ìéêõë\x0006<¢Ä#Zñ\x0004_)\x000e\x001fñl\x0006'øíxa#\x001eYâx³ºH<\x0012\x000bØT8ª£Z·Gf:ã8²â\x0007
ÇDnw6ÂÑ%\x001cÝº;\áì\x0002ã\x001c1VÝÉCN·S	pL	Ç4ï£Jv\x0003³}h{AËy³\x0015\x000boÄcK<¶u{¤#j z\x001dçJÛ\oãÜ\x0016\x0003L#\x001eWâq\x001d\x0008û]NJAÕ\x0012íz}|Ç·î\x0015$|\x000c´±â4Ø<Å2\x0012\x000cMÂSDeÉ	Ï
Yú\x0004û¦ºÍ¨Â×Â¹U:«\x0000B\x00137	§"\x0018-ò{ßANÒ\x0008¨Î¼Y<[F\x0019W\x0003
vH4¹y`|âçtæÍâÙåZ\x0003còÖÂRõÕ`@T\x0007 J>óf\x0001\x001dN\x000cC¸ðäSèIAì)?ù-F@æÍ"Ú\x000b\x001a^bÎ#mÌtÆO\x0014A¼\x0012Ñ¼YF\x0007Áì7"\x0011\x0007\x001doæ?oWú4Â©$4o\x0015Ñ:Ø¼\x0018Þ0Z ³¿ÒÐ3\x0017M½@æÍ2Úå©¤0\x0001/\x0010\x0011Ó\x000eMÕa¼Ñ¼UHkî7;Ä*LiË}¾A\x0013\x0001JHf!í\x0015%ñ3J\x001eèQ¤\x001dÚ.Hi\x0004TIiÑ*¥JÆàh"=Öçj5ñÉÚn\x0015Òá²ÐpèÈh\x001b$³PtÛ\x000c>*¡(Z¢
NB¡\x00184,V)mÌÜG&*!$Z\x0012ns§y~d&ßè©\x0017¨zó¢õÍ+à¢ 8JG¡*\x0004gùD@²zb²õ£ÉS¦\x0014§©Ê,<Nû¬®´l¾ÒF`\x000c\x0005¦^a½fÙÖS½BYÝhÙ|£M>AÍ?V}ëMy\x0017Üíiª\x001b-otP¦TÚ/
éUÍ7'¦§îPu§eóL&¾yáàÉ¬5ôvYR\x001b\x001eU]iÕ|¥Á{W\x0019\x000f~hEñB§¦>zU]iÕz¥õ&µ\x0019Í¥´ÏÅnj»Ø­\x0011P\x001dZh½Ó0¾Sæ~\x001bd¥0\f=¿Í\x001aÕêÌW´èÐSÖ~m\x001f~9Î6ÖK¦uvYÅÄ{=èüLòº\x0019Vðâ³\x0006Q¬"Cn@+Ó±[|wìVðp\x0010ñ6Gd2O/þê¨\x0014k¥\x0001 I\x0018ä¨¶¹æTMNúÄ\x0018ilß-!²³æ,É\x0004ê:xDÃ%Þì-8\\x000c°àa#àÃÁáúqòg\x0019\\x001eYb(\x0014"µÉSà¶ïÎ\x000f\x000eWÿ>Êü D	Jt\x0012ãÖP\x001bé)¦~Gíf;(Yí `p«\x0013¹Þ\x0015g÷ÁpYªw3P©\x0012êØª`QJ\x001a'ë)R#eWêô6\x000fu3*]¢Ò\x001d{e\x001dµÑA[\x0001\x0016ß
\x0007î²íV;*S¢2={Å)\x000c	3ð\x0000\x0005uÌÙ\x001dQÑvP¶\x0004e{®Üâí(·ÇY·\x001c³\x0019+Q¹­âJØ´\x0014ï\x0017dEYogò%(ß±U0°\x0005Kº­Î#]\x000b~»·¡\x0019U\x0011¹\x0005	ÊzöjÓ¨b³Û+¹ÛtDM¡¼¡¼G2EB4 Â\x000e2ÉrÈt»±§\x001dT%Cy\x00105fîè ù\x001c\x001e¡¡q)³\x0019GX	QÞ!Ewy\x0004Jð\x001f0\x0002Å=´YÛFz;¬J^ñ\x000e\x0005bÔSERÚ FmnÝ\x000eê¶Ãªd\x0003ï\x0010\x000e09\o\x001ayP?\x0017£ÃÅvà©\x0001S\x0003KÆUã"\x000e×w÷7·ã³5¡Ï.Ýyn\x000cÖf@Â\x0000ÁP-`q^Ìë³§E\x0013ì\x0010-1Ù>L"wrr¯\x001eßäN\x000f¥·sû1U´<\x0001S¢åé\x0015\x000c+\x001cÂ­Ç\x0004Fpá\x0005ZÆ1j7	Ve\x0017\x0013´Iø¿\x0005\x001d2\x0008[^É7\x000fo?®¯Ç¦¦[oó,^/pXh¸õy¬\x0006t\x0001í¸õ/Ï\x000f\½8\x001b¹øvÈ\x001dlyi-·`bIó­F	NEÎ³/r?69t/¤(\x001fåÉåÕz´;]K3õDöE¦~ç ãÕXSº\x001cÚòRCR\x001a`±\x001c\x0004	cçjS^±N»\x0011.qé\x001e\ÜåqòÁßÈ\x000ek\x001eXÁå$\b([E­?®\x001fî÷Í|{ \x001eÇ\x0011LüCLr;\x0019üãêült\x001a\yçïìÇ\x0003\x0015·	\x000e\x001bïçñ\x000fÛï°\x0011,áÈf8\x0008\x0006È<¹ª6~{ÜC#\x0018UQÍ`|\x001eÄã$ÕäÎÓÖlÒ\x001aÑè\x0012î@Uê	mN\x001eM°\x000f¾\x0011)áV8FP¬\x001anÃc)GîÅv\x0002¯\x0011-ñØV<*h\x0014Ä\x0003Ìh\x0014c¤©`±Ro\x001a\x001e_âñÍûÃ(äiu\x001e¡\x0016þLÂÇ°-­Û§$\x0005Þ\x000c£Ù\x000fÈ	²-WTe¡Øæ>O</^\x000bÂfI¨\x001cµ<ÃQ\x0019S\x0016Îj»©\x0011O%\x0008y³$t9\x001b\x0004óËñ\x0002)æ²¶Ø\x000e&6\x0002ªD!o>³\x000fXastZÐôf\x000f3\x0013§\x0001ªÄ!o>S°[Î(Ò
ìCt¶}óF@Dä­"Q¬¼\x0012ÍuÊHó<\x001eh;\x0006Õ§\x0012¼U&*æHÃât>1\x001c\x0000WhÛÒn\x0004TÉDÞ*\x0014\x0015\x0010jäºW´\x00177CØvc|#\x001cWÁq­p¸¥²\x0018Ø\x001fuCÙNäÛññF<æ­2Z#ªIDÔX4ÃiXD%E«x¾\x0017K\x001eQ|gé2ç)\x000cÛ%Üx*ñ,ZÅ³fy\x000f8\x001bd<k'²³1ÑÞ\x0010µ¡Ú*\x0015í#kLêH'gzø¸D%E«|Ö<Ïo*wÌµj³õ~»*¯\x0011P%E«|V20Au\x0015Ö)ÛºÃkmDS	gÑ*µä\x0010dKÛcru\x0005N\x0008\x0002<_X%E³tV¼¿ì\x0002È\x0001­ \x000e'\x001fQCÑ,\x000euær3Ô*¥7¶ã·md%d³\x000cÒ\x0006þÄ4=U\x000cIª©òSmhY½yÙüæÊ\x0005«rÄmjÝ·kË\x001b\x0001UOL6?1(¦f\x0000CäcçÆ\x0016>Ñ{ÕÍw: Më²æ®vúUwZ6ßi dÛl\x0010Þi-T..êf¨êN«æ;\x001dL o3 NFÚ\x001cÙDÅªª;­Zï´f\x001bEor\x001d¥ÖÂÎíòF@u£õNC8z7CM´Ý\x0014+og \x001a\x0001UZµ^j\x0008sR\x0019\xo9ÌIzÕm×T5â©î´j½ÓÁbÞ\!M9I³éfã\x0013÷\x000fhÀ£/FÑý\x0006oCäñÏÌb2$Ükg,oçÙZ
¢!®°÷Í¸4\x0017{ùM­¹ÌvîVkÚ\x000eB®Ún"ç\x0007Wë×ë««=\x0012Y·Am\x0007öHMÌ$ rGêèàduðzurÒMØD\x001f6[$r7Ä2WÆî\x001a\x0010Ü\x0001MÐd'´\à¨a8ª¦ÎüÌü¶kl\x00076UbSØø\x0013M\x001c¥fÞ\x0004ÿ"sn\x0017¤uaÓ%6Ý
>Gz\x0000À&\x0002\x0018#F\x0019ÅJZÍØL\x001f¶à­$\x0015-lãm)¬Åè>R9G\x000f´\x001aÍ\x001a\x001féf4kã;Dé-x\x0018toÁå·°]=Ð³quef¸I¨6BäÓÆçù+RåkÇwäS[\x0010a^Uä¼ê³þ×õ?ÿëv}uðÃí?ÿs¼¤;\x00014ªI1\x0008"tã(³<\x0017[\x0000\x001d½8:]\x001cüpz4ZW éUÓ«=\x0010\x0014à¯Çb\x000cN¥÷^m§æ:!Ê\x0012¢\x0000Q¨<ß\x001bÊ]±ìn\x0013\x000fÛEË\x0010U	QMÙE\x0006éé\x0012²ÈI\x0010vÑä\x0019ÁrËRê¨Kz\x0002D\x0019àa\x0017Ñ\x001fà¨ÖËÙ\x0007mJf\x0002DæÉ²*.EüßëíLD'D[B´SvQ\x0013g[\x001cX´ô>?m/¯\x0013¡+\x0011ºoRæø\x0012¢xÎ4ÜÝÓk	ç7q» ©\x000fbã93×·È\x000f¬ =ß\x000cýÛ\x0019Nµr ]`\x001b-%~s\x0015
÷¹=Al[6\x0018+ÑÍ§ÈnÆ³`är3ÆeBm#§\x0013c%\x0018ù\x0014ÉHÙs¦I¹G}7=÷ +Ã'\x0008\x001d\x0018ÏYd$\x0018n¢¥jx¿ÀîX½h>áIó`¿:
Á'
©3Q Û1¥ ×Ò©]a^´¦ô©jO5à`ð «IpU6µ-[>^+R54\x001b\x0015/çG£öùúêâóÅ8F\x000bMâ8+\x0014>kÇÊÝÎ\x0001Ñ´}¾:9zÕ\x0004S0Å\x0014\x0006å8M|Ï'\x000eÑ\x0005@Ê\x0012¤\x0002ÒÃ\x0004ÉÑgÂEÏ\x0019Mc»G^vÂT%L5\x0005¦±4Ä:F\x001dK\x0008\x0002½Û=@´\x0013¦.aê	0\x001d÷Ù²NÒ\x000cI/³\x0011éwRÁöÂ4%L3éÐ\x0019'[¨&ÁSg?	¯|ËiKö½®é¦ÀX\x0018VP	jôç
ª\x000cÕ½0}	Ó«»Y2Tój\x0012|\x0007Nr¸Í\x0013IWSe{÷ÐØNµ\x000e¤þ%»Y)!>E\x000bH\x0012db:"0	2Éï\x000e\x000fL\x0004Z)">E\x0013¹ ¨0\x0012xÞã3ÒlC~÷ÈÌúN *âSt\x000b­ 
Î<ØÐk£\x0019l+Z)#>E\x001býk®h¥ø\x0014uä´É±\x0017å(åá\x001dMVòf
­Ô\x0011ÿfõ\x0011¯ô\x0011¢\ä.Hû©±V3.r hç@^Bâ\x00134\x00129GÔ©\x001fì¥Ä¥\x0005S¹l'­n'PQ©$1E%ùàf8
ÉTÓ®Ù&h¤ø\x0002\x001a^Ô\x001eÇ\x0014a\x001f\x000ca¸É\x00156©ÙYóM­2W\x000bPQP1AçyöUhçÙ\x001fÖ»ø©{V¢IL\x0010Mÿ* Õ\x0017\x0013<\x0007Þg"oÕôæ!÷@¥Z\x0000¨¬ðàgÐFòfTL¦%ßÌªÛÉùÝ\x000b´zKò}K²zKrÊ[RLRÁ\x0000JÝÕ:7W79\x001f$K#F[\x001fºrê\x000cÜa¬Aµ\x0013Ë\x0015ùv'\x001f}¯4ÏÆ1eÚ	¨ H\x0001&I=1Ö§k\x0011m\x0005\x000c¼×\x0003\x0013o=A@qûDc >Q6ÝR'©xÕø\x00054húf\x0000õÍ·jà\x000b6¼\x0004M»\x0005Îû
^¡¦3w²-\x0011ÌñC¸~âýÄJÄÖæN}a2·,:K-a
:G v
Piëó«,BÍ¯>^^]~þ\x000cS\x001b/o/F¬#Õ8ÎDi?\x0008ÔÑp<;h<¥AÛ?\x001e\x001c¿z\x0005\x0003\x001cOÆz­ÝpµE´¹\x0007)°ýkD*©ë)R\x0001!ÒC~ºÊ\x0012©º§´¥î	³´¥2oé.Õ
T@Õ4 zK"Ã \x0002¥¾$»{c7P]\x0002ÕÓÎ>eUNQ\x0008Ò:îtPº\x0012©zK1xRßR³ì-µ%R;
iæI\x0005ftì\x000b±ÎÓ´Ö ^g!ez £à"d\x0006§ëÛÛ?Æðÿ¡ ¾Q\x0016+\x001e¥¹`Üì(ï:?xº:=ý÷ý¨DJ´¢\x0012Áh6%"Ãi)Ül(Ég %*ÙÊÓÜ]\x0013[1#&A2Üíà2hÇ¤JLª\x0003Í£8Yàdì
««ÝÉóÓJ¨tÏùÙ|«Kiq¯8M3t;¨;A\x0012é\x0000e6ý>*µelbI ´Ê¨l\x000f*;\x000fÃ@¨\f»\x0017Û\x0007í¨\Êu 
^¢½ÒXj c³\x0006îÕtL¾Ää{Íq>íÐE
¢*cÚA9Ýª¾¡K\x000e·­ÊCÁB­\x0019d\x0001ÅIÚæUnUËõfÁþµw«\x0012ì¼G²ë
\x0015\x0012£²´p±2ó¼0»\x0018ï\x001aaUR÷Qùç.ÍK<ÄÌ-·=Á \x001dU%°xÄ6³â3CÊ9X9\x001b¶´]L|°*ÙÀ»Ã×Û,¦ªú¨\x000csM}£>Ô¸e*s¦yFe\No·)·ãCp¼\x000fÜ×|CZa]Ônµâ5c¥£ÌóÛÛ®®nÀ&Þ¤)«µ\x001e\x000eNÖ×\x001f\x001e.ÞÝ¼\x001d³REðð°eÈYö\x0012N;KØc\x0003¾ÕgçGß¿<ÜQ\x0018E7F¥3½¶ètOA´Qîôta%FÙ¿@\x000c\x0018­ þ&á]\x00160î\x001eÙQ\x0018u7F	jÁfX¸,9Û`Ü\x0019ìÂhJ¦\x001b#Ph\x0014%ñÁ´¼:ñ.}\x001fD[B´ýÛ(8
3m$®3±;å]\x0018}Ñ÷c\x000eù¡\x001e"ô\¼\x0016<ýG\x0002ë¬BøÙiwqöáÕ£æý¯Z\x0005µÝ\x0008. ÒØ\x0016¯\x0004½\x0018%v\x0016âu¬^5ïÖ@ÇA:\x0012Yºjç8ö>Õ}äý\x0017\x0012\x0006£à³\x000e¾>ÛZ.\x0010#·f¶\x0011Õ\x0014ý7\x0012b\x000f8ÏÎZÄ¡\x0017êÝîªË.Õ\x0014ý7Ò\x0000e_zÙY*\x0017Î´;Ãs}\x0018«\x000b)ú/$X`>Å\x0010=wTMo\x0015#ÏÖ3¢\x0012â¢_ÃÄTÚH\x0018Ú0\x001a6E¸ó\x000f»z4bÂ£ñçÊ+_
Ù\x0014ówQVOFö?X²ÂQÞ\x0004Óc­¿ mÔzö»µiÖÿf¬äd?z\x0014cCÈgmf\x001euEü\x000c¦\x0019ü½+=\x0015^x²\x001ctÚÚÌ7}jOFA~°U-nF¥8Å¨ëVéÔ\x0016\x0005\x0006ùî¬v#T6tlX\x0011w?¹ø²wYò<\x0013\x0004F\x0002Z¤þ\x0017&û[ÛÍ<\x0000íè§=¬Ëlè(°"ÆÝKl\x0012\x0002j\x0002.âÙpvç¤V\ªÄ¥zp\x0001ÿ\x0007ÍSËî\x0015Ø\x0015äØo3°vàÒ%.Ýµ_2ógk¹¢Âr\x0000~\x0006*S¢2]»Åè\x0016º3Jíu·â²%.Ûµ[6ïÊ,.\x0010G¢tÓNþÿV\®Äå:p	or\x0014ç\x0017Âç°4söË¸|×~i"ý0çñ×@Ûmèv\EÐ\x001b¤\x0017ëº`&sñ
0N\x00043NîÌ\x001b¶\x0002«Åj\\x0005>\x001e±IE4)\x001bBm6
¬G
Ø\x0010¨0.Yo¨NÅ0FdArPÜOìiÔºY¬ç}Â^f%\x0004ÝÍ\x0018kÄ´sUÂwI{®[\x0016¦ªdíXLU!Wy%íy¸âÈ$(t0v\x0019²\x0018²\#aÍ\x000c5Ä+Ï»$¾Ìz[\x001bM¥[zéíî1\x000e­¸*ÁÊ{$k9ÍåTToq¢z¢ëMzOrBË\Kª²ýew0w\x0000«6LômX#k©q¥òtÃÜ6\x0015mÏ¬R\x0018é]\x00169\x0016aòÓÜx\x0000 mé¦ms\x001eö\x0018®µí\x000fÆkÅh'¨Ç×\x0018Fn\x0014T$ì¬£Éõ\x0010î\x0017\Q§2/½\x0014ô\x001eÙ9ñ«ù\x000eáq×ïë¨*?Ì\x0003yS\x000eyqsywqy1>Û'Ò
$pLp\x000ctÊ\x0018'àÄ.!wô\x001a¨^\x001f\x001d\x001fÍ9ñÃ,7\x001bb»v\x001cd#Â°*;ÈJ\x0012Bgv\x000eaéA(K²\x001b¡Vx\x000c\x0008aè\x0015%o7õÓBoS×ô"T%B5åSÈ=lzb-2¾\x0010±cLm/@S\x00024Ý\x0000\x0015FaDWjã\x0002r\x000eÚ@µ{þO\x000f>WâsÝø\x0018W\x0004¨\x001d\x000eÖ\x000eO;#ÜÅýØ\x0005°\x0008´{¹L¾©\ôëÁCfßÒ&ºaÍ¦Ó\x0015ÉÝÁÙåõè°'îbÖ1n æDÒÊ-5¸\x0007?{wåûë³ã\x0017
ØdMöa\x000bv1ú¬,ü\x0011¡	
Ô\x0004]·»ï¥\x0015*¡©>hÁæ(­§ÜI¦©´á!²GÜC7¬tº¢ýhÙ±<¬\x0011vÌ ±\x000fl\x0014nÙn"Ö\x001d3%4Ó\x0007
bZ\x0008Íi
\x001b&õèQo-QÙ\x000eTP_êÉâV#¿ôYÅ!$svÌØ\çÓÔÔðÃ\x000cÁ
£-)ww'5í/Qù>T<Wä²`\x0016£{\x0018þ=\x0019×#d-;VDG®9&ö\x0013<óc2 Ç²\x0014&Ðèjg/G;¸êmòÇù5ï\x001a\x001f2Yñm&«ÃõÃÝÝúÝ8\x0005µ±É´2WÌ@²\x001aË\x001foÚ:\¿~½ú~tæëÉo3Y5ÁÜè,\x00189\x0005£3­£àó\x0005µã%Î!H\x0013N
Ç`WQ­î\x0011ýÕ\x0007S0\x001d»-0
×yä28QÌ¸<\x0001Nï®é©KCú¶S\x0017TÎe\x0015£1F¹
ÏÉ\x00128MsØ£ß´BP<ÈêÌºe|îÓÜ]úÑ	Ó0ä!­ÛIsá·½-ñ\sÈ$Ð´åùrP\x0014íyÜçc÷K\x001c»/q\x000eÉCp\x0002}+ÊN\x0013?&\x000f¤öF?ÞNÜ³\x0010¿ÏªmC-ÂiÉË×sB¢\x001dg­¦(#\x0018ë-©G?ó\x0019+Å²%6´ÒF[VM@a.\x0002¼eXüÇkÙÝu}(+]´ÅgÕ&å=±Â\x0019\x000f$2Çµwæ·ã¬¤ü\x0016KT«6"*_\x001f\x0007É&udÿ?uï¶\x001c×¬ë¾J½ÀTà|\x0008]¨L\x0007OÍbvßt¤²L"%t·|µ^cÝ­ØWËûf?ßd=ÉF\x0002(Q£F
 8§¹"¦dS³Ýþ\x001a\x0003Hd&2ÿ¤b\x000b&bA»!éÓo´Oâ5\x0006KOmø;j ]\x000fS´ê	ÖÙ>®m¤
V\p×ëôS\x0018)¶±¸k«Óó¤sD\x00111, ë½L¿Q=·ÙäÔóÕ¿·\x001fïÃßÝ~[Þ|¼\x001esì\x001d´Û¡äñhúa\x001cT³9d~´øÏùÉëóðw'\x0017ó£×»1E)Z0S,b\x0006Ç$5º
\x001f:zÚo¾ 5pÊS6qæ$\x000c7~j³ö¨\x001e\x00181Ù©JLÕ©òHr¹î\x0002
>
ZT=ÐÚÀ©KNÝÂir\x0005\x000fL-7)O\x001f\x0015:PÚn¦Á\x001b8MÉi8\x001d=\x0018ÅÁ\x0014\x001e[»æÜ|Ðªáäý#n:»»Ç±4®\x000c\x001eb\x0008Ù±çq_l=ÃN\x000eLÍ¹\x001d^fpyÿ)¢Ên7Óy8###$ïØ±/©tI¥+¨l¹n¸¤4\x000c<Yæ=ÖÊT¶CJ#Qyz1!\x0011¹4kµò%¯¡Òy­ gf¶.ßÔãª'Sñîn¯Ùîðj\x001bK9ò¾Ãa~^Þª³ÛyÍv×*×JO%\x0003l-+§ÕP­ÅD¬Îvç5û]\x000f\x0008Þ ÄVÑ¬yæì`ûDªÎvç5û[¨ZK\x0005¥*7jM\x0005¸Æ
5ýNÂRª³Xðc\x0005\x0017§\x0001í\x0006æár©¬4\x0001J«íËÕõ=ã\x0015\x000b\x0013è$EsP¶¬hÕX.û\x0018x5@×©ãº;ïà.ü#÷ãþ0r!&x\x001ft(=¹\x001cÎ\x000cÔT$oøôäàô|Üwï¿×qÝ\x001dz7PPÙB¸ÒQ¢Ñ´à2m\x00196O|º/ê­$<'\x0006º\\x0005«6SM\x0006d}/&ËOüþÇÿß~\x001a\x001fÆÎ©\x0004hwÂY;äj<\x001f¸¢\x0002_pÞHc}Y/&ËaØt¶h\x0005Ãwl\x0015þóy¸Û,'«`%¬g³ë¹0k6ÊaóâÀ
6U²©ÚojÉE³ÜP¥:¨/Ðº
T\x0012W°éMW²©õ\x000b\x0005£ãÊyÄÝàpÏ©h¦D3µËf b
\x0013Ör\x0003Å\x0015h¶D³µ«Æ¨O
Ð$¾Ì2OÂ\x0017RÁæK6_É\x0006§Ä[¡9Ëù(±9&¹w­[­yøs=¦\x000b[\\x0018Ì\x001bÅ\x000e\x001f¨x\x000e×1!¼Ö<\x0013ÜBg,=l¯Åíµr¬;´8Úræ_jJt?6Ö16>»Y~XÍ.×·\x000f³wá\x001fZíjåÈÂ\x001f KN\x001d_\x001cN/»½BgGóÅìb~xr9{wxr°\x0018-üÔýHYÇH¹\x0011TÄòGFÝ
ÉuN)
¾7¢.\x0011u5¢ðÒ3ªt\x0017gó²?¢-\x0011m\x0003"{ádßÊ?]#Ú½\x0019}Éèë\x0019mÎÏYÆ©PEXgÅuëS[\x0018y÷ÄÔ\x001fÿä#ÃëÏ\x0007#\È°¦8ÑÕÓìy÷é¨±sfxÃ¡1fí\x0001"RÌ¥+ð`¼/dçÔðc\x0003.´Ï'\x001b3PBçÞåÜ\x0004Ù96¼áÜ@®ÀfH¼¤KÃ3äÞçFtÎh87Jå«&|n2,åÚsÕ{CvÎh870ÇæhÎc/¨ÈC÷º\x0002ãu¦\x001fm\x001cm¾»þð\x0000z²»"&j»t2i\¸<Ib³¿àÝáÁ%¨Èî¦\x0012%¨ D\;ýàpyxôg=JT²JÑ@µ¨ÀA9Ï±Pd:.¡t
\x0014Ïmì>\x000f\x0005àÌ¬Õì±T¶¤²\x0015TRQh\x0004ÃOq^'óôÆèÙfÓÔt*_Rù\x001a*Ç5²¬kÄü:ÎÝp'CñÎ®â5ÛJp\x001a\x0014\x000bT¨èÌ²ûÐìçéX}Åk6\x0016·$Þ
¹\x0014Ôûb9îÞT\x0016\x000eÕÙV¼f_qEmõp))\++óZµo+ÞÙV¼f_Á¬b¦s²\x000cP¹ã±´Ó\x0014¬¾")\x0015A.¯oÃ¿ôn/0
·Ð\x0013¤gïz×\x000e&°/\x000fOÂ\x000f;¡D	%* ÈPúÂ«PSäïÜP3àD&Y2ÉºÂ\x0012H£5\x0014mâJÑ\x001d8Ð5\x0019JPª\x0006*X\x0005´ëç^m¼\x001aêÚHeJ*SAÅI\x001a\Ò#3ô Ò:Ù¡÷­H®Dr5H
jXH/Eâ\x0005è
m)3(í¾J÷ké5§Ã\x001c¿×w¯o¯¿>W.	IÕ\x00020\x0015ô¬^ÏÙØZÉñ{}z|xrø·«ÑlM¿^s:5P\x0000ªF\x001c\x0007J)£,©òMÁjDY"Êg¹ªDTÏ\x0012Qº\x001e1\x0004t¤y\x001b@ãætþÄf]M%¢\x0015U\x001f«!y¼\x0015RÙ§ N;ôÏ®Ó)eÔåó\x0017\x000c	º¾¿Þq×[RK´ô Ã]¯ò\x0014K?Ðiæ\x0003\x001d\x001fN %¬¤\x000bW\x0005No°:qjô\x0003Zè%Û6½~¤Ôåë×$0Íò²9I\x0011]ð1Éõ\x001ezì¯Z6]ÒéZ:I¥\x0008\x0016Âð%'\x0004y½í=x*)éL%ë¹èòéÌS«w\x0003JeUt¶¤³tÐ.¹ÊÂM<\x0019\x001f~qÎæJ6WÉ&l\x000e\x0017ÂÊ¥ÚLÈ#è¼ëöó%¯µ$\x001ezÁhá(À2¹Én à«\x0006®\x0014ã*&PL^:
1èìÐÒÙ|£
É:Ôàu¬0¯5ÃB
,ÕÛS¹\®àðf@U°
¯cíx­¹\x0003±l´ÃFQ÷\x0002sùíÆØ=W¯cPx­EaëÎIÇp`Øz9iä¶\x0015\x0010MÅëZ^{lC<M«g-2gÙÞÙ(q\x001aí;\x00006:\x0000\x0007?¯o\x0012»wOo®\x001brá\x001fbÐá\x0011\x0015\x0004Ã\x0019IÊi´´º;FãàEðMb\x0007ïéÑá»\x001db\x000e¶ï\x0006Øè\x0006Ô2r-¥L¬ÅÌLV÷¡Pª0\x0018=3×<'_Åaä\x00013×ºU'MºdÔõP¼v¢ëe¤^d¬Þ\x001dMÉh\x001av£ \x0007NeqÖªcÖÒ2v\x0013uM¶$´Mè*Á)Ã\x0019\x0010ÑX\x001b£÷?/®dtõ.g\x0016áÀ JZÌéÓñ{3úÑ7íF|Ü\x000cî\x001f¦ánDÃhzµ¶ñ\x0008w~¡¨µxx\x000cÙ\x0007Ç,I\x0019Æü\x0010\x000e®ò2+×\x000eùø\x0017³ÅåUøËn2QçD¦J2õÈtI¦\x0005è@R¬èíÜþùÇýòfv±¼¿_^æþ\x0002\x001cö0p\x000fcPiYÖ$\x001eòvq²8\x001fÍ.æççóÃ±\x001c è{\x000bB\x0017B\x0015u¤MIM'Y\x0003"\Ò´r°}½U¬²\x0015ÆJûür ¨3\x0012ÏáÕ¤ª$Um¤0\x000b[Ë¼G\x0019ÎîyÖ¡\x001bjº­FÕ%ªn\T\x0018E)\x0006³o!²ÊZ%l¨¹\x001aÕ¨¦
ÕsMïÜ^k\x0011\x0017Uç \x000fJ\x000eU£Ú\x0012Õ6®*ÌÁ¦\x001a9õëJÈ'9V¾dõ¬>wÞ5ª§W&/\x0007e`jQy×®6\x001aV\x001e¨ø)*YqëªðO\x0001Û1W¼Ñ^A\x001b\x0002Ö°@}
®¬[:!¥jÖ\x0015àfÀ2[.ýÂ¸Q®ËZâdñÎÉâG+\x0004Ùp£RYG¸xiíÚ9Y¼ñhYo©7øÅ8\x001d(Ø©l\x0005\x0006Å\x0017jY\x000b\x0005Hp\x0004Xã¥\x0015\x0014¡¦Û5\x0017ÿ\x0003@÷ëS v¬h´\x0002 \x0014@S³a@\x001dÆDj]]7(\x0013Q
Û±\x0002¢Ñ
0(?}ÀlÓd²¼Î\x0016½É\x0006­°\x001d3 \x001aÍÓf­hÁ)\x0001çÝºD~pêM5lÇ\x0012FKà¬§\x0019\x001b0øH'g«\x0015þø)X;@4Z\x0002g\x000c%3$¿äÃñ¢Â³AYÂú ÓÅ!tWÚä\x0019\x001a\x0004¹\x0001,Û¡êVf{\x0002\x0004oÙpKV5±\x0012½\x0000Q	JD,\x001f®ïn;Úc<_¿
Hð\x000fã1YËn¼IÌ/\x000fOOæ£Ý1È%J.QÁ%B\x0008­lNx\x0010FÓxJa7Jz*¸dÉ%k¸¦f]\x0007\x0005¨©2É'í
.Ur©\x001a.H¾âz1\x0012ÊTb]±\x0000³Ú¹tÉ¥köÕ¹£\x0004ÆÚcûÊ\x0001ÒfÉt\x0005)±LÍre!vé¸}Á¨`_ÑÔN¾Ùu]ÁåJ.WÃÅ\x0015é\x000fÀö¢\x0004¯×Ûkã9g:WñÊ	fUqêgñTøÄs«°ß¬ú« ê\x0018	^c%¸³Ùz9EI^n8YW·Ùû]\x0001Ö9¼æ8r'r'.hpâC¿6ù1}³"±buG¡GOcD&Z}\x0006%éÑPæFa[ú\x0006\x0006éÔlÿÎý\x0019\x0000µmNÄt:­Ëº<'+½s{\x0018Ù]ÚsU|\x0002Ê½_Ü\x001e>¹Bõ$\x001dÍ²¦CºÇ*ñ t\x001fm¡á:¯mHmãýæ\x000b.K#zßÝ\x000bJ@Ï«Ä»
TÀh u5Äùfv~z2®zÑïÇà²Ô<\x000e*¼¦\x0011Ù2tÂçKBAåZP_ú&Ðµ\x001di¤ánq\Ò¡ZñZÒR\x001a©èd¯D\x0015Tÿ\x000fó²©U.O¬ej³3¨\x0005UvPe\x0013*¤ÉqØ³ÀBw­r	èàÐjÎÎqâMçI	GNÏ0¹,Yé¡îé¨ÆõyøW\x0014¤!
º»\x001d=ñÚÃçHè\x0015)©B;9\x0012ºaÁ®\x001fBüsz²Ld²Ls×.Ü:X\x001b¥µ{\x001a0U©\x001a0%%iºÂ\x001b\x0003\x001a\x001fe\x0004î?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ad~
+t¬ ª§h1³j\x001aøUÊ+\x0018v|w]µ6îq-SØ\x001cÂÓ\x0013ª`©ßÎæ\x0000\x001dv¸1z\x001e6ô°A\x0006«\x0015MDÎ°<#ÃÆØ`O\x0011­ét\x0016¿Êh-½¡\x0016ÚD',Y\x001dÚ­iVß³z!k¸"Áâ$}ÒÙ\x0014ø¹q\x000c>\x000bk{µBÕÜ9MjÔ®i\x00175\x0018¿>ÌÒ.\x000fÿ¶<ü\x000bhÑ\x0011mÝ´´7ð$\x0005ãÀë.íð ¢ºþ|9áùæ½¢S4ÏÝ\x0006\x001b\x00185af×7G
BÍì\x0013rhÛ`ið_Öñ³Î,mê\m½5
hyà1¶µS]Ía\x0017\x001f°0nöu=¬Áb\x0015'=H\x001cÅ\x0004Oë?ÒøÆ8ÉjVí1ø\x0008Uô\x0002Vìi7$Yoê¥ÑÙ¨4ël\x001c\x000fe¥ÕO0Zæ\x0013L^À6Úº²\x000f\x000b\x0017m£=C\x000fíek²Õ9\x001cq\x001c«[\»T\x001a\x000f¥í
­\x0011\x001aZc\x001cÍêqË@f\x001by`S¦\x001d\x000ed¦u\x0013Ã¯2Z{¥É|E âëLKÍ;I«sôÖ÷à\x0000ãdèIÚæ«\x0017/]¶\\x001c}L\x001b1m¨SUY´º(\x00028.UÁå\x0003g\x0004µ±7	Qh\x0012p¨j\x00042	¦<÷ÐÔv¸q}Öõ´2××/K®!_ÊjO\x00068\x0017I\x0018ÚMÓV\x0016ÐD\x0008Í\x0019Oã»ÀkË1\x001b\x0017]NÒ¦ÐÅ\x0008øUª	5ÿéµT¨5°Ó¹2³´±3	øUB\x0003,6æBWÊWÚ\x0016~xBøÕ½aDS_È\x0004´Ö±ãõ	hã\x0004\x0004\x0017Óp'ü4mA(ß\x0005´ Ê3SÅ=:ÕE\x0015\x0018ÖÄ\x0013îÚ¨^¶FdiS­T~\x000bë\x0018c\x001c\x0017¯ÍÒê;´Z¨	¾l*´mJ\x001e\x0004Oë\x000e#\x000eÏ<\x0005\x0017îàÊÒI8ù·¦é°\x001b.VUÀ\x0006jR\x00055~l¸=æ¿wPe\x0001XÊF«ö\x0012¹|»¥&Î|Æ(\x0000Ë¾x\4>+Ù;&Á\x0008MBÄ\x0006NO¸¼\x00060ãL¸n_P³)ZsG\x000bL\x000bÊ¼ª\x0006\x000eÌÒ²A\x0017\x0016Ì¡ÞÉ$ÉRI l¢¾§\x001c\x0015pW!ÊjÎH|icïh\x001a/E\x001d\x0019Wåd[\x001bÙ\x001cØ3®¶ªW\x0004ü.S\x0004E
:\x000eò\x0019\x000b\x0014\x001a¥óÅç\x000cZHwR_Id\x0011põ1­Ëv¸à'.x\x001a\x000f\x0012qjÈ	¸î#sRGoµ*Åe7ÑT4E¬c:ÖÜ¡52UF\x001e¹²N«º\x0010inô§\x0004·ÚÝÑ\'Õ\|Ç­æÖbÙÒA£sVòÃ´v5â\x0011imñ8Mëli¨7\x001a´å&CÈ¢à\x0006¬Ò>\x000búÎ^@Àø\x0006mÍÃ_n}ý¶àÞüúÛí\x001d²µ*P1k¾Yj×ÊþU!áùÃ}ôôñ³{ýôG/ï¥õ¦£Å\x0001\x0012ZÝ<D0¡ÉQ÷@LÃëù4lèa\x000cÖà\x0000M°@«90Q×`ÓÈ(ÌÒe\x001e\x0013ÒâWhóu¡6ÃXC°Ú ^o\x000eÃüâ4­îÔ¶\x0004\x0012ÚVfY\x001aOk¢&Û5`Úñö©iÚ%`,´\x0018/
\x000f\x0019_s¥Æ\x0001<diO\x0011­éEk¤¢\x000cõÐgÉ&¾a9ó4¬ï%ëeÅ¡®dÛÊ\x0006lº@3\x000cY.ç\x0015\x0016dM3`®
\x0003ÇB\x001cßÚaíê'´ãXP>ùò\x0002Ô|ð¯È\x0018¨\x0007m{+ãÒi¹.ù¤
°@°®Õ£@yx¦Ëãp¶Ã,¬í\x001d®:ÜÌ¤øª«i4Z.=§\x0004÷ÑBw¾ð«Ö\x0007NÕå°)f;\x001bÒ°1gÖõ´NHCo Ù\x0002¯=ÊÀ"Î¥9\x0016zZ¡9p
3^ÖµrZöK
ãÚ)s`ÎÂêf6Pçs=Ú¤©.xÎ\x0011ó=­Ñâ\x0018r·8¨Þ \x001dÉ5Ëw8Ýa\x0016Ö-e\x0008_eÆËq1\x0002nY5\x0014wyjÌ\x001d'ÚO«\x0015ÞhVó}Ë
ôÕªÿüáÍÍ¯·o÷mxÔ§+\x0015U´ô*9Ç\x001bXÛh÷ß\x001e>¹~úèÙÆ*¦µkZ+¤Å1ð4\x0005\x000cá´àQ'Þ\x001d¥Æó´°¦\x0005)­§y	ù\x0006\x0019q[D¡5À´cª&`Ý\x001aÖ	aó]G©\x00101
°1±"dG¼9(p?­_Óz!­súÊ\x0010jß\x0005*\x0002ïñê,µ
kÚ ¤5v¡U4\x00025ÇÝm8gÚ?0E\x001b×´QF«\x00137\x0007dMhÛB"¦çvW§MkÚ$¥uôÀi\x0015Ï«Ö5ÙnIÞM«{s+´·\x001aWóV\x001e\x0003Ð[nN\x0005ÜOk:Z#£U>Ñ ¢:¢µnòüÖàÝxC­\x0000·ó\x000eZè\x001e´\x000b¼SNá~sZëµpýYºÐ¹\x0007-ô\x000f8È²Î|1¸®¶úÈË,Üö\x0018¨	ÜÎAh¡Ðcñ,]C5Ì%yPiÝIfAw&W\x000bm®j]Æ\x0016G\x0011°.¨fÅÀnÎdÝÛÙ\-4º\x0018ÎP/NÊîwrSÛ\x0003Y÷Óv6W\x000b®Âk\x0019\x000fÓ\x000f¼U9h^,\x0006is\x0012Ô~\Ó\x0019]#5º¸'¾Òæ\x001bZ ýÄ\x0007ÓCÜh\x001b¢í¬Z1Ýf¾$àûC>gª­¯Ø½\x001f·3\x000bFl\x0016\x0012½ë\x0019Ü\x0017hÑ¯kkâÃI>Ât£\x0011F¸H\x0019x9¦ü"¶Â1íæ\x0008Æ	ÚÎ\x0019¡\x0015Ó6²æfXÚ\x001b¸\x001e\x0010iOÒÜÎ,\x0018i,#\x001a<\x0010d\x001b(ÉÃOÏÊ÷þrTR\àns,	£ûY\x0008ÍùÍ¡\x0013¸\x0015³R+æ\x0012\x000f\x0006Ãå±!µE<~£9~
·\x001d­0vÔ®­ÓN9\ð@Áãvyéà$nYZ],¦`Ýµ¸ñ¨\x0006æmýöpÃ	Ü.v´ÂØ\x0011ï\x0011¤º:ÐûS¦mëlÜp½¶ó\x0011Vê#\x0002¿I\x001b\È4Ýh··ï§í\º\x0008Ü¢N´X\x0011\x0004t¥ä¥ß`7g¡Oàv>ÂJ}\x0004vð\x0017Ú²þÝ\x0010mâpÁ\\Ø6IÛù\x0008+¾¯F\x001bØEDË°ö\x001cMÐpç&MáiÇ\x000b3ULW¤	~I3t\x0008ùþõ\x001fw®=ø'²«DÀ®Íz­ÔÍð*µl5:éÒ®?¡ÖbjÚÿ]$¯ñ³N\x0016\x0007³FÞáüâµ={ú?ÿß\x000f¯oßï`Åú$\x0004,S\x001e¬¯¹R\x001cSÃy\x0006]./Ò>}ôòñ£\x0017+ÖQ÷Z\x0008[ð\x0018\x00127¿ÔÙ?wh5®rßÉ¸t9\x0014Æ D`b\x001b\x0001±\x000eÂö
k\x0001	Òì\x0012d}/»C\x0018{Â($ÌQ\x000cmæHc\x0017WÓ´²\x0001\x0018Ö#ì!´ËsSÑEÐ"B\x001b÷ÄeÇT\x000fN¡æýZ¥¥NðCk\x0008w\x0012àùÖ±rQ_¿ý·Û\x001d.K\x0008;B|ÙÖèúí\x0013îÄ)ïajûÑæë\x0017¿{´e3®9£3ß°<mp.²¡¼\\x0011çÆàÝÝ«42ÎqÑ"\x0006:5Y òÎ\x0002¥N!¥Í\x001b÷^PÓ\x001aD\x0015\x0015P¯ÛÀðÔ\x0016èMÕÜ	ºÊº`ù \x0015IÔUÊ\x001cUÓ
°¬hÙ¼§ììÔÓôÓ&z)d4KÜ·Kf'¨í~v+úÙ3(ÐÏ\x001euÛ%¸\x00025ßØ¶¼½ ®\x0003u¢Ý^ñ¾\x001bKUÈùç"¾l¡OPOèÔ\x0013dêi¨ã\x0003p\x0006¿¥}\x00114\x0001;ÆOøá¡ÓPihÄ\0sÆÄ\x001aÊÁýNN×)¨)hYcáKFJ-
JO\x0019Q]èö\x0004í\x0014ÔÉ\x0014ô¥÷zjÊªB(ãcªB[\x0019´1Il?g§¡^¦¡®ÞÈËj£døÄ»ëã'8C§¡A¦¡@&!Ô8¾êe\x0007Ó	\x001a\x001aº\x001f>È~x\x001a\x00069#U¼å\x001fÞ°O
güð\x0011Ö\x0011D\x000254
5&*oÁ1A¼k{©ä>P­º#_\x0005¤Zñ\x0002\x001b\x001c^@¶É+Þ\x0004ra\x0016Ä\x001cèR\x0005_;%\x0012©§«Q\x0006
T:)2éñ^¯\x001e&
h\x0012*^Á\x0017B`FÇz3A¶\x0013\x0014zL¢2üÂUoJq<þaÔu§\x001e¿ÊB<G{×°´­yzrõÚ\x001e´ïEêE"\x0005ßDuM.uÝ|ûÝ­¥]&4u
²üw)Þ\x0008\x0015\x0013++n<óZ[\x001b.S·ò\x001f|\x0011Vyòoo>¾ÙÃéqøª5m)9ê.ÖºêJ\x0003lªê·×¯ÜÏ¹^»gc¿vo?¨5¼l
kèÁ\x0017'\x0011¨Ýæ¿Ôö¤VDê"½GfRKíÇ\x00114t³8l/©ëI\x0014\x000cnÉ(¤Øè_E\x001aéP\x0005p\x0017§½ ¡\x0007
\x0012P¯)«\ú\x001dH©$[ñô9R×ÿøNôããÚ'\x0012iúIMÁÐª\x001cJ§­¿´©\x0013É\x00147\x0013)8Z)jÊ¿þxLè$hêAèÇ7\x0014ìã\x001cº%%Öl¡¼:A¢©ÿíè·ódù¦D-»1ßê4n^÷\x001aÕ\x001a%#\x0005ª\x0001\x0004¬
5\x0004\x001a\x001bhØºî\x0004]ª+\x000bèº¼r\x0002·¨j³©2i`[º½á|'éRRH×(\x001bi/S+iJ4-\x0007´æx\x0004öãAê{RQp\x0002oªÄ¡ÆjO;!8Álë\x001a\x0014d w«j|jfPj Í Çc\x0013ã{P/\x0002ÅIÖÕDaÁ'-5ôä\x0019\x001cèã.ßøÐÜS>Oµî(ÿöë!òy\x0002\x0016éqÎØû(:÷94¡©\x0012:S£=Ê\x0006JpÔ.MbH_%\x0011tÛMªñÎÏ\x00114µ¯äß~c\x0003ÒnÒ¥\x0005 ®{\x0000öxE?½m=LÖ/JzB\x000ceµïAEÇ	\x000bøèÜã\x000b³&F6P~³°s/iìI£4RO{ËV÷°òtv\x0018Ôt¡	~ÜI\x0014?i{\x0002t)1,Òí"³½¤Ðüh6 6.?¾c5gþøÐÝóð«\x0014\x000bçÙF\x0001Ï,¤à\x0016ðëCèIEV_µ¬©Î\x0012úñ­e\x0013å6\x001fqwºþä;YÞëÏ\x0001\x000bzM"RÃîÉÇã±uýÉw¢¯x\x0012\x0007à\x0010pÅ\x0019\x001eàØ$pw¶¾?ú^tôUËâ$xª¶ïÎîõýÑ÷£\x001f¡ ÙÑ7¦an&¢÷bö§I\x0014C­1ói¢bèL\x001aÚq:\x001eZzRÉ\x001d\x001f7ë4ÒHÃ\x0010£å©¾tc\x0001ÛnÒÔGQI\x0012E:«±*)ï­É\x0001K»=m·ï%í4\x0014§Ñ³ÏO´<\x0002Ë4\x0011ï¥Þ&1
¾¬ü¨&*Ò\x0014L\x001a4aöS¢èD9þé-_I\x000c7\x001då~³p\x001fæj\x001db®\x0016ÙM	ÔÓ,â\$&Û¼Óñ 
úL\x00142QùdSy+`ë\x0006{&xÓ¼Ó\x0011?ª´ëË¶°Ö,ó\x0003o\x001f|yûæÁõë÷÷£Z½g¨\x0013ù\x000cxq\x0007W'Dw¡B¿Î\x000f|ôàËGO\x001e\?~q\x001f¬^M¾ÄßÕàË)ÚºµÛéÈRËm¨\x0011ÂÖüùôÂlÙ©{L-ÄLâ(ûTj#\x0001(\x001e\QõÆÄÞýB] *­Ñº6æ\x0010Û;i²l)\x0015©´z¥]gÖz\x0011mv¥¼­
¯RfDq½\x0019Ø­©½»a×³ñp\x0019"@>Rõ9ÂaC½«°:ßV+­
[kT&h{S ´\x0005\x0000æª/å\x0015y\x000cË¦\x0000\x000báÏµ½h­T´^Ï\x001c\x000e«¨k@+6\x0007ÖB»Ã´e\x000e\x0016çbWß\x0012w Ã¥â.{¡~6t\x0016Á\x0006EpXæSa­¾ª3¢tâIÓÙOlÝÏ:{P,=(]ó\x0008-fæñ\x0005*CFûz'i¡w` t`\x0019û
b¾\x0012ð;ÏSZóeö\x000c=Þ|Ð|9\x000b¬µ\x0011GVÔ3f8±\x000bv¹Üûh¡§\x0005!-´ÔUÌ¡¢®¡ÁµuU¶\x0017Ö2OÒº^\x0013P\x0013\x001c.ª"ÙêÈ\x0016Á´Î|·=#ðr}Dã\x0011
nkTÏB5F0¾Õ©]h¥]\x0002\x000b­\x0005\x0019-î~bZCûÀÀò®µX×\x001b\x001c¦õ®-~\x0015Ù\x0004\x0017[KBÆiù¶­@Y\x001fÚ¦iMO+õ
õÖGÎge\x0003\x0013¹>ÝbÁ¼V¨	ÎðwFZqKú)×\x001bï|O+óe¸Þ£vÇ./²	VÞfÚqJ{6ö´²Æ»pe['MÍ¿C\x000ee"S\x0014!õ,É\x000e÷±5(áªÈê\x001cljý4ê IÈÎ²T/.Éí|ÛÃý®_¾ûøæöo7ï,97¿Þ¼½«»Ó*m|ð¼\x0001ÝrU¸70\x001c/ûåóWO\x001e}wýâ«JxyýôúÅã­¬GÁ^]Ï\x0011»\ÏÅÜ8t©öÍâR(¨}³`I/Æ\x0008\x0019õ2ÉÖÂácÔ5Wk|õé\x0003©©/Ý»éeØË°Ó
ÄØ­@'cS_hÆvô\x000e­Ë§a¯^\x0010\x001bm\x0018;\x001bºÚeÐv\x0000a\x0007hº=\x000c'Ü½¸Ý\x0001q;ÅH³¸Mm"Cnz\x001dõãvL\x0019ör+Øx\x0013ckG9"nn\x0014O\x0000ÿ\x0005â\x000e½¸Ã\x0011qg\x0013èªv\x0007¥kÆÏçÖ°)ñÃû{iä)ÜØÉ#æ6VigyÃ&lÚ\x0013Ýú#Ï(Äv=¶;mxÎ\x001fvúHc\x0019¨JÁç{ß¨JÈÝ«I<¢&\x0019°-¦#vÓî4|Áa§^Üé¸±£Æ\x0013wIfU5qlLâpé»7ÞéñvXÌÂÚ\x001dë\x000cÀÌmË9M¹ê\x001c<~= í@
8¦»"+6$ñ´ dµ §2#Ì2óÙþ¥Ñ@
I¬ÙãE«2nÝùr\x0013sç«\x0016E®I×ÎàÍ9YCë¸eØ¶Ç¶G°óíÛ³¸i¶Væö-òÃùBîÔs\x001f±Árì\x001a²§W¸=kwðçÉ»¦Ì¡h*¹&o\x001dký\x001e\x000eGoò\x000eÃg\x0019·ïõÄ\x001fÑ|A°,oË7\x001cB÷°kKÆ\x001dz\x0013\x0018\x000eÀ|¡^Ó"oSÏ¥W)6y§'±»Q2d1·6hû*·®O~8ÒÇÿ\x001blé>ÛöÜö\x00007s¥ÀD\x0007[¸ysþÓa£¼»wðæ÷ØãEÜÊÔ\x0014_æ¶<Öxw»L½»L\x0007Ü¥·íî2¼\x0001~\x000fû\x0000DÜVwú_åÜH×R\x000f©ÆS¸æÅ=,l\x0010b\x001eû¸1·JæDÅº×3sójo\x001d¡2lÓ]ÎJi³\x001c;òmç«dêÐ\x0012=Ãúf\x0019µíÎ$~S\x0007CýM\x0019Û×eS\x001e£MIkìeÜÐ%1Ë¤!176å	ôµÏ1»!îÇD\x0013x\x001aµëuÄ\x001dÐ \x0002Ï'\x000c
®B=Á¶\x0008ÖÓ®ëzèÂ}@Ú(cgåVÕÃ\x0007ð¶YîÓ.gÖ÷\x0016Ð\x001f°4\x000feª\x0011lðZ·DÏiÒö =\x0012	\x0006ãZ$¨\\x001d{¹]hò>O½}¯Þþzg5¡ÇøÚ³´{å°0YÈÝ«·?¢Þm®Ã:Ó\x0013L\x000b¼Ó°JÆ\x001dº@\x0010¿\x001e0çú\x000c\x001a¬ /y°jØN'ã½ÓGN\x0002,^-ÜÎaJ³pëÈÜz8ïGÆzýNô»m©À¢aÃf09±æDì^½Ó!ë
´ïÎà, HÖ\x0004ÈX{vCY#5OHKp§g\x001fÏÂ\x001eö¶	±M}ÄvkEe\x0017\x0006ÙD:Ç:çpí´ø\x0015\x0014ôÜGâ×º©;Õww4üTiÍy·3P¾ç>dLTKfb\x000bÉ[Û¦'§ùJ0½\x0003joï´*"Äx(îæ\x0000ÖÂp^¨\x0010;õØ\x0007rkÞ;T
WUØËú.[úNÂ¶] _\x000f(IâÀ\x001bû;év\x0016\x000c§\x0004ÑÇÇÝkÉÔ1ÚÀÚF¹C­BE\x001b¸p\x000fû\x0011Ü½1±G	\x000eè&n£QÑ«zóÎ\x0003{bj
 çCxGå<$¾²¤ß¾E&ãêo!wì¹\³Lô$ñ\x0005
ËOXÞÃé®2n×½Uâ×\x0003)ªDmwYÞ
[o«¼y\x001d\x001dÏq÷\x0017K8r±ô¶½Ä£xâ\x0006¾1d=9ï\ö748rCÃº.6n²'ØêÐ¸ÏÓþ\x0006GnhÞ´
*8YÔÛð\x0006Q;Þ·&Ã\x000e½#jébCÜ¡ey\x001cWæ>ïB\x000c}a\x000f\x001c)ìñÊqp\x0012©=¦ø¢ã99ïb	}i#\x001c©mÄ%%` Ô[s\x0002Âî¾\x001e	Ô#ùì"9Ý\x0013=\x0017	bÎ±Ï+Étª³Þøõz»ÐîÃÖ±z\x0007\x000e½Ï«q*öÜ\x0007Ô¤Ôñ7qSòØÅþ\x000bÄÝ?¸#\x000f#\x000e{>ÉYFÃ».4í\x001e÷(Ê¸û7\x0006wäÁaÇ:;K×
©g5árO!w/o{DÞ8½åZÝÅæu\ïuÜ\x0011¯ã°ß/;|µÌ\x0001	' Æ#7ØºÇ>TIå8{\x001cqP=×­ñ>`üóÓ¸c¯&ñ`åWlÎÒ\x001aª\x0013äG\x001d;^$äî­`<b\x0005­¢-ò\x0006§×qm¡q\x0019xu\x0012·ï\x0013lþH
|Õ¡"X8Êw4HÍ÷yWbß;KÄY:MèTfM§\x0005jÐ^Zm\x001c®q÷EwþPÑ.IÌÂÅIÜß¢lóäm;õÆ¯Z\x0018L
ª²Êpµ 8Ã1l:¯
ÌCg\x0006Kù¸;ðËv\x0004à§?\x0000Ý°O»\x0010û>\x0001á$ *a³ÿÁ¨°yß¸Òçiw÷G.òà
?¡¡P±4v 6-9OÞÞöÜ\x0007þÀk\x000e½#Ô\x0005^í\x001aö°[RÝ×¦û#µé8]A\x0017tU»míb9\x001c\x0008%â\x000e¦óñøUÎoï6¶\x0010^,-/%Â\x0010ö´¼wèóÇáHþ\x0018rü\x0017 °UM,N´!ìaw¢\x000c\x001b:íÆ¯\x0007Äí¹*$î\x0004À	\x0011ç¿X>{\x001cd\x0001\x000b3ù)*ÔfP\x0014÷òÒz\x0011\x000c¾s9øõ\x0000wl\x0005¥Þò»v\x000eHÚ{üi2ôip$m\x0002Ö´çxüÈ`c{?ï\x001aCj×ØñÀ´ØÜ²h	]+mkdµö¼rÒÐWm#U\x001bÈMI*§°hð\x000e¶:¯.\x0013\x000bÆ×Øé-ÉwÐj{<é67hc\x0017×ig2öíÎñP»³
ü\x0016å\x0011ëÚmXw;*õÜG\x000e%8\x001ampO\x001aU\x001dÃRy£Ð)7~=dºÓR)H½\x00178>»\x0015K§&}ef<RcË(ùÃô°m}k\x001c>¯Q;öï9ñÈ{\x000ej7\x0015ÉfþÈÚÝZYÏÓîl\x0004×ªª\x001d,ªPp\x0004\x001f`°\x00147\x001c
% p\x0017\x001e§(\x001c£O4i%«§.bË\x000b3ý\x0019ÙXe5~)\x0007ËðÅjl¿ùøûy=nX¥]!ùJïi2«\x0003Þeí¬<ô²p_¿ú÷{Qu*d5©-6Éª¡iê)\x0000OºVÃ\x001cæ<lê`\x0010VÓë$(,¢"X\x000b<@|\x0018?M³®fá\x0016_%T\x0002wÅ¨¦Ö\x0002¢\x00124ÒÍÇûQ¡C\x0005¡X@yçf©çé¼e,Ç	¤\x0002\x0018¡\x0002 ó \x001dLÉò:\x000eÓöo9µ9í|7¬í4À
5\x0000\x0007tÒÔk\x001eÚP`Y\x0007ôæ|îý°\x000eX¡\x000edBÞu¡l\x001b'­R\x001d6¨LÃ.wn]/Ú5¼ØR%àyâ¦­a\x0007Ð<ªïP½\x0010\x0015®t\x0013k¤Ù×Z·Ó\x0015NQXèN\x0017ÈN\x0017®\x0003§µaÙÍVãªS\x001bÓ­=öÓ¨®;[Nv¶°<2²\]\x001däêÊËØ\x001euÎÃvruB¹FÇÓÌr(éÄ"Ù\x0018ÙjéÍ¥'»a¥\x0002\x0008»Þ)0\x0003\x001bBÛÐ¢vtè\x0010\x0016lNìÞÍ\x001a:Ö dõË\x0016\x0015êÐ§\x000c»¬\x00122ú\x0014ØØ\x0019­(3Z\x001e\x0017\x001dò\x00161Åcðµo\x000bÌ9vS`\x000cÖ%^!¨±]±/íxË©3çØØØ¯(<_¯Âs»ëtÖ\x000c\x001bø|Ùñ$ÆYØÔ\x0005ÜI\x0016p{¯Û29ãy¯v¼ÑÙs<Bê¢$
p\x000c§¦ÕB9ö&Ã\x0015\x0014_\x000eì°æ5v¬QÈê(YU3\Mcíæ\x000e¬ý¬Æ&©ÆZcµ
õñ\x0011mn;ÐN¹\x001eè;·Y%UYKiëLëxßÆ\x0008¢\x001d6\x0008ÍÓBO+ÕYß¼-NtìÁÚ"¼3tV«ØÃJ6ðBamo´9Öfw\x000bÃtØ4­î<ÖR\x0017¦Û²)«ù®
ml¢=Öõ´B\x001f\x0016ÚZiu ­\x0017\x001f27¬Á¦íÓ\x0005Z/ÀyìÄÀ6¿æv8si¶×\x0004#Ô\x0004\x0017I0n\x000fc8Ãé>»¡é2y·O%ün\x0019\x000eçÏð\x000cY\x000e=­4ò
8
¿JÖ`½[¬i~l<j~¶Oqha\x0003ÓÉ|\x000fsOäK£fcë\x0013 æi{M\x0010&9|L¸ÍÃÓâ¤H²Mm\x0001áöZ¿ý´}²ÓJ¯¦\x000f­Í"ð\x0019\x000b§\n4ô\x0000Ò\x000b¹nK(ýblãetas	å~Ú>¢\x0001aDM\x0002_>òBg®ÛÍ¬ã\x0019þÓ¬½ÒPi\x0013wT\x001dZ®åeÚÇS.\x000cºO!ii\x000e	'<\x001eä\Ó-7)¦+¨wÓº^\x000fT\x000fRsº!Ñ6\x00074\x0008|s§¤hµë]\x0013º\x0004¼å\x0017¹ýÝ\x0004]ÚÜ½\x001f6ô°ÂÜ\x000cnÇ Ú´ÊÐqæÓãSÛ\x0019´½Ú
SteÎ\x0011©m
´¨,\x001aÍæ+ßuN¡õ½Úzá£òíÖuÂÑãn»\x001fS:%²õ}¬è¥Ùzw\x0005tkHÖªeZÛÔö\x0014ûåû3æeg¬äëI\x0011²\x0008\x0013öìuÓ)o«!Û6J_îÊ9 áu¥vYV;\x001cÏ5OÛ_v£ì²\x00135-\x0002u¼û\x000b\x001aÙïúáxÖiÚ>õ¥¹¯2CÛ\x001c.x~\x0019_¶¿"Û>ù¥Ù¯`Ër¦ågüÔ\x0016V\x001fÍÔ\x0005õ¾<\x0002û¿îÖÓ<¼ùíã\x000f¯ßîÙ
\x001a°B¹\x001a1\x000b9\x0008«9°¤Û\x0004;°>¼þæÕÃÇÏ6\x0012¹YR
9E®Ù erÀB®xùAûëQ&Àí\x001aüºÂ)p,L±\x0015\x001c<I[ùLº¿}\x001cÖä)Ï\x0007Ìë\x0017rØKà<a3©ûÆ&¸Ýûæ)nà\x0019E\x0016°ÕÎWpÇ=TIíû8Aî×äT\x0017Nm­¢\x0007öCdRlYNÅ\x000ekìOº\x001e¦°]¼"=QõÛÒãE\x0002\x0013ØqýIqá\x0014vÔäÈ³¼S)qËÜÉ~Ç\x001dá\x0013ÜiÍýIéì\x00147^;_ \x0002ó«\x000bÎ1:Ó¢¬vø¡ûù¤Zy
=q\x00035X(^b§Ô6!\x0018îoH ï\x001dç1Ï\x0005eNgù¨äÜ»ÕÏDï<ç§sè<pÓ\x001aÜVí¡ÑÜß·3Ñ;ß©\x000f9O§\x0002£[ei¿jjµgùîØA1Þ9O}È{:ãØ{\x001a\m_Í¹\x0010Xê;&üM wþS\x001fr ¸A¢D\x0013\x001c\x0015Ñ%Ó¬0Ü\x0017,Fï\x001c¨>äA\x001d´0Ñàô%ÒõÀó	s\x0004|ªÂtNôÓ±\x001dSèØ\x0011kHa¨\x0008(\x0008M_vtÎLw~T\x001fr¤¸qEÌ=^Û\x000brì~*yçIõ!Wê¢¥\x000czQ\x0017¨VÝâþ\x0019Vûô÷£ÎC®ÔÕÑK6\x001bÃ:C9sk¶ù\x001e}*wçH?Ýt8ÃíóEÎ\x001b]¢etßDnvL»@ï¯ \x001c©ÏÑ­'©ã?E¬èÀí?a¼tTÞ9RsÈz\x0008MÑs¬K\x000bP<)è\x001dS&Ð;GúéÂ)tãh^F§®ê,õÀ\x000bAÊ\x0010×\x0013Ñ;Gj\x000e9Ò\x0003.«eÔNãîuDwmp¡÷îLËh:Gj\x000e9Rßù\x0017q©a£®OÕÎ~Ú?%ô\x001c©×5VâÑqQGùn·	ôÎ\x001d}:5w\x0006=ÖL­ÕÆ^Åª,^s?;6\x000bÈm;_ôéØÜ)ãvk §+Rsîùõ{¶LwÎÈ\x001erF\x00114M	²Xx­«ÿ÷mY7;\x0006,O wÎèÓ
Sè¸æ®¢+lÑªÎÈ{Þ7ä`Çå	ô>#zÈ\x0019Å6Öª¨Ù\x0019ùÀ-ù^í;Þ9£O\x0007\x0016O Ç|lxþy2©n\x0003s)FvFàwÌ\x0018@ï=äbm\x0014·
\x000b
ë\x0011
mM©;æ3MpwèÓ±SÜ«\¬²Ü-0÷Eè{&¾-è7ï¸ýí"wç>\x001d\x000b8ÃT> 5ÐUÙ\x000fÅzÎá-Ü\x000fKàÄ"ïüÐ§\x001b\x001d§Ð
wÑ\x0015ÛR%^:=É´ìX÷´\x001c:O\x0004G<QTËìCôXÑy07¸\x001dÓÓvª
tnèÓY^Sò\x0006C%1V©fËCh*nw\x000c<\x0010xgË?\x001dÁ3î-ö\x0000\x0015ãvïªåìô©î\x0013:k\x0008G¬aT:azáö»!
w`\x001d´c+ï\x0004zgXàa*óÖÙ\x0019	ô«÷L\x0007¼Â«\x0013ä]#v%b[&ï©\x001555¤xl\x001d8u¦¾N_Â1}É1\x000b\x000f8ôJS²¼Ó\x0002» Î2-Ê¬§9Ô§óOg9L=\x0001`ñR50\x0015®Õ,¶Ý«ùqJÔbí\x0003®ü\x0007]sôÓÛ÷oö\x0000çpÄP`\x000e¸æ»Ö\x0005M56\x0011'QlV<}ôâÉ\x000eÎÅ '8	g\x0007ÁçÃX&\x0003b0Õ«¤´ÙJ²S/7\x001eäÄ¯ó \x0001,eQ \x000c\x0012/\x001a\x0010ÊõµÍæÂ¤®'u"Rèy3Ta=c&Å7L\x001aðIÒÐ\x0006	)ÖÝRm\x0015f5ëÐ\x0011écé035Iº4Â\x0016Òu'ìnR,7í\x001cþ\x0008îã©.#j5þ'AS/Ò$\x0012©/\x000fÚ,ÒÚHæ³³0M¤ÇIîH\x0016:E&àêß\x000cÎ¶«WSÚl\x0015ØIºd
ézÇ~ÒW¯ÛË~\x0003ýú[u³\x0003>®¦\x0006zH¦FÑ0\x0004ìÈ©á8£ÔT!QSâ09
õ8ù`ë<-\x0004µÄiN°úÆuç\x001e¿
@U¤¥~;|cµPÑÀ¤Ã²¹IRßÔDª\x000cÍ\x0019\x00073¡è8ÑsT\x0010·j)wöFß~öC
\x0014¥\x001a\x0002Õ¶&'üøKño!]\x0017ÿNz*¶\x0001\\x0015\x001bHKuàã\x0014ÏU¤½Õ7"«©¸Ý\x0006Ëìk«\x000f<87*·Ç?cêiUwð«D m\x0000îoTt´æ¨ÔmµÙì'."\\x001aÙ/h,$àêÔ\x0014XG\x0019t»Wa')ô"\x0005HËëu
L<UÉdÒCv,\x0005¾ÇI{D¦\x001eG	ÕÞÝî$RÏ!Þ\x001e°\x0013ÔuîÞ:»ÇX\x00065a¬gY¤¶t³\x0019'é²¤\x0006%ôN4ð$d[\x0005½&R»Ù	¶´WÓ US
öBpt\x001dE5
í×?\x000eL\x0007#å\x0005	ð$!ÜêbÈ;YêWÃi2Çc=è)©W\x001aWo\x0015Råù\x0017eÒÍÞÕ º\x0013)~\x0004¥¼P	"Î
Ñ\x001c\x001a\x0002
Ã\x001a¡IRÓç"$\x0019¶\x0008ÔÄ«È§)\x0012çfÇýNÌ>µ\x0003¢Ü\x000eÞê-é(>b\x001bu}\x001cu$Î\x0002nN&ÌgP\x001e&S-nvÑí\x0004u½HH¤àØ9EÖJ6?ÐP.\x001cxH{K
"Kêç\x0006û½ÊDê¨:\x0003ÇÉ\x001d']­¯CÒ²¾Ntm¦®Ä¤Â\x0015Ù'~_Ïê\x001fßéîÇÇ¯Âû}MC%Ð¸É¡r\x000ceü\x0019"5ÝïèÇÿß!Ò>,u¢°Ôã\x001eÎª¥ÉÒ~\x001dÔRªôË×Ò\x0013òÏniú.¤ë¦ï	Òzì\x0003ê\x0004A×D!\x001e	ó­wéÚ\x000f-¶û./?¾yýÛÎZ\x0015Ci\x0008\x00132YÍê%ïùÝÇ·,1èËWO\x001e³Ô¬ITqÕ~Ù\x0016ÁEXÊðr\x000eµÙÓ¹Ô®I­4ó(ßdêH¦\x001f¤ÌvVo7)¬IABZÖ9&S*²vI5n»ÞMêÖ¤N$S\x000b¼¼\x0002¥K"µÜcjÎÑR¿æô"FG3uD\x0015I4¶öas&ØnÒ°&
"\x001aK\x0015°\x0006_ <Ô´E\x000fi8G~4®I£H¦\x0001(¹I\x0013î\x001d¨µº\ÙeÕfëùnÒ´&M"jËkÜQ¦ÔDç±\x000ceº'ßKºôý\x0015»¯DBõ@¡&`\x0004]«,k{ê;C¨ºwQ2\x001f¥,mÔ\x000b`0R
¿jæ4aNuç¢´ÈGá¦ÄK_\x001c× æ\x0008ºiê°te\x001aµóQZä¤\x0002æ¢Lj\x001d§\\x000cíø\x000f\x001b>§Q;'¥e^
(o.ÜÅäõÚÛ9Ý¨Ò"7}ÿÕ"TjÏs\x001bó³PO9TÒ2Ge5½åaT\x001dæZáÝ\x001eÇ¿\x001bµsTZä©0¯§ YU\x001aíhVukPÊnÔÎSi«Ò4I-\x000b5ÕÍä.AlKð-ê\x0004ÒÎSi«Â>kª£\x001c_6ÿ¶ÿÍyT{IMç©ÈSù\x0014Úúñ\x00004è+o!\x0019ö¼N£vÊ<\x00156úWòøõ|ù³K0}\x0006f\x0012¹)	Ì\x0012}?n{\x000e7«îFíÜ¹©\x001cD;\x000eS\x0014W
;«yäv}ÌnÔÎM\x0019Âö¼1æß¿
ÕðÐ
kO	SLç¥ÌKaóÕ²&ö¸6ìÁªsP;7eDnÊo+9SëÕvAánöiÒÎK\x0019Ê\x000e3)8´Ö²Ce3¥Õ\x0019¶ßt^Ê¼o³¦LT
·l×¾Íæûá«éÜ¹)S¶EUª¸
\x000c\x0012kê)þÔv^ÊÊ¼6¸[½ÊÔÕGèd};RÎBÚ9)+sRS\x0014Ôã
m³Þ\x001c\x0002¾\x001b³sRVä¤2\x0015Õ\x001f¨5­`JÖ¶½õ§Ä§¶O÷É|²-?á\x0003\x001a"Ó°lß=å§ï\\x0015¹(§\x000c;þ\x001b\x001cif\x000bw\x000e[·ù²»´sQVä¢p¸+û x\x0016\x0001xn\x0015¶Æ"ÔÎð[áÇ}FÎS°XÌ_Pn¨hw£vÖÔ¬)\x0006~Q=7¾\x0001ðÂe³¹Õl/)tF
DF*ÿ\x000fí6ÌLÛ"À4\x0017c3P»ã\x000f¢ãÃÿÒ\x0013¸à²zSÀÍP\x001cM"ÕîTìTåhÚRà\x0017=\x0016yÔhÊ±©²ï»Q»S\x0005²Sµl9
1Ñª¸d\x00134\x00058ÅªBwª@vªLâÎFQ\x0003|Á\x0001\x001c¤!U×¿¢\x0014À\x0019Y©\x001aø¹Ï¸æ\x0001¶w×0ê\x001e)sçU²\VVó[ßÜ~¼ý°o¤¨¥G^ëT\x001b\x0014¡yO÷\x000cyòèÕ£[]hæÎ«$\x001a\x0011i\x0008ôf!\x0018,)¤ÑS@oU#Ó÷Ú5©\x0015\x0016_Dª-7²ª\x0014yØiÜ|BÛ
kP\x0010&OIt\x000bùvêy(\x001e!ÂQ'gº5©\x0013Zø_Ì½]®&Çn%:\x0015Mà\x0016ÿÇ²\>.@(I\x0007·ò9ÕÇ\x0005èHFIrß~ëiô\x000cnÃ3ét0/¹wî¬\x000cf a7`×Þ\x0012Ô«A.F\¤ý)M»0[×aeé¼å\x0017\x000b¦=ÒdA\x001aq\x001bÏïÂ«Yän0ÈÒè
ç«®"Í{¤ÙdSz\x0004>§aHÄRC|GZOÿ2Ò²GZL6Mß{º¸*«UQ¥¾÷]\x0006Z÷@«-F\x0001¯Wk\x0017û(®\x000f¹J:_øs\x0011èN\x0014uQrÂ¤EòFï@·Ô.úöP¬=¿
U3¢h/\x0002{T\x000bX%K\x0012£æC\x0001©i¨¢ÀÄQököïïIXó\x0013ÙÀJ>ßæp\x0015ªâ(0TlWi÷°*_P¡\x000cÞ?}í½T\x0014XªAd:mq^ú<|\x0019¢³ÔAµ\x0000©")°±\x0014íæ8d=FE²ü\x0012¤¤ÀÄR©Å~\x0016fmÁÜ¤Ef«|fûßU¤¤ÀÄRÑEîÝr"/)ò·\x001ce	TÅR`¢)zIaI'\x0012/çn´Ü\x0010/?_3q\x0015ªâ)0\x0011U$ùföþF®üq,\x00128ßv\x0011)*¢B\x0013QeéMï[6=
½ò<QÎ]Eªx
M<\x0015Û=Z²éòùä
Å¨+N*ê«§¨j\x001a;Oa}´$¡ÄÔ\ÄTT<6¢b\x000f/2 ­ªrRyÎ¸åÓç²®BUD&¢¢F\x0004Qu¥\x0001)îòèó©hÃe¨©ÐÂTÅUyÞ¤Ð<ëç$ª±ÎJ\ª¨
MTU{|O<)SI ­N{.CU\6®Ê²¹ÇÓÝÊ;/\x0011\x0000NÛ/CU\&®¢á(ÞÐî¦£s\x001aå"/I\x0000PQ\x0015Ú¨:QÊ0ªT§ÜãB}¸[c\x0016ªW\åM\E\x0003R¬v\x0001F£oÌ\x0012\x0000äÔ^q·qU3ªçMBí"Àë3¼êdYC\x0000^q7qUiP<9Êõ&fØ¨Ûè}¨úÝÏÆU´'TYª]ýPi,å|s×U¨«¼«ª\x001b{_\x0010=_ÿ2:Q6ö:»ÓH\x0015UyÓ¥*\x0001ð\x000f¤Ó³Ý©åúïN\x0005.CUTåMTÕ>õ\x0008ªTúgÑq\x0001È¸$Yõª¼ªhª\x0013ÄªYÆ<|aÔ%ß_171\x0015)\x0013ò¹ÌÖ!À½&L)ò&jYÜS=µ&ó3E}!-­¸ü\x0005ESÁDSµ¬ñ\x0001ú#ëz©øgJ\x0016@U<\x0015L<Õ)[X|Nòîï4ÏtZG¿\x000cUñT°ðTqàè
}³j.Rñ/1v\x0015<\x0015\x0014O\x0005\x0013Oµ+©Pª¯EÞÓ\x001fÅiê¢^T\x0017¨,4EÚL]\x000cËCÚ6n6mB¶é§ß h*Øhäß\x001f6ÍÜF\x0003¼vlº¦¢©`¡)Rgz\x0015ÙÿÃèô-Uî©éxËÎ4TESÁFS´\x0000­l`\x0008N
*íºÄª§§HIô¢\x0001[(è7j»_òkJQU°QUvªbxU¥áGvþÓÑ¹«H£bªhaªâR\x001dÏ\x0014µJoRõc\x001dÄ»_TL\x0015mLUT©|Fy¦\x0008#M-iIF\x0015\x0015SE\x001bS5¨¦:Ê?2\x0012Mü¬ª*ÚªFn£Û¬äI\x001dÄ¨§2N*¦&¦\x0002Ñ9ß.$Ã¨Eæ¦cZR÷ºÂFU¥JA­\x001eE\x000fQÖÃ\x0015ÚEy\x0019©bªhb*hôïXX=C¿û§^«íFuK©¢bªhb*Úß.¥_¬£}^z¨\x000b.ÉT¢"ªh"*H\x0013U,5o+_Óö¹6 Áø]\x0006ªx*x*c¶\x000f\x001f\x0012,H*,iPI¨¨Ú?â+U³)Ð#\x0010\x0019\x0015¨\x001f­z:p\x0019ª"ªd"*Ue\x001cÙÍ¹aIçGRÑ?¢?¤ðÖ3Oj³|O©²¨À®¯¤bj2ÅT\x001aôâ2\x0015-iõ<=':£tYT\x0005ªd\x000bT	yQµoijÙI¹úK8^\x0006ªÜ?ÙÜ¿Å)'ß*Ó¨QÊ©\x0005ÜR²r©ls©ÄÍÛBg®¥Ä óÛÖ¡\x0005HGeGÑ2>~LÏy\x000cy¦Q¡\òCeC\x0015ÚÐÈï~	è]b\x0014SÓ÷´¬û(M\x001eU0=¶\x001c\x000fqQH;Ý)p\x0019§r¨lr¨\x0012²¬¨¥^ê!~ü¢\x001cª\x001c
i^ >ÿ\x0014\x0007Ò%5ÿ¢\x001cª\x001cªýséùÁÆ¦"\x0012G'E<Ü*2
UyT±y\x0014­\x0015à\x0015è¾ÊcZc¦±\x0016úT\x0016õ2TåQÅæQtCeß÷r\x001ek¨{m\x0005PåRÅæR5K^
¯7QFKKüfVåRÕæRÕ³\x001cvûúÍ»¼@ê\x0010U>UM>UakM¼Øµ}²\x0017yìO'\x0012/CU>UM>U=Hqª\x0005W^Y6\x001eRòª<ª<ªÒz\x000eAê¥5æÓÅù\x000f7eNCÕ=ô&Ú ²÷·k\x0015÷&åÇÖ]\\x0011§àÉð3yUWµ4¬ ©Æ
U°»\Æª\x001b¾Í­¨çC"wM¶À;
èi\x001fp6¿z\x000c{!¶ÀZ\x0018ëc·û\x000c\x0000ô\x0014
ýhÂ$û§¡oF\x001aFúT7ã2RÝôëlUÇ\x001b%B2(½(³;\>õéÐÅ³0z©¨´Þ\x0003V\x0019kÃ[\x0014XU{ibÛ£\x0018°`\x001b«èXG3ÝéËPµcF\x0014JK{^ñ~mRÎ"µÖTWÜ\x0001àIã¿©ó¿YµH;mûx!J³ê(¨\x0015\x0005OÚéMýô-Î²[\x0010Êèý®NºS]Ñú\x0007ºM\x001dL}ê\x001bÖ,v2õYÇÍöw­Àª=ËÔý]÷¼qÒC£©¢¹4\x0000¬x¬\x0004ÝR
Æê$;G\x001aV9úÃ®iÅ\x0015èFe0u*\x0017×nÕAZ\x0000X¼V/³ÔiÅ 
èî_0µÿnHÓ£W!\x000bR9\x00001¯ª{jÁÔT[¶Nz¦×Æ\x0008[\x0000Æ¨RZRZ\x0001ÿdúÏæXyÔ\x0002­\x0006±+'®	ýw\x000bÐ
 `ê\x0000-à\x0014\x0001\x001cï\x0017­5»õtWÆe¬Ú±L}
«}6»\x0006î«m×ì\x0001uÅ\x0008 èE0u,\x0016W"¯Fór\x0001>\x0002q`u+¦\x0015@·\x0001©\x000fuñ£5iL¯I&Ài h\x0005TíY¦æºÒòýWÒ\\x0011ºFMêÝ\x000cuÅ;\x000bè50õ¬5¨EòV2ëc§^f\x0014³®`,Ý\x0008\x0006¦N°vME\x0019\x0003q¡ÈÄb\x001d@Ì+ân¯\x0002SU3+ÊÕÅÑûløÙjÚ¤µ\x0000«îZ\x0002SÛR»§Vá\x0001çy+\x0005	~Ë»PL+ÞÚ@÷\x0002©\x0019¨PVÅ5V×Ç:ÖPÅ®+FA·Ø©Ç¦4ZQ0j\x000cv¡c\x0005Ù¡\x0011ý\x0012ÎÒ+`j]ig\x0000E¤ZÃKéXQúÁ#®°\x0000Ý\x0012\x0002¦\x0002ÙZY¥\x0019F>¯Q\x001aB#
ë]Åª\x001b-ÀÔiA\x0005jÑUlqª·\x0004'ê7î%XÁ\x0004ºÑ\x0002L\x0016Íµ¶2Ko´rµ|#àVÌ.î´\x0000S«\x0005ípãF[¬
\å0\x0010eõC(+Jn {-ÀÔlQ Fî
Ã\x001aó+>­Un\x0004¡ê]ª=ËÔnÑ \x000eq½\x001ayM2a\x0006ÖPN¥j¯bÕý\x0016`j¸(H3Ü\x0017ÍÂý¸\x001bvMK«î¸\x0000SËEAÌ¢«\1ôÇÁD7N\x0014¬KÎî¹\x0000SÓEÁvÅvÌ\x0004Ñ	ÃB[a(+*¯è\\x000b7á/\x000e\x0003µ?f7¬Q\x00186%e"Ýx\x0001¦ÎBÅÁ\x001cø\x000c\x0000
_t¬Ò%\x0010ÒNFÐ­\x0017`ê½(t\x0001,d\x001dðµÜRXRÓ\x0006Ý|\x0001¦îÒ'Õç^}K7çÒÚç\x00158µ_Z/
)¸ÇYMÝ¯Z5(kÉn½\x0000SïE¡öÅ"XA2,\x000bAXÒ%\x0004ºù\x0002LÝ\x0017\x0005\x000b¼Êã¤\x0002G«:nÜ]ÚUã§ùøÛ\x001en\x000bØô\x001bÚæ¸\x0019\x0006\x0017	¬¶9fÓ­\x0010cþIÉ.Ql_|ùîã/\x0017`&RÜê\x001f½+ý´Fz×è3©%½\x000có»·ß|\x001eãC\x001a0î¥®b+\x0003¡Qé\x0000\x0019a<
ÿ×@z\x0005Ò[@²\x0019\x0003u\x0008vþÓ¶³ 	aPf\x000c\x00063\x000euí[o÷Ô\x0006ÛéS%R0>îRqº1Éâq¤ÑJÈÝÍg^~
bT\x0010ã<Ä¹·¢Aô\«li*Ê·.§[H/,
d\x0007!Ê\x0012o,gþi-²`<½:_Á\x0008\x000f±Ï-ô¸b°dé1½Gì\x0012\x0019ß"ÚÇ>Í@/|¨\x0012m ÷²D-Y¸ë3Ò[Nm¬ì5x*It	¤W_[UN®Dé÷ÜâOm©(\x000eSÖy/¡Ô¾
\x0006çÎÄÜ2ÊwA\x001f$w%]BU¤\x001f§QÒYä\x000fN\x001d©ÈÇ²\x0008Êx:Ü
eÐ(Ã¼ï¨
¥tw\x0014\x0010©Ìòt²ï
Jt
%ý8²AKüÅ3r9¯\x0000]Ù\x0019åi_Ç% Ó\x000b°ä\x0017È\x000f
edÌ\x0002;ÐhænDÇ¨¼\x0007£\x001ae;øÂ\x0017v²%+Òî¹»>îDÞ\x0019Ø\x0011#?\x0006O²ý	xO\x000bãP¢:\x001eçÏe,á\x0015pF¢Ëñ´ÜÎåí/îQÛ\x0012çm\x0019I\x000e§\x0013äC\x000f±8ÏcQ¹la÷Pf2\x001bP¶[n\x0005êI¼g{Tå¨\x001eî^!BP(C0 ,0¢z£!fH\x0017|q8A½hËþå©5ÿeþ£{n/kùFí]\x0005í·#fsÞ?õ ÷Ó>Äz£g\x0016ë¥F\x0003N9Úé\aÐ÷O
:
46\x0007÷ìëÔ«%\x0016åÊ7e\x001d·#R\x0003ú×§@ÿ:
´\x0005xd X¸©¬8QjnG´ÞÍ[Dÿé/OCü_æc<¼Bñçõ
¸4Bü\x001dá'%&NÓu{1ñïþãýüñ/ï/\x0001unc \x0002J\x001cßu³\x0017ùâÜ©¤Ôwo¾zûåë+hB[héå°Z)Ôe²\x000fLeSYö¡ÔHh÷JSh\x0011i¦´£<b}ôÃ¶§ùçe°Ê´ÞjZ¬ÐÀ"¯@ÈTBîG¶Öó«h\x0003ìÑîûæÐzn~\x0008$ßå\x0019lzÚ5`³\x0002`\x0003Å5Ëf¾ÄÓÙãÐ®À\x001aÕÖ3Û¾=?Ý$/\x00116\x0013WÉ18]Ôt\x001d­:´Ñzh[ÈâT:Ñ\x0014£­\x000e\x0004ícü\x001eì¾§`\x000elbíöv\x000e<¯nh`ÙÃÙ¤Ì¬f%u9&\x0016\x0016¶÷\x0003\x000c£v_ÆU³Õª©\x000cJhÉ`Ía`= »µª¨U­Q+ç>nÒ rwYÜbÚÀÖ¾¯ÝÍÇm\ë¬ÍÈÝ\x001a!
mfY^k9æ»\x000c\x0017m\x0001­Æ-%\x0012B»¤r	Ve	ÅóGç«p½¶®7ÛØµ!\x0000\x0015\x001b×%9\x000bñ¼ª$h7â\x0005ôºÏ0Pñfë3üõß	ì\x0017_½ÿøÛoïÿòY¤ÙÅiqSdô¼rÚN%\x001elUá\x0003¨ßþø\x0003ýâ«×o¿ÿþõ/\x001bÑ> \x001bÚ­\x0008j@½lÈØ/Ô{,°\x0017uXññ
DXq{\x00052`-éUoâ
\ï4ô®\x00141¬?Ì\x000fg±>6älX·\x00159óXIÑÇÐã(/{À<\x000c{<Ùù\x0014íÙÅG*»AÝrY\x0003T_D&7ÒTêP¥%.·ÿøaà5ì#ãÚÐn)\x0005ív¡ízC\x0004íqÁ,Ú¤m¶\x001d­>Òsµïh30)´$g\x0015}hñÐæ1\x001e«ã\x0018öå(Ûr\x0015¶
ÉiB»	±\x0019Ðfz\x0018ÞÀn¸{EYå!\x001c?\x001aÌõ*Î\x0006o³9nc\x00076\x0003ËÑÚ\x0017÷\x001be(Çó}³h£6m46\x000f-ú¡KäÐ\x0002¼°l&z\x0005M`ÁH`´á\x0015þ3~\x000c¼¬ÍÈè\x001b%.\x001b\x0016±ü¤ÖåÒ\x001eöö­^ÿû_8ùæýï\x001f½Æ\x0014Rö¯Ü*\x001dûèdia7H§ôaÓÑë?¿ù3o^ÿðöÛÓ´áâ\x001e.Zá¶ëã¶^Gê¥êq\x0017ox\x000fd-xý\x001e¯7âÍÉrûaûc_¢TH¨X\x001aü\x000f;R,xÃ\x001eo0\x001fÈYBÃ»õWôó0FÓððîhÁ\x001b÷x£Õ¾ÅË$]\x000bbá½Ñ\x001fÊYà¦=Üd5¯+YÃ;Ú¼üÐÖ\x001bU,pó\x001en¶Z7æ1N\x0005£ª¹LÔ\x001dkZð=Þb>
õ\x00151ªÖ\x001b\x0012[Èc¤êPÁÈ·îñV+Þv\x001dc
³vÙcMÈÒ\x0012Ñ4ï"û&\x000b+[ü_s7Pl\x0001Vº \!Ëì¢ëÝßÔ4ô±;Ü¸b\x0001¬è\x0002¬|H"§\x0001FoAN#@\x001cvµY\x0000+¾\x0000+a´Kî\x0010
§\x001ew¸ÁP_L\x0016À0ÀÊ\x0018´uXh{\x001b\x001fÃ\x000bñXÛØ\x0002XQ\x0006X9#\x0015\x001cúöY¥@\x0015é \x0018\x000eõX-\x0015i5ZÞ+»\x001dÉö\x0007ü\x0008\x0012«R4P¤\x0001VÖ þp\x0016d _â\x0013!ý\x0008ÍÀ²ü\x0006À»6qÊ\x0011pó¯W, AA­×Ð¤ª©kà*Ò@+iÄDÅE`eâÂiG×!SÎ³lèy\x000fýÂ\x0016×H¢]¨.³¢HÁ,ã8/L<ÏÀ\x0006Ìú\x001e·á<^£ÿéý\x001fÿþá÷ß?\\x001b\x000b;r\x0017"Äl»\x0015×Ñù~Zø§×?þùÍ\x000f?¼¹\x0016÷hÑÖ9\x001ex\x000c®¿EFºä3Ú\x0004§;[&Ðú=ZoD[ä¯Ù6²*"½H3\x0008ÕÄ 
{´Á6W {Åf[\x0017_ùÖ%é\x0005JîT»k\x0002mÜ£VÛºÑ
û\x0000 Ë[ÉKOèó`Ó\x001el2&7z#\x0000ôD§}zVìø0ö\x0004Ò¼Gf\x001d³úÛåC\x0000²¼{á-{´Åh×è¤q±å}þ9Ò¬N\x0012Ó6zO ­{´Õh[jTH<\x001c\x00138\x001fËÎËàÉ"´ ÁÊ\x000c´¾§\x001b\x0017Û©¨õ)ÜtÚr5\x0001WÅZ°\x0006[Èë5vlÉBß¦?;ÜpÚ¿2\x0001W/°Æ¯\x001bôæ\x0005l~\x0016zürµq71«\x0015hUT\x0000kXp-Óe¸»
iv¯Ã$]ÖÀU\x0006FO£×Ü©\x000c²g¹DªPq\x0010óéñu¸¨<
³\x0008»\x0005Òué]âÁøm:SÛ\x001a¸ÊÓÐèi\x0014uC÷4HE:\x0018vQjkÎî>/çó»8;Âu\x0012¶#Ì\x001d¤®¸2ðM#\x0007¿Ý&\x001eÓ,í\x0017-z|ñÃ¯|úøëÏÇJÅuÖÊh\x000c\x0016ûfB'f«Ë/ÏGÿøÅ\x000fßþøîí·_}\x000e'8·ÇI?\x001aÒ\x0013\x0003v 5ó¦gê\x0019ìF­\x0000/ëü]GúxÓÛ\x0002\x001a¢Ë¬\x0013«¾l_H»#Å¥'. m\x0019óÒ\x001ae¹êÞûõÇ¿ÿúÛûKÒ\x0003Qf[f~]ÉÀ*Êïx<\x000b¸»B~ýöëo¿}vóe¼¸ÇV¼}\x0014pÃ[¢HÐKºà=lÀ²àõ{¼Þ\x0016¿²}Kéï
Í¾Y6ÿµüá3o¥ñ=Þ`ÅÛP±$Q&öõ·
ÞtØÛdÁ\x001b÷x£\x0015/z\x001e\x000bÞðfùhAð~®6|\x0019oÚãMF¼Ø¢X_¯9^\x001bnx(zw[ðæ=ÞlÆ+K,VÃy>¿NöÁaYv~Ë\x001eo±âí©#æÄÃe©Q;÷º%ÜDh\x0001[÷`«Ù¸2`Ð\x0002ï·42®ìÚÅú¹ÊÏU¼»á\ò;g\x0005Ü¼uà\x0007Q/\x0005\x0011ªñÇB5\x0016¼Ü¬ìFIÖØËÁSûû·ÈP<\x0016a\x0001¬Ø
¬ô\x0018.yè}¥\x0015½ß0Ê»#æ80ÈÂ\x0000,hlÁ«è\x0002¬|íB\x0001È!\x0002YL\x001e\x000e¯k\x0016À*þ9\x0000\x0007ÙÌ´±ðN0®"8P1
ÌA
#÷Fc\x000b¼ôÇ~%ðþp \x00010ª æ á"¯<miN¦Ê®l(
Qþ¸%Ò\x0002Xù\x001cZ}\x0014.û$-R¯N@¸3\x001c\x000f\x001f¤-Ó¡Õéhý1;]ÒßË¶ýÇ\x0012%hÁÈ\x001aÀÊéÐêtôÖÐª[äõÔþÒ\x0001³Æ\x0003õw®:ÃÊéÐêt\x0006Ñm,&\x001b\x001crøNb\x0000ìÓy«Ó°tàØ=ÂuõÛ$Qâx#Ê\x000c`ðOK^.ÿùã§_ùë¾ô¦³\x0015àù:Tn:LeÌ|fÉÉÎ?¿}÷í7ÿøæ«¯Nß¢üÓò¥WåËYÄBu\x0001iÿ¸ïH&.þ*Ä~ØÛ\x0011g\x0016¢¢m\x0001gî4Ë\x0014W\x0001\x000e{Àáùñ\x0012¡^fi&\x001eÒY\x00118î\x0011G;bé¨\x000fØ·w\x001b{9Æx\x0018MÓ\x001eq2#FÞC±ù]o|¡S<ÜnÙÈ{¼ÙÂ\x0019»\x001dn]öÝÂYÜîTc
pÙ\x0003.ö#\x0001Ü®\x001eH8È!F\x001apZ¸î\x0011W»Ý01xªgt\x0013ÔMS	Å\x0019ÄóÆ\x001eÎndÏÏìßHýð»UF\x0006MxvÆ\x000bn
Ù«Ó\x001cG\x001dÎÕá¦\x0010+Â\x001b\x0017y+x;\x0017\x001bëhÙË +Æ\x0003;å\x0005\x0010\x001a¸¢\x0005;_¬§²êS\x0015çÁ
ÒT¡sáBxßy\x001b×\x0014dEz`g=züI£yÃ±÷\x0015.å´\x0004>\x0005Y±\x001eØiZ"¸®\=ï¹¦³,Úzº-l
²">¸Á|^\x0014\x001d ¥WÃÈÒ|tª´<\x0005X\x0011\x001fÜ`¾ ²*wÞý¨.Õi§ +æ\x001bÔ<«\x0015 æGv!!.&·GPQ\x001fÞ ¾òê8\x0008Y\x0007?\x0010¯
\x0017¨\x000fo0_ä\x0019ÚÔX8&\x0017¹8Åxº\v
±¾êÝ`¾Ä«æ\x001bäáËÍ	\x0007âUÁ\x0002\x0015ñá
âË¼­)ç]\x0012ddéþa\x0019ñ¡">¼A|ß,\x001aäÂTI	
ñ²\x0017\x0000T¼7x¯\x0005¸ÌÝ\x0016Eæ§£OËN²â=¼Á{R0ï¤y=dÅ{x÷
å\x001bd\x0004ÖiV\x001e\x0007\x0003OU§ +æC;óa\x001cÝ¬ÜdJ\x0014qåÓîÐ)À÷ÐÎ{qH\x0011`Ïá¢¬QÄSõÈ\x0019È^ñ¿Á{\x0013\x0007p©?"oy²äC°ÌÊ^Ñ·ÓHmõ6Àð4^¸º*ó*({{P~8ó,ÍÕ\x000ex\x0001§\x000b5§ «\x0010çí!.y\x001eÛ	´°¶k´¥êâ\x0003ò2+«xáíñ"#Ëm{÷{ª ²½\x0011q_Pî\x0017ìîW\x001cO©6ÈÙSÅ<¬|º{a
²r¿`w¿R¥õ"\x0006ö¨\}\x0019!Öïßvï«Eª"Ûîåî},Ä@§bU\x000e\x0017ï\x0005³ïe"\x0007`è\x0011®¦ñÞ\x0002§Ã< ûð¤áæ¡÷ºMßÿÇÿú÷ÿø_.(µ¤\x000cô\x000eÐ[nRåRd,9¡4`Åã\x000b(µ|ÿæÏoÞ)µ\x0008Ú°G\x001b¬hi"1\x000f´©O$æ1\x001aÞÐ\x001ei´i6YÑ¶û(7fRIëknr©RöÇwY´GdB»="àô¾V~ö.£Q÷øye\x001a+(¬`ÄKá\x0004\x0013ËÔRJk·Z~É\x0015tÈñTÂë2\åd`õ2ªÔTö²Â²XÍ´Y6\x001bb8®ÚLÃõ
®7Â-tã`7#¢ØNB¥IaÝ%hUL\x0000sP Ùdî\x0008rò,ßnG²@\x0018'd¦ÑF6Zm¤R¤­ß'i\x001bA¤qr\x000f'íçáª\x0010\x0006Ö\x0018¶U\x001e
ñ¼aªGCüqf\x001anVp³Õº±\x0012ù¦nÚZöPÖb\x001ekQXÕ´t\x001bªlZInJ©¢3á\ò2ÜªàV#Üê\x001c\x0016XÃ«¶¸\x0016Ä´KN\x0001*&C+a²Cz@¨C}\x0003\x0007§Á**C+më9 Ðî\x001e\x0010r\x000cÖ\x001f_×¦áê|ÑLe-éEfÛ$úR5>¨ìx¶~\x001a®"\x0007´\x0003'C\x001dI
öü¶&ifÄpÜ2
W±\x0003ZÙ¡¶@à9QHÈ£}µ lmG<Þþ4
W±\x0003ZÙÁ7\x0006\x000bìh\x0015¹·£Ô\x001cËÈÇ×¸b\x0007´²C­a]/ÒsÍäÖÔÃnòy´\x001fÐÊ\x000f¤Zý¸ìT6n¦Ë\x0017f»æá*~@#?\x0016\x000fyj\x001déÅº÷\x0003Ö"=­øÂ\x0013Î,Z¯(Â[)Â·¨[ä&©ßÐn9)\x001b÷\Lõ2\E\x0012ÞH\x0012Åµ`P9~â¶¢lqãU!Ó`\x0015Ex+ExjóJlÛÚé·¶4dÛ´æ$(ðVð2ÒE\x000fý¦³ÉUË<âc B·\x0004Ú6]$±év\x0005YÈDÌ»äÎ\x001b\x0005«\x0005\x001fùå\x001cé­ã\x0001ø1êy¬\x001e5\x000fW¿,YAláËùÁ¼}kiÅ ÷²ê.¶A1o°2o\x000c0È!\x0016fÞ\x0019\x0007Üc
Y¸Q\x001dh=\x000c
¥ÌqmîÝº>j&¾°z\x001a®`Ñ\x001aÁ¨7QÐ\x0006N\x001a«¯ù(,·Q\x001dÝh=º#ØÖiÛ\x000fB»:\x000e¬k2Æ¨Îm´Û\x0014\x000ce¡m
A2F¨Ç\x0002!ÓpUÀÖj\x001anÖÎDd¸IN\x0002\x001eÏSOÃMêÜ&ë¹ÍÉÑn®\x000eW\x001a×\x0018d^\x0012]^rLêà&ëÁ%6ÇIXD®\x0007×XDÆ\x0011aM¦ôs¾õìvÛaB¹7AÕä|Z\x001bq:¹ÉzrKã³Èh\x0013ð`Cm¬;à®É\x0016²"l%Òâ,kð§\x0014¹²S¯ãâ{¼ùh\x001a®r´lu´Ò@Éõ!\x00152t!\x001fº&\x001e\|³r´lu´vS\x0018pI\x0014@ÞbZûhÕ+H6¿`\x001c·"\x001dOû'±EÎYÅl\x000b-\x0008ä¦Ñ\x001b'æ¹æGug«©È¡¨¶<7Wëm\x0000µ¤ñÇ2³p\x000cÅ\x0018\x0019£^2!Ú·sÔGu\x0007ýü¦¨ÀP¡8éFFÚéé\x0018í\x0000\x000bÇÝÓ`UX(Æ°P\x001c
+ðI ±úÎ¿5ZLKÆÖÀU~V~Öàò1À ×É\x001aÇ\x0013H=îAÆª¬X\x000c°JQ2\x0017á 'IyY\x0013Àªr±ju±­Q³\pýMÆ»ã{Üý8
WùXµúXû'ã\x000eAÝ¥\x001d­´\x0005pòp[U«Am¹¢ 
cØ_V¦6¸\x0015ópU«!pøÜÃWj|!] PÒ\x0012'«ÊÉªÕÉZ2;F¨ýU¡Á
a%L¶Ó\x0017ì
6V?£º$«]%Ý
¬\x000e#ò;Pd [ÃèG#Þ\x001cF
Å\¶oÅwIA\x001dts\x0018ýhÄKe\x0012±oê\x0015DË#à=ÔÙÇ«{+Õ×Hî»²»\x0011_°º\ÀÁiK®ëàtÃ³ú÷Z\x001aå­)±zß8¿øvî,Þ'
mÖ¶M}a¶w<\x0010õI+RGÔMbhí\x0012+$+Ç!C_\x001a\0.Kú®P÷]¡µñª\x000eíî\x0012ûq(Q\x001e[f¾âE\x0004u+\x0013Z{
µµñÅÖ=·ÂèuÍõÒñ=^ (`uñ×Ú\x001dTH¶f({Æ®YÞÀ:/·´x,M<\x0005öI¿µá¦´´§íÚIÈâhÕ.\x000b¿¤xO{X¬V{ÛûxùFÃ[$|A¸o\x001e¯ö4k\x0017K©-ð&!MN6¼àdõçVg½\x0018´YBÚ\x0011­£e°\x0016Nx\x0001hÍôc®`a|Òfaí³¨í#a,»Ú\x0005\x0007\x0008ïèÃ[R\GÝ¸ÖÎÚ)-èdèp·ç\>»K\x001aHQ7\x0003 µ\x001b BÏ\x00146¼-)Û¦à\x001b^Ù5vñ±éôäêN\x0000´¶\x0002ÔmO\x0002\x0004V£\x0005|tdærÉ´ç`õ±µö\x0002Ôv)§iw\x0001ËÇÖ£l#yÄ»`·ôë\x0001vâÆ6bÏb/HÛòxÿU\x0019åßx-~ýåý_ßÿöû§\x0017Îl»\x000e>ñ±du²@{7D(\x0015ijÒPv=_c}Á¶íÃ?9µÖg¼\x001aH¸ê¡áÙn\x0003-
\x0010
Ï|\x001bmÐ9ùö³\x0011mËf¸;(·û0Ç¯\x000cNÐ^,ú¢}\x0012l9ÚÆvZ\x0003G[z%c´^\x0004Ö=\«KykÜmàZÄ¶\x001dÂTÈ²k®\x0005ÙÈû¡k\x0001V\x0008kÉØµÀð¹G\x001c÷\x000cõ
ÐPø¡\x001ew[tÀ5Ó<\x001e"nÿ_Y!ÿßéÉkyÂSÌ:XAW\x001ab\x0016s¼¾¶QMí·JÁ®7La¼¡Ò²<®\x0001y¤R<¡âs[ÛMÝJí8RtMÜ)ïÝ8ÕK+.<\x0005\x001dn¸a»"Ë¾vG*2`Y%©HqÅ\x0014êß?|zzªéWÿsb\x0017\x001dpãd\x00144óä\x0007ÄÑÃ´ÑÿþoOÓ¸ÿf\x001dd¬±iÔytì=é.U­ªÛ~Aªºßýüþ/} ûË÷ÿöÇ_>þre\x001c;\x0013ÿõõ3ÛÖ\x001cî\x000clÒî\x0011{÷Õë/û@ö¯¿ûñË·ßc\x000bbÜ#F3âùòÜ\x0010ó\x001bU¤t´
âÃUu&Ä~Ø\x00117ßëäíIê¼/¬Am\x0012â£tÃ8ì\x0011\x0007+bl=\x0003Ý\x0010o\x0012ò
q\x0011þ\x000c=&Äq8\x0011£,4õ¤Ø7ñÖP%¾e8\x0014\x00026!N{ÄÉ¸]øºêkC,\x0017¾Mc|¨pn\x0002÷³ù\x0018ÇôJð¢tN\x0006Xá°»Ï\x0004¸ì\x0001\x0017û\x0010©eôÍÍNZÐòñã\x0011âãËÀ­{¸ÕîtR«õ´&û\x0011CÚÑ±ä½Å¾êÆ\x001dÎØój\x000cßW\x0002xøO«N\x0004h¶3Ó]n'7ó!öÀì\HB5È«¢\x0004(¶\x0003;ÝUÇw¨ÍÆÜ\x0018F	éx]¤	±b;°Ó]I¯8£ðH{;àÁ\x001dþðp
±¯áÉ4V
JuëÛOÿõ?þÿÿt\x0005¯÷I^ã\x0003-ëJ\x0019Á!·Ð)?\x0013°úöÝ?½ùó»\x000bhwª
m\x000eF´9PCâ4¡bGë7r\x000eÇ%ÛY´E¡-V´eH°\x0005\x001a\x001f*\x001d-5Óv´åø)k\x0012-<Á\x0008-ì¥Áæà¢hþÒûf\x001fÝnp\x001d»ãLm\x001a®>
`>\x000b4ÿÚOnh9fì{.kä¬¼\x0015\x0017À-QÁ-Ñ\x00087JsDs4à¡¡°u÷ÃàOfáÖ¬àÖl)ðM?Ä«õWB_*uK>\x0013×º
\x0017«².ýø\x0019®:èFcÔ%2}±pL#/¡²ÒaãJÒ,Ü¤\x000e\x0003ýhKz³}X$$çxúÂWî\Ç\x0003&Ñø\x0013Mîw\x0007ü'D»k ´{ê)´4+ä\x0019-r\ ]ê,hkIá\x0006Zß£ýbÓ÷øò_?üýã/\x001bàï>½ÿøéã%	;ß\x0012õ\x001evS­[Ød8¡%«pdÞ/ÿùÍ×o¿Ù ÷îõÛwo¯@
r4Cvòh]#
èR¨ÁWFì\x000f¸-+ì\x0011S»
1æÈ
3´\x000bç¯pØIg\x000c\x000fí°eÙ¹Ê\x000bå¢C\x001ch£aÇì\x000f\x001b,\x001f3p\x001bf\x001a3¸yÜÖ\x0007tÈ5\x0008äpX\x0019µ@.Êý¶ðn+4\x0019b5UÃýð0é1 ÆÇôq÷¾`FL3Z\x001d1¶ÐÜJÈ+ÙÊÞ\x001fêtZ0?¦
7Ì4nhµr¥y
sÜ$Á7ÌÜkÙ0ÇCE>\x0003æü´'ÌÛ;
3ô¹\x0017ÂL"\}Î,¡\x000b\x001cç\x0012©5.ÁL\x000cºsÁ\x001c4 \x0005ÎÕíz1µ±ôìÐ.bì7ÙÇí¿kþ YµA×_üüþ\x001f>þúÇÏ\x001f.\ïÛ­{¼fÓ\x0002³^àH£h×²/¾zýÅ\x000fo¿ýñ«7\x0005a\x000f6
,æ¾HÂë\x0002r	¥E4·Ty\x0005ÖÝøVÃZ
k\x0000ÞüîZ»\x0004f
ãm*\x001eË4ÎÝMí4°5Á:~å¡\x001a/`Å²éäb\x001d,<ÞV	,ýhC[x|Ëcq±5´Òçs~y\x0005Ê\x0004Úº(¡}l¥ö°Ê\x00074Ã\x0002Ú*¥\x0017v¦Ñ&ÖxlÀP\x0017øØ¶6mûòµs\x0002,ªØ\x0005h\x000c^½«½6²z\INèÚ¹\x0002­W>\x0006Þèdô¾³åf\x0012ø.\x0005ÒÐJ\x0003cqÇúÓh³F±¶ò»¯'Q}æ\x0005\x001e»ü$Ì,ØÖû\x0006ö!ö>yjEÊÙ{(,·ÓN­\x000ct6*^rl\x0008Á\x001a\x0011@LNÄÓXJ_àdUÏ\x0004Ø¨ÏA4\x0003'\x000bÓ\x001bZY,ÔL+\x0005k|,é\x0007Ê@l[ïY¿¦Ù6\x000f´Çý<Óh£F\x001b-hS\x001dj;
lé+!K,A\x000e?\x001e/\x0006«!\x0019Á\x0017ïm×\x001b\x001c9Æöâ{fÑîT\x001f\x0008m.ÆcÜÖÐV\x0016º£cËñ«Ån\x0013h&²b%2ÿ}f¶\x00123C\x0014f mï\x0005`«\x0006[`Ûµ\x000cÙÇ\x0012òòB³Ò6\x001e¶çÑFk¼3P\x001c\x001f¸mSèÉ"Ê±
ÇzaÓhµU£µ\x001bNâ\x001d¿\x0015(\x0011ÛÖ%NV57T#7ÄûÚIð¬§Ñl+\x001aål_÷u´èTþÎI3%\x000bOH7-¹;¢\x001aª\x0018ú
ÑR=Ax¸Øq\x0017þe´íøÿ¤tÉ\x001föO¥|ñ]<ù\x001cØì¨é/´N\x0013¶\x0016k\x000fóÚ\x000cp8ì"O\x001e?~ñÝëïx÷y°\x000fÎ%°)À6+²\x0004OQ¤?|»òs]
ðPÙ}\x0016ìn¤Àn#Ý\x0016ÓåÐ=±Õie´!Ã¡\x001aß4Ø])e;\x0011h4mæ9\x000cOÒã\x000cÖ\x0015îZÏ\x000e3Åi´»w\B»ÇAÛ\ÌõHÚÝqãÖ³5´ó\x000cÓhõ©\x0005ë±õ2ÊMWð~w¤Gº,¶z¢Óh«>¶Õvl#Iá\x0002Û-\x0013Z?NÂakÀ<Ú¤Ñ&\x001bZ,üª¸­ßª\x001d,xñ±ì.9ÙqSaGNÙ~´!uÜÐâ·Ö·\x001eiå|ý
\x000fÃGÝzC\x000b`CKj\x0014\x0012¼ø)&\x0013\x0012­!\x001c6\x0014N£}ÌEoh±ØÐºÑ:]a1
¬%\x000eÛ\x001en\x001dFëU¬ÝÆ
h\x0003i¸w\x000f£¶Í­o¬¡ÍÜ¬¹Ý\x0001ÛN¨\x001eKØNð£!àë÷þöÇO\x001f¿ÔC\x0018}\x001d·òÄB\x001f-}¤g»F¿~ýîO?¾y÷ö³àÅ=^4ãÅ"Ö¥¼¶o¬\x0018Aâ±¨\x0005±ß#öfÄÍ¬/\x0006V_k¥[¨] 'b-Ã\x001ep0\x0003\x000e²¯]ËdÂÆäVvº7p
pÜ\x0003fÀ¹a~ªq""éa\Ñ15jN\x0001N{ÀÉîtI¦><¢n\x0002ÿüÌx<DhA÷³\x00191ÉYñ[zs4=	âu¢ì\x0011\x0017û)\x0006nmó#°
À§\x000b;§\x0000×=àj\x0005ÜRpî\x000fÙÞG\x001d\x001fã4\x001cñ´Oo\x0006ñã\x0006´q³6OÏwây¢ü/\x0012£ÍñV6Ðlg¦;ÒºC>\x0015¹·\x0019¹\x000e#\x001fËÈY +Â\x0003;ãå4jS-Éô¼\x0001`HE\x00158ÌÕL\x0015ãòHfG)|/Znc\x001dÕ´U\x0001\x0019\x0014åóHï«ì\x0015º
SCì¤JëéÒõ)ÈôÀÌz${\x0017\x0004²,ò¬¾\x000cÄ§«µ§\x0010+Ö\x0003;í5®<ÅD¯\x0010Or\x0002v9y:¬h\x000fÌ¼ÚEI\x000erå}Ö¯ËI>mõB¬h\x000fì¼W\x0003÷Ìn¥läìeV¬¸Ã©]\x0013dE|`g¾XF=;ï\x0005\x0018\x0015â\x0017&æ
Q\x0011\x001f/9Ñ&h¾d\x00178º\x001b¥C¨\x000fíÌ\x0017½Ôá±H7Y
Ntr9^/e¬¯zfæK®>­\x0014%½ðQgæãw@\x0013dÅ|hg¾\x000c£í¥ý\x0011x&ohä|Rv¬¨\x000fÍÔGrÅ[÷Ràn¸\x0012RmNÇBñ\x0016ÈúÐN}ï<C¦-'\x001fe\x001da.§c\x0017S\x0015÷¡û6¶æéRVRhT-\]]©Q\x0011\x001fÚ¯fÞ»Ý\x000erå¢\
)HÛa9|z5AVÌfæ#®.Xv\x0018\x0013Wö¸e·\x0011TÄvâ«c7¦WÅ\x001f,´n\¾ê-Ë+âóvâ~\x001c\x0010\x0007dWGo]åy^\x00117\x0013_n·¾¤¢¨®\x0014ÙåÓð®Jà¼b=og½v©æÎ#j¥Î|qPH8iJ¬_8Í¬\x0003«\x0008Í²Â\x0006>&Ñwr[ +ÖóvÖkA[¦0¹¡O\x0010`°ÞªÔÂ+ÒófÒË¹°6¬G@Ñ'Iê3.È^7^é[,=TdÍXE.SÜ_\x0004Wq7s^»hÈ1Z©½C\x001ei;\x001d¬8Ï9¯ÐÅ~¥\x0006º]÷»S;!ü8êñ2K\x000bdEzÞLz\x0005\x000bUA6È%ÉvÓB!-óXeå X/Y¯Ä(S
r/7È	9XÐ\x0015u\x0015dÅzÁÌz%Ty5þØ·ÂqÍt\x0013J_\x0005Y\x0011_0\x0013_KÚ¹\x0003asD½Ç.Åãè\x0016Ä÷÷J*¢EçÂó¹È"ÒÖ%ÉA×öÌ¼Wâ¨NÓìºãsD5F(WAVÄ\x0017ÌÄWJ·Y(2·W©\x0003K\x0002Æ:Èøø\x001aNÇ\x0007£eÌw2Vyé¤\x00051« +ò\x000bvò£;µ\x0004±Å9ëSZ÷\x0002\x001e\x0014ù\x00053ùU¼|ËÓDu×\x0013ª\x0019e{à\x000bC¨&Èüü\x000b»_»®\x000e+ËK\x0000­^Y\x00049*òvò«E\x001e\x000e\x0001¤\x0018Yöi¤ã\x0016Àú¢újË#ÇvGÆe\x001f\x0004qZÆÖQQ_4S_uNÞ¡¡çUÔ-£ìaU¼û¢ûªO¬L\x0005\x001cÎ£ZM©é*Äú¢ú*æWÀ¹2èõWÃ\x001cå¹%\x001d+0 ëÆ\x00163õU_©\x001eÒ<v~gib ÝÞU\x0015óE3óÕÄe\x0016¢R³\x0008¾S×Ö*Äø¢øªß&û±\x0008¯2
\x0019TMñx\x0011\x0005±â½hç=/\x0002TÞU&<Þ
Ó±¢©	²â½hæ½\x001adÓBdqì%Î#[×T\x0014ï%3ïÑ¢#~
p¥%ÍI¬,Îç\x000e»NM\x0015ó%;óå@\x0012Tý('i\x0015)0î©qÙKRÌìÌGÜ\x0001|£\­§Ã\x0004§ÊzS\x0015ó%;óå(oà\x001bð
\x0000R,\x0014\x001eYfeE}ÉN}¤\x0017ÀV.,J¿A\x0016+»Ãi\x0015\x0013dE}ÉN}	eÜ\x000e¸Ë·ý5Ä÷pÙólÒ-vâk\x0007¹«ËøFMBÕz\7ÈñUÀ\x0016ÈùùÚAìzÍØr&Äñ5H&Å{ÉÎ{©á-lâÑñTTFb^Ö?\x0014ï%+ïµÏï9ú)F¢À
2pø ¨\x001fÌAÎ÷²÷jàÍÀ~[+Ã\x0007ÙK
\x0017KZu³â½lå=r2\x0019gqu<)(;	\x0013,kÓÊ÷²÷àCv\x0012¥¾\x001e×¥öYñ^¶ó^Í<	ß"Ðà ë bu«êYÑ^¶Ó^\x001d=OÛÚ\x001eìåþ\x0014ÕL\x0015íe+ímGv_\x0006¢\x0012¥ \x0013Ë²ÞÙ¬/Û¯\x0005ÂG¹OÁu+Ë¦ö\x0018å¬§\x0019¬ÌWß4ÊúY.Ò \JNrW¥CYq_¶r\x001fµLËÜ¦kI'?j,ëcb\\x0017â\x0014÷e;÷µ+\x0008\x000f\x0013ðÌH©n\x001cå´Êûâ¾bå¾Òî»¢Aâ:]ð²VÇè\x0005¢¸¯Ø¹¯¹\x001c\x001fT\x001cpûâº&É¢¤X¤î\x0007;\x001fijð±¢YËî"E\x0005åb\x000fÊ©ÊË¡*O\x0001ÕC^Ö£6¨qË¶ÕËØ3â¥\x001d\x0015*PÂÑ{Fx »Ü\x001ep<C
%ëaÔö1úÇ\x0017_ýúûÇß~ûð÷\x000f¿üþÅ»\x000fÿý\x0002âP\x000c\x001fÆ\x0018¥\x001b\x0015d\x001d6©°¼È?~ñÕ·?¼ýþû7_¿ùæ/Þ½ù//[pã\x001e7ÞÀMË99\x00085#\x0008	VÒS^Ûïqû;¸ÑK_j\x0004'ïµ\x0018ä1£E\x0017½Ñ;ìq;¸#J\x0014J¡Oé×t\x001aaÇ=ìx\x0007v\x001a²bTy*±zL=	~\x0006Üi;ÝÁ]TC\x0005£\x001eDröþ.÷°ó\x001dØíÊÂ)H É\x00038\x001a\x0017zÒhÀ]ö¸Ë
ÜÛ\x0000]'uÚÌØ×
T?Ìí_®`\x001a`×=ìz\x00076VyÌ
~Kù±\x001cµÅ\x0017syÜ)ÖtÜ\x001dà!sëxðHÂÖ½«ÙWÂÊà
,ï°%õ
ósh\x0017\~\x000e(M\x001bõåÚ\x0001·"K¸Ã-¥\x001eÀ\x0000é\x0015we\x0007sâ^®\x0012\x001ap+²;lIrD¬£\x0014he1ª%9(¥.=à-á\x000e]f÷ù¨I®axf)ÛG­À\x0015_Â\x001dÂÌ-?á6mÅ¬"_V
5\x0000W	w\x00183ûÂëÃ¼§,û!\x0008ðô²*\x0001¸¢L¸Ã9zé9 Äw\x0006/Rî%¦GEq&Ü!ÍDVmp\x0006\x001eÇ#p	/¿[\x001bp+Ò;¬\x000bJåÈ2=·ç1dì_Á\x00075ñ\x000ek\x0016\x0007"ØçIÑ-^ý¶Áô6ñ\x000em\x0016\x0000ê&Ýdî4õh§º\x0015»ÚþJßïkãFoJj}\x0016\x0005JZFÇÕ\x000eLR¹k7Í%foÀõÕn'/?}¸Ø@\x0008\x000fÍ
çº2Yû!W~Öòøå»7§\x000f'\x0002\x0013÷0q\x001ef;ÌA\x0014Ü-eMpI ¯\x00138ý\x001e§·³9VQ ¯Òt\x001f^wV!¸3ìq\x0006=Û
ÇîbvþBª\x0014lÎÓ~â«0ã\x001ef´ªZ2Ê?nä\x0019dªê|ÛUi\x000f3Y¬\x001a6bÌR\x0017j\x0017*9ñTîã*Î¼Ç
æ¬°[\x0000F'k\x0018Û¶Ëé[éUe³XìëÇö^Í[ú.ö\x000c§MÂWqÖ=Îj±§\x001fs<ÛI
º\x00034çÓ\x0011á0w7iOÎbÏêx!T#ý"WèÅÈKó±xï,PMF\x00166jÌCS/Ý Ègk\x001eI\x000bå¿\x000b*:\x0002\x000b\x001fAË®d\x000eØõÎÆûÏlK¾
Tñ\x0011X\x0008©å\x001b\x0012è³©É2\x0002h>UÔº
SÑ\x0011Xø\x0008àÑÓ"S_öS\x001bÁ\x0001Ó~Î«@\x0015!ªh$¥ÂºíTL¸OeZ®¢T|\x0004\x0016Bv1©¬,»Dkû\x001fiÑ++Ò%P\x0004\x0006F*´Û'É\x0002­ÈýÝ%ÍdéT\x0001à*NEH`a$ðQtX %L[\x0004MtòG³¿[ñå\x0015#
-ráæ	J\x0013·¨\x0014\(£â$´p\x0012D/\x000f´q¦v\x000e)¬Ï´ö_\x0005ª8	
T¶\x0002õ!\x0004Ò¦êØJ:-Ó^\x0005ª¯H&NUd@\x0001yaZ¢IOS
K,ª8	
´UìQn\x001fC¢z7ÒåSÑÄ«@\x0015+¡\x001aeæ mÎ½ÒhTd46_\x0005ªX	
¬T¨;\x000bÜ\x0018\x0017º5ª\x001ayS8\x001di½
T\x0011\x0013©W©m:&uféSüLcóU ÐBLàÌ)¢+Rä«yì÷Ó¾¹«@\x00153¡*\x000eæÔ_V\x0013u×I\x0015WyTÌ\x0016f¢\x0014Oô;\x001cù?gxrYr§Ý[\x0017qzELÞBLÏK_jâ)àfÄ::&K]\x0010F½"&o!&Zó+Â\x0017¹×éR\x0013ä\x001cïdùÕu¼H\x0010Gf±7±$Ú\x000e/­ÉTçºS?ÝYh\x0006\x000cebvk³AAÑôry\x0002§b%oa%lÉ½t\x0006Çû!Ú¥V<>¦»°&*Vò\x0016V"¥\x0010V\x0002PûLo"¾\x0013\x0005ãu&³@\x0015+y\x000b+aï+èM±¿ã4\x0015}1¾\9\x0000ªXÉX)nåaI\x001d'$aè@Ä\x0015×\x0010¯XÉ[X	}\x0017Ñö\x001fá+íº$
71Î#\\x0005ªXÉX)T¡oÅí)ÞPñ§#\x0017\x0006\x0015í)Ú\x0017/r6®Ö^¤Ì)Ê\x0018
,f¼\x000eTû`
÷C\x0010«\x000c¶O?Fs#6Ã_\x0005ªâ}0ÅûêÇ\x0001½#gNcìr\x0005Ï\x0007]ª1ÅûX¸\x0008Û4\x0018T\x0016aG<Y2~\x001d¨÷Á\x0012ïÑy®ñ»ì?a$$¤±\x0000§¢Á\x0012Eqëj\x0004Ï1N\x0010MÝXNi®âT±)Xb\x0013b\x0006²ö×î)3\x0011}\x001dch~Á*6EKlBJC\x0018¨X4\x000cþL+rû¨\>Z\\x001ec\x0018%RºK\x0012Äâ#ê¢j*Øjû1ëåÏ\x00067\|\x001dJUi,ã=W9ø,\O\x0008è¼õ×?~oHÿ÷ÿøo~û·÷?üõ\x000bX]}×-¾»±(´Èf"¬Çý&ßþøCCûÅï¿{ýÕÛo¿ù<ZÜ£E#ZºÞ÷B\x0013fÌ¼A:Ë~Èå8\x0006ë÷`½Õ´)qq\x0004s\x000ccqp\x0016Y8ÿ@À4Ú°G\x001b¬¦\x0005Z©ÖÑz~l¶õR¼mÿKh_ia¨q\x000f5
<ÕÎlá\x000eÝfX#{Üü24í&+ÒZyi\x000bíúâq=:°\x001c	ð\x0005E§é#Pöh\x0019­¨ö´\x0003[¹½²d'
­-\x001d2ì,ZP\x0007\x0016¬'ÖåÂÍï37'\x0016ÑÂõÇ%çi¬ê\x001cù äÌE³[\x0015¬É]:±\x0005«\x0001XÏAû78Á"WK\x001e8;Þ\x00078\x000bwW"Np7(¬ß\x0005±Pg\x0018WNí\x000bK8¦Ñj\x0006³R£ý^lÜ\x0018ûÔ\x000fÅ.¶­¯Ç\x0017×i´ÊÇÐìcA\x0016´ã¦YÈ¡VÖÈ\x0004¼Ff\x001a­ò24{÷ô
´]¹p:ÞÐz\x0019*
Ç[7¦Ñ*7Cs¸¥AÝÌÂ[\x001dí\x00197¼ ½2\x000b×+7óf7Ê XI·'\x0008iÔÒC]c]¯òZoLl©c÷ñå¹yªÄ$ó0Ñ\x001f¿gLÃUaÁÃÂ\x0010ØÄZ6)ºÍºN:iâ±Xå4ZÙ\x001aSÛT«\x001aÆ&¢Ðm;&_b8\x0016ÂF«7\x00071'+A6QÖPß¬cEéi´*¹õÆì6ÀH<Ê³"%æ¯x¼ {\x001e®¹Þ\x001cs\x001dÊ8|\x000bã¬\x0007Ó¬;îæáø=n\x001anVpó
ë²qsåÍÁÍ¸øxìZ6zE\x0011ÞL\x0011¤o%
%zÃØ¸òÖ\xw/ò\x0004·\x0019
h\x001e¸?ve&µ\x0016À
"ùíÄDë\x001a¹¶]v+\x0008^Ðm«n0¿'4^(¢&îG¾Pe\x0005(½.«ß\x0013Ì\x000f
-\x001aÈ£]CÞÛJ»°K¡ûÎi¸*\x0005k\x001c£N¡àG++ß&Û­}(â\x001f\x0017\x0013§áª8\x0016q,S«\x0018w\x000e\x0001ÍtÛ\x0006L<îÇ\x0006«ÂX0_(i]\x0014k¨Ö4.^Ã(\x0015^\x00017ªL7Z3]HC¥\x0016#²U!©Dit;\x001e¥«ÂX´1(QNîcÏniÁ`¬;~n«2ÝhÍt©#Ú[ÒË¯w-Õ\x001d«I\x001bK¦áª¨\x001b­Q\x0017]\x0012)k\x000fQ(¸1\x001a\x0006Ç%ñi¸*êFkÔÅÇ¦3\{*T±î\x000bý¹ÓpUÔÖ¨KkS½¢\x0007Öò,5Èî\x0016X7©È¬Â\x0001÷ðøYû©T'½ºå\x0005Y¾i¸ÊÕÕÕ|H²-À\x0010Ät(\x000fyÕ\x001d\x000bbNÃUg7YÏ®'
3V¡?öm\x0007²N·â\x0017¬\x000eC¶\x001eF_C\x0008'\x0008\x001e6Gá°Õ²²n¶Z7ÄaÝØ×>\\x0002²½*·4uÉaÈ*2dkd\x0008\x0001hY.|+=S
îqoô$\ÐÏº`~×ý¿?BQUêþÎ¿©mw
'\x0005ªg§qÁ¤Ñç5äSÔá\x0006j@74ù\x001bß\-Ü\x0018ëYÃ\x001a®¡Öµ±(\x0012¡Ü*k(2ß4=,*\>hÀ\x001fì\x001dW)\73¢c©®5m\x0001å§ÿª\x0001ÿW+à@\x0011¸\x001fäøÏq6;ÒY÷¯\x001aï_o\x001b8÷\x0007?6°8?n\x00037\x0000þW
ø_­u«H\x001dB½nxX¾4\x00162[=^\x001f`\x0000ü7
øoV\x000b;ÎÕ°\x0004Ç|WhÔNê«.OC[\x0003f\x000fm¥H¡ãµ#-\x0013ÊaM
>øg\x0001Ùß ZÇ
¶¬Qò\x0010f¢g×Eã½>\x001cï­¼¬¯9ÈVÆ{	¥$¯r¿¿hÀ±æÈã-i^Hâ¼IÐHÞ-À. îÓ¢¦â\x001eÝ?¿ÿãÿ»ð¾^¨î*ËsE\x0005¼ø\x001cÇxË(Ú_½þñÿý<Æ°Ç\x0018æ1ÊvßvùìaÌÇ#ê,áE|q/Nãk7\x000bhAZ½Ð\x000f'Æ\x001aD?\x0005NÄ«.bL{i\x001ec®²ýÞøIÏÃcGòæêEy\x000f1ÌÈµè¥´
&ºÈîLê"Æ²ÇXæ16*áß\x0006ðûG#¬±¸ùåVÑË\x0018ë\x001ecÇH\x0015^yk\x001e7\x001bØáå\x001dÂW!>ÄR¶Q\x00067±1¼<ÙºÄ
$í[IZxykðe @Â<Hð¤é ú8ý\x001a«<ûãòØ\x0014H\x0015¿a>çÇx"ÒOä\x0018?Z¸Ñ+~\x001ecsg\x0011Æ	U^¼ql\x000bË'Û1.TA\x001cæ£xªN"$=Êvû\x0002CÌ#§3!Ù U\x0014ù0Nâ«,LB\x001e¸áíÛ\x0016 Þ\x0005©â8Ì\x0007òö=E\x0016¥]î¨\x001fm³dqC°iÁçV\x001c\x000c¼eë"àQYY¨Ý0\x001eÒlg\x0002\x00171ª@\x000eó¼±òÐOuAH\x001b¼¶çú²ØU¨B9\x001aB9µÍ\x0007¶¤¨ç·´2\x000eã«ü\x0014H\x0015ÊÑ\x0010Ê\x001f¹EÍãsC\x001e<é¼\x0008R§âP^Ì¡PäW'#J¾¬Òs\x0019£
åh\x0008ååæHÅKî\x0012@?²òòVÂË Õ}\x0001-\x0017\x0006/oÑ43Õ×u\x0017/{s¸£¢\x001b´\\x001aÜ¸4Mé¾_\x001adéçªÝenpn
l=Ä\x0001y>²±vÛ'~\x0017£b\x001b4\\x001bÂØctÓæ\x0004(åøÚýø£Ø\x0006çÙ¦ø!Îº\x0002!\x001fzQøòüóenÐpq \x0012i\x0019È#EËMô·éÆ«Hî
<GÙõÔnØr\x0003ón|î³¥'\x00171ª é
A²â`èèÃ÷@.Eý³õ=\x0017!ªðãçÃ\x000fU	\x001c³v@Öo!R^sxYKõz¶»³äw'û|stUî+gæ8\x0004.ò©ªùg°Bx*¢\x001bv"º_üü¿ÿÇÿ|ûË_ÿøí÷O\x001f?|\x001ek Y
jð\x001eº\x0016Gl1õr~¡p´~ñÕ\x0017o¿ùÇ\x001f¿ÿáÝÛ7\x0007ö\x00190íBîcïÁÓ^/\x0002\x001cZ6Ô\x0003S¦åGk\x0000W\x0005¸Þ@\x000cÓ¤à]äµG¡xÏñTNôNf CT~´b\x0006/\x000fîÁ£ã¹P+çvÍÌõåÑí)Ìå¬\x001bæÇvÖy;çÊ·öv2
ß5C\x0005~s§£±\x00042îÚQHoã±â{Þû\x0000¸\x001a\x0013(ÍïùJt´/´CÎ'bM
óñ°)Â\x0013=xjÚk\x001cööïÿöþ·ßúØù×¿þñá÷Kç$oÈ=\x0008rÀí g\x000f\x0003ìaNðöëï^ÿ}\x001f=ÿúÛ\x001fßüp¾S\x000fHÃ\x0013b´#U\x001a\x0003	ôeR-y)\x0012.Âáû§
³ßcövÌÅõ½\x0001saaÉLk\x0017ÅÌó6Èa\x000f9Ø!\x0007\x0006Ü\x0010vmÑ¢)f/\x0003\x001c÷£\x001dpv<Ú\x001c(³Ø0W'ñ-\x001dNoÙ0§=ædÇìK\x001f-	Ø²ó~Ilf¥t¨ÙlC÷ó\x001cù2òS(hG¹ÈÉðkilë\x001es½YFb\x0002"\x000b*\x0011fnÁÌ$_°
3è¸|#0Ó\x0006Î¹1_¿\x0008QÈ(w¼KÝYE9¸\x0011æÚå·ðyvU³\x000bÃá\x0016\x001aZ
¸\x00117\x0012o¡	P\x0003WN3f~sÏñxºÚY9!ÜðÂ\x0018X",Pç`âÀ.)ó\x001chÿt9«ß-gmÑû/þüñÃÇ\x001b¸?½ÿt!5"A#Yih]2ô3\x001dX\x00184»óÔèõ\x0017~ûæíWíüéõ»Ò#ÿtU¨ß­
5n!\x001a¥I3ùÄý5¤²«'Âú Ó\x001etº\x0003:Vn\x001eôÉEèÉ(LÔõ²2Û$è¼\x0007ïÄÓâ*£\x000c·çvxY\x0003i\x0012tÙ.w@'/µÏÔð{6tã³5\x0016s\x001f\x0005o¿ß³i\x0003=Ö\x0010&\x000f¯ rÓq\x001c=L Uð\x001bÑÆlå	¦Ñ\x000bïN$r\x0011?|¹Æ3	Ú+?ô7\x001c1mò½#æß{ö\x0015ùþê"N\x001cÏEj¯\ÑßðÅD#ú,Ü¸÷Ýd/Í\x0011
ø±ü\x0011¸rGÃ\x001fItV\x0014çiáY_*ekb pöb0;(\x000c·\²]Yúsm%\x0011eÉX¦¬$¾,W7Û+Üþ½Ø;µ4»rn\x001dx\x000b^\x0006ÿò~M\x0003pEëá\x0016¯çm9åÆ6-ÁÎBU\x0016j7òãvN#påá\x0016M¶¯0ðv\x0003ãàMãè\x000c|&\x000e~\x0016wU¸ëÍøÍÃÝí" Öæ\x0017\x0010t'ûÝ¦Q?¦d·ì\x000fn¡®\x0003uÙ\x0004û=ûZz\x000b\x0003JT\x0019o8f$1.\x001aåiA¨rÄp"Ô9[§Û÷ü²Ò\x001a¸
7:^D¶Öu¸[Æ[Æ\x0006~ó:ÐL/ØÂ'bÈÓÀ:áéÖ	÷YÊpµ!$PL>¬K¬Kå\x0010þÐK5\x0005C¹\x0008SÚÊë¯Z0dm´\x000cñd\x001dÊu«;\x0000ýè¾½ó<di_ÿñó/W.îT=¤Bçvºéµ¡\x001b»%VÂóç{f^ÿøÕ7gWvÁ{hÁ	g£|u¬óÛp\\x0011üË

\x00130ý\x001e¦·ÀtþUä´Éqg~/p2ÊÓ\x001d3Wa=Ì`Ô§ÍÖlåçTYÓÒ¥3Õä«8ã\x001eg´à,UNgu,O8QN§?]s\x0015gÚãL\x0016¹°üøöfÐßh¬óT&ý*Ì¼M0=	OKR/]æßhx}\x0017=ÎbúìC2ªFÇ\x001aL9\x0015©fû|º,ö*ÎºÇY-8c6OÚoËOµ$Ë'ö<Õñ¿s7X@AÞ\x0019Ïgf{Fn>¦Â/Ã,'þë05\x0017YÈ»n6(;©è$aéäð:NÅE`!#ò#Öe¤â¯çóYp¼\x0019ôåI	 ÀBGYr×ê°fÆfÐ\x0005~\x0004ÀÄGÜâ[I}¯'ØI\x0016¶4/Ï8M Td\x0004&6jTYÄ0\x0018\x0001¶L=!\x000bp*2\x0002\x0013\x001bµO]Ý=½âôÎ#:ôh¶\x0002§b#°Ð\x0011ôÁ@Iô{ßt¦O/aþt§íU ÀÄGàYAxó÷>éLü}\x0001LÅF`¡#HE$%*ÉËw¢(ÑPnb¼\x0013\x0015\x001b¡Èø|¶HZù»×AuEVÐÂG´óªAG\x001e\x0012åÉÂôõOàÔw#\x0013\x001fA\x0010¤Jm¶
Zør\x0014`E\x0004EÅGhá#ãÉ­¦ÄísÍ  ¡éd*x\x0002¨"$4\x0011\x0012-½\x0011fj®î\7\x0003º\x0005\x001d*NB\x000b'ÑJhäÔ.Ã+Ç~d"uÉW&N\x001bÎ\x001cÝù"\x0017xF¯ÙÓ¯MÐÄI)Êt\x0007Ù\x001f³£êz3è«\x001c*NB\x0013'ÑúâÀ\x0016\x001dÉH
aXôt\x0015ãU ÐtIjèØå\x001f]p$E9ý\x0002^±7±\x0012z^d\x001cÚ_{äÊ\x0007\x0014r\x0008§ËB¯\x0002U¬äM·$WY÷Ã\x0012´lD|¾Eû\x0005Y½W´äM´;Æ¯RK\x0000\x0012Cã[¼×ov¦[RKïzGs¥ú*sâT%\x000f
þ¤¶|\x001d¨b%ob%\x001a4d\x000feÜe"¤Òæu¼í¢äÃcîâ$Ûø'­©8É8©å¡½\x000bj%#«^W¤w^q7=ÛµCéù³Ós\x0003Ð:\x001c)\x000cJ\\x0007ª8É8©Q;0ËçQ¹Åq¬\x000få¤\x0014|\x001d¨â$oã$GCýÓ'©Ò4 Y®ÈC"¥`!%ê\x0000íe@\x0002ä\x001c²\x000coº¢<\x0013\x0014)\x0005ÓU©dnZ%Y*9¢id#u\x0005'\x0005ÅIÁÂIÐ4ÇúRyn®\x0001eù\x001cÝI_Ëu éªÔ\x0012ÑÄA´Áò^&¢{Yh\x0002¨.%YHÔ+\x0013ûR¡í\x0006TnóÑ\x001d+ÞN\x0002U¬\x0014LW¥ >=7Gè\x0014_\x0010ó\x0004ªx)Xx	èí»0PÑØ!=$Îôòlç\x0004PELÁtYj)3Oðmê Ê{}XaOEKÁBKÔ-88Õ"}ÃåOº¼¯ãT¬\x0014Lïw|úÁJ\¦	I\¾±Òw±¨X)ZX©Ý^Eqyé1\x000eÁÐ´àxFÅIÑÂI\x0014"ûQµ>
§¸Q^áïQqR´p\x0012Å÷(ç\x0013$_\x000e^Û¢[ñÀ\x001c\x0015'E\x000b'Ò²DÐ0^Å\x0002V±è
HT\x0014-´í,å9\x0015yÅ	ÑDôX7u\x0012¨îo°p\x0012)Ò\x0016vy_hm\x0003º»#¯(yFÅIÑÂI\x001cð\x0019k?£#cÎ°âÓ«`\x001fMÁ>!?¶3t\{ÛÌô³~½Ë@
¢É\x0014DgE°@9eö£É!äÓàWªðLáihPn÷déïÍòñVåI ÊëÉë}\x001cï81VûÃ¢+Þqî\x001629¯Ü£\x001e\x001c\x0019wi¾
aE;FR®L®ò\x0016\x001e\x001c\x0004y ñIºÙ^X¶03+OÊ&OrbKà¢§÷#¶£°\x0000¤ò¢lò"¯2\x001fNÈ´'³\x0003E\x0001êWôeåEÙäE¬\x001d\x0015ZV+}ÚAÞBñxoò$LåCÙäC(\x000bÔ·
\x001dòáY\x000e'¬¨+dåEÙäE>P~ÿðiôg\x0018^ô²ÌÕu E¹Q1¹\x00111'\x001a\x0010§\x0004O\2\x0015åHÅäHÜÔNò
\\x000f8êÇ·®\x0008]lx72ÔUý\x000f¿þñóÿé¯³cÑ¹äq£«È²ÃÙ%\x0018O\x000eþèþÃ·?~õæÏ¯ßýãåiî'ºç\x001boà&;~\x001f\x0005Z<Û£*È\x0003~Ã#kí÷°ý\x001dØnKO\x00046÷cº,}:q=îp\x00077VVÝ\x0000¨¯BÏ­\x0001$æF<ü²Â{ØñÖ)5ð\x0001\x0006õº*÷ëï*VØi\x000f;Ý\x001db\x0008-áá*\x001aÐ\x0004\x0001ã>d\x000e+î¼Ço\x0012Q¾
@ÂÇÄÖpÞZq=îr\x0007w¬¬ÏÜp'éN(A;AðÑ¶\x0005Aw\x0003xm)\x0017ÄÃ\x001cµJËáþ +n\x001d¼ïDï
ÐGwCûOÉ<Ü\x0013\x001cêúÎâö®h²ôtd\x001eþî×?þöá·ÿçO¿~úÛµcR
7UØpro\x0018Èú£\á4÷íjÿçOß¾ûÓ\x0015Ô¸GvÔÕUò¡Õ,! #\x0015ùlt\x001aµß£öwl])~l¶n¡$g¶5ØæJí½ËP=êpÃÖ-+IyïUVÆÁÅÖ'\x0013ÒÓ¨ã\x001eu¼gk\x000e±E\x0011>\x0001YCiSè:Ôi:Ý°5fÞó°I`f>×õE­êÙPç=ê|ÃÖ-É\x0018Ò.Ù\.*Ãº¥Þµ&Q=êrÃÖ~«%\x0016ÂäÈ÷PôÉîth\x0012uÝ£®wlX<)DWX-\x0016©È¹Î§ýrs¨wZ3dvwÃØ´*K
ôTÌJa\x0018ûìc\x0012¶&Ç;ìXc_Í\x0010BåÍØÒ_QÒiÛÂ$jEp\x001dcæVÅÍØCËLê0-{={B­Ø\x0011îÐ#\x0015\x000e;Ñ\x0004\x0012Ê\x000clmQ¦-'\x001aJÓ¨\x0015ÏÀ\x001d¢\x0019{PBÈ \x000fMÍ!\x0005õiÛÝ$j\x0015±áVÈNü\x0017BBªo¨\x0013¿\x0016ÿòÒyØ*øÁèW©s\x0011\x0012Râ=4­óÂ\x0004
U\x0014Á\x001bQfÒÔio\x001eÉj:ÿD­Ü\x0011o¸cu(eçv\x0018ä\x0015
Ôs<­?M¢Vî7Ü±:Ï\x0011ÛÓ>{¾9ñÆ\x001cN;÷&Q+wÄ\x001bîXIÈCN\x0015QtqÎ2ÌÃVîwÜÚ¡ÙÚá! 7\x001eZ\x001bç¬¼)Õí*ö\x0010
±Ü\x0010d^s»ùº^r\x0001ÚÚÀ7ß·§ÐãMè@ÛúE\x0012\x001fÐÓ¸ÜÔu¾éòSðù&ømø°g°Qä\x0010`(­|ÚO?w?\x0005_o\x000f"m\x001bêÐr"¬%6
]\x0005_>òÔíç»ßÿë6~ÿøÛ¥w©L\x001d\x000f½ì¥ä±~9ÈÎpü öÝW¯¿äúÍ»\x001fÞ~þ(U>Ôí¡ÄWF¬.ñ¼é'Éêp\x001c
-pã\x001en´Âõ.â\x0006·\x0006î|)T(c¼Çc,\x0016¼y7ñJ[fÃ[e#L;¶Ið\x001eòº\x0005oÝã­f¼*a¸=1ÜP\x0004n9ª=\x001aàö6³»y`ZixË+'e¿m8^gc\x0001¬Ü
ÌþÖ\x0000;60 /i¹ìH×E\x0007\x0002ÃÙãPT\x001bàüÊ±Ça\x0013|¸ÏÚW9\x001c\x0018=.8Y`\x00037¶î÷ÚBµ\x0018Æ\x000e;,ÇÙåPV\x000bc»|á\x0018ª\x0018ø°=Ò\x0000\x0018Ï¡Ùç\x0010û\x0018L3°Õ\x0017Hµ$T"ð±Êµ\x0005®ò84{\x001c:\x001esGRÝ\x0013F\x0006|l\x0017E\x0008T\x000eFKµF\x001e0Û\x000epì\x0011Ë8\x000f÷\x000f0ø'ëlÀûç= úõÃÏïùëµ½	 
©>ø¡{9îÜxøÞ¨«qúöÍW¯¿ùÇ\x000b°q\x000fûY\x0011ñ:lÖdIîà[l\x0013Áe,£\x0000p8bÅí÷¸õLáN27åC\x001c\x0002>ÈMÐ\x001f¾ÌXq=îg= 3¸¡ÿõ§Ò"bó^v_fÒÿ];îq?k\x0002ÁíelË×@Ö\x0011ø$jCÙ\x001fÊZq§=îg] 3¸[r_äÅ ðö±¼]¶å,÷°5ÌÀa,zËytWÎBsNÃ7VÜeûY\x0013È\x000cî"ÚDÛ{iù,á$\x001fÊ\x0016[q×=îz\x0007wÎâ"¹+Rºvs9Ì¡°\x001fU®tõ®Ìà¦*\x0011W^Æåº¡\x0007p·\x0012¸fË\x001bt¹Í\x0018ñ\x0001\x000f\x0000RÂ
(åòæ ï*»\x000e\ñ%Ü"Ì*ë ÇÀn &y¶øáýÐ
\\x0011&ÜbÌô<½\x0001\x0008\Ñç´Ð/AÑ%ÜâK*òû\x0017@\x0018<æº.AÑ%ÜâË2ÄFÕð4H%-
îB÷áuà/á\x0016aÖ$\x0003\x000c\x0001vW»G\x0001~X\x0015µ\x0002W	·(^JÙ1©¤Á\x0006\x0017¹\x0002\x001c+nÅp2i¬kþ~l\\x000bÂôei\x001cT	·\x0018³d®1\x0006Ú5ÃCÌ²\x001f½\x0011æá\x0015Í\x001b\x0015c>ïöÀ
´¥¸·×Èrå+Ä0¯¨\x0018\x0013ï1fi²\x0010³t´´l|TÐWæ(¨ow\x0018\x0013ZBÅóÙ!4µèÏKÿVà1ñ\x001eczrÇ\x000e<É !m^NÉ\x0015*ÒÄ[¤ÙBa6¢,zêÔá'E£ÃáX+pÅx5Q®\x000fä(\x0012ÄÅÙ¬À\x0015kâ-ÖLUz\x0017b»áW\x0019ð\x0016
Ñ\x0014\x001e½i[+ÖÄ[¬l¯
j%L\x0017ài©s*þÁ[ü\x0013½¤Åmñ|¿ Ë{[Yz±÷*û[a<DY¡\x0019©® óà2½\êÊ\x0014¯\x001fÜnECDé\x0001Dõ«ÑOfò¾éUPñ·Kû\x0003öM?v³U8Ô[±\x0002W¾éoøf¬µÈ`J\x000cYZo=Ê\x0019¯à\x0017^~¼òMÃ7c-²K)Ä8$÷ü\x0008*ín¿ð\x000e\x0011s{øN$ZbÒ\x000eïhk×\x000b#5×q+ß\x000c7|s[*çØ7c±Ç\x000eò+£aP¾\x0019nøæ¶ÆTx¬ÒXãy¶\x0001_b\x0005åáoÆG\x0018§U¬lñ$b>õ¸\x0013Í
\ùf¸å\x0001ÇLPÊ¯¤/^®É@\x0017Þ7£rÍxË5[\x0014|Rr¤Po´ÌY\x001fÊÞÏ\x0002o·q]\x0017l¿x^\x0017üò×OÿõÓû_®\x0000OuHê`3x¿ß§ê¥ýjB\x0005þå·ï¾þöÝëo. Ç=òg÷¶)ä\x0011å\x001aÑ2p\x001eiJ¥JïY*\x0017&#'û=ògáp
y	rÈB£Ø\$M\x0012)V.D\x001eöÈÝÜ¦·ë>ÎËa)	d}=\x001c\x00001\x0003{àÏ\x0002ù\x0014ðìÄ?±±h÷ÏvöesoÊZ«fäiüÙÕm
9D»Ús÷I;A2¸Ü.ËÏ\x000f'ç=òg\x001c4< ½7§ns'w×:hÙ#öæ9¼eZÜd×l¸i-\x0015|µÍë\x001eù3ú
>±Íe¦¶\x0005E7l~ØMlE¾Û
VóA­pÊè%ñªPªCp\x001bP*¤Ö"ÁåóÜ?\x0001]sè=\x0012õ(¢\x0008DE]\ ÅEÙwH5u!tE¢ÏëSVOUt(°f.¨¤\JZ\èóá\x001c\x0017Éþ³<²Â@*1Ã>73tÅ¢Ï«SF\x000fEÊ´e0u/}hè§+ÏC\x0013Ð\x0015>/\x001cNYÝÉº¬\x0006=±X*C·¤ý->%®ôyépÊê(5!Lå¥e
\x001dåÂ++"}^;å#ÍÆR(ëí|ÃèåóU¡	èI\x000f§ »Bñp\x001eÊ8ê#I?\x00194#WLú¼8ÇGYz@ÈèdûR3úÊd\x0017\x0015>/"Î@\x000fT%ç î=×´Rª²Ìf\x001dVBWTú¼8eõ%\x000bÀê$õÊuä/[&ÌÈõuô\x0016ÒH<×*\x0010@4"GÝ-uRTTú¼8ç¤^Æ¸hm#r\x0012àÂ8/û¦ÌÐ\x0015>¯%ÎY\x001däÝ\x001fj]ËxE¶úxç\x0019º¢ÒçÕÄ9èÔ\x0007ÒÏKåú-uK|µFWLú¼8<H#äÊæ
ºÌçÆ+}O\x0013Ð\x0015>/(ÎBç«\x001dm´éþ
ºtömÊ\x000b¡+*Å{T
E\x0004úôl¥²ç %ÄK®¨ôy1tÎèEfi;O`\x00179.uéqñIý½K©O\x000f¹»Ì
Ú)\x000fuÁ°ôÁË+"}^Èéì¢4+\x0011],\x000e+¹È+\x001aõ÷.¤»\x0011Y¼W \x0013éÅ
¯¼\x001byý¬{F  w+4£K\x0006\x0010ËÒ\x0017\x000c¯hÔß»ÆÌ:\x0011¤\x0019ùØ%\x001eÃÚó¢Xôyù|.M\x001fë H2ñÝÈÉôÒG\x0000¯HÔß»R¹EB\x000bpb»TtU\x000b=+3\x0017¯HôyåÎæQ.h]Là÷.'ë4#,%Q¯HÔß#Ñ<¤\x0012ÁmÔ;ô\x0011\x0019÷ð¡+\x0016}Þ¶0÷
0Zä	zf«C>_!d\x001e\x0014o»Í2]\x0016¥áÆ±YæB£â\x0004nE¢Ï\x001b.æ/nìH 	JîëØ(·âÑp¯<J\x0005:VýÎE\x0012ÝòØ²ÔæE7Ì½ëfÑâ¢Å4½Ë"þ¿öÝ%èêè½ò(\x000cõXÚ\x0015¹>\x001aÆj¢¼ôÝ%(\x001a}Þé2W¬{¬¥\x001e@®I»(ËÚyZ	]\x0011i¸W!Å:ÖS¶4f\x001c\x0018ÿX±µ\x0012¹âÑç]:s\x0000I\x001a£H$qUÚË»\x000bÉ\x0019­®x4ÜâÑ\x0014\x001eG=xjÞ^Då>Ä²2\x0005\x0008G·\x0018Í@ÏD.õô\x00199z\x0001u¦ñp\x0015zT<\x001aoñhJ(ÕJöRi·\x0016CÇVâ=>ztÄJb«£T\x001aÃ±\x0014\x0019º
ëñVXÏm±¶X\x0013ú\x0015£FY5\x0018ÂÒ7Æ¨bc¼\x0015\x001b3ià°:W\x0002êÃèK¹4ª\x0000\x0013o\x0005Üu\x0013Flì½nlq\x0017ôú¯#OÊIÓ-'Í	\x001e¡1Êb;9cCú\x0015	\x0013Ð¦[Ns×tZVÉ\x0000[ô\x001d¹[y^rÒtÏI\x001få\x0017G£½\x0003³erÔË\x0005M	èºÃë\x00167\x0006¢h6Wº"íF¡®©\x0004@ØÖ\x001fíTeè®ôÐ»üç÷üþ[ûÓ\x0017ÿôó¯ÿýÓû¿|\x001eº,\x0014jÐcû\x0004Ü\x000eÐnE¼\x000e¤Twºí_ÿøÃ÷íO_üÓWßþw¯¿ü<vÜcÇ[Ø¡]îú8WKÜ·I¶£Î²¥\x001c\x0001Ø¡û=tÏì\x0011ús\x001dÅ\x0015¾"UõRÏâÍC\x000f{èáÕ\x0003P¯îfõB-ÜQÊéfÌyèq\x000f=Þ³:uÔÕnö8ÖÐ¡\x0003V6{>\x001c\x0007°cO{ìéæa\x0017R¢¥NüxDÍ^ãé¾Çyìe½Ü<2¤7ìÑóêìvd¢Ø½îÎÆ¾S@¡\x0000énÇ<ö}!4cD½ö
|tt=âCsª>?\x000f^EH¸\x0017"Dv_­{£\x0013mÚRýé\x000eøyì*DÂ½\x0018´ÕO|£¦nw\x0010«×ÃL;r\x0015!á^¤Âtdb¢ö\x001d¶º\x0013^:.#Ù±«\x0010	÷b$¶^ù¸»LÊµÙ!IB\x0010\x000eÀìà³\x0002o\x001e\x0019\x001eohÉ\x000c\x00133éTEz\x001eyUÈë=äYÚ`bÌ\x0005Ð\x001aö"àýaG©\x0019<ª\x001c\x0012ï%\x0018¤$6ÃS§@?3\x001ce
®1Ç®¢\x000cÞ2¡ð,O/è\x0015ÆÎ#
üZÃ\x001fç3¿ð¶ü\x001d|á%:ÔÚÀ¥\x0008nð+n£1ädOÿ\x000eñî_Á
!rùåY|zû+ÔÛO\x001f/Üø\x0007ÏM\x000e#\x000f$ADI\x001eùe¸oß½=½åÅ§7¥¸¿)]²Y	3bõ¢eÜ¢Êå°%`\x000e£ßcôÓ\x0018Û¿À-º©®\x001d#+ 4î<Ô\x0018ö\x0010Ã¼\x0019£ãâD3céo
bIUÌÏòîk\x0018ã\x001ecÇH{\x0007:Ä\x001aÉ6CñÚ/	¹\x00061í!&\x0019=+ bö\x0004º72B°\x001eLÎaÌ{Ù`FjmKkðÞ_¥àbNûýénõk\x0010Ë\x001eb185Ú}\x000eØK\x001fäÔ(V<lÄX÷\x0010ë¼OçØ»\x001c±`\x0010P¹\x0013)ùìoûËþ~\x0017Õýîrø®¢XM½Èf\x0014\x0015º\x0016¾ïjÐ\x00143Ï1
\x0004GZí\x001c\x0013[Ò\x000fKÞöjP\x001c\x0003\x0006	"¾Õ\x00028t)ífÈ\x001c\x0005ãù¢k \x0015Éej 6ÄÍE\x001aH\x0018 ëéÓÉ5fÀÀ3
Jà#I\x0017\x0000>ÜETx\x001f£¢\x0019ç\x0019u+ìÛíkoïÜD× «\x0015àtÕÍ5hÀÀ4ðÈ)h?ø6ÏZ¥ÓÕk\x0010\x0015ÏÀ<Ñ 5k²g§..Õ\x001c;U1£;ÜP1Q\x0011
\x0018\x0006\x001c+[#78{ôI¬\x0018\x0017|jÅ4` \x0008\×mvL¯RaCâ8\x0000S Qq
\x001a¸Æ{B&ig§IÂÙÍ¤·O$*®A\x000b×8Ö»Çv[ì[%K\x001c[t\x000eµ æ@ê\x000blhÃ-ó¡§ýrÝE\x000c\x000fç'æ0ª00ÞRq¾.\x0010i'ö\x001bä\x0017W"íÛ¾*D¢!DÒRÁÄ\x0008ãNèÃA·9*þ !þx\x000bCÙÝ°¬ÍrS\x0018½rmoqíÀí_-þp]csmY|â\x000e{¨æ@*¯ñ\x0006¯q\x0005\x0002èÒÚ¥¤(Ó§k Ûøy·i\x0017\x0017ÞxShðB\x000e¤\\x001a\x0002Æ³\x0017ók\x0018×x×Ðu¿6
¡ñr"ýi\x0011ë\x001aFå5Þr?Lò±i[dhc7ÞaÓð\x0014Ä &\x0018\x0006ÇJ\x0005×\x0015N(?+BÚÇÝ{s Óy§iy÷p\x001aÚPÎW¯$\x0018}¶\x001b2`øIM¢\x0006*²´lêËýð÷¿Ð»é×ïÿøôë/Ç\x0019=	gl!ËÒw×#-Ff8Âùå?¿ùúí7ô^úõë\x001fß}ûÍg±>e\x0008+5ËX°¦Èó2\x0006Ãúb¶\x0014Á	Øc)g`ßúË{	iÁ=RâZUåé4o\x0003\x000f(V-Ô\x001d|gÍ
Ü2l3¡
þa×±2ä=\x0019,\x001c^ÁgÁbR`éG\x0013XÙ
Ý´ÔoÔ±¦ì;X8îO\x0005\x0002K?Ú,¹§>Qù¼·&4ª%àÑ\x0015h\x001e+j¬¶3\x001bãÕÂWd5W*&
Z¸Xa\x0016m~<t\x0010ZúÑäaÁ3	H'7û%êêhs<\z86\x0015º\x001d,hûþÖDZ(Üã\x001f\x00127\x000f×\x000fûf¡RÎ½\Å\x0008\x0015GXIK&û¶Þìöx¿Æ,ÚêÑ&´c¹h¢ì]I>ÌÛ\x0012j\x0012Óh½:´ô£\x0005-©Tõ~ÃÔòÑa[dÁ\x001aBY¶h´ÆÐ.'¾Û\x000bxÀ#d9	!\x001d\x001aL£*|Ñ&´Ô×ÁVxä1Ü-^Cq\x000bLÛèQ3.ýlB\x001bE?!z.UnjÃ»À4Ü\x001a4Üj¶7Ì¦\x000cÈàé6û¸Á¥G¨\x0005p\x0001ÕÁÝ~¶&}r µm$4ÀZ¼ÕãaÉu\x001an\x001an°åà±Y×uG°-	ê\x0012\x0013B\x0010>Ô\x0015pÑ=Í\x0016g·$\x001aÆ ¸4WÊ"\x0007Q6\x0002UÚª¾\x0002îcâ«Ã¥«§%¯õ·\x0015\x0001¥«¦$Ïò\x0000¤à}/Spå©$sÉÒ\x0011òå¿¾'$ÿòéãû_þúy°íê\x001ahX"ÊY\x001aqB\x0012]\x001dÀCG£{#ÿù\x001fÞ½}ýÍ?~\x001e-îÑ¢\x0011-I£
ÚØÏé4ó\x001b[C{¨©k@ë÷h½\x0011-½þÆ¶ß\x001a;Zê\x001bèh]^6ìÑ\x0006+ÚÀË}\x001aZÏ{ â\x0008¹
í=qhã\x001em4¢\x000c5D\x001a¥ã³]_lµöP\x0015ªç\x0017\x000f*Óó¬
¡e\x0015%WV\x00196ïÑf#Úâ{ZCóWM\x001bEò	àPÆß\x0000¶ìÁ\x0016#Ø,Ëz|ÌKÛÑ\x0010
|\x000eÌ¶îÑV#Ú'"£M¶\x0007oh\x000c]µôc
ÚFrÉ£Ûd\x0016nr,\x0016çc_¸¡-ÃÉ\x000eï»\x0006°Æ¬<Ö²q|\x001cÈÇV\x0006.;\x0008 h\x000c<cÉIOþÖW×Å$âªîÅúÆ$XÅb`¤±D\x0005ÂnÚG{},²»Æ¥\x0017§I&Ñ*\x0016\x0003#Q^Ð·Gz\x0012Þá^ÃÄ¶é¥ræ$\Ec`ä±Djo\x001co1HP\x0016Õ¸Öä\x0008 ¨\x000c\¶
rqLp,Ù\x0011³\x0008_¹E´\x000bÈÀÈd¤\x0017Q9& ãÕ\x0011qht¸|ø\x0018j@«\x000cTIF_ÐV\x001eRíëç%,«¨\x000c\Fâ-\x0012Á\x001a­¥Ô¤GÀ
/ö#ÎÁEÅehä²\\x001c¯´ &«Þ-B:nãäæºÆº¨Ø\x000clF\x001a
]\x0004v½Ê|\x0018<Ï§dÄC\x0019\x0003\Å\x0010hd\x0008á\x000f\x001cÄRæí2q((\x0003,J\x0015P\4Ü
-ðíÁÉìOC+!÷xÓº\x0001®
ch\x000cc¥R²§->]D>Ö±8\x001b\x0017TYrÜ~ÿðIç¹ô\x000bSx"éX@ÉobÍBÂ/ÎµÍÆ²§Á9§ÂUIú¬¹Òn\x0018¢GÕþó«"ð~\x0018QË4Ò4jçïÑ¢Õ~aËND×\x001aÍ­É|Ñ?µuû\x000fm3\x000b\x000bzRééB\x0008äò4/6]D
\x0010t£¥ûÉ»7ÿö±AûýÃ¹$Z¹\x0005\x000c<ëUã~Óñû®tW¼ùîmû'?¼9k\x0003ép\x001fÊM\x00047:#ÜZx××:VÏiÞú`Íi5'\x001bÖBå¿¯×¯#Ã
\x0012*;íÇ¿\x000e·*ÓV£i\x000b]úA\x0000äò\x001fÍ\x0014F?Uð¸\x0016vc7°}¬pñ!÷\x00169hAv¤ã
$óxwúwßª?ëhþ¡66\x001cí¡6vÚÆt\x001dï®µw»w¢ÕÓÆ^½æ»ÜwS¼7åNçX'ð&×èmMæbíÖ
¯äÁ!³&ùëx½Æë­xÜæ[\x001cpó0Ä¡^LÛ'áf
7\x001báfif\x000c.T.ý\x0014ïÎ_Z7èð\x0010á¡]/y\x0018ª\x001d\x0007d\x001dËå!¾uÖú}\x001dnÔ§!ZOC;\x0002yèËæÀheýs¨ÊÛ\x0006¸ú4Dëi\x001bÂ7YYÏpEV>Ó¹Âëp¬pÃØ³ÕF~C-b\x0011¼\x000eoÑ±·Xco\x001ckÌ]»#E>\x000e9\x000f¹áÓÑÒËxÑ)¼ô£Ý¾"aºÆ
W4©ñ°ad\x001e.ªD\x0007ÑD\x0006i)
@el;öP\x001c!N£%5¨\x001dZúñ?iÞBÎª{»·Ôôõ¿ø\x0000ÿñÅïÿøí·\x000f\x0017n?H¢ÍýÎV\x0007þbt%ì²÷bö¯ÿüæ\x001bÂûã\x0017_¾þñûïß|\x001e«ßcõ&¬ð8\x0006®]\x0013cu#ãÍãóXó\x001ek¶au0\x0004d×2¨Þ.\x001eÂQ@Z÷P«	ª\x000bc¿\x001e´ÛZÕ
%}\x0006õp	ö4VÐÇÕv^[¾ñJvuyÎ\x0012\x001a{=v»\x001dÎ?LcÝ=õÒ+³`õ©dÆJïÒ>G\x000cA&ÅZ¾~øZö\x000cëqË>\x0003ÍEÕb\x0002]V±YÕ3Ò\x00109yAp
é.
ß@S\x001aná\x0015¯S \x000e\x001cd¨lÒ\x000ew§bÐß>Ø>>]\x00178ÿ\x000e\x0005ú[i¢¯ÙRÃÇ°)¨>ªHE?Z VuÞú\x0008Ü£ÝÒmîuÍÇ¡s@«²)ýh\x0001JïÏ]^-P.tï§9\x0013F
+\x0002\x0015)æïÀn\x0002ú\x0016«¶\x0003dÏ½ÅV­\x000cÆ6îZ5"ÕmôË\x0012RE¹¥TÙ<\x001dj¨·£\x0014yå\x000eèæ¤\x0016 UÚÂ\x0002´0\x0015XÅÓKb\x0015ýa]r
jÑ
ýhJ«cÆX^jCÅ°å=sP³"úÑ\x0004\x0015\x000bKtúJ\x001dl¬Yè¤ñø\x0019q
i\x0005¦\x0011©ßåªé¡6Wäª/sêÄ\O\x0000é\x0017óÚÜ>qb\x00153\x000f\x0011
r\x0008b<TÇ»78ÿ\x0012\x0006h¿èÂ\x0000¿þñ{\x0007úëÏ¿þý_>nÏ`Í\x0014ZcßÇk&%MèÁ°råö®óüÎòí?t¤ß~õí×ÿðöÍ»Îæ÷QV ¼[YÁ·±§Ü\x00052
foe½\x001a
Kl\x0014x¡ýö9à3ëî\x000c·À`KÌå\x0019®¬¯¬´¼áÂqoó´}óCU\x0010Ó&ÄÅ·ËV\x0007ÂP¢ÂÄeKËæ\x000f_¿ç\x0001?j7\x001bà­xc\x0002\x001c¬NLTj`"[ü^RA4 Î\x001aq6"n\x0001M^¹R=ñJÎ'îÆ-$¶\x0006qÕë\x001dÄ\x0011\x0003RëBG,µR\x001a\¸ :Æ\x0005­Ç\x0018K«
,j²²æcé<\x0003â¤\x0011Ï1x\x001ek·Ðe§7\x0011\x0014AÇUôyÄõ|\x001bbr\x000fÛ©ðîU?\x00141ó{W;\x00149É5w
sG¡a»\x0015\x001aL\x0006ÎAn\x0011-\x0000÷+dÃë\x0004oÆK\x0000ïÇ<\x001bàmÌÓ\x0006¸ÆWÐweFä	´\x0006ØKÛkuÇb¤³a÷J·Ñ\x001dýl\x001c1J±7Òßi\x000bu¼(\x0016Ö\x0012È9jÈÔ\x0018cÜBpÂ\x000fPû}æ}¥¢Sàpo\x0001qÑ9Å6FiC\x000cN6îÒÔ_G\x001c²4å´¢\x001bÂô\x0004±5¶ÑëRé'Øù$G'ó'ùx£ô<d\x0000}7-3\x001bä\e!£/E$ir!cá¬yÈ¾hÈÞ\x001aàHF«;4#Î\x0017å,\x001f_
£>\x0017½j\x000b\x0017ÈwÐÍÈ,üÕ®ö|S=nµóÑÏFÈ\x0015ä}ÏÓ®º\x0014³\F©»	d\x0004måí=Æ\x00049µìÍ![Ùq¼H"Öéï´\x0006q\x0008\x001aq°foÔ7ÏÎGÏ\x0014ØÏEÒ|üá¸í<d\x000fF6\x00171AÎ®ò½©¥l¢jQ*ÁÔZ¶\x0008q}Ø¾e\x0008Ôõ¸=S4çnäì¥¼JJÓK ?¹ý\x001eÒbØ+y\x0008ò"÷Ú\x0018\x001f\x0002}¼}ÁÕ´¼«{\x001dù/?þí×¿ý\x001fêÞ&Ù#Ç÷Ü
7ð®9\x0000ÿ´\x001cQ\x0014SI3RñCÖõ&iÌJZ¥ÌT\x0015%u½Qo£g=|¯·Q;é´#\x001cð\x0013~\x0015'n8"ÚºJL«¯ßÅq\x0007àîÀ\x001f¼\x0007R·]Ð#N§Hu=Ë".qWÕðÅ«o¾ûæÍîóuc\x0015°ôØ\x000fZäÐÇ~\r{oíÇYýÀêm¬^ûIç\x000cbÈ¤V½["=EºÒbä\x0015m¤!jíX
k\ö¶ÀF}
(q·Öí8l\x0019`\x0011¶há#\x001fòA,´ï¶¤Ý$a	Ö°\x00046ØXôlÄ+es_°q;BLÃ\x000e\x000b\x000b6F-y5g(ÂÚo¨âÝö)V?,Yo\²,j@òz\x001eÄ\x0011\x0014¯Û+äKV¬\x001fV¬7®XâP\x000f\x001bä¢½Âö+¸\x001d\x000ffaÃ°bqÅæ´¾mÅ»ÝZ¼ã°C8\x0008Æp\x0003k²´U \x00076Õ3f	XÓ°Ö°l°%LÍÒÀ\x0008oûë\x0012Ô0 \x0006\x000bjÝý:ÍsG»¥ÊªvÝ,»\x0003l4ÚzyHY\x0014Ò\x0016Xj×íw¬iØ4¬ØdZ±Õ²^K1CÖöûjYÍ
ß-\x001d=\x000e\x0006Ødå	jYÔ¼ fÞ\x0017ìV\x0011\x001fg\x001dl29YV=æycu¼Ñ\x0016Ö Ç\x0012vE¥\x000fÃæaÉfÓüè.å\x0018ZíU5,ôUpIVE lÃ-xÉ\x001aý>:ÞU	\x0018X·ß1\x0005´\x000c[«\x0018·\x0016ö\x000e\x001fÛÚ
¸\x0015´ùKA\x0019¬ZVeaWyÈRñ^­Zn\x000bà \x000c[«\x0018·V«¬Ø}V×µ(>\qB\x00047º)å§\x0012íÔ`Ñ\x001bRÓíºÆiÚÕ "¦]O*²­\x0013éJëõDK©\x0007/ÚÔ¦¥ñôMÆ-\x0016n+!\x0002«¼.´·´\x001b·ßMf\x0001\x0010¨¦l«ú'Q1Õ°QJq\x0013÷öé2pWxuûÖBk\x000c\x0008!ß\x001eýT¶\x001a¶¿ª^t\x001f×¬7®Ùz¨Í
\x001b4;ô,	)«`·ï8í¸\x0010¼q!$ºù\x0003d}±Fú\x000e»"ÖÂx\x0001Û¦ÂFQD\\x001e[\x0017jòØ\x001f×wç\x001d\x001d-\x001beA&a-}aa´Û>}\x001866\x001a\x0017m{¸Yhëf²\x000c¨;ÚíÇyÚ0Ò\x001a\x000f`D®mÙbroä=vÛî¶@\x001d¦\x001dÏ4`=ÔÔ3¢\Ñó3uVÚm/¹ñP\x0003ÆS
\x000béGq\x00081ê·=ù¦Ý!\x0015ió¸n³mÝr\x0003´¿¢ÿ¼¨O\x0005v\x0007ú\x001c§\x001dãñ`\x0003­¸Ñ:1¬vê\x0014¸«Ðu\x000cÂ#9×¥Ãà\x000fxõ÷ùøË/
öýß>}ùû1V.jk*&¡fa®ùÚz\\x0010Ë.º
¿Ç}õí÷Ïß½kÈïÿôòí·GqMvb/WßÄRT¸+_mKSiMLgl\x001cDc\x000eÌ\x0002`\x001bË`RòÖ^3\x0011û5±7\x0013ctaY\x0015MÛ&ù¢M\x001cKÍõEÄaM\x001cÌÄ^'\x000e.6&±1$5ñæQÒ\x0004\x001c×ÀÑ\x000cÌB<\x0002\x001ch\x0013³KÓU¼Y'o\x0002Nkàd_\x0013AêJ)\x0010X\x0001¯	Ô5±Ùh"Îkâl%v¹\x001f®«\x0018D#¯Fd½
«ÿËl\ÖÄÅ¾(HÎkÕÆ^"G·ïf©\x0016ÆØa\x000e\x001eïCEÕd©\x0006îzº\x000fÑSÄÞÁr;Úy\x0002=w{IMBåýúçßþÇ\x0011Ü\3\x001dñÃ5.Ç¦cÏw\x000f= ½r Jûõw\x001fþûÓ°àÒ\x001av©I´Ð\x0016§r\x0010ü¸'\x0015b>8½fHÛÙï,­\x001fi½\x001b¨Û\x0005)a{Ö©°*l\x001eó°e
Xl°\x0010$XøÈY{£­~XúÃ¶àÜ,-
¦E2¶¦\x000fÒESM+4,\x0011"°eû\q\x001c\x0016Ý\x0007)ÊúÕÕgüùó¯ùòóo¿üëoGz*Yke	\x0013!Gh5w¡²Ë%Nqy»\x0010zÉýñ»7ï¿ªèïþáÃN\x000f¨\x0010ß\x001aVø&Ñ5K\x000c$\x0007^@Z\x000e\s\x0006é({³Ò'q F;q\x001a].°WÔ~q^ ìHL\x0012Ç8WE!ÉÚ+\x001b\x00140ò\×ñ5ÈÃÔ
åÙkÞ^£¼¦ñ£9ß\x00150eNÃædß}Dí¡*²®IKÜYrW2ºÍ£\x0005yÜ}`ß~.kÅ
7ý4\x0007Ç#rtû!îÌo=È\x000c\x0014ÇCóre}ëp­þøþý~<tÀç[^Uæ§vÂw\x0012à$~Ä¼=LF«Oþæõ?¾xµ#!Ä¸&F+q=ÏKõ
A.¢-Uó\x001d\x0019ºøºi
LV`nmlÕ£XS÷¥Þ5\x0014§ãrù\x0012ð*^¿æõf\x0003óxd\x0012\x0003ëË{. Òh5oÞPÃ8-LA*Í	I+FsJ¶ç)ã8m\x001cHz&\x0008êznQrqrµ¶ô^EÖÄÉlc.+e j¥E[¬xÙ\¶ó8ÛmÅ\x0019\x0013Ä(#Rê:&]ÇK·ò5ÄeM\Ì6fEXYÇà¤+>¤\x0003é\x0013OÎ¹xõÚÍáÃÙ½±ôm\x0013k\x000e8±1ÉIuX¯Z\x00150\x0006<sÄãñå­RX6£%¹H&\x0014Óö} x\x0008x`x<»UïQýÛäò§n=K×ú\x0017öÄ]¦\x0007æÇmU\x001aCZçÒ\x001cD»FéËb\x0008\x000cQ\x000fÌa¨èä\x0001¨\x0006wMÂAPwAU1&ä!ì9îaÆ\x0007\x0017%$Q¨ÉÅ.¼Y¾aB\x001eâ\x001e\x0003\x001fÕ´\x0018¹\x001eUÛ ¨â|_É»zSÀCØ\x0003{Ü«XLÌ·AêuQøë,<Ä\x0010°\x0007\x0011òìÛ:Îr\x0006)Ë\x0005± ï
lÍ ã\x0010DÐ\x001cD¼\x0003½w%sñï\ú²p·À! 9,Òer
Á(å\x0007ÅëV«¼\x0005ç&s\x0018a]¸"Fv7#\x0007=8¹ÍÊ4\x0013ñ\x0010EÐ~rYóz~²\x0011Õ\x001d\x0017@¯r\x00168Ä\x00104Ç\x0010¾HíjØkãe\x000b¾ÝEØÕ¶B\x001eb\x0008cÇ[¤æ\x0006ÿFQ×1^râ\x0010BÐ\x001cB<\x0016ñÈ¼\x0016v%Vàí	+&à! 9Ô\x0013¾\x0008ï\x0010?Ø\x0015xö¯«"_¶£\x0013ÏNÞ\x0007Ñ]î´Ú\x001btEîAäºk!\x001câ\x001eã^ÚFêº\x0008ÝÊI/Z"\ed\x001aÂ\x001eÙÃ\x001eÆU#\x00078ÊWô F¾ìj°GöëÂfÊÐ>G8K3\x0019¿¬ïIâM\x0011\x000fQìQ¯\x0012\x00075²ª8Vä¢'Ôívs\x0013òx_h\x000e{Aü1¿I·âü\x0008ÐCÈe¼CÔ#sÔc9
\x00197èRxhQ\x001aõµûP¯
z4\x0004=2\x0007½Àg[\x0008i\x001b\x000fIïY¸\x0000ò*â!è9è\x0005Â¾ñxn[Æ¨×ô!oâ¨Gæ¨Ç5ra¸l<\x0012bMÜ®\x001aå\x0014ñ\x0010ôÈ\x001côB{\}y¯\x0005SR#ÇÍ·H\x000b²\x001fB7L¨u.JßYáw\x0011!¾ì8í\x0000âÍ\x0001{ÎÒ½a)ªþ\¨_\x000c\x0005tWå~ Þ\x001cAB)¬ ¹ gÐ­GZ»\x001d\x0003lv"\x0008âí\x0011¤ô2M\x0007Q«\x000bQR+{¼ÌÊã£9ððêV/¥\x001eûZÉ\x0018-KìK¹*îù!xs\x0014©.LÇÛW'¤'\x0011òRUwßf9	ypÊÞìy:eJ²ý¼èÙ\x0017}÷Ñew°±ÜÁ­g¯áT²k¹kà¹dì÷pÝÍþ;àÆÒã6D\x0012ÝÌR¼ú\x0008µÙT3EþQQ:úôè}ýû¬vt¨ý\x0007]{y\x0002]|Q\x0007»EÚì][\x0011ÿõ\x0010ÓìÄE°ÐK8yÕO»òSÄ~MìíÄ(o
lWsvqi½nÄ¸© b"\x000ekâ`&F'e¬%ÿ À)v±ô«;\x000e\x001c×ÀñÌ2\x0016I|äç\x001cÐe¬òs°)Ød"Nkâd7qo!vÌ^3©~{*O¸ãÄyMí6v\x0012M|=r¶ßl¬c¢{*f\x001f'.kâb&¦ÈZ«£Ên©¸
Jz"c>L|{agâG/ì3È®ÏÒC\x0007r!PÝÈÅÓ&d\x0018Ánå ë\x0002øOÕÊÚ?\x0018üfá¬	y\x0008z`z®ù@
Ù^£,äsàUÈCÔ\x0003{Ø«ÑYÔm\x0001G4+ky M	a\x0013ò\x0010öÀ\x001e÷ªEë
2I-\x001c[YÂHÈ\x001e&ä!î=ð5©|FæÂß6¯&9T±àªÔ:<D>8\x0011úÔtÖ@"ó\x000bÙ+ëº¸,ðÁ\x0010FàD\x001cñ*ÃI²W\x0017×Wr|êý02\x000e^\x0019í^\x000bíÛ²à.NÉ.ªQðTÝÓqâ1­?×gm\x0019ÊX²fÉº÷®Z\x001588\x000b<$K÷Å\x0012D:¯&pÁo6'6^aÍºæã
¹Ç=¢«â\x001e\x000e[\x000fOl½¢"ÍÀ³9I­Üg³>uy\x0018­Gö­G GjÏÊ% Þ¢Ü¦\x000b_]Ð°÷È¾÷j¨v^¡;¸oÃÇO¯e*8:¸ú?¬Gàþé?þ×?\x001fÁÍ\x001e\x001eJË,*ÌèªgÖÐû´ö\x0004\x0015þôòíwo\x000e\x00014XAE aRm¨
J\x0002¶§ÌÞ®8iy54\x0002IUçBÄÌ>CVn\x001e&Io
ùLº\x001e6>AÊ\x0002\x0015Í#Ôc½ÜjVR×\x0018\x000f¦ØS	<H\x001a\x0007Òh"M%÷¡\É©&³K\x0014v'5\x001f$½<eÒM¤¹²¶ÿSÖ\x0007ÇäBîãÃpOþå i\x0019¶~1mýA¥£\x0019Z@½Î
Ã\x000bv>¬Ô3¸p=U|\x0002\
hY$U\x0016RÊJÕa¨0l}\x0000ÓÞO1èjÝE\x000f²LuÂR\x0006¿Ó\x0014v\x0014
\x0005hÛQaÉ½\x0002ª0Â"&ÓPÃf\x0011Í$*
;ª
\x001eGõ*cÑ©XÕ¢*¤5U¤aØQüÑD
zèÍ<£AoC²¢îËE\x001fD#j´¡\x0012uTJ­ÚKõõëOùë$i\x001a·²m\x001eÌÜ¢TöËü·Ê[}ÞmÂ=ÇímÛ\x001f¢^ç@üúÝN·rç÷\x0005\x000e´ØHYÒ¾ùTnx÷r\x001b:iÙLSçPÑ
¨è¨®£rì\x0003¸\x0017±§ê\x0013Î\x0007ªÕ(\x0014L>5r»¸xÿ¤£Nã2öMHwÂ\x000f¢î\x001fmî?æåòeAåNfY©(oð\x0019weß¦4HSÖ\x0013JÎZ\x0004\x001c5FØÕ>\x0008:)´©ÈÝö-GÍ\0)  ã3âNãýaT?¢z\x001bjLúí\x0017GR\x001a\x000bº¥è
«\x00115\x0018QÞÖ\x0017~JêP­êÝùèi<J'SH\x0001ôq§H·Â³ÊÉà\x0015Ù\x001fæ\x00115ÛP=©=\x000f\x0011rm­f½qËÛCÑ\x000e\x0002ácÙ\x0002ühC|óéç/ÿüéÙ»ÿú4æ2\x0017O´°Rô¤\x0006êÚGè6[o\x0018ôß½ýæå³wÏß|ý4)®IÑBê]Îÿäµ
+\x0010éOÜ[¥S ´\x0006%Ië~J¦T\x0002«\x0014ybV3)ÞÍ¦§HýÔLÚúûMK\x001bW[mª\x0013÷s©)Î°æ\x000c&ò¶o5Ñ\x0019ßé\x0016F\x0010É+ôw\x0015 §Hã4,\x001aT\x001f³\x001ebh\x0016Í\x0012ôÙ¤÷¢þ\x0014iZ&Mùt"6E \x001fj`[T¼;\x001cf
4¯A³É¤M-ªT\x0003îúrWx
³¬1Í wPd3ª=U~\x0014ï\x000f!]K
à\x001fTWv&Q$æÊÖw\x0012¨h\x0017»ªúS¤cp²E'.x(bÔ$W}\x0001û(\x0010wEs§Pè\x0004¶ðT·{7*é÷O}\x0019nË`N£\x000eñ	l\x0001Ê÷V©tPAà*¹FzW$l
zgJP\x000e±	lÁÉ;\x0019_Å\x000fgÜ\x0013³\x00184Q_¦ÛCg
:8}°yýz~nEíüÊ¶]P\x0011;êöØ÷YÔÁÉR.2¤Æv:ç{úå»»ÓufPqpShrSGµò2ÖÔ$JóRÚ\x001eÝ<Ë9æ¥¦O¡WSóíiÑìD'>`ØÙ<:ì)4í)j\x0003«ª3rz®:¬\x0008¹=à\x0004gpã¡_»Åíÿã§/_\x0016\x0011¸·õøôñË±ìÔÉi¿\x001eR(µ°hN»×Rß¿zùöí"\x0003Çç¨ço\x000fPã\x001aOP×%²jyzDW/ªuî^¥\x001a i
M' ë\x0012Ö­\x0016U7²\x0006¯¬Á«Ü\x000ee ökjÚ£\[Vê(z¹\x0005Þ\x001f\x000cc \x000ekêpÅe\x001at ©@åò\x001b5u¾{à6@Ç5t<\x0001Í¯nM' W«7½à¹-¬Q§+©Ó: .Króx2Ð»RS\x000f"ñî T\x0003u^Sç\x0013Ô9õô\x000c³¹©ÔØOfÛ*Ä6ê²¦.vê[\x0017p %¿Á'UG·Ða\x001ezU
Î!Æ¡&Ý\\x0019Þ²!\x001fU	¾4îe\x0019\x0006ê10,ª.R.U×Z¾éû¤1¤»wa\x0006ì!2ÂÐXc·Ìíáq'2Î­b÷ñ:
Cl\x0013ÁQ¹-Ø\x00194¢\x0007Õ0O÷\x001fr\x000cÔCl\x0013Á1$í
^\x000eù Ô^\x001b``[4Î=\x0004G8\x0011\x001dyâ'Ýî£Û
è÷=èîÞ¢\x0018¨è\x0008'Â#Ô\x0014\x0019ÄTÃc\x0013þ­èàZÈÛ2÷6ì!<Âø\x0018y¾¢`³$TÛQ+þ\x0012ÄM½"#ö\x0010\x001fáD\x0000* \x001f\x000cBÖ3,Ízq#ö\x0010 áD~\x0019¸Ù°I
C$
6\x0010îêÉÏcã\x0010"ñDº\x001d9T
óíf#Ü\x001dpk`\x001eÏ`'"
Z\x00176ÏiMz2\x0000÷Þp\x0002Û\x0015\x001a\x000f¼\Ê»\x001e,ÿ·OëÿýðéË¯G¦¦ð±Ï\x0013qA\x000ew7¶ðywwBØ^¾©ÿ÷ÃË·ïw^\x000e\x0019×ÌhgæùÇÍÐ%GyëÊ\x0000:ÕÌÃÝ»yfZ3Ù{Í¯\x000bìR\x0006­uLõ¨¾;q
Ù¯½\x001dÙyI®KFy\x0002É.g-Òww\x001dÞ<rX#\x0007;r@\x0019$Hdex}_Ú¯(CkähF\x000em\x0005/È©<©«¾D­|÷~l\x001e9­Ó	¡ÙõPY¿v±r(zÛÒî¸Æ)æ¼fÎv3Ç^rÀã3Ú\x0015tv\x001e»ï^íÎ35s9aç¢w%â\x0003\x0005ñÍÝið¸³o§Û%8»¡¹ÓÛpÍÊ u5_æa'B`Y\x001eù£\}dtº\x0005éþ=ä<ô\x0010\x0002Á\x001e\x0003ÃMÌ¿°Rw«.ýåÏÃn?Â\x001cô\x0010\x0003áD\x0010d\x0007§T\x0006\x001d²Åýv#¼
z`\x000fÁe½[/RÆOØïÖÓþ$ð)è!\x000eÂ@\x0018UìXñªÝ1åå"¾.ß!\x0012ÂPÐóº#9±tVïA»sÌC(\x0013±Ð\x0013o¾fè$]\x000c¹	iµm¸W\x001b8Ç<B8\x0013\x000bA«\x0006n¹¨#½È«f¾,\x0014Â\x0010
áD,Dßãw.RØÎýajç»ÓÌ8B<\x0011
S?{\x0017HMq'×\x0008Øí¼Û5Ç<\x0004C<\x0011\x000ckÒ\x001fog+Åÿ¿8[áx\x001e<\x0011\x000cyn¢DpV9ji¿KúHán)Ä<ô\x0010\x000cÑ\x001e\x000cCu\x0017Q=\x0007JWÍüc\x000f\x0003amÐC0Ä\x0013gBè\x0000\x0005ûÔ#`\x0001O±ôuÇ\x0015\x001c!Ú!§¤2\x0017¤ðM¯lD u\x001e<fê*è!\x0018¢=\x0018F\x001ef"'Y'¾\x0003H5KËP¯B\x001eb!Úca¨{Oý\x001d·ÌDßsÀnÛñ\x001có\x0010WÐ\x001eWsÚÛã¸ Jr\x0010Õßá¦\x0000«	\x0006'Mv'íóÒÕÝ [3jé\x0019\x0007nê¸ÙÇË/»¯óÅ÷£&\x001fY¬ìdóu¾\x0006·A'ÜëòÇ%$9~×¥!]\x0015z·n\x000ezØdß¾Â$ÇoÂ\x0007]\x001dAï9(î¶\x0000ÍA\x000fìÐû¬³ô
Êté<±`D½þÊ)f?ìAb\x000frýz\x0010Cg.È¡/é.~ØþÄ>Ä ½\x0017¥þi\x0014è¨ï³t]ôöÃ6ôöm¸t7h\x0016UÍ"×³xO£/Û~ØþÄ6L©§Ñ\x0010¤\x0011+\x0015,×\x001f±ü°\x000bý]XJw\x001d £o8\x0014ê.Üïs\x000eÃ\x000e'²èèuÌIq¥)¥Õ³lêÆËÂw\x0018\x0016G8qgõ\x0000\x000bý\ÜéxV^Ñ×=S?ÿúéËx\x001fÍ?0¢³ØTNý®Ô·ë\x000e$ý®ôºðBk\x001dgÉ@ø'æ¬	ûÙ%;©¨ïwÓEjõGèå\x000cyr\x0014¹­AÐc"ñÑü²\x0004õw\x0016S\x0016çWÖ9ëÀ©¸SÝ§zIMWìN\x0017þ<>ókâms>ÿí/þå Öwî1ñ
j\x001b¢á`wu?ÿðÕËï÷¾\x0015\x0016×°hÍÎ;\x0011¤Â\x0014T¼ä"\x0017ÓËH¢khiMKFÓ&\x0015&©´¥\x001dhKÔ±C´{@õkToC-<Á0
j\x0016ñ´½è,.S\x0019¯¡
kÚ`4lukYiÓCi"XEViw5\x001f&hÓ6\x0019m\x001b´®\x0011«ùikÞ¬\x000bÁïjiLÐæ5m6n1ïÕl\x001bë¢h!£\x0014ÔÁ!;UÑ´eM[´5\x0001Rç\x0015¤@·TËvïU®ñ\x0007«·b^ÁÎH[ó(\x000eç!5_[ÈuÜÝ;	Ü12ØBCv|ö\x0000ÁÝÛ&'\x0013N	ï¶ZNâ\x000e±\x0001¬Á¡DQWª¸EjèJu¸\x001dwsx\x0001w\x0008\x000e`\x000eÙ¡>²VÜô ÆÍØi/\x001dÂ\x0003ØâC\x0006\x0017äæ\x001eSBí.%N»INà\x000eñ\x0001l\x0001¢¢ô´bºÍåÉ7ÚM±U\x0003m\x001ch£Ñ¸àåQ»Øy1nÑ±¼wÅ\x000c&qp\x0006¶xV° *\x0011Ë>s²ÏôA¤âîj®Là\x000eñ\x000c\x0001m×¥Û¼Ø¾»K»ò\x0013¸C@\x0003kD\x000bËöRë¶êTÖ	Ý]\x0013q\x0008ih\x000ci<×H\x000f\x0019øIr±.è\x0000S¢Î\x000f84´´Ýà&§sÆ\x000bB7î5\x0001ÇÓ1¢Õ³\x000e¾JÙ·ÖüÈO}é¦ÖÂ\x0010ÑÐ\x001aÑ¢ê]TãLe.Ô7Ú¾jØ\x0004í\x0010ÒÐ\x001aÒ\x0002È
<ªhläW	=JúÝJÃ	Ú!¢¡5¢e'z\x0002K\x0000Nm_ñ©´l;D4´F´\x0008=þ¥òf1®/z¼/$4;D4´F´úý{IÅ×\x001bR\x000fh»¯¸\x0013´C@Ck@«{ËW(¾Õõò<\x001dÐ¥àïöLâ\x000e\x0001
­\x0001­¦åêqc[
§î\x0015.:¢Ñ\x0010ÏÈ\x001aÏ2êñºâ¶jÜ\x0014»[(×D\x0008\x001aâ\x0019\x0019ã\x0019°æa¹%7Qòò\x0008=¹¹f£Ñx!f\x0010\x0000îæs{¸Ýl0Ð\x000e>>\x0017ú¸JK27¼h÷o¥Ý@ \x001d\x0018\x0019\x0018ç¹¤ÉBXå¹¡'\x000b×"hp\x000bdt\x000bE\x0006bTÜÔÞe\x0019W§\x0000\x0013]t+ææ­\x001b§¹\x0008májÿæÞ²»ý²´Ã>óÖ}\x0016|Ó\x0019Gw²\x0014|¿gò»Ý*\x0007h!»ñ\x0005\x0002XÌs4òúÇ>\x001e¹\x001eõ>I©\x001a\x00165% \x0017!,²\x0001»\x001a3òúÕëç\x0007XqÍ6V¾Wj¨\x001d5;PÔÍû»yTZ£	µ\x001aóA¬
Eæ2æ\x0012¤>ú°)è7ê×¨ÞhU^ôÊJ2\x001b§Ô4§¯Í\x0014a5¬YÍ¬5?7\x001dVÆÎâ¥q.®Y\x0002qÍ\x001amvå-Ý¬2é\x0019"vÔK@Ó\x001a4\x0019\x001aô¸°8ËbåT«nÇyÖ¼fÍFw5Ìr'AwWÔªOM¶<ÈZÖ¬ÅfW®ô\x0014»ÆÐ¢VÈÙëuGÝWO\x000c[<Æº\x0012Ëä0àuy³aå-\x0007¼¿í¬KX0\x0000Æ8@¨y,×:\x0005a%ß½ëfËÀ<ìà]Áè^D+wqY(~\x0000;ëæKÃ<ëà±Àè²@Õrë'(àJß]ïÐó°'\x0000+ \x0007ÒE\ÃÙ&rE¶~»ðt\x001a\x0016í¶í<p¢±¶+Ûî®mQÂyÖaÅ¢mÅ"d.¥_`¾0ä¬\x001dâ<à\x0012¿ÃEÛE·è´5'ëE\x0000¨:Y'ÍàdZ48.²9.~]\x0010õdWÝôîÅ 'ð°-Êð;Ø;ª´z*X×Tµ\x0001ÿÀÂHZ\x0000ÝËÆ\x001e¾63'\x000cKùÑ!§gÜN\ß|úüë\x001f\x0015yP
µ^rX~+÷â\x000bô\x000eÑ»\x0012?LúÍË7ï_=ß?r	-®iÑFË\x001aÿ}©Ì`\x0001§!á¾Æÿ$,­aÉhÚê[½À&2ªÛû]p»Ïú\x0013°~
ë­½¹®¸èª6Ë¶ì6\x0013NÐ5m0´u\x0002YC}Ú fÛÝ1O\x0013´qM\x001b¶þð\wTL\x0000tËÖAZ³&«eÔ"\x0015HíL]´\x0012o\x0003\å\x000fò6Ûý\x00184ü×U\x000bJëîN)¤-kÚb´­ï©LI7Óª«
¸Û¤t\x001cv=\x0003 \x000fE_S´ËÕ±ÁÐ^qév\x0006Û»8\x001dâ\x0002\x0018\x0003\x0003y/oËBhÍ®<¢(èBØM;;8[0z[ÆÕ¨Ë
²\x0014T6­î²ÝR	ÜÁÑ§~ÏQPÓØæ=§aé×Ó¬+Úg«YYï¹%
ZÎ^Ó\x001aaÀ
\x0006'¡)<\x001a±TÐ°ß½ûõã_?\x001d\x0000­ûév{PWÂbY;6ÞMþúÃ³wïýòiBZ\x0013Ò<apýî\x0018´$-\x0010¦~Éy\x001e1¬\x0011Ã4b=\x0008huLÍ\x0000µ
¼¢ëkb¾ï¬\x000e3¦5cfä3VSâÂ\x0000rÉ\ÛÖ\x0018ãý­ÃeÍXf\x00193KowÄ\x0019«E¥ÆH+¢î¿½<Éçað\x001eú÷ÌºÉ¬/õâoþþãg\x0016oüéã³\x0017_~þí|úõ×\x0003¨>×ä¤]\x0011FêAùò½mðâÃfvýâO/¿}õÕ\x001b_?öâíw\x001fþûË÷ïWàó\x0000Ï\x0000§ÜÆqÉt(>ï¯:©ÍF²IÞÛ\x0010=æå\x0019zv^§ã»B@ÈA®
O\x001bÀy0p>e`\x0017¤gû(ø6n\x0001ÇêS7õÌîð¶{\x0011\x0016nÕé\x000cË\x001fOÐz\x0010}­üÜ\x0011Ä¼òtP¼ßÌ\çÌ\x000b\x0010FâS;@\x00160\x000e\x0001
YçV\x0014ï6ï¹'qX\x000fKóÎ\x0005Qdb}$¾K² ÔEðØµóÄ·ï_¾ÍÄ\P@²(Èë\x0012NE3Å³îíiâä\x0007b®\x0011³\x0013cââ¶éú,\x00042Õ¬ºµÍõIâ\x00031'\x001cvbòªÀQNµñ\x0013Jëtñq3W%\x001e7^9³ñOÒ<\x0018\x0011N¶d)\x001c!\x000bB\x001dºaçñÇ3«BÊ88\x001fSö\x0004rt¬¡cs2×$0\x000e\x001b?Úc	R¸¸É¤d,c5ñæóÍ$ñþà©ü'VÃ¶Ù65ÿi»FO~¶ròYÜqEÊ~xB\x0017_¥<×°´F\x00107ï>&ãà'øã%ÑÜ\x0007¯3%ëzÐlmózqv\ÀñÔ\x0002f¯ÖVCÂ\x0007Y\x000f\x000e46Íw§IÞ2Ä
þxkÁ%Y£>X.\x0006M¥9bºUY3ñ2\x0011ÎL\x001c2Ê¨I¾\x0010Ó-W§7\x0007wÍ\x0012çøÌüÌ«{®H|ýCJïë;þx\x0018\x00161<abÊÒ6RÈÕ*¸Ì\x0008Ê\x001aËf?Ù$ñ­\x000ct!æS·ØÄ#±u\x0019·Ñèõ¤IqÍ»ý£Äuq=ºcò°~è{ÇÇ~:r#V=V\x0003³çâë60A¢6\x0015`W2æÝó·/^¾~½{#æ\x001fMÊcZ´Ñ\x0016·¼H/´õ0'êGèT,&àÝ1y´´¦%#m=ÌµèV7@Ó\x000fÂ c;¿7ê×¨Þ\x001aõb´\x00066)±­´}6J\x0008»\x0017£\x0013´aM\x001b´ÙÉµ¾çÖæÂ\x00129ñZs½÷	Ú¸¦FÚ²ÌH_hShó\x0001ø\x0015XDXTê\x001aØ´M&Ø\x001a\x001cµ®\x0016Ø²,ßV¥ºÂýÙ°y
°EÀóåChzW\x0014åy'ÅýÑ'\x0013´eM[´t\x001d ¡\õ&\x0006BËÕKWÐÞ\x001eúÀà¸,¦¸YêìG\x0015Õ´YmiÀ\x001dã-EWtìoEÄöbÂÅøº\x0014h·Ñivc`\x000bd\x0011ê6\x0013õ\x001cßª¬Òmîáb \x0003î\x0010ÈÀ\x0016É"\x0010Èì\x001bA\x000e\x0012É\x0017¤ä{÷khX\x0006¶`\x0016Á\x0007\x0015WÅ\x0010¥±f2N7ZØtÀ\x001d\x0019Ø¢Y>E7\x0018ëîÅ¶»µ
\x0007`1=\x001e°`õ$ùýOÏ^ÿüù\x000fäµ®8é\x000fKcéê\x000bÈØâvôª><ûþmMl¿{óÍÓ¤¸&E\x000b)pÚûø¡f½\x001c«_ÝÎóäqRZÉ¦\x0014¤\x0000?ðPÎöHéë?%w
î{Ìú5©·}û:7\x00072ñ3ÅbSÔë%·]Ò>M\x001aÖ¤Á@Z]}\x0010ù/~è\x0011\x0005\x0012>0ªMwúµgHã4lÊ£=@H\xøâ$9,¬gz\x0001h^fI³DÎ|ô©fwÅ2]èM«Ôe\x000e5i\x0007^X\x0006!ÇôôíX\x001aü\x0002ÔÁKÅM\x0011\x0017%5×\x001fXK­Õ~UT½`vtÎ\x0011TÊñÑMAxü>ùÃ~¬¡ê¿}óñËËÀ%ìÐq££V\x000ePOâ¯rëÃÝÆ\x000f¯^¾ª1ëÙ7ÏßîU/\x0008<®á\x001fßÝÎÁÇº\x0015øÖ` û­iÌ6ú´ÙFvÖô¯ÁfM\x001fQ\x000eg\x000b}b{=÷Vú'/\x001bçèýþñÍî,=Ï l¢¹¡z6]³ÚUoÛÍÓÚ	ú°¦ü¬2KOÄÊí¹ª°ÞgY8à¾çkøø_lÏ¦5üãûõYø&¿\x001dqÃ¨ðèu"5\x000bø]
×ð¯Ú§·,I!_Ý²Yä«é#éÝÔ<²Ó¯\x000eÿìë\x001f×úLã;\x001d\x0014\x0019	%V|bRO\x0004OÞdÏá\x000fÞ\x001eÎ¹ûÀ
\x0016êî=4\x0011ÀU jý/Æ\x001fÜýï=&£\x0015THl+\x001f
õ¡6gÇ²Ùäv~p¿+\x000b¥¯	mjKËVZ¿SòYN¶Ü	s­×ÁëÀ9·\x0013k\Ò±®u»²rÊ\x001fT3mßÛÀ/\x0003þã\x0007¨Yü\t¬\x001d×½à{]Ær¨×âãdâ¹,3º¤µ»D\x0001eÐ$Æ6©LO?úÍá\x000f;÷we#³ø±ð\x0010³\x0005?lU|,Éñé­9üaëâÉ­ëbï«ôüÎÖ²\x001d\x000f*áË¦>Ì	üaëþîE~\x0016?F\x0017ùÐ'èx'ÓÂbÁMÁý\x0013ôÃÎÅ³;×gÑi"_@³|Ò1\x0007±¦\x0014×.}\x001av.Ý¹^%E(@ìsY£VÉ×.\x001d\x001aOXg7.\x0016\x001d%\x001cø2Vf\x000c°©úx\x0002Ø¸tvã²ê±bÑy
Õ\x0005I²\­umÌ¥áBçÎ)\x0015?ÉÆå*\x0015y&\x001d6á6\x0000O°\x000fNÎ:\x001d<Ôt1}	:å;âôx»Ù~\x00028§ÐÙJAÍô³C)'­)L¿·®õ:~8¨ø³\x0007\x001aeQÆ%³*HË¬CVXÒèRüÁíü®¾Ûp/ÕjjpE6E*m6/Oà\x000fnÇ½\x001cá'Áç\x0016;yÚF=gÁ¶Ìä	üaëú³7\x000c\\x0007×Ö~"â	Ö\x000b¾¶à&¸øè|ÁË\x0017\x0002\x0007oÈ\ñPték	n?"ØñÃ/³÷ÉÉ5vv@$\x0007t\x001btq®\x0013m\x001bÎ^È¦$%\x001d\x0011ôBN¦$%\x001d'ðÇ+Í³Û6c+ÈçAZP}¦À?Ý\x00073Ç>ìÙpvÏVÓË\x0001k\x00185QÓ7þ;£RìôqXôñô#JîSØøª\x000fYôVð\x000fTáÎàãø\x000eÁ\x001fÏñ{\x0012íì~áå4ÙÙ|a=s5µî\x0002ë)þÉ¹\x001b*R¿ÏU8Q«p¤ÜEÜ.Î8éño!\x0003ñÎ%Í$ã£(\x0004}ç©ròUàÅÏ*ð»_\x0002Îÿ\x0012@"+AÈmÐrÕéú]!<Ý÷8@<þ%j<ùKð¨&vDK4«§à"Y\x001ch8üt7ï±ßÂGµõ\x0007ãÃî?þÓÓÌÉ%Tm].¡l\x0002 1ëe\x0003Æ'\x000cÿâùç/n \x0000WS9JÓz&äVéÅ\x000cË!\x0011I	yÕï/ð'\x0010q@Äÿ~@ôÿ	\x0011ýðE{Ë\x0017]\x0006ô\x0011R\x0014åÒ4Ç\x0010åÎ\x0017sÞß>»\x0010\x0006Dþh0#k:Ç¦{ÁÏín1û¤VÜTCxL8¶\x000b^\x0019ñÊ.<q'	¯«\x001dTº(í\x001bÙSéZ\x0012O\Ìî~ÁøÈÙØ¼MNNnîùSº²ÇÎ\x0018h\x0004Þ±á¸IÐ´K"_eãðA=¶\x0007§ßqÞ]v\x00080É\x0006\x0008E\x001e]q9\x00145\x0005I\x0016cTI\x0013o]4®B²­Â£êÔ¬\x0003¶aÍ\x0000U\x0016&Ùùüà©ù£/ó×½¡Zç¨ÕÖõ\x000b~"·ÞâÃøèy½þà\x000fëêõïúøù_ã\x0006·CóKîzp.¨Ä5Q¾iYî©×}ÿúùøÀÝm{uËì\x0007doEÎ=ÙÇÌsÒeY¤±´«\x00129\x001c\x0006ä`E.^5r&¹UËA\x0007GG
ó&â8\x0010G³Éë0Ìó+\x001b2é¹§M9y\x0013q\x001aÓ\x0001\x001bç8mì³4ðV\x001b£ÜVfß'£xÜ¼®4!\x0001¹ØÝ\x0005v¥¸z¼ÀÏ	ª\x0016¶ù(hA¾%\x0001¼\x00038ie\x001e´)ë¢<h\x0016 RØ¸Yycâ\x0017Ì¼.ÊUd5±{çuþ÷AÍD<Ä\x00104Ç\x0010\x001e{jâÀõ=õu¼;f
\x0006d2#£ë\x0002³.ña¥¥6:NËï7õN!\x000fa\x000fÍa¯8§£n3·Í£\x001eª<læÜ&ä!ì¡9ìÕxÁ¥zQæg\x001cUsVdJ-!î¡9î-êþbåäþª:j\x001d¨äaWht
y\x0008|h\x000e|9¨T\x000cò\x001a\x0011-Lß'VÕ}xU\x0018Á!ò¡9ò\x0015ê\x0013
øæ%X;½Ã¨ð-!ò¡9òÕ\x0015ÐOk\\x0015PäÈ«úcà5È4D>2G¾âû¸\x001cQ
\x001fsÀ/óË4\x0004?²\x0007?\x001ebF=%jª¹×:^\x0011Ñ\x0010üÈ\x001cü¸C&ð^NñÁëÈ\x0015Ö¡»
y\x0008~d\x000e~¥\x001eæeT\x0010Ël\x0006q\x0018å\x0014]æãh\x0008~d\x000f~5¯zW¢z!«rô(½Û	<<\x0004?:qæ#[zO=°î¦Á×o béµ´ò$yéÓ0ë±Zï\x0004B\x001f'·?°ñ\x0010¸wÁóM]È?äÕ[æoÏ¾úøï¿üòé×'y)grá\x0013HíÏ,ú¶ðf³¾õåÃ³¯ÿã»w/ß?[Ò\x001a·$#n$®ißÔE²4\x0003p°TöåÅ*\x0017ÐÂí¡iaýÒ=»\x000c¡^h£oºB\x0015\x0017e®X*yW\x0001ò0.º\x0001?Zpy\x0000<ÝùÀj1¯Ü	¦\x0002q¯\x000eå8.\x000ck\x0001Á¶\x0018
wòIp2¶­âfU\x0017ÊÛ)ò<ï-©XxÉÙxçÝ¶xk"Áw\x0001ÌË
Â\x001b6gRÿw{Ri£+ã¥*ìíÏ¿ýÊ¾ìÙ»?~þõÙ·\x001fÿýïG\x0014¯)G­\x0002v\Mø\x0007\x001e8J¤ÕûÁoVg¼ýîÃ{vfÏÞ=õæý³oÿã·{â×9Ñßg¬Ì1;£ú½-Ã+sG¦mA\x0011\x000br\x000ekd®\x0012²"³Èñ×ä87;×Ü¾¾ØL(LÌy`Î'Æí*g¶Ñ¹}äÔvrla.Ë	;óÐz\x0019Å×DQÖ³Þ\x0001úK]\x0004
k\ùÙ\x001f[©iY\x0012QfÎøF]Ó¾:¶[¨oï"\x000bõò0b£æIR\x0003âÜ¢­·Ø:¤Òm}Õ\x00020Ú:Øm]OH¢^\x001d\x0008\x0011Tê¬Sß
5QÇÁK/ÕJ\x001d¢H¨z:]×þ6:'nv§Z¨\x0011Íhß\x001e£ÄBâ©á¹³®9¬mÍ[\x000bt\x0018\x0017H8±@jÈ±äÉ·öè¾I\x0016Üì+±@W\x0003­¡ù£\x0015º¢å5£V¥\x0018\x001dßÒöV¤«VuÌq¤vj¾@lÔ¾æ!¡­êØ'n´}Él¢Î#µ=.¦j`©heÁÖeÈet	v\x001eÁöñÏB]Ü@Í¥2V[G\x001daD!æöbR;GÛcÍ\x000cÐÉ\x000fÐüÑlêê@@
>k
âÛ^L\x0001oFW:Å:0u*}\x0014	ÀËÚkjÚ\x0018µP§a3òG35ßt©~CjWÎÕÖ\ß¨óv¡zÜéÄfdázYÖïÌãKàµ\x0010Õ]fê2ºØM]]ÿñ]b»ùb\x000f\x0002ÚDtÛÇIê,5Î\x0008à<U]n
\x0013Û×u&jzDm?,®PÍ
º¬YjEm®Ã\x000e°í©SD'Ò^ì[_µ¶
\x0010&\x0017åÖ\x0000.=¢¶§©5ç×îEà^¨c_ØÛZ\x0006\x0016ìõøÅîh_#5Ñ\x0010µÇ¥+N÷£Ê$(W])\x0000­Ô×\x0019{¹¬°º \x0003+`\x0004G-hO7UGLÔã\x0001}ùl¦ Ï9\x0001\x0017 .ÔE³'\x000bNè\x0008el\x001a@®ïi\x000f\x0015ßüí§g?|úòS¥>6YÂñÝGlõ¦ÒÀ\x0014¢\x0014ô°ÀÑ½ïxýìo_Wä\x0003°¸E#,|ºÁ¶ÚwRÕ×D¼Wú7IKkZ²Ñ\x001cU2*gm*\x000c<\x0006CÖÛöÍó´~Më­´ú^E\ùPÄ¶A\x0015¢îZOÂ5l0Â\x0006©¬%®B\x0019}\x0001¨»î>\x0007NÂÆ5l4Â²\x000eÐº }½!¸¬´WÁ¦5l2ÂÖÜGb\¡>*çÙiCã]%ËIÚ²¦-FZ$F\x0010;ìm¥»êÛs°+9SvµÎFëkþÐ^#¼«	oË¶:\x0007Y\x0008î\x0016dLâÁ\x0018\x001a|vrÛìë¿oÚô\x0013¥\x0005ºÆ}Á\x0010\x001aÀ\x0018\x001b|Me\x0000[\x001eRÅ¸Ú³wgb¨\x0001w
`\x000c\x000e>F)ô|Q+NÁ÷Ñ\x0017u-Ü«@Ä\x001d\x0003\x0018£\x0003Oõ\x0012ãrÇ\x0018×Ia\x000e7x^\x0013\x001d`\x000e`\x000c\x000få%£à:©½\x0008ä¥«!ùr·Âe\x0012w\x000f`\x000c\x0010+ã&Ç\x0013"Å¸ºrÓ¦^v\x0008\x0010`\x0010\x001e´¦yÖçÊmR(\x0005zðq³ÙÚ\x0007Ül4.+"ÈFã\x0014§­\x0005\x000cQ­/ÊÂ`\x0008h`hÕyq¦Ø\x0016\x0003I1u ì¸éî9\\x001cB\x001a\x001aC\x001añh$Y\x000cIfJ\x0007ôQ½XÞ¾ §\x001d"\x001a\x001a#\x001aE\x001c%ðÔ/`Bå\x0004\x0017\x0005`\x001cO;ÆVÓX.\Ëe-_@\x0012UñºÓ¶ï\x001bæqÆÆ¯£LsrÄ5É\x000b.ª×
.\á\x0010ÒÐ\x001aÒjz«¡fèYpIoßý¶t\x0001wihi\x0004Iú¾«\x001fó¢°\x0013\x0010´òÆçÍº1\x0003î\x0010ÓÐ\x001aÓz~QGD=ª×½xM:CPCcP#ðòn¾¸]IÍ±+>T·{g\x0018\x001aZ\x001aBÇÕ \x0001\x0018/º³Á!¢¡1¢+ýÔÓe­\x0002º¤çxÑ¥

1¬1Âé\x0003ùr²ÏÜÍ-à5+Æ;&«Ó­¶M^öÌ\x0014¢Zí3\x001a¼\x0018\x0019½\x0018\x0016½^ð\UÓ¼+®+z¸;Do\x0012wp\x000bdt\x000bÈríR	å
\x000fú¡Jº&\x001b£AÆFµ{~M8é»Zf¨\x0014±±JÕSÁk\x0002\x001bßA\x0013Ðøà$¾Õ-\x0018ÄÔ%ëÂ8\x001dÞèÔÎR\x0013{+ïÿn\x0008úõ@|5Iow
Èïÿ\üHA+4±ìvh~·È\x0002½ß«ê\x0017P\¢	4¤(ò^\x0018½Þî\x0017âbðÆºÛæx\x001cÖ¨d³)jµ\x000c&È,¸ &íÀ´ÛHsÕ¯Y½Í¬Yg`LY¤\x000b¡ö)áîÐ¿ã¨a\x001a¨Q\x0004I1F© `T©QC¤½^\x00150¸e\x0015¬;Pf\x0016\x0002ë¢´bâåå²-\x0004\x000fA÷W¸{8ì=2r¼=úñ\x0016\x0019$\x0018ÿøóç_?~þçCcaëÎr\x0007ïûh%\x001aKI¼Û¬=ºÉ|üñ»7ï¿ùf·_fAUÓAEq2Â\x00143ãÔQas33Ë+ó¾@Óqd\x001c¬\x000ch7s\x000fÒØ± ç¡#on:\x00033ÒÀdfæcp«k­ÿ"/mk\x0011ª+¦§&\x001fgÎ00g°2W3Êp]ÎN: #°Ò¤Úy_7é03ÙßôúXu@:\x001a¹ª5)ó\x0013zTÇãÈ\x001cíÌT	óp\x0003ßNq5o×õÏSÌb\x000cyÀu¾}ÀÝ\x001f?}yö\x001fÿ×³Êÿo\x001f:
³@¥\ðÔ-è$±Ôk\x0001ï¦h_xöÇo=¯?|ùÃó×O\x0013Ç5q4\x0013ó\x0004Ù"sæ³*\x0010\x0004n#\x0011ät÷g\x001a9¯³\x001d\x0019QJ£<ò éÅÏù\x000e@öÛµð\x0006d\x001cÑÎÌR sÜSÓ,	.÷Éè÷§¸O\x0012§a%'ûR°
,V®\x000e/£, ñî«À$3À`e\x0000»]\x0001½ zx\x0006\x0019ÛË/
:ß=ÎBßÂö\x0002Ý5@\x000cò\x001a4F\x0015&õ%&Òõ¼3\x0019sù¦K½0d7tÎ2C¡¦\x001aQM¾èÐ¢Tþ»\x0012cÐq4t´\x001bW´Ac\x0000çÕÑç¼o·Ym@o7gã\x0001ºþàvfÝw?ÿôã_?~ùñ×ÿø_O\x0003ÇÄ}Û­é'\x0015íéÇ$Ã\x000cã¶>cKóY`÷Ýw¯_}ýüí«÷{"Ákd<¨7à\x0005/cG39í¿Ktÿ<=ËLkf:cfvþÅÎØd@P7 k_gh¿ö' ««ðE [¤\x0017è\´
¶ìÈ¹ÍB5t8\x0001]¢ ®n£IÙgì7C\x0011v4bf¡ã\x001a:Ú¡!hÁ*gþí\x0015¬¦rz\x0011Â¦Ô¬9¯ó	C×:X*À£6Þí]kM2¯Æpúx\x001bdmZ\x001d(Ù3qÚ«4:w]F=úè\x0013N:f¯\x001d(PÓQ\x0006UÑwKSæ\x0007'
g¼´\x000bÜLµ0·\x0003ÀbièÛ\x0012Ù6êÁMÃ	?ÍM=	uá³ábi*Q©ï'\x001dÓÔ\x0013:\x0016§­»\x0010£ä¤\x0019N\x0018ióºÀF=ø<8áô¸MjBZzê\x0017[gm¤ßKð¦©\x0007¯\x0007'Ü^¬¨¥tê6\x001b+\x000e\x001baêËâ\x000b\x000e~\x000fOø½x+èY'b¡ö¹Ûú2\x0017cwÂp[¸=¬ÞÄÔ\x0018tÅBÝ,õ°\x0019ñÌfôZ\x0016\x001c\x0016I=¬\x0004î²\x0008Ã^Ä3{±=L-Ô\x0010¹SIÖÎç½ÿò7O=ìE<³\x0017k²TÚI\x00001Ý¼µ
Er/ÊUÔ4ìE:³\x0017)ÉE
!E\x0015\x0011\x0005R\x001dµD³
mÔÃf¤3±¦KE¨¹qP¨¡oÆíc\x0013ô°\x0017éÌ^D¼\x001aô¤\x0008 Ï\x0015ùþ½Ç4ô°\x0017éÌ^\x0004íêA\x0014eà|Aöâuç[\x0018\x0006÷,W	·\x0017CCÒ\x0017z[º«I\x001e\x0018U\x00055Ä+N¹\x0005\x001eÙ»ÀÍÞ¿=ûþç>={þÛ¯?ÿýç¿üøÓqI	A\x0007ÏyðRr\x001fÐ|÷ûáÙ÷ßÕ=ÿðþ»o¿ûêÕë'¹WÏÌ
NóxH\x0011á'¢yL«\x0005önÖgÉWC½¼\x000b?[ÈëK'ò£ó\x0014rw?!1ÇüÔb)]äR|\x00109e,:	>ÞË\x0007OãbIg\x0016Ë¢Íß\x0012\x0013_£½¨*\x0007Ð*ùîþ49®\x0002\x000fw
÷Èóx{ 1­?¸å¯¿={ñéó¯\x0007&±jaÖH\x001eDs¦:D½¹|ÿèûáÙoÞïM+SÌ4`&\x0003&d\x0013ÆrjL6ÇÎaÞ
,\x0019ÈÕ;óPµ¤I§ùæû\x0017zÇ1óm_º\x000eÅØ­ÙÛ lÎLÃ\x000cÃÚ\x000cµé£îs\x001bi;\x0008ò­cìómï6\x0014\x001eÇ,°Æ,`À\x0004ä¶fMj¯Ü¬kH].\x0001Ïé+Å\x0001Æ\x000c\x0006L\x0017õ
#ñ«`fUu¨~ïé/ý
çÂ\x0008·«Of~÷9\x0001é\x0013ö
Ä¶\x000c
RÕ±«-ïÏyÚôxx"¡¢ó\x001f«¿?&zBõ¨Ã¤M/HYu¼ï¿\x0007¿|÷ìWÕÓïK\x001e+,®aÑ\x0008·ÙfÜ#$°^ª¨Ph¥5,Y-ë´\x0002\x0007B´ó}µ¬ÔP/\x0013¯¡õkZo_\x00072\x0019${ÔÒNÔ)¬ö~1Ã\x001cmXÓ\x0006#mu\x0002^\x0016B=ô ÐbÝ£0\x0001\x001b×°Ñ
K}ÕòØd/°:¢Ô»ë©)Ú´¦MVZ§ª¥<a£\x000eÛ#\x0002m¢yÚ²¦-6ZÏ²:ëÁñh´zÝàÝÎ\x001dÉ\x000c-ÎÖèm=¿\x001aè\x0015ëÕî6Ìæ\x001aZ\x0017Keí®Ëç<Ci1C2ßêsI÷ZÜ-ú>À\é±]­0\x0014ÌþòìÅÇ_~ùx×\x0017.$[lÌOw­º0ñeñ»g/¿{÷ü\x0010o\x001cx£78Éb¹ª^\x001b¯¶­\x0014\x001f6ÛÚLÈe@.fd§¡W¬ö¬\x0014
m%äÍëT\x000b²\x001f¬ì­V\x000e\x000e³¼×Õ<,q¨[Je\x000cë*>oNO´ §´FNÉ¾04$ó1{v\x0017d'Mõ/oVDZWUÔ\x0015y(¢³²O\x001c1\x001a².þ\x0008 þ­"ïþ<\x000cqX\x0018p\x0019ò²®\x0016#"êþË»s¥'³\x001b³3#û"=cEÆ[qB¬y°®\x000cØ\x0014K00£\x001f]·úÀõM\x000b|¥1:¢;Â\x001eï,³s4×8É¨\x0011õ«ûéÓ¿}üò×\x0005ú«?ýëo?þÇÿür(üAõ"Ù9rò¢\x001c«#ÏýÕw\x001f^¿üáùÛ¯\x0017ô¯¿þ\x000f¯^¾­ðÛGO%÷kr¼hg!·Ã¶[¹\x0002®_l\x0005\x0016#yXSäu$>,l5½O O£Ýæys´Û]ò'\x0017LZÃ§sð!¡*ñ\x0000nßj,Ï
¿]ÏbÏkø|Òò,Í,:,:\x0018åù.*ûæÕÎ^Öìå¤áÉË4\x000eZæN7»kE\x000e\x000bgnÅ\x001eÛr_ÍñvM\x0018í\x000c¹O$o¦ìbZ\x001bO*]3\x0002ÑoÝk­~;Ë,ðpÒì.éëL\x0006mèI¥\x001e\x001ctÍø­\x0000j§\x001f¼;sï¹è\\x0000\x001eÚÜ{â(¡ß\x0011°ÃÓ\x0000Og×
p¾¢ð(ëF2\x0017fZñOÂ\x000fÑ	Î'¾\x0001WeòÌst\x0016?\x0012ÜöëfB`§\x001f"\x0014\x000cQë`tÝÈ¥~]7YU\x0002qóÄ\x000e\x001f\x0007øx\x000e\x001ey®8Ê(SSìê\x000e7ôvø!¼ÂÉøÊ×2=o¬[|ÊQÛñ[Æ®¤\x001fâ+\x000c°\x0018³\\x0006\x0012\x000f'm5=)ö· ²©l\x001f\x0002,°Ë´ÅîI\x000eý)w¥ø\x0007_ºäq\x0008±x2ÄÖÌE¦\x0005W»'.«Zì®Ã\x001bÈmv°ØáÇ#ÈÉ Uÿ'å\x0014D#"E×åX`ó&ÀN?8z<éè¡8-ðæ9é©uZÄ¬¦Í"\x0008;üà*ñ¤«ÈYdçóÐÎ$¼6»ÁÁWâI_	É«x\x001a÷ªj×ü¸©ûg\x001f\%tÀcÔE¹æ±%\x0008Áé4Ñµ\x0007)\x001c|%ôÀº.Ò
rÝÁ¢*¹7ë Íð4xK:é-¡:\x001c±<x¹9`=VÕD÷×\x001eHh8ÐÉ\x0003	8lÙMµ|i\x0003\x000e\x0003«\x001ajï{ÙÜj\x001f\=tõ®zH±|Íè·ñÔ½}¹ÔWÒàèé¤£gYÜÔ23VyHbyçtÙl+äÚéNfô.ê;ç~
';Ö©\x0002|ªvú!NÑÉ8åHoÞ'p7Óz\x001b\x001e_v)û\x0010¥èdb\x0001¿,\x0007\x000eÁºZ¤C0\x0005Ü,²Ó\x000faN)1'Yõõ4Õ|%\x0005ê¦ß\x001c\x0002k\x001f¢\x0014R¡Ô®Ö-%^\x000e"P¹Yûc&÷Cò'C\x0014Ï\x0008RÊÂu
²âIÅþÒµ·\x0007~\x0008Qþ\
<º½\x0015í{.Úo®\x0006£ëRâu\x0000vø!Dùs!*°êÎ)|\x001aiW\x001fÜ¬:Æ(?\ùsWfç¦¨ú1\x0017\x0011éU\x0019Ed¯5ýø¢s.ÂeBXÞé!\x00164\x0004UËûKÝ¼\x001f\x0002¬?\x0017`\x0003§*ÅO"ªÇÍ&N;û\x0010^ý¹ð\x001aê_\x0017q¾eâøJ¨§*±üÅðC|õçâkÈ·^öÂg\x0011Ï:MÑ»Íá·vú!¾úsñ5d\x0004-^2ö¾\x0000.ô¬rs¥~\x0008°þdÍÜ\x0005Üàc^\x0000Ò´]vb\x000fC
çblH<	GV=©j1\x0017´«å7{ÜíðC
'clM\x0000úª÷Ú¡\=Mi°9»ÅN?\x0004Ùp2È²zÜ\x0013z\x0018\x000fmÕ/êr\x0012Üìm°Ó\x000fq*SuëÛN!­Ï%\x0016
TW'8e]ï(ûrjëV»Kgeñ×Rs<=ÏIÂ%'\x001e6ÿüGO9÷Â\x0016HÛÏrù¨¥¤wàÚweüóÇG¿ÀÇÿR¿Çß-#<½8SÓ1x\x0011Eï+¡CO´],yÂ\x000f=þ%Âù_¢\x001e\x000bU¬ \x0017»ØXrcÛzÊg~_?}yôKðONý\x0012Tt@sáÊ\x001c	gNßËÉ_\x0014¡<\x001aTÊÕó«ño?~ùõÇÏd¡C©ËÛ\x0005qÖiQñC¿+\x000býíó·ï_½ÙÕVZ\Ó¢Ö©T#FPÇÎa·Z|Ö´d¥Í¢\x001bHÜTÃª°òNWñ\x001c©_z+)> ïê¨­"®Ú5©È¡ß\x0011°¢
kÚ`¶«ê\x0012#yIÙÙ´]e´\dÛ¸¦vÛÆÔ\x0005$}\x0011Ûfß\x0017ÂE´iM¬´¯\\x0016Ú^xÂ
HºÃpóyÃ@×´ÙH\x001btN{¥-2H¤ÚV_®#îÈSLÑ5m±Úºmk u	úXz¿OwõV<¸Ä\x0005gwµ^6\x0019Ëè²íÌ]ãiabæ0¶H³.´.=\x0014\x0012ÓºN{Q\x0018!9:¤DþÝ­>!Þ45	;D101}ûYh³f\x0008¾Ó^ã\x0011`d`
e¡è\x000c/®\x000c\x001e4¡	yóþØ;20Ç²Ô§ûåå¥GbY§ÝkÙ \x001dB\x0019XcY\x0008\£Òh\x0014UÆ\x0014\x000e¬Í»\x001d\x0013¸C,\x0003k0K S¼\x00187k0+¾ã^\x0013\x001e`\x0008f`f \x0012	\x001eb\x001f\x001fÂ)¸à¦«ph\x0006Öp\x0016òW\·x;>\x0018®q\x000c8\x00044´\x0006´Ð'aA¼-znSÜâ/\x000e\x0011
­\x0011-dÑöÐ\x001b¥×~,ìJ'\x001cÀ­ÇÑå,|kÁª.Ãä«¿ÿËÇ_~iÈo~þ÷O_\x000e\x0015oBèSU\x000b>HÁ²/Zä6\x0015}^}ûýówï\x001aòïþñåÛ§y3­yYÄÐÈëûK\x001d÷JG\x0001îSã·ïM,Ài\x0000NVà&¹\x0000s/Jl\x001fø¸]òe\x0000^½T`~þ0\x0001SM\x0016¼Z8ê»PÆ\x000e\6oÈ-ÀÕÂT¼¦¼N\x0007üU^-\x0008ôestÌ</¸a	óG#p&QF_×JETvE\x001fú7S\x001d\x00030\x000c+bÑ[·\x0001³R¾\x0014d\x0015Êä±X·÷×\x0000ã\x0008v`§wWHË@öu_çÖ\x0000ËHlõÃ\x0014za¨\x0003½\x000eN©'Âæ\x001b¾\x000188\x0017±IB<+XpãmøQØJ(
¸q´o4Û\x0017Ö<\x0003 Ì\x0003á¤G0n¾Z\x001aËhàb50\x000fÕj ú§M·=%.a%±Ù¹8O.¬ù£ÅÃ¥#k\x000bKéóÎ/
\x001b\x0008#.qëiÞÅnà¶cÐ²\x0000ÏH\x0006`\x001cV\x0004´Úw\x0019²²¬aVÑmÀIË¶U\x00146xïè	ìh]4[\x0015hcßpEÍëo\x001bnëa0/Äd'ö\\x000fÐ³¨\x0006µ;t!ÞOh ö#±·¯`¦7\x000fD2·«ÚX¯ßÎm \x000e#q0\x0013û~=É­\x0010òv»ÜüË\x001a\x0017Ù8ÄÑL\x000cñA\x001e¸o¦±I¡h²\x00166)\x001eÞu5\x001a\x001f\x0005YJuö|ñ·_þZÿO_\x000e?#·\x0004\x001dXYD©:I\x000caSBÏõóÛ¯¿{óæåÛÝ3¨Rã\x001aOPóuZÎ>ÄÞD:¤u}¯£¦55 N*¸â=f¹H<ëO¨Ýý	tóÔ~MíÏØºÈhiÏòÃ¨½kÚÛ·s7#uXS3¶N,C¹PCÔ>àõ9.Ù;ÓÔqM\x001dÏPc_×¤×ÄìSß\x0017R§5u:ãC\x0016ÁÚé ÞÄ7qbë]\x001dÅIè¼ÎgL
RX7c·ðjj\x0011ë¯q÷Zsº¬©Ë\x0019S\x0013¿z15ER¨Zs\x000eþã2ê<IÃ\x000bã¼\x000fQ¹Ýº\x001bA\x001ep«\x000fÑ+o)¹\x000e{§#©ëã;¾°µ±&Ó{õ\x0012ØCp3Ñ/:e¦:ÏÐÎº´I÷ãÎ¬´iì!:Â©ðE#Ëó\x0005´\Öð¨Øqg>ä4ö\x0010\x001eáL|LNÇ\x0012\x0017µ©#Ñ
yï!ÌÀ8Só'éR$.ë÷?\x00155õÎ,¬ãØ%?Êúø&pÌ«Ã³ïüôåX!g)õÀµ\x0014ÞQÉ­91¬ó!s~òÊ«þÇ^½|»_9(Ì´f¦3ÌEuF<:~HkÔQG ¸§n9& ã\x001a:±tÞ¥[ô8ÅÔ"\x001d6êU©Ô\x001ceØ©þ»¤ð¦bG.\x000fX°SìÍ\x0016\x000f#µ\x001f¨ý\x0019ê E±\x001ehfWj]ÖåÉ«ÑãÔ8Ø\x001aÏØºñvÅ¿Þ)ÛX\x0015ûBcãèAì.$-
Î²\x001dYP»-¨HÌ*"6j?lGoßÉaâ©Q'\x001dB\x001cQ\x000c«±7õ©mØaX#áÌ\x001aá;&êû1¨±\x001dõýx\x001b	µÃ\x0019k×¬ìz)^¨S§v×\x0019;\x000eÆgÍªA°Qª\x000e3\x0017AèÊ~òâé8v\x001a°Ó\x0019ìr]V±E|.GÉâ¶\x0002¿yðØéÇ\x000eqÈÜ~ÊÈuÎ¥ó\x0019KGU'~²GY ú\x0002Ùìß4b\x000f»1Ù1Hù\x0011qzÝò'?JízÅ8N]\x0006cSÆ.¢ÅÉÕ\x00062	û;õS×Ö\x0013ÔÃÂ.g\x0016v
\x000f1
6èfÌ:h,o^O at×pÂ_×lµÃò.K)(\x001f\x000cºÃ~² ã8w\x001cR\x0011þø\x001b\x001e]¬ÖÄlu±:CSÔþuª©j»Ì^G,\x0005\x001e÷O\x0013°y
m°¥æwê8j-yµ¯Pi7ãø<íê¾i\x0019\x000ciµ­²\x0016©?©íqp[XÐÀê\x0007Vo5­cÖp\x0013\x0003iIW®Û­`ÀM\x0003n²6i\x0003:ãÊäºlKÇ½fÝ®W0T°ÎY7ÈÓEÝeðÐ*#ªuK_\x000c»7Ó\x0013¸4àÑºÙÉíÿb]¯N!nÝ½+é	Ü8àF«uH£\x0011\x000f«jW\x001b>õ\x0003 +×¬\x0005\x001aKFãº\x0000b;pEW}J\x000bJ¯\x0006ÜÁ1Õ1@W­gë:Y\x000b)ëAÕmDÌãúa§yëNã\x001b91®gÎ6÷\x000béµà\x0008á\x0011¢°ö¦ø\x0005rÀû¬óÊ2î>¢Là\x000ekÁ[×B5©Æ_ÌziáK?o »&Hø!Hxc(ûÒ%/ªHÕº\x0011\x0015wwbÙ\x0004îÜxkvIeMy1dY\x000c¥g7Å~ó´+=\x0012Î\x001bÑHK o$Ä£fÚtªú\x000f¡âð¢\x0016\x0006¯\x001b¬^\x0017Qb*®Ê¦TãBÇÝ«. \x001d"Z°F4,<\x001f¤Ñ¢¼	WÚ¢N\x00177\x0005	\x000c¸eÀ-v\9ö÷ÒOTÿ!§+vëIãÆaéFóÒÅ~æ¡¨!-¨ '/ÝkBZ\x001cNhÑxD[vZ\x0012ëF}$sêÄî\x000fc\x001d\x0016n´.ÜjO¯>Ç\x00036Ö\x001e~i·÷xvX·Ñºn\x001el3¥°\x0017B·íý1ìS¸iÈm5·ñNet\x0019×Ë³\x0012P¹\x001awp¹ÉêrkÌW0âþH]\x000cQþ¢3Z\x001a\x0016C2/$-9ÄòBY\x0017C÷¹þ¢\x0007'­NÌ\x0013×ÎªWhbu1¤_¸&Däa1dób(ýH\x0019ú=\x0000*®¿(\x0017ËCê­©£¯xÕ\x0014äµ¼?¼ørÑR\x0018oÅ¬c]®åf[¥@=ün²ÏÓáÌS¬g\x001e¯èÕ¶$ãBªm®{í±\x0013¸Ã>+Ö}\x0016¢^.\x001eÐjRÖWÂ5¬C¦P¬/Ò¾PM«\x0011ª=½zÜ°[!;;$\x000bÅ,\x0004\x001d½ZqAz\x0017ªqÆ³Ía~\x0006Ú!>\x0014k|`-ÙeÉé\x001baÀþF\x0018v\x0005\x001f\x000eã\x001b\x0005þhã·ÃzÂîÃ<i.\x0016¯9¬£×\x001a!êFÓd,ù¾ÓúKU¼Æ-\x001bïËõ.$¢íÖÅ\x001bõ=0Ü\x001eçÃE¸eÄµ®^Ö_ÓÕ{!\x0015eudqWoé8/«\x0017¬«·n1±n"=\x0000÷¾\x000b×÷Ñëùù¤â&êæ;è\x0010@Cäº\x0000aäµF\x0018D/EI\x0017oÐÕ®IÍ\x0001òkÍpbóÊ\x000bÒIXÍÛ\x001fÓâE¾\x0017Ç?´æ8u9d\x00159÷\x000b\x0000Ê»«\x00002#®5ÇÉØ×<YßêuÒ®lÜ\x0004k\x001cY­IC\x000e|ÛM+9NêOìé¬\x0001p|¨DëI"õ¡\x0008\ìâtéê
ºhåÒ¸\x0014È¼\x0014J7o\x001b\x0013ÝÌ\x001bºy7gk\x0019xÇ¬ÁüÆÇàÔós¹×­Ç`½Ëó×ÜÀx±\x000bæÝ¢CåÉ#vÏd\x0013¿\x0014_rXñª\x0014Ìw¥\x0019u\x000c.÷T\x0001>r\x000fåô\x001e´B÷ãåqýêÓþô¥þ#~=6O¯Bëð	Î³\x00187B ´¤vKZ¾zùöo¹\x0013âýþHyxÜ	\x0001yÝÿjàÆ\x0007éÉ,]`\x0005½<P¤\x001c7=­Ø´Æ¦3ØÁË=Tåî3ª1j\x0003zNÕ|Vn¿æög¸}V\x0015)ÏqÊ-½'<7v/îÍr5w8ÃKó\x001b·¦n	Óå\x001dw\x001dÈ,w\sÇSë$É\x0001Äûå½0uI©\x001c7óZ±Ó\x001a;Á®ñ0RÇî30vî+I^sç3Ü\c+Ø}ª-ö)Ô9ìjiÎb5v±cGÇÍÆùÆÝV	WtsïewÜ«³*ä¡\x001bÖ°-*@z>QÉø¨¢í°5d^¸-a'Âeµgke;YàÞß,~¡ÿ!\Â©xY\x000f\x0002"5äyxQk¬'ºÅ÷\x0012ÕYî!^ÂY
î{zê\x001a3¤¢¼Ë+ÃuÜC¼S\x0001³F¬ÜAeE\x0008TA).\x0004\x001f\x0002&Ë
\x0007\x0005\x0007¾e«FÇöÄ\x001c+ø\x00101áDÈ¬ÎtÂOô \x0006Gý®rÄ,÷\x00102áDÌ¬\x0006Ï]^$:\x0011@MZ¨\x0006å\x001eB&çþpCb¯Ø\x000ezMe÷\x0012o\x0016|\x0008p*jr©£øp´_BT\x0011Ü\x001d®1	CÔÄSQ3G©:÷\x001e¡[ÜIqiµøî<Yð!jâ©¨ØÓB>·\x0013\x000fÝÃé,ÌSQ'p¨FJ\x0002Ù\x0018ªþEv»e\x0003³àCØÄSa³Z¼HU;fµ¸z\x0015·[Á7\x000b>ÄM<wÐ$6s[* ª4Ø¥t²Û½\x0001\x0005\x001fâ&\2)k\x0015>Ó£5ÊnAÌ,ø\x00107ñÔQ\x0013µªºZÜ= \x000cÖÒ§Ä§D¹fÁÀ§\x0002'RÏÅ]àòÚfq<´\x000cÊ¹\x000e|xê´é¢ÎGñä»Å\x001a\x001cvf¹Àg\x0003§H\x0011Oô\x001a8UÄ(íöbLÓ\x0010èÜ©
\x001fHuvèÔ\x0014\x000bR\x0007¿poÒx[xÊ×V\x0016ÃîÅ	ú
¿p¡Ðà\x000béÔ­[Ñ\x0011Å,{ è\x0004YÅuò¦´{ð(têúª0E\x001e5órkzJ{!÷°1éÄÆ\ÆÏGñèzÐÌ}}raâéO½>ðuxì\x0019­ï×ázØ¼zØþÔ%¾\x000f=Ô×\x0018$EÑ±Fy·­v\x0016{ØþÔ®¤È\x001dÍ	\x001d¯îûÚÐ\x000fÛÒÚ\x0018\x001f2v¥Â¡ø\x0013ú+->ìKj_rKZ<è¸sDê©Õî(Ið0ìËpj_r\x000f6ö¥"\x0013«ûùì6eç¹\x001fÍ÷\Nù
ûÝÇ\x001f?ÿÊà?~ùëHAç{RªÛ3Nrf»\x0004ån\x0003ù»ç¯Þ¼gè7Ïß~ý4-®iÑHËû¯ÁÖ\x0013¦¨PNóCØ\x0014&7°Ò¬¬½Ò?.«\x001f!J\x0012÷GÎMÒú5­·ÑBÀÔLëùQÖAài6Ý}\x0012¤kÚh£­G+mbÌ5pËs°GM80Ü-¤ÍkÚl¤­ÇCÙcrO£Y*Ql{·*rÖ¶ÃìåÅ¾ü\x0003Ó¨GÃ6:êÁJ'oøH
\x001dî¶fïchoÎQûÕu¡\x0015|<¹K¼\x0019Þ/èõf¡Ñ\x000c]·\x0004
¾CÕÁMQe\x001bjÜ»ö\x001fN\x0003F\x001a\x0006B¿øøÛ/¿üüùo?ÿt(ÊÕÓÈ³UÛjQ\x0003»¶4rá÷È\x001d\x0011Ðç\x001fÞ½ûîÍ¾{½\x001bäÒã°±ÐÌÔòüYê±ÍÓ\x000c Õ#¥)vÅV§i
Lv`D5röQt\x0012£Qóî\x001bõ\x001c³_3û\x0013ÌYºµC.Yô£O"7X\x0000ã®Zó\x0014sX3\x0007;3Ü±/Å#QìdL´û80Ç\x001c×ÌÑÎÌÃ-\x0016æèjøk\x001e#ú,e.\x0005i÷¢`9­\x0019ëhñ¤\x001e»Î+ìJE5åß½\x0004cÎkæ|j\x000föõL\x000f$[PªTërÞ-ZC.käb7s
Ò0\x00122\x0007±²+\x0014\x0017w+r¦Wu-i#=Ë¬Á« ÚÈX\x000fòªX\x001cî^ÖÍ\x0011\x000fÁ\x0004ND\x0013\x000cÑ\x0016FrùA|Fë\ÂnË\x001có\x0010OàD@ÉYj®CÌ}`h\x0008RÒW\x0017øîóí\x001cô\x0010PàDD)À
ó\x000btuÔmaÔYrç²\x001døç_?}\x0019w!ÿÀ¼Dô]«ÆoFïºF¤@¸¸´ûÌ?¾ÎF\x0017tÍF-û\x0011ÊCóÔ9\x0004~\x0000`rR÷yì\x000f/Xß\x0000æ\x001e;y×Ê^üíÓßü\ýôÿü\x001fÿçóÏÿüÛ?ýôéË§'¡«Y®üsÝË¿Ï¾HW0Â/þôòÛWo*÷³×Ï¿ùæÃ«×¯_¾}yßàJ\x001e\x0007òx\x000blÛÓmFi.ðÜX-éôæ9Ë\x0008Nn
^?\x0000/õß§Ó¾³oºúÌ{³!Ü\x0008\x0007ð|
¼Z\x001cõA./uÅF	8\x0019Ê+åÖ\x0015ÌÜ\x001c|Ïp7µ\x001eÏÉunÜý@P¹qk[Ú¸×ãFlê$8FÆÆºÌC©ìòÆ_ê×Y\x001cÆ%\x000eg×xÔ«èP\x0013VÿÉÚ^r/V7,]hõ4zÄtÒ%Vgs\x001bØ\VK="l¥(Fî<úÃ|Ê!Öã¸>¸\x0004ÀÐî\x0017<ëÛÊ\x000e­§õ­c¤½äO{gØkþíCc×c\x000e¯\x00179N²xèuìx{Rdvþxj½8Û³àX\x001aLV\x000cÈH?Uº=ì'(%=÷8O­a¥²\x00079øäz»bÂã4\x0018oÒ^ÿø\x000b?\x0018\x001dÑÌæ|\ÄeYª¼\x001dâëúçÐÈ\x001aü;iÖëWïø­h'9Ç7h0Þ M±:\x0015YbòÖ\x000e[}cÊÊº{IrÖ¬ddM"²¿Èíg1«Ê}ðtîKPý\x001aÕ\x001bQUÿ5öÛ°ª\x0012õ!Ã5¨a\x001a¨:ºÀ±\x000e¢z]¬q·Râ8j\£F\x001bjÊ:¯À\x0005hW u­ú¾\x0000®!MkÒd6ª´½:Êr÷ÁVUÔ¸é´æYó5ÛX#é\x0003¡«pNÌêc_\x0001ñÅZÖ¬Å¾¯Äµ\x0012¶ùÕ¼¯¤8ì\x000b\x0014\x001dF½]Á£\x000b°\x0019Ö\x001a¸D\x0018ÁQ\x0010¡ªâ@Õ\x0001CØmx9\x000e;,cÌJ]x\x001aX6ªpØ,;\x000e;Ä\x00010\x0006¨7ÎÕ²À\x0003Í\x0017Ø@Ý²aï\x0006æ8ìà^Áè_k\x0000Èþñõ\x0004}É^³
\x0006¯\x0005F·Å:ê¶Ü\x0017W@NÝVð{×Ça\x0007W\x0000F_àQ_Wy¬\x0014e¡DÝ½Íz\x001a¶\x001fWãà:%|þÛ_~ûçß\x000eKI\x0007²Ne\x001b¼ }9¢ç\x001f¾úðÍýÂ!|\ëp
5ju\x000bRSIU°!¤]íã¨´F%\x001b*:Õ
fÔD*Ê¬¨{©ëqR¿&õöï¿gÙ¢ýæó-ËÞ\x001d®y\x001c5¬QÑ¨Ø¿ÿ¨ÃK«QUH-ä]Mùã¬qÍ\x001a¬^\x0017\x0000p\x000b ª8Näú¼+PÓ\x001a5\x0019Q£ïºtçR².Öí«yÖ²f-6ÖJ$jdO\x0007¢9ÄêüÍ®nWÛâ0+ÕèZÉó©®\x0001\x0011qj×»\x0002\x000bÇY\x0007\x0005Få\x0003\x0007ÕÕkgQ5¬Æ\x0018NÆ\x0001t~\x000cYÈÞk5ê·gßþø×\x001f\x000f &\x001eÄ¤\ì/uè\x0019;iÍ%Ð'Q}xöí«¯_=
JkP2R\x0017ÛJÚ'Ó¢\x000ei\x0008nsÀ4¨_z\x000bhÌN\x001c+XA!«@tpE®Ó¤aM\x001a¬ß½/?yØ­_¾ú*·éW§Iã4lÊï=òåÇ¤Â~ètvbTîS¤\x001eõ\x001c@\x001a{\x000e^ü·ÿzdógÛiõH¹\x001eï¯b=fë9ÛÓæCÏWÿðüÍ×{_`c\Ã®ø§`³ô@"OðI©Á&y\x001dáçîÝKÃ°iMFXA-\x0015Ö=P\x0010Ëªè\x000f»ó¦\x000eÃf\Ã®×§`õ¤<÷\x0002@`³.¸9át\x001evX³Ù¸fY-1\x000bln\x0003*,WÁ\x0008ìn}\x0018¶ø5lñFËêH\x0019,|éVÄ²ª\x0011ïÓ®àÅQXpeN}\x000bm=nyjz(¶_\x000cø|É¢õ\x0015!ÓfãBpr3¬\x0012îÄyùÜiw\x000b\x0013\x000fÓ"\x000c´k\x0019Ú¨\x0016È"á\x000cT¥Å|\x000b\x000b»\x0017DiýHk\·I\x000c\x001bÝ¬YºÁÊþ%ÆQR?¸.þh"
QÔ'kb@­t¹Òj\x001fkM\x000cò\x0015î\x0000Æx\x000bÖësV£u,>´Ðº~?°+`~\x00186°Á
ëxªEKc±M;JÒÛ,Ø¿'<L;º`t\x0007<2BhkúÚ¼\x0010d\x0005¤KL\x001bGØhõ:'\x0000yÀ.yY\x0007wãþ£ÁQØ4º®dt]ÞL\x0016rù.¬Ë`,ÚÓ°nùµ\x0008\x000fG¡Ä÷×?Õ<ü@ö!ªP\x0013¸Ô®¶YI9ÃþõËçï¿®yøÓ¬e`-6Ö~§á]BQ#ÉÅ°Éï?t\x001fõ\x0003¬7Â¢>\x001dÕUê¥Ý"S=ëeÝî¥ÆaØ8ÀF#,\x0004y­®UK\x0008ê2PÍÅ\x0000»¹aÓ\x0000¬°ÀÉË²dë¹F\x000cëµu³ús¬Þáx`ô<hmu
o=dúí/¾üzÄ\x001d\x0010²\j¡ÅvZ`?\x0015qÛ|Õ\x0003nk#ûÓ¯^¾}ÿ$tÈkh\x000cVh·H.4iE\x0019ÑS¡©\x0018ÄÍz\x0013ttkèúÉ
MÁs\x0011`\tÝB¹«ân¶°Øq\x0000F;0W-\x0000\x001e$\x0011Uí§2ï]ÑMA¯Ë\x0017qèf^\x001a §__ÓFÍÉÈ;ÞV³2Aai\x0013K#:-rõõ`Y²¬¾	q3I·@¯\x000e@¾½æÙM]1T\x0011]\x0007ª\x0006JÞì4Q»\x0010ÎlCr2ª£Ú;Iµup]hS\x0008×FFêtb$9jøåOeèìÝ
½9}ÈBM4Ä\x0016þh¥"Cr<ºV\x00109¶Êª°y\x001fiaë¶ºû!ZSÉ®çq¹HÉZUS³ÍÔh\x001aèq1(õbÐ?}úéÇ¤\x001a@ûêß
R\x00041he\x001dm·#p®ñ§¯_}·wâ Ç\x0005 Ô\x000b@óyè÷ÑA\x00053jÉ|÷Ì£|´æ£Y>¾wn
9ÊeCåë÷cîîýØQ<¿Æó³x½%ºâ¡\x000e3¯JïÜ]Õ££|aÍ\x0017fù\\x00107Ì·ùm:`¬&ë÷RÝ£|qÍ\x0017§·\x0007I]\x0014.cìu{èä:Þ»Q<ÊÖ|iÚ~¹oß\x001c\x001fb\x0014ûõ«ïíºó\x0019¾¼æË³|AFpUóyÑz¬\x0019×\x0007ûêÎGñÊ\x001a¯\x0018v¯¯8¯óÝúö »Ý¿\x0007ùVEt+Ò<\x000e|¿Âª´¸\x0017rý\x001dÆß=¶\x001e\x0005\x001cÃÇtüày9ú
ÇvmÅÅ7)ô
rï	î(à\x0010?`:\x0014=K/_qÃ´\x0016
ùûã¤ò
ñ\x0003¦\x0003\x0008Ï»V\x0003\x0016È1ô7Ì³;\x0018\x0006\x000f
Ó.:\x001daAò¥Êúô\x001bëQ¾Á\x0003Â´\x000bL©_¢ÓA÷\x0004º\x0001Oºh\x0018Ôvd\x0015jóÿÿ\x000bñ/Ò)|ÜÄó?üðã'n`zöÍÇ\x0003=L¬^ÔëÔ\x0016õ¢(êEH»êE?¼zÉmKÏ¾y¾×¹\x0010\x001eÕüð²Û±ß}ËÅIG2ë#M¿XOaRòS°Hwø¢atïnìÃ³o¹2i'¥VJ\S¢29ieÃ¼4­/ä¢l\x001aÚ)¥<NIkJ2P\x0006;ÑJ©Õ~\x0005³º\x001eVr9O\x0019ÖÁ@éQÎR5íg)L(µ¾\x001eî¿\x001d§LkÊd ¤ÐÏ)1J"[0RO´ï× \x001c§µ#j;¨\x000b-L´\x0004wÝDE+è1kÚS³\x001e»Iÿ÷¦Q\x0006}2ùÿ¶TÒóYo°äÛðÏ\x001f:â6ëß!\x0013=Ô\x000c<5MËUx½\x000cß\x001c\x0005Ö;+ù>üÍó×+÷9rb\x001e_8ù£Ó'î\x0007®¢mA»Wyã=ç@\x0013'gín\x0013<ªüzÐ×ÆÖB=ÎÙ¥\x0012\x001aç 0Á-/Üð!úNçMø§1\x001dE\x0018½gýÁº´ÿýÏ¿}ùõÓO?\x001dS+)õÓ^\x0017cu§I´b£\x0014\x001bäe0åý·÷ß}xûþåÛ¯wuV\x0014¹¬Ë	dßêü}µ³ª\x0014ö+ìv»þ¦q02±2©HIlwkYBUvD{éSÐ4®3Ð(Y¥O:@¹öï*æàÖÌÁÙ94´õ\yè\x0003#Q÷Û\x0001§S\3§hgæù\x0017bæ$w4	µ:©ÚywLÀ\x000c3Ü\x000e£Ì\x000ck
¯IèEDÄÐN\x0015o¡¤ni¸ÊÒ@ã\x0000:á:°0êbë\x0014»46ÉÓ4k_µ¦!¶\x000e'lIô\x0003*u£W\x0002ò,Ô×­\x0018\x0006ê\x0018NØ\x001aEf±R{¹ZI(/c\x0015z·Çm
º\x000cî?ÚuÐ\x0001z\x0011Wx[Ö\x001a¶ëúÞ+É>H\x001d\x001eS¦0S~ÿ·O_þ~¨×\x0005ø=½µg5Ë¨9¥<Ô¸ý\x0011¢ïÿôòí·GHqM&Ò2ñ¹&«¼MÖpªßÜî\x001a>JJkR2Bd\x001dS&H\{µdì,|ÑHóÝ\x000b)R¿&õ&Ò¥\x0004¤.{mx­6%¹ñp»e­AÃ\x001a4@\x001dÝ@½Nw¬;,)è¦¬Ï4i\FÛ2\x00059®Õ/\x001fDÿ¤T§ô¹|÷=q4­IÔÕý\x001e£zétJ>\x0004êËô­×¤ÙºLsê¤ [_½»¼ü\x001e$½=U,îÔÙü©¶bðÝ\x0002ßË6ª\x0013°\x0010o<:z~ëwäûJÀcÒ\x0017Yü¤3awDíaÒÁóÍõ×ü¶MqçûÍ\x0007ÙüÅë*á\x0012\x000eþ\x0014l\x000e\x0015¶Æ~ï©*=	Üî´Ã \x0002r<WY¶/:¨ÝSî¨w§cL¡\x000e\x001fL»EøþtJ\x0014\x0015MQ\x0000÷êâ°ùÑ´ùYDÈÉ:Ò4Æ;J\x0007\x0001Þ\x001dæ2:&S¦-å0<\x0008)·´##¿Ì(é~ný\x0014)ÆG\x001e\x0015ãÚ£>ûéã³ï¿|üëW\x0014B0ä²(³`{åEPæ.é³×Ï}ÿöù×/ï\x0008á
&
dÂ\x0005$F¡wé¡´·\x0004\x001fQ9ËÎTÇ\x001bçS\x0016
\x0003j0¡Ö\x0013äü\x0015Tö*8¹Q®¨;\x0017`\x0007Mz\x001bê´pÓÔ×£g¹ö¤à»<\x0017ß\x0007·h\x001eH³´ºý\x001c\x001aiÒKÐâ³Þ¹°\x0013¡Y\x0014pÜKhûêY=°½ÁzZÄÏ¯Çõ4PÜ	ú\x0007Ao½\x0015\x000bè­¹b
4v*\x0006ú~\x0018z\x0017výÖî{ÒÃß=«\x0014Ë´WVÖr³©\x0008\x0003WÖf 6½ÕÀ. ·\x000eì)Pn«j.*p-Ml ¹ ^° _4}ý\x0019H\x001ei¸Fõ\x000eyJn¨\x001d\x0015Áã¬·îëõÖ~=Ë*½¡\x0001PR©ÂïaÂZv:\x0018'XÇ%MK cëKôYË
K$RÖ¸3Ùï0+â°\x0006\x0010mk xe
\x0004­2¾²jÏ-¸%ÇQo\x001d\x000bêíµã\x0004jN¿C=âþBõ·BoòV¹z+ì¤(\x000b@G®VÔt6\x0000à£ -Iá"õqG\x0015%å¢\x0007W*§9G{Ú¼NÕå÷'R½ÛX´Ò\x0005¶E§@Ó¸i;±2\x00177\x0015QQ%\x0005ÐP\x000fÙ;
¶\x0007A³\x001f@³7YÔÅv4ÁÐ\x0012ÕÅ NeBêÉô\x0002\x0017åý°Hùã<jMB\x0004Ô¾etËû\x0006
éþMßS\x0006uîÑ½9ß£­ºÐDÒêÓ¿üøùPÃ²ó×&Ã¦ê¬ÚMoa©w©xÙ®3ï\x0012<M×êå÷¯Þì¶-»G7ÓLíÏPç\x00071qjUPZk±l*\x0019\x0018©ã: ê\x0004kX¡ÈQ\x0000Óæª0"ç5r>\x001c\x001eÚp\x000b\x001e4ÊGF­^\x000cãf\x001bz5¸Êµ[\x0013Áç\x0015»ëá\x0016×úí¯[\x001f0ìE8³\x0019£Sq¡ÈÃg`kÓ\x000cn+ãNb{xô åayÐúþ§ÿÔÿøóç_?\x001eb\x000e9óp\x0002y®ÏK\x0005\x0015\x000bücõ ò\x001a7¿ýüE#þãwoÞ?\x001f\x001fÞê´km¨<¾º½vgê3CªY\x0004-3¨·èÁ¨\x001c<¨\x001etOzhCHGÊøÍP7\x0003\x0006&»M¹¤¯Õ\x001f\x0015¾ÞjÓo\x0008t®Fõogm\x0007ÔlGe|\x0019ÔÃ
nm¥×Ñ+7oa'Pá\x0016*Êç;#kH¢ísâÎÊ\x001a´0\x0003Òfwß!V\x0017`,\x0012X.å\x0006ý¾\x0017\x001fÿþ/Ïþøåãç:peÌí$²õÈ\x001bDÇ×ÉjåAº{NëÃ³\x0017Ï¿ýþÙ\x001fß>óbÇ×
4®¡ñ\x001ct×
\x000fY4}µG÷Úg'©iMM'¨\x0001ä<Iü¢\x0004Ò*\x0011´:âæéÇHí×Ôþ\x000cu^Ëjkà\x0002ë¦¢a-ÂæXF#uXS\x0013Ô\x000eu9°P±häk.\ÕqÍ\x001cÏXºC[­Ø-½÷ÌQ§5u²Sóý£L/òDÂR\x0002ê@âæK:¯©ó¹õ!/ú¬\¬ëCOywÐe
]N:g\x001dy\x000f¤b¢Æ=*ÝÔ{Ú.sÔ«|#;³Bb÷{¨w\x0014ux5öæí¤z\x00081p"Æp>,#DRolë#\x000eXvñ:ìÁ[Ã	w\x0012Î²\x001dÕØÚ\x0003SÈfÑAj*ºë\x000fÊýûUo[^üü÷¿\x001c¹mñEgùÄÏ×" \x001bJ?lß\x000c}÷á½^¹¼øîÛ¯vîvõÀ^J{`7à\x0006\x0016±JPVº\x0014õ½\x0014µÀ¶\x001b¦qoÜ\x0018gp{c¡>©\x001agðýwGÚp\x001e7\x000f¸Ù[c\x0008\x0013øzVëF[Ê\x001dIÎY\ ÁºüÑÆ[OM¢¿Æ\x0005Ø\x0016/Ïb\x0017ó¦íW¢iÞ\x0002\x0003/·+x\x0013\x000ezÝlIy«Ný¼\x0005.WÄ¬÷\x001a\x00197[ä+\x0015í&XÚx\x0017ÜHZá\x001e·ÇÎMó\x0006?ð\x0006oäm#Àµ"¿©úð\x0004mÙØn~Æ-Ãfã6Üâ¥®Íó\x001cp×VCr½Åd[\x0015Æ@Á\x001fM¼)Dí©Mtk±¯1¯a³-_\x0005óyiâW9hæÍ"b
l\x0017äLãÞ®­\x0016ÜåÑÃdÝ®þÅ´\x0012SÛb~jÚ|JçÅ×è\x001c¸¿¨ÍÎó!\x0006õe	¤(\x0015¿Ýç=ÏëG^«sð±/[õCõ\x000e]ÿ²\x0004}ÇÌÁ:TP¾{_x¹\b±ÜV¤Âr«Wàq9\x0004ër(oaÞ\x0017§úØ´L·®ïKòHFïÞ¶B
ÉðdÅÅ;È#GÅõ\x0017áÒKFÜUûÍÇÜjK#÷¼ÈnË·@Ó¸Á\x000fÖ
ÞjÝäùívÁuEç\x0011d§*¨ü{\x0005î¸\x0018u1ðãDb*é¡­Ý\x001cI\x001779çió°\x0016ø£Í¸\x001c\x001eq%Ph7ÄR}p\x0001nÄ!ÍáFÏàØÛ6\è
µ*¾ò\x001eËz·\x001fõ\x0005Ö\x000f¶å6Xr2¦ÝSõhr`KAîxRíz¾iã+7Ý\x0018ê\x00080Õ/@Ûh½9"nW\x001f§\x0005|,Ã\x0000Û?~ùÿûÐûl\x000c2\x0007ÕA¨õøU\x0007(íÎOøãÛ»ï²Ây[\x0005ÌéÉ\x0002JEµ,¨¸ SµRîÝD»ÃÆ4ÚLE\x001erìC \x00175ëFºWÆ4
¤ÉBê¹R¦æÀoI³~ùw\x0005#'@o¥g\x000c\x001aÀdRì¹x©Ù¨G\x001bí4¦¥þê4é°Liôâ?g§"õpª6]=÷£¤a 
&Ò\x001aR0PµiR¹A×;xvGÂ?EêÂã\x0001°\x0001WòZ|}ûß\x000e^ß&\x0002.õ|5nÉB­G®Ì	nG¼êØóãÉªá6YuV\x0017k=\x001b\x0007ÕºãêTï\x0016õÍÁÆ5l4Â²*¦ÆF\x001d®ÊjYÝ/A£ÍkÚl¢%GhÍ<Z±½õ°D.»\x0012­s´ëw\x001e¼usÍâÖ<Pjú-&¸\x001et\x000c\x001cÝ/AÃ\x0001\x0017¸5\x0015qÅ\x0010ÚÙg&\x0015WÌ÷ãÖ@{§ÌSP-\x0006¶=¶\x000cZ\x0016PôÚ×ö\x0011:{:q3
\x0003m0ÒÒr\x000b\x001eÿ_æÞ.»®äÆó
'P\ñý±òRÒ²¼$RE¹ÚõâÅÌdeê^¥dSbvÙO=A÷FÍ¤Gr\x0008 NÄÑ>ûÄÆ¡«õ`¶K?bG \x0010\x0008à\x000f\x001a©U[ú×\N\x0002WÝå³Ûp\x0007 e>!d|û¥9æÊa)\1nd\x000fæW$T¶áÆ\x00017J×B¦|¸A-ö\x001a\x001cÀÿÈ´©Zëü·á\x000e.L\x000b}\x0018\x0005ôÈ'\x0005³vm¤ýò{µ\x00007\x000f¸Yj]NK7k\x001eüSÀUZ}8ìÞDk\x0006k\x001e\x0017U#»\x0001ì®á\x001bvp¸FêpÁ¶7ZØ\x0019\x0005N½=Üö¹
wÂda\x0018\x000eðà)ÜÚq½7\\x001bM\x001b\x0016}X0l\x001b®\x001dp­Ðº:·¡á:p°P|-Y÷¼®\x00194#<ÒõäÆ¬:M,\x001a\x001cVÕn·à\x000e^×\x0008½ncjÉTt|Ë(çÂåÃZ\x0005Ûp\x00077fn,ü\x000bªë\x0004Úg;Á~"ÓÚÁ-X¡[5J£­Nº\x0001aµ"¬ÆÙaYá>K(}XqèFs±,U×Ä|ÇFëö¸dáN\x0013w#uW6yJ»kRâXyøDwÊ}j'àÈY?EË#4æ¶æÿ4wË}è ¶tÎ\x001e³\x000b
â³ÄMãnE}g\x001b´Ù6rK#ZecÄGÎ8ð(°\\x0004°Y?ºu¼Ïï\x00129\x0017\x001fÿóÿöi*\x0013
Îº¤¨ÇE^\x0016\x0018\x0002sH¹üTB©«Ë××GÚÂ^2\x0007¥÷¥°\x0016kÓ\x000b,ê2\x0010,¿ø\x0006¿.;:\x000fk{X+µ<Ã¢­¾
LÛ`WÅcæa]\x000fëäË\x001c±ÂAîA]l[Ø\x000eë{X/Õi\x0007Û²äà\x0014r]KéÎÃ\x001e6Ha\x0015Õ7ZtÁ4Z)yêÐöëê¾ó¬±grÃÖ
\x0010`Õ<\x0007|\x0017\x001bÖ-oM=lÂúæ\x000c´«ÕK\x0008Ë\x00192ÑOó\&ÑÍ\x001aÔªïû\x0019ñ]ïæÓß\x001egÆf\x0018M"r1²/¹Õë\x001dø°wsý¯·k\x001dÛy/k¸Fm@¤|2\x0005Ñ7=}íV\x0007rn"¶=±\x0013»sW×\x0003JR×\x001f@Ìõ:,fúEÄ®'vRb5M ·!Z.\x0008ÄQ³¼[ÔºØ÷Ä^L3+\x001cÙûÄð-Þ'µ_à»8ôÄAL\x001c5^+*±fá}ðº,ç\x0017Û\x001cEÄ±'bâ¤xU`¡!b~\x0002eüd&N=p\x0012\x0003û@ZÎeã)ÃbmQ,&K6\x0011ë\x0010G_\´\x0018Å«»ßî\x001e¾¼ÿ8ë\à²Aðl\x0011]\x0006¦9\x0015+^Õwz}qóîåÕ\x0004ªéQ\x0008\x0015gÚP¢\x0004«ñjÖÌ{¥e×Å}¦YmÏjefÍöP!å\x000cïÚi±®F2
ê{P/3ªÖT\x001f\x001e¯Á!°LîrûåvÔÐ£\x0006\x0011jØ)e¥ûPQW"-¨±G2«ZCïXùÓ¾Êíô}¢¥zÖ$4«åüMLÎ]\x000f~+\x000egB¶ v3\x001dÑY)\x0019«óÜëpp\x000c±r7h4k*é\x001b`í°\x0006¬l\x0011`·dXêî\x0005Vñz5kUA3°&Û\x0002Û\x001d\ö;Û] n>\x0001íû3ò"\x000eû\x00119O£¹û\x0001Kõ9Osx¬\x0019Ü\x001fn®öåÕêýÁEL\x0008Û\x00171m¥ñA&fÓäZ'³u+Nk\x0003ënô9²\x0006%c\x001b\x000eM08»N=w¥©¬;<6l\x000bl\x000c=l\x000cbX«Vã\x000c£]ù1\x000f\x0007Ø,\\x0005Ç Çhj\x0018.\x0003.\x000f2ËÝ[[YÓ`Ø$4,°êZf\x0011Ým¯6ÛP¯æêfa\x001b¶WpÒý¥ûIÞÒ2`=*WSJGi4Z
7Çgð\x000fðæøæáîËÙ\x0015`\x001ceô>rÛ·Çé\x000eui\x0000¬Ýe).[on.Þ]Á¿il#ný	ÜB1/×\x0015¼VUÅ#Í.Ô\x0010ÅÇ\x001aU­øÙCr#ÛôÏ2TSl¬T¨Øø-PéJ\x001bTv¤²ß\x0006\x001f©ü·@eôà\x0014ðÇÿTØ]:ÞµK»é¨ãvóéñûÏÿröâÓÃ/s\x0003ç6\x000c¼W17¸kQ1P\,Âî¥Ün®o_Àÿyq}óbUüàm\x000foO÷ôÇ\x001cü\x001aÔé -ÏTJ£­O=|<\x0015\x001e+¨\x000f¢ÈïcZÌé@{ú|*½,¨çâQ!*·6¹¸XÐ Ç×ã²?yÝõ
5Õª¡&Y¿µ%.êÉÀ?¬|}òÒ·÷-&NtÔ£âµ\x0016¯t'ðûßÊï\x0014n¨ö·X\x001bSù½gû/^FNà\x001f6¯>y÷ºxNn3z\x000c´ªëáqÁéØ\x0013Á4¾Ù×Á3U\x0007é7÷\x000f¿ßüé×©·9Íé!Ñ\x0019\x0016%×©='°\x0016N¿¹¼ùáòêù\x001fgxMÏk¤¼>s
\x001b« jÙrÖ<ë6¬>{n¡µ=­\x0015Ó\x0006~!PX¨hÖr\x0005»óOe]×ó:1¯­S*À¸\äµÏ­ÄÄ­Ý\x0004·àú\x001e×KqÆñ\x0014µ´6\x0003 ·ñÚe\x001f\x0001oèy\x0017'S\x0011ïn\x0002ö4¡\x000c"Ä'Ûl±çâå ¹FQµqÀ\x001b¹$bQKPzÜ$6¯=çú
]í²v
Ö­-ÙF{Ú,¦Å*\x00082®¦h\x000fx}jÆ]Ë\x0011màÕãI!>*0\x0019Ïì	[´
°um·­<\x001dm\x0003\x001e¯\x0016{_\x0013(½Y,h»V×eW^:¶\x0001\x000fîLý±ÜT2ÙÀnY`m\x0003¯3ølB[\x0011\x000e_­ÑK>ÿõþ·÷\x001féAù\x000f¿M
\x000c°:±°+Ün5=z È\x0004é>¥rGþ
\x0019 _¿¼¢\x0007å?Ü¾^\x001dpÀÌvd¶Rf@¢ö\x0011ï3Ï7¥@2vÉ-6ïýìÅÈ.Q;\x0011¾)R¥ªM\x000ep4Ë\x00131Ç9ñ\x0002hid(U¹\x000eÆb\x001b§9ÌY¾4èñ\x0006\x001fÄ©±\x0008V\x0006gHc^, ç0 £Ø¸t\x0007ÆsCfV®Ýx[ÊÄ¼<é@ÀlwÏ¤È?J\x0003û9ï²£â$ÛF·¤è\x0017õÁDÌfd6bfÎµ©Ìpg*\x000f{\x001eë\x0012ØÎOä4ì®w¶\x0012;ùÊð4\x0016Ñc\ÏÄ\x001e¡RÔO´ÿ¬\x001d|\x0006þ(ÝFÑD7X\x0018*±±;ÊóÂX\x000c1$Ì£Ï°bap\x0003Ò\x0011¨r</' ñUQmZ,ý\x0010 »qÿ9ùþÃJçúâç.\x0013G5é\x0001¤\x0016\x001b\x001f$Ì~8µñG!³\x0008ÎÏðÚ\x001flvmÿéÅéÞ"f?2m1²ÍÌ\x0014hdOÄhæ'C#²x\x0007Z8\x0001«¬+Æ\x00174ò\x0017ÌÌ;0<Õ\x0006t>ÈâC\x001bù4±>PU£ÍQñj^¬ q\x0003\x0006ù\x0006tªs\x00019fM]3Ix*f32Ë\x000f@pnV%Á_`æ\x000eü\x0014ôâ0p\x0011³\x001bÅG Á\x0019qÕÎ&YJ`Øä4-
¦9Ìâ\x000eãæZàà­|lCÈÎi|\x0001²\x001fÏ\x0013Âyxþ·Ê6G§¨4'ùå§\x0007	³\x001dn®ø£Ôk8O­IðÿÄQ6Ãæ\x0014y±èEìÕ?}s¢
y0sØ'$P£ÿ©ÓÈÄÌµ\x001a¼ÁêérH´½[\x0014k0çq9çsí\x0001òÆZ\x0016W3½Ó{u:³va¯LÞý§û?Ý=ü<U\x0014y.aY\x0016\x001d\x000f
`âcOOº¸ù~µxïy\x0017\x0003GÕ2áÊ,×M|Æ\x001f{¨&\x0003qüöí@lÅÄ¨\x0014^\x000b½MÆ¤¶µjÅO{Î\x001f-å`äe±'æM\x0003o:V1¶cÍ»8#};o\x001ex³xEdO\x0013}q¯]*±sGë\x001d¦pêq\x0012ãB8O"p¨ý\x0014\x001dI\x0001\x001aÇ:e\x0013ï¶ó\x000e.ÍÉ}ZÌçD\x0014\x000bW&\x0015}íb½ïv^3ð\x001a¹\x000fæÇ=à-\x0005ëä!xùÚxlvç\x001c¯\x001dx­×{\x001eó±»¦n7ey®sÓ\x001em×
¼NÎ\x001bÎÙY\x001a[¥,÷\x0000nSháäÜo¿tåaºS\x0006í³³UÚ§ªn\x0006.ÅÆ>EkªZïuÙíQ¦ØSâ>`\x001aoéUÁ©\x0008wèZ²óQ*¦K¯
ÓºoÈU ´\x0013\x001c)É\x0017g¬O¨íÂÉ\x0006Ö0MË\x0002ZóyÄÌÂ¯\x001c\x000b}åd¸å6iM\x0005L`äcâàëzXZ\x000bW§C\x0005ZèdOn
vÆ->ëOsZ5pZ%ä´\x001fÈQò´ £lÎåÚiLç\x0006Ìýá\x0016Ó(æ\x0008SÓ£QLÉ5Îå9ô³ÝD!äüj¢Ð4g4\\x001f¨£XÌ¦-Ï|S2qäRNØ;4Ü¤ÌÌ«Û'	EoNæ1Ý)üì8(\x0006\x001eápÐ@Ç½f\x0011\x0003¿øº²\x00013AY;K_\x0015ÕQ\x0000Í©eÆæ9ÓÈd°x&
ªÎ¶wÑñYxëãi¤g¦Eé%\x0012ýw\x001a½cl=É¨\x0008~
§µÃa?w\x0011U3\x0017Å \x0012S·|PÑþ<§\x001bÎv»?­d\x0013ÅÎh·§LB6øFÉÛ(\x001f\x001dÄuÓVÎYårËw·Ì4÷|"§\x001f9¥;|w)i4w÷Ãw§¨>rÎÉ9]\x001aìéö\x0007©Lû%\x001có[¿»ÅÂõzjæ¦C\x0010Í²þ,§7Ã~/¢X²Ó=ÑS)ª^rOFJ¿¿,B1Íé}ä½p\x001fy¬Ïä©?Gc\x000e\x001c$ÇtZP\x001b²çÒõ\x0019Ûà=ÜR\x0010nqQ"/_c\x000eÍÌ8úx/õñ.æÖ\x0001e|\x001dømÒi×¢ \x0007ÌR#úäFQõ³sÁÑøé#\x000f÷INº4á\x000cÛë+åþÖ\x000fïïßøpöâîa\x0006\x0017|\x001c.Ë*±f	q-ßà£QG²Ô\x0008üÃËË¯à?}qq³6çøMÏÿÀÖ6~sjº\x0019(\x0018Hü&³>QZT!8ßöü_Émmµ¿÷T@£Î}]Õ6óµÏèÅ\x0008ë\x0014~×ó%¾µ?ñ	\x000cØñÉæx6¬ÅûË)ü¾çÿJk³ý#)¤Úd¸ø\x001fn×ÿ\Ô6þÐó%Ì%X?,qäÛ	ã\x0014ëè¼ø*v
ìù¿éÚÊ\x001f#ÃÙ¤=½Fg¸¯Õ\x001cË nçO=ÿWª][ùCÜI\x000c\x0005v÷NsÁ¨Eá\x0013øwõ\x0001Åÿ«\x0013\x0001­¸R\x0015ç\x0001SÕYt¡\x001d\x0000Î/=_K~\x0001cÔ^\x001cN\x001eØUå¿þû§Ï¾¼©ÉÇ¦m\x0012òÀ,yí7³UA
æ£\x000e×ä¿þóõÛëw/×:\x0008\x0008Õô¨F\x0017\x0013b5ôè2\x0010Ò;°IOÄj{V+cÅl~ »rux6_KL\6ÏêzV'c5r(`WC'!:°«]ëËgõ=«\x0017®ÀsRÀ#Ð½?³Â\x001f*¼¬uÄÍ£\x001e5ÈPµ£b_£\x001fë\x0003T6ò\x0001³®6sÎ³Æ5ÊX1\x0017ÍfÕô¸\x0007K óÖqM)i5õ¬IÆ
÷?Åvµ@Í'å´Úõ4{Ô,ÜY\x0006\x000f²jVÏ½\x0005Õ%Ïf]U\x0006fÝdå P"Ø2«Ö
JÍF\x0005Í\x0007Ôm\x001dO-á±¥8Ú\x0004Ë\x0006nÖ3&·Íõ4\x001d\x0002-;\x000b\nií³Ñ®\x001d[+Ây~r@=\x000eÚäÖ\x000bH0»u[·\x0018¶E¶u»ÖÈ»!*ØG6bäH^\x0001
	[C Z Nó`:íW´¥aÖÁ«O\x000fï?}S²0\x0014\x001b8\x0003~·JÜGÿÃ4§v\x0000ê«ë×ï&HMOj$¤Ñò°$E5â
9s:+ÄEµðÍ¤¶'µ"ºL·7Úñå)RË\x000b/'µ¶ºÔlu)D\x001a
?÷+C]\x00131Å{ÚfRßzMájØ¦D4£|£\x001bÏ|ýÐ\x0006MCàÇJ\x0013x:K,[tY
|3iêI´J;\x0016Ò:B1*Gý1¸Õ	À³Ü+º(%âÌ¶
ÿFáúíUhûÉ®NF\x001d|\x00169©ä5Íµp\x001asu:®£ðù)>½\x001e6¾\x0016íüäÛ@u\x0014Ügå1çÛ[àª´ãQTeösÊ¿]VãíÝû_þåÙýÃÇ»g\x0012\x001aÎpB\x0003µ^iâÙÊ\x0006Só\x0019o/^^½;{vysuqóýqhÓC\x0013 #·ã#ÛN´Þs\x001a\x000cUÚöÔö\x0004jëvÉ/ÏÊõ.ó3Qk©£Ð®v'@ûD\x0017\x0006Yª¹\x0015çø¬¥ë6"û\x001eÙ3ØI\x0017Ú\x0005\x001ab\x000b7\x001f«9É»ø\x001c/¤\x000e=u8e#rñEeÓZÚ\x001c½6,½­\x0016\x000fb!uì©£Zaë;QcDN\x000f\x0002¬d\x000bÄbç¾:õÔé\x0004[cÖüö< ÇÅ6@`¹CTFÝMèFW­NÀÆ÷ÐM%¹.¸Ôý\x0004\x000b\x001bÜÐ^ÞY
Òl¯ÿó¾û8¥'\x0017TÈT¯ï¬Q-]®©Û+Fµ~Ç¼|{qµ®#§öuÙÔ Ë¶
ÖÔ³5UV\x001føq\x000e\x001cÇêír\x001aÖö°VnÙL5\x001dø&\x0011Ù²\x001c»åÅJýí°®uRXz/\x0005V[.ärM\x00144®'¦Y}Ïê¬\x0010Pd
s»d:øê¶2\x0002}\x0013lèaÜ°ÊÑ*0¤5\x0011Ûtp ðl3kìY£Ô°­dÛdEú?(\x0017Å÷·´Øã¾\x001d6õ°I\x0008V)}Ù\x0011PÇ5®ÞÞçIsO¤©UÐÔÞÙ¦Ë]Iõx\x0018HO\x0003¸\x0017ó
>ò$[ÜZkëIÒiÚÁÁj±u\5´k\x0005¸ª3¬JñÍÃ\x000eNKK½§æY\\x0004¬;­&m\x001d<ÉÞÒ#ÐRO`cËã%j\x0010«s\x0019j\Mã\x001d\x0013vïGne½øðï\x000f÷?ããÿëGÁ¾\x001cÇÅê
îMÑÕ+²×s\x000f&\x001f\x001c-qñê\x000f7ßã«ÿë[ÀÞ\x001dG6=²9\x0001+)-%$
³çy°H\x000ex;³íí	Ì\x000eá¥5\x000cvæ«\x0004\x00046Üvf×3;93l6®J\ñïuäJe«\x000fæÎ·3ûÙ´i"Y¶¹u)ëýÁíÌ¡g\x000erfnS¶Y³\x0000×ÓéÖÆCÇÜväØ#G1²Å\x0017Kêü\x0002G[Ð J\x001eù ÛÎzæ$gÆªkKÌ\x0015êÌáõOè6rÏåÌ>ñÈ²lXÒÇÐììn9wWyôzJ\x000e\x001dÊÐºº ¹\x001aÇÔöàr\x001f»\x000cz<\x0006åç \x0013$«\x0005Öô\x0000ã-N0$K'Ûz8\x0008µü$´ÙQÍÊRÅ!ªåX>U\x000eÊUo\x001eNB-?
±b?ïÀ¬\x001aA{¾*Yg\x000ez8V´ü\q1°yvÒÛÞéæ;DÌÃ±¢åçË\x0006GØT0'XwmÙþ ~õ<´ÓeTCÜ©>Á%(~%úôéã»÷\x001fïÏî\x001eÿãìù¯ïïg\x0004\x0005<×7`à\x0017¨õgp'¤ÚììvñõÕ»Wð+Ýþ7øo¼¼\Ów©¿L×\x0015¿Lé?ý·q\x0019\x0005£Ë\x0012
\x001a/\x0006Õ-fO¥\x0008ðþ9¿M'"¿Í×"b¢ß&%G¯TAç"ÔU~\x001bMZã\x0010|-jÁüÛtÍøÛ|­Ø,û6.Sl\x0010´	4ÈçìùÛÅ¼ØÉ¿M\x001eüT¿M$å4¸Ç¥öm2=@$±Øð~êo\x0003á_ÿÛàOòÛXKb_AÕúéòÛDáÏÆ/Ì'ÿ6~üm¾¿ù4­Îù	Ôã¹#Ã¿ÌbÙßÉ¿L\x0018\Ú¼ìÁ^úm¬"A
ØA\x0017\x001a*=åo\x0003÷
<mÌ®ï
Çøp\x000eìñìÝ¯ÿí8wr¥\x0005
\x000eÅ*cIà7ð§ÃÅÂ·gïþøç×Ç\x0011Ó6#jK¡I\x\x000b¡Ô³ß³y@Ì[\x00111ú¤
Ö\x0004\x0017×2ý\x001b\x0010\x001d×1\x0015\x000fæg'\x0011íð¡íæ\x000fQ½'#FLÏ\x0012!çxxË$¡=¡Û	\x0003öÔ\x0017ÄªSR\x0011Yä	\x0002ûS\x0011w¢¸Ø&\x0011o@L<\x0018\x00143-Å6\x0007Å.îoB\x001c¾s\x0010|gG¡.üW3OÈµ\B\x0015Zì\Ú¸\x0013OAÄh¶#²:/\x001c¿±ê\x0013\x0014+²ú\x0018\x0004\x001e§"ú\x0001ÑoGÔ$\x0005jJ.XWDåô²rÆ\x000c¡¶%ÅnwðÿÝ¶A:~¾x?Ñ¨\x0016cu7\x0008jl¤9(]mé[T
nÃÑñÐùþòæåüg\x0005Þ\x0008\x001cô·\x000bì4®\x0001m»¨\x0005ê$o>ÜýTÁóO\x0000üÓq^ªªU_5¦1\x000ceØ!ÊWKkõÍ«çe-<¿¾\x0005ÚçGa»Q&\x0008um\x0012XMNÞ£¶jÍÜ\x0000,©Rfí\x0017&oeÝÉj\x0014VÕ°B\x0004[+(}\x000eûlòYø_FkÜ2qi=x÷·Çûû/_¦æ\x001d\x0019\x001c#UÓ\x001eZ³ntj¸\x0001O×¬7\x0017ÿz{ysùîÝêëÛÓ\x0002@b#&ÖKú°|«Vc¤"\x0016]õâ½TDl{b+·q¦.;erµÅ
©6\x000eu+W¸m!v=±Û¸_Ø8*ÕJp©¤>«`Óê ·-Ä¾'öRbs#öòè	Ïd"\x000equ\x000eá\x0016âÐ\x0013\x0007¹õ9/HZ
°(¼áE±Úw·	8öÀQlâdø©B\x0007CòI'¶ðúl¿-¼©çMòmg¨º\x0008Df=³Ä=m!¬VÝo\x0002Î=p\x0016\x001b\x0018SÐ5o®£a¡¸¤¹É9¤Å\x0002I	q×éÒÐ±uMDÒº\x0002dOE)¶Ó²Ö\x0004y8>´øüèqä^G\ÇÍÊë\x0013K·¬\x000b=ô\x000esºï\x001dÜºù"iUÊ¤\x000fë9ñQ­V;æÀý~páÇàâýÇÏ¦2Gäð­ªÁMäâ£è\x0017ëª\x001bêË«·×kY"Æ4=¦aZ\x0016ÃBÉ`\x0012Ú=eb7ÿSÚÔÊH\x0015=º\x0002©ÃÆÕ¦!2éú(ÍYR×:©MI>ÔÆÄÞ\x00065Y°muÍúÔHqò\x000fÕL£4gfrwXì\x0010&Åîá½R.ÛéÙ§Ç\x000f÷¿ß=ü\x/>üx÷åáÓ\x000cpP\x001cæ \x0014?U¿À½ü-N_Z®Ï®o_]þpqó}Á¾xõìâÝÍõ\x0004·í¹í)ÜÎÇl?q\x0007ÖnLg±\x0014Û÷Øþ\x0014lØs$Ýê¥³"\x0000,=¿gµx;\x0012rë8,x
8(×íQôªæí³¥	FUîïéÀó\x0000O\x0000GYZ	
ÿ®ú\x0010¨Ñ£cÌvñ®/ä6¦çÆG&1wrºx9\x001c@\x001aÚ\x0004æv\x0007Û
Üî\x0014n|>¤\x0015\x001e\x0012ÆËÔ@Íö~u¢÷ý ®~°\x001fCð\x001c\x0002¡8\x0008`\x000f:\x0018\x0007\x0019SSÕ<$ÚÕÞ8}\x000e!ÐZ\x0004¤÷]®®Oi\T«\x0019\x001cÑÒ\x0013O4ýC\x0012\ßãz)®×ÜÄgPð¿&Ù0nå]\x0014ÔàÆ\x001e7Jq!`«jr¨[ìj¾]y\x0016/êÉpsOÀ¥Ñâ:Á¿%ÜÄ÷Qðm'âÂ\x0006qwÃ3á\x001f|7ÎÎ¼yüéî¯÷\x001fãºh¸Ì½Oµj5ªªcåW~}àõÍíó7¯áj7àâ"^pfu5Ds\x0006kÁj0µþÚá°ËõI»<XwC>\x000bë8äsm\x0003§&à¼c¯í²`Ý¢tÁvÛ7\x0008yM(¸UÖ\x0002D U{ËcxÓâÚÝÌkvÕÈ?
í06F^¯,¥%<ª\x0017ÐÚ
G\x0006OòÚ×JyÞå¢\x0005ûÖ^,£½fóbÅäv^\x0006^d¼^%:á\x0008ãpÞ;8\x0007Þ¸Ø¾¹w7Ò³ð#=çyñi¶fà7X7\x0014V\x0002ïrfm;o\x001cy£×Áe´¦Õ¢	m¿áº%Þå\x0017Í¼näuR^²\\x000b\x0008"
\x0006q#I®/\x001cÈ»XÅ¾77\x0019¡}­"!Ú9@²/,_âEu¹§àõqàÅ\x001fE¼Æp\x0019x4^Ê¼×ïzIÙüiÑç+ùÄÀôm:aò^¶\x0012¢.[yóéýû\x000f÷SÊ7åLªø6¢Ì5Þ<cä®Ù´<ÜSA7×/ß]¾º\Ó¾aZÓÓ\x001a)­§\x0005ì\x001cÜ<kKQ[]^Mbo µ=­\x0015ÒºÒSiÕ¹&ÛòäN ]íïÜ@ëzZ'¥ÕMÔßY\x0012\x0005)LûD°¾õBXãiôUY\x0008U-\x0006£ÝB8
\x0016ÎÎñÆ\x0006ÿ C´go\x001eßO âóqf­¶Ìò\x00108ò´g£\x0017G'3*ü=·/'@w£\x0008j¬\x0014\x0005êzÍ>`mr!MJÆ­
\x0013L£º\x0001ÕP!R \{Vª¾{\x0003j¦rã¤\x000f¶­l!íF~\x0003©Õ\x0012R êùóÃq\x0010
©Ó¤\x000cßß=Å÷ßÝ&\x0011Õy\x0011j+ær)\x0017)ÄjiN+8=ÓPÓDß\x001fë\x001eª³JX\x0018£ÉªôÖ£\x000f×-F]¾ô\x0012g\x00188åZ\x001dj6ÆºNñZNqyRÊFîâÙâ¦èë\x001bEI;pÊE¢¯OS
\x001c­³¤Iõ¤IÉÖ)7µÀ!V±\x0017$¥ºÝ¤½[S¤DÕ»éª­yntuXî®ÉQÅ¶§Ìb
a+«\x001fÜ?þ(±+voÕý\x001fñ&Ví
á
±ª¼ªâ?Ë\x001a\x0006ÿ?6VBéþbW\x0015¼\x0003î«ÌûJ-\x0006Ù[QÓd¨¨\x001c¯
´\x0004ßäª¢æ\x00115KÝ©\x0011@®Vq\x0016wEnUÅU1­IV£\x0007VüQ´³\x001cÔÕ\x0005Ô\x0019-f
\x001cX)ÿ\x0014\x0007kßûe©÷Kæ\x0005j"\x0011v­\x001d«Å\x000b°]S<igi\x0015Ç;ÆÙºß}wñûýG}þ÷_>Îäë½ÃåJ"J¥`\x001dÎNhÉ®\x0017?\^\x0011îó?¿¸Z^ã­\x0005i6p«h6W5Ü2rhÃâÐV\x0001mèiÖ\x001b*âu\x0006¯²\x0015Öñ\x0015\x000bç¿=
lêa\x0010\x0016odZ[K\x000b­Émðä¢(îvZ3,\x0004#]	­ÕÕáÀ"_ï¯¨ËYqÊ¶&\x000f´YFëq&T¥µºfà\x0002=\x0017\x000b9µtmÇµºÇÅ;Ì·k\x0007\+ÃÅºìIE/B<HÑÅt\x0001®\x001fp½\x0010W+¬k¬Ê\x0011­ç.\x000b\x001a,\x000e\x001cßëÅà\x0001H
ËÇªz¥õ!'ö¹z±ÕC@;¬\x0005'\\x000bÿeK×
kÁ	×Â\x0019nT=.ü$\\x000b\x001bi4[\x0013Ö\x0002\x0017=êÅÇ¯ioâ\x0007Ô,D
øú\\x000b\x0011BôU>dÎ\x0018j³XÈ¿Ô¸¿Üí\x001dfw²e¸ÔfO%4à\x0012TÓ8\x0015æÃ÷/?ï\x0011ÿ,\¸ò6Ãù\x001bxá6Íe	V\x0011ñO{Ä?É·\x001aP\x0005+	Ä<ÆÖ¦'tøÇ=â\x001f«B±tøÑñª`t#xO"Vz_QÛýµÇ\x001f\x001fy\x0012ÌØgGmv¢óä¢çâ\x001f»¨\x001eÛ\x0017ÿ\Ü>»}q;l{d{\x0002²"Y\x000e«­ÆòÝÂ\x001cHf¼è=\x0019³ë¹ÜÛ©¹CGîGq>rs ]¡ßÆì{f\x0002³â©®\x001an\x001aõ	\x0007Më\x0004;2y\x000bsè99ä
ç\x0005ù¸ä\[\x001bv±ÚJÆ\x001c{æx\x0002s¢\x0017^°³BuÃjgÕÚ0\x0017\x001fö¶1;[²u¯\x0010ªÈµ\x0017ôÏgoîÿþðþþa\x0006\x001av\x001e
 * 5ýI¹5aãÚ×\x001eÑß½¹üóÍËË	èh{h\x0002Ð*iº0{x¬\x0002þ\x0006éC\x0019â'FÒÞÒ:I©MòþÞc\x0011VíÜö³é1,F\x001a"j£\x0006j£ä¶v\x001eÇ³Õ\x0005\x0012¹?(jQÀ\x0005²Ze±:
\x000b¤tÈK©!F²´B|\x0019àV¨gj½­Q+$°BB:7¨#þÛ²B´mÔz8"êl\x0006êlä¶Öä\x0018Kj¨ä:*v!zqrÏ6jë\ñ{;\x0017Ø,z'óòöþá¯>Ì¨\x001a&¬cH¤:\x0004VöU¤Ä©Ô]Q£y{yóæúÕ !¡îòAÚÞ´7¢ªsSQÕc\x0004 #\x0015àôáñ¹\x001bHéI\x001a&§\x0016a?ÏFeq\x001asxöä\x0006T?|/ûþÖóüdÌYER#Ê­jÝSXÕ\x00015È¬Ê\x0003,\x000c¾Ã:B´*7xÕWT¦QÃ\x001ad¨`Õ:Ä\x0004äV%·bUÏ¨åüÓ¨:íu\x000e\x0017¿[IË¤ ³7w\x0013eÑÁNRôù\x0001´Öf4ëeù¯uDÐÛAæ4=§pâ·7$Ï«àÆ\x0012ZÒFóÚq;Ì\x00039´×4VÂØÊ\x0004Á\x001e[]\x000bd°lÊCÅA[,ézJ'¡4¾}qTÂ«sq5¯L\x001b\x000eªRmÁô=¦\x0017a*8\x000b\x0006kw\x000bóÐ¹´3ôA´0
å`aÂ\x001aõ¼2\x001ds\x001e¬	ÛÂ\x0019{Î(à´õjPíi¨â6+j=\x000cÖ\x001dÔçØzÌ$üì|\x001ci1úìm\x0013=ÉòÌ=gpÂ·®`8²Â<àT¼ÜÁ\x0001\x0014\x001b8ûÁ­;áß=Ñ$¥bÐzcïÎB2`Ð	Ïy\x0014t<$'\x0011v\x0010hÌ.Yeì²øéVÐá$Ò£ÈO$¨U­W\x0004PÚ\x0012]|Ú
:\x001cGZr\x001eÙ¨)o"¬*'ç	è+0¶\x000e'\x001cI\x0016Âe:ÜcÖÔM\x0008\x001f>³"¦=8ùo\x000bèp&iÉ¡d\x0013õË\x001b¬§Q¼Bã|
{\x000eGI\x0016'.P ze¦Ù7ÅÅ$ÅVÎáHÒ3É¡f\x0014-Ðè)ç
[>0¨Y\x001c­¹\x0015t8´äT²ç­Â×$3\x0008\x0006ÝJ\x0007õÎ¶\x000e§\x001dKXX\x000c\x001a2ÉÁ©Äb«â7Ã©dD§I|?B×T_\x000er¹|ÓN:(Ò·\x0005t8èTú¯\x0008Ìx=\x0012\x001dJÖrT\x001fÑí³A3ë[/Kl\x0005\x001d|½\x0011ùz\x001fiÞ=,QÏñ²r|Ê\x001fNâlá\x001c|¨\x0011ùÐ¤Ú\x0004\x0017Î:\x000b&«éË8sã<
:ø&#òMÙr®)bW]½uªäùËcuòé\x0011³í\x0015ë
ÅÕ¶y(\x001cïÚîñâæhíüaÚªÉÐåEðÚ©\x000cÿÿñ?/Qÿ8¨Ó^Q1Ã±ªJ\x001c(Rd°8#üpñìÙ«³Ká?rÐû³:î\x0013·aFWº\x001d*Ê¶jå^¯\x0014ú7Ê£öt=¨\x0013\x001aüÜµ®S»Ôºj3}ùIþ' õ=©zGÊ\x000eçÐòpÁ]Ig:8»j\x0003éîý\x000fI£\x0015~}OØÅ¨\x001ek\x001eê×g¡/ï\x000f'o'×h\x001a>}\x0012~{â§Eêè²ìµáÚn¿Ö:kÐnøKÙôYøñÿ¹¨1î]á¦÷
]^Ýý~÷ñç)\x001bÀáì\x0013yø4YRâ¹¥ÄýâÜþýÕÅ\x000f\x0017Wß¯\x0013Uè.ì\x0003h£äÐFÑ´CÀ³Zfõ`g\x0016m,¶\x0003´=\x0001ZSð\x000fK\x001b\x0010Ú+Õ2úuf"h\x001b{h\x001båÐÖ`äR_Lr½`\x0001´æÁ,Îc
^ÓÐ~X\x001eþåáx\x001e­ÁæE[e¼¼a)a8I¦¡\x000f¸6"\x001ev¡?a\x0017:55X^d
\x0011ó \x0007»ø*²òn^\x00172\x0007/gÆC®íÁHÈp°\x0017_+DÌ»6Qdá$fJháÌ\x000fz\x0000ô¥ÝÝr\x001d\x000c:\x000fÐY\x000e\x001dB{ 
ù\x000b´íÙzqh\x0008º;¬c=¬ÅÐB °4eº\x0010
­JéÍ3\x000f+:°¢aIÁä4áÉãPF²³9}q\x0018ã÷4Pà|í\x001aô¯Àá¼\x0007ö\x0019i¸\x000b±4¶²T\x0018Û8IT]S¾¸º¸yþ\x0012À'`M\x000fk¤°ß;P¤!×üÛM\x0004ZÖ\x0015ÐÚÖJi\x0003êÄa÷µqÜü\x001a|<8çw#­ëiÜ¶u!\x001crm,GÛjÊøÅ!\x0001lèa\x0010\x0016»µi ¢^]å÷$\x00089ÖZ 7ÐÆ6Ji\x0003ÐÕ*T¯ª¶\x0008µaÓbéì\x0014ír Á¨©GMRÔÚ9¦L¨Ñ%ZÓwþ`íÀ6£v\x0008Ðq)\x0019jT¾Õ#+U\x0007[\x0001mt¬¯W\x0015;6à\x000e®K\x000b}W\x0004\x0017P\x001fì,Qí\x0008VÈ~·¦\:»\x0006Üþruãr½~\x0016²ðÐ¥ÈãñU;lTUZ\x0014©dÊëÕ¦òý¯ïö¾þ,d¶¤ú\x0002çT\x001e
O[Z\x0016)ÝÄh|ÏhüvFp¡µJÌ§È3l\x000c\x0014$f\x0017ãMvøØVðµ\x0003\]3¤¯U¢ÑÓ½ýI,Ù.CÈ¼\x001d²þcÈP\x0019\x001d]Ó§\x0018W·\x001b>µ\x0013|jÏ
¬(xD£°ª\x0011®\x000eNZ·¢u{-IÖÙ>Ô{{÷øËÜ$\x0011Ô\x000c©®\x001dÖcm©K9ðÏ\x0007_\x0011òíÅíõR`;\x0006yi$¨ºP\x001bTÉÑ\x0017L\x0017ø\_L6Ki{J+ oN3$ÒS9KÊ)\x0004Æ\]³®çt"kÂe$R\x0004)\x0002MÙ«Æ¹\x001aÝÏrúÓKìiZÛªã9êË6'\x0010¥D·b\x001e3öP 	]ÓW\x000f¦YsUÏj\x00163õIbMåv÷\x000e>ÄS7QO°:wÇxqIJ´Ô9Þòü¶\x001c¹àÆ\x0002{\x000e\x0003ªûì\x00072mØL\x00038s3kËû\x0004½8}\x0016×òÄéºè\x0008ìÐ5	=½¹ÿü·ÇÑ¤^'ãi<\ì(úpf1ØäöÛ³7oÿõvu0i¥ÝiÝ"m/u»Ö±öV0J\x0013¬eZW¥çisêis\x0012Ò*RfH«c®sÆ}ÐÉÓyoãê´÷iÜ~ê+¾ÐÛ,äj\x0003ïô\J*¯Éã®¶óúaéâ"^\x0015\}û
Ú{ê~\x000cu²õÊí¸iÄMR\\x0013è\x001a\x001atëÖ\x000c*4²µ«VÇqï\x001e\x0015/JÖwß½°öìù§ß~»KèÝZ\x0000ñ/¯ïfFÖ\x0011\x0004uËÙ\x0004[Þ\x001cÆåÇ¯7p\x000b={~ýúõ%ÜF/^Q1ÄëÙµ;ü&\x000eA¿ÀÝ¿\x0001ÄÚºJ6b
(SIåçq»x\x0018¯ü\x0006·\x000eÿÇ\x0011ÿÇS?@:¥Øª8\x001d=a«Éâ4æü(k¾~»È\x001cÖùÃýÙëû_fV:\\x0012Eì\x0004\x0002¶ZÝåµ¥.\x001dÖ:ÞÜ\½¾|±¶1uWt¬]Cá&Xk©ó\x001b`MU\x001b\x0003×Mß\x0018µ\x001d¼mbõ\x0003«ÿFY÷F1h	\x000fï»ÿý?ÿ×To)ö¡S\x000e>iª /×õúåÖÒ6?ïæåëË\x001fÖ\x001bK×ô¼FÌ\x001b\x000cÍE3\x0010\x0003ÓÍ×(3×Þk{\+Çm5¹Þ7o\x0019f5Y¼\x0005ØõÀN\x000e\x001c±B\x0017D-¦\x0003`|Aø\x001eØË\x00136âÇªí\x0007ÀüFçá\x0002õDÀ¡\x0007\x000ebàh¨\x0007\x001d,Ü¦\x001agËj!~¹\x0007]\x0002\x001c{à(\x0006N¾=*ê@mspUJláEu\x0013	oêyÜÀËls$-\x0004\x0006n¯ fUTy\x000bpî³ÜÀz+¬2Üï\x0007\x0006nWg·zÅß\x0000Ü½Õà¡¡äÄ¼0l:~ºMÙ·ä]\x001d\x00050C¬÷ý°\x001eýð«É7ü¬
Ý58\x0017Ä
\x000fm<\x0017,)s°ý¯>à\x001f+90{åáx¼í 	Û+ª\x000c°ñé©
Þ8-±j»ºÑ&A­\x001a\x000cª A
Ê\x0010h`ÐUuíIÐèzÐè$ ^qq\x000fx«s5\x00193¾pÁ8ýÓCh×â\x0002Ò\f¥\x0016*zàÅ¤3új=\x0007=KjFR# Å\x0015
À,O_/x5¾õ9.N:ÛHÚ5Ö!©ö\x0012R\x001d¹Ý\x001bÂBþú)rç\x0012w-ö$Íã×Ï¯_]-­ÓP_ ÊEÏT\\x001d\x00023Gjâ@?n'ÅÛw¤Å¦ZØvÔé.Êö¥Ì¦ÎäÛ\x000eê\x0003Ç±\x001egoé
Êå\x0004¼v@½Z/õ,6
6	Î&e\x0013M\x0014­æ,.\x001fV»NÍk¯ö\x001c=©¸Ò¬¢§J\x0006gÛ¥XI3ÏjUq¥a4Ç4GÉyÃ¿j|í­«WZ8ïy$<@	®}z§ÃÞiÁiQÝ*´Ð éÛ7\x0013\x000bô=\x001f¾<þ(\x0000Å\x0001J;PC ­Qõ)¶¼ÃÇ\x001f\x0005 	>¼n\x001f^rz
\x001b3µ\x000f?Aºöá£\x001f¢Ñè%ñ(öÿÔg\\x0003\x0017\x0014
Xw\x0012kN\x0019,Q:Õ ¨ÅÐ&ÉNRÀ\x00134Õº<ôN\òh0©s*)\x001eÂ\x001di9·{{¼¢j"
$¥1~¢O ÆOa\x0008JJñ4s¯jÐ\x001e«¸+)7ªè4Cº¶H!ê\x001d0£\x0008\x0013î¡\x000cåxu*\x0016m\x000e:.>3Ícj¿\x00178yIäT^pNæ)ÓU¾m7;Gã\x001aüÿz÷Û_?cKØëûÇ\x000f\x0013ÐØB\x001d¨ÞÕEO96 wT=Ï«Ãwßâ?zýæ-¶½¾¼}5ó+äáWÈ'ÿ
ez]Ñ¥ª°6¾þ
Z-kð+è]ú
\x0005üñÔß\x0001ZÖß!Âa\x001cëWÈgDÅ	A'ü
¦:Å\x001bÞÔ©àWÐ6Ú\x0005,Ì¢f\x0015m\x0008Ï(nþ\x001dvùò;Xuòïà4¹\x001aì,ä¡RðEèí/ùE9û\x0013~\x0007»\x001bÇ¿\x0003þxâï`­¡óÇj\x0006\x000f'\x000fR\x0015ARz}\x001cñößÁíÒçeG+òï\x0000[º­%¥p8IÒbJï_awÏ+¿Â0{]ô+8Ú -ø"%óëÀWÑëPR_Ñ¯`s\x0018s?ð\x000fÆÜÏåÇ\x000fð»Ü?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¾ýøeÕY³\x0012hZ\x0008A³ \x0002x {¦tã\x0001bF}~¼}öòMëxñ\x0005ªà¦
\x000cñÆ0\x0001oÇ¸´BÉ'$òcH½%ÞA.ô[¯ÃU\x0006J\üç ®	tÛÀwíT\\x0012Í0{d=';àÊ\x001awt7x,+IWhÉ
È:\x0018+oHðõò×\x000cò¢\x000cXjú\x0006áyv
\x0018
duQ3u\x0017^WóºÑõu,_\x0002x¯£(Ø°Ì{qÑ:ÞPóaÞT­Ñ{j<P\x000eu´¸8"j\x00196i.ïüä\x001bÐ¬ò¬}: ÚªÔI\x000cÌ\x0015¦¤§¯5Ôq ÉäTcQæ½;àÿf3Ý#õÙ\x0010©Ó\x0010\x001e#|úòÛ/\x0011û§\x000fÿÿ>>¬Ìø\x0008à5KÉÿèÕ\x0003kòåÉÎÇ7¯~ì¼=¾xöòúî+wAÌºbÖÿÚÌA\x0002Ä?p)\x0000ui~ütÿÛ/ë|±°Ô\x001a!UàÇ`e\x0015&»Ç`êÍ|ywõêÀL\x0003 ®\x001cÄ\x001e#]@\x0015ßôÄÀÄk\x001b\x0015ïý¼ªäU£¼¨zp£mKõ×1ä6XìØ	W¸z\x0018\x0017xR­r\z\x001doÜ*ó.¨¿õñ×\x000cï^ICï"¯â¢\x000bE÷ãÛÈôãÚ\x0012×\x000e/¯e-Ãhlçå
|Úôo\x001f¯+yÝðòú<ÑÀ¢\x001eY\x0007ÍÛA7\x0002õ~^_òúa^ÖVQIÍnl,¶¯\x001aád?n(qÃ(.äç\x0017eì\x0013º`ZÇ¶L5ÚÌûq¡|Iî\x001f`\x00066±¡{±Äê{£i\x0013SÃe4ÁÄßÀ&ó\x000fi\x001bF\x0017Zs\x0019²çß(Çe$8<s#²´g^.þ!\x0017½Å8âã[\x001cÌqxvz·n²²ÆþJGË¬Â\x0013v\x0016À3\x0018Z\x0012û\x001cF¼|Ó9\x000eÏß-\x000cWflUb«-Ø:|(\x000e\x0015¡ÚB
\°g`©® ZÔzÓb\x001b¬°µÅ;Ó´Aòè\x0016#\x0017b7¶)±Í\x0016l\x0008\x001c]ÈðÄ\x0001q\s\x0018\x0017{Ç-âJj·ZFOmò\x0016äTò0`\x0003¼Ú\x0010µ/©ý\x0016j\x001fð\x0002°- Ä=Ï#ì¸Ø¡Ä\x000e[°%FÍ£\x0000¥aq%#*:çÌ+2Ø´C<¦µ-ÔÒ´±e\x001eM´£éÔ&lØ
f¨dH8þ_{¹] »ò4°ÅÕHË£\x000f"·'!±x"©J\x0001{?ë\x0007«-¾\x0006\x0002Og¬¶ÐT\x0015dùHb!ËnÜ³-ÞF¬U=¹öd\x0001e\x0010|mYîÊíÃ®
lñ6XÇÛÛ\x0006ñ\x0002!\x001bî.Õ\x0010·­¸í¦cÉ¢\x0015\x0012\x001b¨*Sçy¨°ÜWÒ]yIØâ&±\x001d³Ä´aR\x0006\x0017é\x001a¿§5©ü$lqè\x001d\x0005\x0005ÛÒcSt¥¸½Ä@Ce[Öñö\x0016+\x0008I4+Y\x0013ÁÖ\x0004T\x000e\x0001]1i¥Hº²r
ÄÙ/4?,xðvÌsH\x001bjC«]Ù@¹Å\x0006\x0002î´Ú2M¦¸ó4?í\x0016R\x000bË-Â®ã©7XbªìtòPJ\x0003
ÕÍ±8ðÏokò·[Ü\x000ep\x0002\x0006ÞÝ\x000eäÀ{©v²üT6\x000bÏÂ¿
\x001cµ*ôBD.ö¸2\x0004{W·¢\x001e¹r÷ñýÃç/ïV<h\x000c¥,CKn\x0008ÑkuX\x0018FOÜ/o®_¿ùn©êá<í\x0010´Ã\x00083ð4B%\x0005u ã\x001dGç^*_ïc6%³ÙÀ¬¸!:uî¼Ìäo´jÔ0»Ùm`6·ø,GÈ<êZ·ôb¹ÊýMK=\x0017_k"/¼;§q³oEH]åwð\x000fe³ãëÇû¿ÝG\x0003òáóÇ\x000f+KÝAðH\x0006\x0003£©ùnfýÂñ×·W×º&äÅë/ÚjIÌoÃ\x0013{Ù§5\x0004\x000fìstp8\x0012às~£r±\x0013^\x0004q6Z%þ¡îý´²P?8JMa\x0011+Ë\x0014Ä»\x0002UÕ\x0005ß\x0018Ö;×éß-iR1¨.Aõ\x0000(¾×o¤î \x0013å\x001c^ì^EjJR3D*	ÓJê$ÀVcÉK\x0019Êõ¶Ä´Cñx¥)ÍÓ²æ\x000ey=/uh¬\x0002u%¨\x001b\x0002<\x0007·c	\x0015UóE¿±\x001aÔ ~\x00084ÆÊ:%C\x001b\x00067ú
\x0017A½>\x0016ÐsÜóå\x0000\x001aµ\x0010Þ¿_\x0019«iÈêÕØ\x0007K\x000f\x0000!w^BÐ(pssµ ÷Ì¼²äÃ¼"?gÅé\x0013E¼27m.¼fu\x0002«\x0012X\x0003[n2E· 	XeàÝxuÉ«Çy%ç\x0003\x000c:azÈòs³qC\x0012rØÄf\x000b1WJ	¢\x000fìnÚØÄvXÅ«?MQ0Âåg7Ï·ië.¨\x0002u\x0010»Ø\x0013O\x000fVØp\x0003²ö:ï
XV\x0004ê ö%±\x001f'ÖTü9\x0011ÓÝH;ÎkY·\×ÕC\x001cJâ0NL~#\x0002K®Ò^ä¨ñ\x000cÐzàB@Wo?½Ä8#wæ(]ÛOØ
¹vwÃþN¡\x0018Çæù\x0011V»¬QbÍ²@^\x0007råñ`Øåá*û93aÝ\x001f¹òy0ìô°ÒfÝè¸«éJ;\x001bM\x0003ÈÛa¿§\x001cPÎêÖÜ²¾8Hµ¸r"0îEb\x0014L\x0014:\x0006´ÈZ²M¾ðÀÓ\y\x0011\x0018w#1\x0018¢èM£êâ
5"n
5\x0018 ®¼\x0008»\x0011«HS..²d¸Á\x0019Ù,õÜ÷!Wn\x0004Æý\x0008Î]£Ev²U1Ðg\x000b·T\x0005ØG,+?"ÇýÉºAÑßQãd\ä\x001c$ëåz\x001eäÊÈq?b|Fv&»>\x0005l/ôn[YVFY\x001be±5ÖôYCï\x0016uÊ*²Ã¡½Â7\x0010\x0012çöYÐéüzcõ\x00059Û\x000eäÊÄÉq\x0013\x0017Á<\x0005\x0018Ñ@ó*á½¬4ðú+\x001b'Çmlmà72-r¡.È}v W6NÛ8\x001dB¾\x000f»c\x000c#ó
ª5®\x001fYUFN\x001b9eraõ\ \x0017y·{µªl\x001a·qÈbb5/r6ËªÑ\x001d>\ÅÊj<VVKÑ&dj8	ÙÆ-)\x0010ö\x0011×é¡q«,=OzÕèS\x0014¿eâ½+¬Æm²9¼0Óãzê]6\x000c,\x001bi\x001dÈA7õÃDìãÇ\x000f«XM\x000cÙ¨tKªé®¬.dÆÉ¢MVÌÃÞ¾|Ñ~\x0016ç\x000f£"g±º ] .Ã\x00129´A3¤n\x000cUë#5äH­2:3 g[ÍoúÖül»P\x0005Ç­ÎÉÄh*F3ÂSòc'I¤ÙÀÙl
\x000b¢®+\x0017ÒÔ¿öÈÏBX	\x0012³ÉÙ:à:\x0003µ$d¾\x0016ÒVvd%éÔ\x0008~
§£.-\x0016Ò:k\x0011}èG\x0010\x001d©­Ä_[Ó\x0013[¤\x0004Þ\x000bZ£+!mµ#íÐ©±\9-%\x001aÖmÔb!	¹\x0016RVrèÇf\x0017$eÖBv"\x0017whÇ«²ªkHËÉ
}+Ïx<>W$\x0013ðøl?ãþ5îÏ!Ö¸E)°Æº\x0011Jw8«ý`¡Rû\x0012¬8\x0007\x0014Å;àý§ÃÓÓãã®{ý×Rä¨)\x0000IÔÄ»WVC6K³N®î\x000eO··ÿÞé\x0013ç/jBWºÝ=¨ÂÂÇ$×è\x001c?\x0000æ<ÝR\x0018½\x001e5¨a\x0008\x0015gI¦\x0019C1PâÙññòÊ-aVÂòCð:T¨7ÀØ\x000e@A\x001aB±Ò\x0019/ÚpA\x000cX\x001b\x001e^§E^îDñ'5=ÇÿFaä\x0014²0\x0015K\x0015ëUW¬z5Ørñ9jÒ>k\x000c74':Q]êÆP±h\x00128$Wr{+\x0012eÅÖu¤sý7J9F\x001a}*«ËÚ"ï
ó\x001do¹de%kµ\x0001äà\x0006Àâ\x001fBü¦§òkjÈ]ö¡Î)
Q¦(zÍU´ü*ßëdsåò½n\x000fÔj\x0007¨Á\x001d\x0010M\x0014*Ìi\x0012©Èo5r½ªªß_
þþ8\x000bQ%·ô©_HåRx­]ÕÕï¯\x0007ÐÜV¦Qæ\x0012\x0011.?ñ¥RÕËª«eÕË*\x0000Ë*Ù\x0007h*|6ùUf)-¼\x001eÕV¨v\x0008\x0015E$ììY5k^\x0000/+,õ\x0005­gõ\x0015«\x001fd\x0005n¼ÿÍ/ÍJù}nÓº\x001ay\x0016²Æ?pÈzsúùôùa<¡Óy$J\x0000I%v\x0012ß\&N'\x001eånO¯¯¯.BÊ\x0012R\x000e@Æ_Û¤àßÇ= |4ô\x0010\x0010¯W\x000bS\x001bÖBª\x0012R¬¤`_\x001a ÐÕOÒe*®ãBÙïZD]"êÁu$Äxì½åuT\x0004©\x0017\x0003®4%¤\x0019YÇdä´¤Û&-W;Äÿuá·ÐvÐ*ï\x0014J
Z:3ÜwáÀøöÅ!\x001bn\x0019]ÉèFVÑr\x000fNPû$\x0016uòB.Ì8X»¾ôC?5»ô\x001aÒ¯Mïëq?.\WBÎ\x0005Z\x0014#?·äfëx7ÆÚÒ{6vaÀíZÊjOÂÈ¦Ä\x0004IòãÁ±8t$1\¼unþÁ¡úÁaä\x0017÷ù\x0016\x0017¤æGéX\x0000Õl¨µvPÊê\x0017\x0003¿¸\x0017Þ:\x0014Öô«tÀ\x001d\x00039XªH¸D\x0019;k\=:Åë_;}ú+ä\x001fî×©\x001b\x001a¡\x0015w\x001dXOeçX@Ê\x0001\x001a\x0005\x001f×Ï_\x001dïîrüõU[ßU¬6 Ç«&äàòëÀc\x0003lìÕo1_Zg]Bë
ÐÙyNÐ©ÿ\x000b\x0011Yo[\x0011fÛv\x001aþðó(¶\x000eNQc#X4\x0011iD#x\x0012­ûC};qÒÃíAý\x0019ó<óÓs\x000c$&
Û_>Oív¯Þ>¯ë\x0004¯èU\x0014"h\x0012f ¹èJw}ùæõÔi÷êæøú\x0002+øùAbbõÓD7l¤2©Û+þa\x001d_\x0014G¦n/\x0008ÕíçY$X\x0014í\x001a[8µ0
ë\x0005Åñ0Ò¾\x0011®D«i[So\x0010VêùZ°Ó¿\x0007`Á¡¤LK\x001bíEª"\x0015Ó\ò	VêìP\x0007¬­·ìôï\x0011X«§!\x0005\x0008ëP8\x001b­°\x000bAú~­á1ÖÃª0O#ìôï\x0011X\x0014ä$éUv-¹7\x0017#Vìßn8áu6\x0006ÅÓ;U¾	`ªÊÒU Þ¡>=®K78'Í\x0014`4óõ\Lson8Þãÿ{¼\x0004éE	éÅ\x0000¤ÒìÌ\x0002*$$\x0007\x001cra\x0004è·¡ZÊ0²j\x001a";Qbú4¹Ü\x0000ÖóZ6&Ù¬§\x0004Q­%þ³\x001fÓ°ö_üÅ=5Çè 8É\x0007f!Ö^)kL9éÙ©\x0006+òo®ù1\x0002ÌB1ÌZL]cê\x0011L.á«\x001bRbQ\x00030\x000b5\+1¡þÑaäGÏc\x000eq\x000eô\x0013"«`
åõ¢Áj¿í¬Ä5¦\x001cÂT¤	\x001btCó8u0yoÚ·ýµ¦Æ\x001c9é6<1tÒQÉVÓpò\x0019\x0016\x0012Q+)uM©G(\x0003WB\x0008ÆEêÀ-È\x0016ZCJÌV*ÍQY{À&\x000fz;
Õª»Þá¸ÇÅä-óqø\x0003ÖýEþvª*üþq}I¡·jR\x0017Â\x0017=Îk_ô¾½¬Ñ£?j
¿¿½PPÈ¼¶âµ¼¨cÍ\x001dY\x0016èª­Í­zêÛn©×W¼þ_}}ç¡3È3gþÅyeÅ+ÿåy«óæþuÏ[pçâLnzéI¸wïûåô\x0001w¼züõïÿ³îØÜU! æOó\¬\x0003÷m_¸ï^_½úáø\x0002çxÜÜ\x001co/ñ¸s&7½\x0001mÃ\x0017B6ÑÇQY¥fçáT£M}^ôj+½×<y\x0002/\x000f\x0016ßæ=\x0013\x001a{ÃøºÄ×[ñ£\x000bäVe;
¥Mïxõ\x001b½OÃô¦¤7é\x001d
¦Æ;|£M%/t§tøB»+½-éífúÜxf´Ï}$%¿â\x001dþÛÈ0¾/ñý\x000eøÔ\x0006c´ÍóÏ4×Æ9ÑhÌïÆ·Î×\x0007\x0017¢õóÓßNïVf«ùÍ"Ff3MO\x0014ý9ùmhÎ >?þéxûÝeVS²AVOcÅ$\x001fó?\x001dGÕò^TW¢º1Ô\x0018î¥\x0014éM
ÇBPD-¡ñ\x000e´\x0016Ô{MçªÞW÷\x001f>ãÿò¸NH\x00059	ÿ"®ÃÂÙô¾æ¹K..ìr]ï««××¯ñ¹½úz°;w3ÎUU½\x0003´2ggÔJïÙÌyãKe\x0016qAøé²ÝJüÃ\x001fðÅ0±g¿~þ¸*B\x0003ëäàp¹$Ï)´cºé¨}\x000bv'öìãÓ\x000bAT"¶s
ñÄõ·Á$Y\x001fa@ÓKPÜ\x0013fµ]Â\x0001¦J¤YÂzÇ0³«_\x001fÞß\x001f~üòááÿ~Y'_hP@kJPèö¨ÌËò¦Q¢Kå\x0003\x0017Ño®\x000e?¾yqýooÚ\x000cî*p·	\x001cçï¤w\x0010\x0004Íéâ©ìqk,Û>ìPaMØ^aAµæQ\x0002GIÖå­<CäóË\x0000ã»À\x0006r\x001c\x0011M³)¥çàÚzÎ\x0013É\x001bUácäÕV1¶ô\x0018\x0017Üç6&ÉOáª\x0015ÛWÅlÚ,\x0016{mi¼&>(¦2\ÇÅÍFµÆ¶¼%
ÀmµWì¦½b\x0005à\x0006\x000e§,qf¦½"[O4]àfz\x0016/m\x001a¬?¨mþxzXweW-ãñÛ\x001bx~{¼ú&f\x001dé/¹\x001f×KWvâS8\x0013o=7x=¯T\x0012ºÑØô¶è!(z`Ò\x000e'7nã\x00058+Ý\x0001Yüy|ÿþ>Þ>\x001c^Ç°îaU«\x0016N±!ù~ðNåÃ@|á\x001b9\x0006õWõêøâð:\x0006w×í-\x0002µ\x0011\x0018µG}*xèèY|*#`ÓpèÝÀ®\x0002v\x001b\x0001gLÄ" {uúD£J²\x001fXUÀj\x0018Øæ\x0015\x0006G\x0005ñ¨Iáþ4¨x\x0017à¹R\x0002±Nb\x0010Øë,\x001b²¯¶Üq& Qò5qË¨MÀÅ£)\x0002O¦Äñ¬	"fÍñ\x001akÞÅNãÞ%ÚLà?Gc8G»ØyA^/®±ã5\x0016¢näÚPÀ\x0006K9I6WP\x000c­³\x001c	¾!â±zO\x0008w&î,Ü$îü*ºçÓ_î\x000fO?þío\x000f\x001f\x001eV¹
¼_TÄ\x0008(F`s¿-qxôËÇï¯\x000eO_þéO×/®Û^a]	ë\x0006a ÄPüÏè\x0013+pÁ¥\x0014­h/l(aÃ l¼Jy*\x000fõRh&¶UìÓK;+l!-ö·
áb=N¸ÖÑë%xq\x001b½´³*
Òb\x0006~lÛÊ\\o¹>n[.\x0010\x000e
Á÷^ZWÑºQZi)pW1\x001ay\x0002i\x0014º3¤àâ"xãý§\x00137T¸a\x000cwª¹\x0006Ú¹Ú>
8\x0019·!RÝ[ø\x0008Ä|Ä\x0010¯W3¯ Q Ñ\x0006s@4\x0011»ì]¨íÂÔ¡=´\x001dp*3µ
xj±1=Ì!ª!?Ó[\x001f5\x0018<k\x0012ÓÙ¼{ãM?\x001d5Ë2¹ø\x0006¸\x000f®©qÍ(nÜ²Nå²|:l8vxmC8§××¼~WÜ8\x0013ª°â\x001b\x0007{['®¬\x000f\x001c>lBS+pÀ.´y1\x0008Ëw\x0017Ë+e+\x0007q}ÑJ\x0012C$_\x0001Æ\x0002*¶4Þ!×óÊú\x0005\x000f\x001clyúñËÛ_NëÇéÉÆ¿:Â\x000b\x0008\x000c2Ë\x00024æküÓoýp¼]w	¹èbÈJl`0\x000b×IÌC ttGYt¿¡V>@=\x000b\x0019!5T
Sc¯85ßzj\x0015¸Ô,i¨\x001b^¹\x001f\x001alµ;¦AbÃÔrzÑ6\x0008\x0008º%\x0003\x0008VchUköSëBé\x0004­\x0011þÃÔñ²Ig(\x001eE»:\x00173`\x0015÷jêæµh.
GFÃ±e©ó2Aj"q©¹26.õzê\x000bk=Ë\x001bNØXÐ6í4OÆÊÓ\x001d\x001fÀð\x0004zm\x001bY\x0001lYÏâ\x0015Ç?/z û~\t ü|\t×üÛ\x0006»\x0007Þ³óX¸çôË'þëÃýãºü¶Q¬SíR^Þg¥Q\x0003\x000bÏ#è;dþéúêváMý|\x0012½'Ñ {ÃB¿j\x0016úÅ®FbÖ'³\x0011fS2qfg¹
T¼Ì*OT
×8ìJd7l£\x0005IÄÞ¼Ì;cA¦8Äa\x00031äEV¬¢ <_þâf^\x0010{édý-f\x000f\x001d@CA©Â«¶£\x0003ÈÅì¦»\x0018A®Î\x001fl8^!'×B\x0015Í.ðÎÐ~AV¯¹:°á\x0000ÆI¸b,¥é8ÌÓ®QÝ\x0001\x001d½«¬jrð\x000f\óÓýw\x001f]Ù\x0013öR½Wäâï\x000enAäõ§«\x0017ß½\(\x001ccÈ,¯5A²¼V\x001f¥gy=/Y0WâvÆ\P«Yé\éÜØb@Y¶$ÏO
Kó.Q
\x0003ç*5«°~üøéþ·_\x000e¯N\x001fÖÅ\x000fÓ\Y\x0007Tx\x0007Q×¢uË?þøòîêÕ\x000fWÇÛ\x0017K\x000f2çj5C\x0001X)S%VXs)^ü\x0002\x001e\x0014oÿí¿æm?n+×@\x000e\x001cFVW>¡!OZÏÊõ\x001c9±Ð7ÔÇ«K^=¾Àã\x001c£!/pÐ\,v[`S\x0002ñ\x00056¬¾3õ²\x0006<\x0003ÛàÛ1C\x001f°-í80°6Á±Ù´À>©/Ìñéãu%¯Ûb\x001fhv\x0016³s|í\x000f\x000býÂ}À¾\x0004öãÀ\x0007\\x0018pO\x000cï\x0008N	Y¿`|»\x000b\x0015\x001cUpF\x001dËÛ\x001a\x0014aæÑÞy\x001e¯kXõ/1×Ïä7¸woÌXÈÙuhÞË,\x000c\x001fÇVn.væeÑèòîËáÕÇÇ=E.É%Ç\x0000*\x001edMF\x0016c±§èÕËÛ¥!\x0006ÿ?sï¶\x001cÇ¤ë¾J½@Ãâ|0^\x0015AB\x001b\x0008p
 ×tßÈ
`B7\x0004hDOw_ÍkÌí¾u½ß ßdd»G¸Ge$*\x0013\x0019\x00183­eXôU\x001c=üð{_M,¨NQH\x0013¨3|¢9«JñdMî \x0006ê"§ö¸CÄ½ÙÝÝ~½Ý=MmÍ¬P*'\x001fh\x000e;
å;\x000e\x000c^\x001eY5RhtPNÎNß|\x001aï*Û¯x
¾Ó~\x0006µöìô#ª¸5hú\x0005ñã&jÝ¥Ö\x000b¨½d\x0011\\\x001bW±+«Ø¾Ðdx
µë+w»Z¹\x001bB7¿L&V¼±Nj\x0019%;N\x0006\x0010\x0018ÞAÇ?N¡U]Z5Ö9Ê
T¨KzÈZrJ\x0015\x0018qã«b2­îÒê¹´ÅûµuGO
S<<a!-X(=ë]w´&o~ÙÞoï&¡ÂÁÈ-ç=6\x000fÍ\x001e`õÒQå¼ã\x001f×çë³9MÓ´sj\x000czÑÙë\x001dÆU4|\x0013ã^{\x0005L×Åts0­¦ M¥i4\x00158A4>\x0019ºa\x000e&<!Ê!«¨w(ÔËì0ÝDÎ\x0019¦»b- ÚqÏ tèe#\x0017å<\x000bè¨`ë ±ÿbÝègÿ¸ÙM¬"P\x0006E\x0008S\x000c\x000eè
N´¸\x001aÁÿ´:ûÓñÉpBxìoöØm>2I!]\x0008Æ\x0001u\x0012+\x001e^÷Ílì¿Ïc·ûùtJc=q+9©áÉàÊ;a´µÕ4LÓÅ4s\x00063ªâQ±<p=7\x0014qqÄE3\x00193t1ÃÑvßÎ:ò«ËvÞ0¯@©«×Kw~½üþ¶éÃy°X[m¨ï6ÀJnüË^d/G<³/\x000e­\x0016¶>à\x0017{[oõÃîîî\x001aNÒI¤QâïÆ¬,#%·éQ\x0003ò\x0007Ù\x001cYýprvö\x0016ÎÒ\x0017YUUÍd"MÊ(Ò÷,uþúW!Õ]R=wT#?\\x0015\x0006Ar!TlåÁ5fóO5]X3\x0013V\x0005ÎÎRF°4C\x001ejH_°\x0011ÖvaíÜ5à9Ù	GV\x0007Z\x0005\x001c\x0007ÃÔWu]X7\x0013\x0016÷>m.l/«Ð¥¥ \x0007ªü[a}\x0017ÖÏÕf\x0012hª`+Â
6V×=5tYÃLÖ`°óU\x001eXî+\x0002ë_¨°z_g\x0015Ä.l	\x000bçª/Ç\x0016)ùIÏ\x0017×k\x001d\²¾\x000eæÞ\x0007Øý÷d¥I\x0019¹^Þ6\x000e[²rî1\x001b"Û\x0004ðz:"!bUVìâs+lupÉ¹'WÐ%=Ì	R\x001aá,)KzÔ«²§\x001d°a¤L°ûRùÜþ±WØw»{úû\x0014^iµb\x0005Ê`©ó%\Ê\x00149ÏÎUuÿÙéÉ§\x001f\x001c`bÞ÷Dfëf3\x001bX\x00109P\x0003'kÌ>zÇc\x000cÖÂKy|c5Ìqþ0;¡¨K\x000cØj4\x000fs\x001cwn :Þ<ÌjÌªÎ¿kVª]*»S Ê/wöÂ\x0014Óã\x001cò8Ë²M-Ó¸FûãÝ\x000eÈ/&¬È´PN²Úi÷\x0019Êµ>¼ þýñìä\x0014?"µBÈ¾Ó¬ÕldÅ5\x0014ÒJEiÒ}LÄnÀaÔNl+b»XÓå\x0001Ö£aKR\x0019
Xo\x0006úÔ7 «¨kû\x000c«Ý>s\x001eòÝÿüç|¿X\x0004o\x0002\x001ds\x0018®áìù(©?ÇR¡Ã¡\x001bÊµ|¶B\x0011\x0004][>\x001c\x0016 ;&OBv\x000b\x001a£æ¶+*\x000cEZ÷n:DF7Ýüav\x0014qÒ2\x0008lZoðo\x0018å53«Y-`\x000e\x0012Ã	\x0019Ó«rnt´ë\x0005í¯¾YºzÝVØh1fhØ*û¬*A¿PË´\x001eLBïw^Ý\x0007ÈÞ>Ü~ûöÕ\x0017 ^ß½ÛNm¿i©º
l7ÇM¶uäD6?ÒôöâôòòO«w«õùû³õH`Dô5\x0000/î½¹ÜE\Ê	SZÆ\x0005~ßù1-¬fn×åv¸ÑuNþÉÜMòC8%k$wa2¶\x0012ª._"ùýw^ÙÛÕ×èZ;~x¼¿½ûe{3ÉüðQê8nAÖÉ%I3^}¹þ\x001cWø\x001aÿÃï>­/6ç§g?®_ü"ûÒùôE¨t~Ù\x0017	"¼¨I!DÈèXLM\x000cèw.ù"¡ð*3bKÞº\\x0001¯<V/\x000eØ\x0005à¿\x0012Õ(ñ\x001a3â±£&Eà\x0005£Jp§°e\x001b\x001b\x0013èùElýE^eFÐë@gªæ.=`øóS(\x000cÅ|\x0011[Ï}\x00191ã¦ð>Ò&Dð÷ð\x0003\x0002~K¾G¬'$¾Ê`\x001b¿ì¬pE¹à!iøÐ\x0003¥³¾Ïý¾9²Ç'_ééòq{ÿð¸ýu²¼\x0015ØiG*ò°wN²:*¡$Ô)åãúüb³þ0ª&ÆÄº"Ö³Q=#»3%ÆÛ8°ûB»\x0001ÙvbS\x0011ÙÄ°c)\x001c'0,ßÊ\x0012%³²\x0014¨\x0003¾·fbW\x0011»¹ÄÂG¾QYEæDtÁaNxP
x6C\x0005\x001cæ/cÍÑ\x0003×°±.C<äk%Þ\x0017\x001e#±\x00163µ7,T\x0001MS\x0016­d«taÀBh'®6»ñ4\x0000q×2JLÔÙÐÐ9\x0007v\x001akWÕ´ºé-äÙ\x000bÃ³EO=Ò\x001dU®ô`ZÖ\x000cèm\x000fz»àP\x0016\x0004\x001d8p«bazHé9ôÀSoÏ|Ýc¾Í\Ê¤\x000e
)fºÆ¼­Wbþ¹ÇüóÜc.\x0018ÒvcN±\x000e(Ê\x001bñ97\x0014ÍogþÒcþ2w\x0005ûàúÔíPèËõ7\x0014Ø± w=èÝÜ\x001c.éÎ¦\x0014\x0011¹ã¡^ÎÜïqíU7\x0013éãöq1]föMÍ¹^Á²-7¨;Hù\x001d\x001f×1Û­îU7\x000fi:¤
8ñ\x0012\x000e5Ee \\x0004"\x0006Ä\x001c\x0018mÑÎ`\x0004KGRÛ\x001b\x0019¨8°ÓC\x0001®ÑLQJØ\x0004¾_hé;I|w7\x000f\x0013ÛÚÜ¨\x0002´µ\x000bo\x000fºÓl\x0018x\x0015\x0012åç
ØìÃÎ\x0002ª» z\x0016¨3¥\x0002Á®ã\x000eè\x0015VÛeµóXµÊÛHbû\x0018\x0012Í\x0005SÁ\x0016ÔÑÉ*úó_8?ÃáômÚ"ÅHá\x0014þHoi-$)\x0002¹ Gzt}cértÖ)Qµ2ê\x0018ÍÓa}\x0011º\x0003zq-ºË¨ÛÇqïîr&â21FU¼D#\x0001û\x0017\x0018E´¦Ç\x0014ÂÉëûï\x000f·÷»ÕåöñûÃãíÃÄ\x0007\x0019G±üdh´v0aØOº>¿º8=?Y]®7W\x0017Ó¡«ßõK{\.íYÿmw¿/aÿã\x0013|Ü}Vä¥ç\x0008\x0007û*o+-b×Ï~ÎúóÉù¾ýàãÉÕÅùð»~Ë\x0015>Kàeì¸ò²tvQ%ï ¸²ÙôºK¯\x0017\x000e½EÕ\x0008è(iþ\x0003K|6½íÒÛ¥ô%GÅ9î3«-E
rà}ÜLïc/\x0015~}v³}¼Ý=>&oÛñÃÓõîñûDeèÜÏÑ/\x0005§`.]°f(4ªý¨\x001fúãéÉf|mÇ\x0017Þl®N'|\x0005Õý
jùWÈ:Öé+àU¿\x0001%äÂ\x0017\x0018Hs^ð\x0005t÷\x000bèå_\x0000¬\A\x0002»VSò«ô¢b\x001e\x001b|½ÖW\x0008ÆÁWÐaÀ\x0000÷\x001d~ìd¶l¶7ð\x0006¦ÿ!b´ÙzÂÎ19}\x0008\x0013á\x0013¹öa mwÖ²Y\x001fÃ\x0013dL±Ml\x0016 S#/\x001deð¹¤\x0017©©Ú[{;`EÍ¡v5µO\x001dlrëÃ8\x000b
á\x0001´eæ!#µÙôk"éð¼ÜÝ\x0003íj»ºÜM«ÃRNÍÝö<\x001fîZ±ÃÅë±fBØâðä\x001cWëÕåÉHééWG\x001aÓ-êÁ
ç\x0008ë\x0017ÄH\x0013´ãëvÄiç6]n³ÛZî)qÞÝµ\x001a¢ÛÄÑ§L#·ër»%Ü.p>\x000b/Zj*\x0015F\x0013¹¥éå\x0015¡\x001f
¬{ÚÞb>ßãÝî\x001bîË÷Û§»»i\x001e\x0018Âã,t\x001dEMÜCäÿöi}9}³KÜï×à4\x001f9OBÏ±\x000f¿Hýr|[mnÿöp;¹ÑW\x0008tó£¿Ó©()YÇýø>çåjsúùât3Z\x001c±÷¹\x0000mÄll#à\x0018ÌO`
)\x001c\x0008Mµá\x0016\x0013¤^
:TÐa	4¶ÓÚhv,%AÛ\x001d^JÿlÁ®H¿D\x000cjëL­\x0002·z\x0015\<h¥\x001bxÅÏ î´YGêÔf}6¶cåY*ß\x0019ÚòP\x000f¸Ëg1»Ù-aæâ\0*\x001d¥ûiL? ìÈÄ\x001cl]\x000fµ^4ÔáHåCÄ\x0007Mò\x0014Q\x0017ðÕ¶£¬Ï\x0010¹è\x0010\x0014 ÷\x0011ï\\x0002ÏîI©^màv5·{y7$4\x0001ãíÉÁ2\x00121;ÖÜq\x0011·¡\x0016\x001eË{ó+\x0019ì\x0007Æ~©0b
5\x0018\x000eu\x001c\x0019~âÈ}öðtûmõn÷·Ûo\x0013+h}jÑÜY\x0016öd>J\x001c$)õb,9ûìâÓ)ÞíO/Çî2w¨¸Ã\x0012n§\x001du\x0019Ay\x000c\x000eszÍmÊb\x001cp©´ËÐ{-À/øµpüpÿ\x00056÷ScoÍV§ù'%·ñôÁ\x000e?\x0013/ÎßÁ»æ|\x0002©êªy¤l4%RÈÝ'\x0001é°\x0003¾TwIõ,R\x0019ñ\x0016Ééld)`	°¹#"w
¤¦Kjæê¢÷\x0003Ö4i+Iµýá·V\x0003¨ëºY $\x00113\x001f8\x0013Æº2óÃO«	Áä\x0006\x0012{\x0015%
$tí/øùçi>%¬(Ê/X\x001dQï;Ù\x0013\x0018²u¯\x0018ntý\x0005?ü0îJÊ×DM\x001cç\x0013»ìÆ\x0003b£sÌ\x0008ab9PöÙJ¬dE\x001fç\x0011Û@í
\x0018¥áb&6A\x0011±~±ÃÁ4b½ïÄøq&1<há Ë¥sÁ
rkh?¤\x0006Ò
l;&&\x0000ÛºD\x0003°Án¬!»êdî3\x0003v&\x0017h\x000f/¿ÀQç¬eMÀ/ÞØjI\noï¿tàÄp \x001di¼eQ%äKe]{ìËõéù\x0015é\x0007\x000e&g0{¬Øã"vé9\x001e\x0003ìLc¬ô*ì\x0003wñ<vgºìÎ,c\x000fºø\x001aø¦ô® ÉÌô¯Kî*r·pÔýõTºèK¥'Ç\x001dÊÙ¾·5\x0011½rlÌ@Çn\x0016æ\x0014¬Àä\x00053Ðôy\x0016»ÞW«!;~\\x0002\x0001vKF±£¯"-4+#'T´Á\x000f¦«õLe¿W³¾¸»E±õñ£i/*ÁSÒhð,í\x0018<¿`£\x001a8bÐ\x001c¹8;E½õD±£WïK[û½´õ\rßØ/\x001cxÁ\x000bÃÜr¸¨\x0006·îrëEÜZPò¨tF¡ZQ&'Óß0°Tf.¹Y6âªîdzÇRû\x0006ÏÝGC\x001cñÎ$·]r»tÌ5¥FÑ\x001dûC>&1?\x0003ÜuÁÝ²!·|£]ëxÈ\x0015-óàFr	gû.¹_:ä9\x000f\x0016È-ÃâG&\x001f)-m W\x0016\x000bBiC¿x\x001f;ÇùÝvõîök\x000e*m~yöL³^âþ\x0000³<ÞXx¹KrÀ\x0017Îô³õêÝéû\x001c[Êÿ·¡Ò^©}RîKMÁØÀÅ{CÓë»ë§oß`>¦Í´¨,Eº§*â\x001f\x0008K9Û¡\x001e\x0010ìÃ!ééõÙÛO0)0\x00197Û/Ûoß\x001f¾Å¾ö)}\x000b¥\x000b¬òÕÜ\x0005)æ·½Q±T\x001dJ/\x0019û\x001aC\x0016\x0002
]
ý
_CY'Cåu'#r³Vø\x001aíßb|Eík¤ò0¯°¢°í!5\x001e\x0002ëÁç´(¸vÖ\x000eÜ_\x000b¾D¬¿D|\x0005åèO~£,¤Â\x0019ï\x0016^Y¯ü-¤«ÚÑ\x0006Ç_-ÿ2Ú*xÓæRMÜ\x001d{\x0014ÅZ¥9»Ãô\x0013ÈL´]ÁëÓ»ïÓ®\x0008LóôÔ\x0007\x000c_\x0011Òsí²÷cò'«Ó³««ImÔÎ#ut
\x0003)+ÂhéÜ\x0014é¤2Vc\x001aç¡ÚRG­$÷\x0019\x0000SeÂHÃªé¨ª~5oþ-=³Ô³m\x0003/Ø½·~ÑôG\x001a\x0014¹b\x0019`Å¯ó\x0007ÞyOß&I|ÀAá¹} ?æ$
©=ëà{=ÐÃáÙ+ïÓå ÊGÆÆª½\x000e6~Ïô­d¹v²á.S\x001b¾|>´Ü%>ý¬/ßUÂG#\x000c¥UàP\x0013:xº£Nî¯\x00109!Ùô¯ÊÖW:Þ6'£\x00191¾¯2ï»*ós¸±·\x000e¹ø£'É+à.\x000cfLß·Ûv¹í2n*c\x0008ü¸S¾È\x0016ÈW\x0019lj×ì^ßÈ ð¬\Gï\x001f·÷_V'Ê«ÛJÏ¬õ	·w	¥
8\x0002ökûýf}þnõy}6x«ü£\x0005\x001a~ñÆvB«ë§¯°\x0017w«·O_î¿Lmy1JÊ\x001eÀB\x001c^%Çp\x0003ùÆ|g¯?½Ýx²zûióþÓù»±|Læ·\x0015¿]Ì_JJáW*ýá\x001f,áø[qÆWðTû´÷\x001f)ÿ¦«¶}üuwÿ}j·A¸\x0004\x0002ûI\x0003)yé\x0008Ç\x000c9\x001bý\x000b\x0016ÓÇõæÃÉùÕh\x001a,3.³ÍìÁ´£\x0017µµ\x00049t\x0014ü \x001eÚ s]\x0017Ù-@¦ÈVF64ÌùU£#\x0005g{g´Ã$*\x0015}~¸ÝM\x0017Ñ¹û¼"Û\x0018\x0015)\x0007)õ)<Èúùâô$Iç
	W\x0006×Ï\x001apoT\x0004süp?µÉlÌN\x0012ÌñÅyje2tÜõeÎÅ^æüíãÃnZk&\x0013$×BÁ\x0013\x000b_Iä¾Ü£"±o7\x0017'#mP04#¢%DA\x00070ì}Ãcêgpûx³ûíyªíçØn\x001e9Lüß¶w«·wÛûiå{(_Léï(ïHmåTà\x0012Cx\x0003ZÁdÃí¶z{¶>?.¾æ0ÔþrÃ<äîåv÷óãîËêÿÜNLÂN\s._\x0010.dL\x001b2ø`}öÃæäÝêÿå`;êgRÃ~&¡ÓD,w\x0007\x0018h¥¦}`(K\x001a]X\x0008lÕ\x000fÔ^\x001eb¹5ÐÒõ\x001e¢ð7{i£w\x000f7«?î¶÷««íãi\x0001m+­cYÕà\x0015)à¡¡LKB\x000c´a'M£ãÕ\x001fOÖç««õæ\x001dö#-\x000e=úC¼#ÁærÚõ"ô@e2h6
\x001ean\x0007rTç±ûÝ/e¿ØE$á\x001düÀÃ®\x0006:hÎd×\x0015»^Æî\x0002ê«$v¼_ÝpË	¡\x0007üÙ³Ø¥¨Æ]\x00036yÑx¸X!x.NÅîkÂÛ\x001a~áf
Í L\x0013Î\x0002ÿÆÙÂþèõ^K7«÷,jà±ß|V\x0016Æ@qÖ8Ô
\x001fÒ-äÍ\x001b	UGJàæÝÃ4l¥\x001d\x0017]i\x0001·z\x00165\x0015Qd/r8¤]B5ï.P\x001e{\x001cµ»D\x00005-\x0019¬`ÓSWP°Z)£YDAI\x000f^\x000eõlcÕ°âÇ9¬E_Jcº\x0003éè\x0005OÕ¥Ò
Ôh¶¡\x001aÕÌC\x00156WfbQl Öt\x0002ÃÄj\x0007*NX­Xñã\x000cV\x0005ïOÐX$màÝEá\x0014/â@\x0006F\x001bk\x0015+ªjµ³¢êuö\x0011Eµ_U$Ê,Å@ZÔDNí»VïÛÀÒ×dÓ¿ß=þºE\x001d	dþq÷x
/Ð?|x¸ÿ¾ý:­ÀÞ
KªÒÉÈ\x0012\x00150l\x0018*ïF\x0013úýÉæÃ\x001a5%ÎV?lÞbdúÃÅùÕúýÈF_g\x001a'Ïx­¯#í
Ð@}\x0000vÂÖAK¾ª¾z­¯£,^-åëd\x0013Ü±Y_çåÛêÛ×ú6Úµ\x0006ß4æd°ÿµµVm\x001dój[\x0007î¨hèëH®UÀÌ29Ãµ
\x000b¾­¶}µ­ãX7uÓÐ´u|ñ£ù!ÄÙ_G×î\x0014ø\x0005ºS~ÜþºÛ>%÷íãÃýL2È<m{£BvXXI7°u^\x001d>\8YJ®îÓÍÅù»?½\x000c«º°êw\x000e«»°úw\x000ekº°æw\x000ek»°öw\x000eëº°îw\x000eë»°~6,fÙ\x0011¯ötYÉ]ë
Âg\x0010.qOl©E«4Vi\x000eæ\x000c'îº8\x0010CA\x001c»Äq6±\x0011i\x001cwê\x0004b®\x0006\x0010\x0003µÉíÀRTWOì8Q×ø¹\x001d\x0017\x0001È\x0001ÑÄ\x0019Äõ¥¶àV³\x00142\x0007bC l/,\x0019Ù¼\x001aruµÉ\x0005w[j0Å>=4°\x001dáÅ«-dY]prÁ
çHL^b+_K{3n`ï
TÎ@®®9¹àÓÔp2\x001dpOd%_ýÕe'çßv^\x001dÑqµ³4ÈÑñ\x0001ç^mYT\x0017}ã\x0005x\x001bG¾ô\x0004\x0013+ö ñ«quíÉÙ÷\x001eöo¡7\x000b%?±,j\x0002óM=àà\Ý{röÅ\x0007\x000b\x0015g'd\x0013I»\x0005÷O¼Ú(W\x0017}óa Ð]íøY\x000eouÃ£<$\x0013Ñ¬ª«OÍ¾úBiö\x0001G\x001c'vXål\x0019åW#®®>5ûê\x000b¨dÑY\x0017´û\äó"ÄÃÞ\x0019Èõ«nöÕ\x0017'¯µÄÂZM»ÏÎ) \x000fD4f WW}õ\x0005Ô×¢S\x0019µ\x0011
!³OÆ
É²Ï@®®>5ûê\x000bÆpÑAíkZ\x0018åT6¯·«OÍ¾ù°]-\x0017ØÝ>ï=-\x000c?Ì\x001aÎ\x000câêêSó¯>\x001fh!ÃÎµxVs÷,X\x0015\x0003=(g\x0010W7ó\x0005Iºíp\8jø\x0005ÈL\x001c\x0006Dzg\x0010W\x0017ñ\x0005].>¸E4\x0013Wu\x000c\x0003\x001c3«OÍ¿ø\§ùÉES¸#ß"¯eÂéêÚÓó¯=£8Ñ\x0008Y·À«b¨vz\x0006quíé\x0005×#ÁC \x000et\x001ak>í@\x001b\x0019¼Õ§çßyR\x001eEG¼l7»ç}­sB×ÎÌùo½\x0018í&\x0005%ç\x0002fYÂv@Àn\x0006ruáéùo½à¸¹5ì;
4X%5\x0015v La\x0006ruãé\x0005o=bÝ\x0019ÙQù<<öL¹@ä«-äêÊÓ\x000büþhÿØ£AØ\x0007²f\x0010WWïä4ºØôJbÊ|vÀqù¶s\x0003ºÖ3«;O/ðrÊ¢~\x0002'ÝyÒ\x0014\x001f@|µÍW]yz¾\x0013FÏ\x000b8=ù\x000cËÞóòµn\x0010SÝyf¾SÒô\x001c\x0016²bÍHç_í6Õg~¯±;x×q\x0010ÉÍÝÊ³í5`ÿ:­v\x0012¶³\x001e¾ã~r\x0012Ì¹ð¡ºpwëßß\x0002ü\x0011fcê@\x0013ü¢SÄt¶½TiÊYeû99E\x0005|:çê¥*®N7ÃÞ¤v³/páMpûÇ»ï·ßáïgO»ïß'¦ñc­¼xu%¯N\x0015×\x001dð\x0006qñãGì\x0014\x000e?ûtruUÕä÷èC¨[1á/0üüññá×Ýý\x0016u´\x001en~Ù­Þí~~ÜÞßLì5\x0008öfn 07å£âüª¡þA\x001f7\x0017\x001fNÎ×¨§u\x0001Ë\x0004¾É\x000fõùñÈ\x0002!ü½?9áü@/AT2¤Ú\x0004\x0005K¶²\x0003\x0019\x001aóùCÅ\x001fò©\x0014\þ\x0002p\x000cæ²ªÇ¼Ò\x0003¥Ó³¿@WWÙ'\x0007Ý¢/àEêô\x0005\x0004wWNQíWjàôÿ\x0005\õ\x0005ÜÒ/ïd\x0015ò++HGíl~]ñë¥üèvÌ½*\x0006C	qØ3OQ\x000cøU¿©VYºUT
_ÀçûT\x0005AùÀo_i\x000b_Ã¿¬:Aßb2 gpä§ZUøûÕte\x001c\x0000Fó*\x0019\x0002Ñqó58q8 ì\x0006L-TøOµªð÷«,3È,ªQ\x0005Oýï»¦kJDr\x0007©O8*\x0001ÛUüìéýñêäÅ«	 C\x001f2 ä¿=~ßW¹¾\x0015q?± K&\x001d\z\x0004Öa®èÂ\x0017\x0004\x001e
ôþ·ÍÕ¾Êýó),ó«¸¥U\x00157:7gk-Üc³¶d§
-gÔÖ<¼(\x001aÉMÄMÈK¹US Ý@¤Þ­6LÖB¬\x0000¶íáwäY%&\x000bèÒÏ>£ê2ªY^\x001cQ\x001d¾µT6
\x000f5×áËÃGÜdDÝEÔ³\x0010QX4P\x0000*«\x001eJÅ]8±ÉÍ2DÓE4³\x0010QöÙ\x0002´¥M%ÁReFe\x000e?f'3Ú.£Å(ÝQdUeC!l8òXá"È\x0001êÉ®Ëèæ1JnÚÿ¹5TÒF\x0003®ûÉ¾Ëèg1Â\x0019oh9f\x0001·Ì(\x0011
´E¡Ë\x0018æÎµ§^yVs\x001eæ{\x0000\x0007= ô=1v\x0019ã<FMoçÔÏ/×Ê\x0000#ËK¡\x0007ÆTÆ*Op1wA\x0006ü\x0000\x000b\x0007Rí\x0007!ëkfÞ=£\x0014U-Âq\x001eQ+¾f\x0006	\x0011«[FÎ»f\×ey\x001dÅMq \x0018w2duÏÈy\x0017Ôò#£¤»°t©u\x0003\x0012\x0019«FÎ¼iö\x0010HFó4\x0003\x0005ù!«FÎ»j-»\x0006Û1ÑlkÇê>6Î»jþ\x000e|qöïøGÜ4\x000fßo¿}Û¡ðÆ
;­o¶7·ÛIö»B5âÛ¥¢ÓG©³b\x0000ã8ð3I
\x0014C]\^^ úÆ
\x001f\x001eëãõñéúr[u¹ÕRn°42¶u¥OR¹\x0016`\x000f¸Çf`ë.¶^\x001d¸@\x000e®¦ \x0008ÛÆò(\x001dXÀíØ¦m¯\x0012GÎ\x0000lYhhx]\x0001¯Æm»Üv!76±§ÚI#(ü&<«z°[\x0006n°vn×åv\x000b¹aqÐpkîT"¼+¥´bèaÒí»Ø~!6ÐY^&\x001aÙÌÍ=r¥\x0018\x0008kÍà\x000e]î°t¸-ë¼D+\x000b7ëöÁò\x001e²¼Û¹c;.]ÞûmiÕ\x0011¯îâ¡\x001bHYJËØá£{1ÿâ
~|³yxú¾[}ùÿü¯f\òßÉ7W¿<<>îîo\x0010Rû;Àë5ÂËú(	©bü3\x001dy°dJkùÇÍæäüøÍæâÓÕÉêÝêâÏëÃ\x0002D{*Êæa*4P¦SI»À\x0000\x0015öþPÓ\x001f\x0000+æ\x001a\x0019X±\x001e¬Ø4XØkRf¬àðfNXT\x000c\x000bUG9\x000fËÓ=FXø±\x0001Ë¼Ð\x0000+:jèbÈE9er:u;V°ÕháÇÉXAXGË	\x000c\x0012È¼¶"yGTv·ÏÂT+KX1\x0015ËNÅ\x0002³9À\x0000(4\x0000Xðç,0\x0001XQÌ\òÑÖX¶	\x000b\x001eìéí\x000e(^F¶\x0013J\x0012\x00173V¬W|lYñ\x0001ãkI
IXò\x001aþli#z3\x0013Kr1\x0001aåK³òÏÅüÖ\x0000.-èÜÛxÞ\x0001!×5oØ\x0001µbÊF\x001a#tj%®\x0018èà\x0006ÝM\Y.Íí\x0017\x0017Xa.T²\x000fw\x000f»\x0017öbºû\x0012\x001ca½\x0018òÝ\x000fo4U²«#\x001d{qv±9¬|¿gºËV7ÿzM\x001a\x0013Ø¤ÌuM8f¹Ã"°ÙÜ¤l\x001e\x001b\x000bÁ\x0013[\x0012o\x0019¸àóMädô2ÇÊñ´È1	Ãî½\x000bàB
×8«Q¡îvÃ\x001e\x0019vg®£QF\x0006ó ÜA1à=\x001d©Ê1\x0013ítèLÊðA8ÍlÑ-\x0018¸z7ÈÖí\x0010mn«\x0000hÔQ\x0004Ñèf\x00026µ-ÖÃ\x0016Û
NÂ,\x000e\x0002l"ÒV£-;H\x0015:¬ü|8¥c\x0017\x000e?6ÁÉe!\x000cx½ÓÈÙÜÿ\x0010àd.w	ç|\x0005×û~\x0019Îç\x0016\x0000§M®`@8Þ\x000e:Î«§UµN+¶QÉÓåoàLN\x00048o\x0017¦z&ÃMpò9ôØ\x0010à\x001c_\x000f¬¸4\x0013®VÝ:­ÜhÀaÿ¹\-÷ài3÷CW\x0013'ÿ"kâäË~·zûÙ#d\x001a_L.ß\Ze×±wZ	¾U½
\x0007nûÕÛ\x000bÌ\x0006\x001c&ëúò/Rï'\x0002û¶ú|»{úûêøýßûÝ¸\x0014±ï`Zt\x0002\x00190tAÒ¢ÃËõ\x0010àåêóéÉ§GéÑó\x0001¥Ù=g÷©Èk\x0006(ÌqªÒÇCOä~É\x0006à\x0013Ùú¸\x00184Ä.hs@ðd¦KÔû
ÙL.§àÕqèMÓÄÉ}3,Ï\x0000Å¸/b'èl¸(±¿ãÂ!K´4Ö¤ó\x0014ÕÇm&5ÔÎ\x001cIË\x0003-\x0002Uª\x0002Uj\x0016¨¹l\x00194\x001e¼ÔlnEqèÝFjkR;Ô¹\x001cÁ!õÙ
¤Æ\x001a&=x.5zQ¢4ë\x000cÐ è\x0004\x0018)ð´J©ßÂ\x0004ÕÅ«TÕ\x0007)~AªáÒv\x001e\x00026§üz§Ë+àÐs³
SÕj\x001e&&\x0006Ñ\x001d\x0004o&­¼bR·øR¦: ðã\x001cRãè©Hsoj§Mà©WvñÝ¤uE\x001fçFåMTJ>ó
ætE®\x000f9AHM½Ì¼íULN\x001dGÝ4T+Åv\BµÆÕTÊKÌZã_VgÛ±kÞ¬ºÝIÞäÊGwR\x0015Åß}Z­_¢\x0015Ul¢²x?f*WI!g3#T³¹´íriÛÄ\x0015ØS©àõ È\x00144»\x0004uýØjâ2Õ,¶YôB\x0005.Q<¨¡8\x0005µu³¹lÅe¸°Ý39+eC\x0005Kê9X¹\x0002 ã\x0015ôoªfñßV?¤LèïÛ¬Ã:ø\x000049G\x0014éT\x00195\x0014\x001cÈx*\x001e~Ç\®~HIÏWk\x0014`\x001d§\x000c\x0015eC)x+(:mì³÷:,´¾\x000bi};¤À×\x0002M´\x0012ä1´¹$n×\x0001_fÅ8èú"ÈXAÆ\x0019^äþWyðP\x001aWÒ/\x001eJg»\x0018\x0006m¦t>\x000b\x0012ä	O
IR©C'ò\x000cF)ªÄíøÒ"HìÎç;Ärà8±\x0018SVC\x001fg`ê#G!ë¶\x0001eð¼ÁIi	¥­!Û~\x000eagIòh\x000bxU\x001f\x001cÄ\x000cÆóm\x0017äí3éë9÷ísî#,LGÛ\x0007Ë´3¥dÈhlNæö.3T¨<f\x001f¶ß\x001eÆÎÉ(ØfÐX{\x001f.R(²d°WÎa¯ÔõæòâÓ8ìx¥$æã©F8Kña_àUã\x0008ðN
Wâ4¸X
\x001c~ló*\x0017¿\x0001zY[5Ñª\x0001Gè\x00148Õ
+7ø±
Îð¡mÍ\x0002T\x0008çxä^0rÊW#\x001fÛà$\x0007\x0017­\x0016\x0013áLÞ\x0014\x001a\x0005põ´ª9ÓÙ¬*\x001ed\x001e8MróÐ´p]4üØ\x0006va>ð,íòn »P\x0003ð\x0003y\x0012[\x0015[Ã&èÅ&°$8\x001e·\x001cü\x0004ÕÊùp®ûVÙQ¢	NäÂqó(Ç¯H-\x0002\x0006¼°ÀKpÝJù\x0017oêÑñÃÓÍ/Û\~5º$Ù*\x0010AsÛzå)\x0007À);ôl;¾øtüãúüp\x0017×= \x0016]@-Ú	IÏa<b\x001a¥KÂi7ô"JX
¡1"Ýc ½\x0001cè\x0014çèÔ\x0011vBS¡i\x001fCÉáPlÂ\x0006*<É9ÈªÙ³,rin'~áfOÇVYÿãëxS,¤Ï*9Ì³÷ºc¨¬ÿô~,éÃ÷FOäªÛ\x0016¶\x0010P»$³ù\x0012ý)A=-ìÑ)h¾BóhNç.?\x0018Ó\x0013¹\x0016óQ\x0004GCåù4MVl²ÍçNÀ\x0006¯@§^ \x001b°	½-.[\x000cml\x001ai\x0001\x001bjfd³\x0018\x001eBìà\x0013\x0003öÉ$6)T
?6Ái\x0002\x0019.Jò[ÒPÔ\x0001öÊ²pÊä:HÃ\x0012´ú*3)§p>²\x0015²l\x000e/ÄÆr
\x0008§i§¡<ipºÓpØm.±¹\x0018$¹Zx£¦æùhÖUhÖµ ÁSÖf&dìb	Q9S\x000b\x000e_84+8ß4n\x001ee
r¢t¹§Yv\x0007HJk\x0013V\x001d¶ì^ýc$ÖÇHj\x001e~»ûò³ÝÍ÷ñ4(Kß\x0000\x0011.ÈùcÇÏä6ì\x0017~zònuvr|5a\x0011Ó¡âº¤²6Þ§£J»;\x00138ü&JìUh5ð0kAµÕ ¦;h\x0006ªOÂl	\x0015^ßs-É[\x0005/\x00041ðÞh@URtQUÝ}2ªs\x001cÙ²ðúðtÕùÈ¨Æ\x001f>±P}5ªøq\x000eª\x001cÚÂÆ¿\x001d% \x0003Ú\x000e\x000bPQÙ¤´\x0005Ì¿Èm\x0001K:Ðf÷·ÝÝöñËXJO6W6¨\x0003Ö¤uj¼ÔôÓF\x001fN	Ú|>9[oÞ]\x000f»¦3cg8ÑVF)5%\\x0008lá\x001cÆ\x001bö#À?q0FÜe\x001c\x001fÆN¦
"vSm&"*CÞ`H\x0007ÝúÑ0¡9\x00132PuÒ,PuÓ,&\x0012zÎçÃ
A2üM ôVM\x0016\x0017\x0011ê#\x000b\x0008u'=~"¡2\x0011=2¡ÈÅ£ÞDI©\x0000\x001a«À!:S!:ÓèxQ3ïi\x0013ù}¬=ô5\x0019Ðt\x001eð\x0018fÓ¢\x0015PKË1H­s×]o\x0005g1ë¤Q±\x0008ÑT[\x0005?¶"¢Xeö yàd;#íÁ(Ì²h¬¬\x0010Ñ!ÕI)ùPô"¢\x001ahFd7\x0007ó¦¦\x0013ºj¯àÇæy\x0016t\x0011
\x0017bÖU\x0018©úFË°ì¼¡"\x000cÍçB[§ÙPØÆDo\x001c\x000f¢?Í)\x001eb:»9~ùþ°½}¼\x001d»Sû\x001b\x0007+\x0013ÃeÌÅÿJ-Tg°tãêÃúts:r/'¶NÜ\x000bØ0ìÕÂ\x0006\x000fzËl\æ²Méyl©}'½L	ÌÓí<\x0012>ï\x001e¿î\x001eG3_±Ø\x001cÀp/LA\x0006\x0003<	O6ïO6Ã\x000f\x0017D\x0017/F>\x0011=Õ\x0008x\x001e\x0018ó<\x000cÔ¿LÄëFº\x0000¯tMâÓ}ÔÖís\x0001¤ìÝ\x001f\x0008L\x0005\x000c¾\x0002\x000c¾\x0015Ð\x001a\x000eÆY\x0019±S~ÜS=Nµ,K\x0000c=±y\x0004±ßX$@ÎÖüÄç\x0005¬â¡WôK2\x000bðv²RôN±&à\x001dÿ²ýç\x000bI·þ
ê`\x001bkÊ·öºD«í@Îíñë?å²é½/umïO`¡á©UQeÝ*L³å\x001ex_
d­OSäEÝS\\x0013Ñ%²\x0004×WÖOÃ¬Å@®ýp¸6áE6&ì,:õ¦^rW\x000f·ßV'¬\x001f\x000fòc\x0001!óÊê¬\\x0001]if ²ãruµ¹8½\m>a¥üX¤?ÁÊÎ[\x0019u\x0014¥kÀÐ§\x00043\x001f
ææ!®T­Aï\x000eÃ6`m*`mæ\x0002£p^æ
ßÌÒG~\x0001¸\x001a¼\x0006^ß_
þ
õþò´úø0\x0016ÛÇGg'^Ìðbâde\x0019¨ZV»^dv;¼\x0018é¨~LGåÎD"0­d®ÒRNq8GZv \^3Qò×u<Ä*¦.=lÁüÏþ×É×»Ûo£&\x000cöPdÂhr­;x>Ñ-çD|>RØçøäýÙéå&YWå\x0006veoµ­¯\x001foo\x001e¾ß¾pÈ}\x0005GÒ±¸\x0004\x0003\x0013o7§Ç\x0017W§c\x0017Iæ\x000c¶Ë\x0019l;§Ø\x001b8u¤x»E)w\x000eî¸ÃÙ'
UUoèUõN\x0007\x0015(ÖS¹#åð (Gz\x001cômO\x0000iQvU'âNäó	ïïI$\x001fçv4Á*NêöÞf5k,\x001etü7\x0007\x000fÅOxÑ\%uü\x0015ü\x001c'í\x001eá@Z\x001dá-¬ã¨Ù±d²2\x0015ìoÃO\x0001L\x0006Y\x0004kzÇ!LR}9~¸EçÞèÍ
g~nKâ0ÃÓ\x0006\x0002\x0007G\x0015°\x000fY\x001f`âÏGSø\x0013`§\x0003/1×Hè±`¼èí¦UPd\x000e×æT@_\x0001úf@oÈj\x0014\x000b3OpÒp\x000b\x0001}5¾}\x0004ÎÍ\q\x0004-ÇJ}x!\x0007ó\x0006¦\x0011ÊNE0\x0010J%\x0011æ,ká9Ðz¬\x001d#ÄÁ£òEDÕm1ZÌt\x0008_¬vñØE:ÚÌÔ-\x0012Ì\x001bÃ{yðeúBKë&\x0001®\x0017\x0000gù\x001dà\x0005¨-Ù^|cë¡Pø4¸jälóÈ¡\x001e\x0015E\x0000ðÑLlìÿ×\x000fÁ	pý´)Ó¦ÀÔ¹»Kö×UÂø6ZV­bÌ
*Á\x0008½áÉÖ¡ëÄÅgÞ³³d]¥ß\9º\x0012W]>¯ZùÀÎÏ\x000bÜì$ªî\x0016ü^öBö]]\x0001éyÐWZËðû¾{üm\FxzWµèøí'tä51T\x0008\x0006ãÕÉæãXô¹Ûs2ÿ­Ù4S
úÁ-UéY\x0018
Uè|)J¯£Î<~/\x0017ôë«\x0010ÐÈU8\x001dMp:\x0017Z,¾WÒ·¨\x001bÙ|5l¾qØ|ä¢ÞÐy-éÏõì	0
M¹´æ:'C©Á¦ê\x000f¿Þ®\x0003¦åÔ$°ù0wN®<æ\x000e'ê¥êÃ÷çÔm`hü\x0012d7Å½©\x0012YÐ\x0013Û9¬\x001fF#ÉiùQ¶2\V·c\x0011²ãÏÖÔÁa\x0005æõÁ\x0001á§¿ÜéíÓ?Ê5c©R¬ðx÷ÏO2gÁ.¹Ú>=¦\x0000 aÆI@eI\x001dps>\x0002\x0000+ÍÍµZeÝéõ§M2î»¹g\x0017WûÀ1ÿá\x0019\x0012¦Âá_
HA¦t}dò\x0014Ð\x0006&[\®\x0008Í,ô£\x0001
Ã¸\x0002P\x001e\x0006*©2)LA7\x0019ÊÈÚ¸\x0000
çNµM\x001ezÊ}R2wÜB(|dd(µlöRZYúÑ6R¨  ô~¤0.¡ÌÒéó\x0008å[ àN2²\x000cå-Cå¤÷ùPx´¦\x001f
P2Õ{$(,SÎL©\x0017db²~\x0019Â%®\x001a×yH\x0005È\x0014tÌý%pó\x0005ZRäZ¡Â×ÅB\x001dÍô£\x0003õaû-=¥×ÛÞÀELnÊpØY"©)ôÓÁ szÁ\x0001¶\x000fëKxG¯?¯Ï¦\x0010\x001a$4ó\x0008uR\x000e"B\x0019\x0010OzB\x001cÓ&DJ?f *Å³TÚ\x0008ÊÑ\x000ck+N²\x0016DV¸Òó\x0010m² \x0013¢\x000beQ£n\x0000ý*Ý®ÌLÄxDè)Q¥g\x000e\x0011R+yÿ\x0016ÿ¡ùVó>ù!Ñm^éS;P\x0019ïÏ÷\x0001ùd*\x0019ò\x0013©(\x0002&À`ÎDG\x001aèE\x001ax\x0012ø<F\x0006FËä1ÊâhÆ°\x0006o%e\x001bh\x0002"d\x001a3B\x0006C\x0014Fè\x00054¨Ç¡\x001bf
h$Ñ (
_\x0012çl>
®i#\x001ah\x000c\x001b7\x0006N-oGa\x0002¯\x001bëÕ\x0012\x001a¸ªo ±©è\x0010iTÈÊ\86Ì"å\x0002\x0016Ì	q-ó¤S\x0014\x0004Y°o"'\x0018j\x001d3\x0013\x0006.Ú7¡\x0005&\x0015õ#Lê2\x001f	î\x0016©²\x0018Ô<$i~4\x000c
]ÆZªT.0v·0nÁ
\x0005,;B¸SÆ&ä£Or«¥î~F/9ùR9yú1ÆÅRl°ï)ül`°#\x0014óp\x0002>kC'ôe¬\x000b¯\x0003¼CÙßÒåý
\x0007âüXbpñMþ9\x0011\x0007ö2ú9\x0010ÇbÕ#\x001bÓå£Ø ;p>O*ÓÉ?§òÀ æá]+ñq\x0010òÛ\x000e\x001b\x001f-Áq	gú½6-ÑPÍ5Ð\x0004ºÄ¢~13qðÊ?§âÀ5Jâ±G\x0019'¥xÒà%£\x0013\x0013N\x0016v ÉÒß¼
m	\x001aúÍÛÆêÙóÏ©<F'ù3ä\x0011o+­'\x001e-æ<2Y§ùçd\x001eGÇ2ð#ÂI.»£â½=ÓÞäqBÒþH8>Ëí!æéRaÁjV&9MÌô{\x0002ûyÀ$\x001e©r*òø2]jÁY\x0004òÏÉ<|§§ñQx-ã³`{¥@xþ9Góá#\x0015\x001f¸xxæ_êÀ\x001c7
¦`´¶\x000e&
*Â¡'ÄâÙgúÍ\x000fS\x001d§¸&uª7%\x00058\x0018ÓÍ?§â\x0002q\x001c6\x0010Ì¯Ð²Ý£Ç§£Ð7\x001c!¹û2NêJqd°`x4&\x0012çÓx0É<ÚJu_Tê^Ev2\x000bÎ\x001eñüs*²©\x00035ò\x0018ÓV\x0007½VÇ,x\x0010Ë$¬Nå148(ÊDã\x0014-\x001eíäÂ¤{ËL¿·Ù1`£Ð`WÌc\x0017ÌMôs*\x000eúAóRýxV\x001bÔp±ÕL\x001cìkNÄ\x0001û:u¶IFã§\x001f:º¨\x000b¶ºEnþ9G¥\x0016Îy«[ÞêÖ\x0016Yë\x0005<>ð~º	¯$µ-ÔhZÈÜ5\x0006,\x000bÔóO<0Ø\x000b..æË·Ì|\x0014b)\x0012]\(sÂ<vÁøä\x0016L?§ò8Ïf\x0018&v\x001a\x001a\x001fÁ»K*ßóÛ­ù"S\x000fÏÀX\x0012^·ÿHQåÁ§:í1­\x001dce(nÀÞ&¥e
3^×êö\x000f\x0019Á\x0010Ò
4ÅÛdµÎZÿH\x0013É¡YB#ük*
î+M41+(l=Ç4¶Ç¶ÒÀ2ª&ÐL±ÓÀ\x0007Ç(zÑÀÀ÷0
FÐ5.·9B\x001aUh¼^@»Ñ\x0016b\x0015?Ð\x0001Ê)¹\x0000\x0005Cc®ad,ë×vV\x000cÇJ[²`PdÇ\x0006@scáÄ	\x0002\x0010Üp`Üª%4`xÛ@c¬\x000eÒxU¼pÎÃ´÷vhcA;44BEÉÛÿ¤%SHÌÕ+\x0005^O¢e"Ç×,¦\x0010ðáàPn\x0001L.3/+M§XÀt\x0018&¦\x000bVp*ï-g\x0008di\x0019§¥%,=ªà\x0008K¦*9,LÃõ\x0001å=\x000e5VB³`CÉä®0
çðhgÀËØº@4F,\x001aôiØßBq®\x0002ÒðÕmKXÇö\x001bê/ÿÏ?õ_:±×nløáéîö~7?¡\x000eäjOq\x0008zG\x0017iÄ`FÎOg§ç'#y\x001d{2sÕNæö\x0011r\x001aFç
ÕÞh°\x0000t3\x001a¦¦ËFÑÐ\x0005£
¥\x000cµ Á×3íhåpJõðDæ\x001dÉÁ\x00062Xó¶Ì:¾ø1ÆD\x0007Ul\x0008õ\x001aÓ	\x0017k'³|½¨hÙ%\x001e£({@¼\x0006\x001a,	ßf16èh¥qp%
«80G¶\x000bÑàß\x0011ÚG-rt\x0017GOhËþ¬Ã»-hÛÊÝ.v\x000eµwÛh{¹}üm·zûøôu7\x001a_UïbEÉÈ\x0011IZ,\x00190Ôá>­s¢íåzóñdõvóéýÉðSrÏO?ük\x0006 å´&\x0013\x0015\x0016²e£Æò\x0003AÔ¡úÙü¾A¨S! \x0012bOÇF``BýJ\x00193PqB"jQse\x000c¥{\x001dBØ\x001døW;!ÖC3¡Ém¦ÐVä"%äë¬CÎç13MQ5,ò\x000bSijd>\x001fÞ³óV¡8¢\x0001Äf/<\x0014>\x0005>û:\x0010ýÐzÞ"L¦\ÞÈ©©X^<JÖ©u³	9IêwL\x0008\x0013læMòÿ*¡òOÛÛ%Ú)\x0005;Û>ý\x0013@Fñ´ö©3åâQÍò6I·ç\¼ÚiÑ)\x0007;[ú3ün\x0012\x001c»Zéì>7µ£Ç2øôeÓÉ\x0014èµõ6x¥\x0012A\x001bO\x0012¬Ófë*Ô&Ì\<|\x001aJ3\x0003O¢\x0013*áal;d¼i/}¹6G,Úñà\x0002¡ãYçÐÇV0u:Â<ºÔÉ ng0NIO\x0011B£ò=tFK F/æÏíúþÛü5\x0019YÉCóæÍûï»ç\x0010ÃïmwD\x000fH¤	%Ê\x000f\x000e__\x001d\x001f.Î¯NjQ	hcü;DcÃï÷\x0006F\x0005þõ;Dc;àwöëîá«þÖõ´wë\x000e7Ûoßw·£»T¡qíY§Ø_iæôEg«û¡[v¸Y_^íÒ\x000e\x001eü[Ç\x0011\x0001às\\x0005`Uà4\x0003\x0017\x000fWO4òá-\x0018fðÉ\x001bùH\x0000cÇ#ý.¼Æø%Ý´ô£}\x00005Qhg$çÑD\x0013#ø

ýÚéG; à\x001c?ÿ\x0000%Ï°	\x0003®I¿l¯\x001f\\x0012òÃîÊÝ\x000eËp=~ÝÝ£ÌèÞµ=\x0019`,qr\x0014%¤ª\x000e\x0013`µëæýÉ9ÊÈ\x000coß=]¯¬`2\x00147VÛÜÞ\x0003K^+Ã¸C&­t%VÕ:v¡f.\x0005¹ëï?èÑH·/¡lÅóËe»,Iÿ\x001a\x0013d\x0016ÓY\x000c§\x001ft\x0011;Îûò¸¥Ï\x0008ö_È(\x000feí´âa¤Ùvj\x0013&â)!,e\x000f\x001a+\x0014'\x0015\x0019EI3VÉ©Ë­xX\x0016~´âIY¼?\x001aÍc`Òr\[CI"Íx
ñT;I
/*&K+t\x0003±ûL\x001d¬\x001ahÃÆ¦Ä5Û>|R[\x00188×\x0016¼\x0012~ùÎÅ:\x0017t\x0019|Ñð¹gÈj	*8§ùY+Ãòéèä6ò)ÍE*ðö±Y:P\x0005/(Ôb¢;HßÊJy¢o¾ÕõgóøIë8÷×EM)o!¾ÊøåÊÞ\x0019Û\x0017ß\x0014ßÃì3
¢¹À)y!\x001cÌÝÆ§o{,:,\x001dçòåööþûêOw·»$ñöñöáéËøõ+°ëC®¨ã\x00102¬=^æ\x0003÷r}z~µúã§³Ó$ñvszñéÝ\x0014\\x000c\x001c:¿\x00047\x0016\x0001\x0016úpâûX
ó
¼ÒýÇcøþSn9Ôk4´z»{üþ!D\x001f#Û¢*Éb@c/=êúûÌg°z{²¹úÓËL©}ú1É)Á@ZF:\x000c1-ëñZ\x0004¥SºKþ9
ëÝ ìºó¬ÓâóÑÄòróÝ+/PýüÕýý/úpdþãÝÃ0\x0011¦\x0019rx\x0019=(\x001dDèÝ§Õ\x0015Ò\x0005>]Láy\x0016Y\x001eç±(6\x0000Jmæ,\x000e {\x0019\x001eÍ@\x0018âÒ¦H\x0017G\x0000V;è\x000c\x0014Ä¾èu(<
3Ü\x001arÿ½äAô\x0014h\x0004"\x000eã	«
\x0011Z^·\x0010\x0005Y|%[^ra{«Mäùúø«ÿró°\x0002÷Xþy6Õé÷g¼L\x001d"Ê*ªXgüÿÕÝ\x0014_ÇÌ\x0006üël»:ÞÞmÇ\x000fp£¨¸\x0013Þ\x0004ª\x0014\x0006GöGËj­WÇë³õÈQ½§`ÏÖ4XC\x0007v\x0018=°\x001c\x0019nãØýý}øKâo ÷´gÛ¿=Ü>Þv¯\x0005®\x001e_^Iµ!Ó¦ÎÖ/N7<ß¿}½ÿË¶»£Îv/­[+RW ´ø|ÌBúxØH\x00066V­IZ±7Û/ÛoßÁ\x0016â?\x0010\x0001näµ ÿZúÅ\x001bÙµ¤þø°½¿AB£Ü÷`\x0011ãÊ¡ø([ñÊ\x001e~£ýñb}~>-ÏtYùé´i¢sÑrì\x0007+x1ë­\x000e¹O§ËmM®êj2JÞ1ÿ³8E,Ù
\x0007&£ºhV%ÛØdÉË³øúá«¿¤6È\x0001Ôd<]ãéF<¾å.\x0012Ý~^²Ô\x0002:\x001d*:\x001dÚèæäeìZo¼¨\x0014G[6vÖVtÖ6ÑÙ`Ø«\x00128\x001cbÉ9?\å7.ÔçIh;P¬|ÿ`µ\x000bM-¼kyj\x000fKA4àÅ\x001a/¶áY.J^\x0015I£gKÁ>(3\x0019Ojôh\x001c½\'ð&§Ç2EÆ;X>>\x001dÏW\x0007\x001e~lÁ3ð:T<¹Îcï-ûT°Î"¼XÝ\x0016étoÁÃbwµÇS\x0019OwPKg2\x001eþ\x0017»l;VàÖO²t®P¢\x0017eã\x001e\x0014×Ngª¥§MÛÒ3Â£üÇ\x0006²/óI2\x0008\x000bðê»V7^¶ðåT\x0001\x0013\x0002U<zg,1Ä2SÀdIyÆÃMx&ìÍîüªu\x001d?ü@`*ª.\x000c£Ú.\x000cL?,\x0005fHäÀÛàùÕíã2<ç*<çð0\x001cy(\x0000\x001dp¦ð\x0013¼ç¤h¦\x000b!eB!\x0002Ô<±*²\x0000m\x0000Öçò\x0006\x000f{ñtð¬hÄÃÎkDçÈ
Ç\x0017?<íAYµ\x00068]ÃµYyÊå\x000eÎ²-`"\x0017¤ám¼\x000cÏÖxmûB9MºL\x0019Ï\x0012
¯§ª\x0003\x0019?6áa:\x0019åOkMÑ=\x000f§\x000boÛeV¨U¡¦k»Ì\x0014lUÊ{3Z\x001eQæ3¼-ÜAq¶étº\x001e;Ý8vz¯~¨\x0015ðØ/ñä²¡U×v[(íØ\x0012@<Ox¶\x001cyráà¹®ñ@Æ\x0011Óeá\x0011j¸0Cöë}éê×ø8\x00033©\\x0017ÚPØÖÃ#\x001d\N/\x001a<W\x001f*®ñPÎ°
÷\x0005ÈÉÓNÊAAª\x0006¼Úe!ÚÌ(¼\x0012\x0015Uåy¦÷©Øk	«n\x000cüØ'\x001c»-Rl\x000b¨ÈV\x001e<\x0016Yy.TûÖ¶}+ç(\x001eí\x000cåeÁc¢\x0013ñ|íËóÎ<\x0001oï²q\x0005\x0006x8\x000b}Ù¹Ö\x001e~Ï
¯mk`Î2z%ÛW©½µrPNj:^}ßúÆûVÈqE\x001c=O«ÞèÒÑ3¥çM¥'Tà,3##\x0016ú§°G,qÏÃBÓñluiàÇ&<©÷ë(UÊK¿×Ô]ö\x0006
µ#9´yEÔvg9¨&Ë¶]f«u\x0017lÓº\x0013QÆýaØ\x0018\x00106êW¡µ1\x0010Û\x0001P:6|v$»X*òÁVYd
DWÈÑ5È0þï\x000bË]ÄÎ^¯rÙÆÚg\x0011Û|\x0016\x0018µ-Õ{Õñ\x0001O÷Ï2K
Ófºx±máù H\x001b2]¶Ù\x0017	4û-»ä6XÚuÕ¦Ô\x0006>G\x0019\x0015h"çóÄy\x0017<wWèÜPuoÂ\x001b0ì\x0013öK³ÃÃ\x000e£f&Ö}ÔÌóÄV\x001e\x000bNÖ/-\x000e_²\x000b×-]D§<g\x000e\x001aor\x001b£®¨\x0012¶DXÈç*>×ÊgÙgÙ¿¥r\x0007Ï×	<íxØ\x0014àukX&ááð,=\x001d\x0003¬Ýg\x0016Î®ò\x0015oÅ3E¼\x001e\x0019Ôô SLX?\x001egðÅ/¶Î.\x0018¡ä§¥¥íÈXW;´ãiÛÅëÖÚL\x001b>_n[2.úgå>3\x0007+m\x001aøªE·\x001e-ØxÌ\x0015o¨a>+\x000f{.ÚùL5~¦uüÌþÒÐ¦ðí\x0015»pw8ÑÅC
Â¶áKi\x0002ùN¥¤¿¼^'E\x0012òZw\x0007K¿\x0004ÅÅ@¢ä¸ìì¶æ³Í|Öä´áUÏÉUÎ/»:d=½²}~\x0005É¦&>ò¬ãÜ²Ã\x000fîÆ\x000f\x0013÷ø¬dÏ¶Ì'\x0005×\x0014ðY3\x001fö§ë\x001eÎ¢ùtAëOp­\x00176¯ç\x0005èç\x001e0V?åJåý/rÍr\x0011íL,£²02bý~^
Óºó\x0008\x001a®F7Ñ»Ã:½é7c¢0\x000cèk@ß
\x0018"«ì)a¸E\x0011,u\x001a=¬ú<\x0019poÕ'ÀU?\x0011P³Þ¨\x0015\x0012u´\T\x0015.K\x0000Õ]@eu+ á¸,þe\x00004%s åÍt@[\x0003ÚV@Ë1?©%\x0016èè\x0018Ð\x000f4\x0015\x000cXO±jâ¤ômháÀ¦=¢©\x001b	î ¯¥/Ö|m{DË¹\x0004RÚ\x000c,R+3gøZXñ\x0013üë\x0017ü-üâMú	ØÍ,\x0015=üáäÛo·£Ý\x0008£ÍÂ0ÚÔ)Ü¤¾\x001a¬ü¯Ã³dLìd+\x001dN.?nN ýOÿqûË7$9Ð\x0005©êlëË»Ý-¶Zã|
\x000f`w»ûÛÝÓß\x0011M£NqzÀ\x0019\x000b/5Õ§¼sBåþ©\x00127sb;;9?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Ý\x001eÝ<\x001f½½8°x.TG\x0014óå¥ÿ\x0015ãJÚm¨Ü°ïëýùõÕÕæèäúèíÙùËÄF·ÄF/&ü¹ñy©ä{1Ö,ÀN½o³Íø1¢VìxßàóáÑÉÏ\x000fÏ7w\x0007ºNJ?Ð(ªC÷0\.´
ptÄ>à7øxt\x0002Ü'{U¶À©\x0005N\x000b¥Õ!ëd#¥\x0014°ß.¾`Å\x001a`Ý¯ðÒ%F_ÛRY²OØ
8¸²|S\x0007_
8wÀãS7{¡R$£UÙy¤Ñª\x000eËï=uBbã[b3~\x0007K\x001dgJS=³£\x0014ì  Ë\x0005Í¯µÄ¶Û\x0013vé\x0000Óu\ÊRQ¢»ô_P}#¬\x0010z-àníÒ\x0015Æ9*Æ\x0001±¼jà³FfbõZK¬Ò6ø.âfá>v¦¼¶ÂÁs\¸\x0016ç<AÐæÕºmÁC@­¿,[ìä;nê:ÇÈÎLÌ]Ñë"p­Æi\x0004µ{Ðòûûþã@16¹4VfdE±p\x000c(ê;¤³´Ý»7hXù	@Ï5-ì¸Üh.,Øà6\x0000W²ª\x0011þ¾:êý.\x0008Ö¶°ãò£Ù+\x001b¨~\x001d\x001c\x0014Ó\x0003­NßÇÜÃëÐºÖ-£UÑ\x000cÕ!\x0000kR­ær²Úï-æ±5,bu9xJ_+½-\x001fp4\x0012`uÚï©Í£\x001dûiÚ´ÃÆÎn~¸;\x0001ÃzüH\x0011§Z\x0000\x001dG§½+IZíg'ÏO\x000fEÎfü¹M;ÃëE(X*J½BdC­ðÁfí\x0019ª+\x0006\x0016Bù\x0016Ê\x000b BMÅ)CÕ\x000b\x000fæ\Ê+ B\x000b\x0015fC\x0019­8ÃjqR\x0010¥?4i.A@êwâ¾ùP±"(GO'ö;\x0000s2ÆîDïó¡R\x000bæCÙ@®\x0005D\x001eXávS
]É\x000cªI\x0002\x001aµÜgPy*/*	\x0005Ê¿¸¤*ïæ_æSÊÌ§JöØ2U
/½vü\x0001]¾«tg\x0014ô|«`áj¢\x000c­¡Dwá\x0015¬î\x000e \x0002qÒ@ñ¢Js\x0018\x0013T¬Ti'%4ª;zþ\x0011´ÒÊÊÖ´r0´©°Çi9Rwþôü\x0003èT,-\x0014Å*DFH¤\x0006­[A;ª,ú|IÁ&ìøóñRù\x0005P*Þåáz'ß~;z÷øp÷4ÿ¸ÿ?ÿëÿðë¯êMÁ®Sá\x000fMU/UsµT×NeÐÞ]^
S@Î¾?ÿðáPp\x0011ÆIäÐ%e´1\x001fLÅ\x001a¢r\x0015WÇ©Ìí\x0002\ÛâÚ¸Qi.D%NCUUÑr¶q¯´º®ÅuKW7køUV×\x0015]\x0007\x000c5·!é\x0014_\x0007×·¸~éêêÈ5ÁYJ¬Æa6,­nx¥Í\x0010ZÜ°x3\x0004Ö\x0014ÆªxÞ»Ióâvå\x0012+hcK\x001bÒ:EúG°¸$£6Õ.¤WÚ¹¹¥ÍKi½:æs\x0016ÈOà³òÚ<õÎ$§mÞPBÿ"Ãµ»\x0011!î@\x0013Q\x0016WsG1¯³\x0017tG,½$bP¥Å	×7R=jÏ\x0002+Ñª×1\x000cº»%ôÒk"zC*¨hwi3°®þ«\x0019]Ý\x0019]½ÔêÆ¤¹ù\x0013ÍX¢Í\x001b\x0013/®y¥;MwVW/6»t7°ß2à¤dÚ\x000cÜ§ô+­ogvõR»2*ú\x0002`©¿
'Ì×N\x0010ýJëÛ\x0019^½Øò¦P}¤¸ö\x0007=Ã~\x0008êYêxÓÒõuG\x001f2EnX_¹W åÐw\x0019owUèÅwE%ü\x0004^ÏzÄq\x0008ÉÅ×á5Ýea^\x0016@É
º\x00108 Ä°¾$ß\x0002ëÝë\x0018_Ó]\x0016fée ü*
@î¸Ã\x0005yx}ÃëØ\x0007Ó\x0014K/\x000c~\x0019»\x001eLE¹Ü¬SyóTÕÅ\x0002Þ.¦0Kd©æ¡ì_ê5U¶/Úø:Îéî7³ô~\x0003\x0003[àø~stZqÌ+íßî~3Kï·\x0014LõÓÆ1på¼ÑÌ\x0004\x001dôJö¡»/ÌÒû"%Gc\x0015×òóÕµ¡Õí&\x0019ñvö×,µ¿Yùêi\x000bÅ°6UÞW²¿¶³gv©=ËÆ7\x000cäÍ4\x0007\x0001\x0018wìõïò+pûÃRó*vì>\x0004Vüºñ¸Ýi³KO[\x0006@Þ$\Â,PàX}\x0002<ù©Ê²\x0005¸Ýa³K\x000f[N
n$Ý\x001d,`ÜWv£v¾}\x001d|>útût÷tôöæë0\x001fy&¤C\x0007ßÉ°äRÜ9bÂdÍÙõÑ§ÍÕéÕÑÛûf$·©LrH +å
"u¼Ó\x0006Hî\x001f1ÙMµ}É\x0018§\x0013W\x0002v)$T*\x000b°ÙÒcaR,ÿCK§ª\æRS¹R¹Ô¾ytys÷õé_N¾þ|{QqPCwá,sØI\Úût\x0008£æÍ£ËÓWG'\x001fßof \x0016Ñ\x0011ñ-½ôGbò2¡AÓó¦ö½ÊÌ2D×":1"\x000eH*ZsÂ+8îóóJM5fË\x0008SK¤\x0006nÎR\x000b¤\x001cöáÏ¬¹ê\x0003ü¾©\x0006w\x0019an	³ÐyzïPN9\x001e6\x0017IÜ\x0015\x0010õê¯¬û³">,Æ[*IP8&ä+b¢º$mGÍE¾cô,#ö\x00109^ÆÀFÇLµ¶Ë\x0018cÇ\x0018åTEu	ç¯
j¯áq+N\x001cD5²¿Ó`Ü}o\x0019NÑ-ø5>g[½¸gý>\x000f\x0013q_ä²-\x0015q\x0005ÅÞäð P\x001e\x0001L
6Ý³ûf¹ÌÈ°\x000b»Ä	GX².Na9z\x0017£ù\x0016ÍË>fä\x0010'YþqP	­«w£\x0016-ÈÐ\x000c
$Â\x000fJB¨\x0000Î«fÕº\x000f\x001a[´(B3à
7èæªì½ÚsBg¢¥\x0016-Ð´/å2H\x0016)'\x0010rHGÕ¹Uh¹EË24*\x001cÇñ·µæ){ÏhqJúd6YãÆ^Pd\x0006ª£,§î5çI\x000cöñªc {s+²·(²ähÌì¶S.o¹j;¥s2ÍtlFÄ6ÌvB170\x0019Üj­\x0017æöùM3Ñ:Ã¦E
ç¨\x001aÚmpF=ÝTj\x0011M­ÛneÓ"ÓæCÂzaÝ\x000cË>©\x0014V¡ÒÉ*¶Î~h\x0001ãH2iè\x000b·\x001eðÅØR^uÃëÎh\x0005ñ\x0007gåY\x0005\x0017UÑh×¨s6\x0019W»\x001bÕ;Eïî¿=<ï÷Ùp²a\x0019zµA\x0015·rHá/¦Ê;¦Ñ>]_\x001fð×Ì¸¶Ý¨Nµíe4­3ÉÁk\x001cH\x000fAÕúÉ<yWÍ&³--âÊ\\x001dHÂD'\x0016êõë\x0016ÍµhN´h*QË\x0010Ö:pÍ¢ÁAÐ¼jÎÇl4ß¢yÑªÅ¨ú\x0016DëaÕ\x000cGøI5¶ùh±E24OZM\x001aû\x0011ÈæêÈ\x0005Äjú¦M[²,#ÓÜÌ­³¥Ô8±&NAÌ%Ûú\x001eåP²S`j)¸\x0002Jú¬% u\x000c\x000ef£õFMfÕtÑóD¡\x0017Çº6\x000f\x000f\x0001kÐ:£¦EVM\x0019Ci/ñ2	\x001cÀ\x0007eÛ\x0011ìä55­³\x001dZd<à?\x0003âÊÏ \x0003Ëk¨IÅ·ùhíÐ2ãÂ\x001a¤,äØÔÔm®srëÈBG\x0016Dd*\x001d&\x000eú88êO\x000eÎp<V±ufMËì\x001aD.Ô¢|É\x000eÂ¢QÃ+E­2¸º3kZf×Tf\x0019
];À`ÕÈâêìVY\Ó\x0019\x000f#3\x001eÊ\x001fÇ\x0013{H?\x0003¶\x001do¶=ñûl¶Îñ02Ï\x0003\x0014«¢¯'ÔkVØÒÓÉ¢ÙlÝ\x00115²#ªTeÃ\x001e\x0005bs$\x001d\x0004_uWÔ±%\x0001Í&W6\x0008\x000ehÝ¨¦\x001dÛ¿âºíÖ\x0004#<	TN\x0013\x001fæC{´Îa³Ý
o%7¼Åº\x0007V\x0012\x000cu.
>	Ã<¥\x0015l½\x000b.;	ôr¨\x000e8?ËÔLf=fsu§À
½\]tr\x0001
\x0013ÍDÆ7U´aÙm ý8ÿíÛ¶ËO\x000f½ýöíöùñèäþæß\x001fo¾Þ}=TØ\x000f\x001e[f1lEM­!;WUÅÓD\x001fÊ§óï6ë£³\x001fÎ¯O>~<ôvíÇ
Î^ýÉ,FáaËÚØý:LÊ1th^[
m[h»
kM\x0003[MÕóêBZÊìZf·ÙY®îF\x0011r\x0012H!Uh¿SP¶\x001c:¶Ðq9´6U°8óÜh[RUèÕD\x0013áRèÜBçåÐà\x0007q)\x001cøAVÚð9Ü©[L¬{Ë±Ütx[ß7P[§<âP®Z¾[=½ÚwÔ~9µ7ü
!Ô6	÷>×ð©¶É¥ÔÝÖ+ötK£¶ÜÐ=umbyEänCë\x0015;:ÛZìj3h¶ù°-t55x¿ýusÎ¶nþÿù_ÿ{óíéî÷Ç[\x00145=¤l¥,ÕE·\x001f9\x0010	Ñpøf§¼Ö£ÍåÕéç
ê\x001e\x0012µ"LÛbÚ\x0005ØBîIZ×*Î\x0003\x0005Sã¥à&\\x001e)fl1ã\x0012L\x0013Y\x0006\x0005IèÑ³c'³RÊÔR¦%>gP tïdT¯#Ì\x0018&Â\x0001)fn1ó\x0002L\x001c\x0014S\x0015r$¡\x001f£-k%ö%{Ë0u\x001c!\x0015ãq®×\x001bÅ3Bpy¥¦Ã4\x000b0M6¬Íª\x001bñSSs©z*\x001d"åt\x001d§[Âi-5Ð¨
\x0017X8B±@º×\x0013É.)§ï8ýÏséBA1YÅL\x0013«Îèä<\x001d)gè8ÃõÄ\x0016\x0019C\x0019×ÄßÝiÞ*N=¨J9;Ó©ØNE&É+Åb/&Ö³§ÀH!;Ë©N
_ÚÒs!w,\x0017¨XC=ûÌº\x0014³³zéL¾t Ár¦*Ýa<'·!½|Ö¿Üütóíéq/gÓÍ\x0015©K¼ÁÓ\x0003J²làg
m¦\x0002i:ûn\x0016Ùw\x0015°
\x0010ÓÄ0Nòd`g_áº47K\x000c<\x0010ñ³¬µGôY\x001eÝ×ë1;OÎ,pålÆ>úbpôS)\x000c*°t®Så¦RÎî\x001e2Kî!
ÿ¤=ìêu¬Ô\x0005îÒzdº{È,¸ìÐíT\x0013¥sIRR_ñú\x0015,én!³ä\x0016Ò¶
ë[\x0014Ó¥j\x0006Ã5\x0003:¾77\x000c¼Ñ,Å\x0002:TÇTÕ7×So§BNÛYN»ÈrúÈï¨Î;êÉ\x000bÖW\x001d9ï×{s¶ûîvÑwG&ºe½;\x0013)$2ö5¼N×­§[²`1ø\x0004<?Èm%m\ÿÝ]gÜ\x0002«d3=Pã\x00105råTäÍë!»î\x0016|tmfA:ä,-l`â]®¯°Ýaw\x000b\x000e»Å"`ætoöá\x0001çÔ°IqVá/_ú¼Â%ÇÝWÙHüòt\x0017±\x0016¢6Su®rÐzÐØy¾¬ç±j`æYß\x000b\x0016t}°azYÞâ×á/òÏzÅ:¡Ö\x0017©¡T|Ù§fª«DìÎiÁ¥_Bë\x0014ÜïºØ|Ù%8\x0015;Ì°\x001fÖÛRcw\x0016×.\ÜdqÈÔ°¸ÑÑ\x001cõ 
\x000frÏòM{ÓoÚEa\x0008Þ CX\x0006P"\x0011Ö?ÕJ­ß\x0007@úcOúã\x0012;`ùÚ·ZmR_c&¿Æbq\x001eÔø®ðÍÝ\x001f·_oï\x000e
1\x001fÆ;Ð\x00089\x0008Û\x0013óMªõä\x0014Ò£7§ÿ¶ù¸¹>=4Â\©ñ3°ò#}kø£?n_Ú3"!%.ãÖU×aÅ×n\x0007ëæ\x0008þèß6/,áøõTùLô\x001cÀ\x0010¸ê1æ|\x001c¨.¥à'?Jè\KçdtC\x001c¹ò\x0011þÐ:®«âåKÓ2æ\x0002>ßòyéêAà¦QÇº\x0017r9Uä\x001aàÌ´bõ|@Ý- \x0016® Î¸åÌvJµÐPaEw!D¶±#ÂoÝÉºìÀ¬·áâ`lMZK;Â,%«^\x0012\x0011\x001a]`=ÏÑ\x000c>L\x0001Oh:+cf\x0006\x001f¥¸à;e\x0007z Ì÷¡K×Pëqîø¿ÿç?\x001eï¾}{øºÏãëu\x0019\x0008¢p4A	yI\x001bùÓÔûÊæèûÍÅéååùÇé|KçtxuÆi\x0013X'Ù@\x0019ÚÅ©gYty\Jwg$\Á%wûx·ÿCì8?dtöÉJóF9³wÃ\x0015ÜryèU:+òîh\x0017\x0019\x001d\x0016IrÖE%U\x000cÆ¹\x001a7Ø½³2æCæ\x0016r<æåL®Ó*\x001fÇÀr4ÏCggW,¤"eíQvÃCù	Ýá}ÿí/7O·7Ïû7¢É¬X¬LÔ¬%,O\x0014èZåá\x0001ø ÿöû«ÍÉõË`¦\x00053\x00120Ôç.×Ê*2ÀDÖv\x0003«Õ­Ù	þ!¬ÙÙÃ\x0013\x001cÚÛ_o¿>
:1\x0017\x000f?Þ\x001d6ÔÇdê\x001cÕxåV`E\x0005\x001c¹Á=;¿£»ù°ùx5¨Ä\¿9ýØ>Dð\x001fAM\x000bj¢$\x000cuß\x000e½\x0013¥ë½Pñì58mËip\:\x0014°K8Þ²Ü+z\x0015N×rº%qa\x001b8­£Þ5\x0000M\x0015´ÓM^\x000cê[P¿\x0004\x0014Ý/\x0002uUºS9Ç}ô¹{Ä]\x000c\x001aZÐ°hEáÓ\x000eõéb\x0018Üéü*')¶qÑ\x000eM¬\x001d,jsÈÜ"«õ«¦\x00164-:òöØÓQ\x0002W2îÊ±¶g/ß¢á/ÿñãÃ§@Ö©©ù}÷ðëM©\x001fÃÚêá¯ýÓÙíÑö\x0004ÿ¼\x0008\x001eNL¥ÀÐÇ\x0008\x0002|\x0013ùQÿv ÓØg{òls4À]q
Ù»ó\x000f'ûÆ:$°=V¤U(s}Lz8Ú\x0003/1=N\x001f\x001a\x0008Ö q¢UÊºx×°JeÁ\x0006$[T	`ÊÈÒ5HpNlôq0\x0005)\x000fº¯\x0003\x0012y2x\x001f¯þp°%£\x0008'Ã
oË*%ëi/e?t¬¯AÃDHF\x001fkÚKjM9¬R´÷Ò`!V a\x001fg3\x0013f\x000e÷%Ü\x0005&ë1Ø\x0018I&6l=õö·»ùÅÜýAÎT\x0017c|;º¼ý÷çÇ¯w_¿\x001d Ã;³ÔgzYÊ²§b&-V½	ý\x0007¬þñåÑåæóë§\x001f÷\x0005\x001d`±	b@­lQ¢\x0001@¸êmBÀ¤L\x0019é®²ËI¿
 nTí\x0010F3<Ixã (Z\x001b\x0002,\x0005®ëù°OÆ.áóp n\x0003?Tã\x0016ã<Í®S)Ù^\x0010L\x0008Uéª÷Xëïy°\x000c;\x0005Â!=þ
pÈl^\x0002\x0008!¤/|Ñb>màËå\x001d\x000fø´zoW[rQCMh¬Â|\x001a\x0012âÓm!\x0004[\x0013V\x0010þ\x001eýþòØÜ£ïîïo~.ronàO\x001e\x000eóe\x001fË \x0013ïÀÎ`Î\x001eøPÞ!\x0016¾l\x0007-ßçÓ³³÷EÍóÍ	üÉù<¼r§ñ"Åà®+x®è9\x0002\x0019\x0019¥xå2¯/Q\x0004à·«ÇtúUÖ¯5ùâÙmF:YÖ®¼' ÝÈ\x0005X7\x0016ã%\x0015(Vo"!\x001f\kdË¦y\x0005>8\x0016zÉÑÀ\x001e\x0014[øÀ\x000eòÇul³Sé5ø°ÒÈ?oRe^ÊðyÃ0\x0010mX?«øúHÑ¼
\x001fÆ1f	Â\x0018fàsÃsÑÀ§K.\x0000ø¢~ïE~Fþ}Eyèb[p~s\x001a\x001c\x0018ðÔ\x0003¯\x001f$:_à»yürûÛ\x0018.<üöôÇó(\x0008Ä£\x001fn¾üíùö\x0010WÀu\x001b,r\x000cÆq0\x0011<Å\x0012(f·ãâÃÁÑ\x000f'oÿõzïÛA\x0007µ
\x0003gByL¤\x0012u\x0005\x0012\x0007*ï\x0002Å\x0013\x0011ãìµXÛ¸k>á\x0002¢0ôU
Vñ\x0011ËÕXÛ@g6vå
£¬\x0016:^\x0015)DÄÚ
QTm¬3\x0017\x000bnócCTÃ¸\¤r12U
µ\x000e\x000b6§mxB8\x000e¶®V1\x0014Á¹â¨\x000f{+.ãúãßþöÛÍnLÅÁÈ\x0010LVqÜbÎÃ ­!2Tå\x0018\x001a5v})0$\x001b1¨Ë2Ì!âiC@\x0014#9ã!ò¼­QAÇ\x001eB´T
ObÃãm\x0019\x0013ZV(qì\fÈ\x000fK4\x0019Ï\x000b¨K1ÌZ"Ë\x0018¬õ sli!Òf7¸\x000e	¢,BÂ*íDHtàD­4\x001aO4JzÌAÃTÐ\x0004\x0017s¹a\x001296¸²[ÉD.á|&£¨ó\x001e,fe\x0007¦T\x0014Z)­ür­e¹NÙ\x0012fdRt\x001c¢ªLáàÁ\x0004ÿymeL¶\x000c#D&O\x0001QH¡ÔgàvR»\x0017ÜeÉ·Ë¥î\x000b
SBA¹òíòÖ0­4\x0004\x0018Ô"KÁöPè1gv\\x000c\x0001	f\x0000É+¿\x001c;í\x0002"c¬#\x0010_\x0017\x0008Iy6Ú¯<uì¨\x000b´-6À¤\x0019\x001eÃËÓû9O¦?\x0005L°ÎF´Ã¥Ò\x0005\'ØìeåW»\x001bü[\x0005ÉîØ\3¤³G1 ²»\x0003§­ÓÚ%\x0002§ËxégËº"ÙÀ-V¤É'\x0010\x0001\x0013\x0018[#ò\x0006r|àPý;±LìÄápÁL`\x0000Ì\x001dH=d\x001e¹r÷ZÃÙý	?\Æ\x0004ßÞÈü84@©D\x0006<:ÞN~íÃ¶"+s\x0008ÊMR^ù\õu}\x000cü2\x0013V^*¸ÎVæ\x0010¸\x001aBÁ\x001ebÓ­ãogÒZ&0Væ\x0010\x0003W¶8N¦Ôd-)_Ï|jí§\x0003ËdeaJV¥5\x0000ß\x001dVC\x0016Àðkh0+ï^~ÞùM^há\x0004&2O!ñ:¥éGc\x0001\x0013|z+\x000b2Éà\x0000X&\ø=4Ù¸Ò¿äG\x0016	\x0013Iÿ\x0003Spõf¥Ò\x0011Ê8Ö5Lðí­ÌdfË·]Ä7)2\x0005Â\x0015Ö\x0002zë0E~ËÆN×Hf<\x001a^'oV~;ì\x001ct2=Ç\x0006\x0010×x\x0005«£KÎ"¯ÝOüä$¹I\x0012Ö	«îh¸V#µn8ØÞ?9a\x0008\x00159ÔÄ¢#ÌS~¥#*rNæ`âh^Je&·½£æOWnq\x0007æÒÉ<:EâQÀ\x0004¦)sf.­µ\x00048\x0018×\x001d:J7ád\x0017*ýI©¦V^\x001biê¿Ü\x000cy\x001bÑ
¼R\x0018\x0000[6&Ô\x0000xQBåÎÛø»i*6ÊPD¬d~ûðüøíîöñ²$#ñJ6,s%It¦&\x000cíÄ¥7\x00143¿=¿¾¸<Ý\ì	^\x001a²¦|K@\x0016¨\x0005ÈÒùX\x0015ó\x0019U)÷×F+=q\x0006Gd3­É°
àÀ/O\x0004g\x0002ÅéØ,ÈlqÂfÉÙà0z9[i
.\x000bè\x00010àd¯ºp\x0013[M\x000e×$gÃAÀa2.\!Ó\x001c$Ã²½¼Ùf5)aÁ²i*^<÷àtÝoSnòL¸¿YóåñoÍËÚY¡º;¸XÑR§\x000f\x0001â/òM(=\x001bZeíú#@,{\x001b\x000c:r*ç\x0018["\x0008ì£bãe¼ª\x001cf9F93×Ã¢\x001d(\x001cùö	¶.GXÎQÎÚ<\x000e]4b\x0011#bûía}å\x0018Åç"²ygqà"dÞ\x001fú¸x\x0004Æv\x0005àP#gnË1i±\x001bò1s1,\x0003\x0001ÿÐ'ZÄ«aâ¯RÞ-æ­FÊ(´8¬F\x001ak
 *ð.\x001d2\x000bAø¹bæ(ò²aI2\x0006&eI\x001c/µËÏ-?RÌÜ!®~\x001ct³iMt)[Õûå$ô41oMT¦¤\x0016\x0016=³_f,EC*»¸\x001e$f®I(p¸&\x0019g(5¡R\x0005Ø°#GD\x0002{\x001dÿ5$RB\x0014Ëå·$¿ÕRCrÿã~Mß­ã?»ùýáîñð»¨?NÛ\x0004\x001f9¨}ù\x001cÔ¤/vòùüôb\x000eOWÄ?Ç:òÿbPÕSÝ5\x0018y\x0002r±$<ÝÓú\x001c\x001ejÆìu
±Ô³×Óâù@·7\x000b\x0008'Eó+ªé©¦ÓóôÃ| î©Î
i^!°+X\x0006^\x0012Ç\x0012*N>\x0015Í\x0007êÞúç¬âÎ\x0014ì¬wK÷ùÕÑ¨É0~>P÷Ò?\x0007ÈW  0\x0004Ä\x000fØvú)m>N÷Ê?\x0003\x0007x\x0016",3ÐÄoün:§?gôÆ?g}\x000c94@ä±Å±|°È;ÈÉöùDý\x000bÿ%2Üi¥\x0019h(\x000fÆín\x0019\x001a½ïÏ[#ÇÏÖêÿ0ºã\x0007Ù0\x0015ÞIúôyD\½¢°/¶õ\x0006ë¶5ß©\x0002 ]Kr}ÔÃî4þh~e|Òáoö·&×rúëo7ß¾ÍÎL\x0005W
JÕ+ÎËÝ\x0016\x001bôgíôÃ§ËËY9 «ÜùB®\x0014j]M\x001cJÚ\x0006´ë÷Ó¯V®!\x001alpÅå5x§\x0015´hk\x0015Ò¨|s\x0019Zñ\x0004¤«f*\x001aì1\x0013iÕl¬Á¼\x0002Z¹ñä\x001fTQr
'\x0004þ 2Ë?èûéoêf2ßxöð|ØÛ\x00053\x00118©î¨±	Îj­ãS×ß`9;¿Ô¸¼óÀc±,v(A; Ùä8Y<ÕG'B\x001aç>_DØ±¤¡bÜVj­ùÅÏ	7S4Îx¾d(2fxª)DÜ%jÝÚÏ6Ns¾\x00044\x000c¹!WÜD®êVÉrÑÕkÆÉÍ\x0017×H%~XAq¶ZkÊÅè4¶Tr¤qVóÅUR®&4\x001d×KúLmÙ`\x0005&^úD@ó;\x000bÈÁ>ò\x0005\x0008\x0005@¯æk\x001d±foöw&QçoÎBB+\x000bôö\x0008a9'¤ýÞ'D÷>åßm-ÒÃóÁäsyÜ\x001f2¬Þ*n\x0008HÉNåàÆ ç×\x0007ÒÍ
\x0000Ù\x0000àìà«9\x0002àÄÎâÄ¥LN\x001cêÄ\x001b»\x000c\x000e÷\x0000!ñó\x0008à±è\x0001\x0000²¢é\x0019\x0003@^\x0006@Ûô%\x0000lÔ+
ú\x001eçHFjÊt\x001bÃøn&@Ý/.ç{\x001bö] sQMÅÖä \x0005\x0004úÇûð·ûÝ«\x001aþ?=ßýqóõé`¾.ç2.Ø\x0007¯\x0013W\x0011[Wzhq¥<­ðgï®OÿíäãÕ\x001c°îÂ\x000b\x0016¨\x0018À\x0014\x0002æ(ë\x001dÝô¥\x000c¬»¶ç%Ø@VÌÔ¦\x001eÌ\x0006óMÕ4IÁº»r&¶äª\x0006ìÝ¦\x00020\x001b¨­\x0007À¦*,¤`Ý9\x0017,¶{"\x000f\x001bu\x0005R{u÷æL0C½lÃQ%Y\x0003®iGÆÕ]3¹ìv\x0011TÊ\x0015ÊN>ë F7èL*\x0014 Ï\x0004æ¸¸\x001f5ò,¬ß_]æf6\x0019öa\x0013Xæ÷SçÖ\x0003i?Q\x0006Ö&pfañ©dÜ;Æ\x00025@6Õ$%k\x00139sÉ²\x000eT\x0019¼õXf?åT×lJ\x0014FHÖÕúÎ$Ã\x0017ãb÷Qâ®\x0016öPe­ònªtM
Ö\x0016üÎ\x0006ÃÓ,¡ìÕ@ÙC±þcve¿³É¬£Ô\x000ein'QÙò½\x001dëgG/×&yÎÌg\x001bhy_aµå¶sÉpr\x001f½"ãÈ¤òb\x001aUâË\x0012üóÉø[FÖ\x0016¸Î%s`[éd¤PW\x000fÉÀ[÷Lö
×xWR:¬d6\x0003ÎëÃ&FyþÓ¯ª-*M\x0005qLÙûV£6^Y.íª\x0008rµ¥³¹"î(²XØhtÖ|*í+¬X[_:LÑuiQÆÉ\x0013\x0018õxÀ\x0017õ¯\x0000Ù'©¹@½_S¶>üéÝ,\x001akø[\x0016ñäd°\x001fÔ\x\x0015Ùö[«ëqINiÈ¸àoáò\x0002®L+V.\x0001ârü-Íz\x0003£¼ôX¢´P"2cù[Z«ø[õ5­Ù0\x0015\x0002×m\x0005!\x0002äi0\x0008\x0018)Vqé£\x001bÀ\x0015@ø\x001eb@\x000b\x0010¡µ®(R\x0008ÓÊ½ìoLÖýö×ßþ¸ÿÏ©÷­!vùð\x000cÿ©C`
¾§¥\x000e\x001aØE\x000bUm#õÞF}v\x00182jç×\x0017o÷g3\x001a¸Ñ#×\8l¥+l6r%\x001483[Üó$¤\x001b½sÍ¥óJ=\x0010Öq=±ñÜzä^môÐ5-q#\x0008\x0008-Õo^­ä\x000fl>Çâ\x0004Ícµ,ây~¼\x0004¼ð:nô\x0010'Àsº¾æè4ÆÛóFØÂ½tVK\x001eALæ47ãFã96Æ\x001c=?ë¤åë¯£îßwSX\x0012÷x{¸N0kÊ	E8,<a\x001dw¼E\x001d'\x0010¬»ØÌBêsÐû \³T6pãRn\x0015\x0011u/rs¢æÚ8©aZ$Í­¡LÄÞ4¹¥îT¨v>Ú·£÷\x000f?Ý>\x001dÔ~ÂN\Gßl\x001b\x0000û*þd&¯ôË£÷çï6Wûup\x001a¢vf\x0011á$B½TgE-e\x0010ÎM}1	OíÃ\x0003ÿD\x0016\x000b\x0002_µÖÆ\x0019E\x001de!»©§¦\x0017\x001eïþúÍæ£m\x0019\=>ü\x0006\x000c_z~¡*¥HÉc\Â^ *LÑ,\0\x0012
Ø\x000e4¸º8ÿ\x0004¿~|·O¿Ã\x001béµÎÄ³ºÁ0d´XÅ×IU~b§\x0010¯äÕ¥xÎ)Ö\x0010Áôp%ÈäË1\x001c1\x0011Ü¯_þãî©-ëiT<¿{øúÓ7¬\x0005¹9,ä\x000fä|\x0001\x0005¯)\x000eÀ×HÇ§Ññüîüã»K,\x000899$åÙPî(òÎ§ôEF¢òÜælq¢
]û\x0005QçaþdÔÓÃ_§ûän^(Óöq[¸\x0012\x0014×Ó¨`Ø¼M*FÎ CÅÚ
¶?´÷ÝÃßo\x000e«A`Â5ä(¯ÅuõÁ­ÓaªU\x0015ÖíÝùO®\x000eU8ÛÂY\x0019ò$Ô\x0012°ë1sJ¦Cí¶up®sB8ÇÝU9ë-\2\x000cV®oá¼\x0008.@`§u£zA£Ø
\x0002¸©ø]\x0000\x0017Z¸ +¢Êx `{ð\x0013,RºÌtJS>\x0000.¶pQ\x0008\x0017è´ÂÊ%\x0012W\x000eº6%ëI¡}	\já\x000cÎÕ}ª¨jPÃï\x0004ÝºÏªUgJ\x000e\x001c\x0000RQPøØBtÁ)C' ë«W¿mÊÇéÇÔ×m]Î¨»NwGBËÎO7®æ>\x0014¿ec½Õ:¸îHhÙð°×Ji\x0002D¡
¢a=91cÜäÛ±®;\x0013Zv(|ðõPXÍ¡ÊqjÆh7Ý\x0015Ðå.è\)Á\x0019öÙp\x0013	\x0015bóÑLw^ì¼âÓ1°ZÇ±×a¯\x0014:»®sLÌ3qð-yÓÁmVú|<ñÄL¿$\x000bèLGgG"rý6\x001cR
ÈàH°ÈÖÐÝ¼®óÌqrà«»í¾sºÐa£#ï»ué,±Yb\x00173×Q(fá\x000bõËNÈ\x0017è:sbdæÄÙÌ-\x001cºSÞ}J¡Ù)\x0015E	]gNÌX0v|EOÏ\x001fØÁW÷ÝäëÂ|:Û
+;\x0015\x0016ehé2Ø¤=[â8ùÎ6\x0003Î#\x001d³t.!<|ú÷·\x000f?¿à±\x001bË/§>r\x0005áçÉ5*c¸K
¯ÞoÎ/ÞÏÁ3-âéÈ¥\x0003\x00182Fjûv\x0014Åª¤&âD! m\x0001­xý4?
ÇÉiCã¸ß\x0018»$×\x0002º\x0016ÐWÐñÛ 8£Üïc¸\x001f\x0003\x0000'¼(! o\x0001½x\x0005=yÈø¿Ü2i¼á\x0015L\x0013
#=àdîµÒ.Ohsðà\x000f8Ë=öL\x0017'üwáòÅ\x00160¯VJy|æâ\x0013ì¹Rp¢&CÈZ¾$åSªàa\x0001Ó¶!?³\x0013ª©BÀÜ\x0002æ\x0005'8Pñ3ö.±	\x000c\x0018&jGdº7Ñb\x001b
#ÛhËWH{ã_%$ì°\x0016aT)1u
\x001d\x0013\x0006W×pí.ÔÝ)Ñâc¢2ëÜ`;IæZ"\x0011ÝD@4\x0010n¡þ"\x001f|èçoßn\x000f×ßGî\x000b\x0010\x0008qs­å\x00065ôÂéæèÍõååfiD\x00053-yÞ[.\x000f:»(ÀwÇäÃá\.ÛrY	\x0017x|ªÉ#O[
VqÝ^RÓusÁ\\x000bæD_2²\x0010·µÕêjK¦KærùË\x0016,Ók\x0000|ÈJ±ªúyÓåäs¹BË\x0015$\IQ\x00012¹ÓSk¸ì&î©(Ë\x0015[®(úü>;\x0017[m¹ñ$­\x0003K-X\x0012-X"õÚ¡\x001eî\x0002K]mhÇÖ\x001dÉÜeáLtÏ£\x001f\x0019EÁ­\x0001Ó½q\x0015YWÔþ¦%3±¶mcÀ\x001a®Î¶jqM*Rz3¸í\x001b\x0018J\x0018\x0015®0%\x00152\x001f¬³aZbÄR} \x000e\x0018ø\x0007CÍM\x0014O«Ôdû\²Îi\x0019Kª6àè)^1ö2Üd~i6WgÅ´Ä%Íó;aÅ\x000c·ë`\x001b\x0003­ØX¹@HÖÙ1-1d8_·\x000b8úºq\x0000\x0014­V\x0008KÖ\x00192-±d¨/Oq3Õ#³û\x0015BäOÖY2-1e¸ÿ©\x001dÒUã\x0007þÀÚQO.Í&Ûæ§\x0007wLÖ,q¬bqÊ¤æî>:\x0001ða×\x0018YÓ\x0019Y#1²I\x000f25ÃEÅ\x0013ÅpÂ\x0010­Ù\x001e\x001dÒ¹d½\x000b+2³°¹´£53õk²àÂ5d\x0013k$^,Z
ªv;
l5êUû¬»\x0001è\x0006ÀÇÀ\x0012À'dé\x0005Ë\x000f¾*¨)aìùdÝ
`D76¬¾Í(ï&öüCîØKÖÝ\x0001Ft\x0007A>uX3§ñ\x0002\x001dÈ\x0012wFâ\x0013×\x001a²î\x000e0¢;@ÛcºÎ]-G³\x0010\x0008ðu¾*º4Ý\x0015`DW\x0000OQÅbm\x0004sÕÉvyÍèn\x0000#º\x00010ãÂKfù\x0002Õ\x00012kVÌvfÖÊÌl¦I´¥wÛ»ÙdIa°ùd}D.2fC×¹2\ül#\x000b+Ãµ0)ü1¬3\x0019Vd2PMO²­ÎYâ^Ò±L\x0010¬;Vt.±6ÚvPåÍ³Åài¦&\x0002Î'ëö¿\x0015ík9ëm}Æës Ëý=bì3É\w\x0000è\x00008E7\x0010Ám54rí¿Å©\x0004+Èº\x0003àD\x0007ÀYö´±9J.2Üê79Kq>Yw\x0000è\x0000¸Únf£á\x0014gg½_å5ºî\x00048Ñ	\x0008U©\x0017Î$:\x0001.åYDd¾û^ò5sÄ#\x000eÎ½âf?ë&ëÝgukæ%k} J 6¹ÈdjÕnÍ`Í\x0002¹t!ÑÔ«9Ç>È¹¯ ëN@\x0010 R¢ËÉg\x001b8\x0005\x0014y@-\x0017Ó
\x000csÉº¯\x0019\x0004_3hì\x0015(d):ÑË\x0003°*MN#udIB\x0006Î>í³A\x001cn0´1Ða³v8\x001b,wW@\x0016\\x0001\x0001/§¢ëå=ËÂEÔD.`)®ºÏs·Ë²dá\x0007,U2Þ£Q¤\x000fQ»\x0014ÇYýÏÝ·ÌoÖ¬ty8øB1Qã>ü'PgõIc£\x0011rÐ4µ½HÙ\x0015ED\x0003¿\x0001Ì­¹4µêR-ø§³Ñ"êe\x000ecð.fé°Ud}ÞX	2\x001aQ»H¢à^«D³¤\x0012L¸	V\çºÌÁ?O\x0013[c9`Sip\x0005Ä,Ðl\x0016\x0015ýù§ÛÇ.ªû\x0013þ xÖ©9G\x000f\x0001'¿Îùú<·Ê¦Y?4 ÷qJÓ>'"à¦\x001d\x0008\x0003\x0002+\x0005ÙTÃ;;%Ö-\x0008ïv\x0000­\x001cÊ\x001c¸c)~å	nó\x0001\x001fx\x0004hd|1*êÍÿÕ,m5?]Ä´êyÌ\x001d¾ \@l'	\x0015KM\x001cc_|º	e~Ì·ó³\x00140T\x000bÇ\x0018\x0004XÛ4]ãÄ\x001d@#\x0005eóÛ·\x0016\x000eëKËÂÛ?Ø¿ô5\x001càún{?ßÜÞ<ÿtûå\x0017\&ï±b\x001cÍ\x001fÎ8¤k\x0016[Ï\x0014ÕdãçÍÉõ»
üÉ\x000c@Ó\x0002\x001a) \·ÅÙ\x000c'ÓEÂ"ñy?Ù\x0013(á³-òYn[ð8å§(Âª\x0002xF}oº\x0014á\\x000bçÄÇIA\x0008å\x0015U²aG=m½¡\x000ebåêù\x0016Ð/X=\x0012ÁVÀíêà×\x0002\x00160ÏGbAÚG÷\x001f§HM«W0µI¼&*¡ö\x0005õ/F_õFÇµ\x0002r>Ó- ®`Âú¿òÈ`ð\x0014ÀI9\¹q5ù\x0012\x000bÓYèÁÊà\x000fÂ³â¨×Ò\x00074I[®9°4v§\x0016p\x001a7*·\x001f¸ÜîÓÍóýÑ»ÛßoÿëÐ\x001dsÍ¸Þ.ð\x001dg\x0014\x0017\x0012¤±?^"N®Ïà&ù|rý?_f3-\x0011±á°eòQC\x0015æÂô\x0018×¶M<ØlËfeëá\x001a×)NFN¡¤±\x0014Ëµ\NÆ\x0015yÁjmÎÔ®­Òx4Ì·d^FæynÊð5y\x001cç	zi<L\x000c\x0017Z¸ ü¤Ú\x0003Ê°È\~¦ä\x000fEp±28çùu$`¥\x0014Á9öÓD¥-µlIøUI¾&àlhé(p¦\x0012"¶Ü²e\x0019\x001b¾ÝhÓ¨j6ÀÕ
A[gÜ¶ýÐáUÂ-\x0017xì©ÉüH®#?E$?ÖÄÂõ·ðZ(ýãeéê¼Z­j·(È\x0010Ñu÷]\x000c8YqêÀs¥µÕn%ÑÝÅ e7ÇUK\x001fVãã¡\x001dæðp+Oîn\x0007-¼\x001e¶Mnèç|][PÒN­»\x001f´ìÀ&w¾ P»PX\x001b:¹Jv\x0011\w?há\x0005¡Q0\x0005Îp}¶Ö¦®ßÍçèº\x000bBËn\x0008lrçãj\x0002ÀYÝ¼éüÄ\x0000x\x0011]wEhá\x001dP·\x001fÖG6&õHL\x000c·\x0014ÑuÝ\x0012ÞEÔ\x0004\x001aè \x0014³´ïªÀ|ò+\x000f¬én	#»%°\x000b&©C%=¢CQ Z»~c\x0011]wM\x0018Ù5"îä5ÙÀ	F×¼tiÝ¡0}ô »%à\x001f¾=²
Ø\x0017P\x000fÅn®»&ðÀä\x001d9'6UÌÏ)Lpèº{ÂÈî	4(T)íÖ Ôµh\x0012\x0013Ñu7\x0011Þ\x0014(¹]à®
\x0001{ÒT\x0008®»)ì¦}W·\x001d8 Ôø¤ìöPL<\x000cèºÂÈn
§<e\x000ctÑÒxy¸y¹j(åAµén
#»)¼³Ü"\x0006jZánd:?Q¡,¢ën
#»),\x0018\x0014êµ\x000bØIS\x0005\x000chßeµ2µÝMa7U$¤\x000b§ÂðÏ¡S±òÈÚî¦°²\x0002¼\x0000\x001c*0Ð¡pVÙwÃTÆ²vzbjª®»*¬ìª@Õ|\x0015Ï\x0015\x0014QLuÚãD®O5É®
kjç}Dß³hÝDv=³¨'\x0015Áu7Ý\x00146»cK÷Xò\x0001ðÉ8Ëb¢áGD×Ý\x0014VvS¤ù\x001eu~¯b­*WP\x0011]wUXÙU1<+ÒÕ)\x0007QYþ²ëØºÂÊ.
ã
Ow!hÌÃuK·X\x00133TDpÝ=ae÷\x0004ÒyÅç\x0013M:7Çõä±0·®»'¬ì0:°0eLTÌ|^sX·ç\wM8Ù5a Ê¦Ü	\x0018_ìî\x001a>lª\x001fv¢.E\x0004×Ý\x0012NvKèTëÀâFP,U$ý"¥V¦Ö]wK8Ù-a|-©Àîö@Kg¹°?§!Q"ºîp²[B\x0007Åý@ØæR\x001eÄ Ì \x001e\x0012\x0008·'fåèúg	Ù5atÂ&½aí²å\x001b\x0016%ìùË®|hrÝ5ád×VâX|V,\x0005ëÞo¢á¿ù:[çºKÂÉ.	³É-D5ëXñI:|JOÔ¬èºkÂÉ®	\x0014£ë\x001f{È7qÌÉ09m\x001d]wO8Ù=1\x000c{¥\x000fkªÂ"\x001c\x0015¶'fBÕKD×Ý\x0013NvO`8µ0%\x0008\x001a\x0013­\x001dFî.èut¾»(¼ì¢Ðº¾:%§©ºÞ»àùPL\x0014àºÂË.
\x0005Æ®Ø\x0014¸\x0015|QËtSÂÔ"ºî¢ð²BE¬\x0012/ß5Ó\x000bw,©ÂÊ\x001dß]\x0013^vMà´nR§HEÚcX9n\x0002\x001eFÜ®£ë®	/»&à®G"q³	Ð±!\x0016$¬£ë_°e×Ä [LW,=tYë.OÜèºÂË.
Oa$9®\x0014%\x0000.²9É\x0013
\x0014"ºî¢ð¢Âe,/a:®M\x0000G^±8õÊtgèÌI\x0010\x0013±ûª\x001cC\x0017Ê5üö¤õ®;²Atd]6[¹ö\x0018*]½cuX\x0008Ý¡\x0008¢Cá²ÊÈàÙó¤i°8J¢¯<\x0014¡ÛvA¸í¢±F\x0013\x001d|*ªcÓÀ¹rí:\x000f <\x00000£Xà¬¢t§×QWmêµ\x001dÕV°QRkçæ\x0015æ*ãàI\x0017ÕçP\x001f>':seïcD¸'¥ÞÔ·\x0014ixiP<F\x000ck)V¦>ÍÎ:\x001a)¤Û&{Òì\x001dÀ¹í4¡<&Kãí@:)¤
u¦oÄ\x0006Ùbjb¢qT*É«Rv>·B\x0006<Óü¬¸]ÕìäÜº\²ÚùÜâ¯\x001dP\x001ckì1×U¦Z²5¡µÕ"î\x0011rµzTé±WmKúpûøåùñáþðYQäa¡\x0004\x001f×ÎÀ_Êófö¨\x0013|Ø\¼½¾8?;°x\x0004[¸,\x001bLôà$$TÁcÿ&º\x0018\x001f¦§wÎfkj¢­ÑN\x0007\x0017i¤Kr\x0010f3 £ºOãÍôðùt±£2:\x0008uËÐwÜ[ôÚ
\x0011\x0011í8ãÌäÀ\x0019\x0001]÷]µðÃÂ9%8?J=¾·
SrM%p¦û°FøañQ¥|X«5	vxË³¯
\x001f­Róéº\x000fk\x001f\x0016|\x0007KIÇ\x0004Ç®);Z÷]M÷]ð»:MsÒÖ£3\x0011iº1SÁ\x0012ºæõ\x0007è\x001aµYt\x0010{_è¬£ÆUïx²!ÏÖ­­\x001c6Õ5Q1PG\x000bXØôéÎ³é\w$ìHhì\x001e,ßUU9R\x000f>\x000c\x001d	Lì­£³\x001d\x0015Ò\x0005*±Hª
æ¡\x0017H¶\x000eÅüÖÑu»ÎÉvÆTèf¯\x001eÓ-\x000eë\x0004ÖÑuæÄÉÌ	6Ë\x0013\x001b3\x001c"Ó\x000f.\x0015¡Þr\x0015\w(ìP\x0018Ï*(1»L³\x0000KJtvz>ëlº&#
t^"c\x00173gâmLlìöÆO×\x001dY/;²\x0016\x001bà¥Ki8.O¢<å0OM\x0013À\x000eÎ\x0008.SmoÒ¡	xÒ¦±nµóÝõ²\x0013kqÌaÃSÈ\\x0017=×Êq¢|VD×X/;±8Ô\x0006§%gø¦\x001f1òD´#K\x001d\}XðBhØ¹ê\x0014ë<­ª:.t'6ÈN¬Vº\x0018VªÒyªv3\x0013ï+"¶îH\x0004Ù\x0000kÆÖ\x0004ç\x001cÑp`-L\x000b\x0008Ì¦ÝÊEáÊá²r
p"?\x0011Û´ í|´ná¢pá¼£,|R6ì
>tóÂÉys\x0002:×Ñ9¡o©q;áøJ*NÅ4\x0000ßþ+7]ìÿ(þá\x001a8¦Ë?
ý³\x0003\ª·V\x000f×Ù(³%Æ\x0018rëà\x0010(Ãæ]\x0007çm-©Ëë\x0014ÂFrá¿9\x0012Æ\x001d³¡QñíèÓíÓÝ\x0013üÇþãð\x000fPçQ\x0015\x000bMfÍÎÉAL8gëÓæêô
þÏÅÁ!$aÜ	\x001aT;~v6¥×u\x001a\x00138\x0007Í¤PõIÖ31,`tÛ`ø@O#"+§5=NMD\x0019[Ê¸2°¨áÐË\x001b§bt¹¥ÌK(ýv\x001eeí]\x0013ëx°0)½(£l\x001a2ê\x0006ÔÎÆ´µ<\x000eü\x0004n\x00046a;åÊ¯ßM\x001a2´#\x001c$«\x0019·\x001cj§w\x001d\x0016\x0012Ôú\x0013®»\x0013®\x001cq\x001c\x0013Æ\x0016Sö\x0005²i²²;ãzÑ!7ø\x0003
ÅÈ46,Ú:±IMOt\x0014av\/9å~¨ü\x001e0·\x001d¹½ô¹q!fwÊõcN­/8%Ñh©ÚÓ\x0014ÝdÆMÆhº3nqL-ðä\x0018O¦`ÕYûÌî\x0019DÝRîy	ã¶µ ºÙ±óÑó£«ÀgÙeÅfÈú)\x001fW¸®ÃtK0«\x0019r9pû¿ÉU·ß¾Æ\x0007ï¸YrÄ\x0001³\x000cKÁ\x001bÅ\x000e\x0011O½1RrBÈî%\x0007<U;äb@ßÈ\x000eÃyª³¡÷¿-SÇmKÒ\Çac|¾\x0015o=9lL¶¶;ßvÉùÏMµÆ.Ö\x00194&×ÉPÓÉk!fwxìÃ\x0003~:Îâ\x0000L\x001epf\x0005'Õ+Ý7·K¾9Ê?ñp¦Hé§`5·ÑF5Ñù>\x001b\x0013þ¹½\x0011üÐL\x000cü|÷å¿\x001f¤SXö`(cib\x000c+ÇOÅpìóéÛïÿü2i±Ì|¬¶³>£«ú\x0019\x001bTðUe\x0005m±¬\x0000+¦ªú\x0019L¹ÉmLÖk°\å\x0004X¾Æ\x000cá5ayîÒê¾Oå[*/ù¾:%Ð`±rþÖ¬Uh©Ê¹:\x000f\x0003\x0014ÚYË  Ì?ÌÄ-V\x0014`\x0005]\x000e«\x000euºV\x001e.7\x000fk\x001b×
æA	¸À¥g·Ù:\x001eÆ¡«X\x000cÓO3¹z³%°[XJg8Î\x001cJÊ¯\x0003Eãdf.Wg·´ÄpiÖz\x001e\x0002K\x0012MÀ
X^/½b{éÎpiåÒº¦b üa\x0013¡êPE¿Æ êÎriéBa)^/ÏÉ\x0017µ\x0001ÄµÆJèÎviñ²ÛYâ(àÀÚW[ç2ÿù\õÒ\x0002ó\x0005^\x000f+ÕxeyÖòÉ×àk­×ùÒ\x0002ûê#ªQ²>Ì5ýh?+u\IÀ\x0015,·k`eXÃ¸\x001aaMVNÍã2]5\x0002»:d\x001ai½Pg*në\x0010i3ý;\x0013«3«F`V\x001dN(¡P/\x000e7\x001d\x001aùÍÖõ_³\½;(0«\x000e+(¸Këj³­YcVMg¾À|\x0001\x0003Ð9\x0008Xù²ªÎP´ÕY	#°\x0012ÎÖ\x0011º.inRJ±\x0006fúA~\x001eív½\x0015ìz]¦®'±\x0003U³Ã«>£íÝzÁíhp°×vÛgª©§QOOiÕ}F+øÚåífvr¼ß&±òdIÊ<,×}E7ÿ+Â
)vìñ\x0015ª(~¹ÌWv\x000eÓ#ÀgbõAÐü³3¸Ñ\x0017tJ±\x0002Î}ªZ\x0015Ó¯î3¹º+ÈÍ¿PY©¶n\x0007<T\x0017©&[å4]	8Êw\x001fÑ\x000b>"\x000eo§\x0001\x00111RYì PÍ"\x000b+\x000cïî\x001f?ÿþq\x0019v|¤p#Ä²VàÆ\³\x0011+¼Aß]?~þõõ\x0007\x0018ú¡ÜÑ¬87$º¹üÀu=Td¨ÎhùùFkhkãH\x0016¾`¦ÅÒUjOéÌÅê¬oµ\x000b*s\x0003r,\x0012Yõq
\ûé¹
3±ºcè\x0005ÇÐ¹\x001ai\x000cÚç\x0003g½s\x0014<_±µBw\x000eà\x001c:\x0008\x00027±\x000f\x0013=\x0006._ûýôD¥\ÝI\x000cè±}¬V"ý\x001a\x0017P¡õ&VPu\x00071\x0008\x000e"Îª\x000eÜ}­)¼MÏ\x001f1NHÃÌÇêb\x0010\x001cETø¡\x0016¿\\x0005õ *®â\ÓÃvfbu7b\x0010Ü\x0016|?êFKÉS\x0006Îam\x001awO·ÌäêSp\x0002\x000ba£e+5ÏÖ\x0005s´¹\x0006YØÅ\±ÏÁÍ\x000fb1^­²H.ÒÃK*ò¥\x0018&fGemõ\x0014EfMõÔË1#x©T[/\¤Æs}IÐÓ­,³ñX×ÌÄúo\x001dµ\x001bãi'ÂC]éL\x00054F{\x0008_\x0007^ï³ÂÉï[\x001eËkäÛÂ\x0001å©÷\x001eN-÷;na¦Û
fÃ?­hé°ß|E*IÉ<÷;æEnÎ¾$\x001fÚ½÷7÷·O\x0007ßÖRlH\x001c\x0018^ÒlJ\x0007éD3!\x0001okïOÎ6W\x0007Õ\x0018ÍµhNsMÝm#]·­Ý~K\x0016Z² "sU\x000eÑ£H(\x0015ë[>\x0007qòjOZ²$"SqÜÌìÑÝ`\x000b2%K7\x0007ÍØ¿Â\x000fjÊÆ.þùox\x0012Þ=?~»94\x0006\x00157Ðý\x001f®Tm8lR,t¡®}¹Áxw}qyrh"
\x0016Ô,\x0003­"zIsîÀáÄG&¬£\x0016ÚÔ."õç½ãLn­,+MÏG\x0016º\x0016Ô-\x0003Í¬#°\x0013}|çX¾ÆOè&/ õ-©_D\x001a\\x0001Âù]¢{nÈQaòUEL\x001aZÒ°\x0014\AVÉ\x0002\x0017ÕÐ\x0006ËúgûJe¤makì
[%\x001aù6ëpÌkê-;­¯ññuo¢Ù(\x001f¹ 9\x001bî³}jtºÑ^Ú\x0019)½ÌJÁ"9íìLýüy¦3bÒîìëe\x001fûîËÊd\\4Uz¦TÉ\x0017v'J/;R%{B8_ \QµÂë¬iìHãÒËª4sàÇ_@Í¬i\x0015&)Ä¨©CMPuâ\x0001W9³Ä¥\x000b\\x0013§u|¹¢ÎNev
\'j\x0002\x0006\x0017<]U¨\x001dZ¨^\x0003µ³Tf¥\x0002ÔÄêRn\x001bTð _ÃRÎI1Ë¼\x0014,#.¤ÆQÃÃt\x000fKM½Æjºão\x0016\x001d,Ù4I`?9E\x0016,µ÷i39m\LÚ)³èLa9dÑ!\x0002·ÔR9ìPI^H­\x001c±,EµÝ²Î\x0014PQÌ\x0014\x0007ñ\x0004Ú¨³ÇÖ¿Æ²Ýç·Ë>?\x000b.\x001bÕøD²CeT!uÆ½Æ÷wÝ¢ºP\x00165\x000c3\·gÊR7¥vSã´\x0016 v~[ä§Ç«íä±\x000c¬¬¤!ÆÊõAÊ2GE³ï\x001f-\x0002M7\x0015Kz³§È\ÚíU·l¯VñcpNiI©Dc­ük`vvÊ-³SF/û\x00146\x0002e¤¡ô Mÿ
¨¹CÍËN?5\x0018D\x0013õ1}Ò\x001a\x0004#\x001b^#FñÝÙ÷\x000b\x0014f\x001a]f-x¸\x0010èÉDÃÑz5
Ýkj(å\x00131ûÉ\x0007cé05@N\x001a;w*.r§\x001cD{å½\x0007çï\x0013KD3¡%¾Kº¯\x0007fÀÌÝæe\x000bZûÇ\x00003óe
HÛ4Nê\x000f\x0008\x00164sh¹Ë¡=|ùåöp\x001eR³*W°(÷CZ0;SØ|=MxþöûÃM%y4Ë]ÒìE4¼ÓéYÖzG\x001d\x0008ØYÂM/j²|}>oÑ¼\x0008M¥c[ò#¨ Gâ(\x001dFh{/h¡E\x000b²UãiÓ(ÐYZTñ)å\x001dô¾à}&YlÉ¢\x000cK¼TI+Ø\x001cêtúð\x0013Ü¾3;\x0013-µhI´hZq}å')Ôn¤·`÷¹<óÈÚ\îSr/¯\x001aV,Ñ\x0001Í¦J8î\x000enO\x0003÷\¶Îvhñ@y\x0015_ÏS´lü"\x001d«Èºó©E\x0007\x0014!îâqIï\\x0015&+`æ£u§@\x0001JHR\x001aØÙÄOÛ¶K
É®:\x0006º;\x0006Zt\x000e\x0014ø't\x001b8]%°\x0001-ì4Ë;¶,`s(AGãM\x001dÄ%®ì6ø¦Ý{³ÑÚ\x001cOîs</£ùÚq%ÛTl\íh2{Ú3ç²u¨Ü¢.ák;5Ã\x00186º:Ô~9¿§Áu.ëÐhÙp\M¦/:H\\x000eËy\x001e\x001c|ÑU¦Ít\x0006ÄH\x000c\x0008\x0004<\x001c\x0005\x000fM14¿AëÚL\x0011&57g³ÙÎìZÙuÉr·Næ¡\ZÕEûò3Á:óa%æÃá0îTÓj¨Zº3KÓe1³Ù\w:É=êà\x000còÈ\x000b=§³<¦ÖL\x000c©°u\x0007Á\x000e\x0002ÄU(t<\x0014Õá¼Ú\x0012ve£\x000e
°uî¤øn\x0018ýJZô8£¶D0)+\x0016Ì\x001a>,`óÝ7õ¢o
®ÔY\x0014¼çüï á_ØÒJ¶îzÙ7ÅôÿÏÜÛlÙ\x001bw¾¯Ã{\x0007Í\x0005\x0004¾FI2«ZÉ\x000fÌòÇD+«*-±/EÊ,R-{ä×ðì\x000eÛÏ¡7ñ\ÄF\x0004\x000e°sÎ\x000eìsÝå^«U¢-\x001fc\x0003@ â\x001fôMCàÒà|Cà¹ãnóílÝ>u¢}*Zäx\x0003Îø¡§H£ê`¿c\x0005\x0013[oVxÚr»:Tmz\x0013÷\x001a,çä¨{ìðF¸ïZº&4BB0ýñ\x0006árÑb\x0011Õ|Ñ:|>G¨aUÀ\x0003ê&\x001cùþóû¿<,.ò×¥4N`R\x001f\x0013
ê\x0008Û÷on¸n«ÖP¦22(Ë$äû3õõÉP£ÎñÉb¬sP®r2(ÜE
7\x001fùT¡´|Þ\x0007ãpÉ·L^ÆOª.Ävo©H/|PãkÕ9¦¦4\x0000WAå¸¶|<\x0014 !}®\x0014©)Q/Í\x0005"(c×j\x001eö æñõê÷¾bíÃýû\|<µ\x0013Q;,ñÛZ@\x0011W³È]Ñh\mô(T»¿úáöÕ=&Ùî®®_Þ(,µk!
{\x0010ÒúD7 cUq1ªP\x000fü\x0002 ¶\x0005µS \x000e¨$hÃYK\x000f
ÑN\x0015sºÓMq\x0006KUâA§|«&\x0019$:Æ²=G»WÌé[N?ÇÉò ùÃ\x0003&5\x000bhµ§\x001d5¾AC\x000b\x001a¦@ó¬ \x0007%\x0002c\x001c[t8£A\x000c\x001a[Ð8\x0003\x001aÉ9D~bJ6ëHgÈN\x00182µi\x000eRÏÄü¢¢¯^'Å0j±r6z'¶Ñ;æÀ¾Ä2\x0001Szt4ÄÏ\x000cRRbÒÞÕOùú¨-ï¤%gK.4èM/A
\x001d)ÌÙÔòËOvDU\x000b+\x0005.£P£'\x00021içìõ·_R\x001dôõ
Ò³·£E3êx\x0010v^TO¹Q-ê9ï\x0015\x0008ð¿\x0017ÕsÒsÞÉÔó\x0013TÀ
µòíyø§¹nãÃÜÆw,ò·S<²êv\x001aM\x0012v¡\x0013LÅN8/
¨ò\x0017çÉ+6é"\x0015°´I`&(ñ9`¨%\x0014yã["\x0005¨Õ\x001e£\x001781iwØÃÌiïó_odØdçÔ²òCíþÍ¤:­ñò\x001fðãôÝ§¯ï¹zùøþÃO§\x001eÐ3¡Êhx[ÅvTÍ_«AáÔÝ«ûÛ·W/onïî^x=g@Û\x0002Z) \x00007âÍ©¤ÈÚ>
äW¾\x0005ôR@UËymöôEMÛ¥@Ó£\x0003Ío!`h\x0001\x0010ÐZOwðìÌ=µ¢æÐ¦[(?\x001aÉ)\x0004L-`\x0002Bó:ìø\x0013GÇ.sü­ï\x0001\x001e¢8\x0004ä(n;¡\x000f¬hq´
}c]_ýý@ÕEH¨;B-%Ì_¶Ì\x001cÌÑå¹9Ñ°Üý6ì\x001cz\x001a½ôÎ\x001exØUä\x000c\x0007V'ìåëü:\x001aü°-\x0018©\x0004_ÖAT!$t\x001d¡\x0013\x0012|Í¥¹ÝùFËÚ\x0000!yþÆjP9.$ì\¡úBü²\R¢¦dC¨%EzÐÓ($ì\ú\x001aH©Ü\x0019Q\x001a_=©ìÌ÷ºBè<
H=qµ1ß@	·HP\x0016Â\x0008{Ïcè\x0003\x0006é>ÎU\x001aäÒì\x000b3 °
\x0007¯ÊBBÓ\x0011\x001aé7öÔ\x0000\x0007vÑð\x001a[	a *%$ì|
H}
 bYñ5\x0010êÀ)Ôt"ÂÑó°ó5 õ59È×\x0000
àÓlÂÃWÖ\x0003\x0011Y!açk@êk\x0000ÙÙ«\x001bj\x001bM¶á Û+$ìâ.\x0006^`¸T\x0010ßfhÊ¸W\x001cw]À×Ä/Jùª\x0016tÀç7ô\x0012¿ñ Ù#$ì¼5½µZôe\x0017B°ôô°\x001a-6¦½«ÐtþÚHý5@àÞx0æó½ÜM·\x0011!`\x0017\x0018\x001ai`¸Ì\x0002&g¨\x0015
Ér
a\x0018tð
	»\x0003ÅH\x000f\x0014\x001cÒJAÃBHÅ¾¬\x0008r	Àî<1Òó\x0004KD©	Z'Í5¿9ä¦ÐÕJ4·6Ro­­ç3Y\x0007 [¼³}¡µæÜy2.Õg¼Î\x0011\x001a©#ÔNó6ÖØSFÕ\x0006\x0015-\x000cÄ£6\x001a\x0010À¯JôóIr\x0001ûðpõâáóûº)H§ÔirXM·(\x0015@znx;:*àîúêÅõÛ¼)ÿ³¼¦å5³¼_<=\x0016"8V ç:ù¨Æ\x0013ðfm\x000bl§
\x001c)üÎli*òÚUÁK±5L\x001b7r!±W@5ÎÙ¸,!\x0013a¬£/\x0002ÖÐM3¾\x001cïL©%þÝ§?ýñoÿûó©T#ÖQ£~|%\x001fª£áyÈq¬fY÷êå³ßÞ¼9h$Èf9öªj1dR\x0014\x000fÅüBºñù|¢Y¡\x0010Æ^"DÓ!\x001a9¢öOx¬´á,
hF´ã9°\x0012Äf.Ê\x0004+9b3­\x001eÝ\x0015ÕB3£6Ã.\x000f\x0019c÷¥ýÄÎÿÒ¸\x0010R4µ<Ðk\x0002¨ñìp\x0011#t g´ú	
5³¢`IÛ\x0002´\x001e*È\x0018»åè'#\x0016âó\x0018VËÛ\x001aB_ïú÷í¶´\x0013¤e\x0014ó1]dtô\x0001`(\x0000,ô\x001d¤Cæ\x000b\x000e=\x0017§\x0004Ü\x0015\x00029 #È8¤±\x0013ë\x0004Pn\x0012Àú¹\x001e!CçÂÿÁìJ\x0011HÆñµ\x0016á½=\x001eù,bìüO\x0010û\x001f×\x000bi»fÆª\x001fiY
\x0006òÍ~·\x0003
\x0003
\x0013\x000eÈ\x001b\x0001I °yå#uÜoÈÎ\x0001\x0005±\x0003rZyî­NÖâ-h1¤§Êªü±-$2ÈÎ\x0001	\x0007ä\x000f{;ój>m,[R\x0007ß ;\x0007\x0014&\x001c¯5\x0011ç}ó¶ñT]Òp¶©\x000c2tAþ¹µá}\x0013qÄI±$ëü¥±\x000c±óaÂGæ]C-ô\x0011\x000f\x001e¶££ä.àºp<ÃñlG©ûò±=Åh6pÅO»í\x0018;7\x001egÜ¸å\x000fÔ¡/3.[;bÙì^ÈÎÇ	?;´±ã\x0013ÊjØÀCè÷_\x0018bç £ÜAæx::³\x00177^³Ãq\x0005Ãöa\x0019dç ã,Ã?B0õá0\x001fÙT\x0018Ýp­\x000cÒuN\x000e\x0019ò	Ôlä+mñø.\x0011dç £ØAfHÍ:CÑÕtdç3lÉ1v\x001e2ÎD{.p	_¾òºSÂþ¯:÷&Ü\x000fÎ\x0001.¡®Gåe2¤wÜB3¬\x0014Bvî'M\c©Î,¦²ÍæSuåE|óI\x0013×Ã2`hÙ×)ñc1ÄêÃÇ
¾2ÈÎù¤	çã¸®"àDQÏ\x001aÇUpq,5/ìO\x0012;\x001f\x0014êèZ\x0006ë\x0014H\x0013Y3ýGvêBÈ4sM4héð"-|=¬\x001d^û=dê<dñùVS¼O@gÉk!³\x0017ß\x000fÙÅgI.ÅãÊ\x001dvénªZ\x0007ü¹ýî$V÷Á+§T¨ðU¢ òìèÆÃeEÐ#ÎÜa57´à\½ÄnÅì<ìÑ´2=åL\x001a\x0007õ\x0006\x001c8\x0006õªM¾<îöåZ÷_[ÏäL
v-»;Y\x0012ÚÆ ÍVÉ­½±Ö½)õ)\x001dµ¾¢:
_¿ªØÚî\x0013Gk×CN\x0019ÅËpB-ßm,·x^`ïèÐSNxJ¬M¢Böèj\x0008\x0014êÁ8*S\x0012§-º>ìºhrUt¡ÅbáHÃ\x000f\x0015\x0008¯9kÖ|xÌ°\x001a.kÉ·\x001d]íJùI\x001dmÏý\x0019p«®Zp]Wíã×¿^=ýôõó\x001fNE\x001b!9\x001eâó"(³+½±ßãh®\x00196\x0006ÜÜÿÃÕÓW÷o¾?è[D/Ez)úZ\x0010\x001dæ)Mi\x0001dÂ0\x001ac)$\x000c-a\x0013ú\x0011\x0003ÅÞ\x0004\x0016Yq­\x0012"Æ\x00161Ê\x0011#]r¼ÇÖ\x0000î¦3ü<ÒÐ\x0014\x0012¦0	ÁPQ¶÷ò}\x00190Up¤Ce;a;0Þõ
\x001b\x00115ÆrÊÈUÏÑÌ\x0008\x0019¡c\x00193²\x0018	¶7lGÞ.n$~#dì¶ï\x0017àP-ïè@I ´cä-=³1_çVR\x0011y?f7{û§??üòËùúëûÓ#{°Ûð¬	cm4îøn_¼¾~ûva|}{zfÏÊá ]\x0010ÒÅ:-=A$µLo\x000cO\x0017Ñ°JXÈñRx9dô4TÀ\x0004
q½aA·ÊLñÚq"niPñyn=¾\x001a\x001aruLßZÐs;ö«#\x0019»r\x000eá÷³¯\x0019ñdO0ç¼\x0003\x001c\x0002hP\x000bóY7¼Ã<»Ï§Jûüz&ofm\x0001³¡p¶z\x0015ÁüxÌÜV0Ó\x0019Å,]\x0017WbÉ`uÂ\\x0018ª³næ²-\x0015\x0019\x000c¨Ý6s-Ó=\x0017°Pë÷Âøv²\x0015Ìµ`Nd0ÇC=óYÞç\x0006·\x0018Ço[¹|Ëå\x0006\x000b¡ÆPÆ°ÁL¡aýV°Ð\x0005Á<\x000fHÂ\x0008Y\x0005¶Xª\x0011ò.°ØEá4\x0019\\x0003åàò\x0004\x001dC-ë\x001d`©\x0005K"¥'\x000794O{2h^úi¨3½«éôM\x0010·Íb{'\x0003ID\x0016ëw3\x0014\x0006ÜLÖû}ãO\ì#Û Í4KÈË}·u_Ë<\x001dá\x0019 ±\x001c\x0014D¾ &;ÚLÖyX-s±.\x000cÁs2\x001fÁ\x000c+ÛGLo\x0005ë<¹²Àê×\x0001µ´L×)ôãLäV²Îi/³o(éØÉràãµ=Þ_w¾LË¯CS`
l3Jæ©]Çî|\x00169³l2\x001aÉo«Ùd¼ÌÜpBÞV2è¼\x0019È¼\x0019ÏÄñ¨\x0013xgò@¼ü9öìLè¼\x0019¼5Ut\x0012¦\x0013ÛÌñÖ\x001cOÞJÖ±"oæ\x00169ÂÅfùêäÙf\x0014þh5ÁØ\x000eÖ± csøÃ;\x0013Ëø\x0000p¼3Ã8«¹¬s³ s³9Ì(\x0007@ÄÖ¼ÐûYìaÝs4A\x0017É(µ»µ\x0002*óÖd
â\x0014Ç5ò[Éº\x0013\x0000¤'\x0000Í~ÍÁÿÁdìÌÜø	w+Xw\x0000ì\x0000àÙ|4Y\qd2Þi8ñm3Yw\x0000ì\x0000 y©_IÐ`</ÕïºÆAçþAæþÏX×ÀdÁp\x0014Ó<é¼¿yÿÚ	\x0018s
®eq¬ô.²Îû\x001b÷¯7¹¨
FBd2^ýzÏâ7ó7"çÏ\x0004\x0016=_ª&C¶¬ObH½?LP8`¼\x001dk½¬óþF\x001ad'\x001a\x0010«"
\x0015ÈËÌÑ©Õèõe;YçýÔûóÌr£8|x³ÌÿÑ]d÷72ï_§ß$\x001d¨\x000b\x0005mVg*ï9LçýÔû{2Y^q¶\x0007hÛæçv²Îû\x001b÷O¬ñáv6YÍ\x0019ïÊ\x0019î\x00000²\x0003@Õ£3\x0019¶>£ÇÑÍT¶óþVäýQ/\x0018*øò¶\x000c<¸Ù\x000e´Y\x0004d÷·2ï¯¹É\x001frçú \x000cçñì\x0001ë¼¿þÀÚc)±É\x0012k·¬óþVæý5·zÇài\x0000É!Wò}Ë¬Ob¼¿«S\x0017RL\x0007ÕëaWÚßvÞßÊ¼?ð\x001c\x001e,ÑæìOËâ¸e`+Xçü­Èù£ÉJÉÒª\x0015²ÅØ¥]yÛ¹X+r±NÖ¼*zµÅcÐ¶\x0004=®CÚÈå:Wæ¤IYìíNSGðJNõ<°ëÉËu\x000eÃ3\x0004S8Âæf0ÃáèÉ:ád^Ü¢\x0002\x001cÅåÆm\x001e[±:oád±¢gQå¡\x0006þÜù¯Á\x000egëm&ë6¥>.1Ytø0W,Æ}\x0008à÷-²nW:Ñ®,,ÒO8ðçb6\x0008Ãéu[Á|w{É9îq)Z;Øå=¿±ÃV°n[zÉ¶D°Hà±L#0\x0018\x000b×ï\x000bb}·þ½dýãË
5è\x000cÉ	Ù:ÎÃøáðçÍdÝié%§%¾¨FR©Î\x0012dè\x0008<>\x000cÄ«\x0004dý«¯dgú°¾Ø,5E\x0018:U¥ï0ncÚJÖíL/Ù>Xî7\x0006HxÕ,d<!Ù¤]\x0019ÙÐArbú*\x0001\x001bÀ³JUþ¬oTºo$Ý:¢uó
õ{\x0001Õ»ú%¶ ~¯±´ÁV²nEÑ:Ã#\x001aVòÎ&m-7¬±2ÄV²î\x0019%\x0017Ì¥åµ¬3\x000f¶\x000eâð,">\x001cs°\x0019,u'@\x0000I«Z__\x0005J½M\x001cmÐc	­dÝ2Keæóûg^)~+ô\x0018Ôò-ÓX/e+X`I\x0004WÆó4\x0000 GßE¹Ì
$Ì\x0005d7K\x0012orÌÏ
[8f¸¬>\x001a7¾mãÒ«7%XeÙd*\x001f\x0002×x6\x0019wq8n¢ßÖW>(A¤á\x0015Xz,Ì×ÜÀµR8×Ù¸
f+éÑ\x00047l5Ç½Þ>Õ¢¤¼Ð\x0008-ª\x0000­¯ÊP(Èã<fjv)ÐK¬\x0004â=\x0000{\x001eÌu_ùÿVb5Ã\x001f4ß5Q*Asû1ô`C÷Åoøo%VKt;Ï\x00079_érpÄ\x001bt<ú{+ÙªþGR\x0000´|OjaÁñ\x0002@d¤ûcHØõÈÚN\x001bzk:m6Þí(C«ü·/tû²íÚþþ¡³ýÍð*| 9¼\x0011ó£¾ÛsUOam»¼é%¶[Î+\x0012GóÜçýàF\x0013a\x0004kº(ý°±>ïã3J}áä·j³+Ña`Í\x000f\x001a\x0011`T¬çc¾ïQÉªqõ?û	p,s
A÷\x0015Ñu
¿ùÍ³?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=\x0011ã\x001cà<~\x000bÿCowjþ°/(å\x0012 ¥ì­b·\x0005:0]\'û8¢ÉR4ùÿÎ'S¥\j¼\,(\x000b|[©,²YjÅÈÑbSc1]éR2ý\x0008_L+ì¾
ÌÑ,ª\x0016èûB²lÂ¥é\x0012Í¢Gøh
÷Áæj2À83Ø$AOd¶Ì>ÂGSz#ÓÀdFW5Ãp\x0017òmõÑ\){f<ñ£)"ÔP"y6vî\x0012Í¢ùGøjÜÓSÓfe-=5Ï&\x0002ä\x001eÑî;¸\x0016Ç6\x001fy\x0000ãg}LÒX)3SéÈ.Ùj7ä1ü\x0010Î6Ráw\x0018;JÓkó|Âiì­rEø#ø"ÌYcß
?âùµMe>ºD«\\x0011þ\x0008¾\x0008ôÞ¤W8·1M\x0013\x001eËÌ!H1tVy#ü1Ü\x0011ØÝ\x001e¤K¼¾ ÆÕ\x0017á³M¥
»d«ü\x0011þ\x0008\x000e	ð\x0018 )ªp>@ÆïfÉ´M\x0004Í]Uî\x0008\x0004$(I¼AH¢©5&µ)Ú.Ù*?GÂ´¶:êH\x0017\x000b
1°öÙ¶Mmdï­òHø#¸$\x001c¹bA¶`æ<1klÛ¦²¬]²U.	\x0004\x0004\x0006]%Úí`æ¸DnYG¡({¤Ï&*D<KÂÀbzüløÕ\x001cU\x0018CH÷H:RT\x001ex\x0004	\\x0006\x0011¢Q\x0013µ%|4j\x0016\x000cÑèTihunä1#ÁIèÿ«`ÀQIZOJR<ÿ/*D<G"uv$­%GRZ­²\x0001x¬×Vmñ\x0018f[XÌ¬`MQ.R\x001aKÏÍOÑ\x0015tÉV\x00197ñ(ÆÍeöM.cä\x001d³?Ä²Äüc¹[¢2\x0000âQRÓ½A6\x00163üQM\x0012;s´\x0011¸)\x001diwà½\x0019}`ZóµÓSÍ]²UïM>JÞ!³Ô\x0016ûh>Ñ7ïgý9+w{üëÝööËß[êI^¢æw¤.³\\x0013ÍºmÒ;?ø×óÃ³wÿ{\x001e´(Aõ áF!ÝqD­iÂÀ\x0019;Ëú°\x001c³)1\x000eÌÚd¶A¸¿\x00004¶q:#fGà\x0017cæõåè¹\x001dáx±F¢3üPm´Vc°¹àå e\x0005Zv\x000eÎtZt
läL\x001bEN\Ìw)/\x0005í*Ð®\x00034ãqÉ!ÐPi\x0015ûfc]7·í¸ÙÕbQï~Îªu\x0007í¨q8	P+	±¥%R';îêV[m\x001a!x}´vð²Aß÷²\x0014´ª@«[íÉ\x0010m`"Í\x0018Jí©Â#h]Ö= E>ép«Ñe3RçÝTóH#êJS\x000eU
dÕvx
^jFì¼BÌR­,\x0007í+Ð¾\x0003´Ö\x001bÅ±Í\x0012Q6\x0018E]5\x0008´¬^¢ìyÀ_ër-\x0006×\x001b\x0018,ÂPö\x001cf\x0015U¥õTÖó\x001b>\x0013Ï9m#\x001c\x0019\x00187Në©ÊgR\x001dN\x0010²Õ©\x000c)Ø\x0005'üy\x0002¾å¨+µ§:Ô\x001ew>nä\x0002ÔñJ \x0013>1\x001c\x0007¿j¾Uh)êJï©\x000e½ÇÁ«Nq\x0001Ìï¦±\x00008l¬U91ÛÍ½\x001cu¥÷TÞc&\x0007ØT¸EAÓ®\x000e>;u¼\x001cuå9©\x001eÏ)xÓR\x001e6êÀ¨®EN\x000bLÕsÛPëJè\x000e\x001dÂ­¦*â~C\x0018j>òÃNZW\x001aD÷]ç*¥w×B\x0012hÈÅB]i\x0010Ýã8\x0005Ã,©]\x001c3{NdÑg\x0017¢/G]½EÝõ\x00165ù RzZJ¨#Ô0Ô5\x0008µ©ÎÚôhk\x001fÞ"vI\x0013M{Ô{¸]\x0002ö\x000e»!¦Ì{Bs\x0008m\x00115'OsF%j6U4k\x0004]©=Ó¡öb]\x0005A\x0007\x0013Ã\x000cÃ¨ÔÇ\x0017,>[ÚVjÏv©=AGÍ½¥t¦Pë¼\x001av­muAlÏ\x000518Ä{ÆâsÔ¶¿`{Ø,hlU.øh%4­½M;4ÐôÿþåîýÕå_î\x0008u\x001d¡7\x001eÒeÄ%BTWv*ýú\x0006öìÐHÓÑóç'Çÿz~4+F\x0011¬\x00071 XïC9K{_¼78]f\x0018UI½òSÄ£k\x0005\x0011 b ;\x0011Æ©ß0t\x000e½\x0016ñAt%\x001e!\x000c·I\x001b$S¸Ç¹ÝðÐ#a*1ÌÏa<N-Úðÿ\x0001\x000eÁ\x001aÆÐVOîY)H1~\x0016\x0004ñ³\x0011Hl\x000e\x000fcÓ¦	*ÅÓ\x0003Ñ\x00139µT\x000fD\x000ey ÐC\x0004 áébyFó]jr\x001a|­\x001c®Ãy \x0006wØ\x00069\x000cåüS6ñODUOD
y"Ù8¥\x0013\x0008.\x001e\x0008y?4"i\x0016Dí\x0011³(ÆãÈQSMÜcjÝ0cãpl¬\x001b#\x00113NÌ\x0013VÇi£yÈ¦l: ë¼×Éò
Í9\x0008*p¹YÒÅmØ®G\x000cñÀCfÈÚ\x000fý\x0015¹&7Ë
³\x0014ò®\x001a ïHLÛ1ç%À§FÑbjrÞÎOc.Ä\Ýe¾ú23adÈØÀ$-O¦Óù-\x001aÓ·,nþ\x00109\x0002?\x0008}öâòK\x0000ý?ÿù_?ß\·\x000cüÉ\\x00070Àö¥ÑUPÈnà"o|qü.à>8|uúúÝ°ß\x0007
\x001e`ËlXJq°\x001b`7C\x0016,OõiK4\x0000NhÝæ\x0001Ö¼\x0002\x000cÓ¨«\x0000\x0003!\x00132H@\x0005\x0011ÙÈ¬@¥áåäF¾%¹ª·\x001c=\x000fÿ\x0000Ã'qõàO\x0017Ûu0YäX`>¦¥\x0013Ç¢k<i#«\x0007::|=U×¤ÁÏ¹N¤Ái`õù¶©ó(xé\x0006k÷ÙmµT¼·lj[W\x001aT}~xWGô»»+sý>àk¨ãÏÙÍÝÔòâæç÷©'%*>8ï/¿ÜÞ\]
ð¤fÒD=&­Ö?\x000bº\x0018\x001a£¢RPJÆdó÷ÇïÎNONÞ>;;=\x001bUO_=nØ\x0010sAÿ÷ïPÁÅ?M¨Â¡\x0001#GDÅ h\x0006TÒ¥Ú\x001f ]\x001a«aqÐ¤ÏÒoÛiÉ\x0004\x000c¸$L9©tZÉË8ÖKE\ª\x0015\x0017ì^\x0011\x0017P~EX<y)\x0000+N\x0000vÀÒñ¸tëq	\x001bï>Àr\x001cÔJÂ¾\x0001ï<®¨¢Óo\x0003.\x0015,FÜ÷1\x001d\x0017Sim$ÀäÑëaYHs¥ß\x0016XÚ¦)¥\x0000+8\x0015@\x001ep)\x001fÑóXè@\x0005¥çôÛJÙÈÜ\x0000¨Dì4¨\x0004\x001e\x00171 Z\x000fËAQúm%Eì	\x0000X2Ò~EX0ÆpÉ¸]£\x0003WxèÏÒo\x0013.hu	»V\x0000Å¥õ
Â¶¾;ï\x0004\®M¥ª 1cX\x0000¸\dc¸pKgÀåL&ý6á\x0002Ú¹ô\x001dm0ç!¼¸\x0007\x0015,l\x0005âÞG\¾\x0015\x0010\x0018pÁNÓô\x0018±\x001a\x0011`iÖ\x0005KÀ\x001cÖ³ôÛ\x0004§®)e\x0011Îget×Ý\x0012<â­ $1J b´\x000f¸´LÅßËò.Õ%84¤ß\x0016\Â
1\x0010¼GX<Õÿá¸Ä*X¿üvóáÃ/1ñ\x0013TÜ\x0015\x0007r@ö\x0010 ï,jxa$æY°<<D\x0011Q\x0010pïR\x0015t%³` óLËÅ`\x0000F\x0000\x0013`\x0011º\x0004,Rt	WHë\x001602fO\x0013\x0018â3Øêµ\x0016JÐkÚ6@\x0011<\x0016ð#9D#Rc6 qr=\x001aÃÀKo¸2ÞÅÅ¢Å&ë&AIÝd+@RÅòOdcTH¸ÂsAo.±¼\x0003MøÂVµ a1­\x0018ÑD¶þtg&4Ü®GãÃ\x0017òË¿R@V}\x00064\x001a*ðhÒ\x0008F\x0000cÍú\x000b\x000cÿ>ã¼\x00050±R
hF[¯\x0005®6\x000cpô~øÔ\x0002'ùÜ-pæx£94UG8Á	p^ÿ 8<&Þð¢\x0002\x001c\x001fKh\x0000GÄ4Xcñ}\x000bÞñª`\x001dÊ3nÛ\x0004
ó6i¾ðgH\x0016E8®\x000eëÐ}±Ñ#þ,Fc\x001dF"¸ÐðÇÆ§ÔUð>ü¾Íl\x0003æMpß\x0000ÇØ[\x00058VÂ0hc=\x000e·j½Î\x0011Ñ«-§£\x0013Y#À1
öD8l&7ÆtÀ\x0000§ÅëÄ¯\x0017OâXa\x0012=\x000e\x001cXoÁcaüY~y¬X\x0001\x001a
Hð]\x0019£}óM¾þíoòÏð®b\x0006¢L@\x001c¼Üþ2e8]0ã)@ä,Ä>Áq\x0007ïÏ³4ó
síæ~\x000fþàåá981¸?KáxØÔ\x001ayP¿\¿ð¿(=,¨´Þ\x001fG/ã û;þ,\x0013^´O®1×ÚáÍÑ©HªB\x000c\x001dIíWbä\x001a¾#H#\x001d¡\x0018ç"¥¾?\x0019³\x000c\x0002,ª\x0005Aã\x0000\x0013@ðÅ"\x001cn\x0005Ô\x0008îO+,\x0003\x000eRüY\x000e'
!\x0001\x001cÇp(Áá\x0004Ç/\x0015ÞÄ³ø³\x0018ÚÁ1.(Âqàh¾útx4\x000céw)\x001e\x0003£¯é[Ç¡\x0001x¼txyâÕZ\x0007J»éw1\x001e¡Ðs óé|`\x001b\x001dá±j5\x001e\x0005\x0005éw)\x001eÇRõ)àq>â\x0007<áÐ\x0018>t#öýÒ\x0016<Àg~\x0017ãá©Ë$àñR wa¸Ç$\x00143õf\x0015pqXô.k\x001e\x0003ÔkÖ'%\x001dáqÂ gÊYû}¾øß~R±ô¡¡ô±;»7W©ÎõÐùÀîwL(ìÉÝ\x001cë\x000bÌ}O9á9?\x0000"Ðy@\x0016\x0000Ù\x0006@\x000c®t@\x001cè\x00010°èb\x0004@âÞ\x0003Z\x0006\x0008\x001aNÅå'¤Ó{\x0000\x0004£x<e-¤ÅÊ\x0010óÎß«\x0010\x0001r\x000cl\x0017c-ÞA\x000f\x0015lªÂ\x0010êªpä½Wz) 0`L5\x0000\x0012Bl,\x001ePÎ\x0017WO\x000cüõx"\x0005DüY~@Põ$·\x0001u\x0004$)¹ÃUÇ\x0017òjPB¬0\x001aK>Ã\x0014½Í\x000cËeR)
¹îO£.D\x0014ë\x0006L¶<3îy¤L\x0004DPÊÃ&\x001dºÎ1°\x001e\x0011(ùô»ü\x0016±´­)¦\x0010ðiA\x0007¤\Ï'³\x0011m\x0003ëLÊ=ALa%QqÙa×ôzD."rM\â\x0011$\x000c¥O\x001aæ~Gq!"\x001f\x0011ù&DA\x001fz,V&¢ôÙ\x000f[\x0000A»Ã³ô»\x001c²\x001büf.\x0016ë°\x0001õ<|Øïó,ý.·f!|·ÁïÑÑÃÝ\x001bk,D¤#"Ý(\x0018Uï1×¬³}Í\x000f_
ÞñÑ\x0001\x0000DÖµ â"\x000ej\x0001"-wyUÊ¸Héîu\x0019!ÑSú]\x0008*\x0018t\x0008Ø)*&\x000eèþèp!\x001a\x0018.H¿ËÑú±ÆCÂ#\x00022j\x0015úþØy!"\x0013ÏÇ4Oð\Ó\x0007³,Ý\x001f.\x001c¡q²C/Â¾Ûgéw9\x001aa('ej5ùCK*q¹\x001eã
Ã>ÏÒo\x0003"\x001d;Ú\x0000\x0011×Ð\x0010	ºÑþþDÐ2DÅ(5\x0011eÉvX8®
ò\x000c\x0015£b¶ãR+\x0016ÃDÖðè\x000fÞá\x0011I\x00019´eðê;\x0000A\x000c~\x001b\x00001²eV±\x0010r÷Ø\x000e\x0015K\x0018J6\x0018³ðÍ\x0004¶~	\x000bz1\x0001rôÉök¥Mp¢áP-C¹à~p\x0003{ÁC\x0014\x0002zt²\x001dZCÔ~#\x0012i\x000b\x0019 ò\x0015«\x0012\x0011ý²é\x0002Dü×_Í§¸\x0001\x0008¬\x000eüçÕÍõ\x0017Øú\x0013û\x0017·?]O¦¤¹ö\x001bª\x0019@ éÁ§\x0015{
¸+HÐÃz\x0014ãû\x0017gÇ/_?Î¨\x0004\x0014CâO\x0013,¦D5\x0007X`C0q¯$Ån¯\x0001m!®\x001bþ\x001f·¿^ÇººOùâ`ÍÊÁ\x000eÇd/¸þÉ'±\x0006.
üû\x0005)ú°Oå`÷ïs\x0018!\x000e\x0015r%F£(`«Bb¨='\ÿ\x0012%m %ìñ?«\x000eRÇ½X\x0001dø\x001b@#HMõ\x0019ý@·h+H\x0005	\x000bUe-\x001a@êì]y\x0015\x0019öÒIRþBû!\x0007\x0019íQmZ0º8\x0015\x0002\x0018µ¡\x000c=Ê\x0001â `\x0010j«Ðr#9u\x0000x\x000b\x0007ÆRw\x0011ú\x0001O¾	dÆAåè*i¶\x0018¥rÆÆyiQb2Ø« ëþük+H\x000b´\x0008éw\x0005H\x0003y«¨\x001e
WR%Kâ<:µRHuo«b+J\x0017ë¿NòU(-£@I9n±«!8ãØ\x0018\x001bNRxÝ\x0012F\x0017¥ß5(Ô{ÁÈ\x000eÛQ½Ae\x001e\x000eÛ?¦hD	©
Y',\x001a¾¸÷ÞÑÌ\x001a¬+)\x000f^uDù@Ïl+ÈXíH¿k3ìª	\x0001:Ã8"\x001c%&XBÐf\x001eðI\x001bQB\x0005#ý®úà\x000eK,Pz\x0016ÖÒ)Bé\x001eÊKµ¡àõ¤ß5(iL)\x001d\x0017`¢ûÊ°\x0011RZ¶ßK¶\x0012eªÓ¯ó2\x0014¸?ÉÉ\x000e\x00170÷\x0005õ¦\x0010%¿¿	¸\x0019¥(Ý:q&µOÞ\x001cæFãËF8lRB[Tú]21S\x0002JXx\x0003(úâc¸Tp½Óï*\x001a»¾\x0003J\x000bNGBqt@O6\x0002%TÓï*\x0014\x001dë "©ìÍ\x001cq'Æ¼q\x0005\x001d¼éw\x0015JHmD£\x0015\x000f!<Æ^Ò©
c aÌ&ý®\x0001ÉM\ß\x0007(\x0015éôè\x00101RN?TyiC	\x001bô¥ß\x0015(=\x0010Á¥³4Á
a$!òÄR\x001c\x0012\x001eÒ@\x001d-ý®Ai5zDÚ¨¸ 1U¯iÜ+8¯]_üçß®nÞ#un$Ì}w»ýëÅíç4\x000ep|{9+ªõ[Í!0K_\x001a[iBX»×öùîìðû£³·i àøìx\x001eWÌ\x0006ÈV\Ìc\x000fK\x000c·96y
ÀÔ~Â½\x001dña+.\x0011µ)ÃD½\x0011ð?N!¶îE­ðM°B\x0018óB\x00026}êãPéÞ¯h8tI4ÃòèÐÓRÔrÍ\x001c%Þ+ä´ã\x0002
gÛç[\x000fVhÐ¬Ô9O¸\x000e×\x0017ùáï?_ ?Af%8üù\x001fÿ}uy\x0016¡/yì1©µNJÐY+Í¿ï\x0019=|utr|¶O«\x0002$´	ø Û0"H	Õ4#MÉ_¡ö£æ I¬\x0003é¨n\x0017Îo#°øËÑ¿ïÚ^\x0010æÃôZ\x001c'\x0010#B,3Fîý~`c\x0015Fh\^ý©Ù\x0006»\x001eÒ²ìt\x001d}Æ¸_Ü[\x0011r\x000eÔxÞþfL$ÖÇf\x0011Fo*lBÜÓö½
dðÖä0\x001eNÒQ[¯D\x000eJ8É1O\x0006¶öÊµÊ\x0007VA`\x0002,UQÐ\x0008\x001eôj \x0017HÚµ %5Q\x0000(¬`Xo¤þýÄÁ\x001aRS«1êÈ\x0012\x0018o¤¦³\x0010,ÑAý¶×&Ûë;-DÆ!à\x0019:þùíg4onÿñßàl\x0008CRK.ä@ ¿i\x001cÆfÚíÕ¤_½9|ÆïÍÙ\x0002Dÿ4B¢v/\x000e	Y°\x0014ÆÂÁ1²¦\x000f\x0016Ý¸&XÐï¡é¨\x0006>6/;D
¥u\x001f* Åÿ´¡R\x000cÇ\x000e¹Ê÷ÞxI°öò¬í°*ÿ´Á\x0012\x0006»
\x0002,A½DúPµu\x0005å\x0002øOãa¢Oè©Ð[Aµ7ÓÇn\x0007Öþ
ed½¾oÁ¨IÖ[bFÛN\y
°\x0011Âyl\x001eÀPÄê\x001dvb\x0004»\x0017Wì ±Íç%\x0004\x000e·r\x000fìb8G iÎ\x0002feºpí
×M¸´EtPô0cÅB/°ìÊ¬V«p]üýÃç÷ehÿâÓÅÏ×)Ä±>\x0001\x000búCÜ	µIÝª°Ý	\x000fK\x001bWkÓ\x0017ß\x001d½:~\x0002­Î\x000e\x0013ùA-Ûê#&\x0017Ëp&h0ÅìEÏ­ ÊÕç\x0004c¸\x001eSÑÂÄÙ1\x001cNé;&(«À É\x0000\x0001!Q\x0013-\x0010ê\x0011"ÞuJ6 þ´`\x0002\x001aït,ÿKô\x00190#Èëût0¡þ,þ4\x001d\x0014Û ¦GpmÀdîÁ$àDãA\x0019ï°âÍ'á}yÐïõf¶îøÓ¤\x000c\x0004M<ép£RãX8\x001doòÚ¯'Õ¥ýõªÌÂüfûùËÅÕda\x0013Â \x0008G\x0001û¢IC¨.ü
Ë¯r¿o=xÆAe¾;:E\x0002tøN,F¢8Nò\x0004$gÇQÃ\x0018\x0010Þü>"[¤dKX$ÜeH`w}b	î
VÕ/¦
Éß>^üåÓ]éa\x00169²`ÕÂí¹¸îÞ`\x0012{h·äÌig¨1ÜØú}\x0015Y2°k¯^?tuvàèÁ\x001c^YiqX×Àò\x001al\x0017Ýk>\\x0003\x000e\x0012EÏâO3:Éw­QF(Ê|ò="\x0006x\x0017ÿË?l¡!\x0011DL¿Ål_p]n?N]5	\\x001cQo?Ièj«¦\x001c\x001a\x0018\x0018ú»ôêàåað\Î¾Å\x000568ý¶à
\x00126]A\x0019\x000c
P:2\x0013%^}\x0005	Å\x0007çVá\x0002µ~p\x0005ÿIê+ÄZ°OÁêUÂuùs\x000e×ç¿\x000fæWäÄLø;\x001a§o·¿\x0005ÿs¦\x000eÏ¨\x000e/ö
ëÔå\x000eõ¦¾=ü÷à>t¿v¸ øìe+.\x0018"q¹\x001aB°/MZvÿ¨ÄrX»p«
\x0017\x0013|\x000b¸4vp*(ÅåîN\ÀçÅyëy\x0019¯¨Í\x00077AIê§¸¿Q¡\x0001\x0017ä¦ãO\x001b®à)\x0018:/±AX\x0002}\x0006õ\x0010­ÚR\í?m¸\x000c\x0006µ0pq?ãýÃ·
¸ ã\x0017\x001aq	äõ\x000c¸lîÂ)åëþjôr\pôÏDÑv»\x000cWøo0U¤cÃ¤{o9F]rØs!0	z9þ4\x0001S\x0012gr5÷&%Ö\x0014Ñ´H£ô½}cËQi¸ñºùÚx\x001e(lb×]ZÖ\x001bµ=Ãá3p<Ö\x001d×¥¸Ôû\x001cÕj¸\x0008¾\x0008+î\x000eß^n¯ÿñÿÝL\x000e¡`\x000b\x0015«+Í1/C>+ïóâÏ\x000f\x001d\x001f¾~qúÐ@Á_Ì¿\x000f¸f&.)W\x0017WW7w¿NAc>:à½F\x001dÆ±ú\x0016H+}à÷B\x000b§\x0016\ÓóÅF®}#6.°ãFÅµN4im\x0008Z¸½Ð$ðhÆVlcX-½Ñ\x0018	sÃhQ\x0004ççÁÀl\x0006Ü/\x001f..þú\x001bîØ{¦ËF oþñß7wWSÃ\x0018F\x0018NÃ\x0018 ?R\x0014\x000bKÒÒÉ=0ÚóÍÑéùÉ<JéÞ\x0019ºyT±w\x0013ÖÂ½§~pû¨Ègï§tõñ×Ë«í¶¤®¤üß»ííOw\x0017_&?!Ïup\x0001Ó4é\x000b"f@æîÏ¾;<{y~ôn\x0016Ñ~u`	¢àG{\x0014*IAô8ÞËûk\x0003K1QJ\x0003&`yÇª¢\x0016BÄDê±ûk;Ó®áï¯â\x0016
´õû{¹½ýp9\x001d¥1pql\x001eÆ&P*tvy´x}/\x000fÏ^\x001c?\x0018¢e`iB\x001c~Ú\x0003É%wC=¶R¨]¡øÁ,Ò4²_Û¿ý\x0019÷óÄ­<\x0005°×\x001f>Ý\ÞN÷Î ¿$0aJí¢n¯\x001eL¹½>~ñÝéñÙ<0¦j\x0007\x0006\5\x0012±\x0019\x0018èHÝÓÔ¦ ¼0;í·®ù\x000c\x0015\x0002\x0007ÊÁUÓ/¶×Û©ÌN\x001cxÂÙh`²AÛ\x0018\x001c\x001dL¾9ùÐäÃ×\x000few®øÇ+\x001e^c\x00100ªwø]\x000c'r\x000c1qkãQ±ýVÞ].âU\x000bá	§½7þÙî\x001fùâó\x001d¼½üéæ·ÛI_ÐS£Ò´CÂk\x001a¸Òls(¼·Ç/Oÿýèìs"xðª\x0007¹\x0004_xqISÄ§ïÝZO<ô\x000f^®øâ¢Ó\x000fÚ\x0017Úð)¥\x0015\x0013\x0007Ìq:\x001b"X÷v\x001d<Å\x0000tùëÂH\x001düµÀ÷òâöjRý\x0007ÏË E$¬À7 $¶B\x0004³ý=xytvò úGp*\x0018Û\x0002ªªR\x000bÀq-6è»B"1Z\x0001%¸ä»> j\x0017qá\x0002\\x001en\x0001ÇAÃ©[U\x0001\x001dìÿIèzÀ±^ÎÖèl#:\x0019l\x0012\x000eR©¸b#úÒ\x0013\x0013ðboFi)<Î\x0018öþíþ!v\x0001\x0016FáùööýåÅ¤Q\x0008\x0016>æÒ!³!ë\x0013ÇÅ$\?ð(Þ\x001e<?<{~|ô A@|Á¦øà¯­\x0000ÃÄb»6<'º´\x001c:hNxÐ¢.\x0004\x0019÷Uï@jÑ\x000eR(¤ó
 U®\x00040ZwÁ&*ms _ý»È°b\x000f¶c]\x0008víúâàèÃÍd `I^\x000cæ+(k¥©´t\x001fÇóÑÁÉA\x0008{}tpôâôÁ@À\x001aY5r-ØÜªÎJÛ3l´Û{\x000f7l;Z[¡µkÑ
óÆÔªv\x001a[Uý\x001ebÝv´ÕE0«/Úx\x001a-
6ÐÑðä>Ð*´Öh­[\x0016D\x0010lÌn¦&£¸_z9XËÙ\x000f´²þ!v,ïtýÕöàÝíÝO0mUÑÖ\x001bÄ«áPóz\x0019!\x001eÐ\x0003°©òÝÙyøûC\x0018EÒø2c\x0014àhÔ
\x0001/>ýãÿ¿.u+Ã°C
\x001cq[¸ã¦ðÇ×\x000f&ï\x0008ã%<Çá\x0005_C <\x0015ç(\x0001õ\x001eÙ\x000f~8ä\\x0002\x0010\x0018`
\x0010¦\x0011!wØe%9¬sL\x0000¡A \x0002´Z>Z\x0006ÐÖ\x0000m3@É°!Sr®ìÒ\x001aA­ô\x000f&ô \x0004îó\x0002a¤BoD\]\x0019W§\x001eÄ¤\x0008Ot}`¡ª\x000f,Tó\x0007|q	\x0014àÈ\x000cÜª\x0008>õ\x0017\x0016í_X\x0006\x001f#±
IØÄlb)
RÍCÑÌ\x001cBÚÐÀV[¦âßÜý6WØÇã<Ç\x0008Í	÷çàßÿû4,aX	\x000bþº\x001cÐ\x0016{5ÐÔKªes\x000f$f&qI\x0013\x001cË\x000e$dÍ÷\x0016R{sýe{9Ã8ä\x00044\x001dÑLÅ9\x001cá$Í\x0014ìE÷åãoO_¿;<~Þ@J[6ïfÖ\x0010/R8¸2ü\x0005ãfW£4ar÷\x000fû\x0019ËÙNSOqNí&^aÌ\x000eÓò\<hÞ&\x001aM\x0011\x001cg¦\x0004\x0007mC§8\x00017
ÇVÊð¿ïáÖ·%è\Î5¢Ó\x001a7\x001f\x0008\x0008U5Æ0<³^\x0005#Ü³
\x001dgèLLzEtA)§F4\x001dþ\x0019_\x0008( M¡Óqk«Úùá\x001f©:Ìs\x00197¸¾¼½ùüyzëRÐ,\x00121æ=]°@02%oãÊÖg§oß>üDÐÀína4pU*lI3D*´YÇ\x001a\x0005ÝÑ|äW¢|(g2Ùy%~øxù]Æ¶^Ø\x001eÃKõüâSlñ[p+;þ?\x0008È®®¶·ÿrrs÷>.Â\x0005!dvÌ¸¬7`
ÏøÙp\x00053¼ÏÁ8eÂwrrxö/'§ç\x0010?\x001f\x0015\x001aûÅw±ïïp\x0001Lh,Z
\x0013(ÏD	Ã\x0011¦æi_1;ß\x0005ýÕ~¼÷4Ã9ÚÞýzðÍÍÝ%H
·F# µ0³NTûÔ<é\x0004ä' 7ttxþo\x0007ß¿xà)\x001fäOþîÞo²½ûr\x0019ó³³G
û\x000fâ÷Á\x0014Ä\x0000\x0015Zgj¨ì¡3=9<mÈó\x0018÷?|\x0003FZ½\x0015¬­ë|#Feñ0qÓ×s1F X\x0011&¤Ó9B\x0002
X:#ÆÔ·\x001b0:>è\x001c¡\x0016µö\x001cS\x001b?`Ôj:B\x0005\x001eç/Ö!¼ýøË\x00153÷¿7\x0017×Mø¯â\x0018|<E·I\x001fZyI\x0010'\x0011á9:~È×®\x0010Öw±	!K­\x0010ÙPUÚÝ)N]Å\x0006õUl¨tÜá &_È\x001c!D§q\x001dÄ?³ÿ¸Ðò^­C«§f\x0000Z!dÌ\x0004å¨\
7<D	¤Ç\x0013MïÄM|x\x0015Uo_ã,ÆçcÃ\x0010à\x000bÎD,án`Q!C}ÃZO¹/ìo·÷ß»ïúËÁ7w?/1ÆXKç(pwÀ\x0019TdÂ	»[¦uÎ»Óóõ»ðÇW\x000fÚÄ\x0002ïþy6ãYÌd¾N4½\x001bØâÆc\x0002^m¦Ïµ\x0011ï¾6oÅ«}Ü£\x001dñÂâÈ\x00047Q\x0004´B\x000fE»¯×ÛÑ¦µä\x0001mì^L·!6©%¼ÌN{Gx¡±\x000b¯õq \x0001OGoûÔÍ\x001bwÚ\x001c5Â
ÿËL\x0017\º0ãñjt`\x001cÕåãíÇû»¿¨»¿ÝgD\x000f¾\x0007¶â/_\x0016è¯`Emöé¸ÙÝèÎk~²uÎçÁ÷@^üîÝC*¬@¹gHP\x0002K(a·FKÊÑj'&­}\x0003Ê=[ÚÇÐ
PJ\x0013Û\x0001%®\x000c(ý´#ß²V\x0000(ÝFÊRé
\x001devâ\x0019\x0016½ûAÖ¯¾
døÊ\x0002?¸r1<JÞ\x001dD.è oÿü³øò±x;y¢æj\x000bQæ/\x0017WW\x000b`\x001a#UÜ+
\x000f\x001dj#<éQx\x001a\x001dwÆÜçâå\x0011C3ß\x001c<Pýª¦÷³\x000e©öä¦@¡xA©r£·\x000ehzB+J¨à8DjSà! £\x0005\x0012çò\x0008 é\x0015­\x0003ê\x0018´kL0è¸#pÃ¥çtGµ2ã4=¥H!«T§l·ð¤"¥äÔ}Oi\x001dÌd8WÂ\x0004SäQ1\x0001^6EÔ\x000c¼£uf-ÒàA'\x0015ê`\x00048\x0005%A;iCÉ%{3ÝôGþåZmïQP\x000fÞÞÜýøãÕ²è.
"&\x00143î\x001aôÁ ñû\x000cÒn&äíéù·ß>4B]¡¬S\x001bJ))\x001dÂ\x0002,NS:Fa2ÎÆ ¬5S\x001bJ\x001fP¢q7u;~sm(Tænê· ¬ÕR\x001bJãb?? ¦uD\x0005¾RùQ(kÔÒî\x0012#ÂÇ<SÔIä(û<5\x0018k}Ô\x0011Þ¸N'É¡[© ÚÜçr®AYë¢6ÊÆÚdüÞ6§\x0012s&¶úõ\x000cÄ­\x0006©7d¬\x0005è\x0008RÑ\x0003\x0017~\x0014Ê ÎüZ©êPr´b»ìv\x001aÒw_¶×?*=-aÿöænQB\x0016öÚ¢t"zcpaé>JsïËN\x000bÙ¿==(\x0019[àB%Þ\x000bË¡Æq&æÞ£Õ&\x001bcäý\x001f·\x0005\x0017ªí6\2Ò?Ä¯é0Ê\x0019BÅï}½-¨PM·¡\x0002\x0003§¥=¦µÂS poâ¿	\x0015ªå6TZÅEö\x0011\x0000\x0001\x0015nO\x0005X÷&\x0007p¡*nüj#PqÀâII_1{\x0006ò^°\x0005\x0017*ßÆ;Ïc\x00065ú\x00026²ËÇ;Ïè-
q¯_5ëúç»­ùq_GD÷ôÕöòörs\x001a«Qxh\x001c(0SéÆe§ïÞÌ)5e\x001e\x001e¼:<>;~È1-\x0010\x0016Ú¢\x0011aEý\x000e *ZK_Uû\x0007f\x0013¾Bk4âó2çÄp'\x0000\x000cá|\x000e\x0000,\x0014Hë\x0001ÚTI»´ø8 \x0019TmïO;4#,I+Â´Þ	c9ôCb9{oÔÙ°P+íÐ¥<\x000f`¦b¶¢ðÝÝkî\x0011\x0016
¦õ!Kì\x000b×PÓC¶|:roF®Ý
Ð ÷PèØn\x0011]¦\x001c\x0007»{s\x0010²\x001f>¿°ÿJ\x001a¦TÝ°\x0012 Æn\x001fcÏN·\x0017\x0013Û»_\x0001
Q®N¾±\x0008àdÌÓmÀ¦å¤1\x001dï?\x001e¼¸½ùü,xn)mxxþoe\x001fH8Û\x0010J u10­Z\x0004&Çç1+7\x0008!¼\x0014Ó~*N¤\x0000BÏ£\x0010ÏPÐ\x0017Öùg\x0004B\x001eù ¤h¨"\x0007>@Êo\x0010¥Ãâ\x0010äÍ(*®=m?Å \x0002¡ú\x001f!²Ø*\x0007\x00105\x0016ÚÇ%"C Bì\x001cÚ Âºú8\x0008\x0010¥NÉ7`f²Ùk\x00180ó§¶\x001e¢Þ @\x0018/\x0017	 \x00129;(GÝÄÝªÍÆ34.\x0015-\x0002Ä \x000e]D(<µ\x001e\x0005«=ê"
àS\x0015¼ý+Ë¸X3}eI\x0008µñÙóâ£\x0010\x0019\x001a\x0011
¾q¨\x0012\x001dO\x0000Q\x001az*Ê\x000fûÌ
\x00135Í\x00120ä\x0014>á\x0010¹ÁoÈ-÷Ùêõ¾\x0015 PP0á
6Åî\x0019OÛß'®A:\x0003´oÉøqX^\x0002î\x000eºãeT\x0016Ø\x0013N.\x000e^çæîúýöA ß\x001d¾zþ\x0000ùN\x0005\x0015H,Ì~¿æ\x0012¨Á\x0005ç\x0006 :²Ô\x001a¥¨À£#6\x0014©\x0002¤j
RIÏ'"\x0015	)n@H@ÕûíÃ\x0016 2àYäå\x0008
øgßlïn±R1uOi\x0014Ð\x0006ÃLw8Uº\x0001\x0010F\x0003ØèÛýtq?Ôè¦}sx~ö`±¢+YVÁµng«\x0004éw/)5\x0002y¸Áh}ÝáÚ\x0014àÀUPÉõÓ%×WÅ
ÃñB8¶?÷¸\x0010/ð\x0007âÕ\x0015<±ï\x0003ÞÜ\x0010N9\x001co¸¸zåå<\x0010¨¿|jßp1§4\x001b~y¡\kÖÂ\x0005C:ÌËÈ×\x000fxsÊ@)0ñfV>6ËmdcëÀXj\x0007\x0004¼ÒÓùB\x0006k,Þ\x0000äc+ñ
lçæR>\x0001øXAçË__h|rkÏW:
JB\x000c\x0017³I\x001b¬¤¶P¥üèûËa.óµú!85\x001c/0©\x00056Qr±ç/\x000c\x0004\x000cûëâÏ*ÀÎ³-Y¶:\x0001¶Ù^Ä#\x0000ó?ÿå?äÇûÌÛÝÁ«»«Ë\x0019·Á{r×\x0011ªÛÄ»«È¦\x0002h#g\x001f¼:=?9~ÈeØ\x0004bSåVä©á\x001f^tA\x001bòmäó\rß6,E)X6»ÀW÷©{íºncÏÿUø\x0002á\x0002Pø»4¢dZ¦\x0017%êR×wâEËMG\x0016ÝÄ\x0019õkô´gYý\x0008=ÌôüP@\x0015ÎÞ:{\x0003Ø`®}×Íâ$Î\x0007Ø@¡P¨úVÞW
¸ú\x0008\x0003\x0013ã ÷-l5$½w"$ GÔf'SÍ\x0017éùeº1¤K\x00012âµÕeFÃÁ1VQbÄÜëvÊxI\x0015t¬\x001aÊZGJ]|XSq¬ÖR¢ÀÌôÓ©ÙÑÖ¹\x0002)iG'và¢Üé!·B¢H\x000e ¤¤)\x00039àBÅ	ZM:\x000bé§Òèü
¯P:§«ae\x0014gÕ5Ûå÷WþI'UV´¼ò³)!=¾}Q(JZSC\x0006½»ª`PañpéÇ\x0014\x0011oi¾\x001dÑPê\x0017~m$§±\x001d²\x000e<¾jQV2â\x0013ofÄä\x0015Ú7Â¦Ïó\x0018\x000c3ºo½Ä¨þp};=¼Kw¤{Tºûm\x0019\x0012\x001f\R\x001fæ£Jz6Vð\x0014\x000eûö=9¿ýt\x0013ÿ¦¿`@\x0004Îã\x0019niô\x0016E¥.?¯Z0ååî}­¼q[ÊË4ãV\x0004bô#<
/jýâ?ç!=*gè\x001b9	WûÇÁåÛH+nÀ\x0011q5òÊ¬%¸ø&÷\x0018¸d\x0005q}¾F#nNZE\ÈòÈ\x001b\x001eez%¾¾§F`#\x0003%\x0001{ÛÊ%`K\x0015¶Ý$jL§V`\x0008)\x0001\x0004QBÂd`ïØ>\x0004;\x0012Øýåçü\x0000ÓGÑi··§ï¯Þýåi\x0016±\x0015ÍÈ¨Ú§ó\x001a\x0006A\x000e\x0014(+ÑByç'Ñ >÷M|çÃo÷?[\x0012:w±hÐ.=þD+a³»Éy2ßÿ¡ÜÿÁ U{ú¯^½~Æ]t3\x000eMîaYÚ)ægY\x001d¦å(\x001b\x001enÞ"Ñ\x0001Ì.Ñ8Lëq\x001d³éÊã@üÃR¢|ð\x0002¾\x0014\x000fÄßÆ\x000eÌâÃ`¥\x0012hÂÔ1Ñu\x001b¦0t`tl¥É\x0014tÂ4\x0003^(c4RbBIúiÄ\x0004¬ôcNÈIk(±Ä!)\x00007`6úY\x0006§I\x000b/)àMíÓ³«¿®Y'\x0001RshR(B§<m!ìõ$ý×¸\x001dÆAôìä\x0016iÇ\x0001(-:8ã\x0006wdâ?_\x0002\x001c'ç¨±\x001cúo\x0004*£Æ-¤)ó@;ÃoÒÊ;?\x0014/úÍ &ð]@ÄmOñ\x0008ç9a\x0017R
êfPýóÝÇ0I°Üq¦\x001a Û_¾_¹µDWÄî·
hJ­òYFÒ`|ãéê.^<=t@çt·vh,ø¦òì'M©Å4hv)ò(Ð~cú¨½Ï/Ò§6µù.£\x000cU³ê¬\x001eúÁý aØc.Ô¸>\x0004Oµ6°\x0005:~Doº ¥fo¦>¡æ©N³CÍ\x001d:¨±;T¾<\x001aëË\x0002ñZ¤(ÇcPæS\x001d­²¢É¶oeåR\x0016R\x001bÇ¡.\x001d=zdU\x0003cT*ÃÉ\x000eôB <jï<\x0012v	'ö`{*ÜKõ\x00049\x0013\x0006W6Q»á6$|üáï7ÜßéYxúñãÕÝ§µ\x001b²:ebñ´(÷\x0017LDÍA\x001c\x0019]u\x000c3\\x001d=ý×ÿþts}ø,<}ýúäòÍák\x0019â³²]¨^ÑÉ\x0012PÐ6¹k\x0006¾\x0014Æb\x0011þ£4^Î(k^BnÅj=£¦V&Qþùæû»OÉ\x0003ÞëÇºçÜÞý¸~A·\x0014\x0018Eû@õqÉ\x001aª\x0006ÂµE°±ÎÅåónÑ[\x0011µ3ûpc
Fû,y\x0012=%
\x000bï]sL¡\x00169Î\x000edì2o<Y\x0006sLÐ\x0001ed÷XÀ¦{æ8Ø².@C:0¯j´d+Äðý÷S¿&óÉ\x0013¿âüú¯7W«6Þ¤÷ñª_I°ÿ2àÄé÷«Ûíüô³U<¹jhÅó\x001cÈõq.#<EÙ
¢ÃÌ\x001fÛ:yÎQÉ¬Â x\x0000\x0000áéu«ZG~'\x001bé¢_Nâ\\x0011bÆ\x0007Êg\x0012ßã\x0007áÅ¿\x0011þ£
\x000fØuA\x0007\x001eï\x0012tCCáuC_'Ó-R4N\x001fv&Ìs4Óé
óùAko×\x0002¼Ï°:\x000b:Ë[D>J
ù&ÞO÷ËÏÒý\x00023+¯¯n¢Õúúöãõ¯?­=l\x0008*îÁ°»Êå[Æ
Iñx}SM\x000f\x001b¯OÎ^¾9úúâõé«¯V¹÷\x000fö&nMú¤Ñ(*J!Fn6â n,MÜX¹¢û¸!dÙ­¤Ãõ@#vq¢súÝ#QSBS\x000fµ³¬z\x0014ÿ\x0014h£y\x0005<ÙmQ
ì\x001f®Â¯Y\x0016øÁÝu~\x0014?zuuw½\x0006aÎµø¢8B\x001fújái|rWIoãG¯N.O\x000f%C\ýø\x0017øÇýg_È³\x0002þ/¬y&\x0000Jf"N¾`5\x0008
3Kk|ë×\x0017o±ZðK²Výñ}°ø@¥\x001aRÙ\x0013Â:ÐàEaÝþÖÀþíÝ\x000fð!\x0019º¸;Ôú&¢^ß¿_¿µ¢5\x0014ÿèé¬5,ÜÆU°o"êéÛó
X,Ñ}°Ò^\x0011ÖS\x0015\x0016gÖÁúÙÑ\x0006ûkõÌ\x0016\x001f+\x0018ªâG\x000f½\x0018\x000cÅª-ß	\x000b$`-yÓd\x0010vÈ2\x0010ÿøpûÔx\x0019-º?à¿¹»¿^{fò^f!T¬i-G2pm:êðWX®·ØpéôÐ+Ó\x0012³áL;%>-R9D´\x0006Ù\x0004à1ÁöÕ»l¸vJ*ãi¦yïGJ«³L«I¸Ti\x001a,£|!UEi9\x001bNYAñ5-à\x0012a±ß\x000c1\x001aPíÁ¥µ.$ÞlJ©u²ù£(÷oUÕSÛW¥rkGo¡Tê^5q?ÔS»Á¼qªÃUü¢¨¨½\x00112.Ô	´2b½ÄôÓ
i\x0004eä\x0002%\x0014áD]
½RýÅéÛE5×ñ\x001f¯"bü»¥d×ýß»¬´¿lÕ}ÎoV]BÖB«N!\x0012\x0005ê°#'Ï\x0013å·Äö§xëÅt`BA'Ì\m0\x0015ª±q\x0003ÒÁ)É	\x0015¾D4½!Çk¿?\x001c5iÇä[`;¦¦d&ÎCjñâtúÃG;'kStpªcò<Á\x001d{\x0004)ÍÂ\x001bD-%Üüxu÷}¤\x000cø&~vØòîÇx-K#zõ§§×\x001f?þëk/>i\x001d8\x001bt®·~\x001då<Äã\x0008MÔw'Íytrùüô%6¯H\x000f=OO£%8ôÒÃô2­ÿü»\x001d_³ t\x0001E~i\x0008Y;Ç\x0005gRë\x0001ü¿þæþþ³I\x0016\x000cíìNt2e\x0014}Z©\x0013íCª$Mñèí*sT@\x0017AqØ)6s°\x0014zÈ\x0017¾6Ä\x0003	£P[ôð%'k$gt\x000c õ\x001b\x0001±\x0012Ó\x0005BÉ×ÖßzÀ\x001c¶­Ñ)C?T43*àk
,Ê`\x0005I%Éè÷
DÄ¥SíÓhsÖôX:,-M£!%n\x0001î°µjfÄÝÒó©ÿ}ñHÆCó§Æ\x001c|C±i­I4Éî:C\x0008g\x000e»$Í\x0018ÿ\x0005ÓÌèTZQ/\x001f
$õ"#\x00069\x00071ânQí[\x0006ûR@,\x0002qÂUÜ)Hô0Ë\x0003®~\x001a\x0019-P¿Èè¨Áà}\x001f6[Çþò·¿ÀÇijÒ\x0001Éí%gÞ\x0018âÅ\x000e%\x001e\x0015ã\x001au®\x0014Ø\x0019X(M­VÝÐîj©{p±¿\x000eáÆ«¦Ë¹ê\x000e\Á\x000b\x0006\øùöÏ7Ø±\x0004ð;¥÷Q\x001aw/QkßÊruÎ4ÑBìe¹¤\x000b1q;\x000e·ðbú¿r] \x001dª-UP\x000bÉÊð\x0011²jF+!ÑûN?íÞåÄ.\©¤´°\ù\x000bÚ-TÝ5¢@úi\x0007u2¹kø¾­JH@{Ñ¥bÐvNâ\x000cÐ9¡Ê5ëÏi@XÙ´Sâ&
]È\s§R¦Zþæ¢L¥XÚ´Sâ\x000e
];(®HxGè±gP_U§Ü
ªÑÈ¥fP\x0006+\x0015r\x001a££5æB\x0005|,\x001dÇw
mº8MÊwCLKê\x0018dâæyÑ \x000f´JØÁò8
>·'APÌp\x0014\x0017\î³\x0014\x000ckæÄ7ÏôÓÎi=kÄS%(â}¥¨»pw;(f
ù\x001e«&d	°¯\x0006¿qpïIð0Ð|¦öâé§\x00194 \x001ey¢ôI-Ã±ý\\x0012%jÇÄ\x000bz×GÁ\x000cA)^\x001cI\x0013ìJ¨\x001bhB
êo¤vP\x000b¼ÒW¹£gü;YU>üÒãV+häJ?í !°ömÜçÉ{ÆÒz\x0008¬ï\x0004jàZ,ÉJ?\x001d =&5¤\x0001\x0000\G¥GÚ&L|~\x001a9=fÎ\x0017¹!ái'A©£ÒØci\x001c'Öõ¦vN¡Ê;W¼w\x0006OÚ\x0014ELÑ \x0006'ÔtMhÜ?üN
á4£åm3ÎèÀS\x001e;\x0005>I?í ØÜ^%]=´â¶?\x001a\x0005Ã·bkøñ}J
\x000e\x0018\x0005ß\x000fþøþæãºàGDz+\x0004*ËOýík@\x001dhs?#U\x0018¯ï#M7¸\x0004Êe$\x0011´¨#¥GífÐ^N\x0007)x®Æo¯ID\x0015M4[é0×â¸ÓO\x0007iÜëÎïViØ·O®Ö>U¢bB~`ðëPeê{¨ \x001fQ\x001cZå¾¯#Åpeúé EiTÁºN¨~^&µÒÍ«Cu)K¤\x00035\x001e£^±.Ztïr\x0007ªvr¿zè¬¢=*¢:ªÙÃYUTÜ¢A°Ò8vV\x001c»êáµ¾nV
)":ON[{µ«dÄ/ÿðR_Å\x0018B\x0011Ì2/§bTF\¤
hÕwÚ:Ôhîiã\x0007\x001c(\x0005'ð	e@V\x001e¥u¤X~ÚI=¶e;)Ê\x001fá£tQ*­\x00194e|§\x000ePSD\x0008°­{RRøDº{ÕAÁ'ÑµN½\x0015)DB"\x001c-±,ì®~ÿ8T\¢Ð·N½Î%<©­<«#w?¨ÒÖáK!ªd]\þP¹?G<¢Æ¢jDíÛSÑØ;6T]\x0014lôÉ\x000b@´û\x001eé§\x0003Uí\x0016@ôVÈEØÕljíÝ¤\x0012\x0015\x0017ÀÃD\x001dªâÐ³Þµ¬\x0011·ÕHo:\x0015L¤\x001eTÍWSÔp¦«©Ä¾©\x0014X\x0012¤oGÅ§ôÓ*r\x001cãý2p´\x0014v\x0017\x0018yRÅ÷\x0011û ÎSKj\x0018US\x0006aD5å\x001a]\x001b¬DÅ·1ûàÂ_*\\x0011 ÅTU\x001eaÔ%ÿvTL"\x0001×µ«\ ?E(RgÐ\\x00177¿\x001c&õa\¿\x000eS§Ê·DjI*IxYHkg¤I»­ïô\x0017Pâ^rÄ\\x0004YÔ¥k\x0003§¨¸L]×2uÃ\x0013õ(ãrh_Ã&i;(<xøZRûõù=/ú«e\x0016éÚ×Ñ:RTFK?\x001d¤Î\x0015½\Ç¢Ýe|^ªek\x0006MV$ýôR#T\x0017'\x0013e5]\x0014Aï@Å7=Ñ·÷]NÄK¨¬f\x0011Qùm\ç"âa¨\x0012eÒd×iê¬eyì8¿\x0014ð\x0011ßsµªM¨$Eá\Ùe¦SÇÞw,¤d½Ü\x0005QåÐà\x0014Þ(¤I¥KD-/<BóÛCÝiI;úaæNÝ¬R\x0019\x0016³ÊÔñ0Í*·9ÔbhhZ£\x000cQúé@5E\x0012%hêÈ\x0018É./F\x000eU¼ó¦\x001eTÅq4Tð§&±{ 
Âa¨h« ÏVÅYeTÇÍt
'\x0010êRKvÔ¤\x0007¢»üiÌ\x000b¬å/s¯zL5ã÷H\x0008cÍj*n×\x000f\x001eÍ«PÁpDEÚ,Í¨¢\x000f\x0005Å\x0010ºî£ãÊâø\x0003ë]Ls\x000c\x001bê\x0000àMJ÷]§\x001c@îfóâ\x001c\x001d\x0000XÂH¨C]jÌ·{¢}×u\x001a[NQà\x0017³e\x001cuôâ0:ø¥B¼\x000eR<ª\x001e&EÖ"f $ªøÑÙ¨z9Ò\x00010x ÎSU*.ÀÄ\x0004à\x0008U\x0019?ò:mÐóM?=¨>+¥#*÷óÀcl©Ä~¯üEüýÝTÆIwJ¬Ë¯hRùÒÐ\x0019\x000e¦\x0018.\x0012BG%íþ\x0003Ê®\x000cúúèËo_¿>(Vµ\x0003eåÎfP!²°+~ÏwTm*v®f\x001a\x0006ºSrn&ÅÄCØ'E1gÞP¹¹Ç8R¬\x000c\x0017¡Ôr¯Ôdú5B*`(inè";H52áiª8;Ö(îÑ¬\tî E}\x0005	\x001d¤6'ïÒÍ@MÉJ¹uß8ÐýZjP¯²e¾¢ð2µ¡$\x001cûÁ\x001f\x001fÛsO\x0013%ë·¾)S*\x0005¿øhVQ`ìP\x001b,YµÝº,ÂûúpöLðìKY3vbV\x000e#m\x0004¹U[tO³'eU©Ù\x0008nIÐ»\x0003\x0014ðÁwL)\x0008Nãö\x001aÏÆ\x0019
E\x0017_5¦(¡Ãª¸ñ)ÉGúâZWÞ%eî<\x0014\x000ff©;©\x0012Òeè©ÒQLDüÆÚ(¼ìIÝcL1ºKCä\x0003ÊG)=Øì?Hòª&¥ÇÓ´\\x0003\x0019}Î\x0000'Ç\x001a(|7¶Ç@\x0019Çm±ôÚòÏöÒ»Æb½°U=\x0007~à \x0008c}Fi¾êQ\x0007ça¤\x000fÒ»êwç\x001a=Ìâ'R+v§\x00135¥øp"]Â}îÞç³¢®¶\x001c=\x0005\x0013Æ.R|7¾Ç>ý9qú5ê\x0002g  8\x001ci¬,zÌHP.¾êñóã±>-Ý!ï9^ØÕ³jè*tU÷¬°
>½Ð\x001c¶¡TÁi\x0018z*ôUû\x000c\x0011çT\x000bÎsJr(3öëãÀ\x0015t,SÌã¥ú\x001da=§öD_©\x001c<§Ì~IàW\x0013á¹´Ð:Ë\x001f±mO;'\x001e ªç\x0014MY»\x000e]T÷jLTpCQ\x0010×#:V)êIjdáXÑ*Åú<¥Â\x000c&ÝÏA¬ÞO²ì'á\x000cWH8(f_\x000e&Åné§}ç\Ë!C\x0008&Ú\x0014(\x001eáGbâ	
å	ãIÅÜ¾<ë(+n{Àï\x0003¦cÛk[!\x0003¥4wäö+`µ#6¾½GÊß0\x0006é\x0007ÓW½WWwW¿®6?wâ"ÿGÞéqt=JH9â7>zvw{\x0011µ~O^\x001dl}¼CdMÊ\x000eFÎû=?æDF`FjmÆ0b$KvÆx\x0007¡Ü\x0008å\x001d=âE/SMM~È\x001aÃëÑt0ºòÒ\x0004Ñ©wÄh,]?Å¬A,\x0001×È
M¹¦,ëzÕE×3¿\x0006
\x0002ÄGÙ\x000e(S  úñYl\x0016¬à²'ãÄ¸\x000f/³WÅZFÏ¯_\x0000Ä³ÀJ\x000eÖ\x001b?òCï=ÒÔ2*ÉO\x001f¸w,Í£d÷ÝqÜÑ¡y-\x0016õxÀß\x001e#gf\x00183Î6îÚ:t@ªì\x000c2Ô \x0005!ù[»´È\x0007Ar\x0003²fÈÀÚ/ 8s\x000c¬QP }m.¥\x0014\x001d+\x0012\x001c\x0007#$[\x001fà¿&\x00156\x000cÄ\x0012{©:fÒ¨Tp¶6g`b\x0004Þ­­ABìY\x001f¶Pø>\x0017Zãd\x001b\x0019`\x001d\x0018Ðñ¹MI\x0011\x0003\x001dHX\x0001vñ¸¹a\x0018$\x001aHÙc%µ+&\x0008xãpÄ0uð\x001b\x0006îm÷ÏP=|\x001f\x00082¶â×æú\x000bã,Â}­z6÷.Ë.õ\x0015¡ãÆêÂ8lÛ(t\x0000èÇÈH\x001dÇ\x0001k@43ÒÞ¶9\x0019r\x0010ä~Ü­\x0001.ßZD/2òÇÖãÎD9Zé§Ùÿ1ü\x0016¤5$e¼ä[Ú±²\x001eí\x001aV"ý´zã>p]ãÁ­ùæÅ_;åýüLÖw\x001dd<Wx&M4E&\x001f7^±%wN\x000c»z\x0019\x0011¯\x000bé§\x0015rWb\x000cÇÀë\x001dä@F\x0014ò\x0011í÷ìxäq÷\x0007á\x0018ùyÒ¹q{\x001b\x001bµ<1=_;BBùØ¹
2Ò£³aëDþõÇ¿Ú¿ûï&\x001f~è«ëßVð¥Ï±&<hÁ
\x0015â^_s+Þ\x001e½:ýv
]ÛSÅ\x0016	ÈvÇÿ\x0000UE\x000f³´\x0019ÄFa¢ VÅF/x$$DWVÐ¥¶Ð!l\x000f²Ëjà¤Ë?z
§»*RNìSòv8|
ªí«bÝ	G#\x000bb×Âc\x000c\x001bFl¥\x0011Í\x0013\x0017¨\x0012/îF\x0010Ùø3°zÉ¯CÏ(ý4Á©R$î
õE\x0000¾í¡^á\x0008²Úâ\x0015d6¤|
0IvûKKé\x0008·z\x0015­Û{Ñ®3}\x0002\x0015\x00049Wj×ÅØ5\x0003\Ç¹ªÒ·NKùt:7¡½ \x0002§Y¤'â~8ñç_~¹M²ÍhæEWG¯Þ_Ý|Xëb ¤M?t{nÍn°`9\x0011b\x0013ÎUqé$üêüäìå¡ôä\x0002úM=©Èv\x0005Û]&,q¹×ªZh\x0007WMzó÷RüôÝ¤±V\x0006}uûáÓÑó«_n?\Z\x0001ÕÊfÙIéuðÇ$)®©~Zx£ª:\x0016gäW\x0017/ß\x001c=?yqñòôÍ*2·3jG\x0006½\x0004lÓ))eÍ
Ã-SãÇ@èºÊÿÚÂ,uÖTÌ(õG\x0012øBOÂÕu²î`ÞË´mgÅ-eµ dË¸4¼'dkªºV3û\x000f?ÉûÓK\x0017î»ù®{}õãú¦³Û^\x0004É\x001fÛ/ÖG¢nÓ½>y~pÏí(¹Ct;fÈ\x000fØ\x0003Gs«^ï;\x001f\x0019YgÅ*1±\x001cÈt`N\x001a4).[4Þpã#½Ð\x001c°\x0012KÁ\\x000f¥*Ý®\x0014Pt<RÊB¹ÚF¤\x0012\x000bB\x0007¥\x000eÇ)\x0003w\x0007\x0017Xþäzä\â¾4¶\x0012»¸©¤\x0006gñÆh¹+¨YíÑ\x0000þ¦Õ\x001dS\x0019rgfnZI\x0002¸\x001bqw`Æ1Û¹Äì\x0000úâÖRÈÂ\x0004É¦Èù{\x001c_M}Ïº´>ë'a]EÑg|a "Ê/ôãjÇÄ\x0014ÈÐcØ\x001dä$bZn\x001eîÙm{5Sîú7czÉ­ââµ2Ë\x000ex\x0014ñÊ\x000cbà\x0006Úµ1lßA9\x0018jíB¤U&÷¨\x0005\x0011\x0006~ôÏi¥Ööâ\x0006/Ê|îzéÆ¿\x001d\x0018ÛP=GV¹|\x0006¿{N\x0007KÆ]Mä\x0007AØ\x000câïÎñèøÝ;,§&û\x000e©Ý0NÔ´I?íFIäºÈUÞÜCL'd\x0011çQ\x000f\x001fîª1]ÎoÆ\x001fMró+öÖ0Jô¤ã2[øH©(6~ôÀ³iìÀM¤r;Ð\x001eÛ\x0019bë2§w@\x0010M¼âéÌå§£8qÿ¨®Mùid<\x0003i¶Ç¯n\x00183K9ÂÄ\x001c0eº\x001cNJb\x0001»\x001fP¤¤¸Å:ùÛÃ0ñùWÙ­õ»0]¹
inV«ÅBwÕvÎ/yµØL"N)÷º"]\x001c¼Ý\x000fô9\x0015&x(×³8Ág©¡\x0019¯\x0019|eÓ\x0014Án»¿w¿w7)èFij^_Ý|øô§gï¯îXwéBÎóÞ£çýNS*«Ò×'g/ß\x001c=;?yûÅ:n<@Xßí_¹õ\x0008Åg\x0002êË\x0013\x0017­ðçpã}â{q¥É=E0Pj¨¢×fR®÷ÿl£}XyÞ«-ßéÍ¢ãk)-TbÃÒÁ¼\x000f;x£gJ&\x0017-X OÊ~5¡6Ü\x00072þ-¸\x0000YÕ#â*Ö1âjnmij\x001cª&ÜýçÆÙ5ùi)âFc+x5\x0004æÕ5gl\x001b/úþÞuòzq±­¥bo+\x00040/Ô¼J´ðªT
0»¢¶ðb\x0003è<¿ÖïCyÀJëÁ¼(¬tïzp¤F\x001fy!Pnä¥¬vÿ!¼êÏêýï>\x001b|}}ww}ôüæý÷×w«qsÌË÷VCn\x0018®\x0007KmZÇ^ÕsD?½¼<=z~vþôôòPð¼°+\x000c	¨Y\ \x0005\x001e{X%ò¸	}rÂ1c[3yhx
j&PÙFÚ\x0010\x0004\x001f­\¸Yé(¹.Þ*ÄcN;\x001ag5·Ð-ðT×ðÑ\x0011ÎO\x0017¶\x0008\x000bì4þðÐØ¿à±üÕ\x0011<PêEçáÍ#²£ã¥lïÄkgrç\x0018Ü¬ª\x0014lôxÉûÐðÊÕ\x000c¿ß	ºuÕdáÃ´_\x0005 áªá§Ð`\x001fsæñÀT¾{Õ8Ó
"<6i\x000c\x0019\x001eËÑ²Yð3}¦Ô¬ÙT\x0013|<èm~Ã3q\x001c@K^3ºmxnE\x0007<øAô£w=\x00137®¥y\x0007v\x0015\x001e\x001dÍ;tÛxmÃ1­w\x000f?\x001d\x000cOA%Oö±Ø±j\x0010f¥mì¹³kôb){UÄ\x0008©\x000fë£±£	ØÞ5c@°K\x0013{×Xn\x0008\x0011ç=½_>\x001a;Öw[x4ôÜn¤°7ÊñÄÛÇô\x000b\x0000ó|Àö\x001aItj\x0004Ý-P'dZ"|K²K+¼N~p·_`°r-[\x001aë$¯\x001a%(m[¦+ÒãÁ?Tm·$Úðê¦ã7 ;\x0019á\x001fÑÔ|¦t\x001b»Nm{Ý8zìW\x000f	ÿ°[s\x0013¼\x0017\x0014º×SGÁ\x0015¼hâ³^ú#Á¦o\x000b¼ÅK\x0008ÁKOÏ\x0018\x0016\x0004\x0015\x0007ÝóLèu'­uÇ´jJÇd\x0005+Ä\x000ey\x0007ùL¿ß6öP\x001a\x0000¼]ãgØPêGøÏô¬m7\x0003t¶Ù[Ðª\x00048\x001e\x0011\x001ds0­ëÝ­\x0016ë\x0017=\x0005¿øÞ²*Ì5ÅîR\x000ei7»£T,òjl6\x001aLqãÝ#N|*ZÊK]ðRÓCdg5ø¯ØÐdá±ìïÿøËÝß>½õÍÕû÷·÷ë
Ó\x0016¥\x001bdh8«\x0010\x0002°§²¾¦iÏ7'çç\x0017o\x000fKLOH÷\x0013¸êI|\x0012)ïÅë-¤5bèÕ¤Iè©FM{P-½ç®=Ê©V\x0008õ¤\x000fSPjIM\x0008\\x000c$vÅ@ØRPsÂÙ8T¼TI×ê\x0005Å\x0013CK!j¸P$lU\x0013´jÒÏÄô«IÈ¥Ï\x0014s
ó¤º"ä©ôØúµ¨:^bòq\x00110§ËÝYuRÙÕú\x0016N\x000c ¥vNY^Òs)w\x0017kw\x0003\x00143¥×kwëA5N¨îPQ\x0012=\x0010ÜÎµ\x0002¶&NPÝ5¡b·¤,_Þ¬×ç×>\x000cwÔ\x0007ªÔ\x0008)%6×R\x001a\x001d\x0000X¶¨\x0007Å¦à{¾<ìÒäp×;\x0002-ú:ÊØ \x0006·»éÚóØçz\x001fF3Gnñ\x001eÍ_>ÜJ&%¿%-IABÄ?:ª·Ô\Õ\x0008"\x000c\¢)p~A±ö\x0015\M`±\x001då¹é%è
õ§zPÌ
µS\x0011ôzP\x0003©2Ô\x00115U\x0014²&GnO:
\x0013Ó
ì,ç \x001a3^\x0018Y\x000bYpkÞx¾±\x001fø;)Õ'¤vPÌ=£\x001ati\x000bh½Ðbµ\y\x001dô\x001fïôßÿþã¬ªà>Q¿ï7¢¡ôfQW§³¢ô\x001ff|\x0008/Ï¾<zvyqH\x0011±\x0000NäÚ\x0008Á\x0016B|«'×Î¨2\x000bR~Xî~Ú\x0010uÜ×v'v¯X\x0004ª4V\x0015wZ	1÷%iº´\x0011îz¯Çÿ6k6Z\x0013x\x0012ôÝÚ\x0010UlTÍ+Q[Ç¢d(àXÊ¦èð;qØ\x00005"F§öIúiDÔ6{\x001bYù\w«þ\x0012£>4`ájúiE,ªiÑ=§ÒÕÈVÜ¨\x0005aVÄò²Ù¨R³JD4¾h?iî³cäøS+":léÞh¸_2.å%Ä"\x001f*Í¨µ\x0008¸ñÒO#"8î«%\x0018<@i\x001c\x0011ÑÅ"¸Ü¨\x0014ë^*ÈMÊî\x0013#ê Ç!zDlßÑÓIµÃ¦$°\x001c¸\x0019·[P!ý4\x0012F/\x001aÒâ$z\x00168-}³\x0017D\x001a	q¬é§\x0010ÅÑx³(Ë¢TÆÏ¼ \x0012ÛJXÞô	'\x000b<1¬è-\x000bq\x0018"\x001aôÓè<K+P¬\x001bj\x000cëØê°\x0010\x001ahDDó\x0005öÚ\x0010±N?#6µ6¬##Çm]Sô6DÔ\x001b£ÍBM\x0007\x0011Q\x0015Ù§ \x000eKÝ4"âõ2ý4"\x0002\x001eÍ¢£µ(u9Z\x0016©Z\x0011ñh	ÍG\x000b @:mx\x0010æý¬C9Å°
­ñF~\x001a	¥`5÷x/åvÍ¶XÐálE´Ø>èÃÒJ4|öiËM\x00114\x0016"Äô\x0003Ù|ö¥î"¤ ¤r\x0012tB\x0004Ö!ó£¶sü_ÀÖáÍÎ,å³§(9\ªmésèÍ(w[cÒúi$\x0004UôÑ%w¶{r­"¢\x001cXú¯7"c\x0016tÓåt\x0016Üz7na\x000bq× ¼ñ3"¥Pô]i¼é\x0017\x001a
4"îºm7!*|	£ITl´µ±ån:ÎÞ î\úi$ô),ÎÌ§s¼k±p[x¬iCLN±i_èa\x0007n­­ùV\x0015m+o\x0016)GY\x001cç|úiD\x0004YbvÆR$':>ìÊÂ°h°H.ý´Nb(ÝõDzÃ9Ü5Õô\x000b\x000f\x001e­Ø×\x0002½mÔÞäVª
Jcéa\x0012/ú£.Ï\x0006[S¦FÄèyQ¬	C³ôÆQ<è3²Ú\x000cµ6Baùè%ß\x001eâR,âª\x000bï0­¸W:l"Ê=¨\x0012:\x0006Bt¾\x0004f]ï
¶.I?ñ\x0012 ¸)*R«¶\ÅHb#"Ö¾§ÖYTl·Sí¿ãYäd~ÅÁ¿Súiµ}\x001c\x0019WeV'X:ûùQ\x000eÄä­Pz]:w+ÉJí©ï\x0018}æ\x0005ñ*D4¶ßå\x000e0»¿zÁ<ûéú\x000f\x0008ûô_ÿ¼zôâönUØ9	9ÑÓeàH·fYQH2
Ó¿Û\x000cøÙW§/Î^"óÓÓó£\x0017\x0017\x0007åÚù)5ª
tQ{ÍºÅñÂ@\x0019§ñè)­óR:ÔHn/¦ÜøZØÅ\x001d$ß¸£kDÀeW8Ýj0¶a«^lÃ}¾\x0011r0´µJ¢k6ÁÆW°¾U"±©7}\$±Sî¡Øníz±ei
\x0008%+K+nj\x0006*:Ò¸ ÙÌÝ_xòÙ~y}ÿç\x0015j/ò¢&·Ý\x0014¡<1»| l\x000fúåéÛ/W2«ÏÌu\x0005´w)IOT\x0010Èh,Wæë^HkÖ0Ö±Ù5Ð¨SM3mt6ª¼eLØ\x000eh;¶3íù(kvä.q¼¡È~6Ï¾sAq{Ö¸\x0010ÈcÓbw§Pý8èè+L 1Ûµ8~)'ÉTG÷·tòf!¥·\x0019\x001aÏÙ©é\x0010ÔÑäQY\x000cVZZÒ%ÉÏ ®ô@ê¸U¦ÔøÓC-eÑdwYÊ\x000f\x0013½}¡n¤õÀ)5ô\x0019j\x001bçûQ\x001aÏ\x0002üAï\x0002Öv$ôÜzÈ^ó!}
\Ä¼¥©fé¸@ÄÈÓEù²6½Qð)`É§ÍÈo@Æ]Öq\x0005Î¨Mç\x0002±üÍ
yYÇÿ\x000eQ\x001b±ÀÞAíæÔ}G9.kÉ&Äpp9hÍÙ&Yüg\x001cõÜ>\x0013b\x001d\x0015\"5<\x0018\x0014éäHm\x0010;kÛ9×Áæ\x0012WìtjS\x0005	R[Ã\x000fKÿ\x0006R\x00075£\x000e¹ÆTÙ\x0010à \x0011
[QÄÀú Ê8ÌR\x001eF­Rã¿ìóB|®Æn¨ù>6DòëñväºF
Î\x0019uç\G\x0002¯\x000fôt \x0003?\x0001 jýHj=kÝ9×¤È¨ù@×Â*ý8ÔóSFu2R\x0014\x0013µÎ×\-EéEë\x001e2f¾¬Mç²¶¡4"6q_æ@H(¡F\x0007Kå\-Ð6ùÖr7Ó\x0016½)ó«ëßînïïVÚZ`¨Lsð\x0011Oi	éÍÈ\x0006«Cõ;âW§ß^^¼½<ØÌ'+:\x0012Ï\x0017t-1H(ãõÒè5@(¬\x001fGläØÈ®9\x000e"\x0005<ÒZö$[\x0001:þ&¶òðM\x0007±\x0011«>âÀ!=Ð%®¯-÷aEýÁqÄ>L}è[\x0015îm©ùÞ\x0011wþ`zW;p)p.à¸Û¨ù©ã¶=ñ,ä¬{«F®â0³\x0014¡ËRü)\x000f%=#Æ\x001f~Ié 63bÓE¬CJô£EA½Ïâ^áVÚ/+-Ä>ÇîvÄ\x001eÏ½\x001dñ=¾³¬°b£kzb£Ñ\x0016x\x0001+8Yßâ+Ë
¥sSJç\x001a)¡ÜýâqÁ«ÖJjäÑçÕ5PAÝ§s)Z1££Æõ"qÕznÈ]JZÔá'µ*L¡\:ËqÛø¯ýòëÕÇ×GÏ~ºúåW\«_^Åºjm\x0015Ïª,±OH/Ð«¸g/^¼~}zôì«\x0017¯p¹~y\x0012×ê
·Sn,éâ]£MÂ:À9x\x0012\x0003Ë5º¸Íl¾Mï|Êjié93pãW]rÊ\x0016ÞÕ»°Ýlº]÷tÇµa\x0008[\x0006îæ#s\x0010ôÁ3®ÛÎ¸m÷2òz\:¬ÄeâøéÇ
YÞðÝ½ÿËûæ»IË´{Öç¿'_>\x001e\x001b¬\x001d/23<IþøÝ²
ï««\x000fïî®Þ]'a\x0011ëuV~Õñ´7ÕT\x001e`ãM;äIw&E,|sv~~rù§$«û§W'/]<;å·ïó\x0013|ú>ûÏäÛÇ$ÉÉß|xwûáÃýuùÃÃA \x0004ÂA8\x000eBçP:\x000eÂP\x0015·3©IÖã\x000c\x0002Óõ\x0007
"´hÔ%}	Îøuq#èÇ\x001a\x0004æ]\x000e\x001aK	\x001eéK¸I pMü\x0012áÑ¾\x0004f§\x0019§®\x001fèVSÝ\x0011\x001cy\x001e~´-ò5ÃÆÀû\x001a¥(
\x0017\x0013\x0017?Î\x0018¢3ãÆ!\x0000I	XE\x000fÕq\x000cZ\x0000Û&óx	Û1\x000c\x0019DPâÆ·
Èc\x0000Ï¦)Å\x001f\x001eg\x000cØxwÌ\x0018¤L±y\x001cée¤ÑïlÒAÈÔuÌ(\x0004í-f8ç]­¥ãÕ\x001a\x001e?Î ð¸\x001er^;LåÉ>©\x0005o³`\x0005ÃíDK}£\x001eg\x0014ÜuxÀ(\x001cgËà¥%ÍÆQXM1.'öc\x0002{k\x000c9'\x000câ­\x0001Ò®_EP¢²óé\x001dèqFÁÍx\x0006l\x000bçr/.\Q9¾+J²óä\x0014fÕ?Î(P`ÈYñßº¢°3ü\x0010Cë´\x0014t£pØD\x0016£$VKº(Çe\x001fË\x0005ÄK²\x001ac¢4$òi\x0011]%ò\x0001µ4¤¦å\x0005Ç2´¹!ÝÍ­==\x001cØ¸³\x0005·[Pé	ïqF==øã\x000e«4Y(H©ìh¡$½E\x000b¥\x001eëàÆtG5ÄB¹$D?\x0016
ò§ðÁÒç=>.?Î(Pèc#è\x0000$7lüG®È°\x0010<ÅS8÷±F*t\x000b\x0005IÐdÌ \x0004Ð®°^çxR°\x000bîÑÜY@É1\x0006JøºO¡\x0012Y´\x0005O<Þ\x0014q½=Ö\x0007I¿pÌðòÚ,öËîl\x0012¹å³âñÖ\x0013ö\x0019\x0018ã\x0008þ÷m
!¿ûþæ#\x0006\x0003ñFÜ¹M Ê6+M®MN¡4ÊÅxà£ù´ðÝ§ë»tÇÀþ;üaF}h ?¨¦íN^z &4q»½öÙ_ÿòó/\x001fÒH<vË{òä¿n?Ä1ü¿ÿù¿NÞ}ºùëMiUúæöþ®vuÅÉ§â\x000eRây\x0010RP\x0018\x0001E\x000f\x000eâ¿.^ÆQ\x001c<{söÍYi]úæâíåÁ1|øõ¾×\x000fâå\x001f¾¾ºûáæÃÇZjÐRM\x0010"ç±Z®¦óbÝ}}ôõÉå\x0017g/_\x001fd½\x0016×tmÎÓ+Ä¯×ïo®«§\x0017Mh 88\ÃmA\x0001%bÄå®\x000e§WW§çg§OÞ]ýpõñÓÝuù\x0003aÊûßþûu\x0012ø~vûî§ßê'R­\x0008n\x0006Ê	2ñ4Ð
å³g_}[\x0003ãÀm`øöOÑRu©\x000c¦¨X*\x001auwØêUåàn\x0013Â¤M§KN-Z³\x0012O×·L5XØ¶Í³i}%°\x001c@À\x0019ÓP\ÔáëQ-\x0018G9ÚÈâ\x0015!Pô>^\x001c\x0002d2Ë~¶Ñö°Ñ_&\x0013·wîÝ§A9¿:úâö\x001e·hõ\x0001"K{@I¸ ©¤8ú¦áðÄE÷ÅÅ[Ü¡§59Ý\x0001Ýl6xºáX\x0010}KÁ\x000fbD	S©ú 5ßLp¤Ê\x0015)\x001doÚ¸©\x000f´\x0010{(ã±-èðYæ\x0018aInÖWMËòêîÝõ¯\x000b\x0014KëA{9×i`Wc¾_KI2ý\x000eÞYÚ&\x0012\x0013Oñ\x001f],\x001ff1Ç 
m½`	\x001b!)\x0016Ö¹qrâwüÚ!gæàÎáw7ð\x000bÆ§\x0012û1v~p+²\x0001BÇ&Od´:ôµõR¼·\x0011â\x000e]_\x00156¤7X)IW8ÉGØ6JLpÎÏ\x001dtnÅ\x0011)ãñìó\x001d\²\x0014©P··+ é¶Ú\x0001éâüåHìä\x0015J\x0007¼$G­Hlç\x0004}+2\x001aëÜ\x0013	÷á4\x0014É=ì\x001d88ÄWCùé\x001eÔý4cã¼ñæ\x0012m·£\x0018¤ÉéÎy\x0012ù­Ç-Ocº¨\x001c»VÁºäÄÌ:ù\x001cþøþêÃ§{÷\x000blPåP+zÒñjáÂr~ñæìõëÓ\x0017§/ßàÿôóóoðFôû¦t\x001b5¾ÏRÚE0ðxe\x0010¨SyÁHìö²\x0019\x001bø¹#(;QGlCúüq²í`ì|ÁÙB¦f\x001brCÍ}Ö1×uáÐïÁÎ×­Øª¼V\x0006o»Mé\x0014^&ÓÔùn´y²K Ê\x0007ÉnAÄôKö=ÔüÈ½
Û	©yi{È¢\)è¤x¶SÿöÜìgoå\x000e$@j½cÆ¦¼]/aá6ßM/À[±"};\x001en>blðlHÂÈ=ØüZº\x0015ÛBê\x000c È:\x0000\x0016{\x0003ðâ\x000eK>o\x000fw\t\x000f\x001akö¬òN\x0016PHZ&üö [p{¸é]w«1Á´\x0013²Üà)\x001c)@¸S
ùHnzÊÝ:ßBpôÏ\x0007µÒòÒ£\x0011\xÆíâæ\x001bÒÆùöZ"ØèåQÞ±Å\x0008.åuaÓóVl¼AÑtã\x0003:qsf·7ç±Æ»Üö6r[\x0015I~¬¦m©\x001c[ïÔ;l 7¿ÉnoÃùÛèt§
§È­Iû3úfì©ÃÏ°[¹µ#ÍódN\x0002Í·\x0004v\x0004å\x00103]&è³û\x000bO&}>\x001e~üõêÇ\x000f·ï«\x001ffLp¹Q}ü[y
¬)ÁT«\x0017²B¨?Òë£Ó×¯N¿¼8MÌ{ï2\x0005[O±õ6ìè
R\x000e§Ð©J\x0012#ÀÀ
XJ/ÿ\x000c÷¡'¥n¦èf\x001bºÝ½àXk]"»\x0017\x001c<ÒKI,=ða
\x001f6ÁÇË
çkÆïIoÛÊ{ÎÅ`\x0016Rº:à©~à¥Ø6õÂó1\x0014M-ÓÇK3\x0016õÒ>í¢3z¹qîC	r\x0003ã8÷¡ÁÝÂå¾~fgä6CÙ\x0003\x001eD¢¼e]à\x0007àÔÇa$<Ìàa\x001b¼\x00139ÛÉ 6½á$e0K¯×=ì3K)·Jï\7ÿü4¡Wü4¡Â`z;£·èÁ³0ññ¨RôÞÍ-Ç\x001d,½ÞvÑ»\x0019½Û6÷"ø±	Kâ¨Ì½\Jë¡÷3z¿mî\x001dõ\x001eF-\x0015>d\x001dw£tÊ¶³Jn;© ^9²±Ä:®|3UNs\x0015
r¬ f\x0007ÚvP%\x0015\x001e¢7¹Y
æ,\x0004r1·Í1[¥\x001dTjÛA\x0005Ñ­ñùUÙG#)±Ap­jô*Wáçþð¶s
3òÏøÝ9eYÜÐ©Á¬SjÛ9\x0005APöñÑôhÃ)%¼nÔ`ßRÍN*µí¤\x0002iÈ3ôPÄ´ç©W\x000bïü]ô3·^móë±\x000fMöo|\x001cÎ\x0007u­%,dótÁÏYµíU\x0018\x0010ËSï¼¦·¹T3Jôb´Á\x001d³jÛ1ò\x0001&Ï½\x000bÞãÂ!ßRI\x0018\x000c?;eÕ¶SV9êÞ\x0010Þ\x001aªÁ4\x0012Zõ2,eØöÐÏYµñ\x001euãÂ	Y~\x0012§D3ãÜ\x000föp`vÎÂ¶s\x0016ÛvæÆÆÆt\x0006Î½ãTmé\x0007{ö0;gaÛ9°\x0004ï4¥EÅ=«ËÂ\x0019kp`vÌÂ¶c\x0016;²gì°\x0001Ï3¯X4CÁþ\x0019ÌN*ØvRÉ u¦·ÞÑ\x0013*ª¦Å
\x0006¯ÙI\x0005ÛN*l\x001fÓò\x0018xÕ{^õÖ\x000f¦\x001dU°í¨à(mÖØR\x001b\x0019\x0017=Ï½\x0008K¥"=ô³£
¶\x001dU*ÒgPÚÎ:ûÆ\x0006c~yîõà8\x0008ÌÎ*ØvVýûç~vVÁ¶³J&!Ü8÷&ý1Í=;9r±Ø¼^Ï¬½ÞhíÎ\x0004Ö\x0002!FpôOª\x001c.øÙÅDo»È\x0010øVe}öpt.\x0007Ïûü¥a­_\x0004¶;âÄ\x0013'ìèÙz½ÍÖËx<\x0011¼%eß8õ3UeÊ\x001e\x001f	?3õz©\x0017ÒrÌ\x0018ß©È¯G'¦Þ±N\x0019K½ÍX¦\x000eMèuî©\x0019é­¡¹sµPpÖC?3z±Äül°bÜä\x0010\x0014pÃn\x0017Å±×\x001233f±ë:uxÐIë£8`-\x001fTnáå¾~f-Í6kïÜKTmÊN\x0002H^8f¡Æ«\x0003^ÎC	rk,\x0001\x0004UU£¦N9©K_$Ö\x0011½\x0012¦ª×ùµ0Õ¿n\x0019!Iôx\x001b$!wô\x00158Yy1Ó¦i\x0010ñ\x0006MåP»¿0Q&|~õéÝO×ïoïkÉãå50Í)\x0007¢ ¼´yå\x0016?¨ÎõùÉg__¼]ÇVSlµ\x0005ÛSæ\x0013\x000eÌØSÉüÒª\x0019[O±õ\x0006l,îÒe¶©ðGÙÝd¯Öz7P)µÙ@·\x0010ÊÛ³Yå\x000e©uàÉÆjqØvm·`\x001b.üÃT¡à	ÛqR¾Y(\x0016iÇvSl·\x0001\x001bcd´#µI¥lÍ·&¯`U+£ÚO©ý\x0016jWìÍA>¤Vk	*¤¹\x001a°Ã\x0014;lY#EÈ4(Ï©´\x001c\x0014ÃT¬Öo¶Ø\x001d\x001d\x0016G;\x0012õ/h¶EI!¡Ü3«-·m,±\x0001\x001crj\x0004(Ð±§Íª6c\x0003öÌjË-f[\x0018®:\x000bÚ\x001e;m_f[¯*S5`ÏìÜ`\x0000­åv`qqs´=ú\\x0004¡\x0018¸'åÌ\x0000Ê
\x0016\x0010#\x00166\x0016¢
'?é¹ ÞéVµ7\x001a¸g¶Dn0&F]¾µ¤*ôfKiù\x000b\x0005>ÍØjfLÔ\x0006cb1§V·5¹Hîé6z$÷ÌsU\x001b\W}ãÈHÏu`R{¶&Ko\x0002ÍØsÏu
4\x0015â0É'ßÖ@ì©u)¬\x0006jQÃ\x0006j¬L¢\x0002\x001fÄY0\x0017ÒJ^ÛC})5³ÜjåwÊ²¶±·Oö\x0001\x0005x6%©&g\x0018÷ÌãV\x001b\n\x0010¸ JæN°q¾MÉÉ7ëb
Ü³#Gm8rÙ
Ån Ø9¯b]S½{æ½ª
î«\x0001îZD°)Õ×{.Ý\x0008ëjO
Ø³\x0013Gm9qþ­Ë\x0004fG\x000el8r\x000c\Qå¦ÒhN¸òN:7ðú\x000e³#\x00076\x001c9\x0006\x000b\x0006©TÆ\x0014ù\x0001Q<*i\x001c¹gg\x000el9sP~¸ã©©h¨\x0011Vø\x000c<*avèÀC\x0007Å=Hæ/.c\x0008¬Qªa\x0007\x001e:03Þð1Þ0ó»aßýoæYAøÃXA¥ÐàÜ\x001bH\x000e¶¯ò¸´5ù±Úq×\x0005\x0011,û(\x0010F¸ÚíEã_(ãû£\x0017×ï¯ÿqó¡úJ\x001c\x001c½[\x000fArpMXó·G/NÏOÿëìå:2L¡\x0017Ù\x0017if\x001fYKBª\x0018A¹Ö XOu7±ñ¬Þh¢W¯
à¹à.È5\x001dÄ\x0006b3%6ÝÄ;Åe\x0001)ÖÈ\x0013¤ZÊ\x000cmD¶SdûGd?%öÝÄÚ°ÚUò8@æ\x0002û*®
Àa
\x001cº¥`\x0005ç+u£µ ·I,=\x000e·\x0011ïbÉ¼©?Àª3ó&ûí,w\x0018LÔs<Ë¥
6ãg\x0006Nn°p;\x000e\x0019[4ÚÁ±\x0012\x001e¾
cÙ\x000b¹Á`@QÇ«Î\x0011ÇÚøqm\x000c#v3b×¿2\x000cF\x000b^ªÓÊP¬¿¾ÖÖ©\x0001yfâd¿À¢¢F\x0005\x0001)ò_f©¯yfåd¿S\x000f?k]nr\x001cK\x0015Yp~ØÒØ¹;59E:xÊ:ÂÁ«Y-HÉ´"Ï<OÕíz¢£7;|¦øíÜ0\x0017CÍN\x0013Õ}¸P^b´g!½ \x001an­T\x0003òÌ2«~Ë,CZÁIÊ=°!¾C\x0013òÀ13Ìªß0KH¿¤ØN=»ñNÂf\x000eÅ\x0012j?¯MÁÀ3#§ú²,\x001b\x0008Ø\x0017.Q¢ÓÎ©zàÕI\x00199ÕoäÐ1ÊKÙèøG ãËîPæi\x00143Ì,\x0006ô['óü²ÚïÍÅë\x0013\x001aÁØ$Ä¬\x001c-
\x001bÖrn\x001agû\x000fº÷Ó*É\x001ab¿?kK\x000eäêûxY\x0019fæ`¶\x0005¡{\x000b:l\x00129eÜ±§,Á¾k½G\x001bg[\x0010º· 3»6V³®R¬aåZ{¦zf=Ûº?^JGÔ\x000bÒH\x0016AV=\x0015\x000bz³­Ì³-¨»· §y®\x001duáÖq/\x0000ïù z\x0016ÑÝ\x0001\x0018\Ïdê6TM\x000f2ìæyÜzáÌÂ%\x0010Ú\x0015£ .\x001eÞ|\x0016*~Z\x0011kY\x0008\x0015àr?
Uæ4TnCþ\x0003w"ÿûëßî®êëZ±
9çÿ$f´(ÿë\x000e¯nnIþ\x0005w%ÿ·§ß^,$\x0001Ëý´TÓR7\x000f\x0003ï\ê§HÁ\x000e+£¹ÌÒ.\x0004júa§Ã°\x0003\x0011Ù
Hs.\U<
¿ptöÂOGá\x0007ÂTlIEö@º\x0018¬nÔèF\x000fb¡()Cqó(ðÅ\x0014¨ìØPî°J8\x001d/lëöq\x0018»÷Èalyäxu\x0017ÿÓ7¿^½OÖééíýÝÕ£VÕ±\x001c(ÅÓ\\x0017\x0005°\x0012Y{uyöòÙÙ«ód¦^¼½|¾>\x00065\x001dÚ>\x0006%(C7!7áÃ\x00082+¾ÃòÁÐ5\x0006=\x001dÞ<\x0006å}d.
I´'J\x0014¹R«Ð5\x00043\x001dÙ>\x0004Ôes$5äyCØ\x0012\x0003±r\x0017é\x001a\x000eÂn\x001fãüã8\x0008ÎÐD\x0015
ÖÐÿñ\x0008ÓAí°®|	ì[gh\x0010laýªoï\x0018v\x0006ÖØ]
øA(VÞ6xË¥Â;£¹á¬rK\x0012½£×íö5ÞË%Âc\x00125ñeAüJH¯k\x00103û*·\x001bX\x0014©\x0000SJØ\ÉÆÂ®$ubfaå\x0000\x0013\x001b	 \x00197-èE\x0006¥6X\x0014j©7Q÷(föIn7PØ)^8,âP:p\x0007AµöHÚ5
?\x001bß>
+IõÄ\x000bÎÓ¦\x0018P× fVVn7³Òznæ<@R?±\x001caQb¥T¯g\x0014jf¡Ôv\x000b%#«¡Q ¨g¶³Z\x0015\x0015\x0014Ts\x0019>
\x0002\x0006\x0002(à\x001c/x@ï\x0010q\x0014½q·Ñ5\x0007¥¶»PÂhVù´ÆP\x001f:\x0005EÛbü\x0008Ül\x0004në\x0008Lê\x0017«åä\x0001p=Å°ñcíkµy_G)$ù1\x001c´ôÚ\x0019\x0007A
Ãlj´>z\x00140Û×°y_'©R:îâ
päzØàVrSºF1;´aó¡\x001dG!ø¸3¨UO
a½.ßâ\x0011¶õ4úG[Ã¬Ýý` nÀ@þ[69<\x0018
ù&á\x0018HÇq¦âuÃK½\x0001ÛÇböc8FLI¿º¹¾»ÿ|y{ÿãu½¸2V¹¸2(>ú¼ä÷lX§qOéWg§ñ//Þ>?]Bý\x0008¨\x001dt@yVÊ@inOèÜèR­V`µ\x000f@O\x0007 7\x000fÀz¤ÇÐ\x0007\x0002mYé7,)ov\x000eÁMà6\x000f!r_P¢}éJ\x0008jI!©s\x0008~:\x0004¿}\x0008\x0015ª°Ô:\c9%\x0005»Þ]½q\x0008°V¾÷Á <º¦1p=K\x001c
_Âôoç\x0010fYnÞÍúD¦Í ©¶E\x0005Yd¯ýjÑBû\x0018fûYnÞÐF«ä»H\x001aä©±Jà«[-k\x001fÃlCËÍ;ÚXWÆÙÙ¬\x0006Ç
V]­Xl\x001fÃlGËÍ[ÚXI\x000fÕ\x0006\x000b`è\x001d,Ç×ëåÛ\x0010fC\x0008`,I,\x0018o©É)òûvÅíë\x0018$µÝ$Ñû\x0010ÊÀó\x0000\àE¤a%[®c\x00003ÿHmvL°EO=º\x0017Ô\x0000:éÄUHw\x0001fc­c°Ø¡$áCz±K\x001dª8|5ÿ¨c\x00043ª6T+\º¾¥!(Ö(½£XKÕî\x0018
Án\x001e²tïqÑ[R,p <¿øÚñyv(¨ÍBt0Ø â\x0018¨W¯p²¼Z¯¼
õav(¨ÍÕú
\x001bç\x0002«v	ËÍ·¤_K:n\x0018C\ó;[ü\x000b\x0013Yº÷WGßÜ|\x001fo×ïßW·(÷¶d@\x001a,Z¦\x000cdOíBã\x0011«Eùç'Gßá}óôüüt\x001d_MñÕFüèÕ9ÊFve
iÁ±ÖH¿*Ð¯§øz\x001b>¢R÷³È.©ï³"\x001fÛÁª%jÅ7S|³qöãÕÆSÆ½¼x´ä×]/Ör÷ñÝ\x0014ßm}	\J¢miñ«5'k¸%Íõ.ú0¥\x000f[×¢CÌjp¤§
ó&]×k£s»³Ñð Æ\x0017ÐÒ\x0010¥^Ç¥Ï¥\x000fë*µøzßlêd6'YW8\x0002\x0014&­~¿õß03ÚþÅ;\x000c{qa¡\x0015÷$ß
\x0007º¤ëìzÊ®ÿXìvÊnÿ\x0018ìf¿ß¸YxT\x001f}sýáSµ¹`"Wak
ªÀ{
ùÅºHÜküß<}ùfÉÇqû\x0011Q7¶Bc¿ùl`\x0000ê
Ú²dYü²\x0003¡a

ýÐÑ*RßßèH²\x001c_\x0011¶÷BV8ÆÕÐz
­û¡I¦Çavv&6ÜÍÕì\x0016b3%6½ÄNHQÖ\x0006C\x0008í%é<\x0008ðë\x0001jh;¶ýÓl\x0003Åömü3µÁ\x001eÜ+t×J:Z ý\x0014Ú÷Ccø ±q\x00005²6ìá\x0006¿Ô¤\x0011z\x0012Bvó\x0010róú0\x0014ÿ¶NyÖpÂ¼36xãÖ´Ù;Ùmð\¼>SúIªþ¡2%«D©í_\x0015|m¡þîjûª\x001b\x001c\x001d(âÖé¥\x001d¹±D¸GnÆùëg2Ö;aöåíÔî1ù½
\x000cëê{±&pÓ´¸÷f\lñ"iìt .²`ã³q­¦´ÉìÏ¸ß4ãÁðßIºN!º-S.ú047ûìf\x0013;Þ2=\x0015GÍ4Á\x0014D8Ü±yÁÌBM¾Uy\x001eë¯ïÿ^Kí´IShÂ
÷BDýkÖ9±«Òî¯ñ=ÿÍé§oÿs\x001d\OÁõ&pMÏùÖ¢$3IIóÉcWEÒ[°¥bK³[ðÝÒJ\x0007QªÝä&5ØAh$¹û
ä\x001aÅøLI?ÐÀR\x0011 :\x0008> ÿ|=aï\x001egÒ\x0002\x0017&¼H\x001b'S£¤9Îµ;>uÏª~Âw/\x001a\x001cþ \x0013®Ýlcº
Øè¿ZZáVsðG:îúæCEDý[;%·v\x000b¹·ÜçÂxÍ/`2®\x0016²*¢"Å¦\Î\x0017¹Ü´Êã2OýHÑ\x001cbLÂæø ×´íÚÈaN¾eÇ]IIA\x001cR\x0015HR\x001fçR¢\x0000\x0015y\x0010õèf>éfÛ¤Ët'N'ì\x0004ÈÙ´D\x0007ràJ»W\x0019]nA·%\x0004";kèÈxãä«[EæF\x0003ú|ÁM\x000bæß\x001eæ\x000b&l[0ü$ÿH\x0006û\x0007¡G\x000có³?l9ü­³Ç\x0004ï¡´Ie\x0001¿µ\x001a&r%fþ\x0016þË-öERjt\x001c\x0004§»EûÂB*!Èõ§Ü\x0006t;Gßt\x001e"h½â PD/²m#Ï#%çNÜ´Ò­,\x0014ãYä\x0004r\x001b¹`öüÅmG)¯Àa|RºÂ=Ð¸\x0000Ìì"À\x0016»há@V=\x001aïºFë7Ð\x001aôý÷\x0007áöú]½ÿ¯V¿`\x0005­\x0015Ò0$fYQÑÈ5ÍØôlòìäüütáÝDì?A\x0008·÷ÆßÈ
M>ß,âÂ.ªÝEÉAã¸aÊ
[æ;¸cÂÖ.3¤Öy|\x00035¨6\x000e[O±õ\x001ffºílyÛ-ëÛKÉW~\x00197&X\x0002«bÅù®yN&î\x0003·8­m»iq?>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ág\ëZê,üÅ$u\x0006­c·¿Þ\x0007SºÊs¡PéÖ[hjÐqBÓ @'\x000ftÆBãØùÿy\x0013\x000cé\x0001i6ä\x0015%¯èå6Vàf¥\x001fy-åç;ò:pe+»×Ä©\x0015¸¼¹\x001a\\x001b±ùòªWu/¯ÆÁÄëPÚG\x0018O"9óSv:xuÉ«{y¹ÇöWàey;(7M\x0011?ÐDßÄkJ^ÓË\x001b\x0002SjcÐ´¾Ö¢.?0ö¸×¼¶{ÿzÐeI¼\x0002s\x0006Ôâü|¿n\x0007®/qýÀqóK½\x0017zê\x0011ÙhóòÚöv\x001b_© ö\x0013ÅMòVa,éölµ{yeÍx·9\x000bæÁcoAÅ\x001e\x0002¡¹e#ÞÊñnsf\x0018´Ä§îx¼\x0012gÆit²\x0011peÎx·=.N¹É*=\x000c\x0017´L\x000ei4ñVæwÛ3«qCÀlt\`A\x0012!\x001aÚ\x0008¸²g¼Û I?©S¨c×wÒå9¤ÕÄë*^×½£WK\x000bÌó(A'ù´À´Q+\x000bÌ»M0Èg\x001d
ïAN8&Ï¶·\x0003Ê\x0008n#¬u~*+^`Ã\x001e)Úø­Îÿ~··Æ»þE¶h&Â6y\x0005V2ðCÊ¢maOí]>4å»'ú\x0011Y:Ícf1ú\x0011$y4zúõå(üE©\x0003ý¿ÿù_§\x001fÞß~\×Ë)ÅÛ1Qô2>æØ.V£ºÊÑéËgç¯\x000e´r\x0012¯(yE//\x001bÓW9t\x001fKM¸æ»kÁ%®ì_^ÆØè\x0010hfã¦\x001c.¯ïçnçU%¯ê^^\x0010£³yy-
xY£õ=(3»W¼º}uÖ¯ëëx^_¼Íõ=¨ µWÛ\x000fì_¥\x00152\x0018\x000fKÅh}ç\x0007§¶óVû÷o\x0008OOFËüT\x0013Î\x001b\x0016X;_\x0001ô\x0019ðlë<ÒNÒÑ8°~ZO¢`ûfë °0lßakÆöÍ\x0003Û7\x000f?Þ¬JóÝ\x000b±p*\x000f"\x000b¬KNÎñC¹\x0008ÀýæìÐØ\x0019¢U%­ê¥Õ\x0006]²\x0011êY?tzùaUÐÕ°ºÕÝ°
+!-3ùi6ÀRÁæ¡{\\x0003¬)aM÷>P¸\x000fÿÂ\x001cD'áø¡ ¡\x0001Ö°vd\x001bdUG\x0008-n\x0003\Z~èJ?Ñ.\x0019=z@u½¨&\x000eqJë\x001a\x001aÊÓ+:_â Pßêõ%­ï¥\x0019\x000bi]¹AðY\x0007\x0016s;âPng=,g%,g½´ª°\x00066)lÀ\x0005ÒÑç|Õ6x\x0010WT¸¢\x0017×ã\x0004yOÒÆ,õ6¶WæwÛ\x0003Çpm-(ÖdáT\x0003å\x001c \x0008[G+ª°ïu\x001bh-^àÁ  _ 	ÇçÐWãrµ7ù&üEù\x001ctv}³[§9Æ'©e3Àá=\x0007/ÂgÏÏN\x000e](Õ^l\x0000²SðcgËcÁp\x000eÍ«|5rªSu­gØ§v²¯iiÔ
ÓjäÔ%§îáÔkv\x0002ÆPÎÍ\x0017Í4B\x0012Òô@`Pæ«¢xU4\x0012ç\x0010Û:à«9mÉi{8
\x0007íØÈi
¦8É\x0012eÚ\x001e:í«1]éz0ab\x0000b
´¡Æâ@\x001dëæ\x001b\x001a9}Éé{8½¤\x001b7<÷&Ïd\x0019f¬;\x0014£¬å~´¬kAÅ±Ê\x0017AïÆMCxÍ\x0001§´ST¢S³)¡\x001dÖïYA2Lf
Ê+ãÉ{¬§\x0016¢þpµÎCÁ¬²\x000bØâ\x0017_mPÞµC¹\x0004}¨ä5EVÝ
VÞSìtHêý\x000e­Ò°iyØõ¼ðì)MûÚ]\x0008R)e±ÅNerWvâþµËËô^ð\x0014þ§û£§»÷·«\x001a¯â+B\x001ed\x001c&ÇD1\/b¾9zzòìüdYt0E)z0AKOãðATÑ\yUFNYrÊ®åäØÇ\x0006u3"¿\x00148Ku\x001dó
ªäT]ë	44/Í£,¥\x0006\x0006-%ë9uÉ©»Ös:F6E8Osvô\x0016¿tSBÇ»¶ä´]©¡¹Eãa§²\x0003±èzNWrº\x001eN\x0017õëp¼\ÎE\x0005×FÉ\x001d\x0018ù³Ó¾ÓrÌ¢ÃD%\x0012´4íÀ«ÕjÌ"±£\x0018¯u=¥ß;3øüCÅP\x001b,'¯]Q/rzäð\x000e"%ÕHz½1}\x0018Tx^ûÌð\x0017à3Q»2eH^Ýÿ|õ~M$üo\Tu®[£³Øf¸à\x0008\x000b\x0003\x0017Ô¹bê,`	IWo^>;4wÃóÚ1\x0001³ìg\x0006a\X¤¹>&1ó,­\x0017^R:±°ÌbÙâk vxÕ\x0007f|\x001dÖ­3¯Ö÷/4gáÞ;yl	G
ÕMõü¼¡\x000ehíJh8"ÝÐaK°ÜGn}%\x0013.VXedô|Ý\x0001mm	\x001d~ê?:êùã1ô2m\x000f/é\x0018Î\x000fiæ¼6\x001d|Èxxü
ÔÂeã!	z#f¥*æØ8ÒË+ü g ó2k¬ù\x000cÝÙB;²\x0010Õ2Ãý¶CY\x001cÜ£R(\x0019\x00114>k\x00199_wßCmkê-\x001db\x0008\x000cfùòhÄ\x000clø§ù6vjYSË\x0011ê©oVÝí´\x0011$è,õFÖCèjSÃÝÔ0V
\x000fbc\x000cg@R\x0007\x000fâüÌvhÉX	
?\x000e@³	Zæl	Þ¨\x0017ú¸Ú©Ùº@
/jÝÔáÃ-¤ÅÓ[¨ÑÊ`ð!æËd:¨k(\x0007"³\\x001d\x001bCâ*é,*µ=á,nµ«\x0005ÿþûï\x0003¦OÆF¿¸GD<\x0011L\x001f'#2ÿÜÔ\x0007þ~\x001füý\x0000¸&±õ\x0000n3·ð\x0005÷ûÜ\x000eXmêR\x001fólµIì\x0006Ô6ã~·Ïýn#\x001fù¹Ü(z\x0002êíSÿk`µÝ±¡ÅÖy(EÇr^î¾{·Ï½\x001bZmÇ§\x0016Üo\x001fðïoöÁo\x0006\x0016Üõ\x000e+®r(¥èF#ç+YúÀØ\x0007ÿa`Å
\x000e¬\x0005{âL^q5mñíÜNù|®\x0007þª\x001bÉÓë<'Ó\x0018ÆÈÓ
WýjÕ¯\x0006V]A+®º&÷C\x0007t6ÓÇýÓ>÷O\x0003Ü\x0002;;VÁáOÛ|£l\x0003ÿ¸\x000fþã¿WnZð¼S4vÜlºà×ûÜ×\x0003vÅc\x001f\x000bØ\x0015nÓÐz\x000f²Ìî¿ÙªÔètwÿûQDµ®\x001f\x0004²¨¹X2ìç< Ã3Ã)=TOqtzòæ\x001fGq(ÕÁ\x0010»ÿxfYÙÞJí´G\x001d-\x0019.=&kÆÒÎÖbyQ;µ,©å\x0000µ%ÚêÜ\x000bà9ºKÍ\x000ewò¶A«\x0012Z@k¬X.êm$hÃÀØ¡Vj]Rë\x0011êpÓZ'e?Ïi\x0019?TØÊlJfóµlj[RÛ\x0011jÕVc\x001f\ ÆXJ«-wµ+©Ý\x0000µS¨a!%^p<·Ùê)s¨6¸\x0015ÚÐ~\x0000ÚN\x001bDÉ,Ý\x001a E¾\x0006/Åê.Þêl]ÕNÍÁ­Dj\x0013_\x0012"µ\x0011¨»0p¬\x000f»ö\x0003ñîk^9F>â\x0019­\x001bd\mJÕÆl¼:XHÞ]yF>â\x001a¿èjW¾8G'²L \x000cWJ4"\x0018ï)s¸º¸
ºr|Ä7~Ñµ®¼#\x001fqÎ\x0002k\l!rc­ç\x000eßN>¬ãÓ]¹G>à\x001f\x0003!ÊÍ`û'ó\x0007¢\x0002\x0019ÏÏ±ìÃ®ü#\x001fqÞcnG2Û®=÷*\x0007«jáÝ¦\x000f»ò|ÀE~ÑÕ\x0016\x0014\x0003>Ò3Ç
î\x0016[0Zl1ÿÜÔG]¹Hñµ¸HQß\x001d\x0007\$È\x0006r\x001câ©r³\x0017a\x0018Å\x000e«M´aW.R|-.RT.R\x000c¸HÏ\x0005FÚáVÄ0\x0019\x0001Cí®­Ø\x0014_\x0014\x0014\x0003NòË®vå$Å×r\x0014\x0014\x0003Nò®6\x0013eB>%ÐÊzþÇn\x0010ûRx"IáQ\x0015æ/_ÿøáê~Õø\x0012\x0011®èÐÊ\x000bÂÃLê|¿qRæ\¼áÜ\x001d~AÌÏ¿yyúæ|\x0005µ/©ý\x0008u\x0014æJÔ&
­²ÕÜ:\x0017¨çU@º¨Ò®¬×-³ÀnÀ¶Ø\x0000$EN\x0018.æµÐú°e-G°EÔ¿Øþk,ºö}ø©ZWÔzÅó\x0008Ôa\x00078´ß õ\x0003Ui-Ø¢Ú#bd\x0018\x0003ó\x0018\x0012¶ÆT9îhÌë`uaKVbK6Í¢Ê\x001f`k{Ìs!9çx"å|\x0013^\x0017¶©VÛ\x000c¬6³\x001eå±pSÐYÚçþ\x000c\x0013¶þf«úDª#É­ÀíPó{{ÂÍ\x0003uÏ-Ø¶²Úðc?v`\x001d\x0019óüÇ¸Ú¹\x000cÐ0¿\x001d¶Àx$!àéß%*jEluì37\x0013Ä=¯ÔÅ-UÅ-ÕÈ.qøÐî\x001dµÆq¯òî\x000e»ÿp½T\x000b·q\x0015·q\x0003ÜÁdÍ7oâ¸ÈÈí\x0018§Ï:tq{Qq{ñuì\x0013\x0018YÚn1t,9\x0014ÇÇõ\x000e¡kv\x0011<?Z\x001bæ6¦¤ª\x001b~ìÇæìX§\x000c¦ç\x001ad\x0018ã6á\x001e§Êð
ÍTUýN>UýNóé´ØRá\x001d>_\x0002\x0018®º} ¼a\x0015>\x0017ûÒú¤õ¿»Ú}8z²ûåÓõÝ'gp³j\x0008ÿÁ¬¸´v\x0012]¼¥}wzòòèÉÉëËç\x00170ÏàìÕ®,D\x0017%º\x0018D÷XÐhý$\x001fèH\x0019\x0015r[²«]
³Ô¨?v®ÿ"tS¢1tiPsÝAö;/»W¤\x0001=_9ÕÍnKv;ÈÎ±v×ñé\x001eáp$ª3\x001b²»Ý±+ ª-¤bF[-¾pw¡û\x0012Ý\x000f.»Ç\x0018 N´Î÷ Ïè
=è^
ØG6Æ®Å´e$&U\x0014ÉN\x001dÒ2î¯û uWÔ®E¼B'xlµõ\x000b3Çºá+óÎ\x0007í{¸\x000cÏm\x001e~îÐ\x0004¿)º¬Ðåà¦Ñ(c\x0013E»}^w*ãbYÅ¤\x000b¾rM|Ð7uÇ9äaÓd±°î¤8¾,Þ\x0005¯+x=\x0008/ók¡\x00136O¤\x000fìhhÄ|\x0006´\x001b½ò«|Ð±Z3Í\x000fQYV=%í¹¬yÕÅ^ùU>èXCüï=++M~c;SùU>èX§2_\x0007ÆÞ£v'\x00064z~Öq7|åYù k
wê<ï2ÀfT*TþÀÛP\x000fº¨<«\x0018ô¬Î ÔSÙ³y×(çõ²c\x0017{åXÅ cu\x000c³1°g8ÊfÒä\x0016½¬¼ß\x0005_y'1èÄ§9XøßU\x001aÛJÃÊo\x001aÊÀA\x0003\x001fv
4ÁÖ`©Ç-oØ¦&^T&^\x000cx/	Þ³cM<Èq$x7/\x0008Ð
_Ùx1hãÃ¶ÁTâ1ªv÷vþ\x0011¦\x001b¾2òbÐÈ{AW\x0000/²§YVÞn\x001bÔÈÊRÊQKÉY\x0001ãH\x0014OiTtI\x000bü¼z7W1¼\x001cá½/`\x0017\x0013N«Õ\x0017;0n§kÙ«@X\x000e\x0006Â\x0001>g®§YÒ=?1±m\À|%J\x0018oÝXÄÐ}ÿ3¸üpÊ\x0013+\x0014ÃZ~¨£Û6.Ûÿ\x0004î¿\x0001tò\x0005\óÉì`-_ÓÞ=øì\x001bØð7ä\x0004&\x00114¨tåû 
zsÛ¦YÕþ7¨áOø²\x0019K.?û-ÈñßÁ±\x0003ùÖ\x001c÷)\x001bb7{¤(\x0006j%[º{ün@\x0004;T%Ñ \x0005h'77W©êõÍîÓîÃºR*\x0015®á6½gBy¬1:·¸¨8\x0003}rvv©^\¼<XH]ìºÃ
Ö¹ìòN]Aâù\x000e¹\x001eb_\x0011ûnb&¢\x0004bísû¸3¹ùÉH.f7ö\x000cñÁ=!y\x000bï¶}¥©M71g1ö\x0005b¸uä\x0005X\x0012\x0013þaöèu +]"Ã#óc_dU;õ\x0015;Y
Ì[\x0003þ¦wHwÊm|°;\x0004íÙ0«|_»X$íâ©\x001fÿ"\x0000}ºú¿N>|¸úôiÕð\x000f#C`îynt\x0010`éÑCbo\x0017áçàON^¾<½¼<$)°¯\x0014,RðWE_È\x0001½\x001aÃ×~*\x000e´
\x000bc\x001ctjå*»\x0007ê^ñMoFñuT,ø\x0002ßô\x001cÎ"Á\x0007y\x001añ]µúntõa||®ÌtPy\x0012é%£¢ãy¡ñnzÏKzÏ\x0007éCøgóâ\x0007Þ$¦\x0001\x0017;Üú|>ïÛÏh0Êþ²A~#¢pB¬BV8#Çq¥L= ¢ÕÈ/ªåçbtýEüBn\âW\x001aðæ\x0001õF~Y\x0019Nøq_Ûã¼}à:Ï.Ã¹Ä©\x001añUåµêjÙ.ü(jó|ÖuÖ[âßÖòsSo3ºý¥D\x0005lïiý­ÍÓ\x0018
³|[~[¯¿\x001d]hèv¹ÚÍdÑ§Ào°XÏÌ?èå\x0017¬ZÁF×\x001f4±s¤á8ºÓ*µjÛõ/åW¿_íàgSV5l¥\Öa¥Aþx³ßV¾\x0017~\x001câ)T2ï4=3ÆË\x0016[~ÂM~Ûõ¯½¯\x0018u¿0.OXð0üGæë¶Áóû *a\x001b¿ÕúK9ºþSµª± «\x001dù©/©mCOð]ñ»A~f§óKÑá\x0018ù3=?sµ_Õüj£f+ÔÄc6YÜ?ú!µ¿F~#*~#Æø%4tfûciÚvÖÓèSÚzùíàòÀU\x0019_ã\x0000
m5\x000fÚn\x001d}Öõæ)\x0002­õ"{ÐX¢8\x001d!\x0015òóùöÏ`~_¢ÎDÝß?~ø\x0014®Þ^_]ßÜ¬"géò\x0015%Òd_NRþ-OTùû«áÓ£·ÏO­V%´\x001aöð`fýiLòp !ü\|»o§Ö%µî§æ!ÒWy\x00128ùOàtj+\x000cÚ¡M	m\x0006\x001aÆ%ûh\x0014ÅÜâ\x00180{à±¾ÚÔv`©\x0019)sjç³\x0008±öo¸­\x000b
2?iu-¶Ôø6\x0019\x0002w«Ë¥Al¨&Û
[ùê4ú\x0001lhnÊ#B¡//6Ös8¶,\x000bÓLmª-b\x0006÷H\x001eù`Bäk< íùbMA+6¯\x0008üØÏÍIØ(ë\x000cÆrn¶ØWVó\x0001;Âa?ç­
ÌÙøá{i¸ðm-jl1­±ÐÊp\x0005\x0018\x0003¶ÄIHj¹>¯[ÕDl\x0012æ-'_CÛàY±<x®Û×Ü\x0003¦ë@\x001fÉ°6\x000cg{Yª¤[Ë[Ë1\x0013¨3·e Ûl V»[¶<²ÛÕ\x000eÇx\x001c9%Ä°,{\x001c]XÆoæp¨[å\x000eN=ßú5tM¦ÕÎÈ-Ö>¶3ëyàH\x0010B¶Û:øy»±âÅX¾áR»\x001aÛ]\x0010òØwÍ<ÞÐ¸Ó¨*¯æ\x0013Ô]Üµ\x0005\x0014#\x00169CËÍ\x0004Zî\x0010÷Ñ¼¯eíÜfnÍ+nÍÇ¸Eà
>¥»
ÍNØÎÁ\x000bW\x001fI7t$\x0005doq¼Z®
ä\x000e¯7á\x000e¼ÙõFøÊ\x0002Â\x0003û[À}\x001dÅðÓ|ÆpÁÁý­ývë-yu\x0003|è\x000e<
¤\x0012\x000e;\x0007&emç»ô»¸eµÞR¬·ñ0·5i¨cíIÞ%\x001a
¥6£\x00165õH\x0004¨34Ê\x0008mHÌ,\x0017ï6cÛz±íàbó¬üëmP\x0011¸AÁºí·´õæ¶#ÛÐÉðý$Aa°\x000fLå¤vnWs8K¸Hf\x0011qk°\x0017\x0007ßÜË²­ÜªÎñÀCÆÄgnÂ®ãöó¯X¹©©\x00167e§v\x0003A\x0015Ã¡¯ÆúÜ¸\x0016>\x0007ç\x0017³ù×Ã6n¡}s\x00056Rv=ºÙ\x001d]îîÖ%¡#çâEÉqI¸zät½°Ë¥0xåäèòäâpÛ×©Ö('×Ç*t4\x001e£ÚeÎ²\x0006Öå&£&VS²ÎuMêý¸®YO^s·ñººÕu²jTë¬8õÃL¬ËC·\x001bXËB!_ÌFhÜ\x0004iªòÞÂ*b=0Ëa=ª¨VçÙâ\x0016ê©fÕf'í¹Ôx¶ÜrgG	»Pwíö\x0004Â_L\x0013\x0000ôíõÿü÷í*ÒX\x0018»\x001f¼ÂW\x0017%HêÇÍ+CM¤Áf\x001fZV·'ñ\x0003°¢\x0013GéªÔ0Ã1%#)Ð»	¬,ae'¬dÔÈ,\x001d\¤Ro\x000cuuÊåF\x0013¬*aU/ìÔü\x000b¡°ÊZ,$p½n\x0013¬.au/¬+¶·+\x0015\x0008Q%®¬RÛìYSÂ~Xl/â¨\x001e`
­ì6¬¶dµ½ÆQSa`\x0017²ª
.ìò=®d=lµ\	êú·kGî\x0004:íJb$f-4¬ª/a}'lØ£(¥L\x0007æB°Êl²\x0005
'ëôm£u¸´\x0006ôj2-ÚX1?·¶ö^½î\x000b\x00164Ë_ÍËPþ
õÄ½Z~]m¢­Ü\x0017ïõ_Ê\x001dË¼\x0013B0ã\x000c
/a«\¾»7ÑVþ÷:°/\x0014\x001aðÊñ^\x000f¦Ádrr[6#\x0007&Õ6Û¶r`¼×}©¥­¼\x0002ïv\x000b_¶r
¼Û7X|ÿëG%BR¿óM\x001c­´¢2·bÀÜæ\x0002à\x001c8î[LÓ\x0004ç°
menE·¹Õ\x0018C¨CÙ;\x00124Õ&Ó­\x0010D}Uè¶µ\x0016§p:å'[Këºü\x0006Ð´®ñ\x0012½ÆËÈ)D°¨@©$\x000ez\x000e»`¨"ZÑ\x001bÒéi	\x0011c¢Åw
¯\x000f
\x000bm ­ìèµ\x0007FOºFÄF$Å´óM9­°²2\x0007²×\x001c\x0018ãÊÕPÎ`\x0005Æ3vë¬Îì=cÆ ¡õ$=0	ÁÓÕ\x0016´Õ!ÝÌEp\x0001<Ãúâ|gb»\x0013«ªz]%vÒcos
\x0001\x0006\\x0008t\x000eh\x0015æ¬Fæ×¤ð\x0017Húæv÷aÕ\x000cïTOn\x000c\x0016:àt.\x0003Ã´°5\x0016Wöów#¡(	E3az(0â3\x0005JÔ¨ã£²$í\x0006UM­eD¨\x0014\x0012:1L¨JBÕN\x0018ÌQ^BZ\x0012BáLZg¯k\x0001u	¨\x0001ARÕÐ6Ì\x000fBc½³Ë\x000fk	MIhÚ	éÈjq´@5LgÆÏ-\x0001m3 \x0004	Äç1ý#¬ ¼ì|Ö\x0002º\x0012Ðµ¯à´	
v_±¥\x0015\\x000cÖ\x0002ú\x0012Ð7\x0003ªX¾K(sñÓ\x0012.>T­$,t¬ÁZ³ö5ôXn5§Úÿ\x0010\x0008á"ªÑmÈkÒîQB\x001eEÓ5Cx=ÅkÆZÄÊ£ðv\x0002
ê\x0010ó½-Ä\x0010\x0017càµKáí>%\*¥Ós¦àÊ\x0011\x000b×"V>·;\x0010Õ\x0008G«\x001dâkn>.£OáíNÅ\x0016k¨ñ\x0016)ùd³íðy®
o÷*Ja\x0007R°ÔäU,\x0006áN
\x000e¼r+¼Ý¯X\x0003\x0013!0þÂg\x0016q97·°ò+¼Ý±hu`\x0014ó\x001azÅ\x001bfyRöZÂÊ±ðvÏâhr¦Õ\x000c×Pä\x0017eí\x000eT«­$\x0014c\x0011í%`ãé¬ ïów^~¡_X9\x0016ÑîX\x001ce.¬¢F\x001b\x0019\x0010\x0005×"ÖWvÇ\x0012Â\x00065ý³ðVq°ò+¢Ý¯xÅÅ­2\x0018?HÕµn¡O¶°r+¢Ý­\x0018Rr°Ê$wò|ÔJjç\x0017­E¬\x001chv,i¬­ÃÏÂ\x0002ÅåßZÂÊ¯v¿bIaÕ*É\x0007ÉÞî÷\ù\x0015ÑìW¤pdµC<\x0015;4Ã·uH"VE´;\x0016KO~`q°VnÍË\x000f~k\x0001+¿"ý
lÄ<HÚæó°\x000bi\x0001b+ùdåUd»Wq¢°6^íû=í\x0016s`k	+§"\x0010
Uÿ­¢\x00067iÉbëeùöµSíN\x0005*ÐQÖ8\x0002MGyÔ\x001eÊ:ÿÕìT@HØ¡É¦7F9]õ²ðZÄÊ«Èv¯âi\x0002U\x000c=¤¶âòXµWÍ^å\x000b\x0018DY¹\x0015ÙîV¼"u\x0011Ñá\x000bT\x0012/Î\x000b*--[Ín\x0005Þd­"£±¨n\x0003z¹ºh-båVd³[\x0011 í'C;sZE¬^\x001e­³\x0016±r,²Ù±|½¨*Ë­:,·&ç,-eH,]LÕüHë\x0016ÄÊr«fË\x001dÎ\x000bvO\x0007÷\x000c
à	M£\x0011ªL·j7Ýð®&&Ó\x000fkô4 /Ïª~»h6ÝQ\x001aü¢óÕTª)G2­SéVí\x0017\x0002Ë)Î!íËéM=,â¨ÍQåVÍ;h,UEÄ+£\x000e\x00175\x001c©Êr«vËm5êÚX,¢Pö¡\x0018µª2ÛªÝlKzÓØ"9 =±\x0016±2Ûªý>\x0000MÖ¢Y7¢R\x0014å.¢®n\x0004ºùF\x0000îyÚTO¥=a\x001fF\x0010ºr,ºÝ±\x0014 ÛâL)ÈY(»\x0016±r,ºÝ±@}\x0014ú>IÃ(¦­¨G\x0013ºr,ºÝ±x³mÁ&fm-e¦;ÁpÀ­+Ç¢Û\x001d\x0016\x0014Íªi\x0011LÎð"Ö¯âí~Å1¬ç&\x0007­"ÝNÕpBQWE·;\x0016íPØ+\x0006³8\x0017ÕÉ\x0019N×éÊ±èöL\x0013hù[:Ð9
¡ëé²øÎZÄÊpëöx;DÒÐi±9\x000cóôT¥ßLe¹M»åvþxÚ8wX[O[q°²¦Ý*zOÏºa+âi1~º^ZLerL³ÉFO[Åò>ÄK\x001b\\x0007L]äÒ|%LtÃ\x001brá´\x000fí\x0014ã\x000c/a\x0015æ0LJÇ\x0001C\x0000>§8vY$nõï¸ñ~Ë»æ_³Á`+'£è\x0019-#\x001bu~ÆìQvJ(ºâS6\x0007×\x001eÔ\x000e\x0014.¯~P«f~¥G5,¨ly\x0013âô\x0006
\x001d\x0002ùYmzÍXØ[[:Ä÷Ay\x000fg°dôXÅ&AÜ\x0019®\x001eÀ¯­\x000fþ¥®±)B¿]}¸O³mN®o×
¶\x0011J`tkBèã2IJ­V«Y}òöôå4Ùæäùù¡±6HëJZ×I+i³\x0011J8\x001cVÚAÎÍ´¼¢å½¸°¸<Ëüi\x001c\x0000\x0013\x0016\x0017µ å|QL3î\x000e\x0007\H÷â¢êEÀÍ³k%ÚR;/Ò\x000c;å¨X|´è5,-Ð4ÅD\x0015Ç æõÍ[aaèW¹\x0011L'­ä\x000eohQÉm9QîLÎÛÖf^_o\ß¹s%x]SV\x001e\x001cÞ¡öªaó\x0007­¸¢Pb0õõãfá>\x0015\x0000qX·ÅfgíæUðyUes£\\x0017¯`¹8W	I}¹(5¨\x0017ÆZ5ÓÖtÓ
¼À\¬\x001d7m^­çÅymÍk»y%&7%h\x0008ã\x0005\x000foOZÍ«}6óúÊìÂ}¼àxqÆ\x001dK·=¥âóùâV^¹ç&zý\x000cáWÖnÚÐkÀfóÃ
y\x000býCà$V\x0017¯uè¥¡YN\x0001S#ï|©ùz^%¨¦ÆLPP
W÷b§ÐÛë\x000f«&Àrß°4\x000cã !H@u\x0001ã\x0016RÊ¯Þ\Æ6¡·Ï_\x001eZ+ö\x0005\x0005	\x00027
\x000fu éví "!ÉâÀ¤ÚdrU8eóÑm\x001bëì¬1ÛÓ¾¨*B\x0003U6\x0008áÂÍsk¼íhcnÛ5^·\x001f\x001f«ÚkÐ\x0001eòrØØÝÑùÇ»«ÝýïkhcÅR\x000f\x000e½Nq\x0017\x0013BÖr¡(&T\\x001c¿º8=yóMIlºÃ¾ÍUàPTÞÃ-\x0007_¾bÙÞFÄ¾$öýk¬\x0011ØçK\x0004\x0008q\x0012ð¼ø_\x0007p¡:¢R;Jï\x001a{ÐuKÈ"k\x0012å</EÖÌ+dÞ¿ÈhÎ\x00022v\x0016L+!Ï_ÕzE,úÓLÚÌs\x0017D\x000bVy«³W¨Ô¾ÒlQ\x0015\x0017V\x0019÷²aVy³½¬*d5báò\x001b*¬r*f\x0003\x000bÄózÏ=ÄIæ\x00036Ùc¸ÃAØ!ï\x000b­RÏ±éA®l2ï7ÊN\x001c£½yiÕ´È³\x0001p\x000f±­m7±g(%\x000bÛÂ(:|\x000bW\x0011»þ5\x0010úâ"£µÀ&79ÿDÜ\x0001,*,úM2ô&àÉÓùU\x001b`2Éz+/"*O-ú]µ÷X³\x0002ÁÉöÍNÖbþ&×¬*_­º}µa$¿Æµ \x001aµTóÕ\x001dÈºr|ºÛñ\x0019cð¡\x000b¥#­Ñy8¬\x000bcÚ9Ûú98kÌg·Æ*bïÔía®ã\x000bÖ¿ÎZ\x0011sª\x0017Ì
NaÌäVÌµcÝVÎð>wP@ªÊ²Æ`G4ØÁ÷¢åþpÙ2Oûó\\x0004eÃßâ%
òû\x001b1×{£?ø\x000cV\x0018\x0007/q!rBØÏzÚÏ\x001b!zkî­aÅqØÍËÕ3mv\x0004eåOàÇ^f\x0010öSm¸µÒ\x0012³Üê\x0008ê:ÓÝÁ\x001ct.ç\x0013È\x0001á\x0019\x0019\x0013\x0018\x0002äR7B®Y÷/³²tûcæ8#ch$\x001eõ¾ØÖÙöofx	ÍÑ\x001cãy4¨µ)dÞÊms·\x0017ö3\x001b½\x00180iIe;gQ
B,¼Ò´3\x000bYÇ ²;\x0008uaqs1s2\x001aX\x001cí¼<q\x000f²©»Ï))nfVÂë~bÆÛ0óJ^=ÌuÜÜoç\x001c³ÓÖ`~Á9\x0011ÂÎW{w\x0010ëê
?ö\x0012\x0000Ï«¬Xa\x00070óC5;M½Mÿf\x0016¤h\x0003óÒ Pëè\x000e(\x001e\x0018*¿\x001eÙï]¨ú7øöÈùÈO"0:#/ô\x0012¶3Ë:]\x000b?ö2\x001b9^\x0001ÇÀHèùÇÝ\x000eàz_Èþ}áÈ5tL\x001b¨\x0005d¯°»K¨yÕvdU?;ÄwØNdi²zTØlÇ>e3<õ¯\x0008ñÀ|õ\x0015ÈáVR?êA~|ï	òæuOkª-\x000fÑ~®9æTëä|ÉZù\x0004yöúà)ßàÍã\x0004ï\x000eZî½ÄîX\x0003z«©>Ñ;¤®ºMheI+;×6Ý§ãÚrOãqBMZÛ­hUI«zw\x0002u\x001e\x001bop¦;§Ë\x001eLIßV´ºwm-\x0014ÿ$A"1jB\x001f|é_\x0007kJXÓ\x000bKò\x0002lJ6iò«íÖÁº\x0012ÖuÂBm®	Y\x0012y6R´kç\x0006Úi}Ië;iA5djéÏÝµ\\x0013­ïôn¦-¦ó4õ¼\x000bW+ð	©@X\x001fËTpÍ¡®ïù¹¹í¸µsèõ\x000e
\x0019´éå^p\x0003'=(¶\x0011må\x001cxw\x00101ÜÝW\x0000ãTÔê\x0016\x0002ßvÚÊ9ð^ï\x0010\x0002H?uu1U¨i+lä\x001dxå\x001dx§{IÕ2w¨Ìãdp\x0007MÌëv¶ãVî÷ú\x0007hÚÌ[AbÅ0WpâF°{àþ\x0001¤s] ñ4QiÆ=Ä\x000cÛàÚ
×ö³©G[y¬\x0012å4tÊKó×áVþl¿Ø}ýêê\¦bò>\x0010\x0012«'¬÷Û·¼rf¼ÓñàpsåD`E­sAZç\x0001w\x001b+*o&:½\x0019F¥\x0019+±ë!\ \x001câÎ÷q·ãVÞLtz3Î¦x<\x000erI\x0016´Bôüä©vÚúªÓéÍ8´¸å}\x000bÓxQ­\x001bofÖ?\:¾\x000e·rg¢Ó`\x0018ûc÷ZÉ¶Ú\x000b;\x0013½îLh¨H«+@ %âjÔq°NmtÒ*w&:Ý\x0019\x0007wF¶.(Êã^ØÆÊ^¦=¾\x0001\x0018I"V&§AUã6¸?\x0013þ\x000c\x0004sPn´#\zµîá²üu¸?\x0013½þÌI\x0018¢\x001a\x000bqÇ*wÉQ\x001bÓòù2ªvÜÊ§^\x00164÷\x001a%1g#¨ÇÔÎÏo¦KÛoØYM\x001bâ¯\x001ck@U=)Ì5~¾±¸\x001d·ri²×¥\x0019*E2ÒÓÄ\x0004\x0012rµfþ\x0019¶\x001d·òi²Ó§	æs"D\x0007j
£1³ ­ßN[§ïz]\x001aLeÏk\x001bnYß\x0015«\x0015aªÏ6°CÛï}Y\x000b\x000b|¹¾D3\x0019S\x000eG\x0010\x0015-ëp+&{\x001dZ\x0017³HQØ¢` ÒêRO§\x000blÇ­<ìôhÁ\x0019ä;f,?ö8%p&°\x001b¥\x001beåÐd¯Cs\x001c÷áQ7-{\x0008\x000c\x0017Ô¼H;nåÐd§CS SÛø\\x0008nÒÖ
¾
{PùÃm[ëp+&;\x001dZ\x001dQU]úZ\x001aÅ«ì¼zG3­ª<êô\x0010Áæ¢ûÕ0=w¦SÑµY\x0018.Ð[ÙÜýîéÕf\x000cjãòI\x0013:P=æõ~¸\x001fy\x001dnýfÒiu!!uå)Yn\x000c5b^=ª\x001d·2cªÓééGy\x000bS1\x0000×
T53b^E±\x001d·2\x000cªÓ0@Q¶¤aª^t\x001dÇ\x00074c7Ú\x000cº\x001dugìXô½\x0018\x0010X°\x0019w¬à\x001báV^Bwz	e(Á -Í)\x0008wJ¡î¼ÌO;nµ\x0019t÷µÇAT\x0013q¡Ç!+C
|é±|~8Øg¸\x000bÚ%µr\x0011ºÓE(g°\x0005Útò àéBÉæ'@4¯¬©\ét\x0011\x001a&eæÍ1ÏVÚ¼-ßèÇT.b_²b5®Ö8¸)*Ã$«`\x001d\x0005æj£`LØRk'g\x0018àoú®Á\x001abÉ8ÄI5ñ¦æ(güF\x0001o Þ\x000b"ßu^ÖHÏVC\x00022_$\x0016\x0004\x0004û°M¾©ýuVÝË\x000cõ,\x0002ßÚ\x0019BsNÚeb¾Ã³#
9éZåDä®3û¤1ã\x0000^\x0003çYÚ\x0017ó:à\x001dÙ=`ß\x000b<Å<pþ,
>Á¬ÿÐG2ò³ógúÏ\x001fêÙjV\x0008^çQ\x0017ÐÊùÁA\x001då-ßÿz¿ûtu[9¿å¿{Ô¦Ï\x0016¼ÿ ²iÀT©ü\x001aÏp_;¶Ý¾~··¯ûì\x001d×¥\x0017\x000cªè¸è¸'Õç0ÜúÎ¡\x0016M\x000eV/?\x0016jF¢\x001cj¾£¨£\x0006j[ô\x001fÃ`7q/[\x0016µûS-¡Z(¿S	np·ç\x0006;ÍÝ\x0017;¥ÙÃ5\x0013K÷}U°\x0013þ&[íîo¯¾	ÿÉë5"QðMJåV\x000b{Þ\x000c\x0017\x0008ÏNÞ\x001e}srþôù\x0001Q\x0011ÄU\x0015®zì¸ºÂÕ\x001d×T¸¦\x0013©©ZÖ`ä¦,M§\x0016Ë²õm¸¶Âµ}¸Â;¸)¥\x001d\x0012ÊP5Áü©ÖU´®q}®\x0012Òjv*Eæ\x001báú
×?Ú­køç¤Á\x001f\x0002,ÁÿâãýÝÝÕÍõ³¦!½Ð²bª\x0016kÍø¼\x000c\x000e°¾xõæââôìùËCÂ¯T¤¢Tc~ÊrIcÎ$
e\x0016Ë3
ZHeI*»H#ùi6¥Ø%­èâfmáT%§ê]Q£É\x001d]*$\x0015EÊùÛf+©.Iuß
\x001aZ\x0002å9*VtQ¿Ó¦û4yÚ£\x0016W\x0014µ5jå[ImIj»H­ÆXãý1¾±Ñ\x0008\x0013>ßMÜ
êJP×\x0007\x001axpR«ä/\x000bKº	©/I}\x001f)¶A\x000bJ\x001eº"\x0019	ã/hQ4\x0016ÃíÁè³>TAÊéá\x001ecpf7mÓùöÛVÒÚ=õù'#Qá\x0017\x00165ÏÚ	?Q_Ï|µn+jåx2\x0016ëI¡Q\x0006§þ2:Sby>U\x000bjå xq"xúilðb*Ù^PZP+\x001fÅû\x0014Ô\x0008Y2ý4ìy:U¸S^9)Þç¥4N}6£|>u÷Í_\[1+\x001fÅûa¹¹\x0000N ¢+:P[pV÷Y~m¨ïLá»ðljÙØÄV÷Y~¥©ÜIpôQl¾\x0003¢\x0011UT_ôY~å%\x001d|YBF¡Ô|Å]+ieùEå^\x0016@\x00147çi\x0014]\x000fiE­o&}_s\x000cû\x000c\x0014&äEÅfN®·PDe÷EÝ
g4\x0019gAi/Õ
S0Åæ[Ò[Q+»/úì>Ü³
÷©<ªP\x0018\x001a%Ìæ\x001bÌZQ+*ú\x000cj8S\x0016\x001b ÐìâËcf[8+*ú\x000c*´`4á[êq`xRYY)Ùg¥¾Ì/\x0017Ùúï:×h\x0019\x000e°\x0017TFåØ|\x0005þjZ¶§\x0000yÙ¦¾¿?úûÇûÛ\x000f×7«H'­.\x001bB\x0014z\x0019Ô³ùF\x000c\x0000}öæèï¯Þ¿|~ö0¨(AE\x001f(Çü¤5\x0002ç\x0008z\x0007pvyÆf\x000b©,Ie\x001f©ÆaD\x000e5V¡q\x0008Ã)?/d»\x0007ºð\Áö\x0004\x0012RõQzj×µ
\x000b¤Îí\x0003CZÖÓ¤¦T0ì¾±Na\x0014MMÎÏ7ß4\x0016hÆè\x0012ÝF
b[\x000c!5ÞL8Êq;»|ß_\x001aÌ]}`ÒHÝºpùÓÕíÏë^ÖöX¦\x000c÷¨ôSS1÷SÅËÚå·§ç/\x000eÎk0{÷~ ÞëÞo@¶ÖCR2!ü¤
zEîpXÝ<H\x0001ä½	)\x0012\x0017Ëqm÷Î\x0008\x0017\x0001¸\x001c.ZÉ×zz[aóÂýíÄÖj­yô«ÌÍtç«lö\x001b \x001dt8yJ\x000f¥iKGÐ\x000fvA®\x0016{ÐÝV\x0003 ñ\x0000 \x001dB«í¡Õ\x001e´êÖÆ¼\x0006èT¥á¹6´¥ç\x000b{ õ\x001et·åÛÏl\x000f»ÝJs·ÿlèèÙðåÕýo+\x0007´\x001b!§4§ç4Dw1àyyúæí¡8×í¿\x0015:z+\'¦\x001d\x001böAN\x001bÈi\x000c±Y\x001eC¼O|²yùè
\x000e|Ø¢é(¡½<àw%*ñT3Þôvi¢\x0014cúíNÚ#óe³
|ºäÓÍ¿^Gg[Ód{\x0019"DÉY\x000cºVòÏ´ò)sp¬ÕX§p&\x0016Äx¶Ä³Í¿^NÏýá^«î¤£º\x000f»þ]ÉçJ>7p:GÍ&éiýìÂ¦õ|¾äóÍÛy¬*v¥_ïâ,ßuxÅÅÄM¯{
ë'¨R\x0006îy\x001e­ËVÛ×¾£ÙyTj6/e8TÐu~ù\x0012è\x0016®Énÿ
ÏMoxM¿Zß\x001b¤j\x0008Ä!À\Lã®\»ÊqðfÏ\x00017ã|6¼Á\x001eiiQïPöæ\x0001Àp­\x0003ð\x0017\x0010\x0018<ÿùÝÝ]e^ßì>|º¾º]y§àq\x001fJxµ\x0010ÈêmNÞ8iÞÎ<ñúäâ"3¯ÏN^^>?=?\x0014enYrË!n\x0011{ö"7Gû\x0003É2âu/ÜºäÖCÜ
"1Zï\x0014UxuË·æ¶%·\x001dä»'r«ÌµV¶æö%·\x001fâ6ñÅoo`\x001fpÏ\x001a>n^Ë±iª\x001bEñ¿\x0004¼:|ìdÚéd\x0016;%\x000b\x000en
^L>v4ýt4­b¦->ëõÁ÷g¥\x0016\x0004WG7; þáêÓ§l\x0002\x0007U[ç§²POiØùÞåÛ*V@~zzyyÐéì½\x0016âµ Ø¡®u&µ\x0002µWrßj1²m%%±ì%\x0016L\x0008ðÔ¸*5*~ú\x0003U\x0003­Äª$VÝÄMÏG&MqÒp»=±.u?±¦ë¬7X9.ß=\x001aMIlú9ª\x0006o\x001e\x0010\x0015íùÎ³\x001eb[\x0012Ûþ}¬±ÌzO\x001d8ý\x0000Äï·\x0002v%°ë7\x0015\x001e\x001f\x0017]p%y¬½T8\x0017ÃÏ.÷\x0000û\x0012Ø÷\x0003C.pZáÌ;må[#p1|«|\x0017k'Î°Ö[r\x001eî)\x000b#¬\x001bpÜ\x001f" ÉÛ=ÙÝ¾ûx}·z+8*Ý t¢+)_î,yrrþäÕó\x0015¢¤\x0014=µaZN>auæ9Ú e	); Ã÷
\x0013|q®&_îzYO©JJÕAi\x0015*®Ã¬µ\x001cFJ.&IÝÅ³´Rºg-EYÛ³©µ[nKSRµ¤Dp¨ô\x001bgÞ¯Y4¤ë)mIi{(Sü\x0007ã^\x0016Ó:ë!]	éz 5ô\x000c&AWC\x0016$ÇXÐ:·Á\x0011÷%¥ï 4(§®øI;Á±åÜÕÅ¨\x00029¹ ¶Å¤áF°\x0012\x0017sRÇu!ÔzÌÚõôø\x001e;UB?ÃãJ0~~Ðx¹Ð-÷¥þ%£c\x0013£ö(®\x0003æcõ½¤ªåÒ¶õKYKÞc/ Q\x001dÀåâA\ÊñãÃ+KÄ{L\x0011Ì
ç´1©C\x0004[\x0003ÃÆ|ø7þ\x0010¦¨~é¢ç\x001e`Î\x000f³OóÚ¡mÕ/]ôüÒÃ·\x000e\x0018]oüÂbûbXÍñCTNRôxÉppoj\x000cÞ\x0005lÈL9·j£¬üèq@z\x001aâ IU8\x001c/jíü¨6\x0007Ä\x000b\x0018°ï:baIÝ+\x0002rÇ)Ê$\x0005
~åº¦\x000c{³\x0003SÑ Q8C\x001c­IÌ-÷¬® Õ{\x001cá/à§?ýÏÿóéjw¿êö®\x0004Î¯·FdVz°¦\x0002V+\x000f\x0015°>ýöäòôäÍÃ¨¢D\x0015}¨ab¢!ñy¦âtÃpË÷ \x0016TY¢ÊÎUeØ¶h­Ä\x0002vé©ØË\x001dÈ14 ª\x0012Uu¢J*qQ;m\x0000z÷tóÓfZQuª»Q]Þ«!ªÏ¡¼bÓóûr×r\x000bª)QM'ªPíT\x00072må2¤\x0016T[¢ÚNTNCÈ:\x0016¸WI\x0006À/Çx-¨¾Dõ}¨r:åcôËC\x0008õPqøZR^ÕN»
#þ2©B­Ú©Rd\x000bÊ+CÅ;-\x0015ó©©ì\x0001+nH®Â-'DZX«3Å;\x000f}ÉWñã,µ­ÂE
¿Vª;\x0013¨J.,*øÎ¥õÓÒ\x001a<XS½\x000b;ÔtñðÒH\HWÇ*¸iöë}\x0008YÞí>®urÊZÐá¦çs¥¯ã¹òJûù¹\x001c8úõM\x0008[¼Z«*\Õ+ÒÚ*-·\x0001eû\x001aõ×7ÁÕ\x0015®îÅU\x001cU\çd§\x0014®îÁyç«i5/i5ï¤\x0005é5G´i.ç4\x0001g3ZQÑÞµÅé\x0006Ê¢æJÅ6ySÛÎZ2Ý{ÊÂ%'ûÀdX\x0014Ù\x000e§l£¥­Nî=eÁÉ\x001a5­m>e\x001e«mõshÇ­Nî=e ¿S¬.î[Ú¶ó\x001alí´¦¢5½´\x0012\x0013\x0003°¸¸\x0015ÔdÁ6¢µ\x0015­í¥Õ¨n\x0003k+\x0011×Ñ1×ÍmÅå¢Ú
qvd\x000f¯×\x0016g\x000b©ðé×\x000b+qëÚyq«V^QÄµ\x0002T\x0019|\x0017¯dÒcå³\x0012<Gá^Z\x001ebaÜv3¯¬\\x0004üØÇ\x001b.ãù£8O\x0007^:sìZÌ§2qU½¼ªwyÆd{\x001cØ\x0012ÃÜðÑ\x000b£.y\x001d«xÃ}¼Þcì\x0018.
¹jÌ+y.Íæ\x000bh[ye1ë"ðÂ]¼ðv¯Ô2Ë_z-Qþ2Äh\x00183iª\x0001~ìÃÕT-&µË³?½Æ\x001e&e·9lJïE}Æ\x000côoñá ¬×äD?¬æE\x001a[p÷ë)\x0004ÕSÜ~ØÝ¿"ËÛëÝ:yQ\x0018\x0019¯Ó´\x001a-*"x½\\x0013trþòäÍ3¨\x0004¹<~r@\x0004\x0013eÉ,\x0007u\x001br åÿè/üÂ@ë.dU"«~dFÝ\x001e\x000e\x001aS°\x0010g x9_ZÚÅ¬KfÝÏ,\x0015FÀÎ !KqÃ®ÞnkÙô3sj(ë5yT0&årmÉlûaOÞ\x001b*x'\x0007cy7cv%³\x001bXgOfCi\x0014Î\x0016Ç_xµÜ ÔÌìKf?°Î1ïg,Îó:û\x001c·y»äie.J#ÄT\x001aÑeëä±È\x0003\x001eU²­cÈ¬Ùfg×.eÀ§(u<Îz|ã\x000fÿ	4\x001cóù©.fQ1\x0001cÇ1_í´ 2ÏÑ@ëåòãfèÊ\x000fò\x0001G\x0018\x0016:×¥;È\x0008;|f£\x001d½üüß\x000c]yB>à
Ãõ)_GÀ}34w\x001cM´ÞÎÜñÊ\x0015ò\x0001_¨iF[ùc7nð6ÄÍÐ/ä\x0003Î0l\x000f6(s©HõÆ/$\x0007»+_ÈG¡§@É\x0017\x000f\x0007\x001a·´ÛpwTÎ\x000fxÃ\x0000eÅ\MÐ\x00119/AWÞ\x000f¸CÍÉ§\x001e¹üD.Üo\x0017*Ê\x001d\x0001w¨c²0¹\x0016*
V\x001cEð¡Úq3èÊ\x001f\x0011øå\x0002\x000fQ9D1à\x0010õÔzaIÔUa1\x0014¨QoÆ\¹\x00161àZS\x0002\x000fÜ\x001dâåºööKVõø\x0018/ZøøøèïZEÕT¼míz±¡)#\x000f\x0001rrHQÇ÷rY¥´ý*¾¿âjdÅa\x0000%r¬WÓ|~\q\x00179¯\x0017÷/8Ü»\x0014z\x001a1)\x000bP\x001cbk\x0014;°ßÕØïú±5
ä\x0013Ç,\x0013§Íü(Í¾ðip3t4¿@\x0014%ÂZW0üE4S
òÛÝÏW»{ø'èi^\x0001Îµ\x000fÂ\x0000Î`DetðV\x000b,\x0017\x0013l¾\x0004sÊE~{òâôä
ü\x0013´5?¯+|=\x000f/mÞg\x0015Ä\x0000ï¯Ïg\x0018ºé)é\x0019¤w\x0012\x001b0`ñSU©ÕÊÑâ?eo¥w\x0015½\x001b¥×XW\x000eôB%z5\x001b[Ó\x001bYÒ\x001b9JOuÜ°uR+ÕØæ*¸zà)¼ÞVôvÞ0~,ÕD7>?9\x001aýøÕÖ1[ÇÊ®ülãã­BÀïzCz^\x0012ð¿ÁcøÆ­ÅöÁz\x001aÁæÕûñM?hvâ<øiõOø\x0002Ë.\x0005W¸ïæWÍçjÐèCw¢Õ´ùS\x001c\x000c£qû,;éçw5ÿèîO%c¸þ©Ü\x001a,{\x0014ì§àFz]o~=ºù/ÐÞÓî¿ôóÛÔtzj³ÑtæÝã\x0014Å\x000c|SÓÉµ¯ùý(¿G·k\x001cæ\x0002ÿ¶ëojëcF­O¸\x000eê"lÈëï\x0005mÿyåên~Ë+~ËÇøa\x0006 ¬\x000fÏÖÓç¿\õãË\x001a0î\x0001e9m$`-ÞTÄü\x0013s?}}xíàác§ÙL7rPÆß_ðúºÂ\x0007]Õì\x0018÷ËUw\x0016ª×è¶µ-¾¨l?ü8Ï³¾óÞçTµ\x0013þÆ«/ë»®\x001c¼ì\x0004n2\x0011?Çm\x00164fS×+tuv\x001e=»©í\x0000·O**´Q\x0001o\^¹a\x0015¿a£ü67'ÆõOÍ)ÖÁ³aäç0\x0006nC~å*ë\x0003?\x000eòk¬ÛëßÓµå¡Õø|¯!\x0014\x000cÏÔ¸ôúãÕJ-'K=ÕQº'çç%©¡C\x001d+¯_\x001eÔ\x0018âû\x0003-xÙ
º\x001e2ì,\x0004úM¹\x001cGiÌx¦\x000fµ\x0001­¤T%¥ê \x0004	=K5\x0016¹±J\x0019K	zS\x000fQÎ·*!¢.\x0011u\x0007¢áT\x0006ÂiÌ\x0012(ë@Ö/¤+)]Ï4Øî¸,FÚT\x0015Ä[ÓWS\x0016ÂW\\x0003a\x001a0%et\x0005ÇI¥JaM©\x0017ËÀÖcVg÷\x001c¿n[[tmàZ\x001d~5Q8,ýïþ×·ÿóÿ~ººÞ^ßÜ¬ÄSø¦l!=\x0017#iNõ|/}\x0011bGß¾º<=|ûüììRsþ\x0004Q~Øà\x0013\x0018Ç\x001b¼\x0015~zÒ"\x0011"5_~>ð	²ü\x0004ùUþ\x0016Tù	jß&o¡§zY\x001a\x001e°ý'èò\x0013ô\x0006\x0010\x001e\x0005-Åô6jiÂ¸0ð	¦ü\x0004³Åoîi°çØo\x001eü7~Â|>bà\x0013lù	vß\x0002'AÆ°§LÞHVÐ¨çùùOpå'¸-~\x000b\x0002ªäÌ= Ks+ç¯6\x0003àËOð[ü\x0016ÇÅÁU¤¬,­¢Á«óu\x0002ýPLg\x0000×ÆÆ¿\x0001äl,J;jR4\x0006ó±3¯½ó\x0016î9\x001c\x00062*O¿
 Ío
|Båù&îÙÞ¢|¦ó¼¢\x001eøÊ=ó-üs8
\x001aU»ü±h4Éam½*ÿÌ7qÐ4DA&\x0006=ÉÍÍg\x001b\x0007¾¡rÐ|+\x000fÊO\x00064\x0015ê&\x0006ëæëÅ\x0006¾¡òÐ|\x000b\x0017Í5M
#Í1Ö;¬L8ð	æ¸è/þk¨\4ßÂGð\x0008Åj§ºTiè\x0013æ\x000bñ\x0007>¡rÑ|\x000b\x001f
\x0003²UR67ZÂÌ\x001fÔ3óåBýß *\x001f-6ðÑP\x001e
² í_Eµ\x000b3Û\x0006¾¡rÒb\x0013'\x001d\x0013eIßO`\x0012Eb^ÏÚyåþO¨¯Ð[8é\x0010gCÉðkð$©·q!*ÿ&¶ðoBÒÖ\x001e«ãÃoT\x0016çi\x0007¾¡ò
b\x000bß\x0010v\x0012C¥H\x0005Ñé\x001bð\x000bæÇl\x000c|Aå\x001aÄ&®Abo½¤\x001d\x0005ÔS·~~Öò7\x001cÌÊ/MînN2ªØR\x0016NòìZÿ/@V\x0006UnaP%IT¥i*¥øÂÌö\x000c|Ceä\x0016ÖH
ìÎò(Ôòu$$o6ÿ=TæHnd¾àA`¢¬¡NUø¯/­ÇýT{#¥Ý\x0006;JB2,\x001dlÒÚiÝúò#Eý\x0019á÷¾Ág\x0008wÌ1âc4#Ó\x0016·/¶\x001bI²Ö¡7ù
3~ú\x0004Li8)7srf$³¡Û\x0017»ÛO×\x001f^ÿt}sýËªdµ4]ÓYÒç\x0017<¦^Ô\x0017qr~ùüåÑëo=ý0¯(yE//(Ûàt&«ñ\x0003¯&Z.6\x000b6òÊWv¯/Ãõu|5_ÎÒÁ«J^ÕÍëh.GË1X\x001az(_liäÕ%¯îå¼Unñ:W\x001cÜá±Ñ"ÛðÚ×vóJ|¶Q\x0002á`&ç_¦\x001by}Éë»yI³\x000böÅù\x001dFu-ë'·ñ\x0016r3=§w\x0000[Hd¦
a¦	¤#Ä\x0007Î5\x0002×\x0006¸Û\x0002øe`!P@hEóbùu½\x0011¸²À¼Û\x0004\x001b\x0012!tl\x001a<ÃP£Ö/´µt\x0000W&?~\x001bÌ+\x001bÌ»° wó\x0017%^|\\x00066Är3/s±/.ðã¢\x0010Í©ùÁ\x000eÞÊ\x0006ó^#\x001cþXcç¸F¹\x0012®±!ÑåþìF`W\x0001»^`HGg\x0013áQô;\x001aã} »¹WTFXô\x001aa¦åñ´\x001fòí*¸j\_µ,\x0007ÓÈ[\x0007½&AÍIË^Kòr|Y%¾
XV\x000b,»\x0017Ø\x0006³\x0016BcbO*Aj+/'YqSJÈ»ÞM¬Q.<\x0004xEâ\x000eGyµ\)Új&jæ`(z­Ä66«°'0c9®3ó==®cjrÏÎã]§÷4Ã\x0005GC\x000c]\x000eHÏ53ïö»×ÙQ}®¤Ia¯)È®c^(eûÅÎ,Þ§JíÕ­Ec\x0011\x0002M±ÜIïÍFÎW\x0012O\x0005Ú\x000fUïW<³x[î!Å>\x0010\x0005J\x001e\x0013/rf^'ª\x0015Sª\x0007ÓÂX³,[\x000bÝÜ0áqì~°Ùi\x001d©.Iuïf=ààmn£4zð\x0012\x000fô5­\x00035%¨é\x00025T^£¸ÏµfÖÐ@h(sÚÔ¤¶ÔjXÈDj¨ÑÍa·\x0006Ì:ÛÔ¤¾Ôq<MÌaG§ÏFÕ°´ÁWÃÓ%¸ÔSJD¥gk9'±Éiâµ!í³¤Î \x00162Øéb<Î²4â!yu¤!å}Ô
\x001aÅ\x0001ù½ndó`Cã*RQýîE×ïÞ\x0006\x000b*Óï^KK4­¥9fAµ®\x0015µ2¦¢ËZ© n¨\\x001cãN
V4£.¼5¢jUMßªJöTK\x000búX©§\x000f×ô!)U ®\x0002u} T\x000b4/z'ñ\x001ecÌü³V+juú]×é·0D*¢è_XR\x0014v1\x000bï¹­¤áw]?\x001c\x001e¬\x0019ÖeEVhH%Ô:RW¡úÚGu¢x¬fj:S\x001aÏÞ"8åµ¥â¦K,
	ÿæ¬ \x0016,\x0015íU©6Ø«ÜÖ¬¶Ï¥:Q`\x0018¦8Á\x0013Á\x0016¬¦fí\x000bþ;6\x001c?tª4}g~ty\x001b¨`{®ªoQWÍ¾JÂ\x0010Á|¢No½%jd\x0015²b\x0015²Up0\x0013Vä\x000c\°VØ¥ô¼
e\x001b«¬ìóV |\x001f\x0014@;Ó&' É\x0007KÉ¦\x0004­aUuô\x000f?v°jo²¶\x001aêÄ\x0014¶c¨\x0007UV¡\x001aUô¡:ÊÐ¤²Áê\x001dé¶XU]í\x0000ø±\x0007Õ¨cL+\x000c¶O¸\x0010«[¤yHþd
«.ÚtÁz3×Å\x001aâ\x0000B\x0016NVás\x0017,n#\x0005ÍÒ2\x0008]\x0015.)YÔ\x000b,&µc©Üæ\x001aàXYòcAøÇ\x0017\x000e\x0006S³_\x0012GÀüvõ\x0001z¯î \x0013x\x001bþ3×W·wkòRO]rCQ\x0010ä\x00015NTqj>\x001dpòöô%4\x001b^@6ðüÕËÏOÏ/\x001e\x0006\x0017%¸\x0018\x0002\x001a\x0006fDðp[ÈÃ{5æ1O·õË\x0012\\x000e{K³Ã7ä	Ùá\x0016Ýdj>WÔK®Jr5D®\x0018ª\x000cYÁñá<ltj
oGì%×%¹\x001e]ó<JÊÂ,õÏ×|6è\x00057%¸\x0019;Q\x0010wyÑ\x0008ÏÒ6MÓ÷»Ü+hÌ%ÐÞ¥ÉÎ2OÝzówø^p_û!p1ÍZ.g\x0011|¾Ï°¼¬ÂIóbFÐ\x0019\x000c\ÇÆóüxf¸§Èy­^ôÚ

ù!%QEÈ+)ntC
îÁïoyDyåø'ô4®:è/W@·\x0001îE¯\x000c:\x001f²èJkìl¶iÉ{ÝPUö¦®W\x0006\x000fYt¥C@
zøÌMÅ¿j^r­\x0017¼2è|È¢+ÃQ\x0006<»"ciÁ··Êò4e\x0000Ü2\x0014"mnó6wøb¼¤§Ð^¹"þ\x0015ù"QYt1fÑÃ¢|Åêkã8¢ÏO\x0018í%¯Ãó!«¨%´]Zs\x0001[>.ºF)\x001aëÝ\x0016\x0006ýw¶÷|ÿ\x000fïÏ>~º¾»»úùêÃ§£«£ó?ütu{ôþÿó¿^Ý®àgPÉ\x0015PR¹d-XFì2Ï^0Î^]>¿¸8}qúòòèìôèüU¸Û\x001f=;zuþð7Èò\x001bä\x0016ß yÎL*5¡Ã7`¥«\x0011ó­#ß ÊoP\x001b|äZQÜåþ'c$Y\x0006#ß ËoÐ\x001b|\x0003óÌTLæ±xÁ[\x0019|tÏ»|)?Álñ	^dA&}öØç®ý¬!\x001aù\x0004[~Ýf'å÷\x000f	B¡:ï$ª{ñó\x000elä\x001b\ù
no\x0008aÍ\x0013Ó\x0019¦ðáéÎÑ¯as«äËoð\x001b|±(\¡ºàø
ÐV¿a~¾ÇÀ7Ð%+~\x0003\²Æ?\x0002_S\x0015×ùÝ/|\x00036Ð\x0019è/Ùø\x001bxõ
|oÖ?z¸Ê¾!¯¿À´òÊMó-ü4
ä\x0019÷á{xöqJEæ§9u|C°Hð\x0007´]Lñ7U$\x0003ï~¼ùøó»\x0010#­@\x0007a)\x0014Ýëº\x0007!l~j\x0005dó}ú\x0018"½9zúêìÕ'!@z\x0008\x0017£t\x0003t\x0014Ôþ
¨½®¨½þ\x001a¨ç%5üø\x0015PKmJjøñQSý§\x0010BÎóuåòêç_nÖ^V\x0004S8~Áj9?Iý)Î,\x000fµÊåé×g¯Xbÿ\x0005D¤\x0017>^®IQY¨@É¢C×óo£\x001d¼²äÝëí)ÖÈ<HMjN¹=¹ÕêªVu¯.Í#°Zì¢ÅW<·P(×Á«K^ÝÉË=IuXËq`§TØ­ä\x0016jP:xMÉkº×7o]m!¹¶®££¶<#¼\x0011Ö°¶{qÕ¦Æ\x001f©p!oÄëJ^×½¸RºP:ûÙúnwØ|Éë{×\x0017D\x0010òú:g\p"¸y\x0017ôMÚyRïüÒÒiË<ÉDCÙG6f~Zß­x+WÁ»}\x0005s(\x0013®'$å«Ix¡â¿\x0003¸²¾¼Ûü2MµÖäYH\x0001X­O\x001c¯Ì\x0019ïµgÜ;ìP²66\x0012g±d\x0002\x001bÙ_^\x0008Þk#@Ð\x0016'HÀ0¼ÂÃ\x0017¨n\x0000fFÔá\x0019È\x0016\x0014uË\x00019Ä7×\x001f®Ö\x0010KhW\x0003]9	ócbá\x0007J§\x0008Â\x00083ÈÄºÀ\x001cBÊ³ç/O\x001fF^©"²\x001ebV\x001a3°\x000fV\x0002µ\x0010OÕv@\\x0016Ûµ\x0012\x001b\x0017|@\x001cÜHj\x0018N@¡õ¼¦h\x0017´« ]?t\x0008Ñ`~óls¥¨W"w¹`ÿ\x000e\x000epi6Õv6\x0003ûÙÄÙª\x0011Ú£¤´WÁfdh9ï¥{ ,¡\x001cXi\x0019{Ç\x0000Ú
\x00089ÓJk¡ùá\x0006\x0006h^L³SXÎ¸z¼ûëÚÜé
ò\x0005©me?ªqn\x001a\x001e
jøñ+ VZÔðã×@m+\x0008?~
ÔUÔ}
Ôºö1zÄÉ|AÏ(Ü¤L\x001dú®;\	Ê\x0013Ïñ´W¨f\x0012b§Ãc¼Wq\x000bé÷*àÉÕ¶ïüú·ðçûû£·W·ï?®+¯\x0017\x000e»\x0016\x0018\x001dI5ën\x001aÅ)\x000fÖ×\x0007öóçoÃÏÞ\x001c½==öêPýzú\x0004Qø
?¡èÃO(û°¾OpõoÁ}}¿\x0005]$t çù¯ï\x0013$¯>Aò¯ï\x0013tý	úëû\x0004#ªOZ² M~ïp^º\\x001d\x001c¾\x0001Õý94¬lú
VV&ÉÊq$uÆwÎ\x0019¨\x0018Nß­6ÍO(èùpé«\x0017 ¹<=Ü\ý¾ûðþöêèÝ\x001fk\x0012FÚÐ *\x0010ÛÍ]BÖ+ªý<XxrvúÏÎO¾9ù·\x0007©§\x0007ji\x0006°¡\x0017\x000fÉhDcÔ°r¸¿
{j%\x0005lÃF°\x0005ö½YÔé(©ÍÁrÕ&jÎ+jÎG°DþL®ÉvÌPðÁì6lUílø±\x001f\x001b\x001e|³z\x0017¼¥ú¼·Å¤õw¨®¹[[å\x000e;ak»ùá¥\x000fEAc ¸\x0019vÙ"èðW#\x0016%?«9­i³ðI~l=ÎØ«\x0017"X~¼ÿ\x0014Ç/\x0002Ñ§£ï®VµwFUH³ÐÌáC«wt1±ó[åüÕË¨9~\x0011~¼<úîô`§ØKê\x0002´ø: ¥,¡¡ç¹\x0013khæ%©³\«i¸?9\x0007½4ï \x0011«X=~bUm\x000cõul)\x0015\x0003ÐyüÐWÐÑ7>~jÐâ¬&xD\x0007óx7¶Ü×§Ó¨ô«£ÝÑÙîÃ§«Û\x000fë¦uBp=\x000b\x000c\x0005Ë0\x000e"k
Ï\x0007}éqóèì$ü¿§ç/\x000fM{Ê@lº­A±à¿³ÔÔWíÙ|q}\x000f±-m?1;V\x0018ê1£.9	\x00035\x0010mÀ®\x0004v_Ã¦ð%±üK\9©ºG¼ÆEç±&\x0001ô,²ÅVìÂá&\x0014Dñ\x0007#XÌOñ73½V]\x0004Þ£ûÛ«uSo8\x0014¼c\x00087®Fp\x001a¥õÁäøEà=:ys~zpâMb\x0006=ù\x0019~ìôr´áyj54MÌ¹ù)\x001c=ÔºZéxÇê¥6\x0016
3\x0014öLí¦1\x00062gmÐ¦6cÐÊ§Ô>óA\x0019â&f#+f#\x0007¶CuukãèÂ¬LFC\x000ej=5QûÚ÷SÃ 3,eÌ*¹õAA½\x0016jQT%\x0005jQ%µï\x000f\x0005]&\x000ft²(¬«Ñ±Ì§iz Ee?\x0018°\x001faS£Æ×\x001a0Vµz\x0008¶¡eJ,\	\x000bMàæ
ÂIlÙºIÈ!<ÛlHQm\x0010)ú7
7\x0014ùq\x001aoN¤£	Dþ¤a\x0013µ¬×Zö¯µ1¶u\x0008D\x000c*Fz(Á\x000f=\x00114QëZì\x0010\x001dÚP]î³|°¢ä#Tê¡^(#uñBÙnø\x0018\x000est *µdµ¢y9\x0007cVQïÂæ¨*HO »\x0004ÞÕÝõû«\x000f?`ïêîèï\x001f?|Ú­,,à\x0008\x0015UCxnL
·oRS²óõç§\x0017Ï¾|\x001a"¾Ó£¿¿zyyr°¸ØEÉ.\x0006Ù)T
ì\x0019\Nàó5Ü½à²\x0004àâ\x0011©¡{9±Su´Y(6îe×%»\x001ec\x0017´ @.3»\x001dAÊ!z¾Í·Ýìf]f¥O\x000b¯1Y@U2¸õÂð^tW¢»Atz	å\x0016npÕå|ÒîKt?îQM\x0016FZ\õ+p'9*É8²1tÉpR¢I\x001d
\x001dý¾×0ídç¼6ì|Ð´³©Hú<æ1\5qV³óî¿\x001e\x0014Î¿¯:
áY³®âl\x0002×Ð¼\x0003LÖ7	.Ô\x0013øAã\x0016h®\	
?vc\x001b¥@\x0004$½\x0012¶1\x001cÃ-ó`5Ãznc*nc\x0006¸Äì\x000bÿZ¨Ä»ÃÚò-ÜBë\x001b~ìç\x000eb¸D\x000c\x0019#¢t :<\x0012a\x001d¶\x0010ûC\x0004
:\x0006\x0015ÜûUO»,DX,"-f.¹ä4\x000f4S¿9zýæÀ.\x0012ÊP6\x0013¦\x0019=)\x001bÅò
\x0007\x0008)2Ë\x001df+	uI¨Û	9M\x000e÷ÝÔQ\x0016n04\x0014x9ù»Ï|¦i\x001a@©%¨$@\x0014àó\x000b#\x001aZ\x0008mIhÛ	)¥TN\x0018ä\x001c\x000fº8Ð\x0014½Ðî1®¡/	}Ï9É0;YãIV4ëyþW\x0010.L\x0013ûÃDñò°OÂÑÀVgOë\x001cý\x0015óÚ\x0014¶ÛÂ¿þw\´	iÈpË"r\x001aðnuNk½§îÕåQk\x0011+sÍ»ìuÆ\x001ajçX
³7ùöª"Tí>Ï\x001dO¾<\x0003KMá~¾Æ¶°r(¼Ã£üÅg¹2¼Ý\x001aNS¹ÁãÑ\x0012\x0016så{×,!W¬67ðs3¤\x0005Üô{&
T.q\x0012·ÏB7E6Õ0\x0018ÝÄâG\x0013à0¿wbÂ_'&µë´Â\x0007RJ\x000eÎv*QÜS|~~R\x0006Í1íay#¿7y;òn^\x0005\x0012
\x0017Õ\x001f\x00147ô¼¶<;~%¯°ûÂF6	\x001baùÎÛÝÍÕ»«Rµ\x0002¤\x0007 tG3/Å\x001cF\x001aÍí|¾\x0013KwÞ¾¼xu(¹¸¶Äµ½¸\x001a^,QdXcÔ\x0006¶ôçýe\x0007±+]/1\x000cÿq)kâ5Cµ
§³û4á¿}~\x00077\x0013«Â\x0005\x0004b\x0015}@\x0017³\x0007­ï¸-\x000c\x000fAIê¯\x0013&?KKüÂìßvd[m8¾\x00139X^­ÌÓ>|ø,§`Ì¼Ì_;²Þã¾ð²\x0013Y\x0006ÿr\x001c\x000f\x001f\x0001ÑIÇ;sÇ-iµ"\x000bV\³ 8mY'³\x0002é+\x0011¡PÁ\x001cÃ:{æM\x0012\\x0008\x0012æí[\x00034ÛWncõ\x0010û£§7\x001fï\x0000ýiøëãÂ\x0014Â°\x0004pñËé¿lou-$çÎ^]À\x0007<
_òüPkÍ¾\x001b«'ÙôÑ\x000bÌ	\x0003Äò¤+Ã°hC-$¼ûéeI/Gé5
Ã\x000bãqXk,NÎKP]½\x0019ÛjãØAz)0O \x000cZ@o4\x000eoSó:ßÝøÒWkï\x0007ñ5G±$¡\x0004\x000eó6
mJÌ?ivã\x00179M¬Ó£ø\x000eß¿T¹0\x001a\x0002\x001cP«ù¬}7½­6¾\x001dÝùÎÃGú`8i6>\x000fJï7µ:|Ïf²Q«éL~¬\x0002|G¹p<¹`'¶Ä/ê&â\x0000\x00106o\x0015Ã»\x0003Hp)\x0013ñåìa7¾q\x0015¾qøãî\x0001A.ËÇ,¾\x0015J;_ÉÙÍïêåw£Ë´&\x0013¿À±ÖÑ$ÁùËE/~1\x00035º\6ï©ô{åà­ãX ç#Ê~|Wã\x000fî\x001e\x0007#1eÆgXÆç\x0004LJ»­ß\x0012¼2ðã0®×âÞc\x0013ø\x0010'í|Y7¿¬×_®?§Ò\x0010Xÿ´ù\x001dIèI»­í\x0014ªÞýjp÷»ip5wv?\x0006úZmCN¡êí£F·O¸¨<ÅÔ[¿\x001cùMÂõ¿]uó\x0017oÐÀoÌ ¿41Ö¹Ü,\x0011l'^X¤9<\x0008ªßÕëïF×\x001f9óòÓ|n/\x0018-ÿÁîã\x000e|_ã\x000fÍÎ1Z~¯ò\x000cÀ¯5ñoz|%¯î\x000fÞ\x001878]C":á+ÌCK³íòC\x0016¾Â\x001f\~\x000f/²B\x0007®ëæ·I³mà,UukjðÚâÃÇ\x0014\x001dRõKøOùéôn\x001aûHåjþAç\x0005JÖGäíï\x0018Ç¾'©·u¾ÅõÈo\x0006½×qÓ ~a\x001c%\x0003ÿ¦Ö\x0013bÁß\x000e\x001e_o\x0014íÿÀ\x0015ð¸ÿõ¼m7¿¯ùý(¿µ86òçý¯(zÐÇF·ó×	+?è½<Hó\x001a:¿i Wà§às!7ÛË¯jó¯\x0006Í¸û(âw2\x001frÌbÂ0¬ÿ¦çW©_òÃpÀl?¦Ê
Î4ñojÿ­\x0012'ðã\x0018¿ÆÚj~òÄW® ó¿iôPèã%ü±àSÎ3f\x001eEóÃµ¥ã»­ûWí\x001fêó\x000fc+¥£|rÌz\x001e³\x0015óí\x001dü².	ñ·Ri\x0016:ìn½_÷¼)°S©¬¡%1S«í\x0003\x001afÐnüääüÿ¼9ô¶"ë)Wuó\x001a(°J)\x001eéLNpÂèÔ¼ÐÏo.fW2»~æ°£sã|órÓóRbJÙÍcîaVõ:÷/´fK\x000bÆ	ëÄ,£Ilü°\x001cx\x000b³©Í\x0000³ÁyÊúc74W
¡ç'¹ô@\x0017\x0012Õ [aû¡¥Ç´Ò\x001eäq#´ÆÈE»ù±´\x001dÐ¥¶ZT)`ýÔ\x001aµ\x0003Áp`¼k¡\x0011\x000cmÇVûsUS\x000fljípx1y­¡*3SÏ\x0017ï¢v5u¿ý\x0000e²ì\x001cUØ,6Å\x0001¨ç\x0015z¨]½ÖnÄR\x001bÐ'Ô\x000c{Ñã\x001c\x0004-ÍVgQÊÀÝÐ Ï¨³{¡²IÏ­\x000e#TáÔvÀÁÀ\x0008ñì\x0014Ã=4¥N¨,;­vµ¬ã\x000eø±©}.aÑ³g\x0008pæêCâ£-Ðª\x001eØÔ_\x0010Ú×Ð¾\x001b\x001aDYò¼\x001es+Þ¡QVmµ©Ë´\x0016P+ÝO­\x0015wÊ\x0010¤¦Ú3ÏIJoæ\x0017¥©×Ú\x000c¬uºü&jwg\x001a»Ð6\x001bØjm¾¯:f\x0018¨\x001cýío·»ß®nïÒ\x0015æ§Ý§«Ýý\x001aæ°}¡®*\x0015:ÇP52RW\x0010³Èçáör~n/ß\¼y\x0010¹\x0010
	ÈPJÑË\x001c6²Ff\x0007\x00039é\x001dõ#©Y×\x0005m+h;°Ð$RÝ<$S15éX3+³\x0017SÃûg\x001eñþöæúþûv\x0005óØ>g¬Ésk¨eÄñùé©õ~s\x000e\x0003º\x000eíêD^¸Åý¹Wl!W.\·°[ÞæQ6ÙX\x001doæëJ»ÈyQ\x000e\x0010þkáÇ!t\x0006\x0015©g¡\x000eÒÓPÊ\x0015wóµäE
äGØMäÖ\x0008\x0014¹7OÃJç%ÌúÐ\x000b\x0003è;&tlÉ¢ÂA)ODn\x0012º^ásÖ¢ë\x001a]\x000f¢\x001b\a¿HD×ö¯Ø0®2/ðã\x0010º]"(\x0006ÉqÑí[ûJr1µ\x0005\x0000¹`]ÜÈ5#å;xþOÎSSËv»EÈÊº\x00089d]d\x0008S°«ÁùTU
?Ü-^<0¡
Ý×èWMèVÐ0Î`ÞU²é 
Km´+2\x000fkÑ]îÆÐÇD õ\x0006Eå¤RtP[©
½|à\x000fèñ\x0000\x001djaQJS`yE\x0008ÒqÕÕ|\x0019~\x001fº¬ÌCæ\x0005âðl^\x001c×¹íÁB\x000c¢\x001fT\x000fkD7Q\x001f\x0007ÐW¸×]\x0008Âr9¯\x0010h\x001aý,êq¼\x001aËØ¾èð\x001e(<R!IÔOÉÃª\x0016-èW¶Q}×lAçVD\x00045÷¦EgÖb´×:èC\x0017ÕªÃCè\x001a_1¡tBÇ¾d9_Ón+Wª>Ï·¡3)ò\x001cÅò¥f[yP%´\³Ê4êÏ³XMäÆbé\x0007ÊäK!uBµ&=»\x0016½¶êzÌª\x0003z¾ÙEtÑí_.kt9®Q~&3\t
`¶3ºöFzÌ\x001b\x00017w\x0013¸Fp¹=¸®\x000e(ü8\x0004®HyÎ³ÜT\x0005ùÎ|>ùvFQkW\x000f%\x0001¸b]ïQ©\x0019IFÑoêªÁ4Ù\x001dÁ_
\x0001rRáÔRÅµ¡cúÀ°ñu_À÷û¼yêó.\x0014¢^ìîo×
Dy\x000fM%\x0011ÐÖ_ciN\x001b=ðØvqôâäÍùa(d\x0016%³ègñÙ8©å1*C$U+\x0007£¥·b%³ìgÖ\x001ewÊÛ\z5¥ø|á\x0017³*U?3·ø8\x0018|Þ\x001bÖOãÛ¢\ðFÌºdÖ\x0003Ì\x001eêòP0\x000bú\x001f0¯%\x001eÆ[MÉlº×n%;6Ù`@èÙî\x000cÚÙ\x000e0Ó-Ù V%kç-§ýüÀ}­ÙÌ®ÙÒ\x0013qÔøç\x0015.3P{p-2/¦yyÞÚ\x0004í\x0018VC\x0018Ç¡Ë>AcÑcó:K=Ô¢ÚÐ\\x000clièSÉn%Ùºpa \x0019\x0019¶Ù(\x0012ËXõ\x001b\x000e'
Öæ\x001b­0«<uÖX7ßØ×Cm«CÈíÀ1\x0014\x0006õK2¹¢×:ªèµîdÕzjÉ«\x0003~ì¥¶ãe,\x0010\x001egõr#Mm,\x000eÙ\x0006ZW[Zêþ-m`ô ÍÐ¦zXl~°\x000f¥4\x001b¨MeñàÇnjH~LÍIàVc\x0004îîÛ@+^-5üØ
\x001d\x0002\x000fÎ¢\x0011h¹Ãc\x001eóÿ£î]ã8²üÍWÉ'ùýbX%Á$2\x0010`ãBû×ldI2EB\x0002\x0001
\x0017JÔª·ó\x0008½e×~Þ@oÒO2ç¸\x0013\x0019qÉ\x0008Ïì\x001a°Ú:E TÒ\x001e\x001eîçú;pËìÚ7©ËßE\x0014\x0013!A\x000b,a3¤m«x¥±\x001aqOÐªqì\x0019U~ìY0HfÝÂG\x0019%m<¦ÖÛÇS&uù®¶Ø=Eï"¶Ã\x0013uÐ7ÈbÝ	Ô¦qì\x0019S~ìáYGÅ2\x00165ò	b+;Ï-îù\x0004jßð[ðÇbj-ªµ6#gVpøÉ-ÖIûúç÷;û}18Øx|ËXÉ7ºõÜmçÅ8ë4ð\x000fà\x001fÊ÷IÄÎdÞ'¼â.¬÷ÉÞ?\x0000_n/ó¿2ü,¬¨ê8^`ÕnúùðíÍ\x0012 ÿç?ÿkþt¿|?r,	Þ\x0001Ôæ\x0005J"¤ÃÄZCRêÚn×üíÉ\x001cq"ÉüEs&IµÆrC\x0018\x001bÉÔ¦Î\x0001éOw_¯\x001f7#8ô{×Qò]ÓÔ94ÓI »»§ÎÍ~:{{|9?\x0019Ø\x0013r£m\x0005yU1/j¦\x0013¯JÃ@\x0013/º \x0014>pý"¶xuW¯/ØGTaHÖ\x0006·òhM\x0018\x001cê7\x001e×ÔqM1.jÇÒò
I\x0015<a=\x001feH¨ºÛ3\Un\x000eWáªSÖát.ñ¼u}µ¶ãX·.­«ãºb\\x0014ÞSUP4\x0007dÀÕR\x001c\x0014\x0015®_®s\x0012¯¯óúçÿ¦Å:o,çU|Á¡\'uÓÀO+÷ó¦ÉÆòÊòõµO\x0006Bu	78V\x0017UÝý\x0006yh\x001c¼¢W°¬´Ð\x0007V\x0012¯®âã\x0003êáÓ¶ocftÚÂêpÁ®\x0010U³T4c\x0003vE5\x0017Qu×OÇ¶Øv'ìÿõOÇk\x0019üF^ödùm\x001clÐê@f
W¥%U\x0008E°ñóÉæ°
a[êÝ\x0018VSg5e¬8\x001cSU¬9¡\x0016¥¡FA`Õ[óÞ£X]Õ\x0015±z8!pdcbõøÇÜQ@Ý\x001bNÁ1ãYC5\x0014²jÔqÏ¬\x0006­Day¨|ØÕ\x0019Z\x000f\x001d\x000fÕ>\x0013XM\x001a\x0019¨\x0015uü\x0003«gÖíÍÏ£X\x001b¯,{·¼µ\x0007´]
\x000f}C!r~µÙ\x000fkãÕeï\x0016xi°rU4X\x0019`Éç\x0001X»µw\x0014lãÝ¥/K)\x0004«Ió-
G3é\x0000v{â\x0018XßØ±¾pÇÜ¨S]j\x0005\x001b-m\x0003ø;¶V¾
¶q\x0012ØBXz]4÷
ÅÑ¢\x0014¤Há´\x0019¯=\x0016V6¯\x0003)
/\x0004éRüL§Yª\x0014\x0016ðO$\x0001r½-±4¶>&>æ\x0011s%k\x001bsj\x0006iµ¬Tô%YaN»í
}chuVÑ\x0006ÌÒÚ®/[E\x001e\x001a¬íö¦ë1´Ím+\x000b÷-²É÷EÚh©"¢ v¦5¨Ã¼\x0007ÚØ¸nÓ°è\x0012Z¸p±(\x000bCM"\x0012*t\x0019½\x0017£K©Æù?ÑÆ\x0016\x000b@6Rò\x0005h\x0007gf¥ÕMû@\x0017\x001a\x00081kä'ZgÈi*¢ 3~»ÔÈ\x0010í\x0012lFiÆBc´íÇ'Àý0&>\x001a¢áa¼\x0012Þ7"\x00185gkáÛl6ùò
x¶Ó:­)§uzMKå\x0012cÙ\x001fl¨ÃRØJê"ÁR­aeI Ý2£y,m¬ÓÆrZÒ\x0002H´\ÔÁSv÷F+\x001b\x001bA\x0016ï\x0004\x0016üFZÏ²rßÛVº\x0006­+¤\x0005£FÑV\x0003ªáL ªNéé´¾Aë7­RuZ¥Jwç`T¬\x0007[K7tßà¥É¸¶kKq×¡"P\x0003ºO*Z´s»}²é¸«Jwn¨fq#\x000eÊ%\[án\x0003=\x0016·±uUáÖ\x0002oXÚºóÑ
·g\ØX\Ø\x0005¾\x0019MRèù\x001f\x001e\x001eùº|xHÑºë»²óU}Æã*¥8ìa­íÖ^=~óv~qBu\x0017Çg§}Óì\x0008Ô×A}\x0011hô7s\óPy»Ö÷Ü
 Û\x0016u]¬\x0018Á~®«ºnªERì©-YV+¹áÝáð8Ò\x001eÕ\\x0013º'!O]UÓXUS¶ªð©m\x0006\x0015\x000bµg]j(ôÞvúbSYCãµ
eï\x0015Ü\x0003ÜçÀ?÷tf\x0005.\x0012ÇJ}ÀFYÅ°D	¬2<¼Áa
"U¦\x0002-Á\x001aÛé\x0005_¦ñÇ!¦
ÖÙüËòöãõê~\©¤\x0012,¡b\x001c\x0007ê¼×<+ÆÉnÉÖ5ñÅlþf~úòxq>4y¸U[íÂ
¶\x000cÕá\x001bkø*óåì®\x001a*äÖun½Óz«\x0003EÜNBºGå]Âî\x0016h(Ä6ul³ÓrÇ\x0014ÏMË­ù*öì.N-ä¶un»Ór\x0013´\x0013X \x0017ó.ÍÊÙ\x0017ô::ö¶ØZs¥§kÜ7ÏV¥\x0013Ý"eÜº±Øz§Õ6\x001eOÌ-°ï+qWý»nÛQ=Û6ÖÛî´ÞV³8ÑR+À\x001déØ¶±[× \x000cÜ5\x0016Üí´à`À¹J\x0001|ä6R\x001b»[\x0002¸ëÊFxéV<ò`j\x0003ºËÇIÐ¬\x0017åþÀUãôÆ\x001fËÁ1GàèÕ\x0014Ì<0î¸åØb\x0011ÏÞÈ}ã\x0000OcqËÉag[ÒËº­<¬E÷xÓ«æ?î@î<\x000bìhíy&SÜCj{dËÈUÓFQ»X)H®H\x0007ÐpÓq&°$gwoU\x0019¸n^@z÷38ËN¢\x001do¸Åª\x001a\\x001aºÃFSÉE¾ÖÛ\x001c6
ºó\x0015a_ß*\x000eV
:È\x0001¢A»ªÆt×\x001dÌON\x0016\x0004||>TÑ\x000c[\x0003?j3C\x0014b6eF^ßÃ:¯fó§÷«ûO£:»±\x0007%\x000b¼  /þ15+6
Eì.Ýèì~}\x000e«½Í¯^,Î_\x000fu¨ço±vwÒ·r÷o¡sÙGú\x0016\x001a«\x000cVàh\x0018£S3õ[èæ·ØÔMù!¾®	ïÁ·Ð-á½\x001fã[hßø\x0016zSgâÇø\x00165%Aü\x0016-%Á\x001fã[Ðø\x0016aS:cú·@ÍÏ¬X\x00120¹DSAåÈÜÖ&<ý[\x0018Ñ8iMKJ³à[`\x0016NZlL£\x0001\x001dX¿ÛU\x0006§~\x000b×ü\x0016Â1%ß"R)}@Ï³¼Rv »|	Ù|\x0014-m­\x001fâµ05	ÂTÉ±©ã7ý[xmÉè\x0008QjØ,«ÊÀvÚ.4ñKøÆ9Û\x0016Üú\x0011\x001ebsCí¾£°®HÐ\x0011e\x000cõ/ye9¬-zÊ¢¯!µhúÄðì\x0013Ó\x0000¡¬·³7wO7c§\x0016\x0007Ü=©µ-p\x0007o» ÕàèÄ,æ§³7gW'CSy=171×&æNfö\x001c·^ði\x001a$"Z/»\x000b¨\x000busuñ:\x0007¡\x000e\x0014·\x0010F*øõ°_8÷!\x0006\x0007ÓObMæXÎ,Qo;wÈZîë
ë8æÐHÜ)ÄÞ41ÜPH¬*­*+yØ\x000fÕ\x000ctç\x0006çNa\x000eÍ\x0011Êwt\x001c¼Äi<´È\x0015e]0C³÷&!&r(FÖ7\x0016n\x001f±©ÎáºsÓUóSåç\Ðß?\x0013\x0015+ã7B6Ý½Ç\x0005ÌªÉ¬v`®4\x000c7¬ë\x0013\x0002ËE8µ·u^;Q\x0019¨RfuÀó¤|ì=#÷äk
k
(l]12mÄl$W*È÷7jôîY×4\x00174Î­ÅÌpmÓÑ¬1JI%*'¤YÕ\x001dº)`ví\U;\x0019 jÅ@°¢ºå,SF§0{Û`ö¶Y¡ÏCÀm»hØ<²ûÚÎu½\x0016Mz-eÈÉ\x001fÈÄð·fÅ5Äi\x0007¹Náµ%Æ\x001fKyáÒ£áËë~\x0002ø_± Ýjð\x0005Ì¾a\x0019á¥Ì¦²@µå(0ªÌìÎ8Ng¶¢Á?2c+\x001f1»H©t0K9g§öeÎÙ¦¡oË
}0ødÖ¨Ís¡5r=º¯\x0005Ì¦ñúáÅÌ·3NS4KYWëÜ]S\x001cT\x00039¨rdÏcX±@+\x0012±äU\x000eÝ²£\x0005È±\x001cËd­qï"W½¹êÎîVµÎì»Ùí°½gM;ã-÷ÃsdwJu·"\x00150«&³Ú9¦¾jdF\x0019]:èøs{{\x0001iÜ'øc)r\x0007ìÄ\x0003G;Ãqp\x0000|=]Î7WÙ¯2F^HJsµiXËr;ßÝ\x0008ZÀÜt[]¹Û\x001a½ä.\x001at[\x0003]'g°º\x0006¥éÌÞ4ñÇbf]¥j1¶¡ø
ä Lw¿G\x0001rsý.ËlX2Ðaui¾8Óoo×ÉÏ«ûÍ+\x0005Uz«\x0018÷7¨\x001fAÇ\x001d\x0019\k³·ÀbC÷ø«Âøb<æ\x001b\x0005\x000f©¼)èµvàîwK.:XWUK¬ùj
\x0007Ý\x0019U `\x0007sÑ\x0004\x000eÎÎ*D®\x001a1ãÂqJ\x0017³³ó7jv]@´ÎÑâê
ÞJE%\x001e\x000eÞAÑE½M%u\x001cîzL\x0018â\x0006W\x000b7 ÑòÈwg«Q.nÕ°\x001eE+kb_\x0000TÓp}RPË1[MýÎ\x000eCâ\x001cÏßª{?·\x0016åBÞFSî$^ÅumÖs£Ã=Ë\x0007ÜÇcyMcón**çub/áj6\x0007\x0008_!n«Þý(^ÕäU?\x0000ïÏ«MâU\x0011²\x000bª\x0012æÄìòúÀ dÛ\x001eî¼mÚÏ£?l"(D\x000elsZK\x0012{Î8ÞÃû9Ð÷MÞ_ÊvU\B¹¹ªÂÙª\x0010ÞÊmÏ£ßo"¿öÈwÈwÈ§¨Zl"ó\éâúî(Ñxd¥7-®	[>ÌÎW_¾.ï\x001fGÕ1j¡)rï­ä)¦Já@Yîëbv¾xóv~~9\x0002V×au\x0019,Î¦cH«s;K0ÎT£uåá\x0014XS5++%÷\x000cyòGMàIâCÚ¦S@]\x001dÔn\x0001Ã=Û°7Ií\x000bö@5°Ã\x000féCN¡õuZ_JK#¸T`Pø\x001fñpB\x0015º['£:j(Ý\x0001\x000f/\x001f5Î&L´±ZØØ]¯36ÖicéÂ:\x000eG\x0004m±\x000f6¯-çý£îé.J»®îBZ)J\x0017WU\x0013|ÁXç\x0010«aìÝ\x0016ïtZÙ ¥ëÙà
\x001a\\x000b>\x000fª1ìº[N:nãR¥·L3C\x0012®ÔTh\x0016XCÚFÙÓ¹?¶q+ÈÂk\x0001|aN\x0006£X!\x0014\x000eÛjdi÷;\x001d·q/Èâáß´¸¶AkKi+\x001dST~"¹XxÑ\x0018·§#z:nã.¥¬fØ\x0007lÚ%\x001bÕ©`uC§Á8\x001d·qÉÒÛ\x000cN1M®eõJØ\x000bì¸ã\x0018ýà6.4Yz£Á\x001dA6M\x0000ËÜð1VM6ÝuÙÓq\x001b7,½Ò$\x001b·àQÅ ¾hL»÷L5î3U|­t\x001aKn\x0003À²§TiöÛ¸ÐTé\x0006ï\x0019%\x0002¯RqÜ\x000f\x001f}w]ãtØ¦S|\x0001\x001cÍõ<\x0002`9\x001eÝÓÚ6î3UzÁ\x0005A]¬æûûqäâ~h\x001b×*¾ÎªÀMuölåÌÃ,ß~p\x001b\x0017*½ äÔ
öKæfà`\x0005Ï\x0000|@àºÛ#òB¬ÛA\x0015ß\x000eëB¨\x0006
\x0018\x0003´±GyúÒ6n\x0007UìïHÎ\x0015U$9­*yòNCç\x0013puãÄÕ¥'.0Re\x001af­òâZéyßîËjÔ\x0003W\x0017\x001f¸\x001aïÛ´\x0017bý5cK!ìéTÐ#W\x0017\x001f¹Ë\x001e¢17Éw¯Íp¥b\x0017Âó0+\x0000d\x0005»ÆR½ýà6Î\]zæ*'W>\x0018$o]ÁÕ\x000e\x0018\x001dÛý\x000cÓ
ÿAú\x000f\x0014¯Áe¥Ã¶r{\x001d
ÞîgY\x001bç­.-\x0019\x0012%{\x000ew¬ð{:½\x001a¶­.\x000e×\x0018R±ª¾²ÏÚ×Ø6ZÓx¿LñûeÑFÌ¸\x001e\x0007Te\J¸}Ek©\x0017\x0005äèíz\x0018Æó\x000bàj¹É\x000b÷C9°¨\(¨Acm\x001e\x0015ÖÉÆßdV~7f²u£áÚºÓ-0_àI´¨Õ\x000eÔÿ&gMèÖþ(VÑU\x0011Sg)Ã
Gq5{ÙïÉM]«)¢M¿)Ý Ê­7µkm]·µð\x001bsíà\x00175+mñáîf¤(]k÷òì_YeþÂ°ý»8:;\x0019\x0004ñ\x001by?\x0004UE Q³Ï\x0006¿ZÔªc \x0011ß\x0003©®ê²%UÜ'ç°`6-ÞÅM\x001dÎ¡\x0010i·¡Ã¦i0Ä¶§,sêYÓÈÈ3~Cw7ÑÔ\x0005uuRWD
Ï¶¨\x0013Õz\x001anÇñÃFÎXN_çôÏø]
uÐP\x0002Ù\x0007¡«wÉENê]\x001a4ÆÇÆ:i,Û¤"MIÏ>T^Y\x0015Â\x000e'OGÖÄ\x001b|3½7eM5Åqx\x001a{^W3ê\x0006Ïü±¤Í\x0013¿øÈg}cØ¦H×ô¡[\x0014o*jã$eG©7àÅÊ9HÍÿ|OÇãTÔÆi*ËÓÃ©¿N%N[Ä\x0019<ë«º`\x000f\x0014ÙÛ~öqDÉÆ/ËÞü\x0018YÓÎ£ßÈ÷=·n\x0007ÙÝ83\x0011U5^(UöBJ£/p\x0000!	\x001bÇA÷\x0010zÖ
ë|Ö
ë)ÀÆiâ[¥$óîÇz/\x000cê°`IZþÅ\x000bøÅ!þxxtwsô¢O®oWË§í¬ÊK-ð½GÑ\x0012\x000b7@vÃ\x0015\x000eÎN°&:Ý]Nwvrç;\x001e.æWkÚ&åZ\x00140Q&QÀgDåÖ?7%IàâN$Tè÷zù\x0000ÉGÄ}±zx\x0018#\x0004\x0000ó\x0010\x0010\x001cÇâ´âWK¸ÁY¯ç\x0017à¼Dê\x0017!
\x0018u\x0017M\x001d\x001eÜ\x0005^ ÏUlÒÀ¿|ÐJO2=éÜBvëe\x001dü\x0011\x0016^Ø¸á\x001fÚ¸©~t³¼¾_=>;2Rí\x001aÏ¬\x0014Õ05SÍ+ì[Z×»<:A\x0001ÉËËÁ³ÎnZErµ\x001by\x0016IÕü\x0001M*3<ÁRî{¤\x0014\×ÁõNà°Î<"\x0012GÅÊLÎÓ=ö¾ä¦Nn~ %wup·Ûç\x001f^r\x001aÇh©ÃxK®6Õþn\x000e\x0014Æ\x0019Èó§û»\x0011ÔRËv\:UËË
 óCîÞ×¬×l~u~F¶ç&£©3çÈ(×sCQ6\x0007N¢\x0014¶\x0012qT\x001e¥\x0010SòìP8 »\x0007w·0[÷x&UÒ5xs\x001eë³"Õ²AÚjù¬HccªX¾GÿIµl¼ïZ¿ñÿ{¤Îá\x001bµ.\x0006_\x001câLz\x0001\x0014³w·ËÇ\x0011¤ÂÝ@éÔ4ç8·(´Ò²hJO·\x0006^À\x000f³g§óË\x0018~öÌ:O1Ñµ6ÛÇ§Ù»ÕýÇQ\x0013jE\x0001+H3nñÌâh£í®Æ¤¦ÚW³wóót2nhàB\§S/b\x0016õ¶4Ú\x0014þSµÍ©¡æöñ´µé?\x0018Ë´2bÃN¢\x0005ë\x000f°\x001f8£\x0007{ñGãÊ\x0018ë¸øc\x0011¯_i£èdÞ\x000bÑª\x0003¸Û±«Ö\x0017\x0018ââe¸Î°ª b\x0011l0Ç¢fÝuÚ-Þ"\x000bUMXU\x0008k-W¨©07âq\x001dÔ¿\x0018¿¸¡±uñÇç»¸ºÖpù'áKa#¶g	\x0017G/Z\x0014X\x001fF²3ÝÑÈ©«kEÚÈ+C)¯àê SÕFQi\x0019R`\x0018\x000f«\x001b§Ö¥§Â¿e'øæÊúÒõËXä\O\x0014ÑÃº\x001cS°FÚ±¶Å³Zb­þ\x0017übÃÿZÎÎ¯¿]ÿýß÷£¤Áå¥:ÒàE¤è¿r\x0006Û­·\x0018dóÙùñ»ãÅùb9è:sØ\x001cè0\x0005\x001aG9)²"¢ÖD¯-¶\x0013z¬5C\x000fTX$îèêÜqSä}\x0012·Ô08\x0007YÝ];6yîz:\x0015[&£²VQ\x0008Ë\x0002ÿà·÷w_V·Ë\\x0017r³¼ÿô4rl
¦*hÁÜV¤\x0000\x0003+x\x001aÙm®½=?{³8¿äúùùë«áÉ1Ä¿Ö÷A~÷Ù_(¨ñ\x0016¼wsà²Ìä:ÊÝ­Z\\x001fM\x001d\x001f¯_ ìr¶?Á¯ÁMbÇÕÔoÛ=\x0001§¿~Ã¿7]ç?ÔþÑ.6¾\x0000J/þH_À
Ñx\x0001ÒÏ;¾\x0002Âñéã<×¤y-©yÄD%öµdôÍ\x000føÅáÚ\x000ex\x000bÈ÷«Ùû»»\x001b\x000cry\x0002dòlärp\x001có²{P\x0018]«o\x0001÷|1{q~vqqv1Î­ìëT0²Ë¸#<Î8¦\x0002\x001cUB0$\x0013\\x0007CÊ\x0005ü"ü¼l®þr×å¯*^mØUàø\x000cCº\x0013¾Â{\x0011d#\x000bô\x0002~Y \x0013Øô?-\x001eá/oolTl\x001cUö±H\x000ccãB	Ê»EP=´ï\x000eáÂf?Í¯.á/oOà7}E\x000e\x0015®ªãªb\c)Ç
\x0016$é!GÎ¥ñ±Ó\x0001ê Ýº¾¡\x000e\x001cýúÆ:n|î¸UmVÞ½âÙïöØ\x0001Ùp\x001f;6$QÎÕªuOwÏL\x0001sÕ\x001a±µáÙ2£/±Ý§\x0008çÚåýò\x001b\âùVuwû\x0008Xcí\x0012å47\x0002ú`«F\x0004pDYø¤ûV¿<ùR¯ÎN/á·[F:\x0012½ªÓ«\x001f^×éõôVóø\x0008\x001f\x001cúý¹ Ñpéd÷«Ù\x000bßSCGä¦Nn~´uwuz÷ÑËÆÚË\x001fmñkåo4üÆÞ?Üæñ
|ÿ£á7Úühÿão~SÚÖ7°?È7PAlÄ{¨Úfï®W×7³îîoîFMÒSÒ\x0019\x0010¬d!-\x0002wxÙn%ãsM\x001f/Of?
Ðcj]§Ö;PGuàZ*Ò"ÔUN(Ê\x0001A¯ÉÐ¦\x000emvYjÇ#¼`[°~\x0016Å/LwºÚÖ©í\x000eÔ\x0001CA´Ô<ù/hÅÍUQv\x0007*Ê¨}Úï@½\x001eÖ\x0014DUûPM\x0004\x0003Íc9îÂ¬«W\x0011ûõ51P=«¿i*µl¼rw\x0011ÚÐR+KrÝ¸Ô¼­UwÎ³\x000c»±­å.û\x001a®MÊËay*u¹èµ6ûÛ×ºyðí²Ú!pFP4yÖ®\x0012ì\x0016ï½nø¥sü#ÆÛî\x001e¯\x001f\x001eV_V·3\x0000Ío¾^ßlÕÀÓ\x0003Ët
`ßyó\x0000''|w\x0007ÔÉÙåñÅÅâÍâôr¾õüäíñÉP×FE¯ëôúG£7uzó£ÑÛ:½ÝÞÃ\x0015$^ñÁ\x0018EP\x001c ë)è¥ï4­*tWGw?ÚÂû:½ßqáQsr½ðy²A\x0014¦\x0012\x000e	¾3ÇUN\x001fêôáG[ûX§?\x0008½P&ª]_­\x0006GÕ6§\x001f_/¿\x00037p-Á+:\x000f<PÙ`t¤ò~Ûøóãù?·\x0013+ß Æ\x001fK5w\x0004Ië¨\x0014 8S\x0011ËÁÊÞñÄz=u\x0019ñÇBb´\x000f)e\x0011`³Íå\x0014§,d÷ÚÉÀ&6\x0018,\x0003§ªâpSàÀö\x000c\x001ci}£Ü6­a\x0014®©\x0005Ò\x0013.þüySÁÙrs\x000f/K7q\x001e©Ø)\x0016yrìY§ÔÖ\x0011\x001e£7q\x0013\x001a·q)4ìcY |\x0003ocÞÅÝ«	ÈÂø¦7,°nÝ\x001a}´ü8TÆvAvÞ\x0003]àZVv·í\x001eóÊÆGó#8×j¶ÈYW³\x001d\x000fë¨*P\x001elÇÍûÑ\x000e7ã4
NSÄé\x0002öP°ø²æ)k({ÏÜÜi V7\x001e¼.\x00015¦²Ã6i°4­h\x001cT\x001a\x0018\x0007êT\x001dÔ©\x0012Pmyî\x0010\x0016X;â=s¦ú\x0006¨/\x0003õ\x0007¶¨|ßÖD`\x0007â\x001c£9CãÉ¢'/\x001dë
%õõ\x0014fô\x0011þÃ \x0003±Ññ ¾\x0001ê@U%±l9UíQXAÅEFÖÆ¥!h\x001a64 ^C¬\x001e}Êác5î$º`ÑhRÝ$ÕE¤^p÷Tp\·rB|àûî)tÓH­lZYH\x001aÖ¤Î3i¨Hw? T«)Ä\x0012R¡pf*©\x0010V}à±NÈ\x0008øXR-\x001a\x0013þ¸\x001b©\x000c$I\x000b¤½/µËí´D©Ì\x0018I\x001dÉ×«ÙÛåýòãõh'1\x0008'\x0014 JRa\x0000Ún×£ãËÅìíü|þòx\x0004¤­CÚg
éêîBú:¤¦±\x000e\x0019§Cz¸Ýi<F4=òÐ{°Az§:d_Î4êè\x0012!ÖÑMFÌj+\x0019Q¡4Ekñ1¤º;& ª\x0006¢*@ÄFB\x0012ö7ë¶!lÓ¤£²ÛHÀ¨\x001bº`;
£ëùI\x001b\x000eQ	~Ô=	\x0003R>Ó\x0013²Q\x0010Á¤øÉ\x000fÝë¤Û>¼\x0008Õ«ãY±[º\x001e\x001f~\x000c-\Ya£t\x0000ì 
¶/]Þ¯0F9jmµJêYc$ÆæÃV\x0011ì_º<_`r;·©s]¸1M©*n
kKL¿\x0013·Þ¢ê2ÛÕ¹ÝNë½«¦Ë$îPç\x000e;q[Îß$nRÑáé²ÈÝi q×&ÜÁ¿\x0000¯\x0016\x001cE®R\x0014ÐVRQëPvè\x001eÎX\x0008Þx1ånoæ¿\x0005\x001c\x000e©\x0014µª©¢4ÊúJ\x00167×«Ùëûå·ë¤H½]±Â\x0003\x0012\x001e\x0015Î\x0013ô\x000eYÐ\x0011¥+ú\x001bJ\x0016'ÇÙëó9¶Cnev
f·\x000bsà±\x0005¨îH3ÏÖÑ\x000c\x001c¹'æ êÌAý\x0000Ìõ\x0019ë"ä Á\x000f\x0000\x001dÐáGv¶\x0001ÃÏ\x001eZ5WZý\x0010+­+­~öÃ£®uò\x001c¡Á\x0017KáûZÐ	¬ØÈæ½X-Æ\x0005W
ÇëfOÅê@Óâ6<¤Ôu\x0017Ô\x0012M/\x0016ó«Á¹àD\x001cT8¨\x001fØ4Í\x000f@ÜØ\x0015áùï
¹ÄRRdé\x0015\x000fÐ³*\x0005ýsÕ¢¢d³ÝÏSálhZuxX¨æ¾x·¼\x001d×F'Á;Æyi©MÞEÊK»`
Ë¦¹î\x001a¢\x001añ»ùéº¹²IÞ5ÊT÷ý\x000c1kÊ~i1céj\x0002'«\x000bIe\x000eD\x0016¡,&£u·Þu²zúMÐ°\x001f6ý&JÁÉHüc\x000ee¸èX\x001f¶ò¶Ü~\x001f©\x0008\x001bZ\x0002B\x000bUIí«åÓû»§ûO£^§\x0018qêQ.\x0013÷\x0014\x0008\x0013 T%×\x0003³\x000e®f¯æW/Î®Î_\x000f¼ÿÄ\x001aë¬±UpIò PÁ²^\x000fÕ+oE}/hÔü¾\x0010X\x0006\x0006ÿæî\x0001=Ð£»§ÇëQG\x0002s;ù]!\x001a\x000fX\x0005ÎÕ$pÓõìOÎ.Ðõ<:»º<>=ü°ü¸|x¼ï'UuRõIuT?gR['µÏÔÕIÝs&õuRÿIC4<gÒX'Ï´¦úç©xÎ¨Í£ÿ9ý¾ñöû×_by\x001c
¹RÀæ¨\x001a!ðH>#{
¨[.Tå\x001a¨øc	+ÖIy*Nnªñ\x0010¬}¨COÊrÜ²Âgb]KeÃ/²Tv56ðîË×ëqÕ\x0013à I,?K *Oï\\x000cdü\x0019±e>êÙ·ÇÃ¥\x001e\x00142_×ubÈ\x001c5ín\x001f¨Öãîþv5ºÜ\x001e\x001d+\x001aÏ\x00056\x0015Õzaó]Õ\x000eÖ½\x0019ÞÌ¨äãìüt±¥Ô^$i+§\x0005\x0007ôâ
¥ÿ	eÊÆ§>X
¯\x001d`RÑoÝãüÖvÏ\x0010©«üo+¡ÍÌfVAfÓÌ«LbÆég9ÉimåÂF\x001aål£5\x0005Y¥B c×7tã,ì7.åS.\x001eIõjÌÛç\x0004dÉëò(õ¦³H¹¥<·v¶gÊ\x0010¼t)rqIjW\x001dnWF­¹±nì3EÍUGÅ\x001f\x000bQQ­ ·2ú¨#
òÀ¯
£L·úe\x0007ëÆ,\x0005·9SÔÕfb*íèîË§ÛÑ
G!ÂÚ×Å\x0007¯Cß1vtöæÍÕéÐ\x001b·9YÔÕ&NÆ\x001cÇÀ\x0017Mr¨¨fa\x000eÍÄ«ë¼ºW	ÃüpApÑ²6¬Ü÷ñ~xk£\x0011]}4â³[à%Kn\x0016¿(gù­\x001eà
¾\x000bnþûÓrTGAG'\x000etÞÄZ{\x000cÌ`>XyÉ\x0017²ëY¿¸{ø\x0014n¸ù\Í\x0017Ix;¸j«ÀQy+=Y¥-qXlö\x0014Nâ\x0016J ·[OÐ_\x001câUìëiöv9âvS6 æ7)ú\x0006I1e¸hºUÁ\x000e¶á\ÍàëyÅ4 ÈÔoÀJm\x0015¼^~YTo\x000c²/QpT\"\x0006m-\x0011x=3\x001f\x0014Ìà².8\x0014\x000fñÇ\x001f\\x0006¹j\x0015\x001eM!\x001dAGR\x001bRÌ\x0004>rÃS\x0015?\$Ú@HáÒ@Èµq<¿¾\x001f#1d£ÓÉ´HÇ\x001d#tÜ9Ñ-s[ÙÅ8Cêbíyð\x001f*X»Q\x0006¿¨	®~\x0019Ã©±)+\x0014\x001e¼l¾[­xÆfìnÕ ×îtqõj;¢®#êéØBMs@âB\x0013ùª\x000b.\x000c\x0005ïÇ1:£ÎhY\x0015;âp+Çëh¹åE\x000cæÄÆ1ú:£Î¨\x0015Wïzjo³²J>=,b¬\x0003Æ\x0007-XZ\x0004Ëx%MQ¶o´C3F1ÊÆf\x0005»QÛÔB´á6m\x00194zÒ\x0017Õ8HÛ´\x0005+\x0019\x000eX\x0011ÇV»q­$÷°Ý(\x000b¶ã¿±±!eÁ£fW\x0005¥ùè±ÅÊ£ê\x0002Y»nð\x0004\x0005\x000b\x0019«øKT´\x001d9nÿý®¶±¶`\x0019¥IJÁøb[Ë­ &ðe\x0018\÷\x0014¥ñ²b g?O¿\x000bqDn\x001d°z3Üqë;ìH¹é[Ëo£ßn?ÞßÝ¬À¨Æ7»ªcU[¾µ}èn\x0000g_j6?}y~v:d]dÜÚ¸:ÄU¥¼2ÊùCùÿ
Ý9ï\x0001#x³¹V\x0017\x00046µ$l%J8.	ïD`í6ï\x001c\x0007ÁÌäÖåcöú£Æ\x001eá ýFÄªN¬JáÚ9LLcò\x0019\x0003ËîK©\x0000X×u1pHD\x0019¸\x001a#3Ýx00?ØÖm11ì\x0004\x001aà¥ZiHYµ)º+]
]Ø\x0015\x0013ÃYË
§\x0013Áù\x000fÕ6î¹½
C8\x0014\x0013k`,]\x0014¡"V/(ö¶c8\x0016\x0013+P»Ù2¯¬Ü§0´[ÂESONåÅùã\x001d\x00199ÎÍö\x0002\x000e7Ü\x0015Yék¬\x000f\x001e\x0012iðP]ëdâÈ\x0015ïildðàÆP_±aÕA&2n<©Í[éC_ÕØ\x001csôºb=\x0010w³\x001d­Æ\x0005\x0001´Ë9ZjôÓùÚFq¿=ÍÐU\x0014îd1;Z\x000c\x0001B6gÜÌ1\x001bgÜ¬î°îþî\x001bþ4\x0006\Eu@Õ.âUà.\x001azÙÝ\x0005³æ>:ÃÆºó³wøÓ\x001a¾ÊðJÜÇªV\x0004×\x0013þxx²½X¦q\x0003£²æRD\x000ei\x0005\x0003Îcv"fÃ\x0012.Y\x0003³\x0017ó4gà´wißK\x0013]ð\x000b´).î\x001eÒ6v¶:Þ\x0014\x001848È\x0019ÆÕ=\x0002I\x0017gW\x0017i/ôd¥ûÈU\íB\x001eã<ºTf}ø`ù`Ö¢û¤+%·ur»Óë,äeä$M¢·ºG+©\x0014ÜÕÁÝNàR/}JøeN¯\x000bB:\x000fêRp_\x0007÷;í\x0015pHCXxG¡|\x001fP÷#òï¼ÄKÉC<ì¶Wrå­<\x000c{yÁ±\x000ccØëú¦t¬V\[,iN{ÅpdßZÑð>÷¸l\x001c+r·sE\x000bæÞNÉz!¼èÝyªRrÝ ×»írÉ©A\x0014 ÎùLo(\x001f,¦ór/Eor§#1xÅ:RÒK&÷°u\x0014£ËÎ[³\x0014½ñÊÞPp²°à!£+R÷ô`T«Þíè¢Ç\x0006zÜ
]\x0011E[³ýú<7Ý÷
ÉUãxQ»\x001d/`
*KÇKXsÁ\x001f\x0018ºûÜ/ªap©,.\t:^tÈ:\x0000îLÕL±ÏÝ¢\x001aÇÚíx;,±a\x000c®È\x0007Zt"KÁM\x0003Üì\x0004î\x0014YfpÍX{ån,j·ÅG\x0016ÇÁ°ö¤@«z²ã¥èEív²t"\x0018=Ð6_\x000fµí\x00162+D×£Eïx´¤Ñô\x0019Ý¤\x0008µ©jÕ÷IÞ8Yô'Kê{JäÁ³\x001b
)Yå»Ã¥è
£Kïftá<uÚ/¨+Èè<Tî\x0011\x000eeèÒ6/Q»Ó^÷RRdBjGgÞK-ÿ\x0017,]Ý´tõ®¦nà2\x0006©$\x001fØÛÇg£ßãÙh|c¯ãåì
E©}Vb$.g\x0019ñaT^ô~6»s\x001bî?Ã?-¿¬O³uzº_þr¿\x001aY\x0006\x0007o&åÀÃ= ò½È5²§Sù§ùÅüjör6¿:¿:_¼\\x000c!ç\x001céúîÇóW§P\x0016/4fË\x0016\x001fW£\x001acD>ËÀã\x0008!c©4µ¬¶=SU«U>\x0001ñà*gdÛ@¶?\x0000²Sud§3²\x0015\x001b]lðÃæTÕóëoðãlV÷\x001fïF"¨ª\x0019èÂÔ\x001a}t\x001cÏRªûÚ9YOW=?~\x00078Ôfqþòlû7X{Íø
¤Þõ+¤:Ää\x0008\x0005+Ò\x0008Õü\x0015dÔö._Á6¾Ýù+Èªæ8às\x0001ûÓóSÝY²¯°1ÃÛj÷?÷\x001f\x0001
áÿ1¦Î\x0016î\x0018-¸_Ç[3lÎVý:ÞùÎ\x001b\x0014Éÿ1?	FèÌûs\x0012ÂÍÙ\x0008?ÿ\x001fL\x001a«öXñ½/\x0016\ És\x001b\x000cU)zg¨rUöxý3=¨ÿe\x0000¼yýü\x001fç¶ðÌÞ®\x001e¯\x001fgó÷«Ç1K\x000e ì\x0011Y\x0003àÔÔÅj\x0019^uë¾4ágo\x0017Ç³ùËóÅåÖ/PÍùL_@¶fñLý\x0006`&bß|ú\x0006BÓ¨2ç5ÏüraÌúú
B¦ÜÐÚ?Â_$ÿ¨6c\x0012ÎÞî¾^?.oF%T¨ÊBrk¥bí ºSµ\x0001øï;{{|9?¡ôY\x0011Ç¤U²ÎÐÂ/\x000e¥¬ç;±Þùíêûý
Á¨ý\x000ençº3bêY*¨\x0012&ÝnUº\x0013ëß.þy¾åßèò!\c\x001b¸Æ>o\«\x001a¸V=wÜú¤TFNÚ¦Ïú½Ø8}!²Ä)XW¯îîgÿ?³£ÏË§?Ç½nò gêá¢dWAqì¬ÓáÕÙÕùl>;ûñÿl.ªM·¸YYqhê
to·w\x000f¿?kõúÀ¦æO©D\x0011$é\x0012/C·\x0001UuÏ½]üÇÕ¢ó( ÐØ\x0000Ï\x0016Ô:¨\x0015Ï\x00164Êß×Q£<|ÿìXNW×ZÊ\x000c~±)em\x001e,rx\x0018iúXÆ&\x0011XËó^¤\x0017Ê©Ðí©´ý`ÅÃE¥³Ô\x0000\x0017n³zÒåêÉúYut7NDU¢"N+¬\x0014\x001ct÷\x0004\x001cDè\x001e\x0000Ñ8§ÎP@u\x0000UÕQ7/gºä\x001aÚõl>¬¡
õÂå-nÇëQå.Á	EÂáØ¹\x0001°\x0011\x001cUª53\x0016×Áªù)nËãùi·\x001dÆ£R5;Æ\x001dâÍÅM^Óìíòæéã\x0008f-;\x001c\x000e\x001c×\x0016j/snÚÆÁÆ¼ÆÉg½\½\x001c"·MòMæ\x0019+£íG
°µcøüzõ×\x0018XÒ[¹Û:dáâ\x0008g\x0004\x0007è<vù
kçÇÿkS-³YYgKV\x0001\x001c<âÍzúX?²(R±Â¿ÿ{d°ÐW3vâq\x0011'
é\x0012\x0006×R°ÃÝ°ª\x000e«9¬®Ãêg\x000ekê°æÃÚ:¬}æ°®\x000eë9¬¯Ãúg\x000e\x001bê°áÃÆ:l|¦°2ªæ¥\x0000¿hÙ±éþ_ë<\x0007£Û±f3ü]åMÉ<
ôaYìtãí¿ÀÖó\x001a®øùéîÓ£þt¥1ÎïïWÉQ8yº½¦:sEc#EòÇ>­0l\x0007xQa\x0008Wc\Ty\x000c-¢$ç3Áäjþ\x0008\x0006#æHw}õzq·ù9|&¯àäêô8Õw÷Ã6·Üa.\x0011ðÒ\x0007üûß]ßÜ,?­°d4!'UÑR	<`Iïæ\x0000ÿv\x0003\x000bþøîøädþº/Ó&°j<\x0012LþÅtÖ',¶íîn?.áQoÁ\x0003\x0017P2]FKý\x00166ÐØ;:;}9§Ú(þò\x0014ß§\x0015K\x0003t)Fÿúú1=EM\x0001Byøzy»üt÷þz÷\x0018ìøì*9ÍÅÉÎ4ØöHÁfé·ùéüõÙãEÅ¿>¾¬G²\x001b®\x0001\x0002\x000b­Æhê\x0002\x0010$¨\x0001\x0010\x001c+8LNòq\x0005¡G/NÍlÈá\x0015A%\x000eÆÐ¹P®\x000c\x0003wòX\x000c\x0017ýÃå/¾\x0012«õÐå\x001cpÄÙ±\x001cÞaÉCÚ\x001e\x0001\x001bä\x0013F:.i{ìðXàêÆr`íez«Q¼"7[`)£f\x0010\x0003ée p[û± !
\x0012N+âÀÏ\x000b\x0012\x0015.AÙ\x001d\x001e\x000c¼jaôÇAïõ9±'\x0010éwX\x0010¸dãèêS±`º\x0006"/³t¦\x0005\x0011Ë\x000f\x0010ÌcàÿÜ"!sá\x0016Q6kÔá\x0016ñ¼"ÞïU|íåØC\x0015µ\x0019,mVms5?;\x0002	Y#­\x000c\x0004ª\x001c{¨â 5__#òéîTõÖÄ\x001dv+&ãåØc5 \x0001-	ì\x0012I\x000fÇF^¸ÃvÅ\x0004 \x001c{²â\x00004:Yv9$×be$ð`åè³ÕF¾jLóªóU\x0013ù,¡Îô2\x0012Øërôéêm*²Nk¢ò\x0010§Æ1¿\x000b\x0008¬rìé
8Ý\x0001AÌâ\x0002ðp¡k/*WN"dÊm\x0019y¦ÈTk®\x001d[ð¸Ç.æ|ÿù¾ÍÒmÙÊoÌò7ÿkÃ<½XÝ|ûû_\x001fÿþï$ÂØOc\x0014\x001bk°asá\x0010\x0006\x0005=Ñ\x0018g7Wgöbqò\x000eó~Ã±\x0006ÄvÒ³\x0001béÙ\x0000±é4\x001aHgåA\x0004\x0002×S}Ô\x001c\x0012w\x0006å4 ¶¡
\x0010ÛRÏ\x0006ª±@ÎK2yLYoä1Øôx,M\x001f-æaÛêð¬m¬ç\x0002TZÏ\x0005¨ºÔÿ\x0005J\x0017Ø:Âq¸V\x0008|ú_{ãH\x0017ðj\x0002$U¯3¤N9u
K M\x0003Ò<OH×tÏ\x0013Ò7 ýóÚïáÐm¼9/ð\x0014Æ7çîö\x0011\x0000ïo÷\x001f\x0007à\x000cú.9Û8iì@$'WÁºæ%&º%<;½\x0004°óÓùùËn¬\x0010~þÓ=­ÞßbT\x001bÿ×éc~ûázu{»UiÎË§¯S£Îñâ\x0010\x000e_ÝÝXÞü\x0002&È§têéH|R¸>\x0000WÊ\x0016GÔD3õÕÙùÑüä?Päp~zt¼8=]ÌªDçËùÕÛ°Até¯°
·`ú(\x0015:kÉ\x0003¬\x0012\x0007è	záøÌ
KìöÆªáN\x001f¬\x0002^\x001dì\x0011Q¶?dXãhafo°èw¦RX\x0014\x0001Ò\x0019\x00166Ñ\x0019VåÚöheLÒ)ûu`2¤bX\x00121\x0008+bV·FXm\x00086»á{Õ¸\x0003ô.Û\x0000ÓfØç6Á 5ÁZ±7Ø&}ú(6O\x001cWÂDêÒ\x0000X%0¢	Rím\x001b\x0004Ü\x0001am Ö°&dKu>\x0006\x0006«âö\x0004+H¦®ØeÓÆ$\x0012\x000b´¨R\x0014èìÊ½®p*è½m\x0003)0\x0011?KÏY$t\x0019ÖÊBK\x0001\x0005P\x0012-J°íÖ¦,bú,¤u*$M>À÷tÖF³\x0006»¦öEYÃüYH­ýé\x000e8õ<¡F©i\x001b\x0008\x000cª} *íÓ
æÏ.#PXÔ'Tí4öo\x0001mÄk¢ÕÞíë\x0006S\x0006xóg!¬*	àæuölT"\x000b_À'Å¤}ÐÂÂ\x0019?K6hÚ³\x0001ÇÒ*IKëòFHööÞhqUógé
¹\x001fiµBqFÜ¶Á(C´Vîë
Ã,j¢ÕÅk\x000b{!óhé±QÏ%Z~w2aoØâ?K÷­\x000eè² ­Ma3­Ô¹Ï'¢ó¾ÖÖà9s?\x000bwB´!§@$>ó\x001cî\x0010éH\x0000»|o¶Ñ(ÿ?Ko\x0006°¸l^Z¯³\x001e ¿ÉHKkö\x0008ë\x0005Âúò\x000cÓ'(oh\x0005YÁb¿3Ñ}]ºÆ Ý?Ki³Ô"À\x001aö¹¡H°Â}½cÆáë?Ka%ÍM^Ya~¤5.O{\x0012µ\x0017÷E\x001b±¼"Ò»E@+P·(dZøo2­KÿðhÕ\x001fâÇzÅO\x0016Å^kd?~þû_·ÿkµÅ¨Å¡\x0002)!>\x0017¢¬U6Á\x001dí\x0017\x000c%±Y\x001fûò§Åéb±\x001d2§»
!q9UÄi=&CÚÜ:\x000cVµm®Ñ7\x001fùðÛm\x001dòÛê6O{~y÷áqõt?;Z>\¹Æ¿^ß\x000f³ª¨\x0005\x0015ÆÉ(áä-²}èDh_\x0006ï\x0016§yæóË³£ËÅÕùìh~qüæ\x0018ÿz|>\x0002;gîvÃ\x0006VHèäú\x001c>@_X·öÁ®Ø9¿·\x0013vp&_½¸3\Ve\x0003lçó\x0000v\x001bî:çÜv£6â×:dwï\x001dÁµ6{ß"9\x000f¶\x00135Ú62\x001f\x0015Ñ
2\x001c<Z\x0019[â½=cçfÖÃÜÀºÛG\x000b\x0007\x0017óÔ\x000f«^½²u7ïNÿÿzuÙyG×^±ù\x000e\x0016\x0011ïNö	XDÿçãÍãê¡~­dìªuÿÅýõòöqÖX4³µ9AìqÒ%\x0005¡ì¡­zõ_\x001fÏO/·C6NìUÄHþ\x001bx\x0018dÿ`LË+lÏ\x0013!¨j\x0005,\x0000'Hí\x0008Ré£b2dã4\x0006cUtò \x0010ÒD~Ú¨«¸\x001fÆ\QÆè8<nxÄ
Br\Ô\x0007ß²È
!\x001b\x0017ÄDÈ<
\x0016!¥Îöi%\x0019Ò}mÉ\P\x0002©c\x001a[!U®o\x0004oÇÓí\x0005qO/7\x0017'Qò	Éç@\x0019\x0014Sú°/JªX(zàÚW}q/ið\x000fîÊv¶*GË(#_o$\x000e\x000cíJ>ÂÞn.)-{sDµ)£g\x000fA\x001aÊÑ\x0018ÌÜîÊMË(áÕÉ7\x000e¸]d¬JÎ'\x001a\x001a'¸\x000fH*Z)´I§	)á\x001ew®\x001cêì1!´cñT¥Zz{§x\x0000PÂ«N\x0019D\x001ck £ûzÞTÁZz{k²0Ä\x0012ØÄ ]\x0019Ý×!\x0004Æ½\x000c¥~ýÀÝ\x0001\x001bk¶zÞn_Ï\x001b\x000b\x001d
o\x001d#}õ\x000b
zRêjl\x0017\x000eQ¢ì*¼uÖ\x0014¨¿AVo¸
|\x001e'z2¤<LúÔÅV!HÁî§4Õ\x0005nöõÀq¶*½tP\x0003!_:xì¨ÈÛ-_¯ÍÞ\x001d\x000c\x001cªÒ{\x0007çqÅj-\x0005¿<ë\x0007¾Ó®üüýIÅO5oìÅÝÓÍêÛòþcêÔ|³¼ü~ÿ@í¥çÿëáúáq'í\x000cÓQd¯KìðÊ¶QÊZàÿ6oô\x0017/Sãæùùå?Ï/¨¹\x0014å=..çiÎÎ6úì¦í\x001eÃÖ¹È++Ú<ªEw»¹{w¦ÏþÛ~è\x0019Ýg\x0005 \x0002U\x0017¾e¤ì½ºý +n±iDZÞ5ØWéMë\x0004Þ>û{û¡wÜb*±i-æ¼RIÅ{ßõÙ\x0013ÜÓ;ëè ÅWYÜ\x000cßÙ\x0018\x0008_·Ìðñs1ÿ~ð½ÂÃ1¯¾æ¯)\x001f\x0002{Çm^;Óçç^Z&/#=Æ:4½¸¼ô­ÐøÎðÙ=ß\x000f|Ðh\x001eçãsW\x0015ÀWUÑ´\x0002»â³K¼\x0017~ÍÍ[\x0007\x001cQI/näÕO\x0015ûÅ'Gt?ø\x0012v>-¿"\x001d\x0007À\x000fJ\x001d£lñû?ÿ¼uºÇV ä¯Oïo®³\Ý`
¡ÁD "[ð`d¤B7
6[ùo"],ÞÍÏ_V´o¯^\x001c£\ÝVÚ¶m0\x0016µUP\x0006Ð:%©Ä	K[èdì\x0008PìBÛ¾P§Ñ\x001a\x0004m\x0013­Ï¢z\x001e´T\x0000\x001dtËEØ¶}N£õ\x0012Uv\x001d
m-Ô?Þ#lûº\x0006Õ,D\x001b}á	tÇ\x0004Ñøí\x0002Û¾\x001c'®¬©VÖV5Åri\x0016\x001bN÷\x0008Û¾N&nÚ¦¨§\x0003!\x001dgVQ9\x0016Ð¶¯ïrÚ®Ûc"®? ãË\x0019ª\x0019J¶\x0012ÑâØ\x001fmÇe1qÛÊjÛz·\x0004ÛÖ\x001b^Ü°Ïµ¥À`9­P\x0014\x000bÅX[Ó¨TÞ\x0000»×­@Á·b\,ÕÍQ´\x0017\x000cÕ\x0007¨\x0018·UÞ²\x000b.\x0005¸Êqá¼u¼º¾æõ¼\x0017tËVÛåæ­g×w8Ê4;ä6èõY¦ø,m·v*ô¯\x001fùóÏ\x0004yh*ka!ÑÍåýõm\x0015»6÷óã\x0008Eêó8*\x001fÁ\x0014Û¼!jjZ³ù	XdÇGÛ\x0008qÀëaú(AÄÃ \x0007z%É\x001d@\x0014ê\x001dCh½^\x0005¨y>¦#êè\x0005W\x0012\x001b-©
"Dky\x0015ÛöV\x0001¢C3(}\x0014 ¢\x001dhri¶>\x000b\x0001Àä×HK¿\x000fD-\x0004é£\x0000Ñ¸<\x0001Ç¿WCÕÚ\x0001 \x0012ÑéRa	gþ,`*¼Ä¹]ÑfU.ìÒÊé°3²U3^À¨±Ø)\x00160
¦cÏ\x0000
2\x000f.{ÔÒ-_ÇOV~ûÍ%åA¼åãZtþín¸\x0004Ô¦1Û\x00143:$gØÖÂ³¡\x001fz\x0016oþî¬¯è³\x0002BéÃô1\x001aÈ:Î®ôt4{\x0015Ï*Ç\x000c\x0016\x0002Et	ÓÇh ç\x0014i)ayx Tr¶\x000eöÄ¦¶\x001dhùåæ£ú\ó\x001b
/°\x0007÷áÛ®
E½^\x0018¤¢×3*gìFgTëNk\x0008/¾¿_\\x001c/zë¬jÙÿ-äôp×U9\x0006kKea¦ÕRLcà8ö/fJáè sDñj[ÌýóRNEÎ9ZYV
ÛN¨$ÌéØªß/æÌy\x0019§yb(rúH±ì½ÕÄ\x0019ÌfL¬3;åë§
'N\x0017)öÊãÓû½­göÇ\x000b×S9Ê
Àz
æDë9÷ö\x001aå¨técOmf	\x0013söùPÒbG\x000eÖu7Î?îoï~õ$ø\x001aôÅõÍÍêýòéã6oÀ¥[\x00183¢\x001eNÎ@÷q [F(Ùs¨\x0003ããÅùÕË­\x0008p>¦\x0013\x0006LjªNÕÜÖï\øi÷ãÌÒG\x0001"¼8RôÊç»\x001a\x0010i8=V;ø~Oe<"ü³á´T¾è94\x00045åçµãUôI²#µC{ÛocO@Ä,ú(XEm\x000e\x001c\x0010cí©Î^qÉì³/¦\x0011FlÄE[Ñ\x001bAæO³±*\x001fØÇcvé\x0010\x0017®Pèªé\x001dìµ\x001cK3ZrÁ\x0003hµ*L ´þ¸ÿUö^w_ÞãÁ­\x0007£\x000eØ3ª¤eü-sK£gU\x0011m\x00074\x001ego^àÁþqMß×´nñ¨ºÊf©Ëih0Â#£î4 :Ãæ\x000cñ¤`ErÓ\x0014±
EHª¶(\x001c¹'T£¼ÓGéª¢Öw\x000eù*¬IÎ\x001b \x001a*RÇßjÈºüõÓ÷O¡ç¥q«êæ±~wË"B½.z¥6Iã È4D-é;Ärý¶Ð³Ó,&4Ìæð[¦©lÚó¥-tD[(ÁIj+¢U\x00124\x0016îÓW%\x001c¶\x0000¦jBGË÷ËÛ-V7:E¥×ÆP\x0011e$\x0010ñ¦^²£ùùiß\x0013]á!«WÌ(0Øtùz-|\x001eh
`dÜJØ~ý{nìÞÆ?>`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=»ø2Ö!îX«¸÷r¬¾d¶\x000b\x0015YÌè"\x0010 '\x001eQ J\x0011ÇPñë</p><p>¬\x0001\x000c0\x0011\x0001Fwµ/ò</p><p>`\x0006Mx×KÁü®:k@°ONñ¯·ÿ¿\x000f³~UÅä\x0011¦,\x0017)23gø{\x00009{×Ä7$@ùÄ-XÒ\x0004\x0012\x0011\x0003?Uq\x001aä<\x00187÷\x0002¼\x0018¥¯P>½\x0011÷£Ts9\x0002Ùµ"²É\x0002¶\x0007C\x0015ÄÝ Å¢´Q\x0014àúVT\x00004\x0014J;]»\x0010¦\x001c¹iU5C©=å\x001f+fF\x001eNV±³~úMx)LY-KüÚ\x000cSkÏ\x0005Ø¡dê³Ê\x000eu\x0013!ñ\x0016£Ê\Äù¤2w	Î@ÝéÐöìØ\x0008Ã¡\x0014+·|\x0017âÔ&Ù¾m®Í\x000b¹sn~Ýî;ß±\x0015\x0008·QÐÜe\x00029qê(3óýfÏy\x0019ý¡lþA¼¿½ÁÒæ\x001fï¶n\x001a$(%zý'9N½ôÕ×OÚï/NO°ÈùÍõùæìdGéãûí\x000fÛÏ_`þø/; e\x001cNâ+Q»R_R$"Ýò]ç!\x001dZ1j-Ö£«fQí\x001e½\x0015Ú?¼.T7Ô£|C\x0014</p><p>\x0007 \x0014_OOTá¡DI-õuÑA¨mµ¬íúum`\x001fû^Q"r¥=\x0013ýÆzT\x001fÎÐõ¨*+\x0004,íP<Ô\x001dµ¯\x0016_¿@¬ÖÇrè\x001aÃ mYÖ;Ú\x001d\x0007¡\x000eÕP\x0003\x001an\x000f9,kn\x0005äJå×Î\x001bÜ!¨Qs|ð\x0003Î\x0010¼§Y2xÜàs{\·ãZ</p><p>[£>`°}©E\x0015JOÂ¢´}ó¦#l_Ã>à\x0010qó½°;àvQºâ­ê·FF¾\x0005ÂNÊ kGÛ®dJpÑ ;Ø\x0017vÝ\x00119ª¬H°õjØ\x000ecÖ,u$â\x0012lSÎ£­ëE¢\x000fX$XoA\x0007_º\x000c©b@\x0019Ý\x000fu}©Ë\x0003nulf\x0015e-\x0008v)¾ÆfîÝ`Û\x001a¶=\x0000¶NÖ^>H"*@dÓzèG\x0018ºÝ58´M×vº\x0017y´\x001d6?­îF§\x000eíëËÆ¯¿lt\x001cÄvyîoc\x0011¶ÝL?\x0014F\x001dÃ\x000e\x0007\x001c$j¨RP¦¾ôµ2¡ÛT²\x001aí,§º\x0012¶ç¬ ÜÑº_
½H½î¶HÔè,Áëa\x001bWª\x000b@ç<v,d¬#\x0007\x0007ÁÖÕÌÒ¬kG;R\\x0006õ\x0008°QS\x001aíá¶ñ¶ß"±%\x0005\WÂ¢ØÎrZ\x0001ìÃR.®ºmI\x0015«K2ë¼®íµà\x0007U¥ù\x0000´¬ô!»Ý5º¶þô\x0001Ö_Ò¥c\x0004(\x0006g¥\x001bïf´¢Fì\x0018¶\EÁq,)Ýz8ýl1H6Ý®H=*FØIYv%llNF9RÆ !`u8FàóCUÅ\x0005;U\WÛYé¸T¹@/Mø\x001aÆ®Z\x0016é¸©\x001a³«
jÇMcÓ¶\x000e`_\x0006d\x001aØe=n8\x0003\x001b_Â80î4Ï|îy)'7»y\x001e£ÿðÃ/ÆÝÿð!\x000b~fÏ÷·>mLÝâ	\x0007@¿Üüúpÿøù\x0006!Y-`nÖ\x0014\x001cTphÁþ9Þ;ÔÑoA[J,{{ò§Ëë«\x0017ïOÏÎ6¯OH:x</p><p>Dz'K\x001f\x000b@(,\x0008L\x000fè\x0000Â$¹!Dá4¶K(èýü	©Á -BÎoÊ?HùMOnrÉçw·\x000f÷w?ÜÀ÷Ï³#$a%%s\x001cÀÅ¤ÜàA-©\x0004\x001b[\x0017t³³\ûùÝéåÅù7'ð}*+}ÀJÏ\x001dWaÕ\x0007ÒÉTt°jÆjr=°º</p><p>«[2DSÓNò$¬x\x0011V\x0012/9\x0010«·c¬ðm
VØ­J\x0012VñU\x0012RÙ\x0001§´\x0015ÎÜ×\x000e4yjLÉû\x0019ßhPc\x000f°ä1Xô¿Vuô°`S^s\x0002kð^Éã*º,å]\x0017°q\x001dØP«LUS\x0019¬é»µø!Áúu#kC¶ qdSÃç\x000465[É`]\x0017°±^³qÝÅ8Á%\x0017	¬ÄÖBé¶ÇA c=²qÝÈ¢þ«/'¬ÊXñÑ\x0006Þ\x000f×b¥ìW«^\x000c?xîÎåýã\x0017</p><p>6ÆÍ×ûÇ¿Í^¨Á©¬{^BUgiPj$ÁTâu\x0005&|¾C`d¼¿¸þ·ý\x0008C04#\x00149Ñ\x0006\x0010J´}2B\x0017è RÊù\x0003\x0011º</p><p>¡kFh%Nàdà«qB\x0008N3#\x0014ñ@Ã^G¸ÕÛ\x0010\x0002\x0010	¡ácLdrw7#Õ:ÍëP+\x001eCef\x0012B­\x0019 \x0008\x0001B\x0001Ê$oÔP¹l\x0003B\x0014=§¢\x000c2îZ!Í\x0010)!&Á&Bå\x001f\x0004ß\x0010¢§Y\x001c<*Ô\x0010[÷Çè@\x00105ö\x0017L\x0010Q`F1Ê\x0003!êz\x0014uë(ú¨óû-BL2L\x0019¢,\x0013íí\x0010mµ¥mÝÏp¸`sé´u*ÝL\x0010$\x0013\x0003\x0016å¾\x0013'{e\x0013ø|=¾y\x0008Á^#_\x0011\x00151°ø';X\x0006wà­"\x0007c=C´Í\x0010U\x0000`p6Åµ2DAC(ý®IÙ\x000c1È</p><p>"J1·A´>W\x001f\x0019|eÀ¿&·3\x001cÚæ@±ÞÎ±y;k[\x000eEëøê\x0003\x0013Øð(îZd­\x0010¨&:Ã4C4´a¯ðD£´Dh\x000f¼©n\x0016eZo\x0016\x0017\x0003»bzð\x0019\x0015&\x0015f&\x001e8ÏÊVK\x0011¿¶BåØÎRü	¢a\x0013G\x001a(ÄXøµ\x0011"\x0000!{\x001b«àbgt2D}à£IÌ ê$æÝ\x0004QÒ\x0007@«\x0002\x0019Òy>sÔêÞÂ¥òaÈzô\x001f6¨Â\x0005Ó|vÿåöóçoî¾¤ÜûÛY\x001a,¹Ü9\x0005îàØoñ\x0016#Ø;¦âÙÅ»Ó««7'çïRIîåÅé\x0002jS­À)ÈI¤\x0006]W¾¦Sâ\x000cÔiÛ\x0003¨\x001e\x0003Õk:vN\x0002êSjX</p><p>	9Ç#êw­²u@Í\x0018¨Y\x00054ò}:3PÍÅÀ#j\x000fz®õ\x001aí¢77+\x0000&u)lë3ëW+,fPdûØ\x0004Ò</p><p>]Pîî¡$¯$¦°¯ÏK\x0001*=\x00068È.\x0006¨r!Z^4ßàk±KíÂîAÔPË1B¬+jC´\x001dó\x0014Å_-~5=\x0000 ©\x0000æ!Ã\x0019$y%ZÁ^âö\x0007 ¬V¡n_¹</p><p>0b\x0005H\x001eÂP\x0000ê]ë±\x0015à((\x0011((Ñ\x0004\x00106s Ç\x0008)Ø¨0£ZÊC'Ù«1B¯\x0011úÜ¹\x001c\x0011*|ãÊ\x0008Ed»\x0007x;Âj\x0019úæe\x0008'·&\x0006oî\x001c\x001bãóPË÷ÉÈA¶\x0015 ØÜd9Z\x0011ÐåÊ±1O±1\x000fº\x0007"t\x0015B×<6·Ã1tå0ô\x001c½\x0003#êà1¬6oß(v²%Ìxv_´nãP-ÁÐ¼\x0004Á\x0007Ôá±'=D?\x0001á®ûÒPªê2Á¯\x0010eÌ¹C\x0000QÓ\x0008J>©µ>t\x00049§¶àk>gb³</p><p></p><p>(p'\x0019bÜ
~¶B´Å_Û zL\x0008"·1X\x0013Bãôj1+\x0015\x000c×\x001dª9ûáE#uÚ;ù²½ûñè_\x001foï>ßßíñ\x0004í8G\x001b\x001a³¡(Ä(w ò³ÆÑÙÑÉ»Íùë£½>=¿º8ß\x000bÙ1d|:_
¹<Èa\x000eMÎ«-\x0006´Ý0Ç</p><p>s\9p0\ràGÁ7\x001eä`;\x0001vz\x000cØé\x0003\x0000Ûø-gf(lÿD¬:\x000crV\x001d\x000e(R\x0001/iª\x0010æ\x001f?Ý~ÞF"CÎSB\x0013=ò5e\x0015û]ó´U\x0012Ø×g§WSõøf¤Ä\x0007O<%óJ\x001eØ«í-øcïï~wÃX\x0001\x0016Êl¿¹À¡|îG±3WSðÅ6o.Î§$jG\x0008Õ\x0018¡jG\x0008©/îb\x001eCçÙöm÷l¶K\x000bBiª14k â*\x0006Ã\x0010\x0019¡|öm»\x0005¡®ÆP·\x000fbåK\x0010aGÂ
¯&\x001cÑU\x0018]#F\x0015c</p><p>ágm\x0010g\x0006þp¾ÂèÛgÚær]|\x0011I
òvQ\x001c\x00150êàýbÄ\x0018£\x0011ísíÊ[»N|y9J^f×VjÇ8Ê
Âæ\x0005¶}\x001cu.\x00145©§®fUÊ\x001eÑU'£k?\x001ae§¶Q0jÆ(ãÁs\x001dª¹\x000e­s­°\x0007\x0013I)'Ö£±¼\x001e¥6ý£	c5×¡u®\x0001ã(+@\x001e3D¶:ÜM[h(e¨\x000epÌnÄè$çTê\ynê!&v}ð\x0015 c
2¶ôÅÀ\x000c©Y\x001aIÁÉòàPªê\x000cÇ¯­\x0018­ÉR\x001bdSRØ´d\x0006¨g-Ê&õ0ªöa\x0004_¢~©k'Eý¢.\x000fïâÐ=#mmÙÖÃGEí8 ¡½äCÜ:6\x001dexÞh\x0002©kº\x0019¤\x0002kG\x0015\x001c?µ<ÝòÉ#N\x0003H%²\x0015^l3øA\x0012|:ýùíçÏ)½ýýÍÃI^c.?N\x0016·\x001cs\x0018è¦)É*Zï.ÉÓ7o7WW)ÁýýÉåëI\x0001ã0Û\x0011'»\x0011£p¹v\x0018£/¦ÜNøÐî\x0011ÙÑù1FÌekÂÖYm0ÀÔ"=\x000f¢]?2¹XcÓ\x000cþ³züèùúÓöá\x0006|Ã½¦\x0019{2AptÃâÍÝm]^=_m.OÀ)ÜQ\\x0019åâª\x0019d(G¸±%£Æ»bSØ8õz¼\x0018¤\x0015H)AÆáY$§ä'Ovg&\x0013!\x0017CT5DÕ\x000cQJì@¯\x0019\x001fË8>yCl\x0007éª\x0005ºA5t¡¤Oyön~è\x000cåEv7VÑ\x000erTL «ü¤e }	¨`?1Ê\x000cÞgÄ'±ýå HbftÔß `LÕ8\x000fóaËhFë±<ÁÛÀv\x000f¬È©ÜTs¹\x001f¡õcÖ·"´¡=c\x00146\x0008\x0000¾å\x001c\x0004P\x000e`\x00080½f´ ÔØp\x0012_ñ	´§uN«É<´\x0010\x0012c*µxo\x0008\x000bW¢ÍRXyOËrSOîéÅ\x0010c
1¶BcÜ-\x000bÇ7:®\x0004ÐÃÔ^pHÙL\x0008«ÍE\x0008±ñ\x000b½8QÃ´âÚ©¬Ò}\x0010·ÂÔ\x0011Ç
*vréø/KkÍ¦#¦j\x000eHù!²ãÌ@\x0018\x0005®\x001aÃUÿìpe=ºkWrªcìµ\x0012xÆ÷>p«Ñë\x0017Û¢e=NêdÙ³5ÅýFyÛ>xuW¯\x001d^Çep%q¸\x0000[^\x0016¼à</p><p>®ùg]½B¼Ù\x0006ç<\x0017»RïÐß]\x0008!JJ0*	WSB\x000e'ÛéÝg¿J³ñ\x001dº\x001c{1\x000e÷\x0014bT»ò±\x000b@\x0006Ã\x0001-|è³äãÁH\x0011­\x0005(O'¶hW@ax>U° Ê\x0019\x001fwïÒöTCÅU\x001aH»+ü¾\x001ffÌ*H\x0008\x0013»@%Ú\x0011FÁm\x000fÁ8äE$aWu\x0001F\x0011ÙÕ®H0¡³)mÒõ0M²?ÅàkÀ´óüØxñýûÛ=\x0011£ÈU\x0006mz¼yUÐÝ|Àâ£ãsãÅ«w\x0017§{J;\x0006&Ö µY\x0004=uÅ.u\]¯v×\x0000\x001d^o\x0011(¾Þ®\x0000j\x0004\x00073M\x0014åýÖsN¿BQøÃê</p><p>©^7¤¦¼ù`\x000e=¹HsûUÜ}ZtÈ\x0007E¤Z®EÊË\x0014\x000e)rD¬ã¹»Y2«V¯×M¾\¹\x0003G;ÆçòäsAÝg´UH«¯Wî|[RÔ}ü¡ýT\x0012m9\x001céàÄ#RcÖm(É9êV(~>µì'k±k´\x0000ÝÜ(uJ\x000f@vSé\x001bK«x*A&QÊÀwj§¾´ÀZåbðQ\x0004Á\x0004Inþò°½ûþ§=w\x0015÷·Ë\x0000ÃÉZÔ\x0016ìT0\x0007½¿o/7çp{í\x0005;Ø'	¬Ýuõ\x0017
üëüÄáf°»ïý«À*cÇ`ñk;XR|dP¡öæè2×ña<à °"!\x000f\x0016P`RÆÎ.ÛÜ}{swwsôzû°Ç\x0006t&kdbVæ\x0003ÌøÈÑ</p><p>¿[`Zí6À{zr~~rôz3)î?|ùy¡\x00180/Q±\x0016âåýíç£·7\x000f\x000f·{\x001e?0¹XäN`ïd\x0019|\x0006xßóòâôêèíÉå%jg3º\x000c¢Ñ\x001f¦Øù\x0007/è\x00113©*¼úiûøóÞDNÏ\x0015Ú\x001at(_µm7ggIPáÕwë7°×3¨ô¹Ì¨12£\x001aÁ)$¹Æ05@OÈ\x0004WAÚ]¹\x0001X5d¦uÈà÷Sn.ü°  \x0017þúL+Ö\x000fY¬ÅFd°ò¥)CF1x\x0013­gd»}ÈÌ7?þú}¾\x0013a\x0003á³íÑåö+lÈÜR\x0012\x001cóâìæèíýíoÛ/ÿr¶æ×Û-vêÒ°GÊ¿z\x0011\x0005æ³¢Åî¬3àpàË/æ6zj*-a ³KyrôöâôÏwÿr/©º<Ý¼\x0003ìG÷°I§\x001bT1ã¡\x000eÆÏ\x001b1C6i]&ÈÆ\x0010d³c: ÆS0ô@¬Dnõ\x000bÁïHz8jC¬uè\x0004\x0019\x001b6â?ÐÂHÉ\x001eé£Ë8§l\x001a\x001ch\x0015ÄN'K\x001aè\ß\x00014`{>\x000e_Îêé\jÂ\x0019i¤©±\x0016t~ãî\x0001Ú"è>çá\x0015
n4Ðª¬^ãié£\x0003dÇÇFPYr\x0010![¬M¯\x00052hé£\x0003æ³qò8ëH C,ã,{Ö\x0008ºËÑ!EÖÜ"Ðù¸\x000b\x0018£í½8"b]0S3Í9I#f¯Ëqç:Æ"ôq8h\x0015²\x0018\x001f.iW:\x000cVã®Óµ"±æ8}tÀìrB8öï</p><p>¨á1YôÚø8>\x000e\x0007ÝChE\x0007¥Ñ\x0011tô\x000cÚ÷Ú¨>:e%íAåø´S±×¥Î\úè8ä\x0010\x001d\x000es</p><p>Õ&ÐI´®ï^k\x0003Ë(ÓG\x0007Ð¾lBï±]K\x0006mÊH\x0007Ó	4¦i§.#Í6Oúù4Ò\x0003èN\x000bÚà=hº\ð\x0013\x001eim}î¦ç¢@{qàyçú÷\x001fÝ`è\x0006CÌé\x0003\x0000\Ý?þ:6#¶Iä?\x001dv°r#
³ckTj3}§\x001c]]\¿lLZÕ\x0008V\x001f\x000c\x0016_hC\x0006ÉÔ15Ð\x001a?=º
h1Û7}\x001c\x0016ëuFëlî~
h-o;iýô\x0001×\x0000\x0017·[ú8\x0010.\x000fÒàº[}9ìî\x0018îÌ)±\x001c®Æîéã@¸Þô\x0000nH¢{	®R¼tý÷×\x0000\x0017_0ÓÇp±</p><p>öYThÈ¥Åà\x0003¹PÄû\x000f÷rú8\x0010.8OI»\x0002à¢ºF>\x0016tGWôØj\x001aõÒÇ¡p)É\x0010\x000f\x0006ø+\x001d\x000cBóèÚ\x0019'¤\x0005..\x0006øb°Éç@¸Þ§·\x0004×\x0019¶(;c¬íûåæ¯¿ýåßS°×âAh?\x001f½Ú>|Í	¯kHA\x000b°'En`7wÂ\x0002w=íç)¼WG¯6ï§aG%vÝH\x001f\x0007C÷°6÷\x0005È!·oÚå÷Ã\x0011c3}\x001cXæÆØËcº#¼JN»¤-\x0015FÒÇ¡½¥¼NK%ñ1 À.\x0018ìæ&È</p><p>!«\x001ea)\x0010bu·õäõ#àC­	°AÀ¦\x0007`%õ2bå	²V\x0005òt(¹
r@È¡\x0003d'sÂbL\x0016%vÔaÈvæbnÖ^ú8\x0018rô¹×\x000bBv[]\x0012\x0016Î}Q¶X¬>z\x0016^Òi¡ðàÈÇåµ¬ÔAG²þ	ü _Ð;Â|Íô\x0001ÞÑ«¶\x000f\x001fáv{ó°ÊA2ÞE:\x0012Ig\x0005`[eÉWaÎjÛàÃÓåËóóöÓæÃ]\x00087\x000fO:\x0016Ù:ý«á\x0007QÔx3\x001du\x0016Õt\x0005.\x0010¯¢ðy´±öü\x00021\x001fþöõ§»>\x0010*9âù\x0013°½||ø´½û!¿\x00127£\x0016!EêûÐG¢x²\x0017ÞçæÒY 5cf¼¼¾<Û3ÝF{\x0004Üb\x0002]þ<\x001c8«Ïóx -ç±Ñ»&ÔÞÎ\x0019G#ÔÏä\x000fRû­R\x001fr»á\x0017.îØ­²^Ú7cÒ&ËÆ¶*·SãÃq¯3¯^bG£</p><p>ó|1j,Z÷¾\x000bj|ôÚÁ¡øÉO gO\x0006Ð)é7}\x001c\x001aÓ¸Èê0\x0018mÉ7¢ôH¢£óLÚ`c2Cúè\x0000\x001b£ß6Ã6¢÷Ni:Att~Ö¾k\x0016©ûÀ\x0002Æ¢deBmØÆÆO¡~øñ?é6Ç\x0016~¼úé\x001e»p­\x001bÁpv.;*Ø®</`(( §¥Wß]`\x0017¯ý0K´å\x0010ÊæÌ\x000c3¿§:°$ÃvW\x0002uX´>Ö\x0003uØ@8?î)¯\x0003\x001flð/hÕj\x0012¨X\x0001ô'¸?¿\x0003né'£\x001aðQÏe\x0008«ïÉÓ½T\x001fç]¨|IO\x0001\x0016¿ý°½ý
ÛÉ!çüyuÿø\x0019Så/ïsÜ</p><p>ÓÂ§giCîz;ÿàMÉ#S¯.®¯0þò\x0002Sç&â<Äûï¿Þ¦ô3¸âì\x00005¥õ­»M¹Á</p><p>î7³	äð9¡&^Æ2þÁû×GýåëR
\x001dVÎ]ý</p><p>&ÄªàPmÎ¦\x0000j8N§\x0010<ÜÉrrÉ^ý	LçÒþãñ×ñ¾:¥P]ð J\x001fl\x0008G\x0005\x0007«¡JÓÎ2aÚ\x0017EéAÚ]sPËIu(TÅ\x000e]NüÎûÊ{_\x000eU;¹LA\x001dÎªÃ :\x0011Ò«@:¯lz©Kç\x0015\x0000ZM\x001b¼³HïVýí\x0017R JºS\x0008\x0014\x0013¦_=Ü|ÁÎ?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-T5D9dexZ/cCiUZh975uzyTlKbxM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-86EQoaZAvfTOi7RAh2+UJDJm2b8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-HSuDxH0A3TToXbLpTgvcCFykcNg`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-fON6yvvOQsyoQejlzuD6s2z2r/o`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8110-Xyb0v8ex0eRZ+eaRRBKsCVFPn/8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `95ae-oOWfcmDM0eDI944f/deNKDEwXlI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-fON6yvvOQsyoQejlzuD6s2z2r/o`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-0et8+JuflGKs31rYghEs50ClDXg`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-8LIGTYDLT8XjxMEJW7V5Jh01tDs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-2J6wyeHZbKRS+yfW5iM3V2FMihE`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>ᶞ�>C�ױg�\x0002�Fa��n�$�)�L</p>
  
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
