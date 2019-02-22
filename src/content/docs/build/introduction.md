---
title: Introduction to Skills
layout: onboarding.hbs
columns: two
order: 1
---

# {{title}}

This page provides a high level overview of developing skills for Misty. It describes how Misty works with your code and explores how coding a robot is different from developing for mobile or the web. Finally, it provides guidelines for sharing skills and collaborating with other devlopers in the Misty Community Skills GitHub organization.

## Understanding Misty's Skills

Applications you develop for the Misty platform are called **skills**. When you write a skill for Misty, you:

1. take some of Misty's sensory data
2. process that data using Misty's API or send it off to a cloud service
3. have Misty do something in response

For example, you might write skills to have Misty do the following:

* roam your office and greet people she recognizes
* respond with movement and sound when you touch her head or chin
* deliver an object to someone specific

The first step in writing a skill for Misty is deciding what you want the skill to do. Then you can choose to write the skill using Misty's on-robot JavaScript API, her REST API, or a combination of the two. Once written, you can share your skill with other Misty developers on GitHub.

## Using Misty's APIs

There are two main methods you can use to write skills for Misty.

* Use Misty's on-robot JavaScript API to write code that runs internally on Misty.
* Use Misty's REST API to write code that runs on an external device to exchange data and commands with Misty over your local WiFi network.

While Misty's on-robot JavaScript and REST APIs include many of the same commands, they differ in architecture and implementation. Understanding these differences will help you choose which method to use.

### Misty's On-Robot JavaScript API

Code that you write with Misty's on-robot JavaScript API runs internally on the robot. When you use the on-robot JavaScript API, you write your JavaScript code on your computer. Then you upload this code to your robot alongside a `.json` file with rules that define how Misty should execute the code. Learn more about file structure and code architecture [here](../../../docs/build/local-skill-architecture/#file-structure-amp-code-architecture).

Misty's JavaScript engine supports most features of ES6 available in modern web browsers. Note, though, that when you write JavaScript to run on Misty's, there is no [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) for your code to manipulate.

The syntax for using a command in Misty's JavaScript API is:

```JavaScript
misty.<COMMAND>(parameters);
```

So, for example, to change the color of Misty’s logo LED, you would call the `misty.ChangeLED()` command like this:

```JS
misty.ChangeLED(255, 0, 0);
```

In addition to methods for using Misty's robot capabilities, the on-robot JavaScript API includes methods for:

* sending debug messages
* saving data to Misty
* handling data from sensor and skill events
* controlling the flow of your code's execution
* sending external requests to third party web APIs
* starting and stopping the execution of other JavaScript code files on Misty

See the [On-Robot JavaScript API reference documentation](../../../docs/reference/javascript-api) for the full list of commands.

#### When Should I Use Misty's On-Robot JavaScript API?

When you use Misty's on-robot JavaScript API, commands are not sent to your robot over an internet connection. This means you can expect Misty to respond to commands immediately after they execute in your code. This is different from using Misty's REST API, where you can expect some lag between executing a command and seeing Misty respond.

Consider using Misty's on-robot JavaScript API when

* you need Misty to respond to commands immediately after they execute in your code
* you want Misty to be able to run a skill even when she doesn't have a connection to the internet
* you are writing a skill that does not require input from a keyboard or a mouse

### Misty's REST API

You will learn about what you should consider when you're programming a robot

Coding a robot: general

Coding a robot: Misty-specific

How to send code to Misty



* Skill Runner uses the endpoints from Misty's REST API for uploading and managing skills. Skill Runner is the tool we provide for developers who are working with Misty, but if you have other ideas for an interface for uploading and managing on-robot code, we encourage you to do so!

Misty has two basic types of skill architecture. You can write skills using Misty's on-robot JavaScript API, or you can use her REST API.

When you write a skill using Misty's [on-robot JavaScript API](../../skills/local-skill-architecture), you upload your code to the robot and it runs internally on Misty. This differs from writing a skill with [Misty's REST API](../../skills/remote-command-architecture), where your code runs on an external device (say, in desktop browser or on a Raspberry Pi) and not onboard the robot.

## More high level information about skill development

- Includes more high-level information about the  differences between the two architectures

### Something else that's probably good to know

- Describes how architectures can be used together

### Even more helpful content

- Suggest which architecture to use based on your goals

## Sharing Skills

Once you've written a skill, we encourage you to share your work to the [Misty Community Skills GitHub](https://github.com/MistyCommunitySkills) organization.

*More information about skill sharing*
*More information about skill sharing*
*More information about skill sharing*
*More information about skill sharing*
*More information about skill sharing*
*More information about skill sharing*

You can also find helper libraries, code samples, wrappers, and other useful tools for skill development in the [Misty Community](https://github.com/MistyCommunity) GitHub organization.

*More information about libraries, code samples, and wrappers*
*More information about libraries, code samples, and wrappers*
*More information about libraries, code samples, and wrappers*
*More information about libraries, code samples, and wrappers*
*More information about libraries, code samples, and wrappers*