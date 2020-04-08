---
title: COVID19 and BCG (TB) Vaccine
description: >-
  Whatever doesn’t kill you, makes you stronger, unless it does eventually kill
  you.
date: '2020-04-06T07:48:23.372Z'
categories: []
keywords: []
slug: /@PandeySudhendu/covid19-and-bcg-tb-vaccine-93b01bfa458a
---

> **Whatever doesn’t kill you, makes you stronger, unless it does eventually kill you.**

![BCG Vaccination vs COVID19 Confirmed Cases (per million population)](img\BCG1.png)
BCG Vaccination vs COVID19 Confirmed Cases (per million population)

If you read through some of the [articles](https://www.google.com/search?q=bcg+covid+19&oq=bcg+cov&aqs=chrome.2.69i57j0l5j69i61l2.7635j0j7&sourceid=chrome&ie=UTF-8), researchers and doctors are **suggesting** a strong correlation between the number of COVID19 cases (confirmed, fatality) vs whether the country does or does not have a nation-wide (or large scale) BCG immunization program.

Scientists around the world are rushing to create a vaccine for COVID19, but we should not expect anything coming out so early.

In my previous article, [COVID19- India’s Progression](https://medium.com/@PandeySudhendu/covid19-indias-progression-1f0f75450772), I discussed why I think under just _good enough_ measures (no mass migration, no large gathering, and [reasonable lockdown period](https://medium.com/@PandeySudhendu/modeling-a-pandemic-sir-model-18a8c76034a1) obedience), India might not see as many cases (in millions) as some experts are predicting.

This article expands on that theory with some new insight that has come to light recently.

First, a word of caution:

_I am not a scientist or an epidemiologist and not qualified to comment on the subject of epidemic & vaccine. This article is for pedagogical purposes and merely provides the reader with all the data necessary to understand if in fact there is any correlation or not. Even if we do find any correlation, we cannot assume causation right away because there are many other factors not part of the comparison. Nevertheless, it is a good starting point to explore this relation deeper._

![image from xkcdimage from xkcd](https://cdn-images-1.medium.com/max/800/0*bavKLC7i_U2Xdxrx.png)
image from xkcd

**What is BCG Vaccine**: Bacillus Calmette–Guérin (BCG) is a vaccine primarily used against tuberculosis and to stop meningitis. It’s a century-old vaccine (the 1920s). This vaccine is given to infants and different countries have different policies for nation-wide BCG immunization.

Note that though both affect the respiratory system, TB is a bacterial infection unlike COVID19, which is viral. Nevertheless, the BCG vaccine helps strengthen the immune system, which is our first line of defense against all types of infectious diseases. More benefits [here](https://www.youtube.com/watch?v=LLTcNHfRuVs).

**Why do some countries have it** (or why others don’t): It has to do with the TB burden a country is facing. Developing countries like India for example, have higher TB cases, hence BCG mass immunization was started right after independence, in 1948. China started country-level immunization in the 1930s. Iran started in the mid-1980s. For western countries, most of them don’t have BCG immunization for the entire population.

**What is the claim made**: According to various researchers and medical professionals, there seems to be a direct correlation between BCG vaccination status and the number of COVID19 cases.

**What does it mean**? The countries which follow standard nation-wide vaccination program for BCG see much lesser number of COVID19 cases (and hence lesser death).

**The potential conclusion made**: That BCG vaccination helps to immunize not only against TB but also against other infectious diseases, COVID19 seems to be one (SARS as well was less infectious to BCG vaccinated countries).

**How are countries reacting**: Few countries have already started doing the trial and giving BCG to their healthcare workers and the general population. Australia is taking the lead. Netherland has started giving it to its healthcare workers and the elderly population. Other countries, where BCG is part of the national vaccination program are happy but cautious of the result.

**The data**: The data for this blog is sourced and curated from WHO and Worldometer (links provided at the end). [TIBCO Spotfire](https://www.tibco.com/products/tibco-spotfire), a leading advance data analytical tool is used to create all the visualizations. The BCG immunization data is of 2018. The COVID19 data is as of 5th April, 2020.

### The Big Picture

![TreeMap: The size determines the number of cases. The color red: No BCG, Green: BCG](img\BCG2.png)
TreeMap: The size determines the number of cases. The color red: No BCG, Green: BCG

The above representation is [TreeMap](https://en.wikipedia.org/wiki/Treemapping). The bigger the boxes, the more COVID19 cases _per 1 million population_. The color denotes whether there is a national-level BCG vaccination (as of 2018). It is very much evident that all the countries without national level BCG have more cases per 1 million as are on the upper left corner. All the green boxes are small and are tucked right in the lower right corner.

### **Covid19 Confirmed Cases with BCG Status**

Below two scatterplot shows COVID19 confirmed cases for countries which have BCG immunization program vs the one which does not. Since different countries have vastly different populations, we are normalizing the data to cases per million instead of the entire population.

![](img\1__J69__m2Z3aoQXbJg1SUjvRw.png)

For the above, we observe:

1.  Per million cases are in the lower range for countries with BCG immunization (the maximum is 1600 per 1 million for Monaco).
2.  Per million cases for countries with no BCG immunization goes to a maximum of around 8000 (for San Marino)
3.  For BCG immunized population, the countries are clustered at the bottom of the Y-axis, whereas for no-BCG immunized countries, we see that data is spread across Y-axis and no cluster is apparent. Clustering is the first step to recognize if certain patterns exist.

### Covid19 Death Cases with BCG Status

Below two scatterplot shows COVID19 fatality for countries which have BCG immunization program vs the one which does not. We are normalizing the data to cases per million instead.

![](img\1__TY__yEZR7Bt5ePCzGM0ksrQ.png)

1.  Per million death cases are in the lower range for countries with BCG immunization (the maximum is around 45 per 1 million for China).
2.  Per million death cases for countries with no BCG immunization goes to a maximum of around 950+. This is almost 20 times compared to countries with BCG immunization.

### Countries with 10,000+ cases for COVID9

![](img\1__mcqNUk0__VniEswvrXr__1Rw.png)

For 15 countries with 10K+ cases as of writing this article, we can see that 11 do not have any kind of BCG vaccination policy.

How do we explain China and Iran, both of which have 99% of BCG vaccination? Of course, the population is the biggest reason, they are in the top 10. Merely based on cases per million, it averages out.

Yet, for China, we can argue that since it was the epicenter of the pandemic, it was caught off-guard and hence we see such high numbers.

For Iran on the other hand, the universal BCG started in the mid-1980s and hence population aged 40+ years today are not vaccinated. Unfortunately, COVID19 hit older people worst and that might explain.

In summary, although this looks a decent correlation which must be explored more and tested with other factors. It should not be taken at face value and more analysis, expert studies should be carried out. Nevertheless, just like Australia and the Netherlands, countries can start experimenting and giving it to healthy healthcare professionals to see if does indeed help.

**Source**:

[BCG Data for 2018.](https://apps.who.int/gho/data/node.main.A830?lang=en)

[COVID19 Data as of 5th April, 2020.](https://www.worldometers.info/coronavirus/)

[News.](https://www.khaleejtimes.com/coronavirus-outbreak/bcg-vaccine-a-potential-new-tool-to-fight-covid-19-study)

**My other articles**:

[COVID19- India’s Progression](https://medium.com/@PandeySudhendu/covid19-indias-progression-1f0f75450772)

[Modeling a Pandemic — SIR Model](https://medium.com/@PandeySudhendu/modeling-a-pandemic-sir-model-18a8c76034a1)