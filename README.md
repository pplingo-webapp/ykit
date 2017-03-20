# Ykit [![CircleCI](https://circleci.com/gh/YMFE/ykit.svg?style=shield)](https://circleci.com/gh/YMFE/ykit)

It's a pain to set webpack configs for various apps. Ykit offers reliable encapsulated configuration and help you manage it. You can start to run an app easily and customize your project through ykit's flexable config.

## Quick Start

1. `npm install ykit -g`
2. `mkdir ykit-app && cd ykit-app`
3. `ykit init`
4. `cd .. && ykit server`
5. Check out `localhost/ykit-app/index.html`

After setting up your project, there will be the config file called `ykit.js` in your project root directory：

```javascript
module.exports = {
    plugins: [],
    config: {
        export: ['./scripts/index.js', './styles/index.css'],
        modifyWebpackConfig: function modifyWebpackConfig(baseConfig) {
            // edit webpack configs
            return baseConfig;
        }
    },
    hooks: {},
    commands: []
};
```

## Config Options

- **plugins** - To configure plugins inside of a configuration file, use the plugins key, which contains a list of plugin names. Every plugin encapsulates respective webpack configs.
- **config** - Config object:
    - **exports** - Asset entries.
    - **modifyWebpackConfig** - Callback function for editing kyt's Webpack configs.

## Document

Visit [http://ued.qunar.com/ykit/][1] For more doc.

[1]: http://ued.qunar.com/ykit/index.html
