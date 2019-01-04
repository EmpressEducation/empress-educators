# **HTML formatting**

!!! Summary 
    Follow Google's standard HTML and CSS formatting guidelines.

Follow Google's [HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html). Exception: don't leave out optional elements.

In particular, here are a couple of basic guidelines from that style guide, which generally apply to other documentation source files, too (YAML, Markdown, etc.):

-   **Don't use tabs** to indent text; use spaces only. Different text editors interpret tabs differently, and some Markdown features expect spaces and not tabs.
-   **Indent by 2 spaces** per indentation level.
-   **Use all-lowercase** for elements and attributes.
-   **Don't leave trailing spaces** at the end of a line. (Except as needed for Markdown.)

___

### **Line length**

Break lines at 80 characters except in the following cases:

-   The metadata tags at the top of files (such as `page.metaDescription`) have to be all on one line, so those lines can be as long as needed.
-   If a URL in a link has a line break, the link won't work. If a URL is longer than 80 characters (quite common), you're stuck with it. In that case, put the URL on its own line with the `href` attribute to make it easier to review the text before and after, as the following example shows:

You can find more information in <a
href="https://example.com/long-url/johan-gambolputty-de-von-ausfern-...-von-hautkopf-of-ulm.html"
class="external-link">his biography.</a>

Break code snippets (in <pre> blocks) at 80 characters.

**Note:** Older files may use different line lengths. If you're making small changes to a file that has a consistent line length other than 80 characters, then make your changes conform to that file's line length rather than reformatting the whole file.

**Note:** When adding line breaks, make sure you don't change the meaning of the code! If you're not familiar with the programming language, ask for help from someone who is. But sometimes you just can't avoid a long line.