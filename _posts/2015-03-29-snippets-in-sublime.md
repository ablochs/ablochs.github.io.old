---
layout: post
title:  "Snippets in Sublime"
date:   2015-03-29
categories: sublime
tags: [sublime, workflow]

---

Create a new snippet: ```Tools > New Snippet...```

Save a file-name.sublime-snippet

```
<snippet>
    <content><![CDATA[
{% highlight ${1:python} %}
    ${2:code}
{% endhighlight %}
]]></content>
    <!-- Optional: Set a tabTrigger to define how to trigger the snippet -->
    <tabTrigger>jekyll_highlight</tabTrigger>
    <!-- Optional: Set a scope to limit where the snippet will trigger -->
    <scope>text.plain</scope>
</snippet>
```

Then you should be able to run
```
jekyll_hightligh > Tab
```
