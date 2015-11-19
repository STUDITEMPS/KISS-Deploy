# Gitlab
## Starting only Gitlab:
Export the gitlab secret key and db password found in the wiki in Pages -> KISS Development Tech Home -> Anleitungsartikel
```sh
export GITLAB_SECRETS_DB_KEY_BASE=XXXXX
export DB_PASS=XXXXX
docker-compose up -d gitlab
```

## Starting CI-runners:
When Gitlab is running export the runner token found at GITLAB-URL/ci/admin/runners
```sh
export RUNNER_TOKEN=XXXXX
docker-compose up -d gitlabrunner
```

## Starting everything:
Combine both commands:
```sh
export GITLAB_SECRETS_DB_KEY_BASE=XXXXX
export DB_PASS=XXXXX
export RUNNER_TOKEN=XXXXX
docker-compose up -d
```

## Scaling CI-runners:
```sh
docker-compose scale gitlabrunner=NUMBER_OF_RUNNERS
```
docker-compose remembers the number of runners for the next start if you shut down and restart the runners
