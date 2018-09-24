---
layout: post
title: Finally a home for my thoughts
tags:
  - random
  - exciting-stuff
published: true
---
I had sunteja.com for about 2 years, during which i hosted it on aws for an year on t2.nano(100qps and the vm would go haywire). once my aws-free tire credits were exausted (I didnt want to pay for hosting), i parked with domain monetisation until it expired. i looked at alternative hostings such as [medium](https://medium.com), but was not happy with their offering since they stopped providing [custom domains](https://help.medium.com/hc/en-us/articles/115003053487-Custom-Domain-FAQ) may be having too many vhosts is slowing down their lbs.

after a lot of searching i came across github pages, at first i didnt know that github provided custom domains, after a lot of indolence (also i'm lousy at designing UI's),here it is.

I have couple of compains though, while the industry is pushing for https as the default webprotocol, github still doesnt support it for custom domains, they could have easily written a lets-encrypt bot to auto-generate certificates and push it to their lbs to do ssl offloading, the next one is A records, asking customers to point their naked A records to github ips is a bad design, deprecating these ips for github will be pain, if ever in future they want to depricate the ips, they have to ask all the respective domain holders to point their dns to the new set, and wait till there are no requests on the old ips (if they dont want to loose any traffic) instead github could have given only CNAME on a subdomain and seamlessly moved ips around (the later might be biased concern of a devops/sre)

Anyway finally i got it done.

UPDATE: github [is rolling out https support for custom domains](https://blog.github.com/2018-05-01-github-pages-custom-domains-https/) in partnership with lets encrypt, they also included information about ANAME, ALIAS records in their documentation for supported dns providers
