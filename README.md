# Palindrome Checker

  

A fun and simple web application built with vanilla **HTML**, **CSS**, and **JavaScript** that determines whether a given input text is a palindrome.

  

The application adheres strictly to the definition of a palindrome by **ignoring punctuation, spacing, and case differences**.

  

---

  

## Features

  

-  **Case & Punctuation Agnostic:** Input is cleaned by removing non-alphanumeric characters and converting to lowercase.

-  **Intuitive UI:** Clean, modern layout styled with CSS.

-  **Client-Side Logic:** Fast and instant — all processing happens in the browser.

-  **User-Friendly Alerts:** Alerts the user if they attempt to check an empty input.

  

---

  

## 🛠️ Technology Stack

**HTML5** - Provides structure (input field, button, result display).  
**CSS3** - Styles the interface with modern layout, shadows, and responsive elements.  
**JavaScript** - Implements the palindrome logic, DOM manipulation, and event handling.  

  

---

  

## Palindrome Logic Explained

  

The core logic relies on cleaning the input, normalizing the case, reversing the string, and comparing the two.

  

### Clean the Input

```js

const  replaced = textInput.value.replace(/[^A-Za-z0-9]/g, "").toLowerCase();

```

### How  It  Works:

1.  Cleaning  with .replace()

The  Regular  Expression:

```js
/[^A-Za-z0-9]/g
```
Removes  any  character  NOT  in:
- A–Z
- a–z
- 0–9
  
Example:

```
"My age is 0, 0 si ega ym." → "Myageis00siegaym"
```

2.  Case Normalization
.toLowerCase() makes  the  comparison  case-insensitive.

Example:

```
"Myageis00siegaym" → "myageis00siegaym"
```

3.  Reversal  and  Comparison
The  string  is  reversed  and  checked  against  the  original:
```javascript
const  reversed = [...replaced].reverse().join("");
```
If  replaced === reversed, the  input  is  a  palindrome.

### Installation & Setup

This is a fully client-side project — setup is quick.

1.  Clone  the  Repository
```bash
git  clone https://github.com/PrinceLemayian/Palindrome-checker
```

2.  Navigate  to  the  Project  Directory

```bash
cd  palindrome-checker
```

3.  Run  the  Application
Open  the  index.html  file  in  your  web  browser
(usually  by  double-clicking  it).

### Usage

- Open index.html 
- Type  any  word, phrase, or  sentence  into  the  input  box
- Click  the  "Check"  button
- The  result  will  appear  below  the  input
