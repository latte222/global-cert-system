# Global Certification System

A React-based certification operations management system for team testing and collaboration.

## Features

- Dashboard with key metrics
- Product management
- Case tracking and management
- Gantt chart timeline view
- User management
- Mobile-responsive design
- Real-time tweaks and customization

## Project Structure

```
├── index.html              # Main entry point
├── trial/                  # React components
│   ├── db.jsx             # Database and state management
│   ├── ui.jsx             # UI utilities and hooks
│   ├── screens-shell.jsx  # Main layout/shell
│   ├── screens-dash.jsx   # Dashboard screens
│   ├── screens-products.jsx # Products management
│   ├── screens-cases.jsx  # Cases management
│   ├── screens-gantt.jsx  # Gantt chart view
│   ├── screens-users.jsx  # User management
│   ├── tweaks-panel.jsx   # Tweaks configuration UI
│   └── tweaks.jsx         # Tweaks state
├── .gitignore
└── README.md
```

## Getting Started

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/latte222/global-cert-system.git
cd global-cert-system
```

2. Open `index.html` in your browser (no build step required)

### Deployment to Vercel

1. Push this repository to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "Import Project"
4. Select your GitHub repository
5. Click "Deploy"

Your site will be live at `https://global-cert-system.vercel.app` (or your custom domain)

## Technology Stack

- **React 18** - UI framework
- **Babel Standalone** - JSX compilation in the browser
- **Google Fonts** - Typography (Inter, JetBrains Mono)

## Contributing

Team members can test the system at the live Vercel URL. To make changes:

1. Clone the repository locally
2. Edit the component files in the `trial/` folder
3. Commit and push changes to GitHub
4. Vercel will automatically redeploy

## Component Development

Each screen component exports to `window.Screens`:

```javascript
const MyComponent = () => {
  return <div>My component</div>;
};

window.Screens = window.Screens || {};
Object.assign(window.Screens, { MyComponent });
```

This pattern allows components to be loaded in any order via script tags.

## Notes

- No build process required - pure HTML + React in the browser
- All components use Babel standalone for JSX transpilation
- State management is global via `window.Screens` and `window.UI`
- Mobile-responsive design using viewport detection in `useViewport()`

---

**Ready to deploy?** Push this folder to GitHub and connect to Vercel!
