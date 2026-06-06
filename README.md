## Globetrotter

Submitted by: **Heartwill Gbekle**

Estimated time spent: **10** hours spent in total

Deployed Application (optional): [Globetrotter Deployed Site](https://heartwillgbekle.github.io/Globetrotter/)

### Application Features

#### CORE FEATURES

- [X] **Home Page**
  - [X] A heading that mentions the destination.
  - [X] An introductory paragraph that welcomes visitors and describes the purpose of the website. 
  - [X] An evocative image *or* other visual media (video, hero-video background, etc.) that represents the location.
  - [X] Content organized using Flexbox for a fluid layout.

- [X] **Top Attractions Page**
  - [X] A separate page featuring a minimum of three attractions, each including a:
    - [X] Name
    - [X] Photo
    - [X] Brief description
  - [X] Each attraction is styled the same
    - E.g. same font, image size, title size, etc. 
  - [X] Content arranged with Flexbox for consistency and responsiveness.

- [X] **Guide Page** *(build one guide page of the type you choose below)*
  - [X] A separate page that is *one* of the following: a Food Guide, an Accommodations Guide, *or* an Upcoming Local Events Guide.
  - [X] At least three entries thematic to your choice that provide a:
    - [X] Title
    - [X] Address
    - [X] Description
    - [X] Link with more information (e.g. link to a restaurant page)
  - [X] Each entry should be:
    - [X] Catered to a specific type of traveler (families, backpackers, etc.)
    - [X] Styled the same
      - E.g. same font, title size, etc.
  - [X] Content arranged with Flexbox for consistency and responsiveness. 

- [X] **Photo Gallery**
  - [X] Separate page with at least five images related to the site's topic.
  - [X] Each image should include a caption describing the image.
  - [X] Presented in a responsive design using Flexbox.

- [X] **Navigation Bar**
  - [X] Navigation bar with working links to each of the following pages:
    - [X] Home Page
    - [X] Top Attractions
    - [X] Photo Gallery
    - [X] Guide Page (Food Guide, Accommodations Guide, _or_ Upcoming Local Events Guide)
  - [X] Navigation bar can be accessed from each page of the website.
  - [X] Styled with Flexbox that adapts to different screen sizes.  

- [X] **Smartphone Friendly**
  - [X] A design that is fully functional and aesthetically pleasing on smartphones is achieved using media queries.

### Stretch Features

- [ ] **Additional Media**
  - [ ] Embed a piece of media that is not an image or text and relates to the travel content such as a:
    - Map
    - Video
    - Song

- [ ] **Enhanced Layouts**
  - [ ] Utilize CSS Grid on one or more pages for a unique layout.

- [X] **Interactive Navigation**
  - [X] Implement a dropdown menu where at least one menu item includes a nested dropdown menu to access additional categories or sub-pages.

- [X] **Travel Newsletter Form**
  - [X] Create a form to allow users to sign up for a travel newsletter, enhancing user engagement.
  - [X] *Note*: You do not have to collect and save the data submitted using the form. 

- [X] **Deployment**
  - [X] Deploy your website so it's accessible to the public outside of your local machine. 
  - [X] **VIDEO WALKTHROUGH SPECIAL INSTRUCTIONS:** For ease of grading, please film yourself using your deployed URL with the URL visible in your video. 

- [X] **Custom Styling**: Add a personal touch to your site's design.
  - [X] Integrate at least one custom font using Google Fonts to add personality to your site.
  - [X] Experiment with at least one CSS property not covered in the lessons or labs to customize your page further.

### Walkthrough Video
**Walkthrough video:** [Globetrotter Walkthrough](https://www.loom.com/share/9e723d6343b740d1b3eccc351832d93d)

### Reflection

* Did the topics discussed in your labs prepare you to complete the assignment? Be specific, which features in your weekly assignment did you feel unprepared to complete?

The labs provided a solid foundation for the core HTML structure and basic Flexbox layouts. The semantic HTML section was particularly useful for understanding when to use article, figure, and nav elements appropriately. However, I felt less prepared for some of the more complex Flexbox patterns, particularly:

- **Equal-height cards across rows**: The labs covered basic flex properties, but not the pattern of using flex: 1 on card bodies combined with flex-direction: column on the parent to create uniform card heights. I had to experiment and research this pattern independently.

- **Nested dropdown navigation**: While the labs covered basic navigation bars, implementing a CSS-only dropdown with nested menus required understanding positioning contexts and pseudo-classes in more depth than the labs provided. The hover state management for nested menus was particularly tricky.

- **Responsive design strategy**: The labs introduced media queries, but didn't cover the decision-making process of choosing between mobile-first vs desktop-first approaches, or how to determine appropriate breakpoint values. I had to research device viewport sizes and common breakpoint patterns independently.

- **Custom CSS properties beyond basics**: Properties like backdrop-filter and advanced gradient patterns weren't covered in labs, so implementing the Kente-inspired divider required external research and experimentation.

Overall, the labs gave me the vocabulary and basic patterns, but real-world implementation required a lot of independent problem-solving and research.

* If you had more time, what would you have done differently? Would you have added additional features? Changed the way your project responded to a particular event, etc.

**What I'd add:**
1. **Interactive map integration** — Embed a Google Maps or Mapbox map showing all attractions and food locations, with clickable markers that link to the relevant sections. This would help visitors visualize the city layout and plan their routes.

2. **Events calendar section** — Add a page featuring cultural events, festivals, and live music venues, especially highlighting "Detty December" (the annual diaspora homecoming celebration). This would make the site more useful for trip planning.

3. **CSS Grid for the gallery** — Convert the photo gallery from Flexbox to CSS Grid for more precise control over image placement and to create a true masonry layout with varying image sizes.

4. **Image optimization** — Replace all images with properly optimized WebP versions with responsive srcset attributes for different screen sizes. Currently, large images load at full resolution on mobile, which impacts performance.

5. **Accessibility improvements** — Add skip-to-content links, improve keyboard navigation through the dropdown menus, and test with actual screen readers to ensure the site is fully accessible.

**What I'd do differently:**
1. **Start with mobile-first CSS** — I wrote desktop styles first and added mobile overrides, which led to some redundant code. Mobile-first would have been cleaner and more maintainable.

2. **Plan the content pivot earlier** — I originally designed the Food Guide for restaurants, then switched to traditional dishes mid-project. If I'd done the content research before building the HTML structure, I could have avoided restructuring the page.

3. **Use CSS custom properties more strategically** — I removed all CSS variables for simplicity, but in retrospect, keeping variables for spacing values would have made responsive adjustments easier without sacrificing readability.

4. **Test on real devices sooner** — I relied on browser developer tools for responsive testing, but testing on actual phones and tablets would have caught layout issues earlier, particularly with the dropdown navigation on touch devices.

* Reflect on your project demo, what went well? Were there things that maybe didn't go as planned? Did you notice something that your peer did that you would like to try next time?

**What went well:**
- The design system felt cohesive and genuinely reflected Accra's identity. The Ghana flag colors and Kente-inspired divider immediately communicated the destination without being heavy-handed.
- The dropdown navigation worked smoothly and the nested menu pattern was intuitive. Reviewers appreciated the quick access to specific attractions.
- The decision to pivot from restaurants to traditional dishes paid off — the food guide became more educational and culturally authentic, which aligned better with the site's goal of going "beyond the tourist surface."

**What didn't go as planned:**
- The em dash removal was tedious and manual. I should have been more consistent with punctuation from the start rather than having to go back and fix it across all pages.
- I initially used a light blue color scheme before switching to green, which meant redoing all the color values. If I'd committed to the Ghana flag colors from the beginning (as planned in planning.md), I would have saved time.
- The dropdown menu doesn't work well on touch devices without JavaScript for click-to-open functionality. The CSS `:hover` solution works on desktop but isn't ideal for mobile — I should have considered this earlier.

**What I'd try next time:**
- I noticed peers using video backgrounds in their hero sections, which added a lot of visual interest without overwhelming the page. I'd like to experiment with subtle video or animated elements in future projects.
- Some projects had smooth scroll animations and transitions between sections that made navigation feel more polished. Learning how to implement `scroll-behavior: smooth` and intersection observer animations would enhance the user experience.
- I'd like to try implementing a light/dark mode toggle, which several peers included. It's a good exercise in CSS custom properties and state management, and it improves accessibility for users with different visual preferences.

### Open-source libraries used

- [Google Fonts - Playfair Display](https://fonts.google.com/specimen/Playfair+Display) - Custom serif font used for all headings to add editorial weight and sophistication

### Shout out

Give a shout out to somebody from your cohort that especially helped you during your project. This can be a fellow peer, instructor, TA, mentor, etc.

*Shout out to Mussie, Benny and Emmanuel*