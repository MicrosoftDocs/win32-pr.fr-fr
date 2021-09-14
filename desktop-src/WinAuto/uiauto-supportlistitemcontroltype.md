---
title: ListItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- UI Automation, prise en charge du type de contrôle ListItem
- UI Automation, type de contrôle ListItem
- UI Automation, arborescence pour le type de contrôle ListItem
- UI Automation, propriétés du type de contrôle ListItem
- UI Automation, modèles de contrôle pour le type de contrôle ListItem
- UI Automation, événements pour le type de contrôle ListItem
- arborescences, type de contrôle ListItem
- Propriétés, type de contrôle ListItem
- modèles de contrôle, type de contrôle ListItem
- événements, type de contrôle ListItem
- prise en charge du type de contrôle ListItem
- ListItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ListItem
- types de contrôle, modèles de contrôle pour le type de contrôle ListItem
- types de contrôles, prise en charge de ListItem
- types de contrôles, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf7275212d44b795f354cb895c2d64727e375ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192651"
---
# <a name="listitem-control-type"></a>ListItem (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **ListItem** .

Les contrôles d’élément de liste sont un exemple de contrôles qui implémentent le type de contrôle **ListItem** .

Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **ListItem** . Les exigences d’UI Automation s’appliquent à tous les contrôles d’élément de liste où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Événements obligatoires](#required-events)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’élément de liste et décrit ce que peut contenir chaque affichage. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>ListItem<ul><li>Image (0 ou plus)</li><li>Text (0 ou plus)</li><li>Edition (0 ou plus)</li></ul></li></ul> | <ul><li>ListItem</li></ul> | 




 

Les enfants d’un contrôle d’élément de liste dans l’affichage de contenu de l’arborescence UI Automation doivent toujours afficher des enfants nuls. Si la structure du contrôle est telle que d’autres éléments sont contenus sous l’élément de liste, il doit suivre les spécifications de la prise en charge d’UI Automation pour le type de contrôle [TreeItem](uiauto-supporttreeitemcontroltype.md) .

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **ListItem** . Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation. Allouez la propriété **AutomationId** pour un élément de liste si l’élément est connu pour être cohérent entre les différentes instances de l’interface utilisateur. Si l’élément de liste est rempli dynamiquement et n’est pas prévisible, laissez la propriété **AutomationId** vide.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | La valeur de cette propriété doit inclure la zone de contenu de l’image et du texte de l’élément de liste.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Dépend      | Si le contrôle de liste a un point interactif (point sur lequel vous pouvez cliquer pour que la liste prenne le focus), ce point doit être exposé via cette propriété. Si le contrôle de liste est intégralement couvert par les éléments de liste descendants, il retourne l’erreur [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) pour indiquer que le client doit demander à un élément à l’intérieur du contrôle de liste un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ListItem** | Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques.   | Le texte d’aide des contrôles de liste doit expliquer pourquoi l’utilisateur est amené à faire un choix dans une liste d’options. Il s’agit généralement du même type d’informations que dans une info-bulle. Par exemple, « sélectionnez un élément pour définir la résolution d’affichage de votre moniteur ».                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Le contrôle de liste est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Le contrôle de liste est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le conteneur peut accepter l’entrée au clavier, cette propriété doit avoir la valeur **true**.                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Dépend      | Cette propriété doit retourner une valeur indiquant si l’élément de liste fait actuellement l’objet d’un défilement dans le conteneur parent qui implémente le modèle de contrôle [Scroll](uiauto-implementingscroll.md) .                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Dépend      | Si le contrôle contient l’État mis à jour dynamiquement, cette propriété doit être prise en charge afin qu’une technologie d’assistance puisse recevoir des mises à jour lorsque l’état de l’élément change.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Dépend      | Cette propriété doit être exposée pour les contrôles d’élément de liste qui représentent un objet sous-jacent. Ces contrôles d’élément de liste ont généralement une icône associée au contrôle que les utilisateurs associent à l’objet sous-jacent.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consultez les remarques.   | S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **ListItem** . La valeur par défaut est « élément de liste » pour en-US ou anglais (États-Unis).                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | La valeur de la propriété Name d’un contrôle d’élément de liste provient de l’étiquette de texte de l’élément.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’élément de liste. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support | Notes                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dépend | Si l’élément peut être manipulé pour afficher ou masquer des informations, le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) doit être implémenté.                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Dépend | Si la navigation spatiale d’un élément à un élément est prise en charge dans le conteneur de liste, et si le conteneur est organisé en lignes et en colonnes, le modèle de contrôle [GridItem](uiauto-implementinggriditem.md) doit être implémenté.                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Dépend | Si l’élément a une commande qui peut être exécutée sur celui-ci, séparément de la sélection, le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) doit être implémenté. Il s’agit généralement d’une action associée au double-clic sur le contrôle d’élément de liste. les exemples sont le lancement d’un document à partir de Windows Explorer ou la diffusion d’un fichier musical dans Microsoft Lecteur Windows Media.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Dépend | Si l’élément de liste est contenu dans un conteneur qui peut faire l’objet d’un défilement, le modèle de contrôle [ScrollItem](uiauto-implementingscrollitem.md) doit être implémenté.                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dépend | Un contrôle d’élément de liste qui prend en charge la sélection doit implémenter le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) . Cela permet aux contrôles d’élément de liste de transmettre des informations quand ils sont sélectionnés.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dépend | Si l’élément de liste est sélectionnable et que l’action n’effectue pas de changement d’état de sélection, le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) doit être implémenté.                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dépend | Si l’élément peut être modifié, le modèle de contrôle [value](uiauto-implementingvalue.md) doit être implémenté. Les modifications apportées au contrôle d’élément de liste entraînent des modifications des valeurs des propriétés [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) et [**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md) . |



 

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation qui répertorient les contrôles d’éléments qui doivent être pris en charge. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. | Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété ItemStatusPropertyId.                                            | Si le contrôle prend en charge la propriété [**ItemStatus**](uiauto-automation-element-propids.md) , doit prendre en charge cet événement.        |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.                                 | Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.                 |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                                               | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.                   |



 

## <a name="remarks"></a>Notes

Si un conteneur héberge des éléments de liste, les principaux moyens de navigation doivent être placés dans les éléments de la liste. Placer le focus sur des sous-éléments via la navigation dans la liste peut être confus pour les utilisateurs et les outils d’accessibilité. Si le conteneur héberge une liste verticale d’éléments, le fait d’appuyer sur les touches haut et bas doit parcourir les éléments, mais le fait d’appuyer sur les touches de direction droite et gauche peut accéder aux sous-éléments de l’élément ayant le focus, tels que les colonnes de liste ou les sous-éléments d’interface utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




