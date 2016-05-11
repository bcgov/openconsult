The following provides the [required](#required), [recommended](#recommended) and [optional](#optional) fields that compose the core openconsult dataset.

### Required

Field                                | DataType | Description
-------------------------------------|----------|------------
ConsultationId                       | TEXT     | A unique ID used internally by the consulting organization to identify this particular consultation. If not such ID exists, one should be generated for publishing purposes.
Title                                | TEXT     | A short-form description of the consultation, preferably under 140 characters.
StatusCurrent <sup>[1](#note1)</sup> | TEXT     | The current status of the consultation.
OrganizationName                     | TEXT     | The name of the organization on who's behalf the consultation is being conducted. For most data publishers this will always be themselves. For agencies that facilitate consultations for multiple organizations it may vary.


<a name="note1">1</a>. `StatusCurrent` is not required if the optional Status changes dataset is provided.

### Recommended
Field                                        | DataType | Description
---------------------------------------------|----------|------------
Description                                  | TEXT     | A detailed description of the consultation.
GeographicScope <sup>[2](#note2)</sup>       | TEXT     | In the area in which the consultation is relevant, e.g. "Vancouver", "British Columbia", "Lower mainland", "Strathcona".
GeographicScopeObject <sup>[2](#note2)</sup> | [GeoJSON](http://geojson.org/geojson-spec.html) | A GeoJSON object representing the location of the application. Points, multi-points, polygons and multi-polygons are all acceptable.

<a name="note2">2</a>. It is acceptable to provide either `GeographicScope` or `GeographicScopeObject`. If both are available both should be provided.

### Optional

Field                  | DataType          | Description
-----------------------|-------------------|------------
StatusCurrentMapped    | TEXT              | The current status of the consultation mapped to one of these standardized values: <ul><li>Planned</li><li>Active</li><li>Completed</li><li>Re-opened</li></ul>
GeographicScopeType    | TEXT              | The nature of the geographic scope in which the consultation is relevant, e.g. "City", "Province", "Region", "Neighbourhood".
PublicEventTitle       | TEXT              | A short-form description of the nature of the public event. If there is more than one public event or channel of engagement use the optional public events dataset instead.
PublicEventStartDate   | TEXT (YYYY-MM-DD) | The date the public event was or will be held. If the event will span multiple days, include the a value in the `PublicEventEndDate` field.
PublicEventEndDate     | TEXT (YYYY-MM-DD) |  The date the public event ended or is planned to end.
PublicEventDescription | TEXT              | A detailed description of the nature of the public event.
PublicEventAddress1    | TEXT              | The street address of the public event, if applicable, or the first line of the address for multi-line addresses.
PublicEventAddress2    | TEXT              | The second line of the address for multi-line addresses.
PublicEventLocality    | TEXT              | The city/town of the address.
PublicEventRegion      | TEXT              | The province/state of the address.
PublicEventLink        | TEXT              | A link to the online component of the public event, if applicable.
PublicEventStartTime   | TEXT (HH:MM)      | The start time of the public event. Use local time zone, or local time with [UTC offset](https://en.wikipedia.org/wiki/ISO_8601#Time_offsets_from_UTC) (hh:mm±hh:mm).
PublicEventEndTime     | TEXT (HH:MM)      | The end time of the public event. Use local time zone, or local time with [UTC offset](https://en.wikipedia.org/wiki/ISO_8601#Time_offsets_from_UTC) (hh:mm±hh:mm).
