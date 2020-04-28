---
title: Guidelines
description: This page aims to both provide guidelines for working on this site, and in doing so establish the project's aims. 
author: ibraheem_rodrigues
---

{% include toc.md %}

## Contributing

Contributions are welcome, as long as they fit the style, aims and ethos of this project, detailed here.

If you have any suggestions or issues either submit a [github issue]({{site.github.issues_url}}) or [email me](site.author.email).

If you want to create content for this project, please first read over these guidelines.

You should either:

- Fork this repo, make your changes/additions and then submit a pull request.
- Get in touch using one of the links above

Seed `README.md` for how to run the jekyll site locally.

## Key Terms

These are the key terms, that should be used when refereing to parts of the project.

- **Spegman's Every Ref.** (aka 'The Project', 'The Guide', 'The Site')
  - **Content** - Everything in the `_content/` folder
    - **Categories** - Information grouped by common theme/context
      - **Pages** (aka 'Guides')
  - **Infrastructure** (aka 'The Code') - Anything that is a part of the site, but not directly viewable by the end user
  

## Structuring a Page

All pages should be written in markdown. This site uses [kramdown-flavour markdown](https://kramdown.gettalong.org/) as is standard for Jekyll sites.

Page files should be under their respective [category](#current-categories) in the `_content` folder, and must include the front matter as defined [below](#template).

Files can be structured in one of two ways:
1. `<category>/<name>.md` (e.g.`misc/spoons.md`)
2. `<category>/<name>/index.md` (e.g. `misc/spoons/spoons.md`)

File names should separate words with underscores `_` (snake case)

### Template
```md
---
title: Spoons # Mandatory
description: Common and popular spoons # Optional
author: j_spegman # Mandatory

image: spoon.png #  Optional, for SEO
---

Spoons come in 3 flavours...
```

### Adding media
If you wish to add media to use in a page (images, etc.):
- Use [file structure 2](#structuring-a-page)
- Put media files in the page folder

Media which is generic to all pages in a category may be included in the category folder.

### Adding a Table of Contents
To include a table of contents in on page, add the following code at the top, immediately following the front matter.

{% raw %}
```md
---
# Blah, blah front matter
---

{% include toc.md %}

<!-- Content here -->
```
{% endraw %}


## Writing Guidelines

Guides should be factual and to the point. However this guide is as much about interest as it is about factuality - while all included information must be true, we do not aim to be encyclopedic.

We aim to collect things that are useful, unusual, or tell a story of the human endeavour to understand and categorise the world around us.

### Standardisation

For the sake of consistency:

- Spelling should be according to British English
- Use CE/BCE as opposed to AD/BC
- Dates should be in the DD/MM/YYYY format
- Times should be given in 24 hour format (00:00 - 11:59)

### Block Quotes

To quote directly from a source, or elsewhere in the guide, use a block quote:

```md
> To be, or not to be
```

When you give attribution, either link to a source as [below](#citing-sources) or use the following syntax for direct attribution:

```md
> To be, or not to be
>
> *Hamlet by William Shakespeare, Act 3 Scene 1*
```

```md
> To be, or not to be
>
> [*Hamlet by William Shakespeare, Act 3 Scene 1*](http://shakespeare.mit.edu/hamlet/hamlet.3.1.html)
```

### Maths
We use MathJAX (v2) to render mathematical equations.

Use `$$` to define equations:
```
$$ y = mx + c $$
```

> $$ y = mx + c $$


This works for both inline and block level (automatically detected, note `$...$` is not supported by kramdown):

```
Quadratic equations have the form \$$ y = ax^2 + bx + c $$
```

> Quadratic equations have the form $$ y = ax^2 + bx + c $$

To force it to render in the opposite level (inline to block and vice versa) use `\$$ ... $$`

```
If $$ y = 0 $$ you can find x: \$$ x=\frac{-b\pm\sqrt{b^2-4ac}}{2a} $$
```

> If $$ y = 0 $$ you can find x: \$$ x =\frac{-b\pm\sqrt{b^2-4ac}}{2a} $$

The [LaTeX Wiki](https://en.wikibooks.org/wiki/LaTeX/Mathematics#Symbols) has a good reference for typesetting equations.

### Citing sources

Prefer: \\
**Primary sources (firsthand evidence)** over \\
 **Secondary sources (interpretations, analyses)** over \\
 **Tertiary sources (compilations, summarisations)**.

As such Wikipedia (tertiary) is usually never a good source.

Citations should include (at a minimum) author, place of access (book title/page, website url) and date accessed (websites only).

To cite sources use kramdown's footnote syntax:

```md
Spoons are most commonly made of steel.[^1] <!-- Link to footnote -->

Spoons come in many flavours.[^1] <!-- Use it again-->

[^1]: https://spoons.info (Accessed 01/04/2020) <!-- Define the footnote -->

```

See the [kramdown footnote docs](https://kramdown.gettalong.org/syntax.html#footnotes) for more.


## Site Structure

Content for this project can be found in the `/_content/` folder.

Within this folder, subfolders for each category can be found ([list](#current-categories)). All reference pages must be in one of these subfolders, else they will not be indexed.

Each category folder must include an `index.md`, with the following front matter:

```md
---
title: <CATEGORY NAME HERE>
layout: category
---
```

### Important Files

| Name | File | Description |
|----------|--------|-------------|
| Home | `index.md` | Site homepage. |
| Guidelines | `guidelines.md` | Information related to contributing to the reference. |
| README | `README.md`| Information related to developing the technical side of the site. |
| WIP/Planned Content | `wip.md` | Record of work-in-progress or planned pages |


### Current Categories

| Category | Folder | Description |
|----------|--------|-------------|
| Miscellaneous |`misc/`| Anything that does not belong in another category. |
| Mathematics | `mathematics/` | Math(s) related reference. Geometry, Numbers, Set tTheory etc. |
| Science | `science/` | Scientific reference - Physics, Chemistry, Biology etc.  |
| Standards | `standards/` | Reference for standards - e.g from ISO, w3c, Unicode Consortium |
| Languages | `language/` | Languages, alphabets and linguistics reference |

### Adding an author
To add yourself as an author, add an entry to `/_data/authors.yml`, like follows:

```yml
j_spegman:
    name: Jeg Spegman
    email: jeg@speg.info
    url: https://twitter.com/spegman
```

Your name will link to `url` (see top of page)

See the [template](#template) for how to list a page's author

## Versioning

We aim to follow [Semantic Versioning](https://semver.org/), however as the original specification is not intended for non-code applications, the following guidelines will be used to follow semver's spirit - chiefly to communicate intent.

> Under this scheme, version numbers and the way they change convey meaning about the underlying code and what has been modified from one version to the next.
>
> [*https://semver.org/*](https://semver.org/)


### Content Related Versioning

Changes to the content of the site (specifically everything under `/_content/`) should increment the version numbers for the following reasons:

`MAJOR.MINOR.PATCH`

- MAJOR - changes which overhaul content/formatting structure
- MINOR - content additions and removals
- PATCH - content updates and fixes (spelling, accuracy, etc.)

**Important notes when changing pages (MINOR changes):**

If a page is moved or merged with another, the new page should redirect from the old page url:

```yml
---
redirect_from: /misc/old_page
---
```

If a page is deleted, a file should be left in its place informing any users of this change.

Whether these temporary pages should be kept after a MAJOR change should be decided on a case by case basis.

### Infrastructure Related Versioning

Versions seeing updates to code and should increment version numbers as per the original semver spec, and suffix `-code` to the version:

`MAJOR.MINOR.PATCH-code`




