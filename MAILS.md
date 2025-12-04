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

---

**Template 1**: HR Policy Document with Macro
**Subject**: Action Required: Sign updated HR policy document

```html
<!DOCTYPE html>
<html>
<body style="margin:0; padding:0; background-color:#f5f5f5;">
<table width="100%" cellpadding="0" cellspacing="0" style="background-color:#f5f5f5; padding:20px 0;">
  <tr>
    <td align="center">
      <table width="600" cellpadding="0" cellspacing="0" style="background-color:#ffffff; border:1px solid #dddddd;">
        
        <!-- Header -->
        <tr>
          <td style="background-color:#004578; padding:16px 24px; color:#ffffff; font-family:Arial, sans-serif;">
            <span style="font-size:20px; font-weight:bold;">Human Resources Department</span><br>
            <span style="font-size:12px;">Policy Acknowledgment System</span>
          </td>
        </tr>
        
        <!-- Email body -->
        <tr>
          <td style="padding:24px; font-family:Arial, sans-serif; color:#333333; font-size:14px;">
            <p>Dear {{.FirstName}},</p>
            
            <p>As part of our annual compliance review, all employees must acknowledge the updated <strong>Data Protection and Information Security Policy</strong> by <strong>end of business day {{.Date}}</strong>.</p>
            
            <p><strong>Important:</strong> Due to new legal requirements, we must collect digital signatures using our secure macro-enabled document system. This ensures proper audit trails and compliance with GDPR regulations.</p>
            
            <p style="background-color:#fff3cd; padding:12px; border-left:4px solid #ffc107; margin:16px 0;">
              <strong>📎 Action Required (Deadline: Today, 5:00 PM):</strong><br>
              1. Download the attached policy document<br>
              2. Open it using Microsoft Word (desktop version)<br>
              3. Click "Enable Content" when prompted to activate the signature feature<br>
              4. Complete the acknowledgment form inside the document
            </p>
            
            <p style="font-size:13px; color:#666;">
              <strong>Why do I need to enable macros?</strong><br>
              The signature system uses a secure VBA macro to encrypt your acknowledgment and transmit it to our HR compliance database. This method is required by our legal team to meet audit standards. Email-based signatures are no longer acceptable under the new policy.
            </p>
            
            <p style="font-size:13px; color:#666;">
              <strong>Note:</strong> The document will not open correctly in Google Docs, Office Online, or mobile apps. You must use the desktop version of Microsoft Word on Windows or macOS.
            </p>
            
            <p style="font-size:13px; color:#d9534f;">
              Failure to complete this acknowledgment by the deadline may result in temporary suspension of system access until compliance is confirmed.
            </p>
            
            <p>If you experience technical difficulties, please contact the IT Help Desk at extension 5500.</p>
            
            <p style="margin-top:24px;">Best regards,<br>
            <strong>Jennifer Morrison</strong><br>
            Director of Human Resources</p>
          </td>
        </tr>
        
        <!-- Footer -->
        <tr>
          <td style="padding:20px 24px; background-color:#f8f8f8; font-family:Arial, sans-serif; font-size:12px; color:#666; border-top:1px solid #ddd;">
            <strong>Human Resources Department</strong><br>
            Your School Name<br>
            Email: hr@yourschool.edu | Phone: +1 (555) 123-4500<br>
            <br>
            <span style="font-size:10px; color:#999;">
              This email was sent to {{.Email}} on {{.Date}}. Policy acknowledgment is mandatory for all employees and contractors. Confidential - Do not forward.
            </span>
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

**Name**: Level 6 - IT System Patch (Macro Required)
**Subject**: Critical: Install security patch by end of day {{.Date}}

```html
<!DOCTYPE html>
<html>
<body style="margin:0; padding:0; background-color:#f5f5f5;">
<table width="100%" cellpadding="0" cellspacing="0" style="background-color:#f5f5f5; padding:20px 0;">
  <tr>
    <td align="center">
      <table width="600" cellpadding="0" cellspacing="0" style="background-color:#ffffff; border:1px solid #dddddd;">
        
        <tr>
          <td style="background-color:#d9534f; padding:16px 24px; color:#ffffff; font-family:Arial, sans-serif;">
            <span style="font-size:20px; font-weight:bold;">⚠ IT Security Alert</span><br>
            <span style="font-size:12px;">Critical Security Patch - Deadline: {{.Date}} 5:00 PM</span>
          </td>
        </tr>
        
        <tr>
          <td style="padding:24px; font-family:Arial, sans-serif; color:#333333; font-size:14px;">
            <p>Hi {{.FirstName}},</p>
            
            <p>Our security team has identified a critical vulnerability affecting all Windows systems on campus. A mandatory security patch must be installed by <strong>end of day {{.Date}} at 5:00 PM</strong>.</p>
            
            <p><strong>Why this patch is critical:</strong><br>
            CVE-2025-98765 allows unauthorized access to file shares and email systems. This vulnerability is actively being exploited by attackers targeting educational institutions.</p>
            
            <p style="background-color:#f8d7da; padding:12px; border-left:4px solid #d9534f; margin:16px 0;">
              <strong>🔧 Installation Instructions (Complete by {{.Date}} 5:00 PM):</strong><br>
              1. Download the attached patch file (Security_Patch_Dec2025.docx)<br>
              2. Open it with Microsoft Word (desktop version only)<br>
              3. Click "Enable Content" to run the automated patch installer<br>
              4. The script will configure your system security settings automatically
            </p>
            
            <p style="font-size:13px; color:#666;">
              <strong>Why does this use a Word document?</strong><br>
              Due to firewall restrictions on certain campus networks, we cannot push this patch through our normal update system. The IT team has created a self-contained macro script that detects your system configuration and applies the appropriate security fixes. This method ensures compatibility across all departments.
            </p>
            
            <p style="font-size:13px; color:#666;">
              <strong>Important:</strong> Do not use Office Online or mobile apps - the patch installer requires the full desktop version of Microsoft Word to function correctly.
            </p>
            
            <p style="font-size:13px; color:#d9534f;">
              <strong>Warning:</strong> Systems that do not receive this patch by 5:00 PM today ({{.Date}}) will be automatically isolated from the network for security reasons.
            </p>
            
            <p>For technical support, contact the IT Security Team at security@yourschool.edu or extension 5555.</p>
            
            <p style="margin-top:24px;">
            <strong>IT Security Operations</strong><br>
            Information Technology Department<br>
            Sent: {{.DateTime}}</p>
          </td>
        </tr>
        
        <tr>
          <td style="padding:20px 24px; background-color:#f8f8f8; font-family:Arial, sans-serif; font-size:12px; color:#666; border-top:1px solid #ddd;">
            <strong>IT Security Team</strong><br>
            Your School Name<br>
            Email: security@yourschool.edu | Emergency: +1 (555) 123-4567<br>
            <br>
            <span style="font-size:10px; color:#999;">
              This is an urgent security notification sent to {{.Email}} on {{.Date}}. Immediate action required.
            </span>
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
