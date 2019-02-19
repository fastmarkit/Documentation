---
title: Introduction to Skills
layout: onboarding.hbs
columns: two
order: 1
---

# {{title}}

Welcome! On this page

Here you will learn about skill development and the different methods you can use to code Misty. You will learn how Misty works with your code and you'll understand what makes coding a robot different from other kinds of software development. You will also be introduced to the GitHub repositories set up for skill and tool sharing.

## What's a Skill?

A skill is code you write to make Misty do something. Most skills involve some combination of the following:

1. take some of Misty's sensory data
2. process that data using Misty's API or send it off to a cloud service
3. have Misty do something in response

You write skills for Misty using her on-robot JavaScript API, her REST API, or both. Code that you write with Misty's on-robot JavaScript API runs internally on Misty. Code that you write with Misty's REST API runs on an external device and exchanges data and commands with Misty over your local WiFi network.


## Using Misty's APIs

While Misty's on-robot JavaScript and REST APIs include many of the same commands, they differ in architecture and implementation. Understanding these differences will help you choose which API to use in your skills.

### On-Robot JavaScript API

Code that you write with Misty's on-robot JavaScript API runs internally on the robot. To use this API, you write JavaScript in a text editor on your computer. When complete, you upload the JavaScript code file to your robot alongside a `.json` meta file with rules defining how Misty should execute the code. Learn more about file structure and code architecture [here](../../../docs/build/local-skill-architecture/#file-structure-amp-code-architecture).

The syntax for using a command in Misty's JavaScript API is:

```JavaScript
misty.<COMMAND>(parameters);
```

So, for example, to change the color of Misty’s logo LED, you would call the `misty.ChangeLED()` command like this:

```JS
misty.ChangeLED(255, 0, 0);
```

In addition to commands for controlling Misty's robot capabilities, the on-robot JavaScript API includes methods for:

* sending debug messages
* saving data to Misty
* handling data from sensor and skill events
* controlling the flow of your code's execution
* sending external requests to third party web APIs
* starting and stopping the execution of other JavaScript code files on Misty

See the [On-Robot JavaScript API reference documentation](../../../docs/reference/javascript-api) for the full list of commands.

Misty's JavaScript engine supports most ES6 features you can use with most modern web browsers. Note that when you write JavaScript to run on Misty's, there is no [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) for your code to manipulate.

Because the on-robot JavaScript API are not sent to your robot over an internet connection, you can expect Misty to respond to JavaScript API commands right away. You might use Misty's JavaScript API when you need Misty to respond to commands as soon as they execute in your code

There are many benefits to writing code that can execute entirely on your robot. Consider using Misty's on-robot JavaScript API when you need to execute code in an environment without a reliable internet connection, or when you need Misty to react to commands without any lag time. 

Use the on-robot JavaScript API to write code that runs internally on the robot, and use Misty's REST API to write code that runs on an external device (like a desktop browser or a Raspberry Pi) and not onboard the robot.

You will learn some of what makes coding a robot different from coding other computing devices.

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