An optional status changes dataset is included in case there is detailed information available about the historical and/or future lifecycle of the consultation. This information can replace or supplement the `StatusCurrent` field in the core dataset.

[Required](#required), [recommended](#recommended) and [optional](#optional) fields are provided.

### Required

Field          | DataType          | Description
---------------|-------------------|------------
ConsultationId | TEXT              | Provides data link back to core applications information by consultation ID.
Status         | TEXT              | A short-form description of the status.
StatusDate     | TEXT (YYYY-MM-DD) | Indicates the date at which this status became applicable to this consultation, or the date at which it is planned to become applicable.

### Recommended

Field          | DataType | Description
---------------|----------|------------
StatusMapped   | TEXT     | Status mapped to one of these standardized values:  <ul><li>Planned</li><li>Active</li><li>Completed</li><li>Re-opened</li></ul>

### Optional

Field             | DataType | Description
------------------|----------|------------
StatusDescription | TEXT     | A detailed description of current status.
