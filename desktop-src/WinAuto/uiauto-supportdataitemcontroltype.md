---
title: DataItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- UI Automation, prise en charge du type de contrôle DataItem
- UI Automation, type de contrôle DataItem
- UI Automation, arborescence pour le type de contrôle DataItem
- UI Automation, propriétés du type de contrôle DataItem
- UI Automation, modèles de contrôle pour le type de contrôle DataItem
- UI Automation, événements pour le type de contrôle DataItem
- UI Automation, grandes listes et le type de contrôle DataItem
- arborescences, type de contrôle DataItem
- Propriétés, DataItem (type de contrôle)
- modèles de contrôle, type de contrôle DataItem
- événements, type de contrôle DataItem
- grandes listes
- prise en charge du type de contrôle DataItem
- DataItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle DataItem
- types de contrôles, modèles de contrôle pour le type de contrôle DataItem
- types de contrôles, listes de grande taille et type de contrôle DataItem
- types de contrôles, prise en charge de DataItem
- types de contrôles, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49840dbe2aeed9200ebf02b80e270cd8fa3e0747
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122597"
---
# <a name="dataitem-control-type"></a>DataItem (type de contrôle)

Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **DataItem** .

Une entrée dans une liste de contacts est un exemple de contrôle d’élément de données. Un contrôle d’élément de données contient des informations intéressantes pour l’utilisateur final. Il est plus complexe que l’élément de liste simple, car il contient des informations plus détaillées.

Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **DataItem** . Les exigences d’UI Automation s’appliquent à tous les contrôles d’élément de données où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.

Cette rubrique contient les sections suivantes.

-   [Structure d’arborescence classique](#typical-tree-structure)
-   [Propriétés pertinentes](#relevant-properties)
-   [Modèles de contrôle requis](#required-control-patterns)
-   [Utilisation de DataItems dans des listes volumineuses](#working-with-dataitems-in-large-lists)
-   [Événements obligatoires](#required-events)
-   [Exemple de type de contrôle DataItem](#dataitem-control-type-example)
-   [Rubriques connexes](#related-topics)

## <a name="typical-tree-structure"></a>Structure d’arborescence classique

Le tableau suivant représente un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’élément de données et décrit ce que peut contenir chaque vue. Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).




| Affichage de contrôle | Affichage de contenu | 
|--------------|--------------|
| <ul><li>DataItem<ul><li>Selon le cas (0 ou plus. Peut être structuré dans une hiérarchie)</li></ul></li></ul> | <ul><li>DataItem<ul><li>Selon le cas (0 ou plus. Peut être structuré dans une hiérarchie)</li></ul></li></ul> | 




 

Un élément de données dans une grille de données peut héberger divers objets, notamment une autre couche d’éléments de données ou des éléments de grille spécifiques tels que du texte, des images ou des contrôles d’édition. Si l’élément de données a un rôle d’objet spécifique, l’élément doit être exposé en tant que type de contrôle spécifique ; par exemple, un type de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) pour un élément de données sélectionnable dans la grille.

## <a name="relevant-properties"></a>Propriétés pertinentes

Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle DataItem. Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).



| Propriété UI Automation                                                                                              | Valeur        | Notes                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consultez les remarques.   | La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consultez les remarques.   | Rectangle externe qui contient l’ensemble du contrôle.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consultez les remarques.   | Pris en charge s’il existe un rectangle englobant. Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle d’élément de données doit toujours être du contenu.                                                                                                                                                        |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | Le contrôle d’élément de données doit toujours être un contrôle.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consultez les remarques.   | Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consultez les remarques.   | Si le contrôle contient l’État mis à jour dynamiquement, cette propriété doit être prise en charge afin qu’une technologie d’assistance puisse recevoir des mises à jour lorsque l’état de l’élément change.        |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Consultez les remarques.   | Il s’agit de la valeur de chaîne qui transmet à l’utilisateur final l’objet sous-jacent représenté par l’élément. Exemples : « fichier multimédia » et « contact ».                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | Les contrôles d’élément de données n’ont pas d’étiquette de texte statique.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consultez les remarques.   | Chaîne localisée correspondant au type de contrôle **DataItem** . La valeur par défaut est « Data Item » pour en-US ou anglais (États-Unis).                                                              |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consultez les remarques.   | Le contrôle d’élément de données contient toujours un élément de texte principal que l’utilisateur reconnaît comme identificateur pour l’élément.                                                                           |



 

## <a name="required-control-patterns"></a>Modèles de contrôle requis

Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’élément de données. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Modèle de contrôle                                                   | Support | Notes                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dépend | Si l’élément de données peut être développé ou réduit pour afficher et masquer des informations, le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) doit être pris en charge.                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Dépend | Les éléments de données prennent en charge le modèle de contrôle [GridItem](uiauto-implementinggriditem.md) quand une collection d’éléments de données est disponible dans un conteneur qui peut faire l’objet d’une navigation spatiale d’un élément à l’élément.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Dépend | Tous les éléments de données prennent en charge la possibilité de faire défiler la vue avec le modèle de contrôle [ScrollItem](uiauto-implementingscrollitem.md) quand leur conteneur de données contient plus d’éléments que l’écran ne peut en contenir.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dépend | La possibilité de sélectionner les éléments de données dépend du contenu.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Dépend | Si l’élément de données est contenu dans un type de contrôle [DataGrid](uiauto-supportdatagridcontroltype.md) qui a un élément d’en-tête, il doit prendre en charge le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) . |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dépend | Si l’élément de données contient un État qui peut être parcouru, il doit prendre en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) .                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dépend | Si le texte principal de l’élément de données est modifiable, le modèle de contrôle [value](uiauto-implementingvalue.md) doit être pris en charge.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Utilisation de DataItems dans des listes volumineuses

Étant donné que les listes volumineuses sont souvent virtualisées dans des infrastructures d’interface utilisateur pour aider à améliorer les performances, un client UI Automation ne peut pas utiliser la fonctionnalité de requête UI Automation pour rechercher le contenu de l’arborescence complète de la même façon que dans d’autres conteneurs d’éléments. Un client doit faire défiler l’élément dans l’affichage (ou développer le contrôle pour afficher toutes les options disponibles) avant d’accéder à l’ensemble complet d’informations de l’élément de données.

lors de l’appel de [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) sur l’élément UI Automation pour l’élément de données, Microsoft Windows Explorer retourne avec succès et fait en sorte que le focus soit défini sur le contrôle d’édition dans la sous-arborescence d’éléments de données.

## <a name="required-events"></a>Événements obligatoires

Le tableau suivant répertorie les événements UI Automation que les contrôles d’élément de données doivent prendre en charge. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).



| Événement UI Automation                                                                                                                                                | Notes                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId. | Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.                                              | Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.                                          | Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété ItemStatusPropertyId.                                            | Si le contrôle prend en charge la propriété [**ItemStatus**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.        |
| [**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.                                 | Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.                 |
| [**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.                                               | Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.                   |



 

## <a name="dataitem-control-type-example"></a>Exemple de type de contrôle DataItem

L’image suivante illustre un type de contrôle DataItem dans un contrôle List-View.

![capture d’écran du contrôle List-View avec le type de contrôle DataItem](images/dataitemxmpl.jpg)

L’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation relative au contrôle d’élément de données sont affichés ci-dessous. Les modèles de contrôle de chaque élément Automation sont indiqués entre parenthèses. Le **groupe** « contoso » fait également partie de la grille du contrôle hôte de grille de données. Pour obtenir un exemple d’une structure de grille de niveau supérieur, consultez [type de contrôle DataGrid](uiauto-supportdatagridcontroltype.md).




| Arborescence UI Automation-vue de contrôle | Arborescence UI Automation-affichage du contenu | 
|-----------------------------------|-----------------------------------|
| <ul><li>Groupe "Contoso" (Table, Grid)<ul><li>DataItem "Accounts Receivable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>Image "Accounts Receivable.doc"</li><li>Edit "Name" (TableItem, GridItem, Value "Accounts Receivable.doc")</li><li>Edit "Date modified" (TableItem, GridItem, Value "25/08/2006 15:29")</li><li>Modifiez « Size » (GridItem, TableItem, value « 11,0 Ko »)</li></ul></li><li>DataItem "Accounts Payable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>...</li></ul></li></ul></li></ul> | <ul><li>Groupe "Contoso" (Table, Grid)<ul><li>DataItem "Accounts Receivable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>Image "Accounts Receivable.doc"</li><li>Edit "Name" (TableItem, GridItem, Value "Accounts Receivable.doc")</li><li>Edit "Date modified" (TableItem, GridItem, Value "25/08/2006 15:29")</li><li>Modifiez « Size » (GridItem, TableItem, value « 11,0 Ko »)</li></ul></li><li>DataItem "Accounts Payable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>...</li></ul></li></ul></li></ul> | 




 

Si une grille représente une liste d’éléments sélectionnables, les éléments d’interface utilisateur sélectionnables correspondants peuvent être exposés avec le type de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) au lieu du type de contrôle DataItem. Dans l’exemple précédent, les éléments **DataItem** (« accounts Receivable.doc » et « accounts Payable.doc ») sous **Group** (« contoso ») peuvent être améliorés en les exposant en tant que types de contrôle ListItem, car ce type prend déjà en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble d'UI Automation](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




