# [DRAFT] RZZT Policy Document Registers-004: Register of Secretaries

This policy document sets out the legislative requirements for maintaining the Register of Secretaries, and establishes procedures for meeting those requirements.

## Legislative requirements

The _Companies Act 2006_ (UK) c 46 ('CA2006') requires all companies to maintain a Register of Secretaries, unless a private company elects to keep this information on a Government-held public register: CA2006 ss 274A, 275(1). RZZT maintains its own register to protect the personal information of its secretaries.

The Register of Secretaries _must_ contain (a) the name and any former names of the Secretaries, and (b) a service address: CA2006 s 277(1). Former names are names used for business purposes within the last 20 years: CA2006 s 277(3)–(4). The service address may be stated to be 'The company's registered office': s 277(5). Different rules apply for corporate secretaries and firms: see CA 2006 s 278.

The Register of Secretaries must be kept available for inspection at the company's registered office: CA2006 s 277(3). This requirement is satisfied if it is maintained in electronic form and accessible from the registered office. All members have the right to inspect the Register of Directors free of charge, and any other person may inspect it on payment of a fee: CA2006 s 277(5).

## Maintaining the Register of Secretaries

The Company Secretary shall maintain the Register of Secretaries, including updating the details of Secretaries as necessary and appropriate. If the position of Company Secretary is vacated the Directors shall maintain the Register of Secretaries until the position is filled.

The Register of Secretaries shall be kept electronically, in such form as to be available from the Company's registered office, and accessible at all times by the Company Secretary and Directors with the exception of routine maintenance and unplanned outages.

The Company Secretary shall make and keep a current backup copy or copies of the Register (in addition to any other backup copies) which must be accessible to the Company Secretary at least once every five working days.

The Directors may also choose to make and keep backup copies of their own.

## Contents of the Register of Secretaries

The Register of Secretaries shall include the following information about each Secretary as required by law:

- their full forename(s) and surname,
- any former names used in business within the last 20 years, and
- their service address.

The service address shall, by default, be 'The Company's registered office' unless the Secretary requests otherwise.

The Register of Secretaries shall also include the following information about each Secretary:

- their company-provided email address,
- their IRC nickname used for meetings of the company and Directors,
- the date they were appointed, and
- the date they ceased to be a Secretary.

The Company Secretary must update the Register of Secretaries to reflect any changes within five working days of being notified that amendments are required.

The Company Secretary must not remove any person from the Register of Secretaries, regardless of whether they have ceased to be a Secretary.

## Requests to inspect and be given a copy of the Register of Secretaries

Any person may request, in writing, to inspect or be given a copy of the Register of Secretaries, or part thereof. If the person making such request is a member, no charge shall be imposed. If the person making such request is not a member, a charge may be imposed as determined by the Directors.

The Company Secretary shall comply with a request to inspect or be given a copy of the Register of Secretaries within five working days. When complying with a request, the Company Secretary shall ensure that the Register is up-to-date.

## Technical procedure

A Python script has been created to process company registers and create static HTML pages containing the required information. For the Register of Secretaries, this script processes a CSV file named 'register-of-secretaries.csv' and creates a file called 'register-of-secretaries.html'. As a CSV file, it can be edited with standard spreadsheet and text editing software.

### Columns

The Register of Secretaries CSV file includes the following columns:

- surname,
- forenames,
- former_names,
- service_address,
- email,
- irc,
- appointed, and
- terminated.

Each column corresponds with the information required by this policy. The 'former_names' column should be surrounded by double inverted commas (") and list the names in non-inverted form separated by a comma and a space. The 'service_address' should be 'The Company's registered office', or be in the standard format used in the relevant country (which should always include a postcode) and be surrounded by double inverted commas (") to preserve commas. The 'appointed' and 'terminated' columns are the dates the person became and ceased to be a Secretary respectively, and should be in ISO 8601 extended format (YYYY-MM-DD).