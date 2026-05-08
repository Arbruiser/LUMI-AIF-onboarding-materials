---
layout: default
title: Chapter 1 - Getting Started with LUMI
nav_order: 2
---

# This is an example of an extra page
You can use this to add structure and introduce chapters/modules and not have everything on one page. 

You can even **add subchapters** to this chapter by creating another `.md` file (e.g., `chapter-1-1`) if you edit the header of this file to be something like:

```yaml
---
layout: default
title: Chapter 1 - Getting Started with LUMI
nav_order: 2
has_children: true
---
```

... and the header of the new subchapter as:

```yaml
---
layout: default
title: Authentication & Environment
parent: Chapter 1 - Getting Started with LUMI  # Matches the title of the parent page
nav_order: 1               # Order within the chapter
---
```
all pages other than `index.md` can have any name. 