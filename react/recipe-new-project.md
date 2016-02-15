Preparing global utilities:
- sudo npm install babel webpack -g

Creating a new react application:
- npm init
- npm --save react react-dom
- npm --save-dev babel-core babel-loader babel-preset-es2015 babel-preset-react

Configuring webpack:

```javascript
module.exports = {
	entry: "./app/components/Main.js",
	output: {
		filename: "public/bundle.js"
	},
	module: {
		loaders: [
			{
				test: /\.jsx?$/,
				exclude: /(node_modules|bower_components)/,
				loader: 'babel',
				query: {
					presets: ['react', 'es2015']
				}
			}
		]
	}
}
```