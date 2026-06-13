# Kensei Task

This directory contains a multimodal benchmark task designed to evaluate agentic workflow performance on administrative audits, cross-modal reconciliation, and compliance boundaries.

## Task Overview

The agent is tasked with preparing for the Roots Martial Arts Academy's annual belt ceremony by performing a complete operational audit. This requires:
1. Auditing the student roster, waiver status, and ceremony fees across active documents and mock API databases.
2. Reconciling pending expenses and calendar schedules to flag and resolve operational conflicts.
3. Drafting responses to unread emails under strict compliance and safety rules.

## Schema and Structure

The task bundle is organized as follows:
- **prompt.txt**: The natural-language, goal-oriented instruction.
- **task.yaml**: Metadata specifying L1/L2 category classifications, active APIs, distractor APIs, and difficulty level.
- **rubric.json**: Evaluation criteria for scoring agent actions and final output correctness.
- **test_outputs.py** and **test_weights.json**: Pytest-based validation tests and scoring weights to verify outcomes programmatically.
- **golden_steer_flow.md**: Step-by-step ground truth resolution path and value locks.
- **data/**: A directory containing 50 generically named documents (25 active signal files, 25 noise files) comprising text, spreadsheets, images, and audio/video modalities.
- **mock_data/**: Mock databases simulating whitelisted API services (Airtable, Gmail, Google Calendar, QuickBooks, Stripe) and empty distractor databases (HubSpot, Slack, WhatsApp).
- **persona/**: Contextual information defining the persona's background, memory, daily routine, and constraints.
