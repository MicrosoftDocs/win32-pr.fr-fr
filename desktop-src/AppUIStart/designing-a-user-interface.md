---
title: Conception d’une interface utilisateur
description: Cette section décrit en détail certaines des tâches associées à la conception d’une interface utilisateur pour une application Windows.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97d5027baf7276b1353e03254478545e554daa5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463451"
---
# <a name="designing-a-user-interface"></a>Conception d’une interface utilisateur

Cette section décrit en détail certaines des tâches associées à la conception d’une interface utilisateur pour une application Windows.

-   [Introduction](#introduction)
-   [Spécifications fonctionnelles](#functional-requirements)
-   [Analyse de l’utilisateur](#user-analysis)
    -   [Instructions de problème](#problem-statements)
    -   [Priorité](#priorities)
-   [Conception conceptuelle](#conceptual-design)
-   [Conception logique](#logical-design)
-   [Conception physique](#physical-design)

## <a name="introduction"></a>Introduction

La conception de l’interface utilisateur peut être divisée en trois éléments essentiels : fonctionnalités, esthétiques et performances.

Plus souvent, le principal objectif du développement de l’application est la fonctionnalité. L’application peut-elle être utilisée ? Autorise-t-il les utilisateurs à effectuer des tâches ? Toutefois, la fonctionnalité n’est qu’une partie de l’histoire.

Les esthétiques décrivent comment les éléments sont affichés et présentés, le style dans lequel les choses sont communiquées à l’utilisateur. Les esthétiques sont très subjectives et beaucoup plus difficiles à quantifier que les exigences fonctionnelles et les mesures de performance. Les esthétiques s’imposent généralement à des choix simples : la façon dont les couleurs se complètent les unes avec les autres ou comment les éléments de l’interface utilisateur transmettent leur signification, qui affectent souvent la manière dont une personne pense à un élément et influence la réussite de son utilisation.

Les performances sont mesurées par non seulement la vitesse, mais également la fiabilité. Si une application semble intéressante, est facile à utiliser, mais se bloque de façon répétée, elle ne sera probablement pas très efficace. L’application doit fournir à l’utilisateur une confiance totale dans sa fiabilité.

Voici quelques-unes des tâches de phase de conception qui peuvent contribuer à une interface utilisateur réussie pour une application Windows.

## <a name="functional-requirements"></a>Spécifications fonctionnelles

Tenez compte des suggestions suivantes au début de la phase de conception pour optimiser l’expérience utilisateur dans l’audience la plus large possible :

-   Suivez les instructions relatives à la conception de l’interface utilisateur.

    Familiarisez-vous avec les instructions d’interaction avec l' [expérience utilisateur Windows](../uxguide/guidelines.md) et reportez-vous souvent sur la conception, l’implémentation et le test de la progression de l’interface utilisateur de l’application.

-   Assurez-vous que l’interface utilisateur est accessible.

    Veillez à intégrer l’accessibilité dans la conception de l’interface utilisateur à partir du début du cycle de vie du produit. La réadaptation de l’accessibilité peut être extrêmement coûteuse, car une partie du développement de l’accessibilité nécessite une attention au niveau de l’architecture. Pour plus d’informations, téléchargez le [logiciel d’ingénierie pour l’ebook d’accessibilité](https://www.microsoft.com/download/details.aspx?id=19262).

-   Prendre en charge la place de marché internationale.

    Windows comprend des technologies qui permettent de prendre en charge de nombreuses cultures et langages écrits dans une application Windows. Si l’application cible la place de marché internationale, il est important d’inclure la prise en charge de l’internationalisation dans la conception de l’interface utilisateur à partir du début du projet. Pour plus d’informations, consultez [internationalisation pour les applications Windows](../intl/international-support.md).

## <a name="user-analysis"></a>Analyse de l’utilisateur

Une étape critique dans la conception d’une interface réussie consiste à acquérir une compréhension de base de ce que les utilisateurs ont besoin et veulent d’une application avant d’écrire du code. N’oubliez pas que les utilisateurs potentiels d’une application effectuent déjà leur travail d’une certaine manière, et que les outils et les processus existants doivent être reconnus le plus complet possible. Ne concevez pas sans que ces problèmes soient entièrement étudiés.

L’approche la plus simple et la plus formelle est la communication avec les utilisateurs prévus du produit. Obtenir des informations directement à partir de la source : Évitez d’utiliser des responsables ou des dirigeants comme serveurs proxy pour les véritables consommateurs. Envisagez de faire en sorte que de petits groupes de développeurs et de responsables de programme paient des visites informelles aux utilisateurs dans leur lieu de travail, où il est possible de discuter de leur fonctionnement et de recueillir des détails sur les problèmes rencontrés avec leurs outils actuels.

N’oubliez pas que vous ne devez pas poser de questions principales ou biaisées, car cela affecte directement la qualité et la validité des commentaires des utilisateurs. Gardez à l’esprit les points suivants lorsque vous composez des questions pendant cette phase :

-   Qui sont nos utilisateurs ? Quelles sont les compétences et les connaissances nécessaires ?
-   Quelles sont les différentes sources de données que nous pouvons utiliser pour comprendre leur expérience ?
-   Quels sont les objectifs et les tâches qui seront utilisés par notre produit ?
-   Quelles sont les hypothèses que nous effectuons et comment les vérifier ?
-   Quelles sont les sources de données ? (Les études de convivialité et les évaluations heuristiques sont de bons endroits pour commencer.)

### <a name="problem-statements"></a>Instructions de problème

Une fois que tous les commentaires des utilisateurs ont été collectés, analysez-les et transformez-les en problèmes et exigences connexes. Essayez d’éviter de réfléchir aux solutions à ce stade. Assurez-vous que les problèmes sont entièrement identifiés, pas seulement les symptômes.

Il est souvent utile de composer une liste d’instructions de problème en une phrase (du point de vue des utilisateurs) pour chaque problème ou exigence. Par exemple, « redimensionner la largeur de la zone d’édition à 15 caractères » n’est pas un problème. Mais « il est trop difficile de taper des termes de recherche longs » est une instruction de problème valide. La différence est spectaculaire. Essayez de ne pas définir la solution et le problème en même temps : souvent, le problème réel est perdu. Dans cet exemple, il peut y avoir de nombreuses autres façons de résoudre le problème des termes de recherche, notamment la modification de la taille de la zone d’édition. Gardez toujours les autres solutions à l’esprit.

Voici des exemples supplémentaires d’instructions de problème :

-   Il est difficile de naviguer d’une section du site Web à une autre.
-   Les utilisateurs doivent attendre trop longtemps le chargement du logiciel.
-   Nos messages d’erreur de sécurité sont difficiles à comprendre.
-   La page d’inscription contient trop de questions et les utilisateurs l’abandonnent souvent.
-   La recherche d’un produit spécifique sur l’index de site est trop difficile.

Si les déclarations de problème sont suffisamment larges, il est probable qu’il y ait de nombreuses façons novatrices et créatives de les résoudre.

### <a name="priorities"></a>Priorités

L’acte consistant à prendre une liste d’éléments et à les classer par priorité définit une mise en version. Sans priorités claires, les équipes peuvent combattre et prendre des mesures sur ce qui doit être fait et les éléments à couper. Le travail impliqué dans le paramétrage des priorités doit être plus facile avec la recherche terminée, mais il s’agit toujours d’un défi.

La définition des priorités requiert la possibilité d’évaluer au moins trois critères : planification, équipe et entreprise. Il peut y avoir une planification prédéfinie pour le projet, qui limite la taille et l’échelle du travail qui peut être effectué. Un problème susceptible de nécessiter la réécriture de la moitié de la base de code ne doit pas être tenté durant un petit cycle de version.

La composition et la nature d’une équipe définissent les genres de travail qui peuvent être effectués. Quels autres engagements l’équipe a-t-elle ? Existe-t-il un concepteur ou un ingénieur à la convivialité sur l’équipe ? Quelles sont les compétences de l’équipe en matière de conception Web ou d’interface utilisateur ? La dernière et la plus importante sont les considérations commerciales. Quels sont les objectifs de chiffre d’affaires pour ce projet ? Quels sont les concurrents ? Quels sont les avantages de la résolution de certains problèmes ? Quels sont les partenariats pouvant être falsifiés ? Toutes les autres considérations doivent également être identifiées avant de hiérarchiser la liste.

Une fois l’ordre de priorité défini, la liste des instructions à problème définit la direction du produit et s’assure que le développement est ciblé dans les domaines appropriés.

## <a name="conceptual-design"></a>Conception conceptuelle

En règle générale, l’interface utilisateur n’est pas traitée dans la phase de conception conceptuelle. Toutefois, cette phase requiert un modèle d’entreprise complet avec des profils utilisateur complets et des scénarios d’utilisation qui sont impératifs pour une expérience utilisateur réussie.

## <a name="logical-design"></a>Conception logique

La phase de conception logique est le moment où les prototypes initiaux qui prennent en charge la conception conceptuelle sont développés.

Les technologies matérielles et logicielles spécifiques à utiliser pendant le développement sont également identifiées dans cette phase, qui peuvent déterminer les fonctionnalités de l’interface utilisateur dans le produit final. Pour plus d’informations, consultez technologies de l' [interface utilisateur](user-interface-technologies-for-windows-applications.md).

Outre les outils de développement, les différentes exigences matérielles et les facteurs de forme qui doivent être ciblés par l’application doivent être identifiés.

## <a name="physical-design"></a>Conception physique

La phase de conception physique détermine la façon dont une conception d’interface utilisateur doit être implémentée pour le matériel et les facteurs de forme spécifiques qui ont été identifiés dans la conception logique.

Au cours de cette phase, les limitations du matériel ou du facteur de forme peuvent entraîner des contraintes inattendues sur l’interface utilisateur qui nécessitent des améliorations significatives de la conception.

 

 