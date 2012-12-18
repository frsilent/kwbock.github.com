---
layout: default
title: Kyle Bock
---
<div class="row-fluid">
    <div class="span12 well">
        This is the future home of my blog. I'm hoping to use this place to write about interesting projects I'm working on or as a place to write about intersting tools or tips found while working on my projects. More to come soon.
    </div>
</div>

<div class="row-fluid">
    <div class="span8 ">
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
    </div>
    <div class="span4">
        <aside class="well">
            <header>
                <legend><h4>Projects</h4></legend>
            </header>
            <div class="aside-content">
                <ul>
                    <li><a href="http://github.com/kwbock/clipster">Clipster</a></li>
                    <li><a href="http://github.com/kwbock/KBButton">KBButton</a></li>
                    <li><a href="http://github.com/kwbock/KBTextField">KBTextField</a></li>
                </ul>
            </div>
        </aside>
        <aside class="well">
            <header>
                <legend><h4>Categories</h4></legend>
            </header>
            <div class="aside-content">

            </div>
        </aside>
    </div>
</div>