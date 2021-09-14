---
title: ToolBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ToolBar. Les contrôles de barre d’outils permettent aux utilisateurs finaux d’activer les commandes et les outils contenus dans une application.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- UI Automation, prise en charge du type de contrôle ToolBar
- UI Automation, type de contrôle ToolBar
- UI Automation, arborescence pour le type de contrôle ToolBar
- UI Automation, propriétés du type de contrôle ToolBar
- UI Automation, modèles de contrôle pour le type de contrôle ToolBar
- UI Automation, événements pour le type de contrôle ToolBar
- arborescences, type de contrôle ToolBar
- Propriétés, type de contrôle ToolBar
- modèles de contrôle, type de contrôle ToolBar
- événements, type de contrôle ToolBar
- prise en charge du type de contrôle ToolBar
- ToolBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ToolBar
- types de contrôles, modèles de contrôle pour le type de contrôle ToolBar
- types de contrôles, prise en charge pour la barre d’outils
- types de contrôles, barre d’outils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194c9aabaa684370b99d23d91c979ff3410305b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122557"
---
# <a name="toolbar-control-type"></a>ToolBar (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Toolbar** . Les contrôles de barre d’outils permettent aux utilisateurs finaux d’activer les commandes et les outils contenus dans une application.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Toolbar** . Les exigences d’UI Automation s’appliquent à tous les contrôles ToolBar où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles ToolBar et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>ToolBar<ul><li>Plusieurs contrôles (0 ou plus)</li></ul></li></ul> | <ul><li>ToolBar<ul><li>Plusieurs contrôles (0 ou plus)</li></ul></li></ul> | 




 

Un contrôle ToolBar peut contenir n’importe quel type de contrôle dans sa sous-arborescence. Le plus souvent, ils contiennent des boutons, des zones de liste modifiables et des boutons partagés.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **Toolbar** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur       | Notes                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.  | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.  | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.  | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.       |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Barre** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle ToolBar est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle ToolBar est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.  | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Un contrôle ToolBar n’a jamais d’étiquette.                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.  | Chaîne localisée correspondant au type de contrôle **Toolbar** . La valeur par défaut est « barre d’outils » pour en-US ou anglais (États-Unis).                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Dépend     | Le contrôle ToolBar n’a pas besoin d’un nom, sauf si plusieurs sont utilisés dans une application. S’il en existe plusieurs, chacun doit avoir un nom distinctif (par exemple, « mise en forme » ou « mode plan »). |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles ToolBar. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support | Notes                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Dépend | Si la barre d’outils peut être ancrée à différentes parties de l’écran, elle doit prendre en charge le modèle de contrôle [Dock](uiauto-implementingdock.md) .                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dépend | Si la barre d’outils peut être développée et réduite pour afficher davantage d’éléments, elle doit prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Dépend | Si la barre d’outils peut être redimensionnée, pivotée ou déplacée, elle doit prendre en charge le modèle de contrôle [Transform](uiauto-implementingtransform.md) .                          |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles ToolBar. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. | Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




