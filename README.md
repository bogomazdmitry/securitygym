# Security Gym

Secure Software Development Training Platform

This fork fixes Docker startup and exercise-checking compatibility:

- Node.js 22 with webpack 4 compatibility and a frozen Yarn lockfile.
- PostgreSQL readiness checks before the API starts.
- Compatible Flask-WTF and SQLite driver versions for the exercise images.
- Reduced Go build parallelism to fit the executor's memory limit.

Validated locally: frontend development and production builds, registration and
login, and a sample exercise check for Python, JavaScript, and Go.

## Run Locally

Clone the project

```bash
  git clone https://github.com/bogomazdmitry/securitygym
```

Go to the project directory

```bash
  cd securitygym
```

Build images for running tests

```bash
  make imagesbuild
```

Start the server

```bash
  make devrun
```

Open http://localhost:8000 in your browser. The UI runs on Node.js 22 inside
Docker; its dependencies are pinned in `ui/react-ui/yarn.lock`.

## Deployment

Build images for running tests

```bash
  make imagesbuild
```

To deploy this project run

```bash
  make prodrun
```
