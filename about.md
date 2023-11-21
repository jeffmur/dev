---
title: About 🧑‍💻
permalink: /about/
layout: page
excerpt: Contact information and resume
comments: false
---

![](/assets/img/banner.png)

I am Jeffrey Murray Jr, a passionate software developer. Welcome to my personal blog, a platform where I explore various topics and showcase my projects. I am drawn towards solving complex problems, driven by an insatiable eagerness to learn. While writing isn’t my strongest suit, this blog is my commitment to not only improve my articulation skills but also to share comprehensive articles on subjects that fascinate me, with the help of [ChatGPT](https://chat.openai.com) of course.

### Contact ✨

- Email me: [{{ site.author.email }}](mailto:{{ site.author.email }})
- View my projects: [github.com/{{ site.author.github }}](https://github.com/{{ site.author.github }})
- Connect with me: [linkedin.com/in/{{ site.author.linkedin }}](https://linkedin.com/in/{{ site.author.linkedin }})

### Resume 📰

<p>Last Modified: <span class="post-item-date" id="lastModified"></span>

<script>
    const date = new Date(document.lastModified);
    document.getElementById("lastModified").innerHTML = date.toDateString();
</script>
<br>
<a href="{{ site.author.resume }}" target="_blank">View Resume</a>

</p>