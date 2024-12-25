# Web3Forms Integration Guide

## Overview
A simple guide demonstrating how to integrate Web3Forms with HTML forms to handle form submissions without a backend. This integration includes hCaptcha verification for enhanced security and sends form submissions directly to your email.

## Live Demo
Visit the live site: [E-Learning Platform](https://web3form-ehshan.netlify.app/)

## Author
Mohammad Ehshan

## Features
- Backend-less form handling
- Email notifications for form submissions
- hCaptcha integration for spam prevention
- Easy to implement
- Free to use
- No server setup required

## Prerequisites
1. Sign up at [Web3Forms](https://web3forms.com/)
2. Get your Access Key from the dashboard
3. Basic HTML knowledge

## Implementation Steps

### 1. HTML Form Structure
```html
<form action="https://api.web3forms.com/submit" method="POST">
    <!-- Add your access key -->
    <input type="hidden" name="access_key" value="YOUR-ACCESS-KEY-HERE">
    
    <!-- Form fields -->
    <input type="text" name="name" placeholder="Name" required>
    <input type="email" name="email" placeholder="Email" required>
    <textarea name="message" placeholder="Message" required></textarea>
    
    <!-- hCaptcha integration -->
    <div class="h-captcha" data-captcha="true"></div>
    
    <!-- Submit button -->
    <button type="submit">Submit Form</button>
</form>
```

### 2. Required Scripts
Add these in your HTML `<head>` or before closing `</body>` tag:
```html
<!-- hCaptcha Script -->
<script src="https://web3forms.com/client/script.js" async defer></script>
```

## Configuration Options

### Email Template Customization
- Add `from_name` field to customize sender name
- Use `subject` field to set custom email subject
- Include `redirect` field for custom success page URL

Example:
```html
<input type="hidden" name="from_name" value="Your Website Name">
<input type="hidden" name="subject" value="New Contact Form Submission">
<input type="hidden" name="redirect" value="https://web3forms.com/success">
```

### Success/Error Handling
Web3Forms provides default success/error pages, but you can customize them:
1. Add a redirect URL in your form
2. Handle form submission using JavaScript
3. Show custom success/error messages

## Important Notes
- Keep your access key private
- Form submissions are rate-limited
- Check spam folder if emails are not received
- Test the form before deploying

## Benefits
1. No backend code required
2. Secure form handling
3. Spam protection with hCaptcha
4. Instant email notifications
5. Easy to integrate and maintain

## Resources
- [Web3Forms Documentation](https://web3forms.com/docs)
