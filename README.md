# www-chapter-okinawa

OWASP Foundation Web Respository

Website: <https://owasp.org/www-chapter-okinawa/>

## Building

```sh
rm -f Gemfile.lock
docker pull jekyll/jekyll:latest
docker run -it --rm \
  -v ${PWD}:/srv/jekyll \
  jekyll/jekyll:latest \
  jekyll build
```

### Use bundle cache

```sh
docker run -it --rm \
  -v ${PWD}:/srv/jekyll \
  -v ${PWD}/vendor/bundle:/usr/local/bundle \
  jekyll/jekyll:latest \
  jekyll build
```

If you want to know more [Jekyll Docker](https://github.com/envygeeks/jekyll-docker/blob/master/README.md).

### Auto regeneration

```sh
docker run -it --rm \
  -v ${PWD}:/srv/jekyll \
  -v ${PWD}/vendor/bundle:/usr/local/bundle \
  jekyll/jekyll:latest \
  jekyll build --watch --incremental
```

### serve

```sh
docker run -it --rm \
  -v ${PWD}:/srv/jekyll \
  -v ${PWD}/vendor/bundle:/usr/local/bundle \
  -p 4000:4000
  jekyll/jekyll:latest \
  jekyll serve --incremental
```

Browse to <http://localhost:4000/>
