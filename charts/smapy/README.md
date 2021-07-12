This chart installs [SMApy](https://github.com/jonkerj/smapy) on your k8s
cluster using Helm. You'll need to provision just a couple of things:

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | misc  | environment, specified as KEY: VALUE |
| envSecret | string | smapy-secrets | secret to load environment from |
