---
title: Markdown
---

# Markdown
This Markdown cheat sheet provides a quick overview of all the Markdown syntax elements.

## Basic
### Heading
```md
# H1
## H2
### H3
```

### Bold
```md
**bold text**
```
**bold text**

### Italic
```md
*italicized text*
```
*italicized text*

### Blockquote
```md
> blockquote
```
> blockquote

### Ordered List
```md
1. One
2. Two
3. Three
```
1. One
2. Two
3. Three

### Unordered List
```md
- First
- Second
- Third
```
- First
- Second
- Third

### Code
```md
`code here`
```
`code here`

### Horizontal Rule
```md
---
```
---

### Link
```md
[title](https:www.example.com)
```
[title](https:www.example.com)

### Image
```md
![alt text](/code-helper/minions.jpg)
```
![alt text](/code-helper/minions.jpg)

## Extended
### Table
```md
| Header1   | Header2 |
|-----------|---------|
| Title1    | a       |
| Title2    | b       |
```
| Header1   | Header2 |
|-----------|---------|
| Title1    | a       |
| Title2    | b       |

### Alignment
```md
| Left      | Centre  | Right    |
|:----------|:-------:|---------:|
| Title1    | a       |1         |
| Title2    | b       |2.0       |
```
| Left      | Centre  | Right    |
|:----------|:-------:|---------:|
| Title1    | a       |1         |
| Title2    | b       |2.0       |

### Fenced Code Block
```md
    ```
    {
      "name": "John Smith",
      "age" : 21
    }
    ```
```
```
{
  "name": "John Smith",
  "age" : 21
}
```

### Footnote
```md
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.
```
Here's a sentence with a footnote. [^1]

[^1]: This is the footnote.

### Heading ID
```md
### My Heading {#custom-id}
```
```html
<h3 id="custom-id">My Heading</h3>
```

### Definition List
```md
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```
```html
<dl>
  <dt>First Term</dt>
  <dd>This is the definition of the first term.</dd>
  <dt>Second Term</dt>
  <dd>This is one definition of the second term. </dd>
  <dd>This is another definition of the second term.</dd>
</dl>
```

### Strikethrough
```md
~~The world is flat.~~
```
~~The world is flat.~~

### Task List
```md
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```
Output will show the first checkbox ticked