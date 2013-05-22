Develop a mobile-friendly app with the aide of the **Responsive Design View**, **appcache** command and [Firefox OS Simulator](https://developer.mozilla.org/en-US/docs/Tools/Firefox_OS_Simulator).

## Testing Responsive Design

To see how your app would look at various screen sizes, use the **Responsive Design View**:

[[images/responsive-view.png|width=700px]]

Set the page's dimensions with various presets, or add a custom preset for later use.

## Debugging AppCache

If you use [AppCache](https://developer.mozilla.org/en-US/docs/HTML/Using_the_application_cache) to enable offline support in your app, you can use the `appcache` command to debug it.

First open the **Developer Toolbar** from the **Web Developer** menu, then type `help appcache` into the prompt to see all the appcache commands:

[[images/appcache.png|width=700px]]

[More info in this blog post](http://flailingmonkey.com/application-cache-not-a-douchebag)

## Simulating Mobile Events

Load your app in Firefox on the [Firefox OS Simulator](https://developer.mozilla.org/en-US/docs/Tools/Firefox_OS_Simulator) and simulate touch events, `deviceorientation` events, and the Geolocation API, from the [Simulator toolbar](https://developer.mozilla.org/en-US/docs/Tools/Firefox_OS_Simulator#Simulator-toolbar)
