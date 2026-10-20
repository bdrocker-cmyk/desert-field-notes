I1
Target and symptom: No language in HTML 
Cause: The original HTML root was just HTML without the lang attribute
Correction: <html> was changed to <html lang="en">
Evidence: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/lang also NU HTML validator
Verification: Initial test was notice of no lang attribute in code, second verification was check of elements tab with webpage.
I2
Target and symptom: There was no viewpoint tag set 
Cause: There was no viewport element assigned to the html
Correction: added additional line under the meta charset and it was <meta name="viewport" content="width=device-width" />
Evidence:Nu HTML Validator (https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/meta/name/viewport) 
Verification: Opened hmtl in browser and changed to device width automatically
I3
Target and symptom: the index html link on line 15 was not linked
Cause: the original line said "resource.html" while the page linked was for resources.html/ resource.html was also a page and had to be added as such in file path
Correction: Added the s to resources and saved the line/ referenced pages before resources.html
Evidence:(https://developer.mozilla.org/en-US/docs/Web/API/URL)
Verification: opened page in browser again and link to resources page opened
I4
Target and symptom: intro heading heirarchy was wrong  
Cause: Intro heading was H3 instead of H2 
Correction: changed h3 to h2
Evidence: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/header
Verification: inspected html structure and confirmed change
I5
Target and symptom: The image file description did not match the image depiction
Cause: the image description initially stated image123
Correction: Changed the text alternative to "Sand dune with cactus and sun."
Evidence: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/img
Verification: Saved line, re-opened in web browser, clicked picture and inspected the code.
R1
Target and symptom: The stylesheet path was incorrect due to no style popping up in resources page.
Cause: the stylesheet link was not rooted properly
Correction: Added "../css/styles.css"
Evidence: https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL
Verification: Re-opened in browser, webpage was expanded and style referencing was off.
R2
Target and symptom: similarly to stylesheet path, path was incorrect for home link
Cause: home link path was <li><a href="index.html">Home</a></li>
Correction: added "../" before the index.html on that line
Evidence: https://developer.mozilla.org/en-US/docs/Learn_web_development/Howto/Web_mechanics/What_is_a_URL
Verification: Re-opened resources page in browser and attempted to go to home( successful)
C1
Target and symptom: the website had no outline around tabbing for visual effect
Cause: the focus line had an outline of none
Correction: added a:focus-visible with a 3px solid blue line
Evidence: https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Selectors/:focus-visible
Verification: Re-opened in browser, webpage showed blue border around tabbing areas/links
C2
Target and symptom: Page cut off additional tabs when shrinking size of window
Cause: width percentage not added
Correction: Added width 100% to allow size adjustments as window expands/shrinks
Evidencehttps://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/width
Verification: Re-opened in browser, webpage was expanded and when shrinking the sizing adjusted to fit all tabs
C3
Target and symptom: cards grid was using a fixed column width, not allowing movement/shrinking properly 
Cause: grid-template-columns: repeat(3, 360px) caused display to be fixed no matter window size
Correction: Added changed to repeat(auto-fit, minmax(min(100%,250px), 1fr));
Evidence: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Grids "As many columns as will fit"
Verification: Re-opened in browser, webpage adjusted to different sizes with no overflow
C4
Target and symptom: The cards background color wasnt showing the reusable color class
Cause: featured ID selector was higher specificity than original class selector
Correction: removed featured-card css rule
Evidence: https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade/Specificity
Verification: Re-opened in browser, webpage card changed from yellow to green.
C5
Target and symptom: repsonsive media wasnt responding at smaller screen width
Cause: media required a minimum of 700px and max of 500px at the same time which isnt possible
Correction: changed media tab to (max-width: 700px)
Evidence: https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Media_queries/Using
Verification: Re-opened in browser, used developer tools to test page at 600px viewport width, header changed to vertical layout and navigation appeard below the title


Code Defense:
C4
Symptom: Featured card displayed yellow background instead of green background defined by reusable featured class
Cause:#featured-card ID selector had higher selectivity than featured class selector. Causing the the background selector to take over the class style.
Correction: removed the #featured-card CSS rule, allowing featured class to take control of background
Evidence:https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade/Specificity
Verification: After taking out the rule, the featured card changed from yellow to green, verifying the proposed issue and allowing background control.
