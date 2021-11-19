# no-Patient

Basisprofil for Norwegian Patient information. Defined by The Norwegian Directorate of eHealth. Should be used as a basis for further profiling in use-cases where specific identity information is needed. The basis profile is open, but derived profiles should close down the information elements according to specification relevant to the use-case.

You can find the resource on <https://simplifier.net/Velferdsteknologi2/no-Patient>. 

{{link:Velferdsteknologi2/no-Patient}}

## Points for further discussion
- Should the basis profil close down the identification methods to be used for patients (probably unwise)
- Is there information present that we want to code with norwegian CodeSystems? (gender f.ex)
- Should we propose that nationality is provided as a part of the base-resource in the FHIR spec?

## Extensions used

- Middlename {{link:Velferdsteknologi2/no-middlename}}
- Bydel {{link:Velferdsteknologi2/no-bydel}}
- Nationality {{link:CoreProfilesSTU3/patient-nationality}}

## Profiles used

- Address {{link:Velferdsteknologi2/no-Address-v05}}

## Example

{{link:Velferd-test-og-lek/Patient-example}}

## Profile documentation
{{render:Velferdsteknologi2/no-Patient}}

