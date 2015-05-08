# polymer-spline-graph

**This element is compatible with Polymer 0.5.**

__Example:__

```
	<polymer-element name="polymer-spline-graph-demo">
		<template>
			<polymer-spline-graph
				chartTitle="Spline Chart Demo"
				categories="{{ categories }}"
				series="{{ series }}"
				zoneLength="{{ zoneLength }}" ></polymer-spline-graph>
		</template>
		<script src="../lodash/lodash.js"></script>
		<script>
			Polymer({
				publish: {
					categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
					series: [
						{
							name: 'Line 1',
							data: [29.9, 71.5, 106.4, 129.2, 144.0, 176.0, 135.6, 148.5, 216.4, 194.1, 95.6, 54.4]
						}, {
							name: 'Line 2',
							data: [54.4, 29.9, 71.5, 106.4, 129.2, 144.0, 176.0, 135.6, 148.5, 216.4, 194.1, 95.6]
						}
					],
					zoneLength: 8,
				}
			});
		</script>
	</polymer-element></polymer-element>
	<polymer-spline-graph-demo></polymer-spline-graph-demo>
```

# General Attributes

### `series`

Array of objects containing name and data points.
```
[
	{
		name: 'Line 1',
		data: [29.9, 71.5, 106.4, 129.2, 144.0, 176.0, 135.6, 148.5, 216.4, 194.1, 95.6, 54.4]
	}, {
		name: 'Line 2',
		data: [54.4, 29.9, 71.5, 106.4, 129.2, 144.0, 176.0, 135.6, 148.5, 216.4, 194.1, 95.6]
	}
]
```

### `chartTitle`

Title displayed above graph. Default `null`

### `yAxisTitle`

Title displayed left of graph. Default `null`

### `width`

Container width. Default `400`

### `height`

Container width. Default `400`

### `options`

Object to extend highcarts

# Spline Graph

### `categories`

Labels below x axis

### `zoneLength`

Break point along the x axis where the solid line becomes dotted. Default `null`

# Live Spline Graph

### `onLoad`

Function getting adding new data to the series.

### `timezoneOffset`

Timezone offset. Example PST is `8`

### `xAxislInterval`

The approximate pixel interval of the tick marks.