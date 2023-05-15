# Next.JS-Tutorial
## Installiation:    
npm install next@latest react@latest
 ## react-dom@latest
Running the development server:   npm run dev

### Overview
### package.json 
Where all our library get installed

### package-lock.json

It's pretty much the same as package.json but it locks all the packages.

### config file 
It's using the app directory

### json.config

### gitignore 
The stuff that we don't want to push on Github including environment variables.

### public
This is where we see all our images, svgs and whatnot ?

What essentially this API rout is going to allow us to do is to query data from a DB
for example do off in here on the backend (server-side rendering with Next off on the server and using server-side component)

### App folder
This is the most important folder in Next JS
This is where we define our pages. It contains layout.js , page.js and also global.css
#### layout.js 
this file is the main entry point of our application and all of our components are wrapped within it as its children. As a result any code we write within this file such as a p tag hello world would be displayed in every rout page you create. This unique file enables you to personalize the behavior of your application by providing a common layout or template for all of the pages. Any components that we include in this file will be shared throughout our entire application. 
Additionally this file also allows us to customize the appearance of our HTML document so we can set things like language and we can also modify the metadata for all pages as well as add the script tags, links or even fonts as it is done in this case. 
In the nutshell if we want to add something that should stay consistent across all routes such as navbar, footer or toolkit wrapper we should place it in the layout.js file.

#### page.js

This simply represents the home page rout of the application. i.e. it's what we see if we go to localhost:3000/

This page even though it looks like a normal react functional component it is being
rendered as something known as a server-side component 

#### global.css 

This file contains the global CSS styles of the entire application 
It is imported to the layout.js file so that every single rout inherits it 
We might have Tailwind imports which will helps us utilize Tailwind within our
application now.
### Note:
By default all the components created in next.js within the app folder are react server components which means that next js leverages server-side rendering to enhance the initial page loading speed resulting in improved SEO and user experience.

Now if we want to turn that server side component by default into a client-side one 
we need to add the "use client" directive to the top of our page to turn it into a 
client-side component 

Using both server-side and client-side component allows us to leverage the benefits of server-side rendering while still utilizing react capabilities for building dynamic and interactive user interfaces. 

Whenever we utilizing state or hooks like useStates in react or other client-side management solutions it is important to declare the component as a client-side component 
State Management in react is primarily handled on the client-side where the component state is managed and updated within the browser.

When to should use server vs. client components?

In the documentation is recommend using server components (default in the app directory) until we have a need to use a Client Component.
Essentially doing what we are doing until get error, so we transform it to client component 