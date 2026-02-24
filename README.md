# Marriage Certificate Generator

A beautiful, web-based tool for generating Islamic marriage certificates as PDF documents. Built with HTML, CSS, and JavaScript - perfect for GitHub Pages hosting.

## Features

- 📝 **Easy Form Interface** - Simple form to input all required information
- 🎨 **Custom Certificate Design** - Uses your own certificate template image as background
- 📱 **Responsive Design** - Works on desktop and mobile devices
- 📄 **PDF Generation** - High-quality PDF output using html2pdf.js
- ✨ **Professional Styling** - Modern, clean interface with smooth animations
- 🔒 **Client-Side Only** - All processing happens in the browser, no server required

## Live Demo

[View the live application](https://yourusername.github.io/marriage-certificate)

## How to Use

1. Fill in all required fields:
   - Groom's full name
   - Bride's full name
   - Mahr amount
   - Ceremony date
   - Imam's full name

2. Click "Generate Certificate"
3. Review the generated certificate
4. Click "Download PDF" to save your certificate

## Setup for GitHub Pages

1. **Fork or clone this repository**
   ```bash
   git clone https://github.com/yourusername/marriage-certificate.git
   cd marriage-certificate
   ```

2. **Replace the certificate image**
   - Replace `certificate.png.jpeg` with your own certificate template
   - Make sure the image dimensions work well (recommended: 8.5" x 11" aspect ratio)

3. **Adjust text positioning** (if needed)
   - Edit the CSS classes in `index.html`:
     - `.groom-name`, `.bride-name`, `.mahr-amount`, `.ceremony-date`, `.imam-name`
   - Modify `top`, `left`, `right`, `bottom` values to match your certificate layout

4. **Enable GitHub Pages**
   - Go to your repository settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Save the settings

5. **Access your site**
   - Your site will be available at: `https://yourusername.github.io/repository-name`

## Customization

### Certificate Template
- Replace `certificate.png.jpeg` with your certificate design
- Ensure the image is high resolution for best PDF quality

### Text Positioning
Adjust the CSS positioning classes to match your certificate layout:

```css
.groom-name {
  top: 300px;    /* Distance from top */
  left: 150px;   /* Distance from left */
  font-size: 24px;
}
```

### Styling
- Modify colors, fonts, and layout in the `<style>` section
- Customize the form appearance and certificate overlay

## Technical Details

- **HTML5** - Semantic markup and modern form inputs
- **CSS3** - Flexbox, Grid, and responsive design
- **Vanilla JavaScript** - No frameworks, lightweight and fast
- **html2pdf.js** - Client-side PDF generation library

## Browser Support

- Chrome/Edge (recommended)
- Firefox
- Safari
- Mobile browsers

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - feel free to use this project for personal or commercial purposes.

## Support

If you encounter any issues or have questions, please open an issue in the GitHub repository.