# Hamilton Institute Blog <img src='img/logo2.png' align="right" height="139" />

This repository hosts the content of the Hamilton Institute blog 
[insert link here later], where our research group publishes blog
posts about a wide variety of topics. Currently, we are focusing
on our COVID-19 in Ireland project, so the posts will be mainly related
to our findings regarding this subject



## Contribution guide
------------------------------------------------------------------------
  
  This is a `jekyll` based website, but if you have any familiarity with
R/Rmarkdown, the contribution will be very simple. First, two main R packages 
need to be installed:
  
  * `knitr`
* `distill`

They're both available from CRAN. If you are interested in publishing a 
post in this blog, follow these steps:


0) **Clone this repository in your local machine.** If you don't
know how to do that, please follow [this guide](https://brunaw.com/slides/git-workshop/git-workshop.html) or ask
another member of the group for help. 


If this is not your first time writing a blog post, please
**pull** the repository changes first, also described in the
previous link. Not doing this will generate conflicts between 
your local folder and the current state of the repository. 

1) Assuming R and RStudio to be already installed, open a new RStudio 
session in the repository you just cloned. Preferably, you can use
an [RStudio project](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects). 


2) In your RStudio session, check if your directory is set to be 
your local folder of the blog repository and load the two packages: 
  
  ```
# install.packages("knitr","distill")
library(knitr)
library(distill)
```

4) Run the following command to create a new rmarkdown file
for your post: 
  
  ```
create_post("Insert the title of you post here")
```

This will create a new folder in the `_posts` folder,
where the content of your post will be stored. 

5) Open the new rmarkdown file and write the post. You can follow
the guidelines [at this link](https://rstudio.github.io/distill/) 
for more details on how to write a `distill` rmarkdown post. 

Since the post is rmarkdown based, it will accept pretty much 
everything that rmarkdown uses: R code, python code, images, 
html tags, etc. For guidelines on how to use rmarkdown, please
[see this link](https://bookdown.org/yihui/rmarkdown/). 

6) **Knit** your rmarkdown file, by either clicking the 'knit' button on
RStudio or using the `command + enter + k` shortcut. Please verify
that an .html file was created in your post folder, and check
that everything is as you expected it to be in that file. 

7) At last, run the following in your RStudio session:
  
  ```
library(rmarkdown)
render_site()
```

And check how your post looks like in the blog, by opening 
the `docs/index.html` and going to the *Posts* section of the
blog. 

8) Upload your new post to the GitHub repository, as described at 
[this link](https://brunaw.com/slides/git-workshop/git-workshop.html). 
At this step, **please avoid uploading objects such as**
  
  - The .DS_Store objects
- The .Rproj file, in case you created one in your local machine

Those objects are not part of the blog and shouldn't be uploaded. 
In addition, since this repository belongs to a big group, 
please avoid changing other features
of the blog without letting the maintainers know first. A small
change in one of the core files might lead the blog to 
fully stop working.  

After this, you're done and your post will soon appear in the blog!
  If you have any questions, please [raise an issue](https://github.com/hamilton-institute/hamilton-institute.github.io/issues) or get in touch via Slack. 

------------------------------------------------------------------------