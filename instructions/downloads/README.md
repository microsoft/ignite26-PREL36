# PREL36 lab downloads

The sample documents, catalog, images, and skills are copied from Agent Academy Recruit NextGen. The evaluation CSV is authored for PREL36 using those lab resources. In the Skillable VM, preserve the original sample file layout under `D:\LabFiles\PREL36`. For example, this folder's `skills\device-guidance-v1-0-3\SKILL.md` becomes `D:\LabFiles\PREL36\skills\device-guidance-v1-0-3\SKILL.md`. Download the evaluation CSV from the repository to the VM's **Downloads** folder during section 7; it does not require a VM image update.

| File | Use |
| --- | --- |
| [Guest Wi-Fi guide](./knowledge/Contoso_Guest_WiFi_Connection_Guide.docx) | Learner knowledge upload |
| [Initial device skill](./skills/device-guidance-v1-0-1/SKILL.md) | First skill test |
| [Refined device skill](./skills/device-guidance-v1-0-3/SKILL.md) | Column mappings and additional requirements |
| [Workflow-enabled device skill](./skills/device-guidance-v1-0-4/SKILL.md) | Confirmation and workflow submission |
| [Troubleshooting skill](./skills/it-troubleshooting-procedure/SKILL.md) | Reusable IT troubleshooting |
| [Contoso IT Concierge baseline evaluation](./evaluation/Contoso-IT-Concierge-Baseline.csv) | Seven conversations for the pre-publish evaluation lab |
| [EmployeeAssets workbook](./setup/EmployeeAssets.xlsx) | Delivery-team list provisioning, not a learner import |
| [Device images](./setup/device-images/) | Delivery-team copies of the sample catalog images |

For a single file on GitHub, open its link, then use **Download raw file**. Do not save the GitHub HTML preview as `SKILL.md`, `.docx`, `.xlsx`, or `.csv`. Keep each skill in its own folder.

Import the evaluation CSV as **Conversations**, not **Single responses**. Its header is `conversationNumber,question,response`; repeated conversation numbers group follow-up turns. It has seven conversations and nine question/response rows. The reference responses describe the unchanged sample catalog and Wi-Fi guide; **General quality** does not compare actual answers against them. Follow the [evaluation lab](../07-Review-And-Evaluate.md) for the required factual, tool, and no-email evidence checks.

The skill names and workflow input/output names are intentionally preserved from the source, because they form the runtime contract. They are not event codes. Original license and author metadata remain in the skills; see the [Agent Academy MIT license](../assets/LICENSE-Agent-Academy).
