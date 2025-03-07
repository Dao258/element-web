Changes in [1.11.35](https://github.com/vector-im/element-web/releases/tag/v1.11.35) (2023-07-04)
=================================================================================================

## 🦖 Deprecations
 * Remove `feature_favourite_messages` as it is has been abandoned for now ([\#11097](https://github.com/matrix-org/matrix-react-sdk/pull/11097)). Fixes #25555.

## ✨ Features
 * Don't setup keys on login when encryption is force disabled ([\#11125](https://github.com/matrix-org/matrix-react-sdk/pull/11125)). Contributed by @kerryarchibald.
 * OIDC: attempt dynamic client registration ([\#11074](https://github.com/matrix-org/matrix-react-sdk/pull/11074)). Fixes #25468 and #25467. Contributed by @kerryarchibald.
 * OIDC: Check static client registration and add login flow ([\#11088](https://github.com/matrix-org/matrix-react-sdk/pull/11088)). Fixes #25467. Contributed by @kerryarchibald.
 * Improve message body output from plain text editor ([\#11124](https://github.com/matrix-org/matrix-react-sdk/pull/11124)). Contributed by @alunturner.
 * Disable encryption toggle in room settings when force disabled ([\#11122](https://github.com/matrix-org/matrix-react-sdk/pull/11122)). Contributed by @kerryarchibald.
 * Add .well-known config option to force disable encryption on room creation ([\#11120](https://github.com/matrix-org/matrix-react-sdk/pull/11120)). Contributed by @kerryarchibald.
 * Handle permalinks in room topic ([\#11115](https://github.com/matrix-org/matrix-react-sdk/pull/11115)). Fixes #23395.
 * Add at room avatar for RTE ([\#11106](https://github.com/matrix-org/matrix-react-sdk/pull/11106)). Contributed by @alunturner.
 * Remove new room breadcrumbs ([\#11104](https://github.com/matrix-org/matrix-react-sdk/pull/11104)).
 * Update rich text editor dependency and associated changes ([\#11098](https://github.com/matrix-org/matrix-react-sdk/pull/11098)). Contributed by @alunturner.
 * Implement new model, hooks and reconcilation code for new GYU notification settings ([\#11089](https://github.com/matrix-org/matrix-react-sdk/pull/11089)). Contributed by @justjanne.
 * Allow maintaining a different right panel width for thread panels ([\#11064](https://github.com/matrix-org/matrix-react-sdk/pull/11064)). Fixes #25487.
 * Make AppPermission pane scrollable ([\#10954](https://github.com/matrix-org/matrix-react-sdk/pull/10954)). Fixes #25438 and #25511. Contributed by @luixxiul.
 * Integrate compound design tokens ([\#11091](https://github.com/matrix-org/matrix-react-sdk/pull/11091)). Fixes vector-im/internal-planning#450.
 * Don't warn about the effects of redacting state events when redacting non-state-events ([\#11071](https://github.com/matrix-org/matrix-react-sdk/pull/11071)). Fixes #8478.
 * Allow specifying help URLs in config.json ([\#11070](https://github.com/matrix-org/matrix-react-sdk/pull/11070)). Fixes #15268.

## 🐛 Bug Fixes
 * Fix error when generating error for polling for updates ([\#25609](https://github.com/vector-im/element-web/pull/25609)).
 * Fix spurious notifications on non-live events ([\#11133](https://github.com/matrix-org/matrix-react-sdk/pull/11133)). Fixes #24336.
 * Prevent auto-translation within composer ([\#11114](https://github.com/matrix-org/matrix-react-sdk/pull/11114)). Fixes #25624.
 * Fix caret jump when backspacing into empty line at beginning of editor ([\#11128](https://github.com/matrix-org/matrix-react-sdk/pull/11128)). Fixes #22335.
 * Fix server picker not allowing you to switch from custom to default ([\#11127](https://github.com/matrix-org/matrix-react-sdk/pull/11127)). Fixes #25650.
 * Consider the unthreaded read receipt for Unread dot state ([\#11117](https://github.com/matrix-org/matrix-react-sdk/pull/11117)). Fixes #24229.
 * Increase RTE resilience ([\#11111](https://github.com/matrix-org/matrix-react-sdk/pull/11111)). Fixes #25277. Contributed by @alunturner.
 * Fix RoomView ignoring alias lookup errors due to them not knowing the roomId ([\#11099](https://github.com/matrix-org/matrix-react-sdk/pull/11099)). Fixes #24783 and #25562.
 * Fix style inconsistencies on SecureBackupPanel ([\#11102](https://github.com/matrix-org/matrix-react-sdk/pull/11102)). Fixes #25615. Contributed by @luixxiul.
 * Remove unknown MXIDs from invite suggestions ([\#11055](https://github.com/matrix-org/matrix-react-sdk/pull/11055)). Fixes #25446.
 * Reduce volume of ring sounds to normalised levels ([\#9143](https://github.com/matrix-org/matrix-react-sdk/pull/9143)). Contributed by @JMoVS.
 * Fix slash commands not being enabled in certain cases ([\#11090](https://github.com/matrix-org/matrix-react-sdk/pull/11090)). Fixes #25572.
 * Prevent escape in threads from sending focus to main timeline composer ([\#11061](https://github.com/matrix-org/matrix-react-sdk/pull/11061)). Fixes #23397.

Changes in [1.11.34](https://github.com/vector-im/element-web/releases/tag/v1.11.34) (2023-06-20)
=================================================================================================

## ✨ Features
 * OIDC: add delegatedauthentication to validated server config ([\#11053](https://github.com/matrix-org/matrix-react-sdk/pull/11053)). Contributed by @kerryarchibald.
 * Allow image pasting in plain mode in RTE ([\#11056](https://github.com/matrix-org/matrix-react-sdk/pull/11056)). Contributed by @alunturner.
 * Show room options menu if "UIComponent.roomOptionsMenu" is enabled ([\#10365](https://github.com/matrix-org/matrix-react-sdk/pull/10365)). Contributed by @maheichyk.
 * Allow image pasting in rich text mode in RTE ([\#11049](https://github.com/matrix-org/matrix-react-sdk/pull/11049)). Contributed by @alunturner.
 * Update voice broadcast redaction to use MSC3912 `with_rel_type` instead of `with_relations` ([\#11014](https://github.com/matrix-org/matrix-react-sdk/pull/11014)). Fixes #25471.
 * Add config to skip widget_build_url for DM rooms ([\#11044](https://github.com/matrix-org/matrix-react-sdk/pull/11044)). Fixes vector-im/customer-retainer#74.
 * Inhibit interactions on forward dialog message previews ([\#11025](https://github.com/matrix-org/matrix-react-sdk/pull/11025)). Fixes #23459.
 * Removed `DecryptionFailureBar.tsx` ([\#11027](https://github.com/matrix-org/matrix-react-sdk/pull/11027)). Fixes vector-im/element-meta#1358. Contributed by @florianduros.

## 🐛 Bug Fixes
 * Fix translucent `TextualEvent` on search results panel ([\#10810](https://github.com/matrix-org/matrix-react-sdk/pull/10810)). Fixes #25292. Contributed by @luixxiul.
 * Matrix matrix scheme permalink constructor not stripping query params ([\#11060](https://github.com/matrix-org/matrix-react-sdk/pull/11060)). Fixes #25535.
 * Fix: "manually verify by text" does nothing ([\#11059](https://github.com/matrix-org/matrix-react-sdk/pull/11059)). Fixes #25375. Contributed by @kerryarchibald.
 * Make group calls respect the ICE fallback setting ([\#11047](https://github.com/matrix-org/matrix-react-sdk/pull/11047)). Fixes vector-im/voip-internal#65.
 * Align list items on the tooltip to the start ([\#11041](https://github.com/matrix-org/matrix-react-sdk/pull/11041)). Fixes #25355. Contributed by @luixxiul.
 * Clear thread panel event permalink when changing rooms ([\#11024](https://github.com/matrix-org/matrix-react-sdk/pull/11024)). Fixes #25484.
 * Fix spinner placement on pinned widgets being reloaded ([\#10970](https://github.com/matrix-org/matrix-react-sdk/pull/10970)). Fixes #25431. Contributed by @luixxiul.

Changes in [1.11.33](https://github.com/vector-im/element-web/releases/tag/v1.11.33) (2023-06-09)
=================================================================================================

## 🐛 Bug Fixes
 * Bump matrix-react-sdk to v3.73.1 for matrix-js-sdk v26.0.1. Fixes #25526.

Changes in [1.11.32](https://github.com/vector-im/element-web/releases/tag/v1.11.32) (2023-06-06)
=================================================================================================

## ✨ Features
 * Redirect to the SSO page if `sso_redirect_options.on_welcome_page` is enabled and the URL hash is empty ([\#25495](https://github.com/vector-im/element-web/pull/25495)). Contributed by @dhenneke.
 * vector/index.html: Allow fetching blob urls ([\#25336](https://github.com/vector-im/element-web/pull/25336)). Contributed by @SuperKenVery.
 * When joining room in sub-space join the parents too ([\#11011](https://github.com/matrix-org/matrix-react-sdk/pull/11011)).
 * Include thread replies in message previews ([\#10631](https://github.com/matrix-org/matrix-react-sdk/pull/10631)). Fixes #23920.
 * Use semantic headings in space preferences ([\#11021](https://github.com/matrix-org/matrix-react-sdk/pull/11021)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings - Ignored users ([\#11006](https://github.com/matrix-org/matrix-react-sdk/pull/11006)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings - profile ([\#10973](https://github.com/matrix-org/matrix-react-sdk/pull/10973)). Fixes #25461. Contributed by @kerryarchibald.
 * Use semantic headings in user settings - account ([\#10972](https://github.com/matrix-org/matrix-react-sdk/pull/10972)). Contributed by @kerryarchibald.
 * Support `Insert from iPhone or iPad` in Safari ([\#10851](https://github.com/matrix-org/matrix-react-sdk/pull/10851)). Fixes #25327. Contributed by @SuperKenVery.
 * Specify supportedStages for User Interactive Auth ([\#10975](https://github.com/matrix-org/matrix-react-sdk/pull/10975)). Fixes #19605.
 * Pass device id to widgets ([\#10209](https://github.com/matrix-org/matrix-react-sdk/pull/10209)). Contributed by @Fox32.
 * Use semantic headings in user settings - discovery ([\#10838](https://github.com/matrix-org/matrix-react-sdk/pull/10838)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings -  Notifications ([\#10948](https://github.com/matrix-org/matrix-react-sdk/pull/10948)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings - spellcheck and language ([\#10959](https://github.com/matrix-org/matrix-react-sdk/pull/10959)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings Appearance ([\#10827](https://github.com/matrix-org/matrix-react-sdk/pull/10827)). Contributed by @kerryarchibald.
 * Use semantic heading in user settings Sidebar & Voip ([\#10782](https://github.com/matrix-org/matrix-react-sdk/pull/10782)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings Security ([\#10774](https://github.com/matrix-org/matrix-react-sdk/pull/10774)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings - integrations and account deletion ([\#10837](https://github.com/matrix-org/matrix-react-sdk/pull/10837)). Fixes #25378. Contributed by @kerryarchibald.
 * Use semantic headings in user settings Preferences ([\#10794](https://github.com/matrix-org/matrix-react-sdk/pull/10794)). Contributed by @kerryarchibald.
 * Use semantic headings in user settings Keyboard ([\#10793](https://github.com/matrix-org/matrix-react-sdk/pull/10793)). Contributed by @kerryarchibald.
 * RTE plain text mentions as pills ([\#10852](https://github.com/matrix-org/matrix-react-sdk/pull/10852)). Contributed by @alunturner.
 * Allow welcome.html logo to be replaced by config ([\#25339](https://github.com/vector-im/element-web/pull/25339)). Fixes #8636.
 * Use semantic headings in user settings Labs ([\#10773](https://github.com/matrix-org/matrix-react-sdk/pull/10773)). Contributed by @kerryarchibald.
 * Use semantic list elements for menu lists and tab lists ([\#10902](https://github.com/matrix-org/matrix-react-sdk/pull/10902)). Fixes #24928.
 * Fix aria-required-children axe violation ([\#10900](https://github.com/matrix-org/matrix-react-sdk/pull/10900)). Fixes #25342.
 * Enable pagination for overlay timelines ([\#10757](https://github.com/matrix-org/matrix-react-sdk/pull/10757)). Fixes vector-im/voip-internal#107.
 * Add tooltip to disabled invite button due to lack of permissions ([\#10869](https://github.com/matrix-org/matrix-react-sdk/pull/10869)). Fixes #9824.
 * Respect configured auth_header_logo_url for default Welcome page ([\#10870](https://github.com/matrix-org/matrix-react-sdk/pull/10870)).
 * Specify lazy loading for avatars ([\#10866](https://github.com/matrix-org/matrix-react-sdk/pull/10866)). Fixes #1983.
 * Room and user mentions for plain text editor ([\#10665](https://github.com/matrix-org/matrix-react-sdk/pull/10665)). Contributed by @alunturner.
 * Add audible notifcation on broadcast error ([\#10654](https://github.com/matrix-org/matrix-react-sdk/pull/10654)). Fixes #25132.
 * Fall back from server generated thumbnail to original image ([\#10853](https://github.com/matrix-org/matrix-react-sdk/pull/10853)).
 * Use semantically correct elements for room sublist context menu ([\#10831](https://github.com/matrix-org/matrix-react-sdk/pull/10831)). Fixes vector-im/customer-retainer#46.
 * Avoid calling prepareToEncrypt onKeyDown ([\#10828](https://github.com/matrix-org/matrix-react-sdk/pull/10828)).
 * Allows search to recognize full room links ([\#8275](https://github.com/matrix-org/matrix-react-sdk/pull/8275)). Contributed by @bolu-tife.
 * "Show rooms with unread messages first" should not be on by default for new users ([\#10820](https://github.com/matrix-org/matrix-react-sdk/pull/10820)). Fixes #25304. Contributed by @kerryarchibald.
 * Fix emitter handler leak in ThreadView ([\#10803](https://github.com/matrix-org/matrix-react-sdk/pull/10803)).
 * Add better error for email invites without identity server ([\#10739](https://github.com/matrix-org/matrix-react-sdk/pull/10739)). Fixes #16893.
 * Move reaction message previews out of labs ([\#10601](https://github.com/matrix-org/matrix-react-sdk/pull/10601)). Fixes #25083.
 * Sort muted rooms to the bottom of their section of the room list ([\#10592](https://github.com/matrix-org/matrix-react-sdk/pull/10592)). Fixes #25131. Contributed by @kerryarchibald.
 * Use semantic headings in user settings Help & About ([\#10752](https://github.com/matrix-org/matrix-react-sdk/pull/10752)). Contributed by @kerryarchibald.
 * use ExternalLink components for external links ([\#10758](https://github.com/matrix-org/matrix-react-sdk/pull/10758)). Contributed by @kerryarchibald.
 * Use semantic headings in space settings ([\#10751](https://github.com/matrix-org/matrix-react-sdk/pull/10751)). Contributed by @kerryarchibald.
 * Use semantic headings for room settings content ([\#10734](https://github.com/matrix-org/matrix-react-sdk/pull/10734)). Contributed by @kerryarchibald.

## 🐛 Bug Fixes
 * Use consistent fonts for Japanese text ([\#10980](https://github.com/matrix-org/matrix-react-sdk/pull/10980)). Fixes #22333 and #23899.
 * Fix: server picker validates unselected option ([\#11020](https://github.com/matrix-org/matrix-react-sdk/pull/11020)). Fixes #25488. Contributed by @kerryarchibald.
 * Fix room list notification badges going missing in compact layout ([\#11022](https://github.com/matrix-org/matrix-react-sdk/pull/11022)). Fixes #25372.
 * Fix call to `startSingleSignOn` passing enum in place of idpId ([\#10998](https://github.com/matrix-org/matrix-react-sdk/pull/10998)). Fixes #24953.
 * Remove hover effect from user name on a DM creation UI ([\#10887](https://github.com/matrix-org/matrix-react-sdk/pull/10887)). Fixes #25305. Contributed by @luixxiul.
 * Fix layout regression in public space invite dialog ([\#11009](https://github.com/matrix-org/matrix-react-sdk/pull/11009)). Fixes #25458.
 * Fix layout regression in session dropdown ([\#10999](https://github.com/matrix-org/matrix-react-sdk/pull/10999)). Fixes #25448.
 * Fix spacing regression in user settings - roles & permissions ([\#10993](https://github.com/matrix-org/matrix-react-sdk/pull/10993)). Fixes #25447 and #25451. Contributed by @kerryarchibald.
 * Fall back to receipt timestamp if we have no event (react-sdk part) ([\#10974](https://github.com/matrix-org/matrix-react-sdk/pull/10974)). Fixes #10954. Contributed by @andybalaam.
 * Fix: Room header 'view your device list' does not link to new session manager ([\#10979](https://github.com/matrix-org/matrix-react-sdk/pull/10979)). Fixes #25440. Contributed by @kerryarchibald.
 * Fix display of devices without encryption support in Settings dialog ([\#10977](https://github.com/matrix-org/matrix-react-sdk/pull/10977)). Fixes #25413.
 * Use aria descriptions instead of labels for TextWithTooltip ([\#10952](https://github.com/matrix-org/matrix-react-sdk/pull/10952)). Fixes #25398.
 * Use grapheme-splitter instead of lodash for saving emoji from being ripped apart ([\#10976](https://github.com/matrix-org/matrix-react-sdk/pull/10976)). Fixes #22196.
 * Fix: content overflow in settings subsection ([\#10960](https://github.com/matrix-org/matrix-react-sdk/pull/10960)). Fixes #25416. Contributed by @kerryarchibald.
 * Make `Privacy Notice` external link on integration manager ToS clickable ([\#10914](https://github.com/matrix-org/matrix-react-sdk/pull/10914)). Fixes #25384. Contributed by @luixxiul.
 * Ensure that open message context menus are updated when the event is sent ([\#10950](https://github.com/matrix-org/matrix-react-sdk/pull/10950)).
 * Ensure that open sticker picker dialogs are updated when the widget configuration is updated. ([\#10945](https://github.com/matrix-org/matrix-react-sdk/pull/10945)).
 * Fix big emoji in replies ([\#10932](https://github.com/matrix-org/matrix-react-sdk/pull/10932)). Fixes #24798.
 * Hide empty `MessageActionBar` on message edit history dialog ([\#10447](https://github.com/matrix-org/matrix-react-sdk/pull/10447)). Fixes #24903. Contributed by @luixxiul.
 * Fix roving tab index getting confused after dragging space order ([\#10901](https://github.com/matrix-org/matrix-react-sdk/pull/10901)).
 * Attempt a potential workaround for stuck notifs ([\#3384](https://github.com/matrix-org/matrix-js-sdk/pull/3384)). Fixes vector-im/element-web#25406. Contributed by @andybalaam.
 * Handle trailing dot FQDNs for domain-specific config.json files ([\#25351](https://github.com/vector-im/element-web/pull/25351)). Fixes #8858.
 * Ignore edits in message previews when they concern messages other than latest ([\#10868](https://github.com/matrix-org/matrix-react-sdk/pull/10868)). Fixes #14872.
 * Send correct receipts when viewing a room ([\#10864](https://github.com/matrix-org/matrix-react-sdk/pull/10864)). Fixes #25196.
 * Fix timeline search bar being overlapped by the right panel ([\#10809](https://github.com/matrix-org/matrix-react-sdk/pull/10809)). Fixes #25291. Contributed by @luixxiul.
 * Fix the state shown for call in rooms ([\#10833](https://github.com/matrix-org/matrix-react-sdk/pull/10833)).
 * Add string for membership event where both displayname & avatar change ([\#10880](https://github.com/matrix-org/matrix-react-sdk/pull/10880)). Fixes #18026.
 * Fix people space notification badge not updating for new DM invites ([\#10849](https://github.com/matrix-org/matrix-react-sdk/pull/10849)). Fixes #23248.
 * Fix regression in emoji picker order mangling after clearing filter ([\#10854](https://github.com/matrix-org/matrix-react-sdk/pull/10854)). Fixes #25323.
 * Fix: Edit history modal crash ([\#10834](https://github.com/matrix-org/matrix-react-sdk/pull/10834)). Fixes #25309. Contributed by @kerryarchibald.
 * Fix long room address and name not being clipped on room info card and update `_RoomSummaryCard.pcss` ([\#10811](https://github.com/matrix-org/matrix-react-sdk/pull/10811)). Fixes #25293. Contributed by @luixxiul.
 * Treat thumbnail upload failures as complete upload failures ([\#10829](https://github.com/matrix-org/matrix-react-sdk/pull/10829)). Fixes #7069.
 * Update finite automata to match user identifiers as per spec ([\#10798](https://github.com/matrix-org/matrix-react-sdk/pull/10798)). Fixes #25246.
 * Fix icon on empty notification panel ([\#10817](https://github.com/matrix-org/matrix-react-sdk/pull/10817)). Fixes #25298 and #25302. Contributed by @luixxiul.
 * Fix: Threads button is highlighted when I create a new room ([\#10819](https://github.com/matrix-org/matrix-react-sdk/pull/10819)). Fixes #25284. Contributed by @kerryarchibald.
 * Fix the top heading of notification panel ([\#10818](https://github.com/matrix-org/matrix-react-sdk/pull/10818)). Fixes #25303. Contributed by @luixxiul.
 * Fix the color of the verified E2EE icon on `RoomSummaryCard` ([\#10812](https://github.com/matrix-org/matrix-react-sdk/pull/10812)). Fixes #25295. Contributed by @luixxiul.
 * Fix: No feedback when waiting for the server on a /delete_devices request with SSO ([\#10795](https://github.com/matrix-org/matrix-react-sdk/pull/10795)). Fixes #23096. Contributed by @kerryarchibald.
 * Fix: reveal images when image previews are disabled ([\#10781](https://github.com/matrix-org/matrix-react-sdk/pull/10781)). Fixes #25271. Contributed by @kerryarchibald.
 * Fix accessibility issues around the room list and space panel ([\#10717](https://github.com/matrix-org/matrix-react-sdk/pull/10717)). Fixes #13345.
 * Ensure tooltip contents is linked via aria to the target element ([\#10729](https://github.com/matrix-org/matrix-react-sdk/pull/10729)). Fixes vector-im/customer-retainer#43.

Changes in [1.11.31](https://github.com/vector-im/element-web/releases/tag/v1.11.31) (2023-05-10)
=================================================================================================

## ✨ Features
 * Improve Content-Security-Policy ([\#25210](https://github.com/vector-im/element-web/pull/25210)).
 * Add UIFeature.locationSharing to hide location sharing ([\#10727](https://github.com/matrix-org/matrix-react-sdk/pull/10727)).
 * Memoize field validation results ([\#10714](https://github.com/matrix-org/matrix-react-sdk/pull/10714)).
 * Commands for plain text editor ([\#10567](https://github.com/matrix-org/matrix-react-sdk/pull/10567)). Contributed by @alunturner.
 * Allow 16 lines of text in the rich text editors ([\#10670](https://github.com/matrix-org/matrix-react-sdk/pull/10670)). Contributed by @alunturner.
 * Bail out of `RoomSettingsDialog` when room is not found ([\#10662](https://github.com/matrix-org/matrix-react-sdk/pull/10662)). Contributed by @kerryarchibald.
 * Element-R: Populate device list for right-panel ([\#10671](https://github.com/matrix-org/matrix-react-sdk/pull/10671)). Contributed by @florianduros.
 * Make existing and new issue URLs configurable ([\#10710](https://github.com/matrix-org/matrix-react-sdk/pull/10710)). Fixes #24424.
 * Fix usages of ARIA tabpanel ([\#10628](https://github.com/matrix-org/matrix-react-sdk/pull/10628)). Fixes #25016.
 * Element-R: Starting a DMs with a user ([\#10673](https://github.com/matrix-org/matrix-react-sdk/pull/10673)). Contributed by @florianduros.
 * ARIA Accessibility improvements ([\#10675](https://github.com/matrix-org/matrix-react-sdk/pull/10675)).
 * ARIA Accessibility improvements ([\#10674](https://github.com/matrix-org/matrix-react-sdk/pull/10674)).
 * Add arrow key controls to emoji and reaction pickers ([\#10637](https://github.com/matrix-org/matrix-react-sdk/pull/10637)). Fixes #17189.
 * Translate credits in help about section ([\#10676](https://github.com/matrix-org/matrix-react-sdk/pull/10676)).

## 🐛 Bug Fixes
 * Fix: reveal images when image previews are disabled ([\#10781](https://github.com/matrix-org/matrix-react-sdk/pull/10781)). Fixes #25271. Contributed by @kerryarchibald.
 * Fix autocomplete not resetting properly on message send ([\#10741](https://github.com/matrix-org/matrix-react-sdk/pull/10741)). Fixes #25170.
 * Fix start_sso not working with guests disabled ([\#10720](https://github.com/matrix-org/matrix-react-sdk/pull/10720)). Fixes #16624.
 * Fix soft crash with Element call widgets ([\#10684](https://github.com/matrix-org/matrix-react-sdk/pull/10684)).
 * Send correct receipt when marking a room as read ([\#10730](https://github.com/matrix-org/matrix-react-sdk/pull/10730)). Fixes #25207.
 * Offload some more waveform processing onto a worker ([\#9223](https://github.com/matrix-org/matrix-react-sdk/pull/9223)). Fixes #19756.
 * Consolidate login errors ([\#10722](https://github.com/matrix-org/matrix-react-sdk/pull/10722)). Fixes #17520.
 * Fix all rooms search generating permalinks to wrong room id ([\#10625](https://github.com/matrix-org/matrix-react-sdk/pull/10625)). Fixes #25115.
 * Posthog properly handle Analytics ID changing from under us ([\#10702](https://github.com/matrix-org/matrix-react-sdk/pull/10702)). Fixes #25187.
 * Fix Clock being read as an absolute time rather than duration ([\#10706](https://github.com/matrix-org/matrix-react-sdk/pull/10706)). Fixes #22582.
 * Properly translate errors in `ChangePassword.tsx` so they show up translated to the user but not in our logs ([\#10615](https://github.com/matrix-org/matrix-react-sdk/pull/10615)). Fixes #9597. Contributed by @MadLittleMods.
 * Honour feature toggles in guest mode ([\#10651](https://github.com/matrix-org/matrix-react-sdk/pull/10651)). Fixes #24513. Contributed by @andybalaam.
 * Fix default content in devtools event sender ([\#10699](https://github.com/matrix-org/matrix-react-sdk/pull/10699)). Contributed by @tulir.
 * Fix a crash when a call ends while you're in it ([\#10681](https://github.com/matrix-org/matrix-react-sdk/pull/10681)). Fixes #25153.
 * Fix lack of screen reader indication when triggering auto complete ([\#10664](https://github.com/matrix-org/matrix-react-sdk/pull/10664)). Fixes #11011.
 * Fix typing tile duplicating users ([\#10678](https://github.com/matrix-org/matrix-react-sdk/pull/10678)). Fixes #25165.
 * Fix wrong room topic tooltip position ([\#10667](https://github.com/matrix-org/matrix-react-sdk/pull/10667)). Fixes #25158.
 * Fix create subspace dialog not working ([\#10652](https://github.com/matrix-org/matrix-react-sdk/pull/10652)). Fixes #24882.

Changes in [1.11.30](https://github.com/vector-im/element-web/releases/tag/v1.11.30) (2023-04-25)
=================================================================================================

## 🔒 Security
 * Fixes for [CVE-2023-30609](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE-2023-30609) / GHSA-xv83-x443-7rmw

## ✨ Features
 * Pick sensible default option for phone country dropdown ([\#10627](https://github.com/matrix-org/matrix-react-sdk/pull/10627)). Fixes #3528.
 * Relate field validation tooltip via aria-describedby ([\#10522](https://github.com/matrix-org/matrix-react-sdk/pull/10522)). Fixes #24963.
 * Handle more completion types in rte autocomplete ([\#10560](https://github.com/matrix-org/matrix-react-sdk/pull/10560)). Contributed by @alunturner.
 * Show a tile for an unloaded predecessor room if it has via_servers ([\#10483](https://github.com/matrix-org/matrix-react-sdk/pull/10483)). Contributed by @andybalaam.
 * Exclude message timestamps from aria live region ([\#10584](https://github.com/matrix-org/matrix-react-sdk/pull/10584)). Fixes #5696.
 * Make composer format bar an aria toolbar ([\#10583](https://github.com/matrix-org/matrix-react-sdk/pull/10583)). Fixes #11283.
 * Improve accessibility of font slider ([\#10473](https://github.com/matrix-org/matrix-react-sdk/pull/10473)). Fixes #20168 and #24962.
 * fix file size display from kB to KB ([\#10561](https://github.com/matrix-org/matrix-react-sdk/pull/10561)). Fixes #24866. Contributed by @NSV1991.
 * Handle /me in rte ([\#10558](https://github.com/matrix-org/matrix-react-sdk/pull/10558)). Contributed by @alunturner.
 * bind html with switch for manage extension setting option ([\#10553](https://github.com/matrix-org/matrix-react-sdk/pull/10553)). Contributed by @NSV1991.
 * Handle command completions in RTE ([\#10521](https://github.com/matrix-org/matrix-react-sdk/pull/10521)). Contributed by @alunturner.
 * Add room and user avatars to rte ([\#10497](https://github.com/matrix-org/matrix-react-sdk/pull/10497)). Contributed by @alunturner.
 * Support for MSC3882 revision 1 ([\#10443](https://github.com/matrix-org/matrix-react-sdk/pull/10443)). Contributed by @hughns.
 * Check profiles before starting a DM ([\#10472](https://github.com/matrix-org/matrix-react-sdk/pull/10472)). Fixes #24830.
 * Quick settings: Change the copy / labels on the options ([\#10427](https://github.com/matrix-org/matrix-react-sdk/pull/10427)). Fixes #24522. Contributed by @justjanne.
 * Update rte autocomplete styling ([\#10503](https://github.com/matrix-org/matrix-react-sdk/pull/10503)). Contributed by @alunturner.

## 🐛 Bug Fixes
 * Fix create subspace dialog not working ([\#10652](https://github.com/matrix-org/matrix-react-sdk/pull/10652)). Fixes vector-im/element-web#24882
 * Fix multiple accessibility defects identified by AXE ([\#10606](https://github.com/matrix-org/matrix-react-sdk/pull/10606)).
 * Fix view source from edit history dialog always showing latest event ([\#10626](https://github.com/matrix-org/matrix-react-sdk/pull/10626)). Fixes #21859.
 * #21451 Fix WebGL disabled error message ([\#10589](https://github.com/matrix-org/matrix-react-sdk/pull/10589)). Contributed by @rashmitpankhania.
 * Properly translate errors in `AddThreepid.ts` so they show up translated to the user but not in our logs ([\#10432](https://github.com/matrix-org/matrix-react-sdk/pull/10432)). Contributed by @MadLittleMods.
 * Fix overflow on auth pages ([\#10605](https://github.com/matrix-org/matrix-react-sdk/pull/10605)). Fixes #19548.
 * Fix incorrect avatar background colour when using a custom theme ([\#10598](https://github.com/matrix-org/matrix-react-sdk/pull/10598)). Contributed by @jdauphant.
 * Remove dependency on `org.matrix.e2e_cross_signing` unstable feature ([\#10593](https://github.com/matrix-org/matrix-react-sdk/pull/10593)).
 * Update setting description to match reality ([\#10600](https://github.com/matrix-org/matrix-react-sdk/pull/10600)). Fixes #25106.
 * Fix no identity server in help & about settings ([\#10563](https://github.com/matrix-org/matrix-react-sdk/pull/10563)). Fixes #25077.
 * Fix: Images no longer reserve their space in the timeline correctly ([\#10571](https://github.com/matrix-org/matrix-react-sdk/pull/10571)). Fixes #25082. Contributed by @kerryarchibald.
 * Fix issues with inhibited accessible focus outlines ([\#10579](https://github.com/matrix-org/matrix-react-sdk/pull/10579)). Fixes #19742.
 * Fix read receipts falling from sky ([\#10576](https://github.com/matrix-org/matrix-react-sdk/pull/10576)). Fixes #25081.
 * Fix avatar text issue in rte ([\#10559](https://github.com/matrix-org/matrix-react-sdk/pull/10559)). Contributed by @alunturner.
 * fix resizer only work with left mouse click ([\#10546](https://github.com/matrix-org/matrix-react-sdk/pull/10546)). Contributed by @NSV1991.
 * Fix send two join requests when joining a room from spotlight search ([\#10534](https://github.com/matrix-org/matrix-react-sdk/pull/10534)). Fixes #25054.
 * Highlight event when any version triggered a highlight ([\#10502](https://github.com/matrix-org/matrix-react-sdk/pull/10502)). Fixes #24923 and #24970. Contributed by @kerryarchibald.
 * Fix spacing of headings of integration manager on General settings tab ([\#10232](https://github.com/matrix-org/matrix-react-sdk/pull/10232)). Fixes #24085. Contributed by @luixxiul.

Changes in [1.11.29](https://github.com/vector-im/element-web/releases/tag/v1.11.29) (2023-04-11)
=================================================================================================

## ✨ Features
 * Allow desktop app to expose recent rooms in UI integrations ([\#16940](https://github.com/vector-im/element-web/pull/16940)).
 * Add API params to mute audio and/or video in Jitsi calls by default ([\#24820](https://github.com/vector-im/element-web/pull/24820)). Contributed by @dhenneke.
 * Style mentions as pills in rich text editor ([\#10448](https://github.com/matrix-org/matrix-react-sdk/pull/10448)). Contributed by @alunturner.
 * Show room create icon if "UIComponent.roomCreation" is enabled ([\#10364](https://github.com/matrix-org/matrix-react-sdk/pull/10364)). Contributed by @maheichyk.
 * Mentions as links rte ([\#10463](https://github.com/matrix-org/matrix-react-sdk/pull/10463)). Contributed by @alunturner.
 * Better error handling in jump to date ([\#10405](https://github.com/matrix-org/matrix-react-sdk/pull/10405)). Contributed by @MadLittleMods.
 * Show "Invite" menu option if "UIComponent.sendInvites" is enabled. ([\#10363](https://github.com/matrix-org/matrix-react-sdk/pull/10363)). Contributed by @maheichyk.
 * Added `UserProfilesStore`, `LruCache` and user permalink profile caching ([\#10425](https://github.com/matrix-org/matrix-react-sdk/pull/10425)). Fixes #10559.
 * Mentions as links rte ([\#10422](https://github.com/matrix-org/matrix-react-sdk/pull/10422)). Contributed by @alunturner.
 * Implement MSC3952: intentional mentions ([\#9983](https://github.com/matrix-org/matrix-react-sdk/pull/9983)).
 * Implement MSC3973: Search users in the user directory with the Widget API ([\#10269](https://github.com/matrix-org/matrix-react-sdk/pull/10269)). Contributed by @dhenneke.
 * Permalinks to message are now displayed as pills ([\#10392](https://github.com/matrix-org/matrix-react-sdk/pull/10392)). Fixes #24751 and #24706.
 * Show search,dial,explore in filterContainer if "UIComponent.filterContainer" is enabled ([\#10381](https://github.com/matrix-org/matrix-react-sdk/pull/10381)). Contributed by @maheichyk.
 * Increase space panel collapse clickable area ([\#6084](https://github.com/matrix-org/matrix-react-sdk/pull/6084)). Fixes #17379. Contributed by @jaiwanth-v.
 * Add fallback for replies to Polls ([\#10380](https://github.com/matrix-org/matrix-react-sdk/pull/10380)). Fixes #24197. Contributed by @kerryarchibald.
 * Permalinks to rooms and users are now pillified ([\#10388](https://github.com/matrix-org/matrix-react-sdk/pull/10388)). Fixes #24825.
 * Poll history -  access poll history from room settings ([\#10356](https://github.com/matrix-org/matrix-react-sdk/pull/10356)). Contributed by @kerryarchibald.
 * Add API params to mute audio and/or video in Jitsi calls by default ([\#10376](https://github.com/matrix-org/matrix-react-sdk/pull/10376)). Contributed by @dhenneke.
 * Notifications: inline error message on notifications saving error ([\#10288](https://github.com/matrix-org/matrix-react-sdk/pull/10288)). Contributed by @kerryarchibald.
 * Support dynamic room predecessor in SpaceProvider ([\#10348](https://github.com/matrix-org/matrix-react-sdk/pull/10348)). Contributed by @andybalaam.
 * Support dynamic room predecessors for RoomProvider ([\#10346](https://github.com/matrix-org/matrix-react-sdk/pull/10346)). Contributed by @andybalaam.
 * Support dynamic room predecessors in OwnBeaconStore ([\#10339](https://github.com/matrix-org/matrix-react-sdk/pull/10339)). Contributed by @andybalaam.
 * Support dynamic room predecessors in ForwardDialog ([\#10344](https://github.com/matrix-org/matrix-react-sdk/pull/10344)). Contributed by @andybalaam.
 * Support dynamic room predecessors in SpaceHierarchy ([\#10341](https://github.com/matrix-org/matrix-react-sdk/pull/10341)). Contributed by @andybalaam.
 * Support dynamic room predecessors in AddExistingToSpaceDialog ([\#10342](https://github.com/matrix-org/matrix-react-sdk/pull/10342)). Contributed by @andybalaam.
 * Support dynamic room predecessors in leave-behaviour ([\#10340](https://github.com/matrix-org/matrix-react-sdk/pull/10340)). Contributed by @andybalaam.
 * Support dynamic room predecessors in StopGapWidgetDriver ([\#10338](https://github.com/matrix-org/matrix-react-sdk/pull/10338)). Contributed by @andybalaam.
 * Support dynamic room predecessors in WidgetLayoutStore ([\#10326](https://github.com/matrix-org/matrix-react-sdk/pull/10326)). Contributed by @andybalaam.
 * Support dynamic room predecessors in SpaceStore ([\#10332](https://github.com/matrix-org/matrix-react-sdk/pull/10332)). Contributed by @andybalaam.
 * Sync polls push rules on changes to account_data ([\#10287](https://github.com/matrix-org/matrix-react-sdk/pull/10287)). Contributed by @kerryarchibald.
 * Support dynamic room predecessors in BreadcrumbsStore ([\#10295](https://github.com/matrix-org/matrix-react-sdk/pull/10295)). Contributed by @andybalaam.
 * Improved a11y for Field feedback and Secure Phrase input ([\#10320](https://github.com/matrix-org/matrix-react-sdk/pull/10320)). Contributed by @Sebbones.
 * Support dynamic room predecessors in RoomNotificationStateStore ([\#10297](https://github.com/matrix-org/matrix-react-sdk/pull/10297)). Contributed by @andybalaam.

## 🐛 Bug Fixes
 * Use a newly generated access_token while joining Jitsi ([\#24646](https://github.com/vector-im/element-web/pull/24646)). Fixes #24687. Contributed by @emrahcom.
 * Fix cloudflare action pointing at commit hash instead of tag ([\#24777](https://github.com/vector-im/element-web/pull/24777)). Contributed by @justjanne.
 * Allow editing with RTE to overflow for autocomplete visibility ([\#10499](https://github.com/matrix-org/matrix-react-sdk/pull/10499)). Contributed by @alunturner.
 * Added auto focus to Github URL on opening of debug logs modal ([\#10479](https://github.com/matrix-org/matrix-react-sdk/pull/10479)). Contributed by @ShivamSpm.
 * Fix detection of encryption for all users in a room ([\#10487](https://github.com/matrix-org/matrix-react-sdk/pull/10487)). Fixes #24995.
 * Properly generate mentions when editing a reply with MSC3952 ([\#10486](https://github.com/matrix-org/matrix-react-sdk/pull/10486)). Fixes #24924. Contributed by @kerryarchibald.
 * Improve performance of rendering a room with many hidden events ([\#10131](https://github.com/matrix-org/matrix-react-sdk/pull/10131)). Contributed by @andybalaam.
 * Prevent future date selection in jump to date ([\#10419](https://github.com/matrix-org/matrix-react-sdk/pull/10419)). Fixes #20800. Contributed by @MadLittleMods.
 * Add aria labels to message search bar to improve accessibility ([\#10476](https://github.com/matrix-org/matrix-react-sdk/pull/10476)). Fixes #24921.
 * Fix decryption failure bar covering the timeline ([\#10360](https://github.com/matrix-org/matrix-react-sdk/pull/10360)). Fixes #24780 #24074 and #24183. Contributed by @luixxiul.
 * Improve profile picture settings accessibility ([\#10470](https://github.com/matrix-org/matrix-react-sdk/pull/10470)). Fixes #24919.
 * Handle group call redaction ([\#10465](https://github.com/matrix-org/matrix-react-sdk/pull/10465)).
 * Display relative timestamp for threads on the same calendar day ([\#10399](https://github.com/matrix-org/matrix-react-sdk/pull/10399)). Fixes #24841. Contributed by @kerryarchibald.
 * Fix timeline list and paragraph display issues ([\#10424](https://github.com/matrix-org/matrix-react-sdk/pull/10424)). Fixes #24602. Contributed by @alunturner.
 * Use unique keys for voice broadcast pips ([\#10457](https://github.com/matrix-org/matrix-react-sdk/pull/10457)). Fixes #24959.
 * Fix "show read receipts sent by other users" not applying to threads ([\#10445](https://github.com/matrix-org/matrix-react-sdk/pull/10445)). Fixes #24910.
 * Fix joining public rooms without aliases in search dialog ([\#10437](https://github.com/matrix-org/matrix-react-sdk/pull/10437)). Fixes #23937.
 * Add input validation for `m.direct` in `DMRoomMap` ([\#10436](https://github.com/matrix-org/matrix-react-sdk/pull/10436)). Fixes #24909.
 * Reduce height reserved for "collapse" button's line on IRC layout ([\#10211](https://github.com/matrix-org/matrix-react-sdk/pull/10211)). Fixes #24605. Contributed by @luixxiul.
 * Fix `creatorUserId is required` error when opening sticker picker ([\#10423](https://github.com/matrix-org/matrix-react-sdk/pull/10423)).
 * Fix block/inline Element descendants error noise in `NewRoomIntro.tsx` ([\#10412](https://github.com/matrix-org/matrix-react-sdk/pull/10412)). Contributed by @MadLittleMods.
 * Fix profile resizer to make first character of a line selectable in IRC layout ([\#10396](https://github.com/matrix-org/matrix-react-sdk/pull/10396)). Fixes #14764. Contributed by @luixxiul.
 * Ensure space between wrapped lines of room name on IRC layout ([\#10188](https://github.com/matrix-org/matrix-react-sdk/pull/10188)). Fixes #24742. Contributed by @luixxiul.
 * Remove unreadable alt attribute from the room status bar warning icon (nonsense to screenreaders) ([\#10402](https://github.com/matrix-org/matrix-react-sdk/pull/10402)). Contributed by @MadLittleMods.
 * Fix big date separators when jump to date is enabled ([\#10404](https://github.com/matrix-org/matrix-react-sdk/pull/10404)). Fixes #22969. Contributed by @MadLittleMods.
 * Fixes user authentication when registering via the module API ([\#10257](https://github.com/matrix-org/matrix-react-sdk/pull/10257)). Contributed by @maheichyk.
 * Handle more edge cases in Space Hierarchy ([\#10280](https://github.com/matrix-org/matrix-react-sdk/pull/10280)). Contributed by @justjanne.
 * Further improve performance with lots of hidden events ([\#10353](https://github.com/matrix-org/matrix-react-sdk/pull/10353)). Fixes #24480. Contributed by @andybalaam.
 * Respect user cancelling upload flow by dismissing spinner ([\#10373](https://github.com/matrix-org/matrix-react-sdk/pull/10373)). Fixes #24667.
 * When starting a DM, the end-to-end encryption status icon does now only appear if the DM can be encrypted ([\#10394](https://github.com/matrix-org/matrix-react-sdk/pull/10394)). Fixes #24397.
 * Fix `[object Object]` in feedback metadata ([\#10390](https://github.com/matrix-org/matrix-react-sdk/pull/10390)).
 * Fix pinned messages card saying nothing pinned while loading ([\#10385](https://github.com/matrix-org/matrix-react-sdk/pull/10385)). Fixes #24615.
 * Fix import e2e key dialog staying disabled after paste ([\#10375](https://github.com/matrix-org/matrix-react-sdk/pull/10375)). Fixes #24818.
 * Show all labs even if incompatible, with appropriate tooltip explaining requirements ([\#10369](https://github.com/matrix-org/matrix-react-sdk/pull/10369)). Fixes #24813.
 * Fix UIFeature.Registration not applying to all paths ([\#10371](https://github.com/matrix-org/matrix-react-sdk/pull/10371)). Fixes #24814.
 * Clicking on a user pill does now only open the profile in the right panel and no longer navigates to the home view. ([\#10359](https://github.com/matrix-org/matrix-react-sdk/pull/10359)). Fixes #24797.
 * Fix start DM with pending third party invite ([\#10347](https://github.com/matrix-org/matrix-react-sdk/pull/10347)). Fixes #24781.
 * Fix long display name overflowing reply tile on IRC layout ([\#10343](https://github.com/matrix-org/matrix-react-sdk/pull/10343)). Fixes #24738. Contributed by @luixxiul.
 * Display redacted body on ThreadView in the same way as normal messages ([\#9016](https://github.com/matrix-org/matrix-react-sdk/pull/9016)). Fixes #24729. Contributed by @luixxiul.
 * Handle more edge cases in ACL updates ([\#10279](https://github.com/matrix-org/matrix-react-sdk/pull/10279)). Contributed by @justjanne.
 * Allow parsing png files to fail if thumbnailing is successful ([\#10308](https://github.com/matrix-org/matrix-react-sdk/pull/10308)).

Changes in [1.11.28](https://github.com/vector-im/element-web/releases/tag/v1.11.28) (2023-03-31)
=================================================================================================

## 🐛 Bug Fixes
 * (No changes, version bumped to sync with element-desktop.)

Changes in [1.11.27](https://github.com/vector-im/element-web/releases/tag/v1.11.27) (2023-03-31)
=================================================================================================

## 🐛 Bug Fixes
 * Fix detection of encryption for all users in a room ([\#10487](https://github.com/matrix-org/matrix-react-sdk/pull/10487)). Fixes #24995.

Changes in [1.11.26](https://github.com/vector-im/element-web/releases/tag/v1.11.26) (2023-03-28)
=================================================================================================

## 🔒 Security
 * Fixes for [CVE-2023-28427](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE-2023-28427) / GHSA-mwq8-fjpf-c2gr
 * Fixes for [CVE-2023-28103](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE-2023-28103) / GHSA-6g43-88cp-w5gv

Changes in [1.11.25](https://github.com/vector-im/element-web/releases/tag/v1.11.25) (2023-03-15)
=================================================================================================

## ✨ Features
 * Remove experimental PWA support for Firefox and Safari ([\#24630](https://github.com/vector-im/element-web/pull/24630)).
 * Only allow to start a DM with one email if encryption by default is enabled ([\#10253](https://github.com/matrix-org/matrix-react-sdk/pull/10253)). Fixes #23133.
 * DM rooms are now encrypted if encryption by default is enabled and only inviting a single email address. Any action in the result DM room will be blocked until the other has joined. ([\#10229](https://github.com/matrix-org/matrix-react-sdk/pull/10229)).
 * Reduce bottom margin of ReplyChain on compact modern layout ([\#8972](https://github.com/matrix-org/matrix-react-sdk/pull/8972)). Fixes #22748. Contributed by @luixxiul.
 * Support for v2 of MSC3903 ([\#10165](https://github.com/matrix-org/matrix-react-sdk/pull/10165)). Contributed by @hughns.
 * When starting a DM, existing rooms with pending third-party invites will be reused. ([\#10256](https://github.com/matrix-org/matrix-react-sdk/pull/10256)). Fixes #23139.
 * Polls push rules: synchronise poll rules with message rules ([\#10263](https://github.com/matrix-org/matrix-react-sdk/pull/10263)). Contributed by @kerryarchibald.
 * New verification request toast button labels ([\#10259](https://github.com/matrix-org/matrix-react-sdk/pull/10259)).
 * Remove padding around integration manager iframe ([\#10148](https://github.com/matrix-org/matrix-react-sdk/pull/10148)).
 * Fix block code styling in rich text editor ([\#10246](https://github.com/matrix-org/matrix-react-sdk/pull/10246)). Contributed by @alunturner.
 * Poll history: fetch more poll history ([\#10235](https://github.com/matrix-org/matrix-react-sdk/pull/10235)). Contributed by @kerryarchibald.
 * Sort short/exact emoji matches before longer incomplete matches ([\#10212](https://github.com/matrix-org/matrix-react-sdk/pull/10212)). Fixes #23210. Contributed by @grimhilt.
 * Poll history: detail screen ([\#10172](https://github.com/matrix-org/matrix-react-sdk/pull/10172)). Contributed by @kerryarchibald.
 * Provide a more detailed error message than "No known servers" ([\#6048](https://github.com/matrix-org/matrix-react-sdk/pull/6048)). Fixes #13247. Contributed by @aaronraimist.
 * Say when a call was answered from a different device ([\#10224](https://github.com/matrix-org/matrix-react-sdk/pull/10224)).
 * Widget permissions customizations using module api ([\#10121](https://github.com/matrix-org/matrix-react-sdk/pull/10121)). Contributed by @maheichyk.
 * Fix copy button icon overlapping with copyable text ([\#10227](https://github.com/matrix-org/matrix-react-sdk/pull/10227)). Contributed by @Adesh-Pandey.
 * Support joining non-peekable rooms via the module API ([\#10154](https://github.com/matrix-org/matrix-react-sdk/pull/10154)). Contributed by @maheichyk.
 * The "new login" toast does now display the same device information as in the settings. "No" does now open the device settings. "Yes, it was me" dismisses the toast. ([\#10200](https://github.com/matrix-org/matrix-react-sdk/pull/10200)).
 * Do not prompt for a password when doing a „reset all“ after login ([\#10208](https://github.com/matrix-org/matrix-react-sdk/pull/10208)).

## 🐛 Bug Fixes
 * Fix incorrect copy in space creation flow ([\#10296](https://github.com/matrix-org/matrix-react-sdk/pull/10296)). Fixes #24741.
 * Fix space settings dialog having rogue title tooltip ([\#10293](https://github.com/matrix-org/matrix-react-sdk/pull/10293)). Fixes #24740.
 * Show spinner when starting a DM from the user profile (right panel) ([\#10290](https://github.com/matrix-org/matrix-react-sdk/pull/10290)).
 * Reduce height of toggle on expanded view source event ([\#10283](https://github.com/matrix-org/matrix-react-sdk/pull/10283)). Fixes #22873. Contributed by @luixxiul.
 * Pillify http and non-prefixed matrix.to links ([\#10277](https://github.com/matrix-org/matrix-react-sdk/pull/10277)). Fixes #20844.
 * Fix some features not being configurable via `features` ([\#10276](https://github.com/matrix-org/matrix-react-sdk/pull/10276)).
 * Fix starting a DM from the right panel in some cases ([\#10278](https://github.com/matrix-org/matrix-react-sdk/pull/10278)). Fixes #24722.
 * Align info EventTile and normal EventTile on IRC layout ([\#10197](https://github.com/matrix-org/matrix-react-sdk/pull/10197)). Fixes #22782. Contributed by @luixxiul.
 * Fix blowout of waveform of the voice message player on narrow UI ([\#8861](https://github.com/matrix-org/matrix-react-sdk/pull/8861)). Fixes #22604. Contributed by @luixxiul.
 * Fix the hidden view source toggle on IRC layout ([\#10266](https://github.com/matrix-org/matrix-react-sdk/pull/10266)). Fixes #22872. Contributed by @luixxiul.
 * Fix buttons on the room header being compressed due to long room name ([\#10155](https://github.com/matrix-org/matrix-react-sdk/pull/10155)). Contributed by @luixxiul.
 * Use the room avatar as a placeholder in calls ([\#10231](https://github.com/matrix-org/matrix-react-sdk/pull/10231)).
 * Fix calls showing as 'connecting' after hangup ([\#10223](https://github.com/matrix-org/matrix-react-sdk/pull/10223)).
 * Prevent multiple Jitsi calls started at the same time ([\#10183](https://github.com/matrix-org/matrix-react-sdk/pull/10183)). Fixes #23009.
 * Make localization keys compatible with agglutinative and/or SOV type languages ([\#10159](https://github.com/matrix-org/matrix-react-sdk/pull/10159)). Contributed by @luixxiul.

Changes in [1.11.24](https://github.com/vector-im/element-web/releases/tag/v1.11.24) (2023-02-28)
=================================================================================================

## ✨ Features
 * Display "The sender has blocked you from receiving this message" error message instead of "Unable to decrypt message" ([\#10202](https://github.com/matrix-org/matrix-react-sdk/pull/10202)). Contributed by @florianduros.
 * Polls: show warning about undecryptable relations ([\#10179](https://github.com/matrix-org/matrix-react-sdk/pull/10179)). Contributed by @kerryarchibald.
 * Poll history: fetch last 30 days of polls ([\#10157](https://github.com/matrix-org/matrix-react-sdk/pull/10157)). Contributed by @kerryarchibald.
 * Poll history - ended polls list items ([\#10119](https://github.com/matrix-org/matrix-react-sdk/pull/10119)). Contributed by @kerryarchibald.
 * Remove threads labs flag and the ability to disable threads ([\#9878](https://github.com/matrix-org/matrix-react-sdk/pull/9878)). Fixes #24365.
 * Show a success dialog after setting up the key backup ([\#10177](https://github.com/matrix-org/matrix-react-sdk/pull/10177)). Fixes #24487.
 * Release Sign in with QR out of labs ([\#10182](https://github.com/matrix-org/matrix-react-sdk/pull/10182)). Contributed by @hughns.
 * Hide indent button in rte ([\#10149](https://github.com/matrix-org/matrix-react-sdk/pull/10149)). Contributed by @alunturner.
 * Add option to find own location in map views ([\#10083](https://github.com/matrix-org/matrix-react-sdk/pull/10083)).
 * Render poll end events in timeline ([\#10027](https://github.com/matrix-org/matrix-react-sdk/pull/10027)). Contributed by @kerryarchibald.

## 🐛 Bug Fixes
 * Stop access token overflowing the box ([\#10069](https://github.com/matrix-org/matrix-react-sdk/pull/10069)). Fixes #24023. Contributed by @sbjaj33.
 * Add link to next file in the export ([\#10190](https://github.com/matrix-org/matrix-react-sdk/pull/10190)). Fixes #20272. Contributed by @grimhilt.
 * Ended poll tiles: add ended the poll message ([\#10193](https://github.com/matrix-org/matrix-react-sdk/pull/10193)). Fixes #24579. Contributed by @kerryarchibald.
 * Fix accidentally inverted condition for room ordering ([\#10178](https://github.com/matrix-org/matrix-react-sdk/pull/10178)). Fixes #24527. Contributed by @justjanne.
 * Re-focus the composer on dialogue quit ([\#10007](https://github.com/matrix-org/matrix-react-sdk/pull/10007)). Fixes #22832. Contributed by @Ashu999.
 * Try to resolve emails before creating a DM ([\#10164](https://github.com/matrix-org/matrix-react-sdk/pull/10164)).
 * Disable poll response loading test ([\#10168](https://github.com/matrix-org/matrix-react-sdk/pull/10168)). Contributed by @justjanne.
 * Fix email lookup in invite dialog ([\#10150](https://github.com/matrix-org/matrix-react-sdk/pull/10150)). Fixes #23353.
 * Remove duplicate white space characters from translation keys ([\#10152](https://github.com/matrix-org/matrix-react-sdk/pull/10152)). Contributed by @luixxiul.
 * Fix the caption of new sessions manager on Labs settings page for localization ([\#10143](https://github.com/matrix-org/matrix-react-sdk/pull/10143)). Contributed by @luixxiul.
 * Prevent start another DM with a user if one already exists ([\#10127](https://github.com/matrix-org/matrix-react-sdk/pull/10127)). Fixes #23138.
 * Remove white space characters before the horizontal ellipsis ([\#10130](https://github.com/matrix-org/matrix-react-sdk/pull/10130)). Contributed by @luixxiul.
 * Fix Selectable Text on 'Delete All' and 'Retry All' Buttons ([\#10128](https://github.com/matrix-org/matrix-react-sdk/pull/10128)). Fixes #23232. Contributed by @akshattchhabra.
 * Correctly Identify emoticons ([\#10108](https://github.com/matrix-org/matrix-react-sdk/pull/10108)). Fixes #19472. Contributed by @adarsh-sgh.
 * Remove a redundant white space ([\#10129](https://github.com/matrix-org/matrix-react-sdk/pull/10129)). Contributed by @luixxiul.

Changes in [1.11.23](https://github.com/vector-im/element-web/releases/tag/v1.11.23) (2023-02-14)
=================================================================================================

## ✨ Features
 * Description of QR code sign in labs feature ([\#23513](https://github.com/vector-im/element-web/pull/23513)). Contributed by @hughns.
 * Add option to find own location in map views ([\#10083](https://github.com/matrix-org/matrix-react-sdk/pull/10083)).
 * Render poll end events in timeline ([\#10027](https://github.com/matrix-org/matrix-react-sdk/pull/10027)). Contributed by @kerryarchibald.
 * Indicate unread messages in tab title ([\#10096](https://github.com/matrix-org/matrix-react-sdk/pull/10096)). Contributed by @tnt7864.
 * Open message in editing mode when keyboard up is pressed (RTE) ([\#10079](https://github.com/matrix-org/matrix-react-sdk/pull/10079)). Contributed by @florianduros.
 * Hide superseded rooms from the room list using dynamic room predecessors ([\#10068](https://github.com/matrix-org/matrix-react-sdk/pull/10068)). Contributed by @andybalaam.
 * Support MSC3946 in RoomListStore ([\#10054](https://github.com/matrix-org/matrix-react-sdk/pull/10054)). Fixes #24325. Contributed by @andybalaam.
 * Auto focus security key field ([\#10048](https://github.com/matrix-org/matrix-react-sdk/pull/10048)).
 * use Poll model with relations API in poll rendering ([\#9877](https://github.com/matrix-org/matrix-react-sdk/pull/9877)). Contributed by @kerryarchibald.
 * Support MSC3946 in the RoomCreate tile ([\#10041](https://github.com/matrix-org/matrix-react-sdk/pull/10041)). Fixes #24323. Contributed by @andybalaam.
 * Update labs flag description for RTE ([\#10058](https://github.com/matrix-org/matrix-react-sdk/pull/10058)). Contributed by @florianduros.
 * Change ul list style to disc when editing message ([\#10043](https://github.com/matrix-org/matrix-react-sdk/pull/10043)). Contributed by @alunturner.
 * Improved click detection within PiP windows ([\#10040](https://github.com/matrix-org/matrix-react-sdk/pull/10040)). Fixes #24371.
 * Add RTE keyboard navigation in editing ([\#9980](https://github.com/matrix-org/matrix-react-sdk/pull/9980)). Fixes #23621. Contributed by @florianduros.
 * Paragraph integration for rich text editor ([\#10008](https://github.com/matrix-org/matrix-react-sdk/pull/10008)). Contributed by @alunturner.
 * Add  indentation increasing/decreasing to RTE ([\#10034](https://github.com/matrix-org/matrix-react-sdk/pull/10034)). Contributed by @florianduros.
 * Add ignore user confirmation dialog ([\#6116](https://github.com/matrix-org/matrix-react-sdk/pull/6116)). Fixes #14746.
 * Use monospace font for room, message IDs in View Source modal ([\#9956](https://github.com/matrix-org/matrix-react-sdk/pull/9956)). Fixes #21937. Contributed by @paragpoddar.
 * Implement MSC3946 for AdvancedRoomSettingsTab ([\#9995](https://github.com/matrix-org/matrix-react-sdk/pull/9995)). Fixes #24322. Contributed by @andybalaam.
 * Implementation of MSC3824 to make the client OIDC-aware ([\#8681](https://github.com/matrix-org/matrix-react-sdk/pull/8681)). Contributed by @hughns.
 * Improves a11y for avatar uploads ([\#9985](https://github.com/matrix-org/matrix-react-sdk/pull/9985)). Contributed by @GoodGuyMarco.
 * Add support for [token authenticated registration](https ([\#7275](https://github.com/matrix-org/matrix-react-sdk/pull/7275)). Fixes #18931. Contributed by @govynnus.

## 🐛 Bug Fixes
 * Jitsi requests 'requires_client' capability if auth token is provided ([\#24294](https://github.com/vector-im/element-web/pull/24294)). Contributed by @maheichyk.
 * Remove duplicate white space characters from translation keys ([\#10152](https://github.com/matrix-org/matrix-react-sdk/pull/10152)). Contributed by @luixxiul.
 * Fix the caption of new sessions manager on Labs settings page for localization ([\#10143](https://github.com/matrix-org/matrix-react-sdk/pull/10143)). Contributed by @luixxiul.
 * Prevent start another DM with a user if one already exists ([\#10127](https://github.com/matrix-org/matrix-react-sdk/pull/10127)). Fixes #23138.
 * Remove white space characters before the horizontal ellipsis ([\#10130](https://github.com/matrix-org/matrix-react-sdk/pull/10130)). Contributed by @luixxiul.
 * Fix Selectable Text on 'Delete All' and 'Retry All' Buttons ([\#10128](https://github.com/matrix-org/matrix-react-sdk/pull/10128)). Fixes #23232. Contributed by @akshattchhabra.
 * Correctly Identify emoticons ([\#10108](https://github.com/matrix-org/matrix-react-sdk/pull/10108)). Fixes #19472. Contributed by @adarsh-sgh.
 * Should open new 1:1 chat room after leaving the old one ([\#9880](https://github.com/matrix-org/matrix-react-sdk/pull/9880)). Contributed by @ahmadkadri.
 * Remove a redundant white space ([\#10129](https://github.com/matrix-org/matrix-react-sdk/pull/10129)). Contributed by @luixxiul.
 * Fix a crash when removing persistent widgets (updated) ([\#10099](https://github.com/matrix-org/matrix-react-sdk/pull/10099)). Fixes #24412. Contributed by @andybalaam.
 * Fix wrongly grouping 3pid invites into a single repeated transition ([\#10087](https://github.com/matrix-org/matrix-react-sdk/pull/10087)). Fixes #24432.
 * Fix scrollbar colliding with checkbox in add to space section ([\#10093](https://github.com/matrix-org/matrix-react-sdk/pull/10093)). Fixes #23189. Contributed by @Arnabdaz.
 * Add a whitespace character after 'broadcast?' ([\#10097](https://github.com/matrix-org/matrix-react-sdk/pull/10097)). Contributed by @luixxiul.
 * Seekbar in broadcast PiP view is now updated when switching between different broadcasts ([\#10072](https://github.com/matrix-org/matrix-react-sdk/pull/10072)). Fixes #24415.
 * Add border to "reject" button on room preview card for clickable area indication. It fixes vector-im/element-web#22623 ([\#9205](https://github.com/matrix-org/matrix-react-sdk/pull/9205)). Contributed by @gefgu.
 * Element-R: fix rageshages ([\#10081](https://github.com/matrix-org/matrix-react-sdk/pull/10081)). Fixes #24430.
 * Fix markdown paragraph display in timeline ([\#10071](https://github.com/matrix-org/matrix-react-sdk/pull/10071)). Fixes #24419. Contributed by @alunturner.
 * Prevent the remaining broadcast time from being exceeded ([\#10070](https://github.com/matrix-org/matrix-react-sdk/pull/10070)).
 * Fix cursor position when new line is created by pressing enter (RTE) ([\#10064](https://github.com/matrix-org/matrix-react-sdk/pull/10064)). Contributed by @florianduros.
 * Ensure room is actually in space hierarchy when resolving its latest version ([\#10010](https://github.com/matrix-org/matrix-react-sdk/pull/10010)).
 * Fix new line for inline code ([\#10062](https://github.com/matrix-org/matrix-react-sdk/pull/10062)). Contributed by @florianduros.
 * Member avatars without canvas ([\#9990](https://github.com/matrix-org/matrix-react-sdk/pull/9990)). Contributed by @clarkf.
 * Apply more general fix for base avatar regressions ([\#10045](https://github.com/matrix-org/matrix-react-sdk/pull/10045)). Fixes #24382 and #24370.
 * Replace list, code block and quote icons by new icons ([\#10035](https://github.com/matrix-org/matrix-react-sdk/pull/10035)). Contributed by @florianduros.
 * fix regional emojis converted to flags ([\#9294](https://github.com/matrix-org/matrix-react-sdk/pull/9294)). Fixes #19000. Contributed by @grimhilt.
 * resolved emoji description text overflowing issue ([\#10028](https://github.com/matrix-org/matrix-react-sdk/pull/10028)). Contributed by @fahadNoufal.
 * Fix MessageEditHistoryDialog crashing on complex input ([\#10018](https://github.com/matrix-org/matrix-react-sdk/pull/10018)). Fixes #23665. Contributed by @clarkf.
 * Unify unread notification state determination ([\#9941](https://github.com/matrix-org/matrix-react-sdk/pull/9941)). Contributed by @clarkf.
 * Fix layout and visual regressions around default avatars ([\#10031](https://github.com/matrix-org/matrix-react-sdk/pull/10031)). Fixes #24375 and #24369.
 * Fix useUnreadNotifications exploding with falsey room, like in notif panel ([\#10030](https://github.com/matrix-org/matrix-react-sdk/pull/10030)). Fixes matrix-org/element-web-rageshakes#19334.
 * Fix "[object Promise]" appearing in HTML exports ([\#9975](https://github.com/matrix-org/matrix-react-sdk/pull/9975)). Fixes #24272. Contributed by @clarkf.
 * changing the color of message time stamp ([\#10016](https://github.com/matrix-org/matrix-react-sdk/pull/10016)). Contributed by @nawarajshah.
 * Fix link creation with backward selection ([\#9986](https://github.com/matrix-org/matrix-react-sdk/pull/9986)). Fixes #24315. Contributed by @florianduros.
 * Misaligned reply preview in thread composer #23396 ([\#9977](https://github.com/matrix-org/matrix-react-sdk/pull/9977)). Fixes #23396. Contributed by @mustafa-kapadia1483.

Changes in [1.11.22](https://github.com/vector-im/element-web/releases/tag/v1.11.22) (2023-01-31)
=================================================================================================

## 🐛 Bug Fixes
 * Bump version number to fix problems upgrading from v1.11.21-rc.1

Changes in [1.11.21](https://github.com/vector-im/element-web/releases/tag/v1.11.21) (2023-01-31)
=================================================================================================

## ✨ Features
 * Move pin drop out of labs ([\#22993](https://github.com/vector-im/element-web/pull/22993)).
 * Quotes for rich text editor (RTE) ([\#9932](https://github.com/matrix-org/matrix-react-sdk/pull/9932)). Contributed by @alunturner.
 * Show the room name in the room header during calls ([\#9942](https://github.com/matrix-org/matrix-react-sdk/pull/9942)). Fixes #24268.
 * Add code blocks to rich text editor ([\#9921](https://github.com/matrix-org/matrix-react-sdk/pull/9921)). Contributed by @alunturner.
 * Add new style for inline code ([\#9936](https://github.com/matrix-org/matrix-react-sdk/pull/9936)). Contributed by @florianduros.
 * Add disabled button state to rich text editor ([\#9930](https://github.com/matrix-org/matrix-react-sdk/pull/9930)). Contributed by @alunturner.
 * Change the rageshake "app" for auto-rageshakes ([\#9909](https://github.com/matrix-org/matrix-react-sdk/pull/9909)).
 * Device manager - tweak settings display ([\#9905](https://github.com/matrix-org/matrix-react-sdk/pull/9905)). Contributed by @kerryarchibald.
 * Add list functionality to rich text editor ([\#9871](https://github.com/matrix-org/matrix-react-sdk/pull/9871)). Contributed by @alunturner.

## 🐛 Bug Fixes
 * Fix RTE focus behaviour in threads ([\#9969](https://github.com/matrix-org/matrix-react-sdk/pull/9969)). Fixes #23755. Contributed by @florianduros.
 * #22204 Issue: Centered File info in lightbox ([\#9971](https://github.com/matrix-org/matrix-react-sdk/pull/9971)). Fixes #22204. Contributed by @Spartan09.
 * Fix seekbar position for zero length audio ([\#9949](https://github.com/matrix-org/matrix-react-sdk/pull/9949)). Fixes #24248.
 * Allow thread panel to be closed after being opened from notification ([\#9937](https://github.com/matrix-org/matrix-react-sdk/pull/9937)). Fixes #23764 #23852 and #24213. Contributed by @justjanne.
 * Only highlight focused menu item if focus is supposed to be visible ([\#9945](https://github.com/matrix-org/matrix-react-sdk/pull/9945)). Fixes #23582.
 * Prevent call durations from breaking onto multiple lines ([\#9944](https://github.com/matrix-org/matrix-react-sdk/pull/9944)).
 * Tweak call lobby buttons to more closely match designs ([\#9943](https://github.com/matrix-org/matrix-react-sdk/pull/9943)).
 * Do not show a broadcast as live immediately after the recording has stopped ([\#9947](https://github.com/matrix-org/matrix-react-sdk/pull/9947)). Fixes #24233.
 * Clear the RTE before sending a message ([\#9948](https://github.com/matrix-org/matrix-react-sdk/pull/9948)). Contributed by @florianduros.
 * Fix {enter} press in RTE ([\#9927](https://github.com/matrix-org/matrix-react-sdk/pull/9927)). Contributed by @florianduros.
 * Fix the problem that the password reset email has to be confirmed twice ([\#9926](https://github.com/matrix-org/matrix-react-sdk/pull/9926)). Fixes #24226.
 * replace .at() with array.length-1 ([\#9933](https://github.com/matrix-org/matrix-react-sdk/pull/9933)). Fixes matrix-org/element-web-rageshakes#19281.
 * Fix broken threads list timestamp layout ([\#9922](https://github.com/matrix-org/matrix-react-sdk/pull/9922)). Fixes #24243 and #24191. Contributed by @justjanne.
 * Disable multiple messages when {enter} is pressed multiple times ([\#9929](https://github.com/matrix-org/matrix-react-sdk/pull/9929)). Fixes #24249. Contributed by @florianduros.
 * Fix logout devices when resetting the password ([\#9925](https://github.com/matrix-org/matrix-react-sdk/pull/9925)). Fixes #24228.
 * Fix: Poll replies overflow when not enough space ([\#9924](https://github.com/matrix-org/matrix-react-sdk/pull/9924)). Fixes #24227. Contributed by @kerryarchibald.
 * State event updates are not forwarded to the widget from invitation room ([\#9802](https://github.com/matrix-org/matrix-react-sdk/pull/9802)). Contributed by @maheichyk.
 * Fix error when viewing source of redacted events ([\#9914](https://github.com/matrix-org/matrix-react-sdk/pull/9914)). Fixes #24165. Contributed by @clarkf.
 * Replace outdated css attribute ([\#9912](https://github.com/matrix-org/matrix-react-sdk/pull/9912)). Fixes #24218. Contributed by @justjanne.
 * Clear isLogin theme override when user is no longer viewing login screens ([\#9911](https://github.com/matrix-org/matrix-react-sdk/pull/9911)). Fixes #23893.
 * Fix reply action in message context menu notif & file panels ([\#9895](https://github.com/matrix-org/matrix-react-sdk/pull/9895)). Fixes #23970.
 * Fix issue where thread dropdown would not show up correctly ([\#9872](https://github.com/matrix-org/matrix-react-sdk/pull/9872)). Fixes #24040. Contributed by @justjanne.
 * Fix unexpected composer growing ([\#9889](https://github.com/matrix-org/matrix-react-sdk/pull/9889)). Contributed by @florianduros.
 * Fix misaligned timestamps for thread roots which are emotes ([\#9875](https://github.com/matrix-org/matrix-react-sdk/pull/9875)). Fixes #23897. Contributed by @justjanne.

Changes in [1.11.20](https://github.com/vector-im/element-web/releases/tag/v1.11.20) (2023-01-20)
=================================================================================================

## 🐛 Bug Fixes
 * (Part 2) of prevent crash on older browsers (replace .at() with array.length-1)

Changes in [1.11.19](https://github.com/vector-im/element-web/releases/tag/v1.11.19) (2023-01-18)
=================================================================================================

## 🐛 Bug Fixes
 * fix crash on browsers that don't support `Array.at` ([\#9935](https://github.com/matrix-org/matrix-react-sdk/pull/9935)). Contributed by @andybalaam.

Changes in [1.11.18](https://github.com/vector-im/element-web/releases/tag/v1.11.18) (2023-01-18)
=================================================================================================

## ✨ Features
 * Switch threads on for everyone ([\#9879](https://github.com/matrix-org/matrix-react-sdk/pull/9879)).
 * Make threads use new Unable to Decrypt UI ([\#9876](https://github.com/matrix-org/matrix-react-sdk/pull/9876)). Fixes #24060.
 * Add edit and remove actions to link in RTE [Labs] ([\#9864](https://github.com/matrix-org/matrix-react-sdk/pull/9864)).
 * Remove extensible events v1 experimental rendering ([\#9881](https://github.com/matrix-org/matrix-react-sdk/pull/9881)).
 * Make create poll dialog scale better (PSG-929) ([\#9873](https://github.com/matrix-org/matrix-react-sdk/pull/9873)). Fixes #21855.
 * Change RTE mode icons ([\#9861](https://github.com/matrix-org/matrix-react-sdk/pull/9861)).
 * Device manager - prune client information events after remote sign out ([\#9874](https://github.com/matrix-org/matrix-react-sdk/pull/9874)).
 * Check connection before starting broadcast ([\#9857](https://github.com/matrix-org/matrix-react-sdk/pull/9857)).
 * Enable sent receipt for poll start events (PSG-962) ([\#9870](https://github.com/matrix-org/matrix-react-sdk/pull/9870)).
 * Change clear notifications to have more readable copy ([\#9867](https://github.com/matrix-org/matrix-react-sdk/pull/9867)).
 * combine search results when the query is present in multiple successive messages ([\#9855](https://github.com/matrix-org/matrix-react-sdk/pull/9855)). Fixes #3977. Contributed by @grimhilt.
 * Disable bubbles for broadcasts ([\#9860](https://github.com/matrix-org/matrix-react-sdk/pull/9860)). Fixes #24140.
 * Enable reactions and replies for broadcasts ([\#9856](https://github.com/matrix-org/matrix-react-sdk/pull/9856)). Fixes #24042.
 * Improve switching between rich and plain editing modes ([\#9776](https://github.com/matrix-org/matrix-react-sdk/pull/9776)).
 * Redesign the picture-in-picture window ([\#9800](https://github.com/matrix-org/matrix-react-sdk/pull/9800)). Fixes #23980.
 * User on-boarding tasks now appear in a static order. ([\#9799](https://github.com/matrix-org/matrix-react-sdk/pull/9799)). Contributed by @GoodGuyMarco.
 * Device manager - contextual menus ([\#9832](https://github.com/matrix-org/matrix-react-sdk/pull/9832)).
 * If listening a non-live broadcast and changing the room, the broadcast will be paused ([\#9825](https://github.com/matrix-org/matrix-react-sdk/pull/9825)). Fixes #24078.
 * Consider own broadcasts from other device as a playback ([\#9821](https://github.com/matrix-org/matrix-react-sdk/pull/9821)). Fixes #24068.
 * Add link creation to rich text editor ([\#9775](https://github.com/matrix-org/matrix-react-sdk/pull/9775)).
 * Add mark as read option in room setting ([\#9798](https://github.com/matrix-org/matrix-react-sdk/pull/9798)). Fixes #24053.
 * Device manager - current device design and copy tweaks ([\#9801](https://github.com/matrix-org/matrix-react-sdk/pull/9801)).
 * Unify notifications panel event design ([\#9754](https://github.com/matrix-org/matrix-react-sdk/pull/9754)).
 * Add actions for integration manager to send and read certain events ([\#9740](https://github.com/matrix-org/matrix-react-sdk/pull/9740)).
 * Device manager - design tweaks ([\#9768](https://github.com/matrix-org/matrix-react-sdk/pull/9768)).
 * Change room list sorting to activity and unread first by default ([\#9773](https://github.com/matrix-org/matrix-react-sdk/pull/9773)). Fixes #24014.
 * Add a config flag to enable the rust crypto-sdk ([\#9759](https://github.com/matrix-org/matrix-react-sdk/pull/9759)).
 * Improve decryption error UI by consolidating error messages and providing instructions when possible ([\#9544](https://github.com/matrix-org/matrix-react-sdk/pull/9544)). Contributed by @duxovni.
 * Honor font settings in Element Call ([\#9751](https://github.com/matrix-org/matrix-react-sdk/pull/9751)). Fixes #23661.
 * Device manager - use deleteAccountData to prune device manager client information events ([\#9734](https://github.com/matrix-org/matrix-react-sdk/pull/9734)).

## 🐛 Bug Fixes
 * Display rooms & threads as unread (bold) if threads have unread messages. ([\#9763](https://github.com/matrix-org/matrix-react-sdk/pull/9763)). Fixes #23907.
 * Don't prefer STIXGeneral over the default font ([\#9711](https://github.com/matrix-org/matrix-react-sdk/pull/9711)). Fixes #23899.
 * Use the same avatar colour when creating 1:1 DM rooms ([\#9850](https://github.com/matrix-org/matrix-react-sdk/pull/9850)). Fixes #23476.
 * Fix space lock icon size ([\#9854](https://github.com/matrix-org/matrix-react-sdk/pull/9854)). Fixes #24128.
 * Make calls automatically disconnect if the widget disappears ([\#9862](https://github.com/matrix-org/matrix-react-sdk/pull/9862)). Fixes #23664.
 * Fix emoji in RTE editing ([\#9827](https://github.com/matrix-org/matrix-react-sdk/pull/9827)).
 * Fix export with attachments on formats txt and json ([\#9851](https://github.com/matrix-org/matrix-react-sdk/pull/9851)). Fixes #24130. Contributed by @grimhilt.
 * Fixed empty `Content-Type` for encrypted uploads ([\#9848](https://github.com/matrix-org/matrix-react-sdk/pull/9848)). Contributed by @K3das.
 * Fix sign-in instead link on password reset page ([\#9820](https://github.com/matrix-org/matrix-react-sdk/pull/9820)). Fixes #24087.
 * The seekbar now initially shows the current position ([\#9796](https://github.com/matrix-org/matrix-react-sdk/pull/9796)). Fixes #24051.
 * Fix: Editing a poll will silently change it to a closed poll ([\#9809](https://github.com/matrix-org/matrix-react-sdk/pull/9809)). Fixes #23176.
 * Make call tiles look less broken in the right panel ([\#9808](https://github.com/matrix-org/matrix-react-sdk/pull/9808)). Fixes #23716.
 * Prevent unnecessary m.direct updates ([\#9805](https://github.com/matrix-org/matrix-react-sdk/pull/9805)). Fixes #24059.
 * Fix checkForPreJoinUISI for thread roots ([\#9803](https://github.com/matrix-org/matrix-react-sdk/pull/9803)). Fixes #24054.
 * Snap in PiP widget when content changed ([\#9797](https://github.com/matrix-org/matrix-react-sdk/pull/9797)). Fixes #24050.
 * Load RTE components only when RTE labs is enabled ([\#9804](https://github.com/matrix-org/matrix-react-sdk/pull/9804)).
 * Ensure that events are correctly updated when they are edited. ([\#9789](https://github.com/matrix-org/matrix-react-sdk/pull/9789)).
 * When stopping a broadcast also stop the playback ([\#9795](https://github.com/matrix-org/matrix-react-sdk/pull/9795)). Fixes #24052.
 * Prevent to start two broadcasts at the same time ([\#9744](https://github.com/matrix-org/matrix-react-sdk/pull/9744)). Fixes #23973.
 * Correctly handle limited sync responses by resetting the thread timeline ([\#3056](https://github.com/matrix-org/matrix-js-sdk/pull/3056)). Fixes vector-im/element-web#23952.
 * Fix failure to start in firefox private browser ([\#3058](https://github.com/matrix-org/matrix-js-sdk/pull/3058)). Fixes vector-im/element-web#24216.

Changes in [1.11.17](https://github.com/vector-im/element-web/releases/tag/v1.11.17) (2022-12-21)
=================================================================================================

## ✨ Features
 * Add inline code formatting to rich text editor ([\#9720](https://github.com/matrix-org/matrix-react-sdk/pull/9720)).
 * Add emoji handling for plain text mode of the new rich text editor ([\#9727](https://github.com/matrix-org/matrix-react-sdk/pull/9727)).
 * Overlay virtual room call events into main timeline ([\#9626](https://github.com/matrix-org/matrix-react-sdk/pull/9626)). Fixes #22929.
 * Adds a new section under "Room Settings" > "Roles & Permissions" which adds the possibility to multiselect users from this room and grant them more permissions. ([\#9596](https://github.com/matrix-org/matrix-react-sdk/pull/9596)). Contributed by @GoodGuyMarco.
 * Add emoji handling for rich text mode ([\#9661](https://github.com/matrix-org/matrix-react-sdk/pull/9661)).
 * Add setting to hide bold notifications ([\#9705](https://github.com/matrix-org/matrix-react-sdk/pull/9705)).
 * Further password reset flow enhancements ([\#9662](https://github.com/matrix-org/matrix-react-sdk/pull/9662)).
 * Snooze the bulk unverified sessions reminder on dismiss ([\#9706](https://github.com/matrix-org/matrix-react-sdk/pull/9706)).
 * Honor advanced audio processing settings when recording voice messages ([\#9610](https://github.com/matrix-org/matrix-react-sdk/pull/9610)). Contributed by @MrAnno.
 * Improve the visual balance of bubble layout ([\#9704](https://github.com/matrix-org/matrix-react-sdk/pull/9704)).
 * Add config setting to disable bulk unverified sessions nag ([\#9657](https://github.com/matrix-org/matrix-react-sdk/pull/9657)).
 * Only display bulk unverified sessions nag when current sessions is verified ([\#9656](https://github.com/matrix-org/matrix-react-sdk/pull/9656)).
 * Separate labs and betas more clearly ([\#8969](https://github.com/matrix-org/matrix-react-sdk/pull/8969)). Fixes #22706.
 * Show user an error if we fail to create a DM for verification. ([\#9624](https://github.com/matrix-org/matrix-react-sdk/pull/9624)).

## 🐛 Bug Fixes
 * Prevent unnecessary m.direct updates ([\#9805](https://github.com/matrix-org/matrix-react-sdk/pull/9805)). Fixes #24059.
 * Fix checkForPreJoinUISI for thread roots ([\#9803](https://github.com/matrix-org/matrix-react-sdk/pull/9803)). Fixes #24054.
 * Load RTE components only when RTE labs is enabled ([\#9804](https://github.com/matrix-org/matrix-react-sdk/pull/9804)).
 * Fix issue where thread panel did not update correctly ([\#9746](https://github.com/matrix-org/matrix-react-sdk/pull/9746)). Fixes #23971.
 * Remove async call to get virtual room from room load ([\#9743](https://github.com/matrix-org/matrix-react-sdk/pull/9743)). Fixes #23968.
 * Check each thread for unread messages. ([\#9723](https://github.com/matrix-org/matrix-react-sdk/pull/9723)).
 * Device manage - handle sessions that don't support encryption ([\#9717](https://github.com/matrix-org/matrix-react-sdk/pull/9717)). Fixes #23722.
 * Fix hover state for formatting buttons (Rich text editor) (fix vector-im/element-web/issues/23832) ([\#9715](https://github.com/matrix-org/matrix-react-sdk/pull/9715)).
 * Don't allow group calls to be unterminated ([\#9710](https://github.com/matrix-org/matrix-react-sdk/pull/9710)).
 * Fix replies to emotes not showing as inline ([\#9707](https://github.com/matrix-org/matrix-react-sdk/pull/9707)). Fixes #23903.
 * Update copy of 'Change layout' button to match Element Call ([\#9703](https://github.com/matrix-org/matrix-react-sdk/pull/9703)).
 * Fix call splitbrains when switching between rooms ([\#9692](https://github.com/matrix-org/matrix-react-sdk/pull/9692)).
 * bugfix: fix an issue where the Notifier would incorrectly fire for non-timeline events ([\#9664](https://github.com/matrix-org/matrix-react-sdk/pull/9664)). Fixes #17263.
 * Fix power selector being wrongly disabled for admins themselves ([\#9681](https://github.com/matrix-org/matrix-react-sdk/pull/9681)). Fixes #23882.
 * Show day counts in call durations ([\#9641](https://github.com/matrix-org/matrix-react-sdk/pull/9641)).

Changes in [1.11.16](https://github.com/vector-im/element-web/releases/tag/v1.11.16) (2022-12-06)
=================================================================================================

## ✨ Features
 * Further improve replies ([\#6396](https://github.com/matrix-org/matrix-react-sdk/pull/6396)). Fixes #19074, #18194 #18027 and #19179.
 * Enable users to join group calls from multiple devices ([\#9625](https://github.com/matrix-org/matrix-react-sdk/pull/9625)).
 * fix(visual): make cursor a pointer for summaries ([\#9419](https://github.com/matrix-org/matrix-react-sdk/pull/9419)). Contributed by @r00ster91.
 * Add placeholder for rich text editor ([\#9613](https://github.com/matrix-org/matrix-react-sdk/pull/9613)).
 * Consolidate public room search experience ([\#9605](https://github.com/matrix-org/matrix-react-sdk/pull/9605)). Fixes #22846.
 * New password reset flow ([\#9581](https://github.com/matrix-org/matrix-react-sdk/pull/9581)). Fixes #23131.
 * Device manager - add tooltip to device details toggle ([\#9594](https://github.com/matrix-org/matrix-react-sdk/pull/9594)).
 * sliding sync: add lazy-loading member support ([\#9530](https://github.com/matrix-org/matrix-react-sdk/pull/9530)).
 * Limit formatting bar offset to top of composer ([\#9365](https://github.com/matrix-org/matrix-react-sdk/pull/9365)). Fixes #12359. Contributed by @owi92.

## 🐛 Bug Fixes
 * Fix issues around up arrow event edit shortcut ([\#9645](https://github.com/matrix-org/matrix-react-sdk/pull/9645)). Fixes #18497 and #18964.
 * Fix search not being cleared when clicking on a result ([\#9635](https://github.com/matrix-org/matrix-react-sdk/pull/9635)). Fixes #23845.
 * Fix screensharing in 1:1 calls ([\#9612](https://github.com/matrix-org/matrix-react-sdk/pull/9612)). Fixes #23808.
 * Fix the background color flashing when joining a call ([\#9640](https://github.com/matrix-org/matrix-react-sdk/pull/9640)).
 * Fix the size of the 'Private space' icon ([\#9638](https://github.com/matrix-org/matrix-react-sdk/pull/9638)).
 * Fix reply editing in rich text editor (https ([\#9615](https://github.com/matrix-org/matrix-react-sdk/pull/9615)).
 * Fix thread list jumping back down while scrolling ([\#9606](https://github.com/matrix-org/matrix-react-sdk/pull/9606)). Fixes #23727.
 * Fix regression with TimelinePanel props updates not taking effect ([\#9608](https://github.com/matrix-org/matrix-react-sdk/pull/9608)). Fixes #23794.
 * Fix form tooltip positioning ([\#9598](https://github.com/matrix-org/matrix-react-sdk/pull/9598)). Fixes #22861.
 * Extract Search handling from RoomView into its own Component ([\#9574](https://github.com/matrix-org/matrix-react-sdk/pull/9574)). Fixes #498.
 * Fix call splitbrains when switching between rooms ([\#9692](https://github.com/matrix-org/matrix-react-sdk/pull/9692)).
 * [Backport staging] Fix replies to emotes not showing as inline ([\#9708](https://github.com/matrix-org/matrix-react-sdk/pull/9708)).

Changes in [1.11.15](https://github.com/vector-im/element-web/releases/tag/v1.11.15) (2022-11-22)
=================================================================================================

## ✨ Features
 * Make clear notifications work with threads ([\#9575](https://github.com/matrix-org/matrix-react-sdk/pull/9575)). Fixes #23751.
 * Change "None" to "Off" in notification options ([\#9539](https://github.com/matrix-org/matrix-react-sdk/pull/9539)). Contributed by @Arnei.
 * Advanced audio processing settings ([\#8759](https://github.com/matrix-org/matrix-react-sdk/pull/8759)). Fixes #6278. Contributed by @MrAnno.
 * Add way to create a user notice via config.json ([\#9559](https://github.com/matrix-org/matrix-react-sdk/pull/9559)).
 * Improve design of the rich text editor ([\#9533](https://github.com/matrix-org/matrix-react-sdk/pull/9533)). Contributed by @florianduros.
 * Enable user to zoom beyond image size ([\#5949](https://github.com/matrix-org/matrix-react-sdk/pull/5949)). Contributed by @jaiwanth-v.
 * Fix: Move "Leave Space" option to the bottom of space context menu ([\#9535](https://github.com/matrix-org/matrix-react-sdk/pull/9535)). Contributed by @hanadi92.

## 🐛 Bug Fixes
 * Make build scripts work on NixOS ([\#23740](https://github.com/vector-im/element-web/pull/23740)).
 * Fix integration manager `get_open_id_token` action and add E2E tests ([\#9520](https://github.com/matrix-org/matrix-react-sdk/pull/9520)).
 * Fix links being mangled by markdown processing ([\#9570](https://github.com/matrix-org/matrix-react-sdk/pull/9570)). Fixes #23743.
 * Fix: inline links selecting radio button ([\#9543](https://github.com/matrix-org/matrix-react-sdk/pull/9543)). Contributed by @hanadi92.
 * Fix wrong error message in registration when phone number threepid is in use. ([\#9571](https://github.com/matrix-org/matrix-react-sdk/pull/9571)). Contributed by @bagvand.
 * Fix missing avatar for show current profiles ([\#9563](https://github.com/matrix-org/matrix-react-sdk/pull/9563)). Fixes #23733.
 * Fix read receipts trickling down correctly ([\#9567](https://github.com/matrix-org/matrix-react-sdk/pull/9567)). Fixes #23746.
 * Resilience fix for homeserver without thread notification support ([\#9565](https://github.com/matrix-org/matrix-react-sdk/pull/9565)).
 * Don't switch to the home page needlessly after leaving a room ([\#9477](https://github.com/matrix-org/matrix-react-sdk/pull/9477)).
 * Differentiate download and decryption errors when showing images ([\#9562](https://github.com/matrix-org/matrix-react-sdk/pull/9562)). Fixes #3892.
 * Close context menu when a modal is opened to prevent user getting stuck ([\#9560](https://github.com/matrix-org/matrix-react-sdk/pull/9560)). Fixes #15610 and #10781.
 * Fix TimelineReset handling when no room associated ([\#9553](https://github.com/matrix-org/matrix-react-sdk/pull/9553)).
 * Always use current profile on thread events ([\#9524](https://github.com/matrix-org/matrix-react-sdk/pull/9524)). Fixes #23648.
 * Fix `ThreadView` tests not using thread flag ([\#9547](https://github.com/matrix-org/matrix-react-sdk/pull/9547)). Contributed by @MadLittleMods.
 * Handle deletion of `m.call` events ([\#9540](https://github.com/matrix-org/matrix-react-sdk/pull/9540)). Fixes #23663.
 * Fix incorrect notification count after leaving a room with notifications ([\#9518](https://github.com/matrix-org/matrix-react-sdk/pull/9518)). Contributed by @Arnei.

Changes in [1.11.14](https://github.com/vector-im/element-web/releases/tag/v1.11.14) (2022-11-08)
=================================================================================================

## ✨ Features
 * Loading threads with server-side assistance ([\#9356](https://github.com/matrix-org/matrix-react-sdk/pull/9356)). Fixes #21807, #21799, #21911, #22141, #22157, #22641, #22501 #22438 and #21678. Contributed by @justjanne.
 * Make thread replies trigger a room list re-ordering ([\#9510](https://github.com/matrix-org/matrix-react-sdk/pull/9510)). Fixes #21700.
 * Device manager - add extra details to device security and renaming ([\#9501](https://github.com/matrix-org/matrix-react-sdk/pull/9501)). Contributed by @kerryarchibald.
 * Add plain text mode to the wysiwyg composer ([\#9503](https://github.com/matrix-org/matrix-react-sdk/pull/9503)). Contributed by @florianduros.
 * Sliding Sync: improve sort order, show subspace rooms, better tombstoned room handling ([\#9484](https://github.com/matrix-org/matrix-react-sdk/pull/9484)).
 * Device manager - add learn more popups to filtered sessions section ([\#9497](https://github.com/matrix-org/matrix-react-sdk/pull/9497)). Contributed by @kerryarchibald.
 * Show thread notification if thread timeline is closed ([\#9495](https://github.com/matrix-org/matrix-react-sdk/pull/9495)). Fixes #23589.
 * Add message editing to wysiwyg composer ([\#9488](https://github.com/matrix-org/matrix-react-sdk/pull/9488)). Contributed by @florianduros.
 * Device manager - confirm sign out of other sessions ([\#9487](https://github.com/matrix-org/matrix-react-sdk/pull/9487)). Contributed by @kerryarchibald.
 * Automatically request logs from other users in a call when submitting logs ([\#9492](https://github.com/matrix-org/matrix-react-sdk/pull/9492)).
 * Add thread notification with server assistance (MSC3773) ([\#9400](https://github.com/matrix-org/matrix-react-sdk/pull/9400)). Fixes #21114, #21413, #21416, #21433, #21481, #21798, #21823 #23192 and #21765.
 * Support for login + E2EE set up with QR ([\#9403](https://github.com/matrix-org/matrix-react-sdk/pull/9403)). Contributed by @hughns.
 * Allow pressing Enter to send messages in new composer ([\#9451](https://github.com/matrix-org/matrix-react-sdk/pull/9451)). Contributed by @andybalaam.

## 🐛 Bug Fixes
 * Fix regressions around media uploads failing and causing soft crashes ([\#9549](https://github.com/matrix-org/matrix-react-sdk/pull/9549)). Fixes matrix-org/element-web-rageshakes#16831, matrix-org/element-web-rageshakes#16824 matrix-org/element-web-rageshakes#16810 and vector-im/element-web#23641.
 * Fix /myroomavatar slash command ([\#9536](https://github.com/matrix-org/matrix-react-sdk/pull/9536)). Fixes matrix-org/synapse#14321.
 * Fix config.json failing to load for Jitsi wrapper in non-root deployment ([\#23577](https://github.com/vector-im/element-web/pull/23577)).
 * Fix NotificationBadge unsent color ([\#9522](https://github.com/matrix-org/matrix-react-sdk/pull/9522)). Fixes #23646.
 * Fix room list sorted by recent on app startup ([\#9515](https://github.com/matrix-org/matrix-react-sdk/pull/9515)). Fixes #23635.
 * Reset custom power selector when blurred on empty ([\#9508](https://github.com/matrix-org/matrix-react-sdk/pull/9508)). Fixes #23481.
 * Reinstate timeline/redaction callbacks when updating notification state ([\#9494](https://github.com/matrix-org/matrix-react-sdk/pull/9494)). Fixes #23554.
 * Only render NotificationBadge when needed ([\#9493](https://github.com/matrix-org/matrix-react-sdk/pull/9493)). Fixes #23584.
 * Fix embedded Element Call screen sharing ([\#9485](https://github.com/matrix-org/matrix-react-sdk/pull/9485)). Fixes #23571.
 * Send Content-Type: application/json header for integration manager /register API ([\#9490](https://github.com/matrix-org/matrix-react-sdk/pull/9490)). Fixes #23580.
 * Fix joining calls without audio or video inputs ([\#9486](https://github.com/matrix-org/matrix-react-sdk/pull/9486)). Fixes #23511.
 * Ensure spaces in the spotlight dialog have rounded square avatars ([\#9480](https://github.com/matrix-org/matrix-react-sdk/pull/9480)). Fixes #23515.
 * Only show mini avatar uploader in room intro when no avatar yet exists ([\#9479](https://github.com/matrix-org/matrix-react-sdk/pull/9479)). Fixes #23552.
 * Fix threads fallback incorrectly targets root event ([\#9229](https://github.com/matrix-org/matrix-react-sdk/pull/9229)). Fixes #23147.
 * Align video call icon with banner text ([\#9460](https://github.com/matrix-org/matrix-react-sdk/pull/9460)).
 * Set relations helper when creating event tile context menu ([\#9253](https://github.com/matrix-org/matrix-react-sdk/pull/9253)). Fixes #22018.
 * Device manager - put client/browser device metadata in correct section ([\#9447](https://github.com/matrix-org/matrix-react-sdk/pull/9447)). Contributed by @kerryarchibald.
 * Update the room unread notification counter when the server changes the value without any related read receipt ([\#9438](https://github.com/matrix-org/matrix-react-sdk/pull/9438)).

Changes in [1.11.13](https://github.com/vector-im/element-web/releases/tag/v1.11.13) (2022-11-01)
=================================================================================================

## 🐛 Bug Fixes
 * Fix default behavior of Room.getBlacklistUnverifiedDevices ([\#2830](https://github.com/matrix-org/matrix-js-sdk/pull/2830)). Contributed by @duxovni.
 * Catch server versions API call exception when starting the client ([\#2828](https://github.com/matrix-org/matrix-js-sdk/pull/2828)). Fixes vector-im/element-web#23634.
 * Fix authedRequest including `Authorization: Bearer undefined` for password resets ([\#2822](https://github.com/matrix-org/matrix-js-sdk/pull/2822)). Fixes vector-im/element-web#23655.

Changes in [1.11.12](https://github.com/vector-im/element-web/releases/tag/v1.11.12) (2022-10-26)
=================================================================================================

## 🐛 Bug Fixes
 * Fix config.json failing to load for Jitsi wrapper in non-root deployment ([\#23577](https://github.com/vector-im/element-web/pull/23577)).

Changes in [1.11.11](https://github.com/vector-im/element-web/releases/tag/v1.11.11) (2022-10-25)
=================================================================================================

## ✨ Features
 * Device manager - tweak string formatting of default device name ([\#23457](https://github.com/vector-im/element-web/pull/23457)).
 * Add Element Call participant limit ([\#23431](https://github.com/vector-im/element-web/pull/23431)).
 * Add Element Call `brand` ([\#23443](https://github.com/vector-im/element-web/pull/23443)).
 * Include a file-safe room name and ISO date in chat exports ([\#9440](https://github.com/matrix-org/matrix-react-sdk/pull/9440)). Fixes #21812 and #19724.
 * Room call banner ([\#9378](https://github.com/matrix-org/matrix-react-sdk/pull/9378)). Fixes #23453. Contributed by @toger5.
 * Device manager - spinners while devices are signing out ([\#9433](https://github.com/matrix-org/matrix-react-sdk/pull/9433)). Fixes #15865.
 * Device manager - silence call ringers when local notifications are silenced ([\#9420](https://github.com/matrix-org/matrix-react-sdk/pull/9420)).
 * Pass the current language to Element Call ([\#9427](https://github.com/matrix-org/matrix-react-sdk/pull/9427)).
 * Hide screen-sharing button in Element Call on desktop ([\#9423](https://github.com/matrix-org/matrix-react-sdk/pull/9423)).
 * Add reply support to WysiwygComposer ([\#9422](https://github.com/matrix-org/matrix-react-sdk/pull/9422)). Contributed by @florianduros.
 * Disconnect other connected devices (of the same user) when joining an Element call ([\#9379](https://github.com/matrix-org/matrix-react-sdk/pull/9379)).
 * Device manager - device tile main click target ([\#9409](https://github.com/matrix-org/matrix-react-sdk/pull/9409)).
 * Add formatting buttons to the rich text editor ([\#9410](https://github.com/matrix-org/matrix-react-sdk/pull/9410)). Contributed by @florianduros.
 * Device manager - current session context menu ([\#9386](https://github.com/matrix-org/matrix-react-sdk/pull/9386)).
 * Remove piwik config fallback for privacy policy URL ([\#9390](https://github.com/matrix-org/matrix-react-sdk/pull/9390)).
 * Add the first step to integrate the matrix wysiwyg composer ([\#9374](https://github.com/matrix-org/matrix-react-sdk/pull/9374)). Contributed by @florianduros.
 * Device manager - UA parsing tweaks ([\#9382](https://github.com/matrix-org/matrix-react-sdk/pull/9382)).
 * Device manager - remove client information events when disabling setting ([\#9384](https://github.com/matrix-org/matrix-react-sdk/pull/9384)).
 * Add Element Call participant limit ([\#9358](https://github.com/matrix-org/matrix-react-sdk/pull/9358)).
 * Add Element Call room settings ([\#9347](https://github.com/matrix-org/matrix-react-sdk/pull/9347)).
 * Device manager - render extended device information ([\#9360](https://github.com/matrix-org/matrix-react-sdk/pull/9360)).
 * New group call experience: Room header and PiP designs ([\#9351](https://github.com/matrix-org/matrix-react-sdk/pull/9351)).
 * Pass language to Jitsi Widget ([\#9346](https://github.com/matrix-org/matrix-react-sdk/pull/9346)). Contributed by @Fox32.
 * Add notifications and toasts for Element Call calls ([\#9337](https://github.com/matrix-org/matrix-react-sdk/pull/9337)).
 * Device manager - device type icon ([\#9355](https://github.com/matrix-org/matrix-react-sdk/pull/9355)).
 * Delete the remainder of groups ([\#9357](https://github.com/matrix-org/matrix-react-sdk/pull/9357)). Fixes #22770.
 * Device manager - display client information in device details ([\#9315](https://github.com/matrix-org/matrix-react-sdk/pull/9315)).

## 🐛 Bug Fixes
 * Send Content-Type: application/json header for integration manager /register API ([\#9490](https://github.com/matrix-org/matrix-react-sdk/pull/9490)). Fixes #23580.
 * Make ErrorView & CompatibilityView scrollable ([\#23468](https://github.com/vector-im/element-web/pull/23468)). Fixes #23376.
 * Device manager - put client/browser device metadata in correct section ([\#9447](https://github.com/matrix-org/matrix-react-sdk/pull/9447)).
 * update the room unread notification counter when the server changes the value without any related read receipt ([\#9438](https://github.com/matrix-org/matrix-react-sdk/pull/9438)).
 * Don't show call banners in video rooms ([\#9441](https://github.com/matrix-org/matrix-react-sdk/pull/9441)).
 * Prevent useContextMenu isOpen from being true if the button ref goes away ([\#9418](https://github.com/matrix-org/matrix-react-sdk/pull/9418)). Fixes matrix-org/element-web-rageshakes#15637.
 * Automatically focus the WYSIWYG composer when you enter a room ([\#9412](https://github.com/matrix-org/matrix-react-sdk/pull/9412)).
 * Improve the tooltips on the call lobby join button ([\#9428](https://github.com/matrix-org/matrix-react-sdk/pull/9428)).
 * Pass the homeserver's base URL to Element Call ([\#9429](https://github.com/matrix-org/matrix-react-sdk/pull/9429)). Fixes #23301.
 * Better accommodate long room names in call toasts ([\#9426](https://github.com/matrix-org/matrix-react-sdk/pull/9426)).
 * Hide virtual widgets from the room info panel ([\#9424](https://github.com/matrix-org/matrix-react-sdk/pull/9424)). Fixes #23494.
 * Inhibit clicking on sender avatar in threads list ([\#9417](https://github.com/matrix-org/matrix-react-sdk/pull/9417)). Fixes #23482.
 * Correct the dir parameter of MSC3715 ([\#9391](https://github.com/matrix-org/matrix-react-sdk/pull/9391)). Contributed by @dhenneke.
 * Use a more correct subset of users in `/remakeolm` developer command ([\#9402](https://github.com/matrix-org/matrix-react-sdk/pull/9402)).
 * use correct default for notification silencing ([\#9388](https://github.com/matrix-org/matrix-react-sdk/pull/9388)). Fixes #23456.
 * Device manager - eagerly create `m.local_notification_settings` events ([\#9353](https://github.com/matrix-org/matrix-react-sdk/pull/9353)).
 * Close incoming Element call toast when viewing the call lobby ([\#9375](https://github.com/matrix-org/matrix-react-sdk/pull/9375)).
 * Always allow enabling sending read receipts ([\#9367](https://github.com/matrix-org/matrix-react-sdk/pull/9367)). Fixes #23433.
 * Fixes (vector-im/element-web/issues/22609) where the white theme is not applied when `white -> dark -> white` sequence is done. ([\#9320](https://github.com/matrix-org/matrix-react-sdk/pull/9320)). Contributed by @florianduros.
 * Fix applying programmatically set height for "top" room layout ([\#9339](https://github.com/matrix-org/matrix-react-sdk/pull/9339)). Contributed by @Fox32.

Changes in [1.11.10](https://github.com/vector-im/element-web/releases/tag/v1.11.10) (2022-10-11)
=================================================================================================

## 🐛 Bug Fixes
 * Use correct default for notification silencing ([\#9388](https://github.com/matrix-org/matrix-react-sdk/pull/9388)). Fixes vector-im/element-web#23456.

Changes in [1.11.9](https://github.com/vector-im/element-web/releases/tag/v1.11.9) (2022-10-11)
===============================================================================================

##   Deprecations
 * Legacy Piwik config.json option `piwik.policy_url` is deprecated in favour of `privacy_policy_url`. Support will be removed in the next release.

## ✨ Features
 * Device manager - select all devices ([\#9330](https://github.com/matrix-org/matrix-react-sdk/pull/9330)). Contributed by @kerryarchibald.
 * New group call experience: Call tiles ([\#9332](https://github.com/matrix-org/matrix-react-sdk/pull/9332)).
 * Add Shift key to FormatQuote keyboard shortcut ([\#9298](https://github.com/matrix-org/matrix-react-sdk/pull/9298)). Contributed by @owi92.
 * Device manager - sign out of multiple sessions ([\#9325](https://github.com/matrix-org/matrix-react-sdk/pull/9325)). Contributed by @kerryarchibald.
 * Display push toggle for web sessions (MSC3890) ([\#9327](https://github.com/matrix-org/matrix-react-sdk/pull/9327)).
 * Add device notifications enabled switch ([\#9324](https://github.com/matrix-org/matrix-react-sdk/pull/9324)).
 * Implement push notification toggle in device detail ([\#9308](https://github.com/matrix-org/matrix-react-sdk/pull/9308)).
 * New group call experience: Starting and ending calls ([\#9318](https://github.com/matrix-org/matrix-react-sdk/pull/9318)).
 * New group call experience: Room header call buttons ([\#9311](https://github.com/matrix-org/matrix-react-sdk/pull/9311)).
 * Make device ID copyable in device list ([\#9297](https://github.com/matrix-org/matrix-react-sdk/pull/9297)). Contributed by @duxovni.
 * Use display name instead of user ID when rendering power events ([\#9295](https://github.com/matrix-org/matrix-react-sdk/pull/9295)).
 * Read receipts for threads ([\#9239](https://github.com/matrix-org/matrix-react-sdk/pull/9239)). Fixes #23191.

## 🐛 Bug Fixes
 * Use the correct sender key when checking shared secret ([\#2730](https://github.com/matrix-org/matrix-js-sdk/pull/2730)). Fixes vector-im/element-web#23374.
 * Fix device selection in pre-join screen for Element Call video rooms ([\#9321](https://github.com/matrix-org/matrix-react-sdk/pull/9321)). Fixes #23331.
 * Don't render a 1px high room topic if the room topic is empty ([\#9317](https://github.com/matrix-org/matrix-react-sdk/pull/9317)). Contributed by @Arnei.
 * Don't show feedback prompts when that UIFeature is disabled ([\#9305](https://github.com/matrix-org/matrix-react-sdk/pull/9305)). Fixes #23327.
 * Fix soft crash around unknown room pills ([\#9301](https://github.com/matrix-org/matrix-react-sdk/pull/9301)). Fixes matrix-org/element-web-rageshakes#15465.
 * Fix spaces feedback prompt wrongly showing when feedback is disabled ([\#9302](https://github.com/matrix-org/matrix-react-sdk/pull/9302)). Fixes #23314.
 * Fix tile soft crash in ReplyInThreadButton ([\#9300](https://github.com/matrix-org/matrix-react-sdk/pull/9300)). Fixes matrix-org/element-web-rageshakes#15493.

Changes in [1.11.8](https://github.com/vector-im/element-web/releases/tag/v1.11.8) (2022-09-28)
===============================================================================================

## 🐛 Bug Fixes
 * Bump IDB crypto store version ([\#2705](https://github.com/matrix-org/matrix-js-sdk/pull/2705)).

Changes in [1.11.7](https://github.com/vector-im/element-web/releases/tag/v1.11.7) (2022-09-28)
===============================================================================================

## 🔒 Security
* Fix for [CVE-2022-39249](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE%2D2022%2D39249)
* Fix for [CVE-2022-39250](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE%2D2022%2D39250)
* Fix for [CVE-2022-39251](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE%2D2022%2D39251)
* Fix for [CVE-2022-39236](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE%2D2022%2D39236)

Changes in [1.11.6](https://github.com/vector-im/element-web/releases/tag/v1.11.6) (2022-09-20)
=========================================================================================================

## ✨ Features
 * Element Call video rooms ([\#9267](https://github.com/matrix-org/matrix-react-sdk/pull/9267)).
 * Device manager - rename session ([\#9282](https://github.com/matrix-org/matrix-react-sdk/pull/9282)).
 * Allow widgets to read related events ([\#9210](https://github.com/matrix-org/matrix-react-sdk/pull/9210)). Contributed by @dhenneke.
 * Device manager - logout of other session ([\#9280](https://github.com/matrix-org/matrix-react-sdk/pull/9280)).
 * Device manager - logout current session ([\#9275](https://github.com/matrix-org/matrix-react-sdk/pull/9275)).
 * Device manager - verify other devices ([\#9274](https://github.com/matrix-org/matrix-react-sdk/pull/9274)).
 * Allow integration managers to remove users ([\#9211](https://github.com/matrix-org/matrix-react-sdk/pull/9211)).
 * Device manager - add verify current session button ([\#9252](https://github.com/matrix-org/matrix-react-sdk/pull/9252)).
 * Add NotifPanel dot back. ([\#9242](https://github.com/matrix-org/matrix-react-sdk/pull/9242)). Fixes #17641.
 * Implement MSC3575: Sliding Sync ([\#8328](https://github.com/matrix-org/matrix-react-sdk/pull/8328)).
 * Add the clipboard read permission for widgets ([\#9250](https://github.com/matrix-org/matrix-react-sdk/pull/9250)). Contributed by @stefanmuhle.

## 🐛 Bug Fixes
 * Make autocomplete pop-up wider in thread view ([\#9289](https://github.com/matrix-org/matrix-react-sdk/pull/9289)).
 * Fix soft crash around inviting invalid MXIDs in start DM on first message flow ([\#9281](https://github.com/matrix-org/matrix-react-sdk/pull/9281)). Fixes matrix-org/element-web-rageshakes#15060 and matrix-org/element-web-rageshakes#15140.
 * Fix in-reply-to previews not disappearing when swapping rooms ([\#9278](https://github.com/matrix-org/matrix-react-sdk/pull/9278)).
 * Fix invalid instanceof operand window.OffscreenCanvas ([\#9276](https://github.com/matrix-org/matrix-react-sdk/pull/9276)). Fixes #23275.
 * Fix memory leak caused by unremoved listener ([\#9273](https://github.com/matrix-org/matrix-react-sdk/pull/9273)).
 * Fix thumbnail generation when offscreen canvas fails ([\#9272](https://github.com/matrix-org/matrix-react-sdk/pull/9272)). Fixes #23265.
 * Prevent sliding sync from showing a room under multiple sublists ([\#9266](https://github.com/matrix-org/matrix-react-sdk/pull/9266)).
 * Fix tile crash around tooltipify links ([\#9270](https://github.com/matrix-org/matrix-react-sdk/pull/9270)). Fixes #23253.
 * Device manager - filter out nulled metadatas in device tile properly ([\#9251](https://github.com/matrix-org/matrix-react-sdk/pull/9251)).
 * Fix a sliding sync bug which could cause rooms to loop ([\#9268](https://github.com/matrix-org/matrix-react-sdk/pull/9268)).
 * Remove the grey gradient on images in bubbles in the timeline ([\#9241](https://github.com/matrix-org/matrix-react-sdk/pull/9241)). Fixes #21651.
 * Fix html export not including images ([\#9260](https://github.com/matrix-org/matrix-react-sdk/pull/9260)). Fixes #22059.
 * Fix possible soft crash from a race condition in space hierarchies ([\#9254](https://github.com/matrix-org/matrix-react-sdk/pull/9254)). Fixes matrix-org/element-web-rageshakes#15225.
 * Disable all types of autocorrect, -complete, -capitalize, etc on Spotlight's search field ([\#9259](https://github.com/matrix-org/matrix-react-sdk/pull/9259)).
 * Handle M_INVALID_USERNAME on /register/available ([\#9237](https://github.com/matrix-org/matrix-react-sdk/pull/9237)). Fixes #23161.
 * Fix issue with quiet zone around QR code ([\#9243](https://github.com/matrix-org/matrix-react-sdk/pull/9243)). Fixes #23199.

Changes in [1.11.5](https://github.com/vector-im/element-web/releases/tag/v1.11.5) (2022-09-13)
===============================================================================================

## ✨ Features
 * Device manager - hide unverified security recommendation when only current session is unverified ([\#9228](https://github.com/matrix-org/matrix-react-sdk/pull/9228)). Contributed by @kerryarchibald.
 * Device manager - scroll to filtered list from security recommendations ([\#9227](https://github.com/matrix-org/matrix-react-sdk/pull/9227)). Contributed by @kerryarchibald.
 * Device manager - updated dropdown style in filtered device list ([\#9226](https://github.com/matrix-org/matrix-react-sdk/pull/9226)). Contributed by @kerryarchibald.
 * Device manager - device type and verification icons on device tile ([\#9197](https://github.com/matrix-org/matrix-react-sdk/pull/9197)). Contributed by @kerryarchibald.

## 🐛 Bug Fixes
 * Description of DM room with more than two other people is now being displayed correctly ([\#9231](https://github.com/matrix-org/matrix-react-sdk/pull/9231)). Fixes #23094.
 * Fix voice messages with multiple composers ([\#9208](https://github.com/matrix-org/matrix-react-sdk/pull/9208)). Fixes #23023. Contributed by @grimhilt.
 * Fix suggested rooms going missing ([\#9236](https://github.com/matrix-org/matrix-react-sdk/pull/9236)). Fixes #23190.
 * Fix tooltip infinitely recursing ([\#9235](https://github.com/matrix-org/matrix-react-sdk/pull/9235)). Fixes matrix-org/element-web-rageshakes#15107, matrix-org/element-web-rageshakes#15093 matrix-org/element-web-rageshakes#15092 and matrix-org/element-web-rageshakes#15077.
 * Fix plain text export saving ([\#9230](https://github.com/matrix-org/matrix-react-sdk/pull/9230)). Contributed by @jryans.
 * Add missing space in SecurityRoomSettingsTab ([\#9222](https://github.com/matrix-org/matrix-react-sdk/pull/9222)). Contributed by @gefgu.
 * Make use of js-sdk roomNameGenerator to handle i18n for generated room names ([\#9209](https://github.com/matrix-org/matrix-react-sdk/pull/9209)). Fixes #21369.
 * Fix progress bar regression throughout the app ([\#9219](https://github.com/matrix-org/matrix-react-sdk/pull/9219)). Fixes #23121.
 * Reuse empty string & space string logic for event types in devtools ([\#9218](https://github.com/matrix-org/matrix-react-sdk/pull/9218)). Fixes #23115.

Changes in [1.11.4](https://github.com/vector-im/element-web/releases/tag/v1.11.4) (2022-08-31)
===============================================================================================

## 🔒 Security
* Fixes for [CVE-2022-36059](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE%2D2022%2D36059) and [CVE-2022-36060](https://cve.mitre.org/cgi-bin/cvekey.cgi?keyword=CVE%2D2022%2D36060)

Learn more about what we've been up to at https://element.io/blog/element-web-desktop-1-11-4-a-security-update-deferred-dms-and-more/
Find more details of the vulnerabilities at https://matrix.org/blog/2022/08/31/security-releases-matrix-js-sdk-19-4-0-and-matrix-react-sdk-3-53-0

## ✨ Features
 * Device manager - scroll to filtered list from security recommendations ([\#9227](https://github.com/matrix-org/matrix-react-sdk/pull/9227)). Contributed by @kerryarchibald.
 * Device manager - updated dropdown style in filtered device list ([\#9226](https://github.com/matrix-org/matrix-react-sdk/pull/9226)). Contributed by @kerryarchibald.
 * Device manager - device type and verification icons on device tile ([\#9197](https://github.com/matrix-org/matrix-react-sdk/pull/9197)). Contributed by @kerryarchibald.
 * Ignore unreads in low priority rooms in the space panel ([\#6518](https://github.com/matrix-org/matrix-react-sdk/pull/6518)). Fixes #16836.
 * Release message right-click context menu out of labs ([\#8613](https://github.com/matrix-org/matrix-react-sdk/pull/8613)).
 * Device manager - expandable session details in device list ([\#9188](https://github.com/matrix-org/matrix-react-sdk/pull/9188)). Contributed by @kerryarchibald.
 * Device manager - device list filtering ([\#9181](https://github.com/matrix-org/matrix-react-sdk/pull/9181)). Contributed by @kerryarchibald.
 * Device manager - add verification details to session details ([\#9187](https://github.com/matrix-org/matrix-react-sdk/pull/9187)). Contributed by @kerryarchibald.
 * Device manager - current session expandable details ([\#9185](https://github.com/matrix-org/matrix-react-sdk/pull/9185)). Contributed by @kerryarchibald.
 * Device manager - security recommendations section ([\#9179](https://github.com/matrix-org/matrix-react-sdk/pull/9179)). Contributed by @kerryarchibald.
 * The Welcome Home Screen: Return Button ([\#9089](https://github.com/matrix-org/matrix-react-sdk/pull/9089)). Fixes #22917. Contributed by @justjanne.
 * Device manager - label devices as inactive ([\#9175](https://github.com/matrix-org/matrix-react-sdk/pull/9175)). Contributed by @kerryarchibald.
 * Device manager - other sessions list ([\#9155](https://github.com/matrix-org/matrix-react-sdk/pull/9155)). Contributed by @kerryarchibald.
 * Implement MSC3846: Allowing widgets to access TURN servers ([\#9061](https://github.com/matrix-org/matrix-react-sdk/pull/9061)).
 * Allow widgets to send/receive to-device messages ([\#8885](https://github.com/matrix-org/matrix-react-sdk/pull/8885)).

## 🐛 Bug Fixes
 * Add super cool feature ([\#9222](https://github.com/matrix-org/matrix-react-sdk/pull/9222)). Contributed by @gefgu.
 * Make use of js-sdk roomNameGenerator to handle i18n for generated room names ([\#9209](https://github.com/matrix-org/matrix-react-sdk/pull/9209)). Fixes #21369.
 * Fix progress bar regression throughout the app ([\#9219](https://github.com/matrix-org/matrix-react-sdk/pull/9219)). Fixes #23121.
 * Reuse empty string & space string logic for event types in devtools ([\#9218](https://github.com/matrix-org/matrix-react-sdk/pull/9218)). Fixes #23115.
 * Reduce amount of requests done by the onboarding task list ([\#9194](https://github.com/matrix-org/matrix-react-sdk/pull/9194)). Fixes #23085. Contributed by @justjanne.
 * Avoid hardcoding branding in user onboarding ([\#9206](https://github.com/matrix-org/matrix-react-sdk/pull/9206)). Fixes #23111. Contributed by @justjanne.
 * End jitsi call when member is banned ([\#8879](https://github.com/matrix-org/matrix-react-sdk/pull/8879)). Contributed by @maheichyk.
 * Fix context menu being opened when clicking message action bar buttons ([\#9200](https://github.com/matrix-org/matrix-react-sdk/pull/9200)). Fixes #22279 and #23100.
 * Add gap between checkbox and text in report dialog following the same pattern (8px) used in the gap between the two buttons. It fixes vector-im/element-web#23060 ([\#9195](https://github.com/matrix-org/matrix-react-sdk/pull/9195)). Contributed by @gefgu.
 * Fix url preview AXE and layout issue & add percy test ([\#9189](https://github.com/matrix-org/matrix-react-sdk/pull/9189)). Fixes #23083.
 * Wrap long space names ([\#9201](https://github.com/matrix-org/matrix-react-sdk/pull/9201)). Fixes #23095.
 * Attempt to fix `Failed to execute 'removeChild' on 'Node'` ([\#9196](https://github.com/matrix-org/matrix-react-sdk/pull/9196)).
 * Fix soft crash around space hierarchy changing between spaces ([\#9191](https://github.com/matrix-org/matrix-react-sdk/pull/9191)). Fixes matrix-org/element-web-rageshakes#14613.
 * Fix soft crash around room view store metrics ([\#9190](https://github.com/matrix-org/matrix-react-sdk/pull/9190)). Fixes matrix-org/element-web-rageshakes#14361.
 * Fix the same person appearing multiple times when searching for them. ([\#9177](https://github.com/matrix-org/matrix-react-sdk/pull/9177)). Fixes #22851.
 * Fix space panel subspace indentation going missing ([\#9167](https://github.com/matrix-org/matrix-react-sdk/pull/9167)). Fixes #23049.
 * Fix invisible power levels tile when showing hidden events ([\#9162](https://github.com/matrix-org/matrix-react-sdk/pull/9162)). Fixes #23013.
 * Space panel accessibility improvements ([\#9157](https://github.com/matrix-org/matrix-react-sdk/pull/9157)). Fixes #22995.
 * Fix inverted logic for showing UserWelcomeTop component ([\#9164](https://github.com/matrix-org/matrix-react-sdk/pull/9164)). Fixes #23037.

Changes in [1.11.3](https://github.com/vector-im/element-web/releases/tag/v1.11.3) (2022-08-16)
===============================================================================================

## ✨ Features
 * Improve auth aria attributes and semantics ([\#22948](https://github.com/vector-im/element-web/pull/22948)).
 * Device manager - New device tile info design ([\#9122](https://github.com/matrix-org/matrix-react-sdk/pull/9122)). Contributed by @kerryarchibald.
 * Device manager generic settings subsection component ([\#9147](https://github.com/matrix-org/matrix-react-sdk/pull/9147)). Contributed by @kerryarchibald.
 * Migrate the hidden read receipts flag to new "send read receipts" option ([\#9141](https://github.com/matrix-org/matrix-react-sdk/pull/9141)).
 * Live location sharing - share location at most every 5 seconds ([\#9148](https://github.com/matrix-org/matrix-react-sdk/pull/9148)). Contributed by @kerryarchibald.
 * Increase max length of voice messages to 15m ([\#9133](https://github.com/matrix-org/matrix-react-sdk/pull/9133)). Fixes #18620.
 * Move pin drop out of labs ([\#9135](https://github.com/matrix-org/matrix-react-sdk/pull/9135)).
 * Start DM on first message ([\#8612](https://github.com/matrix-org/matrix-react-sdk/pull/8612)). Fixes #14736.
 * Remove "Add Space" button from RoomListHeader when user cannot create spaces ([\#9129](https://github.com/matrix-org/matrix-react-sdk/pull/9129)).
 * The Welcome Home Screen: Dedicated Download Apps Dialog ([\#9120](https://github.com/matrix-org/matrix-react-sdk/pull/9120)). Fixes #22921. Contributed by @justjanne.
 * The Welcome Home Screen: "Submit Feedback" pane ([\#9090](https://github.com/matrix-org/matrix-react-sdk/pull/9090)). Fixes #22918. Contributed by @justjanne.
 * New User Onboarding Task List ([\#9083](https://github.com/matrix-org/matrix-react-sdk/pull/9083)). Fixes #22919. Contributed by @justjanne.
 * Add support for disabling spell checking ([\#8604](https://github.com/matrix-org/matrix-react-sdk/pull/8604)). Fixes #21901.
 * Live location share - leave maximised map open when beacons expire ([\#9098](https://github.com/matrix-org/matrix-react-sdk/pull/9098)). Contributed by @kerryarchibald.

## 🐛 Bug Fixes
 * Some slash-commands (`/myroomnick`) have temporarily been disabled before the first message in a DM is sent. ([\#9193](https://github.com/matrix-org/matrix-react-sdk/pull/9193)).
 * Use stable reference for active tab in tabbedView ([\#9145](https://github.com/matrix-org/matrix-react-sdk/pull/9145)). Contributed by @kerryarchibald.
 * Fix pillification sometimes doubling up ([\#9152](https://github.com/matrix-org/matrix-react-sdk/pull/9152)). Fixes #23036.
 * Fix highlights not being applied to plaintext messages ([\#9126](https://github.com/matrix-org/matrix-react-sdk/pull/9126)). Fixes #22787.
 * Fix dismissing edit composer when change was undone ([\#9109](https://github.com/matrix-org/matrix-react-sdk/pull/9109)). Fixes #22932.
 * 1-to-1 DM rooms with bots now act like DM rooms instead of multi-user-rooms before ([\#9124](https://github.com/matrix-org/matrix-react-sdk/pull/9124)). Fixes #22894.
 * Apply inline start padding to selected lines on modern layout only ([\#9006](https://github.com/matrix-org/matrix-react-sdk/pull/9006)). Fixes #22768. Contributed by @luixxiul.
 * Peek into world-readable rooms from spotlight ([\#9115](https://github.com/matrix-org/matrix-react-sdk/pull/9115)). Fixes #22862.
 * Use default styling on nested numbered lists due to MD being sensitive ([\#9110](https://github.com/matrix-org/matrix-react-sdk/pull/9110)). Fixes #22935.
 * Fix replying using chat effect commands ([\#9101](https://github.com/matrix-org/matrix-react-sdk/pull/9101)). Fixes #22824.

Changes in [1.11.2](https://github.com/vector-im/element-web/releases/tag/v1.11.2) (2022-08-03)
===============================================================================================

## ✨ Features
 * Live location share -  focus on user location on list item click ([\#9051](https://github.com/matrix-org/matrix-react-sdk/pull/9051)). Contributed by @kerryarchibald.
 * Live location sharing - don't trigger unread counts for beacon location events ([\#9071](https://github.com/matrix-org/matrix-react-sdk/pull/9071)). Contributed by @kerryarchibald.
 * Support for sending voice messages as replies and in threads ([\#9097](https://github.com/matrix-org/matrix-react-sdk/pull/9097)). Fixes #22031.
 * Add `Reply in thread` button to the right-click message context-menu ([\#9004](https://github.com/matrix-org/matrix-react-sdk/pull/9004)). Fixes #22745.
 * Starred_Messages_Feature_Contd_II/Outreachy ([\#9086](https://github.com/matrix-org/matrix-react-sdk/pull/9086)).
 * Use "frequently used emojis" for autocompletion in composer ([\#8998](https://github.com/matrix-org/matrix-react-sdk/pull/8998)). Fixes #18978. Contributed by @grimhilt.
 * Improve clickability of view source event toggle button  ([\#9068](https://github.com/matrix-org/matrix-react-sdk/pull/9068)). Fixes #21856. Contributed by @luixxiul.
 * Improve clickability of "collapse" link button on bubble layout ([\#9037](https://github.com/matrix-org/matrix-react-sdk/pull/9037)). Fixes #22864. Contributed by @luixxiul.
 * Starred_Messages_Feature/Outreachy ([\#8842](https://github.com/matrix-org/matrix-react-sdk/pull/8842)).
 * Implement Use Case Selection screen ([\#8984](https://github.com/matrix-org/matrix-react-sdk/pull/8984)). Contributed by @justjanne.
 * Live location share - handle insufficient permissions in location sharing ([\#9047](https://github.com/matrix-org/matrix-react-sdk/pull/9047)). Contributed by @kerryarchibald.
 * Improve _FilePanel.scss ([\#9031](https://github.com/matrix-org/matrix-react-sdk/pull/9031)). Contributed by @luixxiul.
 * Improve spotlight accessibility by adding context menus ([\#8907](https://github.com/matrix-org/matrix-react-sdk/pull/8907)). Fixes #20875 and #22675. Contributed by @justjanne.

## 🐛 Bug Fixes
 * Replace mask-images with svg components in MessageActionBar ([\#9088](https://github.com/matrix-org/matrix-react-sdk/pull/9088)). Fixes #22912. Contributed by @kerryarchibald.
 * Unbreak in-app permalink tooltips ([\#9087](https://github.com/matrix-org/matrix-react-sdk/pull/9087)). Fixes #22874.
 * Show a back button when viewing a space member ([\#9095](https://github.com/matrix-org/matrix-react-sdk/pull/9095)). Fixes #22898.
 * Align the right edge of info tile lines with normal ones on IRC layout ([\#9058](https://github.com/matrix-org/matrix-react-sdk/pull/9058)). Fixes #22871. Contributed by @luixxiul.
 * Prevent email verification from overriding existing sessions ([\#9075](https://github.com/matrix-org/matrix-react-sdk/pull/9075)). Fixes #22881. Contributed by @justjanne.
 * Fix wrong buttons being used when exploring public rooms ([\#9062](https://github.com/matrix-org/matrix-react-sdk/pull/9062)). Fixes #22862.
 * Re-add padding to generic event list summary on IRC layout ([\#9063](https://github.com/matrix-org/matrix-react-sdk/pull/9063)). Fixes #22869. Contributed by @luixxiul.
 * Joining federated rooms via the spotlight search should no longer cause a "No known servers" error. ([\#9055](https://github.com/matrix-org/matrix-react-sdk/pull/9055)). Fixes #22845. Contributed by @Half-Shot.

Changes in [1.11.1](https://github.com/vector-im/element-web/releases/tag/v1.11.1) (2022-07-26)
===============================================================================================

## ✨ Features
 * Enable URL tooltips on hover for Element Desktop ([\#22286](https://github.com/vector-im/element-web/pull/22286)). Fixes undefined/element-web#6532.
 * Hide screenshare button in video rooms on Desktop ([\#9045](https://github.com/matrix-org/matrix-react-sdk/pull/9045)).
 * Add a developer command to reset Megolm and Olm sessions ([\#9044](https://github.com/matrix-org/matrix-react-sdk/pull/9044)).
 * add spaces to TileErrorBoundary ([\#9012](https://github.com/matrix-org/matrix-react-sdk/pull/9012)). Contributed by @HarHarLinks.
 * Location sharing - add localised strings to map ([\#9025](https://github.com/matrix-org/matrix-react-sdk/pull/9025)). Fixes #21443. Contributed by @kerryarchibald.
 * Added trim to ignore whitespaces in email check ([\#9027](https://github.com/matrix-org/matrix-react-sdk/pull/9027)). Contributed by @ankur12-1610.
 * Improve _GenericEventListSummary.scss ([\#9005](https://github.com/matrix-org/matrix-react-sdk/pull/9005)). Contributed by @luixxiul.
 * Live location share - tiles without tile server (PSG-591) ([\#8962](https://github.com/matrix-org/matrix-react-sdk/pull/8962)). Contributed by @kerryarchibald.
 * Add option to display tooltip on link hover ([\#8394](https://github.com/matrix-org/matrix-react-sdk/pull/8394)). Fixes #21907.
 * Support a module API surface for custom functionality ([\#8246](https://github.com/matrix-org/matrix-react-sdk/pull/8246)).
 * Adjust encryption copy when creating a video room ([\#8989](https://github.com/matrix-org/matrix-react-sdk/pull/8989)). Fixes #22737.
 * Add bidirectonal isolation for pills ([\#8985](https://github.com/matrix-org/matrix-react-sdk/pull/8985)). Contributed by @sha-265.
 * Delabs `Show current avatar and name for users in message history` ([\#8764](https://github.com/matrix-org/matrix-react-sdk/pull/8764)). Fixes #22336.
 * Live location share - open latest location in map site ([\#8981](https://github.com/matrix-org/matrix-react-sdk/pull/8981)). Contributed by @kerryarchibald.
 * Improve LinkPreviewWidget ([\#8881](https://github.com/matrix-org/matrix-react-sdk/pull/8881)). Fixes #22634. Contributed by @luixxiul.
 * Render HTML topics in rooms on space home ([\#8939](https://github.com/matrix-org/matrix-react-sdk/pull/8939)).
 * Hide timestamp on event tiles being edited on every layout ([\#8956](https://github.com/matrix-org/matrix-react-sdk/pull/8956)). Contributed by @luixxiul.
 * Introduce new copy icon ([\#8942](https://github.com/matrix-org/matrix-react-sdk/pull/8942)).
 * Allow finding group DMs by members in spotlight ([\#8922](https://github.com/matrix-org/matrix-react-sdk/pull/8922)). Fixes #22564. Contributed by @justjanne.
 * Live location share - explicitly stop beacons replaced beacons ([\#8933](https://github.com/matrix-org/matrix-react-sdk/pull/8933)). Contributed by @kerryarchibald.
 * Remove unpin from widget kebab menu ([\#8924](https://github.com/matrix-org/matrix-react-sdk/pull/8924)).
 * Live location share - redact related locations on beacon redaction ([\#8926](https://github.com/matrix-org/matrix-react-sdk/pull/8926)). Contributed by @kerryarchibald.
 * Live location share - disallow message pinning ([\#8928](https://github.com/matrix-org/matrix-react-sdk/pull/8928)). Contributed by @kerryarchibald.

## 🐛 Bug Fixes
 * Remove the ability to hide yourself in video rooms ([\#22806](https://github.com/vector-im/element-web/pull/22806)). Fixes #22805.
 * Unbreak in-app permalink tooltips  ([\#9100](https://github.com/matrix-org/matrix-react-sdk/pull/9100)).
 * Add space for the stroke on message editor on IRC layout ([\#9030](https://github.com/matrix-org/matrix-react-sdk/pull/9030)). Fixes #22785. Contributed by @luixxiul.
 * Fix pinned messages not re-linkifying on edit ([\#9042](https://github.com/matrix-org/matrix-react-sdk/pull/9042)). Fixes #22726.
 * Don't unnecessarily persist the host signup dialog ([\#9043](https://github.com/matrix-org/matrix-react-sdk/pull/9043)). Fixes #22778.
 * Fix URL previews causing messages to become unrenderable ([\#9028](https://github.com/matrix-org/matrix-react-sdk/pull/9028)). Fixes #22766.
 * Fix event list summaries including invalid events ([\#9041](https://github.com/matrix-org/matrix-react-sdk/pull/9041)). Fixes #22790.
 * Correct accessibility labels for unread rooms in spotlight ([\#9003](https://github.com/matrix-org/matrix-react-sdk/pull/9003)). Contributed by @justjanne.
 * Enable search strings highlight on bubble layout ([\#9032](https://github.com/matrix-org/matrix-react-sdk/pull/9032)). Fixes #22786. Contributed by @luixxiul.
 * Unbreak URL preview for formatted links with tooltips ([\#9022](https://github.com/matrix-org/matrix-react-sdk/pull/9022)). Fixes #22764.
 * Re-add margin to tiles based on EventTileBubble ([\#9015](https://github.com/matrix-org/matrix-react-sdk/pull/9015)). Fixes #22772. Contributed by @luixxiul.
 * Fix Shortcut prompt for Search showing in minimized Roomlist ([\#9014](https://github.com/matrix-org/matrix-react-sdk/pull/9014)). Fixes #22739. Contributed by @justjanne.
 * Fix avatar position on event info line for hidden events on a thread ([\#9019](https://github.com/matrix-org/matrix-react-sdk/pull/9019)). Fixes #22777. Contributed by @luixxiul.
 * Fix lost padding of event tile info line ([\#9009](https://github.com/matrix-org/matrix-react-sdk/pull/9009)). Fixes #22754 and #22759. Contributed by @luixxiul.
 * Align verification bubble with normal event tiles on IRC layout ([\#9001](https://github.com/matrix-org/matrix-react-sdk/pull/9001)). Fixes #22758. Contributed by @luixxiul.
 * Ensure timestamp on generic event list summary is not hidden from TimelineCard ([\#9000](https://github.com/matrix-org/matrix-react-sdk/pull/9000)). Fixes #22755. Contributed by @luixxiul.
 * Fix headings margin on security user settings tab ([\#8826](https://github.com/matrix-org/matrix-react-sdk/pull/8826)). Contributed by @luixxiul.
 * Fix timestamp position on file panel ([\#8976](https://github.com/matrix-org/matrix-react-sdk/pull/8976)). Fixes #22718. Contributed by @luixxiul.
 * Stop using :not() pseudo class for mx_GenericEventListSummary ([\#8944](https://github.com/matrix-org/matrix-react-sdk/pull/8944)). Fixes #22602. Contributed by @luixxiul.
 * Don't show the same user twice in Spotlight ([\#8978](https://github.com/matrix-org/matrix-react-sdk/pull/8978)). Fixes #22697.
 * Align the right edge of expand / collapse link buttons of generic event list summary in bubble layout with a variable ([\#8992](https://github.com/matrix-org/matrix-react-sdk/pull/8992)). Fixes #22743. Contributed by @luixxiul.
 * Display own avatars on search results panel in bubble layout ([\#8990](https://github.com/matrix-org/matrix-react-sdk/pull/8990)). Contributed by @luixxiul.
 * Fix text flow of thread summary content on threads list ([\#8991](https://github.com/matrix-org/matrix-react-sdk/pull/8991)). Fixes #22738. Contributed by @luixxiul.
 * Fix the size of the clickable area of images ([\#8987](https://github.com/matrix-org/matrix-react-sdk/pull/8987)). Fixes #22282.
 * Fix font size of MessageTimestamp on TimelineCard ([\#8950](https://github.com/matrix-org/matrix-react-sdk/pull/8950)). Contributed by @luixxiul.
 * Improve security room settings tab style rules ([\#8844](https://github.com/matrix-org/matrix-react-sdk/pull/8844)). Fixes #22575. Contributed by @luixxiul.
 * Align E2E icon and avatar of info tile in compact modern layout ([\#8965](https://github.com/matrix-org/matrix-react-sdk/pull/8965)). Fixes #22652. Contributed by @luixxiul.
 * Fix clickable area of general event list summary toggle ([\#8979](https://github.com/matrix-org/matrix-react-sdk/pull/8979)). Fixes #22722. Contributed by @luixxiul.
 * Fix resizing room topic ([\#8966](https://github.com/matrix-org/matrix-react-sdk/pull/8966)). Fixes #22689.
 * Dismiss the search dialogue when starting a DM ([\#8967](https://github.com/matrix-org/matrix-react-sdk/pull/8967)). Fixes #22700.
 * Fix "greyed out" text style inconsistency on search result panel ([\#8974](https://github.com/matrix-org/matrix-react-sdk/pull/8974)). Contributed by @luixxiul.
 * Add top padding to EventTilePreview loader ([\#8977](https://github.com/matrix-org/matrix-react-sdk/pull/8977)). Fixes #22719. Contributed by @luixxiul.
 * Fix read receipts group position on TimelineCard in compact modern/group layout ([\#8971](https://github.com/matrix-org/matrix-react-sdk/pull/8971)). Fixes #22715. Contributed by @luixxiul.
 * Fix calls on homeservers without the unstable thirdparty endpoints. ([\#8931](https://github.com/matrix-org/matrix-react-sdk/pull/8931)). Fixes #21680. Contributed by @deepbluev7.
 * Enable ReplyChain text to be expanded on IRC layout ([\#8959](https://github.com/matrix-org/matrix-react-sdk/pull/8959)). Fixes #22709. Contributed by @luixxiul.
 * Fix hidden timestamp on message edit history dialog ([\#8955](https://github.com/matrix-org/matrix-react-sdk/pull/8955)). Fixes #22701. Contributed by @luixxiul.
 * Enable ReplyChain text to be expanded on bubble layout ([\#8958](https://github.com/matrix-org/matrix-react-sdk/pull/8958)). Fixes #22709. Contributed by @luixxiul.
 * Fix expand/collapse state wrong in metaspaces ([\#8952](https://github.com/matrix-org/matrix-react-sdk/pull/8952)). Fixes #22632.
 * Location (live) share replies now provide a fallback content ([\#8949](https://github.com/matrix-org/matrix-react-sdk/pull/8949)).
 * Fix space settings not opening for script-created spaces ([\#8957](https://github.com/matrix-org/matrix-react-sdk/pull/8957)). Fixes #22703.
 * Respect `filename` field on `m.file` events ([\#8951](https://github.com/matrix-org/matrix-react-sdk/pull/8951)).
 * Fix PlatformSettingsHandler always returning true due to returning a Promise ([\#8954](https://github.com/matrix-org/matrix-react-sdk/pull/8954)). Fixes #22616.
 * Improve high-contrast support for spotlight ([\#8948](https://github.com/matrix-org/matrix-react-sdk/pull/8948)). Fixes #22481. Contributed by @justjanne.
 * Fix wrong assertions that all media events have a mimetype ([\#8946](https://github.com/matrix-org/matrix-react-sdk/pull/8946)). Fixes matrix-org/element-web-rageshakes#13727.
 * Make invite dialogue fixed height ([\#8934](https://github.com/matrix-org/matrix-react-sdk/pull/8934)). Fixes #22659.
 * Fix all megolm error reported as unknown ([\#8916](https://github.com/matrix-org/matrix-react-sdk/pull/8916)).
 * Remove line-height declarations from _ReplyTile.scss ([\#8932](https://github.com/matrix-org/matrix-react-sdk/pull/8932)). Fixes #22687. Contributed by @luixxiul.
 * Reduce video rooms log spam ([\#8913](https://github.com/matrix-org/matrix-react-sdk/pull/8913)).
 * Correct new search input’s rounded corners ([\#8921](https://github.com/matrix-org/matrix-react-sdk/pull/8921)). Fixes #22576. Contributed by @justjanne.
 * Align unread notification dot on threads list in compact modern=group layout ([\#8911](https://github.com/matrix-org/matrix-react-sdk/pull/8911)). Fixes #22677. Contributed by @luixxiul.

Changes in [1.11.0](https://github.com/vector-im/element-web/releases/tag/v1.11.0) (2022-07-05)
===============================================================================================

## 🚨 BREAKING CHANGES
 * Remove Piwik support ([\#8835](https://github.com/matrix-org/matrix-react-sdk/pull/8835)).

## ✨ Features
 * Document how to configure a custom `home.html`. ([\#21066](https://github.com/vector-im/element-web/pull/21066)). Contributed by @johannes-krude.
 * Move New Search Experience out of beta ([\#8859](https://github.com/matrix-org/matrix-react-sdk/pull/8859)). Contributed by @justjanne.
 * Switch video rooms to spotlight layout when in PiP mode ([\#8912](https://github.com/matrix-org/matrix-react-sdk/pull/8912)). Fixes #22574.
 * Live location sharing - render message deleted tile for redacted beacons ([\#8905](https://github.com/matrix-org/matrix-react-sdk/pull/8905)). Contributed by @kerryarchibald.
 * Improve view source dialog style ([\#8883](https://github.com/matrix-org/matrix-react-sdk/pull/8883)). Fixes #22636. Contributed by @luixxiul.
 * Improve integration manager dialog style ([\#8888](https://github.com/matrix-org/matrix-react-sdk/pull/8888)). Fixes #22642. Contributed by @luixxiul.
 * Implement MSC3827: Filtering of `/publicRooms` by room type ([\#8866](https://github.com/matrix-org/matrix-react-sdk/pull/8866)). Fixes #22578.
 * Show chat panel when opening a video room with unread messages ([\#8812](https://github.com/matrix-org/matrix-react-sdk/pull/8812)). Fixes #22527.
 * Live location share - forward latest location ([\#8860](https://github.com/matrix-org/matrix-react-sdk/pull/8860)). Contributed by @kerryarchibald.
 * Allow integration managers to validate user identity after opening ([\#8782](https://github.com/matrix-org/matrix-react-sdk/pull/8782)). Contributed by @Half-Shot.
 * Create a common header on right panel cards on BaseCard ([\#8808](https://github.com/matrix-org/matrix-react-sdk/pull/8808)). Contributed by @luixxiul.
 * Integrate searching public rooms and people into the new search experience ([\#8707](https://github.com/matrix-org/matrix-react-sdk/pull/8707)). Fixes #21354 and #19349. Contributed by @justjanne.
 * Bring back waveform for voice messages and retain seeking ([\#8843](https://github.com/matrix-org/matrix-react-sdk/pull/8843)). Fixes #21904.
 * Improve colors in settings  ([\#7283](https://github.com/matrix-org/matrix-react-sdk/pull/7283)).
 * Keep draft in composer when a slash command syntax errors ([\#8811](https://github.com/matrix-org/matrix-react-sdk/pull/8811)). Fixes #22384.
 * Release video rooms as a beta feature ([\#8431](https://github.com/matrix-org/matrix-react-sdk/pull/8431)).
 * Clarify logout key backup warning dialog. Contributed by @notramo. ([\#8741](https://github.com/matrix-org/matrix-react-sdk/pull/8741)). Fixes #15565. Contributed by @MadLittleMods.
 * Slightly improve the look of the `Message edits` dialog ([\#8763](https://github.com/matrix-org/matrix-react-sdk/pull/8763)). Fixes #22410.
 * Add support for MD / HTML in room topics ([\#8215](https://github.com/matrix-org/matrix-react-sdk/pull/8215)). Fixes #5180. Contributed by @Johennes.
 * Live location share - link to timeline tile from share warning ([\#8752](https://github.com/matrix-org/matrix-react-sdk/pull/8752)). Contributed by @kerryarchibald.
 * Improve composer visiblity ([\#8578](https://github.com/matrix-org/matrix-react-sdk/pull/8578)). Fixes #22072 and #17362.
 * Makes the avatar of the user menu non-draggable ([\#8765](https://github.com/matrix-org/matrix-react-sdk/pull/8765)). Contributed by @luixxiul.
 * Improve widget buttons behaviour and layout ([\#8734](https://github.com/matrix-org/matrix-react-sdk/pull/8734)).
 * Use AccessibleButton for 'Reset All' link button on SetupEncryptionBody ([\#8730](https://github.com/matrix-org/matrix-react-sdk/pull/8730)). Contributed by @luixxiul.
 * Adjust message timestamp position on TimelineCard in non-bubble layouts ([\#8745](https://github.com/matrix-org/matrix-react-sdk/pull/8745)). Fixes #22426. Contributed by @luixxiul.
 * Use AccessibleButton for 'In reply to' link button on ReplyChain ([\#8726](https://github.com/matrix-org/matrix-react-sdk/pull/8726)). Fixes #22407. Contributed by @luixxiul.
 * Live location share - enable reply and react to tiles ([\#8721](https://github.com/matrix-org/matrix-react-sdk/pull/8721)). Contributed by @kerryarchibald.
 * Change dash to em dash issues fixed ([\#8455](https://github.com/matrix-org/matrix-react-sdk/pull/8455)). Fixes #21895. Contributed by @goelesha.

## 🐛 Bug Fixes
 * Reduce video rooms log spam ([\#22665](https://github.com/vector-im/element-web/pull/22665)).
 * Connect to Jitsi unmuted by default ([\#22660](https://github.com/vector-im/element-web/pull/22660)). Fixes #22637.
 * Work around a Jitsi bug with display name encoding ([\#22525](https://github.com/vector-im/element-web/pull/22525)). Fixes #22521.
 * Make invite dialogue fixed height ([\#8945](https://github.com/matrix-org/matrix-react-sdk/pull/8945)).
 * Correct issue with tab order in new search experience ([\#8919](https://github.com/matrix-org/matrix-react-sdk/pull/8919)). Fixes #22670. Contributed by @justjanne.
 * Clicking location replies now redirects to the replied event instead of opening the map ([\#8918](https://github.com/matrix-org/matrix-react-sdk/pull/8918)). Fixes #22667.
 * Keep clicks on pills within the app ([\#8917](https://github.com/matrix-org/matrix-react-sdk/pull/8917)). Fixes #22653.
 * Don't overlap tile bubbles with timestamps in modern layout ([\#8908](https://github.com/matrix-org/matrix-react-sdk/pull/8908)). Fixes #22425.
 * Connect to Jitsi unmuted by default ([\#8909](https://github.com/matrix-org/matrix-react-sdk/pull/8909)).
 * Maximize width value of display name on TimelineCard with IRC/modern layout ([\#8904](https://github.com/matrix-org/matrix-react-sdk/pull/8904)). Fixes #22651. Contributed by @luixxiul.
 * Align the avatar and the display name on TimelineCard ([\#8900](https://github.com/matrix-org/matrix-react-sdk/pull/8900)). Contributed by @luixxiul.
 * Remove inline margin from reactions row on IRC layout ([\#8891](https://github.com/matrix-org/matrix-react-sdk/pull/8891)). Fixes #22644. Contributed by @luixxiul.
 * Align "From a thread" on search result panel on IRC layout ([\#8892](https://github.com/matrix-org/matrix-react-sdk/pull/8892)). Fixes #22645. Contributed by @luixxiul.
 * Display description of E2E advanced panel as subsection text ([\#8889](https://github.com/matrix-org/matrix-react-sdk/pull/8889)). Contributed by @luixxiul.
 * Remove inline end margin from images on file panel ([\#8886](https://github.com/matrix-org/matrix-react-sdk/pull/8886)). Fixes #22640. Contributed by @luixxiul.
 * Disable option to `Quote` when we don't have sufficient permissions ([\#8893](https://github.com/matrix-org/matrix-react-sdk/pull/8893)). Fixes #22643.
 * Add padding to font scaling loader for message bubble layout ([\#8875](https://github.com/matrix-org/matrix-react-sdk/pull/8875)). Fixes #22626. Contributed by @luixxiul.
 * Set 100% max-width to display name on reply tiles ([\#8867](https://github.com/matrix-org/matrix-react-sdk/pull/8867)). Fixes #22615. Contributed by @luixxiul.
 * Fix alignment of pill letter ([\#8874](https://github.com/matrix-org/matrix-react-sdk/pull/8874)). Fixes #22622. Contributed by @luixxiul.
 * Move the beta pill to the right side and display the pill on video room only ([\#8873](https://github.com/matrix-org/matrix-react-sdk/pull/8873)). Fixes #22619 and #22620. Contributed by @luixxiul.
 * Stop using absolute property to place beta pill on RoomPreviewCard ([\#8872](https://github.com/matrix-org/matrix-react-sdk/pull/8872)). Fixes #22617. Contributed by @luixxiul.
 * Make the pill text single line ([\#8744](https://github.com/matrix-org/matrix-react-sdk/pull/8744)). Fixes #22427. Contributed by @luixxiul.
 * Hide overflow of public room description on spotlight dialog result ([\#8870](https://github.com/matrix-org/matrix-react-sdk/pull/8870)). Contributed by @luixxiul.
 * Fix position of message action bar on the info tile on TimelineCard in message bubble layout ([\#8865](https://github.com/matrix-org/matrix-react-sdk/pull/8865)). Fixes #22614. Contributed by @luixxiul.
 * Remove inline start margin from display name on reply tiles on TimelineCard ([\#8864](https://github.com/matrix-org/matrix-react-sdk/pull/8864)). Fixes #22613. Contributed by @luixxiul.
 * Improve homeserver dropdown dialog styling ([\#8850](https://github.com/matrix-org/matrix-react-sdk/pull/8850)). Fixes #22552. Contributed by @justjanne.
 * Fix crash when drawing blurHash for portrait videos PSB-139 ([\#8855](https://github.com/matrix-org/matrix-react-sdk/pull/8855)). Fixes #22597. Contributed by @andybalaam.
 * Fix grid blowout on pinned event tiles ([\#8816](https://github.com/matrix-org/matrix-react-sdk/pull/8816)). Fixes #22543. Contributed by @luixxiul.
 * Fix temporary sync errors if there's weird settings stored in account data ([\#8857](https://github.com/matrix-org/matrix-react-sdk/pull/8857)).
 * Fix reactions row overflow and gap between reactions ([\#8813](https://github.com/matrix-org/matrix-react-sdk/pull/8813)). Fixes #22093. Contributed by @luixxiul.
 * Fix issues with the Create new room button in Spotlight ([\#8851](https://github.com/matrix-org/matrix-react-sdk/pull/8851)). Contributed by @justjanne.
 * Remove margin from E2E icon between avatar and hidden event ([\#8584](https://github.com/matrix-org/matrix-react-sdk/pull/8584)). Fixes #22186. Contributed by @luixxiul.
 * Fix waveform on a message bubble ([\#8852](https://github.com/matrix-org/matrix-react-sdk/pull/8852)). Contributed by @luixxiul.
 * Location sharing maps are now loaded after reconnection ([\#8848](https://github.com/matrix-org/matrix-react-sdk/pull/8848)). Fixes #20993.
 * Update the avatar mask so it doesn’t cut off spaces’ avatars anymore ([\#8849](https://github.com/matrix-org/matrix-react-sdk/pull/8849)). Contributed by @justjanne.
 * Add a bit of safety around timestamp handling for threads ([\#8845](https://github.com/matrix-org/matrix-react-sdk/pull/8845)).
 * Remove top margin from event tile on a narrow viewport ([\#8814](https://github.com/matrix-org/matrix-react-sdk/pull/8814)). Contributed by @luixxiul.
 * Fix keyboard shortcuts on settings tab being wrapped ([\#8825](https://github.com/matrix-org/matrix-react-sdk/pull/8825)). Fixes #22547. Contributed by @luixxiul.
 * Add try-catch around blurhash loading ([\#8830](https://github.com/matrix-org/matrix-react-sdk/pull/8830)).
 * Prevent new composer from overflowing from non-breakable text ([\#8829](https://github.com/matrix-org/matrix-react-sdk/pull/8829)). Fixes #22507. Contributed by @justjanne.
 * Use common subheading on sidebar user settings tab ([\#8823](https://github.com/matrix-org/matrix-react-sdk/pull/8823)). Contributed by @luixxiul.
 * Fix clickable area of advanced toggle on appearance user settings tab ([\#8820](https://github.com/matrix-org/matrix-react-sdk/pull/8820)). Fixes #22546. Contributed by @luixxiul.
 * Disable redacting reactions if we don't have sufficient permissions  ([\#8767](https://github.com/matrix-org/matrix-react-sdk/pull/8767)). Fixes #22262.
 * Update the live timeline when the JS SDK resets it ([\#8806](https://github.com/matrix-org/matrix-react-sdk/pull/8806)). Fixes #22421.
 * Fix flex blowout on image reply ([\#8809](https://github.com/matrix-org/matrix-react-sdk/pull/8809)). Fixes #22509 and #22510. Contributed by @luixxiul.
 * Enable background color on hover for chat panel and thread panel ([\#8644](https://github.com/matrix-org/matrix-react-sdk/pull/8644)). Fixes #22273. Contributed by @luixxiul.
 * Fix #20026: send read marker as soon as we change it ([\#8802](https://github.com/matrix-org/matrix-react-sdk/pull/8802)). Fixes #20026. Contributed by @andybalaam.
 * Allow AppTiles to shrink as much as necessary ([\#8805](https://github.com/matrix-org/matrix-react-sdk/pull/8805)). Fixes #22499.
 * Make widgets in video rooms immutable again ([\#8803](https://github.com/matrix-org/matrix-react-sdk/pull/8803)). Fixes #22497.
 * Use MessageActionBar style declarations on pinned message card ([\#8757](https://github.com/matrix-org/matrix-react-sdk/pull/8757)). Fixes #22444. Contributed by @luixxiul.
 * Expire video member events after 1 hour ([\#8776](https://github.com/matrix-org/matrix-react-sdk/pull/8776)).
 * Name lists on invite dialog ([\#8046](https://github.com/matrix-org/matrix-react-sdk/pull/8046)). Fixes #21400 and #19463. Contributed by @luixxiul.
 * Live location share - show loading UI for beacons with start timestamp in the future ([\#8775](https://github.com/matrix-org/matrix-react-sdk/pull/8775)). Fixes #22437. Contributed by @kerryarchibald.
 * Fix scroll jump issue with the composer ([\#8788](https://github.com/matrix-org/matrix-react-sdk/pull/8788)). Fixes #22464.
 * Fix the incorrect nesting of download button on MessageActionBar ([\#8785](https://github.com/matrix-org/matrix-react-sdk/pull/8785)). Contributed by @luixxiul.
 * Revert link color change in composer ([\#8784](https://github.com/matrix-org/matrix-react-sdk/pull/8784)). Fixes #22468.
 * Fix 'Logout' inline link on the splash screen ([\#8770](https://github.com/matrix-org/matrix-react-sdk/pull/8770)). Fixes #22449. Contributed by @luixxiul.
 * Fix disappearing widget poput button when changing the widget layout ([\#8754](https://github.com/matrix-org/matrix-react-sdk/pull/8754)).
 * Reduce gutter with the new read receipt UI ([\#8736](https://github.com/matrix-org/matrix-react-sdk/pull/8736)). Fixes #21890.
 * Add ellipsis effect to hidden beacon status ([\#8755](https://github.com/matrix-org/matrix-react-sdk/pull/8755)). Fixes #22441. Contributed by @luixxiul.
 * Make the pill on the basic message composer compatible with display name in RTL languages ([\#8758](https://github.com/matrix-org/matrix-react-sdk/pull/8758)). Fixes #22445. Contributed by @luixxiul.
 * Prevent the banner text from being selected, replacing the spacing values with the variable ([\#8756](https://github.com/matrix-org/matrix-react-sdk/pull/8756)). Fixes #22442. Contributed by @luixxiul.
 * Ensure the first device on a newly-registered account gets cross-signed properly ([\#8750](https://github.com/matrix-org/matrix-react-sdk/pull/8750)). Fixes #21977. Contributed by @duxovni.
 * Hide live location option in threads composer ([\#8746](https://github.com/matrix-org/matrix-react-sdk/pull/8746)). Fixes #22424. Contributed by @kerryarchibald.
 * Make sure MessageTimestamp is not hidden by EventTile_line on TimelineCard ([\#8748](https://github.com/matrix-org/matrix-react-sdk/pull/8748)). Contributed by @luixxiul.
 * Make PiP motion smoother and react to window resizes correctly ([\#8747](https://github.com/matrix-org/matrix-react-sdk/pull/8747)). Fixes #22292.
 * Prevent Invite and DevTools dialogs from being cut off ([\#8646](https://github.com/matrix-org/matrix-react-sdk/pull/8646)). Fixes #20911 and undefined/matrix-react-sdk#8165. Contributed by @justjanne.
 * Squish event bubble tiles less ([\#8740](https://github.com/matrix-org/matrix-react-sdk/pull/8740)).
 * Use random widget IDs for video rooms ([\#8739](https://github.com/matrix-org/matrix-react-sdk/pull/8739)). Fixes #22417.
 * Fix read avatars overflow from the right chat panel with a maximized widget on bubble message layout ([\#8470](https://github.com/matrix-org/matrix-react-sdk/pull/8470)). Contributed by @luixxiul.
 * Fix `CallView` crash ([\#8735](https://github.com/matrix-org/matrix-react-sdk/pull/8735)). Fixes #22394.

Changes in [1.10.15](https://github.com/vector-im/element-web/releases/tag/v1.10.15) (2022-06-14)
=================================================================================================

## 🐛 Bug Fixes
 * Fix missing element desktop preferences ([\#8798](https://github.com/matrix-org/matrix-react-sdk/pull/8798)). Contributed by @t3chguy.

Changes in [1.10.14](https://github.com/vector-im/element-web/releases/tag/v1.10.14) (2022-06-07)
=================================================================================================

## ✨ Features
 * Make Lao translation available ([\#22358](https://github.com/vector-im/element-web/pull/22358)). Fixes #22327.
 * Option to disable hardware acceleration on Element Desktop ([\#22295](https://github.com/vector-im/element-web/pull/22295)). Contributed by @novocaine.
 * Configure custom home.html via `.well-known/matrix/client["io.element.embedded_pages"]["home_url"]` for all your element-web/desktop users ([\#7790](https://github.com/matrix-org/matrix-react-sdk/pull/7790)). Contributed by @johannes-krude.
 * Live location sharing - open location in OpenStreetMap ([\#8695](https://github.com/matrix-org/matrix-react-sdk/pull/8695)). Contributed by @kerryarchibald.
 * Show a dialog when Jitsi encounters an error ([\#8701](https://github.com/matrix-org/matrix-react-sdk/pull/8701)). Fixes #22284.
 * Add support for setting the `avatar_url` of widgets by integration managers. ([\#8550](https://github.com/matrix-org/matrix-react-sdk/pull/8550)). Contributed by @Fox32.
 * Add an option to ignore (block) a user when reporting their events ([\#8471](https://github.com/matrix-org/matrix-react-sdk/pull/8471)).
 * Add the option to disable hardware acceleration ([\#8655](https://github.com/matrix-org/matrix-react-sdk/pull/8655)). Contributed by @novocaine.
 * Slightly better presentation of read receipts to screen reader users ([\#8662](https://github.com/matrix-org/matrix-react-sdk/pull/8662)). Fixes #22293. Contributed by @pvagner.
 * Add jump to related event context menu item ([\#6775](https://github.com/matrix-org/matrix-react-sdk/pull/6775)). Fixes #19883.
 * Add public room directory hook ([\#8626](https://github.com/matrix-org/matrix-react-sdk/pull/8626)).

## 🐛 Bug Fixes
 * Stop Jitsi if we time out while connecting to a video room ([\#22301](https://github.com/vector-im/element-web/pull/22301)). Fixes #22283.
 * Remove inline margin from UTD error message inside a reply tile on ThreadView ([\#8708](https://github.com/matrix-org/matrix-react-sdk/pull/8708)). Fixes #22376. Contributed by @luixxiul.
 * Move unread notification dots of the threads list to the expected position ([\#8700](https://github.com/matrix-org/matrix-react-sdk/pull/8700)). Fixes #22350. Contributed by @luixxiul.
 * Prevent overflow of grid items on a bubble with UTD generally ([\#8697](https://github.com/matrix-org/matrix-react-sdk/pull/8697)). Contributed by @luixxiul.
 * Create 'Unable To Decrypt' grid layout for hidden events on a bubble layout ([\#8704](https://github.com/matrix-org/matrix-react-sdk/pull/8704)). Fixes #22365. Contributed by @luixxiul.
 * Fix - AccessibleButton does not set disabled attribute ([\#8682](https://github.com/matrix-org/matrix-react-sdk/pull/8682)). Contributed by @kerryarchibald.
 * Fix font not resetting when logging out ([\#8670](https://github.com/matrix-org/matrix-react-sdk/pull/8670)). Fixes #17228.
 * Fix local aliases section of room settings not working for some homeservers (ie ([\#8698](https://github.com/matrix-org/matrix-react-sdk/pull/8698)). Fixes #22337.
 * Align EventTile_line with display name on message bubble ([\#8692](https://github.com/matrix-org/matrix-react-sdk/pull/8692)). Fixes #22343. Contributed by @luixxiul.
 * Convert references to direct chat -> direct message ([\#8694](https://github.com/matrix-org/matrix-react-sdk/pull/8694)). Contributed by @novocaine.
 * Improve combining diacritics for U+20D0 to U+20F0 in Chrome ([\#8687](https://github.com/matrix-org/matrix-react-sdk/pull/8687)).
 * Make the empty thread panel fill BaseCard ([\#8690](https://github.com/matrix-org/matrix-react-sdk/pull/8690)). Fixes #22338. Contributed by @luixxiul.
 * Fix edge case around composer handling gendered facepalm emoji ([\#8686](https://github.com/matrix-org/matrix-react-sdk/pull/8686)).
 * Fix a grid blowout due to nowrap displayName on a bubble with UTD ([\#8688](https://github.com/matrix-org/matrix-react-sdk/pull/8688)). Fixes #21914. Contributed by @luixxiul.
 * Apply the same max-width to image tile on the thread timeline as message bubble ([\#8669](https://github.com/matrix-org/matrix-react-sdk/pull/8669)). Fixes #22313. Contributed by @luixxiul.
 * Fix dropdown button size for picture-in-picture CallView ([\#8680](https://github.com/matrix-org/matrix-react-sdk/pull/8680)). Fixes #22316. Contributed by @luixxiul.
 * Live location sharing - fix square border for image-less avatar (PSF-1052) ([\#8679](https://github.com/matrix-org/matrix-react-sdk/pull/8679)). Contributed by @kerryarchibald.
 * Stop connecting to a video room if the widget messaging disappears ([\#8660](https://github.com/matrix-org/matrix-react-sdk/pull/8660)).
 * Fix file button and audio player overflowing from message bubble ([\#8666](https://github.com/matrix-org/matrix-react-sdk/pull/8666)). Fixes #22308. Contributed by @luixxiul.
 * Don't show broken composer format bar when selection is whitespace ([\#8673](https://github.com/matrix-org/matrix-react-sdk/pull/8673)). Fixes #10788.
 * Fix media upload http 413 handling ([\#8674](https://github.com/matrix-org/matrix-react-sdk/pull/8674)).
 * Fix emoji picker for editing thread responses ([\#8671](https://github.com/matrix-org/matrix-react-sdk/pull/8671)). Fixes matrix-org/element-web-rageshakes#13129.
 * Map attribution while sharing live location is now visible ([\#8621](https://github.com/matrix-org/matrix-react-sdk/pull/8621)). Fixes #22236. Contributed by @weeman1337.
 * Fix info tile overlapping the time stamp on TimelineCard ([\#8639](https://github.com/matrix-org/matrix-react-sdk/pull/8639)). Fixes #22256. Contributed by @luixxiul.
 * Fix position of wide images on IRC / modern layout ([\#8667](https://github.com/matrix-org/matrix-react-sdk/pull/8667)). Fixes #22309. Contributed by @luixxiul.
 * Fix other user's displayName being wrapped on the bubble message layout ([\#8456](https://github.com/matrix-org/matrix-react-sdk/pull/8456)). Fixes #22004. Contributed by @luixxiul.
 * Set spacing declarations to elements in mx_EventTile_mediaLine ([\#8665](https://github.com/matrix-org/matrix-react-sdk/pull/8665)). Fixes #22307. Contributed by @luixxiul.
 * Fix wide image overflowing from the thumbnail container ([\#8663](https://github.com/matrix-org/matrix-react-sdk/pull/8663)). Fixes #22303. Contributed by @luixxiul.
 * Fix styles of "Show all" link button on ReactionsRow ([\#8658](https://github.com/matrix-org/matrix-react-sdk/pull/8658)). Fixes #22300. Contributed by @luixxiul.
 * Automatically log in after registration ([\#8654](https://github.com/matrix-org/matrix-react-sdk/pull/8654)). Fixes #19305. Contributed by @justjanne.
 * Fix offline status in window title not working reliably ([\#8656](https://github.com/matrix-org/matrix-react-sdk/pull/8656)).
 * Align input area with event body's first letter in a thread on IRC/modern layout ([\#8636](https://github.com/matrix-org/matrix-react-sdk/pull/8636)). Fixes #22252. Contributed by @luixxiul.
 * Fix crash on null idp for SSO buttons ([\#8650](https://github.com/matrix-org/matrix-react-sdk/pull/8650)). Contributed by @hughns.
 * Don't open the regular browser or our context menu on right-clicking the `Options` button in the message action bar ([\#8648](https://github.com/matrix-org/matrix-react-sdk/pull/8648)). Fixes #22279.
 * Show notifications even when Element is focused ([\#8590](https://github.com/matrix-org/matrix-react-sdk/pull/8590)). Contributed by @sumnerevans.
 * Remove padding from the buttons on edit message composer of a event tile on a thread ([\#8632](https://github.com/matrix-org/matrix-react-sdk/pull/8632)). Contributed by @luixxiul.
 * ensure metaspace changes correctly notify listeners ([\#8611](https://github.com/matrix-org/matrix-react-sdk/pull/8611)). Fixes #21006. Contributed by @justjanne.
 * Hide image banner on stickers, they have a tooltip already ([\#8641](https://github.com/matrix-org/matrix-react-sdk/pull/8641)). Fixes #22244.
 * Adjust EditMessageComposer style declarations ([\#8631](https://github.com/matrix-org/matrix-react-sdk/pull/8631)). Fixes #22231. Contributed by @luixxiul.

Changes in [1.10.13](https://github.com/vector-im/element-web/releases/tag/v1.10.13) (2022-05-24)
=================================================================================================

## ✨ Features
 * Go to space landing page when clicking on a selected space ([\#6442](https://github.com/matrix-org/matrix-react-sdk/pull/6442)). Fixes #20296.
 * Fall back to untranslated string rather than showing missing translation error ([\#8609](https://github.com/matrix-org/matrix-react-sdk/pull/8609)).
 * Show file name and size on images on hover ([\#6511](https://github.com/matrix-org/matrix-react-sdk/pull/6511)). Fixes #18197.
 * Iterate on search results for message bubbles ([\#7047](https://github.com/matrix-org/matrix-react-sdk/pull/7047)). Fixes #20315.
 * registration: redesign email verification page ([\#8554](https://github.com/matrix-org/matrix-react-sdk/pull/8554)). Fixes #21984.
 * Show full thread message in hover title on thread summary ([\#8568](https://github.com/matrix-org/matrix-react-sdk/pull/8568)). Fixes #22037.
 * Tweak video rooms copy ([\#8582](https://github.com/matrix-org/matrix-react-sdk/pull/8582)). Fixes #22176.
 * Live location share - beacon tooltip in maximised view ([\#8572](https://github.com/matrix-org/matrix-react-sdk/pull/8572)).
 * Add dialog to navigate long room topics ([\#8517](https://github.com/matrix-org/matrix-react-sdk/pull/8517)). Fixes #9623.
 * Change spaceroomfacepile tooltip if memberlist is shown ([\#8571](https://github.com/matrix-org/matrix-react-sdk/pull/8571)). Fixes #17406.
 * Improve message editing UI ([\#8483](https://github.com/matrix-org/matrix-react-sdk/pull/8483)). Fixes #9752 and #22108.
 * Make date changes more obvious ([\#6410](https://github.com/matrix-org/matrix-react-sdk/pull/6410)). Fixes #16221.
 * Enable forwarding static locations ([\#8553](https://github.com/matrix-org/matrix-react-sdk/pull/8553)).
 * Log `TimelinePanel` debugging info when opening the bug report modal ([\#8502](https://github.com/matrix-org/matrix-react-sdk/pull/8502)).
 * Improve welcome screen, add opt-out analytics ([\#8474](https://github.com/matrix-org/matrix-react-sdk/pull/8474)). Fixes #21946.
 * Converting selected text to MD link when pasting a URL ([\#8242](https://github.com/matrix-org/matrix-react-sdk/pull/8242)). Fixes #21634. Contributed by @Sinharitik589.
 * Support Inter on custom themes ([\#8399](https://github.com/matrix-org/matrix-react-sdk/pull/8399)). Fixes #16293.
 * Add a `Copy link` button to the right-click message context-menu labs feature ([\#8527](https://github.com/matrix-org/matrix-react-sdk/pull/8527)).
 * Move widget screenshots labs flag to devtools ([\#8522](https://github.com/matrix-org/matrix-react-sdk/pull/8522)).
 * Remove some labs features which don't get used or create maintenance burden: custom status, multiple integration managers, and do not disturb ([\#8521](https://github.com/matrix-org/matrix-react-sdk/pull/8521)).
 * Add a way to toggle `ScrollPanel` and `TimelinePanel` debug logs ([\#8513](https://github.com/matrix-org/matrix-react-sdk/pull/8513)).
 * Spaces: remove blue beta dot ([\#8511](https://github.com/matrix-org/matrix-react-sdk/pull/8511)). Fixes #22061.
 * Order new search dialog results by recency ([\#8444](https://github.com/matrix-org/matrix-react-sdk/pull/8444)).
 * Improve pills ([\#6398](https://github.com/matrix-org/matrix-react-sdk/pull/6398)). Fixes #16948 and #21281.
 * Add a way to maximize/pin widget from the PiP view ([\#7672](https://github.com/matrix-org/matrix-react-sdk/pull/7672)). Fixes #20723.
 * Iterate video room designs in labs ([\#8499](https://github.com/matrix-org/matrix-react-sdk/pull/8499)).
 * Improve UI/UX in calls ([\#7791](https://github.com/matrix-org/matrix-react-sdk/pull/7791)). Fixes #19937.
 * Add ability to change audio and video devices during a call ([\#7173](https://github.com/matrix-org/matrix-react-sdk/pull/7173)). Fixes #15595.

## 🐛 Bug Fixes
 * Fix video rooms sometimes connecting muted when they shouldn't ([\#22125](https://github.com/vector-im/element-web/pull/22125)).
 * Avoid flashing the 'join conference' button at the user in video rooms ([\#22120](https://github.com/vector-im/element-web/pull/22120)).
 * Fully close Jitsi conferences on errors ([\#22060](https://github.com/vector-im/element-web/pull/22060)).
 * Fix click behavior of notification badges on spaces ([\#8627](https://github.com/matrix-org/matrix-react-sdk/pull/8627)). Fixes #22241.
 * Add missing return values in Read Receipt animation code ([\#8625](https://github.com/matrix-org/matrix-react-sdk/pull/8625)). Fixes #22175.
 * Fix 'continue' button not working after accepting identity server terms of service ([\#8619](https://github.com/matrix-org/matrix-react-sdk/pull/8619)). Fixes #20003.
 * Proactively fix stuck devices in video rooms ([\#8587](https://github.com/matrix-org/matrix-react-sdk/pull/8587)). Fixes #22131.
 * Fix position of the message action bar on left side bubbles ([\#8398](https://github.com/matrix-org/matrix-react-sdk/pull/8398)). Fixes #21879. Contributed by @luixxiul.
 * Fix edge case thread summaries around events without a msgtype ([\#8576](https://github.com/matrix-org/matrix-react-sdk/pull/8576)).
 * Fix favourites metaspace not updating ([\#8594](https://github.com/matrix-org/matrix-react-sdk/pull/8594)). Fixes #22156.
 * Stop spaces from displaying as rooms in new breadcrumbs ([\#8595](https://github.com/matrix-org/matrix-react-sdk/pull/8595)). Fixes #22165.
 * Fix avatar position of hidden event on ThreadView ([\#8592](https://github.com/matrix-org/matrix-react-sdk/pull/8592)). Fixes #22199. Contributed by @luixxiul.
 * Fix MessageTimestamp position next to redacted messages on IRC/modern layout ([\#8591](https://github.com/matrix-org/matrix-react-sdk/pull/8591)). Fixes #22181. Contributed by @luixxiul.
 * Fix padding of messages in threads ([\#8574](https://github.com/matrix-org/matrix-react-sdk/pull/8574)). Contributed by @luixxiul.
 * Enable overflow of hidden events content ([\#8585](https://github.com/matrix-org/matrix-react-sdk/pull/8585)). Fixes #22187. Contributed by @luixxiul.
 * Increase composer line height to avoid cutting off emoji ([\#8583](https://github.com/matrix-org/matrix-react-sdk/pull/8583)). Fixes #22170.
 * Don't consider threads for breaking continuation until actually created ([\#8581](https://github.com/matrix-org/matrix-react-sdk/pull/8581)). Fixes #22164.
 * Fix displaying hidden events on threads  ([\#8555](https://github.com/matrix-org/matrix-react-sdk/pull/8555)). Fixes #22058. Contributed by @luixxiul.
 * Fix button width and align 絵文字 (emoji) on the user panel ([\#8562](https://github.com/matrix-org/matrix-react-sdk/pull/8562)). Fixes #22142. Contributed by @luixxiul.
 * Standardise the margin for settings tabs ([\#7963](https://github.com/matrix-org/matrix-react-sdk/pull/7963)). Fixes #20767. Contributed by @yuktea.
 * Fix room history not being visible even if we have historical keys ([\#8563](https://github.com/matrix-org/matrix-react-sdk/pull/8563)). Fixes #16983.
 * Fix oblong avatars in video room lobbies ([\#8565](https://github.com/matrix-org/matrix-react-sdk/pull/8565)).
 * Update thread summary when latest event gets decrypted ([\#8564](https://github.com/matrix-org/matrix-react-sdk/pull/8564)). Fixes #22151.
 * Fix codepath which can wrongly cause automatic space switch from all rooms ([\#8560](https://github.com/matrix-org/matrix-react-sdk/pull/8560)). Fixes #21373.
 * Fix effect of URL preview toggle not updating live ([\#8561](https://github.com/matrix-org/matrix-react-sdk/pull/8561)). Fixes #22148.
 * Fix visual bugs on AccessSecretStorageDialog ([\#8160](https://github.com/matrix-org/matrix-react-sdk/pull/8160)). Fixes #19426. Contributed by @luixxiul.
 * Fix the width bounce of the clock on the AudioPlayer ([\#8320](https://github.com/matrix-org/matrix-react-sdk/pull/8320)). Fixes #21788. Contributed by @luixxiul.
 * Hide the verification left stroke only on the thread list ([\#8525](https://github.com/matrix-org/matrix-react-sdk/pull/8525)). Fixes #22132. Contributed by @luixxiul.
 * Hide recently_viewed dropdown when other modal opens ([\#8538](https://github.com/matrix-org/matrix-react-sdk/pull/8538)). Contributed by @yaya-usman.
 * Only jump to date after pressing the 'go' button ([\#8548](https://github.com/matrix-org/matrix-react-sdk/pull/8548)). Fixes #20799.
 * Fix download button not working on events that were decrypted too late ([\#8556](https://github.com/matrix-org/matrix-react-sdk/pull/8556)). Fixes #19427.
 * Align thread summary button with bubble messages on the left side ([\#8388](https://github.com/matrix-org/matrix-react-sdk/pull/8388)). Fixes #21873. Contributed by @luixxiul.
 * Fix unresponsive notification toggles ([\#8549](https://github.com/matrix-org/matrix-react-sdk/pull/8549)). Fixes #22109.
 * Set color-scheme property in themes ([\#8547](https://github.com/matrix-org/matrix-react-sdk/pull/8547)). Fixes #22124.
 * Improve the styling of error messages during search initialization. ([\#6899](https://github.com/matrix-org/matrix-react-sdk/pull/6899)). Fixes #19245 and #18164. Contributed by @KalleStruik.
 * Don't leave button tooltips open when closing modals ([\#8546](https://github.com/matrix-org/matrix-react-sdk/pull/8546)). Fixes #22121.
 * update matrix-analytics-events ([\#8543](https://github.com/matrix-org/matrix-react-sdk/pull/8543)).
 * Handle Jitsi Meet crashes more gracefully ([\#8541](https://github.com/matrix-org/matrix-react-sdk/pull/8541)).
 * Fix regression around pasting links ([\#8537](https://github.com/matrix-org/matrix-react-sdk/pull/8537)). Fixes #22117.
 * Fixes suggested room not ellipsized on shrinking ([\#8536](https://github.com/matrix-org/matrix-react-sdk/pull/8536)). Contributed by @yaya-usman.
 * Add global spacing between display name and location body ([\#8523](https://github.com/matrix-org/matrix-react-sdk/pull/8523)). Fixes #22111. Contributed by @luixxiul.
 * Add box-shadow to the reply preview on the main (left) panel only ([\#8397](https://github.com/matrix-org/matrix-react-sdk/pull/8397)). Fixes #21894. Contributed by @luixxiul.
 * Set line-height: 1 to RedactedBody inside GenericEventListSummary for IRC/modern layout ([\#8529](https://github.com/matrix-org/matrix-react-sdk/pull/8529)). Fixes #22112. Contributed by @luixxiul.
 * Fix position of timestamp on the chat panel in IRC layout and message edits history modal window ([\#8464](https://github.com/matrix-org/matrix-react-sdk/pull/8464)). Fixes #22011 and #22014. Contributed by @luixxiul.
 * Fix unexpected and inconsistent inheritance of line-height property for mx_TextualEvent ([\#8485](https://github.com/matrix-org/matrix-react-sdk/pull/8485)). Fixes #22041. Contributed by @luixxiul.
 * Set the same margin to the right side of NewRoomIntro on TimelineCard ([\#8453](https://github.com/matrix-org/matrix-react-sdk/pull/8453)). Contributed by @luixxiul.
 * Remove duplicate tooltip from user pills ([\#8512](https://github.com/matrix-org/matrix-react-sdk/pull/8512)).
 * Set max-width for MLocationBody and MLocationBody_map by default ([\#8519](https://github.com/matrix-org/matrix-react-sdk/pull/8519)). Fixes #21983. Contributed by @luixxiul.
 * Simplify ReplyPreview UI implementation ([\#8516](https://github.com/matrix-org/matrix-react-sdk/pull/8516)). Fixes #22091. Contributed by @luixxiul.
 * Fix thread summary overflow on narrow message panel on bubble message layout ([\#8520](https://github.com/matrix-org/matrix-react-sdk/pull/8520)). Fixes #22097. Contributed by @luixxiul.
 * Live location sharing - refresh beacon timers on tab becoming active ([\#8515](https://github.com/matrix-org/matrix-react-sdk/pull/8515)).
 * Enlarge emoji again ([\#8509](https://github.com/matrix-org/matrix-react-sdk/pull/8509)). Fixes #22086.
 * Order receipts with the most recent on the right ([\#8506](https://github.com/matrix-org/matrix-react-sdk/pull/8506)). Fixes #22044.
 * Disconnect from video rooms when leaving ([\#8500](https://github.com/matrix-org/matrix-react-sdk/pull/8500)).
 * Fix soft crash around threads when room isn't yet in store ([\#8496](https://github.com/matrix-org/matrix-react-sdk/pull/8496)). Fixes #22047.
 * Fix reading of cached room device setting values ([\#8491](https://github.com/matrix-org/matrix-react-sdk/pull/8491)).
 * Add loading spinners to threads panels ([\#8490](https://github.com/matrix-org/matrix-react-sdk/pull/8490)). Fixes #21335.
 * Fix forwarding UI papercuts ([\#8482](https://github.com/matrix-org/matrix-react-sdk/pull/8482)). Fixes #17616.

Changes in [1.10.12](https://github.com/vector-im/element-web/releases/tag/v1.10.12) (2022-05-10)
=================================================================================================

## ✨ Features
 * Made the location map change the cursor to a pointer so it looks like it's clickable (https ([\#8451](https://github.com/matrix-org/matrix-react-sdk/pull/8451)). Fixes #21991. Contributed by @Odyssey346.
 * Implement improved spacing for the thread list and timeline ([\#8337](https://github.com/matrix-org/matrix-react-sdk/pull/8337)). Fixes #21759. Contributed by @luixxiul.
 * LLS: expose way to enable live sharing labs flag from location dialog ([\#8416](https://github.com/matrix-org/matrix-react-sdk/pull/8416)).
 * Fix source text boxes in View Source modal should have full width ([\#8425](https://github.com/matrix-org/matrix-react-sdk/pull/8425)). Fixes #21938. Contributed by @EECvision.
 * Read Receipts: never show +1, if it’s just 4, show all of them ([\#8428](https://github.com/matrix-org/matrix-react-sdk/pull/8428)). Fixes #21935.
 * Add opt-in analytics to onboarding tasks ([\#8409](https://github.com/matrix-org/matrix-react-sdk/pull/8409)). Fixes #21705.
 * Allow user to control if they are signed out of all devices when changing password ([\#8259](https://github.com/matrix-org/matrix-react-sdk/pull/8259)). Fixes #2671.
 * Implement new Read Receipt design ([\#8389](https://github.com/matrix-org/matrix-react-sdk/pull/8389)). Fixes #20574.
 * Stick connected video rooms to the top of the room list ([\#8353](https://github.com/matrix-org/matrix-react-sdk/pull/8353)).
 * LLS: fix jumpy maximised map ([\#8387](https://github.com/matrix-org/matrix-react-sdk/pull/8387)).
 * Persist audio and video mute state in video rooms ([\#8376](https://github.com/matrix-org/matrix-react-sdk/pull/8376)).
 * Forcefully disconnect from video rooms on logout and tab close ([\#8375](https://github.com/matrix-org/matrix-react-sdk/pull/8375)).
 * Add local echo of connected devices in video rooms ([\#8368](https://github.com/matrix-org/matrix-react-sdk/pull/8368)).
 * Improve text of account deactivation dialog ([\#8371](https://github.com/matrix-org/matrix-react-sdk/pull/8371)). Fixes #17421.
 * Live location sharing: own live beacon status on maximised view ([\#8374](https://github.com/matrix-org/matrix-react-sdk/pull/8374)).
 * Show a lobby screen in video rooms ([\#8287](https://github.com/matrix-org/matrix-react-sdk/pull/8287)).
 * Settings toggle to disable Composer Markdown ([\#8358](https://github.com/matrix-org/matrix-react-sdk/pull/8358)). Fixes #20321.
 * Cache localStorage objects for SettingsStore ([\#8366](https://github.com/matrix-org/matrix-react-sdk/pull/8366)).
 * Bring `View Source` back from behind developer mode ([\#8369](https://github.com/matrix-org/matrix-react-sdk/pull/8369)). Fixes #21771.

## 🐛 Bug Fixes
 * Fix Jitsi Meet getting wedged at startup in some cases ([\#21995](https://github.com/vector-im/element-web/pull/21995)).
 * Fix camera getting muted when disconnecting from a video room ([\#21958](https://github.com/vector-im/element-web/pull/21958)).
 * Fix race conditions around threads ([\#8448](https://github.com/matrix-org/matrix-react-sdk/pull/8448)). Fixes #21627.
 * Fix reading of cached room device setting values ([\#8495](https://github.com/matrix-org/matrix-react-sdk/pull/8495)).
 * Fix issue with dispatch happening mid-dispatch due to js-sdk emit ([\#8473](https://github.com/matrix-org/matrix-react-sdk/pull/8473)). Fixes #22019.
 * Match MSC behaviour for threads when disabled (thread-aware mode) ([\#8476](https://github.com/matrix-org/matrix-react-sdk/pull/8476)). Fixes #22033.
 * Specify position of DisambiguatedProfile inside a thread on bubble message layout ([\#8452](https://github.com/matrix-org/matrix-react-sdk/pull/8452)). Fixes #21998. Contributed by @luixxiul.
 * Location sharing: do not trackuserlocation in location picker ([\#8466](https://github.com/matrix-org/matrix-react-sdk/pull/8466)). Fixes #22013.
 * fix text and map indent in thread view ([\#8462](https://github.com/matrix-org/matrix-react-sdk/pull/8462)). Fixes #21997.
 * Live location sharing: don't group beacon info with room creation summary ([\#8468](https://github.com/matrix-org/matrix-react-sdk/pull/8468)).
 * Don't linkify code blocks ([\#7859](https://github.com/matrix-org/matrix-react-sdk/pull/7859)). Fixes #9613.
 * read receipts: improve tooltips to show names of users ([\#8438](https://github.com/matrix-org/matrix-react-sdk/pull/8438)). Fixes #21940.
 * Fix poll overflowing a reply tile on bubble message layout ([\#8459](https://github.com/matrix-org/matrix-react-sdk/pull/8459)). Fixes #22005. Contributed by @luixxiul.
 * Fix text link buttons on UserInfo panel ([\#8247](https://github.com/matrix-org/matrix-react-sdk/pull/8247)). Fixes #21702. Contributed by @luixxiul.
 * Clear local storage settings handler cache on logout ([\#8454](https://github.com/matrix-org/matrix-react-sdk/pull/8454)). Fixes #21994.
 * Fix jump to bottom button being always displayed in non-overflowing timelines ([\#8460](https://github.com/matrix-org/matrix-react-sdk/pull/8460)). Fixes #22003.
 * fix timeline search with empty text box should do nothing ([\#8262](https://github.com/matrix-org/matrix-react-sdk/pull/8262)). Fixes #21714. Contributed by @EECvision.
 * Fixes "space panel kebab menu is rendered out of view on sub spaces"  ([\#8350](https://github.com/matrix-org/matrix-react-sdk/pull/8350)). Contributed by @yaya-usman.
 * Add margin to the location map inside ThreadView ([\#8442](https://github.com/matrix-org/matrix-react-sdk/pull/8442)). Fixes #21982. Contributed by @luixxiul.
 * Patch: "Reloading the registration page should warn about data loss" ([\#8377](https://github.com/matrix-org/matrix-react-sdk/pull/8377)). Contributed by @yaya-usman.
 * Live location sharing: fix safari timestamps pt 2 ([\#8443](https://github.com/matrix-org/matrix-react-sdk/pull/8443)).
 * Fix issue with thread notification state ignoring initial events ([\#8417](https://github.com/matrix-org/matrix-react-sdk/pull/8417)). Fixes #21927.
 * Fix event text overflow on bubble message layout ([\#8391](https://github.com/matrix-org/matrix-react-sdk/pull/8391)). Fixes #21882. Contributed by @luixxiul.
 * Disable the message action bar when hovering over the 1px border between threads on the list ([\#8429](https://github.com/matrix-org/matrix-react-sdk/pull/8429)). Fixes #21955. Contributed by @luixxiul.
 * correctly align read receipts to state events in bubble layout ([\#8419](https://github.com/matrix-org/matrix-react-sdk/pull/8419)). Fixes #21899.
 * Fix issue with underfilled timelines when barren of content ([\#8432](https://github.com/matrix-org/matrix-react-sdk/pull/8432)). Fixes #21930.
 * Fix baseline misalignment of thread panel summary by deduplication ([\#8413](https://github.com/matrix-org/matrix-react-sdk/pull/8413)).
 * Fix editing of non-html replies ([\#8418](https://github.com/matrix-org/matrix-react-sdk/pull/8418)). Fixes #21928.
 * Read Receipts "Fall from the Sky" ([\#8414](https://github.com/matrix-org/matrix-react-sdk/pull/8414)). Fixes #21888.
 * Make read receipts handle nullable roomMembers correctly ([\#8410](https://github.com/matrix-org/matrix-react-sdk/pull/8410)). Fixes #21896.
 * Don't form continuations on either side of a thread root ([\#8408](https://github.com/matrix-org/matrix-react-sdk/pull/8408)). Fixes #20908.
 * Fix centering issue with sticker placeholder ([\#8404](https://github.com/matrix-org/matrix-react-sdk/pull/8404)). Fixes #18014 and #6449.
 * Disable download option on <video/> , preferring dedicated download button ([\#8403](https://github.com/matrix-org/matrix-react-sdk/pull/8403)). Fixes #21902.
 * Fix infinite loop when pinning/unpinning persistent widgets ([\#8396](https://github.com/matrix-org/matrix-react-sdk/pull/8396)). Fixes #21864.
 * Tweak ReadReceiptGroup to better handle disambiguation ([\#8402](https://github.com/matrix-org/matrix-react-sdk/pull/8402)). Fixes #21897.
 * stop the bottom edge of buttons getting clipped in devtools ([\#8400](https://github.com/matrix-org/matrix-react-sdk/pull/8400)).
 * Fix issue with threads timelines with few events cropping events ([\#8392](https://github.com/matrix-org/matrix-react-sdk/pull/8392)). Fixes #20594.
 * Changed font-weight to 400 to support light weight font ([\#8345](https://github.com/matrix-org/matrix-react-sdk/pull/8345)). Fixes #21171. Contributed by @goelesha.
 * Fix issue with thread panel not updating when it loads on first render ([\#8382](https://github.com/matrix-org/matrix-react-sdk/pull/8382)). Fixes #21737.
 * fix: "Mention highlight and cursor hover highlight has different corner radius" ([\#8384](https://github.com/matrix-org/matrix-react-sdk/pull/8384)). Contributed by @yaya-usman.
 * Fix regression around haveRendererForEvent for hidden events ([\#8379](https://github.com/matrix-org/matrix-react-sdk/pull/8379)). Fixes #21862 and #21725.
 * Fix regression around the room list treeview keyboard a11y ([\#8385](https://github.com/matrix-org/matrix-react-sdk/pull/8385)). Fixes #21436.
 * Remove float property to let the margin between events appear on bubble message layout ([\#8373](https://github.com/matrix-org/matrix-react-sdk/pull/8373)). Fixes #21861. Contributed by @luixxiul.
 * Fix race in Registration between server change and flows fetch ([\#8359](https://github.com/matrix-org/matrix-react-sdk/pull/8359)). Fixes #21800.
 * fix rainbow breaks compound emojis ([\#8245](https://github.com/matrix-org/matrix-react-sdk/pull/8245)). Fixes #21371. Contributed by @EECvision.
 * Fix RightPanelStore handling first room on app launch wrong ([\#8370](https://github.com/matrix-org/matrix-react-sdk/pull/8370)). Fixes #21741.
 * Fix UnknownBody error message unalignment ([\#8346](https://github.com/matrix-org/matrix-react-sdk/pull/8346)). Fixes #21828. Contributed by @luixxiul.
 * Use -webkit-line-clamp for the room header topic overflow ([\#8367](https://github.com/matrix-org/matrix-react-sdk/pull/8367)). Fixes #21852. Contributed by @luixxiul.
 * Fix issue with ServerInfo crashing the modal ([\#8364](https://github.com/matrix-org/matrix-react-sdk/pull/8364)).
 * Fixes around threads beta in degraded mode ([\#8319](https://github.com/matrix-org/matrix-react-sdk/pull/8319)). Fixes #21762.

Changes in [1.10.11](https://github.com/vector-im/element-web/releases/tag/v1.10.11) (2022-04-26)
=================================================================================================

## ✨ Features
 * Handle forced disconnects from Jitsi ([\#21697](https://github.com/vector-im/element-web/pull/21697)). Fixes #21517.
 * Improve performance of switching to rooms with lots of servers and ACLs ([\#8347](https://github.com/matrix-org/matrix-react-sdk/pull/8347)).
 * Avoid a reflow when setting caret position on an empty composer ([\#8348](https://github.com/matrix-org/matrix-react-sdk/pull/8348)).
 * Add message right-click context menu as a labs feature ([\#5672](https://github.com/matrix-org/matrix-react-sdk/pull/5672)).
 * Live location sharing - basic maximised beacon map ([\#8310](https://github.com/matrix-org/matrix-react-sdk/pull/8310)).
 * Live location sharing - render users own beacons in timeline ([\#8296](https://github.com/matrix-org/matrix-react-sdk/pull/8296)).
 * Improve Threads beta around degraded mode ([\#8318](https://github.com/matrix-org/matrix-react-sdk/pull/8318)).
 * Live location sharing -  beacon in timeline happy path ([\#8285](https://github.com/matrix-org/matrix-react-sdk/pull/8285)).
 * Add copy button to View Source screen ([\#8278](https://github.com/matrix-org/matrix-react-sdk/pull/8278)). Fixes #21482. Contributed by @olivialivia.
 * Add heart effect ([\#6188](https://github.com/matrix-org/matrix-react-sdk/pull/6188)). Contributed by @CicadaCinema.
 * Update new room icon ([\#8239](https://github.com/matrix-org/matrix-react-sdk/pull/8239)).

## 🐛 Bug Fixes
 * Fix: "Code formatting button does not escape backticks" ([\#8181](https://github.com/matrix-org/matrix-react-sdk/pull/8181)). Contributed by @yaya-usman.
 * Fix beta indicator dot causing excessive CPU usage ([\#8340](https://github.com/matrix-org/matrix-react-sdk/pull/8340)). Fixes #21793.
 * Fix overlapping timestamps on empty messages ([\#8205](https://github.com/matrix-org/matrix-react-sdk/pull/8205)). Fixes #21381. Contributed by @goelesha.
 * Fix power selector not showing up in user info when state_default undefined ([\#8297](https://github.com/matrix-org/matrix-react-sdk/pull/8297)). Fixes #21669.
 * Avoid looking up settings during timeline rendering ([\#8313](https://github.com/matrix-org/matrix-react-sdk/pull/8313)). Fixes #21740.
 * Fix a soft crash with video rooms ([\#8333](https://github.com/matrix-org/matrix-react-sdk/pull/8333)).
 * Fixes call tiles overflow ([\#8096](https://github.com/matrix-org/matrix-react-sdk/pull/8096)). Fixes #20254. Contributed by @luixxiul.
 * Fix a bug with emoji autocomplete sorting where adding the final "&#58;" would cause the emoji with the typed shortcode to no longer be at the top of the autocomplete list. ([\#8086](https://github.com/matrix-org/matrix-react-sdk/pull/8086)). Fixes #19302. Contributed by @commonlawfeature.
 * Fix image preview sizing for edge cases ([\#8322](https://github.com/matrix-org/matrix-react-sdk/pull/8322)). Fixes #20088.
 * Refactor SecurityRoomSettingsTab and remove unused state ([\#8306](https://github.com/matrix-org/matrix-react-sdk/pull/8306)). Fixes matrix-org/element-web-rageshakes#12002.
 * Don't show the prompt to enable desktop notifications immediately after registration ([\#8274](https://github.com/matrix-org/matrix-react-sdk/pull/8274)).
 * Stop tracking threads if threads support is disabled ([\#8308](https://github.com/matrix-org/matrix-react-sdk/pull/8308)). Fixes #21766.
 * Fix some issues with threads rendering ([\#8305](https://github.com/matrix-org/matrix-react-sdk/pull/8305)). Fixes #21670.
 * Fix threads rendering issue in Safari ([\#8298](https://github.com/matrix-org/matrix-react-sdk/pull/8298)). Fixes #21757.
 * Fix space panel width change on hovering over space item ([\#8299](https://github.com/matrix-org/matrix-react-sdk/pull/8299)). Fixes #19891.
 * Hide the reply in thread button in deployments where beta is forcibly disabled ([\#8294](https://github.com/matrix-org/matrix-react-sdk/pull/8294)). Fixes #21753.
 * Prevent soft crash around room list header context menu when space changes ([\#8289](https://github.com/matrix-org/matrix-react-sdk/pull/8289)). Fixes matrix-org/element-web-rageshakes#11416, matrix-org/element-web-rageshakes#11692, matrix-org/element-web-rageshakes#11739, matrix-org/element-web-rageshakes#11772, matrix-org/element-web-rageshakes#11891 matrix-org/element-web-rageshakes#11858 and matrix-org/element-web-rageshakes#11456.
 * When selecting reply in thread on a thread response open existing thread ([\#8291](https://github.com/matrix-org/matrix-react-sdk/pull/8291)). Fixes #21743.
 * Handle thread bundled relationships coming from the server via MSC3666 ([\#8292](https://github.com/matrix-org/matrix-react-sdk/pull/8292)). Fixes #21450.
 * Fix: Avatar preview does not update when same file is selected repeatedly ([\#8288](https://github.com/matrix-org/matrix-react-sdk/pull/8288)). Fixes #20098.
 * Fix a bug where user gets a warning when changing powerlevel from **Admin** to **custom level (100)** ([\#8248](https://github.com/matrix-org/matrix-react-sdk/pull/8248)). Fixes #21682. Contributed by @Jumeb.
 * Use a consistent alignment for all text items in a list ([\#8276](https://github.com/matrix-org/matrix-react-sdk/pull/8276)). Fixes #21731. Contributed by @luixxiul.
 * Fixes button labels being collapsed per a character in CJK languages ([\#8212](https://github.com/matrix-org/matrix-react-sdk/pull/8212)). Fixes #21287. Contributed by @luixxiul.
 * Fix: Remove jittery timeline scrolling after jumping to an event ([\#8263](https://github.com/matrix-org/matrix-react-sdk/pull/8263)).
 * Fix regression of edits showing up in the timeline with hidden events shown ([\#8260](https://github.com/matrix-org/matrix-react-sdk/pull/8260)). Fixes #21694.
 * Fix reporting events not working ([\#8257](https://github.com/matrix-org/matrix-react-sdk/pull/8257)). Fixes #21713.
 * Make Jitsi widgets in video rooms immutable ([\#8244](https://github.com/matrix-org/matrix-react-sdk/pull/8244)). Fixes #21647.
 * Fix: Ensure links to events scroll the correct events into view ([\#8250](https://github.com/matrix-org/matrix-react-sdk/pull/8250)). Fixes #19934.

Changes in [1.10.10](https://github.com/vector-im/element-web/releases/tag/v1.10.10) (2022-04-14)
=================================================================================================

## 🐛 Bug Fixes
 * Fixes around threads beta in degraded mode ([\#8319](https://github.com/matrix-org/matrix-react-sdk/pull/8319)). Fixes #21762.

Changes in [1.10.9](https://github.com/vector-im/element-web/releases/tag/v1.10.9) (2022-04-12)
===============================================================================================

## ✨ Features
 * Release threads as a beta feature ([\#8081](https://github.com/matrix-org/matrix-react-sdk/pull/8081)). Fixes #21351.
 * More video rooms design updates ([\#8222](https://github.com/matrix-org/matrix-react-sdk/pull/8222)).
 * Update video rooms to new design specs ([\#8207](https://github.com/matrix-org/matrix-react-sdk/pull/8207)). Fixes #21515, #21516 #21519 and #21526.
 * Live Location Sharing - left panel warning with error ([\#8201](https://github.com/matrix-org/matrix-react-sdk/pull/8201)).
 * Live location sharing - Stop publishing location to beacons with consecutive errors ([\#8194](https://github.com/matrix-org/matrix-react-sdk/pull/8194)).
 * Live location sharing: allow retry when stop sharing fails ([\#8193](https://github.com/matrix-org/matrix-react-sdk/pull/8193)).
 * Allow voice messages to be scrubbed in the timeline ([\#8079](https://github.com/matrix-org/matrix-react-sdk/pull/8079)). Fixes #18713.
 * Live location sharing - stop sharing to beacons in rooms you left ([\#8187](https://github.com/matrix-org/matrix-react-sdk/pull/8187)).
 * Allow sending and thumbnailing AVIF images ([\#8172](https://github.com/matrix-org/matrix-react-sdk/pull/8172)).
 * Live location sharing - handle geolocation errors ([\#8179](https://github.com/matrix-org/matrix-react-sdk/pull/8179)).
 * Show voice room participants when not connected ([\#8136](https://github.com/matrix-org/matrix-react-sdk/pull/8136)). Fixes #21513.
 * Add margins between labs sections ([\#8169](https://github.com/matrix-org/matrix-react-sdk/pull/8169)).
 * Live location sharing - send geolocation beacon events - happy path ([\#8127](https://github.com/matrix-org/matrix-react-sdk/pull/8127)).
 * Add support for Animated (A)PNG ([\#8158](https://github.com/matrix-org/matrix-react-sdk/pull/8158)). Fixes #12967.
 * Don't form continuations from thread roots ([\#8166](https://github.com/matrix-org/matrix-react-sdk/pull/8166)). Fixes #20908.
 * Improve handling of animated GIF and WEBP images ([\#8153](https://github.com/matrix-org/matrix-react-sdk/pull/8153)). Fixes #16193 and #6684.
 * Wire up file preview for video files ([\#8140](https://github.com/matrix-org/matrix-react-sdk/pull/8140)). Fixes #21539.
 * When showing thread, always auto-focus its composer ([\#8115](https://github.com/matrix-org/matrix-react-sdk/pull/8115)). Fixes #21438.
 * Live location sharing - refresh beacon expiry in room ([\#8116](https://github.com/matrix-org/matrix-react-sdk/pull/8116)).
 * Use styled mxids in member list v2 ([\#8110](https://github.com/matrix-org/matrix-react-sdk/pull/8110)). Fixes #14825. Contributed by @SimonBrandner.
 * Delete groups (legacy communities system) ([\#8027](https://github.com/matrix-org/matrix-react-sdk/pull/8027)). Fixes #17532.
 * Add a prototype of voice rooms in labs ([\#8084](https://github.com/matrix-org/matrix-react-sdk/pull/8084)). Fixes #3546.

## 🐛 Bug Fixes
 * Avoid flashing the Jitsi prejoin screen at the user before skipping it ([\#21665](https://github.com/vector-im/element-web/pull/21665)).
 * Fix editing `<ol>` tags with a non-1 start attribute ([\#8211](https://github.com/matrix-org/matrix-react-sdk/pull/8211)). Fixes #21625.
 * Fix URL previews being enabled when room first created ([\#8227](https://github.com/matrix-org/matrix-react-sdk/pull/8227)). Fixes #21659.
 * Don't use m.call for Jitsi video rooms ([\#8223](https://github.com/matrix-org/matrix-react-sdk/pull/8223)).
 * Scale emoji with size of surrounding text ([\#8224](https://github.com/matrix-org/matrix-react-sdk/pull/8224)).
 * Make "Jump to date" translatable ([\#8218](https://github.com/matrix-org/matrix-react-sdk/pull/8218)).
 * Normalize call buttons ([\#8129](https://github.com/matrix-org/matrix-react-sdk/pull/8129)). Fixes #21493. Contributed by @luixxiul.
 * Show room preview bar with maximised widgets ([\#8180](https://github.com/matrix-org/matrix-react-sdk/pull/8180)). Fixes #21542.
 * Update more strings to not wrongly mention room when it is/could be a space ([\#7722](https://github.com/matrix-org/matrix-react-sdk/pull/7722)). Fixes #20243 and #20910.
 * Fix issue with redacting via edit composer flow causing stuck editStates ([\#8184](https://github.com/matrix-org/matrix-react-sdk/pull/8184)).
 * Fix some image/video scroll jumps ([\#8182](https://github.com/matrix-org/matrix-react-sdk/pull/8182)).
 * Fix "react error on share dialog" ([\#8170](https://github.com/matrix-org/matrix-react-sdk/pull/8170)). Contributed by @yaya-usman.
 * Fix disambiguated profile in threads in bubble layout ([\#8168](https://github.com/matrix-org/matrix-react-sdk/pull/8168)). Fixes #21570. Contributed by @SimonBrandner.
 * Responsive BetaCard on Labs ([\#8154](https://github.com/matrix-org/matrix-react-sdk/pull/8154)). Fixes #21554. Contributed by @luixxiul.
 * Display button as inline in room directory dialog ([\#8164](https://github.com/matrix-org/matrix-react-sdk/pull/8164)). Fixes #21567. Contributed by @luixxiul.
 * Null guard TimelinePanel unmount edge ([\#8171](https://github.com/matrix-org/matrix-react-sdk/pull/8171)).
 * Fix beta pill label breaking ([\#8162](https://github.com/matrix-org/matrix-react-sdk/pull/8162)). Fixes #21566. Contributed by @luixxiul.
 * Strip relations when forwarding ([\#7929](https://github.com/matrix-org/matrix-react-sdk/pull/7929)). Fixes #19769, #18067 #21015 and #10924.
 * Don't try (and fail) to show replies for redacted events ([\#8141](https://github.com/matrix-org/matrix-react-sdk/pull/8141)). Fixes #21435.
 * Fix 3pid member info for space member list ([\#8128](https://github.com/matrix-org/matrix-react-sdk/pull/8128)). Fixes #21534.
 * Set max-width to user context menu ([\#8089](https://github.com/matrix-org/matrix-react-sdk/pull/8089)). Fixes #21486. Contributed by @luixxiul.
 * Fix issue with falsey hrefs being sent in events ([\#8113](https://github.com/matrix-org/matrix-react-sdk/pull/8113)). Fixes #21417.
 * Make video sizing consistent with images ([\#8102](https://github.com/matrix-org/matrix-react-sdk/pull/8102)). Fixes #20072.

Changes in [1.10.9-rc.4](https://github.com/vector-im/element-web/releases/tag/v1.10.9-rc.4) (2022-04-11)
=========================================================================================================

Changes in [1.10.9-rc.3](https://github.com/vector-im/element-web/releases/tag/v1.10.9-rc.3) (2022-04-08)
=========================================================================================================

Changes in [1.10.9-rc.2](https://github.com/vector-im/element-web/releases/tag/v1.10.9-rc.2) (2022-04-06)
=========================================================================================================

Changes in [1.10.9-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.10.9-rc.1) (2022-04-05)
=========================================================================================================

## ✨ Features
 * Release threads as a beta feature ([\#8081](https://github.com/matrix-org/matrix-react-sdk/pull/8081)). Fixes #21351.
 * More video rooms design updates ([\#8222](https://github.com/matrix-org/matrix-react-sdk/pull/8222)).
 * Update video rooms to new design specs ([\#8207](https://github.com/matrix-org/matrix-react-sdk/pull/8207)). Fixes #21515, #21516 #21519 and #21526.
 * Live Location Sharing - left panel warning with error ([\#8201](https://github.com/matrix-org/matrix-react-sdk/pull/8201)).
 * Live location sharing - Stop publishing location to beacons with consecutive errors ([\#8194](https://github.com/matrix-org/matrix-react-sdk/pull/8194)).
 * Live location sharing: allow retry when stop sharing fails ([\#8193](https://github.com/matrix-org/matrix-react-sdk/pull/8193)).
 * Allow voice messages to be scrubbed in the timeline ([\#8079](https://github.com/matrix-org/matrix-react-sdk/pull/8079)). Fixes #18713.
 * Live location sharing - stop sharing to beacons in rooms you left ([\#8187](https://github.com/matrix-org/matrix-react-sdk/pull/8187)).
 * Allow sending and thumbnailing AVIF images ([\#8172](https://github.com/matrix-org/matrix-react-sdk/pull/8172)).
 * Live location sharing - handle geolocation errors ([\#8179](https://github.com/matrix-org/matrix-react-sdk/pull/8179)).
 * Show voice room participants when not connected ([\#8136](https://github.com/matrix-org/matrix-react-sdk/pull/8136)). Fixes #21513.
 * Add margins between labs sections ([\#8169](https://github.com/matrix-org/matrix-react-sdk/pull/8169)).
 * Live location sharing - send geolocation beacon events - happy path ([\#8127](https://github.com/matrix-org/matrix-react-sdk/pull/8127)).
 * Add support for Animated (A)PNG ([\#8158](https://github.com/matrix-org/matrix-react-sdk/pull/8158)). Fixes #12967.
 * Don't form continuations from thread roots ([\#8166](https://github.com/matrix-org/matrix-react-sdk/pull/8166)). Fixes #20908.
 * Improve handling of animated GIF and WEBP images ([\#8153](https://github.com/matrix-org/matrix-react-sdk/pull/8153)). Fixes #16193 and #6684.
 * Wire up file preview for video files ([\#8140](https://github.com/matrix-org/matrix-react-sdk/pull/8140)). Fixes #21539.
 * When showing thread, always auto-focus its composer ([\#8115](https://github.com/matrix-org/matrix-react-sdk/pull/8115)). Fixes #21438.
 * Live location sharing - refresh beacon expiry in room ([\#8116](https://github.com/matrix-org/matrix-react-sdk/pull/8116)).
 * Use styled mxids in member list v2 ([\#8110](https://github.com/matrix-org/matrix-react-sdk/pull/8110)). Fixes #14825. Contributed by @SimonBrandner.
 * Delete groups (legacy communities system) ([\#8027](https://github.com/matrix-org/matrix-react-sdk/pull/8027)). Fixes #17532.
 * Add a prototype of voice rooms in labs ([\#8084](https://github.com/matrix-org/matrix-react-sdk/pull/8084)). Fixes #3546.

## 🐛 Bug Fixes
 * Fix URL previews being enabled when room first created ([\#8227](https://github.com/matrix-org/matrix-react-sdk/pull/8227)). Fixes #21659.
 * Don't use m.call for Jitsi video rooms ([\#8223](https://github.com/matrix-org/matrix-react-sdk/pull/8223)).
 * Scale emoji with size of surrounding text ([\#8224](https://github.com/matrix-org/matrix-react-sdk/pull/8224)).
 * Make "Jump to date" translatable ([\#8218](https://github.com/matrix-org/matrix-react-sdk/pull/8218)).
 * Normalize call buttons ([\#8129](https://github.com/matrix-org/matrix-react-sdk/pull/8129)). Fixes #21493. Contributed by @luixxiul.
 * Fix editing <ol> tags with a non-1 start attribute ([\#8211](https://github.com/matrix-org/matrix-react-sdk/pull/8211)). Fixes #21625.
 * Show room preview bar with maximised widgets ([\#8180](https://github.com/matrix-org/matrix-react-sdk/pull/8180)). Fixes #21542.
 * Update more strings to not wrongly mention room when it is/could be a space ([\#7722](https://github.com/matrix-org/matrix-react-sdk/pull/7722)). Fixes #20243 and #20910.
 * Fix issue with redacting via edit composer flow causing stuck editStates ([\#8184](https://github.com/matrix-org/matrix-react-sdk/pull/8184)).
 * Fix some image/video scroll jumps ([\#8182](https://github.com/matrix-org/matrix-react-sdk/pull/8182)).
 * Fix "react error on share dialog" ([\#8170](https://github.com/matrix-org/matrix-react-sdk/pull/8170)). Contributed by @yaya-usman.
 * Fix disambiguated profile in threads in bubble layout ([\#8168](https://github.com/matrix-org/matrix-react-sdk/pull/8168)). Fixes #21570. Contributed by @SimonBrandner.
 * Responsive BetaCard on Labs ([\#8154](https://github.com/matrix-org/matrix-react-sdk/pull/8154)). Fixes #21554. Contributed by @luixxiul.
 * Display button as inline in room directory dialog ([\#8164](https://github.com/matrix-org/matrix-react-sdk/pull/8164)). Fixes #21567. Contributed by @luixxiul.
 * Null guard TimelinePanel unmount edge ([\#8171](https://github.com/matrix-org/matrix-react-sdk/pull/8171)).
 * Fix beta pill label breaking ([\#8162](https://github.com/matrix-org/matrix-react-sdk/pull/8162)). Fixes #21566. Contributed by @luixxiul.
 * Strip relations when forwarding ([\#7929](https://github.com/matrix-org/matrix-react-sdk/pull/7929)). Fixes #19769, #18067 #21015 and #10924.
 * Don't try (and fail) to show replies for redacted events ([\#8141](https://github.com/matrix-org/matrix-react-sdk/pull/8141)). Fixes #21435.
 * Fix 3pid member info for space member list ([\#8128](https://github.com/matrix-org/matrix-react-sdk/pull/8128)). Fixes #21534.
 * Set max-width to user context menu ([\#8089](https://github.com/matrix-org/matrix-react-sdk/pull/8089)). Fixes #21486. Contributed by @luixxiul.
 * Fix issue with falsey hrefs being sent in events ([\#8113](https://github.com/matrix-org/matrix-react-sdk/pull/8113)). Fixes #21417.
 * Make video sizing consistent with images ([\#8102](https://github.com/matrix-org/matrix-react-sdk/pull/8102)). Fixes #20072.

Changes in [1.10.8-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.10.8-rc.1) (2022-03-22)
=========================================================================================================

## ✨ Features
 * Live location sharing: live share warning in room ([\#8100](https://github.com/matrix-org/matrix-react-sdk/pull/8100)).
 * Add simple live share warning ([\#8066](https://github.com/matrix-org/matrix-react-sdk/pull/8066)).
 * extract reusable styled live beacon icon ([\#8103](https://github.com/matrix-org/matrix-react-sdk/pull/8103)).
 * Don't restore MemberInfo from RightPanel history when viewing a room ([\#8090](https://github.com/matrix-org/matrix-react-sdk/pull/8090)). Fixes #21487.
 * Allow sending files as replies as per MSC3676 ([\#8020](https://github.com/matrix-org/matrix-react-sdk/pull/8020)). Fixes #7156.
 * kill beacons on expiry ([\#8075](https://github.com/matrix-org/matrix-react-sdk/pull/8075)).
 * enable geolocation behaviour in location picker for live share type ([\#8068](https://github.com/matrix-org/matrix-react-sdk/pull/8068)).
 * Improve formatting features in the editor ([\#7104](https://github.com/matrix-org/matrix-react-sdk/pull/7104)). Fixes #19501. Contributed by @alexanderstephan.
 * Support MSC3026 busy presence ([\#8043](https://github.com/matrix-org/matrix-react-sdk/pull/8043)).
 * Show displayname in non-narrow thread summeries ([\#8036](https://github.com/matrix-org/matrix-react-sdk/pull/8036)). Fixes #19646.
 * Tweak search dialog based on new designs ([\#7980](https://github.com/matrix-org/matrix-react-sdk/pull/7980)). Fixes #21285 and #21289.
 * fallback to event text in location body when map unavailable ([\#7982](https://github.com/matrix-org/matrix-react-sdk/pull/7982)). Fixes #20655.
 * Send pin drop location share events ([\#7967](https://github.com/matrix-org/matrix-react-sdk/pull/7967)).

## 🐛 Bug Fixes
 * fix quicktime video thumbnailing ([\#8108](https://github.com/matrix-org/matrix-react-sdk/pull/8108)). Fixes #21505.
 * Fix scroll behaviour in space panel ([\#8111](https://github.com/matrix-org/matrix-react-sdk/pull/8111)). Fixes #21467.
 * Fix emoting with emoji or pills ([\#8105](https://github.com/matrix-org/matrix-react-sdk/pull/8105)). Fixes #21497.
 * Remove padding of InviteDialog & fix visual regression ([\#8076](https://github.com/matrix-org/matrix-react-sdk/pull/8076)). Fixes #20631. Contributed by @luixxiul.
 * Fixes mx_MLocationBody_markerBorder ([\#8069](https://github.com/matrix-org/matrix-react-sdk/pull/8069)). Fixes #21444. Contributed by @luixxiul.
 * Make margin and padding of mx_InviteDialog_other consistent ([\#8063](https://github.com/matrix-org/matrix-react-sdk/pull/8063)). Fixes #20631. Contributed by @luixxiul.
 * Fix freeze/crash when 1:1 calling ([\#8057](https://github.com/matrix-org/matrix-react-sdk/pull/8057)). Fixes #21181.
 * Don't assume that widget IDs are unique ([\#8052](https://github.com/matrix-org/matrix-react-sdk/pull/8052)). Fixes #21399.
 * Fix the header of Space landing page ([\#8048](https://github.com/matrix-org/matrix-react-sdk/pull/8048)). Fixes #21402. Contributed by @luixxiul.
 * Fix buttons alignment of Space list header ([\#8047](https://github.com/matrix-org/matrix-react-sdk/pull/8047)). Fixes #21401. Contributed by @luixxiul.
 * Fix null-guarding regression around reply_to_event dispatch ([\#8039](https://github.com/matrix-org/matrix-react-sdk/pull/8039)).
 * Fix clicking on copy link to thread wrongly opening thread ([\#8038](https://github.com/matrix-org/matrix-react-sdk/pull/8038)). Fixes #20653.
 * Fix regression around replying to search results ([\#8035](https://github.com/matrix-org/matrix-react-sdk/pull/8035)). Fixes #21389.
 * Share shared history keys in the background ([\#8031](https://github.com/matrix-org/matrix-react-sdk/pull/8031)). Fixes #21192.
 * Paginate responses to pinned polls ([\#8025](https://github.com/matrix-org/matrix-react-sdk/pull/8025)). Fixes #21382.
 * Fix incorrect usage of unstable variant of `is_falling_back` ([\#8016](https://github.com/matrix-org/matrix-react-sdk/pull/8016)).
 * Fix issues with ThreadSummary in msc-enabled mode ([\#8018](https://github.com/matrix-org/matrix-react-sdk/pull/8018)). Fixes matrix-org/element-web-rageshakes#11401 and matrix-org/element-web-rageshakes#11400.
 * Fix alignment of polls within threads ([\#8017](https://github.com/matrix-org/matrix-react-sdk/pull/8017)). Fixes #21235.
 * Fix issues with thread summaries being wrong or stale ([\#8015](https://github.com/matrix-org/matrix-react-sdk/pull/8015)). Fixes #21363 and #21204.
 * Fix button border color of LeaveSpaceDialog ([\#8010](https://github.com/matrix-org/matrix-react-sdk/pull/8010)). Fixes #21365. Contributed by @luixxiul.
 * Fix room list scroll jumps ([\#7991](https://github.com/matrix-org/matrix-react-sdk/pull/7991)). Fixes #19322.
 * Fix a variety of issues with HTML → Markdown conversion ([\#8004](https://github.com/matrix-org/matrix-react-sdk/pull/8004)). Fixes #10648, #20718, #10722, #10389, #17610 #9984 and #20140.
 * Wrap EventTile rather than its children in an error boundary ([\#7945](https://github.com/matrix-org/matrix-react-sdk/pull/7945)).
 * Normalized shortcut formatting for quote expansion control ([\#7995](https://github.com/matrix-org/matrix-react-sdk/pull/7995)). Fixes #19685. Contributed by @Sinharitik589.
 * Fix buttons and text layout on Security Key dialog ([\#7996](https://github.com/matrix-org/matrix-react-sdk/pull/7996)). Fixes #21330. Contributed by @luixxiul.
 * Fix formatting not being applied after links ([\#7990](https://github.com/matrix-org/matrix-react-sdk/pull/7990)). Fixes #20091.

Changes in [1.10.7](https://github.com/vector-im/element-web/releases/tag/v1.10.7) (2022-03-15)
===============================================================================================

## 🔒 SECURITY FIXES

 * Fix a bug where URL previews could be enabled in the left-panel when they
   should not have been.

## ✨ Features
 * Add a config.json option to skip the built-in Jitsi welcome screen ([\#21190](https://github.com/vector-im/element-web/pull/21190)).
 * Add unexposed account setting for hiding poll creation ([\#7972](https://github.com/matrix-org/matrix-react-sdk/pull/7972)).
 * Allow pinning polls ([\#7922](https://github.com/matrix-org/matrix-react-sdk/pull/7922)). Fixes #20152.
 * Make trailing `:` into a setting ([\#6711](https://github.com/matrix-org/matrix-react-sdk/pull/6711)). Fixes #16682. Contributed by @SimonBrandner.
 * Location sharing > back button ([\#7958](https://github.com/matrix-org/matrix-react-sdk/pull/7958)).
 * use LocationAssetType ([\#7965](https://github.com/matrix-org/matrix-react-sdk/pull/7965)).
 * Location share type UI ([\#7924](https://github.com/matrix-org/matrix-react-sdk/pull/7924)).
 * Add a few more UIComponent flags, and ensure they are used in existing code ([\#7937](https://github.com/matrix-org/matrix-react-sdk/pull/7937)).
 * Add support for overriding strings in the app ([\#7886](https://github.com/matrix-org/matrix-react-sdk/pull/7886)).
 * Add support for redirecting to external pages after logout ([\#7905](https://github.com/matrix-org/matrix-react-sdk/pull/7905)).
 * Expose redaction power level in room settings ([\#7599](https://github.com/matrix-org/matrix-react-sdk/pull/7599)). Fixes #20590. Contributed by @SimonBrandner.
 * Update and expand ways to access pinned messages ([\#7906](https://github.com/matrix-org/matrix-react-sdk/pull/7906)). Fixes #21209 and #21211.
 * Add slash command to switch to a room's virtual room ([\#7839](https://github.com/matrix-org/matrix-react-sdk/pull/7839)).

## 🐛 Bug Fixes
 * Remove Lojban translation ([\#21302](https://github.com/vector-im/element-web/pull/21302)).
 * Merge pull request from GHSA-qmf4-7w7j-vf23 ([\#8059](https://github.com/matrix-org/matrix-react-sdk/pull/8059)).
 * Add another null guard for member ([\#7984](https://github.com/matrix-org/matrix-react-sdk/pull/7984)). Fixes #21319.
 * Fix room account settings ([\#7999](https://github.com/matrix-org/matrix-react-sdk/pull/7999)).
 * Fix missing summary text for pinned message changes ([\#7989](https://github.com/matrix-org/matrix-react-sdk/pull/7989)). Fixes #19823.
 * Pass room to getRoomTombstone to avoid racing with setState ([\#7986](https://github.com/matrix-org/matrix-react-sdk/pull/7986)).
 * Hide composer and call buttons when the room is tombstoned ([\#7975](https://github.com/matrix-org/matrix-react-sdk/pull/7975)). Fixes #21286.
 * Fix bad ternary statement in autocomplete user pill insertions ([\#7977](https://github.com/matrix-org/matrix-react-sdk/pull/7977)). Fixes #21307.
 * Fix sending locations into threads and fix i18n ([\#7943](https://github.com/matrix-org/matrix-react-sdk/pull/7943)). Fixes #21267.
 * Fix location map attribution rendering over message action bar ([\#7974](https://github.com/matrix-org/matrix-react-sdk/pull/7974)). Fixes #21297.
 * Fix wrongly asserting that PushRule::conditions is non-null ([\#7973](https://github.com/matrix-org/matrix-react-sdk/pull/7973)). Fixes #21305.
 * Fix account & room settings race condition ([\#7953](https://github.com/matrix-org/matrix-react-sdk/pull/7953)). Fixes #21163.
 * Fix bug with some space selections not being applied ([\#7971](https://github.com/matrix-org/matrix-react-sdk/pull/7971)). Fixes #21290.
 * Revert "replace all require(.svg) with esm import" ([\#7969](https://github.com/matrix-org/matrix-react-sdk/pull/7969)). Fixes #21293.
 * Hide unpinnable pinned messages in more cases ([\#7921](https://github.com/matrix-org/matrix-react-sdk/pull/7921)).
 * Fix room list being laggy while scrolling 🐌 ([\#7939](https://github.com/matrix-org/matrix-react-sdk/pull/7939)). Fixes #21262.
 * Make pinned messages more reliably reflect edits ([\#7920](https://github.com/matrix-org/matrix-react-sdk/pull/7920)). Fixes #17098.
 * Improve accessibility of the BetaPill ([\#7949](https://github.com/matrix-org/matrix-react-sdk/pull/7949)). Fixes #21255.
 * Autofocus correct composer after sending reaction ([\#7950](https://github.com/matrix-org/matrix-react-sdk/pull/7950)). Fixes #21273.
 * Consider polls as message events for rendering redactions ([\#7944](https://github.com/matrix-org/matrix-react-sdk/pull/7944)). Fixes #21125.
 * Prevent event tiles being shrunk/collapsed by flexbox ([\#7942](https://github.com/matrix-org/matrix-react-sdk/pull/7942)). Fixes #21269.
 * Fix ExportDialog title on export cancellation ([\#7936](https://github.com/matrix-org/matrix-react-sdk/pull/7936)). Fixes #21260. Contributed by @luixxiul.
 * Mandate use of js-sdk/src/matrix import over js-sdk/src ([\#7933](https://github.com/matrix-org/matrix-react-sdk/pull/7933)). Fixes #21253.
 * Fix backspace not working in the invite dialog ([\#7931](https://github.com/matrix-org/matrix-react-sdk/pull/7931)). Fixes #21249. Contributed by @SimonBrandner.
 * Fix right panel soft crashes due to missing room prop ([\#7923](https://github.com/matrix-org/matrix-react-sdk/pull/7923)). Fixes #21243.
 * fix color of location share caret ([\#7917](https://github.com/matrix-org/matrix-react-sdk/pull/7917)).
 * Wrap all EventTiles with a TileErrorBoundary and guard parsePermalink ([\#7916](https://github.com/matrix-org/matrix-react-sdk/pull/7916)). Fixes #21216.
 * Fix changing space sometimes bouncing to the wrong space ([\#7910](https://github.com/matrix-org/matrix-react-sdk/pull/7910)). Fixes #20425.
 * Ensure EventListSummary key does not change during backpagination ([\#7915](https://github.com/matrix-org/matrix-react-sdk/pull/7915)). Fixes #9192.
 * Fix positioning of the thread context menu ([\#7918](https://github.com/matrix-org/matrix-react-sdk/pull/7918)). Fixes #21236.
 * Inject sender into pinned messages ([\#7904](https://github.com/matrix-org/matrix-react-sdk/pull/7904)). Fixes #20314.
 * Tweak info message padding in right panel timeline ([\#7901](https://github.com/matrix-org/matrix-react-sdk/pull/7901)). Fixes #21212.
 * Fix another freeze on room switch ([\#7900](https://github.com/matrix-org/matrix-react-sdk/pull/7900)). Fixes #21127.
 * Fix out of memory error when failing to acquire location ([\#7902](https://github.com/matrix-org/matrix-react-sdk/pull/7902)). Fixes #21213.
 * Fix edge case in context menu chevron positioning ([\#7899](https://github.com/matrix-org/matrix-react-sdk/pull/7899)).
 * Fix composer format buttons on WebKit ([\#7898](https://github.com/matrix-org/matrix-react-sdk/pull/7898)). Fixes #20868.
 * manage voicerecording state when deleting or sending a voice message ([\#7896](https://github.com/matrix-org/matrix-react-sdk/pull/7896)). Fixes #21151.
 * Fix bug with useRoomHierarchy tight-looping loadMore on error ([\#7893](https://github.com/matrix-org/matrix-react-sdk/pull/7893)).
 * Fix upload button & shortcut not working for narrow composer mode ([\#7894](https://github.com/matrix-org/matrix-react-sdk/pull/7894)). Fixes #21175 and #21142.
 * Fix emoji insertion in thread composer going to the main composer ([\#7895](https://github.com/matrix-org/matrix-react-sdk/pull/7895)). Fixes #21202.
 * Try harder to keep context menus inside the window ([\#7863](https://github.com/matrix-org/matrix-react-sdk/pull/7863)). Fixes #17527 and #18377.
 * Fix edge case around event list summary layout ([\#7891](https://github.com/matrix-org/matrix-react-sdk/pull/7891)). Fixes #21180.
 * Fix event list summary 1 hidden message pluralisation ([\#7890](https://github.com/matrix-org/matrix-react-sdk/pull/7890)). Fixes #21196.
 * Fix vanishing recently viewed menu ([\#7887](https://github.com/matrix-org/matrix-react-sdk/pull/7887)). Fixes #20827.
 * Fix freeze on room switch ([\#7884](https://github.com/matrix-org/matrix-react-sdk/pull/7884)). Fixes #21127.
 * Check 'useSystemTheme' in quick settings theme switcher ([\#7809](https://github.com/matrix-org/matrix-react-sdk/pull/7809)). Fixes #21061.
 * Fix 'my threads' filtering to include participated threads ([\#7882](https://github.com/matrix-org/matrix-react-sdk/pull/7882)). Fixes #20877.
 * Remove log line to try to fix freeze on answering VoIP call ([\#7883](https://github.com/matrix-org/matrix-react-sdk/pull/7883)).
 * Support social login & password on soft logout page ([\#7879](https://github.com/matrix-org/matrix-react-sdk/pull/7879)). Fixes #21099.
 * Fix missing padding on server picker ([\#7864](https://github.com/matrix-org/matrix-react-sdk/pull/7864)).
 * Throttle RoomState.members handlers ([\#7876](https://github.com/matrix-org/matrix-react-sdk/pull/7876)). Fixes #21127.
 * Only show joined/invited in search dialog ([\#7875](https://github.com/matrix-org/matrix-react-sdk/pull/7875)). Fixes #21161.
 * Don't pillify code blocks ([\#7861](https://github.com/matrix-org/matrix-react-sdk/pull/7861)). Fixes #20851 and #18687.
 * Fix keyboard shortcut icons on macOS ([\#7869](https://github.com/matrix-org/matrix-react-sdk/pull/7869)).

Changes in [1.10.7-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.10.7-rc.1) (2022-03-08)
=========================================================================================================

## ✨ Features
 * Add a config.json option to skip the built-in Jitsi welcome screen ([\#21190](https://github.com/vector-im/element-web/pull/21190)).
 * Add unexposed account setting for hiding poll creation ([\#7972](https://github.com/matrix-org/matrix-react-sdk/pull/7972)).
 * Allow pinning polls ([\#7922](https://github.com/matrix-org/matrix-react-sdk/pull/7922)). Fixes #20152.
 * Make trailing `:` into a setting ([\#6711](https://github.com/matrix-org/matrix-react-sdk/pull/6711)). Fixes #16682. Contributed by @SimonBrandner.
 * Location sharing > back button ([\#7958](https://github.com/matrix-org/matrix-react-sdk/pull/7958)).
 * use LocationAssetType ([\#7965](https://github.com/matrix-org/matrix-react-sdk/pull/7965)).
 * Location share type UI ([\#7924](https://github.com/matrix-org/matrix-react-sdk/pull/7924)).
 * Add a few more UIComponent flags, and ensure they are used in existing code ([\#7937](https://github.com/matrix-org/matrix-react-sdk/pull/7937)).
 * Add support for overriding strings in the app ([\#7886](https://github.com/matrix-org/matrix-react-sdk/pull/7886)).
 * Add support for redirecting to external pages after logout ([\#7905](https://github.com/matrix-org/matrix-react-sdk/pull/7905)).
 * Expose redaction power level in room settings ([\#7599](https://github.com/matrix-org/matrix-react-sdk/pull/7599)). Fixes #20590. Contributed by @SimonBrandner.
 * Update and expand ways to access pinned messages ([\#7906](https://github.com/matrix-org/matrix-react-sdk/pull/7906)). Fixes #21209 and #21211.
 * Add slash command to switch to a room's virtual room ([\#7839](https://github.com/matrix-org/matrix-react-sdk/pull/7839)).

## 🐛 Bug Fixes
 * Remove Lojban translation ([\#21302](https://github.com/vector-im/element-web/pull/21302)).
 * Add another null guard for member ([\#7984](https://github.com/matrix-org/matrix-react-sdk/pull/7984)). Fixes #21319.
 * Fix room account settings ([\#7999](https://github.com/matrix-org/matrix-react-sdk/pull/7999)).
 * Fix missing summary text for pinned message changes ([\#7989](https://github.com/matrix-org/matrix-react-sdk/pull/7989)). Fixes #19823.
 * Pass room to getRoomTombstone to avoid racing with setState ([\#7986](https://github.com/matrix-org/matrix-react-sdk/pull/7986)).
 * Hide composer and call buttons when the room is tombstoned ([\#7975](https://github.com/matrix-org/matrix-react-sdk/pull/7975)). Fixes #21286.
 * Fix bad ternary statement in autocomplete user pill insertions ([\#7977](https://github.com/matrix-org/matrix-react-sdk/pull/7977)). Fixes #21307.
 * Fix sending locations into threads and fix i18n ([\#7943](https://github.com/matrix-org/matrix-react-sdk/pull/7943)). Fixes #21267.
 * Fix location map attribution rendering over message action bar ([\#7974](https://github.com/matrix-org/matrix-react-sdk/pull/7974)). Fixes #21297.
 * Fix wrongly asserting that PushRule::conditions is non-null ([\#7973](https://github.com/matrix-org/matrix-react-sdk/pull/7973)). Fixes #21305.
 * Fix account & room settings race condition ([\#7953](https://github.com/matrix-org/matrix-react-sdk/pull/7953)). Fixes #21163.
 * Fix bug with some space selections not being applied ([\#7971](https://github.com/matrix-org/matrix-react-sdk/pull/7971)). Fixes #21290.
 * Revert "replace all require(.svg) with esm import" ([\#7969](https://github.com/matrix-org/matrix-react-sdk/pull/7969)). Fixes #21293.
 * Hide unpinnable pinned messages in more cases ([\#7921](https://github.com/matrix-org/matrix-react-sdk/pull/7921)).
 * Fix room list being laggy while scrolling 🐌 ([\#7939](https://github.com/matrix-org/matrix-react-sdk/pull/7939)). Fixes #21262.
 * Make pinned messages more reliably reflect edits ([\#7920](https://github.com/matrix-org/matrix-react-sdk/pull/7920)). Fixes #17098.
 * Improve accessibility of the BetaPill ([\#7949](https://github.com/matrix-org/matrix-react-sdk/pull/7949)). Fixes #21255.
 * Autofocus correct composer after sending reaction ([\#7950](https://github.com/matrix-org/matrix-react-sdk/pull/7950)). Fixes #21273.
 * Consider polls as message events for rendering redactions ([\#7944](https://github.com/matrix-org/matrix-react-sdk/pull/7944)). Fixes #21125.
 * Prevent event tiles being shrunk/collapsed by flexbox ([\#7942](https://github.com/matrix-org/matrix-react-sdk/pull/7942)). Fixes #21269.
 * Fix ExportDialog title on export cancellation ([\#7936](https://github.com/matrix-org/matrix-react-sdk/pull/7936)). Fixes #21260. Contributed by @luixxiul.
 * Mandate use of js-sdk/src/matrix import over js-sdk/src ([\#7933](https://github.com/matrix-org/matrix-react-sdk/pull/7933)). Fixes #21253.
 * Fix backspace not working in the invite dialog ([\#7931](https://github.com/matrix-org/matrix-react-sdk/pull/7931)). Fixes #21249. Contributed by @SimonBrandner.
 * Fix right panel soft crashes due to missing room prop ([\#7923](https://github.com/matrix-org/matrix-react-sdk/pull/7923)). Fixes #21243.
 * fix color of location share caret ([\#7917](https://github.com/matrix-org/matrix-react-sdk/pull/7917)).
 * Wrap all EventTiles with a TileErrorBoundary and guard parsePermalink ([\#7916](https://github.com/matrix-org/matrix-react-sdk/pull/7916)). Fixes #21216.
 * Fix changing space sometimes bouncing to the wrong space ([\#7910](https://github.com/matrix-org/matrix-react-sdk/pull/7910)). Fixes #20425.
 * Ensure EventListSummary key does not change during backpagination ([\#7915](https://github.com/matrix-org/matrix-react-sdk/pull/7915)). Fixes #9192.
 * Fix positioning of the thread context menu ([\#7918](https://github.com/matrix-org/matrix-react-sdk/pull/7918)). Fixes #21236.
 * Inject sender into pinned messages ([\#7904](https://github.com/matrix-org/matrix-react-sdk/pull/7904)). Fixes #20314.
 * Tweak info message padding in right panel timeline ([\#7901](https://github.com/matrix-org/matrix-react-sdk/pull/7901)). Fixes #21212.
 * Fix another freeze on room switch ([\#7900](https://github.com/matrix-org/matrix-react-sdk/pull/7900)). Fixes #21127.
 * Fix out of memory error when failing to acquire location ([\#7902](https://github.com/matrix-org/matrix-react-sdk/pull/7902)). Fixes #21213.
 * Fix edge case in context menu chevron positioning ([\#7899](https://github.com/matrix-org/matrix-react-sdk/pull/7899)).
 * Fix composer format buttons on WebKit ([\#7898](https://github.com/matrix-org/matrix-react-sdk/pull/7898)). Fixes #20868.
 * manage voicerecording state when deleting or sending a voice message ([\#7896](https://github.com/matrix-org/matrix-react-sdk/pull/7896)). Fixes #21151.
 * Fix bug with useRoomHierarchy tight-looping loadMore on error ([\#7893](https://github.com/matrix-org/matrix-react-sdk/pull/7893)).
 * Fix upload button & shortcut not working for narrow composer mode ([\#7894](https://github.com/matrix-org/matrix-react-sdk/pull/7894)). Fixes #21175 and #21142.
 * Fix emoji insertion in thread composer going to the main composer ([\#7895](https://github.com/matrix-org/matrix-react-sdk/pull/7895)). Fixes #21202.
 * Try harder to keep context menus inside the window ([\#7863](https://github.com/matrix-org/matrix-react-sdk/pull/7863)). Fixes #17527 and #18377.
 * Fix edge case around event list summary layout ([\#7891](https://github.com/matrix-org/matrix-react-sdk/pull/7891)). Fixes #21180.
 * Fix event list summary 1 hidden message pluralisation ([\#7890](https://github.com/matrix-org/matrix-react-sdk/pull/7890)). Fixes #21196.
 * Fix vanishing recently viewed menu ([\#7887](https://github.com/matrix-org/matrix-react-sdk/pull/7887)). Fixes #20827.
 * Fix freeze on room switch ([\#7884](https://github.com/matrix-org/matrix-react-sdk/pull/7884)). Fixes #21127.
 * Check 'useSystemTheme' in quick settings theme switcher ([\#7809](https://github.com/matrix-org/matrix-react-sdk/pull/7809)). Fixes #21061.
 * Fix 'my threads' filtering to include participated threads ([\#7882](https://github.com/matrix-org/matrix-react-sdk/pull/7882)). Fixes #20877.
 * Remove log line to try to fix freeze on answering VoIP call ([\#7883](https://github.com/matrix-org/matrix-react-sdk/pull/7883)).
 * Support social login & password on soft logout page ([\#7879](https://github.com/matrix-org/matrix-react-sdk/pull/7879)). Fixes #21099.
 * Fix missing padding on server picker ([\#7864](https://github.com/matrix-org/matrix-react-sdk/pull/7864)).
 * Throttle RoomState.members handlers ([\#7876](https://github.com/matrix-org/matrix-react-sdk/pull/7876)). Fixes #21127.
 * Only show joined/invited in search dialog ([\#7875](https://github.com/matrix-org/matrix-react-sdk/pull/7875)). Fixes #21161.
 * Don't pillify code blocks ([\#7861](https://github.com/matrix-org/matrix-react-sdk/pull/7861)). Fixes #20851 and #18687.
 * Fix keyboard shortcut icons on macOS ([\#7869](https://github.com/matrix-org/matrix-react-sdk/pull/7869)).

Changes in [1.10.6](https://github.com/vector-im/element-web/releases/tag/v1.10.6) (2022-03-01)
===============================================================================================

## 🐛 Bug Fixes
 * Fix some crashes in the right panel

Changes in [1.10.5](https://github.com/vector-im/element-web/releases/tag/v1.10.5) (2022-02-28)
===============================================================================================

## 🌐 Translations
 * This release contains a significant update to the Japanese translations, contributed by Suguru Hirahara (@luixxiul). ありがとうございます!

## ✨ Features
 * Support "closed" polls whose votes are not visible until they are ended ([\#7842](https://github.com/matrix-org/matrix-react-sdk/pull/7842)).
 * Focus trap in poll creation dialog ([\#7847](https://github.com/matrix-org/matrix-react-sdk/pull/7847)). Fixes #20281.
 * Add labs flag: Show only current profile on historical messages ([\#7815](https://github.com/matrix-org/matrix-react-sdk/pull/7815)).
 * Keep unsent voice messages in memory until they are deleted or sent ([\#7840](https://github.com/matrix-org/matrix-react-sdk/pull/7840)). Fixes #17979.
 * A link to `#/dm` in a custom home.html will open the "Direct Messages" dialog. ([\#7783](https://github.com/matrix-org/matrix-react-sdk/pull/7783)). Contributed by @johannes-krude.
 * set icon-button-color to be configurable via quaternary-content variable ([\#7725](https://github.com/matrix-org/matrix-react-sdk/pull/7725)). Fixes #20925. Contributed by @acxz.
 * Allow editing polls ([\#7806](https://github.com/matrix-org/matrix-react-sdk/pull/7806)).
 * Abstract spotlight to allow non-room results too ([\#7804](https://github.com/matrix-org/matrix-react-sdk/pull/7804)). Fixes #20968, matrix-org/element-web-rageshakes#10766, matrix-org/element-web-rageshakes#10777, matrix-org/element-web-rageshakes#10767 matrix-org/element-web-rageshakes#10760 and matrix-org/element-web-rageshakes#10752.
 * Display '(edited)' next to edited polls ([\#7789](https://github.com/matrix-org/matrix-react-sdk/pull/7789)).
 * Use the resize observer polyfill consistently ([\#7796](https://github.com/matrix-org/matrix-react-sdk/pull/7796)). Fixes matrix-org/element-web-rageshakes#10700.
 * Consolidate, simplify and improve copied tooltips ([\#7799](https://github.com/matrix-org/matrix-react-sdk/pull/7799)). Fixes #21069.
 * Suggest `@room` when `@channel`, `@everyone`, or `@here` is typed in composer ([\#7737](https://github.com/matrix-org/matrix-react-sdk/pull/7737)). Fixes #20972. Contributed by @aaronraimist.
 * Add customisation point to disable space creation ([\#7766](https://github.com/matrix-org/matrix-react-sdk/pull/7766)).
 * Consolidate RedactionGrouper and HiddenEventGrouper into MELS ([\#7739](https://github.com/matrix-org/matrix-react-sdk/pull/7739)). Fixes #20958.
 * Unify widget header actions with those in right panel ([\#7734](https://github.com/matrix-org/matrix-react-sdk/pull/7734)).
 * Improve new search dialog context text for exactly 2 parent spaces ([\#7761](https://github.com/matrix-org/matrix-react-sdk/pull/7761)).

## 🐛 Bug Fixes
 * Fix command key missing in keyboard shortcuts tab ([\#21102](https://github.com/vector-im/element-web/pull/21102)). Contributed by @SimonBrandner.
 * [Release] Tweak info message padding in right panel timeline ([\#7909](https://github.com/matrix-org/matrix-react-sdk/pull/7909)).
 * [Release] Fix edge case around event list summary layout ([\#7892](https://github.com/matrix-org/matrix-react-sdk/pull/7892)).
 * Wire up CallEventGroupers for Search Results ([\#7866](https://github.com/matrix-org/matrix-react-sdk/pull/7866)). Fixes #21150.
 * Fix edge case around event list summary layout ([\#7867](https://github.com/matrix-org/matrix-react-sdk/pull/7867)). Fixes #21153.
 * Fix misalignment with Event List Summaries ([\#7865](https://github.com/matrix-org/matrix-react-sdk/pull/7865)). Fixes #21149.
 * Fix non-customizable keybindings not working as expected ([\#7855](https://github.com/matrix-org/matrix-react-sdk/pull/7855)). Fixes #21136 and matrix-org/element-web-rageshakes#10830.
 * Fix accessibility around the room list treeview and new search beta ([\#7856](https://github.com/matrix-org/matrix-react-sdk/pull/7856)). Fixes matrix-org/element-web-rageshakes#10873.
 * Inhibit tooltip on timeline pill avatars, the whole pill has its own ([\#7854](https://github.com/matrix-org/matrix-react-sdk/pull/7854)). Fixes #21135.
 * Fix virtual / native room mapping on call transfers ([\#7848](https://github.com/matrix-org/matrix-react-sdk/pull/7848)).
 * Fix ScrollPanel data-scrollbar not responding to window resizing ([\#7841](https://github.com/matrix-org/matrix-react-sdk/pull/7841)). Fixes #20594.
 * add cursor: pointer to actionable poll options ([\#7826](https://github.com/matrix-org/matrix-react-sdk/pull/7826)). Fixes #21033.
 * Tear down AppTile using lifecycle tracking ([\#7833](https://github.com/matrix-org/matrix-react-sdk/pull/7833)). Fixes #21025.
 * Fix layout inconsistencies with the room search minimized button ([\#7824](https://github.com/matrix-org/matrix-react-sdk/pull/7824)). Fixes #21106.
 * Fix space panel notification badge behaviour and metrics ([\#7823](https://github.com/matrix-org/matrix-react-sdk/pull/7823)). Fixes #21092.
 * Fix left panel widgets causing app crashes (again) ([\#7814](https://github.com/matrix-org/matrix-react-sdk/pull/7814)).
 * Fix right panel data flow ([\#7811](https://github.com/matrix-org/matrix-react-sdk/pull/7811)). Fixes #20929.
 * set mask-size for icons ([\#7812](https://github.com/matrix-org/matrix-react-sdk/pull/7812)). Fixes #21047.
 * Fix room create tile not showing up with hidden events shown ([\#7810](https://github.com/matrix-org/matrix-react-sdk/pull/7810)). Fixes #20893.
 * Fix delayed badge update for mentions in encrypted rooms ([\#7813](https://github.com/matrix-org/matrix-react-sdk/pull/7813)). Fixes #20859.
 * Fix add existing space not showing any spaces ([\#7801](https://github.com/matrix-org/matrix-react-sdk/pull/7801)). Fixes #21087. Contributed by @c-cal.
 * Fix edge cases around event list summaries with hidden events and redactions ([\#7797](https://github.com/matrix-org/matrix-react-sdk/pull/7797)). Fixes #21030 #21050 and #21055.
 * Improve styling of edge case devtools state keys ([\#7794](https://github.com/matrix-org/matrix-react-sdk/pull/7794)). Fixes #21056.
 * Don't scroll to bottom when executing non-message slash commands ([\#7793](https://github.com/matrix-org/matrix-react-sdk/pull/7793)). Fixes #21065.
 * Fix cutout misalignment on some decorated room avatars ([\#7784](https://github.com/matrix-org/matrix-react-sdk/pull/7784)). Fixes #21038.
 * Fix desktop notifications for invites showing user IDs instead of displaynames ([\#7780](https://github.com/matrix-org/matrix-react-sdk/pull/7780)). Fixes #21022. Contributed by @c-cal.
 * Fix bad pluralisation on event list summary hidden message handling ([\#7778](https://github.com/matrix-org/matrix-react-sdk/pull/7778)).
 * Properly recurse subspaces for leave space dialog options ([\#7775](https://github.com/matrix-org/matrix-react-sdk/pull/7775)). Fixes #20949 and #21012.
 * Fix translation for keyboard shortcut displaynames ([\#7758](https://github.com/matrix-org/matrix-react-sdk/pull/7758)). Fixes #20992. Contributed by @c-cal.
 * Fix space member list opening with back button ([\#7773](https://github.com/matrix-org/matrix-react-sdk/pull/7773)). Fixes #21009. Contributed by @c-cal.
 * Fix sort order for facepiles which was exactly reverse ([\#7771](https://github.com/matrix-org/matrix-react-sdk/pull/7771)).
 * Fix state events being wrongly hidden when redacted ([\#7768](https://github.com/matrix-org/matrix-react-sdk/pull/7768)). Fixes #20959.
 * Event List Summary guard against missing event senders ([\#7767](https://github.com/matrix-org/matrix-react-sdk/pull/7767)). Fixes #21004.
 * Fix all settings button opening sidebar settings tab ([\#7765](https://github.com/matrix-org/matrix-react-sdk/pull/7765)). Fixes #20998. Contributed by @c-cal.
 * Fix theme selector dropdown overflow ([\#7764](https://github.com/matrix-org/matrix-react-sdk/pull/7764)). Fixes #20996. Contributed by @c-cal.
 * Fix widget and mjolnir state events showing with mxid not name ([\#7760](https://github.com/matrix-org/matrix-react-sdk/pull/7760)). Fixes #20986.
 * Fix space member list not opening ([\#7747](https://github.com/matrix-org/matrix-react-sdk/pull/7747)). Fixes #20982. Contributed by @c-cal.
 * Handle highlight notifications in timeline card button ([\#7762](https://github.com/matrix-org/matrix-react-sdk/pull/7762)). Fixes #20987. Contributed by @SimonBrandner.
 * Fix add existing space not showing any spaces ([\#7751](https://github.com/matrix-org/matrix-react-sdk/pull/7751)).
 * Inhibit Room List keyboard pass-thru when the search beta is enabled ([\#7752](https://github.com/matrix-org/matrix-react-sdk/pull/7752)). Fixes #20984.
 * Add unread notification dot to timeline card button ([\#7749](https://github.com/matrix-org/matrix-react-sdk/pull/7749)). Fixes #20946. Contributed by @SimonBrandner.

Changes in [1.10.5-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.10.5-rc.1) (2022-02-22)
=========================================================================================================

## 🌐 Translations
 * This release contains a significant update to the Japanese translations, contributed by Suguru Hirahara (@luixxiul). ありがとうございます!

## ✨ Features
 * Support "closed" polls whose votes are not visible until they are ended ([\#7842](https://github.com/matrix-org/matrix-react-sdk/pull/7842)).
 * Focus trap in poll creation dialog ([\#7847](https://github.com/matrix-org/matrix-react-sdk/pull/7847)). Fixes #20281.
 * Add labs flag: Show only current profile on historical messages ([\#7815](https://github.com/matrix-org/matrix-react-sdk/pull/7815)).
 * Keep unsent voice messages in memory until they are deleted or sent ([\#7840](https://github.com/matrix-org/matrix-react-sdk/pull/7840)). Fixes #17979.
 * A link to `#/dm` in a custom home.html will open the "Direct Messages" dialog. ([\#7783](https://github.com/matrix-org/matrix-react-sdk/pull/7783)). Contributed by @johannes-krude.
 * set icon-button-color to be configurable via quaternary-content variable ([\#7725](https://github.com/matrix-org/matrix-react-sdk/pull/7725)). Fixes #20925. Contributed by @acxz.
 * Allow editing polls ([\#7806](https://github.com/matrix-org/matrix-react-sdk/pull/7806)).
 * Abstract spotlight to allow non-room results too ([\#7804](https://github.com/matrix-org/matrix-react-sdk/pull/7804)). Fixes #20968, matrix-org/element-web-rageshakes#10766, matrix-org/element-web-rageshakes#10777, matrix-org/element-web-rageshakes#10767 matrix-org/element-web-rageshakes#10760 and matrix-org/element-web-rageshakes#10752.
 * Display '(edited)' next to edited polls ([\#7789](https://github.com/matrix-org/matrix-react-sdk/pull/7789)).
 * Use the resize observer polyfill consistently ([\#7796](https://github.com/matrix-org/matrix-react-sdk/pull/7796)). Fixes matrix-org/element-web-rageshakes#10700.
 * Consolidate, simplify and improve copied tooltips ([\#7799](https://github.com/matrix-org/matrix-react-sdk/pull/7799)). Fixes #21069.
 * Suggest `@room` when `@channel`, `@everyone`, or `@here` is typed in composer ([\#7737](https://github.com/matrix-org/matrix-react-sdk/pull/7737)). Fixes #20972. Contributed by @aaronraimist.
 * Add customisation point to disable space creation ([\#7766](https://github.com/matrix-org/matrix-react-sdk/pull/7766)).
 * Consolidate RedactionGrouper and HiddenEventGrouper into MELS ([\#7739](https://github.com/matrix-org/matrix-react-sdk/pull/7739)). Fixes #20958.
 * Unify widget header actions with those in right panel ([\#7734](https://github.com/matrix-org/matrix-react-sdk/pull/7734)).
 * Improve new search dialog context text for exactly 2 parent spaces ([\#7761](https://github.com/matrix-org/matrix-react-sdk/pull/7761)).

## 🐛 Bug Fixes
 * Fix command key missing in keyboard shortcuts tab ([\#21102](https://github.com/vector-im/element-web/pull/21102)). Contributed by @SimonBrandner.
 * Wire up CallEventGroupers for Search Results ([\#7866](https://github.com/matrix-org/matrix-react-sdk/pull/7866)). Fixes #21150.
 * Fix edge case around event list summary layout ([\#7867](https://github.com/matrix-org/matrix-react-sdk/pull/7867)). Fixes #21153.
 * Fix misalignment with Event List Summaries ([\#7865](https://github.com/matrix-org/matrix-react-sdk/pull/7865)). Fixes #21149.
 * Fix non-customizable keybindings not working as expected ([\#7855](https://github.com/matrix-org/matrix-react-sdk/pull/7855)). Fixes #21136 and matrix-org/element-web-rageshakes#10830.
 * Fix accessibility around the room list treeview and new search beta ([\#7856](https://github.com/matrix-org/matrix-react-sdk/pull/7856)). Fixes matrix-org/element-web-rageshakes#10873.
 * Inhibit tooltip on timeline pill avatars, the whole pill has its own ([\#7854](https://github.com/matrix-org/matrix-react-sdk/pull/7854)). Fixes #21135.
 * Fix virtual / native room mapping on call transfers ([\#7848](https://github.com/matrix-org/matrix-react-sdk/pull/7848)).
 * Fix ScrollPanel data-scrollbar not responding to window resizing ([\#7841](https://github.com/matrix-org/matrix-react-sdk/pull/7841)). Fixes #20594.
 * add cursor: pointer to actionable poll options ([\#7826](https://github.com/matrix-org/matrix-react-sdk/pull/7826)). Fixes #21033.
 * Tear down AppTile using lifecycle tracking ([\#7833](https://github.com/matrix-org/matrix-react-sdk/pull/7833)). Fixes #21025.
 * Fix layout inconsistencies with the room search minimized button ([\#7824](https://github.com/matrix-org/matrix-react-sdk/pull/7824)). Fixes #21106.
 * Fix space panel notification badge behaviour and metrics ([\#7823](https://github.com/matrix-org/matrix-react-sdk/pull/7823)). Fixes #21092.
 * Fix left panel widgets causing app crashes (again) ([\#7814](https://github.com/matrix-org/matrix-react-sdk/pull/7814)).
 * Fix right panel data flow ([\#7811](https://github.com/matrix-org/matrix-react-sdk/pull/7811)). Fixes #20929.
 * set mask-size for icons ([\#7812](https://github.com/matrix-org/matrix-react-sdk/pull/7812)). Fixes #21047.
 * Fix room create tile not showing up with hidden events shown ([\#7810](https://github.com/matrix-org/matrix-react-sdk/pull/7810)). Fixes #20893.
 * Fix delayed badge update for mentions in encrypted rooms ([\#7813](https://github.com/matrix-org/matrix-react-sdk/pull/7813)). Fixes #20859.
 * Fix add existing space not showing any spaces ([\#7801](https://github.com/matrix-org/matrix-react-sdk/pull/7801)). Fixes #21087. Contributed by @c-cal.
 * Fix edge cases around event list summaries with hidden events and redactions ([\#7797](https://github.com/matrix-org/matrix-react-sdk/pull/7797)). Fixes #21030 #21050 and #21055.
 * Improve styling of edge case devtools state keys ([\#7794](https://github.com/matrix-org/matrix-react-sdk/pull/7794)). Fixes #21056.
 * Don't scroll to bottom when executing non-message slash commands ([\#7793](https://github.com/matrix-org/matrix-react-sdk/pull/7793)). Fixes #21065.
 * Fix cutout misalignment on some decorated room avatars ([\#7784](https://github.com/matrix-org/matrix-react-sdk/pull/7784)). Fixes #21038.
 * Fix desktop notifications for invites showing user IDs instead of displaynames ([\#7780](https://github.com/matrix-org/matrix-react-sdk/pull/7780)). Fixes #21022. Contributed by @c-cal.
 * Fix bad pluralisation on event list summary hidden message handling ([\#7778](https://github.com/matrix-org/matrix-react-sdk/pull/7778)).
 * Properly recurse subspaces for leave space dialog options ([\#7775](https://github.com/matrix-org/matrix-react-sdk/pull/7775)). Fixes #20949 and #21012.
 * Fix translation for keyboard shortcut displaynames ([\#7758](https://github.com/matrix-org/matrix-react-sdk/pull/7758)). Fixes #20992. Contributed by @c-cal.
 * Fix space member list opening with back button ([\#7773](https://github.com/matrix-org/matrix-react-sdk/pull/7773)). Fixes #21009. Contributed by @c-cal.
 * Fix sort order for facepiles which was exactly reverse ([\#7771](https://github.com/matrix-org/matrix-react-sdk/pull/7771)).
 * Fix state events being wrongly hidden when redacted ([\#7768](https://github.com/matrix-org/matrix-react-sdk/pull/7768)). Fixes #20959.
 * Event List Summary guard against missing event senders ([\#7767](https://github.com/matrix-org/matrix-react-sdk/pull/7767)). Fixes #21004.
 * Fix all settings button opening sidebar settings tab ([\#7765](https://github.com/matrix-org/matrix-react-sdk/pull/7765)). Fixes #20998. Contributed by @c-cal.
 * Fix theme selector dropdown overflow ([\#7764](https://github.com/matrix-org/matrix-react-sdk/pull/7764)). Fixes #20996. Contributed by @c-cal.
 * Fix widget and mjolnir state events showing with mxid not name ([\#7760](https://github.com/matrix-org/matrix-react-sdk/pull/7760)). Fixes #20986.
 * Fix space member list not opening ([\#7747](https://github.com/matrix-org/matrix-react-sdk/pull/7747)). Fixes #20982. Contributed by @c-cal.
 * Handle highlight notifications in timeline card button ([\#7762](https://github.com/matrix-org/matrix-react-sdk/pull/7762)). Fixes #20987. Contributed by @SimonBrandner.
 * Fix add existing space not showing any spaces ([\#7751](https://github.com/matrix-org/matrix-react-sdk/pull/7751)).
 * Inhibit Room List keyboard pass-thru when the search beta is enabled ([\#7752](https://github.com/matrix-org/matrix-react-sdk/pull/7752)). Fixes #20984.
 * Add unread notification dot to timeline card button ([\#7749](https://github.com/matrix-org/matrix-react-sdk/pull/7749)). Fixes #20946. Contributed by @SimonBrandner.

Changes in [1.10.4](https://github.com/vector-im/element-web/releases/tag/v1.10.4) (2022-02-17)
===============================================================================================

## 🐛 Bug Fixes
 * Fix bug where badge colour on encrypted rooms may not be correct until anothe rmessage is sent

Changes in [1.10.3](https://github.com/vector-im/element-web/releases/tag/v1.10.3) (2022-02-14)
===============================================================================================

 * Add map tile URL for location sharing maps to sample config (and element.io release app config)

Changes in [1.10.2](https://github.com/vector-im/element-web/releases/tag/v1.10.2) (2022-02-14)
===============================================================================================

## ✨ Features
 * Support a config option to change the default device name ([\#20790](https://github.com/vector-im/element-web/pull/20790)).
 * Capitalize "Privacy" in UserMenu ([\#7738](https://github.com/matrix-org/matrix-react-sdk/pull/7738)). Contributed by @aaronraimist.
 * Move new search experience to a Beta ([\#7718](https://github.com/matrix-org/matrix-react-sdk/pull/7718)). Fixes vector-im/element-meta#139 #20618 and #20339.
 * Auto select "Other homeserver" when user press "Edit" in homeserver field ([\#7337](https://github.com/matrix-org/matrix-react-sdk/pull/7337)). Fixes #20125. Contributed by @SimonBrandner.
 * Add unread badges and avatar decorations to spotlight search ([\#7696](https://github.com/matrix-org/matrix-react-sdk/pull/7696)). Fixes #20821.
 * Enable location sharing ([\#7703](https://github.com/matrix-org/matrix-react-sdk/pull/7703)).
 * Simplify Composer buttons ([\#7678](https://github.com/matrix-org/matrix-react-sdk/pull/7678)).
 * Add a warning to the console to discourage attacks and encourage contributing ([\#7673](https://github.com/matrix-org/matrix-react-sdk/pull/7673)). Fixes #2803. Contributed by @SimonBrandner.
 * Don't show replaced calls in the timeline ([\#7452](https://github.com/matrix-org/matrix-react-sdk/pull/7452)). Contributed by @SimonBrandner.
 * Tweak `/addwidget` widget names ([\#7681](https://github.com/matrix-org/matrix-react-sdk/pull/7681)).
 * Chat export parameter customisation ([\#7647](https://github.com/matrix-org/matrix-react-sdk/pull/7647)).
 * Put call on hold when transfer dialog is opened ([\#7669](https://github.com/matrix-org/matrix-react-sdk/pull/7669)).
 * Share e2ee keys when using /invite SlashCommand ([\#7655](https://github.com/matrix-org/matrix-react-sdk/pull/7655)). Fixes #20778 and #16982.
 * Tweak spotlight roving behaviour to reset when changing query ([\#7656](https://github.com/matrix-org/matrix-react-sdk/pull/7656)). Fixes #20537 #20612 and #20184.
 * Look up tile server info in homeserver's .well-known area ([\#7623](https://github.com/matrix-org/matrix-react-sdk/pull/7623)).
 * Add grouper for hidden events ([\#7649](https://github.com/matrix-org/matrix-react-sdk/pull/7649)).
 * The keyboard shortcut is control (or cmd) shift h. ([\#7584](https://github.com/matrix-org/matrix-react-sdk/pull/7584)). Contributed by @UwUnyaa.

## 🐛 Bug Fixes
 * [Release] Fix cutout misalignment on some decorated room avatars ([\#7785](https://github.com/matrix-org/matrix-react-sdk/pull/7785)).
 * [Release] Fix add existing space not showing any spaces ([\#7756](https://github.com/matrix-org/matrix-react-sdk/pull/7756)).
 * [Release] Inhibit Room List keyboard pass-thru when the search beta is enabled ([\#7754](https://github.com/matrix-org/matrix-react-sdk/pull/7754)).
 * [Release] Fix space member list not opening ([\#7755](https://github.com/matrix-org/matrix-react-sdk/pull/7755)).
 * Null-guard ELS from null summaryMembers ([\#7744](https://github.com/matrix-org/matrix-react-sdk/pull/7744)). Fixes #20807.
 * Improve responsiveness of the layout switcher ([\#7736](https://github.com/matrix-org/matrix-react-sdk/pull/7736)).
 * Tweak timeline card layout ([\#7743](https://github.com/matrix-org/matrix-react-sdk/pull/7743)). Fixes #20846.
 * Ensure location bodies have a width in bubbles ([\#7742](https://github.com/matrix-org/matrix-react-sdk/pull/7742)). Fixes #20916.
 * Tune aria-live regions around clocks/timers ([\#7735](https://github.com/matrix-org/matrix-react-sdk/pull/7735)). Fixes #20967.
 * Fix instances of decorated room avatar wrongly having their own tabIndex ([\#7730](https://github.com/matrix-org/matrix-react-sdk/pull/7730)).
 * Remove weird padding on stickers ([\#6271](https://github.com/matrix-org/matrix-react-sdk/pull/6271)). Fixes #17787. Contributed by @SimonBrandner.
 * Fix width issue of the composer overflow menu items ([\#7731](https://github.com/matrix-org/matrix-react-sdk/pull/7731)). Fixes #20898.
 * Properly handle persistent widgets when room is left ([\#7724](https://github.com/matrix-org/matrix-react-sdk/pull/7724)). Fixes #20901.
 * Null guard space hierarchy ([\#7729](https://github.com/matrix-org/matrix-react-sdk/pull/7729)). Fixes matrix-org/element-web-rageshakes#10433.
 * Fix add existing rooms button ([\#7728](https://github.com/matrix-org/matrix-react-sdk/pull/7728)). Fixes #20924. Contributed by @SimonBrandner.
 * Truncate long server names on login/register screen ([\#7702](https://github.com/matrix-org/matrix-react-sdk/pull/7702)). Fixes #18452.
 * Update PollCreateDialog-test to snapshot the html and not react tree ([\#7712](https://github.com/matrix-org/matrix-react-sdk/pull/7712)).
 * Fix creating polls outside of threads ([\#7711](https://github.com/matrix-org/matrix-react-sdk/pull/7711)). Fixes #20882.
 * Open native room when clicking notification from a virtual room ([\#7709](https://github.com/matrix-org/matrix-react-sdk/pull/7709)).
 * Fix relative link handling in Element Desktop ([\#7708](https://github.com/matrix-org/matrix-react-sdk/pull/7708)). Fixes #20783.
 * Reuse CopyableText component in all places it can be ([\#7701](https://github.com/matrix-org/matrix-react-sdk/pull/7701)). Fixes #20855.
 * Fit location into the width of the container ([\#7705](https://github.com/matrix-org/matrix-react-sdk/pull/7705)). Fixes #20861.
 * Make Spotlight Dialog roving reset more stable ([\#7698](https://github.com/matrix-org/matrix-react-sdk/pull/7698)). Fixes #20826.
 * Fix incorrect sizing of DecoratedRoomAvatar in RoomHeader ([\#7697](https://github.com/matrix-org/matrix-react-sdk/pull/7697)). Fixes #20090.
 * Use a more correct test for emoji ([\#7685](https://github.com/matrix-org/matrix-react-sdk/pull/7685)). Fixes #20824. Contributed by @robintown.
 * Fix vertical spacing in `compact` `<ContextMenu>` ([\#7684](https://github.com/matrix-org/matrix-react-sdk/pull/7684)). Fixes #20801.
 * Fix the sticker picker ([\#7692](https://github.com/matrix-org/matrix-react-sdk/pull/7692)). Fixes #20797.
 * Fix publishing address wrongly demanding the alias be available ([\#7690](https://github.com/matrix-org/matrix-react-sdk/pull/7690)). Fixes #12013 and #20833.
 * Prevent MemberAvatar soft-crashing when rendered with null member prop ([\#7691](https://github.com/matrix-org/matrix-react-sdk/pull/7691)). Fixes #20714.
 * Ensure UserInfo can be rendered without a room ([\#7687](https://github.com/matrix-org/matrix-react-sdk/pull/7687)). Fixes #20830.
 * Make polls fill column width in bubbles layout ([\#7661](https://github.com/matrix-org/matrix-react-sdk/pull/7661)). Fixes #20712.
 * Add a background to expanded nick name in IRC layout to make it readable. ([\#7652](https://github.com/matrix-org/matrix-react-sdk/pull/7652)). Fixes #20757. Contributed by @UwUnyaa.
 * Fix accessibility and consistency of MessageComposerButtons ([\#7679](https://github.com/matrix-org/matrix-react-sdk/pull/7679)). Fixes #20814.
 * Don't show shield next to deleted messages ([\#7671](https://github.com/matrix-org/matrix-react-sdk/pull/7671)). Fixes #20475. Contributed by @SimonBrandner.
 * Fix font size of spaces between big emoji ([\#7675](https://github.com/matrix-org/matrix-react-sdk/pull/7675)). Contributed by @robintown.
 * Fix shift-enter repeating last character ([\#7665](https://github.com/matrix-org/matrix-react-sdk/pull/7665)). Fixes #17215. Contributed by @SimonBrandner.
 * Remove Unpin option from maximised widget context menu ([\#7657](https://github.com/matrix-org/matrix-react-sdk/pull/7657)).
 * Fix new call event grouper implementation for encrypted rooms ([\#7654](https://github.com/matrix-org/matrix-react-sdk/pull/7654)).
 * Fix issue with tile error boundaries collapsing in bubbles layout ([\#7653](https://github.com/matrix-org/matrix-react-sdk/pull/7653)).
 * Fix emojis getting cropped in irc & bubble layouts by anti-zalgo ([\#7637](https://github.com/matrix-org/matrix-react-sdk/pull/7637)). Fixes #20744.
 * Fix space panel edge gradient not applying on load ([\#7644](https://github.com/matrix-org/matrix-react-sdk/pull/7644)). Fixes #20756.
 * Fix search results view for layouts other than Group/Modern ([\#7648](https://github.com/matrix-org/matrix-react-sdk/pull/7648)). Fixes #20745.

Changes in [1.10.2-rc.2](https://github.com/vector-im/element-web/releases/tag/v1.10.2-rc.2) (2022-02-09)
=========================================================================================================

## 🐛 Bug Fixes
 * [Release] Fix add existing space not showing any spaces ([\#7756](https://github.com/matrix-org/matrix-react-sdk/pull/7756)).
 * [Release] Inhibit Room List keyboard pass-thru when the search beta is enabled ([\#7754](https://github.com/matrix-org/matrix-react-sdk/pull/7754)).
 * [Release] Fix space member list not opening ([\#7755](https://github.com/matrix-org/matrix-react-sdk/pull/7755)).

Changes in [1.10.2-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.10.2-rc.1) (2022-02-08)
=========================================================================================================

## ✨ Features
 * Support a config option to change the default device name ([\#20790](https://github.com/vector-im/element-web/pull/20790)).
 * Move new search experience to a Beta ([\#7718](https://github.com/matrix-org/matrix-react-sdk/pull/7718)). Fixes vector-im/element-meta#139 #20618 and #20339.
 * Capitalize "Privacy" in UserMenu ([\#7738](https://github.com/matrix-org/matrix-react-sdk/pull/7738)). Contributed by @aaronraimist.
 * Auto select "Other homeserver" when user press "Edit" in homeserver field ([\#7337](https://github.com/matrix-org/matrix-react-sdk/pull/7337)). Fixes #20125. Contributed by @SimonBrandner.
 * Add unread badges and avatar decorations to spotlight search ([\#7696](https://github.com/matrix-org/matrix-react-sdk/pull/7696)). Fixes #20821.
 * Enable location sharing ([\#7703](https://github.com/matrix-org/matrix-react-sdk/pull/7703)).
 * Simplify Composer buttons ([\#7678](https://github.com/matrix-org/matrix-react-sdk/pull/7678)).
 * Add a warning to the console to discourage attacks and encourage contributing ([\#7673](https://github.com/matrix-org/matrix-react-sdk/pull/7673)). Fixes #2803. Contributed by @SimonBrandner.
 * Don't show replaced calls in the timeline ([\#7452](https://github.com/matrix-org/matrix-react-sdk/pull/7452)). Contributed by @SimonBrandner.
 * Tweak `/addwidget` widget names ([\#7681](https://github.com/matrix-org/matrix-react-sdk/pull/7681)).
 * Chat export parameter customisation ([\#7647](https://github.com/matrix-org/matrix-react-sdk/pull/7647)).
 * Put call on hold when transfer dialog is opened ([\#7669](https://github.com/matrix-org/matrix-react-sdk/pull/7669)).
 * Share e2ee keys when using /invite SlashCommand ([\#7655](https://github.com/matrix-org/matrix-react-sdk/pull/7655)). Fixes #20778 and #16982.
 * Tweak spotlight roving behaviour to reset when changing query ([\#7656](https://github.com/matrix-org/matrix-react-sdk/pull/7656)). Fixes #20537 #20612 and #20184.
 * Look up tile server info in homeserver's .well-known area ([\#7623](https://github.com/matrix-org/matrix-react-sdk/pull/7623)).
 * Add grouper for hidden events ([\#7649](https://github.com/matrix-org/matrix-react-sdk/pull/7649)).
 * The keyboard shortcut is control (or cmd) shift h. ([\#7584](https://github.com/matrix-org/matrix-react-sdk/pull/7584)). Contributed by @UwUnyaa.

## 🐛 Bug Fixes
 * Null-guard ELS from null summaryMembers ([\#7744](https://github.com/matrix-org/matrix-react-sdk/pull/7744)). Fixes #20807.
 * Improve responsiveness of the layout switcher ([\#7736](https://github.com/matrix-org/matrix-react-sdk/pull/7736)).
 * Tweak timeline card layout ([\#7743](https://github.com/matrix-org/matrix-react-sdk/pull/7743)). Fixes #20846.
 * Ensure location bodies have a width in bubbles ([\#7742](https://github.com/matrix-org/matrix-react-sdk/pull/7742)). Fixes #20916.
 * Tune aria-live regions around clocks/timers ([\#7735](https://github.com/matrix-org/matrix-react-sdk/pull/7735)). Fixes #20967.
 * Fix instances of decorated room avatar wrongly having their own tabIndex ([\#7730](https://github.com/matrix-org/matrix-react-sdk/pull/7730)).
 * Remove weird padding on stickers ([\#6271](https://github.com/matrix-org/matrix-react-sdk/pull/6271)). Fixes #17787. Contributed by @SimonBrandner.
 * Fix width issue of the composer overflow menu items ([\#7731](https://github.com/matrix-org/matrix-react-sdk/pull/7731)). Fixes #20898.
 * Properly handle persistent widgets when room is left ([\#7724](https://github.com/matrix-org/matrix-react-sdk/pull/7724)). Fixes #20901.
 * Null guard space hierarchy ([\#7729](https://github.com/matrix-org/matrix-react-sdk/pull/7729)). Fixes matrix-org/element-web-rageshakes#10433.
 * Fix add existing rooms button ([\#7728](https://github.com/matrix-org/matrix-react-sdk/pull/7728)). Fixes #20924. Contributed by @SimonBrandner.
 * Truncate long server names on login/register screen ([\#7702](https://github.com/matrix-org/matrix-react-sdk/pull/7702)). Fixes #18452.
 * Update PollCreateDialog-test to snapshot the html and not react tree ([\#7712](https://github.com/matrix-org/matrix-react-sdk/pull/7712)).
 * Fix creating polls outside of threads ([\#7711](https://github.com/matrix-org/matrix-react-sdk/pull/7711)). Fixes #20882.
 * Open native room when clicking notification from a virtual room ([\#7709](https://github.com/matrix-org/matrix-react-sdk/pull/7709)).
 * Fix relative link handling in Element Desktop ([\#7708](https://github.com/matrix-org/matrix-react-sdk/pull/7708)). Fixes #20783.
 * Reuse CopyableText component in all places it can be ([\#7701](https://github.com/matrix-org/matrix-react-sdk/pull/7701)). Fixes #20855.
 * Fit location into the width of the container ([\#7705](https://github.com/matrix-org/matrix-react-sdk/pull/7705)). Fixes #20861.
 * Make Spotlight Dialog roving reset more stable ([\#7698](https://github.com/matrix-org/matrix-react-sdk/pull/7698)). Fixes #20826.
 * Fix incorrect sizing of DecoratedRoomAvatar in RoomHeader ([\#7697](https://github.com/matrix-org/matrix-react-sdk/pull/7697)). Fixes #20090.
 * Use a more correct test for emoji ([\#7685](https://github.com/matrix-org/matrix-react-sdk/pull/7685)). Fixes #20824. Contributed by @robintown.
 * Fix vertical spacing in `compact` `<ContextMenu>` ([\#7684](https://github.com/matrix-org/matrix-react-sdk/pull/7684)). Fixes #20801.
 * Fix the sticker picker ([\#7692](https://github.com/matrix-org/matrix-react-sdk/pull/7692)). Fixes #20797.
 * Fix publishing address wrongly demanding the alias be available ([\#7690](https://github.com/matrix-org/matrix-react-sdk/pull/7690)). Fixes #12013 and #20833.
 * Prevent MemberAvatar soft-crashing when rendered with null member prop ([\#7691](https://github.com/matrix-org/matrix-react-sdk/pull/7691)). Fixes #20714.
 * Ensure UserInfo can be rendered without a room ([\#7687](https://github.com/matrix-org/matrix-react-sdk/pull/7687)). Fixes #20830.
 * Make polls fill column width in bubbles layout ([\#7661](https://github.com/matrix-org/matrix-react-sdk/pull/7661)). Fixes #20712.
 * Add a background to expanded nick name in IRC layout to make it readable. ([\#7652](https://github.com/matrix-org/matrix-react-sdk/pull/7652)). Fixes #20757. Contributed by @UwUnyaa.
 * Fix accessibility and consistency of MessageComposerButtons ([\#7679](https://github.com/matrix-org/matrix-react-sdk/pull/7679)). Fixes #20814.
 * Don't show shield next to deleted messages ([\#7671](https://github.com/matrix-org/matrix-react-sdk/pull/7671)). Fixes #20475. Contributed by @SimonBrandner.
 * Fix font size of spaces between big emoji ([\#7675](https://github.com/matrix-org/matrix-react-sdk/pull/7675)). Contributed by @robintown.
 * Fix shift-enter repeating last character ([\#7665](https://github.com/matrix-org/matrix-react-sdk/pull/7665)). Fixes #17215. Contributed by @SimonBrandner.
 * Remove Unpin option from maximised widget context menu ([\#7657](https://github.com/matrix-org/matrix-react-sdk/pull/7657)).
 * Fix new call event grouper implementation for encrypted rooms ([\#7654](https://github.com/matrix-org/matrix-react-sdk/pull/7654)).
 * Fix issue with tile error boundaries collapsing in bubbles layout ([\#7653](https://github.com/matrix-org/matrix-react-sdk/pull/7653)).
 * Fix emojis getting cropped in irc & bubble layouts by anti-zalgo ([\#7637](https://github.com/matrix-org/matrix-react-sdk/pull/7637)). Fixes #20744.
 * Fix space panel edge gradient not applying on load ([\#7644](https://github.com/matrix-org/matrix-react-sdk/pull/7644)). Fixes #20756.
 * Fix search results view for layouts other than Group/Modern ([\#7648](https://github.com/matrix-org/matrix-react-sdk/pull/7648)). Fixes #20745.

Changes in [1.10.1](https://github.com/vector-im/element-web/releases/tag/v1.10.1) (2022-02-01)
===============================================================================================

## 🐛 Bug Fixes
 * Fix the sticker picker ([\#7692](https://github.com/matrix-org/matrix-react-sdk/pull/7692)). Fixes vector-im/element-web#20797.
 * Ensure UserInfo can be rendered without a room ([\#7687](https://github.com/matrix-org/matrix-react-sdk/pull/7687)). Fixes vector-im/element-web#20830.
 * Fix publishing address wrongly demanding the alias be available ([\#7690](https://github.com/matrix-org/matrix-react-sdk/pull/7690)). Fixes vector-im/element-web#12013 and vector-im/element-web#20833.

Changes in [1.10.0](https://github.com/vector-im/element-web/releases/tag/v1.10.0) (2022-01-31)
===============================================================================================

## ✨ Features
 * Tweak room list header menu for when space is active ([\#7577](https://github.com/matrix-org/matrix-react-sdk/pull/7577)). Fixes #20601.
 * Tweak light hover & active color for bubble layout ([\#7626](https://github.com/matrix-org/matrix-react-sdk/pull/7626)). Fixes #19475.
 * De-labs Metaspaces ([\#7613](https://github.com/matrix-org/matrix-react-sdk/pull/7613)).
 * De-labs Message Bubbles layout ([\#7612](https://github.com/matrix-org/matrix-react-sdk/pull/7612)).
 * Add customisation point for mxid display ([\#7595](https://github.com/matrix-org/matrix-react-sdk/pull/7595)).
 * Add labs flag for default open right panel ([\#7618](https://github.com/matrix-org/matrix-react-sdk/pull/7618)). Fixes #20666.
 * Tweak copy for the Sidebar tab in User Settings ([\#7578](https://github.com/matrix-org/matrix-react-sdk/pull/7578)). Fixes #20619.
 * Make widgets not reload (persistent) between center and top container  ([\#7575](https://github.com/matrix-org/matrix-react-sdk/pull/7575)). Fixes #20596. Contributed by @toger5.
 * Don't render a bubble around emotes in bubble layout ([\#7573](https://github.com/matrix-org/matrix-react-sdk/pull/7573)). Fixes #20617.
 * Add ability to switch between voice & video in calls ([\#7155](https://github.com/matrix-org/matrix-react-sdk/pull/7155)). Fixes #18619. Contributed by @SimonBrandner.
 * Re-renable Share option for location messages ([\#7596](https://github.com/matrix-org/matrix-react-sdk/pull/7596)).
 * Make room ID copyable ([\#7600](https://github.com/matrix-org/matrix-react-sdk/pull/7600)). Fixes #20675. Contributed by @SimonBrandner.
 * Improve the look of the keyboard settings tab ([\#7562](https://github.com/matrix-org/matrix-react-sdk/pull/7562)). Contributed by @SimonBrandner.
 * Add tooltips to emoji in messages ([\#7592](https://github.com/matrix-org/matrix-react-sdk/pull/7592)). Fixes #9911 and #20661. Contributed by @robintown.
 * Improve redundant tooltip on send button in forward dialog ([\#7594](https://github.com/matrix-org/matrix-react-sdk/pull/7594)). Contributed by @twigleingrid.
 * Allow downloads from widgets. ([\#7502](https://github.com/matrix-org/matrix-react-sdk/pull/7502)). Contributed by @Fox32.
 * Parse matrix-schemed URIs ([\#7453](https://github.com/matrix-org/matrix-react-sdk/pull/7453)).
 * Show a tile at beginning of visible history ([\#5887](https://github.com/matrix-org/matrix-react-sdk/pull/5887)). Fixes #16818 #16679 and #19888. Contributed by @robintown.
 * Enable the polls feature ([\#7581](https://github.com/matrix-org/matrix-react-sdk/pull/7581)).
 * Display general marker on non-self location shares ([\#7574](https://github.com/matrix-org/matrix-react-sdk/pull/7574)).
 * Improve/add notifications for location and poll events ([\#7552](https://github.com/matrix-org/matrix-react-sdk/pull/7552)). Fixes #20561. Contributed by @SimonBrandner.
 * Upgrade linkify to v3.0 ([\#7282](https://github.com/matrix-org/matrix-react-sdk/pull/7282)). Fixes #17133 #16825 and #5808. Contributed by @Palid.
 * Update sidebar icon from Compound ([\#7572](https://github.com/matrix-org/matrix-react-sdk/pull/7572)). Fixes #20615.
 * Replace home icon with new one ([\#7571](https://github.com/matrix-org/matrix-react-sdk/pull/7571)). Fixes #20606.
 * Make the `Keyboard Shortcuts` dialog into a settings tab ([\#7198](https://github.com/matrix-org/matrix-react-sdk/pull/7198)). Fixes #19866. Contributed by @SimonBrandner.
 * Add setting for enabling location sharing ([\#7547](https://github.com/matrix-org/matrix-react-sdk/pull/7547)).
 * Add a developer mode 'view source' button to crashed event tiles ([\#7537](https://github.com/matrix-org/matrix-react-sdk/pull/7537)).
 * Replace `kick` terminology with `Remove from chat` ([\#7469](https://github.com/matrix-org/matrix-react-sdk/pull/7469)). Fixes #9547.
 * Render events as extensible events (behind labs) ([\#7462](https://github.com/matrix-org/matrix-react-sdk/pull/7462)).
 * Render Jitsi (and other sticky widgets) in PiP container, so it can be dragged and the "jump to room functionality" is provided ([\#7450](https://github.com/matrix-org/matrix-react-sdk/pull/7450)). Fixes #15682. Contributed by @toger5.
 * Allow bubble layout in Thread View ([\#7478](https://github.com/matrix-org/matrix-react-sdk/pull/7478)). Fixes #20419.
 * Make LocationPicker appearance cleaner ([\#7516](https://github.com/matrix-org/matrix-react-sdk/pull/7516)).
 * Limit max-width for bubble layout to 1200px ([\#7458](https://github.com/matrix-org/matrix-react-sdk/pull/7458)). Fixes #18072.
 * Improve look of call events in bubble layout ([\#7445](https://github.com/matrix-org/matrix-react-sdk/pull/7445)). Fixes #20324. Contributed by @SimonBrandner.
 * Make files & voice memos in bubble layout match colouring ([\#7457](https://github.com/matrix-org/matrix-react-sdk/pull/7457)). Fixes #20326.
 * Allow cancelling events whilst they are encrypting ([\#7483](https://github.com/matrix-org/matrix-react-sdk/pull/7483)). Fixes #17726.

## 🐛 Bug Fixes
 * [Release] Fix left panel widgets causing app-wide crash ([\#7660](https://github.com/matrix-org/matrix-react-sdk/pull/7660)).
 * Load light theme prior to HTML export to ensure it is present ([\#7643](https://github.com/matrix-org/matrix-react-sdk/pull/7643)). Fixes #20276.
 * Fix soft-crash when hanging up Jitsi via PIP ([\#7645](https://github.com/matrix-org/matrix-react-sdk/pull/7645)). Fixes #20766.
 * Fix RightPanelStore assuming isViewingRoom is false on load ([\#7642](https://github.com/matrix-org/matrix-react-sdk/pull/7642)).
 * Correctly handle Room.timeline events which have a nullable `Room` ([\#7635](https://github.com/matrix-org/matrix-react-sdk/pull/7635)). Fixes matrix-org/element-web-rageshakes#9490.
 * Translate keyboard shortcut alternate key names ([\#7633](https://github.com/matrix-org/matrix-react-sdk/pull/7633)). Fixes #20739.
 * Fix unfocused paste handling and focus return for file uploads ([\#7625](https://github.com/matrix-org/matrix-react-sdk/pull/7625)).
 * Changed MacOS hotkey for GoToHome view. ([\#7631](https://github.com/matrix-org/matrix-react-sdk/pull/7631)). Contributed by @aj-ya.
 * Fix issue with the new composer EmojiPart which caused infinite loops ([\#7629](https://github.com/matrix-org/matrix-react-sdk/pull/7629)). Fixes #20746.
 * Upgrade linkifyjs to fix schemes as domain prefixes ([\#7628](https://github.com/matrix-org/matrix-react-sdk/pull/7628)). Fixes #20720.
 * Show bubble tile timestamps for bubble layout inside the bubble ([\#7622](https://github.com/matrix-org/matrix-react-sdk/pull/7622)). Fixes #20562.
 *  Improve taken username warning in registration for when request fails ([\#7621](https://github.com/matrix-org/matrix-react-sdk/pull/7621)).
 * Avoid double dialog after clicking to remove a public room ([\#7604](https://github.com/matrix-org/matrix-react-sdk/pull/7604)). Fixes #20681. Contributed by @c-cal.
 * Fix space member list right panel state ([\#7617](https://github.com/matrix-org/matrix-react-sdk/pull/7617)). Fixes #20716.
 * Fall back to legacy analytics for guest users ([\#7616](https://github.com/matrix-org/matrix-react-sdk/pull/7616)).
 * Always emit a space filter update when the space is actually changed ([\#7611](https://github.com/matrix-org/matrix-react-sdk/pull/7611)). Fixes #20664.
 * Enlarge emoji in composer ([\#7602](https://github.com/matrix-org/matrix-react-sdk/pull/7602)). Fixes #20665 #15635 and #20688. Contributed by @robintown.
 * Disable location sharing button on Desktop ([\#7590](https://github.com/matrix-org/matrix-react-sdk/pull/7590)).
 * Make pills more natural to navigate around ([\#7607](https://github.com/matrix-org/matrix-react-sdk/pull/7607)). Fixes #20678. Contributed by @robintown.
 * Fix excessive padding on inline images ([\#7605](https://github.com/matrix-org/matrix-react-sdk/pull/7605)). Contributed by @robintown.
 * Prevent pills from being split by formatting actions ([\#7606](https://github.com/matrix-org/matrix-react-sdk/pull/7606)). Contributed by @robintown.
 * Fix translation of "powerText" ([\#7603](https://github.com/matrix-org/matrix-react-sdk/pull/7603)). Contributed by @c-cal.
 * Unhide display names when switching back to modern layout ([\#7601](https://github.com/matrix-org/matrix-react-sdk/pull/7601)). Fixes #20676. Contributed by @robintown.
 * Fix space member list not opening ([\#7609](https://github.com/matrix-org/matrix-react-sdk/pull/7609)). Fixes #20679. Contributed by @SimonBrandner.
 * Fix translation for the "Add room" tooltip ([\#7532](https://github.com/matrix-org/matrix-react-sdk/pull/7532)). Contributed by @c-cal.
 * Make the close button of the location share dialog visible in high-contrast theme ([\#7597](https://github.com/matrix-org/matrix-react-sdk/pull/7597)).
 * Cancel pending events in virtual room when call placed ([\#7583](https://github.com/matrix-org/matrix-react-sdk/pull/7583)). Fixes #17594.
 * Fix alignment of unread badge in thread list ([\#7582](https://github.com/matrix-org/matrix-react-sdk/pull/7582)). Fixes #20643.
 * Fix left positioned tooltips being wrong and offset by fixed value ([\#7551](https://github.com/matrix-org/matrix-react-sdk/pull/7551)).
 * Fix MAB overlapping or overflowing in bubbles layout and threads regressions ([\#7569](https://github.com/matrix-org/matrix-react-sdk/pull/7569)). Fixes #20403 and #20404.
 * Fix wrong icon being used for appearance tab in space preferences dialog ([\#7570](https://github.com/matrix-org/matrix-react-sdk/pull/7570)). Fixes #20608.
 * Fix `/jumptodate` using wrong MSC feature flag ([\#7563](https://github.com/matrix-org/matrix-react-sdk/pull/7563)).
 * Ensure maps show up in replies and threads, by creating unique IDs ([\#7568](https://github.com/matrix-org/matrix-react-sdk/pull/7568)).
 * Differentiate between hover and roving focus in spotlight dialog ([\#7564](https://github.com/matrix-org/matrix-react-sdk/pull/7564)). Fixes #20597.
 * Fix timeline jumping issues related to bubble layout ([\#7529](https://github.com/matrix-org/matrix-react-sdk/pull/7529)). Fixes #20302.
 * Start a conference in a room with 2 people + invitee rather than a 1:1 call ([\#7557](https://github.com/matrix-org/matrix-react-sdk/pull/7557)). Fixes #1202. Contributed by @SimonBrandner.
 * Wait for initial profile load before displaying widget ([\#7556](https://github.com/matrix-org/matrix-react-sdk/pull/7556)).
 * Make widgets and calls span across the whole room width when using bubble layout ([\#7553](https://github.com/matrix-org/matrix-react-sdk/pull/7553)). Fixes #20560. Contributed by @SimonBrandner.
 * Always show right panel after setting a card ([\#7544](https://github.com/matrix-org/matrix-react-sdk/pull/7544)). Contributed by @toger5.
 * Support deserialising HR tags for editing ([\#7543](https://github.com/matrix-org/matrix-react-sdk/pull/7543)). Fixes #20553.
 * Refresh ThreadView after React state has been updated ([\#7539](https://github.com/matrix-org/matrix-react-sdk/pull/7539)). Fixes #20549.
 * Set initial zoom level to 1 to make zooming to location faster ([\#7541](https://github.com/matrix-org/matrix-react-sdk/pull/7541)).
 * truncate room name on pip header ([\#7538](https://github.com/matrix-org/matrix-react-sdk/pull/7538)).
 * Prevent enter to send edit weirdness when no change has been made ([\#7522](https://github.com/matrix-org/matrix-react-sdk/pull/7522)). Fixes #20507.
 * Allow using room pills in slash commands ([\#7513](https://github.com/matrix-org/matrix-react-sdk/pull/7513)). Fixes #20343.

Changes in [1.9.10-rc.2](https://github.com/vector-im/element-web/releases/tag/v1.9.10-rc.2) (2022-01-26)
=========================================================================================================

## 🐛 Bug Fixes
 * Fix crash in settings / appearance

Changes in [1.9.10-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.9.10-rc.1) (2022-01-26)
=========================================================================================================

## ✨ Features
 * Enable posthog on app.element.io ([\#20539](https://github.com/vector-im/element-web/pull/20539)).
 * Tweak room list header menu for when space is active ([\#7577](https://github.com/matrix-org/matrix-react-sdk/pull/7577)). Fixes #20601.
 * Tweak light hover & active color for bubble layout ([\#7626](https://github.com/matrix-org/matrix-react-sdk/pull/7626)). Fixes #19475.
 * De-labs Metaspaces ([\#7613](https://github.com/matrix-org/matrix-react-sdk/pull/7613)).
 * De-labs Message Bubbles layout ([\#7612](https://github.com/matrix-org/matrix-react-sdk/pull/7612)).
 * Add customisation point for mxid display ([\#7595](https://github.com/matrix-org/matrix-react-sdk/pull/7595)).
 * Add labs flag for default open right panel ([\#7618](https://github.com/matrix-org/matrix-react-sdk/pull/7618)). Fixes #20666.
 * Tweak copy for the Sidebar tab in User Settings ([\#7578](https://github.com/matrix-org/matrix-react-sdk/pull/7578)). Fixes #20619.
 * Make widgets not reload (persistent) between center and top container  ([\#7575](https://github.com/matrix-org/matrix-react-sdk/pull/7575)). Fixes #20596. Contributed by @toger5.
 * Don't render a bubble around emotes in bubble layout ([\#7573](https://github.com/matrix-org/matrix-react-sdk/pull/7573)). Fixes #20617.
 * Add ability to switch between voice & video in calls ([\#7155](https://github.com/matrix-org/matrix-react-sdk/pull/7155)). Fixes #18619. Contributed by @SimonBrandner.
 * Re-renable Share option for location messages ([\#7596](https://github.com/matrix-org/matrix-react-sdk/pull/7596)).
 * Make room ID copyable ([\#7600](https://github.com/matrix-org/matrix-react-sdk/pull/7600)). Fixes #20675. Contributed by @SimonBrandner.
 * Improve the look of the keyboard settings tab ([\#7562](https://github.com/matrix-org/matrix-react-sdk/pull/7562)). Contributed by @SimonBrandner.
 * Add tooltips to emoji in messages ([\#7592](https://github.com/matrix-org/matrix-react-sdk/pull/7592)). Fixes #9911 and #20661. Contributed by @robintown.
 * Improve redundant tooltip on send button in forward dialog ([\#7594](https://github.com/matrix-org/matrix-react-sdk/pull/7594)). Contributed by @twigleingrid.
 * Allow downloads from widgets. ([\#7502](https://github.com/matrix-org/matrix-react-sdk/pull/7502)). Contributed by @Fox32.
 * Parse matrix-schemed URIs ([\#7453](https://github.com/matrix-org/matrix-react-sdk/pull/7453)).
 * Show a tile at beginning of visible history ([\#5887](https://github.com/matrix-org/matrix-react-sdk/pull/5887)). Fixes #16818 #16679 and #19888. Contributed by @robintown.
 * Enable the polls feature ([\#7581](https://github.com/matrix-org/matrix-react-sdk/pull/7581)).
 * Display general marker on non-self location shares ([\#7574](https://github.com/matrix-org/matrix-react-sdk/pull/7574)).
 * Improve/add notifications for location and poll events ([\#7552](https://github.com/matrix-org/matrix-react-sdk/pull/7552)). Fixes #20561. Contributed by @SimonBrandner.
 * Upgrade linkify to v3.0 ([\#7282](https://github.com/matrix-org/matrix-react-sdk/pull/7282)). Fixes #17133 #16825 and #5808. Contributed by @Palid.
 * Update sidebar icon from Compound ([\#7572](https://github.com/matrix-org/matrix-react-sdk/pull/7572)). Fixes #20615.
 * Replace home icon with new one ([\#7571](https://github.com/matrix-org/matrix-react-sdk/pull/7571)). Fixes #20606.
 * Make the `Keyboard Shortcuts` dialog into a settings tab ([\#7198](https://github.com/matrix-org/matrix-react-sdk/pull/7198)). Fixes #19866. Contributed by @SimonBrandner.
 * Add setting for enabling location sharing ([\#7547](https://github.com/matrix-org/matrix-react-sdk/pull/7547)).
 * Add a developer mode 'view source' button to crashed event tiles ([\#7537](https://github.com/matrix-org/matrix-react-sdk/pull/7537)).
 * Replace `kick` terminology with `Remove from chat` ([\#7469](https://github.com/matrix-org/matrix-react-sdk/pull/7469)). Fixes #9547.
 * Render events as extensible events (behind labs) ([\#7462](https://github.com/matrix-org/matrix-react-sdk/pull/7462)).
 * Render Jitsi (and other sticky widgets) in PiP container, so it can be dragged and the "jump to room functionality" is provided ([\#7450](https://github.com/matrix-org/matrix-react-sdk/pull/7450)). Fixes #15682. Contributed by @toger5.
 * Allow bubble layout in Thread View ([\#7478](https://github.com/matrix-org/matrix-react-sdk/pull/7478)). Fixes #20419.
 * Make LocationPicker appearance cleaner ([\#7516](https://github.com/matrix-org/matrix-react-sdk/pull/7516)).
 * Limit max-width for bubble layout to 1200px ([\#7458](https://github.com/matrix-org/matrix-react-sdk/pull/7458)). Fixes #18072.
 * Improve look of call events in bubble layout ([\#7445](https://github.com/matrix-org/matrix-react-sdk/pull/7445)). Fixes #20324. Contributed by @SimonBrandner.
 * Make files & voice memos in bubble layout match colouring ([\#7457](https://github.com/matrix-org/matrix-react-sdk/pull/7457)). Fixes #20326.
 * Allow cancelling events whilst they are encrypting ([\#7483](https://github.com/matrix-org/matrix-react-sdk/pull/7483)). Fixes #17726.

## 🐛 Bug Fixes
 * Load light theme prior to HTML export to ensure it is present ([\#7643](https://github.com/matrix-org/matrix-react-sdk/pull/7643)). Fixes #20276.
 * Fix soft-crash when hanging up Jitsi via PIP ([\#7645](https://github.com/matrix-org/matrix-react-sdk/pull/7645)). Fixes #20766.
 * Fix RightPanelStore assuming isViewingRoom is false on load ([\#7642](https://github.com/matrix-org/matrix-react-sdk/pull/7642)).
 * Correctly handle Room.timeline events which have a nullable `Room` ([\#7635](https://github.com/matrix-org/matrix-react-sdk/pull/7635)). Fixes matrix-org/element-web-rageshakes#9490.
 * Translate keyboard shortcut alternate key names ([\#7633](https://github.com/matrix-org/matrix-react-sdk/pull/7633)). Fixes #20739.
 * Fix unfocused paste handling and focus return for file uploads ([\#7625](https://github.com/matrix-org/matrix-react-sdk/pull/7625)).
 * Changed MacOS hotkey for GoToHome view. ([\#7631](https://github.com/matrix-org/matrix-react-sdk/pull/7631)). Contributed by @aj-ya.
 * Fix issue with the new composer EmojiPart which caused infinite loops ([\#7629](https://github.com/matrix-org/matrix-react-sdk/pull/7629)). Fixes #20746.
 * Upgrade linkifyjs to fix schemes as domain prefixes ([\#7628](https://github.com/matrix-org/matrix-react-sdk/pull/7628)). Fixes #20720.
 * Show bubble tile timestamps for bubble layout inside the bubble ([\#7622](https://github.com/matrix-org/matrix-react-sdk/pull/7622)). Fixes #20562.
 *  Improve taken username warning in registration for when request fails ([\#7621](https://github.com/matrix-org/matrix-react-sdk/pull/7621)).
 * Avoid double dialog after clicking to remove a public room ([\#7604](https://github.com/matrix-org/matrix-react-sdk/pull/7604)). Fixes #20681. Contributed by @c-cal.
 * Fix space member list right panel state ([\#7617](https://github.com/matrix-org/matrix-react-sdk/pull/7617)). Fixes #20716.
 * Fall back to legacy analytics for guest users ([\#7616](https://github.com/matrix-org/matrix-react-sdk/pull/7616)).
 * Always emit a space filter update when the space is actually changed ([\#7611](https://github.com/matrix-org/matrix-react-sdk/pull/7611)). Fixes #20664.
 * Enlarge emoji in composer ([\#7602](https://github.com/matrix-org/matrix-react-sdk/pull/7602)). Fixes #20665 #15635 and #20688. Contributed by @robintown.
 * Disable location sharing button on Desktop ([\#7590](https://github.com/matrix-org/matrix-react-sdk/pull/7590)).
 * Make pills more natural to navigate around ([\#7607](https://github.com/matrix-org/matrix-react-sdk/pull/7607)). Fixes #20678. Contributed by @robintown.
 * Fix excessive padding on inline images ([\#7605](https://github.com/matrix-org/matrix-react-sdk/pull/7605)). Contributed by @robintown.
 * Prevent pills from being split by formatting actions ([\#7606](https://github.com/matrix-org/matrix-react-sdk/pull/7606)). Contributed by @robintown.
 * Fix translation of "powerText" ([\#7603](https://github.com/matrix-org/matrix-react-sdk/pull/7603)). Contributed by @c-cal.
 * Unhide display names when switching back to modern layout ([\#7601](https://github.com/matrix-org/matrix-react-sdk/pull/7601)). Fixes #20676. Contributed by @robintown.
 * Fix space member list not opening ([\#7609](https://github.com/matrix-org/matrix-react-sdk/pull/7609)). Fixes #20679. Contributed by @SimonBrandner.
 * Fix translation for the "Add room" tooltip ([\#7532](https://github.com/matrix-org/matrix-react-sdk/pull/7532)). Contributed by @c-cal.
 * Make the close button of the location share dialog visible in high-contrast theme ([\#7597](https://github.com/matrix-org/matrix-react-sdk/pull/7597)).
 * Cancel pending events in virtual room when call placed ([\#7583](https://github.com/matrix-org/matrix-react-sdk/pull/7583)). Fixes #17594.
 * Fix alignment of unread badge in thread list ([\#7582](https://github.com/matrix-org/matrix-react-sdk/pull/7582)). Fixes #20643.
 * Fix left positioned tooltips being wrong and offset by fixed value ([\#7551](https://github.com/matrix-org/matrix-react-sdk/pull/7551)).
 * Fix MAB overlapping or overflowing in bubbles layout and threads regressions ([\#7569](https://github.com/matrix-org/matrix-react-sdk/pull/7569)). Fixes #20403 and #20404.
 * Fix wrong icon being used for appearance tab in space preferences dialog ([\#7570](https://github.com/matrix-org/matrix-react-sdk/pull/7570)). Fixes #20608.
 * Fix `/jumptodate` using wrong MSC feature flag ([\#7563](https://github.com/matrix-org/matrix-react-sdk/pull/7563)).
 * Ensure maps show up in replies and threads, by creating unique IDs ([\#7568](https://github.com/matrix-org/matrix-react-sdk/pull/7568)).
 * Differentiate between hover and roving focus in spotlight dialog ([\#7564](https://github.com/matrix-org/matrix-react-sdk/pull/7564)). Fixes #20597.
 * Fix timeline jumping issues related to bubble layout ([\#7529](https://github.com/matrix-org/matrix-react-sdk/pull/7529)). Fixes #20302.
 * Start a conference in a room with 2 people + invitee rather than a 1:1 call ([\#7557](https://github.com/matrix-org/matrix-react-sdk/pull/7557)). Fixes #1202. Contributed by @SimonBrandner.
 * Wait for initial profile load before displaying widget ([\#7556](https://github.com/matrix-org/matrix-react-sdk/pull/7556)).
 * Make widgets and calls span across the whole room width when using bubble layout ([\#7553](https://github.com/matrix-org/matrix-react-sdk/pull/7553)). Fixes #20560. Contributed by @SimonBrandner.
 * Always show right panel after setting a card ([\#7544](https://github.com/matrix-org/matrix-react-sdk/pull/7544)). Contributed by @toger5.
 * Support deserialising HR tags for editing ([\#7543](https://github.com/matrix-org/matrix-react-sdk/pull/7543)). Fixes #20553.
 * Refresh ThreadView after React state has been updated ([\#7539](https://github.com/matrix-org/matrix-react-sdk/pull/7539)). Fixes #20549.
 * Set initial zoom level to 1 to make zooming to location faster ([\#7541](https://github.com/matrix-org/matrix-react-sdk/pull/7541)).
 * truncate room name on pip header ([\#7538](https://github.com/matrix-org/matrix-react-sdk/pull/7538)).
 * Prevent enter to send edit weirdness when no change has been made ([\#7522](https://github.com/matrix-org/matrix-react-sdk/pull/7522)). Fixes #20507.
 * Allow using room pills in slash commands ([\#7513](https://github.com/matrix-org/matrix-react-sdk/pull/7513)). Fixes #20343.

Changes in [1.9.9](https://github.com/vector-im/element-web/releases/tag/v1.9.9) (2022-01-17)
=============================================================================================

## ✨ Features
 * Add permission dropdown for sending reactions ([\#7492](https://github.com/matrix-org/matrix-react-sdk/pull/7492)). Fixes #20450.
 * Ship maximised widgets and remove feature flag ([\#7509](https://github.com/matrix-org/matrix-react-sdk/pull/7509)).
 * Properly maintain aspect ratio of inline images ([\#7503](https://github.com/matrix-org/matrix-react-sdk/pull/7503)).
 * Add zoom buttons to the location view ([\#7482](https://github.com/matrix-org/matrix-react-sdk/pull/7482)).
 * Remove bubble from around location events ([\#7459](https://github.com/matrix-org/matrix-react-sdk/pull/7459)). Fixes #20323.
 * Disable "Publish this room" option in invite only rooms ([\#7441](https://github.com/matrix-org/matrix-react-sdk/pull/7441)). Fixes #6596. Contributed by @aaronraimist.
 * Give secret key field an `id` ([\#7489](https://github.com/matrix-org/matrix-react-sdk/pull/7489)). Fixes #20390. Contributed by @SimonBrandner.
 * Display a tooltip when you hover over a location ([\#7472](https://github.com/matrix-org/matrix-react-sdk/pull/7472)).
 * Open map in a dialog when it is clicked ([\#7465](https://github.com/matrix-org/matrix-react-sdk/pull/7465)).
 * a11y - wrap notification level radios in fieldsets ([\#7471](https://github.com/matrix-org/matrix-react-sdk/pull/7471)).
 * Wrap inputs in fieldsets in Space visibility settings ([\#7350](https://github.com/matrix-org/matrix-react-sdk/pull/7350)).
 * History based navigation with new right panel store ([\#7398](https://github.com/matrix-org/matrix-react-sdk/pull/7398)). Fixes #19686 #19660 and #19634.
 * Associate room alias warning with public option in settings ([\#7430](https://github.com/matrix-org/matrix-react-sdk/pull/7430)).
 * Disable quick reactions button when no permissions ([\#7412](https://github.com/matrix-org/matrix-react-sdk/pull/7412)). Fixes #20270.
 * Allow opening a map view in OpenStreetMap ([\#7428](https://github.com/matrix-org/matrix-react-sdk/pull/7428)).
 * Display the user's avatar when they shared their location ([\#7424](https://github.com/matrix-org/matrix-react-sdk/pull/7424)).
 * Remove the Forward and Share buttons for location messages only ([\#7423](https://github.com/matrix-org/matrix-react-sdk/pull/7423)).
 * Add configuration to disable relative date markers in timeline ([\#7405](https://github.com/matrix-org/matrix-react-sdk/pull/7405)).
 * Space preferences for whether or not you see DMs in a Space ([\#7250](https://github.com/matrix-org/matrix-react-sdk/pull/7250)). Fixes #19529 and #19955.
 * Have LocalEchoWrapper emit updates so the app can react faster ([\#7358](https://github.com/matrix-org/matrix-react-sdk/pull/7358)). Fixes #19749.
 * Use semantic heading on dialog component ([\#7383](https://github.com/matrix-org/matrix-react-sdk/pull/7383)).
 * Add `/jumptodate` slash command ([\#7372](https://github.com/matrix-org/matrix-react-sdk/pull/7372)). Fixes #7677.
 * Update room context menu copy ([\#7361](https://github.com/matrix-org/matrix-react-sdk/pull/7361)). Fixes #20133.
 * Use lazy rendering in the AddExistingToSpaceDialog ([\#7369](https://github.com/matrix-org/matrix-react-sdk/pull/7369)). Fixes #18784.
 * Tweak FacePile tooltip to include whether or not you are included ([\#7367](https://github.com/matrix-org/matrix-react-sdk/pull/7367)). Fixes #17278.

## 🐛 Bug Fixes
 * Ensure group audio-only calls don't switch on the webcam on join ([\#20234](https://github.com/vector-im/element-web/pull/20234)). Fixes #20212.
 * Fix wrongly wrapping code blocks, breaking line numbers ([\#7507](https://github.com/matrix-org/matrix-react-sdk/pull/7507)). Fixes #20316.
 * Set header buttons to no phase when right panel is closed ([\#7506](https://github.com/matrix-org/matrix-react-sdk/pull/7506)).
 * Fix active Jitsi calls (and other active widgets) not being visible on screen, by showing them in PiP if they are not visible in any other container ([\#7435](https://github.com/matrix-org/matrix-react-sdk/pull/7435)). Fixes #15169 and #20275.
 * Fix layout of message bubble preview in settings ([\#7497](https://github.com/matrix-org/matrix-react-sdk/pull/7497)).
 * Prevent mutations of js-sdk owned objects as it breaks accountData ([\#7504](https://github.com/matrix-org/matrix-react-sdk/pull/7504)). Fixes matrix-org/element-web-rageshakes#7822.
 * fallback properly with pluralized strings ([\#7495](https://github.com/matrix-org/matrix-react-sdk/pull/7495)). Fixes #20455.
 * Consider continuations when resolving whether a tile is last in section ([\#7461](https://github.com/matrix-org/matrix-react-sdk/pull/7461)). Fixes #20368 and #20369.
 * Fix read receipts and sent indicators for bubble layout ([\#7460](https://github.com/matrix-org/matrix-react-sdk/pull/7460)). Fixes #18298 and #20345.
 * null-guard dataset mxTheme to prevent html exports from exploding ([\#7493](https://github.com/matrix-org/matrix-react-sdk/pull/7493)). Fixes #20453.
 * Fix avatar container overlapping give feedback cta ([\#7491](https://github.com/matrix-org/matrix-react-sdk/pull/7491)). Fixes matrix-org/element-web-rageshakes#7987.
 * Fix jump to bottom button working when on a permalink ([\#7494](https://github.com/matrix-org/matrix-react-sdk/pull/7494)). Fixes #19813.
 * Remove the Description from the location picker ([\#7485](https://github.com/matrix-org/matrix-react-sdk/pull/7485)).
 * Fix look of the untrusted device dialog ([\#7487](https://github.com/matrix-org/matrix-react-sdk/pull/7487)). Fixes #20447. Contributed by @SimonBrandner.
 * Hide maximise button in the sticker picker  ([\#7488](https://github.com/matrix-org/matrix-react-sdk/pull/7488)). Fixes #20443. Contributed by @SimonBrandner.
 * Fix space ordering to match newer spec ([\#7481](https://github.com/matrix-org/matrix-react-sdk/pull/7481)).
 * Fix typing notification colors ([\#7490](https://github.com/matrix-org/matrix-react-sdk/pull/7490)). Fixes #20144. Contributed by @SimonBrandner.
 * fix fallback for pluralized strings ([\#7480](https://github.com/matrix-org/matrix-react-sdk/pull/7480)). Fixes #20426.
 * Fix right panel soft crashes chat rooms ([\#7479](https://github.com/matrix-org/matrix-react-sdk/pull/7479)). Fixes #20433.
 * update yarn.lock and i18n ([\#7476](https://github.com/matrix-org/matrix-react-sdk/pull/7476)). Fixes #20426 and #20423.
 * Don't send typing notification when restoring composer draft ([\#7477](https://github.com/matrix-org/matrix-react-sdk/pull/7477)). Fixes #20424.
 * Fix room joining spinner being incorrect if you change room mid-join ([\#7473](https://github.com/matrix-org/matrix-react-sdk/pull/7473)).
 * Only return the approved widget capabilities instead of accepting all requested capabilities ([\#7454](https://github.com/matrix-org/matrix-react-sdk/pull/7454)). Contributed by @dhenneke.
 * Fix quoting messages from the search view ([\#7466](https://github.com/matrix-org/matrix-react-sdk/pull/7466)). Fixes #20353.
 * Attribute fallback i18n strings with lang attribute ([\#7323](https://github.com/matrix-org/matrix-react-sdk/pull/7323)).
 * Fix spotlight cmd-k wrongly expanding left panel ([\#7463](https://github.com/matrix-org/matrix-react-sdk/pull/7463)). Fixes #20399.
 * Fix room_id check when adding user widgets ([\#7448](https://github.com/matrix-org/matrix-react-sdk/pull/7448)). Fixes #19382. Contributed by @bink.
 * Add new line in settings label ([\#7451](https://github.com/matrix-org/matrix-react-sdk/pull/7451)). Fixes #20365.
 * Fix handling incoming redactions in EventIndex ([\#7443](https://github.com/matrix-org/matrix-react-sdk/pull/7443)). Fixes #19326.
 * Fix room alias address isn't checked for validity before being shown as added ([\#7107](https://github.com/matrix-org/matrix-react-sdk/pull/7107)). Fixes #19609. Contributed by @Palid.
 * Call view accessibility fixes ([\#7439](https://github.com/matrix-org/matrix-react-sdk/pull/7439)). Fixes #18516.
 * Fix offscreen canvas breaking with split-brained firefox support ([\#7440](https://github.com/matrix-org/matrix-react-sdk/pull/7440)).
 * Removed red shield in forwarding preview. ([\#7447](https://github.com/matrix-org/matrix-react-sdk/pull/7447)). Contributed by @ankur12-1610.
 * Wrap status message ([\#7325](https://github.com/matrix-org/matrix-react-sdk/pull/7325)). Fixes #20092. Contributed by @SimonBrandner.
 * Move hideSender logic into state so it causes re-render ([\#7413](https://github.com/matrix-org/matrix-react-sdk/pull/7413)). Fixes #18448.
 * Fix dialpad positioning ([\#7446](https://github.com/matrix-org/matrix-react-sdk/pull/7446)). Fixes #20175. Contributed by @SimonBrandner.
 * Hide non-functional list options on Suggested sublist ([\#7410](https://github.com/matrix-org/matrix-react-sdk/pull/7410)). Fixes #20252.
 * Fix width overflow in mini composer overflow menu ([\#7411](https://github.com/matrix-org/matrix-react-sdk/pull/7411)). Fixes #20263.
 * Fix being wrongly sent to Home space when creating/joining/leaving rooms ([\#7418](https://github.com/matrix-org/matrix-react-sdk/pull/7418)). Fixes matrix-org/element-web-rageshakes#7331 #20246 and #20240.
 * Fix HTML Export where the data-mx-theme is `Light` not `light` ([\#7415](https://github.com/matrix-org/matrix-react-sdk/pull/7415)).
 * Don't disable username/password fields whilst doing wk-lookup ([\#7438](https://github.com/matrix-org/matrix-react-sdk/pull/7438)). Fixes #20121.
 * Prevent keyboard propagation out of context menus ([\#7437](https://github.com/matrix-org/matrix-react-sdk/pull/7437)). Fixes #20317.
 * Fix nulls leaking into geo urls ([\#7433](https://github.com/matrix-org/matrix-react-sdk/pull/7433)).
 * Fix zIndex of peristent apps in miniMode ([\#7429](https://github.com/matrix-org/matrix-react-sdk/pull/7429)).
 * Space panel should watch spaces for space name changes ([\#7432](https://github.com/matrix-org/matrix-react-sdk/pull/7432)).
 * Fix list formatting alternating on edit ([\#7422](https://github.com/matrix-org/matrix-react-sdk/pull/7422)). Fixes #20073. Contributed by @renancleyson-dev.
 * Don't show `Testing small changes` without UIFeature.Feedback ([\#7427](https://github.com/matrix-org/matrix-react-sdk/pull/7427)). Fixes #20298.
 * Fix invisible toggle space panel button ([\#7426](https://github.com/matrix-org/matrix-react-sdk/pull/7426)). Fixes #20279.
 * Fix legacy breadcrumbs wrongly showing up ([\#7425](https://github.com/matrix-org/matrix-react-sdk/pull/7425)).
 * Space Panel use SettingsStore instead of SpaceStore as source of truth ([\#7404](https://github.com/matrix-org/matrix-react-sdk/pull/7404)). Fixes #20250.
 * Fix inline code block nowrap issue ([\#7406](https://github.com/matrix-org/matrix-react-sdk/pull/7406)).
 * Fix notification badge for All Rooms space ([\#7401](https://github.com/matrix-org/matrix-react-sdk/pull/7401)). Fixes #20229.
 * Show error if could not load space hierarchy ([\#7399](https://github.com/matrix-org/matrix-react-sdk/pull/7399)). Fixes #20221.
 * Increase gap between ELS and the subsequent event to prevent overlap ([\#7391](https://github.com/matrix-org/matrix-react-sdk/pull/7391)). Fixes #18319.
 * Fix list of members in space preview ([\#7356](https://github.com/matrix-org/matrix-react-sdk/pull/7356)). Fixes #19781.
 * Fix sizing of e2e shield in bubble layout ([\#7394](https://github.com/matrix-org/matrix-react-sdk/pull/7394)). Fixes #19090.
 * Fix bubble radius wrong when followed by a state event from same user ([\#7393](https://github.com/matrix-org/matrix-react-sdk/pull/7393)). Fixes #18982.
 * Fix alignment between ELS and Events in bubble layout ([\#7392](https://github.com/matrix-org/matrix-react-sdk/pull/7392)). Fixes #19652 and #19057.
 * Don't include the accuracy parameter in location events if accuracy could not be determined. ([\#7375](https://github.com/matrix-org/matrix-react-sdk/pull/7375)).
 * Make compact layout only apply to Modern layout ([\#7382](https://github.com/matrix-org/matrix-react-sdk/pull/7382)). Fixes #18412.
 * Pin qrcode to fix e2e verification bug ([\#7378](https://github.com/matrix-org/matrix-react-sdk/pull/7378)). Fixes #20188.
 * Add internationalisation to progress strings in room export dialog ([\#7385](https://github.com/matrix-org/matrix-react-sdk/pull/7385)). Fixes #20208.
 * Prevent escape to cancel edit from also scrolling to bottom ([\#7380](https://github.com/matrix-org/matrix-react-sdk/pull/7380)). Fixes #20182.
 * Fix narrow mode composer buttons for polls labs ([\#7386](https://github.com/matrix-org/matrix-react-sdk/pull/7386)). Fixes #20067.
 * Fix useUserStatusMessage exploding on unknown user ([\#7365](https://github.com/matrix-org/matrix-react-sdk/pull/7365)).
 * Fix room join spinner in room list header ([\#7364](https://github.com/matrix-org/matrix-react-sdk/pull/7364)). Fixes #20139.
 * Fix room search sometimes not opening spotlight ([\#7363](https://github.com/matrix-org/matrix-react-sdk/pull/7363)). Fixes matrix-org/element-web-rageshakes#7288.

Changes in [1.9.9-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.9.9-rc.1) (2022-01-11)
=======================================================================================================

## ✨ Features
 * Ship maximised widgets and remove feature flag ([\#7509](https://github.com/matrix-org/matrix-react-sdk/pull/7509)).
 * Properly maintain aspect ratio of inline images ([\#7503](https://github.com/matrix-org/matrix-react-sdk/pull/7503)).
 * Add zoom buttons to the location view ([\#7482](https://github.com/matrix-org/matrix-react-sdk/pull/7482)).
 * Remove bubble from around location events ([\#7459](https://github.com/matrix-org/matrix-react-sdk/pull/7459)). Fixes #20323.
 * Disable "Publish this room" option in invite only rooms ([\#7441](https://github.com/matrix-org/matrix-react-sdk/pull/7441)). Fixes #6596. Contributed by @aaronraimist.
 * Add permission dropdown for sending reactions ([\#7492](https://github.com/matrix-org/matrix-react-sdk/pull/7492)). Fixes #20450.
 * Give secret key field an `id` ([\#7489](https://github.com/matrix-org/matrix-react-sdk/pull/7489)). Fixes #20390. Contributed by @SimonBrandner.
 * Display a tooltip when you hover over a location ([\#7472](https://github.com/matrix-org/matrix-react-sdk/pull/7472)).
 * Open map in a dialog when it is clicked ([\#7465](https://github.com/matrix-org/matrix-react-sdk/pull/7465)).
 * a11y - wrap notification level radios in fieldsets ([\#7471](https://github.com/matrix-org/matrix-react-sdk/pull/7471)).
 * Wrap inputs in fieldsets in Space visibility settings ([\#7350](https://github.com/matrix-org/matrix-react-sdk/pull/7350)).
 * History based navigation with new right panel store ([\#7398](https://github.com/matrix-org/matrix-react-sdk/pull/7398)). Fixes #19686 #19660 and #19634.
 * Associate room alias warning with public option in settings ([\#7430](https://github.com/matrix-org/matrix-react-sdk/pull/7430)).
 * Disable quick reactions button when no permissions ([\#7412](https://github.com/matrix-org/matrix-react-sdk/pull/7412)). Fixes #20270.
 * Allow opening a map view in OpenStreetMap ([\#7428](https://github.com/matrix-org/matrix-react-sdk/pull/7428)).
 * Display the user's avatar when they shared their location ([\#7424](https://github.com/matrix-org/matrix-react-sdk/pull/7424)).
 * Remove the Forward and Share buttons for location messages only ([\#7423](https://github.com/matrix-org/matrix-react-sdk/pull/7423)).
 * Add configuration to disable relative date markers in timeline ([\#7405](https://github.com/matrix-org/matrix-react-sdk/pull/7405)).
 * Space preferences for whether or not you see DMs in a Space ([\#7250](https://github.com/matrix-org/matrix-react-sdk/pull/7250)). Fixes #19529 and #19955.
 * Have LocalEchoWrapper emit updates so the app can react faster ([\#7358](https://github.com/matrix-org/matrix-react-sdk/pull/7358)). Fixes #19749.
 * Use semantic heading on dialog component ([\#7383](https://github.com/matrix-org/matrix-react-sdk/pull/7383)).
 * Add `/jumptodate` slash command ([\#7372](https://github.com/matrix-org/matrix-react-sdk/pull/7372)). Fixes #7677.
 * Update room context menu copy ([\#7361](https://github.com/matrix-org/matrix-react-sdk/pull/7361)). Fixes #20133.
 * Use lazy rendering in the AddExistingToSpaceDialog ([\#7369](https://github.com/matrix-org/matrix-react-sdk/pull/7369)). Fixes #18784.
 * Tweak FacePile tooltip to include whether or not you are included ([\#7367](https://github.com/matrix-org/matrix-react-sdk/pull/7367)). Fixes #17278.

## 🐛 Bug Fixes
 * Ensure group audio-only calls don't switch on the webcam on join ([\#20234](https://github.com/vector-im/element-web/pull/20234)). Fixes #20212.
 * Fix wrongly wrapping code blocks, breaking line numbers ([\#7507](https://github.com/matrix-org/matrix-react-sdk/pull/7507)). Fixes #20316.
 * Set header buttons to no phase when right panel is closed ([\#7506](https://github.com/matrix-org/matrix-react-sdk/pull/7506)).
 * Fix active Jitsi calls (and other active widgets) not being visible on screen, by showing them in PiP if they are not visible in any other container ([\#7435](https://github.com/matrix-org/matrix-react-sdk/pull/7435)). Fixes #15169 and #20275.
 * Fix layout of message bubble preview in settings ([\#7497](https://github.com/matrix-org/matrix-react-sdk/pull/7497)).
 * Prevent mutations of js-sdk owned objects as it breaks accountData ([\#7504](https://github.com/matrix-org/matrix-react-sdk/pull/7504)). Fixes matrix-org/element-web-rageshakes#7822.
 * fallback properly with pluralized strings ([\#7495](https://github.com/matrix-org/matrix-react-sdk/pull/7495)). Fixes #20455.
 * Consider continuations when resolving whether a tile is last in section ([\#7461](https://github.com/matrix-org/matrix-react-sdk/pull/7461)). Fixes #20368 and #20369.
 * Fix read receipts and sent indicators for bubble layout ([\#7460](https://github.com/matrix-org/matrix-react-sdk/pull/7460)). Fixes #18298 and #20345.
 * null-guard dataset mxTheme to prevent html exports from exploding ([\#7493](https://github.com/matrix-org/matrix-react-sdk/pull/7493)). Fixes #20453.
 * Fix avatar container overlapping give feedback cta ([\#7491](https://github.com/matrix-org/matrix-react-sdk/pull/7491)). Fixes matrix-org/element-web-rageshakes#7987.
 * Fix jump to bottom button working when on a permalink ([\#7494](https://github.com/matrix-org/matrix-react-sdk/pull/7494)). Fixes #19813.
 * Remove the Description from the location picker ([\#7485](https://github.com/matrix-org/matrix-react-sdk/pull/7485)).
 * Fix look of the untrusted device dialog ([\#7487](https://github.com/matrix-org/matrix-react-sdk/pull/7487)). Fixes #20447. Contributed by @SimonBrandner.
 * Hide maximise button in the sticker picker  ([\#7488](https://github.com/matrix-org/matrix-react-sdk/pull/7488)). Fixes #20443. Contributed by @SimonBrandner.
 * Fix space ordering to match newer spec ([\#7481](https://github.com/matrix-org/matrix-react-sdk/pull/7481)).
 * Fix typing notification colors ([\#7490](https://github.com/matrix-org/matrix-react-sdk/pull/7490)). Fixes #20144. Contributed by @SimonBrandner.
 * fix fallback for pluralized strings ([\#7480](https://github.com/matrix-org/matrix-react-sdk/pull/7480)). Fixes #20426.
 * Fix right panel soft crashes chat rooms ([\#7479](https://github.com/matrix-org/matrix-react-sdk/pull/7479)). Fixes #20433.
 * update yarn.lock and i18n ([\#7476](https://github.com/matrix-org/matrix-react-sdk/pull/7476)). Fixes #20426 and #20423.
 * Don't send typing notification when restoring composer draft ([\#7477](https://github.com/matrix-org/matrix-react-sdk/pull/7477)). Fixes #20424.
 * Fix room joining spinner being incorrect if you change room mid-join ([\#7473](https://github.com/matrix-org/matrix-react-sdk/pull/7473)).
 * Only return the approved widget capabilities instead of accepting all requested capabilities ([\#7454](https://github.com/matrix-org/matrix-react-sdk/pull/7454)). Contributed by @dhenneke.
 * Fix quoting messages from the search view ([\#7466](https://github.com/matrix-org/matrix-react-sdk/pull/7466)). Fixes #20353.
 * Attribute fallback i18n strings with lang attribute ([\#7323](https://github.com/matrix-org/matrix-react-sdk/pull/7323)).
 * Fix spotlight cmd-k wrongly expanding left panel ([\#7463](https://github.com/matrix-org/matrix-react-sdk/pull/7463)). Fixes #20399.
 * Fix room_id check when adding user widgets ([\#7448](https://github.com/matrix-org/matrix-react-sdk/pull/7448)). Fixes #19382. Contributed by @bink.
 * Add new line in settings label ([\#7451](https://github.com/matrix-org/matrix-react-sdk/pull/7451)). Fixes #20365.
 * Fix handling incoming redactions in EventIndex ([\#7443](https://github.com/matrix-org/matrix-react-sdk/pull/7443)). Fixes #19326.
 * Fix room alias address isn't checked for validity before being shown as added ([\#7107](https://github.com/matrix-org/matrix-react-sdk/pull/7107)). Fixes #19609. Contributed by @Palid.
 * Call view accessibility fixes ([\#7439](https://github.com/matrix-org/matrix-react-sdk/pull/7439)). Fixes #18516.
 * Fix offscreen canvas breaking with split-brained firefox support ([\#7440](https://github.com/matrix-org/matrix-react-sdk/pull/7440)).
 * Removed red shield in forwarding preview. ([\#7447](https://github.com/matrix-org/matrix-react-sdk/pull/7447)). Contributed by @ankur12-1610.
 * Wrap status message ([\#7325](https://github.com/matrix-org/matrix-react-sdk/pull/7325)). Fixes #20092. Contributed by @SimonBrandner.
 * Move hideSender logic into state so it causes re-render ([\#7413](https://github.com/matrix-org/matrix-react-sdk/pull/7413)). Fixes #18448.
 * Fix dialpad positioning ([\#7446](https://github.com/matrix-org/matrix-react-sdk/pull/7446)). Fixes #20175. Contributed by @SimonBrandner.
 * Hide non-functional list options on Suggested sublist ([\#7410](https://github.com/matrix-org/matrix-react-sdk/pull/7410)). Fixes #20252.
 * Fix width overflow in mini composer overflow menu ([\#7411](https://github.com/matrix-org/matrix-react-sdk/pull/7411)). Fixes #20263.
 * Fix being wrongly sent to Home space when creating/joining/leaving rooms ([\#7418](https://github.com/matrix-org/matrix-react-sdk/pull/7418)). Fixes matrix-org/element-web-rageshakes#7331 #20246 and #20240.
 * Fix HTML Export where the data-mx-theme is `Light` not `light` ([\#7415](https://github.com/matrix-org/matrix-react-sdk/pull/7415)).
 * Don't disable username/password fields whilst doing wk-lookup ([\#7438](https://github.com/matrix-org/matrix-react-sdk/pull/7438)). Fixes #20121.
 * Prevent keyboard propagation out of context menus ([\#7437](https://github.com/matrix-org/matrix-react-sdk/pull/7437)). Fixes #20317.
 * Fix nulls leaking into geo urls ([\#7433](https://github.com/matrix-org/matrix-react-sdk/pull/7433)).
 * Fix zIndex of peristent apps in miniMode ([\#7429](https://github.com/matrix-org/matrix-react-sdk/pull/7429)).
 * Space panel should watch spaces for space name changes ([\#7432](https://github.com/matrix-org/matrix-react-sdk/pull/7432)).
 * Fix list formatting alternating on edit ([\#7422](https://github.com/matrix-org/matrix-react-sdk/pull/7422)). Fixes #20073. Contributed by @renancleyson-dev.
 * Don't show `Testing small changes` without UIFeature.Feedback ([\#7427](https://github.com/matrix-org/matrix-react-sdk/pull/7427)). Fixes #20298.
 * Fix invisible toggle space panel button ([\#7426](https://github.com/matrix-org/matrix-react-sdk/pull/7426)). Fixes #20279.
 * Fix legacy breadcrumbs wrongly showing up ([\#7425](https://github.com/matrix-org/matrix-react-sdk/pull/7425)).
 * Space Panel use SettingsStore instead of SpaceStore as source of truth ([\#7404](https://github.com/matrix-org/matrix-react-sdk/pull/7404)). Fixes #20250.
 * Fix inline code block nowrap issue ([\#7406](https://github.com/matrix-org/matrix-react-sdk/pull/7406)).
 * Fix notification badge for All Rooms space ([\#7401](https://github.com/matrix-org/matrix-react-sdk/pull/7401)). Fixes #20229.
 * Show error if could not load space hierarchy ([\#7399](https://github.com/matrix-org/matrix-react-sdk/pull/7399)). Fixes #20221.
 * Increase gap between ELS and the subsequent event to prevent overlap ([\#7391](https://github.com/matrix-org/matrix-react-sdk/pull/7391)). Fixes #18319.
 * Fix list of members in space preview ([\#7356](https://github.com/matrix-org/matrix-react-sdk/pull/7356)). Fixes #19781.
 * Fix sizing of e2e shield in bubble layout ([\#7394](https://github.com/matrix-org/matrix-react-sdk/pull/7394)). Fixes #19090.
 * Fix bubble radius wrong when followed by a state event from same user ([\#7393](https://github.com/matrix-org/matrix-react-sdk/pull/7393)). Fixes #18982.
 * Fix alignment between ELS and Events in bubble layout ([\#7392](https://github.com/matrix-org/matrix-react-sdk/pull/7392)). Fixes #19652 and #19057.
 * Don't include the accuracy parameter in location events if accuracy could not be determined. ([\#7375](https://github.com/matrix-org/matrix-react-sdk/pull/7375)).
 * Make compact layout only apply to Modern layout ([\#7382](https://github.com/matrix-org/matrix-react-sdk/pull/7382)). Fixes #18412.
 * Pin qrcode to fix e2e verification bug ([\#7378](https://github.com/matrix-org/matrix-react-sdk/pull/7378)). Fixes #20188.
 * Add internationalisation to progress strings in room export dialog ([\#7385](https://github.com/matrix-org/matrix-react-sdk/pull/7385)). Fixes #20208.
 * Prevent escape to cancel edit from also scrolling to bottom ([\#7380](https://github.com/matrix-org/matrix-react-sdk/pull/7380)). Fixes #20182.
 * Fix narrow mode composer buttons for polls labs ([\#7386](https://github.com/matrix-org/matrix-react-sdk/pull/7386)). Fixes #20067.
 * Fix useUserStatusMessage exploding on unknown user ([\#7365](https://github.com/matrix-org/matrix-react-sdk/pull/7365)).
 * Fix room join spinner in room list header ([\#7364](https://github.com/matrix-org/matrix-react-sdk/pull/7364)). Fixes #20139.
 * Fix room search sometimes not opening spotlight ([\#7363](https://github.com/matrix-org/matrix-react-sdk/pull/7363)). Fixes matrix-org/element-web-rageshakes#7288.

Changes in [1.9.8](https://github.com/vector-im/element-web/releases/tag/v1.9.8) (2021-12-20)
=============================================================================================

## ✨ Features
 * Include Vietnamese language ([\#20029](https://github.com/vector-im/element-web/pull/20029)).
 * Simple static location sharing ([\#19754](https://github.com/vector-im/element-web/pull/19754)).
 * Add support for the Indonesian language ([\#20032](https://github.com/vector-im/element-web/pull/20032)). Fixes #20030. Contributed by @Linerly.
 * Always unhide widgets on layout change (pinning a widget) ([\#7299](https://github.com/matrix-org/matrix-react-sdk/pull/7299)).
 * Update status message in the member list and user info panel when it is changed ([\#7338](https://github.com/matrix-org/matrix-react-sdk/pull/7338)). Fixes #20127. Contributed by @SimonBrandner.
 * Iterate space panel toggle collapse interaction ([\#7335](https://github.com/matrix-org/matrix-react-sdk/pull/7335)). Fixes #20079.
 * Spotlight search labs ([\#7116](https://github.com/matrix-org/matrix-react-sdk/pull/7116)). Fixes #19530.
 * Put room settings form elements in fieldsets ([\#7311](https://github.com/matrix-org/matrix-react-sdk/pull/7311)).
 * Add descriptions to ambiguous links for screen readers ([\#7310](https://github.com/matrix-org/matrix-react-sdk/pull/7310)).
 * Make tooltips keyboard accessible ([\#7281](https://github.com/matrix-org/matrix-react-sdk/pull/7281)).
 * Iterate room context menus for DMs ([\#7308](https://github.com/matrix-org/matrix-react-sdk/pull/7308)). Fixes #19527.
 * Update space panel expand mechanism ([\#7230](https://github.com/matrix-org/matrix-react-sdk/pull/7230)). Fixes #17993.
 * Add CSS variable to make the UI gaps consistent and fix the resize handle position ([\#7234](https://github.com/matrix-org/matrix-react-sdk/pull/7234)). Fixes #19904 and #19938.
 * Custom location sharing. ([\#7185](https://github.com/matrix-org/matrix-react-sdk/pull/7185)).
 * Simple static location sharing ([\#7135](https://github.com/matrix-org/matrix-react-sdk/pull/7135)).
 * Finish sending pending messages before leaving room ([\#7276](https://github.com/matrix-org/matrix-react-sdk/pull/7276)). Fixes #4702.
 * Dropdown follow wai-aria practices for expanding on arrow keys ([\#7277](https://github.com/matrix-org/matrix-react-sdk/pull/7277)). Fixes #3687.
 * Expose PL control for pinned events when lab enabled ([\#7278](https://github.com/matrix-org/matrix-react-sdk/pull/7278)). Fixes #5396.
 * In People & Favourites metaspaces always show all rooms ([\#7288](https://github.com/matrix-org/matrix-react-sdk/pull/7288)). Fixes #20048.
 * Don't allow calls when the connection the server has been lost ([\#7287](https://github.com/matrix-org/matrix-react-sdk/pull/7287)). Fixes #2096. Contributed by @SimonBrandner.
 * Analytics opt in for posthog ([\#6936](https://github.com/matrix-org/matrix-react-sdk/pull/6936)).
 * Don't inhibit current room notifications if user has Modal open ([\#7274](https://github.com/matrix-org/matrix-react-sdk/pull/7274)). Fixes #1118.
 * Remove the `Screen sharing is here!` dialog ([\#7266](https://github.com/matrix-org/matrix-react-sdk/pull/7266)). Fixes #18824. Contributed by @SimonBrandner.
 * Make composer buttons react to settings without having to change room ([\#7264](https://github.com/matrix-org/matrix-react-sdk/pull/7264)). Fixes #20011.
 * Decorate view keyboard shortcuts link as a link ([\#7260](https://github.com/matrix-org/matrix-react-sdk/pull/7260)). Fixes #20007.
 * Improve ease of focusing on Room list Search ([\#7255](https://github.com/matrix-org/matrix-react-sdk/pull/7255)). Fixes matrix-org/element-web-rageshakes#7017.
 * Autofocus device panel entry when renaming device ([\#7249](https://github.com/matrix-org/matrix-react-sdk/pull/7249)). Fixes #19984.
 * Update Space Panel scrollable region ([\#7245](https://github.com/matrix-org/matrix-react-sdk/pull/7245)). Fixes #19978.
 * Replace breadcrumbs with recently viewed menu ([\#7073](https://github.com/matrix-org/matrix-react-sdk/pull/7073)). Fixes #19528.
 * Tweaks to informational architecture 1.1 ([\#7052](https://github.com/matrix-org/matrix-react-sdk/pull/7052)). Fixes #19526, #19379, #17792, #16450, #19881, #19892, #19300, #19324, #17307, #17468 #19932 and #19956.

## 🐛 Bug Fixes
 * [Release] Fix inline code block nowrap issue ([\#7407](https://github.com/matrix-org/matrix-react-sdk/pull/7407)).
 * don't collapse spaces in inline code blocks (https ([\#7328](https://github.com/matrix-org/matrix-react-sdk/pull/7328)). Fixes #6051. Contributed by @HarHarLinks.
 * Fix accessibility regressions ([\#7336](https://github.com/matrix-org/matrix-react-sdk/pull/7336)).
 * Debounce User Info start dm "Message" button ([\#7357](https://github.com/matrix-org/matrix-react-sdk/pull/7357)). Fixes #7763.
 * Fix thread filter being cut-off on narrow screens ([\#7354](https://github.com/matrix-org/matrix-react-sdk/pull/7354)). Fixes #20146.
 * Fix upgraded rooms wrongly showing up in spotlight ([\#7341](https://github.com/matrix-org/matrix-react-sdk/pull/7341)). Fixes #20141.
 * Show votes in replied-to polls (pass in getRelationsForEvent) ([\#7345](https://github.com/matrix-org/matrix-react-sdk/pull/7345)). Fixes #20153.
 * Keep all previously approved widget capabilities when requesting new capabilities ([\#7340](https://github.com/matrix-org/matrix-react-sdk/pull/7340)). Contributed by @dhenneke.
 * Only show poll previews when the polls feature is enabled ([\#7331](https://github.com/matrix-org/matrix-react-sdk/pull/7331)).
 * No-op action:join if the user is already invited for scalar ([\#7334](https://github.com/matrix-org/matrix-react-sdk/pull/7334)). Fixes #20134.
 * Don't show polls in timeline if polls are disabled ([\#7332](https://github.com/matrix-org/matrix-react-sdk/pull/7332)). Fixes #20130.
 * Don't send a poll response event if you are voting for your current c… ([\#7326](https://github.com/matrix-org/matrix-react-sdk/pull/7326)). Fixes #20129.
 * Don't show options button when the user can't modify widgets ([\#7324](https://github.com/matrix-org/matrix-react-sdk/pull/7324)). Fixes #20114. Contributed by @SimonBrandner.
 * Add vertical spacing between buttons when they go over multiple lines ([\#7314](https://github.com/matrix-org/matrix-react-sdk/pull/7314)). Contributed by @twigleingrid.
 * Improve accessibility of opening space create menu ([\#7316](https://github.com/matrix-org/matrix-react-sdk/pull/7316)).
 * Correct tab order in room preview dialog ([\#7302](https://github.com/matrix-org/matrix-react-sdk/pull/7302)).
 * Fix favourites and people metaspaces not rendering their content ([\#7315](https://github.com/matrix-org/matrix-react-sdk/pull/7315)). Fixes #20070.
 * Make clear button images visible in high contrast theme ([\#7306](https://github.com/matrix-org/matrix-react-sdk/pull/7306)). Fixes #19931.
 * Fix html exporting and improve output size ([\#7312](https://github.com/matrix-org/matrix-react-sdk/pull/7312)). Fixes #19436 #20107 and #19441.
 * Fix textual message stripping new line ([\#7239](https://github.com/matrix-org/matrix-react-sdk/pull/7239)). Fixes #15320. Contributed by @renancleyson-dev.
 * Fix issue with room list resizer getting clipped in firefox ([\#7303](https://github.com/matrix-org/matrix-react-sdk/pull/7303)). Fixes #20076.
 * Fix wrong indentation with nested ordered list unnesting list on edit ([\#7300](https://github.com/matrix-org/matrix-react-sdk/pull/7300)). Contributed by @renancleyson-dev.
 * Fix input field behaviour inside context menus ([\#7293](https://github.com/matrix-org/matrix-react-sdk/pull/7293)). Fixes #19881.
 * Corrected the alignment of the Edit button on LoginPage. ([\#7292](https://github.com/matrix-org/matrix-react-sdk/pull/7292)). Contributed by @ankur12-1610.
 * Allow sharing manual location without giving location permission ([\#7295](https://github.com/matrix-org/matrix-react-sdk/pull/7295)). Fixes #20065. Contributed by @tulir.
 * Make emoji picker search placeholder localizable ([\#7294](https://github.com/matrix-org/matrix-react-sdk/pull/7294)).
 * Fix jump to bottom on message send ([\#7280](https://github.com/matrix-org/matrix-react-sdk/pull/7280)). Fixes #19859. Contributed by @SimonBrandner.
 * Fix: Warning: Unsupported style property pointer-events. Did you mean pointerEvents? ([\#7291](https://github.com/matrix-org/matrix-react-sdk/pull/7291)).
 * Add edits and replies to the right panel timeline & prepare the timelineCard to share code with threads ([\#7262](https://github.com/matrix-org/matrix-react-sdk/pull/7262)). Fixes #20012 and #19928.
 * Fix labs exploding when lab group is empty ([\#7290](https://github.com/matrix-org/matrix-react-sdk/pull/7290)). Fixes #20051.
 * Update URL when room aliases are modified ([\#7289](https://github.com/matrix-org/matrix-react-sdk/pull/7289)). Fixes #1616 and #1925.
 * Render mini user menu for when space panel is disabled ([\#7258](https://github.com/matrix-org/matrix-react-sdk/pull/7258)). Fixes #19998.
 * When accepting DM from People metaspace don't switch to Home ([\#7272](https://github.com/matrix-org/matrix-react-sdk/pull/7272)). Fixes #19995.
 * Fix CallPreview `room is null` ([\#7265](https://github.com/matrix-org/matrix-react-sdk/pull/7265)). Fixes #19990, #19972, matrix-org/element-web-rageshakes#7004 matrix-org/element-web-rageshakes#6991 and matrix-org/element-web-rageshakes#6964.
 * Fixes more instances of double-translation ([\#7259](https://github.com/matrix-org/matrix-react-sdk/pull/7259)). Fixes #20010.
 * Fix video calls ([\#7256](https://github.com/matrix-org/matrix-react-sdk/pull/7256)). Fixes #20008. Contributed by @SimonBrandner.
 * Fix broken i18n in Forgot & Change password ([\#7252](https://github.com/matrix-org/matrix-react-sdk/pull/7252)). Fixes #19989.
 * Fix setBotPower to not use `.content` ([\#7179](https://github.com/matrix-org/matrix-react-sdk/pull/7179)). Fixes #19845.
 * Break long words in pinned messages to prevent overflow ([\#7251](https://github.com/matrix-org/matrix-react-sdk/pull/7251)). Fixes #19985.
 * Disallow sending empty feedbacks ([\#7240](https://github.com/matrix-org/matrix-react-sdk/pull/7240)).
 * Fix wrongly sized default sub-space icons in space panel ([\#7243](https://github.com/matrix-org/matrix-react-sdk/pull/7243)). Fixes #19973.
 * Hide clear cache and reload button if crash is before client init ([\#7242](https://github.com/matrix-org/matrix-react-sdk/pull/7242)). Fixes matrix-org/element-web-rageshakes#6996.
 * Fix automatic space switching wrongly going via Home for room aliases ([\#7247](https://github.com/matrix-org/matrix-react-sdk/pull/7247)). Fixes #19974.
 * Fix links being parsed as markdown links improperly ([\#7200](https://github.com/matrix-org/matrix-react-sdk/pull/7200)). Contributed by @Palid.

Changes in [1.9.8-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.9.8-rc.1) (2021-12-14)
=======================================================================================================

## ✨ Features
 * Include Vietnamese language ([\#20029](https://github.com/vector-im/element-web/pull/20029)).
 * Simple static location sharing ([\#19754](https://github.com/vector-im/element-web/pull/19754)).
 * Add support for the Indonesian language ([\#20032](https://github.com/vector-im/element-web/pull/20032)). Fixes #20030. Contributed by @Linerly.
 * Always unhide widgets on layout change (pinning a widget) ([\#7299](https://github.com/matrix-org/matrix-react-sdk/pull/7299)).
 * Update status message in the member list and user info panel when it is changed ([\#7338](https://github.com/matrix-org/matrix-react-sdk/pull/7338)). Fixes #20127. Contributed by @SimonBrandner.
 * Iterate space panel toggle collapse interaction ([\#7335](https://github.com/matrix-org/matrix-react-sdk/pull/7335)). Fixes #20079.
 * Spotlight search labs ([\#7116](https://github.com/matrix-org/matrix-react-sdk/pull/7116)). Fixes #19530.
 * Put room settings form elements in fieldsets ([\#7311](https://github.com/matrix-org/matrix-react-sdk/pull/7311)).
 * Add descriptions to ambiguous links for screen readers ([\#7310](https://github.com/matrix-org/matrix-react-sdk/pull/7310)).
 * Make tooltips keyboard accessible ([\#7281](https://github.com/matrix-org/matrix-react-sdk/pull/7281)).
 * Iterate room context menus for DMs ([\#7308](https://github.com/matrix-org/matrix-react-sdk/pull/7308)). Fixes #19527.
 * Update space panel expand mechanism ([\#7230](https://github.com/matrix-org/matrix-react-sdk/pull/7230)). Fixes #17993.
 * Add CSS variable to make the UI gaps consistent and fix the resize handle position ([\#7234](https://github.com/matrix-org/matrix-react-sdk/pull/7234)). Fixes #19904 and #19938.
 * Custom location sharing. ([\#7185](https://github.com/matrix-org/matrix-react-sdk/pull/7185)).
 * Simple static location sharing ([\#7135](https://github.com/matrix-org/matrix-react-sdk/pull/7135)).
 * Finish sending pending messages before leaving room ([\#7276](https://github.com/matrix-org/matrix-react-sdk/pull/7276)). Fixes #4702.
 * Dropdown follow wai-aria practices for expanding on arrow keys ([\#7277](https://github.com/matrix-org/matrix-react-sdk/pull/7277)). Fixes #3687.
 * Expose PL control for pinned events when lab enabled ([\#7278](https://github.com/matrix-org/matrix-react-sdk/pull/7278)). Fixes #5396.
 * In People & Favourites metaspaces always show all rooms ([\#7288](https://github.com/matrix-org/matrix-react-sdk/pull/7288)). Fixes #20048.
 * Don't allow calls when the connection the server has been lost ([\#7287](https://github.com/matrix-org/matrix-react-sdk/pull/7287)). Fixes #2096. Contributed by @SimonBrandner.
 * Analytics opt in for posthog ([\#6936](https://github.com/matrix-org/matrix-react-sdk/pull/6936)).
 * Don't inhibit current room notifications if user has Modal open ([\#7274](https://github.com/matrix-org/matrix-react-sdk/pull/7274)). Fixes #1118.
 * Remove the `Screen sharing is here!` dialog ([\#7266](https://github.com/matrix-org/matrix-react-sdk/pull/7266)). Fixes #18824. Contributed by @SimonBrandner.
 * Make composer buttons react to settings without having to change room ([\#7264](https://github.com/matrix-org/matrix-react-sdk/pull/7264)). Fixes #20011.
 * Decorate view keyboard shortcuts link as a link ([\#7260](https://github.com/matrix-org/matrix-react-sdk/pull/7260)). Fixes #20007.
 * Improve ease of focusing on Room list Search ([\#7255](https://github.com/matrix-org/matrix-react-sdk/pull/7255)). Fixes matrix-org/element-web-rageshakes#7017.
 * Autofocus device panel entry when renaming device ([\#7249](https://github.com/matrix-org/matrix-react-sdk/pull/7249)). Fixes #19984.
 * Update Space Panel scrollable region ([\#7245](https://github.com/matrix-org/matrix-react-sdk/pull/7245)). Fixes #19978.
 * Replace breadcrumbs with recently viewed menu ([\#7073](https://github.com/matrix-org/matrix-react-sdk/pull/7073)). Fixes #19528.
 * Tweaks to informational architecture 1.1 ([\#7052](https://github.com/matrix-org/matrix-react-sdk/pull/7052)). Fixes #19526, #19379, #17792, #16450, #19881, #19892, #19300, #19324, #17307, #17468 #19932 and #19956.

## 🐛 Bug Fixes
 * Fix accessibility regressions ([\#7336](https://github.com/matrix-org/matrix-react-sdk/pull/7336)).
 * Debounce User Info start dm "Message" button ([\#7357](https://github.com/matrix-org/matrix-react-sdk/pull/7357)). Fixes #7763.
 * Fix thread filter being cut-off on narrow screens ([\#7354](https://github.com/matrix-org/matrix-react-sdk/pull/7354)). Fixes #20146.
 * Fix upgraded rooms wrongly showing up in spotlight ([\#7341](https://github.com/matrix-org/matrix-react-sdk/pull/7341)). Fixes #20141.
 * Show votes in replied-to polls (pass in getRelationsForEvent) ([\#7345](https://github.com/matrix-org/matrix-react-sdk/pull/7345)). Fixes #20153.
 * Keep all previously approved widget capabilities when requesting new capabilities ([\#7340](https://github.com/matrix-org/matrix-react-sdk/pull/7340)). Contributed by @dhenneke.
 * Only show poll previews when the polls feature is enabled ([\#7331](https://github.com/matrix-org/matrix-react-sdk/pull/7331)).
 * don't collapse spaces in inline code blocks (https ([\#7328](https://github.com/matrix-org/matrix-react-sdk/pull/7328)). Fixes #6051. Contributed by @HarHarLinks.
 * No-op action:join if the user is already invited for scalar ([\#7334](https://github.com/matrix-org/matrix-react-sdk/pull/7334)). Fixes #20134.
 * Don't show polls in timeline if polls are disabled ([\#7332](https://github.com/matrix-org/matrix-react-sdk/pull/7332)). Fixes #20130.
 * Don't send a poll response event if you are voting for your current c… ([\#7326](https://github.com/matrix-org/matrix-react-sdk/pull/7326)). Fixes #20129.
 * Don't show options button when the user can't modify widgets ([\#7324](https://github.com/matrix-org/matrix-react-sdk/pull/7324)). Fixes #20114. Contributed by @SimonBrandner.
 * Add vertical spacing between buttons when they go over multiple lines ([\#7314](https://github.com/matrix-org/matrix-react-sdk/pull/7314)). Contributed by @twigleingrid.
 * Improve accessibility of opening space create menu ([\#7316](https://github.com/matrix-org/matrix-react-sdk/pull/7316)).
 * Correct tab order in room preview dialog ([\#7302](https://github.com/matrix-org/matrix-react-sdk/pull/7302)).
 * Fix favourites and people metaspaces not rendering their content ([\#7315](https://github.com/matrix-org/matrix-react-sdk/pull/7315)). Fixes #20070.
 * Make clear button images visible in high contrast theme ([\#7306](https://github.com/matrix-org/matrix-react-sdk/pull/7306)). Fixes #19931.
 * Fix html exporting and improve output size ([\#7312](https://github.com/matrix-org/matrix-react-sdk/pull/7312)). Fixes #19436 #20107 and #19441.
 * Fix textual message stripping new line ([\#7239](https://github.com/matrix-org/matrix-react-sdk/pull/7239)). Fixes #15320. Contributed by @renancleyson-dev.
 * Fix issue with room list resizer getting clipped in firefox ([\#7303](https://github.com/matrix-org/matrix-react-sdk/pull/7303)). Fixes #20076.
 * Fix wrong indentation with nested ordered list unnesting list on edit ([\#7300](https://github.com/matrix-org/matrix-react-sdk/pull/7300)). Contributed by @renancleyson-dev.
 * Fix input field behaviour inside context menus ([\#7293](https://github.com/matrix-org/matrix-react-sdk/pull/7293)). Fixes #19881.
 * Corrected the alignment of the Edit button on LoginPage. ([\#7292](https://github.com/matrix-org/matrix-react-sdk/pull/7292)). Contributed by @ankur12-1610.
 * Allow sharing manual location without giving location permission ([\#7295](https://github.com/matrix-org/matrix-react-sdk/pull/7295)). Fixes #20065. Contributed by @tulir.
 * Make emoji picker search placeholder localizable ([\#7294](https://github.com/matrix-org/matrix-react-sdk/pull/7294)).
 * Fix jump to bottom on message send ([\#7280](https://github.com/matrix-org/matrix-react-sdk/pull/7280)). Fixes #19859. Contributed by @SimonBrandner.
 * Fix: Warning: Unsupported style property pointer-events. Did you mean pointerEvents? ([\#7291](https://github.com/matrix-org/matrix-react-sdk/pull/7291)).
 * Add edits and replies to the right panel timeline & prepare the timelineCard to share code with threads ([\#7262](https://github.com/matrix-org/matrix-react-sdk/pull/7262)). Fixes #20012 and #19928.
 * Fix labs exploding when lab group is empty ([\#7290](https://github.com/matrix-org/matrix-react-sdk/pull/7290)). Fixes #20051.
 * Update URL when room aliases are modified ([\#7289](https://github.com/matrix-org/matrix-react-sdk/pull/7289)). Fixes #1616 and #1925.
 * Render mini user menu for when space panel is disabled ([\#7258](https://github.com/matrix-org/matrix-react-sdk/pull/7258)). Fixes #19998.
 * When accepting DM from People metaspace don't switch to Home ([\#7272](https://github.com/matrix-org/matrix-react-sdk/pull/7272)). Fixes #19995.
 * Fix CallPreview `room is null` ([\#7265](https://github.com/matrix-org/matrix-react-sdk/pull/7265)). Fixes #19990, #19972, matrix-org/element-web-rageshakes#7004 matrix-org/element-web-rageshakes#6991 and matrix-org/element-web-rageshakes#6964.
 * Fixes more instances of double-translation ([\#7259](https://github.com/matrix-org/matrix-react-sdk/pull/7259)). Fixes #20010.
 * Fix video calls ([\#7256](https://github.com/matrix-org/matrix-react-sdk/pull/7256)). Fixes #20008. Contributed by @SimonBrandner.
 * Fix broken i18n in Forgot & Change password ([\#7252](https://github.com/matrix-org/matrix-react-sdk/pull/7252)). Fixes #19989.
 * Fix setBotPower to not use `.content` ([\#7179](https://github.com/matrix-org/matrix-react-sdk/pull/7179)). Fixes #19845.
 * Break long words in pinned messages to prevent overflow ([\#7251](https://github.com/matrix-org/matrix-react-sdk/pull/7251)). Fixes #19985.
 * Disallow sending empty feedbacks ([\#7240](https://github.com/matrix-org/matrix-react-sdk/pull/7240)).
 * Fix wrongly sized default sub-space icons in space panel ([\#7243](https://github.com/matrix-org/matrix-react-sdk/pull/7243)). Fixes #19973.
 * Hide clear cache and reload button if crash is before client init ([\#7242](https://github.com/matrix-org/matrix-react-sdk/pull/7242)). Fixes matrix-org/element-web-rageshakes#6996.
 * Fix automatic space switching wrongly going via Home for room aliases ([\#7247](https://github.com/matrix-org/matrix-react-sdk/pull/7247)). Fixes #19974.
 * Fix links being parsed as markdown links improperly ([\#7200](https://github.com/matrix-org/matrix-react-sdk/pull/7200)). Contributed by @Palid.

Changes in [1.9.7](https://github.com/vector-im/element-web/releases/tag/v1.9.7) (2021-12-13)
=============================================================================================

 * Security release with updated version of Olm to fix https://matrix.org/blog/2021/12/03/pre-disclosure-upcoming-security-release-of-libolm-and-matrix-js-sdk
 * Fix a crash on logout

Changes in [1.9.6](https://github.com/vector-im/element-web/releases/tag/v1.9.6) (2021-12-06)
=============================================================================================

## ✨ Features
 * Add unread indicator to the timelineCard header icon ([\#7156](https://github.com/matrix-org/matrix-react-sdk/pull/7156)). Fixes #19635.
 * Only show core navigation elements (call/chat/notification/info) when a widget is maximised ([\#7114](https://github.com/matrix-org/matrix-react-sdk/pull/7114)). Fixes #19632.
 * Improve ThreadPanel ctx menu accessibility ([\#7217](https://github.com/matrix-org/matrix-react-sdk/pull/7217)). Fixes #19885.
 * Allow filtering room list during treeview navigation ([\#7219](https://github.com/matrix-org/matrix-react-sdk/pull/7219)). Fixes #14702.
 * Add right panel chat timeline ([\#7112](https://github.com/matrix-org/matrix-react-sdk/pull/7112)). Fixes #19633.
 * Hide server options hint when disable_custom_urls is true ([\#7215](https://github.com/matrix-org/matrix-react-sdk/pull/7215)). Fixes #19919.
 * Improve right panel resize handle usability ([\#7204](https://github.com/matrix-org/matrix-react-sdk/pull/7204)). Fixes #15145. Contributed by @weeman1337.
 * Spaces quick settings ([\#7196](https://github.com/matrix-org/matrix-react-sdk/pull/7196)).
 * Maximised widgets always force a call to be shown in PIP mode ([\#7163](https://github.com/matrix-org/matrix-react-sdk/pull/7163)). Fixes #19637.
 * Group Labs flags ([\#7190](https://github.com/matrix-org/matrix-react-sdk/pull/7190)).
 * Show room context details in forward dialog ([\#7162](https://github.com/matrix-org/matrix-react-sdk/pull/7162)). Fixes #19793.
 * Remove chevrons from RoomSummaryCard_Button ([\#7137](https://github.com/matrix-org/matrix-react-sdk/pull/7137)). Fixes #19644.
 * Disable op/deop commands where user has no permissions ([\#7161](https://github.com/matrix-org/matrix-react-sdk/pull/7161)). Fixes #15390.
 * Add option to change the size of images/videos in the timeline ([\#7017](https://github.com/matrix-org/matrix-react-sdk/pull/7017)). Fixes vector-im/element-meta#49 #1520 and #19498.

## 🐛 Bug Fixes
 * Fix left panel glow in Safari ([\#7236](https://github.com/matrix-org/matrix-react-sdk/pull/7236)). Fixes #19863.
 * Fix newline on edit messages with quotes ([\#7227](https://github.com/matrix-org/matrix-react-sdk/pull/7227)). Fixes #12535. Contributed by @renancleyson-dev.
 * Guard against null refs in findSiblingElement ([\#7228](https://github.com/matrix-org/matrix-react-sdk/pull/7228)).
 * Tweak bottom of space panel buttons in expanded state ([\#7213](https://github.com/matrix-org/matrix-react-sdk/pull/7213)). Fixes #19921.
 * Fix multiline paragraph rendering as single line ([\#7210](https://github.com/matrix-org/matrix-react-sdk/pull/7210)). Fixes #8786. Contributed by @renancleyson-dev.
 * Improve room list message previews ([\#7224](https://github.com/matrix-org/matrix-react-sdk/pull/7224)). Fixes #17101 and #16169.
 * Fix EmojiPicker lazy loaded rendering bug ([\#7225](https://github.com/matrix-org/matrix-react-sdk/pull/7225)). Fixes #15341.
 * Prevent default avatar in UserInfo having pointer cursor ([\#7218](https://github.com/matrix-org/matrix-react-sdk/pull/7218)). Fixes #13872.
 * Prevent duplicate avatars in Event List Summaries ([\#7222](https://github.com/matrix-org/matrix-react-sdk/pull/7222)). Fixes #17706.
 * Respect the home page as a context for the Home space ([\#7216](https://github.com/matrix-org/matrix-react-sdk/pull/7216)). Fixes #19554.
 * Fix RoomUpgradeWarningBar exploding ([\#7214](https://github.com/matrix-org/matrix-react-sdk/pull/7214)). Fixes #19920.
 * Polish threads misalignments and UI diversion ([\#7209](https://github.com/matrix-org/matrix-react-sdk/pull/7209)). Fixes #19772, #19710 #19629 and #19711.
 * Fix Manage Restricted Join Rule Dialog for Spaces ([\#7208](https://github.com/matrix-org/matrix-react-sdk/pull/7208)). Fixes #19610.
 * Fix wrongly showing unpin in pinned messages tile with no perms ([\#7197](https://github.com/matrix-org/matrix-react-sdk/pull/7197)). Fixes #19886.
 * Make image size constrained by height when using the ImageSize.Large option ([\#7171](https://github.com/matrix-org/matrix-react-sdk/pull/7171)). Fixes #19788.
 * Prevent programmatic scrolling within truncated room sublists ([\#7191](https://github.com/matrix-org/matrix-react-sdk/pull/7191)).
 * Remove leading slash from /addwidget Jitsi confs ([\#7175](https://github.com/matrix-org/matrix-react-sdk/pull/7175)). Fixes #19839. Contributed by @AndrewFerr.
 * Fix automatic composer focus, regressed by threads work ([\#7167](https://github.com/matrix-org/matrix-react-sdk/pull/7167)). Fixes #19479.
 * Show space members when not invited even if summary didn't fail ([\#7153](https://github.com/matrix-org/matrix-react-sdk/pull/7153)). Fixes #19781.
 * Prevent custom power levels from breaking roles & permissions tab ([\#7160](https://github.com/matrix-org/matrix-react-sdk/pull/7160)). Fixes #19812.
 * Room Context Menu should respond to tag changes ([\#7154](https://github.com/matrix-org/matrix-react-sdk/pull/7154)). Fixes #19776.
 * Fix an edge case when trying to join an upgraded room ([\#7159](https://github.com/matrix-org/matrix-react-sdk/pull/7159)).

Changes in [1.9.6-rc.2](https://github.com/vector-im/element-web/releases/tag/v1.9.6-rc.2) (2021-12-01)
=======================================================================================================

 * Fixed release from correct branch

Changes in [1.9.6-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.9.6-rc.1) (2021-11-30)
=======================================================================================================

## ✨ Features
 * Tweaks to informational architecture 1.1 ([\#7052](https://github.com/matrix-org/matrix-react-sdk/pull/7052)). Fixes #19526, #19379, #17792, #16450, #19881, #19892, #19300, #19324, #17307, #17468, #19932 #19956 and #19526.
 * Add unread indicator to the timelineCard header icon ([\#7156](https://github.com/matrix-org/matrix-react-sdk/pull/7156)). Fixes #19635 and #19635.
 * Only show core navigation elements (call/chat/notification/info) when a widget is maximised ([\#7114](https://github.com/matrix-org/matrix-react-sdk/pull/7114)). Fixes #19632 and #19632.
 * Improve ThreadPanel ctx menu accessibility ([\#7217](https://github.com/matrix-org/matrix-react-sdk/pull/7217)). Fixes #19885 and #19885.
 * Allow filtering room list during treeview navigation ([\#7219](https://github.com/matrix-org/matrix-react-sdk/pull/7219)). Fixes #14702 and #14702.
 * Add right panel chat timeline ([\#7112](https://github.com/matrix-org/matrix-react-sdk/pull/7112)). Fixes #19633 and #19633.
 * Hide server options hint when disable_custom_urls is true ([\#7215](https://github.com/matrix-org/matrix-react-sdk/pull/7215)). Fixes #19919 and #19919.
 * Improve right panel resize handle usability ([\#7204](https://github.com/matrix-org/matrix-react-sdk/pull/7204)). Fixes #15145 and #15145. Contributed by @weeman1337.
 * Spaces quick settings ([\#7196](https://github.com/matrix-org/matrix-react-sdk/pull/7196)).
 * Maximised widgets always force a call to be shown in PIP mode ([\#7163](https://github.com/matrix-org/matrix-react-sdk/pull/7163)). Fixes #19637 and #19637.
 * Group Labs flags ([\#7190](https://github.com/matrix-org/matrix-react-sdk/pull/7190)).
 * Show room context details in forward dialog ([\#7162](https://github.com/matrix-org/matrix-react-sdk/pull/7162)). Fixes #19793 and #19793.
 * Remove chevrons from RoomSummaryCard_Button ([\#7137](https://github.com/matrix-org/matrix-react-sdk/pull/7137)). Fixes #19644 and #19644.
 * Disable op/deop commands where user has no permissions ([\#7161](https://github.com/matrix-org/matrix-react-sdk/pull/7161)). Fixes #15390 and #15390.
 * Add option to change the size of images/videos in the timeline ([\#7017](https://github.com/matrix-org/matrix-react-sdk/pull/7017)). Fixes vector-im/element-meta#49, #1520 #19498 and vector-im/element-meta#49.

## 🐛 Bug Fixes
 * Fix links being parsed as markdown links improperly ([\#7200](https://github.com/matrix-org/matrix-react-sdk/pull/7200)).
 * Fix left panel glow in Safari ([\#7236](https://github.com/matrix-org/matrix-react-sdk/pull/7236)). Fixes #19863 and #19863.
 * Fix newline on edit messages with quotes ([\#7227](https://github.com/matrix-org/matrix-react-sdk/pull/7227)). Fixes #12535 and #12535. Contributed by @renancleyson-dev.
 * Guard against null refs in findSiblingElement ([\#7228](https://github.com/matrix-org/matrix-react-sdk/pull/7228)).
 * Tweak bottom of space panel buttons in expanded state ([\#7213](https://github.com/matrix-org/matrix-react-sdk/pull/7213)). Fixes #19921 and #19921.
 * Fix multiline paragraph rendering as single line ([\#7210](https://github.com/matrix-org/matrix-react-sdk/pull/7210)). Fixes #8786 and #8786. Contributed by @renancleyson-dev.
 * Improve room list message previews ([\#7224](https://github.com/matrix-org/matrix-react-sdk/pull/7224)). Fixes #17101 #16169 and #17101.
 * Fix EmojiPicker lazy loaded rendering bug ([\#7225](https://github.com/matrix-org/matrix-react-sdk/pull/7225)). Fixes #15341 and #15341.
 * Prevent default avatar in UserInfo having pointer cursor ([\#7218](https://github.com/matrix-org/matrix-react-sdk/pull/7218)). Fixes #13872 and #13872.
 * Prevent duplicate avatars in Event List Summaries ([\#7222](https://github.com/matrix-org/matrix-react-sdk/pull/7222)). Fixes #17706 and #17706.
 * Respect the home page as a context for the Home space ([\#7216](https://github.com/matrix-org/matrix-react-sdk/pull/7216)). Fixes #19554 and #19554.
 * Fix RoomUpgradeWarningBar exploding ([\#7214](https://github.com/matrix-org/matrix-react-sdk/pull/7214)). Fixes #19920 and #19920.
 * Polish threads misalignments and UI diversion ([\#7209](https://github.com/matrix-org/matrix-react-sdk/pull/7209)). Fixes #19772, #19710, #19629 #19711 and #19772.
 * Fix Manage Restricted Join Rule Dialog for Spaces ([\#7208](https://github.com/matrix-org/matrix-react-sdk/pull/7208)). Fixes #19610 and #19610.
 * Fix wrongly showing unpin in pinned messages tile with no perms ([\#7197](https://github.com/matrix-org/matrix-react-sdk/pull/7197)). Fixes #19886 and #19886.
 * Make image size constrained by height when using the ImageSize.Large option ([\#7171](https://github.com/matrix-org/matrix-react-sdk/pull/7171)). Fixes #19788 and #19788.
 * Prevent programmatic scrolling within truncated room sublists ([\#7191](https://github.com/matrix-org/matrix-react-sdk/pull/7191)).
 * Remove leading slash from /addwidget Jitsi confs ([\#7175](https://github.com/matrix-org/matrix-react-sdk/pull/7175)). Fixes #19839 and #19839. Contributed by @AndrewFerr.
 * Fix automatic composer focus, regressed by threads work ([\#7167](https://github.com/matrix-org/matrix-react-sdk/pull/7167)). Fixes #19479 and #19479.
 * Show space members when not invited even if summary didn't fail ([\#7153](https://github.com/matrix-org/matrix-react-sdk/pull/7153)). Fixes #19781 and #19781.
 * Prevent custom power levels from breaking roles & permissions tab ([\#7160](https://github.com/matrix-org/matrix-react-sdk/pull/7160)). Fixes #19812 and #19812.
 * Room Context Menu should respond to tag changes ([\#7154](https://github.com/matrix-org/matrix-react-sdk/pull/7154)). Fixes #19776.
 * Fix an edge case when trying to join an upgraded room ([\#7159](https://github.com/matrix-org/matrix-react-sdk/pull/7159)).

Changes in [1.9.5](https://github.com/vector-im/element-web/releases/tag/v1.9.5) (2021-11-22)
=============================================================================================

## ✨ Features
 * Make double-clicking the PiP take you to the call room ([\#7142](https://github.com/matrix-org/matrix-react-sdk/pull/7142)). Fixes #18421 #15920 and #18421. Contributed by @SimonBrandner.
 * Add maximise widget functionality ([\#7098](https://github.com/matrix-org/matrix-react-sdk/pull/7098)). Fixes #19619, #19621 #19760 and #19619.
 * Add rainfall effect ([\#7086](https://github.com/matrix-org/matrix-react-sdk/pull/7086)). Contributed by @justjosias.
 * Add root folder to zip file created by export chat feature ([\#7097](https://github.com/matrix-org/matrix-react-sdk/pull/7097)). Fixes #19653 and #19653. Contributed by @aaronraimist.
 * Improve VoIP UI/UX ([\#7048](https://github.com/matrix-org/matrix-react-sdk/pull/7048)). Fixes #19513 and #19513. Contributed by @SimonBrandner.
 * Unified room context menus ([\#7072](https://github.com/matrix-org/matrix-react-sdk/pull/7072)). Fixes #19527 and #19527.
 * In forgot password screen, show validation errors inline in the form, instead of in modals ([\#7113](https://github.com/matrix-org/matrix-react-sdk/pull/7113)). Contributed by @psrpinto.
 * Implement more meta-spaces ([\#7077](https://github.com/matrix-org/matrix-react-sdk/pull/7077)). Fixes #18634 #17295 and #18634.
 * Expose power level control for m.space.child ([\#7120](https://github.com/matrix-org/matrix-react-sdk/pull/7120)).
 * Forget member-list query when switching out of a room ([\#7093](https://github.com/matrix-org/matrix-react-sdk/pull/7093)). Fixes #19432 and #19432. Contributed by @SimonBrandner.
 * Do pre-submit availability check on username during registration ([\#6978](https://github.com/matrix-org/matrix-react-sdk/pull/6978)). Fixes #9545 and #9545.

## 🐛 Bug Fixes
 * Adjust recovery key button sizes depending on text width ([\#7134](https://github.com/matrix-org/matrix-react-sdk/pull/7134)). Fixes #19511 and #19511. Contributed by @weeman1337.
 * Fix bulk invite button getting a negative count ([\#7122](https://github.com/matrix-org/matrix-react-sdk/pull/7122)). Fixes #19466 and #19466. Contributed by @renancleyson-dev.
 * Fix maximised / pinned widget state being loaded correctly ([\#7146](https://github.com/matrix-org/matrix-react-sdk/pull/7146)). Fixes #19768 and #19768.
 * Don't reload the page when user hits enter when entering ban reason ([\#7145](https://github.com/matrix-org/matrix-react-sdk/pull/7145)). Fixes #19763 and #19763.
 * Fix timeline text when sharing room layout ([\#7140](https://github.com/matrix-org/matrix-react-sdk/pull/7140)). Fixes #19622 and #19622.
 * Fix look of emoji verification ([\#7133](https://github.com/matrix-org/matrix-react-sdk/pull/7133)). Fixes #19740 and #19740. Contributed by @SimonBrandner.
 * Fixes element not remembering widget hidden state per room ([\#7136](https://github.com/matrix-org/matrix-react-sdk/pull/7136)). Fixes #16672, matrix-org/element-web-rageshakes#4407, #15718 #15768 and #16672.
 * Don't keep spinning if joining space child failed ([\#7129](https://github.com/matrix-org/matrix-react-sdk/pull/7129)). Fixes matrix-org/element-web-rageshakes#6813 and matrix-org/element-web-rageshakes#6813.
 * Guard around SpaceStore onAccountData handler prevEvent ([\#7123](https://github.com/matrix-org/matrix-react-sdk/pull/7123)). Fixes #19705 and #19705.
 * Fix missing spaces in threads copy ([\#7119](https://github.com/matrix-org/matrix-react-sdk/pull/7119)). Fixes #19702 and #19702.
 * Fix hover tile border ([\#7117](https://github.com/matrix-org/matrix-react-sdk/pull/7117)). Fixes #19698 and #19698. Contributed by @SimonBrandner.
 * Fix quote button ([\#7096](https://github.com/matrix-org/matrix-react-sdk/pull/7096)). Fixes #19659 and #19659. Contributed by @SimonBrandner.
 * Fix space panel layout edge cases ([\#7101](https://github.com/matrix-org/matrix-react-sdk/pull/7101)). Fixes #19668 and #19668.
 * Update powerlevel/role when the user changes in the user info panel ([\#7099](https://github.com/matrix-org/matrix-react-sdk/pull/7099)). Fixes #19666 and #19666. Contributed by @SimonBrandner.
 * Fix avatar disappearing when setting a room topic ([\#7092](https://github.com/matrix-org/matrix-react-sdk/pull/7092)). Fixes #19226 and #19226. Contributed by @SimonBrandner.
 * Fix possible infinite loop on widget start ([\#7071](https://github.com/matrix-org/matrix-react-sdk/pull/7071)). Fixes #15494 and #15494.
 * Use device IDs for nameless devices in device list ([\#7081](https://github.com/matrix-org/matrix-react-sdk/pull/7081)). Fixes #19608 and #19608.
 * Don't re-sort rooms on no-op RoomUpdateCause.PossibleTagChange ([\#7053](https://github.com/matrix-org/matrix-react-sdk/pull/7053)). Contributed by @bradtgmurray.

Changes in [1.9.5-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.9.5-rc.1) (2021-11-17)
=======================================================================================================

## ✨ Features
 * Make double-clicking the PiP take you to the call room ([\#7142](https://github.com/matrix-org/matrix-react-sdk/pull/7142)). Fixes #18421 #15920 and #18421. Contributed by @SimonBrandner.
 * Add maximise widget functionality ([\#7098](https://github.com/matrix-org/matrix-react-sdk/pull/7098)). Fixes #19619, #19621 #19760 and #19619.
 * Add rainfall effect ([\#7086](https://github.com/matrix-org/matrix-react-sdk/pull/7086)). Contributed by @justjosias.
 * Add root folder to zip file created by export chat feature ([\#7097](https://github.com/matrix-org/matrix-react-sdk/pull/7097)). Fixes #19653 and #19653. Contributed by @aaronraimist.
 * Improve VoIP UI/UX ([\#7048](https://github.com/matrix-org/matrix-react-sdk/pull/7048)). Fixes #19513 and #19513. Contributed by @SimonBrandner.
 * Unified room context menus ([\#7072](https://github.com/matrix-org/matrix-react-sdk/pull/7072)). Fixes #19527 and #19527.
 * In forgot password screen, show validation errors inline in the form, instead of in modals ([\#7113](https://github.com/matrix-org/matrix-react-sdk/pull/7113)). Contributed by @psrpinto.
 * Implement more meta-spaces ([\#7077](https://github.com/matrix-org/matrix-react-sdk/pull/7077)). Fixes #18634 #17295 and #18634.
 * Expose power level control for m.space.child ([\#7120](https://github.com/matrix-org/matrix-react-sdk/pull/7120)).
 * Forget member-list query when switching out of a room ([\#7093](https://github.com/matrix-org/matrix-react-sdk/pull/7093)). Fixes #19432 and #19432. Contributed by @SimonBrandner.
 * Do pre-submit availability check on username during registration ([\#6978](https://github.com/matrix-org/matrix-react-sdk/pull/6978)). Fixes #9545 and #9545.

## 🐛 Bug Fixes
 * Adjust recovery key button sizes depending on text width ([\#7134](https://github.com/matrix-org/matrix-react-sdk/pull/7134)). Fixes #19511 and #19511. Contributed by @weeman1337.
 * Fix bulk invite button getting a negative count ([\#7122](https://github.com/matrix-org/matrix-react-sdk/pull/7122)). Fixes #19466 and #19466. Contributed by @renancleyson-dev.
 * Fix maximised / pinned widget state being loaded correctly ([\#7146](https://github.com/matrix-org/matrix-react-sdk/pull/7146)). Fixes #19768 and #19768.
 * Don't reload the page when user hits enter when entering ban reason ([\#7145](https://github.com/matrix-org/matrix-react-sdk/pull/7145)). Fixes #19763 and #19763.
 * Fix timeline text when sharing room layout ([\#7140](https://github.com/matrix-org/matrix-react-sdk/pull/7140)). Fixes #19622 and #19622.
 * Fix look of emoji verification ([\#7133](https://github.com/matrix-org/matrix-react-sdk/pull/7133)). Fixes #19740 and #19740. Contributed by @SimonBrandner.
 * Fixes element not remembering widget hidden state per room ([\#7136](https://github.com/matrix-org/matrix-react-sdk/pull/7136)). Fixes #16672, matrix-org/element-web-rageshakes#4407, #15718 #15768 and #16672.
 * Don't keep spinning if joining space child failed ([\#7129](https://github.com/matrix-org/matrix-react-sdk/pull/7129)). Fixes matrix-org/element-web-rageshakes#6813 and matrix-org/element-web-rageshakes#6813.
 * Guard around SpaceStore onAccountData handler prevEvent ([\#7123](https://github.com/matrix-org/matrix-react-sdk/pull/7123)). Fixes #19705 and #19705.
 * Fix missing spaces in threads copy ([\#7119](https://github.com/matrix-org/matrix-react-sdk/pull/7119)). Fixes #19702 and #19702.
 * Fix hover tile border ([\#7117](https://github.com/matrix-org/matrix-react-sdk/pull/7117)). Fixes #19698 and #19698. Contributed by @SimonBrandner.
 * Fix quote button ([\#7096](https://github.com/matrix-org/matrix-react-sdk/pull/7096)). Fixes #19659 and #19659. Contributed by @SimonBrandner.
 * Fix space panel layout edge cases ([\#7101](https://github.com/matrix-org/matrix-react-sdk/pull/7101)). Fixes #19668 and #19668.
 * Update powerlevel/role when the user changes in the user info panel ([\#7099](https://github.com/matrix-org/matrix-react-sdk/pull/7099)). Fixes #19666 and #19666. Contributed by @SimonBrandner.
 * Fix avatar disappearing when setting a room topic ([\#7092](https://github.com/matrix-org/matrix-react-sdk/pull/7092)). Fixes #19226 and #19226. Contributed by @SimonBrandner.
 * Fix possible infinite loop on widget start ([\#7071](https://github.com/matrix-org/matrix-react-sdk/pull/7071)). Fixes #15494 and #15494.
 * Use device IDs for nameless devices in device list ([\#7081](https://github.com/matrix-org/matrix-react-sdk/pull/7081)). Fixes #19608 and #19608.
 * Don't re-sort rooms on no-op RoomUpdateCause.PossibleTagChange ([\#7053](https://github.com/matrix-org/matrix-react-sdk/pull/7053)). Contributed by @bradtgmurray.

Changes in [1.9.4](https://github.com/vector-im/element-web/releases/tag/v1.9.4) (2021-11-08)
=============================================================================================

## ✨ Features
 * Improve the look of tooltips ([\#7049](https://github.com/matrix-org/matrix-react-sdk/pull/7049)). Contributed by @SimonBrandner.
 * Improve the look of the spinner ([\#6083](https://github.com/matrix-org/matrix-react-sdk/pull/6083)). Contributed by @SimonBrandner.
 * Polls: Creation form & start event ([\#7001](https://github.com/matrix-org/matrix-react-sdk/pull/7001)).
 * Show a gray shield when encrypted by deleted session ([\#6119](https://github.com/matrix-org/matrix-react-sdk/pull/6119)). Contributed by @SimonBrandner.
 * <notes> ([\#7057](https://github.com/matrix-org/matrix-react-sdk/pull/7057)). Contributed by @ndarilek.
 * Make message separator more accessible. ([\#7056](https://github.com/matrix-org/matrix-react-sdk/pull/7056)). Contributed by @ndarilek.
 * <notes> ([\#7035](https://github.com/matrix-org/matrix-react-sdk/pull/7035)). Contributed by @ndarilek.
 * Implement RequiresClient capability for widgets ([\#7005](https://github.com/matrix-org/matrix-react-sdk/pull/7005)). Fixes #15744 and #15744.
 * Respect the system high contrast setting when using system theme ([\#7043](https://github.com/matrix-org/matrix-react-sdk/pull/7043)).
 * Remove redundant duplicate mimetype field which doesn't conform to spec ([\#7045](https://github.com/matrix-org/matrix-react-sdk/pull/7045)). Fixes #17145 and #17145.
 * Make join button on space hierarchy action in the background ([\#7041](https://github.com/matrix-org/matrix-react-sdk/pull/7041)). Fixes #17388 and #17388.
 * Add a high contrast theme (a variant of the light theme) ([\#7036](https://github.com/matrix-org/matrix-react-sdk/pull/7036)).
 * Improve timeline message for restricted join rule changes ([\#6984](https://github.com/matrix-org/matrix-react-sdk/pull/6984)). Fixes #18980 and #18980.
 * Improve the appearance of the font size slider ([\#7038](https://github.com/matrix-org/matrix-react-sdk/pull/7038)).
 * Improve RovingTabIndex & Room List filtering performance ([\#6987](https://github.com/matrix-org/matrix-react-sdk/pull/6987)). Fixes #17864 and #17864.
 * Remove outdated Spaces restricted rooms warning ([\#6927](https://github.com/matrix-org/matrix-react-sdk/pull/6927)).
 * Make /msg <message> param optional for more flexibility ([\#7028](https://github.com/matrix-org/matrix-react-sdk/pull/7028)). Fixes #19481 and #19481.
 * Add decoration to space hierarchy for tiles which have already been j… ([\#6969](https://github.com/matrix-org/matrix-react-sdk/pull/6969)). Fixes #18755 and #18755.
 * Add insert link button to the format bar ([\#5879](https://github.com/matrix-org/matrix-react-sdk/pull/5879)). Contributed by @SimonBrandner.
 * Improve visibility of font size chooser ([\#6988](https://github.com/matrix-org/matrix-react-sdk/pull/6988)).
 * Soften border-radius on selected/hovered messages ([\#6525](https://github.com/matrix-org/matrix-react-sdk/pull/6525)). Fixes #18108. Contributed by @SimonBrandner.
 * Add a developer mode flag and use it for accessing space timelines ([\#6994](https://github.com/matrix-org/matrix-react-sdk/pull/6994)). Fixes #19416 and #19416.
 * Position toggle switch more clearly ([\#6914](https://github.com/matrix-org/matrix-react-sdk/pull/6914)). Contributed by @CicadaCinema.
 * Validate email address in forgot password dialog ([\#6983](https://github.com/matrix-org/matrix-react-sdk/pull/6983)). Fixes #9978 and #9978. Contributed by @psrpinto.
 * Handle and i18n M_THREEPID_IN_USE during registration ([\#6986](https://github.com/matrix-org/matrix-react-sdk/pull/6986)). Fixes #13767 and #13767.
 * For space invite previews, use room summary API to get the right member count ([\#6982](https://github.com/matrix-org/matrix-react-sdk/pull/6982)). Fixes #19123 and #19123.
 * Simplify Space Panel notification badge layout ([\#6977](https://github.com/matrix-org/matrix-react-sdk/pull/6977)). Fixes #18527 and #18527.
 * Use prettier hsName during 3pid registration where possible ([\#6980](https://github.com/matrix-org/matrix-react-sdk/pull/6980)). Fixes #19162 and #19162.

## 🐛 Bug Fixes
 * Add a condition to only activate the resizer which belongs to the clicked handle ([\#7055](https://github.com/matrix-org/matrix-react-sdk/pull/7055)). Fixes #19521 and #19521.
 * Restore composer focus after event edit ([\#7065](https://github.com/matrix-org/matrix-react-sdk/pull/7065)). Fixes #19469 and #19469.
 * Don't apply message bubble visual style to media messages ([\#7040](https://github.com/matrix-org/matrix-react-sdk/pull/7040)).
 * Handle no selected screen when screen-sharing ([\#7018](https://github.com/matrix-org/matrix-react-sdk/pull/7018)). Fixes #19460 and #19460. Contributed by @SimonBrandner.
 * Add history entry before completing emoji ([\#7007](https://github.com/matrix-org/matrix-react-sdk/pull/7007)). Fixes #19177 and #19177. Contributed by @RafaelGoncalves8.
 * Add padding between controls on edit form in message bubbles ([\#7039](https://github.com/matrix-org/matrix-react-sdk/pull/7039)).
 * Respect the roomState right container request for the Jitsi widget ([\#7033](https://github.com/matrix-org/matrix-react-sdk/pull/7033)). Fixes #16552 and #16552.
 * Fix cannot read length of undefined for room upgrades ([\#7037](https://github.com/matrix-org/matrix-react-sdk/pull/7037)). Fixes #19509 and #19509.
 * Cleanup re-dispatching around timelines and composers ([\#7023](https://github.com/matrix-org/matrix-react-sdk/pull/7023)). Fixes #19491 and #19491. Contributed by @SimonBrandner.
 * Fix removing a room from a Space and interaction with `m.space.parent` ([\#6944](https://github.com/matrix-org/matrix-react-sdk/pull/6944)). Fixes #19363 and #19363.
 * Fix recent css regression ([\#7022](https://github.com/matrix-org/matrix-react-sdk/pull/7022)). Fixes #19470 and #19470. Contributed by @CicadaCinema.
 * Fix ModalManager reRender racing with itself ([\#7027](https://github.com/matrix-org/matrix-react-sdk/pull/7027)). Fixes #19489 and #19489.
 * Fix fullscreening a call while connecting ([\#7019](https://github.com/matrix-org/matrix-react-sdk/pull/7019)). Fixes #19309 and #19309. Contributed by @SimonBrandner.
 * Allow scrolling right in reply-quoted code block ([\#7024](https://github.com/matrix-org/matrix-react-sdk/pull/7024)). Fixes #19487 and #19487. Contributed by @SimonBrandner.
 * Fix dark theme codeblock colors ([\#6384](https://github.com/matrix-org/matrix-react-sdk/pull/6384)). Fixes #17998. Contributed by @SimonBrandner.
 * Show passphrase input label ([\#6992](https://github.com/matrix-org/matrix-react-sdk/pull/6992)). Fixes #19428 and #19428. Contributed by @RafaelGoncalves8.
 * Always render disabled settings as disabled ([\#7014](https://github.com/matrix-org/matrix-react-sdk/pull/7014)).
 * Make "Security Phrase" placeholder look consistent cross-browser ([\#6870](https://github.com/matrix-org/matrix-react-sdk/pull/6870)). Fixes #19006 and #19006. Contributed by @neer17.
 * Fix direction override characters breaking member event text direction ([\#6999](https://github.com/matrix-org/matrix-react-sdk/pull/6999)).
 * Remove redundant text in verification dialogs ([\#6993](https://github.com/matrix-org/matrix-react-sdk/pull/6993)). Fixes #19290 and #19290. Contributed by @RafaelGoncalves8.
 * Fix space panel name overflowing ([\#6995](https://github.com/matrix-org/matrix-react-sdk/pull/6995)). Fixes #19455 and #19455.
 * Fix conflicting CSS on syntax highlighted blocks ([\#6991](https://github.com/matrix-org/matrix-react-sdk/pull/6991)). Fixes #19445 and #19445.

Changes in [1.9.3](https://github.com/vector-im/element-desktop/releases/tag/v1.9.3) (2021-10-25)
=================================================================================================

## ✨ Features
 * Convert the "Cryptography" settings panel to an HTML table to assist screen reader users. ([\#6968](https://github.com/matrix-org/matrix-react-sdk/pull/6968)). Contributed by [andybalaam](https://github.com/andybalaam).
 * Swap order of private space creation and tweak copy ([\#6967](https://github.com/matrix-org/matrix-react-sdk/pull/6967)). Fixes #18768 and #18768.
 * Add spacing to Room settings - Notifications subsection ([\#6962](https://github.com/matrix-org/matrix-react-sdk/pull/6962)). Contributed by [CicadaCinema](https://github.com/CicadaCinema).
 * Use HTML tables for some tabular user interface areas, to assist with screen reader use ([\#6955](https://github.com/matrix-org/matrix-react-sdk/pull/6955)). Contributed by [andybalaam](https://github.com/andybalaam).
 * Fix space invite edge cases ([\#6884](https://github.com/matrix-org/matrix-react-sdk/pull/6884)). Fixes #19010 #17345 and #19010.
 * Allow options to cascade kicks/bans throughout spaces ([\#6829](https://github.com/matrix-org/matrix-react-sdk/pull/6829)). Fixes #18969 and #18969.
 * Make public space alias field mandatory again ([\#6921](https://github.com/matrix-org/matrix-react-sdk/pull/6921)). Fixes #19003 and #19003.
 * Add progress bar to restricted room upgrade dialog ([\#6919](https://github.com/matrix-org/matrix-react-sdk/pull/6919)). Fixes #19146 and #19146.
 * Add customisation point for visibility of invites and room creation ([\#6922](https://github.com/matrix-org/matrix-react-sdk/pull/6922)). Fixes #19331 and #19331.
 * Inhibit `Unable to get validated threepid` error during UIA ([\#6928](https://github.com/matrix-org/matrix-react-sdk/pull/6928)). Fixes #18883 and #18883.
 * Tweak room list skeleton UI height and behaviour ([\#6926](https://github.com/matrix-org/matrix-react-sdk/pull/6926)). Fixes #18231 #16581 and #18231.
 * If public room creation fails, retry without publishing it ([\#6872](https://github.com/matrix-org/matrix-react-sdk/pull/6872)). Fixes #19194 and #19194. Contributed by [AndrewFerr](https://github.com/AndrewFerr).
 * Iterate invite your teammates to Space view ([\#6925](https://github.com/matrix-org/matrix-react-sdk/pull/6925)). Fixes #18772 and #18772.
 * Make placeholder more grey when no input ([\#6840](https://github.com/matrix-org/matrix-react-sdk/pull/6840)). Fixes #17243 and #17243. Contributed by [wlach](https://github.com/wlach).
 * Respect tombstones in locally known rooms for Space children ([\#6906](https://github.com/matrix-org/matrix-react-sdk/pull/6906)). Fixes #19246 #19256 and #19246.
 * Improve emoji shortcodes generated from annotations ([\#6907](https://github.com/matrix-org/matrix-react-sdk/pull/6907)). Fixes #19304 and #19304.
 * Hide kick & ban options in UserInfo when looking at own profile ([\#6911](https://github.com/matrix-org/matrix-react-sdk/pull/6911)). Fixes #19066 and #19066.
 * Add progress bar to Community to Space migration tool ([\#6887](https://github.com/matrix-org/matrix-react-sdk/pull/6887)). Fixes #19216 and #19216.

## 🐛 Bug Fixes
 * Fix leave space cancel button exploding ([\#6966](https://github.com/matrix-org/matrix-react-sdk/pull/6966)).
 * Fix edge case behaviour of the space join spinner for guests ([\#6972](https://github.com/matrix-org/matrix-react-sdk/pull/6972)). Fixes #19359 and #19359.
 * Convert emoticon to emoji at the end of a line on send even if the cursor isn't there ([\#6965](https://github.com/matrix-org/matrix-react-sdk/pull/6965)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix text overflows button on Home page ([\#6898](https://github.com/matrix-org/matrix-react-sdk/pull/6898)). Fixes #19180 and #19180. Contributed by [oliver-pham](https://github.com/oliver-pham).
 * Space Room View should react to join rule changes down /sync ([\#6945](https://github.com/matrix-org/matrix-react-sdk/pull/6945)). Fixes #19390 and #19390.
 * Hide leave section button if user isn't in the room e.g peeking ([\#6920](https://github.com/matrix-org/matrix-react-sdk/pull/6920)). Fixes #17410 and #17410.
 * Fix bug where room list would get stuck showing no rooms ([\#6939](https://github.com/matrix-org/matrix-react-sdk/pull/6939)). Fixes #19373 and #19373.
 * Update room settings dialog title when room name changes ([\#6916](https://github.com/matrix-org/matrix-react-sdk/pull/6916)). Fixes #17480 and #17480. Contributed by [psrpinto](https://github.com/psrpinto).
 * Fix editing losing emote-ness and rainbow-ness of messages ([\#6931](https://github.com/matrix-org/matrix-react-sdk/pull/6931)). Fixes #19350 and #19350.
 * Remove semicolon from notifications panel ([\#6930](https://github.com/matrix-org/matrix-react-sdk/pull/6930)). Contributed by [robintown](https://github.com/robintown).
 * Prevent profile image in left panel's backdrop from being selected ([\#6924](https://github.com/matrix-org/matrix-react-sdk/pull/6924)). Contributed by [rom4nik](https://github.com/rom4nik).
 * Validate that the phone number verification field is filled before allowing user to submit ([\#6918](https://github.com/matrix-org/matrix-react-sdk/pull/6918)). Fixes #19316 and #19316. Contributed by [VFermat](https://github.com/VFermat).
 * Updated how save button becomes disabled in room settings to listen for all fields instead of the most recent ([\#6917](https://github.com/matrix-org/matrix-react-sdk/pull/6917)). Contributed by [LoganArnett](https://github.com/LoganArnett).
 * Use FocusLock around ContextMenus to simplify focus management ([\#6311](https://github.com/matrix-org/matrix-react-sdk/pull/6311)). Fixes #19259 and #19259.
 * Fix space hierarchy pagination ([\#6908](https://github.com/matrix-org/matrix-react-sdk/pull/6908)). Fixes #19276 and #19276.
 * Fix spaces keyboard shortcuts not working for last space ([\#6909](https://github.com/matrix-org/matrix-react-sdk/pull/6909)). Fixes #19255 and #19255.
 * Use fallback avatar only for DMs with 2 people. ([\#6895](https://github.com/matrix-org/matrix-react-sdk/pull/6895)). Fixes #18747 and #18747. Contributed by [andybalaam](https://github.com/andybalaam).

Changes in [1.9.3-rc.3](https://github.com/vector-im/element-desktop/releases/tag/v1.9.3-rc.3) (2021-10-25)
===========================================================================================================

## 🐛 Bug Fixes
 * Remove highlightjs CSS ([\#19483](https://github.com/vector-im/element-web/pull/19483)). Fixes vector-im/element-web#19476


Changes in [1.9.3-rc.2](https://github.com/vector-im/element-desktop/releases/tag/v1.9.3-rc.2) (2021-10-20)
===========================================================================================================

## 🐛 Bug Fixes
 * Fix conflicting CSS on syntax highlighted blocks ([\#6991](https://github.com/matrix-org/matrix-react-sdk/pull/6991)). Fixes vector-im/element-web#19445

Changes in [1.9.3-rc.1](https://github.com/vector-im/element-desktop/releases/tag/v1.9.3-rc.1) (2021-10-19)
===========================================================================================================

## ✨ Features
 * Swap order of private space creation and tweak copy ([\#6967](https://github.com/matrix-org/matrix-react-sdk/pull/6967)). Fixes #18768 and #18768.
 * Add spacing to Room settings - Notifications subsection ([\#6962](https://github.com/matrix-org/matrix-react-sdk/pull/6962)). Contributed by [CicadaCinema](https://github.com/CicadaCinema).
 * Convert the "Cryptography" settings panel to an HTML to assist screen reader users. ([\#6968](https://github.com/matrix-org/matrix-react-sdk/pull/6968)). Contributed by [andybalaam](https://github.com/andybalaam).
 * Use HTML tables for some tabular user interface areas, to assist with screen reader use ([\#6955](https://github.com/matrix-org/matrix-react-sdk/pull/6955)). Contributed by [andybalaam](https://github.com/andybalaam).
 * Fix space invite edge cases ([\#6884](https://github.com/matrix-org/matrix-react-sdk/pull/6884)). Fixes #19010 #17345 and #19010.
 * Allow options to cascade kicks/bans throughout spaces ([\#6829](https://github.com/matrix-org/matrix-react-sdk/pull/6829)). Fixes #18969 and #18969.
 * Make public space alias field mandatory again ([\#6921](https://github.com/matrix-org/matrix-react-sdk/pull/6921)). Fixes #19003 and #19003.
 * Add progress bar to restricted room upgrade dialog ([\#6919](https://github.com/matrix-org/matrix-react-sdk/pull/6919)). Fixes #19146 and #19146.
 * Add customisation point for visibility of invites and room creation ([\#6922](https://github.com/matrix-org/matrix-react-sdk/pull/6922)). Fixes #19331 and #19331.
 * Inhibit `Unable to get validated threepid` error during UIA ([\#6928](https://github.com/matrix-org/matrix-react-sdk/pull/6928)). Fixes #18883 and #18883.
 * Tweak room list skeleton UI height and behaviour ([\#6926](https://github.com/matrix-org/matrix-react-sdk/pull/6926)). Fixes #18231 #16581 and #18231.
 * If public room creation fails, retry without publishing it ([\#6872](https://github.com/matrix-org/matrix-react-sdk/pull/6872)). Fixes #19194 and #19194. Contributed by [AndrewFerr](https://github.com/AndrewFerr).
 * Iterate invite your teammates to Space view ([\#6925](https://github.com/matrix-org/matrix-react-sdk/pull/6925)). Fixes #18772 and #18772.
 * Make placeholder more grey when no input ([\#6840](https://github.com/matrix-org/matrix-react-sdk/pull/6840)). Fixes #17243 and #17243. Contributed by [wlach](https://github.com/wlach).
 * Respect tombstones in locally known rooms for Space children ([\#6906](https://github.com/matrix-org/matrix-react-sdk/pull/6906)). Fixes #19246 #19256 and #19246.
 * Improve emoji shortcodes generated from annotations ([\#6907](https://github.com/matrix-org/matrix-react-sdk/pull/6907)). Fixes #19304 and #19304.
 * Hide kick & ban options in UserInfo when looking at own profile ([\#6911](https://github.com/matrix-org/matrix-react-sdk/pull/6911)). Fixes #19066 and #19066.
 * Add progress bar to Community to Space migration tool ([\#6887](https://github.com/matrix-org/matrix-react-sdk/pull/6887)). Fixes #19216 and #19216.

## 🐛 Bug Fixes
 * Fix leave space cancel button exploding ([\#6966](https://github.com/matrix-org/matrix-react-sdk/pull/6966)).
 * Fix edge case behaviour of the space join spinner for guests ([\#6972](https://github.com/matrix-org/matrix-react-sdk/pull/6972)). Fixes #19359 and #19359.
 * Convert emoticon to emoji at the end of a line on send even if the cursor isn't there ([\#6965](https://github.com/matrix-org/matrix-react-sdk/pull/6965)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix text overflows button on Home page ([\#6898](https://github.com/matrix-org/matrix-react-sdk/pull/6898)). Fixes #19180 and #19180. Contributed by [oliver-pham](https://github.com/oliver-pham).
 * Space Room View should react to join rule changes down /sync ([\#6945](https://github.com/matrix-org/matrix-react-sdk/pull/6945)). Fixes #19390 and #19390.
 * Hide leave section button if user isn't in the room e.g peeking ([\#6920](https://github.com/matrix-org/matrix-react-sdk/pull/6920)). Fixes #17410 and #17410.
 * Fix bug where room list would get stuck showing no rooms ([\#6939](https://github.com/matrix-org/matrix-react-sdk/pull/6939)). Fixes #19373 and #19373.
 * Update room settings dialog title when room name changes ([\#6916](https://github.com/matrix-org/matrix-react-sdk/pull/6916)). Fixes #17480 and #17480. Contributed by [psrpinto](https://github.com/psrpinto).
 * Fix editing losing emote-ness and rainbow-ness of messages ([\#6931](https://github.com/matrix-org/matrix-react-sdk/pull/6931)). Fixes #19350 and #19350.
 * Remove semicolon from notifications panel ([\#6930](https://github.com/matrix-org/matrix-react-sdk/pull/6930)). Contributed by [robintown](https://github.com/robintown).
 * Prevent profile image in left panel's backdrop from being selected ([\#6924](https://github.com/matrix-org/matrix-react-sdk/pull/6924)). Contributed by [rom4nik](https://github.com/rom4nik).
 * Validate that the phone number verification field is filled before allowing user to submit ([\#6918](https://github.com/matrix-org/matrix-react-sdk/pull/6918)). Fixes #19316 and #19316. Contributed by [VFermat](https://github.com/VFermat).
 * Updated how save button becomes disabled in room settings to listen for all fields instead of the most recent ([\#6917](https://github.com/matrix-org/matrix-react-sdk/pull/6917)). Contributed by [LoganArnett](https://github.com/LoganArnett).
 * Use FocusLock around ContextMenus to simplify focus management ([\#6311](https://github.com/matrix-org/matrix-react-sdk/pull/6311)). Fixes #19259 and #19259.
 * Fix space hierarchy pagination ([\#6908](https://github.com/matrix-org/matrix-react-sdk/pull/6908)). Fixes #19276 and #19276.
 * Fix spaces keyboard shortcuts not working for last space ([\#6909](https://github.com/matrix-org/matrix-react-sdk/pull/6909)). Fixes #19255 and #19255.
 * Use fallback avatar only for DMs with 2 people. ([\#6895](https://github.com/matrix-org/matrix-react-sdk/pull/6895)). Fixes #18747 and #18747. Contributed by [andybalaam](https://github.com/andybalaam).

Changes in [1.9.2](https://github.com/vector-im/element-desktop/releases/tag/v1.9.2) (2021-10-12)
=================================================================================================

## 🐛 Bug Fixes
 * Upgrade to matrix-js-sdk#14.0.1

Changes in [1.9.1](https://github.com/vector-im/element-desktop/releases/tag/v1.9.1) (2021-10-11)
=================================================================================================

## ✨ Features
 * Decrease profile button touch target ([\#6900](https://github.com/matrix-org/matrix-react-sdk/pull/6900)). Contributed by [ColonisationCaptain](https://github.com/ColonisationCaptain).
 * Don't let click events propagate out of context menus ([\#6892](https://github.com/matrix-org/matrix-react-sdk/pull/6892)).
 * Allow closing Dropdown via its chevron ([\#6885](https://github.com/matrix-org/matrix-react-sdk/pull/6885)). Fixes #19030 and #19030.
 * Improve AUX panel behaviour ([\#6699](https://github.com/matrix-org/matrix-react-sdk/pull/6699)). Fixes #18787 and #18787. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * A nicer opening animation for the Image View ([\#6454](https://github.com/matrix-org/matrix-react-sdk/pull/6454)). Fixes #18186 and #18186. Contributed by [SimonBrandner](https://github.com/SimonBrandner).

## 🐛 Bug Fixes
 * [Release] Fix space hierarchy pagination ([\#6910](https://github.com/matrix-org/matrix-react-sdk/pull/6910)).
 * Fix leaving space via other client leaving you in undefined-land ([\#6891](https://github.com/matrix-org/matrix-react-sdk/pull/6891)). Fixes #18455 and #18455.
 * Handle newer voice message encrypted event format for chat export ([\#6893](https://github.com/matrix-org/matrix-react-sdk/pull/6893)). Contributed by [jaiwanth-v](https://github.com/jaiwanth-v).
 * Fix pagination when filtering space hierarchy ([\#6876](https://github.com/matrix-org/matrix-react-sdk/pull/6876)). Fixes #19235 and #19235.
 * Fix spaces null-guard breaking the dispatcher settings watching ([\#6886](https://github.com/matrix-org/matrix-react-sdk/pull/6886)). Fixes #19223 and #19223.
 * Fix space children without specific `order` being sorted after those with one ([\#6878](https://github.com/matrix-org/matrix-react-sdk/pull/6878)). Fixes #19192 and #19192.
 * Ensure that sub-spaces aren't considered for notification badges ([\#6881](https://github.com/matrix-org/matrix-react-sdk/pull/6881)). Fixes #18975 and #18975.
 * Fix timeline autoscroll with non-standard DPI settings. ([\#6880](https://github.com/matrix-org/matrix-react-sdk/pull/6880)). Fixes #18984 and #18984.
 * Pluck out JoinRuleSettings styles so they apply in space settings too ([\#6879](https://github.com/matrix-org/matrix-react-sdk/pull/6879)). Fixes #19164 and #19164.
 * Null guard around the matrixClient in SpaceStore ([\#6874](https://github.com/matrix-org/matrix-react-sdk/pull/6874)).
 * Fix issue (https ([\#6871](https://github.com/matrix-org/matrix-react-sdk/pull/6871)). Fixes #19138 and #19138. Contributed by [psrpinto](https://github.com/psrpinto).
 * Fix pills being cut off in message bubble layout ([\#6865](https://github.com/matrix-org/matrix-react-sdk/pull/6865)). Fixes #18627 and #18627. Contributed by [robintown](https://github.com/robintown).
 * Fix space admin check false positive on multiple admins ([\#6824](https://github.com/matrix-org/matrix-react-sdk/pull/6824)).
 * Fix the User View ([\#6860](https://github.com/matrix-org/matrix-react-sdk/pull/6860)). Fixes #19158 and #19158.
 * Fix spacing for message composer buttons ([\#6852](https://github.com/matrix-org/matrix-react-sdk/pull/6852)). Fixes #18999 and #18999.
 * Always show root event of a thread in room's timeline ([\#6842](https://github.com/matrix-org/matrix-react-sdk/pull/6842)). Fixes #19016 and #19016.

Changes in [1.9.1-rc.2](https://github.com/vector-im/element-desktop/releases/tag/v1.9.1-rc.2) (2021-10-08)
===========================================================================================================

## 🐛 Bug Fixes

Changes in [1.9.1-rc.1](https://github.com/vector-im/element-desktop/releases/tag/v1.9.1-rc.1) (2021-10-04)
===========================================================================================================

## ✨ Features
 * Decrease profile button touch target ([\#6900](https://github.com/matrix-org/matrix-react-sdk/pull/6900)). Contributed by [ColonisationCaptain](https://github.com/ColonisationCaptain).
 * Don't let click events propagate out of context menus ([\#6892](https://github.com/matrix-org/matrix-react-sdk/pull/6892)).
 * Allow closing Dropdown via its chevron ([\#6885](https://github.com/matrix-org/matrix-react-sdk/pull/6885)). Fixes #19030 and #19030.
 * Improve AUX panel behaviour ([\#6699](https://github.com/matrix-org/matrix-react-sdk/pull/6699)). Fixes #18787 and #18787. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * A nicer opening animation for the Image View ([\#6454](https://github.com/matrix-org/matrix-react-sdk/pull/6454)). Fixes #18186 and #18186. Contributed by [SimonBrandner](https://github.com/SimonBrandner).

## 🐛 Bug Fixes
 * Fix leaving space via other client leaving you in undefined-land ([\#6891](https://github.com/matrix-org/matrix-react-sdk/pull/6891)). Fixes #18455 and #18455.
 * Handle newer voice message encrypted event format for chat export ([\#6893](https://github.com/matrix-org/matrix-react-sdk/pull/6893)). Contributed by [jaiwanth-v](https://github.com/jaiwanth-v).
 * Fix pagination when filtering space hierarchy ([\#6876](https://github.com/matrix-org/matrix-react-sdk/pull/6876)). Fixes #19235 and #19235.
 * Fix spaces null-guard breaking the dispatcher settings watching ([\#6886](https://github.com/matrix-org/matrix-react-sdk/pull/6886)). Fixes #19223 and #19223.
 * Fix space children without specific `order` being sorted after those with one ([\#6878](https://github.com/matrix-org/matrix-react-sdk/pull/6878)). Fixes #19192 and #19192.
 * Ensure that sub-spaces aren't considered for notification badges ([\#6881](https://github.com/matrix-org/matrix-react-sdk/pull/6881)). Fixes #18975 and #18975.
 * Fix timeline autoscroll with non-standard DPI settings. ([\#6880](https://github.com/matrix-org/matrix-react-sdk/pull/6880)). Fixes #18984 and #18984.
 * Pluck out JoinRuleSettings styles so they apply in space settings too ([\#6879](https://github.com/matrix-org/matrix-react-sdk/pull/6879)). Fixes #19164 and #19164.
 * Null guard around the matrixClient in SpaceStore ([\#6874](https://github.com/matrix-org/matrix-react-sdk/pull/6874)).
 * Fix issue (https ([\#6871](https://github.com/matrix-org/matrix-react-sdk/pull/6871)). Fixes #19138 and #19138. Contributed by [psrpinto](https://github.com/psrpinto).
 * Fix pills being cut off in message bubble layout ([\#6865](https://github.com/matrix-org/matrix-react-sdk/pull/6865)). Fixes #18627 and #18627. Contributed by [robintown](https://github.com/robintown).
 * Fix space admin check false positive on multiple admins ([\#6824](https://github.com/matrix-org/matrix-react-sdk/pull/6824)).
 * Fix the User View ([\#6860](https://github.com/matrix-org/matrix-react-sdk/pull/6860)). Fixes #19158 and #19158.
 * Fix spacing for message composer buttons ([\#6852](https://github.com/matrix-org/matrix-react-sdk/pull/6852)). Fixes #18999 and #18999.
 * Always show root event of a thread in room's timeline ([\#6842](https://github.com/matrix-org/matrix-react-sdk/pull/6842)). Fixes #19016 and #19016.

Changes in [1.9.0](https://github.com/vector-im/element-desktop/releases/tag/v1.9.0) (2021-09-27)
=================================================================================================

## ✨ Features
 * Fix space keyboard shortcuts conflicting with native zoom shortcuts ([\#19037](https://github.com/vector-im/element-web/pull/19037)). Fixes #18481 and undefined/element-web#18481.
 * Say Joining space instead of Joining room where we know its a space ([\#6818](https://github.com/matrix-org/matrix-react-sdk/pull/6818)). Fixes #19064 and #19064.
 * Add warning that some spaces may not be relinked to the newly upgraded room ([\#6805](https://github.com/matrix-org/matrix-react-sdk/pull/6805)). Fixes #18858 and #18858.
 * Delabs Spaces, iterate some copy and move communities/space toggle to preferences ([\#6594](https://github.com/matrix-org/matrix-react-sdk/pull/6594)). Fixes #18088, #18524 #18088 and #18088.
 * Show "Message" in the user info panel instead of "Start chat" ([\#6319](https://github.com/matrix-org/matrix-react-sdk/pull/6319)). Fixes #17877 and #17877. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix space keyboard shortcuts conflicting with native zoom shortcuts ([\#6804](https://github.com/matrix-org/matrix-react-sdk/pull/6804)).
 * Replace plain text emoji at the end of a line ([\#6784](https://github.com/matrix-org/matrix-react-sdk/pull/6784)). Fixes #18833 and #18833. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Simplify Space Panel layout and fix some edge cases ([\#6800](https://github.com/matrix-org/matrix-react-sdk/pull/6800)). Fixes #18694 and #18694.
 * Show unsent message warning on Space Panel buttons ([\#6778](https://github.com/matrix-org/matrix-react-sdk/pull/6778)). Fixes #18891 and #18891.
 * Hide mute/unmute button in UserInfo for Spaces as it makes no sense ([\#6790](https://github.com/matrix-org/matrix-react-sdk/pull/6790)). Fixes #19007 and #19007.
 * Fix automatic field population in space create menu not validating ([\#6792](https://github.com/matrix-org/matrix-react-sdk/pull/6792)). Fixes #19005 and #19005.
 * Optimize input label transition on focus ([\#6783](https://github.com/matrix-org/matrix-react-sdk/pull/6783)). Fixes #12876 and #12876. Contributed by [MadLittleMods](https://github.com/MadLittleMods).
 * Adapt and re-use the RolesRoomSettingsTab for Spaces ([\#6779](https://github.com/matrix-org/matrix-react-sdk/pull/6779)). Fixes #18908 #18909 and #18908.
 * Deduplicate join rule management between rooms and spaces ([\#6724](https://github.com/matrix-org/matrix-react-sdk/pull/6724)). Fixes #18798 and #18798.
 * Add config option to turn on in-room event sending timing metrics ([\#6766](https://github.com/matrix-org/matrix-react-sdk/pull/6766)).
 * Improve the upgrade for restricted user experience ([\#6764](https://github.com/matrix-org/matrix-react-sdk/pull/6764)). Fixes #18677 and #18677.
 * Improve tooltips on space quick actions and explore button ([\#6760](https://github.com/matrix-org/matrix-react-sdk/pull/6760)). Fixes #18528 and #18528.
 * Make space members and user info behave more expectedly ([\#6765](https://github.com/matrix-org/matrix-react-sdk/pull/6765)). Fixes #17018 and #17018.
 * hide no-op m.room.encryption events and better word param changes ([\#6747](https://github.com/matrix-org/matrix-react-sdk/pull/6747)). Fixes #18597 and #18597.
 * Respect m.space.parent relations if they hold valid permissions ([\#6746](https://github.com/matrix-org/matrix-react-sdk/pull/6746)). Fixes #10935 and #10935.
 * Space panel accessibility improvements ([\#6744](https://github.com/matrix-org/matrix-react-sdk/pull/6744)). Fixes #18892 and #18892.

## 🐛 Bug Fixes
 * Fix spacing for message composer buttons ([\#6854](https://github.com/matrix-org/matrix-react-sdk/pull/6854)).
 * Fix accessing field on oobData which may be undefined ([\#6830](https://github.com/matrix-org/matrix-react-sdk/pull/6830)). Fixes #19085 and #19085.
 * Fix reactions aria-label not being a string and thus being read as [Object object] ([\#6828](https://github.com/matrix-org/matrix-react-sdk/pull/6828)).
 * Fix missing null guard in space hierarchy pagination ([\#6821](https://github.com/matrix-org/matrix-react-sdk/pull/6821)). Fixes matrix-org/element-web-rageshakes#6299 and matrix-org/element-web-rageshakes#6299.
 * Fix checks to show prompt to start new chats ([\#6812](https://github.com/matrix-org/matrix-react-sdk/pull/6812)).
 * Fix room list scroll jumps ([\#6777](https://github.com/matrix-org/matrix-react-sdk/pull/6777)). Fixes #17460 #18440 and #17460. Contributed by [robintown](https://github.com/robintown).
 * Fix various message bubble alignment issues ([\#6785](https://github.com/matrix-org/matrix-react-sdk/pull/6785)). Fixes #18293, #18294 #18305 and #18293. Contributed by [robintown](https://github.com/robintown).
 * Make message bubble font size consistent ([\#6795](https://github.com/matrix-org/matrix-react-sdk/pull/6795)). Contributed by [robintown](https://github.com/robintown).
 * Fix edge cases around joining new room which does not belong to active space ([\#6797](https://github.com/matrix-org/matrix-react-sdk/pull/6797)). Fixes #19025 and #19025.
 * Fix edge case space issues around creation and initial view ([\#6798](https://github.com/matrix-org/matrix-react-sdk/pull/6798)). Fixes #19023 and #19023.
 * Stop spinner on space preview if the join fails ([\#6803](https://github.com/matrix-org/matrix-react-sdk/pull/6803)). Fixes #19034 and #19034.
 * Fix emoji picker and stickerpicker not appearing correctly when opened ([\#6793](https://github.com/matrix-org/matrix-react-sdk/pull/6793)). Fixes #19012 and #19012. Contributed by [Palid](https://github.com/Palid).
 * Fix autocomplete not having y-scroll ([\#6794](https://github.com/matrix-org/matrix-react-sdk/pull/6794)). Fixes #18997 and #18997. Contributed by [Palid](https://github.com/Palid).
 * Fix broken edge case with public space creation with no alias ([\#6791](https://github.com/matrix-org/matrix-react-sdk/pull/6791)). Fixes #19003 and #19003.
 * Redirect from /#/welcome to /#/home if already logged in ([\#6786](https://github.com/matrix-org/matrix-react-sdk/pull/6786)). Fixes #18990 and #18990. Contributed by [aaronraimist](https://github.com/aaronraimist).
 * Fix build issues from two conflicting PRs landing without merge conflict ([\#6780](https://github.com/matrix-org/matrix-react-sdk/pull/6780)).
 * Render guest settings only in public rooms/spaces ([\#6693](https://github.com/matrix-org/matrix-react-sdk/pull/6693)). Fixes #18776 and #18776. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix message bubble corners being wrong in the presence of hidden events ([\#6776](https://github.com/matrix-org/matrix-react-sdk/pull/6776)). Fixes #18124 and #18124. Contributed by [robintown](https://github.com/robintown).
 * Debounce read marker update on scroll ([\#6771](https://github.com/matrix-org/matrix-react-sdk/pull/6771)). Fixes #18961 and #18961.
 * Use cursor:pointer on space panel buttons ([\#6770](https://github.com/matrix-org/matrix-react-sdk/pull/6770)). Fixes #18951 and #18951.
 * Fix regressed tab view buttons in space update toast ([\#6761](https://github.com/matrix-org/matrix-react-sdk/pull/6761)). Fixes #18781 and #18781.

Changes in [1.8.6-rc.2](https://github.com/vector-im/element-desktop/releases/tag/v1.8.6-rc.2) (2021-09-22)
===========================================================================================================

## 🐛 Bug Fixes
 * Fix spacing for message composer buttons ([\#6854](https://github.com/matrix-org/matrix-react-sdk/pull/6854)).

Changes in [1.8.6-rc.1](https://github.com/vector-im/element-desktop/releases/tag/v1.8.6-rc.1) (2021-09-21)
===========================================================================================================

## ✨ Features
 * Fix space keyboard shortcuts conflicting with native zoom shortcuts ([\#19037](https://github.com/vector-im/element-web/pull/19037)). Fixes #18481 and undefined/element-web#18481.
 * Say Joining space instead of Joining room where we know its a space ([\#6818](https://github.com/matrix-org/matrix-react-sdk/pull/6818)). Fixes #19064 and #19064.
 * Add warning that some spaces may not be relinked to the newly upgraded room ([\#6805](https://github.com/matrix-org/matrix-react-sdk/pull/6805)). Fixes #18858 and #18858.
 * Delabs Spaces, iterate some copy and move communities/space toggle to preferences ([\#6594](https://github.com/matrix-org/matrix-react-sdk/pull/6594)). Fixes #18088, #18524 #18088 and #18088.
 * Show "Message" in the user info panel instead of "Start chat" ([\#6319](https://github.com/matrix-org/matrix-react-sdk/pull/6319)). Fixes #17877 and #17877. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix space keyboard shortcuts conflicting with native zoom shortcuts ([\#6804](https://github.com/matrix-org/matrix-react-sdk/pull/6804)).
 * Replace plain text emoji at the end of a line ([\#6784](https://github.com/matrix-org/matrix-react-sdk/pull/6784)). Fixes #18833 and #18833. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Simplify Space Panel layout and fix some edge cases ([\#6800](https://github.com/matrix-org/matrix-react-sdk/pull/6800)). Fixes #18694 and #18694.
 * Show unsent message warning on Space Panel buttons ([\#6778](https://github.com/matrix-org/matrix-react-sdk/pull/6778)). Fixes #18891 and #18891.
 * Hide mute/unmute button in UserInfo for Spaces as it makes no sense ([\#6790](https://github.com/matrix-org/matrix-react-sdk/pull/6790)). Fixes #19007 and #19007.
 * Fix automatic field population in space create menu not validating ([\#6792](https://github.com/matrix-org/matrix-react-sdk/pull/6792)). Fixes #19005 and #19005.
 * Optimize input label transition on focus ([\#6783](https://github.com/matrix-org/matrix-react-sdk/pull/6783)). Fixes #12876 and #12876. Contributed by [MadLittleMods](https://github.com/MadLittleMods).
 * Adapt and re-use the RolesRoomSettingsTab for Spaces ([\#6779](https://github.com/matrix-org/matrix-react-sdk/pull/6779)). Fixes #18908 #18909 and #18908.
 * Deduplicate join rule management between rooms and spaces ([\#6724](https://github.com/matrix-org/matrix-react-sdk/pull/6724)). Fixes #18798 and #18798.
 * Add config option to turn on in-room event sending timing metrics ([\#6766](https://github.com/matrix-org/matrix-react-sdk/pull/6766)).
 * Improve the upgrade for restricted user experience ([\#6764](https://github.com/matrix-org/matrix-react-sdk/pull/6764)). Fixes #18677 and #18677.
 * Improve tooltips on space quick actions and explore button ([\#6760](https://github.com/matrix-org/matrix-react-sdk/pull/6760)). Fixes #18528 and #18528.
 * Make space members and user info behave more expectedly ([\#6765](https://github.com/matrix-org/matrix-react-sdk/pull/6765)). Fixes #17018 and #17018.
 * hide no-op m.room.encryption events and better word param changes ([\#6747](https://github.com/matrix-org/matrix-react-sdk/pull/6747)). Fixes #18597 and #18597.
 * Respect m.space.parent relations if they hold valid permissions ([\#6746](https://github.com/matrix-org/matrix-react-sdk/pull/6746)). Fixes #10935 and #10935.
 * Space panel accessibility improvements ([\#6744](https://github.com/matrix-org/matrix-react-sdk/pull/6744)). Fixes #18892 and #18892.

## 🐛 Bug Fixes
 * Revert Firefox composer deletion hacks ([\#6844](https://github.com/matrix-org/matrix-react-sdk/pull/6844)). Fixes #19103 and #19103. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix accessing field on oobData which may be undefined ([\#6830](https://github.com/matrix-org/matrix-react-sdk/pull/6830)). Fixes #19085 and #19085.
 * Fix pill deletion on Firefox 78 ([\#6832](https://github.com/matrix-org/matrix-react-sdk/pull/6832)). Fixes #19077 and #19077. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix reactions aria-label not being a string and thus being read as [Object object] ([\#6828](https://github.com/matrix-org/matrix-react-sdk/pull/6828)).
 * Fix missing null guard in space hierarchy pagination ([\#6821](https://github.com/matrix-org/matrix-react-sdk/pull/6821)). Fixes matrix-org/element-web-rageshakes#6299 and matrix-org/element-web-rageshakes#6299.
 * Fix checks to show prompt to start new chats ([\#6812](https://github.com/matrix-org/matrix-react-sdk/pull/6812)).
 * Fix room list scroll jumps ([\#6777](https://github.com/matrix-org/matrix-react-sdk/pull/6777)). Fixes #17460 #18440 and #17460. Contributed by [robintown](https://github.com/robintown).
 * Fix various message bubble alignment issues ([\#6785](https://github.com/matrix-org/matrix-react-sdk/pull/6785)). Fixes #18293, #18294 #18305 and #18293. Contributed by [robintown](https://github.com/robintown).
 * Make message bubble font size consistent ([\#6795](https://github.com/matrix-org/matrix-react-sdk/pull/6795)). Contributed by [robintown](https://github.com/robintown).
 * Fix edge cases around joining new room which does not belong to active space ([\#6797](https://github.com/matrix-org/matrix-react-sdk/pull/6797)). Fixes #19025 and #19025.
 * Fix edge case space issues around creation and initial view ([\#6798](https://github.com/matrix-org/matrix-react-sdk/pull/6798)). Fixes #19023 and #19023.
 * Stop spinner on space preview if the join fails ([\#6803](https://github.com/matrix-org/matrix-react-sdk/pull/6803)). Fixes #19034 and #19034.
 * Fix emoji picker and stickerpicker not appearing correctly when opened ([\#6793](https://github.com/matrix-org/matrix-react-sdk/pull/6793)). Fixes #19012 and #19012. Contributed by [Palid](https://github.com/Palid).
 * Fix autocomplete not having y-scroll ([\#6794](https://github.com/matrix-org/matrix-react-sdk/pull/6794)). Fixes #18997 and #18997. Contributed by [Palid](https://github.com/Palid).
 * Fix broken edge case with public space creation with no alias ([\#6791](https://github.com/matrix-org/matrix-react-sdk/pull/6791)). Fixes #19003 and #19003.
 * Redirect from /#/welcome to /#/home if already logged in ([\#6786](https://github.com/matrix-org/matrix-react-sdk/pull/6786)). Fixes #18990 and #18990. Contributed by [aaronraimist](https://github.com/aaronraimist).
 * Fix build issues from two conflicting PRs landing without merge conflict ([\#6780](https://github.com/matrix-org/matrix-react-sdk/pull/6780)).
 * Render guest settings only in public rooms/spaces ([\#6693](https://github.com/matrix-org/matrix-react-sdk/pull/6693)). Fixes #18776 and #18776. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix message bubble corners being wrong in the presence of hidden events ([\#6776](https://github.com/matrix-org/matrix-react-sdk/pull/6776)). Fixes #18124 and #18124. Contributed by [robintown](https://github.com/robintown).
 * Debounce read marker update on scroll ([\#6771](https://github.com/matrix-org/matrix-react-sdk/pull/6771)). Fixes #18961 and #18961.
 * Use cursor:pointer on space panel buttons ([\#6770](https://github.com/matrix-org/matrix-react-sdk/pull/6770)). Fixes #18951 and #18951.
 * Fix regressed tab view buttons in space update toast ([\#6761](https://github.com/matrix-org/matrix-react-sdk/pull/6761)). Fixes #18781 and #18781.

Changes in [1.8.5](https://github.com/vector-im/element-desktop/releases/tag/v1.8.5) (2021-09-14)
=================================================================================================

## ✨ Features
 * Add bubble highlight styling ([\#6582](https://github.com/matrix-org/matrix-react-sdk/pull/6582)). Fixes #18295 and #18295. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Create narrow mode for Composer ([\#6682](https://github.com/matrix-org/matrix-react-sdk/pull/6682)). Fixes #18533 and #18533.
 * Prefer matrix.to alias links over room id in spaces & share ([\#6745](https://github.com/matrix-org/matrix-react-sdk/pull/6745)). Fixes #18796 and #18796.
 * Stop automatic playback of voice messages if a non-voice message is encountered ([\#6728](https://github.com/matrix-org/matrix-react-sdk/pull/6728)). Fixes #18850 and #18850.
 * Show call length during a call ([\#6700](https://github.com/matrix-org/matrix-react-sdk/pull/6700)). Fixes #18566 and #18566. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Serialize and retry mass-leave when leaving space ([\#6737](https://github.com/matrix-org/matrix-react-sdk/pull/6737)). Fixes #18789 and #18789.
 * Improve form handling in and around space creation ([\#6739](https://github.com/matrix-org/matrix-react-sdk/pull/6739)). Fixes #18775 and #18775.
 * Split autoplay GIFs and videos into different settings ([\#6726](https://github.com/matrix-org/matrix-react-sdk/pull/6726)). Fixes #5771 and #5771. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Add autoplay for voice messages ([\#6710](https://github.com/matrix-org/matrix-react-sdk/pull/6710)). Fixes #18804, #18715, #18714 #17961 and #18804.
 * Allow to use basic html to format invite messages ([\#6703](https://github.com/matrix-org/matrix-react-sdk/pull/6703)). Fixes #15738 and #15738. Contributed by [skolmer](https://github.com/skolmer).
 * Allow widgets, when eligible, to interact with more rooms as per MSC2762 ([\#6684](https://github.com/matrix-org/matrix-react-sdk/pull/6684)).
 * Remove arbitrary limits from send/receive events for widgets ([\#6719](https://github.com/matrix-org/matrix-react-sdk/pull/6719)). Fixes #17994 and #17994.
 * Reload suggested rooms if we see the state change down /sync ([\#6715](https://github.com/matrix-org/matrix-react-sdk/pull/6715)). Fixes #18761 and #18761.
 * When creating private spaces, make the initial rooms restricted if supported ([\#6721](https://github.com/matrix-org/matrix-react-sdk/pull/6721)). Fixes #18722 and #18722.
 * Threading exploration work ([\#6658](https://github.com/matrix-org/matrix-react-sdk/pull/6658)). Fixes #18532 and #18532.
 * Default to `Don't leave any` when leaving a space ([\#6697](https://github.com/matrix-org/matrix-react-sdk/pull/6697)). Fixes #18592 and #18592. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Special case redaction event sending from widgets per MSC2762 ([\#6686](https://github.com/matrix-org/matrix-react-sdk/pull/6686)). Fixes #18573 and #18573.
 * Add active speaker indicators ([\#6639](https://github.com/matrix-org/matrix-react-sdk/pull/6639)). Fixes #17627 and #17627. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Increase general app performance by optimizing layers ([\#6644](https://github.com/matrix-org/matrix-react-sdk/pull/6644)). Fixes #18730 and #18730. Contributed by [Palid](https://github.com/Palid).

## 🐛 Bug Fixes
 * Fix autocomplete not having y-scroll ([\#6802](https://github.com/matrix-org/matrix-react-sdk/pull/6802)).
 * Fix emoji picker and stickerpicker not appearing correctly when opened ([\#6801](https://github.com/matrix-org/matrix-react-sdk/pull/6801)).
 * Debounce read marker update on scroll ([\#6774](https://github.com/matrix-org/matrix-react-sdk/pull/6774)).
 * Fix Space creation wizard go to my first room button behaviour ([\#6748](https://github.com/matrix-org/matrix-react-sdk/pull/6748)). Fixes #18764 and #18764.
 * Fix scroll being stuck at bottom ([\#6751](https://github.com/matrix-org/matrix-react-sdk/pull/6751)). Fixes #18903 and #18903.
 * Fix widgets not remembering identity verification when asked to. ([\#6742](https://github.com/matrix-org/matrix-react-sdk/pull/6742)). Fixes #15631 and #15631.
 * Add missing pluralisation i18n strings for Spaces ([\#6738](https://github.com/matrix-org/matrix-react-sdk/pull/6738)). Fixes #18780 and #18780.
 * Make ForgotPassword UX slightly more user friendly ([\#6636](https://github.com/matrix-org/matrix-react-sdk/pull/6636)). Fixes #11531 and #11531. Contributed by [Palid](https://github.com/Palid).
 * Don't context switch room on SpaceStore ready as it can break permalinks ([\#6730](https://github.com/matrix-org/matrix-react-sdk/pull/6730)). Fixes #17974 and #17974.
 * Fix explore rooms button not working during space creation wizard ([\#6729](https://github.com/matrix-org/matrix-react-sdk/pull/6729)). Fixes #18762 and #18762.
 * Fix bug where one party's media would sometimes not be shown ([\#6731](https://github.com/matrix-org/matrix-react-sdk/pull/6731)).
 * Only make the initial space rooms suggested by default ([\#6714](https://github.com/matrix-org/matrix-react-sdk/pull/6714)). Fixes #18760 and #18760.
 * Replace fake username in EventTilePreview with a proper loading state ([\#6702](https://github.com/matrix-org/matrix-react-sdk/pull/6702)). Fixes #15897 and #15897. Contributed by [skolmer](https://github.com/skolmer).
 * Don't send prehistorical events to widgets during decryption at startup ([\#6695](https://github.com/matrix-org/matrix-react-sdk/pull/6695)). Fixes #18060 and #18060.
 * When creating subspaces properly set restricted join rule ([\#6725](https://github.com/matrix-org/matrix-react-sdk/pull/6725)). Fixes #18797 and #18797.
 * Fix the Image View not openning for some pinned messages ([\#6723](https://github.com/matrix-org/matrix-react-sdk/pull/6723)). Fixes #18422 and #18422. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Show autocomplete sections vertically ([\#6722](https://github.com/matrix-org/matrix-react-sdk/pull/6722)). Fixes #18860 and #18860. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix EmojiPicker filtering to lower case emojibase data strings ([\#6717](https://github.com/matrix-org/matrix-react-sdk/pull/6717)). Fixes #18686 and #18686.
 * Clear currentRoomId when viewing home page, fixing document title ([\#6716](https://github.com/matrix-org/matrix-react-sdk/pull/6716)). Fixes #18668 and #18668.
 * Fix membership updates to Spaces not applying in real-time ([\#6713](https://github.com/matrix-org/matrix-react-sdk/pull/6713)). Fixes #18737 and #18737.
 * Don't show a double stacked invite modals when inviting to Spaces ([\#6698](https://github.com/matrix-org/matrix-react-sdk/pull/6698)). Fixes #18745 and #18745. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Remove non-functional DuckDuckGo Autocomplete Provider ([\#6712](https://github.com/matrix-org/matrix-react-sdk/pull/6712)). Fixes #18778 and #18778.
 * Filter members on `MemberList` load ([\#6708](https://github.com/matrix-org/matrix-react-sdk/pull/6708)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix improper voice messages being produced in Firefox and sometimes other browsers. ([\#6696](https://github.com/matrix-org/matrix-react-sdk/pull/6696)). Fixes #18587 and #18587.
 * Fix client forgetting which capabilities a widget was approved for ([\#6685](https://github.com/matrix-org/matrix-react-sdk/pull/6685)). Fixes #18786 and #18786.
 * Fix left panel widgets not remembering collapsed state ([\#6687](https://github.com/matrix-org/matrix-react-sdk/pull/6687)). Fixes #17803 and #17803.
 * Fix changelog link colour back to blue ([\#6692](https://github.com/matrix-org/matrix-react-sdk/pull/6692)). Fixes #18726 and #18726.
 * Soften codeblock border color ([\#6564](https://github.com/matrix-org/matrix-react-sdk/pull/6564)). Fixes #18367 and #18367. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Pause ringing more aggressively ([\#6691](https://github.com/matrix-org/matrix-react-sdk/pull/6691)). Fixes #18588 and #18588. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix command autocomplete ([\#6680](https://github.com/matrix-org/matrix-react-sdk/pull/6680)). Fixes #18670 and #18670. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Don't re-sort the room-list based on profile/status changes ([\#6595](https://github.com/matrix-org/matrix-react-sdk/pull/6595)). Fixes #110 and #110. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix codeblock formatting with syntax highlighting on ([\#6681](https://github.com/matrix-org/matrix-react-sdk/pull/6681)). Fixes #18739 #18365 and #18739. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Add padding to the Add button in the notification settings ([\#6665](https://github.com/matrix-org/matrix-react-sdk/pull/6665)). Fixes #18706 and #18706. Contributed by [SimonBrandner](https://github.com/SimonBrandner).

Changes in [1.8.4](https://github.com/vector-im/element-web/releases/tag/v1.8.4) (2021-09-13)
=================================================================================================

## 🔒 SECURITY FIXES
 * Fix a security issue with message key sharing. See https://matrix.org/blog/2021/09/13/vulnerability-disclosure-key-sharing
   for details.

Changes in [1.8.2](https://github.com/vector-im/element-desktop/releases/tag/v1.8.2) (2021-08-31)
=================================================================================================

## ✨ Features
 * Documentation for sentry config ([\#18608](https://github.com/vector-im/element-web/pull/18608)). Contributed by [novocaine](https://github.com/novocaine).
 * [Release]Increase general app performance by optimizing layers ([\#6672](https://github.com/matrix-org/matrix-react-sdk/pull/6672)). Fixes #18730 and #18730. Contributed by [Palid](https://github.com/Palid).
 * Add a warning on E2EE rooms if you try to make them public ([\#5698](https://github.com/matrix-org/matrix-react-sdk/pull/5698)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Allow pagination of the space hierarchy and use new APIs ([\#6507](https://github.com/matrix-org/matrix-react-sdk/pull/6507)). Fixes #18089 and #18427.
 * Improve emoji in composer ([\#6650](https://github.com/matrix-org/matrix-react-sdk/pull/6650)). Fixes #18593 and #18593. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Allow playback of replied-to voice message ([\#6629](https://github.com/matrix-org/matrix-react-sdk/pull/6629)). Fixes #18599 and #18599. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Format autocomplete suggestions vertically ([\#6620](https://github.com/matrix-org/matrix-react-sdk/pull/6620)). Fixes #17574 and #17574. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Remember last `MemberList` search query per-room ([\#6640](https://github.com/matrix-org/matrix-react-sdk/pull/6640)). Fixes #18613 and #18613. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Sentry rageshakes ([\#6597](https://github.com/matrix-org/matrix-react-sdk/pull/6597)). Fixes #11111 and #11111. Contributed by [novocaine](https://github.com/novocaine).
 * Autocomplete has been updated to match modern accessibility standards. Navigate via up/down arrows rather than Tab. Enter or Tab to confirm a suggestion. This should be familiar to Slack & Discord users. You can now use Tab to navigate around the application and do more without touching your mouse. No more accidentally sending half of people's names because the completion didn't fire on Enter! ([\#5659](https://github.com/matrix-org/matrix-react-sdk/pull/5659)). Fixes #4872, #11071, #17171, #15646 #4872 and #4872.
 * Add new call tile states ([\#6610](https://github.com/matrix-org/matrix-react-sdk/pull/6610)). Fixes #18521 and #18521. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Left align call tiles ([\#6609](https://github.com/matrix-org/matrix-react-sdk/pull/6609)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Make loading encrypted images look snappier ([\#6590](https://github.com/matrix-org/matrix-react-sdk/pull/6590)). Fixes #17878 and #17862. Contributed by [Palid](https://github.com/Palid).
 * Offer a way to create a space based on existing community ([\#6543](https://github.com/matrix-org/matrix-react-sdk/pull/6543)). Fixes #18092.
 * Accessibility improvements in and around Spaces ([\#6569](https://github.com/matrix-org/matrix-react-sdk/pull/6569)). Fixes #18094 and #18094.

## 🐛 Bug Fixes
 * [Release] Fix commit edit history ([\#6690](https://github.com/matrix-org/matrix-react-sdk/pull/6690)). Fixes #18742 and #18742. Contributed by [Palid](https://github.com/Palid).
 * Fix images not rendering when sent from other clients. ([\#6661](https://github.com/matrix-org/matrix-react-sdk/pull/6661)). Fixes #18702 and #18702.
 * Fix autocomplete scrollbar and make the autocomplete a little smaller ([\#6655](https://github.com/matrix-org/matrix-react-sdk/pull/6655)). Fixes #18682 and #18682. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix replies on the bubble layout ([\#6451](https://github.com/matrix-org/matrix-react-sdk/pull/6451)). Fixes #18184. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Show "Enable encryption in settings" only when the user can do that ([\#6646](https://github.com/matrix-org/matrix-react-sdk/pull/6646)). Fixes #18646 and #18646. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix cross signing setup from settings screen ([\#6633](https://github.com/matrix-org/matrix-react-sdk/pull/6633)). Fixes #17761 and #17761.
 * Fix call tiles on the bubble layout ([\#6647](https://github.com/matrix-org/matrix-react-sdk/pull/6647)). Fixes #18648 and #18648. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix error on accessing encrypted media without encryption keys ([\#6625](https://github.com/matrix-org/matrix-react-sdk/pull/6625)). Contributed by [Palid](https://github.com/Palid).
 * Fix jitsi widget sometimes being permanently stuck in the bottom-right corner ([\#6632](https://github.com/matrix-org/matrix-react-sdk/pull/6632)). Fixes #17226 and #17226. Contributed by [Palid](https://github.com/Palid).
 * Fix FilePanel pagination in E2EE rooms ([\#6630](https://github.com/matrix-org/matrix-react-sdk/pull/6630)). Fixes #18415 and #18415. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix call tile buttons ([\#6624](https://github.com/matrix-org/matrix-react-sdk/pull/6624)). Fixes #18565 and #18565. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix vertical call tile spacing issues ([\#6621](https://github.com/matrix-org/matrix-react-sdk/pull/6621)). Fixes #18558 and #18558. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix long display names in call tiles ([\#6618](https://github.com/matrix-org/matrix-react-sdk/pull/6618)). Fixes #18562 and #18562. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Avoid access token overflow ([\#6616](https://github.com/matrix-org/matrix-react-sdk/pull/6616)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Properly handle media errors  ([\#6615](https://github.com/matrix-org/matrix-react-sdk/pull/6615)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix glare related regressions ([\#6614](https://github.com/matrix-org/matrix-react-sdk/pull/6614)). Fixes #18538 and #18538. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix long display names in call toasts ([\#6617](https://github.com/matrix-org/matrix-react-sdk/pull/6617)). Fixes #18557 and #18557. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix PiP of held calls ([\#6611](https://github.com/matrix-org/matrix-react-sdk/pull/6611)). Fixes #18539 and #18539. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix call tile behaviour on narrow layouts ([\#6556](https://github.com/matrix-org/matrix-react-sdk/pull/6556)). Fixes #18398. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix video call persisting when widget removed ([\#6608](https://github.com/matrix-org/matrix-react-sdk/pull/6608)). Fixes #15703 and #15703.
 * Fix toast colors ([\#6606](https://github.com/matrix-org/matrix-react-sdk/pull/6606)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Remove tiny scrollbar dot from code blocks ([\#6596](https://github.com/matrix-org/matrix-react-sdk/pull/6596)). Fixes #18474. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Improve handling of pills in the composer ([\#6353](https://github.com/matrix-org/matrix-react-sdk/pull/6353)). Fixes #10134 #10896 and #15037. Contributed by [SimonBrandner](https://github.com/SimonBrandner).

Changes in [1.8.1](https://github.com/vector-im/element-desktop/releases/tag/v1.8.1) (2021-08-17)
=================================================================================================

## 🐛 Bug Fixes
 * Fix multiple VoIP regressions ([matrix-org/matrix-js-sdk#1860](https://github.com/matrix-org/matrix-js-sdk/pull/1860)).

Changes in [1.8.0](https://github.com/vector-im/element-desktop/releases/tag/v1.8.0) (2021-08-16)
=================================================================================================

## ✨ Features
 * Show how long a call was on call tiles ([\#6570](https://github.com/matrix-org/matrix-react-sdk/pull/6570)). Fixes #18405. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Add regional indicators to emoji picker ([\#6490](https://github.com/matrix-org/matrix-react-sdk/pull/6490)). Fixes #14963. Contributed by [robintown](https://github.com/robintown).
 * Make call control buttons accessible to screen reader users ([\#6181](https://github.com/matrix-org/matrix-react-sdk/pull/6181)). Fixes #18358. Contributed by [pvagner](https://github.com/pvagner).
 * Skip sending a thumbnail if it is not a sufficient saving over the original ([\#6559](https://github.com/matrix-org/matrix-react-sdk/pull/6559)). Fixes #17906.
 * Increase PiP snapping speed ([\#6539](https://github.com/matrix-org/matrix-react-sdk/pull/6539)). Fixes #18371. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Improve and move the incoming call toast ([\#6470](https://github.com/matrix-org/matrix-react-sdk/pull/6470)). Fixes #17912. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Allow all of the URL schemes that Firefox allows ([\#6457](https://github.com/matrix-org/matrix-react-sdk/pull/6457)). Contributed by [aaronraimist](https://github.com/aaronraimist).
 * Improve bubble layout colors ([\#6452](https://github.com/matrix-org/matrix-react-sdk/pull/6452)). Fixes #18081. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Spaces let users switch between Home and All Rooms behaviours ([\#6497](https://github.com/matrix-org/matrix-react-sdk/pull/6497)). Fixes #18093.
 * Support for MSC2285 (hidden read receipts) ([\#6390](https://github.com/matrix-org/matrix-react-sdk/pull/6390)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Group pinned message events with MELS ([\#6349](https://github.com/matrix-org/matrix-react-sdk/pull/6349)). Fixes #17938. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Make version copiable ([\#6227](https://github.com/matrix-org/matrix-react-sdk/pull/6227)). Fixes #17603 and #18329. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Improve voice messages uploading state ([\#6530](https://github.com/matrix-org/matrix-react-sdk/pull/6530)). Fixes #18226 and #18224.
 * Add surround with feature ([\#5510](https://github.com/matrix-org/matrix-react-sdk/pull/5510)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Improve call event tile wording ([\#6545](https://github.com/matrix-org/matrix-react-sdk/pull/6545)). Fixes #18376. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Show an avatar/a turned off microphone icon for muted users ([\#6486](https://github.com/matrix-org/matrix-react-sdk/pull/6486)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Prompt user to leave rooms/subspaces in a space when leaving space ([\#6424](https://github.com/matrix-org/matrix-react-sdk/pull/6424)). Fixes #18071.
 * Add support for screen sharing in 1:1 calls ([\#5992](https://github.com/matrix-org/matrix-react-sdk/pull/5992)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).

## 🐛 Bug Fixes
 * Dismiss electron download toast when clicking Open ([\#18267](https://github.com/vector-im/element-web/pull/18267)). Fixes #18266.
 * [Release] Fix glare related regressions ([\#6622](https://github.com/matrix-org/matrix-react-sdk/pull/6622)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * [Release] Fix PiP of held calls ([\#6612](https://github.com/matrix-org/matrix-react-sdk/pull/6612)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * [Release] Fix toast colors ([\#6607](https://github.com/matrix-org/matrix-react-sdk/pull/6607)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix [object Object] in Widget Permissions ([\#6560](https://github.com/matrix-org/matrix-react-sdk/pull/6560)). Fixes #18384. Contributed by [Palid](https://github.com/Palid).
 * Fix right margin for events on IRC layout ([\#6542](https://github.com/matrix-org/matrix-react-sdk/pull/6542)). Fixes #18354.
 * Mirror only usermedia feeds ([\#6512](https://github.com/matrix-org/matrix-react-sdk/pull/6512)). Fixes #5633. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix LogoutDialog warning + TypeScript migration ([\#6533](https://github.com/matrix-org/matrix-react-sdk/pull/6533)).
 * Fix the wrong font being used in the room topic field ([\#6527](https://github.com/matrix-org/matrix-react-sdk/pull/6527)). Fixes #18339. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix inconsistent styling for links on hover ([\#6513](https://github.com/matrix-org/matrix-react-sdk/pull/6513)). Contributed by [janogarcia](https://github.com/janogarcia).
 * Fix incorrect height for encoded placeholder images ([\#6514](https://github.com/matrix-org/matrix-react-sdk/pull/6514)). Contributed by [Palid](https://github.com/Palid).
 * Fix call events layout for message bubble ([\#6465](https://github.com/matrix-org/matrix-react-sdk/pull/6465)). Fixes #18144.
 * Improve subspaces and some utilities around room/space creation ([\#6458](https://github.com/matrix-org/matrix-react-sdk/pull/6458)). Fixes #18090 #18091 and #17256.
 * Restore pointer cursor for SenderProfile in message bubbles ([\#6501](https://github.com/matrix-org/matrix-react-sdk/pull/6501)). Fixes #18249.
 * Fix issues with the Call View ([\#6472](https://github.com/matrix-org/matrix-react-sdk/pull/6472)). Fixes #18221. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Align event list summary read receipts when using message bubbles ([\#6500](https://github.com/matrix-org/matrix-react-sdk/pull/6500)). Fixes #18143.
 * Better positioning for unbubbled events in timeline ([\#6477](https://github.com/matrix-org/matrix-react-sdk/pull/6477)). Fixes #18132.
 * Realign reactions row with messages in modern layout ([\#6491](https://github.com/matrix-org/matrix-react-sdk/pull/6491)). Fixes #18118. Contributed by [robintown](https://github.com/robintown).
 * Fix CreateRoomDialog exploding when making public room outside of a space ([\#6492](https://github.com/matrix-org/matrix-react-sdk/pull/6492)). Fixes #18275.
 * Fix call crashing because `element` was undefined ([\#6488](https://github.com/matrix-org/matrix-react-sdk/pull/6488)). Fixes #18270. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Upscale thumbnails to the container size ([\#6589](https://github.com/matrix-org/matrix-react-sdk/pull/6589)). Fixes #18307.
 * Fix create room dialog in spaces no longer adding to the space ([\#6587](https://github.com/matrix-org/matrix-react-sdk/pull/6587)). Fixes #18465.
 * Don't show a modal on call reject/user hangup ([\#6580](https://github.com/matrix-org/matrix-react-sdk/pull/6580)). Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fade Call View Buttons after `componentDidMount` ([\#6581](https://github.com/matrix-org/matrix-react-sdk/pull/6581)). Fixes #18439. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix missing expand button on codeblocks ([\#6565](https://github.com/matrix-org/matrix-react-sdk/pull/6565)). Fixes #18388. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * allow customizing the bubble layout colors ([\#6568](https://github.com/matrix-org/matrix-react-sdk/pull/6568)). Fixes #18408. Contributed by [benneti](https://github.com/benneti).
 * Don't flash "Missed call" when accepting a call ([\#6567](https://github.com/matrix-org/matrix-react-sdk/pull/6567)). Fixes #18404. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix clicking whitespaces on replies ([\#6571](https://github.com/matrix-org/matrix-react-sdk/pull/6571)). Fixes #18327. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix composer not being disabled when sending voice messages ([\#6562](https://github.com/matrix-org/matrix-react-sdk/pull/6562)). Fixes #18413.
 * Fix sizing issues of the screen picker ([\#6498](https://github.com/matrix-org/matrix-react-sdk/pull/6498)). Fixes #18281. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Stop voice messages that are playing when starting a recording ([\#6563](https://github.com/matrix-org/matrix-react-sdk/pull/6563)). Fixes #18410.
 * Fix random box appearing when clicking room list headers. ([\#6561](https://github.com/matrix-org/matrix-react-sdk/pull/6561)). Fixes #18414.
 * Null guard space inviter to prevent the app exploding ([\#6558](https://github.com/matrix-org/matrix-react-sdk/pull/6558)).
 * Make the ringing sound mutable/disablable ([\#6534](https://github.com/matrix-org/matrix-react-sdk/pull/6534)). Fixes #15591. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix wrong cursor being used in PiP ([\#6551](https://github.com/matrix-org/matrix-react-sdk/pull/6551)). Fixes #18383. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Re-pin Jitsi if the widget already exists ([\#6226](https://github.com/matrix-org/matrix-react-sdk/pull/6226)). Fixes #17679. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix broken call notification regression ([\#6526](https://github.com/matrix-org/matrix-react-sdk/pull/6526)). Fixes #18335. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * createRoom, only send join rule event if we have a join rule to put in it ([\#6516](https://github.com/matrix-org/matrix-react-sdk/pull/6516)). Fixes #18301.
 * Fix clicking pills inside replies ([\#6508](https://github.com/matrix-org/matrix-react-sdk/pull/6508)). Fixes #18283. Contributed by [SimonBrandner](https://github.com/SimonBrandner).
 * Fix grecaptcha regression ([\#6503](https://github.com/matrix-org/matrix-react-sdk/pull/6503)). Fixes #18284. Contributed by [Palid](https://github.com/Palid).
 * Fix compatibility with accounts where the security passphrase was created on a mobile device ([\#1819](https://github.com/matrix-org/matrix-js-sdk/pull/1819)).

Changes in [1.7.34](https://github.com/vector-im/element-desktop/releases/tag/v1.7.34) (2021-08-02)
===================================================================================================

## 🔒 SECURITY FIXES
 * Sanitize untrusted variables from message previews before translation
   Fixes vector-im/element-web#18314

## ✨ Features
 * Fix editing of `<sub>` & `<sup`> & `<u>`
   [\#6469](https://github.com/matrix-org/matrix-react-sdk/pull/6469)
   Fixes #18211
 * Zoom images in lightbox to where the cursor points
   [\#6418](https://github.com/matrix-org/matrix-react-sdk/pull/6418)
   Fixes #17870
 * Avoid hitting the settings store from TextForEvent
   [\#6205](https://github.com/matrix-org/matrix-react-sdk/pull/6205)
   Fixes #17650
 * Initial MSC3083 + MSC3244 support
   [\#6212](https://github.com/matrix-org/matrix-react-sdk/pull/6212)
   Fixes #17686 and #17661
 * Navigate to the first room with notifications when clicked on space notification dot
   [\#5974](https://github.com/matrix-org/matrix-react-sdk/pull/5974)
 * Add matrix: to the list of permitted URL schemes
   [\#6388](https://github.com/matrix-org/matrix-react-sdk/pull/6388)
 * Add "Copy Link" to room context menu
   [\#6374](https://github.com/matrix-org/matrix-react-sdk/pull/6374)
 * 💭 Message bubble layout
   [\#6291](https://github.com/matrix-org/matrix-react-sdk/pull/6291)
   Fixes #4635, #17773 #16220 and #7687
 * Play only one audio file at a time
   [\#6417](https://github.com/matrix-org/matrix-react-sdk/pull/6417)
   Fixes #17439
 * Move download button for media to the action bar
   [\#6386](https://github.com/matrix-org/matrix-react-sdk/pull/6386)
   Fixes #17943
 * Improved display of one-to-one call history with summary boxes for each call
   [\#6121](https://github.com/matrix-org/matrix-react-sdk/pull/6121)
   Fixes #16409
 * Notification settings UI refresh
   [\#6352](https://github.com/matrix-org/matrix-react-sdk/pull/6352)
   Fixes #17782
 * Fix EventIndex double handling events and erroring
   [\#6385](https://github.com/matrix-org/matrix-react-sdk/pull/6385)
   Fixes #18008
 * Improve reply rendering
   [\#3553](https://github.com/matrix-org/matrix-react-sdk/pull/3553)
   Fixes vector-im/riot-web#9217, vector-im/riot-web#7633, vector-im/riot-web#7530, vector-im/riot-web#7169, vector-im/riot-web#7151, vector-im/riot-web#6692 vector-im/riot-web#6579 and #17440
 * Improve performance of room name calculation
   [\#1801](https://github.com/matrix-org/matrix-js-sdk/pull/1801)

## 🐛 Bug Fixes
 * Fix browser history getting stuck looping back to the same room
   [\#18053](https://github.com/vector-im/element-web/pull/18053)
 * Fix space shortcuts on layouts with non-English keys in the places of numbers
   [\#17780](https://github.com/vector-im/element-web/pull/17780)
   Fixes #17776
 * Fix CreateRoomDialog exploding when making public room outside of a space
   [\#6493](https://github.com/matrix-org/matrix-react-sdk/pull/6493)
 * Fix regression where registration would soft-crash on captcha
   [\#6505](https://github.com/matrix-org/matrix-react-sdk/pull/6505)
   Fixes #18284
 * only send join rule event if we have a join rule to put in it
   [\#6517](https://github.com/matrix-org/matrix-react-sdk/pull/6517)
 * Improve the new download button's discoverability and interactions.
   [\#6510](https://github.com/matrix-org/matrix-react-sdk/pull/6510)
 * Fix voice recording UI looking broken while microphone permissions are being requested.
   [\#6479](https://github.com/matrix-org/matrix-react-sdk/pull/6479)
   Fixes #18223
 * Match colors of room and user avatars in DMs
   [\#6393](https://github.com/matrix-org/matrix-react-sdk/pull/6393)
   Fixes #2449
 * Fix onPaste handler to work with copying files from Finder
   [\#5389](https://github.com/matrix-org/matrix-react-sdk/pull/5389)
   Fixes #15536 and #16255
 * Fix infinite pagination loop when offline
   [\#6478](https://github.com/matrix-org/matrix-react-sdk/pull/6478)
   Fixes #18242
 * Fix blurhash rounded corners missing regression
   [\#6467](https://github.com/matrix-org/matrix-react-sdk/pull/6467)
   Fixes #18110
 * Fix position of the space hierarchy spinner
   [\#6462](https://github.com/matrix-org/matrix-react-sdk/pull/6462)
   Fixes #18182
 * Fix display of image messages that lack thumbnails
   [\#6456](https://github.com/matrix-org/matrix-react-sdk/pull/6456)
   Fixes #18175
 * Fix crash with large audio files.
   [\#6436](https://github.com/matrix-org/matrix-react-sdk/pull/6436)
   Fixes #18149
 * Make diff colors in codeblocks more pleasant
   [\#6355](https://github.com/matrix-org/matrix-react-sdk/pull/6355)
   Fixes #17939
 * Show the correct audio file duration while loading the file.
   [\#6435](https://github.com/matrix-org/matrix-react-sdk/pull/6435)
   Fixes #18160
 * Fix various timeline settings not applying immediately.
   [\#6261](https://github.com/matrix-org/matrix-react-sdk/pull/6261)
   Fixes #17748
 * Fix issues with room list duplication
   [\#6391](https://github.com/matrix-org/matrix-react-sdk/pull/6391)
   Fixes #14508
 * Fix grecaptcha throwing useless error sometimes
   [\#6401](https://github.com/matrix-org/matrix-react-sdk/pull/6401)
   Fixes #15142
 * Update Emojibase and Twemoji and switch to IamCal (Slack-style) shortcodes
   [\#6347](https://github.com/matrix-org/matrix-react-sdk/pull/6347)
   Fixes #13857 and #13334
 * Respect compound emojis in default avatar initial generation
   [\#6397](https://github.com/matrix-org/matrix-react-sdk/pull/6397)
   Fixes #18040
 * Fix bug where the 'other homeserver' field in the server selection dialog would become briefly focus and then unfocus when clicked.
   [\#6394](https://github.com/matrix-org/matrix-react-sdk/pull/6394)
   Fixes #18031
 * Standardise spelling and casing of homeserver, identity server, and integration manager
   [\#6365](https://github.com/matrix-org/matrix-react-sdk/pull/6365)
 * Fix widgets not receiving decrypted events when they have permission.
   [\#6371](https://github.com/matrix-org/matrix-react-sdk/pull/6371)
   Fixes #17615
 * Prevent client hangs when calculating blurhashes
   [\#6366](https://github.com/matrix-org/matrix-react-sdk/pull/6366)
   Fixes #17945
 * Exclude state events from widgets reading room events
   [\#6378](https://github.com/matrix-org/matrix-react-sdk/pull/6378)
 * Cache feature_spaces\* flags to improve performance
   [\#6381](https://github.com/matrix-org/matrix-react-sdk/pull/6381)

Changes in [1.7.33](https://github.com/vector-im/element-web/releases/tag/v1.7.33) (2021-07-19)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.33-rc.1...v1.7.33)

 * No changes from rc.1

Changes in [1.7.33-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.33-rc.1) (2021-07-14)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.32...v1.7.33-rc.1)

 * Translations update from Weblate
   [\#17991](https://github.com/vector-im/element-web/pull/17991)
 * Revert "Don't run nginx as root in docker"
   [\#17990](https://github.com/vector-im/element-web/pull/17990)
 * Don't run nginx as root in docker
   [\#17927](https://github.com/vector-im/element-web/pull/17927)
 * Add VS Code to gitignore
   [\#17982](https://github.com/vector-im/element-web/pull/17982)
 * Remove canvas native dependencies from Dockerfile
   [\#17973](https://github.com/vector-im/element-web/pull/17973)
 * Remove node-canvas devDependency
   [\#17967](https://github.com/vector-im/element-web/pull/17967)
 * Add `reskindex` to development steps
   [\#17926](https://github.com/vector-im/element-web/pull/17926)
 * Update Modernizr and stop it from polluting classes on the html tag
   [\#17921](https://github.com/vector-im/element-web/pull/17921)
 * Convert a few files to TS
   [\#17895](https://github.com/vector-im/element-web/pull/17895)
 * Do not generate a lockfile when running in CI
   [\#17902](https://github.com/vector-im/element-web/pull/17902)
 * Fix lockfile to match listed dependencies
   [\#17888](https://github.com/vector-im/element-web/pull/17888)
 * Remove PostCSS calc() processing
   [\#17856](https://github.com/vector-im/element-web/pull/17856)
 * Make issue template styling more consistent and improve PR template
   [\#17691](https://github.com/vector-im/element-web/pull/17691)
 * Update jsrsasign to ^10.2.0 (Includes fix for CVE-2021-30246)
   [\#17170](https://github.com/vector-im/element-web/pull/17170)
 * Migrate to `eslint-plugin-matrix-org`
   [\#17847](https://github.com/vector-im/element-web/pull/17847)
 * Remove spurious overflow: auto on #matrixchat element
   [\#17647](https://github.com/vector-im/element-web/pull/17647)
 * Enhance security by disallowing CSP object-src rule
   [\#17818](https://github.com/vector-im/element-web/pull/17818)

Changes in [1.7.32](https://github.com/vector-im/element-web/releases/tag/v1.7.32) (2021-07-05)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.32-rc.1...v1.7.32)

 * No changes from rc.1

Changes in [1.7.32-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.32-rc.1) (2021-06-29)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.31...v1.7.32-rc.1)

 * Update to react-sdk v3.25.0-rc.1 and js-sdk v12.0.1-rc.1
 * Translations update from Weblate
   [\#17832](https://github.com/vector-im/element-web/pull/17832)
 * Fix canvas-filter-polyfill mock path
   [\#17785](https://github.com/vector-im/element-web/pull/17785)
 * Mock context-filter-polyfill for app-tests
   [\#17774](https://github.com/vector-im/element-web/pull/17774)
 * Add libera.chat to default room directory
   [\#17772](https://github.com/vector-im/element-web/pull/17772)
 * Improve typing of Event Index Manager / Seshat
   [\#17704](https://github.com/vector-im/element-web/pull/17704)
 * Bump dns-packet from 1.3.1 to 1.3.4
   [\#17478](https://github.com/vector-im/element-web/pull/17478)
 * Update matrix-widget-api to fix build issues
   [\#17747](https://github.com/vector-im/element-web/pull/17747)
 * Fix whitespace in Dockerfile
   [\#17742](https://github.com/vector-im/element-web/pull/17742)
 * Upgrade @types/react and @types/react-dom
   [\#17723](https://github.com/vector-im/element-web/pull/17723)
 * Spaces keyboard shortcuts first cut
   [\#17457](https://github.com/vector-im/element-web/pull/17457)
 * Labs: feature_report_to_moderators
   [\#17694](https://github.com/vector-im/element-web/pull/17694)

Changes in [1.7.31](https://github.com/vector-im/element-web/releases/tag/v1.7.31) (2021-06-21)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.31-rc.1...v1.7.31)

 * Upgrade to React SDK 3.24.0 and JS SDK 12.0.0

Changes in [1.7.31-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.31-rc.1) (2021-06-15)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.30...v1.7.31-rc.1)

 * Upgrade to React SDK 3.24.0-rc.1 and JS SDK 12.0.0-rc.1
 * Translations update from Weblate
   [\#17655](https://github.com/vector-im/element-web/pull/17655)
 * Upgrade matrix-react-test-utils for React 17 peer deps
   [\#17653](https://github.com/vector-im/element-web/pull/17653)
 * Fix lint errors in Webpack config
   [\#17626](https://github.com/vector-im/element-web/pull/17626)
 * Preload only `woff2` fonts
   [\#17614](https://github.com/vector-im/element-web/pull/17614)
 * ⚛️ Upgrade to React@17
   [\#17601](https://github.com/vector-im/element-web/pull/17601)

Changes in [1.7.30](https://github.com/vector-im/element-web/releases/tag/v1.7.30) (2021-06-07)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.30-rc.1...v1.7.30)

 * Upgrade to React SDK 3.23.0 and JS SDK 11.2.0

Changes in [1.7.30-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.30-rc.1) (2021-06-01)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.29...v1.7.30-rc.1)

 * Upgrade to React SDK 3.23.0-rc.1 and JS SDK 11.2.0-rc.1
 * Translations update from Weblate
   [\#17526](https://github.com/vector-im/element-web/pull/17526)
 * Add Modernizr test for Promise.allSettled given js-sdk and react-sdk depend
   on it
   [\#17464](https://github.com/vector-im/element-web/pull/17464)
 * Bump libolm dependency, and update package name.
   [\#17433](https://github.com/vector-im/element-web/pull/17433)
 * Remove logo spinner
   [\#17423](https://github.com/vector-im/element-web/pull/17423)

Changes in [1.7.29](https://github.com/vector-im/element-web/releases/tag/v1.7.29) (2021-05-24)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.29-rc.1...v1.7.29)

## Security notice

Element Web 1.7.29 fixes (by upgrading to olm 3.2.3) an issue in code used for
decrypting server-side stored secrets. The issue could potentially allow a
malicious homeserver to cause a stack buffer overflow in the affected function
and to control that function's local variables.

## All changes

 * Upgrade to React SDK 3.22.0 and JS SDK 11.1.0
 * [Release] Bump libolm dependency, and update package name
   [\#17456](https://github.com/vector-im/element-web/pull/17456)

Changes in [1.7.29-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.29-rc.1) (2021-05-19)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.28...v1.7.29-rc.1)

 * Upgrade to React SDK 3.22.0-rc.1 and JS SDK 11.1.0-rc.1
 * Translations update from Weblate
   [\#17384](https://github.com/vector-im/element-web/pull/17384)
 * Prevent minification of `.html` files
   [\#17349](https://github.com/vector-im/element-web/pull/17349)
 * Update matrix-widget-api/react-sdk dependency reference
   [\#17346](https://github.com/vector-im/element-web/pull/17346)
 * Add `yarn start:https`
   [\#16989](https://github.com/vector-im/element-web/pull/16989)
 * Translations update from Weblate
   [\#17239](https://github.com/vector-im/element-web/pull/17239)
 * Remove "in development" flag from voice messages labs documentation
   [\#17204](https://github.com/vector-im/element-web/pull/17204)
 * Add required webpack+jest config to load Safari support modules
   [\#17193](https://github.com/vector-im/element-web/pull/17193)

Changes in [1.7.28](https://github.com/vector-im/element-web/releases/tag/v1.7.28) (2021-05-17)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.28-rc.1...v1.7.28)

## Security notice

Element Web 1.7.28 fixes (by upgrading to matrix-react-sdk 3.21.0) a low
severity issue (GHSA-8796-gc9j-63rv) related to file upload. When uploading a
file, the local file preview can lead to execution of scripts embedded in the
uploaded file, but only after several user interactions to open the preview in
a separate tab. This only impacts the local user while in the process of
uploading. It cannot be exploited remotely or by other users. Thanks to
[Muhammad Zaid Ghifari](https://github.com/MR-ZHEEV) for responsibly disclosing
this via Matrix's Security Disclosure Policy.

## All changes

 * Upgrade to React SDK 3.21.0 and JS SDK 11.0.0

Changes in [1.7.28-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.28-rc.1) (2021-05-11)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.27...v1.7.28-rc.1)

 * Upgrade to React SDK 3.21.0-rc.1 and JS SDK 11.0.0-rc.1
 * Switch back to release version of `sanitize-html`
   [\#17231](https://github.com/vector-im/element-web/pull/17231)
 * Bump url-parse from 1.4.7 to 1.5.1
   [\#17199](https://github.com/vector-im/element-web/pull/17199)
 * Bump lodash from 4.17.20 to 4.17.21
   [\#17205](https://github.com/vector-im/element-web/pull/17205)
 * Bump hosted-git-info from 2.8.8 to 2.8.9
   [\#17219](https://github.com/vector-im/element-web/pull/17219)
 * Disable host checking on the webpack dev server
   [\#17194](https://github.com/vector-im/element-web/pull/17194)
 * Bump ua-parser-js from 0.7.23 to 0.7.24
   [\#17190](https://github.com/vector-im/element-web/pull/17190)

Changes in [1.7.27](https://github.com/vector-im/element-web/releases/tag/v1.7.27) (2021-05-10)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.27-rc.1...v1.7.27)

 * Upgrade to React SDK 3.20.0 and JS SDK 10.1.0

Changes in [1.7.27-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.27-rc.1) (2021-05-04)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.26...v1.7.27-rc.1)

 * Upgrade to React SDK 3.20.0-rc.1 and JS SDK 10.1.0-rc.1
 * Translations update from Weblate
   [\#17160](https://github.com/vector-im/element-web/pull/17160)
 * Document option for obeying asserted identity
   [\#17008](https://github.com/vector-im/element-web/pull/17008)
 * Implement IPC call to Electron to set language
   [\#17052](https://github.com/vector-im/element-web/pull/17052)
 * Convert Vector skin react components to Typescript
   [\#17061](https://github.com/vector-im/element-web/pull/17061)
 * Add code quality review policy
   [\#16980](https://github.com/vector-im/element-web/pull/16980)
 * Register RecorderWorklet from react-sdk
   [\#17013](https://github.com/vector-im/element-web/pull/17013)
 * Preload Inter font to avoid FOIT on slow connections
   [\#17039](https://github.com/vector-im/element-web/pull/17039)
 * Disable `postcss-calc`'s noisy `warnWhenCannotResolve` option
   [\#17041](https://github.com/vector-im/element-web/pull/17041)

Changes in [1.7.26](https://github.com/vector-im/element-web/releases/tag/v1.7.26) (2021-04-26)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.26-rc.1...v1.7.26)

 * Upgrade to React SDK 3.19.0 and JS SDK 10.0.0

Changes in [1.7.26-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.26-rc.1) (2021-04-21)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.25...v1.7.26-rc.1)

 * Upgrade to React SDK 3.19.0-rc.1 and JS SDK 10.0.0-rc.1
 * Translations update from Weblate
   [\#17031](https://github.com/vector-im/element-web/pull/17031)
 * Bump ssri from 6.0.1 to 6.0.2
   [\#17010](https://github.com/vector-im/element-web/pull/17010)
 * Fix `NODE_ENV` value for CI environments
   [\#17003](https://github.com/vector-im/element-web/pull/17003)
 * Use React production mode in CI builds
   [\#16969](https://github.com/vector-im/element-web/pull/16969)
 * Labs documentation for DND mode
   [\#16962](https://github.com/vector-im/element-web/pull/16962)
 * Rename blackboxing to new option ignore list
   [\#16965](https://github.com/vector-im/element-web/pull/16965)
 * Remove velocity-animate from lockfile
   [\#16963](https://github.com/vector-im/element-web/pull/16963)
 * Add mobile download link configuration
   [\#16890](https://github.com/vector-im/element-web/pull/16890)
 * Switch develop to not-staging Scalar by default
   [\#16883](https://github.com/vector-im/element-web/pull/16883)
 * Support a config option to skip login/welcome and go to SSO
   [\#16880](https://github.com/vector-im/element-web/pull/16880)

Changes in [1.7.25](https://github.com/vector-im/element-web/releases/tag/v1.7.25) (2021-04-12)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.25-rc.1...v1.7.25)

 * Upgrade to React SDK 3.18.0 and JS SDK 9.11.0

Changes in [1.7.25-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.25-rc.1) (2021-04-07)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.24...v1.7.25-rc.1)

 * Upgrade to React SDK 3.18.0-rc.1 and JS SDK 9.11.0-rc.1
 * Translations update from Weblate
   [\#16882](https://github.com/vector-im/element-web/pull/16882)
 * Revert "Docker image: serve pre-compressed assets using gzip_static"
   [\#16838](https://github.com/vector-im/element-web/pull/16838)
 * Move native node modules documentation to element-desktop
   [\#16814](https://github.com/vector-im/element-web/pull/16814)
 * Add user settings for warn before exit
   [\#16781](https://github.com/vector-im/element-web/pull/16781)
 * Change ISSUE_TEMPLATE bold lines to proper headers
   [\#16768](https://github.com/vector-im/element-web/pull/16768)
 * Add example for deployment into Kubernetes
   [\#16447](https://github.com/vector-im/element-web/pull/16447)
 * Create bare-bones `PULL_REQUEST_TEMPLATE.md`
   [\#16770](https://github.com/vector-im/element-web/pull/16770)
 * Add webpack config and labs flag docs for voice messages
   [\#16705](https://github.com/vector-im/element-web/pull/16705)

Changes in [1.7.24](https://github.com/vector-im/element-web/releases/tag/v1.7.24) (2021-03-29)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.24-rc.1...v1.7.24)

 * Upgrade to React SDK 3.17.0 and JS SDK 9.10.0

Changes in [1.7.24-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.24-rc.1) (2021-03-25)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.23...v1.7.24-rc.1)

 * Upgrade to React SDK 3.17.0-rc.2 and JS SDK 9.10.0-rc.1
 * Translations update from Weblate
   [\#16766](https://github.com/vector-im/element-web/pull/16766)
 * Docker image: serve pre-compressed assets using gzip_static
   [\#16698](https://github.com/vector-im/element-web/pull/16698)
 * Fix style lint issues
   [\#16732](https://github.com/vector-im/element-web/pull/16732)
 * Updated expected webpack output in setup guide
   [\#16740](https://github.com/vector-im/element-web/pull/16740)
 * Docs for `loginForWelcome`
   [\#16468](https://github.com/vector-im/element-web/pull/16468)
 * Disable rageshake persistence if no logs would be submitted
   [\#16697](https://github.com/vector-im/element-web/pull/16697)

Changes in [1.7.23](https://github.com/vector-im/element-web/releases/tag/v1.7.23) (2021-03-15)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.23-rc.1...v1.7.23)

 * Upgrade to React SDK 3.16.0 and JS SDK 9.9.0

Changes in [1.7.23-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.23-rc.1) (2021-03-10)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.22...v1.7.23-rc.1)

 * Upgrade to React SDK 3.16.0-rc.2 and JS SDK 9.9.0-rc.1
 * Translations update from Weblate
   [\#16655](https://github.com/vector-im/element-web/pull/16655)
 * Improve docs for customisations
   [\#16652](https://github.com/vector-im/element-web/pull/16652)
 * Update triage guide to match the new label scheme
   [\#16612](https://github.com/vector-im/element-web/pull/16612)
 * Remove a couple useless 'use strict' calls
   [\#16650](https://github.com/vector-im/element-web/pull/16650)
 * Remove old conferencing doc
   [\#16648](https://github.com/vector-im/element-web/pull/16648)
 * Bump elliptic from 6.5.3 to 6.5.4
   [\#16644](https://github.com/vector-im/element-web/pull/16644)
 * Add option for audio live streaming
   [\#16604](https://github.com/vector-im/element-web/pull/16604)
 * Update velocity-animate dependency
   [\#16605](https://github.com/vector-im/element-web/pull/16605)
 * Add Edge to the supported tier
   [\#16611](https://github.com/vector-im/element-web/pull/16611)
 * Add multi language spell check
   [\#15851](https://github.com/vector-im/element-web/pull/15851)
 * Document feature_spaces
   [\#16538](https://github.com/vector-im/element-web/pull/16538)

Changes in [1.7.22](https://github.com/vector-im/element-web/releases/tag/v1.7.22) (2021-03-01)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.22-rc.1...v1.7.22)

## Security notice

Element Web 1.7.22 fixes (by upgrading to matrix-react-sdk 3.15.0) a moderate
severity issue (CVE-2021-21320) where the user content sandbox can be abused to
trick users into opening unexpected documents after several user interactions.
The content can be opened with a `blob` origin from the Matrix client, so it is
possible for a malicious document to access user messages and secrets. Thanks to
@keerok for responsibly disclosing this via Matrix's Security Disclosure Policy.

## All changes

 * Upgrade to React SDK 3.15.0 and JS SDK 9.8.0

Changes in [1.7.22-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.22-rc.1) (2021-02-24)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.21...v1.7.22-rc.1)

 * Upgrade to React SDK 3.15.0-rc.1 and JS SDK 9.8.0-rc.1
 * Translations update from Weblate
   [\#16529](https://github.com/vector-im/element-web/pull/16529)
 * Add hostSignup config for element.io clients
   [\#16515](https://github.com/vector-im/element-web/pull/16515)
 * VoIP virtual rooms, mkII
   [\#16442](https://github.com/vector-im/element-web/pull/16442)
 * Jitsi widget: Read room name from query parameters
   [\#16456](https://github.com/vector-im/element-web/pull/16456)
 * fix / sso: make sure to delete only loginToken after redirect
   [\#16415](https://github.com/vector-im/element-web/pull/16415)
 * Disable Countly
   [\#16433](https://github.com/vector-im/element-web/pull/16433)

Changes in [1.7.21](https://github.com/vector-im/element-web/releases/tag/v1.7.21) (2021-02-16)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.21-rc.1...v1.7.21)

 * Upgrade to React SDK 3.14.0 and JS SDK 9.7.0

Changes in [1.7.21-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.21-rc.1) (2021-02-10)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.20...v1.7.21-rc.1)

 * Upgrade to React SDK 3.14.0-rc.1 and JS SDK 9.7.0-rc.1
 * Translations update from Weblate
   [\#16427](https://github.com/vector-im/element-web/pull/16427)
 * Add RegExp dotAll feature test
   [\#16408](https://github.com/vector-im/element-web/pull/16408)
 * Fix Electron type merging
   [\#16405](https://github.com/vector-im/element-web/pull/16405)
 * README: remove Jenkins reference
   [\#16381](https://github.com/vector-im/element-web/pull/16381)
 * Enable PostCSS Calc in webpack builds
   [\#16307](https://github.com/vector-im/element-web/pull/16307)
 * Add configuration security best practices to the README.
   [\#16367](https://github.com/vector-im/element-web/pull/16367)
 * Upgrade matrix-widget-api
   [\#16347](https://github.com/vector-im/element-web/pull/16347)

Changes in [1.7.20](https://github.com/vector-im/element-web/releases/tag/v1.7.20) (2021-02-04)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.19...v1.7.20)

 * Upgrade to React SDK 3.13.1

Changes in [1.7.19](https://github.com/vector-im/element-web/releases/tag/v1.7.19) (2021-02-03)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.19-rc.1...v1.7.19)

 * Upgrade to React SDK 3.13.0 and JS SDK 9.6.0
 * [Release] Upgrade matrix-widget-api
   [\#16348](https://github.com/vector-im/element-web/pull/16348)

Changes in [1.7.19-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.19-rc.1) (2021-01-29)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.18...v1.7.19-rc.1)

 * Upgrade to React SDK 3.13.0-rc.1 and JS SDK 9.6.0-rc.1
 * Translations update from Weblate
   [\#16314](https://github.com/vector-im/element-web/pull/16314)
 * Use history replaceState instead of redirect for SSO flow
   [\#16292](https://github.com/vector-im/element-web/pull/16292)
 * Document the mobile guide toast option
   [\#16301](https://github.com/vector-im/element-web/pull/16301)
 * Update widget-api to beta.12
   [\#16303](https://github.com/vector-im/element-web/pull/16303)
 * Upgrade deps 2021-01
   [\#16294](https://github.com/vector-im/element-web/pull/16294)
 * Move to newer base image for Docker builds
   [\#16275](https://github.com/vector-im/element-web/pull/16275)
 * Docs for the VoIP translate pattern option
   [\#16236](https://github.com/vector-im/element-web/pull/16236)
 * Fix Riot->Element in permalinkPrefix docs
   [\#16227](https://github.com/vector-im/element-web/pull/16227)
 * Supply server_name for optional federation-capable Jitsi auth
   [\#16215](https://github.com/vector-im/element-web/pull/16215)
 * Fix Widget API version confusion
   [\#16212](https://github.com/vector-im/element-web/pull/16212)
 * Add Hebrew language
   [\#16210](https://github.com/vector-im/element-web/pull/16210)
 * Update widget-api to beta 11
   [\#16177](https://github.com/vector-im/element-web/pull/16177)
 * Fix develop Docker builds
   [\#16192](https://github.com/vector-im/element-web/pull/16192)
 * Skip the service worker for Electron
   [\#16157](https://github.com/vector-im/element-web/pull/16157)
 * Use isolated IPC API
   [\#16137](https://github.com/vector-im/element-web/pull/16137)

Changes in [1.7.18](https://github.com/vector-im/element-web/releases/tag/v1.7.18) (2021-01-26)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.17...v1.7.18)

 * Upgrade to React SDK 3.12.1 and JS SDK 9.5.1

Changes in [1.7.17](https://github.com/vector-im/element-web/releases/tag/v1.7.17) (2021-01-18)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.17-rc.1...v1.7.17)

 * Upgrade to React SDK 3.12.0 and JS SDK 9.5.0

Changes in [1.7.17-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.17-rc.1) (2021-01-13)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.16...v1.7.17-rc.1)

 * Upgrade to React SDK 3.12.0-rc.1 and JS SDK 9.5.0-rc.1
 * Translations update from Weblate
   [\#16131](https://github.com/vector-im/element-web/pull/16131)
 * webplatform: Fix notification closing
   [\#16028](https://github.com/vector-im/element-web/pull/16028)
 * Stop building code and types for Element layer
   [\#15999](https://github.com/vector-im/element-web/pull/15999)

Changes in [1.7.16](https://github.com/vector-im/element-web/releases/tag/v1.7.16) (2020-12-21)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.16-rc.1...v1.7.16)

 * Upgrade to React SDK 3.11.1 and JS SDK 9.4.1

Changes in [1.7.16-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.16-rc.1) (2020-12-16)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.15...v1.7.16-rc.1)

 * Upgrade to React SDK 3.11.0-rc.2 and JS SDK 9.4.0-rc.2
 * Translations update from Weblate
   [\#15979](https://github.com/vector-im/element-web/pull/15979)
 * Bump ini from 1.3.5 to 1.3.7
   [\#15949](https://github.com/vector-im/element-web/pull/15949)
 * Document pull request previews
   [\#15937](https://github.com/vector-im/element-web/pull/15937)
 * Improve asset path for KaTeX fonts
   [\#15939](https://github.com/vector-im/element-web/pull/15939)
 * Fix an important semicolon
   [\#15912](https://github.com/vector-im/element-web/pull/15912)
 * Bump highlight.js from 10.1.2 to 10.4.1
   [\#15898](https://github.com/vector-im/element-web/pull/15898)
 * Add gitter.im to room directory
   [\#15894](https://github.com/vector-im/element-web/pull/15894)
 * Extend Platform to support idpId for SSO flows
   [\#15771](https://github.com/vector-im/element-web/pull/15771)
 * Include KaTeX CSS as a dependency
   [\#15843](https://github.com/vector-im/element-web/pull/15843)

Changes in [1.7.15](https://github.com/vector-im/element-web/releases/tag/v1.7.15) (2020-12-07)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.15-rc.1...v1.7.15)

 * Upgrade to React SDK 3.10.0 and JS SDK 9.3.0

Changes in [1.7.15-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.15-rc.1) (2020-12-02)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.14...v1.7.15-rc.1)

 * Upgrade to React SDK 3.10.0-rc.1 and JS SDK 9.3.0-rc.1
 * Include KaTeX CSS as a dependency
   [\#15843](https://github.com/vector-im/element-web/pull/15843)
 * Translations update from Weblate
   [\#15884](https://github.com/vector-im/element-web/pull/15884)
 * added katex.min.css to webpack for math support (main PR in matrix-react-
   sdk)
   [\#15277](https://github.com/vector-im/element-web/pull/15277)
 * Rebrand package name and other details
   [\#15828](https://github.com/vector-im/element-web/pull/15828)
 * Bump highlight.js from 9.18.1 to 10.1.2
   [\#15819](https://github.com/vector-im/element-web/pull/15819)
 * Update branding of packaging artifacts
   [\#15810](https://github.com/vector-im/element-web/pull/15810)
 * Update the react-sdk reference in the lockfile
   [\#15814](https://github.com/vector-im/element-web/pull/15814)
 * Update widget API for good measure in Element Web
   [\#15812](https://github.com/vector-im/element-web/pull/15812)
 * Stop publishing Element to NPM
   [\#15811](https://github.com/vector-im/element-web/pull/15811)
 * Add inotify instance limit info to README
   [\#15795](https://github.com/vector-im/element-web/pull/15795)

Changes in [1.7.14](https://github.com/vector-im/element-web/releases/tag/v1.7.14) (2020-11-23)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.14-rc.1...v1.7.14)

 * Upgrade to React SDK 3.9.0 and JS SDK 9.2.0

Changes in [1.7.14-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.14-rc.1) (2020-11-18)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.13...v1.7.14-rc.1)

 * Upgrade to React SDK 3.9.0-rc.1 and JS SDK 9.2.0-rc.1
 * Translations update from Weblate
   [\#15767](https://github.com/vector-im/element-web/pull/15767)
 * Update the widget-api for element-web
   [\#15717](https://github.com/vector-im/element-web/pull/15717)

Changes in [1.7.13](https://github.com/vector-im/element-web/releases/tag/v1.7.13) (2020-11-09)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.13-rc.1...v1.7.13)

 * Upgrade to React SDK 3.8.0 and JS SDK 9.1.0

Changes in [1.7.13-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.13-rc.1) (2020-11-04)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.12...v1.7.13-rc.1)

 * Upgrade to React SDK 3.8.0-rc.1 and JS SDK 9.1.0-rc.1
 * Translations update from Weblate
   [\#15644](https://github.com/vector-im/element-web/pull/15644)
 * Add countly experiment to develop/nightly configs
   [\#15614](https://github.com/vector-im/element-web/pull/15614)
 * Add documentation for new UIFeature flag regarding room history settings
   [\#15592](https://github.com/vector-im/element-web/pull/15592)
 * Rename Docker repo in docs
   [\#15590](https://github.com/vector-im/element-web/pull/15590)
 * Fix Jitsi regressions with custom themes
   [\#15575](https://github.com/vector-im/element-web/pull/15575)

Changes in [1.7.12](https://github.com/vector-im/element-web/releases/tag/v1.7.12) (2020-10-28)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.11...v1.7.12)

 * Upgrade to React SDK 3.7.1 and JS SDK 9.0.1
 * [Release] Fix Jitsi regressions with custom themes
   [\#15577](https://github.com/vector-im/element-web/pull/15577)

Changes in [1.7.11](https://github.com/vector-im/element-web/releases/tag/v1.7.11) (2020-10-26)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.11-rc.1...v1.7.11)

 * Upgrade to React SDK 3.7.0 and JS SDK 9.0.0

Changes in [1.7.11-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.11-rc.1) (2020-10-21)
=========================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.10...v1.7.11-rc.1)

 * Upgrade to React SDK 3.7.0-rc.2 and JS SDK 9.0.0-rc.1
 * Update Weblate URL
   [\#15516](https://github.com/vector-im/element-web/pull/15516)
 * Translations update from Weblate
   [\#15517](https://github.com/vector-im/element-web/pull/15517)
 * Jitsi accept theme variable and restyle
   [\#15499](https://github.com/vector-im/element-web/pull/15499)
 * Skip editor confirmation of upgrades
   [\#15506](https://github.com/vector-im/element-web/pull/15506)
 * Adjust for new widget messaging APIs
   [\#15495](https://github.com/vector-im/element-web/pull/15495)
 * Use HTTPS_PROXY environment variable for downloading external_api.min…
   [\#15479](https://github.com/vector-im/element-web/pull/15479)
 * Document customisation points
   [\#15475](https://github.com/vector-im/element-web/pull/15475)
 * Don't fatally end the Jitsi widget when it's not being used as a widget
   [\#15466](https://github.com/vector-im/element-web/pull/15466)
 * electron-platform: Pass the user/devce id pair when initializing the event
   index.
   [\#15455](https://github.com/vector-im/element-web/pull/15455)

Changes in [1.7.10](https://github.com/vector-im/element-web/releases/tag/v1.7.10) (2020-10-20)
===============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.9...v1.7.10)

 * [Release] Adjust for new widget messaging APIs
   [\#15497](https://github.com/vector-im/element-web/pull/15497)
 * Upgrade to React SDK 3.6.1

Changes in [1.7.9](https://github.com/vector-im/element-web/releases/tag/v1.7.9) (2020-10-12)
=============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.9-rc.1...v1.7.9)

 * Upgrade to React SDK 3.6.0 and JS SDK 8.5.0

Changes in [1.7.9-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.9-rc.1) (2020-10-07)
=======================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.8...v1.7.9-rc.1)

 * Upgrade to React SDK 3.6.0-rc.1 and JS SDK 8.5.0-rc.1
 * Update from Weblate
   [\#15406](https://github.com/vector-im/element-web/pull/15406)
 * Update Jest and JSDOM
   [\#15402](https://github.com/vector-im/element-web/pull/15402)
 * Add support for dehydration/fallback keys
   [\#15398](https://github.com/vector-im/element-web/pull/15398)
 * Remove riot-bot from sample config
   [\#15376](https://github.com/vector-im/element-web/pull/15376)
 * Switch to using the Widget API SDK for Jitsi widgets
   [\#15102](https://github.com/vector-im/element-web/pull/15102)
 * Remove workbox
   [\#15352](https://github.com/vector-im/element-web/pull/15352)
 * Disable workbox when running in webpack dev server, not in dev mode
   [\#15345](https://github.com/vector-im/element-web/pull/15345)
 * Update Riot -> Element in contribute.json
   [\#15326](https://github.com/vector-im/element-web/pull/15326)
 * Update Riot -> Element in redeploy.py
   [\#15336](https://github.com/vector-im/element-web/pull/15336)
 * Update Riot -> Element in docs/feature-flags.md
   [\#15325](https://github.com/vector-im/element-web/pull/15325)
 * Update Riot -> Element in element.io/README.md
   [\#15327](https://github.com/vector-im/element-web/pull/15327)
 * Update Riot -> Element in VectorAuthFooter
   [\#15328](https://github.com/vector-im/element-web/pull/15328)
 * Update Riot -> Element in VectorEmbeddedPage
   [\#15329](https://github.com/vector-im/element-web/pull/15329)
 * Update Riot -> Element in docs/review.md
   [\#15330](https://github.com/vector-im/element-web/pull/15330)
 * Update Riot -> Element in welcome.html
   [\#15332](https://github.com/vector-im/element-web/pull/15332)
 * Update Riot -> Element in issues-burndown.pl
   [\#15333](https://github.com/vector-im/element-web/pull/15333)
 * Update Riot -> Element in redeploy.py
   [\#15334](https://github.com/vector-im/element-web/pull/15334)
 * Update Riot -> Element in index.ts
   [\#15335](https://github.com/vector-im/element-web/pull/15335)
 * Update Riot -> Element Web in issue templates
   [\#15324](https://github.com/vector-im/element-web/pull/15324)
 * Give the Jitsi widget an icon to help with discovery
   [\#15316](https://github.com/vector-im/element-web/pull/15316)
 * Jitsi widget wrapper updates for hangup button
   [\#15219](https://github.com/vector-im/element-web/pull/15219)
 * Tidy up Service Worker, only run Workbox in production
   [\#15271](https://github.com/vector-im/element-web/pull/15271)
 * Remove conference handler
   [\#15274](https://github.com/vector-im/element-web/pull/15274)
 * Rebrand the webpack pipeline for Element
   [\#15266](https://github.com/vector-im/element-web/pull/15266)
 * Replace dummy sw.js with pre-caching and runtime-caching workbox SW
   [\#15196](https://github.com/vector-im/element-web/pull/15196)

Changes in [1.7.8](https://github.com/vector-im/element-web/releases/tag/v1.7.8) (2020-09-28)
=============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.8-rc.1...v1.7.8)

 * Upgrade to React SDK 3.5.0 and JS SDK 8.4.1

Changes in [1.7.8-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.8-rc.1) (2020-09-23)
=======================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.7...v1.7.8-rc.1)

 * Upgrade to React SDK 3.5.0-rc.1 and JS SDK 8.4.0-rc.1
 * Update from Weblate
   [\#15262](https://github.com/vector-im/element-web/pull/15262)
 * Upgrade sanitize-html
   [\#15260](https://github.com/vector-im/element-web/pull/15260)
 * Document config for preferring Secure Backup setup methods
   [\#15251](https://github.com/vector-im/element-web/pull/15251)
 * Add end-user documentation for UI features
   [\#15190](https://github.com/vector-im/element-web/pull/15190)
 * Update git checkout instructions
   [\#15218](https://github.com/vector-im/element-web/pull/15218)
 * If no bug_report_endpoint_url, hide rageshaking from the App
   [\#15201](https://github.com/vector-im/element-web/pull/15201)
 * Bump node-fetch from 2.6.0 to 2.6.1
   [\#15153](https://github.com/vector-im/element-web/pull/15153)
 * Remove references to Travis CI
   [\#15137](https://github.com/vector-im/element-web/pull/15137)
 * Fix onNewScreen to use replace when going from roomId->roomAlias
   [\#15127](https://github.com/vector-im/element-web/pull/15127)
 * Enable Estonian in language menu
   [\#15136](https://github.com/vector-im/element-web/pull/15136)

Changes in [1.7.7](https://github.com/vector-im/element-web/releases/tag/v1.7.7) (2020-09-14)
=============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.6...v1.7.7)

 * Upgrade to React SDK 3.4.1

Changes in [1.7.6](https://github.com/vector-im/element-web/releases/tag/v1.7.6) (2020-09-14)
=============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.6-rc.1...v1.7.6)

 * Upgrade to React SDK 3.4.0 and JS SDK 8.3.0

Changes in [1.7.6-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.6-rc.1) (2020-09-09)
=======================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.5...v1.7.6-rc.1)

 * Upgrade to React SDK 3.4.0-rc.1 and JS SDK 8.3.0-rc.1
 * Update from Weblate
   [\#15125](https://github.com/vector-im/element-web/pull/15125)
 * Support usage of Jitsi widgets with "openidtoken-jwt" auth
   [\#15114](https://github.com/vector-im/element-web/pull/15114)
 * Fix eslint ts override tsx matching and delint
   [\#15064](https://github.com/vector-im/element-web/pull/15064)
 * Add testing to review guidelines
   [\#15050](https://github.com/vector-im/element-web/pull/15050)

Changes in [1.7.5](https://github.com/vector-im/element-web/releases/tag/v1.7.5) (2020-09-01)
=============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.5-rc.1...v1.7.5)

## Security notice

Element Web 1.7.5 fixes an issue where encrypted state events could break incoming call handling.
Thanks to @awesome-michael from Awesome Technologies for responsibly disclosing this via Matrix's
Security Disclosure Policy.

## All changes

 * Upgrade to React SDK 3.3.0 and JS SDK 8.2.0

Changes in [1.7.5-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.5-rc.1) (2020-08-26)
=======================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.4...v1.7.5-rc.1)

 * Upgrade to React SDK 3.3.0-rc.1 and JS SDK 8.2.0-rc.1
 * Update from Weblate
   [\#15045](https://github.com/vector-im/element-web/pull/15045)
 * Document .well-known E2EE secure backup setting
   [\#15003](https://github.com/vector-im/element-web/pull/15003)
 * Add docs for communities v2 prototyping feature flag
   [\#15013](https://github.com/vector-im/element-web/pull/15013)
 * Update links in README.md to point to Element
   [\#14973](https://github.com/vector-im/element-web/pull/14973)
 * Make kabyle translation available
   [\#15027](https://github.com/vector-im/element-web/pull/15027)
 * Change Riot to Element in readme
   [\#15016](https://github.com/vector-im/element-web/pull/15016)
 * Update links to element in the readme
   [\#15014](https://github.com/vector-im/element-web/pull/15014)
 * Link to Element in F-Droid as well
   [\#15002](https://github.com/vector-im/element-web/pull/15002)
 * Settings v3: Update documentation and configs for new feature flag behaviour
   [\#14986](https://github.com/vector-im/element-web/pull/14986)
 * Update jitsi.md with Element Android details
   [\#14952](https://github.com/vector-im/element-web/pull/14952)
 * TypeScript: enable es2019 lib for newer definitions
   [\#14983](https://github.com/vector-im/element-web/pull/14983)
 * Add reaction preview labs flags to develop
   [\#14979](https://github.com/vector-im/element-web/pull/14979)
 * Document new labs tweaks
   [\#14958](https://github.com/vector-im/element-web/pull/14958)

Changes in [1.7.4](https://github.com/vector-im/element-web/releases/tag/v1.7.4) (2020-08-17)
=============================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.4-rc.1...v1.7.4)

 * Upgrade to React SDK 3.2.0 and JS SDK 8.1.0

Changes in [1.7.4-rc.1](https://github.com/vector-im/element-web/releases/tag/v1.7.4-rc.1) (2020-08-13)
=======================================================================================================
[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.3...v1.7.4-rc.1)

 * Upgrade to React SDK 3.2.0-rc.1 and JS SDK 8.1.0-rc.1
 * Update policy links to element.io
   [\#14905](https://github.com/vector-im/element-web/pull/14905)
 * Update from Weblate
   [\#14949](https://github.com/vector-im/element-web/pull/14949)
 * Try to close notification on all platforms which support it, not just
   electron
   [\#14939](https://github.com/vector-im/element-web/pull/14939)
 * Update bug report submission URL
   [\#14903](https://github.com/vector-im/element-web/pull/14903)
 * Fix arm docker build
   [\#14522](https://github.com/vector-im/element-web/pull/14522)

Changes in [1.7.3](https://github.com/vector-im/element-web/releases/tag/v1.7.3) (2020-08-05)
=============================================================================================

## Security notice

Element Web 1.7.3 (as well as the earlier release 1.7.2) fixes an issue where
replying to a specially formatted message would make it seem like the replier
said something they did not. Thanks to Sorunome for responsibly disclosing this
via Matrix's Security Disclosure Policy.

Element Web 1.7.3 (as well as the earlier release 1.7.2) fixes an issue where an
unexpected language ID in a code block could cause Element to crash. Thanks to
SakiiR for responsibly disclosing this via Matrix's Security Disclosure Policy.

## All changes

[Full Changelog](https://github.com/vector-im/element-web/compare/v1.7.3-rc.1...v1.7.3)

 * Upgrade to React SDK 3.1.0 and JS SDK 8.0.1

Changes in [1.7.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.7.3-rc.1) (2020-07-31)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.7.2...v1.7.3-rc.1)

 * Upgrade to React SDK 3.1.0-rc.1 and JS SDK 8.0.1-rc.1
 * Make Lojban translation available
   [\#14703](https://github.com/vector-im/riot-web/pull/14703)
 * Update from Weblate
   [\#14841](https://github.com/vector-im/riot-web/pull/14841)
 * Remove redundant lint dependencies
   [\#14810](https://github.com/vector-im/riot-web/pull/14810)
 * Bump elliptic from 6.5.2 to 6.5.3
   [\#14826](https://github.com/vector-im/riot-web/pull/14826)
 * Update mobile config intercept URL
   [\#14796](https://github.com/vector-im/riot-web/pull/14796)
 * Fix typo in https://
   [\#14791](https://github.com/vector-im/riot-web/pull/14791)

Changes in [1.7.2](https://github.com/vector-im/riot-web/releases/tag/v1.7.2) (2020-07-27)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.7.1...v1.7.2)

 * Upgrade to React SDK 3.0.0 and JS SDK 8.0.0
 * Update from Weblate
   [\#14778](https://github.com/vector-im/riot-web/pull/14778)
 * Capitalize letters
   [\#14566](https://github.com/vector-im/riot-web/pull/14566)
 * Configure eslint package and fix lint issues
   [\#14673](https://github.com/vector-im/riot-web/pull/14673)
 * Riot → Element
   [\#14581](https://github.com/vector-im/riot-web/pull/14581)
 * Remove labs info for the new room list
   [\#14603](https://github.com/vector-im/riot-web/pull/14603)
 * Convince Webpack to use development on CI
   [\#14593](https://github.com/vector-im/riot-web/pull/14593)
 * Move dev dep to the right place
   [\#14572](https://github.com/vector-im/riot-web/pull/14572)
 * Bump lodash from 4.17.15 to 4.17.19
   [\#14552](https://github.com/vector-im/riot-web/pull/14552)
 * Update all mobile links to match marketing site
   [\#14541](https://github.com/vector-im/riot-web/pull/14541)

Changes in [1.7.1](https://github.com/vector-im/riot-web/releases/tag/v1.7.1) (2020-07-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.7.0...v1.7.1)

 * Upgrade to React SDK 2.10.1
 * Fix SSO session ID paramater
   [\#14544](https://github.com/vector-im/riot-web/pull/14544)
 * Run pngcrush on vector-icons
   [\#14488](https://github.com/vector-im/riot-web/pull/14488)
 * Fix hosting signup link
   [\#14502](https://github.com/vector-im/riot-web/pull/14502)
 * Use the right protocol for SSO URLs
   [\#14513](https://github.com/vector-im/riot-web/pull/14513)
 * Fix mstile-310x150 by renaming it
   [\#14485](https://github.com/vector-im/riot-web/pull/14485)
 * Update blog and twitter links to point to Element
   [\#14478](https://github.com/vector-im/riot-web/pull/14478)

Changes in [1.7.0](https://github.com/vector-im/riot-web/releases/tag/v1.7.0) (2020-07-15)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.8...v1.7.0)

 * App name changed from Riot to Element
 * Upgrade to React SDK 2.10.0
 * Remove redundant enum
   [\#14472](https://github.com/vector-im/riot-web/pull/14472)
 * Remove font scaling from labs
   [\#14355](https://github.com/vector-im/riot-web/pull/14355)
 * Update documentation and remove labs flag for new room list
   [\#14375](https://github.com/vector-im/riot-web/pull/14375)
 * Update from Weblate
   [\#14434](https://github.com/vector-im/riot-web/pull/14434)
 * Release the irc layout from labs
   [\#14350](https://github.com/vector-im/riot-web/pull/14350)
 * Fix welcomeBackgroundUrl array causing background to change during use
   [\#14368](https://github.com/vector-im/riot-web/pull/14368)
 * Be more explicit about type when calling platform startUpdater
   [\#14299](https://github.com/vector-im/riot-web/pull/14299)

Changes in [1.6.8](https://github.com/vector-im/riot-web/releases/tag/v1.6.8) (2020-07-03)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.8-rc.1...v1.6.8)

 * Upgrade to JS SDK 7.1.0 and React SDK 2.9.0

Changes in [1.6.8-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.6.8-rc.1) (2020-07-01)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.7...v1.6.8-rc.1)

 * Upgrade to JS SDK 7.1.0-rc.1 and React SDK 2.9.0-rc.1
 * Update from Weblate
   [\#14282](https://github.com/vector-im/riot-web/pull/14282)
 * Show a download completed toast in electron
   [\#14248](https://github.com/vector-im/riot-web/pull/14248)
 * Add the new spinner feature labs flag
   [\#14213](https://github.com/vector-im/riot-web/pull/14213)
 * Fix loading-test for SSO plaf changes
   [\#14212](https://github.com/vector-im/riot-web/pull/14212)
 * Fix spelling on startup error page
   [\#14199](https://github.com/vector-im/riot-web/pull/14199)
 * Document fonts in custom theme
   [\#14175](https://github.com/vector-im/riot-web/pull/14175)
 * Update from Weblate
   [\#14129](https://github.com/vector-im/riot-web/pull/14129)
 * ElectronPlatform: Implement the isRoomIndexed method.
   [\#13957](https://github.com/vector-im/riot-web/pull/13957)
 * ElectronPlatform: Add support to set and get the index user version.
   [\#14080](https://github.com/vector-im/riot-web/pull/14080)
 * Mark the new room list as ready for general testing
   [\#14102](https://github.com/vector-im/riot-web/pull/14102)

Changes in [1.6.7](https://github.com/vector-im/riot-web/releases/tag/v1.6.7) (2020-06-29)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.6...v1.6.7)

 * Upgrade to React SDK 2.8.1

Changes in [1.6.6](https://github.com/vector-im/riot-web/releases/tag/v1.6.6) (2020-06-23)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.6-rc.1...v1.6.6)

 * Upgrade to JS SDK 7.0.0 and React SDK 2.8.0

Changes in [1.6.6-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.6.6-rc.1) (2020-06-17)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.5...v1.6.6-rc.1)

 * Upgrade to JS SDK 7.0.0-rc.1 and React SDK 2.8.0-rc.1
 * Update from Weblate
   [\#14067](https://github.com/vector-im/riot-web/pull/14067)
 * Update from Weblate
   [\#14032](https://github.com/vector-im/riot-web/pull/14032)
 * Attempt to fix decoder ring for relative hosted riots
   [\#13987](https://github.com/vector-im/riot-web/pull/13987)
 * Upgrade deps
   [\#13952](https://github.com/vector-im/riot-web/pull/13952)
 * Fix riot-desktop manual update check getting stuck on Downloading...
   [\#13946](https://github.com/vector-im/riot-web/pull/13946)
 * Bump websocket-extensions from 0.1.3 to 0.1.4
   [\#13943](https://github.com/vector-im/riot-web/pull/13943)
 * Add e2ee-default:false docs
   [\#13914](https://github.com/vector-im/riot-web/pull/13914)
 * make IPC calls to get pickle key
   [\#13846](https://github.com/vector-im/riot-web/pull/13846)
 * fix loading test for new sso pattern
   [\#13913](https://github.com/vector-im/riot-web/pull/13913)
 * Fix login loop where the sso flow returns to `#/login`
   [\#13889](https://github.com/vector-im/riot-web/pull/13889)
 * Fix typo in docs
   [\#13905](https://github.com/vector-im/riot-web/pull/13905)
 * Remove cross-signing from labs
   [\#13904](https://github.com/vector-im/riot-web/pull/13904)
 * Add PWA Platform with PWA-specific badge controls
   [\#13890](https://github.com/vector-im/riot-web/pull/13890)
 * Modernizr check for subtle crypto as we require it all over the place
   [\#13828](https://github.com/vector-im/riot-web/pull/13828)

Changes in [1.6.5](https://github.com/vector-im/riot-web/releases/tag/v1.6.5) (2020-06-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.4...v1.6.5)

* Upgrade to JS SDK 6.2.2 and React SDK 2.7.2

Changes in [1.6.4](https://github.com/vector-im/riot-web/releases/tag/v1.6.4) (2020-06-05)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.3...v1.6.4)

* Upgrade to JS SDK 6.2.1 and React SDK 2.7.1

Changes in [1.6.3](https://github.com/vector-im/riot-web/releases/tag/v1.6.3) (2020-06-04)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.3-rc.1...v1.6.3)

## Security notice

Riot Web 1.6.3 fixes a vulnerability in single sign-on (SSO) deployments where Riot Web could be confused into sending authentication details to an attacker-controlled server. Thanks to Quentin Gliech for responsibly disclosing this via Matrix's Security Disclosure Policy.

## All changes

 * Fix login loop where the sso flow returns to `#/login` to release
   [\#13915](https://github.com/vector-im/riot-web/pull/13915)

Changes in [1.6.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.6.3-rc.1) (2020-06-02)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.2...v1.6.3-rc.1)

 * Upgrade to JS SDK 6.2.0-rc.1 and React SDK 2.7.0-rc.2
 * Get rid of welcome.html's Chat with Riot Bot button
   [\#13842](https://github.com/vector-im/riot-web/pull/13842)
 * Update from Weblate
   [\#13886](https://github.com/vector-im/riot-web/pull/13886)
 * Allow deferring of Update Toast until the next morning
   [\#13864](https://github.com/vector-im/riot-web/pull/13864)
 * Give contextual feedback for manual update check instead of banner
   [\#13862](https://github.com/vector-im/riot-web/pull/13862)
 * Add app-load doc
   [\#13834](https://github.com/vector-im/riot-web/pull/13834)
 * Update Modular hosting link
   [\#13777](https://github.com/vector-im/riot-web/pull/13777)
 * Replace New Version Bar with a Toast
   [\#13776](https://github.com/vector-im/riot-web/pull/13776)
 * Remove webpack-build-notifier from lockfile
   [\#13814](https://github.com/vector-im/riot-web/pull/13814)
 *  Add media queries and mobile viewport (#12142)
   [\#13818](https://github.com/vector-im/riot-web/pull/13818)
 * Fix @types/react conflict in matrix-react-sdk
   [\#13809](https://github.com/vector-im/riot-web/pull/13809)
 * Fix manual update checking, super in arrow funcs doesn't work
   [\#13808](https://github.com/vector-im/riot-web/pull/13808)
 * Update from Weblate
   [\#13806](https://github.com/vector-im/riot-web/pull/13806)
 * Convert platforms to Typescript
   [\#13756](https://github.com/vector-im/riot-web/pull/13756)
 * Fix EventEmitter typescript signature in node typings
   [\#13764](https://github.com/vector-im/riot-web/pull/13764)
 * Add docs and labs flag for new room list implementation
   [\#13675](https://github.com/vector-im/riot-web/pull/13675)
 * Add font scaling labs setting.
   [\#13352](https://github.com/vector-im/riot-web/pull/13352)
 * Add labs flag for alternate message layouts
   [\#13350](https://github.com/vector-im/riot-web/pull/13350)
 * Move dispatcher references in support of TypeScript conversion
   [\#13666](https://github.com/vector-im/riot-web/pull/13666)
 * Update from Weblate
   [\#13704](https://github.com/vector-im/riot-web/pull/13704)
 * Replace favico.js dependency with simplified variant grown from it
   [\#13649](https://github.com/vector-im/riot-web/pull/13649)
 * Remove Electron packaging scripts
   [\#13688](https://github.com/vector-im/riot-web/pull/13688)
 * Fix postcss order to allow mixin variables to work
   [\#13674](https://github.com/vector-im/riot-web/pull/13674)
 * Pass screenAfterLogin through SSO in the callback url
   [\#13650](https://github.com/vector-im/riot-web/pull/13650)

Changes in [1.6.2](https://github.com/vector-im/riot-web/releases/tag/v1.6.2) (2020-05-22)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.1...v1.6.2)

 * Upgrade to React SDK 2.6.1

Changes in [1.6.1](https://github.com/vector-im/riot-web/releases/tag/v1.6.1) (2020-05-19)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.1-rc.1...v1.6.1)

 * Upgrade to React SDK 2.6.0 and JS SDK 6.1.0

Changes in [1.6.1-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.6.1-rc.1) (2020-05-14)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0...v1.6.1-rc.1)

 * Upgrade to React SDK 2.6.0-rc.1 and JS SDK 6.1.0-rc.1
 * Update from Weblate
   [\#13673](https://github.com/vector-im/riot-web/pull/13673)
 * Add notranslate class to matrixchat to prevent translation by Google
   Translate
   [\#13669](https://github.com/vector-im/riot-web/pull/13669)
 * Added Anchor Link to the development of matrix sdk
   [\#13638](https://github.com/vector-im/riot-web/pull/13638)
 * Prefetch the formatting button mask svg images
   [\#13631](https://github.com/vector-im/riot-web/pull/13631)
 * use a different image in previews
   [\#13488](https://github.com/vector-im/riot-web/pull/13488)
 * Update from Weblate
   [\#13625](https://github.com/vector-im/riot-web/pull/13625)
 * Remove electron_app as we now have riot-desktop repo
   [\#13544](https://github.com/vector-im/riot-web/pull/13544)
 * add new images for PWA icons
   [\#13556](https://github.com/vector-im/riot-web/pull/13556)
 * Remove unused feature flag from config
   [\#13504](https://github.com/vector-im/riot-web/pull/13504)
 * Update from Weblate
   [\#13486](https://github.com/vector-im/riot-web/pull/13486)
 * Developer tool: convert rageshake error locations back to sourcecode
   locations
   [\#13357](https://github.com/vector-im/riot-web/pull/13357)
 * App load tweaks, improve error pages
   [\#13329](https://github.com/vector-im/riot-web/pull/13329)
 * Tweak default device name to be more compact
   [\#13465](https://github.com/vector-im/riot-web/pull/13465)
 * Tweak default device name on macOS
   [\#13460](https://github.com/vector-im/riot-web/pull/13460)
 * Update docs with custom theming changes
   [\#13406](https://github.com/vector-im/riot-web/pull/13406)
 * Update from Weblate
   [\#13395](https://github.com/vector-im/riot-web/pull/13395)
 * Remove docs and config for invite only padlocks
   [\#13374](https://github.com/vector-im/riot-web/pull/13374)
 * Revert "Add font scaling labs setting."
   [\#13351](https://github.com/vector-im/riot-web/pull/13351)
 * Expand feature flag docs to cover additional release channels
   [\#13341](https://github.com/vector-im/riot-web/pull/13341)
 * Optimized image assets by recompressing without affecting quality.
   [\#13034](https://github.com/vector-im/riot-web/pull/13034)
 * Add font scaling labs setting.
   [\#13199](https://github.com/vector-im/riot-web/pull/13199)
 * Remove encrypted message search feature flag
   [\#13325](https://github.com/vector-im/riot-web/pull/13325)
 * Fix `default_federate` settting description
   [\#13312](https://github.com/vector-im/riot-web/pull/13312)
 * Clarify that the .well-known method for Jitsi isn't available yet
   [\#13314](https://github.com/vector-im/riot-web/pull/13314)
 * add config option to tsc resolveJsonModule
   [\#13296](https://github.com/vector-im/riot-web/pull/13296)
 * Fix dispatcher import to be extension agnostic
   [\#13297](https://github.com/vector-im/riot-web/pull/13297)
 * Document more config options in config.md (fixes #13089)
   [\#13260](https://github.com/vector-im/riot-web/pull/13260)
 * Fix tests post-js-sdk-filters change
   [\#13295](https://github.com/vector-im/riot-web/pull/13295)
 * Make Jitsi download script a JS script
   [\#13227](https://github.com/vector-im/riot-web/pull/13227)
 * Use matrix-react-sdk type extensions as a base
   [\#13271](https://github.com/vector-im/riot-web/pull/13271)
 * Allow Riot Web to randomly pick welcome backgrounds
   [\#13235](https://github.com/vector-im/riot-web/pull/13235)
 * Update cross-signing feature docs and document fallback procedures
   [\#13224](https://github.com/vector-im/riot-web/pull/13224)

Changes in [1.6.0](https://github.com/vector-im/riot-web/releases/tag/v1.6.0) (2020-05-05)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0-rc.6...v1.6.0)

 * Cross-signing and E2EE by default for DMs and private rooms enabled
 * Upgrade to React SDK 2.5.0 and JS SDK 6.0.0

Changes in [1.6.0-rc.6](https://github.com/vector-im/riot-web/releases/tag/v1.6.0-rc.6) (2020-05-01)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0-rc.5...v1.6.0-rc.6)

 * Upgrade to React SDK 2.5.0-rc.6 and JS SDK 6.0.0-rc.2

Changes in [1.6.0-rc.5](https://github.com/vector-im/riot-web/releases/tag/v1.6.0-rc.5) (2020-04-30)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0-rc.4...v1.6.0-rc.5)

 * Upgrade to React SDK 2.5.0-rc.5 and JS SDK 6.0.0-rc.1
 * Remove feature flag docs from docs on release
   [\#13375](https://github.com/vector-im/riot-web/pull/13375)

Changes in [1.6.0-rc.4](https://github.com/vector-im/riot-web/releases/tag/v1.6.0-rc.4) (2020-04-23)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0-rc.3...v1.6.0-rc.4)

 * Upgrade to React SDK 2.5.0-rc.4 and JS SDK 5.3.1-rc.4

Changes in [1.6.0-rc.3](https://github.com/vector-im/riot-web/releases/tag/v1.6.0-rc.3) (2020-04-17)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0-rc.2...v1.6.0-rc.3)

 * Upgrade to React SDK 2.5.0-rc.3 and JS SDK 5.3.1-rc.3

Changes in [1.6.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.6.0-rc.2) (2020-04-16)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.6.0-rc.1...v1.6.0-rc.2)

 * Upgrade to React SDK 2.5.0-rc.2 and JS SDK 5.3.1-rc.2
 * Enable cross-signing / E2EE by default for DM without config changes

Changes in [1.6.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.6.0-rc.1) (2020-04-15)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.16-rc.1...v1.6.0-rc.1)

 * Enable cross-signing / E2EE by default for DM on release
   [\#13179](https://github.com/vector-im/riot-web/pull/13179)
 * Upgrade to React SDK 2.5.0-rc.1 and JS SDK 5.3.1-rc.1
 * Add instruction to resolve the inotify watch limit issue
   [\#13128](https://github.com/vector-im/riot-web/pull/13128)
 * docs: labs: add a pointer to config.md
   [\#13149](https://github.com/vector-im/riot-web/pull/13149)
 * Fix Electron SSO handling to support multiple profiles
   [\#13028](https://github.com/vector-im/riot-web/pull/13028)
 * Add riot-desktop shortcuts for forward/back matching browsers&slack
   [\#13133](https://github.com/vector-im/riot-web/pull/13133)
 * Allow rageshake to fail in init
   [\#13164](https://github.com/vector-im/riot-web/pull/13164)
 * Fix broken yarn install link in README.md
   [\#13125](https://github.com/vector-im/riot-web/pull/13125)
 * fix build:jitsi scripts crash caused by a missing folder
   [\#13122](https://github.com/vector-im/riot-web/pull/13122)
 * App load order changes to catch errors better
   [\#13095](https://github.com/vector-im/riot-web/pull/13095)
 * Upgrade deps
   [\#13080](https://github.com/vector-im/riot-web/pull/13080)

Changes in [1.5.16-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.16-rc.1) (2020-04-08)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.15...v1.5.16-rc.1)

 * Upgrade React SDK to 2.4.0-rc.1 and JS SDK to 5.3.0-rc.1
 * Update from Weblate
   [\#13078](https://github.com/vector-im/riot-web/pull/13078)
 * Mention Jitsi support at the .well-known level in Jitsi docs
   [\#13047](https://github.com/vector-im/riot-web/pull/13047)
 * Add new default home page fallback
   [\#13049](https://github.com/vector-im/riot-web/pull/13049)
 * App load order tweaks for code splitting
   [\#13032](https://github.com/vector-im/riot-web/pull/13032)
 * Add some docs about Jitsi widgets and Jitsi configuration
   [\#13027](https://github.com/vector-im/riot-web/pull/13027)
 * Bump minimist from 1.2.2 to 1.2.3 in /electron_app
   [\#13030](https://github.com/vector-im/riot-web/pull/13030)
 * Fix Electron mac-specific shortcut being registered on Web too.
   [\#13020](https://github.com/vector-im/riot-web/pull/13020)
 * Add a console warning that errors from Jitsi Meet are fine
   [\#12968](https://github.com/vector-im/riot-web/pull/12968)
 * Fix popout support for jitsi widgets
   [\#12975](https://github.com/vector-im/riot-web/pull/12975)
 * Some grammar and clarifications
   [\#12925](https://github.com/vector-im/riot-web/pull/12925)
 * Don't immediately remove notifications from notification trays
   [\#12861](https://github.com/vector-im/riot-web/pull/12861)
 * Remove welcome user from config
   [\#12894](https://github.com/vector-im/riot-web/pull/12894)

Changes in [1.5.15](https://github.com/vector-im/riot-web/releases/tag/v1.5.15) (2020-04-01)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.14...v1.5.15)

## Security notice

The `jitsi.html` widget wrapper introduced in Riot 1.5.14 could be used to extract user data by tricking the user into adding a custom widget or opening a link in the browser used to run Riot. Jitsi widgets created through Riot UI do not pose a risk and do not need to be recreated.

It is important to purge any copies of Riot 1.5.14 so that the vulnerable `jitsi.html` wrapper from that version is no longer accessible.

## All changes

 * Upgrade React SDK to 2.3.1 for Jitsi fixes
 * Fix popout support for jitsi widgets
   [\#12980](https://github.com/vector-im/riot-web/pull/12980)

Changes in [1.5.14](https://github.com/vector-im/riot-web/releases/tag/v1.5.14) (2020-03-30)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.14-rc.1...v1.5.14)

 * Upgrade JS SDK to 5.2.0 and React SDK to 2.3.0

Changes in [1.5.14-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.14-rc.1) (2020-03-26)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.13...v1.5.14-rc.1)

 * Upgrade JS SDK to 5.2.0-rc.1 and React SDK to 2.3.0-rc.1
 * Update from Weblate
   [\#12890](https://github.com/vector-im/riot-web/pull/12890)
 * App load tweaks
   [\#12869](https://github.com/vector-im/riot-web/pull/12869)
 * Add review policy doc
   [\#12730](https://github.com/vector-im/riot-web/pull/12730)
 * Fix artifact searching in redeployer
   [\#12875](https://github.com/vector-im/riot-web/pull/12875)
 * Fix Jitsi wrapper being large by getting the config from elsewhere
   [\#12845](https://github.com/vector-im/riot-web/pull/12845)
 * Add webpack stats which will be used by CI and stored to artifacts
   [\#12832](https://github.com/vector-im/riot-web/pull/12832)
 * Revert "Remove useless app preloading from Jitsi widget wrapper"
   [\#12842](https://github.com/vector-im/riot-web/pull/12842)
 * Remove useless app preloading from Jitsi widget wrapper
   [\#12836](https://github.com/vector-im/riot-web/pull/12836)
 * Update from Weblate
   [\#12829](https://github.com/vector-im/riot-web/pull/12829)
 * Fix version for Docker builds
   [\#12799](https://github.com/vector-im/riot-web/pull/12799)
 * Register Mac electron specific Cmd+, shortcut to User Settings
   [\#12800](https://github.com/vector-im/riot-web/pull/12800)
 * Use a local widget wrapper for Jitsi calls
   [\#12780](https://github.com/vector-im/riot-web/pull/12780)
 * Delete shortcuts.md
   [\#12786](https://github.com/vector-im/riot-web/pull/12786)
 * Remove remainders of gemini-scrollbar and react-gemini-scrollbar
   [\#12756](https://github.com/vector-im/riot-web/pull/12756)
 * Update electron to v7.1.14
   [\#12762](https://github.com/vector-im/riot-web/pull/12762)
 * Add url tests to Modernizr
   [\#12735](https://github.com/vector-im/riot-web/pull/12735)
 * ElectronPlatform: Add support to remove events from the event index.
   [\#12703](https://github.com/vector-im/riot-web/pull/12703)
 * Bump minimist from 1.2.0 to 1.2.2 in /electron_app
   [\#12744](https://github.com/vector-im/riot-web/pull/12744)
 * Add docs and flag for custom theme support
   [\#12731](https://github.com/vector-im/riot-web/pull/12731)
 * Declare jsx in tsconfig for IDEs
   [\#12716](https://github.com/vector-im/riot-web/pull/12716)
 * Remove stuff that yarn install doesn't think we need
   [\#12713](https://github.com/vector-im/riot-web/pull/12713)
 * yarn upgrade
   [\#12691](https://github.com/vector-im/riot-web/pull/12691)
 * Support TypeScript for React components
   [\#12696](https://github.com/vector-im/riot-web/pull/12696)

Changes in [1.5.13](https://github.com/vector-im/riot-web/releases/tag/v1.5.13) (2020-03-17)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.13-rc.1...v1.5.13)

 * Upgrade to JS SDK 5.1.1 and React SDK 2.2.3

Changes in [1.5.13-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.13-rc.1) (2020-03-11)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.12...v1.5.13-rc.1)

 * Update from Weblate
   [\#12688](https://github.com/vector-im/riot-web/pull/12688)
 * Fix Docker image version for develop builds
   [\#12670](https://github.com/vector-im/riot-web/pull/12670)
 * docker: optimize custom sdk builds
   [\#12612](https://github.com/vector-im/riot-web/pull/12612)
 * riot-desktop open SSO in browser so user doesn't have to auth twice
   [\#12590](https://github.com/vector-im/riot-web/pull/12590)
 * Fix SSO flows for electron 8.0.2 by re-breaking will-navigate
   [\#12585](https://github.com/vector-im/riot-web/pull/12585)
 * index.html: Place noscript on top of the page
   [\#12563](https://github.com/vector-im/riot-web/pull/12563)
 * Remove will-navigate comment after Electron fix
   [\#12561](https://github.com/vector-im/riot-web/pull/12561)
 * Update loading test for JS SDK IDB change
   [\#12552](https://github.com/vector-im/riot-web/pull/12552)
 * Upgrade deps
   [\#12528](https://github.com/vector-im/riot-web/pull/12528)

Changes in [1.5.12](https://github.com/vector-im/riot-web/releases/tag/v1.5.12) (2020-03-04)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.11...v1.5.12)

 * Upgrade to React SDK 2.2.1
 * Revert to Electron 7.1.12 to fix Arch Linux tray icon
 * Fix image download links so they open in a new tab

Changes in [1.5.11](https://github.com/vector-im/riot-web/releases/tag/v1.5.11) (2020-03-02)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.11-rc.1...v1.5.11)

 * Upgrade to JS SDK 5.1.0 and React SDK 2.2.0
 * Fix SSO flows for Electron 8.0.2 by disabling will-navigate
   [\#12585](https://github.com/vector-im/riot-web/pull/12585)

Changes in [1.5.11-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.11-rc.1) (2020-02-26)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.10...v1.5.11-rc.1)

 * Upgrade to JS SDK 5.1.0-rc.1 and React SDK 2.2.0-rc.1
 * Change Windows signing to warning when missing token
   [\#12523](https://github.com/vector-im/riot-web/pull/12523)
 * Modernizr remove t3st/es6/contains
   [\#12524](https://github.com/vector-im/riot-web/pull/12524)
 * Switch out any eval-using Modernizr rules
   [\#12519](https://github.com/vector-im/riot-web/pull/12519)
 * Update from Weblate
   [\#12522](https://github.com/vector-im/riot-web/pull/12522)
 * Notify electron of language changes
   [\#12487](https://github.com/vector-im/riot-web/pull/12487)
 * Relax macOS notarisation check to print a warning
   [\#12503](https://github.com/vector-im/riot-web/pull/12503)
 * Clarify supported tier means desktop OSes
   [\#12486](https://github.com/vector-im/riot-web/pull/12486)
 * Use noreferrer in addition to noopener for edge case browsers
   [\#12477](https://github.com/vector-im/riot-web/pull/12477)
 * Document start / end composer shortcuts
   [\#12466](https://github.com/vector-im/riot-web/pull/12466)
 * Update from Weblate
   [\#12480](https://github.com/vector-im/riot-web/pull/12480)
 * Remove buildkite pipeline
   [\#12464](https://github.com/vector-im/riot-web/pull/12464)
 * Remove exec so release script continues
   [\#12435](https://github.com/vector-im/riot-web/pull/12435)
 * Use Persistent Storage where possible
   [\#12425](https://github.com/vector-im/riot-web/pull/12425)

Changes in [1.5.10](https://github.com/vector-im/riot-web/releases/tag/v1.5.10) (2020-02-19)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.9...v1.5.10)

 * Get rid of dependence on usercontent.riot.im
   [\#12292](https://github.com/vector-im/riot-web/pull/12292)
 * Add experimental support tier
   [\#12377](https://github.com/vector-im/riot-web/pull/12377)

Changes in [1.5.9](https://github.com/vector-im/riot-web/releases/tag/v1.5.9) (2020-02-17)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.9-rc.1...v1.5.9)

 * Automate SDK dep upgrades for release
   [\#12374](https://github.com/vector-im/riot-web/pull/12374)

Changes in [1.5.9-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.9-rc.1) (2020-02-13)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.8...v1.5.9-rc.1)

 * Upgrade JS SDK to 5.0.0-rc.1 and React SDK 2.1.0-rc.2
 * Update from Weblate
   [\#12354](https://github.com/vector-im/riot-web/pull/12354)
 * Add top left menu shortcut
   [\#12310](https://github.com/vector-im/riot-web/pull/12310)
 * Remove modernizr rules for features on which we only soft depend
   [\#12272](https://github.com/vector-im/riot-web/pull/12272)
 * Embed CSP meta tag and stop using script-src unsafe-inline
   [\#12258](https://github.com/vector-im/riot-web/pull/12258)
 * Add contribute.json
   [\#12251](https://github.com/vector-im/riot-web/pull/12251)
 * Improve Browser checks
   [\#12232](https://github.com/vector-im/riot-web/pull/12232)
 * Document padlock flag
   [\#12173](https://github.com/vector-im/riot-web/pull/12173)
 * Enable cross-signing on /develop
   [\#12126](https://github.com/vector-im/riot-web/pull/12126)
 * Switch back to legacy decorators
   [\#12110](https://github.com/vector-im/riot-web/pull/12110)
 * Update babel targets
   [\#12102](https://github.com/vector-im/riot-web/pull/12102)
 * Install deps for linting
   [\#12076](https://github.com/vector-im/riot-web/pull/12076)
 * Update from Weblate
   [\#12062](https://github.com/vector-im/riot-web/pull/12062)
 * Change to minimal Webpack output
   [\#12049](https://github.com/vector-im/riot-web/pull/12049)
 * Remove docs for new invite dialog labs feature
   [\#12015](https://github.com/vector-im/riot-web/pull/12015)
 * ElectronPlatform: Add the indexSize method.
   [\#11529](https://github.com/vector-im/riot-web/pull/11529)
 * ElectronPlatform: Add the ability to load file events from the event index
   [\#11907](https://github.com/vector-im/riot-web/pull/11907)
 * Fix the remainder of the cookie links
   [\#12008](https://github.com/vector-im/riot-web/pull/12008)
 * Use bash in Docker scripts
   [\#12001](https://github.com/vector-im/riot-web/pull/12001)
 * Use debian to build the Docker image
   [\#11999](https://github.com/vector-im/riot-web/pull/11999)
 * Update cookie policy urls on /app and /develop config.json
   [\#11998](https://github.com/vector-im/riot-web/pull/11998)
 * BuildKite: Only deploy to /develop if everything else passed
   [\#11996](https://github.com/vector-im/riot-web/pull/11996)
 * Add docs for admin report content message
   [\#11995](https://github.com/vector-im/riot-web/pull/11995)
 * Load as little as possible in index.js for the skinner
   [\#11959](https://github.com/vector-im/riot-web/pull/11959)
 * Fix webpack config (by stealing Dave's config)
   [\#11956](https://github.com/vector-im/riot-web/pull/11956)
 * Force Jest to resolve the js-sdk and react-sdk to src directories
   [\#11954](https://github.com/vector-im/riot-web/pull/11954)
 * Fix build to not babel modules inside js/react sdk
   [\#11949](https://github.com/vector-im/riot-web/pull/11949)
 * Fix webpack to babel js-sdk & react-sdk but no other deps
   [\#11944](https://github.com/vector-im/riot-web/pull/11944)

Changes in [1.5.8](https://github.com/vector-im/riot-web/releases/tag/v1.5.8) (2020-01-27)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.8-rc.2...v1.5.8)

 * Fixes for alias display and copy / paste on composer

Changes in [1.5.8-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.5.8-rc.2) (2020-01-22)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.8-rc.1...v1.5.8-rc.2)

 * Fix incorrect version of react-sdk

Changes in [1.5.8-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.8-rc.1) (2020-01-22)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.7...v1.5.8-rc.1)

This version contains an upgrade to the cryptography database
version. Once users run this version, their session's indexeddb
store will be upgraded and older version of Riot will no longer
be able to read it. Users will have to log out and log in if
the version of Riot is downgraded back to a previous version.

 * Fix webpack config (by stealing Dave's config)
   [\#11994](https://github.com/vector-im/riot-web/pull/11994)
 * Fix webpack to babel js-sdk & react-sdk but no other deps
   [\#11947](https://github.com/vector-im/riot-web/pull/11947)
 * Update from Weblate
   [\#11934](https://github.com/vector-im/riot-web/pull/11934)
 * Fix rageshake post-sourcemaps
   [\#11926](https://github.com/vector-im/riot-web/pull/11926)
 * Fix yarn start concurrent commands
   [\#11895](https://github.com/vector-im/riot-web/pull/11895)
 * Run the react-sdk reskindexer for developers
   [\#11894](https://github.com/vector-im/riot-web/pull/11894)
 * Update labs documentation for feature_ftue_dms given new scope
   [\#11893](https://github.com/vector-im/riot-web/pull/11893)
 * Fix indentation on webpack config and make sourcemapped files legible
   [\#11892](https://github.com/vector-im/riot-web/pull/11892)
 * Remove spinner check
   [\#11891](https://github.com/vector-im/riot-web/pull/11891)
 * Don't minifiy builds of develop through CI packaging
   [\#11867](https://github.com/vector-im/riot-web/pull/11867)
 * Use Jest for tests
   [\#11869](https://github.com/vector-im/riot-web/pull/11869)
 * Support application/wasm in Docker image
   [\#11858](https://github.com/vector-im/riot-web/pull/11858)
 * Fix sourcemaps by refactoring the build system
   [\#11843](https://github.com/vector-im/riot-web/pull/11843)
 * Disable event indexing on develop
   [\#11850](https://github.com/vector-im/riot-web/pull/11850)
 * Updated blog url
   [\#11792](https://github.com/vector-im/riot-web/pull/11792)
 * Enable and document presence in room list feature flag
   [\#11829](https://github.com/vector-im/riot-web/pull/11829)
 * Add stub service worker so users can install on desktop with Chrome
   [\#11774](https://github.com/vector-im/riot-web/pull/11774)
 * Update from Weblate
   [\#11826](https://github.com/vector-im/riot-web/pull/11826)
 * Sourcemaps: develop -> feature branch
   [\#11802](https://github.com/vector-im/riot-web/pull/11802)
 * Update build scripts for new process
   [\#11801](https://github.com/vector-im/riot-web/pull/11801)
 * Make the webpack config work for us
   [\#11712](https://github.com/vector-im/riot-web/pull/11712)
 * Updates URL for Electron Command Line Switches
   [\#11810](https://github.com/vector-im/riot-web/pull/11810)
 * Import from src/ for the react-sdk and js-sdk
   [\#11714](https://github.com/vector-im/riot-web/pull/11714)
 * Convert components to ES6 exports
   [\#11713](https://github.com/vector-im/riot-web/pull/11713)
 * Remove now-retired package.json property
   [\#11660](https://github.com/vector-im/riot-web/pull/11660)

Changes in [1.5.7](https://github.com/vector-im/riot-web/releases/tag/v1.5.7) (2020-01-13)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.7-rc.2...v1.5.7)

 * Enable and document presence in room list feature flag
   [\#11830](https://github.com/vector-im/riot-web/pull/11830)

Changes in [1.5.7-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.5.7-rc.2) (2020-01-08)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.7-rc.1...v1.5.7-rc.2)

 * Update to react-sdk rc.2 to fix build

Changes in [1.5.7-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.7-rc.1) (2020-01-06)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.6...v1.5.7-rc.1)

 * Update from Weblate
   [\#11784](https://github.com/vector-im/riot-web/pull/11784)
 * Add docs for feature_bridge_state flag
   [\#11778](https://github.com/vector-im/riot-web/pull/11778)
 * Add docs for feature_ftue_dms flag
   [\#11758](https://github.com/vector-im/riot-web/pull/11758)
 * Fix version file for Docker images
   [\#11721](https://github.com/vector-im/riot-web/pull/11721)
 * Add accelerators to context menu options like cut&paste in electron
   [\#11690](https://github.com/vector-im/riot-web/pull/11690)
 * electron-main: Provide a better error message if Seshat isn't installed.
   [\#11691](https://github.com/vector-im/riot-web/pull/11691)
 * Update from Weblate
   [\#11672](https://github.com/vector-im/riot-web/pull/11672)
 * Remove babel-plugin-transform-async-to-bluebird
   [\#11662](https://github.com/vector-im/riot-web/pull/11662)
 * Clarify which versions of what we support
   [\#11658](https://github.com/vector-im/riot-web/pull/11658)
 * Remove the code that calls the origin migrator
   [\#11631](https://github.com/vector-im/riot-web/pull/11631)
 * yarn upgrade
   [\#11617](https://github.com/vector-im/riot-web/pull/11617)
 * Remove draft-js dependency
   [\#11616](https://github.com/vector-im/riot-web/pull/11616)

Changes in [1.5.6](https://github.com/vector-im/riot-web/releases/tag/v1.5.6) (2019-12-09)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.6-rc.1...v1.5.6)

 * No changes since rc.1

Changes in [1.5.6-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.6-rc.1) (2019-12-04)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.5...v1.5.6-rc.1)

 * Update Lithuanian language name
   [\#11599](https://github.com/vector-im/riot-web/pull/11599)
 * Enable more languages
   [\#11592](https://github.com/vector-im/riot-web/pull/11592)
 * Fix Docker build for develop and publish a /version file
   [\#11588](https://github.com/vector-im/riot-web/pull/11588)
 * Remove unused translations
   [\#11540](https://github.com/vector-im/riot-web/pull/11540)
 * Update from Weblate
   [\#11591](https://github.com/vector-im/riot-web/pull/11591)
 * Update riot.im enable_presence_by_hs_url for new matrix.org client URL
   [\#11565](https://github.com/vector-im/riot-web/pull/11565)
 * Remove mention of vector.im as default identity server on mobile guide
   [\#11544](https://github.com/vector-im/riot-web/pull/11544)
 * Clean up and standardise app config
   [\#11549](https://github.com/vector-im/riot-web/pull/11549)
 * make it clear that seshat requires electron-build-env (at least on macOS)
   [\#11527](https://github.com/vector-im/riot-web/pull/11527)
 * Add postcss-easings
   [\#11521](https://github.com/vector-im/riot-web/pull/11521)
 * ElectronPlatform: Add support for a event index using Seshat.
   [\#11125](https://github.com/vector-im/riot-web/pull/11125)
 * Sign all of the Windows executable files
   [\#11516](https://github.com/vector-im/riot-web/pull/11516)
 * Clarify that cross-signing is in development
   [\#11493](https://github.com/vector-im/riot-web/pull/11493)
 * get rid of bluebird
   [\#11301](https://github.com/vector-im/riot-web/pull/11301)
 * Update from Weblate
   [\#11488](https://github.com/vector-im/riot-web/pull/11488)
 * Add note in README about self-hosted riot installs requiring custom caching
   headers
   [\#8702](https://github.com/vector-im/riot-web/pull/8702)
 * De-dup theming code
   [\#11445](https://github.com/vector-im/riot-web/pull/11445)
 * Add eslint-plugin-jest because we inherit js-sdk's eslintrc and it wants
   [\#11448](https://github.com/vector-im/riot-web/pull/11448)

Changes in [1.5.5](https://github.com/vector-im/riot-web/releases/tag/v1.5.5) (2019-11-27)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.4...v1.5.5)

* Upgrade to JS SDK 2.5.4 to relax identity server discovery and E2EE debugging
* Upgrade to React SDK 1.7.4 to fix override behaviour of themes
* Clarify that cross-signing is in development
* Sign all of the Windows executable files

Changes in [1.5.4](https://github.com/vector-im/riot-web/releases/tag/v1.5.4) (2019-11-25)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.4-rc.2...v1.5.4)

 * No changes since rc.2

Changes in [1.5.4-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.5.4-rc.2) (2019-11-22)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.4-rc.1...v1.5.4-rc.2)

 * react-sdk rc.2 to fix an error in Safari and some cosmetic
   bugs

Changes in [1.5.4-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.4-rc.1) (2019-11-20)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.3...v1.5.4-rc.1)

 * Add doc for custom themes
   [\#11444](https://github.com/vector-im/riot-web/pull/11444)
 * Use new theme API in react-sdk
   [\#11442](https://github.com/vector-im/riot-web/pull/11442)
 * preload warning triangle
   [\#11441](https://github.com/vector-im/riot-web/pull/11441)
 * Update from Weblate
   [\#11440](https://github.com/vector-im/riot-web/pull/11440)
 * Add entitlements file for mic & camera permissions on macOS
   [\#11435](https://github.com/vector-im/riot-web/pull/11435)
 * Fix error/exception in electron signing script
   [\#11429](https://github.com/vector-im/riot-web/pull/11429)
 * Merge the `feature_user_info_panel` flag into `feature_dm_verification`
   [\#11426](https://github.com/vector-im/riot-web/pull/11426)
 * Let the user's homeserver config override the build config
   [\#11409](https://github.com/vector-im/riot-web/pull/11409)
 * Add cross-signing labs flag to develop and document
   [\#11408](https://github.com/vector-im/riot-web/pull/11408)
 * Update from Weblate
   [\#11405](https://github.com/vector-im/riot-web/pull/11405)
 * Trigger a theme change on startup, not just a tint change
   [\#11381](https://github.com/vector-im/riot-web/pull/11381)
 * Perform favicon updates twice in Chrome
   [\#11375](https://github.com/vector-im/riot-web/pull/11375)
 * Add labs documentation for Mjolnir
   [\#11275](https://github.com/vector-im/riot-web/pull/11275)
 * Add description of user info feature in labs doc
   [\#11360](https://github.com/vector-im/riot-web/pull/11360)
 * Update from Weblate
   [\#11359](https://github.com/vector-im/riot-web/pull/11359)
 * Add DM verification feature to labs.md
   [\#11356](https://github.com/vector-im/riot-web/pull/11356)
 * Add feature_dm_verification to labs
   [\#11355](https://github.com/vector-im/riot-web/pull/11355)
 * Document feature flag process
   [\#11341](https://github.com/vector-im/riot-web/pull/11341)
 * Remove unused feature flags
   [\#11343](https://github.com/vector-im/riot-web/pull/11343)

Changes in [1.5.3](https://github.com/vector-im/riot-web/releases/tag/v1.5.3) (2019-11-06)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.2...v1.5.3)

 * Remove the 'auto hide menu bar' option on Mac
   [\#11326](https://github.com/vector-im/riot-web/pull/11326)
 * Expose feature_user_info_panel on riot.im/develop
   [\#11304](https://github.com/vector-im/riot-web/pull/11304)
 * Upgrade electron-notarize
   [\#11312](https://github.com/vector-im/riot-web/pull/11312)
 * Fix close window behaviour on Macos
   [\#11309](https://github.com/vector-im/riot-web/pull/11309)
 * Merge: Add dependency to eslint-plugin-react-hooks as react-sdk did
   [\#11307](https://github.com/vector-im/riot-web/pull/11307)
 * Add dependency to eslint-plugin-react-hooks as react-sdk did
   [\#11306](https://github.com/vector-im/riot-web/pull/11306)
 * Update from Weblate
   [\#11300](https://github.com/vector-im/riot-web/pull/11300)

Changes in [1.5.2](https://github.com/vector-im/riot-web/releases/tag/v1.5.2) (2019-11-04)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.1...v1.5.2)

 * Fix close window behaviour on Macos
   [\#11311](https://github.com/vector-im/riot-web/pull/11311)

Changes in [1.5.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.1) (2019-11-04)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.1-rc.2...v1.5.1)

 * No changes since rc.2

Changes in [1.5.1-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.5.1-rc.2) (2019-11-01)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.1-rc.1...v1.5.1-rc.2)

 * Updated react-sdk with fix for bug that caused room filtering to
   omit results.

Changes in [1.5.1-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.1-rc.1) (2019-10-30)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.0...v1.5.1-rc.1)

 * Add ability to hide tray icon on non-Mac (which has no tray icon)
   [\#11258](https://github.com/vector-im/riot-web/pull/11258)
 * Fix bug preventing display from sleeping after a call
   [\#11264](https://github.com/vector-im/riot-web/pull/11264)
 * Remove mention of CI scripts from docs
   [\#11257](https://github.com/vector-im/riot-web/pull/11257)
 * Fix skinning replaces being broken since being rewritten as React FC's
   [\#11254](https://github.com/vector-im/riot-web/pull/11254)
 * Update config docs about identity servers
   [\#11249](https://github.com/vector-im/riot-web/pull/11249)
 * Remove unneeded help about identity servers
   [\#11248](https://github.com/vector-im/riot-web/pull/11248)
 * Update from Weblate
   [\#11243](https://github.com/vector-im/riot-web/pull/11243)
 * Update sample config for new matrix.org CS API URL
   [\#11207](https://github.com/vector-im/riot-web/pull/11207)
 * clarify where the e2e tests are located
   [\#11115](https://github.com/vector-im/riot-web/pull/11115)
 * Update from Weblate
   [\#11171](https://github.com/vector-im/riot-web/pull/11171)
 * Prevent referrers from being sent
   [\#6155](https://github.com/vector-im/riot-web/pull/6155)
 * Add darkModeSupport to allow dark themed title bar.
   [\#11140](https://github.com/vector-im/riot-web/pull/11140)
 * Fix the label of Turkish language
   [\#11124](https://github.com/vector-im/riot-web/pull/11124)
 * Update default HS config to match well-known
   [\#11112](https://github.com/vector-im/riot-web/pull/11112)

Changes in [1.5.0](https://github.com/vector-im/riot-web/releases/tag/v1.5.0) (2019-10-18)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.5.0-rc.1...v1.5.0)

 * Upgrade to JS SDK v2.4.2 and React SDK v1.7.0
 * Port Windows signing and macOS notarization to release
   [\#11158](https://github.com/vector-im/riot-web/pull/11158)
 * Sign main Windows executable
   [\#11126](https://github.com/vector-im/riot-web/pull/11126)
 * Notarise the macOS app
   [\#11119](https://github.com/vector-im/riot-web/pull/11119)

Changes in [1.5.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.5.0-rc.1) (2019-10-09)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.4.2...v1.5.0-rc.1)

 * Update from Weblate
   [\#11104](https://github.com/vector-im/riot-web/pull/11104)
 * Bump Olm to 3.1.4 for olm_session_describe
   [\#11103](https://github.com/vector-im/riot-web/pull/11103)
 * Enable Webpack production mode for start:js:prod
   [\#11098](https://github.com/vector-im/riot-web/pull/11098)
 * add settingDefaults to sample config
   [\#9919](https://github.com/vector-im/riot-web/pull/9919)
 * Add config.json copy instruction to 'Development' as well
   [\#11062](https://github.com/vector-im/riot-web/pull/11062)
 * Revert "Run yarn upgrade"
   [\#11055](https://github.com/vector-im/riot-web/pull/11055)
 * Run yarn upgrade
   [\#11050](https://github.com/vector-im/riot-web/pull/11050)
 * Request persistent storage on Electron
   [\#11052](https://github.com/vector-im/riot-web/pull/11052)
 * Remove docs for CIDER feature
   [\#11047](https://github.com/vector-im/riot-web/pull/11047)

Changes in [1.4.2](https://github.com/vector-im/riot-web/releases/tag/v1.4.2) (2019-10-04)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.4.2-rc.1...v1.4.2)

 * Document troubleshooting for memory leaks and getting profiles
   [\#11031](https://github.com/vector-im/riot-web/pull/11031)

Changes in [1.4.2-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.4.2-rc.1) (2019-10-02)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.4.1...v1.4.2-rc.1)

 * Custom themes MVP
   [\#11017](https://github.com/vector-im/riot-web/pull/11017)
 * Document permalinkPrefix setting
   [\#11007](https://github.com/vector-im/riot-web/pull/11007)

Changes in [1.4.1](https://github.com/vector-im/riot-web/releases/tag/v1.4.1) (2019-10-01)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.4.0...v1.4.1)

 * Upgrade to React SDK 1.6.1 to fix critical
   [blank screen issue](https://github.com/vector-im/riot-web/issues/10983)
 * Upgrade to JS SDK 2.4.1 to to ignore crypto events with empty content
 * Update from Weblate
   [\#11010](https://github.com/vector-im/riot-web/pull/11010)
 * Update from Weblate
   [\#11001](https://github.com/vector-im/riot-web/pull/11001)
 * Upgrade deps
   [\#10980](https://github.com/vector-im/riot-web/pull/10980)

Changes in [1.4.0](https://github.com/vector-im/riot-web/releases/tag/v1.4.0) (2019-09-27)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.4.0-rc.2...v1.4.0)

* Many improvements related to privacy and user control of identity services and integration managers
* Upgrade to React SDK 1.6.0 and JS SDK 2.4.0

Changes in [1.4.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.4.0-rc.2) (2019-09-26)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.4.0-rc.1...v1.4.0-rc.2)

 * Upgrade to React SDK 1.6.0-rc.2
 * Work around Yarn confusion with `react-gemini-scrollbar` package

Changes in [1.4.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.4.0-rc.1) (2019-09-25)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.6...v1.4.0-rc.1)

 * Upgrade to React SDK 1.6.0-rc.1 and JS SDK 2.4.0-rc.1
 * Update from Weblate
   [\#10961](https://github.com/vector-im/riot-web/pull/10961)
 * Don't log query parameters as they may contain secrets
   [\#10929](https://github.com/vector-im/riot-web/pull/10929)
 * Document more shortcuts
   [\#10906](https://github.com/vector-im/riot-web/pull/10906)
 * Point to #develop and use the same gemini-scrollbar version as the react-sdk
   [\#10893](https://github.com/vector-im/riot-web/pull/10893)
 * Tweak lock file to pull in only one React version
   [\#10874](https://github.com/vector-im/riot-web/pull/10874)
 * document disable_custom_urls
   [\#10844](https://github.com/vector-im/riot-web/pull/10844)
 * Install guide tweaks
   [\#10838](https://github.com/vector-im/riot-web/pull/10838)
 * Switch to React 16
   [\#10480](https://github.com/vector-im/riot-web/pull/10480)
 * Update install guide
   [\#10810](https://github.com/vector-im/riot-web/pull/10810)
 * Clarify that HTTPS is not just needed for VoIP
   [\#6146](https://github.com/vector-im/riot-web/pull/6146)
 * Bump eslint-utils from 1.4.0 to 1.4.2
   [\#10692](https://github.com/vector-im/riot-web/pull/10692)
 * Add docs for tabbed integration managers labs flag
   [\#10641](https://github.com/vector-im/riot-web/pull/10641)
 * Change integrations_widgets_urls default configuration
   [\#10656](https://github.com/vector-im/riot-web/pull/10656)
 * Add docs for the CIDER composer flag
   [\#10638](https://github.com/vector-im/riot-web/pull/10638)
 * add cider composer labs flag
   [\#10626](https://github.com/vector-im/riot-web/pull/10626)
 * Upgrade to Electron 6.0.3
   [\#10601](https://github.com/vector-im/riot-web/pull/10601)
 * Upgrade to Electron 6
   [\#10596](https://github.com/vector-im/riot-web/pull/10596)
 * Update from Weblate
   [\#10591](https://github.com/vector-im/riot-web/pull/10591)
 * Upgrade electron-builder to 21.2.0
   [\#10579](https://github.com/vector-im/riot-web/pull/10579)
 * Set SUID bit on chrome-sandbox for Debian
   [\#10580](https://github.com/vector-im/riot-web/pull/10580)
 * Load config.json before loading language so default can apply
   [\#10551](https://github.com/vector-im/riot-web/pull/10551)
 * Bump matrix-react-test-utils for React 16 compatibility
   [\#10543](https://github.com/vector-im/riot-web/pull/10543)
 * Add --help to electron app
   [\#10530](https://github.com/vector-im/riot-web/pull/10530)
 * Allow setting electron autoHideMenuBar and persist it
   [\#10503](https://github.com/vector-im/riot-web/pull/10503)
 * Upgrade dependencies
   [\#10475](https://github.com/vector-im/riot-web/pull/10475)

Changes in [1.3.6](https://github.com/vector-im/riot-web/releases/tag/v1.3.6) (2019-09-19)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.5...v1.3.6)

 * Fix origin migrator for SSO logins
   [\#10920](https://github.com/vector-im/riot-web/pull/10920)

Changes in [1.3.5](https://github.com/vector-im/riot-web/releases/tag/v1.3.5) (2019-09-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.5-rc.3...v1.3.5)

 * Updated js-sdk and react-sdk for some more minor bugfixes

Changes in [1.3.5-rc.3](https://github.com/vector-im/riot-web/releases/tag/v1.3.5-rc.3) (2019-09-13)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.5-rc.2...v1.3.5-rc.3)

 * js-sdk rc.1 to include report API

Changes in [1.3.5-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.3.5-rc.2) (2019-09-13)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.5-rc.1...v1.3.5-rc.2)

 * Pull in more fixes from react-sdk rc.2

Changes in [1.3.5-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.3.5-rc.1) (2019-09-12)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.4...v1.3.5-rc.1)

 * Cosmetic fixes from react-sdk rc.1

Changes in [1.3.4](https://github.com/vector-im/riot-web/releases/tag/v1.3.4) (2019-09-12)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.4-rc.1...v1.3.4)

 * Updated react-sdk and tweaks to mobile install guide

Changes in [1.3.4-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.3.4-rc.1) (2019-09-11)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.3...v1.3.4-rc.1)

 * Update install guide
   [\#10831](https://github.com/vector-im/riot-web/pull/10831)

Changes in [1.3.3](https://github.com/vector-im/riot-web/releases/tag/v1.3.3) (2019-08-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.2...v1.3.3)

 * Linux-only release to fix sandboxing with Electron 5 on Debian
   [\#10580](https://github.com/vector-im/riot-web/pull/10580)

Changes in [1.3.2](https://github.com/vector-im/riot-web/releases/tag/v1.3.2) (2019-08-05)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.1...v1.3.2)

 * Updated react-sdk for deactivated account error message on login

Changes in [1.3.1](https://github.com/vector-im/riot-web/releases/tag/v1.3.1) (2019-08-05)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.1-rc.1...v1.3.1)

 * Updated js-sdk for notifications fix and react-sdk for registration fix

Changes in [1.3.1-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.3.1-rc.1) (2019-07-31)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.0...v1.3.1-rc.1)

 * Upgrade to JS SDK 2.3.0-rc.1 and React SDK 1.5.0-rc.1
 * Update from Weblate
   [\#10436](https://github.com/vector-im/riot-web/pull/10436)
 * Describe our existing features better in documentation
   [\#10418](https://github.com/vector-im/riot-web/pull/10418)
 * Upgrade to Electron 5
   [\#10392](https://github.com/vector-im/riot-web/pull/10392)
 * Remove edits and reactions feature flags from docs and config
   [\#10363](https://github.com/vector-im/riot-web/pull/10363)
 * Cachebust config file requests
   [\#10349](https://github.com/vector-im/riot-web/pull/10349)
 * Convert install-app-deps to subcommand
   [\#10334](https://github.com/vector-im/riot-web/pull/10334)
 * Add riot.im configuration files
   [\#10327](https://github.com/vector-im/riot-web/pull/10327)
 * Require descriptions in mxSendRageshake and remove infinite loop in issue
   templates
   [\#10321](https://github.com/vector-im/riot-web/pull/10321)
 * Remove unused disable_identity_server config flag
   [\#10322](https://github.com/vector-im/riot-web/pull/10322)
 * Verify i18n in CI
   [\#10320](https://github.com/vector-im/riot-web/pull/10320)

Changes in [1.3.0](https://github.com/vector-im/riot-web/releases/tag/v1.3.0) (2019-07-18)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.0-rc.3...v1.3.0)

 * Upgrade to React SDK 1.4.0 and JS SDK 2.2.0
 * Message editing and reactions features enabled
 * Remove edits and reactions feature flags from docs and config
   [\#10365](https://github.com/vector-im/riot-web/pull/10365)

Changes in [1.3.0-rc.3](https://github.com/vector-im/riot-web/releases/tag/v1.3.0-rc.3) (2019-07-15)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.0-rc.2...v1.3.0-rc.3)

 * Update to react-sdk rc.3 to fix a bug where a room admin could generate a room
   that would cause Riot to error, and some stuck notifications.

Changes in [1.3.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.3.0-rc.2) (2019-07-12)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.3.0-rc.1...v1.3.0-rc.2)

 * Upgrade to React SDK 1.4.0-rc.2 and JS SDK 2.2.0-rc.2
 * Fix regression from Riot 1.3.0-rc.1 when listing devices in user settings

Changes in [1.3.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.3.0-rc.1) (2019-07-12)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.4...v1.3.0-rc.1)

 * Upgrade to React SDK 1.4.0-rc.1 and JS SDK 2.2.0-rc.1
 * Update from Weblate
   [\#10328](https://github.com/vector-im/riot-web/pull/10328)
 * Upgrade dependencies
   [\#10308](https://github.com/vector-im/riot-web/pull/10308)
 * Upgrade dependencies
   [\#10260](https://github.com/vector-im/riot-web/pull/10260)

Changes in [1.2.4](https://github.com/vector-im/riot-web/releases/tag/v1.2.4) (2019-07-11)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.3...v1.2.4)

 * Upgrade to React SDK 1.3.1 and JS SDK 2.1.1
 * Upgrade lodash dependencies
 * JS SDK 2.1.1 includes a fix for ephemeral event processing
 * React SDK 1.3.1 includes a fix for account deactivation

Changes in [1.2.3](https://github.com/vector-im/riot-web/releases/tag/v1.2.3) (2019-07-08)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.3-rc.1...v1.2.3)

 * Upgrade to React SDK 1.3.0 and JS SDK 2.1.0
 * JS SDK 2.1.0 includes a fix for an exception whilst syncing

Changes in [1.2.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.2.3-rc.1) (2019-07-03)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.2...v1.2.3-rc.1)

 * Change update URL to match new host
   [\#10247](https://github.com/vector-im/riot-web/pull/10247)
 * Update from Weblate
   [\#10219](https://github.com/vector-im/riot-web/pull/10219)
 * Extract configuration docs to separate file
   [\#10195](https://github.com/vector-im/riot-web/pull/10195)
 * Add e2e/warning.svg to preload
   [\#10197](https://github.com/vector-im/riot-web/pull/10197)
 * Fix Electron vector: links
   [\#10196](https://github.com/vector-im/riot-web/pull/10196)
 * Display a red box of anger for config syntax errors
   [\#10193](https://github.com/vector-im/riot-web/pull/10193)
 * Move config-getting to VectorBasePlatform
   [\#10181](https://github.com/vector-im/riot-web/pull/10181)
 * Update from Weblate
   [\#10124](https://github.com/vector-im/riot-web/pull/10124)
 * Fix default Electron window and tray icons
   [\#10097](https://github.com/vector-im/riot-web/pull/10097)

Changes in [1.2.2](https://github.com/vector-im/riot-web/releases/tag/v1.2.2) (2019-06-19)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.2-rc.2...v1.2.2)

 No changes since rc.2

Changes in [1.2.2-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.2.2-rc.2) (2019-06-18)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.2-rc.1...v1.2.2-rc.2)

 * Update to react-sdk and js-sdk rc.2 for registration fixes,
   redaction local echo fix and removing unnecessary calls
   to the integration manager.

Changes in [1.2.2-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.2.2-rc.1) (2019-06-12)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.1...v1.2.2-rc.1)

 * Update from Weblate
   [\#10012](https://github.com/vector-im/riot-web/pull/10012)
 * Add funding details for GitHub sponsor button
   [\#9982](https://github.com/vector-im/riot-web/pull/9982)
 * Do not fail on server liveliness checks during startup
   [\#9960](https://github.com/vector-im/riot-web/pull/9960)
 * Hide guest functions on the welcome page if not logged in
   [\#9957](https://github.com/vector-im/riot-web/pull/9957)
 * Add Albanian and West Flemish languages
   [\#9953](https://github.com/vector-im/riot-web/pull/9953)
 * Update from Weblate
   [\#9951](https://github.com/vector-im/riot-web/pull/9951)
 * Add docs for defaultCountryCode
   [\#9927](https://github.com/vector-im/riot-web/pull/9927)
 * Use the user's pre-existing HS when config validation fails
   [\#9892](https://github.com/vector-im/riot-web/pull/9892)
 * Low bandwidth mode
   [\#9909](https://github.com/vector-im/riot-web/pull/9909)
 * Fix Twemoji loading on Windows dev machines
   [\#9869](https://github.com/vector-im/riot-web/pull/9869)
 * Base Docker image on nginx:alpine, not the larger nginx:latest
   [\#9848](https://github.com/vector-im/riot-web/pull/9848)
 * Validate homeserver configuration prior to loading the app
   [\#9779](https://github.com/vector-im/riot-web/pull/9779)
 * Show resolved homeserver configuration on the mobile guide
   [\#9726](https://github.com/vector-im/riot-web/pull/9726)
 * Flag the validated config as the default config
   [\#9721](https://github.com/vector-im/riot-web/pull/9721)
 * Clarify comment on is_url and hs_url handling
   [\#9719](https://github.com/vector-im/riot-web/pull/9719)
 * Validate default homeserver config before loading the app
   [\#9496](https://github.com/vector-im/riot-web/pull/9496)

Changes in [1.2.1](https://github.com/vector-im/riot-web/releases/tag/v1.2.1) (2019-05-31)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.0...v1.2.1)

 * Upgrade JS SDK to 2.0.0 and React SDK to 1.2.1 to fix key backup and native emoji height

Changes in [1.2.0](https://github.com/vector-im/riot-web/releases/tag/v1.2.0) (2019-05-29)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.2.0-rc.1...v1.2.0)

 * Upgrade to JS SDK v1.2.0 and React SDK v1.2.0 to fix some regressions

Changes in [1.2.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.2.0-rc.1) (2019-05-23)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.1.2...v1.2.0-rc.1)

 * Update from Weblate
   [\#9802](https://github.com/vector-im/riot-web/pull/9802)
 * remove emojione
   [\#9766](https://github.com/vector-im/riot-web/pull/9766)
 * Make Dockerfile work for develop and other branches
   [\#9736](https://github.com/vector-im/riot-web/pull/9736)
 * add description of new labs feature for message editing
   [\#9728](https://github.com/vector-im/riot-web/pull/9728)
 * Remove karma junit output
   [\#9628](https://github.com/vector-im/riot-web/pull/9628)
 * yarn upgrade
   [\#9626](https://github.com/vector-im/riot-web/pull/9626)
 * Respond quickly to buildkite pokes
   [\#9617](https://github.com/vector-im/riot-web/pull/9617)
 * Delay creating the `Favico` instance
   [\#9616](https://github.com/vector-im/riot-web/pull/9616)
 * Add reactions feature to config sample
   [\#9598](https://github.com/vector-im/riot-web/pull/9598)

Changes in [1.1.2](https://github.com/vector-im/riot-web/releases/tag/v1.1.2) (2019-05-15)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.1.1...v1.1.2)

 * react-sdk v1.1.2 to fix single sign-on and GIF autoplaying

Changes in [1.1.1](https://github.com/vector-im/riot-web/releases/tag/v1.1.1) (2019-05-14)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.1.0...v1.1.1)

 * react-sdk v1.1.1 to fix regressions with registration

Changes in [1.1.0](https://github.com/vector-im/riot-web/releases/tag/v1.1.0) (2019-05-07)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.1.0-rc.1...v1.1.0)

 * Add Dockerfile
   [\#9632](https://github.com/vector-im/riot-web/pull/9632)
 * Add Dockerfile (part 2)
   [\#9426](https://github.com/vector-im/riot-web/pull/9426)
 * Add new scalar staging url
   [\#9601](https://github.com/vector-im/riot-web/pull/9601)

Changes in [1.1.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.1.0-rc.1) (2019-04-30)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.8...v1.1.0-rc.1)

 * Convert redeploy.py to buildkite
   [\#9577](https://github.com/vector-im/riot-web/pull/9577)
 * Add package step to buildkite pipeline
   [\#9568](https://github.com/vector-im/riot-web/pull/9568)
 * Don't fail if there's no local config to remove
   [\#9571](https://github.com/vector-im/riot-web/pull/9571)
 * Change jenkins script to package script
   [\#9567](https://github.com/vector-im/riot-web/pull/9567)
 * Remove config.json from package dir
   [\#9555](https://github.com/vector-im/riot-web/pull/9555)
 * use the release version of olm 3.1.0
   [\#9550](https://github.com/vector-im/riot-web/pull/9550)
 * Fix default for --include arg
   [\#9517](https://github.com/vector-im/riot-web/pull/9517)
 * update installation instructions with new repo
   [\#9500](https://github.com/vector-im/riot-web/pull/9500)
 * Use packages.matrix.org for Olm
   [\#9498](https://github.com/vector-im/riot-web/pull/9498)
 * Add separate platform electron build commands
   [\#9412](https://github.com/vector-im/riot-web/pull/9412)
 * Add support for custom profile directory
   [\#9408](https://github.com/vector-im/riot-web/pull/9408)
 * Improved mobile install guide
   [\#9410](https://github.com/vector-im/riot-web/pull/9410)
 * Remove vector-electron-desktop from README
   [\#9404](https://github.com/vector-im/riot-web/pull/9404)
 * Update from Weblate
   [\#9398](https://github.com/vector-im/riot-web/pull/9398)
 * bump olm version to 3.1.0-pre3
   [\#9392](https://github.com/vector-im/riot-web/pull/9392)
 * Add expiration to mobile guide cookie
   [\#9383](https://github.com/vector-im/riot-web/pull/9383)
 * Fix autolaunch setting appearing toggled off
   [\#9368](https://github.com/vector-im/riot-web/pull/9368)
 * Don't try to save files the user didn't want to save
   [\#9352](https://github.com/vector-im/riot-web/pull/9352)
 * Setup crypto store for restore session tests
   [\#9325](https://github.com/vector-im/riot-web/pull/9325)
 * Update from Weblate
   [\#9333](https://github.com/vector-im/riot-web/pull/9333)
 * Add "Save image as..." button to context menu on images
   [\#9326](https://github.com/vector-im/riot-web/pull/9326)
 * Configure auth footer links through Riot config
   [\#9297](https://github.com/vector-im/riot-web/pull/9297)

Changes in [1.0.8](https://github.com/vector-im/riot-web/releases/tag/v1.0.8) (2019-04-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.7...v1.0.8)

 * No changes in this release. This is the same code as v1.0.7 from our new clean-room
   packaging and signing infrastructure.

Changes in [1.0.7](https://github.com/vector-im/riot-web/releases/tag/v1.0.7) (2019-04-08)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.6...v1.0.7)

 * Hotfix: bump js-sdk to 1.0.4, see https://github.com/matrix-org/matrix-js-sdk/releases/tag/v1.0.4

Changes in [1.0.6](https://github.com/vector-im/riot-web/releases/tag/v1.0.6) (2019-04-01)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.6-rc.1...v1.0.6)

 * Add "Save image as..." button to context menu on images
   [\#9327](https://github.com/vector-im/riot-web/pull/9327)

Changes in [1.0.6-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.0.6-rc.1) (2019-03-27)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.5...v1.0.6-rc.1)

 * Use `on_logged_in` action in tests
   [\#9279](https://github.com/vector-im/riot-web/pull/9279)
 * Convert away from `Promise.defer`
   [\#9278](https://github.com/vector-im/riot-web/pull/9278)
 * update react-sdk version in yarn lockfile
   [\#9233](https://github.com/vector-im/riot-web/pull/9233)
 * "Render simple counters in room header" details
   [\#9154](https://github.com/vector-im/riot-web/pull/9154)
 * Use medium agents for the more resource intensive builds
   [\#9238](https://github.com/vector-im/riot-web/pull/9238)
 * Add log grouping to buildkite
   [\#9223](https://github.com/vector-im/riot-web/pull/9223)
 * Switch to `git` protocol for CI dependencies
   [\#9222](https://github.com/vector-im/riot-web/pull/9222)
 * Support CI for matching branches on forks
   [\#9212](https://github.com/vector-im/riot-web/pull/9212)
 * Update from Weblate
   [\#9199](https://github.com/vector-im/riot-web/pull/9199)
 * Declare the officially supported browsers in the README
   [\#9177](https://github.com/vector-im/riot-web/pull/9177)
 * Document some desktop app things
   [\#9011](https://github.com/vector-im/riot-web/pull/9011)
 * Use Buildkite for CI
   [\#9165](https://github.com/vector-im/riot-web/pull/9165)
 * Update version number in issue templates
   [\#9170](https://github.com/vector-im/riot-web/pull/9170)
 * Remove node 8.x from the build matrix
   [\#9159](https://github.com/vector-im/riot-web/pull/9159)
 * Update Electron help menu link
   [\#9157](https://github.com/vector-im/riot-web/pull/9157)

Changes in [1.0.5](https://github.com/vector-im/riot-web/releases/tag/v1.0.5) (2019-03-21)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.4...v1.0.5)

 * Hotfix for [\#9205](https://github.com/vector-im/riot-web/issues/9205) disabling jump prevention for typing notifications, while we're reworking this functionally to enable it again soon.

Changes in [1.0.4](https://github.com/vector-im/riot-web/releases/tag/v1.0.4) (2019-03-18)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.4-rc.1...v1.0.4)

 * No changes since rc.1

Changes in [1.0.4-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.0.4-rc.1) (2019-03-13)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.3...v1.0.4-rc.1)

 * Update from Weblate
   [\#9152](https://github.com/vector-im/riot-web/pull/9152)
 * Use modern Yarn version on Travis CI
   [\#9151](https://github.com/vector-im/riot-web/pull/9151)
 * Switch to `yarn` for dependency management
   [\#9132](https://github.com/vector-im/riot-web/pull/9132)
 * Update from Weblate
   [\#9104](https://github.com/vector-im/riot-web/pull/9104)
 * Don't copy the 32 bit linux deb
   [\#9075](https://github.com/vector-im/riot-web/pull/9075)
 * Change olm dependency to normal dep
   [\#9068](https://github.com/vector-im/riot-web/pull/9068)
 * Add modular.im hosting link to electron app config
   [\#9047](https://github.com/vector-im/riot-web/pull/9047)
 * Nudge karma to 3.1.2
   [\#8991](https://github.com/vector-im/riot-web/pull/8991)
 * Add support for localConfig at $appData/config.json.
   [\#8983](https://github.com/vector-im/riot-web/pull/8983)

Changes in [1.0.3](https://github.com/vector-im/riot-web/releases/tag/v1.0.3) (2019-03-06)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.2...v1.0.3)

 * react-sdk 1.0.3 to fix ctrl+k shortcut and room list bugs

Changes in [1.0.2](https://github.com/vector-im/riot-web/releases/tag/v1.0.2) (2019-03-06)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.2-rc.3...v1.0.2)

 * New react-sdk for minor hosting link fixes

Changes in [1.0.2-rc.3](https://github.com/vector-im/riot-web/releases/tag/v1.0.2-rc.3) (2019-03-05)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.2-rc.2...v1.0.2-rc.3)

 * Add modular.im hosting link to electron app config
   [\#9051](https://github.com/vector-im/riot-web/pull/9051)

Changes in [1.0.2-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.0.2-rc.2) (2019-03-01)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.2-rc.1...v1.0.2-rc.2)

 * Update to react-sdk rc.3

Changes in [1.0.2-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.0.2-rc.1) (2019-03-01)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.1...v1.0.2-rc.1)

 * Set a require alias for the webapp directory
   [\#9014](https://github.com/vector-im/riot-web/pull/9014)
 * Update from Weblate.
   [\#8973](https://github.com/vector-im/riot-web/pull/8973)
 * set chrome path for travis CI explicitly
   [\#8987](https://github.com/vector-im/riot-web/pull/8987)
 * Updated install spinner
   [\#8984](https://github.com/vector-im/riot-web/pull/8984)
 * Allow disabling update mechanism
   [\#8911](https://github.com/vector-im/riot-web/pull/8911)
 * Allow configuration of whether closing window closes or minimizes to tray
   [\#8908](https://github.com/vector-im/riot-web/pull/8908)
 * Fix language file path for Jenkins
   [\#8854](https://github.com/vector-im/riot-web/pull/8854)
 * Document and recommend `default_server_name`
   [\#8832](https://github.com/vector-im/riot-web/pull/8832)
 * Cache busting for icons & language files
   [\#8710](https://github.com/vector-im/riot-web/pull/8710)
 * Remove redesign issue template
   [\#8722](https://github.com/vector-im/riot-web/pull/8722)
 * Make scripts/make-icons.sh work on linux
   [\#8550](https://github.com/vector-im/riot-web/pull/8550)

Changes in [1.0.1](https://github.com/vector-im/riot-web/releases/tag/v1.0.1) (2019-02-15)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.0...v1.0.1)


Changes in [1.0.0](https://github.com/vector-im/riot-web/releases/tag/v1.0.0) (2019-02-14)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.0-rc.2...v1.0.0)

 * Add snipping lines to welcome page without guests
   [\#8634](https://github.com/vector-im/riot-web/pull/8634)
 * Add home page to fix loading tests
   [\#8625](https://github.com/vector-im/riot-web/pull/8625)

Changes in [1.0.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v1.0.0-rc.2) (2019-02-14)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v1.0.0-rc.1...v1.0.0-rc.2)

 * Update from Weblate.
   [\#8615](https://github.com/vector-im/riot-web/pull/8615)
 * Replace favicon assets to ones with transparent backgrounds
   [\#8600](https://github.com/vector-im/riot-web/pull/8600)
 * Refreshed icons
   [\#8594](https://github.com/vector-im/riot-web/pull/8594)
 * Fix order of fetch-develop-deps / npm install
   [\#8566](https://github.com/vector-im/riot-web/pull/8566)
 * Revive building dark theme
   [\#8540](https://github.com/vector-im/riot-web/pull/8540)
 * Update from Weblate.
   [\#8546](https://github.com/vector-im/riot-web/pull/8546)
 * Repair app loading tests after welcome page
   [\#8525](https://github.com/vector-im/riot-web/pull/8525)
 * Support configurable welcome background and logo
   [\#8528](https://github.com/vector-im/riot-web/pull/8528)
 * Update from Weblate.
   [\#8518](https://github.com/vector-im/riot-web/pull/8518)
 * Document `embeddedPages` configuration
   [\#8514](https://github.com/vector-im/riot-web/pull/8514)
 * README.md : Syntax Coloring
   [\#8502](https://github.com/vector-im/riot-web/pull/8502)

Changes in [1.0.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v1.0.0-rc.1) (2019-02-08)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.9...v1.0.0-rc.1)

 * Update from Weblate.
   [\#8475](https://github.com/vector-im/riot-web/pull/8475)
 * Add configurable welcome page
   [\#8466](https://github.com/vector-im/riot-web/pull/8466)
 * fix app tests after force enabling lazy loading + removing feature flag
   [\#8464](https://github.com/vector-im/riot-web/pull/8464)
 * Allow Electron to zoom with CommandOrControl+=
   [\#8381](https://github.com/vector-im/riot-web/pull/8381)
 * Hide sign in / create account for logged in users
   [\#8368](https://github.com/vector-im/riot-web/pull/8368)
 * Fix home page link target
   [\#8365](https://github.com/vector-im/riot-web/pull/8365)
 * Add auth background image and update Riot logo
   [\#8364](https://github.com/vector-im/riot-web/pull/8364)
 * New homepage
   [\#8363](https://github.com/vector-im/riot-web/pull/8363)
 * Spell homeserver correctly
   [\#8358](https://github.com/vector-im/riot-web/pull/8358)
 * Merge redesign into develop
   [\#8321](https://github.com/vector-im/riot-web/pull/8321)
 * Disable room directory test because it doesn't work
   [\#8318](https://github.com/vector-im/riot-web/pull/8318)
 * Tweak auth overflow on Windows and Linux
   [\#8307](https://github.com/vector-im/riot-web/pull/8307)
 * Clean up Custom Server Help dialog
   [\#8296](https://github.com/vector-im/riot-web/pull/8296)
 * Cache-bust olm.wasm
   [\#8283](https://github.com/vector-im/riot-web/pull/8283)
 * Completely disable other themes for now (#8277)
   [\#8280](https://github.com/vector-im/riot-web/pull/8280)
 * Remove support for team servers
   [\#8271](https://github.com/vector-im/riot-web/pull/8271)
 * Add target="_blank" to footer links
   [\#8248](https://github.com/vector-im/riot-web/pull/8248)
 * Fix device names on desktop
   [\#8241](https://github.com/vector-im/riot-web/pull/8241)
 * Fix literal &lt/&gt in notifications
   [\#8238](https://github.com/vector-im/riot-web/pull/8238)
 * Fix registration nextLink on desktop
   [\#8239](https://github.com/vector-im/riot-web/pull/8239)
 * Add returns to fetch-develop-deps
   [\#8233](https://github.com/vector-im/riot-web/pull/8233)
 * Update electron builder
   [\#8231](https://github.com/vector-im/riot-web/pull/8231)
 * Try fetching more branches for PRs
   [\#8225](https://github.com/vector-im/riot-web/pull/8225)
 * Use content hashing for font and image URLs
   [\#8159](https://github.com/vector-im/riot-web/pull/8159)
 * Develop->Experimental
   [\#8156](https://github.com/vector-im/riot-web/pull/8156)
 * Update from Weblate.
   [\#8150](https://github.com/vector-im/riot-web/pull/8150)
 * Correct the copying of e-mail addresses in the electron app
   [\#8124](https://github.com/vector-im/riot-web/pull/8124)
 * Start documenting keyboard shortcuts
   [\#7165](https://github.com/vector-im/riot-web/pull/7165)
 * Update issue templates
   [\#7948](https://github.com/vector-im/riot-web/pull/7948)
 * Added new colour var to all themes
   [\#7927](https://github.com/vector-im/riot-web/pull/7927)
 * Redesign: apply changes from dharma theme to status theme
   [\#7541](https://github.com/vector-im/riot-web/pull/7541)
 * Redesign: ignore setting and always show dharma theme for now
   [\#7540](https://github.com/vector-im/riot-web/pull/7540)

Changes in [0.17.9](https://github.com/vector-im/riot-web/releases/tag/v0.17.9) (2019-01-22)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.9-rc.1...v0.17.9)

 * Bugfix in react-sdk for setting DM rooms

Changes in [0.17.9-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.17.9-rc.1) (2019-01-17)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.8...v0.17.9-rc.1)

 * Merge develop into experimental
   [\#8003](https://github.com/vector-im/riot-web/pull/8003)
 * Electron: Load app from custom protocol
   [\#7943](https://github.com/vector-im/riot-web/pull/7943)
 * Fix the IndexedDB worker
   [\#7920](https://github.com/vector-im/riot-web/pull/7920)
 * Make clear that the Debian package is for desktop
   [\#7919](https://github.com/vector-im/riot-web/pull/7919)
 * Run the Desktop app in a sandbox
   [\#7907](https://github.com/vector-im/riot-web/pull/7907)
 * Update to new electron single instance API
   [\#7908](https://github.com/vector-im/riot-web/pull/7908)
 * Update the tests to match https://github.com/matrix-org/matrix-react-
   sdk/pull/2340
   [\#7834](https://github.com/vector-im/riot-web/pull/7834)

Changes in [0.17.8](https://github.com/vector-im/riot-web/releases/tag/v0.17.8) (2018-12-10)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.8-rc.1...v0.17.8)

 * No changes since rc.1

Changes in [0.17.8-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.17.8-rc.1) (2018-12-06)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.7...v0.17.8-rc.1)

 * Update from Weblate.
   [\#7784](https://github.com/vector-im/riot-web/pull/7784)
 * Add a function to send a rageshake from the console
   [\#7755](https://github.com/vector-im/riot-web/pull/7755)
 * Re-apply "Run lint on travis builds and use modern node versions"
   [\#7738](https://github.com/vector-im/riot-web/pull/7738)
 * Revert "Run lint on travis builds and use modern node versions"
   [\#7737](https://github.com/vector-im/riot-web/pull/7737)
 * Run lint on travis builds and use modern node versions
   [\#7490](https://github.com/vector-im/riot-web/pull/7490)
 * Fix missing js-sdk logging
   [\#7736](https://github.com/vector-im/riot-web/pull/7736)
 * Add $accent-color-50pct as a CSS variable to the Status theme
   [\#7710](https://github.com/vector-im/riot-web/pull/7710)

Changes in [0.17.7](https://github.com/vector-im/riot-web/releases/tag/v0.17.7) (2018-11-22)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.6...v0.17.7)

 * Warning when crypto DB is too new to use.
 * Fix missing entries from js-sdk in rageshake logs

Changes in [0.17.6](https://github.com/vector-im/riot-web/releases/tag/v0.17.6) (2018-11-19)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.6-rc.2...v0.17.6)

 * No changes since rc.2

Changes in [0.17.6-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.17.6-rc.2) (2018-11-15)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.6-rc.1...v0.17.6-rc.2)

 * Update to js-sdk 0.14 and react-sdk rc.2. rc.1 was broken as it was built against
   js-sdk 0.13 which does not use the new Olm 3.0 API.

Changes in [0.17.6-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.17.6-rc.1) (2018-11-15)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.5...v0.17.6-rc.1)

 * Update from Weblate.
   [\#7708](https://github.com/vector-im/riot-web/pull/7708)
 * Add Japanese (#7599)
   [\#7673](https://github.com/vector-im/riot-web/pull/7673)
 * Allow Webpack dev server to listen to all interfaces
   [\#7674](https://github.com/vector-im/riot-web/pull/7674)
 * Remove the request-only stuff we don't need anymore
   [\#7637](https://github.com/vector-im/riot-web/pull/7637)
 * Correct the author of the electron app
   [\#7615](https://github.com/vector-im/riot-web/pull/7615)
 * Mock fs, tls, and net to support request in the browser
   [\#7552](https://github.com/vector-im/riot-web/pull/7552)
 * Update chokidar to transitively get newer fsevents
   [\#7598](https://github.com/vector-im/riot-web/pull/7598)
 * Support WebAssembly version of Olm
   [\#7385](https://github.com/vector-im/riot-web/pull/7385)

Changes in [0.17.5](https://github.com/vector-im/riot-web/releases/tag/v0.17.5) (2018-11-13)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.4...v0.17.5)

 * Include change that was supposed to be included in orevious version

Changes in [0.17.4](https://github.com/vector-im/riot-web/releases/tag/v0.17.4) (2018-11-13)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.3...v0.17.4)

 * Add banner with login/register links for users who aren't logged in

Changes in [0.17.3](https://github.com/vector-im/riot-web/releases/tag/v0.17.3) (2018-10-29)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.3-rc.1...v0.17.3)

 * Fix for autocompleting text emoji from react-sdk v0.14.2

Changes in [0.17.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.17.3-rc.1) (2018-10-24)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.2...v0.17.3-rc.1)

 * Update from Weblate.
   [\#7549](https://github.com/vector-im/riot-web/pull/7549)
 * Don't set tags on notifications
   [\#7518](https://github.com/vector-im/riot-web/pull/7518)
 * Update to latest electron builder
   [\#7498](https://github.com/vector-im/riot-web/pull/7498)
 * Fix Tinter.setTheme to not fire using Firefox
   [\#6831](https://github.com/vector-im/riot-web/pull/6831)

Changes in [0.17.2](https://github.com/vector-im/riot-web/releases/tag/v0.17.2) (2018-10-19)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.1...v0.17.2)

 * Update react-sdk version to "Apply the user's tint once the MatrixClientPeg is moderately ready"
 * Electron: don't set tags on notifications
   [\#7518](https://github.com/vector-im/riot-web/pull/7518)

Changes in [0.17.1](https://github.com/vector-im/riot-web/releases/tag/v0.17.1) (2018-10-18)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.0...v0.17.1)

 * Stop electron crashing
   [\#7517](https://github.com/vector-im/riot-web/pull/7517)

Changes in [0.17.0](https://github.com/vector-im/riot-web/releases/tag/v0.17.0) (2018-10-16)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.17.0-rc.1...v0.17.0)

 * Phased rollout of lazyloading
   [\#7503](https://github.com/vector-im/riot-web/pull/7503)
 * Update to latest electron builder
   [\#7501](https://github.com/vector-im/riot-web/pull/7501)

Changes in [0.17.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.17.0-rc.1) (2018-10-11)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.5...v0.17.0-rc.1)

 * Revert "also commit the lock file when bumping version as it is now
   committed to the repo"
   [\#7483](https://github.com/vector-im/riot-web/pull/7483)
 * Update from Weblate.
   [\#7478](https://github.com/vector-im/riot-web/pull/7478)
 *  Fix riot-web Promise.defer warnings (#7409)
   [\#7444](https://github.com/vector-im/riot-web/pull/7444)
 * Use HTTPS cloning for riot-web too
   [\#7459](https://github.com/vector-im/riot-web/pull/7459)
 * Disable webpack-dev-server auto reload
   [\#7463](https://github.com/vector-im/riot-web/pull/7463)
 * Silence bluebird warnings
   [\#7462](https://github.com/vector-im/riot-web/pull/7462)
 * Fix reskindex on matrix-react-side not being called if using build script
   [\#7443](https://github.com/vector-im/riot-web/pull/7443)
 * Fix double-closed tags
   [\#7454](https://github.com/vector-im/riot-web/pull/7454)
 * Document how to turn off Piwik and bug reports (#6738)
   [\#7435](https://github.com/vector-im/riot-web/pull/7435)
 * also commit the lock file when bumping version as it is now committed to the
   repo
   [\#7429](https://github.com/vector-im/riot-web/pull/7429)
 * Update a bunch of deps
   [\#7393](https://github.com/vector-im/riot-web/pull/7393)
 * Don't show mobile guide if deep linking
   [\#7415](https://github.com/vector-im/riot-web/pull/7415)
 * Don't show custom server bit on matrix.org
   [\#7408](https://github.com/vector-im/riot-web/pull/7408)
 * Update Webpack to version 4
   [\#6620](https://github.com/vector-im/riot-web/pull/6620)
 * Webpack4
   [\#7387](https://github.com/vector-im/riot-web/pull/7387)

Changes in [0.16.6](https://github.com/vector-im/riot-web/releases/tag/v0.16.6) (2018-10-08)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.5...v0.16.6)

 * Update to matrix-react-sdk v0.13.6

Changes in [0.16.5](https://github.com/vector-im/riot-web/releases/tag/v0.16.5) (2018-10-01)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.5-rc.1...v0.16.5)

 * Don't show mobile guide if deep linking
   [\#7415](https://github.com/vector-im/riot-web/pull/7415)
 * Don't show custom server bit on matrix.org
   [\#7408](https://github.com/vector-im/riot-web/pull/7408)

Changes in [0.16.5-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.16.5-rc.1) (2018-09-27)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.4...v0.16.5-rc.1)

 * Update from Weblate.
   [\#7395](https://github.com/vector-im/riot-web/pull/7395)
 * Reduce the number of terminals required to build riot-web to 1
   [\#7355](https://github.com/vector-im/riot-web/pull/7355)
 * Small typo in release notes v0.16.3
   [\#7274](https://github.com/vector-im/riot-web/pull/7274)

Changes in [0.16.4](https://github.com/vector-im/riot-web/releases/tag/v0.16.4) (2018-09-10)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.4-rc.1...v0.16.4)

 * No changes since rc.1

Changes in [0.16.4-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.16.4-rc.1) (2018-09-07)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.3...v0.16.4-rc.1)

 * Update from Weblate.
   [\#7296](https://github.com/vector-im/riot-web/pull/7296)
 * Fix config not loading & mobileguide script being loaded in riot
   [\#7288](https://github.com/vector-im/riot-web/pull/7288)
 * Instructions for installing mobile apps
   [\#7272](https://github.com/vector-im/riot-web/pull/7272)
 * Tidy up index.js
   [\#7265](https://github.com/vector-im/riot-web/pull/7265)

Changes in [0.16.3](https://github.com/vector-im/riot-web/releases/tag/v0.16.3) (2018-09-03)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.3-rc.2...v0.16.3)

 * SECURITY FIX: This version (and release candidates) pull in an upstream security
   fix from electron to fix CVE-2018-15685. Electron users should update as soon as
   possible. Riot-web run outside of Electron is unaffected.

Changes in [0.16.3-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.16.3-rc.2) (2018-08-31)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.3-rc.1...v0.16.3-rc.2)

 * Update js-sdk to fix an exception causing the room list to become unresponsive.

Changes in [0.16.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.16.3-rc.1) (2018-08-30)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.2...v0.16.3-rc.1)

 * Update from Weblate.
   [\#7245](https://github.com/vector-im/riot-web/pull/7245)
 * Revert "Remove package-lock.json for now"
   [\#7128](https://github.com/vector-im/riot-web/pull/7128)
 * Remove package-lock.json for now
   [\#7115](https://github.com/vector-im/riot-web/pull/7115)

Changes in [0.16.2](https://github.com/vector-im/riot-web/releases/tag/v0.16.2) (2018-08-23)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.1...v0.16.2)

 * Support new server notices format

Changes in [0.16.1](https://github.com/vector-im/riot-web/releases/tag/v0.16.1) (2018-08-20)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.1-rc.1...v0.16.1)

 * No changes since rc.1

Changes in [0.16.1-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.16.1-rc.1) (2018-08-16)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.0...v0.16.1-rc.1)

 * Update from Weblate.
   [\#7178](https://github.com/vector-im/riot-web/pull/7178)
 * CSS for MAU warning bar
   [\#7152](https://github.com/vector-im/riot-web/pull/7152)
 * CSS for user limit error
   [\#7139](https://github.com/vector-im/riot-web/pull/7139)
 * Unpin sanitize-html
   [\#7132](https://github.com/vector-im/riot-web/pull/7132)
 * Pin sanitize-html to 0.18.2
   [\#7129](https://github.com/vector-im/riot-web/pull/7129)

Changes in [0.16.0](https://github.com/vector-im/riot-web/releases/tag/v0.16.0) (2018-07-30)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.0-rc.2...v0.16.0)

* Update react-sdk version for bugfixes with Jitsi widgets and the new composer

Changes in [0.16.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.16.0-rc.2) (2018-07-24)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.16.0-rc.1...v0.16.0-rc.2)

 * Update to react-sdk rc.2 to remove Jitsi conference calling from labs

Changes in [0.16.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.16.0-rc.1) (2018-07-24)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.7...v0.16.0-rc.1)

 * Update from Weblate.
   [\#7082](https://github.com/vector-im/riot-web/pull/7082)
 * Sample config for jitsi integration URL
   [\#7055](https://github.com/vector-im/riot-web/pull/7055)

Changes in [0.15.7](https://github.com/vector-im/riot-web/releases/tag/v0.15.7) (2018-07-09)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.7-rc.2...v0.15.7)

 * No changes since rc.2

Changes in [0.15.7-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.15.7-rc.2) (2018-07-06)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.7-rc.1...v0.15.7-rc.2)

 * Update react-sdk and js-sdk

Changes in [0.15.7-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.15.7-rc.1) (2018-07-04)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.6...v0.15.7-rc.1)

 * add override for colour of room tile text within memberinfo (unreadable)
   [\#6889](https://github.com/vector-im/riot-web/pull/6889)

Changes in [0.15.6](https://github.com/vector-im/riot-web/releases/tag/v0.15.6) (2018-06-29)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.6-rc.2...v0.15.6)

 * Pull in bug fixes from react-sdk

Changes in [0.15.6-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.15.6-rc.2) (2018-06-22)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.6-rc.1...v0.15.6-rc.2)

 * Update to react-sdk rc.2 for fix to slash commands

Changes in [0.15.6-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.15.6-rc.1) (2018-06-21)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.5...v0.15.6-rc.1)

 * Update from Weblate.
   [\#6915](https://github.com/vector-im/riot-web/pull/6915)
 * [electron] Fix desktop app --hidden flag
   [\#6805](https://github.com/vector-im/riot-web/pull/6805)

Changes in [0.15.5](https://github.com/vector-im/riot-web/releases/tag/v0.15.5) (2018-06-12)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.5-rc.1...v0.15.5)

 * No changes since rc.1

Changes in [0.15.5-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.15.5-rc.1) (2018-06-06)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.4...v0.15.5-rc.1)

 * Update from Weblate.
   [\#6846](https://github.com/vector-im/riot-web/pull/6846)

Changes in [0.15.4](https://github.com/vector-im/riot-web/releases/tag/v0.15.4) (2018-05-25)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.4-rc.1...v0.15.4)

 * Add cookie policy link to desktop app config

Changes in [0.15.4-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.15.4-rc.1) (2018-05-24)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.3...v0.15.4-rc.1)

 * Update from Weblate.
   [\#6792](https://github.com/vector-im/riot-web/pull/6792)
 * Hide URL options for e2e blob: URL images
   [\#6765](https://github.com/vector-im/riot-web/pull/6765)
 * Fix right click menu in electron
   [\#6763](https://github.com/vector-im/riot-web/pull/6763)
 * Update to electron 2.0.1
   [\#6764](https://github.com/vector-im/riot-web/pull/6764)
 * Add instructions for changing translated strings
   [\#6528](https://github.com/vector-im/riot-web/pull/6528)

Changes in [0.15.3](https://github.com/vector-im/riot-web/releases/tag/v0.15.3) (2018-05-18)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.2...v0.15.3)

 * Fix right click menu in electron
   [\#6763](https://github.com/vector-im/riot-web/pull/6763)
 * Update to electron 2.0.1
   [\#6764](https://github.com/vector-im/riot-web/pull/6764)
 * Hide URL options for e2e blob: URL images
   [\#6765](https://github.com/vector-im/riot-web/pull/6765)

Changes in [0.15.2](https://github.com/vector-im/riot-web/releases/tag/v0.15.2) (2018-05-17)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.1...v0.15.2)

 * Update to matrix-react-sdk v0.12.5 to fix image size jumps

Changes in [0.15.1](https://github.com/vector-im/riot-web/releases/tag/v0.15.1) (2018-05-16)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0...v0.15.1)

 * Fix package-lock.json which was causing errors building the Electron app
 * Update Electron version

Changes in [0.15.0](https://github.com/vector-im/riot-web/releases/tag/v0.15.0) (2018-05-16)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0-rc.6...v0.15.0)

 * No changes since rc.6

Changes in [0.15.0-rc.6](https://github.com/vector-im/riot-web/releases/tag/v0.15.0-rc.6) (2018-05-15)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0-rc.5...v0.15.0-rc.6)

 * Update to matrix-react-sdk 0.12.4-rc.6

Changes in [0.15.0-rc.5](https://github.com/vector-im/riot-web/releases/tag/v0.15.0-rc.5) (2018-05-15)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0-rc.4...v0.15.0-rc.5)

 * Update to matrix-react-sdk 0.12.4-rc.5

Changes in [0.15.0-rc.4](https://github.com/vector-im/riot-web/releases/tag/v0.15.0-rc.4) (2018-05-14)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0-rc.3...v0.15.0-rc.4)

 * Update from Weblate.
   [\#6726](https://github.com/vector-im/riot-web/pull/6726)
 * Update to matrix-react-sdk 0.12.4-rc.4

Changes in [0.15.0-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.15.0-rc.3) (2018-05-11)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0-rc.2...v0.15.0-rc.3)

 * Update to matrix-react-sdk 0.12.4-rc.3

Changes in [0.15.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.15.0-rc.2) (2018-05-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.15.0-rc.1...v0.15.0-rc.2)

 * Update to matrix-react-sdk 0.12.4-rc.2

Changes in [0.15.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.15.0-rc.1) (2018-05-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.3-rc.1...v0.15.0-rc.1)

 * No changes since 0.14.3-rc.1

Changes in [0.14.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.14.3-rc.1) (2018-05-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.2...v0.14.3-rc.1)

 * Update from Weblate.
   [\#6688](https://github.com/vector-im/riot-web/pull/6688)
 * Don't show presence on matrix.org
   [\#6638](https://github.com/vector-im/riot-web/pull/6638)
 * Enforce loading babel-polyfill first
   [\#6625](https://github.com/vector-im/riot-web/pull/6625)
 * Update hoek
   [\#6624](https://github.com/vector-im/riot-web/pull/6624)
 * Fix args in the release wrapper script
   [\#6614](https://github.com/vector-im/riot-web/pull/6614)

Changes in [0.14.2](https://github.com/vector-im/riot-web/releases/tag/v0.14.2) (2018-04-30)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.2-rc.3...v0.14.2)

 * No changes since rc.3

Changes in [0.14.2-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.14.2-rc.3) (2018-04-26)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.2-rc.2...v0.14.2-rc.3)

 * Fix CSS dependency versions to be the same as those in react-sdk to fix
   left panel header positions.

Changes in [0.14.2-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.14.2-rc.2) (2018-04-26)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.2-rc.1...v0.14.2-rc.2)

 * Fix Download of attachments in e2e encrypted rooms in Firefox

Changes in [0.14.2-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.14.2-rc.1) (2018-04-25)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.1...v0.14.2-rc.1)

 * Update from Weblate.
   [\#6602](https://github.com/vector-im/riot-web/pull/6602)
 * Add readme bit on cross-origin renderer
   [\#6600](https://github.com/vector-im/riot-web/pull/6600)
 * Update from Weblate.
   [\#6573](https://github.com/vector-im/riot-web/pull/6573)
 * Copy media from react-sdk
   [\#6588](https://github.com/vector-im/riot-web/pull/6588)
 * Fix favicon
   [\#6580](https://github.com/vector-im/riot-web/pull/6580)
 * Update from Weblate.
   [\#6569](https://github.com/vector-im/riot-web/pull/6569)
 * move everything not explicitly riot (or status) branded into matrix-react-
   sdk
   [\#6500](https://github.com/vector-im/riot-web/pull/6500)
 * Remove presence management
   [\#5881](https://github.com/vector-im/riot-web/pull/5881)
 * change vector-web repo to riot-web in changelog
   [\#6480](https://github.com/vector-im/riot-web/pull/6480)
 * Update from Weblate.
   [\#6473](https://github.com/vector-im/riot-web/pull/6473)
 * Bump source-map-loader version to avoid bug /w inline base64 maps
   [\#6472](https://github.com/vector-im/riot-web/pull/6472)
 * Add CSS for new group admin radio button
   [\#6415](https://github.com/vector-im/riot-web/pull/6415)
 * Rxl881/sticker picker styling
   [\#6447](https://github.com/vector-im/riot-web/pull/6447)
 * Stickerpacks
   [\#6242](https://github.com/vector-im/riot-web/pull/6242)
 * Force gemini on HomePage
   [\#6368](https://github.com/vector-im/riot-web/pull/6368)
 * Rename the Riot-Web Translations Room
   [\#6348](https://github.com/vector-im/riot-web/pull/6348)
 * Add disable-presence-by-hs option to sample config
   [\#6350](https://github.com/vector-im/riot-web/pull/6350)
 * Reword the BugReportDialog.js as per @lampholder
   [\#6354](https://github.com/vector-im/riot-web/pull/6354)

Changes in [0.14.1](https://github.com/vector-im/riot-web/releases/tag/v0.14.1) (2018-04-12)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0...v0.14.1)

 * Remove presence management feature from labs
 * Fix an issue where Riot would fail to load at all if certain
   extensions were installed on Firefox
 * Fix an issue where e2e cryptography could be disabled due to
   a migration error.

Changes in [0.14.0](https://github.com/vector-im/riot-web/releases/tag/v0.14.0) (2018-04-11)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0-rc.6...v0.14.0)

 * Cosmetic changes for group UI

Changes in [0.14.0-rc.6](https://github.com/vector-im/riot-web/releases/tag/v0.14.0-rc.6) (2018-04-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0-rc.5...v0.14.0-rc.6)

 * Bump react-sdk to [rc.6](https://github.com/matrix-org/matrix-react-sdk/releases/tag/v0.12.0-rc.6)

Changes in [0.14.0-rc.5](https://github.com/vector-im/riot-web/releases/tag/v0.14.0-rc.5) (2018-04-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0-rc.4...v0.14.0-rc.5)

* Add CSS for new control to set group join policy

Changes in [0.14.0-rc.4](https://github.com/vector-im/riot-web/releases/tag/v0.14.0-rc.4) (2018-03-22)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0-rc.3...v0.14.0-rc.4)

 * Fix tagging rooms as direct messages

Changes in [0.14.0-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.14.0-rc.3) (2018-03-20)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0-rc.2...v0.14.0-rc.3)

 * Fix a bug where the badge on a room tile would not update
   when a room was read from a different device.

Changes in [0.14.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.14.0-rc.2) (2018-03-19)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.14.0-rc.1...v0.14.0-rc.2)

 * Take TagPanel out of labs
   [\#6347](https://github.com/vector-im/riot-web/pull/6347)
 * Add languages (czech, galician and serbian)
   [\#6343](https://github.com/vector-im/riot-web/pull/6343)

Changes in [0.14.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.14.0-rc.1) (2018-03-19)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.5...v0.14.0-rc.1)

 * Force update RoomSubList after reading a room
   [\#6342](https://github.com/vector-im/riot-web/pull/6342)
 * Ensure entire LeftPanel is faded when settings open
   [\#6340](https://github.com/vector-im/riot-web/pull/6340)
 * Update from Weblate.
   [\#6330](https://github.com/vector-im/riot-web/pull/6330)
 * Implement a simple shouldComponentUpdate for DNDRoomTile
   [\#6313](https://github.com/vector-im/riot-web/pull/6313)
 * Remove og:image with status.im URL
   [\#6317](https://github.com/vector-im/riot-web/pull/6317)
 * Add change delay warning in GroupView settings
   [\#6316](https://github.com/vector-im/riot-web/pull/6316)
 * Correctly position mx_TagPanel_clearButton
   [\#6289](https://github.com/vector-im/riot-web/pull/6289)
 * Fix gap between avatar and border
   [\#6290](https://github.com/vector-im/riot-web/pull/6290)
 * Fix bug where cannot send group invite on GroupMemberInfo phase
   [\#6303](https://github.com/vector-im/riot-web/pull/6303)
 * Fix themeing bug with Firefox where "disabled" ignored
   [\#6301](https://github.com/vector-im/riot-web/pull/6301)
 * Changes for E2E "fudge-button"
   [\#6288](https://github.com/vector-im/riot-web/pull/6288)
 * Make sure mx_TagPanel_tagTileContainer occupies full height
   [\#6286](https://github.com/vector-im/riot-web/pull/6286)
 * Add transparent CSS class for RoomTile
   [\#6281](https://github.com/vector-im/riot-web/pull/6281)
 * Fix crash; fs event received /w langauge file empty
   [\#6273](https://github.com/vector-im/riot-web/pull/6273)
 * Add setting to disable TagPanel
   [\#6269](https://github.com/vector-im/riot-web/pull/6269)
 * CSS for my groups microcopy
   [\#6257](https://github.com/vector-im/riot-web/pull/6257)
 * Add Bulgarian to the list of languages
   [\#6246](https://github.com/vector-im/riot-web/pull/6246)
 * Make media dropdown wider
   [\#6245](https://github.com/vector-im/riot-web/pull/6245)
 * Make dropdowns with long options degrade more gracefully
   [\#6244](https://github.com/vector-im/riot-web/pull/6244)
 * Fix un-tinted "View Community" icon in TagTile context menu
   [\#6223](https://github.com/vector-im/riot-web/pull/6223)
 * Fix RoomDropTarget and emptySubListTip to have containers
   [\#6160](https://github.com/vector-im/riot-web/pull/6160)
 * Fix syntax error of wrong use of self-closing HTML tag
   [\#6154](https://github.com/vector-im/riot-web/pull/6154)
 * Use translucent black for RoomSubList bg to fix tinting
   [\#6227](https://github.com/vector-im/riot-web/pull/6227)
 * CSS for changing "R" to "X" for clearing group filter
   [\#6216](https://github.com/vector-im/riot-web/pull/6216)
 * CSS for new global TagPanel filter
   [\#6187](https://github.com/vector-im/riot-web/pull/6187)
 * Separate the middle panel from the room list
   [\#6194](https://github.com/vector-im/riot-web/pull/6194)
 * Only use DNDRoomTile for editable sub lists
   [\#6176](https://github.com/vector-im/riot-web/pull/6176)
 * Adjust CSS to prevent scrollbars on message panel spinner
   [\#6131](https://github.com/vector-im/riot-web/pull/6131)
 * Implement riot-web side of dragging GroupTile avatars to TagPanel
   [\#6143](https://github.com/vector-im/riot-web/pull/6143)
 * Fix LeftPanel size being incorrect when TagPanel disabled
   [\#6140](https://github.com/vector-im/riot-web/pull/6140)
 * Fix TagPanel from collapsing to < 60px when LP collapsed
   [\#6134](https://github.com/vector-im/riot-web/pull/6134)
 * Temporary hack to constrain LLP container size.
   [\#6138](https://github.com/vector-im/riot-web/pull/6138)
 * Fix typo
   [\#6137](https://github.com/vector-im/riot-web/pull/6137)
 * Add context menu to TagPanel
   [\#6127](https://github.com/vector-im/riot-web/pull/6127)
 * Make room tagging flux-y
   [\#6096](https://github.com/vector-im/riot-web/pull/6096)
 * Move groups button to TagPanel
   [\#6130](https://github.com/vector-im/riot-web/pull/6130)
 * Fix long group name pushing settings cog into void
   [\#6106](https://github.com/vector-im/riot-web/pull/6106)
 * Fix horizontal scrollbar under certain circumstances
   [\#6103](https://github.com/vector-im/riot-web/pull/6103)
 * Split MImageBody into MFileBody to match JS Classes.
   [\#6067](https://github.com/vector-im/riot-web/pull/6067)
 * Add Catalan
   [\#6040](https://github.com/vector-im/riot-web/pull/6040)
 * Update from Weblate.
   [\#5777](https://github.com/vector-im/riot-web/pull/5777)
 * make FilteredList controlled, such that it can externally persist filter
   [\#5718](https://github.com/vector-im/riot-web/pull/5718)
 * Linear Rich Quoting
   [\#6017](https://github.com/vector-im/riot-web/pull/6017)
 * Highlight ViewSource and Devtools ViewSource
   [\#5995](https://github.com/vector-im/riot-web/pull/5995)
 * default url, not domain
   [\#6022](https://github.com/vector-im/riot-web/pull/6022)
 * T3chguy/num members tooltip
   [\#5929](https://github.com/vector-im/riot-web/pull/5929)
 * Swap RoomList to react-beautiful-dnd
   [\#6008](https://github.com/vector-im/riot-web/pull/6008)
 * CSS required as part of moving TagPanel from react-dnd to react-beautiful-
   dnd
   [\#5992](https://github.com/vector-im/riot-web/pull/5992)
 * fix&refactor DateSeparator and MessageTimestamp
   [\#5984](https://github.com/vector-im/riot-web/pull/5984)
 * Iterative fixes on Rich Quoting
   [\#5978](https://github.com/vector-im/riot-web/pull/5978)
 * move piwik whitelists to conf and add piwik config.json info to readme
   [\#5653](https://github.com/vector-im/riot-web/pull/5653)
 * Implement Rich Quoting/Replies
   [\#5804](https://github.com/vector-im/riot-web/pull/5804)
 * Change author
   [\#5950](https://github.com/vector-im/riot-web/pull/5950)
 * Revert "Add a &nbsp; after timestamp"
   [\#5944](https://github.com/vector-im/riot-web/pull/5944)
 * Add a &nbsp; after timestamp
   [\#3046](https://github.com/vector-im/riot-web/pull/3046)
 * Corrected language name
   [\#5938](https://github.com/vector-im/riot-web/pull/5938)
 * Hide Options button from copy to clipboard
   [\#2892](https://github.com/vector-im/riot-web/pull/2892)
 * Fix for `If riot is narrow enough, such that 'Send a message (unecrypted)'
   wraps to a second line, the timeline doesn't fit the window.`
   [\#5900](https://github.com/vector-im/riot-web/pull/5900)
 * Screenshot UI
   [\#5849](https://github.com/vector-im/riot-web/pull/5849)
 * add missing config.json entry such that scalar-staging widgets work
   [\#5855](https://github.com/vector-im/riot-web/pull/5855)
 * add dark theme styling to devtools input box
   [\#5610](https://github.com/vector-im/riot-web/pull/5610)
 * Fixes #1953 by adding oivoodoo as author
   [\#5851](https://github.com/vector-im/riot-web/pull/5851)
 * Instructions on security issues
   [\#5824](https://github.com/vector-im/riot-web/pull/5824)
 * Move DND wrapper to top level component
   [\#5790](https://github.com/vector-im/riot-web/pull/5790)
 * Widget title bar max / min visual cues.
   [\#5786](https://github.com/vector-im/riot-web/pull/5786)
 * Implement renumeration of ordered tags upon collision
   [\#5759](https://github.com/vector-im/riot-web/pull/5759)
 * Update imports for accessing KeyCode
   [\#5751](https://github.com/vector-im/riot-web/pull/5751)
 * Set html lang attribute from language setting
   [\#5685](https://github.com/vector-im/riot-web/pull/5685)
 * CSS for new TagPanel
   [\#5723](https://github.com/vector-im/riot-web/pull/5723)
 * getGroupStore no longer needs a matrix client
   [\#5707](https://github.com/vector-im/riot-web/pull/5707)
 * CSS required for moving group publication toggles to UserSettings
   [\#5702](https://github.com/vector-im/riot-web/pull/5702)
 * Make sure the SettingsStore is ready to load the theme before loading it
   [\#5630](https://github.com/vector-im/riot-web/pull/5630)
 * Add some aria-labels to RightPanel
   [\#5661](https://github.com/vector-im/riot-web/pull/5661)
 * Use badge count format for member count in RightPanel
   [\#5657](https://github.com/vector-im/riot-web/pull/5657)
 * Exclude the default language on page load
   [\#5640](https://github.com/vector-im/riot-web/pull/5640)
 * Use SettingsStore to get the default theme
   [\#5615](https://github.com/vector-im/riot-web/pull/5615)
 * Refactor translations
   [\#5613](https://github.com/vector-im/riot-web/pull/5613)
 * TintableSvgButton styling
   [\#5605](https://github.com/vector-im/riot-web/pull/5605)
 * Granular settings
   [\#5468](https://github.com/vector-im/riot-web/pull/5468)
 * CSS/components for custom presence controls
   [\#5286](https://github.com/vector-im/riot-web/pull/5286)
 * Set widget tile background colour
   [\#5574](https://github.com/vector-im/riot-web/pull/5574)
 * Widget styling tweaks
   [\#5573](https://github.com/vector-im/riot-web/pull/5573)
 * Center mixed content warnings in panel.
   [\#5567](https://github.com/vector-im/riot-web/pull/5567)
 * Status.im theme
   [\#5578](https://github.com/vector-im/riot-web/pull/5578)

Changes in [0.13.5](https://github.com/vector-im/riot-web/releases/tag/v0.13.5) (2018-02-09)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.4...v0.13.5)

 * SECURITY UPDATE: Sanitise URLs from 'external_url'. Thanks to walle303 for contacting
   us about this vulnerability.

Changes in [0.13.4](https://github.com/vector-im/riot-web/releases/tag/v0.13.4) (2018-01-03)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.3...v0.13.4)

 * Change config of riot.im electron build to fix some widgets not working. This only affects
   electron builds using the riot.im config - for all other builds, this is identical to
   v0.13.3.

Changes in [0.13.3](https://github.com/vector-im/riot-web/releases/tag/v0.13.3) (2017-12-04)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.2...v0.13.3)

 * Bump js-sdk, react-sdk version to pull in fix for [setting room publicity in a group](https://github.com/matrix-org/matrix-js-sdk/commit/aa3201ebb0fff5af2fb733080aa65ed1f7213de6).

Changes in [0.13.2](https://github.com/vector-im/riot-web/releases/tag/v0.13.2) (2017-11-28)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.1...v0.13.2)


Changes in [0.13.1](https://github.com/vector-im/riot-web/releases/tag/v0.13.1) (2017-11-17)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.0...v0.13.1)

 * SECURITY UPDATE: Fix the force TURN option for inbound calls. This option forced the use
   of TURN but only worked for outbound calls and not inbound calls. This means that if you
   enabled this option expecting it to mask your IP address in calls, your IP would still
   have been revealed to the room if you accepted an incoming call.
 * Also adds the Slovak translation.

Changes in [0.13.0](https://github.com/vector-im/riot-web/releases/tag/v0.13.0) (2017-11-15)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.0-rc.3...v0.13.0)


Changes in [0.13.0-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.13.0-rc.3) (2017-11-14)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.0-rc.2...v0.13.0-rc.3)


Changes in [0.13.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.13.0-rc.2) (2017-11-10)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.13.0-rc.1...v0.13.0-rc.2)

 * Make groups a fully-fleged baked-in feature
   [\#5566](https://github.com/vector-im/riot-web/pull/5566)

Changes in [0.13.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.13.0-rc.1) (2017-11-10)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.7...v0.13.0-rc.1)

 * Fix app tile margins.
   [\#5561](https://github.com/vector-im/riot-web/pull/5561)
 * Fix wrapping of long room topics (and overlap with apps)
   [\#5549](https://github.com/vector-im/riot-web/pull/5549)
 * Don't display widget iframes whilst loading.
   [\#5555](https://github.com/vector-im/riot-web/pull/5555)
 * Update from Weblate.
   [\#5558](https://github.com/vector-im/riot-web/pull/5558)
 * Adjust CSS for GroupView
   [\#5543](https://github.com/vector-im/riot-web/pull/5543)
 * CSS for adding rooms to a group with visibility
   [\#5546](https://github.com/vector-im/riot-web/pull/5546)
 * CSS for pinned indicators
   [\#5511](https://github.com/vector-im/riot-web/pull/5511)
 * Implement general-purpose tooltip "(?)"-style
   [\#5540](https://github.com/vector-im/riot-web/pull/5540)
 * CSS for improving group creation UX, namely setting long description
   [\#5535](https://github.com/vector-im/riot-web/pull/5535)
 * CSS for room notif pills in composer
   [\#5531](https://github.com/vector-im/riot-web/pull/5531)
 * Do not init a group store when no groupId specified
   [\#5520](https://github.com/vector-im/riot-web/pull/5520)
 * CSS for new pinned events indicator
   [\#5293](https://github.com/vector-im/riot-web/pull/5293)
 * T3chguy/devtools 1
   [\#5471](https://github.com/vector-im/riot-web/pull/5471)
 * Use margin to separate "perms" in the room directory
   [\#5498](https://github.com/vector-im/riot-web/pull/5498)
 * Add CSS for CreateGroupDialog to give group ID input suffix and prefix style
   [\#5505](https://github.com/vector-im/riot-web/pull/5505)
 * Fix group invites such that they look similar to room invites
   [\#5504](https://github.com/vector-im/riot-web/pull/5504)
 * CSS for Your Communities scrollbar
   [\#5501](https://github.com/vector-im/riot-web/pull/5501)
 * Add toggle to alter visibility of room-group association
   [\#5497](https://github.com/vector-im/riot-web/pull/5497)
 * CSS for room notification pills
   [\#5494](https://github.com/vector-im/riot-web/pull/5494)
 * Implement simple GroupRoomInfo
   [\#5493](https://github.com/vector-im/riot-web/pull/5493)
 * Add back bottom border to widget title bar
   [\#5458](https://github.com/vector-im/riot-web/pull/5458)
 * Prevent group name looking clickable for non-members
   [\#5478](https://github.com/vector-im/riot-web/pull/5478)
 * Fix instanceof check, was checking against the Package rather than class
   [\#5472](https://github.com/vector-im/riot-web/pull/5472)
 * Use correct group store state when rendering "Invite to this community"
   [\#5455](https://github.com/vector-im/riot-web/pull/5455)
 * Leverages ES6 in Notifications
   [\#5453](https://github.com/vector-im/riot-web/pull/5453)
 * Re-PR #4412
   [\#5437](https://github.com/vector-im/riot-web/pull/5437)
 * fix comma error of features example
   [\#5410](https://github.com/vector-im/riot-web/pull/5410)
 * Devtools: make filtering case-insensitive
   [\#5387](https://github.com/vector-im/riot-web/pull/5387)
 * Highlight group members icon in group member info
   [\#5432](https://github.com/vector-im/riot-web/pull/5432)
 * Use CSS to stop greyed Right/LeftPanel UI from being interactable
   [\#5422](https://github.com/vector-im/riot-web/pull/5422)
 * CSS for preventing editing of UI requiring user privilege if user
   unprivileged
   [\#5417](https://github.com/vector-im/riot-web/pull/5417)
 * Only show UI for adding rooms/users to groups to privileged users
   [\#5409](https://github.com/vector-im/riot-web/pull/5409)
 * Only show "Invite to this community" when viewing group members
   [\#5407](https://github.com/vector-im/riot-web/pull/5407)
 * Add trash can icon for delete widget
   [\#5397](https://github.com/vector-im/riot-web/pull/5397)
 * CSS to improve MyGroups in general, and add placeholder
   [\#5375](https://github.com/vector-im/riot-web/pull/5375)
 * Rxl881/parallelshell
   [\#4881](https://github.com/vector-im/riot-web/pull/4881)
 * Custom server text was i18ned by key
   [\#5371](https://github.com/vector-im/riot-web/pull/5371)
 * Run prunei18n
   [\#5370](https://github.com/vector-im/riot-web/pull/5370)
 * Update from Weblate.
   [\#5369](https://github.com/vector-im/riot-web/pull/5369)
 * Add script to prune unused translations
   [\#5339](https://github.com/vector-im/riot-web/pull/5339)
 * CSS for improved MyGroups page
   [\#5360](https://github.com/vector-im/riot-web/pull/5360)
 * Add padding-right to Dialogs
   [\#5346](https://github.com/vector-im/riot-web/pull/5346)
 * Add div.warning and use the scss var
   [\#5344](https://github.com/vector-im/riot-web/pull/5344)
 * Groups->Communities
   [\#5343](https://github.com/vector-im/riot-web/pull/5343)
 * Make the 'add rooms' button clickable
   [\#5342](https://github.com/vector-im/riot-web/pull/5342)
 * Switch to gen-i18n script
   [\#5338](https://github.com/vector-im/riot-web/pull/5338)
 * Use _t as _t
   [\#5334](https://github.com/vector-im/riot-web/pull/5334)
 * fix groupview header editing visuals (pt 1)
   [\#5330](https://github.com/vector-im/riot-web/pull/5330)
 * bump version to prevent eslint errors
   [\#5316](https://github.com/vector-im/riot-web/pull/5316)
 * CSS for invited group members section
   [\#5303](https://github.com/vector-im/riot-web/pull/5303)
 * Handle long names in EntityTiles by overflowing correctly
   [\#5302](https://github.com/vector-im/riot-web/pull/5302)
 * Disable labs in electron
   [\#5296](https://github.com/vector-im/riot-web/pull/5296)
 * CSS for Modifying GroupView UI matrix-org/matrix-react-sdk#1475
   [\#5295](https://github.com/vector-im/riot-web/pull/5295)
 * Message/event pinning
   [\#5142](https://github.com/vector-im/riot-web/pull/5142)
 * Sorting of networks within a protocol based on name
   [\#4054](https://github.com/vector-im/riot-web/pull/4054)
 * allow hiding of notification body for privacy reasons
   [\#4988](https://github.com/vector-im/riot-web/pull/4988)
 * Don't use MXIDs on the lightbox if possible
   [\#5281](https://github.com/vector-im/riot-web/pull/5281)
 * CSS for lonely room message
   [\#5267](https://github.com/vector-im/riot-web/pull/5267)
 * Bring back dark theme code block border
   [\#5037](https://github.com/vector-im/riot-web/pull/5037)
 * CSS for remove avatar buttons
   [\#5282](https://github.com/vector-im/riot-web/pull/5282)

Changes in [0.12.7](https://github.com/vector-im/riot-web/releases/tag/v0.12.7) (2017-10-16)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.7-rc.3...v0.12.7)

 * Released versions of react-sdk & js-sdk

Changes in [0.12.7-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.12.7-rc.3) (2017-10-13)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.7-rc.2...v0.12.7-rc.3)

 * Hide the join group button
   [\#5275](https://github.com/vector-im/riot-web/pull/5275)

Changes in [0.12.7-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.12.7-rc.2) (2017-10-13)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.7-rc.1...v0.12.7-rc.2)


Changes in [0.12.7-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.12.7-rc.1) (2017-10-13)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.6...v0.12.7-rc.1)

 * switch to new logos, and use import rather than VAR
   [\#5203](https://github.com/vector-im/riot-web/pull/5203)
 * Clarify what an integrations server is
   [\#5266](https://github.com/vector-im/riot-web/pull/5266)
 * Update from Weblate.
   [\#5269](https://github.com/vector-im/riot-web/pull/5269)
 * Remove trailing comma in JSON
   [\#5167](https://github.com/vector-im/riot-web/pull/5167)
 * Added default_federate property
   [\#3849](https://github.com/vector-im/riot-web/pull/3849)
 * CSS for greying out login form
   [\#5197](https://github.com/vector-im/riot-web/pull/5197)
 * Fix bug that made sub list placeholders not show for ILAG etc.
   [\#5164](https://github.com/vector-im/riot-web/pull/5164)
 * Factor out EditableItemList component from AliasSettings
   [\#5161](https://github.com/vector-im/riot-web/pull/5161)
 * Mark and remove some translations
   [\#5110](https://github.com/vector-im/riot-web/pull/5110)
 * CSS for "remove" button on GroupRoomTile
   [\#5141](https://github.com/vector-im/riot-web/pull/5141)
 * Create basic icon for the GroupRoomList tab and adding rooms to groups
   [\#5140](https://github.com/vector-im/riot-web/pull/5140)
 * Add button to get to MyGroups
   [\#5131](https://github.com/vector-im/riot-web/pull/5131)
 * Remove `key` prop pass-thru on HeaderButton
   [\#5137](https://github.com/vector-im/riot-web/pull/5137)
 * Implement "Add room to group" feature
   [\#5125](https://github.com/vector-im/riot-web/pull/5125)
 * Add Jitsi screensharing support in electron app
   [\#4967](https://github.com/vector-im/riot-web/pull/4967)
 * Refactor right panel header buttons
   [\#5117](https://github.com/vector-im/riot-web/pull/5117)
 * CSS for publicity status & toggle button
   [\#5104](https://github.com/vector-im/riot-web/pull/5104)
 * CSS for "X" in top right of features users/rooms
   [\#5103](https://github.com/vector-im/riot-web/pull/5103)
 * Include Finnish translation
   [\#5051](https://github.com/vector-im/riot-web/pull/5051)
 * Redesign membership section of GroupView
   [\#5096](https://github.com/vector-im/riot-web/pull/5096)
 * Make --config accept globs
   [\#5090](https://github.com/vector-im/riot-web/pull/5090)
 * CSS for GroupView: Add a User
   [\#5093](https://github.com/vector-im/riot-web/pull/5093)
 * T3chguy/devtools 1
   [\#5074](https://github.com/vector-im/riot-web/pull/5074)
 * Alter opacity for flair
   [\#5085](https://github.com/vector-im/riot-web/pull/5085)
 * Fix ugly integ button
   [\#5082](https://github.com/vector-im/riot-web/pull/5082)
 * Group Membership UI
   [\#4830](https://github.com/vector-im/riot-web/pull/4830)

Changes in [0.12.6](https://github.com/vector-im/riot-web/releases/tag/v0.12.6) (2017-09-21)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.5...v0.12.6)

 * Use matrix-js-sdk v0.8.4 to fix build

Changes in [0.12.5](https://github.com/vector-im/riot-web/releases/tag/v0.12.5) (2017-09-21)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.4...v0.12.5)

 * Use react-sdk v0.10.5 to fix build

Changes in [0.12.4](https://github.com/vector-im/riot-web/releases/tag/v0.12.4) (2017-09-20)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.4-rc.1...v0.12.4)

 * No changes

Changes in [0.12.4-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.12.4-rc.1) (2017-09-19)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.3...v0.12.4-rc.1)

 * Fix test for new behaviour of 'joining' flag
   [\#5053](https://github.com/vector-im/riot-web/pull/5053)
 * fix really dumb blunder/typo preventing system from going to sleep.
   [\#5080](https://github.com/vector-im/riot-web/pull/5080)
 * T3chguy/devtools
   [\#4735](https://github.com/vector-im/riot-web/pull/4735)
 * CSS for unignore button in UserSettings
   [\#5042](https://github.com/vector-im/riot-web/pull/5042)
 * Fix alias on home page for identity room
   [\#5044](https://github.com/vector-im/riot-web/pull/5044)
 * generic contextual menu for tooltip/responses
   [\#4989](https://github.com/vector-im/riot-web/pull/4989)
 * Update from Weblate.
   [\#5018](https://github.com/vector-im/riot-web/pull/5018)
 * Avoid re-rendering RoomList on room switch
   [\#5015](https://github.com/vector-im/riot-web/pull/5015)
 * Fix menu on change keyboard language issue #4345
   [\#4623](https://github.com/vector-im/riot-web/pull/4623)
 * Make isInvite default to false
   [\#4999](https://github.com/vector-im/riot-web/pull/4999)
 * Revert "Implement sticky date separators"
   [\#4991](https://github.com/vector-im/riot-web/pull/4991)
 * Implement sticky date separators
   [\#4939](https://github.com/vector-im/riot-web/pull/4939)

Changes in [0.12.3](https://github.com/vector-im/riot-web/releases/tag/v0.12.3) (2017-09-06)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.3-rc.3...v0.12.3)

 * No changes

Changes in [0.12.3-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.12.3-rc.3) (2017-09-05)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.3-rc.2...v0.12.3-rc.3)

 * Fix plurals in translations
   [\#4971](https://github.com/vector-im/riot-web/pull/4971)
 * Update from Weblate.
   [\#4968](https://github.com/vector-im/riot-web/pull/4968)

Changes in [0.12.3-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.12.3-rc.2) (2017-09-05)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.3-rc.1...v0.12.3-rc.2)

 * New react-sdk version to pull in new translations and fix some translation bugs.


Changes in [0.12.3-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.12.3-rc.1) (2017-09-01)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.2...v0.12.3-rc.1)

 * Fix overflowing login/register buttons on some languages issue #4804
   [\#4858](https://github.com/vector-im/riot-web/pull/4858)
 * Update vector-im to riot-im on Login
   [\#4943](https://github.com/vector-im/riot-web/pull/4943)
 * lets let people know that the bug report actually sent properly :)
   [\#4910](https://github.com/vector-im/riot-web/pull/4910)
 * another s/vector/riot/ in README
   [\#4934](https://github.com/vector-im/riot-web/pull/4934)
 * fix two room list regressions
   [\#4907](https://github.com/vector-im/riot-web/pull/4907)

Changes in [0.12.2](https://github.com/vector-im/riot-web/releases/tag/v0.12.2) (2017-08-24)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.1...v0.12.2)

 * Update react-sdk and js-sdk to fix bugs with incoming calls, messages and notifications
   in encrypted rooms.

Changes in [0.12.1](https://github.com/vector-im/riot-web/releases/tag/v0.12.1) (2017-08-23)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.1-rc.1...v0.12.1)

 * [No changes]

Changes in [0.12.1-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.12.1-rc.1) (2017-08-22)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.12.0-rc.2...v0.12.1-rc.1)

 * Update from Weblate.
   [\#4832](https://github.com/vector-im/riot-web/pull/4832)
 * Misc styling fixes.
   [\#4826](https://github.com/vector-im/riot-web/pull/4826)
 * Show / Hide apps icons
   [\#4774](https://github.com/vector-im/riot-web/pull/4774)

Changes in [0.12.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.12.0-rc.1) (2017-08-16)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.4...v0.12.0-rc.1)

 * Update from Weblate.
   [\#4797](https://github.com/vector-im/riot-web/pull/4797)
 * move focus-via-up/down cursors to LeftPanel
   [\#4777](https://github.com/vector-im/riot-web/pull/4777)
 * Remove userId property on RightPanel
   [\#4775](https://github.com/vector-im/riot-web/pull/4775)
 * Make member device info buttons fluid and stackable with flexbox
   [\#4776](https://github.com/vector-im/riot-web/pull/4776)
 * un-i18n Modal Analytics
   [\#4688](https://github.com/vector-im/riot-web/pull/4688)
 * Quote using innerText
   [\#4773](https://github.com/vector-im/riot-web/pull/4773)
 * Karma tweaks for riot-web
   [\#4765](https://github.com/vector-im/riot-web/pull/4765)
 * Fix typo with scripts/fetch-develop-deps.sh in Building From Source
   [\#4764](https://github.com/vector-im/riot-web/pull/4764)
 * Adjust CSS for optional avatars in pills
   [\#4757](https://github.com/vector-im/riot-web/pull/4757)
 * Fix crypto on develop
   [\#4754](https://github.com/vector-im/riot-web/pull/4754)
 * Fix signing key url in readme
   [\#4464](https://github.com/vector-im/riot-web/pull/4464)
 * update gitignore to allow .idea directory to exist in subdirs
   [\#4749](https://github.com/vector-im/riot-web/pull/4749)
 * tweak compact theme
   [\#4665](https://github.com/vector-im/riot-web/pull/4665)
 * Update draft-js from 0.10.1 to 0.11.0-alpha
   [\#4740](https://github.com/vector-im/riot-web/pull/4740)
 * electron support for mouse forward/back buttons in Windows
   [\#4739](https://github.com/vector-im/riot-web/pull/4739)
 * Update draft-js from 0.8.1 to 0.10.1
   [\#4730](https://github.com/vector-im/riot-web/pull/4730)
 * Make pills, emoji translucent when sending
   [\#4693](https://github.com/vector-im/riot-web/pull/4693)
 * Widget permissions styling and icon
   [\#4690](https://github.com/vector-im/riot-web/pull/4690)
 * CSS required for composer autoscroll
   [\#4682](https://github.com/vector-im/riot-web/pull/4682)
 * CSS for group edit UI
   [\#4608](https://github.com/vector-im/riot-web/pull/4608)
 * Fix a couple of minor errors in the room list
   [\#4671](https://github.com/vector-im/riot-web/pull/4671)
 * Styling for beta testing icon.
   [\#4584](https://github.com/vector-im/riot-web/pull/4584)
 * Increase the timeout for clearing indexeddbs
   [\#4650](https://github.com/vector-im/riot-web/pull/4650)
 * Make some adjustments to mx_UserPill and mx_RoomPill
   [\#4597](https://github.com/vector-im/riot-web/pull/4597)
 * Apply CSS to <pre> tags to distinguish them from each other
   [\#4639](https://github.com/vector-im/riot-web/pull/4639)
 * Use `catch` instead of `fail` to handle room tag error
   [\#4643](https://github.com/vector-im/riot-web/pull/4643)
 * CSS for decorated matrix.to links in the composer
   [\#4583](https://github.com/vector-im/riot-web/pull/4583)
 * Deflake the joining test
   [\#4579](https://github.com/vector-im/riot-web/pull/4579)
 * Bump react to 15.6 to fix build problems
   [\#4577](https://github.com/vector-im/riot-web/pull/4577)
 * Improve AppTile menu bar button styling.
   [\#4567](https://github.com/vector-im/riot-web/pull/4567)
 * Transform `async` functions to bluebird promises
   [\#4572](https://github.com/vector-im/riot-web/pull/4572)
 * use flushAllExpected in joining test
   [\#4570](https://github.com/vector-im/riot-web/pull/4570)
 * Switch riot-web to bluebird
   [\#4565](https://github.com/vector-im/riot-web/pull/4565)
 * loading tests: wait for login component
   [\#4564](https://github.com/vector-im/riot-web/pull/4564)
 * Remove CSS for the MessageComposerInputOld
   [\#4568](https://github.com/vector-im/riot-web/pull/4568)
 * Implement the focus_room_filter action
   [\#4560](https://github.com/vector-im/riot-web/pull/4560)
 * CSS for Rooms in Group View
   [\#4530](https://github.com/vector-im/riot-web/pull/4530)
 * more HomePage tweaks
   [\#4557](https://github.com/vector-im/riot-web/pull/4557)
 * Give HomePage an unmounted guard
   [\#4556](https://github.com/vector-im/riot-web/pull/4556)
 * Take RTE out of labs
   [\#4500](https://github.com/vector-im/riot-web/pull/4500)
 * CSS for Groups page
   [\#4468](https://github.com/vector-im/riot-web/pull/4468)
 * CSS for GroupView
   [\#4442](https://github.com/vector-im/riot-web/pull/4442)
 * remove unused class
   [\#4525](https://github.com/vector-im/riot-web/pull/4525)
 * Fix long words causing MessageComposer to widen
   [\#4466](https://github.com/vector-im/riot-web/pull/4466)
 * Add visual bell animation for RTE
   [\#4516](https://github.com/vector-im/riot-web/pull/4516)
 * Truncate auto-complete pills properly
   [\#4502](https://github.com/vector-im/riot-web/pull/4502)
 * Use chrome headless instead of phantomjs
   [\#4512](https://github.com/vector-im/riot-web/pull/4512)
 * Use external mock-request
   [\#4489](https://github.com/vector-im/riot-web/pull/4489)
 * fix Quote not closing contextual menu
   [\#4443](https://github.com/vector-im/riot-web/pull/4443)
 * Apply white-space: pre-wrap to mx_MEmoteBody
   [\#4470](https://github.com/vector-im/riot-web/pull/4470)
 * Add some style improvements to autocompletions
   [\#4456](https://github.com/vector-im/riot-web/pull/4456)
 * Styling for apps / widgets
   [\#4447](https://github.com/vector-im/riot-web/pull/4447)
 * Attempt to flush the rageshake logs on close
   [\#4400](https://github.com/vector-im/riot-web/pull/4400)
 * Update from Weblate.
   [\#4401](https://github.com/vector-im/riot-web/pull/4401)
 * improve update polling electron and provide a manual check for updates
   button
   [\#4176](https://github.com/vector-im/riot-web/pull/4176)
 * Fix load failure in firefox when indexedDB is disabled
   [\#4395](https://github.com/vector-im/riot-web/pull/4395)
 * Change missed 'Redact' to 'Remove' in ImageView.
   [\#4362](https://github.com/vector-im/riot-web/pull/4362)
 * explicit convert to nativeImage to stabilise trayIcon on Windows [Electron]
   [\#4355](https://github.com/vector-im/riot-web/pull/4355)
 * Use _tJsx for PasswordNagBar (because it has <u>)
   [\#4373](https://github.com/vector-im/riot-web/pull/4373)
 * Clean up some log outputs from the integ tests
   [\#4376](https://github.com/vector-im/riot-web/pull/4376)
 * CSS for redeisng of password warning
   [\#4367](https://github.com/vector-im/riot-web/pull/4367)
 * Give _t to PasswordNagBar, add CSS for UserSettings password warning
   [\#4366](https://github.com/vector-im/riot-web/pull/4366)
 * Update from Weblate.
   [\#4361](https://github.com/vector-im/riot-web/pull/4361)
 * Update from Weblate.
   [\#4360](https://github.com/vector-im/riot-web/pull/4360)
 * Test 'return-to-app' functionality
   [\#4352](https://github.com/vector-im/riot-web/pull/4352)
 * Update from Weblate.
   [\#4354](https://github.com/vector-im/riot-web/pull/4354)
 * onLoadCompleted is now onTokenLoginCompleted
   [\#4335](https://github.com/vector-im/riot-web/pull/4335)
 * Tweak tests to match updates to matrixchat
   [\#4325](https://github.com/vector-im/riot-web/pull/4325)
 * Update from Weblate.
   [\#4346](https://github.com/vector-im/riot-web/pull/4346)
 * change dispatcher forward_event signature
   [\#4337](https://github.com/vector-im/riot-web/pull/4337)
 * Add border on hover for code blocks
   [\#4259](https://github.com/vector-im/riot-web/pull/4259)

Changes in [0.11.4](https://github.com/vector-im/riot-web/releases/tag/v0.11.4) (2017-06-22)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.3...v0.11.4)

 * Update matrix-js-sdk and react-sdk to fix a regression where the
   background indexedb worker was disabled, failures to open indexeddb
   causing the app to fail to start, a race when starting that could break
   switching to rooms, and the inability to invite users with mixed case
   usernames.

Changes in [0.11.3](https://github.com/vector-im/riot-web/releases/tag/v0.11.3) (2017-06-20)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.2...v0.11.3)

 * Update to matrix-react-sdk 0.9.6 to fix infinite spinner bugs
   and some parts of the app that had missed translation.

Changes in [0.11.2](https://github.com/vector-im/riot-web/releases/tag/v0.11.2) (2017-06-19)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.2-rc.2...v0.11.2)

 * Add more languages and translations
 * Add a 'register' button

Changes in [0.11.2-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.11.2-rc.2) (2017-06-16)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.2-rc.1...v0.11.2-rc.2)

 * Update react-sdk to pull in fixes for URL previews, CAS
   login, h2 in markdown and CAPTCHA forms.
 * Enable Korean translation
 * Update from Weblate.
   [\#4323](https://github.com/vector-im/riot-web/pull/4323)
 * Fix h2 in markdown being weird
   [\#4332](https://github.com/vector-im/riot-web/pull/4332)

Changes in [0.11.2-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.11.2-rc.1) (2017-06-15)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.1...v0.11.2-rc.1)

 * Attempts to deflakify the joining test
   [\#4313](https://github.com/vector-im/riot-web/pull/4313)
 * Add a test for the login flow when there is a teamserver
   [\#4315](https://github.com/vector-im/riot-web/pull/4315)
 * Remove onload simulator from loading test
   [\#4314](https://github.com/vector-im/riot-web/pull/4314)
 * Update from Weblate.
   [\#4305](https://github.com/vector-im/riot-web/pull/4305)
 * Test that we handle stored mx_last_room_id correctly
   [\#4292](https://github.com/vector-im/riot-web/pull/4292)
 * Ask for email address after setting password for the first time
   [\#4301](https://github.com/vector-im/riot-web/pull/4301)
 * i18n for setting email after password flow
   [\#4299](https://github.com/vector-im/riot-web/pull/4299)
 * Update from Weblate.
   [\#4290](https://github.com/vector-im/riot-web/pull/4290)
 * Don't show the tooltips when filtering rooms
   [\#4282](https://github.com/vector-im/riot-web/pull/4282)
 * Update from Weblate.
   [\#4272](https://github.com/vector-im/riot-web/pull/4272)
 * Add missing VOIP Dropdown width
   [\#4266](https://github.com/vector-im/riot-web/pull/4266)
 * Update import and directory path in the Translations dev guide
   [\#4261](https://github.com/vector-im/riot-web/pull/4261)
 * Use Thai string for Thai in Language-Chooser
   [\#4260](https://github.com/vector-im/riot-web/pull/4260)

Changes in [0.11.1](https://github.com/vector-im/riot-web/releases/tag/v0.11.1) (2017-06-14)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.0...v0.11.1)

 * Update to react-sdk 0.9.4 to prompt to set an
   email address when setting a password and make
   DM guessing smarter.

Changes in [0.11.0](https://github.com/vector-im/riot-web/releases/tag/v0.11.0) (2017-06-12)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.0-rc.2...v0.11.0)

 * More translations & minor fixes

Changes in [0.11.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.11.0-rc.2) (2017-06-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.11.0-rc.1...v0.11.0-rc.2)

 * Update to matrix-react-sdk rc.2 which fixes the flux
   dependency version and an issue with the conference
   call bar translation.


Changes in [0.11.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.11.0-rc.1) (2017-06-09)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.10.2...v0.11.0-rc.1)

 * Update from Weblate.
   [\#4258](https://github.com/vector-im/riot-web/pull/4258)
 * Update from Weblate.
   [\#4254](https://github.com/vector-im/riot-web/pull/4254)
 * Update from Weblate.
   [\#4253](https://github.com/vector-im/riot-web/pull/4253)
 * Expect to see HTTP /join/#some:alias when we the view knows it
   [\#4252](https://github.com/vector-im/riot-web/pull/4252)
 * Update from Weblate.
   [\#4250](https://github.com/vector-im/riot-web/pull/4250)
 * add explicit import to utf8 polyfill and rip out unused imports
   [\#4169](https://github.com/vector-im/riot-web/pull/4169)
 * Added styling for copy to clipboard button
   [\#4204](https://github.com/vector-im/riot-web/pull/4204)
 * Update from Weblate.
   [\#4231](https://github.com/vector-im/riot-web/pull/4231)
 * Update from Weblate.
   [\#4218](https://github.com/vector-im/riot-web/pull/4218)
 * Update CSS for ChatInviteDialog
   [\#4226](https://github.com/vector-im/riot-web/pull/4226)
 * change electron -> electron_app which was previously missed
   [\#4212](https://github.com/vector-im/riot-web/pull/4212)
 * New guest access
   [\#4039](https://github.com/vector-im/riot-web/pull/4039)
 * Align message timestamp centrally about the avatar mid-point
   [\#4219](https://github.com/vector-im/riot-web/pull/4219)
 * Remove '/' from homepage URL
   [\#4221](https://github.com/vector-im/riot-web/pull/4221)
 * Chop off 'origin/'
   [\#4220](https://github.com/vector-im/riot-web/pull/4220)
 * Update from Weblate.
   [\#4214](https://github.com/vector-im/riot-web/pull/4214)
 * adjust alignment of message menu button in compact layout
   [\#4211](https://github.com/vector-im/riot-web/pull/4211)
 * Update from Weblate.
   [\#4207](https://github.com/vector-im/riot-web/pull/4207)
 * Fix Tests in ILAG
   [\#4209](https://github.com/vector-im/riot-web/pull/4209)
 * Update from Weblate.
   [\#4197](https://github.com/vector-im/riot-web/pull/4197)
 * Fix tests for new-guest-access
   [\#4201](https://github.com/vector-im/riot-web/pull/4201)
 * i18n for SetPasswordDialog
   [\#4198](https://github.com/vector-im/riot-web/pull/4198)
 * Update from Weblate.
   [\#4193](https://github.com/vector-im/riot-web/pull/4193)
 * to make the windows volume mixer not explode as it can't resize icons.
   [\#4183](https://github.com/vector-im/riot-web/pull/4183)
 * provide react devtools in electron dev runs
   [\#4186](https://github.com/vector-im/riot-web/pull/4186)
 * Fix DeprecationWarning
   [\#4184](https://github.com/vector-im/riot-web/pull/4184)
 * room link should be a matrix.to one
   [\#4178](https://github.com/vector-im/riot-web/pull/4178)
 * Update home.html
   [\#4163](https://github.com/vector-im/riot-web/pull/4163)
 * Add missing translation for room directory
   [\#4160](https://github.com/vector-im/riot-web/pull/4160)
 * i18n welcome
   [\#4129](https://github.com/vector-im/riot-web/pull/4129)
 * Tom welcome page
   [\#4038](https://github.com/vector-im/riot-web/pull/4038)
 * Fix some tests that expect Directory (they should expect HomePage)
   [\#4076](https://github.com/vector-im/riot-web/pull/4076)
 * Add "Login" button to RHS when user is a guest
   [\#4037](https://github.com/vector-im/riot-web/pull/4037)
 * Rejig the PaswordNagBar
   [\#4026](https://github.com/vector-im/riot-web/pull/4026)
 * Allow team server config to be missing
   [\#4024](https://github.com/vector-im/riot-web/pull/4024)
 * Remove GuestWarningBar
   [\#4020](https://github.com/vector-im/riot-web/pull/4020)
 * Make left panel better for new users (mk III)
   [\#4023](https://github.com/vector-im/riot-web/pull/4023)
 * Implement default welcome page and allow custom URL /w config
   [\#4015](https://github.com/vector-im/riot-web/pull/4015)
 * Add warm-fuzzy for successful password entry
   [\#3989](https://github.com/vector-im/riot-web/pull/3989)
 * autoFocus new password input in SetPasswordDialog
   [\#3982](https://github.com/vector-im/riot-web/pull/3982)
 * Implement dialog to set password
   [\#3921](https://github.com/vector-im/riot-web/pull/3921)
 * Replace NeedToRegister with SetMxId dialog
   [\#3924](https://github.com/vector-im/riot-web/pull/3924)
 * Add welcomeUserId to sample config
   [\#3906](https://github.com/vector-im/riot-web/pull/3906)
 * CSS for mxIdDialog redesign
   [\#3885](https://github.com/vector-im/riot-web/pull/3885)
 * Implement PasswordNagBar
   [\#3817](https://github.com/vector-im/riot-web/pull/3817)
 * CSS for new SetMxIdDialog
   [\#3762](https://github.com/vector-im/riot-web/pull/3762)

Changes in [0.10.2](https://github.com/vector-im/riot-web/releases/tag/v0.10.2) (2017-06-06)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.10.1...v0.10.2)

 * Hotfix for bugs where navigating straight to a URL like /#/login and
   and /#/forgot_password


Changes in [0.10.1](https://github.com/vector-im/riot-web/releases/tag/v0.10.1) (2017-06-02)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.10.0...v0.10.1)

 * Update to matrix-react-sdk 0.9.1 to fix i18n error which broke start chat in some circumstances

Changes in [0.10.0](https://github.com/vector-im/riot-web/releases/tag/v0.10.0) (2017-06-02)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.10.0-rc.2...v0.10.0)

 * Update from Weblate.
   [\#4152](https://github.com/vector-im/riot-web/pull/4152)

Changes in [0.10.0-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.10.0-rc.2) (2017-06-02)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.10.0-rc.1...v0.10.0-rc.2)

 * Update from Weblate.
   [\#4150](https://github.com/vector-im/riot-web/pull/4150)
 * styling for webrtc settings
   [\#4019](https://github.com/vector-im/riot-web/pull/4019)
 * Update from Weblate.
   [\#4140](https://github.com/vector-im/riot-web/pull/4140)
 * add styles for compact layout
   [\#4132](https://github.com/vector-im/riot-web/pull/4132)
 * Various tweaks to fetch-develop-deps
   [\#4147](https://github.com/vector-im/riot-web/pull/4147)
 * Don't try to build with node 6.0
   [\#4145](https://github.com/vector-im/riot-web/pull/4145)
 * Support 12hr time on DateSeparator
   [\#4143](https://github.com/vector-im/riot-web/pull/4143)
 * Update from Weblate.
   [\#4137](https://github.com/vector-im/riot-web/pull/4137)
 * Update from Weblate.
   [\#4105](https://github.com/vector-im/riot-web/pull/4105)
 * Update from Weblate.
   [\#4094](https://github.com/vector-im/riot-web/pull/4094)
 * Update from Weblate.
   [\#4091](https://github.com/vector-im/riot-web/pull/4091)
 * Update from Weblate.
   [\#4089](https://github.com/vector-im/riot-web/pull/4089)
 * Update from Weblate.
   [\#4083](https://github.com/vector-im/riot-web/pull/4083)

Changes in [0.10.0-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.10.0-rc.1) (2017-06-01)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.10...v0.10.0-rc.1)

 * basic electron profile support
   [\#4030](https://github.com/vector-im/riot-web/pull/4030)
 * Finish translations for vector-im/riot-web
   [\#4122](https://github.com/vector-im/riot-web/pull/4122)
 * Translate src/vector
   [\#4119](https://github.com/vector-im/riot-web/pull/4119)
 * electron flashFrame was way too annoying
   [\#4128](https://github.com/vector-im/riot-web/pull/4128)
 * auto-launch support [Electron]
   [\#4012](https://github.com/vector-im/riot-web/pull/4012)
 * Show 12hr time on hover too
   [\#4092](https://github.com/vector-im/riot-web/pull/4092)
 * Translate src/notifications
   [\#4087](https://github.com/vector-im/riot-web/pull/4087)
 * Translate src/components/structures
   [\#4084](https://github.com/vector-im/riot-web/pull/4084)
 * Smaller font size on timestamp to better fit in the available space
   [\#4085](https://github.com/vector-im/riot-web/pull/4085)
 * Make travis run the build with several versions of node
   [\#4079](https://github.com/vector-im/riot-web/pull/4079)
 * Piwik Analytics
   [\#4056](https://github.com/vector-im/riot-web/pull/4056)
 * Update from Weblate.
   [\#4077](https://github.com/vector-im/riot-web/pull/4077)
 * managed to eat the eventStatus check, can't redact a local-echo etc
   [\#4078](https://github.com/vector-im/riot-web/pull/4078)
 * show redact in context menu only if has PL to/sent message
   [\#3925](https://github.com/vector-im/riot-web/pull/3925)
 * Update from Weblate.
   [\#4064](https://github.com/vector-im/riot-web/pull/4064)
 * Change redact -> remove to improve clarity
   [\#3722](https://github.com/vector-im/riot-web/pull/3722)
 * Update from Weblate.
   [\#4058](https://github.com/vector-im/riot-web/pull/4058)
 * Message Forwarding
   [\#3688](https://github.com/vector-im/riot-web/pull/3688)
 * Update from Weblate.
   [\#4057](https://github.com/vector-im/riot-web/pull/4057)
 * Fixed an input field's background color in dark theme
   [\#4053](https://github.com/vector-im/riot-web/pull/4053)
 * Update from Weblate.
   [\#4051](https://github.com/vector-im/riot-web/pull/4051)
 * Update from Weblate.
   [\#4049](https://github.com/vector-im/riot-web/pull/4049)
 * Update from Weblate.
   [\#4048](https://github.com/vector-im/riot-web/pull/4048)
 * Update from Weblate.
   [\#4040](https://github.com/vector-im/riot-web/pull/4040)
 * Update translating.md: Minor suggestions
   [\#4041](https://github.com/vector-im/riot-web/pull/4041)
 * tidy electron files, they weren't pwetty
   [\#3993](https://github.com/vector-im/riot-web/pull/3993)
 * Prevent Power Save when in call (Electron)
   [\#3992](https://github.com/vector-im/riot-web/pull/3992)
 * Translations!
   [\#4035](https://github.com/vector-im/riot-web/pull/4035)
 * Kieran gould/12hourtimestamp
   [\#3961](https://github.com/vector-im/riot-web/pull/3961)
 * Don't include src in the test resolve root
   [\#4033](https://github.com/vector-im/riot-web/pull/4033)
 * add moar context menus [Electron]
   [\#4021](https://github.com/vector-im/riot-web/pull/4021)
 * Add `Chat` to Linux app categories
   [\#4022](https://github.com/vector-im/riot-web/pull/4022)
 * add menu category for linux build of app
   [\#3975](https://github.com/vector-im/riot-web/pull/3975)
 * Electron Tray Improvements
   [\#3909](https://github.com/vector-im/riot-web/pull/3909)
 * More riot-web test deflakification
   [\#3966](https://github.com/vector-im/riot-web/pull/3966)
 * Script to fetch corresponding branches of dependent projects
   [\#3945](https://github.com/vector-im/riot-web/pull/3945)
 * Add type="text/css" to SVG logos
   [\#3964](https://github.com/vector-im/riot-web/pull/3964)
 * Fix some setState-after-unmount in roomdirectory
   [\#3958](https://github.com/vector-im/riot-web/pull/3958)
 * Attempt to deflakify joining test
   [\#3956](https://github.com/vector-im/riot-web/pull/3956)

Changes in [0.9.10](https://github.com/vector-im/riot-web/releases/tag/v0.9.10) (2017-05-22)
============================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.10-rc.1...v0.9.10)

 * No changes


Changes in [0.9.10-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.10-rc.1) (2017-05-19)
======================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.9...v0.9.10-rc.1)

 * CSS for left_aligned Dropdowns, and adjustments for Country dd in Login
   [\#3959](https://github.com/vector-im/riot-web/pull/3959)
 * Add square flag pngs /w genflags.sh script
   [\#3953](https://github.com/vector-im/riot-web/pull/3953)
 * Add config for riot-bot on desktop app build
   [\#3954](https://github.com/vector-im/riot-web/pull/3954)
 * Desktop: 'copy link address'
   [\#3952](https://github.com/vector-im/riot-web/pull/3952)
 * Reduce rageshake log size to 1MB
   [\#3943](https://github.com/vector-im/riot-web/pull/3943)
 * CSS for putting country dd on same line as phone input
   [\#3942](https://github.com/vector-im/riot-web/pull/3942)
 * fix #3894
   [\#3919](https://github.com/vector-im/riot-web/pull/3919)
 * change vector->riot on the surface
   [\#3894](https://github.com/vector-im/riot-web/pull/3894)
 * move manifest.json outward so it is scoped properly
   [\#3888](https://github.com/vector-im/riot-web/pull/3888)
 * add to manifest
   [\#3799](https://github.com/vector-im/riot-web/pull/3799)
 * Automatically update component-index
   [\#3886](https://github.com/vector-im/riot-web/pull/3886)
 * move electron -> electron_app because npm smart
   [\#3877](https://github.com/vector-im/riot-web/pull/3877)
 * Fix bug report endpoint in config.sample.json.
   [\#3863](https://github.com/vector-im/riot-web/pull/3863)
 * Update 2 missed icons to the new icon
   [\#3851](https://github.com/vector-im/riot-web/pull/3851)
 * Make left panel better for new users (mk II)
   [\#3804](https://github.com/vector-im/riot-web/pull/3804)
 * match primary package.json
   [\#3839](https://github.com/vector-im/riot-web/pull/3839)
 * Re-add productName
   [\#3829](https://github.com/vector-im/riot-web/pull/3829)
 * Remove leading v in /version file, for SemVer and to match Electron ver
   [\#3683](https://github.com/vector-im/riot-web/pull/3683)
 * Fix scope of callback
   [\#3790](https://github.com/vector-im/riot-web/pull/3790)
 * Remember and Recall window layout/position state
   [\#3622](https://github.com/vector-im/riot-web/pull/3622)
 * Remove babelcheck
   [\#3808](https://github.com/vector-im/riot-web/pull/3808)
 * Include MXID and device id in rageshakes
   [\#3809](https://github.com/vector-im/riot-web/pull/3809)
 * import Modal
   [\#3791](https://github.com/vector-im/riot-web/pull/3791)
 * Pin filesize ver to fix break upstream
   [\#3775](https://github.com/vector-im/riot-web/pull/3775)
 * Improve Room Directory Look & Feel
   [\#3751](https://github.com/vector-im/riot-web/pull/3751)
 * Fix emote RRs alignment
   [\#3742](https://github.com/vector-im/riot-web/pull/3742)
 * Remove unused `placeholder` prop on RoomDropTarget
   [\#3741](https://github.com/vector-im/riot-web/pull/3741)
 * Modify CSS for matrix-org/matrix-react-sdk#833
   [\#3732](https://github.com/vector-im/riot-web/pull/3732)
 * Warn when exiting due to single-instance
   [\#3727](https://github.com/vector-im/riot-web/pull/3727)
 * Electron forgets it was maximized when you click on a notification
   [\#3709](https://github.com/vector-im/riot-web/pull/3709)
 * CSS to make h1 and h2 the same size as h1.
   [\#3719](https://github.com/vector-im/riot-web/pull/3719)
 * Prevent long room names/topics from pushing UI of the screen
   [\#3721](https://github.com/vector-im/riot-web/pull/3721)
 * Disable dropdown highlight on focus
   [\#3717](https://github.com/vector-im/riot-web/pull/3717)
 * Escape HTML Tags from Linux Notifications (electron)
   [\#3564](https://github.com/vector-im/riot-web/pull/3564)
 * styling for spoilerized access token view in Settings
   [\#3651](https://github.com/vector-im/riot-web/pull/3651)
 * Fix Webpack conf
   [\#3690](https://github.com/vector-im/riot-web/pull/3690)
 * Add config.json to .gitignore
   [\#3599](https://github.com/vector-im/riot-web/pull/3599)
 * add command line arg (--hidden) for electron app
   [\#3641](https://github.com/vector-im/riot-web/pull/3641)
 * fix ImageView Download functionality
   [\#3640](https://github.com/vector-im/riot-web/pull/3640)
 * Add cross-env into the mix
   [\#3693](https://github.com/vector-im/riot-web/pull/3693)
 * Remember acceptance for unsupported browsers.
   [\#3694](https://github.com/vector-im/riot-web/pull/3694)
 * Cosmetics to go with matrix-org/matrix-react-sdk#811
   [\#3692](https://github.com/vector-im/riot-web/pull/3692)
 * Cancel quicksearch on ESC
   [\#3680](https://github.com/vector-im/riot-web/pull/3680)
 * Optimise RoomList and implement quick-search functionality on it.
   [\#3654](https://github.com/vector-im/riot-web/pull/3654)
 * Progress updates for rageshake uploads
   [\#3648](https://github.com/vector-im/riot-web/pull/3648)
 * Factor out rageshake upload to a separate file
   [\#3645](https://github.com/vector-im/riot-web/pull/3645)
 * rageshake: fix race when collecting logs
   [\#3644](https://github.com/vector-im/riot-web/pull/3644)
 * Fix a flaky test
   [\#3649](https://github.com/vector-im/riot-web/pull/3649)

Changes in [0.9.9](https://github.com/vector-im/riot-web/releases/tag/v0.9.9) (2017-04-25)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.9-rc.2...v0.9.9)

 * No changes


Changes in [0.9.9-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.9.9-rc.2) (2017-04-24)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.9-rc.1...v0.9.9-rc.2)

 * Fix bug where links to Riot would fail to open.


Changes in [0.9.9-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.9-rc.1) (2017-04-21)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.8...v0.9.9-rc.1)

 * Update js-sdk and matrix-react-sdk to fix registration without a captcha (https://github.com/vector-im/riot-web/issues/3621)


Changes in [0.9.8](https://github.com/vector-im/riot-web/releases/tag/v0.9.8) (2017-04-12)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.8-rc.3...v0.9.8)

 * No changes

Changes in [0.9.8-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.9.8-rc.3) (2017-04-11)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.8-rc.2...v0.9.8-rc.3)

 * Make the clear cache button work on desktop
   [\#3598](https://github.com/vector-im/riot-web/pull/3598)

Changes in [0.9.8-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.9.8-rc.2) (2017-04-10)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.8-rc.1...v0.9.8-rc.2)

 * Redacted events bg: black lozenge -> torn paper
   [\#3596](https://github.com/vector-im/riot-web/pull/3596)
 * Add 'app' parameter to rageshake report
   [\#3594](https://github.com/vector-im/riot-web/pull/3594)

Changes in [0.9.8-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.8-rc.1) (2017-04-07)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.7...v0.9.8-rc.1)

 * Add support for indexeddb sync in webworker
   [\#3578](https://github.com/vector-im/riot-web/pull/3578)
 * Add CSS to make Emote sender cursor : pointer
   [\#3574](https://github.com/vector-im/riot-web/pull/3574)
 * Remove rageshake server
   [\#3565](https://github.com/vector-im/riot-web/pull/3565)
 * Adjust CSS for matrix-org/matrix-react-sdk#789
   [\#3566](https://github.com/vector-im/riot-web/pull/3566)
 * Fix tests to reflect recent changes
   [\#3537](https://github.com/vector-im/riot-web/pull/3537)
 * Do not assume getTs will return comparable integer
   [\#3536](https://github.com/vector-im/riot-web/pull/3536)
 * Rename ReactPerf to Perf
   [\#3535](https://github.com/vector-im/riot-web/pull/3535)
 * Don't show phone number as target for email notifs
   [\#3530](https://github.com/vector-im/riot-web/pull/3530)
 * Fix people section again
   [\#3458](https://github.com/vector-im/riot-web/pull/3458)
 * dark theme invert inconsistent across browsers
   [\#3479](https://github.com/vector-im/riot-web/pull/3479)
 * CSS for adding phone number in UserSettings
   [\#3451](https://github.com/vector-im/riot-web/pull/3451)
 * Support for phone number registration/signin, mk2
   [\#3426](https://github.com/vector-im/riot-web/pull/3426)
 * Confirm redactions with a dialog
   [\#3470](https://github.com/vector-im/riot-web/pull/3470)
 * Better CSS for redactions
   [\#3453](https://github.com/vector-im/riot-web/pull/3453)
 * Fix the people section
   [\#3448](https://github.com/vector-im/riot-web/pull/3448)
 * Merge the two RoomTile context menus into one
   [\#3395](https://github.com/vector-im/riot-web/pull/3395)
 * Refactor screen set after login
   [\#3385](https://github.com/vector-im/riot-web/pull/3385)
 * CSS for redacted EventTiles
   [\#3379](https://github.com/vector-im/riot-web/pull/3379)
 * Height:100% for welcome pages on Safari
   [\#3340](https://github.com/vector-im/riot-web/pull/3340)
 * `view_room` dispatch from `onClick` RoomTile
   [\#3376](https://github.com/vector-im/riot-web/pull/3376)
 * Hide statusAreaBox_line entirely when inCall
   [\#3350](https://github.com/vector-im/riot-web/pull/3350)
 * Set padding-bottom: 0px for .mx_Dialog spinner
   [\#3351](https://github.com/vector-im/riot-web/pull/3351)
 * Support InteractiveAuth based registration
   [\#3333](https://github.com/vector-im/riot-web/pull/3333)
 * Expose notification option for username/MXID
   [\#3334](https://github.com/vector-im/riot-web/pull/3334)
 * Float the toggle in the top right of MELS
   [\#3190](https://github.com/vector-im/riot-web/pull/3190)
 * More aggressive rageshake log culling
   [\#3311](https://github.com/vector-im/riot-web/pull/3311)
 * Don't overflow directory network options
   [\#3282](https://github.com/vector-im/riot-web/pull/3282)
 * CSS for ban / kick reason prompt
   [\#3250](https://github.com/vector-im/riot-web/pull/3250)
 * Allow forgetting rooms you're banned from
   [\#3246](https://github.com/vector-im/riot-web/pull/3246)
 * Fix icon paths in manifest
   [\#3245](https://github.com/vector-im/riot-web/pull/3245)
 * Fix broken tests caused by adding IndexedDB support
   [\#3242](https://github.com/vector-im/riot-web/pull/3242)
 * CSS for un-ban button in RoomSettings
   [\#3227](https://github.com/vector-im/riot-web/pull/3227)
 * Remove z-index property on avatar initials
   [\#3239](https://github.com/vector-im/riot-web/pull/3239)
 * Reposition certain icons in the status bar
   [\#3233](https://github.com/vector-im/riot-web/pull/3233)
 * CSS for kick/ban confirmation dialog
   [\#3224](https://github.com/vector-im/riot-web/pull/3224)
 * Style for split-out interactive auth
   [\#3217](https://github.com/vector-im/riot-web/pull/3217)
 * Use the teamToken threaded through from react sdk
   [\#3196](https://github.com/vector-im/riot-web/pull/3196)
 * rageshake: Add file server with basic auth
   [\#3169](https://github.com/vector-im/riot-web/pull/3169)
 * Fix bug with home icon not appearing when logged in as team member
   [\#3162](https://github.com/vector-im/riot-web/pull/3162)
 * Add ISSUE_TEMPLATE
   [\#2836](https://github.com/vector-im/riot-web/pull/2836)
 * Store bug reports in separate directories
   [\#3150](https://github.com/vector-im/riot-web/pull/3150)
 * Quick and dirty support for custom welcome pages.
   [\#2575](https://github.com/vector-im/riot-web/pull/2575)
 * RTS Welcome Pages
   [\#3103](https://github.com/vector-im/riot-web/pull/3103)
 * rageshake: Abide by Go standards
   [\#3149](https://github.com/vector-im/riot-web/pull/3149)
 * Bug report server script
   [\#3072](https://github.com/vector-im/riot-web/pull/3072)
 * Bump olm version
   [\#3125](https://github.com/vector-im/riot-web/pull/3125)

Changes in [0.9.7](https://github.com/vector-im/riot-web/releases/tag/v0.9.7) (2017-02-04)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.7-rc.3...v0.9.7)

 * Update to matrix-js-sdk 0.7.5 (no changes from 0.7.5-rc.3)
 * Update to matrix-react-sdk 0.8.6 (no changes from 0.8.6-rc.3)

Changes in [0.9.7-rc.3](https://github.com/vector-im/riot-web/releases/tag/v0.9.7-rc.3) (2017-02-03)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.7-rc.2...v0.9.7-rc.3)
 * Update to latest Olm to fix key import/export and use of megolm sessions
   created on more recent versions
 * Update to latest matrix-react-sdk and matrix-js-sdk to fix e2e device
   handling

Changes in [0.9.7-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.9.7-rc.2) (2017-02-03)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.7-rc.1...v0.9.7-rc.2)

 * Update matrix-js-sdk to get new device change
   notifications interface for more reliable e2e crypto

Changes in [0.9.7-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.7-rc.1) (2017-02-03)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.6...v0.9.7-rc.1)

 * Better user interface for screen readers and keyboard navigation
   [\#2946](https://github.com/vector-im/riot-web/pull/2946)
 * Allow mxc: URLs for icons in the NetworkDropdown
   [\#3118](https://github.com/vector-im/riot-web/pull/3118)
 * make TopRightMenu more intuitive
   [\#3117](https://github.com/vector-im/riot-web/pull/3117)
 * Handle icons with width > height
   [\#3110](https://github.com/vector-im/riot-web/pull/3110)
 * Fix jenkins build
   [\#3105](https://github.com/vector-im/riot-web/pull/3105)
 * Add CSS for a support box in login
   [\#3081](https://github.com/vector-im/riot-web/pull/3081)
 * Allow a custom login logo to be displayed on login
   [\#3082](https://github.com/vector-im/riot-web/pull/3082)
 * Fix the width of input fields within login/reg box
   [\#3080](https://github.com/vector-im/riot-web/pull/3080)
 * Set BaseAvatar_image bg colour = #fff
   [\#3057](https://github.com/vector-im/riot-web/pull/3057)
 * only recalculate favicon if it changes
   [\#3067](https://github.com/vector-im/riot-web/pull/3067)
 * CSS tweak for email address lookup
   [\#3064](https://github.com/vector-im/riot-web/pull/3064)
 * Glue the dialog to rageshake: honour sendLogs flag.
   [\#3061](https://github.com/vector-im/riot-web/pull/3061)
 * Don't use hash-named directory for dev server
   [\#3049](https://github.com/vector-im/riot-web/pull/3049)
 * Implement bug reporting logic
   [\#3000](https://github.com/vector-im/riot-web/pull/3000)
 * Add css for bug report dialog
   [\#3045](https://github.com/vector-im/riot-web/pull/3045)
 * Increase the max-height of the expanded status bar
   [\#3043](https://github.com/vector-im/riot-web/pull/3043)
 * Hopefully, fix intermittent test failure
   [\#3040](https://github.com/vector-im/riot-web/pull/3040)
 * CSS for 'searching known users'
   [\#2971](https://github.com/vector-im/riot-web/pull/2971)
 * Animate status bar max-height and margin-top
   [\#2981](https://github.com/vector-im/riot-web/pull/2981)
 * Add eslint config
   [\#3032](https://github.com/vector-im/riot-web/pull/3032)
 * Re-position typing avatars relative to "is typing"
   [\#3030](https://github.com/vector-im/riot-web/pull/3030)
 * CSS for avatars that appear when users are typing
   [\#2998](https://github.com/vector-im/riot-web/pull/2998)
 * Add StartupWMClass
   [\#3001](https://github.com/vector-im/riot-web/pull/3001)
 * Fix link to image for event options menu
   [\#3002](https://github.com/vector-im/riot-web/pull/3002)
 * Make riot desktop single instance
   [\#2999](https://github.com/vector-im/riot-web/pull/2999)
 * Add electron tray icon
   [\#2997](https://github.com/vector-im/riot-web/pull/2997)
 * Fixes to electron desktop notifs
   [\#2994](https://github.com/vector-im/riot-web/pull/2994)
 * Auto-hide the electron menu bar
   [\#2975](https://github.com/vector-im/riot-web/pull/2975)
 * A couple of tweaks to the karma config
   [\#2987](https://github.com/vector-im/riot-web/pull/2987)
 * Deploy script
   [\#2974](https://github.com/vector-im/riot-web/pull/2974)
 * Use the postcss-webpack-loader
   [\#2990](https://github.com/vector-im/riot-web/pull/2990)
 * Switch CSS to using postcss, and implement a dark theme.
   [\#2973](https://github.com/vector-im/riot-web/pull/2973)
 * Update redeploy script to keep old bundles
   [\#2969](https://github.com/vector-im/riot-web/pull/2969)
 * Include current version in update check explicitly
   [\#2967](https://github.com/vector-im/riot-web/pull/2967)
 * Add another layer of directory to webpack chunks
   [\#2966](https://github.com/vector-im/riot-web/pull/2966)
 * Fix links to fonts and images from CSS
   [\#2965](https://github.com/vector-im/riot-web/pull/2965)
 * Put parent build hash in webpack output filenames
   [\#2961](https://github.com/vector-im/riot-web/pull/2961)
 * update README to point to new names/locations
   [\#2846](https://github.com/vector-im/riot-web/pull/2846)

Changes in [0.9.6](https://github.com/vector-im/riot-web/releases/tag/v0.9.6) (2017-01-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.6-rc.1...v0.9.6)

 * Update to matrix-js-sdk 0.9.6 for video calling fix

Changes in [0.9.6-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.6-rc.1) (2017-01-13)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.5...v0.9.6-rc.1)

 * Build the js-sdk in the CI script
   [\#2920](https://github.com/vector-im/riot-web/pull/2920)
 * Hopefully fix Windows shortcuts
   [\#2917](https://github.com/vector-im/riot-web/pull/2917)
 * Update README now the js-sdk has a transpile step
   [\#2921](https://github.com/vector-im/riot-web/pull/2921)
 * Use the role for 'toggle dev tools'
   [\#2915](https://github.com/vector-im/riot-web/pull/2915)
 * Enable screen sharing easter-egg in desktop app
   [\#2909](https://github.com/vector-im/riot-web/pull/2909)
 * make electron send email validation URLs with a nextlink of riot.im
   [\#2808](https://github.com/vector-im/riot-web/pull/2808)
 * add Debian Stretch install steps to readme
   [\#2809](https://github.com/vector-im/riot-web/pull/2809)
 * Update desktop build instructions fixes #2792
   [\#2793](https://github.com/vector-im/riot-web/pull/2793)
 * CSS for the delete threepid button
   [\#2784](https://github.com/vector-im/riot-web/pull/2784)

Changes in [0.9.5](https://github.com/vector-im/riot-web/releases/tag/v0.9.5) (2016-12-24)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.4...v0.9.5)

 * make electron send email validation URLs with a nextlink of riot.im rather than file:///
 * add gnu-tar to debian electron build deps
 * fix win32 shortcut in start menu

Changes in [0.9.4](https://github.com/vector-im/riot-web/releases/tag/v0.9.4) (2016-12-22)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.3...v0.9.4)

 * Update to libolm 2.1.0. This should help resolve a problem with browser
   sessions being logged out ([\#2726](https://github.com/vector-im/riot-web/issues/2726)).

Changes in [0.9.3](https://github.com/vector-im/riot-web/releases/tag/v0.9.3) (2016-12-22)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.2...v0.9.3)

 * (from matrix-react-sdk) Fix regression where the date separator would be displayed
   at the wrong time of day.
 * README.md: fix GFMD for nativefier
   [\#2755](https://github.com/vector-im/riot-web/pull/2755)

Changes in [0.9.2](https://github.com/vector-im/riot-web/releases/tag/v0.9.2) (2016-12-16)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.1...v0.9.2)

 * Remove the client side filtering from the room dir
   [\#2750](https://github.com/vector-im/riot-web/pull/2750)
 * Configure olm memory size
   [\#2745](https://github.com/vector-im/riot-web/pull/2745)
 * Support room dir 3rd party network filtering
   [\#2747](https://github.com/vector-im/riot-web/pull/2747)

Changes in [0.9.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.1) (2016-12-09)
==========================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.1-rc.2...v0.9.1)

 * Update README to say how to build the desktop app
   [\#2732](https://github.com/vector-im/riot-web/pull/2732)
 * Add signing ID in release_config.yaml
   [\#2731](https://github.com/vector-im/riot-web/pull/2731)
 * Makeover!
   [\#2722](https://github.com/vector-im/riot-web/pull/2722)
 * Fix broken tests
   [\#2730](https://github.com/vector-im/riot-web/pull/2730)
 * Make the 'loading' tests work in isolation
   [\#2727](https://github.com/vector-im/riot-web/pull/2727)
 * Use a PNG for the icon on non-Windows
   [\#2708](https://github.com/vector-im/riot-web/pull/2708)
 * Add missing brackets to call to toUpperCase
   [\#2703](https://github.com/vector-im/riot-web/pull/2703)

Changes in [0.9.1-rc.2](https://github.com/vector-im/riot-web/releases/tag/v0.9.1-rc.2) (2016-12-06)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.1-rc.1...v0.9.1-rc.2)

 * Fix clicking on notifications
   [\#2700](https://github.com/vector-im/riot-web/pull/2700)
 * Desktop app: Only show window when ready
   [\#2697](https://github.com/vector-im/riot-web/pull/2697)

Changes in [0.9.1-rc.1](https://github.com/vector-im/riot-web/releases/tag/v0.9.1-rc.1) (2016-12-05)
====================================================================================================
[Full Changelog](https://github.com/vector-im/riot-web/compare/v0.9.0...v0.9.1-rc.1)

 * Final bits to prepare electron distribtion:
   [\#2653](https://github.com/vector-im/riot-web/pull/2653)
 * Update name & repo to reflect renamed repository
   [\#2692](https://github.com/vector-im/riot-web/pull/2692)
 * Document cross_origin_renderer_url
   [\#2680](https://github.com/vector-im/riot-web/pull/2680)
 * Add css for the iframes for e2e attachments
   [\#2659](https://github.com/vector-im/riot-web/pull/2659)
 * Fix config location in some more places
   [\#2670](https://github.com/vector-im/riot-web/pull/2670)
 * CSS updates for s/block/blacklist for e2e
   [\#2662](https://github.com/vector-im/riot-web/pull/2662)
 * Update to electron 1.4.8
   [\#2660](https://github.com/vector-im/riot-web/pull/2660)
 * Add electron config
   [\#2644](https://github.com/vector-im/riot-web/pull/2644)
 * Move getDefaultDeviceName into the Platforms
   [\#2643](https://github.com/vector-im/riot-web/pull/2643)
 * Add Freenode & Mozilla domains
   [\#2641](https://github.com/vector-im/riot-web/pull/2641)
 * Include config.sample.json in dist tarball
   [\#2614](https://github.com/vector-im/riot-web/pull/2614)

Changes in [0.9.0](https://github.com/vector-im/vector-web/releases/tag/v0.9.0) (2016-11-19)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.4...v0.9.0)

 * Add a cachebuster to /version
   [\#2596](https://github.com/vector-im/vector-web/pull/2596)
 * Add a 'View decrypted source' button
   [\#2587](https://github.com/vector-im/vector-web/pull/2587)
 * Fix changelog dialog to  read new version format
   [\#2577](https://github.com/vector-im/vector-web/pull/2577)
 * Build all of the vector dir in the build process
   [\#2558](https://github.com/vector-im/vector-web/pull/2558)
 * Support for get_app_version
   [\#2553](https://github.com/vector-im/vector-web/pull/2553)
 * Add CSS for mlist truncation
   [\#2565](https://github.com/vector-im/vector-web/pull/2565)
 * Add menu option for `external_url` if present
   [\#2560](https://github.com/vector-im/vector-web/pull/2560)
 * Make auto-update configureable
   [\#2555](https://github.com/vector-im/vector-web/pull/2555)
 * Missed files electron windows fixes
   [\#2556](https://github.com/vector-im/vector-web/pull/2556)
 * Add some CSS for  scalar error popup
   [\#2554](https://github.com/vector-im/vector-web/pull/2554)
 * Catch unhandled errors in the electron process
   [\#2552](https://github.com/vector-im/vector-web/pull/2552)
 * Slight grab-bag of fixes for electron on Windows
   [\#2551](https://github.com/vector-im/vector-web/pull/2551)
 * Electron app (take 3)
   [\#2535](https://github.com/vector-im/vector-web/pull/2535)
 * Use webpack-dev-server instead of http-server
   [\#2542](https://github.com/vector-im/vector-web/pull/2542)
 * Better support no-config when loading from file
   [\#2541](https://github.com/vector-im/vector-web/pull/2541)
 * Fix loading with no config from HTTP
   [\#2540](https://github.com/vector-im/vector-web/pull/2540)
 * Move 'new version' support into Platform
   [\#2532](https://github.com/vector-im/vector-web/pull/2532)
 * Add Notification support to the Web Platform
   [\#2533](https://github.com/vector-im/vector-web/pull/2533)
 * Use the defaults if given a blank config file
   [\#2534](https://github.com/vector-im/vector-web/pull/2534)
 * Implement Platforms
   [\#2531](https://github.com/vector-im/vector-web/pull/2531)

Changes in [0.8.4](https://github.com/vector-im/vector-web/releases/tag/v0.8.4) (2016-11-04)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.4-rc.2...v0.8.4)

 * No changes

Changes in [0.8.4-rc.2](https://github.com/vector-im/vector-web/releases/tag/v0.8.4-rc.2) (2016-11-02)
======================================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.4-rc.1...v0.8.4-rc.2)

 * Fix the version in the generated distribution package

Changes in [0.8.4-rc.1](https://github.com/vector-im/vector-web/releases/tag/v0.8.4-rc.1) (2016-11-02)
======================================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.3...v0.8.4-rc.1)

Breaking Changes
----------------
 * End-to-end encryption now requires one-time keys to be
   signed, so end-to-end encryption will not interoperate
   with previous releases of vector-web. End-to-end encryption
   remains in beta.

Other Changes
-------------
 * Rename the package script/output dir to 'dist'
   [\#2528](https://github.com/vector-im/vector-web/pull/2528)
 * Avoid errors if olm is missing
   [\#2518](https://github.com/vector-im/vector-web/pull/2518)
 * Put a cachebuster in the names of CSS and JS files
   [\#2515](https://github.com/vector-im/vector-web/pull/2515)
 * Bump to olm 2.0.0
   [\#2517](https://github.com/vector-im/vector-web/pull/2517)
 * Don't include the world in the published packages
   [\#2516](https://github.com/vector-im/vector-web/pull/2516)
 * Use webpack to copy olm.js
   [\#2514](https://github.com/vector-im/vector-web/pull/2514)
 * Don't include two copies of the CSS in the tarball
   [\#2513](https://github.com/vector-im/vector-web/pull/2513)
 * Correct text alignment on room directory search
   [\#2512](https://github.com/vector-im/vector-web/pull/2512)
 * Correct spelling of 'rel'
   [\#2510](https://github.com/vector-im/vector-web/pull/2510)
 * readme tweaks
   [\#2507](https://github.com/vector-im/vector-web/pull/2507)
 * s/vector/riot/ in the readme
   [\#2491](https://github.com/vector-im/vector-web/pull/2491)
 * Switch to babel 6, again
   [\#2480](https://github.com/vector-im/vector-web/pull/2480)
 * Revert "Switch to babel 6"
   [\#2472](https://github.com/vector-im/vector-web/pull/2472)
 * Switch to babel 6
   [\#2461](https://github.com/vector-im/vector-web/pull/2461)

Changes in [0.8.3](https://github.com/vector-im/vector-web/releases/tag/v0.8.3) (2016-10-12)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.2...v0.8.3)

 * Centre images in dialog buttons
   [\#2453](https://github.com/vector-im/vector-web/pull/2453)
 * Only show quote option if RTE is enabled
   [\#2448](https://github.com/vector-im/vector-web/pull/2448)
 * Fix join button for 'matrix' networks
   [\#2443](https://github.com/vector-im/vector-web/pull/2443)
 * Don't stop paginating if no rooms match
   [\#2422](https://github.com/vector-im/vector-web/pull/2422)

Changes in [0.8.2](https://github.com/vector-im/vector-web/releases/tag/v0.8.2) (2016-10-05)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.1...v0.8.2)

 * Add native joining of 3p networks to room dir
   [\#2379](https://github.com/vector-im/vector-web/pull/2379)
 * Update to linkify 2.1.3
   [\#2406](https://github.com/vector-im/vector-web/pull/2406)
 * Use 'Sign In' / 'Sign Out' universally
   [\#2383](https://github.com/vector-im/vector-web/pull/2383)
 * Prevent network dropdown resizing slightly
   [\#2382](https://github.com/vector-im/vector-web/pull/2382)
 * Room directory: indicate when there are no results
   [\#2380](https://github.com/vector-im/vector-web/pull/2380)
 * Room dir: New filtering & 3rd party networks
   [\#2362](https://github.com/vector-im/vector-web/pull/2362)
 * Update linkify version
   [\#2359](https://github.com/vector-im/vector-web/pull/2359)
 * Directory search join button
   [\#2339](https://github.com/vector-im/vector-web/pull/2339)

Changes in [0.8.1](https://github.com/vector-im/vector-web/releases/tag/v0.8.1) (2016-09-21)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.8.0...v0.8.1)


Changes in [0.8.0](https://github.com/vector-im/vector-web/releases/tag/v0.8.0) (2016-09-21)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.5-r3...v0.8.0)

 * Dbkr/rebrand
   [\#2285](https://github.com/vector-im/vector-web/pull/2285)
 * Listen for close_scalar and close the dialog box when received
   [\#2282](https://github.com/vector-im/vector-web/pull/2282)
 * Revert "improve lipstick and support scalar logout"
   [\#2281](https://github.com/vector-im/vector-web/pull/2281)
 * improve lipstick and support scalar logout
   [\#2280](https://github.com/vector-im/vector-web/pull/2280)
 * Fix changelog links
   [\#2071](https://github.com/vector-im/vector-web/pull/2071)
 * Paginate Room Directory
   [\#2241](https://github.com/vector-im/vector-web/pull/2241)
 * Make redeploy script symlink config
   [\#2240](https://github.com/vector-im/vector-web/pull/2240)
 * Update the version of olm to 1.3.0
   [\#2210](https://github.com/vector-im/vector-web/pull/2210)
 * Directory network selector
   [\#2219](https://github.com/vector-im/vector-web/pull/2219)
 * Wmwragg/two state sublist headers
   [\#2235](https://github.com/vector-im/vector-web/pull/2235)
 * Wmwragg/correct incoming call positioning
   [\#2222](https://github.com/vector-im/vector-web/pull/2222)
 * Wmwragg/remove old filter
   [\#2211](https://github.com/vector-im/vector-web/pull/2211)
 * Wmwragg/multi invite bugfix
   [\#2198](https://github.com/vector-im/vector-web/pull/2198)
 * Wmwragg/chat multi invite
   [\#2181](https://github.com/vector-im/vector-web/pull/2181)
 * shuffle bottomleftmenu around a bit
   [\#2182](https://github.com/vector-im/vector-web/pull/2182)
 * Improve autocomplete behaviour (styling)
   [\#2175](https://github.com/vector-im/vector-web/pull/2175)
 * First wave of E2E visuals
   [\#2163](https://github.com/vector-im/vector-web/pull/2163)
 * FilePanel and NotificationPanel support
   [\#2113](https://github.com/vector-im/vector-web/pull/2113)
 * Cursor: pointer on member info create room button
   [\#2151](https://github.com/vector-im/vector-web/pull/2151)
 * Support for adding DM rooms to the MemberInfo Panel
   [\#2147](https://github.com/vector-im/vector-web/pull/2147)
 * Wmwragg/one to one indicators
   [\#2139](https://github.com/vector-im/vector-web/pull/2139)
 * Added back the Directory listing button, with new tootlip
   [\#2136](https://github.com/vector-im/vector-web/pull/2136)
 * wmwragg/chat invite dialog fix
   [\#2134](https://github.com/vector-im/vector-web/pull/2134)
 * Wmwragg/one to one chat
   [\#2110](https://github.com/vector-im/vector-web/pull/2110)
 * Support toggling DM status of rooms
   [\#2111](https://github.com/vector-im/vector-web/pull/2111)
 * Formatting toolbar for RTE message composer.
   [\#2082](https://github.com/vector-im/vector-web/pull/2082)
 * jenkins.sh: install olm from jenkins artifacts
   [\#2092](https://github.com/vector-im/vector-web/pull/2092)
 * e2e device CSS
   [\#2085](https://github.com/vector-im/vector-web/pull/2085)
 * Bump to olm 1.1.0
   [\#2069](https://github.com/vector-im/vector-web/pull/2069)
 * Improve readability of the changelog dialog
   [\#2056](https://github.com/vector-im/vector-web/pull/2056)
 * Turn react consistency checks back on in develop builds
   [\#2009](https://github.com/vector-im/vector-web/pull/2009)
 * Wmwragg/direct chat sublist
   [\#2028](https://github.com/vector-im/vector-web/pull/2028)

Changes in [0.7.5-r3](https://github.com/vector-im/vector-web/releases/tag/v0.7.5-r3) (2016-09-02)
==================================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.5-r2...v0.7.5-r3)

 * Bump to matrix-react-sdk 0.6.5-r3 in order to fix bug #2020 (tightloop when flooded with join events)


Changes in [0.7.5-r2](https://github.com/vector-im/vector-web/releases/tag/v0.7.5-r2) (2016-09-01)
==================================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.5-r1...v0.7.5-r2)

 * Bump to matrix-react-sdk 0.6.5-r1 in order to fix guest access

Changes in [0.7.5-r1](https://github.com/vector-im/vector-web/releases/tag/v0.7.5-r1) (2016-08-28)
==================================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.5...v0.7.5-r1)

 * Correctly pin deps :(

Changes in [0.7.5](https://github.com/vector-im/vector-web/releases/tag/v0.7.5) (2016-08-28)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.4-r1...v0.7.5)

 * re-add leave button in RoomSettings
 * add /user URLs
 * recognise matrix.to links and other vector links
 * fix linkify dependency
 * fix avatar clicking in MemberInfo
 * fix RoomTagContextMenu so it works on historical rooms
 * warn people to put their Matrix HS on a separate domain to Vector
 * fix zalgos again
 * Add .travis.yml
   [\#2007](https://github.com/vector-im/vector-web/pull/2007)
 * add fancy changelog dialog
   [\#1972](https://github.com/vector-im/vector-web/pull/1972)
 * Update autocomplete design
   [\#1978](https://github.com/vector-im/vector-web/pull/1978)
 * Update encryption info in README
   [\#2001](https://github.com/vector-im/vector-web/pull/2001)
 * Added event/info message avatars back in
   [\#2000](https://github.com/vector-im/vector-web/pull/2000)
 * Wmwragg/chat message presentation
   [\#1987](https://github.com/vector-im/vector-web/pull/1987)
 * Make the notification slider work
   [\#1982](https://github.com/vector-im/vector-web/pull/1982)
 * Use cpx to copy olm.js, and add watcher
   [\#1966](https://github.com/vector-im/vector-web/pull/1966)
 * Make up a device display name
   [\#1959](https://github.com/vector-im/vector-web/pull/1959)

Changes in [0.7.4-r1](https://github.com/vector-im/vector-web/releases/tag/v0.7.4-r1) (2016-08-12)
==================================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.4...v0.7.4-r1)
 * Update to matrix-react-sdk 0.6.4-r1 to fix inviting multiple people


Changes in [0.7.4](https://github.com/vector-im/vector-web/releases/tag/v0.7.4) (2016-08-11)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.3...v0.7.4)

 * Don't show border on composer when not in RTE mode
   [\#1954](https://github.com/vector-im/vector-web/pull/1954)
 * Wmwragg/room tag menu
   [\#1941](https://github.com/vector-im/vector-web/pull/1941)
 * Don't redirect to mobile app if verifying 3pid
   [\#1951](https://github.com/vector-im/vector-web/pull/1951)
 * Make sure that we clear localstorage before *all* tests
   [\#1950](https://github.com/vector-im/vector-web/pull/1950)
 * Basic CSS for multi-invite dialog
   [\#1942](https://github.com/vector-im/vector-web/pull/1942)
 * More tests for the loading process:
   [\#1947](https://github.com/vector-im/vector-web/pull/1947)
 * Support for refactored login token handling
   [\#1946](https://github.com/vector-im/vector-web/pull/1946)
 * Various fixes and improvements to emojification.
   [\#1935](https://github.com/vector-im/vector-web/pull/1935)
 * More app-loading tests
   [\#1938](https://github.com/vector-im/vector-web/pull/1938)
 * Some tests of the application load process
   [\#1936](https://github.com/vector-im/vector-web/pull/1936)
 * Add 'enable labs' setting to sample config
   [\#1930](https://github.com/vector-im/vector-web/pull/1930)
 * Matthew/scalar
   [\#1928](https://github.com/vector-im/vector-web/pull/1928)
 * Fix unit tests
   [\#1929](https://github.com/vector-im/vector-web/pull/1929)
 * Wmwragg/mute mention state fix
   [\#1926](https://github.com/vector-im/vector-web/pull/1926)
 * CSS for deactivate account dialog
   [\#1919](https://github.com/vector-im/vector-web/pull/1919)
 * Wmwragg/mention state menu
   [\#1900](https://github.com/vector-im/vector-web/pull/1900)
 * Fix UnknownBody styling for #1901
   [\#1913](https://github.com/vector-im/vector-web/pull/1913)
 * Exclude olm from the webpack
   [\#1914](https://github.com/vector-im/vector-web/pull/1914)
 * Wmwragg/button updates
   [\#1912](https://github.com/vector-im/vector-web/pull/1912)
 * Wmwragg/button updates
   [\#1828](https://github.com/vector-im/vector-web/pull/1828)
 * CSS for device management UI
   [\#1909](https://github.com/vector-im/vector-web/pull/1909)
 * Fix a warning from RoomSubList
   [\#1908](https://github.com/vector-im/vector-web/pull/1908)
 * Fix notifications warning layout
   [\#1907](https://github.com/vector-im/vector-web/pull/1907)
 * Remove relayoutOnUpdate prop on gemini-scrollbar
   [\#1883](https://github.com/vector-im/vector-web/pull/1883)
 * Bump dependency versions
   [\#1842](https://github.com/vector-im/vector-web/pull/1842)
 * Wmwragg/mention state indicator round 2
   [\#1835](https://github.com/vector-im/vector-web/pull/1835)
 * Wmwragg/spinner fix
   [\#1822](https://github.com/vector-im/vector-web/pull/1822)
 * Wmwragg/mention state indicator
   [\#1823](https://github.com/vector-im/vector-web/pull/1823)
 * Revert "Presentation for inline link"
   [\#1809](https://github.com/vector-im/vector-web/pull/1809)
 * Wmwragg/modal restyle
   [\#1806](https://github.com/vector-im/vector-web/pull/1806)
 * Presentation for inline link
   [\#1799](https://github.com/vector-im/vector-web/pull/1799)
 * CSS for offline user colours
   [\#1798](https://github.com/vector-im/vector-web/pull/1798)
 * Wmwragg/typography updates
   [\#1776](https://github.com/vector-im/vector-web/pull/1776)
 * webpack: always use the olm from vector-web
   [\#1766](https://github.com/vector-im/vector-web/pull/1766)
 * feat: large emoji support
   [\#1718](https://github.com/vector-im/vector-web/pull/1718)
 * Autocomplete
   [\#1717](https://github.com/vector-im/vector-web/pull/1717)
 * #1664 Set a maximum height for codeblocks
   [\#1670](https://github.com/vector-im/vector-web/pull/1670)
 * CSS for device blocking
   [\#1688](https://github.com/vector-im/vector-web/pull/1688)
 * Fix joining rooms by typing the alias
   [\#1685](https://github.com/vector-im/vector-web/pull/1685)
 * Add ability to delete an alias from room directory
   [\#1680](https://github.com/vector-im/vector-web/pull/1680)
 * package.json: add olm as optionalDependency
   [\#1678](https://github.com/vector-im/vector-web/pull/1678)
 * Another go at enabling olm on vector.im/develop
   [\#1675](https://github.com/vector-im/vector-web/pull/1675)
 * CSS for unverify button
   [\#1661](https://github.com/vector-im/vector-web/pull/1661)
 * CSS fix for rooms with crypto enabled
   [\#1660](https://github.com/vector-im/vector-web/pull/1660)
 * Karma: fix warning by ignoring olm
   [\#1652](https://github.com/vector-im/vector-web/pull/1652)
 * Update for react-sdk dbkr/fix_peeking branch
   [\#1639](https://github.com/vector-im/vector-web/pull/1639)
 * Update README.md
   [\#1641](https://github.com/vector-im/vector-web/pull/1641)
 * Fix karma tests
   [\#1643](https://github.com/vector-im/vector-web/pull/1643)
 * Rich Text Editor
   [\#1553](https://github.com/vector-im/vector-web/pull/1553)
 * Fix RoomDirectory to join by alias whenever possible.
   [\#1615](https://github.com/vector-im/vector-web/pull/1615)
 * Make the config optional
   [\#1612](https://github.com/vector-im/vector-web/pull/1612)
 * CSS support for device verification
   [\#1610](https://github.com/vector-im/vector-web/pull/1610)
 * Don't use SdkConfig
   [\#1609](https://github.com/vector-im/vector-web/pull/1609)
 * serve config.json statically instead of bundling it
   [\#1516](https://github.com/vector-im/vector-web/pull/1516)

Changes in [0.7.3](https://github.com/vector-im/vector-web/releases/tag/v0.7.3) (2016-06-03)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.2...v0.7.3)

* Update to react-sdk 0.6.3

Changes in [0.7.2](https://github.com/vector-im/vector-web/releases/tag/v0.7.2) (2016-06-02)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.1...v0.7.2)

 * Correctly bump the dep on new matrix-js-sdk and matrix-react-sdk

Changes in [0.7.1](https://github.com/vector-im/vector-web/releases/tag/v0.7.1) (2016-06-02)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.7.0...v0.7.1)

 * Fix accidentally committed local changes to the default config.json (doh!)

Changes in [0.7.0](https://github.com/vector-im/vector-web/releases/tag/v0.7.0) (2016-06-02)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.6.1...v0.7.0)

 * Update to matrix-react-sdk 0.6.0 - see
   [changelog](https://github.com/matrix-org/matrix-react-sdk/blob/v0.6.0/CHANGELOG.md)
 * Style selection color.
   [\#1557](https://github.com/vector-im/vector-web/pull/1557)
 * Fix NPE when loading the Settings page which infini-spinnered
   [\#1518](https://github.com/vector-im/vector-web/pull/1518)
 * Add option to enable email notifications
   [\#1469](https://github.com/vector-im/vector-web/pull/1469)

Changes in [0.6.1](https://github.com/vector-im/vector-web/releases/tag/v0.6.1) (2016-04-22)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.6.0...v0.6.1)

 * Update to matrix-react-sdk 0.5.2 - see
   [changelog](https://github.com/matrix-org/matrix-react-sdk/blob/v0.5.2/CHANGELOG.md)
 * Don't relayout scrollpanels every time something changes
   [\#1438](https://github.com/vector-im/vector-web/pull/1438)
 * Include react-addons-perf for non-production builds
   [\#1431](https://github.com/vector-im/vector-web/pull/1431)

Changes in [0.6.0](https://github.com/vector-im/vector-web/releases/tag/v0.6.0) (2016-04-19)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.5.0...v0.6.0)

 * Matthew/design tweaks
   [\#1402](https://github.com/vector-im/vector-web/pull/1402)
 * Improve handling of notification rules we can't parse
   [\#1399](https://github.com/vector-im/vector-web/pull/1399)
 * Do less mangling of jenkins builds
   [\#1391](https://github.com/vector-im/vector-web/pull/1391)
 * Start Notifications component refactor
   [\#1386](https://github.com/vector-im/vector-web/pull/1386)
 * make the UI fadable to help with decluttering
   [\#1376](https://github.com/vector-im/vector-web/pull/1376)
 * Get and display a user's pushers in settings
   [\#1374](https://github.com/vector-im/vector-web/pull/1374)
 * URL previewing support
   [\#1343](https://github.com/vector-im/vector-web/pull/1343)
 * 😄 Emoji autocomplete and unicode emoji to image conversion using emojione.
   [\#1332](https://github.com/vector-im/vector-web/pull/1332)
 * Show full-size avatar on MemberInfo avatar click
   [\#1340](https://github.com/vector-im/vector-web/pull/1340)
 * Numerous other changes via [matrix-react-sdk 0.5.1](https://github.com/matrix-org/matrix-react-sdk/blob/v0.5.1/CHANGELOG.md)

Changes in [0.5.0](https://github.com/vector-im/vector-web/releases/tag/v0.5.0) (2016-03-30)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.4.1...v0.5.0)

 * Prettier, animated placeholder :D
   [\#1292](https://github.com/vector-im/vector-web/pull/1292)
   (Disabled for now due to high CPU usage)
 * RoomDirectory: use SimpleRoomHeader instead of RoomHeader
   [\#1307](https://github.com/vector-im/vector-web/pull/1307)
 * Tell webpack not to parse the highlight.js languages
   [\#1277](https://github.com/vector-im/vector-web/pull/1277)
 * CSS for https://github.com/matrix-org/matrix-react-sdk/pull/247
   [\#1249](https://github.com/vector-im/vector-web/pull/1249)
 * URI-decode the hash-fragment
   [\#1254](https://github.com/vector-im/vector-web/pull/1254)

Changes in [0.4.1](https://github.com/vector-im/vector-web/releases/tag/v0.4.1) (2016-03-23)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.4.0...v0.4.1)
 * Update to matrix-react-sdk 0.3.1; see
   https://github.com/matrix-org/matrix-react-sdk/blob/v0.3.1/CHANGELOG.md
   (Disables debug logging)

Changes in [0.4.0](https://github.com/vector-im/vector-web/releases/tag/v0.4.0) (2016-03-23)
============================================================================================
[Full Changelog](https://github.com/vector-im/vector-web/compare/v0.3.0...v0.4.0)

 * Update to matrix-react-sdk 0.3.0; see
   https://github.com/matrix-org/matrix-react-sdk/blob/master/CHANGELOG.md

Other changes
 * permalink button
   [\#1232](https://github.com/vector-im/vector-web/pull/1232)
 * make senderprofiles clickable
   [\#1191](https://github.com/vector-im/vector-web/pull/1191)
 * fix notif spam when logging in from a guest session by correctly logging out
   first.
   [\#1180](https://github.com/vector-im/vector-web/pull/1180)
 * use new start_login_from_guest dispatch for cancellable logins from guest
   accounts
   [\#1165](https://github.com/vector-im/vector-web/pull/1165)
 * Use then() chaining rather than manual callbacks
   [\#1171](https://github.com/vector-im/vector-web/pull/1171)
 * Remove trailing whitespace
   [\#1163](https://github.com/vector-im/vector-web/pull/1163)
 * Update the actions of default rules instead of overriding.
   [\#1037](https://github.com/vector-im/vector-web/pull/1037)
 * Update README to include `npm install` in react-sdk
   [\#1137](https://github.com/vector-im/vector-web/pull/1137)

Changes in vector v0.3.0 (2016-03-11)
======================================
 * Lots of new bug fixes and updates

Changes in vector v0.2.0 (2016-02-24)
======================================
 * Refactor of matrix-react-sdk and vector to remove separation between views and
   controllers
 * Temporarily break the layering abstraction between vector and matrix-react-sdk
   for expedience in developing vector.
 * Vast numbers of new features, including read receipts, read-up-to markers,
   updated look and feel, search, new room and user settings, and email invites.

Changes in vector v0.1.2 (2015-10-28)
======================================
 * Support Room Avatars
 * Fullscreen video calls
 * Mute mic in VoIP calls
 * Fix bug with multiple desktop notifications
 * Context menu on messages
 * Better hover-over on member list
 * Support CAS auth
 * Many other bug fixes

Changes in vector v0.1.1 (2015-08-10)
======================================

 * Support logging in with an email address
 * Use the Vector identity server
 * Fix a bug where the client was not stopped properly on logout
 * Fix bugs where field values would be forgotten if login or registration failed
 * Improve URL bar navigation
 * Add explanatory help text on advanced server options
 * Fix a bug which caused execptions on malformed VoIP invitations
 * Remove superfluous scrollbars on Firefox
 * Numerous CSS fixes
 * Improved accessibility
 * Support command-click / middle click to open image in a new tab
 * Improved room directory
 * Fix display of text with many combining unicode points

Changes in vector v0.1.0 (2015-08-10)
======================================
Initial release
