# Kurator-Service-iDigBio
A specialized Kurator workflow that interacts with iDigBio API with embedded server that accepts remote requests

A data reader that takes parameters and reads data from iDigBio search API. An embedded jetty server will be started once the workflow is invoked, which will listen to requests at a ceratin port, process the request and push the parameters to the reader that reads data from iDigBio search API. The resulting JSON string will be returned to the user and the user can choose to render it as a spreadsheet.

List of parameters for iDigBio search API:
* limit: number of returning records
* rq: projection parameters

List of parameters for Kuration workflow:
* workflow: workflow to use
* Authority check list to use for SciNameValidator actor
* Tax: toggle taxonomy mode for SciNameValidator actor

Exmaple: "some_host"/?limit=5&authority=GBIF&workflow=DwCa

This repository only contains the code for the workflow file. Please refer to FilteredPush/Kurator repository (https://sourceforge.net/projects/filteredpush/) for the complete code set and more information about data curation workflows.

Note: the termination issue still needs to be solved
