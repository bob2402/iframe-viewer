# IFrame Viewer

A simple web application that allows you to view any webpage in an iframe with custom URL parameters. Perfect for testing, embedding, and sharing web content with specific parameters.

## Features

- 📺 Display any webpage in an iframe
- 🔗 Add custom URL parameters dynamically
- 🚀 Simple to use - just add parameters to the URL
- 📱 Responsive design
- 🔒 Secure iframe implementation with sandbox attributes

## Usage

### Method 1: Direct URL Parameters

Simply add the target URL and any additional parameters to the viewer URL:

```
https://yourusername.github.io/iframe-viewer/?url=https://example.com&param1=value1&param2=value2
```

**How it works:**
- `url` - The base URL of the page you want to display
- Any additional parameters (like `param1`, `param2`) will be automatically appended to the target URL

**Example:**
```
https://yourusername.github.io/iframe-viewer/?url=https://example.com&foo=bar&page=2
```

This will display `https://example.com?foo=bar&page=2` in the iframe.

### Method 2: Interactive Input

1. Open the viewer in your browser
2. Enter the URL in the input field
3. Click "Load URL" or press Enter
4. The page will be displayed in the iframe with any URL parameters from the current page

## Deployment on GitHub Pages

This project is designed to work seamlessly with GitHub Pages:

1. **Fork or clone this repository**

2. **Enable GitHub Pages:**
   - Go to your repository Settings
   - Navigate to "Pages" section
   - Under "Source", select "GitHub Actions"

3. **Deploy:**
   - The included GitHub Actions workflow (`.github/workflows/pages.yml`) will automatically deploy to GitHub Pages when you push to the main branch
   - Alternatively, you can trigger the workflow manually from the Actions tab

4. **Access your viewer:**
   - Once deployed, access it at: `https://yourusername.github.io/iframe-viewer/`

## Local Development

To test locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/iframe-viewer.git
   cd iframe-viewer
   ```

2. Open `index.html` in your browser or use a local server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Or Python 2
   python -m SimpleHTTPServer 8000
   
   # Or Node.js
   npx http-server
   ```

3. Navigate to `http://localhost:8000/?url=https://example.com`

## Security Notes

- The iframe uses sandbox attributes for security
- Always be cautious about what URLs you load
- Some websites may prevent being displayed in iframes (X-Frame-Options)

## Examples

### View Google with a search query:
```
?url=https://www.google.com/search&q=github
```

### View a documentation page:
```
?url=https://docs.github.com
```

### YouTube video embed:
```
?url=https://www.youtube.com/embed/VIDEO_ID
```

## License

MIT License - feel free to use this project however you'd like!