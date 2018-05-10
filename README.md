## Personalized blog & profile

[![Website PageSpeed](https://pagespeed-badges.herokuapp.com/?url=rahulja.in)](https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Frahulja.in%2F)
[![Lighthouse Performance score: 100/100](https://lighthouse-badge.appspot.com/?score=100&compact&category=Performance)](files/Lighthouse-Report.pdf)
[![Lighthouse PWA score: 82/100](https://lighthouse-badge.appspot.com/?score=82&compact&category=PWA)](files/Lighthouse-Report.pdf)
[![Lighthouse Accessibility score: 86/100](https://lighthouse-badge.appspot.com/?score=86&compact&category=Accessibility)](files/Lighthouse-Report.pdf)
[![Lighthouse Best Practices score: 94/100](https://lighthouse-badge.appspot.com/?score=94&compact&category=Best+Practices)](files/Lighthouse-Report.pdf)
[![Lighthouse SEO score: 90/100](https://lighthouse-badge.appspot.com/?score=90&compact&category=SEO)](files/Lighthouse-Report.pdf)

[![GitHub license](https://img.shields.io/github/license/xRahul/xRahul.github.io.svg?style=flat-square)](https://github.com/xRahul/xRahul.github.io/blob/new-site/LICENSE)
[![Build Status](https://travis-ci.org/xRahul/xRahul.github.io.svg?branch=new-site)](https://travis-ci.org/xRahul/xRahul.github.io)
![Gem Version](https://img.shields.io/gem/v/jekyll.svg)
[![Dependency Status](https://gemnasium.com/badges/github.com/xRahul/xRahul.github.io.svg)](https://gemnasium.com/github.com/xRahul/xRahul.github.io)
[![security](https://hakiri.io/github/xRahul/xRahul.github.io/new-site.svg)](https://hakiri.io/github/xRahul/xRahul.github.io/new-site)

![Image of rahulja.in](https://github.com/xRahul/xRahul.github.io/raw/new-site/_assets/images/posts/configure-this-site-locally-for-development/og-image%402x.png "rahulja.in")

Install ruby 2.4.3

```bash
rbenv install 2.4.3
rbenv global 2.4.3
ruby -v
```

Install site

```bash
git clone https://github.com/xRahul/xRahul.github.io.git
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=36000'
cd xRahul.github.io/
git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
git fetch --all
git pull --all

bin/setup
--or--
npm run setup
```

Run local development server

```bash
LC_ALL=en_US.UTF-8 bundle exec jekyll serve --drafts
--or--
npm run local
```

Deploy to github master branch

```bash
bin/deploy
--or--
npm run publish
```
