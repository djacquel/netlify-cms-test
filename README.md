## Debuging Netlify CMS

Basic Jekyll 4.0

Installed admin following https://www.netlifycms.org/docs/add-to-your-site/

Configured posts edition with :

    backend:
      name: git-gateway
      branch: master

    site_url: https://upbeat-euler-2e4306.netlify.com
    display_url: https://upbeat-euler-2e4306.netlify.com

    media_folder: "img"

    collections:
      - name: "posts"
        label: "Posts"
        folder: "_posts"
        create: true
        slug: "{{year}}-{{month}}-{{day}}-{{slug}}"
        fields:
          - {label: "Title", name: "title", widget: "string"}
          - {label: "Publish Date", name: "date", widget: "datetime"}
          - {label: "Featured Image", name: "thumbnail", widget: "image"}
          - {label: "Body", name: "body", widget: "markdown"}

Everything is ok.

Added summary config for posts

    summary: "{{year}}-{{month}}-{{day}}-{{slug}}"

Everything is ok

