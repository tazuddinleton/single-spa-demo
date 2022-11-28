# Single-Spa

Framework that allows apps written in different front-end frameworks work together. Features are as follows
- You can write apps in different frameworks and make them work together
- Lazy loading
- Hot-swappable apps
- Encourages using system-js to load modules instead of module federation. However both can work together.
- Tool for local development, using import-map-override you can run only one micro app locally, other apps can run from dev/prod server
- Tool for deployment import-map-deployer 
- CLI for development create-single-spa
- Common utility module, need not to be registered as mfe app or parcel.
- Cross mfe export/import
- Shared dependencies loads only once
  - Using import-maps
  - Using module federation
  - Both (not recommended by core team)
- Mono repo discouraged
- Deployable using CDN or docker container
- Discourages using global state management system like redux.

# Key ideas
## In-browser module vs Build time module
Review [this video](https://www.youtube.com/watch?v=Jxqiu6pdMSU&list=PLLUD8RtHvsAOhtHnyGx57EYXoaNsxGrTU&index=2)

Or the whole [play list](https://www.youtube.com/playlist?list=PLLUD8RtHvsAOhtHnyGx57EYXoaNsxGrTU) for better insight into doing mfe using single-spa.


# Create App
To create Apps using single spa first create a root-config, then add mfe applications go it. Refere to this [guide](https://single-spa.js.org/docs/getting-started-overview) for detail.

To add root config: `npx create-single-spa --moduleType root-config`

To add mfe app: `npx create-single-spa --moduleType app-parcel`


