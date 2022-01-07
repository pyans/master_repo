# A Template for Master Thesis

## Feature

- Build tex source without LaTeX setup
    - Use Docker instead
- Automated build on cloud
    - [x] GitHub Actions
    - [x] BitBucket Pipelines

## Environment

- macOS 10.14 or later
- Docker Desktop for Mac 2.1 or later

or use Linux.

- Ubuntu 18.04 LTS
- Docker 18.06 ot later

This repository will use TeX Live 2019 on Ubuntu 19.10.

## Usage

The default operation is to use a Docker container.
If you want to operate it natively instead of Docker, set the environment variable `USE_DOCKER=no`.The default is `USE_DOCKER=yes`.

Build with Docker environment.

```bash
$ make pdf
```

Build with your own LaTeX environment.

```bash
$ USE_DOCKER=no
$ make pdf
```

Watch the tex source and build continuously.

```bash
$ make watch
```

After deleting all artifacts from the previous compilation, run the compilation.

```bash
$ make all
```

Delete all artifacts.

```bash
$ make clean
```

Create a new branch from the current branch, do an empty commit, and push to the remote.
After that, use the `hub` command to display the pull request creation page in a your browser.
You can specify the branch name at runtime. If not specified, the default value `WIP` will be used.

```bash
$ make draft branch=NAME
```

If you want to use custom `.latexmkrc`, please add it into this repository.
Use the following command to copy the `.latexmkrc` used in the container directly under this directory.

```bash
$ make latexmkrc
```

Runs a lint locally.
You will need to install Nodejs and run `npm install` beforehand.

```bash
$ make lint
```

Fixed the ones that violated lint and can be applied automatically.
You will need to install Nodejs and run `npm install` beforehand.

```bash
$ make fix
```

## Automated build

GitHub Actions and BitBucket Pipelines will start when you push your changes to `master` branch.  
It build PDF automatically, and you can download the latest artifact.

If you want to leave older version, please use `tag`.  

```bash
$ git tag -a v1.0.0 -m "Some messages"
$ git push --tags
```

The archives will be available on GitHub Releases or BitBucket Download.

### BitBucket Pipelines

Setup your credential for Pipeline is needed.
Please follow this guide to deploy the artifacts.

https://support.atlassian.com/ja/bitbucket-cloud/docs/deploy-build-artifacts-to-bitbucket-downloads/

### NOTE

Automated build on cloud consume some resources. The resources is limited for private repository.

- GitHub Actions
    - Free: 2000 minutes / month
    - Pro (Academic): 3000 minutes / month
- BitBucket Pipelines
    - Free: 50 minutes / month
    - Academic: 500 minutes / month

If you do not want to use them, please disable them from their settings.

## Author

Shoma Kokuryo
