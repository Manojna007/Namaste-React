Chapter 01 - Inception

Q: What is Emmet?

A: Emmet is a powerful tool for web developers that boosts productivity when writing HTML and CSS. It allows you to type short abbreviations, which then expand into full code snippets. For instance, typing div>ul>li*5 in Emmet will generate a structured HTML list with five items, saving time and minimizing the need to manually write repetitive code.

Q: Difference between a Library and a Framework?

A:

React (Library):

	•	Flexibility: React is a JavaScript library focused on building user interfaces, especially for single-page applications (SPAs).
	•	Your Control: You are in charge of how your app is structured. You call React’s functions, manage state, and handle events as you see fit.
	•	Analogy: Think of React like a toolkit where you have the freedom to decide what to build and how to organize it. You’re the architect.

Next.js (Framework):

	•	Predefined Structure: Next.js builds on React and comes with a framework to handle common features like routing, server-side rendering (SSR), and static site generation (SSG).
	•	Framework’s Control: The framework dictates some structure (e.g., routing) and automates some processes (e.g., SSR), but you still use React to build the UI components.
	•	Analogy: Next.js is more like having a house blueprint—you follow a predefined structure but can still customize the rooms using React.

In essence, React gives you full flexibility, while Next.js offers structure along with useful features to speed up development.

Q: What is CDN? Why do we use it?

A: A Content Delivery Network (CDN) is a system of distributed servers that deliver web content to users based on their geographic location. It enhances performance by reducing the physical distance between the user and the server. CDNs are widely used to:

	•	Speed up the loading of websites by serving cached content from servers closer to the user.
	•	Reduce server load and bandwidth consumption.
	•	Enhance security through features like DDoS protection.

Q: Why is React called React?

A: React is named React because of its ability to efficiently react to data changes. React’s declarative nature allows developers to describe what the UI should look like based on the application’s state, and React ensures the UI updates when that state changes. It was developed by Facebook with the goal of building dynamic user interfaces with minimal DOM manipulation and a responsive user experience.

Q: What is crossorigin in the script tag?

A: The crossorigin attribute in a <script> tag controls how the browser handles cross-origin requests for the script file. It’s used in scenarios where you are loading resources like scripts from a different domain (e.g., a CDN). There are two primary values:

	•	anonymous: This allows for cross-origin requests without sending credentials (cookies or HTTP authentication).
	•	use-credentials: This sends credentials (cookies or HTTP authentication) along with the cross-origin request.

This attribute is crucial when dealing with CORS (Cross-Origin Resource Sharing), ensuring secure and controlled sharing of resources between domains.

<script src="https://cdn.example.com/script.js" crossorigin="anonymous"></script>

Q: Difference between React and ReactDOM?

A:

	•	React: A JavaScript library for building reusable user interface components. It focuses on the logic behind creating elements and managing component state.
	•	ReactDOM: A separate library that connects React with the DOM (Document Object Model). It provides methods like ReactDOM.render() to display React components in the browser, and it handles server-side rendering via ReactDOMServer.

In summary, React is for building components, while ReactDOM takes care of rendering them into the browser.

Q: Difference between react.development.js and react.production.js via CDN?

A:

	•	react.development.js: This version includes helpful error messages, warnings, and debug information to aid in the development process. It’s slower but provides more detailed error handling.
	•	react.production.js: Optimized for performance, this version removes debugging and error-checking code to minimize file size and improve performance. This is the version you should use in a live, production environment.

Q: What is async and defer in script tags?

A:

	•	Async: The script is fetched and executed asynchronously (in the background), without blocking the HTML parser. As soon as the script is ready, it is executed immediately, which might interrupt HTML parsing.

<script src="script.js" async></script>


	•	Defer: The script is also fetched asynchronously, but it only runs after the HTML document has finished parsing, ensuring that the DOM is fully built before the script is executed. This is recommended when scripts depend on the DOM being available.

<script src="script.js" defer></script>



For modern JavaScript, always use type="module" for better code organization and performance:

<script type="module" src="main.js"></script>

This enables features like top-level await, async execution, and strict mode by default. It’s especially useful for projects where you want to break code into modules for better maintainability.