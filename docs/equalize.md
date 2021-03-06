# Equalize

A jQuery plugin for equal dimensions.

* [Use](#use)
* [Options](#options)
* [Methods](#methods)
* [CSS](#css)

## Use 

#### Main

```markup
equalize.js
equalize.css
```

#### Dependencies

```markup
core.js
mediaquery.js
```

### Basic

By default, Equalize will set the height of an element's children to the largest of the group:

```javascript
$(".target").equalize();
```

```markup
<div class="target">
	<div>...</div>
	<div>...</div>
	<div>...</div>
</div>
```

### Targets

Specify a valid `target` selector to equalize specific child elements:

```javascript
$(".target").equalize({
	target: ".child"
});
```

```markup
<div class="target">
	<div>
		<p class="child">...</p>
	</div>
	<div>
		<p class="child">...</p>
	</div>
	<div>
		<p class="child">...</p>
	</div>
</div>
```

### Width

Set the `protperty` to width to Equalize the widths of elements, rather than heights:

```javascript
$(".target").equalize({
	property: "width"
});
```

## Options

Set instance options by passing a valid object at initialization, or to the public `defaults` method. Custom options for a specific instance can also be set by attaching a `data-equalize-options` attribute to the target elment. This attribute should contain the properly formatted JSON object representing the custom options.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| `maxWidth` | `string` | `'Infinity'` | Width at which to auto-disable plugin |
| `minWidth` | `string` | `'0'` | Width at which to auto-disable plugin |
| `property` | `string` | `"height"` | Property to size; 'height' or 'width' |
| `target` | `string` | `null` | Target child selector |

## Methods

Methods are publicly available to all active instances, unless otherwise stated.

### defaults

Extends plugin default settings; effects instances created hereafter.

```javascript
$.equalize("defaults", { ... });
```

#### Parameters

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| `options` | `object` | `{}` | New plugin defaults |

### destroy

Removes plugin instance.

```javascript
$(".target").equalize("destroy");
```

### disable

Disables instance of plugin

```javascript
$(".target").equalize("disable");
```

### enable

Enables instance of plugin

```javascript
$(".target").equalize("enable");
```

## CSS

| Class | Type | Description |
| --- | --- | --- |
| `.fs-equalize-element` | `element` | Target Element |

