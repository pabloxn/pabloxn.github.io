---
description: Data items
---

# Data Dictionary

### Report data items

| Data Item | Description | Type | Example | Field Name |
| :--- | :--- | :--- | :--- | :--- |
| Title | Formal title | Text | Mr / Mrs / Ms | {client.title} |
| Claimant Forename | Claimant's Given name | Text | Paul | {client.firstName} |
| Claimant Surname | Claimant's Family name | Text | Newns | {client.lastName} |
| Claimant Name | Claimant's full name | Text | Mr Paul Newns | {client.fullName} |
| Claimant Address | Claimant's home address | Text | 1 The Street, Town | {client.address} |
| Claimant Email | Claimant's Email Address | Text | person@provider.com | {client.email} |
| Claimant Mobile | Claimants Mobile No. | Text | 07123456789 | {client.mobile} |
| Claimant DoB | Claimant's Date of Birth | Date | 01/02/73 | {client.dob} |
| Claimant Age | Claimant's Age | Text | 45 years | {client.age} |
| Claimant Sex | Sex | Code | Male / Female | {client.gender} |
| Claimant Occupation | Occupation | Text | Builder | {client.occupation} |
| Clinic Name | Clinic Name | Text | Clinic 1 | {clinic.name} |
| Clinic City | Clinic City | Text | Cambridge | {clinic.city} |
| Clinic Address | Clinic Address / Interview address | Text | 1 The High Street, Town | {clinic.address} |
| Case Title | Case Title | Text | RTA Motorcycle | {case.title} |
| Incident Date | Date of incident | Date | 02/03/18 | {case.incidentDate} |
| Claimant Age at incident | The Claimants Age at the incident date | Text | 42 Years | {case.clientAge} |
| Instructing Party Name | Solicitor or intermediate - payer | Text | A Company | {case.ip} |
| Solicitor Name | Solicitor | Text | A Company | {case.solicitor} |
| Our Ref | InClinic reference | Text | KN190089 | {case.ourRef} |
| Payer Ref | Payer/Referrer Reference | Text | dd-13440/3 | {case.payerRef} |
| Solicitor Ref | Solicitor Reference | Text | SC/8783782/m | {case.solicitorRef} |
| Diagnosis | Claimants Diagnosis | Text | Phobia | {case.diagnosis} |
| Diagnostic Code | Claimants Diagnostic Code | Text | D7K | {case.diagCode} |
| Diagnostic Description | Claimants Diagnosis description | Text | Phobia is defined... | {case.diagDesc} |
| Incident Description | Incident Description | Text | It was a terrible... | {case.incidentDesc} |
| Injuries | Injuries from incident | Text | broken leg | {case.injuries} |
| Initial GAD7 | Initial GAD7 score | Text | 7 | {case.gad7} |
| Initial PHQ9 | Initial PHQ9 score | Text | 12 | {case.phq9} |
| Initial Pain Catastrophe Scale | Initial Pain Catastrophe Scale score | Text | 21 | {case.painCatScale} |
| Interview Date | Date of attended appointment | Date | 04/05/19 | {appointment.date} |
| Interview Time | Appointment Time | Time | 13:30 | {appointment.time} |
| Arrive Time | Appointment recommended arrival time | Time | 13:15 | {appointment.arriveTime} |
| Interview Duration | Appointment Duration | Minutes | 45 | {appointment.duration} |
| Age at Interview | The claimants age at the interview date | Text | 41 Years | {client.ageAtAppt} |
| Psychologist | Report author | Text | Dr Crazy Mann | {clinician.name} |

### pipes

You can manipulate certain fields with a pipe \|. A pipe sits in the the curly brackets after the field name. The pipe name is then added.

{fieldName\|pipeName}

e.g. {case.clientAge\|dateLong}

#### strings

Manipulates a string

|  | Description | example |  |
| :--- | :--- | :--- | :--- |
| capitalise | Changes the first character to uppercase | {client.pronouns.himher\|capitalise} | Her |

#### dates

format dates

| Pipe | Description | example |  |
| :--- | :--- | :--- | :--- |
| dateShort | This is the default format | {client.dob} or {client.dob\|dateShort} | 01/02/73 |
| dateMedium | This is a short text version of the date | {client.dob\|dateMedium} | 1 Feb 1973 |
| dateLong | This long text version of the date | {client.dob\|dateLong} | 1 February 1973 |

#### time

format time

| Pipe | Description | example |  |
| :--- | :--- | :--- | :--- |
| time24 | This is the default format | {appointment.time} or {appointment.time\|time24} | 13:30 |
| time12 | This is time with am/pm | {appointment.time\|time12} | 1:30 pm |

### generic items

| Data item | Description | Db name |
| :--- | :--- | :--- |
| his/her | gender specific entry | {client.pronouns.hisher} |
| him/her |  | {client.pronouns.himher} |
| he/she |  | {client.pronouns.heshe} |
| himself/herself |  | {client.pronouns.himher}self |
| parent | father/mother | {client.pronouns.parent} |
| report date | today's date | {today} |

### Stats

| Data Item | Descritpion | Db name |
| :--- | :--- | :--- |
| Client DNA Total | Clients Did Not Attend total | {client.stats.dnaTotal} |

### Items not currently in database

| Data Item | Description | Type | Example |
| :--- | :--- | :--- | :--- |
| Expert name | Medical or GP report writer | Text | Mr Wright |
| Pre-Driving Anxiety | Pre-incident driving anxiety score | Numerical | 2 |
| Post-Driving Anxiety | Post-incident driving anxiety score | Numerical | 6 |
| Pre-Passenger Anxiety | Pre-incident passenger anxiety score | Numerical  | 1 |
| Post-Passenger Anxiety | Post-incident passenger anxiety score | Numerical  | 7 |
| Pre-Mood Level | Pre-incident mood level score | Numerical | 4 |
| Post-Mood Level | Post-incident mood level score | Numerical | 6 |
| Reports | medical / GP / Hospital / Therapy / 1st |  |  |

