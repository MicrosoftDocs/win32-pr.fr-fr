---
description: Indique que le navigateur DVD a commencé à exécuter ou à terminer de relire les données karaoké.
ms.assetid: 910bf809-a56a-4d02-9c7e-429769a4ec2b
title: EC_DVD_KARAOKE_MODE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_KARAOKE_MODE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4edbdb337c4b57a7ed09bd63a8ed4fb0d1946b289b369badab64b561000d3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928569"
---
# <a name="ec_dvd_karaoke_mode"></a>\_ \_ mode karaoké du DVD EC \_

Indique que le [navigateur DVD](data-flow-in-the-dvd-navigator.md) a commencé à exécuter ou à terminer de relire les données karaoké.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur booléenne. Si la **valeur est true**, une piste de karaoké est lue. Dans le cas contraire, aucune piste karaoké n’est lue.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le lecteur DVD signale cet événement chaque fois qu’il modifie des domaines.

Cet événement est déclenché dans tous les domaines DVD.

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

 

 




