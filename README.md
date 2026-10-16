# Digital Agency

## Project Overview

Digital Agency is a fictional digital and technology company offering web development, UI/UX design, digital consulting, and digital strategy. This collaborative frontend assignment builds a responsive three-page website based on the client's [AI-CSS Assignment PDF].

The landing page follows the client's visual reference, Roboto typography, and color palette. The remaining pages must share the same visual identity.

## Technologies Used

- Semantic HTML5
- Vanilla CSS, Flexbox, and CSS media queries
- Roboto, imported from Google Fonts
- Git and GitHub for version control and collaboration

JavaScript, CSS Grid, Sass, and frameworks are prohibited. The PDF permits Font Awesome only for icons; it is not currently used. No build tools or package installation are required.

## Website Pages

| Page            | File            | Current implementation                                      |
| --------------- | --------------- | ----------------------------------------------------------- |
| Home            | `index.html`    | Hero, four service cards, illustrative testimonial, and CTA |
| Services        | `services.html` | Empty file; implementation pending                          |
| About & Contact | `about.html`    | Empty file; implementation pending                          |

## Project Structure

```text
digital-agency/
├── AI-CSS Assignment.pdf
├── README.md
├── index.html
├── services.html
├── about.html
├── css/
│   ├── base.css
│   ├── home.css
│   ├── navigation.css
│   ├── services.css
│   └── about.css
└── assets/
    └── images/
```

`base.css` defines the shared font, colors, reset, typography, links, and buttons. `home.css` styles the landing page. The other stylesheets and `assets/images/` are currently empty. Empty directories may not appear in a Git clone until tracked files are added.

## Team Members and Responsibilities

These are assigned responsibilities, not claims of completed work.

| Team member                   | Responsibilities                                                                                                                           |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **Hakim Salaues — Team Lead** | Landing page (`index.html`, `css/home.css`); global styling (`css/base.css`); GitHub coordination, documentation, and integration          |
| **Fadi Omer**                 | Services page (`services.html`, `css/services.css`); shared navigation, header, and footer; CSS-only hamburger menu (`css/navigation.css`) |
| **Lulamani Maluleka**         | About & Contact page (`about.html`, `css/about.css`); responsive images; responsive QA support                                             |

## Responsive Design

The assignment requires testing at approximately:

| Device  | Viewport width  |
| ------- | --------------- |
| Mobile  | 375px           |
| Tablet  | 768px           |
| Desktop | 1200px or wider |

The implemented landing CSS uses Flexbox for the hero, service cards, and CTA. Cards change from four columns to two below 1200px and one below 768px. Below 768px, the hero and CTA stack vertically. The CTA can also wrap when its text group and link cannot fit beside each other.

Hakim reported manual responsive testing of the initial landing implementation. The subsequent CTA adjustment received a source review, but its browser verification is still pending. Final testing must be repeated after navigation, images, and other pages are integrated: check horizontal overflow, readable text, image proportions, section overlap, visible keyboard focus, and mobile menu usability.

Responsive image source selection is not implemented yet. The team must choose an appropriate technique, such as `srcset`/`sizes` or `<picture>`, and explain why it suits the selected images.

## Getting Started

Clone the repository:

```bash
git clone https://github.com/hakimsalaues/digital-agency.git
cd digital-agency
```

Open the folder in VS Code. Install the **Live Server** extension if needed, then right-click `index.html` and select **Open with Live Server**. The page opens in your browser with automatic refresh when files are saved.

No `npm install` or `npm run dev` command is required. An internet connection is needed to load Roboto from Google Fonts; otherwise, the sans-serif fallback is used.

## AI-Assisted Development

The assignment's process is:

**Think → Try → Ask AI → Understand → Test → Accept, Modify or Reject**

The documented landing-page work used AI assistance at these stages:

1. Planning the global CSS design system and reusable styles.
2. Building and explaining the semantic HTML landing structure.
3. Implementing Flexbox layouts and responsive CSS.
4. Reviewing accessibility and assignment compliance, including the PDF's embedded references.
5. Evaluating and adjusting the CTA to group its text beside the link, following the client reference.

An AI review identified insufficient contrast for normal-sized light text on the required blue background. The team evaluated that finding against the client's mandatory colors instead of automatically changing the palette. The palette remains unchanged; the accessibility concern is still recorded for consideration.

AI explanations and source reviews support the team's decisions; they do not replace understanding or browser testing. This record does not establish other members' AI stages, the initial team discussion, or completion of every testing step. The PDF also requires the team to discuss and understand CSS-only menu options before seeking AI assistance for that feature.

## Project Status

**Implemented landing-page work:** semantic sections, four service cards, clearly illustrative testimonial, shared design foundation, responsive Flexbox styles, and revised CTA grouping. The client font and palette are defined in CSS.

**Pending before submission:**

- Shared header, navigation, and footer integration.
- CSS-only hamburger menu implementation and integration.
- Replacement of five image placeholders with responsive images and technique explanations.
- Services and About & Contact page implementation.
- Browser verification of the revised CTA and final cross-page responsive, keyboard, and visual QA.
- Updates to this README with verified integration status, image decisions, and actual test results.
