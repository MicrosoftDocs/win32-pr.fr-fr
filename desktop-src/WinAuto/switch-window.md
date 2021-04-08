---
title: Fenêtre de basculement (référence des éléments d’interface utilisateur MSAA)
description: La fenêtre commutateur s’affiche chaque fois qu’un utilisateur appuie sur ALT + TAB pour basculer vers une autre application. La fenêtre commutateur contient une icône pour chaque application en cours d’exécution.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675618"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Fenêtre de basculement (référence des éléments d’interface utilisateur MSAA)

La fenêtre commutateur s’affiche chaque fois qu’un utilisateur appuie sur ALT + TAB pour basculer vers une autre application. La fenêtre commutateur contient une icône pour chaque application en cours d’exécution.

Le nom de classe de fenêtre pour la fenêtre de commutateur est « \# 32771 ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

La fenêtre commutateur prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Méthode                                                                    | Commentaires                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | L’objet de fenêtre de commutateur lui-même n’a pas de propriété **DefaultAction** . La méthode [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) pour chaque élément de la fenêtre Switch active l’élément spécifié. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Propriétés IAccessible

La fenêtre commutateur prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                           |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | L’objet de fenêtre de commutateur lui-même n’a pas de propriété **DefaultAction** . La propriété **DefaultAction** pour chaque élément de la fenêtre commutateur est « Switch ».                                                                     |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | L’objet parent de la fenêtre de basculement ne peut pas recevoir le focus. Seuls les enfants individuels peuvent recevoir le focus.                                                                                                                          |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | L’objet de fenêtre de commutateur lui-même n’a pas de propriété **Name** . La propriété **nom** de chaque icône d’application dans la fenêtre commutateur est la même que le nom de l’application affichée.                                         |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | L’objet de fenêtre de commutateur lui-même a une propriété **role** « Window \[ 32771 \] ». En outre, chaque icône d’application dans la fenêtre commutateur a la propriété **role** [**ListItem du \_ système \_ de rôle**](object-roles.md). |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | L’objet de fenêtre de commutateur lui-même ne prend pas en charge la propriété **State** . La valeur d' **État** pour les éléments de la vue liste est le [**focus du \_ système \_ d’État**](object-state-constants.md).                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




