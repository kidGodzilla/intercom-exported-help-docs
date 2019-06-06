# What Permissions do I need to grant to Meeting Room 365 for Office 365?

We care a lot about privacy & security as well, and I'm glad you reached out to learn more. We've taken great care to design our app to request the minimum number of permissions required to facilitate display functionality, and store as little data as possible.  
  
In doing so, we do not require any administrator-level privileges for Office 365, only user-level access for a resource mailbox (which has little access to systems outside it's own calendar and mailbox in the first place).  
  
We request three things (as outlined in the permissions grant flow, attached below and displayed each time you sign in to the Meeting Room 365 application):

[![](https://downloads.intercomcdn.com/i/o/76467575/8b1aa2bbe07bdb375e651d77/permissions.png)](https://downloads.intercomcdn.com/i/o/76467575/8b1aa2bbe07bdb375e651d77/permissions.png)

1.  **User.profile**  – this provides your name and email, and in some cases, your organization and/or title. We require this to retrieve your email address correctly.
2.  **Calendars.readwrite**  – this provides access to calendars owned by the resource mailbox user. By default, this is a single calendar used to manage resource bookings. We can read and write events (write is required for Instant Reservations, which are utilized by 91% of our users).
3.  **Offline_access**  – This allows us to access data in the above two permission scopes until you sign out of your account. We require this because, the alternative system provided by Microsoft, would require a user to sign back in on the tablet every 4 hours. This behavior is OAuth 2.0 compliant & pretty standardized across the tech industry.

I've used the Microsoft permission-level grant codes so that you can reference these in the Microsoft documentation as well:  [https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-permissions-and-consent](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-permissions-and-consent)

Additionally, we go pretty far to ensure our users maintain positive control of their accounts. Your authentication tokens are stored securely in your tablet, not in our systems, so that access is secured in your on-premises environment. That means requests can only be initiated from your tablet (and not our systems) to access Office 365, and only through the application sandbox. Additionally, this access can be revoked instantly through Azure AD in the event you lose control of the hardware device(s) running our software.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU2NzA4NjYxNl19
-->