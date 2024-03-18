# Jenkins with CASC Configuration and Job DSL Testing

This project offers a Dockerized Jenkins environment configured via CASC (Configuration as Code) and Job DSL scripting, enabling efficient testing of your Jenkins jobs.

## Features:

- Automated testing of Jenkins jobs
- Reproducible and maintainable configurations through code

## Prerequisites:

- Docker (https://www.docker.com/)
- Docker Compose (https://docs.docker.com/compose/)
- Git (optional)

## Getting Started:

### Clone:
```Bash
git clone https://github.com/Thomaltarix/My_Marvin.git
```

### Environment Variables:
Create a `.env` file for environment variables (passwords, jcasc config...)

### Start Jenkins:
```Bash

docker-compose up --build
```

- Builds Jenkins image
- Creates persistent configuration volume
- Mounts volume and scripts (if present)

### Access Jenkins:
Open `http://localhost:8080` (or your mapped port) and log in.

### Verify Configuration and Jobs:
- Check if CASC configurations and Job DSL scripts applied correctly
- Create additional configurations or Job DSL scripts within Jenkins (optional)

## Customization:

- `my_marvin.yml`: Define CASC configurations (https://www.jenkins.io/doc/book/managing/casc/)
- `job_dsl.groovy`: Create jobs using Job DSL plugin (https://plugins.jenkins.io/job-dsl/)
- `.env` (Optional): Dynamic values in CASC or Job DSL

## Notes:

- Initial build uses root for security, then switches to jenkins user.
- Consider dedicated Jenkins user with appropriate permissions for production.
- Docker Compose simplifies multi-container management.

**Happy Testing!**