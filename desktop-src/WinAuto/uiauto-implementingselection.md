---
title: Selection (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ISelectionProvider, y compris des informations sur les propriétés, les méthodes et les événements.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- UI Automation, implémenter le modèle de contrôle Selection
- UI Automation, modèle de contrôle Selection
- UI Automation, ISelectionProvider
- ISelectionProvider
- implémentation des modèles de contrôle Selection d’UI Automation
- Modèles de contrôle de sélection
- modèles de contrôle, ISelectionProvider
- modèles de contrôle, implémenter la sélection UI Automation
- modèles de contrôle, sélection
- interfaces, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029269"
---
# <a name="selection-control-pattern"></a>Selection (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), y compris des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle **Selection** est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants sélectionnables. Les enfants de cet élément doivent implémenter [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Selection** , notez les conventions et recommandations suivantes :

-   Les contrôles qui implémentent [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) autorisent la sélection d’un ou de plusieurs éléments enfants. Par exemple, les zones de liste, les affichages de liste et les arborescences prennent en charge les sélections multiples, alors que les zones de liste modifiable, les curseurs et les groupes de cases d’option prennent en charge la sélection unique
-   Les contrôles qui ont une plage minimale, maximale et continue, tels que le contrôle Slider **volume** d’un lecteur multimédia, doivent implémenter [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) au lieu de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).
-   Les contrôles à sélection unique qui gèrent des contrôles enfants qui implémentent [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), tels que le curseur **résolution d’écran** dans la boîte de dialogue des propriétés d' **affichage** pour Windows, ou le contrôle de sélection du **Sélecteur de couleurs** de Microsoft Word (Voir l’image suivante), doivent implémenter [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); leurs enfants doivent implémenter à la fois [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) et [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![image présentant un exemple de mappage de chaîne d’échantillons de couleurs](images/uia-valuepattern-colorpicker.jpg)

-   Les menus ne prennent pas en charge le modèle de contrôle **Selection** . Si vous utilisez des éléments de menu qui incluent à la fois des graphiques et du texte (tels que les éléments du **volet de visualisation** dans le menu **affichage** de Microsoft Outlook) et que vous devez communiquer l’État, vous devez implémenter [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Membres requis pour **ISelectionProvider**

Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .



| Membres nécessaires                                                                                | Type de membre | Notes                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Propriété    | Aucun                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Propriété    | Aucun                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Méthode      | Aucun                                                                        |
| [**\_InvalidatedEventId de sélection UIA \_**](uiauto-event-ids.md) | Événement       | Déclenchez cet événement lorsqu’une sélection dans un conteneur a changé de manière significative. |



 

Les propriétés [**ISelectionProvider :: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) et [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) peuvent être dynamiques. Par exemple, l’état initial d’un contrôle peut ne pas avoir d’éléments sélectionnés par défaut, ce qui indique que **IsSelectionRequired** a la valeur false. Toutefois, une fois qu’un élément a été sélectionné, le contrôle doit toujours avoir au moins un élément sélectionné. De la même façon, dans quelques cas rares, un contrôle peut autoriser la sélection de plusieurs éléments lors de l’initialisation, mais n’autoriser par la suite que des sélections uniques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Modèle de contrôle SelectionItem](uiauto-implementingselectionitem.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




