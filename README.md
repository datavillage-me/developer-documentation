# Datavillage Documentation

## Deployment

This static website is automatically deploy using GitHub Pages and can be accessed [here](https://datavillage-me.github.io/developer-documentation/)

## Development

This site uses [mkdocs](https://www.mkdocs.org/).
To use mkdocs locally, first install the python dependencies :
``` bash
$> pip install -r requirements.txt
```

Then, the documentation can be served locally uising 
``` bash
$> mkdocs serve
```

or deployed online using
``` bash
$> mkdocs gh-deploy
```

which will build then deploy the docs to the gh-pages branch of the current git repo, i.e. https://docs.datavillage.me/00-index.html