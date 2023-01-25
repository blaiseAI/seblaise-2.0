---
title: "How I Built a Covid-19 Vaccination Tracker"
date: 2022-04-03T23:15:00+07:00
slug: built-covid-19-vaccination-tracker
category: hackathon
summary:
description:
cover:
  image: "covers/what-is-bioinformatics.jpg"
  alt: "Built a Covid-19 Vaccination Tracker"
  caption:
  relative: true
showtoc: true
draft: false
---

## What I built

Covid-19 Vaccination Tracker

### Category Submission:

Program for the People

### Web App source code

https://github.com/blaiseAI/covid-vaccination-tracker

### Screenshots

- Serie ["First prototype"]

  > This is my first prototype with `react.js`
  >
  > ![first-prototype](https://dev-to-uploads.s3.amazonaws.com/i/incuzse3ds6t5ytooyte.png)

- Serie ["Old friend Cors"]

  > `cors` challenges outcome while using `react.js`
  >
  > ![Alt Text](https://cdn.discordapp.com/attachments/545028771401433088/796508072251490334/unknown.png)

- Serie ["Final Submission"]
  > 🚀 App using Digital Ocean App Platform
  >
  > ![Alt Text](https://dev-to-uploads.s3.amazonaws.com/i/ou11jckv18udzf0t1q2x.png)

### Description

🦠Covid 19 Tracker Canada - Vaccination Tracker 📈

### Link to Source Code

[Source-code](https://github.com/blaiseAI/covid-vaccination-tracker)

### Permissive License

[MIT](https://choosealicense.com/licenses/mit/)

## Background

At first i really didn't know what i wanted to build, but in the back of my head i wanted to build something that help the community during this hard times with COVID-19 pandemic. Last year i wanted to build a covid-19 Tracker using `react.js` but i always failed to do so because i was getting started learning the framework, so this has been bugging me to build some web app that is going to help us all and i told my self that with this **DO challenge** it was my opportunity to pick it up no matter what framework i will use to build it. So i came up with an idea to build a **COVID-19 Vaccination Tracker** in Canada since i live in **Edmonton, Alberta**. I am planning to expend to a world wide COVID-19 vaccination tracker soon.

### How I built it

This challenge has taught so many lessons than i thought, I was thinking it was going to be a piece of cake to build some simple app but unfortunately deployment can be tricky and thanks to couple **DO** Tutorial i managed to deploy my **COVID-19 Vaccination Tracker**. Originally i started building this web app with a simple react app and scrapping vaccination data from an external `api` up to this point everything was going great i was running my app on my local and i had my data being displayed in my app, so when i deployed my app old friend cors got triggered why one because the `api` source server did not allow old friend `cors` from a non origin url which is when i was deployed the origin request was not coming from local anymore and the `api` i am relying on does not support that, i was really frustrated at that moment but did not give up after doing some research i found well this can't be complicated and i found `https://cors-anywhere.herokuapp.com/` which is a url you append to a url with a cors issue and it solves that but this seemed to be to good to be true it wasn't not after couple hours then `https://cors-anywhere.herokuapp.com/` server went down so did my data and at this point like "wow " i came in thinking that it was gonna be easy and it kept on getting complicated not until i came across `next.js` when i was reading in their docs it said i could do some serverside logic and "boom✨🚀" all excited again next came as a life saver because instead of making the fetch on the front-end, it has the back-end do it, which passes the results as props to the front-end component and after implementing this it all was easy as `Deploying to DO`.
Picked new skills yes indeed i had never used next.js and i had to learn it as i was building this app.

### Additional Resources/Info

- [How To Deploy a Next.js App to App Platform
  ](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-next-js-app-to-app-platform)
- [Nextjs](https://nextjs.org/)
