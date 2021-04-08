---
description: Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès vidéo du récepteur d’enregistrements.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752453"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a>Attribut du récepteur d’enregistrements du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ \_ échantillons traités

Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès vidéo du récepteur d’enregistrements.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

La valeur maximale de cet attribut est 17.

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

 

 




