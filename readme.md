# Ungic SASS props

**ungic-sass-props** - this is a Dart SASS module allows you to work with properties by combining with standard values and provides an api to get project properties

## Get Started

First add [ungic-sass-props](https://npmjs.com/package/ungic-sass-utils) npm package to your project

```
npm install "ungic-sass-props"
```

and use it as a module in your sass projects:

```
@use "ungic-sass-props" with (
	$properties: (
		....
	)
)
```

See *examples/project.scss* directory of this package

## Documentation

### $properties
- **Type:** `variables`

	Contains passed project properties

### $default_properties
- **Type:** `variables`

	Contains all default project properties

### prop($prop, $args...)
- **Type:** `function`

- **Parameters:**
	- **$prop** <span class="mark">string</span> - property name
	- **$args** <span class="mark">Number</span> - any arguments for property handler (see property-handlers.scss and props-handlers.scss)
- **Usage:** `prop($prop, $args...)`

	Get processed value by property name

### props($merge_with_defaults: false), properties($merge_with_defaults: false)
- **Type:** `function`

- **Parameters:**
	- **$merge_with_defaults** <span class="mark">boolean</span> - merge default properties with project properties or not
- **Usage:** `props()`

	Get a map of all properties, if "true" is passed, the default properties will be merged with the project properties
