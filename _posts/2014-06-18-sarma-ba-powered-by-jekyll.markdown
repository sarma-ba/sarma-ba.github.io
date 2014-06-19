---
layout: post
title:  "Sarma.ba je live. Powered by Jekyll and Github Pages!"
author: "mribica"
author-link: "https://twitter.com/mribica"
date:   2014-06-18 14:24:41
categories: sarma
---

Napokon je lansirana i zvanična stranica za Sarma: Sarajevo Ruby meetups. Koristimo [jekyll][jekyll] uz podršku [GitHub stranica][github-pg].

{% highlight ruby %}
def hello
  puts "Vozdra, raja!"
end
{% endhighlight %}

## Instalacija

Želite sličnu stranicu za sebe? Instalirajte jekyll gem:

~~~
$ gem install jekyll
~~~

## Kreiranje projekta

Da bi kreirani projekat bio kompatibilan sa standardom GitHub stranica potrebno je ispravno imenovati projekat.
Za privatne račune treba koristiti ime `[username].github.io`, odnosno `[organization-name].github.io` za GitHub organizacije.

U slučaju [sarma-ba](https://github.com/sarma-ba) organizacije, kreirali smo projekat na sljedeći način:

~~~
$ jekyll new sarma-ba.github.io
~~~

## Testiranje

Jako je praktično i kroisno moći testirati stranicu dok je razvijate.
Lagano možemo testirati pokretanjem lokalnog servera:

~~~
$ jekyll server
  http://0.0.0.0:4000/
~~~

## Deploy

~~~
$ git push
~~~

Nakon `git push`-a GitHub pages automatski preuzima sadržaj iz `master` brancha i servira ga kao GitHub stranicu.

## Napomene

~~~
$ jekyll server --watch
~~~

Pokreće lokalni server, prati izmjene i automatski rekreira nove stranice.

**Napomena**: Nakon svake izmjene `_config.yml` fajla je potrebno ponovo pokrenuti server.

### Twitter Share

U `_config.yml` dodati `username: [vaš twitter handle]` i na kraju `_layouts/post.html` dodati:

~~~
<a href="https://twitter.com/share" class="twitter-share-button" data-via="{{ site.username }}">Tweet</a>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
~~~

[jekyll]:    http://jekyllrb.com
[github-pg]: https://pages.github.com
[author-name]: mribica
[author-link]: https://twitter.com/mribica
