## Angular Heremaps
[![Build Status](https://travis-ci.org/mjaric/ng2-heremaps.svg?branch=master)](https://travis-ci.org/mjaric/ng2-heremaps)
[![npm](https://badge.fury.io/js/ng2-heremaps.svg)](https://badge.fury.io/js/ng2-heremaps)

Allows you to interact with the HERE Maps API for JavaScript through Angular.

Check [API Documentation](https://mjaric.github.io/ng2-heremaps/)

## Install

```bash
npm install ng2-heremaps @types/heremaps --save
```

## Setup

**step 1:** add ng2-heremaps to app NgModule

```typescript
import { HereMapsModule } from 'ng2-heremaps';

@NgModule({
  imports: [
    ...
    HereMapsModule.forRoot({
      apiKey: 'your heremaps API key',
      appId: 'your heremaps API id',
      apiVersion: '3.0',
      libraries: ['core', 'service']
    }),
    ...
  ],
  bootstrap: [AppComponent],
  declarations: [AppComponent]
})
class AppModule {}
```

## Use

### Basic map
```html
 <div style="height: 400px; width: 600px;">
    <heremap [center]="{latitude: 40.730610, longitude: -73.935242}"></heremap>
  </div>
```

#### Inputs

| Input                  | Type                           | Default           | Description                                                                 |
| ---------------------- | ------------------------------ | ----------------- | --------------------------------------------------------------------------- |
| `autoFitMarkers`         | `boolean`                    | true              | Should map auto resize bounds to current set of markers                     |
| `backgroundColor`        | `string`                     | transparent       | This color will be visible when tiles have not yet loaded as the user pans. |
| `center`                 | `LatLng` or `Location`       | **REQUIRED**      | The initial Map center.                                                     |
| `enableDoubleClickZoom`  | `boolean`                    | true              | Enables/disables zoom and center on double click.                           |
| `draggable`              | `boolean`                    | true              | If false, prevents the map from being dragged.                              |
| `keyboardShortcuts`      | `boolean`                    | true              | If false, prevents the map from being controlled by the keyboard.           |
| `scrollwheel`            | `boolean`                    | true              | If false, disables scrollwheel zooming on the map.                          |
| `zoom`                   | `number`                     | 5                 | Map zoom level                                                              |
| `minZoom`                | `number`                     | null              | The minimum zoom level which will be displayed on the map.                  |
| `maxZoom`                | `number`                     | null              | The maximum zoom level which will be displayed on the map.                  |
| `disableDefaultUI`       | `boolean`                    | false             | Enables/disables all default UI.                                            |
| `mapTypeControl`         | `boolean`                    | false             | Enabled/Disabled state of the Map type control.                             |
| `rotateControl`          | `boolean`                    | false             | Enabled/Disabled state of the Rotate control.                               |
| `scaleControl`           | `boolean`                    | true              | Enabled/Disabled state of the Scale control.                                |
| `streetViewControl`      | `boolean`                    | false             | Enabled/Disabled state of the Street View Pegman control.                   |
| `animateZoom`            | `boolean`                    | true              | Enabled/Disabled zoom animation.                                            |
| `zoomControl`            | `boolean`                    | true              | Enabled/Disabled state of the Zoom control.                                 |

### Directives
There are directives for directions, markers, and polylines. Please see the files directly to see the available inputs and outputs.
