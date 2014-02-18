# Wordpress Meetup 18.02.2014

## WordPress as team communication tool (Ruben)

WordPress has **evolved** from blogging system to full website (community, communication, ...).

Using [P2](http://p2theme.com/), you can have a private communication website, quite useful for teams. It provides a clean & simple system to communicate, a bit Twitter-like. It also provides an e-mail notification tool.

Cleaned the mailbox usage by 1/3, so quite useful. It provides a place to share less important stuffs, inspiration, links, ...

Automattic use it internally : [reference](http://ma.tt/2009/05/how-p2-changed-automattic/)
A new version is coming, [called 02](http://www.slideshare.net/beaulebens/o2-wcsf2013). (it's [available here](http://geto2.com/))

**Downside** : P2 theme conflicts a lot with other plugins.

// hipchat

## Sell Media Presentation (Eric)

Quite all-in-one plugin, but hard to modify as it seems oriented towards *simple users*.

Allow you to specify a lot of parameters, variations of a single product.

Integrate a Paypal and an e-mail system. Allows you to bluk upload items and set parameters.

Product is free but you have to pay for the support.

It's [available here](http://graphpaperpress.com/plugins/sell-media/)

## Site critic

**How can you modify user roles to work with Custom Post Types ?**
You've got to modify user roles capabilities to allow edit/post custom post types. You set up those capabilities when making custom post types and you assign them to user roles, so those roles can handle those capabilities.

**How can I modify the post excerpt & featuered image on my site? [MaggieFearn](http://maggiefearn.com/blog/)**
You've got to build a template pulling in the last XX blogposts and then just use the featured image capability and the title. Which will render something like this :

	<h1 itemprop="headline" class="post-title"><a href="<?php the_permalink() ?>" rel="bookmark" title="<?php _e('Link to','theme'); ?> <?php the_title_attribute(); ?>" itemprop="url"><?php the_title(); ?></a></h1>

	<a href="<?php the_permalink() ?>" rel="bookmark" title="<?php _e('Link to','theme'); ?><?php the_post_thumbnail('home-thumb', array('class' => 'featthumb', 'alt' => ''.get_the_title().'', 'title' => ''.get_the_title().'')); ?></a>

**How can I change my website font?**
There a a lot of Fonts, like [Google Fonts plugin](http://wordpress.org/plugins/wp-google-fonts/) allowing you to simply modify your website fonts.

**Get back the follow button from Wordpress.com ?**
Install [Jetpack](https://wordpress.org/plugins/jetpack/). Then you just contact Automattic Support so they move your suscribers from your old Wordpress.com site to your brand new self hosted WordPress installation

**How to boost my website speed?**
Pay attention to the things you load (social share buttons for example), install some cache and minification plugins. Here's a [cache plugin](http://wordpress.org/plugins/w3-total-cache/).