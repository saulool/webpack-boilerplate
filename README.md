# webpack-boilerplate
Webpack boilerplate to kickstart your project

##What's included?
This boilerplate comes with the following features:
- Dependency injection into your HTML file
- SASS compiler & SASS linter
- Twitter Bootstrap 3
- Caching features (adding hash do filename and then only change the hash if the file's content have changed)
- jQuery
- Babel

##What do I need to change?
- Choose the name of your destination folder (this is the folder where all the bundles will be compiled into) and then rename the name dist to the name that you want.

<pre>
output: {
  	path: path.resolve(__dirname, '<b>dist</b>'),
    filename: '[name].[chunkhash].js'
  }
</pre>

<pre>
devServer: {
	contentBase: "./<b>dist</b>"
}
</pre>

- Define the vendors and the name of your bundle.

<pre>
entry: {
	<b>bundle: __dirname + '/src/index.js'</b>,
	<b>vendor: ['babel-polyfill']</b>
}
</pre>

- And finally rename your css bundle to the name that you want.

<pre>
const extractSCSS = new ExtractTextPlugin('<b>styles.css</b>');
</pre>

After that you will need to import your packages into your entry javascript file