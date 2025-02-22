# Changelog

This project uses [Semantic Versioning 2.0.0](http://semver.org/).

## main

## 1.1.0

- NEW: Added getDomainRenewal and getDomainRegistration endpoints (dnsimple/dnsimple-php#72)

## 1.0.0

- BREAKING CHANGES: Wrap `GuzzleHttp\Exception\ClientException` (dnsimple/dnsimple-php#63)
  - **400** http exceptions are wrapped in `BadRequestException`
  - **404** http exceptions are wrapped in `NotFoundException`
  - All other **4xx** exceptions are wrapped in `HttpException` which the other classes inherit
  - The new exception classes come with [improved interface](src/Dnsimple/Exceptions/HttpException.php) e.g. `->getAttributeErrors()` to get validation errors.
- CHANGED: Add support for PHP ^8.0 (dnsimple-php#64)
- CHANGED: Deprecate Certificate's `contact_id` (dnsimple/dnsimple-php#46)
- CHANGED: Add documentation to CONTRIBUTING.md
- FIXES: Version number of the client

## 0.4.0

- CHANGED: Add support for DNSSEC key-data interface (dnsimple/dnsimple-php#29).

## 0.3.1

- CHANGED: Deprecates `service.getDomainPremiumPrice`

## 0.3.0

- NEW: Added `service.getDomainPrices` to retrieve whether a domain is premium, and the prices to register, transfer, and renew. (dnsimple/dnsimple-php#18)

## 0.1.0

Initial public release.
