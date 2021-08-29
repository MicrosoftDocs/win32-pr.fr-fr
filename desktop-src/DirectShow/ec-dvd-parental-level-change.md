---
description: Signale que le niveau parental du contenu DVD créé va être modifié.
ms.assetid: c6817e1a-f860-4ba2-9e0f-e195624230c5
title: EC_DVD_PARENTAL_LEVEL_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PARENTAL_LEVEL_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f990e8441cd6585d30a9876204f07099345f22f49895d4d429655405d498ed63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102929"
---
# <a name="ec_dvd_parental_level_change"></a>\_modification du \_ \_ niveau parental du DVD \_ EC

Signale que le niveau parental du contenu DVD créé va être modifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur de type LONG représentant le nouveau niveau parental défini dans le lecteur.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le filtre de [navigateur DVD](dvd-navigator-filter.md) ne prend pas en charge les modifications de niveau parental pendant la diffusion en continu en réponse aux commandes SetTmpPML sur un disque DVD.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdevcode. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> <dt>

[Codes de notification des événements DVD](dvd-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




