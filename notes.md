# Accessibility in Javascript Applications

- https://marcysutton.github.io/js-a11y-workshop/
- https://marcysutton.github.io/js-a11y-workshop/slides/
- https://github.com/marcysutton/js-a11y-workshop
- Prototyping without React using Parcel - https://github.com/marcysutton/parcel-prototype-scaffold
- Could also use CodePen and CodeSandbox for rapid prototyping

## Overview

- Accessibility - making the web more inclusive _with_ and _for_ people with disabilities.
- MS a11y toolkit - file:///Users/josephcastle/Desktop/inclusive_toolkit_manual_final.pdf
- JS apps
  - Client rendered - no traditional page reloads
  - Built with frameworks - React, Vue, Ember, Angular, etc.
  - Sometimes server-rendered with “hydration”
  - Challenges and opportunities
- Responsive design is good for accessibility - built for mobile, have viewports

## Debugging Accessibility

- A11y debugging steps

  - Render in a web browser - see how CSS & markup affect site in browser
  - Test controls with the keyboard - interactive items, not all elements need this
  - Use accessibility web extensions - chrome extensions
  - Check color contrast - number one problem on the web
  - Test with screen readers - better to do user testing on this, can use for basic testing
  - Use magnification & zoom - lot of low vision users, check experience

- Debugging examples

  - Anchors with lack of href will make it not tab-able
  - Use axe in Chrome Dev Tools - focus on violations first, others nice to have and may be subjective
  - Use function + command + F5 to use Chrome voice over

- Hidden vs. Visible CSS

  - .visually-hidden {border: 0;
    clip: rect(0 0 0 0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px;}
  - .opacity {opacity: 0;}
  - .displayNone {display: none;}
  - .visibility {visibility: hidden;}

- Accessibility Tree - chrome://accessibility

- Currently focused element - type into console and click on page - helps to find elements you can't see on focus
  document.body.addEventListener('focusin', (event) => {
  console.log(document.activeElement)
  })

- Contrast shown in color picker in Elements/Style

- ARIA Landmarks - https://www.w3.org/TR/wai-aria-practices/examples/landmarks/index.html
