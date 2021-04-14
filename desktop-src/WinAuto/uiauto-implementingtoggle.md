---
title: Basculer le modèle de contrôle
description: Fournit des instructions et des conventions pour l’implémentation de IToggleProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Toggle est utilisé pour prendre en charge les contrôles qui peuvent parcourir un ensemble d’États et conserver un État une fois défini.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- UI Automation, implémenter le modèle de contrôle Toggle
- UI Automation, basculer le modèle de contrôle
- UI Automation, IToggleProvider
- IToggleProvider
- implémentation des modèles de contrôle Toggle d’UI Automation
- Activer/désactiver les modèles de contrôle
- modèles de contrôle, IToggleProvider
- modèles de contrôle, implémenter le basculement d’UI Automation
- modèles de contrôle, bascule
- interfaces, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379755"
---
# <a name="toggle-control-pattern"></a>Basculer le modèle de contrôle

Fournit des instructions et des conventions pour l’implémentation de [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **Toggle** est utilisé pour prendre en charge les contrôles qui peuvent parcourir un ensemble d’États et conserver un État une fois défini.

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IToggleProvider**](#required-members-for-itoggleprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Toggle** , notez les conventions et recommandations suivantes :

-   Les contrôles qui ne conservent pas l’État lorsqu’ils sont activés, tels que les boutons, les boutons de barre d’outils et les liens hypertexte, doivent implémenter [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) à la place.
-   Un contrôle doit parcourir ses États de basculement ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) dans l’ordre suivant : **ToggleState \_ sur**, **ToggleState \_ off** et, s’il est pris en charge, **ToggleState \_ indéterminé**.
-   L’option **bascule** ne fournit pas de méthode d’état défini en raison de problèmes liés à la configuration directe d’une case à cocher à trois États sans parcourir sa séquence [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) appropriée.
-   Le contrôle de case d’option n’implémente pas [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), car il n’est pas en mesure de parcourir ses États valides.

## <a name="required-members-for-itoggleprovider"></a>Membres requis pour **IToggleProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .



| Membres nécessaires                                          | Type de membre | Notes |
|-----------------------------------------------------------|-------------|-------|
| [**Bascule**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | Méthode      | Aucun  |
| [**ToggleState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | Propriété    | Aucun  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




