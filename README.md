![DK Hostmaster Logo][DKHMLOGO]

# DK Hostmaster Self-service Portal Service Specification

[![Markdownlint Action](https://github.com/DK-Hostmaster/sb-service-specification/actions/workflows/markdownlint.yml/badge.svg)](https://github.com/DK-Hostmaster/sb-service-specification/actions/workflows/markdownlint.yml)
[![Spellcheck Action](https://github.com/DK-Hostmaster/sb-service-specification/actions/workflows/spelling.yml/badge.svg)](https://github.com/DK-Hostmaster/sb-service-specification/actions/workflows/spelling.yml)

X.X 2021-09-16
Revision X.X

<!-- MarkdownTOC bracket=round levels="1,2,3,4,5" indent="  " autolink="true" autoanchor="true" -->

- [Introduction](#introduction)
  - [About this Document](#about-this-document)
  - [License](#license)
  - [Document History](#document-history)
  - [The .dk Registry in Brief](#the-dk-registry-in-brief)
- [SB in Brief](#sb-in-brief)
- [SB Service](#sb-service)
  - [SSL/TLS Support](#ssltls-support)
  - [Available Environments](#available-environments)
    - [production](#production)
- [Features](#features)
  - [Authorize Change Name Servers](#authorise-change-name-servers)
  - [Authorize Change Registrar](#authorise-change-registrar)
- [References](#references)
- [Resources](#resources)
  - [Mailing list](#mailing-list)
  - [Issue Reporting](#issue-reporting)
- [Appendices](#appendices)

<!-- /MarkdownTOC -->

<a id="introduction"></a>

## Introduction

This document describes the registrar self-service portal (RP) offered by DK Hostmaster.

The document is targeted at registrars as audience.

<a id="about-this-document"></a>

### About this Document

This specification describes version 5.X.X of the DK Hostmaster Self-service portal (SB). Future releases will be reflected in updates to this specification, please see the document history section below.

The documentation is aimed at registrars for support of end-customers interacting with SB.

Do note that the specification describes the latest released service. Service version is listed in the Document History, so given changes implemented in the service are reflected in the specification.

Any future additions and changes to the implementation are not within the scope of this document and will not be discussed or mentioned throughout this document.

This document is owned and maintained by DK Hostmaster A/S and must not be distributed without this information.

All examples provided in the document are fabricated or changed from real data to demonstrate request and operations etc. any resemblance to actual data are coincidental.

This document is not the authoritative source for business and policy rules and possible discrepancies between this an any authoritative sources are regarded as errors in this document. This document is aimed at being the external technical specification and describes the implementation facing the users and is an interpretation of authoritative sources and can therefor be erroneous.

<a id="license"></a>

### License

This document is copyright by DK Hostmaster A/S and is licensed under the MIT License, please see the separate LICENSE file for details.

<a id="document-history"></a>

### Document History

X.X 2021-09-16

- Initial revision
- Describes service version 5.0.0

<a id="the-dk-registry-in-brief"></a>

### The .dk Registry in Brief

DK Hostmaster is the registry for the ccTLD for Denmark (dk). The current model used in Denmark is based on a sole registry, with DK Hostmaster maintaining the central DNS registry.

<a id="sb-in-brief"></a>

## SB in Brief

SB is a web based service aimed at registrants and other non-registrar end-users, for interacting with the DK Hostmaster registry.

<a id="sb-service"></a>

## SB Service

<a id="ssltls-support"></a>

### SSL/TLS Support

The SB service supports the following protocols for transport security:

- TLSv1.2

<a id="available-environments"></a>

### Available Environments

DK Hostmaster offers the following two environments:

- production

Updates to both environments are announced via the tech-announce mailing list.

Please see the [information page][DKHMMAIL] for details on subscribing etc.

<a id="production"></a>

#### production

- `https://sb.dk-hostmaster.dk/`

<a id="features"></a>

## Features

<a id="authorise-change-name-servers"></a>

### Authorise Change Name Servers

1. Log in to the self-service portal
2. Find the domain name in the list of domain names you want to work on
3. Click on the domain name to go to the detailed overview
4. On the detail page, locate the section "Authorisations codes" on the right side of the page
5. Click "Change Name Servers" to go to the page to generate the authorisation code
6. Click "GENERATE CODE"

A code is now generated, this code should be provided to the registrar or name server administrator to whom the user wants to use for name service.

Once the code is in the possession of the registrar, it can be used to execute the actual.

The authorisation code works:

- Only for a single domain name
- Only for a single operation
- Has a lifespan of 14 days
- Can be replace with a new code
- Can be deleted, meaning the authorisation is retracted

<a id="authorise-change-registrar"></a>

### Authorise Change Registrar

1. Log in to the self-service portal
2. Find the domain name in the list of domain names you want to work on
3. Click on the domain name to go to the detailed overview
4. On the detail page, locate the section "Authorisations codes" on the right side of the page
5. Click "Change To Registrar Management" or "Change Registrar" to go to the page to generate the authorisation code
6. Click "GENERATE CODE"

A code is now generated, this code should be provided to the registrar to whom the registrant wants to transfer.

Once the code is in the possession of the registrar, it can be used to execute the actual operation of transferring the domain name.

The authorisation code works:

- Only for a single domain name
- Only for a single operation
- Has a lifespan of 14 days
- Can be replace with a new code
- Can be deleted, meaning the authorisation is retracted

<a id="references"></a>

## References

List of references used in this document in alphabetical order.

<a id="resources"></a>

## Resources

A list of resources for the DK Hostmaster Self-service Portal support is located below.

<a id="mailing-list"></a>

### Mailing list

DK Hostmaster operates a mailing list for technical discussion and inquiries about the DK Hostmaster offerings. To subscribe to this list, write to the address below and follow the instructions. Please note that the list is for technical discussion only, any issues beyond the technical scope will not be responded to, please send these to the contact issue reporting address below and they will be passed on to the appropriate entities within DK Hostmaster.

- tech-discuss+subscribe@liste.dk-hostmaster.dk

<a id="issue-reporting"></a>

### Issue Reporting

For issue reporting related to this specification, the RP implementation or test, sandbox or production environments, please contact us. You are of course welcome to post these to the mailing list mentioned above, otherwise use the regular support channels.

<a id="appendices"></a>

## Appendices

[DKHMLOGO]: https://www.dk-hostmaster.dk/sites/default/files/dk-logo_0.png
[DKHMMAIL]: https://www.dk-hostmaster.dk/en/mailing-lists
