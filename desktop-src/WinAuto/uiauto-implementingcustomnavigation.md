---
title: Modèle de contrôle CustomNavigation
description: Fournit des instructions et des conventions pour implémenter l’interface ICustomNavigationProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196721"
---
# <a name="customnavigation-control-pattern"></a>Modèle de contrôle CustomNavigation

Fournit des instructions et des conventions pour implémenter l’interface **ICustomNavigationProvider** , y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **CustomNavigation** est utilisé pour activer la navigation personnalisée entre des contrôles dans des structures de type hiérarchie, telles que des éléments de liste, des listes à puces, des listes numérotées et des en-têtes. Cela permet aux fournisseurs de décrire des structures ou de définir les relations navigables à l’aide de l’élément seul et pas seulement du contrôle conteneur.

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ICustomNavigationProvider**](#required-members-for-icustomnavigationprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le fournisseur **CustomNavigation** , notez les conventions et recommandations suivantes :

-   Les valeurs de propriété pour **PositionInSet**, **SizeOfSet** et **Level** sont des valeurs entières basées sur un.
-   **ICustomNavigationProvider** ne fournit pas de manipulation active du contrôle, comme déplacer des positions, ajouter et supprimer des éléments, ou promouvoir et rétrograder des niveaux.
-   Les contrôles qui implémentent **ICustomNavigationProvider** ont généralement une structure hiérarchique, mais peuvent ignorer des niveaux à l’aide de la méthode **Navigate** . Les propriétés **PositionInSet**, **SizeOfSet** et **Level** sont requises sur le modèle.

## <a name="required-members-for-icustomnavigationprovider"></a>Membres requis pour **ICustomNavigationProvider**

Les propriétés suivantes sont requises pour implémenter l’interface **ICustomNavigationProvider** .



| Membres nécessaires                                                                  | Type de membre | Notes                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [**CachedLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | Propriété    | Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | Propriété    | Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CachedSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | Propriété    | Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentLevel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | Propriété    | Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentPositionInSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | Propriété    | Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**CurrentSizeOfSet**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | Propriété    | Situé sur l’interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) . |
| [**Sélectionnez**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | Méthode      | Aucun                                                                                |



 

Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[ListItem, contrôle](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[Contrôle HeaderItem](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[DataItem, contrôle](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




