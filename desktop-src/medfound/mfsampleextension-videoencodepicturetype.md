---
description: Spécifie le type d’image qui est sortie par un encodeur vidéo.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Attribut MFSampleExtension_VideoEncodePictureType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519585"
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

## <a name="remarks"></a>Notes

L' [**encodeur vidéo H. 264**](h-264-video-encoder.md) définit cet attribut sur les exemples de sortie qu’il génère. La valeur de l’attribut est un membre de l’énumération [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
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

 

 




