# Internal Complaint Review and Appointment Workflow

## Guide for Customer Care, Service Coordinators, and Service Team

The Customer Complaint Registration Portal receives customer and sales-channel service requests. Each submitted complaint is reflected in the authenticated Jacky's Service Portal, where the Customer Care Executive reviews the request and creates the appointment.

Use the internal portal link:

**https://service-jackys.github.io/portal/**

## End-to-end workflow

```text
Customer or Sales Channel submits complaint
                ↓
Complaint appears in Scheduler → Complaint Inbox
                ↓
CCE reviews and completes missing information
                ↓
CCE loads the complaint into New Request
                ↓
CCE enters appointment date and time
                ↓
CCE creates the appointment
                ↓
Complaint is linked to the appointment and marked Scheduled
```

## 1. Open the internal portal

1. Open **https://service-jackys.github.io/portal/**.
2. Sign in using your authorized Service Portal account.
3. Open the **Scheduler** section.
4. Select **Complaint Inbox**.

The Complaint Inbox is available only to authorized users with Scheduler access.

## 2. Review the Complaint Inbox

The inbox displays submitted complaints, normally with the newest requests first. Review the following information:

- Complaint reference number.
- Date received.
- Customer or company name.
- Contact number and email.
- Location and region.
- Brand, model, and serial or item code.
- Complaint description.
- Current complaint status.

Use the status filter to focus on new, pending, or other complaint categories. Use the refresh control to retrieve the latest submissions.

The Dashboard complaint indicator shows the number of complaints that are not yet Scheduled, Closed, or Cancelled.

## 3. Open and review a complaint

Select a complaint row to open its details. Confirm the information submitted by the customer or sales representative.

Complete or correct the fields that are owned by the internal service team, including:

- Location and region.
- B2B branch or school.
- Site contact information.
- Customer number.
- Sales order number.
- Brand, model, and serial or item code.
- CCE notes.
- Warranty classification.
- Appointment date and time, when already known.
- Assigned technician, when appropriate.
- Final service status.
- Complaint status.

Use **Save Complaint** when you are updating the complaint record without creating the appointment yet.

## 4. Complaint statuses

Use only the status that accurately represents the current stage:

| Status | Use when |
| --- | --- |
| **New** | The complaint has been received and has not yet been reviewed. |
| **Under Review** | Customer Care is reviewing the request or contacting the customer. |
| **Pending Information** | Required information or confirmation is still awaited. |
| **Ready for Scheduling** | The request is complete and can be scheduled. |
| **Scheduled** | The appointment has been successfully created and linked. |
| **Closed** | The service request lifecycle is complete. |
| **Cancelled** | The request has been cancelled and will not be scheduled. |

Do not mark a complaint as **Scheduled** manually before the appointment has been successfully created through the New Request workflow.

## 5. Load the complaint into New Request

After reviewing the complaint:

1. Select **Load into New Request**.
2. Confirm that the Scheduler New Request form contains the correct customer information.
3. Confirm or complete the following required fields:
   - Customer Name.
   - Contact No.
   - Appointment Date.
   - Appointment Time.
4. Complete any remaining service details.
5. Select a technician if assignment is ready; otherwise leave it unassigned if the existing process allows assignment later.
6. Confirm the warranty and customer information.

The complaint reference is retained on the New Request form and will be linked to the appointment when the appointment is created.

### Important appointment rule

A newly submitted complaint normally does not contain an appointment date or time. Loading the complaint keeps the default appointment date available, but the CCE must enter a valid appointment time before creating the appointment.

The appointment cannot be created until Customer Name, Contact No., Appointment Date, and Appointment Time are completed.

## 6. Create the appointment

When the New Request form is complete:

1. Review all customer and service details.
2. Confirm the appointment date and time.
3. Confirm the technician assignment or leave it according to the scheduling process.
4. Select the appointment creation action.
5. Wait for the success confirmation and appointment number.
6. Return to Complaint Inbox or refresh it to confirm the complaint is now linked and marked **Scheduled**.

The system creates the appointment and updates the complaint linkage together under the protected Scheduler process. If the linkage cannot be completed, the appointment creation is rolled back rather than leaving an incomplete appointment record.

Do not create a second appointment for the same complaint unless the original attempt clearly failed and the record was not created.

## 7. After scheduling

After successful appointment creation:

- Keep the complaint reference and appointment number together.
- Confirm the complaint status is **Scheduled**.
- Communicate the appointment details to the customer or sales representative.
- Add any required follow-up notes through the internal workflow.
- Use the existing Scheduler update process for later changes.

The customer-facing portal does not expose technician information, scheduler records, internal notes, warranty decisions, or appointment management.

## Common issues and actions

### The complaint is not visible

- Select **Refresh** in Complaint Inbox.
- Confirm that you are signed in with Scheduler permission.
- Check the status filter.
- Confirm that the customer or sales representative received a successful complaint reference.

### Customer Name or Contact No. is missing after loading

- Return to Complaint Inbox and open the complaint again.
- Confirm the source complaint contains the submitted values.
- If the issue persists, record the complaint reference and contact the system administrator.

### Appointment Date and Time validation appears

This normally means one or both appointment fields are blank. Enter the appointment date and appointment time in New Request, then submit again.

A complaint submission is not an appointment confirmation; the internal team must complete these scheduling fields.

### The complaint cannot be marked Scheduled

Do not force the status manually. Confirm that:

- The complaint reference was retained on New Request.
- Customer Name and Contact No. are complete.
- Appointment Date and Time are complete.
- The complaint still exists in Complaint Inbox.
- The user has Scheduler permission.

If the problem continues, retain the error message, complaint reference, and time of the attempt for investigation.

### Duplicate complaint submissions

Search by complaint number, customer name, contact number, or sales order number before creating a new appointment. If duplicates exist, keep the correct complaint active and update the duplicate according to the team's operating procedure.

## Responsibilities

### Customer Care Executive

- Review new complaints.
- Contact the customer or sales channel when clarification is needed.
- Complete internal fields accurately.
- Set the correct complaint status.
- Load the complaint into New Request.
- Enter appointment date and time.
- Create and verify the linked appointment.

### Sales Team or Sales Channel

- Submit complete and accurate customer information.
- Provide the complaint reference to the customer.
- Avoid creating duplicate complaints.
- Support Customer Care with missing order, customer, or site information.

### Service Coordinator or Supervisor

- Monitor open complaint counts.
- Review pending and ready-for-scheduling complaints.
- Support technician and appointment allocation.
- Confirm that scheduled complaints are followed through to closure.

## Security and data handling

- Use only your own authorized Service Portal account.
- Never share login credentials or session information.
- Do not expose the internal portal link or screenshots containing customer data publicly.
- Enter only information necessary for service processing.
- Treat customer contact details, order information, service history, and internal notes as confidential.

## Quick links

- **Internal Service Portal:** https://service-jackys.github.io/portal/
- **Customer Complaint Registration:** https://service-jackys.github.io/complaints/
