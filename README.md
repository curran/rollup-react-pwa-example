# rollup-react-pwa-example
An example project setup with Rollup, server-side React rendering, and code splitting.

This is a rather experimental setup that aims for the following:

 * Understandable and minimal dependencies and dev dependencies.
 * Use of Rollup
 * Use of React
 * Server side rendering (SSR)
 * Code splitting
 * Large dependencies excluded from our bundle(s), sourced from a CDN instead

It turns out that SSR and code splitting are a bit tricky to get working at the same time. To make this happen, I ended up generating three builds: server, client, and client2 (which is the lazy loaded browser-only portion of the client). For dynamic module loading I opted to use `d3-require` as it's the smallest AMD loader I could find.
