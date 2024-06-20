# Curls

![](https://i.imgur.com/frdOwf4.gif)

![](https://i.imgur.com/7XDM7Zs.gif)

![](https://i.imgur.com/w7bW8K9.gif)

This is a text status host.

Users claim a `curl` and get a key to be able to update it.

For instance `https://curls.website/funone` would return the current content of the `funone` curl.

The response is always pure text, there is no json or anything.

There is no history, or any other features except hosting the current text.

To view and edit a curl there's some html pages available but you are encouraged to use your own tools to view and edit.

Edit:

```
curl -X POST -d "curl=mycurl&key=mykey&content=mycontent" https://curls.website/edit
```

View:

```
curl https://curls.website/[curl]
```

Get data of one or more (json response):

```
curl -X POST -d "curl=somecurl&curl=othercurl" https://curls.website/curls
```

---

## Intended Use

How I think this can be used is by users sharing their curls to others and then they add them to a program. The program would update every added curl every 5 minutes to check for changes. So a user gets an overview of the status of many people.

The status of the people you choose can serve as calls of action or to know about interesting activities happening in real time.

Yes it's similar to Twitter except there's no history or other kind of privacy invading mechanisms in place. And there's no CORS restrictions, reading and editing the curl status should be as easy as possible, from within any application.

Having lots of these self-hosted is probably best than a big central node, unless that one is well protected against attacks. This doesn't mean this is distributed or anything, each node have their own curls.

---

## Dashboard

I have my own implementation of a program that uses curls.

It is located at `https://curls.website/dashboard`.

---

## Accounts

There are no accounts. You claim a curl once, you are given the key once.

There are no mechanisms to recover a lost key.

---

## Sort

There are 3 sort modes that tell how to sort the items.

### Recent

The most recently updated curls go at the top.

### Order

The curls are ordered based on the order in the `curlist` at the left.

### Alpha

The curls are ordered alphanumerically.