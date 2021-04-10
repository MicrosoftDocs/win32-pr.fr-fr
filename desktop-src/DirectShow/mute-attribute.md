---
description: L’attribut muet spécifie l’État muet de l’objet.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Attribut muet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109434"
---
# <a name="mute-attribute"></a>Attribut muet

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

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

 

 



