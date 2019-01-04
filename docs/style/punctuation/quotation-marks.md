# **Quotation marks**

!!! Summary 
    Use straight double quotation marks and apostrophes.

___
### **Commas and periods with quotation marks**

Commas and periods go inside quotation marks, in the standard American style, despite it being inconsistent with the way things are done in code, and inconsistent with the standard British style.

#### **Examples**

!!! failure "British" 
    See the section titled "Care and feeding of the emu".

!!! success "American (and Google)" 
    See the section titled "Care and feeding of the emu."

**Exception:** When you put a keyword or other literal string in quotation marks, put any other punctuation outside the quotation marks. In those cases, the quotation marks indicate an exact literal string, so don't add anything extraneous inside the quotation marks. But in general, don't put quotation marks around an item that's in code font, unless the quotation marks are part of the item.

#### **Examples**

!!! failure "Not Recommended" 
    If you enter "foo," the program crashes.

!!! success "Better" 
    If you enter "foo", the program crashes.

!!! success "Recommended" 
    If you enter `foo`, the program crashes.

!!! note "Note" 
    Literal-minded tech people are often resistant to the American style, on the grounds that it's illogical. However, despite its illogic, the American style shows no sign of going away, even in technical publications; if you look at 100 books published by major American publishers (even technical books), chances are good that at least 99 of them use the American style. For example, in early 2017, recent O'Reilly and Apress books that we looked at still use the American style.

___

### **Straight and curly quotation marks**

Most typefaces support two forms of quotation marks and apostrophes: straight marks and "curly" or "typographic" marks. Some tools, like Google Docs, automatically convert straight quotation marks and apostrophes to the curly versions as you type. However, our guidance is to always use straight quotation marks and straight apostrophes, for these reasons:

-   It's easy to get the direction of curly quotation marks (especially apostrophes) wrong. Using straight marks avoids this problem.
-   Code *requires* straight marks.
-   Many writers use coding tools (for example, Subversion) for working directly with markup. Because these tools do not produce curly marks by default, the writer must manually insert the marks, which is error prone.

#### **Examples**

!!! failure "Not Recommended" 
    The section's title is "Care and feeding of the emu."

!!! success "Recommended" 
    The section's title is "Care and feeding of the emu."

___

### **Single quotation marks**

The only times to use single quotation marks in our documentation are the following:

-   In code examples, in languages that use single quotation marks.
-   When nesting a quotation inside another quotation.

In the latter case, put the primary speaker's quote in double quotation marks and the quote inside the primary speaker's quote in single quotation marks, in the standard American style. (This is opposite to the standard British style.)

#### **Examples**

!!! failure "British" 
    She said, 'I heard him shout "Help", and saw him floundering in the water.'

!!! success "American (and Google)" 
    She said, "I heard him shout 'Help,' and saw him floundering in the water."

!!! note "Note" 
    For information about how to use quotation marks with links, see [Punctuation with links](https://developers.google.com/style/link-text#punctuation-with-links).