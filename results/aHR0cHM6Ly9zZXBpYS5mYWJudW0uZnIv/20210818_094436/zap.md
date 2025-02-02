
# ZAP Scanning Report

Generated on Wed, 18 Aug 2021 09:35:55


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 3 |
| Informational | 4 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 3 | 
| Source Code Disclosure - Java | Medium | 1 | 
| X-Frame-Options Header Not Set | Medium | 3 | 
| Incomplete or No Cache-control Header Set | Low | 3 | 
| Permissions Policy Header Not Set | Low | 9 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 4 | 
| Modern Web Application | Informational | 4 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js](https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class s{constructor(e,t){this._parent=e,this._name=t?t.name||"unnamed":"<root>",this._properties=t&&t.properties||{},this._zoneDelegate=new a(this,this._parent&&this._parent._zoneDelegate,t)}static assertZonePatched(){if(e.Promise!==D.ZoneAwarePromise)throw new Error("Zone.js has detected that ZoneAwarePromise `(window|global).Promise` has been overwritten.\nMost likely cause is that a Promise polyfill has been loaded after Zone.js (Polyfilling Promise api is not necessary when zone.js is loaded. If you must load one, do so before loading zone.js.)")}static get root(){let e=s.current;for(;e.parent;)e=e.parent;return e}static get current(){return O.zone}static get currentTask(){return P}static __load_patch(t,i){if(D.hasOwnProperty(t)){if(r)throw Error("Already loaded patch: "+t)}else if(!e["__Zone_disable_"+t]){const r="Zone:"+t;n(r),D[t]=i(e,s,z),o(r,r)}}get parent(){return this._parent}get name(){return this._name}get(e){const t=this.getZoneWith(e);if(t)return t._properties[e]}getZoneWith(e){let t=this;for(;t;){if(t._properties.hasOwnProperty(e))return t;t=t._parent}return null}fork(e){if(!e)throw new Error("ZoneSpec required!");return this._zoneDelegate.fork(this,e)}wrap(e,t){if("function"!=typeof e)throw new Error("Expecting function got: "+e);const n=this._zoneDelegate.intercept(this,e,t),o=this;return function(){return o.runGuarded(n,this,arguments,t)}}run(e,t,n,o){O={parent:O,zone:this};try{return this._zoneDelegate.invoke(this,e,t,n,o)}finally{O=O.parent}}runGuarded(e,t=null,n,o){O={parent:O,zone:this};try{try{return this._zoneDelegate.invoke(this,e,t,n,o)}catch(r){if(this._zoneDelegate.handleError(this,r))throw r}}finally{O=O.parent}}runTask(e,t,n){if(e.zone!=this)throw new Error("A task can only be run in the zone of creation! (Creation: "+(e.zone||m).name+"; Execution: "+this.name+")");if(e.state===k&&(e.type===S||e.type===Z))return;const o=e.state!=v;o&&e._transitionTo(v,b),e.runCount++;const r=P;P=e,O={parent:O,zone:this};try{e.type==Z&&e.data&&!e.data.isPeriodic&&(e.cancelFn=void 0);try{return this._zoneDelegate.invokeTask(this,e,t,n)}catch(s){if(this._zoneDelegate.handleError(this,s))throw s}}finally{e.state!==k&&e.state!==w&&(e.type==S||e.data&&e.data.isPeriodic?o&&e._transitionTo(b,v):(e.runCount=0,this._updateTaskCount(e,-1),o&&e._transitionTo(k,v,k))),O=O.parent,P=r}}scheduleTask(e){if(e.zone&&e.zone!==this){let t=this;for(;t;){if(t===e.zone)throw Error(`can not reschedule task to ${this.name} which is descendants of the original zone ${e.zone.name}`);t=t.parent}}e._transitionTo(y,k);const t=[];e._zoneDelegates=t,e._zone=this;try{e=this._zoneDelegate.scheduleTask(this,e)}catch(n){throw e._transitionTo(w,y,k),this._zoneDelegate.handleError(this,n),n}return e._zoneDelegates===t&&this._updateTaskCount(e,1),e.state==y&&e._transitionTo(b,y),e}scheduleMicroTask(e,t,n,o){return this.scheduleTask(new c(E,e,t,n,o,void 0))}scheduleMacroTask(e,t,n,o,r){return this.scheduleTask(new c(Z,e,t,n,o,r))}scheduleEventTask(e,t,n,o,r){return this.scheduleTask(new c(S,e,t,n,o,r))}cancelTask(e){if(e.zone!=this)throw new Error("A task can only be cancelled in the zone of creation! (Creation: "+(e.zone||m).name+"; Execution: "+this.name+")");e._transitionTo(T,b,v);try{this._zoneDelegate.cancelTask(this,e)}catch(t){throw e._transitionTo(w,T),this._zoneDelegate.handleError(this,t),t}return this._updateTaskCount(e,-1),e._transitionTo(k,T),e.runCount=0,e}_updateTaskCount(e,t){const n=e._zoneDelegates;-1==t&&(e._zoneDelegates=null);for(let o=0;o<n.length;o++)n[o]._updateTaskCount(e.type,t)}}s.__symbol__=I;const i={name:"",onHasTask:(e,t,n,o)=>e.hasTask(n,o),onScheduleTask:(e,t,n,o)=>e.scheduleTask(n,o),onInvokeTask:(e,t,n,o,r,s)=>e.invokeTask(n,o,r,s),onCancelTask:(e,t,n,o)=>e.cancelTask(n,o)};class a{constructor(e,t,n){this._taskCounts={microTask:0,macroTask:0,eventTask:0},this.zone=e,this._parentDelegate=t,this._forkZS=n&&(n&&n.onFork?n:t._forkZS),this._forkDlgt=n&&(n.onFork?t:t._forkDlgt),this._forkCurrZone=n&&(n.onFork?this.zone:t.zone),this._interceptZS=n&&(n.onIntercept?n:t._interceptZS),this._interceptDlgt=n&&(n.onIntercept?t:t._interceptDlgt),this._interceptCurrZone=n&&(n.onIntercept?this.zone:t.zone),this._invokeZS=n&&(n.onInvoke?n:t._invokeZS),this._invokeDlgt=n&&(n.onInvoke?t:t._invokeDlgt),this._invokeCurrZone=n&&(n.onInvoke?this.zone:t.zone),this._handleErrorZS=n&&(n.onHandleError?n:t._handleErrorZS),this._handleErrorDlgt=n&&(n.onHandleError?t:t._handleErrorDlgt),this._handleErrorCurrZone=n&&(n.onHandleError?this.zone:t.zone),this._scheduleTaskZS=n&&(n.onScheduleTask?n:t._scheduleTaskZS),this._scheduleTaskDlgt=n&&(n.onScheduleTask?t:t._scheduleTaskDlgt),this._scheduleTaskCurrZone=n&&(n.onScheduleTask?this.zone:t.zone),this._invokeTaskZS=n&&(n.onInvokeTask?n:t._invokeTaskZS),this._invokeTaskDlgt=n&&(n.onInvokeTask?t:t._invokeTaskDlgt),this._invokeTaskCurrZone=n&&(n.onInvokeTask?this.zone:t.zone),this._cancelTaskZS=n&&(n.onCancelTask?n:t._cancelTaskZS),this._cancelTaskDlgt=n&&(n.onCancelTask?t:t._cancelTaskDlgt),this._cancelTaskCurrZone=n&&(n.onCancelTask?this.zone:t.zone),this._hasTaskZS=null,this._hasTaskDlgt=null,this._hasTaskDlgtOwner=null,this._hasTaskCurrZone=null;const o=n&&n.onHasTask;(o||t&&t._hasTaskZS)&&(this._hasTaskZS=o?n:i,this._hasTaskDlgt=t,this._hasTaskDlgtOwner=this,this._hasTaskCurrZone=e,n.onScheduleTask||(this._scheduleTaskZS=i,this._scheduleTaskDlgt=t,this._scheduleTaskCurrZone=this.zone),n.onInvokeTask||(this._invokeTaskZS=i,this._invokeTaskDlgt=t,this._invokeTaskCurrZone=this.zone),n.onCancelTask||(this._cancelTaskZS=i,this._cancelTaskDlgt=t,this._cancelTaskCurrZone=this.zone))}fork(e,t){return this._forkZS?this._forkZS.onFork(this._forkDlgt,this.zone,e,t):new s(e,t)}intercept(e,t,n){return this._interceptZS?this._interceptZS.onIntercept(this._interceptDlgt,this._interceptCurrZone,e,t,n):t}invoke(e,t,n,o,r){return this._invokeZS?this._invokeZS.onInvoke(this._invokeDlgt,this._invokeCurrZone,e,t,n,o,r):t.apply(n,o)}handleError(e,t){return!this._handleErrorZS||this._handleErrorZS.onHandleError(this._handleErrorDlgt,this._handleErrorCurrZone,e,t)}scheduleTask(e,t){let n=t;if(this._scheduleTaskZS)this._hasTaskZS&&n._zoneDelegates.push(this._hasTaskDlgtOwner),n=this._scheduleTaskZS.onScheduleTask(this._scheduleTaskDlgt,this._scheduleTaskCurrZone,e,t),n||(n=t);else if(t.scheduleFn)t.scheduleFn(t);else{if(t.type!=E)throw new Error("Task is missing scheduleFn.");g(t)}return n}invokeTask(e,t,n,o){return this._invokeTaskZS?this._invokeTaskZS.onInvokeTask(this._invokeTaskDlgt,this._invokeTaskCurrZone,e,t,n,o):t.callback.apply(n,o)}cancelTask(e,t){let n;if(this._cancelTaskZS)n=this._cancelTaskZS.onCancelTask(this._cancelTaskDlgt,this._cancelTaskCurrZone,e,t);else{if(!t.cancelFn)throw Error("Task is not cancelable");n=t.cancelFn(t)}return n}hasTask(e,t){try{this._hasTaskZS&&this._hasTaskZS.onHasTask(this._hasTaskDlgt,this._hasTaskCurrZone,e,t)}catch(n){this.handleError(e,n)}}_updateTaskCount(e,t){const n=this._taskCounts,o=n[e],r=n[e]=o+t;if(r<0)throw new Error("More tasks executed then were scheduled.");0!=o&&0!=r||this.hasTask(this.zone,{microTask:n.microTask>0,macroTask:n.macroTask>0,eventTask:n.eventTask>0,change:e})}}class c{constructor(t,n,o,r,s,i){this._zone=null,this.runCount=0,this._zoneDelegates=null,this._state="notScheduled",this.type=t,this.source=n,this.data=r,this.scheduleFn=s,this.cancelFn=i,this.callback=o;const a=this;this.invoke=t===S&&r&&r.useG?c.invokeTask:function(){return c.invokeTask.call(e,a,this,arguments)}}static invokeTask(e,t,n){e||(e=this),j++;try{return e.runCount++,e.zone.runTask(e,t,n)}finally{1==j&&_(),j--}}get zone(){return this._zone}get state(){return this._state}cancelScheduleRequest(){this._transitionTo(k,y)}_transitionTo(e,t,n){if(this._state!==t&&this._state!==n)throw new Error(`${this.type} '${this.source}': can not transition to '${e}', expecting state '${t}'${n?" or '"+n+"'":""}, was '${this._state}'.`);this._state=e,e==k&&(this._zoneDelegates=null)}toString(){return this.data&&void 0!==this.data.handleId?this.data.handleId.toString():Object.prototype.toString.call(this)}toJSON(){return{type:this.type,state:this.state,source:this.source,zone:this.zone.name,runCount:this.runCount}}}const l=I("setTimeout"),u=I("Promise"),h=I("then");let p,f=[],d=!1;function g(t){if(0===j&&0===f.length)if(p||e[u]&&(p=e[u].resolve(0)),p){let e=p[h];e||(e=p.then),e.call(p,_)}else e[l](_,0);t&&f.push(t)}function _(){if(!d){for(d=!0;f.length;){const t=f;f=[];for(let n=0;n<t.length;n++){const o=t[n];try{o.zone.runTask(o,null,null)}catch(e){z.onUnhandledError(e)}}}z.microtaskDrainDone(),d=!1}}const m={name:"NO ZONE"},k="notScheduled",y="scheduling",b="scheduled",v="running",T="canceling",w="unknown",E="microTask",Z="macroTask",S="eventTask",D={},z={symbol:I,currentZoneFrame:()=>O,onUnhandledError:C,microtaskDrainDone:C,scheduleMicroTask:g,showUncaughtError:()=>!s[I("ignoreConsoleErrorUncaughtError")],patchEventTarget:()=>[],patchOnProperties:C,patchMethod:()=>C,bindArguments:()=>[],patchThen:()=>C,patchMacroTask:()=>C,setNativePromise:e=>{e&&"function"==typeof e.resolve&&(p=e.resolve(0))},patchEventPrototype:()=>C,isIEOrEdge:()=>!1,getGlobalObjects:()=>{},ObjectDefineProperty:()=>C,ObjectGetOwnPropertyDescriptor:()=>{},ObjectCreate:()=>{},ArraySlice:()=>[],patchClass:()=>C,wrapWithCurrentZone:()=>C,filterProperties:()=>[],attachOriginToPatched:()=>C,_redefineProperty:()=>C,patchCallbacks:()=>C};let O={parent:null,zone:new s(null,null)},P=null,j=0;function C(){}function I(e){return"__zone_symbol__"+e}o("Zone","Zone"),e.Zone=s}("undefined"!=typeof window&&window||"undefined"!=typeof self&&self||global),Zone.__load_patch("ZoneAwarePromise",(e,t,n)=>{const o=Object.getOwnPropertyDescriptor,r=Object.defineProperty,s=n.symbol,i=[],a=s("Promise"),c=s("then");n.onUnhandledError=e=>{if(n.showUncaughtError()){const t=e&&e.rejection;t?console.error("Unhandled Promise rejection:",t instanceof Error?t.message:t,"; Zone:",e.zone.name,"; Task:",e.task&&e.task.source,"; Value:",t,t instanceof Error?t.stack:void 0):console.error(e)}},n.microtaskDrainDone=()=>{for(;i.length;)for(;i.length;){const t=i.shift();try{t.zone.runGuarded(()=>{throw t})}catch(e){u(e)}}};const l=s("unhandledPromiseRejectionHandler");function u(e){n.onUnhandledError(e);try{const n=t[l];n&&"function"==typeof n&&n.call(this,e)}catch(o){}}function h(e){return e&&e.then}function p(e){return e}function f(e){return Z.reject(e)}const d=s("state"),g=s("value"),_=s("finally"),m=s("parentPromiseValue"),k=s("parentPromiseState");function y(e,t){return n=>{try{v(e,t,n)}catch(o){v(e,!1,o)}}}const b=s("currentTaskTrace");function v(e,o,s){const a=function(){let e=!1;return function(t){return function(){e||(e=!0,t.apply(null,arguments))}}}();if(e===s)throw new TypeError("Promise resolved with itself");if(null===e[d]){let u=null;try{"object"!=typeof s&&"function"!=typeof s||(u=s&&s.then)}catch(l){return a(()=>{v(e,!1,l)})(),e}if(!1!==o&&s instanceof Z&&s.hasOwnProperty(d)&&s.hasOwnProperty(g)&&null!==s[d])w(s),v(e,s[d],s[g]);else if(!1!==o&&"function"==typeof u)try{u.call(s,a(y(e,o)),a(y(e,!1)))}catch(l){a(()=>{v(e,!1,l)})()}else{e[d]=o;const a=e[g];if(e[g]=s,e[_]===_&&!0===o&&(e[d]=e[k],e[g]=e[m]),!1===o&&s instanceof Error){const e=t.currentTask&&t.currentTask.data&&t.currentTask.data.__creationTrace__;e&&r(s,b,{configurable:!0,enumerable:!1,writable:!0,value:e})}for(let t=0;t<a.length;)E(e,a[t++],a[t++],a[t++],a[t++]);if(0==a.length&&0==o){e[d]=0;try{throw new Error("Uncaught (in promise): "+((c=s)&&c.toString===Object.prototype.toString?(c.constructor&&c.constructor.name||"")+": "+JSON.stringify(c):c?c.toString():Object.prototype.toString.call(c))+(s&&s.stack?"\n"+s.stack:""))}catch(l){const o=l;o.rejection=s,o.promise=e,o.zone=t.current,o.task=t.currentTask,i.push(o),n.scheduleMicroTask()}}}}var c;return e}const T=s("rejectionHandledHandler");function w(e){if(0===e[d]){try{const n=t[T];n&&"function"==typeof n&&n.call(this,{rejection:e[g],promise:e})}catch(n){}e[d]=!1;for(let t=0;t<i.length;t++)e===i[t].promise&&i.splice(t,1)}}function E(e,t,n,o,r){w(e);const s=e[d],i=s?"function"==typeof o?o:p:"function"==typeof r?r:f;t.scheduleMicroTask("Promise.then",()=>{try{const o=e[g],r=n&&_===n[_];r&&(n[m]=o,n[k]=s);const a=t.run(i,void 0,r&&i!==f&&i!==p?[]:[o]);v(n,!0,a)}catch(o){v(n,!1,o)}},n)}class Z{constructor(e){const t=this;if(!(t instanceof Z))throw new Error("Must be an instanceof Promise.");t[d]=null,t[g]=[];try{e&&e(y(t,!0),y(t,!1))}catch(n){v(t,!1,n)}}static toString(){return"function ZoneAwarePromise() { [native code] }"}static resolve(e){return v(new this(null),!0,e)}static reject(e){return v(new this(null),!1,e)}static race(e){let t,n,o=new this((e,o)=>{t=e,n=o});function r(e){t(e)}function s(e){n(e)}for(let i of e)h(i)||(i=this.resolve(i)),i.then(r,s);return o}static all(e){let t,n,o=new this((e,o)=>{t=e,n=o}),r=2,s=0;const i=[];for(let a of e){h(a)||(a=this.resolve(a));const e=s;a.then(n=>{i[e]=n,r--,0===r&&t(i)},n),r++,s++}return r-=2,0===r&&t(i),o}get[Symbol.toStringTag](){return"Promise"}then(e,n){const o=new this.constructor(null),r=t.current;return null==this[d]?this[g].push(r,o,e,n):E(this,r,o,e,n),o}catch(e){return this.then(null,e)}finally(e){const n=new this.constructor(null);n[_]=_;const o=t.current;return null==this[d]?this[g].push(o,n,e,e):E(this,o,n,e,e),n}}Z.resolve=Z.resolve,Z.reject=Z.reject,Z.race=Z.race,Z.all=Z.all;const S=e[a]=e.Promise,D=t.__symbol__("ZoneAwarePromise");let z=o(e,"Promise");z&&!z.configurable||(z&&delete z.writable,z&&delete z.value,z||(z={configurable:!0,enumerable:!0}),z.get=function(){return e[D]?e[D]:e[a]},z.set=function(t){t===Z?e[D]=t:(e[a]=t,t.prototype[c]||P(t),n.setNativePromise(t))},r(e,"Promise",z)),e.Promise=Z;const O=s("thenPatched");function P(e){const t=e.prototype,n=o(t,"then");if(n&&(!1===n.writable||!n.configurable))return;const r=t.then;t[c]=r,e.prototype.then=function(e,t){return new Z((e,t)=>{r.call(this,e,t)}).then(e,t)},e[O]=!0}if(n.patchThen=P,S){P(S);const t=e.fetch;"function"==typeof t&&(e[n.symbol("fetch")]=t,e.fetch=(j=t,function(){let e=j.apply(this,arguments);if(e instanceof Z)return e;let t=e.constructor;return t[O]||P(t),e}))}var j;return Promise[t.__symbol__("uncaughtPromiseErrors")]=i,Z});const n=Object.getOwnPropertyDescriptor,o=Object.defineProperty,r=Object.getPrototypeOf,s=Object.create,i=Array.prototype.slice,a=Zone.__symbol__("addEventListener"),c=Zone.__symbol__("removeEventListener");function l(e,t){return Zone.current.wrap(e,t)}function u(e,t,n,o,r){return Zone.current.scheduleMacroTask(e,t,n,o,r)}const h=Zone.__symbol__,p="undefined"!=typeof window,f=p?window:void 0,d=p&&f||"object"==typeof self&&self||global,g=[null];function _(e,t){for(let n=e.length-1;n>=0;n--)"function"==typeof e[n]&&(e[n]=l(e[n],t+"_"+n));return e}function m(e){return!e||!1!==e.writable&&!("function"==typeof e.get&&void 0===e.set)}const k="undefined"!=typeof WorkerGlobalScope&&self instanceof WorkerGlobalScope,y=!("nw"in d)&&void 0!==d.process&&"[object process]"==={}.toString.call(d.process),b=!y&&!k&&!(!p||!f.HTMLElement),v=void 0!==d.process&&"[object process]"==={}.toString.call(d.process)&&!k&&!(!p||!f.HTMLElement),T={},w=function(e){if(!(e=e||d.event))return;let t=T[e.type];t||(t=T[e.type]=h("ON_PROPERTY"+e.type));const n=this||e.target||d,o=n[t];let r;if(b&&n===f&&"error"===e.type){const t=e;r=o&&o.call(this,t.message,t.filename,t.lineno,t.colno,t.error),!0===r&&e.preventDefault()}else r=o&&o.apply(this,arguments),null==r||r||e.preventDefault();return r};function E(e,t,r){let s=n(e,t);if(!s&&r&&n(r,t)&&(s={enumerable:!0,configurable:!0}),!s||!s.configurable)return;const i=h("on"+t+"patched");if(e.hasOwnProperty(i)&&e[i])return;delete s.writable,delete s.value;const a=s.get,c=s.set,l=t.substr(2);let u=T[l];u||(u=T[l]=h("ON_PROPERTY"+l)),s.set=function(t){let n=this;n||e!==d||(n=d),n&&(n[u]&&n.removeEventListener(l,w),c&&c.apply(n,g),"function"==typeof t?(n[u]=t,n.addEventListener(l,w,!1)):n[u]=null)},s.get=function(){let n=this;if(n||e!==d||(n=d),!n)return null;const o=n[u];if(o)return o;if(a){let e=a&&a.call(this);if(e)return s.set.call(this,e),"function"==typeof n.removeAttribute&&n.removeAttribute(t),e}return null},o(e,t,s),e[i]=!0}function Z(e,t,n){if(t)for(let o=0;o<t.length;o++)E(e,"on"+t[o],n);else{const t=[];for(const n in e)"on"==n.substr(0,2)&&t.push(n);for(let o=0;o<t.length;o++)E(e,t[o],n)}}const S=h("originalInstance");function D(e){const t=d[e];if(!t)return;d[h(e)]=t,d[e]=function(){const n=_(arguments,e);switch(n.length){case 0:this[S]=new t;break;case 1:this[S]=new t(n[0]);break;case 2:this[S]=new t(n[0],n[1]);break;case 3:this[S]=new t(n[0],n[1],n[2]);break;case 4:this[S]=new t(n[0],n[1],n[2],n[3]);break;default:throw new Error("Arg list too long.")}},P(d[e],t);const n=new t((function(){}));let r;for(r in n)"XMLHttpRequest"===e&&"responseBlob"===r||function(t){"function"==typeof n[t]?d[e].prototype[t]=function(){return this[S][t].apply(this[S],arguments)}:o(d[e].prototype,t,{set:function(n){"function"==typeof n?(this[S][t]=l(n,e+"."+t),P(this[S][t],n)):this[S][t]=n},get:function(){return this[S][t]}})}(r);for(r in t)"prototype"!==r&&t.hasOwnProperty(r)&&(d[e][r]=t[r])}function z(e,t,o){let s=e;for(;s&&!s.hasOwnProperty(t);)s=r(s);!s&&e[t]&&(s=e);const i=h(t);let a=null;if(s&&!(a=s[i])&&(a=s[i]=s[t],m(s&&n(s,t)))){const e=o(a,i,t);s[t]=function(){return e(this,arguments)},P(s[t],a)}return a}function O(e,t,n){let o=null;function r(e){const t=e.data;return t.args[t.cbIdx]=function(){e.invoke.apply(this,arguments)},o.apply(t.target,t.args),e}o=z(e,t,e=>function(t,o){const s=n(t,o);return s.cbIdx>=0&&"function"==typeof o[s.cbIdx]?u(s.name,o[s.cbIdx],s,r):e.apply(t,o)})}function P(e,t){e[h("OriginalDelegate")]=t}let j=!1,C=!1;function I(){try{const e=f.navigator.userAgent;if(-1!==e.indexOf("MSIE ")||-1!==e.indexOf("Trident/"))return!0}catch(e){}return!1}function L(){if(j)return C;j=!0;try{const e=f.navigator.userAgent;-1===e.indexOf("MSIE ")&&-1===e.indexOf("Trident/")&&-1===e.indexOf("Edge/")||(C=!0)}catch(e){}return C}Zone.__load_patch("toString",e=>{const t=Function.prototype.toString,n=h("OriginalDelegate"),o=h("Promise"),r=h("Error"),s=function(){if("function"==typeof this){const s=this[n];if(s)return"function"==typeof s?t.call(s):Object.prototype.toString.call(s);if(this===Promise){const n=e[o];if(n)return t.call(n)}if(this===Error){const n=e[r];if(n)return t.call(n)}}return t.call(this)};s[n]=t,Function.prototype.toString=s;const i=Object.prototype.toString;Object.prototype.toString=function(){return this instanceof Promise?"[object Promise]":i.call(this)}});let R=!1;if("undefined"!=typeof window)try{const e=Object.defineProperty({},"passive",{get:function(){R=!0}});window.addEventListener("test",e,e),window.removeEventListener("test",e,e)}catch(ge){R=!1}const x={useG:!0},M={},N={},A=/^__zone_symbol__(\w+)(true|false)$/;function F(e,t,n){const o=n&&n.add||"addEventListener",s=n&&n.rm||"removeEventListener",i=n&&n.listeners||"eventListeners",a=n&&n.rmAll||"removeAllListeners",c=h(o),l="."+o+":",u=function(e,t,n){if(e.isRemoved)return;const o=e.callback;"object"==typeof o&&o.handleEvent&&(e.callback=e=>o.handleEvent(e),e.originalDelegate=o),e.invoke(e,t,[n]);const r=e.options;r&&"object"==typeof r&&r.once&&t[s].call(t,n.type,e.originalDelegate?e.originalDelegate:e.callback,r)},p=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,o=n[M[t.type].false];if(o)if(1===o.length)u(o[0],n,t);else{const e=o.slice();for(let o=0;o<e.length&&(!t||!0!==t.__zone_symbol__propagationStopped);o++)u(e[o],n,t)}},f=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,o=n[M[t.type].true];if(o)if(1===o.length)u(o[0],n,t);else{const e=o.slice();for(let o=0;o<e.length&&(!t||!0!==t.__zone_symbol__propagationStopped);o++)u(e[o],n,t)}};function d(t,n){if(!t)return!1;let u=!0;n&&void 0!==n.useG&&(u=n.useG);const d=n&&n.vh;let g=!0;n&&void 0!==n.chkDup&&(g=n.chkDup);let _=!1;n&&void 0!==n.rt&&(_=n.rt);let m=t;for(;m&&!m.hasOwnProperty(o);)m=r(m);if(!m&&t[o]&&(m=t),!m)return!1;if(m[c])return!1;const k=n&&n.eventNameToString,b={},v=m[c]=m[o],T=m[h(s)]=m[s],w=m[h(i)]=m[i],E=m[h(a)]=m[a];let Z;function S(e){R||"boolean"==typeof b.options||null==b.options||(e.options=!!b.options.capture,b.options=e.options)}n&&n.prepend&&(Z=m[h(n.prepend)]=m[n.prepend]);const D=u?function(e){if(!b.isExisting)return S(e),v.call(b.target,b.eventName,b.capture?f:p,b.options)}:function(e){return S(e),v.call(b.target,b.eventName,e.invoke,b.options)},z=u?function(e){if(!e.isRemoved){const t=M[e.eventName];let n;t&&(n=t[e.capture?"true":"false"]);const o=n&&e.target[n];if(o)for(let r=0;r<o.length;r++)if(o[r]===e){o.splice(r,1),e.isRemoved=!0,0===o.length&&(e.allRemoved=!0,e.target[n]=null);break}}if(e.allRemoved)return T.call(e.target,e.eventName,e.capture?f:p,e.options)}:function(e){return T.call(e.target,e.eventName,e.invoke,e.options)},O=n&&n.diff?n.diff:function(e,t){const n=typeof t;return"function"===n&&e.callback===t||"object"===n&&e.originalDelegate===t},j=Zone[Zone.__symbol__("BLACK_LISTED_EVENTS")],C=function(t,n,o,r,s=!1,i=!1){return function(){const a=this||e,c=arguments[0];let l=arguments[1];if(!l)return t.apply(this,arguments);if(y&&"uncaughtException"===c)return t.apply(this,arguments);let h=!1;if("function"!=typeof l){if(!l.handleEvent)return t.apply(this,arguments);h=!0}if(d&&!d(t,l,a,arguments))return;const p=arguments[2];if(j)for(let e=0;e<j.length;e++)if(c===j[e])return t.apply(this,arguments);let f,_=!1;void 0===p?f=!1:!0===p?f=!0:!1===p?f=!1:(f=!!p&&!!p.capture,_=!!p&&!!p.once);const m=Zone.current,v=M[c];let T;if(v)T=v[f?"true":"false"];else{const e="__zone_symbol__"+(k?k(c):c)+"false",t="__zone_symbol__"+(k?k(c):c)+"true";M[c]={},M[c].false=e,M[c].true=t,T=f?t:e}let w,E=a[T],Z=!1;if(E){if(Z=!0,g)for(let e=0;e<E.length;e++)if(O(E[e],l))return}else E=a[T]=[];const S=a.constructor.name,D=N[S];D&&(w=D[c]),w||(w=S+n+(k?k(c):c)),b.options=p,_&&(b.options.once=!1),b.target=a,b.capture=f,b.eventName=c,b.isExisting=Z;const z=u?x:void 0;z&&(z.taskData=b);const P=m.scheduleEventTask(w,l,z,o,r);return b.target=null,z&&(z.taskData=null),_&&(p.once=!0),(R||"boolean"!=typeof P.options)&&(P.options=p),P.target=a,P.capture=f,P.eventName=c,h&&(P.originalDelegate=l),i?E.unshift(P):E.push(P),s?a:void 0}};return m[o]=C(v,l,D,z,_),Z&&(m.prependListener=C(Z,".prependListener:",(function(e){return Z.call(b.target,b.eventName,e.invoke,b.options)}),z,_,!0)),m[s]=function(){const t=this||e,n=arguments[0],o=arguments[2];let r;r=void 0!==o&&(!0===o||!1!==o&&!!o&&!!o.capture);const s=arguments[1];if(!s)return T.apply(this,arguments);if(d&&!d(T,s,t,arguments))return;const i=M[n];let a;i&&(a=i[r?"true":"false"]);const c=a&&t[a];if(c)for(let e=0;e<c.length;e++){const n=c[e];if(O(n,s))return c.splice(e,1),n.isRemoved=!0,0===c.length&&(n.allRemoved=!0,t[a]=null),n.zone.cancelTask(n),_?t:void 0}return T.apply(this,arguments)},m[i]=function(){const t=this||e,n=arguments[0],o=[],r=H(t,k?k(n):n);for(let e=0;e<r.length;e++){const t=r[e];o.push(t.originalDelegate?t.originalDelegate:t.callback)}return o},m[a]=function(){const t=this||e,n=arguments[0];if(n){const e=M[n];if(e){const o=t[e.false],r=t[e.true];if(o){const e=o.slice();for(let t=0;t<e.length;t++){const o=e[t];this[s].call(this,n,o.originalDelegate?o.originalDelegate:o.callback,o.options)}}if(r){const e=r.slice();for(let t=0;t<e.length;t++){const o=e[t];this[s].call(this,n,o.originalDelegate?o.originalDelegate:o.callback,o.options)}}}}else{const e=Object.keys(t);for(let t=0;t<e.length;t++){const n=A.exec(e[t]);let o=n&&n[1];o&&"removeListener"!==o&&this[a].call(this,o)}this[a].call(this,"removeListener")}if(_)return this},P(m[o],v),P(m[s],T),E&&P(m[a],E),w&&P(m[i],w),!0}let g=[];for(let r=0;r<t.length;r++)g[r]=d(t[r],n);return g}function H(e,t){const n=[];for(let o in e){const r=A.exec(o);let s=r&&r[1];if(s&&(!t||s===t)){const t=e[o];if(t)for(let e=0;e<t.length;e++)n.push(t[e])}}return n}function B(e,t){const n=e.Event;n&&n.prototype&&t.patchMethod(n.prototype,"stopImmediatePropagation",e=>function(t,n){t.__zone_symbol__propagationStopped=!0,e&&e.apply(t,n)})}function G(e,t,n,o,r){const s=Zone.__symbol__(o);if(t[s])return;const i=t[s]=t[o];t[o]=function(s,a,c){return a&&a.prototype&&r.forEach((function(t){const r=`${n}.${o}::`+t,s=a.prototype;if(s.hasOwnProperty(t)){const n=e.ObjectGetOwnPropertyDescriptor(s,t);n&&n.value?(n.value=e.wrapWithCurrentZone(n.value,r),e._redefineProperty(a.prototype,t,n)):s[t]&&(s[t]=e.wrapWithCurrentZone(s[t],r))}else s[t]&&(s[t]=e.wrapWithCurrentZone(s[t],r))})),i.call(t,s,a,c)},e.attachOriginToPatched(t[o],i)}const q=Zone.__symbol__,$=Object[q("defineProperty")]=Object.defineProperty,U=Object[q("getOwnPropertyDescriptor")]=Object.getOwnPropertyDescriptor,W=Object.create,V=q("unconfigurables");function X(e,t,n){const o=n.configurable;return K(e,t,n=Y(e,t,n),o)}function J(e,t){return e&&e[V]&&e[V][t]}function Y(e,t,n){return Object.isFrozen(n)||(n.configurable=!0),n.configurable||(e[V]||Object.isFrozen(e)||$(e,V,{writable:!0,value:{}}),e[V]&&(e[V][t]=!0)),n}function K(e,t,n,o){try{return $(e,t,n)}catch(r){if(!n.configurable)throw r;void 0===o?delete n.configurable:n.configurable=o;try{return $(e,t,n)}catch(r){let o=null;try{o=JSON.stringify(n)}catch(r){o=n.toString()}console.log(`Attempting to configure '${t}' with descriptor '${o}' on object '${e}' and got error, giving up: ${r}`)}}}const Q=["absolutedeviceorientation","afterinput","afterprint","appinstalled","beforeinstallprompt","beforeprint","beforeunload","devicelight","devicemotion","deviceorientation","deviceorientationabsolute","deviceproximity","hashchange","languagechange","message","mozbeforepaint","offline","online","paint","pageshow","pagehide","popstate","rejectionhandled","storage","unhandledrejection","unload","userproximity","vrdisplyconnected","vrdisplaydisconnected","vrdisplaypresentchange"],ee=["encrypted","waitingforkey","msneedkey","mozinterruptbegin","mozinterruptend"],te=["load"],ne=["blur","error","focus","load","resize","scroll","messageerror"],oe=["bounce","finish","start"],re=["loadstart","progress","abort","error","load","progress","timeout","loadend","readystatechange"],se=["upgradeneeded","complete","abort","success","error","blocked","versionchange","close"],ie=["close","error","open","message"],ae=["error","message"],ce=["abort","animationcancel","animationend","animationiteration","auxclick","beforeinput","blur","cancel","canplay","canplaythrough","change","compositionstart","compositionupdate","compositionend","cuechange","click","close","contextmenu","curechange","dblclick","drag","dragend","dragenter","dragexit","dragleave","dragover","drop","durationchange","emptied","ended","error","focus","focusin","focusout","gotpointercapture","input","invalid","keydown","keypress","keyup","load","loadstart","loadeddata","loadedmetadata","lostpointercapture","mousedown","mouseenter","mouseleave","mousemove","mouseout","mouseover","mouseup","mousewheel","orientationchange","pause","play","playing","pointercancel","pointerdown","pointerenter","pointerleave","pointerlockchange","mozpointerlockchange","webkitpointerlockerchange","pointerlockerror","mozpointerlockerror","webkitpointerlockerror","pointermove","pointout","pointerover","pointerup","progress","ratechange","reset","resize","scroll","seeked","seeking","select","selectionchange","selectstart","show","sort","stalled","submit","suspend","timeupdate","volumechange","touchcancel","touchmove","touchstart","touchend","transitioncancel","transitionend","waiting","wheel"].concat(["webglcontextrestored","webglcontextlost","webglcontextcreationerror"],["autocomplete","autocompleteerror"],["toggle"],["afterscriptexecute","beforescriptexecute","DOMContentLoaded","freeze","fullscreenchange","mozfullscreenchange","webkitfullscreenchange","msfullscreenchange","fullscreenerror","mozfullscreenerror","webkitfullscreenerror","msfullscreenerror","readystatechange","visibilitychange","resume"],Q,["beforecopy","beforecut","beforepaste","copy","cut","paste","dragstart","loadend","animationstart","search","transitionrun","transitionstart","webkitanimationend","webkitanimationiteration","webkitanimationstart","webkittransitionend"],["activate","afterupdate","ariarequest","beforeactivate","beforedeactivate","beforeeditfocus","beforeupdate","cellchange","controlselect","dataavailable","datasetchanged","datasetcomplete","errorupdate","filterchange","layoutcomplete","losecapture","move","moveend","movestart","propertychange","resizeend","resizestart","rowenter","rowexit","rowsdelete","rowsinserted","command","compassneedscalibration","deactivate","help","mscontentzoom","msmanipulationstatechanged","msgesturechange","msgesturedoubletap","msgestureend","msgesturehold","msgesturestart","msgesturetap","msgotpointercapture","msinertiastart","mslostpointercapture","mspointercancel","mspointerdown","mspointerenter","mspointerhover","mspointerleave","mspointermove","mspointerout","mspointerover","mspointerup","pointerout","mssitemodejumplistitemremoved","msthumbnailclick","stop","storagecommit"]);function le(e,t,n){if(!n||0===n.length)return t;const o=n.filter(t=>t.target===e);if(!o||0===o.length)return t;const r=o[0].ignoreProperties;return t.filter(e=>-1===r.indexOf(e))}function ue(e,t,n,o){e&&Z(e,le(e,t,n),o)}function he(e,t){if(y&&!v)return;if(Zone[e.symbol("patchEvents")])return;const n="undefined"!=typeof WebSocket,o=t.__Zone_ignore_on_properties;if(b){const e=window,t=I?[{target:e,ignoreProperties:["error"]}]:[];ue(e,ce.concat(["messageerror"]),o?o.concat(t):o,r(e)),ue(Document.prototype,ce,o),void 0!==e.SVGElement&&ue(e.SVGElement.prototype,ce,o),ue(Element.prototype,ce,o),ue(HTMLElement.prototype,ce,o),ue(HTMLMediaElement.prototype,ee,o),ue(HTMLFrameSetElement.prototype,Q.concat(ne),o),ue(HTMLBodyElement.prototype,Q.concat(ne),o),ue(HTMLFrameElement.prototype,te,o),ue(HTMLIFrameElement.prototype,te,o);const n=e.HTMLMarqueeElement;n&&ue(n.prototype,oe,o);const s=e.Worker;s&&ue(s.prototype,ae,o)}const s=t.XMLHttpRequest;s&&ue(s.prototype,re,o);const i=t.XMLHttpRequestEventTarget;i&&ue(i&&i.prototype,re,o),"undefined"!=typeof IDBIndex&&(ue(IDBIndex.prototype,se,o),ue(IDBRequest.prototype,se,o),ue(IDBOpenDBRequest.prototype,se,o),ue(IDBDatabase.prototype,se,o),ue(IDBTransaction.prototype,se,o),ue(IDBCursor.prototype,se,o)),n&&ue(WebSocket.prototype,ie,o)}Zone.__load_patch("util",(e,t,r)=>{r.patchOnProperties=Z,r.patchMethod=z,r.bindArguments=_,r.patchMacroTask=O;const a=t.__symbol__("BLACK_LISTED_EVENTS"),c=t.__symbol__("UNPATCHED_EVENTS");e[c]&&(e[a]=e[c]),e[a]&&(t[a]=t[c]=e[a]),r.patchEventPrototype=B,r.patchEventTarget=F,r.isIEOrEdge=L,r.ObjectDefineProperty=o,r.ObjectGetOwnPropertyDescriptor=n,r.ObjectCreate=s,r.ArraySlice=i,r.patchClass=D,r.wrapWithCurrentZone=l,r.filterProperties=le,r.attachOriginToPatched=P,r._redefineProperty=X,r.patchCallbacks=G,r.getGlobalObjects=()=>({globalSources:N,zoneSymbolEventNames:M,eventNames:ce,isBrowser:b,isMix:v,isNode:y,TRUE_STR:"true",FALSE_STR:"false",ZONE_SYMBOL_PREFIX:"__zone_symbol__",ADD_EVENT_LISTENER_STR:"addEventListener",REMOVE_EVENT_LISTENER_STR:"removeEventListener"})});const pe=h("zoneTask");function fe(e,t,n,o){let r=null,s=null;n+=o;const i={};function a(t){const n=t.data;return n.args[0]=function(){try{t.invoke.apply(this,arguments)}finally{t.data&&t.data.isPeriodic||("number"==typeof n.handleId?delete i[n.handleId]:n.handleId&&(n.handleId[pe]=null))}},n.handleId=r.apply(e,n.args),t}function c(e){return s(e.data.handleId)}r=z(e,t+=o,n=>function(r,s){if("function"==typeof s[0]){const e=u(t,s[0],{isPeriodic:"Interval"===o,delay:"Timeout"===o||"Interval"===o?s[1]||0:void 0,args:s},a,c);if(!e)return e;const n=e.data.handleId;return"number"==typeof n?i[n]=e:n&&(n[pe]=e),n&&n.ref&&n.unref&&"function"==typeof n.ref&&"function"==typeof n.unref&&(e.ref=n.ref.bind(n),e.unref=n.unref.bind(n)),"number"==typeof n||n?n:e}return n.apply(e,s)}),s=z(e,n,t=>function(n,o){const r=o[0];let s;"number"==typeof r?s=i[r]:(s=r&&r[pe],s||(s=r)),s&&"string"==typeof s.type?"notScheduled"!==s.state&&(s.cancelFn&&s.data.isPeriodic||0===s.runCount)&&("number"==typeof r?delete i[r]:r&&(r[pe]=null),s.zone.cancelTask(s)):t.apply(e,o)})}function de(e,t){if(Zone[t.symbol("patchEventTarget")])return;const{eventNames:n,zoneSymbolEventNames:o,TRUE_STR:r,FALSE_STR:s,ZONE_SYMBOL_PREFIX:i}=t.getGlobalObjects();for(let c=0;c<n.length;c++){const e=n[c],t=i+(e+s),a=i+(e+r);o[e]={},o[e][s]=t,o[e][r]=a}const a=e.EventTarget;return a&&a.prototype?(t.patchEventTarget(e,[a&&a.prototype]),!0):void 0}Zone.__load_patch("legacy",e=>{const t=e[Zone.__symbol__("legacyPatch")];t&&t()}),Zone.__load_patch("timers",e=>{fe(e,"set","clear","Timeout"),fe(e,"set","clear","Interval"),fe(e,"set","clear","Immediate")}),Zone.__load_patch("requestAnimationFrame",e=>{fe(e,"request","cancel","AnimationFrame"),fe(e,"mozRequest","mozCancel","AnimationFrame"),fe(e,"webkitRequest","webkitCancel","AnimationFrame")}),Zone.__load_patch("blocking",(e,t)=>{const n=["alert","prompt","confirm"];for(let o=0;o<n.length;o++)z(e,n[o],(n,o,r)=>function(o,s){return t.current.run(n,e,s,r)})}),Zone.__load_patch("EventTarget",(e,t,n)=>{!function(e,t){t.patchEventPrototype(e,t)}(e,n),de(e,n);const o=e.XMLHttpRequestEventTarget;o&&o.prototype&&n.patchEventTarget(e,[o.prototype]),D("MutationObserver"),D("WebKitMutationObserver"),D("IntersectionObserver"),D("FileReader")}),Zone.__load_patch("on_property",(e,t,n)=>{he(n,e),Object.defineProperty=function(e,t,n){if(J(e,t))throw new TypeError("Cannot assign to read only property '"+t+"' of "+e);const o=n.configurable;return"prototype"!==t&&(n=Y(e,t,n)),K(e,t,n,o)},Object.defineProperties=function(e,t){return Object.keys(t).forEach((function(n){Object.defineProperty(e,n,t[n])})),e},Object.create=function(e,t){return"object"!=typeof t||Object.isFrozen(t)||Object.keys(t).forEach((function(n){t[n]=Y(e,n,t[n])})),W(e,t)},Object.getOwnPropertyDescriptor=function(e,t){const n=U(e,t);return n&&J(e,t)&&(n.configurable=!1),n}}),Zone.__load_patch("customElements",(e,t,n)=>{!function(e,t){const{isBrowser:n,isMix:o}=t.getGlobalObjects();(n||o)&&e.customElements&&"customElements"in e&&t.patchCallbacks(t,e.customElements,"customElements","define",["connectedCallback","disconnectedCallback","adoptedCallback","attributeChangedCallback"])}(e,n)}),Zone.__load_patch("XHR",(e,t)=>{!function(e){const p=e.XMLHttpRequest;if(!p)return;const f=p.prototype;let d=f[a],g=f[c];if(!d){const t=e.XMLHttpRequestEventTarget;if(t){const e=t.prototype;d=e[a],g=e[c]}}function _(e){const t=e.data,o=t.target;o[s]=!1,o[l]=!1;const i=o[r];d||(d=o[a],g=o[c]),i&&g.call(o,"readystatechange",i);const u=o[r]=()=>{if(o.readyState===o.DONE)if(!t.aborted&&o[s]&&"scheduled"===e.state){const n=o.__zone_symbol__loadfalse;if(n&&n.length>0){const r=e.invoke;e.invoke=function(){const n=o.__zone_symbol__loadfalse;for(let t=0;t<n.length;t++)n[t]===e&&n.splice(t,1);t.aborted||"scheduled"!==e.state||r.call(e)},n.push(e)}else e.invoke()}else t.aborted||!1!==o[s]||(o[l]=!0)};return d.call(o,"readystatechange",u),o[n]||(o[n]=e),T.apply(o,t.args),o[s]=!0,e}function m(){}function k(e){const t=e.data;return t.aborted=!0,w.apply(t.target,t.args)}const y=z(f,"open",()=>function(e,t){return e[o]=0==t[2],e[i]=t[1],y.apply(e,t)}),b=h("fetchTaskAborting"),v=h("fetchTaskScheduling"),T=z(f,"send",()=>function(e,n){if(!0===t.current[v])return T.apply(e,n);if(e[o])return T.apply(e,n);{const t={target:e,url:e[i],isPeriodic:!1,args:n,aborted:!1},o=u("XMLHttpRequest.send",m,t,_,k);e&&!0===e[l]&&!t.aborted&&"scheduled"===o.state&&o.invoke()}}),w=z(f,"abort",()=>function(e,o){const r=e[n];if(r&&"string"==typeof r.type){if(null==r.cancelFn||r.data&&r.data.aborted)return;r.zone.cancelTask(r)}else if(!0===t.current[b])return w.apply(e,o)})}(e);const n=h("xhrTask"),o=h("xhrSync"),r=h("xhrListener"),s=h("xhrScheduled"),i=h("xhrURL"),l=h("xhrErrorBeforeScheduled")}),Zone.__load_patch("geolocation",e=>{e.navigator&&e.navigator.geolocation&&function(e,t){const o=e.constructor.name;for(let r=0;r<t.length;r++){const s=t[r],i=e[s];if(i){if(!m(n(e,s)))continue;e[s]=(e=>{const t=function(){return e.apply(this,_(arguments,o+"."+s))};return P(t,e),t})(i)}}}(e.navigator.geolocation,["getCurrentPosition","watchPosition"])}),Zone.__load_patch("PromiseRejectionEvent",(e,t)=>{function n(t){return function(n){H(e,t).forEach(o=>{const r=e.PromiseRejectionEvent;if(r){const e=new r(t,{promise:n.promise,reason:n.rejection});o.invoke(e)}})}}e.PromiseRejectionEvent&&(t[h("unhandledPromiseRejectionHandler")]=n("unhandledrejection"),t[h("rejectionHandledHandler")]=n("rejectionhandled"))})}}`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class s{constructor(e,t){this._parent=e,this._name=t?t.name||"unnamed":"<root>",this._properties=t&&t.properties||{},this._zoneDelegate=new a(this,this._parent&&this._parent._zoneDelegate,t)}static assertZonePatched(){if(e.Promise!==D.ZoneAwarePromise)throw new Error("Zone.js has detected that ZoneAwarePromise `(window|global).Promise` has been overwritten.\nMost likely cause is that a Promise polyfill has been loaded after Zone.js (Polyfilling Promise api is not necessary when zone.js is loaded. If you must load one, do so before loading zone.js.)")}static get root(){let e=s.current;for(;e.parent;)e=e.parent;return e}static get current(){return O.zone}static get currentTask(){return P}static __load_patch(t,i){if(D.hasOwnProperty(t)){if(r)throw Error("Already loaded patch: "+t)}else if(!e["__Zone_disable_"+t]){const r="Zone:"+t;n(r),D[t]=i(e,s,z),o(r,r)}}get parent(){return this._parent}get name(){return this._name}get(e){const t=this.getZoneWith(e);if(t)return t._properties[e]}getZoneWith(e){let t=this;for(;t;){if(t._properties.hasOwnProperty(e))return t;t=t._parent}return null}fork(e){if(!e)throw new Error("ZoneSpec required!");return this._zoneDelegate.fork(this,e)}wrap(e,t){if("function"!=typeof e)throw new Error("Expecting function got: "+e);const n=this._zoneDelegate.intercept(this,e,t),o=this;return function(){return o.runGuarded(n,this,arguments,t)}}run(e,t,n,o){O={parent:O,zone:this};try{return this._zoneDelegate.invoke(this,e,t,n,o)}finally{O=O.parent}}runGuarded(e,t=null,n,o){O={parent:O,zone:this};try{try{return this._zoneDelegate.invoke(this,e,t,n,o)}catch(r){if(this._zoneDelegate.handleError(this,r))throw r}}finally{O=O.parent}}runTask(e,t,n){if(e.zone!=this)throw new Error("A task can only be run in the zone of creation! (Creation: "+(e.zone||m).name+"; Execution: "+this.name+")");if(e.state===k&&(e.type===S||e.type===Z))return;const o=e.state!=v;o&&e._transitionTo(v,b),e.runCount++;const r=P;P=e,O={parent:O,zone:this};try{e.type==Z&&e.data&&!e.data.isPeriodic&&(e.cancelFn=void 0);try{return this._zoneDelegate.invokeTask(this,e,t,n)}catch(s){if(this._zoneDelegate.handleError(this,s))throw s}}finally{e.state!==k&&e.state!==w&&(e.type==S||e.data&&e.data.isPeriodic?o&&e._transitionTo(b,v):(e.runCount=0,this._updateTaskCount(e,-1),o&&e._transitionTo(k,v,k))),O=O.parent,P=r}}scheduleTask(e){if(e.zone&&e.zone!==this){let t=this;for(;t;){if(t===e.zone)throw Error(`can not reschedule task to ${this.name} which is descendants of the original zone ${e.zone.name}`);t=t.parent}}e._transitionTo(y,k);const t=[];e._zoneDelegates=t,e._zone=this;try{e=this._zoneDelegate.scheduleTask(this,e)}catch(n){throw e._transitionTo(w,y,k),this._zoneDelegate.handleError(this,n),n}return e._zoneDelegates===t&&this._updateTaskCount(e,1),e.state==y&&e._transitionTo(b,y),e}scheduleMicroTask(e,t,n,o){return this.scheduleTask(new c(E,e,t,n,o,void 0))}scheduleMacroTask(e,t,n,o,r){return this.scheduleTask(new c(Z,e,t,n,o,r))}scheduleEventTask(e,t,n,o,r){return this.scheduleTask(new c(S,e,t,n,o,r))}cancelTask(e){if(e.zone!=this)throw new Error("A task can only be cancelled in the zone of creation! (Creation: "+(e.zone||m).name+"; Execution: "+this.name+")");e._transitionTo(T,b,v);try{this._zoneDelegate.cancelTask(this,e)}catch(t){throw e._transitionTo(w,T),this._zoneDelegate.handleError(this,t),t}return this._updateTaskCount(e,-1),e._transitionTo(k,T),e.runCount=0,e}_updateTaskCount(e,t){const n=e._zoneDelegates;-1==t&&(e._zoneDelegates=null);for(let o=0;o<n.length;o++)n[o]._updateTaskCount(e.type,t)}}s.__symbol__=I;const i={name:"",onHasTask:(e,t,n,o)=>e.hasTask(n,o),onScheduleTask:(e,t,n,o)=>e.scheduleTask(n,o),onInvokeTask:(e,t,n,o,r,s)=>e.invokeTask(n,o,r,s),onCancelTask:(e,t,n,o)=>e.cancelTask(n,o)};class a{constructor(e,t,n){this._taskCounts={microTask:0,macroTask:0,eventTask:0},this.zone=e,this._parentDelegate=t,this._forkZS=n&&(n&&n.onFork?n:t._forkZS),this._forkDlgt=n&&(n.onFork?t:t._forkDlgt),this._forkCurrZone=n&&(n.onFork?this.zone:t.zone),this._interceptZS=n&&(n.onIntercept?n:t._interceptZS),this._interceptDlgt=n&&(n.onIntercept?t:t._interceptDlgt),this._interceptCurrZone=n&&(n.onIntercept?this.zone:t.zone),this._invokeZS=n&&(n.onInvoke?n:t._invokeZS),this._invokeDlgt=n&&(n.onInvoke?t:t._invokeDlgt),this._invokeCurrZone=n&&(n.onInvoke?this.zone:t.zone),this._handleErrorZS=n&&(n.onHandleError?n:t._handleErrorZS),this._handleErrorDlgt=n&&(n.onHandleError?t:t._handleErrorDlgt),this._handleErrorCurrZone=n&&(n.onHandleError?this.zone:t.zone),this._scheduleTaskZS=n&&(n.onScheduleTask?n:t._scheduleTaskZS),this._scheduleTaskDlgt=n&&(n.onScheduleTask?t:t._scheduleTaskDlgt),this._scheduleTaskCurrZone=n&&(n.onScheduleTask?this.zone:t.zone),this._invokeTaskZS=n&&(n.onInvokeTask?n:t._invokeTaskZS),this._invokeTaskDlgt=n&&(n.onInvokeTask?t:t._invokeTaskDlgt),this._invokeTaskCurrZone=n&&(n.onInvokeTask?this.zone:t.zone),this._cancelTaskZS=n&&(n.onCancelTask?n:t._cancelTaskZS),this._cancelTaskDlgt=n&&(n.onCancelTask?t:t._cancelTaskDlgt),this._cancelTaskCurrZone=n&&(n.onCancelTask?this.zone:t.zone),this._hasTaskZS=null,this._hasTaskDlgt=null,this._hasTaskDlgtOwner=null,this._hasTaskCurrZone=null;const o=n&&n.onHasTask;(o||t&&t._hasTaskZS)&&(this._hasTaskZS=o?n:i,this._hasTaskDlgt=t,this._hasTaskDlgtOwner=this,this._hasTaskCurrZone=e,n.onScheduleTask||(this._scheduleTaskZS=i,this._scheduleTaskDlgt=t,this._scheduleTaskCurrZone=this.zone),n.onInvokeTask||(this._invokeTaskZS=i,this._invokeTaskDlgt=t,this._invokeTaskCurrZone=this.zone),n.onCancelTask||(this._cancelTaskZS=i,this._cancelTaskDlgt=t,this._cancelTaskCurrZone=this.zone))}fork(e,t){return this._forkZS?this._forkZS.onFork(this._forkDlgt,this.zone,e,t):new s(e,t)}intercept(e,t,n){return this._interceptZS?this._interceptZS.onIntercept(this._interceptDlgt,this._interceptCurrZone,e,t,n):t}invoke(e,t,n,o,r){return this._invokeZS?this._invokeZS.onInvoke(this._invokeDlgt,this._invokeCurrZone,e,t,n,o,r):t.apply(n,o)}handleError(e,t){return!this._handleErrorZS||this._handleErrorZS.onHandleError(this._handleErrorDlgt,this._handleErrorCurrZone,e,t)}scheduleTask(e,t){let n=t;if(this._scheduleTaskZS)this._hasTaskZS&&n._zoneDelegates.push(this._hasTaskDlgtOwner),n=this._scheduleTaskZS.onScheduleTask(this._scheduleTaskDlgt,this._scheduleTaskCurrZone,e,t),n||(n=t);else if(t.scheduleFn)t.scheduleFn(t);else{if(t.type!=E)throw new Error("Task is missing scheduleFn.");g(t)}return n}invokeTask(e,t,n,o){return this._invokeTaskZS?this._invokeTaskZS.onInvokeTask(this._invokeTaskDlgt,this._invokeTaskCurrZone,e,t,n,o):t.callback.apply(n,o)}cancelTask(e,t){let n;if(this._cancelTaskZS)n=this._cancelTaskZS.onCancelTask(this._cancelTaskDlgt,this._cancelTaskCurrZone,e,t);else{if(!t.cancelFn)throw Error("Task is not cancelable");n=t.cancelFn(t)}return n}hasTask(e,t){try{this._hasTaskZS&&this._hasTaskZS.onHasTask(this._hasTaskDlgt,this._hasTaskCurrZone,e,t)}catch(n){this.handleError(e,n)}}_updateTaskCount(e,t){const n=this._taskCounts,o=n[e],r=n[e]=o+t;if(r<0)throw new Error("More tasks executed then were scheduled.");0!=o&&0!=r||this.hasTask(this.zone,{microTask:n.microTask>0,macroTask:n.macroTask>0,eventTask:n.eventTask>0,change:e})}}class c{constructor(t,n,o,r,s,i){this._zone=null,this.runCount=0,this._zoneDelegates=null,this._state="notScheduled",this.type=t,this.source=n,this.data=r,this.scheduleFn=s,this.cancelFn=i,this.callback=o;const a=this;this.invoke=t===S&&r&&r.useG?c.invokeTask:function(){return c.invokeTask.call(e,a,this,arguments)}}static invokeTask(e,t,n){e||(e=this),j++;try{return e.runCount++,e.zone.runTask(e,t,n)}finally{1==j&&_(),j--}}get zone(){return this._zone}get state(){return this._state}cancelScheduleRequest(){this._transitionTo(k,y)}_transitionTo(e,t,n){if(this._state!==t&&this._state!==n)throw new Error(`${this.type} '${this.source}': can not transition to '${e}', expecting state '${t}'${n?" or '"+n+"'":""}, was '${this._state}'.`);this._state=e,e==k&&(this._zoneDelegates=null)}toString(){return this.data&&void 0!==this.data.handleId?this.data.handleId.toString():Object.prototype.toString.call(this)}toJSON(){return{type:this.type,state:this.state,source:this.source,zone:this.zone.name,runCount:this.runCount}}}const l=I("setTimeout"),u=I("Promise"),h=I("then");let p,f=[],d=!1;function g(t){if(0===j&&0===f.length)if(p||e[u]&&(p=e[u].resolve(0)),p){let e=p[h];e||(e=p.then),e.call(p,_)}else e[l](_,0);t&&f.push(t)}function _(){if(!d){for(d=!0;f.length;){const t=f;f=[];for(let n=0;n<t.length;n++){const o=t[n];try{o.zone.runTask(o,null,null)}catch(e){z.onUnhandledError(e)}}}z.microtaskDrainDone(),d=!1}}const m={name:"NO ZONE"},k="notScheduled",y="scheduling",b="scheduled",v="running",T="canceling",w="unknown",E="microTask",Z="macroTask",S="eventTask",D={},z={symbol:I,currentZoneFrame:()=>O,onUnhandledError:C,microtaskDrainDone:C,scheduleMicroTask:g,showUncaughtError:()=>!s[I("ignoreConsoleErrorUncaughtError")],patchEventTarget:()=>[],patchOnProperties:C,patchMethod:()=>C,bindArguments:()=>[],patchThen:()=>C,patchMacroTask:()=>C,setNativePromise:e=>{e&&"function"==typeof e.resolve&&(p=e.resolve(0))},patchEventPrototype:()=>C,isIEOrEdge:()=>!1,getGlobalObjects:()=>{},ObjectDefineProperty:()=>C,ObjectGetOwnPropertyDescriptor:()=>{},ObjectCreate:()=>{},ArraySlice:()=>[],patchClass:()=>C,wrapWithCurrentZone:()=>C,filterProperties:()=>[],attachOriginToPatched:()=>C,_redefineProperty:()=>C,patchCallbacks:()=>C};let O={parent:null,zone:new s(null,null)},P=null,j=0;function C(){}function I(e){return"__zone_symbol__"+e}o("Zone","Zone"),e.Zone=s}("undefined"!=typeof window&&window||"undefined"!=typeof self&&self||global),Zone.__load_patch("ZoneAwarePromise",(e,t,n)=>{const o=Object.getOwnPropertyDescriptor,r=Object.defineProperty,s=n.symbol,i=[],a=s("Promise"),c=s("then");n.onUnhandledError=e=>{if(n.showUncaughtError()){const t=e&&e.rejection;t?console.error("Unhandled Promise rejection:",t instanceof Error?t.message:t,"; Zone:",e.zone.name,"; Task:",e.task&&e.task.source,"; Value:",t,t instanceof Error?t.stack:void 0):console.error(e)}},n.microtaskDrainDone=()=>{for(;i.length;)for(;i.length;){const t=i.shift();try{t.zone.runGuarded(()=>{throw t})}catch(e){u(e)}}};const l=s("unhandledPromiseRejectionHandler");function u(e){n.onUnhandledError(e);try{const n=t[l];n&&"function"==typeof n&&n.call(this,e)}catch(o){}}function h(e){return e&&e.then}function p(e){return e}function f(e){return Z.reject(e)}const d=s("state"),g=s("value"),_=s("finally"),m=s("parentPromiseValue"),k=s("parentPromiseState");function y(e,t){return n=>{try{v(e,t,n)}catch(o){v(e,!1,o)}}}const b=s("currentTaskTrace");function v(e,o,s){const a=function(){let e=!1;return function(t){return function(){e||(e=!0,t.apply(null,arguments))}}}();if(e===s)throw new TypeError("Promise resolved with itself");if(null===e[d]){let u=null;try{"object"!=typeof s&&"function"!=typeof s||(u=s&&s.then)}catch(l){return a(()=>{v(e,!1,l)})(),e}if(!1!==o&&s instanceof Z&&s.hasOwnProperty(d)&&s.hasOwnProperty(g)&&null!==s[d])w(s),v(e,s[d],s[g]);else if(!1!==o&&"function"==typeof u)try{u.call(s,a(y(e,o)),a(y(e,!1)))}catch(l){a(()=>{v(e,!1,l)})()}else{e[d]=o;const a=e[g];if(e[g]=s,e[_]===_&&!0===o&&(e[d]=e[k],e[g]=e[m]),!1===o&&s instanceof Error){const e=t.currentTask&&t.currentTask.data&&t.currentTask.data.__creationTrace__;e&&r(s,b,{configurable:!0,enumerable:!1,writable:!0,value:e})}for(let t=0;t<a.length;)E(e,a[t++],a[t++],a[t++],a[t++]);if(0==a.length&&0==o){e[d]=0;try{throw new Error("Uncaught (in promise): "+((c=s)&&c.toString===Object.prototype.toString?(c.constructor&&c.constructor.name||"")+": "+JSON.stringify(c):c?c.toString():Object.prototype.toString.call(c))+(s&&s.stack?"\n"+s.stack:""))}catch(l){const o=l;o.rejection=s,o.promise=e,o.zone=t.current,o.task=t.currentTask,i.push(o),n.scheduleMicroTask()}}}}var c;return e}const T=s("rejectionHandledHandler");function w(e){if(0===e[d]){try{const n=t[T];n&&"function"==typeof n&&n.call(this,{rejection:e[g],promise:e})}catch(n){}e[d]=!1;for(let t=0;t<i.length;t++)e===i[t].promise&&i.splice(t,1)}}function E(e,t,n,o,r){w(e);const s=e[d],i=s?"function"==typeof o?o:p:"function"==typeof r?r:f;t.scheduleMicroTask("Promise.then",()=>{try{const o=e[g],r=n&&_===n[_];r&&(n[m]=o,n[k]=s);const a=t.run(i,void 0,r&&i!==f&&i!==p?[]:[o]);v(n,!0,a)}catch(o){v(n,!1,o)}},n)}class Z{constructor(e){const t=this;if(!(t instanceof Z))throw new Error("Must be an instanceof Promise.");t[d]=null,t[g]=[];try{e&&e(y(t,!0),y(t,!1))}catch(n){v(t,!1,n)}}static toString(){return"function ZoneAwarePromise() { [native code] }"}static resolve(e){return v(new this(null),!0,e)}static reject(e){return v(new this(null),!1,e)}static race(e){let t,n,o=new this((e,o)=>{t=e,n=o});function r(e){t(e)}function s(e){n(e)}for(let i of e)h(i)||(i=this.resolve(i)),i.then(r,s);return o}static all(e){let t,n,o=new this((e,o)=>{t=e,n=o}),r=2,s=0;const i=[];for(let a of e){h(a)||(a=this.resolve(a));const e=s;a.then(n=>{i[e]=n,r--,0===r&&t(i)},n),r++,s++}return r-=2,0===r&&t(i),o}get[Symbol.toStringTag](){return"Promise"}then(e,n){const o=new this.constructor(null),r=t.current;return null==this[d]?this[g].push(r,o,e,n):E(this,r,o,e,n),o}catch(e){return this.then(null,e)}finally(e){const n=new this.constructor(null);n[_]=_;const o=t.current;return null==this[d]?this[g].push(o,n,e,e):E(this,o,n,e,e),n}}Z.resolve=Z.resolve,Z.reject=Z.reject,Z.race=Z.race,Z.all=Z.all;const S=e[a]=e.Promise,D=t.__symbol__("ZoneAwarePromise");let z=o(e,"Promise");z&&!z.configurable||(z&&delete z.writable,z&&delete z.value,z||(z={configurable:!0,enumerable:!0}),z.get=function(){return e[D]?e[D]:e[a]},z.set=function(t){t===Z?e[D]=t:(e[a]=t,t.prototype[c]||P(t),n.setNativePromise(t))},r(e,"Promise",z)),e.Promise=Z;const O=s("thenPatched");function P(e){const t=e.prototype,n=o(t,"then");if(n&&(!1===n.writable||!n.configurable))return;const r=t.then;t[c]=r,e.prototype.then=function(e,t){return new Z((e,t)=>{r.call(this,e,t)}).then(e,t)},e[O]=!0}if(n.patchThen=P,S){P(S);const t=e.fetch;"function"==typeof t&&(e[n.symbol("fetch")]=t,e.fetch=(j=t,function(){let e=j.apply(this,arguments);if(e instanceof Z)return e;let t=e.constructor;return t[O]||P(t),e}))}var j;return Promise[t.__symbol__("uncaughtPromiseErrors")]=i,Z});const n=Object.getOwnPropertyDescriptor,o=Object.defineProperty,r=Object.getPrototypeOf,s=Object.create,i=Array.prototype.slice,a=Zone.__symbol__("addEventListener"),c=Zone.__symbol__("removeEventListener");function l(e,t){return Zone.current.wrap(e,t)}function u(e,t,n,o,r){return Zone.current.scheduleMacroTask(e,t,n,o,r)}const h=Zone.__symbol__,p="undefined"!=typeof window,f=p?window:void 0,d=p&&f||"object"==typeof self&&self||global,g=[null];function _(e,t){for(let n=e.length-1;n>=0;n--)"function"==typeof e[n]&&(e[n]=l(e[n],t+"_"+n));return e}function m(e){return!e||!1!==e.writable&&!("function"==typeof e.get&&void 0===e.set)}const k="undefined"!=typeof WorkerGlobalScope&&self instanceof WorkerGlobalScope,y=!("nw"in d)&&void 0!==d.process&&"[object process]"==={}.toString.call(d.process),b=!y&&!k&&!(!p||!f.HTMLElement),v=void 0!==d.process&&"[object process]"==={}.toString.call(d.process)&&!k&&!(!p||!f.HTMLElement),T={},w=function(e){if(!(e=e||d.event))return;let t=T[e.type];t||(t=T[e.type]=h("ON_PROPERTY"+e.type));const n=this||e.target||d,o=n[t];let r;if(b&&n===f&&"error"===e.type){const t=e;r=o&&o.call(this,t.message,t.filename,t.lineno,t.colno,t.error),!0===r&&e.preventDefault()}else r=o&&o.apply(this,arguments),null==r||r||e.preventDefault();return r};function E(e,t,r){let s=n(e,t);if(!s&&r&&n(r,t)&&(s={enumerable:!0,configurable:!0}),!s||!s.configurable)return;const i=h("on"+t+"patched");if(e.hasOwnProperty(i)&&e[i])return;delete s.writable,delete s.value;const a=s.get,c=s.set,l=t.substr(2);let u=T[l];u||(u=T[l]=h("ON_PROPERTY"+l)),s.set=function(t){let n=this;n||e!==d||(n=d),n&&(n[u]&&n.removeEventListener(l,w),c&&c.apply(n,g),"function"==typeof t?(n[u]=t,n.addEventListener(l,w,!1)):n[u]=null)},s.get=function(){let n=this;if(n||e!==d||(n=d),!n)return null;const o=n[u];if(o)return o;if(a){let e=a&&a.call(this);if(e)return s.set.call(this,e),"function"==typeof n.removeAttribute&&n.removeAttribute(t),e}return null},o(e,t,s),e[i]=!0}function Z(e,t,n){if(t)for(let o=0;o<t.length;o++)E(e,"on"+t[o],n);else{const t=[];for(const n in e)"on"==n.substr(0,2)&&t.push(n);for(let o=0;o<t.length;o++)E(e,t[o],n)}}const S=h("originalInstance");function D(e){const t=d[e];if(!t)return;d[h(e)]=t,d[e]=function(){const n=_(arguments,e);switch(n.length){case 0:this[S]=new t;break;case 1:this[S]=new t(n[0]);break;case 2:this[S]=new t(n[0],n[1]);break;case 3:this[S]=new t(n[0],n[1],n[2]);break;case 4:this[S]=new t(n[0],n[1],n[2],n[3]);break;default:throw new Error("Arg list too long.")}},P(d[e],t);const n=new t((function(){}));let r;for(r in n)"XMLHttpRequest"===e&&"responseBlob"===r||function(t){"function"==typeof n[t]?d[e].prototype[t]=function(){return this[S][t].apply(this[S],arguments)}:o(d[e].prototype,t,{set:function(n){"function"==typeof n?(this[S][t]=l(n,e+"."+t),P(this[S][t],n)):this[S][t]=n},get:function(){return this[S][t]}})}(r);for(r in t)"prototype"!==r&&t.hasOwnProperty(r)&&(d[e][r]=t[r])}function z(e,t,o){let s=e;for(;s&&!s.hasOwnProperty(t);)s=r(s);!s&&e[t]&&(s=e);const i=h(t);let a=null;if(s&&!(a=s[i])&&(a=s[i]=s[t],m(s&&n(s,t)))){const e=o(a,i,t);s[t]=function(){return e(this,arguments)},P(s[t],a)}return a}function O(e,t,n){let o=null;function r(e){const t=e.data;return t.args[t.cbIdx]=function(){e.invoke.apply(this,arguments)},o.apply(t.target,t.args),e}o=z(e,t,e=>function(t,o){const s=n(t,o);return s.cbIdx>=0&&"function"==typeof o[s.cbIdx]?u(s.name,o[s.cbIdx],s,r):e.apply(t,o)})}function P(e,t){e[h("OriginalDelegate")]=t}let j=!1,C=!1;function I(){try{const e=f.navigator.userAgent;if(-1!==e.indexOf("MSIE ")||-1!==e.indexOf("Trident/"))return!0}catch(e){}return!1}function L(){if(j)return C;j=!0;try{const e=f.navigator.userAgent;-1===e.indexOf("MSIE ")&&-1===e.indexOf("Trident/")&&-1===e.indexOf("Edge/")||(C=!0)}catch(e){}return C}Zone.__load_patch("toString",e=>{const t=Function.prototype.toString,n=h("OriginalDelegate"),o=h("Promise"),r=h("Error"),s=function(){if("function"==typeof this){const s=this[n];if(s)return"function"==typeof s?t.call(s):Object.prototype.toString.call(s);if(this===Promise){const n=e[o];if(n)return t.call(n)}if(this===Error){const n=e[r];if(n)return t.call(n)}}return t.call(this)};s[n]=t,Function.prototype.toString=s;const i=Object.prototype.toString;Object.prototype.toString=function(){return this instanceof Promise?"[object Promise]":i.call(this)}});let R=!1;if("undefined"!=typeof window)try{const e=Object.defineProperty({},"passive",{get:function(){R=!0}});window.addEventListener("test",e,e),window.removeEventListener("test",e,e)}catch(ge){R=!1}const x={useG:!0},M={},N={},A=/^__zone_symbol__(\w+)(true|false)$/;function F(e,t,n){const o=n&&n.add||"addEventListener",s=n&&n.rm||"removeEventListener",i=n&&n.listeners||"eventListeners",a=n&&n.rmAll||"removeAllListeners",c=h(o),l="."+o+":",u=function(e,t,n){if(e.isRemoved)return;const o=e.callback;"object"==typeof o&&o.handleEvent&&(e.callback=e=>o.handleEvent(e),e.originalDelegate=o),e.invoke(e,t,[n]);const r=e.options;r&&"object"==typeof r&&r.once&&t[s].call(t,n.type,e.originalDelegate?e.originalDelegate:e.callback,r)},p=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,o=n[M[t.type].false];if(o)if(1===o.length)u(o[0],n,t);else{const e=o.slice();for(let o=0;o<e.length&&(!t||!0!==t.__zone_symbol__propagationStopped);o++)u(e[o],n,t)}},f=function(t){if(!(t=t||e.event))return;const n=this||t.target||e,o=n[M[t.type].true];if(o)if(1===o.length)u(o[0],n,t);else{const e=o.slice();for(let o=0;o<e.length&&(!t||!0!==t.__zone_symbol__propagationStopped);o++)u(e[o],n,t)}};function d(t,n){if(!t)return!1;let u=!0;n&&void 0!==n.useG&&(u=n.useG);const d=n&&n.vh;let g=!0;n&&void 0!==n.chkDup&&(g=n.chkDup);let _=!1;n&&void 0!==n.rt&&(_=n.rt);let m=t;for(;m&&!m.hasOwnProperty(o);)m=r(m);if(!m&&t[o]&&(m=t),!m)return!1;if(m[c])return!1;const k=n&&n.eventNameToString,b={},v=m[c]=m[o],T=m[h(s)]=m[s],w=m[h(i)]=m[i],E=m[h(a)]=m[a];let Z;function S(e){R||"boolean"==typeof b.options||null==b.options||(e.options=!!b.options.capture,b.options=e.options)}n&&n.prepend&&(Z=m[h(n.prepend)]=m[n.prepend]);const D=u?function(e){if(!b.isExisting)return S(e),v.call(b.target,b.eventName,b.capture?f:p,b.options)}:function(e){return S(e),v.call(b.target,b.eventName,e.invoke,b.options)},z=u?function(e){if(!e.isRemoved){const t=M[e.eventName];let n;t&&(n=t[e.capture?"true":"false"]);const o=n&&e.target[n];if(o)for(let r=0;r<o.length;r++)if(o[r]===e){o.splice(r,1),e.isRemoved=!0,0===o.length&&(e.allRemoved=!0,e.target[n]=null);break}}if(e.allRemoved)return T.call(e.target,e.eventName,e.capture?f:p,e.options)}:function(e){return T.call(e.target,e.eventName,e.invoke,e.options)},O=n&&n.diff?n.diff:function(e,t){const n=typeof t;return"function"===n&&e.callback===t||"object"===n&&e.originalDelegate===t},j=Zone[Zone.__symbol__("BLACK_LISTED_EVENTS")],C=function(t,n,o,r,s=!1,i=!1){return function(){const a=this||e,c=arguments[0];let l=arguments[1];if(!l)return t.apply(this,arguments);if(y&&"uncaughtException"===c)return t.apply(this,arguments);let h=!1;if("function"!=typeof l){if(!l.handleEvent)return t.apply(this,arguments);h=!0}if(d&&!d(t,l,a,arguments))return;const p=arguments[2];if(j)for(let e=0;e<j.length;e++)if(c===j[e])return t.apply(this,arguments);let f,_=!1;void 0===p?f=!1:!0===p?f=!0:!1===p?f=!1:(f=!!p&&!!p.capture,_=!!p&&!!p.once);const m=Zone.current,v=M[c];let T;if(v)T=v[f?"true":"false"];else{const e="__zone_symbol__"+(k?k(c):c)+"false",t="__zone_symbol__"+(k?k(c):c)+"true";M[c]={},M[c].false=e,M[c].true=t,T=f?t:e}let w,E=a[T],Z=!1;if(E){if(Z=!0,g)for(let e=0;e<E.length;e++)if(O(E[e],l))return}else E=a[T]=[];const S=a.constructor.name,D=N[S];D&&(w=D[c]),w||(w=S+n+(k?k(c):c)),b.options=p,_&&(b.options.once=!1),b.target=a,b.capture=f,b.eventName=c,b.isExisting=Z;const z=u?x:void 0;z&&(z.taskData=b);const P=m.scheduleEventTask(w,l,z,o,r);return b.target=null,z&&(z.taskData=null),_&&(p.once=!0),(R||"boolean"!=typeof P.options)&&(P.options=p),P.target=a,P.capture=f,P.eventName=c,h&&(P.originalDelegate=l),i?E.unshift(P):E.push(P),s?a:void 0}};return m[o]=C(v,l,D,z,_),Z&&(m.prependListener=C(Z,".prependListener:",(function(e){return Z.call(b.target,b.eventName,e.invoke,b.options)}),z,_,!0)),m[s]=function(){const t=this||e,n=arguments[0],o=arguments[2];let r;r=void 0!==o&&(!0===o||!1!==o&&!!o&&!!o.capture);const s=arguments[1];if(!s)return T.apply(this,arguments);if(d&&!d(T,s,t,arguments))return;const i=M[n];let a;i&&(a=i[r?"true":"false"]);const c=a&&t[a];if(c)for(let e=0;e<c.length;e++){const n=c[e];if(O(n,s))return c.splice(e,1),n.isRemoved=!0,0===c.length&&(n.allRemoved=!0,t[a]=null),n.zone.cancelTask(n),_?t:void 0}return T.apply(this,arguments)},m[i]=function(){const t=this||e,n=arguments[0],o=[],r=H(t,k?k(n):n);for(let e=0;e<r.length;e++){const t=r[e];o.push(t.originalDelegate?t.originalDelegate:t.callback)}return o},m[a]=function(){const t=this||e,n=arguments[0];if(n){const e=M[n];if(e){const o=t[e.false],r=t[e.true];if(o){const e=o.slice();for(let t=0;t<e.length;t++){const o=e[t];this[s].call(this,n,o.originalDelegate?o.originalDelegate:o.callback,o.options)}}if(r){const e=r.slice();for(let t=0;t<e.length;t++){const o=e[t];this[s].call(this,n,o.originalDelegate?o.originalDelegate:o.callback,o.options)}}}}else{const e=Object.keys(t);for(let t=0;t<e.length;t++){const n=A.exec(e[t]);let o=n&&n[1];o&&"removeListener"!==o&&this[a].call(this,o)}this[a].call(this,"removeListener")}if(_)return this},P(m[o],v),P(m[s],T),E&&P(m[a],E),w&&P(m[i],w),!0}let g=[];for(let r=0;r<t.length;r++)g[r]=d(t[r],n);return g}function H(e,t){const n=[];for(let o in e){const r=A.exec(o);let s=r&&r[1];if(s&&(!t||s===t)){const t=e[o];if(t)for(let e=0;e<t.length;e++)n.push(t[e])}}return n}function B(e,t){const n=e.Event;n&&n.prototype&&t.patchMethod(n.prototype,"stopImmediatePropagation",e=>function(t,n){t.__zone_symbol__propagationStopped=!0,e&&e.apply(t,n)})}function G(e,t,n,o,r){const s=Zone.__symbol__(o);if(t[s])return;const i=t[s]=t[o];t[o]=function(s,a,c){return a&&a.prototype&&r.forEach((function(t){const r=`${n}.${o}::`+t,s=a.prototype;if(s.hasOwnProperty(t)){const n=e.ObjectGetOwnPropertyDescriptor(s,t);n&&n.value?(n.value=e.wrapWithCurrentZone(n.value,r),e._redefineProperty(a.prototype,t,n)):s[t]&&(s[t]=e.wrapWithCurrentZone(s[t],r))}else s[t]&&(s[t]=e.wrapWithCurrentZone(s[t],r))})),i.call(t,s,a,c)},e.attachOriginToPatched(t[o],i)}const q=Zone.__symbol__,$=Object[q("defineProperty")]=Object.defineProperty,U=Object[q("getOwnPropertyDescriptor")]=Object.getOwnPropertyDescriptor,W=Object.create,V=q("unconfigurables");function X(e,t,n){const o=n.configurable;return K(e,t,n=Y(e,t,n),o)}function J(e,t){return e&&e[V]&&e[V][t]}function Y(e,t,n){return Object.isFrozen(n)||(n.configurable=!0),n.configurable||(e[V]||Object.isFrozen(e)||$(e,V,{writable:!0,value:{}}),e[V]&&(e[V][t]=!0)),n}function K(e,t,n,o){try{return $(e,t,n)}catch(r){if(!n.configurable)throw r;void 0===o?delete n.configurable:n.configurable=o;try{return $(e,t,n)}catch(r){let o=null;try{o=JSON.stringify(n)}catch(r){o=n.toString()}console.log(`Attempting to configure '${t}' with descriptor '${o}' on object '${e}' and got error, giving up: ${r}`)}}}const Q=["absolutedeviceorientation","afterinput","afterprint","appinstalled","beforeinstallprompt","beforeprint","beforeunload","devicelight","devicemotion","deviceorientation","deviceorientationabsolute","deviceproximity","hashchange","languagechange","message","mozbeforepaint","offline","online","paint","pageshow","pagehide","popstate","rejectionhandled","storage","unhandledrejection","unload","userproximity","vrdisplyconnected","vrdisplaydisconnected","vrdisplaypresentchange"],ee=["encrypted","waitingforkey","msneedkey","mozinterruptbegin","mozinterruptend"],te=["load"],ne=["blur","error","focus","load","resize","scroll","messageerror"],oe=["bounce","finish","start"],re=["loadstart","progress","abort","error","load","progress","timeout","loadend","readystatechange"],se=["upgradeneeded","complete","abort","success","error","blocked","versionchange","close"],ie=["close","error","open","message"],ae=["error","message"],ce=["abort","animationcancel","animationend","animationiteration","auxclick","beforeinput","blur","cancel","canplay","canplaythrough","change","compositionstart","compositionupdate","compositionend","cuechange","click","close","contextmenu","curechange","dblclick","drag","dragend","dragenter","dragexit","dragleave","dragover","drop","durationchange","emptied","ended","error","focus","focusin","focusout","gotpointercapture","input","invalid","keydown","keypress","keyup","load","loadstart","loadeddata","loadedmetadata","lostpointercapture","mousedown","mouseenter","mouseleave","mousemove","mouseout","mouseover","mouseup","mousewheel","orientationchange","pause","play","playing","pointercancel","pointerdown","pointerenter","pointerleave","pointerlockchange","mozpointerlockchange","webkitpointerlockerchange","pointerlockerror","mozpointerlockerror","webkitpointerlockerror","pointermove","pointout","pointerover","pointerup","progress","ratechange","reset","resize","scroll","seeked","seeking","select","selectionchange","selectstart","show","sort","stalled","submit","suspend","timeupdate","volumechange","touchcancel","touchmove","touchstart","touchend","transitioncancel","transitionend","waiting","wheel"].concat(["webglcontextrestored","webglcontextlost","webglcontextcreationerror"],["autocomplete","autocompleteerror"],["toggle"],["afterscriptexecute","beforescriptexecute","DOMContentLoaded","freeze","fullscreenchange","mozfullscreenchange","webkitfullscreenchange","msfullscreenchange","fullscreenerror","mozfullscreenerror","webkitfullscreenerror","msfullscreenerror","readystatechange","visibilitychange","resume"],Q,["beforecopy","beforecut","beforepaste","copy","cut","paste","dragstart","loadend","animationstart","search","transitionrun","transitionstart","webkitanimationend","webkitanimationiteration","webkitanimationstart","webkittransitionend"],["activate","afterupdate","ariarequest","beforeactivate","beforedeactivate","beforeeditfocus","beforeupdate","cellchange","controlselect","dataavailable","datasetchanged","datasetcomplete","errorupdate","filterchange","layoutcomplete","losecapture","move","moveend","movestart","propertychange","resizeend","resizestart","rowenter","rowexit","rowsdelete","rowsinserted","command","compassneedscalibration","deactivate","help","mscontentzoom","msmanipulationstatechanged","msgesturechange","msgesturedoubletap","msgestureend","msgesturehold","msgesturestart","msgesturetap","msgotpointercapture","msinertiastart","mslostpointercapture","mspointercancel","mspointerdown","mspointerenter","mspointerhover","mspointerleave","mspointermove","mspointerout","mspointerover","mspointerup","pointerout","mssitemodejumplistitemremoved","msthumbnailclick","stop","storagecommit"]);function le(e,t,n){if(!n||0===n.length)return t;const o=n.filter(t=>t.target===e);if(!o||0===o.length)return t;const r=o[0].ignoreProperties;return t.filter(e=>-1===r.indexOf(e))}function ue(e,t,n,o){e&&Z(e,le(e,t,n),o)}function he(e,t){if(y&&!v)return;if(Zone[e.symbol("patchEvents")])return;const n="undefined"!=typeof WebSocket,o=t.__Zone_ignore_on_properties;if(b){const e=window,t=I?[{target:e,ignoreProperties:["error"]}]:[];ue(e,ce.concat(["messageerror"]),o?o.concat(t):o,r(e)),ue(Document.prototype,ce,o),void 0!==e.SVGElement&&ue(e.SVGElement.prototype,ce,o),ue(Element.prototype,ce,o),ue(HTMLElement.prototype,ce,o),ue(HTMLMediaElement.prototype,ee,o),ue(HTMLFrameSetElement.prototype,Q.concat(ne),o),ue(HTMLBodyElement.prototype,Q.concat(ne),o),ue(HTMLFrameElement.prototype,te,o),ue(HTMLIFrameElement.prototype,te,o);const n=e.HTMLMarqueeElement;n&&ue(n.prototype,oe,o);const s=e.Worker;s&&ue(s.prototype,ae,o)}const s=t.XMLHttpRequest;s&&ue(s.prototype,re,o);const i=t.XMLHttpRequestEventTarget;i&&ue(i&&i.prototype,re,o),"undefined"!=typeof IDBIndex&&(ue(IDBIndex.prototype,se,o),ue(IDBRequest.prototype,se,o),ue(IDBOpenDBRequest.prototype,se,o),ue(IDBDatabase.prototype,se,o),ue(IDBTransaction.prototype,se,o),ue(IDBCursor.prototype,se,o)),n&&ue(WebSocket.prototype,ie,o)}Zone.__load_patch("util",(e,t,r)=>{r.patchOnProperties=Z,r.patchMethod=z,r.bindArguments=_,r.patchMacroTask=O;const a=t.__symbol__("BLACK_LISTED_EVENTS"),c=t.__symbol__("UNPATCHED_EVENTS");e[c]&&(e[a]=e[c]),e[a]&&(t[a]=t[c]=e[a]),r.patchEventPrototype=B,r.patchEventTarget=F,r.isIEOrEdge=L,r.ObjectDefineProperty=o,r.ObjectGetOwnPropertyDescriptor=n,r.ObjectCreate=s,r.ArraySlice=i,r.patchClass=D,r.wrapWithCurrentZone=l,r.filterProperties=le,r.attachOriginToPatched=P,r._redefineProperty=X,r.patchCallbacks=G,r.getGlobalObjects=()=>({globalSources:N,zoneSymbolEventNames:M,eventNames:ce,isBrowser:b,isMix:v,isNode:y,TRUE_STR:"true",FALSE_STR:"false",ZONE_SYMBOL_PREFIX:"__zone_symbol__",ADD_EVENT_LISTENER_STR:"addEventListener",REMOVE_EVENT_LISTENER_STR:"removeEventListener"})});const pe=h("zoneTask");function fe(e,t,n,o){let r=null,s=null;n+=o;const i={};function a(t){const n=t.data;return n.args[0]=function(){try{t.invoke.apply(this,arguments)}finally{t.data&&t.data.isPeriodic||("number"==typeof n.handleId?delete i[n.handleId]:n.handleId&&(n.handleId[pe]=null))}},n.handleId=r.apply(e,n.args),t}function c(e){return s(e.data.handleId)}r=z(e,t+=o,n=>function(r,s){if("function"==typeof s[0]){const e=u(t,s[0],{isPeriodic:"Interval"===o,delay:"Timeout"===o||"Interval"===o?s[1]||0:void 0,args:s},a,c);if(!e)return e;const n=e.data.handleId;return"number"==typeof n?i[n]=e:n&&(n[pe]=e),n&&n.ref&&n.unref&&"function"==typeof n.ref&&"function"==typeof n.unref&&(e.ref=n.ref.bind(n),e.unref=n.unref.bind(n)),"number"==typeof n||n?n:e}return n.apply(e,s)}),s=z(e,n,t=>function(n,o){const r=o[0];let s;"number"==typeof r?s=i[r]:(s=r&&r[pe],s||(s=r)),s&&"string"==typeof s.type?"notScheduled"!==s.state&&(s.cancelFn&&s.data.isPeriodic||0===s.runCount)&&("number"==typeof r?delete i[r]:r&&(r[pe]=null),s.zone.cancelTask(s)):t.apply(e,o)})}function de(e,t){if(Zone[t.symbol("patchEventTarget")])return;const{eventNames:n,zoneSymbolEventNames:o,TRUE_STR:r,FALSE_STR:s,ZONE_SYMBOL_PREFIX:i}=t.getGlobalObjects();for(let c=0;c<n.length;c++){const e=n[c],t=i+(e+s),a=i+(e+r);o[e]={},o[e][s]=t,o[e][r]=a}const a=e.EventTarget;return a&&a.prototype?(t.patchEventTarget(e,[a&&a.prototype]),!0):void 0}Zone.__load_patch("legacy",e=>{const t=e[Zone.__symbol__("legacyPatch")];t&&t()}),Zone.__load_patch("timers",e=>{fe(e,"set","clear","Timeout"),fe(e,"set","clear","Interval"),fe(e,"set","clear","Immediate")}),Zone.__load_patch("requestAnimationFrame",e=>{fe(e,"request","cancel","AnimationFrame"),fe(e,"mozRequest","mozCancel","AnimationFrame"),fe(e,"webkitRequest","webkitCancel","AnimationFrame")}),Zone.__load_patch("blocking",(e,t)=>{const n=["alert","prompt","confirm"];for(let o=0;o<n.length;o++)z(e,n[o],(n,o,r)=>function(o,s){return t.current.run(n,e,s,r)})}),Zone.__load_patch("EventTarget",(e,t,n)=>{!function(e,t){t.patchEventPrototype(e,t)}(e,n),de(e,n);const o=e.XMLHttpRequestEventTarget;o&&o.prototype&&n.patchEventTarget(e,[o.prototype]),D("MutationObserver"),D("WebKitMutationObserver"),D("IntersectionObserver"),D("FileReader")}),Zone.__load_patch("on_property",(e,t,n)=>{he(n,e),Object.defineProperty=function(e,t,n){if(J(e,t))throw new TypeError("Cannot assign to read only property '"+t+"' of "+e);const o=n.configurable;return"prototype"!==t&&(n=Y(e,t,n)),K(e,t,n,o)},Object.defineProperties=function(e,t){return Object.keys(t).forEach((function(n){Object.defineProperty(e,n,t[n])})),e},Object.create=function(e,t){return"object"!=typeof t||Object.isFrozen(t)||Object.keys(t).forEach((function(n){t[n]=Y(e,n,t[n])})),W(e,t)},Object.getOwnPropertyDescriptor=function(e,t){const n=U(e,t);return n&&J(e,t)&&(n.configurable=!1),n}}),Zone.__load_patch("customElements",(e,t,n)=>{!function(e,t){const{isBrowser:n,isMix:o}=t.getGlobalObjects();(n||o)&&e.customElements&&"customElements"in e&&t.patchCallbacks(t,e.customElements,"customElements","define",["connectedCallback","disconnectedCallback","adoptedCallback","attributeChangedCallback"])}(e,n)}),Zone.__load_patch("XHR",(e,t)=>{!function(e){const p=e.XMLHttpRequest;if(!p)return;const f=p.prototype;let d=f[a],g=f[c];if(!d){const t=e.XMLHttpRequestEventTarget;if(t){const e=t.prototype;d=e[a],g=e[c]}}function _(e){const t=e.data,o=t.target;o[s]=!1,o[l]=!1;const i=o[r];d||(d=o[a],g=o[c]),i&&g.call(o,"readystatechange",i);const u=o[r]=()=>{if(o.readyState===o.DONE)if(!t.aborted&&o[s]&&"scheduled"===e.state){const n=o.__zone_symbol__loadfalse;if(n&&n.length>0){const r=e.invoke;e.invoke=function(){const n=o.__zone_symbol__loadfalse;for(let t=0;t<n.length;t++)n[t]===e&&n.splice(t,1);t.aborted||"scheduled"!==e.state||r.call(e)},n.push(e)}else e.invoke()}else t.aborted||!1!==o[s]||(o[l]=!0)};return d.call(o,"readystatechange",u),o[n]||(o[n]=e),T.apply(o,t.args),o[s]=!0,e}function m(){}function k(e){const t=e.data;return t.aborted=!0,w.apply(t.target,t.args)}const y=z(f,"open",()=>function(e,t){return e[o]=0==t[2],e[i]=t[1],y.apply(e,t)}),b=h("fetchTaskAborting"),v=h("fetchTaskScheduling"),T=z(f,"send",()=>function(e,n){if(!0===t.current[v])return T.apply(e,n);if(e[o])return T.apply(e,n);{const t={target:e,url:e[i],isPeriodic:!1,args:n,aborted:!1},o=u("XMLHttpRequest.send",m,t,_,k);e&&!0===e[l]&&!t.aborted&&"scheduled"===o.state&&o.invoke()}}),w=z(f,"abort",()=>function(e,o){const r=e[n];if(r&&"string"==typeof r.type){if(null==r.cancelFn||r.data&&r.data.aborted)return;r.zone.cancelTask(r)}else if(!0===t.current[b])return w.apply(e,o)})}(e);const n=h("xhrTask"),o=h("xhrSync"),r=h("xhrListener"),s=h("xhrScheduled"),i=h("xhrURL"),l=h("xhrErrorBeforeScheduled")}),Zone.__load_patch("geolocation",e=>{e.navigator&&e.navigator.geolocation&&function(e,t){const o=e.constructor.name;for(let r=0;r<t.length;r++){const s=t[r],i=e[s];if(i){if(!m(n(e,s)))continue;e[s]=(e=>{const t=function(){return e.apply(this,_(arguments,o+"."+s))};return P(t,e),t})(i)}}}(e.navigator.geolocation,["getCurrentPosition","watchPosition"])}),Zone.__load_patch("PromiseRejectionEvent",(e,t)=>{function n(t){return function(n){H(e,t).forEach(o=>{const r=e.PromiseRejectionEvent;if(r){const e=new r(t,{promise:n.promise,reason:n.rejection});o.invoke(e)}})}}e.PromiseRejectionEvent&&(t[h("unhandledPromiseRejectionHandler")]=n("unhandledrejection"),t[h("rejectionHandledHandler")]=n("rejectionhandled"))})}}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 3
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js](https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/runtime-es2015.c38a6edb350405b56932.js](https://sepia.fabnum.fr/runtime-es2015.c38a6edb350405b56932.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/runtime-es5.c38a6edb350405b56932.js](https://sepia.fabnum.fr/runtime-es5.c38a6edb350405b56932.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js](https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/assets/logo_lite.svg](https://sepia.fabnum.fr/assets/logo_lite.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js](https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/runtime-es2015.c38a6edb350405b56932.js](https://sepia.fabnum.fr/runtime-es2015.c38a6edb350405b56932.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/runtime-es5.c38a6edb350405b56932.js](https://sepia.fabnum.fr/runtime-es5.c38a6edb350405b56932.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/styles.f72457cb1e9c6a6f2f5f.css](https://sepia.fabnum.fr/styles.f72457cb1e9c6a6f2f5f.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js](https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js)
  
  
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

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js](https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Select`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js](https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Db`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: "function _createForOfIteratorHelper(t,e){var n;if("undefined"==typeof Symbol||null==t[Symbol.iterator]){if(Array.isArray(t)||(n=", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="runtime-es2015.c38a6edb350405b56932.js" type="module"></script>`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="runtime-es2015.c38a6edb350405b56932.js" type="module"></script>`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js](https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="runtime-es2015.c38a6edb350405b56932.js" type="module"></script>`
  
  
  
  
Instances: 4
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://sepia.fabnum.fr/runtime-es5.c38a6edb350405b56932.js](https://sepia.fabnum.fr/runtime-es5.c38a6edb350405b56932.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js](https://sepia.fabnum.fr/polyfills-es5.7bebc223554456e35572.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/robots.txt](https://sepia.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/styles.f72457cb1e9c6a6f2f5f.css](https://sepia.fabnum.fr/styles.f72457cb1e9c6a6f2f5f.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/sitemap.xml](https://sepia.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js](https://sepia.fabnum.fr/polyfills-es2015.b43d4dcd8c503294cc94.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/runtime-es2015.c38a6edb350405b56932.js](https://sepia.fabnum.fr/runtime-es2015.c38a6edb350405b56932.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es5.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/](https://sepia.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://sepia.fabnum.fr/assets/logo_lite.svg](https://sepia.fabnum.fr/assets/logo_lite.svg)
  
  
  * Method: `GET`
  
  
  
  
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
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16777216`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `402653184`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `335544320`
  
  
  
  
* URL: [https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js](https://sepia.fabnum.fr/main-es2015.2d94e01622772aa752ec.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `603979776`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>16777216, which evaluates to: 1970-07-14 04:20:16</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
