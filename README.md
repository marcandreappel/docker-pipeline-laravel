# Docker image for Laravel Bitbucket pipeline

A Docker image for PHP 7.4 Laravel projects, conceived for Bitbucket Pipelines.

### bitbucket-pipeline.yml

```yaml
image: marcandreappel/docker-pipeline-laravel:latest

pipelines:
  branches:
    master:
    - step:
        script:
        - curl -so phing.phar https://www.phing.info/get/phing-latest.phar
        - php artisan ...
```

