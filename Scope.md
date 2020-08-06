# Scope <!-- omit in toc -->

## Table of Contents <!-- omit in toc -->

- [Business Case](#business-case)
- [Scope Management](#scope-management)
- [Requirements Register](#requirements-register)
  - [By RoleRole](#by-rolerole)
  - [By Technicalities](#by-technicalities)
    - [UI](#ui)
- [System Requirements](#system-requirements)

### Business Case

As a Covid 19 tracking measure, customers of 'Gastgewerbe' in Germany have to provide the 'Gastgewerbe' some personal information, such as:

- **phone number**
- **adress**
- **full name**

This is usually carried out with the help of preprinted forms (pen & paper).

This application aims to catapult 'Gastgewerbe' into the information era. By replacing the analog acquisition and management of customer data with digital means, 'Gastgewerbe' managers can save time and money. At the same time, 'Gastgewerbe' customers are going to have a more comfortable experience at the 'Gastgewerbe'.

### Scope Management

Requirements shall be tracked in a table like so:

| ID  | Role     | Domain   | Importance | Description                                                                                                                                                    |
| --- | -------- | -------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 01  | Customer | Security | High       | As customer, I want my personal information to stay undisclosed to everyone at all times, except to health authorities in case of a suspected case of Covid 19 |

The Description should be a user story.

---

4 roles are a given: **Customer**, **Developer**, **Owner** and **User**. By no means is this list complete. New roles may be added at any time.

| Role      | Description                                                                               |
| --------- | ----------------------------------------------------------------------------------------- |
| Customer  | Customer of a 'Gastgewerbe'                                                               |
| Developer | Developer of this app                                                                     |
| Owner     | Manager in charge of a 'Gastgewerbe'                                                      |
| User      | User of the App, usually staff tasked with aquisition of customer data at a 'Gastgewerbe' |

Similarly, this list of domains is incomplete as well. However, assigning each requirement a domain is just a nice to have anyway.

| Domain      | Description                                       |
| ----------- | ------------------------------------------------- |
| Security    | Everything related to protection of customer data |
| Feature     | Regarding a feature the app should provide        |
| Performance | Regarding the performance of a given Feature      |

---

Requirements can be identified, documented and updated continously.

### Requirements Register

Central requirement of the app is to perform 'Kontakterfassung':

> (8) Die Kontaktnachverfolgbarkeit ist sicherzustellen, sofern dies in dieser Verordnung ausdrücklich bestimmt wird (Kontakterfassung). Kontaktdaten (Name, Vorname, Anschrift, Telefonnummer) sind in diesem Fall von dem Betreiber einer Einrichtung oder Veranlasser einer Ansammlung oder sonstigen Zusammenkunft unter Einhaltung der datenschutzrechtlichen Bestimmungen zu erheben und für eine Frist von einem Monat aufzubewahren; nach Ablauf der Aufbewahrungsfrist sind die Daten unverzüglich zu löschen. Sich aus anderen Rechtsvorschriften ergebende Datenaufbewahrungspflichten bleiben unberührt. Das zuständige Gesundheitsamt kann, soweit dies zur Erfüllung seiner nach den Bestimmungen des Infektionsschutzgesetzes (IfSG) und dieser Verordnung obliegenden Aufgaben erforderlich ist, Auskunft über die Kontaktdaten verlangen; die Daten sind unverzüglich zu übermitteln. Eine Verarbeitung der Daten zu anderen Zwecken ist nicht zulässig.

#### By RoleRole

| ID  | Role       | Domain      | Importance | Description                                                                                                                                                                                                      |
| --- | ---------- | ----------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 01  | Customer   | Security    | High       | As customer, use of the app guarantees that my personal information stays undisclosed to everyone at all times, except to health authorities in case of a suspected case of Covid 19                             |
| 02  | Customer   |             | High       | As customer, I want convenient access to 'Gastgewerbe' services.                                                                                                                                                 |
| 03  | Owner      | Feature     | High       | As owner, I want to aquire customer data to be able to operate my business.                                                                                                                                      |
| 04  | Owner      | Feature     | High       | As owner, I want to store customer data to be able to operate my business.                                                                                                                                       |
| 05  | Owner      | Feature     | High       | As owner, I want to export customer data to comply with health authority requests.                                                                                                                               |
| 06  | Owner      | Security    | High       | AS owner, I want to store customer data in a secure and protected manner, to comply with DSVGO                                                                                                                   |
| 07  | Owner      | Security    | High       | As owner, I want customer data to be deleted automatically one month after it was first recorded, to comply with regulations                                                                                     |
| 08  | Owner      | Performance | High       | As owner, I want to provide my customers a convenient way to submit their data, to increase customer satisfaction                                                                                                |
| 09  | User       | Feature     | Medium     | As user, I want to spend minimal effort on collecting customer data                                                                                                                                              |
| 10  | User       | Feature     | High       | As user, I do not want to be responsible for data security                                                                                                                                                       |
| 11  | User       | Feature     | Medium     | As user, I want an easy to operate application to make my job easy                                                                                                                                               |
| 12  | Government | Feature     | Medium     | As government, we want to limit exposure of all people to the coronavirus to contain the spread of Covid 19. E.g. we would like to prevent different people from using the same shared pen or any other surfaces |

#### By Technicalities

##### UI

- record customer data page
- export customer data page

## System Requirements

&nbsp;

#### 1. Non-Functional Requirements

##### 1.1 Product Requirements

&nbsp;

| NFID | Priority| Description |
| --- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------|
| 01 | High | The application should be able to run on all modern iOS and Android devices |
| 02 | Medium | All text should be available both in German and English |
| 03 | High | All customer data will be stored on a SQL Server installed on a Raspberry Pi (or similar device) situated in a secure location within the business premises |

##### 1.2 Security Requirements

&nbsp;

| NFID | Priority| Description |
| --- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------|
| 04 | High | All encryption should be done via RSA or similar assymetric encryption algorithm |
| 05 | High | Once the customer data is transferred to the employee device, it should be immediately and automatically encrypted using the public key of the server device |
| 06 | High | Customer data is only then decrypted with the server device's private key when a health authority has requested an export of customer data regarding a suspected case of CoVID-19 |
| 07 | High | All customer data will be automatically deleted after a period of 30 days in accordance with government regulations |

&nbsp;

#### 2. Functional Requirements
##### 2.1 Requirements for the Customer

&nbsp;

| FID | Priority| Description |
| --- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------|
| 01 | High | A tab called "Customer" should exist on the start page of the application where the user can click in order to be directed to the Customer view of the application |
| 02 | High | A form field should exist on the Customer page to input the following customer information: last name, first name, address, telephone numer and optionally an email address |
| 03 | High | A button should exist at the bottom of the form field where the customer can press to generate a QR code from the provided information |
| 04 | High | Upon generation of the QR code referenced in FID 03, the application opens a new window with the generated QR code in which the QR code can then be scanned |
| 05 | Medium | The customer should have the option to save the QR code for future use by clicking on a Save button on the generated page which contains the QR code, upon clicking the Save button a popup window should appear that contains a form field in which the customer specifies what the QR code should be called |
| 06 | Medium | Saved QR codes should be accessed by a tab on the App Bar called QR Codes |
| 07 | Medium | The QR codes page should contain a list view of all saved QR codes referenced by their saved name |
| 08 | Medium | Upon clicking on the name of the QR code, a new page should appear containing the QR code and a Delete button user to delete outdated QR codes |

&nbsp;

##### 2.2 Requirements for the Employee

&nbsp;

| FID | Priority| Description |
| --- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------|
| 09 | High |  A tab called "Employee" should exist on the start page of the application where the user can click in order to be directed to the Employee view of the application |
| 10 | High | A Register button should exist on the employee page that enables the employee to register their device via their MAC address with the Server device over a WiFi or Bluetooth connection |
| 11 | High | A Scan button should exist on the employee page that enables the employee to scan and read the customer's QR codes |
| 12 | High | The employee should be able to store customer data on their own device until the end of their shift, when they are then able to sync their locally stored customer data to ther server device |
| 13 | High | A Sync button should exist on the employee page that enables the employee to transfer their locally stored customer data to the server device over a WiFi or Bluetooth connection |
| 14 | High | Upon syncing the customer data with the server device, all customer data should be automatically deleted from the employee's device |

&nbsp;

##### 2.3 Requirements for the Server Device

&nbsp;

| FID | Priority| Description |
| --- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------|
| 15 | High | The server device should have WiFi and/or Bluetooth capabilities |
| 16 | High | The server device should be able to generate a key pair for use in assymetric cryptography |
| 17 | High | The server device should be able to host a SQL server for data storage |
| 18 | High | After a succesful registration from a mobile device, the server device should automatically send their public key to the registered device |
| 19 | High | The server device should be able to decrypt customer information and export these when requested |


