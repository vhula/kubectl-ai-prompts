# kubectl-ai-prompts

## Installation of kubectl-ai

```bash
git clone https://github.com/sozercan/kubectl-ai.git && \
cd kubectl-ai && \
go install
```

Please, ensure that ```$GOPATH/bin``` is in your path.

## Configuration

```bash
export OPENAI_API_KEY=<your OpenAI key>
```

## Usage of kubectl ai

```bash
kubectl ai ...
```

## Examples of prompts

|   Name   |  Prompt   |  Description   |  Example   |
-----------|:---------:|:--------------:|:----------:|
| app.yaml         | ```kubectl ai "Create deployment with container with image gcr.io/k8s-k3s/demo:v1.0.0. Add labels app=demo and run=demo. The name is app. Port is 80 with the name http"```          |                | [app.yaml](yaml/app.yaml)           |
| app-cronjob.yaml         |  ```kubectl ai 'Create a CronJob'```         |                |  [app-cronjob.yaml](yaml/app-cronjob.yaml)          |
| app-job.yaml         |  ```kubectl ai 'Create a Job'```         |                |  [app-job.yaml](yaml/app-job.yaml)          |
| app-livenessProbe.yaml         |  ```kubectl ai 'Create a Pod with liveness probe on port 8080'```         |                |  [app-livenessProbe.yaml](yaml/app-livenessProbe.yaml)          |
| app-readinessProbe.yaml         |  ```kubectl ai 'Create a Pod with readiness probe on port 8080 and path /ready'```         |                |  [app-readinessProbe.yaml](yaml/app-readinessProbe.yaml)          |
| app-volumeMounts.yaml         |  ```kubectl ai 'Create a Pod with readiness probe on port 8080 and path /ready, liveness probe and volume mount with name data and path /data'```         |                |  [app-volumeMounts.yaml](yaml/app-volumeMounts.yaml)          |
| app-multicontainer.yaml         |  ```kubectl ai "create a deployment with two containers: nginx and debian"```         |                |  [app-multicontainer.yaml](yaml/app-multicontainer.yaml)          |
| app-resources.yaml         |  ```kubectl ai "create a pod with resources limits and requests"```         |                |  [app-resources.yaml](yaml/app-resources.yaml)          |
| app-secret-env.yaml         |  ```kubectl ai "create a pod with secret username and secret password"```         |                |  [app-secret-env.yaml](yaml/app-secret-env.yaml)          |