# rurouni-programmers

# 1. Rurouni Programmers
Repository for the Rurouni Programmers team for the [O'Reilly Fall 2024 Archiectural Kata Challenge](https://learning.oreilly.com/live-events/architectural-katas-fall-2024/0642572006974/)

## Team Members
- David Gethers [LinkedIn]()
- Yong Kim [LinkedIn]()
- Richard Bellamy [LinkedIn]()

## Introduction

### Mission

[Diversity Cyber Council](https://www.diversitycybercouncil.com/) is a 501c3 Non-Profit that
serves under-represented demographics in the tech industry by facilitating education, training,
and staffing opportunities to establish a sustainable and diverse talent pipeline to the workforce.

### Company Information
ClearView is a supplemental HR platform that anonymizes candidate
information while highlighting objective skills and qualifying experience to reduce bias in the
hiring process. Clear View will also be service based, enabling DEI consultants to shadow
employer interviews to rate the interviewer and report findings to executive management in an
effort to proactively and strategically reduce bias in the interview process.

### Users
* Employers - companies invested in providing a more equitable experience to career seekers.
* Job Candidate - professionals seeking a less tedious and more equitable hiring process
  that values their skills and abilities.
* Administrators - Management of the platform, registering users, providing data analytic
  reports on company performance and solution building services with executives.

## Requirements
* The platform must leverage AI to re-construct job seeker resumes into a S.M.A.R.T goal
  format and quantifiable align their experience to open roles posted by the hiring
  manager.
* Similarity Score/Match with job descriptions is a hard requirements.
* AI provided resume tips is a hard requirement.
* AI eliminating any potential racial, lifestyle, cultural, etc. indicators is a hard requirement.
* Back end process data aggregation is a hard requirement.

## Data Points:
* Data Point 1 - Deciding to move forward with a candidate
* Data Point 2 - Unlocking a full candidate profile to offer an interview
* Data Point 3 - 5 question survey to job candidate about interviewer
* Data Point 4 - 5 question survey to interviewer about job candidate
* Data Point 5 - Accumulation of demographic data after rejecting a candidate or
presenting an offer

Monthly data and analytic report presenting KPI metrics as it relates to the interview and hiring
process.

## Architeture characteristics

<img src="images/architecture-characteristics-worksheet.png">
<img src="images/architecture-styles-worksheet-v2.png">

## Choosing the architecture

Non-profit organization with a limited budget, the architecture must be cost effective and scalable.
Simpliicity is key since the non-profit will not have huge staff of software engineers for DEVOPS, support, and development.
Performance is important since the platform will be used by employers, job candidates, and administrators.
Integration

Domain-Based User Interface

There are three distinct user types that will interact with the platform: Employers, Job Candidates, and Administrators.
Each user type will have a unique set of features and functionality that they can access.

<img src="images/domain-based-user-interface.png">

### Storage

Single Relational Database

In order to reduce the coupling between the different services/components there will be logical partitions in the database.
This will take the form of diifferent schemas in the database.

Schemas:
* Common
* Employer
* Job Candidate
* Administrator

Object Storage for Resumes

The reason to store the resumes in object storage is the size of a typical resume will be between 100-300KB for .doc/.docx files, 
200-500KB for pdf files, and if images are embedded 500K to 2-3MB.


Since this architecture only has one quanta the number of services is limited. Anywhere between 4 to 12 sepearately deployed services.
As services become more fine-grained, issues surrounding orchestration and choreography start to appear. Both orchestration and choreography 
are required when multiple services must be coordinated to complete a certain business transaction.

Architectural `quantum` is an independently deployable component with high functional cohesion

### Compute

## Designing the architecture

### Non-Functional Requirements

## Use Cases

## Team Topologies