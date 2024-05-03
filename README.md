## streaming-avatar

## Introduction

This HeyGen Streaming Avatar SDK provides a convenient way for developers to better interface with HeyGen's Streaming Avatar. 

## Installation 

```
npm install @heygen/streaming-avatar
```

To build and compile the typescript sources to javascript run install then:
```
npm run build
```

## Basic Usage

For an indepth demo, please refer to our Streaming Avatar SDK demo. 

```
import { Configuration, NewSessionData, StreamingAvatarApi} from 'streaming-avatar';

const streamingAvatar = new StreamingAvatarApi(
      new Configuration({apiKey: 'ENTER_API_KEY_HERE'})
    )

async function main(){
    await avatar.current.createStartAvatar(
      { newSessionRequest: 
        { quality: "low",
          avatarName: avatarId, 
          voice:{voiceId: voiceId}
        }
      });
}

main();

```

## Troubleshooting FAQ

### How do I get an API Key?

Either an an API Key or Trial Token from HeyGen is required to run this Streaming API demo. API Keys are reserved for Enterprise customers, whereas both Creator and Teams plan users can activate and use a Trial token. You can retrieve either the API Key or Trial Token by logging in to HeyGen and navigating to this page in your settings: https://app.heygen.com/settings?nav=API

### Which Avatars can I use with this project?

By default, there are several Public Avatars that can be used in Streaming. (AKA Streaming Avatars.) You can find the Avatar IDs for these Public Avatars by navigating to app.heygen.com/streaming-avatar and clicking 'Select Avatar'.

In order to use a private Avatar created under your own account in Streaming, it must be upgraded to be a Streaming Avatar. Only 1. Finetune Instant Avatars and 2. Studio Avatars are able to be upgraded to Streaming Avatars. This upgrade is a one-time fee and can be purchased by navigating to app.heygen.com/streaming-avatar and clicking 'Select Avatar'.

Photo Avatars are not compatible with Streaming and cannot be used.

### Which voices can I use?

Most of HeyGen's AI Voices can be used with the Streaming API. To find the Voice IDs that you can use, please use the List Voices v2 endpoint from HeyGen: https://docs.heygen.com/reference/list-voices-v2

### Why am I encountering issues with testing?

Most likely, you are hitting your concurrent session limit. While testing the Streaming API, your account is limited to 3 concurrent sessions. Please endeavor to close unused Streaming sessions with the Close Session endpoint when they are no longer being used; they will automatically close after some minutes.

You can check how many active sessions you have open with the List Sessions endpoint: https://docs.heygen.com/reference/list-sessions
