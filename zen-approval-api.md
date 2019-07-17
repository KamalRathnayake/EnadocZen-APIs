## Enadoc Zen Approval API


**1. Listing Approval Items**

**GET** https://{host}/workspaceapi/api/inboxitems/type/pending?isApproval=true

*Content-Type: application/json*
```javascript
[
{
  "id": 7925,
  "caption": "Approval Inbox Item 1",
  "type": "approval",
  "filterType": "Pending",
  "date": "2019-07-17T09:56:12.017",
  "workflowInstaceId": 12745,
  "taskId": "11376",
  "completedBy": null,
  "submissionId": null,
  "identityValues": "[]",
  "approvalCardValues":[
      {
          "title":"Name",
          "value":"John"
      },
      {
          "title":"Destination",
          "value":"Philippines"
      },
      {
          "title":"Purpose",
          "value":"Training"
      }
  ]
  "approvalCompletionLink":"https://zen.enadoc.com:8080/formsapi/approvals/5f02d250-148a-41cd-8986-1f6e1b42f745"
},
{
  "id": 7926,
  "caption": "Approval Inbox Item 2",
  "type": "approval",
  "filterType": "Pending",
  "date": "2019-07-18T09:56:12.017",
  "workflowInstaceId": 12745,
  "taskId": "11376",
  "completedBy": null,
  "submissionId": null,
  "identityValues": "[]",
  "approvalCardValues":[
      {
          "title":"Name",
          "value":"John"
      },
      {
          "title":"Destination",
          "value":"Philippines"
      },
      {
          "title":"Purpose",
          "value":"Training"
      }
  ]
  "approvalCompletionLink":"https://zen.enadoc.com:8080/formsapi/approvals/bb6c7052-b651-4331-bc97-3fd48056a6a1"
},
...
]

```

**2. Notifying the user approval to Zen**

**POST** https://zen.enadoc.com:8080/formsapi/approvals/bb6c7052-b651-4331-bc97-3fd48056a6a1

*Content-Type: application/json*
```javascript
{
	isApproved:true, 
    comment: "Test Comment"
}
```

