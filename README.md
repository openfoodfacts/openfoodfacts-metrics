# openfoodfacts-metrics

This repository is here to coordinate the metrics and dashboard that can be collected / displayed around the Open Food Facts projects
<img style="width: 300px" source="https://github.com/user-attachments/assets/4a70c5cb-bce0-4b07-93ad-1bb2ba457995"></img>


## How to contribute

There are different ways to contribute:
* propose a discussion around a metric we should capture, why and how
* pick an issue and try to find a technical solution to it
* create dashboards using [superset](https://sql.openfoodfacts.org) to help gain 

## Tools

* https://sql.openfoodfacts.org offers a superset instance currently fed with some data sources:
  see [the documentation](https://sql.openfoodfacts.org/superset/dashboard/20/) and [the wiki page](https://wiki.openfoodfacts.org/Superset)

  This is a tool to use in priority because it have it's own data replication which do not impact the website / app.
  * It has a replication of openfoodfacts-query database which is used to get facets (so you can re-create all corresponding insights, and more)
  and all products modifications events.
  * It also have the daily duckdb import, duckdb is very good at making aggregations (column oriented database)
  
* https://mirabelle.openfoodfacts.org/ is used by data quality and has some display capability, but superset should be preferred for new work
* We have a matomo instance that monitor the websites and mobile apps https://analytics.openfoodfacts.org/ we may give access if you need to (it is GDPR compliant)

We have a grafana instance that was collecting metrics, but it's currently not really reliable (robotoff is pushing data to it, but we should use openfoodfacts-exports for that)
* https://metrics.openfoodfacts.org (Based on Grafana)

* See also: https://wiki.openfoodfacts.org/Metrics

### Related
We also have tools, that are less in the scope of this repository, but can be useful:

* [Facets on the servers](https://wiki.openfoodfacts.org/Holistic_product_view) are an interesting way of visualizing data, but beware that it might be slow and subject to rate limits
* [Advanced search](https://world.openfoodfacts.org/cgi/search.pl) is yet another tool but also don't work if you have a lot of data to display
* Future deployment of [search-a-licious](https://github.com/openfoodfacts/search-a-licious) should also (thanks to [explorer interface](https://github.com/openfoodfacts/openfoodfacts-explorer/)) is a promising future tool to use for instant visualization


