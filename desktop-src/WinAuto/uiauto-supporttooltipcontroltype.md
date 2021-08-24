---
title: ToolTip (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ToolTip. Les contrôles ToolTip sont des fenêtres indépendantes qui contiennent du texte.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- UI Automation, prise en charge du type de contrôle ToolTip
- UI Automation, type de contrôle ToolTip
- UI Automation, arborescence pour le type de contrôle ToolTip
- UI Automation, propriétés du type de contrôle ToolTip
- UI Automation, modèles de contrôle pour le type de contrôle ToolTip
- UI Automation, événements pour le type de contrôle ToolTip
- arborescences, type de contrôle ToolTip
- Propriétés, ToolTip (type de contrôle)
- modèles de contrôle, info-bulle (type de contrôle)
- événements, type de contrôle ToolTip
- prise en charge du type de contrôle ToolTip
- ToolTip (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ToolTip
- types de contrôle, modèles de contrôle pour le type de contrôle ToolTip
- types de contrôles, prise en charge d’info-bulle
- types de contrôle, info-bulle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31a20e6d4b61851e57bd2609d58075477b8e62999f5e10e34f02d86e010797a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899289"
---
# <a name="tooltip-control-type"></a>ToolTip (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **ToolTip** . Les contrôles ToolTip sont des fenêtres indépendantes qui contiennent du texte.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **ToolTip** . Les exigences d’UI Automation s’appliquent à tous les contrôles ToolTip où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles ToolTip et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Info-bulle
<ul>
<li>Text (0 ou plus)</li>
<li>Image (0 ou plus)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Info-bulle</li>
</ul></td>
</tr>
</tbody>
</table>



 

Les contrôles ToolTip apparaissent uniquement dans l’affichage de contenu de l’arborescence UI Automation s’ils peuvent recevoir le focus clavier. Sinon, toutes les informations de l’info-bulle sont disponibles à partir de la propriété [**IUIAutomationElement :: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (ou [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) sur l’élément auquel l’info-bulle fait référence.

Les info-bulles doivent apparaître sous le contrôle auquel leurs informations font référence. Les clients doivent écouter le [**\_ ToolTipOpenedEventId UIA**](uiauto-event-ids.md) pour s’assurer qu’ils obtiennent régulièrement des informations contenues dans les info-bulles.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **ToolTip** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur       | Notes                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.  | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.  | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.  | Le point cliquable doit être la partie de l’info-bulle qui ferme le contrôle. Certaines info-bulles n’ont pas cette possibilité et n’ont pas de point cliquable.                                                                                                                                                                                                  |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Dépend     | Si le contrôle ToolTip peut recevoir le focus clavier, il doit apparaître dans l’affichage de contenu de l’arborescence. S’il s’agit d’un texte uniquement, il est disponible en tant que propriété [**IUIAutomationElement :: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (ou [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) à partir du contrôle qui l’a déclenché. |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | Vrai        | Le contrôle ToolTip est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.  | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Les contrôles ToolTip sont toujours étiquetés automatiquement par leur contenu.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.  | Chaîne localisée correspondant au type de contrôle ToolTip. La valeur par défaut est « ToolTip » pour « fr-fr » ou « anglais » (États-Unis).                                                                                                                                                                                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.  | Le nom du contrôle ToolTip est le texte affiché dans l’info-bulle.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles ToolTip. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                   | Support | Notes                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Dépend | Pour une meilleure accessibilité, un contrôle d’info-bulle peut prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , bien qu’il ne soit pas obligatoire. Le modèle de contrôle Text est utile quand le texte possède un style complexe et des attributs (par exemple, couleur, gras et italique). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Dépend | Les info-bulles qui peuvent être fermées en cliquant sur un élément d’interface utilisateur doivent prendre en charge le modèle de contrôle de [fenêtre](uiauto-implementingwindow.md) pour pouvoir se fermer automatiquement.                                                                                                                 |



 

## <a name="required-events"></a>Événements obligatoires

Les contrôles ToolTip doivent déclencher l’événement [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) lorsqu’ils s’affichent à l’écran. L’événement inclut une référence à l’élément UI Automation de l’info-bulle elle-même.

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles ToolTip. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                            | Notes                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.          |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                          | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                      | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                                    |                                                                                                                            |
| [**\_TextChangedEventId de texte UIA \_**](uiauto-event-ids.md)                                                          | Si le contrôle prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**\_Fenêtre UIA \_ WindowClosedEventId**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [Window](uiauto-implementingwindow.md) , il doit prendre en charge cet événement.           |
| [**\_Fenêtre UIA \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [Window](uiauto-implementingwindow.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété WindowWindowVisualStatePropertyId. | Si le contrôle prend en charge le modèle de contrôle [Window](uiauto-implementingwindow.md) , il doit prendre en charge cet événement.           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




