# Jekyll Personal Website

The theme is an blogger friendly Jekyll expansion port of GitHub official [personal website](https://github.com/github/personal-website) theme. It supports card-like archives as the latest posts. Each post can have previous, next, related posts, and comments. Card archives support pagination by category are available. Designed to easily apply metadata, analytics, verification, rss feed and sitemap. Contact forms are also supported.

I've attached a screenshot of the archive below, and you can see my personal website as a demo page [here](https://Lee-Yunseok.GitHub.io).

![sample screenshot](https://yggdrasilstudio.sirv.com/lee_yunseok/2019/11/jekyll-personal-website-posts-cards-screenshot.webp)

### Showcase your software development skills

This repository gives you the code you'll need to kickstart a personal website that showcases your work as a software developer. And when you manage the code in a GitHub repository, it will automatically render a webpage with the owner's profile information, including a photo, bio, and repositories.

Your personal website is waiting to be personalized, though. It includes space to highlight your specific areas of interest in software development, like languages or industries. And it's standing by to publish your next great blog post.

It's all possible using the combination of [Jekyll](https://jekyllrb.com/docs/) (for building your website), [GitHub Pages](https://pages.github.com/) (for hosting your website), and [GitHub's API](https://developer.github.com/v3/) (for automatically populating your website with content).

## Installation

### Fork the `lee-yunseok/jekyll-personal-website` repo

You'll be making your own copy of the "personal website starter" repository so you have your own project to customize. A "fork" is a copy of a repository. So select "Fork" atop [the `github/personal-website` repository](https://github.com/github/personal-website).

Once you've found a home for your forked repository, it's yours. You're the owner, so you're ready to publish, if you wish.

### Install in your local development environment

If you want to manage your website in a local web development environment, you'll be using [Ruby](https://jekyllrb.com/docs/installation/).

Once you've found a home for your forked repository, **[clone it](https://help.github.com/articles/cloning-a-repository/)**.

#### Install Jekyll

Jekyll is a [Ruby Gem](https://jekyllrb.com/docs/ruby-101/#gems) that can be installed on most systems.

1. Install a full [Ruby development environment](https://jekyllrb.com/docs/installation/)
2. Install Jekyll and [bundler](https://jekyllrb.com/docs/ruby-101/#bundler) [gems](https://jekyllrb.com/docs/ruby-101/#gems)
```
gem install jekyll bundler
```
3. Change into your new directory
```
cd jekyll-personal-website
```
4. Install missing gems
```
bundle install
```
5. Build the site and make it available on a local server
```
bundle exec jekyll serve
```

You should see something like:

```
Configuration file: /octocat/personal-website/_config.yml
            Source: /octocat/personal-website
       Destination: /octocat/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
   GitHub Metadata: No GitHub API authentication could be found. Some fields may be missing or have incorrect data.
                    done in 14.729 seconds.
 Auto-regeneration: enabled for '/octocat/personal-website'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

Don't worry about the "No GitHub API authentication could be found" message. [API authentication is only necessary](https://github.com/jekyll/github-metadata/blob/master/docs/authentication.md) if you intend to display more detailed metadata, like a branch name.

6. Now browse to [http://localhost:4000](http://localhost:4000)

### Publish

When you host your personal website's code on GitHub, you get the support of free hosting through GitHub Pages.

**The fastest approach** is to rename your repository `username.github.io`, where `username` is your GitHub username (or organization name). Then, the next time you push any changes to your repository's `master` branch, they'll be accessible on the web at your `username.github.io` address.

**If you want to use a custom domain**, you'll want to add it to your repository's "Custom domain" settings on github.com. And then register and/or [configure your domain with a DNS provider](https://help.github.com/articles/quick-start-setting-up-a-custom-domain/).

## Customization

It's your website, and you control the source code. So you can customize everything, if you like. But we've provided a handful of quick customizations for you to consider as you get your website off the ground.

### Quick configuration changes

Most customizations can be done in a matter of seconds, by revising your repository's `_config.yml` file. Just remember to restart your local server each time you save new changes so your Jekyll-powered website rebuilds correctly:

1. Shut down your server by entering the keyboard command <kbd>CTRL</kbd>+<kbd>c</kbd>
2. Restart your server: `bundle exec jekyll serve`

#### Layout

Your website will display in a two-column layout by default on larger-screen devices, with your photo, name, and basic information displayed in a left-aligned "sidebar." You can quickly switch to a "stacked" single-column layout by changing the line in your `_config.yml` file that reads `layout: sidebar` to `layout: stacked`.

#### Style

Your website appears with a "light" white and gray background by default, with dark text. You can quickly switch to a "dark" background with white text by changing the line in your `_config.yml` file that reads `style: light` to `style: dark`.

#### Timezone

Set your [timezone](https://github.com/tzinfo/tzinfo-data/blob/master/lib/tzinfo/data/indexes/countries.rb) like this below so your posts will be displayed in your timezone.

`timezone: America/Los_Angeles`

#### GitHub User Settings

This theme requires you to enter GitHub user data.

```
origin_url: Your website url.
repository: your_login_name/your_repository
avatar_url: Your GitHub avatar image url.
name: Your name.
login: Your GitHub login name.
email: Your email address. Leave it blank if you don't want to show your email.
bio: Your short bio.
org: Your GitHub organization. Leave it blank if you don't have your own organization.
location: Your location.
hireable: Set "true" or "false".
```

#### Default Metadata tags

This will fill `<head> </head>`.

```
title: Your website title.
description: Your website description.
keyword: Your website keyword.
```

#### Projects

The "My Projects" section of your website is generated by default with your nine most recently "pushed" repositories. It also excludes repositories that you forked, by default. But each of these parameters can be quickly customized in your repository's `_config.yml` file, under the `projects` dictionary line.

Parameters include:

- `sort_by`: The method by which repositories are sorted. Options include `pushed` and `stars`.
- `limit`: The maximum number of repositories that will be displayed in the "My Projects" section of your website. Out of the box, this number is set to `9`.
- `exclude`:
   - `forks`: When `true`, repositories you've forked will be excluded from the listing.
   - `projects`: A list the repository names you want to exclude from the listing.

#### Topics

Your website comes pre-configured with three topics (e.g. "Web design" and "Sass") that appear in a section titled "My Interests." These are also stored in your repository's `_config.yml` file, where you can define each topic's name and two other optional details:

- `web_url`: The web address you'd like to your topic to link to (e.g. `https://github.com/topics/sass`).
- `image_url`: The web address of an (ideally square) image that you'd like to appear with your topic.

#### Social media

Your website supports linking and sharing to social media services you're using, including Behance, Dribbble, Facebook, LinkedIn, Medium, Stack Overflow, Twitter, and YouTube. To identify the services you use:

1. Edit your repository's `_config.yml` file.
2. Edit the `social_media` dictionary line, and represent the services you like in a simple `key: value` form:

```
social_media:
  behance: your_username
  dribbble: your_username  
  facebook: your_username
  hackerrank: your_username
  instagram: your_username
  keybase: your_username
  linkedin: your_username
  medium: your_username
  stackoverflow: your_user_id
  telegram: your_username
  twitter: your_username
  unsplash: your_username
  vk: your_username
  website: http://your_website_url
  youtube: your_username
```

Links to your profile for each of the services you define will appear in the `<header>` of your website, appended to your bio. And if those services support sharing, any blog posts that you publish will include links to share that post using each social media service.

**Note**: This feature is supported by two files in your repository:

- `/_data/social_media.yml`: Defines each of the supported services, including variable name, display name, URL path, and SVG icon.
- `/_includes/social_media_share_url.html`: Outputs the share URL required for any of the supported social media services that support sharing URLs.

If you're interested in adding a social media service that's not already supported in this repo, you can edit these two files to build that support.

#### Facebook admin

This will use your [facebook page metadata](https://www.facebook.com/help/community/question/?id=759789947398518) when who share your post. Leave it blank if you don't want it.

`facebook_admins: Your Facebook admin number.`

#### Disqus comment

People can leave comments on your posts. Add your site and just type your [Disqus short name](https://help.disqus.com/en/articles/1717111-what-s-a-shortname). Leave it blank if you don't want it.

`disqus: Your Disqus short name.`

#### Website verification

Enter the verification codes to make them work.

```
google_verification: YOUR_VERIFICATION_CODE
bing_verification: YOUR_VERIFICATION_CODE
naver_verification: YOUR_VERIFICATION_CODE
norton_verification: YOUR_VERIFICATION_CODE
```

#### Google Analytics

Just add your [tracking code](https://support.google.com/analytics/answer/1008080).

`google_analytics: YOUR_TRACKING_CODE`

## About page

Edit `_/includes/about.html` file so you can include more information about you using HTML and [Liquid](https://jekyllrb.com/docs/liquid/).

## Adding pages

To **add a page** to your website (e.g. detailed resume):

1. Create a new `.html` or `.md` file at the `/_pages/` of your repository.
2. Give it a filename that you want to be used in the page's URL (e.g. `http://yourname.github.io/pages/filename`).
3. At the start of your file, include the following [front matter](https://jekyllrb.com/docs/front-matter/):

```
---
layout: pages
title: "YOUR_PAGE_TITLE"
description: "YOUR_PAGE_DESCRIPTION"
permalink: pages/YOUR_PAGE/
---
```

4. If you want to use Liquid, enter only front matter in your page file, then create a file with the contents in `_includes`, and add `include_html: YOUR_LIQUID_FILE` to front matter in the page file.

## Adding category page

To **add a category page** to your website like **Blog** menu:

1. Create a new `.html` or `.md` file at the `/_categories/` of your repository with front matter.

```
---
layout: categories
title: "YOUR_CATEGORY_TITLE"
description: "YOUR_CATEGORY_DESCRIPTION"
permalink: YOUR_CATEGORY_NAME
pagination:
  enabled: true
  category: YOUR_CATEGORY_NAME
---
```

2. Add a new link in your `_config.yml` with their [Octicon](https://octicons.github.com/).

```
  - title: YOUR_CATEGORY_NAME
    octicon: OCTICON_NAME
    url: YOUR_CATEGORY_NAME
```

## Adding blog posts

To **add a blog post** to your website:

1. Create a new `.md` file in your repository's `/_posts/` directory.
2. Give it a filename using the following format:

```
YEAR-MONTH-DAY-title.MARKUP
```

3. At the start of your file, include the following [front matter](https://jekyllrb.com/docs/front-matter/):

```
---
layout: post
title: "YOUR_POST_TITLE"
date: 2019-01-29 00:00:00
description: 'meta description'
og_type: article
tags:
- Blog
categories:
- Blog
twitter_text: 'Type description for twitter card'
introduction: 'Type your description for Thought section or category page'
---
```

Your website comes with a placeholder blog post that you can reference. Notably, its [front matter](https://jekyllrb.com/docs/front-matter/) declares `published` as `false`, so that it won't appear on your website.

While you can define a `layout` in the front matter, your website is pre-configured to assign the `post` layout to all of the posts in your `/_posts/` directory. So you don't have to declare that in your posts.

Jekyll's conventions for authoring and managing blog posts is very flexible. You can [learn more in Jekyll's documentation for "Posts."](https://jekyllrb.com/docs/posts/)

You can also specify an image or video to be used as a thumbnail in Thought section or category page. Just add `image: YOUR_IMAGE_URL` or `youtube: YOUTUBE_VIDEO_URL`, `vimeo: VIMEO_VIDEO_URL`, `video: YOUR_VIDEO_URL` to the front matter.

### Use jQuery lightSlider in your post

Add image sliders on your post using the [jQuery lightSlider](https://github.com/sachinchoolur/lightslider) supported by the theme. Just write the code anywhere you want in the post.

```
<div class="yslider">
  <ul>
    <li>
      <img src="YOUR_IMG_URL" alt="YOUR_IMG_DESCRIPTION" />
    </li>
    ## INSERT MORE <li><img></li> LIKE ABOVE IN ORDER ##
  </ul>
</div>
```

## Use Formspree contact form

Replace your email address to `YOUR_EMAIL_ADDRESS` in the `/_pages/contact.md`. So people can send you an inquiry mail via [Formspree](https://formspree.io/).

## Privacy policy

Enter your privacy policy at the `/_pages/privacy-policy.md`. You can easily make using [Privacy Policy Generator](https://www.privacypolicygenerator.info/).

## Styles

Your website is pre-configured to use [GitHub's very flexible CSS framework called "Primer,"](https://styleguide.github.com/primer/). It's currently referenced within your `styles.scss` file, using the CSS import at-rule:

```
@import url('https://unpkg.com/primer/build/build.css');
```

You are, of course, welcome to remove it or replace it with another framework. Just bear in mind that the HTML that your website came pre-packaged with references multiple Primer "utility classes" to define things like column widths, margins, and background colors.

You also have the option to add on to and extend Primer's styles by adding custom CSS to your `/assets/styles.scss` Sass stylesheet. By editing this file, you can customize your website's color scheme, typography, and more.


## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
