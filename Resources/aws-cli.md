# aws-cli commands
## Install
* [MAC]()


## Secrets
```
# For getting a secret key from secret manager
SECRET_ID = <secret> # Insert the name of the secret key

aws secretsmanager get-secret-value \
    --secret-id SECRET_ID 

```

