Use the **Profiler** tool to find out where your JavaScript code is spending too much time. The Profiler periodically samples the current JS call stack and compiles statistics about the samples.

## Collecting a Profile

Once you've opened the **Profiler** tool, you can start profiling by clicking the **Start** button:

[[images/start-profiler.png]]

Stop profiling by clicking the **Stop** button.

### Collecting with console.profile()

Another way to collect a profile is to call `console.profile()` and `console.profileEnd()` in your JavaScript:

```javascript
console.profile("detection"); // start a profile with name "detection"

kittydar.detectCats(canvas);

console.profileEnd("detection"); // stop profiling
```

Once `profileEnd()` is called, a new profile will be added to the Profiler UI. **Note**: `console.profile()` only collects a profile if the Devtools Window is open.

## Analyzing a Profile

Once profiling is stopped and a profile has been collected, it will show up in the Profiler UI:

[[images/new-profile.png]]

The profile will have a chart of the samples running along the top. The horizontal axis is sample number, and the vertical axis is call stack size at that sample.

The sampled calls are presented at the bottom half as a tree of calls. Calls are nested under their callers. Along the left side are statistics about the number of samples that contain that call:

**Running Time** - The first number listed is the total number of samples with that call in it. The second is the percentage of samples with that call.

**Self** - The number of samples where that call is at the top of the call stack, i.e. it's inside that function's code and not a function it's calling.

Grey-colored calls are functions in the browser, not your code.

Red samples along the chart indicates the browser was blocked during those samples (bad).

## Analyzing a Sample Range

Examine a particular range of samples by clicking and dragging your mouse along the sample graph from the desired start point to end point. A new range will show up next to the Profile:

[[images/profiler-range.png]]





