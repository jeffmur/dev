---
title: About 🧑‍💻
permalink: /about/
layout: page
excerpt: Contact information and resume
comments: false
---



### Contact ✨

- Email me: [{{ site.author.email }}](mailto:{{ site.author.email }})
- View my projects: [github.com/{{ site.author.github }}](https://github.com/{{ site.author.github }})
- Connect with me: [linkedin.com/in/{{ site.author.linkedin }}](https://linkedin.com/in/{{ site.author.linkedin }})

### Resume 📰

<p>Last Modified: <span class="post-item-date" id="lastModified"></span></p>

<script>
    const date = new Date(document.lastModified);
    document.getElementById("lastModified").innerHTML = date.toDateString();
</script>

<a href="{{ site.author.resume }}" target="_blank">View Resume</a>

