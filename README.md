# Awesome Browser Extension Development [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of the best tools, frameworks, libraries, and resources for building modern browser extensions (Chrome, Edge, Firefox, Safari) in 2026. Covers Manifest V3, cross-browser development with WXT and Plasmo, build tooling, testing, publishing automation, security, and growth.

<div align="center">

<a href="https://extensionbooster.net">
  <img src="https://extensionbooster.net/logo.webp" alt="Extension Booster" width="150" />
</a>

<h3>💎 &nbsp;DIAMOND SPONSOR&nbsp; 💎</h3>

<p>
  <b><a href="https://extensionbooster.net">Extension Booster</a></b><br/>
  <sub>The growth platform for extension and app developers</sub>
</p>

<p>
  <sub>⭐ Real reviews &nbsp;·&nbsp; 📊 Cross-marketplace analytics (Chrome · Edge · Android · Workspace) &nbsp;·&nbsp; 🔁 Manifest V2 to V3 converter</sub>
</p>

<a href="https://extensionbooster.net"><b>🚀 Start free at extensionbooster.net →</b></a>

</div>

## Contents

- [Official Documentation](#official-documentation)
- [Frameworks and Boilerplates](#frameworks-and-boilerplates)
- [Manifest V3 and Migration](#manifest-v3-and-migration)
- [Cross-Browser and Polyfills](#cross-browser-and-polyfills)
- [UI and Components](#ui-and-components)
- [Messaging and Storage](#messaging-and-storage)
- [Build Tools and Bundlers](#build-tools-and-bundlers)
- [Testing and Debugging](#testing-and-debugging)
- [Publishing and Store Automation](#publishing-and-store-automation)
- [Analytics and Monetization](#analytics-and-monetization)
- [Growth and Store Optimization](#growth-and-store-optimization)
- [Security and Privacy](#security-and-privacy)
- [Example Open-Source Extensions](#example-open-source-extensions)
- [Communities and Newsletters](#communities-and-newsletters)
- [Tools and Utilities](#tools-and-utilities)

---

## Official Documentation

The primary references maintained by browser vendors and standards bodies.

- [Chrome Extensions (Chrome for Developers)](https://developer.chrome.com/docs/extensions) - The definitive reference for Chrome extension APIs, manifest keys, permissions, and Manifest V3 architecture.
- [Chrome Extensions API Reference](https://developer.chrome.com/docs/extensions/reference/api) - Full API surface for all Chrome extension namespaces, with live examples and changelog.
- [Chrome Web Store Developer Docs](https://developer.chrome.com/docs/webstore) - Publishing guidelines, listing policies, review processes, and monetization options for the Chrome Web Store.
- [What's New in Chrome Extensions](https://developer.chrome.com/docs/extensions/whats-new) - Official changelog tracking new APIs, deprecations, and platform changes across Chrome versions.
- [MDN WebExtensions (Firefox)](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions) - Cross-browser WebExtensions API reference covering Firefox, Chrome, and Edge with compatibility tables.
- [Firefox Extension Workshop](https://extensionworkshop.com/) - Mozilla's guide for building, testing, and publishing Firefox add-ons, including Firefox-specific capabilities.
- [Microsoft Edge Extensions Docs](https://learn.microsoft.com/en-us/microsoft-edge/extensions/) - Microsoft Learn documentation covering Edge extension development, publishing to the Edge Add-ons store, and MV3 guidance.
- [Safari Web Extensions (Apple Developer)](https://developer.apple.com/documentation/safariservices/safari-web-extensions) - Apple's guide for building Safari extensions using the WebExtensions API, with Xcode packaging instructions.
- [Safari Extensions Overview (Apple)](https://developer.apple.com/safari/extensions/) - Landing page for all Safari extension types including web extensions, app extensions, and content blockers.

---

## Frameworks and Boilerplates

Purpose-built frameworks and starter templates that reduce extension setup time.

- [WXT](https://wxt.dev/) - Next-generation browser extension framework with HMR, auto-reloading, TypeScript-first design, and support for all major UI frameworks.
- [WXT GitHub](https://github.com/wxt-dev/wxt) - Source repository for WXT, with 7,000+ stars and active community on Discord.
- [Plasmo](https://www.plasmo.com/) - Battery-packed browser extension SDK with React/Vue/Svelte support, live reload, and built-in publishing workflows.
- [Plasmo GitHub](https://github.com/PlasmoHQ/plasmo) - Source repository for the Plasmo framework, including BPP (Browser Platform Publish) GitHub Action.
- [CRXJS Vite Plugin](https://crxjs.dev/vite-plugin/) - Vite plugin for Chrome/browser extensions with true HMR in content scripts, zero-config manifest handling, and MV3 support.
- [CRXJS GitHub](https://github.com/crxjs/chrome-extension-tools) - Source for the `@crxjs/vite-plugin` package and chrome-extension-tools monorepo.
- [Extension.js](https://extension.js.org/) - Zero-config, framework-agnostic browser extension framework with HMR for all extension contexts and first-class TypeScript support.
- [Extension.js GitHub](https://github.com/extension-js/extension.js) - Open-source MIT-licensed repository for Extension.js with React, Vue, Svelte, and Preact templates.
- [vite-plugin-web-extension](https://github.com/aklinker1/vite-plugin-web-extension) - Vite plugin that auto-builds all inputs from manifest.json and opens a browser for development with HMR.
- [vitesse-webext](https://github.com/antfu-collective/vitesse-webext) - Opinionated WebExtension starter built on Vite and Vue 3, by Anthony Fu, with webext-bridge messaging and VueUse storage.
- [chrome-extension-boilerplate-react-vite](https://github.com/Jonghakseo/chrome-extension-boilerplate-react-vite) - Chrome and Firefox extension boilerplate using React, Vite, TypeScript, and Turborepo for fast multi-package builds.
- [web-extension-starter](https://github.com/abhijithvijayan/web-extension-starter) - "Write once, run on any browser" extension starter with React, TypeScript, Vite, and cross-browser manifest generation.
- [browser-extension-template](https://github.com/fregante/browser-extension-template) - Minimal boilerplate with Parcel 2, webext-options-sync, and auto-publishing by fregante.

---

## Manifest V3 and Migration

Resources for understanding MV3 architecture and migrating from MV2.

- [What is Manifest V3? (Chrome)](https://developer.chrome.com/docs/extensions/develop/migrate/what-is-mv3) - Official overview of MV3 goals, key changes (service workers, declarativeNetRequest, CSP), and platform vision.
- [Migrate to Manifest V3 (Chrome)](https://developer.chrome.com/docs/extensions/develop/migrate) - Step-by-step migration guide covering background script changes, API substitutions, and manifest key updates.
- [MV3 Migration (Microsoft Edge)](https://learn.microsoft.com/en-us/microsoft-edge/extensions-chromium/developer-guide/manifest-v3) - Edge-specific MV3 overview and migration timeline mirroring Chrome's transition.
- [Resuming the Transition to MV3 (Chrome Blog)](https://developer.chrome.com/blog/resuming-the-transition-to-mv3) - Official blog post on MV2 deprecation timelines, including the June 2024 Chrome 127 enforcement rollout.
- [declarativeNetRequest API Reference](https://developer.chrome.com/docs/extensions/reference/api/declarativeNetRequest) - Full reference for the MV3 network-request filtering API that replaces the blocking webRequest API.
- [MV3 Migration Pitfalls (DEV Community)](https://dev.to/_350df62777eb55e1/manifest-v3-migration-pitfalls-lessons-from-17-chrome-extensions-2j3h) - Practical lessons from migrating 17 real extensions, covering service worker lifecycle, storage, and messaging edge cases.
- [Extension Booster MV2 to V3 Auto-Converter](https://extensionbooster.net) - Automated tool that converts Manifest V2 extensions to V3 format, available as part of the Extension Booster platform.

---

## Cross-Browser and Polyfills

Libraries and resources for writing extensions that work across Chrome, Firefox, Edge, and Safari.

- [webextension-polyfill (Mozilla)](https://github.com/mozilla/webextension-polyfill) - Lightweight Promise-based polyfill for the browser WebExtension API, enabling Firefox-style `browser.*` calls to work in Chrome.
- [Build a Cross-Browser Extension (MDN)](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Build_a_cross_browser_extension) - MDN guide covering strategy, namespace handling, API gaps, and testing across browsers.
- [webextension-toolbox](https://github.com/webextension-toolbox/webextension-toolbox) - Small CLI toolbox that compiles and validates extensions targeting Chrome, Firefox, Edge, and Safari from a single codebase.
- [Browser Compatibility (Firefox Extension Workshop)](https://extensionworkshop.com/documentation/develop/browser-compatibility/) - Firefox's reference for which WebExtension APIs are supported across browsers, with notes on Firefox-specific capabilities.
- [webextension-polyfill-ts](https://github.com/lusito/webextension-polyfill-ts) - TypeScript-ready wrapper around Mozilla's webextension-polyfill with full type definitions.

---

## UI and Components

Frameworks, patterns, and libraries for building popup, options, side panel, and content-script UIs.

- [shadcn/ui in Extensions (Extension.js docs)](https://extension.js.org/docs/integrations/shadcnui) - Guide for using shadcn/ui components inside browser extensions with Tailwind CSS and proper content-script isolation.
- [WXT Content Scripts UI Guide](https://wxt.dev/guide/essentials/content-scripts) - WXT documentation on injecting isolated UI into host pages using Shadow DOM to prevent style conflicts.
- [Headless UI](https://headlessui.com/) - Completely unstyled, accessible UI components for React and Vue, well-suited for extension popups and options pages.
- [Radix UI](https://www.radix-ui.com/) - Low-level, accessible UI primitives for React, used as the foundation for shadcn/ui and easy to adapt for extension contexts.
- [wxt-react-shadcn-tailwindcss-chrome-extension](https://github.com/imtiger/wxt-react-shadcn-tailwindcss-chrome-extension) - Reference boilerplate combining WXT, React, shadcn/ui, and Tailwind CSS with proper Shadow DOM isolation for content scripts.
- [vite-web-extension (JohnBra)](https://github.com/JohnBra/vite-web-extension) - Chrome and Firefox extension template using React 19, TypeScript, and Tailwind CSS with a focus on developer ergonomics.

---

## Messaging and Storage

Libraries for type-safe cross-context communication and storage in extensions.

- [webext-bridge](https://github.com/serversideup/webext-bridge) - Messaging library with batteries included for sending type-safe messages between background, content scripts, popup, devtools, and options pages.
- [@webext-core/messaging](https://webext-core.aklinker1.io/) - Lightweight, type-safe wrapper around extension messaging APIs, part of the webext-core collection.
- [@webext-core/storage](https://github.com/aklinker1/webext-core) - Type-safe, alternative storage API for browser extensions built on webextension-polyfill.
- [webext-storage-cache](https://github.com/fregante/webext-storage-cache) - Cache values in extension storage with automatic expiration and a memoize-like API for caching function results.
- [webext-options-sync](https://github.com/fregante/webext-options-sync) - Manages and auto-saves extension options forms with support for defaults and migrations across Chrome and Firefox.
- [webext-dynamic-content-scripts](https://github.com/fregante/webext-dynamic-content-scripts) - Automatically registers content scripts on domains added via optional permission grants at runtime.
- [webext-messenger (PixieBrix)](https://github.com/pixiebrix/webext-messenger) - Component-level messaging framework for browser extensions with type-safe RPC-style calls between contexts.

---

## Build Tools and Bundlers

Plugins and CLI tools for integrating browser extension builds into modern toolchains.

- [web-ext (Mozilla)](https://github.com/mozilla/web-ext) - Mozilla's official CLI for building, running, linting, and signing web extensions, with live-reload for Firefox and Chromium.
- [vite-plugin-web-extension (samrum)](https://github.com/samrum/vite-plugin-web-extension) - Vite plugin for generating cross-browser ES module-based extensions from a single manifest, supporting MV2 and MV3.
- [webpack-webextension-plugin](https://github.com/webextension-toolbox/webpack-webextension-plugin) - Webpack plugin that compiles WebExtension manifest.json files and adds smart auto-reload during development.
- [webext-fun (fregante)](https://github.com/fregante/webext-fun) - Collection of small, focused WebExtension utility packages covering patterns, permissions, content scripts, and tools.
- [webext-content-scripts](https://github.com/fregante/webext-content-scripts) - Utility functions for injecting content scripts programmatically from the background in both MV2 and MV3.

---

## Testing and Debugging

Tools for unit testing, end-to-end testing, and debugging browser extensions.

- [Playwright (Microsoft)](https://github.com/microsoft/playwright) - End-to-end testing framework supporting Chromium, Firefox, and WebKit, with official APIs for loading and testing extensions.
- [playwright-webextext](https://github.com/ueokande/playwright-webextext) - Playwright extension library for loading Firefox add-ons and Chromium extensions from the local filesystem in tests.
- [sinon-chrome](https://github.com/acvetkov/sinon-chrome) - Mocks all Chrome extension APIs using Sinon stubs, enabling unit testing of extension logic in Node.js without a browser.
- [@types/chrome](https://www.npmjs.com/package/@types/chrome) - TypeScript type definitions for the Chrome extension API, maintained by DefinitelyTyped.
- [webext-core in-memory polyfill](https://webext-core.aklinker1.io/) - In-memory implementation of webextension-polyfill for unit testing extension code outside a browser environment.
- [mdn/webextensions-examples](https://github.com/mdn/webextensions-examples) - Official Mozilla repository of working Firefox add-on examples covering common extension patterns and API usage.
- [Chrome DevTools Extensions Debugging](https://developer.chrome.com/docs/extensions/get-started) - Official guide to loading unpacked extensions, using the service worker inspector, and debugging content scripts in Chrome DevTools.

---

## Publishing and Store Automation

Tools for automating extension uploads and publishing to browser stores via CI/CD.

- [chrome-webstore-upload](https://github.com/fregante/chrome-webstore-upload) - Node.js library for uploading and publishing Chrome extensions to the Chrome Web Store via the Google API.
- [chrome-webstore-upload-cli](https://github.com/fregante/chrome-webstore-upload-cli) - CLI wrapper around chrome-webstore-upload for use in shell scripts and GitHub Actions workflows.
- [web-ext sign/publish](https://extensionworkshop.com/documentation/develop/getting-started-with-web-ext/) - Mozilla's web-ext CLI supports signing and submitting extensions to addons.mozilla.org via the AMO API.
- [wdzeng/edge-addon](https://github.com/wdzeng/edge-addon) - GitHub Action for publishing extensions to the Microsoft Edge Add-ons store using the Edge Add-ons API v1.1.
- [wdzeng/firefox-addon](https://github.com/wdzeng/firefox-addon) - GitHub Action for publishing new versions of Firefox add-ons to addons.mozilla.org using the AMO API.
- [Plasmo BPP (Browser Platform Publish)](https://docs.plasmo.com/framework/workflows/submit) - Plasmo's built-in GitHub Action for simultaneously submitting to Chrome Web Store, Firefox Add-ons, and Edge Add-ons.
- [WXT Publishing Guide](https://wxt.dev/guide/essentials/publishing.html) - WXT's built-in publishing CLI supporting Chrome Web Store, Firefox, and Edge in a single command.
- [Upload to Edge Add-ons (GitHub Marketplace)](https://github.com/marketplace/actions/upload-to-edge-add-ons) - Standalone GitHub Action for uploading extension packages directly to the Microsoft Edge Add-ons store.

---

## Analytics and Monetization

Privacy-respecting analytics and payment solutions designed for browser extensions.

- [ExtPay (ExtensionPay)](https://extensionpay.com/) - Payment and licensing service for browser extensions requiring no server, integrating with Stripe and supporting all major browsers.
- [ExtPay GitHub](https://github.com/Glench/ExtPay) - Open-source library for ExtensionPay.com with methods for checking paid status and opening payment pages from extension code.
- [Plausible Analytics](https://plausible.io/) - Privacy-friendly, cookie-free web analytics with a lightweight script, GDPR-compliant, usable from extension options or web app sidecars.
- [Umami](https://umami.is/) - Open-source, self-hostable privacy-focused analytics alternative to Google Analytics, suitable for extension landing pages and companion web apps.
- [PostHog](https://posthog.com/) - Open-source product analytics platform with session recording and feature flags, deployable self-hosted for full data control.

---

## Growth and Store Optimization

Tools and resources for growing installs, managing reviews, and optimizing store listings.

- [Extension Booster](https://extensionbooster.net) - All-in-one growth platform for browser extension and app developers: real user reviews, install and rating tracking, competitor analysis across Chrome, Edge, Android, and Google Workspace, plus MV2-to-V3 auto-conversion.
- [Chrome Web Store Listing Best Practices](https://developer.chrome.com/docs/webstore/best_listing) - Official Google guidance on writing compelling store descriptions, choosing screenshots, and improving discoverability.
- [Firefox Add-ons Listing Guide (Extension Workshop)](https://extensionworkshop.com/documentation/develop/best-practices-for-collecting-user-data-consents/) - Mozilla's best practices for user data consent disclosures, which directly affect listing approval and user trust.
- [App Store Optimization (ASO) for Extensions](https://developer.chrome.com/docs/webstore) - Chrome Web Store developer hub covering metadata, category selection, and performance metrics for store rankings.

---

## Security and Privacy

References and tools for writing secure, privacy-respecting browser extensions.

- [OWASP Browser Extension Vulnerabilities Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Browser_Extension_Vulnerabilities_Cheat_Sheet.html) - OWASP's structured reference covering XSS, excessive permissions, insecure storage, unsafe script loading, and mitigation strategies.
- [Content Security Policy for Extensions (Chrome)](https://developer.chrome.com/docs/extensions/reference/manifest/content-security-policy) - Chrome's reference for the `content_security_policy` manifest key, covering MV3 restrictions and allowed directives.
- [Content Security Policy for Extensions (MDN)](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Content_Security_Policy) - MDN guide explaining how CSP applies to extension pages, background scripts, and content scripts.
- [Content Security Policy for Extensions (Edge)](https://learn.microsoft.com/en-us/microsoft-edge/extensions/developer-guide/csp) - Microsoft's documentation on using CSP to control resource loading in Edge extensions.
- [Permissions Best Practices (Chrome)](https://developer.chrome.com/docs/extensions/develop/concepts/permission-warnings) - Official guide to minimizing permission footprint, using optional permissions, and writing clear permission rationale.
- [Firefox Extension Security Best Practices](https://extensionworkshop.com/documentation/develop/build-a-secure-extension/) - Mozilla's security guide covering data handling, secure communication, and permission minimization for Firefox extensions.

---

## Example Open-Source Extensions

Well-known, production-quality open-source extensions to learn from.

- [uBlock Origin](https://github.com/gorhill/uBlock) - Highly efficient ad and content blocker for Chromium and Firefox, a reference implementation for declarativeNetRequest and content script performance.
- [Dark Reader](https://github.com/darkreader/darkreader) - Dark mode extension for Chrome and Firefox using dynamic CSS theme generation; excellent example of large-scale content script architecture.
- [Vimium](https://github.com/philc/vimium) - Keyboard-driven browser navigation extension in the spirit of Vim; clean, minimal CoffeeScript/TypeScript codebase.
- [Refined GitHub](https://github.com/refined-github/refined-github) - Extension that enhances the GitHub UI with hundreds of micro-improvements; exemplary use of content scripts and MV3 patterns.
- [SponsorBlock](https://github.com/ajayyy/SponsorBlock) - Crowdsourced YouTube sponsor-skip extension demonstrating efficient background API calls, content script timing, and community data pipelines.
- [Bitwarden Clients](https://github.com/bitwarden/clients) - Official monorepo for Bitwarden's browser extension (Chrome, Firefox, Safari, Edge); shows Angular-based extension UI and secure storage patterns.
- [Wappalyzer (Open Source)](https://github.com/enthec/webappanalyzer) - Technology detection extension using content scripts and pattern matching; good example of large rule-set management.

---

## Communities and Newsletters

Places to ask questions, share projects, and stay current with the extension ecosystem.

- [r/chrome_extensions (Reddit)](https://www.reddit.com/r/chrome_extensions/) - Active subreddit for Chrome extension developers and users covering development questions, reviews, and updates.
- [r/firefox_extensions (Reddit)](https://www.reddit.com/r/firefox_extensions/) - Reddit community focused on Firefox add-on development and discovery.
- [Chromium Extensions Google Group](https://groups.google.com/a/chromium.org/g/chromium-extensions) - Official discussion group for Chrome extension developers, monitored by the Chrome extensions team.
- [Firefox Add-ons Community Forum (Mozilla Discourse)](https://discourse.mozilla.org/c/add-ons/35) - Mozilla's official forum for add-on developers, including API discussions, AMO policy, and announcement threads.
- [WXT Discord](https://wxt.dev/) - Active Discord community for the WXT framework, covering usage questions, framework development, and extension ecosystem discussions.
- [Plasmo Discord](https://www.plasmo.com/) - Plasmo's community Discord for framework questions, templates, and sharing extensions built with Plasmo.
- [Chrome for Developers Blog](https://developer.chrome.com/blog) - Official blog with monthly "What's happening in Chrome Extensions" posts and I/O recap articles.
- [Extension Workshop Blog (Mozilla)](https://extensionworkshop.com/blog/) - Mozilla's blog covering Firefox add-on news, policy updates, and developer spotlights.

---

## Tools and Utilities

Generators, validators, and standalone utilities that improve the extension development workflow.

- [Chrome Extension Icon Generator](https://alexleybourne.github.io/chrome-extension-icon-generator/) - Browser-based tool that generates all required icon sizes (16, 32, 48, 128 px) from a single uploaded image.
- [Chrome Extension Icon Generator GitHub](https://github.com/alexleybourne/chrome-extension-icon-generator) - Open-source repository for the icon generator tool.
- [Awesome-WebExtensions (fregante)](https://github.com/fregante/Awesome-WebExtensions) - Complementary curated list by fregante focused on small utility packages and libraries for the WebExtensions API.
- [webext-tools](https://github.com/fregante/webext-tools) - Small collection of utility functions for common WebExtension tasks such as getting the current tab or checking context.
- [webext-patterns](https://github.com/fregante/webext-patterns) - Utilities for working with match patterns and URL globs in browser extensions.
- [webext-inject-on-install](https://github.com/fregante/webext-inject-on-install) - Automatically injects content scripts into existing tabs when an extension is first installed, solving a common bootstrapping problem.
- [Manifest Validator (Mozilla Discourse)](https://discourse.mozilla.org/t/manifest-v3-validation-tools/102915) - Community thread discussing available manifest validation approaches for MV3 extensions.
- [webextension-toolbox generator](https://github.com/webextension-toolbox/generator-web-extension) - Yeoman generator that scaffolds a cross-browser extension project using webextension-toolbox as the compiler.
- [vite-plugin-web-extension (samrum) create CLI](https://github.com/samrum/create-vite-plugin-web-extension) - Interactive CLI for scaffolding new extension projects using `@samrum/vite-plugin-web-extension` with framework choice.

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for entry format rules, quality standards, and the pull request checklist. All suggestions welcome via issues or PRs.

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Released under the [MIT License](LICENSE). Copyright (c) 2026 Quang Phan.

---

<p align="center">
  <sub>Curated for developers · Powered by <a href="https://extensionbooster.net"><b>Extension Booster</b></a>, grow your extensions and apps with real reviews and cross-marketplace analytics.</sub>
</p>
