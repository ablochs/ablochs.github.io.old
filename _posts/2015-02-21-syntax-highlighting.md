---
layout: post
title:  "Syntax highlighting in jykell"
date:   2015-02-21
categories: jekyll
tags: "syntax highlighting" code
---

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}