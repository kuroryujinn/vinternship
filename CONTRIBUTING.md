---
layout: page
title: Contributing
permalink: /contributing/
---

# How to Add a Markdown File to This Repository

This guide explains how to contribute a new markdown file (page) to the Vinternship site.

---

## Prerequisites

Before you begin, make sure you have:

- A [GitHub](https://github.com) account
- Git installed locally (`git --version` to verify)
- Followed the setup steps in the [GitHub Guide](/vinternship/git-guide/)

---

## Step 1 – Fork and Clone the Repository

Fork the repository on GitHub, then clone your fork locally:

```bash
git clone "https://github.com/<your-username>/vinternship.git"
cd vinternship
```

Create a new branch for your changes:

```bash
git checkout -b add/my-new-page
```

---

## Step 2 – Create Your Markdown File

Create a new `.md` file in the root of the repository (or in the appropriate collection folder). Every page intended to appear on the site **must** begin with a YAML front matter block:

```markdown
---
layout: page
title: My New Page
permalink: /my-new-page/
---

# My New Page

Write your content here using standard Markdown syntax.
```

### Front Matter Fields

| Field       | Required | Description                                      |
|-------------|----------|--------------------------------------------------|
| `layout`    | Yes      | Use `page` for a standard site page              |
| `title`     | Yes      | The title shown in the browser tab and header    |
| `permalink` | Yes      | The URL path for the page (e.g. `/my-new-page/`) |
| `order`     | No       | Controls sort order in navigation menus          |
| `parent`    | No       | Groups the page under a parent navigation item   |

---

## Step 3 – (Optional) Add the Page to the Navigation

If you want your page to appear in the site header, add its filename to the `header_pages` list in `_config.yml`:

```yaml
header_pages:
  - Intro.md
  - MyNewPage.md   # ← add your file here
```

---

## Step 4 – Commit and Push Your Changes

```bash
git add .
git commit -m "docs: add MyNewPage.md"
git push origin add/my-new-page
```

---

## Step 5 – Open a Pull Request

Go to your forked repository on GitHub. You will see a **Compare & pull request** banner. Click it, add a short title and description, then click **Create Pull Request**.

A member of the VLED team will review your PR, leave comments if needed, and merge it once approved.

---

## Markdown Basics

| Element        | Syntax                                      |
|----------------|---------------------------------------------|
| Heading        | `# H1`, `## H2`, `### H3`                  |
| Bold           | `**bold text**`                             |
| Italic         | `*italic text*`                             |
| Link           | `[link text](https://example.com)`          |
| Image          | `![alt text](image.png)`                   |
| Inline code    | `` `code` ``                               |
| Code block     | ` ```language … ``` `                      |
| Unordered list | `- item`                                    |
| Ordered list   | `1. item`                                   |
| Horizontal rule| `---`                                       |

For a full reference, see the [Markdown Guide](https://www.markdownguide.org/basic-syntax/).

---

*Happy Contributing!*
