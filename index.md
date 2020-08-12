---
layout: home
---

I’m a software engineer working at the intersection of entertainment and technology. We’re talkin’ visual effects, VR / AR, and game development.

<p><strong>New:</strong> {% for post in site.posts limit:1 %}
  <a href="{{ post.url }}">
            {{ post.title }}
          </a>
{% endfor %}</p>
