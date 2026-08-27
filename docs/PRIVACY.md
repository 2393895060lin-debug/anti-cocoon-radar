# Privacy and publication boundary

## Keep local

The following must not enter commits or remote repositories:

- Real run logs, search histories and notification bodies.
- Automation memory, chat transcripts and operational histories.
- Real names, personal contact details, account identifiers and machine usernames.
- Absolute local paths, project IDs, automation IDs and connected-account metadata.
- Passwords, tokens, keys, cookies, recovery codes and other authentication material.
- Unpublished client work, private project details and licensed source material.

## Use placeholders

Templates should use neutral markers such as `<USER_DISPLAY_NAME>`, `<WORKSPACE_ROOT>` and `<RECIPIENT>`. Store real values only in ignored local configuration or an approved credential manager.

## Before the first push

1. Review the exact staged file list.
2. Search staged content for names, email addresses, local drive paths, usernames, IDs and secret patterns.
3. Confirm runtime directories and local configuration are ignored.
4. Check repository visibility and destination account.
5. Review commit history as well as the current working tree; deleting a secret from the latest file does not remove it from earlier commits.

An ignore file prevents accidental tracking but is not encryption and does not protect files that were already committed.
