---
layout: blog_page
title: "AtoZ Sass Intro: Installing Sass"
category: blog
excerpt: >
  In the previous post we learned what Sass is, where is came from and
  its different syntaxes and compilers. 
  
  In this post, we'll look at a couple of ways to install Sass and set up
  our development environment.
---

This is part 2 of a 4-part introductory series to Sass in preparation
for the video series [AtoZ Sass](http://www.atozsass.com).

* Part 1: [What is Sass](/blog/what-is-sass)
* Part 2: [Installing Sass](/blog/installing-sass)
* Part 3: [Organising Sass with Partials](/blog/organising-sass-with-partials)
* Part 4: [Variables, Mixins and Nested Selectors](/blog/sass-variables-nesting-and-mixins)

In the previous post we learned what Sass is, where is came from and
its different syntaxes and compilers. 

In this post, we'll look at a couple of ways to install Sass and set up
our development environment.

I'll show you how few steps there are in getting up and running from the
command line on a Mac and then go through a load of resources for
using Sass with a GUI (Graphical User Interface) application and for
Windows.


## Installing Sass on the Command Line

Every Mac has an application called "terminal" which enables power users
to control their machine by issuing a series of commands. It's not the
most attractive interface in the world but it's very fast to work with
once you get over the learning curve.

There are other terminal apps available that have a number of extra
useful features if you want to really level up your command line skills.
My preference is [iTerm2](http://www.iterm2.com) but for installing and
compile Sass, the default terminal app is absolutely fine. 

We're going to install Ruby Sass. If you're on a Mac, Ruby will be
installed by default but you may need to install RubyGems. 

Details of installation can be found on the [RubyGems
website](https://rubygems.org/pages/download). 

If you're on Windows, there are instructions to help you get Sass
installed on the [sass-lang.com](http://sass-lang.com/install) website.

With Ruby and RubyGems installed, we can now install Sass. In the
terminal, type the following command: 

{% highlight bash %}
gem install sass
{% endhighlight %}

All being well, you should see a success message along the lines of 
	
{% highlight bash %}
1 gem installed
{% endhighlight %}

Congratulations, you're done. That was pretty painless, wasn't it?

If you're not keen on the command line, there's a section below about
various apps and tools to help you get up and running. But do give the
terminal a try - it's just a matter of getting used to it.


## Compiling Sass

Now that Sass is installed, we're ready to write some Sass code and
compile it. Follow these steps to set up a Sass project and practice
compiling your code on the command line.

First, create a folder for this demo project called "sass-project".
Inside that folder create a sub-folder called `scss` and another one
called `css`. The `scss` folder will hold our Sass files and the `css`
folder is where the CSS will be compiled to. You should have a folder
structure as follows:

{% highlight bash %}
sass-project
|- scss
|- css
{% endhighlight %}

Into the `scss` folder, create a file called `style.scss`. 

{% highlight bash %}
sass-project
|- scss
   |- style.scss
|- css
{% endhighlight %}

Using your favourite text editor, add some CSS to the `style.scss`
file. It can be any valid CSS code at all as any valid CSS is also valid *Sass*.
Below is some sample code you can use:

{% highlight css %}
body {
	color: #333;
	font-size: 100%:
	font-family: 'Avenir', 'Arial', sans-serif;
}
a {
	color: #f00;
	text-decoration:none;
}
{% endhighlight %}

Now that we have some Sass code to work with, we can run the compiler
and see what happens.

Back in the terminal, we can use the `sass` command to compile our code.
We need to provide details of the path to our Sass file and the path
that we want our CSS compiled to.

We can do that with the following command:

{% highlight bash %}
sass scss/style.scss:css/style.css
{% endhighlight %}

The input path `scss/style.scss` is separated from the output path
`css/style.css` by a `:` colon character. You can choose any name for
the compiled CSS file but it's conventional to use the same name as the
Sass file.

Having run this command our Sass has been compiled. If we open the
`style.css` file in a text editor, we'll be able to see some almost
identical code within. 

Below is what's generated by running the Sass compiler:

{% highlight css %}
body {
	color: #333;
	font-size: 100%:
	font-family: 'Avenir', 'Arial', sans-serif; }
a {
	color: #f00;
	text-decoration:none; }
{% endhighlight %}

It would be a bit tedious to have to run the compiler manually every
time we made a change to our Sass but fortunately, the compiler has
a `--watch` option which will constantly watch our files for changes and
recompile whenever we save.

To automatically compile run the following command:

{% highlight bash %}
sass scss/style.scss:css/style.css --watch
{% endhighlight %}

Now any further changes will be detected by Sass and compiled
automatically.

At the moment we're just writing normal CSS but in the next post in this
series, we'll start diving into some of the fancier features and write
some Sassy CSS.

But before we wrap this up, let me share some resources for those that
prefer a more visual interface rather than typing out commands one by
one into a terminal.

## Apps for Preprocessing

For me, the command line is the quickest way to get up and running and
work with Sass. But I know it's not everyone's cup of tea and not
everyone works on a Mac. Here's a selection of apps for compiling Sass
(and other preprocessors).

There's [CodeKit](http://incident57.com/codekit/) which is
a full-featured paid product that does a lot more than just compile Sass
files. I've not used it myself but I've heard really good things.

Other paid apps include [Ghost Lab](http://www.vanamco.com/ghostlab),
[LiveReload](http://livereload.com/) and [Preprocs](https://prepros.io/).
Codekit is Mac only but the others are all cross-platform.

There's also a selection of free or open source solutions such as
[Compass App](http://compass.handlino.com/),
[Koala](http://koala-app.com/) and
[Scout](http://mhs.github.io/scout-app/)

When I teach beginner Sass classes in person, I recommend Koala as it
works on both Mac and PC and has a very minimal, simple interface which
makes it quick to learn and get familiar with.

So, with a good understanding of [what Sass is](/blog/what-is-sass) and our
development environment all set up and our compiler watching for
changes, we're ready to start working with Sass. 

Sign up to the mailing list below to ensure you don't miss the next
installment of this series which will be all about file organisation.

If you're new round here, why not check out the first 26 episodes in
AtoZ CSS Season 1 and if you can't get enough CSS goodness, I have an
ebook all about CSS layout for you at
[atozcss.com/books](http://www.atozcss.com/books).

As always, if you have any questions or comments, you can tweet me
[@guyroutledge](http://www.twitter.com/guyroutledge) or drop me an email.

## Other Posts in this Series

* Part 1: [What is Sass](/blog/what-is-sass)
* Part 2: [Installing Sass](/blog/installing-sass)
* Part 3: [Organising Sass with Partials](/blog/organising-sass-with-partials)
* Part 4: [Variables, Mixins and Nested Selectors](/blog/sass-variables-nesting-and-mixins)
