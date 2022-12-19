## Build
It is possible to build the website using the jekyll docker image. To do this, first build the docker image
```bash
docker build . -t hartzerj_website
```

Then run jekyll build in the image after mounting the current directory
```shell
docker run --rm --volume="$PWD:/srv/jekyll" -it hartzerj_website jekyll build
```

Finally, serve the website with the current directory mounted 
and the port mapped to [localhost:4000](http://localhost:4000/)
```shell
docker run --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 -it hartzerj_website jekyll serve --watch
```