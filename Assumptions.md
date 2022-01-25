## The Assumptions

arhictectures described on this project where designed based on a few assumptions:

### Assumption1 - The described API's are stored in an "unknown" location

     so they have been delegated to a Broker (Apache Kafka should be a good choice, considering escalation capabilities)


### Assumption2 - Kubernetes could be a good choice

    Kubernetes or swarm are usually the tools used to orchestrate containerization. Assuming that we want scalability in our calls, we should have a Kubernetes managing containers in which instances of the "Customer Servicer" application will run

### Assumption3 - We can only work with what we currently have

    We assume that we won't deploy any advanced model in the near future, and we can only use the API's that were made available to us, along with a "dumb" AI model, that is, just a common workflow, where common  subjects can be dealt with but complex requisitions must be answered with simple answers. Anything more complex than retrieving information will be escalated to an "agent"

### Assumption4 - Non persistent database

    As all the data mentioned in the example is considered to be sensitive. I'm assuming they won't be further stored, so they will not persist and thus are session related only. Because of that I believe they would be better contained within the container themselves, but it may be that that they are in a GCP or something similar, stored using a SQL system, so this will be left unsolved in the current proposal
