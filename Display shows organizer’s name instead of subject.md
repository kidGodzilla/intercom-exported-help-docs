# Display shows organizer’s name instead of subject

Solution to a common Office 365 & Exchange Resource Mailbox Issue

In Office 365 & Microsoft Exchange, by default, your resource mailbox won’t show your Meeting Subject. Instead, it replaces this with your organizer’s name. This occurs for privacy reasons, but it’s only the default. Most organizations opt to see meeting subjects instead.

[![](https://downloads.intercomcdn.com/i/o/63645955/629c6decf06d8abb14f8681a/1%2AF7fDIy5NWqr9gYaW-8SuwA.png)](https://downloads.intercomcdn.com/i/o/63645955/629c6decf06d8abb14f8681a/1%2AF7fDIy5NWqr9gYaW-8SuwA.png)

Consider the following:

-   A Resource mailbox is configured to AutoAccept in an Microsoft Exchange Server or Office 365 environment.
-   You send a meeting request to the Resource mailbox.
-   The meeting request is accepted automatically, and the meeting subject is displayed correctly in the organizer’s mailbox.

In this scenario, when you log on to the  **Resource mailbox**, you see that the  **meeting subject**  is replaced with the  **organizer’s name**.

# Why is this happening?

This is default behavior for Exchange Web Services and Office 365. It occurs because two configuration parameters,  **AddOrganizerToSubject**  and  **DeleteSubject**  are set to  **$True**.

# Solution

The good news is, you don’t have to open  **PowerShell**  to update this setting. You can update it directly from the  [**Meeting Room 365**](https://meetingroom365.com/)  **admin portal**.

[![](https://downloads.intercomcdn.com/i/o/63645956/2e03e120782f7ccdf44021f7/1%2AZlUG_QBOi44VgoHDorqRag.jpeg)](https://downloads.intercomcdn.com/i/o/63645956/2e03e120782f7ccdf44021f7/1%2AZlUG_QBOi44VgoHDorqRag.jpeg)

Just click on your display menu, and then click on the third icon (PowerShell).

Then, enter the password for your resource mailbox:

[![](https://downloads.intercomcdn.com/i/o/63645958/6684fed1b14493cf774f0b67/1%2Ag7Xtc3Br1P9AEH8yPJCB1Q.jpeg)](https://downloads.intercomcdn.com/i/o/63645958/6684fed1b14493cf774f0b67/1%2Ag7Xtc3Br1P9AEH8yPJCB1Q.jpeg)

This queues the display for PowerShell configuration in our system (which usually takes a few minutes).

Once this is completed, all  **new meetings**  scheduled on this resource mailbox will display their full subject, along with any other details you have configured to display. For existing meeting reservations, the damage is already done, and the subject has been deleted.

[![](https://downloads.intercomcdn.com/i/o/63645961/ae9f5a9bd76e4004be48ab35/1%2A-IxpFByb0gGf6tZTJG6ZCQ.png)](https://downloads.intercomcdn.com/i/o/63645961/ae9f5a9bd76e4004be48ab35/1%2A-IxpFByb0gGf6tZTJG6ZCQ.png)

# Prefer to do this manually?

## View your current configuration (optional):

To view these value for the Resource mailbox, run the one of the following cmdlets:

For Exchange Server 2016, Exchange Server 2013 or Exchange Server 2010

Get-CalendarProcessing -Identity <RESOURCEMAILBOX> | FL

For Exchange Server 2007

Get-MailboxCalendarSettings -identity <RESOURCEMAILBOX>  
|FL

## Update your Configuration:

To resolve this issue, follow these steps:

For Office 365, Exchange Server 2016, Exchange Server 2013 or Exchange Server 2010 (PowerShell):

Set-CalendarProcessing -Identity <RESOURCEMAILBOX> -DeleteSubject $False -AddOrganizerToSubject $False

Exchange Server 2007 (PowerShell):

Set-MailboxCalendarSettings -Identity <RESOURCEMAILBOX> -AutomateProcessing AutoAccept -AddOrganizerToSubject $False -DeleteSubject $False

**Source:** [https://support.microsoft.com/en-us/help/2842288/resource-mailbox-s-calendar-shows-the-organizer-s-name-instead-of-the](https://support.microsoft.com/en-us/help/2842288/resource-mailbox-s-calendar-shows-the-organizer-s-name-instead-of-the)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NDM0OTE1MDZdfQ==
-->