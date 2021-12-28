# strapi-plugin-wysiwyg-template
A bootstrap template for developing Strapi WYSIWYG editor plugin

## How to use

1. Create a new repo using this template, naming it after your plugin. For example, if your plugin is called `my-editor`, the new repo's name should be `strapi-plugin-wysiwyg-my-editor`.
2. Clone the new repo into you strapi project's plugin folder, making the following file structure:
   ```
   <strapi project root>
   ├── src
   │   └── plugins
   │       └── strapi-plugin-wysiwyg-my-editor
   └── config
       └── plugins.js
   ```
3. Edit the file *config/plugin.js* of you strapi project by adding this setting:
   ```js
   module.exports = {
     // ...
     'strapi-plugin-wysiwyg-my-editor': {
       enabled: true,
       resolve: './src/plugins/strapi-plugin-wysiwyg-my-editor'
     },
     // ...
   }
   ```
4. Edit the *package.json* of the plugin by renaming all `template`s to `my-editor`s.
5. To implement a new editor, you'll need to start your work on the file *admin/src/components/Editor/index.js*.
6. Start Strapi with `yarn develop --watch-admin` and go!