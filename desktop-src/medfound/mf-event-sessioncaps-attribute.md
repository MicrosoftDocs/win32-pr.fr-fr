---
description: Contient des indicateurs qui définissent les fonctionnalités de la session multimédia, en fonction de la présentation actuelle.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: Attribut MF_EVENT_SESSIONCAPS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175c81d1cc231204060a63a90ffe9e2432b73bdec35c7885dea203416995ea92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973788"
---
# <a name="mf_event_sessioncaps-attribute"></a>\_ \_ Attribut SESSIONCAPS de l’événement MF

Contient des indicateurs qui définissent les fonctionnalités de la session multimédia, en fonction de la présentation actuelle.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut contient une opération **de bits or** de zéro, un ou plusieurs indicateurs. Pour obtenir la liste des indicateurs possibles, consultez [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).

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

 

 




