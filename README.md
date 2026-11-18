# Campus Stores – Product Engineering Practical

## Overview

This submission improves the Campus Stores equipment desk by introducing a **Request-wise Equipment Tracker** to provide better visibility into equipment issuance, returns, and outstanding items.

The improvement is based on the experience of completing the sample shift, particularly the partial return of equipment and the handover between two shifts.

## 1. What I observed

The existing application provides a useful workflow for managing equipment:

- Approved requests provide the equipment requirements.
- Inventory tracks individual physical units and their availability.
- The loan register maintains a separate issue slip for each physical unit.
- The desk book captures messages and handover notes.

However, when a request contains multiple equipment items, the operator needs to refer to individual loan slips to understand the overall return status of that request.

This becomes particularly relevant when equipment is returned in multiple stages or remains outstanding across shifts.

## 2. What I changed

### Request-wise Equipment Tracker

I introduced a dedicated Request Tracker section that consolidates equipment information at the request level.

The improvement includes:

- Grouping equipment by its approved request.
- Displaying the total number of items issued and returned.
- Showing the return status of each individual physical unit.
- Adding visual progress indicators to communicate return completion.
- Distinguishing returned items from outstanding items.

The tracker derives its information from the existing loan records, avoiding the need for a separate tracking process.

## 3. Evidence from the sample shift

I used the Film Society's Courtyard Screening request (RQ-214) to evaluate the workflow.

The request involved three physical units:

- HDMI projector (PR-04)
- Portable speaker (SP-02)
- USB-C to HDMI adapter (AD-12)

All three items were issued to Kabir Sen using separate loan slips.

At Friday, 7:30 pm, the projector and speaker were returned, while the adapter remained outstanding with Leela Das.

The next morning, at Saturday 9:00 am, the adapter was returned and the request was completed.

The tracker made the following progression visible:

| Stage | Items issued | Items returned |
|---|---:|---:|
| After pickup | 3 | 0 |
| Friday evening | 3 | 2 |
| Saturday morning | 3 | 3 |

## 4. What I retained

I retained the existing application structure and its core workflows:

- Individual loan slips for physical-unit accountability.
- Inventory availability and repair status.
- Existing return-recording functionality.
- Desk book for communication and shift handover.
- Time-based sample shift progression.

The tracker complements these features rather than replacing them.

## 5. Walkthrough using the improved product

For the Courtyard Screening request:

1. Open the approved request and identify the required equipment.
2. Issue each physical unit through the loan register.
3. Use the Request Tracker to verify the issuance status.
4. Record the projector and speaker returns at the evening counter.
5. Identify the adapter as the outstanding item.
6. Add a handover note for the next shift.
7. Record the adapter's return the following morning.
8. Verify that all three items are returned in the Request Tracker.

## 6. How I would evaluate the improvement

I would test the updated workflow at a real equipment counter during multiple shift handovers.

One key observation would be the **time taken by an incoming staff member to identify all outstanding equipment for a request without assistance from the previous shift**.

A reduction in this time, along with fewer missed or incorrectly recorded returns, would indicate that the tracker is improving operational clarity.

## Conclusion

The improvement focuses on making the equipment return process easier to understand, particularly when a request involves multiple physical units and partial returns.

Rather than replacing the existing workflow, the Request-wise Equipment Tracker adds a consolidated view that helps desk staff maintain visibility and accountability across shifts.

The prototype demonstrates how a small, targeted product improvement can address a practical operational problem while preserving the strengths of the original application.
