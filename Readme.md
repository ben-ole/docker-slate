[Slate](https://github.com/lord/slate) boxed in a minimal [docker image](https://hub.docker.com/r/elchbenny/docker-slate).

# Usage in Development with docker compose

```yaml

  docs:
    image: elchbenny/docker-slate    
    ports:
      - 4002:4567
    volumes:
      - ./path-to-your-source/index.html.md:/slate/slate-2.0.0/source/index.html.md

```

visit http://localhost:4002

# Generate Documentation

- `docker-compose exec docs bundle exec middleman build`
- check the build folder (`/slate/slate-2.0.0/build`) of the container