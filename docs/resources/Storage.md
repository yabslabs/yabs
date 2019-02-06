# Storage

## metadata

The metdata field is constructed in the same way as it is with `kubernetes`.
Under normal usage minimaly need a `name`.

## spec

```yaml
apiVersion: alpha/v1
kind: Storage
metadata:
  name: github.com storage
spec:
  - name: Cache
    type: fs
    path: cache/
  - name: Backup
    type: s3
    path: https://somes3bucket
    Access_key_ID: {someKeyID}
    Secret_access_key: {someSecret}
  - name: Archive
    type: s3
    path: https://somes3bucket
    Access_key_ID: {someKeyID}
    Secret_access_key: {someSecret} 
```

### Storage Types

fs, s3...