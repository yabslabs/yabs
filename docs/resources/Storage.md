# Storage

## metadata

The metdata field is constructed in the same way as it is with `kubernetes`.
Under normal usage minimaly need a `name`.

## spec

```yaml
apiVersion: alpha/v1
kind: Storage
metadata:
  name: backup
spec:
  - type: s3
    path: https://somes3bucket
    Access_key_ID: {someKeyID}
    Secret_access_key: {someSecret}
```

### Storage Types

fs, s3...