# RELECTICVE ANSWERS

## Class 01 The 2026 Web Ecosystem

                    (1)
    HTML File
        │

    HTML Parser
        │
    DOM Tree
    (Document Object Model)

        html
         ├── head
         └── body
              ├── h1
              ├── p
              └── div

                    │
        CSS + DOM Combined
                     │
             Render Tree
      (Only visible elements)

                    │

                 Layout
      (Calculates size & position)

                    │

                  Paint
      (Pixels drawn on the screen)

                    │

             Final Webpage

WHY UNDERSTANDING THIS MATTERS AS A WEB DEVELOPER

Understanding this process helps developer build faster and better westites. Too many layout make the pages laggy and if the webpage is slow, knowing the rendering process helps to identify performance and problems. Understanding the process helps to optimize code to improve loading speed and user exprience. it also helps debugging easy.

                    (2)

QUIC solves the problem of slow and interrupted internet connections. Older internet systems using TCP can pause everything when one piece of data is lost, making websites and videos slower.

QUIC, used in HTTP/3, makes the internet faster by allowing data to move independently. If one part is delayed, the others continue loading normally.

It also helps mobile users because connections stay active when switching from Wi-Fi to mobile data.

QUIC helps pages load faster, reduces buffering, and gives smoother online experiences even on weak networks.

            (3)

One website i visit is an online money lender, what is notices is that their layout is poor and the navbar is overlapping, this happen when the developer did not use proper semantic tag like `<header>`, `<nav>`, `<main>`, and `<footer>`. poor accessibility for the screen reader, button and link are unclear.

        PRODUCT THINKING

            (1)

Semantic HTML helps search engines clearly understand the structure and meaning of a chef’s blog content, which can improve SEO and increase traffic.

`<main>` tells search engines where the most important content of the page is located.

`<article>` identifies each blog post as a complete piece of content, such as a recipe or cooking tutorial. Search engines can index these posts more accurately.

`<header>` contains important information like the blog title, headings, author name, and publication date. This helps search engines understand the topic of the page.

`<aside>` is used for related recipes, cooking tips, ads, or side content. It separates less important content from the main article.
\*\*

        (2)

The benefit of Edge computering is lower latency because data travels a shorter distance between players and servers. Action happen almost instantly.

        ENGINEERING BEST PRACTICE

I disagree with the idea of using only `<div>` elements everywhere, even if the website appears to work fine. While `<div>` tags are useful for layout and styling, relying on them for everything ignores the benefits of semantic HTML.

Semantic HTML improves **SEO**. Search engines like Google use semantic tags to understand the structure and meaning of content. For example, an `<article>` clearly tells search engines that the content is a blog post or news article, which can improve ranking and visibility.

Semantic HTML helps with **code maintainability**. When another developer reads the code, tags like `<header>` or `<section>` immediately explain the purpose of the content. A page filled only with `<div>` tags becomes harder to understand and maintain over time.

Semantic elements improve **accessibility**. Screen readers used by visually impaired users understand tags like `<main>`, `<nav>`, `<article>`, and `<footer>` better than generic `<div>` tags. This helps users navigate websites more easily.

## Class 02 Typography & Information Hierarchy

                (1)

The `<em>` tag is used to give **emphasis** to a word or phrase, while the `<i>` tag is mainly used to display text in an italic style without adding special meaning.

`<em>` is semantic, meaning screen readers may change their tone when reading it aloud. It tells browsers and search engines that the text is important or stressed.

Example:

    <p>You <em>must</em> save your work before closing the app.</p>

Here, “must” is strongly emphasized.

`<i>` is mostly for visual styling or special text such as foreign words, book titles, or technical terms.

Example:

    <p>I recently read <i>Things Fall Apart</i> by Chinua Achebe.</p>

Here, the book title is italicized but not emphasized.

                (2)

1.  **`<button>`**
    Screen readers recognize `<button>` as an interactive element. They announce it as a "button" and allow keyboard users to activate it easily. Browsers handle it specially because buttons are meant for actions like submitting forms or opening menus.

2.  **`<img>` with `alt` text**
    Screen readers read the `alt` attribute to describe images for visually impaired users. This helps users understand the meaning or purpose of an image.

3.  **`<a>` (Anchor Links)**
    Screen readers identify links and often allow users to jump through them quickly. Browsers treat them specially because links are used for navigation between pages or sections.
    This improves accessibility and page understanding.

                      (3)

    Aria-label can be use when an element is has no visible text but still needs a description for screen reader. it okay to use correct semantic element.

             Accessibility Reflection


                     Product Thinking

I would organize the content so developers can quickly scan, understand, and find what they need.

## `<h1>` — Payment API Documentation

This is the main title of the entire documentation page.

## `<h2>` — Introduction

Explain what the API does, supported formats (JSON, REST), and common use cases.

### `<h3>` — Base URL

Show the main API endpoint.

### `<h3>` — Authentication

Explain API keys, tokens, and authorization headers.

## `<h2>` — Quick Start Guide

Help developers make their first successful request quickly.

### `<h3>` — Example Request

Provide sample code using JavaScript or Python.

### `<h3>` — Example Response

Show sample JSON responses.

---

## `<h2>` — Endpoints

Each major API feature gets its own subsection.

## Class 03 Modern Assets & Linking

            (1)

I will first convert the image to AVIF (best compression and quality) or WebP (Fallback for wider support). these formats reduce file size dramatically while keeping good quailty.

I will resize the image properly. The tools to use TinyPNG or ImageOPtim. The reason is for faster loading, better Core web Vitals, lower bandwidth usage and also improved SEO.

            (2)

srcset is an HTML image attribute that allows the browser to choose the most appropriate image file based on the user's screen size, resolution.

            (3)

rel="noopener" is important because it prevents malicious websites opened in a new tab from secretly taking control of the original page and tricking users into phishing or scam attacks.

        Engineering Thinking

## Class 04 Modern Forms & User Experience

                (1)



                (2)

The autocomplete attribute tells the browser what kind of information an input field expects so it can: reduce typing effort,
improve accessibility and mobile UX.

        List 5 different values

(1) email

    <input type="email" autocomplete="email" />

Give feedback
Used for
login forms,
signup forms,
newsletter subscriptions.

(2) New Password

    <input type="password" autocomplete="new-password" />

Used for
account creation,
password reset forms.

(3) Name

    <input type="text" autocomplete="name" />

Used for
registration forms,
checkout pages,
profile settings.

(4) current-password

    <input type="password" autocomplete="current-password" />

Used for
login forms.

(5) street-address

    <input type="text" autocomplete="street-address" />

Used for
ecommerce checkout,
delivery forms,
billing information.

            Engineering Best Practice

form.html

## 05 The CSS Engine — Box Model & Specificity

                    (1)

+--------------------------------------------------+
| MARGIN |
| +--------------------------------------------+ |
| | BORDER | |
| | +--------------------------------------+ | |
| | | PADDING | | |
| | | +--------------------------------+ | | |
| | | | CONTENT | | | |
| | | | Text, image, button, etc. | | | |
| | | +--------------------------------+ | | |
| | +--------------------------------------+ | |
| +--------------------------------------------+ |
+--------------------------------------------------+

Content: the thing inside the element like text image e.t.c
Padding: Space insider the border, around the content.
Border: The line wrapping the padding/content.
Margin: Space outside the element, separating it from other elements.

.first div {
margin-bottom: 20px;
}

.second div {
margin-top: 30px;
}
How much space between them?
30px because vertical margins between block elements can collapse.

                (2)

CSS specificity determines which rule the browser should use or applies when multiple selectors target the same element.

| Selector              | Specificity |
| --------------------- | ----------- | ------ |
| `.header nav ul li a` | `(0,1,4)`   | winner |
| `nav a.active`        | `(0,1,2)`   | loss   |
| `.nav-links a`        | `(0,1,1)`   | loss   |

the winner has the highest number of element selectors after the class count ties.

                (3)

The system the browser uses to decide which CSS rule getw applied when multiple rules targets the same element is called CASCADE.

Cascade help developer to write few and clean CSS.

        Engineering Thinking

content-box.html

## 06 Flexbox Mastery

            (1)

Flex-basis: it is refer to as the "starting seat size".

If three person were in a class:
Person A starts with 100cm of Seat
Person B starts with 200cm
Person C starts with 150cm

Each person space that was taken is called Flex-Basis

Flex-grow: it is the refer to the extra space the person get. Flex-grow decide who is allow to grow and how much.

Flex-shrink: it is refer to the space give up, like in the example above, if the class is overcrowded, flex-shrink decides who sacrifices seat space first.

            (2)

align-items:stretch will not work as expected when a flex item already has an explicit size.

    <div class="container">
      <div class="card auto-height">Auto Height</div>

      <div class="card fixed-height">Fixed Height</div>
    </div>

                Engineering Thinking
                (1)

nav.html

                (2)

instagram.html

## 07 CSS Grid & Layout Complexity

                (1)

CSS Grid is used when you need two-dimensional layout control, which means you care about the rows and the columns at the same time. while flexbox is mainly designed for one-dimensional layouts (either a row or a column).

    3 specific scenarios

1.  Full Page Layouts
    +----------------------------------+
    | Header |
    +----------+-----------------------+
    | Sidebar | Main Content |
    | | |
    +----------+-----------------------+
    | Footer |
    +----------------------------------+

2.  Card Galleries/ Photo Layout
    Card | Card | Card
    Card | Card | Card
    Card | Card | Card

3.  Dashboard Layouts
    +-----------+-----------+
    | Featured | Small |
    | Article | Article |
    | +-----------+
    | | Small |
    +-----------+-----------+

              Engineering Thinking

                     (1) ASCII Layout Sketch

┌──────────────────────────────────────┐
│ HERO ARTICLE │
│ (spans full width) │
└──────────────────────────────────────┘

┌──────────────────┬───────────────────┐
│ Secondary Article│ Secondary Article │
│ 1 │ 2 │
└──────────────────┴───────────────────┘

┌──────────────────────────────────────┐
│ WIDE BOTTOM ARTICLE │
└──────────────────────────────────────┘

┌────────────┬────────────┬────────────┐
│ Small Art. │ Small Art. │ Small Art. │
│ 1 │ 2 │ 3 │
└────────────┴────────────┴────────────┘

The code for the Grid grid.html

            (2)

dashboard.html

## Class 08 Tailwind CSS Fundamentals

                (1)

The utility-first philosophy means:
Instead of writing custom CSS classes like .card, .button, or .hero, you build designs directly in HTML using small single-purpose utility classes.

                (2)

I don't uunderstand.

            Product Thinking

Tailwind Css make coding easy and straightforward, it optimized and also easy to load on webpage because it is not using external css it is inline and it make it fas to load.

            Engineering Thinking

## 10 Memory & Variables

        (1)

Let: it is use when the value is going to be reassign  
const: it is use when the value will not be reassign again.
var: it can also be reassigned
┌──────────┬──────────────┬───────────┬──────────────┐
│ Keyword │ Scope │ Hoisted? │ Reassignable │
├──────────┼──────────────┼───────────┼──────────────┤
│ var │ Function │ Yes │ Yes │
│ let │ Block │ Yes* │ Yes │
│ const │ Block │ Yes* │ No │
└─────────────────────────────────────────────────┘

            (2)

The Temporal Dead Zone is the time between entering a scope → and the variable being initialized
during which a let or const variable exists but cannot be accessed.

            JavaScript
    console.log(user);
    let user = "Adisa";

        OUTPUT
    ReferenceError:
    Cannot access 'user' before initialization
