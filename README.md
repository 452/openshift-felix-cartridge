# OpenShift OSGI cartridge

This cartridge embeds the Apache Felix runtime as a base for OSGI based applications on OpenShift.

## How to use

Just create a new gear with this cartridge by issuing

```
rhc create-app <your app name> http://cartreflect-claytondev.rhcloud.com/github/mthmulders/openshift-felix-cartridge
```

## Control

At this time, there is no functionality exposed by default. When you start the cartridge, Felix is started for you, however there is no public facing interface. To control the runtime, you need to SSH inside your gear and manage the environment using the provided telnet server. This allows you to use the [Gogo shell](http://felix.apache.org/site/apache-felix-gogo.html).

```
rhc ssh <your app name>
telnet ${OPENSHIFT_FELIX_IP} 6666
```