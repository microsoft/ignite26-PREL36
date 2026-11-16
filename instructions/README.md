# PREL36: Build your first agent in Copilot Studio

These are the attendee instructions for the four-hour Microsoft Ignite 2026 pre-day lab. You will build **Contoso IT Concierge**, an IT support agent powered by the **GitHub Copilot harness** in Microsoft Copilot Studio.

The agent answers grounded IT questions, retrieves current devices from SharePoint, follows reusable skills, and calls a workflow to email a confirmed device request. Before publishing, you'll review its configuration, improve its device-selection rules, and run a reusable evaluation. Sending a request is not approval, procurement, or a stock reservation.

## Four-hour agenda

The schedule includes **220 minutes of instruction and hands-on work plus two 10-minute breaks**. Times are delivery estimates, not measured completion times. Complete the sections in order; each extends the same agent.

| Elapsed time | Section | Minutes |
| --- | --- | --- |
| 00:00-00:15 | [Introduction, sign-in, and agent fundamentals](./00-Introduction.md) | 15 |
| 00:15-00:25 | [Create a solution](./01-Create-A-Solution.md) | 10 |
| 00:25-01:00 | [Build and ground the agent](./02-Build-And-Ground-The-Agent.md) | 35 |
| 01:00-01:15 | [Add the SharePoint tool](./03-Add-The-SharePoint-Tool.md) | 15 |
| 01:15-01:25 | Break | 10 |
| 01:25-01:55 | [Add and refine skills](./04-Add-And-Refine-Skills.md) | 30 |
| 01:55-02:05 | Break | 10 |
| 02:05-02:50 | [Build the device-request workflow](./05-Build-The-Device-Request-Workflow.md) | 45 |
| 02:50-03:10 | [Test the solution end to end](./06-Test-End-To-End.md) | 20 |
| 03:10-03:40 | [Review, improve, and evaluate the agent](./07-Review-And-Evaluate.md) | 30 |
| 03:40-04:00 | [Publish and plan for operation](./08-Publish-And-Wrap-Up.md) | 20 |

The evaluation block includes one run. If it reveals a problem, correct it and rerun before publishing rather than skipping a failed check to meet the schedule. Rehearse this revised pacing in the assigned tenant; evaluation runtime can vary.

## Optional early-finisher activities

After publishing, [section 9: Bonus labs](./09-Bonus-Labs.md) offers four independent exercises: analyze an asset CSV with Python and generate charts/a PowerPoint deck, save and reuse a response-format memory, add Work IQ for people and calendar tasks, or try the **App (Preview)** capability with sample prompts for an asset dashboard, warranty planner, or support-intake prototype. Choose what fits your remaining time; these activities are outside the four-hour agenda and are not required for completion. The bonus CSV is downloaded from the repository, not preinstalled in the VM.

## Learning outcomes

By the end of the lab, you will be able to:

- Build a scoped, instruction-driven agent and ground its answers in approved knowledge.
- Connect a live SharePoint tool and reusable skills that guide reliable device selection.
- Improve device-selection rules and evaluate a reusable set of support, inventory, and boundary conversations before publishing.
- Call a workflow after confirmation, verify successful and cancelled requests, and publish the agent to an employee channel.

## Skillable conventions

Open the **Resources** panel for your assigned virtual machine credentials, Microsoft 365 account, Power Platform environment, SharePoint site URL, and lab email address. Use only your assigned lab resources.

Text surrounded by `+++` becomes clickable autotype text in Skillable. Multiline prompts and instructions appear in fenced text blocks for copying. Select the destination field before using autotype or pasting.

> [!IMPORTANT]
> Wait for autotype to finish before interacting with the virtual machine. Do not paste VM credentials into Microsoft 365 sign-in fields. Use the appropriate credentials from **Resources**.

The SharePoint URL uses `@lab.CloudCredential(WWLM365E7).TenantPrefix` to insert the assigned tenant prefix in Skillable. The delivery team must map the `WWLM365E7` credential to the learner's Microsoft 365 tenant and verify that the URL resolves before delivery. Outside Skillable, use the actual **Contoso IT** site URL from **Resources** instead of the unresolved token. `@lab.Title` in the introduction resolves to the hosted lab title.

## Lab resources

The four-hour path assumes the lab account, authoring environment, **Contoso IT** SharePoint site, **EmployeeAssets** list, and Outlook mailbox are prepared before the session. Attendees do not create subscriptions, buy credits, or administer tenant policies.

The [downloads folder](./downloads/README.md) contains the original sample documents and skills plus the evaluation and optional asset-analysis CSVs. The hosted VM should expose the original sample files under `D:\LabFiles\PREL36`. Download the evaluation CSV in section 7 and, if needed, the bonus CSV in section 9 from the repository to the VM's **Downloads** folder; neither requires a VM image update. If another VM file is missing, use the corresponding download link in the instructions, or ask your instructor.

> [!NOTE]
> Screenshots include Agent Academy assets, event captures, and cropped evaluation controls from LAB665. Sample tenant names, account names, and environments can differ from yours. Use the resources assigned to you, not values visible in screenshots.

## Delivery preparation

Instructors and Skillable authors: complete [Lab environment setup](../docs/Lab-Environment-Setup.md) before delivery. That document includes resource requirements, the list schema contract, source mapping, and the outstanding delivery checks. The four-hour path requires a working GitHub Copilot harness authoring experience and available Copilot Credits.

## Source and continued learning

Adapted from [Agent Academy Recruit NextGen](https://microsoft.github.io/agent-academy/recruit-nextgen/), source revision [`b9a562f`](https://github.com/microsoft/agent-academy/tree/b9a562f2505c4dd31c356dca0f01f45832f5707f/docs/recruit-nextgen). Original content and assets are copyright Microsoft Corporation and are reused under the [MIT license](./assets/LICENSE-Agent-Academy).

This event lab is a condensed adaptation, not the complete Recruit NextGen course. Tenant provisioning, extended theory, the intermediate device skill revision, optional email HTML styling, and the Academy badge submission are outside the timed attendee path. Completing PREL36 does not automatically award an Agent Academy badge.

Select **Next** to begin, or open [Introduction](./00-Introduction.md) when reading on GitHub.
