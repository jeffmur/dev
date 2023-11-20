---
title: About 🧑‍💻
permalink: /about/
layout: page
excerpt: Contact information and resume
comments: false
---



### Contact Me ✨

- {{ site.author.email }}
- github.com/{{ site.author.github }}
- linkedin.com/in/{{ site.author.linkedin }}

### Resume 📰

<p>Last Modified: <span class="post-item-date" id="lastModified"></span></p>

<script>
    const date = new Date(document.lastModified);
    document.getElementById("lastModified").innerHTML = date.toDateString();
</script>

<a href="/assets/pdf/Murray-Jeffrey-Resume.pdf" target="_blank">View PDF</a>

