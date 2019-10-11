---
title: What is Exosuit?
---

Exosuit was born out of my desire to make deploying Rails to AWS
as easy as deploying Rails to Heroku.

## What's wrong with deploying Rails with Heroku?

A lot of the time, nothing. Heroku is great for a lot of cases.
I've used Heroku for Rails deployment many times in the past
and I expect to use it many times in the future.

But sometimes, for whatever reason, you can't or don't want to use Heroku.

These reasons include, but aren't necessarily limited to:

- You don't want to pay Heroku's fees
- You want fine-grained control over your infrastructure
- You want to gain practice using AWS directly to build your career skills
- You're running an application that needs HIPAA compliance

Unfortunately, if you give up Heroku, it's a long drop to bare AWS, with a hard landing.

## What's so bad about Rails + AWS?

In my experience, deploying a Rails application to AWS is a huge fucking pain in the ass.
AWS's own documentation is pretty hard to understand.
The blog posts online explaining how to deploy Rails to AWS are frequently
incomplete, out of date, or just plain incomprehensible.

I've deployed Rails applications to AWS several times and each time it took
several hours of frustrating, mentally taxing effort.

As I see it, there's no reason things must be this way!
Why can't there be a tool that makes Rails + AWS deployment
about as easy as Heroku deployment?

## The dream

Below is how I intend Exosuit to work.
I intend and expect that the grand total time between
step 1 and step 5 is about five minutes.

**Step 1**: `cd` into your Rails project directory.

```shell
$ cd my_rails_project
```

**Step 2**: Install the Exosuit CLI tool.

```shell
$ brew tap jasonswett/exosuit && brew install exosuit
```

**Step 3**: Create your Exosuit app.
This will register your app with Exosuit, a necessary prerequisite to step 4.

```shell
$ exo create
```

**Step 4**: Do a `git push` which will automatically
initialize your production server,
create a database instance and deploy your application code.

```shell
$ git push exosuit master
```

**Step 5**: Visit your fully working production application, live on the internet.

```shell
$ exo open
```

## Want to try it out?

Exosuit doesn't do all this stuff yet but it does some of it.

Visit the
[Getting Started with Exosuit]({% link getting-started.md %}) guide
to see exactly what Exosuit can do right now.
