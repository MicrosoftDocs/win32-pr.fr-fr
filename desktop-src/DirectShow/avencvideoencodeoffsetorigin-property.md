---
description: Spécifie les angles gauche et supérieur du rectangle de découpage, si la vidéo est rognée.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propriété AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdc4ffd1f168fa98ce71937b5ddc22d429c573481575432e94964fdfc5205b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275759"
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

## <a name="remarks"></a>Remarques

Les applications peuvent définir cette propriété pour rogner la vidéo d’entrée. Utilisez la propriété [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) pour spécifier la largeur et la hauteur du rectangle de découpage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




