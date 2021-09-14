---
title: Pane (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- UI Automation, prise en charge du type de contrôle Pane
- UI Automation, type de contrôle Pane
- UI Automation, arborescence pour le type de contrôle Pane
- UI Automation, propriétés pour le type de contrôle Pane
- UI Automation, modèles de contrôle pour le type de contrôle Pane
- UI Automation, événements pour le type de contrôle Pane
- arborescences, type de contrôle Pane
- Propriétés, Pane (type de contrôle)
- modèles de contrôle, type de contrôle Pane
- événements, type de contrôle Pane
- prise en charge du type de contrôle Pane
- Pane (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Pane
- types de contrôles, modèles de contrôle pour le type de contrôle Pane
- types de contrôles, prise en charge pour le volet
- types de contrôles, volet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b335496d8d40d20ccc68f6bc2b048c87ff608dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192632"
---
# <a name="pane-control-type"></a>Pane (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Pane** .

Le type de contrôle **Pane** est destiné aux régions potentiellement défilantes qui ont un contenu disparate. Il est utilisé pour représenter un objet dans un frame ou une fenêtre de document. Les utilisateurs peuvent naviguer entre les contrôles de volet et dans le contenu du volet actuel. Les contrôles de volet représentent un niveau de regroupement inférieur à celui de Windows ou de documents, mais au-dessus des contrôles individuels. L’utilisateur navigue entre les volets en appuyant sur TAB, F6 ou Ctrl+Tab, en fonction du contexte.

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Pane** . Les exigences d’UI Automation s’appliquent à tous les contrôles de volet où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Exemple de type de contrôle Pane](#pane-control-type-example)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de volet et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Volet</li></ul> | <ul><li>Volet</li></ul> | 




 

Un contrôle de volet apparaît toujours dans les affichages de contrôle et de contenu. N’exposez pas un objet layout en tant que volet dans l’affichage de contrôle ou de contenu si l’objet est utilisé uniquement pour la présentation visuelle.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de volet. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur      | Notes                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | Si une combinaison de touches spécifique donne le focus au volet, ces informations doivent être exposées via cette propriété.                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques. | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques. | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques. | Cette propriété expose un point interactif du contrôle de volet qui, lorsque vous cliquez dessus, place le focus sur le volet.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Volet**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques. | Le texte d’aide pour les contrôles de volet doit expliquer l’objectif du frame et sa relation avec d’autres frames. Une description est nécessaire si l’objectif et la relation des frames ne sont pas clairs par rapport à la valeur de la propriété [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) . |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle de volet est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Le contrôle de volet est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques. | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques. | Les contrôles Pane n’ont pas d’étiquette statique. S’il existe une étiquette de texte statique, il doit être exposé via cette propriété.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques. | Chaîne localisée correspondant au type de contrôle **Pane** . La valeur par défaut est « Pane » pour en-US ou anglais (États-Unis).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques. | La valeur de cette propriété doit toujours être un titre clair, concis et explicite.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de volet. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                         | Support | Notes                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Dépend | Implémentez le modèle de contrôle [Dock](uiauto-implementingdock.md) si le contrôle de volet peut être ancré.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dépend | Implémentez le modèle de contrôle [Scroll](uiauto-implementingscroll.md) si le contrôle de volet peut défiler.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dépend | Implémentez le modèle de contrôle [Transform](uiauto-implementingtransform.md) si le contrôle de volet peut être déplacé, redimensionné ou pivoté sur l’écran.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Jamais   | Si l’élément doit implémenter le modèle de contrôle [Window](uiauto-implementingwindow.md) , le contrôle doit être basé sur le type de contrôle [Window](uiauto-supportwindowcontroltype.md) . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de volet. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Notes                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Exemple de type de contrôle Pane

L’image suivante illustre un contrôle qui implémente le type de contrôle **Pane** .

![capture d’écran montrant un exemple de contrôle de volet](images/panexmpl.jpg)




| Arborescence UI Automation — vue contrôle | Arborescence UI Automation — affichage du contenu | 
|-----------------------------------|-----------------------------------|
| <ul><li>Volet<ul><li>Tree (modèle Scroll)<ul><li>TreeItem</li><li>...</li></ul></li></ul></li><li>Volet<ul><li>Modifier (modèle Scroll)</li></ul></li></ul> | <ul><li>Volet<ul><li>Tree (modèle Scroll)<ul><li>TreeItem</li><li>...</li></ul></li><li>Volet<ul><li>Modifier (modèle Scroll)</li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




