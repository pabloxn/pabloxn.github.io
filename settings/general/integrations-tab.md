---
description: This page is the setup for integrations
---

# Integrations \(Tab\)

## FireText

FireText is a third party service for the sending and receiving of SMS messages. It is used for the automatic communication by text to clients for confirmations and reminders. You will need to setup an account with them and they will supply the required key to use their services.

There are several fields to fill in as described below:

#### API Key 

This is the security key that is supplied by FireText and is required to enable this to function.

#### Scheduled Messages

This defines the scheduled SMS messages to sends. This area has two fields per section. The first field is for the [SMS template](../sms-templates.md) to be used and the second section defines the date calculation to work out when to send the message in relation to either the activation date or the appointment date. All the SMS messages are created on the creation of the appointment. The date calculations are further defined in [Date Calculation](../../technical-user-guides/date-calculations.md) section. The scheduled messages are:

1. **Confirmation** -  This is the initial message and is part of confirming the appointment the date calculation is in relation to creation of the appointment. 
2. **Reminder 1** - This is the first available reminder message and its send date is calculated related to the appointment date.
3. **Reminder 2** - This is the second available reminder message and its send date is calculated related to the appointment date.

