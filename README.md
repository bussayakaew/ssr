# SSR - Router with SSR for Node & Meteor

![logo](https://raw.githubusercontent.com/ssrwpo/ssr/master/doc/logo_small.png)

Server side rendering with Express, react-router-4 & redux for Meteor.

## Project documentation

Please visit our [project page](https://ssrwpo.github.io/)

### Installation in your own project

You can replace yarn by your favorite way of installing NPM packages.  
To install yarn : https://yarnpkg.com/en/docs/install  
To install "meteor yarn" : ```meteor npm i -g yarn```  

```
meteor yarn add is-retina lodash moment react react-dom react-helmet react-intl \
  react-intl-redux react-redux react-router-dom actual electrode-react-ssr-caching \
  express farmhash helmet html-minifier intl receptacle url-pattern useragent \
  styled-components
meteor add ssrwpo:ssr
```

### To run the demo based on this repository

```
git clone https://github.com/ssrwpo/ssr.git && cd ssr
meteor yarn install
cd demo
meteor yarn install
yarn meteor
```

## Package development

### Benchmarks
For profiling the most appropriate libraries or function call a benchmark suite
is setup in `benchmarks`. Launch a test using [`babel-node`](https://babeljs.io/docs/usage/cli/#babel-node).

Ex. `babel-node benchmarks/getFromObject.js`

### Debug helpers
The last request and last response received in Express are exposes by this
package as `debugLastRequest` and `debugLastResponse`, respectively. In Meteor's
shell, you can access them via:

```js
import { debugLastRequest, debugLastResponse } from 'meteor/ssrwpo:ssr';
```

### Launching tests
This project uses [Jest](https://facebook.github.io/jest/) and [chai](http://chaijs.com/).

```
# In one-shot mode:
yarn test
# In watch mode:
yarn test.watch
```

### Linting
The linter is based on [ESlint](http://eslint.org/) configured with [Airbnb styles](https://github.com/airbnb/javascript).

```
yarn lint
```

:warning: All code must be linted before sending any PR. See the [Contributing guide](./CONTRIBUTING.md).

## Artwork

Logo created by [Alexandre Tabbuso](https://www.facebook.com/TabbusoAlexandre/).

## 3rd party documentation
- [Application router: react-router-4](https://react-router.now.sh)
- [Egghead's React router 4 - videos tutorials](https://egghead.io/lessons/react-run-the-react-router-v4-examples-with-create-react-app)
- [Universal logging: pino](https://github.com/pinojs/pino)
- [Protocol: Robots.txt](http://www.robotstxt.org/)
- [Protocol: Sitemaps](https://www.sitemaps.org/)
- Not a 3rd party but strongly recommended: [sitemap.js](https://github.com/ekalinin/sitemap.js)
- [Protocol: Humans.txt](http://humanstxt.org/)
- [Server side security: helmet](https://github.com/helmetjs/helmet)
- [Server side performance profiling: benchmark](https://benchmarkjs.com/)
- [In memory LRU cache: receptacle](https://github.com/DylanPiercey/receptacle)
- [Server side component caching: electrode-react-ssr-caching](https://github.com/electrode-io/electrode-react-ssr-caching)
- [User agent parser: useragent](https://github.com/3rd-Eden/useragent)
- [Meteor issue on Hot code push](https://github.com/meteor/meteor/issues/7115)
- [Discussions about Hot code push issue](https://forums.meteor.com/t/app-constantly-refreshing-after-an-update/23586/143)
- [Unit tests: Jest](https://facebook.github.io/jest/)
- [Unit tests: chai](http://chaijs.com/)
- [styled-components](https://styled-components.com/)
- Not a 3rd party but strongly recommended: [polished](https://polished.js.org/)

## Links
- [Atomic design](http://patternlab.io/)
- [Reactjs - Speed up Server Side Rendering - Sasha Aickin](https://www.youtube.com/watch?v=PnpfGy7q96U)
- [Hastening React SSR with Component Memoization and Templatization](https://www.youtube.com/watch?v=sn-C_DKLKPE)
- [Server-Side Rendering: Live Code Session - Supercharged (with info on cache control)](https://www.youtube.com/watch?v=8LM4p7l9YMY)
- [AppCache](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache#Browser_compatibility)
- [Caching best practices & max-age gotchas](https://jakearchibald.com/2016/caching-best-practices/)
- [Increasing Application Performance with HTTP Cache Headers](https://devcenter.heroku.com/articles/increasing-application-performance-with-http-cache-headers)
- [Progressive Web Apps With React](https://addyosmani.com/blog/progressive-web-apps-with-react/)
- [Discussion on main thread at client side initial rendering](https://github.com/developit/preact/issues/407)

## Sites using this engine in production

- [Panoply City](https://www.panoplycity.com/)
