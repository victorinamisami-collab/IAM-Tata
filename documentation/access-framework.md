# Role-Based Access Control (RBAC) Matrix

This matrix defines the high-level access logic approved for the enterprise environment. It serves as the business blueprint for the engineering team to implement in production.


| Job Role | Permitted Actions | Restricted Actions | Business Justification |
| :--- | :--- | :--- | :--- |
| **Cybersecurity Consultant** | Read-only access to system logs, view security configurations. | Modifying network settings, deleting logs, creating new user accounts. | Requires full visibility to audit systems and find risks without altering production environments. |
| **IAM Risk Auditor** | Read access to user permission lists, view compliance reports. | Accessing raw customer data, changing system passwords. | Needs to verify that access controls match corporate policies without seeing sensitive data. |
| **System Administrator** | Full read and write access to infrastructure configurations. | Modifying external audit logs or overriding independent security policies. | Requires high-level access to maintain operations, but must remain subject to independent security logging. |

## Verification and Compliance
Every 90 days, automated or manual access reviews must be conducted against this matrix. Any account possessing permissions outside of these definitions will be automatically flagged for revocation to prevent "privilege creep."

