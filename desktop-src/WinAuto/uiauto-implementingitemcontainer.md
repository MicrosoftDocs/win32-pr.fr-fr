---
title: Modèle de contrôle ItemContainer
description: Fournit des instructions et des conventions pour l’implémentation de IItemContainerProvider, y compris des informations sur les méthodes. Le modèle de contrôle ItemContainer est utilisé pour prendre en charge la virtualisation d’éléments.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- UI Automation, implémentation du modèle de contrôle ItemContainer
- UI Automation, modèle de contrôle ItemContainer
- UI Automation, IItemContainerProvider
- IItemContainerProvider
- implémentation des modèles de contrôle ItemContainer d’UI Automation
- Modèles de contrôle ItemContainer
- modèles de contrôle, IItemContainerProvider
- modèles de contrôle, implémenter des ItemContainer UI Automation
- modèles de contrôle, ItemContainer
- interfaces, IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69c0407a8f167a3a89b908c1b5555a9d32363b38b3ce5ab4d1794e726666a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413452"
---
# <a name="itemcontainer-control-pattern"></a>Modèle de contrôle ItemContainer

Fournit des instructions et des conventions pour l’implémentation de [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider), y compris des informations sur les méthodes. Le modèle de contrôle **ItemContainer** est utilisé pour prendre en charge la virtualisation d’éléments.

Les contrôles qui contiennent un grand nombre d’éléments enfants peuvent utiliser la virtualisation pour gérer efficacement les éléments. Avec la virtualisation, le contrôle conserve les informations complètes en mémoire pour un sous-ensemble d’éléments à un moment donné. En règle générale, le sous-ensemble comprend uniquement les éléments qui sont actuellement visibles pour l’utilisateur. Les informations complètes sur les autres éléments virtualisés sont conservées dans le stockage et sont chargées en mémoire, ou réalisées, car le contrôle en a besoin, par exemple, lorsque de nouveaux éléments sont visibles par l’utilisateur.

Par exemple, le diagramme suivant montre une zone de liste qui contient des milliers d’éléments virtualisés. Étant donné que le contrôle gère uniquement des informations complètes pour les éléments enfants qui sont actuellement visibles, le fournisseur peut exposer des éléments Microsoft UI Automation uniquement pour les éléments 100-127.

![Diagramme montrant les éléments d’une zone de liste virtualisés et non virtualisés](images/virtualizeditems.jpg)

Les contrôles qui utilisent la virtualisation représentent un défi, car seuls les éléments réalisés (dévirtualisés) sont entièrement disponibles en tant qu’éléments UI Automation dans l’arborescence UI Automation. Les éléments virtualisés n’existent pas dans l’arborescence, donc les informations les concernant ne sont pas disponibles.

Pour fournir des informations sur les éléments virtualisés, les fournisseurs implémentent le modèle de contrôle **ItemContainer** , qui expose l’interface [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) . La méthode [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) recherche des éléments enfants en fonction de la valeur d’une propriété particulière, telle que **Name**, **AutomationId** ou **IsSelected**. Si un élément est virtualisé, **FindItemByProperty** récupère un élément d’espace réservé UI Automation pour l’élément. Un élément d’espace réservé est une implémentation de l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) qui prend en charge uniquement le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

La méthode [**IVirtualizedItemProvider ::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) Complete permet à un client de demander qu’un élément virtualisé soit réalisé, exposant ainsi un élément UI Automation complet pour l’élément afin que toutes les propriétés et tous les modèles nécessaires soient disponibles.

Bien que l’objectif principal du modèle de contrôle **ItemContainer** est de prendre en charge les scénarios de conteneur virtualisés, il peut être implémenté par n’importe quel conteneur qui récupère des éléments enfants par nom, que le conteneur utilise ou non la virtualisation.

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **ItemContainer** , notez les conventions et recommandations suivantes :

-   Tout contrôle pouvant contenir des éléments virtualisés doit prendre en charge le modèle de contrôle **ItemContainer** . Tout conteneur qui prend en charge la récupération d’éléments en fonction d’une valeur de propriété peut prendre en charge ce modèle, que le conteneur utilise ou non la virtualisation.
-   Lorsqu’un conteneur est virtualisé, d’autres modèles de contrôles tels que la [sélection](uiauto-implementingselection.md), la [table](uiauto-implementingtable.md)et la [grille](uiauto-implementinggrid.md) peuvent être affectés. Par exemple, la méthode [**ISelectionProvider :: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) peut prendre en charge uniquement les éléments qui se trouvent dans la fenêtre d’affichage, ou uniquement les éléments sélectionnés qui ne sont pas virtualisés actuellement.
-   Le modèle de contrôle [Scroll](uiauto-implementingscroll.md) ne doit pas être affecté par la virtualisation.
-   Aucun nombre d’éléments ou aucune information d’index n’est disponible pour les éléments virtualisés. Un contrôle virtualisé peut utiliser la propriété **DescribedBy** ou **ItemStatus** pour fournir ces informations, si nécessaire.
-   Les développeurs de contrôles doivent documenter et publier les détails de toutes les propriétés UI Automation et les modèles de contrôle affectés par l’utilisation de la virtualisation. Bien que les modèles de contrôle ItemContainer et [VirtualizedItem](uiauto-implementingvirtualizeditem.md) offrent une prise en charge de base, ils peuvent ne pas prendre en charge certains comportements de virtualisation.

Les instructions et exigences suivantes s’appliquent à la méthode [**IItemContainerProvider :: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) .

-   Bien que cela ne soit pas obligatoire, Microsoft recommande vivement que [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) prenne en charge les propriétés **Name**, **AutomationId** et **IsSelected** .
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) peut être lent s’il doit parcourir plusieurs objets pour trouver un objet correspondant.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) peut être appelé à plusieurs reprises pour rechercher des éléments dans l’ordre. Les éléments peuvent être dans n’importe quel ordre tant que chaque élément n’est retourné qu’une seule fois.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) peut être implémenté pour rechercher uniquement les éléments qui apparaissent dans l’affichage de contrôle ou de contenu de l’arborescence UI Automation. Les éléments qui apparaissent uniquement dans l’affichage brut peuvent être ignorés pour éviter de récupérer plusieurs éléments qui représentent uniquement une partie d’un « élément » pour l’utilisateur.
-   Lorsque les critères de recherche correspondent à un élément virtualisé, le fournisseur peut retourner un élément d’espace réservé qui prend en charge le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Les indications suivantes s’appliquent aux éléments d’espace réservé :
    -   La récupération d’un élément d’espace réservé pour un élément virtualisé ne doit pas entraîner de modification de l’interface utilisateur.
    -   L’élément d’espace réservé doit être un homologue d’autres éléments enfants (un événement de modification de structure est requis).
    -   Lorsque cela est possible, le fournisseur peut créer un élément Automation complet au lieu d’un espace réservé.
-   Lorsque les critères de recherche correspondent à un élément non virtualisé, le fournisseur doit retourner l’élément réel, et non un espace réservé.
-   Quand aucun élément n’est trouvé, [**IItemContainerProvider :: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) doit définir le paramètre *PFound* sur la **valeur null** et retourner **S \_ OK**.
-   Lorsque le paramètre *PropertyId* a la valeur 0, le fournisseur doit retourner l’élément suivant après *pStartAfter*.
-   Si le paramètre *pStartAfter* est **null** et que *PropertyId* est égal à 0, le fournisseur doit retourner le premier élément dans le conteneur.
-   Lorsque le paramètre *PropertyId* est égal à 0, le paramètre value est ignoré.

Les indications et exigences suivantes s’appliquent aux éléments d’espace réservé pour les éléments virtualisés dans l’arborescence UI Automation.

-   Bien que les fournisseurs soient encouragés à prendre en charge un plus grand nombre de propriétés et de modèles de contrôle pour un élément d’espace réservé, seul le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) est requis.
-   Le fournisseur peut invalider un élément d’espace réservé précédent quand [**IItemContainerProvider :: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) est appelé à nouveau. (Si un client doit réaliser l’élément d’espace réservé, il doit le faire immédiatement ; sinon, l’élément peut être invalidé si **FindItemByProperty** est appelé à nouveau ou si la fenêtre d’affichage change pour une raison quelconque.)
-   Les actions d’interface utilisateur telles que le défilement ou le redimensionnement peuvent entraîner la modification de la fenêtre d’affichage du conteneur et l’affichage d’un nouvel ensemble d’éléments enfants. Dans ce cas, les éléments d’espace réservé précédemment récupérés peuvent ne pas être disponibles dans l’arborescence UI Automation.
-   Le fournisseur ne doit pas virtualiser les éléments d’interface utilisateur qui sont disponibles à l’écran dans la fenêtre d’affichage de l’objet conteneur.

## <a name="required-members-for-iitemcontainerprovider"></a>Membres requis pour IItemContainerProvider

La méthode suivante est requise pour l’implémentation de l’interface [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) .



| Membres nécessaires                                                               | Type de membre | Notes |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Méthode      | Aucun  |



 

Le modèle de contrôle **ItemContainer** n’a pas de propriétés ou d’événements associés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Modèle de contrôle VirtualizedItem](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




