---
description: Spécifie le type d’image qui est sortie par un encodeur vidéo.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Attribut MFSampleExtension_VideoEncodePictureType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be87284be3b605e3af70d64df98e5d762aa7cc353bb83b5f61a110d1242ae1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973168"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>\_Attribut MFSampleExtension VideoEncodePictureType

Spécifie le type d’image qui est sortie par un encodeur vidéo.

## <a name="data-type"></a>Type de données

**eAVEncH264PictureType \_ B** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarques

L' [**encodeur vidéo H. 264**](h-264-video-encoder.md) définit cet attribut sur les exemples de sortie qu’il génère. La valeur de l’attribut est un membre de l’énumération [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Encodeur vidéo H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 




