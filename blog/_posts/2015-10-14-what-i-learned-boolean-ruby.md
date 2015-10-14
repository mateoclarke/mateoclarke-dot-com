---
layout: post
title: What I Learned Yesterday - Booleans have no natural ordering in Ruby
---

*Every day at AcademicWorks, the Engineering Team has a Dev Sync where we share something we learned from the day before. Here is what I learned yesterday...*

## So I wanted to sort stuff in Ruby

Say I have a list of books that a user likes and I want these books listed out in a table. But we also happen to know which of these books is the user's absolute favorite book. That book should be displayed at the top of the list! And fortunately, we have a helper method already defined, `#favorite?`, which returns `true` if the book in question is the user's favorite.

Easy, let's sort our list of books using `book.favorite?`:

```ruby
books.sort_by { |book| book.favorite? }
```

But this returns an error: `ArgumentError: comparison of TrueClass with false failed`

## What I Learned

## More resources
- [Facebook: Official React Tutorial](https://facebook.github.io/react/docs/tutorial.html)
- [Egghead: Build Your First React.js App](https://egghead.io/series/build-your-first-react-js-application)
