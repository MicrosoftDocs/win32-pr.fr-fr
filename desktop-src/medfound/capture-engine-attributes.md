---
description: Les attributs suivants peuvent être utilisés pour configurer le moteur de capture.
ms.assetid: C153F0AD-4E8B-41DA-B7FB-8D10AC20D22E
title: Attributs du moteur de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1340fa69f80d456a29331d303f313d41c31ee41
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "106539148"
---
# <a name="capture-engine-attributes"></a>Attributs du moteur de capture

Les attributs suivants peuvent être utilisés pour configurer le moteur de capture.

Les attributs suivants sont liés aux appareils de capture :



| Attribut                                                                                                                              | Description                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [\_flux d' \_ appareil photo du moteur de capture MF \_ \_ \_ bloqué](mf-capture-engine-camera-stream-blocked.md)                                            | Signale que la capture vidéo est bloquée par le pilote.                                                         |
| [\_flux d' \_ appareil photo du moteur de capture MF \_ \_ \_ débloqué](mf-capture-engine-camera-stream-unblocked.md)                                        | Signale que la capture vidéo est restaurée après avoir été bloquée.                                                        |
| [\_ \_ Gestionnaire D3D du moteur de capture MF \_ \_](mf-capture-engine-d3d-manager.md)                                                                 | Définit un pointeur vers le Gestionnaire de périphériques DXGI sur le moteur de capture.                                                   |
| [décodeur du moteur de capture MF- \_ \_ \_ attribut de \_ \_ \_ déverrouillage FIELDOFUSE MFT \_](mf-capture-engine-decoder-mft-fieldofuse-unlock-attribute.md)      | Permet au moteur de capture d’utiliser un décodeur qui a des restrictions de champ d’utilisation.                                    |
| [moteur de capture MF- \_ \_ \_ désactiver \_ DXVA](mf-capture-engine-disable-dxva.md)                                                               | Spécifie si le moteur de capture utilise l’accélération vidéo DirectX (DXVA) pour le décodage vidéo.                    |
| [les \_ \_ \_ transformations matérielles de désactivation de capture MF \_](mf-capture-engine-disable-hardware-transforms.md)                                        | Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.                       |
| [le \_ moteur de capture MF \_ active la \_ \_ \_ notification STREAMSTATE de l’appareil photo \_](mf-capture-engine-enable-camera-streamstate-notification.md)         | Indique si les notifications d’état de flux doivent être activées.                                                    |
| [\_attribut de \_ \_ \_ \_ \_ déverrouillage FIELDOFUSE MFT de l’encodeur du moteur de capture \_ MF](mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute.md)      | Permet au moteur de capture d’utiliser un encodeur qui a des restrictions de champ d’utilisation.                                   |
| [\_GUID du \_ Générateur d’événements du moteur de capture MF \_ \_ \_](mf-capture-engine-event-generator-guid.md)                                              | Identifie le composant qui a généré un événement de capture.                                                           |
| [\_index du \_ flux d’événements du moteur de capture MF \_ \_ \_](mf-capture-engine-event-stream-index.md)                                                  | Identifie le flux qui a généré un événement de capture.                                                                 |
| [configuration de la MEDIASOURCE du moteur de \_ capture MF \_ \_ \_](mf-capture-engine-mediasource-config.md)                                                   | Contient les propriétés de configuration de la source de capture.                                                          |
| [\_exemples de \_ \_ \_ \_ \_ traitement audio maximal \_ du récepteur \_ d’enregistrements du moteur de capture MF](mf-capture-engine-record-sink-audio-max-processed-samples.md)     | Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès audio du récepteur d’enregistrements.                   |
| [échantillons du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ échantillons non traités \_](mf-capture-engine-record-sink-audio-max-unprocessed-samples.md) | Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès audio du récepteur d’enregistrements. |
| [\_exemples de vidéo du récepteur d’enregistrements du moteur de capture MF \_ \_ \_ \_ \_ Max \_ processed \_](mf-capture-engine-record-sink-video-max-processed-samples.md)     | Définit le nombre maximal d’exemples traités qui peuvent être mis en mémoire tampon dans le chemin d’accès vidéo du récepteur d’enregistrements.                   |
| [vidéo du récepteur d’enregistrements du moteur de capture MF- \_ \_ \_ \_ \_ \_ nombre maximal d' \_ échantillons non traités \_](mf-capture-engine-record-sink-video-max-unprocessed-samples.md) | Définit le nombre maximal d’échantillons non traités qui peuvent être mis en mémoire tampon pour traitement dans le chemin d’accès vidéo du récepteur d’enregistrements.  |
| [\_type de \_ récepteur du moteur de capture MF \_ \_](/windows/desktop/api/mfcaptureengine/ne-mfcaptureengine-mf_capture_engine_sink_type)                                                                     | Spécifie un type de récepteur de capture.                                                                                  |
| [moteur de capture MF- \_ \_ \_ utiliser \_ \_ uniquement le périphérique audio \_](mf-capture-engine-use-audio-device-only.md)                                           | Spécifie si le moteur de capture capture l’audio mais pas la vidéo.                                                 |
| [moteur de capture MF- \_ \_ \_ utiliser \_ \_ uniquement un périphérique vidéo \_](mf-capture-engine-use-video-device-only.md)                                           | Spécifie si le moteur de capture capture la vidéo mais pas l’audio.                                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureEngine :: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 



