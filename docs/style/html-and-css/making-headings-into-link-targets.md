# **Making headings into link targets**

!!! Summary 
    Use an `id` attribute when turning a heading into a link target.

To add a link target to a heading in HTML, add an `id` attribute to the `<section>` element that surrounds the heading's section. Don't use `<a name>`.

To add a link target to a heading in Markdown, add the following to the end of the line that the heading is on: `{: #*id-of-anchor* }`, where *id-of-anchor* is the ID for this heading.

In both HTML and Markdown, use lowercase for `id` values, and put hyphens between words.

#### **Examples**

Not recommended (HTML version):

<h2><a name="Introduction_To_Everything">Introduction to everything</a></h2>

Also not recommended (HTML version):

<a name="Introduction_To_Everything"></a>
<h2>Introduction to everything</h2>

Acceptable (HTML version):

<h2 id="introduction-to-everything">Introduction to everything</h2>

Recommended (HTML version):

<section id="introduction-to-everything">
<h2>Introduction to everything</h2>
...
</section>

Recommended (Markdown version):

## Introduction to everything {: #introduction-to-everything }