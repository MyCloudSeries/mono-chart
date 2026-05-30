# Mono-Chart: One Stop Chart for All Deployments
A Single Helm Template for Deploying Many Application to Kubernetes, instead of using different Helm Charts for different applications.

The only difference are the parameters passed via the values.yaml file or via direct Helm CLI values.

## To Deploy use the following commands

```helm repo add https://mycloudseries.github.io/mono-chart/```

```helm install myapp monochart/mono-chart```

# Variables and Values

| Variables           | Description                                             | Default            |
| ------------------- | ------------------------------------------------------- | ------------------ |
| `service_name`      | Name of the service or application                      | `myapp`            |
| `environment`       | Deployment environment (e.g., `dev`, `staging`, `prod`) | `dev`              |
| `image_tag`         | Docker image tag to deploy                              | `latest`           |
| `replicas`          | Number of application replicas                          | `1`                |
| `memory_limit`      | Memory limit for the main application container         | `400Mi`            |
| `cpu_limit`         | CPU limit for the main application container            | `20m`              |
| `cron_memory_limit` | Memory limit for the cron job container                 | `400Mi`            |
| `cron_cpu_limit`    | CPU limit for the cron job container                    | `20m`              |
| `enable_ingress`    | Whether to enable Kubernetes Ingress resource           | `false`            |
| `enable_secret`     | Whether to create and use Kubernetes Secret             | `false`            |
| `cron`              | Whether to enable cron job deployment                   | `false`            |
| `app_url`           | Application domain or URL                               | `demo.example.com` |
| `health_check_path` | Path for the application's health check endpoint        | `/health`          |
| `imageuri`          | Full Docker image URI to pull from                      | `nimboya/myapp`    |
| `container_port`    | Port exposed by the application container               | `80`               |

