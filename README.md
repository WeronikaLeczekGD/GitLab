# GitLab


## 1. Create a new empty repository in Gitlab. Use Gitlab instructions to add the code from your forked spring-petclinic repository. Add your Dockerfile.

## 2. Create 2 docker repositories on your own Nexus Repository (Instruction) or https://hub.docker.com/ called “main” and “mr”. Alternatively, you can use GitLab Container Registry with 2 different image names in one repository (see Image naming convention).

## 3. Add .gitlab-ci.yml file and describe the following behavior there:

### The pipeline for a merge request should include the following jobs:

1. Checkstyle

Use Maven or Gradle checkstyle plugin to generate a code style report. It should be available as a job artifact.

2. Test (with Maven or Gradle)

3. Build

Build without tests (with Maven or Gradle).

Note: For the first 3 jobs, the GitLab runner can use maven:3.8.5-openjdk-17 docker image.

4. Create a docker image

Using your Dockerfile in the spring-petclinic repo, create a docker image with spring-petclinic application,  tag it using CI_COMMIT_SHORT_SHA and push it to the “mr” repository.

Note: Use Docker to build Docker images | GitLab 

### The pipeline for the main branch should include the following job:

1. Create a docker image

Build a docker image and push it to the “main” repository.


## Ad 1

Pushing project to gitlab:

![Screenshot 2023-01-09 at 21 32 48](https://user-images.githubusercontent.com/114099418/211403862-8d79ccb2-af46-41cb-b4cd-e798ac69f593.png)

Here it is:

![Screenshot 2023-01-15 at 16 06 35](https://user-images.githubusercontent.com/114099418/212549387-4c739b6a-db9b-494c-ae4d-a5367687de2b.png)


I also added and connected a runner:

![Screenshot 2023-01-10 at 11 14 05](https://user-images.githubusercontent.com/114099418/212548878-6a2b2a65-2e74-413b-bd08-a89c0873f59f.png)


## Ad 2

I have created those 2 repository in previous task on dockerhub

## Ad 3

My yml file:



