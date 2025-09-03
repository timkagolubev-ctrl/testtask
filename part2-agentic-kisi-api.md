# Kisi Event-Based API

## Event Model Overview

Kisi uses an **event-based** [API](https://docs.kisi.io/platform/apis) model where system activities are published as discrete events. Each event represents a state change and is delivered in a structured JSON payload. These payloads include metadata such as the actor (user or system), the resource involved (door, lock, reader, controler), the timestamp, the organisation and the outcome.  
An example of a JSON payload can be seen below:
```json
{
  "uuid": "d7cf3333-a492-4e5d-b20-as45fg4334f",
  "actor_type": "string",
  "actor_id": 1804,
  "actor_name": "John Johnson",
  "object_type": "Lock",
  "object_id": 2006,
  "object_name": "Entrance door",
  "organization_id": 18,
  "place_id": 46,
  "success": true,
  "type": "lock.unlock",
  "error_code": null,
  "error_message": null,
  "created_at": "2025-09-03T21:29:00Z"
}
```
Examples of events can include an unlocking of the door, a denial of access or an addition of a new user's credentials to the system.  

