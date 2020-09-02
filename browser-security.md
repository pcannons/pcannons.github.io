## Web app security checklist

**Same-origin policy (SOP)**

The browser protects a window.document from `scheme://hostname:port` accessing another window.document's DOM unless the `scheme://hostname:port` of the other document is identical.

Embedded resources such as images, CSS, and scripts are not restricted by SOP and can be accessed and loaded across different origins. Embedded means resources loaded from tags like `<image>`, `<audio>`, `<video>`.
  
[SOP Details](https://web.dev/same-origin-policy/)
  

**Cross-origin resource sharing (CORS)**

Owner of a specific `scheme://hostname:port` can poke holes in the SOP to allow access to it. To do this they can specify safe `scheme://hostname:port`, collections of them, or * meaning everything.

It's bad practice to use * unless you have a set of public APIs or resources.
  

**Cross-site request forgery (CSRF)**

Tricking a browser into submitting a request to a URL such as `scheme://hostname:port/send_money`. To protect against this, the browser first gets a CSRF token and then appends it to the end of the request: `scheme://hostname:port/send_money?token=random_string`

If the owner of the specific URL poked a hole in the SOP using CORS, for example by setting it to *, then the attacker can simply request the CSRF token first rendering this defense useless.
  

**Cross-site scripting (XSS)**

Injecting malicious code into a website to exploit the client or server side.
  

**Content Security Policy (CSP)**

Browsers trust all code that shows up on a page as being legitimate. The browser is unable to distinguish between scripts that are part of the application versus malicious third-party injections. 

CSP follows a whitelist approach. Anything loaded from unexpected domains doesn't load and throws an error, preventing certain types of XSS attacks from happening. 

e.g. `Content-Security-Policy: script-src 'self' https://trusted-domain.com`

[CSP Details](https://developers.google.com/web/fundamentals/security/csp)