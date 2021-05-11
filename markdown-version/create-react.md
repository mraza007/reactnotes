## Create ReactApp
- Create React App is a utility script that,
  - Creates a skeleton react project.
  - Sets it up so that JS files are run through Babel automatically.
  - lets us use super modern JS features/Idioms.
  - makes testing and deployment easier.

## Installation.

- You can install react using `npm`.
- You can also install react using `npx`.
- `npx create-react-app <app_name>`

```sh
├── package.json
├── package-lock.json
├── public //Rarely needs editing
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
├── README.md
└── src // This is where React Stuff goes
    ├── App.css //CSS for component
    ├── App.js //Example Component
    ├── App.test.js // Component tests 
    ├── index.css // site-wide css
    ├── index.js //start of JS
    ├── logo.svg // React Logo
    ├── reportWebVitals.js
    └── setupTests.js
```

- React Comes with WebPack.
  - Webpack enables module importing/exporting.
  - Packages up all CSS/Images/JS into a single file for the browser.
  - reduces http requests for performance,
  - hot reloading 
  - enables easy testing and deployment.

## React Conventions

- Each component goes into a separate file. For Example `src/Car.js` for Car Component.
- Components Extends Component (imported from react)
  - Export Component as a default object.
- `App.js` is the top component

## Assets and CSS in ReactApp.
- Make `CSS` file for each component. For instance, `House.css` for House object.
- Conventional to add `className="House"` onto **House** div.
  - And use that as prefix for sub-items to style:
   
   ```html
   <div className="House">
   <p className="House-title"> {this.props.title} </p>
   <p className="House-address"> {this.props.addr} </p>
  </div> 

   ```
