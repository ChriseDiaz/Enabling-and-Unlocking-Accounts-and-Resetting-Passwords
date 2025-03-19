<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Enabling and Unlocking Accounts and Resetting Passwords (Azure)</h1>
This tutorial will help you understand how account lockout works, how to manage user accounts, and how to monitor authentication events of Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube/ClipChamp: Enabling and Unlocking Accounts and Resetting Passwords](https://youtu.be/g0OsqpcXJX4?si=d24ZYUj0qzeToRbD)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- Active Directory Users and Computers
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

-Configure Group Policy to set an account lockout threshold.

-Attempt failed logins to trigger an account lockout.

-Unlock and reset the password.

-Disable and re-enable the account to observe the effect.

-Monitor logs both on the domain controller and client machine.

<h2>Deployment and Configuration Steps</h2>

<p>
![Image](https://github.com/user-attachments/assets/fde0cd4d-37fb-45e5-841b-2aabcff193bc)
</p>
<p>
Process for dealing with account lockouts:

1.Log in to dc-1.

2.Pick a random user account created previously.

3.Attempt to log in 10 times with an incorrect password.

4.Configure Group Policy to set the account lockout threshold after 5 failed login attempts.

5.Attempt to log in 6 times with an incorrect password.

6.Observe that the account is locked out in Active Directory.

7.Unlock the account.

8.Reset the password.

9.Attempt to log in with the new password.

This process demonstrates how to configure account lockouts and manage account access in Active Directory.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Steps for enabling, disabling accounts, and observing logs:

1.Disable the user account in Active Directory.

2.Attempt to log in with the disabled account and observe the error message.

3.Re-enable the account in Active Directory.

4.Attempt to log in again with the re-enabled account.

Observing Logs:

1.Check the logs on the Domain Controller for any relevant events.

2.Check the logs on the client machine to see any login-related activity or errors.

This process covers managing user account status and reviewing logs on both the Domain Controller and Client machine.
</p>
<br />
