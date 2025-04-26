# Idle Kubernetes Cluster Scanner

A simple OpenOps workflow to automatically detect Kubernetes clusters with less than 10% CPU/Memory utilization.

## About

Idle Kubernetes clusters waste cloud costs silently.  
This workflow continuously scans your cluster utilization and alerts you when it falls below a healthy threshold.

## How It Works

1. **Schedule**: Runs at regular intervals.
2. **Fetch Metrics**: Collects cluster usage data from Kubernetes.
3. **Condition Check**: Flags clusters running under 10% utilization.
4. **Slack Alert**: Sends a notification if idle clusters are found.
5. **End**: Completes the workflow cleanly.

## Features

- Fully no-code using OpenOps.
- Easy threshold customization.
- Works with Kubernetes and cloud metric connectors.
- Lightweight and fast to deploy.

## Requirements

- OpenOps account.
- Kubernetes metric connector configured.
- Slack connector for notifications.

## Usage Instructions

1. Import the `idle-k8s-cluster-scanner.json` into OpenOps.
2. Connect your Kubernetes metrics source.
3. Connect your Slack account for alerts.
4. Adjust the schedule timing as per your needs.
5. Optionally, modify the utilization threshold inside the condition block.

## Notes

- You can replace Slack with email or other messaging platforms easily.
- The workflow can be extended to trigger auto-scaling or shutdown actions for idle clusters.
- Edit the "Condition" block to change the 10% threshold to your preferred value.

## Extending This Workflow

- Add cost estimation to highlight financial impact.
- Integrate automatic remediation actions.
- Expand to monitor other cluster resources like persistent volumes.
