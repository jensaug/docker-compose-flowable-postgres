# docker-compose-flowable-postgres

## What?

This is a minimal repo based on the *Docker* section of http://www.flowable.org/downloads.html.

It provides the flowable all-in-one with a persistent postgres backend for local use.

That's it.

## How?

1. Clone this repo. `cd` into it.
2. You'll need `docker-compose` and some sort of `docker` installed. The officla GUI *Docker For Mac* is easiest for these purposes, but if you're a Casebook engineer you may already have `docker-machine`, which would complicate these instructions because it doesn't run services on `localhost`.
  > *tl;dr:* use *Docker for Mac* and `brew install docker-compose` if necessary.
3. Run `./flowable start`
4. First time running? Wait a few minutes for everything to download ad start for the first time. Otherwise, just give it a minute. You can check on how things are doing by running `./flowable info` (Control-C to exit).
5. Visit `localhost:8080/flowable-idm`
6. Want to see where the services are running? `docker-compose ps`
7. Want to stop it? `./flowable stop`

Your data will still be there next time you start. It's stored in a `flowable/` directory in your home directory.
