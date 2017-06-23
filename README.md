# Approval extension

[https://www.contentful.com](Contentful) is a content management platform for web applications, mobile apps and connected devices. It allows you to create, edit & manage content in the cloud and publish it anywhere via powerful API. Contentful offers tools for managing editorial teams and enabling cooperation between organizations.

This extension provides a simple Approval checkbox. When unchecked the entry is unpublished. You can use this extension with 'Boolean' field types.

## Requirements

All the samples require the following dependencies:

### Contentful

- a space to use the widget and the space id.
- an API key for Contentful's Mangement API.

### Local machine

- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/) installed and configured for dependencies management.
- You will need to set [your management API token](https://www.contentful.com/developers/docs/references/authentication/) and install the dependencies for the extension:

```bash
export CONTENTFUL_MANAGEMENT_ACCESS_TOKEN=<content-management-access-token>
npm install
```

## Getting started with local development

Install the dependencies needed with `npm install` or `yarn`.

Create the extension on Contentful:

```bash
contentful-extension create --space-id <space-id>
```

Serve on _<http://localhost:3000>_ using Gulp, automatically watching and reserving any changes:

```bash
gulp watch
```

## Debugging on your local environment

As the Contentful web app is served over HTTPS but your local machine is likely HTTP, you will need to enable access to insecure content.

Read how to do that in [Firefox][ff-mixed] and [Chrome][chrome-mixed].

[chrome-mixed]: https://support.google.com/chrome/answer/1342714
[ff-mixed]: https://support.mozilla.org/en-US/kb/mixed-content-blocking-firefox

## Using the extension in production

To minimize all dependencies and upload the extension to Contentful:

```bash
gulp bundle
contentful-extension update --srcdoc ./dist/index.min.html --force --space-id <space-id>
```

## TODOs

