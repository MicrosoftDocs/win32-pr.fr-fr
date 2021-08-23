---
description: Signale qu’une modification de la vitesse de lecture du DVD a été lancée.
ms.assetid: 2a1e3c21-1623-4e43-8c7b-1a34514442c9
title: EC_DVD_PLAYBACK_RATE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_RATE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8de40dc8fd7f70dda522f4d1faf34f8c05059c6928f80a141d7ac9ae1889ecec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823679"
---
# <a name="ec_dvd_playback_rate_change"></a>\_changement du \_ taux de lecture des DVD EC \_ \_

Signale qu’une modification de la vitesse de lecture du DVD a été lancée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur de type LONG indiquant le nouveau taux de lecture. La valeur est la vitesse de lecture réelle multipliée par 10 000, donc la vitesse de lecture est égale à 10000,0/ *lParam1*. Les valeurs inférieures à zéro indiquent le mode de lecture inversée, tandis que les valeurs supérieures à zéro indiquent le mode de lecture en avant.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cet événement est déclenché dans le domaine de titre.

La *Vitesse* de lecture est l’inverse de la vitesse *de lecture.* Par exemple, si la vitesse de lecture est 2x, le taux est de 0,5.

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

 

 




