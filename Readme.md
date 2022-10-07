
# First time run
* update uid/gid on `.env`
  - `./make_env.sh`
* run jenkins controller
  - `docker-compose up -d`
* see initial password from log
  - `docker-compose logs -f`

# After the first run
- `docker-compose up -d`

# etc
* restart jenkins
  - `docker-compose restart`
* stop jenkins
  - `docker-compose stop`
* check status
  - `docker-compose ps`

# Reference:
`.env` file is used for docker-compose environment variable

You can pass multiple environment variables from an external file through to a service’s containers with the ‘env_file’ option, just like with `docker run --env-file=FILE ...`
`
web:
  env_file:
    - web-variables.env
`

${VARIABLE:-default} evaluates to default if VARIABLE is unset or empty in the environment.
${VARIABLE-default} evaluates to default only if VARIABLE is unset in the environment.

# Link:
- https://docs.docker.com/compose/environment-variables/
- https://docs.docker.com/compose/env-file/
