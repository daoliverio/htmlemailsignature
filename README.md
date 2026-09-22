[README (1).md](https://github.com/user-attachments/files/32539364/README.1.md)
# School Email Signature Generator

This project gives school districts a simple email signature generator that can be added to a district website. Staff members can choose their school, enter their information, preview the signature, and copy it into Outlook.

##See It In Action

- https://www.harcoboe.net/page/email-signature-generator

## What It Does

- Offers Standard and Compact signature templates
- Lets staff select their school or department
- Fills in the school name, address, phone, fax, website, and logo
- Shows a live preview
- Copies a formatted signature for Outlook
- Downloads the finished signature as an HTML file
- Saves unfinished entries in the user's browser
- Works on desktop and mobile screens

## Add the Generator to Your Website

Most school website providers offer a **Custom HTML**, **Embed Code**, or **Source Code** area.

1. Download `Harrison-County-Email-Signature-Generator.html`.
2. Open the file in a plain-text or code editor.
3. Copy the generator code.
4. Sign in to your school website provider.
5. Create or edit the page where the generator will appear.
6. Add a Custom HTML, Embed Code, or Source Code block.
7. Paste the generator code into that block.
8. Save or publish the page.
9. Test the school selector, live preview, copy button, and mobile layout.

Your website provider must allow HTML, CSS, and JavaScript. If it removes `<script>` tags, the generator will not work. In that case, ask the website provider to host the file or allow JavaScript on the page.

## Important: Keep the Code in a Container

The generator should remain inside one main container. This helps keep its styles and controls from affecting the rest of the school website.

```html
<div id="hcs-email-generator-embed">
  <!-- Keep all generator HTML, CSS, and JavaScript here. -->
</div>
```

If you use AI to rewrite this code for your district, tell it:

> Keep the full email signature generator wrapped in one unique container. Scope all CSS and JavaScript to that container so the code does not change other parts of the website.

Use a unique container ID for your district. For example:

```html
<div id="your-district-signature-generator">
  <!-- Generator code -->
</div>
```

CSS should start with that same ID:

```css
#your-district-signature-generator .card {
  background: #ffffff;
}
```

JavaScript should also find the container first:

```js
const root = document.getElementById('your-district-signature-generator');
```

Do not remove the container unless you also update every related CSS selector and JavaScript reference.

## Use It as a Separate Web Page

If your website provider does not allow JavaScript in page blocks, the generator can be hosted as its own page.

1. Rename the HTML file to `index.html`.
2. Upload it to a web server or GitHub Pages.
3. Add a link to the generator from the district website.

## Change It for Your District

Before publishing, update:

- District name and heading
- Brand colors
- School and department names
- Addresses
- Office and fax numbers
- Website links
- School logo links
- Default email wording
- Disclaimer text, if needed

School information is stored in the `SCHOOLS` list inside the HTML file:

```js
{
  key: 'school-key',
  label: 'School Name',
  url: 'https://example.org/school-logo.png',
  address: '123 School Street, Your City, WV 26000',
  phoneOffice: '304-555-0100',
  phoneFax: '304-555-0101',
  web: 'https://www.example.org/school'
}
```

Each school must have a different `key`. If a school does not use fax, leave `phoneFax` empty:

```js
phoneFax: ''
```

## Logo Requirements

- Use an `https://` image link.
- Use a clear PNG or JPG file.
- Keep the logo available at the same web address.
- Test the logo in Outlook Web and the Outlook desktop app.

Some email programs block outside images until the person allows them. This is normal and does not always mean the generator is broken.

## Browser Storage and Privacy

The generator saves entered information in the browser. This helps staff return to unfinished work, but the information can remain on a shared computer.

Staff should select **Clear saved information** after using the generator on a shared device.

## Testing Checklist

Before sharing the page with staff, check that:

- Every school appears in the selector.
- Each school fills in the correct information.
- Each logo loads.
- Both templates display correctly.
- The live preview changes as information is entered.
- The vertical and horizontal divider lines appear.
- The Copy for Outlook button works.
- The signature pastes correctly into Outlook Web.
- The signature pastes correctly into the Outlook desktop app.
- The page works on a phone.
- The generator does not change other parts of the website.

## Maintenance

Review school addresses, phone numbers, website links, and logo links at least once each school year. Test the generator again after your website provider makes a major platform update.

## Files

```text
Harrison-County-Email-Signature-Generator.html
README.md
```

## License

No license is included. Add a license before allowing public reuse or distribution.
