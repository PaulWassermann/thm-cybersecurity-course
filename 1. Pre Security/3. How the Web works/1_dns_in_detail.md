# DNS in detail

## What is DNS ?

DNS stands for Domain Name System. It maps IP addresses to legible strings like URLs.

## Domain Hierarchy

The TLD (Top-Level Domain) is the rightmost part of the domain name: e.g ".com" for "tryhackme.com". There are two types of TLD:

* gTLD (Generic TLD)       : historically, indicates the purpose of the domain
  * .com for commercial purposes
  * .org for an organisation
  * .gov for government

* ccTLD (Country Code TLD) : used for geographical purposes
  * .fr for France
  * .ca for Canada
  * ...

Second-level domain is the part just left of the TLD: e.g "tryhackme" for "tryhackme.com". The second-level domain is limited to 63 characters in [a-z0-9\-].

Finally, the part left of the second-level domain, separated by a comma, is called the subdomain. It has the same restrictions as the second-level domain.

The length of the comma-separated domains cannot exceed 253.

## Record Types

DNS allow to resolve addresses of websites obsviously, but not only. There are different types of records:

* A record     : resolves to an IPv4 address
* AAAA record  : resolves to and IPv6 addess
* CNAME record : resolves to another domain (e.g. "store.tryhackme.com" → "shops.shopify.com")
* MX record    : resolves to the address of the mail server associated with the queried domain
* TXT record   : can have multiple uses

## Making A Request

Here is the different steps when making a DNS request:

1) LOCAL CACHE: First, the computer checks it local cache to see if the domain is there; if absent, make a request to the recursive DNS server
2) RECURSIVE DNS SERVER: Acts as a remote cache, usually provided by the ISP; if absent, make a request to the root DNS server
3) ROOT DNS SERVER: DNS backbone of the internet, redirects to the adequate TLD server
4) TLD SERVER: holds records for where the find the authoritative server to answer the DNS request (also called the name server)
5) AUTHORITATIVE DNS SERVER: holds the DNS records for the domain; all DNS records stored on the server come with a TTL (Time To Live) specifying how long the recursive DNS server or the local cache should hold the record values.
