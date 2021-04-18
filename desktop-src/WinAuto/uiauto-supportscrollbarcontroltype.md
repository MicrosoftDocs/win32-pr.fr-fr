---
title: ScrollBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ScrollBar.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- UI Automation, prise en charge du type de contrôle ScrollBar
- UI Automation, type de contrôle ScrollBar
- UI Automation, arborescence pour le type de contrôle ScrollBar
- UI Automation, propriétés du type de contrôle ScrollBar
- UI Automation, modèles de contrôle pour le type de contrôle ScrollBar
- UI Automation, événements pour le type de contrôle ScrollBar
- arborescences, type de contrôle ScrollBar
- Propriétés, ScrollBar (type de contrôle)
- modèles de contrôle, type de contrôle ScrollBar
- événements, type de contrôle ScrollBar
- prise en charge du type de contrôle ScrollBar
- ScrollBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ScrollBar
- types de contrôle, modèles de contrôle pour le type de contrôle ScrollBar
- types de contrôles, prise en charge de ScrollBar
- types de contrôles, ScrollBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2168401c313dd9139f44ba615de945802b307d64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509206"
---
# <a name="scrollbar-control-type"></a>ScrollBar (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **ScrollBar** .

Les contrôles de barre de défilement permettent à un utilisateur de faire défiler le contenu d’une fenêtre ou d’un conteneur d’élément. Le contrôle se compose d’un ensemble de boutons et d’un contrôle Thumb.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **ScrollBar** . Les exigences d’UI Automation s’appliquent à tous les contrôles de barre de défilement où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de barre de défilement et décrit ce que peut contenir chaque vue. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>ScrollBar
<ul>
<li>Button (0, 2 ou 4)</li>
<li>Thumb (0 ou 1)</li>
</ul></li>
</ul></td>
<td>Non applicable. (Le contrôle de barre de défilement n’a pas de contenu.)</td>
</tr>
</tbody>
</table>



 

Le contrôle de barre de défilement peut avoir entre zéro et cinq enfants. Étant donné que la sous-arborescence a plusieurs contrôles bouton, l’élément doit définir une valeur [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md) spécifique à chaque élément afin de les rendre détectables pour les outils de test automatisés.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de barre de défilement. Notez qu’un contrôle de barre de défilement n’a jamais de contenu ; ses fonctionnalités sont exposées via le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , qui est pris en charge sur le conteneur faisant l’objet d’un défilement.

Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur         | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.    | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.    | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | Le contrôle de barre de défilement n’a pas de points interactifs.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ScrollBar** | Cette valeur est la même pour toutes les infrastructures. Les barres de défilement qui fonctionnent en tant que curseurs doivent utiliser le type de contrôle [Slider](uiauto-supportslidercontroltype.md) .                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | Le contrôle de barre de défilement n’est jamais un élément de contenu. Si la barre de défilement est un contrôle autonome, elle doit respecter le type de contrôle [Slider](uiauto-supportslidercontroltype.md) et retourner [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) pour la propriété [**IUIAutomationElement :: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (ou [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)). |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Le contrôle de barre de défilement est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.    | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété. Un contrôle de barre de défilement prend rarement le focus, mais dans ce cas, le focus doit rester sur le contrôle de barre de défilement lui-même, et non sur les boutons enfants ou le curseur de défilement. L’utilisateur doit être en mesure d’effectuer toutes les actions de défilement à l’aide des touches haut et bas (ou flèche droite et gauche), ou des touches PG. suiv et PG. suiv.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Les barres de défilement n’ont pas d’étiquettes.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.    | Chaîne localisée correspondant au type de contrôle **ScrollBar** . La valeur par défaut est « barre de défilement » pour en-US ou anglais (États-Unis).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL          | Le contrôle de barre de défilement n’a pas d’éléments de contenu et la propriété [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) ne doit pas être définie.                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Consultez les remarques.    | Le contrôle de barre de défilement doit toujours exposer son orientation horizontale ou verticale.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de barre de défilement. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Quand une barre de défilement est utilisée comme contrôle uniquement pour la manipulation de la souris, elle ne prend pas en charge les modèles de contrôle. S’il est utilisé comme un contrôle Slider dans une application, le type de contrôle [Slider](uiauto-supportslidercontroltype.md) doit lui être attribué.

 



| Modèle de contrôle                                           | Support | Notes                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Dépend | Le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) ne doit être pris en charge que si le modèle de contrôle [Scroll](uiauto-implementingscroll.md) n’est pas pris en charge sur le conteneur qui a la barre de défilement. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Jamais   | Le modèle de contrôle [Scroll](uiauto-implementingscroll.md) n’est jamais directement pris en charge sur la barre de défilement.                                                                                                                     |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre de défilement. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.        | Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




