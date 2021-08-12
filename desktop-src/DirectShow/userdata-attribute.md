---
description: L’attribut UserData spécifie les données persistantes définies par l’application pour un objet.
ms.assetid: 7f1390be-93d4-440f-8b46-57a6a3e0e2a1
title: UserData (attribut)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f25b9293781fe89618e7e0db7359f8a7bfbc002f2c2a057314827bdf876262b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651203"
---
# <a name="userdata-attribute"></a>UserData (attribut)

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

L' `userdata` attribut spécifie les données persistantes définies par l’application pour un objet.

## <a name="possible-values"></a>Valeurs possibles

La valeur doit être un nombre hexadécimal avec un nombre pair de chiffres. Les valeurs A-F doivent être en majuscules. N’utilisez pas de préfixe tel que 0x. Exemple : 123ABC.

## <a name="applies-to"></a>S'applique à

[**clip**](clip-element.md), [**composite**](composite-element.md), [**Effect**](effect-element.md), [**Group**](group-element.md), [**Timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Attributs XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetUserData**](iamtimelineobj-setuserdata.md)
</dt> </dl>

 

 



