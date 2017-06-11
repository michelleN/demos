This directory contains resources to show off the inner loop concept with Helm, Draft, and Jenkins.
The inner loop in this context is defined as follows:
1. Code to Commit with Draft
Draft allows a developer to test out their application in Kubernetes. It also creates a Dockerfile and a Helm chart that a developer can throw over the fence for the next phase of the inner loop.
2. Commit to Artifact
Helm is a package manager for Kubernetes. Once a developer commits their code, including the Helm chart and Dockerfile, artifacts are available to whomever has access to that repository. However, in a more proper scenario, there might be a CI process that 1. tags and builds and pushes the image to a registry and 2. packages the helm chart and pushes it to a chart repository.
3. Artifact to deploy with Jenkins
The last piece of the puzzle is deploying the artifact into a deployment environment. For this is example, we'll use Jenkins to deploy the helm chart in the
