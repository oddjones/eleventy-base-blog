---
title: Mental Cigarette breaks (followup)
description: This is a post on My Blog about touchpoints and circling wagons.
date: 2018-09-30
tags:
  - PKM
  - time management
layout: layouts/post.njk
---

# Mental cigarette breaks - followup

So for those of you who are interested in how I got on with my "mental cigarette breaks" thing - my first problem was how to set up a recurring reminder on the hour, every hour but only during weekdays.

This seems like it should be easy - but damn it if it isn't _really stupidly hard_

The problem with things like regular reminders in calendar apps is that they’re not _really_ what calendar apps are for. Calendars are made for scheduling actual things, like meetings, events; real things that happen during your day, that you might need a reminder for.

A reminder (just a reminder) is different. It doesn't actually HAVE an end time - just a start time.

Setting regular reminders is a challenge for the “repeat” functions of most calendars - They’re usually pretty lo-fi - you can schedule something to repeat every day, every week, every month etc - but what if I want to schedule a reminder for every HOUR? (But only every hour between 9-5 on days within my working week) - this is beyond even Microsoft Outlook’s neat little scheduling dialog box.

![Image.png](https://res.craft.do/user/full/4be41629-c0dd-7d6e-3ef3-3a7804729a0f/doc/FD5341FD-0999-4715-81C0-AA486FB3D496/87CB4C0F-1B2B-4C53-9F08-87D6FA77EB24_2/G0j5zsss0yPbE3b2K3yRwSn8MIyuPkMYgOHyUrK6pYsz/Image.png)

This set me on a wild goose chase for the best calendar app for macOs - one that would allow me to enter just reminders (there isn’t one that I could find). I did happen across Fantastical, which I’ve had an on-again off-again relationship with for years - I like their natural language date input which allows me to type things like “In calendar /MCB create event Mental cigarette break every Wed btw 09:00 & 09:01 alert 10 min” - which will create a recurring event in my “MCB” calendar at 9am every Wednesday with an alert 10 minutes beforehand. This is really helpful

I beat my head against this for a while - thinking “this would be so easy to do in Javascript” - so I wrote myself a little Node.JS script to do it.

```javascript
const workdays = ["Mon", "Tue", "Wed", "Thu", "Fri"];
const workHours = [
  "09:00 & 09:01",
  "10:00 & 10:01",
  "11:00 & 11:01",
  "12:00 & 12:01",
  "13:00 & 13:01",
  "14:00 & 14:01",
  "15:00 & 15:01",
  "16:00 & 16:01",
];

workdays.map((day) => {
  workHours.map((hour) => {
    console.log(
      `/MCB Mental cigarette break every ${day} btw ${hour} alert 10 min`
    );
  });
});
```

\#NTS - don’t forget to mention javascript in Apple script editor and bizarre format for scheduling events that stopped me trying

## What do I do in my mental cigarette breaks?

- **Chores** - such as cleaning up the kitchen, emptying the dishwasher etc - The great thing about this is that if I see the primary goal of the exercise as taking a mental break, then the "chore" becomes less of a chore - it's a mantra. A means of staying mindful whilst allowing my brain to ponder whatever I'm working on.
- **Micro DIY tasks** - I have a job to do to put fixings on the back of all the radiator covers in my house, so they sit snug to the wall and don’t fall over, but are easy to remove to clean behind (You wouldn’t believe how much dog hair can accumulate under a radiator cover in a week) - I wouldn’t be able to do ALL of these in a mental cigarette break, I might not even be able to all of one radiator cover - but over the course of a day I can probably do 2 or 3, which saves time out of my valuable weekend.
- **Scheduling task**s to do in the next mental cigarette break - I came up with the idea for doing the radiator covers on my next MCB while I was cleaning up the kitchen. So I took my little bag of fixings and placed them on the radiator cover, making a note to change the reminder of the next MCB
- Breaking tasks into micro-tasks achievable in 10 minutes or less. This fits nicely in with what I’m trying to do on my whole, wider PKM piece - which is all about breaking large tasks down into achievable projects (also fits with what my CBT Therapist is talking about when she talks about “breaking down worries into manageable, fixable chunks”)

![Image.png](https://res.craft.do/user/full/4be41629-c0dd-7d6e-3ef3-3a7804729a0f/doc/FD5341FD-0999-4715-81C0-AA486FB3D496/84A089AD-A341-40C0-8F94-A4452FF17C70_2/UyvSamKQZHfIIXxBJqF4q69KQ99f2bxS2Da6orUxRwQz/Image.png)
