# Article Generator API

## Introducing Jaq
The Jaq JavaScript SDK is a collection of useful methods for the [Jaq n Jil](https://jaqnjil.com/) API, which provides professional grade AI-generated articles and content based on specific parameters. 

[Example article output](https://docs.google.com/document/d/1POjt2QoDBVuVZJqCIxjAnjVMYU3SOk3u0AfVd03W7U8/edit?usp=sharing)

![Jaq n Jil Account](https://3056607630-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FRKSU53pkDVshlFgdOIW8%2Fuploads%2FWIbRVoducdB5wo3IF09b%2Fimage.png?alt=media&token=8abeeda2-5f38-4c2d-a371-80174eb7d8ef)

## Getting your API key
Sign up for a free demo of [Jaq n Jil app](https://alpha.jaqnjil.com/) and locate your API key on your account page:

## Installation & Usage

Install via NPM library:

```
npm install jaq-sdk
```

```
import { Jaq } from './Jaq.js';

const apiKey = 'YOUR_API_KEY';
const jaq = new Jaq(apiKey);

const queryObject = {
  topic: 'artificial intelligence', // This is the only required property
  audience: 'content marketers',
  angle: 'how to use AI to improve workflow',
  outline: 'what is ai?\nhow does ai work?\nhow can ai help you?\nhow to use ai to improve workflow',
  introduction: '', // Jaq will assume parameters if they aren't provided
  callToAction: 'join our newsletter',
};

async function generateArticleSDK(queryObject) {
  try {
    const article = await jaq.generateArticle(queryObject);
    console.log(article);
  } catch (error) {
    console.error(error);
  }
}

generateArticleSDK(queryObject);
```
