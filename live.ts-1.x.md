# Introducing live.ts@v1: Inline loaders, Page Layouts, Client-Side Loader Invocation and more!

In the world of web development, every second counts. A slow website can drive visitors away, and even a small delay can affect conversion rates. That's why we're excited to announce `live.ts@v1`, a new version of our platform that includes several key features to help you build faster, more efficient websites.

In this blog post, we'll take a closer look at three of `live.ts@v1`'s most exciting features: Inline Loader, Page Layouts, and Client-Side Loader Invocation.

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

# Improved expressiveness of the loader functions

We are excited to announce a significant change in the way developers create `loaders` for our platform. With this change, we have simplified the loader creation process, making it easier and faster for developers to create and modify loaders without breaking any existing constraints. This new approach allows us to evolve the platform more quickly, while providing developers with a more streamlined workflow. We believe that this change will help developers to be more productive and efficient in their work, ultimately leading to faster development times and a better user experience for our customers. The new approach removes the necessity for declaring `LoaderReturnType` and simplifies the loader function signature. The old `functions` approach still works, but we have decided to deprecate it. Now, `loaders` can be created and modified inside `loaders/` folder. Check our 1.0.0 [documentation](https://www.deco.cx/docs/en/concepts/loader) for more information.

# Inline Loaders

One of the most significant challenges of web development is loading data efficiently. Previously, creating loaders for your website required opening a separate web page and navigating through the Editor Admin, which could be a time-consuming process and take you away from your code. With `live.ts@v1`, loaders can now be created and used inline, making it easier to create sections and write loaders for use cases when the data has no [interchangeability](https://www.deco.cx/docs/en/tutorials/universal-components). This improvement allows you to stay focused on your code while also streamlining the process of creating and using loaders.

The Inline Loader feature also includes improvements on JSONSchema generator. It now supports intersection, omits types, picks types, extends, recursive types, indexed properties, and much more. With these improvements, you can be sure your data is structured efficiently and accurately.

## Further details

[Proposal](https://github.com/deco-cx/live.ts/issues/164)
Check the [data-fetching](https://www.deco.cx/docs/en/tutorials/data-fetching) documentation for more information.

# Page Layouts

Creating consistent and visually appealing layouts across your website can be a challenge. With `live@v1`'s Page Layouts feature, you can now save your pages as a layout and use them across your site pages. That means you can create a page that has a header and a footer and focus only on the content of your shopping pages.

Page layouts feature also includes sections inside sections, allowing you to build up a section that receives another section as a parameter. This makes it easier to create complex, nested layouts that are easy to maintain.

The sections used in page layouts are shared across all pages that inherints the layout, so whenever you change the page layouts the changes will be reflected in the entire site!

## Further details

Check the [Layout Pages](https://www.deco.cx/docs/en/concepts/layouts) documentation for more information.

# Client-Side Invocation

Client-side loaders invocation in live.ts@v1 is a game-changer for web developers who want to optimize their website's performance. With client-side invocation, you can now call your loaders through an API with a type-safe client-sdk and all the advantages of calling a loader on the server-side. This means you'll have faster pages and won't need to send unnecessary JavaScript to the browser, reducing the amount of code needed to render your pages.

Moreover, the client-side invocation feature ensures that your data fetching is unique across your repository, making it easier to maintain and manage. This way, you'll be able to create more complex applications while ensuring that your data is structured efficiently and accurately. With live.ts@v1, you'll be able to take your web development to the next level and build high-performance applications that deliver the best possible user experience.

## Further details

Check the [Client-side loaders invocation](https://www.deco.cx/docs/en/tutorials/client-side-invocation) documentation for more information.

# Coming soon

We're excited to share with you some of the upcoming features that are in our roadmap:

1. **Durable workflows** - Developers will be able to create workflows as simple functions that are executed in a reliable and durable way. This allows you to create long-running persistent workflows that can survive failures and continue from where they left off. Use case: Integrating with e-commerce platforms like VTEX, where orders can be received and sent to an ERP even if there are system failures.
2. **Type extensions** - You'll be able to write simple functions that extend an existing type without changing your source code.
3. **Secrets storage** - You'll be able to store and use your secrets with confidence, and use them at runtime without compromising the simplicity of running your code locally.
4. **Indexed storage for document collection** - Create your own database API that allows you to create your own data types, store, read, search, and much more! Use case: A blogger wants to create their own blog platform with custom data types and advanced search capabilities.
5. **Dynamically importing blocks** - Add new features to your store without touching any line of code by importing existing blocks from the community and other sites. Use case: A developer wants to add a new payment gateway to their e-commerce store without modifying the existing codebase.
6. **Extend your admin with dashboards** created by developers from the community. Use case: A company wants to track their sales metrics and inventory levels with a custom dashboard created by a third-party developer.
7. **Flawless onboarding with a self-service UI to create your stores** - Simplify the onboarding experience for your users with an intuitive UI that guides them through the process of creating their own store, without requiring any technical knowledge. This is especially useful for sites built with the community-maintained components.
8. **ChatGPT-based suggestions** for your sections, landing pages, images and texts, audience segmentation and more - Use the power of AI to improve the quality and relevance of your content. ChatGPT can provide suggestions for various elements of your website, such as the layout of your landing pages, the images you use, and the messaging you use to target different audience segments. This can help you create more personalized experiences for your users and improve overall engagement.
9. **Inline editing through UI**: This is a giant unlock for us, by enabling business users to easily customize their store's sections and components by clicking on visual elements and editing their properties. With this feature, business users can quickly see how their changes affect the layout and appearance of their store, making it easier to fine-tune and optimize their design.

We are absolutely thrilled to bring all these exciting new features to our users! Our team has been working tirelessly to make sure these enhancements are not only innovative and cutting-edge, but also easy to use and seamlessly integrate with your business processes. We can't wait to see what you create with these new tools and look forward to continuing to improve and evolve our platform to meet the needs of our users. Stay tuned for more updates and announcements!

# Migrate your site now

[Migration Guide](https://www.deco.cx/docs/en/migration-guides/v1.x)
