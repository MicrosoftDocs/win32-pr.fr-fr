---
title: Facilité d’utilisation dans la conception de logiciels
description: Cette rubrique présente le concept d’utilisation et explique pourquoi elle doit être une partie importante de tout projet de conception de logiciels.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b302e63a475d060748e896440b28915816d910e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028756"
---
# <a name="usability-in-software-design"></a>Facilité d’utilisation dans la conception de logiciels

Cette rubrique présente le concept d’utilisation et explique pourquoi elle doit être une partie importante de tout projet de conception de logiciels.

-   [Introduction](#introduction)
-   [Définition de la facilité d’utilisation](#defining-usability)
    -   [Facilité d’utilisation](#ease-of-use)
    -   [Utilisation et utilitaire](#usability-vs-utility)
    -   [Pour l’utiliser et l’utiliser](#liking-it-vs-using-it)
    -   [Découverte et apprentissage et efficacité](#discovery-vs-learning-vs-efficiency)
    -   [Les slogans ne fonctionnent pas](#slogans-do-not-work)
-   [Pourquoi la convivialité est-elle importante ?](#why-is-usability-important)
    -   [Pourquoi devez-vous vous en soucier ?](#why-should-you-care)
    -   [À quoi cela coûte-t-il ?](#what-does-it-cost)
    -   [Comment améliorer l’utilisation ?](#how-do-i-increase-usability)
    -   [Pourquoi dois-je impliquer des utilisateurs ?](#why-should-i-involve-users)
    -   [Ne puis-je pas suivre les instructions ?](#cant-i-just-follow-guidelines)
    -   [Ai-je besoin de créer un laboratoire d’utilisation ?](#do-i-need-to-build-a-usability-lab)
    -   [Comment commencer ?](#how-do-i-get-started)

## <a name="introduction"></a>Introduction

Le terme « convivialité » dans le contexte de la création de logiciels représente une approche qui place l’utilisateur, au lieu du système, au centre du processus. Cette philosophie, connue sous le nom de conception centrée sur l’utilisateur, intègre les préoccupations des utilisateurs et leur défense dès le début du processus de conception, et détermine que les besoins de l’utilisateur doivent être les plus importants pour les décisions de conception.

L’aspect le plus visible de cette approche est le test d’utilisabilité, dans lequel les utilisateurs travaillent et interagissent avec l’interface du produit et partagent leurs vues et leurs préoccupations avec les concepteurs et les développeurs.

## <a name="defining-usability"></a>Définition de la facilité d’utilisation

La section définit ce que signifie la convivialité dans le contexte du développement de logiciels et la façon dont il est associé à d’autres aspects du processus de développement.

### <a name="ease-of-use"></a>Facilité d’utilisation

La facilité d’utilisation est une mesure de la facilité d’utilisation d’un produit pour effectuer des tâches prescrites. Cela est différent des concepts connexes de l’utilitaire et de l’équivalent.

### <a name="usability-vs-utility"></a>Utilisation et utilitaire

Un attribut central qui détermine la qualité d’un produit est utile. Cela mesure si les utilisations réelles d’un produit peuvent atteindre les objectifs que les concepteurs envisagent d’atteindre. Le concept de branches d’utilité est plus loin dans l’utilitaire et la convivialité. Bien que ces termes soient liés, ils ne sont pas interchangeables.

L’utilitaire fait référence à la capacité du produit à effectuer une tâche ou des tâches. Plus le produit est conçu pour effectuer de tâches, plus l’utilitaire est performant.

Envisagez les processeurs Word Microsoft MS-DOS standard à partir de la fin des années 1980. De tels programmes offraient de nombreuses fonctionnalités puissantes de modification et de manipulation de texte, mais nécessitaient des utilisateurs pour apprendre et mémoriser des dizaines de frappes de touches pour les exécuter. Les applications telles que celles-ci peuvent être considérées comme ayant un utilitaire de haut niveau (elles donnent aux utilisateurs les fonctionnalités nécessaires) mais une faible convivialité (les utilisateurs doivent consacrer beaucoup de temps et d’efforts pour les apprendre et les utiliser). En revanche, une application simple et bien conçue, telle qu’une calculatrice, peut être très facile à utiliser, mais n’offre pas beaucoup d’utilitaire.

Les deux qualités sont nécessaires à l’acceptation du marché, et les deux font partie du concept général de l’utilité. Évidemment, si un programme est hautement utilisable mais ne fait rien de valeur, personne ne l’utilise. Et les utilisateurs qui disposent d’un programme puissant, difficile à utiliser, résistent probablement à l’informatique ou recherchent d’autres solutions.

Le test d’utilisabilité vous aide à déterminer la facilité avec laquelle les utilisateurs effectuent des tâches particulières. Toutefois, il ne vous aide pas directement à déterminer si le produit lui-même a une valeur ou un utilitaire. (Les utilisateurs peuvent se renseigner sur les commentaires relatifs à l’utilitaire lors des tests d’utilisation, mais les commentaires doivent être vérifiés avec d’autres méthodes de recherche plus robustes.)

### <a name="liking-it-vs-using-it"></a>Pour l’utiliser et l’utiliser

L’équivalent est toujours une caractéristique souhaitable dans un produit. Si des personnes aiment le produit, elles sont plus susceptibles de l’utiliser et de la recommander à d’autres personnes. Mais comme avec l’utilitaire, vous devez veiller à ne pas vous confondre avec la convivialité.

Les gens aiment souvent un produit, pour des raisons non liées à l’utilitaire et à la convivialité. Ils peuvent être attirés sur son style ou sur l’État qu’ils pensent que le produit confère. Les gens aiment généralement des produits hautement utilisables, mais vous ne devez pas supposer que cela signifie qu’un produit bien aimé est utilisable.

La facilité d’utilisation consiste à déterminer si une personne peut utiliser le produit pour effectuer les tâches qu’elle doit effectuer. Le test d’utilisabilité mesure principalement les performances, et non les préférences. Toutefois, les questionnaires standardisés peuvent être utilisés pour mesurer les préférences d’un produit à l’autre.

### <a name="discovery-vs-learning-vs-efficiency"></a>Découverte et apprentissage et efficacité

Il existe de nombreux aspects de l’utilisation, mais traditionnellement, le terme fait référence spécifiquement aux attributs de la découverte, de l’apprentissage et de l’efficacité.

-   La découverte consiste à rechercher et à trouver la fonctionnalité d’un produit en réponse à un besoin particulier. Les tests d’utilisabilité peuvent déterminer combien de temps il faut à un utilisateur pour trouver une fonctionnalité et le nombre d’erreurs (choix incorrect sur l’emplacement) que l’utilisateur effectue en cours de route.
-   L’apprentissage fait référence au processus par lequel l’utilisateur sait comment utiliser une fonctionnalité découverte pour effectuer une tâche. Les tests d’utilisabilité peuvent déterminer la durée d’exécution de ce processus, ainsi que le nombre d’erreurs que l’utilisateur effectue pendant l’apprentissage de la fonctionnalité.
-   L’efficacité fait référence au point auquel l’utilisateur a « masterisé » la fonctionnalité et l’utilise sans nécessiter d’apprentissage supplémentaire. Les tests d’utilisabilité peuvent déterminer le temps nécessaire à l’utilisateur expérimenté pour exécuter les étapes nécessaires à l’utilisation de la fonctionnalité.

Ces trois aspects essentiels de la convivialité sont fortement influencés par la nature de la tâche en cours et la fréquence à laquelle l’utilisateur l’exécute. Certaines fonctionnalités sont rarement utilisées ou sont tellement complexes que l’utilisateur les réapprend essentiellement à chaque fois. pour ces fonctionnalités, Microsoft développe souvent des assistants pour guider l’utilisateur tout au long du processus.

### <a name="slogans-do-not-work"></a>Les slogans ne fonctionnent pas

Les développeurs de logiciels pensent parfois que des slogans simples tels que « rendre le produit plus utilisable » vous aideront à résoudre les problèmes d’utilisation. Bien qu’une attitude positive à la convivialité soit importante, seuls les tests d’utilisation appropriés avec des utilisateurs ordinaires, dans le contexte du produit en cours de création, peuvent fournir aux développeurs les informations dont ils ont besoin pour créer un produit répondant aux besoins des utilisateurs. « Rendre le produit plus utilisable » doit être le slogan de chaque développeur de logiciels, mais il n’est utile que si le développeur connaît l’utilité de la convivialité. Le test avec les utilisateurs ordinaires est le moyen le plus fiable pour le savoir.

## <a name="why-is-usability-important"></a>Pourquoi la convivialité est-elle importante ?

La section répond à certaines questions courantes sur la raison pour laquelle la convivialité est importante et explique comment incorporer des principes de conception centrés sur l’utilisateur dans le processus de développement.

### <a name="why-should-you-care"></a>Pourquoi devez-vous vous en soucier ?

Si les considérations relatives à la convivialité n’ont pas encore été incorporées dans le processus de conception du produit, vous vous demandez peut-être pourquoi il est nécessaire ou souhaitable. Après tout, il est tout à fait possible de publier un produit fonctionnel sans bogue sans effectuer de travail d’utilisation. Toutefois, l’incorporation de principes de conception centrés sur l’utilisateur peut mener à un produit nettement amélioré dans plusieurs domaines.

La meilleure raison d’effectuer des tests d’utilisation consiste à réduire le nombre d’appels au support technique des utilisateurs. Une mauvaise convivialité est la raison pour laquelle les utilisateurs appellent des lignes de support technique, et chaque responsable de logiciel et gestionnaire des services d’information sait comment le support produit peut être coûteux. En outre, la facturation des utilisateurs pour le support augmente le risque de mécontentement du produit. Si les utilisateurs trouvent qu’il est facile d’utiliser votre produit, ils n’ont pas besoin d’appeler le support technique.

Pour les logiciels produits pour une utilisation interne, la meilleure raison de faire de la convivialité une partie importante du processus de développement est de réduire les coûts de formation. Un produit hautement utilisable est beaucoup plus facile à apprendre pour les utilisateurs qu’un produit pour lequel la convivialité n’était pas une priorité élevée. Les utilisateurs apprennent plus rapidement les fonctionnalités et conservent leurs connaissances plus longtemps, ce qui met directement en corrélation pour réduire les coûts de formation et le temps.

Le test d’utilisabilité permet d’améliorer l’acceptation de l’utilisateur. L’acceptation résulte d’un certain nombre de facteurs, notamment la convivialité, l’utilitaire et l’utilisation. Pour les produits vendus au détail, l’acceptation des utilisateurs se met souvent en corrélation avec les achats répétés ou la loyauté, ce qui signifie que l’utilisateur est susceptible de recommander le produit à d’autres utilisateurs. Pour les applications internes, l’acceptation des utilisateurs est corrélée à la volonté d’utiliser le logiciel pour effectuer les tâches pour lesquelles il a été conçu, ce qui permet d’accroître la productivité. L’augmentation de la convivialité est l’un des facteurs qui peuvent contribuer à augmenter l’acceptation de l’utilisateur.

La convivialité peut vous aider à différencier vos produits de ceux de vos concurrents. Si deux produits sont sensiblement égaux dans l’utilitaire, le produit avec une meilleure convivialité sera probablement considéré comme supérieur. En outre, les recommandations en matière de programmation et d’apparence de Windows et d’accompagnement ont fait l’audit du champ de jeu de l’interface utilisateur de base, de sorte que de nombreux programmes qui traitent des fonctions similaires s’affichent et agissent de manière différente. Ces similarités signifient que les petites différences en matière de convivialité peuvent avoir un impact important sur la préférence de l’utilisateur.

Enfin, chaque produit est testé en vue d’une utilisation finale. Les utilisateurs effectuent des tests d’utilisation sur le produit chaque fois qu’ils l’utilisent, et ils affichent leur verdict par le biais de leur utilisation continue ou de leur absence. Tester le produit avant de le publier sur le marché peut aider à garantir que les expériences des utilisateurs avec le produit sont positives.

### <a name="what-does-it-cost"></a>À quoi cela coûte-t-il ?

Les développeurs de logiciels et les chefs de projet se préoccupent souvent que le lancement d’un processus de conception centré sur l’utilisateur et l’exécution de tests d’utilisation corrects nécessiteront des temps et de l’argent inacceptables. En réalité, le coût du temps et de l’argent consacrés à l’utilisateur est souvent relativement faible et, par conséquent, par rapport au coût de l’absence.

Considérons, par exemple, le coût en temps et en argent d’une révision de conception tardive dans le cycle de développement, par opposition à une date antérieure, lorsque le produit est toujours sur la planche de dessin. Attendre la fin de la période bêta pour exposer les utilisateurs au produit à des fins de test d’utilisabilité peut entraîner un démontage des parties du programme dont le développement a duré beaucoup de temps. Et l’attente jusqu’à la publication du produit, puis l’apport de modifications sur la base de commentaires négatifs ou la prise en charge d’une conception médiocre peuvent augmenter la valeur de façon inattendue en raison des coûts de support produit élevés ou de la réception insuffisante par les utilisateurs.

Une étude d’utilisabilité raisonnable peut généralement être effectuée en environ deux semaines ou moins, et peut réduire de manière considérable le temps et les coûts liés à l’apport de modifications à la fin du cycle de développement. Le coût d’exécution des tests varie en fonction de la nature du produit et des parties de l’interface qui sont testées.

Les tests d’utilisation sont comparables au test de code. Les chefs de projet réussissaient un compte pour le test de code lors de la planification d’un projet de développement. Ils ne le voient pas comme un fichier supplémentaire qui doit être affiché dans le calendrier et le budget du projet. Au lieu de cela, les chefs de projet acceptent les tests de code comme un coût de travail, car l’alternative est tellement plus coûteuse. Il en va de même pour les tests d’utilisation.

### <a name="how-do-i-increase-usability"></a>Comment améliorer l’utilisation ?

Lors de la lecture et de la compréhension de l’importance de la convivialité, les développeurs de logiciels sont parfois tentés d’ajouter de l’utilisation, comme s’il s’agissait d’un ingrédient qui peut simplement être ajouté à un produit pour le rendre plus utilisable. Au lieu de cela, la convivialité doit faire partie du processus de conception lui-même, plutôt que d’une « chose » ajoutée au processus ici ou là. La raison pour laquelle les experts de la convivialité se réfèrent au « focus de l’utilisateur » et à la « conception centrée sur l’utilisateur » est que la convivialité dépend de la conservation des besoins des utilisateurs au niveau du processus de conception. La conception centrée sur l’utilisateur par nécessité implique plus qu’une simple série de règles régissant le positionnement des boutons et des menus dans une interface. Le test de la convivialité est une opportunité de vérifier le travail de conception. Il n’est pas possible de « ajouter » une utilisation à un produit.

Gould, Boies et Lewis (1991) identifient quatre principes importants de la conception centrée sur l’utilisateur :

-   Concentrez-vous au plus tôt sur les utilisateurs.

    Les développeurs doivent se concentrer sur la compréhension des besoins des utilisateurs au début du processus de conception.

-   Conception intégrée.

    Tous les aspects de la conception doivent évoluer en parallèle, plutôt qu’en séquence. Conservez la conception interne du produit conformément aux besoins de l’interface utilisateur.

-   Tests précoces et continus.

    La seule approche actuellement réalisable de la conception de logiciels est empirique : la conception fonctionne si les véritables utilisateurs décident qu’elle fonctionne. L’intégration du test d’utilisabilité tout au long du processus de développement donne aux utilisateurs la possibilité de fournir des commentaires sur la conception avant la sortie du produit.

-   Conception itérative.

    Les grands problèmes masquent souvent des problèmes de petite taille. Les concepteurs et les développeurs doivent réviser la conception de manière itérative à travers des tests.

### <a name="why-should-i-involve-users"></a>Pourquoi dois-je impliquer des utilisateurs ?

Les développeurs doivent reconnaître qu’il ne s’agit pas d’utilisateurs classiques. Ils ont une connaissance plus approfondie et une compréhension du système qu’ils développent que la moyenne de l’utilisateur. Les aspects de l’interface qui ne sont pas clairs ou confus pour la plupart des utilisateurs peuvent donc être parfaitement clairs à une personne qui a travaillé sur le projet. Certains développeurs de logiciels sont en mesure de comprendre avec l’utilisateur moyen, mais il n’y a pas de substitut pour les véritables interactions des utilisateurs réels avec le produit.

En conséquence, en vous concentrant sur les besoins habituels des utilisateurs et en modifiant la conception en fonction des tests des utilisateurs souvent, les développeurs de logiciels orientés utilisateur produisent de meilleures conceptions et, par conséquent, de meilleurs produits.

Une meilleure conception offre une meilleure acceptation des utilisateurs. L’avantage avec les logiciels de vente au détail est évident : les ventes augmentent. L’acceptation est également importante dans le cas d’un logiciel développé pour une utilisation interne : l’augmentation de la conception centrée sur l’utilisateur implique une productivité accrue et un besoin réduit de support. L’implication visible des utilisateurs du début du développement montre également un intérêt pour leurs préoccupations et leurs besoins, ce qui augmente leur volonté de contribuer à l’effort de développement.

### <a name="cant-i-just-follow-guidelines"></a>Ne puis-je pas suivre les instructions ?

Microsoft a développé un ensemble d’instructions d’interface pour la plateforme informatique Windows pour s’assurer que les programmes Windows ont une apparence cohérente. D’autres entreprises ont développé des directives similaires pour d’autres plateformes informatiques, et les experts de la convivialité tels que Jakob Nielsen ont largement écrit sur la conception de pages Web utilisables. Avec la richesse des informations disponibles sur ces sujets, les concepteurs pensent parfois que le respect rigoureux des directives et des normes est tout ce qui est nécessaire pour produire des produits utilisables.

Le problème de cette approche est que les recommandations sont fondamentalement générales. Les directives doivent s’appliquer à une grande variété de cas et, par conséquent, ne pas toujours prescrire la meilleure marche à suivre pour l’application en cours de développement. L’adhésion à un ensemble bien écrit d’instructions peut vous aider dans la conception d’une interface cohérente, mais elle ne peut pas garantir son usablility, sauf si elle est testée avec des utilisateurs réels. Lorsque vous utilisez des instructions, ne les utilisez pas comme un livre de recettes dans lequel les instructions pointent vers le meilleur de tous les résultats. Deux développeurs peuvent implémenter la même règle de deux manières différentes, et les deux implémentations peuvent ne pas être tout aussi appropriées pour la situation. Parfois, une adhésion rigoureuse aux instructions peut entraîner des résultats médiocres ou des conflits entre les instructions. Seule la conception centrée sur l’utilisateur peut aider à vider ces problèmes avant qu’ils ne deviennent des problèmes.

Une autre façon de penser à cela est : laisser la conception centrée sur l’utilisateur être l’arbitre des décisions de conception, et non les instructions de l’interface utilisateur.

### <a name="do-i-need-to-build-a-usability-lab"></a>Ai-je besoin de créer un laboratoire d’utilisation ?

Ne partez pas du principe que le test d’utilisation signifie la validation d’un laboratoire coûteux, avec des caméras montées au plafond, des miroirs unidirectionnels et d’autres pièges de groupe de concentration. Pour vous assurer que les entreprises qui effectuent beaucoup de tests trouvent souvent pratique de créer des laboratoires dédiés, et que les consultants en convivialité disposent souvent d’un large éventail d’installations et d’équipements pour offrir leurs clients. Toutefois, il est utile de procéder à des tests d’utilisation valides dans divers paramètres et dans certains cas.

Une approche consiste simplement à avoir un testeur ? quelqu’un s’est engagé à effectuer des études de participants humains et à collecter des données ? assis derrière un utilisateur lorsqu’il travaille et observe l’utilisateur qui effectue des tâches. Cela peut être facilement effectué dans une salle de conférence ou un bureau. Pour plus d’informations sur les tests par observation, consultez l’entrée Dumas et revaisselle dans [autres ressources](other-resources.md).

À mesure que le test d’utilisabilité se développe et devient plus complexe, les équipements tels qu’une caméra vidéo, un miroir unidirectionnel ou des outils qui vous permettent d’afficher et d’enregistrer l’analyse d’un utilisateur en temps réel peuvent être ajoutés.

En guise d’alternative, les tests peuvent être externalisés auprès des consultants en utilisation. La section suivante contient des conseils sur la recherche des consultants appropriés.

### <a name="how-do-i-get-started"></a>Comment commencer ?

Une fois qu’il a été décidé d’incorporer des principes de conception centrés sur l’utilisateur dans le processus de développement, vous devez décider s’il faut embaucher des professionnels de la convivialité ou externaliser le test d’utilisabilité pour un fournisseur.

L’UPA (utilisabilité Professionals Association) dispose d’un guide de fournisseur qui peut aider à trouver des consultants en convivialité.

Certains groupes de Conseil peuvent également vous aider à configurer des laboratoires de convivialité ou à développer un programme d’utilisation interne pour incorporer des principes d’utilisation dans le processus de conception.

En cas d’embauche de professionnels de l’utilisation, les facteurs humains et la société ergonomiques disposent d’un service de placement qui peut aider à trouver des employés potentiels. De nombreux professionnels de l’utilisation appartiennent également au groupe d’intérêt spécial ACM sur Computer-Human interaction (SIGCHI) et UPA. Placez les publicités sur l’emploi dans leurs publications ou dans leurs conférences.

Quel que soit le routage utilisé, n’oubliez pas qu’il s’agit de services de test. Le principe que les concepteurs ne sont pas des utilisateurs classiques est également vrai pour les professionnels de la convivialité.

Pour plus d’informations sur ces sociétés et organisations, et pour en savoir plus sur les tests d’utilisation et la conception centrée sur l’utilisateur, consultez [autres ressources](other-resources.md).

 

 




