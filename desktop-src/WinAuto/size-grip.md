---
title: Poignée de dimensionnement (référence des éléments d’interface utilisateur MSAA)
description: La poignée de dimensionnement est un pointeur de souris spécial dans le coin inférieur droit d’une fenêtre qui permet à un utilisateur de cliquer et de faire glisser la poignée de dimensionnement pour redimensionner la fenêtre.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010620"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Poignée de dimensionnement (référence des éléments d’interface utilisateur MSAA)

La poignée de dimensionnement est un pointeur de souris spécial dans le coin inférieur droit d’une fenêtre qui permet à un utilisateur de cliquer et de faire glisser la poignée de dimensionnement pour redimensionner la fenêtre.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

La poignée de dimensionnement prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

La poignée de dimensionnement prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                   | Commentaires                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | La propriété **Description** est « peut être utilisée pour redimensionner la largeur et la hauteur d’une fenêtre ».                                                                                   |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | La propriété **Name** est « Size Box ».                                                                                                                                   |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | Fenêtre qui contient la poignée de dimensionnement.                                                                                                                                |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | La propriété **role** est [**la \_ \_ poignée du système de rôle**](object-roles.md).                                                                                  |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | La valeur de la propriété **State** est zéro, ce qui signifie que l’objet est visible, ou le [**système d’État est \_ \_ invisible**](object-state-constants.md). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




