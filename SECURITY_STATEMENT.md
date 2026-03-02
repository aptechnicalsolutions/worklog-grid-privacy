# WorkLog Grid for Jira — Security Statement

**Last updated:** [Insert Date]

AP Technical Solutions LLC (“we”) provides the WorkLog Grid for Jira application (the “App”). This Security Statement describes how the App handles data and relies on Atlassian’s infrastructure for security.

---

## Infrastructure and hosting

- The App is built on **Atlassian Forge** and runs entirely on **Atlassian’s cloud infrastructure**.
- We do not operate our own servers or host any part of the App outside Atlassian’s environment.
- All compute, storage, and network security are managed by Atlassian as part of the Forge platform.

---

## Data handling

- The App **accesses only the data it needs** to provide its functionality: Jira issue metadata, worklogs, user information, and project data, via **Atlassian’s official APIs** and the permissions granted at installation.
- The App **does not transmit customer data to systems outside Atlassian**. All processing occurs within the Atlassian cloud environment.
- Any stored data (user preferences and short-lived cache) is held in **Atlassian Forge key-value storage**, which is part of Atlassian’s hosted environment and subject to Atlassian’s security and compliance practices.

---

## Authentication and access

- **Authentication and authorization** are handled by Atlassian. The App uses the Forge platform’s identity and permission model; we do not implement our own authentication or store credentials.
- The App respects **Jira permissions**: users see only the data they are allowed to access in Jira (e.g. worklogs for issues they can view).

---

## Secure development

- We follow **secure development practices** and do not use Basic authentication or store shared secrets in a way that would expose customer installations.
- The App does not load or execute code from third-party or external hosts at runtime.

---

## Updates and vulnerabilities

- We release updates through the Atlassian Marketplace and Forge deployment process.
- If we become aware of a **security issue** that affects the App, we will address it in line with responsible disclosure and, where appropriate, coordinate with Atlassian’s security processes.

---

## Contact

For security-related questions or to report a concern:

**AP Technical Solutions LLC**  
Email: aptechnicalsolutionsllc@gmail.com

For general data practices, see our [Privacy Policy](../PRIVACY_POLICY.md).
