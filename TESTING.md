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
      * [*Lighthouse Score Feedback From Third Party Testers*](#lighthouse-score-feedback-from-third-party-testers)
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

1. **Intended Outcome** - A header with three evenly spaced out items across the header element.
    * ***Issue Found:*** 
        * Using float left and float right, I found the title stuck to the logo on the left despite using the clear command in the CSS .title selector.
    * ***Solution Used:*** 
        * Used CSS flex instead of float.

    
## **Post Development Testing**
### **Validators**

#### ***HTML*** - https://validator.w3.org/

#### index.html

* No error or warning was found during the validation of index.html. However, there was a "Info" that was also displayed on all my other pages:

![Validation Info Message](docs/screenshots/validation_indexhtml_info.png)

* I couldn't remember setting a slash for elements without a closing tag. After a quick check, I found out that the VSCode extension Prettier, which I had used to quickly format the hmtl code, sets this slash.
* I then removed the slashes in elements without a closing tag on all pages.

#### ***CSS*** - https://jigsaw.w3.org/css-validator/

* style.css tested, no issues found via direct input

![CSS validator badge]()

### **Lighthouse Scores**
### **Test conditions**
* I did all lighthouse tests in incognito mode to avoid interference from browser extensions. 
* I ran the tests for both mobile and desktop. 
 
#### ***Desktop Version:***

index.html

tours.html

booking.html

success.html

404.html

![Desktop Lighthouse Score](docs/screenshots/lighthouse-desktop.jpg) 

**There were several actions required to get to this score:**

1. The initial SEO score was 90 due to having no Meta description tag in the page head. Once I added this, the score became 100.

1. The best practice score was first 93 and impacted by three factors:
    * Aspect ratio of the images on the teachings page. I fixed this by resizing the images proportionately with the calculator found on https://andrew.hedges.name/experiments/aspect_ratio/.

    * There were some anchor tags on the community page and the form feedback page where the contained text was "here". I changed these anchor texts to a more descriptive text indicating where the links would lead the user.

    * The graphic used as an anchor to download the book Modern Buddhism on index.html was the correct size with no need to specify width and height. However, the best practice scored suggested it should have a height and width specified. I used an extension called pesticide to get the dimension of the image and added these to the CSS file under an ID explicitly created for this element (#modbudd-ebook). Once I added the dimensions best practice score became 100.

1. The performance was 93 on the form feedback page but fluctuating around 93 each time I ran the test. I used https://tinypng.com/ to compress the hero image on this page, which took the score to a minimum of 95 or higher each time I ran the lighthouse test.

#### ***Mobile Version:***

* Due to the more significant variance in the performance score, I have included a screenshot for each mobile page. That being said when I asked one of my testers to check the mobile light house scores from his device his performance scores were all the high nineties.

1. ***index.html:***

    ![Mobile Lighthouse Score for index.html](docs/screenshots/lighthouse-mobile-indx.jpg) 

    * Originally, the performance score on the page was around 83. By using a slightly smaller version of the same hero image, I resolved the issue and maintained the responsiveness up to 4000 px in width.

2. ***teaching:***

    ![Mobile Lighthouse Score for teachings.html](docs/screenshots/lighthouse-mobile-teach.JPG)

3. ***community.html:***

    ![Mobile Lighthouse Score for community.html](docs/screenshots/lighthouse-mobile-comm.JPG) 

4. ***Contact.html:***

    ![Mobile Lighthouse Score for teachings.html](docs/screenshots/lighthouse-mobile-contact.jpg)

    * Best practice score has initially been 98 due to the spacing of the mailing list radio buttons. I added a padding bottom to the top div encasing the first input and label, which solved the issue.
    * The performance score is lower on this mobile page due to the hero image. I already compressed the image twice, which had little impact on the score, and unfortunately, there was no more petite version of the image available. To resolve this in the future, I intend to use GIMP to resize an image. However, it was not a viable solution for this project due to the time already spent on the project, and given I would need to learn GIMP from scratch. 

5.  ***form-feedback.html***

    ![Mobile Lighthouse Score for form-feedback.html](docs/screenshots/lighthouse-mobile-feedback.jpg) 
    * I found the performance score on this page lower due to the embedded video. I discovered this by looking at the original trace in the browser dev tools and saw the pages hero image and content loaded quickly. To test this theory, I removed the link from the iframe, and sure enough, the score increased a few points.

#### ***Lighthouse score Feedback From Third Party Testers***
On the whole all scores reported back from third party testers using the lighthouse tool concurred with my own. One interesting thing that was reported back to me was the following when tested outside of Incognito mode: -
  * The best practice score on the pages with a video embedded dropped to 93 due to a console error. 
    * I was able to replicate this to see the error specified that the set:cookie property on the embedded video was being set automatically by the browser to "lax" due to not being specified in my code. 
    * I reduced this error by using "no-cookie" in the youtube URL. However, I was unable to get rid of it outside of incognito mode completely. This error did not show at all in incognito mode.
    * All documentation found on the set:cookie attribute pointed towards Javascript/API, which was outside of my current knowledge base and the scope requirements for this project. 
    * Since, in reality, the browser was only alerting me that by default, the attribute was now "lax" and there was no user impact, I decided that this was not a bug but a browser feature. This is something I would be looking to fix in the future by replacing the embed url with an API call.
  
### **Accessability**
In addition to the accessability score on light house I also used [WAVE - Web accessability evaluation tool](https://wave.webaim.org/) to check my pages for accessability and no errors were returned.
***   
[return to README.md](README.md)