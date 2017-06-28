# Mesosphere’s DC/OS – A Powerful Orchestrator

There are a variety of orchestrators available to manage containerized workloads. DC/OS has some distinct capabilities that set it apart from other orchestrators. One of the capabilities is to easily deploy well-known software applications and frameworks into a DC/OS cluster. 

# Universe Packages

The Universe is a DC/OS package repository that contains services like Spark, Cassandra, Jenkins, and many others. It allows users to install these services with a single click from the DC/OS UI or by a simple DC/OS package install package name command from the DC/OS CLI. Universe Packages give companies across industries a broad toolset to accelerate time to market and the ability to run modern data-driven applications reliably.

 
- **There Are Several Ways To Deploy Your Service Into DC/OS** - (1) use DC/OS marathon command in CLI; (2) use Marathon REST API directly; (3) deploy your service as a package. Using package approach makes your solution consistent with the environment and gives other benefits.
- **Mesosphere DC/OS Universe** – The main value proposition of Universe packages is that they make it effortless to deploy popular and powerful OSS on a DC/OS cluster. 
- **Curated Software** – The beauty of these packages is that they have been curated by Mesosphere, who has taken the time to leverage best practices for a particular software package, as well as thinking about how it can interoperate in the context of a DC/OS cluster.

The Complete List You can find a complete list here: http://universe.DC/OS.io/#/packages, as well as **Appendix A**.

# Partner SDKs

Mesosphere also provides a Partner SDK, allowing partners to easily integrate their technologies with DC/OS. It includes a complete SRE (site reliability engineering) best practices implemented in code. Entire data services ecosystems — such as distributed databases, message queues, caches and analytics technologies — can quickly be integrated with DC/OS. These services can then be installed in seconds for fast and reliable implementations. The packages include proven DC/OS capabilities like automatic failure detection and recovery.	

The DC/OS Universe service catalog includes:

- **Alluxio** for high-speed distributed storage access .
- **Couchbase** high-performance and scalable NoSQL database .
- **DataStax Enterprise**, built on the Apache Cassandra distributed database .
- **Elastic Stack** (Elasticsearch, Logstash, Kibana) for analytics and data insights .
- **Redis** in-memory data structure store for high-performance analytics use cases.

# What a package provides

Universe Packages dramatically simplify what otherwise be a complex installation deployment in a cluster. 

- **Installation Notes** - To begin, they provide preInstallNotes, which gives the user information they’ll need before starting the installation process. For example, you could explain what the resource requirements are for the service, such as "Unicorns take 7 nodes with 1 core each and 1TB of ram." There are also postInstallNotes.
- **Log Management** - Logs and metrics typically come from several places, making it hard to troubleshoot and isolate problems. DC/OS gives operators a comprehensive view into the health of the application and cluster. The logs and metrics can be easily integrated into existing monitoring tools (e.g., Spunk, ELK, Datadog, Prometheus or custom-developed monitoring tools).
- **Security And Compliance** - Are key concerns for enterprises, especially in the context of new technologies such as Docker containers. DC/OS can lower risk by controlling access to applications and services. In addition, it is possible for operators to determine which users have access to debugging and associated apps while limiting access to the underlying infrastructure. In addition, Mesosphere DC/OS has been independently audited for compliance with NIST, ISO, FISMA, OSC and HIPPA certifications.
- **Built In GPU Support** - Gpu-based scheduling on DC/OS means that GPU-enabled hardware can be pooled with the rest of the infrastructure for highest overall utilization, but also be reserved for machine-learning workloads for maximum performance. With GPU acceleration, neural net training can be 10-20 faster than with CPUs. DC/OS now allows you to isolate and reserve GPU resources for the workloads that need them, but also pool these GPU-enabled resources with the rest of the infrastructure for higher overall utilization.

# Universe Package Examples

To drive this point home, imagine the steps needed to deploy some of the better known packages.

- **Cassandra** – Like many software packages it is necessary to first install Java 8. Of course, the Universe Package takes care of this. In addition, setting up the path, running Cassandra as a service, checking the status of Cassandra to verify uptime and health. Setting up the seeds (list of IP addresses), indicating the storage port, the listen address and the transport port are all tasks that need to be setup.
- **Jenkins** – Run your continuous integration, automated testing, and continuous delivery jobs for workloads in a DC/OS cluster. If you were to deploy Jenkins by hand, a significant amount of know how is required. For example, you would need to manually pre-configure autoscale build agents, making it possible for DC/OS to create and destroy agents as demand increases and decreases. You would also need to leverage Nginx as a reverse proxy that rewrites the URIs into the absolute paths that Jenkins requires. More complex work involves setting up Canary deployments, which is a pattern for rolling out releases to a subset of DC/OS nodes, allowing you to test your deployment on a small set of nodes before releasing more widely to production. Finally, the Job DSL plugin allows for jobs to be scripted and templated, allowing entire pipelines to be defined within code rather than manually.

# Data Workloads / Stateful Apps / Tasks on VMs

DC/OS offers powerful support for important workloads. First, is significant support for Data workloads, much of it described above. Second, support for stateful applications is made possible through local persistent volumes, protecting applications from data loss during restarts. The resources the application requires are also reserved. Marathon will implicitly reserve an appropriate amount of disk space (as declared in the volume via persistent.size) in addition to the sandbox disk size you specify as part of your application definition.

# Appendix A - The complete list of Universe Packages

