---
title: Window (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IWindowProvider, y compris des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle Window prend en charge des contrôles qui fournissent des fonctionnalités fondamentales basées sur les fenêtres dans une interface graphique utilisateur traditionnelle.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- UI Automation, implémenter le modèle de contrôle Window
- UI Automation, modèle de contrôle de fenêtre
- UI Automation, IWindowProvider
- IWindowProvider
- implémentation de modèles de contrôle de fenêtre UI Automation
- Modèles de contrôle de fenêtre
- modèles de contrôle, IWindowProvider
- modèles de contrôle, implémenter une fenêtre UI Automation
- modèles de contrôle, fenêtre
- interfaces, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192668"
---
# <a name="window-control-pattern"></a>Window (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), y compris des informations sur les propriétés, les méthodes et les événements. Le modèle de contrôle **Window** prend en charge des contrôles qui fournissent des fonctionnalités fondamentales basées sur les fenêtres dans une interface graphique utilisateur traditionnelle.

Voici des exemples de contrôles qui doivent implémenter ce modèle de contrôle : les fenêtres d’application de niveau supérieur, les fenêtres enfants de l’interface multidocument (MDI), les contrôles de volet de fractionnement redimensionnables, les boîtes de dialogue modales et les fenêtres d’aide de bulle. Pour obtenir des exemples de contrôles implémentant ce modèle de contrôle, consultez [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IWindowProvider**](#required-members-for-iwindowprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Window** , notez les conventions et recommandations suivantes :

-   Pour prendre en charge la possibilité de modifier à la fois la taille de la fenêtre et la position de l’écran à l’aide de Microsoft UI Automation, un contrôle doit implémenter [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) en plus de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Les contrôles qui contiennent des barres de titre et des éléments de barre de titre qui permettent de déplacer, redimensionner, agrandir, réduire ou fermer le contrôle sont généralement requis pour implémenter [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Les contrôles tels que les fenêtres contextuelles d’info-bulle et les menus déroulants de zone de liste déroulante ou de menu n’implémentent généralement pas [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).
-   Les fenêtres d’aide de la bulle se distinguent des info-bulles de base des info-bulles par l’approvisionnement d’un bouton **Fermer** semblable à une fenêtre.
-   Le mode plein écran n’est pas pris en charge par [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , car il est propre aux fonctionnalités d’une application et n’est pas un comportement de fenêtre typique.

## <a name="required-members-for-iwindowprovider"></a>Membres requis pour **IWindowProvider**

Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .



| Membres nécessaires                                                                            | Type de membre | Notes                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**WindowInteractionState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | Propriété    | Il n’est pas garanti que **WindowInteractionState \_ ReadyForUserInteraction** |
| [**IsModal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | Propriété    | None                                                                        |
| [**IsTopmost**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | Propriété    | None                                                                        |
| [**CanMaximize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | Propriété    | None                                                                        |
| [**CanMinimize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | Propriété    | None                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | Propriété    | None                                                                        |
| [**Plus**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | Méthode      | None                                                                        |
| [**SetVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | Méthode      | None                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | Méthode      | None                                                                        |
| [**\_Fenêtre UIA \_ WindowClosedEventId**](uiauto-event-ids.md) | Événement       | None                                                                        |
| [**\_Fenêtre UIA \_ WindowOpenedEventId**](uiauto-event-ids.md) | Événement       | None                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Mappage de modèle de contrôle pour les clients UI Automation](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




