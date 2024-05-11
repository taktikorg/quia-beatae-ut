<img width="75px" height="75px" align="right" alt="Inquirer Logo" src="https://raw.githubusercontent.com/taktikorg/quia-beatae-ut/master/assets/@taktikorg/quia-beatae-ut_readme.svg?sanitize=true" title="Inquirer.js"/>

# Inquirer

[![npm](https://badge.fury.io/js/@@taktikorg/quia-beatae-ut%2Fprompts.svg)](https://www.npmjs.com/package/@@taktikorg/quia-beatae-ut/prompts)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FSBoudrias%2FInquirer.js.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FSBoudrias%2FInquirer.js?ref=badge_shield)

A collection of common interactive command line user interfaces.

![List prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/list.svg)

Give it a try in your own terminal!

```sh
npx @@taktikorg/quia-beatae-ut/demo@latest
```

# Installation

```sh
npm install @@taktikorg/quia-beatae-ut/prompts

yarn add @@taktikorg/quia-beatae-ut/prompts
```

Inquirer recently underwent a rewrite from the ground up to reduce the package size and improve performance. The previous version of the package is still maintained (though not actively developed), and offered hundreds of community contributed prompts that might not have been migrated to the latest API. If this is what you're looking for, the [previous package is over here](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/@taktikorg/quia-beatae-ut).

# Usage

```js
import { input } from '@@taktikorg/quia-beatae-ut/prompts';

const answer = await input({ message: 'Enter your name' });
```

# Prompts

## [Input](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/input)

![Input prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/input.svg)

```js
import { input } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/input) for usage example and options documentation.

## [Select](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/select)

![Select prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/list.svg)

```js
import { select } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/select) for usage example and options documentation.

## [Checkbox](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/checkbox)

![Checkbox prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/checkbox.svg)

```js
import { checkbox } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/checkbox) for usage example and options documentation.

## [Confirm](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/confirm)

![Confirm prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/confirm.svg)

```js
import { confirm } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/confirm) for usage example and options documentation.

## [Password](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/password)

![Password prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/password.svg)

```js
import { password } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/password) for usage example and options documentation.

## [Expand](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/expand)

![Expand prompt closed](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/expand-y.svg)
![Expand prompt expanded](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/expand-d.svg)

```js
import { expand } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/expand) for usage example and options documentation.

## [Editor](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/editor)

Launches an instance of the users preferred editor on a temporary file. Once the user exits their editor, the content of the temporary file is read as the answer. The editor used is determined by reading the $VISUAL or $EDITOR environment variables. If neither of those are present, the OS default is used (notepad on Windows, vim on Mac or Linux.)

```js
import { editor } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/editor) for usage example and options documentation.

## [Raw List](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/rawlist)

![Raw list prompt](https://cdn.rawgit.com/taktikorg/quia-beatae-ut/28ae8337ba51d93e359ef4f7ee24e79b69898962/assets/screenshots/rawlist.svg)

```js
import { rawlist } from '@@taktikorg/quia-beatae-ut/prompts';
```

[See documentation](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/rawlist) for usage example and options documentation.

# Create your own prompts

The [API documentation is over here](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/core), and our [testing utilities here](https://github.com/taktikorg/quia-beatae-ut/tree/master/packages/testing).

# Advanced usage

All @taktikorg/quia-beatae-ut prompts are a function taking 2 arguments. The first argument is the prompt configuration (unique to each prompt). The second is providing contextual or runtime configuration.

The context options are:

| Property          | Type                    | Required | Description                                                  |
| ----------------- | ----------------------- | -------- | ------------------------------------------------------------ |
| input             | `NodeJS.ReadableStream` | no       | The stdin stream (defaults to `process.stdin`)               |
| output            | `NodeJS.WritableStream` | no       | The stdout stream (defaults to `process.stdout`)             |
| clearPromptOnDone | `boolean`               | no       | If true, we'll clear the screen after the prompt is answered |

Example:

```js
import { confirm } from '@@taktikorg/quia-beatae-ut/prompts';

const allowEmail = await confirm(
  { message: 'Do you allow us to send you email?' },
  {
    output: new Stream.Writable({
      write(chunk, _encoding, next) {
        // Do something
        next();
      },
    }),
    clearPromptOnDone: true,
  },
);
```

## Canceling prompt

All prompt functions are returning a cancelable promise. This special promise type has a `cancel` method that'll cancel and cleanup the prompt.

On calling `cancel`, the answer promise will become rejected.

```js
import { confirm } from '@@taktikorg/quia-beatae-ut/prompts';

const answer = confirm(...); // note: for this you cannot use `await`

answer.cancel();
```

# Recipes

## Get answers in an object

When asking many questions, you might not want to keep one variable per answer everywhere. In which case, you can put the answer inside an object.

```js
import { input, confirm } from '@@taktikorg/quia-beatae-ut/prompts';

const answers = {
  firstName: await input({ message: "What's your first name?" }),
  allowEmail: await confirm({ message: 'Do you allow us to send you email?' }),
};

console.log(answers.firstName);
```

## Ask a question conditionally

Maybe some questions depend on some other question's answer.

```js
import { input, confirm } from '@@taktikorg/quia-beatae-ut/prompts';

const allowEmail = await confirm({ message: 'Do you allow us to send you email?' });

let email;
if (allowEmail) {
  email = await input({ message: 'What is your email address' });
}
```

## Get default value after timeout

```js
import { setTimeout } from 'node:timers/promises';
import { input } from '@@taktikorg/quia-beatae-ut/prompts';

const ac = new AbortController();
const prompt = input({
  message: 'Enter a value (timing out in 5 seconds)',
});

prompt
  .finally(() => {
    ac.abort();
  })
  // Silencing the cancellation error.
  .catch(() => {});

const defaultValue = setTimeout(5000, 'timeout', { signal: ac.signal }).then(() => {
  prompt.cancel();
  return 'Timed out!';
});

const answer = await Promise.race([defaultValue, prompt]);
```

## Using as pre-commit/git hooks, or scripts

By default scripts ran from tools like `husky`/`lint-staged` might not run inside an interactive shell. In non-interactive shell, Inquirer cannot run, and users cannot send keypress events to the process.

For it to work, you must make sure you start a `tty` (or "interactive" input stream.)

If those scripts are set within your `package.json`, you can define the stream like so:

```json
  "precommit": "my-script < /dev/tty"
```

Or if in a shell script file, you'll do it like so: (on Windows that's likely your only option)

```sh
#!/bin/sh
exec < /dev/tty

node my-script.js
```

## Wait for config

Maybe some question configuration require to await a value.

```js
import { confirm } from '@@taktikorg/quia-beatae-ut/prompts';

const answer = await confirm({ message: await getMessage() });
```

# Community prompts

If you created a cool prompt, [send us a PR adding it](https://github.com/taktikorg/quia-beatae-ut/edit/master/README.md) to the list below!

[**Interactive List Prompt**](https://github.com/pgibler/@taktikorg/quia-beatae-ut-interactive-list-prompt)<br/>
Select a choice either with arrow keys + Enter or by pressing a key associated with a choice.

```
? Choose an option:
>   Run command (D)
    Quit (Q)
```

[**Action Select Prompt**](https://github.com/zenithlight/@taktikorg/quia-beatae-ut-action-select)<br/>
Choose an item from a list and choose an action to take by pressing a key.

```
? Choose a file Open <O> Edit <E> Delete <X>
❯ image.png
  audio.mp3
  code.py
```

[**Table Multiple Prompt**](https://github.com/Bartheleway/@taktikorg/quia-beatae-ut-table-multiple)<br/>
Select multiple answer from a table display.

```sh
Choose between choices? (Press <space> to select, <Up and Down> to move rows,
<Left and Right> to move columns)

┌──────────┬───────┬───────┐
│ 1-2 of 2 │ Yes?  │ No?   |
├──────────┼───────┼───────┤
│ Choice 1 │ [ ◯ ] │   ◯   |
├──────────┼───────┼───────┤
│ Choice 2 │   ◯   │   ◯   |
└──────────┴───────┴───────┘

```

[**Toggle Prompt**](https://github.com/skarahoda/@taktikorg/quia-beatae-ut-toggle)<br/>
Confirm with a toggle. Select a choice with arrow keys + Enter.

```
? Do you want to continue? no / yes
```

[**Sortable Checkbox Prompt**](https://github.com/th0r/@taktikorg/quia-beatae-ut-sortable-checkbox)<br/>
The same as built-in checkbox prompt, but also allowing to reorder choices using ctrl+up/down.

```
? Which PRs and in what order would you like to merge? (Press <space> to select, <a> to toggle all, <i> to invert selection, <ctrl+up> to move item up, <ctrl+down> to move item down, and <enter> to proceed)
❯ ◯ PR 1
  ◯ PR 2
  ◯ PR 3
```

# License

Copyright (c) 2023 Simon Boudrias (twitter: [@vaxilart](https://twitter.com/Vaxilart))<br/>
Licensed under the MIT license.
