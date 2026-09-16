# CLAUDE.md

This file provides guidance to Claude Code when working in this repository.

## What this is

The presentation layer for Diario Nacional. **This theme owns front-end and dashboard design only** — no business logic, no direct database queries beyond calling functions/hooks exposed by the companion plugin, `diario-nacional-core`. That split is deliberate: the theme should be able to be redesigned or replaced without touching anything that handles money, credits, or legal compliance.

Full project context, business domain, and the phase plan live in `diario-nacional-core`'s `CLAUDE.md` — read that first. The original technical audit of the legacy system being replaced is here: **https://claude.ai/artifact/Fmg4eEzUNc4VsTwpaVVzs8**.

## Design mandate

Jorge has been explicit: the legacy front-end and user dashboard are functional but dated, and a big part of the motivation for this rebuild is a genuinely modern redesign of both. This is **hand-coded HTML/CSS/JS, no page builder** (no Divi, no Elementor) — same reasoning as OpenREAL's theme: a page builder adds a layer of abstraction and weight that a small, purpose-built system doesn't need.

Design work is scheduled as its own phase near the end of the plan (Fase 7), after the functional core is verified equivalent to the legacy system — don't front-load visual polish before the underlying data/logic is solid.

## Environments

Local (LocalWP) → staging (`dev.diarionacional.com.mx`, deployed via cPanel Git Version Control pulling from this repo's `main`) → Jorge's existing cPanel production at `diarionacional.com.mx` (cutover process TBD, deferred until staging is verified). Nothing gets pushed to any shared branch or deployed without Jorge's explicit go-ahead.

## Status

Fase 0: repo scaffolding only, minimal valid WordPress theme header. No templates built yet.
