---
title: SplitButton (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- UI Automation, prise en charge du type de contrôle SplitButton
- UI Automation, type de contrôle SplitButton
- UI Automation, arborescence pour le type de contrôle SplitButton
- UI Automation, propriétés du type de contrôle SplitButton
- UI Automation, modèles de contrôle pour le type de contrôle SplitButton
- UI Automation, événements pour le type de contrôle SplitButton
- arborescences, type de contrôle SplitButton
- Propriétés, type de contrôle SplitButton
- modèles de contrôle, type de contrôle SplitButton
- événements, type de contrôle SplitButton
- prise en charge du type de contrôle SplitButton
- SplitButton (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle SplitButton
- types de contrôles, modèles de contrôle pour le type de contrôle SplitButton
- types de contrôles, prise en charge du SplitButton
- types de contrôles, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e420d369ee09dfd2d92b5e5d79cf94c7013566
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520560"
---
# <a name="splitbutton-control-type"></a>SplitButton (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **SplitButton** .

Le contrôle bouton partagé permet d’effectuer une action sur un contrôle et de développer le contrôle pour afficher la liste des autres actions possibles qui peuvent être effectuées.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **SplitButton** . Les exigences d’UI Automation s’appliquent à tous les contrôles bouton partagé où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Exemple de type de contrôle SplitButton](#splitbutton-control-type-example)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles bouton partagé et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>SplitButton<ul><li>Image (0 ou 1)</li><li>Text (0 ou 1)</li><li>Button (1 ou 2)<ul><li>Menu (0 ou 1 ; apparaît en tant qu’enfant d’un sous-bouton qui prend en charge le modèle ExpandCollapse)<ul><li>MenuItem (1 et plus)</li></ul></li></ul></li></ul></li></ul> | <ul><li>SplitButton<ul><li>Button (1 ou 2)<ul><li>MenuItem (1 et plus)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **SplitButton** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur           | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.      | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.      | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.      | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques.      | Le texte d’aide peut indiquer le résultat de l’activation du bouton partagé, qui contient généralement le même type d’informations que celles présentées via une info-bulle.                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Le contrôle bouton partagé contient des informations pour l’utilisateur final.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | Le contrôle bouton partagé est visible par l’utilisateur final.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.      | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | Les contrôles bouton partagé n’ont pas d’étiquette de texte statique.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.      | Chaîne localisée correspondant au type de contrôle **SplitButton** . La valeur par défaut est « fractionner le bouton » pour en-US ou anglais (États-Unis).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.      | Texte utilisé pour étiqueter le bouton partagé. Chaque fois qu’une image est utilisée pour étiqueter un bouton partagé, un texte de remplacement doit être fourni pour la propriété nom du bouton partagé.                              |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles bouton partagé. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support  | Notes                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obligatoire | Étant donné que les boutons partagés ont toujours la possibilité de développer une liste d’options, ils doivent prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Obligatoire | Étant donné que les boutons partagés ont toujours une action par défaut associée à la méthode [**IInvokeProvider :: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , ils doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation qui doivent être pris en charge par les contrôles bouton Split. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Exemple de type de contrôle SplitButton

L’image suivante illustre un contrôle qui implémente le type de contrôle **SplitButton** .

![capture d’écran montrant un exemple de contrôle SplitButton](images/splitbuttonxmpl.jpg)




| Arborescence UI Automation — vue contrôle | Arborescence UI Automation — affichage du contenu | 
|-----------------------------------|-----------------------------------|
| <ul><li>SplitButton "Nom" (Invoke, ExpandCollapse)<ul><li>Bouton « plus d’options » (Invoke)<ul><li>Menu<ul><li>MenuItem</li><li>...</li></ul></li></ul></li></ul></li></ul> | <ul><li>SplitButton "Nom" (Invoke, ExpandCollapse)<ul><li>Bouton « plus d’options » (Invoke)<ul><li>Menu<ul><li>MenuItem</li><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




