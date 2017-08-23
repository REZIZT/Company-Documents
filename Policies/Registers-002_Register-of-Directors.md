# [DRAFT] RZZT Policy Document Registers-002: Register of Directors

This policy document sets out the legislative requirements for maintaining the Register of Directors, and establishes procedures for meeting those requirements. **This policy should be read together with RZZT Policy Document Reg-003: Register of Directors' Residential Addresses.**

## Legislative requirements

The _Companies Act 2006_ (UK) c 46 ('CA2006') requires all companies to maintain a Register of Directors, unless a private company elects to keep this information on a Government-held public register: CA2006 ss 161A, 162(1). RZZT maintains its own register to protect the personal information of its directors.

The Register of Directors _must_ contain (a) the name and any former names of the Director, (b) a service address, (c) the country or state (or part of the United Kingdom) in which the Director is usually resident, (d) the nationality of the Director, (e) the business occupation of the Director (if any), and (f) the Director's date of birth: CA2006 s 163(1). Former names are names used for business purposes within the last 20 years: CA2006 s 163(3)–(4). The service address may be stated to be 'The company's registered office'. Different rules apply for corporate directors and firms: see CA 2006 s 164.

The Register of Directors must be kept available for inspection at the company's registered office: CA2006 s 162(3). This requirement is satisfied if it is maintained in electronic form and accessible from the registered office.

All members have the right to inspect the Register of Directors free of charge, and any other person may inspect it on payment of a fee: CA2006 s 162(5). The Registrar must be notified within 14 days if a person becomes or ceases to be a director, or if any existing director's particulars required to be contained in the Register of Directors has changed: CA2006 s 167(1). The notice to the Registrar must contain a statement of the particulars of the new director that are required to be included in the Company's Register of Directors and be accompanied by a statement by the company that the person has consented to act in that capacity: CA2006 s 167(2).

## Maintaining the Register of Directors

The Company Secretary shall maintain the Register of Directors, including updating the details of Directors as necessary and appropriate.

The Register of Directors shall be kept electronically, in such form as to be available from the Company's registered office, and accessible at all times by the Company Secretary and Directors with the exception of routine maintenance and unplanned outages.

The Company Secretary shall make and keep a current backup copy or copies of the Register (in addition to any other backup copies) which must be accessible to the Company Secretary at least once every five working days.

The Directors may also choose to make and keep backup copies of their own.

## Contents of the Register of Directors

The Register of Directors shall include the following information about each Director as required by law:

- their full forename(s) and surname,
- any former names used in business within the last 20 years,
- their service address,
- their state, region, province, territory or comparable subnational division and country of residence,
- their nationality,
- their business occupation (if any), and
- their date of birth.

The service address shall, by default, be 'The Company's registered office' unless the Director requests otherwise.

The Register of Directors shall also include the following information about each Director:

- their company-provided email address,
- their IRC nickname used for meetings of the company and Directors,
- the date on which they became a Director, and
- the date on which they ceased to be a Director.

## Updating the Register of Directors

The Company Secretary must update the Register of Directors to reflect any changes within five working days of being notified that amendments are required.

The Company Secretary must not remove any person from the Register of Directors, regardless of whether they have ceased to be a Director.

## Requests to inspect and be given a copy of the Register of Directors

Any person may request, in writing, to inspect or be given a copy of the Register of Directors, or part thereof. If the person making such request is a member, no charge shall be imposed. If the person making such request is not a member, a charge may be imposed as determined by the Directors.

The Company Secretary shall comply with a request to inspect or be given a copy of the Register of Directors within five working days. When complying with a request, the Company Secretary shall make ensure that the Register is up-to-date.

## Technical procedure

A Python script has been created to process company registers and create static HTML pages containing the required information. For the Register of Directors, this script processes a CSV file named 'register-of-directors.csv' and creates a file called 'register-of-directors.html'. As a CSV file, it can be edited with standard spreadsheet and text editing software.

### Columns

The Register of Directors CSV file includes the following columns:

- surname
- forenames,
- former_names,
- service_address,
- email,
- irc,
- residence,
- nationality,
- occupation,
- dob,
- appointed, and
- terminated.

Each column corresponds with the information required by this policy. The 'former_names' column should be surrounded by double inverted commas (") and list the names in non-inverted form separated by a comma and a space. The 'service_address' should be 'The Company's registered office', or be in the standard format used in the relevant country (which should always include a postcode) and be surrounded by double inverted commas (") to preserve commas. The 'residence' column should be surrounded by double inverted commas (") to preserve commas. The 'dob', 'appointed' and 'terminated' columns are the dates of birth and the dates the person became and ceased to be a Director respectively, and should be in ISO 8601 extended format (YYYY-MM-DD).