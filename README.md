# A website/web app template built on Flask and run on Docker

## Design philosophy

Having (finally) delved into the wonderful world of Docker, I wanted to make a template website/web app container to use for future projects. I needed a couple things:

- Python compatibility, allowing complex backend applications (e.g., TensorFlow implementation)
- Standardization of web pages, i.e., site-wide nav-bars, footers, etc.

To accomplish these needs, this template was created using:

- Flask, a Python-based framework for serving web content
- Flask-Bootstrap, allowing HTML templates to be inherited site-wide

Notes on the file/folder structure:

- Page routes are defined in *app/app.py*, points to HTML file
- HTML files found in *app/templates/*; pages [extend](https://pythonhosted.org/Flask-Bootstrap/basic-usage.html) *base.html*
- Anything else found in a website's codebase, images, favicons, CSS files, etc., should go in *app/static/*

## Docker compose

```
$ cd flask-docker-base
$ docker compose up -d
```

Using a web browser, nagivate to *docker-host-ip:8080*.
