---
ms.localizationpriority: medium
description: If your organization has its own email server (also called on-premises server), you must set up connectors to enable mail flow between Microsoft 365 or Office 365 and your email server. For mail flow to work correctly, your connectors must be validated and turned on. Connector validation runs as part of the connector setup process. This article helps if you want to validate your connectors at a different time, or if you want to understand more about the process. Use built-in connector validation to test whether a connector is set up correctly and fix any mail flow issues before you turn the connector on.
ms.topic: article
author: JoanneHendrickson
ms.author: jhendr
ms.assetid: 7805c2f9-302d-4409-a57f-2b4d8296cd5e
ms.reviewer: 
f1.keywords:
- NOCSH
title: Validate connectors in Exchange Online
ms.collection: exchange-online
audience: ITPro
ms.service: exchange-online
manager: serdars

---

# Validate connectors in Exchange Online

If your organization has its own email server (also called on-premises server), you must set up connectors to enable mail flow between Microsoft 365 or Office 365 and your email server. For mail flow to work correctly, your connectors must be validated and turned on. Connector validation runs as part of the connector setup process. This article helps if you want to validate your connectors at a different time, or if you want to understand more about the process. Use built-in connector validation to test whether a connector is set up correctly and fix any mail flow issues before you turn the connector on.

> [!NOTE]
> If you want to change connector settings, Microsoft 365 or Office 365 uses the existing connector settings for mail flow until you save your changes. For more information, see [Change a connector that Microsoft 365 or Office 365 is using for mail flow](set-up-connectors-to-route-mail.md#change-a-connector-that-microsoft-365-or-office-365-is-using-for-mail-flow)

## Validate and turn on connectors

This section describes the procedures to validate and turn on connectors in both the New Exchange admin center (EAC) and Classic EAC.

Before validating and turning on the connectors, sign in to Microsoft 365 or Office 365, choose **Admin**, and then select **Exchange** to go to the New EAC.

> [!NOTE]
> To navigate to Classic EAC, you need not seperately launch its URL. You can navigate from New EAC interface by clicking **Classic Exchange admin center** on the left-bottom.

 **For New EAC**

1. Navigate to **Mail flow > Connectors**. The **Connectors** screen appears.

> [!NOTE]
> Any Microsoft 365 or Office 365 connectors that exist for your organization are listed on the **Connectors** page. This list includes connectors that were created by using the Hybrid Configuration Wizard or PowerShell. You can validate any connector configured for mail flow from Microsoft 365 or Office 365 to your organization's email server, or to a partner organization.

2. Choose and click the connector you want to validate or turn on.

:::image type="content" source="../../media/connector-chosen-in-new-eac.png" alt-text="The screen of New EAC on which the user chooses a connector for viewing its details.":::

3. Click the connector. The connector details screen appears.

4. View the information.

:::image type="content" source="../../media/display-of-validation-details.png" alt-text="The screen on which the validation history details for the connector is displayed.":::

When you select a connector for mail flow that originates in Microsoft 365 or Office 365, you can choose the **Validate this connector** link. You can also see whether the connector was validated previously as shown in the following screenshot.

:::image type="content" source="../../media/connector-validation-link.png" alt-text="The screen on which the link that enables connector validation is displayed.":::

5. Under **Status**, if **Off** is displayed, click **Edit name or status**. The **Connector name** screen appears.

6. Under **What do you want to do after connector is saved**, check the check box for **Turn it on**.

7. Click **Next**. The **Validation email** screen appears.

8. Enter an email address that is part of the active mailbox on your organization's email server.

9. Click **+**, and then click **Validate**. The validation process starts.

10. Once the validation process is completed, click **Save**.

The connector is updated successfully from **being turned off** to **being turned on**.

**For Classic EAC**

1. Navigate to the Classic EAC portal by clicking **Classic Exchange admin center**. Select **mail flow** and then **connectors**.

   Any Microsoft 365 or Office 365 connectors that exist for your organization are listed on the **Connectors** page. This includes connectors that were created by using the Hybrid Configuration Wizard or PowerShell. You can validate any connector configured for mail flow from Microsoft 365 or Office 365 to your organization's email server, or to a partner organization.

2. Choose the connector you want to validate or turn on. You can see information about the connector in the details pane as shown in the following screen shot.

   ![Shows a connector from Microsoft 365 or Office 365 to an Exchange Server that is turned off and has failed validation.](../../media/94d4c6ed-70d0-4a1d-915b-9d089f58d714.png)

3. When you select a connector for mail flow that originates in Microsoft 365 or Office 365, you can choose the **Validate this connector** link. You can also see whether the connector was validated previously as shown in the following screen shot.

   ![Shows a connector that was previously validated and a link to validate the connector again.](../../media/e563a5dd-5e3c-4e78-8d3b-1e4b05a8e5d1.png)

4. With the connector selected, choose **Validate this connector**. The **Validate this connector** dialog box opens. Enter one or more email addresses to start the validation. Microsoft 365 or Office 365 uses these addresses to make sure your mail flow is set up correctly. For example, if you want to validate a connector for mail flow from Microsoft 365 or Office 365 to your organization's email server, enter an email address for a mailbox located on that email server.

5. Choose **Validate** to continue. To find out what issues validation examines, and for details about fixing any validation errors, see [Validate connectors](validate-connectors.md).

6. For each connector, check whether the connector is turned on. If a connector that you need for mail flow isn't turned on, under **Status** choose **Turn it on**.

> [!NOTE]
> If you continue to have mail flow issues after validating a connector, check whether you have set up multiple connectors that might apply in a single scenario. For example, problems can occur if you have more than one connector set up for mail flow from Microsoft 365 or Office 365 to your email server. If you need multiple connectors for mail flow from Microsoft 365 or Office 365 to your email server (or to a partner), ensure you validate and turn on each connector. If you want to change a connector, Microsoft 365 or Office 365 uses the existing connector settings for mail flow until you save your changes. For more information, see [Change a connector that Microsoft 365 or Office 365 is using for mail flow](set-up-connectors-to-route-mail.md#change-a-connector-that-microsoft-365-or-office-365-is-using-for-mail-flow)
 
## See also

[Set up connectors to route mail between Microsoft 365 or Office 365 and your own email servers](set-up-connectors-to-route-mail.md)

[Configure mail flow using connectors](use-connectors-to-configure-mail-flow.md)

[Validate connectors](validate-connectors.md)

[When do I need a connector?](use-connectors-to-configure-mail-flow.md#when-do-i-need-a-connector)
