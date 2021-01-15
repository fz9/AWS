# Auto Create 3 Billing Alarms & Email Notification

This CF Template helps new users on AWS to automagically create 3 Billing Alerts with user input billing amounts to ensure you do not get any suprises at the end of the month.

- This template creates 3 Billing Alarms in CloudWatch and 1 SNS notification.
- Please ensure you execute this template only in the US East North Virginia Region as billing alarms for all regions are consolidated in this region.
- The 3 thresholds are editable. Please input the values according to your budget.
- Ensure you take immediate action once you get the 3rd alert because there will be no alerts after this and the total billing amount could theoretically run to infinity.
- You can add additional billing alerts manually from the cloudwatch dashboard if you wish to.
- The Cloudwatch Alarms & SNS notifications that are created by this template ideally should not cost you anything as they fit very well within the Free Tier. If you are outside of the free tier, please review your total alarms count to ensure you are aware of how much additional this would cost you.
- Please ensure you confirm the alert subscription that would come to your email address post creating this stack.
- The alarms will work only if you have enabled billing alerts in your billing dashboard.

## Setup Instructions

1. Log into your AWS dashboard and ensure you are in the US East North Virginia Region.
2. Go to your Billing Dashboard > Preferences. Enable "Receive Billing Alerts"
3. Go to Cloudformation and click on Create Stack.
4. Click on the Browse button and upload this JSON template.
5. Name the stack eg:Billing Alarms, set your budget values, enter your email address, click Next.
6. Although not necessary, if you wish to configure any options, you can do so at this page and then click Next.
7. Click Create.
8. Check your email inbox for the AWS Notification - Subscription Confirmation email and click on "confirm subscription". Done!
------------