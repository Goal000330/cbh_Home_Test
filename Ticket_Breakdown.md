## Ticket 1: Update Agent model to include custom ids

### Description

Create a new field in the Agent model that allows for custom ids to be saved for each Agent.

### Acceptance Criteria

- A new column named "custom_id" must be added to the Agent table in the database.
- An API endpoint must be created to allow Facilities to update the custom_id field for each Agent in their roster.
- The "generateReport" function should be updated to use the custom_id instead of the internal database id.

### Time/Effort Estimate

2 hours

### Implementation Details

- Use a database migration to add the "custom_id" field to the Agent table.
- Create a new PUT endpoint in the API for Facilities to update the custom_id field.
- Update the query in the "generateReport" function to select the custom_id instead of the Agent's internal id.

## Ticket 2: Update the getShiftsByFacility function to include custom ids

### Description

Update the "getShiftsByFacility" function to include the custom ids of each Agent in the metadata.

### Acceptance Criteria

- The "getShiftsByFacility" function should be updated to include the custom_id field in its selection.
- The metadata for each shift should include the custom id of the Agent assigned to that shift in addition to their internal id.

### Time/Effort Estimate

1 hour

### Implementation Details

- Update the query in the "getShiftsByFacility" function to join the Agents table and select the custom_id field in addition to the existing metadata.

## Ticket 3: Add a field to update Contact Details

### Description

Add a field to the Facility model to allow for contact details to be saved.

### Acceptance Criteria

- A new column named "contact_details" must be added to the Facility table in the database.
- An API endpoint must be created to allow Facilities to update their contact details.
- The contact details of the Facility should be included in the metadata of the report.

### Time/Effort Estimate

2 hours

### Implementation Details

- Use a database migration to add the "contact_details" field to the Facility table.
- Create a new PUT endpoint in the API for Facilities to update their contact details.
- Include the contact details in the metadata of the report.
