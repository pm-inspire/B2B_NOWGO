# B2B Deal Cycle - Complete Description

## Overview

This document describes the complete cycle for the B2B Deal feature in the Seller Dashboard. The system allows sellers to create deals and other sellers to request those deals, creating a B2B marketplace environment.

---

## User Roles

| Role | Description |
|------|-------------|
| **Seller A (Deal Owner)** | Creates and manages deals, reviews incoming requests |
| **Seller B (Buyer)** | Browses available deals, submits requests to purchase |

---

## Phase 1: Deal Creation (Seller A)

### Steps:
1. Seller A logs into the dashboard
2. Navigates to "Create New Deal" section
3. Fills in the deal form with the following required fields:

### Deal Form Fields:

| Field | Type | Description |
|-------|------|-------------|
| **Product Image** | Image Upload | Visual representation of the product |
| **Quantity** | Number | Total units available for this deal |
| **Price** | Currency | Price per unit |
| **Start Date** | Date | When the deal becomes active |
| **End Date** | Date | When the deal expires |

### Outcome:
- Deal is published and visible in the B2B marketplace
- Status is set to "Active"

---

## Phase 2: Deal Discovery (Seller B)

### Steps:
1. Seller B logs into the dashboard
2. Navigates to "Browse Deals" or "Marketplace" section
3. Views list of all active deals from other sellers
4. Can filter/search deals (optional feature)
5. Clicks on a deal to view full details

### Deal Details View Shows:
- Product image
- Available quantity
- Price per unit
- Deal validity period (start & end dates)
- Seller information
- Deal status

---

## Phase 3: Request Submission (Seller B)

### Steps:
1. Seller B views a deal they're interested in
2. Clicks "Request Deal" button
3. Fills in request form:

### Request Form Fields:

| Field | Type | Description |
|-------|------|-------------|
| **Requested Quantity** | Number | Units the buyer wants (max: available quantity) |
| **Message** | Text | Optional note to the deal owner |

4. Submits the request
5. Request status is set to "Pending"

### Outcome:
- Request is created in the system
- Deal owner receives notification
- Buyer can track request in "My Requests" section

---

## Phase 4: Request Review (Seller A)

### Steps:
1. Seller A receives notification of new request
2. Navigates to "Incoming Requests" section
3. Reviews request details:
   - Buyer information
   - Requested quantity
   - Buyer's message
   - Total value calculation

### Decision Options:

| Action | Description | Next Step |
|--------|-------------|-----------|
| **Approve** | Accept the request as-is | Proceed to Deal Completion |
| **Reject** | Decline the request | Buyer notified, can browse other deals |
| **Negotiate** (Optional) | Send counter-offer | Negotiation cycle begins |

---

## Phase 5: Negotiation Cycle (Optional)

If the deal owner chooses to negotiate:

### Steps:
1. Seller A sends counter-offer (modified price/quantity/terms)
2. Seller B receives notification
3. Seller B can:
   - **Accept** → Proceed to Deal Completion
   - **Decline** → Request closed
   - **Counter** → Send new terms back to Seller A
4. Cycle repeats until agreement or rejection

---

## Phase 6: Deal Completion

Once a request is approved:

### Steps:
1. **Agreement Generation**
   - System generates deal agreement/contract
   - Both parties receive confirmation

2. **Payment Processing**
   - Buyer processes payment
   - Payment confirmation sent to both parties

3. **Delivery Arrangement**
   - Seller arranges product delivery
   - Tracking information shared (if applicable)

4. **Deal Closure**
   - Delivery confirmed
   - Deal marked as "Completed"

5. **Rating & Review** (Optional)
   - Both parties can rate the transaction
   - Reviews visible on seller profiles

---

## Status Flow Summary

```
Deal Status:
Draft → Active → (Expired/Sold Out)

Request Status:
Pending → Approved/Rejected/Negotiating → Completed/Cancelled
```

---

## Notifications

The system sends notifications at these points:

| Event | Recipient | Notification |
|-------|-----------|--------------|
| New deal published | All sellers | "New deal available in marketplace" |
| Request submitted | Deal owner | "New request received for [Deal Name]" |
| Request approved | Buyer | "Your request has been approved" |
| Request rejected | Buyer | "Your request has been declined" |
| Counter-offer sent | Recipient | "New counter-offer received" |
| Payment received | Seller | "Payment confirmed for [Deal Name]" |
| Deal completed | Both | "Deal successfully completed" |

---

## Dashboard Sections

### For All Sellers:

| Section | Description |
|---------|-------------|
| **Dashboard Home** | Overview with stats and recent activity |
| **My Deals** | List of deals created by the seller |
| **Create Deal** | Form to create new deals |
| **Browse Deals** | Marketplace to view other sellers' deals |
| **Incoming Requests** | Requests received for seller's deals |
| **My Requests** | Requests the seller has made to others |

---

## Key Metrics to Track

- Total active deals
- Pending requests count
- Approved deals count
- Total transaction value
- Average deal completion time

---

## Summary Flowchart (Text Version)

```
SELLER A                          SELLER B
   │                                  │
   ▼                                  │
[Create Deal]                         │
   │                                  │
   ▼                                  │
[Fill Form: Image, Qty,               │
 Price, Start/End Date]              │
   │                                  │
   ▼                                  │
[Publish Deal] ─────────────────► [Browse Deals]
   │                                  │
   │                                  ▼
   │                            [View Deal Details]
   │                                  │
   │                                  ▼
   │                            [Submit Request]
   │                                  │
   ▼                                  │
[Receive Request] ◄───────────────────┘
   │
   ▼
[Review Request]
   │
   ├──► [Approve] ──► [Generate Agreement] ──► [Process Payment] ──► [Complete]
   │
   ├──► [Reject] ──► [Notify Buyer]
   │
   └──► [Negotiate] ──► [Counter-Offer Cycle]
```

*Document prepared for project owner review and confirmation.*
