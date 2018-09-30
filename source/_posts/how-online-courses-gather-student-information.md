---
title: How online courses gather student information?
description: In this post we analyze how three online learning platforms send information related with user learning activity.
---

## Gathering information

The purpose of this post is to see examples of how well-known learning platforms are gathering student information. I wanted to know how other companies were sending this information while I was reading about xAPI. Although there's nothing in this blog about xAPI (yet), I think it's a good starting point to analyze and understand where xAPI can be applied and be useful. You don't need to know much about xAPI to read this post, but if you want to, you can take a look to this [brief overview](https://xapi.com/overview/). Let's highlight the first paragraph:

> The Experience API (or xAPI) is a new specification for learning technology that makes it possible to collect data about the wide range of experiences a person has (online and offline). This API captures data in a consistent format about a person or group’s activities from many technologies. Very different systems are able to securely communicate by capturing and sharing this stream of activities using xAPI’s simple vocabulary.

In this post, I'm going to explore what's behind Udemy, Udacity and Coursera way of getting student information while playing videos. The way I'm checking this is simply by taking a look to the `Network` tab in the browser's devtools, and diving into the different HTTP requests each platform is sending.

We're going to see how each one track the "Play" action:

## Udemy

```javascript
{
  "userId": 1234567,
  "visitorUUID": "5184bda070534f7badb88e6c6874dd34",
  "userType": "Student",
  "courseId": 000000,
  "courseType": "Paid",
  "objectId": 111111,
  "objectType": "Lecture",
  "ctVersion": "1",
  "category": "Video Controls",
  "action": "video play",
  "extra": {
    "dimension2": "videojs Html5",
    "msPosition": 136697.248,
    "userId": 1234567,
    "format": "video/mp4",
    "quality": "720",
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_13_3) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/66.0.3359.139 Safari/537.36",
    "streamType": "NOT-HLS",
    "bytesSecHighestDecoder": 105620,
    "millisSecHighestBandwidth": 102637,
    "cdn": "level3",
    "assetId": 5772772
  }
}
```

As we can see, the action here is defined as **video play**. There are many other actions that can be tracked, such as:

* "video pause"
* "video volume"
* "video seek forward"
* "video hd: 480" *(change video resolution)*
* "video cc: off" *(change video subtitles)*


## Udacity

```javascript
{
  "integrations": {},
  "context": {
    "page": {
      "path": "/courses/cs271/lessons/48688925/concepts/487421730923",
      "referrer": "https://eu.udacity.com/",
      "search": "",
      "title": "Intro to Artificial Intelligence - Udacity",
      "url": "https://classroom.udacity.com/courses/cs271/lessons/48688925/concepts/487421730923"
    },
    "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_13_3) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/66.0.3359.139 Safari/537.36",
    "library": {
      "name": "analytics.js",
      "version": "3.6.0"
    }
  },
  "properties": {
    "conceptKey": "487421730923",
    "courseKey": "cs271",
    "lessonKey": "48688925",
    "concept_title": "Terminology",
    "course_title": "Intro to Artificial Intelligence",
    "lesson_title": "1. Welcome to AI",
    "course_key": "cs271",
    "content_type": "course",
    "version": "1.0.0",
    "locale": "en-us",
    "startTime": 0,
    "endTime": 10.155488,
    "videoDuration": 317.341,
    "durationWatched": 10.155488,
    "playerState": "paused",
    "atomKey": "48742173"
  },
  "event": "Course Video Watched",
  "anonymousId": "37079069-bbe4-4a20-ab33-b904b2d324fa",
  "timestamp": "2018-05-11T17:55:38.742Z",
  "type": "track",
  "writeKey": "u0v6T1NLYy1dJA9tWDSGSyuFolxZEzUp",
  "userId": "1234567890",
  "sentAt": "2018-05-11T17:55:38.744Z",
  "_metadata": {
    "bundled": [
      "AdWords",
      "Blueshift",
      "Google Analytics",
      "Google Tag Manager",
      "Intercom",
      "Segment.io"
    ],
    "unbundled": []
  },
  "messageId": "ajs-db6933ea06339a2f3734aa02745310dc"
}
```

What Udacity is doing is to send a "pause" action with `durationWatched`, `startTime` and `startTime` values, that can be used to know when the user played and paused the video. All of these wrapped in a *event* named **Course Video Watched**.

## Coursera

```javascript
{
  "clientType": "web",
  "app": "phoenix",
  "clientVersion": "{{ WEBPACK_VERSION_PLACEHOLDER }}",
  "events": [{
    "key": "open_course.video.play",
    "value": {
      "open_course_slug": "geospatial",
      "video_name": "Lesson 1 - Lecture 1",
      "item_id": "8xwbQ",
      "item_name": "Lesson 1 - Lecture 1",
      "lesson_id": "gAaTS",
      "lesson_name": "The Changing Nature of Place",
      "module_id": "EOiNh",
      "module_name": "The Changing Nature of Place",
      "timecode": 5.503129,
      "appName": "ondemand"
    },
    "clientType": "web",
    "url": "https://www.coursera.org/learn/geospatial/lecture/8xwbQ/lesson-1-lecture-1",
    "app": "phoenix",
    "referrerUrl": "https://www.coursera.org/learn/geospatial/home/welcome",
    "guid": "12345678-1234-5678-9012-12345678",
    "visitId": "12345679-1234-5678-9012-34567890",
    "screenSize": {
      "height": 900,
      "width": 1440
    },
    "clientVersion": "{{ WEBPACK_VERSION_PLACEHOLDER }}",
    "clientTimestamp": 1526061514664,
    "sequence": 3571
  }]
}
```

In this last example, they're sending a **"open_course.video.play"** event, along with similar information as the previous examples.

## Conclusion

As we can see, all of these platforms have in common that they send, in this particular example, video interaction events to a server. They're sending the same kind of information, but they're using completely different structures. This is where xAPI comes into play: xAPI specification tries to provide a common way to send, store and understand student interaction.

If you'd like to see how this information could have been sent using xAPI, I'm writing a post about it that will be available soon.
