# Data model "Hendelse"

## Overview of the use-case scenarios

### Oslo Kommune via VKP

<img src="https://git.sarepta.ehelse.no/utvikling/FHIR/raw/master/vkp/ImplementationGuide-definition/images/overview-Oslo.png" alt="Drawing" style="width: 100%;max-width: 1200px"/>

## Hendelse (a VKP Event)

The message sent from the Medication Dispenser service provider to VKP over the I1 interface contains a FHIR bundle with the following FHIR resources. Used to document an event registered in the patients home.
- MessageHeader (no specific profile, but certain parameters are expected)
- MedicationDispense (according to the vkp-MedicationDispense-v05 profile)
- Composition (no specific profile, but a certain format is expected)
- Flag (according to the vkp-Flag-v05 profile)
- Location (according to the vkp-Location-v05 profile)

Only the MessageHeader and MedicationDispense resources are mandatory in the bundle, and the other resources are included only if they are relevant and contain information. 

<img src="https://git.sarepta.ehelse.no/utvikling/FHIR/raw/master/vkp/ImplementationGuide-definition/images/FHIR VKP - hendelse.png" alt="Drawing" style="width: 100%;max-width: 1200px"/>

## Index

{{index:root}}