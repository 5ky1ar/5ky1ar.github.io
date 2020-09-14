# PRoJEct-NeGYa

Hacker style personal homepage template.

Version: v1.01

## Features

1. Crazy
2. Rouge supports code highlighting
3. MathJax formula
4. Article Index
5. Highly customizable
6. Encrypted content (You can also change the element id to cipher text, and write "No access to this field!")

## Changelog

2019.7.17: Update documentation

2019.6.15: Lao Tzu will do this version, and it will work, but I wo n’t change it!

## Instructions

* Download or fork into your own github repository
* Modify _config.yml file
* (Custom domain name) modify CNAME file
* Modify the pages / index.md file to customize the homepage
* Delete files in the _posts / folder and add your own posts
* Sync to github remote warehouse

## Engineering Structure

Function and content isolation TMD!

Website content:
* _posts: articles
* pages: pages
* assets / img: picture

Functional style:
* _includes: subpage modules
* _layouts: page template (simple combination of subpage modules)
* assets / css: style sheet file
* assets / fonts: font files
* assets / js: script file
* _config.yml: configuration file
