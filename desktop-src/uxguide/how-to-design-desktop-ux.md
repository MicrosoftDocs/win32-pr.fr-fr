---
title: Conception de l’expérience utilisateur pour les applications de bureau
description: Une application de bureau de grande qualité est puissante et, en même temps, simple. Grâce à la sélection et à la présentation des fonctionnalités soigneusement équilibrées, vous pouvez obtenir la puissance et la simplicité.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 74433514f61b37ba1c9941c8134767be5458ebc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295983"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Comment concevoir une expérience utilisateur idéale pour les applications de bureau

> [!NOTE]
> ce guide de conception a été créé pour Windows 7 et n’a pas été mis à jour pour les versions plus récentes de Windows. La plupart des conseils s’appliquent toujours en principe, mais la présentation et les exemples ne reflètent pas nos [recommandations en](/windows/uwp/design/)matière de conception.

Une application de bureau de grande qualité est puissante et, en même temps, simple. Grâce à la sélection et à la présentation des fonctionnalités soigneusement équilibrées, vous pouvez obtenir la puissance et la simplicité.

**Offrant**

![capture d’écran de la boîte de dialogue orthographe et grammaire ](images/powerful-simple-image1.png)

**Puissant et simple :**

![capture d’écran de la liste des révisions orthographiques possibles ](images/powerful-simple-image2.png)

l’application idéale basée sur le Windows est à la fois puissante et simple. Bien sûr, vous souhaitez que votre application soit puissante et, bien sûr, que vous souhaitiez la rendre simple, mais pouvez-vous y parvenir ? Il existe une tension naturelle entre ces objectifs, mais cette tension est loin d’être inconciliable. Vous pouvez obtenir la puissance et la simplicité grâce à une sélection et une présentation des fonctionnalités soigneusement équilibrées.

## <a name="what-makes-an-application-powerful"></a>Qu’est-ce qui rend une application puissante ?

Qu’est-ce que la « puissance » signifie vraiment en termes de logiciels ? Une application peut être considérée comme puissante s’il s’agit d’un bourrage-ensemble de fonctionnalités, avec un énorme éventail de fonctionnalités dans une tentative d’utilisation de tous les utilisateurs. Une telle conception n’a pas de chances de réussir, car un ensemble de fonctionnalités non ciblées est peu susceptible de répondre aux besoins de quiconque. Ce n’est pas le type d’alimentation que nous avons après.

Une application est puissante lorsqu’elle a la bonne combinaison de ces caractéristiques :

-   **Donnant.** L’application répond aux besoins de ses utilisateurs cibles, ce qui leur permet d’effectuer des tâches qu’ils n’auraient pas pu faire et d’atteindre leurs objectifs de manière efficace.
-   **Efficace.** L’application permet aux utilisateurs d’effectuer des tâches avec un niveau de productivité et de mise à l’échelle qui n’était pas possible auparavant.
-   **Interfaces.** L’application permet aux utilisateurs d’effectuer efficacement un large éventail de tâches dans diverses circonstances.
-   **Directe.** L’application s’apparente à aider les utilisateurs à atteindre leurs objectifs, au lieu de s’approcher ou de nécessiter des étapes inutiles. Les fonctionnalités telles que les raccourcis, l’accès au clavier et les macros améliorent le sens de l’adressage.
-   **Fixes.** L’application permet aux utilisateurs d’effectuer un contrôle affiné sur leur travail.
-   **Intégrer.** l’application est bien intégrée à Microsoft Windows, ce qui lui permet de partager des données avec d’autres applications.
-   **Avancé.** L’application possède des fonctionnalités de pointe exceptionnelles et novatrices qui ne se trouvent pas dans les solutions concurrentes.

Certaines de ces caractéristiques dépendent de la perception de l’utilisateur et sont relatives aux fonctionnalités actuelles des utilisateurs. Ce qui est considéré comme puissant peut changer au fil du temps. la fonctionnalité de recherche avancée d’aujourd’hui peut donc être très répandue demain.

Toutes ces caractéristiques peuvent être combinées dans notre définition de la puissance :

**Une application est puissante lorsqu’elle permet aux utilisateurs cibles de réaliser leur potentiel complet efficacement.**

Ainsi, la mesure ultime de la puissance est la productivité, et non le nombre de fonctionnalités.

Différents utilisateurs ont besoin d’aide pour atteindre leur potentiel complet de différentes façons. Ce qui est activé pour certains utilisateurs peut nuire à la polyvalence, à la direction et au contrôle pour d’autres. Les logiciels bien conçus doivent équilibrer ces caractéristiques de manière appropriée. Par exemple, un système de publication de bureau conçu pour les personnes qui ne sont pas des professionnels peut utiliser des assistants pour guider les utilisateurs dans des tâches complexes. Ces assistants permettent aux utilisateurs cibles d’effectuer des tâches qu’ils ne seraient normalement pas en mesure d’effectuer. En revanche, un système de publication de bureau destiné aux professionnels peut se concentrer sur la direction, l’efficacité et le contrôle complet. Pour les utilisateurs d’une telle application, les assistants peuvent être limités et frustrants.

**Si vous n’avez qu’une seule chose...**

Comprenez les objectifs de vos utilisateurs cibles et Élaborez un ensemble de fonctionnalités qui leur permet d’atteindre ces objectifs de manière productive.

## <a name="what-makes-a-user-experience-simple"></a>Qu’est-ce qui simplifie l’expérience utilisateur ?

Nous définissons la simplicité comme suit :

**La simplicité est la réduction ou l’élimination d’un attribut d’une conception qui cible les utilisateurs et qui sont considérés comme non essentiels.**

Dans la pratique, la simplicité est obtenue en sélectionnant le jeu de fonctionnalités approprié et en présentant les fonctionnalités de la bonne façon. Cela réduit le temps non essentiel, à la fois réel et perçu.

La simplicité dépend de la perception des utilisateurs. Réfléchissez à la façon dont l’effet d’une transmission automatique dépend du point de vue d’un utilisateur :

-   Pour le pilote classique (l’utilisateur cible), une transmission automatique élimine la nécessité d’une vitesse et d’un embrayage manuels, ce qui facilite grandement la mise en place d’une voiture. Une équipe et un embrayage manuels ne sont pas essentiels pour la tâche de pilotage. ils sont donc supprimés pour des raisons de simplicité.
-   Pour un pilote de voiture de course professionnel, il est essentiel de disposer d’un contrôle direct sur la transmission pour être compétitif. Une transmission automatique a une incidence négative sur les performances de la voiture. elle n’est donc pas considérée comme un résultat plus simple.
-   Pour un mécanicien, une transmission automatique est un mécanisme plus complexe qui, par conséquent, n’est pas plus facile à réparer ou à entretenir qu’une transmission manuelle. Contrairement au mécanicien, l’utilisateur cible ne connaît tranquillement pas cette complexité interne.

Bien que les différents utilisateurs considèrent la transmission automatique différemment, elle est réussie, car elle élimine la nécessité d’une connaissance, d’une compétence et d’un effort non essentiels de la part de ses utilisateurs cibles. Pour le pilote classique, la transmission automatique est une fonctionnalité intéressante, car elle fonctionne simplement.

### <a name="simplicity-vs-ease-of-use"></a>Simplicité et facilité d’utilisation

La simplicité, lorsqu’elle est appliquée correctement, entraîne une facilité d’utilisation. Mais la simplicité et la facilité d’utilisation ne sont pas les mêmes concepts. La facilité d’utilisation est obtenue lorsque les utilisateurs peuvent effectuer une tâche avec succès sans difficulté ou confusion dans un laps de temps approprié. Il existe de nombreuses façons d’obtenir une simplicité d’utilisation et la simplicité, la réduction de la valeur non essentielle, n’est qu’une seule d’entre elles.

Tous les utilisateurs, quel que soit leur niveau de complexité, veulent travailler avec un minimum d’efforts inutiles. Tous les utilisateurs, même les utilisateurs expérimentés, sont principalement motivés pour faire leur travail, et non pour en savoir plus sur les ordinateurs ou votre application.

La simplicité est la méthode la plus efficace pour faciliter l’utilisation et la simplicité d’utilisation. Les fonctionnalités complexes et difficiles à utiliser ne sont pas utilisées. En revanche, des conceptions simples et élégantes qui effectuent bien leur fonction sont un bonheur à utiliser. Ils appellent une réponse émotionnelle positive.

par exemple, considérez la prise en charge des réseaux sans fil dans Microsoft Windows XP. Microsoft aurait pu ajouter un Assistant pour guider les utilisateurs tout au long du processus de configuration. Cette approche aurait abouti à une facilité d’utilisation, mais pas plus simple, car une fonctionnalité non essentielle (l’Assistant) aurait été ajoutée. Au lieu de cela, Microsoft a conçu la mise en réseau sans fil pour se configurer automatiquement. En fin de compte, les utilisateurs ne se soucient pas des détails de configuration, tant qu’il « fonctionne » simplement de manière fiable et sécurisée. Cette combinaison de puissance et de simplicité dans la technologie de réseau sans fil a conduit à sa popularité et à son adoption rapide.

**Si vous n’avez qu’une seule chose...**

Démarrez votre processus de conception avec les conceptions les plus simples qui font le bon travail.

Si vous n’êtes pas satisfait de votre conception actuelle, commencez par supprimer tous les éléments non essentiels. Vous constaterez que ce qui reste est généralement très bon.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Obtention de la simplicité tout en maintenant la puissance

### <a name="design-principles"></a>Principes de conception

Pour obtenir une plus grande simplicité, il est toujours possible de concevoir le probable.

Le possible

Les décisions de conception basées sur ce qui est susceptible d’aboutir à des interfaces utilisateur complexes comme l’éditeur du Registre, dans lequel la conception suppose que toutes les actions sont tout aussi possibles et, par conséquent, nécessitent un effort identique. Étant donné que tout est possible, les objectifs de l’utilisateur ne sont pas pris en compte dans les décisions de conception.

Le probable

Décisions en matière de conception basées sur le résultat probable à des solutions simplifiées, ciblées et basées sur des tâches, où les scénarios potentiels reçoivent le focus et demandent un minimum d’effort à effectuer.

Le principe de conception de la simplicité

**Pour obtenir une plus grande simplicité, concentrez-vous sur ce qui est probable ; réduire, masquer ou supprimer ce qui est improbable ; et éliminent ce qui est impossible.**

Ce que les utilisateurs vont faire est bien plus adapté à la conception que ce qu’ils peuvent faire.

### <a name="design-techniques"></a>Techniques de conception

Pour obtenir une meilleure simplicité tout en maintenant la puissance, choisissez l' **ensemble de fonctionnalités approprié**, localisez les fonctionnalités **dans les bons emplacements** et **réduisez l’effort de les** utiliser. Cette section fournit des techniques courantes pour atteindre ces objectifs.

Choix de l’ensemble de fonctionnalités approprié

«La perfection est obtenue, pas quand il n’y a rien à ajouter,

mais lorsqu’il n’y a rien à retirer.» — Antoine de Saint-Exupery

Les techniques de conception suivantes offrent à vos utilisateurs les fonctionnalités dont ils ont besoin tout en atteignant la simplicité grâce à la réduction ou à la suppression effective :

-   **Déterminez les fonctionnalités dont vos utilisateurs ont besoin.** Comprenez les besoins de vos utilisateurs par le biais de l’analyse des objectifs, des scénarios et des tâches. Déterminez un ensemble de fonctionnalités qui réalisent ces objectifs.
-   **Supprimez les éléments inutiles.** Supprimer les éléments qui ne sont pas susceptibles d’être utilisés ou qui ont des alternatives préférables.
-   **Supprimez la redondance inutile.** Il peut y avoir plusieurs manières efficaces d’effectuer une tâche. Pour plus de simplicité, prenez la décision dure et choisissez celle qui convient le mieux à vos utilisateurs cibles au lieu de les fournir toutes et de choisir une option.
-   **Faites-le « simplement fonctionner » automatiquement.** L’élément est nécessaire, mais toute interaction de l’utilisateur pour le faire fonctionner n’est pas en raison d’un comportement ou d’une configuration par défaut acceptable. Pour plus de simplicité, faites en sorte qu’il fonctionne automatiquement et masquez-le entièrement à l’utilisateur ou réduisez considérablement son exposition.

Rationalisation de la présentation

«La possibilité de simplifier les moyens d’éliminer les

afin que le nécessaire puisse parler.» — Hans Hofmann

Utilisez les techniques de conception suivantes pour préserver la puissance, tout en respectant la perception de la réduction ou de la suppression :

-   **Combinez ce qui doit être combiné.** Placez les fonctionnalités essentielles qui prennent en charge une tâche afin qu’une tâche puisse être exécutée dans un seul emplacement. Les étapes de la tâche doivent avoir un fluide unifié et rationalisé. Décomposez les tâches complexes en un ensemble d’étapes faciles et claires, de sorte que l’emplacement « un » peut être constitué de plusieurs surfaces d’interface utilisateur, comme un Assistant.
-   **Séparez ce qui doit être séparé.** Toutes les opérations ne peuvent pas être présentées dans un même emplacement. par conséquent, vous devez toujours disposer de limites claires et bien choisies. Créez des fonctionnalités qui prennent en charge les scénarios centraux et évidents, et masquez les fonctionnalités facultatives ou créez des périphériques. Séparez les tâches individuelles et fournissez des liens vers les tâches associées. Par exemple, les tâches liées à la manipulation de photos doivent être clairement séparées des tâches liées à la gestion des regroupements de photos, mais elles doivent être facilement accessibles les unes par rapport aux autres.
-   **Éliminez ce qui peut être éliminé.** Procédez à l’impression de votre conception et mettez en évidence les éléments utilisés pour effectuer les tâches les plus importantes. Mettez même en surbrillance les mots dans le texte de l’interface utilisateur qui communiquent des informations utiles. Examinez maintenant ce qui n’est pas mis en surbrillance et envisagez de le supprimer de la conception. Si vous supprimez l’élément, tout se passe-t-il ? Si ce n’est pas le cas, supprimez !
-   La cohérence, la configurabilité et la généralisation sont souvent des qualités souhaitables, mais elles peuvent entraîner une complexité inutile. Passez en revue votre conception pour des efforts inappropriés de cohérence (tels que le texte redondant), la généralisation (par exemple, si deux fuseaux horaires sont suffisants) et la configurabilité (comme les options que les utilisateurs ne sont pas susceptibles de modifier) et éliminer les éléments qui peuvent être éliminés.
-   **Placez les éléments au bon endroit.** Dans une fenêtre, l’emplacement d’un élément doit suivre son utilitaire. Les contrôles, instructions et explications essentiels doivent tous être en contexte dans l’ordre logique. Si vous avez besoin de davantage d’options, exposez-les en cliquant sur un chevron ou un mécanisme similaire. Si des informations supplémentaires sont nécessaires, affichez une info-bulle au pointage de la souris. Placez des tâches, des options et des informations d’aide moins importantes en dehors du processus principal dans une fenêtre ou une page distincte. La technique consistant à afficher des détails supplémentaires en fonction des besoins est appelée Divulgation progressive.
-   **Utilisez des combinaisons significatives de haut niveau.** Il est souvent plus simple et plus évolutif de sélectionner et de manipuler des groupes d’éléments associés que des éléments individuels. Les dossiers, les thèmes, les styles et les groupes d’utilisateurs sont des exemples de combinaisons de haut niveau. Ces combinaisons sont souvent mappées à un objectif de l’utilisateur ou à une intention qui n’est pas visible à partir des éléments individuels. Par exemple, l’intention derrière le modèle de couleurs contraste élevé noir est beaucoup plus évidente que celle d’un arrière-plan de fenêtre noire.
-   **Sélectionnez les contrôles appropriés.** Les éléments de conception sont incorporés par les contrôles que vous utilisez pour les représenter. par conséquent, il est essentiel de sélectionner le bon contrôle pour une présentation efficace. par exemple, la zone de sélection de police utilisée par Microsoft Word affiche à la fois un aperçu de la police et les polices utilisées les plus récentes. De même, la façon dont Word affiche les erreurs potentielles d’orthographe et de grammaire en place est bien plus simple que la boîte de dialogue alternative, comme indiqué au début de cet article.

Réduction des efforts

«Les choses simples doivent être simples.

Les choses complexes doivent être possibles.» — Alan Kay

Les techniques de conception suivantes entraînent une réduction des efforts pour les utilisateurs :

-   **Rendre les tâches détectables et visibles.** Toutes les tâches, mais surtout les tâches fréquentes, doivent être facilement détectables dans l’interface utilisateur. Les étapes requises pour effectuer des tâches doivent être visibles et ne pas reposer sur la mémorisation.
-   **Présentez les tâches dans le domaine de l’utilisateur.** Un logiciel complexe oblige les utilisateurs à mapper leurs problèmes à la technologie. Le logiciel simple effectue cette mise en correspondance en présentant ce qui est naturel. Par exemple, une fonctionnalité de réduction des yeux rouges correspond directement à l’espace problématique et ne nécessite pas que les utilisateurs pensent en termes de détails tels que les teintes et les dégradés.
-   **Placez la connaissance du domaine dans le programme.** Les utilisateurs ne doivent pas être tenus d’accéder à des informations externes pour utiliser correctement votre application. La connaissance du domaine peut aller des données complexes et des algorithmes pour clarifier le type d’entrée valide.
-   **Utilisez du texte compréhensible par les utilisateurs.** Le texte bien conçu est essentiel pour une communication efficace avec les utilisateurs. Utilisez des concepts et des termes familiers à vos utilisateurs. Expliquez en détail ce qui est demandé en langage simple afin que les utilisateurs puissent prendre des décisions intelligentes et éclairées.
-   **Utilisez les valeurs par défaut probables sécurisées et sécurisées.** Si un paramètre a une valeur qui s’applique à la plupart des utilisateurs dans la plupart des cas, et que ce paramètre est à la fois sécurisé et sécurisé, utilisez-le comme valeur par défaut. Faites en sorte que les utilisateurs spécifient des valeurs uniquement lorsque cela est nécessaire.
-   **Utilisez des contraintes.** S’il existe de nombreuses façons d’effectuer une tâche, mais que seules certaines sont correctes, limitez la tâche à ces méthodes correctes. Les utilisateurs ne doivent pas être autorisés à effectuer des erreurs facilement pouvant être évitées.

### <a name="simplicity-does-not-mean-simplistic"></a>La simplicité ne veut pas dire simpliste

«Tout doit être aussi simple que possible,

mais pas plus simple». : Albert Einstein

Nous pensons que la simplicité est essentielle pour une expérience utilisateur efficace et souhaitable, mais il est toujours possible de prendre une bonne chose. L’essence de la simplicité est la réduction ou l’élimination des éléments non essentiels. La suppression du rôle essentiel produit simplement une mauvaise conception. En cas de « simplification », les utilisateurs se déconcertent, ne sont pas confiants ou ne parviennent pas à effectuer correctement les tâches, vous avez supprimé trop.

### <a name="simplicity-does-mean-more-effort-for-you"></a>La simplicité signifie plus de travail pour vous

«Je n’ai plus besoin de cette lettre, car j’ai

pas le temps nécessaire pour le rendre plus concis.» — Blaise Pascal

L’obtention de la simplicité tout en préservant la puissance nécessite souvent une complexité interne importante. Il est généralement plus facile de concevoir des logiciels qui exposent toutes les fonctions technologiques que de concevoir un logiciel qui le masque. ce dernier nécessite une bonne compréhension de vos utilisateurs cibles et de leurs objectifs. La suppression d’une fonctionnalité requiert une discipline, tout en décidant d’ajouter cette fonctionnalité intéressante qui n’est pas vraiment pratique. La simplicité nécessite des choix de conception réels au lieu de rendre tout ce qui est configurable. Les logiciels complexes résultent souvent d’une idée fausse des utilisateurs : ils ont une valeur inutilisée ou des fonctionnalités trop complexes qu’ils ne peuvent pas comprendre.

## <a name="powerful-and-simple"></a>Puissant et simple

La puissance consiste à activer vos utilisateurs et à les rendre productifs. La simplicité consiste à supprimer les fonctionnalités non essentielles et présentant la bonne façon. en comprenant vos utilisateurs cibles et en obtenant un juste équilibre entre les fonctionnalités et la présentation, vous pouvez concevoir des applications basées sur Windows qui effectuent les deux.

 

 