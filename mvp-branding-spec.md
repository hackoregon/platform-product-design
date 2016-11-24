## Feature: Branding

This aims to address a problem with Hack Oregon branding. Visitors to the Hack Oregon website will be met with consistent branding, and volunteers working on Hack Oregon projects will be provided with branding style guides and templates.

### Overview

#### Problem

1. **No consistent branding:** Hack Oregon does not have recognizable branding.
2. **No branding guidelines:** volunteers do not have branding style guides to use when designing websites for Hack Oregon which adds to the problem.

- _How was branding done in the past? Good/Bad/Lessons learned?_

#### Goals

1. **Increase brand awareness:** current brand awareness tests at X%. Increase this to Y%.
2. **Increase volunteer guidance:** X% of time worked on project was wasted in branding.
3. **Keep the website content simple:** avoid data stories as this will come later.
4. **Launch by XX:** UI work depends on branding to be established.

#### Out of Scope

1. **Platform/Backend/API/Data Science:** the website does not require any heavy lifting - there are no data visualizations planned in this iteration.
2. **Internationalization:** restrict to English/US for now.

### Context

#### Use Cases

1. **Volunteers want to:**
  1. **Avoid wasting time on branding decisions:** X% of time spent on project work was wasted in branding.
2. **Hack Oregon wants to:**
  1. **Have better brand recognition:** current brand awareness is at X%, but a similar non-profit has a brand awareness of Y%.
  2. **Get more people involved:** there are currently 200 volunteers at Hack Oregon. Hack Oregon wants to double this to 400 in one year.
  3. **Have consistent branding across platforms:** mobile and desktop experience should be consistent and tailored to fit the form-factor.

#### Assumptions

1. **Need 30 days to run a test to check if brand awareness was increased:** launch on XX. Results available by YY, 2017.
2. **Need 4 weeks to run a test to check if volunteer time spent in branding is reduced:** volunteers meet about twice a week for 3 hours. This provides us with 8 sessions (24 hours) per volunteer to determine whether we saved them (branding) time.

### Proposal

#### Website

We design a simple appealing website, using the branding style guide, that provides history, and information on Hack Oregon. The website also provides information on how people can get involved.

#### Navigation Model

The website has the following pages with corresponding controls/elements:

| Page | Description | Control/Element |
| --- | --- | --- |
| Home | Landing page which contains stories.  For now, how about we feature &quot;Cat&#39;s blog&quot;? We need a voice to connect with the community | Logo |
| About | History/More information/How to get involved. | Button |

These controls/elements are available on all pages.

- _Should we surface a &quot;Donate&quot; button under &quot;About&quot;? Donate time/money/expertise?_
- _Should we surface a &quot;Like Us&quot; button to help spread the word?_

#### UX

1. **Hack Oregon Logo:** top-left corner of all pages. Clicking this takes you to the main page.
2. **About button:** top-right corner of all pages. Clicking this takes you to the About page.
3. **Viewing website/pages:** all navigation paths take users through consistent branding experiences. Hack Oregon branding should be prominent and easily recognizable.
4. **Templates:** maintain an easily discoverable, organized, well labeled, and usable collection of branding templates for core pages. Naming convention: t\_brand\_page\_core\_&lt;optional notes|description|revision&gt;
  1. t\_brand\_page\_core: this is a branding template for a core page.
  2. &lt;optional notes|description|revision&gt;: to allow creating various flavors of branding templates.
5. **Template style guide:** documentation guide on how to apply a template. This guide should be simple (3 easy steps) and contain the following information:
  1. Which template to use and where to find it.
  2. How to apply it to what you&#39;re doing.
  3. How to verify that it was applied correctly.

#### Testing

1. **Volunteer A/B for templates/guides:** get help from volunteers to run A/B tests (with/without templates, with/without guides).

#### Metrics and Reports

1. **Volunteer surveys:** collect and present information from A/B testing.
2. **Logging:**
  1. **Time on website:** log the amount of time a person spends on the Hack Oregon website. _Can we filter out Hack Oregon staff/volunteers?_
3. **Reports:**
  1. **Engagement:**
    1. **Website traffic:** _Can we filter out Hack Oregon staff/volunteers?_
    2. **Time on website:** _Can we filter out Hack Oregon staff/volunteers?_
  2. **Memory:** website/pages memory profile (https://developer.chrome.com/devtools/docs/heap-profiling)
  3. **Likes:** _if we feature a &quot;Like Us&quot; button then we can start measuring/reporting trends (rate, distribution of Likes)_

### Tasks and Timelines

1. **:** MVP spec review complete. Starting:

1.
  1. UX branding work (and focus group testing).
    1. Website and pages.
  2. Incorporating MVP spec feedback.
2. **:** spec is shared with tech leads. Starting:
  1. Tech leads work on standing up website:
    1. No branding.
    2. Home, and About pages have content.
3. **:** UX branding complete. Starting:
  1. UI branding templates/Usage guides (with feedback from volunteers).
  2. Report generation process (automated/manual with documentation)
4. **:** website work is complete. UI branding templates and usage guides are ready for use. Report generation is complete. Starting:
  1. Applying branding/chrome to website
5. **:** website branding/chrome complete. Starting:
  1. Fit/finish/bug fixes
6. **:** launch.
7. **:** sync up before Christmas. Any new tasks generated? Reports?
8. **:** sync up before NYE. Reports?
