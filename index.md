---
layout: page
title: "Modern Times: Rise of Technology in Cinema"
subtitle: An ADA Data Story
cover-img: /assets/img/moderntime_head.jpg
---

In the beginning, there was the void. Then came the big bang, which created all conditions needed for the emergence of the seventh art. However, it was not until the 17th century that its precursor, the magic lantern, and its coloured projections, was invented. A few years later, at the dawn of the 20th century, "Horse in Motion", one of the first chronophotographs, stirred up the crowds. Then, with the advent of celluloid film, sequences became longer, more complex, and more popular until the birth of the movie industry. Ever since, it continues to grow in strength and power. One look at the number of films released over the last few decades suffice to notice its exponential expansion. 

{% include_relative figs/nb_movies_per_year.html %}

Ever since, the development of cinema is characterized by technological breakthroughs, for the worst and for the best. To examine how this technological evolution shaped the movie industry, we used the CMU Movie Corpus dataset, which contains 42,306 plot summaries and corresponding metadata extracted from Freebase. We believe that we should observe a two-fold impact of technology on our dataset: one is on the technology used to produce the movies in itself, thus impacting actor careers and film genres; the other is technology itself as a narrative theme appearing in plot summaries. We seek to measure, through a statistical and data-centered lens, this cultural evolution.


# I - How Technology Shaped The Movie Industry

## The emergence of sound and color

 
<img src="/assets/img/the-wizard-of-oz-black-and-white-to-colour.gif" alt = "Oz color" class = "center"> 

![Oz new colors](/assets/img/the-wizard-of-oz-black-and-white-to-colour.gif)


<p align="center">
  <img src="/assets/img/avatar-icon.png">
</p>

Hm.

<img src="/assets/img/avatar-icon.png" alt = "triaaal" class = "center"> 

This text need to be centered => 

<p align="center">
Text Text Text.

</p>


Re trial


<p class="center">
  <img src="/assets/img/avatar-icon.png">
</p>



Widespread introduction of sound and colour in the 20s revolutionized the industry and correlates with the quick disappearance of silent and black-and-white movies…

{% include_relative figs/genres_evolution_silent_BW.html %}

### Adapt – or perish
In the face of this brutal change, actors need to adapt and seize new opportunities. But while some are able to change their style, others miss the boat and mark the end of a sinking career.

To illustrate this phenomenon, let’s consider shortly the arrival of synchronized score and sound. Sound films became popular in the 1930s, we can all imagine the impact it had on the film industry as actors had to change their approach to acting a scene. Now let’s ask ourselves if such an event changed the career of actors. To do that let’s take all actors in our dataset that have acted in at least one silent film and we compare for all of them the amount of silent movies they each acted in vs the amount of non silent films they acted in. 

But, you might be asking yourself, wouldn’t the retirement of the actor and the potential death due to older age bias the results? An to this we answer, you are absolutely right. We need to be careful with our analysis but unfortunately we do not have access to the actor’s date of passing. However we do have their date of birth. We thus take advantage of that to improve our analysis. Below you find the percentage of actors, selected such that they acted on their last silent film below the age of 50, that « survived » the arrival of sound. tThe threshold parameter is the ratio of number of sound films over the number of silent films above which an actor is considered to have survived the transition. Thus a threshold of 1 means that the survivors have acted in at least as many sound films as silent films.

{% include_relative figs/younger_silent_actors.html %}

But our analysis can still be improved! If we consider that most of these actors have only appeared a handful of films, we can also consider that the survival rate might be influenced by a poor initial career. 

{% include_relative figs/distrib_nb_silent_films.html %}

So we can consider the following analysis: we can compare the survival rate for actors who have acted in less than 5 silent films and actors that have acted in at least 5 silent films. We then find pairs across the two groups whose date of birth and age at last silent film exactly matches. For both groups, similarly as before, we observe the fraction of survivors : 
{% include_relative figs/matched_actors.html %}

... i'll still write a conclusion about this



### Some exceptions… 
Nevertheless, some like Charlie Chaplin survive true to themselves amidst the chaos. Even with the growth and popularity of sound in movies, he decides to stay in his original realm with City of Light, and Modern Times, whose criticism of technology is flagrant, which are still now unforgettable classics. 

<img src="/assets/img/chaplin_industry.gif" alt="Chaplin tech" class = "gif-size-1">

![Chaplin Tech](/assets/img/chaplin_industry.gif)


## The lost ones

But not all were so lucky. Before the 30s, movies usually were stored in flammable nitrate films, which led to many unfortunate loss events: many movies turned to ash in vault fires, taking with them, the collective memory of beloved stories and iconic stars…
To track down these forgotten figures, we investigated another an external database from Wikidata [1] listing the most prominent lost films in the USA.

{% include_relative figs/lost_films_per_year.html %}

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

{% include_relative figs/genres_evolution_war.html %}

Can we find out more events that can be critically reflected through the movie plot summaries? 

We employed Autophrase [3] to extract high quality words from the plot summaries, sorting by tf-idf score. We print the first movie to contain that phrase in its summary to understand where the world was from a cultural standpoint.

Notable pieces of technology make the list of high quality words, with modes of transport such as the **submarine**, **aircraft**, boat (**hull**), and car (a **jeep**) in The Impossible Voyage (1904), Aero NT-54 (1925), The Boat (1921), and Call Out the Marines (1941) respectively. Nuclear fears are alive as early as the 50s with nuclear **fallout** in Day the World Ended (1955). Robots make an appearance with a **computerized** kitten in Push-Button Kitty (1952) and an **android** in Frankenstein Meets the Space Monster (1965). Hypothetical technologies were also present with **cloning** in Tintin and the Lake of Sharks (1972). Finally in the internet age,  Hackers (1995) features **downloading** files.

{% include_relative figs/top_phrases.html %}

After that, we identified several technological events and calculated the mutual information between these events and the plot summaries…

But what about the feelings towards theses technological advancement and their impact on society? To discover this, we made a sentiment analysis of … 

# References

This work would not have been possible without the datasets and code libraries from the following sources.

- [[dataset][1]] Historical Cross-Country Technology Adoption (HCCTA) Dataset. [[article][7]] Comin, D. and Hohijn B., **Cross-Country Technological Adoption: Making the Theories Face the Facts**. Journal of Monetary Economics, January 2004, pp. 39-83.

- [[dataset][8]] CMU Movie Summary Corpus. [[article][9]]**Learning Latent Personas of Film Characters**
David Bamman, Brendan O'Connor, and Noah A. Smith
ACL 2013, Sofia, Bulgaria, August 2013

- [[dataset][6]] Geographic plots made with Natural Earth.

- [[library][2]] luozhouyang/AutoPhraseX. **Automatic Phrase Mining from Massive Text Corpora in Python**.

- [[article][3]] Jingbo Shang, Jialu Liu, Meng Jiang, Xiang Ren, Clare R Voss, Jiawei Han, **Automated Phrase Mining from Massive Text Corpora**, accepted by IEEE Transactions on Knowledge and Data Engineering, Feb. 2018.

- [[article][4]] Jialu Liu*, Jingbo Shang*, Chi Wang, Xiang Ren and Jiawei Han, **Mining Quality Phrases from Massive Text Corpora**, Proc. of 2015 ACM SIGMOD Int. Conf. on Management of Data (SIGMOD'15), Melbourne, Australia, May 2015. (* equally contributed, slides)

- [[article][5]] Lee, Daniel, Huilai Miao, and Yuxuan Fan. **Analyzing Movies Using Phrase Mining**. (2021).

[1]: https://www.nber.org/research/data/historical-cross-country-technology-adoption-hccta-dataset
[2]: https://github.com/luozhouyang/AutoPhraseX
[3]: https://arxiv.org/abs/1702.04457
[4]: https://hanj.cs.illinois.edu/pdf/sigmod15_jliu.pdf
[5]: https://dsc-capstone.org/projects-2020-2021/reports/project_42.pdf
[6]: https://www.naturalearthdata.com/
[7]: https://www.sciencedirect.com/science/article/pii/S0304393203001247
[8]: https://www.cs.cmu.edu/~ark/personas/
[9]: https://www.cs.cmu.edu/~dbamman/pubs/pdf/bamman+oconnor+smith.acl13.pdf









