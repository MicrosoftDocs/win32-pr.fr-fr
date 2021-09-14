---
title: ProgressBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ProgressBar.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- UI Automation, prise en charge du type de contrôle ProgressBar
- UI Automation, type de contrôle ProgressBar
- UI Automation, arborescence pour le type de contrôle ProgressBar
- UI Automation, propriétés du type de contrôle ProgressBar
- UI Automation, modèles de contrôle pour le type de contrôle ProgressBar
- UI Automation, événements pour le type de contrôle ProgressBar
- arborescences, type de contrôle ProgressBar
- Propriétés, ProgressBar (type de contrôle)
- modèles de contrôle, ProgressBar (type de contrôle)
- événements, type de contrôle ProgressBar
- prise en charge du type de contrôle ProgressBar
- ProgressBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ProgressBar
- types de contrôle, modèles de contrôle pour le type de contrôle ProgressBar
- types de contrôles, prise en charge de ProgressBar
- types de contrôles, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 5dc5dd22abcaca70ae9ce86717db6055642a21ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192631"
---
# <a name="progressbar-control-type"></a>ProgressBar (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **ProgressBar** .

Les contrôles de barre de progression indiquent la progression d’une opération de longue durée. Le contrôle se compose d’un rectangle qui se remplit progressivement à l’aide de la couleur de mise en surbrillance système pendant la progression d’une opération.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **ProgressBar** . Les exigences d’UI Automation s’appliquent à tous les contrôles de barre de progression où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

- [Structure d’arborescence classique](#typical-tree-structure)
- [Propriétés pertinentes](#relevant-properties)
- [Modèles de contrôle requis](#required-control-patterns)
- [Événements obligatoires](#required-events)
- [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de barre de progression et décrit ce que peut contenir chaque vue. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).


| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>ProgressBar</li></ul> | <ul><li>ProgressBar</li></ul> | 


Les contrôles de barre de progression n’ont pas d’enfants dans l’affichage de contrôle ou de contenu de l’arborescence UI Automation.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les barres de progression. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).

| Propriété UI Automation                                                                                              | Valeur           | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.      | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.      | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.      | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | Le contrôle de barre de progression est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | Le contrôle de barre de progression est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.      | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.      | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.      | Chaîne localisée correspondant au type de contrôle **ProgressBar** . La valeur par défaut est « barre de progression » pour en-US ou anglais (États-Unis).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.      | Le contrôle de barre de progression tire généralement son nom d’une étiquette de texte statique. En l’absence d’étiquette de texte statique, un développeur d’applications doit exposer une valeur pour la propriété Name.                  |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de barre de progression. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                              | Prise en charge/valeur | Notes                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Dépend       | Les contrôles de barre de progression qui acceptent une plage numérique doivent implémenter le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) .        |
| [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Dépend           | La valeur de cette propriété est la valeur minimale pour laquelle le contrôle peut être défini. Cette valeur doit être inférieure à la valeur [**maximale**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum).                                                      |
| [**Maximale**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Dépend         | La valeur de cette propriété est la valeur maximale pour laquelle le contrôle peut être défini. Cette valeur doit être supérieure à la valeur [**minimale**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum).                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Cette propriété n’est pas obligatoire, car les contrôles de barre de progression sont en lecture seule.                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Cette propriété n’est pas obligatoire, car les contrôles de barre de progression sont en lecture seule.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Dépend       | Les contrôles de barre de progression qui donnent une indication textuelle de la progression doivent implémenter le modèle de contrôle [value](uiauto-implementingvalue.md) . |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | La valeur de cette propriété est toujours **true**.                                                                                            |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Consultez les remarques.    | Cette propriété expose la progression textuelle d’un contrôle de barre de progression.                                                                          |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des barres de progression. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.        | Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                  | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




