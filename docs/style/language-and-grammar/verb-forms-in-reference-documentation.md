# **Verb forms in reference documentation**

!!! Summary 
    In reference docs describing a method, use the form "Creates foo" rather than "Create foo."

When you're writing reference documentation for a method, phrase the main method description in terms of what it does ("Gets," "Lists," "Creates," "Searches"), rather than what the developer would use it to do ("Get," "List," "Create," "Search").

It's a subtle distinction that manifests mostly in whether the initial verb in the description has an "-s" at the end or not.

#### **Examples**

!!! failure "Not Recommended" 
    tasks.insert: Create a new task on the specified task list.

!!! success "Recommended" 
    tasks.insert: Creates a new task on the specified task list.

In a specification that's aimed at *implementors* of an API, it may make more sense to use the verb form without the "-s"; in that context, you're telling the reader what their implementation of the method should do ("create a new task"), whereas in reference docs aimed at developers you're telling them what the existing method does ("creates a new task").