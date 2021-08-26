---
description: Signale l’heure actuelle, au \_ \_ format de code temporel DVD HMSF par rapport au début du titre. Cet événement est déclenché au début de chaque VOBU, qui se produit toutes les 0,4 à 1,0 secondes.
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: EC_DVD_CURRENT_HMSF_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 52a6eb077599b4fe6dfd89267974cb71c0c5a58a65d6c52307d77eb3e98201d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965809"
---
# <a name="ec_dvd_current_hmsf_time"></a>\_ \_ \_ temps HMSF actuel du \_ DVD

Signale l’heure actuelle, au format de [**\_ \_ code temporel DVD HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) par rapport au début du titre. Cet événement est déclenché au début de chaque VOBU, qui se produit toutes les 0,4 à 1,0 secondes.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur ULONG qui contient la structure du \_ \_ code temporel DVD HMSF. Affectez lParam1 à une variable ULONG, puis effectuez un cast de cette variable en un \_ \_ code temporel DVD HMSF pour accéder à ses valeurs.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valeur ULONG contenant une Union d' [**indicateurs de \_ code \_ temporel DVD**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).

</dd> </dl>

## <a name="remarks"></a>Remarques

Le \_ format de \_ code temporel DVD HMSF est destiné à remplacer l’ancien format BCD renvoyé dans les \_ \_ événements de temps courant du DVD \_ . Les codes temporels HMSF sont plus faciles à utiliser. Pour que le navigateur envoie les \_ \_ \_ \_ événements HMSF de temps du DVD en cours au lieu des \_ \_ événements temps courant du DVD \_ , une application doit appeler `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` . Lorsque cet indicateur est défini, le navigateur s’attend également à ce que tous les paramètres de temps dans les méthodes [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) et [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) soient passés comme des \_ \_ codes temporels de DVD HMSF.

Cet événement est déclenché dans les domaines de titre.

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

 

 




