---
description: Spécifie le paramètre de quantification (QP) pour l’encodage vidéo.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: CODECAPI_AVEncVideoEncodeQP, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512915"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>CODECAPI \_ propriété AVEncVideoEncodeQP

Spécifie le paramètre de quantification (QP) pour l’encodage vidéo.

## <a name="data-type"></a>Type de données

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valeur de la propriété

Ensemble de champs 4 16 bits utilisé pour spécifier le RPS de frame dans l’encodage Fixed-QP.

Les champs sont les suivants :

-   Bits 0-15 : QP par défaut
-   Bits 16-31 : QP utilisé pour les frames I
-   Bits 32-47 : QP utilisé pour les frames P
-   Bits 48-63 : QP utilisé pour les frames B

## <a name="remarks"></a>Notes

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

Pour garantir une utilisation cohérente entre différents encodeurs, vous devez supposer que les encodeurs n’examineront que le QP par défaut et peuvent ignorer les valeurs de QP pour les images I/P/B.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

