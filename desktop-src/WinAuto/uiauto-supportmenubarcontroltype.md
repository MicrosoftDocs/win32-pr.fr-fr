---
title: BarreMenus (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- UI Automation, prise en charge du type de contrôle MenuBar
- UI Automation, type de contrôle MenuBar
- UI Automation, arborescence pour le type de contrôle MenuBar
- UI Automation, propriétés pour le type de contrôle MenuBar
- UI Automation, modèles de contrôle pour le type de contrôle MenuBar
- UI Automation, événements pour le type de contrôle MenuBar
- arborescences, type de contrôle MenuBar
- Propriétés, BarreMenus (type de contrôle)
- modèles de contrôle, type de contrôle MenuBar
- événements, type de contrôle MenuBar
- prise en charge du type de contrôle MenuBar
- BarreMenus (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle MenuBar
- types de contrôle, modèles de contrôle pour le type de contrôle MenuBar
- types de contrôles, prise en charge de MenuBar
- types de contrôles, BarreMenus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558a734d69a9197b3e0a8d6c5655405074878bca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192643"
---
# <a name="menubar-control-type"></a>BarreMenus (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **MenuBar** .

Les contrôles de barre de menus sont un exemple de contrôles qui implémentent le type de contrôle **MenuBar** . Les barres de menus permettent aux utilisateurs d’activer les commandes et les options contenues dans une application.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **MenuBar** . Les spécifications d’UI Automation s’appliquent à tous les contrôles de barre de menus où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de barre de menus, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>MenuBar<ul><li>MenuItem (1 ou plus)</li><li>Autres contrôles (0 ou plusieurs)</li></ul></li></ul> | <ul><li>Non applicable<ul><li>MenuItem (1 ou plus)</li><li>Autres contrôles (0 ou plusieurs)</li></ul></li></ul> | 




 

Un contrôle de barre de menus apparaît toujours dans l’affichage de contrôle, mais pas dans l’affichage de contenu, car il ne transmet généralement pas d’informations significatives à l’utilisateur final (sauf si l’application contient plus d’une barre de menus).

Les clients UI Automation peuvent écouter l’événement [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md) pour s’assurer qu’ils sont régulièrement avertis lorsque l’interface utilisateur passe en mode de menu. Quand l’application est en mode de menu, toutes les entrées au clavier peuvent être capturées pour la navigation dans les menus (par exemple, l’entrée peut appeler le menu **Enregistrer** au lieu de taper le caractère dans la zone cliente de l’application). L’événement **UIA \_ MenuModeStartEventId** doit précéder le premier événement [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) pour garantir la cohérence logique. L’événement [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md) suit le dernier événement [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) . Un clic sur un élément de menu peut également déclencher immédiatement l’événement **UIA \_ MenuModeStartEventId** , suivi d’un événement **UIA \_ MenuOpenedEventId** .

Un contrôle de barre de menus peut contenir d’autres contrôles, tels que des contrôles d’édition et des zones de liste déroulante, au sein de sa structure. Ces contrôles supplémentaires correspondent aux « autres contrôles » répertoriés ci-dessus dans les affichages de contrôle et de contenu.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **MenuBar** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur       | Notes                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | NULL        | Les barres de menus n’ont généralement pas de touches accélérateur.                                                                                                                                                                                          |
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | « ALT »       | En appuyant sur la touche ALT, vous devez généralement mettre le focus sur la barre de menus de l’application.                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.  | La valeur exposée par cette propriété doit inclure tous les contrôles qu’elle contient.                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE       | Le contrôle de barre de menus n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle de barre de menus est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE        | Les contrôles de barre de menus sont actifs via le clavier, car les contrôles qu’ils contiennent peuvent recevoir le focus clavier.                                                                                                                                      |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consultez les remarques.  | La valeur de cette propriété varie selon que le contrôle est visible ou non à l’écran.                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Les contrôles de barre de menus n’ont généralement pas d’étiquette.                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.  | Chaîne localisée correspondant au type de contrôle **MenuBar** . La valeur par défaut est « barre de menus » pour en-US ou anglais (États-Unis).                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.  | Le contrôle de barre de menus n’a pas besoin d’un nom, sauf si une application contient plusieurs barres de menus. S’il existe plusieurs barres de menus dans une application, utilisez cette propriété pour exposer des noms distinctifs, tels que « mise en forme » ou « mode plan ». |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Dépend     | Cette propriété indique si le contrôle de barre de menus est horizontal ou vertical.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de barre de menus. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support | Notes                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dépend | Si le contrôle peut être développé ou réduit, il doit implémenter le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Dépend | Si le contrôle peut être ancré à différentes parties de l’écran, il doit implémenter le modèle de contrôle [Dock](uiauto-implementingdock.md) .   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Dépend | Si le contrôle peut être redimensionné, pivoté ou déplacé, il doit implémenter le modèle de contrôle [Transform](uiauto-implementingtransform.md) .      |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre de menus. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




