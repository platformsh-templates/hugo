> [!WARNING]
> **This repository is no longer maintained by our internal teams.**  
> The template is provided *as is* and will not receive updates, bug fixes, or new features.  
> You are welcome to contribute on it or fork the repository and modify it for your own use.
> To deploy this template on [Upsun](https://www.upsun.com), you can use the command [upsun project:convert](https://docs.upsun.com/administration/cli/reference.html#projectconvert)
> on this codebase to convert the existing `.platform.app.yaml` configuration file to the [Upsun Flex format](https://docs.upsun.com/create-apps/app-reference/single-runtime-image.html).

# Hugo for Platform.sh

This template provides a basic Hugo skeleton.  All files are generated at build time, so at runtime only static files need to be served.  The Hugo executable itself is downloaded during the build hook. You can specify the version to use by updating the `.platform.app.yaml` file.  It also includes a minimal template to get you started, but you are free to replace it with your own template.

Hugo is a static site generator written in Go, using Go's native template packages for formatting.

## Features

* Go 1.15
* Automatic TLS certificates
* Hugo downloaded on the fly during build

## Post-install

The `content` directory includes two pieces of sample content, provided so that the initial install has some content to show.  Replace it with your actual content as desired.

You can also remove the `minimal` theme if you so desire and replace it with one you download or one you create yourself.

## Customizations

The following changes have been made relative from initializing a new Hugo project with `hugo new site`. If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.
* The `minimal` theme has been included by default.  Feel free to remove it and replace with your own if you prefer.  Consult the Hugo documentation for instructions on how to add and enable themes.

## References

* [Hugo](https://gohugo.io/)
* [Go on Platform.sh](https://docs.platform.sh/languages/go.html)
