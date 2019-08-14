# security-audit

- [ ] Review latest OWASP Top 10
- [ ] Run automatic security checks
  - [ ] 
- [ ] Update all dependencies
  - [ ] Use LTS versions (Node.js, Ubuntu, etc)
- [ ] No vulnerabilities found in dependencies (GitHub and npm security reports, etc)
- [ ] Lock down ports (tcp, udp, etc)
  - [ ] Only open ports that are absolutely necessary
  - [ ] Only open the smallest subset of absolutely necessary IP addresses on each port


- [ ] TODO put this in order before doing the security audit video
- [ ] We should use OWASP to ensure that our audit is correctly targeting security risks: https://www.owasp.org/images/7/72/OWASP_Top_10-2017_%28en%29.pdf.pdf
  - [ ] This should be part of the audit audit, every time the audit is completed, review the latest security risks
- [ ] Use security scanning sites! It seems like there are a lot of good ones
- [ ] Add this security header scanner: https://securityheaders.com/
- [ ] Add the CSP evaluator: https://csp-evaluator.withgoogle.com/
- [ ] Add CSP checking to the audit
- [ ] Add the Mozilla Observatory scan to the audit: https://observatory.mozilla.org
- [ ] Should we add the Lighthouse checks to the audit?
- [ ] Make sure all cryptographic algorithms are up to date, like which sha algorithm which ECDSA curve, etc
- [ ] New audit to add: Ensure encryption of data in transit and at rest: all ssl connections, force ssl on database, make sure certificates are handled appropriately, ensure database is encrypted and that its keys are rotated every quarter...the database should be reencrypted every quarter???
- [ ] Rotate all keys (All current public and private keys, secrets, etc should be deleted and replaced by newly generated keys. Stripe keys, Twilio keys, GraphQL keys, Prisma keys, Rails keybase, etc should all be rotated.)
- [ ] Rotate all user passwords (All user passwords should be changed. They should be a minimum of 10 characters in length. GitLab, Gmail, AWS, Twilio, Cloud66, Stripe, Slack, etc.)
  - [ ]  Are there other "ports" on other protocols that could have access to the machine?
- [ ] Authentication system (Make sure our authentication system/mechanisms are up-to-date and secure. Study cookies, JWTs, etc and how we are handling them to ensure we are implementing best practices and are not making glaring mistakes.)
- [ ] Authorization system (Ensure that the way we handle access to data/permissions is appropriate. All automated tests for permissions should be passing. The way we handle roles should be appropriate. Physical/logistical access controls should be in place, such as locking screens, not sharing passwords, etc.)
- [ ] Endpoints have proper authentication and authorization (All processes that are accessible through tcp/ip ports should be audited to ensure each endpoint has proper authentication and authorization. Analyze the types of operations, reads or writes, that are permitted. Any permitted operations should only allow access by those who need access.)
- [ ] Ensure physical integrity of all keys (Check that all keys can be physically accessed (for example, check USB drives to ensure the keys can be retrieved). Know where all keys are stored, check all laptops, USB drives, environment variable configs, safes, etc.)
- [ ] Review organizational access control policies (Review organizational access control policies such as who has access to what data, password length, password lifetimes, access to secret keys, password sharing, screen locking, proper data sharing channels (Gmail, Slack, Excel) etc)
- [ ] Sanitize data (Health data, credit card data, and other types of sensitive data with compliance requirements should never be stored in our systems anywhere, unless we can store them compliantly. If we are storing that data, we should track it down and delete it. We should also build the functionality to stop storing the data. Personal data should be deleted over time as it becomes unneeded.)
- [ ]  Revoke access to terminated employees (Review all user accounts. Anyone who is not currently an employee should be completely removed from our system so that they no longer have access to any sensitive data or functionality. Check our database, GitLab, Gmail, Twilio, Stripe, Slack, etc)
- [ ] Review compliance with regulations (Make sure we are compliant with HIPAA, PCI, GDPR, etc)
- [ ] Audit the audit (Take some time to study the latest security best practices. Ensure that our audit process is up-to-date and will lead to sufficient security. Clean up the issue, change wording, add audits, etc.)
- [ ] New audit to add: Ensure proper logging and monitoring. We don't really have a good way of knowing what attacks are taking place on our system, no alarms or anything to notify us of breaches
