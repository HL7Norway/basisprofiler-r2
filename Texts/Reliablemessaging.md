## Reliable messaging

The FHIR MessageHeader can be used in one of two modes, request or response.
-	A requesting message is used to exchange some information to the message receiver
-	A response message is used to report the OperationOutcome of the requesting message
The VKP Hub is expected to respond to any requesting message with the appropriate response reporting the outcome of the request in the message Bundle.

More information about FHIR [messaging](https://www.hl7.org/fhir/messaging.html)
