This vulnerability occurs when sensitive information such as API keys, tokens, or login credentials is hardcoded directly into JavaScript files. Since JavaScript is client-side and fully accessible through browser developer tools, any credentials embedded within the code become visible to all users, resulting in exposure of sensitive system access details.

During the assessment, the test team inspected the application’s JavaScript files using the browser’s developer tools. It was observed that the file <filename.js> contained hardcoded credentials in plain text. By simply opening the Sources tab, the credentials were readable without any authentication or restriction.

Attackers can leverage these exposed credentials to gain unauthorized access to backend APIs or services. This may lead to data leakage, service misuse, account compromise, or further escalation of attacks, especially if the exposed key or password has high privileges or broad access rights.

Remove all hardcoded credentials from JavaScript files and migrate them to secure server-side storage.
Regenerate and rotate the exposed credentials immediately.
Use environment variables, secure vaults, or encrypted configuration systems for secret management.
Implement automated scanning tools to detect hardcoded secrets during development.
