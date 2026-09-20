# The Allies Manifesto

## Deployment

### Local Environment

#### Prerequisites

1. Install Ruby 3.4, Jekyll and Bundler according to [this doc](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll#prerequisites). The gem `github-pages` does not work with Ruby 4.
2. Run `bundle install`.

#### Serving

Run:

```shell
bundle exec jekyll serve --baseurl=""
```

The website is served at: http://localhost:4000

#### Update Dependencies

To update Gemfile.lock, run:

```shell
bundle update

# Linux, Windows (modern Ruby with UCRT), macOS Intel, macOS Apple Silicon
bundle lock --add-platform x86_64-linux --add-platform x64-mingw-ucrt --add-platform x86_64-darwin --add-platform arm64-darwin
```

## Contributing

### Images

Images must be compressed before being committed and pushed. Use [WebP](https://developers.google.com/speed/webp/docs/using) to compress images to 256 KB or less.

[Installation](https://www.npmjs.com/package/cwebp):

```shell
npm install cwebp
```

Usage:

```shell
img_name="assets/img/path/to/name"
cwebp $img_name.jpg -o $img_name.webp -size 262144
```
