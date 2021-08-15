---
description: Indique si \_ l’attribut MFSampleExtension ROIRectangle défini sur l’exemple d’entrée sera respecté ou non.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: CODECAPI_AVEncVideoROIEnabled, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86185f6dbb9dfe16a84e7e85c3faddc8da3a7c1ead91dee2b1086e6fafa456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346979"
---
# <a name="codecapi_avencvideoroienabled-property"></a>CODECAPI \_ propriété AVEncVideoROIEnabled

Indique si l’attribut [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) défini sur l’exemple d’entrée sera respecté ou non.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Remarques

La valeur par défaut est 0.

Si un MFT d’encodeur accepte une valeur différente de zéro, il est supposé que l’encodeur honorera l’attribut [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) défini sur l’exemple d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




