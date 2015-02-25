---
layout: post
title:  "Duplicating a git repository"
date:   2015-02-25
categories: git
tags: [git]

---

{% highlight python %}
git clone --bare https://github.com/exampleuser/old-repository.git
# Make a bare clone of the repository

cd old-repository.git
git push --mirror https://github.com/exampleuser/new-repository.git
# Mirror-push to the new repository

cd ..
rm -rf old-repository.git
# Remove our temporary local repository
{% endhighlight %}

[Github help](https://help.github.com/articles/duplicating-a-repository/)