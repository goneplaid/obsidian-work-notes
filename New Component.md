# New Component
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
- There needs to be some sort of validation that one can pass in that will determine the color state of the rendered object. Let's create an `onRender` event for this. 