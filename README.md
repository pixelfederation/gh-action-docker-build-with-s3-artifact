<!-- start title -->

# GitHub Action: docker build with s3 artifact action

<!-- end title -->
<!-- start description -->

GitHub Action to build docker image with artifact from s3 using buildx

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: pixelfederation/gh-actions-get-multi-yaml-paths@undefined
  with:
    # AWS S3 region of artifact
    # Default: eu-west-1
    aws_region: ""

    # Name of the image
    image_name: ""

    # Tag of the image
    image_tag: ""

    # Buildx options
    # Default: default
    buildx_endpoint: ""

    # Buildx driver-opts
    # Default: env.BUILDKIT_STEP_LOG_MAX_SIZE=-1
    buildx_driver_opts: ""

    # Path to Dockerfile
    dockerfile: ""

    # Docker context
    # Default: .
    context: ""

    # Name of S3 bucket with artifact
    artifacts_bucket: ""

    # Path to artifact file on S3 bucket.
    artifact_name_server: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                  | **Description**                     |             **Default**             | **Required** |
| :------------------------- | :---------------------------------- | :---------------------------------: | :----------: |
| **`aws_region`**           | AWS S3 region of artifact           |             `eu-west-1`             |   **true**   |
| **`image_name`**           | Name of the image                   |                                     |   **true**   |
| **`image_tag`**            | Tag of the image                    |                                     |   **true**   |
| **`buildx_endpoint`**      | Buildx options                      |              `default`              |   **true**   |
| **`buildx_driver_opts`**   | Buildx driver-opts                  | `env.BUILDKIT_STEP_LOG_MAX_SIZE=-1` |   **true**   |
| **`dockerfile`**           | Path to Dockerfile                  |                                     |   **true**   |
| **`context`**              | Docker context                      |                 `.`                 |   **true**   |
| **`artifacts_bucket`**     | Name of S3 bucket with artifact     |                                     |   **true**   |
| **`artifact_name_server`** | Path to artifact file on S3 bucket. |                                     |   **true**   |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start [.github/ghdocs/examples/] -->
<!-- end [.github/ghdocs/examples/] -->
