# Sapling
## A Hugo Theme specifically for daycare and similar service industry companies

This theme is in development and not ready for use...yet


## Submodule Instructions

* Remove existing go.mod and go.sum files
* hugo mod init sapling
  * Creates a go.mod file in the root of the project

Make sure the config file has a module import
[[module.imports]]
  path = "github.com/KeyofSamuel/sapling-hugo-theme"
  # Sapling

this is going to create a go.mod file in the root of your project. In the excellent Discourse discussion “Hugo modules for ‘dummies’,” there’s a bit of ambiguity on what to pass to hugo mod init. If we take the Hugo documentation website as a guide, it’s a good practice to use your repository name. It makes for clear and easy reading, too: module github.com/gohugoio/hugoDocs is more obvious to me than the name of a theme or other label.

Add a theme as a Hugo module
Now for the fun part: let’s pull in a theme. Update the: [module]

[[module.imports]]
    path = "path-to-theme"
    # project theme
Note well that this path does not want a protocol — path = "gitlab.com/neotericdesign-tools/cosette" but no https://. As a standard practice, I like to note in a comment that this is the theme. Hugo is smart and mounts this as if it were at /themes/your-theme/, but it’s nice to be explicit.

Get the project’s module dependencies
While you can just hugo server and watch the magic happen, it’s instructive to be explicit, too. Running hugo mod get walks through your config and resolve external dependencies. At this point, with no theme in your /themes/ folder and no explicit theme declared in your config.toml — no need to declare theme = "my-theme-name" once you’re on modules! — you can run hugo server and see the magic.

Running hugo mod init your-project-repo generates the go.mod file, and thus initializes your project as a module. You can undo that, or redo that, at any time, by deleting the go.mod file and re-initializing the project. When you’ve resolved external dependencies, you’ll see them automatically in the require statement in the go.mod file. The go.sum file contains [cryptographic checksums of the content of the module version]. It’s not a lock file — so it retains checksums for modules even after they’ve been removed from your config.
