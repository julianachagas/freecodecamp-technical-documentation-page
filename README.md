# freeCodeCamp - Technical Documentation Page

Project created for the Responsive Web Design Certification from [freeCodeCamp](https://www.freecodecamp.org/learn).

Project 4/5: [Build a Technical Documentation Page](https://www.freecodecamp.org/learn/responsive-web-design/responsive-web-design-projects/build-a-technical-documentation-page)

## Technologies

- HTML/CSS

## Table of contents

- [Link](#link) 
- [Layout](#layout) 
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Link

- Live Site URL: [CodePen](https://codepen.io/julianachagas/full/vYZvxYy)

## Layout

### Web 🖥️

The navbar is fixed on the left side of the screen and it's always visible to the user (doesn't scroll with the page content).

<img src="screenshots/desktop.png" alt=""/> <br/>

### Mobile 📱

<img src="screenshots/mobile.png" alt=""/> <br/><br/>

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS positioning 

### What I learned

- The CSS `white-space` property

In order to style code blocks with CSS, it was useful to understand how white space inside an element is handled.

The `white-space` property specifies two things:
- Whether and how white space is collapsed;
- Whether lines may wrap at soft-wrap opportunities.

The property can have one of the following values:

- `normal` (initial value)
- `nowrap`
- `pre`
- `pre-wrap`
- `pre-line`
- `break-spaces`

In this project, `white-space: pre-line` was used in the `code` tag to collapse sequences of white space but preserve line breaks (lines are broken at newline characters in the source). 

`white-space: pre` was used to preserve white space in `<span class="css-property">` in order to have the indentation in the code block.

<img src="screenshots/code.png" alt=""/> <br/>

HTML

```html
<div class="code-editor">
  <code>
    <span class="css-selector">.container </span><span class="css-text">{</span>
    <span class="css-property">  display</span><span class="css-text">: grid;</span>
    <span class="css-property">  grid-template-columns</span><span class="css-text">: 1fr 1fr 1fr;</span>
    <span class="css-text">}</span>
  </code>
</div>
```
CSS

```css
.code-editor {
  background-color: var(--gray);
  margin-top: 1rem;
  border-left: 5px solid var(--primary-blue);
  padding: 0 0.5rem 1.5rem 1.5rem;
  overflow-x: auto;
}

.code-editor code {
  white-space: pre-line;
}

.css-property {
  color: #a30008;
  white-space: pre;
}
```

Source: [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space)

<br/>

- The CSS `overflow-x` and `overflow-y` properties

According to [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow):

>The `overflow-x` CSS property sets what shows when content overflows a block-level element's left and right edges. This may be nothing, a scroll bar, or the overflow content.

>The `overflow-y` CSS property sets what shows when content overflows a block-level element's top and bottom edges. This may be nothing, a scroll bar, or the overflow content.

In this project, `overflow-y: auto` was used in the navbar (`height: 100vh;`) so the browser will provide a scrollbar in the y-direction if the content overflows the viewport height. 

`overflow-x: auto` was used in the code block to prevent the lines of code from overflowing the container. 

When we use the value `auto` the browsers will only display the scrollbar if the content overflows, unlike the value `scroll` where browsers always display scrollbars whether or not any content is actually clipped.

<br/>

***
##### Made with 💜 by Juliana Chagas 
