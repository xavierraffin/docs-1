---
title: Writing Your First Snake in Go
permalink: /tutorials/go
layout: card
---

This document will allow you to start developing a Battlesnake snake AI using Golang programming language.

---

## Step 1 - Get started with Gitpod

---

#### Create a GitHub account

GitHub is a platform for storing and managing source code and uses a version control system called Git.

Your snake's source code will be stored on GitHub. It will be publicly available and will stay around for you to use at future events.

Go to https://github.com/join to create an account, and choose the free option.

---

#### Fork the starter snake repository

Forking a GitHub repo lets you copy source code from an open source project to your own GitHub repo.

There is a repo that contains example Golang code to run a very basic battle snake, and you can fork it here: https://github.com/battlesnakeofficial/starter-snake-go/fork

---

#### Start Gitpod

Gitpod will set up your development environment, and host your application. You just need to tell it which GitHub repo to connect to.

Put your github username into the following url instead of `<your-username>`, and go to it.

gitpod.io/#github.com/`<your-username>`/starter-snake-go

You'll need to be logged into GitHub with the same username, and give it permission to your account.

---

#### Start your snake

Once you're in Gitpod, you can run the starter snake. Type `make run` in the terminal console and hit enter.

It will tell you that an application is running on port 9000, and show a button that says `Open Browser`. Hit that button and copy the URL that it goes to. You'll need that later; it is the URL of snake.

---

## Step 2 - Create a battlesnake game

---

#### Add your snake

Now that the starter snake is running, you can put it in the ring!

Go to play.battlesnake.com, go to `My Snakes` (log in with your GitHub), and `Add a Snake`. Choose your name, and use the URL from step 1.4.

---

#### Create a game

on play.battlesnake.com, go to `Create a game`. On the field `Add snakes to the pit`, search for the snake name you just made and click `Add`. You can add other snakes too.

click `Create Game` and it will go into the player. At the bottom of the player, hit `play`. Your snake should go straight to the bottom, since that's all the starter snake knows how to do.

---

## Improve your snake

Now you can make your AI snake do something more intelligent!

---

#### Modify some code

Look around the code to see what's going on, or get someone to help explain it. We'll go through a simple example of what you can change, but the rest is up to you.

Go back to your Gitpod workspace (or find it again at gitpod.io), and open the `routes.go` file. It handles each of the requests that the gameplay server can initiate.

The most important one is `Move()`, and right now it always returns a response with `Move: "down"`. We're going to change it to something slightly more complex:

```
func Move(res http.ResponseWriter, req *http.Request) {
	decoded := api.SnakeRequest{}
	err := api.DecodeSnakeRequest(req, &decoded)
	if err != nil {
		log.Printf("Bad move request: %v", err)
	}
	dump(decoded)

	moveDirection := "left"
	yourHeadCoord := decoded.You.Body[0]

	if yourHeadCoord.X < 3 {
		moveDirection = "up"
	}
	if yourHeadCoord.Y < 3 {
		moveDirection = "right"
	}
	if yourHeadCoord.X > 8 && yourHeadCoord.Y < 8 {
		moveDirection = "down"
	}
	if decoded.Turn > 100 {
		moveDirection = "left"
	}

	respond(res, api.MoveResponse{
		Move: moveDirection,
	})
}
```

---

#### See it in action!

In the terminal, cancel the last `make run` command by hitting ctrl-c. Then start `make run` again. Now it will be running the new code.

In play.battlesnake.com, hit the back button to go back to `Create Game` and run it with your snake in the ring again. Now it should be doing something slightly more interesting.

---

#### Save your changes

To keep your changes on your GitHub repo, you'll need to commit and push the changes.

Git can be a bit complex to learn at first, but we'll do a simple example. Run these in a Gitpod terminal (make sure it's not a terminal that is already running your snake):
```
git add .
git commit -m "Make the snake spin"
git push
```
(You can make your own commit message in the double quotes)

You will need to give additional permissions to Gitpod so that it can write to your repo. Then run `git push` again.

---

## Get competitive!

Keep repeating step 3 with your own changes until you have the best snake!

When a tournament starts, make sure your Gitpod workspace is running. It will timeout after 30 minutes of inactivity (10 minutes if you close the window), and you will have to start it again. If it stops when a game is started, your snake will not respond and lose immediately!
