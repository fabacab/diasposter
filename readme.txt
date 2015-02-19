=== Diasposter ===
Contributors: meitar
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=meitarm%40gmail%2ecom&lc=US&item_name=Diasposter%20WordPress%20Plugin&item_number=diasposter&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted
Tags: Diaspora, post, crosspost, publishing, post formats
Requires at least: 3.1
Tested up to: 4.1.1
Stable tag: 0.1.1
License: GPLv3
License URI: https://www.gnu.org/licenses/gpl-3.0.html

Diasposter cross-posts your WordPress entries to Diaspora. Changes to your WordPress posts are reflected in your Diaspora posts.

== Description ==

Diasposter posts to Diaspora whenever you hit the "Publish" button. Diasposter is very lightweight. It just requires you to connect to your Diaspora account from the plugin options screen. After that, you're ready to cross-post!

* **Secure:** Unlike many other Diaspora tools, this plugin *never writes your login cookie to disk* and strictly enforces encrypted connections between your blog and your Diaspora pod, so your Diaspora access credentials are kept as safe as you keep your WordPress database. This is especially important on Shared Hosting plans where many other customers have access to your server's filesystem!
* **Easy to use:** Seamlessly translates WordPress formatting to beautiful Diaspora posts, with full support for post titles, excerpts, tags, custom post types, and more.
* **Feature-rich:** Numerous additional options let you provide custom linkbacks, set global preferences and per-post settings, and more.

Diasposter uses Diaspora's simple API to keep posts in sync as much as possible; when you delete your WordPress post, your Diaspora post is removed, too. Service integrations let you control the Diaspora auto-tweet and auto-post options right from your WordPress post editing screen. You can even toggle post location sharing on or off.

*Donations for [my WordPress plugins](https://profiles.wordpress.org/meitar/#content-plugins) make up a chunk of my income. If you continue to enjoy this plugin, please consider [making a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=meitarm%40gmail%2ecom&lc=US&item_name=Diasposter%20WordPress%20Plugin&item_number=diasposter&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted). :) Thank you for your support!*

> Servers no longer serve, they possess. We should call them possessors.

--[Ward Cunningham](https://twitter.com/WardCunningham/status/289875660246220800)

Learn more about how you can use this plugin to own your own data in conjunction with [the "Bring Your Own Content" self-hosted Web publishing virtual appliance](http://maymay.net/blog/2014/03/13/bring-your-own-content-virtual-self-hosting-web-publishing/).

== Installation ==

1. Download the plugin file.
1. Unzip the file into your 'wp-content/plugins/' directory.
1. Go to your WordPress administration panel and activate the plugin.
1. Go to Diasposter Settings (from the Settings menu) and either create or enter your Diaspora account settings. Then click "Save Changes."
1. Start posting!!!

See also the [Screenshots](https://wordpress.org/plugins/diasposter/screenshots/) section for a visual walk through of this process.

= Installation notes and troubleshooting =

Diasposter makes use of the [cURL PHP extension](https://php.net/manual/book.curl.php) and expects PHP 5.3 or greater.

It's also possible that your system administrator will apply updates to one or more of the core system packages this plugin uses without your knowledge. If this happens, and the updated packages contain backward-incompatible changes, the plugin may begin to issue errors. Should this occur, please [file a bug report on the Diasposter project's issue tracker](https://github.com/meitar/diasposter/issues/new).

== Frequently Asked Questions ==

= Can I specify a post's tags? =

Yes. WordPress's tags are also crossposted to Diaspora. If you'd like to keep your WordPress tags separate from your Diaspora tags, be certain you've enabled the "Do not send post tags to Diaspora" setting.

Additionally, the "Automatically add these tags to all crossposts" setting lets you enter a comma-separated list of tags that will always be applied to your Diaspora crossposts.

= Does Diasposter properly attribute content sources? =

Yes. By default, Diasposter will set itself up so that your WordPress blog's posts are attributed as the source for each of your crossposts with a link back to the original post on your site.

= Can I send older WordPress posts to Diaspora? =

Yes. Go edit the desired post, verify the crosspost option is set to `Yes`, and update the post.

= What if I edit a post that has been cross-posted? =

If you delete a post that you have previously crossposted, Diasposter will delete it from Diaspora accordingly. Unfortunately, Diaspora provides no mechanism for editing a post after it has been published, so you will need to delete and recreate your post if you want to make changes on Diaspora.

= Can I cross-post Private posts from WordPress to Diaspora? =

Not yet, but this is a planned feature. Feel free to offer suggestions or patches at [the Diasposter project issue tracker](https://github.com/meitar/diasposter/issues/new).

= Can I choose which Diaspora aspects to share with? =

Yes. For each post you make, you can select either "Public" or "All Aspects" or any combination of your other aspects. The sharing rules obey the same rules as the Diaspora* bookmarklet. This means:

* If "All Aspects" is selected, all other selected aspects are ignored.
* If "Public" is selected, but "All Aspects" is not selected, then your post will be shared *publicly.*
* If neither of the previous two options are selected, you may mix-and-match any number of your personal aspects.

= Can I cross-post custom post types? =

Yes. By default, Diasposter only crossposts `post` post types, but you can enable or disable other post types from the plugin's settings screen.

If you're a plugin developer, you can easily make your custom post types work well with Diasposter by implementing the `diasposter_save_post_types`, `diasposter_meta_box_post_types`, and `diasposter_prepared_post` filter hooks. See [Other Notes](https://wordpress.org/plugins/diasposter/other_notes/) for coding details.

= Why don't I see the option to send a tweet automatically even after I set the auto-tweet/auto-post option? =

Make sure you have correctly configured your desired service integration for your Diaspora* account on your Diaspora* pod. Usually, this is available by selecting the "Services" tab from your pod's account setting page (such as at `https://your-diaspora-pod.com/services`). Only the services that you have enabled will be available for you to use in the Diasposter post editing meta box.

= Why aren't my Diaspora* posts showing my location even with "Send post location?" checked? =

You need a plugin that collects post location data before you have any data to share. If you have not installed such a plugin, then there is simply no location data to send to Diaspora*. Neither Diasposter nor WordPress itself collects this information, but numerous other plugins can.

If you have installed a geolocation plugin for WordPress but the location data is still not showing up, it is likely because the other plugin does not save location data in a standard format that other plugins (like Diasposter) can access. Diasposter adheres to the [WordPress Geodata standard](https://codex.wordpress.org/Geodata) for location information, and expects other plugins to behave accordingly. Try using a more well-behaved plugin instead.

= Is Diasposter available in languages other than English? =

Not yet, but I would love to accept translations for additional languages.

With your help it can be translated into many more languages! To contribute a translation of this plugin into your language, please [sign up as a translator on Diasposter's Transifex project page](https://www.transifex.com/projects/p/diasposter/).

= What if my theme doesn't support Post Formats? =

Diasposter will still work even if your theme doesn't support the [Post Formats](http://codex.wordpress.org/Post_Formats) feature. However, consider asking your theme developer to update your theme code so that it supports Post Formats itself for other plugins to use, too.

If you feel comfortable doing this yourself, then in most cases, this is literally a one-line change. Simply use the [add_theme_support()](http://codex.wordpress.org/Function_Reference/add_theme_support) function in your theme's `functions.php` file:

    add_theme_support('post-formats', array('link', 'image', 'quote', 'video', 'audio', 'chat''));

And if you choose to do this yourself, consider getting in touch with your theme's developer to let them know how easy it was! We devs love to hear this kind of stuff. :)

== Screenshots ==

1. When you first install Diasposter, you'll need to connect it to your Diaspora account before you can start crossposting. This screenshot shows how its options screen first appears after you activate the plugin.

2. Once you create and enter your Diaspora account information and click "Save Changes," you'll find you're able to access the remainder of the options page. Set your cross-posting preferences and click "Save Changes." You're now ready to start crossposting!

3. You can optionally choose not to crosspost individual WordPress posts from the Diasposter custom post editing box. This box also enables you to send the post's excerpt rather than its main body to Diaspora, choose which aspects you'd like to share with, and toggle geolocation on or off. (Note that geolocation requires some [geodata](https://codex.wordpress.org/Geodata) to be associated with your post.)

4. Get help where you need it from WordPress's built-in "Help" system.

== Changelog ==

= Version 0.1.1 =

* Feature: Post location sharing can send WordPress [geodata](https://codex.wordpress.org/Geodata) metadata to Diaspora*. Toggle this on or off for each post by sing the new "Send post location?" option.
* Feature: Service integrations for Twitter, Tumblr, WordPress, and Facebook let you control the auto-post for services you have connected to from your Diaspora* pod.

= Verson 0.1 =

* Initial release.

== Other notes ==

Maintaining this plugin is a labor of love. However, if you like it, please consider [making a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=meitarm%40gmail%2ecom&lc=US&item_name=Diasposter%20WordPress%20Plugin&item_number=diasposter&currency_code=USD&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted) for your use of the plugin, [purchasing one of Meitar's web development books](http://www.amazon.com/gp/redirect.html?ie=UTF8&location=http%3A%2F%2Fwww.amazon.com%2Fs%3Fie%3DUTF8%26redirect%3Dtrue%26sort%3Drelevancerank%26search-type%3Dss%26index%3Dbooks%26ref%3Dntt%255Fathr%255Fdp%255Fsr%255F2%26field-author%3DMeitar%2520Moscovitz&tag=maymaydotnet-20&linkCode=ur2&camp=1789&creative=390957) or, better yet, contributing directly to [Meitar's Cyberbusking fund](http://Cyberbusking.org/). (Publishing royalties ain't exactly the lucrative income it used to be, y'know?) Your support is appreciated!

= Developer reference =

Diasposter provides the following hooks for plugin and theme authors:

*Filters*

* `diasposter_save_post_types` - Filter an array of custom post type names to process when Diasposter is invoked in the `save_post` WordPress action.
* `diasposter_meta_box_post_types` - Filter an array of custom post type names for which to show the Diasposter post editing meta box.
* `diasposter_prepared_post` - Filter the `$diaspora_body` string immediately before it gets crossposted to Diaspora.
* `diasposter_services_array` - Filter the array of configured service integrations. Adding values like `facebook` to this array will cause Diasposter to include `facebook` in its JSON request to the Diaspora pod in the `services` field.
