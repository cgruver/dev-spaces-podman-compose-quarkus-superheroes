# dev-spaces-podman-compose-quarkus-superheroes
Demo of using podman-compose in OpenShift Dev Spaces to run the Quarkus Super Heroes Demo

```bash
export API_BASE_URL=https://$(oc get route ${DEVWORKSPACE_ID}-${DEVWORKSPACE_COMPONENT_NAME}-${FIGHTS_SERVICE_PORT}-https-ui -o jsonpath={.spec.host})
podman compose -f deploy/docker-compose/java17.yml -f deploy/docker-compose/monitoring.yml up --remove-orphans
```
