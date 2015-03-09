---
layout: post
title:  "Write list to file with pickly"
date:   2015-03-09
categories: python
tags: [pickle]

---

{% highlight python %}

import pickle

my_list = ["www.test1.dk", "www.test2.dk", "www.test3.dk"]

file_name = "dba.txt"

with open(file_name, 'wb') as f:
    pickle.dump(my_list, f)

with open(file_name, 'rb') as f:
    my_list = pickle.load(f)
    print my_list

{% endhighlight %}