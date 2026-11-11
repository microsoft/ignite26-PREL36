# 1 - Create a solution

A Power Platform solution groups related components so they can move together between environments. You'll work in an **unmanaged** solution for development. A **publisher** identifies component ownership and supplies a prefix.

## Log in

1. Open Microsoft Edge Browser (the Internet icon on the VM desktop) in your virtual machine and go to +++https://copilotstudio.microsoft.com+++.
1. Sign in with the username and TAP from the **Resources** tab.
1. Select the environment dropdown in the bottom left-hand corner and choose the **Dev One** environment.

    ![Select the assigned Power Platform environment](./assets/01.1-select-environment.png)

## Create the publisher

1. Open a new tab and go to +++https://make.powerapps.com+++.
1. Select **Get started** if you see this **Welcome to Power Apps** screen.

    ![Select the assigned Power Platform environment](./assets/01.2-get-started.png)

1. Select the **Environment** picker in the **upper right-hand corner** and switch to the **Dev One** environment.

    ![Select the assigned Power Platform environment](./assets/01.3-switch-environment.png)

1. Select the **Solutions** tab in the **left navigation**.

    ![Open Solutions in Copilot Studio](./assets/01.2-select-solution-tab.png)

1. In **Solution Explorer**, select **+ New solution**.

    ![Create a new solution](./assets/01.4-new-solution.png)

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
1. Confirm that **Contoso Solutions** is selected in the **Publisher** dropdown in **New solution** pane.

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

    If a different solution is shown, select **Set preferred solution**, choose **Contoso IT Concierge Agent**, and select **Apply**. Skip this action if the correct solution is already preferred.

1. Close the Power Apps tab and return to the tab with Copilot Studio.

Select **Next** to build the agent.
