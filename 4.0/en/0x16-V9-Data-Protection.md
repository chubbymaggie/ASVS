# V9: Data Protection Verification Requirements

## Control Objective

There are three key elements to sound data protection: Confidentiality, Integrity and Availability (CIA). This standard assumes that data protection is enforced on a trusted system, such as a server, which has been hardened and has sufficient protections.

Applications have to assume that all user devices are compromised in some way. Where an application transmits or stores sensitive information on insecure devices, such as shared computers, phones and tablets, the application is responsible for ensuring data stored on these devices is encrypted and cannot be easily illicitly obtained, altered or disclosed.

Ensure that a verified application satisfies the following high level data protection requirements:

* Confidentiality: Data should be protected from unauthorized observation or disclosure both in transit and when stored.
* Integrity: Data should be protected being maliciously created, altered or deleted by unauthorized attackers.
* Availability: Data should be available to authorized users as required.

## Security Verification Requirements

| # | Description | L1 | L2 | L3 | Since |
| --- | --- | --- | --- | -- | -- |
| **9.2** | Identify all sensitive data created and processed by the application and ensure that a policy is in place on how to deal with sensitive data. | ✓ | ✓ | ✓ | 4.0 |
| **9.3** | Verify that sensitive data is sent to the server in the HTTP/S message body or headers and that query string parameters from any HTTP verb do not contain sensitive data. | ✓ | ✓ | ✓ | 1.0 |
| **9.4** | Verify that the application sets sufficient anti-caching headers such that any sensitive and personal information displayed by the application or entered by the user should not be cached on disk by mainstream, modern browsers (e.g. visit about:cache to review disk cache). | ✓ | ✓ | ✓ | 4.0 |
| **9.5** | Verify that all cached or temporary copies of sensitive data stored on the server are protected from unauthorized access or purged/invalidated after the authorized user accesses the sensitive data. |  | ✓ | ✓ | 1.0 |
| **9.6** | Verify that users have a method to remove or export their data on demand. | ✓ | ✓ | ✓ | 4.0 |
| **9.7** | Verify the application minimizes the number of parameters in a request, such as hidden fields, Ajax variables, cookies and header values. |  | ✓ | ✓ | 2.0 |
| **9.8** | Verify the application has the ability to detect and alert on abnormal numbers of requests. |  | ✓ | ✓ | 4.0 |
| **9.9** | Verify that data stored in client side storage (such as HTML5 local storage, session storage, IndexedDB, regular cookies or Flash cookies) does not contain sensitive data or PII. | ✓ | ✓ | ✓ | 3.0.1 |
| **9.10** | Verify accessing sensitive data is logged, if the data is collected under relevant data protection directives or where logging of access is required. |  | ✓ | ✓ | 3.0 |
| **9.11** | Verify that sensitive information maintained in memory is overwritten with zeros as soon as it is no longer required, to mitigate memory dumping attacks. |  | ✓ | ✓ | 3.0.1 |
| **9.12** | Verify that sensitive or private information that is required to be encrypted, is encrypted using approved algorithms that provide both confidentiality and integrity. | ✓ | ✓ | ✓ | 3.0.1 |
| **9.13** | Verify that users are provided clear language regarding collection and use of supplied personal information and that users have provided opt-in consent for the use of that data before it is used in any way. | ✓ | ✓ | ✓ | 4.0 |
| **9.14** | Verify that authenticated data is cleared from client storage, such as the browser DOM, after the client or session is terminated. |  | ✓ | ✓ | 3.0 |

## References

For more information, see also:

* [Consider using Security Headers website to check security and anti-caching headers](https://securityheaders.io)
* [OWASP Secure Headers project](https://www.owasp.org/index.php/OWASP_Secure_Headers_Project)
* [User Privacy Protection Cheat Sheet](https://www.owasp.org/index.php/User_Privacy_Protection_Cheat_Sheet)
