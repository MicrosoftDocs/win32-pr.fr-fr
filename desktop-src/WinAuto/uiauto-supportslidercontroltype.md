---
title: Slider (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- UI Automation, prise en charge du type de contrôle Slider
- UI Automation, type de contrôle Slider
- UI Automation, arborescence pour le type de contrôle Slider
- UI Automation, propriétés pour le type de contrôle Slider
- UI Automation, modèles de contrôle pour le type de contrôle Slider
- UI Automation, événements pour le type de contrôle Slider
- arborescences, type de contrôle Slider
- Propriétés, type de contrôle Slider
- modèles de contrôle, curseur, type de contrôle
- événements, type de contrôle Slider
- prise en charge du type de contrôle Slider
- Slider (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Slider
- types de contrôles, modèles de contrôle pour le type de contrôle Slider
- types de contrôles, prise en charge du curseur
- types de contrôles, Slider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354217323ba4c3c59e416f7b9c36661d8ffe8a77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192620"
---
# <a name="slider-control-type"></a>Slider (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Slider** .

Un contrôle Slider est un contrôle composite avec des boutons qui permettent à un utilisateur de définir une plage numérique ou de sélectionner un ensemble d’éléments.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Slider** . Les exigences d’UI Automation s’appliquent à tous les contrôles Slider où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles Slider et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Curseur<ul><li>Bouton (2 ou 4)</li><li>Thumb (1)</li><li>Élément de liste (0 ou plusieurs)</li></ul></li></ul> | <ul><li>Curseur<ul><li>Élément de liste (0 ou plusieurs)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Slider. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | La majorité des contrôles Slider doivent retourner l’erreur [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) , car l’intégralité du rectangle englobant du contrôle Slider est occupée par les contrôles enfants. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Curseur** | Cette valeur est la même pour toutes les infrastructures.                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle Slider est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle Slider est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété. Les enfants (boutons et Thumb) d’un contrôle Slider ne doivent jamais prendre le focus. Le focus doit toujours rester sur le contrôle Slider lui-même.       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | Si une étiquette de texte statique est associée au contrôle, cette propriété doit exposer une référence à ce contrôle. Si le contrôle de texte est un sous-composant d’un autre contrôle, il n’aura pas de propriété **LabeledBy** définie.   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Slider** . La valeur par défaut est « Slider » pour en-US ou anglais (États-Unis).                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le nom du contrôle Slider est généralement généré à partir d’une étiquette de texte statique. S’il n’y a pas d’étiquette de texte statique, une valeur de propriété pour le **nom** doit être affectée par le développeur de l’application.                              |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Slider. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                          | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Dépend       | Un curseur doit prendre en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) si le contenu peut être défini sur une valeur comprise dans une plage numérique.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Dépend       | Un curseur doit prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) si le contenu représente une valeur parmi un ensemble discret d’options. Quand le modèle de contrôle Selection est pris en charge, la sélection correspondante doit être exposée sous la forme d’un ou plusieurs éléments de liste enfants du curseur. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Dépend       | Un curseur doit prendre en charge le modèle de contrôle [value](uiauto-implementingvalue.md) si le contenu représente une valeur parmi un ensemble discret d’options.                                                                                                                                                     |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Slider. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.        | Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.   |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)                                       | Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                  | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




