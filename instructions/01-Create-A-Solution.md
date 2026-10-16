# 1 - Create a solution

**Estimated time:** 15 minutes

A Power Platform solution groups related components so they can move together between environments. You will work in an **unmanaged** solution for development. A **publisher** identifies component ownership and supplies a prefix.

## Create the publisher

1. Confirm that Copilot Studio is using your assigned lab environment.
1. From the left navigation, select the **ellipsis** near the bottom, then select **Solutions** under **Explore**.

    ![Open Solutions in Copilot Studio](./assets/03-select-solutions-in-copilot-studio-navigation.png)

1. In **Solution Explorer**, select **+ New solution**.

    ![Create a new solution](./assets/03-select-new-solution-in-solution-explorer.png)

1. In the **New solution** pane, select **+ New publisher**.

    ![Create a solution publisher](./assets/03-select-new-publisher-for-the-solution.png)

1. On **Properties**, enter the following values:

    | Field | Value |
    | --- | --- |
    | Display name | +++Contoso Solutions+++ |
    | Name | +++ContosoSolutions+++ |
    | Description | +++Microsoft Ignite 2026 PREL36+++ |
    | Prefix | +++cts+++ |
    | Choice value prefix | Keep the automatically generated value |

    ![Configure the custom publisher](./assets/03-configure-the-custom-solution-publisher-properties.png)

1. Select **Save**.
1. Confirm that **Contoso Solutions** is selected in the **New solution** pane.

> [!NOTE]
> If your assigned environment already contains the publisher, reuse it rather than creating a duplicate. Do not modify a publisher owned by another lab participant.

## Create and prefer the solution

1. Enter the following values:

    | Field | Value |
    | --- | --- |
    | Display name | +++Contoso IT Concierge Agent+++ |
    | Name | +++ContosoITConciergeAgent+++ |
    | Version | `1.0.0.0` |
    | Publisher | `Contoso Solutions` |

1. Select **Set as your preferred solution**. This keeps newly created components in the intended solution.

    ![Set the custom solution as preferred](./assets/03-configure-the-new-solution-details.png)

1. Leave optional fields under **More options** blank.
1. Select **Create**.
1. After the empty solution opens, select the **back arrow** to return to Solution Explorer.
1. Confirm that **Contoso IT Concierge Agent** appears as the **Current preferred solution**.

    ![Verify the current preferred solution](./assets/03-preferred-solution-now-the-newly-created-solution.png)

**Verify:** Your custom solution exists and is preferred before you create the agent. If you cannot create solutions, ask your instructor to check your assigned environment role.

Select **Next** to build the agent, or open [Build and ground the agent](./02-Build-And-Ground-The-Agent.md).
