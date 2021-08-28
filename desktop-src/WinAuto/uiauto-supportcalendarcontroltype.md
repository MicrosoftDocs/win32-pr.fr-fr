---
title: Calendar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Calendar. Un contrôle Calendar permet à l’utilisateur de déterminer facilement la date et de sélectionner d’autres dates.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- UI Automation, prise en charge du type de contrôle Calendar
- UI Automation, type de contrôle Calendar
- UI Automation, arborescence pour le type de contrôle Calendar
- UI Automation, propriétés du type de contrôle Calendar
- UI Automation, modèles de contrôle pour le type de contrôle Calendar
- UI Automation, événements pour le type de contrôle Calendar
- arborescences, type de contrôle Calendar
- Propriétés, type de contrôle Calendar
- modèles de contrôle, type de contrôle Calendar
- événements, type de contrôle Calendar
- prise en charge du type de contrôle Calendar
- Calendar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Calendar
- types de contrôle, modèles de contrôle pour le type de contrôle Calendar
- types de contrôles, prise en charge du calendrier
- types de contrôles, calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d51271fb2e9526bc293b9c5d36acc0a65b3b639
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482945"
---
# <a name="calendar-control-type"></a>Calendar (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Calendar** . Un contrôle Calendar permet à l’utilisateur de déterminer facilement la date et de sélectionner d’autres dates.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Calendar** . Les exigences d’UI Automation s’appliquent à tous les contrôles Calendar où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de calendrier et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Calendrier<ul><li>DataGrid<ul><li>Header (0 ou 1)<ul><li>HeaderItem (0 ou 7, la quantité dépend du nombre de jours affichés dans les colonnes)</li></ul></li><li>ListItem (la quantité dépend du nombre de jours affichés)</li><li>Button (0 ou 2 ; pour paginer l’affichage du calendrier)</li></ul></li></ul></li></ul> | <ul><li>Calendrier<ul><li>ListItem (la quantité dépend du nombre de jours affichés)</li></ul></li></ul> | 




 

Les contrôles calendar peuvent être représentés sous différentes formes dans l’interface utilisateur. Les seuls contrôles garantis dans l’affichage de contrôle de l’arborescence UI Automation sont les contrôles de grille de données, d’en-tête, d’en-tête et d’élément de liste.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **Calendar** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Calendrier** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle Calendar est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle Calendar est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.   | La valeur de cette propriété doit être l’étiquette du contrôle de document. En général, le titre du document est utilisé.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **Calendar** . La valeur par défaut est « calendrier » pour en-US ou anglais (États-Unis).                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | Le contrôle Calendar obtient généralement son nom à partir de la date actuelle.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Calendar. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                        | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatoire      | Le contrôle Calendar prend toujours en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) , car les jours d’un mois sont des éléments qui peuvent être parcourus de façon spatiale.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dépend       | La plupart des contrôles calendar prennent en charge le retournement de l’affichage par page. Le modèle de contrôle [Scroll](uiauto-implementingscroll.md) est recommandé pour prendre en charge la navigation de pagination.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Dépend       | La plupart des contrôles Calendar conservent un jour, un mois ou une année spécifique en tant que sélection du sous-élément. Certains calendriers peuvent être sélectionnés de façon multiple et ne peuvent être qu’un seul sélectionnable. Le contrôle Calendar avec des sous-éléments sélectionnables doit prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) .                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obligatoire      | Étant donné que le contrôle Calendar a toujours un en-tête dans sa sous-arborescence pour les jours de la semaine, le modèle de contrôle [table](uiauto-implementingtable.md) doit être pris en charge.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | No            | Le modèle de contrôle [value](uiauto-implementingvalue.md) n’est pas nécessaire pour les contrôles Calendar, car l’élément ne peut pas définir la valeur directement sur le contrôle. Si une date spécifique est associée au contrôle, les informations doivent être fournies par le modèle de contrôle [Selection](uiauto-implementingselection.md) . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de calendrier. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Notes                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                      | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.                                                                                     |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.                                                                                   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété MultipleViewCurrentViewPropertyId.             | Si le contrôle prend en charge la propriété [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) du modèle de contrôle [MultipleView](uiauto-implementingmultipleview.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.                                                                                             |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




