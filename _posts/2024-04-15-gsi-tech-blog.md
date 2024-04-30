---
# List of one or more author names that map to the value of short_name in site.community_members. See the content in the _community_members collection for reference.
authors: 
    - nateboot

# Content categorization. One or more categories can be specified. 
category:
  - community

# Publish date in the format of four digit year, two digit month, two digit day, hour, minute, second, and timezone offset; e.g., 2021-04-12 01:01:01 -0700
date: 2024-04-15 01:01:01 -0700

# An excerpt of the blog post. It is used in the blog post list view, and in the home page what's new list of N most recent blog posts. It is also used as a fallback value for the twittercard:description field if not explictly defined in the front matter.
excerpt: 
  
# Used as a fallback for the Twitter Card image, otherwise not currently used. Is only present in content up to June 3, 2021.
#feature_image: /assets/path/to/image/asset.ext

# Setting to true will result in the inclusion of the MathJax JavaScript library for rendering math equations. For reference see: _includes/include-mathjax.html.
#has_math: true

# Setting to true will result in the inclusion of CSS styles specific to using borders for the table, for table header cells, and table data cells. scientific data tables. For reference see: _includes/science-table-styles.html.
#has_science_table: true

# The layout template to use for rendering the content.
# Options are default, fullwidth, homepage, and post.
layout: post
# Value used for the meta description tag. Also used as a final fallback value for the Twitter Card description field after the excerpt property.
meta_description: "GSI Technology uses OpenSearch as a vector store to solve advanced real world problems in the realms of AI, Aerospace, Defense and even DNA mapping." 

# Value used for the meta keywords tag.
meta_keywords: "ML model, vector store, GSI Technology, OpenSearch AI and ML"

# Set to true to indicate content that was imported from the Open Distro For Elasticsearch blog.
#odfeimport: true

# URL for use by the jekyll-redirect-from plugin.
# When importing your posts and pages from, say, Tumblr, it's annoying and impractical to create new pages in the proper subdirectories so they, e.g. /post/123456789/my-slug-that-is-often-incompl, redirect to the new post URL.
# For reference see: https://github.com/jekyll/jekyll-redirect-from
#redirect_from: /blog/odfe-updates/2019/09/Check-out-earlier-blogposts-on-Open-Distro-for-Elasticsearch/

# The title of the post.
title: "What if satellites spoke in vector?"

# Meta data for the twitter card. The twitter card is used when a link to the blog post is shared on twitter. The twitter card is also used by other social media sites when a link to the blog post is shared on those sites. The twitter card is also used by search engines when a link to the blog post is shared on those sites.

---
Every once in a while I come across a use case that gets me really excited, not just because it aligns with my personal interests but also because I never would have thought that open-source tools would find their way into certain use cases. Recently I was lucky enough to learn about some very complicated real-world problems that could be improved by using OpenSearch, AI, and machine learning (ML). Those problems just happen to involve the realm of observability and, in particular, things that observe our planet.

## What is the problem to be solved?

Here on Earth we’re starting to see more and more cars that can drive themselves, illustrating the need for collision avoidance. It’s pretty easy to simplify the problem statement here. It’s just making sure that stuff doesn’t smash into each other. Compared to our roads, space really is big, but the space where satellites orbit around the earth isn’t quite as big. So we have a common problem of avoiding collisions, whether between satellites or cars. It is very easy for a small piece of debris, even as small as a fleck of paint, to cause significant damage to an orbiting vehicle. For objects that can’t move themselves, there are only passive approaches to be taken. Approaches like orbital altitudes and graveyard orbits are options, but these are passive solutions that help segregate orbits. Once one of these is used for a launched, there’s not much you can do to move it.

Communications satellites are great at talking to each other, but Earth observation satellites don’t always have this strength. They have large arrays of sensors and collect large quantities of data. However, they still need to send their data to the ground for processing. That is to say, these observational satellites don’t really compute their own sensor data. To further complicate this issue, sending sensor data to Earth has to happen during small windows of time due to satellites only being able to transmit to ground stations during small windows in their orbit. This means that not all of the data is sure to make it to the ground. Even after all of this happens, a human still has to review the results.

The number of satellites is ever increasing. We have 5 times more satellites in space than we did 10 years ago. In contrast, the number of humans with the skills to perform this type of processing is decreasing. Humans have become a bottleneck.

![](/assets/media/blog-images/2024-04-15-gsi-tech-blog/objects-launched-annual.jpg)

## What if...

Suppose that a satellite could be outfitted with a card that both stored and computed its own distributed memory (equivalent to having both RAM and CPU) with the capability to run sensor data through an ML model, the goal being to vectorize and pre-process sensor data. Sending a vector or change detection Earthside is a much quicker operation than sending a complete set of sensor data. One of our partners, [GSI Technology](https://gsitechnology.com), might just change the landscape in this regard. They’ve introduced a new kind of chip to the market. The project, called “Gemini-II”, is an APU. It is an extremely power-efficient processing unit that can both store and compute its own distributed memory. You may have seen their booth at [OpenSearchCon 2023](http://www.opensearch.org/events/opensearchcon/2023/north-america/index.html).

The APU technology family is a Compute-in-memory (CiM) architecture that eliminates computation time wasted on data movement by closing the traditional gap between processors (millions in GSI's case) and storage elements, which is highly beneficial for data-intensive workloads. Computation occurs where the data lives---in the storage elements---avoiding traditional processor/memory bottlenecks.

## Several applications

Many organizations use technology like synthetic aperture radar (SAR) to monitor landscapes to check for things like deforestation progress, forest fires, or erosion of coastal areas. Even corporations use this technology to count the number of cars in their stores’ parking lots to help forecast business decisions. We can even use it to predict and detect ships adrift at sea for the purposes of rescue. The same advantage is available here. Instead of sending entire collections of satellite data, we now have the potential to send results that represent those changes instead.

If you want to learn more about GSI Technology solutions, you should check out [their website](https://gsitechnology.com). They’re applying AI and ML to a variety of modern problems. There are many potential applications, including aerospace, genomics, computer vision, cybersecurity in space, vector search in space, data centers in space for the purposes of computing large volumes of data, and more.

## Parting thoughts

Satellites and space sure sound cool, but there may be many other places in which the observability of our own planet can be improved. This may be true not only on a cosmic scale but for any application in which you collect large amounts of data. Imagine a microscope with a bit of computational memory, equivalent to RAM and a CPU, that could supplement the years and years of experience that doctors and scientists have accumulated (not replace, but supplement). Imagine an MRI machine equipped with a model that recognizes brain scan anomalies. As a longtime sufferer of epilepsy, a condition for which only 3 out of 10 cases ever have a root cause determined, I sure wouldn’t mind donating the vector of my brain scans to science---with an open-source license, of course.
