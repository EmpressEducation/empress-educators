# **URLs for images**

!!! Summary 
    Use a site-root-relative URL for images served from the same domain as your page.

When you're including an image that's served from the same domain as your page, use a site-root-relative URL (starting with "/"). Use this URL format (starting from the site root) even if the image is in the same directory as the page that includes it.

### HTML

### Markdown

Insert the URL in the `src` attribute of your `<img>` element:

<img src="/shared/images/arrow-24.png" />

**Note:** There are many valid linking styles. This guideline isn't a general statement about best practices for URLs in all contexts---it's just our house style.