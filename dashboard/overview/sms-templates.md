---
description: >-
  This is a list of template for SMS messages and is used for automated message
  creation and sending.
---

# SMS Templates

## What are SMS templates?

SMS templates are a list of templates that are used to create messages to clients either manually or via an event occurring. You can assign SMS templates to activate when a appointment is created or via the SMS chat sidebar. You can also set a message to arrive in the future. You will need to make sure that the FireText section in [integrations ](general/integrations-tab.md#firetext)is set up to use this functionality.

{% hint style="info" %}
SMS templates can create useful reminders and confirmations to your clients without the user having to enter them.
{% endhint %}

## How do I create an SMS template?

1. Under settings choose 'SMS Templates'
2. Click the ![](../../.gitbook/assets/screenshot-2019-01-23-at-13.22.51.png)Add button and you will the SMS Template Form.
3. You will need to give the template a name, preferably something that is meaningful to its purpose.
4. \[optional\] If you want to send a delayed message \(A message that will arrive in the future\) then you will need to set the  date anchor and date formula fields. To calculate when the message will be sent we need to define when we are calculating from and how long from that point. 
   1. Select the 'Date Anchor' which defines when the calculation is going to be base from. There are two options \[Start and End\]. The Start will define starting the calculation from the start of an event \(e.g. When an appointment was created\) or the end of an event \(e.g. When the appointment happened\).
   2. Enter the formula to calculate the date. These date formulas are defined in the[ Date Calculations](../../technical-user-guides/date-calculations.md) section. \(e.g. +1D with start would send a message a day after the appointment was created. or -5D with end would send a message 5 days before the appointment\).
5. Then you can create the message with the addition of being able to add place holders for record details. To do this click  'Add Field' and then select the field you want. The fields menu will insert field holders at the cursor. These fields will be filled in when the message is created from the template. See [Data Dictionary](../../technical-user-guides/data-dictionary.md) for further guidance. If you are familiar with 'Mail Merge' in Microsoft Office Word then it preforms a similar task.
6. Once you have added the required data then click the ![](../../.gitbook/assets/screenshot-2020-01-31-at-10.47.16.png) Save button and you will be taken back to the list.

### How do I edit an SMS Template?

1. Under settings choose 'SMS Templates'
2. Click the entry in the list that you want to edit.
3. Follow steps 3 to 6 above.

