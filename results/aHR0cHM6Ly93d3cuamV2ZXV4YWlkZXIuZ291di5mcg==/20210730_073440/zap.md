
# ZAP Scanning Report

Generated on Fri, 30 Jul 2021 07:24:10


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 10 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Source Code Disclosure - Java | Medium | 1 | 
| Sub Resource Integrity Attribute Missing | Medium | 8 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Cookie No HttpOnly Flag | Low | 1 | 
| Cookie without SameSite Attribute | Low | 1 | 
| Cookie Without Secure Flag | Low | 1 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Private IP Disclosure | Low | 1 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Retrieved from Cache | Informational | 8 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 15 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 7 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://www.notion.so/JeVeuxAider-gouv-fr-pour-les-coles-et-les-universit-s-a9a595aa05a044b3a1944533a48e71d8" class="custom-link btn border-width-0 btn-color-893878 btn-outline btn-icon-left" target="_blank">Consulter le centre d'aide</a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a target="_blank" rel="noopener" href="https://reserve-civique.crisp.help/fr/" class="ml-1 font-semibold tracking-wide uppercase bg-gray-50 text-xxs text-gray-500 hover:text-blue-800 px-4 xl:px-10 py-2 transition ease-in-out duration-150" data-v-772e0926>
            Centre d'aide
          </a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/69c289c.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/69c289c.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class f{constructor(t){const e=this;for(let i=0;i<t.length;i+=1)e[i]=t[i];return e.length=t.length,this}}function h(t,e){const n=[];let i=0;if(t&&!e&&t instanceof f)return t;if(t)if("string"==typeof t){let r,o;const html=t.trim();if(html.indexOf("<")>=0&&html.indexOf(">")>=0){let t="div";for(0===html.indexOf("<li")&&(t="ul"),0===html.indexOf("<tr")&&(t="tbody"),0!==html.indexOf("<td")&&0!==html.indexOf("<th")||(t="tr"),0===html.indexOf("<tbody")&&(t="table"),0===html.indexOf("<option")&&(t="select"),o=l.createElement(t),o.innerHTML=html,i=0;i<o.childNodes.length;i+=1)n.push(o.childNodes[i])}else for(r=e||"#"!==t[0]||t.match(/[ .<>:~]/)?(e||l).querySelectorAll(t.trim()):[l.getElementById(t.trim().split("#")[1])],i=0;i<r.length;i+=1)r[i]&&n.push(r[i])}else if(t.nodeType||t===d||t===l)n.push(t);else if(t.length>0&&t[0].nodeType)for(i=0;i<t.length;i+=1)n.push(t[i]);return new f(n)}function v(t){const e=[];for(let i=0;i<t.length;i+=1)-1===e.indexOf(t[i])&&e.push(t[i]);return e}h.fn=f.prototype,h.Class=f,h.Dom7=f;"resize scroll".split(" ");const m={addClass:function(t){if(void 0===t)return this;const e=t.split(" ");for(let i=0;i<e.length;i+=1)for(let t=0;t<this.length;t+=1)void 0!==this[t]&&void 0!==this[t].classList&&this[t].classList.add(e[i]);return this},removeClass:function(t){const e=t.split(" ");for(let i=0;i<e.length;i+=1)for(let t=0;t<this.length;t+=1)void 0!==this[t]&&void 0!==this[t].classList&&this[t].classList.remove(e[i]);return this},hasClass:function(t){return!!this[0]&&this[0].classList.contains(t)},toggleClass:function(t){const e=t.split(" ");for(let i=0;i<e.length;i+=1)for(let t=0;t<this.length;t+=1)void 0!==this[t]&&void 0!==this[t].classList&&this[t].classList.toggle(e[i]);return this},attr:function(t,e){if(1===arguments.length&&"string"==typeof t)return this[0]?this[0].getAttribute(t):void 0;for(let i=0;i<this.length;i+=1)if(2===arguments.length)this[i].setAttribute(t,e);else for(const e in t)this[i][e]=t[e],this[i].setAttribute(e,t[e]);return this},removeAttr:function(t){for(let i=0;i<this.length;i+=1)this[i].removeAttribute(t);return this},data:function(t,e){let n;if(void 0!==e){for(let i=0;i<this.length;i+=1)n=this[i],n.dom7ElementDataStorage||(n.dom7ElementDataStorage={}),n.dom7ElementDataStorage[t]=e;return this}if(n=this[0],n){if(n.dom7ElementDataStorage&&t in n.dom7ElementDataStorage)return n.dom7ElementDataStorage[t];const e=n.getAttribute(`data-${t}`);return e||void 0}},transform:function(t){for(let i=0;i<this.length;i+=1){const e=this[i].style;e.webkitTransform=t,e.transform=t}return this},transition:function(t){"string"!=typeof t&&(t=`${t}ms`);for(let i=0;i<this.length;i+=1){const e=this[i].style;e.webkitTransitionDuration=t,e.transitionDuration=t}return this},on:function(...t){let[e,n,r,o]=t;function l(t){const e=t.target;if(!e)return;const o=t.target.dom7EventData||[];if(o.indexOf(t)<0&&o.unshift(t),h(e).is(n))r.apply(e,o);else{const t=h(e).parents();for(let e=0;e<t.length;e+=1)h(t[e]).is(n)&&r.apply(t[e],o)}}function c(t){const e=t&&t.target&&t.target.dom7EventData||[];e.indexOf(t)<0&&e.unshift(t),r.apply(this,e)}"function"==typeof t[1]&&([e,r,o]=t,n=void 0),o||(o=!1);const d=e.split(" ");let f;for(let i=0;i<this.length;i+=1){const t=this[i];if(n)for(f=0;f<d.length;f+=1){const e=d[f];t.dom7LiveListeners||(t.dom7LiveListeners={}),t.dom7LiveListeners[e]||(t.dom7LiveListeners[e]=[]),t.dom7LiveListeners[e].push({listener:r,proxyListener:l}),t.addEventListener(e,l,o)}else for(f=0;f<d.length;f+=1){const e=d[f];t.dom7Listeners||(t.dom7Listeners={}),t.dom7Listeners[e]||(t.dom7Listeners[e]=[]),t.dom7Listeners[e].push({listener:r,proxyListener:c}),t.addEventListener(e,c,o)}}return this},off:function(...t){let[e,n,r,o]=t;"function"==typeof t[1]&&([e,r,o]=t,n=void 0),o||(o=!1);const l=e.split(" ");for(let i=0;i<l.length;i+=1){const t=l[i];for(let e=0;e<this.length;e+=1){const l=this[e];let c;if(!n&&l.dom7Listeners?c=l.dom7Listeners[t]:n&&l.dom7LiveListeners&&(c=l.dom7LiveListeners[t]),c&&c.length)for(let e=c.length-1;e>=0;e-=1){const n=c[e];r&&n.listener===r||r&&n.listener&&n.listener.dom7proxy&&n.listener.dom7proxy===r?(l.removeEventListener(t,n.proxyListener,o),c.splice(e,1)):r||(l.removeEventListener(t,n.proxyListener,o),c.splice(e,1))}}}return this},trigger:function(...t){const e=t[0].split(" "),n=t[1];for(let i=0;i<e.length;i+=1){const r=e[i];for(let e=0;e<this.length;e+=1){const o=this[e];let c;try{c=new d.CustomEvent(r,{detail:n,bubbles:!0,cancelable:!0})}catch(t){c=l.createEvent("Event"),c.initEvent(r,!0,!0),c.detail=n}o.dom7EventData=t.filter(((data,t)=>t>0)),o.dispatchEvent(c),o.dom7EventData=[],delete o.dom7EventData}}return this},transitionEnd:function(t){const e=["webkitTransitionEnd","transitionend"],n=this;let i;function r(o){if(o.target===this)for(t.call(this,o),i=0;i<e.length;i+=1)n.off(e[i],r)}if(t)for(i=0;i<e.length;i+=1)n.on(e[i],r);return this},outerWidth:function(t){if(this.length>0){if(t){const t=this.styles();return this[0].offsetWidth+parseFloat(t.getPropertyValue("margin-right"))+parseFloat(t.getPropertyValue("margin-left"))}return this[0].offsetWidth}return null},outerHeight:function(t){if(this.length>0){if(t){const t=this.styles();return this[0].offsetHeight+parseFloat(t.getPropertyValue("margin-top"))+parseFloat(t.getPropertyValue("margin-bottom"))}return this[0].offsetHeight}return null},offset:function(){if(this.length>0){const t=this[0],e=t.getBoundingClientRect(),body=l.body,n=t.clientTop||body.clientTop||0,r=t.clientLeft||body.clientLeft||0,o=t===d?d.scrollY:t.scrollTop,c=t===d?d.scrollX:t.scrollLeft;return{top:e.top+o-n,left:e.left+c-r}}return null},css:function(t,e){let i;if(1===arguments.length){if("string"!=typeof t){for(i=0;i<this.length;i+=1)for(let e in t)this[i].style[e]=t[e];return this}if(this[0])return d.getComputedStyle(this[0],null).getPropertyValue(t)}if(2===arguments.length&&"string"==typeof t){for(i=0;i<this.length;i+=1)this[i].style[t]=e;return this}return this},each:function(t){if(!t)return this;for(let i=0;i<this.length;i+=1)if(!1===t.call(this[i],i,this[i]))return this;return this},html:function(html){if(void 0===html)return this[0]?this[0].innerHTML:void 0;for(let i=0;i<this.length;i+=1)this[i].innerHTML=html;return this},text:function(text){if(void 0===text)return this[0]?this[0].textContent.trim():null;for(let i=0;i<this.length;i+=1)this[i].textContent=text;return this},is:function(t){const e=this[0];let n,i;if(!e||void 0===t)return!1;if("string"==typeof t){if(e.matches)return e.matches(t);if(e.webkitMatchesSelector)return e.webkitMatchesSelector(t);if(e.msMatchesSelector)return e.msMatchesSelector(t);for(n=h(t),i=0;i<n.length;i+=1)if(n[i]===e)return!0;return!1}if(t===l)return e===l;if(t===d)return e===d;if(t.nodeType||t instanceof f){for(n=t.nodeType?[t]:t,i=0;i<n.length;i+=1)if(n[i]===e)return!0;return!1}return!1},index:function(){let i,t=this[0];if(t){for(i=0;null!==(t=t.previousSibling);)1===t.nodeType&&(i+=1);return i}},eq:function(t){if(void 0===t)return this;const e=this.length;let n;return t>e-1?new f([]):t<0?(n=e+t,new f(n<0?[]:[this[n]])):new f([this[t]])},append:function(...t){let e;for(let n=0;n<t.length;n+=1){e=t[n];for(let i=0;i<this.length;i+=1)if("string"==typeof e){const t=l.createElement("div");for(t.innerHTML=e;t.firstChild;)this[i].appendChild(t.firstChild)}else if(e instanceof f)for(let t=0;t<e.length;t+=1)this[i].appendChild(e[t]);else this[i].appendChild(e)}return this},prepend:function(t){let i,e;for(i=0;i<this.length;i+=1)if("string"==typeof t){const n=l.createElement("div");for(n.innerHTML=t,e=n.childNodes.length-1;e>=0;e-=1)this[i].insertBefore(n.childNodes[e],this[i].childNodes[0])}else if(t instanceof f)for(e=0;e<t.length;e+=1)this[i].insertBefore(t[e],this[i].childNodes[0]);else this[i].insertBefore(t,this[i].childNodes[0]);return this},next:function(t){return this.length>0?t?this[0].nextElementSibling&&h(this[0].nextElementSibling).is(t)?new f([this[0].nextElementSibling]):new f([]):this[0].nextElementSibling?new f([this[0].nextElementSibling]):new f([]):new f([])},nextAll:function(t){const e=[];let n=this[0];if(!n)return new f([]);for(;n.nextElementSibling;){const r=n.nextElementSibling;t?h(r).is(t)&&e.push(r):e.push(r),n=r}return new f(e)},prev:function(t){if(this.length>0){const e=this[0];return t?e.previousElementSibling&&h(e.previousElementSibling).is(t)?new f([e.previousElementSibling]):new f([]):e.previousElementSibling?new f([e.previousElementSibling]):new f([])}return new f([])},prevAll:function(t){const e=[];let n=this[0];if(!n)return new f([]);for(;n.previousElementSibling;){const r=n.previousElementSibling;t?h(r).is(t)&&e.push(r):e.push(r),n=r}return new f(e)},parent:function(t){const e=[];for(let i=0;i<this.length;i+=1)null!==this[i].parentNode&&(t?h(this[i].parentNode).is(t)&&e.push(this[i].parentNode):e.push(this[i].parentNode));return h(v(e))},parents:function(t){const e=[];for(let i=0;i<this.length;i+=1){let n=this[i].parentNode;for(;n;)t?h(n).is(t)&&e.push(n):e.push(n),n=n.parentNode}return h(v(e))},closest:function(t){let e=this;return void 0===t?new f([]):(e.is(t)||(e=e.parents(t).eq(0)),e)},find:function(t){const e=[];for(let i=0;i<this.length;i+=1){const n=this[i].querySelectorAll(t);for(let t=0;t<n.length;t+=1)e.push(n[t])}return new f(e)},children:function(t){const e=[];for(let i=0;i<this.length;i+=1){const n=this[i].childNodes;for(let r=0;r<n.length;r+=1)t?1===n[r].nodeType&&h(n[r]).is(t)&&e.push(n[r]):1===n[r].nodeType&&e.push(n[r])}return new f(v(e))},filter:function(t){const e=[],n=this;for(let i=0;i<n.length;i+=1)t.call(n[i],i,n[i])&&e.push(n[i]);return new f(e)},remove:function(){for(let i=0;i<this.length;i+=1)this[i].parentNode&&this[i].parentNode.removeChild(this[i]);return this},add:function(...t){const e=this;let i,n;for(i=0;i<t.length;i+=1){const r=h(t[i]);for(n=0;n<r.length;n+=1)e[e.length]=r[n],e.length+=1}return e},styles:function(){return this[0]?d.getComputedStyle(this[0],null):{}}};Object.keys(m).forEach((t=>{h.fn[t]=h.fn[t]||m[t]}));const y={deleteProps(t){const object=t;Object.keys(object).forEach((t=>{try{object[t]=null}catch(t){}try{delete object[t]}catch(t){}}))},nextTick:(t,e=0)=>setTimeout(t,e),now:()=>Date.now(),getTranslate(t,e="x"){let n,r,o;const l=d.getComputedStyle(t,null);return d.WebKitCSSMatrix?(r=l.transform||l.webkitTransform,r.split(",").length>6&&(r=r.split(", ").map((a=>a.replace(",","."))).join(", ")),o=new d.WebKitCSSMatrix("none"===r?"":r)):(o=l.MozTransform||l.OTransform||l.MsTransform||l.msTransform||l.transform||l.getPropertyValue("transform").replace("translate(","matrix(1, 0, 0, 1,"),n=o.toString().split(",")),"x"===e&&(r=d.WebKitCSSMatrix?o.m41:16===n.length?parseFloat(n[12]):parseFloat(n[4])),"y"===e&&(r=d.WebKitCSSMatrix?o.m42:16===n.length?parseFloat(n[13]):parseFloat(n[5])),r||0},parseUrlQuery(t){const e={};let i,n,param,r,o=t||d.location.href;if("string"==typeof o&&o.length)for(o=o.indexOf("?")>-1?o.replace(/\S*\?/,""):"",n=o.split("&").filter((t=>""!==t)),r=n.length,i=0;i<r;i+=1)param=n[i].replace(/#\S+/g,"").split("="),e[decodeURIComponent(param[0])]=void 0===param[1]?void 0:decodeURIComponent(param[1])||"";return e},isObject:t=>"object"==typeof t&&null!==t&&t.constructor&&t.constructor===Object,extend(...t){const e=Object(t[0]);for(let i=1;i<t.length;i+=1){const n=t[i];if(null!=n){const t=Object.keys(Object(n));for(let r=0,o=t.length;r<o;r+=1){const o=t[r],desc=Object.getOwnPropertyDescriptor(n,o);void 0!==desc&&desc.enumerable&&(y.isObject(e[o])&&y.isObject(n[o])?y.extend(e[o],n[o]):!y.isObject(e[o])&&y.isObject(n[o])?(e[o]={},y.extend(e[o],n[o])):e[o]=n[o])}}}return e}},_={touch:!!("ontouchstart"in d||d.DocumentTouch&&l instanceof d.DocumentTouch),pointerEvents:!!d.PointerEvent&&"maxTouchPoints"in d.navigator&&d.navigator.maxTouchPoints>=0,observer:"MutationObserver"in d||"WebkitMutationObserver"in d,passiveListener:function(){let t=!1;try{const e=Object.defineProperty({},"passive",{get(){t=!0}});d.addEventListener("testPassiveListener",null,e)}catch(t){}return t}(),gestures:"ongesturestart"in d};class w{constructor(t={}){const e=this;e.params=t,e.eventsListeners={},e.params&&e.params.on&&Object.keys(e.params.on).forEach((t=>{e.on(t,e.params.on[t])}))}on(t,e,n){const r=this;if("function"!=typeof e)return r;const o=n?"unshift":"push";return t.split(" ").forEach((t=>{r.eventsListeners[t]||(r.eventsListeners[t]=[]),r.eventsListeners[t][o](e)})),r}once(t,e,n){const r=this;if("function"!=typeof e)return r;function o(...n){r.off(t,o),o.f7proxy&&delete o.f7proxy,e.apply(r,n)}return o.f7proxy=e,r.on(t,o,n)}off(t,e){const n=this;return n.eventsListeners?(t.split(" ").forEach((t=>{void 0===e?n.eventsListeners[t]=[]:n.eventsListeners[t]&&n.eventsListeners[t].length&&n.eventsListeners[t].forEach(((r,o)=>{(r===e||r.f7proxy&&r.f7proxy===e)&&n.eventsListeners[t].splice(o,1)}))})),n):n}emit(...t){const e=this;if(!e.eventsListeners)return e;let n,data,r;"string"==typeof t[0]||Array.isArray(t[0])?(n=t[0],data=t.slice(1,t.length),r=e):(n=t[0].events,data=t[0].data,r=t[0].context||e);return(Array.isArray(n)?n:n.split(" ")).forEach((t=>{if(e.eventsListeners&&e.eventsListeners[t]){const n=[];e.eventsListeners[t].forEach((t=>{n.push(t)})),n.forEach((t=>{t.apply(r,data)}))}})),e}useModulesParams(t){const e=this;e.modules&&Object.keys(e.modules).forEach((n=>{const r=e.modules[n];r.params&&y.extend(t,r.params)}))}useModules(t={}){const e=this;e.modules&&Object.keys(e.modules).forEach((n=>{const r=e.modules[n],o=t[n]||{};r.instance&&Object.keys(r.instance).forEach((t=>{const n=r.instance[t];e[t]="function"==typeof n?n.bind(e):n})),r.on&&e.on&&Object.keys(r.on).forEach((t=>{e.on(t,r.on[t])})),r.create&&r.create.bind(e)(o)}))}static set components(t){this.use&&this.use(t)}static installModule(t,...e){const n=this;n.prototype.modules||(n.prototype.modules={});const r=t.name||`${Object.keys(n.prototype.modules).length}_${y.now()}`;return n.prototype.modules[r]=t,t.proto&&Object.keys(t.proto).forEach((e=>{n.prototype[e]=t.proto[e]})),t.static&&Object.keys(t.static).forEach((e=>{n[e]=t.static[e]})),t.install&&t.install.apply(n,e),n}static use(t,...e){const n=this;return Array.isArray(t)?(t.forEach((t=>n.installModule(t))),n):n.installModule(t,...e)}}var x={updateSize:function(){const t=this;let e,n;const r=t.$el;e=void 0!==t.params.width?t.params.width:r[0].clientWidth,n=void 0!==t.params.height?t.params.height:r[0].clientHeight,0===e&&t.isHorizontal()||0===n&&t.isVertical()||(e=e-parseInt(r.css("padding-left"),10)-parseInt(r.css("padding-right"),10),n=n-parseInt(r.css("padding-top"),10)-parseInt(r.css("padding-bottom"),10),y.extend(t,{width:e,height:n,size:t.isHorizontal()?e:n}))},updateSlides:function(){const t=this,e=t.params,{$wrapperEl:n,size:r,rtlTranslate:o,wrongRTL:l}=t,c=t.virtual&&e.virtual.enabled,f=c?t.virtual.slides.length:t.slides.length,h=n.children(`.${t.params.slideClass}`),v=c?t.virtual.slides.length:h.length;let m=[];const _=[],w=[];function x(t){return!e.cssMode||t!==h.length-1}let S=e.slidesOffsetBefore;"function"==typeof S&&(S=e.slidesOffsetBefore.call(t));let E=e.slidesOffsetAfter;"function"==typeof E&&(E=e.slidesOffsetAfter.call(t));const O=t.snapGrid.length,C=t.snapGrid.length;let T,k,j=e.spaceBetween,$=-S,M=0,A=0;if(void 0===r)return;"string"==typeof j&&j.indexOf("%")>=0&&(j=parseFloat(j.replace("%",""))/100*r),t.virtualSize=-j,o?h.css({marginLeft:"",marginTop:""}):h.css({marginRight:"",marginBottom:""}),e.slidesPerColumn>1&&(T=Math.floor(v/e.slidesPerColumn)===v/t.params.slidesPerColumn?v:Math.ceil(v/e.slidesPerColumn)*e.slidesPerColumn,"auto"!==e.slidesPerView&&"row"===e.slidesPerColumnFill&&(T=Math.max(T,e.slidesPerView*e.slidesPerColumn)));const I=e.slidesPerColumn,P=T/I,D=Math.floor(v/e.slidesPerColumn);for(let i=0;i<v;i+=1){k=0;const n=h.eq(i);if(e.slidesPerColumn>1){let r,o,l;if("row"===e.slidesPerColumnFill&&e.slidesPerGroup>1){const t=Math.floor(i/(e.slidesPerGroup*e.slidesPerColumn)),c=i-e.slidesPerColumn*e.slidesPerGroup*t,d=0===t?e.slidesPerGroup:Math.min(Math.ceil((v-t*I*e.slidesPerGroup)/I),e.slidesPerGroup);l=Math.floor(c/d),o=c-l*d+t*e.slidesPerGroup,r=o+l*T/I,n.css({"-webkit-box-ordinal-group":r,"-moz-box-ordinal-group":r,"-ms-flex-order":r,"-webkit-order":r,order:r})}else"column"===e.slidesPerColumnFill?(o=Math.floor(i/I),l=i-o*I,(o>D||o===D&&l===I-1)&&(l+=1,l>=I&&(l=0,o+=1))):(l=Math.floor(i/P),o=i-l*P);n.css("margin-"+(t.isHorizontal()?"top":"left"),0!==l&&e.spaceBetween&&`${e.spaceBetween}px`)}if("none"!==n.css("display")){if("auto"===e.slidesPerView){const r=d.getComputedStyle(n[0],null),o=n[0].style.transform,l=n[0].style.webkitTransform;if(o&&(n[0].style.transform="none"),l&&(n[0].style.webkitTransform="none"),e.roundLengths)k=t.isHorizontal()?n.outerWidth(!0):n.outerHeight(!0);else if(t.isHorizontal()){const t=parseFloat(r.getPropertyValue("width")),e=parseFloat(r.getPropertyValue("padding-left")),n=parseFloat(r.getPropertyValue("padding-right")),o=parseFloat(r.getPropertyValue("margin-left")),l=parseFloat(r.getPropertyValue("margin-right")),c=r.getPropertyValue("box-sizing");k=c&&"border-box"===c?t+o+l:t+e+n+o+l}else{const t=parseFloat(r.getPropertyValue("height")),e=parseFloat(r.getPropertyValue("padding-top")),n=parseFloat(r.getPropertyValue("padding-bottom")),o=parseFloat(r.getPropertyValue("margin-top")),l=parseFloat(r.getPropertyValue("margin-bottom")),c=r.getPropertyValue("box-sizing");k=c&&"border-box"===c?t+o+l:t+e+n+o+l}o&&(n[0].style.transform=o),l&&(n[0].style.webkitTransform=l),e.roundLengths&&(k=Math.floor(k))}else k=(r-(e.slidesPerView-1)*j)/e.slidesPerView,e.roundLengths&&(k=Math.floor(k)),h[i]&&(t.isHorizontal()?h[i].style.width=`${k}px`:h[i].style.height=`${k}px`);h[i]&&(h[i].swiperSlideSize=k),w.push(k),e.centeredSlides?($=$+k/2+M/2+j,0===M&&0!==i&&($=$-r/2-j),0===i&&($=$-r/2-j),Math.abs($)<.001&&($=0),e.roundLengths&&($=Math.floor($)),A%e.slidesPerGroup==0&&m.push($),_.push($)):(e.roundLengths&&($=Math.floor($)),(A-Math.min(t.params.slidesPerGroupSkip,A))%t.params.slidesPerGroup==0&&m.push($),_.push($),$=$+k+j),t.virtualSize+=k+j,M=k,A+=1}}let L;if(t.virtualSize=Math.max(t.virtualSize,r)+E,o&&l&&("slide"===e.effect||"coverflow"===e.effect)&&n.css({width:`${t.virtualSize+e.spaceBetween}px`}),e.setWrapperSize&&(t.isHorizontal()?n.css({width:`${t.virtualSize+e.spaceBetween}px`}):n.css({height:`${t.virtualSize+e.spaceBetween}px`})),e.slidesPerColumn>1&&(t.virtualSize=(k+e.spaceBetween)*T,t.virtualSize=Math.ceil(t.virtualSize/e.slidesPerColumn)-e.spaceBetween,t.isHorizontal()?n.css({width:`${t.virtualSize+e.spaceBetween}px`}):n.css({height:`${t.virtualSize+e.spaceBetween}px`}),e.centeredSlides)){L=[];for(let i=0;i<m.length;i+=1){let n=m[i];e.roundLengths&&(n=Math.floor(n)),m[i]<t.virtualSize+m[0]&&L.push(n)}m=L}if(!e.centeredSlides){L=[];for(let i=0;i<m.length;i+=1){let n=m[i];e.roundLengths&&(n=Math.floor(n)),m[i]<=t.virtualSize-r&&L.push(n)}m=L,Math.floor(t.virtualSize-r)-Math.floor(m[m.length-1])>1&&m.push(t.virtualSize-r)}if(0===m.length&&(m=[0]),0!==e.spaceBetween&&(t.isHorizontal()?o?h.filter(x).css({marginLeft:`${j}px`}):h.filter(x).css({marginRight:`${j}px`}):h.filter(x).css({marginBottom:`${j}px`})),e.centeredSlides&&e.centeredSlidesBounds){let t=0;w.forEach((n=>{t+=n+(e.spaceBetween?e.spaceBetween:0)})),t-=e.spaceBetween;const n=t-r;m=m.map((t=>t<0?-S:t>n?n+E:t))}if(e.centerInsufficientSlides){let t=0;if(w.forEach((n=>{t+=n+(e.spaceBetween?e.spaceBetween:0)})),t-=e.spaceBetween,t<r){const e=(r-t)/2;m.forEach(((t,n)=>{m[n]=t-e})),_.forEach(((t,n)=>{_[n]=t+e}))}}y.extend(t,{slides:h,snapGrid:m,slidesGrid:_,slidesSizesGrid:w}),v!==f&&t.emit("slidesLengthChange"),m.length!==O&&(t.params.watchOverflow&&t.checkOverflow(),t.emit("snapGridLengthChange")),_.length!==C&&t.emit("slidesGridLengthChange"),(e.watchSlidesProgress||e.watchSlidesVisibility)&&t.updateSlidesOffset()},updateAutoHeight:function(t){const e=this,n=[];let i,r=0;if("number"==typeof t?e.setTransition(t):!0===t&&e.setTransition(e.params.speed),"auto"!==e.params.slidesPerView&&e.params.slidesPerView>1)if(e.params.centeredSlides)e.visibleSlides.each(((t,e)=>{n.push(e)}));else for(i=0;i<Math.ceil(e.params.slidesPerView);i+=1){const t=e.activeIndex+i;if(t>e.slides.length)break;n.push(e.slides.eq(t)[0])}else n.push(e.slides.eq(e.activeIndex)[0]);for(i=0;i<n.length;i+=1)if(void 0!==n[i]){const t=n[i].offsetHeight;r=t>r?t:r}r&&e.$wrapperEl.css("height",`${r}px`)},updateSlidesOffset:function(){const t=this,e=t.slides;for(let i=0;i<e.length;i+=1)e[i].swiperSlideOffset=t.isHorizontal()?e[i].offsetLeft:e[i].offsetTop},updateSlidesProgress:function(t=this&&this.translate||0){const e=this,n=e.params,{slides:r,rtlTranslate:o}=e;if(0===r.length)return;void 0===r[0].swiperSlideOffset&&e.updateSlidesOffset();let l=-t;o&&(l=t),r.removeClass(n.slideVisibleClass),e.visibleSlidesIndexes=[],e.visibleSlides=[];for(let i=0;i<r.length;i+=1){const t=r[i],c=(l+(n.centeredSlides?e.minTranslate():0)-t.swiperSlideOffset)/(t.swiperSlideSize+n.spaceBetween);if(n.watchSlidesVisibility||n.centeredSlides&&n.autoHeight){const o=-(l-t.swiperSlideOffset),c=o+e.slidesSizesGrid[i];(o>=0&&o<e.size-1||c>1&&c<=e.size||o<=0&&c>=e.size)&&(e.visibleSlides.push(t),e.visibleSlidesIndexes.push(i),r.eq(i).addClass(n.slideVisibleClass))}t.progress=o?-c:c}e.visibleSlides=h(e.visibleSlides)},updateProgress:function(t){const e=this;if(void 0===t){const n=e.rtlTranslate?-1:1;t=e&&e.translate&&e.translate*n||0}const n=e.params,r=e.maxTranslate()-e.minTranslate();let{progress:progress,isBeginning:o,isEnd:l}=e;const c=o,d=l;0===r?(progress=0,o=!0,l=!0):(progress=(t-e.minTranslate())/r,o=progress<=0,l=progress>=1),y.extend(e,{progress:progress,isBeginning:o,isEnd:l}),(n.watchSlidesProgress||n.watchSlidesVisibility||n.centeredSlides&&n.autoHeight)&&e.updateSlidesProgress(t),o&&!c&&e.emit("reachBeginning toEdge"),l&&!d&&e.emit("reachEnd toEdge"),(c&&!o||d&&!l)&&e.emit("fromEdge"),e.emit("progress",progress)},updateSlidesClasses:function(){const t=this,{slides:e,params:n,$wrapperEl:r,activeIndex:o,realIndex:l}=t,c=t.virtual&&n.virtual.enabled;let d;e.removeClass(`${n.slideActiveClass} ${n.slideNextClass} ${n.slidePrevClass} ${n.slideDuplicateActiveClass} ${n.slideDuplicateNextClass} ${n.slideDuplicatePrevClass}`),d=c?t.$wrapperEl.find(`.${n.slideClass}[data-swiper-slide-index="${o}"]`):e.eq(o),d.addClass(n.slideActiveClass),n.loop&&(d.hasClass(n.slideDuplicateClass)?r.children(`.${n.slideClass}:not(.${n.slideDuplicateClass})[data-swiper-slide-index="${l}"]`).addClass(n.slideDuplicateActiveClass):r.children(`.${n.slideClass}.${n.slideDuplicateClass}[data-swiper-slide-index="${l}"]`).addClass(n.slideDuplicateActiveClass));let f=d.nextAll(`.${n.slideClass}`).eq(0).addClass(n.slideNextClass);n.loop&&0===f.length&&(f=e.eq(0),f.addClass(n.slideNextClass));let h=d.prevAll(`.${n.slideClass}`).eq(0).addClass(n.slidePrevClass);n.loop&&0===h.length&&(h=e.eq(-1),h.addClass(n.slidePrevClass)),n.loop&&(f.hasClass(n.slideDuplicateClass)?r.children(`.${n.slideClass}:not(.${n.slideDuplicateClass})[data-swiper-slide-index="${f.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicateNextClass):r.children(`.${n.slideClass}.${n.slideDuplicateClass}[data-swiper-slide-index="${f.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicateNextClass),h.hasClass(n.slideDuplicateClass)?r.children(`.${n.slideClass}:not(.${n.slideDuplicateClass})[data-swiper-slide-index="${h.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicatePrevClass):r.children(`.${n.slideClass}.${n.slideDuplicateClass}[data-swiper-slide-index="${h.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicatePrevClass))},updateActiveIndex:function(t){const e=this,n=e.rtlTranslate?e.translate:-e.translate,{slidesGrid:r,snapGrid:o,params:l,activeIndex:c,realIndex:d,snapIndex:f}=e;let h,v=t;if(void 0===v){for(let i=0;i<r.length;i+=1)void 0!==r[i+1]?n>=r[i]&&n<r[i+1]-(r[i+1]-r[i])/2?v=i:n>=r[i]&&n<r[i+1]&&(v=i+1):n>=r[i]&&(v=i);l.normalizeSlideIndex&&(v<0||void 0===v)&&(v=0)}if(o.indexOf(n)>=0)h=o.indexOf(n);else{const t=Math.min(l.slidesPerGroupSkip,v);h=t+Math.floor((v-t)/l.slidesPerGroup)}if(h>=o.length&&(h=o.length-1),v===c)return void(h!==f&&(e.snapIndex=h,e.emit("snapIndexChange")));const m=parseInt(e.slides.eq(v).attr("data-swiper-slide-index")||v,10);y.extend(e,{snapIndex:h,realIndex:m,previousIndex:c,activeIndex:v}),e.emit("activeIndexChange"),e.emit("snapIndexChange"),d!==m&&e.emit("realIndexChange"),(e.initialized||e.params.runCallbacksOnInit)&&e.emit("slideChange")},updateClickedSlide:function(t){const e=this,n=e.params,r=h(t.target).closest(`.${n.slideClass}`)[0];let o=!1;if(r)for(let i=0;i<e.slides.length;i+=1)e.slides[i]===r&&(o=!0);if(!r||!o)return e.clickedSlide=void 0,void(e.clickedIndex=void 0);e.clickedSlide=r,e.virtual&&e.params.virtual.enabled?e.clickedIndex=parseInt(h(r).attr("data-swiper-slide-index"),10):e.clickedIndex=h(r).index(),n.slideToClickedSlide&&void 0!==e.clickedIndex&&e.clickedIndex!==e.activeIndex&&e.slideToClickedSlide()}};var S={getTranslate:function(t=(this.isHorizontal()?"x":"y")){const{params:e,rtlTranslate:n,translate:r,$wrapperEl:o}=this;if(e.virtualTranslate)return n?-r:r;if(e.cssMode)return r;let l=y.getTranslate(o[0],t);return n&&(l=-l),l||0},setTranslate:function(t,e){const n=this,{rtlTranslate:r,params:o,$wrapperEl:l,wrapperEl:c,progress:progress}=n;let d,f=0,h=0;n.isHorizontal()?f=r?-t:t:h=t,o.roundLengths&&(f=Math.floor(f),h=Math.floor(h)),o.cssMode?c[n.isHorizontal()?"scrollLeft":"scrollTop"]=n.isHorizontal()?-f:-h:o.virtualTranslate||l.transform(`translate3d(${f}px, ${h}px, 0px)`),n.previousTranslate=n.translate,n.translate=n.isHorizontal()?f:h;const v=n.maxTranslate()-n.minTranslate();d=0===v?0:(t-n.minTranslate())/v,d!==progress&&n.updateProgress(t),n.emit("setTranslate",n.translate,e)},minTranslate:function(){return-this.snapGrid[0]},maxTranslate:function(){return-this.snapGrid[this.snapGrid.length-1]},translateTo:function(t=0,e=this.params.speed,n=!0,r=!0,o){const l=this,{params:c,wrapperEl:d}=l;if(l.animating&&c.preventInteractionOnTransition)return!1;const f=l.minTranslate(),h=l.maxTranslate();let v;if(v=r&&t>f?f:r&&t<h?h:t,l.updateProgress(v),c.cssMode){const t=l.isHorizontal();return 0===e?d[t?"scrollLeft":"scrollTop"]=-v:d.scrollTo?d.scrollTo({[t?"left":"top"]:-v,behavior:"smooth"}):d[t?"scrollLeft":"scrollTop"]=-v,!0}return 0===e?(l.setTransition(0),l.setTranslate(v),n&&(l.emit("beforeTransitionStart",e,o),l.emit("transitionEnd"))):(l.setTransition(e),l.setTranslate(v),n&&(l.emit("beforeTransitionStart",e,o),l.emit("transitionStart")),l.animating||(l.animating=!0,l.onTranslateToWrapperTransitionEnd||(l.onTranslateToWrapperTransitionEnd=function(t){l&&!l.destroyed&&t.target===this&&(l.$wrapperEl[0].removeEventListener("transitionend",l.onTranslateToWrapperTransitionEnd),l.$wrapperEl[0].removeEventListener("webkitTransitionEnd",l.onTranslateToWrapperTransitionEnd),l.onTranslateToWrapperTransitionEnd=null,delete l.onTranslateToWrapperTransitionEnd,n&&l.emit("transitionEnd"))}),l.$wrapperEl[0].addEventListener("transitionend",l.onTranslateToWrapperTransitionEnd),l.$wrapperEl[0].addEventListener("webkitTransitionEnd",l.onTranslateToWrapperTransitionEnd))),!0}};var E={setTransition:function(t,e){const n=this;n.params.cssMode||n.$wrapperEl.transition(t),n.emit("setTransition",t,e)},transitionStart:function(t=!0,e){const n=this,{activeIndex:r,params:o,previousIndex:l}=n;if(o.cssMode)return;o.autoHeight&&n.updateAutoHeight();let c=e;if(c||(c=r>l?"next":r<l?"prev":"reset"),n.emit("transitionStart"),t&&r!==l){if("reset"===c)return void n.emit("slideResetTransitionStart");n.emit("slideChangeTransitionStart"),"next"===c?n.emit("slideNextTransitionStart"):n.emit("slidePrevTransitionStart")}},transitionEnd:function(t=!0,e){const n=this,{activeIndex:r,previousIndex:o,params:l}=n;if(n.animating=!1,l.cssMode)return;n.setTransition(0);let c=e;if(c||(c=r>o?"next":r<o?"prev":"reset"),n.emit("transitionEnd"),t&&r!==o){if("reset"===c)return void n.emit("slideResetTransitionEnd");n.emit("slideChangeTransitionEnd"),"next"===c?n.emit("slideNextTransitionEnd"):n.emit("slidePrevTransitionEnd")}}};var O={slideTo:function(t=0,e=this.params.speed,n=!0,r){const o=this;let l=t;l<0&&(l=0);const{params:c,snapGrid:d,slidesGrid:f,previousIndex:h,activeIndex:v,rtlTranslate:m,wrapperEl:y}=o;if(o.animating&&c.preventInteractionOnTransition)return!1;const _=Math.min(o.params.slidesPerGroupSkip,l);let w=_+Math.floor((l-_)/o.params.slidesPerGroup);w>=d.length&&(w=d.length-1),(v||c.initialSlide||0)===(h||0)&&n&&o.emit("beforeSlideChangeStart");const x=-d[w];if(o.updateProgress(x),c.normalizeSlideIndex)for(let i=0;i<f.length;i+=1)-Math.floor(100*x)>=Math.floor(100*f[i])&&(l=i);if(o.initialized&&l!==v){if(!o.allowSlideNext&&x<o.translate&&x<o.minTranslate())return!1;if(!o.allowSlidePrev&&x>o.translate&&x>o.maxTranslate()&&(v||0)!==l)return!1}let S;if(S=l>v?"next":l<v?"prev":"reset",m&&-x===o.translate||!m&&x===o.translate)return o.updateActiveIndex(l),c.autoHeight&&o.updateAutoHeight(),o.updateSlidesClasses(),"slide"!==c.effect&&o.setTranslate(x),"reset"!==S&&(o.transitionStart(n,S),o.transitionEnd(n,S)),!1;if(c.cssMode){const t=o.isHorizontal();let n=-x;return m&&(n=y.scrollWidth-y.offsetWidth-n),0===e?y[t?"scrollLeft":"scrollTop"]=n:y.scrollTo?y.scrollTo({[t?"left":"top"]:n,behavior:"smooth"}):y[t?"scrollLeft":"scrollTop"]=n,!0}return 0===e?(o.setTransition(0),o.setTranslate(x),o.updateActiveIndex(l),o.updateSlidesClasses(),o.emit("beforeTransitionStart",e,r),o.transitionStart(n,S),o.transitionEnd(n,S)):(o.setTransition(e),o.setTranslate(x),o.updateActiveIndex(l),o.updateSlidesClasses(),o.emit("beforeTransitionStart",e,r),o.transitionStart(n,S),o.animating||(o.animating=!0,o.onSlideToWrapperTransitionEnd||(o.onSlideToWrapperTransitionEnd=function(t){o&&!o.destroyed&&t.target===this&&(o.$wrapperEl[0].removeEventListener("transitionend",o.onSlideToWrapperTransitionEnd),o.$wrapperEl[0].removeEventListener("webkitTransitionEnd",o.onSlideToWrapperTransitionEnd),o.onSlideToWrapperTransitionEnd=null,delete o.onSlideToWrapperTransitionEnd,o.transitionEnd(n,S))}),o.$wrapperEl[0].addEventListener("transitionend",o.onSlideToWrapperTransitionEnd),o.$wrapperEl[0].addEventListener("webkitTransitionEnd",o.onSlideToWrapperTransitionEnd))),!0},slideToLoop:function(t=0,e=this.params.speed,n=!0,r){const o=this;let l=t;return o.params.loop&&(l+=o.loopedSlides),o.slideTo(l,e,n,r)},slideNext:function(t=this.params.speed,e=!0,n){const r=this,{params:o,animating:l}=r,c=r.activeIndex<o.slidesPerGroupSkip?1:o.slidesPerGroup;if(o.loop){if(l)return!1;r.loopFix(),r._clientLeft=r.$wrapperEl[0].clientLeft}return r.slideTo(r.activeIndex+c,t,e,n)},slidePrev:function(t=this.params.speed,e=!0,n){const r=this,{params:o,animating:l,snapGrid:c,slidesGrid:d,rtlTranslate:f}=r;if(o.loop){if(l)return!1;r.loopFix(),r._clientLeft=r.$wrapperEl[0].clientLeft}function h(t){return t<0?-Math.floor(Math.abs(t)):Math.floor(t)}const v=h(f?r.translate:-r.translate),m=c.map((t=>h(t)));d.map((t=>h(t))),c[m.indexOf(v)];let y,_=c[m.indexOf(v)-1];return void 0===_&&o.cssMode&&c.forEach((t=>{!_&&v>=t&&(_=t)})),void 0!==_&&(y=d.indexOf(_),y<0&&(y=r.activeIndex-1)),r.slideTo(y,t,e,n)},slideReset:function(t=this.params.speed,e=!0,n){return this.slideTo(this.activeIndex,t,e,n)},slideToClosest:function(t=this.params.speed,e=!0,n,r=.5){const o=this;let l=o.activeIndex;const c=Math.min(o.params.slidesPerGroupSkip,l),d=c+Math.floor((l-c)/o.params.slidesPerGroup),f=o.rtlTranslate?o.translate:-o.translate;if(f>=o.snapGrid[d]){const t=o.snapGrid[d];f-t>(o.snapGrid[d+1]-t)*r&&(l+=o.params.slidesPerGroup)}else{const t=o.snapGrid[d-1];f-t<=(o.snapGrid[d]-t)*r&&(l-=o.params.slidesPerGroup)}return l=Math.max(l,0),l=Math.min(l,o.slidesGrid.length-1),o.slideTo(l,t,e,n)},slideToClickedSlide:function(){const t=this,{params:e,$wrapperEl:n}=t,r="auto"===e.slidesPerView?t.slidesPerViewDynamic():e.slidesPerView;let o,l=t.clickedIndex;if(e.loop){if(t.animating)return;o=parseInt(h(t.clickedSlide).attr("data-swiper-slide-index"),10),e.centeredSlides?l<t.loopedSlides-r/2||l>t.slides.length-t.loopedSlides+r/2?(t.loopFix(),l=n.children(`.${e.slideClass}[data-swiper-slide-index="${o}"]:not(.${e.slideDuplicateClass})`).eq(0).index(),y.nextTick((()=>{t.slideTo(l)}))):t.slideTo(l):l>t.slides.length-r?(t.loopFix(),l=n.children(`.${e.slideClass}[data-swiper-slide-index="${o}"]:not(.${e.slideDuplicateClass})`).eq(0).index(),y.nextTick((()=>{t.slideTo(l)}))):t.slideTo(l)}else t.slideTo(l)}};var C={loopCreate:function(){const t=this,{params:e,$wrapperEl:n}=t;n.children(`.${e.slideClass}.${e.slideDuplicateClass}`).remove();let r=n.children(`.${e.slideClass}`);if(e.loopFillGroupWithBlank){const t=e.slidesPerGroup-r.length%e.slidesPerGroup;if(t!==e.slidesPerGroup){for(let i=0;i<t;i+=1){const t=h(l.createElement("div")).addClass(`${e.slideClass} ${e.slideBlankClass}`);n.append(t)}r=n.children(`.${e.slideClass}`)}}"auto"!==e.slidesPerView||e.loopedSlides||(e.loopedSlides=r.length),t.loopedSlides=Math.ceil(parseFloat(e.loopedSlides||e.slidesPerView,10)),t.loopedSlides+=e.loopAdditionalSlides,t.loopedSlides>r.length&&(t.loopedSlides=r.length);const o=[],c=[];r.each(((e,n)=>{const l=h(n);e<t.loopedSlides&&c.push(n),e<r.length&&e>=r.length-t.loopedSlides&&o.push(n),l.attr("data-swiper-slide-index",e)}));for(let i=0;i<c.length;i+=1)n.append(h(c[i].cloneNode(!0)).addClass(e.slideDuplicateClass));for(let i=o.length-1;i>=0;i-=1)n.prepend(h(o[i].cloneNode(!0)).addClass(e.slideDuplicateClass))},loopFix:function(){const t=this;t.emit("beforeLoopFix");const{activeIndex:e,slides:n,loopedSlides:r,allowSlidePrev:o,allowSlideNext:l,snapGrid:c,rtlTranslate:d}=t;let f;t.allowSlidePrev=!0,t.allowSlideNext=!0;const h=-c[e]-t.getTranslate();if(e<r){f=n.length-3*r+e,f+=r;t.slideTo(f,0,!1,!0)&&0!==h&&t.setTranslate((d?-t.translate:t.translate)-h)}else if(e>=n.length-r){f=-n.length+e+r,f+=r;t.slideTo(f,0,!1,!0)&&0!==h&&t.setTranslate((d?-t.translate:t.translate)-h)}t.allowSlidePrev=o,t.allowSlideNext=l,t.emit("loopFix")},loopDestroy:function(){const{$wrapperEl:t,params:e,slides:n}=this;t.children(`.${e.slideClass}.${e.slideDuplicateClass},.${e.slideClass}.${e.slideBlankClass}`).remove(),n.removeAttr("data-swiper-slide-index")}};var T={setGrabCursor:function(t){const e=this;if(_.touch||!e.params.simulateTouch||e.params.watchOverflow&&e.isLocked||e.params.cssMode)return;const n=e.el;n.style.cursor="move",n.style.cursor=t?"-webkit-grabbing":"-webkit-grab",n.style.cursor=t?"-moz-grabbin":"-moz-grab",n.style.cursor=t?"grabbing":"grab"},unsetGrabCursor:function(){const t=this;_.touch||t.params.watchOverflow&&t.isLocked||t.params.cssMode||(t.el.style.cursor="")}};var k={appendSlide:function(t){const e=this,{$wrapperEl:n,params:r}=e;if(r.loop&&e.loopDestroy(),"object"==typeof t&&"length"in t)for(let i=0;i<t.length;i+=1)t[i]&&n.append(t[i]);else n.append(t);r.loop&&e.loopCreate(),r.observer&&_.observer||e.update()},prependSlide:function(t){const e=this,{params:n,$wrapperEl:r,activeIndex:o}=e;n.loop&&e.loopDestroy();let l=o+1;if("object"==typeof t&&"length"in t){for(let i=0;i<t.length;i+=1)t[i]&&r.prepend(t[i]);l=o+t.length}else r.prepend(t);n.loop&&e.loopCreate(),n.observer&&_.observer||e.update(),e.slideTo(l,0,!1)},addSlide:function(t,e){const n=this,{$wrapperEl:r,params:o,activeIndex:l}=n;let c=l;o.loop&&(c-=n.loopedSlides,n.loopDestroy(),n.slides=r.children(`.${o.slideClass}`));const d=n.slides.length;if(t<=0)return void n.prependSlide(e);if(t>=d)return void n.appendSlide(e);let f=c>t?c+1:c;const h=[];for(let i=d-1;i>=t;i-=1){const t=n.slides.eq(i);t.remove(),h.unshift(t)}if("object"==typeof e&&"length"in e){for(let i=0;i<e.length;i+=1)e[i]&&r.append(e[i]);f=c>t?c+e.length:c}else r.append(e);for(let i=0;i<h.length;i+=1)r.append(h[i]);o.loop&&n.loopCreate(),o.observer&&_.observer||n.update(),o.loop?n.slideTo(f+n.loopedSlides,0,!1):n.slideTo(f,0,!1)},removeSlide:function(t){const e=this,{params:n,$wrapperEl:r,activeIndex:o}=e;let l=o;n.loop&&(l-=e.loopedSlides,e.loopDestroy(),e.slides=r.children(`.${n.slideClass}`));let c,d=l;if("object"==typeof t&&"length"in t){for(let i=0;i<t.length;i+=1)c=t[i],e.slides[c]&&e.slides.eq(c).remove(),c<d&&(d-=1);d=Math.max(d,0)}else c=t,e.slides[c]&&e.slides.eq(c).remove(),c<d&&(d-=1),d=Math.max(d,0);n.loop&&e.loopCreate(),n.observer&&_.observer||e.update(),n.loop?e.slideTo(d+e.loopedSlides,0,!1):e.slideTo(d,0,!1)},removeAllSlides:function(){const t=this,e=[];for(let i=0;i<t.slides.length;i+=1)e.push(i);t.removeSlide(e)}};const j=function(){const t=d.navigator.platform,e=d.navigator.userAgent,n={ios:!1,android:!1,androidChrome:!1,desktop:!1,iphone:!1,ipod:!1,ipad:!1,edge:!1,ie:!1,firefox:!1,macos:!1,windows:!1,cordova:!(!d.cordova&&!d.phonegap),phonegap:!(!d.cordova&&!d.phonegap),electron:!1},r=d.screen.width,o=d.screen.height,l=e.match(/(Android);?[\s\/]+([\d.]+)?/);let c=e.match(/(iPad).*OS\s([\d_]+)/);const f=e.match(/(iPod)(.*OS\s([\d_]+))?/),h=!c&&e.match(/(iPhone\sOS|iOS)\s([\d_]+)/),v=e.indexOf("MSIE ")>=0||e.indexOf("Trident/")>=0,m=e.indexOf("Edge/")>=0,y=e.indexOf("Gecko/")>=0&&e.indexOf("Firefox/")>=0,w="Win32"===t,x=e.toLowerCase().indexOf("electron")>=0;let S="MacIntel"===t;return!c&&S&&_.touch&&(1024===r&&1366===o||834===r&&1194===o||834===r&&1112===o||768===r&&1024===o)&&(c=e.match(/(Version)\/([\d.]+)/),S=!1),n.ie=v,n.edge=m,n.firefox=y,l&&!w&&(n.os="android",n.osVersion=l[2],n.android=!0,n.androidChrome=e.toLowerCase().indexOf("chrome")>=0),(c||h||f)&&(n.os="ios",n.ios=!0),h&&!f&&(n.osVersion=h[2].replace(/_/g,"."),n.iphone=!0),c&&(n.osVersion=c[2].replace(/_/g,"."),n.ipad=!0),f&&(n.osVersion=f[3]?f[3].replace(/_/g,"."):null,n.ipod=!0),n.ios&&n.osVersion&&e.indexOf("Version/")>=0&&"10"===n.osVersion.split(".")[0]&&(n.osVersion=e.toLowerCase().split("version/")[1].split(" ")[0]),n.webView=!(!(h||c||f)||!e.match(/.*AppleWebKit(?!.*Safari)/i)&&!d.navigator.standalone)||d.matchMedia&&d.matchMedia("(display-mode: standalone)").matches,n.webview=n.webView,n.standalone=n.webView,n.desktop=!(n.ios||n.android)||x,n.desktop&&(n.electron=x,n.macos=S,n.windows=w,n.macos&&(n.os="macos"),n.windows&&(n.os="windows")),n.pixelRatio=d.devicePixelRatio||1,n}();function $(t){const e=this,data=e.touchEventsData,{params:n,touches:r}=e;if(e.animating&&n.preventInteractionOnTransition)return;let o=t;o.originalEvent&&(o=o.originalEvent);const c=h(o.target);if("wrapper"===n.touchEventsTarget&&!c.closest(e.wrapperEl).length)return;if(data.isTouchEvent="touchstart"===o.type,!data.isTouchEvent&&"which"in o&&3===o.which)return;if(!data.isTouchEvent&&"button"in o&&o.button>0)return;if(data.isTouched&&data.isMoved)return;if(n.noSwiping&&c.closest(n.noSwipingSelector?n.noSwipingSelector:`.${n.noSwipingClass}`)[0])return void(e.allowClick=!0);if(n.swipeHandler&&!c.closest(n.swipeHandler)[0])return;r.currentX="touchstart"===o.type?o.targetTouches[0].pageX:o.pageX,r.currentY="touchstart"===o.type?o.targetTouches[0].pageY:o.pageY;const f=r.currentX,v=r.currentY,m=n.edgeSwipeDetection||n.iOSEdgeSwipeDetection,_=n.edgeSwipeThreshold||n.iOSEdgeSwipeThreshold;if(!m||!(f<=_||f>=d.screen.width-_)){if(y.extend(data,{isTouched:!0,isMoved:!1,allowTouchCallbacks:!0,isScrolling:void 0,startMoving:void 0}),r.startX=f,r.startY=v,data.touchStartTime=y.now(),e.allowClick=!0,e.updateSize(),e.swipeDirection=void 0,n.threshold>0&&(data.allowThresholdMove=!1),"touchstart"!==o.type){let t=!0;c.is(data.formElements)&&(t=!1),l.activeElement&&h(l.activeElement).is(data.formElements)&&l.activeElement!==c[0]&&l.activeElement.blur();const r=t&&e.allowTouchMove&&n.touchStartPreventDefault;(n.touchStartForcePreventDefault||r)&&o.preventDefault()}e.emit("touchStart",o)}}function M(t){const e=this,data=e.touchEventsData,{params:n,touches:r,rtlTranslate:o}=e;let c=t;if(c.originalEvent&&(c=c.originalEvent),!data.isTouched)return void(data.startMoving&&data.isScrolling&&e.emit("touchMoveOpposite",c));if(data.isTouchEvent&&"touchmove"!==c.type)return;const d="touchmove"===c.type&&c.targetTouches&&(c.targetTouches[0]||c.changedTouches[0]),f="touchmove"===c.type?d.pageX:c.pageX,v="touchmove"===c.type?d.pageY:c.pageY;if(c.preventedByNestedSwiper)return r.startX=f,void(r.startY=v);if(!e.allowTouchMove)return e.allowClick=!1,void(data.isTouched&&(y.extend(r,{startX:f,startY:v,currentX:f,currentY:v}),data.touchStartTime=y.now()));if(data.isTouchEvent&&n.touchReleaseOnEdges&&!n.loop)if(e.isVertical()){if(v<r.startY&&e.translate<=e.maxTranslate()||v>r.startY&&e.translate>=e.minTranslate())return data.isTouched=!1,void(data.isMoved=!1)}else if(f<r.startX&&e.translate<=e.maxTranslate()||f>r.startX&&e.translate>=e.minTranslate())return;if(data.isTouchEvent&&l.activeElement&&c.target===l.activeElement&&h(c.target).is(data.formElements))return data.isMoved=!0,void(e.allowClick=!1);if(data.allowTouchCallbacks&&e.emit("touchMove",c),c.targetTouches&&c.targetTouches.length>1)return;r.currentX=f,r.currentY=v;const m=r.currentX-r.startX,_=r.currentY-r.startY;if(e.params.threshold&&Math.sqrt(m**2+_**2)<e.params.threshold)return;if(void 0===data.isScrolling){let t;e.isHorizontal()&&r.currentY===r.startY||e.isVertical()&&r.currentX===r.startX?data.isScrolling=!1:m*m+_*_>=25&&(t=180*Math.atan2(Math.abs(_),Math.abs(m))/Math.PI,data.isScrolling=e.isHorizontal()?t>n.touchAngle:90-t>n.touchAngle)}if(data.isScrolling&&e.emit("touchMoveOpposite",c),void 0===data.startMoving&&(r.currentX===r.startX&&r.currentY===r.startY||(data.startMoving=!0)),data.isScrolling)return void(data.isTouched=!1);if(!data.startMoving)return;e.allowClick=!1,!n.cssMode&&c.cancelable&&c.preventDefault(),n.touchMoveStopPropagation&&!n.nested&&c.stopPropagation(),data.isMoved||(n.loop&&e.loopFix(),data.startTranslate=e.getTranslate(),e.setTransition(0),e.animating&&e.$wrapperEl.trigger("webkitTransitionEnd transitionend"),data.allowMomentumBounce=!1,!n.grabCursor||!0!==e.allowSlideNext&&!0!==e.allowSlidePrev||e.setGrabCursor(!0),e.emit("sliderFirstMove",c)),e.emit("sliderMove",c),data.isMoved=!0;let w=e.isHorizontal()?m:_;r.diff=w,w*=n.touchRatio,o&&(w=-w),e.swipeDirection=w>0?"prev":"next",data.currentTranslate=w+data.startTranslate;let x=!0,S=n.resistanceRatio;if(n.touchReleaseOnEdges&&(S=0),w>0&&data.currentTranslate>e.minTranslate()?(x=!1,n.resistance&&(data.currentTranslate=e.minTranslate()-1+(-e.minTranslate()+data.startTranslate+w)**S)):w<0&&data.currentTranslate<e.maxTranslate()&&(x=!1,n.resistance&&(data.currentTranslate=e.maxTranslate()+1-(e.maxTranslate()-data.startTranslate-w)**S)),x&&(c.preventedByNestedSwiper=!0),!e.allowSlideNext&&"next"===e.swipeDirection&&data.currentTranslate<data.startTranslate&&(data.currentTranslate=data.startTranslate),!e.allowSlidePrev&&"prev"===e.swipeDirection&&data.currentTranslate>data.startTranslate&&(data.currentTranslate=data.startTranslate),n.threshold>0){if(!(Math.abs(w)>n.threshold||data.allowThresholdMove))return void(data.currentTranslate=data.startTranslate);if(!data.allowThresholdMove)return data.allowThresholdMove=!0,r.startX=r.currentX,r.startY=r.currentY,data.currentTranslate=data.startTranslate,void(r.diff=e.isHorizontal()?r.currentX-r.startX:r.currentY-r.startY)}n.followFinger&&!n.cssMode&&((n.freeMode||n.watchSlidesProgress||n.watchSlidesVisibility)&&(e.updateActiveIndex(),e.updateSlidesClasses()),n.freeMode&&(0===data.velocities.length&&data.velocities.push({position:r[e.isHorizontal()?"startX":"startY"],time:data.touchStartTime}),data.velocities.push({position:r[e.isHorizontal()?"currentX":"currentY"],time:y.now()})),e.updateProgress(data.currentTranslate),e.setTranslate(data.currentTranslate))}function A(t){const e=this,data=e.touchEventsData,{params:n,touches:r,rtlTranslate:o,$wrapperEl:l,slidesGrid:c,snapGrid:d}=e;let f=t;if(f.originalEvent&&(f=f.originalEvent),data.allowTouchCallbacks&&e.emit("touchEnd",f),data.allowTouchCallbacks=!1,!data.isTouched)return data.isMoved&&n.grabCursor&&e.setGrabCursor(!1),data.isMoved=!1,void(data.startMoving=!1);n.grabCursor&&data.isMoved&&data.isTouched&&(!0===e.allowSlideNext||!0===e.allowSlidePrev)&&e.setGrabCursor(!1);const h=y.now(),v=h-data.touchStartTime;if(e.allowClick&&(e.updateClickedSlide(f),e.emit("tap click",f),v<300&&h-data.lastClickTime<300&&e.emit("doubleTap doubleClick",f)),data.lastClickTime=y.now(),y.nextTick((()=>{e.destroyed||(e.allowClick=!0)})),!data.isTouched||!data.isMoved||!e.swipeDirection||0===r.diff||data.currentTranslate===data.startTranslate)return data.isTouched=!1,data.isMoved=!1,void(data.startMoving=!1);let m;if(data.isTouched=!1,data.isMoved=!1,data.startMoving=!1,m=n.followFinger?o?e.translate:-e.translate:-data.currentTranslate,n.cssMode)return;if(n.freeMode){if(m<-e.minTranslate())return void e.slideTo(e.activeIndex);if(m>-e.maxTranslate())return void(e.slides.length<d.length?e.slideTo(d.length-1):e.slideTo(e.slides.length-1));if(n.freeModeMomentum){if(data.velocities.length>1){const t=data.velocities.pop(),r=data.velocities.pop(),o=t.position-r.position,time=t.time-r.time;e.velocity=o/time,e.velocity/=2,Math.abs(e.velocity)<n.freeModeMinimumVelocity&&(e.velocity=0),(time>150||y.now()-t.time>300)&&(e.velocity=0)}else e.velocity=0;e.velocity*=n.freeModeMomentumVelocityRatio,data.velocities.length=0;let t=1e3*n.freeModeMomentumRatio;const r=e.velocity*t;let c=e.translate+r;o&&(c=-c);let f,h=!1;const v=20*Math.abs(e.velocity)*n.freeModeMomentumBounceRatio;let m;if(c<e.maxTranslate())n.freeModeMomentumBounce?(c+e.maxTranslate()<-v&&(c=e.maxTranslate()-v),f=e.maxTranslate(),h=!0,data.allowMomentumBounce=!0):c=e.maxTranslate(),n.loop&&n.centeredSlides&&(m=!0);else if(c>e.minTranslate())n.freeModeMomentumBounce?(c-e.minTranslate()>v&&(c=e.minTranslate()+v),f=e.minTranslate(),h=!0,data.allowMomentumBounce=!0):c=e.minTranslate(),n.loop&&n.centeredSlides&&(m=!0);else if(n.freeModeSticky){let t;for(let e=0;e<d.length;e+=1)if(d[e]>-c){t=e;break}c=Math.abs(d[t]-c)<Math.abs(d[t-1]-c)||"next"===e.swipeDirection?d[t]:d[t-1],c=-c}if(m&&e.once("transitionEnd",(()=>{e.loopFix()})),0!==e.velocity){if(t=o?Math.abs((-c-e.translate)/e.velocity):Math.abs((c-e.translate)/e.velocity),n.freeModeSticky){const r=Math.abs((o?-c:c)-e.translate),l=e.slidesSizesGrid[e.activeIndex];t=r<l?n.speed:r<2*l?1.5*n.speed:2.5*n.speed}}else if(n.freeModeSticky)return void e.slideToClosest();n.freeModeMomentumBounce&&h?(e.updateProgress(f),e.setTransition(t),e.setTranslate(c),e.transitionStart(!0,e.swipeDirection),e.animating=!0,l.transitionEnd((()=>{e&&!e.destroyed&&data.allowMomentumBounce&&(e.emit("momentumBounce"),e.setTransition(n.speed),setTimeout((()=>{e.setTranslate(f),l.transitionEnd((()=>{e&&!e.destroyed&&e.transitionEnd()}))}),0))}))):e.velocity?(e.updateProgress(c),e.setTransition(t),e.setTranslate(c),e.transitionStart(!0,e.swipeDirection),e.animating||(e.animating=!0,l.transitionEnd((()=>{e&&!e.destroyed&&e.transitionEnd()})))):e.updateProgress(c),e.updateActiveIndex(),e.updateSlidesClasses()}else if(n.freeModeSticky)return void e.slideToClosest();return void((!n.freeModeMomentum||v>=n.longSwipesMs)&&(e.updateProgress(),e.updateActiveIndex(),e.updateSlidesClasses()))}let _=0,w=e.slidesSizesGrid[0];for(let i=0;i<c.length;i+=i<n.slidesPerGroupSkip?1:n.slidesPerGroup){const t=i<n.slidesPerGroupSkip-1?1:n.slidesPerGroup;void 0!==c[i+t]?m>=c[i]&&m<c[i+t]&&(_=i,w=c[i+t]-c[i]):m>=c[i]&&(_=i,w=c[c.length-1]-c[c.length-2])}const x=(m-c[_])/w,S=_<n.slidesPerGroupSkip-1?1:n.slidesPerGroup;if(v>n.longSwipesMs){if(!n.longSwipes)return void e.slideTo(e.activeIndex);"next"===e.swipeDirection&&(x>=n.longSwipesRatio?e.slideTo(_+S):e.slideTo(_)),"prev"===e.swipeDirection&&(x>1-n.longSwipesRatio?e.slideTo(_+S):e.slideTo(_))}else{if(!n.shortSwipes)return void e.slideTo(e.activeIndex);e.navigation&&(f.target===e.navigation.nextEl||f.target===e.navigation.prevEl)?f.target===e.navigation.nextEl?e.slideTo(_+S):e.slideTo(_):("next"===e.swipeDirection&&e.slideTo(_+S),"prev"===e.swipeDirection&&e.slideTo(_))}}function I(){const t=this,{params:e,el:n}=t;if(n&&0===n.offsetWidth)return;e.breakpoints&&t.setBreakpoint();const{allowSlideNext:r,allowSlidePrev:o,snapGrid:l}=t;t.allowSlideNext=!0,t.allowSlidePrev=!0,t.updateSize(),t.updateSlides(),t.updateSlidesClasses(),("auto"===e.slidesPerView||e.slidesPerView>1)&&t.isEnd&&!t.isBeginning&&!t.params.centeredSlides?t.slideTo(t.slides.length-1,0,!1,!0):t.slideTo(t.activeIndex,0,!1,!0),t.autoplay&&t.autoplay.running&&t.autoplay.paused&&t.autoplay.run(),t.allowSlidePrev=o,t.allowSlideNext=r,t.params.watchOverflow&&l!==t.snapGrid&&t.checkOverflow()}function P(t){const e=this;e.allowClick||(e.params.preventClicks&&t.preventDefault(),e.params.preventClicksPropagation&&e.animating&&(t.stopPropagation(),t.stopImmediatePropagation()))}function D(){const t=this,{wrapperEl:e,rtlTranslate:n}=t;let r;t.previousTranslate=t.translate,t.isHorizontal()?t.translate=n?e.scrollWidth-e.offsetWidth-e.scrollLeft:-e.scrollLeft:t.translate=-e.scrollTop,-0===t.translate&&(t.translate=0),t.updateActiveIndex(),t.updateSlidesClasses();const o=t.maxTranslate()-t.minTranslate();r=0===o?0:(t.translate-t.minTranslate())/o,r!==t.progress&&t.updateProgress(n?-t.translate:t.translate),t.emit("setTranslate",t.translate,!1)}let L=!1;function z(){}var N={init:!0,direction:"horizontal",touchEventsTarget:"container",initialSlide:0,speed:300,cssMode:!1,updateOnWindowResize:!0,preventInteractionOnTransition:!1,edgeSwipeDetection:!1,edgeSwipeThreshold:20,freeMode:!1,freeModeMomentum:!0,freeModeMomentumRatio:1,freeModeMomentumBounce:!0,freeModeMomentumBounceRatio:1,freeModeMomentumVelocityRatio:1,freeModeSticky:!1,freeModeMinimumVelocity:.02,autoHeight:!1,setWrapperSize:!1,virtualTranslate:!1,effect:"slide",breakpoints:void 0,spaceBetween:0,slidesPerView:1,slidesPerColumn:1,slidesPerColumnFill:"column",slidesPerGroup:1,slidesPerGroupSkip:0,centeredSlides:!1,centeredSlidesBounds:!1,slidesOffsetBefore:0,slidesOffsetAfter:0,normalizeSlideIndex:!0,centerInsufficientSlides:!1,watchOverflow:!1,roundLengths:!1,touchRatio:1,touchAngle:45,simulateTouch:!0,shortSwipes:!0,longSwipes:!0,longSwipesRatio:.5,longSwipesMs:300,followFinger:!0,allowTouchMove:!0,threshold:0,touchMoveStopPropagation:!1,touchStartPreventDefault:!0,touchStartForcePreventDefault:!1,touchReleaseOnEdges:!1,uniqueNavElements:!0,resistance:!0,resistanceRatio:.85,watchSlidesProgress:!1,watchSlidesVisibility:!1,grabCursor:!1,preventClicks:!0,preventClicksPropagation:!0,slideToClickedSlide:!1,preloadImages:!0,updateOnImagesReady:!0,loop:!1,loopAdditionalSlides:0,loopedSlides:null,loopFillGroupWithBlank:!1,allowSlidePrev:!0,allowSlideNext:!0,swipeHandler:null,noSwiping:!0,noSwipingClass:"swiper-no-swiping",noSwipingSelector:null,passiveListeners:!0,containerModifierClass:"swiper-container-",slideClass:"swiper-slide",slideBlankClass:"swiper-slide-invisible-blank",slideActiveClass:"swiper-slide-active",slideDuplicateActiveClass:"swiper-slide-duplicate-active",slideVisibleClass:"swiper-slide-visible",slideDuplicateClass:"swiper-slide-duplicate",slideNextClass:"swiper-slide-next",slideDuplicateNextClass:"swiper-slide-duplicate-next",slidePrevClass:"swiper-slide-prev",slideDuplicatePrevClass:"swiper-slide-duplicate-prev",wrapperClass:"swiper-wrapper",runCallbacksOnInit:!0};const B={update:x,translate:S,transition:E,slide:O,loop:C,grabCursor:T,manipulation:k,events:{attachEvents:function(){const t=this,{params:e,touchEvents:n,el:r,wrapperEl:o}=t;t.onTouchStart=$.bind(t),t.onTouchMove=M.bind(t),t.onTouchEnd=A.bind(t),e.cssMode&&(t.onScroll=D.bind(t)),t.onClick=P.bind(t);const c=!!e.nested;if(!_.touch&&_.pointerEvents)r.addEventListener(n.start,t.onTouchStart,!1),l.addEventListener(n.move,t.onTouchMove,c),l.addEventListener(n.end,t.onTouchEnd,!1);else{if(_.touch){const o=!("touchstart"!==n.start||!_.passiveListener||!e.passiveListeners)&&{passive:!0,capture:!1};r.addEventListener(n.start,t.onTouchStart,o),r.addEventListener(n.move,t.onTouchMove,_.passiveListener?{passive:!1,capture:c}:c),r.addEventListener(n.end,t.onTouchEnd,o),n.cancel&&r.addEventListener(n.cancel,t.onTouchEnd,o),L||(l.addEventListener("touchstart",z),L=!0)}(e.simulateTouch&&!j.ios&&!j.android||e.simulateTouch&&!_.touch&&j.ios)&&(r.addEventListener("mousedown",t.onTouchStart,!1),l.addEventListener("mousemove",t.onTouchMove,c),l.addEventListener("mouseup",t.onTouchEnd,!1))}(e.preventClicks||e.preventClicksPropagation)&&r.addEventListener("click",t.onClick,!0),e.cssMode&&o.addEventListener("scroll",t.onScroll),e.updateOnWindowResize?t.on(j.ios||j.android?"resize orientationchange observerUpdate":"resize observerUpdate",I,!0):t.on("observerUpdate",I,!0)},detachEvents:function(){const t=this,{params:e,touchEvents:n,el:r,wrapperEl:o}=t,c=!!e.nested;if(!_.touch&&_.pointerEvents)r.removeEventListener(n.start,t.onTouchStart,!1),l.removeEventListener(n.move,t.onTouchMove,c),l.removeEventListener(n.end,t.onTouchEnd,!1);else{if(_.touch){const o=!("onTouchStart"!==n.start||!_.passiveListener||!e.passiveListeners)&&{passive:!0,capture:!1};r.removeEventListener(n.start,t.onTouchStart,o),r.removeEventListener(n.move,t.onTouchMove,c),r.removeEventListener(n.end,t.onTouchEnd,o),n.cancel&&r.removeEventListener(n.cancel,t.onTouchEnd,o)}(e.simulateTouch&&!j.ios&&!j.android||e.simulateTouch&&!_.touch&&j.ios)&&(r.removeEventListener("mousedown",t.onTouchStart,!1),l.removeEventListener("mousemove",t.onTouchMove,c),l.removeEventListener("mouseup",t.onTouchEnd,!1))}(e.preventClicks||e.preventClicksPropagation)&&r.removeEventListener("click",t.onClick,!0),e.cssMode&&o.removeEventListener("scroll",t.onScroll),t.off(j.ios||j.android?"resize orientationchange observerUpdate":"resize observerUpdate",I)}},breakpoints:{setBreakpoint:function(){const t=this,{activeIndex:e,initialized:n,loopedSlides:r=0,params:o,$el:l}=t,c=o.breakpoints;if(!c||c&&0===Object.keys(c).length)return;const d=t.getBreakpoint(c);if(d&&t.currentBreakpoint!==d){const f=d in c?c[d]:void 0;f&&["slidesPerView","spaceBetween","slidesPerGroup","slidesPerGroupSkip","slidesPerColumn"].forEach((param=>{const t=f[param];void 0!==t&&(f[param]="slidesPerView"!==param||"AUTO"!==t&&"auto"!==t?"slidesPerView"===param?parseFloat(t):parseInt(t,10):"auto")}));const h=f||t.originalParams,v=o.slidesPerColumn>1,m=h.slidesPerColumn>1;v&&!m?l.removeClass(`${o.containerModifierClass}multirow ${o.containerModifierClass}multirow-column`):!v&&m&&(l.addClass(`${o.containerModifierClass}multirow`),"column"===h.slidesPerColumnFill&&l.addClass(`${o.containerModifierClass}multirow-column`));const _=h.direction&&h.direction!==o.direction,w=o.loop&&(h.slidesPerView!==o.slidesPerView||_);_&&n&&t.changeDirection(),y.extend(t.params,h),y.extend(t,{allowTouchMove:t.params.allowTouchMove,allowSlideNext:t.params.allowSlideNext,allowSlidePrev:t.params.allowSlidePrev}),t.currentBreakpoint=d,w&&n&&(t.loopDestroy(),t.loopCreate(),t.updateSlides(),t.slideTo(e-r+t.loopedSlides,0,!1)),t.emit("breakpoint",h)}},getBreakpoint:function(t){if(!t)return;let e=!1;const n=Object.keys(t).map((t=>{if("string"==typeof t&&0===t.indexOf("@")){const e=parseFloat(t.substr(1));return{value:d.innerHeight*e,point:t}}return{value:t,point:t}}));n.sort(((a,b)=>parseInt(a.value,10)-parseInt(b.value,10)));for(let i=0;i<n.length;i+=1){const{point:t,value:r}=n[i];r<=d.innerWidth&&(e=t)}return e||"max"}},checkOverflow:{checkOverflow:function(){const t=this,e=t.params,n=t.isLocked,r=t.slides.length>0&&e.slidesOffsetBefore+e.spaceBetween*(t.slides.length-1)+t.slides[0].offsetWidth*t.slides.length;e.slidesOffsetBefore&&e.slidesOffsetAfter&&r?t.isLocked=r<=t.size:t.isLocked=1===t.snapGrid.length,t.allowSlideNext=!t.isLocked,t.allowSlidePrev=!t.isLocked,n!==t.isLocked&&t.emit(t.isLocked?"lock":"unlock"),n&&n!==t.isLocked&&(t.isEnd=!1,t.navigation&&t.navigation.update())}},classes:{addClasses:function(){const{classNames:t,params:e,rtl:n,$el:r}=this,o=[];o.push("initialized"),o.push(e.direction),e.freeMode&&o.push("free-mode"),e.autoHeight&&o.push("autoheight"),n&&o.push("rtl"),e.slidesPerColumn>1&&(o.push("multirow"),"column"===e.slidesPerColumnFill&&o.push("multirow-column")),j.android&&o.push("android"),j.ios&&o.push("ios"),e.cssMode&&o.push("css-mode"),o.forEach((n=>{t.push(e.containerModifierClass+n)})),r.addClass(t.join(" "))},removeClasses:function(){const{$el:t,classNames:e}=this;t.removeClass(e.join(" "))}},images:{loadImage:function(t,e,n,r,o,l){let image;function c(){l&&l()}h(t).parent("picture")[0]||t.complete&&o?c():e?(image=new d.Image,image.onload=c,image.onerror=c,r&&(image.sizes=r),n&&(image.srcset=n),e&&(image.src=e)):c()},preloadImages:function(){const t=this;function e(){null!=t&&t&&!t.destroyed&&(void 0!==t.imagesLoaded&&(t.imagesLoaded+=1),t.imagesLoaded===t.imagesToLoad.length&&(t.params.updateOnImagesReady&&t.update(),t.emit("imagesReady")))}t.imagesToLoad=t.$el.find("img");for(let i=0;i<t.imagesToLoad.length;i+=1){const n=t.imagesToLoad[i];t.loadImage(n,n.currentSrc||n.getAttribute("src"),n.srcset||n.getAttribute("srcset"),n.sizes||n.getAttribute("sizes"),!0,e)}}}},R={};class F extends w{constructor(...t){let e,n;1===t.length&&t[0].constructor&&t[0].constructor===Object?n=t[0]:[e,n]=t,n||(n={}),n=y.extend({},n),e&&!n.el&&(n.el=e),super(n),Object.keys(B).forEach((t=>{Object.keys(B[t]).forEach((e=>{F.prototype[e]||(F.prototype[e]=B[t][e])}))}));const r=this;void 0===r.modules&&(r.modules={}),Object.keys(r.modules).forEach((t=>{const e=r.modules[t];if(e.params){const t=Object.keys(e.params)[0],r=e.params[t];if("object"!=typeof r||null===r)return;if(!(t in n)||!("enabled"in r))return;!0===n[t]&&(n[t]={enabled:!0}),"object"!=typeof n[t]||"enabled"in n[t]||(n[t].enabled=!0),n[t]||(n[t]={enabled:!1})}}));const o=y.extend({},N);r.useModulesParams(o),r.params=y.extend({},o,R,n),r.originalParams=y.extend({},r.params),r.passedParams=y.extend({},n),r.$=h;const l=h(r.params.el);if(e=l[0],!e)return;if(l.length>1){const t=[];return l.each(((e,r)=>{const o=y.extend({},n,{el:r});t.push(new F(o))})),t}let c;return e.swiper=r,l.data("swiper",r),e&&e.shadowRoot&&e.shadowRoot.querySelector?(c=h(e.shadowRoot.querySelector(`.${r.params.wrapperClass}`)),c.children=t=>l.children(t)):c=l.children(`.${r.params.wrapperClass}`),y.extend(r,{$el:l,el:e,$wrapperEl:c,wrapperEl:c[0],classNames:[],slides:h(),slidesGrid:[],snapGrid:[],slidesSizesGrid:[],isHorizontal:()=>"horizontal"===r.params.direction,isVertical:()=>"vertical"===r.params.direction,rtl:"rtl"===e.dir.toLowerCase()||"rtl"===l.css("direction"),rtlTranslate:"horizontal"===r.params.direction&&("rtl"===e.dir.toLowerCase()||"rtl"===l.css("direction")),wrongRTL:"-webkit-box"===c.css("display"),activeIndex:0,realIndex:0,isBeginning:!0,isEnd:!1,translate:0,previousTranslate:0,progress:0,velocity:0,animating:!1,allowSlideNext:r.params.allowSlideNext,allowSlidePrev:r.params.allowSlidePrev,touchEvents:function(){const t=["touchstart","touchmove","touchend","touchcancel"];let e=["mousedown","mousemove","mouseup"];return _.pointerEvents&&(e=["pointerdown","pointermove","pointerup"]),r.touchEventsTouch={start:t[0],move:t[1],end:t[2],cancel:t[3]},r.touchEventsDesktop={start:e[0],move:e[1],end:e[2]},_.touch||!r.params.simulateTouch?r.touchEventsTouch:r.touchEventsDesktop}(),touchEventsData:{isTouched:void 0,isMoved:void 0,allowTouchCallbacks:void 0,touchStartTime:void 0,isScrolling:void 0,currentTranslate:void 0,startTranslate:void 0,allowThresholdMove:void 0,formElements:"input, select, option, textarea, button, video, label",lastClickTime:y.now(),clickTimeout:void 0,velocities:[],allowMomentumBounce:void 0,isTouchEvent:void 0,startMoving:void 0},allowClick:!0,allowTouchMove:r.params.allowTouchMove,touches:{startX:0,startY:0,currentX:0,currentY:0,diff:0},imagesToLoad:[],imagesLoaded:0}),r.useModules(),r.params.init&&r.init(),r}slidesPerViewDynamic(){const{params:t,slides:e,slidesGrid:n,size:r,activeIndex:o}=this;let l=1;if(t.centeredSlides){let t,n=e[o].swiperSlideSize;for(let i=o+1;i<e.length;i+=1)e[i]&&!t&&(n+=e[i].swiperSlideSize,l+=1,n>r&&(t=!0));for(let i=o-1;i>=0;i-=1)e[i]&&!t&&(n+=e[i].swiperSlideSize,l+=1,n>r&&(t=!0))}else for(let i=o+1;i<e.length;i+=1)n[i]-n[o]<r&&(l+=1);return l}update(){const t=this;if(!t||t.destroyed)return;const{snapGrid:e,params:n}=t;function r(){const e=t.rtlTranslate?-1*t.translate:t.translate,n=Math.min(Math.max(e,t.maxTranslate()),t.minTranslate());t.setTranslate(n),t.updateActiveIndex(),t.updateSlidesClasses()}let o;n.breakpoints&&t.setBreakpoint(),t.updateSize(),t.updateSlides(),t.updateProgress(),t.updateSlidesClasses(),t.params.freeMode?(r(),t.params.autoHeight&&t.updateAutoHeight()):(o=("auto"===t.params.slidesPerView||t.params.slidesPerView>1)&&t.isEnd&&!t.params.centeredSlides?t.slideTo(t.slides.length-1,0,!1,!0):t.slideTo(t.activeIndex,0,!1,!0),o||r()),n.watchOverflow&&e!==t.snapGrid&&t.checkOverflow(),t.emit("update")}changeDirection(t,e=!0){const n=this,r=n.params.direction;return t||(t="horizontal"===r?"vertical":"horizontal"),t===r||"horizontal"!==t&&"vertical"!==t||(n.$el.removeClass(`${n.params.containerModifierClass}${r}`).addClass(`${n.params.containerModifierClass}${t}`),n.params.direction=t,n.slides.each(((e,n)=>{"vertical"===t?n.style.width="":n.style.height=""})),n.emit("changeDirection"),e&&n.update()),n}init(){const t=this;t.initialized||(t.emit("beforeInit"),t.params.breakpoints&&t.setBreakpoint(),t.addClasses(),t.params.loop&&t.loopCreate(),t.updateSize(),t.updateSlides(),t.params.watchOverflow&&t.checkOverflow(),t.params.grabCursor&&t.setGrabCursor(),t.params.preloadImages&&t.preloadImages(),t.params.loop?t.slideTo(t.params.initialSlide+t.loopedSlides,0,t.params.runCallbacksOnInit):t.slideTo(t.params.initialSlide,0,t.params.runCallbacksOnInit),t.attachEvents(),t.initialized=!0,t.emit("init"))}destroy(t=!0,e=!0){const n=this,{params:r,$el:o,$wrapperEl:l,slides:c}=n;return void 0===n.params||n.destroyed||(n.emit("beforeDestroy"),n.initialized=!1,n.detachEvents(),r.loop&&n.loopDestroy(),e&&(n.removeClasses(),o.removeAttr("style"),l.removeAttr("style"),c&&c.length&&c.removeClass([r.slideVisibleClass,r.slideActiveClass,r.slideNextClass,r.slidePrevClass].join(" ")).removeAttr("style").removeAttr("data-swiper-slide-index")),n.emit("destroy"),Object.keys(n.eventsListeners).forEach((t=>{n.off(t)})),!1!==t&&(n.$el[0].swiper=null,n.$el.data("swiper",null),y.deleteProps(n)),n.destroyed=!0),null}static extendDefaults(t){y.extend(R,t)}static get extendedDefaults(){return R}static get defaults(){return N}static get Class(){return w}static get $(){return h}}var H={name:"device",proto:{device:j},static:{device:j}},U={name:"support",proto:{support:_},static:{support:_}};const W={isEdge:!!d.navigator.userAgent.match(/Edge/g),isSafari:function(){const t=d.navigator.userAgent.toLowerCase();return t.indexOf("safari")>=0&&t.indexOf("chrome")<0&&t.indexOf("android")<0}(),isWebView:/(iPhone|iPod|iPad).*AppleWebKit(?!.*Safari)/i.test(d.navigator.userAgent)};var V={name:"browser",proto:{browser:W},static:{browser:W}},Y={name:"resize",create(){const t=this;y.extend(t,{resize:{resizeHandler(){t&&!t.destroyed&&t.initialized&&(t.emit("beforeResize"),t.emit("resize"))},orientationChangeHandler(){t&&!t.destroyed&&t.initialized&&t.emit("orientationchange")}}})},on:{init(){d.addEventListener("resize",this.resize.resizeHandler),d.addEventListener("orientationchange",this.resize.orientationChangeHandler)},destroy(){d.removeEventListener("resize",this.resize.resizeHandler),d.removeEventListener("orientationchange",this.resize.orientationChangeHandler)}}};const X={func:d.MutationObserver||d.WebkitMutationObserver,attach(t,e={}){const n=this,r=new(0,X.func)((t=>{if(1===t.length)return void n.emit("observerUpdate",t[0]);const e=function(){n.emit("observerUpdate",t[0])};d.requestAnimationFrame?d.requestAnimationFrame(e):d.setTimeout(e,0)}));r.observe(t,{attributes:void 0===e.attributes||e.attributes,childList:void 0===e.childList||e.childList,characterData:void 0===e.characterData||e.characterData}),n.observer.observers.push(r)},init(){const t=this;if(_.observer&&t.params.observer){if(t.params.observeParents){const e=t.$el.parents();for(let i=0;i<e.length;i+=1)t.observer.attach(e[i])}t.observer.attach(t.$el[0],{childList:t.params.observeSlideChildren}),t.observer.attach(t.$wrapperEl[0],{attributes:!1})}},destroy(){this.observer.observers.forEach((t=>{t.disconnect()})),this.observer.observers=[]}};var G={name:"observer",params:{observer:!1,observeParents:!1,observeSlideChildren:!1},create(){const t=this;y.extend(t,{observer:{init:X.init.bind(t),attach:X.attach.bind(t),destroy:X.destroy.bind(t),observers:[]}})},on:{init(){this.observer.init()},destroy(){this.observer.destroy()}}};const J={update(t){const e=this,{slidesPerView:n,slidesPerGroup:r,centeredSlides:o}=e.params,{addSlidesBefore:l,addSlidesAfter:c}=e.params.virtual,{from:d,to:f,slides:h,slidesGrid:v,renderSlide:m,offset:_}=e.virtual;e.updateActiveIndex();const w=e.activeIndex||0;let x,S,E;x=e.rtlTranslate?"right":e.isHorizontal()?"left":"top",o?(S=Math.floor(n/2)+r+l,E=Math.floor(n/2)+r+c):(S=n+(r-1)+l,E=r+c);const O=Math.max((w||0)-E,0),C=Math.min((w||0)+S,h.length-1),T=(e.slidesGrid[O]||0)-(e.slidesGrid[0]||0);function k(){e.updateSlides(),e.updateProgress(),e.updateSlidesClasses(),e.lazy&&e.params.lazy.enabled&&e.lazy.load()}if(y.extend(e.virtual,{from:O,to:C,offset:T,slidesGrid:e.slidesGrid}),d===O&&f===C&&!t)return e.slidesGrid!==v&&T!==_&&e.slides.css(x,`${T}px`),void e.updateProgress();if(e.params.virtual.renderExternal)return e.params.virtual.renderExternal.call(e,{offset:T,from:O,to:C,slides:function(){const t=[];for(let i=O;i<=C;i+=1)t.push(h[i]);return t}()}),void k();const j=[],$=[];if(t)e.$wrapperEl.find(`.${e.params.slideClass}`).remove();else for(let i=d;i<=f;i+=1)(i<O||i>C)&&e.$wrapperEl.find(`.${e.params.slideClass}[data-swiper-slide-index="${i}"]`).remove();for(let i=0;i<h.length;i+=1)i>=O&&i<=C&&(void 0===f||t?$.push(i):(i>f&&$.push(i),i<d&&j.push(i)));$.forEach((t=>{e.$wrapperEl.append(m(h[t],t))})),j.sort(((a,b)=>b-a)).forEach((t=>{e.$wrapperEl.prepend(m(h[t],t))})),e.$wrapperEl.children(".swiper-slide").css(x,`${T}px`),k()},renderSlide(t,e){const n=this,r=n.params.virtual;if(r.cache&&n.virtual.cache[e])return n.virtual.cache[e];const o=r.renderSlide?h(r.renderSlide.call(n,t,e)):h(`<div class="${n.params.slideClass}" data-swiper-slide-index="${e}">${t}</div>`);return o.attr("data-swiper-slide-index")||o.attr("data-swiper-slide-index",e),r.cache&&(n.virtual.cache[e]=o),o},appendSlide(t){const e=this;if("object"==typeof t&&"length"in t)for(let i=0;i<t.length;i+=1)t[i]&&e.virtual.slides.push(t[i]);else e.virtual.slides.push(t);e.virtual.update(!0)},prependSlide(t){const e=this,n=e.activeIndex;let r=n+1,o=1;if(Array.isArray(t)){for(let i=0;i<t.length;i+=1)t[i]&&e.virtual.slides.unshift(t[i]);r=n+t.length,o=t.length}else e.virtual.slides.unshift(t);if(e.params.virtual.cache){const t=e.virtual.cache,n={};Object.keys(t).forEach((e=>{const r=t[e],l=r.attr("data-swiper-slide-index");l&&r.attr("data-swiper-slide-index",parseInt(l,10)+1),n[parseInt(e,10)+o]=r})),e.virtual.cache=n}e.virtual.update(!0),e.slideTo(r,0)},removeSlide(t){const e=this;if(null==t)return;let n=e.activeIndex;if(Array.isArray(t))for(let i=t.length-1;i>=0;i-=1)e.virtual.slides.splice(t[i],1),e.params.virtual.cache&&delete e.virtual.cache[t[i]],t[i]<n&&(n-=1),n=Math.max(n,0);else e.virtual.slides.splice(t,1),e.params.virtual.cache&&delete e.virtual.cache[t],t<n&&(n-=1),n=Math.max(n,0);e.virtual.update(!0),e.slideTo(n,0)},removeAllSlides(){const t=this;t.virtual.slides=[],t.params.virtual.cache&&(t.virtual.cache={}),t.virtual.update(!0),t.slideTo(0,0)}};var Z={name:"virtual",params:{virtual:{enabled:!1,slides:[],cache:!0,renderSlide:null,renderExternal:null,addSlidesBefore:0,addSlidesAfter:0}},create(){const t=this;y.extend(t,{virtual:{update:J.update.bind(t),appendSlide:J.appendSlide.bind(t),prependSlide:J.prependSlide.bind(t),removeSlide:J.removeSlide.bind(t),removeAllSlides:J.removeAllSlides.bind(t),renderSlide:J.renderSlide.bind(t),slides:t.params.virtual.slides,cache:{}}})},on:{beforeInit(){const t=this;if(!t.params.virtual.enabled)return;t.classNames.push(`${t.params.containerModifierClass}virtual`);const e={watchSlidesProgress:!0};y.extend(t.params,e),y.extend(t.originalParams,e),t.params.initialSlide||t.virtual.update()},setTranslate(){this.params.virtual.enabled&&this.virtual.update()}}};const K={handle(t){const e=this,{rtlTranslate:n}=e;let r=t;r.originalEvent&&(r=r.originalEvent);const o=r.keyCode||r.charCode,c=e.params.keyboard.pageUpDown,f=c&&33===o,h=c&&34===o,v=37===o,m=39===o,y=38===o,_=40===o;if(!e.allowSlideNext&&(e.isHorizontal()&&m||e.isVertical()&&_||h))return!1;if(!e.allowSlidePrev&&(e.isHorizontal()&&v||e.isVertical()&&y||f))return!1;if(!(r.shiftKey||r.altKey||r.ctrlKey||r.metaKey||l.activeElement&&l.activeElement.nodeName&&("input"===l.activeElement.nodeName.toLowerCase()||"textarea"===l.activeElement.nodeName.toLowerCase()))){if(e.params.keyboard.onlyInViewport&&(f||h||v||m||y||_)){let t=!1;if(e.$el.parents(`.${e.params.slideClass}`).length>0&&0===e.$el.parents(`.${e.params.slideActiveClass}`).length)return;const r=d.innerWidth,o=d.innerHeight,l=e.$el.offset();n&&(l.left-=e.$el[0].scrollLeft);const c=[[l.left,l.top],[l.left+e.width,l.top],[l.left,l.top+e.height],[l.left+e.width,l.top+e.height]];for(let i=0;i<c.length;i+=1){const e=c[i];e[0]>=0&&e[0]<=r&&e[1]>=0&&e[1]<=o&&(t=!0)}if(!t)return}e.isHorizontal()?((f||h||v||m)&&(r.preventDefault?r.preventDefault():r.returnValue=!1),((h||m)&&!n||(f||v)&&n)&&e.slideNext(),((f||v)&&!n||(h||m)&&n)&&e.slidePrev()):((f||h||y||_)&&(r.preventDefault?r.preventDefault():r.returnValue=!1),(h||_)&&e.slideNext(),(f||y)&&e.slidePrev()),e.emit("keyPress",o)}},enable(){const t=this;t.keyboard.enabled||(h(l).on("keydown",t.keyboard.handle),t.keyboard.enabled=!0)},disable(){const t=this;t.keyboard.enabled&&(h(l).off("keydown",t.keyboard.handle),t.keyboard.enabled=!1)}};var Q={name:"keyboard",params:{keyboard:{enabled:!1,onlyInViewport:!0,pageUpDown:!0}},create(){const t=this;y.extend(t,{keyboard:{enabled:!1,enable:K.enable.bind(t),disable:K.disable.bind(t),handle:K.handle.bind(t)}})},on:{init(){const t=this;t.params.keyboard.enabled&&t.keyboard.enable()},destroy(){const t=this;t.keyboard.enabled&&t.keyboard.disable()}}};const tt={lastScrollTime:y.now(),lastEventBeforeSnap:void 0,recentWheelEvents:[],event:()=>d.navigator.userAgent.indexOf("firefox")>-1?"DOMMouseScroll":function(){const t="onwheel";let e=t in l;if(!e){const element=l.createElement("div");element.setAttribute(t,"return;"),e="function"==typeof element.onwheel}return!e&&l.implementation&&l.implementation.hasFeature&&!0!==l.implementation.hasFeature("","")&&(e=l.implementation.hasFeature("Events.wheel","3.0")),e}()?"wheel":"mousewheel",normalize(t){let e=0,n=0,r=0,o=0;return"detail"in t&&(n=t.detail),"wheelDelta"in t&&(n=-t.wheelDelta/120),"wheelDeltaY"in t&&(n=-t.wheelDeltaY/120),"wheelDeltaX"in t&&(e=-t.wheelDeltaX/120),"axis"in t&&t.axis===t.HORIZONTAL_AXIS&&(e=n,n=0),r=10*e,o=10*n,"deltaY"in t&&(o=t.deltaY),"deltaX"in t&&(r=t.deltaX),t.shiftKey&&!r&&(r=o,o=0),(r||o)&&t.deltaMode&&(1===t.deltaMode?(r*=40,o*=40):(r*=800,o*=800)),r&&!e&&(e=r<1?-1:1),o&&!n&&(n=o<1?-1:1),{spinX:e,spinY:n,pixelX:r,pixelY:o}},handleMouseEnter(){this.mouseEntered=!0},handleMouseLeave(){this.mouseEntered=!1},handle(t){let e=t;const n=this,r=n.params.mousewheel;n.params.cssMode&&e.preventDefault();let o=n.$el;if("container"!==n.params.mousewheel.eventsTarged&&(o=h(n.params.mousewheel.eventsTarged)),!n.mouseEntered&&!o[0].contains(e.target)&&!r.releaseOnEdges)return!0;e.originalEvent&&(e=e.originalEvent);let l=0;const c=n.rtlTranslate?-1:1,data=tt.normalize(e);if(r.forceToAxis)if(n.isHorizontal()){if(!(Math.abs(data.pixelX)>Math.abs(data.pixelY)))return!0;l=-data.pixelX*c}else{if(!(Math.abs(data.pixelY)>Math.abs(data.pixelX)))return!0;l=-data.pixelY}else l=Math.abs(data.pixelX)>Math.abs(data.pixelY)?-data.pixelX*c:-data.pixelY;if(0===l)return!0;if(r.invert&&(l=-l),n.params.freeMode){const t={time:y.now(),delta:Math.abs(l),direction:Math.sign(l)},{lastEventBeforeSnap:o}=n.mousewheel,c=o&&t.time<o.time+500&&t.delta<=o.delta&&t.direction===o.direction;if(!c){n.mousewheel.lastEventBeforeSnap=void 0,n.params.loop&&n.loopFix();let o=n.getTranslate()+l*r.sensitivity;const d=n.isBeginning,f=n.isEnd;if(o>=n.minTranslate()&&(o=n.minTranslate()),o<=n.maxTranslate()&&(o=n.maxTranslate()),n.setTransition(0),n.setTranslate(o),n.updateProgress(),n.updateActiveIndex(),n.updateSlidesClasses(),(!d&&n.isBeginning||!f&&n.isEnd)&&n.updateSlidesClasses(),n.params.freeModeSticky){clearTimeout(n.mousewheel.timeout),n.mousewheel.timeout=void 0;const e=n.mousewheel.recentWheelEvents;e.length>=15&&e.shift();const r=e.length?e[e.length-1]:void 0,o=e[0];if(e.push(t),r&&(t.delta>r.delta||t.direction!==r.direction))e.splice(0);else if(e.length>=15&&t.time-o.time<500&&o.delta-t.delta>=1&&t.delta<=6){const r=l>0?.8:.2;n.mousewheel.lastEventBeforeSnap=t,e.splice(0),n.mousewheel.timeout=y.nextTick((()=>{n.slideToClosest(n.params.speed,!0,void 0,r)}),0)}n.mousewheel.timeout||(n.mousewheel.timeout=y.nextTick((()=>{n.mousewheel.lastEventBeforeSnap=t,e.splice(0),n.slideToClosest(n.params.speed,!0,void 0,.5)}),500))}if(c||n.emit("scroll",e),n.params.autoplay&&n.params.autoplayDisableOnInteraction&&n.autoplay.stop(),o===n.minTranslate()||o===n.maxTranslate())return!0}}else{const e={time:y.now(),delta:Math.abs(l),direction:Math.sign(l),raw:t},r=n.mousewheel.recentWheelEvents;r.length>=2&&r.shift();const o=r.length?r[r.length-1]:void 0;if(r.push(e),o?(e.direction!==o.direction||e.delta>o.delta||e.time>o.time+150)&&n.mousewheel.animateSlider(e):n.mousewheel.animateSlider(e),n.mousewheel.releaseScroll(e))return!0}return e.preventDefault?e.preventDefault():e.returnValue=!1,!1},animateSlider(t){const e=this;return t.delta>=6&&y.now()-e.mousewheel.lastScrollTime<60||(t.direction<0?e.isEnd&&!e.params.loop||e.animating||(e.slideNext(),e.emit("scroll",t.raw)):e.isBeginning&&!e.params.loop||e.animating||(e.slidePrev(),e.emit("scroll",t.raw)),e.mousewheel.lastScrollTime=(new d.Date).getTime(),!1)},releaseScroll(t){const e=this,n=e.params.mousewheel;if(t.direction<0){if(e.isEnd&&!e.params.loop&&n.releaseOnEdges)return!0}else if(e.isBeginning&&!e.params.loop&&n.releaseOnEdges)return!0;return!1},enable(){const t=this,e=tt.event();if(t.params.cssMode)return t.wrapperEl.removeEventListener(e,t.mousewheel.handle),!0;if(!e)return!1;if(t.mousewheel.enabled)return!1;let n=t.$el;return"container"!==t.params.mousewheel.eventsTarged&&(n=h(t.params.mousewheel.eventsTarged)),n.on("mouseenter",t.mousewheel.handleMouseEnter),n.on("mouseleave",t.mousewheel.handleMouseLeave),n.on(e,t.mousewheel.handle),t.mousewheel.enabled=!0,!0},disable(){const t=this,e=tt.event();if(t.params.cssMode)return t.wrapperEl.addEventListener(e,t.mousewheel.handle),!0;if(!e)return!1;if(!t.mousewheel.enabled)return!1;let n=t.$el;return"container"!==t.params.mousewheel.eventsTarged&&(n=h(t.params.mousewheel.eventsTarged)),n.off(e,t.mousewheel.handle),t.mousewheel.enabled=!1,!0}};const et={update(){const t=this,e=t.params.navigation;if(t.params.loop)return;const{$nextEl:n,$prevEl:r}=t.navigation;r&&r.length>0&&(t.isBeginning?r.addClass(e.disabledClass):r.removeClass(e.disabledClass),r[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](e.lockClass)),n&&n.length>0&&(t.isEnd?n.addClass(e.disabledClass):n.removeClass(e.disabledClass),n[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](e.lockClass))},onPrevClick(t){const e=this;t.preventDefault(),e.isBeginning&&!e.params.loop||e.slidePrev()},onNextClick(t){const e=this;t.preventDefault(),e.isEnd&&!e.params.loop||e.slideNext()},init(){const t=this,e=t.params.navigation;if(!e.nextEl&&!e.prevEl)return;let n,r;e.nextEl&&(n=h(e.nextEl),t.params.uniqueNavElements&&"string"==typeof e.nextEl&&n.length>1&&1===t.$el.find(e.nextEl).length&&(n=t.$el.find(e.nextEl))),e.prevEl&&(r=h(e.prevEl),t.params.uniqueNavElements&&"string"==typeof e.prevEl&&r.length>1&&1===t.$el.find(e.prevEl).length&&(r=t.$el.find(e.prevEl))),n&&n.length>0&&n.on("click",t.navigation.onNextClick),r&&r.length>0&&r.on("click",t.navigation.onPrevClick),y.extend(t.navigation,{$nextEl:n,nextEl:n&&n[0],$prevEl:r,prevEl:r&&r[0]})},destroy(){const t=this,{$nextEl:e,$prevEl:n}=t.navigation;e&&e.length&&(e.off("click",t.navigation.onNextClick),e.removeClass(t.params.navigation.disabledClass)),n&&n.length&&(n.off("click",t.navigation.onPrevClick),n.removeClass(t.params.navigation.disabledClass))}};const nt={update(){const t=this,e=t.rtl,n=t.params.pagination;if(!n.el||!t.pagination.el||!t.pagination.$el||0===t.pagination.$el.length)return;const r=t.virtual&&t.params.virtual.enabled?t.virtual.slides.length:t.slides.length,o=t.pagination.$el;let l;const c=t.params.loop?Math.ceil((r-2*t.loopedSlides)/t.params.slidesPerGroup):t.snapGrid.length;if(t.params.loop?(l=Math.ceil((t.activeIndex-t.loopedSlides)/t.params.slidesPerGroup),l>r-1-2*t.loopedSlides&&(l-=r-2*t.loopedSlides),l>c-1&&(l-=c),l<0&&"bullets"!==t.params.paginationType&&(l=c+l)):l=void 0!==t.snapIndex?t.snapIndex:t.activeIndex||0,"bullets"===n.type&&t.pagination.bullets&&t.pagination.bullets.length>0){const r=t.pagination.bullets;let c,d,f;if(n.dynamicBullets&&(t.pagination.bulletSize=r.eq(0)[t.isHorizontal()?"outerWidth":"outerHeight"](!0),o.css(t.isHorizontal()?"width":"height",t.pagination.bulletSize*(n.dynamicMainBullets+4)+"px"),n.dynamicMainBullets>1&&void 0!==t.previousIndex&&(t.pagination.dynamicBulletIndex+=l-t.previousIndex,t.pagination.dynamicBulletIndex>n.dynamicMainBullets-1?t.pagination.dynamicBulletIndex=n.dynamicMainBullets-1:t.pagination.dynamicBulletIndex<0&&(t.pagination.dynamicBulletIndex=0)),c=l-t.pagination.dynamicBulletIndex,d=c+(Math.min(r.length,n.dynamicMainBullets)-1),f=(d+c)/2),r.removeClass(`${n.bulletActiveClass} ${n.bulletActiveClass}-next ${n.bulletActiveClass}-next-next ${n.bulletActiveClass}-prev ${n.bulletActiveClass}-prev-prev ${n.bulletActiveClass}-main`),o.length>1)r.each(((t,e)=>{const r=h(e),o=r.index();o===l&&r.addClass(n.bulletActiveClass),n.dynamicBullets&&(o>=c&&o<=d&&r.addClass(`${n.bulletActiveClass}-main`),o===c&&r.prev().addClass(`${n.bulletActiveClass}-prev`).prev().addClass(`${n.bulletActiveClass}-prev-prev`),o===d&&r.next().addClass(`${n.bulletActiveClass}-next`).next().addClass(`${n.bulletActiveClass}-next-next`))}));else{const e=r.eq(l),o=e.index();if(e.addClass(n.bulletActiveClass),n.dynamicBullets){const e=r.eq(c),l=r.eq(d);for(let i=c;i<=d;i+=1)r.eq(i).addClass(`${n.bulletActiveClass}-main`);if(t.params.loop)if(o>=r.length-n.dynamicMainBullets){for(let i=n.dynamicMainBullets;i>=0;i-=1)r.eq(r.length-i).addClass(`${n.bulletActiveClass}-main`);r.eq(r.length-n.dynamicMainBullets-1).addClass(`${n.bulletActiveClass}-prev`)}else e.prev().addClass(`${n.bulletActiveClass}-prev`).prev().addClass(`${n.bulletActiveClass}-prev-prev`),l.next().addClass(`${n.bulletActiveClass}-next`).next().addClass(`${n.bulletActiveClass}-next-next`);else e.prev().addClass(`${n.bulletActiveClass}-prev`).prev().addClass(`${n.bulletActiveClass}-prev-prev`),l.next().addClass(`${n.bulletActiveClass}-next`).next().addClass(`${n.bulletActiveClass}-next-next`)}}if(n.dynamicBullets){const o=Math.min(r.length,n.dynamicMainBullets+4),l=(t.pagination.bulletSize*o-t.pagination.bulletSize)/2-f*t.pagination.bulletSize,c=e?"right":"left";r.css(t.isHorizontal()?c:"top",`${l}px`)}}if("fraction"===n.type&&(o.find(`.${n.currentClass}`).text(n.formatFractionCurrent(l+1)),o.find(`.${n.totalClass}`).text(n.formatFractionTotal(c))),"progressbar"===n.type){let e;e=n.progressbarOpposite?t.isHorizontal()?"vertical":"horizontal":t.isHorizontal()?"horizontal":"vertical";const r=(l+1)/c;let d=1,f=1;"horizontal"===e?d=r:f=r,o.find(`.${n.progressbarFillClass}`).transform(`translate3d(0,0,0) scaleX(${d}) scaleY(${f})`).transition(t.params.speed)}"custom"===n.type&&n.renderCustom?(o.html(n.renderCustom(t,l+1,c)),t.emit("paginationRender",t,o[0])):t.emit("paginationUpdate",t,o[0]),o[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](n.lockClass)},render(){const t=this,e=t.params.pagination;if(!e.el||!t.pagination.el||!t.pagination.$el||0===t.pagination.$el.length)return;const n=t.virtual&&t.params.virtual.enabled?t.virtual.slides.length:t.slides.length,r=t.pagination.$el;let o="";if("bullets"===e.type){const l=t.params.loop?Math.ceil((n-2*t.loopedSlides)/t.params.slidesPerGroup):t.snapGrid.length;for(let i=0;i<l;i+=1)e.renderBullet?o+=e.renderBullet.call(t,i,e.bulletClass):o+=`<${e.bulletElement} class="${e.bulletClass}"></${e.bulletElement}>`;r.html(o),t.pagination.bullets=r.find(`.${e.bulletClass}`)}"fraction"===e.type&&(o=e.renderFraction?e.renderFraction.call(t,e.currentClass,e.totalClass):`<span class="${e.currentClass}"></span> / <span class="${e.totalClass}"></span>`,r.html(o)),"progressbar"===e.type&&(o=e.renderProgressbar?e.renderProgressbar.call(t,e.progressbarFillClass):`<span class="${e.progressbarFillClass}"></span>`,r.html(o)),"custom"!==e.type&&t.emit("paginationRender",t.pagination.$el[0])},init(){const t=this,e=t.params.pagination;if(!e.el)return;let n=h(e.el);0!==n.length&&(t.params.uniqueNavElements&&"string"==typeof e.el&&n.length>1&&(n=t.$el.find(e.el)),"bullets"===e.type&&e.clickable&&n.addClass(e.clickableClass),n.addClass(e.modifierClass+e.type),"bullets"===e.type&&e.dynamicBullets&&(n.addClass(`${e.modifierClass}${e.type}-dynamic`),t.pagination.dynamicBulletIndex=0,e.dynamicMainBullets<1&&(e.dynamicMainBullets=1)),"progressbar"===e.type&&e.progressbarOpposite&&n.addClass(e.progressbarOppositeClass),e.clickable&&n.on("click",`.${e.bulletClass}`,(function(e){e.preventDefault();let n=h(this).index()*t.params.slidesPerGroup;t.params.loop&&(n+=t.loopedSlides),t.slideTo(n)})),y.extend(t.pagination,{$el:n,el:n[0]}))},destroy(){const t=this,e=t.params.pagination;if(!e.el||!t.pagination.el||!t.pagination.$el||0===t.pagination.$el.length)return;const n=t.pagination.$el;n.removeClass(e.hiddenClass),n.removeClass(e.modifierClass+e.type),t.pagination.bullets&&t.pagination.bullets.removeClass(e.bulletActiveClass),e.clickable&&n.off("click",`.${e.bulletClass}`)}};const it={setTranslate(){const t=this;if(!t.params.scrollbar.el||!t.scrollbar.el)return;const{scrollbar:e,rtlTranslate:n,progress:progress}=t,{dragSize:r,trackSize:o,$dragEl:l,$el:c}=e,d=t.params.scrollbar;let f=r,h=(o-r)*progress;n?(h=-h,h>0?(f=r-h,h=0):-h+r>o&&(f=o+h)):h<0?(f=r+h,h=0):h+r>o&&(f=o-h),t.isHorizontal()?(l.transform(`translate3d(${h}px, 0, 0)`),l[0].style.width=`${f}px`):(l.transform(`translate3d(0px, ${h}px, 0)`),l[0].style.height=`${f}px`),d.hide&&(clearTimeout(t.scrollbar.timeout),c[0].style.opacity=1,t.scrollbar.timeout=setTimeout((()=>{c[0].style.opacity=0,c.transition(400)}),1e3))},setTransition(t){const e=this;e.params.scrollbar.el&&e.scrollbar.el&&e.scrollbar.$dragEl.transition(t)},updateSize(){const t=this;if(!t.params.scrollbar.el||!t.scrollbar.el)return;const{scrollbar:e}=t,{$dragEl:n,$el:r}=e;n[0].style.width="",n[0].style.height="";const o=t.isHorizontal()?r[0].offsetWidth:r[0].offsetHeight,l=t.size/t.virtualSize,c=l*(o/t.size);let d;d="auto"===t.params.scrollbar.dragSize?o*l:parseInt(t.params.scrollbar.dragSize,10),t.isHorizontal()?n[0].style.width=`${d}px`:n[0].style.height=`${d}px`,r[0].style.display=l>=1?"none":"",t.params.scrollbar.hide&&(r[0].style.opacity=0),y.extend(e,{trackSize:o,divider:l,moveDivider:c,dragSize:d}),e.$el[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](t.params.scrollbar.lockClass)},getPointerPosition(t){return this.isHorizontal()?"touchstart"===t.type||"touchmove"===t.type?t.targetTouches[0].clientX:t.clientX:"touchstart"===t.type||"touchmove"===t.type?t.targetTouches[0].clientY:t.clientY},setDragPosition(t){const e=this,{scrollbar:n,rtlTranslate:r}=e,{$el:o,dragSize:l,trackSize:c,dragStartPos:d}=n;let f;f=(n.getPointerPosition(t)-o.offset()[e.isHorizontal()?"left":"top"]-(null!==d?d:l/2))/(c-l),f=Math.max(Math.min(f,1),0),r&&(f=1-f);const h=e.minTranslate()+(e.maxTranslate()-e.minTranslate())*f;e.updateProgress(h),e.setTranslate(h),e.updateActiveIndex(),e.updateSlidesClasses()},onDragStart(t){const e=this,n=e.params.scrollbar,{scrollbar:r,$wrapperEl:o}=e,{$el:l,$dragEl:c}=r;e.scrollbar.isTouched=!0,e.scrollbar.dragStartPos=t.target===c[0]||t.target===c?r.getPointerPosition(t)-t.target.getBoundingClientRect()[e.isHorizontal()?"left":"top"]:null,t.preventDefault(),t.stopPropagation(),o.transition(100),c.transition(100),r.setDragPosition(t),clearTimeout(e.scrollbar.dragTimeout),l.transition(0),n.hide&&l.css("opacity",1),e.params.cssMode&&e.$wrapperEl.css("scroll-snap-type","none"),e.emit("scrollbarDragStart",t)},onDragMove(t){const e=this,{scrollbar:n,$wrapperEl:r}=e,{$el:o,$dragEl:l}=n;e.scrollbar.isTouched&&(t.preventDefault?t.preventDefault():t.returnValue=!1,n.setDragPosition(t),r.transition(0),o.transition(0),l.transition(0),e.emit("scrollbarDragMove",t))},onDragEnd(t){const e=this,n=e.params.scrollbar,{scrollbar:r,$wrapperEl:o}=e,{$el:l}=r;e.scrollbar.isTouched&&(e.scrollbar.isTouched=!1,e.params.cssMode&&(e.$wrapperEl.css("scroll-snap-type",""),o.transition("")),n.hide&&(clearTimeout(e.scrollbar.dragTimeout),e.scrollbar.dragTimeout=y.nextTick((()=>{l.css("opacity",0),l.transition(400)}),1e3)),e.emit("scrollbarDragEnd",t),n.snapOnRelease&&e.slideToClosest())},enableDraggable(){const t=this;if(!t.params.scrollbar.el)return;const{scrollbar:e,touchEventsTouch:n,touchEventsDesktop:r,params:o}=t,c=e.$el[0],d=!(!_.passiveListener||!o.passiveListeners)&&{passive:!1,capture:!1},f=!(!_.passiveListener||!o.passiveListeners)&&{passive:!0,capture:!1};_.touch?(c.addEventListener(n.start,t.scrollbar.onDragStart,d),c.addEventListener(n.move,t.scrollbar.onDragMove,d),c.addEventListener(n.end,t.scrollbar.onDragEnd,f)):(c.addEventListener(r.start,t.scrollbar.onDragStart,d),l.addEventListener(r.move,t.scrollbar.onDragMove,d),l.addEventListener(r.end,t.scrollbar.onDragEnd,f))},disableDraggable(){const t=this;if(!t.params.scrollbar.el)return;const{scrollbar:e,touchEventsTouch:n,touchEventsDesktop:r,params:o}=t,c=e.$el[0],d=!(!_.passiveListener||!o.passiveListeners)&&{passive:!1,capture:!1},f=!(!_.passiveListener||!o.passiveListeners)&&{passive:!0,capture:!1};_.touch?(c.removeEventListener(n.start,t.scrollbar.onDragStart,d),c.removeEventListener(n.move,t.scrollbar.onDragMove,d),c.removeEventListener(n.end,t.scrollbar.onDragEnd,f)):(c.removeEventListener(r.start,t.scrollbar.onDragStart,d),l.removeEventListener(r.move,t.scrollbar.onDragMove,d),l.removeEventListener(r.end,t.scrollbar.onDragEnd,f))},init(){const t=this;if(!t.params.scrollbar.el)return;const{scrollbar:e,$el:n}=t,r=t.params.scrollbar;let o=h(r.el);t.params.uniqueNavElements&&"string"==typeof r.el&&o.length>1&&1===n.find(r.el).length&&(o=n.find(r.el));let l=o.find(`.${t.params.scrollbar.dragClass}`);0===l.length&&(l=h(`<div class="${t.params.scrollbar.dragClass}"></div>`),o.append(l)),y.extend(e,{$el:o,el:o[0],$dragEl:l,dragEl:l[0]}),r.draggable&&e.enableDraggable()},destroy(){this.scrollbar.disableDraggable()}};const ot={setTransform(t,progress){const{rtl:e}=this,n=h(t),r=e?-1:1,p=n.attr("data-swiper-parallax")||"0";let o=n.attr("data-swiper-parallax-x"),l=n.attr("data-swiper-parallax-y");const c=n.attr("data-swiper-parallax-scale"),d=n.attr("data-swiper-parallax-opacity");if(o||l?(o=o||"0",l=l||"0"):this.isHorizontal()?(o=p,l="0"):(l=p,o="0"),o=o.indexOf("%")>=0?parseInt(o,10)*progress*r+"%":o*progress*r+"px",l=l.indexOf("%")>=0?parseInt(l,10)*progress+"%":l*progress+"px",null!=d){const t=d-(d-1)*(1-Math.abs(progress));n[0].style.opacity=t}if(null==c)n.transform(`translate3d(${o}, ${l}, 0px)`);else{const t=c-(c-1)*(1-Math.abs(progress));n.transform(`translate3d(${o}, ${l}, 0px) scale(${t})`)}},setTranslate(){const t=this,{$el:e,slides:n,progress:progress,snapGrid:r}=t;e.children("[data-swiper-parallax], [data-swiper-parallax-x], [data-swiper-parallax-y], [data-swiper-parallax-opacity], [data-swiper-parallax-scale]").each(((e,n)=>{t.parallax.setTransform(n,progress)})),n.each(((e,n)=>{let o=n.progress;t.params.slidesPerGroup>1&&"auto"!==t.params.slidesPerView&&(o+=Math.ceil(e/2)-progress*(r.length-1)),o=Math.min(Math.max(o,-1),1),h(n).find("[data-swiper-parallax], [data-swiper-parallax-x], [data-swiper-parallax-y], [data-swiper-parallax-opacity], [data-swiper-parallax-scale]").each(((e,n)=>{t.parallax.setTransform(n,o)}))}))},setTransition(t=this.params.speed){const{$el:e}=this;e.find("[data-swiper-parallax], [data-swiper-parallax-x], [data-swiper-parallax-y], [data-swiper-parallax-opacity], [data-swiper-parallax-scale]").each(((e,n)=>{const r=h(n);let o=parseInt(r.attr("data-swiper-parallax-duration"),10)||t;0===t&&(o=0),r.transition(o)}))}};const at={getDistanceBetweenTouches(t){if(t.targetTouches.length<2)return 1;const e=t.targetTouches[0].pageX,n=t.targetTouches[0].pageY,r=t.targetTouches[1].pageX,o=t.targetTouches[1].pageY;return Math.sqrt((r-e)**2+(o-n)**2)},onGestureStart(t){const e=this,n=e.params.zoom,r=e.zoom,{gesture:o}=r;if(r.fakeGestureTouched=!1,r.fakeGestureMoved=!1,!_.gestures){if("touchstart"!==t.type||"touchstart"===t.type&&t.targetTouches.length<2)return;r.fakeGestureTouched=!0,o.scaleStart=at.getDistanceBetweenTouches(t)}o.$slideEl&&o.$slideEl.length||(o.$slideEl=h(t.target).closest(`.${e.params.slideClass}`),0===o.$slideEl.length&&(o.$slideEl=e.slides.eq(e.activeIndex)),o.$imageEl=o.$slideEl.find("img, svg, canvas, picture, .swiper-zoom-target"),o.$imageWrapEl=o.$imageEl.parent(`.${n.containerClass}`),o.maxRatio=o.$imageWrapEl.attr("data-swiper-zoom")||n.maxRatio,0!==o.$imageWrapEl.length)?(o.$imageEl&&o.$imageEl.transition(0),e.zoom.isScaling=!0):o.$imageEl=void 0},onGestureChange(t){const e=this.params.zoom,n=this.zoom,{gesture:r}=n;if(!_.gestures){if("touchmove"!==t.type||"touchmove"===t.type&&t.targetTouches.length<2)return;n.fakeGestureMoved=!0,r.scaleMove=at.getDistanceBetweenTouches(t)}r.$imageEl&&0!==r.$imageEl.length&&(n.scale=_.gestures?t.scale*n.currentScale:r.scaleMove/r.scaleStart*n.currentScale,n.scale>r.maxRatio&&(n.scale=r.maxRatio-1+(n.scale-r.maxRatio+1)**.5),n.scale<e.minRatio&&(n.scale=e.minRatio+1-(e.minRatio-n.scale+1)**.5),r.$imageEl.transform(`translate3d(0,0,0) scale(${n.scale})`))},onGestureEnd(t){const e=this,n=e.params.zoom,r=e.zoom,{gesture:o}=r;if(!_.gestures){if(!r.fakeGestureTouched||!r.fakeGestureMoved)return;if("touchend"!==t.type||"touchend"===t.type&&t.changedTouches.length<2&&!j.android)return;r.fakeGestureTouched=!1,r.fakeGestureMoved=!1}o.$imageEl&&0!==o.$imageEl.length&&(r.scale=Math.max(Math.min(r.scale,o.maxRatio),n.minRatio),o.$imageEl.transition(e.params.speed).transform(`translate3d(0,0,0) scale(${r.scale})`),r.currentScale=r.scale,r.isScaling=!1,1===r.scale&&(o.$slideEl=void 0))},onTouchStart(t){const e=this.zoom,{gesture:n,image:image}=e;n.$imageEl&&0!==n.$imageEl.length&&(image.isTouched||(j.android&&t.cancelable&&t.preventDefault(),image.isTouched=!0,image.touchesStart.x="touchstart"===t.type?t.targetTouches[0].pageX:t.pageX,image.touchesStart.y="touchstart"===t.type?t.targetTouches[0].pageY:t.pageY))},onTouchMove(t){const e=this,n=e.zoom,{gesture:r,image:image,velocity:o}=n;if(!r.$imageEl||0===r.$imageEl.length)return;if(e.allowClick=!1,!image.isTouched||!r.$slideEl)return;image.isMoved||(image.width=r.$imageEl[0].offsetWidth,image.height=r.$imageEl[0].offsetHeight,image.startX=y.getTranslate(r.$imageWrapEl[0],"x")||0,image.startY=y.getTranslate(r.$imageWrapEl[0],"y")||0,r.slideWidth=r.$slideEl[0].offsetWidth,r.slideHeight=r.$slideEl[0].offsetHeight,r.$imageWrapEl.transition(0),e.rtl&&(image.startX=-image.startX,image.startY=-image.startY));const l=image.width*n.scale,c=image.height*n.scale;if(!(l<r.slideWidth&&c<r.slideHeight)){if(image.minX=Math.min(r.slideWidth/2-l/2,0),image.maxX=-image.minX,image.minY=Math.min(r.slideHeight/2-c/2,0),image.maxY=-image.minY,image.touchesCurrent.x="touchmove"===t.type?t.targetTouches[0].pageX:t.pageX,image.touchesCurrent.y="touchmove"===t.type?t.targetTouches[0].pageY:t.pageY,!image.isMoved&&!n.isScaling){if(e.isHorizontal()&&(Math.floor(image.minX)===Math.floor(image.startX)&&image.touchesCurrent.x<image.touchesStart.x||Math.floor(image.maxX)===Math.floor(image.startX)&&image.touchesCurrent.x>image.touchesStart.x))return void(image.isTouched=!1);if(!e.isHorizontal()&&(Math.floor(image.minY)===Math.floor(image.startY)&&image.touchesCurrent.y<image.touchesStart.y||Math.floor(image.maxY)===Math.floor(image.startY)&&image.touchesCurrent.y>image.touchesStart.y))return void(image.isTouched=!1)}t.cancelable&&t.preventDefault(),t.stopPropagation(),image.isMoved=!0,image.currentX=image.touchesCurrent.x-image.touchesStart.x+image.startX,image.currentY=image.touchesCurrent.y-image.touchesStart.y+image.startY,image.currentX<image.minX&&(image.currentX=image.minX+1-(image.minX-image.currentX+1)**.8),image.currentX>image.maxX&&(image.currentX=image.maxX-1+(image.currentX-image.maxX+1)**.8),image.currentY<image.minY&&(image.currentY=image.minY+1-(image.minY-image.currentY+1)**.8),image.currentY>image.maxY&&(image.currentY=image.maxY-1+(image.currentY-image.maxY+1)**.8),o.prevPositionX||(o.prevPositionX=image.touchesCurrent.x),o.prevPositionY||(o.prevPositionY=image.touchesCurrent.y),o.prevTime||(o.prevTime=Date.now()),o.x=(image.touchesCurrent.x-o.prevPositionX)/(Date.now()-o.prevTime)/2,o.y=(image.touchesCurrent.y-o.prevPositionY)/(Date.now()-o.prevTime)/2,Math.abs(image.touchesCurrent.x-o.prevPositionX)<2&&(o.x=0),Math.abs(image.touchesCurrent.y-o.prevPositionY)<2&&(o.y=0),o.prevPositionX=image.touchesCurrent.x,o.prevPositionY=image.touchesCurrent.y,o.prevTime=Date.now(),r.$imageWrapEl.transform(`translate3d(${image.currentX}px, ${image.currentY}px,0)`)}},onTouchEnd(){const t=this.zoom,{gesture:e,image:image,velocity:n}=t;if(!e.$imageEl||0===e.$imageEl.length)return;if(!image.isTouched||!image.isMoved)return image.isTouched=!1,void(image.isMoved=!1);image.isTouched=!1,image.isMoved=!1;let r=300,o=300;const l=n.x*r,c=image.currentX+l,d=n.y*o,f=image.currentY+d;0!==n.x&&(r=Math.abs((c-image.currentX)/n.x)),0!==n.y&&(o=Math.abs((f-image.currentY)/n.y));const h=Math.max(r,o);image.currentX=c,image.currentY=f;const v=image.width*t.scale,m=image.height*t.scale;image.minX=Math.min(e.slideWidth/2-v/2,0),image.maxX=-image.minX,image.minY=Math.min(e.slideHeight/2-m/2,0),image.maxY=-image.minY,image.currentX=Math.max(Math.min(image.currentX,image.maxX),image.minX),image.currentY=Math.max(Math.min(image.currentY,image.maxY),image.minY),e.$imageWrapEl.transition(h).transform(`translate3d(${image.currentX}px, ${image.currentY}px,0)`)},onTransitionEnd(){const t=this,e=t.zoom,{gesture:n}=e;n.$slideEl&&t.previousIndex!==t.activeIndex&&(n.$imageEl&&n.$imageEl.transform("translate3d(0,0,0) scale(1)"),n.$imageWrapEl&&n.$imageWrapEl.transform("translate3d(0,0,0)"),e.scale=1,e.currentScale=1,n.$slideEl=void 0,n.$imageEl=void 0,n.$imageWrapEl=void 0)},toggle(t){const e=this.zoom;e.scale&&1!==e.scale?e.out():e.in(t)},in(t){const e=this,n=e.zoom,r=e.params.zoom,{gesture:o,image:image}=n;if(o.$slideEl||(e.params.virtual&&e.params.virtual.enabled&&e.virtual?o.$slideEl=e.$wrapperEl.children(`.${e.params.slideActiveClass}`):o.$slideEl=e.slides.eq(e.activeIndex),o.$imageEl=o.$slideEl.find("img, svg, canvas, picture, .swiper-zoom-target"),o.$imageWrapEl=o.$imageEl.parent(`.${r.containerClass}`)),!o.$imageEl||0===o.$imageEl.length)return;let l,c,d,f,h,v,m,y,_,w,x,S,E,O,C,T,k,j;o.$slideEl.addClass(`${r.zoomedSlideClass}`),void 0===image.touchesStart.x&&t?(l="touchend"===t.type?t.changedTouches[0].pageX:t.pageX,c="touchend"===t.type?t.changedTouches[0].pageY:t.pageY):(l=image.touchesStart.x,c=image.touchesStart.y),n.scale=o.$imageWrapEl.attr("data-swiper-zoom")||r.maxRatio,n.currentScale=o.$imageWrapEl.attr("data-swiper-zoom")||r.maxRatio,t?(k=o.$slideEl[0].offsetWidth,j=o.$slideEl[0].offsetHeight,d=o.$slideEl.offset().left,f=o.$slideEl.offset().top,h=d+k/2-l,v=f+j/2-c,_=o.$imageEl[0].offsetWidth,w=o.$imageEl[0].offsetHeight,x=_*n.scale,S=w*n.scale,E=Math.min(k/2-x/2,0),O=Math.min(j/2-S/2,0),C=-E,T=-O,m=h*n.scale,y=v*n.scale,m<E&&(m=E),m>C&&(m=C),y<O&&(y=O),y>T&&(y=T)):(m=0,y=0),o.$imageWrapEl.transition(300).transform(`translate3d(${m}px, ${y}px,0)`),o.$imageEl.transition(300).transform(`translate3d(0,0,0) scale(${n.scale})`)},out(){const t=this,e=t.zoom,n=t.params.zoom,{gesture:r}=e;r.$slideEl||(t.params.virtual&&t.params.virtual.enabled&&t.virtual?r.$slideEl=t.$wrapperEl.children(`.${t.params.slideActiveClass}`):r.$slideEl=t.slides.eq(t.activeIndex),r.$imageEl=r.$slideEl.find("img, svg, canvas, picture, .swiper-zoom-target"),r.$imageWrapEl=r.$imageEl.parent(`.${n.containerClass}`)),r.$imageEl&&0!==r.$imageEl.length&&(e.scale=1,e.currentScale=1,r.$imageWrapEl.transition(300).transform("translate3d(0,0,0)"),r.$imageEl.transition(300).transform("translate3d(0,0,0) scale(1)"),r.$slideEl.removeClass(`${n.zoomedSlideClass}`),r.$slideEl=void 0)},enable(){const t=this,e=t.zoom;if(e.enabled)return;e.enabled=!0;const n=!("touchstart"!==t.touchEvents.start||!_.passiveListener||!t.params.passiveListeners)&&{passive:!0,capture:!1},r=!_.passiveListener||{passive:!1,capture:!0},o=`.${t.params.slideClass}`;_.gestures?(t.$wrapperEl.on("gesturestart",o,e.onGestureStart,n),t.$wrapperEl.on("gesturechange",o,e.onGestureChange,n),t.$wrapperEl.on("gestureend",o,e.onGestureEnd,n)):"touchstart"===t.touchEvents.start&&(t.$wrapperEl.on(t.touchEvents.start,o,e.onGestureStart,n),t.$wrapperEl.on(t.touchEvents.move,o,e.onGestureChange,r),t.$wrapperEl.on(t.touchEvents.end,o,e.onGestureEnd,n),t.touchEvents.cancel&&t.$wrapperEl.on(t.touchEvents.cancel,o,e.onGestureEnd,n)),t.$wrapperEl.on(t.touchEvents.move,`.${t.params.zoom.containerClass}`,e.onTouchMove,r)},disable(){const t=this,e=t.zoom;if(!e.enabled)return;t.zoom.enabled=!1;const n=!("touchstart"!==t.touchEvents.start||!_.passiveListener||!t.params.passiveListeners)&&{passive:!0,capture:!1},r=!_.passiveListener||{passive:!1,capture:!0},o=`.${t.params.slideClass}`;_.gestures?(t.$wrapperEl.off("gesturestart",o,e.onGestureStart,n),t.$wrapperEl.off("gesturechange",o,e.onGestureChange,n),t.$wrapperEl.off("gestureend",o,e.onGestureEnd,n)):"touchstart"===t.touchEvents.start&&(t.$wrapperEl.off(t.touchEvents.start,o,e.onGestureStart,n),t.$wrapperEl.off(t.touchEvents.move,o,e.onGestureChange,r),t.$wrapperEl.off(t.touchEvents.end,o,e.onGestureEnd,n),t.touchEvents.cancel&&t.$wrapperEl.off(t.touchEvents.cancel,o,e.onGestureEnd,n)),t.$wrapperEl.off(t.touchEvents.move,`.${t.params.zoom.containerClass}`,e.onTouchMove,r)}};const st={loadInSlide(t,e=!0){const n=this,r=n.params.lazy;if(void 0===t)return;if(0===n.slides.length)return;const o=n.virtual&&n.params.virtual.enabled?n.$wrapperEl.children(`.${n.params.slideClass}[data-swiper-slide-index="${t}"]`):n.slides.eq(t);let l=o.find(`.${r.elementClass}:not(.${r.loadedClass}):not(.${r.loadingClass})`);!o.hasClass(r.elementClass)||o.hasClass(r.loadedClass)||o.hasClass(r.loadingClass)||(l=l.add(o[0])),0!==l.length&&l.each(((t,l)=>{const c=h(l);c.addClass(r.loadingClass);const d=c.attr("data-background"),f=c.attr("data-src"),v=c.attr("data-srcset"),m=c.attr("data-sizes"),y=c.parent("picture");n.loadImage(c[0],f||d,v,m,!1,(()=>{if(null!=n&&n&&(!n||n.params)&&!n.destroyed){if(d?(c.css("background-image",`url("${d}")`),c.removeAttr("data-background")):(v&&(c.attr("srcset",v),c.removeAttr("data-srcset")),m&&(c.attr("sizes",m),c.removeAttr("data-sizes")),y.length&&y.children("source").each(((t,e)=>{const n=h(e);n.attr("data-srcset")&&(n.attr("srcset",n.attr("data-srcset")),n.removeAttr("data-srcset"))})),f&&(c.attr("src",f),c.removeAttr("data-src"))),c.addClass(r.loadedClass).removeClass(r.loadingClass),o.find(`.${r.preloaderClass}`).remove(),n.params.loop&&e){const t=o.attr("data-swiper-slide-index");if(o.hasClass(n.params.slideDuplicateClass)){const e=n.$wrapperEl.children(`[data-swiper-slide-index="${t}"]:not(.${n.params.slideDuplicateClass})`);n.lazy.loadInSlide(e.index(),!1)}else{const e=n.$wrapperEl.children(`.${n.params.slideDuplicateClass}[data-swiper-slide-index="${t}"]`);n.lazy.loadInSlide(e.index(),!1)}}n.emit("lazyImageReady",o[0],c[0]),n.params.autoHeight&&n.updateAutoHeight()}})),n.emit("lazyImageLoad",o[0],c[0])}))},load(){const t=this,{$wrapperEl:e,params:n,slides:r,activeIndex:o}=t,l=t.virtual&&n.virtual.enabled,c=n.lazy;let d=n.slidesPerView;function f(t){if(l){if(e.children(`.${n.slideClass}[data-swiper-slide-index="${t}"]`).length)return!0}else if(r[t])return!0;return!1}function v(t){return l?h(t).attr("data-swiper-slide-index"):h(t).index()}if("auto"===d&&(d=0),t.lazy.initialImageLoaded||(t.lazy.initialImageLoaded=!0),t.params.watchSlidesVisibility)e.children(`.${n.slideVisibleClass}`).each(((e,n)=>{const r=l?h(n).attr("data-swiper-slide-index"):h(n).index();t.lazy.loadInSlide(r)}));else if(d>1)for(let i=o;i<o+d;i+=1)f(i)&&t.lazy.loadInSlide(i);else t.lazy.loadInSlide(o);if(c.loadPrevNext)if(d>1||c.loadPrevNextAmount&&c.loadPrevNextAmount>1){const e=c.loadPrevNextAmount,n=d,l=Math.min(o+n+Math.max(e,n),r.length),h=Math.max(o-Math.max(n,e),0);for(let i=o+d;i<l;i+=1)f(i)&&t.lazy.loadInSlide(i);for(let i=h;i<o;i+=1)f(i)&&t.lazy.loadInSlide(i)}else{const r=e.children(`.${n.slideNextClass}`);r.length>0&&t.lazy.loadInSlide(v(r));const o=e.children(`.${n.slidePrevClass}`);o.length>0&&t.lazy.loadInSlide(v(o))}}};const lt={LinearSpline:function(t,e){const n=function(){let t,e,n;return(r,o)=>{for(e=-1,t=r.length;t-e>1;)n=t+e>>1,r[n]<=o?e=n:t=n;return t}}();let r,o;return this.x=t,this.y=e,this.lastIndex=t.length-1,this.interpolate=function(t){return t?(o=n(this.x,t),r=o-1,(t-this.x[r])*(this.y[o]-this.y[r])/(this.x[o]-this.x[r])+this.y[r]):0},this},getInterpolateFunction(t){const e=this;e.controller.spline||(e.controller.spline=e.params.loop?new lt.LinearSpline(e.slidesGrid,t.slidesGrid):new lt.LinearSpline(e.snapGrid,t.snapGrid))},setTranslate(t,e){const n=this,r=n.controller.control;let o,l;function c(t){const e=n.rtlTranslate?-n.translate:n.translate;"slide"===n.params.controller.by&&(n.controller.getInterpolateFunction(t),l=-n.controller.spline.interpolate(-e)),l&&"container"!==n.params.controller.by||(o=(t.maxTranslate()-t.minTranslate())/(n.maxTranslate()-n.minTranslate()),l=(e-n.minTranslate())*o+t.minTranslate()),n.params.controller.inverse&&(l=t.maxTranslate()-l),t.updateProgress(l),t.setTranslate(l,n),t.updateActiveIndex(),t.updateSlidesClasses()}if(Array.isArray(r))for(let i=0;i<r.length;i+=1)r[i]!==e&&r[i]instanceof F&&c(r[i]);else r instanceof F&&e!==r&&c(r)},setTransition(t,e){const n=this,r=n.controller.control;let i;function o(e){e.setTransition(t,n),0!==t&&(e.transitionStart(),e.params.autoHeight&&y.nextTick((()=>{e.updateAutoHeight()})),e.$wrapperEl.transitionEnd((()=>{r&&(e.params.loop&&"slide"===n.params.controller.by&&e.loopFix(),e.transitionEnd())})))}if(Array.isArray(r))for(i=0;i<r.length;i+=1)r[i]!==e&&r[i]instanceof F&&o(r[i]);else r instanceof F&&e!==r&&o(r)}};const ut={makeElFocusable:t=>(t.attr("tabIndex","0"),t),makeElNotFocusable:t=>(t.attr("tabIndex","-1"),t),addElRole:(t,e)=>(t.attr("role",e),t),addElLabel:(t,label)=>(t.attr("aria-label",label),t),disableEl:t=>(t.attr("aria-disabled",!0),t),enableEl:t=>(t.attr("aria-disabled",!1),t),onEnterKey(t){const e=this,n=e.params.a11y;if(13!==t.keyCode)return;const r=h(t.target);e.navigation&&e.navigation.$nextEl&&r.is(e.navigation.$nextEl)&&(e.isEnd&&!e.params.loop||e.slideNext(),e.isEnd?e.a11y.notify(n.lastSlideMessage):e.a11y.notify(n.nextSlideMessage)),e.navigation&&e.navigation.$prevEl&&r.is(e.navigation.$prevEl)&&(e.isBeginning&&!e.params.loop||e.slidePrev(),e.isBeginning?e.a11y.notify(n.firstSlideMessage):e.a11y.notify(n.prevSlideMessage)),e.pagination&&r.is(`.${e.params.pagination.bulletClass}`)&&r[0].click()},notify(t){const e=this.a11y.liveRegion;0!==e.length&&(e.html(""),e.html(t))},updateNavigation(){const t=this;if(t.params.loop||!t.navigation)return;const{$nextEl:e,$prevEl:n}=t.navigation;n&&n.length>0&&(t.isBeginning?(t.a11y.disableEl(n),t.a11y.makeElNotFocusable(n)):(t.a11y.enableEl(n),t.a11y.makeElFocusable(n))),e&&e.length>0&&(t.isEnd?(t.a11y.disableEl(e),t.a11y.makeElNotFocusable(e)):(t.a11y.enableEl(e),t.a11y.makeElFocusable(e)))},updatePagination(){const t=this,e=t.params.a11y;t.pagination&&t.params.pagination.clickable&&t.pagination.bullets&&t.pagination.bullets.length&&t.pagination.bullets.each(((n,r)=>{const o=h(r);t.a11y.makeElFocusable(o),t.a11y.addElRole(o,"button"),t.a11y.addElLabel(o,e.paginationBulletMessage.replace(/\{\{index\}\}/,o.index()+1))}))},init(){const t=this;t.$el.append(t.a11y.liveRegion);const e=t.params.a11y;let n,r;t.navigation&&t.navigation.$nextEl&&(n=t.navigation.$nextEl),t.navigation&&t.navigation.$prevEl&&(r=t.navigation.$prevEl),n&&(t.a11y.makeElFocusable(n),t.a11y.addElRole(n,"button"),t.a11y.addElLabel(n,e.nextSlideMessage),n.on("keydown",t.a11y.onEnterKey)),r&&(t.a11y.makeElFocusable(r),t.a11y.addElRole(r,"button"),t.a11y.addElLabel(r,e.prevSlideMessage),r.on("keydown",t.a11y.onEnterKey)),t.pagination&&t.params.pagination.clickable&&t.pagination.bullets&&t.pagination.bullets.length&&t.pagination.$el.on("keydown",`.${t.params.pagination.bulletClass}`,t.a11y.onEnterKey)},destroy(){const t=this;let e,n;t.a11y.liveRegion&&t.a11y.liveRegion.length>0&&t.a11y.liveRegion.remove(),t.navigation&&t.navigation.$nextEl&&(e=t.navigation.$nextEl),t.navigation&&t.navigation.$prevEl&&(n=t.navigation.$prevEl),e&&e.off("keydown",t.a11y.onEnterKey),n&&n.off("keydown",t.a11y.onEnterKey),t.pagination&&t.params.pagination.clickable&&t.pagination.bullets&&t.pagination.bullets.length&&t.pagination.$el.off("keydown",`.${t.params.pagination.bulletClass}`,t.a11y.onEnterKey)}};const ct={init(){const t=this;if(!t.params.history)return;if(!d.history||!d.history.pushState)return t.params.history.enabled=!1,void(t.params.hashNavigation.enabled=!0);const e=t.history;e.initialized=!0,e.paths=ct.getPathValues(),(e.paths.key||e.paths.value)&&(e.scrollToSlide(0,e.paths.value,t.params.runCallbacksOnInit),t.params.history.replaceState||d.addEventListener("popstate",t.history.setHistoryPopState))},destroy(){const t=this;t.params.history.replaceState||d.removeEventListener("popstate",t.history.setHistoryPopState)},setHistoryPopState(){const t=this;t.history.paths=ct.getPathValues(),t.history.scrollToSlide(t.params.speed,t.history.paths.value,!1)},getPathValues(){const t=d.location.pathname.slice(1).split("/").filter((t=>""!==t)),e=t.length;return{key:t[e-2],value:t[e-1]}},setHistory(t,e){const n=this;if(!n.history.initialized||!n.params.history.enabled)return;const r=n.slides.eq(e);let o=ct.slugify(r.attr("data-history"));d.location.pathname.includes(t)||(o=`${t}/${o}`);const l=d.history.state;l&&l.value===o||(n.params.history.replaceState?d.history.replaceState({value:o},null,o):d.history.pushState({value:o},null,o))},slugify:text=>text.toString().replace(/\s+/g,"-").replace(/[^\w-]+/g,"").replace(/--+/g,"-").replace(/^-+/,"").replace(/-+$/,""),scrollToSlide(t,e,n){const r=this;if(e)for(let i=0,o=r.slides.length;i<o;i+=1){const o=r.slides.eq(i);if(ct.slugify(o.attr("data-history"))===e&&!o.hasClass(r.params.slideDuplicateClass)){const e=o.index();r.slideTo(e,t,n)}}else r.slideTo(0,t,n)}};const pt={onHashCange(){const t=this;t.emit("hashChange");const e=l.location.hash.replace("#","");if(e!==t.slides.eq(t.activeIndex).attr("data-hash")){const n=t.$wrapperEl.children(`.${t.params.slideClass}[data-hash="${e}"]`).index();if(void 0===n)return;t.slideTo(n)}},setHash(){const t=this;if(t.hashNavigation.initialized&&t.params.hashNavigation.enabled)if(t.params.hashNavigation.replaceState&&d.history&&d.history.replaceState)d.history.replaceState(null,null,`#${t.slides.eq(t.activeIndex).attr("data-hash")}`||""),t.emit("hashSet");else{const e=t.slides.eq(t.activeIndex),n=e.attr("data-hash")||e.attr("data-history");l.location.hash=n||"",t.emit("hashSet")}},init(){const t=this;if(!t.params.hashNavigation.enabled||t.params.history&&t.params.history.enabled)return;t.hashNavigation.initialized=!0;const e=l.location.hash.replace("#","");if(e){const n=0;for(let i=0,r=t.slides.length;i<r;i+=1){const r=t.slides.eq(i);if((r.attr("data-hash")||r.attr("data-history"))===e&&!r.hasClass(t.params.slideDuplicateClass)){const e=r.index();t.slideTo(e,n,t.params.runCallbacksOnInit,!0)}}}t.params.hashNavigation.watchState&&h(d).on("hashchange",t.hashNavigation.onHashCange)},destroy(){const t=this;t.params.hashNavigation.watchState&&h(d).off("hashchange",t.hashNavigation.onHashCange)}};const ft={run(){const t=this,e=t.slides.eq(t.activeIndex);let n=t.params.autoplay.delay;e.attr("data-swiper-autoplay")&&(n=e.attr("data-swiper-autoplay")||t.params.autoplay.delay),clearTimeout(t.autoplay.timeout),t.autoplay.timeout=y.nextTick((()=>{t.params.autoplay.reverseDirection?t.params.loop?(t.loopFix(),t.slidePrev(t.params.speed,!0,!0),t.emit("autoplay")):t.isBeginning?t.params.autoplay.stopOnLastSlide?t.autoplay.stop():(t.slideTo(t.slides.length-1,t.params.speed,!0,!0),t.emit("autoplay")):(t.slidePrev(t.params.speed,!0,!0),t.emit("autoplay")):t.params.loop?(t.loopFix(),t.slideNext(t.params.speed,!0,!0),t.emit("autoplay")):t.isEnd?t.params.autoplay.stopOnLastSlide?t.autoplay.stop():(t.slideTo(0,t.params.speed,!0,!0),t.emit("autoplay")):(t.slideNext(t.params.speed,!0,!0),t.emit("autoplay")),t.params.cssMode&&t.autoplay.running&&t.autoplay.run()}),n)},start(){const t=this;return void 0===t.autoplay.timeout&&(!t.autoplay.running&&(t.autoplay.running=!0,t.emit("autoplayStart"),t.autoplay.run(),!0))},stop(){const t=this;return!!t.autoplay.running&&(void 0!==t.autoplay.timeout&&(t.autoplay.timeout&&(clearTimeout(t.autoplay.timeout),t.autoplay.timeout=void 0),t.autoplay.running=!1,t.emit("autoplayStop"),!0))},pause(t){const e=this;e.autoplay.running&&(e.autoplay.paused||(e.autoplay.timeout&&clearTimeout(e.autoplay.timeout),e.autoplay.paused=!0,0!==t&&e.params.autoplay.waitForTransition?(e.$wrapperEl[0].addEventListener("transitionend",e.autoplay.onTransitionEnd),e.$wrapperEl[0].addEventListener("webkitTransitionEnd",e.autoplay.onTransitionEnd)):(e.autoplay.paused=!1,e.autoplay.run())))}};const ht={setTranslate(){const t=this,{slides:e}=t;for(let i=0;i<e.length;i+=1){const e=t.slides.eq(i);let n=-e[0].swiperSlideOffset;t.params.virtualTranslate||(n-=t.translate);let r=0;t.isHorizontal()||(r=n,n=0);const o=t.params.fadeEffect.crossFade?Math.max(1-Math.abs(e[0].progress),0):1+Math.min(Math.max(e[0].progress,-1),0);e.css({opacity:o}).transform(`translate3d(${n}px, ${r}px, 0px)`)}},setTransition(t){const e=this,{slides:n,$wrapperEl:r}=e;if(n.transition(t),e.params.virtualTranslate&&0!==t){let t=!1;n.transitionEnd((()=>{if(t)return;if(!e||e.destroyed)return;t=!0,e.animating=!1;const n=["webkitTransitionEnd","transitionend"];for(let i=0;i<n.length;i+=1)r.trigger(n[i])}))}}};const vt={setTranslate(){const t=this,{$el:e,$wrapperEl:n,slides:r,width:o,height:l,rtlTranslate:c,size:d}=t,f=t.params.cubeEffect,v=t.isHorizontal(),m=t.virtual&&t.params.virtual.enabled;let y,_=0;f.shadow&&(v?(y=n.find(".swiper-cube-shadow"),0===y.length&&(y=h('<div class="swiper-cube-shadow"></div>'),n.append(y)),y.css({height:`${o}px`})):(y=e.find(".swiper-cube-shadow"),0===y.length&&(y=h('<div class="swiper-cube-shadow"></div>'),e.append(y))));for(let i=0;i<r.length;i+=1){const t=r.eq(i);let e=i;m&&(e=parseInt(t.attr("data-swiper-slide-index"),10));let n=90*e,o=Math.floor(n/360);c&&(n=-n,o=Math.floor(-n/360));const progress=Math.max(Math.min(t[0].progress,1),-1);let l=0,y=0,w=0;e%4==0?(l=4*-o*d,w=0):(e-1)%4==0?(l=0,w=4*-o*d):(e-2)%4==0?(l=d+4*o*d,w=d):(e-3)%4==0&&(l=-d,w=3*d+4*d*o),c&&(l=-l),v||(y=l,l=0);const x=`rotateX(${v?0:-n}deg) rotateY(${v?n:0}deg) translate3d(${l}px, ${y}px, ${w}px)`;if(progress<=1&&progress>-1&&(_=90*e+90*progress,c&&(_=90*-e-90*progress)),t.transform(x),f.slideShadows){let e=v?t.find(".swiper-slide-shadow-left"):t.find(".swiper-slide-shadow-top"),n=v?t.find(".swiper-slide-shadow-right"):t.find(".swiper-slide-shadow-bottom");0===e.length&&(e=h(`<div class="swiper-slide-shadow-${v?"left":"top"}"></div>`),t.append(e)),0===n.length&&(n=h(`<div class="swiper-slide-shadow-${v?"right":"bottom"}"></div>`),t.append(n)),e.length&&(e[0].style.opacity=Math.max(-progress,0)),n.length&&(n[0].style.opacity=Math.max(progress,0))}}if(n.css({"-webkit-transform-origin":`50% 50% -${d/2}px`,"-moz-transform-origin":`50% 50% -${d/2}px`,"-ms-transform-origin":`50% 50% -${d/2}px`,"transform-origin":`50% 50% -${d/2}px`}),f.shadow)if(v)y.transform(`translate3d(0px, ${o/2+f.shadowOffset}px, ${-o/2}px) rotateX(90deg) rotateZ(0deg) scale(${f.shadowScale})`);else{const t=Math.abs(_)-90*Math.floor(Math.abs(_)/90),e=1.5-(Math.sin(2*t*Math.PI/360)/2+Math.cos(2*t*Math.PI/360)/2),n=f.shadowScale,r=f.shadowScale/e,o=f.shadowOffset;y.transform(`scale3d(${n}, 1, ${r}) translate3d(0px, ${l/2+o}px, ${-l/2/r}px) rotateX(-90deg)`)}const w=W.isSafari||W.isWebView?-d/2:0;n.transform(`translate3d(0px,0,${w}px) rotateX(${t.isHorizontal()?0:_}deg) rotateY(${t.isHorizontal()?-_:0}deg)`)},setTransition(t){const e=this,{$el:n,slides:r}=e;r.transition(t).find(".swiper-slide-shadow-top, .swiper-slide-shadow-right, .swiper-slide-shadow-bottom, .swiper-slide-shadow-left").transition(t),e.params.cubeEffect.shadow&&!e.isHorizontal()&&n.find(".swiper-cube-shadow").transition(t)}};const mt={setTranslate(){const t=this,{slides:e,rtlTranslate:n}=t;for(let i=0;i<e.length;i+=1){const r=e.eq(i);let progress=r[0].progress;t.params.flipEffect.limitRotation&&(progress=Math.max(Math.min(r[0].progress,1),-1));let o=-180*progress,l=0,c=-r[0].swiperSlideOffset,d=0;if(t.isHorizontal()?n&&(o=-o):(d=c,c=0,l=-o,o=0),r[0].style.zIndex=-Math.abs(Math.round(progress))+e.length,t.params.flipEffect.slideShadows){let e=t.isHorizontal()?r.find(".swiper-slide-shadow-left"):r.find(".swiper-slide-shadow-top"),n=t.isHorizontal()?r.find(".swiper-slide-shadow-right"):r.find(".swiper-slide-shadow-bottom");0===e.length&&(e=h(`<div class="swiper-slide-shadow-${t.isHorizontal()?"left":"top"}"></div>`),r.append(e)),0===n.length&&(n=h(`<div class="swiper-slide-shadow-${t.isHorizontal()?"right":"bottom"}"></div>`),r.append(n)),e.length&&(e[0].style.opacity=Math.max(-progress,0)),n.length&&(n[0].style.opacity=Math.max(progress,0))}r.transform(`translate3d(${c}px, ${d}px, 0px) rotateX(${l}deg) rotateY(${o}deg)`)}},setTransition(t){const e=this,{slides:n,activeIndex:r,$wrapperEl:o}=e;if(n.transition(t).find(".swiper-slide-shadow-top, .swiper-slide-shadow-right, .swiper-slide-shadow-bottom, .swiper-slide-shadow-left").transition(t),e.params.virtualTranslate&&0!==t){let t=!1;n.eq(r).transitionEnd((function(){if(t)return;if(!e||e.destroyed)return;t=!0,e.animating=!1;const n=["webkitTransitionEnd","transitionend"];for(let i=0;i<n.length;i+=1)o.trigger(n[i])}))}}};const gt={setTranslate(){const t=this,{width:e,height:n,slides:r,$wrapperEl:o,slidesSizesGrid:l}=t,c=t.params.coverflowEffect,d=t.isHorizontal(),f=t.translate,v=d?e/2-f:n/2-f,m=d?c.rotate:-c.rotate,y=c.depth;for(let i=0,t=r.length;i<t;i+=1){const t=r.eq(i),e=l[i],n=(v-t[0].swiperSlideOffset-e/2)/e*c.modifier;let o=d?m*n:0,f=d?0:m*n,_=-y*Math.abs(n),w=c.stretch;"string"==typeof w&&-1!==w.indexOf("%")&&(w=parseFloat(c.stretch)/100*e);let x=d?0:w*n,S=d?w*n:0,E=1-(1-c.scale)*Math.abs(n);Math.abs(S)<.001&&(S=0),Math.abs(x)<.001&&(x=0),Math.abs(_)<.001&&(_=0),Math.abs(o)<.001&&(o=0),Math.abs(f)<.001&&(f=0),Math.abs(E)<.001&&(E=0);const O=`translate3d(${S}px,${x}px,${_}px)  rotateX(${f}deg) rotateY(${o}deg) scale(${E})`;if(t.transform(O),t[0].style.zIndex=1-Math.abs(Math.round(n)),c.slideShadows){let e=d?t.find(".swiper-slide-shadow-left"):t.find(".swiper-slide-shadow-top"),r=d?t.find(".swiper-slide-shadow-right"):t.find(".swiper-slide-shadow-bottom");0===e.length&&(e=h(`<div class="swiper-slide-shadow-${d?"left":"top"}"></div>`),t.append(e)),0===r.length&&(r=h(`<div class="swiper-slide-shadow-${d?"right":"bottom"}"></div>`),t.append(r)),e.length&&(e[0].style.opacity=n>0?n:0),r.length&&(r[0].style.opacity=-n>0?-n:0)}}if(_.pointerEvents||_.prefixedPointerEvents){o[0].style.perspectiveOrigin=`${v}px 50%`}},setTransition(t){this.slides.transition(t).find(".swiper-slide-shadow-top, .swiper-slide-shadow-right, .swiper-slide-shadow-bottom, .swiper-slide-shadow-left").transition(t)}};const yt={init(){const t=this,{thumbs:e}=t.params,n=t.constructor;e.swiper instanceof n?(t.thumbs.swiper=e.swiper,y.extend(t.thumbs.swiper.originalParams,{watchSlidesProgress:!0,slideToClickedSlide:!1}),y.extend(t.thumbs.swiper.params,{watchSlidesProgress:!0,slideToClickedSlide:!1})):y.isObject(e.swiper)&&(t.thumbs.swiper=new n(y.extend({},e.swiper,{watchSlidesVisibility:!0,watchSlidesProgress:!0,slideToClickedSlide:!1})),t.thumbs.swiperCreated=!0),t.thumbs.swiper.$el.addClass(t.params.thumbs.thumbsContainerClass),t.thumbs.swiper.on("tap",t.thumbs.onThumbClick)},onThumbClick(){const t=this,e=t.thumbs.swiper;if(!e)return;const n=e.clickedIndex,r=e.clickedSlide;if(r&&h(r).hasClass(t.params.thumbs.slideThumbActiveClass))return;if(null==n)return;let o;if(o=e.params.loop?parseInt(h(e.clickedSlide).attr("data-swiper-slide-index"),10):n,t.params.loop){let e=t.activeIndex;t.slides.eq(e).hasClass(t.params.slideDuplicateClass)&&(t.loopFix(),t._clientLeft=t.$wrapperEl[0].clientLeft,e=t.activeIndex);const n=t.slides.eq(e).prevAll(`[data-swiper-slide-index="${o}"]`).eq(0).index(),r=t.slides.eq(e).nextAll(`[data-swiper-slide-index="${o}"]`).eq(0).index();o=void 0===n?r:void 0===r?n:r-e<e-n?r:n}t.slideTo(o)},update(t){const e=this,n=e.thumbs.swiper;if(!n)return;const r="auto"===n.params.slidesPerView?n.slidesPerViewDynamic():n.params.slidesPerView,o=e.params.thumbs.autoScrollOffset,l=o&&!n.params.loop;if(e.realIndex!==n.realIndex||l){let c,d,f=n.activeIndex;if(n.params.loop){n.slides.eq(f).hasClass(n.params.slideDuplicateClass)&&(n.loopFix(),n._clientLeft=n.$wrapperEl[0].clientLeft,f=n.activeIndex);const t=n.slides.eq(f).prevAll(`[data-swiper-slide-index="${e.realIndex}"]`).eq(0).index(),r=n.slides.eq(f).nextAll(`[data-swiper-slide-index="${e.realIndex}"]`).eq(0).index();c=void 0===t?r:void 0===r?t:r-f==f-t?f:r-f<f-t?r:t,d=e.activeIndex>e.previousIndex?"next":"prev"}else c=e.realIndex,d=c>e.previousIndex?"next":"prev";l&&(c+="next"===d?o:-1*o),n.visibleSlidesIndexes&&n.visibleSlidesIndexes.indexOf(c)<0&&(n.params.centeredSlides?c=c>f?c-Math.floor(r/2)+1:c+Math.floor(r/2)-1:c>f&&(c=c-r+1),n.slideTo(c,t?0:void 0))}let c=1;const d=e.params.thumbs.slideThumbActiveClass;if(e.params.slidesPerView>1&&!e.params.centeredSlides&&(c=e.params.slidesPerView),e.params.thumbs.multipleActiveThumbs||(c=1),c=Math.floor(c),n.slides.removeClass(d),n.params.loop||n.params.virtual&&n.params.virtual.enabled)for(let i=0;i<c;i+=1)n.$wrapperEl.children(`[data-swiper-slide-index="${e.realIndex+i}"]`).addClass(d);else for(let i=0;i<c;i+=1)n.slides.eq(e.realIndex+i).addClass(d)}};const bt=[H,U,V,Y,G,Z,Q,{name:"mousewheel",params:{mousewheel:{enabled:!1,releaseOnEdges:!1,invert:!1,forceToAxis:!1,sensitivity:1,eventsTarged:"container"}},create(){const t=this;y.extend(t,{mousewheel:{enabled:!1,enable:tt.enable.bind(t),disable:tt.disable.bind(t),handle:tt.handle.bind(t),handleMouseEnter:tt.handleMouseEnter.bind(t),handleMouseLeave:tt.handleMouseLeave.bind(t),animateSlider:tt.animateSlider.bind(t),releaseScroll:tt.releaseScroll.bind(t),lastScrollTime:y.now(),lastEventBeforeSnap:void 0,recentWheelEvents:[]}})},on:{init(){const t=this;!t.params.mousewheel.enabled&&t.params.cssMode&&t.mousewheel.disable(),t.params.mousewheel.enabled&&t.mousewheel.enable()},destroy(){const t=this;t.params.cssMode&&t.mousewheel.enable(),t.mousewheel.enabled&&t.mousewheel.disable()}}},{name:"navigation",params:{navigation:{nextEl:null,prevEl:null,hideOnClick:!1,disabledClass:"swiper-button-disabled",hiddenClass:"swiper-button-hidden",lockClass:"swiper-button-lock"}},create(){const t=this;y.extend(t,{navigation:{init:et.init.bind(t),update:et.update.bind(t),destroy:et.destroy.bind(t),onNextClick:et.onNextClick.bind(t),onPrevClick:et.onPrevClick.bind(t)}})},on:{init(){this.navigation.init(),this.navigation.update()},toEdge(){this.navigation.update()},fromEdge(){this.navigation.update()},destroy(){this.navigation.destroy()},click(t){const e=this,{$nextEl:n,$prevEl:r}=e.navigation;if(e.params.navigation.hideOnClick&&!h(t.target).is(r)&&!h(t.target).is(n)){let t;n?t=n.hasClass(e.params.navigation.hiddenClass):r&&(t=r.hasClass(e.params.navigation.hiddenClass)),!0===t?e.emit("navigationShow",e):e.emit("navigationHide",e),n&&n.toggleClass(e.params.navigation.hiddenClass),r&&r.toggleClass(e.params.navigation.hiddenClass)}}}},{name:"pagination",params:{pagination:{el:null,bulletElement:"span",clickable:!1,hideOnClick:!1,renderBullet:null,renderProgressbar:null,renderFraction:null,renderCustom:null,progressbarOpposite:!1,type:"bullets",dynamicBullets:!1,dynamicMainBullets:1,formatFractionCurrent:t=>t,formatFractionTotal:t=>t,bulletClass:"swiper-pagination-bullet",bulletActiveClass:"swiper-pagination-bullet-active",modifierClass:"swiper-pagination-",currentClass:"swiper-pagination-current",totalClass:"swiper-pagination-total",hiddenClass:"swiper-pagination-hidden",progressbarFillClass:"swiper-pagination-progressbar-fill",progressbarOppositeClass:"swiper-pagination-progressbar-opposite",clickableClass:"swiper-pagination-clickable",lockClass:"swiper-pagination-lock"}},create(){const t=this;y.extend(t,{pagination:{init:nt.init.bind(t),render:nt.render.bind(t),update:nt.update.bind(t),destroy:nt.destroy.bind(t),dynamicBulletIndex:0}})},on:{init(){const t=this;t.pagination.init(),t.pagination.render(),t.pagination.update()},activeIndexChange(){const t=this;(t.params.loop||void 0===t.snapIndex)&&t.pagination.update()},snapIndexChange(){const t=this;t.params.loop||t.pagination.update()},slidesLengthChange(){const t=this;t.params.loop&&(t.pagination.render(),t.pagination.update())},snapGridLengthChange(){const t=this;t.params.loop||(t.pagination.render(),t.pagination.update())},destroy(){this.pagination.destroy()},click(t){const e=this;if(e.params.pagination.el&&e.params.pagination.hideOnClick&&e.pagination.$el.length>0&&!h(t.target).hasClass(e.params.pagination.bulletClass)){!0===e.pagination.$el.hasClass(e.params.pagination.hiddenClass)?e.emit("paginationShow",e):e.emit("paginationHide",e),e.pagination.$el.toggleClass(e.params.pagination.hiddenClass)}}}},{name:"scrollbar",params:{scrollbar:{el:null,dragSize:"auto",hide:!1,draggable:!1,snapOnRelease:!0,lockClass:"swiper-scrollbar-lock",dragClass:"swiper-scrollbar-drag"}},create(){const t=this;y.extend(t,{scrollbar:{init:it.init.bind(t),destroy:it.destroy.bind(t),updateSize:it.updateSize.bind(t),setTranslate:it.setTranslate.bind(t),setTransition:it.setTransition.bind(t),enableDraggable:it.enableDraggable.bind(t),disableDraggable:it.disableDraggable.bind(t),setDragPosition:it.setDragPosition.bind(t),getPointerPosition:it.getPointerPosition.bind(t),onDragStart:it.onDragStart.bind(t),onDragMove:it.onDragMove.bind(t),onDragEnd:it.onDragEnd.bind(t),isTouched:!1,timeout:null,dragTimeout:null}})},on:{init(){const t=this;t.scrollbar.init(),t.scrollbar.updateSize(),t.scrollbar.setTranslate()},update(){this.scrollbar.updateSize()},resize(){this.scrollbar.updateSize()},observerUpdate(){this.scrollbar.updateSize()},setTranslate(){this.scrollbar.setTranslate()},setTransition(t){this.scrollbar.setTransition(t)},destroy(){this.scrollbar.destroy()}}},{name:"parallax",params:{parallax:{enabled:!1}},create(){const t=this;y.extend(t,{parallax:{setTransform:ot.setTransform.bind(t),setTranslate:ot.setTranslate.bind(t),setTransition:ot.setTransition.bind(t)}})},on:{beforeInit(){const t=this;t.params.parallax.enabled&&(t.params.watchSlidesProgress=!0,t.originalParams.watchSlidesProgress=!0)},init(){this.params.parallax.enabled&&this.parallax.setTranslate()},setTranslate(){this.params.parallax.enabled&&this.parallax.setTranslate()},setTransition(t){this.params.parallax.enabled&&this.parallax.setTransition(t)}}},{name:"zoom",params:{zoom:{enabled:!1,maxRatio:3,minRatio:1,toggle:!0,containerClass:"swiper-zoom-container",zoomedSlideClass:"swiper-slide-zoomed"}},create(){const t=this,e={enabled:!1,scale:1,currentScale:1,isScaling:!1,gesture:{$slideEl:void 0,slideWidth:void 0,slideHeight:void 0,$imageEl:void 0,$imageWrapEl:void 0,maxRatio:3},image:{isTouched:void 0,isMoved:void 0,currentX:void 0,currentY:void 0,minX:void 0,minY:void 0,maxX:void 0,maxY:void 0,width:void 0,height:void 0,startX:void 0,startY:void 0,touchesStart:{},touchesCurrent:{}},velocity:{x:void 0,y:void 0,prevPositionX:void 0,prevPositionY:void 0,prevTime:void 0}};"onGestureStart onGestureChange onGestureEnd onTouchStart onTouchMove onTouchEnd onTransitionEnd toggle enable disable in out".split(" ").forEach((n=>{e[n]=at[n].bind(t)})),y.extend(t,{zoom:e});let n=1;Object.defineProperty(t.zoom,"scale",{get:()=>n,set(e){if(n!==e){const n=t.zoom.gesture.$imageEl?t.zoom.gesture.$imageEl[0]:void 0,r=t.zoom.gesture.$slideEl?t.zoom.gesture.$slideEl[0]:void 0;t.emit("zoomChange",e,n,r)}n=e}})},on:{init(){const t=this;t.params.zoom.enabled&&t.zoom.enable()},destroy(){this.zoom.disable()},touchStart(t){this.zoom.enabled&&this.zoom.onTouchStart(t)},touchEnd(t){this.zoom.enabled&&this.zoom.onTouchEnd(t)},doubleTap(t){const e=this;e.params.zoom.enabled&&e.zoom.enabled&&e.params.zoom.toggle&&e.zoom.toggle(t)},transitionEnd(){const t=this;t.zoom.enabled&&t.params.zoom.enabled&&t.zoom.onTransitionEnd()},slideChange(){const t=this;t.zoom.enabled&&t.params.zoom.enabled&&t.params.cssMode&&t.zoom.onTransitionEnd()}}},{name:"lazy",params:{lazy:{enabled:!1,loadPrevNext:!1,loadPrevNextAmount:1,loadOnTransitionStart:!1,elementClass:"swiper-lazy",loadingClass:"swiper-lazy-loading",loadedClass:"swiper-lazy-loaded",preloaderClass:"swiper-lazy-preloader"}},create(){const t=this;y.extend(t,{lazy:{initialImageLoaded:!1,load:st.load.bind(t),loadInSlide:st.loadInSlide.bind(t)}})},on:{beforeInit(){const t=this;t.params.lazy.enabled&&t.params.preloadImages&&(t.params.preloadImages=!1)},init(){const t=this;t.params.lazy.enabled&&!t.params.loop&&0===t.params.initialSlide&&t.lazy.load()},scroll(){const t=this;t.params.freeMode&&!t.params.freeModeSticky&&t.lazy.load()},resize(){const t=this;t.params.lazy.enabled&&t.lazy.load()},scrollbarDragMove(){const t=this;t.params.lazy.enabled&&t.lazy.load()},transitionStart(){const t=this;t.params.lazy.enabled&&(t.params.lazy.loadOnTransitionStart||!t.params.lazy.loadOnTransitionStart&&!t.lazy.initialImageLoaded)&&t.lazy.load()},transitionEnd(){const t=this;t.params.lazy.enabled&&!t.params.lazy.loadOnTransitionStart&&t.lazy.load()},slideChange(){const t=this;t.params.lazy.enabled&&t.params.cssMode&&t.lazy.load()}}},{name:"controller",params:{controller:{control:void 0,inverse:!1,by:"slide"}},create(){const t=this;y.extend(t,{controller:{control:t.params.controller.control,getInterpolateFunction:lt.getInterpolateFunction.bind(t),setTranslate:lt.setTranslate.bind(t),setTransition:lt.setTransition.bind(t)}})},on:{update(){const t=this;t.controller.control&&t.controller.spline&&(t.controller.spline=void 0,delete t.controller.spline)},resize(){const t=this;t.controller.control&&t.controller.spline&&(t.controller.spline=void 0,delete t.controller.spline)},observerUpdate(){const t=this;t.controller.control&&t.controller.spline&&(t.controller.spline=void 0,delete t.controller.spline)},setTranslate(t,e){this.controller.control&&this.controller.setTranslate(t,e)},setTransition(t,e){this.controller.control&&this.controller.setTransition(t,e)}}},{name:"a11y",params:{a11y:{enabled:!0,notificationClass:"swiper-notification",prevSlideMessage:"Previous slide",nextSlideMessage:"Next slide",firstSlideMessage:"This is the first slide",lastSlideMessage:"This is the last slide",paginationBulletMessage:"Go to slide {{index}}"}},create(){const t=this;y.extend(t,{a11y:{liveRegion:h(`<span class="${t.params.a11y.notificationClass}" aria-live="assertive" aria-atomic="true"></span>`)}}),Object.keys(ut).forEach((e=>{t.a11y[e]=ut[e].bind(t)}))},on:{init(){const t=this;t.params.a11y.enabled&&(t.a11y.init(),t.a11y.updateNavigation())},toEdge(){this.params.a11y.enabled&&this.a11y.updateNavigation()},fromEdge(){this.params.a11y.enabled&&this.a11y.updateNavigation()},paginationUpdate(){this.params.a11y.enabled&&this.a11y.updatePagination()},destroy(){this.params.a11y.enabled&&this.a11y.destroy()}}},{name:"history",params:{history:{enabled:!1,replaceState:!1,key:"slides"}},create(){const t=this;y.extend(t,{history:{init:ct.init.bind(t),setHistory:ct.setHistory.bind(t),setHistoryPopState:ct.setHistoryPopState.bind(t),scrollToSlide:ct.scrollToSlide.bind(t),destroy:ct.destroy.bind(t)}})},on:{init(){const t=this;t.params.history.enabled&&t.history.init()},destroy(){const t=this;t.params.history.enabled&&t.history.destroy()},transitionEnd(){const t=this;t.history.initialized&&t.history.setHistory(t.params.history.key,t.activeIndex)},slideChange(){const t=this;t.history.initialized&&t.params.cssMode&&t.history.setHistory(t.params.history.key,t.activeIndex)}}},{name:"hash-navigation",params:{hashNavigation:{enabled:!1,replaceState:!1,watchState:!1}},create(){const t=this;y.extend(t,{hashNavigation:{initialized:!1,init:pt.init.bind(t),destroy:pt.destroy.bind(t),setHash:pt.setHash.bind(t),onHashCange:pt.onHashCange.bind(t)}})},on:{init(){const t=this;t.params.hashNavigation.enabled&&t.hashNavigation.init()},destroy(){const t=this;t.params.hashNavigation.enabled&&t.hashNavigation.destroy()},transitionEnd(){const t=this;t.hashNavigation.initialized&&t.hashNavigation.setHash()},slideChange(){const t=this;t.hashNavigation.initialized&&t.params.cssMode&&t.hashNavigation.setHash()}}},{name:"autoplay",params:{autoplay:{enabled:!1,delay:3e3,waitForTransition:!0,disableOnInteraction:!0,stopOnLastSlide:!1,reverseDirection:!1}},create(){const t=this;y.extend(t,{autoplay:{running:!1,paused:!1,run:ft.run.bind(t),start:ft.start.bind(t),stop:ft.stop.bind(t),pause:ft.pause.bind(t),onVisibilityChange(){"hidden"===document.visibilityState&&t.autoplay.running&&t.autoplay.pause(),"visible"===document.visibilityState&&t.autoplay.paused&&(t.autoplay.run(),t.autoplay.paused=!1)},onTransitionEnd(e){t&&!t.destroyed&&t.$wrapperEl&&e.target===this&&(t.$wrapperEl[0].removeEventListener("transitionend",t.autoplay.onTransitionEnd),t.$wrapperEl[0].removeEventListener("webkitTransitionEnd",t.autoplay.onTransitionEnd),t.autoplay.paused=!1,t.autoplay.running?t.autoplay.run():t.autoplay.stop())}}})},on:{init(){const t=this;t.params.autoplay.enabled&&(t.autoplay.start(),document.addEventListener("visibilitychange",t.autoplay.onVisibilityChange))},beforeTransitionStart(t,e){const n=this;n.autoplay.running&&(e||!n.params.autoplay.disableOnInteraction?n.autoplay.pause(t):n.autoplay.stop())},sliderFirstMove(){const t=this;t.autoplay.running&&(t.params.autoplay.disableOnInteraction?t.autoplay.stop():t.autoplay.pause())},touchEnd(){const t=this;t.params.cssMode&&t.autoplay.paused&&!t.params.autoplay.disableOnInteraction&&t.autoplay.run()},destroy(){const t=this;t.autoplay.running&&t.autoplay.stop(),document.removeEventListener("visibilitychange",t.autoplay.onVisibilityChange)}}},{name:"effect-fade",params:{fadeEffect:{crossFade:!1}},create(){const t=this;y.extend(t,{fadeEffect:{setTranslate:ht.setTranslate.bind(t),setTransition:ht.setTransition.bind(t)}})},on:{beforeInit(){const t=this;if("fade"!==t.params.effect)return;t.classNames.push(`${t.params.containerModifierClass}fade`);const e={slidesPerView:1,slidesPerColumn:1,slidesPerGroup:1,watchSlidesProgress:!0,spaceBetween:0,virtualTranslate:!0};y.extend(t.params,e),y.extend(t.originalParams,e)},setTranslate(){"fade"===this.params.effect&&this.fadeEffect.setTranslate()},setTransition(t){"fade"===this.params.effect&&this.fadeEffect.setTransition(t)}}},{name:"effect-cube",params:{cubeEffect:{slideShadows:!0,shadow:!0,shadowOffset:20,shadowScale:.94}},create(){const t=this;y.extend(t,{cubeEffect:{setTranslate:vt.setTranslate.bind(t),setTransition:vt.setTransition.bind(t)}})},on:{beforeInit(){const t=this;if("cube"!==t.params.effect)return;t.classNames.push(`${t.params.containerModifierClass}cube`),t.classNames.push(`${t.params.containerModifierClass}3d`);const e={slidesPerView:1,slidesPerColumn:1,slidesPerGroup:1,watchSlidesProgress:!0,resistanceRatio:0,spaceBetween:0,centeredSlides:!1,virtualTranslate:!0};y.extend(t.params,e),y.extend(t.originalParams,e)},setTranslate(){"cube"===this.params.effect&&this.cubeEffect.setTranslate()},setTransition(t){"cube"===this.params.effect&&this.cubeEffect.setTransition(t)}}},{name:"effect-flip",params:{flipEffect:{slideShadows:!0,limitRotation:!0}},create(){const t=this;y.extend(t,{flipEffect:{setTranslate:mt.setTranslate.bind(t),setTransition:mt.setTransition.bind(t)}})},on:{beforeInit(){const t=this;if("flip"!==t.params.effect)return;t.classNames.push(`${t.params.containerModifierClass}flip`),t.classNames.push(`${t.params.containerModifierClass}3d`);const e={slidesPerView:1,slidesPerColumn:1,slidesPerGroup:1,watchSlidesProgress:!0,spaceBetween:0,virtualTranslate:!0};y.extend(t.params,e),y.extend(t.originalParams,e)},setTranslate(){"flip"===this.params.effect&&this.flipEffect.setTranslate()},setTransition(t){"flip"===this.params.effect&&this.flipEffect.setTransition(t)}}},{name:"effect-coverflow",params:{coverflowEffect:{rotate:50,stretch:0,depth:100,scale:1,modifier:1,slideShadows:!0}},create(){const t=this;y.extend(t,{coverflowEffect:{setTranslate:gt.setTranslate.bind(t),setTransition:gt.setTransition.bind(t)}})},on:{beforeInit(){const t=this;"coverflow"===t.params.effect&&(t.classNames.push(`${t.params.containerModifierClass}coverflow`),t.classNames.push(`${t.params.containerModifierClass}3d`),t.params.watchSlidesProgress=!0,t.originalParams.watchSlidesProgress=!0)},setTranslate(){"coverflow"===this.params.effect&&this.coverflowEffect.setTranslate()},setTransition(t){"coverflow"===this.params.effect&&this.coverflowEffect.setTransition(t)}}},{name:"thumbs",params:{thumbs:{swiper:null,multipleActiveThumbs:!0,autoScrollOffset:0,slideThumbActiveClass:"swiper-slide-thumb-active",thumbsContainerClass:"swiper-container-thumbs"}},create(){const t=this;y.extend(t,{thumbs:{swiper:null,init:yt.init.bind(t),update:yt.update.bind(t),onThumbClick:yt.onThumbClick.bind(t)}})},on:{beforeInit(){const t=this,{thumbs:e}=t.params;e&&e.swiper&&(t.thumbs.init(),t.thumbs.update(!0))},slideChange(){this.thumbs.swiper&&this.thumbs.update()},update(){this.thumbs.swiper&&this.thumbs.update()},resize(){this.thumbs.swiper&&this.thumbs.update()},observerUpdate(){this.thumbs.swiper&&this.thumbs.update()},setTransition(t){const e=this.thumbs.swiper;e&&e.setTransition(t)},beforeDestroy(){const t=this.thumbs.swiper;t&&this.thumbs.swiperCreated&&t&&t.destroy()}}}];void 0===F.use&&(F.use=F.Class.use,F.installModule=F.Class.installModule),F.use(bt);e.default=F},function(t,e,n){"use strict";n.d(e,"a",(function(){return d}));var r=n(1),o=n(38),l=/^(?:(\w+):)\/\/(?:(\w+)(?::(\w+))?@)([\w.-]+)(?::(\d+))?\/(.+)/,c="Invalid Dsn",d=function(){function t(t){"string"==typeof t?this._fromString(t):this._fromComponents(t),this._validate()}return t.prototype.toString=function(t){void 0===t&&(t=!1);var e=this,n=e.host,path=e.path,r=e.pass,o=e.port,l=e.projectId;return e.protocol+"://"+e.publicKey+(t&&r?":"+r:"")+"@"+n+(o?":"+o:"")+"/"+(path?path+"/":path)+l},t.prototype._fromString=function(t){var e=l.exec(t);if(!e)throw new o.a(c);var n=Object(r.c)(e.slice(1),6),d=n[0],f=n[1],h=n[2],v=void 0===h?"":h,m=n[3],y=n[4],_=void 0===y?"":y,path="",w=n[5],x=w.split("/");if(x.length>1&&(path=x.slice(0,-1).join("/"),w=x.pop()),w){var S=w.match(/^\d+/);S&&(w=S[0])}this._fromComponents({host:m,pass:v,path:path,projectId:w,port:_,protocol:d,publicKey:f})},t.prototype._fromComponents=function(t){"user"in t&&!("publicKey"in t)&&(t.publicKey=t.user),this.user=t.publicKey||"",this.protocol=t.protocol,this.publicKey=t.publicKey||"",this.pass=t.pass||"",this.host=t.host,this.port=t.port||"",this.path=t.path||"",this.projectId=t.projectId},t.prototype._validate=function(){var t=this;if(["protocol","publicKey","host","projectId"].forEach((function(component){if(!t[component])throw new o.a("Invalid Dsn: "+component+" missing")})),!this.projectId.match(/^\d+$/))throw new o.a("Invalid Dsn: Invalid projectId "+this.projectId);if("http"!==this.protocol&&"https"!==this.protocol)throw new o.a("Invalid Dsn: Invalid protocol "+this.protocol);if(this.port&&isNaN(parseInt(this.port,10)))throw new o.a("Invalid Dsn: Invalid port "+this.port)},t}()},function(t,e,n){"use strict";var r;n.d(e,"a",(function(){return r})),function(t){t.Unknown="unknown",t.Skipped="skipped",t.Success="success",t.RateLimit="rate_limit",t.Invalid="invalid",t.Failed="failed"}(r||(r={})),function(t){t.fromHttpCode=function(code){return code>=200&&code<300?t.Success:429===code?t.RateLimit:code>=400&&code<500?t.Invalid:code>=500?t.Failed:t.Unknown}}(r||(r={}))},,function(t,e,n){"use strict";n.d(e,"a",(function(){return r}));var r=function(){function t(){this.name=t.id}return t.prototype.setupOnce=function(e,n){e((function(e){var r=n().getIntegration(t);if(r){try{if(r._shouldDropEvent(e,r._previousEvent))return null}catch(t){return r._previousEvent=e}return r._previousEvent=e}return e}))},t.prototype._shouldDropEvent=function(t,e){return!!e&&(!!this._isSameMessageEvent(t,e)||!!this._isSameExceptionEvent(t,e))},t.prototype._isSameMessageEvent=function(t,e){var n=t.message,r=e.message;return!(!n&&!r)&&(!(n&&!r||!n&&r)&&(n===r&&(!!this._isSameFingerprint(t,e)&&!!this._isSameStacktrace(t,e))))},t.prototype._getFramesFromEvent=function(t){var e=t.exception;if(e)try{return e.values[0].stacktrace.frames}catch(t){return}else if(t.stacktrace)return t.stacktrace.frames},t.prototype._isSameStacktrace=function(t,e){var n=this._getFramesFromEvent(t),r=this._getFramesFromEvent(e);if(!n&&!r)return!0;if(n&&!r||!n&&r)return!1;if(n=n,(r=r).length!==n.length)return!1;for(var i=0;i<r.length;i++){var o=r[i],l=n[i];if(o.filename!==l.filename||o.lineno!==l.lineno||o.colno!==l.colno||o.function!==l.function)return!1}return!0},t.prototype._getExceptionFromEvent=function(t){return t.exception&&t.exception.values&&t.exception.values[0]},t.prototype._isSameExceptionEvent=function(t,e){var n=this._getExceptionFromEvent(e),r=this._getExceptionFromEvent(t);return!(!n||!r)&&(n.type===r.type&&n.value===r.value&&(!!this._isSameFingerprint(t,e)&&!!this._isSameStacktrace(t,e)))},t.prototype._isSameFingerprint=function(t,e){var n=t.fingerprint,r=e.fingerprint;if(!n&&!r)return!0;if(n&&!r||!n&&r)return!1;n=n,r=r;try{return!(n.join("")!==r.join(""))}catch(t){return!1}},t.id="Dedupe",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return d}));var r=n(1),o=n(5),l=n(14),c=n(12),d=function(){function t(e){void 0===e&&(e={depth:3}),this._options=e,this.name=t.id}return t.prototype.setupOnce=function(e,n){e((function(e,r){var o=n().getIntegration(t);return o?o.enhanceEventWithErrorData(e,r):e}))},t.prototype.enhanceEventWithErrorData=function(t,e){var n;if(!e||!e.originalException||!Object(o.d)(e.originalException))return t;var c=e.originalException.name||e.originalException.constructor.name,d=this._extractErrorData(e.originalException);if(d){var f=Object(r.a)({},t.contexts),h=Object(l.d)(d,this._options.depth);return Object(o.h)(h)&&(f=Object(r.a)(Object(r.a)({},t.contexts),((n={})[c]=Object(r.a)({},h),n))),Object(r.a)(Object(r.a)({},t),{contexts:f})}return t},t.prototype._extractErrorData=function(t){var e,n,l=null;try{var d=["name","message","stack","line","column","fileName","lineNumber","columnNumber"],f=Object.getOwnPropertyNames(t).filter((function(t){return-1===d.indexOf(t)}));if(f.length){var h={};try{for(var v=Object(r.f)(f),m=v.next();!m.done;m=v.next()){var y=m.value,_=t[y];Object(o.d)(_)&&(_=_.toString()),h[y]=_}}catch(t){e={error:t}}finally{try{m&&!m.done&&(n=v.return)&&n.call(v)}finally{if(e)throw e.error}}l=h}}catch(t){c.a.error("Unable to extract extra data from the Error object:",t)}return l},t.id="ExtraErrorData",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return d}));var r,o=n(1),l=n(69),c=n(6);!function(t){t.Crash="crash",t.Deprecation="deprecation",t.Intervention="intervention"}(r||(r={}));var d=function(){function t(e){void 0===e&&(e={types:[r.Crash,r.Deprecation,r.Intervention]}),this._options=e,this.name=t.id}return t.prototype.setupOnce=function(t,e){Object(l.f)()&&(this._getCurrentHub=e,new(Object(c.e)().ReportingObserver)(this.handler.bind(this),{buffered:!0,types:this._options.types}).observe())},t.prototype.handler=function(e){var n,l,c=this._getCurrentHub&&this._getCurrentHub();if(c&&c.getIntegration(t)){var d=function(t){c.withScope((function(e){e.setExtra("url",t.url);var label="ReportingObserver ["+t.type+"]",details="No details available";if(t.body){var body,n={};for(var o in t.body)n[o]=t.body[o];if(e.setExtra("body",n),t.type===r.Crash)details=[(body=t.body).crashId||"",body.reason||""].join(" ").trim()||details;else details=(body=t.body).message||details}c.captureMessage(label+": "+details)}))};try{for(var f=Object(o.f)(e),h=f.next();!h.done;h=f.next()){d(h.value)}}catch(t){n={error:t}}finally{try{h&&!h.done&&(l=f.return)&&l.call(f)}finally{if(n)throw n.error}}}},t.id="ReportingObserver",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return l}));var r=n(1),o=n(171),l=function(){function t(e){var n=this;void 0===e&&(e={}),this.name=t.id,this._prefix="app:///",this._iteratee=function(t){if(!t.filename)return t;var e=/^[A-Z]:\\/.test(t.filename),r=/^\//.test(t.filename);if(e||r){var l=e?t.filename.replace(/^[A-Z]:/,"").replace(/\\/g,"/"):t.filename,base=n._root?Object(o.b)(n._root,l):Object(o.a)(l);t.filename=""+n._prefix+base}return t},e.root&&(this._root=e.root),e.prefix&&(this._prefix=e.prefix),e.iteratee&&(this._iteratee=e.iteratee)}return t.prototype.setupOnce=function(e,n){e((function(e){var r=n().getIntegration(t);return r?r.process(e):e}))},t.prototype.process=function(t){var e=t;return t.exception&&Array.isArray(t.exception.values)&&(e=this._processExceptionsEvent(e)),t.stacktrace&&(e=this._processStacktraceEvent(e)),e},t.prototype._processExceptionsEvent=function(t){var e=this;try{return Object(r.a)(Object(r.a)({},t),{exception:Object(r.a)(Object(r.a)({},t.exception),{values:t.exception.values.map((function(t){return Object(r.a)(Object(r.a)({},t),{stacktrace:e._processStacktrace(t.stacktrace)})}))})})}catch(e){return t}},t.prototype._processStacktraceEvent=function(t){try{return Object(r.a)(Object(r.a)({},t),{stacktrace:this._processStacktrace(t.stacktrace)})}catch(e){return t}},t.prototype._processStacktrace=function(t){var e=this;return Object(r.a)(Object(r.a)({},t),{frames:t&&t.frames&&t.frames.map((function(t){return e._iteratee(t)}))})},t.id="RewriteFrames",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return w}));var r=n(1),o=n(172),l=n(12),c=n(6),d=n(171),f={id:"Tracing"},h={id:"BrowserTracing"},v={activate:["activated","deactivated"],create:["beforeCreate","created"],destroy:["beforeDestroy","destroyed"],mount:["beforeMount","mounted"],update:["beforeUpdate","updated"]},m=/(?:^|[-_/])(\w)/g,y="root",_="anonymous component",w=function(){function t(e){var n=this;this.name=t.id,this._componentsCache={},this._applyTracingHooks=function(t,e){if(!t.$options.$_sentryPerfHook){t.$options.$_sentryPerfHook=!0;var c=n._getComponentName(t),d=c===y,h={},m=function(r){var l=Object(o.c)();n._rootSpan?n._finishRootSpan(l,e):t.$once("hook:"+r,(function(){var t=e().getIntegration(f);if(t){n._tracingActivity=t.constructor.pushActivity("Vue Application Render");var r=t.constructor.getTransaction();r&&(n._rootSpan=r.startChild({description:"Application Render",op:"Vue"}))}else{var o=function(t){if(t&&t.getScope){var e=t.getScope();if(e)return e.getTransaction()}return}(e());o&&(n._rootSpan=o.startChild({description:"Application Render",op:"Vue"}))}}))},_=function(r,l){var d=Array.isArray(n._options.tracingOptions.trackComponents)?n._options.tracingOptions.trackComponents.indexOf(c)>-1:n._options.tracingOptions.trackComponents;if(n._rootSpan&&d){var f=Object(o.c)(),span=h[l];span?(span.finish(),n._finishRootSpan(f,e)):t.$once("hook:"+r,(function(){n._rootSpan&&(h[l]=n._rootSpan.startChild({description:"Vue <"+c+">",op:l}))}))}};n._options.tracingOptions.hooks.forEach((function(e){var o=v[e];o?o.forEach((function(o){var l=d?m.bind(n,o):_.bind(n,o,e),c=t.$options[o];Array.isArray(c)?t.$options[o]=Object(r.e)([l],c):t.$options[o]="function"==typeof c?[l,c]:[l]})):l.a.warn("Unknown hook: "+e)}))}},l.a.log("You are still using the Vue.js integration, consider moving to @sentry/vue"),this._options=Object(r.a)(Object(r.a)({Vue:Object(c.e)().Vue,attachProps:!0,logErrors:!1,tracing:!1},e),{tracingOptions:Object(r.a)({hooks:["mount","update"],timeout:2e3,trackComponents:!1},e.tracingOptions)})}return t.prototype.setupOnce=function(t,e){this._options.Vue?(this._attachErrorHandler(e),this._options.tracing&&this._startTracing(e)):l.a.error("Vue integration is missing a Vue instance")},t.prototype._getComponentName=function(t){if(!t)return _;if(t.$root===t)return y;if(!t.$options)return _;if(t.$options.name)return t.$options.name;if(t.$options._componentTag)return t.$options._componentTag;if(t.$options.__file){var e=t.$options.__file.replace(/^[a-zA-Z]:/,"").replace(/\\/g,"/"),n=Object(d.a)(e,".vue");return this._componentsCache[n]||(this._componentsCache[n]=n.replace(m,(function(t,e){return e?e.toUpperCase():""})))}return _},t.prototype._finishRootSpan=function(t,e){var n=this;this._rootSpanTimer&&clearTimeout(this._rootSpanTimer),this._rootSpanTimer=setTimeout((function(){if(n._tracingActivity){var r=e().getIntegration(f);r&&r.constructor.popActivity(n._tracingActivity)}n._rootSpan&&n._rootSpan.finish(t)}),this._options.tracingOptions.timeout)},t.prototype._startTracing=function(t){var e=this._applyTracingHooks;this._options.Vue.mixin({beforeCreate:function(){t().getIntegration(f)||t().getIntegration(h)?e(this,t):l.a.error("Vue integration has tracing enabled, but Tracing integration is not configured")}})},t.prototype._attachErrorHandler=function(e){var n=this,r=this._options.Vue.config.errorHandler;this._options.Vue.config.errorHandler=function(o,c,d){var f={};if(c)try{f.componentName=n._getComponentName(c),n._options.attachProps&&(f.propsData=c.$options.propsData)}catch(t){l.a.warn("Unable to extract metadata from Vue component.")}d&&(f.lifecycleHook=d),e().getIntegration(t)&&setTimeout((function(){e().withScope((function(t){t.setContext("vue",f),e().captureException(o)}))})),"function"==typeof r&&r.call(n._options.Vue,o,c,d),n._options.logErrors&&(n._options.Vue.util&&n._options.Vue.util.warn("Error in "+d+': "'+(o&&o.toString())+'"',c),console.error(o))}},t.id="Vue",t}()},function(t,e,n){"use strict";var r,o;n.d(e,"a",(function(){return r})),function(t){t.Ok="ok",t.Exited="exited",t.Crashed="crashed",t.Abnormal="abnormal"}(r||(r={})),function(t){t.Ok="ok",t.Errored="errored",t.Crashed="crashed"}(o||(o={}))}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class f{constructor(t){const e=this;for(let i=0;i<t.length;i+=1)e[i]=t[i];return e.length=t.length,this}}function h(t,e){const n=[];let i=0;if(t&&!e&&t instanceof f)return t;if(t)if("string"==typeof t){let r,o;const html=t.trim();if(html.indexOf("<")>=0&&html.indexOf(">")>=0){let t="div";for(0===html.indexOf("<li")&&(t="ul"),0===html.indexOf("<tr")&&(t="tbody"),0!==html.indexOf("<td")&&0!==html.indexOf("<th")||(t="tr"),0===html.indexOf("<tbody")&&(t="table"),0===html.indexOf("<option")&&(t="select"),o=l.createElement(t),o.innerHTML=html,i=0;i<o.childNodes.length;i+=1)n.push(o.childNodes[i])}else for(r=e||"#"!==t[0]||t.match(/[ .<>:~]/)?(e||l).querySelectorAll(t.trim()):[l.getElementById(t.trim().split("#")[1])],i=0;i<r.length;i+=1)r[i]&&n.push(r[i])}else if(t.nodeType||t===d||t===l)n.push(t);else if(t.length>0&&t[0].nodeType)for(i=0;i<t.length;i+=1)n.push(t[i]);return new f(n)}function v(t){const e=[];for(let i=0;i<t.length;i+=1)-1===e.indexOf(t[i])&&e.push(t[i]);return e}h.fn=f.prototype,h.Class=f,h.Dom7=f;"resize scroll".split(" ");const m={addClass:function(t){if(void 0===t)return this;const e=t.split(" ");for(let i=0;i<e.length;i+=1)for(let t=0;t<this.length;t+=1)void 0!==this[t]&&void 0!==this[t].classList&&this[t].classList.add(e[i]);return this},removeClass:function(t){const e=t.split(" ");for(let i=0;i<e.length;i+=1)for(let t=0;t<this.length;t+=1)void 0!==this[t]&&void 0!==this[t].classList&&this[t].classList.remove(e[i]);return this},hasClass:function(t){return!!this[0]&&this[0].classList.contains(t)},toggleClass:function(t){const e=t.split(" ");for(let i=0;i<e.length;i+=1)for(let t=0;t<this.length;t+=1)void 0!==this[t]&&void 0!==this[t].classList&&this[t].classList.toggle(e[i]);return this},attr:function(t,e){if(1===arguments.length&&"string"==typeof t)return this[0]?this[0].getAttribute(t):void 0;for(let i=0;i<this.length;i+=1)if(2===arguments.length)this[i].setAttribute(t,e);else for(const e in t)this[i][e]=t[e],this[i].setAttribute(e,t[e]);return this},removeAttr:function(t){for(let i=0;i<this.length;i+=1)this[i].removeAttribute(t);return this},data:function(t,e){let n;if(void 0!==e){for(let i=0;i<this.length;i+=1)n=this[i],n.dom7ElementDataStorage||(n.dom7ElementDataStorage={}),n.dom7ElementDataStorage[t]=e;return this}if(n=this[0],n){if(n.dom7ElementDataStorage&&t in n.dom7ElementDataStorage)return n.dom7ElementDataStorage[t];const e=n.getAttribute(`data-${t}`);return e||void 0}},transform:function(t){for(let i=0;i<this.length;i+=1){const e=this[i].style;e.webkitTransform=t,e.transform=t}return this},transition:function(t){"string"!=typeof t&&(t=`${t}ms`);for(let i=0;i<this.length;i+=1){const e=this[i].style;e.webkitTransitionDuration=t,e.transitionDuration=t}return this},on:function(...t){let[e,n,r,o]=t;function l(t){const e=t.target;if(!e)return;const o=t.target.dom7EventData||[];if(o.indexOf(t)<0&&o.unshift(t),h(e).is(n))r.apply(e,o);else{const t=h(e).parents();for(let e=0;e<t.length;e+=1)h(t[e]).is(n)&&r.apply(t[e],o)}}function c(t){const e=t&&t.target&&t.target.dom7EventData||[];e.indexOf(t)<0&&e.unshift(t),r.apply(this,e)}"function"==typeof t[1]&&([e,r,o]=t,n=void 0),o||(o=!1);const d=e.split(" ");let f;for(let i=0;i<this.length;i+=1){const t=this[i];if(n)for(f=0;f<d.length;f+=1){const e=d[f];t.dom7LiveListeners||(t.dom7LiveListeners={}),t.dom7LiveListeners[e]||(t.dom7LiveListeners[e]=[]),t.dom7LiveListeners[e].push({listener:r,proxyListener:l}),t.addEventListener(e,l,o)}else for(f=0;f<d.length;f+=1){const e=d[f];t.dom7Listeners||(t.dom7Listeners={}),t.dom7Listeners[e]||(t.dom7Listeners[e]=[]),t.dom7Listeners[e].push({listener:r,proxyListener:c}),t.addEventListener(e,c,o)}}return this},off:function(...t){let[e,n,r,o]=t;"function"==typeof t[1]&&([e,r,o]=t,n=void 0),o||(o=!1);const l=e.split(" ");for(let i=0;i<l.length;i+=1){const t=l[i];for(let e=0;e<this.length;e+=1){const l=this[e];let c;if(!n&&l.dom7Listeners?c=l.dom7Listeners[t]:n&&l.dom7LiveListeners&&(c=l.dom7LiveListeners[t]),c&&c.length)for(let e=c.length-1;e>=0;e-=1){const n=c[e];r&&n.listener===r||r&&n.listener&&n.listener.dom7proxy&&n.listener.dom7proxy===r?(l.removeEventListener(t,n.proxyListener,o),c.splice(e,1)):r||(l.removeEventListener(t,n.proxyListener,o),c.splice(e,1))}}}return this},trigger:function(...t){const e=t[0].split(" "),n=t[1];for(let i=0;i<e.length;i+=1){const r=e[i];for(let e=0;e<this.length;e+=1){const o=this[e];let c;try{c=new d.CustomEvent(r,{detail:n,bubbles:!0,cancelable:!0})}catch(t){c=l.createEvent("Event"),c.initEvent(r,!0,!0),c.detail=n}o.dom7EventData=t.filter(((data,t)=>t>0)),o.dispatchEvent(c),o.dom7EventData=[],delete o.dom7EventData}}return this},transitionEnd:function(t){const e=["webkitTransitionEnd","transitionend"],n=this;let i;function r(o){if(o.target===this)for(t.call(this,o),i=0;i<e.length;i+=1)n.off(e[i],r)}if(t)for(i=0;i<e.length;i+=1)n.on(e[i],r);return this},outerWidth:function(t){if(this.length>0){if(t){const t=this.styles();return this[0].offsetWidth+parseFloat(t.getPropertyValue("margin-right"))+parseFloat(t.getPropertyValue("margin-left"))}return this[0].offsetWidth}return null},outerHeight:function(t){if(this.length>0){if(t){const t=this.styles();return this[0].offsetHeight+parseFloat(t.getPropertyValue("margin-top"))+parseFloat(t.getPropertyValue("margin-bottom"))}return this[0].offsetHeight}return null},offset:function(){if(this.length>0){const t=this[0],e=t.getBoundingClientRect(),body=l.body,n=t.clientTop||body.clientTop||0,r=t.clientLeft||body.clientLeft||0,o=t===d?d.scrollY:t.scrollTop,c=t===d?d.scrollX:t.scrollLeft;return{top:e.top+o-n,left:e.left+c-r}}return null},css:function(t,e){let i;if(1===arguments.length){if("string"!=typeof t){for(i=0;i<this.length;i+=1)for(let e in t)this[i].style[e]=t[e];return this}if(this[0])return d.getComputedStyle(this[0],null).getPropertyValue(t)}if(2===arguments.length&&"string"==typeof t){for(i=0;i<this.length;i+=1)this[i].style[t]=e;return this}return this},each:function(t){if(!t)return this;for(let i=0;i<this.length;i+=1)if(!1===t.call(this[i],i,this[i]))return this;return this},html:function(html){if(void 0===html)return this[0]?this[0].innerHTML:void 0;for(let i=0;i<this.length;i+=1)this[i].innerHTML=html;return this},text:function(text){if(void 0===text)return this[0]?this[0].textContent.trim():null;for(let i=0;i<this.length;i+=1)this[i].textContent=text;return this},is:function(t){const e=this[0];let n,i;if(!e||void 0===t)return!1;if("string"==typeof t){if(e.matches)return e.matches(t);if(e.webkitMatchesSelector)return e.webkitMatchesSelector(t);if(e.msMatchesSelector)return e.msMatchesSelector(t);for(n=h(t),i=0;i<n.length;i+=1)if(n[i]===e)return!0;return!1}if(t===l)return e===l;if(t===d)return e===d;if(t.nodeType||t instanceof f){for(n=t.nodeType?[t]:t,i=0;i<n.length;i+=1)if(n[i]===e)return!0;return!1}return!1},index:function(){let i,t=this[0];if(t){for(i=0;null!==(t=t.previousSibling);)1===t.nodeType&&(i+=1);return i}},eq:function(t){if(void 0===t)return this;const e=this.length;let n;return t>e-1?new f([]):t<0?(n=e+t,new f(n<0?[]:[this[n]])):new f([this[t]])},append:function(...t){let e;for(let n=0;n<t.length;n+=1){e=t[n];for(let i=0;i<this.length;i+=1)if("string"==typeof e){const t=l.createElement("div");for(t.innerHTML=e;t.firstChild;)this[i].appendChild(t.firstChild)}else if(e instanceof f)for(let t=0;t<e.length;t+=1)this[i].appendChild(e[t]);else this[i].appendChild(e)}return this},prepend:function(t){let i,e;for(i=0;i<this.length;i+=1)if("string"==typeof t){const n=l.createElement("div");for(n.innerHTML=t,e=n.childNodes.length-1;e>=0;e-=1)this[i].insertBefore(n.childNodes[e],this[i].childNodes[0])}else if(t instanceof f)for(e=0;e<t.length;e+=1)this[i].insertBefore(t[e],this[i].childNodes[0]);else this[i].insertBefore(t,this[i].childNodes[0]);return this},next:function(t){return this.length>0?t?this[0].nextElementSibling&&h(this[0].nextElementSibling).is(t)?new f([this[0].nextElementSibling]):new f([]):this[0].nextElementSibling?new f([this[0].nextElementSibling]):new f([]):new f([])},nextAll:function(t){const e=[];let n=this[0];if(!n)return new f([]);for(;n.nextElementSibling;){const r=n.nextElementSibling;t?h(r).is(t)&&e.push(r):e.push(r),n=r}return new f(e)},prev:function(t){if(this.length>0){const e=this[0];return t?e.previousElementSibling&&h(e.previousElementSibling).is(t)?new f([e.previousElementSibling]):new f([]):e.previousElementSibling?new f([e.previousElementSibling]):new f([])}return new f([])},prevAll:function(t){const e=[];let n=this[0];if(!n)return new f([]);for(;n.previousElementSibling;){const r=n.previousElementSibling;t?h(r).is(t)&&e.push(r):e.push(r),n=r}return new f(e)},parent:function(t){const e=[];for(let i=0;i<this.length;i+=1)null!==this[i].parentNode&&(t?h(this[i].parentNode).is(t)&&e.push(this[i].parentNode):e.push(this[i].parentNode));return h(v(e))},parents:function(t){const e=[];for(let i=0;i<this.length;i+=1){let n=this[i].parentNode;for(;n;)t?h(n).is(t)&&e.push(n):e.push(n),n=n.parentNode}return h(v(e))},closest:function(t){let e=this;return void 0===t?new f([]):(e.is(t)||(e=e.parents(t).eq(0)),e)},find:function(t){const e=[];for(let i=0;i<this.length;i+=1){const n=this[i].querySelectorAll(t);for(let t=0;t<n.length;t+=1)e.push(n[t])}return new f(e)},children:function(t){const e=[];for(let i=0;i<this.length;i+=1){const n=this[i].childNodes;for(let r=0;r<n.length;r+=1)t?1===n[r].nodeType&&h(n[r]).is(t)&&e.push(n[r]):1===n[r].nodeType&&e.push(n[r])}return new f(v(e))},filter:function(t){const e=[],n=this;for(let i=0;i<n.length;i+=1)t.call(n[i],i,n[i])&&e.push(n[i]);return new f(e)},remove:function(){for(let i=0;i<this.length;i+=1)this[i].parentNode&&this[i].parentNode.removeChild(this[i]);return this},add:function(...t){const e=this;let i,n;for(i=0;i<t.length;i+=1){const r=h(t[i]);for(n=0;n<r.length;n+=1)e[e.length]=r[n],e.length+=1}return e},styles:function(){return this[0]?d.getComputedStyle(this[0],null):{}}};Object.keys(m).forEach((t=>{h.fn[t]=h.fn[t]||m[t]}));const y={deleteProps(t){const object=t;Object.keys(object).forEach((t=>{try{object[t]=null}catch(t){}try{delete object[t]}catch(t){}}))},nextTick:(t,e=0)=>setTimeout(t,e),now:()=>Date.now(),getTranslate(t,e="x"){let n,r,o;const l=d.getComputedStyle(t,null);return d.WebKitCSSMatrix?(r=l.transform||l.webkitTransform,r.split(",").length>6&&(r=r.split(", ").map((a=>a.replace(",","."))).join(", ")),o=new d.WebKitCSSMatrix("none"===r?"":r)):(o=l.MozTransform||l.OTransform||l.MsTransform||l.msTransform||l.transform||l.getPropertyValue("transform").replace("translate(","matrix(1, 0, 0, 1,"),n=o.toString().split(",")),"x"===e&&(r=d.WebKitCSSMatrix?o.m41:16===n.length?parseFloat(n[12]):parseFloat(n[4])),"y"===e&&(r=d.WebKitCSSMatrix?o.m42:16===n.length?parseFloat(n[13]):parseFloat(n[5])),r||0},parseUrlQuery(t){const e={};let i,n,param,r,o=t||d.location.href;if("string"==typeof o&&o.length)for(o=o.indexOf("?")>-1?o.replace(/\S*\?/,""):"",n=o.split("&").filter((t=>""!==t)),r=n.length,i=0;i<r;i+=1)param=n[i].replace(/#\S+/g,"").split("="),e[decodeURIComponent(param[0])]=void 0===param[1]?void 0:decodeURIComponent(param[1])||"";return e},isObject:t=>"object"==typeof t&&null!==t&&t.constructor&&t.constructor===Object,extend(...t){const e=Object(t[0]);for(let i=1;i<t.length;i+=1){const n=t[i];if(null!=n){const t=Object.keys(Object(n));for(let r=0,o=t.length;r<o;r+=1){const o=t[r],desc=Object.getOwnPropertyDescriptor(n,o);void 0!==desc&&desc.enumerable&&(y.isObject(e[o])&&y.isObject(n[o])?y.extend(e[o],n[o]):!y.isObject(e[o])&&y.isObject(n[o])?(e[o]={},y.extend(e[o],n[o])):e[o]=n[o])}}}return e}},_={touch:!!("ontouchstart"in d||d.DocumentTouch&&l instanceof d.DocumentTouch),pointerEvents:!!d.PointerEvent&&"maxTouchPoints"in d.navigator&&d.navigator.maxTouchPoints>=0,observer:"MutationObserver"in d||"WebkitMutationObserver"in d,passiveListener:function(){let t=!1;try{const e=Object.defineProperty({},"passive",{get(){t=!0}});d.addEventListener("testPassiveListener",null,e)}catch(t){}return t}(),gestures:"ongesturestart"in d};class w{constructor(t={}){const e=this;e.params=t,e.eventsListeners={},e.params&&e.params.on&&Object.keys(e.params.on).forEach((t=>{e.on(t,e.params.on[t])}))}on(t,e,n){const r=this;if("function"!=typeof e)return r;const o=n?"unshift":"push";return t.split(" ").forEach((t=>{r.eventsListeners[t]||(r.eventsListeners[t]=[]),r.eventsListeners[t][o](e)})),r}once(t,e,n){const r=this;if("function"!=typeof e)return r;function o(...n){r.off(t,o),o.f7proxy&&delete o.f7proxy,e.apply(r,n)}return o.f7proxy=e,r.on(t,o,n)}off(t,e){const n=this;return n.eventsListeners?(t.split(" ").forEach((t=>{void 0===e?n.eventsListeners[t]=[]:n.eventsListeners[t]&&n.eventsListeners[t].length&&n.eventsListeners[t].forEach(((r,o)=>{(r===e||r.f7proxy&&r.f7proxy===e)&&n.eventsListeners[t].splice(o,1)}))})),n):n}emit(...t){const e=this;if(!e.eventsListeners)return e;let n,data,r;"string"==typeof t[0]||Array.isArray(t[0])?(n=t[0],data=t.slice(1,t.length),r=e):(n=t[0].events,data=t[0].data,r=t[0].context||e);return(Array.isArray(n)?n:n.split(" ")).forEach((t=>{if(e.eventsListeners&&e.eventsListeners[t]){const n=[];e.eventsListeners[t].forEach((t=>{n.push(t)})),n.forEach((t=>{t.apply(r,data)}))}})),e}useModulesParams(t){const e=this;e.modules&&Object.keys(e.modules).forEach((n=>{const r=e.modules[n];r.params&&y.extend(t,r.params)}))}useModules(t={}){const e=this;e.modules&&Object.keys(e.modules).forEach((n=>{const r=e.modules[n],o=t[n]||{};r.instance&&Object.keys(r.instance).forEach((t=>{const n=r.instance[t];e[t]="function"==typeof n?n.bind(e):n})),r.on&&e.on&&Object.keys(r.on).forEach((t=>{e.on(t,r.on[t])})),r.create&&r.create.bind(e)(o)}))}static set components(t){this.use&&this.use(t)}static installModule(t,...e){const n=this;n.prototype.modules||(n.prototype.modules={});const r=t.name||`${Object.keys(n.prototype.modules).length}_${y.now()}`;return n.prototype.modules[r]=t,t.proto&&Object.keys(t.proto).forEach((e=>{n.prototype[e]=t.proto[e]})),t.static&&Object.keys(t.static).forEach((e=>{n[e]=t.static[e]})),t.install&&t.install.apply(n,e),n}static use(t,...e){const n=this;return Array.isArray(t)?(t.forEach((t=>n.installModule(t))),n):n.installModule(t,...e)}}var x={updateSize:function(){const t=this;let e,n;const r=t.$el;e=void 0!==t.params.width?t.params.width:r[0].clientWidth,n=void 0!==t.params.height?t.params.height:r[0].clientHeight,0===e&&t.isHorizontal()||0===n&&t.isVertical()||(e=e-parseInt(r.css("padding-left"),10)-parseInt(r.css("padding-right"),10),n=n-parseInt(r.css("padding-top"),10)-parseInt(r.css("padding-bottom"),10),y.extend(t,{width:e,height:n,size:t.isHorizontal()?e:n}))},updateSlides:function(){const t=this,e=t.params,{$wrapperEl:n,size:r,rtlTranslate:o,wrongRTL:l}=t,c=t.virtual&&e.virtual.enabled,f=c?t.virtual.slides.length:t.slides.length,h=n.children(`.${t.params.slideClass}`),v=c?t.virtual.slides.length:h.length;let m=[];const _=[],w=[];function x(t){return!e.cssMode||t!==h.length-1}let S=e.slidesOffsetBefore;"function"==typeof S&&(S=e.slidesOffsetBefore.call(t));let E=e.slidesOffsetAfter;"function"==typeof E&&(E=e.slidesOffsetAfter.call(t));const O=t.snapGrid.length,C=t.snapGrid.length;let T,k,j=e.spaceBetween,$=-S,M=0,A=0;if(void 0===r)return;"string"==typeof j&&j.indexOf("%")>=0&&(j=parseFloat(j.replace("%",""))/100*r),t.virtualSize=-j,o?h.css({marginLeft:"",marginTop:""}):h.css({marginRight:"",marginBottom:""}),e.slidesPerColumn>1&&(T=Math.floor(v/e.slidesPerColumn)===v/t.params.slidesPerColumn?v:Math.ceil(v/e.slidesPerColumn)*e.slidesPerColumn,"auto"!==e.slidesPerView&&"row"===e.slidesPerColumnFill&&(T=Math.max(T,e.slidesPerView*e.slidesPerColumn)));const I=e.slidesPerColumn,P=T/I,D=Math.floor(v/e.slidesPerColumn);for(let i=0;i<v;i+=1){k=0;const n=h.eq(i);if(e.slidesPerColumn>1){let r,o,l;if("row"===e.slidesPerColumnFill&&e.slidesPerGroup>1){const t=Math.floor(i/(e.slidesPerGroup*e.slidesPerColumn)),c=i-e.slidesPerColumn*e.slidesPerGroup*t,d=0===t?e.slidesPerGroup:Math.min(Math.ceil((v-t*I*e.slidesPerGroup)/I),e.slidesPerGroup);l=Math.floor(c/d),o=c-l*d+t*e.slidesPerGroup,r=o+l*T/I,n.css({"-webkit-box-ordinal-group":r,"-moz-box-ordinal-group":r,"-ms-flex-order":r,"-webkit-order":r,order:r})}else"column"===e.slidesPerColumnFill?(o=Math.floor(i/I),l=i-o*I,(o>D||o===D&&l===I-1)&&(l+=1,l>=I&&(l=0,o+=1))):(l=Math.floor(i/P),o=i-l*P);n.css("margin-"+(t.isHorizontal()?"top":"left"),0!==l&&e.spaceBetween&&`${e.spaceBetween}px`)}if("none"!==n.css("display")){if("auto"===e.slidesPerView){const r=d.getComputedStyle(n[0],null),o=n[0].style.transform,l=n[0].style.webkitTransform;if(o&&(n[0].style.transform="none"),l&&(n[0].style.webkitTransform="none"),e.roundLengths)k=t.isHorizontal()?n.outerWidth(!0):n.outerHeight(!0);else if(t.isHorizontal()){const t=parseFloat(r.getPropertyValue("width")),e=parseFloat(r.getPropertyValue("padding-left")),n=parseFloat(r.getPropertyValue("padding-right")),o=parseFloat(r.getPropertyValue("margin-left")),l=parseFloat(r.getPropertyValue("margin-right")),c=r.getPropertyValue("box-sizing");k=c&&"border-box"===c?t+o+l:t+e+n+o+l}else{const t=parseFloat(r.getPropertyValue("height")),e=parseFloat(r.getPropertyValue("padding-top")),n=parseFloat(r.getPropertyValue("padding-bottom")),o=parseFloat(r.getPropertyValue("margin-top")),l=parseFloat(r.getPropertyValue("margin-bottom")),c=r.getPropertyValue("box-sizing");k=c&&"border-box"===c?t+o+l:t+e+n+o+l}o&&(n[0].style.transform=o),l&&(n[0].style.webkitTransform=l),e.roundLengths&&(k=Math.floor(k))}else k=(r-(e.slidesPerView-1)*j)/e.slidesPerView,e.roundLengths&&(k=Math.floor(k)),h[i]&&(t.isHorizontal()?h[i].style.width=`${k}px`:h[i].style.height=`${k}px`);h[i]&&(h[i].swiperSlideSize=k),w.push(k),e.centeredSlides?($=$+k/2+M/2+j,0===M&&0!==i&&($=$-r/2-j),0===i&&($=$-r/2-j),Math.abs($)<.001&&($=0),e.roundLengths&&($=Math.floor($)),A%e.slidesPerGroup==0&&m.push($),_.push($)):(e.roundLengths&&($=Math.floor($)),(A-Math.min(t.params.slidesPerGroupSkip,A))%t.params.slidesPerGroup==0&&m.push($),_.push($),$=$+k+j),t.virtualSize+=k+j,M=k,A+=1}}let L;if(t.virtualSize=Math.max(t.virtualSize,r)+E,o&&l&&("slide"===e.effect||"coverflow"===e.effect)&&n.css({width:`${t.virtualSize+e.spaceBetween}px`}),e.setWrapperSize&&(t.isHorizontal()?n.css({width:`${t.virtualSize+e.spaceBetween}px`}):n.css({height:`${t.virtualSize+e.spaceBetween}px`})),e.slidesPerColumn>1&&(t.virtualSize=(k+e.spaceBetween)*T,t.virtualSize=Math.ceil(t.virtualSize/e.slidesPerColumn)-e.spaceBetween,t.isHorizontal()?n.css({width:`${t.virtualSize+e.spaceBetween}px`}):n.css({height:`${t.virtualSize+e.spaceBetween}px`}),e.centeredSlides)){L=[];for(let i=0;i<m.length;i+=1){let n=m[i];e.roundLengths&&(n=Math.floor(n)),m[i]<t.virtualSize+m[0]&&L.push(n)}m=L}if(!e.centeredSlides){L=[];for(let i=0;i<m.length;i+=1){let n=m[i];e.roundLengths&&(n=Math.floor(n)),m[i]<=t.virtualSize-r&&L.push(n)}m=L,Math.floor(t.virtualSize-r)-Math.floor(m[m.length-1])>1&&m.push(t.virtualSize-r)}if(0===m.length&&(m=[0]),0!==e.spaceBetween&&(t.isHorizontal()?o?h.filter(x).css({marginLeft:`${j}px`}):h.filter(x).css({marginRight:`${j}px`}):h.filter(x).css({marginBottom:`${j}px`})),e.centeredSlides&&e.centeredSlidesBounds){let t=0;w.forEach((n=>{t+=n+(e.spaceBetween?e.spaceBetween:0)})),t-=e.spaceBetween;const n=t-r;m=m.map((t=>t<0?-S:t>n?n+E:t))}if(e.centerInsufficientSlides){let t=0;if(w.forEach((n=>{t+=n+(e.spaceBetween?e.spaceBetween:0)})),t-=e.spaceBetween,t<r){const e=(r-t)/2;m.forEach(((t,n)=>{m[n]=t-e})),_.forEach(((t,n)=>{_[n]=t+e}))}}y.extend(t,{slides:h,snapGrid:m,slidesGrid:_,slidesSizesGrid:w}),v!==f&&t.emit("slidesLengthChange"),m.length!==O&&(t.params.watchOverflow&&t.checkOverflow(),t.emit("snapGridLengthChange")),_.length!==C&&t.emit("slidesGridLengthChange"),(e.watchSlidesProgress||e.watchSlidesVisibility)&&t.updateSlidesOffset()},updateAutoHeight:function(t){const e=this,n=[];let i,r=0;if("number"==typeof t?e.setTransition(t):!0===t&&e.setTransition(e.params.speed),"auto"!==e.params.slidesPerView&&e.params.slidesPerView>1)if(e.params.centeredSlides)e.visibleSlides.each(((t,e)=>{n.push(e)}));else for(i=0;i<Math.ceil(e.params.slidesPerView);i+=1){const t=e.activeIndex+i;if(t>e.slides.length)break;n.push(e.slides.eq(t)[0])}else n.push(e.slides.eq(e.activeIndex)[0]);for(i=0;i<n.length;i+=1)if(void 0!==n[i]){const t=n[i].offsetHeight;r=t>r?t:r}r&&e.$wrapperEl.css("height",`${r}px`)},updateSlidesOffset:function(){const t=this,e=t.slides;for(let i=0;i<e.length;i+=1)e[i].swiperSlideOffset=t.isHorizontal()?e[i].offsetLeft:e[i].offsetTop},updateSlidesProgress:function(t=this&&this.translate||0){const e=this,n=e.params,{slides:r,rtlTranslate:o}=e;if(0===r.length)return;void 0===r[0].swiperSlideOffset&&e.updateSlidesOffset();let l=-t;o&&(l=t),r.removeClass(n.slideVisibleClass),e.visibleSlidesIndexes=[],e.visibleSlides=[];for(let i=0;i<r.length;i+=1){const t=r[i],c=(l+(n.centeredSlides?e.minTranslate():0)-t.swiperSlideOffset)/(t.swiperSlideSize+n.spaceBetween);if(n.watchSlidesVisibility||n.centeredSlides&&n.autoHeight){const o=-(l-t.swiperSlideOffset),c=o+e.slidesSizesGrid[i];(o>=0&&o<e.size-1||c>1&&c<=e.size||o<=0&&c>=e.size)&&(e.visibleSlides.push(t),e.visibleSlidesIndexes.push(i),r.eq(i).addClass(n.slideVisibleClass))}t.progress=o?-c:c}e.visibleSlides=h(e.visibleSlides)},updateProgress:function(t){const e=this;if(void 0===t){const n=e.rtlTranslate?-1:1;t=e&&e.translate&&e.translate*n||0}const n=e.params,r=e.maxTranslate()-e.minTranslate();let{progress:progress,isBeginning:o,isEnd:l}=e;const c=o,d=l;0===r?(progress=0,o=!0,l=!0):(progress=(t-e.minTranslate())/r,o=progress<=0,l=progress>=1),y.extend(e,{progress:progress,isBeginning:o,isEnd:l}),(n.watchSlidesProgress||n.watchSlidesVisibility||n.centeredSlides&&n.autoHeight)&&e.updateSlidesProgress(t),o&&!c&&e.emit("reachBeginning toEdge"),l&&!d&&e.emit("reachEnd toEdge"),(c&&!o||d&&!l)&&e.emit("fromEdge"),e.emit("progress",progress)},updateSlidesClasses:function(){const t=this,{slides:e,params:n,$wrapperEl:r,activeIndex:o,realIndex:l}=t,c=t.virtual&&n.virtual.enabled;let d;e.removeClass(`${n.slideActiveClass} ${n.slideNextClass} ${n.slidePrevClass} ${n.slideDuplicateActiveClass} ${n.slideDuplicateNextClass} ${n.slideDuplicatePrevClass}`),d=c?t.$wrapperEl.find(`.${n.slideClass}[data-swiper-slide-index="${o}"]`):e.eq(o),d.addClass(n.slideActiveClass),n.loop&&(d.hasClass(n.slideDuplicateClass)?r.children(`.${n.slideClass}:not(.${n.slideDuplicateClass})[data-swiper-slide-index="${l}"]`).addClass(n.slideDuplicateActiveClass):r.children(`.${n.slideClass}.${n.slideDuplicateClass}[data-swiper-slide-index="${l}"]`).addClass(n.slideDuplicateActiveClass));let f=d.nextAll(`.${n.slideClass}`).eq(0).addClass(n.slideNextClass);n.loop&&0===f.length&&(f=e.eq(0),f.addClass(n.slideNextClass));let h=d.prevAll(`.${n.slideClass}`).eq(0).addClass(n.slidePrevClass);n.loop&&0===h.length&&(h=e.eq(-1),h.addClass(n.slidePrevClass)),n.loop&&(f.hasClass(n.slideDuplicateClass)?r.children(`.${n.slideClass}:not(.${n.slideDuplicateClass})[data-swiper-slide-index="${f.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicateNextClass):r.children(`.${n.slideClass}.${n.slideDuplicateClass}[data-swiper-slide-index="${f.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicateNextClass),h.hasClass(n.slideDuplicateClass)?r.children(`.${n.slideClass}:not(.${n.slideDuplicateClass})[data-swiper-slide-index="${h.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicatePrevClass):r.children(`.${n.slideClass}.${n.slideDuplicateClass}[data-swiper-slide-index="${h.attr("data-swiper-slide-index")}"]`).addClass(n.slideDuplicatePrevClass))},updateActiveIndex:function(t){const e=this,n=e.rtlTranslate?e.translate:-e.translate,{slidesGrid:r,snapGrid:o,params:l,activeIndex:c,realIndex:d,snapIndex:f}=e;let h,v=t;if(void 0===v){for(let i=0;i<r.length;i+=1)void 0!==r[i+1]?n>=r[i]&&n<r[i+1]-(r[i+1]-r[i])/2?v=i:n>=r[i]&&n<r[i+1]&&(v=i+1):n>=r[i]&&(v=i);l.normalizeSlideIndex&&(v<0||void 0===v)&&(v=0)}if(o.indexOf(n)>=0)h=o.indexOf(n);else{const t=Math.min(l.slidesPerGroupSkip,v);h=t+Math.floor((v-t)/l.slidesPerGroup)}if(h>=o.length&&(h=o.length-1),v===c)return void(h!==f&&(e.snapIndex=h,e.emit("snapIndexChange")));const m=parseInt(e.slides.eq(v).attr("data-swiper-slide-index")||v,10);y.extend(e,{snapIndex:h,realIndex:m,previousIndex:c,activeIndex:v}),e.emit("activeIndexChange"),e.emit("snapIndexChange"),d!==m&&e.emit("realIndexChange"),(e.initialized||e.params.runCallbacksOnInit)&&e.emit("slideChange")},updateClickedSlide:function(t){const e=this,n=e.params,r=h(t.target).closest(`.${n.slideClass}`)[0];let o=!1;if(r)for(let i=0;i<e.slides.length;i+=1)e.slides[i]===r&&(o=!0);if(!r||!o)return e.clickedSlide=void 0,void(e.clickedIndex=void 0);e.clickedSlide=r,e.virtual&&e.params.virtual.enabled?e.clickedIndex=parseInt(h(r).attr("data-swiper-slide-index"),10):e.clickedIndex=h(r).index(),n.slideToClickedSlide&&void 0!==e.clickedIndex&&e.clickedIndex!==e.activeIndex&&e.slideToClickedSlide()}};var S={getTranslate:function(t=(this.isHorizontal()?"x":"y")){const{params:e,rtlTranslate:n,translate:r,$wrapperEl:o}=this;if(e.virtualTranslate)return n?-r:r;if(e.cssMode)return r;let l=y.getTranslate(o[0],t);return n&&(l=-l),l||0},setTranslate:function(t,e){const n=this,{rtlTranslate:r,params:o,$wrapperEl:l,wrapperEl:c,progress:progress}=n;let d,f=0,h=0;n.isHorizontal()?f=r?-t:t:h=t,o.roundLengths&&(f=Math.floor(f),h=Math.floor(h)),o.cssMode?c[n.isHorizontal()?"scrollLeft":"scrollTop"]=n.isHorizontal()?-f:-h:o.virtualTranslate||l.transform(`translate3d(${f}px, ${h}px, 0px)`),n.previousTranslate=n.translate,n.translate=n.isHorizontal()?f:h;const v=n.maxTranslate()-n.minTranslate();d=0===v?0:(t-n.minTranslate())/v,d!==progress&&n.updateProgress(t),n.emit("setTranslate",n.translate,e)},minTranslate:function(){return-this.snapGrid[0]},maxTranslate:function(){return-this.snapGrid[this.snapGrid.length-1]},translateTo:function(t=0,e=this.params.speed,n=!0,r=!0,o){const l=this,{params:c,wrapperEl:d}=l;if(l.animating&&c.preventInteractionOnTransition)return!1;const f=l.minTranslate(),h=l.maxTranslate();let v;if(v=r&&t>f?f:r&&t<h?h:t,l.updateProgress(v),c.cssMode){const t=l.isHorizontal();return 0===e?d[t?"scrollLeft":"scrollTop"]=-v:d.scrollTo?d.scrollTo({[t?"left":"top"]:-v,behavior:"smooth"}):d[t?"scrollLeft":"scrollTop"]=-v,!0}return 0===e?(l.setTransition(0),l.setTranslate(v),n&&(l.emit("beforeTransitionStart",e,o),l.emit("transitionEnd"))):(l.setTransition(e),l.setTranslate(v),n&&(l.emit("beforeTransitionStart",e,o),l.emit("transitionStart")),l.animating||(l.animating=!0,l.onTranslateToWrapperTransitionEnd||(l.onTranslateToWrapperTransitionEnd=function(t){l&&!l.destroyed&&t.target===this&&(l.$wrapperEl[0].removeEventListener("transitionend",l.onTranslateToWrapperTransitionEnd),l.$wrapperEl[0].removeEventListener("webkitTransitionEnd",l.onTranslateToWrapperTransitionEnd),l.onTranslateToWrapperTransitionEnd=null,delete l.onTranslateToWrapperTransitionEnd,n&&l.emit("transitionEnd"))}),l.$wrapperEl[0].addEventListener("transitionend",l.onTranslateToWrapperTransitionEnd),l.$wrapperEl[0].addEventListener("webkitTransitionEnd",l.onTranslateToWrapperTransitionEnd))),!0}};var E={setTransition:function(t,e){const n=this;n.params.cssMode||n.$wrapperEl.transition(t),n.emit("setTransition",t,e)},transitionStart:function(t=!0,e){const n=this,{activeIndex:r,params:o,previousIndex:l}=n;if(o.cssMode)return;o.autoHeight&&n.updateAutoHeight();let c=e;if(c||(c=r>l?"next":r<l?"prev":"reset"),n.emit("transitionStart"),t&&r!==l){if("reset"===c)return void n.emit("slideResetTransitionStart");n.emit("slideChangeTransitionStart"),"next"===c?n.emit("slideNextTransitionStart"):n.emit("slidePrevTransitionStart")}},transitionEnd:function(t=!0,e){const n=this,{activeIndex:r,previousIndex:o,params:l}=n;if(n.animating=!1,l.cssMode)return;n.setTransition(0);let c=e;if(c||(c=r>o?"next":r<o?"prev":"reset"),n.emit("transitionEnd"),t&&r!==o){if("reset"===c)return void n.emit("slideResetTransitionEnd");n.emit("slideChangeTransitionEnd"),"next"===c?n.emit("slideNextTransitionEnd"):n.emit("slidePrevTransitionEnd")}}};var O={slideTo:function(t=0,e=this.params.speed,n=!0,r){const o=this;let l=t;l<0&&(l=0);const{params:c,snapGrid:d,slidesGrid:f,previousIndex:h,activeIndex:v,rtlTranslate:m,wrapperEl:y}=o;if(o.animating&&c.preventInteractionOnTransition)return!1;const _=Math.min(o.params.slidesPerGroupSkip,l);let w=_+Math.floor((l-_)/o.params.slidesPerGroup);w>=d.length&&(w=d.length-1),(v||c.initialSlide||0)===(h||0)&&n&&o.emit("beforeSlideChangeStart");const x=-d[w];if(o.updateProgress(x),c.normalizeSlideIndex)for(let i=0;i<f.length;i+=1)-Math.floor(100*x)>=Math.floor(100*f[i])&&(l=i);if(o.initialized&&l!==v){if(!o.allowSlideNext&&x<o.translate&&x<o.minTranslate())return!1;if(!o.allowSlidePrev&&x>o.translate&&x>o.maxTranslate()&&(v||0)!==l)return!1}let S;if(S=l>v?"next":l<v?"prev":"reset",m&&-x===o.translate||!m&&x===o.translate)return o.updateActiveIndex(l),c.autoHeight&&o.updateAutoHeight(),o.updateSlidesClasses(),"slide"!==c.effect&&o.setTranslate(x),"reset"!==S&&(o.transitionStart(n,S),o.transitionEnd(n,S)),!1;if(c.cssMode){const t=o.isHorizontal();let n=-x;return m&&(n=y.scrollWidth-y.offsetWidth-n),0===e?y[t?"scrollLeft":"scrollTop"]=n:y.scrollTo?y.scrollTo({[t?"left":"top"]:n,behavior:"smooth"}):y[t?"scrollLeft":"scrollTop"]=n,!0}return 0===e?(o.setTransition(0),o.setTranslate(x),o.updateActiveIndex(l),o.updateSlidesClasses(),o.emit("beforeTransitionStart",e,r),o.transitionStart(n,S),o.transitionEnd(n,S)):(o.setTransition(e),o.setTranslate(x),o.updateActiveIndex(l),o.updateSlidesClasses(),o.emit("beforeTransitionStart",e,r),o.transitionStart(n,S),o.animating||(o.animating=!0,o.onSlideToWrapperTransitionEnd||(o.onSlideToWrapperTransitionEnd=function(t){o&&!o.destroyed&&t.target===this&&(o.$wrapperEl[0].removeEventListener("transitionend",o.onSlideToWrapperTransitionEnd),o.$wrapperEl[0].removeEventListener("webkitTransitionEnd",o.onSlideToWrapperTransitionEnd),o.onSlideToWrapperTransitionEnd=null,delete o.onSlideToWrapperTransitionEnd,o.transitionEnd(n,S))}),o.$wrapperEl[0].addEventListener("transitionend",o.onSlideToWrapperTransitionEnd),o.$wrapperEl[0].addEventListener("webkitTransitionEnd",o.onSlideToWrapperTransitionEnd))),!0},slideToLoop:function(t=0,e=this.params.speed,n=!0,r){const o=this;let l=t;return o.params.loop&&(l+=o.loopedSlides),o.slideTo(l,e,n,r)},slideNext:function(t=this.params.speed,e=!0,n){const r=this,{params:o,animating:l}=r,c=r.activeIndex<o.slidesPerGroupSkip?1:o.slidesPerGroup;if(o.loop){if(l)return!1;r.loopFix(),r._clientLeft=r.$wrapperEl[0].clientLeft}return r.slideTo(r.activeIndex+c,t,e,n)},slidePrev:function(t=this.params.speed,e=!0,n){const r=this,{params:o,animating:l,snapGrid:c,slidesGrid:d,rtlTranslate:f}=r;if(o.loop){if(l)return!1;r.loopFix(),r._clientLeft=r.$wrapperEl[0].clientLeft}function h(t){return t<0?-Math.floor(Math.abs(t)):Math.floor(t)}const v=h(f?r.translate:-r.translate),m=c.map((t=>h(t)));d.map((t=>h(t))),c[m.indexOf(v)];let y,_=c[m.indexOf(v)-1];return void 0===_&&o.cssMode&&c.forEach((t=>{!_&&v>=t&&(_=t)})),void 0!==_&&(y=d.indexOf(_),y<0&&(y=r.activeIndex-1)),r.slideTo(y,t,e,n)},slideReset:function(t=this.params.speed,e=!0,n){return this.slideTo(this.activeIndex,t,e,n)},slideToClosest:function(t=this.params.speed,e=!0,n,r=.5){const o=this;let l=o.activeIndex;const c=Math.min(o.params.slidesPerGroupSkip,l),d=c+Math.floor((l-c)/o.params.slidesPerGroup),f=o.rtlTranslate?o.translate:-o.translate;if(f>=o.snapGrid[d]){const t=o.snapGrid[d];f-t>(o.snapGrid[d+1]-t)*r&&(l+=o.params.slidesPerGroup)}else{const t=o.snapGrid[d-1];f-t<=(o.snapGrid[d]-t)*r&&(l-=o.params.slidesPerGroup)}return l=Math.max(l,0),l=Math.min(l,o.slidesGrid.length-1),o.slideTo(l,t,e,n)},slideToClickedSlide:function(){const t=this,{params:e,$wrapperEl:n}=t,r="auto"===e.slidesPerView?t.slidesPerViewDynamic():e.slidesPerView;let o,l=t.clickedIndex;if(e.loop){if(t.animating)return;o=parseInt(h(t.clickedSlide).attr("data-swiper-slide-index"),10),e.centeredSlides?l<t.loopedSlides-r/2||l>t.slides.length-t.loopedSlides+r/2?(t.loopFix(),l=n.children(`.${e.slideClass}[data-swiper-slide-index="${o}"]:not(.${e.slideDuplicateClass})`).eq(0).index(),y.nextTick((()=>{t.slideTo(l)}))):t.slideTo(l):l>t.slides.length-r?(t.loopFix(),l=n.children(`.${e.slideClass}[data-swiper-slide-index="${o}"]:not(.${e.slideDuplicateClass})`).eq(0).index(),y.nextTick((()=>{t.slideTo(l)}))):t.slideTo(l)}else t.slideTo(l)}};var C={loopCreate:function(){const t=this,{params:e,$wrapperEl:n}=t;n.children(`.${e.slideClass}.${e.slideDuplicateClass}`).remove();let r=n.children(`.${e.slideClass}`);if(e.loopFillGroupWithBlank){const t=e.slidesPerGroup-r.length%e.slidesPerGroup;if(t!==e.slidesPerGroup){for(let i=0;i<t;i+=1){const t=h(l.createElement("div")).addClass(`${e.slideClass} ${e.slideBlankClass}`);n.append(t)}r=n.children(`.${e.slideClass}`)}}"auto"!==e.slidesPerView||e.loopedSlides||(e.loopedSlides=r.length),t.loopedSlides=Math.ceil(parseFloat(e.loopedSlides||e.slidesPerView,10)),t.loopedSlides+=e.loopAdditionalSlides,t.loopedSlides>r.length&&(t.loopedSlides=r.length);const o=[],c=[];r.each(((e,n)=>{const l=h(n);e<t.loopedSlides&&c.push(n),e<r.length&&e>=r.length-t.loopedSlides&&o.push(n),l.attr("data-swiper-slide-index",e)}));for(let i=0;i<c.length;i+=1)n.append(h(c[i].cloneNode(!0)).addClass(e.slideDuplicateClass));for(let i=o.length-1;i>=0;i-=1)n.prepend(h(o[i].cloneNode(!0)).addClass(e.slideDuplicateClass))},loopFix:function(){const t=this;t.emit("beforeLoopFix");const{activeIndex:e,slides:n,loopedSlides:r,allowSlidePrev:o,allowSlideNext:l,snapGrid:c,rtlTranslate:d}=t;let f;t.allowSlidePrev=!0,t.allowSlideNext=!0;const h=-c[e]-t.getTranslate();if(e<r){f=n.length-3*r+e,f+=r;t.slideTo(f,0,!1,!0)&&0!==h&&t.setTranslate((d?-t.translate:t.translate)-h)}else if(e>=n.length-r){f=-n.length+e+r,f+=r;t.slideTo(f,0,!1,!0)&&0!==h&&t.setTranslate((d?-t.translate:t.translate)-h)}t.allowSlidePrev=o,t.allowSlideNext=l,t.emit("loopFix")},loopDestroy:function(){const{$wrapperEl:t,params:e,slides:n}=this;t.children(`.${e.slideClass}.${e.slideDuplicateClass},.${e.slideClass}.${e.slideBlankClass}`).remove(),n.removeAttr("data-swiper-slide-index")}};var T={setGrabCursor:function(t){const e=this;if(_.touch||!e.params.simulateTouch||e.params.watchOverflow&&e.isLocked||e.params.cssMode)return;const n=e.el;n.style.cursor="move",n.style.cursor=t?"-webkit-grabbing":"-webkit-grab",n.style.cursor=t?"-moz-grabbin":"-moz-grab",n.style.cursor=t?"grabbing":"grab"},unsetGrabCursor:function(){const t=this;_.touch||t.params.watchOverflow&&t.isLocked||t.params.cssMode||(t.el.style.cursor="")}};var k={appendSlide:function(t){const e=this,{$wrapperEl:n,params:r}=e;if(r.loop&&e.loopDestroy(),"object"==typeof t&&"length"in t)for(let i=0;i<t.length;i+=1)t[i]&&n.append(t[i]);else n.append(t);r.loop&&e.loopCreate(),r.observer&&_.observer||e.update()},prependSlide:function(t){const e=this,{params:n,$wrapperEl:r,activeIndex:o}=e;n.loop&&e.loopDestroy();let l=o+1;if("object"==typeof t&&"length"in t){for(let i=0;i<t.length;i+=1)t[i]&&r.prepend(t[i]);l=o+t.length}else r.prepend(t);n.loop&&e.loopCreate(),n.observer&&_.observer||e.update(),e.slideTo(l,0,!1)},addSlide:function(t,e){const n=this,{$wrapperEl:r,params:o,activeIndex:l}=n;let c=l;o.loop&&(c-=n.loopedSlides,n.loopDestroy(),n.slides=r.children(`.${o.slideClass}`));const d=n.slides.length;if(t<=0)return void n.prependSlide(e);if(t>=d)return void n.appendSlide(e);let f=c>t?c+1:c;const h=[];for(let i=d-1;i>=t;i-=1){const t=n.slides.eq(i);t.remove(),h.unshift(t)}if("object"==typeof e&&"length"in e){for(let i=0;i<e.length;i+=1)e[i]&&r.append(e[i]);f=c>t?c+e.length:c}else r.append(e);for(let i=0;i<h.length;i+=1)r.append(h[i]);o.loop&&n.loopCreate(),o.observer&&_.observer||n.update(),o.loop?n.slideTo(f+n.loopedSlides,0,!1):n.slideTo(f,0,!1)},removeSlide:function(t){const e=this,{params:n,$wrapperEl:r,activeIndex:o}=e;let l=o;n.loop&&(l-=e.loopedSlides,e.loopDestroy(),e.slides=r.children(`.${n.slideClass}`));let c,d=l;if("object"==typeof t&&"length"in t){for(let i=0;i<t.length;i+=1)c=t[i],e.slides[c]&&e.slides.eq(c).remove(),c<d&&(d-=1);d=Math.max(d,0)}else c=t,e.slides[c]&&e.slides.eq(c).remove(),c<d&&(d-=1),d=Math.max(d,0);n.loop&&e.loopCreate(),n.observer&&_.observer||e.update(),n.loop?e.slideTo(d+e.loopedSlides,0,!1):e.slideTo(d,0,!1)},removeAllSlides:function(){const t=this,e=[];for(let i=0;i<t.slides.length;i+=1)e.push(i);t.removeSlide(e)}};const j=function(){const t=d.navigator.platform,e=d.navigator.userAgent,n={ios:!1,android:!1,androidChrome:!1,desktop:!1,iphone:!1,ipod:!1,ipad:!1,edge:!1,ie:!1,firefox:!1,macos:!1,windows:!1,cordova:!(!d.cordova&&!d.phonegap),phonegap:!(!d.cordova&&!d.phonegap),electron:!1},r=d.screen.width,o=d.screen.height,l=e.match(/(Android);?[\s\/]+([\d.]+)?/);let c=e.match(/(iPad).*OS\s([\d_]+)/);const f=e.match(/(iPod)(.*OS\s([\d_]+))?/),h=!c&&e.match(/(iPhone\sOS|iOS)\s([\d_]+)/),v=e.indexOf("MSIE ")>=0||e.indexOf("Trident/")>=0,m=e.indexOf("Edge/")>=0,y=e.indexOf("Gecko/")>=0&&e.indexOf("Firefox/")>=0,w="Win32"===t,x=e.toLowerCase().indexOf("electron")>=0;let S="MacIntel"===t;return!c&&S&&_.touch&&(1024===r&&1366===o||834===r&&1194===o||834===r&&1112===o||768===r&&1024===o)&&(c=e.match(/(Version)\/([\d.]+)/),S=!1),n.ie=v,n.edge=m,n.firefox=y,l&&!w&&(n.os="android",n.osVersion=l[2],n.android=!0,n.androidChrome=e.toLowerCase().indexOf("chrome")>=0),(c||h||f)&&(n.os="ios",n.ios=!0),h&&!f&&(n.osVersion=h[2].replace(/_/g,"."),n.iphone=!0),c&&(n.osVersion=c[2].replace(/_/g,"."),n.ipad=!0),f&&(n.osVersion=f[3]?f[3].replace(/_/g,"."):null,n.ipod=!0),n.ios&&n.osVersion&&e.indexOf("Version/")>=0&&"10"===n.osVersion.split(".")[0]&&(n.osVersion=e.toLowerCase().split("version/")[1].split(" ")[0]),n.webView=!(!(h||c||f)||!e.match(/.*AppleWebKit(?!.*Safari)/i)&&!d.navigator.standalone)||d.matchMedia&&d.matchMedia("(display-mode: standalone)").matches,n.webview=n.webView,n.standalone=n.webView,n.desktop=!(n.ios||n.android)||x,n.desktop&&(n.electron=x,n.macos=S,n.windows=w,n.macos&&(n.os="macos"),n.windows&&(n.os="windows")),n.pixelRatio=d.devicePixelRatio||1,n}();function $(t){const e=this,data=e.touchEventsData,{params:n,touches:r}=e;if(e.animating&&n.preventInteractionOnTransition)return;let o=t;o.originalEvent&&(o=o.originalEvent);const c=h(o.target);if("wrapper"===n.touchEventsTarget&&!c.closest(e.wrapperEl).length)return;if(data.isTouchEvent="touchstart"===o.type,!data.isTouchEvent&&"which"in o&&3===o.which)return;if(!data.isTouchEvent&&"button"in o&&o.button>0)return;if(data.isTouched&&data.isMoved)return;if(n.noSwiping&&c.closest(n.noSwipingSelector?n.noSwipingSelector:`.${n.noSwipingClass}`)[0])return void(e.allowClick=!0);if(n.swipeHandler&&!c.closest(n.swipeHandler)[0])return;r.currentX="touchstart"===o.type?o.targetTouches[0].pageX:o.pageX,r.currentY="touchstart"===o.type?o.targetTouches[0].pageY:o.pageY;const f=r.currentX,v=r.currentY,m=n.edgeSwipeDetection||n.iOSEdgeSwipeDetection,_=n.edgeSwipeThreshold||n.iOSEdgeSwipeThreshold;if(!m||!(f<=_||f>=d.screen.width-_)){if(y.extend(data,{isTouched:!0,isMoved:!1,allowTouchCallbacks:!0,isScrolling:void 0,startMoving:void 0}),r.startX=f,r.startY=v,data.touchStartTime=y.now(),e.allowClick=!0,e.updateSize(),e.swipeDirection=void 0,n.threshold>0&&(data.allowThresholdMove=!1),"touchstart"!==o.type){let t=!0;c.is(data.formElements)&&(t=!1),l.activeElement&&h(l.activeElement).is(data.formElements)&&l.activeElement!==c[0]&&l.activeElement.blur();const r=t&&e.allowTouchMove&&n.touchStartPreventDefault;(n.touchStartForcePreventDefault||r)&&o.preventDefault()}e.emit("touchStart",o)}}function M(t){const e=this,data=e.touchEventsData,{params:n,touches:r,rtlTranslate:o}=e;let c=t;if(c.originalEvent&&(c=c.originalEvent),!data.isTouched)return void(data.startMoving&&data.isScrolling&&e.emit("touchMoveOpposite",c));if(data.isTouchEvent&&"touchmove"!==c.type)return;const d="touchmove"===c.type&&c.targetTouches&&(c.targetTouches[0]||c.changedTouches[0]),f="touchmove"===c.type?d.pageX:c.pageX,v="touchmove"===c.type?d.pageY:c.pageY;if(c.preventedByNestedSwiper)return r.startX=f,void(r.startY=v);if(!e.allowTouchMove)return e.allowClick=!1,void(data.isTouched&&(y.extend(r,{startX:f,startY:v,currentX:f,currentY:v}),data.touchStartTime=y.now()));if(data.isTouchEvent&&n.touchReleaseOnEdges&&!n.loop)if(e.isVertical()){if(v<r.startY&&e.translate<=e.maxTranslate()||v>r.startY&&e.translate>=e.minTranslate())return data.isTouched=!1,void(data.isMoved=!1)}else if(f<r.startX&&e.translate<=e.maxTranslate()||f>r.startX&&e.translate>=e.minTranslate())return;if(data.isTouchEvent&&l.activeElement&&c.target===l.activeElement&&h(c.target).is(data.formElements))return data.isMoved=!0,void(e.allowClick=!1);if(data.allowTouchCallbacks&&e.emit("touchMove",c),c.targetTouches&&c.targetTouches.length>1)return;r.currentX=f,r.currentY=v;const m=r.currentX-r.startX,_=r.currentY-r.startY;if(e.params.threshold&&Math.sqrt(m**2+_**2)<e.params.threshold)return;if(void 0===data.isScrolling){let t;e.isHorizontal()&&r.currentY===r.startY||e.isVertical()&&r.currentX===r.startX?data.isScrolling=!1:m*m+_*_>=25&&(t=180*Math.atan2(Math.abs(_),Math.abs(m))/Math.PI,data.isScrolling=e.isHorizontal()?t>n.touchAngle:90-t>n.touchAngle)}if(data.isScrolling&&e.emit("touchMoveOpposite",c),void 0===data.startMoving&&(r.currentX===r.startX&&r.currentY===r.startY||(data.startMoving=!0)),data.isScrolling)return void(data.isTouched=!1);if(!data.startMoving)return;e.allowClick=!1,!n.cssMode&&c.cancelable&&c.preventDefault(),n.touchMoveStopPropagation&&!n.nested&&c.stopPropagation(),data.isMoved||(n.loop&&e.loopFix(),data.startTranslate=e.getTranslate(),e.setTransition(0),e.animating&&e.$wrapperEl.trigger("webkitTransitionEnd transitionend"),data.allowMomentumBounce=!1,!n.grabCursor||!0!==e.allowSlideNext&&!0!==e.allowSlidePrev||e.setGrabCursor(!0),e.emit("sliderFirstMove",c)),e.emit("sliderMove",c),data.isMoved=!0;let w=e.isHorizontal()?m:_;r.diff=w,w*=n.touchRatio,o&&(w=-w),e.swipeDirection=w>0?"prev":"next",data.currentTranslate=w+data.startTranslate;let x=!0,S=n.resistanceRatio;if(n.touchReleaseOnEdges&&(S=0),w>0&&data.currentTranslate>e.minTranslate()?(x=!1,n.resistance&&(data.currentTranslate=e.minTranslate()-1+(-e.minTranslate()+data.startTranslate+w)**S)):w<0&&data.currentTranslate<e.maxTranslate()&&(x=!1,n.resistance&&(data.currentTranslate=e.maxTranslate()+1-(e.maxTranslate()-data.startTranslate-w)**S)),x&&(c.preventedByNestedSwiper=!0),!e.allowSlideNext&&"next"===e.swipeDirection&&data.currentTranslate<data.startTranslate&&(data.currentTranslate=data.startTranslate),!e.allowSlidePrev&&"prev"===e.swipeDirection&&data.currentTranslate>data.startTranslate&&(data.currentTranslate=data.startTranslate),n.threshold>0){if(!(Math.abs(w)>n.threshold||data.allowThresholdMove))return void(data.currentTranslate=data.startTranslate);if(!data.allowThresholdMove)return data.allowThresholdMove=!0,r.startX=r.currentX,r.startY=r.currentY,data.currentTranslate=data.startTranslate,void(r.diff=e.isHorizontal()?r.currentX-r.startX:r.currentY-r.startY)}n.followFinger&&!n.cssMode&&((n.freeMode||n.watchSlidesProgress||n.watchSlidesVisibility)&&(e.updateActiveIndex(),e.updateSlidesClasses()),n.freeMode&&(0===data.velocities.length&&data.velocities.push({position:r[e.isHorizontal()?"startX":"startY"],time:data.touchStartTime}),data.velocities.push({position:r[e.isHorizontal()?"currentX":"currentY"],time:y.now()})),e.updateProgress(data.currentTranslate),e.setTranslate(data.currentTranslate))}function A(t){const e=this,data=e.touchEventsData,{params:n,touches:r,rtlTranslate:o,$wrapperEl:l,slidesGrid:c,snapGrid:d}=e;let f=t;if(f.originalEvent&&(f=f.originalEvent),data.allowTouchCallbacks&&e.emit("touchEnd",f),data.allowTouchCallbacks=!1,!data.isTouched)return data.isMoved&&n.grabCursor&&e.setGrabCursor(!1),data.isMoved=!1,void(data.startMoving=!1);n.grabCursor&&data.isMoved&&data.isTouched&&(!0===e.allowSlideNext||!0===e.allowSlidePrev)&&e.setGrabCursor(!1);const h=y.now(),v=h-data.touchStartTime;if(e.allowClick&&(e.updateClickedSlide(f),e.emit("tap click",f),v<300&&h-data.lastClickTime<300&&e.emit("doubleTap doubleClick",f)),data.lastClickTime=y.now(),y.nextTick((()=>{e.destroyed||(e.allowClick=!0)})),!data.isTouched||!data.isMoved||!e.swipeDirection||0===r.diff||data.currentTranslate===data.startTranslate)return data.isTouched=!1,data.isMoved=!1,void(data.startMoving=!1);let m;if(data.isTouched=!1,data.isMoved=!1,data.startMoving=!1,m=n.followFinger?o?e.translate:-e.translate:-data.currentTranslate,n.cssMode)return;if(n.freeMode){if(m<-e.minTranslate())return void e.slideTo(e.activeIndex);if(m>-e.maxTranslate())return void(e.slides.length<d.length?e.slideTo(d.length-1):e.slideTo(e.slides.length-1));if(n.freeModeMomentum){if(data.velocities.length>1){const t=data.velocities.pop(),r=data.velocities.pop(),o=t.position-r.position,time=t.time-r.time;e.velocity=o/time,e.velocity/=2,Math.abs(e.velocity)<n.freeModeMinimumVelocity&&(e.velocity=0),(time>150||y.now()-t.time>300)&&(e.velocity=0)}else e.velocity=0;e.velocity*=n.freeModeMomentumVelocityRatio,data.velocities.length=0;let t=1e3*n.freeModeMomentumRatio;const r=e.velocity*t;let c=e.translate+r;o&&(c=-c);let f,h=!1;const v=20*Math.abs(e.velocity)*n.freeModeMomentumBounceRatio;let m;if(c<e.maxTranslate())n.freeModeMomentumBounce?(c+e.maxTranslate()<-v&&(c=e.maxTranslate()-v),f=e.maxTranslate(),h=!0,data.allowMomentumBounce=!0):c=e.maxTranslate(),n.loop&&n.centeredSlides&&(m=!0);else if(c>e.minTranslate())n.freeModeMomentumBounce?(c-e.minTranslate()>v&&(c=e.minTranslate()+v),f=e.minTranslate(),h=!0,data.allowMomentumBounce=!0):c=e.minTranslate(),n.loop&&n.centeredSlides&&(m=!0);else if(n.freeModeSticky){let t;for(let e=0;e<d.length;e+=1)if(d[e]>-c){t=e;break}c=Math.abs(d[t]-c)<Math.abs(d[t-1]-c)||"next"===e.swipeDirection?d[t]:d[t-1],c=-c}if(m&&e.once("transitionEnd",(()=>{e.loopFix()})),0!==e.velocity){if(t=o?Math.abs((-c-e.translate)/e.velocity):Math.abs((c-e.translate)/e.velocity),n.freeModeSticky){const r=Math.abs((o?-c:c)-e.translate),l=e.slidesSizesGrid[e.activeIndex];t=r<l?n.speed:r<2*l?1.5*n.speed:2.5*n.speed}}else if(n.freeModeSticky)return void e.slideToClosest();n.freeModeMomentumBounce&&h?(e.updateProgress(f),e.setTransition(t),e.setTranslate(c),e.transitionStart(!0,e.swipeDirection),e.animating=!0,l.transitionEnd((()=>{e&&!e.destroyed&&data.allowMomentumBounce&&(e.emit("momentumBounce"),e.setTransition(n.speed),setTimeout((()=>{e.setTranslate(f),l.transitionEnd((()=>{e&&!e.destroyed&&e.transitionEnd()}))}),0))}))):e.velocity?(e.updateProgress(c),e.setTransition(t),e.setTranslate(c),e.transitionStart(!0,e.swipeDirection),e.animating||(e.animating=!0,l.transitionEnd((()=>{e&&!e.destroyed&&e.transitionEnd()})))):e.updateProgress(c),e.updateActiveIndex(),e.updateSlidesClasses()}else if(n.freeModeSticky)return void e.slideToClosest();return void((!n.freeModeMomentum||v>=n.longSwipesMs)&&(e.updateProgress(),e.updateActiveIndex(),e.updateSlidesClasses()))}let _=0,w=e.slidesSizesGrid[0];for(let i=0;i<c.length;i+=i<n.slidesPerGroupSkip?1:n.slidesPerGroup){const t=i<n.slidesPerGroupSkip-1?1:n.slidesPerGroup;void 0!==c[i+t]?m>=c[i]&&m<c[i+t]&&(_=i,w=c[i+t]-c[i]):m>=c[i]&&(_=i,w=c[c.length-1]-c[c.length-2])}const x=(m-c[_])/w,S=_<n.slidesPerGroupSkip-1?1:n.slidesPerGroup;if(v>n.longSwipesMs){if(!n.longSwipes)return void e.slideTo(e.activeIndex);"next"===e.swipeDirection&&(x>=n.longSwipesRatio?e.slideTo(_+S):e.slideTo(_)),"prev"===e.swipeDirection&&(x>1-n.longSwipesRatio?e.slideTo(_+S):e.slideTo(_))}else{if(!n.shortSwipes)return void e.slideTo(e.activeIndex);e.navigation&&(f.target===e.navigation.nextEl||f.target===e.navigation.prevEl)?f.target===e.navigation.nextEl?e.slideTo(_+S):e.slideTo(_):("next"===e.swipeDirection&&e.slideTo(_+S),"prev"===e.swipeDirection&&e.slideTo(_))}}function I(){const t=this,{params:e,el:n}=t;if(n&&0===n.offsetWidth)return;e.breakpoints&&t.setBreakpoint();const{allowSlideNext:r,allowSlidePrev:o,snapGrid:l}=t;t.allowSlideNext=!0,t.allowSlidePrev=!0,t.updateSize(),t.updateSlides(),t.updateSlidesClasses(),("auto"===e.slidesPerView||e.slidesPerView>1)&&t.isEnd&&!t.isBeginning&&!t.params.centeredSlides?t.slideTo(t.slides.length-1,0,!1,!0):t.slideTo(t.activeIndex,0,!1,!0),t.autoplay&&t.autoplay.running&&t.autoplay.paused&&t.autoplay.run(),t.allowSlidePrev=o,t.allowSlideNext=r,t.params.watchOverflow&&l!==t.snapGrid&&t.checkOverflow()}function P(t){const e=this;e.allowClick||(e.params.preventClicks&&t.preventDefault(),e.params.preventClicksPropagation&&e.animating&&(t.stopPropagation(),t.stopImmediatePropagation()))}function D(){const t=this,{wrapperEl:e,rtlTranslate:n}=t;let r;t.previousTranslate=t.translate,t.isHorizontal()?t.translate=n?e.scrollWidth-e.offsetWidth-e.scrollLeft:-e.scrollLeft:t.translate=-e.scrollTop,-0===t.translate&&(t.translate=0),t.updateActiveIndex(),t.updateSlidesClasses();const o=t.maxTranslate()-t.minTranslate();r=0===o?0:(t.translate-t.minTranslate())/o,r!==t.progress&&t.updateProgress(n?-t.translate:t.translate),t.emit("setTranslate",t.translate,!1)}let L=!1;function z(){}var N={init:!0,direction:"horizontal",touchEventsTarget:"container",initialSlide:0,speed:300,cssMode:!1,updateOnWindowResize:!0,preventInteractionOnTransition:!1,edgeSwipeDetection:!1,edgeSwipeThreshold:20,freeMode:!1,freeModeMomentum:!0,freeModeMomentumRatio:1,freeModeMomentumBounce:!0,freeModeMomentumBounceRatio:1,freeModeMomentumVelocityRatio:1,freeModeSticky:!1,freeModeMinimumVelocity:.02,autoHeight:!1,setWrapperSize:!1,virtualTranslate:!1,effect:"slide",breakpoints:void 0,spaceBetween:0,slidesPerView:1,slidesPerColumn:1,slidesPerColumnFill:"column",slidesPerGroup:1,slidesPerGroupSkip:0,centeredSlides:!1,centeredSlidesBounds:!1,slidesOffsetBefore:0,slidesOffsetAfter:0,normalizeSlideIndex:!0,centerInsufficientSlides:!1,watchOverflow:!1,roundLengths:!1,touchRatio:1,touchAngle:45,simulateTouch:!0,shortSwipes:!0,longSwipes:!0,longSwipesRatio:.5,longSwipesMs:300,followFinger:!0,allowTouchMove:!0,threshold:0,touchMoveStopPropagation:!1,touchStartPreventDefault:!0,touchStartForcePreventDefault:!1,touchReleaseOnEdges:!1,uniqueNavElements:!0,resistance:!0,resistanceRatio:.85,watchSlidesProgress:!1,watchSlidesVisibility:!1,grabCursor:!1,preventClicks:!0,preventClicksPropagation:!0,slideToClickedSlide:!1,preloadImages:!0,updateOnImagesReady:!0,loop:!1,loopAdditionalSlides:0,loopedSlides:null,loopFillGroupWithBlank:!1,allowSlidePrev:!0,allowSlideNext:!0,swipeHandler:null,noSwiping:!0,noSwipingClass:"swiper-no-swiping",noSwipingSelector:null,passiveListeners:!0,containerModifierClass:"swiper-container-",slideClass:"swiper-slide",slideBlankClass:"swiper-slide-invisible-blank",slideActiveClass:"swiper-slide-active",slideDuplicateActiveClass:"swiper-slide-duplicate-active",slideVisibleClass:"swiper-slide-visible",slideDuplicateClass:"swiper-slide-duplicate",slideNextClass:"swiper-slide-next",slideDuplicateNextClass:"swiper-slide-duplicate-next",slidePrevClass:"swiper-slide-prev",slideDuplicatePrevClass:"swiper-slide-duplicate-prev",wrapperClass:"swiper-wrapper",runCallbacksOnInit:!0};const B={update:x,translate:S,transition:E,slide:O,loop:C,grabCursor:T,manipulation:k,events:{attachEvents:function(){const t=this,{params:e,touchEvents:n,el:r,wrapperEl:o}=t;t.onTouchStart=$.bind(t),t.onTouchMove=M.bind(t),t.onTouchEnd=A.bind(t),e.cssMode&&(t.onScroll=D.bind(t)),t.onClick=P.bind(t);const c=!!e.nested;if(!_.touch&&_.pointerEvents)r.addEventListener(n.start,t.onTouchStart,!1),l.addEventListener(n.move,t.onTouchMove,c),l.addEventListener(n.end,t.onTouchEnd,!1);else{if(_.touch){const o=!("touchstart"!==n.start||!_.passiveListener||!e.passiveListeners)&&{passive:!0,capture:!1};r.addEventListener(n.start,t.onTouchStart,o),r.addEventListener(n.move,t.onTouchMove,_.passiveListener?{passive:!1,capture:c}:c),r.addEventListener(n.end,t.onTouchEnd,o),n.cancel&&r.addEventListener(n.cancel,t.onTouchEnd,o),L||(l.addEventListener("touchstart",z),L=!0)}(e.simulateTouch&&!j.ios&&!j.android||e.simulateTouch&&!_.touch&&j.ios)&&(r.addEventListener("mousedown",t.onTouchStart,!1),l.addEventListener("mousemove",t.onTouchMove,c),l.addEventListener("mouseup",t.onTouchEnd,!1))}(e.preventClicks||e.preventClicksPropagation)&&r.addEventListener("click",t.onClick,!0),e.cssMode&&o.addEventListener("scroll",t.onScroll),e.updateOnWindowResize?t.on(j.ios||j.android?"resize orientationchange observerUpdate":"resize observerUpdate",I,!0):t.on("observerUpdate",I,!0)},detachEvents:function(){const t=this,{params:e,touchEvents:n,el:r,wrapperEl:o}=t,c=!!e.nested;if(!_.touch&&_.pointerEvents)r.removeEventListener(n.start,t.onTouchStart,!1),l.removeEventListener(n.move,t.onTouchMove,c),l.removeEventListener(n.end,t.onTouchEnd,!1);else{if(_.touch){const o=!("onTouchStart"!==n.start||!_.passiveListener||!e.passiveListeners)&&{passive:!0,capture:!1};r.removeEventListener(n.start,t.onTouchStart,o),r.removeEventListener(n.move,t.onTouchMove,c),r.removeEventListener(n.end,t.onTouchEnd,o),n.cancel&&r.removeEventListener(n.cancel,t.onTouchEnd,o)}(e.simulateTouch&&!j.ios&&!j.android||e.simulateTouch&&!_.touch&&j.ios)&&(r.removeEventListener("mousedown",t.onTouchStart,!1),l.removeEventListener("mousemove",t.onTouchMove,c),l.removeEventListener("mouseup",t.onTouchEnd,!1))}(e.preventClicks||e.preventClicksPropagation)&&r.removeEventListener("click",t.onClick,!0),e.cssMode&&o.removeEventListener("scroll",t.onScroll),t.off(j.ios||j.android?"resize orientationchange observerUpdate":"resize observerUpdate",I)}},breakpoints:{setBreakpoint:function(){const t=this,{activeIndex:e,initialized:n,loopedSlides:r=0,params:o,$el:l}=t,c=o.breakpoints;if(!c||c&&0===Object.keys(c).length)return;const d=t.getBreakpoint(c);if(d&&t.currentBreakpoint!==d){const f=d in c?c[d]:void 0;f&&["slidesPerView","spaceBetween","slidesPerGroup","slidesPerGroupSkip","slidesPerColumn"].forEach((param=>{const t=f[param];void 0!==t&&(f[param]="slidesPerView"!==param||"AUTO"!==t&&"auto"!==t?"slidesPerView"===param?parseFloat(t):parseInt(t,10):"auto")}));const h=f||t.originalParams,v=o.slidesPerColumn>1,m=h.slidesPerColumn>1;v&&!m?l.removeClass(`${o.containerModifierClass}multirow ${o.containerModifierClass}multirow-column`):!v&&m&&(l.addClass(`${o.containerModifierClass}multirow`),"column"===h.slidesPerColumnFill&&l.addClass(`${o.containerModifierClass}multirow-column`));const _=h.direction&&h.direction!==o.direction,w=o.loop&&(h.slidesPerView!==o.slidesPerView||_);_&&n&&t.changeDirection(),y.extend(t.params,h),y.extend(t,{allowTouchMove:t.params.allowTouchMove,allowSlideNext:t.params.allowSlideNext,allowSlidePrev:t.params.allowSlidePrev}),t.currentBreakpoint=d,w&&n&&(t.loopDestroy(),t.loopCreate(),t.updateSlides(),t.slideTo(e-r+t.loopedSlides,0,!1)),t.emit("breakpoint",h)}},getBreakpoint:function(t){if(!t)return;let e=!1;const n=Object.keys(t).map((t=>{if("string"==typeof t&&0===t.indexOf("@")){const e=parseFloat(t.substr(1));return{value:d.innerHeight*e,point:t}}return{value:t,point:t}}));n.sort(((a,b)=>parseInt(a.value,10)-parseInt(b.value,10)));for(let i=0;i<n.length;i+=1){const{point:t,value:r}=n[i];r<=d.innerWidth&&(e=t)}return e||"max"}},checkOverflow:{checkOverflow:function(){const t=this,e=t.params,n=t.isLocked,r=t.slides.length>0&&e.slidesOffsetBefore+e.spaceBetween*(t.slides.length-1)+t.slides[0].offsetWidth*t.slides.length;e.slidesOffsetBefore&&e.slidesOffsetAfter&&r?t.isLocked=r<=t.size:t.isLocked=1===t.snapGrid.length,t.allowSlideNext=!t.isLocked,t.allowSlidePrev=!t.isLocked,n!==t.isLocked&&t.emit(t.isLocked?"lock":"unlock"),n&&n!==t.isLocked&&(t.isEnd=!1,t.navigation&&t.navigation.update())}},classes:{addClasses:function(){const{classNames:t,params:e,rtl:n,$el:r}=this,o=[];o.push("initialized"),o.push(e.direction),e.freeMode&&o.push("free-mode"),e.autoHeight&&o.push("autoheight"),n&&o.push("rtl"),e.slidesPerColumn>1&&(o.push("multirow"),"column"===e.slidesPerColumnFill&&o.push("multirow-column")),j.android&&o.push("android"),j.ios&&o.push("ios"),e.cssMode&&o.push("css-mode"),o.forEach((n=>{t.push(e.containerModifierClass+n)})),r.addClass(t.join(" "))},removeClasses:function(){const{$el:t,classNames:e}=this;t.removeClass(e.join(" "))}},images:{loadImage:function(t,e,n,r,o,l){let image;function c(){l&&l()}h(t).parent("picture")[0]||t.complete&&o?c():e?(image=new d.Image,image.onload=c,image.onerror=c,r&&(image.sizes=r),n&&(image.srcset=n),e&&(image.src=e)):c()},preloadImages:function(){const t=this;function e(){null!=t&&t&&!t.destroyed&&(void 0!==t.imagesLoaded&&(t.imagesLoaded+=1),t.imagesLoaded===t.imagesToLoad.length&&(t.params.updateOnImagesReady&&t.update(),t.emit("imagesReady")))}t.imagesToLoad=t.$el.find("img");for(let i=0;i<t.imagesToLoad.length;i+=1){const n=t.imagesToLoad[i];t.loadImage(n,n.currentSrc||n.getAttribute("src"),n.srcset||n.getAttribute("srcset"),n.sizes||n.getAttribute("sizes"),!0,e)}}}},R={};class F extends w{constructor(...t){let e,n;1===t.length&&t[0].constructor&&t[0].constructor===Object?n=t[0]:[e,n]=t,n||(n={}),n=y.extend({},n),e&&!n.el&&(n.el=e),super(n),Object.keys(B).forEach((t=>{Object.keys(B[t]).forEach((e=>{F.prototype[e]||(F.prototype[e]=B[t][e])}))}));const r=this;void 0===r.modules&&(r.modules={}),Object.keys(r.modules).forEach((t=>{const e=r.modules[t];if(e.params){const t=Object.keys(e.params)[0],r=e.params[t];if("object"!=typeof r||null===r)return;if(!(t in n)||!("enabled"in r))return;!0===n[t]&&(n[t]={enabled:!0}),"object"!=typeof n[t]||"enabled"in n[t]||(n[t].enabled=!0),n[t]||(n[t]={enabled:!1})}}));const o=y.extend({},N);r.useModulesParams(o),r.params=y.extend({},o,R,n),r.originalParams=y.extend({},r.params),r.passedParams=y.extend({},n),r.$=h;const l=h(r.params.el);if(e=l[0],!e)return;if(l.length>1){const t=[];return l.each(((e,r)=>{const o=y.extend({},n,{el:r});t.push(new F(o))})),t}let c;return e.swiper=r,l.data("swiper",r),e&&e.shadowRoot&&e.shadowRoot.querySelector?(c=h(e.shadowRoot.querySelector(`.${r.params.wrapperClass}`)),c.children=t=>l.children(t)):c=l.children(`.${r.params.wrapperClass}`),y.extend(r,{$el:l,el:e,$wrapperEl:c,wrapperEl:c[0],classNames:[],slides:h(),slidesGrid:[],snapGrid:[],slidesSizesGrid:[],isHorizontal:()=>"horizontal"===r.params.direction,isVertical:()=>"vertical"===r.params.direction,rtl:"rtl"===e.dir.toLowerCase()||"rtl"===l.css("direction"),rtlTranslate:"horizontal"===r.params.direction&&("rtl"===e.dir.toLowerCase()||"rtl"===l.css("direction")),wrongRTL:"-webkit-box"===c.css("display"),activeIndex:0,realIndex:0,isBeginning:!0,isEnd:!1,translate:0,previousTranslate:0,progress:0,velocity:0,animating:!1,allowSlideNext:r.params.allowSlideNext,allowSlidePrev:r.params.allowSlidePrev,touchEvents:function(){const t=["touchstart","touchmove","touchend","touchcancel"];let e=["mousedown","mousemove","mouseup"];return _.pointerEvents&&(e=["pointerdown","pointermove","pointerup"]),r.touchEventsTouch={start:t[0],move:t[1],end:t[2],cancel:t[3]},r.touchEventsDesktop={start:e[0],move:e[1],end:e[2]},_.touch||!r.params.simulateTouch?r.touchEventsTouch:r.touchEventsDesktop}(),touchEventsData:{isTouched:void 0,isMoved:void 0,allowTouchCallbacks:void 0,touchStartTime:void 0,isScrolling:void 0,currentTranslate:void 0,startTranslate:void 0,allowThresholdMove:void 0,formElements:"input, select, option, textarea, button, video, label",lastClickTime:y.now(),clickTimeout:void 0,velocities:[],allowMomentumBounce:void 0,isTouchEvent:void 0,startMoving:void 0},allowClick:!0,allowTouchMove:r.params.allowTouchMove,touches:{startX:0,startY:0,currentX:0,currentY:0,diff:0},imagesToLoad:[],imagesLoaded:0}),r.useModules(),r.params.init&&r.init(),r}slidesPerViewDynamic(){const{params:t,slides:e,slidesGrid:n,size:r,activeIndex:o}=this;let l=1;if(t.centeredSlides){let t,n=e[o].swiperSlideSize;for(let i=o+1;i<e.length;i+=1)e[i]&&!t&&(n+=e[i].swiperSlideSize,l+=1,n>r&&(t=!0));for(let i=o-1;i>=0;i-=1)e[i]&&!t&&(n+=e[i].swiperSlideSize,l+=1,n>r&&(t=!0))}else for(let i=o+1;i<e.length;i+=1)n[i]-n[o]<r&&(l+=1);return l}update(){const t=this;if(!t||t.destroyed)return;const{snapGrid:e,params:n}=t;function r(){const e=t.rtlTranslate?-1*t.translate:t.translate,n=Math.min(Math.max(e,t.maxTranslate()),t.minTranslate());t.setTranslate(n),t.updateActiveIndex(),t.updateSlidesClasses()}let o;n.breakpoints&&t.setBreakpoint(),t.updateSize(),t.updateSlides(),t.updateProgress(),t.updateSlidesClasses(),t.params.freeMode?(r(),t.params.autoHeight&&t.updateAutoHeight()):(o=("auto"===t.params.slidesPerView||t.params.slidesPerView>1)&&t.isEnd&&!t.params.centeredSlides?t.slideTo(t.slides.length-1,0,!1,!0):t.slideTo(t.activeIndex,0,!1,!0),o||r()),n.watchOverflow&&e!==t.snapGrid&&t.checkOverflow(),t.emit("update")}changeDirection(t,e=!0){const n=this,r=n.params.direction;return t||(t="horizontal"===r?"vertical":"horizontal"),t===r||"horizontal"!==t&&"vertical"!==t||(n.$el.removeClass(`${n.params.containerModifierClass}${r}`).addClass(`${n.params.containerModifierClass}${t}`),n.params.direction=t,n.slides.each(((e,n)=>{"vertical"===t?n.style.width="":n.style.height=""})),n.emit("changeDirection"),e&&n.update()),n}init(){const t=this;t.initialized||(t.emit("beforeInit"),t.params.breakpoints&&t.setBreakpoint(),t.addClasses(),t.params.loop&&t.loopCreate(),t.updateSize(),t.updateSlides(),t.params.watchOverflow&&t.checkOverflow(),t.params.grabCursor&&t.setGrabCursor(),t.params.preloadImages&&t.preloadImages(),t.params.loop?t.slideTo(t.params.initialSlide+t.loopedSlides,0,t.params.runCallbacksOnInit):t.slideTo(t.params.initialSlide,0,t.params.runCallbacksOnInit),t.attachEvents(),t.initialized=!0,t.emit("init"))}destroy(t=!0,e=!0){const n=this,{params:r,$el:o,$wrapperEl:l,slides:c}=n;return void 0===n.params||n.destroyed||(n.emit("beforeDestroy"),n.initialized=!1,n.detachEvents(),r.loop&&n.loopDestroy(),e&&(n.removeClasses(),o.removeAttr("style"),l.removeAttr("style"),c&&c.length&&c.removeClass([r.slideVisibleClass,r.slideActiveClass,r.slideNextClass,r.slidePrevClass].join(" ")).removeAttr("style").removeAttr("data-swiper-slide-index")),n.emit("destroy"),Object.keys(n.eventsListeners).forEach((t=>{n.off(t)})),!1!==t&&(n.$el[0].swiper=null,n.$el.data("swiper",null),y.deleteProps(n)),n.destroyed=!0),null}static extendDefaults(t){y.extend(R,t)}static get extendedDefaults(){return R}static get defaults(){return N}static get Class(){return w}static get $(){return h}}var H={name:"device",proto:{device:j},static:{device:j}},U={name:"support",proto:{support:_},static:{support:_}};const W={isEdge:!!d.navigator.userAgent.match(/Edge/g),isSafari:function(){const t=d.navigator.userAgent.toLowerCase();return t.indexOf("safari")>=0&&t.indexOf("chrome")<0&&t.indexOf("android")<0}(),isWebView:/(iPhone|iPod|iPad).*AppleWebKit(?!.*Safari)/i.test(d.navigator.userAgent)};var V={name:"browser",proto:{browser:W},static:{browser:W}},Y={name:"resize",create(){const t=this;y.extend(t,{resize:{resizeHandler(){t&&!t.destroyed&&t.initialized&&(t.emit("beforeResize"),t.emit("resize"))},orientationChangeHandler(){t&&!t.destroyed&&t.initialized&&t.emit("orientationchange")}}})},on:{init(){d.addEventListener("resize",this.resize.resizeHandler),d.addEventListener("orientationchange",this.resize.orientationChangeHandler)},destroy(){d.removeEventListener("resize",this.resize.resizeHandler),d.removeEventListener("orientationchange",this.resize.orientationChangeHandler)}}};const X={func:d.MutationObserver||d.WebkitMutationObserver,attach(t,e={}){const n=this,r=new(0,X.func)((t=>{if(1===t.length)return void n.emit("observerUpdate",t[0]);const e=function(){n.emit("observerUpdate",t[0])};d.requestAnimationFrame?d.requestAnimationFrame(e):d.setTimeout(e,0)}));r.observe(t,{attributes:void 0===e.attributes||e.attributes,childList:void 0===e.childList||e.childList,characterData:void 0===e.characterData||e.characterData}),n.observer.observers.push(r)},init(){const t=this;if(_.observer&&t.params.observer){if(t.params.observeParents){const e=t.$el.parents();for(let i=0;i<e.length;i+=1)t.observer.attach(e[i])}t.observer.attach(t.$el[0],{childList:t.params.observeSlideChildren}),t.observer.attach(t.$wrapperEl[0],{attributes:!1})}},destroy(){this.observer.observers.forEach((t=>{t.disconnect()})),this.observer.observers=[]}};var G={name:"observer",params:{observer:!1,observeParents:!1,observeSlideChildren:!1},create(){const t=this;y.extend(t,{observer:{init:X.init.bind(t),attach:X.attach.bind(t),destroy:X.destroy.bind(t),observers:[]}})},on:{init(){this.observer.init()},destroy(){this.observer.destroy()}}};const J={update(t){const e=this,{slidesPerView:n,slidesPerGroup:r,centeredSlides:o}=e.params,{addSlidesBefore:l,addSlidesAfter:c}=e.params.virtual,{from:d,to:f,slides:h,slidesGrid:v,renderSlide:m,offset:_}=e.virtual;e.updateActiveIndex();const w=e.activeIndex||0;let x,S,E;x=e.rtlTranslate?"right":e.isHorizontal()?"left":"top",o?(S=Math.floor(n/2)+r+l,E=Math.floor(n/2)+r+c):(S=n+(r-1)+l,E=r+c);const O=Math.max((w||0)-E,0),C=Math.min((w||0)+S,h.length-1),T=(e.slidesGrid[O]||0)-(e.slidesGrid[0]||0);function k(){e.updateSlides(),e.updateProgress(),e.updateSlidesClasses(),e.lazy&&e.params.lazy.enabled&&e.lazy.load()}if(y.extend(e.virtual,{from:O,to:C,offset:T,slidesGrid:e.slidesGrid}),d===O&&f===C&&!t)return e.slidesGrid!==v&&T!==_&&e.slides.css(x,`${T}px`),void e.updateProgress();if(e.params.virtual.renderExternal)return e.params.virtual.renderExternal.call(e,{offset:T,from:O,to:C,slides:function(){const t=[];for(let i=O;i<=C;i+=1)t.push(h[i]);return t}()}),void k();const j=[],$=[];if(t)e.$wrapperEl.find(`.${e.params.slideClass}`).remove();else for(let i=d;i<=f;i+=1)(i<O||i>C)&&e.$wrapperEl.find(`.${e.params.slideClass}[data-swiper-slide-index="${i}"]`).remove();for(let i=0;i<h.length;i+=1)i>=O&&i<=C&&(void 0===f||t?$.push(i):(i>f&&$.push(i),i<d&&j.push(i)));$.forEach((t=>{e.$wrapperEl.append(m(h[t],t))})),j.sort(((a,b)=>b-a)).forEach((t=>{e.$wrapperEl.prepend(m(h[t],t))})),e.$wrapperEl.children(".swiper-slide").css(x,`${T}px`),k()},renderSlide(t,e){const n=this,r=n.params.virtual;if(r.cache&&n.virtual.cache[e])return n.virtual.cache[e];const o=r.renderSlide?h(r.renderSlide.call(n,t,e)):h(`<div class="${n.params.slideClass}" data-swiper-slide-index="${e}">${t}</div>`);return o.attr("data-swiper-slide-index")||o.attr("data-swiper-slide-index",e),r.cache&&(n.virtual.cache[e]=o),o},appendSlide(t){const e=this;if("object"==typeof t&&"length"in t)for(let i=0;i<t.length;i+=1)t[i]&&e.virtual.slides.push(t[i]);else e.virtual.slides.push(t);e.virtual.update(!0)},prependSlide(t){const e=this,n=e.activeIndex;let r=n+1,o=1;if(Array.isArray(t)){for(let i=0;i<t.length;i+=1)t[i]&&e.virtual.slides.unshift(t[i]);r=n+t.length,o=t.length}else e.virtual.slides.unshift(t);if(e.params.virtual.cache){const t=e.virtual.cache,n={};Object.keys(t).forEach((e=>{const r=t[e],l=r.attr("data-swiper-slide-index");l&&r.attr("data-swiper-slide-index",parseInt(l,10)+1),n[parseInt(e,10)+o]=r})),e.virtual.cache=n}e.virtual.update(!0),e.slideTo(r,0)},removeSlide(t){const e=this;if(null==t)return;let n=e.activeIndex;if(Array.isArray(t))for(let i=t.length-1;i>=0;i-=1)e.virtual.slides.splice(t[i],1),e.params.virtual.cache&&delete e.virtual.cache[t[i]],t[i]<n&&(n-=1),n=Math.max(n,0);else e.virtual.slides.splice(t,1),e.params.virtual.cache&&delete e.virtual.cache[t],t<n&&(n-=1),n=Math.max(n,0);e.virtual.update(!0),e.slideTo(n,0)},removeAllSlides(){const t=this;t.virtual.slides=[],t.params.virtual.cache&&(t.virtual.cache={}),t.virtual.update(!0),t.slideTo(0,0)}};var Z={name:"virtual",params:{virtual:{enabled:!1,slides:[],cache:!0,renderSlide:null,renderExternal:null,addSlidesBefore:0,addSlidesAfter:0}},create(){const t=this;y.extend(t,{virtual:{update:J.update.bind(t),appendSlide:J.appendSlide.bind(t),prependSlide:J.prependSlide.bind(t),removeSlide:J.removeSlide.bind(t),removeAllSlides:J.removeAllSlides.bind(t),renderSlide:J.renderSlide.bind(t),slides:t.params.virtual.slides,cache:{}}})},on:{beforeInit(){const t=this;if(!t.params.virtual.enabled)return;t.classNames.push(`${t.params.containerModifierClass}virtual`);const e={watchSlidesProgress:!0};y.extend(t.params,e),y.extend(t.originalParams,e),t.params.initialSlide||t.virtual.update()},setTranslate(){this.params.virtual.enabled&&this.virtual.update()}}};const K={handle(t){const e=this,{rtlTranslate:n}=e;let r=t;r.originalEvent&&(r=r.originalEvent);const o=r.keyCode||r.charCode,c=e.params.keyboard.pageUpDown,f=c&&33===o,h=c&&34===o,v=37===o,m=39===o,y=38===o,_=40===o;if(!e.allowSlideNext&&(e.isHorizontal()&&m||e.isVertical()&&_||h))return!1;if(!e.allowSlidePrev&&(e.isHorizontal()&&v||e.isVertical()&&y||f))return!1;if(!(r.shiftKey||r.altKey||r.ctrlKey||r.metaKey||l.activeElement&&l.activeElement.nodeName&&("input"===l.activeElement.nodeName.toLowerCase()||"textarea"===l.activeElement.nodeName.toLowerCase()))){if(e.params.keyboard.onlyInViewport&&(f||h||v||m||y||_)){let t=!1;if(e.$el.parents(`.${e.params.slideClass}`).length>0&&0===e.$el.parents(`.${e.params.slideActiveClass}`).length)return;const r=d.innerWidth,o=d.innerHeight,l=e.$el.offset();n&&(l.left-=e.$el[0].scrollLeft);const c=[[l.left,l.top],[l.left+e.width,l.top],[l.left,l.top+e.height],[l.left+e.width,l.top+e.height]];for(let i=0;i<c.length;i+=1){const e=c[i];e[0]>=0&&e[0]<=r&&e[1]>=0&&e[1]<=o&&(t=!0)}if(!t)return}e.isHorizontal()?((f||h||v||m)&&(r.preventDefault?r.preventDefault():r.returnValue=!1),((h||m)&&!n||(f||v)&&n)&&e.slideNext(),((f||v)&&!n||(h||m)&&n)&&e.slidePrev()):((f||h||y||_)&&(r.preventDefault?r.preventDefault():r.returnValue=!1),(h||_)&&e.slideNext(),(f||y)&&e.slidePrev()),e.emit("keyPress",o)}},enable(){const t=this;t.keyboard.enabled||(h(l).on("keydown",t.keyboard.handle),t.keyboard.enabled=!0)},disable(){const t=this;t.keyboard.enabled&&(h(l).off("keydown",t.keyboard.handle),t.keyboard.enabled=!1)}};var Q={name:"keyboard",params:{keyboard:{enabled:!1,onlyInViewport:!0,pageUpDown:!0}},create(){const t=this;y.extend(t,{keyboard:{enabled:!1,enable:K.enable.bind(t),disable:K.disable.bind(t),handle:K.handle.bind(t)}})},on:{init(){const t=this;t.params.keyboard.enabled&&t.keyboard.enable()},destroy(){const t=this;t.keyboard.enabled&&t.keyboard.disable()}}};const tt={lastScrollTime:y.now(),lastEventBeforeSnap:void 0,recentWheelEvents:[],event:()=>d.navigator.userAgent.indexOf("firefox")>-1?"DOMMouseScroll":function(){const t="onwheel";let e=t in l;if(!e){const element=l.createElement("div");element.setAttribute(t,"return;"),e="function"==typeof element.onwheel}return!e&&l.implementation&&l.implementation.hasFeature&&!0!==l.implementation.hasFeature("","")&&(e=l.implementation.hasFeature("Events.wheel","3.0")),e}()?"wheel":"mousewheel",normalize(t){let e=0,n=0,r=0,o=0;return"detail"in t&&(n=t.detail),"wheelDelta"in t&&(n=-t.wheelDelta/120),"wheelDeltaY"in t&&(n=-t.wheelDeltaY/120),"wheelDeltaX"in t&&(e=-t.wheelDeltaX/120),"axis"in t&&t.axis===t.HORIZONTAL_AXIS&&(e=n,n=0),r=10*e,o=10*n,"deltaY"in t&&(o=t.deltaY),"deltaX"in t&&(r=t.deltaX),t.shiftKey&&!r&&(r=o,o=0),(r||o)&&t.deltaMode&&(1===t.deltaMode?(r*=40,o*=40):(r*=800,o*=800)),r&&!e&&(e=r<1?-1:1),o&&!n&&(n=o<1?-1:1),{spinX:e,spinY:n,pixelX:r,pixelY:o}},handleMouseEnter(){this.mouseEntered=!0},handleMouseLeave(){this.mouseEntered=!1},handle(t){let e=t;const n=this,r=n.params.mousewheel;n.params.cssMode&&e.preventDefault();let o=n.$el;if("container"!==n.params.mousewheel.eventsTarged&&(o=h(n.params.mousewheel.eventsTarged)),!n.mouseEntered&&!o[0].contains(e.target)&&!r.releaseOnEdges)return!0;e.originalEvent&&(e=e.originalEvent);let l=0;const c=n.rtlTranslate?-1:1,data=tt.normalize(e);if(r.forceToAxis)if(n.isHorizontal()){if(!(Math.abs(data.pixelX)>Math.abs(data.pixelY)))return!0;l=-data.pixelX*c}else{if(!(Math.abs(data.pixelY)>Math.abs(data.pixelX)))return!0;l=-data.pixelY}else l=Math.abs(data.pixelX)>Math.abs(data.pixelY)?-data.pixelX*c:-data.pixelY;if(0===l)return!0;if(r.invert&&(l=-l),n.params.freeMode){const t={time:y.now(),delta:Math.abs(l),direction:Math.sign(l)},{lastEventBeforeSnap:o}=n.mousewheel,c=o&&t.time<o.time+500&&t.delta<=o.delta&&t.direction===o.direction;if(!c){n.mousewheel.lastEventBeforeSnap=void 0,n.params.loop&&n.loopFix();let o=n.getTranslate()+l*r.sensitivity;const d=n.isBeginning,f=n.isEnd;if(o>=n.minTranslate()&&(o=n.minTranslate()),o<=n.maxTranslate()&&(o=n.maxTranslate()),n.setTransition(0),n.setTranslate(o),n.updateProgress(),n.updateActiveIndex(),n.updateSlidesClasses(),(!d&&n.isBeginning||!f&&n.isEnd)&&n.updateSlidesClasses(),n.params.freeModeSticky){clearTimeout(n.mousewheel.timeout),n.mousewheel.timeout=void 0;const e=n.mousewheel.recentWheelEvents;e.length>=15&&e.shift();const r=e.length?e[e.length-1]:void 0,o=e[0];if(e.push(t),r&&(t.delta>r.delta||t.direction!==r.direction))e.splice(0);else if(e.length>=15&&t.time-o.time<500&&o.delta-t.delta>=1&&t.delta<=6){const r=l>0?.8:.2;n.mousewheel.lastEventBeforeSnap=t,e.splice(0),n.mousewheel.timeout=y.nextTick((()=>{n.slideToClosest(n.params.speed,!0,void 0,r)}),0)}n.mousewheel.timeout||(n.mousewheel.timeout=y.nextTick((()=>{n.mousewheel.lastEventBeforeSnap=t,e.splice(0),n.slideToClosest(n.params.speed,!0,void 0,.5)}),500))}if(c||n.emit("scroll",e),n.params.autoplay&&n.params.autoplayDisableOnInteraction&&n.autoplay.stop(),o===n.minTranslate()||o===n.maxTranslate())return!0}}else{const e={time:y.now(),delta:Math.abs(l),direction:Math.sign(l),raw:t},r=n.mousewheel.recentWheelEvents;r.length>=2&&r.shift();const o=r.length?r[r.length-1]:void 0;if(r.push(e),o?(e.direction!==o.direction||e.delta>o.delta||e.time>o.time+150)&&n.mousewheel.animateSlider(e):n.mousewheel.animateSlider(e),n.mousewheel.releaseScroll(e))return!0}return e.preventDefault?e.preventDefault():e.returnValue=!1,!1},animateSlider(t){const e=this;return t.delta>=6&&y.now()-e.mousewheel.lastScrollTime<60||(t.direction<0?e.isEnd&&!e.params.loop||e.animating||(e.slideNext(),e.emit("scroll",t.raw)):e.isBeginning&&!e.params.loop||e.animating||(e.slidePrev(),e.emit("scroll",t.raw)),e.mousewheel.lastScrollTime=(new d.Date).getTime(),!1)},releaseScroll(t){const e=this,n=e.params.mousewheel;if(t.direction<0){if(e.isEnd&&!e.params.loop&&n.releaseOnEdges)return!0}else if(e.isBeginning&&!e.params.loop&&n.releaseOnEdges)return!0;return!1},enable(){const t=this,e=tt.event();if(t.params.cssMode)return t.wrapperEl.removeEventListener(e,t.mousewheel.handle),!0;if(!e)return!1;if(t.mousewheel.enabled)return!1;let n=t.$el;return"container"!==t.params.mousewheel.eventsTarged&&(n=h(t.params.mousewheel.eventsTarged)),n.on("mouseenter",t.mousewheel.handleMouseEnter),n.on("mouseleave",t.mousewheel.handleMouseLeave),n.on(e,t.mousewheel.handle),t.mousewheel.enabled=!0,!0},disable(){const t=this,e=tt.event();if(t.params.cssMode)return t.wrapperEl.addEventListener(e,t.mousewheel.handle),!0;if(!e)return!1;if(!t.mousewheel.enabled)return!1;let n=t.$el;return"container"!==t.params.mousewheel.eventsTarged&&(n=h(t.params.mousewheel.eventsTarged)),n.off(e,t.mousewheel.handle),t.mousewheel.enabled=!1,!0}};const et={update(){const t=this,e=t.params.navigation;if(t.params.loop)return;const{$nextEl:n,$prevEl:r}=t.navigation;r&&r.length>0&&(t.isBeginning?r.addClass(e.disabledClass):r.removeClass(e.disabledClass),r[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](e.lockClass)),n&&n.length>0&&(t.isEnd?n.addClass(e.disabledClass):n.removeClass(e.disabledClass),n[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](e.lockClass))},onPrevClick(t){const e=this;t.preventDefault(),e.isBeginning&&!e.params.loop||e.slidePrev()},onNextClick(t){const e=this;t.preventDefault(),e.isEnd&&!e.params.loop||e.slideNext()},init(){const t=this,e=t.params.navigation;if(!e.nextEl&&!e.prevEl)return;let n,r;e.nextEl&&(n=h(e.nextEl),t.params.uniqueNavElements&&"string"==typeof e.nextEl&&n.length>1&&1===t.$el.find(e.nextEl).length&&(n=t.$el.find(e.nextEl))),e.prevEl&&(r=h(e.prevEl),t.params.uniqueNavElements&&"string"==typeof e.prevEl&&r.length>1&&1===t.$el.find(e.prevEl).length&&(r=t.$el.find(e.prevEl))),n&&n.length>0&&n.on("click",t.navigation.onNextClick),r&&r.length>0&&r.on("click",t.navigation.onPrevClick),y.extend(t.navigation,{$nextEl:n,nextEl:n&&n[0],$prevEl:r,prevEl:r&&r[0]})},destroy(){const t=this,{$nextEl:e,$prevEl:n}=t.navigation;e&&e.length&&(e.off("click",t.navigation.onNextClick),e.removeClass(t.params.navigation.disabledClass)),n&&n.length&&(n.off("click",t.navigation.onPrevClick),n.removeClass(t.params.navigation.disabledClass))}};const nt={update(){const t=this,e=t.rtl,n=t.params.pagination;if(!n.el||!t.pagination.el||!t.pagination.$el||0===t.pagination.$el.length)return;const r=t.virtual&&t.params.virtual.enabled?t.virtual.slides.length:t.slides.length,o=t.pagination.$el;let l;const c=t.params.loop?Math.ceil((r-2*t.loopedSlides)/t.params.slidesPerGroup):t.snapGrid.length;if(t.params.loop?(l=Math.ceil((t.activeIndex-t.loopedSlides)/t.params.slidesPerGroup),l>r-1-2*t.loopedSlides&&(l-=r-2*t.loopedSlides),l>c-1&&(l-=c),l<0&&"bullets"!==t.params.paginationType&&(l=c+l)):l=void 0!==t.snapIndex?t.snapIndex:t.activeIndex||0,"bullets"===n.type&&t.pagination.bullets&&t.pagination.bullets.length>0){const r=t.pagination.bullets;let c,d,f;if(n.dynamicBullets&&(t.pagination.bulletSize=r.eq(0)[t.isHorizontal()?"outerWidth":"outerHeight"](!0),o.css(t.isHorizontal()?"width":"height",t.pagination.bulletSize*(n.dynamicMainBullets+4)+"px"),n.dynamicMainBullets>1&&void 0!==t.previousIndex&&(t.pagination.dynamicBulletIndex+=l-t.previousIndex,t.pagination.dynamicBulletIndex>n.dynamicMainBullets-1?t.pagination.dynamicBulletIndex=n.dynamicMainBullets-1:t.pagination.dynamicBulletIndex<0&&(t.pagination.dynamicBulletIndex=0)),c=l-t.pagination.dynamicBulletIndex,d=c+(Math.min(r.length,n.dynamicMainBullets)-1),f=(d+c)/2),r.removeClass(`${n.bulletActiveClass} ${n.bulletActiveClass}-next ${n.bulletActiveClass}-next-next ${n.bulletActiveClass}-prev ${n.bulletActiveClass}-prev-prev ${n.bulletActiveClass}-main`),o.length>1)r.each(((t,e)=>{const r=h(e),o=r.index();o===l&&r.addClass(n.bulletActiveClass),n.dynamicBullets&&(o>=c&&o<=d&&r.addClass(`${n.bulletActiveClass}-main`),o===c&&r.prev().addClass(`${n.bulletActiveClass}-prev`).prev().addClass(`${n.bulletActiveClass}-prev-prev`),o===d&&r.next().addClass(`${n.bulletActiveClass}-next`).next().addClass(`${n.bulletActiveClass}-next-next`))}));else{const e=r.eq(l),o=e.index();if(e.addClass(n.bulletActiveClass),n.dynamicBullets){const e=r.eq(c),l=r.eq(d);for(let i=c;i<=d;i+=1)r.eq(i).addClass(`${n.bulletActiveClass}-main`);if(t.params.loop)if(o>=r.length-n.dynamicMainBullets){for(let i=n.dynamicMainBullets;i>=0;i-=1)r.eq(r.length-i).addClass(`${n.bulletActiveClass}-main`);r.eq(r.length-n.dynamicMainBullets-1).addClass(`${n.bulletActiveClass}-prev`)}else e.prev().addClass(`${n.bulletActiveClass}-prev`).prev().addClass(`${n.bulletActiveClass}-prev-prev`),l.next().addClass(`${n.bulletActiveClass}-next`).next().addClass(`${n.bulletActiveClass}-next-next`);else e.prev().addClass(`${n.bulletActiveClass}-prev`).prev().addClass(`${n.bulletActiveClass}-prev-prev`),l.next().addClass(`${n.bulletActiveClass}-next`).next().addClass(`${n.bulletActiveClass}-next-next`)}}if(n.dynamicBullets){const o=Math.min(r.length,n.dynamicMainBullets+4),l=(t.pagination.bulletSize*o-t.pagination.bulletSize)/2-f*t.pagination.bulletSize,c=e?"right":"left";r.css(t.isHorizontal()?c:"top",`${l}px`)}}if("fraction"===n.type&&(o.find(`.${n.currentClass}`).text(n.formatFractionCurrent(l+1)),o.find(`.${n.totalClass}`).text(n.formatFractionTotal(c))),"progressbar"===n.type){let e;e=n.progressbarOpposite?t.isHorizontal()?"vertical":"horizontal":t.isHorizontal()?"horizontal":"vertical";const r=(l+1)/c;let d=1,f=1;"horizontal"===e?d=r:f=r,o.find(`.${n.progressbarFillClass}`).transform(`translate3d(0,0,0) scaleX(${d}) scaleY(${f})`).transition(t.params.speed)}"custom"===n.type&&n.renderCustom?(o.html(n.renderCustom(t,l+1,c)),t.emit("paginationRender",t,o[0])):t.emit("paginationUpdate",t,o[0]),o[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](n.lockClass)},render(){const t=this,e=t.params.pagination;if(!e.el||!t.pagination.el||!t.pagination.$el||0===t.pagination.$el.length)return;const n=t.virtual&&t.params.virtual.enabled?t.virtual.slides.length:t.slides.length,r=t.pagination.$el;let o="";if("bullets"===e.type){const l=t.params.loop?Math.ceil((n-2*t.loopedSlides)/t.params.slidesPerGroup):t.snapGrid.length;for(let i=0;i<l;i+=1)e.renderBullet?o+=e.renderBullet.call(t,i,e.bulletClass):o+=`<${e.bulletElement} class="${e.bulletClass}"></${e.bulletElement}>`;r.html(o),t.pagination.bullets=r.find(`.${e.bulletClass}`)}"fraction"===e.type&&(o=e.renderFraction?e.renderFraction.call(t,e.currentClass,e.totalClass):`<span class="${e.currentClass}"></span> / <span class="${e.totalClass}"></span>`,r.html(o)),"progressbar"===e.type&&(o=e.renderProgressbar?e.renderProgressbar.call(t,e.progressbarFillClass):`<span class="${e.progressbarFillClass}"></span>`,r.html(o)),"custom"!==e.type&&t.emit("paginationRender",t.pagination.$el[0])},init(){const t=this,e=t.params.pagination;if(!e.el)return;let n=h(e.el);0!==n.length&&(t.params.uniqueNavElements&&"string"==typeof e.el&&n.length>1&&(n=t.$el.find(e.el)),"bullets"===e.type&&e.clickable&&n.addClass(e.clickableClass),n.addClass(e.modifierClass+e.type),"bullets"===e.type&&e.dynamicBullets&&(n.addClass(`${e.modifierClass}${e.type}-dynamic`),t.pagination.dynamicBulletIndex=0,e.dynamicMainBullets<1&&(e.dynamicMainBullets=1)),"progressbar"===e.type&&e.progressbarOpposite&&n.addClass(e.progressbarOppositeClass),e.clickable&&n.on("click",`.${e.bulletClass}`,(function(e){e.preventDefault();let n=h(this).index()*t.params.slidesPerGroup;t.params.loop&&(n+=t.loopedSlides),t.slideTo(n)})),y.extend(t.pagination,{$el:n,el:n[0]}))},destroy(){const t=this,e=t.params.pagination;if(!e.el||!t.pagination.el||!t.pagination.$el||0===t.pagination.$el.length)return;const n=t.pagination.$el;n.removeClass(e.hiddenClass),n.removeClass(e.modifierClass+e.type),t.pagination.bullets&&t.pagination.bullets.removeClass(e.bulletActiveClass),e.clickable&&n.off("click",`.${e.bulletClass}`)}};const it={setTranslate(){const t=this;if(!t.params.scrollbar.el||!t.scrollbar.el)return;const{scrollbar:e,rtlTranslate:n,progress:progress}=t,{dragSize:r,trackSize:o,$dragEl:l,$el:c}=e,d=t.params.scrollbar;let f=r,h=(o-r)*progress;n?(h=-h,h>0?(f=r-h,h=0):-h+r>o&&(f=o+h)):h<0?(f=r+h,h=0):h+r>o&&(f=o-h),t.isHorizontal()?(l.transform(`translate3d(${h}px, 0, 0)`),l[0].style.width=`${f}px`):(l.transform(`translate3d(0px, ${h}px, 0)`),l[0].style.height=`${f}px`),d.hide&&(clearTimeout(t.scrollbar.timeout),c[0].style.opacity=1,t.scrollbar.timeout=setTimeout((()=>{c[0].style.opacity=0,c.transition(400)}),1e3))},setTransition(t){const e=this;e.params.scrollbar.el&&e.scrollbar.el&&e.scrollbar.$dragEl.transition(t)},updateSize(){const t=this;if(!t.params.scrollbar.el||!t.scrollbar.el)return;const{scrollbar:e}=t,{$dragEl:n,$el:r}=e;n[0].style.width="",n[0].style.height="";const o=t.isHorizontal()?r[0].offsetWidth:r[0].offsetHeight,l=t.size/t.virtualSize,c=l*(o/t.size);let d;d="auto"===t.params.scrollbar.dragSize?o*l:parseInt(t.params.scrollbar.dragSize,10),t.isHorizontal()?n[0].style.width=`${d}px`:n[0].style.height=`${d}px`,r[0].style.display=l>=1?"none":"",t.params.scrollbar.hide&&(r[0].style.opacity=0),y.extend(e,{trackSize:o,divider:l,moveDivider:c,dragSize:d}),e.$el[t.params.watchOverflow&&t.isLocked?"addClass":"removeClass"](t.params.scrollbar.lockClass)},getPointerPosition(t){return this.isHorizontal()?"touchstart"===t.type||"touchmove"===t.type?t.targetTouches[0].clientX:t.clientX:"touchstart"===t.type||"touchmove"===t.type?t.targetTouches[0].clientY:t.clientY},setDragPosition(t){const e=this,{scrollbar:n,rtlTranslate:r}=e,{$el:o,dragSize:l,trackSize:c,dragStartPos:d}=n;let f;f=(n.getPointerPosition(t)-o.offset()[e.isHorizontal()?"left":"top"]-(null!==d?d:l/2))/(c-l),f=Math.max(Math.min(f,1),0),r&&(f=1-f);const h=e.minTranslate()+(e.maxTranslate()-e.minTranslate())*f;e.updateProgress(h),e.setTranslate(h),e.updateActiveIndex(),e.updateSlidesClasses()},onDragStart(t){const e=this,n=e.params.scrollbar,{scrollbar:r,$wrapperEl:o}=e,{$el:l,$dragEl:c}=r;e.scrollbar.isTouched=!0,e.scrollbar.dragStartPos=t.target===c[0]||t.target===c?r.getPointerPosition(t)-t.target.getBoundingClientRect()[e.isHorizontal()?"left":"top"]:null,t.preventDefault(),t.stopPropagation(),o.transition(100),c.transition(100),r.setDragPosition(t),clearTimeout(e.scrollbar.dragTimeout),l.transition(0),n.hide&&l.css("opacity",1),e.params.cssMode&&e.$wrapperEl.css("scroll-snap-type","none"),e.emit("scrollbarDragStart",t)},onDragMove(t){const e=this,{scrollbar:n,$wrapperEl:r}=e,{$el:o,$dragEl:l}=n;e.scrollbar.isTouched&&(t.preventDefault?t.preventDefault():t.returnValue=!1,n.setDragPosition(t),r.transition(0),o.transition(0),l.transition(0),e.emit("scrollbarDragMove",t))},onDragEnd(t){const e=this,n=e.params.scrollbar,{scrollbar:r,$wrapperEl:o}=e,{$el:l}=r;e.scrollbar.isTouched&&(e.scrollbar.isTouched=!1,e.params.cssMode&&(e.$wrapperEl.css("scroll-snap-type",""),o.transition("")),n.hide&&(clearTimeout(e.scrollbar.dragTimeout),e.scrollbar.dragTimeout=y.nextTick((()=>{l.css("opacity",0),l.transition(400)}),1e3)),e.emit("scrollbarDragEnd",t),n.snapOnRelease&&e.slideToClosest())},enableDraggable(){const t=this;if(!t.params.scrollbar.el)return;const{scrollbar:e,touchEventsTouch:n,touchEventsDesktop:r,params:o}=t,c=e.$el[0],d=!(!_.passiveListener||!o.passiveListeners)&&{passive:!1,capture:!1},f=!(!_.passiveListener||!o.passiveListeners)&&{passive:!0,capture:!1};_.touch?(c.addEventListener(n.start,t.scrollbar.onDragStart,d),c.addEventListener(n.move,t.scrollbar.onDragMove,d),c.addEventListener(n.end,t.scrollbar.onDragEnd,f)):(c.addEventListener(r.start,t.scrollbar.onDragStart,d),l.addEventListener(r.move,t.scrollbar.onDragMove,d),l.addEventListener(r.end,t.scrollbar.onDragEnd,f))},disableDraggable(){const t=this;if(!t.params.scrollbar.el)return;const{scrollbar:e,touchEventsTouch:n,touchEventsDesktop:r,params:o}=t,c=e.$el[0],d=!(!_.passiveListener||!o.passiveListeners)&&{passive:!1,capture:!1},f=!(!_.passiveListener||!o.passiveListeners)&&{passive:!0,capture:!1};_.touch?(c.removeEventListener(n.start,t.scrollbar.onDragStart,d),c.removeEventListener(n.move,t.scrollbar.onDragMove,d),c.removeEventListener(n.end,t.scrollbar.onDragEnd,f)):(c.removeEventListener(r.start,t.scrollbar.onDragStart,d),l.removeEventListener(r.move,t.scrollbar.onDragMove,d),l.removeEventListener(r.end,t.scrollbar.onDragEnd,f))},init(){const t=this;if(!t.params.scrollbar.el)return;const{scrollbar:e,$el:n}=t,r=t.params.scrollbar;let o=h(r.el);t.params.uniqueNavElements&&"string"==typeof r.el&&o.length>1&&1===n.find(r.el).length&&(o=n.find(r.el));let l=o.find(`.${t.params.scrollbar.dragClass}`);0===l.length&&(l=h(`<div class="${t.params.scrollbar.dragClass}"></div>`),o.append(l)),y.extend(e,{$el:o,el:o[0],$dragEl:l,dragEl:l[0]}),r.draggable&&e.enableDraggable()},destroy(){this.scrollbar.disableDraggable()}};const ot={setTransform(t,progress){const{rtl:e}=this,n=h(t),r=e?-1:1,p=n.attr("data-swiper-parallax")||"0";let o=n.attr("data-swiper-parallax-x"),l=n.attr("data-swiper-parallax-y");const c=n.attr("data-swiper-parallax-scale"),d=n.attr("data-swiper-parallax-opacity");if(o||l?(o=o||"0",l=l||"0"):this.isHorizontal()?(o=p,l="0"):(l=p,o="0"),o=o.indexOf("%")>=0?parseInt(o,10)*progress*r+"%":o*progress*r+"px",l=l.indexOf("%")>=0?parseInt(l,10)*progress+"%":l*progress+"px",null!=d){const t=d-(d-1)*(1-Math.abs(progress));n[0].style.opacity=t}if(null==c)n.transform(`translate3d(${o}, ${l}, 0px)`);else{const t=c-(c-1)*(1-Math.abs(progress));n.transform(`translate3d(${o}, ${l}, 0px) scale(${t})`)}},setTranslate(){const t=this,{$el:e,slides:n,progress:progress,snapGrid:r}=t;e.children("[data-swiper-parallax], [data-swiper-parallax-x], [data-swiper-parallax-y], [data-swiper-parallax-opacity], [data-swiper-parallax-scale]").each(((e,n)=>{t.parallax.setTransform(n,progress)})),n.each(((e,n)=>{let o=n.progress;t.params.slidesPerGroup>1&&"auto"!==t.params.slidesPerView&&(o+=Math.ceil(e/2)-progress*(r.length-1)),o=Math.min(Math.max(o,-1),1),h(n).find("[data-swiper-parallax], [data-swiper-parallax-x], [data-swiper-parallax-y], [data-swiper-parallax-opacity], [data-swiper-parallax-scale]").each(((e,n)=>{t.parallax.setTransform(n,o)}))}))},setTransition(t=this.params.speed){const{$el:e}=this;e.find("[data-swiper-parallax], [data-swiper-parallax-x], [data-swiper-parallax-y], [data-swiper-parallax-opacity], [data-swiper-parallax-scale]").each(((e,n)=>{const r=h(n);let o=parseInt(r.attr("data-swiper-parallax-duration"),10)||t;0===t&&(o=0),r.transition(o)}))}};const at={getDistanceBetweenTouches(t){if(t.targetTouches.length<2)return 1;const e=t.targetTouches[0].pageX,n=t.targetTouches[0].pageY,r=t.targetTouches[1].pageX,o=t.targetTouches[1].pageY;return Math.sqrt((r-e)**2+(o-n)**2)},onGestureStart(t){const e=this,n=e.params.zoom,r=e.zoom,{gesture:o}=r;if(r.fakeGestureTouched=!1,r.fakeGestureMoved=!1,!_.gestures){if("touchstart"!==t.type||"touchstart"===t.type&&t.targetTouches.length<2)return;r.fakeGestureTouched=!0,o.scaleStart=at.getDistanceBetweenTouches(t)}o.$slideEl&&o.$slideEl.length||(o.$slideEl=h(t.target).closest(`.${e.params.slideClass}`),0===o.$slideEl.length&&(o.$slideEl=e.slides.eq(e.activeIndex)),o.$imageEl=o.$slideEl.find("img, svg, canvas, picture, .swiper-zoom-target"),o.$imageWrapEl=o.$imageEl.parent(`.${n.containerClass}`),o.maxRatio=o.$imageWrapEl.attr("data-swiper-zoom")||n.maxRatio,0!==o.$imageWrapEl.length)?(o.$imageEl&&o.$imageEl.transition(0),e.zoom.isScaling=!0):o.$imageEl=void 0},onGestureChange(t){const e=this.params.zoom,n=this.zoom,{gesture:r}=n;if(!_.gestures){if("touchmove"!==t.type||"touchmove"===t.type&&t.targetTouches.length<2)return;n.fakeGestureMoved=!0,r.scaleMove=at.getDistanceBetweenTouches(t)}r.$imageEl&&0!==r.$imageEl.length&&(n.scale=_.gestures?t.scale*n.currentScale:r.scaleMove/r.scaleStart*n.currentScale,n.scale>r.maxRatio&&(n.scale=r.maxRatio-1+(n.scale-r.maxRatio+1)**.5),n.scale<e.minRatio&&(n.scale=e.minRatio+1-(e.minRatio-n.scale+1)**.5),r.$imageEl.transform(`translate3d(0,0,0) scale(${n.scale})`))},onGestureEnd(t){const e=this,n=e.params.zoom,r=e.zoom,{gesture:o}=r;if(!_.gestures){if(!r.fakeGestureTouched||!r.fakeGestureMoved)return;if("touchend"!==t.type||"touchend"===t.type&&t.changedTouches.length<2&&!j.android)return;r.fakeGestureTouched=!1,r.fakeGestureMoved=!1}o.$imageEl&&0!==o.$imageEl.length&&(r.scale=Math.max(Math.min(r.scale,o.maxRatio),n.minRatio),o.$imageEl.transition(e.params.speed).transform(`translate3d(0,0,0) scale(${r.scale})`),r.currentScale=r.scale,r.isScaling=!1,1===r.scale&&(o.$slideEl=void 0))},onTouchStart(t){const e=this.zoom,{gesture:n,image:image}=e;n.$imageEl&&0!==n.$imageEl.length&&(image.isTouched||(j.android&&t.cancelable&&t.preventDefault(),image.isTouched=!0,image.touchesStart.x="touchstart"===t.type?t.targetTouches[0].pageX:t.pageX,image.touchesStart.y="touchstart"===t.type?t.targetTouches[0].pageY:t.pageY))},onTouchMove(t){const e=this,n=e.zoom,{gesture:r,image:image,velocity:o}=n;if(!r.$imageEl||0===r.$imageEl.length)return;if(e.allowClick=!1,!image.isTouched||!r.$slideEl)return;image.isMoved||(image.width=r.$imageEl[0].offsetWidth,image.height=r.$imageEl[0].offsetHeight,image.startX=y.getTranslate(r.$imageWrapEl[0],"x")||0,image.startY=y.getTranslate(r.$imageWrapEl[0],"y")||0,r.slideWidth=r.$slideEl[0].offsetWidth,r.slideHeight=r.$slideEl[0].offsetHeight,r.$imageWrapEl.transition(0),e.rtl&&(image.startX=-image.startX,image.startY=-image.startY));const l=image.width*n.scale,c=image.height*n.scale;if(!(l<r.slideWidth&&c<r.slideHeight)){if(image.minX=Math.min(r.slideWidth/2-l/2,0),image.maxX=-image.minX,image.minY=Math.min(r.slideHeight/2-c/2,0),image.maxY=-image.minY,image.touchesCurrent.x="touchmove"===t.type?t.targetTouches[0].pageX:t.pageX,image.touchesCurrent.y="touchmove"===t.type?t.targetTouches[0].pageY:t.pageY,!image.isMoved&&!n.isScaling){if(e.isHorizontal()&&(Math.floor(image.minX)===Math.floor(image.startX)&&image.touchesCurrent.x<image.touchesStart.x||Math.floor(image.maxX)===Math.floor(image.startX)&&image.touchesCurrent.x>image.touchesStart.x))return void(image.isTouched=!1);if(!e.isHorizontal()&&(Math.floor(image.minY)===Math.floor(image.startY)&&image.touchesCurrent.y<image.touchesStart.y||Math.floor(image.maxY)===Math.floor(image.startY)&&image.touchesCurrent.y>image.touchesStart.y))return void(image.isTouched=!1)}t.cancelable&&t.preventDefault(),t.stopPropagation(),image.isMoved=!0,image.currentX=image.touchesCurrent.x-image.touchesStart.x+image.startX,image.currentY=image.touchesCurrent.y-image.touchesStart.y+image.startY,image.currentX<image.minX&&(image.currentX=image.minX+1-(image.minX-image.currentX+1)**.8),image.currentX>image.maxX&&(image.currentX=image.maxX-1+(image.currentX-image.maxX+1)**.8),image.currentY<image.minY&&(image.currentY=image.minY+1-(image.minY-image.currentY+1)**.8),image.currentY>image.maxY&&(image.currentY=image.maxY-1+(image.currentY-image.maxY+1)**.8),o.prevPositionX||(o.prevPositionX=image.touchesCurrent.x),o.prevPositionY||(o.prevPositionY=image.touchesCurrent.y),o.prevTime||(o.prevTime=Date.now()),o.x=(image.touchesCurrent.x-o.prevPositionX)/(Date.now()-o.prevTime)/2,o.y=(image.touchesCurrent.y-o.prevPositionY)/(Date.now()-o.prevTime)/2,Math.abs(image.touchesCurrent.x-o.prevPositionX)<2&&(o.x=0),Math.abs(image.touchesCurrent.y-o.prevPositionY)<2&&(o.y=0),o.prevPositionX=image.touchesCurrent.x,o.prevPositionY=image.touchesCurrent.y,o.prevTime=Date.now(),r.$imageWrapEl.transform(`translate3d(${image.currentX}px, ${image.currentY}px,0)`)}},onTouchEnd(){const t=this.zoom,{gesture:e,image:image,velocity:n}=t;if(!e.$imageEl||0===e.$imageEl.length)return;if(!image.isTouched||!image.isMoved)return image.isTouched=!1,void(image.isMoved=!1);image.isTouched=!1,image.isMoved=!1;let r=300,o=300;const l=n.x*r,c=image.currentX+l,d=n.y*o,f=image.currentY+d;0!==n.x&&(r=Math.abs((c-image.currentX)/n.x)),0!==n.y&&(o=Math.abs((f-image.currentY)/n.y));const h=Math.max(r,o);image.currentX=c,image.currentY=f;const v=image.width*t.scale,m=image.height*t.scale;image.minX=Math.min(e.slideWidth/2-v/2,0),image.maxX=-image.minX,image.minY=Math.min(e.slideHeight/2-m/2,0),image.maxY=-image.minY,image.currentX=Math.max(Math.min(image.currentX,image.maxX),image.minX),image.currentY=Math.max(Math.min(image.currentY,image.maxY),image.minY),e.$imageWrapEl.transition(h).transform(`translate3d(${image.currentX}px, ${image.currentY}px,0)`)},onTransitionEnd(){const t=this,e=t.zoom,{gesture:n}=e;n.$slideEl&&t.previousIndex!==t.activeIndex&&(n.$imageEl&&n.$imageEl.transform("translate3d(0,0,0) scale(1)"),n.$imageWrapEl&&n.$imageWrapEl.transform("translate3d(0,0,0)"),e.scale=1,e.currentScale=1,n.$slideEl=void 0,n.$imageEl=void 0,n.$imageWrapEl=void 0)},toggle(t){const e=this.zoom;e.scale&&1!==e.scale?e.out():e.in(t)},in(t){const e=this,n=e.zoom,r=e.params.zoom,{gesture:o,image:image}=n;if(o.$slideEl||(e.params.virtual&&e.params.virtual.enabled&&e.virtual?o.$slideEl=e.$wrapperEl.children(`.${e.params.slideActiveClass}`):o.$slideEl=e.slides.eq(e.activeIndex),o.$imageEl=o.$slideEl.find("img, svg, canvas, picture, .swiper-zoom-target"),o.$imageWrapEl=o.$imageEl.parent(`.${r.containerClass}`)),!o.$imageEl||0===o.$imageEl.length)return;let l,c,d,f,h,v,m,y,_,w,x,S,E,O,C,T,k,j;o.$slideEl.addClass(`${r.zoomedSlideClass}`),void 0===image.touchesStart.x&&t?(l="touchend"===t.type?t.changedTouches[0].pageX:t.pageX,c="touchend"===t.type?t.changedTouches[0].pageY:t.pageY):(l=image.touchesStart.x,c=image.touchesStart.y),n.scale=o.$imageWrapEl.attr("data-swiper-zoom")||r.maxRatio,n.currentScale=o.$imageWrapEl.attr("data-swiper-zoom")||r.maxRatio,t?(k=o.$slideEl[0].offsetWidth,j=o.$slideEl[0].offsetHeight,d=o.$slideEl.offset().left,f=o.$slideEl.offset().top,h=d+k/2-l,v=f+j/2-c,_=o.$imageEl[0].offsetWidth,w=o.$imageEl[0].offsetHeight,x=_*n.scale,S=w*n.scale,E=Math.min(k/2-x/2,0),O=Math.min(j/2-S/2,0),C=-E,T=-O,m=h*n.scale,y=v*n.scale,m<E&&(m=E),m>C&&(m=C),y<O&&(y=O),y>T&&(y=T)):(m=0,y=0),o.$imageWrapEl.transition(300).transform(`translate3d(${m}px, ${y}px,0)`),o.$imageEl.transition(300).transform(`translate3d(0,0,0) scale(${n.scale})`)},out(){const t=this,e=t.zoom,n=t.params.zoom,{gesture:r}=e;r.$slideEl||(t.params.virtual&&t.params.virtual.enabled&&t.virtual?r.$slideEl=t.$wrapperEl.children(`.${t.params.slideActiveClass}`):r.$slideEl=t.slides.eq(t.activeIndex),r.$imageEl=r.$slideEl.find("img, svg, canvas, picture, .swiper-zoom-target"),r.$imageWrapEl=r.$imageEl.parent(`.${n.containerClass}`)),r.$imageEl&&0!==r.$imageEl.length&&(e.scale=1,e.currentScale=1,r.$imageWrapEl.transition(300).transform("translate3d(0,0,0)"),r.$imageEl.transition(300).transform("translate3d(0,0,0) scale(1)"),r.$slideEl.removeClass(`${n.zoomedSlideClass}`),r.$slideEl=void 0)},enable(){const t=this,e=t.zoom;if(e.enabled)return;e.enabled=!0;const n=!("touchstart"!==t.touchEvents.start||!_.passiveListener||!t.params.passiveListeners)&&{passive:!0,capture:!1},r=!_.passiveListener||{passive:!1,capture:!0},o=`.${t.params.slideClass}`;_.gestures?(t.$wrapperEl.on("gesturestart",o,e.onGestureStart,n),t.$wrapperEl.on("gesturechange",o,e.onGestureChange,n),t.$wrapperEl.on("gestureend",o,e.onGestureEnd,n)):"touchstart"===t.touchEvents.start&&(t.$wrapperEl.on(t.touchEvents.start,o,e.onGestureStart,n),t.$wrapperEl.on(t.touchEvents.move,o,e.onGestureChange,r),t.$wrapperEl.on(t.touchEvents.end,o,e.onGestureEnd,n),t.touchEvents.cancel&&t.$wrapperEl.on(t.touchEvents.cancel,o,e.onGestureEnd,n)),t.$wrapperEl.on(t.touchEvents.move,`.${t.params.zoom.containerClass}`,e.onTouchMove,r)},disable(){const t=this,e=t.zoom;if(!e.enabled)return;t.zoom.enabled=!1;const n=!("touchstart"!==t.touchEvents.start||!_.passiveListener||!t.params.passiveListeners)&&{passive:!0,capture:!1},r=!_.passiveListener||{passive:!1,capture:!0},o=`.${t.params.slideClass}`;_.gestures?(t.$wrapperEl.off("gesturestart",o,e.onGestureStart,n),t.$wrapperEl.off("gesturechange",o,e.onGestureChange,n),t.$wrapperEl.off("gestureend",o,e.onGestureEnd,n)):"touchstart"===t.touchEvents.start&&(t.$wrapperEl.off(t.touchEvents.start,o,e.onGestureStart,n),t.$wrapperEl.off(t.touchEvents.move,o,e.onGestureChange,r),t.$wrapperEl.off(t.touchEvents.end,o,e.onGestureEnd,n),t.touchEvents.cancel&&t.$wrapperEl.off(t.touchEvents.cancel,o,e.onGestureEnd,n)),t.$wrapperEl.off(t.touchEvents.move,`.${t.params.zoom.containerClass}`,e.onTouchMove,r)}};const st={loadInSlide(t,e=!0){const n=this,r=n.params.lazy;if(void 0===t)return;if(0===n.slides.length)return;const o=n.virtual&&n.params.virtual.enabled?n.$wrapperEl.children(`.${n.params.slideClass}[data-swiper-slide-index="${t}"]`):n.slides.eq(t);let l=o.find(`.${r.elementClass}:not(.${r.loadedClass}):not(.${r.loadingClass})`);!o.hasClass(r.elementClass)||o.hasClass(r.loadedClass)||o.hasClass(r.loadingClass)||(l=l.add(o[0])),0!==l.length&&l.each(((t,l)=>{const c=h(l);c.addClass(r.loadingClass);const d=c.attr("data-background"),f=c.attr("data-src"),v=c.attr("data-srcset"),m=c.attr("data-sizes"),y=c.parent("picture");n.loadImage(c[0],f||d,v,m,!1,(()=>{if(null!=n&&n&&(!n||n.params)&&!n.destroyed){if(d?(c.css("background-image",`url("${d}")`),c.removeAttr("data-background")):(v&&(c.attr("srcset",v),c.removeAttr("data-srcset")),m&&(c.attr("sizes",m),c.removeAttr("data-sizes")),y.length&&y.children("source").each(((t,e)=>{const n=h(e);n.attr("data-srcset")&&(n.attr("srcset",n.attr("data-srcset")),n.removeAttr("data-srcset"))})),f&&(c.attr("src",f),c.removeAttr("data-src"))),c.addClass(r.loadedClass).removeClass(r.loadingClass),o.find(`.${r.preloaderClass}`).remove(),n.params.loop&&e){const t=o.attr("data-swiper-slide-index");if(o.hasClass(n.params.slideDuplicateClass)){const e=n.$wrapperEl.children(`[data-swiper-slide-index="${t}"]:not(.${n.params.slideDuplicateClass})`);n.lazy.loadInSlide(e.index(),!1)}else{const e=n.$wrapperEl.children(`.${n.params.slideDuplicateClass}[data-swiper-slide-index="${t}"]`);n.lazy.loadInSlide(e.index(),!1)}}n.emit("lazyImageReady",o[0],c[0]),n.params.autoHeight&&n.updateAutoHeight()}})),n.emit("lazyImageLoad",o[0],c[0])}))},load(){const t=this,{$wrapperEl:e,params:n,slides:r,activeIndex:o}=t,l=t.virtual&&n.virtual.enabled,c=n.lazy;let d=n.slidesPerView;function f(t){if(l){if(e.children(`.${n.slideClass}[data-swiper-slide-index="${t}"]`).length)return!0}else if(r[t])return!0;return!1}function v(t){return l?h(t).attr("data-swiper-slide-index"):h(t).index()}if("auto"===d&&(d=0),t.lazy.initialImageLoaded||(t.lazy.initialImageLoaded=!0),t.params.watchSlidesVisibility)e.children(`.${n.slideVisibleClass}`).each(((e,n)=>{const r=l?h(n).attr("data-swiper-slide-index"):h(n).index();t.lazy.loadInSlide(r)}));else if(d>1)for(let i=o;i<o+d;i+=1)f(i)&&t.lazy.loadInSlide(i);else t.lazy.loadInSlide(o);if(c.loadPrevNext)if(d>1||c.loadPrevNextAmount&&c.loadPrevNextAmount>1){const e=c.loadPrevNextAmount,n=d,l=Math.min(o+n+Math.max(e,n),r.length),h=Math.max(o-Math.max(n,e),0);for(let i=o+d;i<l;i+=1)f(i)&&t.lazy.loadInSlide(i);for(let i=h;i<o;i+=1)f(i)&&t.lazy.loadInSlide(i)}else{const r=e.children(`.${n.slideNextClass}`);r.length>0&&t.lazy.loadInSlide(v(r));const o=e.children(`.${n.slidePrevClass}`);o.length>0&&t.lazy.loadInSlide(v(o))}}};const lt={LinearSpline:function(t,e){const n=function(){let t,e,n;return(r,o)=>{for(e=-1,t=r.length;t-e>1;)n=t+e>>1,r[n]<=o?e=n:t=n;return t}}();let r,o;return this.x=t,this.y=e,this.lastIndex=t.length-1,this.interpolate=function(t){return t?(o=n(this.x,t),r=o-1,(t-this.x[r])*(this.y[o]-this.y[r])/(this.x[o]-this.x[r])+this.y[r]):0},this},getInterpolateFunction(t){const e=this;e.controller.spline||(e.controller.spline=e.params.loop?new lt.LinearSpline(e.slidesGrid,t.slidesGrid):new lt.LinearSpline(e.snapGrid,t.snapGrid))},setTranslate(t,e){const n=this,r=n.controller.control;let o,l;function c(t){const e=n.rtlTranslate?-n.translate:n.translate;"slide"===n.params.controller.by&&(n.controller.getInterpolateFunction(t),l=-n.controller.spline.interpolate(-e)),l&&"container"!==n.params.controller.by||(o=(t.maxTranslate()-t.minTranslate())/(n.maxTranslate()-n.minTranslate()),l=(e-n.minTranslate())*o+t.minTranslate()),n.params.controller.inverse&&(l=t.maxTranslate()-l),t.updateProgress(l),t.setTranslate(l,n),t.updateActiveIndex(),t.updateSlidesClasses()}if(Array.isArray(r))for(let i=0;i<r.length;i+=1)r[i]!==e&&r[i]instanceof F&&c(r[i]);else r instanceof F&&e!==r&&c(r)},setTransition(t,e){const n=this,r=n.controller.control;let i;function o(e){e.setTransition(t,n),0!==t&&(e.transitionStart(),e.params.autoHeight&&y.nextTick((()=>{e.updateAutoHeight()})),e.$wrapperEl.transitionEnd((()=>{r&&(e.params.loop&&"slide"===n.params.controller.by&&e.loopFix(),e.transitionEnd())})))}if(Array.isArray(r))for(i=0;i<r.length;i+=1)r[i]!==e&&r[i]instanceof F&&o(r[i]);else r instanceof F&&e!==r&&o(r)}};const ut={makeElFocusable:t=>(t.attr("tabIndex","0"),t),makeElNotFocusable:t=>(t.attr("tabIndex","-1"),t),addElRole:(t,e)=>(t.attr("role",e),t),addElLabel:(t,label)=>(t.attr("aria-label",label),t),disableEl:t=>(t.attr("aria-disabled",!0),t),enableEl:t=>(t.attr("aria-disabled",!1),t),onEnterKey(t){const e=this,n=e.params.a11y;if(13!==t.keyCode)return;const r=h(t.target);e.navigation&&e.navigation.$nextEl&&r.is(e.navigation.$nextEl)&&(e.isEnd&&!e.params.loop||e.slideNext(),e.isEnd?e.a11y.notify(n.lastSlideMessage):e.a11y.notify(n.nextSlideMessage)),e.navigation&&e.navigation.$prevEl&&r.is(e.navigation.$prevEl)&&(e.isBeginning&&!e.params.loop||e.slidePrev(),e.isBeginning?e.a11y.notify(n.firstSlideMessage):e.a11y.notify(n.prevSlideMessage)),e.pagination&&r.is(`.${e.params.pagination.bulletClass}`)&&r[0].click()},notify(t){const e=this.a11y.liveRegion;0!==e.length&&(e.html(""),e.html(t))},updateNavigation(){const t=this;if(t.params.loop||!t.navigation)return;const{$nextEl:e,$prevEl:n}=t.navigation;n&&n.length>0&&(t.isBeginning?(t.a11y.disableEl(n),t.a11y.makeElNotFocusable(n)):(t.a11y.enableEl(n),t.a11y.makeElFocusable(n))),e&&e.length>0&&(t.isEnd?(t.a11y.disableEl(e),t.a11y.makeElNotFocusable(e)):(t.a11y.enableEl(e),t.a11y.makeElFocusable(e)))},updatePagination(){const t=this,e=t.params.a11y;t.pagination&&t.params.pagination.clickable&&t.pagination.bullets&&t.pagination.bullets.length&&t.pagination.bullets.each(((n,r)=>{const o=h(r);t.a11y.makeElFocusable(o),t.a11y.addElRole(o,"button"),t.a11y.addElLabel(o,e.paginationBulletMessage.replace(/\{\{index\}\}/,o.index()+1))}))},init(){const t=this;t.$el.append(t.a11y.liveRegion);const e=t.params.a11y;let n,r;t.navigation&&t.navigation.$nextEl&&(n=t.navigation.$nextEl),t.navigation&&t.navigation.$prevEl&&(r=t.navigation.$prevEl),n&&(t.a11y.makeElFocusable(n),t.a11y.addElRole(n,"button"),t.a11y.addElLabel(n,e.nextSlideMessage),n.on("keydown",t.a11y.onEnterKey)),r&&(t.a11y.makeElFocusable(r),t.a11y.addElRole(r,"button"),t.a11y.addElLabel(r,e.prevSlideMessage),r.on("keydown",t.a11y.onEnterKey)),t.pagination&&t.params.pagination.clickable&&t.pagination.bullets&&t.pagination.bullets.length&&t.pagination.$el.on("keydown",`.${t.params.pagination.bulletClass}`,t.a11y.onEnterKey)},destroy(){const t=this;let e,n;t.a11y.liveRegion&&t.a11y.liveRegion.length>0&&t.a11y.liveRegion.remove(),t.navigation&&t.navigation.$nextEl&&(e=t.navigation.$nextEl),t.navigation&&t.navigation.$prevEl&&(n=t.navigation.$prevEl),e&&e.off("keydown",t.a11y.onEnterKey),n&&n.off("keydown",t.a11y.onEnterKey),t.pagination&&t.params.pagination.clickable&&t.pagination.bullets&&t.pagination.bullets.length&&t.pagination.$el.off("keydown",`.${t.params.pagination.bulletClass}`,t.a11y.onEnterKey)}};const ct={init(){const t=this;if(!t.params.history)return;if(!d.history||!d.history.pushState)return t.params.history.enabled=!1,void(t.params.hashNavigation.enabled=!0);const e=t.history;e.initialized=!0,e.paths=ct.getPathValues(),(e.paths.key||e.paths.value)&&(e.scrollToSlide(0,e.paths.value,t.params.runCallbacksOnInit),t.params.history.replaceState||d.addEventListener("popstate",t.history.setHistoryPopState))},destroy(){const t=this;t.params.history.replaceState||d.removeEventListener("popstate",t.history.setHistoryPopState)},setHistoryPopState(){const t=this;t.history.paths=ct.getPathValues(),t.history.scrollToSlide(t.params.speed,t.history.paths.value,!1)},getPathValues(){const t=d.location.pathname.slice(1).split("/").filter((t=>""!==t)),e=t.length;return{key:t[e-2],value:t[e-1]}},setHistory(t,e){const n=this;if(!n.history.initialized||!n.params.history.enabled)return;const r=n.slides.eq(e);let o=ct.slugify(r.attr("data-history"));d.location.pathname.includes(t)||(o=`${t}/${o}`);const l=d.history.state;l&&l.value===o||(n.params.history.replaceState?d.history.replaceState({value:o},null,o):d.history.pushState({value:o},null,o))},slugify:text=>text.toString().replace(/\s+/g,"-").replace(/[^\w-]+/g,"").replace(/--+/g,"-").replace(/^-+/,"").replace(/-+$/,""),scrollToSlide(t,e,n){const r=this;if(e)for(let i=0,o=r.slides.length;i<o;i+=1){const o=r.slides.eq(i);if(ct.slugify(o.attr("data-history"))===e&&!o.hasClass(r.params.slideDuplicateClass)){const e=o.index();r.slideTo(e,t,n)}}else r.slideTo(0,t,n)}};const pt={onHashCange(){const t=this;t.emit("hashChange");const e=l.location.hash.replace("#","");if(e!==t.slides.eq(t.activeIndex).attr("data-hash")){const n=t.$wrapperEl.children(`.${t.params.slideClass}[data-hash="${e}"]`).index();if(void 0===n)return;t.slideTo(n)}},setHash(){const t=this;if(t.hashNavigation.initialized&&t.params.hashNavigation.enabled)if(t.params.hashNavigation.replaceState&&d.history&&d.history.replaceState)d.history.replaceState(null,null,`#${t.slides.eq(t.activeIndex).attr("data-hash")}`||""),t.emit("hashSet");else{const e=t.slides.eq(t.activeIndex),n=e.attr("data-hash")||e.attr("data-history");l.location.hash=n||"",t.emit("hashSet")}},init(){const t=this;if(!t.params.hashNavigation.enabled||t.params.history&&t.params.history.enabled)return;t.hashNavigation.initialized=!0;const e=l.location.hash.replace("#","");if(e){const n=0;for(let i=0,r=t.slides.length;i<r;i+=1){const r=t.slides.eq(i);if((r.attr("data-hash")||r.attr("data-history"))===e&&!r.hasClass(t.params.slideDuplicateClass)){const e=r.index();t.slideTo(e,n,t.params.runCallbacksOnInit,!0)}}}t.params.hashNavigation.watchState&&h(d).on("hashchange",t.hashNavigation.onHashCange)},destroy(){const t=this;t.params.hashNavigation.watchState&&h(d).off("hashchange",t.hashNavigation.onHashCange)}};const ft={run(){const t=this,e=t.slides.eq(t.activeIndex);let n=t.params.autoplay.delay;e.attr("data-swiper-autoplay")&&(n=e.attr("data-swiper-autoplay")||t.params.autoplay.delay),clearTimeout(t.autoplay.timeout),t.autoplay.timeout=y.nextTick((()=>{t.params.autoplay.reverseDirection?t.params.loop?(t.loopFix(),t.slidePrev(t.params.speed,!0,!0),t.emit("autoplay")):t.isBeginning?t.params.autoplay.stopOnLastSlide?t.autoplay.stop():(t.slideTo(t.slides.length-1,t.params.speed,!0,!0),t.emit("autoplay")):(t.slidePrev(t.params.speed,!0,!0),t.emit("autoplay")):t.params.loop?(t.loopFix(),t.slideNext(t.params.speed,!0,!0),t.emit("autoplay")):t.isEnd?t.params.autoplay.stopOnLastSlide?t.autoplay.stop():(t.slideTo(0,t.params.speed,!0,!0),t.emit("autoplay")):(t.slideNext(t.params.speed,!0,!0),t.emit("autoplay")),t.params.cssMode&&t.autoplay.running&&t.autoplay.run()}),n)},start(){const t=this;return void 0===t.autoplay.timeout&&(!t.autoplay.running&&(t.autoplay.running=!0,t.emit("autoplayStart"),t.autoplay.run(),!0))},stop(){const t=this;return!!t.autoplay.running&&(void 0!==t.autoplay.timeout&&(t.autoplay.timeout&&(clearTimeout(t.autoplay.timeout),t.autoplay.timeout=void 0),t.autoplay.running=!1,t.emit("autoplayStop"),!0))},pause(t){const e=this;e.autoplay.running&&(e.autoplay.paused||(e.autoplay.timeout&&clearTimeout(e.autoplay.timeout),e.autoplay.paused=!0,0!==t&&e.params.autoplay.waitForTransition?(e.$wrapperEl[0].addEventListener("transitionend",e.autoplay.onTransitionEnd),e.$wrapperEl[0].addEventListener("webkitTransitionEnd",e.autoplay.onTransitionEnd)):(e.autoplay.paused=!1,e.autoplay.run())))}};const ht={setTranslate(){const t=this,{slides:e}=t;for(let i=0;i<e.length;i+=1){const e=t.slides.eq(i);let n=-e[0].swiperSlideOffset;t.params.virtualTranslate||(n-=t.translate);let r=0;t.isHorizontal()||(r=n,n=0);const o=t.params.fadeEffect.crossFade?Math.max(1-Math.abs(e[0].progress),0):1+Math.min(Math.max(e[0].progress,-1),0);e.css({opacity:o}).transform(`translate3d(${n}px, ${r}px, 0px)`)}},setTransition(t){const e=this,{slides:n,$wrapperEl:r}=e;if(n.transition(t),e.params.virtualTranslate&&0!==t){let t=!1;n.transitionEnd((()=>{if(t)return;if(!e||e.destroyed)return;t=!0,e.animating=!1;const n=["webkitTransitionEnd","transitionend"];for(let i=0;i<n.length;i+=1)r.trigger(n[i])}))}}};const vt={setTranslate(){const t=this,{$el:e,$wrapperEl:n,slides:r,width:o,height:l,rtlTranslate:c,size:d}=t,f=t.params.cubeEffect,v=t.isHorizontal(),m=t.virtual&&t.params.virtual.enabled;let y,_=0;f.shadow&&(v?(y=n.find(".swiper-cube-shadow"),0===y.length&&(y=h('<div class="swiper-cube-shadow"></div>'),n.append(y)),y.css({height:`${o}px`})):(y=e.find(".swiper-cube-shadow"),0===y.length&&(y=h('<div class="swiper-cube-shadow"></div>'),e.append(y))));for(let i=0;i<r.length;i+=1){const t=r.eq(i);let e=i;m&&(e=parseInt(t.attr("data-swiper-slide-index"),10));let n=90*e,o=Math.floor(n/360);c&&(n=-n,o=Math.floor(-n/360));const progress=Math.max(Math.min(t[0].progress,1),-1);let l=0,y=0,w=0;e%4==0?(l=4*-o*d,w=0):(e-1)%4==0?(l=0,w=4*-o*d):(e-2)%4==0?(l=d+4*o*d,w=d):(e-3)%4==0&&(l=-d,w=3*d+4*d*o),c&&(l=-l),v||(y=l,l=0);const x=`rotateX(${v?0:-n}deg) rotateY(${v?n:0}deg) translate3d(${l}px, ${y}px, ${w}px)`;if(progress<=1&&progress>-1&&(_=90*e+90*progress,c&&(_=90*-e-90*progress)),t.transform(x),f.slideShadows){let e=v?t.find(".swiper-slide-shadow-left"):t.find(".swiper-slide-shadow-top"),n=v?t.find(".swiper-slide-shadow-right"):t.find(".swiper-slide-shadow-bottom");0===e.length&&(e=h(`<div class="swiper-slide-shadow-${v?"left":"top"}"></div>`),t.append(e)),0===n.length&&(n=h(`<div class="swiper-slide-shadow-${v?"right":"bottom"}"></div>`),t.append(n)),e.length&&(e[0].style.opacity=Math.max(-progress,0)),n.length&&(n[0].style.opacity=Math.max(progress,0))}}if(n.css({"-webkit-transform-origin":`50% 50% -${d/2}px`,"-moz-transform-origin":`50% 50% -${d/2}px`,"-ms-transform-origin":`50% 50% -${d/2}px`,"transform-origin":`50% 50% -${d/2}px`}),f.shadow)if(v)y.transform(`translate3d(0px, ${o/2+f.shadowOffset}px, ${-o/2}px) rotateX(90deg) rotateZ(0deg) scale(${f.shadowScale})`);else{const t=Math.abs(_)-90*Math.floor(Math.abs(_)/90),e=1.5-(Math.sin(2*t*Math.PI/360)/2+Math.cos(2*t*Math.PI/360)/2),n=f.shadowScale,r=f.shadowScale/e,o=f.shadowOffset;y.transform(`scale3d(${n}, 1, ${r}) translate3d(0px, ${l/2+o}px, ${-l/2/r}px) rotateX(-90deg)`)}const w=W.isSafari||W.isWebView?-d/2:0;n.transform(`translate3d(0px,0,${w}px) rotateX(${t.isHorizontal()?0:_}deg) rotateY(${t.isHorizontal()?-_:0}deg)`)},setTransition(t){const e=this,{$el:n,slides:r}=e;r.transition(t).find(".swiper-slide-shadow-top, .swiper-slide-shadow-right, .swiper-slide-shadow-bottom, .swiper-slide-shadow-left").transition(t),e.params.cubeEffect.shadow&&!e.isHorizontal()&&n.find(".swiper-cube-shadow").transition(t)}};const mt={setTranslate(){const t=this,{slides:e,rtlTranslate:n}=t;for(let i=0;i<e.length;i+=1){const r=e.eq(i);let progress=r[0].progress;t.params.flipEffect.limitRotation&&(progress=Math.max(Math.min(r[0].progress,1),-1));let o=-180*progress,l=0,c=-r[0].swiperSlideOffset,d=0;if(t.isHorizontal()?n&&(o=-o):(d=c,c=0,l=-o,o=0),r[0].style.zIndex=-Math.abs(Math.round(progress))+e.length,t.params.flipEffect.slideShadows){let e=t.isHorizontal()?r.find(".swiper-slide-shadow-left"):r.find(".swiper-slide-shadow-top"),n=t.isHorizontal()?r.find(".swiper-slide-shadow-right"):r.find(".swiper-slide-shadow-bottom");0===e.length&&(e=h(`<div class="swiper-slide-shadow-${t.isHorizontal()?"left":"top"}"></div>`),r.append(e)),0===n.length&&(n=h(`<div class="swiper-slide-shadow-${t.isHorizontal()?"right":"bottom"}"></div>`),r.append(n)),e.length&&(e[0].style.opacity=Math.max(-progress,0)),n.length&&(n[0].style.opacity=Math.max(progress,0))}r.transform(`translate3d(${c}px, ${d}px, 0px) rotateX(${l}deg) rotateY(${o}deg)`)}},setTransition(t){const e=this,{slides:n,activeIndex:r,$wrapperEl:o}=e;if(n.transition(t).find(".swiper-slide-shadow-top, .swiper-slide-shadow-right, .swiper-slide-shadow-bottom, .swiper-slide-shadow-left").transition(t),e.params.virtualTranslate&&0!==t){let t=!1;n.eq(r).transitionEnd((function(){if(t)return;if(!e||e.destroyed)return;t=!0,e.animating=!1;const n=["webkitTransitionEnd","transitionend"];for(let i=0;i<n.length;i+=1)o.trigger(n[i])}))}}};const gt={setTranslate(){const t=this,{width:e,height:n,slides:r,$wrapperEl:o,slidesSizesGrid:l}=t,c=t.params.coverflowEffect,d=t.isHorizontal(),f=t.translate,v=d?e/2-f:n/2-f,m=d?c.rotate:-c.rotate,y=c.depth;for(let i=0,t=r.length;i<t;i+=1){const t=r.eq(i),e=l[i],n=(v-t[0].swiperSlideOffset-e/2)/e*c.modifier;let o=d?m*n:0,f=d?0:m*n,_=-y*Math.abs(n),w=c.stretch;"string"==typeof w&&-1!==w.indexOf("%")&&(w=parseFloat(c.stretch)/100*e);let x=d?0:w*n,S=d?w*n:0,E=1-(1-c.scale)*Math.abs(n);Math.abs(S)<.001&&(S=0),Math.abs(x)<.001&&(x=0),Math.abs(_)<.001&&(_=0),Math.abs(o)<.001&&(o=0),Math.abs(f)<.001&&(f=0),Math.abs(E)<.001&&(E=0);const O=`translate3d(${S}px,${x}px,${_}px)  rotateX(${f}deg) rotateY(${o}deg) scale(${E})`;if(t.transform(O),t[0].style.zIndex=1-Math.abs(Math.round(n)),c.slideShadows){let e=d?t.find(".swiper-slide-shadow-left"):t.find(".swiper-slide-shadow-top"),r=d?t.find(".swiper-slide-shadow-right"):t.find(".swiper-slide-shadow-bottom");0===e.length&&(e=h(`<div class="swiper-slide-shadow-${d?"left":"top"}"></div>`),t.append(e)),0===r.length&&(r=h(`<div class="swiper-slide-shadow-${d?"right":"bottom"}"></div>`),t.append(r)),e.length&&(e[0].style.opacity=n>0?n:0),r.length&&(r[0].style.opacity=-n>0?-n:0)}}if(_.pointerEvents||_.prefixedPointerEvents){o[0].style.perspectiveOrigin=`${v}px 50%`}},setTransition(t){this.slides.transition(t).find(".swiper-slide-shadow-top, .swiper-slide-shadow-right, .swiper-slide-shadow-bottom, .swiper-slide-shadow-left").transition(t)}};const yt={init(){const t=this,{thumbs:e}=t.params,n=t.constructor;e.swiper instanceof n?(t.thumbs.swiper=e.swiper,y.extend(t.thumbs.swiper.originalParams,{watchSlidesProgress:!0,slideToClickedSlide:!1}),y.extend(t.thumbs.swiper.params,{watchSlidesProgress:!0,slideToClickedSlide:!1})):y.isObject(e.swiper)&&(t.thumbs.swiper=new n(y.extend({},e.swiper,{watchSlidesVisibility:!0,watchSlidesProgress:!0,slideToClickedSlide:!1})),t.thumbs.swiperCreated=!0),t.thumbs.swiper.$el.addClass(t.params.thumbs.thumbsContainerClass),t.thumbs.swiper.on("tap",t.thumbs.onThumbClick)},onThumbClick(){const t=this,e=t.thumbs.swiper;if(!e)return;const n=e.clickedIndex,r=e.clickedSlide;if(r&&h(r).hasClass(t.params.thumbs.slideThumbActiveClass))return;if(null==n)return;let o;if(o=e.params.loop?parseInt(h(e.clickedSlide).attr("data-swiper-slide-index"),10):n,t.params.loop){let e=t.activeIndex;t.slides.eq(e).hasClass(t.params.slideDuplicateClass)&&(t.loopFix(),t._clientLeft=t.$wrapperEl[0].clientLeft,e=t.activeIndex);const n=t.slides.eq(e).prevAll(`[data-swiper-slide-index="${o}"]`).eq(0).index(),r=t.slides.eq(e).nextAll(`[data-swiper-slide-index="${o}"]`).eq(0).index();o=void 0===n?r:void 0===r?n:r-e<e-n?r:n}t.slideTo(o)},update(t){const e=this,n=e.thumbs.swiper;if(!n)return;const r="auto"===n.params.slidesPerView?n.slidesPerViewDynamic():n.params.slidesPerView,o=e.params.thumbs.autoScrollOffset,l=o&&!n.params.loop;if(e.realIndex!==n.realIndex||l){let c,d,f=n.activeIndex;if(n.params.loop){n.slides.eq(f).hasClass(n.params.slideDuplicateClass)&&(n.loopFix(),n._clientLeft=n.$wrapperEl[0].clientLeft,f=n.activeIndex);const t=n.slides.eq(f).prevAll(`[data-swiper-slide-index="${e.realIndex}"]`).eq(0).index(),r=n.slides.eq(f).nextAll(`[data-swiper-slide-index="${e.realIndex}"]`).eq(0).index();c=void 0===t?r:void 0===r?t:r-f==f-t?f:r-f<f-t?r:t,d=e.activeIndex>e.previousIndex?"next":"prev"}else c=e.realIndex,d=c>e.previousIndex?"next":"prev";l&&(c+="next"===d?o:-1*o),n.visibleSlidesIndexes&&n.visibleSlidesIndexes.indexOf(c)<0&&(n.params.centeredSlides?c=c>f?c-Math.floor(r/2)+1:c+Math.floor(r/2)-1:c>f&&(c=c-r+1),n.slideTo(c,t?0:void 0))}let c=1;const d=e.params.thumbs.slideThumbActiveClass;if(e.params.slidesPerView>1&&!e.params.centeredSlides&&(c=e.params.slidesPerView),e.params.thumbs.multipleActiveThumbs||(c=1),c=Math.floor(c),n.slides.removeClass(d),n.params.loop||n.params.virtual&&n.params.virtual.enabled)for(let i=0;i<c;i+=1)n.$wrapperEl.children(`[data-swiper-slide-index="${e.realIndex+i}"]`).addClass(d);else for(let i=0;i<c;i+=1)n.slides.eq(e.realIndex+i).addClass(d)}};const bt=[H,U,V,Y,G,Z,Q,{name:"mousewheel",params:{mousewheel:{enabled:!1,releaseOnEdges:!1,invert:!1,forceToAxis:!1,sensitivity:1,eventsTarged:"container"}},create(){const t=this;y.extend(t,{mousewheel:{enabled:!1,enable:tt.enable.bind(t),disable:tt.disable.bind(t),handle:tt.handle.bind(t),handleMouseEnter:tt.handleMouseEnter.bind(t),handleMouseLeave:tt.handleMouseLeave.bind(t),animateSlider:tt.animateSlider.bind(t),releaseScroll:tt.releaseScroll.bind(t),lastScrollTime:y.now(),lastEventBeforeSnap:void 0,recentWheelEvents:[]}})},on:{init(){const t=this;!t.params.mousewheel.enabled&&t.params.cssMode&&t.mousewheel.disable(),t.params.mousewheel.enabled&&t.mousewheel.enable()},destroy(){const t=this;t.params.cssMode&&t.mousewheel.enable(),t.mousewheel.enabled&&t.mousewheel.disable()}}},{name:"navigation",params:{navigation:{nextEl:null,prevEl:null,hideOnClick:!1,disabledClass:"swiper-button-disabled",hiddenClass:"swiper-button-hidden",lockClass:"swiper-button-lock"}},create(){const t=this;y.extend(t,{navigation:{init:et.init.bind(t),update:et.update.bind(t),destroy:et.destroy.bind(t),onNextClick:et.onNextClick.bind(t),onPrevClick:et.onPrevClick.bind(t)}})},on:{init(){this.navigation.init(),this.navigation.update()},toEdge(){this.navigation.update()},fromEdge(){this.navigation.update()},destroy(){this.navigation.destroy()},click(t){const e=this,{$nextEl:n,$prevEl:r}=e.navigation;if(e.params.navigation.hideOnClick&&!h(t.target).is(r)&&!h(t.target).is(n)){let t;n?t=n.hasClass(e.params.navigation.hiddenClass):r&&(t=r.hasClass(e.params.navigation.hiddenClass)),!0===t?e.emit("navigationShow",e):e.emit("navigationHide",e),n&&n.toggleClass(e.params.navigation.hiddenClass),r&&r.toggleClass(e.params.navigation.hiddenClass)}}}},{name:"pagination",params:{pagination:{el:null,bulletElement:"span",clickable:!1,hideOnClick:!1,renderBullet:null,renderProgressbar:null,renderFraction:null,renderCustom:null,progressbarOpposite:!1,type:"bullets",dynamicBullets:!1,dynamicMainBullets:1,formatFractionCurrent:t=>t,formatFractionTotal:t=>t,bulletClass:"swiper-pagination-bullet",bulletActiveClass:"swiper-pagination-bullet-active",modifierClass:"swiper-pagination-",currentClass:"swiper-pagination-current",totalClass:"swiper-pagination-total",hiddenClass:"swiper-pagination-hidden",progressbarFillClass:"swiper-pagination-progressbar-fill",progressbarOppositeClass:"swiper-pagination-progressbar-opposite",clickableClass:"swiper-pagination-clickable",lockClass:"swiper-pagination-lock"}},create(){const t=this;y.extend(t,{pagination:{init:nt.init.bind(t),render:nt.render.bind(t),update:nt.update.bind(t),destroy:nt.destroy.bind(t),dynamicBulletIndex:0}})},on:{init(){const t=this;t.pagination.init(),t.pagination.render(),t.pagination.update()},activeIndexChange(){const t=this;(t.params.loop||void 0===t.snapIndex)&&t.pagination.update()},snapIndexChange(){const t=this;t.params.loop||t.pagination.update()},slidesLengthChange(){const t=this;t.params.loop&&(t.pagination.render(),t.pagination.update())},snapGridLengthChange(){const t=this;t.params.loop||(t.pagination.render(),t.pagination.update())},destroy(){this.pagination.destroy()},click(t){const e=this;if(e.params.pagination.el&&e.params.pagination.hideOnClick&&e.pagination.$el.length>0&&!h(t.target).hasClass(e.params.pagination.bulletClass)){!0===e.pagination.$el.hasClass(e.params.pagination.hiddenClass)?e.emit("paginationShow",e):e.emit("paginationHide",e),e.pagination.$el.toggleClass(e.params.pagination.hiddenClass)}}}},{name:"scrollbar",params:{scrollbar:{el:null,dragSize:"auto",hide:!1,draggable:!1,snapOnRelease:!0,lockClass:"swiper-scrollbar-lock",dragClass:"swiper-scrollbar-drag"}},create(){const t=this;y.extend(t,{scrollbar:{init:it.init.bind(t),destroy:it.destroy.bind(t),updateSize:it.updateSize.bind(t),setTranslate:it.setTranslate.bind(t),setTransition:it.setTransition.bind(t),enableDraggable:it.enableDraggable.bind(t),disableDraggable:it.disableDraggable.bind(t),setDragPosition:it.setDragPosition.bind(t),getPointerPosition:it.getPointerPosition.bind(t),onDragStart:it.onDragStart.bind(t),onDragMove:it.onDragMove.bind(t),onDragEnd:it.onDragEnd.bind(t),isTouched:!1,timeout:null,dragTimeout:null}})},on:{init(){const t=this;t.scrollbar.init(),t.scrollbar.updateSize(),t.scrollbar.setTranslate()},update(){this.scrollbar.updateSize()},resize(){this.scrollbar.updateSize()},observerUpdate(){this.scrollbar.updateSize()},setTranslate(){this.scrollbar.setTranslate()},setTransition(t){this.scrollbar.setTransition(t)},destroy(){this.scrollbar.destroy()}}},{name:"parallax",params:{parallax:{enabled:!1}},create(){const t=this;y.extend(t,{parallax:{setTransform:ot.setTransform.bind(t),setTranslate:ot.setTranslate.bind(t),setTransition:ot.setTransition.bind(t)}})},on:{beforeInit(){const t=this;t.params.parallax.enabled&&(t.params.watchSlidesProgress=!0,t.originalParams.watchSlidesProgress=!0)},init(){this.params.parallax.enabled&&this.parallax.setTranslate()},setTranslate(){this.params.parallax.enabled&&this.parallax.setTranslate()},setTransition(t){this.params.parallax.enabled&&this.parallax.setTransition(t)}}},{name:"zoom",params:{zoom:{enabled:!1,maxRatio:3,minRatio:1,toggle:!0,containerClass:"swiper-zoom-container",zoomedSlideClass:"swiper-slide-zoomed"}},create(){const t=this,e={enabled:!1,scale:1,currentScale:1,isScaling:!1,gesture:{$slideEl:void 0,slideWidth:void 0,slideHeight:void 0,$imageEl:void 0,$imageWrapEl:void 0,maxRatio:3},image:{isTouched:void 0,isMoved:void 0,currentX:void 0,currentY:void 0,minX:void 0,minY:void 0,maxX:void 0,maxY:void 0,width:void 0,height:void 0,startX:void 0,startY:void 0,touchesStart:{},touchesCurrent:{}},velocity:{x:void 0,y:void 0,prevPositionX:void 0,prevPositionY:void 0,prevTime:void 0}};"onGestureStart onGestureChange onGestureEnd onTouchStart onTouchMove onTouchEnd onTransitionEnd toggle enable disable in out".split(" ").forEach((n=>{e[n]=at[n].bind(t)})),y.extend(t,{zoom:e});let n=1;Object.defineProperty(t.zoom,"scale",{get:()=>n,set(e){if(n!==e){const n=t.zoom.gesture.$imageEl?t.zoom.gesture.$imageEl[0]:void 0,r=t.zoom.gesture.$slideEl?t.zoom.gesture.$slideEl[0]:void 0;t.emit("zoomChange",e,n,r)}n=e}})},on:{init(){const t=this;t.params.zoom.enabled&&t.zoom.enable()},destroy(){this.zoom.disable()},touchStart(t){this.zoom.enabled&&this.zoom.onTouchStart(t)},touchEnd(t){this.zoom.enabled&&this.zoom.onTouchEnd(t)},doubleTap(t){const e=this;e.params.zoom.enabled&&e.zoom.enabled&&e.params.zoom.toggle&&e.zoom.toggle(t)},transitionEnd(){const t=this;t.zoom.enabled&&t.params.zoom.enabled&&t.zoom.onTransitionEnd()},slideChange(){const t=this;t.zoom.enabled&&t.params.zoom.enabled&&t.params.cssMode&&t.zoom.onTransitionEnd()}}},{name:"lazy",params:{lazy:{enabled:!1,loadPrevNext:!1,loadPrevNextAmount:1,loadOnTransitionStart:!1,elementClass:"swiper-lazy",loadingClass:"swiper-lazy-loading",loadedClass:"swiper-lazy-loaded",preloaderClass:"swiper-lazy-preloader"}},create(){const t=this;y.extend(t,{lazy:{initialImageLoaded:!1,load:st.load.bind(t),loadInSlide:st.loadInSlide.bind(t)}})},on:{beforeInit(){const t=this;t.params.lazy.enabled&&t.params.preloadImages&&(t.params.preloadImages=!1)},init(){const t=this;t.params.lazy.enabled&&!t.params.loop&&0===t.params.initialSlide&&t.lazy.load()},scroll(){const t=this;t.params.freeMode&&!t.params.freeModeSticky&&t.lazy.load()},resize(){const t=this;t.params.lazy.enabled&&t.lazy.load()},scrollbarDragMove(){const t=this;t.params.lazy.enabled&&t.lazy.load()},transitionStart(){const t=this;t.params.lazy.enabled&&(t.params.lazy.loadOnTransitionStart||!t.params.lazy.loadOnTransitionStart&&!t.lazy.initialImageLoaded)&&t.lazy.load()},transitionEnd(){const t=this;t.params.lazy.enabled&&!t.params.lazy.loadOnTransitionStart&&t.lazy.load()},slideChange(){const t=this;t.params.lazy.enabled&&t.params.cssMode&&t.lazy.load()}}},{name:"controller",params:{controller:{control:void 0,inverse:!1,by:"slide"}},create(){const t=this;y.extend(t,{controller:{control:t.params.controller.control,getInterpolateFunction:lt.getInterpolateFunction.bind(t),setTranslate:lt.setTranslate.bind(t),setTransition:lt.setTransition.bind(t)}})},on:{update(){const t=this;t.controller.control&&t.controller.spline&&(t.controller.spline=void 0,delete t.controller.spline)},resize(){const t=this;t.controller.control&&t.controller.spline&&(t.controller.spline=void 0,delete t.controller.spline)},observerUpdate(){const t=this;t.controller.control&&t.controller.spline&&(t.controller.spline=void 0,delete t.controller.spline)},setTranslate(t,e){this.controller.control&&this.controller.setTranslate(t,e)},setTransition(t,e){this.controller.control&&this.controller.setTransition(t,e)}}},{name:"a11y",params:{a11y:{enabled:!0,notificationClass:"swiper-notification",prevSlideMessage:"Previous slide",nextSlideMessage:"Next slide",firstSlideMessage:"This is the first slide",lastSlideMessage:"This is the last slide",paginationBulletMessage:"Go to slide {{index}}"}},create(){const t=this;y.extend(t,{a11y:{liveRegion:h(`<span class="${t.params.a11y.notificationClass}" aria-live="assertive" aria-atomic="true"></span>`)}}),Object.keys(ut).forEach((e=>{t.a11y[e]=ut[e].bind(t)}))},on:{init(){const t=this;t.params.a11y.enabled&&(t.a11y.init(),t.a11y.updateNavigation())},toEdge(){this.params.a11y.enabled&&this.a11y.updateNavigation()},fromEdge(){this.params.a11y.enabled&&this.a11y.updateNavigation()},paginationUpdate(){this.params.a11y.enabled&&this.a11y.updatePagination()},destroy(){this.params.a11y.enabled&&this.a11y.destroy()}}},{name:"history",params:{history:{enabled:!1,replaceState:!1,key:"slides"}},create(){const t=this;y.extend(t,{history:{init:ct.init.bind(t),setHistory:ct.setHistory.bind(t),setHistoryPopState:ct.setHistoryPopState.bind(t),scrollToSlide:ct.scrollToSlide.bind(t),destroy:ct.destroy.bind(t)}})},on:{init(){const t=this;t.params.history.enabled&&t.history.init()},destroy(){const t=this;t.params.history.enabled&&t.history.destroy()},transitionEnd(){const t=this;t.history.initialized&&t.history.setHistory(t.params.history.key,t.activeIndex)},slideChange(){const t=this;t.history.initialized&&t.params.cssMode&&t.history.setHistory(t.params.history.key,t.activeIndex)}}},{name:"hash-navigation",params:{hashNavigation:{enabled:!1,replaceState:!1,watchState:!1}},create(){const t=this;y.extend(t,{hashNavigation:{initialized:!1,init:pt.init.bind(t),destroy:pt.destroy.bind(t),setHash:pt.setHash.bind(t),onHashCange:pt.onHashCange.bind(t)}})},on:{init(){const t=this;t.params.hashNavigation.enabled&&t.hashNavigation.init()},destroy(){const t=this;t.params.hashNavigation.enabled&&t.hashNavigation.destroy()},transitionEnd(){const t=this;t.hashNavigation.initialized&&t.hashNavigation.setHash()},slideChange(){const t=this;t.hashNavigation.initialized&&t.params.cssMode&&t.hashNavigation.setHash()}}},{name:"autoplay",params:{autoplay:{enabled:!1,delay:3e3,waitForTransition:!0,disableOnInteraction:!0,stopOnLastSlide:!1,reverseDirection:!1}},create(){const t=this;y.extend(t,{autoplay:{running:!1,paused:!1,run:ft.run.bind(t),start:ft.start.bind(t),stop:ft.stop.bind(t),pause:ft.pause.bind(t),onVisibilityChange(){"hidden"===document.visibilityState&&t.autoplay.running&&t.autoplay.pause(),"visible"===document.visibilityState&&t.autoplay.paused&&(t.autoplay.run(),t.autoplay.paused=!1)},onTransitionEnd(e){t&&!t.destroyed&&t.$wrapperEl&&e.target===this&&(t.$wrapperEl[0].removeEventListener("transitionend",t.autoplay.onTransitionEnd),t.$wrapperEl[0].removeEventListener("webkitTransitionEnd",t.autoplay.onTransitionEnd),t.autoplay.paused=!1,t.autoplay.running?t.autoplay.run():t.autoplay.stop())}}})},on:{init(){const t=this;t.params.autoplay.enabled&&(t.autoplay.start(),document.addEventListener("visibilitychange",t.autoplay.onVisibilityChange))},beforeTransitionStart(t,e){const n=this;n.autoplay.running&&(e||!n.params.autoplay.disableOnInteraction?n.autoplay.pause(t):n.autoplay.stop())},sliderFirstMove(){const t=this;t.autoplay.running&&(t.params.autoplay.disableOnInteraction?t.autoplay.stop():t.autoplay.pause())},touchEnd(){const t=this;t.params.cssMode&&t.autoplay.paused&&!t.params.autoplay.disableOnInteraction&&t.autoplay.run()},destroy(){const t=this;t.autoplay.running&&t.autoplay.stop(),document.removeEventListener("visibilitychange",t.autoplay.onVisibilityChange)}}},{name:"effect-fade",params:{fadeEffect:{crossFade:!1}},create(){const t=this;y.extend(t,{fadeEffect:{setTranslate:ht.setTranslate.bind(t),setTransition:ht.setTransition.bind(t)}})},on:{beforeInit(){const t=this;if("fade"!==t.params.effect)return;t.classNames.push(`${t.params.containerModifierClass}fade`);const e={slidesPerView:1,slidesPerColumn:1,slidesPerGroup:1,watchSlidesProgress:!0,spaceBetween:0,virtualTranslate:!0};y.extend(t.params,e),y.extend(t.originalParams,e)},setTranslate(){"fade"===this.params.effect&&this.fadeEffect.setTranslate()},setTransition(t){"fade"===this.params.effect&&this.fadeEffect.setTransition(t)}}},{name:"effect-cube",params:{cubeEffect:{slideShadows:!0,shadow:!0,shadowOffset:20,shadowScale:.94}},create(){const t=this;y.extend(t,{cubeEffect:{setTranslate:vt.setTranslate.bind(t),setTransition:vt.setTransition.bind(t)}})},on:{beforeInit(){const t=this;if("cube"!==t.params.effect)return;t.classNames.push(`${t.params.containerModifierClass}cube`),t.classNames.push(`${t.params.containerModifierClass}3d`);const e={slidesPerView:1,slidesPerColumn:1,slidesPerGroup:1,watchSlidesProgress:!0,resistanceRatio:0,spaceBetween:0,centeredSlides:!1,virtualTranslate:!0};y.extend(t.params,e),y.extend(t.originalParams,e)},setTranslate(){"cube"===this.params.effect&&this.cubeEffect.setTranslate()},setTransition(t){"cube"===this.params.effect&&this.cubeEffect.setTransition(t)}}},{name:"effect-flip",params:{flipEffect:{slideShadows:!0,limitRotation:!0}},create(){const t=this;y.extend(t,{flipEffect:{setTranslate:mt.setTranslate.bind(t),setTransition:mt.setTransition.bind(t)}})},on:{beforeInit(){const t=this;if("flip"!==t.params.effect)return;t.classNames.push(`${t.params.containerModifierClass}flip`),t.classNames.push(`${t.params.containerModifierClass}3d`);const e={slidesPerView:1,slidesPerColumn:1,slidesPerGroup:1,watchSlidesProgress:!0,spaceBetween:0,virtualTranslate:!0};y.extend(t.params,e),y.extend(t.originalParams,e)},setTranslate(){"flip"===this.params.effect&&this.flipEffect.setTranslate()},setTransition(t){"flip"===this.params.effect&&this.flipEffect.setTransition(t)}}},{name:"effect-coverflow",params:{coverflowEffect:{rotate:50,stretch:0,depth:100,scale:1,modifier:1,slideShadows:!0}},create(){const t=this;y.extend(t,{coverflowEffect:{setTranslate:gt.setTranslate.bind(t),setTransition:gt.setTransition.bind(t)}})},on:{beforeInit(){const t=this;"coverflow"===t.params.effect&&(t.classNames.push(`${t.params.containerModifierClass}coverflow`),t.classNames.push(`${t.params.containerModifierClass}3d`),t.params.watchSlidesProgress=!0,t.originalParams.watchSlidesProgress=!0)},setTranslate(){"coverflow"===this.params.effect&&this.coverflowEffect.setTranslate()},setTransition(t){"coverflow"===this.params.effect&&this.coverflowEffect.setTransition(t)}}},{name:"thumbs",params:{thumbs:{swiper:null,multipleActiveThumbs:!0,autoScrollOffset:0,slideThumbActiveClass:"swiper-slide-thumb-active",thumbsContainerClass:"swiper-container-thumbs"}},create(){const t=this;y.extend(t,{thumbs:{swiper:null,init:yt.init.bind(t),update:yt.update.bind(t),onThumbClick:yt.onThumbClick.bind(t)}})},on:{beforeInit(){const t=this,{thumbs:e}=t.params;e&&e.swiper&&(t.thumbs.init(),t.thumbs.update(!0))},slideChange(){this.thumbs.swiper&&this.thumbs.update()},update(){this.thumbs.swiper&&this.thumbs.update()},resize(){this.thumbs.swiper&&this.thumbs.update()},observerUpdate(){this.thumbs.swiper&&this.thumbs.update()},setTransition(t){const e=this.thumbs.swiper;e&&e.setTransition(t)},beforeDestroy(){const t=this.thumbs.swiper;t&&this.thumbs.swiperCreated&&t&&t.destroy()}}}];void 0===F.use&&(F.use=F.Class.use,F.installModule=F.Class.installModule),F.use(bt);e.default=F},function(t,e,n){"use strict";n.d(e,"a",(function(){return d}));var r=n(1),o=n(38),l=/^(?:(\w+):)\/\/(?:(\w+)(?::(\w+))?@)([\w.-]+)(?::(\d+))?\/(.+)/,c="Invalid Dsn",d=function(){function t(t){"string"==typeof t?this._fromString(t):this._fromComponents(t),this._validate()}return t.prototype.toString=function(t){void 0===t&&(t=!1);var e=this,n=e.host,path=e.path,r=e.pass,o=e.port,l=e.projectId;return e.protocol+"://"+e.publicKey+(t&&r?":"+r:"")+"@"+n+(o?":"+o:"")+"/"+(path?path+"/":path)+l},t.prototype._fromString=function(t){var e=l.exec(t);if(!e)throw new o.a(c);var n=Object(r.c)(e.slice(1),6),d=n[0],f=n[1],h=n[2],v=void 0===h?"":h,m=n[3],y=n[4],_=void 0===y?"":y,path="",w=n[5],x=w.split("/");if(x.length>1&&(path=x.slice(0,-1).join("/"),w=x.pop()),w){var S=w.match(/^\d+/);S&&(w=S[0])}this._fromComponents({host:m,pass:v,path:path,projectId:w,port:_,protocol:d,publicKey:f})},t.prototype._fromComponents=function(t){"user"in t&&!("publicKey"in t)&&(t.publicKey=t.user),this.user=t.publicKey||"",this.protocol=t.protocol,this.publicKey=t.publicKey||"",this.pass=t.pass||"",this.host=t.host,this.port=t.port||"",this.path=t.path||"",this.projectId=t.projectId},t.prototype._validate=function(){var t=this;if(["protocol","publicKey","host","projectId"].forEach((function(component){if(!t[component])throw new o.a("Invalid Dsn: "+component+" missing")})),!this.projectId.match(/^\d+$/))throw new o.a("Invalid Dsn: Invalid projectId "+this.projectId);if("http"!==this.protocol&&"https"!==this.protocol)throw new o.a("Invalid Dsn: Invalid protocol "+this.protocol);if(this.port&&isNaN(parseInt(this.port,10)))throw new o.a("Invalid Dsn: Invalid port "+this.port)},t}()},function(t,e,n){"use strict";var r;n.d(e,"a",(function(){return r})),function(t){t.Unknown="unknown",t.Skipped="skipped",t.Success="success",t.RateLimit="rate_limit",t.Invalid="invalid",t.Failed="failed"}(r||(r={})),function(t){t.fromHttpCode=function(code){return code>=200&&code<300?t.Success:429===code?t.RateLimit:code>=400&&code<500?t.Invalid:code>=500?t.Failed:t.Unknown}}(r||(r={}))},,function(t,e,n){"use strict";n.d(e,"a",(function(){return r}));var r=function(){function t(){this.name=t.id}return t.prototype.setupOnce=function(e,n){e((function(e){var r=n().getIntegration(t);if(r){try{if(r._shouldDropEvent(e,r._previousEvent))return null}catch(t){return r._previousEvent=e}return r._previousEvent=e}return e}))},t.prototype._shouldDropEvent=function(t,e){return!!e&&(!!this._isSameMessageEvent(t,e)||!!this._isSameExceptionEvent(t,e))},t.prototype._isSameMessageEvent=function(t,e){var n=t.message,r=e.message;return!(!n&&!r)&&(!(n&&!r||!n&&r)&&(n===r&&(!!this._isSameFingerprint(t,e)&&!!this._isSameStacktrace(t,e))))},t.prototype._getFramesFromEvent=function(t){var e=t.exception;if(e)try{return e.values[0].stacktrace.frames}catch(t){return}else if(t.stacktrace)return t.stacktrace.frames},t.prototype._isSameStacktrace=function(t,e){var n=this._getFramesFromEvent(t),r=this._getFramesFromEvent(e);if(!n&&!r)return!0;if(n&&!r||!n&&r)return!1;if(n=n,(r=r).length!==n.length)return!1;for(var i=0;i<r.length;i++){var o=r[i],l=n[i];if(o.filename!==l.filename||o.lineno!==l.lineno||o.colno!==l.colno||o.function!==l.function)return!1}return!0},t.prototype._getExceptionFromEvent=function(t){return t.exception&&t.exception.values&&t.exception.values[0]},t.prototype._isSameExceptionEvent=function(t,e){var n=this._getExceptionFromEvent(e),r=this._getExceptionFromEvent(t);return!(!n||!r)&&(n.type===r.type&&n.value===r.value&&(!!this._isSameFingerprint(t,e)&&!!this._isSameStacktrace(t,e)))},t.prototype._isSameFingerprint=function(t,e){var n=t.fingerprint,r=e.fingerprint;if(!n&&!r)return!0;if(n&&!r||!n&&r)return!1;n=n,r=r;try{return!(n.join("")!==r.join(""))}catch(t){return!1}},t.id="Dedupe",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return d}));var r=n(1),o=n(5),l=n(14),c=n(12),d=function(){function t(e){void 0===e&&(e={depth:3}),this._options=e,this.name=t.id}return t.prototype.setupOnce=function(e,n){e((function(e,r){var o=n().getIntegration(t);return o?o.enhanceEventWithErrorData(e,r):e}))},t.prototype.enhanceEventWithErrorData=function(t,e){var n;if(!e||!e.originalException||!Object(o.d)(e.originalException))return t;var c=e.originalException.name||e.originalException.constructor.name,d=this._extractErrorData(e.originalException);if(d){var f=Object(r.a)({},t.contexts),h=Object(l.d)(d,this._options.depth);return Object(o.h)(h)&&(f=Object(r.a)(Object(r.a)({},t.contexts),((n={})[c]=Object(r.a)({},h),n))),Object(r.a)(Object(r.a)({},t),{contexts:f})}return t},t.prototype._extractErrorData=function(t){var e,n,l=null;try{var d=["name","message","stack","line","column","fileName","lineNumber","columnNumber"],f=Object.getOwnPropertyNames(t).filter((function(t){return-1===d.indexOf(t)}));if(f.length){var h={};try{for(var v=Object(r.f)(f),m=v.next();!m.done;m=v.next()){var y=m.value,_=t[y];Object(o.d)(_)&&(_=_.toString()),h[y]=_}}catch(t){e={error:t}}finally{try{m&&!m.done&&(n=v.return)&&n.call(v)}finally{if(e)throw e.error}}l=h}}catch(t){c.a.error("Unable to extract extra data from the Error object:",t)}return l},t.id="ExtraErrorData",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return d}));var r,o=n(1),l=n(69),c=n(6);!function(t){t.Crash="crash",t.Deprecation="deprecation",t.Intervention="intervention"}(r||(r={}));var d=function(){function t(e){void 0===e&&(e={types:[r.Crash,r.Deprecation,r.Intervention]}),this._options=e,this.name=t.id}return t.prototype.setupOnce=function(t,e){Object(l.f)()&&(this._getCurrentHub=e,new(Object(c.e)().ReportingObserver)(this.handler.bind(this),{buffered:!0,types:this._options.types}).observe())},t.prototype.handler=function(e){var n,l,c=this._getCurrentHub&&this._getCurrentHub();if(c&&c.getIntegration(t)){var d=function(t){c.withScope((function(e){e.setExtra("url",t.url);var label="ReportingObserver ["+t.type+"]",details="No details available";if(t.body){var body,n={};for(var o in t.body)n[o]=t.body[o];if(e.setExtra("body",n),t.type===r.Crash)details=[(body=t.body).crashId||"",body.reason||""].join(" ").trim()||details;else details=(body=t.body).message||details}c.captureMessage(label+": "+details)}))};try{for(var f=Object(o.f)(e),h=f.next();!h.done;h=f.next()){d(h.value)}}catch(t){n={error:t}}finally{try{h&&!h.done&&(l=f.return)&&l.call(f)}finally{if(n)throw n.error}}}},t.id="ReportingObserver",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return l}));var r=n(1),o=n(171),l=function(){function t(e){var n=this;void 0===e&&(e={}),this.name=t.id,this._prefix="app:///",this._iteratee=function(t){if(!t.filename)return t;var e=/^[A-Z]:\\/.test(t.filename),r=/^\//.test(t.filename);if(e||r){var l=e?t.filename.replace(/^[A-Z]:/,"").replace(/\\/g,"/"):t.filename,base=n._root?Object(o.b)(n._root,l):Object(o.a)(l);t.filename=""+n._prefix+base}return t},e.root&&(this._root=e.root),e.prefix&&(this._prefix=e.prefix),e.iteratee&&(this._iteratee=e.iteratee)}return t.prototype.setupOnce=function(e,n){e((function(e){var r=n().getIntegration(t);return r?r.process(e):e}))},t.prototype.process=function(t){var e=t;return t.exception&&Array.isArray(t.exception.values)&&(e=this._processExceptionsEvent(e)),t.stacktrace&&(e=this._processStacktraceEvent(e)),e},t.prototype._processExceptionsEvent=function(t){var e=this;try{return Object(r.a)(Object(r.a)({},t),{exception:Object(r.a)(Object(r.a)({},t.exception),{values:t.exception.values.map((function(t){return Object(r.a)(Object(r.a)({},t),{stacktrace:e._processStacktrace(t.stacktrace)})}))})})}catch(e){return t}},t.prototype._processStacktraceEvent=function(t){try{return Object(r.a)(Object(r.a)({},t),{stacktrace:this._processStacktrace(t.stacktrace)})}catch(e){return t}},t.prototype._processStacktrace=function(t){var e=this;return Object(r.a)(Object(r.a)({},t),{frames:t&&t.frames&&t.frames.map((function(t){return e._iteratee(t)}))})},t.id="RewriteFrames",t}()},function(t,e,n){"use strict";n.d(e,"a",(function(){return w}));var r=n(1),o=n(172),l=n(12),c=n(6),d=n(171),f={id:"Tracing"},h={id:"BrowserTracing"},v={activate:["activated","deactivated"],create:["beforeCreate","created"],destroy:["beforeDestroy","destroyed"],mount:["beforeMount","mounted"],update:["beforeUpdate","updated"]},m=/(?:^|[-_/])(\w)/g,y="root",_="anonymous component",w=function(){function t(e){var n=this;this.name=t.id,this._componentsCache={},this._applyTracingHooks=function(t,e){if(!t.$options.$_sentryPerfHook){t.$options.$_sentryPerfHook=!0;var c=n._getComponentName(t),d=c===y,h={},m=function(r){var l=Object(o.c)();n._rootSpan?n._finishRootSpan(l,e):t.$once("hook:"+r,(function(){var t=e().getIntegration(f);if(t){n._tracingActivity=t.constructor.pushActivity("Vue Application Render");var r=t.constructor.getTransaction();r&&(n._rootSpan=r.startChild({description:"Application Render",op:"Vue"}))}else{var o=function(t){if(t&&t.getScope){var e=t.getScope();if(e)return e.getTransaction()}return}(e());o&&(n._rootSpan=o.startChild({description:"Application Render",op:"Vue"}))}}))},_=function(r,l){var d=Array.isArray(n._options.tracingOptions.trackComponents)?n._options.tracingOptions.trackComponents.indexOf(c)>-1:n._options.tracingOptions.trackComponents;if(n._rootSpan&&d){var f=Object(o.c)(),span=h[l];span?(span.finish(),n._finishRootSpan(f,e)):t.$once("hook:"+r,(function(){n._rootSpan&&(h[l]=n._rootSpan.startChild({description:"Vue <"+c+">",op:l}))}))}};n._options.tracingOptions.hooks.forEach((function(e){var o=v[e];o?o.forEach((function(o){var l=d?m.bind(n,o):_.bind(n,o,e),c=t.$options[o];Array.isArray(c)?t.$options[o]=Object(r.e)([l],c):t.$options[o]="function"==typeof c?[l,c]:[l]})):l.a.warn("Unknown hook: "+e)}))}},l.a.log("You are still using the Vue.js integration, consider moving to @sentry/vue"),this._options=Object(r.a)(Object(r.a)({Vue:Object(c.e)().Vue,attachProps:!0,logErrors:!1,tracing:!1},e),{tracingOptions:Object(r.a)({hooks:["mount","update"],timeout:2e3,trackComponents:!1},e.tracingOptions)})}return t.prototype.setupOnce=function(t,e){this._options.Vue?(this._attachErrorHandler(e),this._options.tracing&&this._startTracing(e)):l.a.error("Vue integration is missing a Vue instance")},t.prototype._getComponentName=function(t){if(!t)return _;if(t.$root===t)return y;if(!t.$options)return _;if(t.$options.name)return t.$options.name;if(t.$options._componentTag)return t.$options._componentTag;if(t.$options.__file){var e=t.$options.__file.replace(/^[a-zA-Z]:/,"").replace(/\\/g,"/"),n=Object(d.a)(e,".vue");return this._componentsCache[n]||(this._componentsCache[n]=n.replace(m,(function(t,e){return e?e.toUpperCase():""})))}return _},t.prototype._finishRootSpan=function(t,e){var n=this;this._rootSpanTimer&&clearTimeout(this._rootSpanTimer),this._rootSpanTimer=setTimeout((function(){if(n._tracingActivity){var r=e().getIntegration(f);r&&r.constructor.popActivity(n._tracingActivity)}n._rootSpan&&n._rootSpan.finish(t)}),this._options.tracingOptions.timeout)},t.prototype._startTracing=function(t){var e=this._applyTracingHooks;this._options.Vue.mixin({beforeCreate:function(){t().getIntegration(f)||t().getIntegration(h)?e(this,t):l.a.error("Vue integration has tracing enabled, but Tracing integration is not configured")}})},t.prototype._attachErrorHandler=function(e){var n=this,r=this._options.Vue.config.errorHandler;this._options.Vue.config.errorHandler=function(o,c,d){var f={};if(c)try{f.componentName=n._getComponentName(c),n._options.attachProps&&(f.propsData=c.$options.propsData)}catch(t){l.a.warn("Unable to extract metadata from Vue component.")}d&&(f.lifecycleHook=d),e().getIntegration(t)&&setTimeout((function(){e().withScope((function(t){t.setContext("vue",f),e().captureException(o)}))})),"function"==typeof r&&r.call(n._options.Vue,o,c,d),n._options.logErrors&&(n._options.Vue.util&&n._options.Vue.util.warn("Error in "+d+': "'+(o&&o.toString())+'"',c),console.error(o))}},t.id="Vue",t}()},function(t,e,n){"use strict";var r,o;n.d(e,"a",(function(){return r})),function(t){t.Ok="ok",t.Exited="exited",t.Crashed="crashed",t.Abnormal="abnormal"}(r||(r={})),function(t){t.Ok="ok",t.Errored="errored",t.Crashed="crashed"}(o||(o={}))}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://gqlg3qh7po-dsn.algolia.net" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://gqlg3qh7po-dsn.algolia.net" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.crisp.chat" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://static.axept.io" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.axept.io" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.crisp.chat" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://client.axept.io" crossorigin="anonymous">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link data-n-head="ssr" rel="preconnect" href="https://static.axept.io" crossorigin="anonymous">`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/inscription](https://www.jeveuxaider.gouv.fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
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

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form form-register-steps el-form--label-top" data-v-50bd1318>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.jeveuxaider.gouv.fr/engagement/" method="get">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="gdpr-privacy-preferences-frm" action="https://www.jeveuxaider.gouv.fr/engagement/wp/wp-admin/admin-post.php">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" class="gdpr-privacy-preferences-frm" action="https://www.jeveuxaider.gouv.fr/engagement/wp/wp-admin/admin-post.php">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="https://www.jeveuxaider.gouv.fr/engagement/" method="get">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/paris](https://www.jeveuxaider.gouv.fr/villes/paris)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form flex flex-wrap sm:flex-no-wrap gap-4 sm:gap-8" data-v-22645a84>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="#" method="GET" class="w-full flex md:ml-0 mb-0" data-v-90efd6ba>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form aria-labelledby="newsletter-headline" class="sm:flex items-start mt-9 max-w-xl" data-v-24f6217e>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form mt-4 el-form--label-top">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="el-form mt-4 el-form--label-top">`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form aria-labelledby="newsletter-headline" class="sm:flex items-start mt-9 max-w-xl" data-v-24f6217e>`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `uncode_privacy[consent_types]`
  
  
  * Evidence: `Set-Cookie: uncode_privacy[consent_types]`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `uncode_privacy[consent_types]`
  
  
  * Evidence: `Set-Cookie: uncode_privacy[consent_types]`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `uncode_privacy[consent_types]`
  
  
  * Evidence: `Set-Cookie: uncode_privacy[consent_types]`
  
  
  
  
Instances: 1
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"676cd577dad930c5","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.7.0","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"676cd5e97e08c9a9","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.7.0","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/610648/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/610648/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"676cd5648d0330c5","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.7.0","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-3.4.1.js`
  
  
  * Evidence: `<script src="https://code.jquery.com/jquery-3.4.1.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-3.4.1.js`
  
  
  * Evidence: `<script src="https://code.jquery.com/jquery-3.4.1.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/presse/](https://www.jeveuxaider.gouv.fr/engagement/presse/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://code.jquery.com/jquery-3.4.1.js`
  
  
  * Evidence: `<script src="https://code.jquery.com/jquery-3.4.1.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://static.cloudflareinsights.com/beacon.min.js`
  
  
  * Evidence: `<script defer src="https://static.cloudflareinsights.com/beacon.min.js" data-cf-beacon='{"rayId":"676cd5874c5130c5","token":"cba5fa8241b048cbb52ececb5e988a18","version":"2021.7.0","si":10}'></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/organisations/](https://www.jeveuxaider.gouv.fr/engagement/organisations/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/610648/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/610648/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `//tag.aticdn.net/610648/smarttag.js`
  
  
  * Evidence: `<script src="//tag.aticdn.net/610648/smarttag.js"></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/69c289c.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/69c289c.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/robots.txt](https://www.jeveuxaider.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=60, public, no-transform`
  
  
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
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

  
  
  
  
### Private IP Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>A private IP (such as 10.x.x.x, 172.x.x.x, 192.168.x.x) or an Amazon EC2 private hostname (for example, ip-10-0-56-78) has been found in the HTTP response body. This information might be helpful for further attacks targeting internal systems.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat/2847/benevolat-france-benevolat-sarthe-le-mans-15](https://www.jeveuxaider.gouv.fr/missions-benevolat/2847/benevolat-france-benevolat-sarthe-le-mans-15)
  
  
  * Method: `GET`
  
  
  * Evidence: `10.48.29.50`
  
  
  
  
Instances: 1
  
### Solution
<p>Remove the private IP address from the HTTP response body.  For comments, use JSP/ASP/PHP comment instead of HTML/JavaScript comment which can be seen by client browsers.</p>
  
### Other information
<p>10.48.29.50</p><p>10.48.29.50</p><p></p>
  
### Reference
* https://tools.ietf.org/html/rfc1918

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/robots.txt](https://www.jeveuxaider.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/uploads/2021/04/logo-benevolat_0003_Calque-2`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `e6e1-7NzgrGepOWyBnCa6qWLSh7Pk+Gc`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `fe8c-k3ZOwapH+fva/5mfUWrFqWVg8ec`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `d913-cQP7N96apG/8/NrkPTsZS4BlBoM`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `PHN2ZyB3aWR0aD0iNiIgaGVpZ2h0PSIxMiIgdmlld0JveD0iMCAwIDYgMTIiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik01Ljc3NC42MDJMNC4zMzQuNmMtMS42MTYgMC0yLjY2IDEuMDQzLTIuNjYgMi42NTh2MS4yMjVILjIyNWEuMjIzLjIyMyAwIDAwLS4yMjYuMjJWNi40OGMwIC4xMjIuMTAxLjIyLjIyNi4yMmgxLjQ0N3Y0LjQ4YzAgLjEyMi4xMDIuMjIxLjIyNy4yMjFoMS44ODdhLjIyMy4yMjMgMCAwMC4yMjctLjIyVjYuN2gxLjY5MmEuMjIzLjIyMyAwIDAwLjIyNi0uMjJWNC43MDNhLjIxOC4yMTggMCAwMC0uMDY2LS4xNTYuMjMuMjMgMCAwMC0uMTYtLjA2NUg0LjAxNFYzLjQ0NGMwLS40OTkuMTIyLS43NTIuNzktLjc1MmguOTdBLjIyMy4yMjMgMCAwMDYgMi40NzFWLjgyMWEuMjIzLjIyMyAwIDAwLS4yMjYtLjIyeiIgZmlsbD0iI0JDQkZDMiIvPjwvc3ZnPg==`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `cc7b-9fFzSnbMdPfUw9a3Z/VoMZkyDW0`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `d43f-nUkSyuFt+brS2VfpbuxkRC/VVjc`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>r����hi�?�M��N?��(���z�%j���M�	�j��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `BUG`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bDB\b and was detected in the element starting with: "<script>window.__NUXT__=(function(a,b,c,d,e,f,g,h,i,j,k,l,m,n,o,p,q,r,s,t,u,v,w,x,y,z,A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/regles-de-securite](https://www.jeveuxaider.gouv.fr/regles-de-securite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/register/responsable](https://www.jeveuxaider.gouv.fr/register/responsable)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="underline hover:no-underline mt-4 text-lg cursor-pointer" data-v-fd29cafa>Page précédente</a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a tabindex="-1" href="#" class="inactive-link pushed" data-lb-index="0"><div class="t-entry-visual-overlay"><div class="t-entry-visual-overlay-in style-dark-bg" style="opacity: 0.5;"></div></div>
									<div class="t-overlay-wrap">
										<div class="t-overlay-inner">
											<div class="t-overlay-content">
												<div class="t-overlay-text single-block-padding"></div></div></div></div><img src="https://reserve-civique-wp.s3.amazonaws.com/uploads/2021/04/logo-benevolat_0003_Calque-2.png" width="1000" height="563" alt="" /></a>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-head="ssr" data-hid="gtm-noscript" data-pbody="true"><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5S3DCV6&" height="0" width="0" style="display:none;visibility:hidden" title="gtm"></iframe></noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/d16f1d3.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/d16f1d3.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 126`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/acc6283.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/acc6283.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 128`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/689f76e.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/689f76e.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 126`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/69c289c.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/69c289c.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 126`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/166e631.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/166e631.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 126`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/fbe65c5.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/fbe65c5.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 128`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/css/0884d2c.css](https://www.jeveuxaider.gouv.fr/_nuxt/css/0884d2c.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 126`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/_nuxt/071676e.modern.js](https://www.jeveuxaider.gouv.fr/_nuxt/071676e.modern.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 126`
  
  
  
  
Instances: 8
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/collectivite](https://www.jeveuxaider.gouv.fr/collectivite)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr](https://www.jeveuxaider.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/robots.txt](https://www.jeveuxaider.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/*](https://www.jeveuxaider.gouv.fr/*)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/](https://www.jeveuxaider.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/password-reset](https://www.jeveuxaider.gouv.fr/password-reset)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/sitemap.xml](https://www.jeveuxaider.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/login](https://www.jeveuxaider.gouv.fr/login)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/territoires](https://www.jeveuxaider.gouv.fr/territoires)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=60`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/paris](https://www.jeveuxaider.gouv.fr/villes/paris)
  
  
  * Method: `GET`
  
  
  * Evidence: `0142804342`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lyon](https://www.jeveuxaider.gouv.fr/villes/lyon)
  
  
  * Method: `GET`
  
  
  * Evidence: `195173227`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lille](https://www.jeveuxaider.gouv.fr/villes/lille)
  
  
  * Method: `GET`
  
  
  * Evidence: `103533593`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lille](https://www.jeveuxaider.gouv.fr/villes/lille)
  
  
  * Method: `GET`
  
  
  * Evidence: `0366978136`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lille](https://www.jeveuxaider.gouv.fr/villes/lille)
  
  
  * Method: `GET`
  
  
  * Evidence: `637320046`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/marseille](https://www.jeveuxaider.gouv.fr/villes/marseille)
  
  
  * Method: `GET`
  
  
  * Evidence: `0681306516`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/bordeaux](https://www.jeveuxaider.gouv.fr/villes/bordeaux)
  
  
  * Method: `GET`
  
  
  * Evidence: `0757403488`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/](https://www.jeveuxaider.gouv.fr/engagement/ecoles-et-universites/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lille](https://www.jeveuxaider.gouv.fr/villes/lille)
  
  
  * Method: `GET`
  
  
  * Evidence: `195173227`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/bordeaux](https://www.jeveuxaider.gouv.fr/villes/bordeaux)
  
  
  * Method: `GET`
  
  
  * Evidence: `0953046365`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lille](https://www.jeveuxaider.gouv.fr/villes/lille)
  
  
  * Method: `GET`
  
  
  * Evidence: `0139168697`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lille](https://www.jeveuxaider.gouv.fr/villes/lille)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621409209`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lyon](https://www.jeveuxaider.gouv.fr/villes/lyon)
  
  
  * Method: `GET`
  
  
  * Evidence: `1621409209`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lyon](https://www.jeveuxaider.gouv.fr/villes/lyon)
  
  
  * Method: `GET`
  
  
  * Evidence: `637320046`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/villes/lyon](https://www.jeveuxaider.gouv.fr/villes/lyon)
  
  
  * Method: `GET`
  
  
  * Evidence: `103533593`
  
  
  
  
Instances: 15
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0142804342, which evaluates to: 1974-07-11 19:52:22</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=Je%20maintiens%20le%20lien%20avec%20des%20personnes%20fragiles%20isol%C3%A9es](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=Je%20maintiens%20le%20lien%20avec%20des%20personnes%20fragiles%20isol%C3%A9es)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[template_title][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20%C3%A0%20distance)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[type][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27apporte%20une%20aide%20alimentaire%20d%27urgence](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27apporte%20une%20aide%20alimentaire%20d%27urgence)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[template_title][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Mobilisation%20covid-19](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Mobilisation%20covid-19)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[domaines][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Mobilisation%20covid-19](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Bdomaines%5D%5B0%5D=Mobilisation%20covid-19)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[domaines][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20en%20pr%C3%A9sentiel](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btype%5D%5B0%5D=Mission%20en%20pr%C3%A9sentiel)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[type][0]`
  
  
  
  
* URL: [https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27assure%20une%20mission%20de%20mentorat%20pour%20un%20enfant%20ou%20un%20jeune](https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=J%27assure%20une%20mission%20de%20mentorat%20pour%20un%20enfant%20ou%20un%20jeune)
  
  
  * Method: `GET`
  
  
  * Parameter: `refinementList[template_title][0]`
  
  
  
  
Instances: 7
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://www.jeveuxaider.gouv.fr/missions-benevolat?refinementList%5Btemplate_title%5D%5B0%5D=Je%20maintiens%20le%20lien%20avec%20des%20personnes%20fragiles%20isol%C3%A9es</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [input] tag [value] attribute </p><p></p><p>The user input found was:</p><p>refinementList[template_title][0]=Je maintiens le lien avec des personnes fragiles isolées</p><p></p><p>The user-controlled value was:</p><p>je maintiens le lien avec des personnes fragiles isolées</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3
