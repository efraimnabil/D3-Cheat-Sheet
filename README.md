# D3-Cheat-Sheet

This is a cheat sheet for D3.js. It is a work in progress and will be updated as I learn more about D3.

D3 is a JavaScript library for creating dynamic and interactive data visualizations in the browser.

## Table of Contents

- [Basics](#basics)
- [Selections](#selections)

## Basics

### Selecting Elements

```js
d3.select('body') // Selects the first element that matches the selector
d3.selectAll('div') // Selects all elements that match the selector
```

### Appending Elements

```js
d3.select('body')
  .append('div') // Appends a div to the body
```

### Removing Elements

```js
d3.select('body')
  .remove() // Removes the body
```

### Changing Styles

```js
d3.select('body')
  .style('background-color', 'black') // Changes the background color of the body to black
```

### Changing Attributes

```js
d3.select('body')
  .attr('class', 'container') // Adds a class of container to the body
```

### Changing Text

```js
d3.select('body')
  .text('Hello World') // Changes the text of the body to Hello World
```

### Changing HTML

```js
d3.select('body')
  .html('<h1>Hello World</h1>') // Changes the HTML of the body to an h1 with the text Hello World
```

### Changing Classes

```js
d3.select('body')
  .classed('container', true) // Adds a class of container to the body

d3.select('body')
    .classed('container', false) // Removes the class of container from the body
```

### Chaining Methods 

```js
d3.select("body").selectAll("div")
  .data(dataset)
  .enter()
  .append("div")
  .attr("class", "bar")
```

### Changing Properties and Attributes
#### attr vs Properties

```js
d3.select('body')
  .attr('value', 'Hello World') // Changes the value of the body to Hello World

d3.select('body')
    .property('value', 'Hello World') // Changes the value of the body to Hello World
```


## Selections

### Selecting Elements

```js
d3.select('body') // Selects the first element that matches the selector
d3.selectAll('div') // Selects all elements that match the selector
```

### Filtering Elements

```js
d3.selectAll('div')
  .filter('.container') // Filters the selection to only include elements with a class of container
```

### Sorting Elements

```js
d3.selectAll('div')
  .sort(function(a, b) { // Sorts the selection based on the return value of the function
    return a - b;
  })
```

### Data Joins

```js
d3.selectAll('div')
  .data(dataset) // Binds the data to the selection
```

### Data Joins with Key Functions

```js
d3.selectAll('div')
  .data(dataset, function(d) { // Binds the data to the selection using a key function
    return d.id;
  })
```

### Enter Selection

```js
d3.selectAll('div')
  .data(dataset)
  .enter() // Returns a selection containing placeholder nodes for each data point
```
