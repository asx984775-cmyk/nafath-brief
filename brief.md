Version: NAFATH-V1
Track: Networking
## Overview

A national digital identity service allows citizens to access government services using one trusted account. The software should use OpenID Connect to verify users' identities. Artificial intelligence can help detect suspicious login attempts, but its decisions should be reviewed to reduce errors. The mobile application should request only the permissions it needs. Network security is also important because login requests and DNS queries may reveal information about users. DNS over HTTPS can encrypt DNS queries between a device and its DNS resolver, but it does not protect all internet traffic. Phishing-resistant authentication helps prevent attackers from stealing login credentials. Finally, the service must protect personal data and follow Oman's Personal Data Protection Law. These six areas work together to make the service safer, more reliable, and more respectful of citizens' privacy. For networking, the team should carefully evaluate what DNS over HTTPS protects and what it cannot protect.

## Software

OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0. OAuth 2.0 is mainly used to grant applications limited access to resources, while OIDC adds authentication so an application can verify a user's identity. A national login service can use OIDC to confirm who the user is without requiring every government service to manage passwords independently. This separation improves integration between services.

Resource: https://openid.net/specs/openid-connect-core-1_0.html
