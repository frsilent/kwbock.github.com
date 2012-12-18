---
layout: default
title: Kyle Bock
show_about: False
---
<section class="posts">
    {% for post in site.posts %}
    <article class="post well">
        <header>
            <legend>
                <h4><a href="{{ post.url }}">{{ post.title }}</a></h4>
            </legend>
        </header>
        <div class="post-content">
            {{ post.content }}
        </div>
        <footer>
        </footer>
    </article>
    {% endfor %}
</section>
