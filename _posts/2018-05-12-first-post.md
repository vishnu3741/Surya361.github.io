---
layout: post
title: Finally a home for my thoughts
tags:
  - random
  - exciting-stuff
published: true
---
I had sunteja.com for about 2 years, during which i hosted it on aws for an year on t2.nano, using the lamp stack (100qps and the vm would go haywire). once my aws-free tire credits were exausted (I didnt want to pay for hosting), i parked my domain and it stayed there until it expired. during the period it was parked, i looked into hosting a blog on [medium](https://medium.com), but sadly they stopped issuing [custom domains](https://help.medium.com/hc/en-us/articles/115003053487-Custom-Domain-FAQ) as a feature(may be having too many vhosts is slowing down their lbs)i was disappointed and let the domain expire.

eventhough i knew about github pages(i didnt know about custom domains though), i was a bit lazy to  code and also i'm lousy at designing UI's, but after a lot of postpoing here it is.

I have couple of compains though, while the instustry is pushing towards standardising https, github still doesnt support it for custom domains, they could have easily written a lets-encrypt bot to fetch certificates and do ssl offloading, the next one is A records, asking customers to point their naked A records to github ips is a bad desing in my opinion, deprecating these ips for github will be pain in the ass(may be they want to move to aws/gce), if ever in the future they want to depricate the ips, they have to ask all the developers who are using custom domains to point their naked A records to the new set, and wait till there are no requests on the old ips to shutdown (if they want an smooth transition) instead github could have given only CNAME on a subdomain and seamlessly moved ips around (the later might be biased concern of a  devops/sre)

Anyway finally i got it done so Im happy. Cheers

UPDATE: github [is rolling out https support for custom domains](https://blog.github.com/2018-05-01-github-pages-custom-domains-https/) in partnership with lets encrypt, they also included information about ANAME, ALIAS records in their documentation for supported dns providers
