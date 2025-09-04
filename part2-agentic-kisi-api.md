# Kisi Event-Based API

## Event Model Overview

Kisi uses an **event-based** [API](https://api.getkisi.com) model where system activities are published as discrete events. Each event represents a state change and is delivered in a structured JSON payload. These payloads include metadata such as the actor (user or system), the resource involved (door, lock, reader, controler), the timestamp, the organisation and the outcome.  
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

## Integration and use of Kisi API
An event-based API allows for real-time integration of Kisi with external systems and workflows. Each event (door unlock, access denial, user invitation) can be *consumed* via webhooks or API calls. This enables automation, notifications, monitoring, and much more. By linking direct action to resulting events, organizations can connect Kisi with communication platforms, ticketing systems, auditing tools, and custom applications, ensuring that events are integrated into broader operational processes.

### Below are a few examples of how Kisi’s event-based API can be used.
### Slack Notifications
Kisi events can be integrated with Slack to provide real-time alerts. For example, when an access attempt is denied, a webhook can automatically post a message in a designated Slack channel.

### Workflow Automation
Events from Kisi can trigger automated workflows using platforms like Zapier or Microsoft Power Automate. For example, when a door is unlocked, a workflow could log the event in a database, update a CRM record, or notify the facilities team via email.

### Calendar-Based Access
Kisi events can integrate with workplace or scheduling systems (e.g., Google Calendar, OfficeRnD, Robin). For instance, unlocking a meeting room door can be allowed only during a booked time slot, and the system can automatically revoke access when the meeting ends, ensuring secure and efficient space management.
