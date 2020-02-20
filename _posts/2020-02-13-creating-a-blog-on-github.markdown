---
layout: post
title:  "Creating a Blog on GitHub"
date:   2020-02-13 20:37:24 -0500
categories: jekyll update
---
<!---
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

Jekyll requires blog post files to be named according to the following format:

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
--->
One easy way to build GitHub blog quickly is to fork [Jekyll template][jekyll-link]. But if you prefer some adventure and want to experiment eveything from scratch then this post is for you!

The first step to create a blog on GitHub is to have a [GitHub] [github-link] account. After log in to your account you will see a panel on the left to create a repository. Create a new repository and name it **your_user_name.github.io**. When creating the repository make it public, you may skip Initialize the repository with a ReadMe file, choose a licence of your preference. After creating the repository you will get the address of the repository similar to **https://github.com/your_user_name/your_user_name.github.io.git**.

Use the [git][git-command-link] tool to clone the repository to your own machine.

```
$git clone https://github.com/username/username.github.io
```

Now download and install the [Jekyll][jekyll-download-link] tool. This tool will mainly build your website. It has noting to do with GitHub. Open the **Windows command prompt** and check the Jekyll version to ensure it has been installed successfully.

```
jekyll -v
```

Now set the path of the command prompt to your cloned repository **your_user_name.github.io.git** and give the following [command][jekyll-in-existing-link]. The dot (.) here is part of the command.

```
jekyll new .
```

if you have pre-existing files in your repository then 

```
jekyll new . --force
```

It will create the structure of your website. Jekyll can help you to see the website on your localhost. Run the following command on Windows command prompt.

```
jekyll serve
```

It will generate a server address (http://). Copy-paste that to your browser. Your Blog is ready. Congratulations!

Now you can go online pushing your site to your GitHub account. Use the Git bash to give the following command on you project directory

```
$git add --all
$git commit -m "Initial Commit"
$git push -u origin master
```

Now go to to your GitHub repository (refresh if it's already open). It should show the uploaded project in the master branch. Go to the **Settings** of your repository. Under the **GitHub Pages** section you will find the link of your website. If it's showing *Your site is ready to be published at http://* then wait a while and refresh your page. It will change to *Your site is published at http://*

Your blog is online now, but it's holding only the default contents. You can customize it in your own way. One starting point is *_config.yml*. To publish your blog content modify following the format of the post given as an example inside the directory *_posts/*. The link to your post will appear automatically in your Front matter.

You can customize your blog directly on GitHub or on your local machine. If you work on your local machine you can use [VSC][vsc-link] (Visual Studio Code) (a text editor will also do).

After modifying your code, save it and check the website using Jekyll on your own machine

```
jekyll serve
```
If Jekyll is already running simply refresh the page. If the contents of the page doesn't change even after refreshing then stop Jekyll and try

```
bundle exec jekyll clean
jekyll serve
```

When satisfied commit the changes using git bash and push it to your GitHub account.


[jekyll-link]: https://github.com/barryclark/jekyll-now
[jekyll-download-link]: https://jekyllrb.com/docs/installation/windows/
[github-link]: https://github.com/
[git-command-link]: https://pages.github.com/
[jekyll-in-existing-link]: https://michaelsoolee.com/jekyll-existing-folder/
[vsc-link]: https://code.visualstudio.com/