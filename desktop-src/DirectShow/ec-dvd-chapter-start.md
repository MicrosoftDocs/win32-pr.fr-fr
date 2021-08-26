---
description: Signale que le lecteur de DVD a commencé la lecture d’un nouveau programme dans le \_ domaine du nom du domaine DVD \_ .
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9570964efa52380c06034716f0c199cde0498a2c0aeb0502f9db250f87a6ca3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998099"
---
# <a name="ec_dvd_chapter_start"></a>\_début du \_ chapitre du DVD EC \_

Signale que le lecteur de DVD a commencé la lecture d’un nouveau programme dans le \_ domaine du nom du domaine DVD \_ .

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** indiquant le nouveau numéro de chapitre (programme).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

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
</dt> <dt>

[**\_Énumération de domaine DVD**](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




