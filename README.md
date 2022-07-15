# AIR-AIoT Group Website

We build our website based on the [Research Group Web Site Template](https://github.com/uwsampa/research-group-web). For detailed usage, please reference the template's [README](https://github.com/uwsampa/research-group-web/blob/master/README.md).

This work is licensed under a [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

## Personnel

People are listed in `_data/people.yml` in the following format.

```yml
example:
    display_name: "Example Name"
    webpage: "https://example.com"
    role: grad
    image: /img/people/example.jpg
    bio: Example Bio
```

`role`s are defined in `_config.yml`.

`webpage`, `image` and `bio` are optional.

## News Items and Blog Posts

Create a file in the `_posts` directory using the naming convention `YYYY-MM-DD-title-for-url.md`.

The file must begin with [YAML front matter](http://jekyllrb.com/docs/frontmatter/). For news updates, use this:

    ---
    layout: post
    shortnews: true
    ---

For full blog posts, use this format:

    ---
    layout: post
    title:  "Some Great Title Here"
    ---

And concoct a page title for your post. The body of the post goes after the `---` in either case.

You can also customize the icon that is displayed on the news feed. By default it's `newspaper-o`. We use icons from the [FontAwesome](http://fontawesome.io/icons/) icon set.

## Projects

Create a markdown file in the `_projects` folder. Here are the things you can put in the YAML frontmatter:

- `title:` The project title.
- `notitle:` Set this to `true` if you don't want a title displayed on the project card. Optional.
- `description:` The text shown in the project card. It supports markdown.
- `people:` The people working on the project. This is a list of keys from the `_data/people.yml` file.
- `layout: project` This sets the layout of the actual project page. It should be set to `project`.
- `image:` The URL of an image for the project. This is shown on both the project page and the project card. Optional.
- `last-updated:` Date in the format of `YYYY-MM-DD`. The project cards are sorted by this, most recent first.
- `status: inactive` Set this to `inactive` if don't want the project to appear on the front page. Just ignore it otherwise.
- `link:` Set this to an external URL if this project has a page somewhere else on the web. If you don't have a `link:`, then the content of this markdown file (below the YAML frontmatter) will be this project's page.
- `no-link: true` Set this if you just don't want a project page for your project.