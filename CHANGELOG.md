# Changelog

## v0.6.9 _(July 22, 2022)_
- Cloudwatch Logs: 
  - Add option to copy all loaded log events to the clipboard (https://github.com/loladotdev/lola/issues/17)
  - Format and highlight JSON in log events (https://github.com/loladotdev/lola/issues/18)
  - Show timestamps in ISO format. Add option to toggle between UTC and local timezone (https://github.com/loladotdev/lola/issues/24)
  - Bugfix for loading log events out of order (https://github.com/loladotdev/lola/issues/23)
- Add keyboard shortcut `Cmd + O` to open the AWS console (https://github.com/loladotdev/lola/issues/19)

## v0.6.8 _(June 10, 2022)_
- Config: Take `$PATH` into account for credential process providers (https://github.com/loladotdev/lola/issues/13)
- Logs: Bugfix that fixes crashes when opening log groups with empty log lines.

## v0.6.7 _(June 3, 2022)_
- DynamoDB: Fixes rich text content parsing (https://github.com/loladotdev/lola/issues/15)

## v0.6.6 _(May 31, 2022)_
- Logs: Fixes old logs not clearing after refresh issue (https://github.com/loladotdev/lola/issues/14)
- Search: Don't show suggestions for deleted resources.
- Tabs: Don't try opening tabs on launch for deleted resources.

## v0.6.5 _(May 11, 2022)_
- DynamoDB: Expand cell view (double click a cell and click expand icon)
- Adds support for assume role providers (https://github.com/loladotdev/lola/issues/1)
- Adds support to [define a redirect URL template](https://github.com/loladotdev/lola/wiki/Settings#custom-url-template) (https://github.com/loladotdev/lola/issues/9) 
- Fix floating filter history bug in Cloudwatch Logs (https://github.com/loladotdev/lola/issues/10)

## v0.6.4 _(Apr 21, 2022)_
- Fix visual bugs in DynamoDB tables with line breaks & spaces.
- Fix visual bugs in search for step functions.
- Adds in-app report a bug link.

## v0.6.1 _(Apr 6, 2022)_
- Search across profiles (https://github.com/loladotdev/lola/issues/4)
- Settings to use default browser (https://github.com/loladotdev/lola/issues/3)

## v0.6.0 _(Apr 4, 2022)_
- News & Promotion screen
- Limit search filter (`/`) to indexed types.

## v0.5.1 _(Apr 1, 2022)_
- DynamoDB view
- Cloudwatch Logs: Add "expand all messages" mode
- Tabs: Add fullscreen mode 

## v0.5.0 _(Mar 15, 2022)_
- Fix horizontal scrolling of Cloudwatch Logs

## v04.1 _(Mar 11, 2022)_
- Added search for [new resource types](https://github.com/loladotdev/lola/projects/1#card-77129223).
- Federated login on AWS Console button click.

## v0.4.0 _(Feb 18, 2022)_
- First developer preview revision.
- Added SSO Support
- Added app update functionality.
