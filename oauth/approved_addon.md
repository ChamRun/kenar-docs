### الصاق افزونه تایید شده

| CREATE APPROVED ADDON |                     |
|-----------------------|---------------------|
| API Permissions       | ADD_ON_CREATE       |
| OAuth Permissions     | ADDON_USER_APPROVED |

با استفاده از access_token می توانید شماره همراه کاربر احراز شده را دریافت کنید. کافیست رکوئست زیر را بزنید.
```http request
POST https://api.divar.ir/v1/open-platform/users
Content-Type: application/json
x-api-key: {{apikey}}
x-access-token: {{access_token}}

{
    "widgets": {
        "widget_list": [
            {
                "widget_type": "LEGEND_TITLE_ROW",
                "data": {
                    "@type": "type.googleapis.com/widgets.LegendTitleRowData",
                    "title": "کارشناسی دمپایی",
                    "subtitle": "کارشناسی",
                    "has_divider": true,
                    "image_url": "logo"
                }
            }
        ]
    }
}
```

ریسپانس

```json
{
    "id": "123"
}
```