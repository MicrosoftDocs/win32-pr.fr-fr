---
description: Spécifie les caractéristiques actuelles de la source du média.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Attribut MF_EVENT_SOURCE_CHARACTERISTICS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540827"
---
# <a name="mf_event_source_characteristics-attribute"></a>Attribut des caractéristiques de la \_ source d’événement MF \_ \_

Spécifie les caractéristiques actuelles de la source du média.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs de l’énumération des [**\_ caractéristiques MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

Cet attribut est utilisé avec l’événement [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .

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

 

 




