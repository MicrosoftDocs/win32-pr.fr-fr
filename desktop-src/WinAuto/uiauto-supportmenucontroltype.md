---
title: Menu (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- UI Automation, prise en charge du type de contrôle Menu
- UI Automation, type de contrôle Menu
- UI Automation, arborescence pour le type de contrôle Menu
- UI Automation, propriétés du type de contrôle Menu
- UI Automation, modèles de contrôle pour le type de contrôle Menu
- UI Automation, événements pour le type de contrôle Menu
- arborescences, type de contrôle Menu
- Propriétés, type de contrôle Menu
- modèles de contrôle, type de contrôle Menu
- événements, type de contrôle Menu
- prise en charge du type de contrôle Menu
- Menu (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Menu
- types de contrôles, modèles de contrôle pour le type de contrôle Menu
- types de contrôles, prise en charge du menu
- types de contrôles, menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029102"
---
# <a name="menu-control-type"></a>Menu (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **menu** .

Un contrôle menu permet une organisation hiérarchique des éléments associés à des commandes et des gestionnaires d’événements. Dans une application Microsoft Windows classique, une barre de menus contient plusieurs boutons de menu (tels que **fichier**, **Edition** et **fenêtre**) et chaque bouton de menu affiche un menu. Un menu contient un groupe d’éléments de menu (tels que **Nouveau**, **Ouvrir** et **Fermer**), qui peuvent être développés pour afficher des éléments de menu supplémentaires ou pour exécuter une action spécifique quand vous cliquez dessus.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **menu** . Les exigences d’UI Automation s’appliquent à tous les contrôles de menu où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de menu et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Menu
<ul>
<li>MenuItem (1 ou plusieurs)</li>
</ul>
<ul>
<li>Autres contrôles (0 ou plusieurs)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Menu
<ul>
<li>MenuItem (1 ou plusieurs)</li>
</ul>
<ul>
<li>Autres contrôles (0 ou plusieurs)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Les contrôles de menu s’affichent toujours dans l’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation. Les contrôles de menu doivent apparaître sous le contrôle auquel leurs informations font référence. Les clients UI Automation peuvent écouter [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) pour s’assurer qu’ils obtiennent régulièrement les informations véhiculées par les contrôles menu. Les contrôles de menu contextuel constituent un cas particulier. Ils peuvent apparaître en tant qu’enfants du bureau ou d’une fenêtre d’application de niveau supérieur.

Un contrôle de menu peut contenir d’autres contrôles, tels que des contrôles d’édition et des zones de liste déroulante, au sein de sa structure. Ces contrôles supplémentaires correspondent aux « autres contrôles » figurant dans le tableau précédent dans les affichages de contrôle et de contenu.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **menu** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                      | Valeur      | Notes                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **Menu**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | Le contrôle Menu est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | Le contrôle Menu est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULL       | Aucune étiquette n’est censée accompagner un contrôle menu standard.                                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | Le contrôle de menu ne requiert pas la définition d’une propriété **Name** ou peut avoir le même nom que le contrôle associé, par exemple un élément de menu qui a ouvert le sous-menu. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Il n’existe aucun modèle de contrôle obligatoire pour le type de contrôle Menu.

## <a name="required-events"></a>Événements obligatoires

Les contrôles menu doivent déclencher l’événement [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) lorsqu’ils s’affichent à l’écran. L’événement **UIA \_ MenuOpenedEventId** inclut le texte du contrôle. L’événement [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) doit être déclenché quand un menu disparaît de l’écran.

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de menu. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




