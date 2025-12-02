This vulnerability occurs when sensitive information—such as usernames, session tokens, authentication credentials, or API keys—is passed through URL query parameters. Since URLs are logged by browsers, servers, proxies, and third-party tools, any credential placed in the URL becomes exposed and can be retrieved by unauthorized parties. This indicates improper handling of sensitive data during authentication or API communication.

During the assessment, the test team observed that the application transmitted credentials as part of the URL during the login or authentication flow. By monitoring the browser address bar and network requests, it was noted that sensitive values such as <username / token / password> appeared directly within the URL, making them visible in browser history, server logs, and intermediary systems.

Attackers can exploit this weakness by harvesting credentials from browser history, shoulder surfing, proxy logs, or intercepted traffic. This increases the risk of unauthorized access, session hijacking, account compromise, and long-term credential leakage across multiple logging systems.

Avoid sending any sensitive information through URL query parameters.
Use secure POST requests or encrypted request bodies for credential transmission.
Mask or tokenize sensitive values before transmission.
Review and sanitize application logs to remove any previously recorded credentials.
Implement secure authentication flows that properly protect all sensitive data.
