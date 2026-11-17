# GTM Tech Week Design System

The shared design contract for GTM Tech Week websites, event creative, community materials and shareable assets. This is one document: edit the local website's `public/DESIGN.md`; the website serves it at [gtm-week.com/DESIGN.md](https://www.gtm-week.com/DESIGN.md), and the local catalogue reads the same source. The public URL contains the last published version. Unpublished local edits are drafts of this document, not a separate design system.

## Visual catalogue and access

The [full visual catalogue](https://gtm-tech-week-design-system.artur229861.chatgpt.site/design-system) contains browsable foundations, components, sections and page examples. It requires ChatGPT sign-in and access granted by the owner. A ChatGPT account or this public link alone does not grant access. Ask the GTM Tech Week owner to add your sign-in email if you need the catalogue.

This contract stays public so people and AI tools can discover and follow the brand rules. The catalogue is a restricted implementation reference, not another editable contract. Its bundled contract is generated from this source when published. AI tools without authorised catalogue access should use this public document and ask for any examples they need; they must not assume that discovering the link grants access.

## 1. Authority and brand character

Follow explicit instructions for the current work, preserve supplied artwork and approved components, then apply this contract. Use the relevant asset family and named surface below. If a new brief conflicts with an approved asset or locked format, resolve that specific conflict before changing it.

GTM Tech Week is editorial, engineered, European, optimistic and slightly raw. It should feel like a serious movement with cultural energy. Make the main idea obvious in one glance.

- Use confident Space Grotesk headlines, readable body copy and short mono labels.
- Let visible structure, hard edges, rules, rails, grids and hard shadows organise the composition.
- Use warm paper and strong ink fields with deliberate signal colour. Give important ideas space and scale.
- Use large colour tiles for rhythm and smaller coded tiles for transitions when the content needs them. Align the information to that structure.
- Keep documentary photography recognisably human. Preserve approved people, logos, copy, names, dates and claims.
- Keep playful artwork, small tilted cards, markers and functional stickers purposeful. Do not invent slogans or decorate every element.

Starter restrictions are not brand rules. A starter's limited palette, two font weights, generic hover effect or neutral placeholder page must not redefine this system.

## 2. Approved assets and logo use

- [Primary logo](https://www.gtm-week.com/assets/brand/gtm-tech-week-logo.png)
- [Holographic square logo for founding-member assets](https://www.gtm-week.com/assets/brand/gtm-tech-week-holo-logo.png)
- [Founding-member signal texture](https://www.gtm-week.com/assets/community/member-card-signal-texture.jpg)
- [Canonical founding-member generator](https://www.gtm-week.com/community/share)
- [Berlin poster](https://www.gtm-week.com/assets/gtm-week-brandenburg-gate-poster.png)

Use the original asset appropriate to the family. Preserve the square proportions, complete lockup and existing background of the primary mark. Do not redraw it, recolour it, crop it into a new symbol or add effects. Do not convert an approved full-colour mark into a monochrome SVG merely to fit a starter.

Integrate the logo into the composition, including a full tile where appropriate. Do not add floating frames, extra padding, sticker treatment or shadows around the logo without a specific approved source. A tilted surrounding diagram does not imply permission to modify the logo.

Use supplied event artwork as the visual anchor for that event. Keep original scannable QR artwork and its quiet zone; size it for the actual viewing distance. Documentary portraits and logos are not material for generative reinterpretation.

## 3. Colour roles and named surfaces

### Core palette

| Role | Value | Use |
|---|---|---|
| Background | `#f6f1e8` | Warm page field |
| Paper | `#fffaf0` | Original creative and asset paper |
| Strong paper | `#ffffff` | Clean white where the source uses it |
| Ink | `#070707` | Original creative text and structure |
| Muted ink | `#67645c` | Original supporting text |
| Structural line | `#111111` | Original rules and hard shadows |
| Green | `#b8ff00` | Primary signal, highlights and coded tiles |
| Cyan | `#11d8ee` | Cool signal and engineering tiles |
| Yellow | `#ffe100` | Warm signal and tactics tiles |
| Magenta | `#ff3ad7` | Playful signal and execution tiles |
| Orange | `#ff6f32` | Reserved source-specific accent |
| Red | `#ff1f2d` | Reserved source-specific accent; not automatically an accessible text colour |

Prefer one deliberate signal per composition. Several signals may work together in an approved coded sequence: an event rail, principle tiles, programme categories or a system diagram. The full palette is available; every asset does not need every hue. Do not create unrelated rainbow sequences.

### Existing website surfaces

These are intentional, named variations of the same brand. Select the surface first and keep its values coherent.

| Role | Berlin website | Community website |
|---|---|---|
| Page paper | `#f6f1e8` | `#f6f1e8` |
| Primary ink | `#151611` | `#151611` |
| Supporting ink in the catalogue | `#55564c` | `#55564c` |
| Card paper in the catalogue | `#fffdf7` | `#fffdf7` |
| Portrait backing | `#dfded6` | `#dfded6` |
| Main action | Ink fill, cream text | Lime fill, ink text |
| Lime | `#b8ff00` | `#c0ff36` |
| Cyan | `#11d8ee` | `#87e4f4` |
| Pink / magenta | `#ff3ad7` | `#f991d3` |
| Additional coded fill | Yellow `#ffe100` | Diagram lilac `#efd8ff` |

The dusty pink `#efa0c7` belongs to founding-member cards and merchandise. It is not a global website colour. Website paper and ink variations do not silently replace the original creative defaults.

### Application rules

- Use dark ink on bright signal fills. Bright lime, yellow or pink must not become body text on cream.
- Use cream primary ink on dark information fields. Supporting text must remain readable.
- Berlin theme order is green / cyan / yellow / magenta. Its principle tiles use yellow / cyan / magenta. Community diagram areas use cyan and lilac; its functional sticker is pink.
- Use pale tints only for a clear purpose. The catalogue's pale lime `#ebf4be` and dark accent backing `#2b3518` are derived support colours, not extra identity colours.
- Form errors use accessible ink: the current catalogue uses `#9e241b` on light paper and derived `#ffb4ab` on dark surfaces. Never substitute the bright brand red without checking contrast.
- Keep text and fill roles distinct. In the catalogue, `surface-accent` is lime; `surface-signal-cool`, `surface-signal-warm`, `surface-signal-playful` and `surface-signal-soft` carry the coded fills. `ink-on-signal` remains dark even inside an inverted section.
- CSS primitives hold raw values; components use semantic roles such as `ink`, `surface` and `line`. Keep the roles consistent across light and inverted sections. Derived dark-theme values require contrast checks; they are not all measured source values.

## 4. Typography

| Family | Purpose | Supported source weights |
|---|---|---|
| Space Grotesk | Display headlines and major numbers | 500, 600, 700 |
| Inter | Body copy and controls | 400, 500, 600, 700, 800, 900 |
| JetBrains Mono | Labels, dates, metadata, URLs and system language | 500, 700 |

Keep headlines compact, bold and often tightly tracked. Labels are short, uppercase and functional. Body copy is direct and readable; do not set paragraphs in monospace. Avoid decorative typefaces unless supplied artwork already contains them.

Grey two-tone headlines are not a default brand treatment. Prefer strong ink with a source-supported signal marker or underline. The palette must not leave the whole composition looking muted.

Use licensed local font files where the implementation supports them. A font substitute must be named and reviewed. A limited set of weight utilities is an implementation choice, not a restriction on the brand's typography.

### Website catalogue reference scale

Sizes are pixels at the three review widths. They are reference tiers for web components, not universal sizes for social graphics or every hero.

| Tier | 375px viewport | 768px viewport | 1440px viewport | Line height / tracking |
|---|---:|---:|---:|---|
| H1 | 55 | 70 | 74 | 0.96 / -0.075em |
| H2 | 32 | 32 | 49 | 1.08 / -0.05em |
| H3 | 25 | 25 | 25 | 1.15 / -0.04em |
| H4 | 21 | 19 | 19 | 1.3 / -0.025em |
| H5 | 18 | 18 | 18 | Derived supporting tier |
| H6 | 16 | 16 | 16 | Derived supporting tier |

The current catalogue uses a generalised 14px small and 16px regular body scale, with 16/18px and 18/20px larger tiers. Its 11px mono label standardises the source's several small label sizes. Preserve page-specific compositions where a generic tier would weaken the hierarchy.

## 5. Layout, visual rhythm and atmosphere

- Standard web content maximum: 1220px. Use one shared container and deliberate gutters.
- Keep reading order and primary copy left aligned unless the approved composition calls for another alignment.
- Use cream for reading, saturated tile groups for rhythm and strong black sections for emphasis. A colour tile should express a category, step, event or message.
- Prefer a few large compositional decisions to many small decorations. Repeated cards are not a substitute for a clear hierarchy.
- The original atmosphere includes a quiet 44px grid, sparse dots and faint cyan/yellow light. Use these when the composition benefits; the clean paper of the Berlin and community pages is also intentional.
- Keep texture subordinate to type. Use one local glow or signal field, not a full rainbow wash.
- Align headings, imagery, utility text and QR codes to the same structure. Keep negative space and hard rules visible.

The current web catalogue changes layout at 768px and 1024px and is reviewed at 375px, 768px and 1440px. Breakpoints are implementation details; always verify actual stacking, heading wraps and image crops.

## 6. Corners, borders and shadows

| Treatment | Default / original assets | Existing website treatment |
|---|---|---|
| Structural panels, buttons and fields | Square | Square |
| Special utility/media corners | 8px when appropriate | Speaker/mentor cards use 10px |
| People portraits | Circular avatars where the family allows | Circular speaker/mentor portraits |
| Structural borders | 2px ink | 2px ink; 1px dividers and card outlines |
| Compact hard shadow | 4px × 4px | Berlin compact controls: 3px × 3px |
| Primary hard shadow | 8px × 8px | Berlin hero/catalogue panels: 6px × 6px |

These named treatments do not authorize arbitrary new values. Keep the existing surface coherent. Do not turn structural panels into rounded UI cards. Circular people portraits and rounded people cards are specific exceptions, not a direction for every container.

## 7. People, photography and motion

### Speakers and mentors

- Use the approved roster, original portraits, names, roles and verified profile links. Do not invent people, add unconfirmed appearances or infer attendance from a design example.
- Use circular portraits with a face-aware crop. The Berlin pattern is 88px on mobile and 112px at wider sizes, near centre 35% unless a particular portrait needs its approved crop.
- Berlin portraits retain their supplied colour. The community mentor pattern uses grayscale; this is a page-specific treatment, not a global filter.
- For large rosters, use three gently moving horizontal rows with the middle row offset, following the existing speaker composition. The nominal source speed is approximately 32.4px/s. Keep names and faces readable.
- Provide pause/resume, previous/next controls, touch interaction and keyboard navigation. Stop automatic motion while someone interacts or focuses a row, when offscreen, when the tab is hidden and when reduced motion is requested. Pausing on hover is an appropriate reading aid.
- Reduced motion retains manual access to every person. Looping duplicates must be inert and hidden from assistive technology; they must not inflate counts or keyboard stops.
- Preserve usable static content without animation. Decorative movement must not block reading or page scrolling.

### Other photography

Preserve the supplied person and the purpose of the image. Do not stretch faces, generate replacement documentary portraits or apply speaker masks to every asset. The founding-member portrait treatment below has its own locked geometry.

## 8. Components, controls and partner logos

### Controls and composition

- Keep primary actions obvious, with one main action per view. Secondary actions have a clear lower hierarchy.
- Use square controls, visible borders and purposeful hard shadows. Show keyboard focus clearly; do not rely on hover or colour alone.
- Berlin's primary action is dark with cream text and a lime source hover. Community's is lime with dark text and a compact hard shadow. A starter's opacity hover is an implementation approximation, not a brand-wide rule.
- Keep inputs and form states readable, including error, focus and disabled states. Source website fields are square and approximately 52px high.
- FAQ rows use a clear divider and plus/minus state, with keyboard access and reduced-motion support. Native content remains usable without animation.
- Generic content cards are square. People cards retain their separate 10px treatment. Quote layouts use hierarchy and rules; examples must never invent endorsements.
- Use the correct source logo, actual links and the appropriate footer tone. Catalogue navigation and example content are not the production site's complete information architecture.

### Partner logos

- Use supplied originals and verified links. Preserve wordmark proportions, complete lockups and readable detail. Never stretch or crop a logo into a uniform square.
- Preserve full colour and opacity by default. Do not apply blanket grayscale, faded opacity or black conversion. A source-specific alternative treatment needs evidence for that asset.
- Size optically by format: wide wordmark, compact symbol, named mark or featured partner. Preserve internal asset whitespace and compare apparent size rather than imposing identical dimensions.
- Keep Partners and Community partners separate. Featured placement must come from an approved relationship or brief. Do not let a partner mark take over GTM Tech Week's identity.
- For Mentic, use the supplied orange-symbol/black-wordmark SVG rather than superseded logo choices.
- A logo in a design sample does not establish a new partnership, tier or entitlement.

## 9. Reusable website sections

Compose pages from registered sections that share components, roles and the page container. Keep the content separate from the layout so it can change without redesigning the section.

| Pattern | Purpose | Existing source |
|---|---|---|
| Event poster hero | Event title, date tile, original poster and coded themes | [Berlin hero](https://www.gtm-week.com/#hero) |
| Signal principles | Three coloured principles or a dark promise section | [Berlin About](https://www.gtm-week.com/#about), [Community](https://www.gtm-week.com/community) |
| Community system hero | Lime marker, editable diagram, coded areas and functional sticker | [Community hero](https://www.gtm-week.com/community) |
| Moving speaker rows | Original portraits, profile links and accessible movement | [Speakers](https://www.gtm-week.com/#speakers) |
| Partner strip | Format-aware original logos and separate partner groups | [Partners](https://www.gtm-week.com/#partners) |

In the Astro catalogue these are `event-poster-hero`, `signal-principles`, `community-system-hero`, `speaker-rows` and `partner-strip`. Its registry is `src/sections/index.ts`. Starter hero/features/CTA demonstrations are examples of composition, not GTM Tech Week visual references.

When adding a section: identify its source and purpose, choose the appropriate surface, use existing roles and components, expose the copy as typed props, register it and check all three review widths. Document intentional adaptations. A dated example roster, price or logo sample is not a live content feed.

## 10. Asset families and locked formats

### Websites and community pages

Lead with warm paper, black structure, strong headlines, mono labels and documentary photography. Use purposeful signal moments and approved coded sequences. Preserve the relevant Berlin or community surface instead of mixing their values at random.

### Event assets

Anchor each event in its own approved hero artwork. Do not force unrelated formats into a founding-member card or repeat one poster composition regardless of content.

### Curriculum and reports

Make the argument and workflow visible. Use diagrams, evidence and information hierarchy. Avoid dashboard decoration that does not explain the content.

### Founding-member cards and merchandise

The [public generator](https://www.gtm-week.com/community/share) is the canonical component. Keep the following locked:

- Square 1080 × 1080 output.
- 73% portrait field and 27% black copy field.
- Four-colour top rail: green, cyan, yellow, magenta.
- Scoped holographic square logo at top left.
- Name tile immediately beside `FOUNDING MEMBER`.
- Copy order: `I'M BUILDING EUROPE'S`, then `GTM FUTURE`.
- Footer: `GTM TECH WEEK COMMUNITY` and `GTM-WEEK.COM`.
- Status: `FOUNDING MEMBER`.

Use the dusty pink signal texture in the portrait field. The portrait is grayscale, higher contrast, slightly brighter and multiplied into the texture. When zooming out, fill only the unused axis with a straight black edge fade. Never apply a circular, oval or radial portrait mask. Speaker-avatar rules do not apply here.

Members may change only name, photo, zoom and position. Process member photos locally in the browser; do not upload or retain them.

## 11. Implementation and reuse

- Maintain this one contract. The public website serves its own `public/DESIGN.md`; local tools and the catalogue must read that source or an exact generated representation, never an independently edited competing contract.
- Tokens implement the contract. Keep CSS primitive values central, give them semantic roles and use those roles in components. Change the relevant implementation and this contract together when a design decision changes.
- Do not encode starter conveniences as permanent brand limitations: two weights, a single available accent, fixed component counts or one generic layout are not identity rules.
- Keep approved artwork intact. Rebuild editable diagrams as content and code rather than screenshots. Name measured values and derived adaptations honestly.
- Keep build logs, test results, temporary setup details and review history outside this contract. They are evidence about an implementation, not instructions for the brand.
- Keep publication state exact: local changes become publicly shareable at the canonical URL after publication. Do not describe a local preview as a released website.

## 12. Evaluation and quality checks

An output should retain its hierarchy without the logo, in grayscale, with a different approved photo and at phone size. Compare it beside the relevant production surface. Type, structure, paper and purposeful signal colour should identify the system.

Before calling new work ready:

- The primary message is obvious in one glance; reading order and alignment are deliberate.
- The correct asset family, logo variant, palette and portrait geometry are used.
- Copy, dates, names, links and claims match their approved sources.
- Text and focus remain readable. Check intended colour pairs with WCAG relative luminance: at least 4.5:1 for normal text and 3:1 for large text.
- Check mobile, tablet and desktop layouts; for this catalogue use 375px, 768px and 1440px. No unintended horizontal overflow, clipped content or distorted photography.
- Check interactive controls with keyboard, touch and reduced motion, including motion pause and manual navigation.
- Check original logos and image crops visually, not only their file dimensions.
- Generated social downloads match their promised dimensions, QR codes remain scannable and member photos stay local.
- Build and relevant interaction checks pass. Record results separately.

Avoid generic SaaS/dashboard styling, pill and badge clusters, glass cards, decorative rounded panels, arbitrary gradients, unrelated rainbow washes and holographic colour covering entire pages. Do not substitute visual noise for a clear message.
