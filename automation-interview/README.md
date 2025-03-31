# MLS Automation Coding Challenge

## Overview

This coding challenge evaluates your proficiency in web automation using Puppeteer and TypeScript. Your goal is to create a reliable automation script that navigates through a nested iframe structure, logs into an MLS (Multiple Listing Service) website, and submits a new real estate listing.

---

## Scenario

You are automating the submission of real estate listings into an MLS website. This site uses nested iframes to embed the submission form.

Your automation script must:

1. Log into the MLS website.
2. Navigate through nested iframes to access the "New Listing" form.
3. Fill out the form using provided structured data.
4. Submit the form.
5. Handle basic client-side validation errors with retries.
6. Capture a screenshot of the confirmation page after successful submission.

---

## Technical Details

- **Login Page URL:** `https://example-mls.com/login`
- **Dashboard URL (after login):** `https://example-mls.com/dashboard`
- **Iframe Structure:**
  - Outer iframe ID: `#main-frame`
  - Inner iframe attribute: `<iframe title="listing-entry-form">`

### Login Form Fields
- Username field ID: `#username`
- Password field ID: `#password`
- Submit button ID: `#login-button`

### Listing Form Fields (within nested iframes)
- Address: `#address`
- Price: `#price`
- Bedrooms: `#bedrooms`
- Bathrooms: `#bathrooms`
- Description: `#description`
- Submit button ID: `#submit-listing`

### Error Handling
- Client-side validation errors appear within elements with class `.error-message`.
- Retry submissions up to 3 attempts.

---

## Notes
- The login process requires navigating through multiple iframes.
- The submission form is nested within an iframe.