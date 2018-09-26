{% assign packages = site.data.packages | sort:'name' %}
{% for package in packages %}
## {{ package.name }}

> {{ package.slogan }}

{% if package.home %}
**Homepage**: <{{ package.home }}>
{% endif %}
{% if package.repo %}
**Repository**: <{{ package.repo }}>
{% endif %}

{% if package.authors %}
###### Authors
{% for author in package.authors %}
- [{{ author.name }}]({{ author.home | default:'#' }})
{% endfor %}
{% endif %}

{% if package.notes %}
###### Notes
{{ package.notes }}
{% endif %}

{% endfor %}
