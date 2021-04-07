---
title: Rendre les jeux vidéo accessibles aux justifications professionnelles et aux considérations relatives à la conception
description: Cet article est destiné aux développeurs de contenu de jeu et aux producteurs qui veulent atteindre le marché de la communauté d’accessibilité en ajoutant des fonctionnalités d’accessibilité de base pour aider les personnes atteintes de handicaps ou de troubles.
ms.assetid: 95580b75-fb8e-b8a9-2137-40d6c60ae35d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74499068877a400a94eb0ca32c2a1aff4bcf6c6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728596"
---
# <a name="making-video-games-accessible-business-justifications-and-design-considerations"></a>Rendre les jeux vidéo accessibles : justifications et considérations relatives à la conception

Les éditeurs de jeux et les développeurs aiment se concentrer sur les fonctionnalités dont les titres seront remarqués par la communauté de jeux, tels que les graphiques et l’audio. Mais il existe un autre public, qui souhaite participer à ces jeux également. Ces joueurs proviennent de la communauté d’accessibilité, d’une communauté de personnes handicapées, ainsi que de ceux qui s’occupent de leur bien-être.

Cet article est destiné aux développeurs de contenu de jeu et aux producteurs qui veulent atteindre le marché de la communauté d’accessibilité en ajoutant des fonctionnalités d’accessibilité de base pour aider les personnes atteintes de handicaps ou de troubles. Les rubriques suivantes sont abordées :

-   [Qu’est-ce que l’accessibilité ?](#what-is-accessibility)
-   [Pourquoi l’accessibilité est-elle importante ?](#why-is-accessibility-important)
-   [L’état de l’accessibilité dans le secteur des jeux](#the-state-of-accessibility-in-the-games-industry)
-   [Besoin de jeux accessibles](#the-need-for-accessible-games)
-   [Handicaps](#visual-impairments)
-   [Troubles de l’audit](#auditory-impairments)
-   [Troubles de la mobilité](#mobility-impairments)
-   [Troubles de la voix](#vocal-impairments)
-   [Conclusion](#conclusion)
-   [Plus de ressources](#more-resources)

## <a name="what-is-accessibility"></a>Qu’est-ce que l’accessibilité ?

Souvent, lorsque des personnes pensent à l’accessibilité, elles pensent à des éléments tels que les rampes de fauteuil roulant et le sous-titrage sur la télévision. Cela est dû au fait que ces types de fonctionnalités d’accessibilité sont utilisés par ceux qui ont des handicaps évidents. Toutefois, les fonctionnalités d’accessibilité ne sont pas conçues uniquement pour les personnes présentant les handicaps les plus graves. Parmi les utilisateurs de l’ordinateur américain qui vont de 18 à 64 ans, 57% (74,2 millions) sont susceptibles de tirer parti de l’utilisation de technologies accessibles en raison de handicaps et de troubles susceptibles d’avoir un impact sur l’utilisation des ordinateurs. («[Le marché des technologies accessibles : la vaste gamme de capacités et son impact sur l’utilisation des ordinateurs](https://www.microsoft.com/enable/research/phase1.aspx)», Microsoft Corporation La possibilité de faire tourner le volume d’un Payphone permet aux personnes ayant une perte d’audition légère de les utiliser. Un rail à la main sur un vol d’escaliers permet à une personne handicapée de les monter plus facilement.

Parfois, les fonctionnalités standard d’un produit finissent par être des fonctionnalités qui peuvent aider les personnes présentant un handicap. Par exemple, une personne ayant un handicap peut utiliser les paramètres de contraste sur une télévision pour faciliter la visualisation de l’écran. Une personne ayant une maladie de Parkinson peut utiliser une numérotation tactile pour faciliter l’appel téléphonique.

Les fonctionnalités d’accessibilité ont généralement tendance à répondre à l’un des cinq types de handicaps suivants :

-   Acuité visuelle, incapacité à distinguer les couleurs, une vision floue, etc.
-   Audition : malentendants, sourds.
-   Troubles de la parole, différences de langue.
-   Mobilité-poignet, bras, Leg et handles.
-   Troubles de la formation cognitive et défis de raisonnement, y compris la dyslexie.

Dans le contexte des jeux vidéo, l’ajout d’une accessibilité consiste à rendre un titre utilisable par une personne présentant l’un de ces handicaps.

## <a name="why-is-accessibility-important"></a>Pourquoi l’accessibilité est-elle importante ?

Il existe des raisons sociales et financières pour lesquelles les développeurs de jeux doivent penser à rendre leurs produits accessibles.

Pour les enfants et les jeunes adultes qui présentent des handicaps allant de modéré à grave, les jeux vidéo peuvent offrir un certain nombre d’avantages. Les chercheurs de la Jesuit University ont récemment découvert que la diffusion de jeux sportifs ou la lutte contre les jeux aide des enfants et des jeunes adultes souffrant de douleurs chroniques (le journal Edmonton, du 13e au 13 février 2006). En outre, les jeux vidéo ont été prouvés pour aider les enfants à faire face à la chirurgie plus efficacement et avec moins d’effets secondaires, par rapport à tranquilizers (la presse associée, 19 décembre 2004). Les jeux sont même utilisés pour le traitement du cancer ; l’exercice, essentiel à la récupération après la chimiothérapie, a été encouragé par l’utilisation de jeux tels que la révolution de danse (c) lorsque les enfants refusent de participer à d’autres formes d’activité physique.

En outre, permettre aux personnes ayant des handicaps (en particulier les enfants) de participer à des activités que la plupart des personnes apprécient et prendre à accorder peut contribuer à réduire la douleur émotionnelle et la sensation de capter.

Les raisons sociales ne sont pas les seules raisons pour lesquelles les développeurs de jeux doivent introduire des fonctionnalités d’accessibilité dans leurs titres. Les fonctionnalités d’accessibilité peuvent augmenter les ventes en encourageant les personnes handicapées à acheter un titre accessible. Les ventes accrues peuvent également provenir de joueurs qui souhaitent prendre en charge une société qui prend en charge la communauté d’accessibilité. Et enfin, le P.R. positif à partir du support et des groupes de pression d’accessibilité, il offre une publicité gratuite.

La demande d’accessibilité continuera à croître à mesure que le cheptel de jeu vieillit. Au fur et à mesure que les gens évoluent, les plus faibles peuvent devenir plus graves. En outre, les gens sont susceptibles de développer de nouvelles difficultés et de handicaps au fur et à mesure de leur âge. L’ajout de fonctionnalités d’accessibilité de base aux titres peut aider les éditeurs et les développeurs à continuer à attirer leurs revenus à partir de ces clients.

## <a name="the-state-of-accessibility-in-the-games-industry"></a>L’état de l’accessibilité dans le secteur des jeux

Pour la plupart des jeux, l’accessibilité dans les jeux vidéo est une priorité basse. L’une des raisons est due à un manque de sensibilisation entre les développeurs concernant les problèmes d’accessibilité : les développeurs qui ne sont pas désactivés peuvent ne pas savoir comment rendre un titre plus accessible aux personnes atteintes de handicaps.

Une autre raison est que les développeurs disposent d’une quantité limitée de temps et de ressources. Les analyses coût-avantage concluent souvent des problèmes d’accessibilité qui ne méritent pas l’attention et l’investissement de l’industrie des jeux en raison d’hypothèses comme :

-   Le coût de l’implémentation des fonctionnalités d’accessibilité ne justifie pas le retour.
-   Il n’y a pas suffisamment d’audience pour faciliter le développement de l’accessibilité.

Ces hypothèses sont défectueuses. Le fait de rendre les jeux accessibles est bien adapté à l’investissement.

## <a name="the-need-for-accessible-games"></a>Besoin de jeux accessibles

En 2003, Microsoft Corporation a été interrogé par Forrester Research, Inc., pour effectuer une étude complète visant à mesurer le marché actuel et potentiel des technologies accessibles dans le États-Unis et à comprendre comment les technologies accessibles sont actuellement utilisées. L’étude a déterminé que 57% des utilisateurs de l’ordinateur sont susceptibles de tirer parti de l’utilisation de la technologie accessible. Et la demande d’accessibilité future est prévue uniquement pour croître («[technologie accessible dans le calcul : examen de la sensibilisation, de l’utilisation et du potentiel futur](https://www.microsoft.com/enable/research/phase2.aspx)», Microsoft Corporation).

**Figure 1. Croissance prédite du nombre d’utilisateurs de technologies accessibles allant de 2003 à 2010**

![croissance prédite du nombre d’utilisateurs de technologies accessibles allant de 2003 à 2010](images/accessibility-growth.gif)

L’étude a également déterminé que l’utilisation des fonctionnalités d’accessibilité n’était pas limitée aux personnes handicapées. Parmi les utilisateurs d’ordinateurs qui utilisent des utilitaires et des options d’accessibilité intégrées :

-   32% n’ont pas d’handicap ou de déficience.
-   68% ont un handicap ou un handicap sérieux ou sérieux.

L’observation empirique suggère qu’il ne s’agit pas simplement d’une tendance limitée aux PC. Les fonctionnalités d’accessibilité sont souvent utilisées par des personnes sans handicap simplement pour améliorer leur expérience de jeu. Par exemple, un joueur peut compenser un handicap temporaire (tel qu’un pouce brisé), des problèmes environnementaux (tels que le bruit de fond) ou d’autres facteurs de situation.

Étant donné l’augmentation potentielle de l’utilisation de la technologie d’accessibilité, il est essentiel d’éduquer la direction, les concepteurs, les développeurs et les testeurs. De nombreuses entreprises cherchent des moyens de développer sur de nouveaux marchés en dehors des données démographiques de 18-32 mâles. Bien que les éditeurs mullent de savoir comment convaincre peu Suzy de jouer à des jeux ou à grand-mère et grand pour prendre en charge un contrôleur, il existe un marché constitué de personnes qui veulent que désespérément lisent des jeux qui ne seront pas remarqués. Le chiffre d’affaires potentiel qui peut être obtenu à partir d’un effort relativement faible fournissant des fonctionnalités d’accessibilité de base dans un titre est très tangible.

L’inclusion de fonctionnalités d’accessibilité de base dans un titre peut augmenter les ventes par le biais d’un « effet domino », par exemple, en arrivant à des joueurs qui ne peuvent normalement pas jouer le titre ou qui auraient fortement diminué leur expérience. En atteignant ces joueurs, vous accédez également à la communauté d’accessibilité (qui est connue pour un partage rapide des informations sur les produits accessibles et sa prise en charge fidèle des entreprises qui favorisent l’accessibilité). Par extension, les entreprises qui prennent un rôle actif dans cette communauté bénéficient d’une exposition positive aux médias.

En n’incluant pas les fonctionnalités d’accessibilité, vous courez le risque de boycotts et de poursuites potentiels, ainsi que la perte de ventes qui en résulte. De nombreux détaillants et compagnies aériennes ont fait l’expérience d’une absence d’accessibilité et, dans le secteur de la technologie, la communauté aveugle boycotted Internet Explorer 4 pour son manque d’accessibilité.

Voici les différentes catégories de handicaps. Chaque catégorie comprend des suggestions relativement faciles à implémenter qui peuvent rendre un titre accessible à un public plus vaste.

## <a name="visual-impairments"></a>Handicaps

*«Ma présentation a été suivie d’une session de questions et réponses vivantes, et un moment notable s’est produit quand l’un des employés a posé une question sur l’accessibilité dans \[ nos \] jeux... ce personnel de 28 ans est un joueur Avid qui a utilisé pour jouer \[ notre jeu \] avec un grand cercle d’amis. Dans la mesure où il est aveugle en couleurs, il était difficile pour lui de dire aux bons responsables de savoir que le jeu est devenu trop frustrant. Quand la nouvelle version... et \[ que nous n’avons pas \] résolu le problème, il et ses amis ont décidé d’acheter le jeu d’un concurrent à la place.» un cadre de l’industrie anonyme*

Le terme « troubles de la vision » est souvent à l’esprit d’une personne totalement aveugle. Toutefois, il est étonnante de savoir que 8,7% de la population masculine est affectée par un niveau de cécité des couleurs («[Comment les gens héritent-ils de Colorblindness ? À quelle fréquence ?](https://www.webexhibits.org/causesofcolor/2C.mdl), "webexhibits.org). Un autre 1,2% des personnes sont affectées par des formes plus sévères de handicap («[informations d’invalidité : feuille de faits de troubles](https://nichcy.org/disability/specific/visualimpairment)de la vision », « centre de diffusion national pour les enfants avec handicaps »). Cela signifie que presque un des 10 joueurs potentiels rencontrent des problèmes affectant leur vision et qui peuvent avoir un impact sur leur expérience de jeux.

Pour vous aider à comprendre les problèmes de handicap, imaginez que :



| Vous êtes un joueur      | Et vous êtes dans ce scénario                                                                                                                                                                         |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Avec vision normale   | Elle est brillante et ensoleillée, ce qui signifie que vous ne pouvez pas voir les objets sombres sur votre écran. <br/> Vous avez un ancien ensemble de télévision pour que vous ne puissiez pas voir les petits objets et le texte en raison d’une qualité d’image médiocre. <br/> |
| Avec une vision altérée | Un texte de jeu est tellement petit que vous ne pouvez pas le lire. <br/> Vous êtes aveugle. vous ne savez pas quel bouton appuyer lorsque le jeu vous demande d’appuyer sur le bouton rouge. <br/>                   |



 

À l’aide de quelques étapes et fonctionnalités simples, vous pouvez résoudre ces problèmes et améliorer l’expérience de jeu pour les joueurs avec une vision et des joueurs normaux avec un handicap.

1.  Titres de test sur les télévisions noires et blanches. Notez toutes les instances où les éléments, les joueurs, les objectifs et les commandes ne peuvent pas être distingués et ajustez votre palette de couleurs en conséquence.
2.  Donnez aux joueurs la possibilité d’augmenter la taille du texte sur leur écran. Offrent également la possibilité de modifier le taux de défilement du texte. Il est important de se souvenir que l’expérience de la console est de 10 mètres, et non de l’expérience de jeu de 2 pieds que de nombreux développeurs de PC sont utilisés. Même pour les joueurs sans problèmes de vision, les petites IU et le texte peuvent être difficiles à lire sur de longues distances.
3.  Fournissez des fonctionnalités de conversion de texte par synthèse vocale qui peuvent générer la voix sur tout le texte du jeu, y compris les menus de jeu qui suivent le focus sur les boutons. Permet à l’utilisateur de contrôler la vitesse, le pas et le sexe de la voix. Pour éviter que la conversion de texte par synthèse vocale ne soit submergée par d’autres bruits de jeu, donnez aux utilisateurs la possibilité d’ajuster le volume de voix, le bruit ambiant, les sons de jeu actifs et la musique. Incluez également l’option permettant de lire des sons distincts lors de la transition à travers les éléments de menu et les boutons.
4.  Enfin, donnez aux joueurs la possibilité de modifier les paramètres de luminosité et de contraste dans le jeu. Fournir aux utilisateurs la possibilité de choisir leurs propres jeux de couleurs personnalisés afin que les couleurs du texte, de l’arrière-plan et du HUD puissent être personnalisées pour répondre aux besoins d’un individu.

## <a name="auditory-impairments"></a>Troubles de l’audit

*«Les souvenirs de Half-Life renvoient à Haunt US comme un autre chef de chef technologique \[ \] est inutile pour les passionnés de malentendants... Nous espérons qu’aucun prier ! cela si Halo 2 ne voit pas la lumière du jour qu’il sera entièrement sous-titre.» www.DeafGamers.com*

La forme la plus répandue suivante de handicaps pouvant affecter le jeu est l’un des handicaps. Aux États-Unis seuls, plus de 28 millions personnes sont affectées par un type de handicap auditif. Alors que les troubles de l’audition sont souvent associés à l’âge, 17 des enfants 1 000 de plus de 18 ans sont affectés par un handicap auditif («[statistiques sur les troubles auditifs, les infections de l’oreille et les sourds](https://www.nidcd.nih.gov/health/statistics/pages/hearing.aspx)», « Institut national de l’sourd et autres troubles de la communication »). Lorsque l’un d’eux estime que les joueurs d’aujourd’hui sont plus anciens et perdent leur audition à un rythme toujours plus croissant, il est clair que la demande d’accessibilité audio ne peut croître.

Pour vous aider à comprendre les problèmes de dégradation de l’audit, imaginez que :



| Vous êtes un joueur           | Et vous êtes dans ce scénario                                                                                                                                                                                                                                                            |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Avec audition normale       | Vous ne souhaitez pas déranger les personnes afin de vous lancer avec le son muet, mais vous ne pouvez pas jouer au jeu, car les directions ne sont fournies qu’en audio. <br/>                                                                                                                               |
| Avec un handicap auditif | Vous jouez à un tiers fort, mais vous ne pouvez pas dire que vous êtes en feu, car vous ne pouvez pas entendre les coups de pistolet.<br/> Le jeu présente de nombreux bruits ambiants et vous ne pouvez pas entendre les instructions orales qui vous sont fournies. <br/>                                                     |
| Qui est sourd               | Les commentaires audio sont tellement souples, vous ne pouvez pas les entendre, même dans une salle de tranquillité. <br/> Tous vos objectifs vous sont attribués dans l’audio et vous ne pouvez pas déterminer ce que vous êtes censé faire. <br/> Tout le scénario est donné oralement, et vous ne pouvez pas suivre la procédure. <br/> |



 

Avec un travail relativement mineur, vous pouvez rendre votre jeu utilisable et agréable pour les joueurs avec une audition normale et pour les joueurs qui présentent un handicap auditif.

1.  Fermez la légende de toutes les boîtes de dialogue. Cela comprend le contenu et les cinémas dans le jeu. Donnez à ce joueur la possibilité d’activer et de désactiver ces sous-titres.
2.  Lorsqu’un effet sonore fournit des informations essentielles, fournissez également un mécanisme textuel ou tactile (vibrations) pour les commentaires. Par exemple, si une bombe dans votre jeu rend un bruit de bip plus rapide proche de son explosion, fournissez un indicateur visuel (tel qu’une barre de temps) qui permet également au joueur de connaître le temps restant avant l’explosion.
3.  Si votre jeu prend en charge la lecture en ligne, donnez aux joueurs la possibilité d’envoyer des SMS et d’utiliser leur voix pour fournir des informations aux membres de l’équipe et à d’autres joueurs en ligne. Un casque n’est pas utile pour une personne qui ne peut pas entendre et, de plus en plus, les joueurs cherchent à jouer avec d’autres personnes avec lesquelles ils peuvent communiquer et se manipuler en ligne.

## <a name="mobility-impairments"></a>Troubles de la mobilité

*«Videogames offre aux personnes handicapées la possibilité de se reconnecter avec leurs pairs et leurs aptitudes qui ont été perdues ou jamais. Mon expérience personnelle vient d’être paralysé à l’âge de 14 ans et à visiter le centre de loisirs de l’hôpital, et le seul intérêt que je devais sortir de ma dépression était de jouer le système Videogame. Je perdais rapidement de l’intérêt lorsque j’ai appris que je ne pouvais pas les lire...» Robert Florio*

Les handicaps de mobilité sont peut-être le plus difficile des différents handicaps sur lesquels il est possible d’acquérir des statistiques. Cela est principalement dû au fait que ces handicaps peuvent être dus à des maladies, à des troubles neurologiques, à une perte de membres/chiffres, à une paralysie, etc., chacun pouvant avoir un degré d’impact variable sur l’expérience d’un joueur vidéo. Ces handicaps peuvent être congénitals ou se produire plus tard.

Pour vous aider à comprendre les problèmes de dégradation de l’audit, imaginez que :



| Vous êtes un joueur                                 | Et vous êtes dans ce scénario                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sans aucun handicap de mobilité                     | Le contrôleur de jeu comporte un grand nombre de boutons, vous (en tant que passionnés) sont intimidés et vous ne souhaitez pas apprendre à les utiliser. <br/>                                                                                                                                                                          |
| Avec un handicap de mobilité temporaire            | Vous ne pouvez pas utiliser le stick analogique sur votre contrôleur. <br/> Vous avez une jambe, vous ne pouvez pas utiliser le BMD pour un titre de danse.<br/>                                                                                                                                     |
| Avec un handicap de mobilité permanent et sérieux | Vous avez perdu un ARM. vous ne pouvez donc pas utiliser un contrôleur à deux mains. <br/> Vous avez une maladie de Parkinson, et cela vous permet de déclencher accidentellement des boutons sur le contrôleur. <br/> Vous êtes paralysé du cou. vous ne pouvez donc pas utiliser un contrôleur de jeu standard. <br/> |



 

Réfléchir à la prise en compte de tous ces joueurs est difficile, mais il y a des choses faciles à garder à l’esprit lors du développement de vos jeux.

1.  Réduire l’utilisation du bouton et en savoir plus sur les interfaces de menu pour les commandes. Cela s’avère particulièrement utile pour les personnes qui peuvent manquer des chiffres ou des mains. Elle est également utile pour les personnes paralysé qui utilisent des contrôleurs personnalisés.
2.  Autorisez les joueurs à personnaliser la configuration du contrôleur et la sensibilité du bouton/Stick. Cela permet aux personnes qui ont des problèmes de compétences de moteur précises de personnaliser le contrôleur afin de minimiser l’impact de leur handicap sur le jeu. Il permet également une meilleure prise en charge des contrôleurs personnalisés pour les personnes handicapées.
3.  Si votre jeu utilise un type spécifique de périphérique (patin, feu, etc.), autorisez les autres contrôleurs à exécuter les mêmes fonctions. Par exemple, un jeu tel qu’une révolution de danse (c) permet même aux personnes avec restriction de fauteuils de jouer avec leurs amis via l’utilisation d’un contrôleur de poche ordinaire.

## <a name="vocal-impairments"></a>Troubles de la voix

Les troubles de la voix constituent un pourcentage relativement faible de la communauté d’invalidité. Des statistiques spécifiques sont difficiles à venir, mais la preuve montre qu’une majorité des troubles de la voix sont liés à d’autres handicaps (tels que les troubles du moteur ou de l’audition). Toutefois, à mesure que d’autres éditeurs de jeux commencent à explorer l’utilisation de la conférence vocale et de la reconnaissance vocale dans leurs titres, les personnes ayant des troubles de la voix commencent à voir la qualité de leur expérience de jeux. Pour ce faire, il existe des fonctionnalités d’accessibilité de base qui peuvent être implémentées.

Pour vous aider à comprendre les problèmes de dégradation de l’audit, imaginez que :



| Vous êtes un joueur             | Et vous êtes dans ce scénario                                                                                                                                                                                                                                           |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sans aucun handicap vocal    | Vous jouez à un jeu qui requiert des commandes vocales pour contrôler vos caractères et vous ne pouvez pas jouer parce que vous n’avez pas de microphone. <br/> Vous jouez tard à la nuit et vous ne souhaitez pas perturber l’utilisation de votre Communicator. <br/> |
| Qui a un handicap vocal | Vous jouez à un jeu qui requiert des commandes vocales pour contrôler vos caractères et vous ne pouvez pas jouer parce que le jeu ne peut pas reconnaître ce que vous dites.                                                                                                               |
| Qui ne peut pas parler      | Le jeu que vous jouez nécessite une entrée vocale pour que vous ne puissiez pas le lire. <br/> Le jeu en ligne que vous jouez vous attend à ce que vous coordonniez la stratégie via le Communicator pour que vous ne soyez pas en mesure de jouer efficacement. <br/>                                               |



 

Heureusement, il existe des correctifs faciles qui peuvent rendre votre jeu utilisable et agréable pour ces joueurs.

1.  Si un jeu utilise la reconnaissance vocale, fournissez aux joueurs la possibilité de choisir des commandes à partir d’une combinaison de menus ou de boutons.
2.  Si votre titre prend également en charge le mode multijoueur en ligne, donnez aux joueurs la possibilité d’utiliser une macro personnalisable avec des messages audio ou (même mieux pour ceux avec des troubles de l’audition). La prise en charge du clavier pour la conversation est également une option.

## <a name="conclusion"></a>Conclusion

À ce stade, vous pensez peut-être que vous n’avez peut-être pas pu prendre en charge tous ces joueurs dans tous ces scénarios. Et même si vous deviez implémenter chaque suggestion dans ce document, vous ne pouviez pas vous assurer qu’un titre serait entièrement accessible à tout le monde. Toutefois, en suivant ces directives d’accessibilité, vous pouvez rendre votre titre plus attrayant pour la communauté d’accessibilité. Et cela peut uniquement augmenter les ventes.

Pour rendre un titre plus accessible, les développeurs et les éditeurs doivent rechercher des personnes avec différents types de handicaps pour tester l’utilisation de leurs jeux. Cette approche fournit des informations de première main indiquant si un jeu est accessible ou non à un public donné. En tant qu’avantage supplémentaire, le fait de disposer de diverses ressources de développement et de test peut offrir des Insights supplémentaires susceptibles d’améliorer le jeu pour tous les joueurs. Plus important encore, participez à la communauté d’accessibilité et familiarisez-vous avec ces clients potentiels. Organisez un match pour votre titre dans un centre de service sourd local, un hôpital d’enfants ou le centre de l’ancien combattant. Encouragez les développeurs et les testeurs à se déconnecter des organisations locales qui travaillent avec des personnes handicapées, à prendre une classe de langage de signature ou à s’inscrire à des bulletins d’informations d’accessibilité pour suivre la communauté. Sollicitez des commentaires sur les titres précédents à partir de jeux désactivés dans des écoles et lycées locaux.

Personne n’aime capter. En incluant la communauté d’accessibilité dans les tests et la conception de jeux, vous serez en mesure de commercialiser votre titre à un public bien plus vaste et de faire le bon choix pour la communauté et vos résultats.

## <a name="more-resources"></a>Ressources complémentaires

Il existe un certain nombre de ressources Web disponibles qui traitent de l’accessibilité des jeux vidéo, ainsi que d’un certain nombre de sociétés qui se concentrent sur les jeux désactivés. En outre, le groupe de technologies accessible chez Microsoft peut être contacté avec les questions d’accessibilité relatives aux PC à l’adresse suivante : ablecat@microsoft.com . Les questions relatives à l’accessibilité Xbox peuvent être envoyées à : xaccess@microsoft.com .

Sites d’invalidité générale :

-   [Accessibilité des jeux](https://www.game-accessibility.com/)
-   [Site d’accessibilité de Microsoft](https://www.microsoft.com/enable/)
-   [Accessibilité](/previous-versions/windows/internet-explorer/ie-developer/accessibility/gg701968(v=vs.85))

Sites de dégradation de l’audit :

-   [DeafGamers.com](https://www.deafgamers.com/)
-   [Bibliothèque de ressources sourdes](https://www.deaflibrary.org/)

Sites de troubles de la vision :

-   [Institut National Eye Institute](https://www.nei.nih.gov/)
-   [Vischeck](https://www.vischeck.com/)
-   [WebExhibits.org](https://www.webexhibits.org/causesofcolor/2.mdl)

Sites de handicap mobile :

-   [RobertFlorio.com](https://www.robertflorio.com/games)
-   [WebAIM](https://webaim.org/articles/motor/)

Sites de troubles de la parole :

-   [American Speech-Language-Association auditive](https://www.asha.org/public/speech/)

 

