<!--
{
"name": "readme",
"version" : "0.1",
"title" : "Outlearn Hello World",
"description" : "Get Started with Your Path in 5 Minutes",
"homepage" : "https://github.com/outlearn-content/outlearn-modules",
"coverImage" : "https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/assets/lights.jpg",
"freshnessDate" : 2015-05-18,
"author" : "Teppo Jouttenus",
"license" : "CC BY 4.0",
"contact" : {"email" : "teppo@outlearn.com"}
}
-->

<!-- @section -->

## Create an Outlearn Account

### Viewing This on GitHub?

If you are viewing this on GitHub and want to get the full experience, check out [Publishing Great Learning Content](https://pilot.outlearn.com/learn/outlearn/outlearn-publishing) on Outlearn.

### Join With GitHub

You can unleash the power of publishing on Outlearn by joining with your GitHub account. [Click here to create an Outlearn account](https://pilot.outlearn.com/auth/join). Click "Join With GitHub" so that Outlearn can access and publish your content. GitHub will ask for your permission using a popup like the one below.

![GitHub sign-in popup](https://raw.githubusercontent.com/outlearn-content/outlearn-publishing/master/images/authorize.png)

If you have already signed up, you can [go to settings](https://pilot.outlearn.com/settings) and Link GitHub with your Outlearn account.

<!-- @task, "text" : "Create an Outlearn account and then mark this task as completed."-->


<!-- @section -->

## Duplicate and Edit the Template Repo

We know you are busy and would rather focus on writing awesome content than setting up directory structures and choosing naming conventions. Never worry, you'll be all set with our [outlearn-modules](https://github.com/outlearn-content/outlearn-modules) GitHub repository. Your first step is to duplicate this repo. If you are just trying things out and don't mind having your repo public, you can [fork](https://guides.github.com/activities/forking/) outlearn-modules. In that case, you can skip the steps in the code block below.

If you want to use a private repo or want to change the repo name, [create a new repo](https://help.github.com/articles/creating-a-new-repository/) where you want to copy the contents of the template. Next, you need to perform a bare-clone and a mirror-push. The instructions below assume you have created a new repo called `exampleuser/new-repository` and use an `ssh` connection. You can also [clone using `https`](https://help.github.com/articles/duplicating-a-repository/). For `ssh`, type these commands at the command line:

```bash
$ git clone --bare git@github.com:outlearn-content/outlearn-modules.git
# Make a bare clone of the repository

$ cd outlearn-modules.git
git push --mirror git@github.com:exampleuser/new-repository.git
# Mirror-push to the new repository

$ cd ..
$ rm -rf outlearn-modules.git
# Remove our temporary local repository
```

<!-- @task, "text" : "Create a duplicate the outlearn-modules repository, either by forking or by bare-cloning."-->

Once you have duplicated the repository, open up `outlearn.json` found at the root of your newly created duplicate repo. Now update the following Path metadata fields in the file:


| Field | Description                                            |
| ----- | ------------------------------------------------------ |
| name  | used for the database, must be unique for your user account or organization |
| title | shown at the top of Path cards                         |
| description | shown on the Path card as additional information |

The relevant part of your file should now look like this:

```json
"paths" : [
  {
    "name" : "your-new-path-name",
    "title" : "The Name You Just Chose",
    "description" : "More explanation about your the glorious purpose of your path",
    "privacy" : "public",
    "pages" : [
      {"page" : "./pages/welcome.md"},
      {"module" : "my-outlearn-module"},
      {"page" : "./pages/closing.md"}
    ]
  }
],
```

<!-- @task, "text" : "Update Path metadata and push the changes to GitHub."-->

<!-- @section -->

## Publish Your Path

The best way for you to test Path creation is to see your changes in real time on Outlearn. This section will show you how to do that.

Choose [Import Content](https://pilot.outlearn.com/import/github)
from the menu in the top right corner under the user icon.

![GitHub import](https://raw.githubusercontent.com/outlearn-content/outlearn-publishing/master/images/import.png)

Add a GitHub Repository and choose your newly created repo. Modify the default nickname if you want to and import the repository.

![GitHub import](https://raw.githubusercontent.com/outlearn-content/outlearn-publishing/master/images/choose-repo.png)

<!-- @task, "text" : "Import your repository."-->

You should now see the nickname of your integration
under your GitHub Integrations. Click on the name,
then click on the green check under Import History. You
will see the imported Paths and Modules. Now click on the
Path and you will see your very first Outlearn Path, in all its glory.
Congratulations!

![GitHub import](https://raw.githubusercontent.com/outlearn-content/outlearn-publishing/master/images/import-history.png)



<!-- @section -->

## Say Hello!

### Pages and Modules

Now that you've laid out what your Path is all about, it's time to get some content in it. Paths are made up of two basic components: _Pages_ and _Modules_. The Modules are the building blocks of a Path. You might write them all yourself or you can include Modules written by others.

An ideal Module provides good stand-alone learning value, making it a good candidate to be reused effectively in many Paths. As you create your Module, we recommend that you avoid referencing other Modules within the Module content. If you do so, you run the risk of confusing learners who might find themselves in a learning Path that does not includes the referenced Module.

To help make sense of the Modules in your Path, you can put in Context Pages (aka "Path Pages", or just "Pages"). Pages are the glue that holds the Modules together. They let you add in more of your own personality as a curator of modules created by others and they add context for the surrounding Modules. Pages are specific to a Path so you can talk about why you chose the Modules you did, how they fit together, what parts are super important, and relate the content to concepts your specific audience already understands. Use pages whenever a little expert context and commentary might be helpful.


### Outlearn Uses Markdown

We wanted to have an authoring experience that integrates seamlessly with GitHub and is easy as well as expressive. We think Markdown strikes a great balance between those goals. You can read the official [Markdown Syntax](http://daringfireball.net/projects/markdown/syntax) for more details. Outlearn also supports all the extensions of [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/). If you already have your content in Markdown, importing it to Outlearn is a breeze.

### Your First Content Edits

By now you are probably itching to get to publish something you actually wrote. Go ahead and edit the file `welcome.md` in the `pages` directory. You can replace everything there with your very own "Hello World" message, or something else that inspires you! The Pages are written in Markdown so feel free to try out some formatting as well.

Now go back to the [Import Content](https://pilot.outlearn.com/import/github) section on Outlearn, click on the nickname and then click "Re-Import". If you still have your Path open, refresh your browser and you can see your edits. Or navigate to it same way as above. Houston, we have a lift-off!

> **Note**: don't forget to push your committed changes to GitHub before re-importing to Outlearn.  And if you selected the `autoimport` option for this Content Source, you can just refresh the Page and you'll see change momentarily without manually re-importing.

Now you know how to get a "Hello World" Path up in less than 5-minutes. Hopefully you've seen enough of the power of Outlearn Paths to keep reading the rest of this Module to put some real content into your Path.

<!-- @section -->

## Add Your Content

### Organize Your Path

The meat of the Path is in the Modules. Once you have written some new Markdown or repurposed older content, this is how you make it part of your Path:

* Open the `my-outlearn-module.md` file in the `modules` directory.
* Update the metadata at the beginning of the file, including a new name for the Module, e.g. `awesome-first-module`.
* Add your Markdown content to the file under the first section.
* Save your file with a new name. We recommend using the Module name also as the file name, e.g. `awesome-first-module.md`.
* Edit `outlearn.json` and replace `{"module" : "my-outlearn-module"}` with `{"module" : "awesome-first-module"}`. This tells the Path how to reference the new Module.
* Declare the Module in the `modules` section in `outlearn.json` by replacing `"olm" : "./modules/my-outlearn-module.md"` with `"olm" : "./modules/awesome-first-module.md"`. This tells Outlearn where the source file for the Module is.

The body of your `outlearn.json` will now look like this:

```json
"paths" : [
  {
    "name" : "your-new-path-name",
    "title" : "The Name You Just Chose",
    "description" : "More explanation about your the glorious purpose of your Path",
    "privacy" : "public",
    "pages" : [
      {"page" : "./pages/welcome.md"},
      {"module" : "awesome-first-module"},
      {"page" : "./pages/closing.md"}
    ]
  }
],

"modules" : [
  {"olm" : "./modules/awesome-first-module.md"}
],
```

<!-- @task, "text" : "Add your first Module into the Path."-->

### Including Images and Videos

Outlearn supports the regular Markdown syntax for including images.

```markdown
![sea](https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/assets/sea.jpg)
```

You can add videos with the following annotations:

```markdown
< !-- @asset, "contentType": "outlearn/video", "provider": "vimeo", "url": "https://player.vimeo.com/video/67325705" -->

< !-- @asset, "contentType": "outlearn/video", "provider": "youtube", "url": "https://www.youtube.com/embed/CmjeCchGRQo" -->
```


<!-- @section -->

## Enrich Your Content

Outlearn provides a number of annotations in Markdown that act like magic dust.  When you include them, we can create a more interactive and trackable experience for your content.  These annotations are all HTML comments, which means they degrade gracefully when you content is rendered elsewhere (like in a GitHub README.md file).

### Adding Sections

The simplest way to enrich your content is to divide it into sections. Each Module can have one or more sections. A list of sections shows up on tge right side of the content and serves as a navigable table of contents. Sections can also be checked off as completed in order to help learners and Path creators to keep track of progress.

You create a section by adding the following annotation:

```markdown
< !-- @section, "title": "Getting started" -->
```

Alternatively, you can leave out the "title" attribute and the platform will take the first heading after the section tag and make it the title. So you could replace the above code with:

```markdown
< !-- @section -->

## Getting Started
```

This can be especially helpful when you just want to add sections quickly to an existing Markdown file and it also makes the file render more nicely on GitHub.


### Add Tasks, Links

Nothing kills learner motivation like hours of reading and watching videos without a way to try it out yourself. Great teachers push the learners to put new knowledge to practice. The easiest way to create meaningful interactions with the learners on Outlearn is to add tasks, some of which may contain deliverables. A task can be as simple as "Run `make` in your project directory" or more involved such as "Download the library and compile it in your system."

You can optionally define deliverables that are to be submitted as part of task completion. For example, you can ask learners to "Fork the project repo on GitHub, add the following functionality, send a pull request to the original repo, then paste the the pull request URL below." Path authors and organization admins can see which tasks have been done and the contents of the deliverables that learners have submitted. They can then organize further activities such as code reviews.

To add a task:

```markdown
< !-- @task, "text" : "Run the above code example on your own machine."-->
```

If you also want to add a task deliverable:

```markdown
< !-- @task, "hasDeliverable" : true, "text" : "Fork the repository above, fix the broken test, and submit a URL for your pull-request."-->
```

For an external link that gets unfurled inside the platform:

```markdown
< !-- @link, "url" : "https://nodejs.org/", "text": "Install NodeJS" -->
```

### Add Cover Images

Each Module in the Path can have a cover image that's a visual representation of the Path or Module.  Really it's just there to make your content stand out as more attractive, we'll provide a default pattern if you don't add a custom image. You add them in the header with a line:

```markdown
"coverImage" : "https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/assets/lights.jpg",
```

<!-- @section, "title": "Wrapping Up" -->

A couple items to finish up:

* You can delete or repurpose this `README.md` file once you're done with it.
* Feel free to use the duplicated copy of outlearn-modules as a basis for all your content, or author your own learning repositories from scratch, GitHub import is supported for all compatible repos.
