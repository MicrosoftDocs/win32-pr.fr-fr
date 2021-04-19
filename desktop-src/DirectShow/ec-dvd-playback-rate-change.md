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
ms.openlocfilehash: 20ddc41fd70906fabc522daa4dcb7714b71e4251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537442"
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

## <a name="remarks"></a>Notes

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

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




