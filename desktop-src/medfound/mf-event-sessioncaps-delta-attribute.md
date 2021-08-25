---
description: Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Attribut MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714840"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_Attribut de \_ Delta SESSIONCAPS d’événement MF \_

Contient des indicateurs qui indiquent les fonctionnalités qui ont changé dans la session multimédia, en fonction de la présentation actuelle.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut contient un masque de masque indiquant les fonctionnalités qui ont changé. Pour obtenir la liste des indicateurs possibles, consultez [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Les bits sont définis sur 1 dans le masque de bits pour l’une des raisons suivantes :

-   Le bit des fonctionnalités correspondant est passé de 0 à 1.
-   Le bit des fonctionnalités correspondant est passé de 1 à 0.
-   Le bit des fonctionnalités correspondant est resté 1, mais les détails de la fonctionnalité ont été modifiés. Par exemple, le taux de lecture maximal a changé.

Cet attribut est utilisé avec l’événement [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
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

 

 




