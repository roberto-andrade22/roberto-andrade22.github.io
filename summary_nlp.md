[Back to Portfolio](index)

---
## **Text Summarization with Transformers: *The Mandalorian* episode scripts**

### Summary

Due to the importance Natural Language Processing has, its seemingly limitless potential, and the great amount of models that are now readily available for it, it was of great interest to try and implement one of these models to perform a useful task. This project focused on text summarization.

As the title suggests, the topic was episode scripts from a TV show. In particular, seasons 1 and 2 from *The Mandalorian*, as well as season 1 from *The Book of Boba Fett*. The scripts were taken from [here](https://starwars.fandom.com/), and the model used to summarize them was T5-base, leveraging transformers.
<br>

<details>
  <summary markdown="span">Sample input for Episode 1. Click to expand</summary>
     Bar Fight  The episode opens with the eponymous Mandalorian bounty hunter (identified later in the series as Din Djarin) using a tracking fob on an icy planet called Pagodon . Inside a public house , a bearded human trawler and a Quarren trawler are manhandling a blue-skinned Mythrol man , who pleads for his life in Galactic Basic Standard , offering credits in exchange for his life. His pleas are ignored; the bearded trawler wants to kill him for his valuable musk. Before the two trawlers can do any more  harm, the armored and masked Mandalorian steps into the bar. Speaking in Huttese , the bearded trawler tells Djarin that he spilled his drink. Djarin ignores him and silently walks up to the counter. The bearded trawler reiterates his threat to Djarin. The human bartender tells Djarin that he says that he spilled his drink, translating into Basic. The Mythrol tries to break free but the Quarren holds him down. The two trawlers accost Djarin, taking a sudden interest in his beskar armor. The bartender tries... 
</details>
<br>
<details>
  <summary markdown="span">Sample output from Episode 1. Click to expand</summary>
    Din Djarin. Galactic Basic Standard : Bar Fight The episode opens with the eponymous Mandalorian bounty hunter using a tracking fob on an icy planet called Pagodon. Inside a public house, a . Speaking in Basic, the bearded trawler tells Djarin that he spilled his drink. Djarin ignores him and silently walks up to the counter. Speaking in Basic, the bearded trawler tells...
</details>
<br>

### References

* [Full output for all episodes](summaries_nlp)
* [Scripts](https://starwars.fandom.com/)
* [Transformers](https://huggingface.co/models)
* [Full Project](https://github.com/roberto-andrade22/MandoTextAnalytics)

---

[Back to portfolio](index)