---
title: Modeling a Pandemic — SIR Model
description: '‘We do not decide the timeline, the virus does”.'
date: '2020-04-03T09:35:22.568Z'
categories: []
keywords: []
slug: /@PandeySudhendu/modeling-a-pandemic-sir-model-18a8c76034a1
---

> **‘We do not decide the timeline, the virus does”.**

![Lockdown. Stock image-pexels](img\1__LMQCfAOnzbI4wYHJAJsk0Q.jpeg)
Lockdown. Stock image-pexels

Staying indoor, isolation and quarantine makes a lot of sense when an infectious disease (pandemic or epidemic) hits. The reasoning is simple, if a disease is infectious (infects someone who is not already infected), has no current cure or vaccine, the best way to contain it is to avoid contact. The logic is easy to express and understand and hence easy to communicate (although difficult to implement as we can see around the world).

But how do policymakers, epidemiologists, statistician decides the parameter of isolations? How do they determine the extent and timeline of lockdown?

**1\. The duration of lockdown:**

Deciding on the number of days. 5 days vs 10 days vs a month? Or maybe 21 days of lockdown and then 5 days of ease followed by 10 days of lockdown again. Which one is better suited?

**2.** **Extend of lockdown:**

Complete shutdown or selective shutdown (school, public transport, a certain part of cities, etc.)

As you can tell, these two parameters are different for different epidemic and places. In India for example, during the current COVID19, the shutdown is for 21 days and the extend of lockdown is (almost) complete. In Dubai, UAE, the shutdown is for 10 days and the extend is selective (8 pm to 6 am complete, 6 am to 8 pm public transport working and people can move out although have to avoid it).

How do we arrive at these parameters? Contrary to what I thought initially, these values are not random and there is no single formula, but a series of modeling, reasoning and external factors (economical and political) that help us decide.

For this blog, we will look only at the modeling part and that too only at one type of modeling called **SIR** (**Susceptible Infected Recovered**). We will focus on the classical SIR model (Kermack and McKendrick 1927).

**SIR Model**: _An SIR model is an epidemiological model that computes the theoretical number of people infected with a contagious illness in a closed population over time._

![](img\1__1UOy1tPo__BjxZw1YL3F0SQ.png)

Here are some noteworthy aspects of the SIR model:

1\. Any person in the population belongs to either of three classes and only in one of them.

2\. **S: Susceptible** are people who can be infected but yet not infected. This usually is the entire population _minus_ the infected, cured, immuned and dead people.

3\. **I: Infected** are people who are infected and have a chance of making other infected. We at least have to have 1 infected person to start an epidemic.

4\. **R: Recovered (removed)** are people who are no more infected and cannot infect anyone. This includes people who have recovered, developed immunity or people who have died. Hence this class is sometimes called removed. This usually is 0 at the start but it keeps changing as well see below.

5\. We can see that people move fro S to I to R.

6\. We have to determine the rate of changes where people move from S to I and I to R

7\. We can also incorporate new individuals getting added by new birth as flow from ‘elsewhere’ into class S.

8\. We can incorporate people dying of some other cause, not the epidemic as flow from S, I, R to elsewhere.

For pedagogical purposes, we will ignore 7 and 8 for now and assume the population is constant. We will also study the model in a very basic sense.

Firstly, we need the values for the following variables:

![Screenshot from Worldometer](img\1__TsHavlPubgnsOp6__mM2O3g.png)
Screenshot from Worldometer

1.  Susceptible (S)
2.  Infected (I)
3.  Recovered (R)
4.  Total population (N)
5.  Total time (t) — this is an independent variable
6.  **Contagion Rate** (b) — Rate at which susceptible person becomes infected. We have to assume and later refine this.
7.  **Recovery Rate** (k) — The rate at which an infected person moves to recovers (or dies) per day and thus become ineffective. We have to assume and later refine this.

Value 1 to 4 is easily available. The above screenshot is an example of COVID19 status as of 3rd April, 2020. Value 6 and 7 is where the initial guesswork, expertise, past case-study, experience, machine learning, and other factor comes in. In nutshell, b and k both together determine the two factors we saw initially (duration and extend of lockdown).

![](img\1__pqJm5A7KqeBl1s5wkoPc4g.png)

In the simplest form, the differential equations look like this:

![](img\1__eZ58Dg75pkXSD4gHAW4RXA.gif)
![](img\1__nJiy78FCGDPIJTmXwswSRw.gif)
![](img\1__wt5e7nZ6DTwgUXs3sPJsWw.gif)
![](img\1__X52oPRh8ZWN97Te0IeiYTA.png)

Let’s put some values into our parameters. We plot this on a graph where X-axis time, Y-axis the number of people.

To start we take a hypothetical country and note the following values for it.

![](img\1__skXOP3E2Hb1apR3JxQq5jQ.png)

We also make a random guess for b and k values and start evaluating.

**Case 01**: Random Value. Infection is spreading, no lockdown and no cure.

![](img\1__5K__UUfKb1Wf6bmDJUpZhfg.gif)

b= 0.9, k=0.01

**Observation**:

The entire population get’s affected in less than 10 days.

It takes 200+ days for the number of infected to drop

**Case 02**: Partial lockdown. Recovery faster since hospitals have enough time to clear existing

![](img\1__HHEYsCf8rncd60nePZaIXw.gif)

b= 0.5, k=0.1

**Observation**:

The entire population get’s affected in around 20 days.

It takes less than 50 days for the entire population to recover.

**Case 03**: Complete lockdown. Recovery same as case 02

![](img\1__uuMK__MFAsli08SKGrM3p__A.gif)

b= 0.1, k=0.1

**Observation**:

Only 40% of the population ever gets affected!

It takes around 125 days for the entire population to recover and no new infections.

**Case 04**: Partial lockdown. We now have a cure or vaccine.

![](img\1__nAAoZQUpheOY7oK__73YJgQ.gif)

b= 0.5, k=0.6

**Observation**:

Only 10% of the population ever gets affected!

It takes around 30 days for the entire population to recover and no new infections.

As you can observe, the effect of lockdown is tremendous if followed. The recovery rate also affects the curve and hence the importance of finding a vaccine or cure is vital.

Needless to say, these are very simple examples and ignores a lot of details but can be a good starting.

Note: the models are created using [GAMA Platform](https://gama-platform.github.io/), a fantastic opensource modeling tool. They are doing some excellent modeling of COVID19 if you are interested. Check [here](https://gama-platform.github.io/covid19).