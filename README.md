<div align="center">
  <img src="https://avatars.githubusercontent.com/u/166383361?s=200&v=4" alt="Epsilon Delta Logo" width="100" height="100">
  <h1>Epsilon Delta Hugo Theme</h1>
</div>

## Features

## Installation

### Git Submodule

```bash
git submodule add https://github.com/epsilondelta-ai/hugo-theme.git themes/epsilondelta
# Or to update to the latest version
git submodule update --remote
```

### Install TailwindCSS

[Hugo TailwindCSS Document](https://gohugo.io/functions/css/tailwindcss/)  

#### Step 1

```bash
npm install --save-dev tailwindcss @tailwindcss/cli
```

#### Step 2

Add this to your site configuration. e. g. `hugo.toml`

```toml
[build]
  [build.buildStats]
    enable = true
  [[build.cachebusters]]
    source = 'assets/notwatching/hugo_stats\.json'
    target = 'css'
  [[build.cachebusters]]
    source = '(postcss|tailwind)\.config\.js'
    target = 'css'
[module]
  [[module.mounts]]
    source = 'assets'
    target = 'assets'
  [[module.mounts]]
    disableWatch = true
    source = 'hugo_stats.json'
    target = 'assets/notwatching/hugo_stats.json'
```

## Configuration

example here

```toml
[params]
  description = '엡실론델타 테크블로그입니다.' # for meta og tag
  images = ['logo.jpg'] # for meta og tag
  title = '엡실론델타 테크블로그' # for meta og tag
  # [params.social]
  #   facebook_admin = 'jsmith' # for meta og tag
  #   twitter = 'GoHugoIO' # for meta twitter tag
  titleStrong = '엡실론델타'
  titleLight = '테크블로그'
  logo = '/logo.jpg'
  featuredTags = [] # 페이지 상단에 강조하고 싶은 태그들을 나열합니다.

# [services]
#   [services.disqus]
#     shortname = 'your-disqus-shortname'
#   [services.googleAnalytics]
#     id = 'G-MEASUREMENT_ID'

[pagination]
  disableAliases = false
  pagerSize = 6
  path = 'page'

[taxonomies]
  tag = 'tags'
  author = 'authors'
  post = 'posts'
  series = 'series'
```