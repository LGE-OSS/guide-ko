# starter
1. [Generate with the same files and folders](https://github.com/rundocs/starter/generate) from this repository
2. Set up your GitHub Pages to source(/)
3. Now you can view your documentation in your site

## site.pages

| source | link |
| ------ | ---- |
{% for page in site.pages -%}
|{{ page.path }}|[{{ page.url | relative_url }}]({{ page.url | relative_url }})|
{% endfor %}

## Documents
For full documentation, please refer to [rundocs.io](https://rundocs.io/), You can also view [the theme related tests documentation](https://rundocs.github.io/jekyll-rtd-theme)

## Local debug
```
make
make server
```

## License
The theme is available as open source under the terms of the [MIT License](https://github.com/rundocs/jekyll-rtd-theme/blob/master/LICENSE)
