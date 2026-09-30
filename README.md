# BFSP 2026 WP8 - Activity 2 (MetaBuddy): API spec for MetaBuddy communication with ISA Wizard

## Introduction

This repo contains the API specifications as defined in activity 2 of the ELIXIR BFSP 2026 WP8 MetaBuddy program. It documents how the ISA Wizard can access AI enrichment functionalities developed for the MetaBuddy.

There are 2 APIs in the openapi subfolder:
- minimal: contains the minimum calls needed to access the MetaBuddy functionality
- conversational: session based API with support for asynchronous processing, for a more conversational approach with the MetaBuddy functionalities

Each API has a mockup server docker as specified in the docker folder. The mockup servers are currently hosted by Render.com

Currently both the minimal and conversational API versions have been set to 1.0.0.

## Technical details

GitHub Actions are used to build the API documentation in OpenAPI yaml format. These are served on github pages with redocly. A mock server is hosted by Render (free tier) based on a Docker image with Prism. A new action is triggered each time the openapi.yaml file is updated (minimal or conversational) which rebuilds the documentation and redeploys the mock server via a deploy hook. When the version in the OpenAPI spec changes, the GitHub action will also generate a new tag in github.

#### Note on mock server
As the mock server is currently hosted by Render free tier, it can react slowly on the first request as it needs to be reinitialized after a period of inactivity. Once the first request has returned, subsequent requests should return instantly.

## Links

| Resource | URL |
|---|---|
| BFSP 2026 program (full doc) | [Google Doc](https://docs.google.com/document/d/18MXaPiY-Q12EjzYf6m-7YFy6bwJ0x4n9gSVQ0A7HOHk/edit?tab=t.0) |
| Minimal API docs | [vib-agro-incubator.github.io/…/minimal/](https://vib-agro-incubator.github.io/bfsp2026-wp8-metabuddy-activity2/minimal/) |
| Conversational API docs | [vib-agro-incubator.github.io/…/conversational/](https://vib-agro-incubator.github.io/bfsp2026-wp8-metabuddy-activity2/conversational/) |
| Minimal mock server | [bfsp2026-wp8-metabuddy-activity2.onrender.com](https://bfsp2026-wp8-metabuddy-activity2.onrender.com) |
| Conversational mock server | [bfsp2026-wp8-metabuddy-activity2-20ux.onrender.com](https://bfsp2026-wp8-metabuddy-activity2-20ux.onrender.com) |
| Render dashboard | [dashboard.render.com](https://dashboard.render.com/) |
| Stoplight Prism (mock server tooling) | [stoplight.io/open-source/prism](https://stoplight.io/open-source/prism) |


