## Sentry Clone

This repo is intended to be my own personal sentry clone, but I'm leaving it public both for inspiration to others, and as a starting point if you decide to use this project yourself.

## Installing

### WIP
Actual instructions will be written once there's more to these services than just some boilerplate stuff. For now I'm assuming you have a working (nightly) toolchain for Rust, and a working toolchain for JS projects, so to run the projects, populate any `.env` files and run these commands:

```
# UI

# First run
yarn && yarn serve

# after
yarn serve

# API
cargo run

# Or if you have `cargo-watch` installed
cargo watch -x run
```



## Features (Intended)
**UI**
1. Vue + TS based UI
2. 99% GraphQL data layer, might use standard REST for auth
3. Served by Netlify
4. Stretch goal: Service uptime/health monitoring

**Auth Service**
1. Rust + Rocket?
2. REST interface
3. Diesel + Postgres DB?
4. Act as middleman to authenticate Error Logger and future services

**Error Logger Service**
1. Rust + Rocket based API
2. Juniper integration for GraphQL layer
3. MongoDB
3. Hosted on GCP or Linode, not super sure yet
4. Stretch goal: alternate REST layer for clients where GQL is not an option (think MQTT clients/brokers)

## MVP Features
All of the above with auth baked in to error logger service


## Why are you making this?
To be quite clear, if you're looking for something with zero config, an "it just works" mindset, and you don't care about experimentation at all, just use [sentry](sentry.io) and save yourself some trouble. There's even a self hosted option if you're looking for that.

However, I've realized over my years as a developer that a centralized, semi-opinionated error logger is very nice to use. And while I'm not sure how feature packed the finished product will end up being, it should form a nice alternative to other error logging solutions for my purposes.

That and I'm looking for a useful project to expand my experience and get me out of a hobby project rut ;)

## Contributing
While I'm not building this with collaboration in mind, feel free to fork this and 
