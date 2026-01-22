# blog-personal

personal blog hosted by GitHub pages

## Features

- Static site generation with Hugo
- Automated deployment via GitHub Actions
- Hosted on GitHub Pages with custom domain (.ru)

## Usage

### create post

```bash
# creates a draft post from the template in archetypes/post.md
hugo new --kind post <folder>/$(date +%Y%m%d-%H%M%S).md
```

### embedded web server

Start development server at http://localhost:1313/

```bash
hugo server -D
# -D (or --buildDrafts) includes draft posts in build and display
```

## Setup

### Prerequisites

- Homebrew (macOS)
- Git

### Installation

```bash
brew install hugo
hugo new site . --format yaml --force
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### Clone existing repository

```bash
git clone git@github.com:naavlad/blog-personal.git
cd blog-personal
git submodule update --init --recursive
```

## Deploy

Deployment is automated via GitHub Actions. Push to main branch to trigger deployment to GitHub Pages.
