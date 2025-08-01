# Email Setup Guide for Contact Form

To make your contact form actually send emails, you need to set up EmailJS. Follow these steps:

## Step 1: Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

## Step 2: Add Email Service
1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "Gmail" (or your preferred email provider)
4. Connect your email account (sy340190@gmail.com)
5. Note down the **Service ID** (you'll need this)

## Step 3: Create Email Template
1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template:

**Subject:** New Contact Form Message from {{from_name}}

**Content:**
```
Name: {{from_name}}
Email: {{from_email}}
Subject: {{subject}}

Message:
{{message}}
```

4. Save the template and note down the **Template ID**

## Step 4: Get Your Public Key
1. Go to "Account" → "API Keys"
2. Copy your **Public Key**

## Step 5: Update Your Code
Replace the placeholders in `script.js`:

```javascript
// Replace YOUR_EMAILJS_PUBLIC_KEY with your actual public key
emailjs.init("YOUR_EMAILJS_PUBLIC_KEY");

// Replace YOUR_SERVICE_ID with your EmailJS service ID
// Replace YOUR_TEMPLATE_ID with your EmailJS template ID
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', templateParams)
```

## Example:
```javascript
emailjs.init("user_abc123def456");
emailjs.send('service_xyz789', 'template_contact123', templateParams)
```

## Step 6: Test Your Form
1. Open your portfolio website
2. Fill out the contact form
3. Submit the form
4. Check your email (sy340190@gmail.com) for the message

## Troubleshooting
- Make sure all IDs are correct
- Check your browser console for any errors
- Verify your EmailJS account is active
- Ensure your email service is properly connected

## Alternative: Using Formspree
If you prefer a simpler solution, you can also use Formspree:

1. Go to [Formspree.io](https://formspree.io/)
2. Create a free account
3. Create a new form
4. Replace your form action with the Formspree endpoint:

```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

This will automatically handle email sending without any JavaScript configuration needed. 