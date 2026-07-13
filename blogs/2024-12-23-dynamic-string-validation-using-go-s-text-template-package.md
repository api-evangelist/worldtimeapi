---
title: "Dynamic string validation using go's text/template package"
url: "https://dev.to/sleeyax/dynamic-string-validation-using-gos-texttemplate-package-2b65"
date: "2024-12-23"
author: "Sleeyax"
feed_url: "https://dev.to/feed/sleeyax"
---
Imagine you could validate the following string: id: "d416e1b0-97b2-4a49-8ad5-2e6b2b46eae0" static-string: "abc" invalid-string: def random-number: 150 Using go template syntax like this: id: "{{isUUID}}" static-string: "abc" invalid-string: def random-number: {{inRange 100 200}} Well, that would be cool wouldn't it? Unfortunately this isn't supported by go's text/template package. I've built a library which uses a subset of the template syntax to cover this specific use-case: github.com/sleeyax/templatex-go .
