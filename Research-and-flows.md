# KAMPUS StudentPass — updated client flow

Updated 7 October 2026. Open `kampus.html` directly in a browser and refresh any already-open copy. The complete app, images, Kumbh Sans font and demo QR are embedded in one standalone HTML file; no installation or internet is required for the app itself. Source links open external websites.

## Design direction

The client's StudentPass prototype is the primary flow reference. UNiDAYS supplies the palette direction; Mecenat supplies brand-discovery inspiration. The result is an original responsive web app, retaining KAMPUS branding with StudentPass RDC as the service label.

Palette: mint green #8CFFAA, ink #16181D, white #FFFFFF, canvas #F7F8FA, borders #E6E8EE and pale mint #EDFFF2. The structure retains the prior UNiDAYS inspiration; the mint accent follows the latest client request. Dark ink is used on mint buttons and pass surfaces for readability.

Century Gothic is first choice for headings and the KAMPUS identity when installed. Kumbh Sans is embedded for body text and heading fallback. Century Gothic is not redistributed as a webfont; its licensed webfont can be supplied for identical rendering on all devices. Kumbh Sans's SIL Open Font License is included in the HTML source.

## References inspected

- [Client StudentPass RDC prototype](https://claude.ai/artifact/YURFCVqsZUgphJ6kubXwSW): home, offer details, activation, pass, verification, profile, first-visit guidance and partner scanner inspected through the public interactive artifact.
- [UNiDAYS India](https://www.myunidays.com/IN/en-IN): category discovery, search, student verification and online/in-store benefit model.
- [Mecenat Sweden](https://mecenat.com/se): campaign discovery, brand offers, favorites and pass navigation.
- [Kumbh Sans font](https://github.com/google/fonts/tree/main/ofl/kumbhsans): embedded variable font and license.

## Implemented screens and journeys

1. Home: greeting, verification status, campaign panels, categories, six brand shortcuts, offer cards, local businesses and pass access.
2. Search/offers: free-text search, category, channel, location and sorting filters; clear no-results state.
3. Offer details: real brand/photo, demo benefit, instructions, conditions, location, source link, save and share-copy actions.
4. Activated offer: online coupon or in-store demo QR; ten-minute session timer and expired state.
5. StudentPass: verified session profile, institution, demo ID and QR, contrast control and details.
6. Verification: institution → method → fictitious profile → confirmation. Email path simulates approval; document path simulates pending review and approval. No documents are uploaded.
7. Verified success: returns to the chosen offer or opens the pass.
8. First-visit guidance: three-step guide from Help/first visit; skip and next controls.
9. Favorites: save/remove offers with browser-local persistence.
10. Profile: verification, pass, local notification preference, language explanation, help, partner access and end-session action.
11. Partner scanner: simulated scan → valid/invalid state → confirm reduction → used state. Checks verified session, active in-store offer, expiry and prior use. No camera is accessed.
12. Online merchant recap and simulated order completion.

Desktop uses a navigation rail; mobile uses bottom navigation with a prominent StudentPass button. The layout includes small-screen breakpoints and touch-sized primary controls. Final visual checks remain outstanding because browser tooling blocked preview access in this turn.

## Proposed UX improvements

A smaller campaign area puts browsing closer to the first screen. Status and pass access remain visible. The selected offer survives verification, removing the need to search for it again. Channel labels clarify online versus in-store use. Empty, pending, approved, expired, used and invalid states make outcomes explicit. Real offer counts replace the reference's invented large catalog counts. These are design improvements proposed for client review, not usability-study results.

## Real brands, simulated commercial offers

Amazon, Lyko, H&M, Zalando, Samsung and Apple are shown with actual public merchant campaign imagery. Availability, shipping and student eligibility in DRC are not confirmed.

Local businesses include Orange RDC, Vodacom RDC and Pâtes en Folie. The restaurant's official site publishes its address as Immeuble CTC, avenue Wagenia, Gombe, Kinshasa. No precise telecom shop location or nearby distance is invented. The Vodacom image contains its own public campaign wording; that campaign is separate from the prototype's proposed benefit.

All percentages, example CDF prices, coupons, approvals, purchases and redemptions are simulated. The real brands are not presented as confirmed KAMPUS partners. No payments, emails or documents are transmitted. QR payload is the literal non-personal string KAMPUS-DEMO-NOT-VALID-NO-PERSONAL-DATA; the timer is a client-side simulation, not a secure signed-token implementation.

## Asset sources

The following images were retrieved from the cited public pages for the requested client design reference. Public availability is not a transferable image license; confirm usage permissions before public/commercial deployment.

- amazon: [source page](https://mecenat.com/se/amazon) · [image](https://img.meccdn.com/media/bf623a6d-632e-494f-95c5-404e0965c91f.png@jpg?h=600)
- lyko: [source page](https://mecenat.com/se/lyko) · [image](https://img.meccdn.com/media/6ef6b47b-5399-4503-8ed3-c432dcb8f848.jfif?h=600)
- hochm: [source page](https://mecenat.com/se/hochm) · [image](https://img.meccdn.com/media/image1_160_250402174437826295.jpg?h=600)
- zalando: [source page](https://mecenat.com/se/zalando) · [image](https://img.meccdn.com/media/bee10a9e-02ac-453a-8ec5-a9a4482a3451.jpg?h=600)
- samsung: [source page](https://mecenat.com/se/samsung) · [image](https://img.meccdn.com/media/c3fb2aff-583d-4fe3-9bb0-e120e1eb4da8.jfif?h=600)
- apple: [source page](https://mecenat.com/se/apple) · [image](https://img.meccdn.com/media/8478461a-1610-4ecd-928a-159b1b2fdd07.png@jpg?h=600)
- vodacom: [source page](https://www.vodacom.cd/fr/particulier) · [image](https://www.vodacom.cd/sites/drc-portal/files/images/2026-08/Website%20cover.jpg)
- mpesa: [source page](https://www.vodacom.cd/fr/particulier) · [image](https://www.vodacom.cd/sites/drc-portal/files/images/2025-08/mpesamikili2023.png)
- orange-rdc: [source page](https://www.orange.cd/) · [image](https://www.orange.cd/congo_pages/uploads/1/img/2018-02-telephoner-a-tout-moment-sans-contrainte-de-rechargement.jpg)
- Pâtes en Folie: [source page](https://patesenfolie.cd/) · [image](https://patesenfolie.cd/wp-content/uploads/2025/06/dejeuner-e1755538339428.jpg)

- Student lifestyle photo: [Monstera Production on Pexels](https://www.pexels.com/photo/cheerful-black-students-with-documents-standing-close-6281733/). Illustrative stock photo, not a claim of Kinshasa location.

## Verification completed

JavaScript syntax check passed. Node-based logic checks passed for nine catalog offers; text/category/location/local filtering; verification-gated activation; expiry; in-store validation, single-use rejection and online-offer rejection by the scanner; online order simulation; thirteen route render functions; four verification-stage render functions; and image/font embedding. These are logic/source checks, not end-to-end browser checks.

The earlier version's desktop/mobile screenshots and browser-test results do not verify this redesign. Final visual and browser interaction checks were blocked by the browser URL-policy error. User review of desktop and mobile rendering is still needed.

## Production scope

Real authentication, institution verification, document review/storage, merchant onboarding, country availability, server-issued coupons, signed rotating QR codes, partner authorization, redemption audit logs and payment/merchant integrations are not connected. A native mobile application is not included; this is a mobile-responsive standalone web app.

## Latest interface refinement

Authentic logo images replace typed wordmarks for Amazon, Apple, Dell, HP, Lenovo, H&M, Lyko, Zalando and Samsung. Dell/HP/Lenovo are brand discovery shortcuts; no additional commercial offers are invented for them. Category cards now use 15–17px labels, larger mint-backed icons and a two-column mobile layout. The mobile header includes a full-width search row. Non-home app screens include explicit back controls.

The student card uses KAMPUS mint #8CFFAA with dark text, incorporating the supplied reference fields: student name, institution, verified status, validity, ID and QR. The displayed 30 SEP 2027 date is explicitly labelled as a presentation example; demo verification remains session-only. No reference-card identity is copied into the user profile.

Logo asset URLs (retrieved from public Mecenat merchant pages):
- Amazon: [logo image](https://img.meccdn.com/media/logo_196_220304160024324379.png@jpg?h=100)
- HP: [logo image](https://img.meccdn.com/media/logo_114_210407153824705026.png@jpg?h=100)
- Apple: [logo image](https://img.meccdn.com/media/6b44234d-9e8e-41a9-9002-e13a4b95df27.png@jpg?h=100)
- Lenovo: [logo image](https://img.meccdn.com/media/logo_196_231005083148545267.jpg?h=100)
- H&M: [logo image](https://img.meccdn.com/media/logo_118_190527144228471356.png@jpg?h=100)
- Lyko: [logo image](https://img.meccdn.com/media/logo_114_211102161638559088.png@jpg?h=100)
- Samsung: [logo image](https://img.meccdn.com/media/logo_114_200127110226966859.png@jpg?h=100)
- Zalando: [logo image](https://img.meccdn.com/media/6060bd4e-5eac-4383-9341-920806364ac2.png@jpg?h=100)
- Dell: [logo image](https://img.meccdn.com/media/logo_160_230924204621374854.jpg?h=100)

Brand strip updated to a single horizontal, scroll-snapping logo-only carousel with swipe, trackpad, scrollbar and arrow-key support. Cards retain brand filtering actions and accessible brand labels.
