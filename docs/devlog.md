# Alright

So here's the deal.

I've probably built somewhere on the order of... 30 personal blog/portfolios over the years.

Almost every time, I use it as a way to test out new tooling.

The first one I ever built was a straight up HTML site on a LAMP stack, I think? The last few have all been some flavor of React and usually Next.js.

Now, I work in React and Next every day. As a seasoned frontend dev, that's my comfort place. It's a one-liner to spin up a site that's pretty good in those. But where's the fun in that? Where's the ambition, the excitement that comes from just... developing? It hits pretty hollow if you ask me.

On top of that, as of two days ago the minimum hello world Next.js app comes in at 86kb of shared JS, even fully RSC-driven (literally just a page in the app folder with ye olde `<div>hello world</div>`). Now I'm not the kind of twat to sit around and doomsay around the JS ecosystem and how big 86kb is. Next is a workhorse. It gets a lot of shit done in that 86kb, and is a foundation for a hell of a lot more.

That said, it's definitely far from necessary for a static blog.

But I'm also not building a static blog. Maybe this starts as a static blog--that seems like a good first step and all.

The idea is to go further than that though. And again, the point of this project isn't to build a blog. It's to have some fun. I work with Next every day at work, but how often do I write zero-dependency JS/TS? Not every day, that's for sure.

## init

Alright, so step one was straightforward. I'm somewhat limiting my tooling here. And by somewhat I mean:

- aiming for zero production dependencies: html, css, and JS
- allowed to use tooling for development, but try to do things myself
- will likely deploy to Cloudflare, maybe consider Hono
- will see how it goes to just use Bun to handle basically everything else

That means getting started is easy. There are plenty of fun things I'd like to write myself, but scaffolding another package is not one of them.

`bun init` it is.

Cool, that got us started with a basic repo structure, a neat package.json, TS support with some fairly strict (but not crazy) config setup, and all of the other lovely things Bun does for us.

## HTTP server

Okay, let's start with a simple HTTP server.

Bun does the heavy lifting here, and while writing a server is fun, it's not a goal for this project. So we'll start with just what we've got out of the box with Bun and if we need to implement anything custom, we'll take it from there.

A simple HTTP server out of their docs is ez pz. Copying that and a little `bun run api/index.ts` and we're off with some hello world endpoints!

## File-based routing
