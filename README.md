# Hugo Extended Docker Image with NodeJS and PostCSS CLI

This is a docker image I created to build hugo websites, using hugo-extended with both node and postcss-cli on Google Cloud Build.

## Usage

```yaml

steps:
  # install dependencies
  - name: "gcr.io/cloud-builders/yarn"
    args: ["--cwd", "hugo", "install"]
  # Build
  - name: "gcr.io/$PROJECT_ID/hugo-extended"
    args: ["--minify"]
  # Deploy
  # ...

```
