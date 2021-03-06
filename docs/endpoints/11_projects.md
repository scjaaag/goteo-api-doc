---
layout: default
title: Projects
group: endpoint
permalink: /doc/projects.html
---
# Projects endpoint

This section gives you information about projects in [Goteo.org](http://goteo.org)

<a name="projects"></a>
## /projects/

Obtains a list of projects.

```bash
curl -i --basic --user "user:key" {{ site.apiurl }}/projects/
```

### Filters available:

**The [standard set of filters](filters.html) applies to this endpoint with these particulars:**

{{ site.data.projects.parameters_table }}

### Response values:

{{ site.data.projects.definitions_table }}

### Response body:

```json
{{ site.data.projects.example }}
```


<a name="project"></a>
## /projects/{PROJECT_ID}

Gets information about a single project.

```bash
curl -i --basic --user "user:key" {{ site.apiurl }}/projects/llevamealhuerto
```

### Filters available:

* No filters are available in this endpoint
* **{PROJECT_ID}** must be the unique identifier of the project

### Response values:

{{ site.data.project.definitions_table }}

### Response body:

```json
{{ site.data.project.example }}
```

<a name="project"></a>
## /projects/{PROJECT_ID}/donors/

Lists all donors in a project

```bash
curl -i --basic --user "user:key" {{ site.apiurl }}/projects/llevamealhuerto/donors/
```

* **{PROJECT_ID}** must be the unique identifier of the project

### Filters available:

**Some of the [standard set of filters]({{ "doc/filters.html" | prepend: site.baseurl }}) can be applied here:**

{{ site.data.project_donors.parameters_table }}

### Response values:

{{ site.data.project_donors.definitions_table }}

### Response body:

```json
{{ site.data.project_donors.example }}
```
