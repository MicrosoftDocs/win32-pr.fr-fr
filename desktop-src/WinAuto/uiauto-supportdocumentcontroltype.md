---
title: Document (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- UI Automation, prise en charge du type de contrôle document
- UI Automation, type de contrôle de document
- UI Automation, arborescence pour le type de contrôle document
- UI Automation, propriétés du type de contrôle document
- UI Automation, modèles de contrôle pour le type de contrôle document
- UI Automation, événements pour le type de contrôle document
- arborescences, type de contrôle document
- Propriétés, document (type de contrôle)
- modèles de contrôle, type de contrôle document
- événements, type de contrôle document
- prise en charge du type de contrôle document
- Document (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle document
- types de contrôles, modèles de contrôle pour le type de contrôle document
- types de contrôles, prise en charge du document
- types de contrôles, document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb068e5b2d69c3b7ac180b65436888ca550b1db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467796"
---
# <a name="document-control-type"></a>Document (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **document** .

Les contrôles de document permettent à l’utilisateur d’afficher et de manipuler plusieurs pages de texte. Contrairement aux contrôles d’édition qui prennent uniquement en charge une simple ligne de texte sans mise en forme, les contrôles de document peuvent héberger du texte de style et de mise en forme enrichis

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **document** . Les exigences d’UI Automation s’appliquent à tous les contrôles de document où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de document, et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>Document<ul><li>Variable</li></ul></li></ul> | <ul><li>Document<ul><li>Variable</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de document. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Le document comporte une zone interactive qui place le focus sur le document ou sur l’un de ses éléments dans le conteneur du document.                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Document** |                                                                                                                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle de document est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle de document est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.   | La valeur de cette propriété doit être l’étiquette du contrôle de document. En général, le titre du document est utilisé.                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **document** . La valeur par défaut est « document » pour en-US ou anglais (États-Unis).            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | Le contrôle de document obtient généralement son nom à partir du nom de fichier à partir duquel il est chargé. Il est souvent affiché dans le titre de la fenêtre ou du frame qui le contient. |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de document. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle/Propriété de modèle                  | Prise en charge/valeur | Notes                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Dépend       | Le contrôle de document peut couvrir une étendue supérieure à celle de la fenêtre d’affichage. Le contrôle doit prendre en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) si le contenu est défilant.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Obligatoire      | Tous les contrôles de document doivent prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) .                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Dépend       | Alors que les clients UI Automation peuvent utiliser [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) pour obtenir des informations textuelles sur un document, ils ont besoin du modèle de contrôle [value](uiauto-implementingvalue.md) pour définir la valeur interne. Une entrée de texte simple est possible uniquement via le modèle de contrôle value. |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de document. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                        | Notes                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                      | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                  | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.   | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId. | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.           | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.       | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.     | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.               | Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.           |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md)                                                            | Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.     |
| [**\_TextSelectionChangedEventId de texte UIA \_**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**\_TextChangedEventId de texte UIA \_**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                                       | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.             |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




