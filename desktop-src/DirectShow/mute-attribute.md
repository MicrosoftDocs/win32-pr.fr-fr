---
description: L’attribut muet spécifie l’État muet de l’objet.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Attribut muet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d89632e632ec4dbf0fe76a915e073baa769044fa1eaad455c16dd3065dc1c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791039"
---
# <a name="mute-attribute"></a>Attribut muet

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `mute` attribut spécifie l’État muet de l’objet. Si la valeur est **true**, l’objet et ses enfants ne sont pas rendus. Si la valeur est **false**, l’objet est rendu et ses enfants sont rendus en fonction de leur propre État muet. La valeur par défaut est **FALSE**.

## <a name="possible-values"></a>Valeurs possibles

Les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1. Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).

## <a name="applies-to"></a>S'applique à

[**clip**](clip-element.md), [**composite**](composite-element.md), [**Effect**](effect-element.md), [**Group**](group-element.md), [**Timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



