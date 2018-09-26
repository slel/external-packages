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
{% if author.home %}
- [{{ author.name }}]({{ author.home | default:'#' }})
{% else %}
- {{ author.name }}
{% endif %}
{% endfor %}
{% endif %}

{% if package.notes %}
###### Notes
{{ package.notes }}
{% endif %}

{% endfor %}
