# Heroku (partial) Buildpack for Post-release

**This buildpack is deprecated. You need to specify the post-release command in your Procfile instead.**

This buildpack is intended to be inserted into a multi-builpack chain. e.g.

```bash
heroku buildpacks:add -i 1 https://github.com/heroku/heroku-buildpack-postrelease
```

It checks for a `post-release` script in app.json, and if present, writes a
special, hidden script into the slug, which is then run after every release.
For use with the [release-phase beta](https://devcenter.heroku.com/articles/release-phase?preview=1).
