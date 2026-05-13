# Phase 0 Status — Repository Structure

## Status

STRUCTURE CREATED / DECISION RECORD ADDED

## Objective

Create a clean repository structure for the Tracing Board rebuild while preserving existing legacy material.

## Existing Legacy Material

The following existing repo areas are retained:

- `MasonicQuiz/`
- `Papers/`
- `images/`
- `index.html`
- `README.md`
- `RAC`
- `LICENSE`

## New Platform Structure

The new structure separates:

- project control
- public website application
- Discourse configuration and theme work
- infrastructure/deployment scripts
- content model
- documentation
- legacy archive

## Rule

No legacy content is deleted during Phase 0.

## Phase 0 Decision Records

- ADR-0001-platform-architecture.md

## Repository Hygiene

- .gitattributes added to normalise line endings across Windows, GitHub, Codex, Lovable, and Linux deployment environments.