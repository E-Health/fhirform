# FHIRForm Framework

[![FHIRForm](https://raw.github.com/E-Health/fhirform/master/docs/FHIRForm.jpg)](http://canehealth.com)

## About

Structured health data capture is pivotal to the success of any health information system. However, there is no widely accepted standard for the content and presentation of healthcare eForms. FHIRForm is a framework for managing healthcare forms leveraging the HL7 FHIR standard (specifically the Questionnaire resource). FHIRForm framework has several submodules that are separate repositories.

* [Server](https://github.com/dermatologist/fhirform-server). A spring boot adaptation of UHN's HAPI FHIR server with modifications for effective Questionnaire and response handling
* [Editor](https://github.com/E-Health/fred). A FHIR resource editor served by the same server instance. The Editor is a modification of FRED, a project of SMART Health IT, a joint effort of the not-for-profit institutions, Boston Children’s Hospital Computational Health Informatics Program and the Harvard Medical School Department for Biomedical Informatics.
* [Viewer](https://github.com/dermatologist/fhir-questionnaire-render-react) A rendering agent for FHIR Questionnaire using React and Redux that can submit a QuestionnaireResponse.
* [fhirformjs](https://github.com/dermatologist/fhirformjs) An *npm* module for converting Questionnaire items to *JSON schema* for rendering.
* [fhirform-ohdsi](https://github.com/dermatologist/fhirform-ohdsi) Experimental aplication that integrates fhirform with [OMOP CDM](https://ohdsi.org/)

## How to use:

STEP 1: Clone this meta-repository

```
git clone https://github.com/E-Health/fhirform.git
git submodule update --init --recursive
```

STEP 2: Build and install Editor:
```
cd fhirform\editor
mvn clean install

```
STEP 3: Build and install Viewer (optional)

```
cd viewer
npm install
npm build
```
* from the static folder inside build folder, 
copy the file starting with main-xxxx.js to the js folder under server/resources as main.js

STEP 4: Run the server
* from the main project folder
```
./run.sh
```

## How to cite
* To be presented [@ITCH-2019](https://www.uvic.ca/hsd/itch/) (UVic). 

## Demo
[![FHIRForm Demo](https://raw.github.com/E-Health/fhirform/master/docs/fhirform.gif)](http://canehealth.com)

## Contributors

* [Bell Eapen](https://nuchange.ca) | McMaster U
* See also: [:eyes: Drishti | An mHealth sense-plan-act framework!](https://github.com/E-Health/drishti)
