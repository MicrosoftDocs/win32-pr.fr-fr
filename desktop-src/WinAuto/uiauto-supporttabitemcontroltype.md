---
title: TabItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- UI Automation, prise en charge du type de contrôle TabItem
- UI Automation, type de contrôle TabItem
- UI Automation, arborescence pour le type de contrôle TabItem
- UI Automation, propriétés du type de contrôle TabItem
- UI Automation, modèles de contrôle pour le type de contrôle TabItem
- UI Automation, événements pour le type de contrôle TabItem
- arborescences, type de contrôle TabItem
- Propriétés, type de contrôle TabItem
- modèles de contrôle, type de contrôle TabItem
- événements, type de contrôle TabItem
- prise en charge du type de contrôle TabItem
- TabItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle TabItem
- types de contrôle, modèles de contrôle pour le type de contrôle TabItem
- types de contrôles, prise en charge de TabItem
- types de contrôle, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f82b96f5ae64b4cb22d650d6d349f18cb68619d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469106"
---
# <a name="tabitem-control-type"></a>TabItem (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **TabItem** .

Un contrôle d’élément d’onglet est le contrôle dans un contrôle d’onglet qui permet de sélectionner une page spécifique à afficher dans une fenêtre.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **TabItem** . Les spécifications d’UI Automation s’appliquent à tous les contrôles d’élément d’onglet où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles d’élément d’onglet et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>TabItem<ul><li>Image (0 ou 1)</li><li>Texte</li><li>Volet<ul><li>Plusieurs contrôles (0 ou plus)</li></ul></li></ul></li></ul> | <ul><li>TabItem<ul><li>Volet<ul><li>Plusieurs contrôles (0 ou plus)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **TabItem** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur       | Notes                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.  | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.  | Rectangle externe qui contient l’ensemble du contrôle.                                                                                    |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.  | Le contrôle d’élément d’onglet doit avoir une zone interactive qui entraîne la sélection de l’élément.                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)               | Consultez les remarques.  | Cette propriété peut être utilisée comme pointeur vers le volet d’onglets associé. Cela est utile quand il ne peut pas héberger un volet enfant de l’objet élément d’onglet. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TabItem** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle d’élément d’onglet est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | Le contrôle d’élément d’onglet est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.  | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null        | Le contrôle d’élément d’onglet n’a pas d’étiquette de texte statique.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.  | Chaîne localisée correspondant au type de contrôle **TabItem** . La valeur par défaut est « élément d’onglet » pour en-US ou anglais (États-Unis).       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.  | Le contrôle d’élément d’onglet est étiqueté automatiquement.                                                                                                          |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’élément d’onglet. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                 | Support  | Notes                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Obligatoire | Le contrôle d’élément d’onglet doit prendre en charge [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern). |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Jamais    | Le contrôle d’élément d’onglet ne prend jamais en charge [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).             |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’élément d’onglet. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                     | Notes                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                   | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.               | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) |                                                                                                                            |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




