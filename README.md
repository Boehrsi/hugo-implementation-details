# Implementation details

![https://github.com/Boehrsi/hugo-implementation-details/blob/master/docs/screenshot.png](https://github.com/Boehrsi/hugo-implementation-details/blob/master/docs/screenshot.png)

A simple theme for documentation and best practices websites for the [Hugo static site generator](https://gohugo.io/). It was created to provide a simple and minimalistic base for documentation or tips for developers.

# Setup

- Use **Hugo extended** 
- Clone the repository into your `themes` directory in your Hugo project
- Activate the theme in the config file (e.g. `config.toml`) of your Hugo project
- You are ready to use it, no configuration or further setup is required

# How to use

- `content/_index.md` contains the home page
- `content/about.md` contains the about page
- `content/contribute.md` contains the contribute page
- `content/entries` contains all entries
  - An entry is added by creating a **folder**
  - Within the entry folder at least the `index.md` file must exist
  - Additionally and optionally a `bad.md` and / or `good.md` could exist. If those files exist they are shown below the content of the `index.md` file. Those files are meant to show code examples only
  
# Examples

We create a folder `content/entries/awesome-article/` in our Hugo project, which contains the following three files.

## content/entries/awesome-article/index.md


    ---
    title: "Awesome article*"
    date: 2020-09-12T16:00:00+02:00
    authors: ["Mr. Author"]
    categories: ["Good stuff", "Code"]
    links: ["https://dart.dev/"]
    ---

    You shoud do it the right way!


## content/entries/awesome-article/good.md

    ---
    title: "Good is better"
    ---

    ```dart
    void test() {
        // testing is good
    }
    ```

## content/entries/awesome-article/bad.md

    ---
    title: "Bad is not good"
    ---

    ```dart
    void noTest() {
        // bad
    }
    ```
# Resources 

- https://github.com/google/material-design-icons