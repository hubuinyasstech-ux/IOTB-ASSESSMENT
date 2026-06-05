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

1. **`<button>`**
   Screen readers recognize `<button>` as an interactive element. They announce it as a “button” and allow keyboard users to activate it easily. Browsers handle it specially because buttons are meant for actions like submitting forms or opening menus.

2. **`<img>` with `alt` text**
   Screen readers read the `alt` attribute to describe images for visually impaired users. This helps users understand the meaning or purpose of an image.

3. **`<a>` (Anchor Links)**
   Screen readers identify links and often allow users to jump through them quickly. Browsers treat them specially because links are used for navigation between pages or sections.
   This improves accessibility and page understanding.
