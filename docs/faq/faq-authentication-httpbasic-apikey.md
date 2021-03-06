---
layout: post
title: Which authentication method needs to be used with NetLicensing RESTful API?
parent: FAQ & Troubleshooting
nav_order: 100
description: "Which authentication method needs to be used with NetLicensing RESTful API - HTTP Basic Auth or API Key?"
permalink: faq-authentication-httpbasic-apikey
---

{{ page.title }}
=============

## Question

I'm integrating NetLicensing API in my python application and wondering which authentication method should I use to connect to NetLicensing.

## Answer

NetLicensing offering two [authentication alternatives](security): *HTTP Basic Authentication* and *API Key Identification*.

### HTTP Basic Auth

In this approach, base64 encoded username and password need to be sent within a request header to prove authentication.
As this approach uses the HTTP header, so there’s no need to handshakes or other complex response systems.

>*NOTE: While using Basic Auth you will be granted full access to the NetLicensing endpoints (e.g. one level of account access - **super admin**) within your vendor account. You need to make sure the credentials stored and delivered in a secure way within your application and not visible to the end-customers.*

*In most of the cases, we recommend **API Key Identification** as the most secure and flexible option.*

### API Key Identification (recommended)

API Keys allow limited access to NetLicensing API methods depending on the chosen [API Key role](security#api-key-identification).

Leveraging API Keys improves security by:

- Reducing the need to store sensitive credentials on the client-side
- Limiting the set of possible operations which can be done with a particular key
- Creating context-specific keys for the specified customers' segments, products or use cases
- API Keys can be easily revoked if compromised

API Keys are *not expirable* and can be created via NetLicnsing Management Console ([API Access](https://ui.netlicensing.io/#/settings) tab) or RESTful API ([TokenService](token-services)).

<a href="assets/images/faq-netlicensing-apikey.png" class="imagelink" data-lightbox="faq-netlicensing-apikey" data-title="Management Console - Settings - API Keys" data-alt="Management Console - Settings - API Keys">
  <img src="assets/images/faq-netlicensing-apikey.png" />
</a>

#### How to rotate NetLicensing API Keys

Changing compromised API Keys or rotating on a regular schedule is known security best practice.
This shortens the period an API Key is active and therefore reduces the business impact if they are compromised.

Below we will show you the steps, how to rotate NetLicensing API Keys for the end-customers.

To replace API Keys, follow these steps:

- Create a second API Key in addition to the one in use (provide the context for the key in the name field).
- Update all your applications to use the new API Key and make sure this key is rolled-out to all affected end-customers.
- **Test-Test-...Test:** Validate that the applications are working as expected.
- Backup old API Key number for further support requests (e.g. key restoration by our support team).
- Delete the inactive old API Key.

### Refrences

- How to use NetLicensing with Java and Spring Security: [https://netlicensing.io/blog/2020/11/13/netlicensing-spring-security/](https://netlicensing.io/blog/2020/11/13/netlicensing-spring-security/)
