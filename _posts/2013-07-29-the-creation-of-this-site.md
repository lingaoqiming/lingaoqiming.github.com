---
Time-stamp: <2013-07-28 20:19:16 ()>
layout: default
title: "The Creation of This Site"
tags: []

---

Since I just put together my site I do not have any posts, so I'm
going to make my first post about how I built the site that allowed me
to make this post. If you are looking to start a site, feel free to
take anything that you find here, just if you use something that
someone else is the author of, give [credit](/credits) to them.  I
will be sure to mention along the way if I was not the original offer
or if it was influenced by someone else. If it is something that I
wrote, you do not need to credit me (although you can if you would
like), I just hope that it is useful.


## Getting Started

I have been meaning to put together a site for quite a while, I just
have never got around to actually doing it until now. The reason was
mostly a combination of deciding on a domain name, a
CMS/framework/template engine to use, and where to host it.


### Domain Name

Alright, this one was pretty easy, I have actually owned this domain
for a while now, I just was not doing anything with it. I got it from
[Domains At Cost](http://www.domainsatcost.ca/) and I have never had a
problem with them, I am not saying they are the best out there (since
I have only bought a domain through them), but if you don't know where
to purchase your domain, you should be safe going there.


### (CMS | Framework | Template Engine)

The solution to this problem came when a friend of mine mentioned
[Jekyll](http://jekyllrb.com/) and said that I should check it out, so
I did. It had a perfect balance of power and simplicity about it, and
I really enjoyed that everything about it was managed by a directory
structure and variables located in the files. I spend most of my time
in my editor (I am not going to say which one because it does not
matter) and in a terminal, so the idea of managing my site from there
instead of some shittily (is that even a word?) designed admin panel
in some CMS was an instant plus for Jekyll. So, I installed Jekyll on
my local machine and played around with it a for a little bit, quickly
realizing that I had found a template engine that I could *actually*
stand using.



### Where do I host this thing that no one is going to read?

The next big question is "Where do I host my site?". I found the
answer to this at the bottom of Jekyll's home page: "Free hosting with
GitHub pages". I've been using GitHub for a little while and somehow
had never heard of this before. So, I hopped on over to GitHub and low
and behold, free hosting with direct support for Jekyll; beautiful.

All you have to do is make a repo with the name `USERNAME.github.io`
and within a few minutes your site will be served at
`http://USERNAME.github.io`. Now, if you have your own domain, you can
easily have GitHub serve your site from your custom domain, you can
follow the
[instructions](https://help.github.com/articles/setting-up-a-custom-domain-with-pages)
on GitHub's site.

Once you create the repo, you can have it
[auto-generate](https://help.github.com/articles/creating-pages-with-the-automatic-generator)
a website for you. That's what I did and just proceeded to tweak it
from there. You may notice that the theme I am using is one of the
default themes created by
[mattgraham](https://twitter.com/michigangraham) tweaked to my liking.


## The Site

This site has a couple main pieces to it:

- My bio
- The blog
- Projects
- Resources

The best way to write pages (IMHO) is to define a layout in `_layouts`
that has all the header, footer, and navigation code and just has a
content section that will get filled in by each of the pages. I just
have a `default` layout that I use for every page, haven't found a
reason yet to define more than one.


### My Bio

This part is pretty straight forward, it's just a markdown file of me
talking about myself served at the root of the site (so you have to
read it haha), so lets move on.

### The Blog

Nicely, Jekyll is blog aware so it handles blog entries really nicely,
all you have to do is make a file in `/_posts` with a name like
`YYYY-MM-DD-name-of-post.md` and you can easily loop through all of
your posts and link to them and do other cool stuff. If you go to
[/blog](/blog), you willl notice that at the top there is a list of 
all of my blog entries (only one when I wrote this), and below that is
a tag cloud.

The list of posts is pretty easy to generate, there is a `site`
variable called `posts` which is a list of all the blog entries that
you have written, so you can just loop through them and turn them into
links. Just take a look at the
[source](https://raw.github.com/mrenaud92/mrenaud92.github.io/master/blog/index.md).

Underneath that is a tag cloud which I got from
[enrmarc](https://github.com/enrmarc/jekyll-tagcloud).


### Projects

This page just contains a few of the projects that I've worked on with
a little description of each. As of this writing, there isn't anything
on that page yet (not because I haven't done anything), I'll update it
eventually.


### Resources

This is one of the biggest reasons that I wanted to have a site, so
that I could centralize and index a bunch of resources (code,
explanations, links) so that I can point people here as opposed to
sifting through bookmarks and old notes to find where something is.

What I wanted to have was a categorized list of pages, with some pages
able to appear in muliple categories, and able to have some resources
that weren't indexed. I searched around for a bit on a nice, robust
way of doing this but to no avail. So, I sat down and figured out a
scalable way of doing it. I found a
[question](http://stackoverflow.com/questions/17118551/jekyll-generating-a-list-of-pages-not-posts-in-a-given-category/17913214#17913214)
on Stack Overflow from someone who wanted to do something very
similar and wrote a detailed response there so other people can find
it. A *top answer* was already chosen that didn't really fully answer
the question so hopefully people scroll down a little bit. If you find
the answer useful, remember to up vote it so it's more visible.


## Conclusion

Well, that's about it. If you are interested in using Jekyll, check
out the documentation on it's site, make a GitHub page, play around
with it, make it your own.
