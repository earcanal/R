# jsPsych
  *  Browser as the platform for experiments
  * [jsPsych](http://www.jspsych.org/) is a [JavaScript](https://en.wikipedia.org/wiki/JavaScript) library for developing psychology experiments (using [HTML](https://en.wikipedia.org/wiki/HTML) and [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets))
    * [core library](http://docs.jspsych.org/core_library/overview/)
    * [plugins](http://docs.jspsych.org/plugins/overview/) are also fairly easy to write (if necessary) using an existing plugin as a template


## Creating experiments

  * I usually start by copying something similar from the library, but there's [a tutorial](http://docs.jspsych.org/tutorials/rt-task/) if you want to start from scratch.
  * Here's [an experiment I prepared earlier](https://github.com/expfactory-experiments/breath-counting-task)
  * Your browser is also a development environment (press F12 in Chrome)
    * Stimulus editing (HTML and CSS), debugging, breakpoints ...

## Limitations

* JavaScript adds key presses to an event-processing queue.  Queue processing time depends on the browser, computer speed, and other concurrent operating system tasks. (de Leeuw, 2015)
  
## References

de Leeuw, J. R. (2015). jsPsych: A JavaScript library for creating behavioral experiments in a Web browser. Behavior Research Methods, 47(1), 1–12. https://doi.org/10.3758/s13428-014-0458-y
