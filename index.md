---
layout: page
title: "Modern Times: Rise of Technology in Cinema"
subtitle: An ADA Data Story
cover-img: /assets/img/moderntime_head.jpg
---

In the beginning, there was the void. Then came the big bang, which created all conditions needed for the emergence of the seventh art. However, it was not until the 17th century that its precursor, the magic lantern, and its coloured projections, was invented. A few years later, at the dawn of the 20th century, "Horse in Motion", one of the first chronophotographs, stirred up the crowds. Then, with the advent of celluloid film, sequences became longer, more complex, and more popular until the birth of the movie industry. Ever since, it continues to grow in strength and power. One look at the number of films released over the last few decades suffice to notice its exponential expansion. 

*[plot of growing number of movies]*

Ever since, the development of cinema is characterized by technological breakthroughs, for the worst and for the best. To examine how this technological evolution shaped the movie industry, we used the CMU Movie Corpus dataset, which contains 42,306 plot summaries and corresponding metadata extracted from Freebase. We believe that we should observe a two-fold impact of technology on our dataset: one is on the technology used to produce the movies in itself, thus impacting actor careers and film genres; the other is technology itself as a narrative theme appearing in plot summaries. We seek to measure, through a statistical and data-centered lens, this cultural evolution.


# I - How Technology Shaped The Movie Industry

## The emergence of sound and color

 
<img src="/assets/img/the-wizard-of-oz-black-and-white-to-colour.gif" alt = "Oz color" style="display: block; margin: 0 auto;"> 


Widespread introduction of sound and colour in the 20s revolutionized the industry and correlates with the quick disappearance of silent and black-and-white movies…

*[plot of silent/black and white]* 

### Adapt – or perish
In the face of this brutal change, actors need to adapt and seize new opportunities. But while some are able to change their style, others miss the boat and mark the end of a sinking career.

*[text – analysis]*
*[one/two plots]*


### Some exceptions… 
Nevertheless, some like Charlie Chaplin survive true to themselves amidst the chaos. Even with the growth and popularity of sound in movies, he decides to stay in his original realm with City of Light, and Modern Times, whose criticism of technology is flagrant, which are still now unforgettable classics. 

<img src="/assets/img/chaplin_industry.gif" alt="Chaplin tech" class = "gif-size-1">

![Chaplin Tech](/assets/img/chaplin_industry.gif)


## The lost ones

But not all were so lucky. Before the 30s, movies usually were stored in flammable nitrate films, which led to many unfortunate loss events: many movies turned to ash in vault fires, taking with them, the collective memory of beloved stories and iconic stars…
To track down these forgotten figures, we investigated another an external database from Wikidata [1] listing the most prominent lost films in the USA.

*[number of movie lost after release]*

As the dataset is quite small and only considers the release date of the movies – and not their destruction date – we cannot infer much from the graph. But it is interesting to note that while many movies were lost until the 40s, it then became a very rare event thanks to the transition to safer storage films such as cellulose triacetate or polyester films. 
Who are the biggest losers amongst our dataset? A quick analysis revealed that only two actors played in more than one subsequently lost movie: Koyel Mullick and M.G Ramachandra. Let’s take a minute to remember their face and efforts. 

*[ev. Une photo des deux]*

## Remakes

Technology induced big changes, more safety, and a vaster realm of artistic opportunity! This leads to endless remakes of the most popular stories in the world, which can be retold in an infinity of new manners. Have a wild guess: which of these stories had the biggest impact?

*[“fun fact” top-5 of most remade movies, histogram]*

If you have never heard of one of these, then you probably should look them up to better comprehend humanity. For this, you can either choose the original book, or one of its dozens of adaptations. With so many options, everyone should get something out of it, so no excuse to not enrich your cultural background! 

# II – Movies as reflection of technology development and public opinion

Movies are not only impacted by technological advancements but is also a reflection of this evolution and of the minds. 
In this plot, for example, we can clearly see the impact of real-world wars on the number of war films made on the last century.

*[plot war films]*

Can we find out more events that can be critically reflected through the movie plot summaries? 

First, we created wordclouds to identify the technological-related words from the datasets…

After that, we identified several technological events and calculated the mutual information between these events and the plot summaries…

But what about the feelings towards theses technological advancement and their impact on society? To discover this, we made a sentiment analysis of … 




 









