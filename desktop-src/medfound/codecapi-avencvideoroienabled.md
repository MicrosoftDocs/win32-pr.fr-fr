---
description: Indique si \_ l’attribut MFSampleExtension ROIRectangle défini sur l’exemple d’entrée sera respecté ou non.
ms.assetid: 6B3CB513-43E8-4D30-B5A0-CD2E9C9F46BA
title: CODECAPI_AVEncVideoROIEnabled, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345e6ba27a983be910f0dc0ea5d3db34191bdcb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317998"
---
# <a name="codecapi_avencvideoroienabled-property"></a>CODECAPI \_ propriété AVEncVideoROIEnabled

Indique si l’attribut [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) défini sur l’exemple d’entrée sera respecté ou non.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoROIEnabled**

## <a name="remarks"></a>Notes

La valeur par défaut est 0.

Si un MFT d’encodeur accepte une valeur différente de zéro, il est supposé que l’encodeur honorera l’attribut [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md) défini sur l’exemple d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




