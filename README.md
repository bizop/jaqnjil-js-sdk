#Article Generator API
##Introducing Jaq
The Jaq JavaScript SDK is a collection of useful methods for the  API, which provides professional grade AI-generated articles and content based on specific parameters. 
 
##Getting your API key
Sign up for a free demo of  and locate your API key on your account page:
Get your API key on your "My Account" page

##Installation & Usage

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
