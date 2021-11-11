---
layout: posttail
authors: ["Dan Mayer"]
title: "ActiveRecord Association objects can act weird (bug in association#any?)"
category:
tags: []
---
{% include JB/setup %}
Rails, RubyI found a weird issue when working with [ActiveRecord AssociationProxy objects](http://apidock.com/rails/ActiveRecord/Associations/AssociationProxy), they weren't proxying the method correctly.    The issue arose when trying to use the #any? method on an array which should be true when empty. When calling this on a AssociationProxy object that has 0 items it was returning false. Oddly enough inspecting or to_s the association and then calling #any? resulted in the correct behavior. It was so weird though that after looking at other options I ended up using the present?, which always behaved how I expected it to. Even weirder is the issue only presented itself in the rails server debug and production modes. It always acted as one would expect in rails console. I started to dig in more, but ended up yak shaving a lot of other stuff to try to learn exactly what the cause was. If anyone understands the issue better, I would be happy to know more.    Until then, be aware that at least in the 2.3.X versions of rails, ActiveRecord AssociationProxy#any? acts funky and should not be trusted. Use a work around like present? or length > 0 (both worked correctly in console and on dev/production server environments). This is one of these issues where there is so much going on in the rails stack that it is hard to determine where the issue lies.    So for those googling this issue, beware AssociationProxy.any? on has_many relationships.    Example code:

    <script src="https://gist.github.com/1250980.js?file=AR_bug.rb"> </script>