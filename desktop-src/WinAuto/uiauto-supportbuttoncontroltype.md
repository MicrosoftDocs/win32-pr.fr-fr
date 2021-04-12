---
title: Button (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- UI Automation, prise en charge du type de contrôle Button
- UI Automation, type de contrôle Button
- UI Automation, arborescence pour le type de contrôle Button
- UI Automation, propriétés pour le type de contrôle Button
- UI Automation, modèles de contrôle pour le type de contrôle Button
- UI Automation, événements pour le type de contrôle Button
- arborescences, type de contrôle Button
- Propriétés, Button (type de contrôle)
- modèles de contrôle, type de contrôle Button
- événements, Button (type de contrôle)
- prise en charge du type de contrôle Button
- Button (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Button
- types de contrôles, modèles de contrôle pour le type de contrôle Button
- types de contrôles, prise en charge du bouton
- types de contrôle, bouton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197455"
---
# <a name="button-control-type"></a>Button (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Button** .

Un bouton est un objet avec lequel un utilisateur interagit pour effectuer une action. Tel est le cas des boutons OK et Annuler d’une boîte de dialogue. Le contrôle button est un contrôle simple à exposer, car il correspond à une commande unique que l’utilisateur veut exécuter.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Button** . Les spécifications d’UI Automation s’appliquent à tous les contrôles de bouton où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles Button et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Bouton
<ul>
<li>Image (0 ou plus)</li>
<li>Text (0 ou plus)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Bouton</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **Button** (tels que les contrôles Button). Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Un contrôle Button prend généralement en charge une touche accélérateur pour permettre à l’utilisateur final d’effectuer rapidement l’action représentée par le bouton à partir du clavier.                                             |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Button** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | Le texte d’aide doit indiquer ce que sera le résultat final de l’activation du bouton. Il s’agit généralement du même type d’informations que celui présenté dans une info-bulle.                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle Button doit toujours être du contenu.                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle Button doit toujours être un contrôle.                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Les contrôles Button sont étiquetés automatiquement par leur contenu.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Button** . La valeur par défaut est « Button » pour « fr-fr » ou « anglais » (États-Unis).                                                                   |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le nom du contrôle Button est le texte utilisé pour l’étiqueter. Chaque fois qu’une image est utilisée pour étiqueter un bouton, un texte de remplacement doit être fourni pour la propriété **Name** du bouton.                        |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles bouton. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                                  | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Consultez les remarques.    | Quand un bouton est hébergé en tant qu’enfant d’un bouton partagé, le bouton enfant peut prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) à la place du modèle de contrôle [Invoke](uiauto-implementinginvoke.md) ou [Toggle](uiauto-implementingtoggle.md) . Le modèle de contrôle ExpandCollapse peut être utilisé pour ouvrir ou fermer un menu ou une autre sous-structure associée à l’élément Button. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Consultez les remarques.    | Tous les boutons doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) ou le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , mais pas les deux. Le modèle de contrôle Invoke doit être pris en charge lorsque le bouton exécute une commande à la demande de l’utilisateur. Cette commande correspond à une seule opération, par exemple, Couper, Copier, Coller ou Supprimer.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Consultez les remarques.    | Tous les boutons doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) ou le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , mais pas les deux. Le modèle de contrôle Toggle doit être pris en charge si le bouton peut parcourir une série de trois États au maximum. En général, cela est considéré comme un commutateur d’activation/désactivation pour des fonctionnalités spécifiques.                                                                        |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de bouton. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.    | Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




