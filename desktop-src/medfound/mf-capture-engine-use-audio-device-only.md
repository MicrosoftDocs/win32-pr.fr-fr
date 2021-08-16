---
description: Spécifie si le moteur de capture capture l’audio mais pas la vidéo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Attribut MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c248923ae2dce7d5153f8e88cb8eef88d29ea3dbf6ce5c94e4a8ee355af16c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013349"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>\_ \_ \_ \_ \_ Attribut appareil audio \_ de l’utilisation du moteur de capture MF uniquement

Spécifie si le moteur de capture capture l’audio mais pas la vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Si cet attribut a la **valeur true**, le moteur de capture ne sélectionne pas ou n’utilise pas d’appareil de capture vidéo. Affectez la **valeur true** à cet attribut si vous souhaitez capturer du son sans vidéo. La valeur par défaut est **FALSE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du moteur de capture](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




