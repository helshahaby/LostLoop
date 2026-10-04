# LostLoop

AI lost-and-found agent by **Hossam Elshahaby**.

Built for the Agentic AI Hack, Stockholm, 3 October 2026.

- [Live app](https://itemlostandfound.lovable.app)
- [Demo video](https://youtu.be/P0A6O4n_xd8)

## Problem

Owners search scattered posts while reception teams manually compare descriptions and decide whether a claimant owns an item.

## Solution

A finder posts a photo and keeps an identifying detail private. An owner describes the loss. The agent searches candidate items, asks an ownership question, and guides the case toward a custodian-approved return.

## App features

- Photo reporting with editable listing fields and demo images.
- Natural-language claim conversation.
- A hidden detail for ownership questions.
- Live agent activity showing search and verification actions.
- Handover and returned-status workflow described by the app.

## Observed prototype behavior

On 4 October 2026, the public interface and a labelled backpack demo were inspected. The agent searched two records and asked what items and colours were inside the main compartment. The interface attributes the agent to Gemini. A displayed matching score is not a measured accuracy result.

Completed verification, handover, notifications, photo analysis and backend persistence were not independently tested in this review. The proposed architecture in the specification is a recommendation, not a verified source-code inventory.

## Try the demo

1. Open the live app and choose **I lost something**.
2. Enter: `I lost a black backpack with a red keychain`.
3. Watch the activity log as the agent searches and asks a verification question.
4. For this explicitly labelled demo, the homepage gives the expected contents: a laptop and a blue notebook.
5. Follow the remaining app prompts or watch the linked video.

Production records must keep expected verification answers private. The public demo hint must not be reused as a production verification design.

## Suggested architecture

Web client, authenticated backend, item database, image storage and a Gemini agent with constrained search and verification tools. Store private evidence server-side, enforce permissions outside the model, and require custodian confirmation for handover.

## Validation and next steps

Test incorrect claims, ambiguous matches, private-data access, model failures and status persistence. Run a venue pilot measuring recovery time, confirmed returns, incorrect approvals and staff minutes per case. No quantified impact results are claimed yet.

## Deliverables

- `LostLoop_Pitch.pptx`: six slides with click-triggered reveal animations.
- `LostLoop_Project_Specs.pdf`: requirements, proposed architecture and acceptance tests.
- `README.md`: overview and demo links.

Source code and deployment instructions are not included in this documentation package. No repository URL was supplied.
