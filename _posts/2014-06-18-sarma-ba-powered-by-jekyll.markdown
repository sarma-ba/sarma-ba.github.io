---
layout: post
title:  "Sarma.ba je live. Powered by Jekyll and Github Pages!"
author: "mribica"
author-link: "https://twitter.com/mribica"
date:   2014-06-18 14:24:41
categories: sarma
---

Lansirana je zvanicna stranica sarma.ba Sarajevo Ruby Meetup-a. Koristimo [jekyll][jekyll] uz podrsku [github stranica][github-pg].

{% highlight ruby %}
def hello
  puts "Vozdra, raja!"
end
{% endhighlight %}

## Instalacija

~~~ 
$ gem install jekyll
~~~

## Kreiranje projekta

Da bi kreirani projekat bio kompatibilan sa standardom github stranica potrebno je ispravno imenovati projekat.
Za privatne racunu `username.github.io` ili za github organizacije `organization-name.github.io`.

U slucaju `sarma-ba organizacije` koja se nalazi na `https://github.com/sarma-ba` kreiramo projekat:

~~~
$ jekyll new sarma-ba.github.io
~~~

## Testiranje

~~~ 
$ jekyll server
  http://0.0.0.0:4000/
~~~

## Deploy

~~~
$ git push
~~~

Nakon `git push` github pages automatski preuzima sadrzaj i `master` brancha i servira kao github stranicu.

## Napomene

~~~
$ jekyll server --watch
~~~

Pokrece lokalni server, prati izmjene i automatski rekreira nove stranice.
Nakon svake izmjene `_config.yml` potrebno je ponovo pokrenuti server.

### Twitter Share

U `_config.yml` dodati `twitter_username: [vas twitter handle]` i na kraju `_layouts/post.html` dodati: 

~~~
<a href="https://twitter.com/share" class="twitter-share-button" data-via="{{ site.username }}">Tweet</a>
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0];if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src="//platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
~~~


[jekyll]:    http://jekyllrb.com
[github-pg]: https://github.io
[author-name]: mribica
[author-link]: https://twitter.com/mribica
