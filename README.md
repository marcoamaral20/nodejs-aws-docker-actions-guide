# Node.js AWS Docker Deployment with GitHub Actions

This repository provides a workflow for deploying a Node.js application to an Amazon EC2 instance using Docker and GitHub Actions. The workflow automates building Docker images, pushing them to Amazon ECR, and updating an EC2 container with the latest image.

## Workflow Overview

The workflow defined in `docker_ec2_deploy.yml` performs the following steps:

1. **Build Docker Image**: Builds the Docker image for the Node.js application using the provided Dockerfile.

2. **Publish Docker Image**: Pushes the built Docker image to Amazon ECR for storage.

3. **Update EC2 Container**: SSHs into the specified EC2 instance, stops and removes the existing container, pulls the latest Docker image from Amazon ECR, and runs the updated container.

## Usage

To use this workflow in your project, follow these steps:

1. Fork this repository or copy the contents of `docker_ec2_deploy.yml` to your own GitHub Actions workflow file.

2. Replace the workflow file's placeholders with your AWS credentials, repository details, SSH credentials, and any other environment-specific variables.

3. Ensure your Node.js application's Dockerfile is correctly configured in the repository.

4. Commit the changes to your repository. The workflow will automatically trigger on pushes to your specified branch or tags.

## Contributing

Contributions to enhance this workflow are welcome! Feel free to open an issue or create a pull request if you have any suggestions or improvements.

## License

This project is licensed under the [MIT License](LICENSE).
