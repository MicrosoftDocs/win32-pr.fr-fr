---
description: Spécifie si le moteur de capture capture l’audio mais pas la vidéo.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Attribut MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951298"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a>\_ \_ \_ \_ \_ Attribut appareil audio \_ de l’utilisation du moteur de capture MF uniquement

Spécifie si le moteur de capture capture l’audio mais pas la vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, le moteur de capture ne sélectionne pas ou n’utilise pas d’appareil de capture vidéo. Affectez la **valeur true** à cet attribut si vous souhaitez capturer du son sans vidéo. La valeur par défaut est **FALSE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du moteur de capture](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




