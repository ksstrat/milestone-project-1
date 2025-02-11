## Table of Contents
* [**Testing Druing Development**](#testing-during-development)
    * [*Manual Testing*](#manual-testing)
    * [*Bugs and Fixes*](#bugs-and-fixes)
* [**Post Development Testing**](#post-development-testing)
  * [**Validators**](#validators)
      * [*HTML*](#html---httpsvalidatorw3orgnu)
      * [*CSS*](#css---httpsjigsaww3orgcss-validator)
  * [**Lighthouse Scores**](#lighthouse-scores)
      * [*Desktop Version:*](#desktop-version)
      * [*Mobile Version*](#mobile-version)
  * [**Accessability**](#accessability)

## **Testing During Development**
While developing, I've manually tested using the following methods:

1. I manually tested each element for appearance and responsiveness by using a VSCode extension called 'Live Server' to start a local server and then testing my project mainly in the Chrome browser.
    
2. I published the page using GitHub pages and shared the link with friends, including many developers, to test and get feedback.

### ***Manual Testing:***
* To ensure cross-compatibility, I tested the project on four different browsers. The desktop browsers I utilized included:

  1. Chrome
  2. Firefox  
  3. Vivaldi
  4. Safari

* I utilized the browser's developer tools to simulate various screen sizes and devices, ranging from mobile (320 px in width) to Ultra Wide Screens (4000 px in width)." 
* I also asked several people with different android and iphone mobile phones to test the site as well.

### ***Bugs and Fixes:***

During the development process, I identified the following bugs through manual testing:

1. **Intended Outcome** - 
    * ***Issue Found:*** 
        * 
    * ***Solution Used:*** 
        * 

    
## **Post Development Testing**
### **Validators**

#### ***HTML*** - https://validator.w3.org/
***

#### ***index.html***

* No error or warning was found during the validation of index.html. However, there was a "Info" that was also displayed on all my other pages:

![Validation Info Message](docs/screenshots/validation_indexhtml_info.png)

* I couldn't remember setting a slash for elements without a closing tag. After a quick check, I found out that the VSCode extension Prettier, which I had used to quickly format the hmtl code, sets this slash.
* I then removed the slashes in elements without a closing tag on all pages.

#### ***tours.html***

* No error or warning was found during the validation of tours.html

#### ***booking.html***

* No error or warning was found during the validation of booking.html

#### ***success.html***

* No error or warning was found during the validation of success.html

#### ***404.html***

* No error was found during the validation of 404.html

* *Warning Found*

     ![Validation Warning Message](docs/screenshots/validation_404html_warning.png)

* *Solution*
    * Changed the section to div because no structure or heading was needed and the only content was an image

### ***CSS*** - https://jigsaw.w3.org/css-validator/
***

* No error was found during the validation of style.css

* *Warning Found*

    ![Validation Warning Message](docs/screenshots/validation_stylecss_warnings.png)

* All three warnings were directly related to the use of Google Fonts.
* Since these imported style sheets are not checked by the w3c css validator, it issues a warning.
* No change is required here.

### **Lighthouse Scores**
***
### **Test conditions**
* All of the Lighthouse tests were run in the Chrome browser using the developer tools in incognito mode.
* Both desktop and mobile tests were conducted
 
#### ***Desktop Version:***
***

* The Lighthouse Score for desktops regarding "Accessibility", "Best Practices" and "SEO" is for all Pages 100 or near 100.

#### ***index.html***

![index.html Desktop Lighthouse Score](docs/screenshots/lh_desktop_indexhtml_score.png)

#### ***tours.html***

![tours.html Lighthouse Score](docs/screenshots/lh_desktop_tourshtml_score.png)

#### ***booking.html***

![booking.html Lighthouse Score](docs/screenshots/lh_desktop_bookinghtml_score.png)

#### ***success.html***

![success.html Lighthouse Score](docs/screenshots/lh_desktop_successhtml_score.png)

#### ***404.html***

![404.html Lighthouse Score](docs/screenshots/lh_desktop_404html_score.png)

#### ***Mobile Version:***
***

* The Lighthouse score for mobile regarding "Accessibility", "Best Practices" and "SEO" is for all Pages 100 or near 100.
* There are some differences in the performance score between the sites. I will discuss these below.

#### ***index.html***

![index.html Mobile Lighthouse Score](docs/screenshots/lh_mobile_indexhtml_score.png)

#### ***tours.html***

![tours.html Mobile Lighthouse Score](docs/screenshots/lh_mobile_tourshtml_score.png)

#### ***booking.html***

![booking.html Mobile Lighthouse Score](docs/screenshots/lh_mobile_bookinghtml_score.png)

#### ***success.html***

![success.html Mobile Lighthouse Score](docs/screenshots/lh_mobile_successhtml_score.png)

#### ***404.html***

![404.html Mobile Lighthouse Score](docs/screenshots/lh_mobile_404html_score.png)

### **Accessability**
