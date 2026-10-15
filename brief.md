Version: NAFATH-V1
Track: Networking
## Overview

A national digital identity service allows citizens to access government services using one trusted account. The software should use OpenID Connect to verify users' identities. Artificial intelligence can help detect suspicious login attempts, but its decisions should be reviewed to reduce errors. The mobile application should request only the permissions it needs. Network security is also important because login requests and DNS queries may reveal information about users. DNS over HTTPS can encrypt DNS queries between a device and its DNS resolver, but it does not protect all internet traffic. Phishing-resistant authentication helps prevent attackers from stealing login credentials. Finally, the service must protect personal data and follow Oman's Personal Data Protection Law. These six areas work together to make the service safer, more reliable, and more respectful of citizens' privacy. For networking, the team should carefully evaluate what DNS over HTTPS protects and what it cannot protect.
## Software

OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0. OAuth 2.0 is mainly used to grant applications limited access to resources, while OIDC adds authentication so an application can verify a user's identity. A national login service can use OIDC to confirm who the user is without requiring every government service to manage passwords independently. This separation improves integration between services.

Resource: https://openid.net/specs/openid-connect-core-1_0.html

## AI

Artificial intelligence can help a national login service identify unusual sign-in patterns, such as unexpected locations or repeated failed attempts. However, an unusual login does not always mean an attack is happening. AI systems can produce false positives and false negatives, and their decisions may be affected by biased or incomplete data. The service should evaluate the system regularly, protect users' personal information, and provide a safe way to review suspicious cases.

Resource: https://www.nist.gov/itl/ai-risk-management-framework

## Mobile

Android runtime permissions allow users to decide whether an application can access certain sensitive features or data. A national identity application should request only the permissions it genuinely needs and explain why they are required. It should not assume that users will grant every permission. Requesting unnecessary access can reduce user trust and increase privacy risks. The application should continue to work safely when optional permissions are denied.

## Networking

DNS over HTTPS (DoH) sends DNS queries through an encrypted HTTPS connection to a DNS resolver. This helps prevent other parties on the network from easily reading or modifying DNS queries while they travel between the device and the resolver. However, DoH does not encrypt all internet traffic, hide the user's IP address from every service, or guarantee anonymity. A national login service should use HTTPS for its web traffic and understand that DoH is only one part of network privacy and security.

Resource: https://www.rfc-editor.org/rfc/rfc8484.html

Resource: https://developer.android.com/training/perm

## Cybersecurity

Phishing-resistant authentication is designed to prevent attackers from using fake websites to steal login credentials. FIDO2 security keys and passkeys can provide strong protection because they use cryptographic methods tied to the legitimate website or service. Unlike SMS codes, these methods are resistant to common phishing attacks. A national login service should prefer phishing-resistant methods for sensitive accounts and provide secure recovery options if users lose access.

Resource: https://pages.nist.gov/800-63-4/sp800-63b.html

## Data

Oman's Personal Data Protection Law establishes requirements for processing personal data. A national digital identity service should identify the personal data it collects, explain the purpose of processing, protect stored information, and follow applicable legal requirements. The organisation should also check the law's executive regulations and any relevant exceptions before deciding how consent, disclosure, retention, and data-subject rights apply to the service.

Resource: https://www.mtcit.gov.om/

issions/requesting

## Misconception in My Track

A common misconception about networking is that encrypting DNS queries makes all internet activity private. DNS over HTTPS (DoH) encrypts queries between a device and its DNS resolver, but it does not encrypt every connection or hide all identifying information. Websites can still see the IP address connecting to them, and other network traffic may reveal information. Therefore, a national digital identity service should use DoH as one privacy measure alongside HTTPS, strong authentication, and careful data protection.

## Open Question

How can a national digital identity service use DNS over HTTPS to improve users' privacy without assuming that it protects all their internet activity?
