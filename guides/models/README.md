# Models

Amber is independent of your choice of model architectures. We \(Core members\) have built the ORM **Granite**. We also think **Jennifer** built by [Roman Kalnytskyi](https://github.com/imdrasil) is a good option.

When you generate a new amber project, you can specify which model you prefer.

```bash
amber new blog -m crecto --deps
```

We currently support `granite` and `crecto` and default to `granite`.

## Granite

Granite provides a light weight ORM that is focused on taking the results of your query and mapping them to your model. It does not try to shield you from the SQL that lies underneath the mapping. It provides a couple conveniences like `save` and `destroy` for simple INSERT, UPDATE and DELETE statements. It provides `find`, `find_by` and `all` to query the database. It also has basic one-to-many relationships with `belong_to` and `has_many`.

{% page-ref page="granite/" %}

## Jennifer

Jennifer provides an more full featured ORM with a full featured DSL for queries and follows the ActiveRecord pattern found in Rails. If you are looking for a full featured ORM, Jennifer may be your choice of ORM.

{% page-ref page="jennifer/" %}

{% hint style="info" %}
Of course you are not limited to only these options. You may have a need for a high throughput, large dataset, dynamic structured db like **MongoDB** or you need to connect to a microservice or a legacy mainframe. By not being tied to a specific model, we don't limit the possible integrations you may need.
{% endhint %}

