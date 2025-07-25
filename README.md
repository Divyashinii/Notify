# Notify
Static website hosted on Azure and notifies users upon each image upload

## Connecting 2 Azure services (Use case: When user uploads an image, he should get an email)

In this project, we just basically create 2 distinct cloud resources (1 storage account and 1 logic app) and connect them to work together.

**Functionality:**

- users can upload an image through a static website hosted in storage account
- once the users upload images, those will be stored in another container ( `images` ) of the same storage account
- After the image upload to the `images`  container, it will be monitored by the logic app we created, then it will send out an email to the user!

**Cloud Resources to be created:**

| Resource type | Resource name | Purpose |
| --- | --- | --- |
| Resource Group | notifyprojrg | A place/container to store the related resources of this project; in this case: `notifyprojsg`  and `notifyprojlapp` |
| Storage account | notifyprojsg | To host the static website for the users to access, Also store the images uploaded by users |
| Logic App | notifyprojlapp | An Azure service capable of multiple features, but in this case, it helps to send emails to the users about their image upload! |

### Architecture diagram
![Architecture diagram](./Architecture/img.png)
