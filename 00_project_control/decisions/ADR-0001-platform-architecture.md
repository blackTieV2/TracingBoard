# ADR-0001 — Tracing Board Platform Architecture

## Status

Accepted

## Date

2026-05-13

## Context

Tracing Board was formerly a printed Masonic learning and education periodical and later operated through a Wix/Ashlar forum-style site. The forum model became ineffective after platform changes, and traffic declined sharply.

The rebuilt platform must support:

- Masonic papers and educational content
- member questions and discussion
- comments and replies
- multiple learning and committee sections
- Q&A-style engagement
- future live chat or Discord-style integration
- a public identity independent of Layer-8 Labs
- sustainable administration by a small editorial/moderation team

The domain tracingboard.org has been registered for this purpose.

## Decision

The Tracing Board platform will be built using a split architecture:

- tracingboard.org: public editorial and landing website
- community.tracingboard.org: Discourse-based community, forum, Q&A, papers, and member discussion

GitHub is the source of truth for project structure, documentation, site code, infrastructure notes, and operating decisions.

Lovable may be used to rapidly create and iterate the public website.

Codex may be used for engineering support, repository review, refactoring, deployment scripts, hardening, documentation, and automation.

Discourse is the preferred community engine and should not be replaced by a custom-built forum unless a future decision record explicitly reverses this position.

The production public platform should be cloud-hosted and should not be hosted from the Layer-8 Labs home lab at this stage.

## Rationale

A custom forum would create unnecessary security, moderation, authentication, notification, and maintenance risk.

Discourse already provides mature community features such as user accounts, roles, categories, moderation, notifications, email integration, trust levels, and long-form discussion.

Lovable is suitable for rapid visual development of the public site, but it should not be used to reinvent the full community platform.

Codex is suitable for engineering work after the project has a repository, structure, and deployment target.

The Layer-8 Labs home lab should remain available for staging, experimentation, backups, and future private tooling, but not as the first production public host.

## Consequences

The repository must support several workstreams:

- public website development
- Discourse configuration and theme work
- infrastructure and deployment documentation
- editorial governance
- moderation policy
- launch planning
- content migration

The production hosting decision remains separate from the repository structure decision.

## Current Hosting Direction

Preferred initial hosting model:

- Cloudflare: DNS, domain control, basic edge security, and email routing
- DigitalOcean Singapore VPS: Discourse production host
- Lovable, external static hosting, or future VPS deployment: public website hosting option

## Non-Goals

This decision does not approve:

- custom forum development from scratch
- public hosting from Layer-8 Labs
- exposing home-lab services for Tracing Board production
- merging the public Tracing Board identity with layer-8-labs.com
