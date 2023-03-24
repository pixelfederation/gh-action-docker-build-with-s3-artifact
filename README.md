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

    # Name of the image (DEPRECATED in v0.1.5)
    image_name: ""

    # Tag of the image (DEPRECATED in v0.1.5)
    # Use 'image_tags' instead
    image_tag: ""

    # List of tags (replaces deprecated image_name and image_tag)
    # Format: user/app:tag1, user/app:tag2
    image_tags: ""

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

    # List of external cache sources (e.g., type=local,src=path/to/dir)
    cache_from: ""

    # List of cache export destinations (e.g., type=local,dest=path/to/dir)
    cache_to: ""
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                  | **Description**                          |             **Default**             | **Required** |
| :------------------------- | :--------------------------------------- | :---------------------------------: | :----------: |
| **`aws_region`**           | AWS S3 region of artifact                |             `eu-west-1`             |   **true**   |
| **`image_name`**           | Name of the image (DEPRECATED in v0.1.5) |                                     |   **true**   |
| **`image_tag`**            | Tag of the image (DEPRECATED in v0.1.5)  |                                     |   **true**   |
| **`image_tags`**           | List of tags                             |                                     |   **true**   |
| **`buildx_driver_opts`**   | Buildx driver-opts                       | `env.BUILDKIT_STEP_LOG_MAX_SIZE=-1` |   **true**   |
| **`dockerfile`**           | Path to Dockerfile                       |                                     |   **true**   |
| **`context`**              | Docker context                           |                 `.`                 |   **true**   |
| **`artifacts_bucket`**     | Name of S3 bucket with artifact          |                                     |   **true**   |
| **`artifact_name_server`** | Path to artifact file on S3 bucket.      |                                     |   **true**   |
| **`cache_from`**           | List of external cache sources           |                                     |   **false**  |
| **`cache_to`**             | List of cache export destinations        |                                     |   **false**  |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start [.github/ghdocs/examples/] -->
<!-- end [.github/ghdocs/examples/] -->
