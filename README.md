
##### INSTALLATION

    helm repo add bitnami https://charts.bitnami.com/bitnami


##### Create databases

    NAME=app && DB_ENV=dev && helm install database-$NAME-$DB_ENV bitnami/postgresql --namespace databases --create-namespace --set global.postgresql.auth.database=$NAME-$DB_ENV,global.postgresql.auth.username=$NAME-$DB_ENV
