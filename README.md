[README.md](https://github.com/user-attachments/files/32539173/README.md)
# HTML Email Signature Generator

A browser-based tool that helps employees create a consistent email signature for Outlook.

The generator is contained in one HTML file and does not need a server, database, build tool, or outside JavaScript library.

## Features

- Standard signature with a school logo
- Compact, text-only signature
- School and department selector
- Automatic school name, address, office phone, fax, website, and logo
- Live signature preview
- Adjustable logo size
- Optional cell phone, room, social media links, and disclaimer
- Outlook-friendly table layout and inline styles
- Horizontal and vertical divider lines designed for Outlook
- Copy formatted signature to the clipboard
- Download the finished signature as an HTML file
- Save form entries in the current browser
- Clear saved information from the browser
- Responsive layout for desktop and mobile screens

## Project File

```text
Harrison-County-Email-Signature-Generator.html
```

The HTML file includes all page markup, styles, school data, and JavaScript.

## Use the Generator

1. Open `Harrison-County-Email-Signature-Generator.html` in a web browser.
2. Choose the Standard or Compact template.
3. Choose a school or department. Its saved contact information will fill automatically.
4. Enter the employee's name, title, email, and any optional details.
5. Review the live preview.
6. Select **Copy for Outlook**.
7. Open Outlook's signature settings and paste the signature.

The **Download .html** button can also save the finished signature as a separate HTML file.

## Add It to a Website

The file is built as a self-contained embed block. Copy its full contents into a custom HTML or embed block that allows HTML, CSS, and JavaScript.

Some website editors remove `<script>` tags or other code for security. If that happens, host this file as its own web page and link to it instead of pasting it into the editor.

## Publish with GitHub Pages

1. Add the HTML file and this `README.md` to a GitHub repository.
2. Rename the HTML file to `index.html` if you want it to be the site's home page.
3. In the repository, open **Settings > Pages**.
4. Choose **Deploy from a branch**.
5. Select the branch and root folder that contain `index.html`.
6. Save the settings and open the web address GitHub provides.

## Update School Information

School information is stored in the `SCHOOLS` array inside the HTML file. Each school uses this format:

```js
{
  key: 'school-key',
  label: 'School Name',
  url: 'https://example.com/logo.png',
  address: '123 Main Street, City, WV 26000',
  phoneOffice: '304-555-0100',
  phoneFax: '304-555-0101',
  web: 'https://www.example.com/'
}
```

Use a unique `key` for every school. Leave `phoneFax` empty when a school does not have a fax number.

## Change the Look

The main colors are CSS variables near the beginning of the file:

```css
--brand: #003366;
--text: #0A0A0A;
--line: #C9D6E2;
--focus: #FF9900;
```

The signature's Outlook-safe divider lines are set with inline border styles:

```css
border-right: 1px solid #C9C9C9;
border-top: 1px solid #C9C9C9;
```

## Browser Storage and Privacy

The generator saves entered information in the browser's `localStorage`. This makes it easier to return to unfinished work, but information may remain on a shared computer.

Use **Clear saved information** after using the generator on a shared device.

## Outlook Notes

- Outlook may block remote logo images until the recipient allows images.
- Logos depend on their hosted image URLs. A changed or removed URL will break that logo.
- Copy the signature from the generator again after changing its design or school data.
- Outlook versions can render HTML differently. Test the signature in both Outlook Web and the desktop app after major changes.

## Maintenance

Review school addresses, phone numbers, fax numbers, website links, and logo URLs on a regular schedule. Test the copy and paste process after every code update.

