# <img src="https://avatars.githubusercontent.com/u/106743612" alt="logo" style="height: 35px;"/> Demagh8 Wiki

Password protect Jekyll posts. Forked from [lilykonings](https://github.com/lilykonings/jekyll-password-protect).
Visit [my Wiki here!](https://demagh8.github.io)

## Usage
### Unencrypted Posts
Just add a markdown file to ``_posts``. The markdown will be public in github

### Encrypted Posts
Just add a normal post to ``_protected`` then encrypt it using
```bash
WIKIPASS=mypass gulp wiki:encrypt
```
Gulp will simply encrypt your markdown post and create an encrypted version in ```_posts```.

*Important notes*:

* files in ``_protected`` will be git ignored. It's your responsibility to backup
* gulp will re-encrypt all protected posts every run. If you change the ``mypass``, it will affect older/existing posts
* To workaround the above issue, and add extra secrecy, you may delete ``_protected`` posts once encrypted
* To edit an encrypted ``_posts`` later, simply inspect the ``<article>`` element, and [convert it to markdown](https://codebeautify.org/html-to-markdown)
* Liquid templating isn't currently supported in protected posts, use only Markdown syntax supported by [marked](https://marked.js.org/)
