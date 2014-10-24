---
layout: post
title:  Setting up this blog with Jekyll, GitHub and CloudFlare.
date:   2014-10-24 14:13:24
tags:   jekyll tech
author: Jonathan E. Magen
---

For this blog, we chose to use a tool called [Jekyll][jekyll]. We
based this decision on multiple factors after a detailed comparison of
other site-building and blog-building tools. Jekyll is a mature piece
of software with a vibrant community and the backing of GitHub itself.
GitHub uses Jekyll to power their [GitHub Pages][github-pages] feature
since Jekyll requires no server-side software. It generates static
HTML files which you can serve up with minimal overhead from anywhere,
making our blog highly-portable in the event we decide to move away
from GitHub pages.

Jekyll lets you author pages in a lightweight format like
[Markdown][commonmark] which it then compiles and converts into static
HTML complete with an asset pipeline for generating web-optimized
resources. Plus there was [an emoji plugin][emoji-plugin] :smile:.

After following the excellent documentation and customizing some of
the base details, we were ready to give deployment a shot. Jekyll has
a special `_site` directory into which it places your compiled,
ready-to-deploy pages and assets.

Once we had deployed our site to GitHub Pages, it was time to
configure a special subdomain. We happily employ CloudFlare's security
services to provide us with protection from [DDoS][ddos] attacks and
other threats, in addition to their awesome caching layer. Since
configuring CloudFlare requires moving over one's DNS entries, it
became necessary for us to add a CNAME entry to CloudFlare's excellent
DNS manager.

Ultimately, we were able to go from zero to blog in a morning.

[commonmark]:    http://commonmark.org
[github-pages]:  https://pages.github.com
[github]:        https://github.com
[jekyll]:        http://jekyllrb.com
[emoji-plugin]:  https://github.com/yihangho/emoji-for-jekyll
[cloudflare]:    https://cloudflare.com
[ddos]:          https://en.wikipedia.org/wiki/Denial-of-service_attack
