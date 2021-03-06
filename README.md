# full-stack
Notes for full stack course in codecademy

## HTML 
**Introduction to HTML** -
So what exactly is HTML? HTML provides structure to the content appearing on a website, such as images, text, or videos. Right-click on any page on the internet, choose “Inspect,” and you’ll see HTML in a panel of your screen.

HTML stands for HyperText Markup Language:
- A markup language is a computer language that defines the structure and presentation of raw text.
- In HTML, the computer can interpret raw text that is wrapped in HTML elements.
- HyperText is text displayed on a computer or device that provides access to other text through links, also known as hyperlinks.

**HTML Anatomy** -
HTML is composed of elements. These elements structure the webpage and define its content. Let’s take a look at how they’re written.

The diagram to the right displays an HTML paragraph element. As we can see, the paragraph element is made up of:

- An opening tag (`<p>`)
- The content (“Hello World!” text)
- A closing tag (`</p>`)

A tag and the content between it is called an HTML element. There are many tags that we can use to organize and display text and other types of content, like images.

Let’s quickly review each part of the element pictured:

HTML element (or simply, element) — a unit of content in an HTML document formed by HTML tags and the text or media it contains.

HTML Tag — the element name, surrounded by an opening (<) and closing (>) angle bracket.

Opening Tag — the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.

Content — The information (text or other elements) contained between the opening and closing tags of an HTML element.

Closing tag — the second HTML tag used to end an HTML element. Closing tags have a forward slash (/) inside of them, directly after the left angle bracket.

**The Body** -
One of the key HTML elements we use to build a webpage is the body element. Only content inside the opening and closing body tags can be displayed to the screen. Here’s what opening and closing body tags look like:

```
<body>
 
</body>
```
Once the file has a body, many different types of content – including text, images, and buttons – can be added to the 
body.
```
<body>
  <p>What's up, doc?</p>
</body>
```
**HTML Structure** -
HTML is organized as a collection of family tree relationships. As you saw in the last exercise, we placed `<p>` tags within <body> tags. When an element is contained inside another element, it is considered the child of that element. The child element is said to be nested inside of the parent element.
  
```
 <body>
  <p>This paragraph is a child of the body</p>
</body>
```
  
In the example above, the `<p>` element is nested inside the <body> element. The `<p>` element is considered a child of the `<body> `element, and the <body> element is considered the parent. You can also see that we’ve added two spaces of indentation (using the space bar) for better readability.

Since there can be multiple levels of nesting, this analogy can be extended to grandchildren, great-grandchildren, and beyond. The relationship between elements and their ancestor and descendent elements is known as hierarchy.

Let’s consider a more complicated example that uses some new tags:

```
<body>
  <div>
    <h1>Sibling to p, but also grandchild of body</h1>
    <p>Sibling to h1, but also grandchild of body</p>
  </div>
</body>
```
  
In this example, the <body> element is the parent of the <div> element. Both the `<h1>` and `<p>` elements are children of the `<div>` element. Because the `<h1>` and `<p>` elements are at the same level, they are considered siblings and are both grandchildren of the <body> element.

Understanding HTML hierarchy is important because child elements can inherit behavior and styling from their parent element. You’ll learn more about webpage hierarchy when you start digging into CSS.

**Attributes** -
If we want to expand an element’s tag, we can do so using an attribute. Attributes are content added to the opening tag of an element and can be used in several different ways, from providing information to changing styling. Attributes are made up of the following two parts:

- The name of the attribute
- The value of the attribute
One commonly used attribute is the id. We can use the id attribute to specify different content (such as `<div>`s) and is really helpful when you use an element more than once. ids have several different purposes in HTML, but for now, we’ll focus on how they can help us identify content on our page.

When we add an id to a `<div>`, we place it in the opening tag:

```
  <div id="intro">
  <h1>Introduction</h1>
</div>
  ```
**Displaying Text** -
If you want to display text in HTML, you can use a paragraph or span:

Paragraphs (`<p>`) contain a block of plain text.
`<span>` contains short pieces of text or other HTML. They are used to separate small pieces of content that are on the same line as other content.
Take a look at each of these elements in action below:

```
<div>
  <h1>Technology</h1>
</div>
<div>
  <p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
</div>
```

 In the example above, there are two different `<div>`. The second `<div>` contains a `<p>` with <`span>`Self-driving cars`</span>`. This `<span>` element separates “Self-driving cars” from the rest of the text in the paragraph.

It’s best to use a `<span>` element when you want to target a specific piece of content that is inline, or on the same line as other text. If you want to divide your content into blocks, it’s better to use a `<div>`.
 
## CSS
### **FLEXBOX**
**What is Flexbox?**

CSS provides many tools and properties that you can use to position elements on a webpage. Codecademy’s lessons on the box model and CSS display introduce a couple of these techniques.

In this lesson, you will learn about Flexible Box Layout or flexbox, a tool that greatly simplifies how to position elements.

There are two important components to a flexbox layout: flex containers and flex items. A flex container is an element on a page that contains flex items. All direct child elements of a flex container are flex items. This distinction is important because some of the properties you will learn in this lesson apply to flex containers while others apply to flex items.

To designate an element as a flex container, set the element’s display property to flex or inline-flex. Once an item is a flex container, there are several properties we can use to specify how its children behave. In this lesson we will cover these properties:

- justify-content
- align-items
- flex-grow
- flex-shrink
- flex-basis
- flex
- flex-wrap
- align-content
- flex-direction
- flex-flow

**display: flex**
Any element can be a flex container. Flex containers are helpful tools for creating websites that respond to changes in screen sizes. Child elements of flex containers will change size and location in response to the size and position of their parent container.

For an element to become a flex container, its display property must be set to flex.
```
div.container {
  display: flex;
}
```
 
In the example above, all divs with the class container are flex containers. If they have children, the children are flex items. A div with the declaration display: flex; will remain block level — no other elements will appear on the same line as it.

However, it will change the behavior of its child elements. Child elements will not begin on new lines. In the exercises that follow, we will cover how the flex display property impacts the positioning of child elements.
 
**inline-flex**
In the previous exercise, you might have observed that when we gave a div — a block level element — the display value of flex that it remained a block level element. What if we want multiple flex containers to display inline with each other?

If we didn’t want div elements to be block-level elements, we would use display: inline. Flexbox, however, provides the inline-flex value for the display property, which allows us to create flex containers that are also inline elements.
```
<div class='container'>
  <p>I’m inside of a flex container!</p>
  <p>A flex container’s children are flex items!</p>
</div>
<div class='container'>
  <p>I’m also a flex item!</p>
  <p>Me too!</p>
</div>
.container {
  width: 200px;
  height: 200px;
  display: inline-flex;
}
 ```
In the example above, there are two container divs. Without a width, each div would stretch the entire width of the page. The paragraphs within each div would also display on top of each other because paragraphs are block-level elements.

When we change the value of the display property to inline-flex, the divs will display inline with each other if the page is wide enough. As we progress through this lesson, we will cover in more detail how flex items are displayed.

Notice that in the example above, the size of the flex container is set. Currently, the size of the parent container will override the size of its child elements. If the parent element is too small, the flex items will shrink to accommodate the parent container’s size. We’ll explain why in a later exercise.

 ```
<div class='container'>
  <div class='child'>
    <h1>1</h1>
  </div>
  <div class='child'>
    <h1>2</h1>
  </div>
</div>
.container {
  width: 200px;
}
 
.child {
  display: inline-flex;
  width: 150px;
  height: auto;
}
```
In the example above, the .child divs will take up more width (300 pixels) than the container div allows (200 pixels). The .child divs will shrink to accommodate the container’s size. In later exercises, we will explore several ways to handle this.

**justify-content** -
In previous exercises, when we changed the display value of parent containers to flex or inline-flex, all of the child elements (flex items) moved toward the upper left corner of the parent container. This is the default behavior of flex containers and their children. We can specify how flex items spread out from left to right, along the main axis. We will learn more about axes in a later exercise.

To position the items from left to right, we use a property called justify-content.
```
.container {
  display: flex;
  justify-content: flex-end;
}
```
In the example above, we set the value of justify-content to flex-end. This will cause all of the flex items to shift to the right side of the flex container.

Below are five commonly used values for the justify-content property:

- flex-start — all items will be positioned in order, starting from the left of the parent container, with no extra space between or before them.
- flex-end — all items will be positioned in order, with the last item starting on the right side of the parent container, with no extra space between or after them.
- center — all items will be positioned in order, in the center of the parent container with no extra space before, between, or after them.
- space-around — items will be positioned with equal space before and after each item, resulting in double the space between elements.
- space-between — items will be positioned with equal space between them, but no extra space before the first or after the last elements.
In the definitions above, “no extra space” means that margins and borders will be respected, but no more space (than is specified in the style rule for the particular element) will be added between elements. The size of each individual flex item is not changed by this property.
 
**align-items** -
In the previous exercise, you learned how to justify the content of a flex container from left to right across the page. It is also possible to align flex items vertically within the container. The align-items property makes it possible to space flex items vertically.
```
.container {
  align-items: baseline;
}
```
In the example above, the align-items property is set to baseline. This means that the baseline of the content of each item will be aligned.

Below are five commonly used values for the align-items property:

- flex-start — all elements will be positioned at the top of the parent container.
- flex-end — all elements will be positioned at the bottom of the parent container.
- center — the center of all elements will be positioned halfway between the top and bottom of the parent container.
- baseline — the bottom of the content of all items will be aligned with each other.
- stretch — if possible, the items will stretch from top to bottom of the container (this is the default value; elements with a specified height will not stretch; elements with a minimum height or no height specified will stretch).

 These five values tell the elements how to behave along the cross axis of the parent container. In these examples, the cross axis stretches from top to bottom of the container. We’ll learn more about this in a future exercise.

You might be unfamiliar with the min-height and max-height properties, but you have used height and width before. min-height, max-height, min-width, and max-width are properties that ensure an element is at least a certain size or at most a certain size. You’ll see how these become useful as you move throughout this lesson.
 
**flex-grow** -
In Exercise 3, we learned that all flex items shrink proportionally when the flex container is too small. However, if the parent container is larger than necessary then the flex items will not stretch by default. The flex-grow property allows us to specify if items should grow to fill a container and also which items should grow proportionally more or less than others.

 ```
<div class='container'>
  <div class='side'>
    <h1>I’m on the side of the flex container!</h1>
  </div>
  <div class='center'>
    <h1>I'm in the center of the flex container!</h1>
  </div>
  <div class='side'>
    <h1>I'm on the other side of the flex container!</h1>
  </div>
</div>
```
```
.container {
  display: flex;
}
 
.side {
  width: 100px;
  flex-grow: 1;
}
 
.center {
  width: 100px;
  flex-grow: 2;
}
```
 
In the example above, the .container div has a display value of flex, so its three child divs will be positioned next to each other. If there is additional space in the .container div (in this case, if it is wider than 300 pixels), the flex items will grow to fill it. The .center div will stretch twice as much as the .side divs. For example, if there were 60 additional pixels of space, the center div would absorb 30 pixels and the side divs would absorb 15 pixels each.

If a max-width is set for an element, it will not grow larger than that even if there is more space for it to absorb.

All of the previous properties we have learned are declared on flex containers, or the parent elements. This property — flex-grow — is the first we have learned that is declared on flex items.
 
**flex-shrink** -
Just as the flex-grow property proportionally stretches flex items, the flex-shrink property can be used to specify which elements will shrink and in what proportions.

You may have noticed in earlier exercises that flex items shrank when the flex container was too small, even though we had not declared the property. This is because the default value of flex-shrink is 1. However, flex items do not grow unless the flex-grow property is declared because the default value of flex-grow is 0.

 ```
<div class='container'>
  <div class='side'>
    <h1>I'm on the side of the flex container!</h1>
  </div>
  <div class='center'>
    <h1>I'm in the center of the flex container!</h1>
  </div>
  <div class='side'>
    <h1>I'm on the other side of the flex container!</h1>
  </div>
</div>
```
```
.container {
  display: flex;
}
 
.side {
  width: 100px;
  flex-shrink: 1;
}
 
.center {
  width: 100px;
  flex-shrink: 2;
}
```
 
In the example above, the .center div will shrink twice as much as the .side divs if the .container div is too small to fit the elements within it. If the content is 60 pixels too large for the flex container that surrounds it, the .center div will shrink by 30 pixels and the outer divs will shrink by 15 pixels each. Margins are unaffected by flex-grow and flex-shrink.

Keep in mind, minimum and maximum widths will take precedence over flex-grow and flex-shrink. As with flex-grow, flex-shrink will only be employed if the parent container is too small or the browser is adjusted.

**flex-basis** - 
In the previous two exercises, the dimensions of the divs were determined by heights and widths set with CSS. Another way of specifying the width of a flex item is with the flex-basis property. flex-basis allows us to specify the width of an item before it stretches or shrinks.

 ```
<div class='container'>
  <div class='side'>
    <h1>Left side!</h1>
  </div>
  <div class='center'>
    <h1>Center!</h1>
  </div>
  <div class='side'>
    <h1>Right side!</h1>
  </div>
</div>
```
```
.container {
  display: flex;
}
 
.side {
  flex-grow: 1;
  flex-basis: 100px;
}
 
.center {
  flex-grow: 2;
  flex-basis: 150px;
}
```
 
In the example above, the .side divs will be 100 pixels wide and the .center div will be 150 pixels wide if the .container div has just the right amount of space (350 pixels, plus a little extra for margins and borders). If the .container div is larger, the .center div will absorb twice as much space as the .side divs.

The same would hold true if we assigned flex-shrink values to the divs above as well.

**flex** -
The shorthand flex property provides a convenient way for specifying how elements stretch and shrink, while simplifying the CSS required. The flex property allows you to declare flex-grow, flex-shrink, and flex-basis all in one line.

Note: The flex property is different from the flex value used for the display property.

 ```
.big {
  flex-grow: 2;
  flex-shrink: 1;
  flex-basis: 150px;
}
 
.small {
  flex-grow: 1;
  flex-shrink: 2;
  flex-basis: 100px;
}
```
 
In the example above, all elements with class big will grow twice as much as elements with class small. Keep in mind, this doesn’t mean big items will be twice as big as small items, they’ll just take up more of the extra space.

The CSS below declares these three properties in one line.

```
.big {
  flex: 2 1 150px;
}
 
.small {
  flex: 1 2 100px;
}
```
 In the example above, we use the flex property to declare the values for flex-grow, flex-shrink, and flex-basis (in that order) all in one line.

```
.big {
 flex: 2 1;
}
```
In the example above, we use the flex property to declare flex-grow and flex-shrink, but not flex-basis.

```
.small {
  flex: 1 20px;
}
```
 
In the example above, we use the flex property to declare flex-grow and flex-basis. Note that there is no way to set only flex-shrink and flex-basis using 2 values.

The browser to the right has two flex containers, each with three flex items. In style.css, examine the values for each of these items. Notice that the flex-grow and flex-basis values are set for the blue divs.

Stretch the browser window to increase its width. Observe that once the top outer divs reach 100 pixels wide, they begin to grow faster than the top center div. Also notice that once the bottom center div reaches 100 pixels wide, it begins to grow faster than the outer divs.

Now, shrink the browser window and notice that once the top center div reaches 50 pixels wide it begins to shrink faster than the outer divs and when the bottom outer divs reach 75 pixels, they begin to shrink faster than the center div.

**flex-wrap** - 
Sometimes, we don’t want our content to shrink to fit its container. Instead, we might want flex items to move to the next line when necessary. This can be declared with the flex-wrap property. The flex-wrap property can accept three values:

- wrap — child elements of a flex container that don’t fit into a row will move down to the next line
- wrap-reverse — the same functionality as wrap, but the order of rows within a flex container is reversed (for example, in a 2-row flexbox, the first row from a wrap container will become the second in wrap-reverse and the second row from the wrap container will become the first in wrap-reverse)
- nowrap — prevents items from wrapping; this is the default value and is only necessary to override a wrap value set by a different CSS rule.

```
<div class='container'>
  <div class='item'>
    <h1>We're going to wrap!</h1>
  </div>
  <div class='item'>
    <h1>We're going to wrap!</h1>
  </div>
  <div class='item'>
    <h1>We're going to wrap!</h1>
  </div>
</div>
```
```
.container {
  display: inline-flex;
  flex-wrap: wrap;
  width: 250px;
}
 
.item {
  width: 100px;
  height: 100px;
}
```

In the example above, three flex items are contained by a parent flex container. The flex container is only 250 pixels wide so the three 100 pixel wide flex items cannot fit inline. The flex-wrap: wrap; setting causes the third, overflowing item to appear on a new line, below the other two items.

Note: The flex-wrap property is declared on flex containers.
**
align-content** -
Now that elements can wrap to the next line, we might have multiple rows of flex items within the same container. In a previous exercise, we used the align-items property to space flex items from the top to the bottom of a flex container. align-items is for aligning elements within a single row. If a flex container has multiple rows of content, we can use align-content to space the rows from top to bottom.

Below are some of the more commonly used align-content values:

- flex-start — all rows of elements will be positioned at the top of the parent container with no extra space between.
- flex-end — all rows of elements will be positioned at the bottom of the parent container with no extra space between.
- center — all rows of elements will be positioned at the center of the parent element with no extra space between.
- space-between — all rows of elements will be spaced evenly from the top to the bottom of the container with no space above the first or below the last.
- space-around — all rows of elements will be spaced evenly from the top to the bottom of the container with the same amount of space at the top and bottom and between each element.
- stretch — if a minimum height or no height is specified, the rows of elements will stretch to fill the parent container from top to bottom (default value).

```
 <div class='container'>
  <div class='child'>
    <h1>1</h1>
  </div>
  <div class='child'>
    <h1>2</h1>
  </div>
  <div class='child'>
    <h1>3</h1>
  </div>
  <div class='child'>
    <h1>4</h1>
  </div>
</div>
```
```
.container {
  display: flex;
  width: 400px;
  height: 400px;
  flex-wrap: wrap;
  align-content: space-around;
}
 
.child {
  width: 150px;
  height: 150px;
}
```

In the example above, there are four flex items inside of a flex container. The flex items are set to be 150 pixels wide each, but the parent container is only 400 pixels wide. This means that no more than two elements can be displayed inline. The other two elements will wrap to the next line and there will be two rows of divs inside of the flex container. The align-content property is set to the value of space-around, which means the two rows of divs will be evenly spaced from top to bottom of the parent container with equal space before the first row and after the second, with double space between the rows.

Below, we will see each of the properties in action!

Note: The align-content property is declared on flex containers.
 
**flex-direction** - 
Up to this point, we’ve only covered flex items that stretch and shrink horizontally and wrap vertically. As previously stated, flex containers have two axes: a main axis and a cross axis. By default, the main axis is horizontal and the cross axis is vertical.

The main axis is used to position flex items with the following properties:

- justify-content
- flex-wrap
- flex-grow
- flex-shrink
The cross axis is used to position flex items with the following properties:

- align-items
- align-content
The main axis and cross axis are interchangeable. We can switch them using the flex-direction property. If we add the flex-direction property and give it a value of column, the flex items will be ordered vertically, not horizontally.

```
<div class='container'>
  <div class='item'>
    <h1>1</h1>
  </div>
  <div class='item'>
    <h1>2</h1>
  </div>
  <div class='item'>
    <h1>3</h1>
  </div>
  <div class='item'>
    <h1>4</h1>
  </div>
  <div class="item">
    <h1>5</h1>
  </div>
</div>
```
```
.container {
  display: flex;
  flex-direction: column;
  width: 1000px;
}
.item {
  height: 100px;
  width: 100px;
}
```

In the example above, the five divs will be positioned in a vertical column. All of these divs could fit in one horizontal row. However, the column value tells the browser to stack the divs one on top of the other. As explained above, properties like justify-content will not behave the way they did in previous examples.

The flex-direction property can accept four values:

- row — elements will be positioned from left to right across the parent element starting from the top left corner (default).
- row-reverse — elements will be positioned from right to left across the parent element starting from the top right corner.
- column — elements will be positioned from top to bottom of the parent element starting from the top left corner.
- column-reverse — elements will be positioned from the bottom to the top of the parent element starting from the bottom left corner.
Below, we’ll investigate how these work.

Note: The flex-direction property is declared on flex containers.

**flex-flow** - 
Like the shorthand flex property, the shorthand flex-flow property is used to declare both the flex-wrap and flex-direction properties in one line.
```
.container {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
}
```

In the example above, we take two lines to accomplish what can be done with one.

```
.container {
  display: flex;
  flex-flow: column wrap;
}
```
 
In the example above, the first value in the flex-flow declaration is a flex-direction value and the second is a flex-wrap value. All values for flex-direction and flex-wrap are accepted.

Note: The flex-flow property is declared on flex containers.

**Nested Flexboxes** - 
So far, we’ve had multiple flex containers on the same page to explore flex item positioning. It is also possible to position flex containers inside of one another.

 ```
<div class='container'>
  <div class='left'>
    <img class='small' src='#'/>
    <img class='small' src='#'/>
    <img class='small' src='#' />
  </div>
  <div class='right'>
    <img class='large' src='#' />
  </div>
</div>
```
```
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
 
.left {
  display: inline-flex;
  flex: 2 1 200px;
  flex-direction: column;
}
 
.right {
  display: inline-flex;
  flex: 1 2 400px;
  align-items: center;
}
 
.small {
  height: 200px;
  width: auto;
}
 
.large {
  height: 600px; 
  width: auto;
}
```

In the example above, a div with three smaller images will display from top to bottom on the left of the page (.left). There is also a div with one large image that will display on the right side of the page (.right). The left div has a smaller flex-basis but stretches to fill more extra space; the right div has a larger flex-basis but stretches to fill less extra space. Both divs are flex items and flex containers. The items have properties that dictate how they will be positioned in the parent container and how their flex item children will be positioned in them.

We’ll use the same formatting above to layout the simple page to the right.

### **GRID**
**Creating a Grid** - 
 
To set up a grid, you need to have both a grid container and grid items. The grid container will be a parent element that contains grid items as children and applies overarching styling and positioning to them.

To turn an HTML element into a grid container, you must set the element’s display property to one of two values:

- grid — for a block-level grid.
- inline-grid — for an inline grid.

Then, you can assign other properties to lay out the grid to suit your needs.

**Creating Columns** -

By default, grids contain only one column. If you were to start adding items, each item would be put on a new row; that’s not much of a grid! To change this, we need to explicitly define the number of rows and columns in our grid.

We can define the columns of our grid by using the CSS property grid-template-columns. Below is an example of this property in action:
```
.grid {
  display: grid;
  width: 500px;
  grid-template-columns: 100px 200px;
}
```
 
This property creates two changes. First, it defines the number of columns in the grid; in this case, there are two. Second, it sets the width of each column. The first column will be 100 pixels wide and the second column will be 200 pixels wide.

We can also define the size of our columns as a percentage of the entire grid’s width.

```
.grid {
  display: grid;
  width: 1000px;
  grid-template-columns: 20% 50%;
}
```

In this example, the grid is 1000 pixels wide. Therefore, the first column will be 200 pixels wide because it is set to be 20% of the grid’s width. The second column will be 500 pixels wide.

We can also mix and match these two units. In the example below, there are three columns of width 20 pixels, 40 pixels, and 60 pixels:
```
.grid {
  display: grid;
  width: 100px;
  grid-template-columns: 20px 40% 60px;
}
```
 
Notice that in this example, the total width of our columns (120 pixels) exceeds the width of the grid (100 pixels). This might make our grid cover other elements on the page!

**Creating Rows** - 

We’ve learned how to define the number of columns in our grid explicitly. To specify the number and size of the rows, we are going to use the property grid-template-rows.

This property is almost identical to grid-template-columns. Take a look at the code below to see both properties in action.
```
.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template-columns: 100px 200px;
  grid-template-rows: 10% 20% 600px;
}
```
 
This grid has two columns and three rows. grid-template-rows defines the number of rows and sets each row’s height. In this example, the first row is 50 pixels tall (10% of 500), the second row is 100 pixels tall (20% of 500), and the third row is 600 pixels tall.

When using percentages in these two properties, remember that rows are defined as a percentage of the grid’s height, and columns are defined as a percentage of its width.

**Grid Template** - 

The shorthand property, grid-template, can replace the previous two CSS properties. Both grid-template-rows and grid-template-columns are nowhere to be found in the following code!
```
.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template: 200px 300px / 20% 10% 70%;
}
```
 
When using grid-template, the values before the slash will determine the size of each row. The values after the slash determine the size of each column. In this example, we’ve made two rows and three columns of varying sizes.

The same rules from before apply; when using percentages to set rows, each row will be a percentage of the grid’s total height. Columns are still a percentage of the total width.

**Fraction** - 

You may already be familiar with several types of responsive units such as percentages (%), ems and rems. CSS Grid introduced a new relative sizing unit — fr, like fraction.

By using the fr unit, we can define the size of columns and rows as a fraction of the grid’s length and width. This unit was specifically created for use in CSS Grid. Using fr makes it easier to prevent grid items from overflowing the boundaries of the grid. Consider the code below:
```
.grid {
  display: grid;
  width: 1000px;
  height: 400px;
  grid-template: 2fr 1fr 1fr / 1fr 3fr 1fr;
}
```

In this example, the grid will have three rows and three columns. The rows are splitting up the available 400 pixels of height into four parts. The first row gets two of those parts, the second row gets one, and the third row gets one. Therefore the first row is 200 pixels tall, and the second and third rows are 100 pixels tall.

Each column’s width is a fraction of the available space. In this case, the available space is split into five parts. The first column gets one-fifth of the space, the second column gets three-fifths, and the last column gets one-fifth. Since the total width is 1000 pixels, this means that the columns will have widths of 200 pixels, 600 pixels, and 200 pixels respectively.

It is possible to use fr with other units as well. When this happens, each fr represents a fraction of the available space.
```
.grid {
  display: grid;
  width: 100px;
  grid-template-columns: 1fr 60px 1fr;
}
```

In this example, 60 pixels are taken up by the second column. Therefore the first and third columns have 40 available to split between them. Since each gets one fraction of the total, they both end up being 20 pixels wide.

**Repeat** - 

The properties that define the number of rows and columns in a grid can take a function as a value. repeat() is one of these functions. The repeat() function was created specifically for CSS Grid.
```
.grid {
  display: grid;
  width: 300px;
  grid-template-columns: repeat(3, 100px);
}
```

The repeat function will duplicate the specifications for rows or columns a given number of times. In the example above, using the repeat function will make the grid have three columns that are each 100 pixels wide. It is the same as writing:
```
grid-template-columns: 100px 100px 100px;
```

Repeat is particularly useful with fr. For example, repeat(5, 1fr) would split your table into five equal rows or columns.

Finally, the second parameter of repeat() can have multiple values.
```
grid-template-columns: repeat(2, 20px 50px)
```

This code will create four columns where the first and third columns will be 20 pixels wide and the second and fourth will be 50 pixels wide.

**minmax** - 

So far, all of the grids that we have worked with have been a fixed size. The grid in our example has been 400 pixels wide and 500 pixels tall. But sometimes you might want a grid to resize based on the size of your web browser.

In these situations, you might want to prevent a row or column from getting too big or too small. For example, if you have a 100-pixel wide image in your grid, you probably don’t want its column to get thinner than 100 pixels! The minmax() function can help us solve this problem.
```
.grid {
  display: grid;
  grid-template-columns: 100px minmax(100px, 500px) 100px;
}
```

In this example, the first and third columns will always be 100 pixels wide, no matter the size of the grid. The second column, however, will vary in size as the overall grid resizes. The second column will always be between 100 and 500 pixels wide.

**Grid Gap** - 

In all of our grids so far, there hasn’t been any space between the items in our grid. The CSS properties row-gap and column-gap will put blank space between every row and column in the grid.
```
.grid {
  display: grid;
  width: 320px;
  grid-template-columns: repeat(3, 1fr);
  column-gap: 10px;
}
```

It is important to note that grid gap properties does not add space at the beginning or end of the grid. In the example code, our grid will have three columns with two ten-pixel gaps between them.

Let’s quickly calculate how wide these columns are. Remember that using fr considers all of the available space. The grid is 320 pixels wide and 20 of those pixels are taken up by the two grid gaps. Therefore each column takes a piece of the 300 available pixels. Each column gets 1fr, so the columns are evenly divided into thirds (or 100 pixels each).

Finally, there is a shorthand CSS property, gap, that can set the row and column gap at the same time.
```
.grid {
  display: grid;
  width: 320px;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px 10px;
}
```

The example above will set the distance between rows to 20 pixels and the distance between columns to 10 pixels. Unlike other CSS grid properties, this shorthand does not take a / between values! If only one value is given, it will set the column gap and the row gap to that value.

**Multiple Row Items** - 

Using the CSS properties grid-row-start and grid-row-end, we can make single grid items take up multiple rows. Remember, we are no longer applying CSS to the outer grid container; we’re adding CSS to the elements sitting inside the grid!
```
.item {
  grid-row-start: 1;
  grid-row-end: 3;
}
```

In this example, the HTML element of class item will take up two rows in the grid, rows 1 and 2. The values that grid-row-start and grid-row-end accept are grid lines.

Row grid lines and column grid lines start at 1 and end at a value that is 1 greater than the number of rows or columns the grid has. For example, if a grid has 5 rows, the grid row lines range from 1 to 6. If a grid has 8 rows, the grid row lines range from 1 to 9.

The value for grid-row-start should be the row at which you want the grid item to begin. The value for grid-row-end should be one greater than the row at which you want the grid item to end. An element that covers rows 2, 3, and 4 should have these declarations: grid-row-start: 2 and grid-row-end: 5.

It is possible for the value of grid-row-start to be greater than that of grid-row-end. Both properties can also each have negative values. Consult the documentation to learn more about how to use these features.

**Grid Row** - 

We can use the property grid-row as shorthand for grid-row-start and grid-row-end. The following two code blocks will produce the same output:
```
.item {
  grid-row-start: 4;
  grid-row-end: 6;
}
.item {
  grid-row: 4 / 6;
}
```

This code should look similar to the way grid-template is shorthand for grid-template-rowsand grid-template-columns. In this case, the starting row goes before the “/“ and the ending row goes after it. Again, the ending row is exclusive; this grid item will occupy rows four and five.

When an item spans multiple rows or columns using these properties, it will also include the gap if any exists. For example, if an item spans two rows of height 100 pixels and there is a ten-pixel gap, then the item will have a total height of 210 pixels.
 
**Grid Column** - 

The previous three properties also exist for columns. grid-column-start, grid-column-end and grid-column work identically to the row properties. These properties allow a grid item to span multiple columns.

When using these properties, we can use the keyword span to start or end a column or row, relative to its other end. Look at how span is used in the code below:
```
.item {
  grid-column: 4 / span 2;
}
```

This is telling the item element to begin in column four and take up two columns of space. So item would occupy columns four and five. It produces the same result as the following code blocks:

```
.item {
  grid-column: 4 / 6;
}
.item {
  grid-column-start: 4;
  grid-column-end: span 2;
}
.item {
  grid-column-start: span 2;
  grid-column-end: 6;
}
```

span is a useful keyword, because it avoids off-by-one errors (miscalculating the ending grid line) you might make when determining the ending grid line of an element. If you know where you want your grid item to start and how long it should be, use span

**Grid Area** - 

We’ve already been able to use grid-row and grid-column as shorthand for properties like grid-row-start and grid-row-end. We can refactor even more using the property grid-area. This property will set the starting and ending positions for both the rows and columns of an item.
```
.item {
  grid-area: 2 / 3 / 4 / span 5;
}
```

grid-area takes four values separated by slashes. The order is important! This is how grid-area will interpret those values.

- grid-row-start
- grid-column-start
- grid-row-end
- grid-column-end

In the above example, the item will occupy rows two and three and columns three through eight.
Using grid-area is an easy way to place items exactly where you want them in a grid.
