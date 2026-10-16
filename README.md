# Digital Agency

## Project Overview

Digital Agency is a fictional digital and technology agency specializing in Web Development, UI/UX Design, Digital Consulting, and Digital Strategy. Its three-page website introduces the agency to businesses seeking a clearer online presence and practical support for digital projects.

This collaborative CSS assignment is prepared for the October 17, 2026 presentation. It follows the local [client assignment](AI-CSS%20Assignment.pdf), its landing-page reference, Roboto typography, and required palette: `#1F2937`, `#3882F6`, `#F9FAF8`, and `#E5E7EB`.

## Features

- **Home:** agency introduction, five original SVG illustrations, four expertise cards, an illustrative testimonial, and a contact CTA.
- **Services:** Web Development, UI/UX Design, and Digital Consulting descriptions, service lists, and a link to About & Contact.
- **About & Contact:** introduction, mission and vision, three values, responsive artwork, and a demonstration email link.
- Shared header, footer, and navigation connecting all three pages.
- CSS-only hamburger menu below 768px, controlled by a labeled checkbox.
- Responsive Flexbox layouts, media queries, semantic landmarks, and labeled sections.
- Named navigation, `aria-current="page"` on the current link, and `aria-controls` linking the menu checkbox to the navigation. On mobile, the checkbox remains keyboard-focusable and its visible label receives a focus indicator. Links also have visible focus styles.
- Descriptive alt text on Home illustrations; empty alt text on About's decorative artwork.

## Technologies

HTML5, vanilla CSS3, Flexbox, media queries, Roboto (imported from Google Fonts), original local SVGs, and Git/GitHub for version control and collaboration.

JavaScript, CSS Grid, Sass, frameworks, and additional CSS libraries are not used. No build tool or runtime installation is required.

## Project Structure

```text
digital-agency/
|-- AI-CSS Assignment.pdf
|-- README.md
|-- index.html
|-- services.html
|-- about.html
|-- css/
|   |-- base.css
|   |-- home.css
|   |-- services.css
|   |-- about.css
|   `-- navigation.css
`-- assets/
    `-- images/
        |-- about-workspace-desktop.svg
        |-- about-workspace-mobile.svg
        |-- home-team.svg
        |-- home-web-development.svg
        |-- home-ui-ux.svg
        |-- home-consulting.svg
        `-- home-strategy.svg
```

`base.css` provides shared typography, color variables, box sizing, links, and buttons. `navigation.css` styles the shared header, footer, and menu. Each page also loads its own stylesheet.

## Team Contributions

| Team member | Contributions and assignment history |
| --- | --- |
| **Hakim Salaues — Team Lead** | Project coordination; Home page; global styling; About & Contact page, completed after responsibilities were reassigned; final integration and documentation. |
| **Fadi Omer** | Services page; shared header, footer, and navigation; CSS-only hamburger menu. |
| **Lulamani Maluleka** | Initially assigned About & Contact and responsive images. Those responsibilities were reassigned; completed development work is not attributed to her here. |

## Responsive Design

Target viewport widths from the assignment are **375px** (mobile), **768px** (tablet), and **1200px or wider** (desktop).

Flexbox handles the main layouts and wrapping. Home cards use four columns at 1200px and above, two below 1200px, and one below 768px. Home's hero and CTA stack below 768px. About's hero and mission/vision panels also stack below 768px; its values and contact content wrap. Services cards wrap according to available width and explicitly stack at 600px and below. Shared navigation switches to the hamburger menu below 768px.

Home SVGs use intrinsic width/height attributes with `width: 100%`, `max-width: 100%`, and `height: auto`. Vector artwork stays sharp at different display resolutions, while proportional sizing keeps it within its containers.

About uses `<picture>` for responsive image art direction:

```html
<picture class="about-illustration">
  <source media="(max-width: 767px)"
          srcset="assets/images/about-workspace-mobile.svg"
          width="400" height="320" />
  <img src="assets/images/about-workspace-desktop.svg"
       width="640" height="440" alt="" />
</picture>
```

The browser selects the simpler mobile composition up to 767px. Larger viewports use the wider desktop image; `<img>` also supplies the fallback. CSS scales either image proportionally. This technique suits artwork whose composition changes with available space and addresses the PDF's responsive image requirement.

Source checks covered local links, image paths and dimensions, menu references, and preservation of Home content during integration. Final browser verification remains pending: test all target widths for overflow, overlap, readable text, image proportions, keyboard focus, and menu operation. Use Tab to focus the mobile menu checkbox and Space to toggle it, then check the navigation links. These targets are not claims of completed browser tests.

## Getting Started

```bash
git clone https://github.com/hakimsalaues/digital-agency.git
cd digital-agency
```

Open the folder in VS Code. With the **Live Server** extension available, right-click `index.html` and select **Open with Live Server**. Follow the navigation links to the other pages. The HTML files can also be opened directly in a browser.

No npm, Node.js, build tool, or dependency installation is required to run the website. Roboto requires internet access to load from Google Fonts; a sans-serif fallback is provided.

## AI-Assisted Development

Codex supported the documented implementation through CSS design system development, semantic HTML development, Flexbox and responsive styling, code review and accessibility analysis, PDF compliance auditing, CTA layout refinement, original SVG creation, and final code integration and source verification.

The assignment's process is:

**Think → Try → Ask AI → Understand → Test → Accept, Modify or Reject.**

Suggestions were evaluated against the client reference, technical restrictions, and project conventions. For example, the CTA heading and supporting text were grouped to sit beside the link on desktop and stack on mobile.

A contrast recommendation identified insufficient contrast for normal-sized light text on the required blue. The team evaluated that finding against the mandatory palette rather than automatically changing colors. The palette was retained. Services' contact panel and About's hero button use dark text on blue; Home still uses light text on blue in places, so the concern remains open. Palette compliance does not establish accessibility compliance.

AI explanations and static checks support understanding and review; they do not replace browser testing or team acceptance decisions. This record does not establish individual teammates' AI usage, completion of the initial team discussion, or every testing step. The PDF also asks the team to discuss and understand CSS-only menu options before seeking AI assistance for that feature.

## Assignment Compliance

| Client requirement | Implementation evidence |
| --- | --- |
| Semantic HTML | Header, navigation, main, section/article content, and footer elements. |
| Vanilla CSS and external stylesheets | Shared and page-specific styles; no frameworks or extra CSS libraries. |
| Flexbox and media queries | Page layouts, wrapping cards, and responsive breakpoints. |
| Shared navigation/footer | Present on all three pages. |
| CSS-only hamburger menu | Labeled checkbox and `:checked` sibling selectors. |
| Responsive images | Proportionally sized SVGs and About's `<picture>`/`<source>` selection. |
| Roboto | Google Fonts import in `css/base.css`. |
| GitHub collaboration | Shared [GitHub repository](https://github.com/hakimsalaues/digital-agency) and team contributions documented above. |

These notes describe implementation, not accessibility certification or completion of every assignment workflow and browser-testing requirement.

## Project Limitations

This is a fictional, frontend-only demonstration. The testimonial is illustrative, not a real client endorsement. `hello@digitalagency.example` is an explicitly labeled demonstration placeholder, not a monitored company inbox. There is no contact processing, backend, or data storage, and no deployed website is documented here.

Final cross-page browser and keyboard testing remains necessary before presentation. The PDF is present locally but currently untracked in Git; a clone will not include it unless it is added to the repository separately.
