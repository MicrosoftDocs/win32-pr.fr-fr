---
title: Utilisation d’éléments virtualisés
description: Cette rubrique explique comment utiliser les fonctionnalités fournies par les modèles de contrôle ItemContainer et VirtualizedItem pour rechercher et récupérer des informations sur les éléments virtualisés.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- clients, éléments virtualisés UI Automation
- clients, éléments virtualisés
- clients, modèles de contrôle
- clients, modèles de contrôle VirtualizedItem
- clients, modèles de contrôle ItemContainer
- clients, modèles de contrôle VirtualizedItem UI Automation
- clients, modèles de contrôle UI Automation
- clients, modèles de contrôle ItemContainer UI Automation
- UI Automation, éléments virtualisés
- UI Automation, modèles de contrôle
- UI Automation, modèles de contrôle VirtualizedItem
- UI Automation, modèles de contrôle ItemContainer
- Modèles de contrôle VirtualizedItem
- Modèles de contrôle ItemContainer
- modèles de contrôle, VirtualizedItem
- modèles de contrôle, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb29232b06304079ad5b9dfdfb589ad510a5b51f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416135"
---
# <a name="working-with-virtualized-items"></a>Utilisation d’éléments virtualisés

Cette rubrique explique comment utiliser les fonctionnalités fournies par les modèles de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) et [VirtualizedItem](uiauto-implementingvirtualizeditem.md) pour rechercher et récupérer des informations sur les éléments virtualisés.

-   [Vue d’ensemble de la virtualisation](#overview-of-virtualization)
-   [Comment un contrôle prend en charge la virtualisation](#how-a-control-supports-virtualization)
-   [Comment les clients recherchent et réalisent des éléments virtualisés](#how-clients-find-and-realize-virtualized-items)
-   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-virtualization"></a>Vue d’ensemble de la virtualisation

Les contrôles qui contiennent un grand nombre d’éléments enfants peuvent utiliser la virtualisation pour gérer efficacement les éléments. Avec la virtualisation, le contrôle conserve les informations complètes en mémoire pour un sous-ensemble d’éléments à un moment donné. En règle générale, le sous-ensemble comprend uniquement les éléments qui sont actuellement visibles pour l’utilisateur. Les informations complètes sur les autres éléments virtualisés sont conservées dans le stockage et sont chargées en mémoire, ou réalisées, car le contrôle en a besoin, par exemple, lorsque de nouveaux éléments sont visibles par l’utilisateur.

Les contrôles qui utilisent la virtualisation représentent un défi, car seuls les éléments réalisés sont entièrement disponibles sous forme d’éléments Microsoft UI Automation dans l’arborescence UI Automation. Les éléments virtualisés n’existent pas dans l’arborescence, donc les informations les concernant ne sont pas disponibles pour les clients. Pour récupérer des informations sur les éléments virtualisés, les clients ont besoin d’un moyen de forcer l’automatisation de l’interface utilisateur à transmettre la demande pour réaliser les éléments du contrôle. Une fois les éléments réalisés, UI Automation peut créer des éléments UI Automation pour eux. UI Automation comprend deux modèles de contrôle pour permettre aux clients de travailler avec des éléments virtualisés : [ItemContainer](uiauto-implementingitemcontainer.md) et [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Comment un contrôle prend en charge la virtualisation

Tout contrôle pouvant contenir des éléments virtualisés doit prendre en charge le modèle de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) . En outre, tout élément qui peut être virtualisé doit prendre en charge le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Les fonctionnalités exposées par les modèles de contrôle ItemContainer et VirtualizedItem sont accessibles aux clients via les interfaces [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) et [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

## <a name="how-clients-find-and-realize-virtualized-items"></a>Comment les clients recherchent et réalisent des éléments virtualisés

Les clients peuvent utiliser la méthode [**IUIAutomationItemContainerPattern :: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) pour rechercher des éléments enfants dans le conteneur en fonction de la valeur d’une propriété particulière. La méthode peut également récupérer le premier élément dans le conteneur ou l’élément qui suit l’élément spécifié. Si un élément enfant correspondant est trouvé, **FindItemByProperty** récupère une interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour l’élément. Toutefois, si l’élément enfant est virtualisé, l’interface **IUIAutomationElement** est un espace réservé. L’erreur [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) se produit lorsque le client tente d’utiliser l’interface **IUIAutomationElement** pour récupérer des valeurs de propriété ou appeler des méthodes qui ne sont pas encore disponibles. Les propriétés ou méthodes disponibles via un espace réservé dépendent de l’implémentation du contrôle. La seule exigence pour un espace réservé consiste à prendre en charge l’interface [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) .

L’erreur [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) indique au client qu’un élément peut être virtualisé. Le client doit répondre en récupérant l’interface [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) pour l’élément, puis en réalisant l’élément en appelant la méthode [**IUIAutomationVirtualizedItemPattern :: réalise**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) . Si cela se déroule correctement, l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) est entièrement fonctionnelle avec toutes les propriétés appropriées disponibles.

En fonction de l’implémentation du contrôle, l’appel de [**IUIAutomationVirtualizedItemPattern ::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) provision peut entraîner le défilement de l’élément par le contrôle. Toutefois, un client ne doit pas s’appuyer sur l’élément qui fait défiler l’affichage ou le rendre visible. Pour vous assurer que l’élément est visible, le client peut utiliser la méthode [**IUIAutomationScrollItemPattern :: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) .

## <a name="example"></a>Exemple

Pour obtenir un exemple de code qui montre comment utiliser la prise en charge d’UI Automation pour la virtualisation, consultez [Comment récupérer un élément virtualisé](uiauto-howto-retrieve-virtualized-item.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




