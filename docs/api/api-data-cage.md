---
layout: default
title: Code provider API
parent: APIs References
nav_order: 2
---
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta
    name="description"
    content="SwaggerUI"
  />
  <title>SwaggerUI</title>
  <link rel="stylesheet" href="https://unpkg.com/swagger-ui-dist@4.5.0/swagger-ui.css" />
</head>
<body>
<div id="swagger-ui"></div>
<script src="https://unpkg.com/swagger-ui-dist@4.5.0/swagger-ui-bundle.js" crossorigin></script>
<script>
  window.onload = () => {
    window.ui = SwaggerUIBundle({
      /* url: 'https://api-dev.datavillage.me/docs/data-cage-swagger.yaml',
       hardcode permalink to latest main version in the dv-platform codebase */
      url: 'https://raw.githubusercontent.com/datavillage-me/dv-platform/main/packages/api/static/data-cage-swagger.yaml?token=GHSAT0AAAAAAB24CMDQVKBZSMGEMDX2UHDEY357FMA',
      dom_id: '#swagger-ui',
    });
  };
</script>
</body>