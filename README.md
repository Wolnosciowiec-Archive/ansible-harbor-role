Dockerized Project
==================

Automated deployment of Dockerized environment from GIT which includes:

- systemd integration
- production specific .env configuration
- test server specific .env configuration (when: host equals localhost)
- Makefile support to manage the project

Preliminaries
-------------

1. You need a project at any git server.
2. The project need to have a Makefile with task "deployment_pre"
3. Your project need to have an `.env` file, or `.env-template` that will be copied into `.env`

Environment
-----------

```yamlex
# user who deploys the application
deploy_user: tech.admin

project_dir: /project

# this origin will be set only during deployment time
git_deploy_url: https://user:password@somehost/someuser/somerepo

# without user and password, this form will stay on server
git_regular_deploy_url: https://somehost/someuser/somerepo
```
