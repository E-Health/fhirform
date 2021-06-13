# FHIRForm Framework

[![FHIRForm](https://raw.github.com/E-Health/fhirform/master/docs/FHIRForm.jpg)](http://canehealth.com)

## About

Structured health data capture is pivotal to the success of any health information system. However, there is no widely accepted standard for the content and presentation of healthcare eForms. FHIRForm is a framework for managing healthcare forms leveraging the HL7 FHIR standard (specifically the Questionnaire resource). FHIRForm framework has several submodules that are separate repositories.

* [Server](https://github.com/dermatologist/fhirform-server). A spring boot adaptation of UHN's HAPI FHIR server with modifications for effective Questionnaire and response handling
* [Editor](https://github.com/E-Health/fred). A FHIR resource editor served by the same server instance. The Editor is a modification of FRED, a project of SMART Health IT, a joint effort of the not-for-profit institutions, Boston Children’s Hospital Computational Health Informatics Program and the Harvard Medical School Department for Biomedical Informatics.
* [Viewer](https://github.com/dermatologist/fhir-questionnaire-render-react) A rendering agent for FHIR Questionnaire using React and Redux that can submit a QuestionnaireResponse.
* [fhirformjs](https://github.com/dermatologist/fhirformjs) An *npm* module for converting Questionnaire items to *JSON schema* for rendering.
* [fhirform-ohdsi](https://github.com/dermatologist/fhirform-ohdsi) Experimental aplication that integrates fhirform with [OMOP CDM](https://ohdsi.org/)

## Docker

Pre-build docker container is available for testing and can be deployed using the following command. Access it at http://localhost/fhir
(Docker container is for testing only.)
```
docker run -d --name fhirform -p 80:8080 beapen/fhirform:240818
```

## How to build:

STEP 1: Clone this meta-repository

```
git clone https://github.com/E-Health/fhirform.git
git submodule update --init --recursive
```

STEP 2: Build and install Editor:
```
cd editor
mvn clean install

```
STEP 3: Build and install Viewer  (IGNORE THIS STEP)
**The viewer is deprecated**
The [new viewer example is here.](https://github.com/dermatologist/fhir-questionnaire-render-react)

```
cd ../viewer
npm install
npm build
```
* from the build/static folder (in viewer),
copy the file starting with main-xxxx.js to the server resources as main.js
Full path: fhirql/src/main/resources/js/main.js

STEP 4: Run the server  (*Server folder has been renamed to fhirql*)
* from the fhirql folder (cd ../fhirql)
```
mvn spring-boot:run -Dmaven.test.skip=true
```

STEP 5: Access the application at http://localhost:8080/fhir/

## How to cite
Eapen BR, Costa A, Archer N, Sartipi K. FHIRForm: An Open-Source Framework for
the Management of Electronic Forms in Healthcare. Stud Health Technol Inform.
2019;257:80-85. PubMed PMID: 30741177.

```
@article{eapen2019fhirform,
  title={FHIRForm: An Open-Source Framework for the Management of Electronic Forms in Healthcare.},
  author={Eapen, BR and Costa, A and Archer, N and Sartipi, K},
  journal={Studies in health technology and informatics},
  volume={257},
  pages={80--85},
  year={2019}
}
```

## Demo
[![FHIRForm Demo](https://raw.github.com/E-Health/fhirform/master/docs/fhirform.gif)](http://canehealth.com)

## Contributors

* [Bell Eapen](https://nuchange.ca) | McMaster U
* See also: [:eyes: Drishti | An mHealth sense-plan-act framework!](https://github.com/E-Health/drishti)
