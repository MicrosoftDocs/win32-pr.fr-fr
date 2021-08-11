---
description: Important déconseillé.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Exemple MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ead2df415af1584f34661a0c1d18751350d59bd1a94ac48f41d3bf9dca2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241729"
---
# <a name="mfplayer2-sample"></a>Exemple MFPlayer2

> [!IMPORTANT]
> Action déconseillée. Cette API peut être supprimée des futures versions de Windows. Les applications doivent utiliser la [session multimédia](media-session.md) pour la lecture.

 

Présente certaines des fonctionnalités de lecture qui sont omises de l’exemple [SimplePlay](simpleplay-sample.md) , par exemple :

-   Cherche
-   Contrôle du taux (avance rapide et rembobinage)
-   Contrôles de volume audio et de sourdine
-   Zoom vidéo

L’illustration suivante montre les contrôles utilisés pour ces fonctionnalités.

![capture d’écran de l’exemple mfplayer ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les API suivantes.

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**IAudioSessionManager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

cet exemple est disponible dans [Windows le référentiel github exemples classiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
