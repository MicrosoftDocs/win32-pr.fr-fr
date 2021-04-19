---
title: Modèle de contrôle SelectionItem
description: Fournit des instructions et des conventions pour l’implémentation de ISelectionItemProvider, y compris des informations sur les propriétés, les méthodes et les événements.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- UI Automation, implémentation du modèle de contrôle SelectionItem
- UI Automation, modèle de contrôle SelectionItem
- UI Automation, ISelectionItemProvider
- ISelectionItemProvider
- implémentation des modèles de contrôle SelectionItem d’UI Automation
- Modèles de contrôle SelectionItem
- modèles de contrôle, ISelectionItemProvider
- modèles de contrôle, implémenter des SelectionItem UI Automation
- modèles de contrôle, SelectionItem
- interfaces, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511204"
---
# <a name="selectionitem-control-pattern"></a>Modèle de contrôle SelectionItem

Fournit des instructions et des conventions pour l’implémentation de [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), y compris des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle **SelectionItem** est utilisé pour prendre en charge les contrôles qui agissent en tant qu’éléments enfants individuels et sélectionnables de contrôles conteneurs qui implémentent [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ISelectionItemProvider**](#required-members-for-iselectionitemprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **SelectionItem** , notez les conventions et recommandations suivantes :

-   Les contrôles à sélection unique qui gèrent des contrôles enfants qui implémentent [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), tels que le curseur **résolution d’écran** dans la boîte de dialogue des **propriétés d’affichage** pour Windows, doivent implémenter [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); leurs enfants doivent implémenter à la fois [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) et [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

## <a name="required-members-for-iselectionitemprovider"></a>Membres requis pour **ISelectionItemProvider**

Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .



| Membres nécessaires                                                                                                                        | Type de membre | Notes |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**AddToSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | Méthode      | Aucun  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | Propriété    | Aucun  |
| [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | Méthode      | Aucun  |
| [**Sélectionner**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | Méthode      | Aucun  |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | Propriété    | Aucun  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)         | Événement       | Aucun  |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | Événement       | Aucun  |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | Événement       | Aucun  |



 

Si le résultat d’une [**sélection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), d' [**un AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)ou d’un [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) est un élément sélectionné unique, un événement **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) doit être déclenché ; sinon, déclenchez les événements **ElementAddedToSelection** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) ou **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) selon le cas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




