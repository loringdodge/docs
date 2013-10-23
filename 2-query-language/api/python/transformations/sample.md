---
layout: api-command 
language: Python
permalink: api/python/sample/
command: sample 
github_doc: https://github.com/rethinkdb/docs/edit/master/2-query-language/api/python/transformations/sample.md
---

{% apibody %}
sequence.sample(number) → selection
stream.sample(number) → array
array.sample(number) → array
{% endapibody %}

Select a given number of elements from a sequence with uniform random distribution. Selection is done without replacement.

__Example:__ Select 3 random heroes.

```py
r.table('marvel').sample(3).run(conn)
```