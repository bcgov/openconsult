An optional documents dataset is included in the case there is information available regarding documentation relevant to a particular consultation.

### Required

Field          | DataType | Description
---------------|----------|------------
ConsultationId | TEXT     | Provides data link back to core applications information by consultation ID.
DocumentName   | TEXT     | The name of the document, e.g. "Streetscape Drawings".

### Recommended

Field        | DataType | Description
-------------|----------|------------
DocumentLink | TEXT     | A URL link to a publicly-accessible online copy of the document.

### Optional

Field            | DataType | Description
-----------------|----------|------------
Status           | TEXT     | For documents associated with a particular stage in the consultation process, the status name of that stage, e.g. "Review stage". Links document to the status change dataset.
StatusMapped     | TEXT     | For documents associated with a particular stage in the consultation process, the standardized status name of that stage, e.g. "Re-opened". Links document to the status change dataset.
PublicEventTitle | TEXT     | For documents associated with a particular public event, the title of that event, e.g. "Second open house". Links document to the public events dataset.
