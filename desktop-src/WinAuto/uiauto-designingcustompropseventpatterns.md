---
title: Concevoir des propriétés personnalisées, des événements et des modèles de contrôle
description: La conception d’une propriété, d’un événement ou d’un modèle de contrôle personnalisé doit être utile dans un large éventail d’implémentations de contrôles.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- UI Automation, propriétés personnalisées
- UI Automation, vue d’ensemble des événements
- UI Automation, vue d’ensemble des modèles de contrôle
- UI Automation, concevoir des propriétés personnalisées
- UI Automation, concevoir des événements
- UI Automation, concevoir des modèles de contrôle
- UI Automation, WinEvents
- Propriétés personnalisées, concevoir
- événements, concevoir
- événements, WinEvents
- modèles de contrôle, concevoir
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5b95d7daa3570e8b4b9b1d61c7c5f5590c6456d83190195e57af66811f1672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324798"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Concevoir des propriétés personnalisées, des événements et des modèles de contrôle

La conception d’une propriété, d’un événement ou d’un modèle de contrôle personnalisé doit être utile dans un large éventail d’implémentations de contrôles. Les conceptions spécifiques aux contrôles ou aux applications, qui ne sont utiles que dans des scénarios limités, doivent être évitées. La conception doit suivre l’exemple des propriétés, des événements et des modèles de contrôle de Microsoft UI Automation existants, qui ont été correctement spécifiés pour répondre aux besoins d’un large éventail d’applications d’accessibilité et de test automatisé.

L’implémentation de la spécification d’une propriété, d’un événement ou d’un modèle de contrôle personnalisé implique la coopération et l’accord des parties à la fois sur les côtés du client et du fournisseur, et exige que les deux parties implémentent la spécification de manière cohérente. Les entreprises sont encouragées à collaborer avec les organisations du secteur telles que l' [interopérabilité de l’accessibilité (AIA)](https://www.atia.org/) pour concevoir et publier la spécification de la propriété, de l’événement ou du modèle de contrôle personnalisé. De cette façon, le consensus peut être atteint et l’interopérabilité avec la plus grande variété d’applications peut être assurée.

Cette rubrique contient les sections suivantes :

-   [Quand utiliser des propriétés et des événements personnalisés](#when-to-use-custom-properties-and-events)
-   [Conception de propriétés personnalisées](#designing-custom-properties)
-   [Conception d’événements personnalisés](#designing-custom-events)
    -   [Événements UI Automation personnalisés et WinEvents](#custom-ui-automation-events-and-winevents)
-   [Conception de modèles de contrôle personnalisés](#designing-custom-control-patterns)
-   [Types de contrôles personnalisés](#custom-control-types)
-   [Rubriques connexes](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Quand utiliser des propriétés et des événements personnalisés

Avant de créer un modèle de contrôle, d’événement ou de propriété personnalisé, assurez-vous que l’Automation d’interface utilisateur ne fournit pas de solution existante. Par exemple, la création d’un modèle de contrôle « Click » personnalisé n’est pas nécessaire, car le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) décrit déjà cette fonctionnalité.

Si vous décidez qu’une propriété, un événement ou un modèle de contrôle personnalisé est requis, assurez-vous qu’il n’est pas trop vague ou générique. Par exemple, un modèle de contrôle appelé « show » n’est pas utile, car la visibilité d’un contrôle peut être indiquée par une propriété Availability sur l’élément, telle que [**UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) ou [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).

Avant d’implémenter une solution personnalisée, assurez-vous qu’elle est nécessaire, puis concevez entièrement la fonctionnalité.

## <a name="designing-custom-properties"></a>Conception de propriétés personnalisées

UI Automation comprend deux types de propriétés de base : les propriétés des éléments Automation et les propriétés de modèle de contrôle. Les propriétés de l’élément Automation consistent en un ensemble commun de propriétés, telles que Name, AcceleratorKey et ClassName, qui sont exposées par tous les éléments UI Automation, quel que soit le type de contrôle. Les propriétés de modèle de contrôle sont exposées par un contrôle via un modèle de contrôle particulier. Chaque modèle de contrôle a un ensemble correspondant de propriétés de modèle de contrôle que le contrôle doit exposer. Par exemple, un contrôle qui prend en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) expose les propriétés ColumnCount et RowCount.

Une propriété d’élément Automation personnalisée ou une propriété de modèle de contrôle doit respecter les règles de conception suivantes :

-   Une propriété personnalisée doit avoir l’un des types de données suivants spécifié par l’énumération [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) . Aucun autre type de données n’est pris en charge pour les propriétés personnalisées.
    -   **UIAutomationType \_ bool**
    -   **UIAutomationType \_ double**
    -   **\_Élément UIAutomationType**
    -   **UIAutomationType \_ int**
    -   **\_Point UIAutomationType**
    -   **\_Chaîne UIAutomationType**
-   Si la propriété personnalisée contient des données de chaîne ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)), la spécification doit indiquer si la propriété est localisable (autrement dit, si la chaîne peut être traduite dans des langages d’interface utilisateur différents).
-   La propriété personnalisée ne doit pas chevaucher les fonctionnalités ou les fonctionnalités des propriétés existantes.

## <a name="designing-custom-events"></a>Conception d’événements personnalisés

Les applications utilisent les notifications d’événements UI Automation pour répondre aux modifications et aux actions impliquant des éléments d’interface utilisateur. La plupart des propriétés sont associées à des événements de modification de propriété qui sont déclenchés par UI Automation lorsque la valeur de la propriété change. Si vous introduisez une propriété personnalisée, vous devez envisager d’introduire des événements personnalisés correspondants qui peuvent également être nécessaires.

Un événement personnalisé doit respecter les règles de conception suivantes :

-   L’événement personnalisé doit être « sans État ». Elle ne peut pas être associée à une propriété ou une valeur spécifique.
-   L’événement personnalisé ne doit pas chevaucher la définition ou le rôle d’un événement existant.

### <a name="custom-ui-automation-events-and-winevents"></a>Événements UI Automation personnalisés et WinEvents

les [WinEvents](winevents-infrastructure.md) sont un mécanisme de communication et d’événement d’événements très utile dans la plate-forme Microsoft Windows. Toutefois, l’introduction d’un nouvel ID WinEvent est risquée, car cela peut provoquer des collisions avec d’autres applications ou le système d’exploitation, entraînant une instabilité du système. Pour éviter les collisions, Microsoft a défini plusieurs catégories différentes de WinEvents et, pour chaque catégorie, a défini une ou plusieurs plages de valeurs à utiliser en tant qu’ID WinEvent. Pour plus d’informations, consultez [allocation d’ID WinEvent](allocation-of-winevent-ids.md).

Les événements UI Automation personnalisés évitent les conflits en allouant l’ID d’événement en interne dans l’infrastructure UI Automation.

## <a name="designing-custom-control-patterns"></a>Conception de modèles de contrôle personnalisés

Un modèle de contrôle est une interface avec des propriétés, des méthodes et des événements qui définissent une partie discrète des fonctionnalités disponibles à partir d’un élément Automation. Les méthodes de modèle de contrôle permettent aux clients UI Automation de manipuler un aspect particulier du contrôle. Les propriétés et les événements du modèle de contrôle fournissent des informations sur certains aspects du contrôle et fournissent des informations sur l’état de l’élément Automation qui implémente le modèle de contrôle.

Un modèle de contrôle personnalisé doit respecter les règles de conception suivantes :

-   Un modèle de contrôle personnalisé doit couvrir un scénario particulier. Par exemple, le modèle de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) est destiné à interroger un objet contenu indépendamment de l’état de la virtualisation, mais il n’énumère pas ou ne compte pas les objets contenus.
-   Un modèle de contrôle personnalisé ne doit pas chevaucher les fonctionnalités des modèles de contrôle existants. Par exemple, les modèles de contrôle [Invoke](uiauto-implementinginvoke.md) et [ExpandCollapse](uiauto-implementingexpandcollapse.md) ne doivent pas être combinés et présentés comme un nouveau modèle de contrôle. Réutilisez des modèles de contrôle existants ou définissez des scénarios uniques avec de nouveaux modèles de contrôle.
-   Plusieurs modèles de contrôle personnalisés peuvent être conçus pour prendre en charge des scénarios complexes. Par exemple, les modèles de contrôle [Selection](uiauto-implementingselection.md) et [SelectionItem](uiauto-implementingselectionitem.md) fonctionnent ensemble pour prendre en charge les scénarios de sélection d’objets généraux.

## <a name="custom-control-types"></a>Types de contrôles personnalisés

Bien que cette rubrique se concentre sur la façon d’inscrire des propriétés, des événements et des modèles de contrôle UI Automation personnalisés, il est également possible d’introduire de nouveaux types de contrôle. Contrairement aux propriétés personnalisées, aux événements et aux modèles de contrôle, un type de contrôle personnalisé ne peut pas être inscrit par programmation au moment de l’exécution, car il s’agit simplement d’une valeur potentielle de la propriété ControlType UI Automation. Toutefois, un ID de type de contrôle personnalisé peut être défini, publié et mis à la disposition d’autres clients et fournisseurs. Pour plus d’informations sur les types de contrôle, consultez [UI Automation Control types Overview](uiauto-controltypesoverview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Enregistrement des propriétés personnalisées, des événements et des modèles de contrôle](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 