---
description: Detailed description of the workflow for appointment notifications
---

# Appointment Notification \(AN\) Workflow

The appointment notification workflow is triggered when a 'video assesment' or 'video reassessment' appointment is created or edited and does the following;

* sends an SMS to the client
* sends an email confirmation to the Instructing Party \(IP\)
* sends an email confirmation to the client

## Components used in this workflow

* Appointment type - where the trigger is set
* Correspondence template - the emails sent to the IP and client
* SMS template - the SMS sent to the client
* Workflow template - the nested workflows that select the appropriate template
* Venue documents - directions or instructions for the "venue" attached to the client email
* Company documents - pre-assessment questionnaires attached to the client email

and requires the following data to be in inClinic;

* IP email address
* Client email address
* Client mobile number
* Client appointment \(with its component parts e.g. client, contacts \(payer\), case\)

## How it works

When you save a newly created or amend an appointment \(using the video re/assessment type\) you will be prompted...

![](../../../.gitbook/assets/image%20%2813%29.png)

Click on "Yes" to run the workflow.

The system will provide feedback on the successful completion of the elements of the workflow \(see below\) an amber box will appear if there is an error, which will require user action to dismiss.

![](../../../.gitbook/assets/image%20%2816%29.png)

If you click on "No" the worflow will not run and you will need to send the 3 items manually.

#### Manually Send SMS

1. open the SMS function - this opens a right hand margin interface
2. enter the client phone number at the top - this will load any prior messages
3. enter the message at the bottom
4. click the send icon

![sms function icon \(speech bubbles\)](../../../.gitbook/assets/image%20%2819%29.png)

![enter text and click the arrow to send](../../../.gitbook/assets/image%20%2817%29.png)

#### Manually Send IP Email

1. Go to the client record
2. Click on the 'create correspondence' icon - this will open the client communication dialogue
3. Select "AN IP Email" from the template drop down selection - this will display a pre-populated template - you can edit the text here
4. click on the "Email" button \(top right\) - this will open a pop-up 'send email' window where you can edit the email 'header' information \(from, to , cc, subject\) and add attachements
5. Click on "send" to send the email

![Create correspondence icon](../../../.gitbook/assets/image%20%2818%29.png)

#### Manually Send Client Email

1. Go to the client record
2. Click on the 'create correspondence' icon - this will open the client communication dialogue
3. Select the relevant template from the drop down selection e.g. AN Adult Assessment Email - you can edit the text here
4. Click on the "Email" button \(top right\) - this will open a pop-up 'send email' window where you can edit the email 'header' information \(from, to , cc, subject\) and remove and/or add attachements
5. Click on "send" to send the email

## How the workflow is structured

There are fundamentally four types of confirmation;

1. Adult Assessment
2. Child Assessment
3. Adult Reassessment
4. Child Reassessment

Step 1: Whether assessment or reassessment correspondence is sent is dictated by the appointment type use e.g. if you use a "video assessment" appointment type this will trigger the 'assessment' workflow \(rather than the 'reassessment' workflow\).

Step 2: the adult or child template is selected by a function in the workflow \(triggered by step 1\) that then triggers a subsequent workflow.

For example, the workflow "AN Assessment Adult or Child" \(triggered by the appointment creation\) will send the initial client SMS, the email to the IP then, depending on if the client is under 18 or not, will trigger the "AN Assessment Child Email" or "AN Assessment Adult Email" workflow which in turn sends the email confirmation to the client.

![Appointment Notification Workflows and Templates](../../../.gitbook/assets/image%20%2815%29.png)

## Workflows

The following workflows that are set as triggers in the appointment types.

* Video assessment - will trigger the workflow "AN Assessment Adult or Child"
* Video reassessment - will trigger the workflow "AN Reassessment Adult or Child"

### AN Assessment Adult or Child

This workflow will do the following;

* send an sms using the "AN Client SMS" sms template
* send an email using the "AN IP Email" correspondence template
* interrogates the age of the client;
  * if &lt;18 run the workflow "AN Child Assessment Email"
  * if not &lt;18 run the workflow "AN Adult Assessment Email"

#### AN Child Assessment Email

This workflow will send an email using the "AN Child Assessment Client Email" correspondence template.

#### AN Adult Assessment Email

This workflow will send an email using the "AN Adult Assessment Client Email" correspondence template.

### AN Reassessment Adult or Child

This will do the following;

* send an sms using the "AN Client SMS" sms template
* send an email using the "AN IP Email" correspondence template
* interrogates the age of the client;
  * if &lt;18 run the workflow "AN Child Reassessment Email"
  * if not &lt;18 run the workflow "AN Adult Reassessment Email"

#### AN Child Reassessment Email

This workflow will send an email using the "AN Child Reasessment Client Email" correspondence template.

#### AN Adult Reassessment Email

This workflow will send an email using the "AN Adult Reassessment Client Email" correspondence template.

## SMS Template

There is 1 SMS template used in this workflow "AN Client SMS".

**NB: For the SMS to be sent there must be a mobile number recorded in the Client / Details / Directory section**

The template has 2 fields from the client details, which is intended to promote the notion that the message is not SPAM. This will look something like this...

![example AN Client SMS message](../../../.gitbook/assets/image%20%2814%29.png)

To view the messages sent to a mobile number use the sms function icon in the top right of inClinic, enter the phone number and the messages sent to this number will show \(this may take a few seconds to load\).

## Correspondence Templates

There are 5 correspondence templates used in this workflow;

1. AN IP Email
2. AN Adult Assessment Client Email
3. AN Child Assessment Client Email
4. AN Adult Reassessment Client Email
5. AN Child Reassessment Client Email

### AN IP Email

This sends a generic confirmation of the appointment to the IP. This is used in all appointment notifications. It utilises appointment, case, clinic and clinician information. The email originates from "appointments@apsy.co.uk" \(as set in the Settings / Correspondence email setting\).

**NB: For the email to be sent there must be an email address recorded in the IP's Contact / Details / Directory section.**

There is currently no functionality to send to different contacts so all emails will go to only one email.

### AN Client Email

This sends an email confirmation of the appointment to the client. It utilises client, appointment, case, clinic, and clinician information. The email originates from  "appointments@apsy.co.uk".

**NB: For the email to be sent there must be an email address recorded in the Client / Details / Directory section.**

The email has attached the 'venue docs' and the appropriate pre-interview questionnaire.

The client email varies only slightly in the wording \(assessment or reassessment\) or to who it is addressed \(to the parent/guardian in the case of &lt;18 yo clients\), but each template has a different pre-assessment questionnaire associated with it e.g. the AN Adult Assessment Client Email" correspondence template has the "APS Adult Pre-Interview Questionnaire\_adult\_first.docx" questionnaire.

**NB: if there is an attachment set in the template but the document has been removed or does not exist the workflow will not operate.**

## Documents

### Venue docs

The appointment's venue will determine which documents are attached to the AN Client Email. The document \(or documents\) uploaded to the relevant Venue / Documents section will be attached. If there is more than one document all documents will be attached.

For video assessments this will be a 'Client Zoom Guide' and 'Video Link Assessment Information'.

**NB: as the venue has Zoom specific information it is not suitable for non-Zoom appointments e.g. WhatsApp.**

#### **Assessment Questionnaires**

The assessment questionnaire is stipulated in the template and the document is stored in the Settings / Company / Documents section.

![examples of documents stored in the Company documents](../../../.gitbook/assets/image%20%2811%29.png)

When adding a new document for it to be available to select in an email going to a client the 'Use with' field must be set to 'Client' in the company documents.

**NB: If you replace a company document in the company / documents section be sure to re-attach the file to the relevant template\(s\) otherwise the workflow will not operate.**

