---
title: Implémentation d’une interface utilisateur
description: Cette section décrit certaines des tâches associées à l’implémentation d’une interface utilisateur pour une application Windows.
ms.assetid: 889791a7-d12c-4ec6-9b04-8fed14ecdb2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941458e046a85dc6e27a684d8aa3a7ea609e889
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315732"
---
# <a name="implementing-a-user-interface"></a>Implémentation d’une interface utilisateur

Cette section décrit certaines des tâches associées à l’implémentation d’une interface utilisateur pour une application Windows.

-   [Prototype](#prototype)
-   [Composer](#construct)
-   [Ainsi](#simplify)
    -   [Réduire, réutiliser, nettoyer](#reduce-reuse-declutter)
    -   [La meilleure interface utilisateur n’est pas une interface utilisateur](#the-best-ui-is-no-ui)
    -   [L’interface utilisateur est moins performante](#less-ui-is-better-ui)
    -   [L’interface utilisateur cohérente est bonne](#consistent-ui-is-good-ui)

## <a name="prototype"></a>Prototype

Les interfaces utilisateur (IU) doivent être conçues à partir de la liste des scénarios utilisateur et des exigences qui ont été identifiés dans l’étape analyse de l’utilisateur.

Les prototypes peuvent être aussi simples que des croquis de crayon ou aussi complexes que des maquettes d’écran interactives. Conservez tout le travail précédent, car il peut être utile pour montrer aux parties prenantes les alternatives qui ont été prises en compte et explique pourquoi elles ont été ignorées.

Essayez de limiter cette étape à deux ou trois prototypes au maximum. Les prototypes ne doivent pas nécessairement être exhaustifs ; ils doivent simplement simuler efficacement l’expérience de l’utilisation de l’application réelle.

Montrez les prototypes et suivez les commentaires des utilisateurs pour identifier les tendances d’utilisation générale. Si possible, ignorez les prototypes les moins réussis et incorporez autant de commentaires utiles que possible dans un ou plusieurs des prototypes restants. Répétez ce processus à mesure que le temps et les ressources le permettent.

Différents outils de prototypage sont disponibles, dont [SketchFlow](/previous-versions/visualstudio/design-tools/expression-studio-3/ee341458(v=expression.30)) dans Microsoft Expression Studio 3, l’éditeur de disposition dans Microsoft Visual Studio, et même Microsoft Paint.

## <a name="construct"></a>Construction

Lorsque vous implémentez l’interface utilisateur pour une application, tenez compte des points suivants :

-   Structure de commande

    Déterminez s’il faut implémenter une structure de commande traditionnelle basée sur des menus et des barres d’outils, ou une autre structure de commande basée sur l’infrastructure de ruban Windows. Pour plus d’informations, consultez [menus](../menurc/menus.md), [barres d’outils](../controls/toolbar-control-reference.md)et [infrastructure de ruban Windows](../windowsribbon/-uiplat-windowsribbon-entry.md).

-   Fenêtres et boîtes de dialogue

    En fonction de la conception de l’interface utilisateur et du travail de prototypage, implémentez les fenêtres d’application, notamment la fenêtre principale, les fenêtres enfants, les boîtes de dialogue et les boîtes de message. Suivez les instructions de l’expérience utilisateur pour déterminer les styles et les contrôles à utiliser dans les fenêtres et les boîtes de dialogue. Pour plus d’informations, consultez [fenêtres](../winmsg/windows.md), [boîtes de dialogue](../dlgbox/dialog-boxes.md)et [contrôles Windows](../controls/window-controls.md).

-   Contrôles personnalisés

    Créez de nouveaux contrôles personnalisés uniquement si vous ne pouvez pas obtenir les fonctionnalités souhaitées à partir de l’un des contrôles Windows standard. Les nouveaux contrôles personnalisés sont très coûteux à développer et nécessitent un travail supplémentaire pour les rendre accessibles. Si votre application nécessite des contrôles personnalisés, assurez-vous qu’ils sont correctement exposés aux technologies d’assistance. Pour plus d’informations, consultez [contrôles personnalisés](../controls/user-controls-intro.md) et [API Windows Automation](../winauto/windows-automation-api-portal.md).

-   Prise en charge des périphériques d’entrée utilisateur standard

    La plupart des applications Windows doivent prendre en charge les entrées d’utilisateur par le biais du clavier et de la souris. La possibilité de naviguer et d’accéder à toutes les fonctionnalités de l’application par le biais du clavier est particulièrement importante pour les utilisateurs qui sont malvoyants ou qui présentent des problèmes de mobilité. Pour plus d’informations, consultez [entrée d’utilisateur](../inputdev/user-input.md) et le [logiciel d’ingénierie pour l’ebook d’accessibilité](https://www.microsoft.com/download/details.aspx?id=19262).

-   Styles visuels, animations et effets visuels

    Windows comprend plusieurs technologies que vous pouvez utiliser pour ajouter un intérêt visuel et définir l’interface utilisateur en dehors de celle d’autres applications. Cela inclut la spécification des styles visuels des contrôles, l’ajout d’animations aux éléments d’interface utilisateur et l’implémentation de divers effets visuels dans l’interface utilisateur. Pour plus d’informations, consultez [styles visuels](../controls/themes-overview.md), [Gestionnaire d’animations Windows](../uianimation/-main-portal.md)et [Gestionnaire de fenêtrage](../dwm/dwm-overview.md).

## <a name="simplify"></a>Simplifier 

Une expérience utilisateur réussie dépend de l’approche, du point de vue et des hypothèses du développeur pendant le processus de conception. Pour réaliser une compréhension élémentaire de la façon dont une application peut être utilisée par le public cible, il est nécessaire de prendre en compte les contraintes de ce qui convient le mieux aux besoins du développeur. Investir dans ce temps, nos efforts et vos recherches au début d’un projet paient des dividendes à la fin.

### <a name="reduce-reuse-declutter"></a>Réduire, réutiliser, nettoyer

Les fonctionnalités améliorent uniquement un produit s’ils sont réellement utilisés. Dans de nombreux cas, la prolifération des fonctionnalités peut compliquer l’ajout d’icônes, d’éléments de menu, de barres d’outils et de boîtes de dialogue qui interfèrent avec l’efficacité et la productivité au lieu d’ajouter de la valeur.

### <a name="the-best-ui-is-no-ui"></a>La meilleure interface utilisateur n’est pas une interface utilisateur

L’interface utilisateur implique que l’utilisateur doit interagir avec l’application pour faire en sorte qu’un événement se produise. Dans le cas idéal, aucune interaction n’est nécessaire. Du point de vue de l’utilisateur, cela fonctionne. Si une fonctionnalité peut être ajoutée pour supprimer en toute sécurité une interaction avec l’utilisateur, elle améliore considérablement l’expérience utilisateur.

### <a name="less-ui-is-better-ui"></a>L’interface utilisateur est moins performante

Dans de nombreux cas, il n’est pas possible de supprimer complètement l’interaction avec l’interface utilisateur de l’expérience utilisateur. Toutefois, l’interaction moins importante de l’utilisateur requise par une application est meilleure.

Identifiez les activités les plus courantes et les plus importantes que les utilisateurs effectuent avec l’application et faites en sorte que ces fonctions soient les plus visibles dans l’interface utilisateur. Redéléguez les autres fonctions et activités à un État plus faible, visuellement, hiérarchique ou par le biais de paramètres d’application facultatifs et de préférences utilisateur.

-   Remplacer plutôt que ajouter

    La conservation de la règle d’interface utilisateur indique que vous ajoutez des éléments uniquement lorsque vous pouvez prendre un peu de choses. Cette règle force un développeur à réfléchir de manière critique à une nouvelle fonctionnalité en prenant en compte l’impact que la fonctionnalité a sur l’ensemble de l’expérience utilisateur.

    Les nouvelles fonctionnalités ne doivent pas être promues, car elles sont nouvelles : ne confondez pas le marketing avec la convivialité. Pour aider les utilisateurs à trouver de nouvelles fonctionnalités dans votre produit, ajoutez un élément au menu **aide** qui décrit les modifications qui se sont produites depuis la dernière version de l’application.

-   L’utilisateur est une ressource limitée

    Plus la fonctionnalité est exposée à un moment donné, plus il est difficile pour un utilisateur de trouver les fonctionnalités dont il a besoin.

-   Il est impropre à l’interruption

    Quand une application affiche une boîte de dialogue, elle force l’utilisateur à arrêter tout ce qu’elle fait et à faire attention à autre chose. Si possible, supprimez complètement la nécessité d’une boîte de dialogue en évitant les cas d’erreur et les autres expériences utilisateur perturbatrices. Pour plus d’informations sur les instructions relatives aux messages, consultez [messages](https://msdn.microsoft.com/library/dd535525.aspx).

-   Simple peut être puissant

    Une interface utilisateur simple n’implique pas de fonctionnalités insuffisantes. En général, le résultat d’une interface utilisateur plus simple est une courbe d’apprentissage raccourcie, une efficacité accrue et une productivité améliorée. Cela permet à un utilisateur d’accroître ses compétences avec l’application.

### <a name="consistent-ui-is-good-ui"></a>L’interface utilisateur cohérente est bonne

En règle générale, il est recommandé d’assurer la cohérence dans l’ensemble de l’interface utilisateur d’une application. Fournir une interface utilisateur cohérente permet à un utilisateur de devenir plus efficace avec une application plus rapidement. Ils peuvent appliquer leurs connaissances existantes de l’application à différentes situations et utiliser des fonctionnalités inconnues en toute confiance.

Dans de rares cas, la cohérence n’offre aucun avantage à l’utilisateur et peut même dégrader l’expérience utilisateur. N’effectuez pas la cohérence de l’interface utilisateur si cette cohérence altère la capacité à accomplir une tâche. La cohérence en elle-même ne garantit pas la convivialité. Il est erroné de croire que la cohérence dans l’interface entraîne une bonne conception.

Par exemple, l’interface utilisateur de jeux vidéo est généralement très spécifique au type de jeu. Essayer de concevoir une interface utilisateur générique qui fonctionne bien pour deux jeux spécialisés, un qui requiert un volant et un autre qui fonctionne mieux avec une manette de jeu et des boutons, n’aura probablement pas de réussite pour les deux jeux. Au mieux, il est probable que le fond du milieu soit réalisé et n’est pas adapté aux deux.

Pour prendre cette décision, il est important de disposer de bonnes données sur la façon dont les éléments sont utilisés. N’oubliez pas les avantages et les inconvénients de chaque compromis (vitesse par rapport à la fiabilité, facilité d’apprentissage par rapport aux compétences des experts, cohérence globale et optimisation locale) et prenez les meilleures décisions pour la fonctionnalité par rapport à l’ensemble du produit.

La conception consiste à choisir l’échec : l’optimisation pour une seule chose signifie l’échec d’une autre. La clé de la bonne conception de l’interface utilisateur est de pouvoir décider quelles caractéristiques de l’application sont les plus importantes et celles qui peuvent être coupées.

 

 