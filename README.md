# dev-spaces-podman-compose-quarkus-superheroes
Demo of using podman-compose in OpenShift Dev Spaces to run the Quarkus Super Heroes Demo

```bash
export API_BASE_URL=https://$(oc get route ${DEVWORKSPACE_ID}-dev-tools-8082-https-fights -o jsonpath={.spec.host})
podman compose -f super-heroes-compose.yaml -f super-heroes-monitoring.yaml up --remove-orphans
```
