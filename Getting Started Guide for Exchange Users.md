# Getting Started Guide for Exchange Users

### Setting up your first Meeting Room Displays on Microsoft Exchange


[![](https://downloads.intercomcdn.com/i/o/116373972/8fbc2b45c89b8b50d57c4f8b/1%2AAnjsjwb8sYcsEE8uyqDHIw.png)](https://downloads.intercomcdn.com/i/o/116373972/8fbc2b45c89b8b50d57c4f8b/1%2AAnjsjwb8sYcsEE8uyqDHIw.png)

In this article, we'll cover the entire process for setting up Meeting Room displays for Office 365. The first portion of this guide occurs in the Office 365 Admin Portal. So, if you rely on another IT administrator to manage your Office 365 tenant, you'll want to include that person for step 1.  

## Project Outline:

1.  **Create Room Resource Mailboxes**  in Exchange
2.  **Test Exchange Credentials** using the Meeting Room 365 app / Exchange
3.  **Create Meeting Room Displays** in Meeting Room 365
4.  **Set up hardware**  in your office

## Step One: Create Room Resource Mailboxes in Exchange

**a. Configure a Resource Mailbox**

The easiest way to configure a new Resource Mailbox for Exchange 2007–2016 is via Exchange Management Shell. Alternatively, Exchange Management Console (EMC) provides an interface for creating resource mailboxes.

If you're on hosted exchange (Godaddy, Rackspace, etc.), steps may vary.

Follow  [this guide](https://technet.microsoft.com/en-us/library/jj215781(v=exchg.160).aspx)  to see instructions on creating a Resource mailbox on  **Exchange 2013/2016**.  
  
Alternatively, follow  [this guide](https://technet.microsoft.com/en-us/library/bb124952(v=exchg.141).aspx)  to see instructions on creating a Resource Mailbox on  **Exchange 2007/2010**.  

**b. Configure Resource Mailboxes to show meeting subjects**

By default, your resource mailbox will show the organizer’s name as the subject for each meeting.

To resolve this, you will need to  [run a cmdlet](https://support.microsoft.com/en-us/help/2842288/resource-mailbox-s-calendar-shows-the-organizer-s-name-instead-of-the)  in the Exchange Management Shell.

  

## Step Two: Test Exchange Credentials using the Meeting Room 365 app / Exchange

In order to successfully connect Meeting Room 365 to Exchange, you'll need to figure out all of the credentials required to connect to the  **EWS SOAP API**. Those include hostname, username (UPN, not email), password, and EWS Version.

[![](https://downloads.intercomcdn.com/i/o/116376121/5a66ee1fd0f75ff1be8d2b48/image.png)](https://downloads.intercomcdn.com/i/o/116376121/5a66ee1fd0f75ff1be8d2b48/image.png)

Fortunately, it's a pretty simple process of finding and testing these credentials with the  **Meeting Room 365 app**, and  **Outlook Web Access**.

First, you can check your username and password in  **Outlook Web Access**. What trips most people up is the fact that your sign in username (UPN) varies from your mailbox email address on some versions of Exchange. It even varies from patch to patch. It can be the  **user alias**  (myuser), the  **domain+alias**  (\mydomain\myuser), or the  **full email address**  ([myuser@mydomain.com](mailto:myuser@mydomain.com)), and you'll have to try connecting to Meeting Room 365 with all three to figure it out.

When you're ready, open the  [Meeting Room 365 app](https://app.meetingroom365.com/)  (**incognito**  or in  **private browsing mode**  if that's available) to test your credentials.

You'll also need the  **hostname**  for your EWS server. Meeting Room 365 should automatically remove the unnecessary bits if you happen to include them (like protocol and pathname).

If you're getting stuck, reach out to support for more help. We also have  [an article](https://intercom.help/mr365/troubleshooting-and-common-issues/im-experiencing-an-ews-authentication-issue)which covers this in more detail.

  

## Step Three: Create Meeting Room Displays in Meeting Room 365

Next, you will create your Meeting Room displays in Meeting Room 365.

There is a wizard which can be accessed from the  [Meeting Room 365 Admin Portal](https://manage.meetingroom365.com/), to provision a new Meeting Room display for Exchange.

[![](https://downloads.intercomcdn.com/i/o/116374365/599f3ef7fbaa30b2ee6d7d8d/1%2A9PrZL-Js-1ygOmHlCNNYXA.png)](https://downloads.intercomcdn.com/i/o/116374365/599f3ef7fbaa30b2ee6d7d8d/1%2A9PrZL-Js-1ygOmHlCNNYXA.png)

Click the **Red Plus**  in the bottom left corner of the admin portal, and select  **Exchange**.

Next, you will be guided through the process of setting up a resource mailbox (if you haven't already), connect to Exchange (with your resource mailbox credentials and hostname), and finally given a  **Display Key**, which you can use to set up your tablet display.

  

## Step Four: Set up hardware

The final step is to download the Meeting Room 365 app from the app store of choice for your display (iTunes, Google Play, or the Amazon App Store).

[![](https://downloads.intercomcdn.com/i/o/116374204/615a34ea3fb9e603f24e77e4/image.png)](https://downloads.intercomcdn.com/i/o/116374204/615a34ea3fb9e603f24e77e4/image.png)

When prompted, select  `Enter Display Key`, and enter your display key.

**_Tip:_** _You can use_ **_spaces_** _and arbitrary_ **_capitalization_** _to make entering the key easier, especially on devices with auto-correct turned on. Meeting Room 365 will strip these details out automatically._

## That’s it! If you’re stuck, you can always contact us from your admin portal, and we can help you out with setup, configuration, and provisioning.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQwMjU4ODY5NF19
-->