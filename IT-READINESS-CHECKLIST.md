# Workshop IT Readiness Checklist

**Sessions:** Power Apps vibe experience (preview) and Microsoft Copilot Studio

**Goal:** Every participant can build and test in a safe, non-production environment and access the public workshop materials from the internal network.

> **Recommended setup:** Use one IT-managed **Trial** Power Platform environment in the **Asia** region, with **Dataverse** and a participant security group. Create it at least **7 days before training**.

## 1. Environment

- [ ] Create a dedicated environment; do **not** use the Default or Production environment.
- [ ] Set **Type = Trial**, **Region = Asia**, and **Add Dataverse = Yes**.
- [ ] Restrict access with a Microsoft Entra security group containing participants, trainer, and IT support.
- [ ] Confirm the trial remains active through the training date.
- [ ] Use training-only names and sample data; do not use confidential or production data.
- [ ] Record who will remove the environment, apps, agents, connections, and data after training.

> A standard trial environment lasts 30 days and cannot be backed up, restored, copied, or reset. Export anything that must be retained.

## 2. Accounts, licenses, and roles

- [ ] Confirm every participant has a working organizational account and can complete MFA.
- [ ] For Power Apps, assign an existing eligible license or a **30-day Power Apps trial**.
- [ ] For Copilot Studio, assign or allow each participant to activate a **Copilot Studio trial**.
- [ ] Add participants to the environment security group and assign **Environment Maker**.
- [ ] If the lab creates Dataverse tables, also assign **System Customizer** or an approved custom role with the required table privileges.
- [ ] Confirm participants can see and select the training environment in both products.
- [ ] Give the trainer and named IT support staff sufficient access to assist and recover lab work.

> Copilot Studio trial users can create and test agents in the test chat, but **cannot publish** them. Publishing must not be a required lab outcome unless paid licensing and policy are confirmed.

## 3. Enable the Power Apps vibe experience

- [ ] In Power Platform admin center, turn on **Copilot in Power Apps (preview)** at tenant level.
- [ ] Confirm the training environment is in a supported region and is not the Default environment.
- [ ] Use **English prompts** during the lab; the preview currently supports English only.
- [ ] Confirm participants can open [Power Apps vibe](https://vibe.preview.powerapps.com/) or [Power Apps preview](https://make.preview.powerapps.com/).
- [ ] Optional: enable **External Models** only after security and compliance approval.

## 4. Security, data, and connectors

- [ ] Approve the exact lab data sources, knowledge files, connectors, and Power Automate actions, if used.
- [ ] Apply a data policy that allows only required lab connectors and blocks unnecessary external connectors or channels.
- [ ] Confirm organizational policies allow the required generative AI features and any necessary cross-region data movement.
- [ ] Use individual connections; do not share passwords or one common participant account.
- [ ] Keep agent publishing, public channels, and production connections disabled unless explicitly approved.
- [ ] Apply policy changes at least 24 hours before rehearsal.

## 5. Network and devices

- [ ] Use a current Microsoft Edge or Google Chrome browser with pop-ups and required cookies allowed.
- [ ] Confirm outbound **HTTPS and WSS** access for Microsoft sign-in and Power Platform services.
- [ ] Test access through the same Wi-Fi, proxy, VPN, firewall, DNS, and SSL inspection path participants will use.
- [ ] Confirm these portals open without errors:
  - [ ] `https://login.microsoftonline.com`
  - [ ] `https://vibe.preview.powerapps.com`
  - [ ] `https://make.preview.powerapps.com`
  - [ ] `https://copilotstudio.microsoft.com`
- [ ] Prepare stable Wi-Fi, power, a backup internet connection, and at least one spare device.

## 6. Public repository access

Run these tests with a normal participant account and device on the actual internal network.

- [ ] Confirm organizational policy permits participants to access the approved public GitHub repository.
- [ ] Allow outbound HTTPS access to `github.com`, `raw.githubusercontent.com`, and `codeload.github.com`.
- [ ] Open the [public workshop repository](https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public).
- [ ] Open this [IT readiness checklist](https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public/blob/main/IT-READINESS-CHECKLIST.md).
- [ ] Open the [raw README file](https://raw.githubusercontent.com/teerasej/GSB-vibe-coding-and-agent-day-public/main/README.md) or download a sample file.
- [ ] Download the [repository ZIP](https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public/archive/refs/heads/main.zip).
- [ ] If participants will use Git, test an HTTPS clone:

  ```text
  git clone https://github.com/teerasej/GSB-vibe-coding-and-agent-day-public.git
  ```

- [ ] Confirm the browser or download is not blocked by DNS, proxy, firewall, SSL inspection, content filtering, or endpoint security policy.
- [ ] Record any blocked URL, error message, and remediation owner.
- [ ] Prepare an approved offline ZIP copy if repository access cannot be enabled before training.

> **Reference:** [GitHub connectivity troubleshooting](https://docs.github.com/en/get-started/using-github/troubleshooting-connectivity-problems)

| Repository access test | Result |
|---|---|
| Repository page opens | ☐ Pass ☐ Blocked |
| Checklist and raw file open | ☐ Pass ☐ Blocked |
| ZIP or sample file downloads | ☐ Pass ☐ Blocked |
| HTTPS clone, if required | ☐ Pass ☐ Blocked ☐ Not required |

**Tester:** ____________________

**Test date:** ____________________

**Network path:** ☐ Office network ☐ Training Wi-Fi ☐ VPN ☐ Other: __________

**Remediation owner, if blocked:** ____________________

## 7. Mandatory rehearsal

Use a normal participant account—not an administrator account.

- [ ] Sign in and complete MFA.
- [ ] Access the public workshop repository and required files.
- [ ] Select the training environment.
- [ ] Open the Power Apps vibe experience.
- [ ] Create, preview, and run a small app using an English prompt.
- [ ] Open Copilot Studio and create a test agent.
- [ ] Add the approved knowledge source or tool required by the lab.
- [ ] Test the agent successfully in the test chat.
- [ ] If used, authenticate the approved connector and run the required flow or action.
- [ ] Repeat the rehearsal on the training network.

## 8. Training-day support and sign-off

- [ ] Assign one IT contact who can resolve account, MFA, license, environment, network, and repository-access issues.
- [ ] Prepare a support channel and a participant access list.
- [ ] Prepare approved fallback accounts, devices, pair-work instructions, offline repository files, and trainer demo files.
- [ ] If the vibe preview is unavailable, switch to the trainer demonstration or prepared app.
- [ ] If Copilot Studio access fails, use the trainer demonstration and prepared screenshots or results.

| Readiness gate | Pass |
|---|:---:|
| Trial environment and Dataverse are available | ☐ |
| All participant accounts, licenses, and roles are verified | ☐ |
| Required policies, connectors, and network paths are working | ☐ |
| Public repository browser and download tests pass | ☐ |
| Ordinary-user rehearsal passes for both sessions | ☐ |
| IT support and fallback plan are confirmed | ☐ |

**IT owner:** ____________________

**Rehearsal date:** ____________________

**Final status:** ☐ Ready ☐ Ready with limitations ☐ Not ready

## Microsoft references

- [Power Apps vibe experience prerequisites](https://learn.microsoft.com/power-apps/vibe/overview#prerequisites)
- [Permissions to create and edit Dataverse tables](https://learn.microsoft.com/power-apps/maker/data-platform/create-edit-entities-portal#prerequisites)
- [Power Platform trial environments](https://learn.microsoft.com/power-platform/admin/trial-environments)
- [Copilot Studio trial access and limitations](https://learn.microsoft.com/microsoft-copilot-studio/requirements-licensing-subscriptions#sign-up-for-a-copilot-studio-trial)
- [Secure Copilot Studio projects](https://learn.microsoft.com/microsoft-copilot-studio/guidance/sec-gov-phase3)
- [Power Platform data policies](https://learn.microsoft.com/power-platform/admin/wp-data-loss-prevention)
- [Power Apps required network services](https://learn.microsoft.com/power-apps/limits-and-config#required-services)
