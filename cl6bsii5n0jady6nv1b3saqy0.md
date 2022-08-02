## Create a portfolio : 2023 Edition

Hello 👋,

As a developer, you need to have a portfolio to show many things :

- What can you do ? 
- What do you like ?
- Which projects did you realize ?
- How to contact you ?

To answer these questions, a simple website can be enough. But, to make the difference, you can optimize your website with several ways !

## ⚙️ Use a well known framework

In my case, I love React. 

So I'm using a well known React framework called [Next.js](https://nextjs.org/) (maintained by Vercel). I'm using it for many reasons, but the main reason is how it manages rendering and do optimizations. I can strongly advise you to check their [documentation](https://nextjs.org/docs/basic-features/data-fetching/overview) on SSR / SSG / ISR / CSR. 

To handle design, I'm using [TailwindCSS](https://tailwindcss.com/) especially for his simplicity and optimizations from PostCSS.

## ⚡ Focus on speed

A portfolio need to be consulted everywhere, on a train, on a subway, at home, at office, etc. 

As Google recommends, **your website need to be around 500 KB**. It's very small but to give you an example, a page with **1.49 MB need 7 seconds on a fast 3G network** to download and consult.

So you need to use as much as possible to use SVG or WebP and compress it if it is possible. On Next.js, you can generate WebP on the fly with [next/image](https://nextjs.org/docs/api-reference/next/image#required-props).

You can use a CDN to make your website faster across the world. Personally, I use [Vercel](https://vercel.com/) who have this feature.

![Screenshot_2022-07-19_08-15-12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659420422271/noilmmdHa.png align="left")

## 🖥️ Focus on SEO

SEO or Search Engine Optimization is a complicated term to signify a simple thing. How can you optimize your website to be sure that your website will be displayed on Google / Bing / etc.

It doesn't exist a secret formula because everything is opaque, but there are some common things to do :

- Generate Meta tags to help robot indexation ([next-seo](https://github.com/garmeeh/next-seo))
- Respect h1, h2, h3 order 
- Have a domain with your first name and last name and keep it as long as possible
- All your IMG tags need to have an alt attribute

You can use several tools who will help you to optimize your websites :

- Meta tags : [https://metatags.io/](metatags.io)
- SEO : [https://web.dev](web.dev)

## 💬 Translate your websites

In my case, I'm a French developer. So I need to translate my website in French but in English too.

Why ? 

- To be seen by French recruiter for local jobs
- To be seen by International recruiter for local or full-remote jobs

Stupid things, but very important to maximize your chances for your next opportunity !

## 🤖 Make your website automated

I have always heard that developer are lazy people. I can confirm, it is true !

Why did you need to develop a new website (and lose time) every time you create a new project, you publish a new article, you have been hired to a new company ?

I'm a strong fan of [Notion](notion.so/). I'm using it for my personal projects and professionally. 

I have recently seen that is it possible to use Notion as a CMS (Content Management System). 

So for each dynamic part, a Notion page have been created and with Next.js, I refresh and redeploy my website every 10 minutes to refresh changes with [ISR](https://nextjs.org/docs/basic-features/data-fetching/incremental-static-regeneration).

For me, dynamic part are :
- Experiences
- Diplomas
- Projects
- Tools
- News (For this, I'm using [Hashnode API](https://catalins.tech/hashnode-api-how-to-display-your-blog-articles-on-your-portfolio-page))

In automation, **I have pushed the limit further with resume generation**. On my website, you can download my Resume in PDF, who will be generated from Notion data.

## 📃 Bonus : Open source your website

As a developer, open source is very important because every library we used is developed by community and can be freely edited or used.

To make development less shady, I can encourage you to make your code freely accessible to share your knowledge with everyone. 

Maybe some developers will see some issue with your code or will see some language issue and can summit a merge request. 😊

## 🥳 A working example

I have recently updated my website to enter 2023 year ! 

You can consult it on [https://qlaffont.com](qlaffont.com) and the entire code can be consulted it on [Github](https://github.com/qlaffont/qlaffont-website/). 

You can duplicate my Notion pages if you want too !

Have fun and let's code ! 🧑‍💻
