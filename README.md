Asgar ![build](https://travis-ci.com/stefanbc/Asgar.svg?branch=master)
==

A 2 column, free and open source theme for Ghost.

Instalation
--

1. Download the theme from GitHub.
2. Upload the theme as described in the [Ghost Documentation](https://docs.ghost.org/concepts/config/).
3. This theme has multiple custom pages: `about`, `projects` and `speaking`. Checkout the Ghost [docs](https://docs.ghost.org/api/handlebars-themes/context/page/#templates) for more info about custom pages. To customize the data, on the right side, in the `projects` and `speaking` pages you'll first need to add this to your `routes.yaml` file, bellow the `routes` key:
```
  /custom/api/:
    permalink: /custom/api/
    template: api
    content_type: json
```
More info about the `routes.yaml` file [here](https://docs.ghost.org/api/handlebars-themes/routing/).
After that you can customize the `api.hbs` file with your data, just make sure the structure remains the same.

4. Additionally you should replace all the image in the `assets/images` folder. You can use [this useful tool](http://realfavicongenerator.net/).

After you've completed the steps above, you can zip the theme and upload it.

**This theme is compatible with Ghost 2.x.**

Developers
--

You can install all the theme dependencies using:

```
yarn install
```

Available script you can run for development and production:

* `yarn dev` - will build the whole theme for testing.
* `yarn prod` - will build the whole theme for production.
* `yarn watch` - will watch for any sass file modifications and will build.
* `yarn zip` - will zip the theme for production.
* `yarn validate` - will validate the zip created with the previous command.
* `yarn deploy` - will build the theme for production, zip and validate.
