<div align="center">
  <h1> SASS For Beginners: Intro </h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/juadebade/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Juadeb1">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/Juadeb1?style=social">
  </a>

<sub>Author:
<a href="https://www.linkedin.com/in/juadebade/" target="_blank">Juadeb Gabriel</a><br>
<small> October, 2020</small>
</sub>

</div>

- [History of SASS](#history-of-sass)
- [What exactly is SASS](#what-exactly-is-sass)
- [Difference between SASS \& SCSS](#difference-between-sass--scss)
- [Indented syntax](#indented-syntax)
- [SCSS syntax](#scss-syntax)
- [Nesting in Sass](#nesting-in-sass)
- [How Does Sass Work?](#how-does-sass-work)
- [Why should you use Sass?](#why-should-you-use-sass)
- [Features of Sass](#features-of-sass)
  - [Variables in Sass](#variables-in-sass)
- [Extend (@extend)](#extend-extend)
- [Partials and modules](#partials-and-modules)
- [Parent Selector](#parent-selector)
- [Partials in Sass](#partials-in-sass)
- [Mixins in Sass](#mixins-in-sass)
- [Sass Functions and Operators](#sass-functions-and-operators)
- [How to Set Up Sass for VS Code](#how-to-set-up-sass-for-vs-code)
  - [Step 1: Install Live Sass Compiler](#step-1-install-live-sass-compiler)
  - [Step 2: Set the Save Location](#step-2-set-the-save-location)
  - [Step 3: Compile Sass](#step-3-compile-sass)
  - [Step 4: Link the CSS file](#step-4-link-the-css-file)

## History of SASS

There have been several different versions of Sass available over the years. Sass was first created in 2006 using Ruby. However, this version of Sass was deprecated and reached end-of-life in 2019. You shouldn’t use this version of Sass anymore. The main version of Sass currently is called Dart Sass. As the name implies, this version was created using Dart. Version 1.0.0 of Dart Sass was released in March 2018. Dart Sass is the version you’ll likely want to use when starting a new project. There was also another version of Sass called LibSass, which was deprecated in 2020.

## What exactly is SASS

Sass `(Syntactically Awesome Style Sheets)` is a CSS preprocessor that gives your CSS superpowers. Let's face it: writing CSS can be difficult at times, especially in today's world of increasingly complex user interfaces. And many times, you'll find that you're repeating yourself often. Sass comes to the rescue in this situation. It helps you stick to the DRY `(Do Not Repeat Yourself)` philosophy when writing CSS. Sass provides a compiler that allows us to write stylesheets in two different syntaxes, indented and SCSS.
Let's look at each now :

## Difference between SASS & SCSS

Sass uses a different syntax that is indentation-based, similar to Python or Haml. It does not use semicolons or curly braces. Instead, it relies on indentation to indicate nesting and separate properties and values. Here's an example of Sass syntax: _Sass (Syntactically Awesome Style Sheets)_ and _SCSS (Sassy CSS)_ are both popular CSS preprocessors that extend the capabilities of standard CSS. While they are similar in many ways, there is one key difference in their syntax.

## Indented syntax

This is the older syntax that is indented, and gets rid of the curly braces and semi-colons. It has a file extension of _.sass_

```sass
nav
  ul
    margin: 0
    padding: 0
    list-style: none

  li
    display: inline-block

  a
    display: block
    text-decoration: none
```

## SCSS syntax

This is the newer and more popular syntax. It is essentially a subset of the CSS3 syntax. This means that you can write regular CSS with some additional functionalities. Due to its advanced features it is often termed as Sassy CSS. It has a file extension of _.scss_

```scss
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }

  a {
    display: block;
    text-decoration: none;
  }
}
```

## Nesting in Sass

Most of the time, while writing CSS, classes are often duplicated. We can avoid this duplication by nesting styles inside the parent element.

In CSS,

```css
nav {
  height: 10vh;
  width: 100%;
  display: flex;
}

nav ul {
  list-style: none;
  display: flex;
}

nav li {
  margin-right: 2.5rem;
}

nav li a {
  text-decoration: none;
  color: #707070;
}

nav li a:hover {
  color: #069c54;
}
```

With SCSS, the above code can be written like this:

```scss
nav {
  height: 10vh;
  width: 100%;
  display: flex;

  ul {
    list-style: none;
    display: flex;
  }

  li {
    margin-right: 2.5rem;

    a {
      text-decoration: none;
      color: #707070;

      &:hover {
        color: #069c54;
      }
    }
  }
}
```

**Quick Disclaimer: This article uses the SCSS syntax because it's more widely used.**

## How Does Sass Work?

Sass works in such a way that when you write your styles in a .scss file, it gets compiled into a regular CSS file. The CSS code is then loaded into the browser. That is why it's called a `Preprocessor`.

## Why should you use Sass?

- Easy to learn: If you are familiar with CSS already, then you'll be glad to know that Sass actually has a similar syntax, and so you can start using it, even after this tutorial ;
- Compatibility: It is compatible with all versions of CSS. So, you can use any available CSS libraries.
- Saves time: It helps reduce the repetition of CSS, because of its powerful features.
- Reusable code: Sass allows for variables and chunks of code (mixins) that can be reused over and over again. This helps you save time and makes you able to code faster.
- Organized Code: Sass helps keep your code organized by using partials.
- Cross Browser Compatibility: Sass gets compiled into CSS and adds all the necessary vendor prefixes so you don't have to worry about manually writing them out.

## Features of Sass

Here are some of the features that make Sass truly CSS with Superpowers:

### Variables in Sass

Sass variables allow you to reuse the same value in multiple spots in your style sheet. This is accomplished by storing a value in a variable name and then referencing that variable name throughout your style sheet (see the code above for an example). You can store any CSS value: a color, a font, a width, etc.

Variables in Sass start with a dollar sign and don’t have to be wrapped in curly brackets. This is one of Sass's strengths since we can define variables for various properties and use them in any file. The benefit here is that if that value changes, you simply need to update a single line of code. This is done by naming a variable with a dollar symbol $ and then referencing it elsewhere in your code.

```scss
$variable-name: value;
```

Using variables also means it’s easy to update multiple CSS rules at once. In the example above, I can change the $main-color variable to blue, which will automatically update the color property of the h1 tag and the background-color property of the p tag in the compiled CSS. This is easier than having to manually update each CSS rule where the color appears.

```scss
// Sass variable storing fonts
$font-stack: Helvetica, sans-serif;

// Sass variable storing a width value
// Note: Variable names can be one word
$width: 100px;

body {
  font: 100% $font-stack;
}

.rectangle {
  width: $width;
}
```

```scss
$primary-color: #24a0ed;

.text {
  color: $primary-color;
}
button {
  color: $primary-color;
  border: 2px solid $primary-color;
}
```

```scss
nav {
  height: 10vh;
  width: 100%;
  display: flex;

  ul {
    list-style: none;
    display: flex;
  }

  li {
    margin-right: 2.5rem;

    a {
      text-decoration: none;
      color: #707070;

      &:hover {
        color: #069c54;
      }
    }
  }
}
```

## Extend (@extend)

The _@extend_ rule in Sass allows you to group several CSS declarations together and reuse them in multiple rules. The _@extend_ feature uses the following format:

```scss
%custom-colors {
  background-color: green;
  color: yellow;
}

h1 {
  @extend %custom-colors;
}

p {
  @extend %custom-colors;
}

//compiled to
p,
h1 {
  background-color: green;
  color: yellow;
}
```

The @extend rule in Sass allows you to group several CSS declarations together and reuse them in multiple rules. The @extend feature uses the following format:

```scss
%extend-selector-name {
  property 1: value 1;
  property 2: value 2;
  // property 3...
}

.rule-1 {
  @extend %extend-selector-name;
}

.rule-2 {
  @extend %extend-selector-name;
}
```

The type of selector at the top of the code snippet is called a placeholder selector and starts with a %. This selector won’t appear on its own in the CSS output, but its declarations will appear wherever it’s extended. It is also possible to extend an existing CSS rule:

```scss
.my-class {
  background-color: green;
  color: yellow;
}

.my-class-alternate {
  @extend .my-class;
  border: 1px black;
}
```

## Partials and modules

You can create a partial Sass file by adding an underscore to the beginning of the filename, like this: _colors.scss. To load a partial into another Sass file, use the following syntax at the top of your file:

```scss
@use 'colors';
```

You can split up your Sass code into multiple files and still have one CSS file in the end using partials and imports. You can create a partial Sass file by adding an underscore to the beginning of the filename. An example name could be _colors.scss._. The partial file will not be compiled into its own CSS file. Instead, to use the code you import it into a normal Sass file that will be compiled. To import a partial into another Sass file, you can use the following syntax at the top of your file:

```scss
@use 'colors';
```

Notice that you don’t need to include the underscore or the .scss file extension. The @use rule applies Dart Sass 1.23.0 and above. Older versions of Dart Sass used the @import rule, but that is now deprecated.

## Parent Selector

In the Sass code above, you might notice the ampersand symbol _&_ used with the hover pseudo-class. This is called a Parent Selector.

**The parent selector, &, is a special selector invented by Sass that's used in nested selectors to refer to the outer selector. Source [Sass Documentation](https://sass-lang.com/documentation/style-rules/parent-selector/)**

So, in the case of the code above, _&_ will refer to the parent which is the anchor tag _a_.

## Partials in Sass

This is one of the many awesome features of Sass that gives you an advantage. As stylesheets grow large over time, it gets difficult to maintain them. Because of this, it just makes sense to break your stylesheets into smaller chunks. In other words, Partials help you organize and structure your code. To declare a partial, we will start the file name with an underscore, and add it in another Sass file using the @import directive. For example, if we have a _globals.scss_,_variables.scss_, and _buttons.scss_, we could import them into the main SCSS file main.scss.

```scss
@import "globals";
@import "variables";
@import "buttons";
```

You'll notice that the underscore and the .scss are not added. That is because Sass automatically assumes that you are referring to the .sass or .scss file.

## Mixins in Sass

Another major issue with CSS is that you'll often use a similar group of styles. Mixins allow you to encapsulate a group of styles, and apply those styles anywhere in your code using the _@include_ keyword.

An example of when you'd use mixins is when using Flexbox.

```scss
@mixin flex-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-direction: column;
  background: #ccc;
}

.card {
  @include flex-container;
}

.aside {
  @include flex-container;
}
```

## Sass Functions and Operators

Sass provides a suite of tools to help write more programmatic code. Sass offers built-in functions that enable us to do calculations and operations that return a specific value. They range from color calculations to math operations like getting random numbers and calculation of sizes, and even conditionals.

It also provides support for mathematical operators like +, -, \, \*, /, and %, which we can use with the calc function.

Here is an example using a pixel to rem conversion function:

```scss
@function pxToRem($pxValue) {
  $remValue: ($pxValue / 16) + rem;
  @return $remValue;
}

div {
  width: pxToRem(480);
}
```

However, it's important to note that the / operator for division is deprecated, and will be removed in Dart Sass 2.0.0. You can read about it in the Docs.

So, this is how it should be written:

```scss
@use "sass:math";

@function pxToRem($pxValue) {
  @return math.div($pxValue, 16px) * 1rem;
}

div {
  width: pxToRem(480px); // gives 30rem
}
```

Here is an example of conditional logic in a mixin:

```scss
@mixin body-theme($theme) {
  @if $theme == "light" {
    background-color: $light-bg;
  } @else {
    background-color: $dark-bg;
  }
}
```

Sass also provides the lighten and darken functions to adjust a color by a certain percentage.

For example:

```scss
$red: #ff0000;

a:visited {
  color: darken($red, 25%);
}
```

## How to Set Up Sass for VS Code

### Step 1: Install Live Sass Compiler

First, launch Visual Studio Code. Once it's loaded, go to the side panel on the left and select the extensions tab. In the search bar, search for `Live Sass Compiler` and install it. This extension helps us to compile the Sass files — _.scss (or .sass)_ – into _.css_ files.

**OR**

```node
npm install -g sass
```

### Step 2: Set the Save Location

Now change the file path so that Sass gets compiled into the styles folder. To do this, you will make changes to the settings.json file. In VS Code, go to _File > Preferences > Settings_ Now search for live sass compile to change the global settings.

Click on Edit _settings.json_.

[extension](./sass.png)

Now, on the first few lines, where you see this code:

```json
{
  "liveSassCompile.settings.formats": [
    {
      "format": "expanded",
      "extensionName": ".css",
      "savePath": "/"
    }
  ]
}
```

Change "savePath": "/" to "savePath": "/styles", so it now looks like this:

```scss
{
  "liveSassCompile.settings.formats":[
    {
      "format": "expanded",
      "extensionName":".css",
      "savePath":"/styles",
    },

    // You can also use this minified extension for production, as it reduces the file size

    {
      "format": "compressed",
      "extensionName":".min.css",
      "savePath":"/styles",
    }
  ],
}
```

### Step 3: Compile Sass

Now, after saving the settings, go back to the Sass file, and click on the button that says "Watch Sass" at the very bottom of the window.

[watch sass](./sass2.png)

After you click the button, two files get created: _.css_ and a _.css.map_ in the styles folder.

You should not, however, change any of them. Because it already helps you compile the Sass into CSS every time you save new stylings.

### Step 4: Link the CSS file

Then, link the CSS file in your index.html. In our case:

```html
<link rel="stylesheet" href="/styles/main.css" />
```

Now let's try a project.
