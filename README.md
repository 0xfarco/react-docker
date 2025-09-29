# Dockerize react app
---

```bash
npm create vite@latest react-docker
```

- update package.json file

```
--SNIP--
"scripts": {
    "dev": "vite --host",
--SNIP--
```

```bash
docker build -t react-docker .
docker run -p 5173:5173 react-docker 
```
