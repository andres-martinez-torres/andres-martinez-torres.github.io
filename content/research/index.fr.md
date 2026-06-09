+++
title = 'Recherche'
showDate = false
showReadingTime = false
showTableOfContents = true
showComments = false
+++


## Décoder la radicalisation en ligne : l’approche par la théorie du signal

La plupart des recherches sur l’extrémisme et la polarisation en ligne tentent de sonder l’esprit des individus pour comprendre leurs motivations personnelles, ou passent des années à décoder l’idéologie spécifique d’un groupe.

Mes travaux de doctorat adoptent une approche différente. Les communautés en ligne radicales étant souvent anonymes, pseudonymes et hostiles aux chercheurs extérieurs, il est incroyablement difficile de cerner les intentions individuelles. Même si l’on parvenait à interroger le membre d’un groupe, une personne qui accepte de collaborer avec des chercheurs ( issue d’un milieu qui s'y refuse d'ordinaire) : représente-t-elle réellement son groupe ? Collabore-t-elle de bonne foi ?

Au lieu de cela, ma thèse déplace la focale : il ne s'agit plus de savoir *pourquoi* les individus rejoignent ces groupes, mais de comprendre **comment ces groupes fonctionnent en tant que systèmes de communication**.

Pour ce faire, j’aborde l’identité en ligne comme un système de **signalisation biologique**.

---

## Signaux et récompenses

Dans la nature, un signal survit s'il obtient une réaction utile de son environnement ; il disparaît s'il est ignoré ou puni.

Certaines araignées, par exemple, se disputent les toiles. Lorsqu'une toile est déjà occupée, l’araignée « envahisseuse » va délibérément faire vibrer les fils pour afficher sa force et sa taille. L’araignée « défenseuse » perçoit cette vibration et évalue son adversaire sur cette base. Si elle estime que le combat est perdu d’avance, elle abandonne la toile. Cette vibration de la toile est un signal. Si ce comportement s'est développé chez ces araignées, c’est parce qu’au fil de leur évolution, faire vibrer la toile a apporté une récompense (l’araignée occupante fuyait, évitant ainsi un affrontement). Avec le temps, les araignées qui ignoraient le signal d'un rival plus grand ont été tuées. À l'inverse, celles qui s'introduisaient sur une toile sans se signaler ne laissaient pas la possibilité à l’occupante de partir pacifiquement, ce qui conduisait l'envahisseuse à être tuée (si la défenseuse était plus forte) ou blessée, compromettant ses chances de reproduction. Seules les araignées capables de décoder le signal ont évité les combats inutiles et ont survécu pour se reproduire. C'est ainsi que le comportement de vibration de la toile a persisté.

Je soutiens que les communautés en ligne et l'identité qu'elles partagent fonctionnent exactement selon la même logique évolutionnaire. Un marqueur identitaire  (par example, un terme d’argot spécifique, d’un << meme >>  ou d’une opinion radicale) est un signal.

* Si la communauté récompense ce signal par de l’engagement, des mentions « j’aime » ou de la validation, l’utilisateur réitère le comportement.
* Si une publication est moquée ou ignorée, le comportement s'estompe.

Au fil du temps, le signal peut évoluer (par exemple, se radicaliser) et, s'il est récompensé, c'est l'ensemble du groupe qui se radicalisera.

Mes travaux font le lien entre des théories sociologiques classiques, comme la mise en scène de soi face à un public (Goffman) et l'influence du climat de l'opinion publique sur nos discours (Noelle-Neumann), et des données computationnelles modernes. J'opérationnalise cette approche à travers trois étapes méthodologiques concrètes au fil des chapitres de ma thèse.

---
## Sections de la thèse et publications

### 1. Les récompenses sociales dans la « Manosphère »

* **L'objectif :** Comprendre comment les sous-cultures en ligne forment et maintiennent leur identité au fil du temps.
* **La méthode :** J’ai analysé une décennie de données issues de *The Red Pill* — un forum central de la « Manosphère » — en combinant l'analyse de réseaux sociaux et le traitement automatique du langage naturel (NLP). En suivant la manière dont certains marqueurs identitaires étaient récompensés par l'approbation des utilisateurs, j'ai retracé l'évolution du groupe et mesuré l'impact de chocs externes (tels que l'élection présidentielle américaine de 2016) sur son identité collective.

[Article (en anglais) disponible ici](https://www.sciencedirect.com/science/article/pii/S0001691826002416?via%3Dihub).


### 2. Cartographier la polarisation dans l'espace linguistique

* **L'objectif :** Déterminer si l'on peut mesurer le degré de polarisation d'un débat simplement en observant la facilité avec laquelle on peut identifier l'appartenance d'un individu à un groupe.
* **La méthode :** Ce travail aborde la polarisation comme un problème d'identification. Lorsque vous rejoignez une discussion, pouvez-vous facilement identifier la position de quelqu'un (**identifiabilité**) et distinguer les factions opposées (**distinguabilité**) ? Plus cela est facile, plus le débat est polarisé. Par exemple, un utilisateur qui emploie une insulte raciste est beaucoup plus facile à situer idéologiquement que quelqu'un qui écrit « J'aime regarder le foot ». En utilisant des plongements de mots (*word embeddings*), nous avons cartographié les utilisateurs dans un espace linguistique multidimensionnel. Nous avons testé ces métriques sur les tweets du Congrès américain ainsi que sur les débats relatifs à la vaccination contre le COVID-19 en Afrique du Sud afin de prouver leur efficacité pour suivre l'évolution de la polarisation au fil du temps.
* **Code :** Les méthodes développées ici sont entièrement accessibles dans mon package Python open source, `pons_py`. [Voir le dépôt de code sur GitHub](https://github.com/andres-martinez-torres/pons_py).
* **Statut :** À paraître.


### 3. *Phenomenologically Human* : l'utilisation des LLM pour l'étude éthique, générative et reproductible de communautés inaccessibles

* **L'objective :** Comment étudier de manière sûre et éthique une communauté radicale qui a été bannie ou qui est fermée aux chercheurs ?
* **La méthode :** Nous avons introduit un paradigme génératif pour les sciences sociales en entraînant des modèles de langage (*fine-tuning* de Llama 3.2 et Mistral) sur les données d'un forum banni de la « Manosphère » (*r/AskTRP*). À l'aide d'analyses TF-IDF et d'un test de Turing humain, nous avons démontré que ces modèles assimilaient avec succès les signaux linguistiques et identitaires de cette communauté. Nous qualifions ces modèles de *phenomenologically human* (phénoménologiquement humains).
Ils agissent comme des membres simulés de la communauté sur lesquels les chercheurs peuvent mener des expériences en toute sécurité, sans risques éthiques ou logistiques. Utiliser le modèle de base comme groupe témoin nous permet de modifier l'échantillon de la communauté auquel le modèle est exposé (par exemple, les publications les plus aimées, les moins appréciées...) afin d'en comprendre les effets et ce que cela révèle sur le groupe. Un chapitre ultérieur de ma thèse (non publié) utilise cette méthode pour mener une étude qualitative de la communauté, en posant au modèle des questions absentes du jeu de données initial et en analysant ses transformations avant et après l'entraînement.

[Article (en anglais) disponible ici](https://www.sciencedirect.com/science/article/pii/S294988212600023X).