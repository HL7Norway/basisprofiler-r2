# Composition

There is no specific profile for the Composition resource as it adheres to the standard profile defined by HL7. 
Information model for the Composition used in the Message Bundle to document how the response centre resolved an actual event. The information in the Composition is then recorded in the EPR.

<img src="https://git.sarepta.ehelse.no/utvikling/FHIR/raw/master/vkp/ImplementationGuide-definition/images/Composition.png" alt="Drawing" style="width: 100%;max-width: 1200px"/>

## Details

<table class="regular">
  <thead>
  <tr>
    <th>Variable</th>
    <th>Comment</th>
  </tr>
  </thead>
  <tr>
    <td>status</td>
    <td>CompositionStatus according to http://hl7.org/fhir/ValueSet/composition-status</td>
  </tr>
  <tr>
    <td>type.coding</td>
    <td>Uses the LOINC code for Consult note
Example:
<pre><code>
"type":{
   "coding": [
      {
         "code":"11488-4",
         "display":"Consult note"
      }
   ]
}
</pre></code>
</td>
  </tr>
    <tr>
    <td>subject</td>
    <td>Reference to the patient this composition is about
Example: 
<pre><code>"subject":{
   "identifier":{
      "system":"http://ehelse.no/fhir/NamingSystem/FNR",
      "value":"05073500186"
      }
   } </pre></code>
    </td>
  </tr>
  <tr>
    <td>date</td>
    <td>The time the Composition was submitted (i.e. the time of resolution for the MedicationDispense event).
Example: <pre><code> "date":"2017-05-09T10:30:00.936+02:00" </pre></code>
    </td>
  </tr>
  <tr>
    <td>author </td>
    <td>Who authored the Composition.
VKP expects either the author's FNR or HPR-number (HPR: Helsepersonellregisteret, Norwegian central record of Health workers).

System can be: 
<li>http://ehelse.no/fhir/NamingSystem/FNR</li>
<li>http://ehelse.no/fhir/NamingSystem/HPR</li>

Example: 
<pre><code>
"author": [
   {
   "identifier":
      {
      "system":"http://ehelse.no/fhir/NamingSystem/FNR",
      "value":"04056600324"
      },
   "display":"Magnar Koman"
   }
] </pre></code>
 </td>
  </tr>
  <tr>
    <td>title </td>
    <td>Human Readable name/title</td>
  </tr>
  <tr>
    <td>section.text</td>
    <td> 
    Contains the actual Content of the Composition formatted according to FHIR Narrative. Can be XHTML formatted text. 

In the VKP project in Norway the section Narrative is used for two things: 
1.	Response summary: A text describing the resolution of the MedicationDispense event
2.	Signature: Name of author plus a system specific signature identifying the user who submitted the Composition

Example:
<pre><code> 
"section": [
   {
   "title":"Response summary",
   "text":{
      "status":"additional",
      "div":"<xmp><div xmlns="http://www.w3.org/1999/xhtml"> XHTML strukturert tekstinformasjon </div>" </xmp>
      },
   "entry": [
   {
      "reference":"urn:uuid:c31bd880-2b09-4eda-a5a3-90090d49dad5",
      "display":"MedicationDispense"
   }
   ]
   },
   {
      "title":"Signature",
      "text":{
      "status":"additional",
      "div":"<div xmlns="http://www.w3.org/1999/xhtml">
						Magnar Koman (magnark)</div>"
      }
   }
]</pre></code>
See also: {{link:CoreProfilesSTU3/Narrative}}
    </td>
  </tr>
  <tr>
    <td>section.entry</td>
    <td>A reference to data that supports this section. Should be a resolveable reference within the Message Bundle.

Example: 
<pre><code>
"entry": [
   {
   "reference":"urn:uuid:ef91399e-8993-11e7-bb31-be2e44b06b34",
   "display":"MedicationDispense"
   }
]</pre></code>
</td>
  </tr>
</table>


