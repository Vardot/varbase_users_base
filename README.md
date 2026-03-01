# Varbase Users Base

Manages default **Varbase user roles** and **user management configurations**, including role definitions, account settings, and the modules needed to support user management on the site.

## User Roles

Varbase comes with preconfigured default roles tailored for sites with hierarchical content management permissions.

### Super Admin (`administrator`)

Can edit everything in content and configurations for the site.

### Site Admin (`site_admin`)

Can edit, delete, and publish all content on the site.

### SEO Admin (`seo_admin`)

Can edit items related to SEO, Meta tags and Google Analytics.

### Content Admin (`content_admin`)

Can edit all content and publish it but cannot edit anything else not related to the content roles.

### Content editor (`content_editor`)

Has permissions to edit all content on the website but cannot publish any content.

### Authenticated user (`authenticated`)

Any user who can access the website by providing a username or password. This role is provided by default from Drupal and cannot be edited or deleted.

### Anonymous user (`anonymous`)

Any visitor who can access the website without providing a username or password. This role is provided by default from Drupal and cannot be edited or deleted.

## User Management Configurations

This recipe manages the default user account and registration settings needed for a Varbase site, including:

- **Account registration**: Restricted to administrators only by default.
- **Email verification**: Required on registration.
- **Account cancellation**: Defaults to blocking the account.
- **Password reset timeout**: Configurable reset link expiry.
- **Flood control**: IP-based and user-based login attempt limits to protect against brute-force attacks.
- **User notifications**: Email notifications for account activation, password reset, and admin-created accounts.

## Related Recipes

The following Varbase and Drupal CMS recipes extend user management functionality:

- **`drupal_cms_authentication`** — Adds useful authentication tweaks including login by email username, ECA-based user flows, and user picture support.
- **`varbase_security_base`** — Adds security hardening for user accounts including password policy, CAPTCHA, honeypot, antibot, flood control, and username enumeration prevention.
- **`varbase_auth_base`** — Adds Social Single Sign-On support with configurable social authentication providers (e.g. Google).
