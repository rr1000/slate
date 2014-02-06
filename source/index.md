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

Learn how Catalyze complies with HIPPA. We did the hard work so you don't have to. See how we comply below.

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

Implement technical policies and procedures for electronic information systems that maintain electronic protected health information to allow access only to those persons or software programs that have been granted access rights as specified in §164.308(a)(4).

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

- Any data con­tain­ing PHI is encrypted at rest.
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
Remember — a happy kitten is an authenticated kitten!
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

