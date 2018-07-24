---
layout: default
---

{{ site.data.people.pi.name }}'s image reconstruction research group at <br/>
King's College London, St Thomas' Hospital, London SE1&nbsp;7EH, UK

![](images/group.jpg)

# People

- [![{{ site.data.people.pi.name }}][{{ site.data.people.pi.name }}-pure-badge]](#pure-ajr14)

## Post-docs

{% for mem in site.data.people.postdocs %}- [![{{ mem.name }}][{{ mem.name }}-pure-badge]][{{ mem.name}}-pure]{% if mem.github %}
  [![][{{ mem.name }}-github-badge]][{{ mem.name }}-github]{% endif %}
{% endfor %}

## PhD Students

{% for mem in site.data.people.phdstudents %}- [![{{ mem.name }}][{{ mem.name }}-pure-badge]][{{ mem.name}}-pure]
  [![][{{ mem.name }}-cdt-badge]][{{ mem.name }}-cdt]{% if mem.github %}
  [![][{{ mem.name }}-github-badge]][{{ mem.name }}-github]{% endif %}
{% endfor %}

# Downloads

## Projects

- [High-Resolution Heterogeneous Digital Brain Phantom][brain_phantom]

[brain_phantom]: ./brain_phantom/ "downloadable digital brain phantom"

[{{ site.data.people.pi.name }}-pure-badge]: {{ site.data.people.pure.badge.pre }}{{ site.data.people.pi.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.pure.badge.post }}

{% assign members = site.data.people.phdstudents | concat: site.data.people.postdocs %}
{% for mem in members %}
[{{ mem.name }}-pure-badge]: {{ site.data.people.pure.badge.pre }}{{ mem.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.pure.badge.post }}
[{{ mem.name }}-pure]: {{ site.data.people.pure.pre }}{{ mem.pure }}

[{{ mem.name }}-cdt-badge]:  {{ site.data.people.cdt.badge.pre }}{{ mem.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.cdt.badge.post }}
[{{ mem.name }}-cdt]: {{ site.data.people.cdt.pre }}{{ mem.name | downcase | replace: ' ', '-' }}

{% if mem.github %}
[{{ mem.name }}-github-badge]: {{ site.data.people.github.badge.pre }}{{ mem.github }}{{ site.data.people.github.badge.post }}
[{{ mem.name }}-github]: {{ site.data.people.github.pre }}{{ mem.github }}
{% endif %}

{% endfor %}

----

<!--https://codegena.com/generator/iframe-code-generator-->
<div id="pure-ajr14" class="codegena_iframe"><iframe
 src="{{ site.data.people.pure.pre }}{{ site.data.people.pi.pure }}"
 style="background:url('//codegena.com/wp-content/uploads/2015/09/loading.gif') white center center no-repeat;border:0px;"
 height="400" width="600" sandbox=""></iframe></div>
