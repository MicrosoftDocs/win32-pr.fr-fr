---
description: Signale le début de chaque unité d’objet vidéo (VOBU), un segment vidéo d’une longueur de 0,4 à 1,0 secondes.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: f72f49fde761418417b198787ef1b67d654f114f57fcd29bd7aa7edfae4b1e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997999"
---
# <a name="ec_dvd_current_time"></a>\_ \_ heure actuelle du DVD EC \_

Signale le début de chaque unité d’objet vidéo (VOBU), un segment vidéo d’une longueur de 0,4 à 1,0 secondes.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** qui indique le code temporel de lecture actuel dans une mise en forme binaire codée binaire (BCD), minutes, secondes, frames (hh : mm : SS : FF). Membre de la structure du [**\_ code temporel du DVD**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur booléenne (**bool**) indiquant le code temporel. Zéro (0) indique 25 images par seconde, tandis que 1 indique 30 images par seconde (non supprimées). La valeur 2 indique que l’heure de lecture ne peut pas être déterminée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Seuls les films linéaires simples signalent cet événement.

Cet événement est déclenché dans le domaine de titre.

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

 

 




