# proc-ok Action

A simple GitHub Action to trigger deployments on proc-ok using a webhook.

## Features

- Trigger deployments via webhook
- Automatically send commit metadata
- Lightweight and easy to integrate
- Works with custom deployment systems

---

## Usage

```yaml
name: Deploy

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Trigger Deployment
        uses: lutfisobri/proc-ok-action@v1
        with:
          webhook-url: ${{ secrets.PROC_OK_WEBHOOK_URL }}
          token: ${{ secrets.PROC_OK_TOKEN }}