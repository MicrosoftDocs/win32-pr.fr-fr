---
title: StatusBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- UI Automation, prise en charge du type de contrôle StatusBar
- UI Automation, type de contrôle StatusBar
- UI Automation, arborescence pour le type de contrôle StatusBar
- UI Automation, propriétés pour le type de contrôle StatusBar
- UI Automation, modèles de contrôle pour le type de contrôle StatusBar
- UI Automation, événements pour le type de contrôle StatusBar
- arborescences, type de contrôle StatusBar
- Propriétés, type de contrôle StatusBar
- modèles de contrôle, type de contrôle StatusBar
- événements, type de contrôle StatusBar
- prise en charge du type de contrôle StatusBar
- StatusBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle StatusBar
- types de contrôle, modèles de contrôle pour le type de contrôle StatusBar
- types de contrôles, prise en charge de StatusBar
- types de contrôles, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52f3f04db86a8c8ff0e9cad9a3938a17e996e8210960912c3abc5039468e178
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614249"
---
# <a name="statusbar-control-type"></a>StatusBar (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **StatusBar** .

Un contrôle de barre d’état affiche des informations sur un objet affiché dans une fenêtre d’une application, le composant de l’objet ou des informations contextuelles relatives au fonctionnement de cet objet dans votre application.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **StatusBar** . Les exigences d’UI Automation s’appliquent à tous les contrôles de barre d’État où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de barre d’État et décrit ce que peut contenir chaque vue. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>StatusBar
<ul>
<li>Edition (0 ou plus)</li>
<li>ProgressBar (0 ou plusieurs)</li>
<li>Image (0 ou plusieurs)</li>
<li>Bouton (0 ou plusieurs)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Edition (0 ou plus)</li>
<li>ProgressBar (0 ou plusieurs)</li>
<li>Image (0 ou plusieurs)</li>
<li>Bouton (0 ou plusieurs)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de barre d’État. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur         | Remarques                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.    | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.    | Le rectangle englobant d’une barre d’état doit englober tous les contrôles qu’il contient.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.    | Pris en charge s’il existe un rectangle englobant. Si des zones du rectangle englobant ne sont pas interdépendantes et que l’élément effectue un test de positionnement spécialisé, substituez-le et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Le contrôle de barre d’État est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Le contrôle de barre d’État est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Dépend       | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Dépend       | Si un contrôle de barre d’État n’est pas actuellement visible, il retourne la valeur TRUE pour cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Le contrôle de barre d’État n’a généralement pas d’étiquette.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.    | Chaîne localisée correspondant au type de contrôle **StatusBar** . La valeur par défaut est « barre d’État » pour en-US ou anglais (États-Unis).                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.    | Le contrôle de barre d’état n’a pas besoin d’un nom sauf si plusieurs contrôles sont utilisés dans une application. Dans ce cas, distinguez chaque barre par des noms tels que « État Internet » ou « état de l’application ».                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Dépend       | Valeur indiquant l’orientation du contrôle : horizontale ou verticale.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour les contrôles de barre d’État. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                               | Support  | Notes                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Facultatif | Les contrôles de barre d’État doivent prendre en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) pour que les éléments individuels puissent être surveillés et facilement référencés pour les informations. |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre d’État. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Remarques                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété **IsEnabled** , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété **IsOffscreen** , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Remarques

Nous vous recommandons d’utiliser des contrôles d’édition comme éléments de grille enfants dans une barre d’État. Grâce aux contrôles d’édition, il est plus facile d’associer l’objectif du champ d’État à sa valeur à l’aide de la propriété nom et valeur de l’élément. Étant donné que les contrôles de texte ne doivent pas prendre en charge le modèle de contrôle **value** , ils ne doivent pas être utilisés en tant qu’éléments de grille enfants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




