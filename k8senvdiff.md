# K8sEnvDiff

There is a common scenario when working with distributed systems on the Kubernetes platform where resources need to be deployed with aligned container image versions and configurations. From source code versions and Git commit hashes to ConfigMaps and network configurations, these elements are often prone to configuration drift. This is especially true when environments undergo various test scenarios, creating contention between maintaining the Kubernetes environment in a particular state to test new features and performing regression tests to build confidence before releases. This has led to increased interest in Kubernetes configuration management—both to reason about system behaviour, performance, and correctness, and out of curiosity for network visualisation.

While there are existing tools for managing Kubernetes in an ad-hoc manner—Lens and K9s, for instance—even with Lens' recent updates introducing workspaces and plugin support, I feel the core offering falls short. Specifically, it lacks robust functionality for comparing resources both within a single cluster and across multiple clusters.

I propose the need for a tool, at its most basic level, to perform diffs between environments to ensure parity. The tools for this more specific scenario seem to be coming up short.

Several tools exist for local Kubernetes testing, including:

* [Tilt](https://tilt.dev/)
* [Garden](https://garden.io/)
* [Telepresence](https://telepresence.io/)
* [DevSpace](https://www.devspace.sh/)

#### Next Steps:

* Conduct further research into Kubernetes configuration parity tools.
* Develop a proof of concept (PoC) for addressing this gap.
