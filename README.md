# Centiservice/Mats3 JBang Catalog

[JBang](https://jbang.dev) is an open source project that allows developers to instantly run java source code files which may rely on dependencies hosted on Maven Central, by using a special comment notation.

This is Mats3's *JBang Catalog*, which enables a developer to start a "Mats3 optimized" developer ActiveMQ instance as such (featuring the MatsBrokerMonitor for introspection of messages on queues and DLQs, and enables reissuing of DLQ'ed messages)

```shell
jbang activemq@centiservice
```

And when that ActiveMQ instance is running, in another shell start a service consisting of an extremely basic *single-stage Mats3 Endpoint*:
```shell
jbang SimpleService@centiservice@centiservice
```

And then in third shell invoke that service from a main-class:
```shell
jbang SimpleServiceMainFuturization@centiservice
# or
jbang SimpleServiceMainTerminator@centiservice
```

Or a tad more realistic, fire up a Jetty HTTP server so that you can invoke the Endpoint from a browser:
```shell
jbang SimpleServiceHttpServer@centiservice
```

If you want to play with those files, clone down the project at https://github.com/centiservice/mats3-examples, and look in the `jbang` folder.