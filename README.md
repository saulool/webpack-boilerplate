# webpack-boilerplate
Webpack boilerplate to kickstart your project

##What's included?
This boilerplate comes with the following features:
- Dependency injection into your HTML file
- SASS compiler & SASS linter
- Twitter Bootstrap 3
- Caching features (adding hash do filename and then only changes if the file's content changes)
- jQuery
- Babel

##What do I need to change?
- Choose the name of your destination folder (this is the folder where all the bundles will be compiled into) and then rename the name dist to the name that you want.

```
output: {
  	path: path.resolve(__dirname, '**dist**'),
    filename: '[name].[chunkhash].js'
  }
```

```
devServer: {
	contentBase: "./**dist**"
}
```

- Define the vendors and the name of your bundle.

```
entry: {
	**bundle: __dirname + '/src/index.js'**,
	**vendor: ['babel-polyfill']**
}
```

- And finally rename your css bundle to the name that you want.

```
const extractSCSS = new ExtractTextPlugin('**styles.css**');
```

After that you will need to import your packages into your entry javascript file