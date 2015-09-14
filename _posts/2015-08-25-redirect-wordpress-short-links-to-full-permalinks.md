---
layout: post
date:   2015-08-25 09:58:00
title:  "Redirect Wordpress Short Links to Full Permalinks"
---

I'm not sure if "short links" are the official term for them, but the default post permalinks in Wordpress are your site url and a `p` parameter containing the post id.

```
chrisodonnell.io/?p=123456
```

Also, regardless of your chosen permalink structure, post preview links will use this format.

```
chrisodonnell.io/?p=123456&preview=true
```

Short links don't automatically redirect to the post permalink, like some people (me) may have thought they did. If you switch your permalink structure to something more SEO friendly, existing posts should automatically redirect to the proper format. However, future posts will not. If you want all short links to redirect to their respective permalink, place this snippet in your `functions.php`.

**NOTE:** Exclusions like post preview links should be taken into account.

<script src="https://gist.github.com/codfish/7b8c8f4c4f085429f07c.js"></script>

I ran into a situation with a client where short links were being used by a bitly plugin to shorten post urls for social services. This in turn was causing issues with services like LinkedIn that try and scrape the page for information, and links with query parameters seemed to give them trouble.

Another issue was that users were being sent to these ugly permalinks when coming from social networks.

If there are reasons that these "short links" shouldn't redirect to their respective permalinks (outside of previewing links), I'd love to know.
