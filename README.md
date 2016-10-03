## The OpenConsult Data Standard

**OpenConsult** is a draft open standard for publishing data about public consultations.  The standard was initiated in December 2015 as a joint project of the Province of British Columbia and PlaceSpeak.com, under the umbrella of the BCDevExchange program.

## Current Version

The current version is `discussion draft 1`.

## Usage
This is a standard that governments, and other organizations that regularly consult with the public, can use to share information about upcoming, ongoing, and completed consultations. This is a standard that citizens' groups, other governments, and businesses can use to create services that recieve data from multiple consulting organizations for re-publication, re-purposing and research.

## Data structure

The OpenConsult standard consists of a core dataset of consistently named and formatted fields (aka columns) with one entry (row) per consultation. Those required fields are described in the [requirements document](Core-applications-dataset-requirements.md), as well as recommended and optional fields that can be published alongside them.

In addition to the core consultations dataset, there are three optional supplementary datasets, providing additional information about public events, documents, and status changes that might be associated with a given consultation. Each of these optional datasets also consists of required, recommended and optional fields. These optional datasets are linked back to the core dataset by the use of a unique consultation ID field.

For example, in the core consultation dataset there could be one (and necessarily only one) consultation with the ID "2016999". Then in the optional documents dataset there could be 4 associated .PDF documents described, each with "2016999" as the value in their respective `ConsultationId` fields.

This data structure has been proposed because

* it provides a relatively easy way for organizations to quickly publish simple but useful data about their consultations
* it provides scope for more ambitious organizations to publish richer and more useful data
* by avoiding data structures that allow for optionally repeated nesting data (as could be expressed e.g. in JSON or XML) and sticking to spreadsheet-like tables with a fixed number of columns, it can be readily published in common open data portals, e.g. CKAN or Socrata.

## Requirements

The standard's requirements are described in these files:

* [Core-consultations-dataset-requirements.md](Core-consultations-dataset-requirements.md)
* [Optional-status-changes-dataset.md](Optional-status-changes-dataset.md)
* [Optional-public-events-dataset-requirements.md](Optional-public-events-dataset-requirements.md)
* [Optional-documents-dataset-requirements.md](Optional-documents-dataset-requirements.md)

Each set of requirements includes fields that are *required*, *recommended*, and *optional* fields:

* **Required**: These essential fields are necessary to have the basic level of data necessary to make this a useful dataset.
* **Recommended**: These fields are highly recommended in order to give the data real-world usability. If these data are available, then they should be submitted.
* **Optional**: These fields provide useful additional information, which may or may not be relevant in the context of a particular consulting organization or a particular consultation. If the data exists, they should be submitted.

Organizations publishing to the standard are free to publish any additional fields alongside those described in this standard, so long as those fields are clearly not covered by one of the fields described in the standard. Organizations doing so are encouraged to submit those fields as candidates for inclusion.

## Sample Data

Sample Data is provided in the `SampleData` folder demonstrating how real-world data (derived from EngageBC and PlaceSpeak.com) could be formatted to fit the standard. Note that not all fields are required, so not all data being published to the standard will have a structure identical to this sample.

## Examples

[PlaceSpeak.com](https://www.placespeak.com) provides a feed machine-readable feed of all of their public consultations, formatted in JSON and structured according to the draft **openconsult** standard.

The feed is located at [https://www.placespeak.com/api/consultations/](https://www.placespeak.com/api/consultations/).

It currently implements the "core" dataset requirements.

## Project Status
Initial draft for discussion being shared, feedback being collected on the basic structure of the dataset, as well as on the field details.

## Getting Help or Reporting an Issue
If you have opinions about the standard please [submit an issue](https://github.com/bcgov/openconsult/issues) here, or get in touch at <hugh@placespeak.com> | <justin.hewitt@gov.bc.ca>.

## License

Detailed guidance around licenses is available [here](https://github.com/bcgov/BC-Policy-Framework-For-GitHub/blob/master/BC-Open-Source-Development-Employee-Guide/Licenses.md)
   
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons Licence" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/80x15.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">OpenConsult</span> by <span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">the Province of Britich Columbia</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
