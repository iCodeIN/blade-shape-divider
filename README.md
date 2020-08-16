![You could have one of these on your site without breaking a sweat. Ain't that tasty?](./.github/assets/readme-top-divider.svg?raw=true&sanitize=true "Optional Title")

# Blade shape divider

[![Latest Version on Packagist](https://img.shields.io/packagist/v/leuverink/blade-shape-divider.svg?style=flat-square)](https://packagist.org/packages/leuverink/blade-shape-divider)
[![Total Downloads](https://img.shields.io/packagist/dt/leuverink/blade-shape-divider.svg?style=flat-square)](https://packagist.org/packages/leuverink/blade-shape-divider)

A port of [shapedivider.app](shapedivider.app) for Laravel Blade

## Installation
Laravel 7.0 or higher is required.
You can install the package via composer:

``` bash
composer require leuverink/blade-shape-divider
```

## Usage

``` html
<x-shape-divider shape="waves" />
```
*Just like the original, this component needs to be in a container with `position: relative` in order to work properly.*

### Customization
You may use any of these divider shapes:

`waves`, `waves-opacity`, `curve`, `curve-asymmetrical`, `triangle`, `triangle-asymmetrical`, `tilt`, `arrow`, `split` & `book`

Head over to [shapedivider.app](shapedivider.app) and create a shape you like. Settings can be passed as props. When you're happy with the shape divider you created, simply copy over it's settings like the example below.

``` html
<x-shape-divider
    shape="waves-opacity"
    fill="#EEE"
    :flip="true"
    :invert="true"
    position="bottom"
    height="200px"
    width="150%"
/>
```

### Changing divider color
You may pass any valid color code as the `fill` prop. By default the fill is set to `currentColor`, which means the divider inherits the current font color by default. If you want to use a css class to provide the fill color you may do so:

``` html
<!-- Use the text color text-blue-600 to fill the divider -->
<x-shape-divider shape="waves" class="text-blue-600" />

<!-- Setting the fill color overrides the text color inheritance -->
<x-shape-divider shape="waves" fill="#3182CE" />
```

### Prop defaults
Component props have the following defaults. If your shape uses any of the defaults they don't have to be passed as props.
| name | type | default | available options | example value |
|---|---|---|---|---|
| shape | string | `null` (required) | waves, waves-opacity, curve, curve-asymmetrical, triangle, triangle-asymmetrical, tilt, arrow, split & book | `"shape='waves"` |
| fill | `string` | `currentColor` | Accepts any valid color code. Inherits font color by default | `fill="rgba(255, 138, 0, 0.7)"` |
| flip | boolean | `false` | `true|false` | `:flip="true"` |
| invert | boolean | `false` | `true|false` | `:invert="true"` |
| position | string | `top` | `top|bottom` | `position="bottom"` |
| height | string | `150px` | - | `height="200px"` |
| width | string | `100%` | - | `width="260%"` |

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

This port should be pretty much complete. Any new features not available in the original [shapedivider.app](shapedivider.app) fall outside the scope of this project and will not be merged.
Improvements to the API will be considered.
Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

### Security

If you discover any security related issues, please email willem@leuver.ink instead of using the issue tracker.

## Credits
- [True Style Design (creators of shapedivider.app)](https://truestyledesign.co.uk)
- [Willem Leuverink](https://github.com/gwleuverink)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
