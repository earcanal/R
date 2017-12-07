# Using Docker with The Experiment Factory

[The latest docs](https://expfactory.github.io/expfactory/) are a bit "raw"

## What is Docker?

![Docker logo](https://forums.docker.com/uploads/default/original/2X/8/8425fda4f1fa565a5dbf5c5f60cc43a972fd30b9.png)

* [Docker](https://www.docker.com/): applications (e.g. your experiments) as containers
   * Applications are too "granular"
     * Fiddly to configure hosts to cater for every app's requirements and dependencies
   * Virtual machines are too big
   * Hence hosts provide "docks" (the docker application) which is a platform for any shape of container

## The Experiment Factory: a simple container
  * `docker run -v $PWD:/data vanessa/expfactory-builder build test-task state-mindfulness-survey`
  * `Dockerfile`, `startupscript.sh`
  * Same container can be run in the lab (I haven't tried [Docker for Windows](https://docs.docker.com/docker-for-windows/) yet) or online
  * `#docker build --no-cache -t earcanal/study3 .`
  * `docker run -v $PWD/data:/scif/data -d -p 80:80 earcanal/study3 start`
    * Automatic participant-id generated
    * File format is JSON.  Looks a bit scary, but [easy to process with R](https://github.com/earcanal/manjushri/blob/master/R/expfactory.R).
    * Can also write to SQLLite, MySQL, Postgres
      * Data rows are still JSON, but at least everything is in a single file!
  * `docker exec -it ... bash`
  * `docker stop ...`

## 'Headless' online studies coming soon

  * Deploy to your favourite Docker service provider
    * e.g. [Digital Ocean](https://www.digitalocean.com/products/one-click-apps/docker/)
    * Run [headless](https://github.com/expfactory/expfactory/blob/headless/docs/pages/2-usage.md#start-a-headless-experiment-container)
  * `docker run -v $PWD/data:/scif/data -d -p 80:80 earcanal/study3 --experiments test-task,state-mindfulness-survey --database sqlite start`
  * Work in progress: [participant tokens](https://github.com/expfactory/expfactory/issues/39)
