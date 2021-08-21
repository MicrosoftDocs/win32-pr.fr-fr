---
description: Spécifie la largeur et la hauteur de la vidéo encodée, si la vidéo est rognée.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propriété AVEncVideoEncodeDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d99a0c14cbb3f67f7aa1c634a59c5f4cb9184dcd861bc8f14023c4afcebcefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159318"
---
# <a name="avencvideoencodedimension-property"></a>Propriété AVEncVideoEncodeDimension

Spécifie la largeur et la hauteur de la vidéo encodée, si la vidéo est rognée.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>Valeur de la propriété

Les 16 bits supérieurs de la valeur contiennent la largeur en pixels, et les 16 bits inférieurs contiennent la hauteur en pixels.

## <a name="remarks"></a>Remarques

Les applications peuvent définir cette propriété pour rogner la vidéo d’entrée. La taille spécifiée doit être inférieure à la taille des images vidéo d’entrée. Utilisez la propriété [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) pour spécifier les angles gauche et supérieur du rectangle de découpage.

Les encodeurs peuvent retourner cette propriété en tant que fonctionnalité.

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

Pour les encodeurs de caméra UVC 1,5, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) n’est pas pris en charge.

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

 

