---
layout: default
---

{{ site.data.people.pi.name }}'s image reconstruction research group at <br/>
King's College London, St Thomas' Hospital, London SE1&nbsp;7EH, UK

![](images/group.jpg)

# People

- [![{{ site.data.people.pi.name }}][{{ site.data.people.pi.name }}-pure-badge]](#pure-ajr14)

## Post-docs

{% for mem in site.data.people.postdocs %}- {% if mem.pure %}
  [![{{ mem.name }}][{{ mem.name }}-pure-badge]][{{ mem.name}}-pure]{% endif %}{% if mem.rg %}
  [![{{ mem.name }}][{{ mem.name }}-rg-badge]][{{ mem.name}}-rg]{% endif %}{% if mem.github %}
  [![][{{ mem.name }}-github-badge]][{{ mem.name }}-github]{% endif %}{% if mem.left %}
  ![][{{ mem.name }}-left-badge]{% endif %}
{% endfor %}

## PhD Students

{% for mem in site.data.people.phdstudents %}- [![{{ mem.name }}][{{ mem.name }}-pure-badge]][{{ mem.name}}-pure]
  [![][{{ mem.name }}-cdt-badge]][{{ mem.name }}-cdt]{% if mem.rg %}
  [![{{ mem.name }}][{{ mem.name }}-rg-badge]][{{ mem.name}}-rg]{% endif %}{% if mem.github %}
  [![][{{ mem.name }}-github-badge]][{{ mem.name }}-github]{% endif %}{% if mem.left %}
  ![][{{ mem.name }}-left-badge]{% endif %}
{% endfor %}

# Downloads

## Projects

- [High-Resolution Heterogeneous Digital Brain Phantom][brain_phantom]
- [The NURBS-based HUman Brain (NHUB) Phantom][nhub]

[brain_phantom]: ./brain_phantom/ "downloadable digital brain phantom"
[nhub]: https://github.com/casperdcl/brain_phantom "Source code"

## Misc

- [*Multi-modal weighted quadratic priors for robust synergistic PET-MR reconstruction*, PSMR 2018](https://www.youtube.com/watch?v=cbuncWC6oKc)

[{{ site.data.people.pi.name }}-pure-badge]: {{ site.data.people.pure.badge.pre }}{{ site.data.people.pi.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.pure.badge.post }}

{% assign members = site.data.people.phdstudents | concat: site.data.people.postdocs %}
{% for mem in members %}

{% if mem.pure %}
[{{ mem.name }}-pure-badge]: {{ site.data.people.pure.badge.pre }}{{ mem.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.pure.badge.post }}
[{{ mem.name }}-pure]: {{ site.data.people.pure.pre }}{{ mem.pure }}
{% endif %}

[{{ mem.name }}-cdt-badge]:  {{ site.data.people.cdt.badge.pre }}{{ mem.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.cdt.badge.post }}
[{{ mem.name }}-cdt]: {{ site.data.people.cdt.pre }}{{ mem.name | downcase | replace: ' ', '-' }}

{% if mem.github %}
[{{ mem.name }}-github-badge]: {{ site.data.people.github.badge.pre }}{{ mem.github | replace: '-', '--' }}{{ site.data.people.github.badge.post }}
[{{ mem.name }}-github]: {{ site.data.people.github.pre }}{{ mem.github }}
{% endif %}

{% if mem.rg %}
[{{ mem.name }}-rg-badge]: {{ site.data.people.rg.badge.pre }}{{ mem.name | replace: ' ', '_' | replace: '-', '--' }}{{ site.data.people.rg.badge.post }}
[{{ mem.name }}-rg]: {{ site.data.people.rg.pre }}{{ mem.rg }}
{% endif %}

{% if mem.left %}
[{{ mem.name }}-left-badge]: {{ site.data.people.left.badge.pre }}{{ mem.left }}{{ site.data.people.left.badge.post }}
{% endif %}

{% endfor %}

----

<!--https://codegena.com/generator/iframe-code-generator-->
<div id="pure-ajr14" class="codegena_iframe"><iframe
 src="{{ site.data.people.pure.pre }}{{ site.data.people.pi.pure }}"
 style="background:url('//codegena.com/wp-content/uploads/2015/09/loading.gif') white center center no-repeat;border:0px;"
 height="400" width="600" sandbox=""></iframe></div>
