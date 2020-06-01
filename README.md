photo-blog
==========

A general-purpose remote photo documentation application.

This is a follow-along tutorial project motivated by my work at SIL International.

Read more at https://whatdandoes.info/2020/06/01/Simple-Photo-Blogging-for-Partnership-Development/

Tutorial exercises and their solutions can be viewed in the project branches.

# Setup

Clone and install:

```
cd photo-blog
npm install
```

# Test

Start a MongoDB development server:

```
docker run --name dev-mongo -p 27017:27017 -d mongo
```

I use `jasmine` and `zombie` for testing. These are included in the package's development dependencies.

Run all the tests:

```
npm test
```

Run one set of tests:

```
NODE_ENV=test npx spec/models/agentSpec.js
```

## Development

Start a MongoDB development server:

```
docker run --name dev-mongo -p 27017:27017 -d mongo
```

Once created, you can start and stop the container like this:

```
docker stop dev-mongo
docker start dev-mongo
```

Seed database:

```
node seed.js
```

Start `maildev`:

```
docker run -d --name maildev -p 1080:80 -p 25:25 -p 587:587 djfarrelly/maildev
```

Run server:

```
npm start
```



