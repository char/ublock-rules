# ublock-rules

charlotte's ruleset for making sites better using uBlock Origin.

To create a new content blocking rule, right click somewhere on the page,
hit 'Block Element' on the context menu that pops up, and paste the rule in.

## Twitter

### Trending widget

`##section[role="region"]:has(h1:has-text("Trending now"))`

[Screenshot](./images/twitter-trending-widget.png) (cw: shows trending items)

### 'Discover more' under tweets

1. `##[data-testid=cellInnerDiv]:has(h2:has-text(Discover more))`
2. `##[data-testid=cellInnerDiv]:has(h2:has-text(Discover more)) ~ *`

[Screenshot](./images/twitter-discover-more.png)

### Twitter Blue button

`##nav > a[href="/i/twitter_blue_sign_up"]`

[Screenshot](./images/twitter-blue.png)

### Twitter "Verified Orgs"

`##[data-testid=Dropdown] div:has(> a[href="/i/verified-orgs-signup"])`

[Screenshot](./images/twitter-verified-orgs.png)

### Quote tweets of/about JK Rowling

`##article[data-testid=tweet]:has(span:has-text(/^Quote Tweet$/)):has(div[role=link]:has-text(/@?j[. ]*k[ _\-.]*rowling/i))`

### Sidebar widget: "Spaces"

`##[data-testid="sidebarColumn"] h2:has-text(Listen live in Spaces):upward(2)`

## SoundCloud

### Home screen insights widget

`##.insightsSidebarModule`

## Google

### Links to w3schools

1. `###search > div > div > div:has(a[href*=".sqlitetutorial.net/"])`
2. `###search > div > div > div:has(a[href*=".w3schools.com/"])`

## YouTube

### Home page "Shorts" shelf

`##ytd-rich-shelf-renderer[is-shorts]`
