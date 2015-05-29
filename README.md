# SMS with Zendesk #

When we receive a text:
- search for a ticket for that phone number
- if an open ticket is found, append the text to the ticket
- if not, create a new ticket with the text

Replies to that ticket from an agent would be received by sms by the customer (no email)

How to configure Zendesk:

## 1. Create phone field ##
This field will hold customer's phone number

- Go to settings (bottom-left gear)
- Go to 'Ticket Fields'
- Click 'Add Custom Field'
- Select 'Text'
- Set 'Field Title' to 'Phone'
- Press 'Add Field'

The last thing that needs to be done is to get the field id for our custome field
- From the 'Ticket Fields' list, edit the 'Phone' we just created
- Note the 'Custom Field id' and save for future reference


## 2. Create Targets ##
The targets will be triggered when certain actions are taken in Zendesk ex. Make an API call when a comment is made

- Go to settings (bottom-left gear)
- Go to 'Extensions'
- Click 'Add Target'
- Select 'URL Target'
- Set fields as:
