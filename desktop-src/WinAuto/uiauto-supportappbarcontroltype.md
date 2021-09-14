---
title: Type de contrôle AppBar
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- UI Automation, prise en charge du type de contrôle AppBar
- UI Automation, type de contrôle AppBar
- UI Automation, modèles de contrôle pour le type de contrôle AppBar
- modèles de contrôle, type de contrôle AppBar
- prise en charge du type de contrôle AppBar
- Type de contrôle AppBar
- types de contrôles, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf562b125267e9b35239e8490f11ed6ae830
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122617"
---
# <a name="appbar-control-type"></a>Type de contrôle AppBar

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **appbar** .

Une barre d’application est un élément d’interface utilisateur qui présente la navigation, les commandes et les outils à l’utilisateur. pour les applications Windows store, vous pouvez afficher les barres de l’application pour les applications en appuyant sur Windows touche + Z.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **appbar** .

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Événements obligatoires](#required-events)
-   [Événements pertinents](#relevant-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles **appbar** et décrit ce que peut contenir chaque affichage. **Button** est l’élément le plus courant dans un **appbar** , mais les autres contrôles qui appellent des actions pour une application sont également possibles. Un **appbar** peut également avoir 0 ou plusieurs séparateurs (type de contrôle **separator** ), qui apparaissent dans l’affichage de contrôle tels qu’ils sont placés entre les autres contrôles. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>AppBar<ul><li>Bouton (0 ou plusieurs)</li><li>Autres contrôles (0 ou plusieurs)</li></ul></li></ul> | <ul><li>Non applicable<ul><li>Bouton (0 ou plusieurs)</li><li>Autres contrôles (0 ou plusieurs)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **appbar** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | La valeur exposée par cette propriété doit inclure tous les contrôles qu’elle contient.                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Un contrôle de barre d’application n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Un contrôle de barre d’application est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Voir les remarques  | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété. Les contrôles dans la barre de l’application peuvent généralement prendre le focus clavier.                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consultez les remarques. | La valeur de cette propriété varie selon que le contrôle est visible ou non à l’écran.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Les contrôles de la barre de l’application n’ont généralement pas d’étiquette.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **appbar** . La valeur par défaut est « barre d’application » pour en-US ou anglais (États-Unis).                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | Le contrôle de la barre de l’application n’a pas besoin d’un nom, sauf si une application contient plusieurs barres de l’application. S’il existe plusieurs barres d’application dans une application, utilisez cette propriété pour exposer des noms distinctifs, tels que « Top » ou « Bottom ». |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de la barre de l’application. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                   | Notes                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                 | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.             | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Événements pertinents

Le tableau suivant répertorie les événements UI Automation qui sont particulièrement pertinents pour les contrôles qui implémentent le type de contrôle **appbar** , mais qui ne sont pas strictement requis.



| Événement UI Automation                                                                                 | Notes                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                            | Les implémentations de plateforme peuvent déclencher cet événement lorsque le contrôle de la barre de l’application est fermé. |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                            | Les implémentations de plateforme peuvent déclencher cet événement lorsque le contrôle de la barre de l’application est ouvert. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Gestionnaire d’événements de modification de propriété.                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> <dt>

**Référence**
</dt> <dt>

[**Contrôle XAML AppBar**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**WinJS. UI. AppBar, objet**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 
