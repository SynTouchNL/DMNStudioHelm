
# Introduction
Chart made by SynTouch. 
For any changes to the chart, please contact Jan Brekelmans.

# Publishing chart
TODO: Move to pipeline (Something like https://gist.github.com/joaomlneto/b3970c9f022f231c2bbf644a780ebe12)
For now:
```
helm package .
helm repo index .
git commit ....
```

# Using chart:
helm repo add dmnstudio 'https://raw.githubusercontent.com/SynTouchNL/DMNStudioHelm/main'
helm repo update
helm search repo dmnstudio/dmnstudio

# Configuration
## Prerequisites
- A database for the application (The application is tested with Postgress)
- Keycloak installed with a client configured for dmnstudio (One for frontend and one for backend)
- Operaton instances to deploy

## Secrets
The chart provides functionality for using akv secrets. Use this or ensure the secret for dmnStudio is already in place.
The secret file should contain these secrest:
```
QUARKUS_DATASOURCE_PASSWORD: 
QUARKUS_OIDC_CREDENTIALS_SECRET
QUARKUS_OPENAPI_GENERATOR_OPERATON_REST_API_JSON_AUTH_BASIC_AUTH_PASSWORD
```
