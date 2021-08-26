# GSOC-2021-Work-Report
![GSoC logo](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-logo-horizontal.svg)
<h3 align='center'> Project Sponsered By Rocket.Chat </h3>
<p align="center">
  <img src="https://media.glassdoor.com/sql/2244250/rocket-chat-squarelogo-1581602649406.png">
</p>

# Project: Introduce Video Call To Livechat

| **Student** | Deepak Agarwal |
|:---|:---|
| **Organisation** | [Rocket.Chat](https://rocket.chat/) |
| **Project** | [Introduce Video Call To Livechat](https://docs.rocket.chat/contributors/google-summer-of-code/google-summer-of-code-2021) |
| **GitHub** | [@Deepak-learner](https://github.com/Deepak-learner) |
| **Linked In** | [Deepak Agarwal](https://www.linkedin.com/in/deepak-agarwal-9662ba186/) |
| **Email** | <a href="mailto:deepak710agarwal@gmail.com">deepak710agarwal@gmail.com</a> |
| **Website** | [https://deepak-learner.github.io/portfolio/](https://deepak-learner.github.io/portfolio/) |

## About Me
I am Deepak Agarwal, a pre-final year (was a sophomore when started GSoC) B.Tech Information Technology student at Vellore Institute of Technology (VIT, Vellore). Feel free to contact me on any of the contact information mentioned above.

## Mentors:
Special thanks to my mentors for always being there when I need them. I will always be thankful to you. During this program, I get to learn many new things from you guys. Under your guidance, I was always on the right track and able to deliver this project successfully in the end. Looking forward to working with you guys again in future. 

+ **Murtaza Patrawala**&nbsp; &nbsp;[GitHub](https://github.com/murtaza98) &nbsp; [LinkedIn](https://www.linkedin.com/in/murtaza-patrawala-b17419166/)
+ **Gabriel Henriques**&nbsp; &nbsp;[GitHub](https://github.com/gabriellsh) &nbsp; [LinkedIn](https://www.linkedin.com/in/gabrielschnorr/)

## AIM
- Integrate Video call functionality between agent in omnichannel and visitor in LiveChat widget.

- Implementing the Slack-like feature to show call notifications, call records with duration, call ended time etc.right in chat window at agent side (omni-channel) and at visitor side in livechat widget.

- Along with video call with agent, visitor should also have option to chat with agent on the same window.


## A BRIEF OVERVIEW OF MY WORK

### Community Bonding Period
- Explored the different aspects of RocketChat codebase. This project involves work with three repositiory of Rocket.Chat: [Rocket.Chat](https://github.com/RocketChat/Rocket.Chat), [Rocket.Chat.Livechat](https://github.com/RocketChat/Rocket.Chat.Livechat) and [Rocket.Chat.SDK](https://github.com/RocketChat/Rocket.Chat.js.SDK). So, utilize this time to explore and get familiar with codebase. 
- Expanded my knowledge more on Livechat codebase, its APIs and their integration methods, MeteorJS framework, NodeJS functions and mongoDB all of which helped me in achieving my target efficiently.
- Discuss the architecture with mentors to be followed for this project.

### Work Done at Live Chat Widget:
- Add Call Notification and Video call: When agent initiates webrtc call, I add the call notification trigger at live chat widget. And onclick on the accept button, video call will start in iframe. And this iframe will be there as long as the call is not ended by an agent or visitor clicking on the expand button.
- Provide chat option: The main advantage of using iframe is that along with video calls with agents, visitors have options to share files, links or text via chat on the same window. He can scroll to see the previous message under the iframe.
- Add join call button: as soon as the visitor accepts the call, the join call button will be there and will be replaced by call ended time with call duration, when agent ends the calls.
- Add function in SDK: At rocket.chat livechat widget, we use sdk to communicate with rocket server. So, I created the function at the sdk repository  to update the call status at the rc-core database.

### Work Done at RC-Core:
- Webrtc meet page layout: I develop the webrtc meet page layout and depending on the call status different components are being rendered there. For example when the status of call is ‘ended’, the call ended Page will be shown with the close window button. Similarly development is done for other status.
- Show correct avatar at correct place: I make sure to show the correct avatar at the correct place i.e if I am visitor my avatar will be at top right here on my screen. And for the agent screen my avatar will be at center and vice versa.
- Responsive code: All the features developed by me in this project are responsive i.e  all the features can also be accessed in mobile devices.
- Fix bug and add Jitsi Call Support:  Currently there is option to enable jitsi in livechat. And once an agent calls the visitor, we are not receiving any call notification at live chat widget. So, in this project along with webrtc meet app, I also fix this bug, and  now we are able to see the call notification for jitsi call as well . And join call button will also be there.
- Testing of all features: By deploying our project on ngrok, we have done multiple testing on different networks. Even the recorded demo video is on different networks and is working well.
- Cost estimation of stun and turn server: Some stun servers are available for free of cost,  For example the Google STUN server is something you can freely use for development purposes, but, as a free service, there is no SLA. But the cost of turn server is high , but one has an option to implement its own turn server using coturn project.

### Link to pull requests highlighting my work in different repositories as part of GSoC21 @RocketChat

  - [PR1](https://github.com/RocketChat/Rocket.Chat.Livechat/pull/617)
  - [PR2](https://github.com/RocketChat/Rocket.Chat.Livechat/pull/618)
  - [PR3](https://github.com/RocketChat/Rocket.Chat/pull/22854)
  - [PR4](https://github.com/RocketChat/Rocket.Chat.Livechat/pull/629)
  - [PR5](https://github.com/RocketChat/Rocket.Chat/pull/22959)
  - [PR6](https://github.com/RocketChat/Rocket.Chat.js.SDK/pull/142)
  - [PR7](https://github.com/RocketChat/Rocket.Chat/pull/22932)
  - [PR8](https://github.com/RocketChat/Rocket.Chat.Livechat/pull/641)

### My overall contribution in Rocket.Chat organization pre, peri and post GSoC21
- [Merged PRs](https://github.com/search?q=type:pr+author:Deepak-learner+is:merged+created:%3E=2020-11-20+repo:RocketChat/Rocket.Chat+repo:RocketChat/Rocket.Chat.Electron+repo:RocketChat/docs+repo:RocketChat/Rocket.Chat.ReactNative+repo:RocketChat/Rocket.Chat.js.SDK+repo:RocketChat/Rocket.Chat.py.SDK+repo:RocketChat/Rocket.Chat.Livechat+repo:RocketChat/Rocket.Chat.Embedded.arm64+repo:RocketChat/Rocket.Chat.Embedded.armhf+repo:RocketChat/alexa-rocketchat+repo:RocketChat/Opensource-Contribution-Leaderboard+repo:RocketChat/Rocket.Chat.Fuselage+repo:RocketChat/alexa-rocketchat-notification+repo:RocketChat/alexa-rocketchat-flashbriefing+repo:RocketChat/alexa-news-publisher+repo:RocketChat/alexa-rc-multiserver-client+repo:RocketChat/Apps.Rasa+repo:RocketChat/Apps.Dialogflow+repo:RocketChat/rocket.chat.app-poll)
- [Open PRs](https://github.com/search?q=type:pr+author:Deepak-learner+is:open+created:%3E=2020-11-20+repo:RocketChat/Rocket.Chat+repo:RocketChat/Rocket.Chat.Electron+repo:RocketChat/docs+repo:RocketChat/Rocket.Chat.ReactNative+repo:RocketChat/Rocket.Chat.js.SDK+repo:RocketChat/Rocket.Chat.py.SDK+repo:RocketChat/Rocket.Chat.Livechat+repo:RocketChat/Rocket.Chat.Embedded.arm64+repo:RocketChat/Rocket.Chat.Embedded.armhf+repo:RocketChat/alexa-rocketchat+repo:RocketChat/Opensource-Contribution-Leaderboard+repo:RocketChat/Rocket.Chat.Fuselage+repo:RocketChat/alexa-rocketchat-notification+repo:RocketChat/alexa-rocketchat-flashbriefing+repo:RocketChat/alexa-news-publisher+repo:RocketChat/alexa-rc-multiserver-client+repo:RocketChat/Apps.Rasa+repo:RocketChat/Apps.Dialogflow+repo:RocketChat/rocket.chat.app-poll)

## Final Product
 - Provide Video Call Support in Livechat.
 - Two video calls option are now available for Live chat.
 - In this project we develop the webrtc meet app from scratch and also add code to make the jitsi call work at livechat widget. So, now we have two video call options for livechat, one is webrtc meet app and other is jitsi meet app.

<p align="center">
  <img src="https://github.com/Deepak-learner/GSOC-21-Work-Report/blob/70c337f41ab0a188ab4db55b4ccbada41800d7d3/Screenshot%202021-08-26%20at%201.24.01%20PM.png">
</p>

### Project Demo: 
 - [Video call with Webrtc Meet App In Livechat]( https://drive.google.com/file/d/17uI5Fa8xAeHXJ-f-K1WtMVae6xV5JQT8/view?usp=sharing)
 - [Video call with Jitsi Meet App In Livechat](https://drive.google.com/file/d/17N7M2j31syy9SeXSvQZW1xM5Ipcnp7Gq/view?usp=sharing)

### Project Document:
 -  [My Project Propsal](https://docs.google.com/document/d/1ieTO8mlchgp-gxAKTL3EFmvm36a9B7GfetfgDAf9tVc/edit?usp=sharing)
 -  [Project Presentaion to Rocket.Chat Community](https://www.youtube.com/watch?v=tHyY0QVvRC8)
 
### Further steps:
1. Minor UI changes in accordance with Design team suggestions.
2. Any improvements suggested by my mentor.

## Thank you [Rocket.Chat](https://github.com/RocketChat) for an amazing summer of code!
