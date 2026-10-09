# Template for a series of developer presentations

To build a series of HTML presentation from Markdown files, like [this one](https://www.aramislab.fr/multiple-dev-presentations/).

If you only have a single presentation to build, prefer [this template](https://github.com/aramis-lab/dev-presentation).

This repo was generated with the tool [Slidev](https://sli.dev/). Have a look at [this](https://aramislab.fr/dev-presentation) to see what Slidev can do!

To create your own presentations, [create a GitHub repository in the ARAMIS Lab organization](https://github.com/organizations/aramis-lab/repositories/new), select this repository as a template, and follow these instructions:

## Setup

Once you have created your repo from this template, look for all the occurrences of `multiple-dev-presentations` and **replace them with the name of your repository**.

## Installation

### Install Node.js

Install `Node.js`:
```bash
brew install node@24
```

Check `Node.js` version:
```bash
node -v # must return v24.21.0
```

Check `npm` version:
```bash
npm -v # must return 11.19.0
```

### Install the dependencies

```bash
npm install
```

## Start the slide show

To open one of your presentation, run:

```bash
npm run dev <x-presentation.md> # for example npm run dev 1-example.md
```

You can modify the corresponding markdown and view the changes live.

## Build the website

To build the entire website with all your presentations, run:

```bash
npm run site
```

Then, open `http://localhost:3000/<your-repo>/`.

## Add a new presentation

Create a markdown file at the root of the project. The name of the file **must start with a number**.

Then, modify `index.html`, which is the homepage, by adding a reference to your new presentation:

```html
      <a class="menu-card" href="2-new-presentation/index.html">
        <h2>A new presentation</h2>
        <p>Blabla</p>
      </a>
```

> [!NOTE]
> Here, the markdown is named `2-new-presentation.md`.

## Deploy your presentations online

If you want to deploy the series of presentations online, for example to share them, do the following steps:

1. On GitHub, go to `Settings` > `General` > `Danger Zone` > `Change repository visibility`, and make sure that the repository is public.
2. Then `Settings` > `Pages` > `Build and deployment`, and select `GitHub Actions`.
3. Commit something on your `main` branch (for example an empty commit with `git commit --allow-empty -m "trigger documentation deployment"`) and push it on GitHub.
4. On your repository main page, check that the deployment is successful in the section `Deployments` (you may have to refresh).
5. Your presentation should be available at `https://www.aramislab.fr/<your-repo>/` (or `http://www.aramislab.fr/<your-repo>/`).

The presentation will be rebuilt and deployed automatically every time you push on the `main` branch!

