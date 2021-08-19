---
title: RadioButton (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- UI Automation, prise en charge du type de contrôle RadioButton
- UI Automation, type de contrôle RadioButton
- UI Automation, arborescence pour le type de contrôle RadioButton
- UI Automation, propriétés du type de contrôle RadioButton
- UI Automation, modèles de contrôle pour le type de contrôle RadioButton
- UI Automation, événements pour le type de contrôle RadioButton
- arborescences, type de contrôle RadioButton
- Propriétés, RadioButton (type de contrôle)
- modèles de contrôle, RadioButton (type de contrôle)
- événements, type de contrôle RadioButton
- prise en charge du type de contrôle RadioButton
- RadioButton (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle RadioButton
- types de contrôle, modèles de contrôle pour le type de contrôle RadioButton
- types de contrôles, prise en charge de RadioButton
- types de contrôles, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358a71f74b40d8465c910f8afe258183c8ea4d5c322fb70e6b6ea946ef7d44ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825480"
---
# <a name="radiobutton-control-type"></a>RadioButton (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **RadioButton** .

Une case d’option se compose d’un bouton rond et d’un texte défini par l’application (étiquette), d’une icône ou d’une image bitmap qui indique un choix que l’utilisateur peut faire en sélectionnant le bouton. Une application utilise généralement des cases d’option dans une zone de groupe pour permettre à l’utilisateur de choisir parmi un ensemble d’options connexes mais s’excluant mutuellement. Par exemple, l’application peut présenter un groupe de cases d’option parmi lesquelles l’utilisateur peut sélectionner une préférence de format pour le texte sélectionné dans la zone cliente. L’utilisateur peut sélectionner un format aligné à gauche, aligné à droite ou centré en cochant la case d’option correspondante. En règle générale, l’utilisateur peut sélectionner une seule option à la fois parmi un ensemble de cases d’option.

> [!Note]  
> Une autre généralisation de contrôle pour les boutons dans lesquels une seule partie d’un groupe peut être sélectionnée est le contenu d’un bouton bascule. Certaines infrastructures d’interface utilisateur considèrent qu’une case d’option est un bouton bascule spécialisé.

 

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **RadioButton** . Les spécifications d’UI Automation s’appliquent à tous les contrôles de bouton où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de case d’option et décrit ce que peut contenir chaque vue. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>RadioButton</li>
</ul></td>
<td><ul>
<li>RadioButton</li>
</ul></td>
</tr>
</tbody>
</table>



 

Aucun enfant ne figure dans la vue de contrôle ni dans la vue de contenu.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **RadioButton** (tels que les contrôles Button). Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur           | Notes                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.      | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.      | Rectangle externe qui contient l’ensemble du contrôle.                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.      | Le point cliquable doit être un point qui, lorsque vous cliquez dessus, sélectionne la case d’option.                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Le contrôle de case d’option est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Le contrôle de case d’option est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.      | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Les contrôles de cases d’option sont étiquetés automatiquement par leur contenu.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.      | Chaîne localisée correspondant au type de contrôle **RadioButton** . La valeur par défaut est « case d’option » pour en-US ou anglais (États-Unis). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.      | Le nom du contrôle de case d’option est le texte qui s’affiche en regard du bouton qui maintient l’état de sélection.                      |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de case d’option. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                                               | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Obligatoire      | Tous les contrôles de case d’option doivent prendre en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) pour pouvoir être sélectionnés.                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Consultez les remarques.    | La propriété [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) doit toujours être terminée afin qu’un client UI Automation puisse déterminer quelles autres cases d’option dans un contexte spécifique sont liées les unes aux autres. Pour la version Microsoft Win32 de la case d’option, cette propriété n’est pas prise en charge, car il n’est pas possible d’obtenir ces informations à partir de cette infrastructure héritée. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Jamais         | La case d’option ne peut pas passer d’un état à un autre une fois qu’elle a été définie. Le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) ne doit jamais être pris en charge sur une case d’option.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de bouton. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                     | Notes                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                   | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.               | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.     |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Remarques

Une case d’option représente une option sélectionnable unique parmi un groupe de cases d’option homologues. Dans l’idéal, les cases d’option doivent avoir un élément de regroupement qui clarifie les limites des cases d’option homologues. Toutefois, il arrive souvent que la limite soit impliquée par la structure de l’élément d’interface utilisateur. Par exemple, un menu peut contenir un ensemble de cases d’option consécutives à la place d’éléments de menu, ou un ensemble de cases d’option qui se produisent après une étiquette de groupe, mais avant un élément actionnable tel que Button.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




