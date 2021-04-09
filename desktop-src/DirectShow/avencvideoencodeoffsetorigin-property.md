---
description: Spécifie les angles gauche et supérieur du rectangle de découpage, si la vidéo est rognée.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propriété AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108986"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>Propriété AVEncVideoEncodeOffsetOrigin

Spécifie les angles gauche et supérieur du rectangle de découpage, si la vidéo est rognée.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>Valeur de la propriété

Les 16 bits supérieurs de la valeur contiennent le décalage par rapport au bord gauche du frame d’entrée, en pixels. Les 16 bits inférieurs contiennent le décalage par rapport au bord supérieur du frame d’entrée, en pixels.

## <a name="remarks"></a>Notes

Les applications peuvent définir cette propriété pour rogner la vidéo d’entrée. Utilisez la propriété [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) pour spécifier la largeur et la hauteur du rectangle de découpage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




