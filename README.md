# react-intl-snippets README

This extension is a collection of snippets which work with [formatJS's React Intl package](https://formatjs.io/)

## Installation

### Quick Launch

Open _Quick Open_:

- [_Linux_](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf): `Ctrl+P`
- [_macOS_](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf): `⌘P`
- [_Windows_](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf): `Ctrl+P`

Paste the following command and press Enter:

```bash
ext install
```

### Extension Manager

Open the extension manager with ctrl+shift+X (Win/Linux) or cmd+shift+X (macOS), search for `sdfsdfs` and click on the ` [Install``] ` button.

Marketplace

## Features

Describe specific features of your extension including screenshots of your extension in action. Image paths are relative to this README file.

For example, if there is an image subfolder under your extension project workspace:

\!\[feature X\]\(images/feature-x.png\)

> Tip: Many popular extensions utilize animations. This is an excellent way to show off your extension! We recommend short, focused animations that are easy to follow.

## Syntax

### key

m = message
i = useIntl
d = date
dp = date parts
t = time
tp = time parts
dtr = date time range
n = number
np = number parts
p = plural
l = list
lp = list parts
dn= display name

I will be using the above abbreviations in the code and always in the order shown above

### Imports

`intimp` will prefix all the import statements

| prefix    | Code                                      |
| --------- | ------------------------------------------------ |
| `intimpm` | `import { FormattedMessage } from 'react-intl';` |
| `intimpmd` | `import { FormattedMessage, useIntl } from 'react-intl';` |
| `intimpmd` | `import { FormattedMessage, FormattedDate } from 'react-intl';` |
| `intimpmid`  | `import { FormattedMessage, useIntl, FormattedDate } from 'react-intl';` |
| `intimpdp` | `import { FormattedDateParts } from 'react-intl';` |
| `intimpmdp` | `import { FormattedMessage, FormattedDateParts } from 'react-intl';` |
| `intimpmidp` | `import { FormattedMessage, FormattedDateParts } from 'react-intl';` |
| `intimpmidp` | `import { FormattedMessage, FormattedDate, FormattedDateParts } from 'react-intl';` |
| `intimpmidp` | `import { FormattedMessage, useIntl, FormattedDateParts } from 'react-intl';` |
| `intimpmiddp` | `import { FormattedMessage, useIntl, FormattedDate, FormattedDateParts } from 'react-intl';` |
| `intimpiddp` | `import { useIntl, FormattedDate, FormattedDateParts } from 'react-intl';` |
| `intimpddp` | `import { useIntl, FormattedDateParts } from 'react-intl';` |
| `intimpddp` | `import { FormattedDate, FormattedDateParts } from 'react-intl';` |

### Formatted Components

| prefix    | Code                                      |
| --------- | ------------------------------------------------ |
| `fmsg` | `<FormattedMessage id='${1}' defaultMessage='${2}' />${0}` |
| `fmsgv` | `<FormattedMessage id='${1}' defaultMessage='${2}<${4:b}>${3}</${4:b}>${5}' values={{ ${4:b}: chunks => ( <${6:span} className='${7}'>{chunks}</${6:span}> ), }} />${0}` |
| `fdate` | `<FormattedDate value={${1:new Date()} />${0}` |
| `fdp` | `<FormattedDateParts> value={${1:new Date()}} year=\"${2:numeric}\" month=\"${3:numeric}\" day=\"${4:numeric}\" </FormattedDateParts>${0}` |
| `ftime` | `<FormattedTime value={${1:new Date()}} />${0}` |
| `ftp` | `<FormattedTimeParts value={${1: new Date()}} > {parts => ( <> {parts[0].value} {parts[1].value} {parts[2].value} </> )} </FormattedTimeParts>${0}` |

### UseIntl hook API

The initial cursor  placement starts at /$1 and works its way up as you press the tab with the final cursor placement at $0

| prefix    | Code                                      |
| --------- | ------------------------------------------------ |
| `imsg` | `intl.formatMessage({ id: '${1}', defaultMessage: '${2}'})${0}` |
| `imsgv` | `intl.formatMessage({ id: '${1}', defaultMessage: '${2} <${3:b}>$4</${3:b}>'}, { ${5:b}: (chunks) => <${6:span}>{chunks}</${6:span} > } )${0}` |
| `idate` | `intl.formatDate(${1:new Date()})${0}` |
| `idp` | `intl.formatDate( "${1:new Date()}, { year: ${2:'2-digit'}, month: ${2:'long'}, day: ${2:'numeric'} } )${0}` |
| `itime` | `intl.formatTime(${1:new Date()})${0}` |
| `itp` | `intl.formatTime( ${1:new Date()}, { hour: '${2:numeric}', minute: '${3:2-digit}', second: '${4:2-digit}', hour12: ${5:false}, } )${0}` |

---

## Known Issues

This is the initial launch of the snippets and not all of them have been added yet, if you see one you would like to add then please soo our contributing guide

## Release Notes

0.1 initial release with some of the snippets added

---
