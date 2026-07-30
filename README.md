# BFSP 2026 WP8 - Activity 2 (MetaBuddy): API spec for MetaBuddy communcation with ISA Wizard

## Introduction

This repo contains the API specifications as defined in activity 2 of the ELIXIR BFSP 2026 WP8 MetaBuddy program. It documents how the ISA Wizard can access the functionalities developed for the MetaBuddy.

## Technical details

Github Actions are used to build the documentation with redocly. A mock server is hosted by Render (free tier) based on docker and Prism. A new action is triggered each time the openapi.yaml file is updated (minimal or conversational) which rebuilds the documentation and redeploys the mock server with webhooks.

### Note on mock server
The mock server is hosted by Render free tier, which can react slowly on the first request as it needs to be reinitialized after a period of inactivity. 

## Links

Link to full BFSP 2026 program:
https://docs.google.com/document/d/18MXaPiY-Q12EjzYf6m-7YFy6bwJ0x4n9gSVQ0A7HOHk/edit?tab=t.0

Minimal API page:
https://vib-agro-incubator.github.io/bfsp2026-wp8-metabuddy-activity2/minimal/

Conversational API page:
https://vib-agro-incubator.github.io/bfsp2026-wp8-metabuddy-activity2/conversational/

Minimal mock server:
https://bfsp2026-wp8-metabuddy-activity2.onrender.com

Conversational mock server:
https://bfsp2026-wp8-metabuddy-activity2-20ux.onrender.com

Render.com
https://dashboard.render.com/

Stoplight Prism for mock servers
https://stoplight.io/open-source/prism

