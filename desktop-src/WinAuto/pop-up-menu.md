---
title: Menu contextuel (référence des éléments d’interface utilisateur MSAA)
description: Un menu contextuel affiche une liste de commandes de menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840381"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a>Menu contextuel (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets **menu contextuel** à des fins de référence des éléments d’interface utilisateur MSAA. La procédure de création d’objets de **menu contextuel** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un menu contextuel affiche une liste de commandes de menu. Microsoft Active Accessibility crée un objet menu contextuel lorsqu’un élément de menu est ouvert dans une barre de menus. Microsoft Active Accessibility crée également des objets menus contextuels pour les menus contextuels, qui s’affichent quand l’utilisateur clique avec le bouton droit sur un élément d’interface utilisateur.

Le nom de la classe de fenêtre d’un menu contextuel est « \# 32768 ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un menu contextuel prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un menu contextuel prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Récupère le [**IDispatch**](idispatch-interface.md) pour l’élément de menu spécifié. Les ID enfants pour les éléments de menu sont numérotés séquentiellement de haut en bas à partir de 1.                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propriété **ChildCount** est le nombre d’éléments de menu dans le menu, y compris les séparateurs de menu.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propriété **Name** d’un menu contextuel est le même nom que le menu. La propriété **Name** d’un menu contextuel est « context ».                                                                                                                                                                                                                                                                                                                                              |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propriété **parent** est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le menu contextuel et qui possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le menu contextuel.                                                                                                                                                                                                                                                      |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété **role** est le [**système de rôle \_ \_ MENUPOPUP**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notes

-   Les objets de menu contextuel ne déclenchent pas les événements de [**\_ \_ création**](event-constants.md) d’objet d’événement et de [**\_ \_ destruction d’objet d’événement**](event-constants.md) .
-   Les menus à plusieurs colonnes ne prennent pas en charge les indicateurs [**NAVDIR \_ Left**](navigation-constants.md) ou [**NAVDIR \_ Right**](navigation-constants.md) de la méthode [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .
-   Les événements [**du \_ système \_**](event-constants.md) d’événements MENUPOPUPSTART et du système d’événements [**\_ \_ MENUPOPUPEND**](event-constants.md) ne sont pas envoyés de manière cohérente. Il s’agit d’un problème connu qui est traité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barre de menus**](menu-bar.md)
</dt> <dt>

[**Élément de menu**](menu-item.md)
</dt> </dl>

 

 





