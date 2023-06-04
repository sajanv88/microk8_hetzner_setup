# Microk8 setup

This is a simple microk8 hassle free setup that could be used in any cloud server.

## Folder
- You will see the essential yaml in the deployments folder.  
    - cert-manager.production.yaml => will takecare of the ssl certification for your production environment
    - cert-manager.staging.yaml => will be used of staging env (Optional)
    - sample-app.yaml => just use to verify that everything you have configured works fine. 
    - postgresdb.yaml => will create a postgres database. 


Note: For `postgres` database the sensitive informations are all injected via `envsubst` 
For example: `envsubst < deployments/postgresdb.yaml| kubectl apply -f -`
