# Lab 1: Setting up and managing Pay-as-you-go billing in Microsoft 365 copilot

Create a Pay-as-you-go billing policy from scratch, then connect,
monitor, and retire it across its full lifecycle in the Microsoft 365
admin center.

|  |  |
|---|---|
| **Estimated duration** | 1 hour 30 minutes |
| **Level** | Intermediate |
| **Required role** | Global administrator or Billing administrator |
| **Environment** | Microsoft 365 test/lab tenant with an Azure subscription |

## Lab overview

You first build a policy from the ground up — billing details, user
scope, and an optional budget — then connect it to a Copilot service. In
the second half you manage that same policy: connecting a service after
the fact, adding a budget later, monitoring spend, and finally
disconnecting the service and deleting the policy.

Pay-as-you-go billing lets your organization pay only for the Copilot
Credits it consumes, using an Azure subscription as the billing
backbone. Working through the create-then-manage flow end to end gives
you a complete operational picture rather than an isolated setup task.

## What you will learn

- Create a **Pay-as-you-go billing** policy with billing details,
  subscription, resource group, and region.

- Scope a policy to all users or to a specific group.

- Set an optional budget with reset cadence and percentage-based
  spending alerts.

- Connect a **Pay-as-you-go** service to a policy — both during creation
  and afterward.

- Add a budget to a policy that was created without one.

- Monitor organizational spending in the admin center and in Microsoft
  Cost Management.

- Disconnect a service and delete a billing policy cleanly.

## Prerequisites

- Access to a Microsoft 365 test/lab tenant.

- An account with the Global administrator or Billing administrator
  role.

- An existing Azure subscription (or permission to create one) to
  associate with the policy.

- At least one security or distribution group in the tenant for policy
  scoping.

# Task 1 — Create a billing policy and add billing details

1.  Sign in to the **Microsoft 365 admin centre**
    [admin.microsoft.com](%3ca%20href=%22https:/login.microsoftonline.com/common/oauth2/authorize?client_id=00000006-0000-0ff1-ce00-000000000000&amp;response_type=code%20id_token&amp;scope=openid%20profile&amp;state=OpenIdConnect.AuthenticationProperties%3Dt6jMHseTkWXAad9AB7ThzZlS8WzT6LARlRE5VxRDYrtvO1MOLYRMJbbRyZuZDUz8F9NMKbz_lQZ_SCfNSpR9c7mxxoRN4WBCM9J5PRVNN1_7_bXrwh4oIDy9ICK8NRDbol14toaeC41zQEWIRZDC2DHOv-dbgACTJNYB2V_jsZmke4cTCsgqN_Y1YDWlXCHD2U--bp__RFqVNuRl4BsmOg&amp;response_mode=form_post&amp;nonce=639209129157633155.NDI4MjZjNGEtYzg3My00OWY4LWIyNWYtMmU0NDQ3YzUzNWU1MjQ2MzNmZTQtNDJhMi00NGFlLTk3MzQtYTBiZjE4MTM2Nzgx&amp;redirect_uri=https%3A%2F%2Fadmin.microsoft.com%2Flanding&amp;ui_locales=en-US&amp;mkt=en-US&amp;client-request-id=0ab614a7-a1b3-4682-9df2-d9494d40a0b6&amp;claims=%7B%22id_token%22%3A%7B%22xms_cc%22%3A%7B%22values%22%3A%5B%22CP1%22%5D%7D%7D%7D&amp;x-client-SKU=ID_NET472&amp;x-client-ver=8.19.2.0%22%3eSign%20in%20to%20your%20account%3c/a%3e)


    - **Email/Username:** <inject key="AzureAdUserEmail"></inject>

        ![](./media/b1.png)

	- **Password:** <inject key="AzureAdUserPassword"></inject>

        ![](./media/b2.png)

2. On the **Stay signed in?** prompt, click **No**
        ![](./media/b3.png)

3.  In **M365 admin centre** home page, go to **Copilot (1)** from left pane
    \> **Cost management (2)**

     ![](./media/b4.png)

4.  On the **Cost management** tab, select **classic Billing & usage**

    ![A screenshot of a computer AI-generated content may be
 incorrect.](./media/b5.png)

5.  On the **Billing & usage** page, select the **Billing policies (1)** tab, then click **+ Add a billing policy (2)** to create a new billing policy.

    ![](./media/b6.png)

6. On the **Billing details** page, enter **Copilot Chat PAYG - Pilot Group (1)** in the **Name** field, select the appropriate **Subscription (2)**, choose **ODL-Copilot-<inject key="AzureAdUserEmail"></inject> (3)** as the **Resource group**, select **East US (4)** as the **Region**, accept the pay-as-you-go billing terms of service **(5)**, and then click **Next (6)**.

    ![](./media/b7.png)

7. On the **Choose users** page, select **All users (1)** and then click **Next (2)** to continue.

    ![](./media/b8.png)

8. On the **Budget** page, select **Set a budget for this policy (1)**, enter **200 (2)** as the budget amount, keep **On the first day of the month (3)** selected as the reset schedule, and then click **Next (4)**.

    ![](./media/b9.png)

9. On the **Review and create policy** page, review the billing policy details and click **Create policy (1)** to create the policy.

    ![](./media/b10.png)

10. On the **New billing policy created** page, verify that the billing policy was created successfully and click **Done** to finish the setup process.

    ![](./media/b11.png)

# Task 2 — Connect a Pay-as-you-go service and monitor spending

1. On the **Billing & usage** page, select the **Pay-as-you-go services (1)** tab and then select **Microsoft 365 Copilot Chat (2)**.

    ![](./media/b12.png)

2. On the **Manage billing for Microsoft 365 Copilot Chat** page, enable the connection for the **Copilot Chat PAYG - Pilot Group** billing policy by turning on the **Connected (1)** toggle, and then click **Save (2)**.

    ![](./media/b13.png)

3. Verify that the **Billing policy connection(s) updated** message is displayed, confirming that the billing policy has been successfully connected to Microsoft 365 Copilot Chat.

    ![](./media/b14.png)

4. In the Microsoft 365 admin center, expand **Copilot (1)**, select **Cost management (2)**, and then click **classic Billing & usage (3)** to open the billing policy management page.

    ![](./media/b15.png)

5. On the **Billing & usage** page, select the **Billing policies (1)** tab and then choose the **Copilot Chat PAYG - Pilot Group (2)** billing policy.

    ![](./media/b16.png)

6. Review the billing policy details and verify that the policy information, subscription, resource group, and region are configured correctly.

    ![](./media/b17.png)

7. Select the **Budget (1)** tab to review the billing policy spending details and verify that the monthly spending chart **(2)** is displayed.

    ![](./media/b18.png)

8. Select the **Users (1)** tab and verify that the billing policy is assigned to **All users (2)**.

    ![](./media/b19.png)

9. Click **Close** from the top right corner to exit the pop-up.

# Task 3 — Disconnect a pay-as-you-go service and delete the policy

1. In the Microsoft 365 admin center, expand **Copilot (1)**, select **Cost management (2)**, and then click **classic Billing & usage (3)** to open the billing policy management page.

    ![](./media/b15.png)

2. On the **Billing & usage** page, select the **Pay-as-you-go services (1)** tab and then select **Microsoft 365 Copilot Chat (2)**.

    ![](./media/b20.png)

3. On the **Manage billing for Microsoft 365 Copilot Chat** page, turn off the **Connected (1)** toggle for the **Copilot Chat PAYG - Pilot Group** billing policy and then click **Save (2)**.

    ![](./media/b21.png)

4. Verify that the **Billing policy connection(s) updated** message is displayed, confirming that the billing policy has been successfully disconnected from Microsoft 365 Copilot Chat.

    ![](./media/b22.png)

5. On the **Copilot Chat PAYG - Pilot Group** billing policy page, click **Delete billing policy** to remove the billing policy.

    ![](./media/b23.png)

6. In the confirmation dialog, click **Delete** to permanently delete the billing policy.

    ![](./media/b24.png)

## Lab validation checklist

- A pay-as-you-go billing policy exists on the Billing policies tab with
  the name you chose.

- The policy is scoped correctly (All users or your specified group).

- A budget with a reset cadence and at least one alert threshold is
  attached to the policy.

- A Copilot service shows Connected against the policy on the
  Pay-as-you-go services tab.

- Spending data is visible on the Budget tab and (optionally) in
  Microsoft Cost Management.

- The service can be disconnected and the policy deleted without errors.

## Summary

You created a Microsoft 365 Copilot pay-as-you-go billing policy from
scratch — configuring billing details, user scope, and an optional
budget — and connected it to a Copilot service. You then managed that
policy end to end: connecting a service after creation, adding a budget
later, monitoring spend in both the admin center and Microsoft Cost
Management, and finally disconnecting the service and deleting the
policy. You now understand the complete pay-as-you-go billing lifecycle
in a single continuous workflow.
