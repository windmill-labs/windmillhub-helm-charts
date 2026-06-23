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
  imageName: ghcr.io/windmill-labs/windmillhub-ee-public:main
  appUrl: https://app.mywindmill.dev
  imageName: ghcr.io/windmill-labs/windmillhub-ee-public:main
  sslIngress: true
  certArn: arn:aws:acm:us-east-1::myarn
  licenseKey: "LICENSE_KEY"
  # Optional: notify a GitHub content repo on script create/approve (drives its review-PR sync)
  githubDispatchRepo: "owner/content-repo"
  githubDispatchToken: "github_pat_..." # or use githubDispatchTokenSecret below
  githubDispatchTokenSecret:
    name: hub-github-dispatch
    key: token
  extraEnv: []
  affinity: {}
```
