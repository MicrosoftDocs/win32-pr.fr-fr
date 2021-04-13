---
title: Text (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- UI Automation, prise en charge du type de contrôle Text
- UI Automation, type de contrôle Text
- UI Automation, arborescence pour le type de contrôle Text
- UI Automation, propriétés du type de contrôle Text
- UI Automation, modèles de contrôle pour le type de contrôle Text
- UI Automation, événements pour le type de contrôle Text
- arborescences, type de contrôle Text
- Propriétés, type de contrôle Text
- modèles de contrôle, type de contrôle Text
- événements, type de contrôle Text
- prise en charge du type de contrôle Text
- Text (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Text
- types de contrôles, modèles de contrôle pour le type de contrôle Text
- types de contrôles, prise en charge du texte
- types de contrôles, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310590"
---
# <a name="text-control-type"></a>Text (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Text** .

Un contrôle de texte est un élément d’interface utilisateur de base qui représente une partie du texte à l’écran.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Text** . Les exigences d’UI Automation s’appliquent à tous les contrôles d’arborescence où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de texte et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).



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
<li>Texte</li>
</ul></td>
<td><ul>
<li>Text (s’il s’agit de contenu)</li>
</ul></td>
</tr>
</tbody>
</table>



 

Un contrôle de texte peut être utilisé seul comme étiquette ou texte statique dans un formulaire. Il peut également être contenu dans la structure de l’un des éléments suivants :

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [ListItem](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

Les contrôles de texte peuvent ne pas apparaître dans l’affichage de contenu de l’arborescence UI Automation, car le texte est souvent affiché via la propriété **Name** d’un autre contrôle. Par exemple, le texte utilisé pour étiqueter un contrôle de zone de liste déroulante est exposé via la propriété **Name** du contrôle. Étant donné que le contrôle de zone de liste déroulante se trouve dans l’affichage de contenu de l’arborescence UI Automation, le contrôle de texte n’a pas besoin d’être présent. Les contrôles de texte peuvent avoir des enfants dans l’affichage de contenu s’il existe un objet incorporé, tel qu’un lien hypertexte.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de texte. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                                            |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Text**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Dépend    | Le contrôle de texte est du contenu s’il contient des informations qui ne sont pas exposées dans la propriété Name d’un autre contrôle.                                                                                                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle de texte doit toujours être un contrôle.                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                                                           |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Les contrôles de texte n’ont pas d’étiquette de texte statique.                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Text** . La valeur par défaut est « texte » pour en-US ou anglais (États-Unis).                                                                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le nom d’un contrôle de texte peut être le texte qu’il affiche. Toutefois, si le contrôle prend également en charge le modèle de [texte](uiauto-implementingtextandtextrange.md) et que le texte est étendu, n’utilisez pas le contenu de texte intégral comme valeur de **nom** . Au lieu de cela, fournissez une valeur de **nom** plus petite, dérivée d’autres propriétés de votre contrôle. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de texte. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                         | Support | Notes                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Dépend | Si le contrôle de texte est contenu dans un contrôle de table, le modèle de contrôle [GridItem](uiauto-implementinggriditem.md) doit être pris en charge.                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Dépend | Si le contrôle de texte est contenu dans un contrôle de table, le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) doit être pris en charge.                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Dépend | Le texte doit prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) pour une meilleure accessibilité. Toutefois, ce n’est pas obligatoire. Le modèle de contrôle Text est utile quand le texte possède un style complexe et des attributs (par exemple, couleur, gras et italique). |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Jamais   | Un contrôle de texte ne prend jamais en charge le modèle de contrôle [value](uiauto-implementingvalue.md) . Si le texte est modifiable, il s’agit du type de contrôle [Edit](uiauto-supporteditcontroltype.md) .                                                                                    |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation que les contrôles de texte doivent prendre en charge. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**\_TextChangedEventId de texte UIA \_**](uiauto-event-ids.md)                                                 | Si le contrôle prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , il doit prendre en charge cet événement.   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




