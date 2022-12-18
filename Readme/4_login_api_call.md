### Function Description
Login and get tokens

### Api Address 
https://www.invoices.techrad.co.za/api/v1/login

### Payload
to login `{"username":"TestUser","password":"test1234"}`

Create the `username` and `password` via the fusio app [here](https://www.techrad.co.za/apisource/public/apps/fusio/#!/login)

however it's better to use the token (`authorization/token`) so you can revoke it later.

### username
`TestUser`

### password
`test1234`

### Request Method 
- HTTP
- POST

### Headers
| name  |  value | 
| :------------ | :------------ |
|Content-Type|application/json|

### Authentication
| name  |  value | 
| :------------ | :------------ |
|null|Bearer null|

### Request JSON Results Example
```json
//"Content-Type": "application/json"
{
  "method": "POST",
  "transformRequest": [
    null
  ],
  "transformResponse": [
    null
  ],
  "jsonpCallbackParam": "callback",
  "url": "https://www.techrad.co.za/apisource/public/consumer/login",
  "headers": {
    "Content-Type": "application/json",
    "Accept": "application/json, text/plain, */*"
  },
  "data": "{\"username\":\"TestUser\",\"password\":\"test1234\"}",
  "timeout": {}
}
```
### Examples

```bash
curl -X 'POST' \
  'https://ninja.test/api/v1/login?include=clients%2Cinvoices&include_static=include_static%3Dtrue&clear_cache=clear_cache%3Dtrue' \
  -H 'accept: application/json' \
  -H 'X-Api-Secret: password' \
  -H 'X-Api-Token: HcRvs0oCvYbY5g3RzgBZrSBOChCiq8u4AL0ieuFN5gn4wUV14t0clVhfPc5OX99q' \
  -H 'X-Requested-With: XMLHttpRequest' \
  -H 'Content-Type: application/json' \
  -d '{
  "email": "string",
  "password": "1234567"
}'
```

```php

```

### Response Parameter (Output)
| parameter  |  type   | description  | sample value  |
| :------------ | :------------ | :------------ | :------------ |
|  token | string | parameter list  | eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9 |
|  expires_in | int | parameter list  | 1657921976|
|  refresh_token | string | parameter list  | d74d652c7619210351b1-a0578ea1430e9e83f89e439538fa36b7103299d736b5275f-0848942e98|
|  scope | string | parameter list  | backend,backend.account,|

### Response Results Example
```json
{
  "permissions": "[create_invoice]",
  "settings": "The local shop",
  "is_owner": true,
  "is_admin": true,
  "is_locked": true,
  "updated_at": 1231232312321,
  "deleted_at": 12312312321,
  "account": {
    "id": "AS3df3A"
  },
  "company": {
    "id": "WJxbojagwO",
    "size_id": "1",
    "industry_id": "1",
    "slack_webhook_url": "https://slack.com/sh328sj",
    "google_analytics_key": "1",
    "portal_mode": "subdomain",
    "subdomain": "aceme",
    "portal_domain": "https://subdomain.invoicing.co",
    "enabled_tax_rates": 1,
    "fill_products": true,
    "convert_products": true,
    "update_products": true,
    "show_product_details": true,
    "custom_fields": {},
    "enable_product_cost": true,
    "enable_product_quantity": true,
    "default_quantity": true,
    "custom_surcharge_taxes1": true,
    "custom_surcharge_taxes2": true,
    "custom_surcharge_taxes3": true,
    "custom_surcharge_taxes4": true,
    "logo": "logo.png",
    "settings": {
      "timezone_id": "15",
      "date_format_id": "15",
      "military_time": true,
      "language_id": "1",
      "show_currency_code": true,
      "currency_id": true,
      "payment_terms": 1,
      "company_gateway_ids": "1,2,3,4",
      "custom_value1": "Custom Label",
      "custom_value2": "Custom Label",
      "custom_value3": "Custom Label",
      "custom_value4": "Custom Label",
      "default_task_rate": 10,
      "send_reminders": true,
      "enable_client_portal_tasks": true,
      "email_style": "light",
      "reply_to_email": "email@gmail.com",
      "bcc_email": "email@gmail.com, contact@gmail.com",
      "pdf_email_attachment": true,
      "ubl_email_attachment": true,
      "email_style_custom": "<HTML></HTML>",
      "counter_number_applied": "when_sent",
      "quote_number_applied": "when_sent",
      "custom_message_dashboard": "Please pay invoices immediately",
      "custom_message_unpaid_invoice": "Please pay invoices immediately",
      "custom_message_paid_invoice": "Thanks for paying this invoice!",
      "custom_message_unapproved_quote": "Please approve quote",
      "lock_invoices": true,
      "auto_archive_invoice": true,
      "auto_archive_quote": true,
      "auto_convert_quote": true,
      "inclusive_taxes": true,
      "translations": "",
      "task_number_pattern": "{$year}-{$counter}",
      "task_number_counter": 1,
      "reminder_send_time": 32400,
      "expense_number_pattern": "{$year}-{$counter}",
      "expense_number_counter": 1,
      "vendor_number_pattern": "{$year}-{$counter}",
      "vendor_number_counter": 1,
      "ticket_number_pattern": "{$year}-{$counter}",
      "ticket_number_counter": 1,
      "payment_number_pattern": "{$year}-{$counter}",
      "payment_number_counter": 1,
      "invoice_number_pattern": "{$year}-{$counter}",
      "invoice_number_counter": 1,
      "quote_number_pattern": "{$year}-{$counter}",
      "quote_number_counter": 1,
      "client_number_pattern": "{$year}-{$counter}",
      "client_number_counter": 1,
      "credit_number_pattern": "{$year}-{$counter}",
      "credit_number_counter": 1,
      "recurring_invoice_number_prefix": "R",
      "reset_counter_frequency_id": 1,
      "reset_counter_date": "2019-01-01",
      "counter_padding": 1,
      "shared_invoice_quote_counter": true,
      "update_products": true,
      "convert_products": true,
      "fill_products": true,
      "invoice_terms": "Invoice Terms are...",
      "quote_terms": "Quote Terms are...",
      "invoice_taxes": 1,
      "invoice_design_id": "1",
      "quote_design_id": "1",
      "invoice_footer": "1",
      "invoice_labels": "1",
      "tax_rate1": 10,
      "tax_name1": "GST",
      "tax_rate2": 10,
      "tax_name2": "GST",
      "tax_rate3": 10,
      "tax_name3": "GST",
      "payment_type_id": "1",
      "custom_fields": "{}",
      "email_footer": "A default email footer",
      "email_sending_method": "default",
      "gmail_sending_user_id": "F76sd34D",
      "email_subject_invoice": "Your Invoice Subject",
      "email_subject_quote": "Your Quote Subject",
      "email_subject_payment": "Your Payment Subject",
      "email_template_invoice": "<HTML></HTML>",
      "email_template_quote": "<HTML></HTML>",
      "email_template_payment": "<HTML></HTML>",
      "email_subject_reminder1": "<HTML></HTML>",
      "email_subject_reminder2": "<HTML></HTML>",
      "email_subject_reminder3": "<HTML></HTML>",
      "email_subject_reminder_endless": "<HTML></HTML>",
      "email_template_reminder1": "<HTML></HTML>",
      "email_template_reminder2": "<HTML></HTML>",
      "email_template_reminder3": "<HTML></HTML>",
      "email_template_reminder_endless": "<HTML></HTML>",
      "enable_portal_password": true,
      "show_accept_invoice_terms": true,
      "show_accept_quote_terms": true,
      "require_invoice_signature": true,
      "require_quote_signature": true,
      "name": "Acme Co",
      "company_logo": "logo.png",
      "website": "www.acme.com",
      "address1": "Suite 888",
      "address2": "5 Jimbo Way",
      "city": "Sydney",
      "state": "Florisa",
      "postal_code": "90210",
      "phone": "555-213-3948",
      "email": "joe@acme.co",
      "country_id": "1",
      "vat_number": "32 120 377 720",
      "page_size": "A4",
      "font_size": 9,
      "primary_font": "roboto",
      "secondary_font": "roboto",
      "hide_paid_to_date": false,
      "embed_documents": false,
      "all_pages_header": false,
      "all_pages_footer": false,
      "document_email_attachment": false,
      "enable_client_portal_password": false,
      "enable_email_markup": false,
      "enable_client_portal_dashboard": false,
      "enable_client_portal": false,
      "email_template_statement": "template matter",
      "email_subject_statement": "subject matter",
      "signature_on_pdf": false,
      "quote_footer": "the quote footer",
      "email_subject_custom1": "Custom Subject 1",
      "email_subject_custom2": "Custom Subject 2",
      "email_subject_custom3": "Custom Subject 3",
      "email_template_custom1": "<HTML>",
      "email_template_custom2": "<HTML>",
      "email_template_custom3": "<HTML>",
      "enable_reminder1": false,
      "enable_reminder2": false,
      "enable_reminder3": false,
      "num_days_reminder1": 9,
      "num_days_reminder2": 9,
      "num_days_reminder3": 9,
      "schedule_reminder1": "after_invoice_date",
      "schedule_reminder2": "after_invoice_date",
      "schedule_reminder3": "after_invoice_date",
      "late_fee_amount1": 10,
      "late_fee_amount2": 20,
      "late_fee_amount3": 100,
      "endless_reminder_frequency_id": "1",
      "client_online_payment_notification": false,
      "client_manual_payment_notification": false
    }
  },
  "user": {
    "id": "Opnel5aKBz",
    "first_name": "Brad",
    "last_name": "Pitt",
    "email": "brad@pitt.com",
    "phone": "555-1233-23232",
    "signature": "Have a nice day!",
    "avatar": "https://url.to.your/avatar.png",
    "accepted_terms_version": "1.0.1",
    "oauth_user_id": "jkhasdf789as6f675sdf768sdfs",
    "oauth_provider_id": "google"
  },
  "token": {
    "name": "Token Name",
    "token": "AS3df3jUUH765fhfd9KJuidj3JShjA",
    "is_system": true
  }
}
```

---