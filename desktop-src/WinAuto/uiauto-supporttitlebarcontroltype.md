---
title: TitleBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle TitleBar. Un contrôle de barre de titre représente un titre ou une barre de légende dans une fenêtre.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- UI Automation, prise en charge du type de contrôle TitleBar
- UI Automation, type de contrôle TitleBar
- UI Automation, arborescence pour le type de contrôle TitleBar
- UI Automation, propriétés du type de contrôle TitleBar
- UI Automation, modèles de contrôle pour le type de contrôle TitleBar
- UI Automation, événements pour le type de contrôle TitleBar
- arborescences, type de contrôle TitleBar
- Propriétés, TitleBar (type de contrôle)
- modèles de contrôle, type de contrôle TitleBar
- événements, type de contrôle TitleBar
- prise en charge du type de contrôle TitleBar
- TitleBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle TitleBar
- types de contrôle, modèles de contrôle pour le type de contrôle TitleBar
- types de contrôles, prise en charge de TitleBar
- types de contrôles, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940292"
---
# <a name="titlebar-control-type"></a>TitleBar (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **TitleBar** . Un contrôle de barre de titre représente un titre ou une barre de légende dans une fenêtre.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **TitleBar** . Les exigences d’UI Automation s’appliquent à tous les contrôles de barre de titre dans lesquels l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de barre de titre et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Affichage de contrôle</th>
<th>Affichage de contenu</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>TitleBar
<ul>
<li>Menu (0 ou 1)</li>
<li>Button (0 ou plus)</li>
</ul></li>
</ul></td>
<td>(Non applicable ; le contrôle de barre de titre n’a pas de contenu)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **TitleBar** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | La valeur exposée par cette propriété doit inclure tous les contrôles qu’elle contient.                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Spreadsheet** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE        | Le contrôle de barre de titre n’est jamais inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle de barre de titre est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | FALSE        | Un contrôle de barre de titre n’a jamais le focus clavier.                                                                                                                                                        |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Dépend      | Un contrôle de barre de titre retourne une valeur selon qu’elle est visible à l’écran.                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.   | Un contrôle de barre de titre n’a généralement pas d’étiquette.                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle TitleBar. La valeur par défaut est « barre de titre » pour en-US ou anglais (États-Unis).                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""           | La barre de titre ne comporte pas de contenu ; ses informations textuelles sont exposées par le nom de la fenêtre parente.                                                                                                     |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le type de contrôle **TitleBar** n’est pas requis pour prendre en charge les modèles de contrôle. Ses fonctionnalités sont exposées via le modèle de contrôle [Window](uiauto-implementingwindow.md) sur le type de contrôle [Window](uiauto-supportwindowcontroltype.md) .

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre de titre. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




