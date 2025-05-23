# What is this?

* 👀image documentation / [EACH Docker Official Image](https://github.com/docker-library/official-images)👀

* ALL Markdown files here are
  * run -- through -- [tianon's fork of `markdownfmt`](https://github.com/tianon/markdownfmt)
  * verified as formatted correctly -- via -- GitHub Actions

-	[![GitHub CI status badge](https://img.shields.io/github/actions/workflow/status/docker-library/docs/ci.yml?branch=master&label=GitHub%20CI)](https://github.com/docker-library/docs/actions?query=workflow%3A%22GitHub+CI%22+branch%3Amaster)
-	[![library update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/library.svg?label=Automated%20library%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/library/)
	-	[![amd64 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/amd64.svg?label=Automated%20amd64%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/amd64/)
	-	[![arm32v5 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/arm32v5.svg?label=Automated%20arm32v5%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/arm32v5/)
	-	[![arm32v6 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/arm32v6.svg?label=Automated%20arm32v6%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/arm32v6/)
	-	[![arm32v7 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/arm32v7.svg?label=Automated%20arm32v7%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/arm32v7/)
	-	[![arm64v8 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/arm64v8.svg?label=Automated%20arm64v8%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/arm64v8/)
	-	[![i386 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/i386.svg?label=Automated%20i386%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/i386/)
	-	[![ppc64le update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/ppc64le.svg?label=Automated%20ppc64le%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/ppc64le/)
	-	[![s390x update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/s390x.svg?label=Automated%20s390x%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/s390x/)
	-	[![windows-amd64 update.sh status badge](https://img.shields.io/jenkins/s/https/doi-janky.infosiftr.net/job/docs/job/windows-amd64.svg?label=Automated%20windows-amd64%20update.sh)](https://doi-janky.infosiftr.net/job/docs/job/windows-amd64/)

# How do I update an image's docs

* TODO:
Edit the `content.md` for an image; not the `README.md` as it's auto-generated from the contents of the other files in that repo. To see the changes to the `README.md`, run `./update.sh myimage` from the repo root, but do not add the `README.md` changes to your pull request. See also `markdownfmt.sh` point [below](#how-do-i-add-a-new-images-docs).

After opening your Pull Request the changes will be checked by an automated `markdownfmt.sh` before it can be merged. A common issue is incorrect spacing such as with two lines missing an empty line between them (double-spaced).

# How do I add a new image's docs

-	Create a folder for my image: `mkdir myimage`
-	Create a `README-short.txt` (required, 100 char max)
-	Create a `content.md` (required)
-	Create a `license.md` (required)
-	Create a `maintainer.md` (required)
-	Create a `github-repo` (required)
-	Create a `metadata.json` (required)
-	Add a `logo.png` (recommended)

Optionally:

-	Run `./markdownfmt.sh -l myimage` to list any files that are non-compliant to [`tianon/markdownfmt`](https://hub.docker.com/r/tianon/markdownfmt).  
	Any files in the list will result in a failed build during continuous integration.
	-	run `./markdownfmt.sh -d myimage` to see a diff of changes required to pass.
-	Run `./update.sh myimage` to generate `myimage/README.md` for manual review of the generated copy.  
	**Note:** do not actually commit the `README.md` file; it is automatically generated/committed before being uploaded to Docker Hub.

# Files related to an image's docs

## folder `<image name>`

This is where all the partial (e.g. `content.md`) and generated files (e.g. `README.md`) for a given image reside, (e.g. `golang/`). It must match the name of the image used in `docker-library/official-images`.

## `README.md`

This file is generated using `update.sh`. Do not commit or edit this file; it is regenerated periodically by a bot.

## `content.md`

This file contains the main content of your image's long description. The basic parts you should have are a "What Is" section and a "How To" section. The following is a basic layout:

```markdown
# What is XYZ?

// about what the contained software is

%%LOGO%%

# How to use this image

// descriptions and examples of common use cases for the image
// make use of subsections as necessary
```

## `get-help.md`

This file is an optional override of the default `get-help.md`. This is the content of the "Where to get help" part of the "Quick reference" at the top of the generated README. We recommend linking to the best places for community support like forums, chat rooms, or mailing lists.

## `github-repo`

This file should contain the URL to the GitHub repository for the Dockerfiles that become the images. The file should be in a single line ending in a newline with no extraneous whitespace. Only one GitHub repo per image repository is supported. It is used in generating links. Here is an example for `golang`:

```text
https://github.com/docker-library/golang
```

## `license.md`

This file should contain a link to the license for the main software in the image. Here is an example for `golang`:

```markdown
View [license information](http://golang.org/LICENSE) for the software contained in this image.
```

## `logo.png`

Logo for the contained software. While there are not hard rules on formatting, most existing logos are square or landscape and stay within a few hundred pixels of width. Alternatively, a `logo.svg` can be used instead, but only one logo file will apply. To use it within `content.md`, put `%%LOGO%%` as shown above in the basic `content.md` layout.

The image is automatically scaled to a 120 pixel square for the top of the Docker Hub page and Hub search results.

## `maintainer.md`

This file should contain a link to the maintainers of the Dockerfile.

## `metadata.json`

This file contains data about the repo for Docker Hub. The minimum file is defined below. `./metadata.sh [repo-name]` must be used to correctly format it (use `-w` to apply its suggested format changes). Only three sorted unique Docker Hub categories are allowed. `metadata.json` in the root contains the list of categories to choose from. See descriptions for the categories on the [Docker docs site](https://docs.docker.com/docker-hub/repos/categories/).

```json
{
    "hub": {
         "categories": []
    }
}
```

## `README-short.txt`

This is the short description for the Docker Hub, limited to 100 characters in a single line.

> Go (golang) is a general purpose, higher-level, imperative programming language.

## `stack.yml`

This optional file contains a small, working [Compose file for Docker Swarm](https://docs.docker.com/compose/compose-file/compose-file-v3/) showing off how to use the image. To use the `stack.yml`, add `%%STACK%%` to the `content.md` and this will embed the YAML along with a link to directly try it in [Play with Docker](https://labs.play-with-docker.com/).

The file must work via `docker stack deploy` since that is how Play with Docker will launch it, but it is helpful for users to try locally if it works for `docker-compose` as well. Other official images may be referenced within the YAML to demonstrate the functionality of the image, but no images external to the Docker Official Images program may be referenced.

# Files for main Docs repo

## `update.sh`

This is the main script used to generate the `README.md` files for each image. The generated file is committed along with the files used to generate it. Accepted arguments are which image(s) you want to update or no arguments to update all of them.

This script assumes [`bashbrew`](https://github.com/docker-library/bashbrew/releases) is in your `PATH` (for scraping relevant tag information from the library manifest file for each repository).

## `markdownfmt.sh` and `ymlfmt.sh`

These two scripts are for verifying the formatting of Markdown (`.md`) and YAML (`.yml`) files, respectively. `markdownfmt.sh` uses the [`tianon/markdownfmt`](https://hub.docker.com/r/tianon/markdownfmt) image and `ymlfmt.sh` uses the [`tianon/ymlfmt`](https://hub.docker.com/r/tianon/ymlfmt) image.

## `.template-helpers/generate-dockerfile-links-partial.sh`

This script is used by `update.sh` to create the "Supported tags and respective `Dockerfile` links" section of each generated `README.md` from the information in the [official-images `library/` manifests](https://github.com/docker-library/official-images/tree/master/library).

## `.template-helpers/`

The scripts and Markdown files in here are used in building an image's `README.md` file in combination with its individual files.

# Scripts unrelated to templates

## `generate-repo-stub-readme.sh`

This is used to generate a simple `README.md` to put in the image's repo. We use this in Git repositories within https://github.com/docker-library to simplify our maintenance, but it is not required for anyone else. The only argument is the name of the image (or repo), like `golang` and it then outputs the readme to standard out.

## `push.pl` and `push.sh`

These are used by us to push the actual content of the READMEs to the Docker Hub as special access is required to modify the Hub description contents. The `Dockerfile` is used to create a suitable environment for `push.pl`.

# Community

* `#docker-library` IRC channel | [Libera.Chat](https://libera.chat/)
