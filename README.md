This vulnerability arises when an application or system component is left configured with default credentials that are commonly known and publicly documented. These credentials are typically provided by vendors for initial setup and are expected to be changed before deployment. However, if they remain unchanged in a production environment, they can be easily exploited by malicious actors to gain unauthorized access.

During the assessment, the test team observed that the application was accessible using default administrative credentials.

Gain administrative access without needing to exploit other vulnerabilities.

Modify configurations, access sensitive data, or disrupt system operations.

Use the access to plant backdoors, elevate privileges, or pivot to other systems.

Combine this with other vulnerabilities (e.g., internal IP disclosure, open ports) to carry out lateral movement or broader compromise.




Immediately change all default usernames and passwords to strong, unique credentials.

Enforce password complexity and rotation policies for all administrative and privileged accounts.

Disable or remove any unused default accounts if they are not required.
