# ATH Framework

ATH Framework is a D3.js-based interactive tree for curating and browsing your own research resources. Fork it, load your data, and publish it to GitHub Pages at `https://atharvax28.github.io/ath-framework/`.

## Features

- Interactive tree visualization using D3.js
- Click nodes to expand/collapse categories
- Click links to open in new tabs
- Dark mode toggle
- Fully customizable structure

## Local setup (Git Bash friendly)

```bash
# 1. Clone and enter the project
git clone https://github.com/atharvax28/ath-framework.git
cd ath-framework/ath-framework

# 2. Install dependencies (includes d3 vendor copy via postinstall)
npm install

# 3. Start a local preview server
npm start
# → browse http://localhost:8000
```

## Customization

### Adding Your Own Data

Edit the `public/data.json` file to customize the tree. The structure follows this format:

```json
{
  "name": "Category Name",
  "type": "folder",
  "children": [
    {
      "name": "Subcategory",
      "type": "folder",
      "children": [
        {
          "name": "Link Name",
          "type": "url",
          "url": "https://example.com"
        }
      ]
    }
  ]
}
```

### Structure Rules

- **Folders**: Use `"type": "folder"` for categories and subcategories. Folders can contain other folders or URLs.
- **URLs**: Use `"type": "url"` for actual links. Must include a `"url"` field with the full URL.
- **Nesting**: You can nest folders as deeply as you want to organize your resources.

### Example Structure

```json
{
  "name": "My Resources",
  "type": "folder",
  "children": [
    {
      "name": "Work",
      "type": "folder",
      "children": [
        {
          "name": "Project Dashboard",
          "type": "url",
          "url": "https://example.com/dashboard"
        }
      ]
    }
  ]
}
```

## Customization tips

1. **Title & hero text**: Edit the `<title>` tag and `#header` copy in `public/index.html`.
2. **Theme**: Tweak colors and fonts in `public/css/arf.css`.
3. **Layout/behaviour**: Update `public/js/arf.js` for spacing, animation, or new interactions.
4. **Data**: Keep `"type": "folder"` for nested categories and `"type": "url"` for leaves, each with a `url`.

## Directory layout

```
ath-framework/
├── package.json
├── README.md
└── public/
    ├── index.html
    ├── data.json
    ├── css/
    │   └── arf.css
    └── js/
        ├── arf.js
        ├── d3.v3.min.js
        └── vendor/d3/d3.min.js
```
## Notes

- The framework uses D3.js v3 for the tree visualization
- All links open in new tabs
- The tree starts collapsed - click nodes to expand
- Dark mode can be toggled using the button in the top right

Enjoy organizing your ATH resources!


