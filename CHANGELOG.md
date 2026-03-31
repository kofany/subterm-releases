# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v0.2.23] - 2026-03-31


### :bug: Bug Fixes
- Ssh freeze with russh 0.56 + update all dependencies
- Complete i18n for help panel and error messages
- Use rsa-sha2-256/512 instead of deprecated ssh-rsa
- Terminal scrollback history not rendering when scrolled
- Add ssh keepalive to prevent connection timeouts
- Restore corrupted patch file + cleanup
- Selection behavior in apps with mouse tracking (irssi, vim, mc)
- Fix tmux dcs passthrough unwrap causing base64 leakage
- Enable commitmode for changelog builder action
- Restore pagelist.zig memory zeroing for wasm + bump to v0.2.4
- File manager tab shows host name in transfer-only mode
- Remove f5 shortcut for file manager (conflicts with mc, vim)
- Verify and correct keyboard shortcuts in help panel
- Escape key no longer closes dialogs when typing in text input
- Add missing .msi/.rpm to release + fix changelog generation
- Correct sgr mouse motion encoding for no-button events
- Remove f3/alt+d shortcut for debug window (conflicts with mc)
- Password dialog loses focus to terminal
- Aur uses native .pkg.tar.zst instead of .deb
- Add unzip for bun install on arch
- Use npm instead of bun for arch build
- Install bun with symlink for arch build
- Simplify arch package creation from ubuntu .deb
- Native arch linux build with direct bun binary download
- Add nodejs for bun to delegate vite execution
- Add xdg-utils for appimage bundling
- Build only binary on arch, skip bundlers
- Password dialog focus escape and openwrt shell prompt
- Prevent shell injection in changelog workflow
- Help panel fixed size and improved styling
- Correct dpr handling for stock beamterm renderer
- Correct dpr handling with beamterm-terx 0.13.0
- Fix select elements using wrong classes
- Prevent custom select/input styles from overriding daisyui
- Remove legacy css that overrides daisyui component styles
- Properly configure daisyui 5 theme for component styling
- Remove -bordered classes removed in daisyui 5
- Update bun.lock with daisyui dependency
- Biometric unlock not working on windows
- Auth dialog styling and broken update mechanism
- Settings account tab for all storage modes and config_save crash
- Storage convex mock + vitest for convex tests
- Isolate mock.module conflicts between test files
- Wait for exitstatus after eof before breaking loop
- Sidebar host status, startup flash, reconnect ui bugs + recipe improvements
- Fix drag-and-drop - tabs were returning to original position
- Replace html5 drag api with mouse events for reliable drag-and-drop
- Disable dragdropenabled to prevent tauri intercepting dom mouse events
- Enable drag-and-drop for file manager tabs
- Fix file manager + terminal tab integration bugs
- Intercept ctrl+tab in capture phase before terminal input handler
- Change strict pixel validation from throw to warn+render
- Kitty graphics apc_start marker split across ssh reads
- Point update checker to subterm-releases repo



### :construction_worker: CI/CD
- Cross-repo release workflow to publish on outragelabs/terx
- Add aur package auto-publishing
- Add native arch linux build
- Add macos intel build to release workflow
- Move workflows to public repo



### :lock: Security
- Remove legacy credentials.rs with insecure key derivation
- Remove .credentials_backup from git tracking



### :memo: Documentation
- Update changelog.md for v0.1.3
- Update changelog.md for v0.1.4
- Update changelog.md for v0.1.5
- Update changelog.md for v0.1.6
- Update changelog.md for v0.1.7
- Update changelog.md for v0.2.3
- Update changelog.md for v0.2.3
- Fix changelog.md for v0.2.3 (manual correction)
- Expand changelog.md for v0.2.3 with full details
- Update changelog.md for v0.2.4
- Add releases.md and update claude.md with dual-repo info
- Update changelog.md for v0.2.6
- Update changelog.md for v0.2.7
- Update changelog.md for v0.2.8
- Update changelog.md for v0.2.9
- Update changelog.md for v0.2.10
- Update releases.md for public repo builds
- Update changelog.md for v0.2.11
- Update releases.md with public repo workflow details
- Update changelog.md for v0.2.12
- Update changelog.md for v0.2.13
- Update changelog.md for main
- Update changelog.md for v0.2.14
- Fix changelog.md - clean up garbage from failed workflows
- Update releases.md with git-cliff and release body format
- Update changelog.md for v0.2.15
- Update changelog.md for v0.2.16
- Update releases.md - tags required in both repos for git-cliff
- Add git-cliff troubleshooting to releases.md
- Update changelog.md for v0.2.13
- Update changelog.md for v0.2.17
- Document beamterm-terx fork differences from upstream
- Update changelog.md for v0.2.18
- Update changelog.md for v0.2.19
- Update changelog.md for v0.2.20
- Update claude.md and releases.md for v0.2.20
- Update changelog.md for v0.2.21
- Update changelog.md for v0.2.22
- Add clerk + convex + polar migration design
- Add clerk + convex + polar implementation plan
- Add security-first test coverage design plan
- Add detailed security test coverage implementation plan
- Update claude.md to reflect clerk+convex+polar architecture
- Add subterm web app design document
- Add subterm web app implementation plan
- Update webapp plans — fly.io → ovh + caddy + tlsproxy
- Add descriptive plan for gossh-wasm lib and wsproxy



### :recycle: Refactor
- Rewrite selectionmanager with js-based rendering
- Switch from beamterm-terx fork to stock @beamterm/renderer
- Migrate dialogs.ts to daisyui modal pattern
- Migrate core components to daisyui
- Migrate dialogs to daisyui patterns
- Cleanup unused css and update remaining dialogs
- Migrate all ui components to pure daisyui/tailwind
- Replace exec channel with interactive pty popup
- Kitty graphics protocol — fix chunk assembly, pipeline order, validation



### :sparkles: New Features
- Add emoji picker and shortcuts help (v0.1.3)
- Dual-pane file manager + ssh key auth fixes
- Implement ssh host key verification system
- Cursor transparency and configuration improvements
- Smooth selection rendering during mouse drag
- Configurable clipboard shortcuts (ctrl+shift+c/v, shift+insert)
- Alt key toggles block selection mode
- Macos-style toggle switches + persist all settings
- Multiple connections per host + cmd/ctrl+t shortcut
- Focus management, dead key handling, storage cache, streaming utf-8
- Manual password entry + colorterm auto-injection
- Remove 'own supabase' option from storage selector
- Add auto-update system with github releases integration
- Improve changelog display in update dialog
- Display ssh auth banner (rfc 4252)
- Add disconnect dialog with reconnect functionality
- Replace theme arrows with dropdown picker
- Add searchable theme picker with live preview
- Remember window position and size across sessions
- Add daisyui 5 foundation
- Implement ssh agent auth and agent forwarding
- Add use_agent and agent_forward params to ssh_connect
- Add agent auth type and agent_forward field
- Add ssh agent translations (en-us, pl-pl)
- Add agent auth toggle and forward agent checkbox to host dialog
- Integrate agent auth and forwarding in connection flow
- Add local port forwarding (-l) with management ui
- Add biometric unlock (touch id / windows hello)
- Add convex schema with all tables and auth config
- Add clerk webhook handler and user sync
- Add clerk and convex client modules
- Add convex crud functions for all data tables
- Add polar subscription integration with webhook and frontend module
- Rewrite auth ui and auth flow for clerk + subscription check
- Rewrite storage, master-password, and settings for convex + clerk
- Fix polar webhook verification, checkout flow, and auth sync
- Add remote tool provisioning via ssh
- Send csi u sequence for shift+enter (newline in ai tools)
- Add drag-and-drop tab reordering
- Sort hosts by creation date (oldest first)
- Rename terx → subterm + integrate clerk/convex/polar auth
- Add cloudflare access tunnel support for ssh connections



### :white_check_mark: Testing
- Add comprehensive test suite (109 tests) for auth, storage, crypto, and backend
- Expand test coverage to 145 tests (+36) filling all identified gaps
- Add comprehensive hostkeys.rs security tests (~34 tests)
- Add lib/ssh/sftp/port_forward rust tests (~27 tests)
- Add beamterm wasm mock, skip clipboard paste test
- Add ts tests from previous session (encryptionprofiles, http, file-manager-state, session-manager, subscription, update-checker)
- Add ts security tests for clerk, biometry, and themes (70 tests)
- Add convex.ts client tests (10 tests)



### :wrench: Chores
- Bump version to 0.1.4
- Bump version to 0.1.7
- Bump version to 0.1.8
- Bump version to 0.1.9
- Fix changelog workflow + update changelog.md
- Add memory.db to gitignore
- Remove dead code and fix typescript errors
- Bump @kofany/beamterm-terx to 0.12.13
- V0.2.2
- V0.2.3
- Bump version to 0.2.5
- Bump version to 0.2.6
- Bump version to 0.2.8
- Bump version to 0.2.9
- Set version to 0.2.8
- Bump version to v0.2.10
- Bump version to v0.2.11
- Update lockfiles
- Bump version to v0.2.12
- Update russh to 0.57.0
- Update dependencies and remove unused packages
- Bump version to v0.2.13
- Bump version to v0.2.14
- Bump version to v0.2.15
- Bump version to v0.2.16
- Bump version to v0.2.18
- Bump version to v0.2.19
- Bump version to v0.2.20
- Remove all own-supabase references
- Bump version to v0.2.21
- Bump version to v0.2.22
- Add credentials backup file
- Add clerk, convex, polar dependencies and tauri plugins
- Remove supabase dependency and clean up references
- Update ghostty-vt.wasm to upstream b6dbd445d
- Remove obsolete design/plan documents
- Migrate to kofany/subterm + bump v0.2.23




## [v0.2.22] - 2026-02-07


### :bug: Bug Fixes
- Biometric unlock not working on windows



### :memo: Documentation
- Update changelog.md for v0.2.21



### :wrench: Chores
- Bump version to v0.2.22




## [v0.2.21] - 2026-02-07


### :memo: Documentation
- Update changelog.md for v0.2.20
- Update claude.md and releases.md for v0.2.20



### :sparkles: New Features
- Add biometric unlock (touch id / windows hello)



### :wrench: Chores
- Remove all own-supabase references
- Bump version to v0.2.21




## [v0.2.20] - 2026-02-06


### :memo: Documentation
- Update changelog.md for v0.2.19



### :sparkles: New Features
- Add local port forwarding (-l) with management ui



### :wrench: Chores
- Bump version to v0.2.20




## [v0.2.19] - 2026-02-06


### :memo: Documentation
- Update changelog.md for v0.2.18



### :sparkles: New Features
- Implement ssh agent auth and agent forwarding
- Add use_agent and agent_forward params to ssh_connect
- Add agent auth type and agent_forward field
- Add ssh agent translations (en-us, pl-pl)
- Add agent auth toggle and forward agent checkbox to host dialog
- Integrate agent auth and forwarding in connection flow



### :wrench: Chores
- Bump version to v0.2.19




## [v0.2.18] - 2026-02-03


### :bug: Bug Fixes
- Fix select elements using wrong classes
- Prevent custom select/input styles from overriding daisyui
- Remove legacy css that overrides daisyui component styles
- Properly configure daisyui 5 theme for component styling
- Remove -bordered classes removed in daisyui 5
- Update bun.lock with daisyui dependency



### :memo: Documentation
- Update changelog.md for v0.2.17
- Document beamterm-terx fork differences from upstream



### :recycle: Refactor
- Migrate dialogs.ts to daisyui modal pattern
- Migrate core components to daisyui
- Migrate dialogs to daisyui patterns
- Cleanup unused css and update remaining dialogs
- Migrate all ui components to pure daisyui/tailwind



### :sparkles: New Features
- Add daisyui 5 foundation



### :wrench: Chores
- Bump version to v0.2.18




## [v0.2.17] - 2026-02-02

### :bug: Bug Fixes

- Fix DPR handling with beamterm-terx 0.13.0 - use resizePhysical() for precise HiDPI control
- Fix charWidth/charHeight getters to return CSS pixels for FitAddon
- Switch from @beamterm/renderer to @kofany/beamterm-terx 0.13.0

## [v0.2.16] - 2026-02-01

### :bug: Bug Fixes

- Correct DPR handling for stock beamterm renderer - fixes black bars on HiDPI displays when changing font size
- Fix initial terminal sizing on first launch - container now properly measured before fit()

## [v0.2.15] - 2026-02-01

### :sparkles: New Features

- Remember window position and size across sessions

### :bug: Bug Fixes

- Help panel fixed size and improved styling

### :recycle: Refactor

- Switch from beamterm-terx fork to stock @beamterm/renderer

### :memo: Documentation

- Update RELEASES.md with git-cliff and release body format

## [v0.2.14] - 2026-01-31

### :sparkles: New Features

- Searchable theme picker with live preview - dropdown overlay replaces old arrow-based switcher

### :bug: Bug Fixes

- Fix shell injection vulnerability in changelog workflow

### :construction_worker: CI/CD

- Move release workflow to public repo for free GitHub Actions minutes
- Switch to git-cliff for changelog generation

## [v0.2.13] - 2026-01-31

### :wrench: Chores

- Update dependencies to latest stable versions
- Remove unused harfbuzzjs package

## [v0.2.12] - 2026-01-31

### :sparkles: New Features

- Disconnect dialog with reconnect functionality - when SSH connection drops, shows dialog with Reconnect/Close options

### :wrench: Chores

- Update russh to 0.57.0

## [v0.2.11] - 2026-01-31

### :sparkles: New Features

- Display SSH authentication banner (RFC 4252) - shows server's pre-auth message if present

### :construction_worker: CI/CD

- Add macOS Intel (x64) build to release workflow

## [v0.2.10] - 2026-01-30

### :lock: Security

- Remove legacy credentials.rs with insecure key derivation

## [v0.2.9] - 2026-01-29

### :sparkles: New Features

- Remove 'Own Supabase' option from storage selector
- Add auto-update system with GitHub Releases integration

## [v0.2.8] - 2026-01-29

### :bug: Bug Fixes

- Password dialog loses focus to terminal
- AUR uses native .pkg.tar.zst instead of .deb

### :construction_worker: CI/CD

- Add AUR package auto-publishing
- Add native Arch Linux build

## [v0.2.7] - 2026-01-29

### :sparkles: New Features

- Manual password entry option
- COLORTERM auto-injection for truecolor support

### :bug: Bug Fixes

- Correct SGR mouse motion encoding for no-button events
- Remove F3/Alt+D shortcut for debug window (conflicts with mc)

## [v0.2.6] - 2026-01-29

### :bug: Bug Fixes

- File manager tab shows host name in transfer-only mode
- Remove F5 shortcut for file manager (conflicts with mc, vim)
- Verify and correct keyboard shortcuts in help panel
- Escape key no longer closes dialogs when typing in text input
- Add missing .msi/.rpm to release

### :construction_worker: CI/CD

- Cross-repo release workflow to publish on OutrageLabs/terX

## [v0.2.4] - 2026-01-28

### :bug: Bug Fixes

- Restore PageList.zig memory zeroing for WASM

## [v0.2.3] - 2026-01-28

### :sparkles: New Features

- Focus management system with subterm-focus-terminal custom event
- Auto-focus terminal on window focus (Alt+Tab back)
- Dead key handling (disableDeadKeys option) for Windows US International keyboard
- In-memory cache for storage with mutation invalidation
- Update ghostty-vt WASM to latest upstream

### :bug: Bug Fixes

- Streaming TextDecoder for SSH data to handle UTF-8 sequences split across chunks
- Fix Ctrl+H double-firing on Windows

## [v0.2.2] - 2026-01-27

### :bug: Bug Fixes

- Fix tmux DCS passthrough unwrap causing base64 leakage
- Selection behavior in apps with mouse tracking (irssi, vim, MC)

### :wrench: Chores

- Bump @kofany/beamterm-terx to 0.12.13

## [v0.2.1] - 2026-01-17

### :bug: Bug Fixes

- Add SSH keepalive to prevent connection timeouts

## [v0.2.0] - 2026-01-17

### :sparkles: New Features

- Multiple connections per host + Cmd/Ctrl+T shortcut
- macOS-style toggle switches + persist all settings
- Alt key toggles block selection mode

## [v0.1.9] - 2026-01-17

### :sparkles: New Features

- Configurable clipboard shortcuts (Ctrl+Shift+C/V, Shift+Insert)

### :bug: Bug Fixes

- Terminal scrollback history not rendering when scrolled

## [v0.1.8] - 2026-01-16

### :sparkles: New Features

- Smooth selection rendering during mouse drag
- Cursor transparency and configuration improvements

## [v0.1.7] - 2026-01-16

### :sparkles: New Features

- SSH host key verification system

## [v0.1.6] - 2026-01-15

### :sparkles: New Features

- Auto-install terminfo on remote hosts
- Help Panel redesign with tabs

### :bug: Bug Fixes

- Complete i18n for Help Panel and error messages
- Use rsa-sha2-256/512 instead of deprecated ssh-rsa

## [v0.1.5] - 2026-01-15

### :bug: Bug Fixes

- SSH freeze with russh 0.56

### :sparkles: New Features

- Enhanced debug panel
- Error dialogs improvements

## [v0.1.4] - 2026-01-15

### :sparkles: New Features

- Dual-pane SFTP file manager (Norton Commander style)
- SSH key authentication improvements

### :bug: Bug Fixes

- Fix Unicode artifacts in WASM terminal by ensuring memory zeroing

## [v0.1.3] - 2026-01-13

### :sparkles: New Features

- Emoji picker with cross-platform support
- Keyboard shortcuts help panel (F1)

## [v0.1.2] - 2026-01-13

### :bug: Bug Fixes

- Characters disappearing at larger font sizes (25px+)

## [v0.1.1] - 2026-01-12

- Initial release
- Cross-platform SSH client with GPU-accelerated rendering
- WebGL2 terminal renderer via beamterm
- Ghostty VT100 parser integration
- Native text selection support
- Theme support with multiple built-in themes
- Local encrypted storage for credentials
- Subterm Cloud storage option with E2E encryption
