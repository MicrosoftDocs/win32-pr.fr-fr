---
description: Spécifie si le moteur de capture capture la vidéo mais pas l’audio.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Attribut MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd8dd903c4c56b52bf82a97b28edd5148e3c091788376f1ef460047b7f609b51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973968"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a>\_ \_ \_ \_ Attribut appareil vidéo utiliser le moteur de capture MF \_ \_ uniquement

Spécifie si le moteur de capture capture la vidéo mais pas l’audio.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Si cet attribut a la **valeur true**, le moteur de capture ne sélectionne pas ou n’utilise pas de périphérique de capture audio. Affectez la **valeur true** à cet attribut si vous souhaitez capturer une vidéo sans audio. La valeur par défaut est **FALSE**.

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

 

 




