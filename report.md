# Accessibility Report

## Home page

### 1. Skip links
 
The skiplink is referencing "#maincontent". But the "id" "maincontent" is apply is an empty `<div>` which is called `"user-notification"` in "page-outer". So users are going nowhere.
The main content has been inserted in complementary region called `"header-fullwidthblocks-wrap"`.

**Recommandation**: Maybe the compoenant "tenant selector" should be moved in the good place.

### 2. Heading

There isn't any `<h1>` in the page. Only a `<h4>` heading is present. Headings are not explicits.

**Recommandation**: The heading hierachy has to be changed. We could have 2 titles. Ex. "Welcome in a our learning platform" and "Choose a learning platform"

### 3. Policies panel - links

"Continue link" is not an explicit text. The "closing link" contains the value : "X". The closing button content should have a label (ex. `aria-label="Close"`).

### 4. Policies panel - modal content

This panel contains some links which are opening modal box. 

**Recommandation**: The modal's content is not well formated. Ex. Headings are missing.

### 5. Choosing Website Component - Images

Image tag are calling "svg" images. Without image alternative text.

**Recommandation**:  Parameters should be added, as : `alt=""` and `role="image"`.

### 6. Choosing Website Component - Images

Text should better describe the purpose of a link. 

Link's text should contains the name of the website linked. Maybe add a text before the link with the description of the website.
