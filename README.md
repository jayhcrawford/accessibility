# Accessibility For Web
My aim is to create a centralized place where resources and classes can be homogenized.

*please report broken links, and feel free to contribute*
## Resources and Practices

### Test with a screen reader
There are popular operations across screen readers. **macOS VoiceOver's Rotor (and others)** is an example of a popular feature that can increase rapidity of accessible web development. Understanding these operations will help you to understand your audience.
 - "alt" (alternative) text will be read by the screen reader... don't use it for SEO
 - using a div element with an onclick attribute where a button is appropriate negates the useful built-in features of the button element. This applies to many of the so-called **"semantic" HTML elements**. Checkboxes, inputs, textareas, and other elements **have built-in accessibility features.**
 - Utilize hidden elements to increase quality of life for screen reader users. HTML elements with the CSS class below will not render to the screen, but will be read by screen readers:

 ```
    .hidden_but_read_by_screenReader {
        position: absolute;
        left: -10000px; /* Or a large negative value */
        top: auto;
        width: 1px;
        height: 1px;
        overflow: hidden;
    }
 ```
 - Navigate to your favorite social media platform, or web app and press <kbd>Shift</kbd> + <kbd>?</kbd>; this will likely open a panel of shortcuts that create a rich experience for sight-impaired people. The existence of this panel is revealed by screen readers using a hidden element with a CSS style like above. Storing the fact that it's been revealed to the user in localStorage will prevent repetitive experiences for screen reader users.

 ### Manage focus and tabbing
  - Tab trapping is the practice of ensuring that the users tapping experience does not send them out of the webpage and into the browser's control bar--if this would be beneficial. By using conditionals in elements like modals, the tab experience can be "trapped" into the modal.


### Understand ARIA labels and roles
 - ARIA provides the tools and techniques necessary to meet accessibility goals/standards
 - [ARIA attributes list at MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes)


### Test with Developer Tools
 - [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview) is built-in to Chrome and [Lighthouse CI](https://github.com/GoogleChrome/lighthouse-ci) for pipeline integration
 - [WAVE](https://wave.webaim.org/) by WebAIM
 - [axe DevTools](https://chromewebstore.google.com/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd?hl=en-US&pli=1) catch issues while developing
 - [Contrast Accessibility with Chrome DevTools](https://developer.chrome.com/docs/devtools/accessibility/contrast)
 - [Axe-core by Deque](https://github.com/dequelabs/axe-core) accessibility testing engine for websites and other HTML-based user interfaces; CI/CD integration

 ### Authoring Tools
**Linters**
 - [eslint-plugin-jsx-a11y](https://www.npmjs.com/package/eslint-plugin-jsx-a11y) Static AST checker for accessibility rules on JSX elements
 - [Angular codelyzer](https://www.npmjs.com/package/codelyzer) static code analysis of Angular TypeScript projects
 - [eslint-plugin-vuejs-accessibility](https://www.npmjs.com/package/eslint-plugin-vuejs-accessibility) eslint plugin for checking accessibility within .vue files

 **Accessible Design Systems**
 - [Adobe's React Spectrum](https://react-spectrum.adobe.com/react-spectrum/index.html)
 - [Google's Material Design](https://m3.material.io/)




 ## Laws, Organizations, and Guidelines
 - [The Americans with Disabilities Act (ADA)](https://www.ada.gov/#:~:text=The%20Americans%20with%20Disabilities%20Act%20(ADA)%20protects%20people%20with%20disabilities,many%20areas%20of%20public%20life.) protects people with disabilities from discrimination

 - [WAI-ARIA Overview](https://www.w3.org/WAI/standards-guidelines/aria/) (Web Accessibility Initiative - Accessible Rich Internet Applications) [ARIA attributes list at MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes)

 - [WCAG](https://www.wcag.com/) (Web Content Accessibility Guidelines) and [WCAG Techniques](https://www.w3.org/TR/WCAG20-TECHS/)

 - [Section 508](https://www.section508.gov/) Section 508 of the Rehabilitation Act of 1973 mandates that federal agencies ensure their information and communication technology is accessible to people with disabilities

 - [Deque University](https://dequeuniversity.com/) paid training and certification

 - [Microsoft Inclusive Design](https://inclusive.microsoft.design/) 