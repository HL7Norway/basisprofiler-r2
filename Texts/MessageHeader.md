# vkp-MessageHeader

Information model for the vkp-MessageHeader FHIR-profile:

<img src="https://git.sarepta.ehelse.no/utvikling/FHIR/raw/master/vkp/ImplementationGuide-definition/images/vkp-MessageHeader.png" alt="Drawing" style="width: 100%;max-width: 1200px"/>

You can find the resource on <https://simplifier.net/Velferdsteknologi2/vkp-MessageHeader-v05>. Notice 
that the path in the URL is exactly the same as the placeholder.

Profile of the MessageHeader resource. Used in the Norwegian Personal Connected Health project to document events from devices user at the patients home. Messages can contain Resources like: 
 - vkp-MedicationDispense - to document MedicationDispense events
 - vkp-Location - to document changes of the Patients geoposition
 - vkp-Flag - to document events that need attention
 - Composition - additional information about handling of a reported event documented by the person handling that event

## Overview
{{tree:Velferdsteknologi2/vkp-MessageHeader-v05}}

## Details
{{dict:Velferdsteknologi2/vkp-MessageHeader-v05:destination}}
