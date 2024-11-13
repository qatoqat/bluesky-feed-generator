# Bookmark Feed Server

## Setup

Install uv and sync:
```shell
pip install uv
uv sync
```

## Publish feed

Open `publish_feed.py`, fill in the variables.

### Run server

Copy `.env.example` as `.env`. Fill the variables.

> **Note**
> To get value for "BOOKMARKS_URI" you should publish the feed first. 

Run development flask server:
```shell
flask run
```

Run development server with debug:
```shell
flask --debug run
```
> **Note**
> Duplication of data stream instances in debug mode is fine. 
> Read warn below.

> **Warning**
> In production, you should use production WSGI server instead.

Endpoints:
- /.well-known/did.json
- /xrpc/app.bsky.feed.describeFeedGenerator
- /xrpc/app.bsky.feed.getFeedSkeleton

### License

MIT
