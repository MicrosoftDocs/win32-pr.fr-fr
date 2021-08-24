---
description: Spécifie le paramètre de quantification (QP) utilisé pour encoder un échantillon vidéo.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Attribut MFSampleExtension_VideoEncodeQP (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f86253b29dfa93b3699d5175b5c5ef198b4ab24e862901572caafcc55fd62d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777019"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a>\_Attribut MFSampleExtension VideoEncodeQP

Spécifie le paramètre de quantification (QP) utilisé pour encoder un échantillon vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Remarques

L' [**encodeur vidéo H. 264**](h-264-video-encoder.md) définit cet attribut sur les exemples de sortie qu’il génère.

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

 

 




