---
description: Cette rubrique explique comment utiliser MFPlay pour afficher un aperçu de la vidéo d’une caméra vidéo.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Aperçu de la vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516957"
---
# <a name="video-preview"></a>Aperçu de la vidéo

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Cette rubrique explique comment utiliser MFPlay pour afficher un aperçu de la vidéo d’une caméra vidéo.

MFPlay fournit la manière la plus simple de Microsoft Media Foundation pour afficher un aperçu de la vidéo à partir d’un appareil de capture. Vous devez utiliser MFPlay si les conditions suivantes sont vraies :

-   Vous n’avez pas besoin de capturer la vidéo dans un fichier.
-   Vous n’avez pas besoin d’un contrôle affiné sur la façon dont la vidéo est rendue. (Par exemple, vous n’avez pas besoin de contrôler la création du périphérique Direct3D.)
-   Vous n’avez pas besoin de traiter les données vidéo de l’appareil photo avant le rendu.

Dans le cas contraire, le [lecteur source](source-reader.md) peut être une meilleure option.

Pour utiliser MFPlay avec un périphérique de capture vidéo, procédez comme suit :

1.  Créez une source de média pour l’appareil de capture. Consultez [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).
2.  Appelez [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) pour créer une instance de l’objet Player.
3.  Appelez la méthode [**IMFPMediaPlayer :: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) . Transmettez un pointeur vers l’interface IMFMediaSource de la source du média. La méthode reçoit un pointeur vers l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) .
4.  Appelez [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  Appelez [**IMFPMediaPlayer ::P poser**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) pour commencer l’aperçu.

Le code suivant illustre ces étapes :


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



Dans une application classique, vous devez fournir un pointeur vers une interface de rappel dans la fonction [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) et utiliser l’interface de rappel pour obtenir des événements à partir du lecteur. Par souci de simplicité, le code présenté ici ignore ces étapes. Pour plus d’informations, consultez [prise en main avec MFPlay](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Arrêt en cours

Avant de quitter l’application, arrêtez la source du média et l’objet lecteur comme suit :

1.  Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sur la source du média.
2.  Appelez [**IMFPMediaPlayer :: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) sur l’objet Player.


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Capture vidéo](audio-video-capture.md)
</dt> </dl>

 

 



