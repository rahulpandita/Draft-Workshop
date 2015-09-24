---
layout: post
title:  "Creating this blog"
date:   2015-09-22 12:00:00
categories: Tutorial
---

This blog was put together using [Jekyll](https://jekyllrb.com/) and [Github Pages](https://github.com/).
Listed next are the steps I followed:

* Create a Repostory in Github named "blog". While creating the repostory also include a default `.gitignore` file of type Jekyll.
* Clone the repository on your local machine (I have a OSX machine).
* Install Jekyll by running `gem install jekyll` on command prompt. *(No need to install Ruby, as Ruby 2.0 is included in OS X Yosemite and Mavericks. OS X Mountain Lion, Lion, and Snow Leopard ship with Ruby 1.8.7.)*
* Run `jekyll new blog` on command prompt. A folder named "blog" will be created.
* Copy the contents of the folder into the folder where the "blog" repository has been cloned.
* In command prompt switch to "blog" repostory folder and execute command `jekyll serve`. This command compiles the contents of the website into static web pages and places the in "_site" folder. Next, this command hosts (locally) the created pages by default at `http://127.0.0.1:4000/`
* Point your web browser to `http://127.0.0.1:4000/` to see the generated content.
* Use `Ctrl+C` to stop hosting.
* Push the changes back to repository in the branch "gh-pages". This is important because the Github uses this branch to render the pages. All the site related changes must be pushed to "gh-pages" branch. If you had included the default `.gitignore` file of type Jekyll during the creation of the repostory, the generated "_site" folder and its contents will be ignored. This is important because Github internally uses Jekyll to generate web pages, and if you check in "\_site" folder, that may interfere with Github internal process. *Have to confirm this though*
* your blog should be active on `yourGithubUsername`.github.io/blog. If not give it a couple of hours.
* For adding posts, type your posts in markup and place them in the "_posts" folder. The naming convention of the placed file is `yyyy-mm-dd-postname.markdown`. 
* Use the following template for the header of each post. The first lines of the markdown files 
{% highlight console %}
 ---
layout: post
title:  "Post_NAME"
date:   YYYY-mm-DD HH:MM:SS
categories: Tutorial
 ---
{% endhighlight %}

* Run `jekyll serve` on commandline to see how the posts looks and make adjustment to markdown if necessary.
* Push you changes to repository (remember the "gh-pages" branch).
* Happy publishing :smile:

####Other Useful Resources

1. [Jekyll Configuration Information](https://jekyllrb.com/docs/home/)
2. [Github Pages](https://pages.github.com/)
3. [Jekyll Themes](http://jekyllthemes.org/)
4. [Jekyll Blog Tutorial Video](https://www.youtube.com/watch?v=iWowJBRMtpc)
5. [Repostory for this blog](https://github.com/rahulpandita/blog)
6. [Github Markdown](https://guides.github.com/features/mastering-markdown/)
7. [Emoji in Markdown :sunglasses:](https://github.com/jekyll/jemoji)
