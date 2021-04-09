---
description: Spécifie si le moteur de capture capture la vidéo mais pas l’audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Attribut MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951544"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>\_ \_ \_ \_ Attribut appareil vidéo utiliser le moteur de capture MF \_ \_ uniquement

Spécifie si le moteur de capture capture la vidéo mais pas l’audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, le moteur de capture ne sélectionne pas ou n’utilise pas de périphérique de capture audio. Affectez la **valeur true** à cet attribut si vous souhaitez capturer une vidéo sans audio. La valeur par défaut est **FALSE**.

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

 

 




