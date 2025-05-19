# NASA Ocean AI Workshop 2025

![Cover](../media/cover.png)

Welcome to the code base and resource hub for the NASA Ocean AI Workshop 2025 Hackathon. This repository equips you with tools, data access instructions, and resources to excel in the workshop.

## Resources

- **Main Communication**: Join our Slack workspace at [nasa-ocean-ai-wg.slack.com](https://nasa-ocean-ai-wg.slack.com) for updates and collaboration.
- **Agenda and Information**: Access the master Google Sheet pinned in the `#workshop2025` Slack channel for the agenda, key links, and essential details.
- **Useful Links**: Explore the "Bookmarks" folder in the Google Sheet for additional resources.

## Enter the Realm, Become a Knight

Embark on a noble quest to prepare for the NASA Ocean AI Workshop 2025 Hackathon! This guide leads you through essential steps to join the community and uncover vital resources. Each step earns **1 point**—collect all **5 points** to be knighted and ready for the workshop!

### 1. Cross the Castle Gates: Join the Slack (1 Point)

Enter the kingdom’s central hub at [nasa-ocean-ai-wg.slack.com](https://nasa-ocean-ai-wg.slack.com). If you face barriers (e.g., trouble joining), send a raven (email) to Jinbo for aid.

**Earn 1 point** upon entering the Slack workspace.

### 2. Proclaim Your Presence: Introduce Yourself (1 Point)

Make your mark in the `#social` channel. Post a hearty "Hi!" or a brief introduction to share your tale with fellow knights.

**Earn 1 point** after posting your introduction.

### 3. Seek the Guides: Visit the Bookmarks (1 Point)

Journey to the `#workshop2025` channel, your guidepost for the quest. Find the "Bookmarks" on the top bar, open all three bookmarks, and explore every tab in the master Google Sheet to uncover vital scrolls.

**Earn 1 point** after opening all bookmarks and reviewing all tabs in the Google Sheet.

### 4. Explore the Kingdom: Navigate the Google Sheet (1 Point)

Venture deeper into the master Google Sheet to prepare for your quest:

- **Agenda Tab**: Open all links, including the Zoom link, to plan your journey.
- **Parking Tab**: If traveling by "steed" (vehicle), click the links to find the best parking spot.
- **Data Challenge Tab**: Share your bold ideas in this tab (optional but encouraged).
- **Score Board Tab**: Track your workshop exploration progress.

**Earn 1 point** after completing these tasks.

### 5. Join the Guilds: Connect with Channels (1 Point)

Forge alliances by joining channels that ignite your passion, such as `#code`, `#aws-cloud`, `#data-products`, `#social`, or `#sst`. Each guild offers unique wisdom and fellowship.

**Earn 1 point** after joining at least one channel.

---

**Hail, Noble Knight!** With all **5 points** collected, you’ve completed the Knight’s Initiation and are ready to conquer the workshop! Seek counsel in the `#workshop2025` or `#social` Slack channels for guidance.

## Hacker’s Training Survival Kit

This guide is for knights who will wield data by downloading or uploading. Follow these steps to access the workshop’s data and cloud compute environment. Each step earns **1 point**—collect all **5 points** to complete the training!

### 1. Arm Yourself: Install AWS CLI (1 Point)

Equip the AWS Command Line Interface (CLI) to interact with AWS services. Follow the official guide: [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

If you face challenges, seek aid in the `#aws-cloud` Slack channel.

**Earn 1 point** once the AWS CLI is installed.

### 2. Claim the Key: Obtain AWS Credentials (1 Point)

Secure an **AWS Access Key ID** and **Secret Access Key** to unlock the data. Find these credentials in the `#aws-cloud` Slack channel.

**Earn 1 point** after obtaining the key pair.

### 3. Unlock the Vault: Configure AWS Credentials (1 Point)

Configure your AWS CLI with the credentials from Step 2. Run this command:

```bash
aws configure --profile default
```

Enter the prompted details:

```
AWS Access Key ID: [Enter the Access Key ID from Step 2]
AWS Secret Access Key: [Enter the Secret Access Key from Step 2]
Default region name: us-west-2
Default output format: json
```

Test your setup by listing the S3 bucket contents:

```bash
aws s3 ls s3://odsl/cesm_hr_1x1/
```

Expect a file list, such as:

```
2025-05-18 09:21:59          0 
2025-05-18 09:24:16        187 README_CESM_regrid.txt
2025-05-18 09:24:16 4567563517 data_CESM_HR_E03_regrid_1x1deg_pop.h.PD.200101-210001.nc
...
```

Download a file (e.g., `README_CESM_regrid.txt`) to your machine with:

```bash
aws s3 cp s3://odsl/cesm_hr_1x1/README_CESM_regrid.txt ./
```

Explore more data with:

```bash
aws s3 ls s3://odsl/nasa_oceanai_workshop2025/
```

**Earn 1 point** after configuring and testing your AWS CLI.

### 4. Enter the Forge: Access AWS Cloud Compute (1 Point)

To wield the AWS cloud compute environment, share your GitHub username in the `#aws-cloud` Slack channel and tag Jinbo. Once approved, access a JupyterHub interface on AWS for direct S3 data access.

Log in at [https://hub.openveda.cloud](https://hub.openveda.cloud) using your GitHub account.

Gratitude to the EIS and NASA VEDA groups for this mighty resource!

**Earn 1 point** after logging into the cloud environment.

### 5. Craft Your Tools: Run Notebooks in the Cloud (1 Point)

In the cloud environment, reconfigure AWS credentials by repeating Step 3 (`aws configure --profile default` with the same key pair).

Clone the workshop’s GitHub repository for example notebooks:

```bash
git clone https://github.com/nasa-oceanai/workshop2025/
```

Navigate to the `notebooks` directory and run an example notebook. Find them at: [https://github.com/nasa-oceanai/workshop2025/tree/main/notebooks](https://github.com/nasa-oceanai/workshop2025/tree/main/notebooks).

If errors arise, seek help in the `#aws-cloud` Slack channel.

**Earn 1 point** after running a notebook without errors.

---

**Victory, Brave Knight!** With all **5 points** earned, you’ve mastered the Hacker’s Training Survival Kit and are ready to triumph in the hackathon! For support, rally in the `#workshop2025` or `#aws-cloud` Slack channels.

