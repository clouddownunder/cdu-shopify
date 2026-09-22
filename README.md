# Cloud Downunder – Shopify Website

## Project Overview

**Cloud Downunder** is a corporate technology consulting website built on **Shopify**.  
The website presents Cloud Downunder's consulting services, technology capabilities, case studies, industries, events, insights/blog content, testimonials, and contact/enquiry sections.

Website: https://clouddownunder.com.au/

The current website includes Microsoft, Cloud, Data & AI, DevOps, Cybersecurity, Salesforce, Big Data and software development related services.

## Technology Stack

- **Platform:** Shopify
- **Theme:** Custom Shopify theme
- **Templating:** Shopify Liquid
- **Frontend:** HTML5, CSS3, JavaScript
- **Responsive:** Desktop, Tablet and Mobile
- **Content Management:** Shopify Admin
- **Dynamic Content:** Shopify Liquid objects, metafields and metaobjects
- **Images/Assets:** Shopify CDN
- **Forms:** Shopify contact form functionality
- **SEO:** Shopify SEO features + custom Liquid/metadata where required

## Website Structure

The main website contains the following areas:

- Home
- Services
  - Microsoft
  - Microsoft 365
  - Dynamics 365
  - SharePoint
  - ASP.NET
  - C# .NET
  - Sitecore
  - DevOps
  - IoT
  - Salesforce
  - AI
  - Machine Learning
  - Staff Augmentation
  - Big Data
  - Hadoop
  - Spark
  - MongoDB
  - Kafka
  - Hive
  - Tableau
  - Sqoop
  - Cassandra
  - Cloud Computing
  - AWS
  - Azure
  - Google Cloud
  - IBM Cloud
  - Oracle Cloud
  - Cybersecurity
- Work / Case Studies
- Industries
- About
- Insights / Blog
- Events
- Contact

## Shopify Theme Features

### 1. Custom Header

The header includes:

- Main navigation
- Services mega-menu/dropdowns
- Technology/service links
- Responsive mobile navigation
- Contact / enquiry CTA
- Mobile menu interaction

### 2. Homepage

The homepage contains dynamically managed sections including:

- Hero/banner
- Client/trust logos
- Services overview
- Why Cloud Downunder
- Case studies
- Industries
- Methodology/process
- Company statistics
- Team members
- Technology capabilities
- Testimonials
- FAQ
- Upcoming events
- Latest insights/articles
- Contact CTA
- Footer

### 3. Service Pages

Service pages are created using reusable Shopify sections and dynamic content.

Typical service content includes:

- Service hero
- Introduction
- Service capabilities
- Benefits
- Technology/platform information
- Related services
- Case studies
- Testimonials
- CTA/contact section

Example service URL:

`/pages/service/sitecore-development-xm-cloud-migration-australia`

### 4. Case Studies

Case studies present completed projects and business outcomes.

Content can include:

- Client/company
- Industry
- Project description
- Key results
- Statistics
- Technology used
- Images
- Case study details

### 5. Industries

Industry-specific sections are used to present solutions for areas such as:

- Government & Public Sector
- Financial & Professional Services
- Healthcare & Life Sciences
- Retail & eCommerce
- Agriculture & AgTech
- Logistics & Transport
- Manufacturing & Industrial
- Startups & Scale-ups

### 6. Events

The website includes an upcoming events system.

Event information can include:

- Event title
- Event date
- Event time
- Location
- Speaker
- Description
- Registration URL
- Countdown / days-to-go indicator

Event content is managed dynamically through Shopify content structures.

### 7. Blog / Insights

The Insights section displays technology and business articles.

Features include:

- Blog listing
- Multiple blog sources
- Latest article section
- Article date
- Article detail page
- Related/latest articles
- Dynamic article content
- Responsive article layout

Articles are ordered using their published date where required.

### 8. Contact / Enquiry

The website provides enquiry/contact functionality using Shopify's contact form functionality.

Typical fields include:

- First name
- Last name
- Email
- Phone
- Message

Form submissions are handled through Shopify.

## Dynamic Content

The theme uses Shopify's dynamic content capabilities to make the website manageable from Shopify Admin.

Depending on the section, content can be managed using:

- Shopify pages
- Blogs and articles
- Metafields
- Metaobjects
- Theme settings
- Section settings
- Navigation menus

This allows administrators to update content without directly editing Liquid files.

## Theme File Structure

A typical project structure is:

```text
theme/
├── assets/
├── config/
├── layout/
├── locales/
├── sections/
├── snippets/
├── templates/
├── blocks/
└── README.md
```

### `assets/`

Contains:

- CSS files
- JavaScript files
- Images/icons where applicable
- Third-party frontend assets

### `config/`

Contains Shopify theme configuration:

- `settings_schema.json`
- `settings_data.json`

### `layout/`

Contains the main Shopify theme layout, normally:

- `theme.liquid`

### `sections/`

Contains reusable Shopify theme sections such as:

- Header
- Footer
- Hero/banner
- Services
- Case studies
- Industries
- Testimonials
- FAQ
- Events
- Blog/Insights
- Contact
- CTA sections

### `snippets/`

Contains reusable Liquid components used across multiple sections/templates.

### `templates/`

Contains Shopify page templates for different content types, such as:

- Homepage
- Pages
- Blogs
- Articles
- Services
- Case studies
- Contact
- 404

## Development Setup

### Prerequisites

Install the following:

- Shopify CLI
- Node.js
- Git
- Shopify Partner account or appropriate store access

Check Shopify CLI:

```bash
shopify version
```

Check Node.js:

```bash
node -v
```

Check Git:

```bash
git --version
```

## Clone the Repository

```bash
git clone <repository-url>
cd <project-folder>
```

## Shopify Store Login

Authenticate Shopify CLI:

```bash
shopify login
```

Or use the current Shopify CLI authentication flow supported by your Shopify account.

## Connect to the Store

For the Cloud Downunder development workflow, connect the theme to:

```text
clouddownunder.myshopify.com
```

Example:

```bash
shopify theme dev --store clouddownunder.myshopify.com
```

This starts a development preview and allows changes to be tested before publishing.

## Theme Development

Start the Shopify theme development server:

```bash
shopify theme dev --store clouddownunder.myshopify.com
```

The CLI will provide a preview URL.

To push the local theme to Shopify:

```bash
shopify theme push
```

To pull the latest theme files from Shopify:

```bash
shopify theme pull
```

Before pulling or pushing, make sure local changes are committed or backed up.

## Deployment Workflow

Recommended workflow:

1. Pull the latest theme from Shopify/Git.
2. Create a feature branch.
3. Make the required Liquid/CSS/JS changes.
4. Run the Shopify theme development server.
5. Test desktop and mobile layouts.
6. Test dynamic Shopify content.
7. Test forms and links.
8. Check SEO/canonical URLs.
9. Review the Shopify theme check output.
10. Push to the appropriate Shopify theme.
11. Verify the preview theme.
12. Publish only after final approval.

## Important Development Notes

### Liquid

Use Shopify Liquid for:

- Dynamic content
- Product/page/blog data
- Metafields
- Metaobjects
- Theme settings
- Conditional rendering
- Reusable snippets

Avoid hardcoding content when the content is expected to be managed by the client.

### CSS

Use scoped/component-specific CSS to avoid conflicts between sections.

Prefer section-specific classes such as:

```css
.cdu-service-section {}
.cdu-case-study-section {}
.cdu-event-section {}
```

Avoid broad selectors that can unintentionally affect other sections.

### JavaScript

JavaScript should be:

- Lightweight
- Section-aware
- Compatible with Shopify's dynamic rendering
- Safe when sections are loaded multiple times

Use `data-*` attributes for dynamic values where appropriate.

## SEO

SEO considerations for the website include:

- Page titles
- Meta descriptions
- Canonical URLs
- Heading hierarchy
- Image alt text
- Structured data where required
- Internal linking
- Blog/article URLs
- Service page URLs
- 404 handling
- Redirects
- Sitemap
- Robots configuration

When changing URLs, configure Shopify URL redirects where appropriate instead of relying only on frontend JavaScript URL replacement.

## Responsive Design

The website must be tested across:

- Desktop
- Laptop
- Tablet
- Mobile

Important responsive areas include:

- Header/navigation
- Hero sections
- Service cards
- Case study sliders
- Industry sections
- Testimonials
- Events
- Blog cards
- Contact forms
- Footer

## Content Management

Client-editable content should be managed through Shopify Admin wherever practical.

Before changing a dynamic section, check:

1. Which Shopify object provides the content?
2. Is the value coming from a metafield/metaobject?
3. Is it a section setting?
4. Is it controlled by a page/blog/article?
5. Does changing the Liquid affect other pages?

## Testing Checklist

Before publishing changes:

### Functional

- [ ] Header navigation works
- [ ] Mobile menu works
- [ ] All CTA buttons work
- [ ] Contact form submits correctly
- [ ] Event registration links work
- [ ] Blog links work
- [ ] Service links work
- [ ] Case study links work
- [ ] Footer links work

### Responsive

- [ ] Desktop
- [ ] Tablet
- [ ] Mobile
- [ ] Landscape mobile

### Content

- [ ] No placeholder text
- [ ] Images load correctly
- [ ] Alt text is present
- [ ] Dates are correctly formatted
- [ ] Dynamic content displays correctly

### SEO

- [ ] Title tags checked
- [ ] Meta descriptions checked
- [ ] Canonical URLs checked
- [ ] Heading structure checked
- [ ] Internal links checked
- [ ] 404 page checked
- [ ] Redirects checked

### Performance

- [ ] Images optimized
- [ ] Unused JavaScript removed
- [ ] Unused CSS reduced
- [ ] Third-party scripts reviewed
- [ ] Lazy loading used where appropriate

## Production Safety

Do not directly modify the live/published theme for major changes.

Recommended process:

```text
Local Development
       ↓
Shopify Development/Preview Theme
       ↓
Testing & QA
       ↓
Client Approval
       ↓
Production Theme
       ↓
Publish
```

Always keep a backup of the current production theme before making major changes.

## Useful Shopify CLI Commands

### Check CLI version

```bash
shopify version
```

### Login

```bash
shopify login
```

### Start theme development

```bash
shopify theme dev --store clouddownunder.myshopify.com
```

### Pull theme

```bash
shopify theme pull --store clouddownunder.myshopify.com
```

### Push theme

```bash
shopify theme push --store clouddownunder.myshopify.com
```

### List themes

```bash
shopify theme list --store clouddownunder.myshopify.com
```

### Check theme

```bash
shopify theme check
```

## Store Information

| Item | Value |
|---|---|
| Website | https://clouddownunder.com.au/ |
| Shopify Store | clouddownunder.myshopify.com |
| Platform | Shopify |
| Theme Type | Custom Shopify Theme |
| Template Language | Liquid |
| Primary Market | Australia |
| Business Focus | Microsoft, Cloud, Data, AI & Technology Consulting |

## Maintenance

When adding or updating a feature:

1. Identify the relevant Shopify section/template/snippet.
2. Check whether the content is dynamic.
3. Make the change locally.
4. Test using Shopify CLI.
5. Test desktop and mobile.
6. Check console errors.
7. Check Liquid/theme errors.
8. Verify SEO impact.
9. Test all affected links/forms.
10. Push to the preview theme.
11. Get approval before production deployment.

## Support

For website/content-related issues, use the Shopify Admin and theme codebase.

For Shopify-specific platform issues, refer to Shopify's official documentation.

---

**Project:** Cloud Downunder  
**Platform:** Shopify  
**Website:** https://clouddownunder.com.au/
