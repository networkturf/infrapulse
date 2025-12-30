---
layout: post
title: "Understanding BGP Communities for Traffic Engineering"
date: 2024-02-10
author: Kunal Vaidya
tags:
  - BGP
  - Networking
  - Routing
  - Traffic Engineering
---

BGP communities are a powerful mechanism for traffic engineering and route manipulation. In this post, we'll dive deep into how BGP communities work and how to use them effectively.

## What are BGP Communities?

BGP communities are 32-bit values that can be attached to BGP routes to mark them for special treatment. They allow you to group routes and apply policies based on these groups.

## Standard Communities

The most common format is the ASN:Value format:

```
65000:100
```

Where:
- `65000` is the AS number
- `100` is the community value

## Well-Known Communities

There are several well-known communities that have standard meanings:

- `no-export` (65535:65281): Don't advertise to eBGP peers
- `no-advertise` (65535:65282): Don't advertise to any peer
- `local-as` (65535:65283): Don't advertise outside local AS

## Practical Example

Here's how you might use communities to control traffic:

```cisco
route-map SET-COMMUNITY permit 10
  set community 65000:100 additive

route-map FILTER-BY-COMMUNITY permit 10
  match community 1
  set local-preference 200

ip community-list 1 permit 65000:100
```

## Use Cases

1. **Traffic Engineering**: Prefer certain paths based on community values
2. **Route Filtering**: Filter routes at peering points
3. **DDoS Mitigation**: Mark routes for scrubbing
4. **Cost Optimization**: Route traffic through cheaper links

## Best Practices

- Document your community values
- Use consistent numbering schemes
- Consider using extended communities for more complex scenarios
- Test community policies in a lab before deploying

BGP communities are a fundamental tool for any network engineer working with BGP. Master them, and you'll have fine-grained control over your routing policies.

