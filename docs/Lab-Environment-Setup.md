# PREL36 lab environment setup

This document is for instructors, environment preparers, and Skillable authors. It is not part of the timed learner path.

## Delivery status

This package adapts existing Agent Academy instructions and screenshots. Its **240-minute agenda is a planning estimate**. It has not been run end to end in the PREL36 event tenant or imported into the event's Skillable profile. Do not treat source screenshots or static Markdown checks as evidence of live tenant validation.

Before delivery, rehearse the full learner path in a fresh assigned account, verify timings with representative beginners, and resolve the checklist below. No tenant IDs, credential IDs, or provisioned services are invented by these instructions.

## Required resources per learner

| Resource | Required state before the session |
| --- | --- |
| Skillable VM | Browser and File Explorer available; learner can sign in |
| Microsoft 365 account | SharePoint, Outlook mailbox, and employee channel access |
| Power Platform environment | Dataverse available; learner can create solutions, publishers, agents, connector connections, and workflows |
| Copilot Studio | GitHub Copilot harness authoring surface enabled and available in the assigned environment |
| Capacity and policies | Available Copilot Credits; required authoring and publishing permissions; SharePoint and Office 365 Outlook connectors permitted |
| SharePoint site | Contoso IT site using the IT help desk template, with the support content used by the learner tests |
| SharePoint list | EmployeeAssets populated from the original workbook with the schema contract below |
| Employee channel | Teams + Microsoft 365 channel can be added; learner can install and test in at least Teams |
| Lab files | Contents of `instructions/downloads/` staged under `D:\LabFiles\PREL36` |

Use isolated learner environments and learner-owned sites/lists, or otherwise prevent participants from editing each other's solutions and test records. Confirm both the template support content, including Contoso VPN guidance, and the supplied Wi-Fi document are appropriate for the event tenant.

Do not pre-create the learner agent, solution, skills, or workflow in the baseline: attendees create those during the lab.

## Skillable profile and resources

1. Set the lab title to **PREL36: Build your first agent in Copilot Studio** for Microsoft Ignite 2026.
1. Expose these resource values clearly: VM credentials, Microsoft 365 credentials or Temporary Access Pass, assigned Power Platform environment name, Contoso IT SharePoint site URL, and lab email address.
1. Map the supplied resource names to the actual Skillable profile. No `AITour27M365E7` or guessed Ignite credential ID is embedded here.
1. Import learner pages in this exact order:

    ```text
    instructions/00-Introduction.md
    instructions/01-Create-A-Solution.md
    instructions/02-Build-And-Ground-The-Agent.md
    instructions/03-Add-The-SharePoint-Tool.md
    instructions/04-Add-And-Refine-Skills.md
    instructions/05-Build-The-Device-Request-Workflow.md
    instructions/06-Test-End-To-End.md
    instructions/07-Publish-And-Wrap-Up.md
    ```

1. Make the relative `assets/` and `downloads/` folders available to the hosted instructions, or update the platform's asset mappings without changing filenames.
1. Verify the actual Skillable renderer supports the used headings, tables, numbered lists, fenced text blocks, `> [!NOTE]`/`> [!IMPORTANT]` callouts, `+++` autotype spans, and `@lab.Title`. The package follows LAB665's Markdown conventions; it does not use VitePress frontmatter, Vue components, or `:::` containers.
1. Test autotype with URLs and short field values. Multiline text blocks are deliberately copy/paste, not unverified dynamic credential expansions.
1. Stage all downloads and verify upload behavior for standalone `SKILL.md` files.

## Prepare the Contoso IT site

Use the original [Recruit NextGen course setup](https://github.com/microsoft/agent-academy/blob/b9a562f2505c4dd31c356dca0f01f45832f5707f/docs/recruit-nextgen/00-course-setup/index.md#step-5-create-new-sharepoint-site) as the detailed provisioning reference.

1. Create a **Team site** from the **IT help desk** template.
1. Set the site name to **Contoso IT** and, where available, the site address to **ContosoIT**. If provisioning changes the URL, surface the real URL in the learner's **Resources** panel.
1. Verify that the template's support pages are present, especially the Contoso VPN material used in the knowledge test.
1. On the site, select **+ New** > **List**.
1. Under **Import from**, select **Excel**.
1. Upload [EmployeeAssets.xlsx](../instructions/downloads/setup/EmployeeAssets.xlsx).
1. Select the **EmployeeAssets** table.
1. During import, configure:

    | Column | Type |
    | --- | --- |
    | Status | Choice |
    | Manufacturer | Choice |
    | Asset Type | Choice |
    | Color | Choice |
    | Purchase Date | Date and time |
    | Purchase Price | Number |

1. Name the list **EmployeeAssets** and create it.
1. Add **Image URL** as a **Hyperlink** column.
1. In **Edit in grid view**, copy the four source **Image** URLs into their corresponding **Image URL** cells.
1. Verify all four URLs and model/row associations before deleting the original single-line text **Image** column. Only remove that imported sample column, not a site library or an unrelated field.
1. Verify the source device image URLs resolve. If event policy requires event-hosted images, host the supplied images in an accessible location and update only the hyperlink values.

## Required list schema contract

The source skills contain explicit internal SharePoint column names. Import behavior can vary; display names alone do not prove that the list matches.

| Column display name | Internal name expected by the skills | Type |
| --- | --- | --- |
| Status | `field_1` | Choice |
| Manufacturer | `field_2` | Choice |
| Model | `field_3` | Single line of text |
| Asset Type | `field_4` | Choice |
| Color | `field_5` | Choice |
| Image URL | Verify in the prepared list | Hyperlink |

The skills call **Asset Type** "Device Type" in their mapping prose, but query `field_4`. Do not create a second column solely to match that wording.

Open **List settings**, select each column, and inspect the `Field` URL parameter to verify the real internal name. If it differs, update every affected mapping/example in both `device-guidance-v1-0-3/SKILL.md` and `device-guidance-v1-0-4/SKILL.md`, and update the learner mapping table. Preserve the source authorship and license metadata. Do not ship a mismatch as an expected learner failure.

Verify the prepared catalog has enough available laptop options for the sample tests. Learners select letters from the actual returned table rather than assuming a specific model is always option A.

## Runtime contracts to preserve

| Component | Required name or behavior |
| --- | --- |
| Agent | Contoso IT Concierge |
| Solution | Contoso IT Concierge Agent |
| Inventory tool | Get Employee Assets, fixed to the assigned site and EmployeeAssets |
| Troubleshooting skill | `troubleshooting-procedure` |
| Device skill progression | `device-guidance-v1-0-1` -> `device-guidance-v1-0-3` -> `device-guidance-v1-0-4` |
| Workflow tool | Send device request email |
| Workflow text inputs | `sharepointItemId`, `additionalComment`, `requestorName` |
| Workflow text output | `ModelValue`, mapped to the selected device's Model |
| Requester | Authenticated `User.DisplayName`, with `User.Email`/`User.PrincipalName` fallback; never invented |
| Email recipient | The learner's lab mailbox, not an actual manager |
| Side-effect boundary | Explicit confirmation before calling the email workflow |

The stock final skill says the manager will review the request. In this event, the learner's own mailbox simulates that manager. The learner instructions and published listing make this explicit. There is no approval action, purchase, or reservation in the workflow.

## Source mapping and four-hour adaptations

Source: [Agent Academy Recruit NextGen](https://github.com/microsoft/agent-academy/tree/b9a562f2505c4dd31c356dca0f01f45832f5707f/docs/recruit-nextgen), revision `b9a562f2505c4dd31c356dca0f01f45832f5707f`.

| Academy material | PREL36 treatment |
| --- | --- |
| 00 Course setup | Provisioned before the event; attendees verify access |
| 01 Introduction to agents and 02 Fundamentals | Condensed into the introduction and just-in-time explanations |
| 03 Creating a solution | Focus on publisher, unmanaged solution, and preferred solution |
| 04 Build a custom agent | Keep creation, instructions, four knowledge sources, and baseline tests |
| 05 Add tools | Keep fixed-resource SharePoint connector and add an explicit live-data check |
| 06 Add skills | Compare v1.0.1 with v1.0.3; omit a separate v1.0.2 upload; keep troubleshooting |
| 07 Workflows | Keep input/output contract, Get item, email, confirmation, and cancellation; omit optional HTML styling |
| 08 Publish | Configure the listing and test Teams; second-channel test is an extension |
| 09 Licensing | Condense to usage principles and authoritative references; no pricing exercise |
| Badge submission | Link to the full Academy path; do not award a badge for this condensed lab |

Retain the [MIT license copy](../instructions/assets/LICENSE-Agent-Academy) with the reused screenshots, documents, workbook, images, and skill files. Source asset bytes are preserved; event screenshots still need to be verified against the actual tenant.

## Delivery rehearsal checklist

- [ ] Start with a fresh learner account and confirm every Resources value is correct.
- [ ] Confirm the learner can create and prefer the custom solution.
- [ ] Verify GitHub Copilot harness creation, credit capacity, connector consent, and policy access.
- [ ] Verify all four knowledge sources complete processing and support the warranty, VPN, and guest Wi-Fi tests.
- [ ] Confirm EmployeeAssets column mappings and at least two selectable laptop options.
- [ ] Verify both the explicit version checks and natural-language skill routing.
- [ ] Check authenticated requester identity is present in Preview and the employee channel.
- [ ] Verify workflow input types, output value, and event-tenant email sensitivity policy.
- [ ] Confirm no email before confirmation and no workflow submission or email on cancellation.
- [ ] Confirm successful emails contain the correct selected item, requester, and requirement.
- [ ] Verify publication and installation policies, and run an employee-channel live-data test.
- [ ] Confirm local downloads, screenshots, autotype, navigation, and final Submit behavior in Skillable.
- [ ] Rehearse the 220-minute learner path plus two 10-minute breaks; adjust the delivery estimate if needed.
