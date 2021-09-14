---
title: Table (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- UI Automation, prise en charge du type de contrôle table
- UI Automation, type de contrôle table
- UI Automation, arborescence pour le type de contrôle table
- UI Automation, propriétés du type de contrôle table
- UI Automation, modèles de contrôle pour le type de contrôle table
- UI Automation, événements pour le type de contrôle table
- arborescences, type de contrôle table
- Propriétés, table (type de contrôle)
- modèles de contrôle, table (type de contrôle)
- événements, type de contrôle table
- prise en charge du type de contrôle table
- Table (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle table
- types de contrôle, modèles de contrôle pour le type de contrôle table
- types de contrôles, prise en charge de table
- types de contrôles, table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0badb06cfc449140162663625f3fa7282f9c1589
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122566"
---
# <a name="table-control-type"></a>Table (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **table** .

Les contrôles de table contiennent des lignes et des colonnes de texte et, éventuellement, des en-têtes de ligne et des en-têtes de colonnes.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **table** . Les exigences d’UI Automation s’appliquent à tous les contrôles de table où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de table, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Table de charge de travail<ul><li>Text (0 ou 1)</li><li>En-tête (0 ou plus)</li><li>Plusieurs contrôles (0 ou plus)</li></ul></li></ul> | <ul><li>Table de charge de travail<ul><li>Texte (1 ou plus)</li><li>Plusieurs contrôles (0 ou plus)</li></ul></li></ul> | 




 

Si un contrôle de table possède des en-têtes de lignes ou de colonnes, ceux-ci doivent être exposés dans la vue de contrôle de l’arborescence UI Automation. L’affichage du contenu n’a pas besoin d’exposer ces informations, car elles sont accessibles à l’aide de [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de table. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Table**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Consultez les remarques. | Si la table est annotée par un autre élément d’interface utilisateur (par exemple, un élément de texte contenant la description de la table), la propriété DescribedBy doit exposer une référence à l’élément Automation du contrôle de texte.           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | Des détails supplémentaires sur l’objectif de la table doivent être exposés via cette propriété si elle n’est pas suffisamment expliquée par la propriété [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) .      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle de table doit toujours apparaître dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle de table doit toujours apparaître dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à l’élément Automation du contrôle.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **table** . La valeur par défaut est « table » pour en-US ou anglais (États-Unis).                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le contrôle de table obtient généralement la valeur de son nom à partir d’une étiquette de texte statique. S’il n’y a pas d’étiquette de texte statique, l’élément doit affecter une propriété Name qui doit toujours être disponible pour expliquer l’objectif de la table. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de table. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                         | Support                     | Notes                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obligatoire                    | Étant donné que le contrôle table contient des éléments présentés dans une grille, il prend toujours en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) .                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Obligatoire avec les objets enfants | Les objets internes d’une table doivent prendre en charge les modèles de contrôle [GridItem](uiauto-implementinggriditem.md) et [TableItem](uiauto-implementingtableitem.md) . La table elle-même n’a pas besoin de prendre en charge le modèle de contrôle GridItem ou TableItem, sauf si la table fait partie d’une autre table.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obligatoire                    | Le contrôle de table peut toujours avoir des en-têtes associés au contenu.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Obligatoire avec les objets enfants | Les objets internes d’une table doivent prendre en charge les modèles de contrôle [GridItem](uiauto-implementinggriditem.md) et [TableItem](uiauto-implementingtableitem.md) . La table elle-même n’a pas besoin de prendre en charge les modèles de contrôle GridItem et TableItem, à moins que la table fasse partie d’une autre table. |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de table. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




