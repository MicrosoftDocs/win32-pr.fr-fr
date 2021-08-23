---
description: L’attribut Lock spécifie si un objet doit être modifié. Si la valeur est TRUE, l’application doit traiter l’objet comme étant verrouillé et interdire les modifications apportées à cet objet ou à ses enfants. La valeur par défaut est FALSE.
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: verrouiller l’attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdd1718c25aab136219af436543df064bd8f68bb53ea15b00e09e6a18188c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502319"
---
# <a name="lock-attribute"></a>verrouiller l’attribut

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `lock` attribut spécifie si un objet doit être modifié. Si la valeur est **true**, l’application doit traiter l’objet comme étant verrouillé et interdire les modifications apportées à cet objet ou à ses enfants. La valeur par défaut est **FALSE**.

## <a name="possible-values"></a>Valeurs possibles

Valeurs possibles les valeurs suivantes sont définies sur TRUE : y, Y, t, T, 1. Les valeurs suivantes sont définies avec la valeur FALSe : n, N, f, F, 0 (zéro).

## <a name="applies-to"></a>S'applique à

[**clip**](clip-element.md), [**composite**](composite-element.md), [**Effect**](effect-element.md), [**Group**](group-element.md), [**Timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetLocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



