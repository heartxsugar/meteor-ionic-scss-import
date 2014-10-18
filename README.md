# Ionic SCSS Import for Meteor

These are the SCSS files for the [Ionic Mobile Framework](http://ionicframework.com/) converted to `*.import.scss` to be used in Meteor apps.

## Usage
1. Add the `fourseven:scss` package:

`meteor add fourseven:scss`

2. Copy all the files in this repo into `/client/stylesheets/ionic`

3. Import the main `ionic.import.scss` file in your main `.scss` file:

```
@import "./ionic/ionic.import.scss";
```

## Theming via Variables

You can customize the variables inside of `_variables.import.scss`, but I prefer to override them in a separate file. Here's how I set up my custom variables and mixins:

### stylesheets/_mixins.import.scss
```
// Ionic Mixins
@import "./ionic/_mixins.import.scss";

// Add Custom Mixins Here:
```

### stylesheets/_variables.import.scss
```
// Ionic Variables
@import "./ionic/_variables.import.scss";

// Add Custom/Override Variables Here:
$positive: #68BB38;
```

### stylesheets/global.scss
```
@import "./ionic/ionic.import.scss";

@import './_mixins.import.scss';
@import './_variables.import.scss';

html, body {
}
```
