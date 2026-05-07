
# CI/CD Pipeline with Jenkins, Docker, and Kubernetes Project

![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white&style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=flat)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white&style=flat)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?logo=jenkins&logoColor=white&style=flat)
![License](https://img.shields.io/badge/License-MIT-yellow)

This project demonstrates a CI/CD workflow using Jenkins, Docker, and Kubernetes.

Using Jenkins, the pipeline automatically:

- Builds the application
- Creates a Docker image
- Pushes the image to Docker Hub
- Deploys the application to Kubernetes

The project was built to showcase practical experience with deployment automation and container-based workflows.

<https://docs.github.com/en/actions>

<https://docs.docker.com/>

<https://kubernetes.io/docs/home/>

<https://www.jenkins.io/doc/>

---

## Link the github repository in Jenkins (Optional)

1. Install the GitHub Plugin in Jenkins (usually pre-installed)

2. Configure your Jenkins pipeline job

    In your pipeline job configuration, under Build Triggers, check **GitHub hook trigger for GITScm polling** or, for a Multibranch Pipeline, Jenkins will automatically set up webhooks for each branch.

3. Add a GitHub Webhook

    Go to your GitHub repository > Settings > Webhooks, click Add webhook, set the Payload URL to:

    ```
    http://<your-server-ip>:<port>/github-webhook/
    ```

    Choose Just the push event (or select the events you want to trigger builds), click Add webhook.

## Add DockerHub and Kubernetes credentials

1. **Dashboard**>**Manage Jenkins**>**Manage Credentials**>**Global**>**Add Credentials**

2. Add DockerHub username, password and the ID (In Jenkinsfile)

3. Add the Kubernetes config file

## Run the pipeline

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

**Star this repository if it helped you!**
