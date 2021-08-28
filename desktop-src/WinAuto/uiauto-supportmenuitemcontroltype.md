---
title: MenuItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle MenuItem.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- UI Automation, prise en charge du type de contrôle MenuItem
- UI Automation, type de contrôle MenuItem
- UI Automation, arborescence pour le type de contrôle MenuItem
- UI Automation, propriétés du type de contrôle MenuItem
- UI Automation, modèles de contrôle pour le type de contrôle MenuItem
- UI Automation, événements pour le type de contrôle MenuItem
- arborescences, type de contrôle MenuItem
- Propriétés, MenuItem (type de contrôle)
- modèles de contrôle, type de contrôle MenuItem
- événements, type de contrôle MenuItem
- prise en charge du type de contrôle MenuItem
- MenuItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle MenuItem
- types de contrôles, modèles de contrôle pour le type de contrôle MenuItem
- types de contrôles, prise en charge de MenuItem
- types de contrôles, MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a48b94d7fc18cb9a8a6fe924fb73a250ab28708
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482509"
---
# <a name="menuitem-control-type"></a>MenuItem (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **MenuItem** .

Un contrôle menu permet une organisation hiérarchique des éléments associés à des commandes et des gestionnaires d’événements. dans une application Windows classique, une barre de menus contient plusieurs éléments de menu (tels que **fichier**, **edition** et **fenêtre**) et chaque élément de menu affiche un menu. Un menu contient un groupe d’éléments de menu (tels que **Nouveau**, **Ouvrir** et **Fermer**), qui peuvent être développés pour afficher des éléments de menu supplémentaires ou pour exécuter une action spécifique quand vous cliquez dessus.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **MenuItem** . Les spécifications d’UI Automation s’appliquent à tous les contrôles d’élément de menu où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Problèmes d’héritage](#legacy-issues)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles d’élément de menu, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>MenuItem "Aide"<ul><li>Menu (sous-menu de l’élément de menu aide)<ul><li>MenuItem "Rubriques d’aide"</li><li>MenuItem "À propos du Bloc-notes"</li></ul></li></ul></li></ul> | <ul><li>MenuItem "Aide"<ul><li>MenuItem "Rubriques d’aide"</li><li>MenuItem "À propos du Bloc-notes"</li></ul></li></ul> | 




 

L’affichage de contrôle du contrôle d’élément de menu a l’arborescence UI Automation présentée ci-dessus. Notez que l’élément de menu de l' **aide** dans la barre de menus a été ajouté pour mieux illustrer la structure.

Pour l’affichage du contenu, le **menu** est absent de l’arborescence UI Automation, car il ne transmet pas d’informations significatives à l’utilisateur final.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **MenuItem** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation. Allouez la propriété **AutomationId** pour un élément de menu si l’élément est connu pour être cohérent entre les différentes instances de l’interface utilisateur. Si l’élément de menu est rempli dynamiquement et n’est pas prévisible, laissez la propriété **AutomationId** vide. |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.                                                                                                                                                                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle d’élément de menu est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle d’élément de menu est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **MenuItem** . La valeur par défaut est « élément de menu » pour en-US ou anglais (États-Unis).                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | Le nom du contrôle d’élément de menu est le texte utilisé pour l’étiqueter.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles d’élément de menu. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support | Notes                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dépend | Si le contrôle peut être développé ou réduit, implémentez [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Dépend | Si le contrôle exécute une seule action ou commande, implémentez [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dépend | Si le contrôle est utilisé pour effectuer une sélection dans une liste d’options parmi les éléments de menu, implémentez [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dépend | Si le contrôle représente une option qui peut être activée ou désactivée, implémentez [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’élément de menu. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. | Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.       |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.                                 | Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.                 |



 

## <a name="legacy-issues"></a>Problèmes d’héritage

Pour les éléments de menu Microsoft Win32, le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) est pris en charge uniquement lorsqu’un élément de menu est activé et qu’il est possible de déterminer par programmation si la prise en charge du modèle de contrôle Toggle est requise. Étant donné qu’un élément de menu Win32 n’indique pas s’il peut être activé, le modèle de contrôle Invoke est pris en charge quand l’élément de menu n’est pas activé. Le modèle de contrôle Invoke est toujours pris en charge, même pour les éléments de menu qui sont uniquement requis pour prendre en charge le modèle de contrôle toggle. C’est pourquoi les clients ne sont pas confondus quand un élément de menu qui prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) (lorsque l’élément de menu était désactivé) ne prend plus en charge ce modèle lorsqu’il est activé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




