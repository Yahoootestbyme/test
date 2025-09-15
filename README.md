This vulnerability arises when an application does not enforce an account lockout mechanism after repeated failed login attempts. A lack of such a policy allows attackers to perform brute-force attacks—systematically guessing usernames and passwords until they succeed—without any rate-limiting or blocking mechanisms in place.

During the assessment, the test team conducted multiple consecutive failed login attempts using incorrect credentials at the application’s login page. It was observed that:
The application allowed unlimited login attempts without any temporary lockout, CAPTCHA, or delay mechanism.
No warning or rate-limiting response was triggered even after 20+ failed attempts for the same user account.


Attackers can exploit this weakness to perform credential-stuffing attacks using automated tools,Especially critical if users have weak or reused passwords
Lack of lockout or delay enables continuous, high-speed attempts to guess credentials.


Lock the account temporarily after a defined number of failed login attempts (e.g., 5 attempts).
Present CAPTCHA challenges after a few failed attempts to differentiate between humans and bots.
Enforce strong password policies.
Enable multi-factor authentication (MFA) to reduce reliance on password security alone.
