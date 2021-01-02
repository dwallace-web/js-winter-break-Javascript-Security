#Javascript Security

##Intro
##Overview of security concepts
###Common Threats
XXS - CROSS SITE scripting -
csrf - request forgery
sensitive data exposure
injection attacks
obfuscation (wearing a disguise)

###Available Resources
OWASP Foundation
Snyk - identify issues and dependences (more than basic npm audiet)
Retire.js - scan app for known issues and security holes in the code
AppSensor - monitor application for live intrusions

##Security Applied XSS
https://www.google.com/about/appsecurity/learning/xss/
What happens - pushing code into a form
Evaluate data on the server and client side.

Running function that returns code with innerHTML in React is bad. Don't do it. Why?
Answer: code could be pushed into the inter HTML and screw the app.

Never put unstrusted data in the code or on the site.
Sanitize data before returning the unsafe data and displaying it on the page.
Use element.textContent to populate DOM with safe usage
Frames like react/angular have escaping functions built in like dangerouslySetInnerHTML
Many rules for escaping data.

https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html
https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html

##Secutity Applied CSRF

1. evaluate headers and assigned token; validate token and request
2. use JWT/JSON token with tools like Auth0 jwt.io

Three Items in the payload: 1) header, 2) payload, 3) signature

Signature proves the requester is who they say they are.
Token used to eval user data request.

_Autho0_ Authentification in web/mobile apps.

Auth0 is an organisation, who manages Universal Identity Platform for web, mobile and IoT can handle any of them — B2C, B2B, B2E, or a combination.

OAuth 2.0 is a protocol that allows a user to grant limited access to their resources on one site, to another site, without having to expose their credentials.

##Security Applied Sensitive Data

##Security Applied SSJI

##Security Applied Obsfuscation
