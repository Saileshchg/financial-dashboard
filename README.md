## Concepts understood so far

- Styling
- Optimizing Fonts
    - An ideal website loads a page, loads fallback font, downloads the actual font and then, replaces it. This cause some components on the page shift. The shift could be because of different font size. This term is called layout shift
    - Next.js downloads the fonts during build time and hosts them with your other static assets when you use next/font
    - Refer ui/fonts.ts
- Images
    - With using regular html <img> tag, you have to manually handle layout shifts, lazy loading, and sizing for different devices
    - Next.js provide a modified component which is an extension of <img> tag which automatically handles lazy loading, layout shifts, and image sizing for different devices
- Layout
    - Layout.tsx file is the layout for a particular set of pages. Whatever is added in this file is shared with all the components in this repository.
    - It's a react component which takes in children as parameters.
    - Also, when the route changes, only the child component is rerendered and not the entire layout
- Links
    - When using <a> tag, Next.js refreshes the entire page on route change.
    - To optimize that, Next.js introduced <Link> tag, this basically reloads only the part of the page (component) that changed during the route change.
    - How it works? On the server, Next.js code splits the code by components. Essentially, whenever a page loads, only the code required for that page is downloaded
    - Whenever Next.js sees a <Link> component, it prefetches and downloads the component in the browser
- "use client"
    - The usage of hooks requires browser API to be called. Hence, any component that uses React hooks cannot be rendered on server
    - The "use client" at the top of any Next.js component indicates the component to be rendered on client side


## Next.js App Router Course - Starter

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.
