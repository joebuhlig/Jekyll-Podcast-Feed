# Jekyll Podcast Feed

You can use this feed to host a podcast at iTunes. This setup requires a number of settings in both the main site YAML and each posts YAML. I recommend setting up your server to rewrite index.xml files as a directory index. This makes it possible to use this: http://example.com/feed/podcast

To see an example of this feed in action, here are a few links:

My Jekyll generated site: [http://joebuhlig.com](http://joebuhlig.com)

Podcast episode page: [http://joebuhlig.com/whaddyaknowjoe/](http://joebuhlig.com/whaddyaknowjoe/)

Podcast feed: [http://joebuhlig.com/feed/podcast](http://joebuhlig.com/feed/podcast)

You can validate and submit your podcast feed for iTunes submission here:

https://podcastsconnect.apple.com/

# Example Site Configuration

This setup requires a number of settings in your _config.yml file. To see how each of these are used, you can look through the index.xml file of this repo. 

    podcast_url: http://www.joebuhlig.com/whaddyaknowjoe
    podcast_album_art: /assets/base/Whaddya-Know-Joe-Album-Art.png
    podcast_title: Whaddya Know Joe?
    podcast_owner: Joe Buhlig
    podcast_email: email@example.com
    podcast_category: Technology
    podcast_subcategory_one: Software How-To
    podcast_subcategory_two: Gadgets
    podcast_explicit: "no"
    podcast_author: Joe Buhlig
    podcast_description: Productivity stories from the trenches. What works and what I'll never do again. Hosted by Joe Buhlig.
    podcast_summary: Joe Buhlig walks you through real life story and then breaks down the productivity tools and techniques used. It's a great way to learn how to implement the tips and tricks that you see across the web. Productivity stories from the trenches. What works and what to never try.
    podcast_subtitle: Productivity stories from the trenches. What works and what I'll never do again. Hosted by Joe Buhlig.

Note: `podcast_album_art` is required to be a square image between 1400x1400px and 3000x3000px.

# Example Post YAML

You can choose to include a specific GUID on a podcast episode by including the "podcast_guid" setting for the post. This is helpful when migrating from a different hosting service. This is what allowed me to move mine from WordPress to Jekyll. It's not required and I usually leave it off.

    title:  "Episode Title Goes Here"
    date:   2015-10-20
    categories: podcast
    tags:
    - tagone
    - tagtwo
    - tagthree
    permalink: /35/
    image: /assets/posts/Awesome-Podcast-Art.jpg
    podcast_link: http://traffic.libsyn.com/podcast/filename.mp3
    podcast_file_size: 13.7 MB
    podcast_duration: "14:02"
    podcast_length: 13654375
    podcast_guid: ?p=866
    
`podcast_length` is the size of your `podcast_link` file in bytes.
