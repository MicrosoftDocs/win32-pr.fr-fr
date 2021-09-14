---
description: Signale que le numéro de flux audio actuel a changé pour le titre principal du DVD.
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999165"
---
# <a name="ec_dvd_audio_stream_change"></a>\_modification du \_ \_ flux audio du DVD \_ EC

Signale que le numéro de flux audio actuel a changé pour le titre principal du DVD.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valeur **DWORD** indiquant le nouveau numéro de flux audio de l’utilisateur. Les numéros de flux audio sont compris entre 0 et 7. Stream 0xFFFFFFFF indique qu’aucun flux n’est sélectionné.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="remarks"></a>Notes

Le flux audio actuel peut changer automatiquement à l’aide d’une commande de navigation créée sur le disque, ainsi que via le contrôle d’application à l’aide de l’interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Cet événement est déclenché dans tous les domaines.

## <a name="requirements"></a>Spécifications



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

 

 




