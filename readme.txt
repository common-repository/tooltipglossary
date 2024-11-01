=== Plugin Name ===
Contributors: jatls
Donate link: http://thestable.info
Tags: glossary, pages, posts, definitions, tooltip, automatic
Requires at least: 3.0
Tested up to: 3.0
Stable tag: 1.3

Parses posts for defined glossary terms and adds links to the static glossary page containing the definition and a tooltip with the definition.

== Description ==

Parses posts for defined glossary terms and adds links to the static glossary page containing the definition.  The plugin also creates a tooltip containing the definition which is displayed when users mouseover the term.  Based on [automatic-glossary](http://wordpress.org/extend/plugins/automatic-glossary/).

The code has been optimised from automatic-glossary and unnecessary code has been stripped to keep the plugin lean.  However, support for php 4 has been removed and if you are looking for a php 4 glossary, please do download automatic-glossary (although I believe there is a little extra tweaking required).

The tooltip is created with JavaScript based on the article written by [Michael Leigeber](http://www.leigeber.com/author/michael/) [here](http://sixrevisions.com/tutorials/javascript_tutorial/create_lightweight_javascript_tooltip/) and can be customized and styled through the tooltip.css and tooltip.js files.

Users of WordPress versions less than 3.0 should use version 1.1 of this plugin.

== Installation ==

1. Upload the plugin folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Define your glossary terms under the glossary menu item in the administration interface.  The title of the page should be the term.  The body content should be the definition.
4. Create a main glossary page (example "Glossary") with no body content if you wish to.  If you do not create this page then your terms will still be highlighted but there will not be a central listing of all your terms.
5. In the plugin's dashboard preferences, enter the main glossary page's id (optional as above)
6. There are a handful of other optional preferences available in the dashboard.

Note: You must have a call to wp_head() in your template in order for the tooltip js and css to work properly.  If your theme does not support this you will need to link to these files manually in your theme (not recommended).

== Frequently Asked Questions ==

= Does my main glossary page need to be titled "Glossary"? =

No.  It can be called anything.  In fact you don't even need to have a main glossary page.

= Do I need to manually type in an unordered list of my glossary terms on the glossary page? =

No.  Just leave that page blank.  The plugin creates the unordered list of terms automatically.

= How do I add glossary terms? =

Simply add a term under the 'Glossary' section in the adminstration interface.  Title it the glossary term (ex. "WordPress") and put the term's definition into the body (ex. "A neato Blogging Platform").

= What if I need to add or change a glossary term? =

Just add it or change it.  The links for your glossary terms are added to your page and post content on the fly so your glossary links will always be up to date.

== Screenshots ==

1. The options available for TooltipGlossary in the administration area.

== Changelog ==

= 1.3 =
* Bug fixes
* Parser is now less greedy - will now only match the exact term defined (give or take an 's' for plurals in English)
* Users can define the permalink name in the plugin options
* Option to return only the first match on a page/post added

= 1.2 =
* Added custom_post_type for the glossary for WP 3.0
* Main glossary page is now optional

= 1.1 =
* Cleaned up administration interface
* Added style options in admin area

= 1.0 =
* First release
* Optimised code from automatic-glossary
* Added tooltip functionality
