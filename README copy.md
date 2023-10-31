# Otorp.JS
[![Latest Release](https://gitlab.com/tdj.dev/otorp/-/badges/release.svg)](https://gitlab.com/tdj.dev/otorp/-/releases)
[![pipeline status](https://gitlab.com/tdj.dev/otorp/badges/main/pipeline.svg)](https://gitlab.com/tdj.dev/otorp/-/commits/main)

At the heart of our philosophy lies the intent to reuse native code before delving into custom solutions. Hence, this project embarks on its journey with a focus on aliases and extended methods — the bedrock of Otorp.js.

## Simplify and Enhance Your Web Development

Otorp.js is a powerful, lightweight, and versatile JavaScript library designed to simplify and enhance your web development experience. It provides a set of aliases for native methods and shares them between native JavaScript objects to enhance productivity and streamline your code. Otorp.js is built with simplicity and ease of use in mind, enabling developers to write cleaner and more concise code.

## Installation

Incorporating Otorp.js into your project is a breeze. Simply add the following script tag to your HTML file:

```html
<script src="path/to/otorp.min.js"></script>
```

## Getting Started

Once Otorp.js is included in your project, you can immediately start leveraging its methods directly on DOM elements and intance of other native constructor.

### Examples

```javascript
// Add a class to an element
const elem = document.getElementById('myElement');
elem.addClass('highlight');

// Check if an element has a specific class
if (elem.hasClass('highlight')) {
  console.log('The element has the class "highlight".');
}

// Perform an action on each element in an HTMLCollection
const elements = document.getElementsByClassName('items');
elements.setAttr('data-type', "highlighted");
```

## Features

### Configuration Settings Support  
*Empowering Your Coding Experience*

In Otorp.js, you're not just using a library; you're shaping it to suit your coding preferences. We're excited to introduce optional configuration settings that give you the power to customize Otorp.js according to your unique style and needs. With configuration settings support, don't learn Otorp.js; make it learn you.

**Custom Method Prefix**  
*Experience Flexibility and Uniqueness*

Through Configuration Settings Support, Otorp.js introduces the Custom Method Prefix option. This enhancement provides you with heightened control and flexibility. This configuration setting is particularly valuable in preventing potential conflicts with upcoming JavaScript updates or other libraries. By defining a method prefix during initialization, developers can maintain the uniqueness of Otorp.js endpoints, avoiding clashes with emerging JavaScript features.

**Casing Convention Preference**  
*Enhance Clarity and Harmony*

In addition to the Custom Method Prefix, Otorp.js offers the Casing Convention Preference option. This configuration setting empowers you to choose the naming convention for Otorp.js endpoints. This innovative feature enhances your coding experience by providing flexibility in feature naming, ensuring your code aligns seamlessly with your chosen coding style.

**Utilizing the Configuration Settings**
*A Smooth Integration Process*

To harness the power of the configuration settings, follow these straightforward steps:

1. During the inclusion of the Otorp.js library, initialize it with your desired configuration settings:

```html
<script>
  const otorpConfig = {
    prefix: '$', // Define your custom prefix here
    case: 'PascalCase' // Define your casing convention here 
  };
</script>

<script src="path/to/otorp.min.js"></script>
```

2. After initialization, the library will format its features according to the chosen configuration:

```javascript
const elem = document.getElementById('myElement');
elem.$AddClass('highlight'); // 'addClass' becomes '$AddClass'

if (elem.$HasClass('highlight')) {
  console.log('The element has the class "highlight".');
}
```

In this demonstration, the `PascalCase` casing convention and the `$` method prefix. You have the freedom to substitute:
 - `$` with an alternative prefix of your choice, such as `_`, `myPrefix`, or any other.
 -  `PascalCase` with other supported casing conventions (camel, pascal, and snake case).
By embracing these features, you tailor Otorp.js to match your coding style and ensure a harmonious development experience. Explore the possibilities with Otorp.js configuration settings that put you in the driver's seat.

### Document Object Model

- **DOM Manipulation**:
  - Aliases for Native Methods: Providing shorthand methods for common DOM manipulations.
  - Batch Operation: Enabling batch operations on collections like `HTMLCollection` and `NodeList`.

```javascript
// HTML classes
elem.addClass('highlight');
elem.hasClass('highlight');
elem.toggleClass('highlight');
elem.replaceClass('dark', 'light');
elem.removeClass('highlight');

// HTML Attributes
elem.setAttr('data-type', "highlighted");
elem.getAttr('data-type');
elem.removeAttr('data-type');

// Selectors
document.query('.class');
document.querys('.class');
document.selectId('foo');
document.selectClass('foo');
document.selectTag('foo');
document.selectName('foo');

// Mutation
elem.push(node);
elem.rm(node);
elem.replace(node);
elem.insert(position, node);
elem.shift(node);
elem.unshift(node);

// Batch Operation ( alway return undefined )
elements.setAttr('data-type', "highlighted"); // Will set the data-type attribute on all children

```

### Helpers

- **Objects and Data Structures**:
  - Array-Like Enhancements: Empower `HTMLCollection` and `NodeList` with extended `Array` methods, enabling streamlined usage of functions like `reduce`, `every`, etc. Effortlessly apply these operations using intuitive syntax, e.g., `collections.map(fn)`.

```javascript
// Array-Like Enhancements
elems.every(elem => elem.hidden);
elems.each(elem => { /* do something */ }); // alias for forEach
elems.some(elem => elem.checked);
elems.map(elem => elem.parentNode);
elems.reduce((acc, elem) => acc += elem.children.length, 0);
elems.find(elem => elem.id === "foo");
elems.filter(elem => elem.children.length > 2);
```

- **Mathematics and Utilities**:
  - Numeric Functionality: Elevate the capabilities of `Number` instances by integrating `Math` methods directly into numbers. Perform mathematical operations seamlessly. This cohesive integration simplifies numerical computations and enhances code readability. Enjoy the fluidity of expressions like `(2).pow(3)` or `(4).sqrt()`.

```javascript
// Numeric Functionality
const n = -4.321;
n.trunc().abs().pow(2); // return 16
```

## Browser Compatibility

Otorp.js is compatible with modern browsers, including Chrome, Firefox, Safari, and Edge. It leverages native JavaScript features, so no additional dependencies are required.

## Contributing

We welcome contributions from the community! If you find any issues or have suggestions for improvements, feel free to create a pull request or submit an issue on our GitLab repository.

## License

Otorp.js is released under the [MIT License](https://opensource.org/licenses/MIT). You are free to use, modify, and distribute the library as per the terms of this license.

---

With a strong foundation of reusing native code and an emphasis on aliases and extended methods, Otorp.js empowers you to streamline your web development workflow. Start harnessing the power of Otorp.js to create cleaner, more efficient code today!
