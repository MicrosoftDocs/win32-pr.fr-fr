---
description: Identifie le nœud de topologie d’un récepteur de flux.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Attribut MF_EVENT_OUTPUT_NODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cbcbc243c195deb1061417adb6d93271b328fa242b497a7fdb232f5f7695e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244708"
---
# <a name="mf_event_output_node-attribute"></a>\_Attribut de \_ nœud de sortie d’événement MF \_

Identifie le nœud de topologie d’un récepteur de flux.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que [**TOPOID**](topoid.md).

## <a name="remarks"></a>Notes

La valeur de cet attribut est un identificateur de nœud pour un nœud de sortie sur la topologie actuelle. Pour obtenir un pointeur vers le nœud associé, appelez [**IMFTopology :: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) sur la topologie.

Cet attribut est utilisé avec les événements suivants :

-   [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)
-   [MESinkInvalidated](mesinkinvalidated.md)

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

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




