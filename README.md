# FHIRForm Framework

[![FHIRForm](https://raw.github.com/E-Health/fhirform/master/docs/FHIRForm.jpg)](http://canehealth.com)

## About

Structured health data capture is pivotal to the success of any health information system. However, there is no widely accepted standard for the content and presentation of healthcare eForms. FHIRForm is a framework for managing healthcare forms leveraging the HL7 FHIR standard (specifically the Questionnaire resource). FHIRForm framework has several submodules that are separate repositories.

* [Server](https://github.com/dermatologist/fhirform-server). A spring boot adaptation of UHN's HAPI FHIR server with adaptations for effective Questionnaire and response handling
* [Editor](https://github.com/E-Health/fred). A FHIR resource editor served by the same server instance. The Editor is a modification of FRED, a project of SMART Health IT, a joint effort of the not-for-profit institutions, Boston Children’s Hospital Computational Health Informatics Program and the Harvard Medical School Department for Biomedical Informatics.
* [Viewer](https://github.com/dermatologist/fhir-questionnaire-render-react) A rendering agent for FHIR Questionnaire using React and Redux that can submit a QuestionnaireResponse.
* [fhirformjs](https://github.com/dermatologist/fhirformjs) An *npm* module for converting Questionnaire items to *JSON schema* for rendering.
* [fhirform-ohdsi](https://github.com/dermatologist/fhirform-ohdsi) Experimental aplication that integrates fhirform with [OMOP CDM](https://ohdsi.org/)

## How to cite
* To be presented in [ITCH-2019](https://www.uvic.ca/hsd/itch/). 

## Contributors

* [Bell Eapen](https://nuchange.ca) | McMaster U
