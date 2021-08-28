---
title: Spinner (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- UI Automation, prise en charge du type de contrôle Spinner
- UI Automation, type de contrôle Spinner
- UI Automation, arborescence pour le type de contrôle Spinner
- UI Automation, propriétés du type de contrôle Spinner
- UI Automation, modèles de contrôle pour le type de contrôle Spinner
- UI Automation, événements pour le type de contrôle Spinner
- arborescences, type de contrôle Spinner
- Propriétés, Spinner (type de contrôle)
- modèles de contrôle, Spinner (type de contrôle)
- événements, type de contrôle Spinner
- prise en charge du type de contrôle Spinner
- Spinner (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Spinner
- types de contrôle, modèles de contrôle pour le type de contrôle Spinner
- types de contrôles, prise en charge du compteur
- types de contrôles, Spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1472fe400c189b6e5a1e894e1097395e8521e757
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478535"
---
# <a name="spinner-control-type"></a>Spinner (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Spinner** .

Les contrôles compteur sont utilisés pour effectuer une sélection parmi un domaine d’éléments ou une plage de nombres.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Spinner** . Les exigences d’UI Automation s’appliquent à tous les contrôles Spinner où l’infrastructure ou la plateforme de l’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation qui se rapporte aux contrôles Spinner lorsqu’ils prennent en charge les modèles de contrôle **RangeValue** et **Selection** et décrit ce que peut contenir chaque vue. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).

**Modèle de contrôle RangeValue**




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Edit (0 ou 1)</li><li>Button (2)</li></ul></li></ul> | <ul><li>Spinner</li></ul> | 




 

**Selection (modèle de contrôle)**




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Edit (0 ou 1)</li><li>Button (2)</li><li>Élément de liste (0 ou plusieurs)</li></ul></li></ul> | <ul><li>Spinner<ul><li>ListItem (0 ou plus)</li></ul></li></ul> | 




 

Pour vous assurer que les deux boutons de la sous-arborescence de la vue de contrôle peuvent être distingués par des outils de test automatisés, affectez la valeur **ScrollAmount \_ SmallIncrement** ou [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) à la propriété **AutomationId** , le cas échéant. Pour certaines implémentations, le contrôle d’édition associé peut être un homologue du contrôle Spinner.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Spinner. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur       | Notes                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.  | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.  | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.  | Le point interactif du contrôle compteur donne le focus à la partie d’édition du contrôle.                                                                                                                                                                                                                                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Spinner** | Cette valeur est la même pour toutes les infrastructures.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle compteur doit toujours être du contenu.                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle Spinner doit toujours être un contrôle.                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.  | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété. Un contrôle Spinner prend rarement le focus, mais dans ce cas, le focus doit rester sur le contrôle Spinner lui-même, et non sur les boutons enfants. L’utilisateur doit être en mesure d’effectuer toutes les actions de défilement à l’aide des flèches haut et bas. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.  | Les contrôles compteur ont une étiquette de texte statique.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.  | Chaîne localisée correspondant au type de contrôle **Spinner** . La valeur par défaut est « Spinner » pour en-US ou anglais (États-Unis).                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.  | Le contrôle compteur tire généralement son nom d’une étiquette de texte statique.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Spinner. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                                         | Prise en charge/valeur | Notes                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Dépend       | Les contrôles Spinner qui couvrent une plage numérique peuvent prendre en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) .               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Dépend       | Les contrôles Spinner qui ont une liste d’éléments à sélectionner doivent prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) . |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | FALSE         | Les contrôles compteur sont toujours des conteneurs à sélection unique.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Dépend       | Les contrôles Spinner qui couvrent un ensemble descrete d’options ou de nombres peuvent prendre en charge le modèle de contrôle [value](uiauto-implementingvalue.md) .    |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Spinner. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.        | Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ Sélection \_**](uiauto-event-ids.md) de l’événement de modification de propriété InvalidatedEventId.               | Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                  | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




