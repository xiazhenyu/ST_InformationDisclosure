
Annoucements
***********************

我们关注公开社会影响力，社区影响力
5.1 产品发布
 * 产品公告
 * 重大合同公告
5.2 社会新闻
  * 社会新闻数量
  * 社会新闻正面，负面反响
5.3 代码提交活跃度
  * github代码贡献者人数
  * fork人数
  * 提交次数

.. code:: json
	
	{
		"version": "https://jsonfeed.org/version/1",
		"title": "The Shape of Everything",
		"home_page_url": "http://shapeof.com/",
		"feed_url": "http://shapeof.com/feed.json",
		"description": "A website mostly about Mac stuff, written by Gus Mueller",
		"author": {
			"name": "Gus Mueller"
		},
		"items": [
			{
				"id": "http://shapeof.com/archives/2018/11/subethaedit_goes_open_source.html",
				"title": "SubEthaEdit Goes Open Source",
				"content_html": "<p>Dominik Wagner: <a href=\"https://rant.monkeydom.de/posts/2018/11/28/see-is-back\">SubEthaEdit 5 – Now free and open source!</a></p>\n<p>It&#39;s story time.</p>\n<p>Way back in 2003, when <a href=\"https://subethaedit.net\">SubEthaEdit</a> was still called Hydra, it <a href=\"https://www.macworld.com/article/1025343/innovators.html\">won a round of the Mac OS X Innovators Contest</a> from O&#39;Reilly. My app at the time, <a href=\"https://www.voodoopad.com\">VoodooPad</a> (now owned by Primate Labs), also won a place in the contest. <a href=\"https://www.rogueamoeba.com/audiohijack/\">Audio Hijack Pro</a> also made an appearance as a runner up to VoodooPad.</p>\n<p>Because of international and political reasons, VoodooPad got first place with an award of a premier level membership to Apple&#39;s developer program. This was a pretty big deal! The regular membership cost $500 a year, but it came with a 20% discount on hardware which usually made up for the cost.</p>\n<p>The <a href=\"http://web.archive.org/web/20030419100048/http://developer.apple.com:80/membership/premier.html\">premier membership</a> was $3500, but it came with a pass to WWDC along with 10 hardware discounts. Ten! And a pass to WWDC!</p>\n<p>My company was just me, so I only needed one hardware discount. But back in the day, indies helped indies and the hardware discounts were transferable, and I did what was the completely obvious thing to do.</p>\n<p>So I sent a couple of the hardware discounts to the folks at Rogue Amoeba (makers of Audio Hijack) and the folks at the Coding Monkeys (who made SubEthaEdit). We were all pretty happy.</p>\n<p>Then a few days later I got a call for ADC. &quot;What the heck are you doing?&quot; they asked. I said that I didn&#39;t need that many and gave a couple of discounts to them. &quot;Are they doing work for you or something? Because the Coding Monkeys have a student ADC account, and it&#39;s not possible for them to have a hardware discounts and we&#39;re going to transfer those back to you.&quot;</p>\n<p>Well crap. OK.</p>\n<p>&quot;And what about Rogue Amoeba?&quot;. Well, uh- yes. They are doing work for me. Yep. They sure are. Sub-contracting, it&#39;s completely official. Long pause. &quot;OK.&quot;</p>\n<p>To be fair, <a href=\"https://onefoottsunami.com\">Paul Kafasis</a> from Rogue Amoeba was helping me out a lot. Even though he&#39;s about 10 years my junior, he had been doing indie software development for a bit longer at the time and as far as I was concerned, was also quite a bit wiser about the whole business end of it. I got lots of good advice, and his company got some hardware discounts.</p>\n<p>Anyway, that&#39;s my SubEthaEdit story. They eventually won an ADA as well, which I&#39;d rather have than 100 hardware discounts.</p>\n",
				"date_published": "2018-11-28T10:23:02-08:00",
				"url": "http://shapeof.com/archives/2018/11/subethaedit_goes_open_source.html"
			},
			{
				"id": "http://shapeof.com/archives/2019/1/blown_out_curves.html",
				"title": "Blown Out Curves",
				"content_html": "<p>I was working on a bug in Acorn yesterday with the Curves filter, and I noticed that when pushing the green channel to extremes that it became pretty blown out. While first looking at the filtered image I thought the results might be right… but maybe it wasn&#39;t? So I threw a mental note in the back of my head to compare what Curves in Acorn is doing versus Photos and Photoshop.</p>\n<p>And then when was I knee deep in actually fixing the original bug, I realized there was a better way of creating the LUT (lookup table) from the curves data and that idea just kind of stuck in my head as well.</p>\n<p>So after fixing some last minute sandboxing issues for Acorn 6.3 today (it&#39;s <em>always</em> the sandbox!) and submitting it to Apple, I decided to look into these two curves things.</p>\n<p>Turns out that my idea for creating the LUT also fixed the blown out colors bug.</p>\n<center><a href=\"https://shapeof.com/archives/2019/media/blown_out_curves.jpeg\"><img src=\"https://shapeof.com/archives/2019/media/blown_out_curves.jpeg\" width=\"640\" alt=\"Blown out curves.\" border=\"0\"/></a><br/><span class=\"secondaryTextSmall\">(click to embiggen)</span></center>\n\n<p>The left window in this screenshot is the original image. The middle image is what is shipping in Acorn 6.3 and earlier. And finally we have the fixed version (aka, Acorn 6.3.1, which hasn&#39;t left my Mac yet). You can see the whites and the yellows not mixing very well when compared to the fixed version. And finally the filter window on the right is what the green channel was set to, so you can see how much I was pushing it.</p>\n<p>It&#39;s always delightful when things come together like this.</p>\n",
				"date_published": "2019-01-04T14:05:59-08:00",
				"url": "http://shapeof.com/archives/2019/1/blown_out_curves.html"
			}
		]
	}
	
..
 
 JSON Schema
 
.. code:: json

	{
		"version": "https://jsonfeed.org/version/1",
		"user_comment": "This is a podcast feed. You can add this feed to your podcast client using the following URL: http://therecord.co/feed.json",
		"title": "The Record",
		"home_page_url": "http://therecord.co/",
		"feed_url": "http://therecord.co/feed.json",
		"items": [
			{
				"id": "http://therecord.co/chris-parrish",
				"title": "Special #1 - Chris Parrish",
				"url": "http://therecord.co/chris-parrish",
				"content_text": "Chris has worked at Adobe and as a founder of Rogue Sheep, which won an Apple Design Award for Postage. Chris’s new company is Aged & Distilled with Guy English — which shipped Napkin, a Mac app for visual collaboration. Chris is also the co-host of The Record. He lives on Bainbridge Island, a quick ferry ride from Seattle.",
				"content_html": "Chris has worked at <a href=\"http://adobe.com/\">Adobe</a> and as a founder of Rogue Sheep, which won an Apple Design Award for Postage. Chris’s new company is Aged & Distilled with Guy English — which shipped <a href=\"http://aged-and-distilled.com/napkin/\">Napkin</a>, a Mac app for visual collaboration. Chris is also the co-host of The Record. He lives on <a href=\"http://www.ci.bainbridge-isl.wa.us/\">Bainbridge Island</a>, a quick ferry ride from Seattle.",
				"summary": "Brent interviews Chris Parrish, co-host of The Record and one-half of Aged & Distilled.",
				"date_published": "2014-05-09T14:04:00-07:00",
				"attachments": [
					{
						"url": "http://therecord.co/downloads/The-Record-sp1e1-ChrisParrish.m4a",
						"mime_type": "audio/x-m4a",
						"size_in_bytes": 89970236,
						"duration_in_seconds": 6629
					}
				]
			}
		]
	}
	
..