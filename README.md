Absolutely, I'd be happy to help you get started with CSS! Let's begin with the basics.

## Class 1: Introduction to CSS and Text Formatting

### Part 1: Introduction to CSS

**Definition:**
CSS stands for Cascading Style Sheets. It is a language used to describe the presentation of web pages, including their layout, colors, fonts, and more. CSS allows you to control the visual appearance of HTML elements on a webpage.

**Implementation:**
CSS can be applied to HTML elements using three different methods: Inline, Internal, and External.

1. **Inline CSS:**
   Inline CSS is applied directly to an HTML element using the `style` attribute. It's useful for making small, specific style changes.

   ```html
   <p style="color: blue;">This is a blue text.</p>
   ```

2. **Internal CSS:**
   Internal CSS is placed within the `<style>` element in the HTML document's `<head>`. It affects elements throughout the document.

   ```html
   <head>
     <style>
       p {
         color: red;
       }
     </style>
   </head>
   ```

3. **External CSS:**
   External CSS is stored in a separate `.css` file and linked to the HTML document using the `<link>` element. This method is best for maintaining consistent styles across multiple pages.

   ```html
   <head>
     <link rel="stylesheet" type="text/css" href="styles.css" />
   </head>
   ```

### Part 2: Tags vs IDs vs Classes

**Tags:**
HTML tags represent different elements on a webpage, like headings (`<h1>`, `<h2>`, ...), paragraphs (`<p>`), links (`<a>`), etc. You can target these tags in your CSS to apply styles.

**IDs:**
An ID is a unique identifier given to an HTML element using the `id` attribute. IDs are used to target specific elements for styling and JavaScript interactions.

**Classes:**
A class is a reusable identifier applied to one or more HTML elements using the `class` attribute. Classes allow you to apply the same styles to multiple elements.

**Implementation:**

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="styles.css" />
  </head>
  <body>
    <h1>This is a heading</h1>
    <p id="unique-paragraph">This is a unique paragraph with an ID.</p>
    <p class="common-paragraph">This is a common paragraph with a class.</p>
  </body>
</html>
```

### Part 3: CSS Text Formatting

1. **Color:**
   The `color` property is used to change the text color. Colors can be specified in various ways, such as color names, HEX codes, RGB values, etc.

   ```css
   p {
     color: blue;
   }
   ```

2. **Font Family:**
   The `font-family` property defines the typeface for text. You can specify multiple font families, and the browser will use the first available font.

   ```css
   body {
     font-family: Arial, sans-serif;
   }
   ```

3. **Font Style:**
   The `font-style` property is used to apply styles like italic or oblique to text.

   ```css
   em {
     font-style: italic;
   }
   ```

4. **Font Size:**
   The `font-size` property sets the size of the font. It can be specified in various units like pixels (`px`), ems (`em`), or percentages (`%`).

   ```css
   h1 {
     font-size: 24px;
   }
   ```

5. **Using Google Fonts:**
   Google Fonts provides a wide range of free, web-safe fonts that you can use in your projects. To use Google Fonts, you need to link to the font stylesheet in your HTML.

   ```html
   <head>
     <link
       rel="stylesheet"
       href="https://fonts.googleapis.com/css?family=Roboto"
     />
   </head>
   ```

   ```css
   body {
     font-family: "Roboto", sans-serif;
   }
   ```

**Notes:**

- CSS is used to style HTML elements.
- There are three ways to apply CSS: Inline, Internal, and External.
- Tags, IDs, and Classes are used to target specific elements for styling.
- You can format text using properties like color, font family, font style, and font size.
- Google Fonts provides a wide variety of fonts for web use.

**Homework:**

1. Try creating an HTML file and apply different CSS styles to paragraphs, headings, and links.
2. Experiment with different font styles and sizes.
3. Explore Google Fonts and apply a new font to your webpage.

In our next class, we will dive deeper into layout and positioning with CSS. Don't hesitate to ask if you have any questions!

Absolutely, let's delve into each individual component of the `background` property along with its possible values and examples.

## CSS `background` Property Components and Values

### 1. `background-attachment`

This property specifies whether the background image scrolls with the content or remains fixed.

**Possible Values:**

- `scroll`: The background image scrolls with the content.
- `fixed`: The background image remains fixed in place.
- `local`: The background image scrolls with the element's content, ignoring the parent element's scrolling.

**Example:**

```css
.element {
  background-image: url("image.jpg");
  background-attachment: fixed;
}
```

**Example for all:**

```html
<p class="border-box">The background extends behind the border.</p>
<p class="padding-box">
  The background extends to the inside edge of the border.
</p>
<p class="content-box">
  The background extends only to the edge of the content box.
</p>
<p class="text">The background is clipped to the foreground text.</p>
```

```css
p {
  border: 0.8em darkviolet;
  border-style: dashed;
  margin: 1em 0;
  padding: 1.4em;
  background: linear-gradient(60deg, red, yellow, red, yellow, red);
  font: 900 1.2em sans-serif;
  text-decoration: underline;
}

.border-box {
  background-clip: border-box;
}
.padding-box {
  background-clip: padding-box;
}
.content-box {
  background-clip: content-box;
}

.text {
  background-clip: text;
  -webkit-background-clip: text;
  color: rgba(0, 0, 0, 0.2);
}
```

### 2. `background-clip`

This property determines the portion of the background that should be visible based on the element's padding box, border box, or content box.

**Possible Values:**

- `border-box`: The background extends beneath the border.
- `padding-box`: The background extends beneath the padding.
- `content-box`: The background is confined to the content area.

**Example:**

```css
.element {
  background-color: #f2f2f2;
  background-clip: padding-box;
}
```

### 3. `background-color`

This property sets the background color of an element.

**Possible Values:**

- Any valid color value (e.g., color names, HEX codes, RGB values, etc.).

**Example:**

```css
.element {
  background-color: lightblue;
}
```

### 4. `background-image`

This property specifies one or more background images for the element.

**Possible Values:**

- `none`: No background image.
- URL to an image file.

**Example:**

```css
.element {
  background-image: url("pattern.png");
}
```

### 5. `background-origin`

This property defines the origin of the background positioning area.

**Possible Values:**

- `border-box`: Origin is the border box.
- `padding-box`: Origin is the padding box.
- `content-box`: Origin is the content box.

**Example:**

```css
.element {
  background-image: url("image.jpg");
  background-origin: padding-box;
}
```

### 6. `background-position`

This property sets the initial position of the background image(s).

**Possible Values:**

- Keywords: `top`, `bottom`, `left`, `right`, `center`
- Percentages: Relative to the element's size.
- Length values: In pixels, ems, rems, etc.

**Example:**

```css
.element {
  background-image: url("image.jpg");
  background-position: right bottom;
}
```

### 7. `background-repeat`

This property determines how the background image(s) should repeat or not repeat.

**Possible Values:**

- `repeat`: Repeat both horizontally and vertically.
- `repeat-x`: Repeat only horizontally.
- `repeat-y`: Repeat only vertically.
- `no-repeat`: Do not repeat.
- `space`: Repeat as much as possible without clipping, adding space between images.

**Example:**

```css
.element {
  background-image: url("pattern.png");
  background-repeat: no-repeat;
}
```

### 8. `background-size`

This property specifies the size of the background image(s).

**Possible Values:**

- `auto`: Default size of the image.
- `cover`: Resize the image to cover the entire element while maintaining aspect ratio.
- `contain`: Resize the image to fit inside the element while maintaining aspect ratio.
- Length values: In pixels, ems, rems, etc.

**Example:**

```css
.element {
  background-image: url("image.jpg");
  background-size: cover;
}
```

The `background-size` property in CSS is used to control the size of the background image within an element. Here's an explanation of the differences between `cover`, `contain`, and `100%`:

1. **`background-size: cover;`**

   When you set `background-size: cover;`, the background image is scaled to cover the entire content area of the element while maintaining its aspect ratio. This means that the image will be enlarged (if necessary) to completely cover the element, potentially cropping parts of the image if it doesn't fit exactly.
   Basically It maksure that the image will cover all the parts of the element, no gaps are there, but sometimes the image will cropout.

   Example:

   ```css
   .element {
     background-image: url("image.jpg");
     background-size: cover;
   }
   ```

2. **`background-size: contain;`**

   With `background-size: contain;`, the background image is scaled to fit within the element's content area while also maintaining its aspect ratio. This ensures that the entire image is visible, and it might leave empty space around the image if the aspect ratios don't match.

   Example:

   ```css
   .element {
     background-image: url("image.jpg");
     background-size: contain;
   }
   ```

3. **`background-size: 100%;`**

   Setting `background-size: 100%;` means that the background image will be scaled to completely cover the element's content area, regardless of its original aspect ratio. This can lead to the image being stretched or distorted if its proportions are not the same as the element's proportions.

   Example:

   ```css
   .element {
     background-image: url("image.jpg");
     background-size: 100%;
   }
   ```

In summary:

- `cover` ensures the image covers the entire element's content area, potentially cropping parts.
- `contain` scales the image to fit within the element's content area while showing the whole image.
- `100%` scales the image to cover the whole content area, without necessarily maintaining the image's aspect ratio.

Your choice of `background-size` value depends on the visual effect you want to achieve and how you want the background image to interact with the element's dimensions.

### FLEXBOX

Flexbox (Flexible Box Layout) is a powerful layout model in CSS that allows you to design complex layouts and distribute space and alignment of items within a container. It is particularly useful for creating responsive and flexible designs, where the arrangement of elements can adapt to different screen sizes and orientations.

Flexbox introduces a parent-child relationship between a flex container (the parent) and its flex items (the children). The main idea behind flexbox is to provide an efficient way to distribute space and control alignment along a single axis (the main axis) and, optionally, a perpendicular axis (the cross axis).

Here are the key properties of the Flexbox layout model, along with their definitions and implementation examples:

1. **`display: flex;`**

   This property is used to create a flex container. It enables the Flexbox layout for the specified container.

   **Implementation:**

   ```css
   .container {
     display: flex;
   }
   ```

2. **`flex-direction`**

   This property defines the direction of the main axis along which the flex items are laid out.

   **Values:**

   - `row`: Items are placed horizontally in a row (default).
   - `row-reverse`: Items are placed horizontally in a reverse order.
   - `column`: Items are placed vertically in a column.
   - `column-reverse`: Items are placed vertically in a reverse order.

   **Implementation:**

   ```css
   .container {
     display: flex;
     flex-direction: row;
   }
   ```

3. **`flex-wrap`**

   This property controls whether the flex items should wrap to multiple lines if they cannot fit in a single line.

   **Values:**

   - `nowrap`: Items are not wrapped (default).
   - `wrap`: Items wrap onto multiple lines.
   - `wrap-reverse`: Items wrap onto multiple lines in reverse order.

   **Implementation:**

   ```css
   .container {
     display: flex;
     flex-wrap: wrap;
   }
   ```

4. **`justify-content`**

   This property aligns flex items along the main axis.

   **Values:**

   - `flex-start`: Items are packed at the start of the container (default).
   - `flex-end`: Items are packed at the end of the container.
   - `center`: Items are centered along the main axis.
   - `space-between`: Items are evenly distributed with space between them.
   - `space-around`: Items are evenly distributed with space around them.

   **Implementation:**

   ```css
   .container {
     display: flex;
     justify-content: center;
   }
   ```

5. **`align-items`**

   This property aligns flex items along the cross axis (perpendicular to the main axis).

   **Values:**

   - `stretch`: Items are stretched to fill the container's cross-axis (default).
   - `flex-start`: Items are aligned at the start of the cross axis.
   - `flex-end`: Items are aligned at the end of the cross axis.
   - `center`: Items are centered along the cross axis.
   - `baseline`: Items are aligned based on their baseline.

   **Implementation:**

   ```css
   .container {
     display: flex;
     align-items: center;
   }
   ```

6. **`align-content`**

   This property aligns the entire flex container's contents along the cross axis when there's extra space in the container.

   **Values:**

   - `flex-start`: Contents are packed at the start of the cross axis (default).
   - `flex-end`: Contents are packed at the end of the cross axis.
   - `center`: Contents are centered along the cross axis.
   - `space-between`: Contents are evenly distributed with space between them.
   - `space-around`: Contents are evenly distributed with space around them.
   - `stretch`: Contents are stretched to fill the container's cross-axis.

   **Implementation:**

   ```css
   .container {
     display: flex;
     align-content: space-between;
   }
   ```

7. **`order`**

   This property specifies the order of a flex item within its flex container.

   **Values:**

   - Integer values (e.g., `0`, `1`, `2`, ...).

   **Implementation:**

   ```css
   .item {
     order: 2;
   }
   ```

8. **`flex-grow`**

   This property determines how flex items grow to occupy available space on the main axis.

   **Values:**

   - Numeric values (e.g., `0`, `1`, `2`, ...).

   **Implementation:**

   ```css
   .item {
     flex-grow: 1;
   }
   ```

   Example:

   ```css
   <!DOCTYPE html>
   <html lang="en">
   <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .container {
            display: flex;
            flex-wrap: wrap;
            height: 500px;
            border: 2px solid #333;
            align-content: space-between;
            /* align-content: space-between; */
        }

        .item {
            height: 100px;
            border: 1px solid #666;
            margin: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 16px;
        }


    </style>
    <title>align-content Example</title>
   </head>
   <body>
    <div class="container">
        <div class="item" style="flex-grow: 1;">Item 1</div>
        <div class="item" style="flex-grow: 1;">Item 2</div>
        <div class="item" style="flex-grow: 3;">Item 3</div>
        <div class="item" style="flex-grow: 1;">Item 4</div>
        <div class="item" style="flex-grow: 1;">Item 5</div>
        <div class="item" style="flex-grow: 1;">Item 6</div>
        <div class="item" style="flex-grow: 1;">Item 6</div>
        <div class="item" style="flex-grow: 1;">Item 6</div>
        <div class="item" style="flex-grow: 1;">Item 6</div>

    </div>
   </body>
   </html>
   ```

9. **`flex-shrink`**

   This property determines how flex items shrink if they don't have enough space on the main axis.

   **Values:**
   - Numeric values (e.g., `0`, `1`, `2`, ...).

   **Implementation:**
   ```css
   .item {
       flex-shrink: 0;
   }
    ```

10. **`flex-basis`**

    This property defines the initial size of a flex item on the main axis before it's distributed within the flex container.

    **Values:**

    - Length values (e.g., `100px`, `50%`).
    - `auto`: Default size of the item (content size).

    **Implementation:**

    ```css
    .item {
      flex-basis: 200px;
    }
    ```

11. **`align-self`**

    This property overrides the `align-items` value for a specific flex item.

    **Values:**

    - `auto`: Use the value of `align-items` (default).
    - `flex-start`: Align the item at the start of the cross axis.
    - `flex-end`: Align the item at the end of the cross axis.
    - `center`: Center the item along the cross axis.
    - `baseline`: Align the item based on its baseline.
    - `stretch`: Stretch the item to fill the container's cross axis.

    **Implementation:**

    ```css
    .item {
      align-self: flex-end;
    }
    ```

Flexbox is a powerful tool for creating responsive and dynamic layouts. By combining these properties and values, you can create complex and adaptable designs with ease. Remember that the flexibility and convenience of flexbox make it an excellent choice for many layout scenarios.

### Examples of flex properties:

```css
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .container {
            display: flex;
            flex-wrap: wrap;
            height: 500px;
            border: 2px solid #333;
            align-content: space-between;
            /* align-content: space-between; */
        }

        .item {
            flex:1 0 200px;
            height: 100px;
            border: 1px solid #666;
            margin: 5px;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 16px;
        }


    </style>
    <title>align-content Example</title>
</head>
<body>
    <div class="container">
        <div class="item">Item 1</div>
        <div class="item">Item 2</div>
        <div class="item">Item 3</div>
        <div class="item">Item 4</div>
        <div class="item">Item 5</div>
        <div class="item">Item 6</div>
        <div class="item">Item 6</div>
        <div class="item">Item 6</div>
        <div class="item">Item 6</div>

    </div>
</body>
</html>
```

The line `flex: 1 0 100px;` is a shorthand property that combines three individual properties related to flex layout: `flex-grow`, `flex-shrink`, and `flex-basis`.

Here's what each part of `flex: 1 0 100px;` means:

1. **`flex-grow`**: This value controls how much the flex item can grow relative to other flex items within the same container if there's extra space along the main axis.

   - Value: `1` means the item can grow equally along with other items.
   - Value: `0` means the item won't grow if there's extra space.

2. **`flex-shrink`**: This value controls how much the flex item can shrink relative to other flex items if there's not enough space along the main axis.

   - Value: `0` means the item won't shrink if there's limited space.

3. **`flex-basis`**: This value sets the initial size of the flex item before it's distributed within the flex container along the main axis.

   - Value: `100px` sets the initial size of the item to 100 pixels.

So, `flex: 1 0 100px;` indicates that the flex item can grow (but not shrink), and its initial size is set to 100 pixels. The value `1` for `flex-grow` indicates that the item can take up additional space, and the value `0` for `flex-shrink` indicates that the item won't shrink if there's not enough space.

This shorthand property is quite handy when you want to control the behavior of a flex item's growth, shrinkage, and initial size in a compact way.
