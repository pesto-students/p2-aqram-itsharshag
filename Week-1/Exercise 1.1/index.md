## Exercise 1.1

### When a user enters an URL in the browser, how does the browser fetch the desired result ?
When we type a url like "https://www.example.com" in the browser:
1. The browser parses the information contained in the URL like the protocol, the domain name, and the resource
1. The browser communicates with the ISP to do a DNS lookup to get the IP address for the web server
1. After a successful lookup, the browser receives the IP address of the target website
1. The browser opens a TCP connection to the IP address of the web server
1. The browser receives the response from the server and parses it and displays the result
1. If the response is of type HTML, then the browser parses through its contents and fetches all the linked assets like images, CSS files, and JavaScript files

### a. What is the main functionality of the browser?
The main functionality of a browser is to retrieve and display web pages from the World Wide Web.
It fetches information from servers and renders the information in the appropriate way according to the response type.

### b. High level components of a browser
1. **UI (User Interface):** All the visual elements that we see of the browser. This consists of elements like the address bar, refresh page and bookmark buttons, the response section, and the developer tools.
1. **Browser Engine:** The internal engine of the browser recevies input from the browser's user interface and returns the computed results to the user interface to update it appropriately.
1. **Data Storage:** This includes all the storage mechanisms present in a browser like session storage, cookies, local storage, and IndexedDB.
1. **JavaScript Interpreter:** This component is responsible for executing all the JavaScript entered by a user and for updating the DOM to update the display.
1. **Networking:** This components consists of all the logic to parse addresses of different resources and fetch them using the specified protocol.

### c. Rendering engine and its use
Once a request is made, the requested document is received in chunks of 8KB from the networking layer and the following steps of the rendering engine take place:
1. Parse the requested HTML doc in chunks, including the external CSS files and in style elements. Convert the HTML elements into DOM nodes to form a “content tree” or "DOM tree."
1. Simultaneously, the browser creates a render tree. This tree includes both the styling information as well as the visual instructions that define the order in which the elements will be displayed. The render tree ensures that the content is displayed in the desired order.
1. The render tree goes through the layout process. When a render tree is created, the position or size values are not assigned. The entire process of calculating values for evaluating the desired position is called a layout process. In this process, every node is assigned the exact coordinates. This ensures that every node appears at an accurate position on the screen.
1. Finally, the screen is painted, wherein the render tree is traversed, and the renderer’s paint() method is invoked, which paints each node on the screen using the UI backend layer.

Hence, the use of the rendering engine is to parse and display the requested HTML document.

### d. Parsers (HTML, CSS, etc)
**HTML Parser:** The job of the HTML parser is to parse the HTML markup into a parse tree. The algorithm consists of two stages: tokenization and tree construction.

### Order of script processing