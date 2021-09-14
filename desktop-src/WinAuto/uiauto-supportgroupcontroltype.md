---
title: Group (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- UI Automation, prise en charge du type de contrôle de groupe
- UI Automation, type de contrôle de groupe
- UI Automation, arborescence pour le type de contrôle Group
- UI Automation, propriétés du type de contrôle de groupe
- UI Automation, modèles de contrôle pour le type de contrôle Group
- UI Automation, événements pour le type de contrôle Group
- arborescences, type de contrôle de groupe
- Propriétés, groupe de contrôles (type)
- modèles de contrôle, type de contrôle de groupe
- événements, type de contrôle de groupe
- prise en charge du type de contrôle Group
- Group (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Group
- types de contrôles, modèles de contrôle pour le type de contrôle Group
- types de contrôle, prise en charge du groupe
- types de contrôles, groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0cee05f7132a35c8dd3f998ae9af5a89ac2a71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122585"
---
# <a name="group-control-type"></a>Group (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Group** .

Un contrôle de groupe représente un nœud dans une hiérarchie. Le type de contrôle **Group** crée une séparation dans l’arborescence UI Automation de sorte que les éléments regroupés ont une division logique dans l’arborescence UI Automation.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Group** . Les exigences d’UI Automation s’appliquent à tous les contrôles de groupe où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de groupe et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Group<ul><li>0 ou plusieurs contrôles</li></ul></li></ul> | <ul><li>Group<ul><li>0 ou plusieurs contrôles</li></ul></li></ul> | 




 

Les contrôles de groupe incluent généralement la prise en charge d’UI Automation pour les types de contrôle trouvés sous ceux-ci dans la sous-arborescence, y compris les types de contrôle [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)et [DataItem](uiauto-supportdataitemcontroltype.md) . Étant donné qu’un contrôle de groupe est un conteneur générique, tout type de contrôle peut être sous le contrôle de groupe dans l’arborescence.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de groupe. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Groupe**  |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Le contrôle de groupe est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Le contrôle de groupe est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | En général, les contrôles de groupe créent eux-mêmes leurs étiquettes. Dans ce cas, retourne **null**. Si le groupe a une étiquette de texte statique, retournez l’étiquette en tant que valeur de la propriété **LabeledBy** .                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Group** . La valeur par défaut est « Group » pour en-US ou anglais (États-Unis).                                                                     |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le contrôle de groupe tire généralement son nom du texte qui sert d’étiquette au contrôle.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour le type de contrôle **Group** . Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support | Notes                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dépend | Les contrôles de groupe qui peuvent être utilisés pour afficher ou masquer des informations doivent prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de groupe. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. | Si le contrôle prend en charge le modèle de contrôle du modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.                         |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.                       |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.                                 | Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




