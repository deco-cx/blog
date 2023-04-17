# Introducing live.ts@v1 v1: Inline Loader, Layout Pages, Client-Side Loader Invocation and more!

In the world of web development, every second counts. A slow website can drive visitors away, and even a small delay can affect conversion rates. That's why we're excited to announce `live.ts@v1`, a new version of our platform that includes several key features to help you build faster, more efficient websites.

In this blog post, we'll take a closer look at three of `live.ts@v1`'s most exciting features: Inline Loader, Layout Pages, and Client-Side Loader Invocation.

# Acknowledgements

Thanks to everyone who made this release possible!

@Steffany-Martins, @augustocb, @eduardobbrito, @guifromrio, @guitavano, @igorbrasileiro, @lucis, @marialuizaaires, @matheusgr, @mcandeia, @soutofernando, @tlgimenes

# Overview

`live.ts@v1` has revolutionized the configuration engine, making it an exciting tool for developers who want to create non-predictable use cases. The new engine uses a unique and intelligent configuration resolution algorithm that enables you to save functions partially applied in a database to be used in runtime with confidence. The JSONSchema informs the Editor Admin of the possibilities for a given field and the eligible functions to be used, making the process more efficient and error-free.

The new engine also treats configuration as blocks, allowing you to compose multiple blocks together and create and save loaders that can be used inside a section. Pages are now components, and users can bring their own blocks and configurable elements to create a blog or any other type of website.

With near-realtime consistency and zero-latency on request lifecycle, `live.ts@v1` leverages the supabase realtime feature to receive any update just in time and fetch data in the background. This means that the internal configuration state is updated only when necessary, resulting in faster load times and a smoother user experience. You can also select multiple sections and save them into a page or inherit layouts from other pages, making it a versatile tool for developers of all levels.

The new engine has allowed us to create a platform that goes beyond traditional web development. With the power of the new configuration resolution algorithm and the ability to save loaders, sections, and pages as blocks, the possibilities are truly endless.

Developers can now bring their own blocks and configurable elements to create custom pages and components. Pages are no longer limited to a single layout, and sections can receive other sections as parameters. All of this can be achieved with near-realtime consistency and zero-latency on request lifecycle.

But that's just the beginning. With the new engine in place, we can continue to push the boundaries of what's possible in web development. We'll be able to add new features and capabilities that were previously unthinkable, making `live.ts@v1` an even more powerful tool for developers.

So if you're looking to create websites and applications that are both powerful and flexible, you've come to the right place. With `live.ts@v1`, you'll be able to take your development skills to the next level and build amazing things. The future of web development is here, at edge, and we're just getting started.

# Inline Loaders

One of the most significant challenges of web development is loading data efficiently. Previously, creating loaders for your website required opening a separate web page and navigating through the Editor Admin, which could be a time-consuming process and take you away from your code. With `live.ts@v1`, loaders can now be created and used inline, making it easier to create sections and write loaders for use cases when the data has no [interchangeability](https://www.deco.cx/docs/en/tutorials/universal-components). This improvement allows you to stay focused on your code while also streamlining the process of creating and using loaders.

The Inline Loader feature also includes improvements on JSONSchema generator. It now supports intersection, omits types, picks types, extends, recursive types, indexed properties, and much more. With these improvements, you can be sure your data is structured efficiently and accurately.

## Further details

[Proposal](https://github.com/deco-cx/live.ts/issues/164)
Check the [data-fetching](https://www.deco.cx/docs/en/tutorials/data-fetching) documentation for more information.

# Layout Pages

Creating consistent and visually appealing layouts across your website can be a challenge. With `live@v1`'s Layout Pages feature, you can now save your pages as a layout and use them across your site pages. That means you can create a page that has a header and a footer and focus only on the content of your shopping pages.

Layout Pages feature also includes sections inside sections, allowing you to build up a section that receives another section as a parameter. This makes it easier to create complex, nested layouts that are easy to maintain.

The sections used in Layout Pages are shared across all pages that inherints the layout, so whenever you change the Layout page the changes will be reflected in the entire site!

## Further details

Check the [Layout Pages](https://www.deco.cx/docs/en/concepts/layouts) documentation for more information.

# Client-Side Invocation

Client-side loaders invocation in live.ts@v1 is a game-changer for web developers who want to optimize their website's performance. With client-side invocation, you can now call your loaders through an API with a type-safe client-sdk and all the advantages of calling a loader on the server-side. This means you'll have faster pages and won't need to send unnecessary JavaScript to the browser, reducing the amount of code needed to render your pages.

Moreover, the client-side invocation feature ensures that your data fetching is unique across your repository, making it easier to maintain and manage. This way, you'll be able to create more complex applications while ensuring that your data is structured efficiently and accurately. With live.ts@v1, you'll be able to take your web development to the next level and build high-performance applications that deliver the best possible user experience.

## Further details

Check the [Client-side loaders invocation](https://www.deco.cx/docs/en/tutorials/client-side-invocation) documentation for more information.

# Migrate your site now

[Migration Guide](https://www.deco.cx/docs/en/migration-guides/v1.x)
