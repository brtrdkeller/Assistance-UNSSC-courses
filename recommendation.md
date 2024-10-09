---
title: Technicals Recommendations
nav_order: 99
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Home page 

**url:** <https://playground.unssc.org/>

### Skip links
 
The skiplink is referencing "#maincontent". But the "id" "maincontent" is apply is an empty `<div>` which is called `"user-notification"` in "page-outer". So users are going to an empty area.
The main content has been inserted in a `<section role="complementary">` region called `"block_unssctenantselector"`.

{: .highlight } The `id="maincontent` should be moved.

```
<section id="inst1194"
     class=" block_unssctenantselector block  card"
    `id="maincontent`
     data-block="unssctenantselector"
     data-instance-id="1194"
     aria-labelledby="instance-1194-header"
     >
</section>
```

### Heading

There isn't any `<h1>` in the page. Only a `<h4>` heading is present. Headings are not explicit.

{: .highlight } The heading hierachy has to be changed. We could have 2 titles `<h1>` and `<h2>`. Ex. "Welcome in a our learning home page" and "Choose a learning website"

## Main region

The `<section>` has an attribute `aria-labelledby="instance-1194-header"`. It's calling the title inside the `<h5>` tag. Is it the be expected behaviour ?.


```
<section id="inst1194"
     class=" block_unssctenantselector block  card"
     role="complementary"
     data-block="unssctenantselector"
     data-instance-id="1194"
     aria-labelledby="instance-1194-header"
     >
    <div id="instance-1194-header" class="card-header block-header">
        <h5 class="card-title d-inline-block pr-2 h3">Tenant selector</h5>
    </div>
</section>
```

### Policies panel - links

"Continue" link is not an explicit text. The "closing link" contains the value : "X". 

{: .highlight } "Continue" link must be renamed. The closing button content should have a label (ex. `aria-label="Close"`).

### Policies panel - modal content

This panel contains some links which are opening modal box. 

{: .highlight } The modal's content is not well formated. Ex. Headings are missing.

### Choosing Website Component - Images

Image tag are calling an "svg" images. Without image alternative text.

{: .highlight }  Parameters should be added, as : `alt=""` and `role="image"`.

### Choosing Website Component - Link

Text should better describe the purpose of a link. 

Link's text should contains the name of the website linked. MAdd a text before the link with the description of the website.

### Footer landmark

The `<footer>` landmark precise any `role`.

{: .highlight } The `<footer>` landmark should have a `role=contentinfo`.

## Login page

**url:** <https://playground.unssc.org/login/>

### Looking for a different Site
 
Text should better describe the purpose. "Change site" doesn't describe the action enough.

{: .highlight } The link text should be "Change e-learning website" or "Find another e-learning website"

### Looking for a different Site Dialog box
 
User can select a button before validated the redirection in the dialog box. There is any vocal indication that the button is selected or not selected. 

{: .highlight } Item should be selectable with a vocal feedback.

## Main logo

The <alt> attribute value is "The blue line", whereas the text displayed in the logo is "United System Staff College".

## Moodle Privacy Policy page

**url:** <https://playground.unssc.org/admin/tool/policy/view.php?versionid=3&returnurl=https%3A%2F%2Fplayground.unssc.org%2Fadmin%2Ftool%2Fpolicy%2Findex.php>

### Validation

Any link in the header is functional, user is blocked if policies are not validated. Validation `<button>` are at the bottom of the page. A user may not understand he has to go at the bottom of the page validating Policies.

{: .highlight } One option is to put buttons could be on the top. An other option is to renamed the page. Ex. "Validate the Moodle Privacy Policy".

## Main Inside Template Recommendation

### Main banner

The main banner is declared as a `<nav>`. It should be a `<header>`

{: .highlight } Change the `<nav>` container for a `<header>` container for the main banner

### Landmark

When navigating on the interface, any Landmark presents a label. Landmark should have a label for a better navigation

{: .highlight } Add `aria-label` on landmark. Ex. `<header aria-label='Main'>`.

## Dashboard

**url:** <https://playground.unssc.org/my/>

### Skip links visibility
 
Skip links navigation is hidden (when focused) by the header region. 

{: .highlight } Modify the z-index of `.navbar .navbar-top` or `.sr-only-focusable:active, .sr-only-focusable:focus` in CSS code.

### Skip links region

Skip links ("Skip to the main content") redirects the "Activity Bookmarks" block. All the blocks before are skipped. 

### Home link Logo
 
The "home" link redirect to the main page (Dashboard). It should be explicit.

{: .highlight } Rename the image `alt` with a better text (Ex. Home + Name of the website). Or ignore image and had a text in the link with a `class="sr-only"`.

### Main Navigation

Links have a `tabindex=-1` attribute, except "Dashboard". All the other links, except "Dashboard", are ignored by a keyboard navigation.

### Learning Plan Block - Filters

In the filter Dropddown menu, the language filter is not focusable.

{: .note } Filters are accessible but are changing dynamicaly the content of the courses area. If filters are too complicated to use, it is possible to hide them. But users will have to navigate in all their courses. It can be a choice for avoiding blind users to loosing time.

{: .highlight } Add a `tabindex=0` attribute on the `<div>` tag.

```
<div class="dropdown-header icons-collapse-expand list-group-item d-flex align-items-center collapsed"
    data-toggle="collapse"
    data-target="#tags1"
    aria-expanded="false"
    aria-controls="tags1"
    tabindex="0"
>
    <span class="expanded-icon icon-no-margin">
        <i class="fa fa-chevron-down mr-2" aria-hidden="true"></i>
        <span class="sr-only">
            Collapse
        </span>
    </span>
    <span class="collapsed-icon icon-no-margin">
        <i class="fa fa-chevron-right mr-2" aria-hidden="true"></i>
        <span class="sr-only">
            Expand
        </span>
    </span>
    Language
</div>
```

### Learning Plan Block - Live Update 

The content of the block is dynamicaly updated when filters are activated. The update should be vocalized.

{: .highlight } An `aria-live` region should be add in the code for preventing users that content is updated.

```
<div data-region="course_list" class="lp-courses-wrap p-3 position-relative d-flex" aria-live="polite">
        <div class="nocourses text-center p-3 w-100 un-emptystate">
            <img class="icon " alt="" aria-hidden="true" src="https://playground.unssc.org/theme/image.php/synergycustom/block_learning_plan/1727084612/empty-state" />
            <h5>There are no courses to show</h5>
            <a href="https://playground.unssc.org/local/unssc_coursecatalogue/" type="button" data-action="view-all-courses-button" class="btn btn-sm btn-primary my-2">View catalogue</a>
        </div>
</div>
```

### Learning Plan Block - Bookmark Button

The "bookmark" button is not focusable. 

### Previously accessed block - Show more items Button

When the "Show more items" Button is clicked, the focused is lost. 

Recommendation: Focus should be on the first new displayed item.

## Ethics and Integrity in Procurement

**url:** <https://playground.unssc.org/course/view.php?id=104>

### Lesson block

NVDA (Windows/Firefox) don't read the text of the button for expanding the lesson content. `aria-label` is not read. "Narrator" reads text but don't inform anything about the state of the expandable zone.

### "Mark as done" button and Bookmark button

Any action button indicate a feedback after being triggered. 

{: .highlight } Creating an `alert` zone when a button is triggered. The action should be validated (in a dialog box) in the best case.
