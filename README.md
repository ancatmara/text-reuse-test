## Tracer

### System requirements

* Any OS (Windows/OS X/Linux)
* Java 8 — not higher!
* Apache Ant (a build tool)

**NB!** Only use `ant` command when compiling Tracer, any flags (like `verbose`) will later result in *“Unable to access jarfile”* error. 

### Download & compilation

`git clone http://vcs.etrap.eu/tracer-framework/tracer.git`

`cd tracer`

`ant`

### Running

`java -Xmx600m -Deu.etrap.medusa.config.ClassConfig=conf/tracer_config.xml -jar tracer.jar > FILENAME.OUT`

* Your data must be a single `.txt` file in `tracer/data/corpora/*some-folder*`
* Check and update `tracer/conf/tracer_config.xml` before running

### Manual

* [Download & installation](https://gfranzini.gitbooks.io/tracer/content/manual/download-and-installation.html)
* [Troubleshooting](https://gfranzini.gitbooks.io/tracer/content/support/troubleshooting/)
* [Data format](https://gfranzini.gitbooks.io/tracer/content/manual/corpus-preparation.html)
* [Configuration](https://gfranzini.gitbooks.io/tracer/content/manual/configuration/)

## Passim

### Requirements

* Java 8 — not higher!
* Scala
* Sbt ( a build tool for JVM languages)
* Apache Spark
  * Comes with Java 11
  * Depends on Hadoop, which has native libraries that aren't supported in OS X → won’t run on a Mac

**NB!** Build Passim with `sbt` before installing Apache Spark. Spark comes with Java 11, which results in build conflicts when you are compiling Passim with `sbt`.

### Download & compilation

`git clone https://github.com/dasmiq/passim.git`

`cd passim`

`build/sbt package`

This should produce a runnable .jar in `target/scala_*/passim*.jar`.

### Running

`passim "{input.json,directory-of-json-files,some*.json.bz2}" output`

### Docs
[GitHub repo](https://github.com/dasmiq/passim)
