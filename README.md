# FHIRForm Framework - Work in progress

[![QRMine](https://raw.github.com/E-Health/fhirform/master/docs/FHIRForm.jpg)](http://canehealth.com)

## About

Structured health data capture is pivotal to the success of any health information system. However, there is no widely accepted standard for the content and presentation of healthcare eForms. FHIRForm is a framework for managing healthcare forms leveraging the HL7 FHIR standard (specifically the Questionnaire resource). FHIRForm framework has four submodules that are separate projects.

* [Server](https://github.com/dermatologist/fhirform-server). A spring boot adaptation of UHN's HAPI FHIR server with adaptations for effective Questionnaire and response handling
* [Editor](https://github.com/E-Health/fred). A FHIR resource editor served by the same server instance. The Editor is a modification of FRED, a project of SMART Health IT, a joint effort of the not-for-profit institutions, Boston Children’s Hospital Computational Health Informatics Program and the Harvard Medical School Department for Biomedical Informatics.
* [Viewer](https://github.com/dermatologist/fhir-questionnaire-render-react) A rendering agent for FHIR Questionnaire using React and Redux that can submit a QuestionnaireResponse.
* [fhirformjs](https://github.com/dermatologist/fhirformjs) An *npm* module for converting Questionnaire items to *JSON schema* for rendering.

## How to Use

Work in progress

## Contributors

* [Bell Eapen](https://nuchange.ca) | McMaster U
