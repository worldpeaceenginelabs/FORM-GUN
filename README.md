# FORM-GUN

![image](https://user-images.githubusercontent.com/67427045/174142438-2128bc5a-4284-4ebb-8ed7-a4841873cf8b.png)
<br><br><br>

# HOW TO USE
 
- **npm install (installs the dependencies)**
- **npm run dev (preview and hot module reloading)**
- **npm run build (exports static for CDN)**
<br><br><br>

# Svelte Compiler Tutorial with Gun

Can you code in Javascript/Typescript? Do you want Vanilla JS code at the end without learning it?🤩

You can just drop your JS/Typescript file in the red box, and your HMTL file into the green box. (or split your js page's code into js and html and drop them into the boxes)

I just drop you the screenshot of my typical desktop as a visual helper, because you can just test in Typescript whatever you want, to get a first touch with Svelte instant!

Modify the server, test a new script, test the build and load the static files to a cdn maybe?...

Its a fresh npm create vite@latest, nothing touched but App.svelte and npm install gun
https://github.com/worldpeaceenginelabs/FORM-GUN

I would love to read your feedbacks on how you liked to code in Svelte your first time?
<br>

![image](https://user-images.githubusercontent.com/67427045/176132137-16740536-68b9-482e-b5d7-0b86dbb2f85b.png)

# Why vite@latest instead of sveltejs@latest?

I did research a few month ago, sveltejs vs. sveltekit (the text snippet is good summary of it)

if you use the framework (sveltekit) you get their whatever in your code.
if you use the sveltecompiler(sveltejs) you'll get clean buildfiles in vanillajs.

Especially for decentralized/local first apps, you want to go for sveltejs, which's buildfiles run on browser, edge, everywhere... (jamstack)

The environment after npm install vite@latest (choose svelte/TS in the prompt) has a much better dev experience then npm install svelte@latest (very well pre-configured, npm run build is edge-ready from the start and vite is fast as heck, instant startup with hot-reloading)

---

SvelteKit is built on top of Svelte. Svelte alone is just a frontend compiler. More precisely, Svelte delivers its own JavaScript/TypeScript compiler which generates the client-side JavaScript at build time. This compiled JavaScript is specialized to adapt the DOM in such a way that as little data as possible has to be exchanged between server and client. This has numerous benefits for the user experience.

The kit, on the other hand, thus acts as a full-fledged app framework. This allows us to implement all modern best practices such as server-side rendering (SSR), routing, and so on.

---

PS: but we dont want those best practices, because they are old 😂👍 go for the most modern approach of developing apps, the jamstack https://jamstack.wtf/

No limitations:
https://metaverse-dao.pages.dev/ the webgl globe comes from free Cloudflare Pages (edge) and is hydrated by API from different sources. (one is Gun, the other is Openstreetmaps)
