# Published Journals

## Introduction

This is a directory for journal articles.

## How to add a new publication

Create a file named `YYYY-MM-DD-<topic>.md` in this directory. Year, month, and
date should match the article's date published **in an issue**. If either date
or month is not provided by the journal, simply set it to `01`.

The file content should be as followings:

```yaml
---
title: "<Title>"
authors: <Authors>
journal: <Journal>
categories:
  - <category 1>
  - <category 2>
  - ...
tags:
  - <tag 1>
  - <tag 2>
  - ...
redirect_to: <article doi>
---
```

If a publication is accepted, but not yet published in an issue, set the first
digit of the year to `8`, and add `accepted_in: YYYY-MM-DD` to the front matter.
If the publication is not even published online (i.e., no DOI is available),
also add text `*Manuscript in press*` to the content instead redirecting to a
DOI. Full example:

```yaml
# File: _posts/80xx-MM-DD-awesome-title.md
---
title: "<Title>"
authors: <Authors>
journal: <Journal>
categories:
  - <category 1>
  - <category 2>
  - ...
tags:
  - <tag 1>
  - <tag 2>
  - ...
accepted_in: 20xx-MM-DD
---
*Manuscript in press*
```

If a publication is submitted, but not yet accepted for publication, set the
digit of the year to `9`, and add `submitted_in: YYYY-MM-DD` to the front
matter. Omit the `journal` field. Full example:

```yaml
# File: _posts/90xx-MM-DD-awesome-title.md
---
title: "<Title>"
authors: <Authors>
categories:
  - <category 1>
  - <category 2>
  - ...
tags:
  - <tag 1>
  - <tag 2>
  - ...
submitted_in: 20xx-MM-DD
---
```

Note that the date **should be updated as soon as possible** to the date of
publication once the article is published in an issue. Don't forget to change
the file name as well.
