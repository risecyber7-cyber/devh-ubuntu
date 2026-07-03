# Ubuntu CloudLab (GitHub Actions + Tailscale + Remote Desktop)

This project lets you launch a temporary Ubuntu cloud machine using GitHub Actions, connect it to your Tailscale network, and access it remotely.

## Step 1: Open the Repository

Go to:

https://github.com/risecyber7-cyber/devh-ubuntu

## Step 2: View the Workflow

1. Open the **.github/workflows** folder.
2. Click **ubuntucloud.yml**.
3. You can review or edit the workflow before running it.

## Step 3: Run the Workflow

1. Click the **Actions** tab.
2. Select **Ubuntu Lab**.
3. Click **Run workflow**.
4. Leave the branch as **main**.
5. Click the green **Run workflow** button.

## Step 4: Open the Running Job

1. Open the running **Ubuntu Lab** workflow.
2. Click **workflow_dispatch**.
3. Click **ubuntulab** to view the live logs.

## Step 5: Authenticate Tailscale

During the workflow, you'll see a Tailscale authentication link.

1. Click the link.
2. Sign in with your Google account.
3. Click **Connect** to authorize the machine.
4. After authorization, return to the GitHub Actions page.

## Step 6: Get Your Login Credentials

In the workflow logs, locate the **Connection Information** section.

It will display:

* Username
* Password

Save these credentials.

## Step 7: Install Tailscale on Your Computer

Download Tailscale from:

https://tailscale.com/download

1. Install Tailscale.
2. Sign in using **the same Google account** you used to authorize the GitHub runner.
3. Wait until your device is connected to your Tailnet.

## Step 8: Find the Runner

In the Tailscale dashboard, you'll see a machine similar to:

* **Machine Name:** `runnervmkkn4f`
* **OS Hostname:** `runnervmkkn4f`

Copy the **OS Hostname**.

## Step 9: Connect via Remote Desktop

1. Open your Remote Desktop client (such as Microsoft Remote Desktop).
2. In the **Computer** field, paste the copied **OS Hostname**.
3. Enter the username and password shown in the GitHub workflow logs.
4. Connect to your Ubuntu CloudLab.

---

## Notes

* The runner is temporary and will be removed after the workflow finishes or reaches its time limit.
* Each workflow run creates a new machine with a different hostname.
* You must authenticate Tailscale each time a new runner is created.

---

⭐ If you found this project helpful, consider giving the repository a **Star** and following for more useful GitHub Actions and cloud computing projects.
