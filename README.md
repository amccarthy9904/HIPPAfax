# HIPPAfax



### Ring Central
30$ per month, or 25$ * 12 for 1 year
unlimited faxes, one line
additional line 5$ per month
(ring Central API)[https://developers.ringcentral.com/api-reference/Fax/createFaxMessage]

### Twilio fax service in AWS:
https://www.twilio.com/en-us/blog/reliable-fax-pipeline-twilio-aws-expand-access-ballot-box
twilio is no longer offering this service

### Documo
offers API
curl --location 'https://api.documo.com/v1/me' --header 'Authorization: Basic eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI1M2JmNzhmZC1iMjFlLTQ3ODMtODNmZS0yMDgyY2I5MGQyNDMiLCJhY2NvdW50SWQiOiI5MTZlMjVmMS0xYzU4LTRmMjEtYTI0OC0yMWYzZGY1Mjk0YjkiLCJpYXQiOjE3MTIxNzYxOTl9.4a4IqT4DZUojy4cCmcLtktSDfpo1cyqivh5NWICAqCM'

curl --location 'https://api.documo.com/api-keys' --header 'Authorization: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI1M2JmNzhmZC1iMjFlLTQ3ODMtODNmZS0yMDgyY2I5MGQyNDMiLCJhY2NvdW50SWQiOiI5MTZlMjVmMS0xYzU4LTRmMjEtYTI0OC0yMWYzZGY1Mjk0YjkiLCJpYXQiOjE3MTIxNzUwNTB9.ETmNgY8Yv7XlAkW9Hdng70g8bW5eIZZioE_IVLKzcEs'

curl --location 'https://api.documo.com/v1/users/d1077489-5ea1-4db1-9760-853f175e8288' --header 'Authorization:eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI1M2JmNzhmZC1iMjFlLTQ3ODMtODNmZS0yMDgyY2I5MGQyNDMiLCJhY2NvdW50SWQiOiI5MTZlMjVmMS0xYzU4LTRmMjEtYTI0OC0yMWYzZGY1Mjk0YjkiLCJpYXQiOjE3MTIxNzM4MTR9.ce0kxpBXEk8Lol8mFPcTCD25fvPxaJ_dsFi1qcJWDE4'

curl --location 'https://api.documo.com/files' --header 'Authorization: Basic eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI1M2JmNzhmZC1iMjFlLTQ3ODMtODNmZS0yMDgyY2I5MGQyNDMiLCJhY2NvdW50SWQiOiI5MTZlMjVmMS0xYzU4LTRmMjEtYTI0OC0yMWYzZGY1Mjk0YjkiLCJpYXQiOjE3MTIxNzYxOTl9.4a4IqT4DZUojy4cCmcLtktSDfpo1cyqivh5NWICAqCM' --form 'files=@dummy.pdf'

curl --location 'https://api.documo.com/v1/faxes' \
--header 'Authorization: Basic eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOiI1M2JmNzhmZC1iMjFlLTQ3ODMtODNmZS0yMDgyY2I5MGQyNDMiLCJhY2NvdW50SWQiOiI5MTZlMjVmMS0xYzU4LTRmMjEtYTI0OC0yMWYzZGY1Mjk0YjkiLCJpYXQiOjE3MTIxNzYxOTl9.4a4IqT4DZUojy4cCmcLtktSDfpo1cyqivh5NWICAqCM'' \
--header 'Content-Type: multipart/form-data' \
--form 'faxNumber="11234567890"' \
--form 'attachments=@"/Users/File1.pdf"' \
--form 'attachments=@"/Users/File2.pdf"' \
--form 'coverPage="false"' \
--form 'coverPageId="d1077489-5ea1-4db1-9760-853f175e8288"' \
--form 'tags="example"' \
--form 'recipientName="example"' \
--form 'senderName="example"' \
--form 'subject="example"' \
--form 'callerId="example"' \
--form 'notes="example"' \
--form 'cf="{\"example\": \"value\"}"' \
--form 'scheduledDate="2020-01-01T00:00:00.000Z"' \
--form 'webhookId="d1077489-5ea1-4db1-9760-853f175e8288"'

### [HylaFax](https://www.hylafax.org/)
opensource fax software
many free products biult on top
[avantfax](https://sourceforge.net/projects/avantfax/)

### [HIPPA Fax compliance guide](https://hipaafaxguide.com/hipaa-fax-compliance-guide/)
[encrpytion standard](https://www.hhs.gov/hipaa/for-professionals/breach-notification/guidance/index.html)
[encryption doc](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-111.pdf)


### [webhook testing site](https://webhook.site/#!/view/af6dbe5d-e02a-4974-b0da-182711cae263/6fa30794-355c-4cbd-bc87-bcecc1923f32/1)
The media on which the PHI is stored or recorded has been destroyed in one of the following ways:
Paper, film, or other hard copy media have been shredded or destroyed such that the PHI cannot be read or otherwise cannot be reconstructed. Redaction is specifically excluded as a means of data destruction.
Electronic media have been cleared, purged, or destroyed consistent with NIST Special Publication 800-88, Guidelines for Media Sanitization such that the PHI cannot be retrieved.

pay per loggin
2fa
slick front end
archived after 30 days
cheapest storeage
30$-50$ per month

in email
fax to a phone number
we recieve the email, forward it to destination
api integration send an email