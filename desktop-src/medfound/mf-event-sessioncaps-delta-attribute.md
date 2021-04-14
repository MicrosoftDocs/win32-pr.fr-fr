---
description: Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Attribut MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393532"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_Attribut de \_ Delta SESSIONCAPS d’événement MF \_

Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut contient un masque de masque indiquant les fonctionnalités qui ont changé. Pour obtenir la liste des indicateurs possibles, consultez [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Les bits sont définis sur 1 dans le masque de bits pour l’une des raisons suivantes :

-   Le bit des fonctionnalités correspondant est passé de 0 à 1.
-   Le bit des fonctionnalités correspondant est passé de 1 à 0.
-   Le bit des fonctionnalités correspondant est resté 1, mais les détails de la fonctionnalité ont été modifiés. Par exemple, le taux de lecture maximal a changé.

Cet attribut est utilisé avec l’événement [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .

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

 

 




