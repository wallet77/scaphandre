# About containers

There are several ways scaphandre can interact with containers.

You may run scaphandre **in a container**, to not have to manage the dependencies, then measure the power consumption of the **bare metal host**. This is described in the [quickstart tutorial](../tutorials/quickstart.md). Note that you need to expose `/sys/class/powercap` and `/proc` as volumes in the container to allow scaphandre to get the relevant metrics from the bare metal host.

Scaphandre may help you measure the **power consumption of containers** running on a given host. You can already get to that goal using the tips provided in the howto section called ["Get process level power consumption"](../how-to_guides/get-process-level-power-in-grafana.md). It may still require some tweaking and inventiveness from you in making the approriate queries to your favorite TSDB. This should be made easier by the upcoming [scaphandre features](https://github.com/hubblo-org/scaphandre/projects/1).

Another use case scenario would be to measure the power consumption of a **container orchestrator** (like [kubernetes](https://kubernetes.io/)), its nodes and the containers and applications running on it. This is a feature we are [currently working on](https://github.com/hubblo-org/scaphandre/issues/29#issuecomment-755353175) (you may try yourself the helm chart that is proposed in that thread, before it is officially supported).

As described [here](../compatibility.md), scaphandre provides several ways ([sensors](../explanations/sensors.md)) to collect the power consumption metrics. Depending on your use case a sensor should be more suitable than the other. Each of them comes with strengths and weaknesses. This is basically always a tradeoff between precision and simplicity. This is especially true if you run a container-based workloads on public cloud instances. We are working to provide a solution [for that as well](https://github.com/hubblo-org/scaphandre/issues/25).