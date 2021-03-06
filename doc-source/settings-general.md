# General Settings<a name="settings-general"></a>

Use the **General settings** page to specify when Amazon Pinpoint can send messages for campaigns in the current project and how many messages Amazon Pinpoint can send for those campaigns\. This includes settings such as the time frame for sending messages and the maximum number of messages to send to a certain endpoint\. You can also use the **General settings** page to delete a project\.

**Topics**
+ [Configuring Default Settings for Campaigns](#settings-general-campaigns)
+ [Deleting a Project](#settings-general-delete-project)

## Configuring Default Settings for Campaigns<a name="settings-general-campaigns"></a>

You can choose several settings to specify when messages can be sent for campaigns in the current project, and the maximum number of messages that can be sent by default for those campaigns\. After you choose these settings, Amazon Pinpoint applies the settings automatically to any new campaigns that you create for the project\. The settings aren't applied to any campaigns that you previously created, and you can change the settings for a specific campaign at any time\.

**To configure default settings for campaigns**

1. Open the Amazon Pinpoint console at [https://console\.aws\.amazon\.com/pinpoint/](https://console.aws.amazon.com/pinpoint/)\.

1. On the **All projects** page, choose the project that you want to change the default settings for\.

1. In the navigation pane, under **Settings**, choose **General settings**\.

1. Choose **Edit**\.

1. On the **Edit general settings** page, change any of the following settings:
   + **Quiet time** – Change these settings to prevent Amazon Pinpoint from sending campaign messages during specific hours\. When you configure this setting, you provide a start time and an end time that define the time frame when you don't want to send any messages for campaigns\. The times that you specify have to use 24\-hour notation and be in HH:MM format\.
   + **Max daily messages per endpoint** – Specify the maximum number of messages that a campaign can send to a single endpoint during a 24\-hour period\. The value that you specify can't be larger than 100\.
   + **Max campaign messages per endpoint** – Specify the maximum number of messages that a campaign can send to a single endpoint\. The value that you specify can't be larger than 100\.
   + **Max messages per second** – Specify the maximum number of messages that a campaign can send each second\. The value that you specify has to be at least 50 and can't be larger than 20,000\.
   + **Max campaign run time** – Specify the maximum amount of time, in seconds, during which a campaign can attempt to deliver a message after the scheduled delivery time\. The minimum value for this setting is 60 seconds\.

1. When you finish making changes, choose **Save**\.

## Deleting a Project<a name="settings-general-delete-project"></a>

If you want to remove a project from Amazon Pinpoint completely, you can delete the project by using the Amazon Pinpoint console\.

**Warning**  
If you delete a project, Amazon Pinpoint deletes all project\-specific settings, campaigns, and other information for the project\. The information can't be recovered\.

When you delete a project, Amazon Pinpoint deletes all project\-specific settings for the push notification and two\-way SMS messaging channels, and all segments, campaigns, and project\-specific analytics that are stored in Amazon Pinpoint, such as the following:
+ Segments – All segment settings and data\. For dynamic segments, this includes segment groups and filters that you defined\. For imported segments, this includes endpoints, user IDs, and other data that you imported, and any filters that you applied\.
+ Campaigns – All messages, message treatments, message templates and variables, schedules, analytics, and other settings\.
+ Analytics – For campaigns, this includes all engagement metrics, such as the number of endpoints targeted, the number of messages sent, and delivery rates\. For mobile and web apps, this includes all event data that wasn’t streamed to another AWS service such as Amazon Kinesis, all funnels, and all application usage, revenue, and demographic metrics\. Before you delete a project, we recommend that you export this data to another location\. For more information, see [Exporting Dashboards](analytics-charts.md#analytics-exporting)\.

Note that account\-level settings and data for your Amazon Pinpoint account and your AWS account aren't deleted\. This includes:
+ Production access and sending limits for channels\.
+ Dedicated phone numbers for sending SMS and voice messages, and for receiving SMS messages\.
+ Verified identities for sending email and SMS messages\.
+ SMS information such as short codes, long codes, keywords, and registered sender IDs for sending SMS messages\.
+ SMTP credentials and other settings for sending email by using the Amazon Pinpoint SMTP interface\.

In addition, data that's stored in other AWS services isn't deleted\. This includes event data that you streamed to other AWS services such as Amazon Kinesis, files that you imported from an Amazon Simple Storage Service \(Amazon S3\) bucket to define a segment, and any Amazon Pinpoint metrics and spending alarms that you configured in Amazon CloudWatch\.

**To delete a project**

1. Open the Amazon Pinpoint console at [https://console\.aws\.amazon\.com/pinpoint/](https://console.aws.amazon.com/pinpoint/)\.

1. On the **All projects** page, choose the project that you want to delete\.

1. In the navigation pane, under **Settings**, choose **General settings**\.

1. Choose **Delete project**\.

1. Enter the name of the project that you want to delete, and then choose **Ok**\.