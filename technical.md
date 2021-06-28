# HuBMAP Technical Documentation

<details>
<summary>HIVE Software Engineering Principles</summary>

-   Our software development teams use a multi-institutional Agile Scrum approach to create HuBMAP technologies deployed using [microservices in a hybrid cloud](https://portal.hubmapconsortium.org/docs/infrastructure). We run daily distributed stand-ups and two week sprint cycles. This enables continuous new deployments of features and enhancements under permissive open source licenses.
    
-   The HuBMAP Portal principally utilizes the following core technologies, frameworks, and languages: Globus (identity federation, data flow), Python (APIs), Javascript (UI), Neo4j (graph databases), Docker (container per micro service), and Airflow (workflows), among others. Core storage and other high performance services run locally at Pittsburgh Supercomputing Center whereas high availability services run on Amazon Web Services.
    
-   Software issues, enhancement, and feature requests are tracked using a [GitHub issues board](https://github.com/hubmapconsortium/portal-ui/issues) that is populated directly by developers and by user feedback via the help desk.
    
-   HuBMAP technology documentation resides in the [Portal documentation area](https://portal.hubmapconsortium.org/docs) as well as within [HuBMAP GitHub repositories](https://github.com/hubmapconsortium/). Other locations include our [API](https://portal.hubmapconsortium.org/docs/apis) viewable on [SmartAPI](https://smart-api.info/ui/0065e419668f3336a40d1f5ab89c6ba3). We manage our [documentation using markdown](https://github.com/hubmapconsortium/portal-docs).
    
-   HuBMAP technologies use a [microservices architecture](https://portal.hubmapconsortium.org/docs/infrastructure) and is driven by the [API Gateway](https://github.com/hubmapconsortium/gateway#readme), [Provenance services](https://github.com/hubmapconsortium/entity-api#readme), and Pipeline Container Orchestration.
    
We maintain dev, test, and production instances of most HuBMAP systems. In some areas we use continuous integration with [Travis CI](https://travis-ci.org/) or [GitHub CI](https://docs.github.com/en/actions/guides/about-continuous-integration).
</details>

<details>
<summary>HuBMAP Data Ingest</summary>
