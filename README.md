# camel-demos


Organising my camel demos which are scattered over my hard drive, plus unifying them into a consistent set of demos.

You will need to install  [SBT 0.13](http://www.scala-sbt.org/release/docs/Getting-Started/Setup.html)

Example illustrating how to run a project (example uses **most-basic** project)

```bash
$ me@mylinux:camel-demos> sbt
Loading ...
[info] ...
...
> project most-basic
[info] Set current project to most-basic ...
> run
[info] Compiling 2 Scala sources to ...
[info] Running demo.basic.FileDemo
[info] ...
[info] 11:16:46,227 INFO  route1  - received file file1.xml
```

## List of demos

 1. **most-basic**: One of the most basic "Hello World"-type of demos.
 2. **simple-spring**: Similar "Hello World" using Spring
 3. **core-camel**: Similar to **most-basic**, but shows the default single-thread behaviour (tip surround the steps in `threads(5) { ... }`) and includes a unit test.  
 4. **splitter**: Simple demo using xpath based splitter
 5. **aggregator**: Aggregates an XML message. There is also a Java implementation of the same route, just change the Spring configuration to use the Java equivalent
 6. **simple-ftp**: Idempotent ftp consumer
 7. **spring-bean**: Shows the use of the bean component in conjunction with the Spring Registry (demo uses a unit test)
 8. **seda-inout**: Shows an netty:tcp endpoint connecting to a seda endpoint inout (for the client open a telnet session: `telnet localhost 7090`)
 9. **jetty-http**: Simple http endpoint, use for example curl to send data:
 ```bash
 me@my-linux> curl -H "Content-Type: text/plain" --data "hello"  http://localhost:9090/myapp/myservice
 ```
 10. **pipeline-processors-inout**: Illustrates the behaviour of setting the `in` or `out` bodies on pipeline processors (only contains a "unit test")
 11. **simple-jms**: Uses invm JMS (also shows CBR to route xml and csv files)
 12. **spring-jms** Illustrates comfiguration of JMS in Spring
 13. **parallelMulticast**: Illustrated (parallel) multicast. A Java version is also included
 14. **osgi-spring**. This demo has its own  ([readme](osgi-spring/readme.md))











