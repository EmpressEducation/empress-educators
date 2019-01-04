# **Figures and other images**

!!! Summary 
    Use SVG files or crushed PNG images; use the `<figure>` element; don't use the `height` attribute; provide alt text; use your site's standard image styling; provide high-resolution images when practical.

Use images only when they provide useful visual explanations of information that is otherwise difficult to express with words, or for screenshots of UIs that are important to the discussion.

Some best practices for images.

___

### **Creating and saving images**

-   To create a diagram, use any drawing tool.
-   If you have an SVG file, use it as your image. If you don't have an SVG file, then save your image as a PNG file unless you have a good reason to use a different format.
-   Make your screenshots of windows look like real windows, usually windows from a recent version of macOS unless there's a good reason to use a different operating system. For example, include the window's title bar in the screenshot. And if a given window has a drop shadow, then include the drop shadow in the screenshot as well.

___

### **Text associated with images**

Some best practices for text with images:

-   To include an image in your document, wrap your `<img>` element in a `<[figure](https://html.spec.whatwg.org/multipage/semantics.html#the-figure-element)>` element, with a `<[figcaption](https://html.spec.whatwg.org/multipage/semantics.html#the-figcaption-element)>` if appropriate.

    !!! success "Recommended" 
``` html
    <figure id="emu-foot">
      <img src="/assets/images/emu-foot.svg"
        width="120"
        alt="An emu foot has three toes.">
      <figcaption><b>Figure 1.</b>Diagram of an emu's
    foot</figcaption>
    </figure>
```

-   For a figure caption, use the form "<b>Figure *number*.</b> *Description*".
-   Don't end a figure caption with a period unless the caption ends with a full sentence. Generally try to avoid putting full sentences in captions; full sentences are more appropriate for `longdesc` and `alt` text, and for introductory sentences.
-   To refer to a figure, mention it by number ("figure 1"), to avoid spatial descriptions (that is, don't say "the image below").
-   As shown above, use an `[alt](https://html.spec.whatwg.org/multipage/embedded-content.html#alt)` attribute to provide a text alternative for the image, which is used by assistive technologies, such as screen readers, and might appear if the image cannot load.

    However, if the image is decorative (not informative) or it's provided only as a visual aid for information that is already expressed in text, then provide empty alternative text (`alt=""`) so it will be ignored by assistive technologies. (If you exclude the `alt` attribute completely, then screen readers might instead read the filename aloud.)

    As per the [HTML specification](https://html.spec.whatwg.org/dev/images.html#general-guidelines), "the most general rule to consider when writing alternative text is the following: the intent is that replacing every image with the text of its `alt` attribute not change the meaning of the page." So if the alternative text is redundant with surrounding text or it's not useful to visually impaired readers, use the empty tag.

-   In most cases, avoid embedding explanatory text in screenshot graphics; text that's incorporated into a graphic hurts accessibility and increases localization costs. If your text is important enough to be worth embedding, then you can include explanatory text in the image, but in that case, be sure to also provide the same information in a form that people with visual disabilities can use.

___

### **High-resolution images**

Modern browsers can use high-resolution images if they are available; this makes the images look better on high-resolution displays.

To provide a high-resolution image, use the `<img>` element's `srcset` attribute in addition to the standard `src` attribute. The `srcset` attribute lets you specify different image assets for different screen resolutions. It accepts a comma-delimited set of image URLs, with the target screen resolution specified by a size qualifier: `1x` meaning the "standard" resolution, `2x` meaning "double" the resolution, and so on.

If a web browser supports the `srcset` attribute, it selects an image from the specified images that's an appropriate resolution for the current display. If the browser doesn't support the `srcset` attribute, it uses the image in the `src` attribute. Consequently, you must always still include the `src` attribute.

For example, to provide both a standard resolution image and a double-resolution image, add a `srcset` attribute and specify both `1x` and `2x` image assets:

```html
<img src="/assets/images/skateboard.png" 
    srcset="/assets/images/skateboard.png 1x,
    /assets/images/skateboard_2x.png 2x" 
    width="375" alt="" />
```

-   The `width` attribute matches the CSS pixel size used for the page dimensions. (The height is automatically calculated based on the width and the image's proportions; *don't* state it explicitly.)
-   Set the `src` attribute to point to the standard-resolution (`1x`) image, *not* the `2x` version. (Almost everyone who has a high-resolution screen also has a modern browser that can recognize the `srcset` attribute. The `src` attribute is mainly used by older browsers on low-resolution devices, which should download the smaller, low-resolution image.) Even if your original image is the higher-resolution image, set the `src` attribute to use the standard-resolution version; don't force a reader using a low-resolution screen to download a graphic that's higher-resolution than they can view.
-   The filename for the double-resolution image (in this case, `skateboard_2x.png`) can be anything---it's the "` 2x`" value following the filename that informs the browser which resolution the file is. But it's a good idea to use a filename of the form `*basename*_2x.*extension*` to make clear to human readers that it's a double-resolution version of `*basename.extension*`.
-   The double-resolution image must be exactly twice the width and height of the standard image, give or take a pixel. (For example, it's okay for the double-resolution image to be 875x500 and the standard size to be 438x250.)
-   Don't scale up an existing `1x` image to make the `2x` version. If all you have is the `1x` version, then use it alone. But if you're starting with a high-resolution image (at `2x` resolution or better), then you can scale it down to appropriate dimensions for `1x` and `2x`.
-   Currently, only an additional `2x` image is necessary, but someday screen PPI may increase further. So the `srcset` attribute supports further alternative sizes, each specified by the appropriate multiplier, such as `3x` or `4x`.
-   A browser that supports the `srcset` attribute uses only the images provided in that attribute---it ignores the `src` attribute. So specify all available image resolutions in the `srcset` attribute.

!!! note "Note"
    If you frequently revise an image, then you can use the `2x` image for both the `src` and `srcset` attributes, rather than maintaining multiple sizes of the image. If things stabilize and you no longer need to revise the image, then you can add a `1x` version.

For more information, see the HTML specification for the `<[img](https://html.spec.whatwg.org/multipage/embedded-content.html#the-img-element)>` element.

___

### **Laying out images on a page**

-   Don't try to place an image manually; for example, don't use a `style` attribute or other workarounds to control the image's left/right justification or the margins around the image.
-   Don't make your image too small. It's fine for an image to take up the full width of a page.
-   Consider how the image will look when printed out.
-   In general, don't use an image that's wider than the column it appears in. On [developers.android.com](https://developers.android.com), for example, the main-body column is 856px wide, so use images that are no wider than that. In that context, the high-resolution 2x version of the image should be no wider than 1712px.

-   Screenshots at full resolution often take up too much space on the page, so you may have to resize them.
-   If the graphics were created by someone else (for example, a designer on the team you're supporting), it may be fairly trivial for them to provide you with images at the appropriate size. If the images they provide are wider than 856px, ask the designer if they can provide the relevant graphics as 856px/1712px pairs.

-   Don't link to the figure from within the same page unless it's a very long page and you're linking to it from quite far away on the page.
-   Don't center the image on the page.
-   Don't put the `<img>` inside a `<p>`.

To place the image inline (align left):

``` html
<figure id="descriptive-id" class="attempt-left">
<img src="" alt="" width="XXX" />
<figcaption>
  <b>Figure 1.</b> Description of figure
</figcaption>
</figure>
```

To align right:

``` html
<figure id="descriptive-id" class="attempt-right">
  <img src="" alt="" width="XXX" />
  <figcaption>
    <b>Figure 2.</b> Description of figure
  </figcaption>
</figure>
```