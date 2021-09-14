---
title: Spécification UI Automation
description: cette rubrique fournit une vue d’ensemble de la spécification d’automatisation d’interface utilisateur de Microsoft, qui constitue la base de l’implémentation Windows d’ui automation.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d78298299241545033b25dccc8d79376ec55e1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010591"
---
# <a name="ui-automation-specification"></a>Spécification UI Automation

cette rubrique fournit une vue d’ensemble de la spécification d’automatisation d’interface utilisateur de Microsoft, qui constitue la base de l’implémentation Windows d’ui automation. La spécification UI Automation peut être prise en charge sur des plateformes autres que Microsoft Windows. Pour plus d’informations, consultez [UI Automation Specification](./uiauto-specandcommunitypromise.md) .

Cette rubrique contient les sections suivantes :

-   [Introducton](#introducton)
-   [Éléments UI Automation](#ui-automation-elements)
-   [Arborescence UI Automation](#ui-automation-tree)
-   [Propriétés UI Automation](#ui-automation-properties)
-   [Modèles de contrôle UI Automation](#ui-automation-control-patterns)
-   [Types de contrôle UI Automation](#ui-automation-control-types)
-   [Événements UI Automation](#ui-automation-events)
-   [Rubriques connexes](#related-topics)

## <a name="introducton"></a>Introducton

la spécification ui Automation fournit un accès par programme flexible aux éléments de l’interface utilisateur sur le bureau de Windows, ce qui permet aux produits de technologie d’assistance tels que les lecteurs d’écran de fournir aux utilisateurs finaux des informations sur l’interface utilisateur et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard.

UI Automation est plus large dans la portée qu’une simple définition d’interface. Il offre :

-   Un modèle objet et des fonctions qui permettent aux applications clientes de recevoir facilement des événements, de récupérer des valeurs de propriété et de manipuler des éléments d’interface utilisateur.
-   Infrastructure de base pour la recherche et l’extraction au-delà des limites du processus.
-   Ensemble d’interfaces permettant aux fournisseurs d’exprimer l’arborescence, les propriétés générales et les fonctionnalités des éléments d’interface utilisateur.
-   Propriété « type de contrôle » qui permet aux clients et aux fournisseurs d’indiquer clairement les propriétés communes, les fonctionnalités et la structure d’un objet d’interface utilisateur.

UI Automation améliore Microsoft Active Accessibility par :

-   L’activation de clients hors processus efficaces, tout en continuant à autoriser l’accès in-process.
-   Exposant plus d’informations sur l’interface utilisateur d’une manière qui permet aux clients d’être hors processus.
-   Coexister avec et tirer parti de Microsoft Active Accessibility sans hériter de ses limitations. Pour plus d’informations, consultez [comparaison entre Microsoft Active Accessibility et UI Automation](microsoft-active-accessibility-and-ui-automation-compared.md).
-   Fournir une alternative à [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) qui est simple à implémenter.

l’implémentation de la spécification UI Automation dans Windows fonctionnalités des interfaces basées sur le modèle COM (component Object Model) et des interfaces managées.

## <a name="ui-automation-elements"></a>Éléments UI Automation

UI Automation expose chaque partie de l’interface utilisateur aux applications clientes en tant qu' *élément Automation*. Les fournisseurs fournissent des valeurs de propriété pour chaque élément. Les éléments sont exposés sous la forme d’une arborescence, avec le bureau comme élément racine.

Les éléments Automation exposent les propriétés communes des éléments d’interface utilisateur qu’ils représentent. L’une de ces propriétés est le type de contrôle, qui décrit son apparence et ses fonctionnalités de base (par exemple, un bouton ou une case à cocher).

## <a name="ui-automation-tree"></a>Arborescence UI Automation

L’arborescence UI Automation représente l’interface utilisateur entière : l’élément racine est le Bureau actuel et les éléments enfants sont des fenêtres d’application. Chacun de ces éléments enfants peut contenir des éléments représentant des menus, des boutons, des barres d’outils, etc. Ces éléments peuvent à leur tour contenir des éléments tels que des éléments de liste, comme le montre l’illustration suivante.

![capture d’écran montrant l’arborescence UI Automation](images/uiatree.gif)

N’oubliez pas que l’ordre des frères dans l’arborescence UI Automation est très important. Les objets qui sont adjacents les uns aux autres doivent également être adjacents l’un à l’autre dans l’arborescence UI Automation.

Les fournisseurs UI Automation pour un contrôle particulier prennent en charge la navigation parmi les éléments enfants de ce contrôle. Toutefois, les fournisseurs ne sont pas concernés par la navigation entre ces sous-arbres de contrôle. Cela est géré par le noyau UI Automation, à l’aide des informations des fournisseurs de fenêtres par défaut.

Pour aider les clients à traiter les informations de l’interface utilisateur plus efficacement, le Framework prend en charge d’autres vues de l’arborescence Automation : affichage brut, vue de contrôle et affichage du contenu. Comme le montre le tableau suivant, le type de filtrage détermine les vues et le client définit l’étendue d’une vue.



| Arborescence Automation | Description                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Affichage brut        | Arborescence complète des objets d’élément Automation pour lesquels le bureau est la racine.                                          |
| Vue de contrôle    | Sous-ensemble de la vue brute qui est étroitement mappée à la structure de l’interface utilisateur lorsque l’utilisateur la perçoit.                                |
| Vue de contenu    | Sous-ensemble de l’affichage de contrôle qui contient le contenu le plus adapté à l’utilisateur, comme les valeurs d’une zone de liste déroulante de liste déroulante. |



 

Pour plus d’informations, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Propriétés UI Automation

La spécification UI Automation définit deux types de propriétés : les propriétés des éléments Automation et les propriétés de modèle de contrôle. Les propriétés des éléments Automation s’appliquent à la plupart des contrôles, fournissant des informations fondamentales sur l’élément, telles que son nom. Les propriétés de modèle de contrôle s’appliquent aux modèles de contrôle, qui sont décrits ci-après.

Contrairement à Microsoft Active Accessibility, chaque propriété UI Automation est identifiée par un GUID et un nom de programmation, ce qui rend les nouvelles propriétés plus faciles à introduire.

Pour plus d'informations, consultez [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Modèles de contrôle UI Automation

Un modèle de contrôle décrit un aspect particulier des fonctionnalités d’un élément Automation. Par exemple, un simple contrôle « clic » comme un bouton ou un lien hypertexte doit prendre en charge le modèle de contrôle Invoke pour représenter l’action « click ».

Chaque modèle de contrôle est une représentation canonique des fonctions et fonctions possibles de l’interface utilisateur. L’implémentation actuelle d’UI Automation définit 22 modèles de contrôle. l’API Windows Automation peut également prendre en charge des modèles de contrôle personnalisés. Contrairement aux propriétés de rôle ou d’état de Microsoft Active Accessibility, un élément Automation peut prendre en charge plusieurs modèles de contrôle UI Automation.

Pour plus d'informations, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Types de contrôle UI Automation

Un type de contrôle est une propriété d’élément Automation qui spécifie un contrôle connu que l’élément représente. À l’heure actuelle, UI Automation définit 38 types de contrôle, notamment Button, CheckBox, ComboBox, DataGrid, document, HYPERLINK, image, info-bulle, Tree et Window.

Avant de pouvoir assigner un type de contrôle à un élément, l’élément doit respecter certaines conditions, y compris une structure d’arborescence Automation, des valeurs de propriété, des modèles de contrôle et des événements particuliers. Toutefois, vous n’en êtes pas limité. Vous pouvez étendre un contrôle avec des modèles et des propriétés personnalisés, ainsi que les éléments prédéfinis.

Le nombre total de types de contrôle prédéfinis est nettement inférieur à celui des [rôles d’objet](object-roles.md)de Microsoft Active Accessibility, car les modèles de contrôle UI Automation peuvent être combinés pour exprimer un plus grand ensemble de fonctionnalités, contrairement aux rôles Microsoft Active Accessibility.

Pour plus d'informations, consultez [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Événements UI Automation

Les événements UI Automation notifient les applications des modifications apportées à, ainsi que les actions effectuées avec les éléments Automation. Il existe quatre types différents d’événements UI Automation, et ils ne signifient pas nécessairement que l’état visuel de l’interface utilisateur a changé. le modèle d’événement ui automation est indépendant de l’infrastructure [WinEvent](winevents-infrastructure.md) dans Windows, bien que l’API automation Windows rend les événements UI automation interopérables avec Microsoft Active Accessibility framework.

Pour plus d'informations, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Rubriques connexes

[spécification UI automation](./uiauto-specandcommunitypromise.md), [Windows vue d’ensemble de l’API automation](windows-automation-api-overview.md)
