Help make the Firefox developer tools better by filing bugs and writing code.

## Filing a Bug

If you notice a bug in the developer tools, please [file a bug](https://bugzilla.mozilla.org/enter_bug.cgi?product=Firefox&component=Developer%20Tools) on Bugzilla. You'll have to create a Bugzilla account to do so, but that only takes a couple minutes.

## Contributing Code

### Finding a Bug to Fix
If you notice a issue with the tools, you could actually fix it yourself. If a bug doesn't exist yet, file one, and assign the bug to yourself saying that you plan on fixing it.

If you'd like to contribute, but haven't found a bug, you can search for [good first bugs](https://bugzilla.mozilla.org/buglist.cgi?cmdtype=dorem&remaction=run&namedcmd=devtools-first-bugs&sharer_id=249294&list_id=6590054) on Bugzilla.

### Getting Help

At any point if you can't figure out how to do something, you can get help on IRC. Get an IRC client (like [LimeChat](http://limechat.net/mac/) on OS X), log onto the `irc.mozilla.org` network, and join the `#devtools` channel.

Ask your question in the channel, and someone who knows about that area will respond. The best times to ask are in the afternoon on European time or morning in US time on weekdays, when the most people are watching the channel. Everyone is nice there.

### Writing a patch

To write a patch for a devtools bug, you'll need to build Firefox locally and create a patch using the Mercurial VCS. There's a lot of help over at the [MDN Developer Guide](https://developer.mozilla.org/en-US/docs/Developer_Guide). The steps to getting a patch in devtools are:

#### Building Firefox
To write a devtools patch, you'll need to check out the Firefox source code and build it. Check out these [directions for building](https://developer.mozilla.org/en-US/docs/Simple_Firefox_build).

Devtools uses the "fx-team" branch, not mozilla-central, so you'll want to checkout the code with:

```bash
hg checkout https://hg.mozilla.org/integration/fx-team
```

#### Editing the Devtools Code

The devtools are written in JavaScript. Most of the code is located in the `browser/devtools` directory of the Mozilla source code. However, if you're changing the server actors for the remote debugging protocol, you'll find that code in `toolkit/devtools`.

Finding out where to make your changes can be tricky. Generally, each tool has its own subdirectory under the `devtools` directory. It can be helpful to grep for strings you see in the UI or class names you see on elements of the tool's UI (you can find this using the [DOM Inspector](https://addons.mozilla.org/en-us/firefox/addon/dom-inspector-6622/) and [Inspect Context](https://addons.mozilla.org/en-us/firefox/addon/inspect-context/) addons). [DXR](http://dxr.mozilla.org/) is a great web UI for searching and navigating the Firefox code base as well.

If you need a pointer in the right direction, just ask in IRC.

#### Trying Out Your Changes

Most of the time, you'll only need to rebuild the `browser` directory after making a change to the devtool's code:

```
./mach build browser
```

After re-building you can restart Firefox to see the changes reflected. The [Restartless Restart](https://addons.mozilla.org/en-us/firefox/addon/restartless-restart/) addon is handy for this.

You can debug your code with handy log statements or the browser's debugger, check out the [docs on debugging Firefox JavaScript code](https://developer.mozilla.org/en-US/docs/Debugging_JavaScript).

#### Testing Your Changes
You'll want to make sure the devtools tests pass as well. Most devtools tests can be run with this mach command:

```
./mach mochitest-browser browser/devtools
```

That can take awhile to run, so you might want to narrow it down to your tool's subdirectory.

### Submitting a Patch

Make a patch [using Mercurial patch queues](https://developer.mozilla.org/en-US/docs/Mercurial_FAQ#How_can_I_generate_a_patch_for_somebody_else_to_check-in_for_me.3F), and add it as an attachment to the bug.


#### Asking for Review
When you attach your patch file to a bug, you should flag someone for review as well, otherwise it might get lost in the ether. Ask in IRC for a good person to review your patch, mentioning the bug number.


