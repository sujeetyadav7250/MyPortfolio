# Web3Forms Setup Guide for Contact Form

## Quick Setup (Recommended)

### Step 1: Get Your Access Key
1. Go to [Web3Forms.com](https://web3forms.com/)
2. Click "Get Access Key" 
3. Enter your email address
4. Check your email for the access key (it will look like `YOUR-ACCESS-KEY-HERE`)

### Step 2: Update Your HTML
Replace `YOUR_WEB3FORMS_ACCESS_KEY` in your `index.html` file with your actual access key:

```html
<form class="contact-form" id="contactForm" method="POST">
    <input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">
    <input type="hidden" name="subject" value="New Contact Form Submission from Portfolio">
    <input type="checkbox" name="botcheck" style="display: none;">
    <!-- rest of your form fields -->
    <div id="formResult" class="mt-3"></div>
</form>
```

**Example:**
```html
<form class="contact-form" id="contactForm" method="POST">
    <input type="hidden" name="access_key" value="YOUR-ACCESS-KEY-HERE">
    <input type="hidden" name="subject" value="New Contact Form Submission from Portfolio">
    <input type="checkbox" name="botcheck" style="display: none;">
    <!-- rest of your form fields -->
    <div id="formResult" class="mt-3"></div>
</form>
```

### Step 3: Test Your Form
1. Open your portfolio website
2. Fill out the contact form
3. Submit the form
4. Check your email for the message

## How It Works
- When someone submits the form, JavaScript handles the submission via fetch API
- Web3Forms will automatically send you an email with the form data
- You'll receive the form data in your email inbox
- The form shows real-time feedback to users
- Built-in spam protection with honeypot field

## JavaScript Implementation
The form uses JavaScript to handle submissions with better user experience:

```javascript
const contactForm = document.getElementById('contactForm');
const result = document.getElementById('formResult');

contactForm.addEventListener('submit', function(e) {
    e.preventDefault();
    
    const formData = new FormData(contactForm);
    const object = Object.fromEntries(formData);
    const json = JSON.stringify(object);
    
    fetch('https://api.web3forms.com/submit', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
            'Accept': 'application/json'
        },
        body: json
    })
    .then(async (response) => {
        let json = await response.json();
        if (response.status == 200) {
            result.innerHTML = '<div class="alert alert-success">' + json.message + '</div>';
            contactForm.reset();
        } else {
            result.innerHTML = '<div class="alert alert-danger">' + json.message + '</div>';
        }
    })
    .catch(error => {
        result.innerHTML = '<div class="alert alert-danger">Something went wrong!</div>';
    });
});
```

## Additional Features
Web3Forms offers several additional features you can use:

### Honeypot Protection
Add a hidden field to prevent spam:
```html
<input type="hidden" name="botcheck" style="display: none;">
```

### Custom Redirect
Redirect to a custom page after submission:
```html
<input type="hidden" name="redirect" value="https://yoursite.com/thank-you">
```

### Custom Subject
Set a custom email subject:
```html
<input type="hidden" name="subject" value="New Contact Form Submission">
```

## Troubleshooting
- Make sure your access key is correct
- Check that your email is verified
- Look for any JavaScript errors in the browser console
- Test with a simple form submission first
- Check your spam folder if you don't receive emails

## Benefits of Web3Forms
- **Free**: No cost for basic usage
- **No Registration**: Just get an access key and start using
- **Spam Protection**: Built-in honeypot and other anti-spam measures
- **Customizable**: Multiple configuration options
- **Reliable**: High deliverability rates
- **Privacy**: No data stored on their servers

## Alternative: EmailJS
If you prefer more control over the email sending process, you can use EmailJS instead. See the `EMAIL_SETUP.md` file for EmailJS instructions. 