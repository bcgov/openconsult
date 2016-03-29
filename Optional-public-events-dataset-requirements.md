EventAn optional public meetings dataset is included in case there is more than one channel or opportunity for public engagement with regards to a particular consultation project. This can include past or scheduled events.

### Required

Field                | DataType          | Description
---------------------|-------------------|------------
ConsultationId       | TEXT              | Provides data link back to core applications information by application ID.
PublicEventStartDate | TEXT (YYYY-MM-DD) | The date the public event was or will be held. If the event will span multiple days, include a value in the `PublicEventEndDate` field.
PublicEventTitle     | TEXT              | A short-form description of the nature of the public event.

### Optional

Field                  | DataType          | Description
-----------------------|-------------------|------------
PublicEventDescription | TEXT              | A detailed description of the nature of the public event.
PublicEventAddress1    | TEXT              | The street address of the public event, if applicable, or the first line of the address for multi-line addresses.
PublicEventAddress2    | TEXT              | The second line of the address for multi-line addresses.
PublicEventCity        | TEXT              | The city of the address.
PublicEventState       | TEXT              | The province or state of the address.
PublicEventLink        | TEXT              | A link to the online component of the public event, if applicable.
PublicEventEndDate     | TEXT (YYYY-MM-DD) |  The date the public event ended or is planned to end.
PublicEventStartTime   | TEXT (HH:MM)      | The start time of the public event. Use local time zone, or local time with [UTC offset](https://en.wikipedia.org/wiki/ISO_8601#Time_offsets_from_UTC) (hh:mm±hh:mm).
PublicEventEndTime     | TEXT (HH:MM)      | The end time of the public event. Use local time zone, or local time with [UTC offset](https://en.wikipedia.org/wiki/ISO_8601#Time_offsets_from_UTC) (hh:mm±hh:mm).
