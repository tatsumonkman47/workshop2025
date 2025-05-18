# NASA Ocean AI Workshop 2025

![Cover](../media/cover.png)

Welcome to the code base and resource hub for the NASA Ocean AI Workshop 2025 Hackathon. This repository provides all necessary tools, data access instructions, and resources to help participants succeed.

## Resources

- **Main Communication**: Join our Slack workspace at [nasa-ocean-ai-wg.slack.com](https://nasa-ocean-ai-wg.slack.com) for updates and discussions.
- **Agenda and Information**: Find the master Google Sheet pinned in the `#workshop2025` Slack channel. It contains the agenda, key links, and other critical details.
- **Useful Links**: Check the "Bookmarks" folder in the Google Sheet for additional resources.

## Hacker’s Training Survival Kit

This guide is for participants who will download or upload data. Follow these steps carefully to access the workshop's data and cloud compute environment. Each step earns you **1 point**—collect all 5 points to complete the training!

### 1. Install AWS CLI (1 Point)

Install the AWS Command Line Interface (CLI) to interact with AWS services. Follow the official guide: [AWS CLI Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

If you encounter issues, ask for help in the `#aws-cloud` Slack channel.

**Earn 1 point** once the AWS CLI is successfully installed.

### 2. Obtain AWS Credentials (1 Point)

You need an **AWS Access Key ID** and **Secret Access Key** to access the data. These credentials are shared in the `#aws-cloud` Slack channel.

**Earn 1 point** after locating the key pair.

### 3. Configure AWS Credentials (1 Point)

Configure your AWS CLI with the credentials obtained in Step 2. Run the following command in your terminal:

```bash
aws configure --profile default
```

Enter the following details when prompted:

```
AWS Access Key ID: [Enter the Access Key ID from Step 2]
AWS Secret Access Key: [Enter the Secret Access Key from Step 2]
Default region name: us-west-2
Default output format: json
```

Test your configuration by listing the contents of the workshop's S3 bucket:

```bash
aws s3 ls s3://odsl/cesm_hr_1x1/
```

You should see a list of files, including:

```
2025-05-18 09:21:59          0 
2025-05-18 09:24:16        187 README_CESM_regrid.txt
2025-05-18 09:24:16 4567563517 data_CESM_HR_E03_regrid_1x1deg_pop.h.PD.200101-210001.nc
...
```

To download a file (e.g., `README_CESM_regrid.txt`) to your local machine, use:

```bash
aws s3 cp s3://odsl/cesm_hr_1x1/README_CESM_regrid.txt ./
```

Explore additional data by running:

```bash
aws s3 ls s3://odsl/nasa_oceanai_workshop2025/
```

**Earn 1 point** after successfully configuring and testing your AWS CLI setup.

### 4. Access AWS Cloud Compute Environment (1 Point)

To use the AWS cloud compute environment, provide your GitHub username in the `#aws-cloud` Slack channel and tag Jinbo. Once approved, you’ll gain access to a JupyterHub interface hosted on AWS, allowing direct access to S3 data without downloading.

Log in to the cloud environment at [https://hub.openveda.cloud](https://hub.openveda.cloud) using your GitHub account.

Special thanks to the EIS and NASA VEDA groups for providing this resource!

**Earn 1 point** after successfully logging into the cloud compute environment.

### 5. Set Up and Run Notebooks in the Cloud (1 Point)

In the cloud environment, reconfigure your AWS credentials by repeating Step 3 (run `aws configure --profile default` with the same key pair).

Clone the workshop’s GitHub repository to access example notebooks:

```bash
git clone https://github.com/nasa-oceanai/workshop2025/
```

Navigate to the `notebooks` directory and run one of the example notebooks. Example notebooks are available at: [https://github.com/nasa-oceanai/workshop2025/tree/main/notebooks](https://github.com/nasa-oceanai/workshop2025/tree/main/notebooks).

If you encounter errors, seek assistance in the `#aws-cloud` Slack channel.

**Earn 1 point** after successfully running a notebook without errors.

---

**Congratulations!** If you’ve collected all **5 points**, you’ve completed the Hacker’s Training Survival Kit and are ready to dive into the hackathon!

For further questions or support, reach out in the `#workshop2025` or `#aws-cloud` Slack channels.

