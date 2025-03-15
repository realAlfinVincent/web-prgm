# **Flexbox Guide: From Basic to Advanced**

Flexbox (Flexible Box Layout) is a powerful CSS module that provides an efficient way to align and distribute space among items in a container. This guide covers **basic to advanced** flexbox concepts with examples.

---

## **1. Basics of Flexbox**

### **1.1 Enabling Flexbox**
To use Flexbox, set `display: flex;` on a container.

```css
.container
{
    display: flex;
    background-color: lightgray;
    padding: 10px;
}
```

All direct child elements inside `.container` become **flex items**.

### **1.2 Flex Direction**
Defines the direction of flex items.

```css
.container
{
    display: flex;
    flex-direction: row; /* Default: horizontal */
}
```

| Value | Description |
|--------|--------------|
| `row` | Items arranged horizontally (default) |
| `row-reverse` | Items in reverse order |
| `column` | Items arranged vertically |
| `column-reverse` | Items in reverse vertical order |

---

## **2. Aligning Items**

### **2.1 Justify Content (Horizontal Alignment)**
Used to align items **horizontally**.

```css
.container
{
    display: flex;
    justify-content: center; /* Centers items */
}
```

| Value | Effect |
|--------|-------------|
| `flex-start` | Aligns items to the start |
| `flex-end` | Aligns items to the end |
| `center` | Centers items |
| `space-between` | Distributes items with space between them |
| `space-around` | Spaces items with padding on each side |
| `space-evenly` | Equal spacing between items |

### **2.2 Align Items (Vertical Alignment)**
Used to align items **vertically** when `flex-direction: row;`.

```css
.container
{
    display: flex;
    align-items: center; /* Centers items vertically */
}
```

| Value | Effect |
|--------|-------------|
| `stretch` | Stretches items to fill container (default) |
| `flex-start` | Aligns items to the top |
| `flex-end` | Aligns items to the bottom |
| `center` | Centers items vertically |
| `baseline` | Aligns items based on text baseline |

### **2.3 Align Self (Individual Item Alignment)**
Overrides `align-items` for a single item.

```css
.item
{
    align-self: flex-end; /* Moves only this item to bottom */
}
```

---

## **3. Controlling Item Sizes**

### **3.1 Flex Grow**
Defines how much an item can grow relative to others.

```css
.item
{
    flex-grow: 1; /* Items expand equally */
}
```

### **3.2 Flex Shrink**
Controls how items shrink when space is reduced.

```css
.item
{
    flex-shrink: 2; /* Shrinks twice as fast as others */
}
```

### **3.3 Flex Basis**
Sets the default size of an item before resizing.

```css
.item
{
    flex-basis: 200px; /* Default width/height */
}
```

### **3.4 Shorthand: `flex`**
Instead of writing multiple properties, use shorthand:

```css
.item
{
    flex: 1 1 200px; /* flex-grow | flex-shrink | flex-basis */
}
```

---

## **4. Advanced Flexbox Concepts**

### **4.1 Ordering Items**
The `order` property changes item positions.

```css
.item1
{
    order: 2;
}

.item2
{
    order: 1;
}
```

### **4.2 Nested Flexbox**
Flexbox containers can be nested.

```css
.container
{
    display: flex;
}

.nested-container
{
    display: flex;
    flex-direction: column;
}
```

### **4.3 Creating a Responsive Navigation Bar**

```css
nav
{
    display: flex;
    justify-content: space-between;
    padding: 10px;
    background: #333;
}

nav a
{
    color: white;
    text-decoration: none;
    padding: 10px;
}
```

```html
<nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Services</a>
    <a href="#">Contact</a>
</nav>
```

---

## **5. Common Flexbox Layouts**

### **5.1 Centering an Element**

```css
.container
{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh; /* Full page height */
}
```

### **5.2 Creating a Card Layout**

```css
.container
{
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
}

.card
{
    flex: 1 1 300px;
    padding: 20px;
    border: 1px solid #ccc;
}
```

---

## **Conclusion**
Flexbox is a powerful tool for designing responsive layouts. Mastering it will help you create modern web designs easily. 🎯

Would you like more examples? 😊

