# **Dashes**

!!! Summary 
    When you need a dash, use an em dash.

To indicate a break in the flow of a sentence---or an interruption---use an em dash, also known as a long dash. Don't put a space before or after it.

You can type the em dash character in various ways, depending on your platform:

**macOS**

Press `Option+Shift+hyphen`.

**Linux desktop environment**

Enable the Compose key. (Instructions for doing that vary depending on your flavor of Linux; for examples, see [Linux Keyboard Shortcuts For Text Symbols](http://fsymbols.com/keyboard/linux/compose/).) After the Compose key is enabled, you can create an em dash by typing the Compose key followed by three hyphens.

Alternatively, press `Control+Shift+u`, then let go of those keys, then type `2014`, then press `Return`.

Note: These Linux options don't work if you're signed in to the Linux command line from a remote system using ssh or the like; you have to be in a Linux desktop environment.

**Windows**

Turn num lock on, then hold down the left `Alt` key and type 0151 on the numeric keypad.

Don't use an en dash (the shorter dash) or a hyphen in place of an em dash. The use of " -- " (an en dash with spaces around it) in place of an em dash is gradually becoming more common, but it's still not very widespread in the US in professional publishing; so far (as of early 2016), it's mostly used in Canada and a couple of other places. For now, just use the em dash.

___

### **Colons instead of dashes in lists**

Another common but nonstandard construction is to use a hyphen surrounded by spaces to separate an item and its description. Instead, use an HTML [description list](https://developers.google.com/style/lists.html) (`<dl>`) or, in some cases, a colon.

#### **Examples**

!!! failure "Not Recommended" 
    `example - This is an example.`

!!! success "Better"  
    `example: This is an example.`

!!! success "Recommended" 
    for a series of items:
``` html
  <dl>
    <dt>example</dt>
    <dd>This is an example.</dd>
    <dt>another example</dt>
    <dd>This is another example.</dd>
  </dl>
```

!!! failure "Not Recommended" 
    Appendix A - My First Appendix

!!! success "Recommended" 
    Appendix A: My First Appendix