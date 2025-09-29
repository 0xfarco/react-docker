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
docker run -p 5173:5173 -v "$(pwd):/app" -v /app/node_modules react-docker 
```

```bash
docker login
docker tag react-docker <username>/react-docker
docker push <username>/react-docker
```
