# NASA Ocean AI Workshop 2025

![Cover](https://github.com/nasa-oceanai/workshop2025/blob/main/media/cover.png)

Welcome to the code base and resource hub for the NASA Ocean AI Workshop 2025 Hackathon. This repository equips you with tools, data access instructions, and resources to excel in the workshop.

## Resources

- **Main Communication**: Join our Slack workspace at [nasa-ocean-ai-wg.slack.com](https://nasa-ocean-ai-wg.slack.com) for updates and collaboration.
- **Agenda and Information**: Access the master Google Sheet pinned in the `#workshop2025` Slack channel for the agenda, key links, and essential details.
- **Useful Links**: Explore the "Bookmarks" folder in the Google Sheet for additional resources.

## The Hacker's Game - Enter the Realm, Become a Knight

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

---

# Quest for the Ocean Code

Prepare to embark on a three-day quest through the vast ocean of data, from Monday, May 19th to Wednesday, May 21st, 2025! During this hackathon, you’ll form battalions to tackle data challenges, blending ocean science with AI wizardry to decode the mysteries of the sea. Each day brings new trials, forging your team’s path to victory. Below is your **battle plan**, complete with a detailed agenda to guide your journey.

## Day One: Define Your Battlefield (Monday, May 19th)

On the first day, you’ll rally your forces and stake your claim in the realm of ocean data challenges.

- **Morning – Hear the Call to Arms**: Attend the morning session to hear pitches of data challenge ideas. Seek a problem and battalion that ignite your passion, then pledge your allegiance by joining a team.
- **Afternoon – Council of War (2-Hour Hackathon)**: Break into battalions, each dedicated to a challenge. During this two-hour hackathon (1:00 PM – 3:00 PM):
  - Forge bonds with your fellow knights: Share your expertise in detail and learn your comrades’ strengths.
  - Contribute to the war council: Discuss strategies to conquer the challenge.
  - **Goals**:
    1. Clearly define and articulate the physical problem and the ML architecture.
    2. Assign roles to each knight based on their strengths.

### Roles in the Battalion
Every knight plays a vital role in the quest. Volunteer to lead if your tools are ready, or take on a supporting role:

- **Sage of the Tides (Lead Physical Scientist)**: The wise navigator who articulates the physics and its importance in plain English, both in speech and writing.
- **Sorcerer of Algorithms (Lead ML Developer)**: The master of machine learning who designs and crafts the ML architecture to solve the challenge.
- **Lifeguard (Tech Support)**: The vigilant sentinel of the data sea, ensuring the team’s access to the data in AWS cloud and JupyterHub and banishing technical foes.
- **Bard of Chronicles (Reporter)**: The storyteller who documents the battalion’s journey, capturing progress, insights, and victories.
- **Watcher of the Waves (Spectator)**: The observant ally who provides fresh perspectives, cheers the team, and offers support from the sidelines.

- **Earn 1 point** for your battalion after defining the problem
- **Earn 1 point** for outlining the ML architecture
- **Earn 1 point** for assigning roles
- **Earn 1 point** for starting a shared document outlining the problem, dataset and model design

### Day Two: Forge Your Weapons (Tuesday, May 20th)

On the second day of your quest, your battalion will harness the wisdom of the realm’s scholars and forge the tools needed to conquer your challenge. You’ll craft a prototype and test your mettle against the ocean’s mysteries, preparing for the final battle on Day Three.

- **Morning – Gather at the War Table (9:00 AM – 10:00 AM)**: Begin by reflecting on your quest and gathering insights from the day’s scrolls of wisdom. Your **Sage of the Tides** and **Sorcerer of Algorithms** will:
  - Recap Day One’s progress
  - Lay out the day’s battle plan
- **Afternoon – Forge and Test Your Arsenal (2-Hour Hackathon)**: craft and test your prototype. Each knight has a role to play:
  - **Sage of the Tides**: Lead the documentation of the physical context in the shared notes. Answer team questions about physical constraints.
  - **Sorcerer of Algorithms**: Lead the coding of the ML model, starting with a simple prototype. 
  - **Lifeguard**: Assist with data access (e.g., pulling data from S3), answering questions about jupyterhub. 
  - **Bard of Chronicles**: Document the hackathon process in the shared notes, capturing challenges (e.g., data quality issues), decisions (e.g., feature selection rationale), and early results (e.g., model performance metrics). 
  - **Watcher of the Waves**: If you have ML background, test the prototype on a small data subset, providing feedback on initial outputs (e.g., prediction accuracy, visualizations). If you have oceanography background, create some visulizations of the ocean features in the dataset. Save them in the shared document. 

- **Deliverable**: A working ML prototype that processes a data subset and produces initial results (e.g., predictions, a simple visualization like a graph of predicted vs. actual values).
- **Goal**: By the end of the hackathon, your battalion should have a functional prototype tested on a subset of the data, with a clear plan for refinement on Day Three, or the night of Day Two.

#### Points to Earn on Day Two
Earn points for your battalion by completing the following tasks during the day:

- **Earn 1 point** for creating and testing a functional prototype
- **Earn 1 point** for documenting the process in the shared notes, including data features, model architecture, and early findings (at least 2 pages of detailed notes).
- **Earn 1 point** for committing your prototype code and notes to the GitHub repository
- **Earn 1 point** for sketching a draft outline for the final presentation (e.g., slide titles: "Problem," "Approach," "Results").

**Total Possible Points: 4** – These points ensure your battalion is well-prepared for the final day of the quest.

### Day Three: Charge into Battle (Wednesday, May 21st)

On the final day of your quest, your battalion will conquer the battleground and celebrate your triumphs. You’ll refine your prototype, present your victories to the council of knights.

- **Morning – Gather at the War Table**: Reflect on your quest and gather wisdom
  - Discuss progress and challenges with all battalions, identifying areas to improve your prototype (e.g., accuracy, physical relevance).
  - **Deliverable**: An updated prototype with refined results (e.g., improved predictions, new visualizations).
- **Early Afternoon – Final Stand at the Forge (1:00 PM – 2:00 PM)**: Engage in a 1-hour final sprint to polish your prototype and rally for the tournament:
  - **Sage of the Tides**: Validate the final results against oceanographic principles (e.g., ensure predictions reflect realistic current patterns or temperature gradients). Prepare key points for the presentation on the problem’s physical significance.
  - **Sorcerer of Algorithms**:  Finalize the code, help with the presentation.
  - **Lifeguard**: Prepare to share your wisdom on the tools and data format for workshops and future ML collabrations. 
  - **Bard of Chronicles**: Create a 3-slide presentation (3–5 minutes) with sections: "The Challenge" (problem statement), "The Quest" (approach and model), and "The Triumph" (results and impact). Add a recommendation section from **Lifeguard** to the shared notes on dataset improvements and next steps
  - **Watcher of the Waves**: Providing feedback on final outputs, and assist the Bard with presentation visuals (e.g., a key graph or map).
  - **Deliverable**: A 3-slide presentation (e.g., in Google Slides or a shared doc) and a finalized prototype with at least one polished visualization.
  
- **Afternoon – The Final Council (2:00 PM – 2:30 PM)**: Present your triumphs.
  - Each battalion delivers a 3–5 minute presentation to the council of knights (all participants and organizers). The **Bard of Chronicles** leads, with the **Sage of the Tides** and **Sorcerer of Algorithms** explaining the physics and ML solution. The **Lifeguard** and **Watcher of the Waves** chime in when needed.
  - **Final Council (2:30 PM – 4:00 PM)**: Join the panel and group discussions, sharing your quest’s lessons (e.g., dataset challenges, ML insights) and contributing to the realm’s future.

- **Goal**: Deliver a compelling presentation that showcases your battalion’s achievements, document your journey with lessons learned, and provide actionable recommendations for future NASA ocean AI quests.


#### Points to Earn on Day Three
Earn points for your battalion by completing the following tasks:
- **Earn 1 point** for refining your prototype with updated results (e.g., improved predictions, a new visualization like a map of ocean features, training and validation results).
- **Earn 1 point** for completing and delivering a 3-slide presentation during the Grand Tournament, with a recommendation section in the shared notes.
- **Earn 1 point** for contributing at least one meaningful insight during the panel or group discussions (e.g., a dataset improvement idea, a lesson from your ML model).

**Total Possible Points: 3** – These points crown your quest with triumph, showcasing your battalion’s valor and wisdom.

---

Hail, Valiant Knight! Your triumph in the Quest for the Ocean Code has earned you a place of honor in the NASA Ocean AI Working Group!