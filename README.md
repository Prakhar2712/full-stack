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
