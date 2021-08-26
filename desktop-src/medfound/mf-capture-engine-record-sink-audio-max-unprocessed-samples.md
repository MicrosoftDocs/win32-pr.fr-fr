---
description: Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès audio du récepteur d’enregistrements.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: Attribut MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5f6d2a2bcd592d5a6991028af90af008a827940903084054933558ed7088c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060829"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a>Attribut d’échantillonnage du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ échantillons non traités \_

Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès audio du récepteur d’enregistrements.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Remarques

Pour configurer cet attribut sur le moteur de capture, ajoutez-le au paramètre *pAttributes* lorsque vous appelez [**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).

La valeur maximale de cet attribut est 100.

Une fois que l’enregistrement a mis en mémoire tampon le nombre maximal d’échantillons non traités, spécifié par les échantillons du moteur de capture MF nombre maximal d’échantillons non \_ \_ \_ \_ \_ \_ \_ traités \_ , il supprime la fréquence d’images en supprimant des échantillons.

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

 

 




