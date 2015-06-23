# Example of Custom Markdown Renderer

[![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/sourcejs/Source)

Example plugin with custom Markdown renderer for [SourceJS](http://sourcejs.com).

## Quick start

Install the plugin in `sourcejs/user` folder:

```
npm i sourcejs-example-md-extension --save
```

Prepare markdown options `sourcejs/user/options.js`:

```
module.exports = {
    core: {
        processMd: {
            marked: {
                renderer: require('sourcejs-example-md-extension/custom-renderer')
            }
        }
        ...
    }
    ...
};
```

Or if you want to add new language renderer only:

```
module.exports = {
    core: {
        processMd: {
            languageRenderers: {
                jsx: require('sourcejs-example-md-extension/lang-jsx')
            }
        }
        ...
    }
    ...
};
```