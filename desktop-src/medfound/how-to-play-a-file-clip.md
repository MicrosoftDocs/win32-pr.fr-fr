---
description: Cette rubrique explique comment lire un segment d’un fichier multimédia dans MFPlay, en définissant les heures de démarrage et d’arrêt pour la lecture.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Lecture d’un clip de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8773e2658d77b6c603e121d6498a8fb5235eec16d71726049d2d59ec1169f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061529"
---
# <a name="how-to-play-a-file-clip"></a>Lecture d’un clip de fichier

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Cette rubrique explique comment lire un segment d’un fichier multimédia dans MFPlay, en définissant les heures de démarrage et d’arrêt pour la lecture.

**Pour lire un clip**

1.  Appelez [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) ou [**IMFPMediaPlayer :: CreateMediaItemFromObject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) pour créer un élément multimédia pour le fichier.
2.  Si vous le souhaitez, vous pouvez connaître la durée totale du fichier, comme décrit dans [Comment faire pour connaître la durée de lecture](how-to-get-the-playback-duration.md).
3.  Appelez [**IMFPMediaItem :: SetStartStopPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) pour définir les heures de début et de fin. L’heure d’arrêt ne doit pas dépasser la durée du fichier.
4.  Appelez [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) pour démarrer la lecture.

L’exemple suivant utilise la version de blocage de [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl). Si la version non bloquante est utilisée, le code qui apparaît après **CreateMediaItemFromURL** doit être placé dans le gestionnaire pour le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ created** Event. Pour plus d’informations sur les événements dans MFPlay, consultez [réception d’événements à partir du lecteur](getting-started-with-mfplay.md).

Pour connaître la durée du fichier, cet exemple appelle la `GetPlaybackDuration` fonction indiquée dans la rubrique [Comment faire pour connaître la durée de lecture](how-to-get-the-playback-duration.md).


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



