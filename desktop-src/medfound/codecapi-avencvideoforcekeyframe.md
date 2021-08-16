---
description: Force l’encodeur à coder le frame suivant comme une image clé.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: CODECAPI_AVEncVideoForceKeyFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880705"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>CODECAPI \_ propriété AVEncVideoForceKeyFrame

Force l’encodeur à coder le frame suivant comme une image clé.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoForceKeyFrame**

## <a name="property-value"></a>Valeur de la propriété

Si la valeur est différente de zéro, l’encodeur encode le frame suivant comme une image clé. Si la valeur est égale à zéro, l’encodeur choisit s’il faut encoder le frame suivant comme une image clé.

Cette propriété s’applique au frame suivant que l’encodeur reçoit comme entrée. Pour une transformation de Media Foundation (MFT), il s’agit du frame suivant qui est passé à la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . Le paramètre se réinitialise à zéro après le frame suivant.

## <a name="remarks"></a>Remarques

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

