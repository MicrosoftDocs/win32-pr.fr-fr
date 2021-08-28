---
title: Tree (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Tree.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- UI Automation, prise en charge du type de contrôle Tree
- UI Automation, type de contrôle Tree
- UI Automation, arborescence pour le type de contrôle Tree
- UI Automation, propriétés pour le type de contrôle Tree
- UI Automation, modèles de contrôle pour le type de contrôle Tree
- UI Automation, événements pour le type de contrôle Tree
- arborescences, type de contrôle Tree
- Propriétés, type de contrôle Tree
- modèles de contrôle, type de contrôle Tree
- événements, type de contrôle Tree
- prise en charge du type de contrôle Tree
- Tree (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Tree
- types de contrôles, modèles de contrôle pour le type de contrôle Tree
- types de contrôle, prise en charge de l’arborescence
- types de contrôles, arborescence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7ac6330428c2e79fca1e9a51d4ca0f7c63e8a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472845"
---
# <a name="tree-control-type"></a>Tree (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Tree** .

le type de contrôle **Tree** est utilisé pour les conteneurs dont le contenu est pertinent en tant que hiérarchie de nœuds, comme c’est le cas pour l’affichage des fichiers et des dossiers dans le volet gauche de l’explorateur de Windows. Chaque nœud peut contenir d’autres nœuds, appelés nœuds enfants. Vous pouvez afficher les nœuds parents, ou nœuds qui contiennent des nœuds enfants, sous forme développée ou réduite. le contrôle d’arborescence Windows (identifié par [**WC \_ TREEVIEW**](/windows/desktop/Controls/common-control-window-classes)) est un exemple de contrôle qui appartient au type de contrôle **tree** .

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Tree** . Les spécifications d’UI Automation s’appliquent à tous les contrôles d’élément d’arborescence où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’arborescence, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Arborescence<ul><li>DataItem (0 ou plus)</li><li>TreeItem (0 ou plus)<ul><li>TreeItem (0 ou plus)<ul><li>...</li></ul></li></ul></li><li>ScrollBar (0, 1, 2)</li></ul></li></ul> | <ul><li>Arborescence<ul><li>DataItem (0 ou plus)</li><li>TreeItem (0 ou plus)<ul><li>TreeItem (0 ou plus)<ul><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

L’affichage de contrôle de l’arborescence UI Automation se compose des éléments suivants :

-   Zéro de nombreux éléments dans le conteneur (les éléments peuvent être basés sur les types de contrôle [TreeItem](uiauto-supporttreeitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) ).
-   Zéro, un ou deux contrôles scroll bar

L’affichage de contenu de l’arborescence UI Automation se compose de zéro ou de plusieurs éléments dans le conteneur (les éléments peuvent être basés sur les types de contrôle [TreeItem](uiauto-supporttreeitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) ).

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **Tree** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Les contrôles d’arborescence ont un point interactif qui amène l’arborescence ou l’un des éléments du conteneur d’arborescence à recevoir le focus. Un contrôle d’arborescence peut avoir un point cliquable uniquement s’il est possible de cliquer sur un emplacement dans l’arborescence sans entraîner la sélection d’un élément ou la réception du focus. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Arborescence**   | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle d’arborescence est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                         |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle d’arborescence est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | Si une étiquette est associée au contrôle d’arborescence, cette propriété retourne un pointeur [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour cette étiquette. Sinon, la propriété retourne une référence null.                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle d' **arborescence** . La valeur par défaut est « Tree » pour « fr-fr » ou « anglais » (États-Unis).                                                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | La valeur de propriété du nom d’un contrôle d’arborescence provient généralement du texte correspondant à l’étiquette du contrôle. S’il n’y a pas d’étiquette de texte, vous devez fournir une valeur pour cette propriété.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’arborescence. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                                             | Prise en charge/valeur | Notes                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Dépend       | Implémentez le modèle de contrôle [Scroll](uiauto-implementingscroll.md) si les éléments du conteneur d’arborescence peuvent faire l’objet d’un défilement.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Dépend       | Les contrôles d’arborescence qui contiennent un ensemble d’éléments sélectionnables doivent implémenter le modèle de contrôle [Selection](uiauto-implementingselection.md) . Elle n’est pas nécessaire si la sélection d’un élément ne transmet pas d’informations significatives à l’utilisateur. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Consultez les remarques.    | Implémentez cette propriété si le contrôle d’arborescence prend en charge la sélection multiple (la plupart des contrôles d’arborescence ne prennent pas en charge la sélection multiple).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Consultez les remarques.    | La valeur de cette propriété est exposée si le contrôle nécessite la sélection d’un élément.                                                                                                                                               |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation que tous les contrôles d’arborescence doivent prendre en charge. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Notes                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                      | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)                                                            | Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 
