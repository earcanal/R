# Using Docker with The Experiment Factory

[The latest docs](https://expfactory.github.io/expfactory/) are a bit "raw"

## What is Docker?

* [Docker](https://www.docker.com/): applications (e.g. your experiments) as containers
   * Applications are too "granular"
     * Hosts ("docks") can't cater for every app's requirements and dependencies
   * Virtual machines are too big
   * Hence containers
* I haven't tried [Docker for Windows](https://docs.docker.com/docker-for-windows/) yet

## Data

* Automatic participant-id generated
* File format is JSON.  Looks a bit scary, but [easy to process with R](https://github.com/earcanal/manjushri/blob/master/R/expfactory.R).
* Can also write to SQLLite, MySQL, Postgres
  * Still JSON, but at least everything is in a single file :)
