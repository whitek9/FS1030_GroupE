# Group Project Requirements

## Login Page

- [ ] This needs to be the landing page, and leverage a token to authenticate a user and allow them into the authenticated/protected area

## Landing Page & Search Interface

- [ ] Should show user details (e.g. Dr. Smith, employee # 1234567890, Last Login, etc.) as well as clear patient search bar with direction to search by Health Card Number

## Patient Details Page

- [ ] This needs to be the base page where all patient details are displayed, as well as buttons to allow updating of the client record, viewing of record revision history, adding of note to record, and showing existing notes in reverse chronological order

## Update Patient Details Page

- [ ] Do we want to make this on a per-field basis? Consider the menu along the left side of the example page in the Project Instructions document... we could have an "update" button that persists on each page that will then pop up a modal window with an update/add details screen which we can leverage as a design pattern for all pages

## Revision History Page

- [ ] This is fairly simple - should show all notes as line items in reverse chronological order

- [ ] Ideally these could also be searchable and/or sortable, so it defaults to reverse chronological, but could then be sorted to show chronological if desired (this is a stretch goal...!)

## Add Note Page

- [ ] Could this just be a modal that pops up from a button that persists in the basic details area of the Patient Details page? It could then just be a text field and a submit/cancel button - timestamp would be automatically generated once the user submits, and would leverage (most of) the design pattern from the update details modal

## Admin Login Page/Button/Modal

- [ ] Should only be accessible from the secure area (and redirects to the initial login page if we try to navigate to it directly via URL)

- [ ] A couple approaches: requires user to login AGAIN with same username/password, OR we can try and pull it from session storage. If we do that, it just shows an error for those who aren't admins that says "Unauthorized, please contact your administrator for access" or something like that

- [ ] Should have an admin landing page that shows 4 options: Search for Patients, Add New Patient, Search for Care Providers, Add New Care Provider

## Add New Patient Page

- [ ] Flow should walk through each of the following:

- [ ] Name & Contact Information (title(dropdown, NULL), firstName, lastName, Health Card Number, email, phoneNumber, all address fields, Emergency contact name/number/address/relationship)
- [ ] Demographic Information (height, weight, sex, DOB)
- [ ] Medical History (This can be a textarea)
- [ ] Medication and Allergies (This can be a textarea, but should be a searchable list for medications with fields for dosage, start date, notes, etc... bit complicated so let's set it as a stretch goal)
- [ ] Immunization Status (Same as Medication and Allergies)
- [ ] Laboratory Test Results (This can be a textarea)
- [ ] Radiology Images (should show list of URLs to images????)
- [ ] Billing/Insurance Information (insuranceProvider, planContractNum, memberCertNum, planNum, drugPlan, carrierCode)

- [ ] Should also assign patientID via auto-increment, and UUID

- [ ] Upon submitting, should show View Patient Page (from above) with all details and an alert that says `New Patient, ${patient.firstName} ${patient.lastName} successfully added!`

## Add New Care Provider Page

- [ ] Flow should walk through each of the following:

- [ ] Name & Contact Information (title(dropdown, NULL), firstName, lastName, email, phoneNumber, all address fields, Emergency contact name/number/address/relationship)
- [ ] Specialization (NULL)

- [ ] Should also assign careProviderID via auto-increment, and UUID

- [ ] Upon submitting, should show View Care Provider Page (from below) with all details and an alert that says `New Care Provider, ${careProvider.firstName} ${careProvider.lastName} successfully added!`

## Search Patients Page

- [ ] Should show patients based on Healthcare Card Number search as list item(s)

- [ ] Each list item should have three buttons: Update, Delete and View

- [ ] Update button opens Patient Details Page (from above) for that patient in new tab/window with Patient Demographic details modal opened

- [ ] Delete button should allow you to delete, but have an "Are you sure?" message before executing the task - it should only hide from search, but maintain the record in the database

- [ ] View button opens Patient Details Page (from above) for that patient in new tab/window

## Search Care Providers Page

- [ ] Should show Care Providers based on Employee Number search as list item(s)

- [ ] Each list item should have three buttons: Update, Delete and View

- [ ] Update button opens View Care Provider Page (from below) in new tab/window with Update Care Provider Modal opened

- [ ] Delete button should allow you to delete, but have an "Are you sure?" message before executing the task - it should only hide from search, but maintain the record in the database

- [ ] View button View Care Provider Page (from below) in new tab/window

## View Care Provider Page

- [ ] Should show Care Provider details 



