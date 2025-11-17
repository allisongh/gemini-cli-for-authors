# Project overview: Quickstart documentation for Gmail API

## Documentation goals

   1. **Audience:** Gmail API developers. For this project, assume the audience
      primarily codes in Python.
   2. **Goal:** Quickstarts help users immediately get familiar with using a
      product or API feature. These task-based guides should be short (~15min to
      complete). By the end, the developer should have a "Hello world!"
      experience where they've accomplished something, such as successfully called
      an API method.
   3. **Architecture:** The Gmail API's quickstart documentation is published to
      https://developers.google.com/workspace/gmail/api/quickstart. Each quickstart
      gives an example in just one programming language.

## Style guidelines

Your content **must adhere** to the style guidelines
provided in Google's developer documentation style guide
(https://developers.google.com/style).

Before you author any content, you must use review the guidelines
published to the complete site at https://developers.google.com/style.
To access these pages, use your built-in `web_fetch` tool.

### Additional guidelines for writing documentation

When you write content, make sure you follow the following rules:

* **Markdown format:** Format all content in markdown. All lines, including
  code blocks and strings must not exceed 80 characters.
* **Accuracy**: If you can't verify the accuracy of a step or information that
  you generate, add a TODO() marker for the user to verify it and test it after.
  For any code samples you created, you should add `TODO(Test code sample)`.

## Doc template

Below is the heading template you should follow for any quickstart document:

```
# Title (Such as "Python quickstart")

## Objectives

## Prerequisites

## Set up your environment

### Enable the Gmail API

### Configure the OAuth consent screen

## Prepare the workspace

## Set up the sample

TODO(Test code sample)

## Run the sample

```
