This vulnerability arises when a WildFly application server is exposed with its default web interface or welcome page still accessible in a production environment. The default page typically includes version information and references to documentation, management consoles, and sample applications.

During the assessment, the test team accessed the application server  and observed that the WildFly default home page was displayed. The page contained WildFly branding and links to documentation and server management resources.

Information Disclosure: The WildFly default page may reveal server version, deployment details, and technology stack information, helping attackers craft targeted attacks.
Security Misconfiguration Indicator: Publicly accessible default pages suggest a lack of proper server hardening and may imply that management interfaces (such as the WildFly Admin Console or JMX interfaces) are also exposed.


Remove or restrict access to the default WildFly welcome page (welcome-content) in the server configuration.

Restrict Access to Admin Interfaces: Ensure management consoles (e.g., /console, /management) are not accessible from untrusted networks and are protected by strong authentication.

Harden Server Configuration: Follow WildFly hardening best practices to disable unused features, limit port exposure, and secure default deployments.
