=== Diasposter ===
Contributors: maymay
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&amp;business=TJLPJYXHSRBEE&amp;lc=US&amp;item_name=Diasposter%20WordPress%20Plugin&amp;item_number=diasposter&amp;currency_code=USD&amp;bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted
Tags: Diaspora, post, crosspost, publishing, post formats
Requires at least: 3.5
Tested up to: 4.2.2
Stable tag: 0.1.9
License: GPLv3
License URI: https://www.gnu.org/licenses/gpl-3.0.html

Diasposter cross-posts your WordPress entries to Diaspora. Changes to your WordPress posts are reflected in your Diaspora posts.

== Description ==

Diasposter posts to Diaspora whenever you hit the "Publish" button. It can import Disapora comments to your original WordPress posts. It even uploads your WordPress post images as native Diaspora photos.

**Transform your WordPress website into a back-end for Diaspora. Create original posts using WordPress, but publish them to Diaspora. Synchronize with your Diaspora comments. Always have a portable copy (a running backup) of all your original content, plus its Diaspora discussion thread.**

Diasposter implements a simple API to keep posts in sync as much as possible; when you delete your WordPress post, your Diaspora post is removed, too. Comments on your Diaspora posts appear on your WordPress posts. Deleting a comment from your WordPress post deletes it from your Diaspora post, too. Featured images (aka "post thumbnails") and other photos in your WordPress media library can be uploaded directly into Diaspora posts to be hosted on your pod.

Diasposter is very lightweight. It just requires you to connect to your Diaspora account from the plugin options screen. After that, you're ready to cross-post!

* **Secure:** Unlike many other Diaspora tools, Diasposter *never writes your login cookie to disk*, strictly enforces encrypted connections between your blog and your Diaspora pod, and encrypts your password inside WordPress, so your Diaspora access credentials are kept as safe as you keep your WordPress database. This is especially important on Shared Hosting plans where many other customers have access to your server's filesystem!
* **Easy to use:** Seamlessly translates WordPress formatting to beautiful Diaspora posts, with full support for post formats, [featured images](https://codex.wordpress.org/Post_Thumbnails), post titles, automatic and manual [excerpts](https://codex.wordpress.org/Excerpt), tags, custom post types, and more.
* **Feature-rich:** Numerous additional options let you provide custom linkbacks, broadcast your Diaspora post on any social media services integrated with your pod (like Twitter, Tumblr, Facebook, and WordPress), set global preferences and per-post settings, and more.

Diasposter makes use of [Post Formats](http://codex.wordpress.org/Post_Formats) to automatically choose the most appropriate formatting for your Diaspora post. This means:

* WordPress's `Link` post format becomes a Diaspora post whose title is a link to the first link in your post.
* WordPress's `Image` and `Gallery` post formats become Diaspora posts wherein each `<img>` in your post is uploaded directly into your Diaspora post, making a beautiful slideshow on Diaspora.
* WordPress's `Standard`, `Aside`, and `Status` post formats are crossposted exactly as you enter them. (They are left untouched.)

Other options enable tweaking additional metadata from your WordPres entry (notably tags and geo-location data), and more. Diasposter is also [IndieWeb](https://indiewebcamp.com/)-friendly, with built-in support for the [`rel-syndication`](https://indiewebcamp.com/rel-syndication) pattern.

*Donations for my WordPress plugins make up a chunk of my income. If you continue to enjoy this plugin, please consider [making a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&amp;business=TJLPJYXHSRBEE&amp;lc=US&amp;item_name=Diasposter%20WordPress%20Plugin&amp;item_number=diasposter&amp;currency_code=USD&amp;bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted). :) Thank you for your support!*

> Servers no longer serve, they possess. We should call them possessors.

--[Ward Cunningham](https://twitter.com/WardCunningham/status/289875660246220800)

Learn more about how you can use this plugin to own your own data in conjunction with [the "Bring Your Own Content" self-hosted Web publishing virtual appliance](http://maymay.net/blog/2014/03/13/bring-your-own-content-virtual-self-hosting-web-publishing/).

== Installation ==

1. Download the plugin file.
1. Unzip the file into your `wp-content/plugins/` directory.
1. Go to your WordPress administration panel and activate the plugin.
1. Go to Diasposter Settings (from the Settings menu) and either create or enter your Diaspora account settings. Then click "Save Changes."
1. Start posting!!!

See also the [Screenshots](https://wordpress.org/plugins/diasposter/screenshots/) section for a visual walk through of this process.

= Installation notes and troubleshooting =

Diasposter makes use of the [cURL PHP extension](https://php.net/manual/book.curl.php) and expects PHP 5.3 or greater.

It's also possible that your system administrator will apply updates to one or more of the core system packages this plugin uses without your knowledge. If this happens, and the updated packages contain backward-incompatible changes, the plugin may begin to issue errors. Should this occur, please [file a bug report on the Diasposter project's issue tracker](https://github.com/fabacab/diasposter/issues/new).

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

Not yet, but this is a planned feature. Feel free to offer suggestions or patches at [the Diasposter project issue tracker](https://github.com/fabacab/diasposter/issues/new).

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

Yes! This plugin has been translated into the following languages:

* Dutch (`nl_NL`)
    * Thanks, [André](https://www.transifex.com/accounts/profile/mijnheer/)! :D

With your help it can be translated into even more! To contribute a translation of this plugin into your language, please [sign up as a translator on Diasposter's Transifex project page](https://www.transifex.com/projects/p/diasposter/).

= What if my theme doesn't support Post Formats? =

Don't worry, Diasposter will still work even if your theme doesn't support the [Post Formats](http://codex.wordpress.org/Post_Formats) feature. :)

== Screenshots ==

1. When you first install Diasposter, you'll need to connect it to your Diaspora account before you can start crossposting. This screenshot shows how its options screen first appears after you activate the plugin.

2. Once you create and enter your Diaspora account information and click "Save Changes," you'll find you're able to access the remainder of the options page. Set your cross-posting preferences and click "Save Changes." You're now ready to start crossposting!

3. You can optionally choose not to crosspost individual WordPress posts from the Diasposter custom post editing box. This box also enables you to send the post's excerpt rather than its main body to Diaspora, choose which aspects you'd like to share with, and toggle geolocation on or off. (Note that geolocation requires some [geodata](https://codex.wordpress.org/Geodata) to be associated with your post.)

4. Get help where you need it from WordPress's built-in "Help" system.

== Changelog ==

= Version 0.1.9 =

* Bugfix: Fix failed log in attempts on some Diaspora pods.
* Usability:
    * The currently connected Diaspora user account name is now shown on the settings screen.
    * Error messages for certain issues that caused silent failures are now reported to user.
    * Admin notices are now user-dismissible.
* Compatible with WordPress 4.2.2.

= Version 0.1.8 =

* Feature: Support [`rel-syndication` IndieWeb pattern](https://indiewebcamp.com/rel-syndication) as implemented by the recommended [Syndication Links](https://indiewebcamp.com/rel-syndication#How_to_link_from_WordPress) plugin.
    * `rel-syndication` is an IndieWeb best practice recommendation that provides a way to automatically link to crossposted copies (called "POSSE'd copies" in the jargon) of your posts to improve the discoverability and usability of your posts. For Diasposter's `rel-syndication` to work, you must also install a compatible WordPress syndication links plugin, such as the [Syndication Links](https://wordpress.org/plugins/syndication-links/) plugin, but the absence of such a plugin will not cause any problems, either.

= Version 0.1.7 =

* Feature: "Link" [post formats](https://codex.wordpress.org/Post_Formats) are now supported. When you cross-post a link post, the first hyperlink (`<a href="...">` element) in your post will be used as the cross-posted post's link and title.
* Usability: New Dutch (`nl_NL`) translation available. (Thanks, [André Koot](https://www.transifex.com/accounts/profile/mijnheer/)!)
    * Want Diasposter in your language? Join a [Diasposter translation](https://www.transifex.com/projects/p/diasposter/) team!

= Version 0.1.6 =

* Feature: "Image" and "Gallery" [post formats](https://codex.wordpress.org/Post_Formats) now automatically detect `<img>` tags in WordPress post content and directly upload the images themselves to your Diaspora* post. This makes it easy to create beautiful photoset posts on Diaspora simply by inserting images into your WordPress post.

= Version 0.1.5 =

* Bugfix: Improved comment synchronization.
    * Sync'ed comments are now stored as HTML as WordPress expects, not Markdown.
    * Fixed a bug that caused only one comment to be sync'ed per sync subroutine invocation.

= Version 0.1.4 =

* Feature: Comment synchronization automatically detects new comments on your crossposted entries and copies them back to your WordPress post.
    * If you delete a comment on your WordPress post that was originally posted on your Diaspora* cross-post, the comment is also deleted from your Diaspora* post.
    * **This feature is experimental.** It uses a "lazy Salmon-like detection" scheme and is not yet fully tested. Please backup your WordPress database before you enable this feature.

= Version 0.1.3 =

* Feature: WordPress [Featured Images (aka "post thumbnails")](https://codex.wordpress.org/Post_Thumbnails) now become Diaspora* photos. Simply set a Featured Image in your WordPress post to upload it as an image and associate it with your Diaspora* post.
* Usability: Per-post settings now remember their value in between editing different post drafts.

= Version 0.1.2 =

* Feature: Diaspora* pod settings are now cached for ten minutes by default. Optionally, you can configure how long to keep the cache for in the plugin options.
* [Bugfix](https://joindiaspora.com/posts/5622273#b1f350f09a8f0132abc7543d7ed6cc36): Diasposter no longer shows warnings when no service integrations are configured for your account on your Diaspora* pod.

= Version 0.1.1 =

* Feature: Post location sharing can send WordPress [geodata](https://codex.wordpress.org/Geodata) metadata to Diaspora*. Toggle this on or off for each post by using the new "Send post location?" option.
* Feature: Service integrations for Twitter, Tumblr, WordPress, and Facebook let you control the auto-post for services you have connected to from your Diaspora* pod.

= Verson 0.1 =

* Initial release.

== Other notes ==

Maintaining this plugin is a labor of love. However, if you like it, please consider [making a donation](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&amp;business=TJLPJYXHSRBEE&amp;lc=US&amp;item_name=Diasposter%20WordPress%20Plugin&amp;item_number=diasposter&amp;currency_code=USD&amp;bn=PP%2dDonationsBF%3abtn_donate_SM%2egif%3aNonHosted) for your use of the plugin or, better yet, contributing directly to [my's Cyberbusking fund](http://Cyberbusking.org/). (Publishing royalties ain't exactly the lucrative income it used to be, y'know?) Your support is appreciated!

= Developer reference =

Diasposter provides the following hooks for plugin and theme authors:

*Filters*

* `diasposter_save_post_types` - Filter an array of custom post type names to process when Diasposter is invoked in the `save_post` WordPress action.
* `diasposter_meta_box_post_types` - Filter an array of custom post type names for which to show the Diasposter post editing meta box.
* `diasposter_prepared_post` - Filter the `$diaspora_body` string immediately before it gets crossposted to Diaspora.
* `diasposter_services_array` - Filter the array of configured service integrations. Adding values like `facebook` to this array will cause Diasposter to include `facebook` in its JSON request to the Diaspora pod in the `services` field.
