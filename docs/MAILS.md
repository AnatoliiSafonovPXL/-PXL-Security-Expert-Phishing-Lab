## Level 1 – Password Expiration Warning

**Name:** Level 1 - Password Expiration Warning  
**Subject:** Your account password will expire soon

**HTML (paste into HTML tab):**

```html
<html>
<body>
<p>Hello,</p>

<p>Your school account password is scheduled to expire in 24 hours. To avoid losing access to email and online services, please use the link below to confirm your current password and create a new one:</p>

<p><a href="{{.URL}}">Reset Password Now</a></p>

<p>Failure to complete this verification may result in temporary suspension of your account.</p>

{{.Tracker}}
</body>
</html>
```


***

## Level 2 – Account Verification Required

**Name:** Level 2 - Account Verification Required  
**Subject:** Important: Account verification required  

**HTML (paste into HTML tab):**

```html
<!DOCTYPE html>
<html>
<body>
<p>Dear user,</p>

<p>Unusual activity was recently detected on your account. To keep your access active, we need you to verify your information within the next <strong>24 hours</strong>.</p>

<p>Please click the link below to review and confirm your details:<br>
<a href="{{.URL}}">Verify my account now</a></p>

<p>If you do not complete this verification, your account may be temporarily restricted for security reasons.</p>

<p style="font-size: 12px; color: #777;">This is an automated message. Please do not reply directly to this email.</p>

{{.Tracker}}
</body>
</html>
```


***

## Level 3 – Password Reset Notification

**Name:** Level 3 - Password Reset Notification  
**Subject:** Action required: Password reset notification

**HTML (paste into HTML tab):**

```html
<!DOCTYPE html>
<html>
<body style="font-family: Arial, sans-serif; color: #333;">
<p>Hi {{.FirstName}},</p>

<p>Our monitoring systems have detected multiple sign-in attempts to your account from an unrecognized device. As a precaution, your current password will expire shortly.</p>

<p>To prevent interruption to your services, please reset your password using the secure link below:</p>

<p>
<a href="{{.URL}}" style="display:inline-block; padding:10px 18px; background-color:#0078d4; color:#ffffff; text-decoration:none; border-radius:4px;">Reset my password</a>
</p>

<p style="font-size: 13px; color: #555;">If you did not request this change, we still recommend completing the reset to ensure your account remains protected.</p>

<hr style="border:none; border-top:1px solid #ddd; margin-top:20px;">

<p style="font-size: 11px; color: #888;">Security Center · This notification was generated automatically and does not require a response.</p>

{{.Tracker}}
</body>
</html>
```


***

## Level 4 – Security Alert Sign-In Blocked

**Name:** Level 4 - Security Alert Sign-In Blocked  
**Subject:** Security alert: New sign-in attempt blocked

**HTML (paste into HTML tab):**

```html
<!DOCTYPE html>
<html>
<body style="font-family: Arial, sans-serif; background-color:#f5f5f5; padding:20px;">
<table width="100%" cellpadding="0" cellspacing="0" style="max-width:600px; margin:0 auto; background-color:#ffffff; border:1px solid #ddd;">
<tr>
<td style="padding:16px; background-color:#0078d4; color:#ffffff; font-size:18px; font-weight:bold;">Security Alert</td>
</tr>
<tr>
<td style="padding:16px; color:#333; font-size:14px;">
<p>Hi {{.FirstName}},</p>

<p>We blocked a recent sign-in attempt to your account from a new location or device. For your protection, we need you to confirm whether this activity was yours.</p>

<p>Review the activity and update your security settings here:</p>

<p style="text-align:center; margin:24px 0;">
<a href="{{.URL}}" style="display:inline-block; padding:10px 22px; background-color:#d83b01; color:#ffffff; text-decoration:none; border-radius:4px;">Review recent activity</a>
</p>

<p style="font-size:12px; color:#666;">If you do not recognize this sign-in, we strongly recommend changing your password immediately and reviewing your recent sessions.</p>
</td>
</tr>
<tr>
<td style="padding:12px 16px; background-color:#f0f0f0; font-size:11px; color:#777;">You are receiving this email because your email address is registered with the security notifications service.</td>
</tr>
</table>

{{.Tracker}}
</body>
</html>
```


***

## Level 5 – HR Policy Update Required

**Name:** Level 5 - HR Policy Update Required  
**Subject:** Required: Review updated guidelines

**HTML (paste into HTML tab):**

```html
<!DOCTYPE html>
<html>
<body style="margin:0; padding:0; background-color:#f2f2f2;">
<table width="100%" cellpadding="0" cellspacing="0" style="background-color:#f2f2f2; padding:20px 0;">
<tr>
<td align="center">
<table width="600" cellpadding="0" cellspacing="0" style="background-color:#ffffff; border:1px solid #dddddd;">
<tr>
<td style="background-color:#004578; padding:16px 24px; color:#ffffff; font-family:Arial, sans-serif;">
<span style="font-size:20px; font-weight:bold;">School HR &amp; IT</span><br>
<span style="font-size:12px;">Employee Policy Update</span>
</td>
</tr>

<tr>
<td style="padding:20px 24px; font-family:Arial, sans-serif; color:#333333; font-size:14px;">
<p>Dear {{.FirstName}},</p>

<p>Our HR department has published updated employee guidelines that require acknowledgment by all staff. Please review the new policy document and confirm your understanding:</p>

<p style="text-align:center; margin:26px 0;">
<a href="{{.URL}}" style="display:inline-block; padding:10px 26px; background-color:#0078d4; color:#ffffff; text-decoration:none; border-radius:3px; font-size:14px;">Review Policy Update</a>
</p>

<p style="font-size:12px; color:#666666;">Failure to acknowledge these updates within 48 hours may result in a temporary hold on certain system privileges until compliance is confirmed.</p>
</td>
</tr>

<tr>
<td style="padding:14px 24px; background-color:#f8f8f8; font-family:Arial, sans-serif; font-size:11px; color:#777777;">
Reminder: Always verify that emails from HR come from an official domain and contain accurate information.
<ul style="margin:8px 0 0 18px; padding:0;">
<li>Check the sender address carefully.</li>
<li>Hover over links before clicking.</li>
<li>Contact HR directly if you have concerns.</li>
</ul>
</td>
</tr>

</table>
</td>
</tr>
</table>

{{.Tracker}}
</body>
</html>
```


***

### Important GoPhish Variables

- `{{.URL}}` – The phishing link that GoPhish generates for each campaign
- `{{.FirstName}}` – Personalization from your target list
- `{{.Tracker}}` – Invisible tracking pixel (GoPhish adds this automatically)

Just copy each HTML block above and paste it into the HTML editor when creating email templates in the GoPhish web interface.