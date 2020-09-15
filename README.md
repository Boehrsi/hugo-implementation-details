# Implementation Details

![https://github.com/Boehrsi/hugo-implementation-details/blob/master/docs/screenshot.png](https://github.com/Boehrsi/hugo-implementation-details/blob/master/docs/screenshot.png)

A simple theme for documentation and best practices websites for the [Hugo static site generator](https://gohugo.io/). It was created to provide a simple and minimalistic base for documentation or tips for developers.

## Setup

- Use **Hugo extended** 
- Clone the repository into your `themes` directory in your Hugo project
- Activate the theme in the config file (e.g. `config.toml`) of your Hugo project

### Configure the theme (optional)

The following variables can be set in the projects config file (`config.[yaml|toml|json]`). If a variable is not set, the given entry won't be shown.

```
[params]
    github = "YourGitHubLink"
    imprint = "YourImprintLink"
```

### Setup your favicon (optional)

Add the following files to your project. If a file is missing the theme will just skip it.

- static\favicon.ico
- static\icons\android-chrome-192x192.png
- static\icons\android-chrome-512x512.png
- static\icons\apple-touch-icon.png
- static\icons\favicon-16x16.png
- static\icons\favicon-32x32.png
- static\icons\favicon.ico
- static\icons\site.webmanifest

The `site.webmanifest` should be similar to the following snippet.

```
{
    "name": "",
    "short_name": "",
    "icons": [
        {
            "src": "icons/android-chrome-192x192.png",
            "sizes": "192x192",
            "type": "image/png"
        },
        {
            "src": "icons/android-chrome-512x512.png",
            "sizes": "512x512",
            "type": "image/png"
        }
    ],
    "theme_color": "#ffffff",
    "background_color": "#ffffff",
    "display": "standalone"
}
```


## How to use

- `content/_index.md` contains the home page
- `content/about.md` contains the about page
- `content/contribute.md` contains the contribute page
- `content/entries` contains all entries
  - An entry is added by creating a **folder**
  - Within the entry folder at least the `index.md` file must exist
  - Additionally and optionally a `bad.md` and / or `good.md` could exist. If those files exist they are shown below the content of the `index.md` file. Those files are meant to show code examples only
  - A new entry can be added via the Hugo CLI `hugo new --kind entry entries/my-post`
  
## Examples

We create a folder `content/entries/awesome-article/` in our Hugo project, which contains the following three files.

### content/entries/awesome-article/index.md


    ---
    title: "Awesome article*"
    date: 2020-09-12T16:00:00+02:00
    authors: ["Mr. Author"]
    categories: ["Good stuff", "Code"]
    links: ["https://dart.dev/"]
    ---

    You shoud do it the right way!


### content/entries/awesome-article/good.md

    ---
    title: "Good is better"
    ---

    ```dart
    void test() {
        // testing is good
    }
    ```

### content/entries/awesome-article/bad.md

    ---
    title: "Bad is not good"
    ---

    ```dart
    void noTest() {
        // bad
    }
    ```
## Resources 

- Icons: https://github.com/google/material-design-icons