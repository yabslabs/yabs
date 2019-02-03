# Provider

The `provider` defines all specific information for a certain source, for example.

## metadata

The metdata field is constructed in the same way as it is with `kubernetes`.
Under normal usage minimaly need a `name` and a `namespace` (enviroment).
If no `namespace` is set we default to `default`.

## spec

With the `github.com` provider we need to define two values, the `GIT_ACCESS_TOKEN` and `GIT_USERNAME`.
See below for a example.

```yaml
apiVersion: alpha/v1
kind: Provider
metadata:
  name: github.com
  namespace: staging
spec:
  image: yabslabs/provider/github.com
  env:
    - name: GIT_ACCESS_TOKEN
      value: {someAcccessToken}
    - name: GIT_USERNAME
      value: {someUsername}
```