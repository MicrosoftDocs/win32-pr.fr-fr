---
description: Envoyé par VMR-7 et VMR-9 lorsqu’il n’a pas pu accepter une demande de modification de format dynamique du décodeur en amont.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d29703d5ede068710966119f16c44a9e3637249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520936"
---
# <a name="ec_vmr_reconnection_failed"></a>échec de la \_ \_ reconnexion EC VMR \_

Envoyé par VMR-7 et VMR-9 lorsqu’il n’a pas pu accepter une demande de modification de format dynamique du décodeur en amont.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Code d’état retourné par [**IPIN :: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sur la broche d’entrée VMR qui n’a pas réussi la reconnexion.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet événement est transféré aux applications.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




