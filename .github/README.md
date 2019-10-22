# Liquid Includes MathJax
[heading__title]:
  #liquid-includes-mathjax
  "&#x2B06; Top of ReadMe File"


Liquid includes file enables JavaScript sourcing of MathJax on Jekyll built Pages


## [![Byte size of includes-mathjax.html][badge__master__include_mathjax__source_code]][include_mathjax__master__source_code] [![Open Issues][badge__issues__include_mathjax]][issues__include_mathjax] [![Open Pull Requests][badge__pull_requests__include_mathjax]][pull_requests__include_mathjax] [![Latest commits][badge__commits__include_mathjax__master]][commits__include_mathjax__master] [![Includes MathJax Demos][badge__demo__include_mathjax]][demo__include_mathjax]



------


#### Table of Contents


- [:arrow_up: Top of ReadMe File][heading__title]

- [:zap: Quick Start][heading__quick_start]

  - [:memo: Edit Your ReadMe File][heading__your_readme_file]
  - [:factory: Edit Your Layout][heading__your_layout_file]
  - [&#x1F578; Utilize Includes MathJax][heading__utilize]
  - [:floppy_disk: Commit and Push][heading__commit_and_push]

- [&#x1F5D2; Notes][heading__notes]

- [:card_index: Attribution][heading__attribution]

- [&#x2696; License][heading__license]


------



## Quick Start
[heading__quick_start]:
  #quick-start
  "&#9889; Perhaps as easy as one, 2.0,..."


**Bash Variables**


```Bash
_module_name='includes-mathjax'
_module_https_url="https://github.com/liquid-utilities/${_module_name}.git"
_module_relative_path="_includes/modules/${_module_name}"
```


**Bash Submodule Commands**


```Bash
cd "<your-git-project-path>"

git checkout gh-pages
mkdir -vp "_includes/modules"

git submodule add\
 -b master --name "${_module_name}"\
 "${_module_https_url}" "${_module_relative_path}"
```


### Your ReadMe File
[heading__your_readme_file]:
  #your-readme-file
  "&#x1F578; Suggested additions for your ReadMe.md file so everyone has a good time with submodules"


Suggested additions for your _`ReadMe.md`_ file so everyone has a good time with submodules


```MarkDown
Clone with the following to avoid incomplete downloads


    git clone --recurse-submodules <url-for-your-project>


Update/upgrade submodules via


    git submodule update --init --merge --recursive
```


### Your Layout File
[heading__your_layout_file]:
  #your-layout-file
  "&#x1F3ED; Suggested additions for your default layout file"


**[`_layouts/default.html`](https://github.com/jekyll/minima/blob/master/_layouts/default.html)**


```Liquid
<!DOCTYPE html>
<html lang="{{ page.lang | default: site.lang | default: "en" }}">

  {%- include head.html -%}

  <body>
    {%- include modules/includes-mathjax/includes-mathjax.html -%}

    {%- include header.html -%}

    <main class="page-content" aria-label="Content">
      <div class="wrapper">
        {{ content }}
      </div>
    </main>

    {%- include footer.html -%}

  </body>

</html>
```


### Utilize Includes MathJax
[heading__utilize]:
  #utilize-mathjax
  "&#x1F578; How to make use of this submodule within another project"


**`_posts/2019-04-02-points-00-preface.md`**


```YAML
---
layout: post
title:  "Points 00 Preface"
date:   2019-04-02 06:05:58 -0700
categories: graph
mathjax: true
---


> _Unwrapped_ Graph of Nodes Example


$$
  \color{#000}{\fbox{ w }}{
  \color{#2E8B57}{ \xleftarrow[]{\color{#000}{X}} }}
  \color{#00A}{ \fbox{ u } }{
  \color{#2E8B57}{ \xrightarrow[]{\color{#000}{X}} }}
  \color{#000}{\fbox{ v }}
\\
  \color{#000}{\fbox{ u }}{
  \color{#FF0000}{ \xleftarrow[]{\color{#000}{O}} }}
  \color{#00A}{ \fbox{ v } }{
  \color{#2E8B57}{ \xrightarrow[]{\color{#000}{X}} }}
  \color{#000}{\fbox{ w }}
\\
  \color{#000}{\fbox{ v }}{
  \color{#2E8B57}{ \xleftarrow[]{\color{#000}{X}} }}
  \color{#00A}{ \fbox{ w } }{
  \color{#FF0000}{ \xrightarrow[]{\color{#000}{O}} }}
  \color{#000}{\fbox{ u }}
$$
```



### Commit and Push
[heading__commit_and_push]:
  #commit-and-push
  "&#x1F4BE; It may be just this easy..."


```Bash
git add .gitmodules
git add _includes/modules/includes-mathjax


## Add any changed files too


git commit -F- <<'EOF'
:heavy_plus_sign: Adds `liquid-utilities/includes-mathjax#1` submodule



**Additions**


- `.gitmodules`, tracks submodules AKA Git within Git _fanciness_

- `README.md`, updates installation and updating guidance

- `_includes/modules/includes-mathjax`, injects JavaScript sourcing of MathJax
EOF


git push origin gh-pages
```


**:tada: Excellent :tada:** your site is now ready to begin unitizing code from this repository!


___


## Notes
[heading__notes]:
  #notes
  "&#x1F5D2; Additional things to keep in mind when developing"


Some but not all configurations have been made available from site `_config.yml` and page/post FrontMatter contexts


**`_config.yml`**


```YAML
mathjax:
  version: "2.7.5"
  config: "MMLorHTML.js"

  jax:
    - "input/TeX"
    - "input/MathML"
    - "output/HTML-CSS"
    - "output/NativeMML"

  extensions:
    - "tex2jax.js"
    - "mml2jax.js"
    - "MathMenu.js"
    - "MathZoom.js"

  TeX:
    extensions:
      - "AMSmath.js"
      - "AMSsymbols.js"
      - "noErrors.js"
      - "noUndefined.js"
```


Pull Requests are most welcomed to add features and/or fix bugs.


___


## Attribution
[heading__attribution]:
  #attribution
  "&#x1F4C7; Resources that where helpful in building this project so far."


Resources that where helpful in building this project so far


- [MathJax Configuration Documentation](https://docs.mathjax.org/en/v1.0/configuration.html)

- [MathJax Configuration Files Documentation](https://docs.mathjax.org/en/v1.1-latest/config-files.html#the-tex-ams-mml-htmlormml-configuration-file)


___


## License
[heading__license]:
  #license
  "&#x2696; Legal bits of Open Source software"


Legal bits of Open Source software


```
Includes MathJax ReadMe documenting how things like this could be utilized
Copyright (C) 2019  S0AndS0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation; version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```



[badge__commits__include_mathjax__master]:
  https://img.shields.io/github/last-commit/liquid-utilities/includes-mathjax/master.svg

[commits__include_mathjax__master]:
  https://github.com/liquid-utilities/includes-mathjax/commits/master
  "&#x1F4DD; History of changes on this branch"


[include_mathjax__community]:
  https://github.com/liquid-utilities/includes-mathjax/community
  "&#x1F331; Dedicated to functioning code"


[include_mathjax__gh_pages]:
  https://github.com/liquid-utilities/includes-mathjax/tree/gh-pages
  "Source code examples hosted thanks to GitHub Pages!"



[badge__demo__include_mathjax]:
  https://img.shields.io/website/https/liquid-utilities.github.io/mathjax/index.html.svg?down_color=darkorange&down_message=Offline&label=Demo&logo=Demo%20Site&up_color=success&up_message=Online

[demo__include_mathjax]:
  https://liquid-utilities.github.io/mathjax/index.html
  "&#x1F52C; Check the example collection tests"


[badge__issues__include_mathjax]:
  https://img.shields.io/github/issues/liquid-utilities/includes-mathjax.svg

[issues__include_mathjax]:
  https://github.com/liquid-utilities/includes-mathjax/issues
  "&#x2622; Search for and _bump_ existing issues or open new issues for project maintainer to address."


[badge__pull_requests__include_mathjax]:
  https://img.shields.io/github/issues-pr/liquid-utilities/includes-mathjax.svg

[pull_requests__include_mathjax]:
  https://github.com/liquid-utilities/includes-mathjax/pulls
  "&#x1F3D7; Pull Request friendly, though please check the Community guidelines"


[badge__master__include_mathjax__source_code]:
  https://img.shields.io/github/size/liquid-utilities/includes-mathjax/includes-mathjax.html.svg?label=includes-mathjax.html

[include_mathjax__master__source_code]:
  https://github.com/liquid-utilities/includes-mathjax/blob/master/includes-mathjax.html
  "&#x2328; Project source, one Liquid file of actionable code!"
