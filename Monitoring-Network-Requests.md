Monitor network traffic with the **Network** tool.

## Reading the Network Timeline

Once you open the Network panel, you'll be required to reload the page to start monitoring network requests. After reloading you'll see something like this:

[[images/network.png|width=740px]]

This is a list of the network requests your app made, ordered by start time.

The request list has these columns for each request:

* **✓** - HTTP status code
* **Method** - HTTP request method
* **File** - Basename of the path requested
* **Domain** - Domain of the path requested
* **Type** - `Content-type` of the response
* **Size** - Size of the response

### Request Timing Breakdown

The list also has a column with a bar-like graphical representation of the timing of different parts of the request:

[[images/timeline-bar.png|width=600px]]

The colors have the following meanings:

* **pink/purple**: DNS resolution
* **brown**: Connecting over TCP
* **green**: Sending request
* **transparent**: Waiting for server response
* **cyan/white**: Receiving response

After selecting a particular request, you can see an exact breakdown of the times in the **Timing** tab of the sidebar that opens:

[[images/timings.png]]

### Headers

The **Headers** sidebar tab shows the HTTP request and response headers that were sent:

[[images/headers.png|width=400px]]

### Cookies

See the cookies sent with a request in the **Cookies** sidebar tab:

[[images/cookies.png|width=400px]]

### GET Params and POST Data

The **Params** sidebar tab shows the GET params and POST data of a request:

[[images/params.png|width=400px]]

### Response

The response tab shows the response body. If the response is JSON, it will be shown as an inspectable object. If it's an image, a preview will be shown, and HTML and CSS are shown in a source editor:

[[images/response.png|width=400px]]





