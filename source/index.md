---
title: Catalyze HIPPA Docs

language_tabs:
  - ""
  - ""
  - ""

toc_footers:
 - ""
---

# Catalyze HIPPA Compliance

Learn how Catalyze not only complies with HIPPA, but builds a better, more secure environment to mitigate your risk. We did the hard work so you don't have to. See how we comply below.

Standards marked with an (R) are *Required*. Standards marked with an (A) are *Addressable*.

# Administrative Safeguards (see [Â§ 164.308](http://www.hhs.gov/ocr/privacy/hipaa/administrative/securityrule/adminsafeguards.pdf))

Taken directly from the wording of the Security Rule, administrative safeguards are â€œadministrative actions, and policies and procedures, to manage the selection, development, implementation, and maintenance of security measures to protect electronic protected health information and to manage the conduct of the covered entityâ€™s workforce in relation to the protection of that information.â€

## Security Management Process - 164.308(a)(1)(i)

```
Catalyze, Inc. has a risk management policy that defines the risk analysis and risk management process in place. Catalyze, Inc. uses NIST800-30 and 800-26 for performing risk analysis.

Policies address risk inherent within the environment and mitigating the risk to an acceptable level on par with the organizations risk posture.

Catalyze has a Sanction Policy that has sanctions for employees not adhering to certain policies.

Policies and procedures address the requirements of monitoring and logging system level events and actions taken by individuals within the environment. All requests into and out of the Catalyze network are logged, as well as all system events using Logstash. Catalyze, Inc. has implemented multiple logging and monitoring solutions to track events within their environment and to monitor for certain types of behavior.
```

Standard | Description
--------- | -----------
Risk Analysis (R)  | Conduct an accurate and thorough assessment of the potential risks and vulnerabilities to the confidentiality, integrity, and availability of electronic PHI held by the covered entity.
Risk Management (R) | Implement security measures sufficient to reduce risks and vulnerabilities to a reasonable and appropriate level to comply with Sec. 164.306(a) [Security standards: General rules; (a) General requirements].
Sanction Policy (R) | Apply appropriate sanctions against workforce members who fail to comply with the security policies and procedures of the covered entity.
Information System Activity Review (R) | Implement procedures to regularly review records of information system activity, such as audit logs, access reports, and security incident tracking reports.

## Assigned Security Responsibility - 164.308(a)(2)

```
Catalyze, Inc. has formally assigned and documented its security officer.
```

Standard | Description
--------- | -----------
Assigned Security Responsibility (R) | Identify the security official who is responsible for the development and implementation of the policies and procedures required by this subpart for the entity.

## Workforce Security - 164.308(a)(3)(i)

```
Catalyze, Inc. has policies in place require individuals requesting access to ePHI submit an authorization form that is signed and acknowledges their responsibility of safeguarding ePHI. The form must also be approved by the supervisor. Once signed and approved, then the individual will be provisioned access to systems deemed business necessary.

Access to ePHI is based on minimum necessary requirements and least privilege.

Catalyze policies discuss the immediate removal of access once an employee has been terminated, with the Security Officer responsible for terminating the access. Once HR initiates the termination process the termination checklist is reference to ensure necessary actions are taken to remove systems and facilities access.
```

Standard | Description
--------- | -----------
Authorization and/or Supervision (A) | Implement procedures for the authorization and/or supervision of workforce members who work with electronic protected health information or in locations where it might be accessed.
Workforce Clearance Procedure (A) | Implement procedures to determine that the access of a workforce member to electronic protected health information is appropriate.
Termination Procedures (A) | Implement procedures for terminating access to electronic protected health information when the employment of a workforce member ends or as required by determinations made as specified in paragraph (a)(3)(ii)(B) [Workforce Clearance Procedures] of this section.



# Section One - HIPAA 164.312(b)
Implement hardware, software, and/or procedural mechanisms that record and examine activity in information systems that contain or use electronic protected health information.

- organization creation / deletion
- user creation / deletion / update
- application creation / deletion / update
- At the application-level, checks include:
- user login
- user logout
- user access data
- user change data
- admin login
- admin view data
- admin change data
- data storage creation / deletion / update

# Section Two - HIPAA 164.312(a)(1)

Implement technical policies and procedures for electronic information systems that maintain electronic protected health information to allow access only to those persons or software programs that have been granted access rights as specified in Ã‚Â§164.308(a)(4).

- Provide multi-factor / level access controls and account validation.
- Phone Number / Voice Call
- SMS / Text Message Validation

# Section Three - HIPAA 164.312(c)(1)

Implement policies and procedures to protect electronic protected health information from improper alteration or destruction.

- Logging information is securely replicated and stored in multiple geo-redundant locations.

# Section Four - HIPAA 164.310(a)(2)(ii)

Implement policies and procedures to safeguard the facility and the equipment therein from unauthorized physical access, tampering, and theft.

- Strictly enforced security incident reporting process.

# Section Five - HIPAA 164.310(a)(1)

Implement policies and procedures to limit physical access to its electronic information systems and the facility or facilities in which they are housed, while ensuring that properly authorized access is allowed.

SAS 70 Physical security for all cloud hardware. Hardware is high availability (99.9+% uptime).

# Section Six - HIPAA 164.312(a)(2)(iv)

Implement a mechanism to encrypt and decrypt electronic protected health information.

- Any data conÃ‚Â­tainÃ‚Â­ing PHI is encrypted at rest.
- Developers maintain full control over their cryptographic keys.
- All data in transit, between apps and catalyze.io, is protected using SSL encryption that supports or exceeds industry standards.

# Kittens

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import 'kittn'

api = Kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Isis",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember Ã¢â‚¬â€ a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import 'kittn'

api = Kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/3"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Isis",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the cat to retrieve