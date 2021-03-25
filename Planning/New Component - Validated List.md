# New Component - Validated List
---

## [[2021-03-25]] 

---

![[Screen Shot 2021-03-25 at 10.38.38 AM.png]]

### Overview

Component serves as a listing for individual items. The current need is for a Create New Users UI. As the user types, it needs to create badges as the user enters each item.

### Behavioral Brainstorming

#### Initial function

A user needs to be able to focus into this component and start typing text. It kinda needs to initially feel like a textarea component.

#### Continued usage as the user types

As long as their cursor is on the current line, they should see unrendered text. As soon as they hit enter to complete the item, it should then render the text into a component.
- Note: There needs to be some sort of validation that one can pass in that will determine the color-state of the rendered object. Let's create an `onRender` event for this. 



### Physical Elements of the Component

1. A div to serve as a canvas/container
2. A transparent text `<input>` that should always receive focus when the user clicks the overall component.
	1. It should span the width of the container and only should have a leading of `1`
	2. If the user hits the tab key, it should move focus to the next component.
3. A `<VirtualList>` above the text input. Appears empty w/ no height when there are no items.
	2. This is actually perfect (I'm looking at the stories for `<VirtualList>` RN). It has a bunch of facilities that we'll need for this to work.
	1. For instance, we could use `renderRow` for our custom render function. This will render a dismissable label with a conditional color.
4. As the user enters items, the `<VirtualList>` will continue growing with validated, rendered items. As it grows, the scroll position will always need to be at the bottom of the container, always showing the transparent `<input>`


### Major Issue @ 1:34 PM

What about editing existing items? How is that going to work? What if I introduced a typo in an email address and want to change it? Do I just have to nuke it and then enter the corrected version?




