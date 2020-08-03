# Scope <!-- omit in toc -->

## Table of Contents <!-- omit in toc -->

- [Business Case](#business-case)
- [Scope Management](#scope-management)
- [Requirements Register](#requirements-register)
  - [By RoleRole](#by-rolerole)
  - [By Technicalities](#by-technicalities)
    - [UI](#ui)

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

| ID  | Role     | Domain      | Importance | Description                                                                                                                                                                          |
| --- | -------- | ----------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 01  | Customer | Security    | High       | As customer, use of the app guarantees that my personal information stays undisclosed to everyone at all times, except to health authorities in case of a suspected case of Covid 19 |
| 02  | Customer |             | High       | As customer, I want convenient access to 'Gastgewerbe' services.                                                                                                                     |
| 03  | Owner    | Feature     | High       | As owner, I want to aquire customer data to be able to operate my business.                                                                                                          |
| 04  | Owner    | Feature     | High       | As owner, I want to store customer data to be able to operate my business.                                                                                                           |
| 05  | Owner    | Feature     | High       | As owner, I want to export customer data to comply with health authority requests.                                                                                                   |
| 06  | Owner    | Security    | High       | AS owner, I want to store customer data in a secure and protected manner, to comply with DSVGO                                                                                       |
| 07  | Owner    | Security    | High       | As owner, I want customer data to be deleted automatically one month after it was first recorded, to comply with regulations                                                         |
| 08  | Owner    | Performance | High       | As owner, I want to provide my customers a convenient way to submit their data, to increase customer satisfaction                                                                    |
| 09  | User     | Feature     | Medium     | As user, I want to spend minimal effort on collecting customer data                                                                                                                  |
| 10  | User     | Feature     | High       | As user, I do not want to be responsible for data security                                                                                                                           |
| 11  | User     | Feature     | Medium     | As user, I want an easy to operate application to make my job easy                                                                                                                   |

#### By Technicalities

##### UI

- record customer data page
- export customer data page