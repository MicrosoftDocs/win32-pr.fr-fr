---
title: TreeItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle TreeItem.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- UI Automation, prise en charge du type de contrôle TreeItem
- UI Automation, type de contrôle TreeItem
- UI Automation, arborescence pour le type de contrôle TreeItem
- UI Automation, propriétés pour le type de contrôle TreeItem
- UI Automation, modèles de contrôle pour le type de contrôle TreeItem
- UI Automation, événements pour le type de contrôle TreeItem
- arborescences, type de contrôle TreeItem
- Propriétés, TreeItem (type de contrôle)
- modèles de contrôle, type de contrôle TreeItem
- événements, TreeItem (type de contrôle)
- prise en charge du type de contrôle TreeItem
- TreeItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle TreeItem
- types de contrôles, modèles de contrôle pour le type de contrôle TreeItem
- types de contrôles, prise en charge de TreeItem
- types de contrôles, TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c837428a0aeef900779cfccf0a28b46aa276369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106527138"
---
# <a name="treeitem-control-type"></a>TreeItem (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **TreeItem** .

Le type de contrôle **TreeItem** représente un nœud dans un conteneur d’arborescence. Chaque nœud peut contenir d’autres nœuds, appelés nœuds enfants. Vous pouvez afficher les nœuds parents, ou nœuds qui contiennent des nœuds enfants, sous forme développée ou réduite.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **TreeItem** . Les spécifications d’UI Automation s’appliquent à tous les contrôles d’élément d’arborescence où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’élément d’arborescence et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>TreeItem
<ul>
<li>CheckBox (0 ou 1)</li>
<li>Image (0 ou 1)</li>
<li>Button (0 ou 1)</li>
<li>TreeItem (0 ou plus)</li>
</ul></li>
</ul></td>
<td><ul>
<li>TreeItem
<ul>
<li>TreeItem (0 ou plus)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Les contrôles d’élément d’arborescence peuvent avoir zéro ou plusieurs enfants d’élément d’arborescence dans l’affichage de contenu de l’arborescence UI Automation. Si le contrôle d’élément d’arborescence a des fonctionnalités au-delà de ce qui est exposé dans les modèles de contrôle répertoriés ci-dessous, le contrôle doit être basé sur le type de contrôle [DataItem](uiauto-supportdataitemcontroltype.md) .

Les éléments d’arborescence réduits n’apparaissent pas dans l’affichage de contrôle ou l’affichage du contenu tant qu’ils ne sont pas développés et visibles (ou peuvent être défilés dans l’affichage).

L’affichage de contrôle peut contenir des détails supplémentaires pour un contrôle, notamment une image ou un bouton associé. Par exemple, un élément en mode Plan peut contenir une image, ainsi qu’un bouton pour développer ou réduire le plan. Ces objets de détail n’apparaissent pas dans l’affichage de contenu, car les informations sont déjà représentées par l’élément d’arborescence parent.

Les éléments d’arborescence qui défilent à l’écran apparaissent dans les affichages de contrôle et de contenu de l’arborescence UI Automation et doivent avoir la propriété [**IUIAutomationElement :: CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (ou [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) définie sur **true**.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **TreeItem** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Cette propriété doit retourner un emplacement qui entraîne le changement d’état de sélection de l’élément d’arborescence ou le focus.                                                                                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TreeItem** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Le contrôle d’élément d’arborescence est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                       |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Le contrôle d’élément d’arborescence est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                       |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                     |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consultez les remarques.   | Cette propriété indique si un contrôle d’élément d’arborescence défile à partir de l’écran.                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consultez les remarques.   | Si le contrôle contient l’État mis à jour dynamiquement, cette propriété doit être prise en charge afin qu’une technologie d’assistance puisse recevoir des mises à jour lorsque l’état de l’élément change. |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques.   | Si le contrôle d’élément d’arborescence utilise une icône visuelle pour indiquer que est un type particulier d’élément, cette propriété doit être prise en charge et doit indiquer le type d’élément.                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | Les contrôles d’élément d’arborescence créent eux-mêmes leurs étiquettes.                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle TreeItem. La valeur par défaut est « élément d’arborescence » pour en-US ou anglais (États-Unis).                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | Cette propriété expose le texte affiché pour chaque contrôle d’élément d’arborescence.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’élément d’arborescence. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                                                  | Prise en charge/valeur                     | Notes                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Obligatoire                          | Tous les éléments d’arborescence doivent prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , car tous les éléments peuvent être développés ou réduits.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Nœud développé, réduit ou terminal | Les éléments d’arborescence sont des nœuds terminaux quand ils ne sont pas développés ou réduits.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Dépend                           | Implémentez le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) si l’élément d’arborescence peut exécuter une commande.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Dépend                           | Implémentez le modèle de contrôle [ScrollItem](uiauto-implementingscrollitem.md) si le conteneur d’arborescence prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Dépend                           | Implémentez le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) s’il est possible d’avoir une sélection active qui est maintenue quand l’utilisateur retourne au conteneur d’arborescence. |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Obligatoire                          | Cette propriété expose le même conteneur pour tous les éléments du conteneur.                                                                                                                      |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’élément d’arborescence. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                                |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.               |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété ItemStatusPropertyId.                                            | Si le contrôle prend en charge la propriété [**ItemStatus**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.      |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété MultipleViewCurrentViewPropertyId.                     | Si le contrôle prend en charge le modèle de contrôle [MultipleView](uiauto-implementingmultipleview.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                                                        |                                                                                                                                |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.                                 | Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.               |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                                               | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.                 |



 

## <a name="remarks"></a>Notes

Si un élément d’arborescence contient des sous-éléments autres que des nœuds de plan enfants, le fournisseur doit gérer les informations sur les objets enfants avec soin et clairement. Dans UI Automation, l’arborescence est gérée par la hiérarchie d’arborescence elle-même. En ayant un ou plusieurs enfants non-nœud-plan, les différences entre eux et les nœuds de contour enfants réels deviennent gravement ambiguës.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




