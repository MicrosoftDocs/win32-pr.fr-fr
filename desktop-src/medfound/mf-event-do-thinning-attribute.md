---
description: Quand une source de média demande un nouveau taux de lecture, cet attribut spécifie si la source demande également une éclaircie. Pour obtenir une définition de la réduction, consultez à propos du contrôle du taux.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Attribut MF_EVENT_DO_THINNING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951296"
---
# <a name="mf_event_do_thinning-attribute"></a>\_Attribut de \_ fin d’événement MF \_

Quand une source de média demande un nouveau taux de lecture, cet attribut spécifie si la source demande également une éclaircie. Pour obtenir une définition de la réduction, consultez [à propos du contrôle du taux](about-rate-control.md).

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut est utilisé avec l’événement [MESourceRateChangeRequested](mesourceratechangerequested.md) . Si la valeur est **true**, la source du média demande un commutateur à une lecture fine.

La valeur par défaut est **FALSE**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs d'événement](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




