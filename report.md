---
title: Accessibility Report
---

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Context

**Web Site URL:** <https://playground.unssc.org/>

**Date :** 22/09/2024

**Method and Tools used in evaluation:**
 - Wave accessibility checker, 
 - Paul J. Adam Bookmarks, 
 - NVDA, 
 - Color Contrast Analyzer (CCA),
 - Manual Testing.

{: .note }
> When the header receives focus, it lands on the 'Dashboard' button. To access other header buttons, users have to press the left and right arrow keys.
> 
> Although this does not fail any guidelines, to improve navigation, ensure all header buttons can be accessed using tab navigation, or provide a message when the 'Dashboard' button receives focus: 'To access the other buttons, press the left and right arrow keys.'

## Critical accessibility issue.

### Login Page 

**url:** [https://playground.unssc.org/login/index.php](https://playground.unssc.org/login/index.php)

 - **Color contrast issue** - The login button, 'Forgot Password? Link', and 'cookie notice link' do not meet the contrast ratio guideline of 4.5:1.

 - **Error Identification** - The error message is generic and does not provide specific details about the error. More descriptive error messages, such as 'Invalid username' or 'Invalid password,' would help users better understand the issue.

### Home Page 

**url:** <https://playground.unssc.org/](https://playground.unssc.org/)>

 - **Missing alt text** - The card behind The Blue line link, OCHA learn link and The Blue line link, Provide appropriate alt text for the images or mark them as decorative using alt="".

 - **Color contrast issue** - Choose your site heading does not meet the contrast ratio guideline of 4.5:1.
 - **Unlabeled Form Fields** - It should be made more explanatory and prominent to ensure users understand its purpose clearly, such as labeling it 'Close button.'

### Forgot Password Page 

**url:** [https://playground.unssc.org/login/forgot\_password.php](https://playground.unssc.org/login/forgot_password.php)

 - **Color contrast issue** - Search button under Search by username and search by Email, both search buttons does not meet the contrast ratio guideline of 4.5:1.

 - **Error Identification** - Only one error message appears on the screen: 'Enter either username or email address,' even when the user inputs an incorrect email or username, The error message should be specific about the error to help users understand the exact issue.

### Dashboard 

**url:** [https://playground.unssc.org/local/unssc\_coursecatalogue/?catalog\_category=0&page=1&perpage=9&lpfilters=](https://playground.unssc.org/local/unssc_coursecatalogue/?catalog_category=0&page=1&perpage=9&lpfilters=)

 - **Color contrast issue** - search button,  Grid view button, add course link, view all link, lesson 2,3,and 4 and email address at the bottom of the page does not meet the contrast ratio guideline of 4.5:1.
 - **Main Navigation (Tab index – 1 issue)** - The links are accessible using the right and left arrow keys. This suggestion was noted in both the Word report and the Excel report. For better navigation, all the main navigation items/tabs can be brought in tab order.
- **Element does not receive focus** - All elements should be focusable using the keyboard. The Bookmark button is not in tab order and the course progress info icon, such as 6% complete or 100% complete is not properly readable with screen reader.
- **Unlabeled Form Fields** – The combo box next to the Filters button doesn't have an accessible name.

### Course Catalogue 

**url:** <https://playground.unssc.org/local/unssc\_coursecatalogue/?catalog\_category=0&page=1&perpage=9&lpfilters=>

 - **Unlabeled Form Fields -** The combo box next to the grid view button and filter expand button are unlabeled

 - **Color contrast issue -** 2 search buttons, All catalog button, Grid view button, Load more results button and page number button does not meet the contrast ratio guideline of 4.5:1.

### My Learning 

**url:** [https://playground.unssc.org/my/courses.php#maincontent](https://playground.unssc.org/my/courses.php#maincontent)

 - **Color contrast issue** \- The search button and the course name link text do not meet the guideline criterion of a 4.5:1 contrast ratio.

### Best Value for Money

**url:** <https://playground.unssc.org/course/view.php?id=105>

 - **Missing alt text** - The image under 'We want to hear from you!' does not have alt text.

 - **Color contrast issue -** search button, Grid view button, Bookmark button, all link and text under "Course contacts" heading and all other link with light blue color as there link text does not meet the contrast ratio guideline of 4.5:1.

### Ethics and Integrity in Procurement 

**url:** [https://playground.unssc.org/course/view.php?id=104](https://playground.unssc.org/course/view.php?id=104)>

 - **Color contrast issue -** search buttons and Procurement Training link does not meet the contrast ratio guideline of 4.5:1.

### Profile Page

**url:** <https://playground.unssc.org/user/profile.php#sb-5>

 - **Missing alt text** - Images under Community Updates heading do not have an alt text.

 - **Color contrast issue -** search button, View button under Upcoming events heading, Download the mobile app button, download button under My Certificates heading and view all links does not meet the contrast ratio guideline of 4.5:1.

## Less Critical Accessibility issue.

### Home Page 

**url:** [https://playground.unssc.org/](https://playground.unssc.org/)

 - **Heading Hierarchy -**  The 'Choose Your Site' heading is marked as H4, but since it is the only heading on the page, it should be marked as H1.

 - **Bypass block -** There is a 'Skip to Main Content' link on the page, but the focus does not shift anywhere. The screen reader only announces 'content region,' and upon tabbing again, the focus returns to the 'Skip to Main Content' link

### Dashboard 

**url:** [https://playground.unssc.org/local/unssc\_coursecatalogue/?catalog\_category=0&page=1&perpage=9&lpfilters=](https://playground.unssc.org/local/unssc_coursecatalogue/?catalog_category=0&page=1&perpage=9&lpfilters=)

 - **Heading Hierarchy -** The heading hierarchy is broken, with an H5 appearing immediately after an H1 on the page, Mark the headings in a hierarchical order from H1 to H6 without skipping levels, ensuring that H1 is only used to convey the meaning or purpose of the page.

### Course Catalogue 

**url:** [https://playground.unssc.org/local/unssc\_coursecatalogue/?catalog\_category=0&page=1&perpage=9&lpfilters=](https://playground.unssc.org/local/unssc_coursecatalogue/?catalog_category=0&page=1&perpage=9&lpfilters=)

 - **Reflow -** After zooming to 300%, the page starts to flow in two dimensions.

 - **Best Value for Money -** https://playground.unssc.org/course/view.php?id=105

 - **Heading Hierarchy -** The heading hierarchy is broken, with an H3 appearing immediately after an H1 on the page.

### Ethics and Integrity in Procurement 

**url:** [https://playground.unssc.org/course/view.php?id=104](https://playground.unssc.org/course/view.php?id=104)

 - **Heading Hierarchy -** The heading hierarchy is broken, with an H3 appearing immediately after an H1 on the page

### Profile Page 

**url:** <https://playground.unssc.org/user/profile.php#sb-5>

 - **Heading Hierarchy -** The heading hierarchy is broken; the first heading on the page is marked as H6, and H1 to H4 have not been used at all on the page.
 - **“Mark as done” button and Bookmark button** - The status of the button’s changes but because the screen reader focus moves to top of page on pressing Spacebar or Enter key, the user is not getting confirmation of the action. The improvement required is that the screen reader focus should remain on the bookmark or done button when it is activated.

## Minor Accessibility Issue.

### Course Catalogue 

**url:** [https://playground.unssc.org/local/unssc\_coursecatalogue/?catalog\_category=0&page=1&perpage=9&lpfilters=](https://playground.unssc.org/local/unssc_coursecatalogue/?catalog_category=0&page=1&perpage=9&lpfilters=)

 - **Page Title -** The page does not have an appropriate title; it appears to be the same as the link of the page.

### Home Page

**url:** [https://playground.unssc.org/](https://playground.unssc.org/)

- **Policies panel - modal content** - The box appears as a pop-up window, and all the links are accessible using Tab navigation, as well as the up and down arrow keys. They can also be activated with the spacebar. The section/topic can be given a heading style, although not critical