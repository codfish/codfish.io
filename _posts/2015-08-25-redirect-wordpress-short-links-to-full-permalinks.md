---
layout: post
date:   2015-08-25 09:58:00
title:  "Redirect Wordpress Short Links to Full Permalinks"
---
Wordpress short links (`mywordpresssite.com/?p=123456`) don't automatically redirect to the post permalink, like some people (me) may have thought (and think they should). If you switch your permalink structure to something more SEO friendly, existing posts should automatically redirect to the proper format. However, future posts will not. If you want all short links to redirect to their respective permalink, place this snippet in your `functions.php`.

**NOTE:** Exclusions like post preview links should be taken into account.

<script src="https://gist.github.com/codfish/7b8c8f4c4f085429f07c.js"></script>