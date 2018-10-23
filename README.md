# Cloud Foundry Markdown Buildpack

This buildpack allows you to seamlessly publish Markdown pages to a
Cloud Foundry platform: these files are automatically converted to HTML pages.

Just include this buildpack in your app manifest:

```yaml
---
applications:
  - name: appname
    memory: 64MB
    disk_quota: 100MB
    buildpacks:
      - https://github.com/alexandreroman/markdown-buildpack.git
```

Use environment variable `MARKDOWN_STYLESHEET` to specify which CSS stylesheet
to include:

```yaml
---
applications:
  - name: appname
    memory: 64MB
    disk_quota: 100MB
    env:
      MARKDOWN_STYLESHEET: "https://raw.githubusercontent.com/sindresorhus/github-markdown-css/gh-pages/github-markdown.css"
    buildpacks:
      - https://github.com/alexandreroman/markdown-buildpack.git
```

This project is using [Pandoc](http://pandoc.org) to convert Markdown to HTML.

Feel free to contribute!

Copyright (c) 2018 Pivotal Software, Inc.
Licensed under the Apache License, Version 2.0.
