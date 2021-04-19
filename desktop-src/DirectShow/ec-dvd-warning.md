---
description: Signale une condition d’avertissement de DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540202"
---
# <a name="ec_dvd_warning"></a>\_avertissement de DVD EC \_

Signale une condition d’avertissement de DVD.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** indiquant la condition d’avertissement. Membre du type de données énuméré de l' [**\_ Avertissement DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *pParam1* est égal à l' \_ Avertissement DVD \_ ouvert, à la recherche d’avertissement sur le DVD \_ \_ ou \_ à l’avertissement de DVD \_ lu, *LParam2* contient le dernier code d’erreur retourné par **GetLastError**.

</dd> </dl>

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

 

 




