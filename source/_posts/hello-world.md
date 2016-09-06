---
title: Hello World
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)

## Tag plug-in
### Hexo-Tag-FontAwesome
This tag plug-in allows you to use font awesome in the post.
* Install
```bash
npm install hexo-tag-fontawesome
```
   And then copy the `fontawesome.js` to the theme folder you used, put it under the `<your theme>/scripts/tags/`, like `./themes/Next/scripts/tags/`.
* Usage
```markdown
{% fa refresh spin %}
{% fa home fw %}
```


