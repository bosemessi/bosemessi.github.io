---
title: "Possession Chains - To survive or not to survive, that is the question."
layout: post
---

Let me, as is the norm, start by pointing out the inspirations for writing this post. I was having discussions with [Paul Johnson](https://twitter.com/paul_johnson89) about how we could apply survival analysis in football, and he came up with this really cool idea of using survival analysis to investigate possession chains. Also, lots of Barcelona fans (myself included) are voicing dissatisfactions with how the team lacks composure and goes for unnecessary verticality especially in key Champions League games when things are not going their way - this is well documented in Domagoj Kostanjsak's article [here](https://barcafutbol.substack.com/p/how-verticality-intensity-and-defensive?utm_source=substack&utm_campaign=post_embed&utm_medium=web). I finally had the impetus to do some quick checks and finally enter the rabbit hole of survival analysis properly. If you don't care about the rest of the article, this is how Barcelona has been faring over the years in terms of retaining possession for long durations in Champions League matches (since 2008-09). 

![Image](https://bosemessi.github.io/images/Barcelona/BarcelonaSurvival.gif)

# A Brief Intro to Survival Analysis and Methodology

What is survival analysis, you may ask ? In clinical studies, it could be the study of literal survival - that is, time until death from some disease. It could be the study of reoccurence of a disease if it has occured once in the past - eg being cancer. It could have nothing to do with diseases at all - for eg, could be the study of premature births. The end event is often referred to as the "death event".

In the context of football, and in particular for us, we use survival analysis techniques to study the duration of possession chains for Barcelona's UCL campaigns starting from Pep Guardiola's reign. "Possession Chains" are defined sort of loosely - we follow the "touch-based actions" definition of Opta, and a series of touches by the same team constitutes a possession chain. If it's interrupted even for once by an opposition touch-based action, the possession chain comes to an end and a new one starts. So this is different from "possession sequences" where we wait for the opposition to establish control of possession by say, possessing the ball for 6 seconds or more, or possessing the ball for 3 or more controlled touch-based actions etc. We do omit "pinball chains" - basically single action long chains - eg. two players belonging to opposite teams playing head tennis with the football a la the Championship.

We have naturally "censored" data in football. In a clinical study context, this would mean a patient fails to follow up or opt out of an study before the designated end-period of the study arrives, or doesn't encounter "death" ("death" being a mnemonic for actual death, occurence/reoccurence of a disease, occurence/reoccurence of pregnancy etc). Here are some possible censorings that can happen in football :

(i) In the study of possession chains, it can so happen that the first half or the second half of the match comes to an end while one of the team is in possession of the ball - that possession chain didn't encounter the "death event" before the match (the study period) ended.

(ii) The natural objective of possession chains is being able to take a shot at the opposition goal, so any chain that ends with a shot and is not a "pinball chain" also is assumed to have not encountered the "death event", instead it's a "censored chain".

(iii) Now, one can argue that shots are not always possible and the objective of the team should be able to reach as dangerous a zone as possible or achieve the next best thing to a direct shot. These could be - (a) winning a penalty, (b) winning a corner kick or (c) winning a free-kick high up the pitch. Any sequence that ends with a penalty, we will definitely call them "censored".

(iv) Corner kicks are won in different ways. For eg a shot that gets palmed away by the keeper or blocked by a defender and goes out for a corner. However, the shot itself defines the "censoring" so we don't have to overthink about this case. Another eg could be a dangerous cross that's headed out for a corner. Or, a winger works his way to the corner flag, tightly marked by one or many opposition, realises he can't wiggle out of the situation and then kicks the ball against the opposition to win a corner. We will define this particular case as a "censored chain" since this was the next best possible outcome for that chain and is done intentionally. The cross that reached the box before being headed away....well, it's subjective to figure out whether to call it a "censored chain" or not - certainly not possible to deduce only from data, so we are going to define those events as "death events". Any corner kick won within a 10 m radius of the corner flags will be flagged "intentional" and hence "censored".

(v) There is a ton of subjectivity involved with freekicks. Players like Jack Grealish make their bread and butter with winning freekicks high up, but not all players win freekicks intentionally. So, we will skip the subjectivity and call all possession chains ending with a freekick to have met their "death" - no censoring here.

(vi) All other types of chain ends - tackles, interceptions, clearances etc - bring "death" to the chain, no censoring here.

# A Journey through the pages of History 