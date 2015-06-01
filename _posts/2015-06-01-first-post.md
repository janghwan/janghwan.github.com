---
layout: post
title:  "First Post!"
date:   2015-06-01 10:12:27
categories: misc
---
첫번째 포스트입니다.

{% highlight scala %}
object Test extends Controller with Authentication {
  def test = Authenticated(Role.User) ({
    implicit authReq =>
      val conf = new Configuration()
      val ret = conf.get("yarn.resourcemanager.ha.rm-ids")
//      val ret = MerchantAdvertiser.get("Sephora.com, Inc.", models.Product.ADVERTISER_ID_LINKSHARE)
      Ok(ret.toString)
  })
}


{% endhighlight %}

![Chloe]({{site.url}}/assets/chloe-moretz.jpg)
