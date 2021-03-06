# I'm Experiencing an EWS Authentication Issue

Troubleshooting an issue connecting to an Exchange Mailbox

Almost all issues connecting Meeting Room 365 to EWS boil down to EWS authentication issues.

There are a number of factors, such as incorrect hostname or hostname format, incorrect username, incorrect password, or mixing up service user accounts and resource mailbox accounts (when using a delegate).

**However,**  **EWS authentication issues are usually all about knowing the username for the resource mailbox.**  
  
EWS Usernames are tricky and vary from version to version, and since you typically don't sign in with the resource mailbox user, a lot of users have to do a bit of guessing to figure out the correct format for their EWS username.

An  **EWS user**  (with a username and password) is automatically generated by Exchange when you create a Resource Mailbox. However, most users (and experienced admins) never see this, since signing into a resource mailbox account is atypical.

In the latest versions of Exchange, the  **EWS Username**  is typically the email address assigned to the resource mailbox.

But in  **Exchange 2010**, for example, the  **EWS Username**  is usually not the email address for the resource mailbox.

Sometimes, the EWS username must contain the  **domain**  (`\domain\user`  or  `domain\user`) to sign in.

The easiest way of figuring this out is to  **Sign in to Outlook Web Access with your resource mailbox credentials**. We connect to your resource mailbox via the  **Exchange SOAP API**, which is authenticated with the same EWS username and password used to authenticate with OWA. If your username & password works on OWA it should work in Meeting Room 365 as well.

You can also try signing in to  [https://app.meetingroom365.com/](https://app.meetingroom365.com/)  with your EWS credentials, on your desktop, until you get the right combination. This can be aided by using an incognito or private browsing session (so you can easily repeat the process).

  
**Thanks for reading!**  If you have any issues, please reach out to support for assistance.
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTYwMTE4Njg3XX0=
-->