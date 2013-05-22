Debug Javascript with the aid of the **Console** and **Debugger** tools.

## Finding Errors

Any JavaScript errors in your app will be reported in the **Console**:

[[images/console.png]]

## Logging

`console.log()` calls will show up in the Console as well. The Console supports `log`, `info`, `error`, `dir`, `time`, and `profile`, among others. See the [console API](https://developer.mozilla.org/en-US/docs/Web/API/console) for details on each.

## Setting Breakpoints

Pause execution of JavaScript code when it hits a specific line by adding a breakpoint in the **Debugger**. Find the script you want to debug in the Debugger, and click the gutter next to the line to add a breakpoint.

[[images/breakpoints.png]]

### Conditional Breakpoints

Conditional breakpoints are only triggered when a JS expression evaluates to `true `. Set a conditional breakpoint by right-clicking a line and choosing **Add conditional breakpoint**:

[[images/conditional-breakpoint.png]]

### Pause on Exceptions

Automatically break when an exception is thrown by toggling the **Pause on exceptions** item in the Debugger's own settings menu. The settings menu is enabled by clicking the gear icon on the far right of the Debugger toolbar.

[[images/pause-exception.png]]

## After Hitting a Breakpoint

When a breakpoint is hit, the Debugger window looks like this:

[[images/after-breakpoint.png]]

From here you can:

* **Continue (F6)**  - Resume execution of the script
* **Step Over (F7)** - Step to the next line.
* **Step In (F8)** - Step into the current line, descending into any function
calls if there are any. If there are none, this is the equivalent of Step Over.
* **Step Out (Shift-F8)** - Continue execution and pause at the next `return`.

### Examining the Call Stack

When the debugger is paused, you can examine the current call stack using the breadcrumbs along the top of the Debugger. These display the calls from the bottom of the call stack to the top. Clicking one of the breadcrumbs will take you to the script and line of that call.

### Watch Expressions

Watch expressions are JavaScript expressions that are evaluated each time execution pauses.

See the current value of a watch expression in the debugger sidebar. When the value changes, it's briefly highlighted in yellow.

Click **Add watch expression** to add an expression.

[[images/watch-exp.png]]

## Searching in Scripts

Find the right line to visit using the **Filter scripts** search box. Perform full-text search, go directly to a line, and search by function definition or variable name:

[[images/search-scripts.png]]
