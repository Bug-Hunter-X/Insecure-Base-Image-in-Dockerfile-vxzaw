# Insecure Base Image in Dockerfile

This repository demonstrates a common error in Dockerfiles: using an insecure base image (`ubuntu:latest`). This can lead to unexpected behavior and security vulnerabilities because the base image can change without notice.

## Bug

The provided `Dockerfile` uses `ubuntu:latest`, which is a floating tag. This means the image will always pull the newest version of Ubuntu, which may contain unexpected changes. 

## Solution

The solution is to specify a particular version of Ubuntu (e.g., `ubuntu:22.04`) to avoid unforeseen issues and maintain consistent behavior. Using a tagged version ensures reproducibility and reduces security risks.
