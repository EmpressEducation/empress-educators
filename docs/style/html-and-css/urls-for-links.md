# **URLs in links**

!!! Summary 
    For same-server links, use site-root-relative URLs.

___

### **URLs in links to pages on the same server**

When you're linking to another page on the same server, use a site-root-relative URL starting with `/`, even if you're linking to a page in the same directory as the page you're linking from.

**Note**: There are many valid linking styles; this guideline isn't a general statement about best practices for linking in all contexts, it's just our house style.

___

### **Use "https" when possible**

When you're linking to a page on another server (and therefore using an absolute URL), and the server you're linking to supports HTTPS, start the URL with `https` rather than `http`. If the server doesn't support HTTPS, then start the URL with `http`.