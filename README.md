# webpack-template

A project template for web development.

## NPM scripts

- "test": "jest"
- "build": "webpack --config webpack.prod.js"
- "dev": "webpack serve --open --config webpack.dev.js"
- "deploy": "git subtree push --prefix dist origin gh-pages"

## Dev Dependencies

- "@eslint/css": "^0.9.0"
- "@eslint/js": "^9.29.0"
- "@eslint/json": "^0.12.0"
- "@eslint/markdown": "^6.5.0"
- "babel-jest": "^30.0.4"
- "css-loader": "^7.1.2"
- "eslint": "^9.29.0"
- "globals": "^16.2.0"
- "html-loader": "^5.1.0"
- "html-webpack-plugin": "^5.6.3"
- "jest": "^30.0.4"
- "prettier": "3.5.3"
- "style-loader": "^4.0.0"
- "webpack": "^5.99.9"
- "webpack-cli": "^6.0.1"
- "webpack-dev-server": "^5.2.2"
- "webpack-merge": "^6.0.1"

## Deployment

Make sure everything is committed and run these commands to deploy:

```js
git branch gh-pages
git checkout gh-pages && git merge main --no-edit
npm run build
git add dist -f && git commit -m "Deployment commit"
git subtree push --prefix dist origin gh-pages
git checkout main
```

## Values to change

### package.json

- name, description, main, homepage
- repository > url
- bugs > url

### webpack.common.js

- entry
- output > filename
- plugins > HTMLWebpackPlugin template

### webpack.dev.js

- devServer > watchFiles

### package-lock.json

- run "npm install"
