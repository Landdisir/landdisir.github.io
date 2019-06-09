---
layout: post
title: Making This Website
---
Making this site was a real adventure. Mostly because I know very little as of right now so everything feels so foreign.
Right off the bat after forking and filling out basic info in config.yml, I ran into an issue

{% highlight ruby %}
"Deprecation: The 'gems' configuration option has been renamed to 'plugins'. Please update your config file accordingly."
{% endhighlight %}

Turns out all I needed to do was change a single word
{% highlight ruby %}"gems: [jekyll-paginate]" => "plugins: [jekyll-paginate]"
{% endhighlight %}

Currently seeing an issue with
{% highlight ruby %}
"Liquid Warning: Liquid syntax error (line 36): Expected id but found pipe in "{{ post.excerpt | | strip_html | strip_newlines | truncate: 120 }}" in index.html".
{% endhighlight %}

It'll go away if I add spaces between the double curly brackets but then it ruins the posts excerpt as seen below:
![Before](/img/making-site-before.png){: .center-image}
![After](/img/making-site-after.png){: .center-image}

We'll see how this goes later, just wanted to get this started.

Till next time!
