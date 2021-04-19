---
description: L’attribut UserData spécifie les données persistantes définies par l’application pour un objet.
ms.assetid: 7f1390be-93d4-440f-8b46-57a6a3e0e2a1
title: UserData (attribut)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4828e378bcdafddbf83b3676e0941c8a1a066cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521813"
---
# <a name="userdata-attribute"></a>UserData (attribut)

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

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

 

 



