---
layout: post
date:   2015-08-25 09:58:00
title:  "Redirect Wordpress Short Links to Full Permalinks"
---

The default permalink structure in Wordpress are your site url and a `p` parameter containing the post id. I'm not sure if "short links" are the official term for them, but that's what I'm going to refer to them as :). Here's what they look like:

<pre class="language-text">
codfish.io/?p=123456
</pre>

Also, regardless of your chosen permalink structure, preview links will use this format.

<pre class="language-text">
codfish.io/?p=123456&preview=true
</pre>

Short links don't automatically redirect to the post permalink, like some people (me) may have thought they did. If you switch your permalink structure to something more SEO friendly, existing posts should automatically redirect to the proper format. However, future posts will not. If you want all short links to redirect to their respective permalink, place this snippet in your `functions.php`.

**NOTE:** Exclusions like post preview links should be taken into account.

<script src="https://gist.github.com/codfish/7b8c8f4c4f085429f07c.js"></script>

I ran into a situation with a site where short links were being used by a bitly plugin to shorten post urls for social services. This in turn was causing issues with services like LinkedIn that try and scrape the page for information, and links with query parameters seemed to give them trouble.

Another issue was that users were being sent to these ugly permalinks when coming from social networks.

If there are reasons that these "short links" shouldn't redirect to their respective permalinks (outside of previewing posts), I'd love to know.
