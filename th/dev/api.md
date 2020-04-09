---
title: API
description: เข้าถึงทรัพยากรและดำเนินการต่างๆโดยใช้ PreMiD API
published: true
date: 12 ก.พ 2563 22:06 น.
tags:
---

# API

> เส้นทาง URL: https://api.premid.app/ 
> 
> {.is-info}

## API Versioning
> Some API and Gateway versions are now deprecated and are labeled as discontinued in the table below for posterity. 
> 
> {.is-danger}

PreMiD exposes different versions of our API. You can specify version by including it in the request path like `https://api.premid.app/v{version_number}`. Omitting the version number from the route will route requests to the current default version (marked below accordingly).

## Encryption

All HTTP-layer services and protocols (e.g. http) within the PreMiD API use TLS 1.2.

# เอกสาร
> Currently under construction! 
> 
> {.is-danger}

**Choose the API version:**
- [v1 *deprecated*](/dev/api/v1)
- [v2 *active*](/dev/api/v2)
{.links-list}