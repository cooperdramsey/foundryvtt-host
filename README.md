# foundryvtt-host

To update the foundry version, you need to create a new docker image using the latest license url download. Then push that image to docker hub.

To run correctly:
- Create an app service in Azure of B1 tier
- Specify docker compose as the deployment method, and provide the compose file from this repo.
- Once deployed, set the configuration variable WEBSITES_ENABLE_APP_SERVICE_STORAGE = true
- Setup the path mapping to an Azure File Share. Map to the location '/data' on the App Service. Name the mapping 'fvttbackend'
