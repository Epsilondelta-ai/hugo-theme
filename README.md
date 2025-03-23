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
  _merge = 'deep'
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
baseURL = 'https://tech.epsilondelta.ai/'
languageCode = 'ko-KR'
title = '엡실론델타 테크블로그'
theme = 'epsilondelta'
enableRobotsTXT = true

[markup]
  _merge = 'deep'

[params]
  _merge = 'deep'
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
  [params.giscus]
    enabled = true
    repo = 'Epsilondelta-ai/tech.epsilondelta.ai'
    repoId = '***'
    category = 'General'
    categoryId = '***'
    theme = 'light'

# [services]
#   [services.disqus]
#     shortname = 'your-disqus-shortname'
#   [services.googleAnalytics]
#     id = 'G-MEASUREMENT_ID'

[pagination]
  _merge = 'deep'

[taxonomies]
  _merge = 'deep'

[[menus.main]]
name = 'Tags'
pageRef = '/tags'
weight = 10

[[menus.main]]
name = 'Authors'
pageRef = '/authors'
weight = 20

[sitemap]
  changefreq = "daily"
  filename = "sitemap.xml"
  priority = 0.5

[build]
  _merge = 'deep'
[module]
  [[module.mounts]]
    source = 'assets'
    target = 'assets'
  [[module.mounts]]
    disableWatch = true
    source = 'hugo_stats.json'
    target = 'assets/notwatching/hugo_stats.json'
```

## ShortCodes

### codesandbox

```go-template
{{< codesandbox aaaaa >}}

{{< codesandbox id="aaaaa" width="100%" height="500px" >}}
```

### codepen

```go-template
{{< codepen aaaaa >}}

{{< codepen id="aaaaa" width="100%" height="500px" >}}
```
