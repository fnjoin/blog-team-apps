# team-apps 

A spring-boot application that lists deployment running in k8s cluster using Kubernetes Java Client

### Build Pre-requisites

- JDK 11
- `kubectl`

### Running Pre-requisites

- Access to a Kubernetes cluster
- A namespace with some running deployments (`dev` by default)
- The `team` and `app` labels assigned to all deployments that you want returned

### Building/Running the app

```
./gradlew bootRun
```

If you want to run the asynchronous version of the app, use the `async` spring profile:

```
SPRING_PROFILES_ACTIVE=async ./gradlew bootRun
```

If you want to target a Kubernetes namespace other than `dev`, use the `NAMESPACE` environment variable:

```
NAMESPACE=other-ns ./gradlew bootRun
```
