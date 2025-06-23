# Windmill Hub Helm Chart

This is the Helm chart for the Windmill Hub.

For the Windmill helm chart, see
[windmill-helm-charts](https://github.com/windmill-labs/windmill-helm-charts).

## Usage

```bash
helm repo add windmill-labs https://windmill-labs.github.io/windmillhub-helm-charts/
helm repo update
```

Example values.yaml:

```yaml
hub:
  databaseUrl: postgres://username:password@host:port/database
  baseUrl: https://hub.windmill.dev/
  imageName: ghcr.io/windmill-labs/windmillhub-ee-public:main
  sslIngress: true
  certArn: arn:aws:acm:us-east-1::myarn
  affinity: {}
```
