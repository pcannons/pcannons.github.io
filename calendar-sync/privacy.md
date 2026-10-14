# Privacy policy

Sophia Calendar Sync is a personal desktop utility operated by Philipp Cannons. Effective October 13, 2026.

## Access and use

The utility requests Google Drive read-only access to read its configured deadline spreadsheet and syllabus file metadata. Google authorizes this scope across accessible Drive files, but the utility reads only the configured sources. It requests access to events on Google Calendars owned by the authorizing account so it can maintain a dedicated mirror calendar. It also reads selected Apple Calendar events through macOS Calendar permission.

Source dates, event titles, descriptions, locations, course information and source identifiers are used to construct and reconcile mirrored events. Grading interpretations included in event descriptions are derived from the configured course materials. Source attendee lists are not copied, and the utility does not invite guests or generate conferencing links.

## Storage and sharing

Source snapshots, reconciliation records, logs and event IDs are stored locally on the owner's Mac. OAuth credentials are stored locally by the Google Workspace CLI using its encrypted credential store. Mirrored events are sent to the owner's dedicated Google Calendar with private visibility. Calendar sharing configured by the owner still governs access.

The utility does not sell user data, use it for advertising, or send it to a separate application server. This documentation website does not receive calendar data or credentials. The owner may use local records and connected assistant tools to operate and troubleshoot the integration.

## Control and deletion

The owner can stop the local scheduled job, revoke the application's access through Google Account settings, remove local credential and snapshot files, and delete mirrored events or the destination calendar through Google Calendar. Source calendars and source files are not modified by the sync. Local records remain until the owner removes them.

Sophia Calendar Sync's use and transfer of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

Questions: [philipp.cannons@gmail.com](mailto:philipp.cannons@gmail.com). [App homepage](README.md).
