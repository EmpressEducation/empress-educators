# **Code in text**

!!! Summary 
    Use code font for code that appears in text.

!!! note "Note" 
    Where documentation is specific to Android, its heading is preceded by .

In ordinary text sentences (as opposed to, say, [code samples](https://developers.google.com/style/code-samples)), use code font to mark up most things that have anything to do with code. In HTML, use the `<code>` element; in Markdown, use backticks (```).

___

### **Some specific items to put in code font**

-   Language keywords.
-   Class names.
-   Method and function names.
-   XML and HTML element names. (Also place angle brackets (`<>`) around the element name; you may have to escape the angle brackets to make them appear in the document.)
-   Attribute names and values.
-   Filenames and paths.
-   Defined (constant) values for an element or attribute.
-   Namespace aliases.
-   HTTP verbs.
-   HTTP status codes.
-   HTTP content-type values.
-   Query parameter names and values.
-   Command-line utility names.
-   [DNS record types](https://en.wikipedia.org/wiki/List_of_DNS_record_types).

Generally don't put quotation marks around an item that's in code font, unless the quotation marks are part of the item.

___

### **Items to put in ordinary (Roman) font**

-   URLs. (But often it's a good idea to put these on a separate line, enclosed in `<pre>`, or else to turn them into links. See also the page on [link text](https://developers.google.com/style/link-text).)
-   Email addresses.
-   Headings (including table headings). For clarity, where possible, add a noun to the code-related term in the heading: "Calling the Foo method"; "Setting the Bar parameter".

___

### **Other HTML elements for code**

Avoid use of the `<xmp>` element; it's [deprecated](https://html.spec.whatwg.org/multipage/obsolete.html#obsolete-but-conforming-features) in modern HTML.

Use the `<kbd>` element to indicate input to be typed (or otherwise entered) by the user. Use the `<var>` element to indicate any variable (including both specific variable names from code samples and metasyntactic placeholder variables like *foo*). Note that you can use these elements even within a `<pre>` block; for example:

<pre>
$ <kbd>ls <var>filename</var></kbd>
<var>filename</var>
$
</pre>

___

### **Method names**

When you refer to a method name in text, omit the class name except where including it would prevent ambiguity. For example:

Not recommended: To retrieve the zebra's metadata, call its `animal.get()` method.

Recommended: To retrieve the zebra's metadata, call its `get()` method.

Put an empty pair of parentheses after a method name to indicate that it's a method.

___

### **Placeholder variables**

To create a placeholder variable, do the following:

-   In HTML, wrap the placeholder variable in a `<var>` element.
-   In Markdown, use an underscore before and after the placeholder variable.

For placeholder variables, use lowercase characters with hyphen delimiters.

For example, in HTML:

Not recommended:

-   https://developers.google.com/<var>API-name</var>
-   https://developers.google.com/<var>API_name</var>
-   https://developers.google.com/<var>API name</var>
-   https://developers.google.com/<var>api_name</var>
-   https://developers.google.com/<var>apiName</var>

Recommended:

-   https://developers.google.com/<var>api-name</var>
-   https://developers.google.com/<var>method-name</var>

And in Markdown:

Not recommended:

-   https://developers.google.com/_API-name_
-   https://developers.google.com/_API_name_
-   https://developers.google.com/_API name_
-   https://developers.google.com/_api_name_
-   https://developers.google.com/_apiName_

Recommended:

-   https://developers.google.com/_api-name_
-   https://developers.google.com/_method-name_

If the context in which your placeholder variables appear makes using lowercase characters with hyphen delimiters a bad idea, use something else that makes sense to you, but be internally consistent.

___

### **HTTP status codes**

To refer to a single status code, use the following formatting and phrasing:

an HTTP `400 Bad Request` status code

In particular, call it a "status code" instead of a "response code," and put the number and the name in code font. If the "HTTP" is implicit from context, you can leave it out.

To refer to a range of codes, use the following form:

an HTTP `2xx` or `400` status code

In particular, use "*n*xx" (with a specific digit in place of *n*) to indicate "anything in the *n*00-*n*99 range," and put the status code number in code font even if you're leaving out the code's name.

If you prefer to specify an exact range, you can do so:

an HTTP status code in the `200`-`299` range

Here, too, put the numbers in code font.

___

### **Coding style guides**

The following Google coding-style guides are available on GitHub:

-   [JavaScript Style Guide](https://google.github.io/styleguide/javascriptguide.xml).
-   [Java Style Guide](https://google.github.io/styleguide/javaguide.html).
-   [C++ Style Guide](https://google.github.io/styleguide/cppguide.html).

___

### **Keywords**

In general, don't use technical keywords as if they were English verbs or nouns. If in some rare cases you do, then don't try to inflect them.

#### **Examples**

Not recommended: `POST` the data.

Recommended: To add the data, send a `POST` request.

Not recommended: Retrieve information by `GET`ting the data.

Recommended: To retrieve the data, send a `GET` request.

Not recommended: `Close()`ing the file requires you to have `open()`ed it first.

Recommended: You can't close the file before opening it.

Also recommended: You can't call the `close()` method for a file before you call `open()`.

**Exception:** When documenting a Java API, it's common to leave out words like "object" or "instance" and instead just use the class name as a noun: "store the `Foo` you got from the `FooFactory`." If you need to pluralize such nouns, then add "object" or "instance": "store the `Foo` objects you got from the `FooFactory` instances."

___

### **Linking API terms in Android**

When you're writing code comments that you'll turn into generated reference documentation, link to all elements of Android APIs: classes, methods, constants, XML attributes, etc. Use code font and regular HTML `<a>` elements to link to this reference material.

Link `AndroidManifest.xml` elements and attributes to the API guide pages. Link the attribute for a particular widget or layout to its Javadoc in the widget or layout's API reference entry.

Recommended: `<a href="/guide/topics/manifest/data-element.html">data</a>`

Very common classes such as `Activity` and `Intent` don't need to be linked every time. If you use a term as a concept rather than a class, then don't put it in code font and don't capitalize. Here are some objects that do not always require Javadoc links or capitalization:

-   activity, activities
-   service
-   fragment
-   view
-   loader
-   action bar
-   intent
-   content provider
-   broadcast receiver
-   app widget

If you use one of these terms in the context of referring to an actual instance, use the formal class name and link to its reference page. Here are two examples:

Recommended: An [`Activity`](https://developer.android.com/reference/android/app/Activity.html) is an app component that provides a screen with which users can interact ...

Recommended: The user interface for an activity is provided by a hierarchy of views---objects derived from the [`View`](https://developer.android.com/reference/android/view/View.html) class.

To link to a class or method:

-   To link to a class, use the class name as link text. For example: `<a href="/reference/android/widget/TextView">TextView</a>`
-   To link to a method, use the method name as a fragment identifier. If you're linking to a static method, also include the class name in the link text. If you need to distinguish between overloaded versions of a particular method, consider showing the full signature. For example: `<a href="/reference/android/app/Activity.html#onCreate(android.os.Bundle)">onCreate(Bundle)</a>`
-   To link the attribute for a particular widget or layout to its Javadoc in the widget or layout's API reference entry, use the URL for the page, and then add the fragment identifier `#attr_android:*attribute_name*`. For example, to link to the XML attribute `android:inputType` for the `TextView` widget, add the following: `<a href="/reference/android/widget/TextView.html#attr_android:inputType>inputType</a>`