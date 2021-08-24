---
title: Header (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- UI Automation, prise en charge du type de contrôle header
- UI Automation, type de contrôle header
- UI Automation, arborescence pour le type de contrôle header
- UI Automation, propriétés du type de contrôle header
- UI Automation, modèles de contrôle pour le type de contrôle header
- UI Automation, événements pour le type de contrôle header
- arborescences, type de contrôle header
- Propriétés, type de contrôle header
- modèles de contrôle, type de contrôle header
- événements, type de contrôle header
- prise en charge du type de contrôle header
- Header (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle header
- types de contrôle, modèles de contrôle pour le type de contrôle header
- types de contrôles, prise en charge de l’en-tête
- types de contrôles, en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a0d7185fa3c2b2dc1dc7593afd106008890bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482508"
---
# <a name="header-control-type"></a>Header (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **header** .

Le contrôle header fournit un conteneur visuel pour les étiquettes des lignes ou colonnes d’informations.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **header** . Les exigences d’UI Automation s’appliquent à tous les contrôles Header où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles Header et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>En-tête<ul><li>HeaderItem (1 ou plus)</li></ul></li></ul> | (Non applicable) | 




 

Les contrôles Header ont toujours un ou plusieurs enfants dans l’affichage de contrôle de l’arborescence UI Automation.

Les contrôles Header n’ont aucun enfant dans l’affichage de contenu de l’arborescence UI Automation.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Header. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur                                                            | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.                                                       | La valeur de cette propriété doit être unique pour tous les contrôles d’une application.                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.                                                       | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.                                                       | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **En-tête**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE                                                            | Le contrôle header n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE                                                             | Le contrôle header est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.                                                       | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL                                                             | Les contrôles header n’ont pas d’étiquette statique.                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.                                                       | La valeur par défaut est « Header » pour en-US ou anglais (États-Unis).                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.                                                       | Le contrôle header a besoin d’un nom s’il existe plusieurs en-têtes de lignes ou plusieurs en-têtes de colonnes. Cela identifie les informations présentes dans l’en-tête.                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **OrientationType \_** **\_ Vertical** ou horizontal OrientationType | La valeur de cette propriété expose la position du contrôle header, qu’il s’agisse d’un en-tête de ligne (**OrientationType \_ horizontal**) ou d’un en-tête de colonne (**OrientationType \_ vertical**).                 |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour les contrôles Header. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                         | Support | Notes                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dépend | Implémentez le modèle de contrôle [Transform](uiauto-implementingtransform.md) si le contrôle header peut être redimensionné. |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’en-tête. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




