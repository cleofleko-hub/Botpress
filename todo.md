# Project TODO

- [x] Apply the BOTPRESS brand name, exact required hero tagline, dark premium background, and neon technology aesthetic.
- [x] Build responsive top navigation linking to Home, Virtual Numbers, WhatsApp Bots, Proxies, FAQ, and Dashboard.
- [x] Build an asymmetric hero section with clear primary and secondary calls to action and a futuristic product-system visual.
- [x] Build a concise trust-and-capabilities strip without fabricated reviews, ratings, testimonials, or unsupported customer claims.
- [x] Build the Virtual Numbers panel with USA, UK, Canada, Australia, Germany, and France, including flags and service details.
- [x] Display country-specific virtual-number prices: $1.00 for the first five listings and $0.51 for France.
- [x] Add a one-click virtual-number purchase flow with confirmation, wallet-balance validation, success state, and actionable error state.
- [x] Build the WhatsApp Bot panel with guided setup, bot templates, one-click deployment, deployment progress, and status display.
- [x] Add session management, reconnect controls, and bot recovery interactions to the WhatsApp Bot panel.
- [x] Build the Proxies panel with HTTP, SOCKS5, residential, and datacenter proxy types.
- [x] Add proxy region selection, speed and uptime metrics, one-click activation, and activation feedback.
- [x] Integrate the provided authentication flow for sign-up, login, logout, and protected personal dashboard access.
- [x] Build a personal dashboard summarizing wallet balance, active virtual numbers, deployed bots, active proxies, and recent activity.
- [x] Add persistent database models and typed server procedures for wallet state, service purchases, bot deployments, and proxy activations.
- [x] Build a wallet panel with top-up amount selection, transaction feedback, and service-payment handling.
- [x] Add contextual tooltips to unfamiliar controls across all service panels.
- [x] Add step-by-step self-service guides to the Virtual Numbers, WhatsApp Bots, and Proxies panels.
- [x] Add focused FAQ accordions to every service panel plus a global FAQ section.
- [x] Add loading, empty, success, insufficient-balance, unauthenticated, and error states for all key interactions.
- [x] Ensure keyboard navigation, visible focus states, readable contrast, semantic landmarks, and reduced-motion support.
- [x] Verify responsive presentation on desktop and mobile layouts.
- [x] Add or update Vitest coverage for service catalog constants and authenticated service procedures.
- [x] Run TypeScript checks, unit tests, and production build successfully.
- [x] Visually inspect the landing page and dashboard, then refine layout and styling issues.
- [x] Connect Stripe account keys and enable live card wallet top-ups; superseded by the user's Paystack integration requirement.
- [ ] Connect a virtual-number provisioning API so paid pending orders can receive real numbers and credentials.
- [ ] Connect a WhatsApp deployment provider so bot workspaces can generate live pairing sessions, deploy, reconnect, and recover hosted bots.
- [ ] Connect a proxy provisioning API so saved proxy configurations can activate and reveal live credentials.
- [x] Save one completed project checkpoint and provide the project version for review.
- [x] Set every proxy country and proxy type to a fixed purchase price of exactly $1.
- [x] Display the $1 proxy price clearly in proxy cards, configuration summary, confirmation dialog, and dashboard activity.
- [x] Redirect authenticated proxy selections into a Paystack payment confirmation flow before activation.
- [x] Redirect authenticated virtual-number selections into a Paystack payment confirmation flow using the selected country price.
- [x] Add secure Paystack transaction initialization on the server with user, service, amount, currency, and unique reference metadata.
- [x] Add server-side Paystack verification and signed webhook processing before marking purchases paid.
- [x] Add persistent payment records covering initialized, paid, failed, abandoned, and refunded states without storing card details.
- [x] Fulfill successful virtual-number payments into pending provisioning orders and successful proxy payments into pending activation records.
- [x] Add payment return handling with verifying, success, cancelled, and failure screens in the dashboard.
- [x] Add Paystack-powered direct service checkout while preserving the existing wallet ledger for account history.
- [x] Audit every intended website and dashboard button, replacing disabled or non-functional controls with working actions or explicit explanatory prompts.
- [x] Add Vitest coverage for fixed proxy pricing, payment reference validation, Paystack verification outcomes, and paid-service fulfillment.
- [x] Re-run TypeScript checks, tests, production build, and responsive visual inspection after payment integration.
- [x] Save and deliver a new verified project checkpoint containing the Paystack payment experience.
- [x] Adapt the attached deposit modal into the BOTPRESS dark-neon visual system rather than copying its light standalone styling.
- [x] Add a responsive deposit prompt with service context, authenticated customer details, amount input, quick amounts, close controls, focus handling, and keyboard dismissal.
- [x] Start deposit choices at a $1 service value and reject amounts below the configured local-currency equivalent.
- [x] Prefill authenticated name and email instead of using demo customer data.
- [x] Show a review receipt before redirect containing service, region/country, amount, settlement currency, and payment provider.
- [x] Keep Paystack initialization server-side and do not embed or log the provided live public key in application source.
- [x] Replace the attachment's frontend-only success callback with verified server-side payment status before showing success or fulfilling services.
- [x] Add deposit payment prompts for wallet top-up, virtual-number purchase, and proxy purchase using one reusable BOTPRESS checkout component.
- [x] Preserve cancel, retry, loading, error, verifying, and confirmed-payment states from the attached interaction concept.
- [x] Convert the three quick-service buttons into a fixed floating navigator that remains visible while scrolling on mobile and desktop.
- [x] Ensure the fixed navigator is compact, accessible, does not cover important content, and keeps Virtual Numbers, Bot Deployment, and Proxies fully clickable.
- [x] Add a quick-search field to the proxy selector so users can filter proxy types and regions quickly.
- [x] Make every Proxies shortcut open a focused proxy chooser before any purchase or dashboard redirect.
- [x] Show all four proxy types in the shortcut chooser and allow users to choose a type before selecting a country.
- [x] Add a country search field with matching country buttons to the shortcut proxy chooser.
- [x] Restyle the fixed Virtual Numbers, Bot Deployment, and Proxies navigator with a more polished responsive theme.

- [x] Replace the Paystack secret key and settlement settings, then validate the new checkout configuration.

// End of task-specific additions
تع

- [x] Validate the user's replacement Paystack key and publish a new checkpoint only if the live credential and project checks pass.

- [ ] Confirm all Paystack keys exposed in chat have been revoked; regenerated credentials are configured and validated.
