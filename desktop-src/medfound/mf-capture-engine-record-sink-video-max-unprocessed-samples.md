---
description: Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès vidéo du récepteur d’enregistrements.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524253"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a>Vidéo du récepteur d’enregistrements du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ échantillons non traités \_

Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès vidéo du récepteur d’enregistrements.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

La valeur maximale de cet attribut est 17.

Une fois que l’enregistrement a mis en mémoire tampon le nombre maximal d’échantillons non traités, spécifié par le récepteur d’enregistrement du moteur de capture MF, nombre maximal d’échantillons non \_ \_ \_ \_ \_ \_ \_ traités \_ , il supprime la fréquence d’images en supprimant des échantillons.

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

 

 




