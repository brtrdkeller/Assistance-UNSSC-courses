---
title: Technicals Recommandations
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Home page - <https://playground.unssc.org/>

### Skip links
 
The skiplink is referencing "#maincontent". But the "id" "maincontent" is apply is an empty `<div>` which is called `"user-notification"` in "page-outer". So users are going nowhere.
The main content has been inserted in a "complementary" region called `"header-fullwidthblocks-wrap"`.

**Recommandation**: Maybe the component "tenant selector" should be moved in the good place.

### Heading

There isn't any `<h1>` in the page. Only a `<h4>` heading is present. Headings are not explicits.

**Recommandation**: The heading hierachy has to be changed. We could have 2 titles. Ex. "Welcome in a our learning platform" and "Choose a learning platform"

### Policies panel - links

"Continue" link is not an explicit text. The "closing link" contains the value : "X". 

**Recommandation**: "Continue" link must be renamed. The closing button content should have a label (ex. `aria-label="Close"`).

### Policies panel - modal content

This panel contains some links which are opening modal box. 

**Recommandation**: The modal's content is not well formated. Ex. Headings are missing.

### Choosing Website Component - Images

Image tag are calling "svg" images. Without image alternative text.

**Recommandation**:  Parameters should be added, as : `alt=""` and `role="image"`.

### Choosing Website Component - Link

Text should better describe the purpose of a link. 

Link's text should contains the name of the website linked. Maybe add a text before the link with the description of the website.

## Main Template Recommandation

### Main banner

The main banner is declared as a `<nav>`. It should be a `<header>`

**Recommandation**: Change the `<nav>` container for a `<header>` container for the main banner

### Landmark

When navigating on the interface, any Landmark presents a label. Landmark should have a label for a better navigation

**Recommandation**: Add `aria-label` on landmark. Ex. `<header aria-label='Main'>`.

## Dashboard - <https://playground.unssc.org/my/>

### Skip links visibility
 
Skip links navigation is hidden (whend focused) by the header region. 

**Recommandation**: Modify the z-index of `.navbar .navbar-top` or `.sr-only-focusable:active, .sr-only-focusable:focus` in CSS code.

### Skip links region

Skip links redirects the "Activity Bookmarks" block. All the blocks before are skipped. 

### Home link
 
The "home" link redirect to the main page (Dashboard). It should be explicit.

**Recommandation**: Rename the image `alt` with a better text (Ex. Home + Name og the website). Or ignore image and had a text in the link with a `class="sr-only"`.

### Main Navigation

Links have a `tabindex=-1`, except "Dashboard". All the other links than "Dashboard" are ignored by a keyboard navigation.

### Learning Plan Block

The "bookmark" button is not focusable. 

## Ethics and Integrity in Procurement <https://playground.unssc.org/course/view.php?id=104>

### Lesson block

NVDA (Windows/Firefox) don't read the text of the button for expanding the lesson content. `aria-label` is not read. "Narrator" read text but don't teel anything about the state of the expandable zone.

### "Mark as done" button and Bookmark button

Any action button doesn't indicate a feedback after being triggered. 

**Recommandation**: Creating an `alert` zone when a button is triggered. The action should be validated in the best case.


