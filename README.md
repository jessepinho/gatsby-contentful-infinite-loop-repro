This is a reproduction of the infinite-loop issue described in https://github.com/gatsbyjs/gatsby/issues/11364.

Steps to reproduce:

1. `yarn install`
2. `gatsby develop`

Note that there is a `Maximum call stack size exceeded` error in the console. This is due to the circular references in Contentful: Article A has a reference to Article B in its rich-text body, and vice versa. You can try viewing the actual content in Contentful's [Discovery app](https://discovery.contentful.com/entries/by-content-type?delivery_access_token=04QAYaRsr548atM4KwInDCWk8v84agx0uS7r8LrQutk&preview=false&preview_access_token=&space_id=j66qheg22uli), but it currently has some JS errors that are preventing it from working.
