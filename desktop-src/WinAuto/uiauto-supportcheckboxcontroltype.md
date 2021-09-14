---
title: CheckBox (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- UI Automation, prise en charge du type de contrôle CheckBox
- UI Automation, type de contrôle CheckBox
- UI Automation, arborescence pour le type de contrôle CheckBox
- UI Automation, propriétés du type de contrôle CheckBox
- UI Automation, modèles de contrôle pour le type de contrôle CheckBox
- UI Automation, événements pour le type de contrôle CheckBox
- arborescences, type de contrôle CheckBox
- Propriétés, CheckBox (type de contrôle)
- modèles de contrôle, CheckBox (type de contrôle)
- événements, CheckBox (type de contrôle)
- prise en charge du type de contrôle CheckBox
- CheckBox (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle CheckBox
- types de contrôles, modèles de contrôle pour le type de contrôle CheckBox
- types de contrôles, prise en charge de CheckBox
- types de contrôle, CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec20bc259095c41bd1bdc4c3d4e5953be2e883d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122606"
---
# <a name="checkbox-control-type"></a>CheckBox (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **CheckBox** .

Une case à cocher est un objet utilisé pour indiquer un état avec lequel les utilisateurs peuvent interagir pour parcourir cet état. Les cases à cocher présentent une option binaire (oui/non), (activé/désactivé), ou tertiaire (activé, désactivé, indéterminé) à l’utilisateur.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **CheckBox** . Les exigences d’UI Automation s’appliquent à tous les contrôles de case à cocher où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Nœud](#defaultaction)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de case à cocher et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>CheckBox</li></ul> | <ul><li>CheckBox</li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **CheckBox** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                       |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                           |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | La valeur de cette propriété doit toujours être **true**. Cela signifie que le contrôle de case à cocher doit toujours être inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | La valeur de cette propriété doit toujours être **true**. Cela signifie que le contrôle de case à cocher doit toujours être inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Les contrôles de case à cocher sont à étiquette automatique.                                                                                                                                                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **CheckBox** . La valeur par défaut est « case à cocher » pour en-US ou anglais (États-Unis).                                                                                                                                            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | La valeur de la propriété [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (ou [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) du contrôle de case à cocher est le texte qui s’affiche à côté de la zone qui maintient l’État bascule. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de case à cocher. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                  | Prise en charge/valeur | Notes                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Obligatoire      | Les cases à cocher prennent en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) pour permettre à la case à cocher d’être recycle par programmation par le biais de ses États internes. |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de case à cocher. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="defaultaction"></a>Nœud

L’action par défaut de la case à cocher est de placer le focus sur une case d’option et de basculer son état actuel. Comme mentionné précédemment, les cases à cocher présentent une décision binaire (oui/non ou activé/désactivé) à l’utilisateur ou un tertiaire (activé, désactivé ou indéterminé). Si la case à cocher est binaire, l’action par défaut bascule l’état « activé » vers « désactivé » ou l’état « désactivé » vers « activé ». Dans une case à cocher tertiaire, l’action par défaut parcourt les États de la case à cocher dans le même ordre que si l’utilisateur a envoyé des clics de souris successifs au contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




