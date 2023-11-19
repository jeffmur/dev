---
title: about
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

<object data="/assets/pdf/resume.pdf" type="application/pdf" width="800px" height="800px">
    <embed src="/assets/pdf/resume.pdf" type="application/pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="/assets/pdf/resume.pdf">Download PDF</a>.</p>
    </embed>
</object>
