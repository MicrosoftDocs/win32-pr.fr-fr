---
title: List (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle List.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- UI Automation, prise en charge du type de contrôle List
- UI Automation, type de contrôle List
- UI Automation, arborescence pour le type de contrôle List
- UI Automation, propriétés pour le type de contrôle List
- UI Automation, modèles de contrôle pour le type de contrôle List
- UI Automation, événements pour le type de contrôle List
- arborescences, type de contrôle List
- Propriétés, List (type de contrôle)
- modèles de contrôle, List (type de contrôle)
- événements, List (type de contrôle)
- prise en charge du type de contrôle List
- List (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle List
- types de contrôle, modèles de contrôle pour le type de contrôle List
- types de contrôles, prise en charge de List
- types de contrôles, liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac6ecb2e0fc7092507816cf9bbea4f450121c1ec8a2e6a57db3d377506af9d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570459"
---
# <a name="list-control-type"></a>List (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **List** .

Le type de contrôle **List** offre un moyen d’organiser un groupe plat ou des groupes d’éléments et permet à un utilisateur de sélectionner un ou plusieurs de ces éléments. Le type de contrôle **List** a une restriction libre sur les types d’éléments enfants qu’il peut contenir. Les fournisseurs UI Automation peuvent de ce fait prendre en charge un élément bien connu pour les conteneurs de sélection.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **List** . Les exigences d’UI Automation s’appliquent à tous les contrôles de liste où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle et propriétés obligatoires](#required-control-patterns-and-properties)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de liste, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<td>Contient les éléments qui correspondent aux contrôles.</td>
<td>Supprime les informations redondantes de l’arborescence pour permettre aux technologies d’assistance d’utiliser le plus petit ensemble d’informations qui est significatif pour l’utilisateur final.</td>
</tr>
<tr class="even">
<td><ul>
<li>List
<ul>
<li>DataItem (0 ou plus)</li>
<li>ListItem (0 ou plus)</li>
<li>Group (0 ou plus)</li>
<li>ScrollBar (0, 1 ou 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>List
<ul>
<li>DataItem (0 ou plus)</li>
<li>ListItem (0 ou plus)</li>
<li>Group (0 ou plus)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

L’affichage de contrôle pour un contrôle qui implémente le type de contrôle List (par exemple, un contrôle list) se compose des éléments suivants :

-   Zéro ou plusieurs éléments dans le contrôle List (les éléments peuvent être basés sur les types de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Zéro ou plusieurs contrôles group dans un contrôle list
-   Zéro, un ou deux contrôles scroll bar

L’affichage de contenu pour un contrôle qui implémente le type de contrôle List (par exemple, un contrôle list) se compose des éléments suivants :

-   Zéro ou plusieurs éléments dans le contrôle List (les éléments peuvent être basés sur les types de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Zéro ou plusieurs groupes dans le contrôle list

Un contrôle list ne doit pas contenir d’éléments ayant une relation hiérarchique autre que le fait d’être regroupés. Si les éléments ont des enfants dans l’arborescence UI Automation, le conteneur List doit être basé sur le type de contrôle [Tree](uiauto-supporttreecontroltype.md) .

Les éléments sélectionnables dans le contrôle de liste sont disponibles dans les descendants de l’arborescence UI Automation du contrôle de liste. Tous les éléments du contrôle list doivent appartenir au même groupe de sélection. Les éléments sélectionnables dans la liste doivent être exposés en tant que types de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) (et non [DataItem](uiauto-supportdataitemcontroltype.md)).

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **List** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Si le contrôle de liste a un point interactif (point sur lequel vous pouvez cliquer pour que la liste prenne le focus), ce point doit être exposé via cette propriété. Si la valeur de la propriété [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md) est **true**, la tentative de récupération de cette propriété entraîne l’erreur [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) .                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Liste**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | Le texte d’aide sur les contrôles list doit expliquer la raison pour laquelle l’utilisateur est invité à faire un sélection dans une liste d’options. Par exemple, « la sélection d’un élément dans cette liste a pour effet de définir la résolution d’affichage de votre moniteur ».                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Le contrôle de liste est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Le contrôle de liste est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **List** . La valeur par défaut est « list » pour « fr-fr » ou « anglais » (États-Unis).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | La valeur de la propriété **Name** d’un contrôle List doit communiquer la catégorie d’options dans laquelle l’utilisateur est invité à effectuer une sélection. Cette propriété tire généralement son nom d’une étiquette de texte statique. S’il n’y a pas d’étiquette de texte statique, le développeur d’applications doit exposer une valeur pour la propriété **Name** .<br/> Le seul cas où cette propriété n’est pas obligatoire pour les contrôles list, c’est lorsque le contrôle est utilisé dans la sous-arborescence d’un autre contrôle.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Modèles de contrôle et propriétés obligatoires

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de liste. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                                             | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Dépend       | Implémentez le modèle de contrôle [Grid](uiauto-implementinggrid.md) lorsque la navigation dans la grille doit être disponible pour chaque élément.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Dépend       | Implémentez le modèle de contrôle [MultipleView](uiauto-implementingmultipleview.md) si le contrôle peut prendre en charge plusieurs vues des éléments dans le conteneur.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Dépend       | Implémentez le modèle de contrôle [Scroll](uiauto-implementingscroll.md) si les éléments du conteneur peuvent faire l’objet d’un défilement.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Dépend       | Si un contrôle prend en charge le type de contrôle List qui prend en charge la sélection, le contrôle doit implémenter le modèle de contrôle [Selection](uiauto-implementingselection.md) lorsqu’un état de sélection est maintenu entre les éléments contenus dans le contrôle. Si les éléments du contrôle ne peuvent pas être sélectionnés, le type de contrôle [Group](uiauto-supportgroupcontroltype.md) peut être utilisé. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Dépend       | Les contrôles List peuvent être des conteneurs à sélection unique ou multiple.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Dépend       | Avec les contrôles List, la sélection d’un élément n’est pas toujours obligatoire.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Jamais         | Le modèle de contrôle [table](uiauto-implementingtable.md) n’est jamais pris en charge pour le type de contrôle **List** . Si le contrôle doit prendre en charge ce modèle de contrôle, le contrôle doit être basé sur le type de contrôle [DataGrid](uiauto-supportdatagridcontroltype.md) .                                                                                                             |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de liste. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Notes                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                      | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     | Si la disposition des éléments enfants peut être modifiée, le contrôle doit prendre en charge cet événement.                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété MultipleViewCurrentViewPropertyId.             | Si le contrôle prend en charge le modèle de contrôle [MultipleView](uiauto-implementingmultipleview.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.             |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)                                                            | Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





