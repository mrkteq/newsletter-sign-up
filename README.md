# Frontend Mentor - newsletter-sign-up solution

![](/design/desktop-design.jpg)

Source: [Newsletter sign-up challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/newsletter-signup-form-with-success-message-3FC1AZbNrv).

## The challenge

Users should be able to:

- Add their email and submit the form
- See a success message with their email after successfully submitting the form
- See form validation messages if:
  - The field is left empty
  - The email address is not formatted correctly
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

## Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS logical properties
- CSS Grid
- Mobile-first workflow

## What I learned

In CSS, the `isolation` property is used to control the stacking context of an element and its descendants. It is particularly useful when dealing with complex layouts that use overlapping elements or z-index.


```css
.container {
    position: relative;
}

.element1 {
    position: absolute;
    z-index: 1;
}

.element2 {
    position: absolute;
    z-index: 2;
    isolation: isolate; /* This creates a new stacking context */
}

.element3 {
    position: absolute;
    z-index: 1; /* This will stack relative to the container, not element2 */
}
```

CSS `has()` selector is a powerful relational pseudo-class that allows you to select elements based on whether they contain certain child elements. It effectively lets you style a parent element based on its children, making it possible to apply styles conditionally, which was previously not achievable directly with CSS alone..
```css
form:has(> .button) {
  color: red'
}
```

Logical Properties provide a way to create layouts and handle styling in a more flexible and adaptable manner, especially for different writing modes, such as left-to-right (LTR) and right-to-left (RTL) languages. This approach allows developers to write code that is more accessible and internationalisation-friendly.

**Key Concepts of Logical Properties**

1. **Writing Modes**:
   - CSS logical properties can adapt to various writing modes (e.g., horizontal-tb for most languages, vertical-rl for some Asian scripts).
   - The logical properties will adjust automatically based on the document's writing direction.

2. **Logical Axis**:
   - Instead of using physical properties (like `margin-left`, `margin-right`), logical properties use a logical approach that is relative to the element’s writing direction.

3. **Common Logical Properties**:
   - **Margins**:
     - `margin-block-start`: Equivalent to `margin-top` in LTR but becomes `margin-bottom` in RTL.
     - `margin-block-end`: Equivalent to `margin-bottom` in LTR but becomes `margin-top` in RTL.
     - `margin-inline-start`: Equivalent to `margin-left` in LTR but becomes `margin-right` in RTL.
     - `margin-inline-end`: Equivalent to `margin-right` in LTR but becomes `margin-left` in RTL.
   - **Padding**:
     - `padding-block-start`, `padding-block-end`, `padding-inline-start`, and `padding-inline-end` function similarly to margin properties.
   - **Borders**:
     - `border-block-start`, `border-block-end`, `border-inline-start`, and `border-inline-end`.

4. **Width and Height**:
   - `width` and `height` remain the same, but for logical dimensions, you can use:
     - `inline-size`: Represents the width of an element in a logical context.
     - `block-size`: Represents the height of an element in a logical context.

5. **Text Alignment**:
   - Instead of `text-align: left;` or `text-align: right;`, you can use:
     - `text-align: start;` (aligns to the start of the writing direction).
     - `text-align: end;` (aligns to the end of the writing direction).

6. **Flexbox and Grid**:
   - Flexbox and Grid properties also support logical properties.
   - For instance, `justify-content: start;` and `justify-content: end;` will adapt to the direction of content flow.

**Benefits of Logical Properties**
- **Internationalization**: Makes it easier to write CSS that works across multiple languages and layouts.
- **Maintainability**: Reduces the need for media queries and separate stylesheets for RTL layouts.
- **Responsive Design**: Enhances the adaptability of designs to cater to different cultural contexts without extensive rewrites.

**Example Usage**
```css
.element {
  margin-inline-start: 20px; /* Will be margin-left in LTR and margin-right in RTL */
  padding-block-end: 10px; /* Will be padding-bottom in LTR and padding-top in RTL */
}
```


## Continued development

Personal goal: spend a couple of hours a day to building things and playing with these new features.

## Acknowledgments

@KevinPowell (YouTube)