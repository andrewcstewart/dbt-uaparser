# dbt-uaparser

A dbt package with macros for parsing User Agent strings

# Installation instructions

New to dbt packages? Read more about them [here](https://docs.getdbt.com/docs/building-a-dbt-project/package-management/).
1. Include this package in your `packages.yml` file — check [here](https://hub.getdbt.com/dbt-labs/audit_helper/latest/) for the latest version number.
2. Run `dbt deps` to install the package.

# Macros
## create_f_parse_ua_string

This macro will define a UDF that parses UA strings.  First you can use a `run-operation` to create the UDF.

```
dbt run-operation create_f_parse_ua_string
```

Then you can use the UDF within your queries:

```sql
select 
    utils.parse_ua_string(ua_string)
from mydatabase.myschema.mytable
```