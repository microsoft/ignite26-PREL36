# PREL36: Build your first agent in Copilot Studio

These are the attendee instructions for the four-hour Microsoft Ignite 2026 pre-day lab. You will build **Contoso IT Concierge**, an IT support agent powered by the **GitHub Copilot harness** in Microsoft Copilot Studio.

The agent answers grounded IT questions, retrieves current devices from SharePoint, follows reusable skills, and calls a workflow to email a confirmed device request. Sending a request is not approval, procurement, or a stock reservation.

## Four-hour agenda

The schedule includes **220 minutes of instruction and hands-on work plus two 10-minute breaks**. Times are delivery estimates, not measured completion times. Complete the sections in order; each extends the same agent.

| Elapsed time | Section | Minutes |
| --- | --- | --- |
| 00:00-00:20 | [Introduction, sign-in, and agent fundamentals](./00-Introduction.md) | 20 |
| 00:20-00:35 | [Create a solution](./01-Create-A-Solution.md) | 15 |
| 00:35-01:15 | [Build and ground the agent](./02-Build-And-Ground-The-Agent.md) | 40 |
| 01:15-01:35 | [Add the SharePoint tool](./03-Add-The-SharePoint-Tool.md) | 20 |
| 01:35-01:45 | Break | 10 |
| 01:45-02:25 | [Add and refine skills](./04-Add-And-Refine-Skills.md) | 40 |
| 02:25-02:35 | Break | 10 |
| 02:35-03:25 | [Build the device-request workflow](./05-Build-The-Device-Request-Workflow.md) | 50 |
| 03:25-03:45 | [Test the solution end to end](./06-Test-End-To-End.md) | 20 |
| 03:45-04:00 | [Publish and plan for operation](./07-Publish-And-Wrap-Up.md) | 15 |

## Learning outcomes

By the end of the lab, you will be able to:

- Build a scoped, instruction-driven agent and ground its answers in approved knowledge.
- Connect a live SharePoint tool and reusable skills that guide reliable device selection.
- Call a workflow after confirmation, verify successful and cancelled requests, and publish the agent to an employee channel.

## Skillable conventions

Open the **Resources** panel for your assigned virtual machine credentials, Microsoft 365 account, Power Platform environment, SharePoint site URL, and lab email address. Use only your assigned lab resources.

Text surrounded by `+++` becomes clickable autotype text in Skillable. Multiline prompts and instructions appear in fenced text blocks for copying. Select the destination field before using autotype or pasting.

> [!IMPORTANT]
> Wait for autotype to finish before interacting with the virtual machine. Do not paste VM credentials into Microsoft 365 sign-in fields. Use the appropriate credentials from **Resources**.

No event-specific `@lab.CloudCredential(...)` or `@lab.Variable(...)` identifier is assumed in this version. The delivery team must map resource values to its actual Skillable profile before enabling additional dynamic autotype fields. `@lab.Title` in the introduction resolves to the hosted lab title.

## Lab resources

The four-hour path assumes the lab account, authoring environment, **Contoso IT** SharePoint site, **EmployeeAssets** list, and Outlook mailbox are prepared before the session. Attendees do not create subscriptions, buy credits, or administer tenant policies.

The [downloads folder](./downloads/README.md) contains the original sample documents and skills. The hosted VM should expose the same folder structure under `D:\LabFiles\PREL36`. If a VM file is missing, use the corresponding download link in the instructions, or ask your instructor.

> [!NOTE]
> Screenshots are reused from Agent Academy. Sample tenant names, account names, and environments can differ from yours. Use the resources assigned to you, not values visible in screenshots.

## Delivery preparation

Instructors and Skillable authors: complete [Lab environment setup](../docs/Lab-Environment-Setup.md) before delivery. That document includes resource requirements, the list schema contract, source mapping, and the outstanding delivery checks. The four-hour path requires a working GitHub Copilot harness authoring experience and available Copilot Credits.

## Source and continued learning

Adapted from [Agent Academy Recruit NextGen](https://microsoft.github.io/agent-academy/recruit-nextgen/), source revision [`b9a562f`](https://github.com/microsoft/agent-academy/tree/b9a562f2505c4dd31c356dca0f01f45832f5707f/docs/recruit-nextgen). Original content and assets are copyright Microsoft Corporation and are reused under the [MIT license](./assets/LICENSE-Agent-Academy).

This event lab is a condensed adaptation, not the complete Recruit NextGen course. Tenant provisioning, extended theory, the intermediate device skill revision, optional email HTML styling, and the Academy badge submission are outside the timed attendee path. Completing PREL36 does not automatically award an Agent Academy badge.

Select **Next** to begin, or open [Introduction](./00-Introduction.md) when reading on GitHub.
