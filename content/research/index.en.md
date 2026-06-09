+++
title = 'Research'
showDate = false
showReadingTime = false
showTableOfContents = true
showComments = false
+++

## Decoding Online Radicalization: A Signaling Approach

Most research on online extremism and polarization tries to look inside people's heads to understand their personal motivations, or spends years decoding the specific ideology of a group.

My doctoral research takes a different approach. Because radical online communities are often anonymous, pseudonymous, and hostile to outside researchers, understanding individual intentions is incredibly difficult. Even if one managed to interview a group member: does someone that collaborates with researchers (coming from a group that would not do that) really represent the group? Are they collaborating in good faith?

Instead, my thesis shifts the focus away from *why* individuals join these groups to **how these groups function as communication systems**.

To do this, I treat online identity as a system of **biological signaling**.

---

### Signals & Rewards

In nature, a signal survives if it gets a useful reaction from the environment; it dies out if it is ignored or punished. 

For example, certain spiders compete for webs. When the web is occupied by another spider, the 'invading' spider will purposefully shake the web to display its strength and size. The 'defending' spider will sense the vibration and judge its oponent based on it. If it believes that it is a losing fight, the defending spider leaves. The vibration of the web is a signal. It has evolved in these spiders because in their evolution, vibrating the web received a reward (the defending spider left the web and avoided a fight). Over time, the spiders that ignored the signal from a bigger spider were killed. The spiders that did not signal their entry into a web did not  give the defending spider the chance to leave peacefully, leading to the invading spider being killed (if the defender was bigger) or injured in the fight, damaging its chances for reproduction. Only the spiders that understood the signal avoided unnecessary fights and lived to reproduce. With them, the web vibration behaviour persisted. 

I argue online communities and the identity they share work the same way.

Online communities, I argue, share this evolutionary logic. An identity marker, like a specific slang word, a meme, or a radical opinion, is a signal.
* If the community rewards that signal with engagement, upvotes, or validation, the user repeats it.
* If a post is mocked or ignored, the behavior fades.
* Over time, the signal may change (eg., radicalize) and if it gets rewarded, the group overall will radicalize.

My work connects classical social theories—how we perform for an audience (Goffman) and how public opinion climates alter what we say (Noelle-Neumann)—with modern computational data. I break this down into three concrete methodological steps across my research chapters.

---

## Thesis Sections & Publications

### 1. Social Rewards in the "Manosphere"

* **The Focus:** How do online subcultures form and enforce their identity over time?
* **The Method:** I analyzed a decade of data from *The Red Pill*—a central forum within the "Manosphere"—using Social Network Analysis and Natural Language Processing (NLP). By tracking how specific identity markers were rewarded with user approval, I traced the group's evolution and measured how external shocks (like the 2016 US presidential election) altered the forum's collective identity.

[Read the paper here](https://www.sciencedirect.com/science/article/pii/S0001691826002416?via%3Dihub).

### 2. Mapping Polarization in Linguistic Space

* **The Focus:** Can we measure how polarized a debate is purely by looking at how easy it is to tell the group membership of an individual?
* **The Method:** This paper treats polarization as an identification problem. When you join a thread, can you easily identify where someone stands (**identifiability**) and distinguish the opposing factions (**distinguishability**)? The easier it is, the more polarized the debate is. For example, a user writing a racist slur is much easier to identify ideologically than someone posting "I enjoy watching football". Using a word-embeddings, we mapped users in high-dimensional linguistic space. We tested this on US congressional tweets and COVID-19 vaccination debates in South Africa to prove these metrics can track polarization changes over time.
* **Code:** The methods developed here are fully available in my open-source Python package, `pons_py`.  [View code repository on GitHub](https://github.com/andres-martinez-torres/pons_py).
* **Status:** Forthcoming.

### 3. Phenomenologically Human: Using LLMs for ethical, generative, and reproducible study of inaccessible communities

* **The Focus:** How do you safely and ethically study a radical community that has been banned or is closed to researchers?
* **The Method:** We introduced a generative paradigm for social science by fine-tuning Large Language Models (Llama 3.2 and Mistral) on data from a banned "Manosphere" forum (*r/AskTRP*). Using TF-IDF analysis and a human Turing test, we showed that these models successfully assimilated the community's linguistic and identity signals. We term these models "phenomenologically human". 

    They act as simulated community members that researchers can safely experiment on without ethical or logistical hazards. The ability to use the base model as control allows us to change what sample of the community the model is exposed to (e.g., the most liked posts, the least liked ones...), understand its effects, and what that says about the community.  A later chapter in my thesis (unpublished) utilises this method to qualitatively study the community, asking it questions that are not available in the dataset, and analysing the changes in the model before and after fine-tuning.

[Read the paper](https://www.sciencedirect.com/science/article/pii/S294988212600023X).