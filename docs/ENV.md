# ENVIRONMENT VARIABLES CONFIGURATION

This document describes the environment variables that can be used to configure the application, and how to set them up.

---

## Define the env variables on CircleCI

The first step is to define the environment variables on CircleCI. You can do this by going to the project settings, and then to the "Environment Variables" section.

![CircleCI Environment Variables](./media/circle%20env.png)

---

## Make a deploy.sh script

 This will set the environment variables on the server programmatically based on the CircleCI environment variables.

 ![deploy.sh](./media/env%20vars.png)

---
