# Change account password using PowerShell

1. Open PowerShell (Run as administrator).

2. Type the following command to list all the available accounts and press Enter:

```powershell
Get-LocalUser
```

3. Type the following command to create and store the new password inside of a variable and press Enter:

```powershell
$Password = Read-Host "Enter the new password" -AsSecureString
```

4. Type the new password for the account and press Enter.

5. Type the following command and press Enter on each line to apply the new password to the local account:

```powershell
$UserAccount = Get-LocalUser -Name "Administrator"
$UserAccount | Set-LocalUser -Password $Password
```

Obs.: Make sure to replace “Administrator” with the name of the account to reset its password.

6. Once you complete the steps, the new password can now be used.
