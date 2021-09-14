---
title: ComboBox (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- UI Automation, prise en charge du type de contrôle ComboBox
- UI Automation, type de contrôle ComboBox
- UI Automation, arborescence pour le type de contrôle ComboBox
- UI Automation, propriétés du type de contrôle ComboBox
- UI Automation, modèles de contrôle pour le type de contrôle ComboBox
- UI Automation, événements pour le type de contrôle ComboBox
- arborescences, type de contrôle ComboBox
- Propriétés, ComboBox (type de contrôle)
- modèles de contrôle, ComboBox (type de contrôle)
- événements, type de contrôle ComboBox
- prise en charge du type de contrôle ComboBox
- ComboBox (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ComboBox
- types de contrôle, modèles de contrôle pour le type de contrôle ComboBox
- types de contrôles, prise en charge du contrôle ComboBox
- types de contrôles, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9d9f38dab9877aee38773e5c900ee125d2ba6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122605"
---
# <a name="combobox-control-type"></a>ComboBox (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **ComboBox** .

Une zone de liste modifiable est une zone de liste associée à un contrôle statique ou à un contrôle d’édition qui affiche dans la zone de liste l’élément actuellement sélectionné. La zone de liste du contrôle est affichée en permanence ou apparaît uniquement quand l’utilisateur sélectionne la flèche de déroulement (qui est un bouton de commande) à côté du contrôle. Si le champ de sélection est un contrôle d’édition, l’utilisateur peut entrer des informations qui ne sont pas dans la liste. Sinon, l’utilisateur peut sélectionner uniquement les éléments de la liste.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **ComboBox** . Les exigences d’UI Automation s’appliquent à tous les contrôles de zone de liste déroulante où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de zone de liste déroulante et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>ComboBox<ul><li>Edit (0 ou 1)</li><li>List (0 ou 1)</li><li>List Item (enfant de List. De 0 à plusieurs)</li><li>Button (1)</li></ul></li></ul> | <ul><li>ComboBox<ul><li>List Item (De 0 à plusieurs)</li></ul></li></ul> | 




 

Le contrôle d’édition dans l’affichage de contrôle de la zone de liste déroulante n’est nécessaire que si la zone de liste modifiable peut être modifiée pour prendre n’importe quelle entrée, comme c’est le cas de la zone de liste déroulante dans la boîte de dialogue **exécuter** .

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **ComboBox** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | Le texte d’aide pour les contrôles de zone de liste modifiable doit expliquer pourquoi l’utilisateur est invité à choisir une option dans la zone de liste déroulante. Le texte est semblable aux informations présentées dans une info-bulle. Par exemple, « Sélectionnez un élément pour définir la résolution d’affichage de votre moniteur ».                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Les contrôles de zone de liste modifiable sont toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Les contrôles de zone de liste modifiable sont toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Les contrôles de zone de liste modifiable peuvent recevoir le focus clavier. Toutefois, lorsqu’un client UI Automation définit le focus sur une zone de liste déroulante, tout élément de la sous-arborescence de zone de liste déroulante peut recevoir le focus.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | Les contrôles de zone de liste modifiable ont généralement une étiquette de texte statique référencée par cette propriété.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **ComboBox** . La valeur par défaut est « zone de liste déroulante » pour en-US ou anglais (États-Unis).                                                                                                                                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le nom du contrôle de zone de liste déroulante est généralement généré à partir d’une étiquette de texte statique. S’il n’y a pas d’étiquette de texte statique, vous devez affecter une valeur à la propriété **Name** . La propriété **Name** ne doit jamais contenir le contenu actuel de la zone de liste déroulante ou changer lorsque le contenu de la zone de liste déroulante change. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de zone de liste déroulante. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support  | Notes                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obligatoire | Le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) doit être pris en charge, car un contrôle de zone de liste déroulante doit toujours contenir un bouton déroulant.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Dépend  | Affiche la sélection actuelle dans la zone de liste modifiable. La prise en charge du modèle de contrôle [Selection](uiauto-implementingselection.md) est déléguée à la zone de liste sous la zone de liste déroulante, mais n’est peut-être pas toujours possible.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dépend  | Si la zone de liste déroulante peut prendre des valeurs de texte arbitraires, le modèle de contrôle [value](uiauto-implementingvalue.md) doit être pris en charge. Ce modèle permet de définir par programmation le contenu de la chaîne de la zone de liste déroulante. Si le modèle de contrôle value n’est pas pris en charge, l’utilisateur doit sélectionner parmi les éléments de liste dans la sous-arborescence de la zone de liste déroulante. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Jamais    | Le modèle de contrôle [Scroll](uiauto-implementingscroll.md) n’est jamais pris en charge directement sur une zone de liste déroulante. Il est pris en charge si une zone de liste contenue dans une zone de liste déroulante peut faire défiler et uniquement lorsque la zone de liste est visible à l’écran.                                                                                                              |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de zone de liste déroulante. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                                               | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




