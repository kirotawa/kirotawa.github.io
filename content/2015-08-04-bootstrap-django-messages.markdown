---
layout: post
title: "Boostrap x Django messages"
date:  2015-08-04 19:00:20
categories: django boostrap web
---
Recently I need to handle with messages using Django and Boostrap. Issue is that in Django a message.ERROR has not the same tag than Boostrap, instead second has -danger while
Django -error. What happens is that you won't be able to see your beautiful message in a proper way.

In order to fix this is very simple. Into your settings.py file

{% highlight python %}
# adding this line
from django.contrib.messages import constants as message_constants

# and redefine tags constants to match with boostrap messages
MESSAGE_TAGS = {
    message_constants.DEBUG: 'debug',
    message_constants.INFO: 'info',
    message_constants.SUCCESS: 'success',
    message_constants.WARNING: 'warning',
    message_constants.ERROR: 'danger',
 }

{% endhighlight %}

After this, it's done. :)
