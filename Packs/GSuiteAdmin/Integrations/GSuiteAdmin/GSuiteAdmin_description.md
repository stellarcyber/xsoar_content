# Configure an API account on G Suite Admin
Configure a service account and retrieve its key in JSON format by following the steps mentioned here: [https://developers.google.com/identity/protocols/oauth2/service-account#creatinganaccount](https://developers.google.com/identity/protocols/oauth2/service-account#creatinganaccount) or in the integration README.
 

Provide at least one of the scopes mentioned for each command.

### Commands and its scopes
| **Command Name** | **Scope** |
|---|---|
| gsuite-user-create, gsuite-user-update, and gsuite-user-delete, gsuite-user-get, gsuite-user-reset-password | https://www.googleapis.com/auth/admin.directory.user | 
| gsuite-mobile-update | https://www.googleapis.com/auth/admin.directory.device.mobile.action |
| gsuite-mobile-delete | https://www.googleapis.com/auth/admin.directory.user.readonly, https://www.googleapis.com/auth/admin.directory.user, https://www.googleapis.com/auth/cloud-platform | 
| gsuite-role-assignment-list | https://www.googleapis.com/auth/admin.directory.rolemanagement.readonly, https://www.googleapis.com/auth/admin.directory.rolemanagement |
| gsuite-role-assignment-create | https://www.googleapis.com/auth/admin.directory.rolemanagement | 
| gsuite-user-alias-add | https://www.googleapis.com/auth/admin.directory.user.alias, https://www.googleapis.com/auth/admin.directory.user |
| gsuite-token-revoke | https://www.googleapis.com/auth/admin.directory.user.security | 
| gsuite-datatransfer-request-create | https://www.googleapis.com/auth/admin.datatransfer |
| gsuite-datatransfer-list | https://www.googleapis.com/auth/admin.datatransfer, https://www.googleapis.com/auth/admin.datatransfer.readonly | 
| gsuite-group-create | https://www.googleapis.com/auth/admin.directory.group |
| gsuite-group-get | https://www.googleapis.com/auth/admin.directory.group | 
| gsuite-role-create | https://www.googleapis.com/auth/admin.directory.rolemanagement |
| gsuite-custom-user-schema-create, gsuite-custom-user-schema-update | https://www.googleapis.com/auth/admin.directory.userschema |
| gsuite-mobiledevice-list | https://www.googleapis.com/auth/admin.directory.device.mobile.readonly | 
| gsuite-chromeosdevice-action | https://www.googleapis.com/auth/admin.directory.device.chromeos |
| gsuite-chromeosdevice-list | https://www.googleapis.com/auth/admin.directory.device.chromeos.readonly |
| gsuite-chromebrowserdevice-move-ou, gsuite-chromebrowserdevice-list | https://www.googleapis.com/auth/admin.directory.device.chromebrowsers | 
| gsuite-policy-modify, gsuite-policy-schemas-list, gsuite-policy-resolve and gsuite-policy-groups-delete | https://www.googleapis.com/auth/chrome.management.policy |

To execute the command either provide the value of the Admin email in the integration configuration or provide the value of the *admin_email* argument for the command or provide the admin role to the created service account's email by performing the following steps:

1. You must be signed in as a super administrator for this task.
2. Open your Google Admin console (at [https://admin.google.com](https://admin.google.com)).
3. Go to Admin roles.
4. Click the role you want to assign (the appropriate role).
5. Click *Assign Admin*.
6. On the opened page, click *Assign Service Accounts*.
7. Append the email ID of the service account created and click *ASSIGN ROLE* to save.

Precedence of this will be admin_email in the command argument > admin email in the integration configuration > admin role provided to the service account.
