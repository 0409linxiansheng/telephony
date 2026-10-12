### Telephony

Telephony for Frappe apps. Adds Exotel & Twilio integration in any Frappe app.

---

### Installation

本仓库是 [frappe/telephony](https://github.com/frappe/telephony) 的个人镜像分支，内容与上游
`develop` 保持一致，未做功能改动。

You can install this app using the [bench](https://github.com/frappe/bench) CLI:

```bash
cd $PATH_TO_YOUR_BENCH
bench get-app https://github.com/0409linxiansheng/telephony --branch develop
bench install-app telephony
```

> 仓库名 `telephony` 与本 app 名一致，`bench get-app` 会克隆到 `apps/telephony`，
> 所以 `bench install-app telephony` 可以直接执行，不需要额外步骤。
> 默认分支就是 `develop`，因此 `--branch develop` 也可以省略。

---

### Configuration

#### Doctypes

##### TP Twilio Settings

This stores configuration settings for integrating with Twilio provider, including API credentials such as Account SID and Auth Token, Secret, options to enable the integration and record calls.

##### TP Exotel Settings

This holds settings for Exotel provider, such as Account SID, Subdomain, Webhook Verify Token, API Key, API Token, and flags to enable the service and record outgoing calls.

##### TP Call Log

This records details of all telephony calls made through the app, including call ID, from/to numbers, status, duration, type (incoming/outgoing), timestamps, recording URL, and links field for linking calls to related documents.

##### TP Telephony Agent

This defines agents who can make and receive calls, this handles settings like linking to user accounts, mobile numbers, default medium, and specific numbers/devices for each provider.

#### Webhooks and APIs

Webhooks and API configuration for Telephony app will be found in the respective app's documentation that uses this app.

---

### Twilio Setup

https://docs.frappe.io/helpdesk/twilio

### Exotel Setup

https://docs.frappe.io/helpdesk/exotel

---

### Contributing

This app uses `pre-commit` for code formatting and linting. Please [install pre-commit](https://pre-commit.com/#installation) and enable it for this repository:

```bash
cd apps/telephony
pre-commit install
```

Pre-commit is configured to use the following tools for checking and formatting your code:

- ruff
- eslint
- prettier
- pyupgrade

---

### License

agpl-3.0
