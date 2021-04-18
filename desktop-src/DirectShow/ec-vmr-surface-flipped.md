---
description: Envoyé lorsque l’exlocateur VMR-7's a appelé la méthode de retournement DirectDraw sur la surface qui est présentée. Cela permet à VMR de conserver sa table de surfaces DirectXVA synchronisée avec la chaîne de retournement de DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526740"
---
# <a name="ec_vmr_surface_flipped"></a>\_surface EC \_ VMR \_ retournée

Envoyé lorsque l’exlocateur VMR-7's a appelé la méthode de retournement DirectDraw sur la surface qui est présentée. Cela permet à VMR de conserver sa table de surfaces DirectXVA synchronisée avec la chaîne de retournement de DirectDraw.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Code d’état retourné par la méthode de retournement DirectDraw.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Les exlocateurs personnalisés-présentateurs pour VMR-7 doivent envoyer cet événement. Cet événement n’est pas transféré aux applications et n’est pas utilisé avec Allocator-Presenters pour VMR-9.

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

 

 




