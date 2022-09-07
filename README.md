# Datavillage Documentation

## Deployment

This static  website is automatically deploy using GitHub Pages and can be accessed [here](https://datavillage-me.github.io/developer-documentation/)

## Development

This site uses [jekyll](jekyllrb.com) with the [just-the-docs template](https://github.com/just-the-docs/just-the-docs).

To run it locally, make sure all the [jekyll dependencies](https://jekyllrb.com/docs/installation/) are installed on your machine.

Before starting, make sure the following line in the `_config.yaml` is uncommented, if not the theme isn't recognised locally:

```
theme: just-the-docs
```

Then run the following commands:

```bash
gem install jekyll bundler
```

And then at the root project folder:
```bash
bundle exec jekyll serve
```

The website should now be accessible at [http://localhost:4000](http://localhost:4000).