# superset-plugin-chart-pie-chart-custom

This is the Superset Plugin Chart Pie Chart Custom Superset Chart Plugin.

### Usage

To build the plugin, run the following commands:

```
npm ci
npm run build
```

Alternatively, to run the plugin in development mode (=rebuilding whenever changes are made), start the dev server with the following command:

```
npm run dev
```

To add the package to Superset, go to the `superset-frontend` subdirectory in your Superset source folder (assuming both the `superset-plugin-chart-pie-chart-custom` plugin and `superset` repos are in the same root directory) and run
```
npm i -S ../../superset-plugin-chart-pie-chart-custom
```

After this edit the `superset-frontend/src/visualizations/presets/MainPreset.js` and make the following changes:

```js
import { SupersetPluginChartPieChartCustom } from 'superset-plugin-chart-pie-chart-custom';
```

to import the plugin and later add the following to the array that's passed to the `plugins` property:
```js
new SupersetPluginChartPieChartCustom().configure({ key: 'superset-plugin-chart-pie-chart-custom' }),
```

After that the plugin should show up when you run Superset, e.g. the development server:

```
npm run dev-server
```
