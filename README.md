# Action Repository

This repository is used to trigger GitHub events (Push, Pull Request, and Merge)
that are captured by a webhook service.

## Purpose

The goal of this repository is to generate GitHub actions such as:
- Code pushes
- Pull request creation
- Pull request merges

These events are sent via GitHub Webhooks to the `webhook-repo`, where they are
processed and stored in MongoDB. 

## How it works

1. GitHub Webhooks are configured on this repository.
2. On every Push, Pull Request, or Merge action, GitHub sends a payload
   to the webhook endpoint.
3. The webhook endpoint (in `webhook-repo`) processes the payload and saves
   the event details.
4. A frontend UI periodically fetches and displays these events.

## Webhook Events Enabled

- Push
- Pull Request

## Usage

Use this repository to:
- Push commits to any branch
- Create pull requests
- Merge pull requests

Each action will trigger a webhook event and be reflected in the UI.

## Notes

This repository does not contain any backend or frontend logic.
It is only used to generate GitHub events for testing the webhook integration.
