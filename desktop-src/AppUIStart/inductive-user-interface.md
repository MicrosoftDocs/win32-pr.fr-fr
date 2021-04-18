---
title: Interface utilisateur inductive
description: Cette rubrique décrit le modèle d’interface utilisateur appelé interface utilisateur inductif (IUI).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 632e16191b7103cbf6be9fe209ada78781d4a53c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190735"
---
# <a name="inductive-user-interface"></a>Interface utilisateur inductive

Cette rubrique décrit le modèle d’interface utilisateur appelé interface utilisateur inductif (IUI). Également appelé navigation inductive, le modèle IUI suggère comment rendre les applications logicielles plus simples en cassant les fonctionnalités dans des écrans ou des pages faciles à expliquer et à comprendre. Ce modèle IUI est évident dans différents projets Microsoft, tels que Microsoft Money 2000, les applets du panneau de configuration Windows, différents écrans et boîtes de dialogue dans Microsoft Visual Studio 2010 et les volets des tâches de Microsoft Office.

-   [Introduction](#introduction)
-   [IUI en action : résolution d’un problème de conception courant](#iui-in-action-solving-a-common-design-problem)
    -   [Le problème : le logiciel est difficile à utiliser](#the-problem-software-is-hard-to-use)
    -   [Interface utilisateur déduite](#deductive-user-interface)
    -   [Solution : interface utilisateur inductive](#a-solution-inductive-user-interface)
-   [Étapes de création d’une interface utilisateur inductive](#steps-for-creating-an-inductive-user-interface)
    -   [Étape 1 : Focus sur chaque page d’une tâche unique](#step-one-focus-each-page-on-a-single-task)
    -   [Étape 2 : état de la tâche](#step-two-state-the-task)
    -   [Étape 3 : rendre le contenu de la page adapté à la tâche](#step-three-make-the-pages-contents-suit-the-task)
    -   [Étape 4 : proposer des liens vers des tâches secondaires](#step-four-offer-links-to-secondary-tasks)
-   [Conseils supplémentaires](#additional-guidelines)
    -   [Utiliser des modèles d’écran cohérents](#use-consistent-screen-templates)
    -   [Rendez-vous évident comment exécuter la tâche avec les contrôles à l’écran](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Fournir un moyen simple d’effectuer une tâche et d’en démarrer une nouvelle](#provide-screens-for-starting-tasks)
    -   [Rendre l’étape de navigation suivante évidente](#make-the-next-navigational-step-obvious)
-   [Assistance de l’utilisateur](#user-assistance)
    -   [Assistance principale](#primary-assistance)
    -   [Assistance secondaire](#secondary-assistance)
-   [Annexe : conception et test de Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Conception et test de Money 2000](#designing-and-testing-money-2000)
    -   [Tests d’utilisation](#usability-tests)
    -   [Comparaison avec les sites Web](#comparison-with-web-sites)

## <a name="introduction"></a>Introduction

Le IUI est un modèle d’interface utilisateur qui suggère comment rendre les applications logicielles plus simples en cassant les fonctionnalités dans des écrans ou des pages faciles à expliquer et à comprendre. Microsoft a implémenté ce modèle dans Money 2000, une grande application commerciale. Les tests informels suggèrent que les utilisateurs peuvent effectuer des tâches aussi rapidement dans ce modèle que dans des interfaces traditionnelles, et trouver des choses plus facilement.

De nombreuses applications logicielles commerciales incluent des interfaces utilisateur dans lesquelles un écran présente un ensemble de contrôles, mais le laisse à l’utilisateur pour déduire l’objectif de la page et comment utiliser les contrôles pour atteindre cet objectif.

Les principes décrits dans ce document ne nécessitent pas ou n’impliquent pas d’ensembles de conceptions, de contrôles ou d’éléments visuels spécifiques. À l’instar des interfaces utilisateur graphiques, les principes énoncés dans ce document laissent beaucoup de place pour la flexibilité et la créativité en conception.

Les principes généraux de l’interface utilisateur inductive sont illustrés par des exemples tirés de Money 2000.

> [!IMPORTANT]
> Le concept général de IUI est dans son ensemble. Les concepteurs qui utilisent ces techniques sont d’apprendre et de découvrir plus en détail à mesure qu’ils l’utilisent pour leurs logiciels. Les informations contenues dans ce document évoluent au fil du temps, à mesure que les recherches et les connaissances dans ce domaine augmentent. Cette rubrique fournit une présentation de IUI, plutôt qu’un ensemble complet d’instructions.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI en action : résolution d’un problème de conception courant

Cette section traite d’un problème de conception courant avec les produits logiciels d’aujourd’hui et présente IUI comme une technique permettant de surmonter le problème.

### <a name="the-problem-software-is-hard-to-use"></a>Le problème : le logiciel est difficile à utiliser

La plupart des logiciels sont trop difficiles à utiliser. Cette conclusion est tirée des tests d’utilisabilité, des preuves anecdotique et des expériences personnelles des concepteurs de logiciels. Le concept de IUI a été créé en effectuant des recherches, en apportant des hypothèses à ce qui rend le logiciel actuel difficile à utiliser, puis en proposant des solutions. Les concepteurs qui utilisent IUI doivent s’appuyer sur la satisfaction des clients pour déterminer la réussite ultime de la conception.

La plupart des produits logiciels actuels sont difficiles à utiliser pour les raisons générales suivantes :

-   Les utilisateurs ne semblent pas construire un modèle mental adéquat du produit.

    La conception de l’interface pour la plupart des produits logiciels actuels suppose que les utilisateurs comprennent un modèle conceptuel soigneusement créé par les concepteurs. Malheureusement, la plupart des utilisateurs ne semblent jamais acquérir un modèle mental complet et suffisamment précis pour guider leur navigation. Ces utilisateurs sont probablement très occupés et surchargés avec des informations. Ils n’ont pas le temps, l’énergie ou le souhait d’étudier un modèle conceptuel pour leurs logiciels.

-   Même un grand nombre d’utilisateurs à long terme ne maîtrisent jamais les procédures courantes.

    Les concepteurs savent que les nouveaux utilisateurs peuvent rencontrer des problèmes au début, mais ils attendent que ces problèmes persistent quand les utilisateurs apprennent des tâches courantes. Les données d’utilisation indiquent que cela ne se produit pas souvent. Au cours d’une étude, les chercheurs configurent des équipements automatisés pour les utilisateurs de cassettes vidéo à leur bureau. Les bandes ont montré que les utilisateurs qui se concentrent sur la tâche en cours ne remarquent pas nécessairement la procédure qu’ils suivent et n’apprennent pas de l’expérience. La prochaine fois que les utilisateurs effectuent la même opération, ils peuvent tombés de la même façon.

-   Les utilisateurs doivent travailler dur pour déterminer chaque fonctionnalité ou écran.

    La plupart des produits logiciels sont conçus pour les utilisateurs qui comprennent son modèle conceptuel et qui ont des procédures communes. Pour la majorité des clients, chaque fonctionnalité ou procédure est un puzzle indésirable et frustrant. Les utilisateurs peuvent supposer que ces puzzles sont un coût inévitable de l’utilisation d’ordinateurs, mais ils seraient certainement plus heureux sans cette charge.

La meilleure solution à ces problèmes consiste à trouver une stratégie générale permettant de rendre les fonctionnalités des produits logiciels plus évidentes et explicites. Les utilisateurs doivent être en mesure de trouver une fonctionnalité à chaque fois qu’ils en ont besoin et doivent être en mesure d’utiliser cette fonctionnalité chaque fois qu’ils veulent l’utiliser.

### <a name="deductive-user-interface"></a>Interface utilisateur déduite

La plupart des éléments du logiciel aujourd’hui requièrent que l’utilisateur les étudie et déduit leur comportement, comme le montre la capture d’écran suivante.

![capture d’écran d’un exemple de boîte de dialogue Propriétés.](images/iuiguidelines01.png)

Les utilisateurs d’ordinateurs expérimentés, y compris les concepteurs de logiciels, reconnaissent rapidement que cette boîte de dialogue leur permet de gérer une liste de choses. Ils comprennent les boutons situés sous la liste pour ajouter, supprimer et fournir des informations sur les éléments de liste. Toutefois, Notez qu’aucun de ces comportements n’est explicitement indiqué dans la boîte de dialogue elle-même.

Examinons maintenant la boîte de dialogue du point de vue d’un utilisateur occasionnel. De nombreux utilisateurs, lorsqu’ils sont confrontés à cette boîte de dialogue, vous demandent « que suis-je supposé faire ? ». Quand la boîte de dialogue s’affiche, l’utilisateur doit arrêter et déterminer les étapes suivantes. Tout d’abord, l’utilisateur doit déduire le fait que le grand rectangle blanc est une zone de liste vide à remplir avec des éléments. La petite étiquette de texte de la zone, « Things », offre un Conseil vague. Certains utilisateurs essaient de taper dans la zone de liste, car il ressemble à une zone de texte de modification.

Ensuite, l’utilisateur doit déduire que les boutons situés sous la liste affectent son contenu. Certains boutons sont initialement désactivés, ce qui constitue une autre source potentielle de confusion utilisateur. L’utilisateur doit faire des essais avec les contrôles pour savoir comment fonctionne la boîte de dialogue.

L’utilisateur peut également poser d’autres questions : «combien d’éléments dois-je placer dans la liste ? Dois-je entrer des éléments dans un ordre spécifique ? Pourquoi ai-je obtenu cette boîte de dialogue en premier lieu ? Qu’est-ce que c’est ?»

Les utilisateurs sont gênés de leurs objectifs lorsqu’ils doivent déterminer l’objectif d’un écran et comment l’utiliser. Cela représente finalement un coût de la satisfaction des utilisateurs et du temps. Pire encore, les utilisateurs paient ce coût à chaque fois qu’ils font un puzzle sur l’interface chaque fois qu’ils utilisent une fonctionnalité.

Un écran doit avoir un titre qui explique clairement son rôle. Quand les concepteurs créent un écran, ils ont rarement besoin d’avoir un objectif clairement exprimable. Au lieu de cela, il peut simplement faire partie d’un modèle conceptuel plus grand que l’utilisateur doit déduire.

Les études montrent que de nombreux utilisateurs sont confondus même par des opérations de base dans les logiciels. Ils ont des difficultés à comprendre ce que le produit peut faire pour eux, à accéder pour effectuer une opération et à effectuer cette opération une fois qu’ils l’ont trouvé. La simplification des logiciels en apportant des modifications fondamentales est un moyen puissant de satisfaire pleinement les clients existants et d’attirer de nouveaux utilisateurs.

### <a name="a-solution-inductive-user-interface"></a>Solution : interface utilisateur inductive

Pour une nouvelle façon de concevoir des logiciels, l’objectif de IUI est de réduire la quantité de facteurs superflus que les utilisateurs doivent faire pour se déplacer entre les parties d’un produit et utiliser ses fonctionnalités. Le mot inductif provient de l’induite de verbe, ce qui signifie qu’il doit se poser ou se déplacer par influence ou persuasion.

IUI est une extension de l’interface de style Web courante. Dans l’environnement Web, les pages doivent être simples et basées sur des tâches, car chaque information doit être envoyée à un serveur via une connexion relativement lente. Le serveur répond ensuite avec l’étape suivante, et ainsi de suite. Une bonne conception Web consiste à se concentrer sur une seule tâche par page et à fournir une navigation sur les pages. De même, la navigation inductif commence par la mise en focus de l’activité sur chaque page vers une tâche principale unique.

Une interface inductif bien conçue aide les utilisateurs à répondre à deux questions fondamentales qu’ils rencontrent lorsqu’ils regardent un écran :

-   Que dois-je faire maintenant ?
-   Où puis-je aller d’ici pour accomplir ma tâche suivante ?

Le logiciel conçu conformément à ces principes répond à ces questions en commençant par un site fondamental : un écran avec un objectif explicite unique et clairement indiqué est plus facile à comprendre qu’une page sans objectif. Si l’écran est plus facile à comprendre, il sera plus facile pour l’utilisateur de savoir ce qu’il faut faire et où aller à l’étape suivante.

Ce principe fondamental peut être développé en une série de quatre étapes pour la conception de logiciels utilisant IUI :

-   Concentrez chaque écran sur une seule tâche.
-   État de la tâche.
-   Rendre le contenu de l’écran adapté à la tâche.
-   Propose des liens vers des tâches secondaires.

Bien que ce document décrit les principes généraux de IUI, il montre également ces principes en action en montrant des exemples de Money 2000 et d’autres logiciels. Vous devez considérer ces exemples comme des expressions spécifiques de IUI, et non un modèle strict pour l’implémentation.

En plus des quatre étapes mentionnées ci-dessus, vous pouvez renforcer votre interface en suivant les cinq instructions suivantes :

-   Utilisez des modèles d’écran cohérents.
-   Fournissez des écrans pour le démarrage des tâches.
-   Rendez-vous évident comment effectuer la tâche avec les contrôles à l’écran.
-   Fournir un moyen simple d’effectuer une tâche et d’en démarrer une nouvelle.
-   Rendez l’étape de navigation suivante évidente.

### <a name="processes"></a>Processus

De nombreuses tâches requièrent que les utilisateurs parcourent une série d’écrans. Un utilisateur qui effectue une tâche peut cliquer sur un lien vers une tâche secondaire qui quitte la séquence d’écrans qui composent la tâche principale. Lorsque l’utilisateur termine la tâche secondaire, il doit y avoir un moyen simple de renvoyer l’utilisateur directement au point de branche dans la tâche d’origine. Les utilisateurs sont susceptibles d’avoir des difficultés à utiliser des contrôles de navigation conventionnels tels que les boutons **précédent** et **suivant** pour revenir à l’emplacement où ils ont commencé.

Pour offrir cette possibilité, IUI définit un concept de navigation appelé processus, un écran ou une série d’écrans qui effectuent une tâche. Un processus agit comme une sorte de sous-routine de navigation. Les utilisateurs peuvent commencer un processus, travailler par le biais de sa série d’écrans, puis, dans la dernière page, cliquer sur un bouton « terminé » pour revenir rapidement à la page où ils ont commencé le processus.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Étapes de création d’une interface utilisateur inductive

Cette section décrit en détail les quatre étapes que vous pouvez utiliser pour créer un IUI.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Étape 1 : Focus sur chaque page d’une tâche unique

La première étape de la conception d’un IUI consiste à prendre une fonctionnalité ou un ensemble de fonctionnalités et à la décomposer en écrans distincts. Chaque écran doit se concentrer sur une seule tâche, appelée tâche principale de l’écran.

Cette idée semble simple, mais peu d’applications la suivent. La plupart des applications présentent un écran à partir duquel toutes les fonctionnalités associées sont accomplies. Cette conception oblige les utilisateurs à déterminer (déduire) ce qui peut être fait et comment procéder.

La tâche principale peut être spécifique ou ouverte. Par exemple, dans un programme de finance personnel, une tâche spécifique peut être « sélectionner la facture que vous souhaitez payer », tandis qu’une tâche ouverte peut être « passer en revue les performances de vos investissements ».

La tâche principale doit avoir un sens pour l’utilisateur, plutôt qu’une réflexion d’un détail d’implémentation ou d’un autre concept abstrait. La tâche doit être quelque chose que les utilisateurs peuvent envisager d’effectuer, de préférence décrits dans leurs propres mots.

### <a name="example"></a>Exemple

Cette section compare deux versions différentes de Money. Les exemples présentent des fonctionnalités très similaires qui permettent aux utilisateurs d’afficher et de gérer des comptes financiers.

Le modèle IUI a été développé lors de la création de Money 2000, une application de gestion des finances personnelles. Money 2000 est la huitième version majeure du produit. Money 2000 est un programme Windows de grande taille avec plus de 1 million lignes de code.

Money 2000 est une application de type Web. Il ne s’agit pas d’un site Web, mais partage de nombreux attributs avec les sites Web. Son interface utilisateur se compose de pages plein écran affichées dans un frame partagé, avec des outils de déplacement vers l’avant et vers l’arrière via une pile de navigation. Sur cette base, Money 2000 ajoute un ensemble de nouvelles conventions d’interface utilisateur qui créent une expérience utilisateur plus structurée.

Bien que IUI ait été utilisé pour la première fois dans la conception de style Web de Money 2000, il peut également être utilisé avec des éléments d’interface traditionnels, tels que des fenêtres et des boîtes de dialogue.

Dans Money 99, les utilisateurs effectuaient souvent un grand nombre de tâches sur un seul écran. Par exemple, la capture d’écran suivante montre le **Gestionnaire de comptes** qui a présenté toutes les fonctionnalités liées aux comptes dans Money 99 sur un seul écran.

![capture d’écran du gestionnaire de comptes dans Money 99.](images/iuiguidelines02.png)

Cet écran regroupe une tâche courante, en accédant à un compte, ainsi que des tâches peu fréquentes telles que la création et la suppression de comptes. Aucune de ces tâches n’est directement exprimée dans le titre de l’écran, le **Gestionnaire de comptes**. De nombreux utilisateurs peuvent trouver cet écran aussi difficile que l’exemple de boîte de dialogue de la figure 1. Dans les deux cas, l’utilisateur doit déduire l’objectif de l’écran et comment l’utiliser.

Money 2000, qui suit IUI, offre un ensemble quasiment identique de fonctionnalités liées aux comptes, mais les propose sur deux écrans distincts. La capture d’écran suivante montre le premier de ces écrans, qui se concentre entièrement sur la récupération d’un compte par l’utilisateur.

![capture d’écran de l’écran de sélection de compte dans Money 2000.](images/iuiguidelines03.png)

L’écran Money 2000 contient à peu près le même nombre d’éléments visuels que l’écran précédent de Money 99, mais la page est désormais entièrement axée sur la récupération de l’utilisateur pour choisir un compte. Par exemple, dans la version Money 99, un utilisateur devait faire deux clics pour ouvrir un compte : un pour le sélectionner, et un autre pour sélectionner l’opération d’ouverture. Dans la version Money 2000, la seule raison pour laquelle un utilisateur clique sur un compte est de l’ouvrir. un simple clic suffit. Ainsi, même si le nombre d’écrans peut augmenter, le nombre de clics nécessaires pour effectuer une tâche courante est souvent réduit.

Il peut arriver que les utilisateurs souhaitent ajouter ou supprimer un compte. Pour effectuer cette tâche dans Money 2000, les utilisateurs accèdent à un deuxième écran (illustré dans la capture d’écran suivante) qui se concentre sur la configuration des comptes.

![capture d’écran de l’écran de configuration de compte dans Money 2000.](images/iuiguidelines04.png)

L’objectif de chaque écran est plus clair dans la version IUI de Money 2000. En outre, chaque écran a plus d’espace à consacrer à son objectif. Par exemple, le gestionnaire de **comptes** Money 99 peut fournir très peu d’espace au bouton **supprimer le compte** , car il était rarement utilisé par rapport aux autres commandes à l’écran. En revanche, l’écran de configuration de compte dans Money 2000 peut mettre en évidence cette commande, ce qui la rend plus évidente et explicite.

### <a name="what-is-a-single-task"></a>Qu’est-ce qu’une seule tâche ?

Comment savoir si un écran est vraiment axé sur une seule tâche ? Un écran qui prend en charge de nombreuses tâches peut être expliqué comme n’ayant qu’un seul objectif si cet objectif est suffisamment abstrait. Voici une règle empirique : un écran est axé sur un objectif si le concepteur peut exprimer cet objectif avec un titre d’écran concis, explicite et naturel.

Les concepteurs de Money 2000 ont pris en compte la rupture de ces écrans (**Choisissez un compte à utiliser** et **configurez vos comptes dans Money**) sur d’autres écrans. Toutefois, étant donné que chaque écran a déjà un titre concis, explicite et naturel, les concepteurs ont supposé que les écrans étaient suffisamment axés. Lors de la conception d’un écran, si vous ne pouvez pas penser à un titre clair et simple, vous essayez probablement d’accomplir trop de choses sur l’écran.

### <a name="step-two-state-the-task"></a>Étape 2 : état de la tâche

Chaque écran doit être nommé avec une instruction concise et explicite de sa tâche principale. Il peut s’agir d’une instruction directe (« sélectionnez le compte que vous souhaitez équilibrer ») ou d’une question à laquelle l’utilisateur doit répondre (« quel compte voulez-vous équilibrer ? »).

Il s’agit d’un autre principe de simple bruit qui n’est souvent pas pratique. Par exemple, les versions antérieures de Money avaient des écrans avec des titres tels que le **Gestionnaire de services financiers en ligne** et un **compte de bilan**. Les utilisateurs devaient déduire l’objectif et le comportement de ces écrans à partir de la disposition et des étiquettes de leurs contrôles.

Le titre de l’écran ou de la page est très important. Que le produit utilise des fenêtres, des pages de style Web, des boîtes de dialogue ou une autre conception, le titre ne doit pas être autorisé à défiler.

### <a name="usable-screens-have-clear-titles"></a>Les écrans utilisables ont des titres clairs

Les écrans qui effectuent de nombreuses tâches requièrent des titres abstraits ou complexes. Par exemple, l’écran Money 99 illustré à la figure 2 permettait à l’utilisateur d’accéder aux comptes et de configurer des comptes. Le titre abstrait « gestionnaire de compte » a été donné à cette page pour tenter de capturer ces deux rôles. Bien que les utilisateurs puissent avoir des idées sur ce qu’une page « Gestionnaire de comptes » peut faire, ils peuvent ne pas se rendre compte que la tâche la plus courante pour cet écran a simplement choisi un compte.

Certains écrans ou commandes ont des objectifs abstraits qui ne suggèrent pas facilement des titres clairs. Pour ces écrans, les concepteurs peuvent choisir des noms qui sont délibérément imprécis, tels que « paramètres », des mots en monnaie, tels que « QuickStep » ou un jargon qui révèle les détails de l’implémentation (« compactage de base de données »). Ces types de noms sont souvent déroutants ou trompeurs pour les utilisateurs. En outre, ces noms sont généralement des noms qui n’expriment pas l’action que l’utilisateur souhaite accomplir, ce qui augmente la confusion.

Les titres d’écran et les autres noms sont souvent déterminés jusqu’à la fin du processus de conception. Les concepteurs demandent souvent aux rédacteurs de trouver un nom approprié pour un écran une fois qu’il a été conçu et codé. À ce stade, il n’y a pas de recours si un nom correct est introuvable et que l’équipe peut être obligée de régler les noms qui ne sont pas clairs. La solution à ce défaut est que les concepteurs considèrent la clarté des fonctions et des titres d’écran tôt dans le processus de conception.

Les fonctions et titres d’écran doivent se concentrer sur les tâches les plus courantes effectuées par les clients. Les concepteurs sont souvent tentés de fournir des fonctionnalités énormes pour tenter de satisfaire le plus grand nombre de clients, ainsi que les souhaits de l’équipe de conception proprement dite. Toutefois, les fonctionnalités supplémentaires ajoutent toujours de la complexité et d’autres coûts.

### <a name="screen-title-indicates-design-clarity"></a>Le titre de l’écran indique la clarté de la conception

Dans le modèle IUI, les concepteurs choisissent les titres d’écran dans les premières étapes du processus de conception. Au lieu de choisir un titre pour justifier le fonctionnement de l’écran, le titre est utilisé pour déterminer si l’écran est logique. Si aucun titre approprié n’est trouvé, la fonctionnalité est repensée. Si aucune conception ne permet un titre clair et concis (autrement dit, s’il n’existe aucun moyen d’expliquer la fonctionnalité), les concepteurs peuvent abandonner la fonctionnalité. Dans les captures d’écran suivantes, comparez l’écran de paiement de la facture Money 99 sur la gauche, qui fournit une étiquette statique pour la page (« Bill Bills & deposits ») et l’écran Money 2000 correspondant sur la droite, qui a un titre explicite (« cliquez sur la facture que vous souhaitez payer ») :

![capture d’écran qui montre un titre statique dans Money 99 et un titre actif dans Money 2000.](images/iuiguidelines05.png)

Un titre d’écran, qui est bien entendu une expression ou une phrase, est plus facile à modifier qu’une conception ou un code. En dépit de ce fait, l’expérience avec IUI a montré que le fait d’insister sur un titre d’écran clair produit de meilleures conceptions. Les titres doivent être choisis avec l’entrée des membres de l’équipe de formation des utilisateurs et de la convivialité, ainsi que des concepteurs de produits.

Les membres de l’équipe peuvent parfois tenter de reporter cette décision, en supposant que les clients partageront leur compréhension de l’objectif d’un écran. Quand il est nécessaire de fournir une déclaration claire et concise à cet effet, toutefois, les différences d’opinion sont souvent dévoilées. En résolvant ces différences et en sélectionnant un titre tôt, les discussions de conception peuvent se poursuivre de manière plus fluide.

Une fois qu’un titre est choisi, vous ne devez pas le considérer comme non modifiable. Les concepteurs affineront probablement des titres d’écran dans le temps, comme avec n’importe quelle conception. Toutefois, le premier titre choisi doit être aussi puissant que possible à ce niveau de développement.

### <a name="guidelines-for-choosing-screen-titles"></a>Instructions pour le choix des titres d’écran

Cette section décrit une technique simple pour choisir de bons titres d’écran. Pour utiliser cette technique, les concepteurs imaginent qu’un ami demande « qu’est-ce que cet écran ? » et une réponse claire et utile qui termine la phrase « c’est l’écran où vous ? ». Les mots qui terminent la phrase deviennent le titre de l’écran.

Pendant le développement de Money 2000, les rédacteurs de documentation de l’équipe ont créé des directives de titre d’écran pour garantir la qualité et la cohérence. Par exemple, ces instructions suggèrent des titres qui utilisaient des verbes et étaient formulées comme des questions ou des instructions directes. Les concepteurs évitent les noms statiques qui autorisent davantage d’abstraction et peuvent être imprécis.

Pour simplifier les titres, les concepteurs évitent les phrases composées et essaient d’utiliser le langage conversationnel, ce qui évite les termes difficiles et le jargon. Si les concepteurs ne peuvent pas décrire la tâche sans avoir recours à des conjonctions (« et », « ou »), l’écran tente probablement de faire plusieurs tâches et il est moins probable que l’utilisateur soit en mesure de comprendre immédiatement la marche à suivre.

Même lorsqu’un titre est soigneusement choisi, la zone de titre peut être trop petite pour expliquer correctement une tâche complexe. Pour résoudre ce problème, vous pouvez inclure un bref paragraphe descriptif en haut de la zone de contenu de l’écran qui s’articule autour de la tâche.

Le tableau suivant contient des exemples de titres d’écran dans Money 99 et des titres pour les mêmes écrans ou associés dans Money 2000.



| Titres d’écran dans Money 99             | Nouveaux titres d’écran dans Money 2000                         | Commentaire                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Gestionnaire de comptes**                   | **Choisir un compte** **configurer vos comptes**<br/> | Le titre statique a été modifié en titres actifs.          |
| **Détails du compte**                   | **Modifier la configuration du compte**                                | Le titre statique est passé à actif, titre spécifique. |
| **Calendrier des paiements**                  | **Payer une facture**                                          | Le titre vague a été descriptif.                   |
| **Gestionnaire des services financiers en ligne** |                                                         | Page non nécessaire après la reconception.                 |



 

### <a name="making-the-screen-title-prominent"></a>Rendre le titre d’écran visible

Une fois que vous avez réglé sur un titre d’écran utile, il est important de vérifier que l’attention de l’utilisateur est bien attirée dessus. Certaines études ont montré que les utilisateurs lisent rarement du texte d’instructions. Pour vous aider à surmonter ce problème, les titres d’écran doivent être conçus et attrayants pour attirer l’attention de l’utilisateur. La conception visuelle de l’écran doit informer l’utilisateur que le titre est l’élément le plus important à lire.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Étape 3 : rendre le contenu de la page adapté à la tâche

Lors de la création de logiciels qui suivent les instructions de IUI, le travail de conception le plus difficile consiste généralement à casser les fonctionnalités dans des écrans ou des pages. L’étape suivante consiste à déterminer les contrôles qui seront utilisés sur chaque écran pour accomplir sa tâche principale. Ces contrôles composent le contenu de la page, où l’utilisateur a terminé le travail. Le titre et le contenu de l’écran sont deux moitiés d’un dialogue entre le programme et l’utilisateur. Le titre pose la question du programme ou donne une instruction, et l’utilisateur répond par le biais de l’interface de l’écran.

Si le titre de l’écran est clair et simple, la conception de l’écran est généralement simple. Par exemple, l’un des écrans de l’argent 2000 présenté précédemment est intitulé « choisir un compte à utiliser ». Étant donné ce titre, l’écran doit évidemment contenir une liste simple de comptes parmi lesquels l’utilisateur peut choisir. Un autre écran Money 2000 a le titre « cochez les éléments à inclure dans vos taxes ». Naturellement, cet écran contient une liste de contrôle des éléments.

Les utilisateurs doivent être en mesure de déterminer facilement comment utiliser les contrôles pour obtenir la tâche principale de l’écran. Lorsque les utilisateurs sont invités à sélectionner un compte, et qu’ils peuvent rechercher une liste de comptes, ils confirment leur compréhension de la tâche. Cela augmente le risque de réussite des utilisateurs, ce qui augmente également leur confiance dans l’exécution d’autres tâches.

### <a name="screen-content-areas"></a>Zones de contenu d’écran

L’emplacement et la forme exacts des zones de contenu de l’écran dépendent de la conception du logiciel. Dans Money 2000, la zone de contenu de l’écran correspond à tout ce qui se trouve sous le titre de l’écran et à droite de la liste des tâches. Cette région peut faire défiler les écrans longs. Certains contenus non essentiels peuvent également apparaître dans la zone État sous la liste des tâches.

Les concepteurs peuvent choisir de développer la tâche principale de l’écran dans un paragraphe situé en haut de la zone de contenu. Les utilisateurs ne sont jamais tenus de lire ce texte, mais ils peuvent être utiles. De nombreux utilisateurs peuvent l’ignorer et continuer à utiliser correctement l’écran. Contrairement au titre, cette description peut faire défiler le curseur si l’écran est défilant. Pour plus d’informations, consultez [instructions pour le choix des titres d’écran](#guidelines-for-choosing-screen-titles).

Si les concepteurs veulent qu’une page affiche des rappels non essentiels, des alertes ou d’autres informations d’État, elles peuvent être affichées à gauche de la zone de contenu principale, sous la liste des tâches sur le côté gauche de l’écran. D’un point de vue fonctionnel, cette zone d’État est une région supplémentaire pour le contenu de l’écran. Cette zone n’est pas suffisamment visible pour contenir des contrôles essentiels.

### <a name="provide-a-clear-exit-from-the-page"></a>Fournir une sortie en clair à partir de la page

Après avoir terminé une tâche, l’utilisateur est confronté à un autre problème : quand et comment sortir de l’écran. Pour les écrans dont la tâche principale est la navigation, l’exécution de la tâche elle-même déplace l’utilisateur vers l’écran suivant. Sur d’autres écrans, il peut être plus difficile pour l’utilisateur de savoir comment procéder. Par exemple, sur un écran qui demande à l’utilisateur de taper des informations dans les champs, l’utilisateur peut avoir besoin d’aide pour déterminer quand et comment se déplacer. Sur ces pages, il est souvent utile d’offrir un bouton effacer **suivant** ou **terminé** dans un emplacement cohérent.

Les études de convivialité ont montré que les utilisateurs préfèrent utiliser des boutons, même lorsque **des boutons de** navigation globaux, tels que les boutons **précédent** ou principal d’une barre d’outils, sont disponibles. Les utilisateurs ne sont souvent pas à l’aise avec les écrans sans quitter la sortie, même les écrans dont l’objectif est de fournir des informations à lire.

Pour plus d’informations sur ce sujet, consultez [fournir une méthode simple pour effectuer une tâche et en démarrer une nouvelle](#provide-screens-for-starting-tasks) dans la section instructions supplémentaires.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Étape 4 : proposer des liens vers des tâches secondaires

La dernière étape de la conception d’un écran consiste à fournir des liens vers des tâches secondaires, qui sont des fonctionnalités qui n’accomplissent pas directement la tâche principale, mais qui sont liées à l’écran. Par exemple, si la tâche principale sur un écran consiste à écrire une lettre, les tâches secondaires sur cet écran peuvent consister à rechercher une adresse postale ou à imprimer une enveloppe.

Les tâches secondaires peuvent afficher des boîtes de dialogue, modifier la présentation visuelle du contenu de l’écran ou accéder à un autre écran de l’utilisateur. Une tâche secondaire peut accomplir indirectement la tâche principale ou peut rediriger les utilisateurs perdus à l’endroit où ils recherchent.

Si une page est une conversation entre l’ordinateur et l’utilisateur, une tâche secondaire permet à l’utilisateur d’ignorer la question présente de l’ordinateur et de demander à l’ordinateur de faire autre chose à la place. Par exemple, Imaginez cette boîte de dialogue : ordinateur : « quelle facture voulez-vous payer ? ». Utilisateur : « en fait, ce que je veux faire, c’est de trouver une facture que j’ai payée en arrière ».

Certains écrans de votre produit n’ont pas de tâches secondaires, tandis que d’autres en ont plusieurs. Vous devez éviter de créer une longue liste de tâches qui seront probablement difficiles à analyser par l’utilisateur. Si un écran présente une liste relativement longue de tâches secondaires, les tâches les plus courantes doivent être placées en premier, regroupées dans une section distincte ou mises en évidence visuellement.

La liste ne doit pas inclure toutes les tâches secondaires concevables tant qu’elles rendent l’étape de navigation suivante évidente. Au lieu d’offrir de nombreuses tâches secondaires, un écran peut fournir des tâches secondaires qui naviguent vers des pages auxiliaires qui répertorient plus de tâches.

### <a name="visual-design-of-secondary-tasks"></a>Conception visuelle des tâches secondaires

Les tâches secondaires doivent être répertoriées dans une position subordonnée à l’écran, où elles sont accessibles, si nécessaire, mais ne gênent pas l’utilisateur de la tâche principale. Le placement de cette liste dans une position cohérente sur chaque écran aide les utilisateurs à trouver rapidement la liste lorsqu’ils en ont besoin.

Si vous affichez la liste des tâches secondaires sur le côté gauche de l’écran, vous ne devez pas faire défiler la liste elle-même, ni faire défiler avec la page, comme illustré dans la capture d’écran suivante de l’écran de paiement de la **facture** de Money 2000.

![capture d’écran de l’écran de paiement de la facture dans Money 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Conseils supplémentaires

Cette section décrit cinq instructions utiles pour créer un IUI en suivant les quatre étapes décrites dans la section précédente.

### <a name="use-consistent-screen-templates"></a>Utiliser des modèles d’écran cohérents

Lors de la conception de logiciels qui suivent le modèle IUI, vous devez créer un modèle à utiliser comme guide pour chaque écran. Le modèle inductif ne dicte pas que vous utilisez un modèle particulier. Il existe de nombreuses variantes possibles qui peuvent satisfaire une conception inductive. Votre produit n’a besoin que d’un seul modèle pour tous ses écrans, ou vous pouvez créer plusieurs modèles différents à des fins différentes.

Un modèle approprié permet à un nouvel utilisateur de comprendre rapidement comment les écrans du produit fonctionnent. L’utilisation cohérente du modèle dans les écrans du produit fournit un bon fonctionnement de l’interface utilisateur de l’écran à l’écran. À mesure que les utilisateurs apprennent à s’attendre à ce que les mêmes éléments apparaissent dans les mêmes emplacements, ils peuvent analyser et commencer à utiliser chaque nouvel écran plus rapidement.

### <a name="provide-screens-for-starting-tasks"></a>Fournir des écrans pour le démarrage des tâches

Les produits conçus avec IUI utilisent souvent des écrans spéciaux conçus pour démarrer les utilisateurs sur des ensembles de tâches. Ces écrans sont appelés pages d’activité, car ils organisent les groupes associés de tâches courantes. Les pages d’activité fournissent un point de départ pour les utilisateurs. Une page d’activité présente généralement des liens vers d’autres pages où l’utilisateur a réellement effectué le travail. Les pages de l’activité demandent à l’utilisateur « que voulez-vous faire maintenant ? » et présentent une liste de réponses possibles. Les pages d’activité peuvent suivre un modèle spécial pour aider les utilisateurs à les reconnaître.

Une page d’activité crée une bonne page de démarrage par défaut pour un produit. Lorsque les utilisateurs démarrent une application, ils ont généralement une idée de la tâche qu’ils souhaitent accomplir. En règle générale, la raison du démarrage du produit est l’un des petits nombres de tâches très courantes. La page de démarrage par défaut du produit reconnaît cela en faisant savoir comment commencer des tâches courantes.

La page d' **hébergement** de Money 2000 est un exemple de page d’activité. Par défaut, les utilisateurs voient cet écran, où l’accès aux tâches financières courantes, telles que le paiement d’une facture et l’équilibrage d’un compte, s’affiche lorsque l’application démarre.

La capture d’écran suivante montre la page d' **Accueil** de Money 2000.

![capture d’écran de la page d’accueil de Money 2000. Page d’activité qui répertorie quelques tâches courantes et fournit des liens vers des ensembles de tâches sur d’autres pages.](images/iuiguidelines08.png)

Dans la mesure où Money fournit de nombreuses fonctionnalités financières, seules les tâches financières les plus courantes s’inscrivent sur la page d' **hébergement** . Pour toutes les autres tâches, la page d' **hébergement** est un lien vers un ensemble de pages d’activité de filiale nommé centres financiers. Chaque zone principale de Money fournit un centre financier. Ces écrans présentent le niveau de tâche suivant, qui sert de point de départ pour toutes les fonctionnalités dans chaque zone.

Par exemple, la zone **taxes** financières contient les fonctionnalités liées aux taxes du produit. La zone **taxes** propose des liens vers ces fonctionnalités sur une page du **Centre fiscal** , comme illustré dans la capture d’écran suivante.

![capture d’écran de la page de l’espace fiscal Money 2000. ](images/iuiguidelines09.png)

Une page d’activité peut également être beaucoup plus simple si moins d’options sont disponibles. La capture d’écran suivante montre comment une page d’activité peut être utilisée pour la gestion des comptes d’utilisateur Windows.

![capture d’écran d’une page d’activité Money 2000 pour la gestion des comptes d’utilisateur Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Rendez-vous évident comment exécuter la tâche avec les contrôles à l’écran

La meilleure façon de suivre cette règle consiste à choisir un titre d’écran approprié et à limiter l’étendue des tâches principales uniquement aux tâches les plus courantes. Une fois que vous êtes parvenu à un titre et à un objectif clairs pour la page, le choix de la bonne série de contrôles sera simple.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Fournir un moyen simple d’effectuer une tâche et d’en démarrer une nouvelle

Le dernier obstacle qu’un utilisateur rencontre sur un écran est le moment et le mode de départ. L’utilisateur quitte généralement l’écran en cliquant sur un lien ou en exécutant une commande qui navigue vers un autre écran. Ces liens peuvent s’afficher dans la zone de contenu de l’écran, dans la liste des tâches ou dans les barres d’outils de navigation. Les utilisateurs peuvent également quitter un écran en fermant le fichier en cours ou l’application elle-même.

La tâche sur certains écrans consiste à préparer une opération que l’utilisateur doit confirmer ou annuler. Ces écrans offrent généralement un lien qui effectue et valide l’opération, ainsi qu’un autre lien qui annule. Si l’utilisateur ignore ces options et clique sur un autre lien, le programme doit effectuer l’option moins destructrice. Les écrans doivent indiquer ce qui se produit si l’utilisateur prend ce chemin. Vous pouvez utiliser les liens pour rendre cette expression plus évidente. Par exemple, un bouton de validation intitulé « enregistrer les modifications » implique que les modifications apportées à l’écran ne prennent pas effet tant que vous n’avez pas cliqué sur ce bouton.

Même si les utilisateurs peuvent quitter chaque fois qu’ils le souhaitent, vous pouvez toujours proposer un lien qui suggère une sortie évidente de la page. Il en va de même pour les pages qui affichent simplement des informations statiques. Pour plus d’informations sur ce sujet, consultez la section [fournir une sortie en clair à partir de la page](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Démarrage et finalisation des processus

Dans le cadre de cet article, les processus sont des techniques permettant de gérer les tâches qui permettent à l’utilisateur d’utiliser plusieurs écrans.

Supposons qu’un utilisateur clique sur un lien dans la liste de contenu ou de tâche d’un écran et qu’il est dirigé vers un autre écran. Cette page peut, à son tour, être la première d’une série d’écrans qui effectuent un résultat global. À la fin de cette série d’écrans, l’utilisateur souhaite revenir à l’écran qui a précédé le processus. L’utilisateur peut retourner au moins deux façons ? vous pouvez cliquer sur le bouton précédent de manière répétée ou revenir à la page d’hébergement et y accéder ? mais aucune de ces méthodes n’est évidente ou naturelle. La plupart des utilisateurs s’attendent à trouver un bouton sur l’écran final qui les renvoie directement à l’écran d’origine.

Le modèle IUI prend en charge ce scénario par le biais du concept de processus, d’un écran ou d’une série d’écrans traités comme une unité de navigation. Les utilisateurs peuvent entrer le processus, travailler dans ses écrans et, dans le dernier écran, trouver un bouton qui les renvoie à l’emplacement où ils ont démarré. Plus important encore, l’utilisateur peut lancer le processus à partir de plusieurs emplacements dans le produit. Les utilisateurs sont toujours retournés à l’endroit où ils se trouvaient au moment où ils ont commencé le processus.

### <a name="process-name"></a>Nom du processus

Un nom doit être attribué à chaque processus et le nom doit apparaître quelque part sur chaque écran du processus. Money 2000 utilise cette approche. Chaque écran qui fait partie d’un processus global comprend le nom de ce processus en haut. Ce nom de processus s’affiche moins clairement que le titre unique de l’écran, car il est moins important. Le nom du processus rappelle aux utilisateurs le processus qu’ils mènent et renforce la notion selon laquelle tous les écrans du processus font partie d’une seule fonctionnalité. Par exemple, la zone **taxes financières** comprend un processus d' **estimateur fiscal** qui couvre plusieurs écrans. Chaque écran de ce processus affiche à la fois le nom du processus collectif et son titre d’écran unique.

### <a name="implementation-of-processes"></a>Implémentation des processus

Le même processus peut être lancé à partir de différents liens sur différents écrans, et les utilisateurs sont toujours retournés à la page de démarrage appropriée. Ce comportement ne peut pas être obtenu via un lien codé en dur sur l’écran final du processus, car la destination du lien varie. Au lieu de cela, l’application peut implémenter ce comportement en conservant une pile de processus actifs, indépendamment de la pile de navigation normale utilisée par les commandes **Back** et **Forward** . Lorsque l’utilisateur lance un processus, l’écran de lancement fait l’objet d’un push dans la pile de processus. Quand l’utilisateur clique sur le bouton **terminé** sur l’écran final du processus, l’application dépile l’écran de lancement le plus récent de la pile et renvoie l’utilisateur à cet écran.

Quand les utilisateurs quittent un écran dans un processus, le processus reste actif sur la pile de processus. Les utilisateurs peuvent effectuer le processus de sauvegarde à l’écran où ils l’ont laissé, puis continuer. Cela permet aux utilisateurs d’effectuer un détournement, de sauvegarder, puis de poursuivre avec le processus. Pour voir comment ce comportement fonctionne, commencez tout processus d’achat en ligne sur le World Wide Web, laissez le site, puis appuyez sur le bouton **précédent** . Vous serez en général en mesure de reprendre là où vous vous étiez arrêté.

### <a name="done-button"></a>Bouton Terminé

Pour terminer un écran et passer à l’écran suivant du processus, les écrans peuvent afficher un bouton près du bas de la page. L’étiquette de ce bouton est « Next », « done » ou un nom similaire. Si le bouton met fin au processus et que le processus peut être appelé à partir de plusieurs emplacements, la légende du bouton **terminé** peut inclure le nom de l’emplacement appelant.

### <a name="navigation-bar"></a>Barre de navigation

Sur n’importe quel écran, les utilisateurs peuvent décider qu’ils ont terminé la zone actuelle du produit et veulent démarrer autre chose. Il se peut qu’il ne souhaite pas terminer explicitement l’écran actuel avant de passer à une autre partie du produit. Une barre d’outils de navigation peut offrir à l’utilisateur un ensemble de liens pour démarrer de nouvelles tâches. Comme pour les autres listes de liens de tâches, celles-ci doivent suivre le principe de la prochaine étape de navigation évidente, décrite en détail dans la section suivante.

### <a name="make-the-next-navigational-step-obvious"></a>Rendre l’étape de navigation suivante évidente

Peu de programmes peuvent rendre toutes leurs fonctionnalités disponibles en même temps. Les utilisateurs doivent généralement parcourir un programme pour trouver une fonctionnalité particulière. Les utilisateurs sont plus réussis à la navigation s’ils peuvent facilement voir comment obtenir au moins une étape plus proche du résultat souhaité. Les écrans qui utilisent IUI sont conçus avec ce principe à l’esprit.

Par exemple, les pages d’activité n’affichent pas nécessairement chaque tâche ou destination concevable que l’utilisateur peut vouloir atteindre à partir de ce point. Au lieu de cela, les pages d’activité fournissent une liste de tâches suffisamment complètes pour que les utilisateurs puissent facilement déterminer le lien approprié à cliquer, même s’il les amène à une autre page de liens. Les tâches les plus fréquentes doivent être les plus importantes et nécessiter le moins de navigation possible. Les tâches moins fréquentes peuvent nécessiter des étapes supplémentaires.

Voici un exemple de Money 2000. Supposons que les utilisateurs souhaitent effectuer une opération qu’ils effectuent occasionnellement, par exemple en vérifiant le montant estimé du paiement de l’impôt sur les revenus de l’année suivante. Les utilisateurs commencent par rechercher cette fonctionnalité sur la page d’hébergement de Money 2000. Étant donné que la fonctionnalité n’apparaît pas dans la liste des tâches courantes, elle doit analyser la liste des zones financières. La zone **taxes** semble prometteur et clique dessus. La page **Centre d’imposition** contient un lien vers la fonctionnalité d’estimation fiscale qu’elle recherche, afin qu’elle clique dessus et termine sa tâche. En appliquant des principes IUI, Money 2000 permet aux utilisateurs de trouver intuitivement ce qu’ils cherchent.

## <a name="user-assistance"></a>Assistance de l’utilisateur

Cette section décrit un ensemble d’instructions suggérées pour l’intégration du texte d’assistance utilisateur dans un produit qui utilise IUI.

L’assistance principale fait référence à tout le texte visible sur l’écran (comme illustré dans la capture d’écran suivante). L’assistance principale fournit des indices textuels orientés vers les tâches qui permettent aux utilisateurs de comprendre facilement toutes les informations présentées à l’écran. Ils comprennent l’objectif de la page et la façon dont les objets sont liés les uns aux autres pour faciliter les tâches. Étant donné que le texte est directement sur l’écran, les informations qui répondent à des questions de premier peu comme « que dois-je faire ? » est facile d’accès et très visible sans que l’utilisateur n’ait à entreprendre aucune action.

![capture d’écran de l’écran de configuration de compte de Money 2000.](images/iuiguidelines11.png)

L’assistance secondaire est constituée de tout le texte qui n’est pas visible à l’écran, et nécessite une interaction de l’utilisateur pour accéder, par exemple en cliquant ou en pointant sur un élément de l’interface utilisateur. Ce contenu n’est pas essentiel pour accomplir la tâche en cours, mais il est toujours lié directement.

### <a name="primary-assistance"></a>Assistance principale

L’assistance principale peut inclure tout ou partie des composants suivants :

-   Titre de l’écran

    Exemple : modifier votre image

    Le titre de l’écran est le premier et le plus important élément qui s’affiche à l’écran. Son objectif est de décrire dans la langue de l’utilisateur la tâche qui peut être effectuée sur cette page. Le titre de l’écran doit éviter de décrire les détails de l’exécution de la tâche. Le texte dans le titre de l’écran doit faire référence uniquement à la tâche principale de l’écran. En règle générale, la description de la tâche, plus simple et plus rapide, est probablement la plus efficace. Pour plus d’informations sur cette rubrique, consultez étape 2 : état de [la tâche](#step-two-state-the-task).

-   Sous-titre d’écran

    Exemple : vous pouvez également télécharger une nouvelle image à partir d’Internet.

    Même avec un effort attentif, le titre de l’écran peut ne pas être suffisant pour expliquer correctement une tâche complexe. Le sous-titre vous permet de développer l’objectif de l’écran. Vous pouvez utiliser un sous-titre pour clarifier l’objectif de la page, fournir une description de tâche supplémentaire ou définir des attentes. Les utilisateurs qui ne lisent pas le sous-titre doivent pouvoir utiliser la page avec succès. Tout comme le titre, le sous-titre doit éviter de décrire les détails de l’exécution de la tâche.

-   Tâches

    Exemple : modifier l’économiseur d’écran

    Les tâches peuvent être présentées sous forme de liens textuels ou d’images graphiques nécessitant une interaction avec l’utilisateur. Les commandes présentées sous forme de liens de texte doivent être basées sur des verbes et écrites comme des tâches claires et concises.

-   Étiquettes pour les boutons de commande

    Exemple : créer un mot de passe

    Il existe trois types de boutons de commande :

    -   Annuler
    -   Terminé
    -   Commit

    Les boutons Annuler et terminé utilisent simplement « annuler » et « terminé » comme étiquettes. Les boutons de validation doivent utiliser des étiquettes de texte actives au lieu de « OK ». Par exemple, utilisez « créer un mot de passe » au lieu de « OK ».

-   Étiquettes pour d’autres contrôles

    Exemple : tapez votre mot de passe

    Les étiquettes pour les contrôles tels que les cases d’option, les cases à cocher et les zones de texte doivent être écrites de façon claire et concise afin que les utilisateurs sachent exactement ce que sont les contrôles, ceux à utiliser et les informations à fournir pour accomplir leur tâche.

-   Liens « tâches associées »

    Exemple : tâches associées-modifier un autre compte

    Les liens « tâches associées » sont des points d’entrée explicites pour d’autres tâches liées à la fonctionnalité actuelle. Ils doivent être écrits en tant que liens basés sur des tâches.

-   Liens « Voir aussi »

    Exemple : voir aussi-modifier votre thème

    Les liens « Voir aussi » sont des tâches secondaires. Celles-ci sont associées à la tâche principale, mais vont détenir l’utilisateur du contexte actuel. Ils doivent apparaître comme des liens de tâches ordinaires. Pour plus d’informations sur les tâches secondaires, consultez [conception visuelle des tâches secondaires](#visual-design-of-secondary-tasks).

### <a name="secondary-assistance"></a>Assistance secondaire

L’assistance secondaire peut inclure tout ou partie des composants suivants :

-   Info-bulles

    Vous pouvez utiliser une info-bulle pour fournir à l’utilisateur des informations supplémentaires sur un lien de tâche ou un bouton de commande. Par exemple, une info-bulle sur un lien de tâche peut lire « affiche une page dans laquelle vous pouvez choisir une image à utiliser avec votre compte ». L’info-bulle s’affiche lorsque l’utilisateur pointe la souris sur l’objet associé. Vous devez créer des info-bulles pour tous les éléments d’interface utilisateur sur lesquels l’utilisateur peut cliquer.

-   Rubriques d’aide « en savoir plus »

    Exemple : en savoir plus sur le téléchargement d’un fichier

    Les liens « en savoir plus » ouvrent des rubriques d’aide telles que des présentations de fonctionnalités, des informations conceptuelles, des informations de prise en charge et des informations procédurales. Pour réduire l’encombrement, vous devez réduire le nombre de rubriques d’aide « en savoir plus sur » sur l’écran.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Annexe : conception et test de Microsoft Money 2000

Cette section a été adaptée à partir des descriptions de la première partie des concepteurs. Il explique comment l’équipe Money 2000 a modifié le processus de conception et de test pour prendre en charge le modèle IUI.

### <a name="designing-and-testing-money-2000"></a>Conception et test de Money 2000

La conception de Money 2000 à l’aide du modèle de navigation inductif conduit l’équipe à des conceptions de questions qui se trouvaient dans le produit depuis longtemps. Étant donné que les principes du modèle sont simples, il était facile d’adopter le modèle dans le processus de conception et de le conserver. Au final, les concepteurs pensent que le modèle leur a aidé à améliorer les conceptions.

### <a name="clearer-titles-and-designs"></a>Ouvrages et conceptions plus clairs

Les concepteurs de Money 2000 ont remarqué qu’ils décrivaient souvent des fonctionnalités utilisant des mots qui n’étaient pas affichés à l’écran. Dans le modèle IUI, les écrans doivent s’expliquer eux-mêmes. Par exemple, l’équipe a expliqué que l’écran intitulé **Payment Calendar** était destiné au paiement des factures. Dans Money 2000, cet écran est appelé **paiement de factures**. Tous les éléments qui ne sont pas associés à cette fonction ont été déplacés vers les écrans des filiales, ce qui a entraîné une conception plus claire.

Un autre exemple implique un écran appelé **Online Financial Services Manager**. L’équipe s’est efforcée de trouver une explication simple de l’objectif de cet écran. Lorsqu’ils n’ont pas pu arriver à un, ils ont supprimé cet écran et distribué leurs fonctionnalités sur des pages plus logiquement définies.

### <a name="helping-new-designers"></a>Aider les nouveaux concepteurs

L’équipe a découvert qu’il est facile d’enseigner les techniques de conception IUI aux concepteurs de logiciels nouveaux et inexpérimentés. Les techniques permettaient aux concepteurs de tous les niveaux d’expérience d’évaluer leurs conceptions en utilisant des titres d’écran comme test de clarté. Lorsqu’il est forcé de placer un titre clair et concis sur un écran mal conçu, les concepteurs ont rapidement reconnu qu’aucun titre ne suffisait pour la page. Ils se sont rendu compte que le problème n’a pas été de choisir des mots pour un titre, mais plutôt dans une conception de l’écran défectueux. Avec cette compréhension, ils pouvaient ensuite reconcevoir l’écran pour prendre en charge une interaction utilisateur plus claire et, par conséquent, un titre plus clair.

### <a name="including-writers"></a>Y compris les enregistreurs

Au fur et à mesure de la progression de la conception, l’équipe s’est rendu compte que les rédacteurs et les éditeurs de documentation devaient créer des titres d’écran. Les enregistreurs étaient limités dans leur capacité à choisir des titres corrects dans les versions précédentes, car ils n’étaient impliqués qu’à un stade tardif. Les concepteurs ou les programmeurs ont généralement donné des titres de travail temporaires aux écrans. Ces titres ont été utilisés jusqu’à la fin du cycle du produit lorsque les auteurs ont été invités à trouver des titres d’écran finaux. À ce stade, il était trop tard pour réutiliser les écrans mal conçus.

En revanche, l’équipe Money 2000 impliquait des enregistreurs aux premières étapes du processus de conception. Cela a apporté des informations précieuses sur les titres d’écran lorsqu’il pourrait encore aider la conception. Si un écran était trop complexe pour permettre un titre clair, les rédacteurs pourraient suggérer que la page soit repensée.

À la fin du projet, les rédacteurs et les concepteurs pensaient que les titres d’écran étaient plus clairs et plus forts que dans les versions précédentes. Les enregistreurs ont également découvert qu’il est plus facile d’expliquer les nouvelles pages, ce qui simplifie le travail de documentation du produit. Tous les membres de l’équipe ont pensé que l’utilisation de toutes les disciplines dans la phase de conception rendait le produit plus facile et plus facile à utiliser.

### <a name="usability-tests"></a>Tests d’utilisation

Lors du développement de Money 2000, l’équipe a effectué plusieurs tests d’utilisation pour examiner les différences entre l’ancienne structure de navigation de Money 99 et les modifications apportées à la suite de l’application du modèle IUI.

### <a name="prototype-testing"></a>Test de prototype

Au début du processus de développement du produit, les concepteurs ont créé un prototype pour explorer la manière dont les utilisateurs réagissent à IUI. Ce travail a été effectué très tôt dans le processus de développement afin de laisser le temps d’affiner les principes du modèle avant que les programmeurs ne commencent à se détourner vers le produit lui-même.

L’équipe a créé un prototype dans Microsoft Visual Basic et HTML qui a simulé les activités de finance personnelles normalement effectuées dans Money. Dans le prototype, les utilisateurs pouvaient accéder à plus de 50 pages représentant les principales zones du produit. Dans ces domaines, ils peuvent configurer des comptes financiers, payer des factures, afficher des rapports et travailler avec leurs investissements.

Onze participants ont effectué le même ensemble de tâches dans Money 99 et le prototype IUI. Elles ont été affectées de façon aléatoire pour utiliser l’un des produits en premier. Quatre participants étaient des utilisateurs actuels de Money, quatre étaient des utilisateurs actuels d’un produit concurrent et trois n’avaient jamais utilisé un produit de finance personnel auparavant.

Les préférences globales indiquaient que les quatre utilisateurs actuels de Money ont préféré Money 99 (la version qu’ils utilisaient chez eux) tandis que les sept utilisateurs restants ont préféré le nouveau prototype à la version actuelle. Pour toutes les autres mesures, il n’existait aucune différence entre les utilisateurs des trois groupes. En termes de performances globales, les utilisateurs se trouvaient dans la mauvaise zone du produit autant de fois que le nombre de fois qu’ils utilisent Money 99 (2,82 fois par tâche) comme dans le prototype (1,45 fois par tâche). D’autres données de préférence et mesures de performances, même si elles ne sont pas significatives, sont apparues pour privilégier le prototype. Sur la base de ces données et d’autres tests, l’équipe de produit Money a décidé d’incorporer des principes IUI dans Money 2000.

### <a name="product-testing"></a>Test du produit

Une fois que la majorité du code du produit est terminée, l’équipe a effectué une autre étude d’utilisation pour examiner la dernière implémentation de IUI. Dans ce test, 10 participants qui n’avaient jamais utilisé un produit de finance personnel avant n’ont pas été sélectionnés pour utiliser Money 99 ou Money 2000. Tous les utilisateurs ont effectué les mêmes tâches.

Les utilisateurs de Money 2000 ont terminé avec succès 89% des tâches, tandis que les utilisateurs de Money 99 ont terminé avec succès uniquement 74% des tâches. Comme c’est le cas pour le prototype, les utilisateurs sont également censés être plus rapides, mais pas très différents, lors de la navigation dans Money 2000 par rapport à Money 99. En outre, les mesures globales de satisfaction subjective pour la navigation ont également tendance à être plus élevées pour Money 2000 que pour Money 99.

### <a name="controlled-testing"></a>Tests contrôlés

Étant donné que Money 2000 est énorme et complexe, il n’est pas bien adapté à l’exécution d’expériences contrôlées sur les effets de l’application de IUI. Au lieu de cela, l’équipe a créé un environnement plus restreint pour le test.

Le test impliquait une application « Stock Market Viewer » qui permettait aux utilisateurs de modifier l’affichage d’un rapport sur le marché boursier indiqué à l’écran. Les utilisateurs peuvent modifier les colonnes de données incluses dans le rapport, l’ordre des colonnes du rapport, leur alignement et le nombre de décimales utilisées. Les concepteurs souhaitaient voir comment une approche IUI de cette tâche serait exécutée par rapport à une interface utilisateur graphique conventionnelle.

La capture d’écran suivante montre l’interface utilisateur conventionnelle utilisée dans le test. Une seule boîte de dialogue effectue toutes les tâches de personnalisation des rapports. De nombreuses applications fournissent une boîte de dialogue similaire pour la sélection d’un sous-ensemble à partir d’une liste d’éléments. La boîte de dialogue contient deux listes : la liste de gauche affiche toutes les colonnes de rapport disponibles, et la droite affiche le sous-ensemble de colonnes que l’utilisateur a sélectionné pour le rapport. Des contrôles supplémentaires modifient l’ordre et les attributs de mise en forme des colonnes de rapport sélectionnées dans la liste de droite.

![capture d’écran d’une boîte de dialogue conventionnelle.](images/iuiguidelines12.png)

Pour la version IUI de cette tâche, l’équipe a créé une application de type Web. Chaque tâche de personnalisation a été placée sur une page distincte. L’application a également inclus une page principale, illustrée dans la capture d’écran suivante, qui demande aux utilisateurs comment ils souhaitent personnaliser le rapport.

![capture d’écran d’un écran de test IUI.](images/iuiguidelines13.png)

Le fait de cliquer sur les liens de cette page principale permet à l’utilisateur d’accéder à des pages supplémentaires pour effectuer des tâches de personnalisation spécifiques. Par exemple, la capture d’écran suivante montre la page utilisée pour sélectionner des colonnes de rapport.

![capture d’écran d’un écran de test IUI pour la sélection des colonnes de rapport.](images/iuiguidelines14.png)

Dans les tests des deux versions, les sujets étaient invités à personnaliser les rapports à partir d’un état de démarrage donné (indiqué à l’écran) à un état d’objectif spécifié (indiqué sur un document papier). L’ordinateur a conservé le suivi de la durée et du nombre de tentatives effectuées pour personnaliser le rapport. L’ordinateur a informé les utilisateurs lorsqu’ils ont réussi à personnaliser le rapport.

Le test comprenait 88 participants. Chaque participant a été invité à personnaliser un ensemble de 11 rapports avec l’une des deux versions de l’application. En outre, 72 de ces participants ont renvoyé une semaine plus tard pour personnaliser un autre ensemble de 11 rapports à l’aide de la même version de la première session. Chaque sujet a été classé comme utilisateur débutant de l’ordinateur, principalement à l’aide de l’ordinateur pour le courrier électronique, en lisant le solitaire et en surfant sur le Web.

Il n’y avait pas de différences significatives entre les utilisateurs des deux versions ou les autres variables intéressantes. Les utilisateurs ont effectué des tâches à la même vitesse, itéré sur la tâche le même nombre de fois et avaient les mêmes évaluations de satisfaction globales subjectives pour les deux versions. Ce test, par conséquent, n’a pas pu afficher les mesures dans lesquelles IUI a entraîné une amélioration ou une dégradation des performances ou des évaluations subjectives.

Il peut être allégué que si l’utilisateur doit naviguer davantage pour effectuer la tâche, la durée nécessaire à l’exécution de la tâche doit être supérieure. Bien que cette expérience ne suggère pas ce résultat, il est important de noter que les temps de performance moyen et leurs écarts types associés pour les deux approches différentes de cette tâche étaient quasiment identiques.

Des recherches supplémentaires seront nécessaires pour déterminer s’il existe des améliorations mesurables par rapport à l’utilisation de IUI. Au minimum, ce test n’a pas fourni de preuve selon laquelle les IUI nuisent aux performances ou à l’utilisation des produits.

### <a name="comparison-with-web-sites"></a>Comparaison avec les sites Web

De nombreux sites Web bien conçus utilisent des principes similaires au modèle IUI décrit dans ce document. Il s’agit probablement d’un effet secondaire de la façon dont le Web fonctionne. Étant donné qu’il est difficile d’implémenter des interactions complexes entre des contrôles sur une page Web unique, les concepteurs découpent souvent des tâches en parties qui impliquent plusieurs voyages sur le serveur pour obtenir une nouvelle page. Certains sites incluent même des titres de page qui indiquent clairement l’objectif de la page.

Les concepteurs d’applications traditionnelles disposent d’un ensemble d’outils encore plus riches. Cela leur donne plus de flexibilité, mais offre également davantage d’opportunités de créer des pages complexes et confuses. Lors de la création d’interfaces utilisateur inductives, les concepteurs doivent utiliser cette puissance avec discrétion et se souvenir de la clarté et de la simplicité de la valeur.

 

 





