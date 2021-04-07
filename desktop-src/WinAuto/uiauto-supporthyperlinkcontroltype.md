---
title: HYPERLINK (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- UI Automation, prise en charge du type de contrôle HyperLink
- UI Automation, type de contrôle HyperLink
- UI Automation, arborescence pour le type de contrôle HyperLink
- UI Automation, propriétés du type de contrôle HyperLink
- UI Automation, modèles de contrôle pour le type de contrôle HyperLink
- UI Automation, événements pour le type de contrôle HyperLink
- arborescences, type de contrôle HyperLink
- Propriétés, type de contrôle HyperLink
- modèles de contrôle, type de contrôle HyperLink
- événements, type de contrôle HyperLink
- prise en charge du type de contrôle HyperLink
- Hyperlink (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle HyperLink
- types de contrôles, modèles de contrôle pour le type de contrôle HyperLink
- types de contrôles, prise en charge du lien hypertexte
- types de contrôles, lien hypertexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673074"
---
# <a name="hyperlink-control-type"></a>HYPERLINK (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Hyperlink** .

Les contrôles de lien hypertexte créent des liens qui permettent aux utilisateurs de naviguer dans la même page ou d’une page à une autre.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Hyperlink** . Les exigences d’UI Automation s’appliquent à tous les contrôles de lien hypertexte où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de lien hypertexte et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Hyperlink</li>
</ul></td>
<td><ul>
<li>Hyperlink</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de lien hypertexte. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur         | Notes                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.    | La valeur de cette propriété doit être unique pour tous les contrôles d’une application.                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.    | Rectangle externe qui contient l’ensemble du contrôle.                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.    | Le point cliquable du contrôle de lien hypertexte doit être un point qui lance le lien hypertexte si l’utilisateur clique dessus avec le pointeur de la souris.                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Lien hypertexte** |                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Le contrôle de lien hypertexte est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | Le contrôle de lien hypertexte est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.    | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.    | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.    | Chaîne localisée correspondant au type de contrôle **Hyperlink** . La valeur par défaut est « HYPERLINK » pour en-US ou anglais (États-Unis). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.    | Le nom du contrôle de lien hypertexte est le texte affiché sur l’écran comme souligné.                                                  |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation que les contrôles de lien hypertexte doivent prendre en charge. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                  | Prise en charge/valeur                | Notes                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Obligatoire                     | Tous les contrôles de lien hypertexte doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) .                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Dépend                      | Les contrôles de lien hypertexte doivent prendre en charge le modèle de contrôle [value](uiauto-implementingvalue.md) quand le lien contient des informations utilisables et explicites pour l’utilisateur.                                                                              |
| [**Valeur**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Par exemple, «https://www...» | Une URL pour une adresse Internet ou intranet est un exemple de lien hypertexte qui contient des informations explicites pour l’utilisateur. Toutefois, un lien de programmation est significatif uniquement pour une application et n’est pas recommandé pour la propriété **value** . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de lien hypertexte. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Notes

Le type de contrôle HyperLink doit être appliqué uniquement à un objet qui, lorsque vous cliquez dessus, provoque l’exécution de la navigation. elle ne doit pas être appliquée au conteneur du lien hypertexte. Par exemple, seules les « zones réactives » cliquables à l’intérieur d’une image interactive doivent avoir le type de contrôle **Hyperlink** . Il en va de même pour les liens hypertexte dans un champ de texte ou un conteneur de documents. Dans ce cas, seul le texte ou l’image du lien hypertexte doit avoir le type de contrôle **Hyperlink** , et non le conteneur.

Le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) est idéal pour prendre en charge les liens hypertexte incorporés dans les éléments texte ou document.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




