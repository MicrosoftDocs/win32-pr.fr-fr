---
title: Thumb (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- UI Automation, prise en charge du type de contrôle Thumb
- UI Automation, type de contrôle Thumb
- UI Automation, arborescence pour le type de contrôle Thumb
- UI Automation, propriétés du type de contrôle Thumb
- UI Automation, modèles de contrôle pour le type de contrôle Thumb
- UI Automation, événements pour le type de contrôle Thumb
- arborescences, type de contrôle Thumb
- Propriétés, type de contrôle Thumb
- modèles de contrôle, type de contrôle Thumb
- événements, type de contrôle Thumb
- prise en charge du type de contrôle Thumb
- Thumb (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Thumb
- types de contrôles, modèles de contrôle pour le type de contrôle Thumb
- types de contrôles, prise en charge de Thumb
- types de contrôles, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea75b39ae0b17be23886823d446667299e5f0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478785"
---
# <a name="thumb-control-type"></a>Thumb (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Thumb** .

Les contrôles curseur de position fournissent des fonctionnalités qui permettent de déplacer ou de faire glisser un contrôle, par exemple un bouton de barre de défilement, ou de le redimensionner, par exemple un widget de redimensionnement de fenêtre. Notez qu’un contrôle Thumb ne fournit pas de fonctionnalité de glisser-déplacer. Les contrôles Thumb peuvent recevoir le focus de souris, mais pas le focus clavier. Le développeur du contrôle doit implémenter ce dernier pour qu’il se comporte de manière appropriée (déplacement ou redimensionnement).

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Thumb** . Les exigences d’UI Automation appliquent tous les contrôles Thumb où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles Thumb et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Thumb</li></ul> | (Non applicable) | 




 

Les contrôles Thumb n’apparaissent jamais dans l’affichage de contenu, car ils n’existent que pour être manipulés avec une souris. Ils sont exposés via un autre modèle de contrôle, tel que le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , le modèle de contrôle [Transform](uiauto-implementingtransform.md) ou le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , pris en charge sur le conteneur du contrôle Thumb.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Thumb. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Point dans la zone cliente visible du contrôle Thumb.                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Flash**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Le contrôle Thumb n’est jamais inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle Thumb est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété. Un contrôle Thumb peut recevoir le focus s’il est utilisé comme un objet de « pincement » pour le dimensionnement d’une fenêtre ou d’un volet. Un contrôle Thumb dans un curseur ou une barre de défilement ne doit jamais recevoir le focus. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | Les contrôles curseur de position n’ont jamais d’étiquette.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Thumb** . La valeur par défaut est « Thumb » pour « fr-fr » ou « anglais » (États-Unis).                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL       | Étant donné que le contrôle Thumb n’est pas disponible dans l’affichage de contenu de l’arborescence UI Automation, il ne nécessite pas de nom.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles Thumb. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                         | Support  | Notes                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obligatoire | Permet de déplacer le contrôle curseur de position à l’écran. Étant donné que le contrôle Thumb ne peut généralement pas être redimensionné ou pivoté, le modèle de contrôle [Transform](uiauto-implementingtransform.md) prend principalement en charge la fonction [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Thumb. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




