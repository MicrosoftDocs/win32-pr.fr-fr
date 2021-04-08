---
description: GUID de sous-type pour un type de média.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Attribut MF_MT_SUBTYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034589"
---
# <a name="mf_mt_subtype-attribute"></a>\_Attribut de \_ sous-type MF MT

GUID de sous-type pour un type de média.

## <a name="data-type"></a>Type de données

**GUID**

## <a name="remarks"></a>Notes

Le GUID de sous-type définit un type de format de média spécifique dans un type principal. Par exemple, dans la vidéo, les sous-types sont RVB-24, RVB-32, UYVY, AYUV, et ainsi de suite. Dans l’audio, les sous-types incluent l’audio PCM, le Windows Media Audio 9, et ainsi de suite.

Pour connaître les valeurs possibles, consultez les rubriques suivantes :

-   [GUID de sous-type audio](audio-subtype-guids.md)
-   [GUID de sous-type de vidéo](video-subtype-guids.md)

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes :: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




