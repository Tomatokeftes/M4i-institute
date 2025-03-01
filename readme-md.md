# Research Institute Website

This repository contains the website for our Research Institute, hosted on GitHub Pages. The site includes information about our institute, available instruments, and submission forms.

## Files Included

- `index.html` - Home page with institute information and latest news
- `instruments.html` - Page displaying available research instruments
- `forms.html` - Page with downloadable and online submission forms
- `README.md` - This documentation file

## Setup Instructions

### 1. Create a GitHub Repository

1. Log in to your GitHub account
2. Click on the "+" icon in the top right corner and select "New repository"
3. Name your repository (e.g., `research-institute` or `[your-username].github.io` for a user site)
4. Make the repository public
5. Click "Create repository"

### 2. Upload Website Files

#### Option 1: Using GitHub's Web Interface

1. Navigate to your newly created repository
2. Click on "Add file" > "Upload files"
3. Drag and drop or select the HTML files from your computer
4. Add a commit message (e.g., "Initial website upload")
5. Click "Commit changes"

#### Option 2: Using Git Commands

1. Clone the repository to your local machine:
   ```
   git clone https://github.com/yourusername/your-repository-name.git
   ```
2. Copy your HTML files into the cloned directory
3. Add, commit, and push the files:
   ```
   git add .
   git commit -m "Initial website upload"
   git push origin main
   ```

### 3. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings"
3. Scroll down to the "GitHub Pages" section
4. Under "Source", select the branch you want to deploy (usually "main")
5. Click "Save"
6. After a few moments, your site will be published at the URL shown in the GitHub Pages section (typically `https://yourusername.github.io/your-repository-name/`)

## Password Protection

The site includes basic JavaScript password protection. However, it's important to note that this is client-side protection only and not fully secure for truly sensitive information. The current password is set to `research2025`.

To change the password:

1. Open each HTML file (`index.html`, `instruments.html`, `forms.html`)
2. Find the `checkPassword()` function in the JavaScript section near the bottom
3. Change the `correctPassword` variable value to your desired password
4. Save the files and upload them to your repository

```javascript
function checkPassword() {
    const password = document.getElementById('password').value;
    const correctPassword = "your-new-password"; // Change this line
    
    if (password === correctPassword) {
        // Store in session storage that user is authenticated
        sessionStorage.setItem('authenticated', 'true');
        document.getElementById('passwordModal').style.display = 'none';
    } else {
        alert('Incorrect password. Please try again.');
    }
}
```

## Security Considerations

The current password protection uses client-side JavaScript and session storage. This means:

1. The password is visible in the source code of your pages
2. This is not suitable for highly sensitive information
3. Users can bypass the protection by viewing the source code

For stronger security, consider:

- Using a server-side solution with proper authentication
- Using GitHub's private repository feature and controlling access at the repository level
- Implementing a third-party authentication service

## Customization

- **Content**: Edit the HTML files to update text, images, and links
- **Styling**: Modify the CSS within the `<style>` tags in each HTML file
- **Structure**: Add or remove sections as needed
- **Forms**: Update the form fields based on your institute's requirements

## Maintenance

To update your site:

1. Make changes to the local files
2. Commit and push to GitHub (or upload via the web interface)
3. GitHub Pages will automatically update your live site

## Support

If you need assistance with this site, please contact the IT department or the website administrator.
