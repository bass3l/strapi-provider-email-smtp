# strapi-provider-email-smtp
A third-party SMTP email provider for Strapi, tested with Gmail SMTP.

## Installation
In the root directory of your project, run:

```bash
npm i strapi-provider-email-smtp
```

## Configuration
In your `config/plugins.js`, set the following:

```javascript
module.exports = ({ env }) => ({
  email: {
    provider: 'smtp',
    providerOptions: {
      host: 'smtp.gmail.com', //SMTP Host
      port: 465   , //SMTP Port
      secure: true,
      username: 'my.username@gmail.com',
      password: 'my.password',
      rejectUnauthorized: true,
      requireTLS: true,
      connectionTimeout: 1,
    },
    settings: {
      from: 'my.username@gmail.com',
      replyTo: 'my.username@gmail.com',
    },
  },
});
```

Don't forget to allow 'Less Secure Apps' from account security options, if sending via Gmail.
