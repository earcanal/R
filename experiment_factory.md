# The Experiment Factory: An overview

[The Experiment Factory](https://expfactory.github.io/expfactory/) is an open software framework which aims to address the technological barriers to replication in psychology and behavioural science.  This talk will demonstrate how the framework can be used to rapidly create and deploy a study in the lab and online.  

  1. Avoid programming altogether by creating a study from [freely available experimental tasks, surveys and games](https://expfactory.github.io/experiments/)
  1. Use jsPsych to develop your own experiments and surveys that run in a browser. (This is relatively easy if you have experience with ePrime, PsychoPy, OpenSesame etc.)
  1. Deploy your study locally or online using Docker, with data written to files or a database

## The technical replication problem

1. No code sharing, **Procedure** section should be executable 
1. Same study, different code (different bugs!)
1. Unreliable code == unreliable data
  * Everybody writes tests, right?!

## Solutions

* Open Science (software, data)
  * Experiment development tools: PsychoPy, OpenSesame, Psychtoolbox, **jsPsych**
  * Collaboration: [git(hub)](http://github.com/)

# The 'experiment' library (and ontology) 

Github repositories containing [experiments](https://expfactory-experiments.github.io/stroop), [surveys](https://expfactory-experiments.github.io/state-mindfulness-survey), and [games](https://expfactory-experiments.github.io/bucket-game/)
  * Can be run stand-alone or via a web server
    * `git clone git@github.com:expfactory-experiments/test-task.git`
    * `python3 -m http.server`
    
## Bespoke experiments and surveys

* Surveys are simply [TSVs](https://github.com/expfactory-experiments/state-mindfulness-survey)
* Experiments are anything you can do with HTML, CSS and JavaScript, but easiest using [jsPsych](jspsych.md)

# Packaging a study

* [Docker](docker.md)

# A good solution?

* **Productivity**
  * Low bar to producing new tasks
* **Quality control**
  * Continuous integration testing
  * [Acceptance Testing](https://en.wikipedia.org/wiki/Acceptance_testing) with [Selenium](http://www.seleniumhq.org/)
* **Distribution**
  * Containers are simple to distribute and can contain anything e.g. PsychoPy, OpenSesame, Psychtoolbox, ePrime?!

## References

Sochat, V. V., Eisenberg, I. W., Enkavi, A. Z., Li, J., Bissett, P. G., & Poldrack, R. A. (2016). The Experiment Factory: Standardizing Behavioral Experiments. Frontiers in Psychology, 7. https://doi.org/10.3389/fpsyg.2016.00610

*Whilst the objectives in this paper remain the same, this is a fast-moving project and many of the technical elements have been superceeded by [the latest version of the software](https://expfactory.github.io/expfactory/).*
