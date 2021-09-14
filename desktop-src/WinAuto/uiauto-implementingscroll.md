---
title: Scroll (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IScrollProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Scroll est utilisé pour prendre en charge un contrôle qui agit comme un conteneur à défilement pour une collection d’objets enfants.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- UI Automation, implémenter le modèle de contrôle Scroll
- UI Automation, modèle de contrôle Scroll
- UI Automation, IScrollProvider
- IScrollProvider
- implémentation des modèles de contrôle Scroll d’UI Automation
- Modèles de contrôle Scroll
- modèles de contrôle, IScrollProvider
- modèles de contrôle, implémenter le défilement d’UI Automation
- modèles de contrôle, défilement
- interfaces, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010486"
---
# <a name="scroll-control-pattern"></a>Scroll (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **Scroll** est utilisé pour prendre en charge un contrôle qui agit comme un conteneur à défilement pour une collection d’objets enfants.

Le contrôle n’est pas obligatoire pour utiliser des barres de défilement pour prendre en charge la fonctionnalité de défilement, bien que cela le fasse couramment. L’illustration suivante montre un contrôle de défilement qui n’utilise pas de barres de défilement. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

![capture d’écran montrant un contrôle de défilement sans barres de défilement](images/uia-scrollpattern-without-scrollbars.jpg)

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IScrollProvider**](#required-members-for-iscrollprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Scroll** , notez les conventions et recommandations suivantes :

-   Les enfants de ce contrôle doivent implémenter [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).
-   Les barres de défilement d’un contrôle conteneur ne prennent pas en charge le modèle de contrôle **Scroll** . Ils doivent prendre en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) à la place.
-   Lorsque le défilement est mesuré sous forme de pourcentage, toutes les valeurs ou quantités liées à la graduation du défilement doivent être normalisées dans une plage de 0 à 100.
-   La propriété [**IScrollProvider :: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) et la propriété [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) sont indépendantes de la propriété **IsEnabled** .
-   Si la [**propriété IScrollProvider :: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) a la **valeur false**, la propriété [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) doit avoir la valeur 100 (100%) et la propriété [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) la valeur **UIA \_ ScrollPatternNoScroll** (-1). De même, si la propriété [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) a la **valeur false**, la propriété [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) doit avoir la valeur 100 (100%) et la propriété [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) la valeur **UIA \_ ScrollPatternNoScroll** (-1). Cela permet à un client Microsoft UI Automation d’utiliser ces valeurs de propriété dans la méthode [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) tout en évitant une condition de concurrence critique si une direction dans laquelle le client n’est pas intéressé par le défilement est activée.
-   La propriété [**IScrollProvider :: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) est spécifique aux paramètres régionaux. La définition de **HorizontalScrollPercent** sur 100 doit définir l’emplacement de défilement du contrôle sur l’équivalent de sa position la plus à droite pour les langues telles que l’anglais qui sont lues de gauche à droite. Sinon, pour les langues telles que l’arabe, qui sont lues de droite à gauche, la définition de **HorizontalScrollPercent** sur 100 doit définir l’emplacement de défilement à la position la plus à gauche.

## <a name="required-members-for-iscrollprovider"></a>Membres requis pour **IScrollProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .



| Membres nécessaires                                                                  | Type de membre | Notes |
|-----------------------------------------------------------------------------------|-------------|-------|
| [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | Propriété    | None  |
| [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | Propriété    | None  |
| [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | Propriété    | None  |
| [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | Propriété    | None  |
| [**HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | Propriété    | None  |
| [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | Propriété    | None  |
| [**Variable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | Méthode      | None  |
| [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | Méthode      | None  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




