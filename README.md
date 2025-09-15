This vulnerability arises when cookies are set without the Secure and/or HttpOnly attributes. These flags are essential for protecting cookies from being exposed to unintended parties, especially in the context of web applications handling authentication, session management, or sensitive data.

During the assessment, the test team observed that session cookies set by the application were missing the Secure and HttpOnly attributes. This was identified by reviewing the Set-Cookie headers in HTTP responses and browser developer tools during authenticated sessions.

Cookies without the Secure attribute can be sent over unencrypted HTTP, making them vulnerable to interception via man-in-the-middle (MITM) attacks.
Without the HttpOnly flag, cookies can be accessed and exfiltrated by malicious JavaScript injected through XSS vulnerabilities.

Ensure all cookies containing sensitive data (e.g., session identifiers) are flagged with Secure to restrict their transmission to HTTPS connections only
Prevent client-side scripts from accessing cookies by using the HttpOnly flag.
Add the SameSite=Strict or SameSite=Lax attribute to help prevent cross-site request forgery (CSRF) attacks
