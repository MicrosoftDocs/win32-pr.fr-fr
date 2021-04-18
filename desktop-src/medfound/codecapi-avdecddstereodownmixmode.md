---
description: Spécifie le mode stéréo downmix pour un décodeur audio Dolby Digital.
ms.assetid: 270893C6-8B44-4A4D-AE2B-2E58E260F649
title: CODECAPI_AVDecDDStereoDownMixMode, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7caaed1af804e22b3ec6085241746bdf01eb7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393303"
---
# <a name="codecapi_avdecddstereodownmixmode-property"></a>CODECAPI \_ propriété AVDecDDStereoDownMixMode

Spécifie le mode stéréo downmix pour un décodeur audio Dolby Digital.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecDDStereoDownMixMode**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVDecDDStereoDownMixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecddstereodownmixmode) .

## <a name="remarks"></a>Notes

Cet attribut s’applique lorsque l’entrée dans le décodeur est un fichier audio PCM Multichannel, et la sortie est de l’audio stéréo.

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

 

