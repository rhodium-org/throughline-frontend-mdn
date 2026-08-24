# MDN Web Docs front-end best practices — throughline source

This document is **generated from the graph** by `tl docs`; `tl docs --check` gates it in CI. The prose headings are hand-owned — everything between `tl:*` markers is injected from the YAML items, so the published spec can never drift from the graph.

This source re-expresses **MDN Web Docs front-end best practices** as a grounded IDD graph: each best-practice area is a `user_requirement`, and every individual recommendation is a `system_requirement` that `implements` its area. The guide reference lives in `attrs.source_ref`; the throughline UIDs are this source's own and immutable — a consumer cites a rule as `mdn:SR-0001`, never by section name.

It carries
<!-- tl:count type == 'user_requirement' -->
8
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
55
<!-- tl:end --> practice rules.

## Purpose

<!-- tl:item INT-0001 -->
**INT-0001 — Front-end code follows the open-web platform's best practices for accessible, semantic, maintainable HTML, CSS and JavaScript** — `intent`, status `approved`

> MDN Web Docs exists so that front-end code is built on the grain of the open web platform: semantic HTML that describes meaning, CSS that keeps specificity low and layouts fluid, forms and interactions that any person can operate with a keyboard or assistive technology, and pages that are delivered securely and enhance progressively. Following these practices means a page works, is understandable and is maintainable across the widest range of browsers, devices and users, rather than only on the author's machine.

**source_ref**: MDN Web Docs
<!-- tl:end -->

## Semantic HTML

<!-- tl:item UR-0001 -->
**UR-0001 — Semantic HTML** — `user_requirement`, status `approved`

> Use HTML elements for the meaning they carry, so that document structure is conveyed to browsers, search engines and assistive technology.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Semantic HTML
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Semantic HTML') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0001 | system_requirement | approved | Use semantic elements for their meaning, not div and span |
| SR-0002 | system_requirement | approved | Define page structure with document landmarks |
| SR-0003 | system_requirement | approved | Use a single h1 and do not skip heading levels |
| SR-0004 | system_requirement | approved | Use em for emphasis and strong for importance |
| SR-0005 | system_requirement | approved | Use the correct list element for the content |
| SR-0006 | system_requirement | approved | Mark up abbreviations and quotations semantically |
<!-- tl:end -->

## Accessibility

<!-- tl:item UR-0002 -->
**UR-0002 — Accessibility** — `user_requirement`, status `approved`

> Make content operable and understandable for everyone, including keyboard and assistive-technology users, through accessible markup, text alternatives and focus management.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Accessibility
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Accessibility') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0007 | system_requirement | approved | Prefer native controls for built-in keyboard support |
| SR-0008 | system_requirement | approved | Write meaningful link text that stands alone |
| SR-0009 | system_requirement | approved | Warn when a link opens a new window or non-HTML resource |
| SR-0010 | system_requirement | approved | Use real href values, not links as fake buttons |
| SR-0011 | system_requirement | approved | Provide a skip link to the main content |
| SR-0012 | system_requirement | approved | Give meaningful images descriptive alt text |
| SR-0013 | system_requirement | approved | Give decorative images an empty alt attribute |
| SR-0014 | system_requirement | approved | Associate images with captions using figure and figcaption |
| SR-0015 | system_requirement | approved | Associate every form control with a label |
| SR-0016 | system_requirement | approved | Mark up data tables with header cells and scope |
| SR-0017 | system_requirement | approved | Give each data table a caption |
| SR-0018 | system_requirement | approved | Only add tabindex=0 to custom controls, never a positive value |
| SR-0019 | system_requirement | approved | Space interactive targets to prevent mis-activation |
<!-- tl:end -->

## CSS Best Practices

<!-- tl:item UR-0003 -->
**UR-0003 — CSS Best Practices** — `user_requirement`, status `approved`

> Keep stylesheets maintainable by controlling specificity, using the cascade and inheritance deliberately, and organising rules from generic to specific.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: CSS Best Practices
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: CSS Best Practices') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0020 | system_requirement | approved | Style with classes rather than IDs |
| SR-0021 | system_requirement | approved | Avoid !important |
| SR-0022 | system_requirement | approved | Keep selector specificity low |
| SR-0023 | system_requirement | approved | Rely on source order for equal-specificity overrides |
| SR-0024 | system_requirement | approved | Use inheritance rather than repeating declarations |
| SR-0025 | system_requirement | approved | Define generic styles first, then refine with classes |
<!-- tl:end -->

## Responsive Design

<!-- tl:item UR-0004 -->
**UR-0004 — Responsive Design** — `user_requirement`, status `approved`

> Build layouts, media and typography that adapt fluidly to any viewport, working mobile-first from a single-column baseline outward.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Responsive Design
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Responsive Design') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0026 | system_requirement | approved | Include the viewport meta tag |
| SR-0027 | system_requirement | approved | Design mobile-first from a single-column baseline |
| SR-0028 | system_requirement | approved | Define media-query breakpoints in relative units |
| SR-0029 | system_requirement | approved | Build flexible layouts with Flexbox and Grid |
| SR-0030 | system_requirement | approved | Constrain media to their container |
| SR-0031 | system_requirement | approved | Serve appropriately sized images with srcset and picture |
| SR-0032 | system_requirement | approved | Use relative units and avoid fixed widths |
| SR-0033 | system_requirement | approved | Scale typography responsively while preserving zoom |
<!-- tl:end -->

## Forms

<!-- tl:item UR-0005 -->
**UR-0005 — Forms** — `user_requirement`, status `approved`

> Structure and label forms so that controls are understandable, grouped, keyboard-operable and announced correctly by assistive technology.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Forms
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Forms') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0034 | system_requirement | approved | Group related controls with fieldset and legend |
| SR-0035 | system_requirement | approved | Choose the input type that matches the data |
| SR-0036 | system_requirement | approved | Mark mandatory fields with the required attribute |
| SR-0037 | system_requirement | approved | State required-field conventions before the form |
| SR-0038 | system_requirement | approved | Structure long forms with sections and headings |
| SR-0039 | system_requirement | approved | Never nest one form inside another |
<!-- tl:end -->

## Progressive Enhancement

<!-- tl:item UR-0006 -->
**UR-0006 — Progressive Enhancement** — `user_requirement`, status `approved`

> Layer the experience from a working HTML baseline up through CSS and JavaScript, so core content and functionality survive when advanced features are absent.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Progressive Enhancement
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Progressive Enhancement') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0040 | system_requirement | approved | Provide core content and function in plain HTML |
| SR-0041 | system_requirement | approved | Layer CSS as a presentation enhancement |
| SR-0042 | system_requirement | approved | Layer JavaScript as an interactivity enhancement |
| SR-0043 | system_requirement | approved | Feature-detect before using advanced APIs |
<!-- tl:end -->

## Content Security Policy

<!-- tl:item UR-0007 -->
**UR-0007 — Content Security Policy** — `user_requirement`, status `approved`

> Constrain which resources a page may load and execute with a strict Content Security Policy that mitigates cross-site scripting and injection.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Content Security Policy
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Content Security Policy') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0044 | system_requirement | approved | Deliver the policy in the Content-Security-Policy header |
| SR-0045 | system_requirement | approved | Set a restrictive default-src |
| SR-0046 | system_requirement | approved | Avoid unsafe-inline for scripts and styles |
| SR-0047 | system_requirement | approved | Avoid unsafe-eval |
| SR-0048 | system_requirement | approved | Allow trusted scripts with nonces or hashes |
| SR-0049 | system_requirement | approved | Set frame-ancestors to prevent clickjacking |
| SR-0050 | system_requirement | approved | Disable object embeds with object-src none |
| SR-0051 | system_requirement | approved | Test with Content-Security-Policy-Report-Only and reporting |
<!-- tl:end -->

## Transport Security

<!-- tl:item UR-0008 -->
**UR-0008 — Transport Security** — `user_requirement`, status `approved`

> Deliver every resource over HTTPS and enforce it with redirects, HSTS and the removal of mixed content.

*Derives from:* INT-0001

**source_ref**: MDN Web Docs: Transport Security
<!-- tl:end -->

<!-- tl:table type == 'system_requirement' and attrs.get('source_ref', '').startswith('MDN Web Docs: Transport Security') -->
| UID | Type | Status | Title |
|---|---|---|---|
| SR-0052 | system_requirement | approved | Serve every resource over HTTPS |
| SR-0053 | system_requirement | approved | Redirect HTTP to HTTPS permanently |
| SR-0054 | system_requirement | approved | Send HSTS with a long max-age and includeSubDomains |
| SR-0055 | system_requirement | approved | Upgrade legacy insecure requests |
<!-- tl:end -->

