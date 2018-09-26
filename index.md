{% for package in site.data.packages %}
## [{{ package.name }}]({{ package.home }})

> {{ package.slogan }}

Home: {{ package.home }}

Repo: {{ package.repo }}

Authors:
{% for author in package.authors %}
- [{{ author.name }}]({{ author.home }})
{% endfor %}

Notes:
{{ package.notes }}

{% endfor %}
