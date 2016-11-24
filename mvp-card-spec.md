# Feature: Card

[Overview](#overview)

[Problem](#problem)

[Goals](#goals)

[Out of Scope](#out-of-scope)

[Context](#context)

[Use Cases](#use-cases)

[Assumptions](#assumptions)

[Proposal](#proposal)

[Card](#card)

[UX](#ux)

[Testing](#testing)

[Metrics and Reports](#metrics-and-reports)

[Tasks and Timelines](#tasks-and-timelines)

This aims to address problems with Hack Oregon engagement and brand recognition via interactive **things**. Visitors to the website will be able to engage with these branded, interactive things and spend more time on the site. Volunteers will be able to build these things easily. We call these things **Cards**.

- _Guidance/documentation/consistency/ease in tackling tasks can help maximize volunteer engagement, which is a win-win for volunteers and Hack Oregon._

### Overview

#### Problem

1. Content viewed on Hack Oregon&#39;s website does not connect the user to the Hack Oregon brand.
2. Users do not have a way to view the new branded content that Hack Oregon is planning to curate:
  1. Data and visualizations.
  2. Various types of media and text (copy).
  3. Context and metadata.
3. Volunteers do not have a way to easily and consistently create, and work with, this new branded content.

#### Goals

1. **Consistent branding and experience:** presentation of the content connects with the user, and follows Hack Oregon branding guidelines.
2. **Present content in a meaningful way to the user:** A/B test presentations.
3. **Increase engagement:** increase time spent by users on website by X%.

#### Out of Scope

1. **Platform/Backend/API/Data Science:** the work being done here does not require backend support.
2. **Internationalization:** restrict to English/US for now.

### Context

#### Use Cases

1. **Volunteers want to:**
  1. **Quickly and consistently create branded cards for Hack Oregon projects:** on average, X% of time spent on previous project work was wasted in creating new visualizations from scratch. Reduce this by Y% by facilitating easy creation of these cards using templates, and initializing them with defaults.
2. **Website visitors want to:**
  1. **Interact and engage with the content:** We have no previous metrics for visitors engaging with interactive content. We will start collecting information on user interactions with cards.

#### Assumptions

1. **Need 30 days to run a test to check if content interaction increases:** launch on XX. Results available by YY.
2. **We get city data in time:** sensitivity/process-related delays may prevent us from getting and cleaning Portland city data in time for the demo. If we don&#39;t receive and process data in time for the demo, the Data Science and Product leads should work together to come up with an alternative data story.

### Proposal

#### Card

This aims to address the need for a thing that can do all the following:

(These behaviors support multiple user flows. This does not mean that all behaviors will be used all the time. For example, a card with a copy/text asset may not have any associated metadata. However, the card should support storing metadata if the scenario requires it. Also, a copy/text card may support collecting user interaction information, but we may choose not to utilize this functionality.)

1. A card is an object populated with content of Hack Oregon&#39;s choosing
  1. Data (Visualization)
  2. Multimedia
  3. Copy/Text
2. Cards are connected to 1 or more data sources through a single API
3. Cards are defined as a certain type, accepting only the correct &quot;types&quot; of data
4. Cards contain metadata describing relevant attributes. Examples include:
  1. Tags, Description, Story Parent, Notes, Author, Type
5. Cards are branded to connect with the Hack Oregon brand
6. Cards can be standalone, or their state can be driven by a controller(s)
  1. The state of a card is the environment of data it is currently showing

#### UX

1. **Behavior:**
  1. A card must support Hack Oregon branding guidelines.
  2. A card must expose consistent methods to link to, or embed, an asset. The types of assets are:

| Type | Format | Visualization |
| --- | --- | --- |
| Audio | mp4 | player |
| Video | mp4, YouTube | player |
| Image | JPEG, PNG | image |
| Data | raw data, URL (API) | scatterplot, map, histogram |
| Copy/Text | style, size, color, effect |   |
| Controller |   | dropdown, slider |
| Interactive | _game, animation?_ | _?_ |

1.
  1.
    1. A card must expose consistent methods to indicate whether an asset/resource was correctly loaded, as well as expose methods to reload/retry in case of failure.
  2. A card must be of a specific type to link to a specific asset.
    1. _Why do we care about type? Let devs decide based on described behavior/complexity._
  3. A card must expose whether the asset passes a set of rules. A card may contain mechanisms to perform validation on the asset by running a set of rules. It is considered a PASS if no validation mechanisms are specified. Examples of rules:
    1. Rule: There are a correct number of parameters to perform the type of visualization requested.
    2. Rule: The YouTube link is invalid.
    3. Rule: The image URL was not found (returns HTTP 404).
  4. A card must expose consistent mechanisms to store, retrieve, and display information/metadata/custom tags about that asset.
  5. A card must support mechanisms to visualize and interact with an asset.
    1. The visualization mechanism should be able to, given some prior information, appropriately resize the visualization/viewport.
    2. The interaction mechanism should be able to alter the visualization, as well as send notifications of what changed to subscribed controllers.
  6. A card must provide consistent mechanisms to set the state, which may affect what is presented to the person viewing the card (e.g.: provide access to a common/subscribed controller that affects presentation/visualization, by driving state, or serving as a filter to constrain data, on a group or set of cards).
  7. A card must support sharing on facebook, twitter, and medium while maintaining Hack Oregon branding.
  8. A Hack Oregon card can be embedded in another website, which allows collaborators to reuse our cards with our branding.
    1. When a card is embedded in another website, it should behave exactly as if it were on the Hack Oregon website (e.g.: no broken relative URLs).
  9. A card must provide a means to collect user interaction information (such as clicks, or the number of, and which, interactive elements were manipulated).
    1. _Can we get engagement metrics when these cards are embedded on a collaborator&#39;s site? It would be great to know where we get the most eyeballs._
  10. A card must support grouping (collection). A group/collection can hold a number of cards, of any/mixed types (e.g.: [audio, audio, video, image], etc.).
2. **Templates:** maintain an easily discoverable, organized, well labeled, and usable collection of branding templates for cards. Naming convention: t\_brand\_&lt;type&gt;\_&lt;subtype&gt;\_&lt;optional notes|description|revision&gt;
  1. t\_brand: this is a branding template
  2. type: { page, card }
  3. subtype
    1. page: { core, hackoregonstory }
    2. card: { controller, text, image, audio, video, histogram, map, scatterplot }
  4. &lt;optional notes|description|revision&gt;: to allow creating various flavors of branding templates.
3. **Template style guide:** documentation guide on how to apply a template. This guide should be simple (3 easy steps) and contain the following information:
  1. Which template to use and where to find it.
  2. How to apply it to what you&#39;re doing.
  3. How to verify that it was applied correctly.
4. **Website:** Hack Oregon publishes two articles that each contain cards of all asset types in a cohesive narrative.

#### Testing

1. **Volunteer A/B for templates/guides:** get help from volunteers to run A/B tests (with/without templates, with/without guides).
2. **Website:** run focus group testing on which cards/visualizations to display.

#### Metrics and Reports

1. **Volunteer surveys:** collect and present information from A/B testing.
2. **Reports:**
  1. **Engagement:**
    1. **Card interaction:** _Can we filter out Hack Oregon staff/volunteers?_

### Tasks and Timelines

1. **:** MVP spec review complete. Starting:

1.
  1. UX branding work (and focus group testing).
    1. Data story
    2. Cards
  2. UX interactions:
    1. Citizen and website.
    2. Website and data story.
    3. Citizen and data story.
  3. Incorporating MVP spec feedback.
  4. Data Science and Product Leads work together to identify a data story to focus on.
2. **:** data story identified with basic spec is shared with dev team. Starting:
  1. **Card tech spec:** this quick spec should provide a basic idea of the card object, and, where detail has not been provided, briefly explain how desired behavior will be achieved. The data story can help guide specific parts of the spec.
  2. **Card mockups:** tech leads design some basic mockups to work with UX branding. The data story can help guide visualizations.
    1. Basic mockup needs to support branding, setting/updating state, displaying an image, and displaying some informational text.
  3. **Data story write-up:** work with the Data Science team to research and get a narrative in place (images of graphs/charts are fine as basic visualizations).
    1. Article/narrative with images
    2. Spec detailing Data Science methods used to create article
      1. _This will drive initial API design_
3. **:** tech spec review complete. Data story write-up complete. UX interactions complete. Starting:
  1. Dev team incorporating spec feedback.
  2. UX reviews data story and finalizes design.
4. **:** card mockups complete. Starting:
  1. UI branding templates/Usage guides (with feedback from volunteers).
  2. Report generation process (automated/manual with documentation).
5. **:** UI branding templates and usage guides are ready for use. Report generation is complete.
6. **:** data story write-up with basic visualizations, and branding is complete. Starting:
  1. Adding card functionality.
  2. Integrating data story write-up with website.
7. **:** launch.

1. **:** sync up before Christmas. Any new tasks generated? Reports?
2. **:** sync up before NYE. Reports?
3. **:** card functionality complete.
