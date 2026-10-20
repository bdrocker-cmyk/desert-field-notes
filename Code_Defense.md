Code Defense:
C4
Symptom: Featured card displayed yellow background instead of green background defined by reusable featured class
Cause:#featured-card ID selector had higher specificity than featured class selector. Causing the the background selector to take over the class style.
Correction: removed the #featured-card CSS rule, allowing featured class to take control of background
Evidence:https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Cascade/Specificity
Verification: After taking out the rule, the featured card changed from yellow to green, verifying the proposed issue and allowing background control.