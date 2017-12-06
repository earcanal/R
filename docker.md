# Using Docker with The Experiment Factory

[The latest docs](https://expfactory.github.io/expfactory/) are a bit "raw"

## What is Docker?

* [Docker](https://www.docker.com/): applications (e.g. your experiments) as containers
   * Applications are too "granular"
     * Hosts ("docks") can't cater for every app's requirements and dependencies
   * Virtual machines are too big
   * Hence containers
* The Experiment Factory is a very simple container
  * `Dockerfile`, `startupscript.sh`
  * Same container can be run in the lab (I haven't tried [Docker for Windows](https://docs.docker.com/docker-for-windows/) yet) or online
  * `docker build --no-cache -t earcanal/study3 .`
  * `docker run -v $PWD/data:/scif/data -d -p 80:80 earcanal/study3 start`
  * `docker exec -it ...`
  * `docker stop ...`
  * `docker run -v $PWD/data:/scif/data -d -p 80:80 earcanal/study3 --experiments test-task,state-mindfulness-survey --database sqlite start`

## Data

* Automatic participant-id generated
* File format is JSON.  Looks a bit scary, but [easy to process with R](https://github.com/earcanal/manjushri/blob/master/R/expfactory.R).
* Can also write to SQLLite, MySQL, Postgres
  * Still JSON, but at least everything is in a single file :)
