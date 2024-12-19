---
sidebar_position: 6
sidebar_label: API
tags:
   - real-time-update
   - API
---

# Real-time update API

This is the API for managing notifications, receiving new messages and other server events.

**Read more about SSE**:  
- [MDN - Using server-sent events](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events)
- [Stream updates with server-sent events](https://web.dev/articles/eventsource-basics)

## Listen server-sent event

`GET /notifications/watch`

**Response data:**

```json
{
	"type": "NOTIFICATION",
	"data": {
		"title": "bbbbbbbbbbb",
		"content": "aaaaaa",
		"status": "WAITING",
		"priority": "NORMAL",
		"_id": "67640ad50d9b2248416dd499",
		"createdAt": "2024-12-19T12:00:21.053Z",
		"updatedAt": "2024-12-19T12:00:21.053Z",
		"__v": 0,
		"userId": "674fbe152c6b4864bef1f27e",
		"data": {}
	}
}
```

**Explain:**

-  **type:** type of the event which can be **NOTIFICATION** | **MESSAGE**
-  **data:** event data, see the following section for more details

**Event data**

- **title:** title of the event
- **content** basic content
- **status** sending status which can be **SENT** | **FAIL** | **RECEIVED** | **READ** (normally, you shouldn't care about this field)
- **priority** priority of this event, can be **LOW** | **NORMAL** | **HIGH**
- **userId** id of the sender
- **data** an arbitrary object which could be different by the scenario (*I'll update its details later*)
